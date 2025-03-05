## 24. Padding

The `padding` CSS property is commonly used in CSS to add space on the inner side of an element.

### Remember:
- `margin` adds space **outside** an element border.
- `padding` adds space **inside** an element border.

### 24.1. Specific padding properties

`padding` has four related properties that alter the padding of a single edge at once:
- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

The usage of those is very simple and cannot be confused, for example:

```css
padding-left: 30px;
padding-right: 3em;
```

### 24.2. Using the `padding` shorthand

`padding` is a shorthand to specify multiple padding values at the same time, and depending on the number of values entered, it behaves differently.

#### 24.2.1. 1 value
Using a single value applies that to all the paddings: top, right, bottom, left.

```css
padding: 20px;
```

#### 24.2.2. 2 values
Using 2 values applies the first to bottom & top, and the second to left & right.

```css
padding: 20px 10px;
```

#### 24.2.3. 3 values
Using 3 values applies the first to top, the second to left & right, the third to bottom.

```css
padding: 20px 10px 30px;
```

#### 24.2.4. 4 values
Using 4 values applies the first to top, the second to right, the third to bottom, the fourth to left.

```css
padding: 20px 10px 5px 0px;
```

So, the order is **top-right-bottom-left**.

### 24.3. Values accepted

`padding` accepts values expressed in any kind of length unit. The most common ones are:
- `px`
- `em`
- `rem`

But many others exist.

---

## 25. Margin

The `margin` CSS property is commonly used in CSS to add space around an element.

### Remember:
- `margin` adds space **outside** an element border.
- `padding` adds space **inside** an element border.

### 25.1. Specific margin properties

`margin` has four related properties that alter the margin of a single edge at once:
- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

The usage of those is very simple and cannot be confused, for example:

```css
margin-left: 30px;
margin-right: 3em;
```

### 25.2. Using the `margin` shorthand

`margin` is a shorthand to specify multiple margins at the same time, and depending on the number of values entered, it behaves differently.

#### 25.2.1. 1 value
Using a single value applies that to all the margins: top, right, bottom, left.

```css
margin: 20px;
```

#### 25.2.2. 2 values
Using 2 values applies the first to bottom & top, and the second to left & right.

```css
margin: 20px 10px;
```

#### 25.2.3. 3 values
Using 3 values applies the first to top, the second to left & right, the third to bottom.

```css
margin: 20px 10px 30px;
```

#### 25.2.4. 4 values
Using 4 values applies the first to top, the second to right, the third to bottom, the fourth to left.

```css
margin: 20px 10px 5px 0px;
```

So, the order is **top-right-bottom-left**.

### 25.3. Values accepted

`margin` accepts values expressed in any kind of length unit. The most common ones are:
- `px`
- `em`
- `rem`

It also accepts percentage values and the special value `auto`.

### 25.4. Using `auto`

`auto` can be used to tell the browser to select a margin automatically, and it's most commonly used to center an element in this way:

```css
margin: 0 auto;
```

As said above, using 2 values applies the first to bottom & top, and the second to left & right.

The modern way to center elements is to use **Flexbox**, with its `justify-content: center;` directive.

Older browsers do not support Flexbox, so if you need compatibility:

```css
margin: 0 auto;
```

is still a good choice.

### 25.5. Using a negative margin

`margin` is the only property related to sizing that can have a **negative** value. It's extremely useful.

- Setting a negative **top margin** moves an element over elements before it, and given enough negative value, it will move out of the page.
- A negative **bottom margin** moves up the elements after it.
- A negative **right margin** makes the content of the element expand beyond its allowed content size.
- A negative **left margin** moves the element left over the elements that precede it, and given enough negative value, it will move out of the page.

