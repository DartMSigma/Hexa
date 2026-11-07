# Hexa

Hexa is a browser-based color toolkit for exploring colors, building palettes, and checking contrast. It runs as a static site with no build step.

## Run locally

Start a static file server from this folder:

```powershell
python -m http.server 3000
```

Then open [http://localhost:3000](http://localhost:3000).

Alternatively, open `index.html` directly in a browser. The Gemini palette generator may require serving the page from a host that allows browser requests to Google's API.

## Features

- Remembers your selected color in this browser
- Color picker with Hex, RGB, HSL, and OKLCH values
- Ready-made palettes generated from a chosen base color
- Palette workspace with a live base-color preview, copyable hex, and quick base-color actions
- Consistent in-page color selectors for palette, contrast, and gradient controls, with keyboard-accessible saturation, brightness, and hue adjustment
- Dedicated Gradient tab with editable color stops, per-stop opacity, angle control, live preview, quick starts, reverse, and CSS export
- Optional Gemini palette generation using a Google AI Studio API key
- Image color picker with drag-and-drop, a pixel magnifier, local preview, and detected color swatches
- Harmony picker styled to match the site, with keyboard navigation
- Color harmonies that select colors, plus shades, tints, and tones that copy their hex codes
- Contrast checker with a centered reverse action, a live sample, and clear WCAG AA/AAA pass/fail results
- Fixed dark theme
- Subtle page, menu, and palette animations that respect reduced-motion preferences

## Gemini palettes

1. Get an API key from [Google AI Studio](https://aistudio.google.com/apikey).
2. Open **Palettes**, choose a base color, and describe a mood or select a suggested mood.
3. Enter your Gemini API key and choose **Generate palettes**.

The key is used in the browser request to Google's Gemini API. Hexa does not save it. A static page cannot protect a key that it stores for later, so the API key is not persisted. Do not embed a personal API key in a public deployment. The hosted page must allow requests to `generativelanguage.googleapis.com` for Gemini generation to work.

## Saved preferences

Hexa stores only your selected color in this browser's local storage. This value stays in the browser for this site and is not sent to Hexa or another server. Clearing this site's browser data removes it. The Gemini API key is never stored.

## Project files

- `index.html` — page structure and application logic
- `style.css` — site styles
- `fonts/bricolage-grotesque-latin.woff2` — locally hosted interface font (SIL Open Font License 1.1; see `fonts/OFL.txt`)
