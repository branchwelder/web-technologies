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
