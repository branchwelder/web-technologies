# MP3: Dev Toolchain

MP3 is intended to introduce you to a modern web development toolchain in which
you structure and deploy an app which includes external dependencies. In this
project, you will learn how to install libraries, run a local development
server, bundle your code, and deploy your app.

**Initial submission deadline:** Tuesday, 21 February, before class. Submit a
link to your writeup via the Canvas assignment.

You can choose one of three tracks for this project. This project is mainly
about practicing developing an app using modern development tools, and I hope
that it can be an opportunity for you to explore a topic or particular library
you are interested in. **I will check in with you about your project direction
in class.**

1. **_A game._** Since we have just worked with p5, the obvious choice would be
   to use [the p5.play library](https://p5play.org/index.html). However, I have
   provided links to other game frameworks if you are interested in exploring
   them.
2. **_An interactive data visualization._** A number of you indicated that you
   were interested in learning or practicing D3 in the introductory survey.
3. **_Something else._** If you have an idea for another mini project, ask me in
   class or send me a message on Discord. I will likely approve it, but I would
   like to check in with you about it first. For example, you could explore
   development with a component framework such as React.

## Project Requirements

- Your code must be in its own **public** Github repository.
- Your project must combine **at least two libraries** ~~that are installed with
  NPM and recorded in your `package.json`.~~
  - **NOTE:** Due to the issues installing P5/P5.play with NPM, installing your project libraries (e.g. P5 and P5.play) with NPM is no longer a requirement and you are instead allowed to link to a CDN in your `index.html` in order to import them. You still are required to install the *dev dependencies* (dev server, bundler, and deployment tool) with NPM. **See my messages in Discord for more information, and ask any questions there.**
- Your code must be bundled for deployment. You can continue to use rollup, but
  you are allowed (and encouraged) to explore other tools such as Webpack.
- Your project must be deployed. You can deploy to Github Pages with the
  `gh-pages` tool, but you are allowed (and encouraged) to explore other
  deployment options such as Firebase.
- Your `package.json` must include `start`, `build`, and `deploy` scripts, which run your dev server, build tool, and deploy tool, respectively.
- Your main Github branch **must not include** your `node_modules` or `dist`
  folders. (They should be ignored in a `.gitignore`)

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

**DO NOT submit a link to a writeup that does not exist with the intent to edit it later.** Canvas takes screenshots of any website link you submit, so the state of your writeup at time of submission is recorded. Additionally, **we can see your entire git commit history, with timestamps** and can easily tell what the status of your writeup was at time of submission.

## Game Resources

If you are creating a game, your game should have an end condition. Anyone who
plays your game should know when the game is over. For example, this could be a
high score representing the number of enemies killed or the time the player
spends alive.

Allison Parrish's
[examples](https://creative-coding.decontextualize.com/making-games-with-p5-play/)
demonstrate P5.play's core features. It is likely that a basic example for any
feature you want to add to your game can be found on this page. The P5.play
[reference](https://p5play.org/learn/) is an excellent resource that will
supplement the base p5 documentation. Their [demos](https://p5play.org/demos/)
show a series of simple concepts and games that you can use to get started.

If you would like a step-by-step introduction,
[this tutorial](https://workshops.hackclub.com/platformer/) walks you through
how to use P5.play to create an endless runner.. This
[Atari Breakout tutorial](https://workshops.hackclub.com/atari_breakout/) also
shows a simple P5 game.

**I made you an
[example](https://github.com/branchwelder/example-game) that shows what your game repository should look like.**

Some additional resources that might be helpful:

- [Making your sketches work on mobile](https://creative-coding.decontextualize.com/mobile/)
- [JavaScript Game Development Masterclass (Youtube Series)](https://www.youtube.com/playlist?list=PLYElE_rzEw_uryBrrzu2E626MY4zoXvx2)
- [Intro to creative coding cheatsheet](https://www.codecademy.com/learn/learn-p5js/modules/p5js-introduction-to-creative-coding/cheatsheet)
- [The future of web games](https://games.mozilla.org/)
- [List of game engines](http://jstherightway.org/#game-engines) from Javascript
  the right way
- [Tracery](https://github.com/galaxykate/tracery) - a library for making
  grammars for stories

<!-- ### Note: importing P5 when installed to `node_modules`

When you install P5 to `node_modules` and import it into your `index.js` file,
you have to write your code a little bit differently. This is the way you've
normally been writing your p5 setup and draw functions:

```js
let spr;

function setup() {
  createCanvas(windowWidth, windowHeight);
  spr = createSprite(width / 2, height / 2, 40, 40);
  spr.shapeColor = color(255);
}

function draw() {
  background(50);
  spr.position.x = mouseX;
  spr.position.y = mouseY;
  drawSprites();
}
```

When we install p5 to `node_modules`, we need to import it at the top of the
file. However, we also need to make our setup and draw functions global by
attaching them to the `window` object. All you need to do is change the p5
function signatures from `function setup()` to `window.setup = () =>`. That
changes the above sketch to this:

```js
let spr;

window.setup = () => {
  createCanvas(windowWidth, windowHeight);
  spr = createSprite(width / 2, height / 2, 40, 40);
  spr.shapeColor = color(255);
};

window.draw = () => {
  background(50);
  spr.position.x = mouseX;
  spr.position.y = mouseY;
  drawSprites();
};
```

We have to do this because p5 creates a lot of global variables when it is
imported, and it expects `setup` and `draw` to be defined globally. This is a
quirk that is unique to P5 that I find a bit annoying. -->

## Data Viz Resources

You are allowed to use any charting library you wish. There is a nice list
[here](https://awesome.cube.dev/?tools=charts). However, I have experience with
D3 and will be able to best help you with it. If you are new to D3,
[D3.js - a practical introduction](https://www.youtube.com/watch?v=TOJ9yjvlapY)
is a great overview video that walks you through the basic functionality of the
library. I also recommend going through this
[excellent tutorial series](https://michaeloppermann.com/d3) from Michael
Opperman. In particular, the
[Intro to D3](https://github.com/michael-oppermann/d3-learning-material/tree/main/d3-tutorials/1_d3_tutorial)
post has everything you need to know to get started.

I have made a [basic example](https://github.com/branchwelder/example-viz) that
loads data fr0m a CSV and draws rectangles based on the contents.

Your have two options for getting the data that you visualize:

1. Download a dataset from some source and add it to your repository. _**Note**:
   be mindful of the size of your dataset._
2. Use the JavaScript
   [fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
   to request data from an API.
   - if you are using D3, D3 also has a `d3-fetch` library that you can use.
     [Example here](https://www.geeksforgeeks.org/d3-js-d3-fetch-api/)

Some resources:

- [An intro to D3 in 10 basic examples](https://d3-graph-gallery.com/intro_d3js.html)
- [D3 tutorials](https://observablehq.com/@d3/learn-d3) on Observable (an online
  environment similar to Jupyter notebooks)
- [charting libraries](https://awesome.cube.dev/?tools=charts)
- [Introduction to Fetch](https://web.dev/introduction-to-fetch/)
- [Fetch and display data from an API](https://w3collective.com/fetch-display-api-data-javascript/)
- Google


## Resources

- [An Absolute Beginner's Guide to NPM](https://nodesource.com/blog/an-absolute-beginners-guide-to-using-npm/)
- [What is NPM and why do we need it?](https://www.youtube.com/watch?v=P3aKRdUyr0s)
- [Rollup Cheatsheet](https://devhints.io/rollup)
- [Rollup-plugin-copy](https://www.npmjs.com/package/rollup-plugin-copy)
- [Comparing the next generation of build tools](https://css-tricks.com/comparing-the-new-generation-of-build-tools/)

## Tips

### Check your P5/P5.play versions!

I noticed some people were using  very outdated versions of P5 (version 0.7.2 or something, when the latest is something like 1.5.) Keep an eye out for this, especially if you are building off things you find online that might have been posted a long time ago! Features can vary greatly across versions of libraries, and deprecated features might not work in the way you expect. These are the links that my example game uses, which you are free to copy and paste into your `index.html` file:

```html
<script src="https://cdn.jsdelivr.net/npm/p5@1/lib/p5.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/p5@1/lib/addons/p5.sound.min.js"></script>
<script src="https://unpkg.com/@free-side/audioworklet-polyfill/dist/audioworklet-polyfill.js"></script>

<script src="https://cdn.jsdelivr.net/npm/planck@latest/dist/planck.min.js"></script>
<script src="https://p5play.org/v3/p5play.js"></script>
```

### Copying folders to `dist/` with `rollup`

If a `rollup.config.js` file which copies `index.html` to the `dist` folder looks like this:


```js
import copy from "rollup-plugin-copy";

module.exports = {
  input: "index.js",
  output: {
    dir: "dist",
  },
  treeshake: false,
  plugins: [
    copy({
      targets: [{ src: "index.html", dest: "dist" }]
    })
  ],
};
```

Making it also copy a folder called `images` would look like this:


```js
import copy from "rollup-plugin-copy";

module.exports = {
  input: "index.js",
  output: {
    dir: "dist",
  },
  treeshake: false,
  plugins: [
    copy({
      targets: [{ src: ["index.html", "images"], dest: "dist" }]
    })
  ],
};
```

### Adding things to `.gitignore` after they were committed

When you list files/directories in your `.gitignore`, any changes to them are *ignored* by default. They won't be *deleted* if they already exist somewhere. This means that if you add files to your local `.gitignore` which already exist on Github, it won't delete them. You'll need to delete the directories on Github manually:

1. On the Github site for your repo, navigate into the folder you want to delete.
2. Click the top right corner button that says  `. . .`
3. Click "delete directory"
4. **Important:** Scroll to the bottom to press the button that commits your changes.