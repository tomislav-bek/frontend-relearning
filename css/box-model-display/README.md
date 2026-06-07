# CSS Box Model and Display Properties

This module covers the core fundamentals of layout rendering: how the browser calculates element dimensions and how elements behave within the document flow.

---

## 1. The Global Reset and `box-sizing`

Browsers apply default user-agent stylesheets (e.g., adding an automatic `8px` margin to the `<body>` tag). To maintain complete design consistency across different browsers, a global reset is implemented using the universal selector (`*`).

### Box Dimension Calculations: content-box vs. border-box

- **`content-box` (Browser Default):** The `width` property only applies to the innermost content area. The total width on screen is calculated as: `width + padding + border`. This makes layout math unpredictable.
- **`border-box` (Industry Standard):** The `width` property determines the final explicit space the element takes on the screen. The browser automatically shrinks the inner content area to absorb any padding and borders.

In this project, the global reset ensures that all layout math behaves predictably from a baseline of `0`.

---

## 2. Box Model Anatomy Breakdown

Using the `.box-anatomy` element (the yellow box with the crimson border), we demonstrate the four foundational layers:

1. **Content:** The text string inside the box.
2. **Padding (`30px`):** Clear space inside the box. It pushes the text away from the border while retaining the yellow background color.
3. **Border (`5px solid crimson`):** The visible frame wrapped securely around the padding layer.
4. **Margin (`40px` bottom):** The invisible external clearance space that forcefully pushes the next heading down the page.

---

## 3. Display Properties: Block vs. Inline

The `display` property alters how an element behaves in relation to surrounding elements.

### Block Elements (`display: block`)

- **Default tags:** `<div>`, `<p>`, `<h1>`–`<h6>`, `<section>`, `<article>`.
- **Code Behavior:** They occupy the full horizontal width of their parent container and force a line break.
- **Proof in Code:** In `style.css`, even though `.block-example` is restricted to `width: 250px`, the second block element refuses to sit next to it and is forced onto a new line.

### Inline Elements (`display: inline`)

- **Default tags:** `<span>`, `<a>`, `<strong>`, `<em>`.
- **Code Behavior:** They sit side-by-side horizontally within the normal text sequence and only take up the width of their actual text content.
- **Proof in Code:** In `style.css`, the properties `width: 300px;` and `margin-top: 50px;` are explicitly declared on `.inline-example`. When inspected in a browser, these are completely ignored because inline elements lack layout box controls.

---

## Key Takeaways

- Margins push elements away from each other; padding creates structural breathing room inside an individual element.
- Inline elements completely ignore top/bottom margins, top/bottom paddings (in terms of pushing lines away), width, and height.
- To make an inline element respect widths and vertical margins without making it break onto a new line, the display state must be shifted to `display: inline-block`.
