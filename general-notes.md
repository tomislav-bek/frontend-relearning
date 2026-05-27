# Git & GitHub Setup Notes

Personal notes on how I set up Git and GitHub for the first time.

## What we set up

- Git installed.
- GitHub account created.
- Local repository connected to GitHub.

## Step by step

### 1. Git installation

- Downloaded Git from git-scm.com and installed it with default settings.
- Verified it with `git --version` in terminal.

### 2. Git configuration

- Configured name and email globally — this signs every commit.
- `git config --global user.name "Your Name"`
- `git config --global user.email "your@email.com"`
- To verify: `git config --global --list`
- These settings are saved on the PC and apply to all Git projects.

### 3. GitHub account

- Created an account on github.com.
- Using a full name as username looks more professional.
- Renaming an existing account keeps Git history intact.

### 4. Creating the repository

- Created the repo on GitHub: `frontend-relearning`
- Set it to Public — every commit builds visible history for employers.
- Added README on creation.

### 5. Cloning to local machine

- Navigated to Desktop in terminal:
- `cd Desktop`
- Cloned the repo:
- `git clone https://github.com/tomislav-bek/frontend-relearning.git`
- This created a local folder connected to GitHub.
- Opened it in VS Code with right click → Open with Code.

### 6. First commit and push

- Edited `README.md`, then:
- `git add README.md`
- `git commit -m "Update README with learning structure"`
- `git push`

### 7. Authentication issue

- Git push asked for username and password.
- GitHub no longer accepts regular passwords — it needs a Personal Access Token.

How to generate a token:

- GitHub → Profile picture → Settings → Developer settings
- Personal access tokens → Tokens (classic) → Generate new token (classic)
- Give it a name so you know what it is for.
- Expiration: 90 days.
- Scope: check only `repo`
- Copy the token immediately — GitHub shows it only once.
- Windows saved the token via a popup (Windows Credential Manager).
- Next push will work without asking again.

## Daily workflow

- Every time you make changes:
- `git add .`
- `git commit -m "Short description of what you did"`
- `git push`
- `git add .` adds all changed files at once.
- `git add filename` adds only one specific file.

## Git Commit Messages

I started using clearer commit messages that describe the main purpose of each commit.

### Common commit types

- `feat:` — a new feature or something new I added.
- `fix:` — a bug fix.
- `refactor:` — restructuring existing code without changing the main behavior.
- `docs:` — changes to documentation, README, or notes.
- `chore:` — technical or maintenance changes that are not features or bug fixes.

### Examples

- `feat: add new HTML file`
- `feat: add semantic HTML example`
- `fix: correct navbar spacing`
- `refactor: restructure navbar`
- `docs: update README.md and NOTES.md`
- `chore: clean up project files`

### Rule I follow

- I choose one main purpose for each commit message.
- If I change several related things in one commit, I still use one message that describes the whole change.
- Commit messages are short summaries, not a list of every single file or line changed.

## What I learned

- Commit messages should summarize the change, not describe every detail.
- The commit type helps show what kind of change it is.
- I am starting to use this format as a more organized Git practice.

## Key concepts

- `cd` = change directory, used to navigate folders in terminal.
- `git clone` = downloads a repo to local machine.
- `git add` = stages changes for commit.
- `git commit` = saves a snapshot with a message.
- `git push` = sends commits to GitHub.
- Global Git config = saved on the PC and applies to all projects.
- Personal Access Token = GitHub password replacement, expires after a set time.
