---
# Page title
title: The Poll Project 3nd Assignment

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: Part 3

# Date page published
date: 2021-06-06T14:29:57Z

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 50

draft: false

---

{{% callout note %}}
Due Date is <strong>Wed April 30th 10am</strong>
{{% /callout %}}

## Requirements for This Assignments 

- [ ] **(20 pts)** Create a view to create a poll. Upon successful creation, the view should redirect you back to the poll list.
- [ ] **(20 pts)** Create a view to add a single option to a poll. The view should display the poll, its existing options, and a form to add a new option. Upon successful submission, the view should redirect to itself, allowing you to add more options if needed. *(Hint: Use a redirect to reload the page with an empty form.)*
- [ ] **(20 pts)** Create a view to create a response associated with a selected option. The view should display the poll and the chosen option, with a submit button labeled "Confirm Choice." *(Hint: The selected option should be specified in the URL, e.g., `respond/option/5` for option ID 5.)* Upon successful submission, redirect the user to the detailed view of the poll.
- [ ] **(20 pts)** Create a view to edit the poll question and details. Upon successful submission, redirect to the detailed poll view.
- [ ] **(20 pts)** Create a view to edit a single poll option. Upon successful submission, redirect to the detailed poll view.

### ReadMe.md
- [ ] Update the readme file with a section to detail how work was ditributed. The section should include the following:
    - Who was the project manager
    - How work was distributed
    - How the team collaborated
    - Any other information you think is relevant to the project management process

### Bonus Tasks

These tasks require reading the Django documentation and figuring out solutions independently. Attempt these only after completing the main requirements.

- [ ] **(5 pts)** Add a link at the bottom of the poll list view to create a new poll. Link it to the create poll view.
- [ ] **(5 pts)** Add a link next to the poll question in the detailed poll view to edit the poll.
- [ ] **(5 pts)** In the poll edit view, add a link next to each option to edit it, linking to the edit option view.
- [ ] **(5 pts)** In the poll edit view, add a link below the options to add another option, linking to the add option view.
- [ ] **(5 pts)** In the detailed poll view, add a "Vote" link next to each option, linking to the create response view.
- [ ] **(10 pts)** Use Django's [URL template tag](https://docs.djangoproject.com/en/3.2/ref/templates/builtins/#url) to reference paths instead of hardcoding them.
- [ ] **(20 pts)** In the detailed poll view, add a form to allow users to post comments about the poll. Create a model for comments, associating them with a poll. Each comment should include the user's name, email, and the comment text. Display comments above the form in chronological order, including the time they were created.
- [ ] **(5 pts)** If you have used Bootstrap, convert all links for editing into Bootstrap-styled buttons.

## How to Start and Submit Your Project

1. Join the [poll-project part 3 assignment on github classroom](https://classroom.github.com/a/UXhGBlAj).
2. Clone your assignment project using GitHub desktop to your computer and remember to work on the main/master branch.
3. When done, commit then push your work using GitHub Desktop. You can continue to make changes and push code after submission.

## Grading Criteria (Total 100 pts, 5% of total grade)

- If submitted project doesn't work, you will Not receive any credits for this assignment
- Demonstrating proper team work and collaboration **25 pts**
    - Use of pull requests, branching, and proper merging will be checked.
- If submitted project works, breakdown of grades shown next to each requirement (Partial credit could be awarded) **75 pts**
