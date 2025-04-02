---
# Page title
title: The Poll Project 2nd Assignment

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: Part 2

# Date page published
date: 2021-05-26T16:24:05Z

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 40

draft: false

---

{{% callout note %}}
The due date for this assignment is <strong>Wednesday, April 9th, 11:59pm</strong>.
{{% /callout %}}

## Assignment Requirements

- [ ] **15 pts:** Create a view to display all polls with a **published** status. For each poll, show the poll title and the date it will remain active until.
- [ ] **15 pts:** Create a view to display all polls with an **unpublished** status. For each poll, show the poll title and the date it will remain active until.
- [ ] **10 pts:** Create an index view that allows the user to choose between viewing the list of published polls or unpublished polls (**Hint:** This is a page with two links to the respective list views).
- [ ] **15 pts:** Create a detailed view for a single poll that includes the title, the questions, and the list of available choices.
- [ ] **10 pts:** In both poll list views, make the title of each poll a clickable link that opens the corresponding poll's detailed view.
- [ ] **10 pts:** In both poll list views, display the number of options available for each poll.

### Update ReadMe.md

- [ ] Add a section to the `ReadMe.md` file detailing how the work was distributed. Include the following:
    - The project manager's name.
    - How tasks were distributed among team members.
    - How the team collaborated.
    - Any other relevant information about the project management process.

### Bonus Tasks

These tasks require additional research using the Django documentation. Complete them only after finishing the main assignment requirements.

- [ ] In `ReadMe.md`, create a section named **Bonus** and list all the bonus items you completed. Bonus items will not be considered if they are not listed in the `ReadMe.md`.
- [ ] **(10 pts)** Use Django's [url template tag](https://docs.djangoproject.com/en/3.2/ref/templates/builtins/#url) for links instead of hardcoding paths.
- [ ] **(5 pts)** In the poll list views, display the relative time remaining for each poll (e.g., **active for another 10 days, 6 hours, 5 minutes**) instead of the absolute time. Use Django's template filters to achieve this.
- [ ] **(10 pts)** Explore the [Bootstrap CSS framework](https://getbootstrap.com/docs/5.0/getting-started/introduction/) and use it to enhance the appearance of your application.
- [ ] **(20 pts)** Get a head start by reading this [Django forms tutorial](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms). Try creating a view that allows users to submit their responses (**Hint:** You will also need to learn about `ModelChoiceField`).

## How to Start and Submit Your Project

1. Join the [poll-project part 2 assignment on GitHub Classroom](https://classroom.github.com/a/YV0sEa1T).
2. Clone your assignment project using GitHub Desktop and work on the main/master branch.
3. When finished, commit and push your work using GitHub Desktop. You can continue to make changes and push updates after submission.

## Grading Criteria (Total 100 pts, 5% of total grade)

- If the submitted project does not work, you will receive **5 pts only**.
- Demonstrating proper teamwork and collaboration **25 pts**:
    - Use of pull requests, branching, and proper merging will be evaluated.
- If the submitted project works, the breakdown of grades is shown next to each requirement (partial credit may be awarded) **75 pts**.