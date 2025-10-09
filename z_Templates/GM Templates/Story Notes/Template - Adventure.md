---
tags:
  - "#Adventure"
aliases:
whichParty:
completed: false
summary:
---

# `=this.file.name`

> [!grid|col-2]
> **Assigned Party:**  `VIEW[{whichParty}][link]`
>
> **Status:**  `INPUT[toggle:completed]`

> <font color="#7f7f7f">Summarize the overarching adventure, outlining its main premise, goals, and the central conflicts or journey that drives it.</font>

## Database

![[Database - Adventure Note.base]]

## Overview

### Quick References

> [!grid|col-3]
>> **Characters**
>> ```dataview
>> LIST
>> FROM outgoing([[]])
>> WHERE econtains(tags,"Character")
>> SORT file.name ASC
>> ```
> 
>> **Locations**
>> ```dataview
>> LIST
>> FROM outgoing([[]])
>> WHERE econtains(tags,"Location")
>> SORT file.name ASC
>> ```
> 
>> **Organizations**
>> ```dataview
>> LIST
>> FROM outgoing([[]])
>> WHERE econtains(tags,"Organization")
>> SORT file.name ASC
>> ```

### Plot:

> <font color="#7f7f7f">Describe the main plot of the adventure, detailing the central storyline, major conflicts, and the path players are expected to follow.</font>

## Acts

### [[Template - Quest]]
#### Summary:

> <font color="#7f7f7f">Summarize the key events that occurred during the quest or a major story point.</font>

#### Outcomes:

> <font color="#7f7f7f">Summarise the outcomes of the quest or major story point, noting how it advances or resolves this adventure.</font>

### [[Template - Quest]]
#### Summary:

> <font color="#7f7f7f">Summarize the key events that occurred during the quest or a major story point.</font>

#### Outcomes:

> <font color="#7f7f7f">Summarise the outcomes of the quest or major story point, noting how it advances or resolves this adventure.</font>

## Notes