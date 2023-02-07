# Dev Toolchain Walkthrough

In this in-class activity, we will set up a development environment. You should
follow along with these instructions. After you follow these steps, your
repository should look like
[my example](https://github.com/branchwelder/dev-toolchain-example).

## Setup

1. Create a new Github repository and clone it to your computer. Open it in
   VSCode.
2. In the VSCode terminal, ensure you are in the correct directory and run
   `npm init`. This will initialize an NPM project and create a `package.json`
   file. It will walk you through a few prompts in your terminal. You can accept
   the defaults for all of them.

## Installing and using a library

Now, let's install three.js.

1. Install three.js by running `npm install three`. If you look at your
   `package.json`, you will now see `three` listed as a dependency. You will
   also see a new folder show up in your repository: `node_modules`. This is
   where packages installed with NPM live!
2. Create an `index.html` file. Copy the following code into it::

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Cubin' along</title>
    <style>
      body {
        margin: 0;
        overflow: hidden;
      }
    </style>
  </head>
  <body>
    <script src="index.js" type="module" defer></script>
  </body>
</html>
```

3. Create an `index.js` file. Copy over some code that uses `three.js`. This
   comes from their
   [documentation intro](https://threejs.org/manual/#en/fundamentals).

```js
import {
  BoxGeometry,
  Mesh,
  MeshPhongMaterial,
  PerspectiveCamera,
  Scene,
  WebGLRenderer,
  DirectionalLight,
} from "three";

// Create our scene
const scene = new Scene();

// Create the camera so we can see our scene
const camera = new PerspectiveCamera(
  75,
  window.innerWidth / window.innerHeight,
  0.1,
  1000
);

// Create our renderer and add it to the DOM
const renderer = new WebGLRenderer();
renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);

// Create our cube mesh from  a geometry and a material and add it to the scene
const geometry = new BoxGeometry(1, 1, 1);
const material = new MeshPhongMaterial({ color: 0x00ff00 });
const cube = new Mesh(geometry, material);
scene.add(cube);

// Add a directional light so we can see shadows on the cube
const color = 0xffffff;
const intensity = 1;
const light = new DirectionalLight(color, intensity);
light.position.set(-1, 2, 4);
scene.add(light);

// Position the camera
camera.position.z = 5;

// The animation loop updates the cube's rotation
function animate() {
  requestAnimationFrame(animate);
  cube.rotation.x += 0.01;
  cube.rotation.y += 0.01;
  renderer.render(scene, camera);
}

// Start the animation loop
animate();
```

## Local Development with Web Dev Server

We have some starter code, and now we need to run the app. However, we can't use
live server like we've been doing so far. This is because our `index.js` file is
trying to import a library using its name, `three`, but the library files are
stored in `/node_modules`. We need a server that knows how to connect the
imports in `index.js` to the libraries in `node_modules`.

1. Install `web-dev-server`. We will use this instead of live server to serve
   our code: `npm install --save-dev @web/dev-server`
2. Add a script to your `package.json` that we can use to run the dev server.
   Inside the `scripts` section, copy in
   `"start": "web-dev-server --node-resolve --open --watch"`. This means that we
   will be able to run the dev server using `npm run start`
3. Run your app locally: `npm run start`. You should see the rotating cube show
   up!

## Bundling with Rollup

Now, we're going to use Rollup to build our code. It will bundle everything
together nicely.

1. Install Rollup: `npm install rollup --save-dev`.
2. Install the node-resolve plugin:
   `npm install @rollup/plugin-node-resolve --save-dev`, which will bundle
   things we have put in our `node_modules` folder (in this case, three.js).
3. Install the copy plugin: `npm install rollup-plugin-copy --save-dev`. This
   plugin will allow us to copy over certain files to our build folder.
4. Create a configuration file for Rollup called `rollup.config.js`:

   ```js
   import { nodeResolve } from "@rollup/plugin-node-resolve";
   import copy from "rollup-plugin-copy";

   module.exports = {
     input: "index.js",
     output: {
       dir: "dist",
     },
     plugins: [
       copy({
         targets: [{ src: "index.html", dest: "dist" }],
       }),
       nodeResolve(),
     ],
   };
   ```

   This config says to bundle the `index.js file` and output it in a folder
   called `dist`. It also uses the copy plugin to copy over our `index.html`
   file, also putting it in `dist`. It also uses the `node-resolve` plugin to
   include any dependencies in our `node_modules` folder.

5. Add a build script to your `package.json`. Inside the `scripts` field, next
   to your `start` script, add `"build": "rollup --config"`. This will run
   rollup using the config file we just made.
6. Now, you can run the build script you just added by running `npm run build`.
   Do it now. You will see that there is a new folder created called `dist/`,
   which contains two files: `index.html` and `index.js`. However, the
   `index.js` has a lot more code than was in your original `index.js`! All of
   the things that `index.js` depends on, (namely, Three.js), have been
   _bundled_ into one file. This folder now contains the built version of your
   site.

## Deploying to Github Pages

Previously, we have just been able to push our changes in order to update our
Github pages site. That works when all of the code our site needs is included in
our repository. However, now that we have additional dependencies, we need to
figure out how to push the code from the dependencies as well. We can still use
Github pages, though! But we're going to make a few tweaks to our toolchain.

1. Install the `gh-pages` package: `npm install gh-pages --save-dev`
2. Add a `deploy` script to your `package.json`, under the `scripts` section:
   `"deploy": "npm run build && gh-pages -d dist"`
3. Run the deploy script: `npm run deploy`

This will first build your site using the `build` script we made above.
Remember, the `build` script puts the built version of your site in a folder
called `dist/`. Then, our `deploy` script will use the `gh-pages` library to
push everything in your `dist/` folder to a special branch called `gh-pages`.
Github will automatically use this branch as the pages branch and serve your
site files from it.

## View your site

Your site should soon be live! You might have to wait a few minutes for Github's
deployment checks to pass. You will be able to view it at
`<username.github.io>/<repositoryname>`. For me, this looks like
`branchwelder.github.io/dev-toolchain-example/`.

## Pushing your changes to Github

OK - we've deployed our site to the gh-pages branch! However, we have not yet
pushed our changes to our main branch Github. But wait! There is a **VERY
IMPORTANT** thing we have to do first. We need to tell git to **ignore** certain
files. Specifically, we do not want to push the contents of our `node_modules`
folder or our `dist` folder to our main branch. We're recording what
dependencies to install in our `package.json`, so there's no point in pushing
another copy of that code to Github.

1. Create a file named `.gitignore`. This is the file that tells git what things
   it should ignore
2. Inside `.gitignore`, add two lines:

   ```
   node_modules/
   dist/
   ```

3. Now, track your changes with git: `git add --all`. You should **NOT** see
   your `node_modules` or `dist` folders in the list of changed files. If you
   do, you should double check that you made your `.gitignore` correctly.
4. Commit them: `git commit -m "deployed my site"`
5. And push: `git push`

Now, you should see all of your changes in your main branch!
