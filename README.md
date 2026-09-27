# RedPen · PDF Text Editor

A single-file, in-browser PDF text editor. Open a PDF, click any line to rewrite it, add new text anywhere, and export a fresh PDF. Everything runs client-side — no server, no uploads, nothing leaves the browser.

## Live demo

Once GitHub Pages is enabled (see below), it runs at:

    https://<your-username>.github.io/<repo-name>/

## Deploy in three steps

1. Create a new GitHub repo and add these two files at the root:
   - `index.html`
   - `README.md`
2. Go to **Settings → Pages**.
3. Under **Build and deployment → Source**, pick **Deploy from a branch**, choose `main` (or `master`) and the `/ (root)` folder, then **Save**.

Give it a minute, then open the URL above. That's it.

## How to use it

- **Open PDF** — every page renders on screen.
- **Click a line of text** — it becomes editable. Rewrite it, or clear it to delete that text.
- **Add text** — click anywhere on a page to drop in new text.
- **Cover / Ink** — the fill color used to hide the original text, and the color of your new text.
- **Export edited PDF** — downloads `edited.pdf` with your changes baked in.

## How it works

Edits are made by covering the original text with a filled rectangle and redrawing your version on top. This is clean on white pages and simple layouts (letters, invoices, forms, most Word / Docs / Pages exports).

Expect some drift on:
- Colored or textured backgrounds — match the background with the **Cover** color picker.
- Rotated text or tight multi-column layouts.
- Exotic embedded fonts — redrawn text falls back to a close standard font (Helvetica / Times / Courier).
- Scanned PDFs — those are images with no text to grab, so there's nothing to edit.

## Built with

- pdf.js — rendering pages and reading text positions.
- pdf-lib — writing the edited PDF.

Both load from a CDN, so the page needs an internet connection the first time it runs.

## License

MIT — do whatever you like with it.