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

Generate with a default theme:

```sh
pandoc -t revealjs -s input.md -o output.html -V theme=night
```

To add custom css:

```sh
pandoc -t revealjs -s input.md -o output.html --css=slides.css
```

My current command:

```sh
pandoc -t revealjs -s input.md -o output.html -V transition=none -V center=false --css=slides.css
```

## Print to PDF

Open your presentation with print-pdf included in the query string, for example:
http://localhost:8000/?print-pdf. You can test this at
revealjs.com/demo?print-pdf. Open the in-browser print dialog (CTRL/CMD+P).

<!-- ## Converting Markdown to Slide Decks

Pandoc has a few options for converting markdown to slides. I tried all of them
and found the [reveal.js]() approach to work best.

### Gotchas

I found that apt had a woefully outdated version of Pandoc, which meant that
support for reveal.js V4 didn't exist. I didn't realize this for a while and was
very frustrated because my slides were not generating correctly. -->
