# Web Technologies Slides

This directory contains the slide decks for each class session. I am still
trying to figure out the best way to create them, as I want to move away from
relying on services such as Google slides. My current approach is to write the
slides in Markdown and use [Pandoc](https://pandoc.org/) to convert them into a
[reveal.js](https://revealjs.com/) slide deck, which can be exported to PDF.

## quick start...

Install [`pandoc`](https://pandoc.org). The `apt` version is outdated and
doesn't work with [reveal.js](https://revealjs.com/) 4.x. Use the `.deb`
installer instead. The documentation on generating slides is
[here](https://pandoc.org/MANUAL.html#slide-shows).

My current command:

```sh
pandoc -t revealjs -s input.md -o output.html -V transition=none -V pdfSeparateFragments=false --css=slides.css
```

## Saving to PDF

- Open your presentation with print-pdf included in the query string, for
  example: http://localhost:8000/?print-pdf. You can test this at
  revealjs.com/demo?print-pdf.
- Open the in-browser print dialog (CTRL/CMD+P).
- Change the Destination setting to Save as PDF.
- Change the Layout to Landscape.
- Change the Margins to None.
- Enable the Background graphics option.
- Click Save 🎉
