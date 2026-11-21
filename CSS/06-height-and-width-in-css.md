# Height and Width in CSS

By default, block elements (like `<div>`) take up the full available width, while their **height** automatically adjusts to fit the content inside them. If a `<div>` is empty and has no height, padding, or border, its height is usually `0` and it may be invisible.

You can control an element's size using the **`width`** and **`height`** properties.

---

## 1. Fixed Size: Pixels (`px`)

Pixels set a specific size that does not automatically change when the browser window is resized.

```css
div {
  background-color: blue;
  width: 400px;
  height: 400px;
}
```

* **Always include a unit:** Writing `width: 400;` without a unit is invalid for a non-zero length.
* **Overflow:** If an element is bigger than the available space, it may overflow its container and cause a scrollbar to appear.

---

## 2. Relative Size: Percentages (`%`)

Percentages (`%`) set an element's size relative to its containing block (often its parent element). This is useful for responsive web design.

```css
div {
  background-color: blue;
  width: 50%; /* Takes up half of the containing block's width */
}
```

### Important Rule for Percentage Height

For `height: 50%;` to resolve as expected, the containing block generally needs a definite height.

* By default, the height of `body` is usually determined by its content, rather than being a fixed height.
* If the parent has a definite height (for example, `height: 500px;`), the child's `height: 50%;` can resolve to `250px`.

```css
body {
  height: 500px;
}

div {
  background-color: blue;
  width: 50%;
  height: 50%; /* Equals 250px */
}
```

---

## Practice Example: Parent and Child `<div>`

**HTML:**

```html
<div class="parent-div">
  <div class="child-div"></div>
</div>
```

**CSS:**

```css
.parent-div {
  background-color: green;
  width: 50%;     /* Resizes dynamically with the window */
  height: 200px;  /* Fixed height so the child can use % height */
}

.child-div {
  background-color: blue;
  width: 150px;   /* Stays a fixed width */
  height: 50%;    /* Equals 100px (50% of the 200px green parent) */
}
```

* **Pixels (`px`):** Specify a fixed CSS length.
* **Percentages (`%`):** Size an element relative to its containing block. The exact reference depends on the property being used.
