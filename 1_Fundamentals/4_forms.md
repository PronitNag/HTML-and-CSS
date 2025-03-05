# HTML Forms Guide

## Introduction
Forms in HTML allow users to input and submit data to a web server. They are essential for user interactions such as login, search, feedback, and data collection.

## Basic Syntax
```html
<form action="/submit" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    <input type="submit" value="Submit">
</form>
```

## Form Attributes
- `action`: Specifies the URL where form data is sent.
- `method`: Defines the HTTP method (`GET` or `POST`).
- `enctype`: Used for file uploads (`multipart/form-data`).
- `target`: Specifies where to display the response (`_self`, `_blank`, etc.).
- `autocomplete`: Enables or disables autocomplete.
- `novalidate`: Disables HTML5 validation.

## Input Elements

### Text Input
```html
<input type="text" name="username" placeholder="Enter your name">
```

### Password Input
```html
<input type="password" name="password" required>
```

### Email Input
```html
<input type="email" name="email" required>
```

### Number Input
```html
<input type="number" name="age" min="1" max="100">
```

### Radio Buttons
```html
<input type="radio" name="gender" value="male"> Male
<input type="radio" name="gender" value="female"> Female
```

### Checkboxes
```html
<input type="checkbox" name="subscribe" value="yes"> Subscribe to newsletter
```

### Dropdown (Select)
```html
<select name="country">
    <option value="us">USA</option>
    <option value="uk">UK</option>
    <option value="in">India</option>
</select>
```

### Textarea (Multi-line Input)
```html
<textarea name="message" rows="4" cols="30"></textarea>
```

### File Upload
```html
<input type="file" name="file">
```

## Buttons
```html
<input type="submit" value="Submit">
<input type="reset" value="Reset">
<button type="button" onclick="alert('Clicked!')">Click Me</button>
```

## Form Validation
```html
<input type="text" name="username" required pattern="[A-Za-z]{3,}">
```
- `required`: Makes input mandatory.
- `pattern`: Defines a regex pattern.
- `min` and `max`: Limits numbers.
- `maxlength`: Sets character limit.

## Advanced Features

### Placeholder and Autofocus
```html
<input type="text" placeholder="Enter name" autofocus>
```

### Disabled and Readonly
```html
<input type="text" value="Disabled" disabled>
<input type="text" value="Read only" readonly>
```

### Hidden Input
```html
<input type="hidden" name="token" value="123456">
```

### Fieldset and Legend
```html
<fieldset>
    <legend>Personal Information</legend>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
</fieldset>
```

## Conclusion
HTML forms are fundamental for user interactions. They support various input types, validation techniques, and customization options to create interactive web applications.

---

_This guide provides an overview of HTML forms with examples. For more details, refer to [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)._
