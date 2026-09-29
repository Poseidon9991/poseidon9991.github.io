# Design

## World

The Engineer's Graph-Paper Notebook. The portfolio reads as pages from a field engineer's lab notebook: everything sits on a measured graticule, content blocks are ruled like notebook entries, and the hero is a technical-drawing title block (name, role, location, date, rev) — the artifact this profession actually stamps its identity on. The graticule is not decoration; it is the world's measuring tool, and every element aligns to it.

Challenger verdicts from the roll: the oscilloscope signal bench was competitive (engineer's measurement bench, strong audience identification) — it donates two disciplines: "everything on screen is measured against the ten-division graticule" (strict grid alignment) and instrument-green for active/interactive states. The BBS nightboard, rain-night cityscape, mesophotic dive, mid-century magazine, and seed rack were declined: they could not carry a bilingual full-stack developer's range for a recruiter audience without costume.

## Mode

Experience — the work itself leads from the first viewport; the interface recedes.

## Palette (named roles)

- `--paper`: #F3F5EF — cool pale graph-paper ground (light world: recruiters read in daylight and print)
- `--ink`: #1B231E — near-black with a green cast; body and headings
- `--graphite`: #57625B — secondary text, rules at low emphasis
- `--grid`: rgba(27,35,30,0.08) — graticule lines on paper
- `--instrument`: #146B45 — committed accent: links, active states, stamps, the "trace" green donated by the oscilloscope
- `--red-pencil`: #C23A26 — the red margin rule and margin annotations only, as in real graph paper

Color strategy: Restrained-plus — neutral paper world, one committed green accent, red reserved for the notebook's margin ritual.

## Type

- Display: Archivo Variable (Black 800–900, tight tracking -0.02em) — drafting-stencil grotesque for the title block and section heads
- Body: Kantumruy Pro (400/500/600) — a Khmer-and-Latin grotesque; the bilingual identity is the body face itself, so Khmer text needs no costume
- Code: Spline Sans Mono — only for actual code excerpts and tabular measurement readouts in case studies, never for labels
- Base 17px / 1.6 body, measure 65–70ch, balanced headings, weight steps 400 → 600 → 900

## Layout

Left margin column (red rule at 88px on desktop) carries pencil-annotation metadata (dates, plate refs); main content max-width 880px inside it. Mobile: margin collapses to a top rule, graticule stays. Every element aligns to the 8px graticule; section heads sit on a ruled baseline.

## Motion

One authored moment: the hero title block draws itself on load — SVG rules stroke-draw, fields settle with exponential ease-out (600–900ms total), then the page is still. `prefers-reduced-motion`: everything renders in final state. Hover states are measured responses (rule weight change, graticule cell highlight), 120–160ms.

## Signature

The title block, echoed at the footer as a drawing sheet corner (DRAWN BY / DATE / SCALE 1:1 / SHEET 1 OF 1). Certifications carry a small ink-stamp treatment in instrument green.

## Bans honored

No eyebrow labels above headings; no section numbers except case-study "plates" (a drawing set genuinely numbers plates); no gradient text; no mono-as-costume (mono only in real code excerpts); icons are authored single-stroke SVGs; no card grids of icon+heading+text; grid overlay earns its place as the world's own measuring tool.
