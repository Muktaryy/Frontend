# The CSS Universal Selector (`*`)

The **universal selector** is represented by the asterisk symbol (`*`). It selects **every HTML element** in the document.

---

## Why Use the Universal Selector?

Web browsers apply built-in default styles to many HTML elements. For example:

* The `<body>` commonly has a default margin of **`8px`**.
* Headings (`<h1>`–`<h6>`) and paragraphs (`<p>`) commonly have default margins.
* Lists (`<ul>` and `<ol>`) commonly have default margins and left padding.

These default styles can create unexpected spacing and make layouts harder to control.

---

## Resetting Default Spacing

At the beginning of a web project, developers often use the universal selector (`*`) to remove default margins and padding so they can define their own spacing:

```css
* {
  margin: 0;
  padding: 0;
}
```

* **`*`:** Targets all elements in the document.
* **`margin: 0; padding: 0;`:** Removes margins and padding, allowing you to define your own spacing.

The universal selector only resets the properties you specify. It does not remove every browser default style.

---

## A More Complete Reset

You can also include pseudo-elements such as `::before` and `::after` in the reset:

```css
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

This applies the reset to all elements and their `::before` and `::after` pseudo-elements, and makes width and height calculations more predictable.
