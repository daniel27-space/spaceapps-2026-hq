# Sun/Earth visibility calc (generic)
Pattern used in the practice MVP; rewrite fresh during the event.
1. pip install skyfield numpy. Download de421.bsp plus NAIF Moon kernels (moon_pa_de421_1900-2050.bpc, moon_080317.tf, pck00008.tpc).
2. Build the Moon body-fixed frame (MOON_ME_DE421). For each time step (3-6 h), compute Sun and Earth unit vectors from Moon centre.
3. For a site (lat, lon) on sphere R=1737.4 km: elevation = asin(dot(dir, local_up)); azimuth from local east/north.
4. Terrain: sample a LOLA DEM along N azimuths (64-360) to ~150 km with a ~2 m mast, include curvature, store horizon elevation per azimuth. Range about -5..+8.75 deg.
5. Lit = Sun elevation > mask at Sun azimuth (optionally account for 0.27 deg Sun radius). Earth visible likewise.
6. Outputs: % lit, % Earth, % both, longest night (flag lower bound at window edge), windows.
7. Sanity tests: equator ~50% lit, near side Earth ~100%, far side 0%, synodic ~29.5 d; compare pole sites with Mazarico/Glaser values.
8. Export compact JSON for the browser; document window length and UTC.
