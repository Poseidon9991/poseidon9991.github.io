# Design

## World

**Japanese Anime × Shonen Manga Editorial.** The portfolio reads as a crisp Weekly Shonen Jump / Tankōbon issue inked on warm manga paper (`#F5F0E4` / `#FCFBF7` panels) with Ben-Day screentone halftones, thick sumi ink panel frames (`3.5px solid`), offset hard ink block shadows, radiating manga focus lines (`集中線 / shūchūsen`), falling ink speed streaks, and vertical katakana margin SFX (`ドドド`, `ゴゴゴ`, `シャキーン`, `バチッ!!`). Entry is a **Manga Volume Cover (`VOL. 01 // SPECIAL ISSUE`)** with vertical crimson obi spine, radiating speed lines, and `▶ OPEN MANGA · 読む` CTA; clicking or pressing Enter triggers a diagonal comic slash transition (`第01話!!`). A Paper / Midnight Ink switch (`昼 PAPER` / `夜 INK`) flips the entire comic issue into a high-contrast nocturnal Seinen dark ink palette (`#0B0D14` ground, `#141724` panels, paper-white `#F4F0E6` ink borders, crimson `#FF2955` and electric yellow `#FFE033` accents). Desktop pointers use a compact **22×22px Mangaka G-Pen (`Gペン`) nib cursor** that tilts into writing angle with a rotating Japanese SFX badge (`カリッ!`, `書!!`, `チェック!`, `キラッ!`) on interactive hover, while dragging or moving kicks up **Anime Running Dust Clouds (`土煙`), Tumbling Dirt/Rock Debris (`小石`), and floating hand-lettered Japanese Pen SFX glyphs (`サッ`, `カリッ`, `ダッ!`, `シュッ`)** on `#fxCanvas`, paired with toggleable Web Audio G-Pen paper-scratch & nib-tap SFX (`SFX:ON/OFF`). The side scrollbar combines a **shonen diagonal-striped screentone browser scrollbar** with a custom interactive **Manga Tankōbon Scroll Gauge (`#mangaGauge`)** featuring ruler tick marks, halftone fill, sliding `P.01`–`END` thumb, and chapter stamps.

## Mode

Experience — the real production work leads inside an unmistakably Japanese manga/anime comic frame.

## Palette (named roles)

- `--paper` / `--paper-card` / `--paper-alt`: `#F5F0E4` / `#FCFBF7` / `#EFE9DA` — warm print manga newsprint & panel surfaces (Dark: `#0B0D14` / `#141724` / `#1C2032`)
- `--ink` / `--ink-soft` / `--ink-muted`: `#111116` / `#1D1D26` / `#525263` — sumi ink borders, shadows, typography (Dark: `#F4F0E6` / `#ECE6D8` / `#A6ABC2`)
- `--crimson`: `#E6002E` (Dark: `#FF2955`) — primary shonen anime accent (chapter folios, hanko completion seals, slash wipes, hover shadows, language bars)
- `--yellow`: `#FFD400` (Dark: `#FFE033`) — comic highlight bursts, active chapter tags, SFX badges, click pop-words
- `--cyan` / `--green`: `#00B8D9` / `#14A85B` (Dark: `#00E5FF` / `#22E58A`) — terminal & flow completion indicators
- `--term-bg`: `#12131A` — high-contrast Seinen mecha command monitor

## Type

- Display / Manga Impact: **Dela Gothic One** + **Anton** (Japanese + Latin) — hero name, section `h2`s, chapter numbers, katakana SFX, hanko stamps
- Comic Titles & UI Lettering: **Bangers** — card `h3` titles, navigation tabs, buttons, skill chips, stat labels, panel strips, badges
- Mangaka Brush Accents: **Permanent Marker** — arc period stamps, role subtitles, chapter labels
- Comic Dialogue & Body Copy: **Comic Neue** (Bold 700) + **Zen Kaku Gothic New** — speech bubbles, origin narration panels, project descriptions, skill inspector notes
- Khmer: **Kantumruy Pro** (600) — bilingual identity preserved in cover, hero callout tag, and final speech bubble
- Technical / Code: **Spline Sans Mono** (600/700) — interactive console & code excerpts

## Layout

Sticky inked manga chapter header (`HR 巻01`, chapter links `02`–`終`, mobile hamburger below 880px, Paper/Ink switch, `OST:ON/OFF`, `SFX:ON/OFF`) → 980px vertical spread of inked `.manga-panel` chapters (`第01話` through `最終話`, each with chapter strip, Japanese subtitle, folio badge, and Ben-Day halftone corners). Hero spread: asymmetric 2-column layout with speech-bubble intro, 4 inked character stat cards, slash-fill CTA buttons, and tilted Protagonist Cut-In portrait frame (reveals radiating speed lines + speech bubble on hover), followed by interactive `CONSOLE.SH`. Chapters cover Origin (`#about`), 2×2 Ability Arsenal (`#stack`), Story Arcs timeline (`#experience`), Featured Chapters + interactive `SYNC_LAB` canvas + One-Shots (`#work`), GitHub Live Telemetry (`#github`), Training Arcs with official school crests and crimson `済` hanko seals (`#education`), `TO BE CONTINUED` finale (`#contact`), and Manga Colophon footer with OST player + reader counter.

## Motion & Comic Effects

- **Cover & Chapter Slash Wipe**: diagonal crimson/yellow/ink comic slash bar + katakana impact burst (`第01話!!`, `ドン!!`, `シュッ!!`) on cover open, chapter jumps, back-to-top, and terminal `manga` command.
- **Comic Panel Scroll Reveals**: panels slam into view via IntersectionObserver (`translateY` + subtle scale/tilt spring) with staggered child beats.
- **Kinetic Comic Hovers**: panels pop floating katakana SFX badges (`ドン!!`, `ゴゴゴ`, `シャキーン!`, `ドドド`, `ズドン!!`, `修了!!`, `つづく!!`) and deepen shadows into crimson; cards reveal corner speed lines; buttons & contact links execute diagonal ink-slash fills (`skewX` wipe); portrait cut-in tilts and pops an anime speech bubble; school cards stamp their crimson `済` hanko seal; skill chips pop with slight rotation.
- **Click Comic Pop Bursts**: pointerdown on interactive buttons/links spawns a floating starburst pop-word (`ドン!`, `バン!`, `POW!`, `ZAP!`, `SENT!`, `QUEUED!`) at click coordinates.
- **`prefers-reduced-motion: reduce`**: disables sakura petals, margin SFX, cover speed-line spin, slash wipes, click pops, and forces all reveals immediately visible.
