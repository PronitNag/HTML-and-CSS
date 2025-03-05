## 18. Comments
CSS gives you the ability to write comments in a CSS file or in the page header.

The format is the `style` tag:

```css
/* this is a comment */
```

C-style (or JavaScript-style, if you prefer) comments.

This is a multiline comment. Until you add the closing `*/` token, all the lines found after the opening one are commented.

### Example:

```css
#name { 
  display: block; 
} /* Nice rule! */ 

/* #name { display: block; } */

#name { 
  display: block; 
  /* color: red; */ 
} 
```

CSS does not have inline comments, like `//` in C or JavaScript.

Pay attention though - if you add `//` before a rule, the rule will not be applied, making it look like the comment worked. In reality, CSS detected a syntax error and, due to how it works, ignored the line with the error and went straight to the next line.

Knowing this approach lets you purposefully write inline comments, although you have to be careful because you can't add random text like you can in a block comment.

### Example:

```css
// Nice rule!
#name { 
  display: block; 
} 
```

In this case, due to how CSS works, the `#name` rule is actually commented out. To avoid issues, just rely on block comments.

## 19. Custom Properties

In the last few years, CSS preprocessors had a lot of success. It was very common for greenfield projects to start with Less or Sass, and it's still a very popular technology.

### The main benefits of those technologies are:
- They allow nesting selectors.
- They provide easy import functionality.
- They give you variables.

Modern CSS has a new powerful feature called **CSS Custom Properties**, also commonly known as **CSS Variables**.

CSS is not a programming language like JavaScript, Python, PHP, Ruby, or Go where variables are key. But a variable is a variable: a name that refers to a value, and variables in CSS help reduce repetition and inconsistencies by centralizing value definitions.

### 19.1. The basics of using variables

A CSS Variable is defined with a special syntax, prepending two dashes to a name (`--variable-name`), followed by a colon and a value:

```css
:root { 
  --primary-color: yellow; 
} 
```

You can access the variable value using `var()`:

```css
p { 
  color: var(--primary-color); 
} 
```

The variable value can be any valid CSS value:

```css
:root { 
  --default-padding: 30px 30px 20px 20px; 
  --default-color: red; 
  --default-background: #fff; 
} 
```

### 19.2. Create variables inside any element

CSS Variables can be defined inside any element:

```css
:root { 
  --default-color: red; 
} 

body { 
  --default-color: red; 
} 

main { 
  --default-color: red; 
} 

p { 
  --default-color: red; 
} 

span { 
  --default-color: red; 
} 

a:hover { 
  --default-color: red; 
} 
```

### 19.3. Variables scope

Adding variables to a selector makes them available to all its children. 
Using `:root` when defining a CSS variable makes it available to all elements:

```css
:root { 
  --primary-color: yellow; 
} 
```

If a variable is added inside `.container`, it will only be available to children of `.container`:

```css
.container { 
  --secondary-color: yellow; 
} 
```

Variables can be reassigned:

```css
:root { 
  --primary-color: yellow; 
} 

.container { 
  --primary-color: blue; 
} 
```

Outside `.container`, `--primary-color` will be yellow, but inside it will be blue.

You can also assign or overwrite a variable inside HTML using inline styles:

```html
<main style="--primary-color: orange;">
  <!-- ... -->
</main>
```

### 19.4. Interacting with a CSS Variable value using JavaScript

You can set a variable value using JavaScript:

```js
const element = document.getElementById('my-element');
element.style.setProperty('--variable-name', 'a-value');
```

To access a variable value:

```js
const styles = getComputedStyle(document.documentElement);
const value = String(styles.getPropertyValue('--variable-name')).trim();
```

Or for a specific element:

```js
const element = document.getElementById('my-element');
const styles = getComputedStyle(element);
const value = String(styles.getPropertyValue('--variable-name')).trim();
```

### 19.5. Handling invalid values

If a variable is assigned to a property that does not accept its value, it is considered invalid and ignored.

### 19.6. Browser support

CSS Variables are well-supported in modern browsers, except for Internet Explorer and old versions of others. If you need compatibility, use libraries like PostCSS or Myth.

### 19.7. CSS Variables are case sensitive

```css
--width: 100px;
```

is different from:

```css
--Width: 100px;
```

### 19.8. Math in CSS Variables

To perform math operations with CSS Variables, use `calc()`:

```css
:root { 
  --default-left-padding: calc(10px * 2); 
} 
```

### 19.9. Media queries with CSS Variables

CSS Variables work normally with media queries:

```css
body { 
  --width: 500px; 
} 

@media screen and (max-width: 1000px) and (min-width: 700px) { 
  --width: 800px; 
} 

.container { 
  width: var(--width); 
} 
```

### 19.10. Setting a fallback value for `var()`

`var()` accepts a second parameter as the fallback value:

```css
.container { 
  margin: var(--default-margin, 30px);
} 

