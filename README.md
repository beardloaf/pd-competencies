# Product Designer Competency Matrix 2026

An interactive competency matrix for product designers — **Senior → Staff → Principal → Distinguished** across five competencies (Product Thinking, Execution & Impact, Tooling & Automation, Communication & Partnership, People & Leadership), built on the *60% readiness* model.

## Open it

Just open `index.html` in any browser. It's a single self-contained file — CSS and JS are inlined, with no external dependencies — so it works equally well opened from disk, served, or embedded in a preview.

```bash
open index.html        # macOS
```

## What's inside

Three views, switchable from the header:

- **Matrix** — A connected reference table: 5 competencies (rows) × 4 levels (columns). Each cell shows a tight **mastery** line plus a `60% → next` label; hovering it reveals the readiness text in a tooltip. Each column header carries the level's scope (self → team → org → industry); click a header to outline that column in its color. A **Today / Future** toggle swaps the whole matrix between today's model and a near-future cut where designers own the product, ship the front end, and orchestrate AI (the `TODAY` and `FUTURE` arrays in the script). The **Staff** column has an **I / II** toggle (Staff II = Senior Staff), and each cell's footer is anchored to the bottom so the `60% → next` labels line up across a row.
- **Self-Assessment** — A slider per competency (four stops: Senior → Distinguished) whose rail reveals a green→blue→red→yellow gradient and glows more as you climb. A live radar chart, profile summary, and a 3×2 grid of "strength now / growth edge" cards update as you move them. Saves to your browser.
- **Guide** — How to use the matrix for hiring, growth, and team planning, plus the philosophy notes (the 60% rule, uneven growth, stacking levels).

Other niceties: a sticky header row and sticky first column (so labels stay put while scrolling), responsive layout, keyboard-accessible, and a print stylesheet (browser Print → "Save as PDF").

## Editing the content

Everything lives in [`index.html`](index.html) — markup, an inline `<style>`, and an inline `<script>`. The competency text is in the `COMPETENCIES` array inside that script. Each competency has four levels (`senior`, `staff`, `principal`, `distinguished`); each level has:

- `mastery` — the tight line shown in the matrix cell, also the "strength now" in the Self-Assessment
- `readiness` — the 60%-toward-next line, also the "growth edge" in the Self-Assessment (`null` for Distinguished)

Level names and scopes are in the `LEVELS` array; colors are in the `LEVEL_COLORS` map just above it.

## Deploying

`index.html` is a single static file — it deploys as-is to any static host. With the Vercel CLI: `vercel deploy` from this folder.
