
# Basic version control

## 1. What is version control

Version control, also known as source control or revision control, is a system that manages changes to a project's source code or files over time. It allows multiple contributors to work on a project simultaneously, and it keeps track of every modification made to the codebase. This ensures that developers can collaborate effectively, track changes, and revert to previous states if needed
Key aspects of version control include:

1. History Tracking: Version control systems (VCS) maintain a detailed history of changes made to the project. Each change is documented with information such as who made the change, when it was made, and a brief description of the modification.

2. Branching and Merging: Version control allows developers to create branches, which are separate lines of development. This is particularly useful for working on new features or bug fixes without affecting the main codebase. Branches can later be merged back into the main codebase.

3. Collaboration: Multiple developers can work on a project simultaneously without conflicts. The version control system helps manage and merge changes made by different contributors.

4. Revert to Previous States: If a mistake is made or an issue is introduced, developers can easily revert the codebase to a previous state, eliminating the need to manually undo changes.

5. Parallel Development: Version control facilitates parallel development by allowing multiple branches to exist concurrently. This is especially important in large projects with multiple contributors.

6. Conflict Resolution: When two developers make changes to the same part of a file, a conflict can occur during merging. Version control systems provide tools to resolve such conflicts by manually choosing which changes to keep.

## 2. Explain difference between git and github

**Git:**

1. It's a tool that manages and tracks changes in source code during software development

2. Git was created by Linus Torvalds, the same individual who created the Linux operating system.

3. Git handles version control tasks such as tracking changes, managing branches, and facilitating collaboration.

4. Git operates locally on a developer's machine, allowing them to work offline and commit changes to their local repository.

5. Git excels at branching, allowing developers to work on features or bug fixes in isolated branches and then merge them back into the main codebase.

6. Git is known for its speed and efficiency in managing large codebases.

7. Git is widely used across the software development industry for version control.

8. Git is primarily used through a command-line interface, although there are also graphical user interfaces available.

## **Github**

1. GitHub is a web-based platform that provides hosting for software development and version control using Git.

2. GitHub serves as a remote repository for Git repositories, allowing developers to store their code in the cloud.

3. GitHub provides tools for collaboration, including issue tracking, pull requests, and project management features.

4. GitHub facilitates the process of code review and collaboration through pull requests. Developers can propose changes to a repository, and others can review, comment, and merge these changes.

5. GitHub includes a robust issue tracking system for managing and discussing tasks, bugs, and feature requests.

6. GitHub is used for hosting both open-source and private projects.

7. GitHub fosters collaboration within development teams and enables contributions from the broader open-source community.

## 3. List 3 other github alternatives

1. GitLab
2. Bitbucket
3. Beanstalk

## 4. Explain the difference between git fetch and git pull

## **Git fetch**

The primary purpose of git fetch is to download new data from a remote repository.

It fetches changes from the remote repository but does not automatically merge them into your working branch.

If you have made local changes in your working branch, git fetch does not modify your working branch. It simply updates your remote-tracking branches (like origin/master) to reflect changes in the remote repository.

git fetch origin

## **Git pull**

The primary purpose of git pull is to fetch changes from a remote repository and merge them into the current branch.

It performs a git fetch followed by a git merge to update your working branch with the changes from the remote.

If you have made local changes, git pull will attempt to merge the remote changes with your local changes. If conflicts occur, you may need to resolve them manually.

git pull origin master

## 5. Explain in simple terms git rebase and the command for it

**Git rebase** is a Git command that helps you integrate changes from one branch into another by moving or combining a sequence of commits. It's a way to tidy up your commit history and make it look more straightforward.

For example Let's say you have a branch where you've made some commits, and in the meantime, others have made changes in the main branch. You want to bring those changes into your branch to keep things up to date.

**Merge vs. Rebase:**

With git merge, Git creates a new commit that ties together the histories of two branches. This can lead to a more complex history.
With git rebase, Git tries to move or combine the changes in your branch on top of the changes in the main branch, creating a linear history.

**Command for Rebase:**

git checkout your-branch
git pull origin main   # Make sure your branch is up to date
git rebase main

This sequence of commands switches to your branch, pulls the latest changes from the main branch, and then rebases your branch on top of the main branch.

## 6. Explain in simple terms git cherry-pick and the command for it

**git cherry-pick**
 is a Git command that allows you to pick a specific commit from one branch and apply it onto another branch. It's like saying, "I want this particular change from that branch, and I want it in my current branch.

For example Let's say you have made a fix or added a feature in one branch, and you want to bring that specific change into another branch without merging the entire branch.

**Command for Cherry-Pick:**

git checkout destination-branch

git cherry-pick commit-hash

This sequence ofgit commands switches to the destination branch and applies the changes from the specified commit.
