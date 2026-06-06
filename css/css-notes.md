# CSS Master Notes & Theory Hub

CSS (Cascading Style Sheets) is the foundational style sheet language of the web. It is not a programming language; it is a design language used to control the presentation, visual layout, and formatting of HTML elements on a webpage.

---

## A Brief History of CSS

- **1996 (CSS 1)**: Created by Håkon Wium Lie and Bert Bos to separate web content from design. It provided basic control over fonts, text alignment, and colors.
- **1998 (CSS 2)**: Introduced page layouts via floats and absolute positioning, allowing developers to break away from table-based structures.
- **Modern CSS (CSS3 & CSS4 Features)**: Shifted into a modular development system. It revolutionized responsive layouts with Flexbox and CSS Grid, and introduced native animations, custom properties (variables), and container queries.

---

## Core CSS Logic (The Cascade & Inheritance)

### The Cascade Priority

- CSS applies styles from top to bottom. If two rules clash, the browser follows a strict hierarchy to decide which one wins.
- Priority is determined by three factors in this order: Importance (e.g., `!important`), Specificity (how targeted the selector is), and Source Order (the rule written last wins).

### Inheritance

- Many CSS properties automatically pass down from a parent element to its children.
- Text properties like `color`, `font-family`, and `line-height` are inherited, while structural properties like `margin`, `padding`, and `border` are never passed down.

### CSS Anatomy

- A **Selector** targets the specific HTML element (e.g., `h1`).
- A **Declaration Block** is wrapped in curly braces `{}` and contains one or more styles.
- A **Declaration** is a single property-value pair separated by a colon and ended with a semicolon (e.g., `color: blue;`).

---

## Core Inclusion Methods Breakdown

### Inline CSS

- Written directly inside the HTML element using the `style` attribute (e.g., `<p style="color: red;">Text</p>`).
- It has extremely high specificity but makes the HTML messy and difficult to maintain.

### Internal (Embedded) CSS

- Written inside a `<style>` tag placed exclusively within the HTML `<head>` section.
- It is useful for single-page documents but becomes inefficient for multi-page websites.

### External CSS

- Written in a completely separate `.css` file (usually named `style.css`) and linked in the HTML `<head>`.
- This is the absolute industry standard because it separates structure from presentation, caches styles for faster loading, and allows one file to control an entire website.

---

## The Linking Breakdown

### `<link rel="stylesheet" href="style.css">`

- The `rel="stylesheet"` attribute tells the browser that the connected resource is a style sheet.
- The `href` attribute defines the exact file path to your external CSS document.
- Placing this tag inside the HTML `<head>` ensures the browser loads and applies the styles before rendering the body text, preventing unstyled content flashes.
