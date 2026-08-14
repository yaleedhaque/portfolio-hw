# YALEED — a live local network, after dark

An interactive four-chapter night walk through a live local network: gamepads into controllers, PCs into agents, and nine edge projects rendered live in Three.js. Phones into controllers, PCs into agents — no cloud, no account, no trace.

[**Read the build prompt**](PROMPT.md)

## What it does

- Moves a live WebGL camera through the network as the page scrolls — hero, Input, Agents, Devices, Edge, colophon.
- Builds the world procedurally: a hologram **data core** — a spinning cyan data crystal inside a wireframe shell, two cyan orbital rings and one magenta counter-rotator, an energy beam rising through the stack and a blinking beacon — on a glowing circuit-ridge flight with cyan edge rails, twin hologram pylons with magenta diamond tips, floating diamond **device nodes** joined by cyan cable runs, a wireframe **server sphere** overhead with a magenta core and orbit ring, drifting data packets, cyan and magenta data motes, and a projected hologram grid over the court.
- Layers editorial typography and dark gradient scene plates over the 3D world, with section-specific fade and blur transitions.
- Includes chapter navigation, a responsive mobile layout, reduced-motion behavior, and a custom cursor for precise pointer devices.

## How it is made

A deliberately small static site. `index.html` contains the document structure, CSS, procedural scene construction, scroll choreography, and interaction logic. A vendored Three.js r149 build provides WebGL rendering without a package manager or build step.

The data core, pylons, device nodes, cables, server sphere, hologram grid, rain, packets, fog, and post-processing are constructed at runtime. Dark gradient foreground plates sit in normal HTML layers, giving the page its depth while keeping the camera path and lighting live.

## Run locally

From the project root, run:

```bash
python -m http.server 8000
```

Then visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/).

There is no build step, environment variable, analytics script, or runtime network dependency. Python is used only to serve the static files locally; any equivalent static server will work.

## Project structure

```text
portfolio-hw/
├── index.html
├── PROMPT.md
├── README.md
├── .nojekyll
├── .gitignore
└── secret-pathways-assets/
    ├── fonts.css
    ├── three.min.js
    ├── generated/
    └── foreground/png/
```

## Design and attribution

This page is a personalized rebuild of the single-file WebGL experience **Kage** (github.com/MengTo/kage): same camera path, scroll choreography, and post pipeline, re-themed into a hologram data-core network world with entirely new copy, palette, and 3D content. The original Kage grants no license for reuse or redistribution; this is an independent, personal project and is not affiliated with its author.

The vendored Three.js r149 build retains its MIT license notice and copyright attribution. The Onest typeface is used under its open license via the embedded `fonts.css`.

## License

No license is currently granted for reuse or redistribution of this project's code or artwork. The third-party Three.js runtime remains covered by its included MIT license notice.

---

**Md. Yaleed Haque** — [GitHub](https://github.com/yaleedhaque) · [Portfolio](https://yaleedhaque.github.io) · yaleedhaque@users.noreply.github.com
