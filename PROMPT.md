# Build prompt — Portfolio B (YALEED)

Rebuild the one-file WebGL experience **Kage** (MengTo/kage, a five-chapter night walk through a Kyoto mountain temple) into **YALEED** — a four-chapter night walk through a live local network for **Md. Yaleed Haque**: phones into controllers, PCs into agents, nine edge projects, zero cloud.

## Experience

- Keep the fixed full-viewport Three.js canvas, the continuous scroll-driven camera path, the `data-cam` anchors, scroll math, fog, and the full post pipeline (bloom, grain, vignette, grading) unchanged.
- Keep the palette near-black / amber / bone with at most a subtle cyan accent. No neon.
- Re-theme the world, keeping positions and bounding boxes where the camera composes on them:
  - Temple + torii → a central **network-core tower**: stacked node modules with lit amber LED bays, gold corner studs, an antenna mast with an eyebrow ring and a blinking beacon on top.
  - Stairs → a **circuit ridge**: the same stepped ascent with glowing amber edge rails and a hairline of light on each riser.
  - Moon → a large glowing **server disc** overhead (same position, light, and breathing halo).
  - Lanterns → ground **device nodes** (pillars with status panes, warm amber glow) joined by thin amber **cable runs** between every pair.
  - Rain → cooler, slower, cyan-white. Leaves → drifting **data packets** in dark cyan. Embers stay warm amber. Fog/haze unchanged.
- Replace the generated temple plates with dark gradient fallbacks; drop the temple-specific foreground cut-outs (temple wall, shrine ruins, stone lantern) and keep the botanical ones as silhouettes.

## Wordmark

- Render the hero wordmark as **YALEED**, six letters, in `Onest` 700 (the embedded Wordmark subset only carries A, E, G, K — Y, L, D are missing). Set SZ ≈ 224, TRACK ≈ .22, and update the comment above `buildWordmark()`. The no-WebGL fallback wordmark must switch to Onest 700 too.

## Layout and copy

- Page: preloader (“Waking the network”), hero (`Md. Yaleed Haque` + network lead copy, CTA → github.com/yaleedhaque), four chapters — **I Input** (GamePadEcosystem, BluetoothRemoteHid), **II Agents** (StarkAgent, opencode-free-fallback), **III Devices** (Lumen, AetherCompass, OmniFetch, OmniFetch-Android), **IV Edge** (Edge-project; closing line: “Nine projects live. Zero cloud. All public on GitHub.”) — and a footer.
- Chapter chips label the four chapters: Input / Agents / Devices / Edge. Drop every Japanese vertical accent.
- Footer: all nine projects linked to their GitHub repos, `© 2026 Md. Yaleed Haque`, `WebGL · Onest · Dhaka`, contact mailto:yaleedhaque@users.noreply.github.com, and attribution: “Design base: MengTo/kage — no license granted for the original; this is a personalized rebuild”.

## Interaction and quality

- Preserve the custom cursor, anchor navigation, mobile navigation, responsive layouts, semantic landmarks, reveal choreography, and reduced-motion behavior.
- Keep runtime assets local with relative paths; no frameworks, build tooling, analytics, or remote fonts.
- Verify with a local static server (HTTP 200), parse every inline script with Node, and check at desktop and phone widths; grep the final file so `Kage|Kyoto|MengTo|KAGE` appear only in the footer attribution.
