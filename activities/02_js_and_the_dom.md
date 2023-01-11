# Introducing JavaScript

As usual, consult the class
[resource page on JavaScript](/resources/javascript.md) and post any helpful
overviews, tutorials, or videos you find in the Discord.

## Start here

Start with MDN docs
[Intro to JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript).

These articles in particular might be helpful for you:

- [Conditionals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals)
- [Loops](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code)
- [Functions](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions)

Read
[Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction).

## Activity

The slides included a number of codepens that provide simple examples of DOM
interactions:

- [Creating and adding elements](https://codepen.io/branchwelder/pen/oNMZbrG)
- [Adding different kinds of event listeners](https://codepen.io/branchwelder/pen/abjJNmw)
- [Querying the DOM and randomizing colors](https://codepen.io/branchwelder/pen/vYayyOP)

Start by playing around with them and modifying the code.

Once you have a handle on what's going on, test your understanding by adding
some JavaScript to your portfolio page. Begin by creating an `index.js` file in
your top-level directory and importing it into your `index.html` page using a
script tag. **Important:** Ensure that you put this inside your body tag **after
any content** `<body>` tag, after any content:

In `index.html`:

```html
<html>
  <body>
    <!-- The rest of your page content here -->
    <script src="index.js" defer></script>
  </body>
</html>
```

In `index.js`:

```js
console.log("Welcome to my portfolio page!");
```

Now, when you serve your `index.html` page with live server, your browser
console should show `"Welcome to my portfolio page!"`.

Here are some ideas for what you could do:

- Add a button that changes your site between light mode and dark mode
- Add
  [an image gallery ](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Image_gallery)
- Programmatically create your page content instead of building the HTML by hand
- Add links to your social media pages by creating an array of objects that
  contain the URL, service name, and other information (e.g. a link to a logo to
  display). Then, iterate through the array and append each one to your page.
- Collaborate with other students in the class to create a
  [webring](https://en.wikipedia.org/wiki/Webring)

## Resources that might be helpful

- [Introduction to events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)
  [JavaScript Fundamentals](https://javascript.info/first-steps) chapter
