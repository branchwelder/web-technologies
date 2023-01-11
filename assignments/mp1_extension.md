# MP1: A Browser Extension

You've played around with HTML and CSS, and we've written a little bit of
JavaScript. Now it's time to apply what you've learned to build your first tool:
a browser extension. This assignment is intended to help you get familiar with
JavaScript and how you can use it to interact with the DOM.

## Background Reading

Start working on your project following the instructions below, and work through
these resources at your own pace. You should consult these as you have
questions - don't try to memorize the content right away.

Learn a bit about JavaScript:

- Work through the MDN Docs learning area's
  [JavaScript articles](https://developer.mozilla.org/en-US/docs/Learn/JavaScript)
- If you would like a more structured tutorial, I recommend javascript.info's
  [fundamentals chapter](https://javascript.info/first-steps)

Learn about how you can use JavaScript to manipulate the DOM:

- Read javascript.info's [chapter on the DOM](https://javascript.info/document)
- Read
  [this article](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents)
  on manipulating the DOM.
- The MDN docs
  [introduction to events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)

Learn about developing a browser extension from Chrome's documentation:

- [Chrome Extensions 101](https://developer.chrome.com/docs/extensions/mv3/getstarted/extensions-101/)
- [Chrome Extensions development basics](https://developer.chrome.com/docs/extensions/mv3/getstarted/development-basics/)
- [Extension development overview](https://developer.chrome.com/docs/extensions/mv3/devguide/)

## Instructions

To get started, **clone my
[extension toolkit repository](https://github.com/branchwelder/extension-toolkit)**.
This repository contains a number of examples that I created to demonstrate some
of the core features an extension might contain.

**Load the example extensions** in your browser (instructions on loading an
unpacked extension
[here](https://developer.chrome.com/docs/extensions/mv3/getstarted/development-basics/#load-unpacked)).
Start with the `hello_world` example. Once you have them running, play around
with them.

- Understand how the different components talk to each other
- Ensure you can
  [debug your extension](https://developer.chrome.com/docs/extensions/mv3/tut_debugging/)
  by opening the developer console to see any errors

**Make a plan.** We will brainstorm ideas for your extensions in class. To get
ideas, browse the
[list of example Chrome extensions](https://github.com/GoogleChrome/chrome-extensions-samples).
You can also watch the video tutorials linked below for a step-by-step
introduction.

Once you have explored the examples, **create a new repository** on your github
account, name it something like `bookmarker-extension`, and clone it locally.
You can your development by copying over one of the example extensions if you
would like, or from scratch.

**Build your extension.** Don't try to build your project all at once. Start
small: it is better to have a simple project that is functional than a large
project that is broken. For example, if you are building a bookmark extension:

1. Manually write the HTML file that you would like to show in your popup.
2. Write JavaScript that builds the popup HTML programatically from a list of
   urls.
3. Write JavaScript for loading the list of urls from browser storage.
4. Add a text input field to your HTML that can capture and save user input.

Remember to **ask questions**. You are _not_ expected to know how to implement
everything on your own, or right away. Instead, think of something you might
want to make **and then** figure out how to make it. If you have an idea for
your project but you're not sure how to accomplish it, talk to your peers or the
instructors. Post questions on Discord.

## Video Tutorials

- [Create a Google Chrome Extension (For Beginners)](https://www.youtube.com/watch?v=uV4L-wcnK3Y) -
  10 minute video tutorial showing how to make an extension to customize the
  background of your Google page
- [A YouTube Bookmarker Extension](https://www.youtube.com/watch?v=0n809nd4Zu4) -
  one hour video tutorial

## What to turn in

In Canvas, turn in a link to your project writeup. The writeup should be hosted
on your portfolio page, and accessible from your portfolio home page.
Instructions for project writeups are [here](/assignments/writeups.md). **The
writeup asks for an in-progress screenshot of your work.** Keep this in mind as
you work on your project.

## Going Further

- **Publish your extension:** I _strongly_ encourage you to publish your
  extension to the Chrome Web Store following
  [their documentation](https://developer.chrome.com/docs/webstore/publish/).
  This is not required, as you will need to pay a $5 one-time fee to register as
  a developer.
- **Support additional browsers:** You can explore supporting additional
  browsers (e.g. Safari and Firefox). MDN has instructions on how to do this
  [here](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/Build_a_cross_browser_extension).
- **Make an icon for your extension:** You can design one yourself, or use a
  site such as [favicon.io](https://favicon.io/)

## Resources

- Lists
  - [List of example Chrome extensions](https://github.com/GoogleChrome/chrome-extensions-samples) -
    from the Chrome documentation
  - [List of Chrome APIs](https://developer.chrome.com/docs/extensions/reference/) -
    APIs you can use to interact with the browser
- Useful Chrome extension documentation pages
  - [Message passing](https://developer.chrome.com/docs/extensions/mv3/messaging/) -
    how to make your popup communicate with your content scripts
  - [Options pages](https://developer.chrome.com/docs/extensions/mv3/options/) -
    Adding and customizing an options page
  - [Referencing extension files](https://developer.chrome.com/docs/extensions/mv3/architecture-overview/#files) -
    How to include additional files in your extension, such as fonts or images
  - [Debugging](https://developer.chrome.com/docs/extensions/mv3/tut_debugging/) -
    how to debug your extension, open the console, etc
