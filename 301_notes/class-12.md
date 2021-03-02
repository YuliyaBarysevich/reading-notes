# Components/EJS PARTIALS

Partials are useful when we want to reuse the same HTML across multiple views. Partials are as functions, they make large websites easier to maintain, we don't have to change a piece of text in every page it appears in. Instead, we can define that reusable bundle of code in a file andinclude it wherever we need it.

## How does it work?

```html 
<!-- Under the views/partials/ directory create a file callednavbar.ejs which will contain only the HTML for the navigation bar -->

<!-- views/partials/navbar.ejs -->
    <div class="header clearfix">
        <nav>
            <ul class="nav nav-pills pull-right">
                <li role="presentation"><a href="/">Home</a></li>
            </ul>
            <h3 class="text-muted">Node.js Blog</h3>
        </nav>
    </div>

<!-- now we can use them in our index.ejs and other files -->
``` 

```html  

<!-- That's the only we need to do to include the navbar partial -->

<!DOCTYPE html>
    <html>
    <head>
        <meta charset="utf-8">
        <title>document</title>
    </head>
    <body>
        <div class="container">
            <%- include('partials/navbar') %>
        </div>
``` 