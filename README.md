
# SnapShotPro

Enchance Your Screenshots


## Features

1. Multi-Format Export PNG - Lossless, high quality (default) JPEG - Lossy with quality slider (1-100%) WebP - Modern format with quality slider (1-100%) Quality controls appear dynamically only for JPEG/WebP Smart file naming with correct extensions

2. Clipboard Copy One-click "Copy to Clipboard" button Exports as PNG for maximum compatibility Works with the standard clipboard API Success/error notifications

3. Watermark Feature Enable/disable toggle Customizable text content 5 Position Options: Bottom Right (default) Bottom Left Top Right Top Left Center Font size control (10px - 48px) Opacity control (0-100%) Color picker with hex input Smart 20px padding from edges

4. Template System Save current settings as named templates Load templates instantly Clear all templates option Persists in localStorage (survives browser refresh) Shows template count Saves everything: filters, overlays, watermarks, gradients, shadows, canvas size, export settings, etc.


## v4 — AI-Powered Enhancements

The canonical v4 build lives in **`snapshot-pro-v3.html`** (self-contained HTML, no build step). Open it in a modern browser or serve locally with `python3 -m http.server`.

New "AI Enhancements" sidebar section:

- **Smart Auto-Redact** — runs Tesseract.js OCR plus MediaPipe face detection in the browser, then scans recognized text for emails, phone numbers, Luhn-valid credit card numbers, and common API key formats (Anthropic `sk-ant-`, OpenAI `sk-`, Slack `xox*`, GitHub `ghp_`, AWS `AKIA…`). Detections appear as dashed review boxes — accept all to convert them into pixelate/blur redactions that match the existing manual redact pipeline.
- **Auto-Crop & Frame** — trims transparent or uniform-color borders and suggests a device frame (Chrome / macOS / iPhone) based on the resulting aspect ratio.
- **Alt-Text & Caption** — local OCR-based heuristic by default. With an optional Anthropic API key (stored in this browser's `localStorage`), uses Claude vision (`claude-haiku-4-5-20251001` or `claude-opus-4-7`) for higher-quality output.

### API key trust model

Claude calls go directly from the browser to `api.anthropic.com` using the `anthropic-dangerous-direct-browser-access: true` header. Your key is stored only in `localStorage` on this device and is never sent anywhere except the Anthropic API. Only paste a key you control.

## Roadmap

- Coming soon


## Screenshots

<img src="blob:chrome-untrusted://media-app/19c483f6-230d-4d06-8571-f87c5279a55f" alt="Screenshot 2026-03-18 1.50.30 PM.png"/><img width="1317" height="642" alt="image" src="https://github.com/user-attachments/assets/3b533a6a-fdbe-4ba0-a439-2c2988dc5ce1" />


