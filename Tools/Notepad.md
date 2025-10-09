---
tags:
  - Notepad
---
# Notepad

## Checks

> *<font color="#7f7f7f">Some quick checklists I can work through whilst playing the game. Feel free to change these with what works best for you.</font>*

> [!kirk|sessionstart]- Before Session
> - [ ] **Give Hero Points**
> - [ ] **Create new Session Note**
>     - Set properties
> - **Reset**

> [!kirk|travel]- Travel
> - [ ] **Encounter?**
> - [ ] **Cool Locations?**
> - [ ] **Conversations?**
> - [ ] **<font color="#ff0000">Travel through the night?</font>**  `BUTTON[Next-Day]`
> - **Reset**

> [!kirk|longrest]- Long Rest
> - [ ] **Night Events?**
> - [ ] **Dream?**
> - [ ] **<font color="#ff0000">New Day?</font>**  `BUTTON[Next-Day]`
> - [ ] **Healing**
> - [ ] **Spell Prep/ Restore**
> - [ ] **<font color="#ff0000">Eat</font>**
> - **Reset**

> [!kirk|aftersession]- After Session
> - [ ] **Update Session Note Properties**
>     - End Date
>     - Summary
> - [ ] **Check Notes**
> - [ ] **Create/ Move to permanent Notes**
> - [ ] **Check Upcoming Calendar Dates**
> - [ ] **Check Upcoming Planner Events**
> - **Reset**

## Quick References

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


## To-Do

> *<font color="#7f7f7f">A place I can throw down things I need to do so I don't forget.</font>*

-  

## Planner
### Coming up

> *<font color="#7f7f7f">Events that are coming up in the next few sessions I am planning for.</font>*

### Down the line

> *<font color="#7f7f7f">Events that I have planned for down the line, but aren't an immediate concern.</font>*

### Future

> *<font color="#7f7f7f">Plans for the future of the campaign, something I can put on the backburner but come back to.</font>*

## Random Events

> *<font color="#7f7f7f">When things go off course, I like to have a few ticks up my sleeve. So I put a few random events here that I can throw at my party if I need to.</font>*

## Player's Personal Goals

> *<font color="#7f7f7f">Every now and then I check in with my players and find out what their character's personal goals are. Then I note them here so I can work ways in the story I can help them achieve them.</font>*

## Random


