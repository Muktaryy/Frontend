# The CSS `display` Property (`block`, `inline`, `inline-block`)

The **`display`** property controls how an HTML element is displayed in the page layout. It lets you override an element's default behavior—for example, turning an inline element into a block element, or vice versa.

---

## 1. Limitations of Default `inline` Elements

Ordinary inline elements (like `<span>` or `<a>`) are designed to sit inside a line of text. Because of this, some CSS properties behave differently on them:

* **Vertical margins (`margin-top`, `margin-bottom`):** They do not affect the spacing between lines in the normal inline layout. They may extend visually, but they do not push other lines apart.
* **`width` and `height`:** Do not apply to ordinary non-replaced inline elements.

Horizontal margins (`margin-left` and `margin-right`) do affect spacing between inline elements.

```css
span {
  width: 100px;       /* Does not apply to an ordinary inline span */
  height: 100px;      /* Does not apply to an ordinary inline span */
  margin-top: 100px;  /* Does not change the spacing between lines */
  margin-left: 20px;  /* Works */
}
```

---

## 2. Changing Display Values

### `display: block;`

Turns an inline element (like `<span>`) into a block-level box:

* Starts on a **new line**.
* With `width: auto`, normally fills the available width of its parent.
* Respects **`width`**, **`height`**, and all margins, including top and bottom.

```css
span {
  display: block;
  width: 100px;
  height: 100px;
  margin-top: 50px; /* Works */
}
```

### `display: inline;`

Turns a block element (like `<div>` or `<p>`) into an inline-level box:

* Sits alongside other inline content when there is enough space.
* For ordinary non-replaced inline elements, `width` and `height` do not apply.
* Vertical margins do not change the spacing between lines.

```css
div {
  display: inline;
}
```

### `display: inline-block;` (Best of Both Worlds)

Combines features of inline and block:

* **Behaves like inline:** Sits alongside other inline-level content when there is enough space.
* **Behaves like block for sizing:** Respects `width`, `height`, padding, and vertical margins.
* Its width is `auto` by default, so it generally sizes to its content, but you can also set an explicit width.

```css
p {
  display: inline-block;
  width: 150px;
  height: 80px;
  margin-top: 20px;
}
```

* **Common Use Case:** Useful for styling links or other elements so they can sit next to each other while having custom dimensions and spacing.

---

## Summary Comparison

| Property / Behavior | `block` | `inline` | `inline-block` |
| :--- | :--- | :--- | :--- |
| **Starts on a new line?** | Yes, normally | No, normally | No, normally |
| **Default width behavior** | Fills available width when width is `auto` | Fits inline content | Usually sizes to content |
| **Can set `width` and `height`?** | Yes | No, for ordinary non-replaced inline elements | Yes |
| **Vertical margins affect layout?** | Yes | No, not line spacing | Yes |
| **Horizontal margins affect spacing?** | Yes | Yes | Yes |

**Remember:** These are common display behaviors. CSS has other display values too, including `flex`, `grid`, and `none`.
