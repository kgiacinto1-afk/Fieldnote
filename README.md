# Fieldnote — garden companion app

Personal gardening app: a hand-illustrated "book in a garden." Working prototype is a single HTML file tested on iPhone Safari. Target stack later: React Native + Expo + Supabase.

## For Claude: how to resume work
Fetch the current build from this repo (raw file: `fieldnote_garden.html`) into your workspace, then continue from the state below. Assets in `/assets` are the cut-out source art (plants, beds, maps) for any reprocessing — fetch only what you need.

## Current state (end of Phase B)
- **Garden list view**: angled watercolor beds on aged journal paper (ruled lines, frame, age spots, coffee ring); hand-lettered seasonal title; season slider (spring/summer/winter) with a real "This Season" sow-guide card.
- **Bed view (planting)**: tap soil to plant via big picture-picker; Tidy grid (perspective grid lines + snap on tap and drag-release) or Free plant; drag plants to move (clamped per shape); smart-tap disambiguation near empty spots; plant sheet with real Care + Companions doors (Pests/Harvest are placeholders); pull-up button.
- **Four bed shapes**: rectangle, square, round (ellipse map), in-ground row (lane map). Adding a bed = pick shape by picture, opens immediately.
- **Garden Plan view**: journal page, top-down bed art; drag to arrange, pinch to resize, twist to rotate (15° snap), tap to enter bed. Rows stretch length-wise via 3-slice tiling (caps fixed, middle tiles), spots scale 3–13 with length, shrink clamped at furthest planted spot.
- Storage key `fieldnote_garden_v1`. All art embedded as base64 (~10MB; lazy-load later).

## Build rules (every session, Safari/WebKit)
ASCII quotes only in script; no optional chaining `?.`; no backticks/template literals; no `confirm()`/`prompt()`; inline handlers use `data-*` + delegation; no duplicate function definitions; run `node --check` on extracted script before every delivery; deliver via present_files; verify patch anchors before replacing and verify writes after.

## Roadmap
- **Phase C (next)**: finger-draw paths/borders on the Plan page — capture strokes, simplify + Chaikin-smooth, render as pencil lines in the journal style; undo/erase; saved.
- **Phase D**: sun markers (rises here / sets here) + time-of-day slider lighting beds.
- Then: Pests + Harvest door content (migrate from v51 data), Field Notes journal, the Shelf/reference books, plant expansion (~45 candidates, coastal-first), bed rename/delete, production lazy-loading, RN migration.

## Design north star
Handmade, tailored, never generic. Grandma-simple: one thing per screen, tap don't configure, always show the next step, big targets, reversible, plain words.
