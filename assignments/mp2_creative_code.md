# MP2: Creative Coding Explorations

We will be exploring the wonderful P5.js library to create a series of sketches,
starting with a simple artwork generator and finishing with an interactive audio
visualizer. All of your sketches will be organized into a gallery page on you
portfolio website.

**Initial submission deadline:** Tuesday, 7 February, before class. Submit a
link to your writeup via the Canvas assignment.

## Getting Started

Follow [this tutorial](https://p5js.org/get-started/) from the P5.js
documentation to get up and running with your first sketch using their web
editor. The web editor is a great place to quickly iterate on your sketches.
When it's time to move a sketch to your portfolio site, you can simply copy and
paste your code into a JavaScript file.

## Required Sketches

The required sketches increase in complexity. As you work through them, I
recommend watching videos from the Coding Train's
[Programming with p5.js](https://thecodingtrain.com/tracks/code-programming-with-p5-js)
series. Your final gallery must include one sketch in each category, however,
_you are encouraged to make more._ As you work on this assignment, you will
naturally create slight variations of each sketch as you tweak parameters. I
encourage you to make copies of the different variations to fill out your
gallery page! At a minimum, your final sketch gallery should include a sketch in
each of the below categories.

**Sketch One: Static.** Generate a static artwork. It should include some
computational complexity (e.g. iteration, conditionals - you should't specify
each shape manually). To get started, read about the
[coordinate system and shapes](https://p5js.org/learn/coordinate-system-and-shapes.html)
on the P5 website.

_Coding Train:_

- [Shapes and Drawing](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/1-intro/3-shapes-drawing)
- [Color](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/1-intro/4-color)
- [While and For Loops](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/4-loops/1-while-for)
- [Nested Loops](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/4-loops/2-nested)
- [Arrays](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/7-arrays/1-arrays)
  and
- [Arrays and Loops](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/7-arrays/2-arrays-loops)

_Examples:_

- [Lines](https://p5js.org/examples/data-true-and-false.html)
- [Basic shapes](https://p5js.org/examples/form-shape-primitives.html)
- [More basic shapes](https://p5js.org/examples/hello-p5-simple-shapes.html)
- [Gray targets](https://p5js.org/examples/structure-functions.html)
- [Iteration](https://p5js.org/examples/control-iteration.html)
- Iteration and Conditionals
  [example one](https://p5js.org/examples/control-conditionals-1.html) and
  [example two](https://p5js.org/examples/control-conditionals-2.html)
- [Nested Iteration](https://p5js.org/examples/control-embedded-iteration.html)
- [Drawing from a 2d array](https://p5js.org/examples/arrays-array-2d.html)
- [A static pattern](https://p5js.org/examples/structure-width-and-height.html)
- You could also attempt Matt DesLauriers'
  [Exercise 1](https://github.com/mattdesl/workshop-p5-intro/blob/master/exercises/1-drawing.md)
  (solution included)
- [Recursive circles](https://p5js.org/examples/structure-recursion.html)

**Sketch Two: Random.** Generate a static artwork that incorporates some
randomness - in other words, every time you reload the page, the output should
be different.

_Coding Train_

- [Random](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/2-variables/4-random)

_Examples:_

- [Random lines](https://p5js.org/examples/math-random.html)
- [Random chords](https://p5js.org/examples/math-random-chords.html)
- [Random rects](https://glitch.com/edit/#!/p5-example-random-rects)
- You could also try this
  [Hard-Edge Painting](https://github.com/mattdesl/workshop-p5-intro/blob/master/exercises/3-painting.md)
  exercise.

**Sketch Three: Infinite Loop.** This sketch should change over time. You can
accomplish this by changing the value of some variable in your `draw()`
function. For example, you could change a shape's size or hue.

_Coding Train_

- [Bouncing ball](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/3-conditionals/2-bouncing)

_Examples:_

- [Translating squares](https://p5js.org/examples/transform-translate.html)
- [Rotating square](https://glitch.com/edit/#!/p5-example-loop)
- [Transforming and scaling squares](https://p5js.org/examples/transform-scale.html)
- [Spinning stars](https://p5js.org/examples/form-star.html)
- [Bouncing circle](https://p5js.org/examples/motion-bounce.html)
- [Breathing circle](https://glitch.com/edit/#!/p5-example?path=sketch.js)
- [Looping Hexagon](https://glitch.com/edit/#!/p5-example-hexagon)
- [Sine wave](https://p5js.org/examples/math-sine-wave.html)
- [Jittery motion based on perlin noise](https://p5js.org/examples/math-noise1d.html)

**Sketch Four: Interactive.** This sketch should respond to human input.

_Coding Train_

- [Conditionals](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/3-conditionals/3-else-if-and-or)
- [Boolean Variables](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/3-conditionals/4-boolean)
- [MouseX and MouseY](https://thecodingtrain.com/tracks/code-programming-with-p5-js/code/2-variables/1-mouseX-mouseY)

_Examples:_

- [Transforming numbers with a map](https://p5js.org/examples/math-map.html)
- [Circle sizes depend on mouse distance](https://p5js.org/examples/math-distance-2d.html)
- [Draw circles based on mouse speed](https://p5js.org/examples/drawing-patterns.html)
- [Draw lines by dragging the mouse](https://p5js.org/examples/drawing-continuous-lines.html)
- [Draw a pulsing line](https://p5js.org/examples/drawing-pulses.html)
- [Change hue based on mouse position](https://p5js.org/examples/color-hue.html)
- [Draw lots of colorful circles based on mouse position](https://editor.p5js.org/branchwelder/full/rgeVRA-O4)
- [Tickle Jitter](https://p5js.org/examples/interaction-tickle.html)
- [Kaleidoscope drawing tool](https://p5js.org/examples/interaction-kaleidoscope.html)

**Sketch Five: Audio** This sketch should output some audio. Keep in mind that
most browsers require some user interaction with the page (e.g. a click) before
they play audio. See
[this post](https://creative-coding.decontextualize.com/synthesizing-analyzing-sound/)
for a comprehensive introduction to P5.sound.

_Examples:_

- [Loading an mp3](https://p5js.org/examples/sound-load-and-play-sound.html)
- [Play a sound effect](https://p5js.org/examples/sound-sound-effect.html)
- [Generating a tone](https://glitch.com/edit/#!/tone-example-tap?path=sketch.js)
- [Generating a drum noise](https://p5js.org/examples/sound-noise-drum-envelope.html)
- [Directional sound](https://p5js.org/examples/sound-pan-sound.html)
- [Overlapping sound from file](https://p5js.org/examples/sound-play-mode.html)
- [Measuring sound amplitude](https://p5js.org/examples/sound-measuring-amplitude.html)

**Sketch Six: Audio and Visuals** Must create (or analyze) a sound _and_ produce
visuals based on some user input. What the input events are are up to you - it
could be someone talking into a microphone, tapping on the keyboard, or clicking
and dragging with the mouse.

_Examples:_

- [Falling keys (by hannah)](https://editor.p5js.org/branchwelder/sketches/cOrvIAY1O)
- [Light-up keyboard](https://p5js.org/examples/hello-p5-song.html)
- [Circle radius responds to loudness](https://glitch.com/edit/#!/dfpi-audio-mic?path=sketch.js) -
  _uses the microphone as input_

## Resources

- The official [p5.js reference docs](https://p5js.org/reference/) and the
  [p5.sound reference](https://p5js.org/reference/#/libraries/p5.sound)
- [The Coding Train](https://thecodingtrain.com/) a.k.a Daniel Shiffman,
  particularly his
  [Programming with p5.js track](https://thecodingtrain.com/tracks/code-programming-with-p5-js).
  The series starts off assuming no programming knowledge, so it might seem a
  bit basic at first, but it is a fantastic introduction to P5 and Dan is a
  great teacher.
- Matt DesLauriers' cheatsheets:
  - [General snippets](https://github.com/mattdesl/workshop-p5-intro/blob/master/docs/snippets.md)
  - [Functions](https://github.com/mattdesl/workshop-p5-intro/blob/master/docs/functions.md)
  - [Timers](https://github.com/mattdesl/workshop-p5-intro/blob/master/docs/timers.md)
- List of [P5 Libraries](https://p5js.org/libraries/)

## Example galleries

These are galleries of example sketches that I encourage you to look at for
inspiration.

- Matt DesLauriers' demo galleries. These are simple examples that are good for
  showing individual concepts. They range widely in complexity.
  - Gallery of [visual examples](https://p5-demos.glitch.me/)
  - Gallery of [audio examples](https://tone-demos.glitch.me/)
- P5.js [examples](https://p5js.org/examples/) page from the documentation -
  _these are (mostly) basic examples demonstrating core functionality of the
  library._
- OpenProcessing's [trending page](https://openprocessing.org/discover/) - _many
  of these are more advanced than I expect you to do for this project, but they
  serve as a wonderful example of how far you can go with p5 and Processing_

## What to turn in

- **Your sketches** (minimum 6)
  - Hosted on your portfolio site and organized into a sketch gallery (described
    below)
  - When I open your sketch, it should cover the full window (i.e. the canvas
    size should be set from the window height and width. Your code should also
    resize the canvas appropriately when the window is resized.
- **A gallery page** displaying your work
  - Hosted on your portfolio website
  - A screenshot (if static) or gif (if interactive) which links to each sketch
- The **MP2 writeup**
  - Follows the [writeup guidelines](/assignments/writeups.md)
  - Hosted on your portfolio website, as before

You should submit a link to your writeup on Canvas.

## Suggested timeline

As this is a five-credit class, you are expected to work outside of class for
approximately 10 hours per week. Because you have two weeks to work on this
project, you should work outside of class about 20 hours on MP2. This includes
working on your sketches, reading documentation/tutorials, watching videos,
assembling your sketches into a gallery for your portfolio, and completing the
writeup.

For those of you who appreciate scaffolding, here are a series of suggested
intermediate milestones:

### Thursday, Jan 26

- Make drafts of sketches One, Two, and Three
- In class activity on CSS layouts/creating a gallery page

### Tuesday, Jan 31

- Make drafts of Sketches 3 and 4, and link to them from your gallery page
- Add screenshots of each sketch to the gallery page

### Thursday, Feb 2

- Finish Sketch 5 and have ideas/draft of Sketch 6
- Create an outline of your writeup

### Tuesday, Feb 7 (MP2 due)

- Finish Sketch 6 and finalize your gallery page
- Finish your writeup and post it to your portfolio
- Submit a link to your writeup in Canvas
