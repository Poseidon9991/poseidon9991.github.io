# Design

## World

**Frutiger Aero × Y2K × Retro-Game HUD.** The portfolio plays as a bright, glossy game screen set inside a full Frutiger Aero landscape (2026-10 deepening, user-requested "more Frutiger Aero"): the base is a CC0 AI-generated Frutiger Aero wallpaper (teal sky, cyan bubbles, green meadow — `public/fa-vista.jpg`, Wikimedia Commons, converted to 93KB JPEG) blended under semi-transparent aqua→mint sky overlays, with two blurred aurora ribbons (cyan-mint-lime + violet) drifting across the top, three glossy white clouds crossing the sky at 140–230s, a lens-flare shimmer in the upper right, a fixed grass meadow at the viewport bottom (layered green hills, 26 swaying blades, dew drops, tiny flowers), a mixed school of seven fish tracks crossing the sky at different depths — glossy torpedo fish in blue/teal hue-shifts, a gold angelfish, an orange clownfish, a lime-green spiked puffer, and a silvery minnow school — swimming in both directions (mirrored layers) with wagging tails, rising breath-bubble trails, and depth blur on far fish, three large bokeh orbs rising slowly, and 12 bubbles with aqua glow. Frosted-glass panels carry the classic Aero top-gloss sheen (::before at 48% falloff), chrome-gradient display type (Y2K, now continuously flowing via a periodic 2-cycle gradient), and a full game-UI framing — PLAYER 1 hero, SKILL TREE chips, QUEST LOG for experience, LEVEL SELECT for the case studies, GITHUB UPLINK for live API stats, TROPHIES for certifications, and a CONTINUE? arcade contact screen. The visitor counter is a HIGH SCORE. Entry is a CRT boot screen (glossy HR coin, BIOS-style log including "BGM TRACK · LEASE", ▶ PRESS START) over the dimmed landscape; it also unlocks the chiptune audio and starts the background music on first gesture. Background music: a looping hidden YouTube IFrame playlist (nocookie, volume 42) — "LEASE" by Takeshi Abo (xsdWibwQdZE, the user's linked bitcrushed upload) then "Lotus Waters" from the Yume 2kki OST (rj0K5WkNxX4) — toggled by a BGM:ON/OFF HUD button persisted in localStorage; the NOW PLAYING glass chip (animated EQ bars, above the HIGH SCORE footer) names the current track and is itself the skip button. A night mode (sliding day/night switch in the HUD, glossy aqua track by day / deep-navy track by night, chrome knob carrying ☀/☾) swaps the world for a starfield: ink-blue gradient, ~20 fixed stars, fish/bokeh/bubbles removed, clouds dimmed to near-invisible, photo and meadow dimmed, aurora kept as a faint borealis. Superseded both earlier worlds (graph-paper notebook → Win95 homepage → this) at the user's request; they asked for "retro game + Y2K + Frutiger Aero".

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
- Khmer: Kantumruy Pro (600 weight for presence) — bilingual identity preserved, set as glossy glass pills in the hero and contact (the Khmer UI standard font; kept after researching alternatives — no more Frutiger-like Khmer face exists than this)

## Layout

Sticky pill HUD topbar (glass; collapses to a hamburger dropdown below 720px; carries the day/night switch, the BGM:ON/OFF music toggle and the SFX toggle) → 940px stack of glass cards (radius 22, blur + saturate, inset white highlight, top-gloss sheen). Hero: two-column flex with glossy avatar frame (animated shine sweep) and HUD stat grid; stacks photo-first and centered on mobile. Levels carry neon terminal panels (code + canvases). sync_lab.exe is a DPR-aware responsive canvas with an intro line and a live event log. GITHUB UPLINK sits between Work and Trophies: three LED stat tiles (Press Start 2P digits, sun-yellow), animated language bars, and a 13×7 pixel heat map of public events with native tooltips. The scoreboard footer is itself a glass panel (the meadow scrolls behind it), carrying the NOW PLAYING chip, HIGH SCORE and badges. TROPHIES entries lead with glossy white logo tiles (official school marks: NYP wordmark SVG, Guangzhou Industry & Trade Technician College crest, NPIC crest — cropped to their emblem regions, `public/school-*.png|svg`) each pinned with a mini lime ★ badge. Browser surfaces themed: aqua text selection, glossy aqua scrollbar (WebKit + Firefox scrollbar-color). Mobile: hamburger nav, avatar centered, stats 2-up, full-width CTAs and contact pills.

## Motion

Ambient world motion: 12 bubbles rise forever (different sizes/speeds) with aqua glow, three bokeh orbs drift upward, seven fish tracks cross the sky in both directions (46–96s loops, per-species tail wag .55–.9s, gentle bob, rising breath-bubble trails, far fish softened with blur for depth), clouds cross at 140–230s, aurora ribbons drift/rotate over 26s, the lens flare pulses over 11s, grass blades are procedurally redrawn each frame as bending béziers (per-blade phase/speed/lean plus traveling right-to-left wind gusts that breathe in strength, small flutter at gust peaks — no rigid rotation), dew drops pulse, the avatar gloss sweeps every ~4.5s, the hero chrome flows continuously (periodic gradient, 7s cycle), PRESS START / INSERT COIN blink, the NOW PLAYING EQ bars bounce, subtle CRT scanline overlay across the page. The two wireframe canvases auto-rotate with neon glow and accept drag — the world's interactive moment. The sync lab canvas is a DPR-aware responsive animation loop.

Boot motion (2026-10): the site opens on a full-screen CRT boot — glossy HR coin, title, BIOS log lines typing every 150ms, then blinking ▶ PRESS START; click/Enter plays the start jingle (which also unlocks Web Audio), fades the overlay, and only then starts the scroll reveals and the shell's auto-typing, so the hero powers on as the visitor enters. Reduced motion skips the typing delay entirely.

Interaction motion (added at the user's request, 2026-10): sections power-on as they enter the viewport (opacity + 26px rise + slight scale, IntersectionObserver, one-shot) with staggered children inside each card; cards, chips, quests, levels, trophies and badges lift on hover (translate/scale/box-shadow at ~.2s, kept separate from entrance timing via individual transform properties); buttons and terminal controls get a click ripple; HUD links show an active state while scrollspying; a back-to-top arcade button appears after 480px of scroll; the mobile HUD collapses into a hamburger dropdown below 720px. `prefers-reduced-motion`: bubbles, clouds, fish and bokeh removed, shine/blink/chrome-flow frozen, reveals forced visible with no transition, canvases still draggable.

## Signature

The chrome-gradient name flowing over the Frutiger landscape (photo + aurora + fish + meadow); LEVEL SELECT cards with pixel level numbers and neon terminals; the CONTINUE? contact screen with blinking INSERT COIN; the NOW PLAYING chip with live EQ bars; HIGH SCORE footer with sun-yellow LED digits on a glass panel over the meadow.

## Bans honored

No gray bevels (that was the previous world); no true black; no eyebrow labels except the pixel ◆ HUD lines, which are the game world's own language; no fake percentage bars (chips, not XP meters, to avoid invented metrics); icons stay as text glyphs; content identical across all redesigns. The earlier "no fade/slide entrances" ban was lifted by the user's explicit request for scroll-triggered reveals; entrance motion is now a one-shot power-on per section, not a looping effect.
