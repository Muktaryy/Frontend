# Borders in CSS

To add a border around an HTML element, CSS combines **three main properties**: `border-width`, `border-style`, and `border-color`.

---

## 1. The Three Border Properties

```css
div {
  width: 400px;
  height: 400px;
  background-color: blue;

  border-width: 10px;
  border-style: solid;
  border-color: tomato;
}
```

* **`border-width`:** Controls the thickness of the border (e.g., `10px`).
* **`border-style`:** Sets the line style of the border. **This is essential**—the default is `none`, so a border will not appear unless you set a visible border style.
* **`border-color`:** Changes the color of the border. If you do not set one, it generally uses `currentColor` (the element's text color).

---

## 2. Common `border-style` Values

You do not need to memorize every style—you can always look them up on **MDN Web Docs**. Here are some common ones:

* **`solid`:** A single solid line.
* **`dashed`:** A series of short dashed lines.
* **`dotted`:** Evenly spaced dots along the edge.
* **`double`:** Two parallel lines with a small gap between them.
* **`groove`:** Creates a 3D carved or engraved look.

---

## 3. Styling Individual Sides (Exercise Solution)

You can style each side of an element separately using `top`, `right`, `bottom`, and `left` (for example, `border-left-style` or `border-right-color`).

```css
.border-exercise {
  width: 400px;
  height: 400px;
  background-color: chocolate;

  border-width: 10px;
  border-left-style: dashed;
  border-top-style: dotted;
  border-right-style: solid;
  border-bottom-style: double;
  border-right-color: cornflowerblue;
}
```

You can also use shorthand properties such as `border-left`, `border-top`, `border-right`, and `border-bottom`.

* **Tip:** Searching documentation (like **MDN Web Docs**) when you need a specific property is one of the most important habits for any programmer.
