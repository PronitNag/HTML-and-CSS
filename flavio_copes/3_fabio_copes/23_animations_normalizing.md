# 41. Animations

## CSS Animations

CSS Animations are a great way to create visual animations, not limited to a single movement like CSS Transitions, but much more articulated.

An animation is applied to an element using the `animation` property:

```css
.container {
  animation: spin 10s linear infinite;
}
```

`spin` is the name of the animation, which we need to define separately. We also tell CSS to make the animation last 10 seconds, perform it in a linear way (no acceleration or any difference in its speed), and to repeat it infinitely.

You must define how your animation works using keyframes. Example of an animation that rotates an item:

```css
@keyframes spin {
  0% {
    transform: rotateZ(0);
  }
  100% {
    transform: rotateZ(360deg);
  }
}
```

Inside the `@keyframes` definition, you can have as many intermediate waypoints as you want. In this case, we instruct CSS to make the `transform` property rotate the Z-axis from 0 to 360 degrees, completing the full loop.

## 41.1. A CSS Animations Example

I want to draw four circles, all with a starting point in common, all 90 degrees distant from each other:

```html
<div class="container">
  <div class="circle one"></div>
  <div class="circle two"></div>
  <div class="circle three"></div>
  <div class="circle four"></div>
</div>
```

### CSS:

```css
body {
  display: grid;
  place-items: center;
  height: 100vh;
}

.circle {
  border-radius: 50%;
  left: calc(50% - 6.25em);
  top: calc(50% - 12.5em);
  transform-origin: 50% 12.5em;
  width: 12.5em;
  height: 12.5em;
  position: absolute;
  box-shadow: 0 1em 2em rgba(0, 0, 0, 0.5);
}

.one, .three {
  background: rgba(142, 92, 205, 0.75);
}

.two, .four {
  background: rgba(236, 252, 100, 0.75);
}

.one {
  transform: rotateZ(0);
}

.two {
  transform: rotateZ(90deg);
}

.three {
  transform: rotateZ(180deg);
}

.four {
  transform: rotateZ(-90deg);
}
```

You can see them in this Glitch: [CSS Circles Example](https://flavio-css-circles.glitch.me)

### Rotating the Structure

To rotate the entire structure, we apply an animation to the container:

```css
@keyframes spin {
  0% {
    transform: rotateZ(0);
  }
  100% {
    transform: rotateZ(360deg);
  }
}

.container {
  animation: spin 10s linear infinite;
}
```

See it on [CSS Animations Tutorial](https://flavio-css-animations-tutorial.glitch.me)

You can add more keyframes for different effects:

```css
@keyframes spin {
  0% {
    transform: rotateZ(0);
  }
  25% {
    transform: rotateZ(30deg);
  }
  50% {
    transform: rotateZ(270deg);
  }
  75% {
    transform: rotateZ(180deg);
  }
  100% {
    transform: rotateZ(360deg);
  }
}
```

See the example on [Four-Step CSS Animation](https://flavio-css-animations-four-steps.glitch.me)

## 41.2. The CSS Animation Properties

CSS animations offer different parameters you can tweak:

| Property | Description |
|----------|-------------|
| `animation-name` | The name of the animation, referencing an animation created using `@keyframes` |
| `animation-duration` | How long the animation should last, in seconds |
| `animation-timing-function` | The timing function used by the animation (common values: `linear`, `ease`). Default: `ease` |
| `animation-delay` | Optional number of seconds to wait before starting the animation |
| `animation-iteration-count` | How many times the animation should be performed (a number or `infinite`). Default: 1 |
| `animation-direction` | The direction of the animation (`normal`, `reverse`, `alternate`, `alternate-reverse`) |
| `animation-fill-mode` | Defines how to style the element when the animation ends (`none`, `forwards`, `backwards`, `both`) |
| `animation-play-state` | If set to `paused`, it pauses the animation. Default is `running` |

The `animation` shorthand property:

```css
.container {
  animation: spin 10s linear infinite;
}

.container {
  animation: name duration timing-function delay iteration-count direction fill-mode play-state;
}
```

## 41.3. JavaScript Events for CSS Animations

Using JavaScript, you can listen for animation events:

```js
const container = document.querySelector('.container');

container.addEventListener('animationstart', (e) => {
  // do something
}, false);

container.addEventListener('animationend', (e) => {
  // do something
}, false);

container.addEventListener('animationiteration', (e) => {
  // do something
}, false);
```

Be careful with `animationstart`, as animations that start on page load may already be running before JavaScript executes.

## 41.4. Which Properties You Can Animate using CSS Animations

A lot! The same properties you can animate using CSS Transitions are also available for CSS Animations. Here's a partial list:

- `background`
- `background-color`
- `background-position`
- `background-size`
- `border`
- `border-color`
- `border-width`
- `border-radius`
- `box-shadow`
- `color`
- `flex`
- `font-size`
- `grid`
- `height`
- `margin`
- `opacity`
- `padding`
- `transform`
- `visibility`
- `width`
- `z-index`

This list is not exhaustive, but it gives you an idea of the variety of properties you can animate with CSS.

---

This Markdown file can now be saved to GitHub for later reference!

