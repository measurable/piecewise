---
title: "git workflow (2): branching"
date: 2019-11-01T21:00:04+09:00
categories:
    - generic
tags:
    - git
keywords:
inspired:
motivation: ""
draft: true
---

## [Using branches](https://backlog.com/git-tutorial/using-branches/)

Branching allows each developer to branch out from the original code base and isolate their work from others. It also helps Git to easily merge versions later on.

### What is a Git branch?

A Git branch is essentially an independent line of development. You can take advantage of branching when working on new features or bug fixes because it isolates your work from that of other team members.


<figure class="center">
    <img width="96%" alt="" src="../figures/using_branches_001.png">
    <figcaption>
        <span class="pretag">
A git branch is an independent line of development taken from the same source code.
        </span>
    </figcaption>
</figure>

Different branches can be merged into any one branch *as long as they belong to the same repository*.

The diagram below illustrates how development can take place in parallel using branches.

<figure class="center">
    <img width="96%" alt="" src="../figures/using_branches_002.png">
    <figcaption>
        <span class="pretag">
Multiple development projects taking place using the same source code.
        </span>
    </figcaption>
</figure>

Branching enables you to isolate your work from others. Changes in the primary branch or other branches will not affect your branch, unless you decide to pull the latest changes from those branches.

It is a common practice to create a new branch for each task (i.e., a branch for bug fixing, a branch for new features, etc.). This method allows others to easily identify what changes to expect and also makes backtracking simple.

Create a branch
Creating a new branch does not change the repository; it simply points out the commit

For example, let's create a branch called “issue1” using the command git branch.

git branch issue1
The illustration below provides a visual on what happens when the branch is created. The repository is the same, but a new pointer is added to the current commit.


<figure class="center">
    <img width="96%" alt="" src="../figures/using_branches_003.png">
    <figcaption>
        <span class="pretag">
        </span>
    </figcaption>
</figure>