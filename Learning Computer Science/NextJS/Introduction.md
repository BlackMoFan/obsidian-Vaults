[Main tutorial site](https://nextjs.org/learn/foundations/about-nextjs)

- maintained by Vercel
- to create, run `npx create-next-app` in terminal
- a React framework
- Building blocks of web applications:
	1. User Interface - user interacts with this
	2. Routing - navigation
	3. Data Fetching - where data lives and fetching it
	4. Rendering - rendering of static or dynamic content
	5. Integrations - connections to third-party services (CMS, auth, payments, etc.)
	6. Infrastructure - where you deploy, store, and run the application code (serverless, CDN, etc.)
	7. Performance - how to optimize the application for end-users
	8. Scalability - how app adapts as team, data, and traffic grow
	9. Developer Experience - the team's experience building and maintaining the application

## What is React?
	React is a JavaScript library for building interactive UI

- it is up to the developer whether to use the functions in libraries or not
- React is relatively unopinionated (no "right" way to do something, no style guide)
- developers need to spend time configuring tools and reinventing solutions for common application requirements\
- Three core concepts of React:
	1. Components
		- Components allow you to build self-contained, reusable snippets of code. If you think of components as **LEGO bricks**, you can take these individual bricks and combine them together to form larger structures. If you need to update a piece of the UI, you can update the specific component or brick.
	2. Props
		- In ReactJS, the props are **a type of object where the value of attributes of a tag is stored**. The word “props” implies “properties”, and its working functionality is quite similar to HTML attributes. Basically, these props components are read-only components.
	3. State and Hooks
		- React has a set of functions called [hooks](https://reactjs.org/docs/hooks-intro.html). Hooks allow you to add additional logic such as **state** to your components. You can think of state as any information in your UI that changes over time, usually triggered by user interaction
		- You can _use state_ to store and increment the number of times a user has clicked the like button. In fact, this is what the React hook to manage state is called: `useState()`
		- `useState()` returns an array, and you can access and use those array values inside your component using **array destructuring**:
		- The first item in the array is the state `value`, which you can name anything. It’s recommended to name it something descriptive:
			```jsx
			function HomePage() {
			  const [likes] = React.useState();
			
			  // ...
			}
			```
		- The second item in the array is a function to `update` the value. You can name the update function anything, but it's common to prefix it with `set` followed by the name of the state variable you’re updating:
			```jsx
			function HomePage() {
			  const [likes, setLikes] = React.useState();
			
			  // ...
			}
			```
		- You can also take the opportunity to add the initial value of your `likes` state: zero.
			```jsx
			function HomePage() {
			  const [likes, setLikes] = React.useState(0);
			}
		  ```
		- In React, `useState`, as well as any other function starting with ”`use`”, is called a Hook.
		- _Hooks_ are special functions that are only available while React is [rendering](https://react.dev/learn/render-and-commit#step-1-trigger-a-render). They let you “hook into” different React features.
		- State is just one of those features.

How to comment in JS, react, and inside of return ()
	- JS: //, or /* */
	- React: //
	- inside of return (): {/* * */}

- React needs something to uniquely identify items in an array so it knows which elements to update in the DOM

## What is Next.js?

- is a React framework
- by framework, meaning Next.js handles the tooling and configuration needed for React
	- provides additional structure, features, optimizations for app

- You can use React to build your UI, then incrementally adopt Next.js features to solve common application requirements such as routing, data fetching, integrations - all while improving the developer and end-user experience.
- **Fast Refresh**
	- This feature is called [Fast Refresh](https://nextjs.org/docs/basic-features/fast-refresh). It gives you instantaneous feedback on any edits you make and comes pre-configured with Next.js.
	-  Fast Refresh is enabled by default in all Next.js applications on **9.4 or newer**. With Next.js Fast Refresh enabled, most edits should be visible within a second, **without losing component state**.
	- How It Works
		- If you edit a file that **only exports React component(s)**, Fast Refresh will update the code only for that file, and re-render your component. You can edit anything in that file, including styles, rendering logic, event handlers, or effects.
		- If you edit a file with exports that _aren't_ React components, Fast Refresh will re-run both that file, and the other files importing it. So if both `Button.js` and `Modal.js` import `theme.js`, editing `theme.js` will update both components.
- Benefits of using Next.js
	- no babel script, a taste of the complex tooling configuration you no longer have to think about.
	- Fast Refresh