# Colors in CSS

CSS allows you to change the colors of text, backgrounds, borders, and other HTML elements.

## 1. Text Color (`color`)

The `color` property changes the color of an element's text.

```css
p {
  color: red;
}
```

## 2. Background Color (`background-color`)

The `background-color` property changes the background color of an element.

```css
body {
  background-color: lightblue;
}
```

## 3. Named Colors

CSS supports predefined color names that you can use directly.

```css
h1 {
  color: tomato;
}

p {
  color: purple;
}
```

Examples: `red`, `blue`, `green`, `black`, `white`, `orange`, and `tomato`.

## 4. RGB Colors

RGB stands for **Red, Green, Blue**.

It uses three numbers to define a color:

```css
h1 {
  color: rgb(255, 0, 0);
}
```

Each value ranges from `0` to `255`:
- First value: Red
- Second value: Green
- Third value: Blue

Examples:

```css
p {
  color: rgb(0, 0, 255); /* Blue */
}

h2 {
  color: rgb(0, 128, 0); /* Green */
}
```

You can also use `rgba()` to control transparency with an alpha value between `0` (fully transparent) and `1` (fully opaque).

```css
div {
  background-color: rgba(255, 0, 0, 0.5);
}
```

## 5. HEX Colors

HEX stands for **Hexadecimal**. It represents colors using six hexadecimal digits, starting with `#`.

```css
h1 {
  color: #ff0000;
}
```

A HEX color has this structure:

- First two digits: Red
- Next two digits: Green
- Last two digits: Blue

Examples:

```css
p {
  color: #0000ff; /* Blue */
}

h2 {
  color: #008000; /* Green */
}
```

## 6. HSL Colors

HSL stands for **Hue, Saturation, Lightness**.

```css
h1 {
  color: hsl(0, 100%, 50%);
}
```

- **Hue:** The color itself, measured in degrees from `0` to `360`.
- **Saturation:** The intensity of the color, expressed as a percentage.
- **Lightness:** How light or dark the color is, expressed as a percentage.

## Tip: VS Code Color Picker

In VS Code, you can click the colored square that appears next to a CSS color value to open the color picker. It lets you choose colors visually and switch between color formats.
