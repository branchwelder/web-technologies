# More on loops and functions

## Arrow Functions

```js
let hypot = (x, y) => {
  return Math.sqrt(x ** 2 + y ** 2);
};
```

## Iteration: classic

```js
// Low-level, more verbose
for (let i = 0; i < mondayLectures.length; i++) {
  const lecture = mondayLectures[i];
  lecture.textContent = "I hate Mondays 😫";
}
```

## Iteration: for...in

```js
// Iterate over object properties
for (const i in mondayLectures) {
  const lecture = mondayLectures[i];
  lecture.textContent = "I hate Mondays 😫";
}
```

## Iteration: for...of

```js
// Iterate over items
for (const lecture of mondayLectures) {
  lecture.textContent = "I hate Mondays 😫";
}
```

# More JavaScript

## Patterns

`map`, `reduce`, and `filter` are common patterns for transforming a collection
of items en masse

- `map`: transform items 👨 👨 👧 ➡ 👨🏼 👨🏼 👧🏼
- `filter`: choose some of the items 👨 👨 👧 ➡ 👨 👧
- `reduce`: combine items 👨 👨 👧 ➡ 👨‍👨‍👧

## Scoping

```js
if (true) {
  let x = 1;
}

console.log(x);
```

. . .

What do you think will happen?

## Scoping

`let` and `const` are block-scoped

. . .

In other words, they are only visible within the curly braces `{}` they are
declared in.

## Scoping

```js
if (true) {
  let x = 1;
  log();
}

function log() {
  console.log(x);
}
```

. . .

What do you think will happen?

## Scoping

JavaScript uses _lexical scope_

. . .

Scope is determined by syntax, not execution

## You will also see var

```js
// var has different scoping behavior, which can be confusing

var index = 5;

// It is better to use let, but older snippets of code will use var
```

Read more
[here](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Variables#a_note_about_var)
