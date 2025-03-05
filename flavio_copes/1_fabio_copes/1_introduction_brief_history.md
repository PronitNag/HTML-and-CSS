## 2. Introduction to CSS

### 2.1. How does CSS look like

A CSS rule set has one part called **selector**, and the other part called **declaration**. The declaration contains various rules, each composed of a **property** and a **value**.

In this example, `p` is the selector, and applies one rule which sets the value `20px` to the `font-size` property:

```css
p {
  font-size: 20px;
}
```

Multiple rules are stacked one after the other:

```css
p {
  font-size: 20px;
}

a {
  color: blue;
}
```

A selector can target one or more items:

```css
p, a {
  font-size: 20px;
}
```

It can target HTML tags, like above, or HTML elements that contain a certain **class** attribute with `.my-class`, or HTML elements that have a specific **id** attribute with `#my-id`.

More advanced selectors allow you to choose items whose attribute matches a specific value, or also items which respond to **pseudo-classes** (more on that later).

### 2.2. Semicolons

Every CSS rule terminates with a semicolon. Semicolons are not optional, except after the last rule, but it is recommended to always use them for consistency and to avoid errors if another property is added later.

### 2.3. Formatting and indentation

There is no fixed rule for formatting. This CSS is valid:

```css
p {
  font-size: 20px;}
a {color: blue;
}
```

but difficult to read. Stick to some conventions, like those in the examples above:
- Keep selectors and the closing brackets aligned to the left.
- Indent **2 spaces** for each rule.
- Place the opening bracket on the same line as the selector, separated by one space.

Correct and consistent use of spacing and indentation is a visual aid in understanding your code.

---

## 3. A Brief History of CSS

Before moving on, here is a brief recap of the history of CSS.

CSS evolved from the necessity of styling web pages. Before CSS was introduced, web pages looked very similar and "academic" in design. There were limited options for personalization.

HTML 3.2 introduced the option of defining colors inline as HTML element attributes and presentational tags like `<center>` and `<font>`, but this quickly led to a messy and inefficient approach.

CSS allowed for separating **presentation** from **structure**, enabling HTML to focus on defining document structure rather than styling.

CSS is continuously evolving, and techniques that were standard **5 years ago** might now be outdated due to new advancements and browser changes.

### The Early Days of CSS

In the early days, several competing browsers—such as **Internet Explorer** and **Netscape Navigator**—styled pages using HTML-based presentational tags. This approach had several limitations:
- Limited customization opportunities.
- Styling was dependent on the browser.
- Websites were built specifically for one browser due to proprietary, non-standard tags.

As a result, the need for a **universal styling language** became clear.

### Evolution of CSS

- **1994**: Initial idea proposed.
- **1996**: CSS Level 1 (**CSS 1**) recommendation published.
- **1998**: CSS Level 2 (**CSS 2**) published.
- **2002**: First browser to implement the full CSS specification was **Internet Explorer for Mac** (as detailed in this [CSS-Tricks post](https://css-tricks.com/lookback-history-css/)).

Internet Explorer had a major issue with incorrectly implementing the **box model**, leading to years of workarounds and hacks to achieve cross-browser consistency.

### CSS Today

Today, CSS is more powerful than ever. Most browsers adhere to the standards, reducing the need for hacks and workarounds. Instead of numbered versions, the **CSS Working Group** now releases periodic "snapshots" of stable modules.

- The latest snapshot (as of 2018) can be found here: [W3C CSS Snapshot](https://www.w3.org/TR/css-2018/).
- **CSS Level 2** remains the foundation for modern CSS, with many additional features built on top of it.

CSS continues to evolve, offering **flexible**, **efficient**, and **powerful** styling capabilities for web development.


