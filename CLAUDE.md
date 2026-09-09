# ShipLabel

A single-file browser app: markup, CSS and JavaScript all live in `index.html`.
There is no build step and no install — open the file and it works, offline.

Keep it that way. No bundler, no npm, and nothing the app needs in order to
print may come from a CDN. (The ⬇ PDF button is the one exception: it fetches
html2canvas and jsPDF on demand and fails gracefully, since 🖨 Print → "Save as
PDF" covers the same job offline.)

## Working agreement

- **Always merge finished work to `main` and push it.** Develop on the working
  branch, then fast-forward `main` so the change can be seen and published.
  Don't wait to be asked.
- Verify changes in a real browser before reporting them as working. Chromium
  is at `/opt/pw-browsers/chromium-1194/chrome-linux/chrome` and Playwright is
  the usual way to drive it.
- Label geometry is measured in inches and comes from the `STOCKS` table. When
  adding a stock, take the numbers from the maker's own template rather than
  estimating, and centre the grid on the sheet.
