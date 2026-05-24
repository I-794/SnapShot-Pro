# SnapShot-Pro v4 — Pro Editor Overhaul 🎉

**Release date:** 2026-05-24

A major jump from v3. Same single-HTML, zero-runtime-dependency footprint — but the editor now feels like a different application.

Open **`snapshot-pro-v3.html`** in any modern browser (filename preserved so existing links keep working) or serve locally with `python3 -m http.server`.

---

## ✨ What's new

### 🗂 Layers panel
Every annotation, redaction, extra image, text overlay, sticker, watermark, and spotlight is now a real layer. Right-side panel with:
- Visibility toggle (eye)
- Lock toggle
- Double-click to rename
- Drag to reorder z-index

### ⏪ Scrubbable history timeline
Bottom-of-screen dot strip showing every snapshot in your edit history. Click any dot to jump there. `Ctrl+Z` / `Ctrl+Y` still work as before.

### 🔍 Canvas zoom, pan & mini-map
- `Ctrl/Cmd + scroll` — zoom from 10% to 400%, centered on the cursor
- `Space + drag` — pan the canvas
- **Fit** button — reset to 100%
- 160×90 live mini-map in the corner showing your current viewport

### ⌨️ Command palette (`Cmd/Ctrl+K`)
Fuzzy-search any of ~40 commands without hunting through the sidebar:
- Export PNG / JPEG / WebP / HTML card
- Copy to clipboard
- Switch tool (Select, Arrow, Rectangle, Circle, Number, Redact)
- Apply tilt / mesh / scene presets
- Toggle theme, layers panel, spotlight
- Undo, redo, zoom, fit
- Open stickers, clear annotations, reset…

### 🎨 3D tilt
Per-image perspective transform. Sliders for rotate X / Y / Z and perspective. One-click presets:
- **Isometric**
- **Lean**
- **Card**

### 🌈 Mesh gradient backgrounds
A new background mode alongside Gradient / Solid / Transparent. Four radial color blobs composited with screen blending. Interactive 2D pad — drag handles to position blobs, click a handle to recolor. Presets:
- **Aurora**
- **Sunset**
- **Cyber**
- **Pastel**

### 📱 Mockup scenes
Drop your screenshot into a pre-made scene with one click:
- **Laptop** — stylized macOS-style laptop body
- **Phone** — iPhone-style frame with dynamic island
- **Tablet** — tablet body
- **Blurred BG** — heavy blur of your own image as backdrop
- **Floating** — subtle vignette card

### ✨ Sticker library
60+ inline glyph stickers across 4 categories — added as proper annotation layers, fully undoable:
- **Reactions** (🔥 👍 💡 ⭐ ❤️ 🎉 …)
- **Badges** (NEW, HOT, FREE, PRO, BETA, SALE …)
- **Arrows** (→ ← ↑ ↓ ↗ ↘ ⇒ ➜ …)
- **Callouts** (💬 🗨 📢 📌 ⚠ ❓ …)

### 🖱 Alt-click layer select
Hold **Alt** while clicking the canvas to select the topmost annotation/redaction under your cursor — without leaving your current drawing tool. Figma-style.

### 💎 Glass UI
- Backdrop-blur sidebar
- Gradient text on section titles
- Micro-transitions on the command palette and status pill
- Polished annotation toolbar with hover lift + active glow

---

## 🛠 Under the hood

- **Layer-aware drawing** — `drawAnnotations()` and `drawRedactions()` honor a `visible: false` flag, so toggling the eye in the layers panel takes immediate effect.
- **History wrap** — `saveStateToHistory()` is wrapped to refresh both the timeline and the layers panel after every state change.
- **Scene rect override** — scenes paint geometry to the canvas, then return a screen rect that overrides where the main image is drawn. The existing draw pipeline (shadow, border, redactions, annotations, watermark) continues to work unchanged.
- **CSS-based zoom/tilt** — the canvas itself stays at its source dimensions; zoom and 3D tilt are applied as CSS transforms on the wrapper, so click coordinates and exported PNGs are unaffected.
- **No new runtime deps** — still a single HTML file. Nothing to install. Nothing to configure.

## 🧹 Cleanup

Removed a long-standing latent bug: `snapshot-pro-v3.html` had a stray `</script></body></html>` partway through the inline script, followed by a dead duplicate copy of `setupEventListeners()` and `init()` that was never running. (This was the same bug that broke the first v4 attempt.)

## ⌨️ Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl/Cmd + K` | Open command palette |
| `Ctrl/Cmd + S` | Export image |
| `Ctrl/Cmd + Shift + C` | Copy to clipboard |
| `Ctrl/Cmd + Z` | Undo |
| `Ctrl/Cmd + Y` | Redo |
| `Ctrl/Cmd + Scroll` | Zoom |
| `Space + drag` | Pan |
| `Alt + click` | Select layer under cursor |
| `?` | Show keyboard shortcuts overlay |
| `Delete / Backspace` | Delete selected |
| `Escape` | Deselect / select tool |

## 📋 Carried over from v3

Multi-format export (PNG / JPEG / WebP), clipboard copy, watermarks, templates, gradient/solid/transparent backgrounds, device & window frames (macOS, Windows, iPhone, Chrome, Safari, Firefox), annotations (arrow / rect / circle / number), redaction (pixelate / blur), spotlight, auto-layout for multi-image arrangement, light/dark themes, HTML card export.

---

**Thanks for trying SnapShot-Pro v4! 📸**
