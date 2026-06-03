# HTML Containers, Iframes, and Entity Codes

Comprehensive notes on how to group elements using containers, embed separate documents via iframes, and safely display reserved HTML characters.

## Key Concepts

**1. HTML Containers (The div Element)**
The `<div>` (Division) element is a generic, block-level container. It does not possess any semantic meaning, and it has no default visual styling in the browser.

- **Purpose**: It is used strictly as a blank, invisible box to group related HTML elements together.
- **Future Role**: Grouping elements inside a `<div>` makes it possible to target that specific group later for layout adjustments, spacing, and advanced styling once CSS is introduced.

**2. Inline Frames (The iframe Element)**
The `<iframe>` element is used to embed another HTML document or web page directly inside the current document. It functions as a scrollable window to another file or website.

- **src**: The attribute that defines the path or URL of the document to be loaded inside the frame (e.g., `src="../../general-notes.md"`).
- **width & height**: Attributes that set the exact size of the embedded frame window in pixels.

**3. HTML Entities (Special Character Codes)**
HTML entities are text shortcuts used to render characters that are either reserved by HTML syntax or hard to type on a standard keyboard. They always start with an ampersand (`&`) and end with a semicolon (`;`).

- **Reserved Characters**: Symbols like `<` and `>` are part of the HTML structural syntax. Writing them directly in plain text confuses the browser parser, which mistakes them for HTML tags and breaks the page layout.
- **&lt; (Less Than)**: Safely prints the `<` symbol on the screen without opening a tag.
- **&gt; (Greater Than)**: Safely prints the `>` symbol on the screen without closing a tag.

## Why this matters

- **Component Isolation**: Shows an understanding of how to encapsulate different parts of a layout using container blocks before learning CSS layout systems.
- **Document Integration**: Demonstrates the ability to link and embed standalone documents inside each other seamlessly.
- **Code Stability**: Proves that you write secure, robust HTML that correctly handles raw text data and symbols without triggering parsing glitches.
