# Basic CSS Selectors

This section covers the foundational methods used to target and style HTML elements using tags, classes, and IDs.

## Core Concepts

CSS uses selectors to bind styling rules to specific parts of the HTML document. There are three primary ways to target elements:

### 1. Element Selector

Targets every single element of that specific type on the page using the raw HTML tag name.

- Example: `h1` targets all `<h1>` tags globally.

### 2. Class Selector

Targets elements that share a specific class attribute. Classes act as reusable styling blueprints and can be applied to multiple elements on the same page.

- Syntax: Always starts with a dot (`.`) in the CSS file.
- Example: `.text-blue` targets any element with `class="text-blue"`.

### 3. ID Selector

Targets one specific element with a unique ID attribute. An ID must be unique to only one element per page, making it useful for individual layout highlights.

- Syntax: Always starts with a hash (`#`) in the CSS file.
- Example: `#featured-box` targets the element with `id="featured-box"`.

## Key Takeaways

- Classes are ideal for shared styles, and HTML allows you to chain multiple classes together (e.g., `class="text-blue text-large"`).
- IDs should be used sparingly and only for unique, single elements on a page.
- Forgetting the dot (`.`) or hash (`#`) prefixes in CSS will cause the browser to search for a non-existent HTML tag instead of the intended attribute.
