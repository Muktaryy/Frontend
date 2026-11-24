# Rounded Corners in CSS (`border-radius`)

The **`border-radius`** property rounds the corners of an HTML element, giving it a softer appearance.

---

## 1. Rounding All Four Corners

When you use one value, all four corners receive the same radius. A larger value generally creates rounder corners.

```css
div {
  width: 200px;
  height: 200px;
  background-color: blue;
  border-radius: 20px;
}
```

* **`5px`:** A subtle curve.
* **`50px`:** More noticeably rounded corners.

---

## 2. Creating a Circle or Oval

Setting `border-radius: 50%` makes the corners fully rounded relative to the element's dimensions.

For a square element, this creates a **perfect circle**:

```css
.circle {
  width: 200px;
  height: 200px;
  background-color: blue;
  border-radius: 50%;
}
```

**Important:**
* The element needs equal width and height to look like a circle.
* If its width and height are different, `border-radius: 50%` creates an **ellipse** instead.
* There is no general 50% maximum for the radius value. If corner radii overlap, the browser proportionally reduces them so they fit within the element.

---

## 3. Rounding Individual Corners

You can control each corner separately with these properties:

* `border-top-left-radius`
* `border-top-right-radius`
* `border-bottom-right-radius`
* `border-bottom-left-radius`

```css
div {
  border-top-left-radius: 90px;
  border-top-right-radius: 60px;
  border-bottom-right-radius: 30px;
  border-bottom-left-radius: 5%;
}
```

---

## 4. The `border-radius` Shorthand

You can use one to four values instead of writing separate properties.

### One value

Applies the same radius to all four corners.

```css
div {
  border-radius: 20px;
}
```

### Two values

The first value applies to the **top-left and bottom-right** corners. The second applies to the **top-right and bottom-left** corners.

```css
div {
  border-radius: 20px 50px;
}
```

### Three values

The values apply in this order:

1. Top-left
2. Top-right and bottom-left
3. Bottom-right

```css
div {
  border-radius: 10px 30px 50px;
}
```

### Four values

The values apply clockwise, starting from the top-left:

**Order:** top-left → top-right → bottom-right → bottom-left

```css
div {
  border-radius: 90px 60px 30px 5%;
}
```

---

**Remember:** `border-radius` can use different units, such as `px` and `%`, and it can round all corners equally or each corner differently.
