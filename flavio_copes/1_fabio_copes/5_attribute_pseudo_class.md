## 10. Attribute Selectors

We already introduced several of the basic CSS selectors: using element selectors, class, id, how to combine them, how to target multiple classes, how to style several selectors in the same rule, how to follow the page hierarchy with child and direct child selectors, and adjacent siblings.

In this section, we'll analyze attribute selectors, and we'll talk about pseudo-class and pseudo-element selectors in the next two sections.

### 10.1 Attribute Presence Selectors

The first selector type is the attribute presence selector. We can check if an element has an attribute using the `[]` syntax.

This will select all `<p>` tags in the page that have an `id` attribute, regardless of its value:

```css
p[id] {
  /* ... */
}
```

### 10.2 Exact Attribute Value Selectors

Inside the brackets, you can check the attribute value using `=`, and the CSS will be applied only if the attribute matches the exact value specified:

```css
p[id='my-id'] {
  /* ... */
}
```

### 10.3 Match an Attribute Value Portion

While `=` lets us check for an exact value, we have other operators:

- `*=` checks if the attribute contains the partial value.
- `^=` checks if the attribute starts with the partial value.
- `$=` checks if the attribute ends with the partial value.
- `|=` checks if the attribute starts with the partial value and is followed by a dash (common in classes, for example) or just contains the partial value.
- `~=` checks if the partial value is contained in the attribute but separated by spaces from the rest.

All the checks mentioned above are case-sensitive. If you add an `i` just before the closing bracket, the check will be case-insensitive. It's supported in many browsers but not all. Check [Can I use](https://caniuse.com/#feat=css-case-insensitive) for compatibility.

## 11. Pseudo-classes

Pseudo-classes are predefined keywords used to select an element based on its state or to target a specific child.

They start with a single colon `:`.

They can be used as part of a selector and are very useful to style active or visited links, change the style on hover or focus, or target the first child or odd rows. Very handy in many cases.

### Common Pseudo-classes

| Pseudo-class | Targets |
|-------------|---------|
| `:active` | An element being activated by the user (e.g., clicked). Mostly used on links or buttons. |
| `:checked` | A checkbox, option, or radio input type that is enabled. |
| `:default` | The default in a set of choices (e.g., an option in a select or radio buttons). |
| `:disabled` | A disabled element. |
| `:empty` | An element with no children. |
| `:enabled` | An element that's enabled (opposite to `:disabled`). |
| `:first-child` | The first child of a group of siblings. |
| `:focus` | The element with focus. |
| `:hover` | An element hovered with the mouse. |
| `:last-child` | The last child of a group of siblings. |
| `:link` | A link that has not been visited. |
| `:not(selector)` | Any element not matching the selector passed (e.g., `:not(span)`). |
| `:nth-child(n)` | An element matching the specified position. |
| `:nth-last-child(n)` | An element matching the specific position, starting from the end. |
| `:only-child` | An element without any siblings. |
| `:required` | A form element with the `required` attribute set. |
| `:root` | Represents the `html` element. Useful in CSS variables. |
| `:target` | The element matching the current URL fragment (for inner navigation in the page). |
| `:valid` | Form elements that validated client-side successfully. |
| `:visited` | A link that has been visited. |

### Example

A common example: You want to style a link, so you create a CSS rule to target the `<a>` element:

```css
a {
  color: yellow;
}
```

Things seem to work fine until you click a link. The link goes back to the predefined color (blue) when you click it. Then, when you open the link and go back to the page, the link is now blue.

Why does that happen?

Because the link changes state when clicked and enters the `:active` state. And when it has been visited, it enters the `:visited` state (forever, until the user clears their browsing history).

To correctly make the link yellow across all states, you need to write:

```css
a,
a:visited,
a:active {
  color: yellow;
}
```

### `:nth-child()` Usage

The `:nth-child()` pseudo-class deserves special mention. It can be used to target odd or even children:

```css
:nth-child(odd) {
  /* Styles for odd elements */
}

:nth-child(even) {
  /* Styles for even elements */
}
```

It is commonly used in lists to color odd lines differently from even lines:

```css
ul:nth-child(odd) {
  color: white;
  background-color: black;
}
```

You can also use it to target the first three children of an element:

```css
:nth-child(-n+3) {
  /* Styles for the first three children */
}
```

Or to style every fifth element:

```css
:nth-child(5n) {
  /* Styles for every fifth element */
}
```

Some pseudo-classes are just used for printing, like `:first`, `:left`, and `:right`, allowing you to target the first page, all left pages, and all right pages, which are usually styled slightly differently.


