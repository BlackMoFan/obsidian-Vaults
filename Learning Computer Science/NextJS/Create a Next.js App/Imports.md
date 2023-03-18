Link
```js
import Link from 'next/link';
```

- **Note:** Before Next.js 12.2, it was required that the `Link` component wrapped an `<a>` tag, but [this is not required in versions 12.2 and above](https://nextjs.org/blog/next-12-2#:~:text=next/link%20no%20longer%20requires%20manually%20adding%20%3Ca%3E%20as%20a%20child.%20You%20can%20now%20opt%20into%20this%20behavior%20in%20a%20backward%2Dcompatible%20way.)
- The [`Link`](https://nextjs.org/docs/api-reference/next/link) component enables **client-side navigation** between two pages in the same Next.js app.
- Client-side navigation means that the page transition happens _using JavaScript_, which is faster than the default navigation done by the browser.
- Here’s a simple way you can verify it:
	-   Use the browser’s developer tools to change the `background` CSS property of `<html>` to `yellow`.
	-   Click on the links to go back and forth between the two pages.
	-   You’ll see that the yellow background persists between page transitions.
- This shows that the browser does _not_ load the full page and client-side navigation is working.
- If you’ve used `<a href="…">` instead of `<Link href="…">` and did this, the background color will be cleared on link clicks because the browser does a full refresh.

Head
```js
import Head from 'next/head';
```

Image
```js
import Image from 'next/image';
```

- [`next/image`](https://nextjs.org/docs/api-reference/next/image) is an extension of the HTML `<img>` element, evolved for the modern web.
- Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like [WebP](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#webp) when the browser supports it. This avoids shipping large images to devices with a smaller viewport. It also allows Next.js to automatically adopt future image formats and serve them to browsers that support those formats.
- Automatic Image Optimization works with any image source. Even if the image is hosted by an external data source, like a CMS, it can still be optimized.