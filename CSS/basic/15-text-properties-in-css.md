# Text Properties in CSS

Besides `color`, CSS provides several properties to control how text is aligned, decorated, and capitalized. Three common properties are **`text-align`**, **`text-decoration`**, and **`text-transform`**.

---

## 1. `text-align` (Horizontal Alignment)

The **`text-align`** property controls the horizontal alignment of inline content, such as text, inside an element.

* **`left`:** Aligns text to the left.
* **`center`:** Centers text horizontally.
* **`right`:** Aligns text to the right.
* **`justify`:** Adjusts spacing between words so lines (except usually the last line) fill the available width.
* **`start`:** Aligns text to the start of the writing direction.
* **`end`:** Aligns text to the end of the writing direction.

```css
.left {
  text-align: left;
}

.center {
  text-align: center;
}

.right {
  text-align: right;
}

p {
  text-align: justify;
}
```

**Note:** Alignment is relative to the element's content area, not necessarily the whole screen. If you change the element's width, the available space for alignment changes too. The default alignment depends on the writing direction; in left-to-right text, it is usually left.

---

## 2. `text-decoration` (Lines on Text)

The **`text-decoration`** property adds or removes decorative lines on text.

### Line Types

* **`underline`:** Places a line below the text.
* **`overline`:** Places a line above the text.
* **`line-through`:** Draws a line through the text.
* **`none`:** Removes text decoration lines.

### Shorthand Styling

The `text-decoration` shorthand can set the line, style, color, and thickness. The line is optional in the CSS shorthand syntax, and the other values can be supplied as needed.

Common styles include `solid`, `double`, `dotted`, `dashed`, and `wavy`.

```css
h4 {
  text-decoration: underline wavy red 5px;
}
```

You can also control the parts separately:

```css
h4 {
  text-decoration-line: underline;
  text-decoration-style: wavy;
  text-decoration-color: red;
  text-decoration-thickness: 5px;
}
```

### Removing Underlines from Links (`<a>`)

Links are commonly underlined by default in browsers. You can remove that decoration with:

```css
a {
  text-decoration: none;
}
```

---

## 3. `text-transform` (Capitalization)

The **`text-transform`** property changes how text is displayed without changing the original text in the HTML or data source.

* **`uppercase`:** Displays letters in uppercase.
* **`lowercase`:** Displays letters in lowercase.
* **`capitalize`:** Displays the first character of each word in uppercase.

```css
p {
  text-transform: uppercase;
}
```

**Note:** `capitalize` changes the first character of each word; it does not necessarily make the remaining characters lowercase.

---

**Remember:** These properties change how text is presented. They do not rewrite the original text content in your HTML.
