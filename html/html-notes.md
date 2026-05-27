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
