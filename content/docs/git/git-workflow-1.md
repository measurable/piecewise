---
title: "git workflow (1): basic"
date: 2019-11-01T20:25:28+09:00
categories:
    - generic
tags:
    - generic
keywords:
inspired: https://backlog.com/git-tutorial/git-workflow/
motivation: ""
draft: true
---

## Intro: [git workflow](https://backlog.com/git-tutorial/git-workflow/)

There are three main components of a Git project:

- 저장소 (repository)
- 작업공간 (workspace 또는 working tree)
- 스테이지 (stage 또는 index)

The **repository**, or **repo**, is the "container" that tracks the changes to your project files. It holds all the commits---a snapshot of all your files at a point in time---that have been made. You can access the commit history with t`git log`.

The **working tree**, or **working directory**, consists of files that you are currently working on. You can think of a working tree as a file system where you can view and modify files.

The **index**, or **staging area**, is where commits are prepared. The index compares the files in the working tree to the files in the repo. When you make a change in the working tree, the index marks the file as modified before it is committed.

<img width="96%" alt="" src="../figures/git_workflow_001.png" class="center">

Below is the basic Git workflow:

1. Modify files in the working tree.
2. Stage the changes you want to be included in the next commit.
3. Commit changes. Committing will take the files from the index and store them as a snapshot in the repository.

### Three states of Git files

As you can probably guess from the git workflow, files can be in one of three states:

- modified
- staged
- committed

When a file is first modified, the change can only be found in the working tree. You must stage the changes you want to be included in your next commit. *The index contains all file changes that will be committed*. Once you have finished staging files, commit them with a message describing what you changed. The modified files are now safely stored in the repo.

<img width="96%" alt="" src="../figures/git_workflow_002.png" class="center">

## 1. [Creating a repository](https://backlog.com/git-tutorial/creating-a-repository/)

After installing Git on your machine, the first thing you'll need to do is set up a repository.
Once you create a Git repository with your files and directories, you can start tracking changes and versions.

### Remote repositories and local repositories

There are two types of Git repositories: remote and local.

- A *remote* repository is hosted on a remote, or off--site, server that is shared among multiple team members.
- A *local* repository is hosted on a local machine for an individual user.

While you can take advantage of Git version control features with a local repository, collaboration features---like pulling and pushing code changes with teammates---will be better suited on a remote repository.

<figure class="center">
    <img width="96%" alt="" src="../figures/creating_a_repository_001.png">
    <figcaption>
        <span class="pretag">Git remote and local repositories working in harmony.</span>
    </figcaption>
</figure>

### How to create a repository

There are two ways to create a local repository on your machine. You can create a new repository from scratch using a file folder on your computer or clone an existing repository.

#### `git init`
You can create a new repo from scratch using the `git init` command. It can be used to introduce Git into an existing, unversioned project in order to start tracking changes.

#### `git clone`
Use the `git clone` command to copy a remote repository onto your local machine.

By default, `git clone` automatically sets up a local master branch that tracks the remote master branch it was cloned from.

A cloned repository has the same history log as the original one. You can refer and backtrack to any of those commits within your local repository.

## 2. [Recording changes](https://backlog.com/git-tutorial/recording-changes/)

Now that you understand how to create a git repository, you'll need to know how to save file changes.

It is important to note that Git does not automatically save every change you make. *You must tell Git which changes you want to be recorded by staging those changes*. After staging, you can commit the changes so that they are recorded in the repo.

### Making changes

As we mentioned in the Git workflow section, changes are made in the working tree---a directory consisting of the files you are currently working on. The working tree is where you edit files, add new files, and remove files that are no longer needed.

All files that are changed in the working tree are noted as modified in the index. An index is a staging area where new commits are prepared. It sits between the repository and working tree.

Changes made in the working tree will not be saved directly to the repository. All changes must first be staged in the index in order to be saved in the repo. Only the files in the index are committed to the repo.

### `git commit`

The `git commit` command enables you to record file changes in the repository's Git history.

*By committing, you will be able to view all changes chronologically in the respective file or directory*.

<figure class="center">
    <img width="96%" alt="" src="../figures/recording_changes_001.png">
    <figcaption>
        <span class="pretag">The commit history is stored in the local repository.</span>
    </figcaption>
</figure>

A 40--character checksum hash is used to uniquely identify a commit. You can use this checksum hash to retrieve the status or changes of files and directories that were made on the given commit in your repository.

<em class="strongkorean">TIP: </em>
<em class="emkorean">
Separating different types of changes such as bug fixes, new features, and improvements into different sets of commits will allow you and your team members to easily understand why and how those changes were made.
</em>

When committing your changes, you are required to enter a commit message. The commit message should provide descriptive comments regarding the changes you have made.

<em class="strongkorean">TIP: </em>
<em class="emkorean">
Write commit messages that are descriptive and easy to understand for all your team members. The following is a recommended structure for an effective Git commit message:
</em>

```
1st line: Abstract of the contents changed by commits
2nd line: Blank line
3rd line and the following lines: Reason for changes
```

## [Undoing changes](https://backlog.com/git-tutorial/undoing-changes/)

One of the most valuable features of Git is the ability to undo mistakes. When you make a new commit, Git stores a snapshot of your project so that you can go back to an earlier version when you need to.

There are two ways to undo changes: `git revert` and `git reset`.

### `git revert`

You can use the `git revert` command to safely undo a commit that has already been pushed.

While you can also delete a previous commit from the history using `git reset` or `git rebase -i`, it is generally not a good idea because it causes the remote repository to become desynchronized with the local repositories of other members.

<figure class="center">
    <img width="96%" alt="" src="../figures/undoing_changes_001.png">
    <figcaption>
        <span class="pretag">git revert is the safest method of undoing changes.</span>
    </figcaption>
</figure>

### `git reset`

You can discard commits that you no longer need using the `git reset` command. You can specify the scope for the reset command by going into reset mode.

<figure class="center">
    <img width="96%" alt="" src="../figures/undoing_changes_002.png">
    <figcaption>
        <span class="pretag">Use git reset to remove unnecessary commits.</span>
    </figcaption>
</figure>

There are three primary reset modes:

- Mixed (default)
- Soft
- Hard

Mixed mode restores the state of a changed index. Soft mode undoes a previous commit. Hard mode removes all traces of a commit. Below is a breakdown of each reset mode.

<figure class="center">
    <img width="96%" alt="" src="../figures/undoing_changes_003.png">
    <figcaption>
        <span class="pretag">There are three reset modes: soft, mixed, and hard.</span>
    </figcaption>
</figure>


## [Rewriting history](https://backlog.com/git-tutorial/rewriting-history/)

- `git commmit --amend`
- `git rebase`
- `git cherry pick`
- `git merge --squash`

There are times when you need to revise your local commit history. This can include anything from changing your commit message to changing the order of your commits to squashing commits together. In this section, we'll discuss how to rewrite history before sharing your work with others.

### `git commit --amend`

You can modify the *most recent commit* in the same branch by running `git commit --amend`. This command is convenient for adding new or updated files to the previous commit. It is also a simple way to edit or add comments to the previous commit.

<figure class="center">
    <img width="96%" alt="" src="../figures/rewriting_history_001.png">
    <figcaption>
        <span class="pretag">
Use git commit --amend to modify the most recent commit.
        </span>
    </figcaption>
</figure>

### `git rebase`

Rebasing is the process of taking all the changes that were committed on one branch and applying them to a new branch.

Run `git rebase` and add in the `-i` option to rewrite, replace, delete, and merge individual commits in the history. You can also:

- Rewrite a past commit message
- Squash a group of commits together
- Add files that have not been committed

<figure class="center">
    <img width="96%" alt="" src="../figures/rewriting_history_002.png">
    <figcaption>
        <span class="pretag">
Rewriting the commit: Identify the commit you want to rewrite and run the git rebase -i command.
        </span>
    </figcaption>
</figure>

<figure class="center">
    <img width="96%" alt="" src="../figures/rewriting_history_003.png">
    <figcaption>
        <span class="pretag">
Combine commits.
        </span>
    </figcaption>
</figure>

### `git cherry-pick`

You can apply an existing commit from another branch to the current branch within the repository by using the `git cherry-pick` command. Cherry-picking allows you to:

- Move a commit that was committed to the wrong branch to the right branch.
- Add a commit to the current branch based on an existing commit from another branch.

<figure class="center">
    <img width="96%" alt="" src="../figures/rewriting_history_004.png">
    <figcaption>
        <span class="pretag">
        </span>
Take a commit away: Use git cherry-pick to change the branch of a commit.
    </figcaption>
</figure>

### `git merge --squash`

Squashing is the process of merging multiple commits into a single commit.

If you run `git merge` and the `--squash` option, a new commit will group all of the commits from that branch together. The commit will be used to merge into the current branch.

<figure class="center">
    <img width="96%" alt="" src="../figures/rewriting_history_005.png">
    <figcaption>
        <span class="pretag">
Use git merge --squash to unifying commits from a feature/topic branch into a single commit to be merged into your current branch.
        </span>
    </figcaption>
</figure>

## [Syncing repositories](https://backlog.com/git-tutorial/syncing-repositories/)

You'll need to be able to sync your local repository with the remote repository frequently. You'll do this using three commands: `git push`, `git pull`, and `git merge`.

### `git push`

In order to start sharing changes with others, you have to push them to a remote repository using the `git push` command. This will cause the remote repository to update and synchronize with your local repository.

<figure class="center">
    <img width="96%" alt="" src="../figures/syncing_repositories_001.png">
    <figcaption>
        <span class="pretag">Push your local changes to a remote repository.</span>
    </figcaption>
</figure>

### `Git pull`

Whenever somebody pushes their changes to the shared remote repository, your local repository becomes out of date. To re--synchronize your local repository with the newly updated remote repository, simply run the `git pull` operation.

When the `git pull` is executed, the latest revision history will download from the remote repository and import to your local repository.


<figure class="center">
    <img width="96%" alt="" src="../figures/syncing_repositories_002.png">
    <figcaption>
        <span class="pretag">Pull changes from a remote repository to your local repository.</span>
    </figcaption>
</figure>

### `git merge`

Your push to the remote repository will be rejected if your local repository is out of date, possibly because there are some updates on the remote repository that you do not have locally yet.


<figure class="center">
    <img width="96%" alt="" src="../figures/syncing_repositories_003.png">
    <figcaption>
        <span class="pretag">You are unable to push to the remote repository if your local repo is out of date.</span>
    </figcaption>
</figure>

If that is the case, you'll have to use the `git merge` command to grab the latest change from the remote repository before you are allowed to push. Git enforces this to ensure that changes made by other members get retained in the history.

<figure class="center">
    <img width="96%" alt="" src="../figures/syncing_repositories_004.png">
    <figcaption>
        <span class="pretag">You must merge the latest changes before pushing.</span>
    </figcaption>
</figure>

During a "merge", Git will attempt to automatically apply those history changes and merge them with the current branch. However, if there is a conflict in changes, Git will throw an error prompting you to resolve the conflict manually.

### Resolve merge conflicts

When merging two branches, you may come across a conflict that needs resolving before you can properly complete the merge. For example, when two or more members make changes on the same part of a file in the two different branches (remote and local branches in this case), Git will not be able to automatically merge them.

When this happens, Git will add some standard conflict--resolution markers to the conflicting file. The markers help you figure out which sections of the file need to be manually resolved.

<figure class="center">
    <img width="96%" alt="" src="../figures/syncing_repositories_005.png">
    <figcaption>
        <span class="pretag">Example of a conflict occurrence.</span>
    </figcaption>
</figure>

In our example, everything above "=====" is your local content, and everything below it comes from the remote branch.

You must resolve the conflicting parts as shown below before you can proceed with creating a merge commit.

<figure class="center">
    <img width="96%" alt="" src="../figures/syncing_repositories_006.png">
    <figcaption>
        <span class="pretag">Revise the commit to eliminate the conflict.</span>
    </figcaption>
</figure>

