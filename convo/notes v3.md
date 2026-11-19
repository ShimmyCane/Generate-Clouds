# Generate Clouds — notes v3 (archived 2026-11-19)

Read from `gc_notes` (Architecture project, read-only) on 2026-11-19. Thirteen rows still `open`, written against versions 0.5.0 to 0.7.2. The six rows marked done on 2026-11-18 are in `notes v2.md` and are not repeated here. Places are named by city or as "a point"; raw coordinates of places are not written here.

## Status at version 0.7.3

**Built in 0.7.3 (headless tests only, not checked on a device):**

- Stars smaller and dimmer, and they twinkle (each star at its own rate, wall clock). Clouds are drawn over the stars already.
- A thin loading bar at the top of the page while a weather or cloud-notes request runs. Terrain and map-tile loads do not show it yet.
- Panels fade to 20 % opacity after 10 seconds with the pointer off them; hovering, tapping or focusing a panel brings it back.

**Still open (not built):**

1. **Square on the ground that follows the camera** (from space, looking down). The ground must follow the real coastline and land, from real coordinates. A baked ground texture, plain, and higher-resolution snapshots for major cities, so zooming in shows finer detail.
2. **Top 100 cities as high-resolution ground planes**, plus a few natural beaches and landmarks (water, sand, sky). Needs a source and a licence decision before any data is built.
3. **Cloud cover from space is one type everywhere.** The intent is live cloud data from a model. If the link fails, show the last saved data set with its date; if none, a synthetic set (Jimmy will let Claude take the first steps on the synthetic set).
4. **Continents not visible from space.** Looking down from high up, the layout of the Earth's land should be seen.
5. **Zooming out from a pinned place (Shanghai) loses the land** and falls back to something generated. The globe should show the true continents and land masses at every zoom.
6. **Alternate weather sources.** Jimmy wants a short list of other sources with free tests before buying an API key. Research only; no key yet.
7. **Heavy processing; raise the frame rate.** Needs a profile of the latest round before any change. Ask Jimmy which parts he is willing to trade for speed.
8. **Stars:** built in 0.7.3 (see above).
9. **Loading bar:** built in 0.7.3 for weather requests (see above).
10. **Panels fade:** built in 0.7.3 (see above).

**Open question about an earlier note (not in this set):** the "above 5×" weather removal in notes v2 item 3 was withdrawn in `convo v0.13.md`, but the database row for it is marked done. Jimmy should say whether the removal is wanted.
