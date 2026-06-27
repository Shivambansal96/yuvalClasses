# CSS Pseudo Selectors

## 1. What are Pseudo Selectors?

Pseudo selectors allow you to style an element based on its **state**, **position**, or **specific part**.

There are two types:

- **Pseudo Classes (`:`)** – Style an element based on its state.
- **Pseudo Elements (`::`)** – Style a specific part of an element.

### Syntax

```css
selector:pseudo-class {
  /* styles */
}

selector::pseudo-element {
  /* styles */
}
```

---

# 2. Common Pseudo Classes

## User Interaction

### `:hover`

Applies styles when the mouse pointer is over an element.

```css
button:hover {
  background-color: blue;
}
```

---

### `:active`

Applies styles while the element is being clicked.

```css
button:active {
  transform: scale(0.95);
}
```

---

### `:focus`

Applies styles when an input or interactive element is focused.

```css
input:focus {
  border: 2px solid blue;
}
```

---

# 3. Link Pseudo Classes

```css
a:link {
  color: blue;
}

a:visited {
  color: purple;
}

a:hover {
  color: red;
}

a:active {
  color: orange;
}
```

### Order to Remember

```
Link → Visited → Hover → Active
```

---

# 4. Form Pseudo Classes

## `:required`

```css
input:required {
  border: 2px solid red;
}
```

---

## `:disabled`

```css
input:disabled {
  background-color: lightgray;
}
```

---

## `:checked`

```css
input:checked {
  accent-color: green;
}
```

---

## `:valid`

```css
input:valid {
  border: 2px solid green;
}
```

---

## `:invalid`

```css
input:invalid {
  border: 2px solid red;
}
```

---

# 5. Structural Pseudo Classes

## `:first-child`

```css
li:first-child {
  color: blue;
}
```

---

## `:last-child`

```css
li:last-child {
  color: red;
}
```

---

## `:nth-child()`

Second child

```css
li:nth-child(2) {
  color: green;
}
```

Even rows

```css
li:nth-child(even) {
  background: #f2f2f2;
}
```

Odd rows

```css
li:nth-child(odd) {
  background: white;
}
```

Every third element

```css
li:nth-child(3n) {
  font-weight: bold;
}
```

---

## `:only-child`

```css
p:only-child {
  color: purple;
}
```

---

## `:first-of-type`

```css
p:first-of-type {
  color: teal;
}
```

---

## `:last-of-type`

```css
p:last-of-type {
  color: orange;
}
```

---

# Difference

## `:first-child`

Selects the first child regardless of element type.

```css
p:first-child
```

---

## `:first-of-type`

Selects the first `<p>` among its siblings.

```css
p:first-of-type
```

---

# 6. Negation

## `:not()`

```css
button:not(.primary) {
  background: gray;
}
```

Useful for excluding specific elements.

---

# 7. Pseudo Elements

Pseudo elements use **double colons (`::`)**.

---

## `::before`

Adds content before an element.

```css
p::before {
  content: "👉 ";
}
```

---

## `::after`

Adds content after an element.

```css
p::after {
  content: " ✔";
}
```

---

## `::first-letter`

Styles the first letter.

```css
p::first-letter {
  font-size: 2rem;
  color: red;
}
```

---

## `::first-line`

Styles the first line of text.

```css
p::first-line {
  font-weight: bold;
}
```

---

## `::selection`

Styles selected text.

```css
::selection {
  background: yellow;
  color: black;
}
```

---

## `::placeholder`

Styles placeholder text.

```css
input::placeholder {
  color: gray;
}
```

---

# 8. Combining Selectors

```css
nav a:hover {
  color: red;
}

ul li:first-child {
  font-weight: bold;
}

.card:hover img {
  transform: scale(1.1);
}

input:focus::placeholder {
  color: transparent;
}
```

---

# 9. Real-World Examples

### Button Hover

```css
button:hover {
  background: royalblue;
  color: white;
}
```

---

### Zebra Table

```css
tr:nth-child(even) {
  background: #f2f2f2;
}
```

---

### Decorative Icon

```css
h2::before {
  content: "⭐ ";
}
```

---

### Required Fields

```css
input:required {
  border-left: 4px solid red;
}
```

---

### Tooltip

```css
.tooltip::after {
  content: "Hover me!";
}
```

---

# 10. Common Mistakes

- Forgetting the `content` property with `::before` and `::after`
- Confusing `:` with `::`
- Mixing up `:first-child` and `:first-of-type`
- Incorrect `:nth-child()` formulas

---

# Lesson Plan (60–90 Minutes)

1. Introduction to Pseudo Selectors
2. User Interaction Pseudo Classes
3. Link Pseudo Classes
4. Structural Pseudo Classes
5. Form Pseudo Classes
6. `:not()`
7. Pseudo Elements
8. Practical Examples
9. Hands-on Exercises

---

# Practice Exercises

### Exercise 1

Change a button's background color when hovered.

---

### Exercise 2

Highlight the first and last items in a list.

---

### Exercise 3

Apply alternating colors to table rows using `:nth-child()`.

---

### Exercise 4

Add a ⭐ before every heading using `::before`.

---

### Exercise 5

Style the first letter of every paragraph.

---

### Exercise 6

Change the placeholder text color of an input field.

---

### Exercise 7

Style checked checkboxes differently.

---

### Exercise 8

Create a card that grows slightly when hovered.