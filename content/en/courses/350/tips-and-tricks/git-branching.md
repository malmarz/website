---
title: "Git & GitHub Desktop: Branching Guide"
date: 2025-03-04
description: "A simple guide for students on using Git and GitHub Desktop for branching and merging."
draft: false
categories: ["Git"]
tags: ["git", "github", "branching", "desktop"]
# Academic page type (do not modify).
type: book
---

## Overview

Branching should allow you to experiment with code and make mistakes without breaking your project. Keep the following in mind when working with branches:
1. Your working project is always on the main branch. **NEVER CHANGE CODE ON IT! But you can run and test your project from it**
2. To start a new task, create a new branch from the main branch.
3. Switch to the new branch and start working on your task.
4. Once the task is complete and successful, merge the branch back to the main branch.
5. If the branch is broken or no longer needed, delete it.

This guide will help you understand how to create, merge, and delete branches using both GitHub Desktop and the command line. Choose your preferred method:

- [Using GitHub Desktop](#using-github-desktop)
- [Using Git (Command Line)](#using-git-command-line)

---

## Using GitHub Desktop

### 1. Creating a Branch for a Task

1. Open GitHub Desktop.
2. Click on **"Current Branch"** (top-left).
3. Click **"New Branch"**, name it, and click **"Create Branch"**.

### 2. Merging the Branch When the Task is Complete

1. Switch back to the **main branch**.
2. Click **"Branch" > "Merge into Current Branch"**.
3. Select your task branch and merge.

### 3. Deleting a Branch (If No Longer Needed or Messed Up)

1. Click **"Current Branch"**, then **"Manage Branches"**.
2. Right-click the branch and select **"Delete"**.

---

## Using Git (Command Line)

### 1. Creating a Branch for a Task

1. Open your terminal and navigate to the project folder.
2. Create a new branch:
   ```sh
   git checkout -b my-task-branch
   ```
3. Start working on your task in this branch.

### 2. Merging the Branch When the Task is Complete

1. Switch to the main branch:
   ```sh
   git checkout main
   ```
2. Merge your task branch:
   ```sh
   git merge my-task-branch
   ```


### 3. Deleting a Branch (If No Longer Needed or Messed Up)

- Delete locally:
  ```sh
  git branch -d my-task-branch
  ```

---

## Final Notes
- Always create a new branch for each task.
- Test your changes before merging.
- If a branch is broken, delete it and start fresh.
- **Never** work directly on the main branch.
- **Always** pull changes from the main branch before creating a new branch.
- You can run and test your project from the main branch. But don't change code on it.