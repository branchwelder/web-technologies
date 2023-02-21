# Using Fetch to get data

In this activity, we will use JavaScript's `fetch` to get data from an API and
render it with a template. You will extend the
[example](https://github.com/branchwelder/example-fetch), which uses data from
the JSON Placeholder API to fetch and render a fake list of users.

## Setup

Clone and download my
[example repo](https://github.com/branchwelder/example-fetch) which we went over
in class. Install the dependencies (`npm install`) and run the dev server
(`npm run dev`) to see the code in action.

## Tweak it

The example uses [JSON Placeholder API's](https://jsonplaceholder.typicode.com/)
`users/` endpoint to get a list of users. Modify the example code to get data
from a different endpoint from the API and update the template accordingly. The
available routes are `posts`, `comments`, `albums`, `photos`, `todos`, and
`users`. _(You can see example data for each of these endpoints by clicking on
them on the front page of the website.)_

## Next Steps

Peruse [this list](https://github.com/public-apis/public-apis) of publicly
available APIs. Select one of them and use fetch to get some data from one of
its endpoints. Following the pattern from the example, render the data to a page
using a `lit-html` template.

## Resources

- [MDN Docs Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [JSON Placeholder Guide](https://jsonplaceholder.typicode.com/guide/)
- [lit-html docs](https://lit.dev/docs/libraries/standalone-templates/)
- [vite docs](https://vitejs.dev/guide/)
- [Digital Ocean Fetch Tutorial](https://www.digitalocean.com/community/tutorials/how-to-use-the-javascript-fetch-api-to-get-data)
- [List of public APIs](https://github.com/public-apis/public-apis)
