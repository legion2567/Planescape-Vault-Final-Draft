---
tags:
  - TravelCalculator
MilesPerHour: 4
SpeedMultiplier: 1
TemperatureMaxTravelHours: 8
HoursPerDay: 8
TravelDistance: 12
MinutesInDay: "1440"
---
# Travel Speed

> *<font color="#7f7f7f">This is linked to Settlements and PoI notes to calculate travel times.</font>*
> 
> *<font color="#7f7f7f">This is setup for the Pf2e system, if you need different speeds, you will need to set that up.</font>

> [!kirk|info] Video Tutorial
> NOTE: This method still works, but the vault now uses a better way to manage your maps. A tutorial on this will be developed soon, so please look out for that!
>
> <center><iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/8MI5JyiH-Wo?si=G-lpyB0tK_I479FF" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></center>

| PF2e Travel Calculator                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Party Speed (slowest):** `INPUT[inlineSelect(option(1, 10 Feet), option(1.5, 15 Feet), option(2, 20 Feet), option(2.5, 25 Feet),  option(3, 30 Feet),  option(3.5, 35 Feet),  option(4, 40 Feet),  option(5, 50 Feet),  option(6, 60 Feet)):MilesPerHour]`                                                                                                                                                                                                                                            |
| **Terrain Type:** `INPUT[inlineSelect(option(1, Normal Terrain), option(0.5, Difficult Terrain), option(0.333333, Greater Difficult Terrain)):SpeedMultiplier]`                                                                                                                                                                                                                                                                                                                                         |
| **Temperature:** `INPUT[inlineSelect(option(2, Incredible Cold - Moderate dmg every minute), option(4, Extreme Cold - Minor cold dmg every 10 minutes), option(4, Severe Cold - Minor cold dmg every hour), option(4, Mild Cold - None), option(8, Normal - None), option(4, Mild Heat - None), option(4, Severe Heat - Minor fire dmg every hour), option(4, Extreme Heat - Minor fire dmg every 10 minutes), option(2, Incredible Heat - Moderate fire dmg every minute)):TemperatureMaxTravelHours]` |
| **Max Travel Hours Per Day:** `VIEW[round({TemperatureMaxTravelHours},1)]`                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **Travel Hours Per Day:** `INPUT[number:HoursPerDay]` `VIEW[{HoursPerDay}>{TemperatureMaxTravelHours} ? "Suffer Fatigue" : "No Fatigue"]`                                                                                                                                                                                                                                                                                                                                                               |
| **Miles To Travel:**  `INPUT[number:TravelDistance]`                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Distance Travelled Per Day:** `VIEW[round({MilesPerHour}*{HoursPerDay},1)]`  miles                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Days Travel 🕓:** `VIEW[round({TravelDistance} / (({MilesPerHour}*{HoursPerDay})*{SpeedMultiplier}),1)]`                                                                                                                                                                                                                                                                                                                                                                                              |
| **Minutes Travel 🕓:** `VIEW[round({TravelDistance} / ({MilesPerHour} * {SpeedMultiplier}) * 60, 1)]`                                                                                                                                                                                                                                                                                                                                                                                                   |

