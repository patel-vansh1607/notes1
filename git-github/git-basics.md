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