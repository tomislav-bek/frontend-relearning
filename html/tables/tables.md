## HTML Tables

### `<table>` — Table element

- The `<table>` element is used to create a structured table for data.
- It acts as the main container for all other table-related elements.
- It organizes data into rows and columns.

### `<caption>` — Caption element

- The `<caption>` element is used to give the table a title or brief description.
- It helps users quickly understand what data the table displays.
- It must be placed immediately after the opening `<table>` tag.

### `<thead>` — Table head element

- The `<thead>` element is used to group the header content of a table.
- It contains the row or rows that define the titles of your columns.
- It is useful for styling and helps screen readers read data correctly.

### `<tbody>` — Table body element

- The `<tbody>` element contains the main data or core content of the table.
- It separates the primary data rows from the header and footer rows.
- A table can have one or multiple body sections to group data.

### `<tfoot>` — Table foot element

- The `<tfoot>` element is used to group footer content at the bottom of a table.
- It is often used for summary rows, totals, or explanatory notes about the table.
- It appears structurally at the bottom of the table data.

### `<tr>` — Table row element

- The `<tr>` element defines a single horizontal row of cells in a table.
- It acts as a container for header cells (`<th>`) or standard data cells (`<td>`).
- Every cell in a table must live inside a row element.

### `<th>` — Table header cell element

- The `<th>` element defines a cell as a header for a column or a row.
- Text inside this element is usually bold and centered by default.
- It provides critical context to screen readers about the data beneath or beside it.

### `<td>` — Table data cell element

- The `<td>` element defines a standard data cell within a table row.
- It holds the actual data values like text, numbers, images, or links.
- By default, the text inside this element is regular weight and left-aligned.

### Special Attributes

- `scope=""` — Tells screen readers if a header cell (`<th>`) belongs to a column (`col`) or a row (`row`).
- `colspan=""` — Merges multiple columns together into a single wide cell.
- `rowspan=""` — Merges multiple rows together into a single tall cell.

### Small differences

- `<table>` is the outer container for the entire grid.
- `<caption>` is the overall title displayed on top of the table.
- `<thead>`, `<tbody>`, and `<tfoot>` split the grid into semantic logical sections.
- `<tr>` creates the horizontal rows.
- `<th>` is for labels/headers, while `<td>` is for regular data cells.
- `colspan` stretches a cell sideways, while `rowspan` stretches a cell downwards.
