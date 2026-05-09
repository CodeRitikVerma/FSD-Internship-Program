# Beginner-Friendly Git Guide

## What is Git?
Git is a version control system that helps developers:
- Track code changes
- Save project history
- Work with teams
- Restore old versions of files

Think of Git like a **save game system** for coding projects.

---

# 1. Install Git

## Windows

1. Go to: https://git-scm.com/downloads
2. Download Git for Windows
3. Run the installer
4. Keep clicking **Next**
5. Finish installation

After installation, open:
- Git Bash
- Command Prompt
- VS Code Terminal

Check installation:

```bash
git --version
```

Example output:

```bash
git version 2.49.0
```

---

## Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install git
```

Check installation:

```bash
git --version
```

---

## macOS

Install using Homebrew:

```bash
brew install git
```

Check installation:

```bash
git --version
```

---

# 2. Configure Git

Git needs your name and email.

Run:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Example:

```bash
git config --global user.name "Ritik Verma"
git config --global user.email "ritik@gmail.com"
```

Check settings:

```bash
git config --list
```

---

# 3. Create Your First Repository

A repository (repo) is your project folder managed by Git.

## Create Folder

```bash
mkdir my-first-repo
```

## Go Inside Folder

```bash
cd my-first-repo
```

## Initialize Git

```bash
git init
```

Now this folder is a Git repository.

---

# 4. Check Repository Status

```bash
git status
```

This command shows:
- New files
- Modified files
- Deleted files
- Files ready to commit

---

# 5. Create Files

```bash
echo "Hello" > abc.txt
```

Check status:

```bash
git status
```

You will see:
- `abc.txt` is untracked

---

# 6. Add Files to Git

```bash
git add abc.txt
```

Now Git is ready to save this file.

To add all files:

```bash
git add .
```

---

# 7. Make Your First Commit

A commit = snapshot/save point.

```bash
git commit -m "My first commit"
```

---

# 8. View Commit History

```bash
git log
```

You will see:
- Commit ID
- Author
- Date
- Commit message

---

# 9. See Changes in a Commit

```bash
git show <commit-id>
```

Example:

```bash
git show ad7fc9e
```

---

# 10. Create Branches

Branches let you work separately without affecting main code.

## Create Branch

```bash
git branch feature-1
```

## Switch Branch

```bash
git checkout feature-1
```

---

# 11. Check All Branches

```bash
git branch
```

Current branch has `*`.

Example:

```bash
* master
  feature-1
```

---

# 12. Add Changes in a Branch

Create file:

```bash
echo "New feature" > feature.txt
```

Add and commit:

```bash
git add feature.txt
git commit -m "Added feature file"
```

---

# 13. Merge Branches

Go back to master:

```bash
git checkout master
```

Merge branch:

```bash
git merge feature-1
```

Now master has changes from feature-1.

---

# 14. Cherry Pick

Cherry-pick copies ONE commit from another branch.

```bash
git cherry-pick <commit-id>
```

Useful when:
- You want only one change
- Not the whole branch

---

# 15. Clone a Repository

Copy a GitHub project to your computer.

```bash
git clone <repository-url>
```

Example:

```bash
git clone https://github.com/username/project.git
```

---

# 16. Pull Latest Changes

```bash
git pull
```

Downloads latest code from GitHub.

---

# 17. Push Your Changes

```bash
git push
```

Uploads your commits to GitHub.

---

# 18. Create GitHub Account

1. Go to https://github.com
2. Click **Sign Up**
3. Create your account
4. Verify your email

---

# 19. GitHub Personal Access Token (PAT)

GitHub may ask for a token instead of password.

Steps:
1. Go to GitHub Settings
2. Developer Settings
3. Personal Access Tokens
4. Generate New Token
5. Copy token safely

Use it when Git asks for password.

---

# 20. SSH Key Setup (Recommended)

SSH allows password-free GitHub access.

## Generate SSH Key

```bash
ssh-keygen
```

Press Enter multiple times.

## Copy Public Key

```bash
cat ~/.ssh/id_rsa.pub
```

## Add Key to GitHub

1. Open GitHub
2. Go to Settings
3. SSH and GPG Keys
4. Click New SSH Key
5. Paste copied key

Now this works without password:

```bash
git pull
```

---

# 21. Reset Changes

## Remove All Local Changes

```bash
git reset --hard
```

⚠️ Warning:
This deletes uncommitted changes.

---

# 22. Interactive Rebase (Advanced)

Used to:
- Edit commits
- Remove commits
- Rename commits

Example:

```bash
git rebase -i HEAD~3
```

This opens editor for last 3 commits.

---

# 23. Most Common Git Commands

| Task | Command |
|---|---|
| Check version | `git --version` |
| Initialize repo | `git init` |
| Check status | `git status` |
| Add file | `git add file.txt` |
| Add all files | `git add .` |
| Commit | `git commit -m "message"` |
| View history | `git log` |
| Create branch | `git branch branch-name` |
| Switch branch | `git checkout branch-name` |
| Merge branch | `git merge branch-name` |
| Clone repo | `git clone url` |
| Pull changes | `git pull` |
| Push changes | `git push` |

---

# Simple Git Workflow

```bash
git status
git add .
git commit -m "Your message"
git push
```

---

# Easy Understanding of Git Concepts

| Concept | Meaning |
|---|---|
| Repository | Project folder |
| Commit | Save point |
| Branch | Separate workspace |
| Merge | Combine branches |
| Clone | Copy project |
| Pull | Download latest code |
| Push | Upload code |
| Cherry-pick | Copy one commit |
| Rebase | Rewrite history |

---

# Recommended Beginner Practice

Create a practice repo and try:
1. Create files
2. Commit changes
3. Create branches
4. Merge branches
5. Push to GitHub

This is the fastest way to learn Git.
