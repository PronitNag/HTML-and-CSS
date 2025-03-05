## 32. Flexbox

Flexbox, also called **Flexible Box Module**, is one of the two modern layout systems, along with **CSS Grid**.

Compared to **CSS Grid** (which is bi-dimensional), flexbox is a one-dimensional layout model. It will control the layout based on a **row** or **column**, but not both at the same time.

The main goal of flexbox is to allow items to fill the whole space offered by their container, depending on some rules you set.

Unless you need to support old browsers like **IE8 and IE9**, Flexbox is the tool that lets you forget about using:

- Table layouts  
- Floats  
- clearfix hacks  
- `display: table` hacks  

Let's dive into flexbox and become a master of it in a very short time.

### 32.1. Browser support

At the time of writing (**Feb 2018**), it's supported by **97.66% of the users**. All the most important browsers have implemented it for years, so even older browsers (**including IE10+**) are covered.

While we must wait a few years for users to catch up on **CSS Grid**, Flexbox is an older technology and can be used right now.

### 32.2. Enable Flexbox

A flexbox layout is applied to a container by setting:

```css
display: flex;
```

or

```css
display: inline-flex;
```

The content inside the container will be aligned using flexbox.

### 32.3. Container properties

Some flexbox properties apply to the **container**, which sets the general rules for its items. They are:

- `flex-direction`
- `justify-content`
- `align-items`
- `flex-wrap`
- `flex-flow`

#### 32.3.1. Align rows or columns

The first property we see, `flex-direction`, determines if the container should align its items as rows or as columns:

- `flex-direction: row;` places items as a row, in the text direction *(left-to-right for western countries)*.
- `flex-direction: row-reverse;` places items just like `row` but in the opposite direction.
- `flex-direction: column;` places items in a column, ordering **top to bottom**.
- `flex-direction: column-reverse;` places items in a column, just like `column` but in the **opposite direction**.

#### 32.3.2. Vertical and horizontal alignment

By default, items start from the **left** if `flex-direction` is `row`, and from the **top** if `flex-direction` is `column`.

You can change this behavior using:

- `justify-content` → to change the **horizontal alignment**.
- `align-items` → to change the **vertical alignment**.

##### 32.3.2.1. Change the horizontal alignment

`justify-content` has 5 possible values:

- `flex-start`: align to the **left** side of the container.
- `flex-end`: align to the **right** side of the container.
- `center`: align at the **center** of the container.
- `space-between`: display with **equal spacing between them**.
- `space-around`: display with **equal spacing around them**.

##### 32.3.2.2. Change the vertical alignment

`align-items` has 5 possible values:

- `flex-start`: align to the **top** of the container.
- `flex-end`: align to the **bottom** of the container.
- `center`: align at the **vertical center** of the container.
- `baseline`: display at the **baseline** of the container.
- `stretch`: items are **stretched** to fit the container.

##### 32.3.2.3. A note on `baseline`

`baseline` looks similar to `flex-start` in this example, due to my boxes being too simple. Check out this **CodePen** to see a more useful example, originally created by **Martin Michálek**. As you can see there, **items' dimensions are aligned**.

#### 32.3.3. Wrap

By default, items in a flexbox container are kept on **a single line**, shrinking them to fit in the container.

To force the items to **spread across multiple lines**, use:

```css
flex-wrap: wrap;
```

This will distribute the items according to the order set in `flex-direction`. Use:

```css
flex-wrap: wrap-reverse;
```

to reverse this order.

A shorthand property called `flex-flow` allows you to specify `flex-direction` and `flex-wrap` in a **single line**, by adding the `flex-direction` value first, followed by the `flex-wrap` value. For example:

```css
flex-flow: row wrap;
```

### 32.4. Properties that apply to each single item

Until now, we've seen the properties you can apply to the **container**.

**Single items** can have a certain amount of **independence and flexibility**, and you can alter their appearance using these properties:

- `order`
- `align-self`
- `flex-grow`
- `flex-shrink`
- `flex-basis`
- `flex`

Let's see them in detail.

#### 32.4.1. Moving items before/after another one using `order`

Items are ordered based on the `order` they are assigned. By default, every item has `order: 0;` and the appearance in the HTML determines the final order.

You can override this property using `order` on each separate item. You can make an item appear **before all the others** by setting a **negative value**.

#### 32.4.2. Vertical alignment using `align-self`

An item can override the container's `align-items` setting using `align-self`, which has the **same 5 possible values** as `align-items`:

- `flex-start`: align to the **top** of the container.
- `flex-end`: align to the **bottom** of the container.
- `center`: align at the **vertical center** of the container.
- `baseline`: display at the **baseline** of the container.
- `stretch`: items are **stretched** to fit the container.

#### 32.4.3. Grow or shrink an item if necessary

##### 32.4.3.1. `flex-grow`

The default for any item is **0**.

If all items are defined as **1** and one is defined as **2**, the bigger element will take the space of **two "1" items**.

##### 32.4.3.2. `flex-shrink`

The default for any item is **1**.

If all items are defined as **1** and one is defined as **3**, the bigger element will shrink **3x the other ones**. When less space is available, it will take **3x less space**.

##### 32.4.3.3. `flex-basis`

- If set to `auto`, it sizes an item according to its **width or height**, and adds extra space based on the `flex-grow` property.
- If set to `0`, it does **not** add any extra space for the item when calculating the layout.
- If you specify a **pixel value**, it will use that as the length value (**width or height** depends if it's a **row or a column item**).

##### 32.4.3.4. `flex`

This property combines the **above 3 properties**:

```css
flex: flex-grow flex-shrink flex-basis;
```

Example:

```css
flex: 0 1 auto;

