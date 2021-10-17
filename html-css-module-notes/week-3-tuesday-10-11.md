# Week 3: Thursday 10/13

### GitHub Use Cases

#### Single User/Non-production Code

So far we have been using GitHub to store our class work and each student has been working on their own projects.  In this scenario Git/GitHub is being used as a means of:

* backup/version control
* a place to share content (others can view/download your repo)

We're not really concerned about having a version that is always working. We're just working toward a better version over time.

In this scenario, there is little need for branching, as we can just frequently commit and push our changes to GitHub and if needed, view or even revert to an earlier version.

#### Production Ready Version

As soon as there is a need to maintain a production-ready version of the code, then the main branch becomes that version, and changes should be done in a new temporary branch and then those changes can be merged back into the main branch when they have been tested to ensure they will not break the production ready code.

When multiple developers are collaborating on a project, then an added layer of protection is added by requiring all branches to go through an approval process before their changes can be merged into the main branch. This process is called a pull request in GitHub.



### Basic Git Workflow

In all of the above scenarios, a user will be working with the source code in a branch and needs to add/modify/remove files, create snapshots of the project, and push the changes to GitHub. This video briefly reviews this workflow and the associated git commands.

[Basic Git Workflow](https://codewithmosh.com/courses/1120640/lectures/24393738)

### Branching/Merging

When branching is necessary, there are additional git commands that are necessary to work with branches and handling merge conflicts, i.e. when changes in two branches overlap.

[Git Branching](https://codewithmosh.com/courses/1120640/lectures/24394230)

[Collaboration Workflow](https://codewithmosh.com/courses/1120640/lectures/24394587)

### Practice Project

None of this will be very concrete without working with a real repository and walking through each of these steps. We're going to create a practice repository where we can learn:

* how to work in branches
* how to use pull requests
* how to resolve merge conflicts

Click on the following assignment link: [https://classroom.github.com/a/Ifm6Vn-C](https://classroom.github.com/a/Ifm6Vn-C)



### Collaborative News site

We're going to create a new site to use for the collaboration, using the typical way they are created, not as we have been through GitHub Classroom.

Jesse has created the repo in his account and added everyone as collaborators so that we can all clone and push to the repo.

Here's the link to the repo to use.

{% embed url="https://github.com/SJJCoding/Group-newssite" %}

### Step 1 - Setup the Repo for Collaboration

The first step is for one person to go to this repo and click the **Use this template  **button to copy the repo to their own account so that it can be setup with collaborators for this exercise.

Next, we want to invite everyone to be collaborators on the repo. 

Next, all the collaborators should go to the repo and clone it to their local computer.

Now, everyone has a copy of the repo on their local computer and the repo has some starter code in the main branch.

### Step 2 - Review the Site Spec and Create Issues

### Step 3 - Start Working on Issues Assigned to You



### Resources 

{% content-ref url="../appendix/git-github/github-collaboration.md" %}
[github-collaboration.md](../appendix/git-github/github-collaboration.md)
{% endcontent-ref %}

###

###

