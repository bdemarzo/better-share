# Better Share 

 Web Share API Navigator.share() native (Android and IOS) share dialog with fallback modal for unsupported browsers.

Forked it from Chris Yee's Good Share (Thanks!) and made the following changes:

- Rewrote in jquery almost all of the code as it had too many issues/inefficency to use on production
- Configurable now as you can set buttons, classes etc
- Made it far more lightweight as it won't do anything now until the button is clicked. No overlay, no modal etc is created
- It uses Open Graph if no inline url/title/description provided. If provided, overrides og tags
- Added font awesome 4.7 for button icons. It is not required though. You can add your own buttons
- Simplified to just one js and one css files. 
- Comes with facebook, twitter, whatsapp, telegram by default 

Better Share is a social share button library with [Web Share API](https://css-tricks.com/how-to-use-the-web-share-api/) integration.

Using the Web Share API Navigator.share(), it allows the user to share content using the native share dialog, especially mobile on [supported browsers](https://caniuse.com/#feat=web-share). 

For unsupported browsers, a fallback modal window with sharing buttons are used.

[Noticed some websites already use this.](https://www.miragenews.com/ghost-flight-pilots-fall-asleep-with-140-aboard-f16s-scrambled-video/) | [Download](https://github.com/selay/better-share/archive/master.zip)

You can check here in use: https://www.miragenews.com/ghost-flight-pilots-fall-asleep-with-140-aboard-f16s-scrambled-video/

## Features
- Web Share API for native share
- Fallback modal for [unsupported browsers](https://caniuse.com/#feat=web-share)
- Multiple share buttons
- Uses CSS animations
- Fallback modal closes when the site overlay is selected
- Supports [Open Graph Metadata](https://ogp.me/)

## Requirements
- jQuery
- Your website must be served over [HTTPS](https://www.cloudflare.com/learning/ssl/what-is-https/)
- Sharing can only be triggered by a user action (click or touch)

## Getting Started

- Include the CSS and JS files 

```html
<link rel="stylesheet" href="css/better-share.css">
```

```html
<script src="js/better-share.js"></script>
```

- Add the `.better-share` CSS class to you share buttons along with the [data attribute options](#options).

- Eg. It will use og meta tags or just current page url

```html
<button class="better-share">
    <span>Share </span>
    <i class="fa fa-share-alt fa-lg" aria-hidden="true"></i>
 </button>
```

- Eg. You can specify using data-share-title etc to override specific value.

```html
<button class="better-share" data-share-title="Hello World" data-share-url="https://nasa.gov">
    <span>Share </span>
    <i class="fa fa-share-alt fa-lg" aria-hidden="true"></i>
</button>
```

## Options

### data-share-title
The title to be shared.

``data-share-title="Hello World"``

### data-share-text
The text to be shared.

``data-share-text="Lorem ipsum dolor sit amet"``

### data-share-url
The URL to be shared.

``data-share-url="https://nasa.gov"``


