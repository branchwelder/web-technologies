---
title: "JavaScript and the DOM"
author: Hannah Twigg-Smith
---

<!-- # Week 2: JavaScript and the DOM

1/10/23 -->

# Logistics

## Today

- Show-off session (volunteers?)
- Share-back time
- Check-in survey
- Break
- JavaScript intro
- JavaScript activity
- Work time!

## Hair-Tear Shares

- First one is due Jan 17, a week from today

## MP1: Browser extension

For the next two weeks, you will be working on MP1. Instead of me giving you a
bunch of JS to memorize, we are going to do the project the way you might on
your own.

## MP1 steps

1. Think of what you want to make.
2. Figure out how to make it.

## Uncomfortable?

That is OK!

Remember: _you are not graded on your code_.

# Javascript

## What is Javascript?

## Javascript is not Java!

## Brief History

## Why Use Javascript?

Why might we want to use JavaScript?

## Why use JavaScript?

- Store useful values inside variables
- Generate content that can be displayed on your page
- Run code in response to certain events occurring on a web page
- Interact with browser APIS and third-party APIs

## Why use JavaScript?

JavaScript is the _common interface_ that between your personal page, the
browser, and other libraries and frameworks.

# Common Terms

## Interpreted vs compiled

JavaScript is _interpreted_

## Server-side vs Client-side

Client-side code is code that is run on the user's computer

Server-side code is run on the server.

## Server-side vs Client-side

JavaScript can be either client-side or server-side.

## Dynamic vs Static

# Adding JavaScript to your page

## Internal: In a script tag!

```html
<script>
  console.log("Hello world!");
</script>
```

Example: https://codepen.io/branchwelder/pen/abjJNmw

## External: In another file!

`index.html`:

```html
<script src="script.js" defer></script>
```

`index.js`:

```js
console.log("Hello World!");
```

## Loading your script properly

We need to make sure that our JavaScript is loaded in the correct order.

HTML on a page is loaded in the order in which it appears.

If your JavaScript is loaded and parsed before the HTML it is trying to access,
your code won't work!

## `async` and `defer`

# A quick tour of JavaScript

<!-- [https://learnxinyminutes.com/docs/javascript/](https://learnxinyminutes.com/docs/javascript/) -->

<!-- Everyone is coming to this class with different experience levels, but has indicated that they are at familiar with at least one other language, mainly Python and Java. There are many tutorials on the internet that will be more useful to you than me standing up here and lecturing, as you will be able to go through them at your own pace. So, I am going to go through these slides pretty quickly. -->

## Comments

Single line comment:

```js
// I am a comment
```

Multi-line comment:

```js
/*
  I am also
  a comment
*/
```

## Data Types

Seven primitive data types:

- `number` for numbers of any kind: integer or floating-point, integers are
  limited by ±(253-1).
- `bigint` for integer numbers of arbitrary length.
- `string` for strings. A string may have zero or more characters, there’s no
  separate single-character type.
- `boolean` for true/false.
- `null` for unknown values – a standalone type that has a single value null.
- `undefined` for unassigned values – a standalone type that has a single value
  undefined.
- `symbol` for unique identifiers.

And one non-primitive data type:

- `object` for more complex data structures.

## Strings

```js
let str = "Hello";
let str2 = "Single quotes are ok too";
let phrase = `can embed another ${str}`;
```

## Booleans

```js
let nameFieldChecked = true; // yes, name field is checked
let ageFieldChecked = false; // no, age field is not checked
```

## Booleans

```js
let isGreater = 4 > 1;

alert(isGreater); // true (the comparison result is "yes")
```

## `null`

A special value which represents “nothing”, “empty” or “value unknown”.

```js
let age = null;
```

## `undefined`

```js
let age;

alert(age); // shows "undefined"
```

## Arrays

An _ordered_ collection of elements,

```js
const a = [];
const a = Array();
```

## Arrays

```js
const a = [1, 2, 3];
const a = Array.of(1, 2, 3);
```

## Arrays

Arrays can hold any value, even values of different types:

```js
const a = [1, "Flavio", ["a", "b"]];
```

## Arrays

This means we can create _multi-dimensional_ arrays:

```js
const matrix = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9],
];

matrix[0][0]; // 1
matrix[2][0]; // 7
```

# Variables

## Two ways of defining variables

`let` - when it will change in the future

`const` - when it will not change

## `let` versus `const`

<!-- ```js
let happy = true;
``` -->

_Use `const` when you can, and use `let` when you have to._

## you will also see `var`

As you look around the internet, you will also see `var` used to declare
variables.

TL;DR: `var` can be confusing, for a number of reasons. At this point, you don't
need to understand the technical reasons for this.

If you see `var` used somewhere, change it to `let`.

Read more
[here](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Variables#a_note_about_var)

<!-- ## Building your sites from JavaScript

### Why?

You may have noticed that building HTML files manual is tedious!

## Manipulating the DOM

## JSON

### What is JSON?

JSON === JavaScript Object Notation

### What is JSON?

- _A lightweight data interchange format._

### What is JSON?

- _A lightweight data interchange format._
- Based on a subset of JavaScript
- _Human readable_: Easy to read and write
- Typically used to store and send information between a client and a server
- Can be used with almost all modern programming languages

### Remembering the JSON-valid data types

**BASONN**

- Booleans
- Arrays
- Strings
- Objects
- Numbers
- Null

BASONN, rhymes with JSON. -->
