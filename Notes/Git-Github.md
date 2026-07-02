
# 1. What is Git?

Git is a **Distributed Version Control System (DVCS)** used to track changes made to files and projects.

Instead of creating multiple folders like "project-final", "project-final2", or "latest-project", Git keeps a complete history of every meaningful change.

### Key Points

- Tracks changes in a project.
- Maintains project history.
- Helps developers collaborate.
- Allows going back to previous versions.

---

# 2. Why Do We Need Git?

As projects grow, files change frequently.

Git helps me:

- Track every change.
- Undo mistakes.
- Work on new features safely.
- Collaborate with other developers.

Without Git, managing projects would become difficult.

### Key Points

- Keeps project history.
- Makes collaboration easier.
- Prevents accidental loss of work.

---

# 3. What is GitHub?

GitHub is a cloud platform where Git repositories are stored online.

It allows developers to:

- Store projects.
- Share code.
- Collaborate with others.
- Showcase their work.

### Key Points

- Stores Git repositories online.
- Makes collaboration easier.
- Used to share projects.

---

# 4. Git vs GitHub

Many beginners think Git and GitHub are the same.

They are different.

| Git | GitHub |
|------|---------|
| Software | Online Platform |
| Tracks changes | Stores repositories online |
| Works locally | Works on the Internet |

### Key Points

- Git manages the project.
- GitHub stores the project online.

---

# 5. Version Control System (VCS)

A Version Control System keeps track of changes made to files over time.

It allows me to:

- See previous versions.
- Restore old versions.
- Compare changes.
- Understand project history.

Git is a Version Control System.

---

# 6. Repository (Repo)

A Repository is the project folder managed by Git.

It contains:

- Project files.
- Git history.
- Previous commits.

Every Git project has its own repository.

---

# 7. Local Repository vs Remote Repository

### Local Repository

Stored on my computer.

I work here while developing the project.

---

### Remote Repository

Stored online.

Usually hosted on GitHub.

Used for backup and collaboration.

### Key Points

- Local = My computer.
- Remote = GitHub.

---

# 8. README.md

README.md is the first file people usually see when they open a repository.

It explains:

- What the project is.
- Features.
- Installation steps.
- Usage.
- Technologies used.

A good README helps others understand the project.

---

# 9. .gitignore

Some files should not be uploaded to GitHub.

The `.gitignore` file tells Git which files or folders should be ignored.

Examples:

- Temporary files.
- Build files.
- Log files.
- Virtual environments.
- Secret configuration files.

### Key Points

- Prevents unnecessary files from being tracked.
- Keeps repositories clean.

---

# 10. Working Directory

The Working Directory is where I make changes to my project files.

Whenever I edit a file, the changes first appear here.

---

# 11. Staging Area

The Staging Area is a temporary place where I prepare changes before saving them permanently.

Git only commits files that have been added to the staging area.

---

# 12. Commit

A Commit is a snapshot of the project at a specific point in time.

Every commit saves the changes made since the previous commit.

Think of it as a checkpoint in a game.

If something goes wrong, I can return to an earlier checkpoint.

### Key Points

- Saves project history.
- Creates a checkpoint.
- Helps restore previous versions.

---

# 13. Commit Message

A Commit Message is a short description of what changed.

Examples:

```
Initial commit

Add Day 2 notes

Fix README formatting

Update Git notes
```

A good commit message makes the project history easier to understand.

---

# 14. Branch

A Branch is a separate line of development.

It allows developers to work on new features without affecting the main project.

The default branch is usually called:

```
main
```

---

# 15. Merge

Merge combines changes from one branch into another.

For example,

A new feature is completed.

It is then merged into the main branch.

---

# 16. Clone

Clone creates a copy of a GitHub repository on my computer.

Command:

```bash
git clone <repository-url>
```

---

# 17. Push

Push uploads my local commits to GitHub.

Command:

```bash
git push
```

---

# 18. Pull

Pull downloads the latest changes from GitHub and updates my local repository.

Command:

```bash
git pull
```

---

# 19. Fetch

Fetch checks for updates from GitHub without changing my local files.

Command:

```bash
git fetch
```

Unlike `git pull`, it only downloads information.

---

# 20. Git Workflow

A typical Git workflow looks like this:

```
Working Directory

↓

git add

↓

Staging Area

↓

git commit

↓

Local Repository

↓

git push

↓

GitHub
```

---

# 21. Common Git Commands

Initialize a Git repository

```bash
git init
```

Check repository status

```bash
git status
```

Add all files

```bash
git add .
```

Create a commit

```bash
git commit -m "Commit message"
```

Upload changes to GitHub

```bash
git push
```

Download latest changes

```bash
git pull
```

View commit history

```bash
git log
```

Clone a repository

```bash
git clone <repository-url>
```

---
