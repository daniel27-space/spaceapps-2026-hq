# Lessons from the CLPS practice MVP (Oct 2026)
App: https://daniel27-space.github.io/strength-trainer/clps-practice/v2/  (practice only; no code to be reused)

## What worked
- Static site, no build step: three.js via CDN importmap, data as JSON. Publishes trivially to GitHub Pages.
- Split work by contract: calc owns data JSON, 3D owns scene API, UI owns screens. A short CONTRACT file kept parallel workers aligned.
- Precompute heavy work (ephemeris, per-cell grid stats, horizon masks) offline; browser only does lookups. ~1-2 MB per data file was OK.
- Validation against literature (Mazarico 2011, Glaser 2018): Connecting Ridge ~87% vs 89%, Shackleton rim ~87.5% vs 86.7%.
- Shader ray-march shadows beat shadow maps at 1-2 deg sun elevation.
- Sensible default time (21 Nov 2026) where most Artemis regions are lit and Earth visible; avoids a "half black" first view.

## Pitfalls
- Horizon masks floored at -2 deg; from high peaks (Malapert) true horizon is ~-2.9 deg. Use about -5..+8.75 deg range.
- ispace missions are not CLPS; flag or exclude from CLPS counts.
- DEM-edge sites (Draper CP-12 at -75 deg, also cancelled) have rays running off the DEM: unreliable.
- Coarse grid (240 m DEM, 2.9 km cells) misses ridge crests; prefer exact named points, label cell values.
- Year-only dates silently defaulted to a 14 Nov window; label assumptions.
- Show times as UTC, label score as an index not a probability, say "needs relay" for far-side sites.
- Mercator distorts poles; use a polar view.
- Known v2 bugs left: tour overlay, time bar ignoring Plan date.
- Never tested on a real phone/iPad/laptop (headless swiftshader only, very slow). Test on real devices early Saturday.
- Mission dates/status change (Oct 2026: no CLPS landing in 2026, CP-12 cancelled). Re-verify live before demo.

## Data sources
- LOLA DEMs: https://pgda.gsfc.nasa.gov/products/90 , /products/78 ; LDEM_75S_240M used.
- Illumination/PSR: https://pgda.gsfc.nasa.gov/products/69
- Ephemeris: skyfield + JPL DE421, moon_pa_de421 frame (NAIF kernels https://naif.jpl.nasa.gov/pub/naif/generic_kernels/)
- LROC mosaics: https://wms.lroc.asu.edu/lroc/rdr_product_select ; Moon Trek tiles https://trek.nasa.gov/tiles/apidoc/
- Artemis III regions: NASA Oct 2024 update (no official GeoJSON).
