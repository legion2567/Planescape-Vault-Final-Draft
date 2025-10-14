---
tags:
  - SessionNote
aliases:
whichParty:
sessionDate:
recapPlayer:
fc-calendar: Example Calendar
fc-category: Session Notes
fc-date: YYYY-MM-DD
fc-end: YYYY-MM-DD
summary: ""
campaign:
linkedAdventure:
sessionNumber:
---

# `=this.file.name`

> [!kirk|info] Session HUD
> **#**: =this.sessionNumber &nbsp;•&nbsp; **Date**: =this.sessionDate &nbsp;•&nbsp; **Party**: =this.whichParty  
> **Campaign**: =this.campaign &nbsp;•&nbsp; **Adventure**: =this.linkedAdventure &nbsp;•&nbsp; **Recap by**: =this.recapPlayer

> [!tip] Session Toolbar
> ```button
> name: ➕ New Scene Block
> type: append_template
> action: Template - Scene Block
> templater: true
> ```
> ```button
> name: ➡️ Append Idea → Future Session Ideas
> type: command
> action: QuickAdd: Append to Future Ideas
> ```

## Quick References
> [!grid|col-3]
>> ##### Characters
>> ```dataview
>> LIST
>> FROM outgoing([[]])
>> WHERE econtains(tags,"Character")
>> SORT file.name ASC
>> ```
>
>
>> ##### Locations
>> ```dataview
>> LIST
>> FROM outgoing([[]])
>> WHERE econtains(tags,"Location")
>> SORT file.name ASC
>> ```
>
>
>> ##### Organizations
>> ```dataview
>> LIST
>> FROM outgoing([[]])
>> WHERE econtains(tags,"Organization")
>> SORT file.name ASC
>> ```

---

## Recap — *Last Time on Turn of Fortune’s Wheel…*
> [!summary]+ What happened previously
> - *(Bullet the key beats, outcomes, cliffhangers.)*
> - *(Note unresolved threads you want to pick up now.)*

---

## Pre-Session Brainstorm
> [!grid|col-2]
>> **Today’s highlights to aim for**
>> - [ ] 
>> - [ ] 
>> - [ ] 
>>
>> **Not for today → move to [[Future Session Ideas]]**
>> - [ ] 
>> - [ ] 

> [!tip]- Browse & mine prior ideas (embedded)
> ![[Future Session Ideas]]

---

## Loose Structure (High-Speed Checklist)
> [!abstract]
> - [ ] **S-1:** *Scene name* — **Purpose/Stakes:** … — **What they see:** … — **Key DCs:** … — **NPCs/Enemies:** … — **Loot/Clues:** …
> - [ ] **S-2:** *Scene name* — **Purpose/Stakes:** … — **What they see:** … — **Key DCs:** … — **NPCs/Enemies:** … — **Loot/Clues:** …
> - [ ] **S-3:** *Scene name* — **Purpose/Stakes:** … — **What they see:** … — **Key DCs:** … — **NPCs/Enemies:** … — **Loot/Clues:** …
> - [ ] **Fallback:** *Backup beat if pacing shifts*

> [!abstract]- Optional PC Goals quick glance
> - **PC:** *Goal* → *Today’s nudge/beat*
> - **PC:** *Goal* → *Today’s nudge/beat*

---

## Detailed Scenes

> [!summary]- Scene Index (update as you add scenes)
> - [[#scene-1--title-placeholder|Scene 1 — Title Placeholder]]
> - [[#scene-2--title-placeholder|Scene 2 — Title Placeholder]]

### Scene 1 — *Title Placeholder*
> [!grid|col-2]
>> #### Read-Aloud & Intent
>> **Location:**  
>> **Encounter Vibe:**  
>>
>> > [!note] 🎵 **Scene Music:** 
>>
>> **Read-Aloud:**  
>> > “*Boxed text here…*”
>>
>> **Purpose / Why it matters / What’s going down**
>> - 
>>
>> **Sensory Snapshot (What they see/feel/hear)**
>> - 
>>
>> > [!quote]- Visual / Map (optional)
>> > *Drop an image or map here for quick reference.*  
>> > ![[<drag-image-or-map-here>]]
>
>> #### Mechanics & Fallout
>> **Skill Checks / Interactive Elements**
>>
>> | DC | Check | Success / Failure | Effects |
>> | ---: | --- | --- | --- |
>> |  |  |  |  |
>> |  |  |  |  |
>>
>> **NPCs / Creatures present**
>> - **Name** – 3-word hook, p.# stat ref
>>
>> **Loot / Clues Awarded**
>> - 
>>
>> **Faction / Glitch Repercussion**  
>> *Mark if this scene nudges the Planar chessboard or triggers a Glitch Shift.*
>>
>> **DM Note:** 

---

## Session Notes
- 

---

## Post-Session Wrap-Up
> [!grid|col-2]
>> **Quick Recap (bullets)**
>>
>> - 
>>
>> **NPCs involved & new relationships**
>>
>> - 
>
>
>> **Clues / Items / Gold — gained & spent**
>>
>> **Gained**
>> - **Clues** — 
>> - **Items** —
>> - **Gold**  —
>>
>> **Spent / Lost**
>> - **Clues** —
>> - **Items** —
>> - **Gold**  —
>>
>> **Outcomes / Consequences**
>> - 

**PC To-Do (next prep cycle)**
- [ ]  #prep
- [ ]  #prep

> [!note]- DM Thoughts & Next Hooks
> *(free-write reflections, pacing notes, cliff-hangers, repairs)*

---

## Next Session Reminders
- 
