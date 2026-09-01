---
type: location
related:
  - "[World Map](<World Map.md>)"
aliases:
  - Settlement
---
## Overview
A Village is a concrete place on the World Map that players can go to. They are the location at which the majority of gameplay takes place.

## World Map Relation
on the [World Map](<World Map.md>), the Village exists within a single [County](County.md). The following is defined by game developers, not generated:
- The position in the county, and thus in the world map that it occupies.
- The Biome of the Village is determined by its position on the world map.
- The position in the world map + the biome determines the types of [Terror](<The Terror.md>) that the players can expect to encounter here.
	- This information is not just given to the player. The player has to encounter a certain terror to unlock that metadata being displayed in the world map when this village is selected for inspection.

## Generation

The Village is 1:1 with the World Map scaling, however, the world map doesn't show a detailed map of the village. The World Map is a coarse grain map of the World. And players cannot traverse it. The map of a Village is randomly generated once when a player performs the [Establish A Settlement](<Establish A Settlement.md>) action. From then on, that village map for that player's Queendom instance will always remain.


## Loosing a Village
A village is lost when the Lord of the village is killed, but since he is always in the Lord's Manor, and enemy mobs cannot come inside the Lord's Manor, it is more accurate to say, a Village is lost when the Lord's Manor is destroyed.

When this happens. The play through is over, a cutscene is played for loosing the village. The [Main City](<Main City.md>) is loaded while the village map is unloaded, and the players are respawned in the Main City.

## Reclaiming a Village

When players select a destroyed/lost village on the World Map, they will load into the same village map as before, however, the Lord's Manor will randomly be placed somewhere else using the same placement logic from when the map was first generated, but this time on the existing generated map.

Additionally, this time it will JUST be the Lord Manor's building, nothing else. Along with the spawned players will be a small retinue of villagers, engineers, and troops. Players will need to work harder to rebuild a lost village as it will essentially be from scratch.

There will also be a small fort of Realm Mobs where the old Lord Manor used to be. Defeating it will give you a good boost to your new Lord Manor's stockpile.


## Economics

Buildings generate wealth
A portion is sent to the Main City, this counts towards the Kingdoms Wealth. The more villages you have and the more they produce, the more money the Kingdom makes.
The Rest is stored in the Lord's Manor and counts towards the Village's wealth