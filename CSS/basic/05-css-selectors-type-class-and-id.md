# CSS Selectors: Type, Class, and ID

Selectors tell CSS which HTML elements to style. Alongside the **Type Selector**, you can use **ID** and **Class** selectors to target specific elements.

---

## 1. Type Selector

Selects **all** HTML elements of a certain tag name (like `p`, `h1`, or `body`).

```css
p {
  background-color: lightgray;
  color: black;
}
```

---

## 2. ID Selector (`#`)

Selects **one unique element** on the page. An ID name should only be used **once** per page.

**HTML:** Add the `id` attribute to the element:

```html
<p id="red-paragraph">This paragraph is unique.</p>
```

**CSS:** Start with a hashtag `#` followed by the ID name:

```css
#red-paragraph {
  color: red;
}
```

* **Naming Rules:** Do not use spaces, start with a number, or include symbols like `#` or `.` inside the ID name (stick to normal letters and hyphens).

---

## 3. Class Selector (`.`)

Selects **multiple elements** that share the same class. You can reuse a class on as many elements as you want, and one element can have **multiple classes** separated by a space.

**HTML:** Add the `class` attribute to one or more elements:

```html
<p class="green-element">First green text</p>
<p class="green-element gray-background">Green text with gray background</p>
```

**CSS:** Start with a period `.` followed by the class name:

```css
.green-element {
  color: green;
}

.gray-background {
  background-color: gray;
}
```

---

## Specificity (Which Rule Wins?)

When two CSS rules conflict on the same element, the selector with **higher specificity** generally wins:

1. **ID Selector (`#`)** — *Highest specificity*
2. **Class Selector (`.`)** — *Medium specificity*
3. **Type Selector (`p`)** — *Lowest specificity*

> **Example:** If a `<p>` tag has both `id="red-paragraph"` (`color: red`) and `class="green-element"` (`color: green`), the text will be **red** because an ID selector has higher specificity than a class selector.

**Note:** Specificity is not the only factor in the CSS cascade. If competing rules have equal specificity, other cascade rules—such as source order—can determine which one applies.
