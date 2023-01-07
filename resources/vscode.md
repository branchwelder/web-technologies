# VS Code Resources

Visual Studio Code (typically shortened to VS Code) is a lightweight but
powerful source code editor[^docs]. It is overwhelmingly the most popular
development environment, preferred by 75% of professionals and 81% of learners
according to the 2022 Stack Overflow survey[^devsurvey22].

## Start Here

The [VS Code docs](https://code.visualstudio.com/docs) are an excellent resource
and I find them easy to navigate. However, they can be a bit overwhelming due to
the amount of information they contain. As usual, **do not set out to memorize
the content of the documentation**. It exists so that you can consult it when
you have questions. As you use VS Code more, you will naturally pick up things
like keyboard shortcuts. Here are a few articles that will get you started:

- [Setting up](https://code.visualstudio.com/docs/setup/setup-overview)
- [Getting Started (video)](https://code.visualstudio.com/docs/introvideos/basics)
- [Basic Editing](https://code.visualstudio.com/docs/editor/codebasics)

## Useful Reference

- [Keyboard shortcuts reference](https://code.visualstudio.com/docs/getstarted/keybindings#_keyboard-shortcuts-reference)

## Common Issues

These are some issues I've noticed new VS Code users frequently run into.

### Opening the entire filesystem in the explorer

This causes _so_ many strange problems, and it also adds a bunch of visual noise
to your explorer window. I recommend only opening the highest level folder you
need access to. Often, this is just the git repository folder. You can add
additional folders to the workspace by using `File | Add Folder to Workspace`.
If there is a set of folders you typically like to have available in the
explorer pane at the same time, you can save a workspace configuration using
`File | Save Workspace to File` in order to reopen it later.

### Not saving files

Auto save is not turned on by default. If you don't save your file your most
recent work will not be reflected when you run your code. This might seem
obvious, but it's a surprisingly common issue for people who are used to default
autosave (e.g. in Google Docs.) Manually save files with the `CTRL/CMD-s`
shortcut, or turn on autosave (what I do). This is located in Settings pane
(open with `CTRL/CMD-comma`) under `Text Editor > Files`. I typically set it to
`onFocusChange`.

### Installing too many extensions

## Extensions

There are endless possibilities for customizing VS Code. Here are some of the
extensions I have installed! As a general rule, it's good to understand what an
extension does before you install it. They all have _some_ documentation in the
extension marketplace, which you should read before installation. If an
extension is causing issues, you can disable it or uninstall it. It's also good
to uninstall any extensions you're not using, otherwise they will continue to
run in the background.

### Web Development Essentials

- [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) -
  _Local development server inside VSCode_
- [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
- Prettier: _Code formatting for a bunch of web-related languages_
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) -
  _A linter for javascript_

### Nice-to-have

- [Gitlens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- Code Spell Checker: _A spell checker that also works for camelCase_
- Path Intellisense - _Autocompletes filenames (useful for importing things)_
- Path Autocomplete - _autocompletes paths (also useful for importing things)_
- IntelliSense for CSS class names in HTML: _adds autocompletion for your css
  class names_
- Markdown All In One: _keyboard shortcuts, auto preview, formatting, etc. for
  markdown_
- npm: _npm support (we will cover npm later)_
- npm intellisense: _adds autocompletion for npm modules_
- search node modules: _lets you search your gigantic node modules directory_
- visual studio intellicode: _AI autocompletion and suggestions, works WAY
  better than I thought it would_

### Theming and other stuff

- Dracula: _currently my favorite color theme, I also like solarized dark_
- vscode-icons: _nice icon set for filetypes in the built-in file explorer_
- Fluent Icons: _some different icons for vscode features_
- Discord Presence - _displays what you're doing in VSCode in the Discord
  sidebar_

### Styling READMEs

- [Markdown Preview Github Styling](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)
  (Extension Pack)
- [Mermaid Markdown Syntax Support](https://marketplace.visualstudio.com/items?itemName=bpruitt-goddard.mermaid-markdown-syntax-highlighting) -
  Adds syntax highlighting for mermaid charts (which I used to create the gantt
  chart in the [course README](/README.md#coursework))

### Optional, more advanced developer tools

- Individual language support extensions: _there will be an extension for
  practically any language. just search for it in the marketplace._
- snippets: _vscode snippets are little code templates. there are lots of
  extensions for specific snippets, and you can also write your own_
- Better Comments: _styles comments in code based on what type of comment it is_
- Pylance: _lots of features for writing/editing python code_
- Heroku CLI: _if you're using heroku, this lets you run any commands from
  inside VSCode_
- Docker: _again, useful if you use docker_
- Github pull requests and issues: _useful for larger projects that use issues
  or PRs_
- GitLens: _advanced git extension with features like authorship visualization_
- Remote - WSL: _useful for windows users who have the windows subsystem for
  linux installed_
- Vim: _if you prefer vim keybindings, install this. If you do not know vim, do
  not install this_
- Jupyter: _Support for Jupyter notebooks!_

[^docs]: https://code.visualstudio.com/docs
[^devsurvey22]:
    https://survey.stackoverflow.co/2022/#integrated-development-environment
