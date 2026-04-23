# ∞ Infinite Long Press — Template

A **gesture-based depth navigation** pattern for mobile PWAs. Hold any item to dive into deeper layers of detail. Double-tap or press back to surface.

> *"Infinite Long Press is to feature depth what infinite scroll is to content length."*

## Live Demo

**[→ Open on GitHub Pages](https://nothinginfinity.github.io/infinite-long-press/)**

## The Pattern

| Gesture | Action |
|---|---|
| **Hold (0.6s)** | Dive one layer deeper |
| **← Back button** | Surface one layer |
| **Double-tap** | Surface one layer |
| **Depth bar dots** | Visual position indicator |

## What's in the Demo

- **20 prompt cards** — each with real tags and descriptions
- **10 depth layers** per prompt — each layer represents a named feature tier
- **Press-progress ring** — animated SVG ring fills as you hold
- **Haptic feedback** — vibration API on mobile
- **Depth dot bar** — shows current position in the depth stack
- **Dark / light mode** — toggle in header
- **Slide-up layer view** — smooth transition between surface and depth

## Depth Layer Map

| Layer | Name | Represents |
|---|---|---|
| 1 | Actions | Quick actions |
| 2 | Context | Related context |
| 3 | History | Run history |
| 4 | Variants | Saved variants |
| 5 | Analytics | Usage stats |
| 6 | Metadata | Raw prompt data |
| 7 | Chain | Prompt chains |
| 8 | Exports | Export options |
| 9 | Debug | Execution trace |
| 10 | Root | Maximum depth |

## Use as Template

1. Clone the repo
2. Edit `PROMPTS` array in `index.html` with your content
3. Edit `LAYER_CONTENT` array with your actual feature layers
4. Adjust `MAX_DEPTH` and `PRESS_DURATION` constants
5. Deploy anywhere — it's a single HTML file

## Origin

Designed for [Studio OS Chat](https://github.com/nothinginfinity/Studio-OS-Chat) — a mobile-first AI chat PWA.

The concept: instead of navigating *away* from an artifact to see its features, you press *into* it. Each hold reveals a new layer. Depth replaces navigation breadth.
