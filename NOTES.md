# Git & GitHub Setup Notes

Personal notes on how I set up Git and GitHub for the first time.

## What we set up

- Git installed (version 2.53.9)
- GitHub account created
- Local repository connected to GitHub

## Step by step

### 1. Git installation

- Downloaded Git from git-scm.com and installed with default settings.
- Verified with `git --version` in terminal.

### 2. Git configuration

- Configured name and email globally — this signs every commit.
- git config --global user.name "Your Name"
- git config --global user.email "your@email.com"
- To verify: `git config --global --list`
- These settings are saved on the PC and apply to all Git projects.

### 3. GitHub account

- Created account at github.com
- Use full name as username — professional standard
- Renaming existing account keeps Git history intact

### 4. Creating the repository

- Created repo on GitHub: frontend-relearning
- Set to Public — every commit builds visible history for employers
- Added README on creation

### 5. Cloning to local machine

- Navigated to Desktop in terminal:
- cd Desktop
- Cloned the repo:
- git clone https://github.com/tomislav-bek/frontend-relearning.git
- This created a local folder connected to GitHub.
- Opened in VS Code with right click → Open with Code.

### 6. First commit and push

- Edited README.md, then:
- git add README.md
- git commit -m "Update README with learning structure"
- git push

### 7. Authentication issue

- Git push asked for username and password.
- GitHub no longer accepts regular password — needs Personal Access Token.

How to generate token:

- GitHub → Profile picture → Settings → Developer settings
- Personal access tokens → Tokens (classic) → Generate new token (classic)
- Give it a name so you know what it's for
- Expiration: 90 days
- Scope: check only "repo"
- Copy token immediately — GitHub shows it only once

- Windows saved the token via a popup (Windows Credential Manager).
- Next push will work without asking again.

## Daily workflow

- Every time you make changes:
- git add .
- git commit -m "Short description of what you did"
- git push
- `git add .` adds all changed files at once.
- `git add filename` adds only one specific file.

## Key concepts

- `cd` = change directory (navigate folders in terminal)
- `git clone` = download repo to local machine
- `git add` = stage changes for commit
- `git commit` = save snapshot with a message
- `git push` = send commits to GitHub
- Global git config = saved on PC, applies to all projects
- Personal Access Token = GitHub password replacement, expires after set time

## Log

### 13.04.2025.

**Process**
Set up Git and GitHub from scratch. Created frontend-relearning repository, configured Git globally, cloned repo locally, wrote and structured README.md and NOTES.md.

**Learning**

- Commit messages are written as commands, not first person
- `git add .` stages all changed files at once
- README is the public face, NOTES is personal
- Every commit builds visible history — that is the portfolio

**Problems**

- Git push failed — GitHub no longer accepts passwords
- Solution: Personal Access Token via Settings → Developer settings

---

## HTML

HTML (HyperText Markup Language) is the standard language for creating web pages.
The current version is HTML5, released in 2014, which introduced semantic elements,
audio/video support and better structure overall. Browsers read HTML and render it
as visible content on screen.

### HTML Boilerplate

Generated automatically with `!` + Tab in VS Code (Emmet).

**<!DOCTYPE html>**
Tells the browser this is an HTML5 document. Older versions of HTML had longer
and more complex doctypes — this short version is the modern standard.

**<html lang="en">**
Root element that wraps the entire page. The lang attribute tells the browser,
search engines and screen readers what language the content is written in.

**<head>**
Contains metadata about the page — not visible to the user, but important for
the browser, search engines and other tools.

**<meta charset="UTF-8">**
Tells the browser which character encoding to use. UTF-8 supports almost all
characters from all languages, including Croatian letters č, ć, š, đ, ž.

**<meta name="viewport" content="width=device-width, initial-scale=1.0">**
Makes the page responsive. Tells the browser to set the width to the device
screen width and not to zoom out on mobile devices.

**<title>**
Sets the name of the page — visible on the browser tab and in search engine results.

**<body>**
Contains all visible content on the page. Everything the user sees goes here.

### Headings & Paragraphs

**h1-h6**
Define content hierarchy on the page. The lower the number, the more important the
heading. Only one h1 per page — it tells search engines and screen readers what the
page is about. h2-h6 are used for subheadings and deeper structure. Size is visual
but semantics is what matters — CSS can always change the appearance.

**p**
Wraps a block of text into a paragraph. All visible body text on a page goes inside
a p tag. Browsers automatically add spacing above and below each paragraph.

### Log

#### 14.04.2025.

**Process**
Created folder structure for the relearning repo. Added html, css, javascript, react
and nextjs folders. Created first HTML file with headings and paragraph example.
Used .gitkeep to track empty folders in Git.

**Learning**

- Git does not track empty folders — use .gitkeep as a placeholder
- Emmet in VS Code generates HTML boilerplate with ! + Tab
- DOCTYPE tells the browser this is HTML5
- charset UTF-8 supports all characters including Croatian letters
- viewport meta tag makes the page responsive to screen size
- h1-h6 are semantic not just visual — search engines read the hierarchy
- Only one h1 per page
- p tag wraps all visible body text

**Problems**

- Empty folders were not pushed to GitHub — solved with .gitkeep
