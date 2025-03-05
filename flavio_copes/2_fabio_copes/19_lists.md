## 35. Lists

Lists are a very important part of many web pages. CSS can style them using several properties.

### list-style-type

`list-style-type` is used to set a predefined marker to be used by the list:

```css
li { 
  list-style-type: square; 
} 
```

We have lots of possible values, which you can see [here](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type) with examples of their appearance. Some of the most popular ones are `disc`, `circle`, `square`, and `none`.

### list-style-image

`list-style-image` is used to use a custom marker when a predefined marker is not appropriate:

```css
li { 
  list-style-image: url(list-image.png); 
} 
```

### list-style-position

`list-style-position` lets you add the marker `outside` (the default) or `inside` of the list content, in the flow of the page rather than outside of it:

```css
li { 
  list-style-position: inside; 
} 
```

### list-style shorthand

The `list-style` shorthand property lets us specify all those properties in the same line:

```css
li { 
  list-style: url(list-image.png) inside; 
} 

