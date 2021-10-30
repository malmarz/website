---
# Page title
title: Introduction to Terminal

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: Terminal

# Date page published
date: 2021-03-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 2

draft: False
---

The terminal is used to issue commands to the computer, like running a python file or running a Django server. Therefore it is important for you to get familiar with it. The terminal is not a feature of Python, it is part of the operating system. The mac terminal will be different from the Windows terminal slightly. It is a different method to working with files and programs on your computer from the Graphical Interface. You will likely have seen how we have deminstrated that you can run programs and create directories using the the mouse point and click system (known as the graphical interface) or the terminal.

Anything you can do with on Windows/Mac/Linux using the Mouse and Graphical Interface, you can also do with the terminal. Programers prefer the terminal because it is more effecient and flexibile. Because they get into the habit of typing code, it becomes easier to work with the operating system by also performing commands by typing them instead of looking for the appropriate button or icon to click on with your mouse.

## Alternative Names for Terminal

You will come across different names for the terminal, these include:

- The command line
- The command prompt
- The Shell
- The terminal
- The command line shell

When reading references on the internet, keep in mind that these terms can be used interchangeable as they mean the same thing.

## The Python Shell vs Command Line Shell

You must be a ware of the difference between the python shell and the command line shell. The python shell will accept only python code. You start it by typing `python` in the command line shell. You can tell the python shell is running if you see the following prompt:

```bash
>>>
```

When working with the command line shell, you will see the **current working directory** if you are using windows:

```bash
C:\users\username>
```

On macs/linus you will see the host name:
```bash
username>
```

To master the command line, you must first understand the concept of file paths as how commands will be performed is built on this idea.

## File Paths

File path is a concepts that allows us to identify a file/program/directory in the file system. File paths on windows systems look like this:

```bash
C:\users\myname\dir1\filename
```

We read the file name from left to right. The path is separated into parts using the **back slash \\** on windows system. Each part is a step we take in the file system until we reach the file, program, or directory that we need.

This is what each part means in our previous example:
- `C:`: This means that our file, program, or directory is in the C drive. Windows uses alphabit letters to give drives names. A flash drive might get the letter **E:** for example.
- `users` is the name of the directory found at the top of the **C:** drive.
- `myname`: is the name of the directory inside the **users** directory that will contain our file, program, or directory that we need to work with.
- `dir1`: is another directory we are interested in contained inside **myname** directory.
- `filename`: is the file we want to work with contained in the **dir1** directory.

In other words, our file `filename` is inside the directory `dir1`, which is inside another directory called `myname`, which is inside another directory called `users`, which is a directory found in the `C:` drive.

### File paths in Mac and Linux systems

File paths on Mac and Linux systems are almost identical to Windows systems. The only differences that you need to keep in mind are:
1. There are no drive letters, paths always start with the root directory `/`
2. The parts of a path are seperated with **forward slash /** instead of a backward slash \\ like windows.
3. Paths are **case sensistive**, the file myfile is different from MyFile and different from MYFILE. On windows, the letter case do not matter.

## Important Commands

Always keep in mind, when issuing commands in terminal, they are **ALWAYS** performed in the working directory. The workind directory is shown on windows in the prompt, which is the path shown to the left of the **>** character:

```bash
C:\users\username>
```

On mac and linux use the command `pwd` to display the working path.

Another important thing to keep in mind, the commands will will present here work for Mac, Linux, and Windows powershell. Windows power shell is used when you open a terminal on VS Code on windows. Keep in mind that these commands might not work if you use the *CMD* windows command prompt.

Some commands will require that you provide them with a file to perform the command on. Either ensure that you are in the same working directory as the file you want to perform the command on or provide the full path to the file.

Here is the list of important commands that you will need in this course:

To move to dir2 inside dir1 inside the current working directory use:
```bash
> cd dir1\dir2
```
{{% callout note %}}

For Mac/Linux systemes, replace `\` with `/` in the path.

{{% /callout %}}
You can specify as many directories in the path or just a single directory. For example:

```bash
> cd dir1\dir2\dir3
```
 or 

 ```bash
> cd dir1
```



To know what the current working directory is, use:
```bash
> pwd
```

To move one level up in the current working directory, which is the directory containing the current directory use:
```bash
> cd ..
```

To move directly to the home directory use:
```bash
> cd ~
```
To List files in the current working directory use:
```bash
> ls
```

To create a new directory in current working directory:
```bash
> mkdir dirname
```

Where `dirname` is the name of the new directory. Replace it with whatever name you want. I would recommend not using spacing.

To clear the terminal output:
```bash
> cls
```

To start a python interpreter:
```bash
> python
```

To run a python script:
```bash
> python path/to/script.py
```

Replace `path/to/script.py` with the actual path and file name of the python file you want to run.

## Important Tips

- Use up/down arrows in your keyboard to cycle through previous commands you have run instead of retyping them.
- When typing a command or path, hit the tab button for auto completion or to give suggestion on the available options. Learn to use tab as it will make using the terminal quicker for you.
