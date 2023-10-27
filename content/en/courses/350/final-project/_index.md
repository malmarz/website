---
# Page title
title: Final Project

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: Final Project

# Date page published
date: 2021-12-01T13:25:49Z

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 100

draft: false
---

{{% callout note %}}
Demonstrations are due on day before last of our class, Monday, Dec 25th during class time
{{% /callout %}}

# Your Options
Since this is a project course, you are expected to work on a project. You have two options to choose from:
1. You can choose your own project.
2. You can choose to work on the e-commerce project described below.

## Option 1: Choose Your Own Project

You can choose your own project if you think this will drive you to learn more. I will require that you submit a proposal describing your project and include the complete requirements. Your proposal should be shown to me after class or during office hours. You **must get my approval before you can take this options**.

Teams have until Nov 9th to get my approval. Otherwise, they will be forced to take the e-commerce project.

## Option 2: E-Commerce Project

You sit down with a representative of an online retailing business that are looking to build a new e-commerce platform for their business. In the interview, he gives the following description of what they want in the new platform:

'''
We require an e-commerce platform to display our products and allow users to search and purchase items. Since we are an online retailer, our products will have different categories. The product will have a description, a serial number, price, and quantity in store. It would also be preferable to have an image displayed of the product and have simple inventory management as part of the system.

The platform should keep track of our customer information. At the minimum, we expect to keep records of our customers' names, addresses, emails, and phone numbers. The platform should also provide some CRM features to help us manage our customers to improve their loyalty. For that, we need to at least keep track of the purchase history of our customers and calculate a profitability score for them.

We are also interested in ways in which to promote sales of our products. Customers should be able to review and read reviews on our products or see which of our products are selling the most from different categories.
'''

The description would be a good start for your team to set the main requirements. It represents the bare minimum that should be included in the system. You can go beyond what the description provides for additional credits, but be sure to cover the customer requirements.

USe this description to build the ER Diagram for your project then start putting together requirements in the form of tickets. Then start implementing the system and updating the tickets as you get more ideas on how to improve the system. Do your best to implement as much of the requirements as you can. Be sure to leave the tickets that you do not complete in the ticket management system as it will indicate how much you have thought about the system.


## Requirements For Both Options

- [Signup your team](https://classroom.github.com/a/nzIxyJ4Q).
- Team must agree on a project manager. Write the name of the team members on the readme file and make clear who the project team leader is.
- **If you chose option 1:** You must describe the complete requirements of your projects in the Readme file of the project.
- **If you chose option 2:** You must make clear in the readme file that you are working on the e-commerce project and give your project a unique name that reflects what you are selling or the imaginary company you are serving.
- **For both project options:** perform the following project management and design tasks
  - Determine the information requirements of the project by drawing the ER-Diagram. You can use [ERD Plus](https://erdplus.com/) then download the image and post it in the Readme file of the project.
  - Determine the requirements of the project in one of two options:
    1. Write the requirements in the Readme file of the project. They should be broken down into specific task exactly like the requirements in the Poll project assignment you worked on. Each requirement must describe a single task.
    2. **Optional (Bonus based on how well you use it):** Utilize a ticketing system to manage and coordinate your project. Requirments will be written as ticket. You must read and learn agile project management skills on your own here. You will need to invest some time reading and trying out the process. Your options are:
  - [GitHub issues](https://docs.github.com/en/issues)
  - [Trello](https://trello.com/guide)
  - [Jira](https://www.atlassian.com/software/jira/guides/getting-started/introduction#what-is-jira-software)

- Arrange to bring one of your PC to class and use it to demonstrate your project.
- **Important:** Try to go beyond the provided requirements to make your application more valuable. You can only achieve this if you spend time learning new things about Django and utilize your time in class wisely.


## Grading The Final Project

### 1. The Demonstration (30%)

  Each team will be given 10 minutes to demonstrate their web application and show that it works. In the ten minutes you need to perform the following:
  1. Introduce the team members and the general idea of the web application
  2. Demonstrate the main operation in the app from your choosing and not necessarily all the features. But make sure you show the best parts of your application and show that it is well designed and works (Try to sell it to me or get me to invest in it).
  3. Be prepared for a Q&A session about your improvements to the app (how you made it more valuable), using the app, and technical questions about the app.

  In the demo, you will mostly be evaluated based on:
  - How well you utilize your time
  - How well you present your web app and convince us of its added value
  - How well the features you implemented meet the main requirements of the app
  - How well you have prepared the app (be sure to include test data and plan how you will show your app)
  - How well you answers questions (whether technical about the app/design or business about the idea)
  - How well your application works


### 2. The Design (10%)

TThe design effort of the team will be based on:
- The appropriateness of the ERD
- The requirements gathered and written into the ticketing system (be sure not to delete any ticket, even the ones you do not work on)
- Whether you meet the requirements set by the customer in their description or not. You are welcome for this project to go beyond what the customer asked for, but be sure to cover the requirements.

### 3. The Collaboration (30%)

Teams are expected to utilize what they have learned in this course about GitHub and Collaboration. Evaluation will be based on:
- How well you get everyone involved in project development and management
    - Contributing to development
    - Contributing to project management
- How well you utilize GitHub for collaboration and project management, which include:
    - Properly using pull requests
    - Properly using tickets
    - Having clear communication and guidelines in the readme for the team to read

### 4. Individual Contribution (30%)

  Individual contribution will be based on:
  1. The amount of work done by the individual as reported by GitHub (focused on code)
  2. Peer evaluation

### 5. The Code Review

 A final review of the code by the instructor will be performed and could affect your final grade. It will mainly be used to:

 1. Determine that the work was done by the group and not a 3rd party. The group could receive a zero on this project if they received outside assistance. Remember, this is an investment in your self. Work hard to gain the experience.
 2. Determine that the application works as expected.
 3. Evaluate bonus grades which. Your group is expected to list all additions done to the project worthy of a bonus grade in a section named **Bonus Items** in the Readme file of the project. List additional features to the requirements and any Django features you used that we did not explain in class. Be sure to list the file and line number that feature was implemented so your instructor can confirm its use. **Failure to follow this instruction would mean that the project team would not receive any bonus points, only listed bonus items will receive grades**. You can get ideas for bonus activities by reading the [advanced django section]({{< ref "django-advanced" >}}).

