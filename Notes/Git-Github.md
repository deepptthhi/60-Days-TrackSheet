

# What is Git?

Git is a tool that remembers every change I make to my code on **my
computer**.

If I make a mistake, I can always go back to an older version.Think of it like **"Save Game"** in a video game.

# What is GitHub?

GitHub is a website where I upload my Git projects.

It helps me: 
- Back up my code online 
- Access it from anywhere 
- Share it with other people 
- Work with a team


*  Git = Works on my laptop
*  GitHub = Stores my project online

# What is a Commit?

A commit is simply a **saved checkpoint** of my project.

Every commit should have a short message explaining what I changed.

Example:

`Added login page`

instead of

`Update`


# First-Time Setup

``` bash
git config --global user.name "Your Name"
```

Used to set my Git username.

``` bash
git config --global user.email "you@example.com"
```

Used to set my Git email.

``` bash
git config --list
```

Used to check if everything is set correctly.


# How Git Works

Whenever I work on a project, I follow this flow:

Edit code

↓

git add

↓

git commit

↓

git push

### 1. Edit

I write or change my code.

Nothing is saved in Git yet.

### 2. Stage

``` bash
git add filename
```

Used to tell Git:

"I want this file in my next commit."

Or

``` bash
git add .
```

Used to stage every changed file.

### 3. Commit

``` bash
git commit -m "Added navbar"
```

Used to save my staged changes.

### 4. Push

``` bash
git push
```

Used to upload my commits to GitHub.


# Commands I Will Use Every Day

  Command                     Used to...
  --------------------------- -----------------------------------------
  `git status`                Check what has changed.
  `git add .`                 Stage all changed files.
  `git add filename`          Stage one file.
  `git commit -m "message"`   Save the changes.
  `git push`                  Upload changes to GitHub.
  `git pull`                  Download and merge changes from GitHub.
  `git fetch`                 Download changes without merging.
  `git diff`                  See exactly what changed.
  `git log`                   View previous commits.

------------------------------------------------------------------------

# Starting a Repository

If the project is already on GitHub:

``` bash
git clone <repository-url>
```

Used to download the project.

If I created the project on my computer:

``` bash
git init
```

Create a Git repository.

``` bash
git add .
```

Stage all files.

``` bash
git commit -m "Initial commit"
```

Save the project.

``` bash
git remote add origin <repository-url>
```

Connect the project to GitHub.

``` bash
git branch -M main
```

Rename the main branch.

``` bash
git push -u origin main
```

Upload it for the first time.

``` bash
git remote -v
```

See which GitHub repository my project is connected to.

# Branches

A branch is another copy of my project where I can try new ideas safely.

``` bash
git checkout -b feature-name
```

Create and switch to a new branch.

``` bash
git checkout main
```

Go back to the main branch.

If my changes work, I merge them.

If they don't, my main project is still safe.


# Merge

A merge combines changes from one branch into another.

Sometimes Git cannot decide which version to keep.

This is called a **merge conflict**, and I have to fix it manually.


# Undo Mistakes

  -----------------------------------------------------------------------
  Command                          Used to...
  -------------------------------- --------------------------------------
  `git restore file`               Undo changes before staging.

  `git reset file`                 Remove a file from staging.

  `git reset <commit>`             Go back to an older commit but keep
                                   file changes.

  `git reset --hard <commit>`      Go back and delete all later changes.

  `git revert <commit>`            Undo a commit safely by creating
                                   another commit.
  -----------------------------------------------------------------------


# Git Stash

If I'm not finished but need to switch branches:

``` bash
git stash
```

Save my unfinished work temporarily.

``` bash
git stash pop
```

Bring the changes back and remove them from the stash.

``` bash
git stash apply
```

Bring the changes back but keep another copy in the stash.


# Fork and Pull Request

A **Fork** is my own copy of someone else's repository.

A **Pull Request (PR)** is asking the owner to review and merge my
changes.

It's better to make one useful PR than many random ones.


# Extra Commands

  -----------------------------------------------------------------------
  Command                          Used to...
  -------------------------------- --------------------------------------
  `git rm file`                    Delete a file and stage the deletion.

  `git rm --cached file`           Stop tracking a file but keep it on my
                                   computer.
  -----------------------------------------------------------------------


# My Everyday Git Workflow

``` text
git status
git add .
git commit -m "what I changed"
git push
```

This is the workflow I will use almost every day. The other commands are for special situations.
