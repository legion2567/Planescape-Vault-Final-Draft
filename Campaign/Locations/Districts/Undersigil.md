---
tags:
  - Location
  - District
location:
mapmarker:
art: "[[PlaceholderDistrict.png]]"
aliases:
districtType:
organizations:
currentLocation:
  - "[[Sigil]]"
---

> [!infobox | no-blending black]+ <font color="#ffffff">Infobox</font>
> 
> `VIEW[!{art}][text(renderMarkdown)]`
> 
> # Info
> |  |  |
> |---|---|
> | **Aliases** | `VIEW[{aliases}][text]` |
> | **Type** | `VIEW[{districtType}][text]` |
> | **Dominion** | `VIEW[{organizations}][link]` |
> | **Location** | `VIEW[{currentLocation}][link]` |

# `=this.file.name`

> [!quote]- Scene Introduction
> A script to read from when the party arrives to the planet for the first time to set the scene.

> <font color="#7f7f7f">Write a short summary of the planet, highlighting its most defining traits such as it's environment, atmosphere, and its role or significance.</font>

## Database

![[Database - District Note.base]]


## Map

> [!kirk|map] Map
> ```leaflet
> ### TUTORIAL: INSERT VIDEO LINK HERE
> ### Lines that start with ### are commented out, meaning they will not effect the code. Used to offer guidance. Feel free to remove these.
> 
> ### Uncomment (Remove the ### ) height and width if you would like to manually set the height and width of the leaflet display.
> ### height: 600px
> ### width: 640px
> 
> ### id: vallue will be replaced each time you create a new note.
> id: Undersigil
> image: 
> - [[PlaceholderImage.png|Main]]
imageOverlay:
> - [[[PlaceholderImage.png|Overlay #1]]]
> 
> lock: true
> recenter: true
> noScrollZoom: false
> ### Leave the first [0,0], then replace the second [5000,5000] with [HEIGHT, WIDTH] of your image.
> bounds: [[0,0], [5000, 5000]]
> 
> ### Use lat & long to set center point of the map.
> lat: 0
> long: 0
> 
> ### Set min, max and default zoom to your desired zooms levels.
> minZoom: -3.5
> maxZoom: 0
> defaultZoom: -3.5
> zoomDelta: 0.5
> 
> unit: miles
> ### Measure between two points you know the distance of, then scale up and down util you have your desired distance.
> scale: 1
> ### MapIt is the tag we apply to notes we want to mark on the map. Replace "TBD" with whatever you like WITHOUT spaces.
> ### To add a marker to the map, include the MapIt- tag, and the location and mapmarker property within said note.
> markerTag: 
> - "#MapIt-TBD"
> ```

## Keyed Locations

### Example Location:
> <font color="#7f7f7f">Summary of the location.</font>

## Present

### Current Events:

- <font color="#7f7f7f">Example Quest</font>
    -  <font color="#7f7f7f">Summary of a quest the player can get involved in.</font>
- <font color="#7f7f7f">Example Event</font>
    - <font color="#7f7f7f">Summary of an event that's going on on this district which may not relate to a specific quest or may relate to multiple.</font>

## Past

### History:

> <font color="#7f7f7f">Describe the history of the district, including how it was founded, major events that shaped it, and how it became what it is today.</font>

### Secrets, Rumours & Legends:

> <font color="#7f7f7f">Describe the secrets, rumours, and legends surrounding the district, including hidden dealings, whispered tales, and stories that shape its reputation.</font>

## Notes


