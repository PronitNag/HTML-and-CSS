# Adding CSS to an HTML page

CSS is attached to an HTML page in different ways.

## 1. Using the `<link>` tag

The `<link>` tag is the way to include a CSS file. This is the preferred way to use CSS as it's intended to be used: one CSS file is included by all the pages of your site, and changing one line on that file affects the presentation of all the pages in the site.

To use this method, you add a `<link>` tag with the `href` attribute pointing to the CSS file you want to include. You add it inside the `<head>` tag of the site (not inside the `<body>` tag):

```html
<link rel="stylesheet" type="text/css" href="myfile.css" />
```

The `rel` and `type` attributes are required too, as they tell the browser which kind of file we are linking to.

## 2. Using the `<style>` tag

Instead of using the `<link>` tag to point to a separate stylesheet containing our CSS, we can add the CSS directly inside a `<style>` tag. This is the syntax:

```html
<style>
  ...our CSS... 
</style>
```

Using this method we can avoid creating a separate CSS file. It is useful for experimentation before "formalizing" CSS to a separate file or for adding a special line of CSS just to a file.

## 3. Inline Styles

Inline styles are the third way to add CSS to a page. We can add a `style` attribute to any HTML tag and add CSS into it.

```html
<div style="background-color: yellow">...</div>
```

# Selectors

A selector allows us to associate one or more declarations to one or more elements on the page.

## 1. Basic Selectors

Suppose we have a `<p>` element on the page, and we want to display the words inside it using the yellow color. We can target that element using this selector:

```css
p {
  color: yellow;
}
```

Every HTML tag has a corresponding selector, for example: `div`, `span`, `img`.

HTML elements have two attributes commonly used in CSS: `class` and `id`.

- The `class` value can be repeated across multiple elements.
- The `id` can only be used once per document.

Classes are identified using the `.` symbol, while IDs use the `#` symbol.

### Example using a class:

```html
<p class="dog-name">Roger</p>
```

```css
.dog-name {
  color: yellow;
}
```

### Example using an id:

```html
<p id="dog-name">Roger</p>
```

```css
#dog-name {
  color: yellow;
}
```

## 2. Combining Selectors

### 2.1 Targeting an element with a class or id

Example using a class:

```html
<p class="dog-name">Roger</p>
```

```css
p.dog-name {
  color: yellow;
}
```

Example using an id:

```html
<p id="dog-name">Roger</p>
```

```css
p#dog-name {
  color: yellow;
}
```

### 2.2 Targeting multiple classes

Example:

```html
<p class="dog-name roger">Roger</p>
```

```css
.dog-name.roger {
  color: yellow;
}
```

### 2.3 Combining classes and ids

Example:

```html
<p class="dog-name" id="roger">Roger</p>
```

```css
.dog-name#roger {
  color: yellow;
}
```

## 3. Grouping Selectors

You can combine selectors to apply the same declarations to multiple elements. Use a comma to separate them.

Example:

```html
<p>My dog name is:</p>
<span class="dog-name"> Roger </span>
```

```css
p, .dog-name {
  color: yellow;
}
```

## 4. Following the Document Tree with Selectors

You can create a more specific selector by combining multiple items to follow the document tree structure.

Example:

```html
<p> 
  My dog name is: 
  <span class="dog-name"> Roger </span>
</p>
```

```css
p span {
  color: yellow;
}
```

### Direct Children Selector

To make the dependency strict on the first level, use the `>` symbol:

```css
p > span {
  color: yellow;
}
```

Example:

```html
<p> 
  <span> This is yellow </span> 
  <strong>
    <span> This is not yellow </span>
  </strong>
</p>
```

### Adjacent Sibling Selector

Adjacent sibling selectors style an element only if preceded by a specific element, using the `+` operator.

Example:

```css
p + span {
  color: yellow;
}
```

This applies the color yellow to all `span` elements preceded by a `<p>` element:

```html
<p>This is a paragraph</p>
<span>This is a yellow span</span>
```

## More Selectors

We have many more selectors available:

- Attribute selectors
- Pseudo-class selectors
- Pseudo-element selectors

These will be covered in the next sections.
