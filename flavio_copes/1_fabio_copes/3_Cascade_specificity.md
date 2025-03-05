
## 6. Cascade

Cascade is a fundamental concept of CSS. After all, it's in the name itself, the first C of CSS - **Cascading Style Sheets** - it must be an important thing.

### What does it mean?

Cascade is the process, or algorithm, that determines the properties applied to each element on the page. Trying to converge from a list of CSS rules that are defined in various places.

It does so taking into consideration:

- Specificity
- Importance
- Inheritance
- Order in the file

It also takes care of resolving conflicts.

Two or more competing CSS rules for the same property applied to the same element need to be elaborated according to the CSS spec, to determine which one needs to be applied.

Even if you just have one CSS file loaded by your page, there is other CSS that is going to be part of the process. We have the **browser (user agent) CSS**. Browsers come with a default set of rules, all different between browsers. Then your CSS comes into play. Then the browser applies any **user stylesheet**, which might also be applied by browser extensions.

All those rules come into play while rendering the page.

We'll now see the concepts of **specificity** and **inheritance**.

---

## 7. Specificity

What happens when an element is targeted by multiple rules, with different selectors, that affect the same property?

For example, let's talk about this element:

```html
<p class="dog-name">Roger</p>
```

We can have:

```css
.dog-name { 
    color: yellow; 
} 
```

And another rule that targets:

```css
p { 
    color: red; 
} 
```

And another rule that targets:

```css
p.dog-name {
    color: blue;
}
```

Which rule is going to take precedence over the others, and why?

**Enter specificity.** The more specific rule will win. If two or more rules have the same specificity, the one that appears last wins.

Sometimes what is more specific in practice is a bit confusing to beginners. I would say it's also confusing to experts that do not look at those rules that frequently or simply overlook them.

---

### 7.1. How to calculate specificity

Specificity is calculated using a convention.

We have **4 slots**, and each one of them starts at **0 0 0 0**. The slot at the left is the most important, and the rightmost one is the least important.

Like it works for numbers in the decimal system:

- `1 0 0 0` is higher than `0 1 0 0`.

#### 7.1.1. Slot 1

The first slot, the rightmost one, is the least important. We increase this value when we have an **element selector**.

Examples:

```css
p { } /* 0 0 0 1 */
span { } /* 0 0 0 1 */
p span { } /* 0 0 0 2 */
p > span { } /* 0 0 0 2 */
div p > span { } /* 0 0 0 3 */
```

#### 7.1.2. Slot 2

The second slot is incremented by 3 things:

- **Class selectors**
- **Pseudo-class selectors**
- **Attribute selectors**

Examples:

```css
.name { } /* 0 0 1 0 */
.users .name { } /* 0 0 2 0 */
[href$='.pdf'] { } /* 0 0 1 0 */
:hover { } /* 0 0 1 0 */
```

Of course, slot 2 selectors can be combined with slot 1 selectors:

```css
div .name { } /* 0 0 1 1 */
a[href$='.pdf'] { } /* 0 0 1 1 */
.pictures img:hover { } /* 0 0 2 1 */
```

A trick with classes is that repeating the same class increases specificity:

```css
.name { } /* 0 0 1 0 */
.name.name { } /* 0 0 2 0 */
.name.name.name { } /* 0 0 3 0 */
```

#### 7.1.3. Slot 3

Slot 3 holds the most important thing that can affect your CSS specificity: the **id**.

Examples:

```css
#name { } /* 0 1 0 0 */
.user #name { } /* 0 1 1 0 */
#name span { } /* 0 1 0 1 */
```

#### 7.1.4. Slot 4

Slot 4 is affected by **inline styles**.

Example:

```html
<p style="color: red">Test</p>  /* 1 0 0 0 */
```

Even if any other rule in the CSS defines the color, this inline style rule is going to be applied.

---

### 7.2. Importance

Specificity does not matter if a rule ends with `!important`:

```css
p { 
    font-size: 20px !important; 
} 
```

That rule will take precedence over any rule with more specificity. The only way another rule can take precedence is to have `!important` as well and have higher specificity in the other less important slots.

---

### 7.3. Tips

- Use the amount of specificity you need, but not more.
- `!important` is debated among CSS experts. It should be used sparingly.
- Using the `id` attribute for styling is also debated. A better alternative is using **classes**, which have less specificity and are easier to work with.

---

### 7.4. Tools to calculate specificity

You can use the site [Specificity Calculator](https://specificity.keegan.st/) to perform specificity calculations automatically. It's useful for debugging and learning how specificity works in CSS.
