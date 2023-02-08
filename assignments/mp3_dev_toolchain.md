# MP3: Dev Toolchain

MP3 is intended to introduce you to a modern web development toolchain in which
you structure and deploy an app which includes external dependencies. In this
project, you will learn how to install libraries, run a local development
server, bundle your code, and deploy your app.

**Initial submission deadline:** Tuesday, 21 February, before class. Submit a
link to your writeup via the Canvas assignment.

<!--
- Installing dependencies with `npm`
- Local development with `web-dev-server` (`wds`)
- Bundling with `rollup`
- Deploying your app with the `gh-pages` library -->

You can choose one of three tracks for this project. This project is mainly
about practicing developing an app using modern development tools, and I hope
that it can be an opportunity for you to explore a topic or particular library
you are interested in. **I will check in with you about your project direction
in class.**

1. **_A game._** Since we have just worked with p5, the obvious choice would be
   to use the p5.play library. However, I have provided links to other game
   frameworks if you are interested in exploring them.
2. **_An interactive data visualization._** A number of you indicated that you
   were interested in learning or practicing D3 in the introductory survey.
3. **_Something else._** If you have an idea for another mini project, ask me in
   class or send me a message on Discord. I will likely approve it, but I would
   like to check in with you about it first. For example, you could explore
   development with a component framework such as React.

## Project Requirements

- Your code must be in its own **public** Github repository.
- Your project must combine **at least two libraries** that are installed with
  NPM and recorded in your `package.json`. _Note: these do not include your
  development dependencies such as rollup._
- Your code must be bundled for deployment. You can continue to use rollup, but
  you are allowed (and encouraged) to explore other tools such as Webpack.
- Your project must be deployed. You can deploy to Github Pages with the
  `gh-pages` tool, but you are allowed (and encouraged) to explore other
  deployment options such as Firebase
- Your `package.json` must include `start`, `build`, and `deploy` scripts.
- Your main Github branch **must not include** your `node_modules` or `dist`
  folders.

## Instructions

1. Do the [in-class activity](/activities/06_toolchain.md) in order to walk
   through how to set up your own development toolchain.
2. Check in with Hannah (in-class on Thursday Feb 9) about your project
   direction.
3. Create a new **public** repository on Github and clone it to your computer.
4. Set up your development environment, following instructions in the dev
   toolchain activity. In short:
   - initialize a `package.json` with `npm`
   - install a local dev server and create a `start` script
   - add `index.html` and `index.js` files
   - start working on your app, using your dev server
   - install additional libraries with `npm` as you need them
   - write a `.gitignore` that ignores files in your `node_modules/` and `dist`
     folders
   - Commit and push your work to github regularly
   - Install a bundling tool, e.g. rollup, and create a configuration file and
     `build` script
   - Install a deployment tool, e.g. `gh-pages`, and use it to deploy your
     project using a `deploy` script
5. Regularly commit and push your code to Github. Additionally, regularly try to
   build and deploy your app. **Do not** wait until the last minute to work on
   deployment.

## What to submit

In addition to building your project, you should (as usual) complete a writeup
following the [writeup guidelines](/assignments/writeups). Your writeup should
link to your deployed project.

**Submit a link to your MP3 writeup in canvas.**

## Game Track

<!-- When working on your game, have a **win or loss condition**. -->

Read through
[these examples](https://creative-coding.decontextualize.com/making-games-with-p5-play/)
to see P5.play's core features.

A good place to start using the P5.play library is to follow
[this tutorial](https://workshops.hackclub.com/platformer/) from Hack Club.
Their [Atari Breakout tutorial](https://workshops.hackclub.com/atari_breakout/)
also shows a simple P5 game.

Some additional resources that might be helpful:

- [Making your sketches work on mobile](https://creative-coding.decontextualize.com/mobile/)
- [The future of web games](https://games.mozilla.org/)
- [List of game engines](http://jstherightway.org/#game-engines) from Javascript
  the right way
- [Tracery](https://github.com/galaxykate/tracery) A library for making grammars
  for stories
- [JavaScript Game Development Masterclass (Youtube Series)](https://www.youtube.com/playlist?list=PLYElE_rzEw_uryBrrzu2E626MY4zoXvx2)
- [Intro to creative coding cheatsheet](https://www.codecademy.com/learn/learn-p5js/modules/p5js-introduction-to-creative-coding/cheatsheet)

### Note: importing P5 when installed to `node_modules`

When you install P5 to `node_modules` and import it into your `index.js` file,
you have to write your code a little bit differently. This is the way you've
normally been writing your p5 setup and draw functions:

```js
function setup() {
  createCanvas(400, 400);
}

function draw() {
  if (mouseIsPressed) {
    fill(0);
  } else {
    fill(255);
  }
  ellipse(mouseX, mouseY, 80, 80);
}
```

When we install p5 to `node_modules`, we need to import it at the top of the
file. However, we also need to make our setup and draw functions global by
attaching them to the `window` object. All you need to do is change the p5
function signatures from `function setup()` to `window.setup = () =>`. That
changes the above sketch to this:

```js
import "p5";

window.setup = () => {
  createCanvas(windowWidth, windowHeight);
};

window.draw = () => {
  if (mouseIsPressed) {
    fill(0);
  } else {
    fill(255);
  }
  ellipse(mouseX, mouseY, 80, 80);
};
```

We have to do this because p5 creates a lot of global variables when it is
imported, and it expects `setup` and `draw` to be defined globally. This is a
quirk that is unique to P5 that I find a bit annoying.

## Data Viz Track

You can also look at the list of
[charting libraries](https://awesome.cube.dev/?tools=charts)

Some Data Viz resources:

- [D3 tutorials](https://observablehq.com/@d3/learn-d3)
- [charting libraries](https://awesome.cube.dev/?tools=charts)

<!-- ## Additional Resources

- [an introduction to NPM](https://nodejs.dev/en/learn/an-introduction-to-the-npm-package-manager/) -->
