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
This is an **optional** assignment and will give you an opportunity to make up for your quiz and assignments grades.
Due Date is <strong>Thursday Nov 30th 2pm</strong>
{{% /callout %}}

## Requirements for This Assignments 

- [ ] **(15 pts)** Create a view to create a poll that redirects you back to the poll list upon successful completion (Excluding the options, another view will be used to create them)
- [ ] **(15 pts)** Create a view to add a single option to a poll. Link the view to the detailed view of the poll where the user can input the option details and hit submit to add it to the poll. (**Hint:** The option creation view should redirect the user to the detailed poll view)
- [ ] **(30 pts)** Create a view that allows a user to submit their response to a poll.
- [ ] **(15 pts)** Create a view that allows you to edit the poll question and title only. Upon successful completion the user should be redirected to the detailed poll view.

### ReadMe.md
- [ ] Update the readme file with a section to detail how work was ditributed. The section should include the following:
    - Who was the project manager
    - How work was distributed
    - How the team collaborated
    - Any other information you think is relevant to the project management process

### Bonus Tasks

These tasks will involve reading the Django documentation and figuring out things on your own. Perform these tasks only after you complete the previous requirements of the assignment.

- [ ] In ReadMe.md, create a section named **Bonus** and list all the bonus items you completed in this project. Bonus items will be ignored if not listed on Readme.md
- [ ] **(20 pts)** In the show_poll view, add a form to allow for users to post comments about the poll. Do not forget to create a model for the comments that must be associated with a poll. The comment should allow user to enter his name, email, and text of the comment. The comments should be displayed above the comment form in chronological order, which is why you must record the time the comment was created also.
- [ ] **(10 pts)** Read about the [bootstrap CSS framework](https://getbootstrap.com/docs/5.0/getting-started/introduction/) and try to use it to improve the look and feel of your application if you havent done already.
- [ ] **(5 pts)** If you have successfully used bootstrap, try to convert all the link for editing bootstrap to look like buttons

## How to Start and Submit Your Project

1. Join the [poll-project part 3 assignment on github classroom](https://classroom.github.com/a/BRv3EByY).
2. Clone your assignment project using GitHub desktop to your computer and remember to work on the main/master branch.
3. When done, commit then push your work using GitHub Desktop. You can continue to make changes and push code after submission.

## Grading Criteria (Total 100 pts, 10% of total grade)

- If submitted project doesn't work, you will Not receive any credits for this assignment
- Demonstrating proper team work and collaboration **25 pts**
    - Use of pull requests, branching, and proper merging will be checked.
- If submitted project works, breakdown of grades shown next to each requirement (Partial credit could be awarded) **75 pts**