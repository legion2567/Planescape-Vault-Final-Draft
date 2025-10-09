---
tags:
  - VaultHub
time: 304527
dpy: "364"
dpm: "28"
---

# Vault Hub

> [!kirk|info] Guide
> **PLEASE** use the ➡️ [[README]] ⬅️, it answers a lot of common questions you may have and introduces you to the vault.
> 
> **WARNING: If you are going to update your Obsidian version or the plugins, please read [[README#Don't want things to break?]]**
> 
> Everyone's Hub is different, I have given you some tools to get you started. Make it your own!

## Parties

![[Database - Parties.base]]

## Calendar

```calendarium
calendar: Aranor
```


> *<font color="#7f7f7f">A small bit of JavaScript lives under here to help run character age calculations. This code works with an example calendar within the Calendarium plugin that has 364 days (dpy) and 28 days per month (dpm) per year. You are welcome to adapt this to your own calendars, but could become tricky if you have leap years or other such variables in your calendar.</font>*

~~~js-engine
const calendarAPI = Calendarium.getAPI("Example Calendar");
const currentDate = calendarAPI.getCurrentDate()
const time = 364*(currentDate.year)+28*(currentDate.month)+currentDate.day

app.fileManager.processFrontMatter(context.file, (frontmatter) => { frontmatter.time = time; })
//return currentDate//
~~~

## Websites

> *<font color="#7f7f7f">I have left my links down here as examples of how you could use your Hub.</font>*

> [!grid|col-3]
> > [!kirk|rules]- Rules
>> - [Demiplane](https://app.demiplane.com/nexus/pathfinder2e)
>> - [Archives of Nethys](https://2e.aonprd.com)
> 
> > [!kirk|generators]- Generators
>> - [D&D Name Generator](https://www.fantasynamegenerators.com/dungeons-and-dragons.php)
>> - [Pf2e Name Generator](https://www.fantasynamegenerators.com/pathfinder.php)
>> - [City Generator](https://watabou.github.io/city-generator)
>> - [Neighbourhood Generator](https://watabou.github.io/neighbourhood)
>> - [Village Generator](https://watabou.github.io/village-generator)
> 
> > [!kirk|tools]- Other
>> - [Pf2e Encounter Builder](https://maxiride.github.io/pf2e-encounters/#/)

## Note Management

![[Database - Note Management.base]]

