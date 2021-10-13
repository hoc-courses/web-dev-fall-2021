# GitHub Classroom Intro

We are going to be using **GitHub Classroom** to manage homework assignments. It simplifies the task of distributing/collecting assignments.

It will also give you lots of experience using **git** and **GitHub**, which are very useful skills, both for personal use, and one that employers require of new hires.

## Overview

GitHub Classroom allows instructors to create a set of repositories that are templates for assignments that they can then assign to students. For each assignment, GitHub Classroom will make a special URL link and the instructor will share it with the students in the class.

When the student enters the link in a browser, GitHub will create a private repository, with a name that includes both the assignment name and the student's GitHub username. For example, _assignment-1-username_.

**The assignment repository is created within the GitHub Classroom account for the class, not the student's private GitHub account.** This simplifies the workflow for working on assignments. Both the instructor and the student have access to the assignment repository.

### Starting the Assignment

1. instructor provides students with a link to start the assignment.
2. each student pastes the URL in the browser
3. a new assignment repo is created for each student in the GitHub Classroom account
4. students [**clones their assignment repository**](cloning-from-an-existing-github-repo.md) to their local computer

### Working on the Assignment

1. student do some work
2. student adds **(git add .)** files if necessary
3. student commits **(git commit -m\[comment])** their changes
4. student pushes **(git push)** the changes back to your remote repo on GitHub
5. you do some more work
6. return to step 2, if necessary

### Turning in Your Assignment

There is no special step necessary to turn in your assignment. Your instructor has access to the repository and can see when your last push took place.

Once the assignment due date has passed, the instructor will review your work on GitHub, or clone the repository to their local computer so they can review and give feedback.

{% hint style="info" %}
If you have forgotten the URL for the GitHub assignment repo, you can just paste in the assignment URL again and it will take you to the GitHub assignment repo page.
{% endhint %}
