# Flexbox Basics

This section introduces Flexbox, the first CSS layout system covered in this repo that provides real control over alignment and spacing between elements, rather than relying on the default block-stacking behavior.

---

## 1. Why Flexbox, and Why Now

Everything up to this point (Box Model, Display Properties) controls how a _single_ element is sized and rendered. Flexbox is different: it controls the _relationship_ between a parent and its children — how they're spaced, aligned, and ordered relative to each other. It's the natural next step once individual box behavior is understood.

---

## 2. Container and Items

Flexbox always works on a parent-child relationship:

- The **parent** becomes a flex container by setting `display: flex`.
- Every **direct child** of that container automatically becomes a flex item and is laid out according to the container's rules.
- Grandchildren are _not_ automatically affected — only direct children respond to the flex context.

Once `display: flex` is applied, children immediately stop stacking vertically (block behavior) and instead line up in a row.

---

## 3. The Two Axes

Flexbox layout logic is built around two perpendicular axes:

- **Main axis**: the primary direction items flow along. Horizontal by default (`flex-direction: row`).
- **Cross axis**: perpendicular to the main axis. Vertical by default.

This distinction matters because the two most important alignment properties each target a different axis:

| Property          | Controls                     | Default Axis |
| ----------------- | ---------------------------- | ------------ |
| `justify-content` | Main axis alignment/spacing  | Horizontal   |
| `align-items`     | Cross axis alignment/spacing | Vertical     |

---

## 4. `justify-content`

Distributes items along the main axis.

- `justify-content: center` — groups all items together in the center.
- `justify-content: space-between` — pushes the first and last items to the edges, evenly spacing the rest.

---

## 5. `align-items`

Aligns items along the cross axis. Requires the container to have height to visibly demonstrate the effect (a flex row with no defined height has nothing to center against vertically).

`align-items` has a default value even when never explicitly set: `stretch`. This means flex items automatically expand to fill the entire cross axis _if the container has a defined size on that axis_.

This is easy to miss in `row` layouts, since the cross axis (vertical) rarely has a fixed height. It becomes obvious in `column` layouts once the container has a fixed `width`, since the cross axis is now horizontal — items will stretch full-width unless `align-items` is explicitly overridden (e.g. `align-items: flex-start`).

---

## 6. `flex-direction`

Changes which axis is the main axis.

- `flex-direction: row` (default) — main axis is horizontal.
- `flex-direction: column` — main axis becomes vertical.

**Critical detail:** switching to `column` doesn't just change the direction items flow — it **swaps the roles** of `justify-content` and `align-items`. In column mode, `justify-content` now controls vertical spacing, and `align-items` controls horizontal spacing.

---

## Key Takeaways

- `display: flex` only affects direct children — nested elements deeper than one level are unaffected until they get their own `display: flex`.
- The main axis is horizontal by default; `flex-direction: column` flips it to vertical.
- `justify-content` and
