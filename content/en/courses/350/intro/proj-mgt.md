---
# Page title
title: Project Management

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: Project Management

# Page summary for search engines.
summary: Second programming course for MIS majors utilizing Python to build data-driven business applications.

# Date page published
date: 2021-03-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 6

draft: False
diagram: True

---

## Introduction to Project Management

Project management is the process of planning, organizing, and controlling resources to achieve specific goals within defined constraints such as time, budget, and scope. In software development, project management ensures that the project is completed to specification, delivered on time, and stays within budget. This involves coordinating team members, managing requirements, tracking progress, and resolving issues that arise during development.

Key responsibilities of project management include:
- Defining project scope and requirements
- Planning and scheduling tasks
- Allocating resources and assigning responsibilities
- Monitoring progress and managing risks
- Ensuring quality standards are met
- Facilitating communication between stakeholders

## Conventional SDLC (Software Development Life Cycle)

The conventional SDLC, also known as the Waterfall model, is a sequential approach to software development that follows distinct phases:

1. **Requirements Analysis:** Gather and document all system requirements upfront
2. **System Design:** Create detailed architecture and design specifications
3. **Implementation:** Write code based on the design documents
4. **Testing:** Verify that the system meets requirements
5. **Deployment:** Release the software to users
6. **Maintenance:** Fix bugs and make updates as needed

Each phase must be completed before moving to the next phase, with formal reviews and sign-offs at each stage.

### Advantages of Conventional SDLC

- **Clear structure and milestones:** Well-defined phases make it easy to understand project progress
- **Comprehensive documentation:** Detailed documentation at each phase helps with knowledge transfer
- **Easy to manage:** Sequential nature makes it simple to manage and track
- **Works well for stable requirements:** Ideal when requirements are well-understood and unlikely to change
- **Predictable timelines and budgets:** Upfront planning allows for accurate cost and time estimates

### Disadvantages of Conventional SDLC

- **Inflexible to changes:** Difficult and costly to go back and make changes once a phase is complete
- **Late testing:** Problems are discovered late in the development cycle, making them expensive to fix
- **No working software until late:** Customers don't see working software until near the end of the project
- **Risk of misunderstanding requirements:** Requirements gathered at the beginning may not reflect actual needs
- **Not suitable for complex projects:** Long development cycles can lead to outdated solutions by the time of delivery
- **Limited customer involvement:** Customers are primarily involved only at the beginning and end

## Agile Project Management

Agile project management is an iterative approach to software development that emphasizes flexibility, collaboration, and continuous improvement. Unlike the conventional SDLC, agile divides the project into small increments called sprints (typically 1-4 weeks), with each sprint producing a potentially shippable product increment.

Key principles of agile development include:
- **Iterative development:** Build software in small increments rather than all at once
- **Adaptive planning:** Requirements and plans evolve throughout the project
- **Customer collaboration:** Continuous involvement of customers and stakeholders
- **Self-organizing teams:** Team members have autonomy to choose tasks and make decisions
- **Continuous feedback:** Regular reviews and retrospectives to improve processes
- **Responding to change:** Welcome changing requirements, even late in development

The project manager's role in agile is different from traditional approaches:
- **Facilitator rather than controller:** Helps remove obstacles rather than micromanaging tasks
- **Prioritizes the backlog:** Ensures the most valuable features are worked on first
- **Ensures team collaboration:** Facilitates communication between team members and stakeholders
- **May contribute as a developer:** Can work on tasks like other team members
- **Monitors progress:** Tracks sprint progress and helps the team stay on track
- **Sets up collaboration environment:** Provides tools and processes for the team to work effectively

### Advantages of Agile Project Management

- **Flexibility to change:** Requirements can evolve based on feedback and changing business needs
- **Early and continuous delivery:** Working software is delivered frequently, providing value sooner
- **Customer satisfaction:** Regular feedback ensures the product meets customer needs
- **Risk mitigation:** Issues are identified and addressed early in each iteration
- **Team empowerment:** Developers have ownership and can make decisions
- **Improved quality:** Continuous testing and integration lead to fewer bugs
- **Better visibility:** Daily standups and sprint reviews provide transparency

### Disadvantages of Agile Project Management

- **Less predictability:** Difficult to estimate total time and cost upfront
- **Requires commitment:** Needs active participation from customers and stakeholders
- **Documentation may suffer:** Focus on working software can lead to inadequate documentation
- **Challenging for distributed teams:** Requires strong communication, which can be difficult remotely
- **Scope creep risk:** Flexibility can lead to continuously expanding requirements
- **Requires experienced team members:** Self-organization requires mature, skilled developers
- **Not suitable for all projects:** Fixed-price, fixed-scope contracts may not work well with agile

## Using GitHub Projects for Agile Management

GitHub Projects provides a powerful way to implement agile project management using Kanban boards. A Kanban board visualizes work and helps teams manage the flow of tasks from start to completion.

### Creating a GitHub Project

There are two main ways to create a project:

1. **Creating a new repository:** Start from scratch either on GitHub or by pushing from your local environment
2. **Forking an existing project:** Build upon an existing codebase found on GitHub

Once your repository is set up, you can create a GitHub Project board to manage your work.

### Setting Up a Kanban Board

GitHub Projects uses a Kanban-style board with customizable columns. A typical agile board includes:

1. **To Do (Backlog):** Tasks that need to be completed, ordered by priority
2. **Ready:** Tasks that are ready to be worked on next (Optional)
3. **In Progress:** Tasks currently being worked on
4. **In Review:** Tasks that are completed and have a pull request created. These are awaiting review or testing (Optional)
5. **Done:** Completed tasks ready for review or deployment

To create a new project board:
1. Navigate to the "Projects" tab in your repository
2. Click "New Project"
3. Choose "Kanban" as the template
4. Name your project and add a description if desired

{{< figure src="courses/350/project-create.png" caption="GitHub Projects Kanban Board" >}}


Each ticket can represent:
- A new feature to be built
- A bug that needs fixing
- An idea to be discussed
- Documentation to be written
- Any other task that needs completion

{{< figure src="courses/350/project-board.png" caption="GitHub Projects Kanban Board" >}}

#### Creating Effective Issues

When creating issues, ensure each one:
- Describes a specific, actionable task
- Is small enough to be completed in a reasonable timeframe
- Includes clear acceptance criteria
- Is written as a user story when appropriate (e.g., "As a user, I want to... so that...")

{{% callout note %}}
The best method to write useful task descriptions is to write issues as **user stories**. User stories describe functionality from the user's perspective and include what the user does and why. For more information, see this [blog post on writing user stories](https://medium.com/innovation-machine/how-and-why-to-write-great-user-stories-f5a110668246).
{{% /callout %}}

#### Who Creates Issues?

The responsibility of creating issues is shared:
- **Project Manager:** Ensures there are enough issues to keep the team busy and captures key requirements
- **Developers:** Create issues when they discover bugs or have ideas for improvements
- **Users/Customers:** Can submit feature requests or bug reports

{{% callout note %}}
Whether you are the project manager or a team member, you can create issues to capture ideas, bugs, and tasks for the team to work on.
{{% /callout %}}

### Working with the Kanban Board

#### 1. Prioritizing Work (To Do Column)

The project manager organizes tasks in the **Ready** column by priority, with the highest priority items at the top. Team members should select tasks from the top of this column to ensure the most important work gets done first.


#### 2. Claiming and Working on Tasks (In Progress Column)

When a team member starts working on a task, they should:
1. Assign the issue to themselves
2. Move the issue to the **In Progress** column
3. Create a branch to work on the task

![Claiming a task and moving it to In Progress](/gifs/claim-ticket.gif)

{{% callout note %}}
Always assign yourself to a task before starting work. This lets your team members know what you're working on and prevents duplicate effort.
{{% /callout %}}

#### 3. Completing Tasks (Done Column)

When a task is completed:
1. Create a pull request with your changes
2. Move the issue to the **In Review** column
3. Request review from team members or the project manager
4. Once merged, the issue can be closed and moved to the **Done** column


### Monitoring Progress

The Kanban board provides a visual overview of project progress:
- **Backlog column:** Shows the remaining work and priorities
- **Ready column:** Shows tasks ready to be picked up next
- **In Progress column:** Shows who is working on what
- **In Review column:** Shows tasks that are completed and awaiting review
- **Done column:** Shows completed work that is ready to be deployed

If a task remains in **In Progress** for too long, it signals a potential problem that may require the project manager's intervention.

### Collaboration Practices

**Sprint Planning:** Meet at the beginning of each sprint to:
- Review and prioritize the backlog
- Estimate tasks
- Commit to what can be completed in the sprint

**Daily Standups:** Brief daily meetings where team members share:
- What they completed yesterday
- What they're working on today
- Any blockers they're facing

**Sprint Reviews:** At the end of each sprint:
- Demo completed features
- Gather feedback from stakeholders
- Update the backlog based on feedback

**Retrospectives:** Team reflects on:
- What went well
- What could be improved
- Action items for the next sprint

{{% callout note %}}
Regular coordination meetings (weekly or bi-weekly) help teams stay aligned. Use these meetings to review the project board, discuss priorities, address challenges, and collaborate on solutions.
{{% /callout %}}

## Review Questions

1. What is project management and what are its key responsibilities in software development?
2. Describe the phases of the conventional SDLC (Waterfall model).
3. What are the main advantages of using a conventional SDLC approach?
4. What are the main disadvantages of the conventional SDLC?
5. How does agile project management differ from conventional SDLC?
6. What are the key principles of agile development?
7. What are the advantages of using agile project management?
8. What are the challenges or disadvantages of agile approaches?
9. How does the project manager's role differ in agile versus traditional project management?
10. What is a Kanban board and how is it used in GitHub Projects?
11. List the five columns in a GitHub Projects Kanban board and explain what each represents. Which columns are optional?
12. What can a GitHub Issue represent in a software project?
13. Who is responsible for creating issues in an agile project?
14. Why is it important to assign yourself to a task before starting work on it?
15. How should tasks be prioritized and in which column should this prioritization occur?
16. Describe the workflow of a task from creation to completion, including all the columns it moves through.
17. What should you do when you complete a task and are ready for it to be reviewed?
18. What are user stories and why are they useful for writing issues?
19. What are the key collaboration practices in agile (sprint planning, standups, sprint reviews, retrospectives)?
20. What does it signal if a task remains in "In Progress" for too long?