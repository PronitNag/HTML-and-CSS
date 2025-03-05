# Fonts

## 20. Fonts
At the dawn of the web, you only had a handful of fonts you could choose from. Thankfully, today you can load any kind of font on your pages. CSS has gained many nice capabilities over the years in regards to fonts.

The `font` property is the shorthand for a number of properties:

- `font-family`
- `font-weight`
- `font-stretch`
- `font-style`
- `font-size`

Let's see each one of them and then we'll cover `font`. Then we'll talk about how to load custom fonts using `@import` or `@font-face`, or by loading a font stylesheet.

### 20.1. font-family
Sets the font family that the element will use.

#### Why "family"?
Because what we know as a font is actually composed of several sub-fonts, which provide all the styles (bold, italic, light, etc.) we need.

Example:

```css
body {
  font-family: Helvetica;
}
```

You can set multiple values as fallbacks:

```css
body {
  font-family: Helvetica, Arial;
}
```

#### Web Safe Fonts
These fonts are pre-installed on different operating systems. They are categorized into:

**Serif:**

- Georgia
- Palatino
- Times New Roman
- Times

**Sans-Serif:**

- Arial
- Helvetica
- Verdana
- Geneva
- Tahoma
- Lucida Grande
- Impact
- Trebuchet MS
- Arial Black

**Monospace:**

- Courier New
- Courier
- Lucida Console
- Monaco

You can also use generic names:

- `sans-serif` (a font without ligatures)
- `serif` (a font with ligatures)
- `monospace` (a font especially good for code)
- `cursive` (used to simulate handwritten text)
- `fantasy` (for decorative text)

Example:

```css
body {
  font-family: Helvetica, Arial, sans-serif;
}
```

### 20.2. font-weight
Sets the width of a font. Available values:

- `normal`
- `bold`
- `bolder` (relative to parent element)
- `lighter` (relative to parent element)

Or using numeric values:

- `100` (lightest) to `900` (boldest)

Example:

```css
p {
  font-weight: bold;
}
```

### 20.3. font-stretch
Allows selecting a narrow or wide font face, if available. Values:

- `ultra-condensed`
- `extra-condensed`
- `condensed`
- `semi-condensed`
- `normal`
- `semi-expanded`
- `expanded`
- `extra-expanded`
- `ultra-expanded`

### 20.4. font-style
Allows applying an italic style:

```css
p {
  font-style: italic;
}
```

Other values: `oblique`, `normal`.

### 20.5. font-size
Determines font size.

#### Length values:
- `px`, `em`, `rem`, `%`

#### Predefined values:
- `xx-small`, `x-small`, `small`, `medium`, `large`, `x-large`, `xx-large`
- `smaller`, `larger` (relative to parent element)

Example:

```css
p {
  font-size: 20px;
}
```

### 20.6. font-variant
Used to enable small caps. Values:

- `normal`
- `inherit`
- `small-caps`

### 20.7. font
The `font` property allows setting multiple font-related properties at once. Example:

```css
body {
  font: italic bold 20px Helvetica;
}
```

### 20.8. Loading custom fonts using @font-face
`@font-face` allows adding custom fonts by specifying a font file to download.

Example:

```css
@font-face {
  font-family: 'CustomFont';
  src: url('custom-font.woff2') format('woff2');
}
```

## 21. Typography
Additional text styling properties:

- `text-transform`
- `text-decoration`
- `text-align`
- `vertical-align`
- `line-height`
- `text-indent`
- `word-spacing`
- `letter-spacing`
- `text-shadow`
- `white-space`
- `tab-size`
- `writing-mode`
- `hyphens`
- `text-orientation`
- `direction`
- `line-break`
- `word-break`
- `overflow-wrap`

### 21.1. text-transform
Transforms text case. Values:

- `capitalize`
- `uppercase`
- `lowercase`
- `none`

Example:

```css
p {
  text-transform: uppercase;
}
```

### 21.2. text-decoration
Adds decorations to text. Values:

- `underline`
- `overline`
- `line-through`
- `none`

Example:

```css
p {
  text-decoration: underline dashed yellow;
}
```

### 21.3. text-align
Aligns text within a block. Values:

- `left`
- `right`
- `center`
- `justify`

Example:

```css
p {
  text-align: right;
}
```

### 21.4. vertical-align
Aligns inline elements vertically. Values:

- `baseline`
- `sub`
- `super`
- `top`
- `middle`
- `bottom`

Example:

```css
img {
  vertical-align: middle;
}
```

### 21.5. line-height
Controls spacing between lines:

```css
p {
  line-height: 1.5;
}
```

### 21.6. text-indent
Indents first line of a paragraph:

```css
p {
  text-indent: 10px;
}
```

### 21.7. word-spacing
Adjusts spacing between words:

```css
p {
  word-spacing: 2px;
}
```

### 21.8. letter-spacing
Adjusts spacing between letters:

```css
p {
  letter-spacing: 0.2px;
}
```

### 21.9. text-shadow
Applies a shadow to text:

```css
p {
  text-shadow: 2px 2px 5px gray;
}
```

### 21.10. white-space
Controls handling of white space:

```css
p {
  white-space: nowrap;
}
```

### 21.11. overflow-wrap
Controls how words break at line ends:

```css
p {
  overflow-wrap: break-word;
}
```

This Markdown file is now ready to be saved and used on GitHub!

