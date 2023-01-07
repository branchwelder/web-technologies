# Web Technologies Slides

This directory contains the slide decks for each class session. I am still
trying to figure out the best way to create them, as I want to move away from
relying on services such as Google slides. My current approach is to write the
slides in Markdown and use [Pandoc](https://pandoc.org/) to convert them into a
[reveal.js](https://revealjs.com/) slide deck, which can be exported to PDF.

## Converting Markdown to Slide Decks

Pandoc has a few options for converting markdown to slides. I tried all of them
and found the [reveal.js]() approach to work best.

### Gotchas

I found that APT had a woefully outdated version of Pandoc, which meant that
support for reveal.js V4 didn't exist. I didn't realize this for a while and was
very frustrated because my slides were not generating correctly.
