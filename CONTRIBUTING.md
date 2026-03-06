# Contributing to Kittens Index

Welcome! This guide walks you through the full GitHub workflow used in this exercise.

---

## Workflow Overview

```
GitHub (remote)
     │
     │  git clone (one-time setup)
     ▼
Your Computer (local)
     │
     │  edit files
     │  git add
     │  git commit
     │  git push
     ▼
GitHub (remote) ← your changes are now live!
```

---

## Detailed Steps

### 1. Fork (optional for shared repos)

If you do not have write access to the original repo, **fork** it first:

- Click **Fork** in the top-right corner of the GitHub page.
- This creates your own copy at `github.com/<your-username>/kittens_index`.

### 2. Clone via SSH

```bash
# Replace <your-username> with your GitHub username if you forked,
# or use the original repo URL if you have direct access.
git clone git@github.com:<your-username>/kittens_index.git
cd kittens_index
```

### 3. Create a Branch (best practice)

Working on a branch keeps `main` clean:

```bash
git checkout -b add-my-kitten
```

### 4. Edit `kittens.md`

Open the file and add your kitten row as described in that file.

### 5. Stage and Commit

```bash
# Check which files changed
git status

# Stage the changed file
git add kittens.md

# Commit with a clear message
git commit -m "Add <kitten-name> to the index"
```

### 6. Push Your Branch

```bash
git push origin add-my-kitten
```

### 7. Open a Pull Request (if you forked)

- Go to your forked repo on GitHub.
- Click **Compare & pull request**.
- Add a short description and submit.

### 8. Pull Updates from the Remote

Before starting a new session, always sync with the remote:

```bash
# Switch back to main first
git checkout main

# Fetch and merge changes from the remote
git pull origin main
```

---

## Common Git Commands Reference

| Command | What it does |
|---------|-------------|
| `git status` | Show changed/staged files |
| `git add <file>` | Stage a file for commit |
| `git commit -m "msg"` | Save staged changes with a message |
| `git push origin <branch>` | Upload commits to GitHub |
| `git pull origin main` | Download + merge latest changes |
| `git log --oneline` | Show recent commit history |
| `git diff` | Show unstaged changes |

---

## Troubleshooting SSH

| Problem | Fix |
|---------|-----|
| `Permission denied (publickey)` | Your SSH key is not added to GitHub — see Step 0 in README |
| `Host key verification failed` | Run `ssh-keyscan github.com >> ~/.ssh/known_hosts` |
| `remote: Repository not found` | Check the remote URL: `git remote -v` |
