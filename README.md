<p align="center">
  <img src="mark.svg" alt="Gifio — frames interpolating through the spectrum" width="500">
</p>

<h1 align="center">Gifio</h1>

<p align="center">A free, private GIF maker that runs entirely in your browser.<br>No uploads, no servers, no accounts.</p>

<p align="center"><strong><a href="https://dabirdwell.github.io/gifio/">→ Open Gifio</a></strong></p>

---

## What it does

Drop images in. Drag to reorder. Style them. Tune the timing. Download your GIF.

That's it. Your images never leave your computer.

## Features

**Core:**
- Drag-and-drop from Finder, Files, Desktop, anywhere
- Reorder frames by dragging thumbnails
- Live preview with play/pause and frame stepping
- Floyd-Steinberg dithering for better color quality
- Boomerang mode (forward + reverse)
- Adjustable speed, output size, and loop count
- Keyboard shortcuts (Space, arrow keys)

**Style presets (one-click looks):**
- Film noir, Silver gelatin, Sepia, Cyanotype, Faded Polaroid
- Golden hour, Midnight, Overcast, Candy
- Rainbow Glasses — each frame cycles through the spectrum
- Sunset Drift — warm to cool across frames
- Neon Pulse — alternating complementary hues
- Customize panel with brightness, contrast, saturation, warmth, vignette, grain

**Timing intelligence:**
- Smooth loop — cross-fades the last frame into the first for seamless cycling
- Hold first / Hold last — pause on opening or closing frame
- Smart boomerang interaction (smooth loop defers when boomerang is on)

**Quietly smart:**
- Auto-suggests speed, size, and filename based on your images
- Detects B&W source images and suggests tonal presets
- Detects photos and confirms dithering is on
- Suggests smooth loop for longer sequences
- Smart filenames with collision prevention

## Privacy

Everything runs in your browser via JavaScript. Your images are never uploaded anywhere. There is no server, no analytics, no tracking.

## How to use

**Online:** [dabirdwell.github.io/gifio](https://dabirdwell.github.io/gifio/)
**Locally:** Download `index.html` and double-click it.
**Self-host:** It's one file. Put it anywhere you serve HTML.

## How it works

The GIF encoder is written from scratch in vanilla JavaScript — no libraries, no dependencies. Median cut quantization, Floyd-Steinberg dithering, LZW compression, per-frame timing, all per the GIF89a spec. Style presets are canvas pixel operations applied nondestructively at export time.

One HTML file. 46 functions. Zero dependencies.

## Built by

[Humanity and AI](https://humanityandai.com) — Oklahoma City

## License

MIT — do whatever you want with it.
