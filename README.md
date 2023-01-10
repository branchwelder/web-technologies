![](/assets/header.png)

Welcome to Web Technologies! This is the central repository for the course
content, which is organized as follows:

- `activities/` contains instructions for in-class activities
- `assignments/` contains instructions for each course assignment
- `examples/` contains small examples and starter code for the mini projects
- `resources/` contains lists of resources for your reference
- `slides/` contains PDF versions of slides used in class

Please also see [the syllabus](/syllabus.md) for a course overview.

---

## Coursework

This is a project-based course. There is no "one true way" to learn about web
technologies. Instead of problem sets and quizzes in which their work will be
lost to time, students will "just build websites"[^justbuildwebsites]. We will
begin by setting up a portfolio website, which will grow over the quarter to
document projects done for the course. As a result, any work done for this
course will be publicly visible. Coursework comprises mini projects, a final
project, and development reflections ("hair tear shares").

```mermaid
%%{
  init: {
    'theme': 'base',
    'gantt': {
        'numberSectionStyles': '2'
    },
    'themeVariables': {
      'fontFamily': 'monospace',
      'primaryColor': '#8c9aee',
      'primaryBorderColor': '#3C56E2',
      'tertiaryColor': '#f7f75e'
    }
  }
}%%

gantt
title Winter 2023 Assignment Schedule
axisFormat  %b %e

section Continuous
Portfolio             :active,          prf,  2023-01-03, 2023-03-17
Peer Teaching         :active,          pte, 2023-01-03, 2023-03-17

section Shares
Hair Tear Share 1     :milestone, crit, hts, 2023-01-17, 0d
Hair Tear Share 2     :milestone, crit, hts, 2023-02-09, 0d
Demo Day              :milestone, crit, dem, 2023-03-09, 0d

section Mini Projects
Setup                 :active,          mp0, 2023-01-03, 2023-01-10
Browser Extension     :                 mp1, 2023-01-10, 2023-01-24
Audio Visualizer      :                 mp2, 2023-01-24, 2023-02-07
Game                  :                 mp3, 2023-02-07, 2023-02-21

section Final Project
Proposal              :                 fp0, 2023-02-16, 2023-02-23
MVP                   :                 fp1, 2023-02-23, 2023-03-02
Final version         :                 fp2, 2023-03-02, 2023-03-17
```

## Weekly Schedule

<details><summary><h3>Week 1: Intro and HTML/CSS</h3></summary>

#### 1.1 January 3: Welcome and Environment Setup

- Lecture
  - Welcome and course overview
  - [slides](slides/1.1.pdf)
- In-class
  - Activity: [Environment setup](activities/01_intro.md)
- Assigned work
  - [MP0: Portfolio site](projects/mp0_portfolio.md)

#### 1.2 January 5: HTML/CSS Intro

- Lecture
  - Git review: cloning a repo, editing content, pushing changes
  - MP0 example walkthrough
  - HTML/CSS, live demo
  - [slides](slides/1.2.pdf)
- In-class
  - Continue working on [MP0: Portfolio](assignments/mp0_portfolio.md)

</details>

<details><summary><h3>Week 2: The DOM, Javascript, and Web Extensions</h3></summary>

#### 2.1 January 10: Javascript Intro

<!-- TODO: Browser Extension Example -->
<!-- TODO: JS Intro Slides -->
<!-- TODO: JS Interaction example -->
<!-- TODO: MP1 Writeup -->

- Due
  - MP0
- In-class
  - [slides](slides/2.1.pdf)
  - MP0 share
  - JavaScript overview!
  - Break
  - Intro to the DOM
  - Codepen Live demos!
  - Lab time! [activity](/activities/02_js_and_the_dom.md)
- Tonight: MP1 released: browser extension

#### 2.2 January 12

<!-- TODO: Extension Slides -->

- Lecture
  - Browser Extensions overview, MP1 walkthrough
- In-class
  - Continue MP1: Browser Extension

</details>

<details><summary><h3>Week 3: Development Tools and Strategies</h3></summary>

#### 3.1 January 17

<!-- TODO: HTS writeup -->

- Due
  - Hair Tear Share #1
- Lecture
  - Dev Tools
  - Debugging approaches
- In-class
  - Hair Tear Shares
  - Continue MP1: Browser Extension

#### 3.2 January 19

- Lecture
- In-class
  - Continue MP1: Browser Extension

</details>

<details><summary><h3>Week 4: Browser APIs</h3></summary>

### Week 4

#### 4.1 January 24

- Due
  - MP1 - Browser Extension
- Lecture
  - Intro to Browser APIS
- In-class
  - Share: MP1
  - Activity:
  - Begin MP2: Audio Visualizer

#### 4.2 January 26

- Lecture
  - SVG
- In-class
  - Continue MP2: Audio Visualizer

</details>

<details><summary><h3>Week 5: Libraries and Frameworks</h3></summary>

### Week 5

#### 5.1 January 31

- Lecture
  - Web Components: htmlElement, React, and Lit
- In-class
  - Continue MP2: Audio Visualizer

#### 5.2 February 2

- Lecture
- In-class
  - Continue MP2: Audio Visualizer

</details>

<details><summary><h3>Week 6: Games and Interactivity</h3></summary>

#### 6.1 February 7

- Due
  - MP2 - Audio Visualizer
- Lecture
- In-class
  - Share-back: MP2: Audio Visualizer
  - Begin MP3: Game

#### 6.2 February 9

- Due
  - Hair Tear Share #2
- Lecture
- In-class
  - Hair Tear Shares
  - Continue MP3: Game

</details>

<details><summary><h3>Week 7: Mobile</h3></summary>

#### 7.1 February 14 _NO CLASS - HANNAH TRAVELING_

- Outside class
  - Continue MP3: Game

#### 7.2 February 16

- Lecture
- In-class
  - Continue MP3: Game

</details>

<details><summary><h3>Week 8: The Full Stack</h3></summary>

#### 8.1 February 21

- Due
  - MP3 - Game
- Lecture
  - Planning your projects
- In-class
  - MP3 Share

#### 8.2 February 23

- **DUE: FP0 - Final Project Proposal**
- Lecture
  - TBD
- In-class
  - FP0 Share
  - Project work time

</details>

<details><summary><h3>Week 9: Special Topics, Project Iteration</h3></summary>

#### 9.1 February 28

- Lecture
  - TBD
- In-class
  - Project work time

#### 9.2 March 2

- **DUE: FP1 - MVP**
- Lecture
  - TBD
- In-class
  - Project work time

</details>

<details><summary><h3>Week 10: Project wrap-up and Demos!</h3></summary>

#### 10.1 March 7

- Lecture
  - TBD
- In-class
  - Project work time

#### 10.2 March 9

- Lecture
  - Wrap-up, looking forward
- In-class
  - Final Projects demo day and fun!

</details>

<details><summary><h3>Week 11: Finals Week</h3></summary>

#### March 17

- **DUE: FP2: Final Project**
- **DUE: Final Portfolio**

</details>

[^justbuildwebsites]: http://justbuildwebsites.com/
