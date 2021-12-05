Links:  [[008 Web development]]

# Front end
---
[[00811 HTML]]
[[00812 CSS]]
[[00813 JavaScript]]

Tip in CSS:
- To make the images flexible, simply add `max-width:100%` and `height:auto`. Image `max-width:100%` and `height:auto` works in IE7, but not in IE8 (yes, another weird IE bug). To fix this, you need to add `width:auto\9` for IE8.
- source: [http://webdesignerwall.com/tutorials/responsive-design-with-css3-media-queries](http://webdesignerwall.com/tutorials/responsive-design-with-css3-media-queries)

```css
img {
    max-width: 100%;
    height: auto;
    width: auto\9; /* ie8 */
}
```

and then any images you add simply using the img tag will be **flexible**

[JSFiddle example here.](https://jsfiddle.net/jaanhaitojahanhai/cnudrxgq/) No JavaScript required. Works in latest versions of Chrome, Firefox and IE (which is all I've tested).