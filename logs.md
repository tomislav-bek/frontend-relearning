## Log

### 13.04.2025

### Git & GitHub Setup Notes

**Process**

- Set up Git and GitHub version control environments from scratch.
- Created the core `frontend-relearning` remote repository.
- Configured essential Git global settings locally.
- Cloned the remote repository to the local machine workspace.
- Authored and structured the initial repository `README.md` and `NOTES.md` files.

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

- Designed the base folder directory structure for the complete relearning roadmap.
- Added dedicated workspace folders for `html`, `css`, `javascript`, `react`, and `nextjs`.
- Authored the first practice HTML file focusing on headings and semantic paragraphs.
- Implemented `.gitkeep` placeholder files inside empty directories to ensure tracking.

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

- Created the `links-and-images.html` development practice file.
- Embedded an external hyperlink navigating out to Google.
- Implemented a local placeholder image asset inside the markup.

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

- Created a dedicated practice subdirectory for layout lists.
- Authored an `index.html` file testing structured list elements.
- Implemented examples displaying ordered lists and unordered lists side by side.

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

- Created a dedicated `forms.html` workspace practice file.
- Built out form fields to capture user name, user email, and user messages.
- Added a functional submission button to complete the form scope.
- Linked text labels to input areas to keep layout connections clean.

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

- Created a baseline semantic structural layout file for testing.
- Implemented standard structural building blocks like `header`, `nav`, `main`, and `footer`.
- Organized content sections internally using modern tags like `section`, `article`, and `aside`.

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

- Initialized a brand new tables subfolder inside the HTML learning history tree.
- Studied and documented foundational tabular layout elements and accessibility standards.
- Designed a semantic weekly schedule demonstrating row layout foundations and grid sections.
- Configured grid cells with custom span settings and data cell association rules.

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

---

### 27.05.2026

### Documentation Restructuring

**Process**

- Completely restructured the repository's documentation layout and logic.
- Created a dedicated `logs.md` file to track daily progress independently.
- Created a standalone `general-notes.md` master file for global HTML concepts.
- Implemented a decentralized, one-Markdown-file-per-folder structure for topic subfolders.
- Standardized all personal documentation and note filenames to lowercase kebab-case.

**Learning**

- Repository meta files like README require uppercase, while custom note files should use lowercase kebab-case to ensure cross-platform compatibility and clean URLs.
- Co-location (keeping exactly one note file inside its matching code topic folder) prevents documentation from becoming outdated and creates an easily navigable portfolio.

**Problems**

- Managing all notes in a single giant file became cluttered and unreadable as the number of topics grew.
- Solution: Transitioned to a decentralized "Component-Based" documentation system by assigning a single note file to each respective subfolder.

---

### 03.06.2026

### Multi-Line Commit Methodology & Media Implementation

**Process**

- Created a dedicated audio-and-video.html file to practice native media elements.
- Added a matching audio-and-video.md file in the topic folder to document how these elements function.
- Updated the main README.md file with a general overview to integrate the new section into the learning path.
- Transitioned from short single-line Git commits to a detailed multi-line commit methodology using multiple -m flags in the terminal.
- Documented this new Git workflow and formatting standard in the general-notes.md master file.

**Learning**

- Industry-standard Git commits for large updates require a short imperative headline followed by a descriptive, bulleted body to provide clear context for employers.
- Multi-line commits can be executed directly from the raw terminal by chaining multiple -m flags, where each flag generates a new paragraph or bullet point.
- Writing commits in the imperative mood (e.g., "Add" instead of "Added") correctly answers the professional standard of what the commit will do when applied.
- Understood that Markdown syntax like asterisks and hashes belongs in text files for formatting, while clean, raw text should be used inside terminal Bash commands to keep the Git log professional.

**Problems**

- Combining multiple related file changes (HTML, MD, and README updates) under a single short commit message felt incomplete and lacked proper detail.
- Solution: Adopted a structured "Headline + Body" multi-line commit approach to maintain a highly transparent, clean, and professional repository history.

---

### 03.06.2026

### HTML Global Attributes & Page Navigation

**Process**

- Created an attributes-and-navigation folder with HTML and MD files.
- Implemented an isolated anchor link example using the unique id attribute.
- Added a reusable class attribute to multiple elements to practice grouping.
- Documented the core definitions and practical purposes of id and class in the markdown file.
- Updated the main README.md structure to include this global attributes milestone.

**Learning**

- Global attributes like id and class can be applied to absolutely any HTML element.
- The id attribute must be 100% unique per page, which is why anchor navigation requires it to target the destination.
- The class attribute is non-unique and can be shared among multiple elements for grouping.
- Internal page navigation works by combining href="#target-name" on the link with id="target-name" on the destination.

**Problems**

- Encountered a fatal terminal error when trying to run a multi-line git commit using the backslash (\) syntax in VS Code.
- Solution: Realized that Windows PowerShell does not recognize the Bash backslash character for newlines. Solved it by formatting the multi-line commit into a single continuous command chain.

---

### 03.06.2026

### HTML Containers, Iframes, and Special Entities

**Process**

- Created an entities-iframes-and-containers folder with HTML and MD files.
- Used generic div containers to isolate and group related layout elements.
- Implemented an iframe element to embed a local markdown file as a scrollable window.
- Applied HTML entity codes like &lt; and &gt; to display raw code symbols safely in text.
- Documented the full theory and architectural purposes of these elements in the markdown file.

**Learning**

- The div element has no semantic meaning or default styles, serving purely as a structure container for future CSS.
- An iframe acts as an inline window that can load and display standalone documents inside the current page.
- Reserved characters like less-than and greater-than signs must be converted to text entities to prevent browser parsing errors.

**Problems**

- None.

### 06.06.2026

### HTML Practice Showcase

**Process**

- Created a master html-practice-showcase folder to integrate all previously learned HTML concepts into one unified project.
- Designed a structured layout utilizing core semantic tags including header, nav, main, section, article, aside, and footer.
- Implemented fully functional in-page navigation using id attributes to allow seamless scrolling between sections.
- Consolidated diverse elements like forms, tables, ordered/unordered lists, and native media players into a single cohesive document.
- Added a comprehensive README documentation file explaining the architectural decisions and accessibility features of the master page.

**Learning**

- A master webpage requires strict heading hierarchy and clean commenting to remain maintainable as the codebase grows.
- Internal navigation anchors drastically improve user experience by linking menu items directly to specific section IDs.
- Combining multiple advanced elements like forms and tables on one page requires a deep understanding of how block-level and inline elements behave together.

**Problems**

- None.

---

### 06.06.2026

### Basic CSS Selectors

**Process**

- Created a basic-selectors folder containing index.html, style.css, and README.md.
- Implemented core element selectors to apply global styles to headings.
- Utilized reusable class selectors and demonstrated class chaining on a single element.
- Applied a unique ID selector to target an individual featured element layout.
- Documented the syntax rules and foundational target patterns in the module README.

**Learning**

- Class selectors require a dot prefix and are ideal for sharing styles across multiple elements.
- ID selectors require a hash prefix, must remain completely unique, and apply to only one element per page.
- Forgetting style prefixes causes the browser to parse the rule as a non-existent HTML tag.

**Problems**

- None.

---

### 06.06.2026

### Advanced CSS Selectors

**Process**

- Created an advanced-selectors folder to handle complex element targeting rules.
- Implemented grouping selectors to merge styling rules and reduce code repetition.
- Used descendant and strict child combinators to control styles based on HTML nesting structure.
- Applied adjacent sibling combinators, attribute selectors, pseudo-classes, and pseudo-elements.
- Added high-visibility contrast colors to easily identify exactly which selector triggered the style.
- Wrote an extensive README guide breaking down parent-child hierarchy and nesting levels.

**Learning**

- The descendant selector is broad and targets all matching elements at any nesting depth.
- The child selector is strict and targets elements only on the first level of the parent.
- Pseudo-classes handle dynamic user interaction states like mouse hover without using JavaScript.

**Problems**

- None.
