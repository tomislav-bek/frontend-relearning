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

## Key concepts

- `cd` = change directory, used to navigate folders in terminal.
- `git clone` = downloads a repo to local machine.
- `git add` = stages changes for commit.
- `git commit` = saves a snapshot with a message.
- `git push` = sends commits to GitHub.
- Global Git config = saved on the PC and applies to all projects.
- Personal Access Token = GitHub password replacement, expires after a set time.

## Log

### 13.04.2025

**Process**
Set up Git and GitHub from scratch. Created the `frontend-relearning` repository, configured Git globally, cloned the repo locally, and wrote and structured `README.md` and `NOTES.md`.

**Learning**

- Commit messages are written as commands, not first person.
- `git add .` stages all changed files at once.
- README is the public face, NOTES is personal.
- Every commit builds visible history — that is the portfolio.

**Problems**

- Git push failed — GitHub no longer accepts passwords.
- Solution: Personal Access Token via Settings → Developer settings.

---

# HTML

HTML (HyperText Markup Language) is the standard language for creating web pages. HTML5, released in 2014, introduced semantic elements, audio/video support, and better structure overall. Browsers read HTML and render it as visible content on screen.

## HTML Boilerplate

Generated automatically with `!` + Tab in VS Code (Emmet).

### `<!DOCTYPE html>`

- Tells the browser this is an HTML5 document.
- Older versions had longer and more complex doctypes — this short version is the modern standard.

### `<html lang="en">`

- Root element that wraps the entire page.
- The `lang` attribute tells the browser, search engines, and screen readers what language the content is in.

### `<head>`

- Contains metadata about the page.
- Not visible to the user, but important for the browser, search engines, and other tools.

### `<meta charset="UTF-8">`

- Tells the browser which character encoding to use.
- UTF-8 supports almost all characters from all languages, including Croatian letters č, ć, š, đ, ž.

### `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

- Makes the page responsive.
- Tells the browser to use the device width and not zoom out on mobile.

### `<title>`

- Sets the name of the page.
- Visible on the browser tab and in search engine results.

### `<body>`

- Contains all visible content on the page.
- Everything the user sees goes here.

## Headings & Paragraphs

### `h1-h6`

- Define content hierarchy on the page.
- The lower the number, the more important the heading.
- Only one `h1` per page — it tells search engines and screen readers what the page is about.
- `h2-h6` are used for subheadings and deeper structure.
- Size is visual, but semantics matter — CSS can always change the appearance.

### `p`

- Wraps a block of text into a paragraph.
- All visible body text on a page goes inside a `p` tag.
- Browsers automatically add spacing above and below each paragraph.

## Log

### 14.04.2025

**Process**
Created the folder structure for the relearning repo. Added `html`, `css`, `javascript`, `react`, and `nextjs` folders. Created the first HTML file with headings and paragraph examples. Used `.gitkeep` to track empty folders in Git.

**Learning**

- Git does not track empty folders — use `.gitkeep` as a placeholder.
- Emmet in VS Code generates HTML boilerplate with `!` + Tab.
- DOCTYPE tells the browser this is HTML5.
- `charset UTF-8` supports all characters, including Croatian letters.
- The viewport meta tag makes the page responsive to screen size.
- `h1-h6` are semantic, not just visual — search engines read the hierarchy.
- Only one `h1` per page.
- `p` tags wrap visible body text.

**Problems**

- Empty folders were not pushed to GitHub — solved with `.gitkeep`.

### Links & Images

### `<a>` — Anchor element

- The `<a>` element is used to create hyperlinks.
- By itself it does nothing — it needs the `href` attribute to define the destination.
- The `target` attribute controls where the link opens — `target="_blank"` opens in a new tab.
- Convention: use `target="_blank"` for external links, not internal ones.

### `<img>` — Image element

- The `<img>` element displays an image on a web page.
- It is a self-closing tag — it has no closing tag.
- It requires the `src` attribute to define the image source (URL or local file path).
- The `alt` attribute provides a text description of the image — important for accessibility and SEO.

## Log

### 15.04.2025

**Process**
Created `links-and-images.html` with an external link to Google and a placeholder image.

**Learning**

- `<a>` requires `href` to function — without it, it renders as plain text.
- `target="_blank"` opens the link in a new tab — use it for external links only.
- `<img>` is self-closing — no closing tag needed.
- `src` defines the image source — can be a URL or a local file path.
- `alt` describes the image for screen readers and search engines — always include it.

**Problems**

- None.

### Lists

### `<ol>` — Ordered list

- The `<ol>` element is used for lists where the order matters.
- It shows the items with numbers.
- Use it when the sequence is important.

### `<ul>` — Unordered list

- The `<ul>` element is used for lists where the order does not matter.
- It shows the items with bullet points.
- Use it when the items can be in any order.

### `<li>` — List item

- The `<li>` element represents one item inside a list.
- It must go inside an `<ol>` or `<ul>` element.
- Without `<li>`, the list does not have separate items.

### Small difference

- Use `<ol>` when the order matters.
- Use `<ul>` when the order does not matter.

## Log

### 18.04.2026

**Process**

- Created a basic lists folder with `index.html` file with ordered and unordered lists.

**Learning**

- `<ol>` is for ordered lists with a specific order.
- `<ul>` is for unordered lists with bullet points.
- `<li>` is one item in a list.
- This example is simple for now because it will be expanded later in a project.

**Problems**

- None.

### Forms

### `form` — Form element

- The `form` element is used to group input fields and submit them together.
- It is used for collecting or sending data.
- It wraps the whole form.

### `label` — Label element

- The `label` element gives a visible name to an input field.
- It explains what the user should type in that field.
- It is connected to the input with `for` and `id`.

### `input` — Input element

- The `input` element is used for single-line fields.
- `type="text"` tells the browser that the field is for text.
- `type="email"` tells the browser that the field should contain an email address.
- `input` fields are limited because they do not show the full message at once.

### `textarea` — Textarea element

- The `textarea` element is used for longer text.
- It shows the full message better than a normal input field.
- It is useful for messages, comments, or anything longer than one line.

### `button` — Button element

- The `button` element is used to submit the form.
- `type="submit"` tells the browser that the form should be sent.
- It is the final step after filling in the fields.

### `required` — Required attribute

- The `required` attribute makes a field mandatory.
- The form cannot be submitted if the field is empty.
- It is used when the input is important and must be filled in.

### Small difference

- `input` is used for short, single-line values.
- `textarea` is used for longer text that needs more space.
- `label` makes the field clear and easier to understand.

## Log

### 18.04.2026

**Process**

- Created a simple `forms.html` file with name, email, message, and submit button.
- Kept the form simple for learning.
- Used the basic structure with labels and input fields.

**Learning**

- A form is a combination of labels and input fields used for sending or collecting data.
- `label` gives the field a visible name.
- `for` and `id` are used to connect the label with the input.
- `input type="text"` is for text.
- `input type="email"` is for email addresses.
- `textarea` is better for longer messages.
- `button type="submit"` sends the form.
- `required` makes the field mandatory.
- This form is enough for now because later I will make projects where I use more things together.

**Problems**

- None.

### Semantic HTML

### `<header>` — Header element

- The `<header>` element is used for the top part of a page or a section.
- It often contains the logo, navigation, and main introductory information.
- It is commonly placed at the top of the page.
- It can also be used inside other elements like `<article>` or `<section>`.

### `<nav>` — Navigation element

- The `<nav>` element is used for the main navigation of a website.
- It contains links to other pages or important parts of the site.
- It helps users move through the website more easily.

### `<main>` — Main content element

- The `<main>` element contains the main content of the page.
- It should hold the most important content that the page is about.
- Usually there is only one `<main>` on a page.

### `<section>` — Section element

- The `<section>` element is used for a logical part of the page.
- It groups related content together.
- It is used when the content belongs to one clear topic or subtopic.

### `<article>` — Article element

- The `<article>` element is used for a self-contained piece of content.
- It can stand on its own.
- It is still usually related to the main topic of the page.

### `<aside>` — Aside element

- The `<aside>` element is used for side content.
- It contains content that is not the main part of the page.
- It can include related links, extra notes, or additional information.

### `<footer>` — Footer element

- The `<footer>` element is used for the bottom part of a page or section.
- It often contains contact information, copyright, and useful links.
- It can also be used inside other sections of a page.

### Small differences

- `<header>` is for the top part of the page or section.
- `<nav>` is for the main navigation links.
- `<main>` is for the main content only.
- `<section>` is for a logical group of related content.
- `<article>` is for content that can stand on its own.
- `<aside>` is for side content.
- `<footer>` is for the bottom part of the page or section.

## Log

### 19.04.2026

**Process**

- Created a simple semantic HTML file.
- Used `header`, `nav`, `main`, `section`, `article`, `aside`, and `footer`.
- Kept the example simple for learning.

**Learning**

- Semantic HTML helps structure content in a meaningful way.
- `header` is usually at the top and can contain logo and navigation.
- `nav` is for the main navigation of a website.
- `main` contains the main content of the page.
- `section` groups related content together.
- `article` is a self-contained piece of content.
- `aside` is side content that is not the main part of the page.
- `footer` is the bottom part of the page.
- This was a good next step after forms and lists because it helps with page structure.

**Problems**

- None.
