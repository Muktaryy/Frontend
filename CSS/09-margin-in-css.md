# CSS Margin

**Margin** is the space **outside** the border of an element. It pushes neighboring elements away and creates breathing room around the element.

---

## 1. Adding Margin on All Sides

If multiple elements have no margin, they may touch each other and look like one single block. Using the `margin` property with one value adds equal space on **all four sides** (top, right, bottom, and left).

```css
.box {
  background-color: lightgreen;
  height: 50px;
  margin: 20px; /* Adds 20px space on top, bottom, left, and right */
}
```

* **Tip (Browser DevTools):** Right-click an element, choose **Inspect**, and hover over it in the HTML tree—the **orange** highlight shows the element's margin.

---

## 2. Setting Margin for Individual Sides

You can control each side separately using `margin-top`, `margin-right`, `margin-bottom`, and `margin-left`:

```css
.box {
  margin-top: 20px;
  margin-right: 30px;
  margin-bottom: 50px;
  margin-left: 30px;
}
```

---

## 3. Margin Shorthand

Instead of writing four separate lines, you can combine values into one `margin` property:

### Four Values (Clockwise: Top → Right → Bottom → Left)

```css
.box {
  margin: 20px 30px 50px 30px;
}
```

### Two Values (Top & Bottom | Left & Right)

```css
.box {
  margin: 30px 10px; /* 30px top & bottom, 10px left & right */
}
```

### Three Values (Top | Left & Right | Bottom)

```css
.box {
  margin: 20px 30px 40px;
}
```

---

## 4. Removing the Default `<body>` Margin

Browsers commonly apply an **8px margin** to the `<body>` element, which creates a small gap between the page content and the edges of the screen.

To remove this default gap, set the `body` margin to `0`:

```css
body {
  margin: 0;
}
```

* **Zero Unit Rule:** Whenever a CSS value is `0`, you do not need to write a unit (write `0` instead of `0px`).

## 5. Margin Collapsing

Vertical margins between certain block elements can sometimes collapse into a single margin instead of adding together. For example, when two vertical margins meet, the larger margin may be used rather than their sum.
