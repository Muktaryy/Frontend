# How to Add CSS to HTML

There are **three ways** to add CSS to an HTML document.

## 1. Inline CSS

Inline CSS is written directly inside an HTML element using the `style` attribute.

```html
<p style="color: red;">Hello World!</p>
```

**Advantages:**
- Quick to use for testing.
- Useful for styling a single element.

**Disadvantages:**
- Makes HTML harder to read.
- Difficult to maintain when styling many elements.
- Not reusable.

## 2. Internal CSS

Internal CSS is written inside a `<style>` element in the HTML document's `<head>` section.

```html
<!DOCTYPE html>
<html>
<head>
  <style>
    p {
      color: blue;
    }
  </style>
</head>
<body>
  <p>Hello World!</p>
</body>
</html>
```

**Advantages:**
- Keeps CSS separate from the HTML elements.
- Useful for styling a single page.

**Disadvantages:**
- The CSS only applies to that HTML document.
- Can make the HTML file larger and harder to maintain.

## 3. External CSS

External CSS is written in a separate `.css` file and connected to HTML using the `<link>` element.

**HTML file (`index.html`):**

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <p>Hello World!</p>
</body>
</html>
```

**CSS file (`style.css`):**

```css
p {
  color: green;
}
```

**Advantages:**
- Keeps HTML and CSS separate.
- Makes code easier to organize and maintain.
- One CSS file can style multiple HTML pages.
- Browsers can cache the CSS file.

**Disadvantages:**
- Requires an additional file.
- If the CSS file path is incorrect, the styles won't load.

## Quick Comparison

| Method | Where CSS is written | Best use |
|---|---|---|
| Inline | Inside an HTML element | Quick, one-off styling |
| Internal | Inside a `<style>` element | A single page |
| External | In a separate `.css` file | Most websites and projects |

**My recommendation:** Use External CSS for most projects because it keeps your code organized and easier to maintain.
