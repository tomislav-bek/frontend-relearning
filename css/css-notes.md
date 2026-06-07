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

---

### The "Full Width" Misconception

When a block element is said to occupy "full width," it means **100% of its parent container's content width**, not the entire viewport/page width. A block element is horizontally contained by its parent's boundaries and will respect any padding constraints applied to that parent.

---

### Why Inline Elements Ignore Dimensions

By architectural design, inline elements (`display: inline`) are meant to flow seamlessly inside a line of text, just like individual words in a sentence.

Because breaking or expanding a single word horizontally or vertically would destroy the alignment of the entire paragraph, the browser engine is programmed to explicitly disable layout box controls for these elements. As a strict technical rule:

- **`width` and `height` properties are completely deactivated** because an inline element can only be as wide and as tall as its inner content dictates.
- **`margin-top` and `margin-bottom` properties are completely ignored** to prevent the element from disrupting the vertical line-height of the surrounding text sequence.

---

### Block-Level Space Reservation vs. Inner Content Behavior

When a block element expands to occupy full width, it behaves as a strict layout inhibitor rather than scaling its inner text layout properties:

- **Visual Box Reservation**: The element forcefully reserves the entire horizontal plane inside its parent container. Any declared `background-color` or horizontal borders will stretch across the entire available container width. No surrounding elements are permitted to occupy this row.
- **Inner Content Constraints**: The actual text content inside the block container remains unaffected by the horizontal expansion. The text string maintains its natural character length and alignments (defaulting to the left margin), leaving the remainder of the reserved horizontal track as unrendered whitespace.
