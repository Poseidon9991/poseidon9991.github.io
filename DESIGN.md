# Design

## World

**Frutiger Aero × Y2K × Retro-Game HUD.** The portfolio plays as a bright, glossy game screen: an aqua-blue-to-mint gradient sky with drifting bubbles (Frutiger Aero's optimism), frosted-glass panels with glossy highlights, chrome-gradient display type (Y2K), and a full game-UI framing — PLAYER 1 hero, SKILL TREE chips, QUEST LOG for experience, LEVEL SELECT for the case studies, TROPHIES for certifications, and a CONTINUE? arcade contact screen. The visitor counter is a HIGH SCORE. Superseded both earlier worlds (graph-paper notebook → Win95 homepage → this) at the user's request; they asked for "retro game + Y2K + Frutiger Aero".

## Mode

Experience — the work itself leads; the interface recedes.

## Palette (named roles)

- `--sky-a/b/c`: #8FD9FF → #45B5E8 → #A8E8CC — the fixed-attachment gradient sky (blue into Aero mint)
- `--deep`: #07405E — headings and strong text; `--body-ink`: #123A52 — body
- `--aqua`: #00B7E5 / `--aqua-deep`: #0080B0 — primary accent, links, glossy pills
- `--lime`: #58C920 — achievement orbs, the aqua→lime underline bar
- `--magenta`: #FF4FA3 — CONTINUE? title and PRESS START blink
- `--sun`: #FFD447 — the HIGH SCORE digits
- `--term-bg`: #04283E — neon terminal panels

Color strategy: sky/glass world with three committed candy accents (aqua primary, magenta sparingly, sun for score); green reserved for achievements.

## Type

- UI/body: Nunito (400/600/700/800) — rounded humanist, the Frutiger spirit
- Display: Nunito 800 with a 5-stop silver-blue chrome gradient clipped to text (Y2K chrome) for the hero name; section h2s stay solid deep with a gradient underline bar
- HUD/arcade: Press Start 2P at 7–11px — eyebrows, terminal bars, PRESS START, CONTINUE?, badges
- Khmer: Kantumruy Pro — bilingual identity preserved

## Layout

Sticky pill HUD topbar (glass) → 940px stack of glass cards (radius 22, blur + saturate, inset white highlight). Hero: two-column flex with glossy avatar frame (animated shine sweep) and HUD stat grid. Levels carry neon terminal panels (code + 3D canvases). Mobile: HUD nav scrolls horizontally, avatar shrinks, everything stacks.

## Motion

Ambient world motion: 8 bubbles rise forever (different sizes/speeds), the avatar gloss sweeps every ~4.5s, PRESS START / INSERT COIN blink, subtle CRT scanline overlay across the page. The two wireframe canvases auto-rotate with neon glow and accept drag — the world's interactive moment. `prefers-reduced-motion`: bubbles removed, shine/blink frozen, canvases still draggable.

## Signature

The chrome-gradient name over a bubble sky; LEVEL SELECT cards with pixel level numbers and neon terminals; the CONTINUE? contact screen with blinking INSERT COIN; HIGH SCORE footer with sun-yellow LED digits.

## Bans honored

No gray bevels (that was the previous world); no true black; no fade/slide entrances; no eyebrow labels except the pixel ◆ HUD lines, which are the game world's own language; no fake percentage bars (chips, not XP meters, to avoid invented metrics); icons stay as text glyphs; content identical across all redesigns.
