# Git & GitHub Setup Notes

Personal notes on how I set up Git and GitHub for the first time.

## What we set up

-   Git installed (version 2.53.9)
-   GitHub account created
-   Local repository connected to GitHub

## Step by step

### 1. Git installation

Downloaded Git from git-scm.com and installed with default settings.
Verified with `git --version` in terminal.

### 2. Git configuration

Configured name and email globally — this signs every commit.
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
To verify: `git config --global --list`
These settings are saved on the PC and apply to all Git projects.

### 3. GitHub account

-   Created account at github.com
-   Use full name as username — professional standard
-   Renaming existing account keeps Git history intact

### 4. Creating the repository

-   Created repo on GitHub: frontend-relearning
-   Set to Public — every commit builds visible history for employers
-   Added README on creation

### 5. Cloning to local machine

Navigated to Desktop in terminal:
cd Desktop
Cloned the repo:
git clone https://github.com/tomislav-bek/frontend-relearning.git
This created a local folder connected to GitHub.
Opened in VS Code with right click → Open with Code.

### 6. First commit and push

Edited README.md, then:
git add README.md
git commit -m "Update README with learning structure"
git push

### 7. Authentication issue

Git push asked for username and password.
GitHub no longer accepts regular password — needs Personal Access Token.

How to generate token:

-   GitHub → Profile picture → Settings → Developer settings
-   Personal access tokens → Tokens (classic) → Generate new token (classic)
-   Give it a name so you know what it's for
-   Expiration: 90 days
-   Scope: check only "repo"
-   Copy token immediately — GitHub shows it only once

Windows saved the token via a popup (Windows Credential Manager).
Next push will work without asking again.

## Daily workflow

Every time you make changes:
git add .
git commit -m "Short description of what you did"
git push
`git add .` adds all changed files at once.
`git add filename` adds only one specific file.

## Key concepts

-   `cd` = change directory (navigate folders in terminal)
-   `git clone` = download repo to local machine
-   `git add` = stage changes for commit
-   `git commit` = save snapshot with a message
-   `git push` = send commits to GitHub
-   Global git config = saved on PC, applies to all projects
-   Personal Access Token = GitHub password replacement, expires after set time

## Log

### 13.04.2025.

**Process**
Set up Git and GitHub from scratch. Created frontend-relearning repository, configured Git globally, cloned repo locally, wrote and structured README.md and NOTES.md.

**Learning**

-   Commit messages are written as commands, not first person
-   `git add .` stages all changed files at once
-   README is the public face, NOTES is personal
-   Every commit builds visible history — that is the portfolio

**Problems**

-   Git push failed — GitHub no longer accepts passwords
-   Solution: Personal Access Token via Settings → Developer settings
