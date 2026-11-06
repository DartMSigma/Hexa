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

- Color picker with Hex, RGB, HSL, and OKLCH values
- Ready-made palettes generated from a chosen base color
- Optional Gemini palette generation using a Google AI Studio API key
- Color wheel, image color picker, and named CSS color browser
- Color harmonies, shades, tints, and tones
- WCAG contrast checker
- Light and dark themes

## Gemini palettes

1. Get an API key from [Google AI Studio](https://aistudio.google.com/apikey).
2. Open **Palettes**, choose a base color, and describe a mood or select a suggested mood.
3. Enter your Gemini API key and choose **Generate palettes**.

The key is used in the browser request to Google's Gemini API. Hexa does not save it. Do not embed a personal API key in a public deployment. The hosted page must allow requests to `generativelanguage.googleapis.com` for Gemini generation to work.

## Project files

- `index.html` — page structure and application logic
- `style.css` — site styles
- `fonts/bricolage-grotesque-latin.woff2` — locally hosted interface font (SIL Open Font License 1.1; see `fonts/OFL.txt`)
