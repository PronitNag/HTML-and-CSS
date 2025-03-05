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
