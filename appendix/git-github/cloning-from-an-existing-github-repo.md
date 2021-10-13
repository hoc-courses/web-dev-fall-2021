# Cloning from an Existing GitHub Repo

Whenever you want to work in a repository that already exists on GitHub, the first step is to clone the repository.

Cloning a repository creates a copy of a GitHub repository on your local computer and establishes a connection between the two repositories so that they can stay in sync.

#### 1. Get the GitHub repository URL

To clone a GitHub repository, you need to first go to the GitHub repository to get the repository URL. Just click the Code button, and then click the clipboard icon to copy the URL for the repo.

[![](https://github.com/hoc-courses/shared-resources/raw/main/images/clone-copy-url.png)](https://github.com/hoc-courses/shared-resources/blob/main/images/clone-copy-url.png)

#### 2. Issue the git clone command on your local computer

There are two options for how to clone a repository.

**From the Command Line**

Before issuing the **git clone** command, make sure you are in the current directory where you want the repository folder to be created.

**Note:** The Bash Shell doesn't paste without using the right mouse button to bring up the context menu and then selecting the Paste option from the menu.

* type git clone on the command line
* use the context menu to paste in the GitHub repository URL as the second argument
* enter the command

```
git clone [paste GitHub URL here]
```

**From Visual Studio Code**

When VS Code first starts up, you are presented with a welcome screen that gives you the option of cloning a repository.

You can also use the Command Palette and search for Git Clone.\


[![](https://raw.githubusercontent.com/hoc-labs/images/main/assignments-intro-7.png)](https://raw.githubusercontent.com/hoc-labs/images/main/assignments-intro-7.png)

After you click on either of the links shown above, you will be presented with a box to paste in the assignment URL.

[![](https://raw.githubusercontent.com/hoc-labs/images/main/assignments-intro-8.png)](https://raw.githubusercontent.com/hoc-labs/images/main/assignments-intro-8.png)

This will clone the GitHub repository. It will make a local copy of the GitHub repository and set up the .git folder to track the project so that you can manage local changes and stay in sync with the GitHub repo.
