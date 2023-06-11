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
