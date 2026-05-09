# Complete Beginner Git Course

# Table of Contents

1. What is Git?
2. Install Git
3. Configure Git
4. Create Your First Repository
5. Understanding Git Workflow
6. Git Status
7. Adding Files
8. Committing Changes
9. Viewing History
10. Branching
11. Merging
12. Clone Repository
13. Pull Changes
14. Push Changes
15. GitHub Setup
16. SSH Setup
17. Undo Changes
18. Git Reset
19. Git Rebase
20. Cherry Pick
21. Git Stash
22. Git Ignore
23. Common Errors
24. Complete Real Workflow
25. Most Common Commands

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

# 2. Install Git

## Windows

1. Visit:
   https://git-scm.com/downloads

2. Download Git for Windows

3. Install Git

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

# 3. Configure Git

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

# 4. Create Your First Repository

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

# 5. Understanding Git Workflow

Git workflow usually follows this process:

```text
Working Directory -> Staging Area -> Commit -> GitHub
```

### Working Directory
Where you create/edit files.

### Staging Area
Files ready to commit.

### Commit
Saved snapshot/version.

### GitHub
Online backup and collaboration platform.

---

# 6. Git Status

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

# 7. Adding Files

## Add Single File

```bash
git add abc.txt
```

## Add All Files

```bash
git add .
```

---

# 8. Commit Changes

Commit saves your changes.

```bash
git commit -m "Added login page"
```

---

# 9. View Commit History

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

# 10. Create Files

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

# 11. Branching

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

# 12. Merge Branches

Go to master/main branch:

```bash
git checkout master
```

Merge another branch:

```bash
git merge feature-login
```

---

# 13. Clone Repository

Copy repository from GitHub.

```bash
git clone <repository-url>
```

Example:

```bash
git clone https://github.com/username/project.git
```

---

# 14. Pull Latest Changes

Download latest changes from GitHub.

```bash
git pull
```

---

# 15. Push Changes

Upload commits to GitHub.

```bash
git push
```

First push:

```bash
git push -u origin master
```

---

# 16. Create GitHub Account

1. Open:
   https://github.com

2. Sign up

3. Verify email

4. Create repositories

---

# 17. Personal Access Token (PAT)

GitHub may ask for token instead of password.

Steps:
1. GitHub Settings
2. Developer Settings
3. Personal Access Tokens
4. Generate Token
5. Copy token safely

---

# 18. SSH Setup

SSH avoids password every time.

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

# 19. Undo Changes

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

# 20. Git Reset

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

# 21. Git Rebase

Used to:
- Clean commit history
- Edit commits
- Remove commits

Example:

```bash
git rebase -i HEAD~3
```

---

# 22. Cherry Pick

Copy one commit from another branch.

```bash
git cherry-pick <commit-id>
```

---

# 23. Git Stash

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

# 24. Git Ignore

Ignore files/folders.

Create `.gitignore`

Example:

```text
node_modules/
.env
dist/
```

---

# 25. Common Git Errors

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

# 26. Complete Real Workflow

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

## Go Inside Project

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

Edit files.

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

```bash
git pull origin master
```

OR if using main branch:

```bash
git pull origin main
```

---

## Push Changes

```bash
git push origin feature-login
```

---

# 27. Simple Daily Git Workflow

```bash
git status
git add .
git commit -m "Your message"
git pull origin main
git push origin main
```

---

# 28. Most Common Git Commands

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

# 29. Important Git Concepts

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

# 30. Best Practices

- Commit small changes
- Write meaningful commit messages
- Pull before push
- Use branches for features
- Never commit passwords or secrets
- Use `.gitignore`

---

# 31. Recommended Practice

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
