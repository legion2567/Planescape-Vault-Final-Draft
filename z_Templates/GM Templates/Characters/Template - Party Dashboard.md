---
tags:
  - Party
art:
aliases:
partyID:
---

# `=this.file.name`

## Current Party

![[Database - Party Members.base]]

### Known Party Languages

~~~dataview
TABLE WITHOUT ID
  A as "Language",
  rows.file.link as "Spoken By"
FROM "Campaign/Characters"
WHERE econtains(whichParty, this.file.link) AND languages
FLATTEN languages AS A
GROUP BY A
SORT length(rows) DESC
~~~

## Individual Relations

> [!metadata|info] Guide
> Due to the nature of parties changing their name after so many sessions after starting, for simplicity, we use the property of Party1, Party2, etc.
> Because of this, you will need to make a unique relations database for each new party.
>
> I have included the first (Party1) as an example.

![[Database - Party 1 Relations.base]]

## Story

![[Database - Story.base]]

## Notes

