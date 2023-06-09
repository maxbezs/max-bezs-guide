
# Guide for creating a good website
list of images but not background big one
## Result:

![picture alt](https://raw.githubusercontent.com/maxbezs/max_bezs-website-images/main/matrics.webp "all 4 Google matrics 100")

__The main goal is to create understandable, flexible and fast website/ web-app for clients to provide high value service and increase their market competitiveness.__

To reach the goal, I created a guide on how and what to write in order to increase the speed and efficiency of both work and product.

## Guide Structure:
* [Code](#code)
* [Files](#js)
* [JS](JS.md)
* [CSS](CSS.md)
* [HTML](HTML.md)
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



<a name="body"></a>
<a name="js"></a>
