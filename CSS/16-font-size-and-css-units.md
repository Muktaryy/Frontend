# Font Size & CSS Units (`px`, `pt`, `em`, `rem`)

CSS provides several font-related properties, including **`font-size`**, **`font-family`**, **`font-style`**, and **`font-weight`**. The **`font-size`** property controls how large or small text appears.

---

## 1. Absolute Units

Absolute CSS units have fixed conversion relationships to one another. Their physical size on a screen can still vary depending on display scaling and device settings.

### Pixels (`px`)

* A CSS pixel is a reference unit, not necessarily one physical screen pixel.
* For CSS absolute-unit conversions, `1px` equals `1/96` of an inch.
* Commonly used for widths, heights, margins, padding, and font sizes.

### Points (`pt`)

* A point is commonly used in print and word-processing applications.
* `1pt` equals `1/72` of an inch.
* Therefore, `1pt` equals `4/3px`, and `12pt` equals `16px`.

```css
p {
  font-size: 25pt;
}
```

**Default note:** The browser's root element (`html`) typically has a default font size of `16px` (`12pt`). Individual elements may have different default sizes because of browser styles.

---

## 2. Relative Units

Relative units are based on another value, such as a font size or viewport dimension. They are useful for flexible and responsive layouts.

### `em` — Relative to Font Size

The meaning of `em` depends on which property uses it:

* When used for **`font-size`**, `1em` is relative to the parent element's computed font size.
* When used for properties like **`padding`** or **`margin`**, `1em` is relative to the element's own computed font size.

```css
div {
  font-size: 10pt;
}

div p {
  font-size: 2em; /* 2 × 10pt = 20pt */
}

.box {
  font-size: 20px;
  padding: 2em; /* 2 × 20px = 40px */
}
```

### `rem` — Root em

* `rem` is relative to the computed font size of the root element (`html`).
* By default, the root font size is typically `16px` (`12pt`), so `1rem` is usually `16px`.
* Changing the root font size changes the size represented by `rem` throughout the page.

```css
html {
  font-size: 18pt;
}

h1 { font-size: 3rem; }   /* 3 × 18pt = 54pt */
h2 { font-size: 2rem; }   /* 2 × 18pt = 36pt */
h3 { font-size: 1.5rem; } /* 1.5 × 18pt = 27pt */
p  { font-size: 1rem; }   /* 1 × 18pt = 18pt */
```

---

## 3. Why Use `rem`?

* **Consistent scaling:** You can define a base font size on the root element and size other text using `rem`.
* **Maintainable styles:** Changing the root font size can scale many elements together while keeping their proportions.
* **Accessibility:** Relative units can work well with users' browser font-size preferences when used thoughtfully.

However, changing the root font size is not the only way to make typography responsive. You can also use media queries or the `clamp()` function.

### Responsive Font Size with `clamp()`

`clamp(minimum, preferred, maximum)` lets a value grow or shrink within set limits.

```css
h1 {
  font-size: clamp(2rem, 5vw, 4rem);
}
```

Here, the font size scales with the viewport width but never goes below `2rem` or above `4rem`.

---

**Remember:** Use `em` when you want sizing to relate to an element's font size, and `rem` when you want sizing to relate to the root font size. Choose units based on the behavior you want.
