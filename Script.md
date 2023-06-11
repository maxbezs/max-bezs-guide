# Script

In HTML, the `<script>` tag is used to define client-side JavaScript code. It is used to embed or reference JavaScript code within an HTML document. 

Here's an example of how the `<script>` tag is typically used in an HTML file:

```html
<!DOCTYPE html>
<html>
<head>
  ...
</head>
<body>
  ...
  <script>
    // JavaScript code goes here
    ...
  </script>
</body>
</html>
```

Alternatively, you can also use the `src` attribute of the `<script>` tag to reference an external JavaScript file. For example:

```html
<script src="script.js"></script>
```

It's important to note that placing the `<script>` tag in the `<head>` section of the HTML file will cause the script to be executed before the HTML content is rendered => errors will occur. 
