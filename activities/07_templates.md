# Tagged Templates with `lit-html`

**Explore the nav bar example.** Clone and download the
[example repo](https://github.com/branchwelder/example-nav-template) which uses
`lit-html` to make a nav bar template that is used across multiple pages.

**Render part of your portfolio with a lit-html template.** A reusable nav bar
such as the one demonstrated in the example is probably a good place for most
students to start.

- Besides a nav bar, are other parts of your page that might be suitable for
  reusable templates?
- What parts of your markup have you found yourself often copying and pasting?

**Explore installing the lit-html package with npm and bundling your site.**

Install with npm:

```sh
npm install lit-html
```

Importing `html` and `render` where you want to use them:

```js
import { html, render } from "lit-html";
```

- What would need to change in `rollup.config.js` from the previous activity in
  order to also bundle the `lit-html` source?
- What are the benefits to installing packages locally vs. importing them from a
  CDN? What are the drawbacks?

## Resources

- [MDN docs on template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals#Tagged_template_literals)
- [lit-html docs](https://lit.dev/docs/libraries/standalone-templates/)
