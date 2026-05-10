# Complete Beginner Git & GitHub Course

# Table of Contents

1. What is Git?
2. What is GitHub?
3. Difference Between Git and GitHub
4. Install Git
5. Configure Git
6. Create Your First Repository
7. Understanding Git Workflow
8. Git Status
9. Adding Files
10. Committing Changes
11. Viewing History
12. Branching
13. Merging
14. Clone Repository
15. Pull Changes
16. Push Changes
17. GitHub Setup
18. SSH Setup
19. Undo Changes
20. Git Reset
21. Git Rebase
22. Cherry Pick
23. Git Stash
24. Git Ignore
25. Common Errors
26. Complete Real Workflow
27. Most Common Commands
28. Best Practices

---

# 1. What is Git?

Git is a version control system.

It helps developers:
- Track code changes
- Save project history
- Collaborate with teams
- Restore old versions

Think of Git like a **save system for coding projects**.

---

# 2. What is GitHub?

GitHub is a cloud platform where Git repositories are stored online.

GitHub helps developers:
- Store code online
- Collaborate with teams
- Share projects
- Create pull requests
- Backup projects

Website:
https://github.com

---

# 3. Difference Between Git and GitHub

| Git | GitHub |
|---|---|
| Git is a version control system | GitHub is a cloud hosting platform |
| Git tracks code locally | GitHub stores repositories online |
| Git works offline | GitHub usually requires internet |
| Git is installed on your machine | GitHub runs in browser/cloud |
| Git manages project history | GitHub manages collaboration |
| Git is a tool | GitHub is a service/platform |

---

# Simple Understanding

## Git

Git saves and tracks project changes locally.

Example:

```bash
git add .
git commit -m "Added login page"
```

---

## GitHub

GitHub stores your Git repository online.

Example:

```bash
git push origin main
```

This uploads your code to GitHub.

---

# Real Life Analogy

| Real Life Example | Git | GitHub |
|---|---|---|
| Writing notes | Notebook | Google Drive |
| Save game progress | Save file | Cloud backup |
| Project files | Local folder | Online backup |

---

# 4. Install Git

## Windows

1. Visit:
   https://git-scm.com/downloads

2. Download Git for Windows

3. Run installer

4. Keep clicking **Next**

5. Finish installation

Check installation:

```bash
git --version
```

---

## Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install git
```

Check:

```bash
git --version
```

---

## macOS

```bash
brew install git
```

Check:

```bash
git --version
```

---

# 5. Configure Git

Set your username and email.

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Example:

```bash
git config --global user.name "Ritik Verma"
git config --global user.email "ritik@gmail.com"
```

Check configuration:

```bash
git config --list
```

---

# 6. Create Your First Repository

## Create Folder

```bash
mkdir my-first-repo
```

## Enter Folder

```bash
cd my-first-repo
```

## Initialize Git

```bash
git init
```

Now this folder is managed by Git.

---

# 7. Understanding Git Workflow

Git workflow:

```text
Working Directory -> Staging Area -> Commit -> GitHub
```

### Working Directory
Where files are created or edited.

### Staging Area
Files ready to commit.

### Commit
Saved snapshot/version.

### GitHub
Online storage and collaboration.

---

# 8. Git Status

Check repository status:

```bash
git status
```

Shows:
- Modified files
- New files
- Deleted files
- Staged files

---

# 9. Adding Files

## Add Single File

```bash
git add abc.txt
```

## Add All Files

```bash
git add .
```

---

# 10. Commit Changes

Commit saves changes permanently.

```bash
git commit -m "Added login page"
```

---

# 11. View Commit History

```bash
git log
```

Short version:

```bash
git log --oneline
```

View commit details:

```bash
git show <commit-id>
```

Example:

```bash
git show a1b2c3
```

---

# 12. Create Files

```bash
echo "Hello World" > abc.txt
```

Check status:

```bash
git status
```

Add and commit:

```bash
git add .
git commit -m "Created abc.txt"
```

---

# 13. Branching

Branches allow separate development.

## Create Branch

```bash
git branch feature-login
```

## View Branches

```bash
git branch
```

## Switch Branch

```bash
git checkout feature-login
```

## Create + Switch Together

```bash
git checkout -b feature-dashboard
```

---

# 14. Merge Branches

Go to master/main branch:

```bash
git checkout master
```

Merge another branch:

```bash
git merge feature-login
```

---

# 15. Clone Repository

Copy repository from GitHub.

```bash
git clone <repository-url>
```

Example:

```bash
git clone https://github.com/username/project.git
```

---

# 16. Pull Latest Changes

Download latest changes from GitHub.

```bash
git pull
```

---

# 17. Push Changes

Upload commits to GitHub.

```bash
git push
```

First push:

```bash
git push -u origin master
```

---

# 18. Create GitHub Account

1. Open:
   https://github.com

2. Sign up

3. Verify email

4. Create repositories

---

# 19. Personal Access Token (PAT)

GitHub may ask for token instead of password.

Steps:
1. GitHub Settings
2. Developer Settings
3. Personal Access Tokens
4. Generate Token
5. Copy token safely

---

# 20. SSH Setup

SSH avoids entering password repeatedly.

## Generate SSH Key

```bash
ssh-keygen
```

Press Enter multiple times.

## View Public Key

```bash
cat ~/.ssh/id_rsa.pub
```

## Add Key to GitHub

1. GitHub Settings
2. SSH and GPG Keys
3. New SSH Key
4. Paste key

Now GitHub access works without password.

---

# 21. Undo Changes

## Restore File

```bash
git restore abc.txt
```

---

## Unstage File

```bash
git restore --staged abc.txt
```

---

# 22. Git Reset

## Soft Reset

Keeps file changes.

```bash
git reset --soft HEAD~1
```

---

## Hard Reset

Deletes changes permanently.

```bash
git reset --hard HEAD~1
```

⚠️ Dangerous command.

---

# 23. Git Rebase

Used to:
- Clean commit history
- Edit commits
- Remove commits

Example:

```bash
git rebase -i HEAD~3
```

---

# 24. Cherry Pick

Copy one commit from another branch.

```bash
git cherry-pick <commit-id>
```

---

# 25. Git Stash

Temporarily save unfinished work.

## Save Changes

```bash
git stash
```

## View Stashes

```bash
git stash list
```

## Restore Stash

```bash
git stash pop
```

---

# 26. Git Ignore

Ignore files/folders.

Create `.gitignore`

Example:

```text
node_modules/
.env
dist/
```

---

# 27. Common Git Errors

## Error: Permission denied

Fix:
- Configure SSH
- Add SSH key to GitHub

---

## Error: Merge conflict

Happens when same file changed differently.

Fix:
1. Open conflicted file
2. Edit manually
3. Add file
4. Commit changes

---

## Error: Repository not found

Fix:
- Check repository URL
- Check GitHub permissions

---

# 28. Complete Real Workflow

## First Time Setup

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## Clone Repository

```bash
git clone https://github.com/username/project.git
```

---

## Enter Project

```bash
cd project
```

---

## Create Branch

```bash
git checkout -b feature-login
```

---

## Make Changes

Edit project files.

---

## Check Status

```bash
git status
```

---

## Add Changes

```bash
git add .
```

---

## Commit Changes

```bash
git commit -m "Added login feature"
```

---

## Pull Latest Changes Before Push

If using `main` branch:

```bash
git pull origin main
```

If using `master` branch:

```bash
git pull origin master
```

---

## Push Changes

```bash
git push origin feature-login
```

---

# 29. Simple Daily Git Workflow

```bash
git status
git add .
git commit -m "Your message"
git pull origin main
git push origin main
```

---

# 30. Most Common Git Commands

| Task | Command |
|---|---|
| Check version | `git --version` |
| Initialize repo | `git init` |
| Check status | `git status` |
| Add file | `git add file.txt` |
| Add all files | `git add .` |
| Commit | `git commit -m "message"` |
| View logs | `git log` |
| Short logs | `git log --oneline` |
| Create branch | `git branch branch-name` |
| Switch branch | `git checkout branch-name` |
| Create + switch branch | `git checkout -b branch-name` |
| Merge branch | `git merge branch-name` |
| Clone repo | `git clone url` |
| Pull latest code | `git pull` |
| Push changes | `git push` |
| Reset changes | `git reset --hard` |
| Save temporary work | `git stash` |
| Restore stash | `git stash pop` |

---

# 31. Important Git Concepts

| Concept | Meaning |
|---|---|
| Repository | Project folder |
| Commit | Save point |
| Branch | Separate workspace |
| Merge | Combine branches |
| Clone | Copy repository |
| Pull | Download latest code |
| Push | Upload code |
| Rebase | Rewrite history |
| Cherry-pick | Copy one commit |
| Stash | Temporary save |

---

# 32. Best Practices

- Commit small changes
- Write meaningful commit messages
- Pull before push
- Use branches for features
- Never commit passwords or secrets
- Use `.gitignore`

---

# 33. Recommended Practice

Practice these daily:
1. Create repository
2. Create files
3. Commit changes
4. Create branches
5. Merge branches
6. Push to GitHub
7. Pull latest changes
8. Resolve merge conflicts

This is the fastest way to master Git.
