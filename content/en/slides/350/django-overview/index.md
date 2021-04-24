---
title: Django Overview
summary: Gives a general overview of the main steps in the Django development process
authors: []
tags: [isom350]
categories: []
date: "2021-04-24T10:14:50Z"
slides:
  # Choose a theme from https://github.com/hakimel/reveal.js#theming
  theme: moon
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  #   Available highlight themes listed in: https://highlightjs.org/static/demo/
  #   Use lower case names and replace space with hyphen '-'
  highlight_style: dracula

  diagram: true
  diagram_options:
    # Mermaid diagram themes include: default,base,dark,neutral,forest
    theme: dark

  # RevealJS slide options.
  # Options are named using the snake case equivalent of those in the RevealJS docs.
  reveal_options:
    controls: true
    progress: true
    slide_number: c/t  # true | false | h.v | h/v | c | c/t
    center: true
    rtl: false
    mouse_wheel: true
    transition: concave  # none/fade/slide/convex/concave/zoom
    transitionSpeed: default  # default/fast/slow
    background_transition: slide  # none/fade/slide/convex/concave/zoom
    touch: true
    loop: false
    menu_enabled: true
    chalkboard_enabled: true
    history: true
---


# ISOM 350
## Business Application Development

Mohammad AlMarzouq

Overview of Django Development Process

---

```mermaid
graph TD
A[Setup Project] --> B[Start App for Subproject]
B --> C[Define Data Models]
C -->|Work on Single Feature| D[Create View Function] 
D -->E[Wire URLs to View]
E -->F[Create Templates]
F -->|Refine or Work on Next Feature|D
F -->|Refine or Work on Next Subproject|B
```

---

## The Steps

--- 

### 1- Project Setup

- Creates directory structure for project files
- Done once at the beginning of the project

---

### Project Setup Methods

1. **(Recommended for this course)** Creating a **Django Template** project in replit.com. 
2. Importing an existing Django project from GitHub. GitHub project can be a new Django project or forked from a Django project. Use this option when you want to collaborate on an existing project.
3. Using **shell** you type a command to create a Django project.

---

## Asynchronous Collaboration

- Developers working together over time
- Enabled using Git and GitHub
  - Integrated with replit.com
- Requires agreement on workflow
- Better fit for large group collaboration and effort tracking

---

## Asynchronous Collaboration Limitations

- Steep learning curve
- Overhead to using the tools
  - Greater benefits with larger groups
  - Still useful for individuals
- Benefit of using collaboration tools might not be clear
- Success dependent on choice from endless workflows

--- 

## Developer Workflow for Our Course

```mermaid
graph TD
    A[Find new Task]
    B[Create New Branch]
    C[Work on Task]
    D[Commit Work Done]
    E[Send Pull Request to Project Manager]
    A --> B
    B --> C
    C --> D
    D -- Bug Exists --> C
    D -- Task or Fix Complete --> E
    E --> A
```

---

## Branches and Pull Requests

- Always create a branch from main/master to start your work
- Once done, create a pull request to ask the project manager to include your work (merge it) to the project
- Discussion can be started around a pull request where manager can ask members to fix problems in their work
- Pull request is completed if it is successfully merged

---


{{< figure src="courses/350/pr-create.png" caption="Creating a Pull Request in Same Repo" >}}

---

{{< figure src="courses/350/pr-create2.png" caption="Creating a Pull Request To Different Repo" >}}

---

{{< figure src="courses/350/pr-discussion.png" >}}

---

## Git and GitHub

- You need to distinguish between these two
- Git is the tool we use to keep track of the changes made to our source code and combine our work
- GitHub is the cloud platform hosting our git repositories
- GitHub also introduced social coding and project management features to be used with Git

---

## What About Replit?

- Replit is an cloud based IDE
- You use it to write code
- You can pull and push code between it and GitHub

---

## What About Replit?
- When you work alone you pull/import your work to replit.
- When you want your team to see your work you push it to GitHub from replit.
- You work is cloned (i.e., copied) to Replit and another on GitHub
- Each team member gets their own clone of the project code


---

## What If I Cannot Use GitHub?

- Part of your evaluation in this course is based on how well you collaborate through GitHub
- Using Git and GitHub is a very important skill for developers and managers in this age
- You can complete your final project using Synchronous collaboration on replit.com
  - Your grade will suffer from this