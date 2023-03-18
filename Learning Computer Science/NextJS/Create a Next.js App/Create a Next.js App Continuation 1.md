### Assets, Metadata, and CSS
- Next.js has built-in support for [CSS](https://nextjs.org/docs/basic-features/built-in-css-support) and [Sass](https://nextjs.org/docs/basic-features/built-in-css-support#sass-support).
- To add a stylesheet to your application, import the CSS file within `pages/_app.js`.
- For example, consider the stylesheet named `styles.css`.
- You import the styles.css file inside the pages/_app.js file
	```js
	import '../styles.css'
	```
- These styles (`styles.css`) will apply to all pages and components in your application. Due to the global nature of stylesheets, and to avoid conflicts, you may **only import them inside [`pages/_app.js`](https://nextjs.org/docs/advanced-features/custom-app)**.
- In development, expressing stylesheets this way allows your styles to be hot reloaded as you edit them—meaning you can keep application state.
- In production, all CSS files will be automatically concatenated into a single minified `.css` file.

In this lesson, you’ll learn:
-   How to add [static files](https://nextjs.org/docs/basic-features/static-file-serving) (images, etc) to Next.js.
-   How to customize what goes inside the `<head>` for each page.
-   How to create a reusable React component which is styled using [CSS Modules](https://nextjs.org/docs/basic-features/built-in-css-support#adding-component-level-css).
-   How to [add global CSS](https://nextjs.org/docs/basic-features/built-in-css-support#adding-a-global-stylesheet) in [`pages/_app.js`](https://nextjs.org/docs/advanced-features/custom-app).
-   Some useful tips for styling in Next.js.

#### Assets
- Next.js can serve **static assets**, like images, under **the top-level [`public` directory](https://nextjs.org/docs/basic-features/static-file-serving)**. Files inside `public` can be referenced from the root of the application similar to [`pages`](https://nextjs.org/docs/basic-features/pages).
- The `public` directory is also useful for `robots.txt`, Google Site Verification, and any other static assets. Check out the documentation for [Static File Serving](https://nextjs.org/docs/basic-features/static-file-serving) to learn more.
###### Unoptimized Image
- With regular HTML, you would add your profile picture as follows:
```html
<img src="/images/profile.jpg" alt="Your Name" />
```
However, this means you have to manually handle:
-   Ensuring your image is responsive on different screen sizes
-   Optimizing your images with a third-party tool or library
-   Only loading images when they enter the viewport
And more. Instead, Next.js provides an `Image` component out of the box to handle this for you.

##### Image Component and Image Optimization

- [`next/image`](https://nextjs.org/docs/api-reference/next/image) is an extension of the HTML `<img>` element, evolved for the modern web.
- Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like [WebP](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#webp) when the browser supports it. This avoids shipping large images to devices with a smaller viewport. It also allows Next.js to automatically adopt future image formats and serve them to browsers that support those formats.
- Automatic Image Optimization works with any image source. Even if the image is hosted by an external data source, like a CMS, it can still be optimized.
- Images are lazy loaded by default. That means your page speed isn't penalized for images outside the viewport. Images load as they are scrolled into viewport.
- Images are always rendered in such a way as to avoid [Cumulative Layout Shift](https://web.dev/cls/), a [Core Web Vital](https://web.dev/vitals/#core-web-vitals) that Google is going to [use in search ranking](https://webmasters.googleblog.com/2020/05/evaluating-page-experience.html).
- To learn more about Automatic Image Optimization, check out the [documentation](https://nextjs.org/docs/basic-features/image-optimization).
- To learn more about the `Image` component, check out the [API reference for `next/image`](https://nextjs.org/docs/api-reference/next/image).

#### Metadata
- What if we wanted to modify the metadata of the page, such as the `<title>` HTML tag?
- `<title>` is part of the `<head>` HTML tag.
- You can import the `Head` component from the [`next/head`](https://nextjs.org/docs/api-reference/next/head) module.
	```js
	import Head from 'next/head';
	```
- then add the code below inside the return ()
	```jsx
	<Head>
		<title>First Post</title>
	</Head>
	```
- To learn more about the `Head` component, check out the [API reference for `next/head`](https://nextjs.org/docs/api-reference/next/head).
- If you want to customize the `<html>` tag, for example to add the `lang` attribute, you can do so by creating a `pages/_document.js` file. Learn more in the [custom `Document` documentation](https://nextjs.org/docs/advanced-features/custom-document).

##### Third-Part JavaScript
- **Third-party JavaScript** refers to any scripts that are added from a third-party source. Usually, third-party scripts are included in order to introduce newer functionality into a site that does not need to be written from scratch, such as analytics, ads, and customer support widgets.
**Inside the Head component**
- In addition to metadata, scripts that need to load and execute as soon as possible are usually added within the `<head>` of a page. Using a regular HTML `<script>` element, an external script would be added as follows:
	```jsx
	<Head>
	  <title>First Post</title>
	  <script src="https://connect.facebook.net/en_US/sdk.js" />
	</Head>
	```
**Using Script Component of Next.js**
- [`next/script`](https://nextjs.org/docs/api-reference/next/script) is an extension of the HTML `<script>` element and optimizes when additional scripts are fetched and executed.
	```jsx
	import Script from 'next/script';
	```
	
	```jsx
	export default function FirstPost() {
	  return (
	    <>
	      <Head>
	        <title>First Post</title>
	      </Head>
	      <Script
	        src="https://connect.facebook.net/en_US/sdk.js"
	        strategy="lazyOnload"
	        onLoad={() =>
	          console.log(`script loaded correctly, window.FB has been populated`)
	        }
	      />
	      <h1>First Post</h1>
	      <h2>
	        <Link href="/">← Back to home</Link>
	      </h2>
	    </>
	  );
	}
	```

Notice that a few additional properties have been defined in the Script component:

-   `strategy` controls when the third-party script should load. A value of `lazyOnload` tells Next.js to load this particular script lazily during browser idle time
-   `onLoad` is used to run any JavaScript code immediately after the script has finished loading. In this example, we log a message to the console that mentions that the script has loaded correctly

#### CSS
- There are two main classification of CSS in next.js:
	- CSS Modules
	- Global Styles

**CSS Modules**
- [CSS modules](https://nextjs.org/docs/basic-features/built-in-css-support) allow you to locally scope CSS at the component-level by automatically creating unique class names. This allows you to use the same CSS class name in different files without worrying about class name collisions.
- In addition to CSS modules, you can style your Next.js application in a variety of ways, including:
	-   Sass which allows you to import `.css` and `.scss` files.
	-   PostCSS libraries like [Tailwind CSS](https://github.com/vercel/next.js/tree/canary/examples/with-tailwindcss).
	-   CSS-in-JS libraries such as [styled-jsx](https://github.com/vercel/styled-jsx), [styled-components](https://github.com/vercel/next.js/tree/canary/examples/with-styled-components), and [emotion](https://github.com/vercel/next.js/tree/canary/examples/with-emotion)

**Global Styles**
- [CSS Modules](https://nextjs.org/docs/basic-features/built-in-css-support#adding-component-level-css) are useful for component-level styles. But if you want some CSS to be loaded by **every page**, Next.js has support for that as well.
- To load [global CSS](https://nextjs.org/docs/basic-features/built-in-css-support#adding-a-global-stylesheet) to your application, create a file called `pages/_app.js` with the following content:
	```jsx
	export default function App({ Component, pageProps }) {
	  return <Component {...pageProps} />;
	}
	```
- The default export of `_app.js` is a top-level React component that wraps all the pages in your application. You can use this component to keep state when navigating between pages, or to add global styles as we're doing here. [Learn more about `_app.js` file](https://nextjs.org/docs/advanced-features/custom-app).

##### Adding Global CSS
- In Next.js, you can add [global CSS](https://nextjs.org/docs/basic-features/built-in-css-support#adding-a-global-stylesheet) files by importing them from [`pages/_app.js`](https://nextjs.org/docs/advanced-features/custom-app). You **cannot** import global CSS anywhere else.
- The reason that [global CSS](https://nextjs.org/docs/basic-features/built-in-css-support#adding-a-global-stylesheet) can't be imported outside of `pages/_app.js` is that global CSS affects all elements on the page.
- If you were to navigate from the homepage to the `/posts/first-post` page, global styles from the homepage would affect `/posts/first-post` unintentionally.
- You can place the global CSS file anywhere and use any name. So let’s do the following:
	-   Create a top-level `styles` directory and a `global.css` file.
	-   Add the following CSS inside `styles/global.css`. This code resets some styles and changes the color of the `a` tag:
	```css
	html,
	body {
	  padding: 0;
	  margin: 0;
	  font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen, Ubuntu,
	    Cantarell, Fira Sans, Droid Sans, Helvetica Neue, sans-serif;
	  line-height: 1.6;
	  font-size: 18px;
	}
	
	* {
	  box-sizing: border-box;
	}
	
	a {
	  color: #0070f3;
	  text-decoration: none;
	}
	
	a:hover {
	  text-decoration: underline;
	}
	
	img {
	  max-width: 100%;
	  display: block;
	}
	```

- Finally, import the CSS file inside the `pages/_app.js` file you've created earlier on:
```jsx
// `pages/_app.js`
import '../styles/global.css';

export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />;
}
```

- [Styling Tips](https://nextjs.org/learn/basics/assets-metadata-css/styling-tips)
	- Using clsx
	- Customizing PostCSS Config
	- Using Sass