# Third-party software and data

Runtime dependencies:

- Three.js 0.186.1 — MIT. https://github.com/mrdoob/three.js/blob/dev/LICENSE
- Rapier `@dimforge/rapier3d-compat` 0.21.0 — Apache-2.0. https://github.com/dimforge/rapier.js/blob/master/LICENSE

Development tools: TypeScript (Apache-2.0), Vite (MIT), Vitest (MIT), Playwright (Apache-2.0), tsx (MIT), and their transitive dependencies. Exact installed dependency versions are in `package-lock.json`; license texts remain in their installed packages. Copies of runtime notices are included in `public/licenses/` and the production build.

Included nationwide prepared map data (V1.1):

- 한국교육시설안전원 · 공공데이터포털, 전국초중등학교위치표준데이터, reference 2026-10-01. https://www.data.go.kr/data/15021148/standard.do . Names, public school IDs, addresses and coordinates of 2,402 operating high schools. Source policy: https://www.data.go.kr/ugs/selectPortalPolicyView.do . Source fields are preserved and attributed; procedural estimates are labelled.
- Geofabrik South Korea OSM extract, snapshot 2026-10-22T20:21:33Z. https://download.geofabrik.de/asia/south-korea.html . PBF MD5 `afc2b57ca7e71b22f23a64617583623f`. OSM-derived building outlines/land/roads in `public/maps/schools/` are distributed under ODbL 1.0. Detailed provenance is in `docs/SCHOOL_DATA.md` and `public/data/SOURCES.md`.
- Data preparation dependencies (not required or bundled for gameplay): Pyosmium 4.3.2 (BSD-2-Clause), Shapely 2.2.0 (BSD-3-Clause), NumPy (BSD-3-Clause), plus the wheels' respective dependency notices in `.cache/python/`. Preparation code is original.

Optional additional prepared map data:

- © OpenStreetMap contributors. Open Database License (ODbL 1.0). https://www.openstreetmap.org/copyright and https://opendatacommons.org/licenses/odbl/1-0/
- Optional elevation: Open-Meteo Elevation API / Copernicus DEM. https://open-meteo.com/en/docs/elevation-api . Preserve the returned source attribution and check the service's current usage conditions before a large batch.
- The default `demo-school.json` is an original fictional map, not an extract of an actual school. `tests/fixtures/osm-school.json` is a synthetic protocol fixture, not surveyed geographic data.

Technical and behavioral references, accessed 2026-10-24:

- https://hong-iron.github.io/SMASH/
- https://github.com/Hong-Iron/SMASH
- https://github.com/Hong-Iron/SMASH-SNU-YEONGEON
- The reference README describes polygon-based campuses, OSM footprints, prepared elevation data, fragmentation, repeat hits on debris and undo. Its public UI and descriptions informed the requested feature set. No source, shader, texture, sound, map file, logo, or bundled asset from those repositories was copied into this project. Redistribution rights for those repositories were not assumed.
- Rapier official collider documentation: https://rapier.rs/docs/user_guides/javascript/colliders/
- Three.js official geometry documentation: https://threejs.org/docs/
- Overpass QL reference: https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL

All procedural visuals and synthesized audio in this project are original implementation. No generative image service, external photo, game art pack or licensed sound recording is required.
