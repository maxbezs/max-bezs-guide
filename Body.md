# Body

The body of your webpage can contain several semantic elements which add meaning to the structure and content of your webpage. These elements are used by search engines to better understand the content on your webpage and provide a better user experience. This guide will tell you which elements to use in the code.  Those elements that are not listed are not recommended to be used to create web pages.

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

## HTML elements

### Anchor

The `<a>` HTML element, or anchor element, creates a hyperlink to other web pages, files, locations within the same page, email addresses, or any other URL.

The general structure of the `<a>` should look like this:

```html
   <a href="https://example.com" aria-label="Visit Example.com">Visit Example.com</a>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a "link"),
[More](https://dequeuniversity.com/rules/axe/4.6/link-name "link"),
[More](https://developers.google.com/search/docs/crawling-indexing/links-crawlable "link")

<a name="br"></a>

### Line Break

The `<br>` HTML element produces a line break in text (carriage-return). It is useful for writing a poem or an address, where the division of lines is significant.

The general use of the `<br>` should look like this:
```html
   <p>This is a paragraph<br>with a line break.</p>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/br "link")

<a name="button"></a>

### Button

The `<button>` HTML element represents a clickable button, used to submit forms or anywhere in a document that needs simple, standard button functionality. Do not use buttons as navigational elements. Instead, use `<a>`. If your buttons are not for submitting form data to a server, be sure to set their `type` attribute to `"button"`. 

The general structure of the `<button>` should look like this:
```html
   <button type="button" tabindex="0" onclick="myFunction()">Click Me!</button>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button "link")

<a name="div"></a>

### Division

The `<div>` HTML element is the generic container for flow content. It has no effect on the content or layout until styled using CSS. Parent `<div>` should manage positioning of child elements inside it. Try to minimize amount of divs inside divs:

When it comes to nesting HTML code using `<div>` elements, there are a few do's and don'ts to keep in mind to ensure proper structure and maintainability of your code. Here are some examples:

Do's:
1. Do use `<div>` elements to create logical sections or containers for your content.
```html
   <div>
      <h1>Main Heading</h1>
      <p>This is some text.</p>
   </div>
```

2. Do nest `<div>` elements to create hierarchical structures and sub-sections.
```html
   <div>
      <h2>Section Heading</h2>
      <div>
         <p>This is a sub-section.</p>
      </div>
   </div>
```

3. Do use appropriate indentation to enhance code readability.
```html
   <div>
      <h1>Main Heading</h1>
      <div>
         <h2>Section Heading</h2>
         <div>
            <p>This is a sub-section.</p>
         </div>
      </div>
   </div>
```

Don'ts:

1. Don't use `<div>` elements excessively for simple or semantically meaningful elements. Instead, use appropriate HTML elements.
```html
   <!-- Avoid -->
   <div>
      <div>
         <div>
            <p>Some text</p>
         </div>
      </div>
   </div>

   <!-- Prefer -->
   <section>
      <article>
         <p>Some text</p>
      </article>
   </section>
```

2. Don't rely solely on `<div>` elements for layout purposes. Consider using CSS and appropriate HTML elements like `<header>`, `<nav>`, `<footer>`, etc.

```html
   <!-- Avoid -->
   <div id="header">...</div>
   <div id="nav">...</div>
   <div id="content">...</div>
   <div id="footer">...</div>

   <!-- Prefer -->
   <header>...</header>
   <nav>...</nav>
   <main>...</main>
   <footer>...</footer>
```

3. Don't nest `<div>` elements too deeply without a valid reason. Excessive nesting can make your code harder to read and maintain.

```html
   <!-- Avoid -->
   <div>
      <div>
         <div>
            <div>
            <p>Some text</p>
            </div>
         </div>
      </div>
   </div>

   <!-- Prefer -->
   <div>
      <div>
         <p>Some text</p>
      </div>
   </div>
```

Remember, the goal is to create clean, maintainable, and semantically meaningful code. Strive for a balance between structure and readability when nesting `<div>` elements or any other HTML elements.

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div "link")

<a name="hr"></a>

### Thematic Break

The `<hr>` HTML element represents a thematic break between paragraph-level elements. It is typically rendered as a horizontal rule. Use it as a decorative horizontal and vertical separator and don't use div to imitate the `<hr/>` properties.

The general use of the `<hr>` should look like this:

```html
   <p>This is the end of a paragraph.</p>
   <hr>
   <p>This is the start of a new paragraph.</p>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/hr "link")

<a name="img"></a>

### Image

The `<img>` HTML element embeds an image into the document. It is a replaced element. Avoid using images as background for text: Using images as backgrounds for text can make the text inaccessible to screen readers. Instead, use CSS techniques to style text elements while keeping them accessible and searchable.

The general structure of the `<img>` should look like this:
```html
   <img src="image.jpg" alt="Description of image">
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img "link"), 
[More](https://web.dev/learn/design/picture-element/ "link"), 

<a name="input"></a>

### Input

The `<input>` HTML element is used to create interactive controls for web-based forms in order to accept data from the user.

The general structure of the `<input>` should look like this:
```html
   <label for="name">Name:</label>
   <input type="text" id="name" name="name">
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input "link")

<a name="label"></a>

### Label

The `<label>` HTML element represents a caption for an item in a user interface. Use `<label>` only for input.
The general structure of the `<label>` should look like this:
```html
   <label for="name">Name:</label>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label "link")

<a name="p"></a>

### Paragraph

The `<p>` HTML element represents a paragraph.

The general structure of the `<p>` should look like this:

```html
   <p>This is a paragraph.</p>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/p "link")

<a name="table"></a>

### Table

The `<table>` HTML element represents tabular data — that is, information presented in a two-dimensional table comprised of rows and columns of cells containing data. Do not use `<table>` element to create webpage instead use `<div>` with `"grid"` or `"flex"` display style.

The general structure of the `<table>` should look like this:
```html
   <table>
      <tr>
         <th>Header 1</th>
         <th>Header 2</th>
      </tr>
      <tr>
         <td>Data 1</td>
         <td>Data 2</td>
      </tr>
   </table>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table "link")

<a name="ul-ol"></a>

### Unordered List and Ordered List

The `<ul>` HTML element represents an unordered list of items, typically rendered as a bulleted list. The `<ol>` HTML element represents an ordered list of items — typically rendered as a numbered list. You may use `<ul>` inside `<nav>` to structure the links and `<ol>` to show user navigation path for subpages

The general structure of the `<ul>` and `<ol>` should look like this:
```html
   <nav>
      <ul>
         <li><a href="/">Home</a></li>
         <li><a href="/about">About</a></li>
         <li>
            <a href="/products">Products</a>
            <ol>
            <li><a href="/products/category1">Category 1</a></li>
            <li><a href="/products/category2">Category 2</a></li>
            <li><a href="/products/category3">Category 3</a></li>
            </ol>
         </li>
         <li><a href="/contact">Contact</a></li>
      </ul>
   </nav>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul "link")
[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol "link")

<a name="video"></a>

### Video

The `<video>` element in HTML is used to embed a media player into a web page for playing videos. It provides a standardized way to display videos on different platforms and browsers. The `<video>` element supports various attributes and features that allow you to control the playback, appearance, and behavior of the video.

Here is an overview of some important attributes and use cases for the `<video>` element:

1. **src**: This attribute specifies the URL of the video file to be played. It can be a relative or absolute URL.

2. **controls**: When the `controls` attribute is present, it adds default playback controls to the video player, such as play/pause, volume, and progress bar.

3. **autoplay**: When the `autoplay` attribute is present, the video starts playing automatically as soon as the page loads.

4. **loop**: The `loop` attribute enables continuous playback of the video. After reaching the end, it restarts from the beginning.

5. **poster**: The `poster` attribute allows you to specify an image that is displayed as a placeholder before the video starts playing. It can be used to provide a preview or thumbnail image.

6. **width** and **height**: These attributes set the width and height of the video player in pixels. You can specify them directly or use CSS to control the dimensions.

7. **muted**: The `muted` attribute, when present, mutes the audio of the video. This is commonly used for videos that autoplay to avoid sudden sound playback.

8. **preload**: The `preload` attribute determines whether the video should be preloaded when the page loads. It can have three values: `auto`, `metadata`, and `none`. `auto` indicates that the browser should preload the video, `metadata` means only the metadata should be loaded, and `none` means the video should not be preloaded.

9. **source**: The `<source>` element is used as a child of the `<video>` element to specify alternative video sources. This is useful when you want to provide different video formats (e.g., MP4, WebM) to ensure compatibility across different browsers.

10. **track**: The `<track>` element is used to add captions, subtitles, or other textual data to the video. It can specify the URL of a text file and the kind of text data it represents.

The general structure of the `<video>` should look like this:
```html
   <video controls>
      <source src="movie.webm" type="video/webm">
      <source src="movie.mp4" type="video/mp4">
      Your browser does not support the video tag.
   </video>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video "link")

## Heading

<a name="h1"></a>

### H1

The `<h1>` to `<h6>` HTML elements represent six levels of section headings. `<h1>` is the highest section level and `<h6>` is the lowest. Only one `<h1>` for each page.

The general structure of the `<h1>` should look like this:
```html
   <h1>This is a heading 1</h1>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h1 "link")

<a name="h2"></a>

### H2

The `<h2>` to `<h6>` HTML elements represent six levels of section headings. `<h1>` is the highest section level and `<h6>` is the lowest.

The general structure of the `<h2>` should look like this:
```html
   <h2>This is a heading 2</h2>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h2 "link")

<a name="h3"></a>

### H3

The `<h3>` to `<h6>` HTML elements represent six levels of section headings. `<h1>` is the highest section level and `<h6>` is the lowest.

The general structure of the `<h3>` should look like this:
```html
   <h3>This is a heading 3</h3>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h3 "link")

<a name="h4"></a>

### H4

The `<h4>` to `<h6>` HTML elements represent six levels of section headings. `<h1>` is the highest section level and `<h6>` is the lowest.

The general structure of the `<h4>` should look like this:
```html
   <h4>This is a heading 4</h4>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h4 "link")

<a name="h5"></a>

### H5

The `<h5>` to `<h6>` HTML elements represent six levels of section headings. `<h1>` is the highest section level and `<h6>` is the lowest.

The general structure of the `<h5>` should look like this:
```html
   <h5>This is a heading 5</h5>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h5 "link")

<a name="h6"></a>

### H6

The `<h6>` HTML element represents the sixth level of section headings. `<h1>` is the highest section level and `<h6>` is the lowest.

The general structure of the `<h6>` should look like this:
```html
   <h6>This is a heading 6</h6>
```

[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/h6 "link")
