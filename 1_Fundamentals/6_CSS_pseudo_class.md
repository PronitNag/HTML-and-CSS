# CSS Pseudo-Classes

## Introduction
CSS pseudo-classes allow you to apply styles to elements based on their state, position, or interaction with the user. They help target elements dynamically without modifying the HTML structure.

## Syntax
A pseudo-class is added to a selector using a colon (`:`):

```css
selector:pseudo-class {
  property: value;
}
```

For example:

```css
a:hover {
  color: red;
}
```

## Common Pseudo-Classes

### 1. User Interaction
- `:hover` – Styles an element when the mouse is over it.
- `:focus` – Styles an element when it gains focus (like a clicked input field).
- `:active` – Styles an element when it is being clicked.

Example:

```css
button:hover {
  background-color: blue;
}
```

### 2. Structural Pseudo-Classes
- `:first-child` – Selects the first child of a parent.
- `:last-child` – Selects the last child of a parent.
- `:nth-child(n)` – Selects the nth child of a parent.
- `:nth-of-type(n)` – Selects the nth child of a specific type.
- `:only-child` – Selects an element that is the only child of its parent.

Example:

```css
p:first-child {
  font-weight: bold;
}
```

### 3. Form Pseudo-Classes
- `:checked` – Targets checked checkboxes or radio buttons.
- `:disabled` – Targets disabled form elements.
- `:enabled` – Targets enabled form elements.
- `:required` – Targets required input fields.

Example:

```css
input:required {
  border: 2px solid red;
}
```

### 4. Link Pseudo-Classes
- `:link` – Styles unvisited links.
- `:visited` – Styles visited links.
- `:hover` – Styles links when hovered over.
- `:active` – Styles links when clicked.

Example:

```css
a:visited {
  color: purple;
}
```

### 5. Negation
- `:not(selector)` – Excludes elements that match the selector.

Example:

```css
div:not(.special) {
  background-color: gray;
}
```

## Conclusion
Pseudo-classes are a powerful tool for styling elements dynamically based on their state, position, or interaction. By leveraging them, you can create more engaging and interactive web pages.


