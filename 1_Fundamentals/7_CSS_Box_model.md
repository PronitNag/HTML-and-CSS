# Block and Inline Elements

## Block Elements
- Block elements take up the full width of their container.
- They start on a new line.
- Common block elements: `<div>`, `<p>`, `<h1>` - `<h6>`, `<section>`, `<article>`, `<nav>`, `<header>`, `<footer>`, etc.

## Inline Elements
- Inline elements only take up as much width as necessary.
- They do not start on a new line.
- Common inline elements: `<span>`, `<a>`, `<strong>`, `<em>`, `<img>`, `<label>`, `<input>`, etc.

# The Different Boxes That Make Up an Element and How to Style Them

Each HTML element is represented as a rectangular box, consisting of the following parts:

## 1. Width and Height
- The `width` and `height` properties define the dimensions of an element's content area.
- Default behavior: Block elements stretch to the full container width unless specified.

```css
.element {
  width: 200px;
  height: 100px;
}
```

## 2. Margin
- The `margin` property creates space outside the element, separating it from neighboring elements.
- It can be set individually (`margin-top`, `margin-right`, `margin-bottom`, `margin-left`) or as a shorthand.

```css
.element {
  margin: 10px; /* Applies to all sides */
  margin: 10px 20px; /* 10px top/bottom, 20px left/right */
}
```

## 3. Border
- The `border` surrounds the content and padding of an element.
- It consists of width, style, and color.

```css
.element {
  border: 2px solid black;
}
```

## 4. Padding
- The `padding` property adds space between the content and the element's border.
- Like margins, it can be set individually or as a shorthand.

```css
.element {
  padding: 10px; /* Applies to all sides */
  padding: 10px 20px; /* 10px top/bottom, 20px left/right */
}
```

# The Alternative Box Model: `box-sizing: border-box`

## Standard Box Model (Default)
By default, `width` and `height` apply only to the content, excluding padding and border. This can make layouts harder to manage.

```css
.element {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
}
```
- The actual width of the element = `200px (content) + 40px (padding) + 10px (border) = 250px`

## Border-Box Model (`box-sizing: border-box`)
With `box-sizing: border-box`, padding and border are included in the `width` and `height`, making layout calculations easier.

```css
.element {
  box-sizing: border-box;
  width: 200px;
  padding: 20px;
  border: 5px solid black;
}
```
- The actual width remains `200px` regardless of padding and border.

# Margin Collapsing
- When vertical margins of adjacent block elements meet, the larger margin takes effect instead of adding together.
- Example:

```css
.div1 {
  margin-bottom: 20px;
}
.div2 {
  margin-top: 30px;
}
```
- The space between `.div1` and `.div2` will be **30px** (not `20px + 30px = 50px`).

# Basic Display Values

## 1. `display: block;`
- Takes up the full width.
- Starts on a new line.
- Respects width, height, padding, margin.

```css
div {
  display: block;
}
```

## 2. `display: inline;`
- Takes only as much width as necessary.
- Does not start on a new line.
- Ignores width and height properties.

```css
span {
  display: inline;
}
```

## 3. `display: inline-block;`
- Behaves like an inline element but allows width and height to be set.

```css
div {
  display: inline-block;
  width: 100px;
  height: 50px;
}
```

## 4. `display: none;`
- Hides the element completely (removes it from the document flow).

```css
div {
  display: none;
}
```

This covers the key concepts in HTML and CSS box models!



