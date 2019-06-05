This is the central place to manage the Rhythms of Resistance tunesheets. The website and other places link to the generated files in this repository.

[`front.svg`](./front.svg) and [`back.svg`](./back.svg) contain the front and back cover. A `[month]` placeholder can be used to automatically fill in the current month+year.

[`network.odt`](./network.odt) is the description of the RoR network, principles, history and RoR Player.

[`tunes.ods`](./tunes.ods) contains the tune and dance sheets.


Styling guidelines
==================

Tune name
---------

18pt Arial bold, underlined by 2.5pt black double-line

Tune sign
---------

Right of tune name. 12pt Arial.

Groove
------

* Heading "Groove" 12pt Arial bold
* Beat numbers underlined by 1.75pt bold. No lines in between beats
* Instruments left-aligned, 9pt Arial
* Strokes centered, 9pt Arial. In between strokes 0.05pt #969696 vertical lines. In between beats 0.75pt black vertical lines. In between bars 1.75pt black vertical lines. No horizontal lines.
* One free line separating different instruments.

Breaks
------

* Break name: 10pt bold
* Break sign underneath break name, 9pt Arial italic
* Strokes same style as in Groove, but whole break surrounded by 0.75pt black vertical border.
* Any explanation right of break or underneath (right-aligned), 9pt Arial
* No free lines


Generate
========

PDF files are automatically generated and published when committing changes. If you added new pages to the tunesheet or moved pages around, make sure to update the page numbers in the [`make-sheets.sh`](./make-sheets.sh) script.

If you want to do a manual rebuild, follow one of the following instructions.

### Using docker

This is the most reliable way, as no dependencies/fonts (except docker) have to be installed.

```bash
docker run --rm -v "$PWD:/home/ror/sheetbook" rhythmsofresistance/sheetbook-build
```

### By hand

Make sure to have the [BTNGrilledCheese](./BTNGrilledCheese.zip) font and LibreOffice, Inkscape, pdftk, pdfjam and pdfnup installed.

Then run `./make-sheets.sh`.
