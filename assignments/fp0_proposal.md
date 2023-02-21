# Final Project Proposal

In this assignment, you will propose a final project for the class. This is the
first of three assignments which comprise the final project: the proposal, the
prototype, and the final version. The proposal is due on **Tuesday, Feb 28.**

After the proposal, you will create a **functional** prototype of your project
in the first week. It is expected that this will be a minimal version of your
final project. This is to encourage you to scope your development work
appropriately. For the prototype, you should tackle unknowns (such as learning
how to use a new library) before working on things you already know how to do
(such as styling an app with CSS). You will then demo your prototype in class on
**Thursday, March 9**, which is also the last day of class. Your final
submission is due on **Friday, March 17**, which is the last day of the quarter.

## Roadmap

- **2/28:** Proposal due.
  - FP0 writeup posted to portfolio
  - You are **REQUIRED** to check in with me about your project idea
- **3/7:** Prototype due.
  - FP1 writeup posted to portfolio
- **3/9:** Last class, demo day!
  - You are **REQUIRED** to demo your prototype in class.
- **3/17:** Final version due, and final portfolio due.
  - FP2 writeup posted to portfolio

## Project Options

There are few restrictions on what you could do for your final project. I want
to give you space to explore your own interests. That said, here are a few
ideas:

- Revisit one of the mini projects and create a more advanced version. For
  example, now that we have learned about bundling code with Rollup, you could
  build a Chrome extension that relies on a library such as D3.
- Create an app that uses one of Chrome's browser APIs we haven't covered:
  - The [Web Serial API](https://developer.chrome.com/en/articles/serial/) can
    be used to talk to USB devices (Might be cool if you're learning about
    sensors in 439!)
- Using `fetch` and a charting library (e.g. `d3`) to create a queryable data
  dashboard showing data from an API, such as one from
  [this list](https://github.com/public-apis/public-apis)
- Use P5 to create a paint-like drawing app, which lets the user download their
  art!
- Build another game, however, this time use
  [Firebase](https://firebase.google.com/) to implement a user login flow and
  backend database that stores high scores. _I have an in-class activity on
  Firebase planned for 2/23._
- Use [React](https://reactjs.org/)
- Do any of the above, but explore developing for different platforms:
  - [React Native](https://reactnative.dev/) can be used to create a mobile app
  - [Electron](https://www.electronjs.org/) can be used to create a desktop app
  - P5 also has a number of methods that can be used on mobile to detect things
    like screen orientation and acceleration.

## Technical Project Requirements

These requirements are for _both_ the prototype and final version.

- Must be in its own git repository
- The repository must have two releases on Github: the prototype version and the
  final version (this is so we can easily see both version)
- As usual, it must be deployed and publicly accessible
- Must use a dev toolchain that you set up yourself, including:
  - A local development server (e.g. web-dev-server or vite)
  - A build tool (e.g. rollup, webpack, or vite)
  - A deployment tool (e.g. gh-pages)
- **ALL PROJECTS MUST BE APPROVED BY HANNAH**. I will check in with you in-class
  on 2/28.

## Proposal Submission Requirements

For the project proposal, you will create a sub-page on your portfolio website
that includes the following information:

- A one-sentence description of your project
- At least two drawing of your envisioned interface
- Descriptions of two versions of your project:
  - **Prototype version** - A minimal version that demonstrates the core
    features of your app. This should be _functional_, but it does not have to
    be _robust_ or _beautiful_. For example, some parts might be hardcoded
    instead of accepting user input, and you might have minimal CSS styling.
  - **Final Version** - Your envisioned final submission.
- A numbered, step-by-step plan for your development process, with two
  milestones (the prototype version and final version)
- A list of known unknowns (things you don't currently know how to do, but know
  you will have to figure out)
- A list of stretch goals.

Submit a link to this page in Canvas. In addition to submitting the proposal,
you are **required** to check in with me **in-class** on 2/28 so I can approve
your project. If you will be absent from class, you must check in with me via
Discord or email by the end of the day on 2/28.
