# 🔧 Git Basics Notes

---
## 🟡 `git init`
- `git init` initializes a new Git repository in your project folder.
- It creates a hidden `.git` directory where Git stores all the metadata and version history of the project.
- Use it when starting a new project that isn’t already under version control.
- You only run it **once per project** (unless you remove `.git`).
  
```bash
git init
```

- After running `git init`, your folder becomes a Git repository.
- You can now start tracking changes to files in the project.

---
## 🟡 `git clone`
- `git clone` is used to create a **local copy** of a remote repository (like one from GitHub).
- It downloads the full repository history so you can work with it locally.
- Commonly used to contribute to other projects or work with collaborators.

```bash
git clone <repository-url>
```

- Example:

```bash
git clone https://github.com/username/project.git
```

- It automatically creates a new folder named after the repo and sets the `origin` remote to the URL you cloned from.

---

## 🟡 `git status`
- Shows the current state of your working directory and staging area.
- It tells you which files are:
  - Untracked (new files)
  - Modified but not staged
  - Staged but not committed

```bash
git status
```

- Use this frequently to understand what's happening before committing.
- Very helpful in debugging issues related to what is staged vs what isn’t.
---

## 🟡 `git add`
- Adds file changes to the **staging area**.
- This is the step before committing.
- You can stage specific files, folders, or all changes.

```bash
git add <filename>      # Adds a specific file
git add .               # Adds all changes in the current directory
git add -A              # Adds all changes including deletions
```

- Use `git add` to tell Git *“Hey, I want to include this file in the next commit.”*
---
## 🟡 `git commit`

- Takes the staged changes and **records them** in the repository history.
- Commits are like save points in your project.
- Always include a **commit message** to describe what was changed.

```bash
git commit -m "Your commit message"
```

- The message should be **clear and meaningful** (see best practices below).
- If you run `git commit` without `-m`, Git will open a text editor for you to write a message.

---


# 📝 Commit Message Best Practices
A good commit message helps you and others understand what changes have been made and why. Here are some guidelines:

## ✅ Structure:
```plaintext
<type>: <short summary>

<optional longer description>
```

## ✅ Examples of Types:

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Changes to documentation
- `style`: Code style/formatting (white-space, formatting, etc)
- `refactor`: Code changes that neither fix a bug nor add a feature
- `test`: Adding or updating tests

## ✅ Good Examples:

```bash
git commit -m "feat: add user login functionality"
git commit -m "fix: resolve crash on null user input"
git commit -m "docs: update README with setup instructions"
git commit -m "style: format code using Prettier"
```

## ❌ Bad Examples:

```bash
git commit -m "update"
git commit -m "fix stuff"
git commit -m "done"
```
These are unclear and unhelpful for team collaboration or tracking project history.
     
## ✨ Tips:
- Use the imperative mood: `Add`, `Fix`, `Update` (not `Added`, `Fixed`)
- Keep the first line under 50 characters
- Add a blank line between the summary and description (if writing a longer message)
- Explain the *why*, not just the *what*, especially in the long description