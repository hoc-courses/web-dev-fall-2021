# GitHub - Collaboration

### GitHub Collaborative Development

#### Collaborators

A GitHub repository has at a minimum a single owner who created the repository within their account. That owner can add collaborators (other GitHub users) that are given access to the repository. A collaborator is allowed to clone and push changes to the repository. This is the typical set up for a software development group within a company that is working on a project. 

#### Open-source Community

Some repositories want to allow contributions from the development community outside of the collaborators. Git has a featured called forking, which is used for this purpose. 

When you fork a repo, you first go to the repo you wish to fork, click the fork button, and this creates a copy of the repo within your own account. The copy has a link back to the original repo, which enables two important features:

1. You can pull an update from the original to your copy when desired.
2. You can create and test a proposed change locally and then create a pull request to the original repository, asking to merge your changes into their repo.

Let's look at an example of an open-source project: Visual Studio Code. Take a look at the following files: README, Issues, Pull Requests, Insights, Contributors

* README
* Issues
* Pull Requests
* Insights
* Contributors

{% embed url="https://github.com/microsoft/vscode" %}



In this exercise, we're going to focus on the first scenario, where we are limiting the repository to our restricted set of collaborators.

### Software Development Workflow

All git repositories start out with a main branch. This is supposed to be "production ready", meaning that it can be deployed to the production site at any time.

How do you control the process of developers working on features and adding their changes to the production code and minimizing the introduction of bugs into production? There is not a single agreed upon solution. Over the years the solutions have evolved.

Early on, when desktop applications predominated, there was the need (which still exists) to support multiple versions of the software simultaneously. For example, multiple versions of the Chrome browser are out in the field at the same time. If there is a bug discovered in an earlier version, Google has to fix that bug in all of the versions that are currently supported in the field. They cannot say that the customer has to upgrade to the latest version to get the fix. This means that a number of long-lived branches need to be maintained and slows down the whole development process.

Web applications are different. There is only a single version at a time. This reduces the complexity, but it is still a difficult problem and there are lots of different approaches.   Many of the leading websites today have very sophisticated processes to allow them to continually incorporate changes into the live site. 

There are several techniques used to maintain production ready code in the main branch.

1. **Branching**: working in an isolated environment on features and bug fixes, until your code is ready to be incorporated into the main branch.
2. **Testing**: building and running tests continuously on your local changes, and the merge in changes to find bugs as quickly as possible. Tests are then run on the main branch to ensure that the entire code base works with all recent changes incorporated. 
3. **Paired Programming:** having developers work together on features/bugs so that there is a review process built in.
4. **Pull Requests:** requiring that a branch cannot be merged into the main branch until it has been reviewed/approved by at least one other developer.

If you have extremely good automated testing, which is somewhat rare, then you can possibly eliminate the need for branching altogether and just work in your local copy of the main branch, run the tests on your local copy, and then push your changes into the main branch on GitHub. There is a current, somewhat small, movement to support this model, as it reduces the complexity greatly, and thereby increases productivity. 

The more popular approach is the [GitHub Flow ](https://guides.github.com/introduction/flow/)workflow model. It was originated by GitHub and uses short-lived feature branches, pull requests, and continuous automated testing, in feature branches and the main branch, to be able to incorporate changes continuously into their production code.



### Working within a Branch

Git can be tricky to get beyond the basics of working in your own repo in the main branch. It's a steep learning curve and things can go wrong, as sites such as [this ](https://ohshitgit.com)demonstrate.

When working within a branch, you just need to use the few commands:

![](https://lh4.googleusercontent.com/hbDQlM2nAxO4rFA0qfWgHv7cg_ee34dzqtzVegcGz3Z9PsR1cEBThKAABelOApeniKMMf4OJ8XHYSKnAiV0D0f6n6skg5gMgulTfwGf29wxKo5Y6PlI16s9h\_2ZXMhcdm61wsDc=s0)

* **git add** . (add any changes to staging area for next commit) 
* **git commit** -m”comment” (take a snapshot of staging area) 
* **git push** (push changes to GitHub) 
* **git status** (check for current status) 
* **git log --oneline** (show history of changes with one line summary)
* **git pull** (pulls changed files (from other users) from GitHub)

### Branching

Once you need to work with branches, creating, moving between, deleting, there are a new set of git commands you have to use.

* **git branch** \[branch name] (creates a new branch) 
* **git checkout** \[branch name] (changes to branch) 
* **git checkout -b** \[branch-name] (creates a new branch and changes to it) 
* **git branch -d** \[branch-name] (deletes an up-to-date branch) 
* **git branch -D** \[branch-name] (deletes a branch even if there are uncommitted changes)

### Pull Requests

An additional part of the workflow is to create a pull request within GitHub to incorporate a review in the process of merging your branch into the main branch.

![](https://lh6.googleusercontent.com/L9sv47IIwoO7xpJt5ufQPRRN9jozkP63tASQAdvO28PVCSV3ws_dO0guPegZiBsNr4vfT1hL7G0\_ltCyA7jPyyFOOpCjGqqbMJk7wp-w4QSYLJlP9yZIUXKdJ2Piu4RkunC3ddQ=s0)



### Git/GitHub Resources

* [Git and GitHub for Poets - Intro](https://www.youtube.com/watch?v=BCQHnlnPusY\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=2)
* [Git and GitHub for Poets - Branching](https://www.youtube.com/watch?v=oPpnCh7InLY\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=2\&t=9s)
* [Git and GitHub for Poets - Issues](https://www.youtube.com/watch?v=WMykv2ZMyEQ\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=4)
* [Git and GitHub for Poets - Fork and Pull Requests](https://www.youtube.com/watch?v=\_NrSWLQsDL4\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=3)
* [Git and GitHub for Poets - Merge Conflicts](https://www.youtube.com/watch?v=JtIX3HJKwfo\&list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV\&index=10)
* [Undoing commit to wrong branch](https://www.clearvision-cm.com/blog/what-to-do-when-you-commit-to-the-wrong-git-branch/)
* [Net Ninja - Branches](https://www.youtube.com/watch?v=QV0kVNvkMxc\&list=PL4cUxeGkcC9goXbgTDQ0n\_4TBzOO0ocPR\&index=8)
* [Net Ninja - Collaborating on GitHub](https://www.youtube.com/watch?v=MnUd31TvBoU\&list=PL4cUxeGkcC9goXbgTDQ0n\_4TBzOO0ocPR\&index=12)
* [Net Ninja - Merging](https://www.youtube.com/watch?v=XX-Kct0PfFc\&list=PL4cUxeGkcC9goXbgTDQ0n\_4TBzOO0ocPR\&index=10)
* [Git Internals](https://www.youtube.com/watch?v=fWMKue-WBok\&list=PL9lx0DXCC4BNUby5H58y6s2TQVLadV8v7\&index=3)
* [Git States](https://www.youtube.com/watch?v=r8GeKo17VWE)
* [Git Cheat Sheet](https://training.github.com/downloads/github-git-cheat-sheet/)
* [Useful Commands](https://www.youtube.com/watch?v=wnYL4yUd-z0)
* [Undoing Things](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)
* [unwatch repos](https://github.com/watching)
* git help \[command]
* Undo last commit, but keep changes (accidentally checked in on master, meant to be on branch)
  * git reset --soft HEAD\~1
* [Continuous Integration/Deployment](https://resources.github.com/ci-cd/)
