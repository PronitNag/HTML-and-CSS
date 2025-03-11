# Inline vs Block Elements in HTML

## Introduction
HTML elements are categorized as **inline** or **block** based on how they behave in the document flow. Understanding these differences is essential for structuring web pages effectively.

## Block Elements
Block elements **start on a new line** and **take up the full width** available by default. They create distinct sections in the document.

### Common Block Elements
- `<div>` - A generic container for content.
- `<p>` - Defines a paragraph.
- `<h1>` to `<h6>` - Headings of various sizes.
- `<ul>` / `<ol>` - Unordered and ordered lists.
- `<li>` - List items.
- `<table>` - Defines a table.
- `<section>` - Represents a section in a document.
- `<article>` - Represents independent content.
- `<header>` - Represents introductory content.
- `<footer>` - Represents footer content.

### Example
```html
<p>This is a paragraph.</p>
<div>
  <h2>Block elements</h2>
  <p>They start on a new line and take full width.</p>
</div>
```

## Inline Elements
Inline elements **do not start on a new line** and **only take up as much width as necessary**. They are typically used for formatting text within block elements.

### Common Inline Elements
- `<span>` - A generic inline container.
- `<a>` - Anchor (hyperlink).
- `<strong>` - Bold text (important for semantics).
- `<em>` - Italicized text (for emphasis).
- `<b>` - Bold text (without semantic meaning).
- `<i>` - Italicized text (without semantic meaning).
- `<img>` - Displays an image.
- `<code>` - Represents inline code.
- `<mark>` - Highlights text.

### Example
```html
<p>This is <strong>bold</strong> and <em>italic</em> text.</p>
<a href="https://example.com">Visit Example</a>
```

## Key Differences Between Block and Inline Elements
| Feature            | Block Elements                  | Inline Elements              |
|--------------------|--------------------------------|------------------------------|
| Starts on new line? | Yes                            | No                           |
| Takes full width?  | Yes                            | No (only necessary width)    |
| Used for structure? | Yes                            | No (used for formatting)     |

## Conclusion
Understanding inline and block elements helps in designing well-structured web pages. Block elements define layout sections, while inline elements control formatting within those sections.
