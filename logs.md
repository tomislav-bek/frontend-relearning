## Log

### 13.04.2025

### Git & GitHub Setup Notes

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

### 14.04.2025

### HTML Boilerplate and Headings

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

---

### 15.04.2025

### Links & Images

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

---

### 18.04.2026

### Lists

**Process**
Created a basic lists folder with `index.html` file with ordered and unordered lists.

**Learning**

- `<ol>` is for ordered lists with a specific order.
- `<ul>` is for unordered lists with bullet points.
- `<li>` is one item in a list.
- This example is simple for now because it will be expanded later in a project.

**Problems**

- None.

---

### 18.04.2026

### Forms

**Process**
Created a simple `forms.html` file with name, email, message, and submit button. Kept the form simple for learning. Used the basic structure with labels and input fields.

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

---

### 19.04.2026

### Semantic HTML

**Process**
Created a simple semantic HTML file. Used `header`, `nav`, `main`, `section`, `article`, `aside`, and `footer`. Kept the example simple for learning.

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

---

### 11.05.2026

### Tables

**Process**
Started the tables section in the HTML relearning notes. Learned the main table elements and their purpose. Added table structure basics, table sections, the `scope` attribute, and spanning cells. Kept the example simple and semantic for practice.

**Learning**

- Tables are used for structured data in rows and columns.
- `<table>` contains the whole table.
- `<tr>` creates a row.
- `<th>` is used for header cells.
- `<td>` is used for normal data cells.
- `<caption>` gives the table a title.
- `<thead>`, `<tbody>`, and `<tfoot>` help organize the table structure.
- `scope` helps screen readers understand which row or column a header belongs to.
- `colspan` lets a cell span multiple columns.
- `rowspan` lets a cell span multiple rows.
- This section is useful because it improves both structure and accessibility.

**Problems**

- None.

### 27.05.2026

### Documentation Restructuring

**Process**
Completely restructured the repository's documentation logic. Created a dedicated `logs.md` file, a standalone master `general-notes.md` file, and implemented a one-Markdown-file-per-folder layout for topic subfolders. Standardized all personal note files to lowercase kebab-case.

**Learning**

- Repository meta files like README require uppercase, while custom note files should use lowercase kebab-case to ensure cross-platform compatibility and clean URLs.
- Co-location (keeping exactly one note file inside its matching code topic folder) prevents documentation from becoming outdated and creates an easily navigable portfolio.

**Problems**

- Managing all notes in a single giant file became cluttered and unreadable as the number of topics grew.
- Solution: Transitioned to a decentralized "Component-Based" documentation system by assigning a single note file to each respective subfolder.
