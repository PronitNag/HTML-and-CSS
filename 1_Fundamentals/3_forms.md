# This is the form that i created 

-- index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form</title>
</head>
<body>
    <form action="results.html" method="GET">
        <div>
            <label for="Name">Name</label>
            <input type="text"  name="Name" id="Name" value="Pronit">
        </div>

        <div>
            <label for="Password">Password</label>
            <input type="password" name="Password" id="Password">
        </div>

        <button type="submit">Submit</button>
    </form>
</body>
</html>
```

## add this in the same directory to test the form

-add it

-- results.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Results</title>
</head>
<body>
    <div id="results"></div>
    <a href="/">Back to Form</a>

    <script>
        const resultsList=document.getElementById('results');
        new URLSearchParams(window.location.search).forEach((value,name)=>{
            resultsList.append(`${name}:${value}`);
            resultsList.append(document.createElement('br'));
        })
    </script>
    
</body>
</html>
```

# Explanation of Form Attributes in HTML

## 1. `<form action="results.html" method="GET">`
- **`action="results.html"`**: Specifies that when the form is submitted, the data will be sent to `results.html`.
- **`method="GET"`**: Specifies that the form data will be sent using the **GET** method, meaning the data will be appended to the URL as query parameters.

---

## 2. `<label for="Name">Name</label>`
- The `<label>` is used to describe an input field.
- **`for="Name"`**: Links this label to the input field with `id="Name"`, so clicking on the label focuses the input.

---

## 3. `<input type="text" name="Name" id="Name" value="Pronit">`
- **`type="text"`**: Defines a single-line text input field.
- **`name="Name"`**: This is the key for form submission; the entered value will be sent as `Name=UserInput`.
- **`id="Name"`**: Uniquely identifies this input field and links it with `<label for="Name">`.
- **`value="Pronit"`**: Pre-fills the input field with the default value `"Pronit"`.

---

## 4. `<label for="Password">Password</label>`
- Similar to the name label, this links to the password input field with `id="Password"`.

---

## 5. `<input type="password" name="Password" id="Password">`
- **`type="password"`**: Defines a password input field where typed characters are hidden.
- **`name="Password"`**: The value entered will be sent as `Password=UserInput` in the form submission.
- **`id="Password"`**: Uniquely identifies this input field and links it with `<label for="Password">`.

---

## 6. `<button type="submit">Submit</button>`
- **`type="submit"`**: Defines a button that submits the form when clicked.

---

## 7. How Are These Attributes Linked?
- The **`name` attributes** are used when submitting the form, ensuring the data is sent in key-value pairs (`Name=Pronit` and `Password=1234`).
- The **`id` attributes** link input fields with their corresponding `<label>` elements.
- The **`action` and `method` attributes** define where and how the form data is sent.
- The **submit button** triggers the form submission.

---

### Example Form Submission (GET Method)
If the user enters:
- Name: `John`
- Password: `mypassword`

The browser will send the data like this:

