# CSS Padding & The Box Model

**Padding** is the space **inside** an element, between its edge (border) and its content. While `margin` creates space *outside* an element, `padding` pushes the content *inwards*.

---

## 1. Adding Padding

When you add padding to an element, two things happen:
1. The content moves inward, creating a gap between the text/content and the border.
2. By default, the element's total size gets bigger to make room for that inner space.

```css
div {
  width: 300px;
  height: 50px;
  margin: 20px;
  padding: 20px; /* Adds 20px space inside on all 4 sides */
}
```

### Padding on Individual Sides

Just like margin, you can set padding for specific sides (`padding-top`, `padding-right`, `padding-bottom`, and `padding-left`):

```css
div {
  width: 300px;
  height: 50px;
  padding-top: 100px;
  padding-left: 120px;
  padding-right: 90px;
  padding-bottom: 50px;
}
```

---

## 2. The CSS Box Model

Every HTML element is wrapped in a rectangular box that defines how much space it takes up on the page.

From the inside out, the Box Model has **four parts**:
1. **Content:** The actual text, image, or media inside the element.
2. **Padding:** The space between the content and the border.
3. **Border:** The line surrounding the padding and content.
4. **Margin:** The space outside the border that separates the element from other elements.

---

## 3. How Element Size Is Calculated

By default, the `width` and `height` properties set only the size of the content area, not the entire box. To find the element's total size, add the content, padding, and borders together.

### Example Calculation

Suppose a `<div>` has the following styles:

```css
div {
  width: 300px;
  height: 50px;
  padding-top: 100px;
  padding-bottom: 50px;
  padding-left: 120px;
  padding-right: 90px;
  border: 10px solid black;
}
```

* **Total Width:** `300px` (content) + `120px` (left padding) + `90px` (right padding) + `10px` (left border) + `10px` (right border) = **`530px`**
* **Total Height:** `50px` (content) + `100px` (top padding) + `50px` (bottom padding) + `10px` (top border) + `10px` (bottom border) = **`220px`**

## 4. The `box-sizing` Property

The `box-sizing` property controls how the `width` and `height` of an element are calculated.

With `box-sizing: border-box`, the specified width and height include the content, padding, and border. The total size stays within the dimensions you set.

```css
div {
  box-sizing: border-box;
  width: 300px;
  padding: 20px;
  border: 5px solid black;
}
```

In this example, the total width remains **300px**, including the padding and borders.

> **Tip (Web Inspector):** Right-click any element in your browser and select **Inspect** to view a visual diagram of its Box Model and exact pixel measurements.
