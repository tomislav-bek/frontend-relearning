# Git & GitHub Setup Notes

Personal notes on how I set up Git and GitHub for the first time.

## WHAT WE SET UP

- Git installed.
- GitHub account created.
- Local repository connected to GitHub.

---

## STEP BY STEP GUIDE

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
- `git clone https://github.com`
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

**How to generate a token:**

- GitHub → Profile picture → Settings → Developer settings
- Personal access tokens → Tokens (classic) → Generate new token (classic)
- Give it a name so you know what it is for.
- Expiration: 90 days.
- Scope: check only `repo`
- Copy the token immediately — GitHub shows it only once.
- Windows saved the token via a popup (Windows Credential Manager).
- Next push will work without asking again.

---

## DAILY WORKFLOW

- Every time you make changes:
- `git add .`
- `git commit -m "Short description of what you did"`
- `git push`
- `git add .` adds all changed files at once.
- `git add filename` adds only one specific file.

---

## GIT COMMIT MESSAGES

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

---

### Detailed Multi-line Commits

For larger updates that include multiple related changes, I use a multi-line format (a short headline followed by bullet points). This keeps the Git history clean while providing clear context.

- **Headline:** A short imperative summary (under 50 characters).
- **Blank line:** Separates the headline from the body.
- **Body:** Bullet points describing exactly what was added, changed, or updated.

**Terminal syntax for multi-line commits (Windows PowerShell):**
Each `-m` flag creates a new paragraph or bullet point in the terminal. Use the backtick (`) character at the end of each line to continue the command on the next line.

```powershell
git commit -m "Add audio and video learning materials" `
           -m "- Add audio-and-video HTML page with examples" `
           -m "- Add explanation and guide in audio-and-video.md" `
           -m "- Update main README with the new section"
```

### What I learned

- Commit messages should summarize the change, not describe every detail.
- The commit type helps show what kind of change it is.
- I am starting to use this format as a more organized Git practice.

---

## FIXING MISTAKES BEFORE PUSHING

Personal notes on how to fix a commit if a file was forgotten or a mistake was made, **before** running `git push`.

### The Amend Method

If you already made a commit but forgot to include a file (like `README.md`) or made a typo, you can modify the very last commit instead of creating a new one.

#### Scenario A: You forgot to include a changed file

1. Stage the forgotten file:
    ```powershell
    git add filename.ext
    ```
2. Inject the file into the last commit without changing the original commit message:
    ```powershell
    git commit --amend --no-edit
    ```

#### Scenario B: You just want to fix a typo in the last commit message

If the files are correct but you want to rewrite the headline or body:

```powershell
git commit --amend -m "New correct commit message headline" -m "- New correct bullet point"
```

### Important Rule to Follow

- **Only use `--amend` if you have NOT pushed yet.** Once you run `git push`, the commit is public on GitHub and you should not modify it. If it is already pushed, just make a regular new commit.

### What if I accidentally amended AFTER running git push?

If you already pushed the commit to GitHub and then used `--amend` locally, your terminal and GitHub will conflict. Your next regular `git push` will be rejected.

**The Fix (For Personal Repositories Only):**
You can force GitHub to accept your local amended commit and overwrite the remote history. Run this command in your terminal:

```powershell
git push --force
```

_Warning: Only use `--force` on your personal repositories where you are the only person working. Never use it on a shared team repository at a job, as it can overwrite your coworkers' code!_

---

## FIXING MISTAKES AFTER RUNNING GIT PUSH

If you have already pushed your commits to GitHub, the golden rule in a professional environment is to leave the past commits alone. Do not use `--amend` or `--force`. Instead, you fix the mistake by creating a new forward-moving commit.

### Scenario 1: You forgot to include a file or made a text mistake

Simply make the changes, stage them, and create a new commit with a descriptive message.

1. Add the forgotten changes:
    ```powershell
    git add README.md
    ```
2. Commit with a prefix like `docs:` or `fix:` to show it is a correction:
    ```powershell
    git commit -m "docs: add missing global attributes section to README"
    ```
3. Push normally:
    ```powershell
    git push
    ```

### Scenario 2: You introduced a major bug and need to completely undo a pushed commit

If a pushed commit broke the application and you need to safely roll it back without erasing the history, use the `git revert` command. This creates a new commit that does the exact opposite of the bad commit.

1. Find the ID (hash) of the bad commit using `git log`.
2. Run the revert command:
    ```powershell
    git revert a1b2c3d4
    ```
3. Push the reversion to GitHub:
    ```powershell
    git push
    ```

### Why this is the industry standard:

- **Preserves History**: It keeps a transparent log of what went wrong and how it was fixed.
- **Team Safe**: It prevents synchronization conflicts for other developers working on the same project.

---

## KEY CONCEPTS

- `cd` = change directory, used to navigate folders in terminal.
- `git clone` = downloads a repo to local machine.
- `git add` = stages changes for commit.
- `git commit` = saves a snapshot with a message.
- `git push` = sends commits to GitHub.
- Global Git config = saved on the PC and applies to all projects.
- Personal Access Token = GitHub password replacement, expires after a set time.
