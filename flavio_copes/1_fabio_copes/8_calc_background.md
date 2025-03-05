## 16. `calc()`

The `calc()` function lets you perform basic math operations on values, and it's especially useful when you need to add or subtract a length value from a percentage.

### Example Usage:
```css
div {
  max-width: calc(80% - 100px);
}
```

It returns a length value, so it can be used anywhere you expect a pixel value.

### Supported Operations:
- Addition: `+`
- Subtraction: `-`
- Multiplication: `*`
- Division: `/`

**Note:** With addition and subtraction, the space around the operator is mandatory; otherwise, it does not work as expected.

### More Examples:
```css
div {
  max-width: calc(50% / 3);
}

div {
  max-width: calc(50% + 3px);
}
```

## 17. Backgrounds

The background of an element can be changed using several CSS properties:

- `background-color`
- `background-image`
- `background-clip`
- `background-position`
- `background-origin`
- `background-repeat`
- `background-attachment`
- `background-size`
- `background` (shorthand property)

### `background-color`
Accepts a color value, which can be a color keyword, `rgb`, or `hsl` value:
```css
p {
  background-color: yellow;
}

div {
  background-color: #333;
}
```

### `background-image`
Instead of using a color, you can use an image as the background:
```css
div {
  background-image: url(image.png);
}
```

### `background-clip`
Defines the area used by the background image or color:
- `border-box` (default) - Extends up to the border outer edge.
- `padding-box` - Extends the background up to the padding edge, without the border.
- `content-box` - Extends the background up to the content edge, without the padding.
- `inherit` - Inherits from the parent.

### `background-position`
Defines the placement of the background image:
```css
div {
  background-position: top right;
}
```
Valid values:
- `left`, `right`, `center` (X-axis)
- `top`, `bottom` (Y-axis)

### `background-repeat`
Defines how the background image repeats:
- `repeat-x` (repeats horizontally)
- `repeat-y` (repeats vertically)
- `repeat` (repeats in both directions, default)
- `no-repeat` (prevents repetition)

### `background-origin`
Specifies where the background should be applied:
- `padding-box` (default) - Extends to include padding.
- `border-box` - Extends to include the border.
- `content-box` - Excludes padding and border.

### `background-attachment`
Defines if the background scrolls with the viewport:
```css
div {
  background-attachment: fixed;
}
```
Possible values:
- `scroll` (default)
- `fixed` (stays in place while scrolling)
- `local` (scrolls with content)

### `background-size`
Specifies the size of the background image:
- `auto` (default)
- `cover` (expands until the element is fully covered)
- `contain` (scales so the entire image fits within the element)

#### Example Usage:
```css
div {
  background-size: 100%;
}

div {
  background-size: 800px 600px;
}
```

### `background` (Shorthand Property)
Allows multiple background properties to be set in a single line:
```css
div {
  background: url(bg.png) top left no-repeat;
}
```

If the image fails to load, a fallback color can be provided:
```css
div {
  background: url(image.png) yellow;
}
```

### Gradients as Backgrounds
You can also set a gradient as the background:
```css
div {
  background: linear-gradient(#fff, #333);
}
