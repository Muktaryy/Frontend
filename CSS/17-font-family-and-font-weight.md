# Font Family & Font Weight in CSS

Alongside `font-size`, two essential CSS text properties are **`font-family`** (which chooses the typeface) and **`font-weight`** (which controls how thick or thin text appears). Another useful property is **`font-style`**, which controls italic or oblique text.

---

## 1. `font-family` (Choosing a Font)

The **`font-family`** property defines the typeface used for text, such as `Arial`, `Verdana`, `Georgia`, or `Tahoma`.

### Font Names with Multiple Words

If a font name contains spaces, put it in quotation marks:

```css
p {
  font-family: "Times New Roman";
}
```

Single-word font names generally do not need quotation marks.

### Fallback Fonts (Backup Fonts)

Not every computer or device has the same fonts installed. To provide alternatives, list font names separated by commas. The browser tries the first font and moves to the next if it cannot use the previous one.

```css
p {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
```

### Generic Font Families

It is good practice to finish a font list with a generic family so the browser can choose a suitable font if the named fonts are unavailable.

* **`sans-serif`:** Fonts without small finishing strokes at the ends of letters (for example, Arial).
* **`serif`:** Fonts with small finishing strokes at the ends of letters (for example, Times New Roman).
* **`monospace`:** Characters have the same fixed width; useful for code.
* **`cursive`:** Handwriting-style fonts.
* **`fantasy`:** Decorative or stylized display fonts.

---

## 2. Using Custom Fonts with Google Fonts

You can load web fonts from services such as [Google Fonts](https://fonts.google.com/) instead of relying only on fonts installed on a visitor's device.

1. Choose a font and select the weights you need.
2. Open the embed instructions and copy the provided HTML link.
3. Place the link inside the `<head>` section of your HTML document.

Example using Roboto with weights 400 and 700:

```html
<head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
</head>
```

Then apply the font in your CSS:

```css
p {
  font-family: "Roboto", sans-serif;
  font-weight: 400;
}
```

---

## 3. `font-weight` (Text Thickness / Boldness)

The **`font-weight`** property controls how thick or thin text appears.

### Keyword Values

* **`normal`:** Normal text weight; equivalent to `400`.
* **`bold`:** Bold text; equivalent to `700`.

```css
p {
  font-weight: bold;
}

h1 {
  font-weight: normal;
}
```

### Numeric Values

You can use numeric values from **`100`** to **`900`** to request different font weights.

* **`100`:** Thin
* **`200`:** Extra light
* **`300`:** Light
* **`400`:** Normal
* **`500`:** Medium
* **`600`:** Semi-bold
* **`700`:** Bold
* **`800`:** Extra bold
* **`900`:** Black / heaviest

The exact appearance depends on the font. A font may not provide every weight, so the browser uses an available weight according to CSS font matching rules.

```css
p {
  font-weight: 100;
}
```

### Relative Values: `lighter` and `bolder`

These keywords choose a lighter or heavier weight relative to the parent's computed font weight.

They do **not** simply subtract or add 300. CSS uses predefined weight mappings to choose the relative weight.

```css
.parent {
  font-weight: 400;
}

.child {
  font-weight: bolder;
}
```

The child will use a heavier weight relative to its parent. The exact result depends on the parent's weight and the available font weights.

---

## 4. `font-style` (Normal, Italic, and Oblique)

The **`font-style`** property controls whether text is displayed in a normal or slanted style.

Common values:

* **`normal`:** Regular, upright text.
* **`italic`:** Uses an italic typeface style when available.
* **`oblique`:** Displays a slanted version of the text.

```css
p {
  font-style: italic;
}
```

---

**Remember:** `font-family` chooses the typeface, `font-weight` controls its thickness, and `font-style` controls whether it is normal or slanted.
