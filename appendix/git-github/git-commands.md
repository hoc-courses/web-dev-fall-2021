# Git Commands

![](<../../.gitbook/assets/image (63).png>)

## Git Commands - Add, Commit, Push

The following screen capture depicts the main git commands that are involved with working with a git repository without collaboration.

The commands are separated into those operate on your local repository (init, add, commit) and the push command that updates the GitHub repository with your changes.

![](https://raw.githubusercontent.com/hoc-labs/images/main/assignments-intro-9.png)

**git init** - this step occurred automatically when the GitHub repository was cloned to your local computer. It creates a private directory, named .git, that stores all the information for Git to track your repo. You only need to do this step when you create a local repository first.

**git status** - returns a list of untracked (new) and modified files and tracked files (files in the staging area ready for the next commit).

**git add** - adds any changed files to the staging area to be committed to your local repository.

**git commit -m "some message"** - commits the changed files in your staging area to a new snapshot, which is permanently available in the history of tracked changes for your repo. The git commit command takes **an additional flag, -m**, **followed by a message in quotes**, to provide a message to describe the changes associated with this commit.

**git push** - pushes any changes you have made since the last commit to the GitHub repository, thereby syncs up the GitHub repo with your local repo.\


#### Add, Commit, Push Cycle

The three steps **a**dd, **c**ommit, **p**ush, are commonly referred to as the **ACP cycle**, and can be repeated as many times as desired as you work on your project. It is good practice to push to GitHub whenever you are at a stable point, after making changes. This ensures that you can always return to that point if the need arises.

In addition, the **git status** command is used frequently to ensure that the steps in the ACP cycle are being carried out correctly.\


**ACP Walkthrough**

After adding some new files to a project, use the **git status** command to display the list of files that are not staged for the next commit.

[![](https://github.com/hoc-courses/shared-resources/raw/main/images/git-status.png)](https://github.com/hoc-courses/shared-resources/blob/main/images/git-status.png)

Use the **git add .** command to add all of the untracked files to the staging area and then repeat the **git status** command to ensure the files were added.

[![](https://github.com/hoc-courses/shared-resources/raw/main/images/git-status-after-add.png)](https://github.com/hoc-courses/shared-resources/blob/main/images/git-status-after-add.png)

Use the **git commit** command to commit the files in the staging area. This creates a snapshot of your project at this particular point in time. You can view files from a snapshot or return to a snapshot at any point in the future.

Use the **git status** command to verify the files were committed.

[![](https://github.com/hoc-courses/shared-resources/raw/main/images/git-status-after-commit.png)](https://github.com/hoc-courses/shared-resources/blob/main/images/git-status-after-commit.png)

Use the **git push** command to push your snapshot to the GitHub repo. [![](https://github.com/hoc-courses/shared-resources/raw/main/images/git-push.png)](https://github.com/hoc-courses/shared-resources/blob/main/images/git-push.png)\
\


#### Staging Area

One of the most confusing parts, when you're first learning git, is the concept of the staging area and how it relates to a commit.

Commits make up the essence of your project and allow you to track the changes that have been made to the project over time. A commit is a record of what changes you have made since the last time you made a commit.

Essentially, you make changes to your repo (for example, adding a file or modifying one) and then tell git to put those changes into a commit.

So, how do you tell git which files to put into a commit? This is where the staging area come in. When you make changes to your repo, git notices that a file has changed. But, you must add new files to the staging area (the set of files that will be included in the next commit) for them to be included in the commit.

To add a file to a commit, you first need to add it to the staging area. To do this, you use the **git add** command.

Once you've used the git add command to add all the files you want to the staging environment, you can then tell git to package them into a commit using the **git commit** command.
