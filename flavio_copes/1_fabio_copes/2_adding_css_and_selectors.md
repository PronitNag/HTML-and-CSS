
## 4. Adding CSS to an HTML page

CSS is attached to an HTML page in different ways.

### 4.1. Using the `<link>` tag

The `<link>` tag is the way to include a CSS file. This is the preferred way to use CSS as it's intended to be used: one CSS file is included by all the pages of your site, and changing one line on that file affects the presentation of all the pages in the site.

To use this method, you add a `<link>` tag with the `href` attribute pointing to the CSS file you want to include. You add it inside the `<head>` tag of the site (not inside the `<body>` tag):

```html
<link rel="stylesheet" type="text/css" href="myfile.css" />
```

The `rel` and `type` attributes are required too, as they tell the browser which kind of file we are linking to.

### 4.2. Using the `<style>` tag

Instead of using the `<link>` tag to point to a separate stylesheet containing our CSS, we can add the CSS directly inside a `<style>` tag. This is the syntax:

```html
<style> 
  ...our CSS...; 
</style>
```

Using this method, we can avoid creating a separate CSS file. This is a good way to experiment before "formalizing" CSS to a separate file or to add a special line of CSS just to a file.

### 4.3. Inline styles

Inline styles are the third way to add CSS to a page. We can add a `style` attribute to any HTML tag and add CSS into it.

```html
<div style="background-color: yellow">...</div>
```

---

## 5. Selectors

A selector allows us to associate one or more declarations to one or more elements on the page.

### 5.1. Basic selectors

Suppose we have a `<p>` element on the page, and we want to display the words inside it using the yellow color.

We can target that element using this selector:

```css
p { 
  color: yellow; 
} 
```

Every HTML tag has a corresponding selector, for example: `img`, `div`, `span`.

HTML elements have two attributes commonly used within CSS to associate styling to a specific element on the page: `class` and `id`.

- The `class` value can be repeated across multiple elements.
- The `id` can only be used once per document.
- Classes are identified using the `.` symbol, while ids use the `#` symbol.

#### Example using a class:

```html
<p class="dog-name">Roger</p>
```

```css
.dog-name { 
  color: yellow; 
} 
```

#### Example using an id:

```html
<p id="dog-name">Roger</p>
```

```css
#dog-name { 
  color: yellow; 
} 
```

### 5.2. Combining selectors

#### 5.2.1. Targeting an element with a class or id

You can target a specific element that has a class or id attached.

##### Example using a class:

```html
<p class="dog-name">Roger</p>
```

```css
p.dog-name { 
  color: yellow; 
} 
```

##### Example using an id:

```html
<p id="dog-name">Roger</p>
```

```css
p#dog-name { 
  color: yellow; 
} 
```

### 5.2.2. Targeting multiple classes

You can target an element with multiple classes by combining the class names separated with a dot, without spaces.

```html
<p class="dog-name roger">Roger</p>
```

```css
.dog-name.roger { 
  color: yellow; 
} 
```

### 5.2.3. Combining classes and ids

You can combine a class and an id.

```html
<p class="dog-name" id="roger">Roger</p>
```

```css
.dog-name#roger { 
  color: yellow; 
} 
```

### 5.3. Grouping selectors

You can combine selectors to apply the same declarations to multiple selectors. To do so, you separate them with a comma.

```html
<p>My dog name is:</p>
<span class="dog-name"> Roger </span>
```

```css
p, 
.dog-name { 
  color: yellow; 
} 
```

### 5.4. Follow the document tree with selectors

You can create a more specific selector by combining multiple items to follow the document tree structure.

#### Example:

```html
<span> Hello! </span>
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

This works even if the element on the right is multiple levels deep. To make the dependency strict on the first level, you can use the `>` symbol:

```css
p > span { 
  color: yellow; 
} 
```

##### Example:

```html
<p> 
  <span> This is yellow </span> 
  <strong> 
    <span> This is not yellow </span> 
  </strong>
</p>
```

### 5.5. Adjacent sibling selectors

Adjacent sibling selectors let us style an element only if preceded by a specific element using the `+` operator.

```css
p + span { 
  color: yellow; 
} 
```

#### Example:

```html
<p>This is a paragraph</p>
<span>This is a yellow span</span>
```

### 5.6. More selectors

We have many more selectors we can use:

- **Attribute selectors**
- **Pseudo-class selectors**
- **Pseudo-element selectors**

We'll learn more about them in the next sections.
