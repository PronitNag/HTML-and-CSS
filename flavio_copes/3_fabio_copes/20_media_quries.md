## 36.2. Media Feature Descriptors

First, let's introduce **media feature descriptors**. They are additional keywords that we can add to the `media` attribute of `<link>` or the `@import` declaration to express more conditionals over the loading of the CSS.

### List of Media Feature Descriptors:
- `width`
- `height`
- `device-width`
- `device-height`
- `aspect-ratio`
- `device-aspect-ratio`
- `color`
- `color-index`
- `monochrome`
- `resolution`
- `orientation`
- `scan`
- `grid`

Each of them has a corresponding `min-` and `max-`, for example:
- `min-width`, `max-width`
- `min-device-width`, `max-device-width`

Some of these accept a length value which can be expressed in `px`, `rem`, or any length unit. This applies to `width`, `height`, `device-width`, and `device-height`.

#### Example:
```css
@import url(myfile.css) screen and (max-width: 800px);
```
Notice that we wrap each block using media feature descriptors in parentheses.

Some accept a fixed value. For example:
- `orientation` (used to detect the device orientation) accepts `portrait` or `landscape`.
- `scan` (used to determine the type of screen) accepts `progressive` (for modern displays) or `interlace` (for older CRT devices).

Some others require an integer.
- `color` inspects the number of bits per color component used by the device. This is very low-level, but it's available for use (like `grid`, `color-index`, `monochrome`).

#### Example:
```html
<link rel="stylesheet" type="text/css" href="myfile.css" media="screen and (aspect-ratio: 4/3)">
```

- `aspect-ratio` and `device-aspect-ratio` accept a ratio value representing the width-to-height viewport ratio, expressed as a fraction.

#### Example:
```css
@import url(myfile.css) screen and (aspect-ratio: 4/3);
```

- `resolution` represents the pixel density of the device, expressed in a resolution data type like `dpi`.

#### Example:
```css
@import url(myfile.css) screen and (min-resolution: 100dpi);
```

## 36.3. Logic Operators

We can combine rules using `and`:

```html
<link rel="stylesheet" type="text/css" href="myfile.css" media="screen and (max-width: 800px)">
```

We can perform an "or" type of logic operation using commas, which combines multiple media queries:

```css
@import url(myfile.css) screen, print;
```

We can use `not` to negate a media query:

```css
@import url(myfile.css) not screen;
```

**Important:** `not` can only be used to negate an entire media query, so it must be placed at the beginning of it (or after a comma).

## 36.4. Media Queries

All the rules above that apply to `@import` or the `<link>` HTML tag can also be applied inside the CSS.

You need to wrap them in a `@media () {}` structure.

#### Example:
```css
@media screen and (max-width: 800px) {
  /* enter some CSS */
}
```

This is the foundation for **responsive design**.

Media queries can be quite complex. This example applies the CSS only if it's a screen device, the width is between 600 and 800 pixels, and the orientation is landscape:

```css
@media screen and (max-width: 800px) and (min-width: 600px) and (orientation: landscape) {
  /* enter some CSS */
}

