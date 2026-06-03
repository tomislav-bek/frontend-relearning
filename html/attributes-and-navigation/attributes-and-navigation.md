# HTML Global Attributes & Internal Navigation

Notes on how global attributes work in HTML and how they enable inner-page navigation.

## Key Concepts

**Global Attributes**
Global attributes are attributes that can be used on any HTML element. The most critical global attributes are id and class.

- **id**: A unique identifier for a single element. No two elements on the same webpage can share the same id.
- **class**: A non-unique identifier used to group multiple elements together. Multiple elements can share the same class.

_Note: While id and class do not change the visual appearance of elements on their own in pure HTML, they are foundational for linking HTML with CSS and JavaScript later._

**Internal Navigation (Page Anchors)**
Internal navigation allows users to jump or scroll to specific parts of the same webpage instantly. This is done by pairing an anchor tag (`<a>`) with a unique id attribute.

- **The Target**: You assign a unique id to the destination element (e.g., `<h2 id="target-heading">`).
- **The Trigger**: You create a link where the href attribute value starts with a hashtag followed by the target's ID (e.g., `<a href="#target-heading">`).

## Why this matters

- **Modern Layouts**: This methodology is essential for building single-page applications (SPAs) and landing pages.
- **Code Organization**: It prepares the HTML structure for future CSS styling and JavaScript functionality.
