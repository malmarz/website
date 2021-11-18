---
title: HTML Forms
summary: Simple user input
authors: []
tags: [isom350]
categories: []
date: "2021-11-18T05:53:42Z"
draft: false
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

HTML Forms

---

### What Are Forms?

- HTML component 
- Used to send user input to server
- POST forms include data in the body
- GET forms include data in the url
- Submit button is needed to perform send action

---

### Post Form

  ```html
  <form action="" method="POST">
    <!-- data input components here -->
    <input type=submit>
  </form>
  ```

---

### GET Form

  ```html
  <form action="" method="POST">
    <!-- data input components here -->
    <input type=submit>
  </form>
  ```

---

### POST VS GET

- Click the submit button and try to see the difference between the two
- What can you spot?

---

## Final Thoughts

- Using forms the way we did is not secure
  - You can use it for search queries and simple input
- Django Forms is used to make forms more secure
  - Covered in future topic.