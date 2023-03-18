[Tutorial](https://nextjs.org/learn/basics/create-nextjs-app)

To build a complete web application with React from scratch, there are many important details you need to consider:

1. Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
2. You need to do production optimizations such as code splitting.
3. You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
4. You might have to write some server-side code to connect your React app to your data store.

A _framework_ can solve these problems. But such a framework must have the right level of abstraction — otherwise it won’t be very useful. It also needs to have great "Developer Experience", ensuring you and your team have an amazing experience while writing code.

### Next.js: The React Framework
Enter **Next.js**, the React Framework. Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the [pit of success](https://blog.codinghorror.com/falling-into-the-pit-of-success/) when building React applications.

Next.js aims to have best-in-class developer experience and many built-in features, such as:
-   An intuitive [page-based](https://nextjs.org/docs/basic-features/pages) routing system (with support for [dynamic routes](https://nextjs.org/docs/routing/dynamic-routes))
-   [Pre-rendering](https://nextjs.org/docs/basic-features/pages#pre-rendering), both [static generation](https://nextjs.org/docs/basic-features/pages#static-generation-recommended) (SSG) and [server-side rendering](https://nextjs.org/docs/basic-features/pages#server-side-rendering) (SSR) are supported on a per-page basis
-   Automatic code splitting for faster page loads
-   [Client-side routing](https://nextjs.org/docs/routing/introduction#linking-between-pages) with optimized prefetching
-   [Built-in CSS](https://nextjs.org/docs/basic-features/built-in-css-support) and [Sass support](https://nextjs.org/docs/basic-features/built-in-css-support#sass-support), and support for any [CSS-in-JS](https://nextjs.org/docs/basic-features/built-in-css-support#css-in-js) library
-   Development environment with [Fast Refresh](https://nextjs.org/docs/basic-features/fast-refresh) support
-   [API routes](https://nextjs.org/docs/api-routes/introduction) to build API endpoints with Serverless Functions
-   Fully extendable

```shell
npx create-next-app@latest nextjs-blog --use-npm --example "https://github.com/vercel/next-learn/tree/master/basics/learn-starter"
```
- Under the hood, this uses the tool called [`create-next-app`](https://nextjs.org/docs/api-reference/create-next-app), which bootstraps a Next.js app for you. It uses [this template](https://github.com/vercel/next-learn/tree/master/basics/learn-starter) through the `--example` flag.
- **Note:** Before Next.js 12.2, it was required that the `Link` component wrapped an `<a>` tag, but [this is not required in versions 12.2 and above](https://nextjs.org/blog/next-12-2#:~:text=next/link%20no%20longer%20requires%20manually%20adding%20%3Ca%3E%20as%20a%20child.%20You%20can%20now%20opt%20into%20this%20behavior%20in%20a%20backward%2Dcompatible%20way.).

#### Code splitting and prefetching
- Next.js does code splitting automatically, so each page only loads what’s necessary for that page. That means when the homepage is rendered, the code for other pages is not served initially.
- This ensures that the homepage loads quickly even if you have hundreds of pages.
- Only loading the code for the page you request also means that pages become isolated. If a certain page throws an error, the rest of the application would still work.
- Furthermore, in a production build of Next.js, whenever [`Link`](https://nextjs.org/docs/api-reference/next/link) components appear in the browser’s viewport, Next.js automatically **prefetches** the code for the linked page in the background. By the time you click the link, the code for the destination page will already be loaded in the background, and the page transition will be near-instant!

**Summary on this section**
- Next.js automatically optimizes your application for the best performance by code splitting, client-side navigation, and prefetching (in production).
- You create routes as files under [`pages`](https://nextjs.org/docs/basic-features/pages) and use the built-in [`Link`](https://nextjs.org/docs/api-reference/next/link) component. No routing libraries are required.
- You can learn more about the `Link` component [in the API reference for `next/link`](https://nextjs.org/docs/api-reference/next/link) and routing in general [in the routing documentation](https://nextjs.org/docs/routing/introduction).
> **Note:** If you need to link to an _external_ page outside the Next.js app, just use an `<a>` tag without `Link`.