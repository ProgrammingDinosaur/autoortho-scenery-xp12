# AutoOrtho XP12 scenery (streaming mirror)

X-Plane 12 base mesh packages for [AutoOrtho](https://github.com/ProgrammingDinosaur/autoortho4xplane), repackaged so AutoOrtho can **stream them one tile at a time** instead of requiring a full download.

The scenery itself is the **flightwusel** XP12 package set by **[jonaseberle](https://github.com/jonaseberle/autoortho-scenery)**, built with Ortho4XP 1.40 (`water_tech=XP12`, ZL16, ZL18 around airports). All credit for the meshes goes to the author; this repository only changes the packaging:

- The original single solid `.7z` per area is split into `z_<area>_NN.zip` files under 2 GiB, each holding complete 1x1 degree tiles, so a single tile can be read with an HTTP Range request.
- DSFs are 7z-compressed inside the zips (X-Plane reads them natively). Nothing else is modified; `README.txt` and `_docs/` from the original package are included in the first zip of each area.

Original releases, build system and forum thread:
- https://github.com/jonaseberle/autoortho-scenery
- https://forums.x-plane.org/forums/topic/346802-autoortho-scenery-flightwusel-packages-for-x-plane-12-as-torrent-downloads/

## Use

Turn on **Scenery Library → Stream scenery → XP12 set** in AutoOrtho. Tiles are fetched the first time X-Plane needs them. The zips also work with AutoOrtho's classic full-region installer.

These packages contain **no overlays** (roads, forests, buildings). Use simHeaven X-World (or X-World PRO), as the author recommends.

## Attribution

From the original package README:

- Thanks to Matt (kubilus) for developing AutoOrtho.
- eur/greenland: elevation data by Sonny, released under Creative Commons Attribution 4.0 (CC BY 4.0, https://creativecommons.org/licenses/by/4.0/), from https://sonny.4lima.de/. Please consider a donation to Sonny if you like the European mesh.
- viewfinderpanoramas.org 1" data for North America, Japan, New Zealand and Antarctica, by Jonathan de Ferranti (https://viewfinderpanoramas.org/).
- OpenStreetMap data © OpenStreetMap contributors (ODbL).
- Airport fixes: VNLK Lukla patch by Vlad A., LPPT patch, and fixes from the Alps HD ZL17 packages by toadlife.
- XP12 raster layers (elevation, sea level, soundscape, seasons) come from Laminar Research's X-Plane 12 Global Scenery, as produced by Ortho4XP.

## Areas

| Area | Release | Source version |
|---|---|---|
| greenland | `greenland_v1.4` | flightwusel zl16_o4xp1.40.13+je_v1.4 |

More areas are added as they are repackaged.
