# SnapShot-Pro

**Make your screenshots look like they belong in a product launch.**

A self-contained, zero-dependency screenshot editor that lives inside a single HTML file. No build step, no install, no server required. Open `snapshot-pro-v4.html` in any modern browser, or serve it locally with `python3 -m http.server`, and you have a full pro-grade editor at your fingertips.

---

## Quick start

```bash
# Easiest: just open it
open snapshot-pro-v4.html

# Or serve locally (paste-from-clipboard is more reliable across browsers this way)
python3 -m http.server
```

Drag, drop, or paste an image. Hit `?` to see every shortcut. Hit `Cmd/Ctrl+K` if you'd rather type than click.

---

## Get an image in

Four ways, all equally fast. Click the upload zone to browse, drag and drop, paste from your clipboard with `Ctrl+V`, or paste raw SVG code and let SnapShot-Pro rasterize it for you. Loading multiple images works too, and the **Auto Layout** picker lays them out as a stack, side-by-side, or a 2×2 grid with adjustable spacing and alignment.

## Edit the image itself

Rotate in 90° steps, flip horizontally or vertically, and dial in **brightness**, **contrast**, **saturation**, **blur**, **grayscale**, and **sepia** with live sliders. Wrap it in a border with custom width and color, round the corners however much you want, and pad it out from the canvas edge.

## Backgrounds, four ways

- **Gradient** — linear or radial, full 0-360° angle control, two color stops with positions, plus eight presets (Sunset, Ocean, Forest, Fire, Midnight, Rose, Purple Dream, Mint).
- **Mesh gradient** — an interactive 2D pad with four draggable color blobs, each with its own color picker. Four presets: Aurora, Sunset, Cyber, Pastel.
- **Solid** — pick any hex color.
- **Transparent** — checkerboard preview in-editor, true transparency on PNG export.

## Shadows that look right

Tune **blur**, **spread**, **opacity**, **x/y offset**, and **shadow color** independently, or grab one of the **Soft / Medium / Hard / None** presets. Shadows correctly punch out behind the image so antialiasing doesn't bleed through.

## Device and window frames

Wrap your screenshot in a realistic chrome: **macOS Window**, **Windows Window**, **iPhone 15** (with Dynamic Island and home indicator), or **Chrome / Safari / Firefox** browser frames with tabs, nav buttons, and an address bar. Each frame supports a dark or light variant, and you can set the window title or URL to match what you're showcasing.

## 3D tilt

`rotateX`, `rotateY`, and `rotateZ` sliders with adjustable perspective for hero-shot angles a flat screenshot can't pull off. Three one-click presets: **Isometric**, **Lean**, and **Card**.

## Mockup scenes

Drop your screenshot straight into a styled scene with one click: **Laptop**, **Phone**, **Tablet**, **Blurred Background** (uses your image as a heavy-blur backdrop behind a centered version), or **Floating Card**. The image rect adjusts automatically to fit.

## Annotations

A floating toolbar above the canvas with **Select**, **Arrow**, **Rectangle**, **Circle**, **Number** (auto-incrementing callouts), **Redact**, **Spotlight**, and **Stickers**. Pick a stroke color and width and draw directly on the canvas. Everything you draw becomes a real layer you can select, move, delete, lock, or hide.

## Stickers

Around 60 inline glyph stickers across four categories: **Reactions**, **Badges**, **Arrows**, **Callouts**. They drop on as proper layers, ready to drag and reorder.

## Text overlay

Add headline text with custom font (seven families), size, color, bold, and italic. Drag it directly on the canvas to reposition — no typing in coordinates.

## Watermark

Text watermark with adjustable size, opacity, color, and a choice of five positions (corners or center).

## Privacy tools

- **Redact** — draw boxes that pixelate or blur the underlying content, with adjustable intensity. One-click clear-all.
- **Spotlight** — dim everything except a region you draw, with adjustable dim opacity. Great for "look at this part" screenshots.

## Layers panel

Every annotation, redaction, extra image, sticker, text overlay, watermark, and spotlight appears as a proper layer. Toggle visibility, lock layers to prevent accidents, double-click to rename, and drag to reorder z-index. Works like every design tool you already know.

## Scrubbable history

The history isn't just an undo stack — a dot strip at the bottom of the screen shows every step you've taken, and clicking any dot jumps you straight to that state. `Ctrl+Z` and `Ctrl+Y` still work for the impatient. Up to 50 steps retained.

## Canvas viewport: zoom, pan, mini-map

Zoom from 10% to 400% with `Ctrl/Cmd + scroll`, hold `Space` and drag to pan, hit **Fit** to reset. A live mini-map in the corner shows your viewport in context so you don't lose yourself at high zoom levels.

## Command palette

`Cmd/Ctrl+K` opens a fuzzy-search palette over roughly 40 commands: export formats, theme switching, tools, tilt presets, mesh presets, scenes, stickers, layer toggles, and more. If you can name it, you can find it without leaving the keyboard.

## Alt-click layer select

Hold `Alt` while clicking the canvas to select the topmost annotation or redaction under your cursor, without leaving your current drawing tool. Saves a lot of trips back to the toolbar.

## Canvas sizing

Custom width and height, plus one-click social presets: **Twitter** (1200×675), **Instagram** (1080×1080), **Facebook** (1200×630), and **LinkedIn** (1200×627).

## Export

- **PNG** (lossless), **JPEG**, or **WebP** with adjustable quality
- **Copy to clipboard** in one click
- **HTML card export** wraps your image in a standalone HTML page ready to share
- **Templates** — save your current setup (gradients, shadows, frames, watermark, all of it) with a name, then load it back later. Multiple templates supported, stored in localStorage.

## Editor polish

Backdrop-blur glass sidebar, gradient section titles, micro-transitions everywhere, and **light/dark theme** toggle (your choice persists across sessions). Full keyboard shortcuts — hit `?` anytime to see the full list.

---

## Screenshot

<img width="1317" height="642" alt="SnapShot-Pro" src="https://github.com/user-attachments/assets/3b533a6a-fdbe-4ba0-a439-2c2988dc5ce1" />
