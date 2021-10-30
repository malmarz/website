---
# Page title
title: Visual Studio Code

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: VS Code

# Date page published
date: 2021-03-232021-10-30T09:46:26Z

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 1

draft: False
---

This is how VS Code looks like:

{{< figure src="courses/350/vscode.png" width="80%" caption="Visual Studio Code" >}}

- At the very top you have the menu and file tabs that allow you to switch from one file to the next.
- At the far left, there are the icons for the main controls of VS code in which will display different information in the panel next to it. Currently, the file explorer is selected showing the directory and file structure of the project.
- The main screen in the center shows the source code file and to the bottom of it are the terminal and debug consol to see the output of your code.


Let's examine the most important features that you need:

## Openning a File

Done from the top menu.

{{< figure src="courses/350/open-file.png" width="60%"  >}}

You can see that the keyboard shortcut is `ctrl and o` or `cmd and o` for mac

## Running a Python File

Can be done in many ways. The easiest is from the **Run** menu:

{{< figure src="courses/350/vscode-run-file.png" width="60%"  >}}


Output can be see in the terminal below the file editor

{{< figure src="courses/350/vscode-file-output.png" width="60%"  >}}

If you have the python extension installed for VS Code you will also see a run button on the top right of the editor when editing a python file:

{{< figure src="courses/350/vscode-play.png" width="60%"  >}}

Alternatively you can open a command line terminal and write the command to run your python file explicitly by typing:

```
> python filename.py
```
To run python in interactive mode where you type commands and directly see the result, simply open a terminal and type:

```
> python
```

This will give you the python prompt where you can start typing python commands directly into it.

## Openning a Terminal

Done from the **Terminal** menu:

{{< figure src="courses/350/vscode-terminal.png" width="60%"  >}}

Once the terminal is opened, you can perform many tasks there by typing in commands. See the [section on terminal]({{< ref "terminal.md" >}}) to know more about how to use it.

## Using Source Control (Git)

While Git can be used from the GitHub desktop program, there are controls from VS Code that allow you to use Git without leaving VS Code.

First, select the **Source Control** icon on the far left:

{{< figure src="courses/350/vscode-sourcecontrol.png" width="60%"  >}}

The Source Control panel will show the list of file that have changed in your project and display other useful information.

All source code controls for git will be available in this panel.

See the section on Git to learn more about source control.

## VS Code Extension

Extension allow you to add more functionality to VS Code and customize it you your liking. For example, the python extension could be added from extensions in addition to improved color themes and useful functionality that does not exist in VS Code by default.

You can explore the available extentions by selecting the **Extensions** icon on the far left:

{{< figure src="courses/350/vscode-extensions.png" width="60%"  >}}

When selected, list of installed extensions will be displayed in the left panel, in addition to the list of recommended extensions below it based on how you use VS Code.

I would encourage you to explore the available extensions as you become more experienced. Some of them would make your tasks faster. You can very easily uninstall extension that you do not like.

If you do find an interesting extension, please share it with your class.