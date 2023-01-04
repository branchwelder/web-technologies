# MP0 - Portfolio page

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

We will be using Github pages to host our portfolio sites. Here I provide
instructions to create and clone a repository, stage and commit changes, and
push your work using VSCode's built-in source control interface. If you are
already comfortable using the terminal, Github also provides a
[quick overview](https://pages.github.com/) of how to get up and running.

### Create a repository

1. Head over to the GitHub website and create a new repository. Do this by
   clicking the "plus" and selecting "New Repository".
2. On the repository creation page, name your repository `username.github.io`,
   where username is your GitHub username. You can leave all of the settings as
   default. **Ensure that your repository is set to Public**
3. Click the "Create repository" button. You should be redirected to your new
   empty repository.

### Clone it!

If you are comfortable working with git from the command line, feel free to
clone the repository that way (using `git clone repositoryname`).

To instead do this from VSCode:

1. Hit `Control/Command-Shift-P` to open the command palette. Start typing
   Git:Clone. The autocomplete option should show up quickly, use the arrow keys
   to navigate to it and hit enter.
2. Select `Clone from GitHub`. Your available repositories should show up; it
   might take a second. You also might need to sign in with your Github
   credentials.
3. In the dropdown menu, select the repository you just created and choose a
   location on your computer to clone it to.
4. VSCode will ask you if you want to open the cloned repository. Select "Open
   in new window". VSCode will open a new window. The "Explorer" tab in the
   sidebar will be empty because we have not added any files to it yet.

### Copy over the example site

Copy the contents of the example site in this folder into your repository. You
can do this by manually creating each file and directory (e.g. `index.html`) and
copying and pasting in the example content. If this is too tedious, you can also
download a zip file of the course repository by
[navigating to the root directory](https://github.com/branchwelder/web-technologies),
clicking the big green "Code" button, and selecting "Download ZIP". You can then
drag the files into your repository folder.

Once you have finished copying over the example, your folder structure should
look like this:

- `index.html` - your site's home (index) page
- `index.css` - contains the styles for home page
- `bio/` - folder containing the bio page
  - `bio.html` - html for the bio page
  - `bio.css` - styles for the bio page
- `recipe/` - folder containing files for the recipe page
  - `recipe.html` - html for the recipe page
  - `recipe.css` - styles for the recipe page

### Viewing the example site

To Assuming you have installed the VSCode Live Server extension, right click on
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

And now for the momemt we've been waiting for! Customize and build your
portfolio site according to the instructions listed above! The example site is
very minimal, but includes enough to get you started. I recommend starting by
reading through the HTML and identifying how each portion of the HTML file
corresponds to what you see in your browser. Then, you can incrementally change
files and customize the content.

The MDN Web docs are a fantastic resource for you as you learn web technologies.
Their
[getting started guide](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)
is a great introduction to these various technologies and how they fit together.
For this assignment, I recommend reading the getting started, HTML, and CSS
sections (up until the JavaScript section). In particular, I recommend reading
the following articles from the _Getting Started_ section:

- [Dealing with files](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/Dealing_with_files) -
  to understand how files are structured
- [HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics) -
  to get an overview of how an HTML document is structured and what different
  tags mean
- [CSS Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics) -
  to understand how HTML can be styled
- [How the web works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works) -
  to understand the grand scheme

## Additional resources

- [Debugging HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML)
- [HTML elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [CSS cheat sheet](https://websitesetup.org/wp-content/uploads/2019/11/wsu-css-cheat-sheet-gdocs.pdf)

## Turning in your assignment

Once you are happy with your portfolio skeleton, deploy your site by committing
and pushing your changes. Like before, this should automatically update your
site on Github Pages. Submit your work via the Canvas assignment. (It will just
ask for the URL to your site.)
