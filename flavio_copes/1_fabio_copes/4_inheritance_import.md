## 8. Inheritance

When you set some properties on a selector in CSS, they are inherited by all
the children of that selector.

I said *some*, because not all properties show this behavior. This happens because some properties make sense to be inherited. This helps
us write CSS much more concisely since we don't have to explicitly set that
property again on every single child.

Some other properties make more sense to not be inherited. Think about fonts: you don't need to apply the `font-family` to every single
tag of your page. You set the `body` tag font, and every child inherits it,
along with other properties.

The `background-color` property, on the other hand, makes little sense to be inherited.

### 8.1. Properties that inherit

Here is a list of the properties that do inherit. The list is non-comprehensive,
but these are just the most popular ones you'll likely use:

- `border-collapse`
- `border-spacing`
- `caption-side`
- `color`
- `cursor`
- `direction`
- `empty-cells`
- `font-family`
- `font-size`
- `font-style`
- `font-variant`
- `font-weight`
- `font-size-adjust`
- `font-stretch`
- `font`
- `letter-spacing`
- `line-height`
- `list-style-image`
- `list-style-position`
- `list-style-type`
- `list-style`
- `orphans`
- `quotes`
- `tab-size`
- `text-align`
- `text-align-last`
- `text-decoration-color`
- `text-indent`
- `text-justify`
- `text-shadow`
- `text-transform`
- `visibility`
- `white-space`
- `widows`
- `word-break`
- `word-spacing`

### 8.2. Forcing properties to inherit

What if you have a property that's not inherited by default, and you want it
to be inherited in a child?

In the child, you set the property value to the special keyword `inherit`.

**Example:**

```css
body {
  background-color: yellow;
}
p {
  background-color: inherit;
}
```

### 8.3. Forcing properties to NOT inherit

On the contrary, you might have a property inherited and you want to avoid
that.

You can use the `revert` keyword to revert it. In this case, the value is
reverted to the original value the browser gave it in its default stylesheet.

In practice, this is rarely used, and most of the time, you'll just set another
value for the property to overwrite that inherited value.

### 8.4. Other special values

In addition to the `inherit` and `revert` special keywords we just saw, you
can also set any property to:

- **`initial`**: Uses the default browser stylesheet if available. If not, and if
the property inherits by default, inherit the value. Otherwise, do nothing.
- **`unset`**: If the property inherits by default, inherit. Otherwise, do nothing.

## 9. Import

From any CSS file, you can import another CSS file using the `@import` directive.

Here is how you use it:

```css
@import url(myfile.css);
```

`@import url()` can manage absolute or relative URLs.

One important thing you need to know is that `@import` directives must be
placed before any other CSS in the file, or they will be ignored.

You can use media descriptors to only load a CSS file for specific media:

```css
@import url(myfile.css) all;
@import url(myfile-screen.css) screen;
@import url(myfile-print.css) print;
