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
  theme: solarized
  # Choose a code highlighting style (if highlighting enabled in `params.toml`)
  #   Light style: github. Dark style: dracula (default).
  #   Available highlight themes listed in: https://highlightjs.org/static/demo/
  #   Use lower case names and replace space with hyphen '-'
  highlight_style: dracula

  diagram: true
  diagram_options:
    # Mermaid diagram themes include: default,base,dark,neutral,forest
    theme: forest

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
- Submit button is needed to perform submit action

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
  <form action="" method="GET">
    <!-- data input components here -->
    <input type=submit>
  </form>
  ```

---

### Data Input Components

- These are the components used to get input from the user
- There are numerous types depending on type of input you need from the user
- Input types include
  - text, checkbox, radio, email, password ...etc
  - We typically use `label` tag to add labels
  - List can be found [here](https://www.w3schools.com/html/html_form_input_types.asp)

---

### Form Example

  Create the following GET form in a Django template:

  ```html
  <form action="" method="GET">

    <label for="username">Username:</label>
    <input type="text" name="username">
    <br />
    <label for="pwd">Password:</label>
    <input type="password" name="pwd">

    <input type=submit>
  </form>
  ```

---

### Form Input

- Open the view with the form then enter some data
- Click the submit button and see what happens
- Notice the importance of the `name` property in the input tag
  - It specifies the variable name that holds the data

---

### Using Form Input in Views

- Depending on form type (GET vs POST) you access request.GET or request.POST
- Both are just python dictionaries
- Use the `name` value as the key to fetch the data in the input

---

### Using Form Input in Views

```python
def form_view(request):
  print("Username:", request.GET.get("username"))
  print("Password:", request.GET.get("pwd"))
  return render(request, "form.html")
```
- Use the values from the dictionary as you would any variable
---

### GET Vs POST Form

- Replace the form method to `POST`
- Submit some data
  - Can you spot the difference?
  - Fix the view so the data would be printed correctly

---

## GET Vs POST Form

- Do you think POST is more secure than GET?
- You answer should be `no!` both are insecure
- You need to use `https` and Django Forms to improve security
- Using POST is preferable in that case
- GET is more convenient when security is not a concern
  - Search and simple data input

---

## Exercise

Create a calculator view where the user:

- Inputs two values
- Chooses the operation
- Gets the result when the form is submitted

---

## Final Thoughts

- Using forms the way we did is not secure
- You can use it for search queries and simple input
- Django Forms is used to make forms more secure
  - Covered in future topic
