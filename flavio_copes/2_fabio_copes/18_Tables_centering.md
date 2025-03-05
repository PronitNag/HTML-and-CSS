## 33. Tables

**flex: 0 1 auto**  
Tables in the past were greatly overused in CSS, as they were one of the only ways we could create a fancy page layout.  
Today with Grid and Flexbox we can move tables back to the job they were intended to do: styling tables.  

Let's start from the HTML. This is a basic table:

```html
<table>
  <thead>
    <tr>
      <th scope="col">Name</th>
      <th scope="col">Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Flavio</th>
      <td>36</td>
    </tr>
    <tr>
      <th scope="row">Roger</th>
      <td>7</td>
    </tr>
  </tbody>
</table>
```

By default, it's not very attractive. The browser provides some standard styles, and that's it.  
We can use CSS to style all the elements of the table, of course.

### Styling the Table

Let's start with the border. A nice border can go a long way.  
We can apply it on the `<table>` element, and on the inner elements too, like `<th>` and `<td>`:

```css
table, th, td {
  border: 1px solid #333;
}
```

If we pair it with some margin, we get a nice result.

One common thing with tables is the ability to add a color to one row, and a different color to another row.  
This is possible using the `:nth-child(even)` selector:

```css
tbody tr:nth-child(odd) {
  background-color: #af47ff;
}
```

If you add `border-collapse: collapse;` to the table element, all borders are collapsed into one:

```css
table {
  border-collapse: collapse;
}
```

---

## 34. Centering

Centering things in CSS is a task that is very different if you need to center horizontally or vertically.  
In this post, I explain the most common scenarios and how to solve them.  
If a new solution is provided by Flexbox, I ignore the old techniques because we need to move forward, and Flexbox has been supported by browsers for years, including IE10.

### 34.1. Center Horizontally

#### 34.1.1. Text

Text is very simple to center horizontally using the `text-align` property set to `center`:

```css
p {
  text-align: center;
}
```

#### 34.1.2. Blocks

The modern way to center anything that is not text is to use Flexbox:

```css
#mysection {
  display: flex;
  justify-content: center;
}
```

Any element inside `#mysection` will be horizontally centered.

Here is the alternative approach if you don't want to use Flexbox.  
Anything that is not text can be centered by applying an automatic margin to the left and right and setting the width of the element:

```css
section {
  margin: 0 auto;
  width: 50%;
}
```

The above `margin: 0 auto;` is a shorthand for:

```css
section {
  margin-top: 0;
  margin-bottom: 0;
  margin-left: auto;
  margin-right: auto;
}
```

Remember to set the item to `display: block;` if it's an inline element.

### 34.2. Center Vertically

Traditionally, this has always been a difficult task. Flexbox now provides us with a great way to do this in the simplest possible way:

```css
#mysection {
  display: flex;
  align-items: center;
}
```

Any element inside `#mysection` will be vertically centered.

### 34.3. Center Both Vertically and Horizontally

Flexbox techniques to center vertically and horizontally can be combined to completely center an element in the page:

```css
#mysection {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

The same can be done using CSS Grid:

```css
body {
  display: grid;
  place-items: center;
  height: 100vh;
}

