~~~dataviewjs
/**** CONFIG ****/
const DATE_FIELD = "sessionDate";   // MM/DD/YYYY
const NUM_FIELD  = "session";       // integer

/**** HOST CONTEXT (works when this note is transcluded) ****/
const host = app?.workspace?.getActiveFile();
const HOST_PATH   = host?.path ?? null;
const HOST_FOLDER = host?.parent?.path ? host.parent.path + "/" : null;

/**** If we can't detect the host, do nothing ****/
if (HOST_PATH && HOST_FOLDER) {

  /**** HELPERS ****/
  const NAME_NUM_REGEX = /(?:^|[^0-9])(\d{1,4})(?!\d)/;
  const toMoment = v => {
    if (!v) return null;
    const m = moment(v, "MM/DD/YYYY", true);
    return m.isValid() ? m : null;
  };
  const getNum = p => {
    if (p[NUM_FIELD] != null) return Number(p[NUM_FIELD]);
    const m = p.file.name.match(NAME_NUM_REGEX);
    return m ? Number(m[1]) : NaN;
  };

  /**** COLLECT (include ALL session notes in the host folder) ****/
  const rows = dv.pages()
    .where(p => p.file.path.startsWith(HOST_FOLDER))
    .array()
    .map(p => ({ page: p, d: toMoment(p[DATE_FIELD]), n: getNum(p) }));

  /**** SORT: by date (if present), then session #, then filename ****/
  rows.sort((a, b) => {
    if (a.d && b.d) return a.d.diff(b.d);
    if (a.d && !b.d) return -1;
    if (!a.d && b.d) return 1;
    const aN = Number.isNaN(a.n), bN = Number.isNaN(b.n);
    if (!aN && !bN) return a.n - b.n;
    if (!aN && bN) return -1;
    if (aN && !bN) return 1;
    return a.page.file.name.localeCompare(b.page.file.name, undefined, { numeric: true });
  });

  /**** FIND CURRENT (by host path) ****/
  const idx  = rows.findIndex(x => x.page.file.path === HOST_PATH);
  const prev = (idx > 0) ? rows[idx - 1] : null;
  const next = (idx >= 0 && idx < rows.length - 1) ? rows[idx + 1] : null;

  /**** LABELS ****/
  const label = x => {
    if (!x) return "";
    if (!Number.isNaN(x.n)) return `Session ${String(x.n).padStart(3, "0")}`;
    const m = x.page.file.name.match(NAME_NUM_REGEX);
    return m ? `Session ${String(m[1]).padStart(3, "0")}` : x.page.file.name;
  };

  /**** BUILD WRAPPER + BUTTONS ****/
  const wrapper = document.createElement("div");
  wrapper.className = "breadcrumbs-wrapper";
  const aPrev = document.createElement("a");
  aPrev.className = "internal-link elegant-btn";
  const aNext = document.createElement("a");
  aNext.className = "internal-link elegant-btn";
  wrapper.appendChild(aPrev);
  wrapper.appendChild(aNext);
  this.container.appendChild(wrapper);

  /**** WIRE LINKS ****/
  let hasPrev = false, hasNext = false;

  if (prev) {
    aPrev.textContent = `‹ ${label(prev)}`;
    aPrev.setAttribute("href", prev.page.file.path);
    hasPrev = true;
  } else {
    aPrev.style.display = "none";
  }

  if (next) {
    aNext.textContent = `${label(next)} ›`;
    aNext.setAttribute("href", next.page.file.path);
    hasNext = true;
  } else {
    aNext.style.display = "none";
  }

  /**** EXPLICIT ALIGNMENT PER CASE ****/
  if (hasPrev && hasNext) {
    wrapper.style.justifyContent = "space-between"; // middle sessions
  } else if (hasPrev && !hasNext) {
    wrapper.style.justifyContent = "flex-start";    // last session -> left
  } else if (!hasPrev && hasNext) {
    wrapper.style.justifyContent = "flex-end";      // first session -> right
  } else {
    wrapper.style.justifyContent = "center";        // fallback (no neighbors)
  }

  /**** STYLES ****/
  const styles = `
  .breadcrumbs-wrapper {
    display:flex;
    align-items:center;
    gap:1rem;
    margin-top:1.5rem;
  }
  .elegant-btn {
    color: var(--text-normal);
    text-decoration: none;
    font-size: 14px;
    padding: 4px 18px;
    border: 2px solid var(--text-normal);
    background: transparent;
    box-shadow: 8px 8px 0 0 var(--text-normal);
    transition: box-shadow .2s ease;
  }
  .elegant-btn:hover { box-shadow: 0 0 0 0 var(--text-normal); }
  `;
  const styleEl = document.createElement("style");
  styleEl.textContent = styles;
  this.container.appendChild(styleEl);
}
