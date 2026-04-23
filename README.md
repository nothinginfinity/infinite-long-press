# Infinite Long Press — Demo

A template PWA demonstrating the **Infinite Long Press** UI pattern: gesture-based depth navigation where each long press reveals a deeper layer of an artifact, and double-tap surfaces back up.

## Live Demo

👉 **[nothinginfinity.github.io/infinite-long-press](https://nothinginfinity.github.io/infinite-long-press)**

## What is Infinite Long Press?

Instead of navigating horizontally (forward/back) or vertically (scroll), you navigate *inward and outward through depth layers* using press duration:

- **Long press** on any prompt → dives one layer deeper
- **Long press again** → dives deeper still (up to depth 10)
- **Double-tap** anywhere → surfaces back up one level
- **Back button** → same as double-tap

This solves a real mobile UX problem: **feature density without navigation overhead.** Instead of menus, drawers, and modals that break context, everything lives in layers beneath the surface of the thing you're touching.

## Demo Structure

- **20 prompts** on the home screen (styled like Studio OS Chat Prompt History)
- **10 depth layers** per prompt, each showing a different type of artifact data
- **Depth indicator dots** showing current position and traversal history
- **Haptic feedback** via Vibration API on each depth transition
- **Press ring animation** — SVG circle fills as you hold, fires at completion

## Depth Layers

| Depth | Layer Name | What it shows |
|-------|-----------|---------------|
| 1 | Prompt Overview | Full prompt text and context |
| 2 | Prompt Analysis | Intent, tone, keywords |
| 3 | Linked Assets | Files, URLs, references |
| 4 | Token Usage | Model, cost, token count |
| 5 | Session History | Timeline and context |
| 6 | Variations | Similar past prompts |
| 7 | Model Memory | What the model knew |
| 8 | Raw Config | System prompt, temperature |
| 9 | Export Options | Copy, share, .osmd, push |
| 10 | Archive | Version history and diffs |

## Gestures

| Gesture | Action |
|---------|--------|
| Tap | Open prompt (no-op in demo) |
| Long press (600ms) | Go one depth deeper |
| Double-tap | Go one depth back |
| Back button | Go one depth back |

## How to Use as a Template

1. Fork this repo
2. Replace `PROMPTS` array in `index.html` with your own items
3. Replace `depthData` array with your own layer definitions
4. Adjust `MAX_DEPTH` and `LONG_PRESS_MS` constants
5. Enable GitHub Pages → `main` branch → root `/`

## Origin

Designed as a companion pattern to **Studio OS Chat** ([nothinginfinity/Studio-OS-Chat](https://github.com/nothinginfinity/Studio-OS-Chat)). The concept: keep users in one spatial context while giving power users access to arbitrarily deep feature layers — like infinite scroll, but for depth instead of length.

---

*Built by [@nothinginfinity](https://github.com/nothinginfinity)*
