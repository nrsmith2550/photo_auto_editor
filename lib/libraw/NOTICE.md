# Third-party code: RAW decoding

The files in this folder are unmodified copies of **libraw-wasm 1.6.0** from npm (`dist/` folder), which is LibRaw compiled to WebAssembly.

| Component | Source | License |
| --- | --- | --- |
| libraw-wasm (JavaScript wrapper) | https://github.com/ybouane/LibRaw-Wasm | ISC |
| LibRaw (inside `libraw.wasm`) | https://www.libraw.org | LGPL 2.1 or CDDL 1.0, at your option |
| Little CMS (inside `libraw.wasm`) | https://www.littlecms.com | MIT |

To update, copy `index.js`, `worker.js`, `libraw.js` and `libraw.wasm` from a newer `libraw-wasm` release into this folder.
