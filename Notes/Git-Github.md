
# What is Git?

Git is a tool that remembers every change I make to my code on **my computer**.

If I make a mistake, I can always go back to an older version.Think of it like **"Save Game"** in a video game.

# What is GitHub?

GitHub is a website where I upload my Git projects.

It helps me: 
- Back up my code online 
- Access it from anywhere 
- Share it with other people 
- Work with a team

# Git = Works on my laptop
# GitHub = Stores my project online


# What is a Commit?

A commit is simply a **saved checkpoint** of my project. Every commit should have a short message explaining what I changed.

Example:

`Added login page`

instead of

`Update`


# First-Time Setup


Used to set my Git username.
``` bash
git config --global user.name "Your Name"
```

Used to set my Git email.
``` bash
git config --global user.email "you@example.com"
```

Used to check if everything is set correctly.
``` bash
git config --list
```

# How Git Works

Whenever I work on a project, I follow this flow:

┌─────────────────────────┐
│ Write / Edit Code       │
└─────────────┬───────────┘
              ▼
┌─────────────────────────┐
│ git add                 │
│ Stage Changes           │
└─────────────┬───────────┘
              ▼
┌─────────────────────────┐
│ git commit              │
│ Save Changes            │
└─────────────┬───────────┘
              ▼
┌─────────────────────────┐
│ git push                │
│ Upload to GitHub        │
└─────────────────────────┘

### 1. Edit

I write or change my code. Nothing is saved in Git yet.

### 2. Stage

Used to tell Git "I want this file in my next commit." 

Used to stage/add every changed file.
``` bash
git add filename
```
Or

``` bash
git add .
```

### 3. Commit


Used to save my staged changes.

``` bash
git commit -m "Added ...."
```

### 4. Push

Used to upload my commits/changes to GitHub.

``` bash
git push
```

# Commands I Will Use Every Day

``` bash
  `git status`                #Check what has changed.
  `git add .`                 #Stage/add all changed files.
  `git add filename`          #Stage/add one file.
  `git commit -m "message"`   #Save the changes.
  `git push`                  #Upload changes to GitHub.
  `git pull`                  #Download and merge changes from GitHub.
  `git fetch`                 #Download changes without merging.
  `git diff`                  #See exactly what changed.
  `git log`                   #View previous commits.
```

# Starting a Repository

## If the project is already on GitHub: 

Used to download the project.

``` bash
git clone <repository-url>
```

## If I created the project on my computer:

Create a Git repository.

``` bash
git init
```
Stage/add all files.

``` bash
git add .
```

Save the project.

``` bash
git commit -m "Initial commit"
```

Connect the project to GitHub.

``` bash
git remote add origin <repository-url>
```

Rename the main branch.

``` bash
git branch -M main
```


Upload it for the first time.

``` bash
git push -u origin main
```
See which GitHub repository my project is connected to.

``` bash
git remote -v
```



# Branches

A branch is another copy of my project where I can try new ideas safely.

Create and switch to a new branch.

``` bash
git checkout -b feature-name
```

Go back to the main branch.

``` bash
git checkout main
```



If my changes work, I merge them. 
If they don't, my main project is still safe.


# Merge

A merge combines changes from one branch into another.

Sometimes Git cannot decide which version to keep. This is called a **merge conflict**, and I have to fix it manually.


# Undo Mistakes

``` bash
  `git restore file`               #Undo changes before staging.

  `git reset file`                 #Remove a file from staging.

  `git reset <commit>`             #Go back to an older commit but keep file changes.

  `git reset --hard <commit>`      #Go back and delete all later changes.

  `git revert <commit>`            #Undo a commit safely by creating another commit.
```


# Git Stash

If I'm not finished but need to switch branches:

Save my unfinished work temporarily.

``` bash
git stash
```

Bring the changes back and remove them from the stash.

``` bash
git stash pop
```

Bring the changes back but keep another copy in the stash.

``` bash
git stash apply
```




# Fork and Pull Request

A **Fork** is my own copy of someone else's repository.

A **Pull Request (PR)** is asking the owner to review and merge my
changes. It's better to make one useful PR than many random ones.


# Extra Commands

``` bash
  `git rm file`                    #Delete a file and stage the deletion.

  `git rm --cached file`           #Stop tracking a file but keep it on my computer.
```


# My Everyday Git Workflow

```bash
git status
git add .
git commit -m "what I changed"
git push
```

This is the workflow I will use almost every day. The other commands are for special situations.
