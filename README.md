# GIF Studio

A free, private GIF maker that runs entirely in your browser. No uploads, no servers, no accounts.

**[→ Open GIF Studio](https://dabirdwell.github.io/gif-studio/)**

---

## What it does

Drop images in. Drag to reorder. Tune the speed, size, and quality. Download your GIF.

That's it. Your images never leave your computer.

## Features

- **Drag-and-drop** — from Finder, Files, Desktop, wherever
- **Reorder frames** — drag thumbnails to rearrange
- **Live preview** — plays your animation while you tune it
- **Floyd-Steinberg dithering** — dramatically better color quality than naive GIF encoding
- **Boomerang mode** — plays forward then backward, for that satisfying loop
- **Adjustable speed** — 50ms to 2 seconds per frame
- **Adjustable output size** — 200px to 1200px wide
- **Loop control** — forever, once, or a fixed count
- **Keyboard shortcuts** — Space to play/pause, arrow keys to step
- **File size display** — know what you're downloading
- **Zero dependencies** — one HTML file, nothing to install

## Privacy

Everything runs in your browser via JavaScript. Your images are never uploaded anywhere. There is no server, no analytics, no tracking. View source if you want to verify.

## How to use

### Option 1: Use online
Visit **[dabirdwell.github.io/gif-studio](https://dabirdwell.github.io/gif-studio/)**

### Option 2: Use locally
Download `index.html` and double-click it. Opens in any browser.

### Option 3: Self-host
It's one file. Put it anywhere you serve HTML.

## How it works

The GIF encoder is written from scratch in vanilla JavaScript:

1. **Median cut quantization** reduces millions of colors to a 256-color palette
2. **Floyd-Steinberg dithering** (optional) diffuses quantization error across neighboring pixels, producing smoother gradients
3. **LZW compression** encodes each frame using the GIF89a standard
4. **NETSCAPE2.0 extension** controls looping behavior

No libraries. No canvas-to-blob hacks. Just bytes.

## Technical notes

- Input: JPG, PNG, WebP, or any browser-supported image format
- Output: GIF89a with global color table (256 colors)
- Large frames (5000×4000 photos) work fine — they're resized to your chosen output width
- Boomerang mode duplicates interior frames in reverse, so a 7-frame input becomes a 13-frame GIF

## Built by

[Humanity and AI](https://humanityandai.com) — Oklahoma City

## License

MIT — do whatever you want with it.
