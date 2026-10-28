# InVertex

Adaptive text contrast tool. Text renders with `mix-blend-mode: difference`, so every glyph inverts its own background live. No dependencies, single HTML file.

## Use

Open `invertex.html` in a browser, or serve the folder with any static host (GitHub Pages works as-is).

- **Edit text** — type anything (multi-line supported)
- **Upload** — use your own photo, or **Shuffle** for a random one
- **Background** — photo / animated gradient / stripes
- **Colour** — 8 text colours (white = classic full inversion)
- **Size** — font size slider
- **Mode** — `difference` (hard invert) or `exclusion` (soft invert)
- **Drag** — pan the background anywhere; drag the type anywhere; both adapt live

## Export

- **Copy** — production-ready CSS for the current settings
- **Export PNG** — 2x render of the current composition (background + blended text), recomputed pixel-by-pixel on canvas

## Notes

- The default background is an inline SVG gradient, so PNG export works offline.
- Remote shuffle photos are fetched through a CORS-clean copy; if a host blocks it, export falls back with a toast prompt.
- PNG export re-implements the blend in canvas (`|bg - fg|` per pixel), matching the CSS result.

## License

MIT
