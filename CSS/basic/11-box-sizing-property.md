# The CSS `box-sizing` Property

The **`box-sizing`** property controls how the browser calculates the **total width and height** of an element.

---

## The Two Values of `box-sizing`

### 1. `content-box` (Default)

This is the default value of the `box-sizing` property. The `width` and `height` apply only to the **content area**. Any padding or border you add is placed outside the content area, making the element bigger.

* **Total Width** = `width` + left/right padding + left/right border
* **Total Height** = `height` + top/bottom padding + top/bottom border

```css
.content-box {
  box-sizing: content-box; /* Default value */
  width: 200px;
  height: 50px;
  padding: 20px;
  border: 10px solid black;
  /* Actual size: 260px wide x 110px tall */
}
```

---

### 2. `border-box` (Recommended)

When you set `box-sizing: border-box;`, the padding and border are **included inside** the `width` and `height` you set. They take up space within those dimensions instead of making the box bigger.

* **Total Width** = the specified `width` (includes padding and borders)
* **Total Height** = the specified `height` (includes padding and borders)

```css
.border-box {
  box-sizing: border-box;
  width: 200px;
  height: 50px;
  padding: 20px;
  border: 10px solid black;
  /* Actual size: stays exactly 200px wide x 50px tall */
}
```

With `border-box`, the content area becomes smaller to make room for the padding and border.

---

## Why Use `border-box`?

* **Predictable Sizing:** Elements keep the exact width and height you give them, even when you add padding or borders.
* **Easier Responsive Design:** Helps prevent layouts from breaking due to unexpected size increases.

## Common CSS Reset

Many developers apply `border-box` to all elements and their pseudo-elements:

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

This makes element sizing more predictable throughout the page.
