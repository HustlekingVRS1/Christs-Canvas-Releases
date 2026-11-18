# Building footprints for Christ's Canvas

Static files read by the app's House auto-outline. No server, no key.

* `v1/index.json` — coverage box, grid size and the list of cells that have buildings.
* `v1/<row>_<col>.json` — buildings whose centre is in that 0.02° cell
  (row = floor(lat / 0.02), col = floor(lng / 0.02)); coordinates are integer
  1e-6° offsets from the cell's south-west corner.

Coverage: 37.70–38.35° N, 86.20–87.10° W (all of Perry County, IN and
neighbouring parts of Spencer, Dubois, Crawford, Harrison counties, IN and
Hancock, Breckinridge, Daviess, Meade counties, KY) — about 104,000 buildings.

## Source and licence

Building footprints © Microsoft, from
[Global ML Building Footprints](https://github.com/microsoft/GlobalMLBuildingFootprints)
(release 2026-02-03), made available under the
[Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/).
This derived database is likewise available under the ODbL 1.0. It was
produced by `scripts/build_footprints.py` in the app's source repository
(re-encoding and cutting into grid cells; geometry otherwise unchanged).
