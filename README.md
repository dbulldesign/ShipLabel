# Shiplabel

A single-file web app for typing up shipping and address labels and printing
them onto pre-cut label sheets. Open `index.html` in a browser — there is
nothing to install and nothing leaves your machine.

## Label types

Pick the stock from the **Label** menu in the toolbar; the preview, the print
page size and the PDF export all follow it.

| Stock | Label | Per sheet | Sheet |
| --- | --- | --- | --- |
| Uline S-5049G | 8½ × 5½″ | 2 | Letter |
| Uline S-17049G | 4¼ × 5½″ | 4 | Letter |
| Uline S-6229G | 4 × 6″ | 4 | Legal (8½ × 14″) |
| Uline S-5048G | 4 × 2½″ | 8 | Letter |
| Uline S-3847G | 4 × 2″ | 10 | Letter |
| Uline S-5047G | 2⅝ × 1″ | 30 | Letter |
| Avery 8165 | 8½ × 11″ full sheet | 1 | Letter |
| Avery 5168 | 3½ × 5″ | 4 | Letter |
| Avery 5164 | 4 × 3⅓″ | 6 | Letter |
| Avery 5162 | 4 × 1⅓″ | 14 | Letter |
| Avery 5161 | 4 × 1″ | 20 | Letter |
| Dymo Small 30251 | 3½ × 1⅛″ | 1 | Roll, one per label |
| Dymo Large 30321 | 3½ × 1⅖″ | 1 | Roll, one per label (address) |
| Dymo Large 30323 | 4 × 2⅛″ | 1 | Roll, one per label (shipping) |
| Thermal | 4 × 6″ and 4 × 2″ | 1 | One label per page |

The Uline measurements are read out of Uline's own Word templates. Anything
else goes under **Custom size…**, which takes the page size, the grid, the
label size, the margins and the gaps between labels in inches.

## Two kinds of rotation

**Portrait / Landscape** turns the whole sheet. The die-cut doesn't move when
you rotate a sheet, so the grid rotates with the paper — the labels still line
up, but the text now runs along the label's other edge. Feed the sheet into the
printer rotated to match. For one-per-page stocks it simply swaps the media
size, so a 4 × 6″ thermal label prints as 6 × 4″.

**⟳ Text** turns the text on one label, leaving the sheet alone. Click it to
step through 90°, 180° and 270°. It applies to the label you're editing, like
bold or ↕ Middle, so labels on the same sheet can face different ways — useful
when a long address only fits down a narrow label. Shrink-to-fit measures the
turned box, so text is fitted against the edge it actually runs along.

The two combine: a sheet can be landscape and a label on it turned as well.

## Making labels

**Type them** one at a time, or press **📋 Import** to make a batch from a
pasted list or a CSV/TSV file — one label per line, blank lines separating
multi-line addresses, or one label per spreadsheet row.

**× copies** repeats a label. Put `{n}` and `{of}` in the text and each copy is
numbered, so one entry set to 12 copies prints BOX 1 OF 12 through BOX 12 OF 12.

**▊ Barcode** and **▦ QR** put a real, scannable code on the label. Both are
generated inside the page, so they work with no internet. Code 128 takes any
plain keyboard text; QR holds up to 216 characters, including accents. A saved
sheet stores the *value*, and the picture is always redrawn from it.

**🖼 Image** drops in a logo or photo. Big pictures are scaled down so saved
sheets stay small; PNGs keep their transparency.

**＋ Text box** adds another box of text to the label. Each box can be dragged
by its grip and resized from its corner, and holds its own font, size and
alignment — so a return address, a big destination and a barcode can each sit
where you want them. Boxes are stored as a share of the label, so switching
label type keeps the layout in proportion.

**Insert…** has the usual shipping marks (FRAGILE, THIS SIDE UP and so on), and
**＋ Block** keeps the current label's text as a named block — a return address,
say — to reuse on any later label.

Text can sit at the **top, middle or bottom** of the label, and **⟳ Text** turns
it a quarter turn at a time. While you are typing in a turned label the card
swings upright so you can read what you are writing — the line breaks stay
exactly as they will print — and it turns back as soon as you click away. The
note in the label's bar tells you which way it will come out of the printer.

**Text** sets what happens when the text doesn't match its box: *Shrink to fit*
scales it down when it would run over (and says "shrunk to 60%" on the label,
so a point size that appears to do nothing is explained), *Fill the box* scales
it up or down so it uses the whole box — the usual choice for a Dymo label —
and *Leave as typed* prints exactly the point size you picked.

**Right-click** a text box for its alignment, barcode, QR, picture, and the
label's rotate/duplicate/delete. Right-click anywhere else for the text fit,
orientation, printer alignment and print.

Work is **saved as you go** and comes back when you reopen the page. **💾 Save**
writes a file you can keep or send on; **🗑 New** starts a clean sheet; **↩ Undo**
brings back a label you deleted.

### Dymo and other roll printers

A Dymo LabelWriter that is installed on the computer (including a wireless one
joined to your network) shows up in the browser's print dialog like any other
printer — pick it under 🖨 Print. Choose the label type that matches the roll you have loaded — 30251,
30321 or 30323 — first so the page is exactly one label, and set the same
label size in the Dymo driver. If a label comes out turned the wrong way,
**▭ Landscape** flips it.

**If it prints tiny, the paper sizes don't match.** The browser only prints at
the label's real size when the driver is set to that same size; otherwise it
drops the little page onto whatever paper is selected and the label ends up a
fraction of the sheet. Set the driver's paper to the label size and the print
dialog's scale to 100% (not "Fit to page"). The app shows a reminder of the
exact size to pick whenever a one-per-page label type is chosen.

## Printing

**Start at** lets you finish a part-used sheet: set it to the first label still
on the sheet and printing skips the ones already peeled off.

**⇔ Align** shifts everything by hundredths of an inch to correct a printer that
prints slightly off, remembered per label type and orientation. **Print test
grid** puts the label outlines on paper so you can hold a real sheet against it.



Print at 100% / "Actual size" with page scaling off, and check the first sheet
against a blank one before committing a stack of labels.
