# Event Photo Auto-Editor

A browser-based batch editor for event photographers. Drop in a set of photos, pick an event style, check a few frames, and export the whole set edited as a ZIP.

**Live app:** https://nrsmith2550.github.io/photo_auto_editor/

## Features

- **RAW support:** Canon (CR2, CR3), Nikon (NEF), Sony (ARW), Fujifilm (RAF), DNG, Olympus, Panasonic, Pentax and more, decoded in the browser with LibRaw. JPEG, PNG and WebP work too.
- **7 event styles:** Wedding: Light & Airy, Wedding: Warm Film, Corporate & Headshots, Party & Nightlife, Outdoor Golden Hour, Classic B&W, Natural. A strength slider sets how strongly each one is applied.
- **Auto-correction:** white balance, exposure and levels are fixed before the style is applied, so shots from mixed lighting come out consistent.
- **Portrait retouching:** edge-aware skin smoothing that keeps eyes, lashes and hair sharp.
- **Per-photo control:** 13 sliders, a before/after comparison, and "copy to all".
- **Lightroom presets:** save the selected photo's look, or all 7 styles, as `.xmp` presets for Lightroom Classic and Lightroom. They import into an "Event Auto-Editor" preset group. Lightroom's tools work differently, so the results are close, not identical: warmth and tint become a global color-grading tint, skin smoothing becomes negative Texture (which affects the whole photo), and white balance is set to Auto.
- **Batch export:** full resolution or resized, at your choice of JPEG quality, downloaded as a ZIP.

## Privacy

Everything runs in your browser. Photos are never uploaded anywhere.

## Limits

- HEIC files aren't supported yet.
- RAW files are processed in 8-bit with the camera's white balance as the starting point. That suits event work, but heavy exposure recovery has less headroom than in Lightroom.
- A full-size RAW export takes about 3–5 seconds per photo. Exports at 2048 px take under a second.
- EXIF metadata isn't copied to the exported files.
- Skin smoothing works by color, so warm wood, sand or orange walls can get slightly softened. Lower the Skin smoothing slider on those shots.

## Running locally

There's no build step. JPEGs work if you just open `index.html`, but RAW decoding loads a Web Worker, which browsers block for files opened straight from disk. To test RAW locally, serve the folder:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Third-party code

RAW decoding uses LibRaw compiled to WebAssembly. See [`lib/libraw/NOTICE.md`](lib/libraw/NOTICE.md) for licenses.
