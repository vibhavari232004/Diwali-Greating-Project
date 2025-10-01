# Diwali Greeting — Quick & Professional

A lightweight, client-side **Diwali greeting card generator** built with plain HTML, CSS and JavaScript. It produces a styled card preview in the browser and lets users copy the text or export the design as a PNG image.

---

## Features

* Simple, responsive UI with two-column preview + controls.
* Three built-in greeting styles: **Warm**, **Formal**, and **Fun**.
* Auto-generated greeting text using small template sets.
* Confetti animation and decorative lamp SVGs for festive look.
* Copy greeting text to clipboard.
* Download a high-resolution PNG export drawn on a `<canvas>`.
* Fully client-side — no build tools or server required.

---

## Files

* `index.html` — Single-file app containing HTML, CSS and JavaScript.

(If you renamed the file in your project, update the instructions below accordingly.)

---

## Usage

### Open locally

1. Open `index.html` directly in a modern browser (Chrome, Edge, Firefox, Safari). The app is pure front-end and will work without a server for most features.

2. Optional (recommended for full browser compatibility with downloads/clipboard): run a local static server.

* With Python 3:

  ```bash
  python -m http.server 8000
  # then open http://localhost:8000 in your browser
  ```

* With VS Code: install the **Live Server** extension and click *Go Live*.

### How to use

1. Enter the **Recipient / Short prompt** (e.g. name or group).
2. Optionally add a **Short custom note** (adds context to the generated message).
3. Choose a **Style** from the dropdown.
4. Click **Generate Greeting** to update the preview. The card shows a heading, a main greeting line, a subline and a from line.
5. Use **Copy** to copy the card text to clipboard.
6. Use **Download PNG** to export a high-resolution image of the card.

---

## Customization

* **Templates:** Edit the `TEMPLATES` object in the script to change or extend greeting messages for each style.
* **Typography & Colors:** Modify CSS variables at the top of the `<style>` block (`:root`) to change theme colors and accents.
* **PNG export size:** In the `downloadBtn` handler, change `canvas.width` and `canvas.height` to alter the exported image resolution.
* **Add more decorations:** The left/right lamps are inline SVGs in the HTML — replace or edit them to change visuals.

---

## Accessibility & Compatibility

* The UI uses semantic HTML controls. For better accessibility, consider adding `aria-label` and more explicit focus styles.
* Clipboard copying uses the modern Clipboard API (`navigator.clipboard`). Some browsers may require a user gesture or secure context (HTTPS/localhost).
* The canvas export uses fonts available on the client. For consistent typography in the PNG across machines, embed or draw webfonts onto the canvas (more advanced).

---

## Troubleshooting

* **Copy fails:** Browser blocked clipboard access. Try running the page via `http://localhost` or give permission in browser settings. Alternatively select text manually and copy.
* **Download doesn't work:** Some browsers restrict `canvas.toDataURL()` in file:// context. Use a local server or run on HTTPS.
* **Text wrapping/overflow in PNG:** Adjust `wrapText()` parameters (`maxWidth`, `lineHeight`) and the font sizes in the download function.

---

## Deployment

This is a static page — deploy to GitHub Pages, Netlify, Vercel, or any static host by uploading `index.html`.

Example GitHub Pages (repository `gh-pages` branch or `docs/`): push `index.html` and enable Pages in repo settings.

---

## Attribution

* Decorative elements: inline SVG lamps and simple confetti created directly in the markup and CSS.
* Built with plain HTML, CSS and vanilla JavaScript.

---

## License

Use and modify freely. Add a license file if you want to specify terms (e.g., MIT).

---



