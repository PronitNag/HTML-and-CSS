## 37. Feature Queries

Feature queries are a recent and relatively unknown ability of CSS, but a well-supported one.

We can use it to check if a feature is supported by the browser using the `@supports` keyword.

For example, I think this is especially useful, at the time of writing, for checking if a browser supports CSS grid, which can be done using:

```css
@supports (display: grid) { 
  /* apply this CSS */ 
}
```

We check if the browser supports the `grid` value for the `display` property. We can use `@supports` for any CSS property to check any value.

We can also use the logical operators `and`, `or`, and `not` to build complex feature queries:

```css
@supports (display: grid) and (display: flex) { 
  /* apply this CSS */ 
}
```

---

## 38. Filters

Filters allow us to perform operations on elements—things you normally do with Photoshop or other photo editing software, like changing the opacity or the brightness, and more.

You use the `filter` property. Here's an example of it applied to an image, but this property can be used on any element:

```css
img { 
  filter: <something>; 
}
```

### Available filter functions:

- `blur()`
- `brightness()`
- `contrast()`
- `drop-shadow()`
- `grayscale()`
- `hue-rotate()`
- `invert()`
- `opacity()`
- `sepia()`
- `saturate()`
- `url()`

Each function requires a parameter within parentheses.

#### Example:

```css
img { 
  filter: opacity(0.5); 
}
```

This makes the image 50% transparent, as `opacity()` takes a value from `0` to `1`, or a percentage.

You can also apply multiple filters at once:

```css
img { 
  filter: opacity(0.5) blur(2px); 
}
```

---

### 38.0.1. `blur()`
Blurs an element's content. The value determines the blur radius.

```css
img { 
  filter: blur(4px); 
}
```

---

### 38.0.2. `opacity()`
Determines image transparency based on a value from `0` to `1`.

```css
img { 
  filter: opacity(0.5); 
}
```

`filter` can be hardware accelerated, so it should be preferred over the `opacity` property.

---

### 38.0.3. `drop-shadow()`
Applies a shadow that follows the alpha channel of the element.

```css
img { 
  filter: drop-shadow(10px 10px 5px orange); 
}
```

It accepts:
- `offset-x` (horizontal offset, can be negative)
- `offset-y` (vertical offset, can be negative)
- `blur-radius` (optional, defaults to `0`)
- `spread-radius` (optional)
- `color` (optional)

---

### 38.0.4. `grayscale()`
Converts an element to grayscale.

```css
img { 
  filter: grayscale(50%); 
}
```

---

### 38.0.5. `sepia()`
Applies a sepia tone to an element.

```css
img { 
  filter: sepia(50%); 
}
```

---

### 38.0.6. `invert()`
Inverts the colors of an element.

```css
img { 
  filter: invert(50%); 
}
```

---

### 38.0.7. `hue-rotate()`
Rotates the hue of an element by a specified degree.

```css
img { 
  filter: hue-rotate(90deg); 
}
```

---

### 38.0.8. `brightness()`
Alters the brightness of an element.

```css
img { 
  filter: brightness(50%); 
}
```

---

### 38.0.9. `contrast()`
Alters the contrast of an element.

```css
img { 
  filter: contrast(150%); 
}
```

---

### 38.0.10. `saturate()`
Alters the saturation of an element.

```css
img { 
  filter: saturate(150%); 
}
```

---

### 38.0.11. `url()`
Applies a filter defined in an external SVG file.

```css
img { 
  filter: url(filter.svg); 
}
```

For more details on SVG filters, check out [this article on Smashing Magazine](https://www.smashingmagazine.com/2015/05/why-the-svg-filter-is-awesome).

