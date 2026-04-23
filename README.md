# Infinite Long Press — Demo

A template PWA demonstrating the **Infinite Long Press** UI pattern: gesture-based depth navigation where each long press reveals a deeper layer of an artifact, and double-tap surfaces back up.

## 🔴 Live Demo

👉 **[nothinginfinity.github.io/infinite-long-press](https://nothinginfinity.github.io/infinite-long-press)**

> Enable GitHub Pages → Settings → Pages → Branch: `main` / `(root)` to activate.

---

## What's in this demo

### Gestures
| Gesture | Action |
|---|---|
| **Long press** a prompt (600ms) | Dive to Depth 1 |
| **Long press** any card | Zoom into that card (Card Level 1–5) |
| **Long press** the hint bar | Go one prompt depth deeper (up to 10) |
| **Double-tap** anywhere | Go back one level |
| **Back button** | Go back one level |

### Depth System
- **Prompt depth**: 10 levels per prompt (Overview → Analysis → Assets → Tokens → History → Variations → Memory → Config → Export → Archive)
- **Card depth**: 5 levels per card (Summary → Full Detail → Edit History → Related → Raw/Export)
- **Two independent dot rows** — teal for prompt depth, amber for card depth

### Edit Mode
- Tap the **pencil FAB** (bottom right) on any depth screen
- All cards become **inline editable** (contenteditable)
- **Toolbar** slides up with: Share · Send · Use as Prompt
- **Share** uses Web Share API (falls back to clipboard copy)
- **Send** → stub for Studio OS inbox push (coming next)
- **Use as Prompt** → opens the Chat Panel

### Chat Panel
- Slides up full-screen over the depth view
- Shows current depth layer as context
- Text input with Enter-to-send
- **Scaffold mode**: echoes a placeholder response
- Next step: wire in a real LLM API with model selector

---

## Depth Layers

| Depth | Name | Description |
|---|---|---|
| 1 | 📋 Prompt Overview | Full prompt + character/word counts |
| 2 | 🔍 Prompt Analysis | Intent, tone, keywords, complexity |
| 3 | 🧩 Linked Assets | Files, URLs, linked prompts |
| 4 | 📊 Token Usage | Token count, model, estimated cost |
| 5 | 🕓 Session History | Timestamp, session, prior prompt |
| 6 | 🔁 Variations | Similar prior prompts |
| 7 | 🧠 Model Memory | Model context at run time |
| 8 | ⚙️ Raw Config | System prompt, temperature |
| 9 | 📤 Export Options | Copy, share, .osmd, push to repo |
| 10 | 🗂️ Archive | Version history, diffs |

## Card Sub-Levels

| Level | Name |
|---|---|
| 1 | Summary |
| 2 | Full Detail |
| 3 | Edit History |
| 4 | Related |
| 5 | Raw / Export |

---

## Roadmap

- [ ] LLM API settings panel (choose model, enter key)
- [ ] Send to Studio OS inbox via GitHub API
- [ ] Persist edits across sessions (IndexedDB)
- [ ] Haptic patterns per depth level
- [ ] Export full depth tree as `.osmd`

---

## Origin

Designed as a companion pattern to **Studio OS Chat** ([nothinginfinity/Studio-OS-Chat](https://github.com/nothinginfinity/Studio-OS-Chat)).

*Built by [@nothinginfinity](https://github.com/nothinginfinity)*
