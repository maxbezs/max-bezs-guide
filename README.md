
# Guide for creating a good website
list of images but not background big one
## Result:

![picture alt](https://raw.githubusercontent.com/maxbezs/max_bezs-website-images/main/matrics.webp "all 4 Google matrics 100")

__The main goal is to create understandable, flexible and fast website/ web-app for clients to provide high value service and increase their market competitiveness.__

To reach the goal, I created a guide on how and what to write in order to increase the speed and efficiency of both work and product.

## Guide Structure:

* [Files](#js)
* [JS](#js)
* [CSS](#css)
* [HTML](#html)
    * [Head](#head)
        * [Title](#title)
        * [Link tags](#link-tags)
        * [Meta tags](#meta-tags)
    * [Body](#body)
        * [Header](#header)
        * [Footer](#footer)
        * [a](#a)
        * [nav](#nav) 
        * [img](#img)
        * [button](#button)
        * [div](#div)
        * [video](#video)
        * [p](#p)
        * [hr](#hr)
        * [Headers](#headers)
            * [h1](#h1)
            * [h2](#h2)
            * [h3](#h3)
            * [h4](#h4)
            * [h5](#h5)
        * [Script](#script)

<a name="manifest"></a>

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

## Files Structure and names:

```bash
├── css
│   └── **/*.css
├── js
│   └── **/*.js
├── serviceWorker.js
├── index.html
└── manifest.json
```

<a name="head"></a>

## Head:

Every page has to have this code inside `<head>`:
* [Title](#title)
* [Link tags](#link-tags)
* [Meta tags](#meta-tags)

Final code for `<head>` loojs like this:

```html
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="{link}">
    <meta charset="utf-8">
    <meta name="description" content="max_bezs Developing website">
    <meta name="author" content="max_bezs">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="theme-color" content="#000000">
    <meta http-equiv="Cache-control" content="public">
    <link rel="stylesheet" href="{link}">
    <link rel="apple-touch-icon" href="{link}">
    <link rel="icon" type="image/x-icon" href="{link}">
    <link rel="manifest" href="manifest.json">
    <title>About max_bezs code and design profile</title>
```

Link to preconnect fonts has to be at the top for better performance.

<a name="title"></a>
## Title:

```html
    <title></title>
```

## Link tags: 

<a name="link-tags"></a>

### Stylesheet

```html
    <link rel="stylesheet" href="css/index.css">
```
[More](https://www.dofactory.com/html/rel/stylesheet "link")

### Apple Touch Icon

```html
    <link rel="apple-touch-icon" href="{link}">
```
Where {link} is the link to the image

[More](https://webhint.io/docs/user-guide/hints/hint-apple-touch-icons/ "link")

### Icon

```html
    <link rel="icon" type="image/x-icon" href="{link}">
```
Where {link} is the link to the image

[More](https://www.w3schools.com/html/html_favicon.asp "link")

### Stylesheet

```html
    <link rel="stylesheet" href="{link}">
```
Where {link} is the link to the CSS file

[More](https://www.w3schools.com/css/css_howto.asps "link")

### Manifest

```html
    <link rel="manifest" href="manifest.json">
```

Manifest has to be in root folder with all html files. More about Manifest and how to write the best website manifest is [HERE](#manifest)

### Preconnect Fonts

```html
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="{link}">
```
Where {link} is the Google link to the font

We prefer to [Google Fonts](https://fonts.google.com/ "Google Fonts"), but when a client wants to have a personal font not available on the web, we use Github and CSS to host and provide the font files. More info about it in [CSS part](#css).

[More](https://web.dev/font-best-practices/ "link")

## Meta tags: 

<a name="meta-tags"></a>

Every website must include `<meta>` tags

### Charset

```html
    <meta charset="utf-8">
````
[More](https://www.w3schools.com/html/html_charset.asp "meta tag link")

  

### Author

```html
    <meta name="author" content="max_bezs">
````
[More](https://www.w3schools.com/tags/att_meta_name.asp "meta tag link")

  

### Viewport

```html
    <meta name="viewport" content="width=device-width, initial-scale=1">
```
[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Viewport_meta_tag "meta tag link")

  

### Theme color

```html
    <meta name="theme-color" content="#000000">
```
[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name/theme-color "meta tag link")

  

### Cache control

```html
    <meta http-equiv="Cache-control" content="public">
```
[More](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control "meta tag link")

  

### Description

```html
    <meta name="description" content="max_bezs Developing website">
```
[More](https://developer.mozilla.org/en-US/docs/Web/HTML/Viewport_meta_tag "meta tag link") , [More (Google)](https://developers.google.com/search/docs/crawling-indexing/special-tags "meta tag link")

  

### Final code

```html
    <meta charset="utf-8">
    <meta name="author" content="max_bezs">
    <meta name="theme-color" content="#000000">
    <meta http-equiv="Cache-control" content="public">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="max_bezs Developing website service">
```

These `<meta>` should be on every page's `<head></head>`. After that, the Lead Developer will approve or correct them at the end and the page will be ready for publication.🥳

<a name="css"></a>

<a name="body"></a>
<a name="html"></a>
<a name="js"></a>
