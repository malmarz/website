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

draft: true

---

{{% callout note %}}
Due Date is <strong>Sunday Dec 26th before 10AM</strong>
{{% /callout %}}

## Requirements for This Assignments (50 pts)

- [ ] **10 pts:** Create a view to list all the posts which have a **published** status. For each poll in the list, show the poll title and date it will be active until.
- [ ] **10 pts:** Create a view to list all the posts which have a **unpublished** status,  For each poll in the list, show the poll title and date it will be active until.
- [ ] **5 pts:** Create an index view which allows the user to select whether to open the list view for published polls or the list view for unpublished polls (**Hint:** This is just a page with two links to the previous list views).
- [ ] **10 pts:** Create a view to show the details of a single poll which include the title, the questions, and list of choices available
- [ ] **5 pts:** In both poll list views, make the title of each poll into a link that opens the corresponding poll's detailed view when clicked.
- [ ] **10 pts:** In both poll list views, show number of options for each poll.

### Bonus Tasks

These tasks will involve reading the Django documentation and figuring out things on your own. Perform these tasks only after you complete the previous requirements of the assignment.

- [ ] In ReadMe.md, create a section named **Bonus** and list all the bonus items you completed in this project. Bonus items will be ignored if not listed on Readme.md
- [ ] **(10 pts)** For the links, instead of typing the path yourself, give the path names and use the [url template tag from Django](https://docs.djangoproject.com/en/3.2/ref/templates/builtins/#url)
- [ ] **(5 pts)** In the Poll list view, instead of showing absolute time in which the poll will be active until (e.g., 10pm 12/12/2021) show the relative time it will remain active (e.g, **active for another 10 days, 6 hours, 5 minutes**). Search Django's template filters to find the solution. It should be a very simple one. 
- [ ] **(10 pts)** Read about the [bootstrap CSS framework](https://getbootstrap.com/docs/5.0/getting-started/introduction/) and try to use it to improve the look and feel of your application
- [ ] **(20 pts)** Get a head start and read this [Django forms tutorial](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms), try to create a view that allows users to submit their responses **(HINT: You will also need to read about ModelChoiceField)**


## How to Start and Submit Your Project

1. Join the [poll-project part 2 assignment on github classroom](https://classroom.github.com/a/oEFiaoXL).
2. Clone your assignment project using GitHub desktop to your computer and remember to work on the main/master branch.
3. When done, commit then push your work using GitHub Desktop. You can continue to make changes and push code after submission.

## Grading Criteria

- If submitted project doesn't work, you will receive **5 pts only**
- If submitted project works, breakdown of grades shown next to each requirement (Partial credit could be awarded)