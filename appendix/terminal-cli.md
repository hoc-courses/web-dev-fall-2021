# Terminal/CLI

#### Launching Git Bash

To launch Git Bash, open your Windows Start menu and type **Git Bash **or** **open a new **Terminal Window within VS Code**.

The shell will always display some standard information followed by a $ sign. The information before the $ sign includes your username and current directory.

You enter commands by typing the command after the $ sign and hitting the enter key.

When the shell first comes up, it will default to your home directory, which has the alias **\~**. To see where the home directory is, type the command **pwd** (present working directory).

#### CLI - What is a Command?

A command is how you execute a program that performs a specific operation. Many of the CLI's built-in commands focus on working with files and directories, such as the operations that you are used to doing through the Graphical UI for exploring your file system.

When you install certain applications, they may also install programs that can be executed as commands from the CLI. For example, git, the version control system that we installed, has a large number of commands for working with your git repository. We will learn about those in the next section.

**Command Syntax**

The basic syntax of a command: **command-name** \[arguments] \[flags]

**Some commands have no arguments.** You just type the name of the command.

| command   | purpose                    |
| --------- | -------------------------- |
| **pwd**   | present working directory  |
| **ls**    | list contents of directory |
| **clear** | clears the CLI window log  |

**Some commands take one or more arguments.** You type in the name of the command followed by some more information to provide more information to the command.

| command                                  | purpose            |
| ---------------------------------------- | ------------------ |
| **cd** \<directory name>                 | change directory   |
| **mkdir** \<directory name>              | create a directory |
| **touch** \<file name>                   | create a file      |
| **mv** \<old file name> \<new file name> | rename file        |

**Some commands require additional information, that is passed in with flags**, such as rm -r \<directory> (the -r means remove recursively, or all the way down). You can look up the commands to see how each operates in the cheat sheet included in the resource section below.

| command                   | purpose                                  |
| ------------------------- | ---------------------------------------- |
| rm -r \<directory name>   | removed the entire directory tree        |
| ls -l                     | lists contents of directory with details |
| git commit -m"\<message>" | passes a message to the command          |

As you work with the commands, you will learn the rules for how each one works.

#### Useful Commands

| Command                         | Description                                                                |
| ------------------------------- | -------------------------------------------------------------------------- |
| up/down arrows                  | allows you to cycle through previous commands to load and repeat commands. |
| clear                           | clears the terminal window                                                 |
| pwd                             | present working directory                                                  |
| ls                              | List files in the directory                                                |
| ls -a                           | List files in the directory (include hidden files)                         |
| cd \<directory>                 | change the directory                                                       |
| touch \<file>                   | Create an empty file                                                       |
| echo "something" > \<file>      | redirect the output of echo and create a file                              |
| echo "another thing" >> \<file> | append a string to the file                                                |
| mkdir \<directory>              | make a new directory                                                       |
| cd -                            | previous directory                                                         |
| cd ..                           | parent directory                                                           |
| cd /                            | change to the root directory                                               |
| cat \<file>                     | concatenate the file line by line and display it on the terminal           |
| mv \<file>                      | renames the file                                                           |

Resources

* [Learn the Command Line in Terminal](https://openclassrooms.com/en/courses/4614926-learn-the-command-line-in-terminal?status=published)
* [Linux Command Line Cheat Sheet](https://cheatography.com/davechild/cheat-sheets/linux-command-line/).
