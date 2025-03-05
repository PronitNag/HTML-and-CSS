## 22. Box Model
Every CSS element is essentially a box. Every element is a generic box.
The box model explains the sizing of the elements based on a few CSS properties.

From the inside to the outside, we have:
- The content area
- Padding
- Border
- Margin

The best way to visualize the box model is to open the browser DevTools and check how it is displayed:

Here you can see how Firefox tells me the properties of a `span` element I highlighted. I right-clicked on it, pressed **Inspect Element**, and went to the **Layout** panel of the DevTools.

See, the light blue space is the content area. Surrounding it there is the padding, then the border, and finally the margin.

By default, if you set a `width` (or `height`) on the element, that is going to be applied to the content area. All the padding, border, and margin calculations are done outside of the value, so you have to take this into account when you do your calculation.

You can change this behavior using **Box Sizing**.

## 23. Border
The border is a thin layer between padding and margin. Editing the border, you can make elements draw their perimeter on the screen.

You can work on borders by using these properties:
- `border-style`
- `border-color`
- `border-width`

The property `border` can be used as a shorthand for all these properties.

`border-radius` is used to create rounded corners.

You also have the ability to use images as borders, an ability given to you by `border-image` and its specific separate properties:
- `border-image-source`
- `border-image-slice`
- `border-image-width`
- `border-image-outset`
- `border-image-repeat`

Let's start with `border-style`.

### 23.1. The Border Style
The `border-style` property lets you choose the style of the border. The options you can use are:
- `dotted`
- `dashed`
- `solid`
- `double`
- `groove`
- `ridge`
- `inset`
- `outset`
- `none`
- `hidden`

Check this **CodePen** for a live example.

The default for the style is `none`, so to make the border appear at all you need to change it to something else. `solid` is a good choice most of the time.

You can set a different style for each edge using the properties:
- `border-top-style`
- `border-right-style`
- `border-bottom-style`
- `border-left-style`

Or you can use `border-style` with multiple values to define them, using the usual **Top-Right-Bottom-Left** order:
```css
p {
  border-style: solid dotted solid dotted;
}
```

### 23.2. The Border Width
`border-width` is used to set the width of the border.

You can use one of the predefined values:
- `thin`
- `medium` (the default value)
- `thick`

Or express a value in `px`, `em`, `rem`, or any other valid length value.

Example:
```css
p {
  border-width: 2px;
}
```

You can set the width of each edge separately by using four values:
```css
p {
  border-width: 2px 1px 2px 1px;
}
```
Or use the specific edge properties:
- `border-top-width`
- `border-bottom-width`
- `border-left-width`
- `border-right-width`

### 23.3. The Border Color
`border-color` is used to set the color of the border.

If you don't set a color, the border by default takes the color of the text in the element.

Example:
```css
p {
  border-color: yellow;
}
```

You can set the color of each edge separately by using four values:
```css
p {
  border-color: black red yellow blue;
}
```
Or use the specific edge properties:
- `border-top-color`
- `border-right-color`
- `border-bottom-color`
- `border-left-color`

### 23.4. The Border Shorthand Property
The three properties `border-width`, `border-style`, and `border-color` can be set using the shorthand property `border`.

Example:
```css
p {
  border: 2px black solid;
}
```

You can also use the edge-specific properties:
- `border-top`
- `border-right`
- `border-bottom`
- `border-left`

Example:
```css
p {
  border-left: 2px black solid;
  border-right: 3px red dashed;
}
```

### 23.5. The Border Radius
`border-radius` is used to set rounded corners to the border. You need to pass a value that will be used as the radius of the circle that will round the border.

Usage:
```css
p {
  border-radius: 3px;
}
```

You can also use the edge-specific properties:
- `border-top-left-radius`
- `border-top-right-radius`
- `border-bottom-left-radius`
- `border-bottom-right-radius`

### 23.6. Using Images as Borders
One very cool thing with borders is the ability to use images to style them. This lets you be very creative with borders.

We have five properties:
- `border-image-source`
- `border-image-slice`
- `border-image-width`
- `border-image-outset`
- `border-image-repeat`

And the shorthand `border-image`.

I won't go into much detail here as images as borders would need a more in-depth coverage than I can provide in this little chapter. I recommend reading the **CSS Tricks Almanac** entry on `border-image` for more information.

