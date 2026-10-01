# Design

## World

**Frutiger Aero × Y2K × Retro-Game HUD.** The portfolio plays as a bright, glossy game screen: an aqua-blue-to-mint gradient sky with drifting bubbles (Frutiger Aero's optimism), frosted-glass panels with glossy highlights, chrome-gradient display type (Y2K), and a full game-UI framing — PLAYER 1 hero, SKILL TREE chips, QUEST LOG for experience, LEVEL SELECT for the case studies, GITHUB UPLINK for live API stats, TROPHIES for certifications, and a CONTINUE? arcade contact screen. The visitor counter is a HIGH SCORE. Entry is a CRT boot screen (glossy HR coin, BIOS-style log, ▶ PRESS START) that also unlocks the chiptune audio on first gesture. A night mode (sliding day/night switch in the HUD, glossy aqua track by day / deep-navy track by night, chrome knob carrying ☀/☾) swaps the bubble sky for a starfield: ink-blue gradient, ~20 fixed stars, bubbles removed, glass panels recolored deep navy. Superseded both earlier worlds (graph-paper notebook → Win95 homepage → this) at the user's request; they asked for "retro game + Y2K + Frutiger Aero".

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

Color strategy: sky/glass world with three committed candy accents (aqua primary, magenta sparingly, sun for score); green reserved for achievements. Night mode (2026-10, user-requested) re-maps the roles via `[data-theme="dark"]`: sky becomes #0B1826 → #0E2742 → #0F3A2F with a fixed starfield layer, --deep becomes #BFE9FF and --body-ink #A9C9DC so all var-driven text flips light, --aqua-deep lightens to #5FD4FF for link contrast, and glass/chip/quest/level/badge panels get deep-navy equivalents with cyan hairline borders.

## Type

- UI/body: Nunito (400/600/700/800) — rounded humanist, the Frutiger spirit
- Display: Nunito 800 with a 5-stop silver-blue chrome gradient clipped to text (Y2K chrome) for the hero name; section h2s stay solid deep with a gradient underline bar
- HUD/arcade: Press Start 2P at 7–11px — eyebrows, terminal bars, PRESS START, CONTINUE?, badges
- Khmer: Kantumruy Pro — bilingual identity preserved

## Layout

Sticky pill HUD topbar (glass; collapses to a hamburger dropdown below 720px; carries the day/night switch and SFX toggles) → 940px stack of glass cards (radius 22, blur + saturate, inset white highlight). Hero: two-column flex with glossy avatar frame (animated shine sweep) and HUD stat grid; stacks photo-first and centered on mobile. Levels carry neon terminal panels (code + canvases). sync_lab.exe is a DPR-aware responsive canvas with an intro line and a live event log. GITHUB UPLINK sits between Work and Trophies: three LED stat tiles (Press Start 2P digits, sun-yellow), animated language bars, and a 13×7 pixel heat map of public events with native tooltips. Mobile: hamburger nav, avatar centered, stats 2-up, full-width CTAs and contact pills.

## Motion

Ambient world motion: 8 bubbles rise forever (different sizes/speeds), the avatar gloss sweeps every ~4.5s, PRESS START / INSERT COIN blink, subtle CRT scanline overlay across the page. The two wireframe canvases auto-rotate with neon glow and accept drag — the world's interactive moment. The sync lab canvas is a DPR-aware responsive animation loop.

Boot motion (2026-10): the site opens on a full-screen CRT boot — glossy HR coin, title, BIOS log lines typing every 150ms, then blinking ▶ PRESS START; click/Enter plays the start jingle (which also unlocks Web Audio), fades the overlay, and only then starts the scroll reveals and the shell's auto-typing, so the hero powers on as the visitor enters. Reduced motion skips the typing delay entirely.

Interaction motion (added at the user's request, 2026-10): sections power-on as they enter the viewport (opacity + 26px rise + slight scale, IntersectionObserver, one-shot) with staggered children inside each card; cards, chips, quests, levels, trophies and badges lift on hover (translate/scale/box-shadow at ~.2s, kept separate from entrance timing via individual transform properties); buttons and terminal controls get a click ripple; HUD links show an active state while scrollspying; a back-to-top arcade button appears after 480px of scroll; the mobile HUD collapses into a hamburger dropdown below 720px. `prefers-reduced-motion`: bubbles removed, shine/blink frozen, reveals forced visible with no transition, canvases still draggable.

## Signature

The chrome-gradient name over a bubble sky; LEVEL SELECT cards with pixel level numbers and neon terminals; the CONTINUE? contact screen with blinking INSERT COIN; HIGH SCORE footer with sun-yellow LED digits.

## Bans honored

No gray bevels (that was the previous world); no true black; no eyebrow labels except the pixel ◆ HUD lines, which are the game world's own language; no fake percentage bars (chips, not XP meters, to avoid invented metrics); icons stay as text glyphs; content identical across all redesigns. The earlier "no fade/slide entrances" ban was lifted by the user's explicit request for scroll-triggered reveals; entrance motion is now a one-shot power-on per section, not a looping effect.
