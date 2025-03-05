## 14. Units
One of the things you'll use every day in CSS are units. They are used to set
lengths, paddings, margins, align elements and so on. Things like `px`, `em`, `rem`, or percentages.

They are everywhere. There are some obscure ones, too. We'll go through each of them in this section.

### 14.1. Pixels
The most widely used measurement unit. A pixel does not actually correlate
to a physical pixel on your screen, as that varies a lot by device (think high DPI devices vs non-retina devices).

There is a convention that makes this unit work consistently across devices.

### 14.2. Percentages
Another very useful measure, percentages let you specify values in
percentages of that parent element's corresponding property.

#### Example:
```css
.parent { 
  width: 400px; 
} 
.child { 
  width: 50%; /* = 200px */ 
} 
```

### 14.3. Real-world measurement units
We have those measurement units which are translated from the outside world. Mostly useless on screen, they can be useful for print stylesheets. They are:

- `cm` - a centimeter (maps to 37.8 pixels)
- `mm` - a millimeter (0.1cm)
- `q` - a quarter of a millimeter
- `in` - an inch (maps to 96 pixels)
- `pt` - a point (1 inch = 72 points)
- `pc` - a pica (1 pica = 12 points)

### 14.4. Relative units
- `em` - is the value assigned to that element's `font-size`, therefore its exact value changes between elements. It does not change depending on the font used, just on the font size. In typography, this measures the width of the `m` letter.
- `rem` - is similar to `em`, but instead of varying on the current element font size, it uses the root element (`html`) font size. You set that font size once, and `rem` will be a consistent measure across all the pages.
- `ex` - is like `em`, but instead of measuring the width of `m`, it measures the height of the `x` letter. It can change depending on the font used and the font size.
- `ch` - is like `ex` but instead of measuring the height of `x`, it measures the width of `0` (zero).

### 14.5. Viewport units
- `vw` - the viewport width unit represents a percentage of the viewport width. `50vw` means 50% of the viewport width.
- `vh` - the viewport height unit represents a percentage of the viewport height. `50vh` means 50% of the viewport height.
- `vmin` - the viewport minimum unit represents the minimum between the height or width in terms of percentage. `30vmin` is 30% of the current width or height, depending on which one is smaller.
- `vmax` - the viewport maximum unit represents the maximum between the height or width in terms of percentage. `30vmax` is 30% of the current width or height, depending on which one is bigger.

### 14.6. Fraction units
`fr` are fraction units, and they are used in CSS Grid to divide space into fractions.

We'll talk about them in the context of CSS Grid later on.

## 15. `url()`
When we talk about background images, `url()` function is used to load a resource:

```css
div { 
  background-image: url(test.png); 
} 
```

In this case, I used a relative URL, which searches the file in the folder where the CSS file is defined.

I could go one level back:
```css
div { 
  background-image: url(../test.png); 
} 
```

Or go into a folder:
```css
div { 
  background-image: url(subfolder/test.png); 
} 
```

Or I could load a file starting from the root of the domain where the CSS is hosted:
```css
div { 
  background-image: url(/test.png); 
} 
```

Or I could use an absolute URL to load an external resource:
```css
div { 
  background-image: url(https://mysite.com/test.png); 
} 

