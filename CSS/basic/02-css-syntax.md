# CSS Syntax

CSS rules tell the browser how HTML elements should look.

## Basic CSS Syntax

A CSS rule consists of a **selector** and a **declaration block**.

```css
button {
  color: white;
  background-color: blue;
}
```

## Parts of a CSS Rule

- **Selector:** Targets the HTML element you want to style. In this example, `button`.
- **Declaration block:** Everything inside the curly braces `{ }`.
- **Declaration:** A styling instruction inside the declaration block.
- **Property:** What you want to change, such as `color`.
- **Value:** The setting you give to a property, such as `white`.
- **Semicolon (`;`):** Separates declarations.

## Declaration Format

Each declaration follows this format:

```css
property: value;
```

For example:

```css
h1 {
  color: red;
  font-size: 32px;
}
```

Here:
- `color` and `font-size` are properties.
- `red` and `32px` are values.

## CSS Selectors

Selectors tell CSS which HTML elements to target.

Some common selectors include:

- **Type selector:** Selects elements by their HTML tag name, such as `p` or `h1`.
- **Class selector:** Selects elements using a class name, such as `.button`.
- **ID selector:** Selects an element using its ID, such as `#header`.
- **Pseudo-class:** Selects an element in a particular state, such as `button:hover`.

CSS also supports more complex selectors, including combinators.
