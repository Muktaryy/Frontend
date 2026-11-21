# Block vs. Inline Elements in HTML

HTML elements have different default display behaviors. Two common behaviors are **block-level** and **inline-level**. These behaviors are controlled by the CSS `display` property.

---

## 1. Block-Level Elements

A block-level element normally starts on a **new line** and takes up the **available width** of its parent container by default.

* **Stacking Behavior:** Block elements normally appear one below another. Even if you give a block element a smaller `width`, the next block element still starts on a new line.
* **Common Examples:**
  * Headings (`<h1>`–`<h6>`)
  * Paragraphs (`<p>`)
  * Containers (`<div>`)
  * List items (`<li>`)

```html
<h2>First Heading</h2>
<h2>Second Heading</h2>
<!-- Both headings appear stacked one below the other -->
```

---

## 2. Inline-Level Elements

An inline element does **not** normally start on a new line. It sits alongside other inline content and generally takes up only the space its content needs.

* **Sizing Behavior:** For ordinary non-replaced inline elements, setting `width` and `height` does not work as it does on block elements.
* **Common Examples:**
  * Links (`<a>`)
  * Spans (`<span>`)
  * Bold or emphasized text (`<strong>`, `<em>`)

```html
<a href="#">Link 1</a>
<a href="#">Link 2</a>
<span>Some text</span>
<!-- These appear alongside each other when there is enough space -->
```

### A Note About Buttons and Images

Not every element fits neatly into just the block or inline examples:

* **`<button>`:** Normally behaves like an `inline-block` element by default.
* **`<img>`:** Is an inline-level replaced element. Unlike ordinary inline text elements, it supports explicit `width` and `height`.

---

## 3. Inline-Block

The `inline-block` value combines features of inline and block display:

* It sits next to other inline or inline-block elements when there is enough space.
* You can set its `width` and `height`, like a block element.

```css
span {
  display: inline-block;
  width: 150px;
  height: 50px;
}
```

---

## Quick Comparison

| Feature | Block | Inline |
| :--- | :--- | :--- |
| **Starts on a new line?** | Yes, normally | No, normally |
| **Default width behavior** | Fills available parent width | Fits its inline content |
| **Width and height** | Can be set | Ignored for ordinary non-replaced inline elements |
| **Examples** | `<div>`, `<p>`, `<h2>`, `<li>` | `<a>`, `<span>`, `<strong>`, `<em>` |

**Remember:** These are default display behaviors. CSS can change an element's behavior using the `display` property, for example `block`, `inline`, `inline-block`, `flex`, or `grid`.
