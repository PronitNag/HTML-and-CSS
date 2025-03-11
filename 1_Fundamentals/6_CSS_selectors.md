# CSS Selectors

## Introduction
CSS selectors are patterns used to select and style HTML elements. They determine which elements a CSS rule applies to and allow for precise styling control.

## 1. Basic Selectors
These are the simplest selectors used to target elements directly.

### a) Universal Selector (`*`)
Selects all elements in the document.
```css
* {
  margin: 0;
  padding: 0;
}
```

### b) Element Selector
Targets elements by their tag name.
```css
p {
  font-size: 16px;
}
```

### c) Class Selector (`.`)
Targets elements with a specific class.
```css
.button {
  background-color: blue;
}
```

### d) ID Selector (`#`)
Targets a single element with a specific ID.
```css
#header {
  color: red;
}
```

## 2. Grouping Selectors
Allows styling multiple elements at once by separating them with a comma.
```css
h1, h2, h3 {
  font-family: Arial, sans-serif;
}
```

## 3. Combinator Selectors
Used to define relationships between elements.

### a) Descendant Selector (Space)
Targets elements inside another element.
```css
div p {
  color: gray;
}
```

### b) Child Selector (`>`)
Targets direct children only.
```css
ul > li {
  list-style-type: square;
}
```

### c) Adjacent Sibling Selector (`+`)
Targets the next sibling element.
```css
h1 + p {
  font-weight: bold;
}
```

### d) General Sibling Selector (`~`)
Targets all siblings after the given element.
```css
h1 ~ p {
  color: blue;
}
```

## 4. Attribute Selectors
Select elements based on their attributes.

### a) Attribute Exists (`[attribute]`)
```css
input[disabled] {
  background-color: gray;
}
```

### b) Attribute Equals (`[attribute="value"]`)
```css
a[target="_blank"] {
  color: red;
}
```

### c) Attribute Starts With (`[attribute^="value"]`)
```css
input[type^="text"] {
  border: 1px solid black;
}
```

### d) Attribute Ends With (`[attribute$="value"]`)
```css
a[href$=".pdf"] {
  color: green;
}
```

### e) Attribute Contains (`[attribute*="value"]`)
```css
div[class*="box"] {
  padding: 10px;
}
```

## 5. Pseudo-Classes
Define styles based on an element's state.
```css
a:hover {
  color: orange;
}
```

## 6. Pseudo-Elements
Target specific parts of an element.
```css
p::first-line {
  font-weight: bold;
}
```

## Conclusion
CSS selectors provide a powerful way to style web pages efficiently. Understanding different types of selectors helps in writing clean and maintainable CSS code.


