# Firebase

This is a tutorial for setting up Firebase and connecting a Firestore database
to your app. I've linked to their official doc pages when relevant. We are using
the most recent "Web version 9" version of Firebase - make sure you select "Web
version 9" if looking at their examples.

Once you've followed all of the instructions here, your repo should look like
[my example](https://github.com/branchwelder/example-db).

## Set up your project

Create a new repository and clone it to your computer. Inside, set up a basic
webapp structure:

Inside `index.html`:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>my cool app</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <script src="index.js" type="module"></script>
  </body>
</html>
```

Inside `styles.css`:

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
}
```

Inside `.gitignore`:

```
node_modules/
dist/
```

Also, create `index.js`. We'll add to it later.

## Set up the dev environment

Run `npm install vite --save-dev`. This will create a `package.json` without any
extra cruft. Inside the `package.json`, add the following scripts that will run
your vite dev server and build tool:

```json
"scripts": {
  "start": "vite",
  "host": "vite --host",
  "build": "vite build",
  "preview": "vite preview"
}
```

## Create a Firebase Project and register your app

_See the [detailed docs](https://firebase.google.com/docs/web/setup) for more
information about this section._

Before you can add Firebase to your JavaScript app, you need to create a
Firebase project and register your app with that project. When you register your
app with Firebase, you'll get a Firebase configuration object that you'll use to
connect your app with your Firebase project resources.

1. **Create a Firebase project.** Go to the
   [Firebase console](https://console.firebase.google.com/), click **Add
   project**, then follow the on-screen instructions to create a Firebase
   project. You don't need to add Google Analytics for a small test project.
2. On your project page, under where it says "Get started by adding Firebase to
   your app", click the web button (with the `</>` icon)
3. Follow the onscreen instructions to add the Firebase SDK using NPM:
   - Enter a nickname for your app and click "Register App"
   - run `npm install firebase` to install firebase to your project
   - copy the code they give you with the firebase config into your `index.js`
     file.
   - Click **Continue to console**

Your `index.js` should now look like this:

```js
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
const firebaseConfig = {
  // YOUR CONFIG WILL BE HERE
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
```

## Add Cloud Firestore

_See the
[detailed docs](https://firebase.google.com/docs/firestore/quickstart#web-version-9)
for more information about this section._

1. Click on **Cloud Firestore** in your
   [Firebase console](https://console.firebase.google.com/).
2. Click **Create database** and choose **Start in test mode**, and click Next.
   On the next screen, select the location for your database (You can probably
   just confirm the default). Click **Done**.

At the top of `index.js`, below the line that imports `initializeApp`, add a
line to import Cloud Firestore:

```js
import { getFirestore, collection, addDoc } from "firebase/firestore";
```

You'll also need to add a line to initialize the Firestore database:

```js
const db = getFirestore(app);
```

After you add those two lines, your `index.js` should look like this:

```js
import { initializeApp } from "firebase/app";
import { getFirestore, collection, addDoc } from "firebase/firestore";

const firebaseConfig = {
  // YOUR CONFIG WILL BE HERE
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);

// Initialize Cloud Firestore and get a reference to the service
const db = getFirestore(app);
```

## Add some data to the Firestore

Below the code from the previous step, add:

```js
try {
  const docRef = await addDoc(collection(db, "users"), {
    first: "Ada",
    last: "Lovelace",
    born: 1815,
  });
  console.log("Document written with ID: ", docRef.id);
} catch (e) {
  console.error("Error adding document: ", e);
}
```

If you run your development server and open your page locally, you should see a
message output to the console that says
`Document written with ID: 5W0h66qcCQi2wNiNJUuD`. (Nothing will show up on the
page because we haven't added anything to look at yet.)

To confirm that the document was added, go back to the Firebase console for your
app and click on "Firestore Database" in the sidebar under "Project Shortcuts".

It will open to the "Data" tab. You should see a "users" collection and a
document inside with the data you just added! Every time you refresh your app,
it will add a new entry, because right now we're just adding the same data over
and over again when `index.js` runs.

**Your turn:** Modify the `addDoc` function to instead add a document to a
collection called "players", which adds an object containing a player name and a
high score. _Just hard-code it for now._

## Create a simple view

Let's install `lit-html` in order to render a view for our project:
`npm install lit-html`.

At the top of `index.js`, add:

```js
import { html, render } from "lit-html";
```

Below the rest of the code, add:

```js
function handleInput(e) {
  console.log(e.target.value);
}

function view() {
  return html`<h1>my cool app</h1>
    <input type="text" @keydown=${handleInput} />`;
}

render(view(), document.body);
```

`@keydown=${handleInput}` is shortcut for adding an event listener when using a
lit-html template. What this line is saying is, "on keydown, run the handleInput
function". The `handleInput` function above just logs the current value of the
input target.

Run the dev server with `npm run start`. When you type into the input box, you
should see the log messages in the console.

## Send messages to database from user input

**Delete** or comment out the code we added earlier that adds some data to
firestore. In its place, add a function we can call to send a message that will
be recorded in our firestore database.

```js
async function sendMessage(message) {
  console.log("Sending a message!");
  // Add some data to the messages collection
  try {
    const docRef = await addDoc(collection(db, "messages"), {
      time: Date.now(),
      content: message,
    });
    console.log("Document written with ID: ", docRef.id);
  } catch (e) {
    console.error("Error adding document: ", e);
  }
}
```

Modify the `handleInput` function from the previous step to call the
`sendMessage` function if the enter key is pressed:

```js
function handleInput(e) {
  if (e.key == "Enter") {
    sendMessage(e.target.value);
    e.target.value = "";
  }
}
```

If you navigate back to your Firestore, you should see a new collection called
"messages" that contains any message send using your input!

## Render all the messages in the database

Modify the line that imports tools from firestore so that it also imports
`query`, `getDocs`, `orderBy`, and `onSnapshot`:

```js
import {
  getFirestore,
  collection,
  addDoc,
  getDocs,
  onSnapshot,
  query,
  orderBy,
} from "firebase/firestore";
```

Initialize a messages array and create a reference to the messages database. Add
these after the line that initializes the database
`const db = getFirestore(app);`, near the top of the file:

```js
let messages = [];
const messagesRef = collection(db, "messages");
```

Make a function to get all messages:

```js
async function getAllMessages() {
  messages = [];

  const querySnapshot = await getDocs(
    query(messagesRef, orderBy("time", "desc"))
  );
  querySnapshot.forEach((doc) => {
    let msgData = doc.data();
    messages.push(msgData);
  });

  console.log(messages);
  render(view(), document.body);
}

getAllMessages();
```

This function resets the messages array to be empty. Then, it queries the
database to get everything in the messages collection. For each document in the
messages collection, it gets the data out of it using `.data()` and adds it to
the messages array. Then, it re-renders our `view` function to the document
body.

One more step: update the view function to actually show the messages:

```js
function view() {
  return html`<h1>my cool app</h1>
    <input type="text" @keydown=${handleInput} />
    <div id="messages-container">
      ${messages.map((msg) => html`<div class="message">${msg.content}</div>`)}
    </div>`;
}
```

### Monitor for changes

This function watches the "messages" collection for any changes. If there are
any changes, it reruns our `getAllMessages` function, which in turn updates the
view.

```js
onSnapshot(
  collection(db, "messages"),
  (snapshot) => {
    console.log("snap", snapshot);
    getAllMessages();
  },
  (error) => {
    console.error(error);
  }
);
```

## Going beyond

You can use Firebase to build a multiplayer game! See
[this video](https://youtu.be/xhURh2RDzzg) for a tutorial.

## Resources

- [Building a multiplayer game with JavaScript](https://youtu.be/xhURh2RDzzg)
- [Firebase Web Setup](https://firebase.google.com/docs/web/setup?sdk_version=v9)
- [Firebase App Samples](https://firebase.google.com/docs/samples)
- [Firestore Quick Start](https://firebase.google.com/docs/firestore/quickstart#web-version-9)
