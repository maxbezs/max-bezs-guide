# JavaScript

I would not say that there are any clear rules for writing JS code in our case, but it is extremely important to take performance and loading speed into account.  Mainly to focus on code optimization and readability for other programmers, but here are some recommendations for you:

1. **Plan and organize your code structure before starting:**

```javascript
// Example: Plan the structure of your JavaScript code
// Define modules and functions
function moduleA() {
  // Function implementation
}

function moduleB() {
  // Function implementation
}

// Call the functions
moduleA();
moduleB();
```

2. **Follow coding standards and keep your code neat and readable:**

```javascript
// Example: Follow coding standards and use proper indentation
function calculateSum(a, b) {
    // Proper indentation
    return a + b;
}

// Example: Use meaningful variable and function names
function calculateRectangleArea(length, width) {
    // Function implementation
}
```

3. **Break your code into smaller, reusable modules:**

```javascript
// Example: Encapsulate related functionality into functions or classes
function validateEmail(email) {
    // Validation logic
    return isValid;
}

function sendEmail(email) {
    if (validateEmail(email)) {
        // Send email logic
    } else {
        // Handle invalid email
    }
}
```

4. **Avoid using too many global variables to prevent conflicts:**

```javascript
// Example: Use local variables and IIFE to avoid polluting the global namespace
(function() {
    var localVariable = 'This is a local variable';
    // Code that uses localVariable
})();
```

5. **Optimize your code for better performance by reducing unnecessary operations:**

```javascript
// Example: Optimize DOM manipulations
// Inefficient way
for (var i = 0; i < 1000; i++) {
    document.getElementById('element').innerHTML += 'new content';
}

// Optimized way
var element = document.getElementById('element');
var content = '';
for (var i = 0; i < 1000; i++) {
    content += 'new content';
}
element.innerHTML = content;
```

6. **Handle errors gracefully and display meaningful messages to users:**

```javascript
// Example: Error handling
try {
    // Code that may throw an error
} catch (error) {
    console.error('An error occurred:', error.message);
    // Display user-friendly error message
}
```

7. **Secure your code by validating inputs and using secure APIs:**

```javascript
// Example: Validate user input
function processFormData(formData) {
    if (isValid(formData)) {
        // Process the data
    } else {
        // Handle invalid input
    }
}
```

8. **Test your code thoroughly and use debugging tools to fix issues:**

```javascript
// Example: Use console.log for debugging
function calculateSum(a, b) {
    console.log('Calculating sum:', a, '+', b);
    return a + b;
}

var result = calculateSum(3, 5);
console.log('Result:', result);
```

9. **Use version control for easy collaboration and code management:**

```bash
# Example: Git commands for version control
git clone <repository-url>
git add .
git commit -m "Commit message"
git push origin master
```

10. **Document your code to make it easier for others to understand:**

```javascript
// Example: Use code comments for documentation
// This function calculates the area of a rectangle
function calculateRectangleArea(length, width) {
    return length * width;
}
```

## Service Worker

The service worker is used solely to get the PWA mark, which is an important part for a web application, but for a typical website it is just an additional, auxiliary feature. But still it has to be in every website created by you.

The general structure of the `serviceWorker.js` should look like this:

```js
const staticDevCoffee = "max-bezs"
const assets = [
  "/index.html",
  "/css/index.css",
  "/js/scripts.js",
  "/img/logo.png",
  "/serviceWorker.js",
  "/"  
]

self.addEventListener("install", installEvent => {
  installEvent.waitUntil(
    caches.open(staticDevCoffee).then(cache => {
      cache.addAll(assets)
    })
  )
})

self.addEventListener("fetch", fetchEvent => {
    fetchEvent.respondWith(
      caches.match(fetchEvent.request).then(res => {
        return res || fetch(fetchEvent.request)
      })
    )
})
```

[More](https://web.dev/learn/pwa/service-workers/ "link")

## Manifest:

The manifest is used solely to get the PWA mark, which is an important part for a web application, but for a typical website it is just an additional, auxiliary feature. But still it has to be in every website created by you.

The general structure of the `manifest.json` should look like this:
```json
{
  "short_name": "max_bezs",
  "name": "max_bezs designer developer",
  "start_url": "index.html",
  "background_color": "#000000",
  "theme_color": "#000",
  "lang": "en",
  "display": "standalone",
  "icons": [
    {
        "src": "{link-webp}",
        "sizes": "144x144",
        "type": "image/webp",
        "purpose": "any"
    },
    {
        "src": "{link-png}",
        "sizes": "512x512",
        "type": "image/png",
        "purpose": "maskable"
    }
  ]
}
```
Where `{link-webp}` is the link to the .webp icon of the website or company and `{link-png}` is the link to the .png icon of the website or company. 

[More](https://developer.mozilla.org/en-US/docs/Web/Manifest "link")
