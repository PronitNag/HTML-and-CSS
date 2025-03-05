# Semantic Elements in HTML

## What are Semantic Elements?
Semantic elements in HTML provide meaning to web content, making it more understandable for browsers, developers, and assistive technologies. These elements clearly define their purpose, improving accessibility and SEO.

## Common Semantic Elements

### Structural Elements
- `<header>`: Represents the introductory section, typically containing a logo, navigation, or heading.
- `<nav>`: Defines navigation links.
- `<main>`: Represents the main content of a page.
- `<section>`: Groups related content together.
- `<article>`: Represents an independent piece of content, such as a blog post or news article.
- `<aside>`: Contains side content, such as ads, links, or additional information.
- `<footer>`: Defines the footer of a document, often containing copyright information and links.

### Text and Content Elements
- `<mark>`: Highlights text.
- `<time>`: Represents a date or time.
- `<address>`: Defines contact information.
- `<figure>` & `<figcaption>`: Groups images with captions.
- `<details>` & `<summary>`: Creates an expandable/collapsible section.

## Benefits of Semantic Elements
- **Improved Readability:** Makes HTML more understandable for developers.
- **Better Accessibility:** Helps screen readers interpret content correctly.
- **SEO Optimization:** Search engines understand content structure better.
- **Consistency:** Standardizes webpage structure.

## Example Code
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Semantic Elements Example</title>
</head>
<body>
    <header>
        <h1>Welcome to My Website</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
    <main>
        <section>
            <h2>About Us</h2>
            <p>This is an example of semantic HTML elements.</p>
        </section>
        <article>
            <h2>Latest Blog Post</h2>
            <p>Using semantic HTML improves website accessibility and SEO.</p>
        </article>
    </main>
    <aside>
        <p>Related Links</p>
    </aside>
    <footer>
        <p>&copy; 2025 My Website</p>
    </footer>
</body>
</html>
```

## Conclusion
Using semantic elements makes HTML cleaner, more structured, and accessible. Always prefer semantic tags over generic `<div>` and `<span>` where possible.
