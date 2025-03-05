# The CSS Handbook

## 1. Preface

## 2. Introduction to CSS
### 2.1. How does CSS look like
### 2.2. Semicolons
### 2.3. Formatting and indentation

## 3. A brief history of CSS

## 4. Adding CSS to an HTML page
### 4.1. Using the `<link>` tag
### 4.2. Using the `<style>` tag
### 4.3. Inline styles

## 5. Selectors
### 5.1. Basic selectors
### 5.2. Combining selectors
#### 5.2.1. Targeting an element with a class or id
#### 5.2.2. Targeting multiple classes
#### 5.2.3. Combining classes and ids
### 5.3. Grouping selectors
### 5.4. Follow the document tree with selectors

## 6. Cascade

## 7. Specificity
### 7.1. How to calculate specificity
#### 7.1.1. Slot 1
#### 7.1.2. Slot 2
#### 7.1.3. Slot 3
#### 7.1.4. Slot 4
### 7.2. Importance
### 7.3. Tips
### 7.4. Tools to calculate the specificity

## 8. Inheritance
### 8.1. Properties that inherit
### 8.2. Forcing properties to inherit
### 8.3. Forcing properties to NOT inherit
### 8.4. Other special values

## 9. Import

## 10. Attribute selectors
### 10.1. Attribute presence selectors
### 10.2. Exact attribute value selectors
### 10.3. Match an attribute value portion

## 11. Pseudo-classes

## 12. Pseudo-elements

## 13. Colors
### 13.1. Named colors
### 13.2. RGB and RGBa
### 13.3. Hexadecimal notation
### 13.4. HSL and HSLa

## 14. Units
### 14.1. Pixels
### 14.2. Percentages
### 14.3. Real-world measurement units
### 14.4. Relative units
### 14.5. Viewport units
### 14.6. Fraction units

## 15. `url()`

## 16. `calc()`

## 17. Backgrounds

## 18. Comments

## 19. Custom Properties
### 19.1. The basics of using variables
### 19.2. Create variables inside any element
### 19.3. Variables scope
### 19.4. Interacting with a CSS Variable value using JavaScript
### 19.5. Handling invalid values
### 19.6. Browser support
### 19.7. CSS Variables are case sensitive
### 19.8. Math in CSS Variables
### 19.9. Media queries with CSS Variables
### 19.10. Setting a fallback value for `var()`

## 20. Fonts
### 20.1. `font-family`
### 20.2. `font-weight`
### 20.3. `font-stretch`
### 20.4. `font-style`
### 20.5. `font-size`
### 20.6. `font-variant`
### 20.7. `font`
### 20.8. Loading custom fonts using `@font-face`
### 20.9. A note on performance

## 21. Typography
### 21.1. `text-transform`
### 21.2. `text-decoration`
### 21.3. `text-align`
### 21.4. `vertical-align`
### 21.5. `line-height`
### 21.6. `text-indent`
### 21.7. `text-align-last`
### 21.8. `word-spacing`
### 21.9. `letter-spacing`
### 21.10. `text-shadow`
### 21.11. `white-space`
### 21.12. `tab-size`
### 21.13. `writing-mode`
### 21.14. `hyphens`
### 21.15. `text-orientation`
### 21.16. `direction`
### 21.17. `word-break`
### 21.18. `overflow-wrap`

## 22. Box Model

## 23. Border
### 23.1. The border style
### 23.2. The border width
### 23.3. The border color
### 23.4. The border shorthand property
### 23.5. The border radius
### 23.6. Using images as borders

## 24. Padding
### 24.1. Specific padding properties
### 24.2. Using the `padding` shorthand
#### 24.2.1. 1 value
#### 24.2.2. 2 values
#### 24.2.3. 3 values
#### 24.2.4. 4 values
### 24.3. Values accepted

## 25. Margin
### 25.1. Specific margin properties
### 25.2. Using the `margin` shorthand
#### 25.2.1. 1 value
#### 25.2.2. 2 values
#### 25.2.3. 3 values
#### 25.2.4. 4 values
### 25.3. Values accepted
### 25.4. Using `auto` to center elements
### 25.5. Using a negative margin

## 26. Box Sizing

## 27. Display
### 27.1. `inline`
### 27.2. `inline-block`
### 27.3. `block`
### 27.4. `none`

## 28. Positioning
### 28.1. Static positioning
### 28.2. Relative positioning
### 28.3. Absolute positioning
### 28.4. Fixed positioning
### 28.5. Sticky positioning

## 29. Floating and clearing
### 29.1. Clearing

## 30. z-index

## 31. CSS Grid
### 31.1. The basics
#### 31.1.1. `grid-template-columns` and `grid-template-rows`
#### 31.1.2. Automatic dimensions
#### 31.1.3. Different columns and rows dimensions

## 32. Flexbox
### 32.1. Browser support
### 32.2. Enable Flexbox
### 32.3. Container properties

## 33. Tables

## 34. Centering

## 35. Lists

## 36. Media queries and responsive design

## 37. Feature Queries

## 38. Filters

## 39. Transforms

## 40. Transitions

## 41. Animations

## 42. Normalizing CSS

## 43. Error handling

## 44. Vendor prefixes

## 45. CSS for print

This book is designed to help you quickly learn CSS from basics to advanced topics, covering everything from selectors to Flexbox and CSS Grid.

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
