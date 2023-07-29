## Pre-rendering and Data Fetching
<<<<<<< HEAD
=======

### Pre-rendering:
- By default, Next.js pre-renders every page. This means that Next.js _generates HTML for each page in advance_, instead of having it all done by client-side JavaScript. Pre-rendering can result in better performance and [SEO](https://en.wikipedia.org/wiki/Search_engine_optimization). --> **ReactJS does not have this.**
- Two forms:
	- Static Generation
		- generates the HTML at **build time**
		- The pre-rendered HTML is then _reused_ on each request.
	- Server-side Rendering
		- generates the HTML on **each request**.
	- Difference is when it generates the HTML for a page
- 'Hydration'
	- Each generated HTML is associated with minimal JavaScript code necessary for that page. When a page is loaded by the browser, its JavaScript code runs and makes the page fully interactive.
- #### When to use Static Generation v.s. Server-side Rendering
	- We recommend using [**Static Generation**](https://nextjs.org/docs/basic-features/pages#static-generation-recommended) (with and without data) whenever possible because your page can be built once and served by CDN, which makes it much faster than having a server render the page on every request.
	- You can use [Static Generation](https://nextjs.org/docs/basic-features/pages#static-generation-recommended) for many types of pages, including:
		-   Marketing pages
		-   Blog posts
		-   E-commerce product listings
		-   Help and documentation
	- You should ask yourself: "Can I pre-render this page **ahead** of a user's request?" If the answer is yes, then you should choose [Static Generation](https://nextjs.org/docs/basic-features/pages#static-generation-recommended).
	- On the other hand, [Static Generation](https://nextjs.org/docs/basic-features/pages#static-generation-recommended) is **not** a good idea if you cannot pre-render a page ahead of a user's request. Maybe your page shows frequently updated data, and the page content changes on every request.
		- In that case, you can use [**Server-side Rendering**](https://nextjs.org/docs/basic-features/pages#server-side-rendering). It will be slower, but the pre-rendered page will always be up-to-date. Or you can skip pre-rendering and use client-side JavaScript to populate frequently updated data.

#### Static Generation with and without Data
- [Static Generation](https://nextjs.org/docs/basic-features/pages#static-generation-recommended) can be done with and without data.
##### Static Generation with Data using `getStaticProps`
>>>>>>> d545c668a0594a114628cf930b2c0eecbb49b676
