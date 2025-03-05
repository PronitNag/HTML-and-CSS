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


## In the <form> element of your code, the following attributes are used:

# action="results.html"

Specifies the URL (results.html) where the form data will be sent when the user submits the form.<br />
method="GET"<br />

## Defines the HTTP method used to send the form data.<br />
GET means the form data will be appended to the URL as query parameters.<br />
Inside the form, the <input> elements also have attributes that contribute to how data is handled:<br />

type="text" (for Name) and type="password" (for Password)<br />

## Defines the type of input field.<br />
text is for normal text input, and password hides the characters entered.<br />
name="Name" and name="Password"<br />

# The name attribute is crucial as it determines how the data will be sent in the URL.<br />
Example: If a user enters "John" as the name and "abc123" as the password, the URL will be:
<br />
results.html?Name=John&Password=abc123<br />
id="Name" and id="Password"<br />

# The id attribute uniquely identifies the input fields.<br />
It is linked to the <label> using for="Name" and for="Password", ensuring that clicking on the label focuses the associated input field.<br />
value="Pronit" (only in the Name input field)<br />

# Pre-fills the text input field with "Pronit" as the default value.<br />
type="submit" in <button><br />

# This makes the button submit the form when clicked.<br />
How Are They Linked?<br />
The name attributes link the input fields to the form submission process.<br />
The id attributes link the input fields to their respective <label> elements.<br />
The action and method attributes define how and where the form data is sent.<br />
The type="submit" button sends the data when clicked.<br />
