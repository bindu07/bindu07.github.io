---
layout: post
title: "Top Git commands for everyday GitHub user"
description: Essential Git commands for every programmer
---

Git is the open source distributed version control system that facilitates GitHub activities on your laptop or desktop. This cheat sheet summarizes commonly used Git command line instructions for quick reference.
<br>

# Configure tooling

Configure user information for all local repositories

$ git config --global user.name "[name]"
Sets the name you want attached to your commit transactions

$ git config --global user.email "[email address]"
Sets the email you want attached to your commit transactions

![configUserName](/assets/img/gitblog2.png)

<center>Functional Component</center>

# GIT CheatSheet

## Create repositories

When starting out with a new repository, you only need to do it once, either locally, then push to GitHub, or by cloning an existing repositoryr remotely.

#### git init <directory>

Create empty Git repo in specified directory. Run with no arguments to initialize the current directory as a git repository.

#### git clone <repo>

Clone repo located at <repo> onto local machine. Original repo can be located on the local filesystem or on a remote machine via HTTP or SSH

<!-- ![classComponent](/assets/img/classComponent.png) -->

## Branches in Git

Branches are an important part of working with Git. Any commits you make will be made on the branch you're currently “checked out” to. Use git status to see which branch that is.

#### git branch [branch-name]

Creates a new branch

#### git branch -a

lists all the branches in the local and remote repository

#### git checkout [branch-name]

Switches to the specified branch and updates the working directory

#### git merge [branch]

Combines the specified branch’s history into the current branch. This is usually done in pull requests,but is an important Git operation.

#### git branch -d [branch-name]

Deletes the specified branch

## Synchronize changes

Synchronize your local repository with the remote repository on GitHub.com(any Source Control)

#### git fetch

Downloads all history from the remote tracking branches

#### git merge

Combines remote tracking branch into current local branch

#### git fetch

Downloads all history from the remote tracking branches

#### git push

Uploads all local branch commits to GitHub

#### git pull

Updates your current local working branch with all new commits from the corresponding remote branch on GitHub.
git pull is a combination of git fetch and git merge

## Make changes

Browse and inspect the evolution of project files

#### git log

Lists version history for the current branch

#### git status

Shows the staged changes in the current repository

#### git diff [first-branch]...[second-branch]

Shows content differences between two branches

#### git show [commit]

Outputs metadata and content changes of the specified commit

#### git add [file]

Snapshots the file in preparation for versioning

#### git commit -m "[descriptive message]"

Records file snapshots permanently in version history

## Redo commits

Erase mistakes and craft replacement history

#### git reset [commit]

Undoes all commits after [commit], preserving changes locally

# Attaching a screenshot how github works below with master and feature branch.

![classComponent](/assets/img/gitblog1.png)

# Git Terms all programmers use on daily basis

**git :** an open source, distributed version-control system <br>
**GitHub :** a platform for hosting and collaborating on Git repositories <br>
**commit :** a Git object, a snapshot of your entire repository compressed into a SHA <br>
**branch :** a lightweight movable pointer to a commit<br>
**clone :** a local version of a repository, including all commits and branches<br>
**remote :** a common repository on GitHub that all team member use to exchange their changes<br>
**fork :** a copy of a repository on GitHub owned by a different user<br>
**pull request(PR) :** a place to compare and discuss the differences introduced on a branch with reviews, comments,integrated tests. <br>
**HEAD :** representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits when using git checkout<br>
