## 39. Transforms

### 39.1. 2D Transforms

Transforms allow you to translate, rotate, scale, and skew elements in the 2D or 3D space. They are a very cool CSS feature, especially when combined with animations.

The `transform` property accepts these functions:

- `translate()` - moves elements around
- `rotate()` - rotates elements
- `scale()` - scales elements in size
- `skew()` - twists or slants an element
- `matrix()` - performs transformations using a 6-element matrix (less user-friendly but more concise)

We also have axis-specific functions:

- `translateX()` - moves elements on the X axis
- `translateY()` - moves elements on the Y axis
- `scaleX()` - scales elements on the X axis
- `scaleY()` - scales elements on the Y axis
- `skewX()` - skews an element on the X axis
- `skewY()` - skews an element on the Y axis

Example:

```css
.box {
  transform: scale(2, 0.5); /* Doubles width, halves height */
}
```

The `transform-origin` property sets the origin (`0,0` coordinates) for transformations, changing the rotation center.

### 39.2. Combining Multiple Transforms

You can combine multiple transforms by separating each function with a space.

Example:

```css
transform: rotateY(20deg) scaleX(3) translateY(100px);
```

### 39.3. 3D Transforms

3D transforms allow moving elements in a 3D space by adding the Z axis for depth.

Using the `perspective` property, you can specify how far the 3D object is from the viewer.

Example:

```css
.3delement {
  perspective: 100px;
}
```

The `perspective-origin` property determines the viewer's position along the X and Y axes.

Additional functions for the Z axis:

- `translateZ()`
- `rotateZ()`
- `scaleZ()`

Shorthand functions:

- `translate3d(x, y, z)`
- `rotate3d(x, y, z, angle)`
- `scale3d(x, y, z)`

3D transforms are an advanced topic, but worth exploring further!

---

## 40. Transitions

CSS Transitions are the simplest way to create animations in CSS. A transition changes the value of a property over time based on defined parameters.

CSS Transitions are defined by these properties:

| Property                 | Description |
|--------------------------|-------------|
| `transition-property`    | The CSS property to transition |
| `transition-duration`    | Duration of the transition |
| `transition-timing-function` | Timing function (e.g., `linear`, `ease`) - Default: `ease` |
| `transition-delay`       | Delay before starting the animation (optional) |

Shorthand syntax:

```css
.container {
  transition: property duration timing-function delay;
}
```

### 40.1. Example of a CSS Transition

```css
.one, .three {
  background: rgba(142, 92, 205, 0.75);
  transition: background 1s ease-in;
}

.two, .four {
  background: rgba(236, 252, 100, 0.75);
}

.circle:hover {
  background: rgba(142, 92, 205, 0.25); /* Lighter */
}
```

See the example on [Glitch](https://flavio-css-transitions-example.glitch.me)

When hovering `.one` and `.three` (purple circles), there is a transition animation easing the background change. The yellow circles do not transition since they lack the `transition` property.

### 40.2. Transition Timing Function Values

The `transition-timing-function` property defines the acceleration curve of the transition. Common values:

- `linear`
- `ease`
- `ease-in`
- `ease-out`
- `ease-in-out`

You can create custom timing functions using cubic Bezier curves.

### 40.3. CSS Transitions in Browser DevTools

Browser DevTools allow you to visualize and edit transitions in real time.

### 40.4. Animatable CSS Properties

CSS Transitions and Animations can modify a wide range of properties, including:

- `background`
- `background-color`
- `border`
- `border-radius`
- `box-shadow`
- `color`
- `opacity`
- `transform`
- `width`, `height`, `top`, `left`
- `z-index`

... and many more!

For a full list, refer to the official CSS documentation.

