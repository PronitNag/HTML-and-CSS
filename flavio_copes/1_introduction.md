# The CSS Handbook

## 1. Preface

I wrote this book to help you quickly learn CSS and get familiar with the advanced CSS topics.

CSS, a shorthand for Cascading Style Sheets, is one of the main building blocks of the Web. Its history goes back to the '90s, and along with HTML, it has changed a lot since its humble beginnings.

Having created websites since before CSS existed, I have seen its evolution. CSS is an amazing tool, and in the last few years, it has grown a lot, introducing many fantastic features like CSS Grid, Flexbox, and CSS Custom Properties.

This handbook is aimed at a vast audience.

First, the beginner. I explain CSS from zero in a succinct but comprehensive way, so you can use this book to learn CSS from the basics.

Then, the professional. CSS is often considered like a secondary thing to learn, especially by JavaScript developers. They know CSS is not a real programming language, they are programmers and therefore they should not bother learning CSS the right way. I wrote this book for you, too.

Next, the person that knows CSS from a few years but hasn't had the opportunity to learn the new things in it. We'll talk extensively about the new features of CSS, the ones that are going to build the web of the next decade.

CSS has improved a lot in the past few years and it's evolving fast.

Even if you don't write CSS for a living, knowing how CSS works can help save you some headaches when you need to understand it from time to time, for example while tweaking a web page.

CSS (an abbreviation of Cascading Style Sheets) is the language that we use to style an HTML file, and tell the browser how should it render the elements on the page.

In this book, I talk exclusively about styling HTML documents, although CSS can be used to style other things too.

A CSS file contains several CSS rules. Each rule is composed of two parts:
- The **selector**
- The **declaration block**

The selector is a string that identifies one or more elements on the page, following a special syntax that we'll soon talk about extensively.

The declaration block contains one or more declarations, in turn composed of a **property** and **value** pair.

Those are all the things we have in CSS. Carefully organizing properties, associating them with values, and attaching those to specific elements of the page using a selector is the whole argument of this ebook.

## 2. Introduction to CSS

### 2.1. How does CSS look like

A CSS rule set has one part called **selector**, and the other part called **declaration**. The declaration contains various rules, each composed of a **property** and a **value**.

Example:

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

It can target HTML tags, classes (`.my-class`), or IDs (`#my-id`).

### 2.2. Semicolons

Every CSS rule terminates with a **semicolon** (`;`). Semicolons are not optional, except after the last rule, but I suggest always using them for consistency and to avoid errors.

### 2.3. Formatting and indentation

There is no fixed rule for formatting. This CSS is valid but hard to read:

```css
p { font-size: 20px;}
a {color: blue; }
```

A better approach is:

```css
p {
  font-size: 20px;
}

a {
  color: blue;
}
```

Correct and consistent use of spacing and indentation is a visual aid in understanding your code.

## 3. A Brief History of CSS

Before moving on, I want to give you a brief recap of the history of CSS.

CSS was grown out of the necessity of styling web pages. Before CSS was introduced, people wanted a way to style their web pages, which looked all very similar and "academic" back in the day. You couldn't do much in terms of personalization.

HTML 3.2 introduced the option of defining colors inline as HTML element attributes, and presentational tags like `<center>` and `<font>`, but that quickly escalated into a far from ideal situation.

CSS let us move everything presentation-related from the HTML to the CSS so that HTML could get back to defining the structure of the document, rather than how things should look in the browser.

CSS is continuously evolving, and CSS you used five years ago might just be outdated, as new idiomatic CSS techniques emerged and browsers changed.

It's hard to imagine the times when CSS was born and how different the web was. At the time, we had several competing browsers, the main ones being Internet Explorer and Netscape Navigator.

Pages were styled by using HTML, with special presentational tags and attributes, most of which are now deprecated. This meant you had a limited amount of customization opportunities. The bulk of the styling decisions were left to the browser.

After the initial idea proposed in 1994, CSS got its first release in 1996, when the **CSS Level 1** recommendation was published. CSS Level 2 (**CSS 2**) got published in 1998.

Since then, work began on **CSS Level 3**. The CSS Working Group decided to split every feature and work on it separately, in modules.

Browsers weren't especially fast at implementing CSS. We had to wait until 2002 to have the first browser implement the full CSS specification: **IE for Mac**.

Internet Explorer implemented the box model incorrectly right from the start, which led to years of pain trying to have the same style applied consistently across browsers. We had to use various tricks and hacks to make browsers render things as we wanted.

Today, things are much, much better. We can just use the CSS standards without thinking about quirks, most of the time, and CSS has never been more powerful.

We don't have official release numbers for CSS anymore now, but the CSS Working Group releases a "snapshot" of the modules that are currently considered stable and ready to be included in browsers. The latest snapshot is from **2018**.

CSS Level 2 is still the base for the CSS we write today, and we have many more features built on top of it.

---

This is a structured Markdown conversion of the provided text. Let me know if you need any modifications or additional formatting!
