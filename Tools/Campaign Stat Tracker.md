---
tags:
  - StatTracker
---

# Campaign Stat Trackers

## NPCs

### Ancestries

~~~dataview
TABLE WITHOUT ID
  A as "Ancestry",
  length(rows) as "Count"
FROM "Campaign/Characters"
WHERE ancestry
FLATTEN ancestry AS A
GROUP BY A
SORT length(rows) DESC
~~~

### Heritages

~~~dataview
TABLE WITHOUT ID
  A as "Heritage",
  length(rows) as "Count"
FROM "Campaign/Characters"
WHERE heritage
FLATTEN heritage AS A
GROUP BY A
SORT length(rows) DESC
~~~

### Genders

~~~dataview
TABLE WITHOUT ID
  A as "Gender",
  length(rows) as "Count"
FROM "Campaign/Characters"
WHERE gender
FLATTEN gender AS A
GROUP BY A
SORT length(rows) DESC
~~~

### Sexualities

~~~dataview
TABLE WITHOUT ID
  A as "Sexuality",
  length(rows) as "Count"
FROM "Campaign/Characters"
WHERE sexuality
FLATTEN sexuality AS A
GROUP BY A
SORT length(rows) DESC
~~~

### Religions

~~~dataview
TABLE WITHOUT ID
  A as "Religion",
  length(rows) as "Count"
FROM "Campaign/Characters"
WHERE religions
FLATTEN religions AS A
GROUP BY A
SORT length(rows) DESC
~~~


### Occupations

~~~dataview
TABLE WITHOUT ID
  A as "Occupation",
  length(rows) as "Count"
FROM "Campaign/Characters"
WHERE occupation
FLATTEN occupation AS A
GROUP BY A
SORT length(rows) DESC
~~~

## Locations

### Point of Interest Types

~~~dataview
TABLE WITHOUT ID
  A as "Point of Interest",
  length(rows) as "Count"
FROM "Campaign/Points of Interest"
WHERE poiType
FLATTEN poiType AS A
GROUP BY A
SORT length(rows) DESC
~~~
