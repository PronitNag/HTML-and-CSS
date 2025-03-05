# HTML Element Attributes

## What are HTML Attributes?
HTML attributes provide additional information about elements. They are always specified in the opening tag and usually come in name/value pairs like `name="value"`.

## Commonly Used HTML Attributes

### 1. `id` Attribute
- Specifies a unique identifier for an HTML element.
- Example:
  ```html
  <p id="intro">This is an introduction.</p>
  ```

### 2. `class` Attribute
- Defines one or more class names for an element, which can be used in CSS or JavaScript.
- Example:
  ```html
  <div class="container">Content here</div>
  ```

### 3. `style` Attribute
- Used to apply inline CSS styles to an element.
- Example:
  ```html
  <p style="color: blue; font-size: 20px;">Styled text</p>
  ```

### 4. `title` Attribute
- Provides additional information (tooltip) when the user hovers over an element.
- Example:
  ```html
  <abbr title="World Health Organization">WHO</abbr>
  ```

### 5. `href` Attribute
- Used in `<a>` (anchor) tags to specify the URL of the linked page.
- Example:
  ```html
  <a href="https://www.example.com">Visit Example</a>
  ```

### 6. `src` Attribute
- Specifies the source URL of an image, script, or other media.
- Example:
  ```html
  <img src="image.jpg" alt="An image">
  ```

### 7. `alt` Attribute
- Provides alternative text for an image (important for accessibility and SEO).
- Example:
  ```html
  <img src="image.jpg" alt="A beautiful scenery">
  ```

### 8. `width` and `height` Attributes
- Define the dimensions of an image or iframe.
- Example:
  ```html
  <img src="image.jpg" width="300" height="200">
  ```

### 9. `type` Attribute
- Specifies the type of input element or button behavior.
- Example:
  ```html
  <input type="text" placeholder="Enter your name">
  ```

### 10. `placeholder` Attribute
- Provides a hint inside input fields.
- Example:
  ```html
  <input type="email" placeholder="Enter your email">
  ```

### 11. `disabled` Attribute
- Disables an input field, button, or form control.
- Example:
  ```html
  <button disabled>Submit</button>
  ```

### 12. `readonly` Attribute
- Makes an input field read-only.
- Example:
  ```html
  <input type="text" value="Read-only text" readonly>
  ```

### 13. `required` Attribute
- Specifies that an input field must be filled before submitting a form.
- Example:
  ```html
  <input type="text" required>
  ```

### 14. `checked` Attribute
- Used in radio buttons and checkboxes to preselect an option.
- Example:
  ```html
  <input type="checkbox" checked> Subscribe
  ```

### 15. `name` Attribute
- Specifies a name for form elements.
- Example:
  ```html
  <input type="text" name="username">
  ```

### 16. `value` Attribute
- Defines the initial value of an input field.
- Example:
  ```html
  <input type="text" value="Default text">
  ```

### 17. `maxlength` and `minlength` Attributes
- Define character limits for input fields.
- Example:
  ```html
  <input type="text" maxlength="10" minlength="3">
  ```

### 18. `pattern` Attribute
- Defines a regex pattern for input validation.
- Example:
  ```html
  <input type="text" pattern="[A-Za-z]+" title="Only letters allowed">
  ```

### 19. `target` Attribute
- Used in anchor tags to specify how a link should open.
- Example:
  ```html
  <a href="https://example.com" target="_blank">Open in new tab</a>
  ```

### 20. `download` Attribute
- Used in anchor tags to specify that the file should be downloaded instead of opened.
- Example:
  ```html
  <a href="file.pdf" download>Download File</a>
  ```

## Global Attributes
These attributes can be used on any HTML element:

- `id` - Specifies a unique ID.
- `class` - Assigns a CSS class.
- `style` - Inline CSS.
- `title` - Tooltip text.
- `hidden` - Hides the element.
- `draggable` - Makes the element draggable (`true` or `false`).
- `contenteditable` - Allows editing (`true` or `false`).
- `spellcheck` - Enables spell checking (`true` or `false`).

## Conclusion
Understanding HTML attributes is essential for structuring and styling web pages effectively. Keep this guide handy for reference while developing web applications!
