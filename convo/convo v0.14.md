# Generate Clouds — convo v0.14 (2026-11-19)

Version 0.7.3: the small fixes from the newest notes. The larger items are not built yet and need a decision or more data first.

## Built in 0.7.3 (headless tests only)

- **Stars (note 8):** smaller and dimmer; each star twinkles at its own rate. Clouds are drawn over them already. Twinkle uses a wall-clock uniform (`uClock`), so it moves in a still view too.
- **Loading bar (note 9):** a thin bar at the top while a weather or cloud-notes request runs. Not yet on terrain or map-tile loads.
- **Panels fade (note 10):** after 10 seconds with the pointer off the panels, they dim to 20 %. Hover, tap or focus brings them back.

Headless load check with the forecast host mocked: no page errors, the bar is hidden when idle, and the panels fade after 10 s.

## Not built yet, and why

- **Ground square that follows the camera (note 1) and continents not visible from space (notes 4 and 5).** These need the Earth picture and the ground-texture path checked together. I have not yet traced why the land falls back to a generated layout when a place is pinned. Next step: check `js/world.js`, `worldLL` in `js/shader.js` and the terrain grid for a fallback path, with a headless view from 250 km.
- **Top 100 cities and natural landmarks (note 2).** Needs a data source and a licence check (OpenStreetMap tiles are CC BY-SA; the satellite and elevation sources have their own terms). Proposal: a list of 100 cities plus a short list of landmarks, and one baked tile per place built by a script committed to the repo. Needs Jimmy to confirm the list and the source.
- **Live cloud model for the space view (note 3).** The current space cover is NASA GIBS (satellite picture of the day). A model field would replace it. Proposed order: (a) live model, (b) the last saved set with its date, (c) a synthetic set. Needs the model choice first (see note 6).
- **Alternate weather sources (note 6).** Research only. I can list candidates with terms and free tiers in a follow-up if Jimmy wants it.
- **Frame rate (note 7).** Needs a timing profile of the 0.7.x round first. I have not measured it yet, so I will not guess at which part to cut.

## Questions for Jimmy

1. The "above 5×" weather removal (notes v2 item 3) is marked done in the database, but convo v0.13 withdrew it. Keep it removed or not?
2. For the top-100 cities: is the list fine as the well-known cities already in the place chips, or should it be different?
3. For the space view: live model first, or keep the satellite picture as the main source and add the model later?
4. Which parts of the frame-rate work can give up detail (for example the far ground or the cloud resolution from space)?

## Database

No row has been marked done. The thirteen open notes stay open until Jimmy confirms which are built (see `notes v3.md`).
