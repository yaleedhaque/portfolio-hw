# Build prompt — Portfolio B (YALEED)

Rebuild the one-file WebGL experience **Kage** (MengTo/kage, a five-chapter night walk) into **YALEED** — a four-chapter night walk through a live local network for **Md. Yaleed Haque**: phones into controllers, PCs into agents, nine edge projects, zero cloud.

## Experience

- Keep the fixed full-viewport Three.js canvas, the continuous scroll-driven camera path, the `data-cam` anchors, scroll math, fog, and the full post pipeline (bloom, grain, vignette, grading) unchanged.
- Palette: near-black night (`#04070c`) with hologram **cyan** (`#19c8ff`) as the primary note, **magenta** (`#ff2bd6`) as the secondary note, and bone type (`#dfe7e0`). Gold (`#c9a24a`) survives only as a rare trace.
- Re-theme the world, keeping positions and bounding boxes where the camera composes on them:
  - Tower → a hologram **data core**: a spinning cyan data crystal inside a wireframe shell, two cyan orbital rings and one magenta counter-rotator, an energy beam rising through the stack, an antenna mast and a blinking beacon on top (same top height as before).
  - Stairs → the **circuit ridge**: the same stepped ascent with glowing cyan edge rails and a hairline of light on each riser.
  - Moon → a wireframe **server sphere** overhead (same position, light, and breathing halo) with a magenta core and one slow orbit ring.
  - Lanterns → floating diamond **device nodes** on thin pylons (cyan emissive, magenta tips) joined by thin cyan **cable runs** between every pair.
  - Trees → antenna **signal masts** with cyan cross-arms, a signal ring and blinking magenta beacon tips.
  - Rain stays cooler, slower, cyan-white. Leaves are drifting **data packets** in dark cyan. Embers become cyan/magenta **data motes**. Fog/haze unchanged. The court gets a projected cyan hologram grid over the dark floor.
- Replace the foreground cut-out plates (grass, branches, pines, bushes, stones, hills) with dark gradient plates — the `.fg` / `.fg-el` stage choreography (entrance, retire, per-section placement) stays exactly as is; only the artwork changes.

## Wordmark

- Render the hero wordmark as **YALEED**, six letters, in `Onest` 700 (the embedded Wordmark subset only carries A, E, G, K — Y, L, D are missing). Set SZ ≈ 224, TRACK ≈ .22, and update the comment above `buildWordmark()`. The no-WebGL fallback wordmark must switch to Onest 700 too. Re-wash the glyph gradient from pale sage to cyan-white (`rgb(210,246,255)` → `rgb(140,222,255)` → `rgb(64,160,220)`).

## Layout and copy

- Page: preloader (“Waking the network”), hero (`Md. Yaleed Haque` + network lead copy, CTA → github.com/yaleedhaque), four chapters — **I Input** (GamePadEcosystem, BluetoothRemoteHid), **II Agents** (StarkAgent, opencode-free-fallback), **III Devices** (Lumen, AetherCompass, OmniFetch, OmniFetch-Android), **IV Edge** (Edge-project; closing line: “Nine projects live. Zero cloud. All public on GitHub.”) — and a footer.
- Chapter chips label the four chapters: Input / Agents / Devices / Edge. Drop every Japanese vertical accent.
- Footer: all nine projects linked to their GitHub repos, `© 2026 Md. Yaleed Haque`, `WebGL · Onest · Dhaka`, contact mailto:yaleedhaque@users.noreply.github.com, and attribution: “Design base: MengTo/kage — no license granted for the original; this is a personalized rebuild”.

## Interaction and quality

- Preserve the custom cursor, anchor navigation, mobile navigation, responsive layouts, semantic landmarks, reveal choreography, and reduced-motion behavior.
- Keep runtime assets local with relative paths; no frameworks, build tooling, analytics, or remote fonts.
- Verify with a local static server (HTTP 200), parse every inline script with Node, and check at desktop and phone widths; grep the final file so `Kage|Kyoto|MengTo|KAGE` appear only in the footer attribution.
