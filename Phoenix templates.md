# [[Phoenix]] Templates


## comments

```html
<body>
  <div class="container">
    
    <!-- Remove the whole <header>-part -->
    <!-- And add this instead: -->
    <h1>Hello world!</h1>

    <!-- Keep the rest as it is: -->
    <p class="alert alert-info" role="alert"><%= get_flash(@conn, :info) %></p>
    <p class="alert alert-danger" role="alert"><%= get_flash(@conn, :error) %></p>

    <!-- ... -->
    
  </div>
</body>
```

