## 31. CSS Grid

CSS Grid is the new kid in the CSS town, and while not yet fully supported by all browsers, it's going to be the future system for layouts.

CSS Grid is a fundamentally new approach to building layouts using CSS. Keep an eye on the CSS Grid Layout page on [caniuse.com](https://caniuse.com/#feat=css-grid) to find out which browsers currently support it. As of April 2019, all major browsers (except IE, which will never support it) already support this technology, covering 92% of all users.

CSS Grid is not a competitor to Flexbox. They interoperate and collaborate on complex layouts, because CSS Grid works on two dimensions (rows **and** columns) while Flexbox works on a single dimension (rows **or** columns).

Building layouts for the web has traditionally been a complicated topic. Nowadays, you have two very powerful and well-supported tools at your disposal:

- CSS Flexbox
- CSS Grid

These two are the tools to build the web layouts of the future. Unless you need to support old browsers like IE8 and IE9, there is no reason to use:

- Table layouts
- Floats
- clearfix hacks
- `display: table` hacks

In this guide, you'll learn everything needed to go from zero knowledge of CSS Grid to being a proficient user.

---

### 31.1. The Basics

The CSS Grid layout is activated on a container element by setting:

```css
.container {
  display: grid;
}
```

As with Flexbox, you can define properties on the container and individual items in the grid. These properties together determine the final look of the grid.

#### 31.1.1. `grid-template-columns` and `grid-template-rows`

These properties define the number of columns and rows in the grid, and they also set the width of each column/row.

Example:

```css
.container {
  display: grid;
  grid-template-columns: 200px 200px 200px 200px;
  grid-template-rows: 300px 300px;
}
```

Another example:

```css
.container {
  display: grid;
  grid-template-columns: 200px 200px;
  grid-template-rows: 100px 100px;
}
```

#### 31.1.2. Automatic Dimensions

Use `auto` for flexible content:

```css
.container {
  display: grid;
  grid-template-rows: 100px auto 100px;
}
```

#### 31.1.3. Different Column and Row Dimensions

```css
.container {
  display: grid;
  grid-template-columns: 100px 200px;
  grid-template-rows: 100px 50px;
}
```

#### 31.1.4. Adding Space Between Cells

Use `grid-column-gap`, `grid-row-gap`, or shorthand `grid-gap`:

```css
.container {
  display: grid;
  grid-template-columns: 100px 200px;
  grid-template-rows: 100px 50px;
  grid-gap: 25px;
}
```

#### 31.1.5. Spanning Items Across Multiple Columns/Rows

```css
.item1 {
  grid-column: 2 / span 2;
}

.item6 {
  grid-column: 3 / span 2;
}
```

---

### 31.2. More Grid Configuration

#### 31.2.1. Using Fractions (`fr`)

```css
.container {
  grid-template-columns: 1fr 1fr 1fr;
}
```

#### 31.2.2. Using Percentages and `rem`

```css
.container {
  grid-template-columns: 3rem 15% 1fr 2fr;
}
```

#### 31.2.3. Using `repeat()`

```css
.container {
  grid-template-columns: repeat(4, 100px);
}
```

#### 31.2.4. Minimum Width with `minmax()`

```css
.container {
  grid-template-columns: minmax(200px, 3fr) 9fr;
}
```

#### 31.2.5. Positioning Elements with `grid-template-areas`

```css
.container {
  display: grid;
  grid-template-areas:
    'header header header header'
    'sidebar main main main'
    'footer footer footer footer';
}

main { grid-area: main; }
aside { grid-area: sidebar; }
header { grid-area: header; }
footer { grid-area: footer; }
```

---

### 31.3. Fill a Page with a Grid

```css
.container {
  display: grid;
  height: 100vh;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
}
```

### 31.4. Example: Header, Sidebar, Content, and Footer

#### HTML

```html
<div class="wrapper">
  <header>Header</header>
  <article>
    <h1>Welcome</h1>
    <p>Hi!</p>
  </article>
  <aside>
    <ul>
      <li>Sidebar</li>
    </ul>
  </aside>
  <footer>Footer</footer>
</div>
```

#### CSS

```css
.wrapper {
  display: grid;
  grid-gap: 20px;
  grid-template-columns: 1fr 3fr;
  grid-template-areas:
    'header  header'
    'sidebar content'
    'footer  footer';
}

header { grid-area: header; background-color: #fed330; padding: 20px; }
article { grid-area: content; background-color: #20bf6b; padding: 20px; }
aside { grid-area: sidebar; background-color: #45aaf2; }
footer { grid-area: footer; background-color: #fd9644; padding: 20px; }
```

Responsive layout using media queries:

```css
@media (max-width: 500px) {
  .wrapper {
    grid-template-columns: 4fr;
    grid-template-areas:
      'header'
      'content'
      'sidebar'
      'footer';
  }
}
```

### 31.5. Wrapping Up

These are the basics of CSS Grid. There are many advanced features not covered here, but this guide provides a strong foundation for getting started with CSS Grid layout.

