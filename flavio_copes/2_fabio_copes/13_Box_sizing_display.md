26. Box Sizing
 The default behavior of browsers when calculating the width of an element is
 to apply the calculated width and height to the content area, without taking
 any of the padding, border and margin in consideration.
 This approach has proven to be quite complicated to work with.
 You can change this behavior by setting the 
box-sizing  property.
 The 
box-sizing  property is a great help. It has 2 values:
 border-box 
content-box 
content-box  is the default, the one we had for ages before 
became a thing.
 box-sizing 
border-box  is the new and great thing we are looking for. If you set that on
 an element:
 85
.my-div { 
box-sizing: border-box; 
} 
width and height calculation include the padding and the border. Only the
 margin is left out, which is reasonable since in our mind we also typically see
 that as a separate thing: margin is outside of the box.
 This property is a small change but has a big impact. CSS Tricks even
 declared an international box-sizing awareness day, just saying, and it's
 recommended to apply it to every element on the page, out of the box, with
 this:
 *, 
*:before, 
*:after { 
  box-sizing: border-box; 
} 
27. Display
 The 
display  property of an object determines how it is rendered by the
 browser.
 It's a very important property, and probably the one with the highest number
 of values you can use.
 Those values include:
 block 
inline 
none 
contents 
flow 
flow-root 
table  (and all the 
table-*  ones)
 86
flex 
grid 
list-item 
inline-block 
inline-table 
inline-flex 
inline-grid 
inline-list-item 
plus others you will not likely use, like 
ruby .
 Choosing any of those will considerably alter the behavior of the browser
 with the element and its children.
 In this section we'll analyze the most important ones not covered elsewhere:
 block 
inline 
inline-block 
none 
We'll see some of the others in later chapters, including coverage of 
flex  and 
grid .
 27.1. 
inline 
Inline is the default display value for every element in CSS.
 div , p  and 
table ,
 All the HTML tags are displayed inline out of the box except some elements
 like 
section , which are set as 
block  by the user agent (the
 browser).
 Inline elements don't have any margin or padding applied.
 Same for height and width.
 You can add them, but the appearance in the page won't change - they are
 calculated and applied automatically by the browser.
 87
27.2. 
inline-block 
Similar to 
inline , but with 
inline-block  
as you specified.
 27.3. 
block 
width  and 
height  are applied
 As mentioned, normally elements are displayed inline, with the exception of
 some elements, including
 div 
p 
section 
ul 
which are set as 
block  by the browser.
 With 
display: block , elements are stacked one after each other, vertically,
 and every element takes up 100% of the page.
 The values assigned to the 
width  and 
height  properties are respected, if
 you set them, along with 
margin  and 
padding .
 27.4. 
none 
Using 
display: none  makes an element disappear. It's still there in the
 HTML, but just not visible in the browser
