# Changelog

All notable changes to the MLB The Show 26 — Diamond Dynasty Companion. Newest first.

## v1.1.0 — 2026-05-31
- **Two-level ALL / ANY criteria.** Each filter line has its own ALL/ANY switch, plus a top-level "match ALL lines / ANY line" switch — so you can build nested logic like `(Pitcher AND Sinker AND Cutter) AND (35+ OR Vintage OR Live)`. Replaces the old per-criterion "Required" box. ([guide](CRITERIA-GUIDE.md))
- **"Only show matches" toggle** above the spare-players list — hide cards that don't qualify, or keep them all with matches sorted to the top.
- **Bigger, proportionate cards.** Capped the oversized field and enlarged the field/batting-order/rotation/bullpen/bench/pool cards so the lineup builder reads cleanly instead of a giant field with tiny cards.
- **Windowed desktop app.** New Electron installer that runs the app in its own window, alongside the original browser version.
- **In-app update checker.** The app checks for newer versions on launch and shows a download banner when one is available.
- **Docs linked from inside the app.** The criteria guide is linked in the Lineup Builder info, and the import panel links the verifiable bookmarklet/snippet so you can check them before pasting.

## v1.0.0 — 2026-05-30
- Initial release.
- **Duplicates & sell value** — see your extra copies and what each would sell for (sell-to-highest vs quick-sell).
- **Collection tracking** and a **full card-database browser** (gallery / list / stats views, search & filter on every tab, deep card view).
- **Lineup builder** — diamond field, 5-man rotation, 8-man bullpen, 4 bench reserves; auto-build by criteria; sabermetric batting order with handedness staggering; Programs-grind vs Events modes; save/load full builds & filters; undo/redo.
- **Import your collection** — beginner bookmarklet or advanced session-cookie pull; everything stays on your machine.
- **Packaging & hardening** — single-file Windows build, HTML-escaped card data, loopback-only server bind.
