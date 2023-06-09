# Body

## Semantic elements

<a name="navigation"></a>

### Navigation

The `<nav>` element represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents. Common examples of navigation sections are menus, tables of contents, and indexes.

The general structure of the `<nav>` should look like this:
```html
   <nav aria-label='primary menu'>
      <ul>
         <li>
            <a aria-label='home page' href="/">
               Home
            </a>
         </li>
         <li>
            <a aria-label='blog page' href="/blog">
               Blog
            </a>
         </li>
         <li>
            <a aria-label='service page' href="/services">
               Services
            </a>
         </li>
      </ul>
   </nav>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/nav "link")

<a name="header"></a>

### Header

The `<header>` element represents introductory content, typically a group of introductory or navigational aids. You can also use it as beginning of element but try to create only one `<header>` component that contains Logo, Navigation, Button and is on top of each webpage.

The general structure of the `<header>` should look like this:
```html
   <header>
      <a href="/">
         <img alt=" logo" src="logo.png"/>
      </a>
      <nav>
         ...
      </nav>
      <button>Action</button>
   </header>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header "link")

<a name="form"></a>

### Form

The `<form>` element represents a document section containing interactive controls for submitting information. 

The general structure of the `<form>` should look like this:
```html
   <form action="" method="get" class="form-example">
      <label for="email">
         Email: 
      </label>
      <input type="email" name="email" id="email" required>
      <button type="submit">
         Subscribe
      </button>
   </form>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form "link")

<a name="footer"></a>

### Footer

The `<footer>` element represents content at the bottom of a webpage. It is typically used to provide information about the website or to contain links to related content. You should try to create only one `<footer>` component that contains relevant information and is located at the bottom of each webpage. This could include Copyright Notice, Privacy Policy Link, Sitemap, Logo, Contact Information, Social Media Icons, Form.

The general structure of the `footer` should look like this:
```html
   <footer>
      <div>
         <h3>Pages</h3>
         <a aria-label='home page' href="/">
            Home
         </a>
         <a aria-label='blog page' href="/blog">
            Blog
         </a>
         <a aria-label='service page' href="/services">
            Services
         </a>
      </div>
      <div>
         <h3>Services/Products</h3>
         <a aria-label='service 1' href="/services/service-1">
            Service 1
         </a>
         <a aria-label='service 2' href="/services/service-2">
            Service 2
         </a>
         <a aria-label='service 3' href="/services/service-3">
            Service 3
         </a>
      </div>
      <div>
         <h3>Social Media</h3>
         ...
      </div>
      <form>
         ...
      </form>
      <div>
         <img alt="logo" src="logo.png"/>
         <p>© Copyright 2023. All rights reserved.</p>
      </div>
   </footer>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer "link")

<a name="main"></a>

### Main

The `<main>` HTML element represents the dominant content of the `<body>` of a document. The main content area consists the central functionality of an application/webpage. No more than one `<main>` element that doesn't have the `hidden` attribute specified.

The general structure of the `body` should look like this:
```html
   <body>
      <header>
         ...
      </header>
      <main>
         ...
      </main>
      <footer>
         ...
      </footer>
   </body>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main "link")
