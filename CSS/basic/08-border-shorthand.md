# The CSS `border` Shorthand Property

Instead of writing three separate properties (`border-width`, `border-style`, and `border-color`) every time you add a border, CSS lets you combine them into **one single line** using the **`border`** shorthand property.

---

## Long Way vs. Shorthand

### 1. The Long Way (3 Properties)

```css
div {
  border-width: 5px;
  border-style: solid;
  border-color: black;
}
```

### 2. The Shorthand Way (1 Property)

```css
div {
  border: 5px solid black;
}
```

---

## How It Works

The **`border`** property sets all three values at once in one place:

* **`5px`** — sets the `border-width` (thickness)
* **`solid`** — sets the `border-style` (line type)
* **`black`** — sets the `border-color` (color)

Both examples produce the same result, keeping your CSS code shorter, cleaner, and easier to read.

## Important Details

* The values do not have to be written in a fixed order. For example, `border: solid black 5px;` also works.
* If you leave out a value, its corresponding initial value is used.
