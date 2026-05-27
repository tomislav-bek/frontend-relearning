# HTML Master Notes & Theory Hub

HTML (HyperText Markup Language) is the foundational structural language of the web. It is not a programming language; it is a markup language used to label text data so web browsers know how to structure it visually.

---

## A Brief History of HTML

- **1991 (HTML 1.0)**: Created by Tim Berners-Lee at CERN. It contained only 18 basic tags designed purely for sharing scientific text documents.
- **1999 (HTML 4.01)**: Became the web standard for a decade. However, it lacked native multimedia tags, forcing websites to rely on slow, insecure third-party plugins like Flash.
- **2014 (HTML5)**: The modern standard. It completely modernized the web by introducing native video/audio tags, powerful semantic structural elements, and strict rules for accessibility and SEO.

---

## Core HTML Logic (Pure Structure)

### Elements vs. Tags

- A **Tag** is the single code command wrapped in angle brackets (e.g., `<p>`).
- An **Element** is the complete package: the opening tag, the inner content, and the closing tag combined (e.g., `<p>Hello World</p>`).

### Nesting and Parent-Child Relationships

- HTML relies on strict nesting rules. Tags must close in the exact reverse order they were opened (e.g., `<strong><em>Text</em></strong>` is correct).
- The outer tag is the **Parent**, and any tags placed inside it are **Children**. Child elements inherit the language configuration of their parent.

### Attributes Anatomy

- Attributes look like `name="value"` and live exclusively inside the opening tag.
- They provide hidden configuration settings or targets to the tag that the raw text content cannot provide.

---

## The Document Boilerplate Breakdown

### `<!DOCTYPE html>`

- Tells the browser instantly that this file is a modern HTML5 document.
- It forces the browser into "standards mode" so it renders your code correctly instead of guessing.

### `<html lang="en">`

- The root element wrapping the entire document.
- The `lang` attribute is critical for screen readers (accessibility) and tells Google Search what language to expect.

### `<head>`

- The processing brain of the document.
- It holds metadata, tab titles, and external resource connections that are invisible to the user.

### `<meta charset="UTF-8">`

- Configures character encoding.
- UTF-8 is the global standard because it supports almost all symbols and characters, including Croatian letters (č, ć, š, đ, ž).

### `<meta name="viewport" content="width=device-width, initial-scale=1.0">`

- Establishes mobile responsive scaling logic.
- It tells mobile browsers to match the website layout to the actual physical screen width instead of pretending it is a desktop screen.

### `<title>`

- Defines the exact text shown on the browser tab and search engine result links.

### `<body>`

- The visible stage. Everything written here is rendered directly onto the user's screen.

---
