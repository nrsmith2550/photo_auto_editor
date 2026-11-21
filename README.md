# Event Photo Auto-Editor

A browser-based batch editor for event photographers. Drop in a set of photos, pick an event style, check a few frames, and export the whole set edited as a ZIP.

**Live app:** https://nrsmith2550.github.io/photo_auto_editor/

## Features

- **7 event styles:** Wedding: Light & Airy, Wedding: Warm Film, Corporate & Headshots, Party & Nightlife, Outdoor Golden Hour, Classic B&W, Natural. A strength slider sets how strongly each one is applied.
- **Auto-correction:** white balance, exposure and levels are fixed before the style is applied, so shots from mixed lighting come out consistent.
- **Portrait retouching:** edge-aware skin smoothing that keeps eyes, lashes and hair sharp.
- **Per-photo control:** 13 sliders, a before/after comparison, and "copy to all".
- **Batch export:** full resolution or resized, at your choice of JPEG quality, downloaded as a ZIP.

## Privacy

Everything runs in your browser. Photos are never uploaded anywhere.

## Limits

- Accepts JPEG, PNG and WebP only. Export RAW or HEIC files to JPEG first.
- EXIF metadata isn't copied to the exported files.
- Skin smoothing works by color, so warm wood, sand or orange walls can get slightly softened. Lower the Skin smoothing slider on those shots.

## Running locally

Open `index.html` in Chrome, Edge, Firefox or Safari. There's no build step and nothing to install.
