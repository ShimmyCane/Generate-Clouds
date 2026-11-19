# Generate Clouds — convo v0.15 (2026-11-19)

Decisions on the open items in `convo v0.14.md`. Merged PR #1 (0.7.3) into `main`.

## Decisions

1. **Ground square that follows the camera; continents from space; pinned place losing land (notes 1, 4, 5).** Not decided here; these are investigation items.
   - *Answer to my question 1:* the "above 5×" weather removal (notes v2 item 3) is **removed** (Jimmy: "remove it"). Remove the rain, snow, thunderstorm and tornado features above about 5× zoom. Keep the cloud-cover hide button.
2. **Top 100 cities and landmarks (note 2).** Jimmy's reply "use the synthetic set" does not clearly answer this question (it was about the list). Open: confirm the list before any data work.
3. **Cloud cover from space (note 3).** Decided: **live model data**, fed **once a week** and **saved in the cache**. Order: live model (weekly, cached) → last saved set with its date → synthetic set. Jimmy's "use the synthetic set" may refer to this fallback; confirm.
4. **Frame rate (note 7).** Decided: add a **toggle in Settings** for each energy-heavy feature. Claude to propose which features are energy-heavy, from a timing profile, for Jimmy to confirm.
5. **Alternate weather sources (note 6).** Not yet answered.

## Done

- PR #1 merged to `main` (0.7.3: stars, load bar, panel fade). Database rows are still open until Jimmy confirms which are built.

## Next

- Remove the 5× weather features (note v2 item 3).
- Weekly cached model cloud data for the space view, with the dated fallback and the synthetic set.
- Profile the page; add Settings toggles for the energy-heavy features; propose which ones.
- Confirm the top-100 city list and the synthetic-set question.
