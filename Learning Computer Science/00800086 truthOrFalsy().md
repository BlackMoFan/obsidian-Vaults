Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# truthyOrFalsy()
---
Initial Editor content:

	// Write your function here:




	// Uncomment the line below when you're ready to try out your function
	// console.log(truthyOrFalsy(0)) // Should print false

	// We encourage you to add more function calls of your own to test your code!

To do:
1. It can be hard to keep track of [what’s **truthy** or **falsy** in JavaScript](https://developer.mozilla.org/en-US/docs/Glossary/Falsy). Write a function, `truthyOrFalsy()`, that takes in any value and returns `true` if that value is **truthy** and `false` if that value is **falsy**.

Final Editor content:

	// Write your function here:
	const truthyOrFalsy = value => {
	  return value ? true : false;
	}




	// Uncomment the line below when you're ready to try out your function
	console.log(truthyOrFalsy(0)) // Should print false

	// We encourage you to add more function calls of your own to test your code!
	console.log(truthyOrFalsy(null))
	console.log(truthyOrFalsy('null'))
	console.log(truthyOrFalsy(1))

Community Forums:
[What are falsy values in JS? What are truthy values in JS?](https://discuss.codecademy.com/t/what-are-falsy-values-in-js-what-are-truthy-values-in-js/365553)