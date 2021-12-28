Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Introduction
---
You know a bunch about JavaScript syntax, [control flow](https://www.codecademy.com/courses/introduction-to-javascript/lessons/control-flow/exercises/control-flow-intro), and [functions](https://www.codecademy.com/courses/introduction-to-javascript/lessons/functions/exercises/intro-to-functions)! The best way to reinforce these skills is through practice. We’ve created a series of problems designed to use your JavaScript knowledge. We encourage you to review relevant lessons, look things up in the [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference), check out the hints and solution code if you get stuck, and, most of all, have fun!

The tasks provided are designed to be challenging. Throughout this code challenge, we’ll be running tests to check that the functions you write are working correctly. We’ll often provide some example code to test your function. We encourage you to write additional code to test your functions. To pass our tests, your function will need to work as described in the prompt. This means your function may seem to be passing when you run it, but it will still fail the test because it doesn’t run as expected in every situation we’re testing behind the scenes. Take special note of strings—strings must be _identical_ to that requested to pass!

Initial Editor content:

	// Write your function here:
	
	
	//Write code to test your function. Even if we provide code to test your function, you should add further tests to make sure your function works correctly in all the specified situations

To do:
1. Write a function, `greetWorld()`. Your function should have no parameters and return the string `'Hello, World!'`.
	
	Helpful Notes:

	-   Your function can be a function expression or a function declaration.
	-   Notice that the prompt requires your function to _return_ the string—it will not pass the test if the string is printed to the console rather than returned.
	-   Your code must return `'Hello, World!'` _exactly_. The test will not pass with the following strings: `'hello, world!'`, `'Hello, world!'`, `'Hello World!'`, `'Hello World'`, `'Hello, World.'`, etc.

Final Editor content:

	// Write your function here:
	const greetWorld = () => {
	  return 'Hello, World!';
	}


	//Write code to test your function. Even if we provide code to test your function, you should add further tests to make sure your function works correctly in all the specified situations

	let greeting = greetWorld();
	console.log(greeting);
	console.log(greeting.toLowerCase());
	console.log(greeting.toUpperCase());

Community Forums:
[How do I handle JS (or other computer science problems) I’m not sure how to solve?](https://discuss.codecademy.com/t/how-do-i-handle-js-or-other-computer-science-problems-im-not-sure-how-to-solve/365543)