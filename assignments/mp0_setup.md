# MP0: Portfolio Setup

For MP0, you will build a skeleton portfolio page and host it on Github pages.

**Initial submission deadline:** Tuesday, 10 January, before class. Submit a
link to your site via the Canvas assignment.

## Submission Requirements

These are the requirements for your skeleton portfolio site. Read them
carefully!

- **_Hosted on Github pages._** I expect to be able to click the URL you submit
  in Canvas and be taken to your portfolio site.
- **_Includes your own custom styles._** Does it have to be pretty? No. Can it
  be simple? Yes. Does it have to be yours? Absolutely. At a minumum:
  - Non-default fonts and colors
  - Some basic positioning (e.g. centering)
- **_Includes (at least) one CSS transition._** The way you implement this is up
  to you, but you should look over the list of CSS properties and explore ones
  that seem interesting to you. For example, you could make your home page title
  change color, grow larger, and jiggle when someone moves their mouse cursor
  over it.
- **_Includes the following sub-pages:_**
  - **_An "about me" page with a short bio and picture._** If you have concerns
    about putting up public information about yourself on the internet, you are
    free to use pseudonymous information (e.g. a cartoon avatar, internet
    handle, fake bio). I just want to give you the option to make this your real
    portfolio site if you wish.
  - **_A bare-bones "cheatsheets" page._** You will be expected to add to this
    page throughout the quarter. This is primarily **for your own reference**,
    but I expect to see it grow over the quarter. You can start by creating a
    "CSS" section and copying in the snippet of CSS you used to make your CSS
    transition.
  - **_The MP0 Writeup._** A page reflecting on your process building this site.
    You should include the following sections:
    - **Overview**: A step-by-step overview of your process, with at least one
      screenshot of an unfinished site
    - **Issue**: Describe an issue you encountered and how you resolved it. For
      example, you might have had trouble pushing your site to Github, or a
      confusing syntax issue with HTML.
    - **CSS Transition**: A description of the CSS transition you implemented,
      why you chose it, and how you made it work, with a gif of it in action
    - **Ideas and Future**: Bullet points describing additional ideas and
      features you might like to add to your site in the future

### Optional additions

- Purchase and connect a custom domain!
- Add additional sub-pages for prior projects you have done!
- Make it look **really** nice! More CSS beyond the basics.
- Make it mobile-friendly!

## Instructions

**IMPORTANT: Before following these instructions, ensure you have finished
[setting up your environment](/activities/01_environment_setup.md).**

We will be using Github pages to host our portfolio sites. Here I provide
instructions to create and clone a repository, stage and commit changes, and
push your work using VSCode's built-in source control interface. If you are
already comfortable using the terminal, Github also provides a
[quick overview](https://pages.github.com/) of how to get up and running.

### Create a new repository from the template

I have created a template portfolio to help you get started. To create a new
repository from the template:

1. Navigate to
   [the repository page on GitHub](https://github.com/branchwelder/portfolio-skeleton),
   click the big green button that says "Use this template", and select "Create
   a new repository".
2. On the repository creation page, name your repository `username.github.io`,
   where username is your GitHub username. **IMPORTANT**: ensure you enter
   `username.github.io` into the box - don't just enter `.github.io`. You can
   leave the rest of the settings as default.
3. Click the "Create repository" button. You should be redirected to your new
   repository.

### Clone it!

If you are comfortable working with git from the command line, feel free to
clone the repository that way (using `git clone repositoryname`).

Alternatively, you can clone your repo from VS Code's built-in source control
interface:

1. In VS Code, hit `Control/Command-Shift-P` to open the command palette. Start
   typing `git:Clone`. The autocomplete option should show up quickly, use the
   arrow keys to navigate to it and hit enter.
2. Select `Clone from GitHub`. Your available repositories should show up; it
   might take a second. You also might need to sign in with your Github
   credentials.
3. In the dropdown menu, select the repository you just created and choose a
   location on your computer to clone it to.
4. VS Code will ask you if you want to open the cloned repository. Select "Open
   in new window". VSCode will open a new window.

### Viewing the example site

Assuming you have installed the VSCode Live Server extension, right click on
`index.html` in the explorer side bar and click "Open with Live Server". The
page should open automatically in your browser. You can now edit the files
containing your site code and your changes will immediately update the browser -
no need to restart the server.

Don't worry about making any changes for now - move on to the next section and
deploy the example site to Github pages.

### Deploy your site by committing and pushing your changes

These are instructions to commit and push your changes using VSCode's built-in
source control interface. You can instead commit and push your work from the
command line if you are comfortable using it. We will cover command line git
usage in future classes.

1. Open the "Source control" panel in VS Code's left sidebar. You should see a
   list of changes you have made. This panel shows information similar to the
   output of the command `git status`.
2. Hover over the header that says "Changes". You should see a Plus icon (+)
   appear to the right. Click it to stage your changes. This is the equivalent
   to running `git add --all` or `git add .` in the terminal.
3. Enter a commit message (e.g. "Testing my portfolio site") in the text entry
   box above (which should say "message"), and click the "Commit" button. This
   is equivalent to running `git commit -m "my commit message"` in the terminal.
4. The "Commit" button should turn into a button that says "sync changes" -
   click it. This is equivalent to running `git push`. This will push your work
   to your remote repository that is stored on Github's servers.
5. Assuming you are successful, you should see the example site online at
   username.github.io in a few minutes!

## Working on your site!!

And now for the moment we've been waiting for! Customize and build your
portfolio site according to the specifications listed above! The example site is
very minimal, but includes enough to get you started. I recommend starting by
reading through the HTML and identifying how each portion of the HTML file
corresponds to what you see in your browser. Regardless of your experience
level, you can now begin editing your site by tweaking the example.

I recommend using the following resources while you customize your site. **These
technologies are complex, and it is normal to feel overwhelmed as you begin to
learn them.** Importantly, do not try to memorize the content of these articles.
The _much more_ important thing is that you learn how to use their insights for
your own purpose, and remember that you can consult them in the future when you
have questions.

As I mentioned in class, the MDN Web docs are a fantastic resource for you as
you learn web technologies. Their
[getting started guide](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)
is a great introduction to these various technologies and how they fit together.
For this assignment, I recommend fully reading the "Getting started" section,
focusing most closely on the following articles:

- [Dealing with files](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/Dealing_with_files) -
  to understand how files are structured
- [HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics) -
  to get an overview of how an HTML document is structured and what tags are
  available to you
- [CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics) -
  to understand how HTML can be styled
- [How the web works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works) -
  to understand the grand scheme

The following sections on HTML and CSS are much longer. Look at the topics
listed in the sidebar and feel free to read any articles that look interesting.
The articles that are probably most useful for this mini project are:

- [HTML: Creating hyperlinks](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)
- [HTML: Images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)
- [HTML: Debugging](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML)
- [CSS: Text and Font Styling](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)
- [CSS: Sizing](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Sizing_items_in_CSS)
- [CSS: Layout](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Introduction)
- [CSS: Debugging](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Debugging_CSS)
- [CSS: Transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions)

## Additional resources

- [HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [CSS selectors overview](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)
- [CSS cheat sheet](https://websitesetup.org/wp-content/uploads/2019/11/wsu-css-cheat-sheet-gdocs.pdf)

## Turning in your assignment

Once you are happy with your portfolio skeleton, deploy your site by committing
and pushing your changes. Like before, this should automatically update your
site on Github Pages. Submit your work via the Canvas assignment. (It will just
ask for the URL to your deployed site.)
