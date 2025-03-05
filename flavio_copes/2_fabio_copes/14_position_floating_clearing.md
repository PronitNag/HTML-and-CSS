## 28. Positioning

Positioning is what makes us determine where elements appear on the screen, and how they appear.
You can move elements around, and position them exactly where you want.
In this section, we'll also see how things change on a page based on how elements with different positions interact with each other.

We have one main CSS property: `position`.
It can have these 5 values:

- `static`
- `relative`
- `absolute`
- `fixed`
- `sticky`

### 28.1. Static positioning

This is the default value for an element. Static positioned elements are displayed in the normal page flow.

### 28.2. Relative positioning

If you set `position: relative;` on an element, you are now able to position it with an offset, using the properties `top`, `right`, `bottom`, `left`, which are called offset properties. They accept a length value or a percentage.

#### Example:

```html
<div class="parent"> 
  <div class="child"> 
    <div class="box"> 
      <p>Test</p> 
    </div> 
  </div>
</div>
```

#### CSS:

```css
.parent { 
  background-color: #af47ff; 
  padding: 30px; 
  width: 300px; 
} 

.child { 
  background-color: #ff4797; 
  padding: 30px; 
} 

.box { 
  background-color: #f3ff47; 
  padding: 30px; 
  border: 2px solid #333; 
  border-style: dotted; 
  font-family: courier; 
  text-align: center; 
  font-size: 2rem; 
} 
```

Adding `position: relative;`:

```css
.box { 
  /* ... */ 
  position: relative; 
  top: -60px; 
}
```

A negative value for `top` will make the box move up relatively to its container.

### 28.3. Absolute positioning

Setting `position: absolute;` on an element will remove it from the document's flow, and it will no longer follow the original page positioning flow.

```css
.box { 
  /* ... */ 
  position: absolute; 
  top: 0px; 
  left: 0px; 
}
```

The coordinates are relative to the closest container that is not `static`.

```css
.child { 
  /* ... */ 
  position: relative; 
} 

.box { 
  /* ... */ 
  position: absolute; 
  top: 0px; 
  left: 0px; 
}
```

### 28.4. Fixed positioning

Like with absolute positioning, when an element is assigned `position: fixed;`, it's removed from the flow of the page.

```css
.box { 
  /* ... */ 
  position: fixed; 
  top: 0; 
  left: 0; 
}
```

A fixed element stays in place even when scrolling.

### 28.5. Sticky positioning

`position: sticky;` is a hybrid between relative and fixed positioning. It stays in place when scrolling until a certain point.

## 29. Floating and Clearing

The `float` property supports 3 values:

- `left`
- `right`
- `none` (the default)

#### Example:

```html
<div class="parent"> 
  <div class="child"> 
    <div class="box"> 
      <p> 
        This is some random paragraph and an image. 
        <img src="https://via.placeholder.com/100x100" /> 
      </p> 
    </div> 
  </div>
</div>
```

#### CSS:

```css
img { 
  float: left; 
  padding: 20px 20px 0px 0px; 
}
```

Applying `float: right;`:

```css
img { 
  float: right; 
  padding: 20px 0px 20px 20px; 
}
```

A floated element is removed from the normal flow of the page, and the other content flows around it.

## 29.1. Clearing

If you float multiple elements, they stack up horizontally. You can use the `clear` property to control this behavior:

```css
img { 
  float: left; 
  padding: 20px 20px 0px 0px; 
}
```

Using `clear: left;`:

```css
img { 
  clear: left; 
}
```

### Clear Values:

- `left` to clear left floats
- `right` to clear right floats
- `both` to clear both left and right floats
- `none` (default) disables clearing

