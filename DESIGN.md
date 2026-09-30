# Design

## World

**The Year-2000 Programmer's Homepage.** The portfolio reads as a personal homepage from the turn of the millennium, running inside a Windows 95-style desktop: teal #008080 desktop, gray beveled windows with navy→blue title bars (about.txt — Notepad, career.log — Event Viewer, C:\projects — File Manager), an ASCII banner, a scrolling marquee, an Apache "Index of /work/more" project listing, LED visitor counter, 88×31 badges, and a live taskbar clock. It is the era's programmer homepage faithfully rendered — not a parody of it.

Superseded: the Engineer's Graph-Paper Notebook (replaced 30/09/2026 at the user's request — they wanted the old-school web era). Two disciplines carried forward unchanged: the wireframe sync/datastore studies (now re-paletted as green-phosphor CRT renderings inside inset DOS panels — the same 3D content, the era's correct texture) and genuine bilingual Khmer content.

## Mode

Experience — the work itself leads; the interface recedes (unchanged).

## Palette (named roles)

- `--desk`: #008080 — Windows 95 desktop teal with a 1px dither overlay
- `--face`/`--face-hi`/`--face-sh`/`--face-dk`: #C0C0C0 / #FFFFFF / #808080 / #404040 — the classic beveled control face
- `--bar-a`→`--bar-b`: #000080→#1084D0 — title-bar gradient
- `--ink`: #000000 — body text (era-correct true black)
- `--link`: #0000FF, `--visited`: #551A8B — era link colors, underlined, always
- `--green`: #39FF14 — phosphor green, only inside CRT panels
- `#000080` navy — headings inside content; `#C00000` — double-line rubber stamps

## Type

- UI/chrome: Tahoma/MS Sans Serif stack, 12–13px — the era's system font
- Code/ASCII/tables of contents: Courier New — the era's mono
- Khmer: Kantumruy Pro — bilingual identity preserved
- Headings: small navy bold, never display-scale (era pages had no giant display type)

## Layout

Single 780px column of stacked windows on the desktop; each section is a complete window (title bar + optional menu bar + padded gray face). Content panels use sunken white insets; data uses bordered tables, not cards. Mobile: windows fill width, taskbar clock hides, ASCII banner shrinks — the world survives down to phone width.

## Motion

Era-correct ambient motion only: the marquee scrolls forever, the ▮ cursor blinks after the hero statement, the taskbar clock is a real live clock, the visitor counter increments per browser. The two CRT canvases auto-rotate and respond to drag (the world's single "interactive moment"). `prefers-reduced-motion`: marquee and blink freeze, canvases render static but still accept drag.

## Signature

Nested window chrome everywhere; the footer badge row ("BEST VIEWED 800×600", "HTML 4.01", "MADE WITH NOTEPAD") and the Start-button taskbar are the world's closing marks. Certification stamps keep their rotated rubber-stamp treatment.

## Bans honored

Zero rounded corners and zero shadows beyond 1-2px hard bevels; no gradients except the navy title bar (era chrome); no fade/slide entrances; no eyebrow labels; icons are text glyphs (□, ✕, ✉) as the era used them; emojis avoided in UI chrome; the only color beyond gray/navy lives inside the CRT panels where green-on-black belongs.
