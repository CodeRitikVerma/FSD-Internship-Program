# Beginner-Friendly Git Guide

## What is Git?
Git is a version control system that helps developers:
- Track code changes
- Save project history
- Work with teams
- Restore old versions of files

Think of Git like a **save game system** for coding projects.

---

# 1. Check if Git is Installed

Open Terminal and type:

```bash
git --version
```

You may also see:

```bash
g --version
```

### Why do both work?
Because `g` is usually an alias (shortcut) for `git`.

Example:

```bash
alias g='git'
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

Shortcut:

```bash
g st
```

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

---

# 7. Make Your First Commit

A commit = snapshot/save point.

```bash
git commit -m "My first commit"
```

Shortcut:

```bash
g ci -m "My first commit"
```

---

# 8. View Commit History

```bash
git log
```

You will see:
- commit ID
- author
- date
- message

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

Shortcut:

```bash
g br feature-1
```

## Switch Branch

```bash
git checkout feature-1
```

Shortcut:

```bash
g co feature-1
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
- you want only one change
- not the whole branch

---

# 15. Clone a Repository

Copy a GitHub project to your computer.

```bash
git clone <repository-url>
```

Example:

```bash
git clone git@github.com:username/project.git
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

# 18. GitHub Personal Access Token (PAT)

GitHub no longer allows password authentication in many cases.

Steps:
1. Go to GitHub Settings
2. Developer Settings
3. Personal Access Tokens
4. Generate Token
5. Copy token safely

Use it when Git asks for password.

---

# 19. SSH Key Setup (Recommended)

SSH allows password-free GitHub access.

## Generate SSH Key

```bash
ssh-keygen
```

## Copy Public Key

```bash
cat ~/.ssh/id_rsa.pub
```

## Add Key to GitHub

GitHub → Settings → SSH and GPG Keys → New SSH Key

Paste the copied key.

Now:

```bash
git pull
```

works without password.

---

# 20. Reset Changes

## Remove All Local Changes

```bash
git reset --hard
```

⚠️ Warning:
This deletes uncommitted changes.

---

# 21. Interactive Rebase (Advanced)

Used to:
- edit commits
- remove commits
- rename commits

Example:

```bash
git rebase -i HEAD~3
```

This opens editor for last 3 commits.

---

# 22. Most Common Git Commands

| Task | Command |
|---|---|
| Check version | `git --version` |
| Initialize repo | `git init` |
| Check status | `git status` |
| Add file | `git add file.txt` |
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