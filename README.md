
# SnapShot-Pro

Enhance Your Screenshots. A self-contained, zero-build screenshot editor in a single HTML file.

The canonical build is **`snapshot-pro-v3.html`** (now at v4 — filename preserved so existing links keep working). Open it in any modern browser or serve locally with `python3 -m http.server`.

## v4 — Pro Editor Overhaul

A major jump from v3. Same single-HTML, zero-dependency footprint, but the editor now feels like a real pro tool.

- **Layers panel** — every annotation, redaction, extra image, text overlay, sticker, watermark, and spotlight shows up as a draggable layer with visibility toggle, lock, double-click rename, and drag-reorder for z-order.
- **Scrubbable history timeline** — bottom-of-screen dot strip; click any dot to jump to that point in history. Ctrl+Z / Ctrl+Y still work.
- **Canvas zoom & pan + mini-map** — 10–400% zoom (Ctrl/Cmd + scroll), Space-drag to pan, Fit button, and a live mini-map in the corner showing the current viewport.
- **Command palette (Cmd/Ctrl+K)** — fuzzy-search ~40 commands: export, theme, tools, tilt presets, mesh presets, scenes, stickers.
- **3D tilt** — rotateX/Y/Z + perspective sliders with three presets (Isometric, Lean, Card).
- **Mesh gradient backgrounds** — interactive 2D pad with 4 draggable color blobs, plus Aurora / Sunset / Cyber / Pastel presets.
- **Mockup scenes** — drop your screenshot into a Laptop, Phone, Tablet, Blurred Background, or Floating Card scene with a single click.
- **Sticker library** — 4 categories (Reactions, Badges, Arrows, Callouts), ~60 inline glyph stickers added as proper layers.
- **Alt-click layer select** — hold Alt while clicking the canvas to select the topmost annotation/redaction under your cursor without leaving your current drawing tool.
- **Glass UI** — backdrop-blur sidebar, gradient section titles, micro-transitions, polished toolbar buttons.

## Carried over from v3

Multi-format export (PNG / JPEG / WebP), clipboard copy, watermarks, templates, gradient/solid/transparent backgrounds, device & window frames (macOS, Windows, iPhone, Chrome, Safari, Firefox), annotations (arrow / rect / circle / number), redaction (pixelate / blur), spotlight, auto-layout for multi-image arrangement, light/dark themes, keyboard shortcuts, HTML card export.

## Screenshots

<img width="1317" height="642" alt="SnapShot-Pro v3" src="https://github.com/user-attachments/assets/3b533a6a-fdbe-4ba0-a439-2c2988dc5ce1" />
