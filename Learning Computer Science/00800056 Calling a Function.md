Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Calling a Function
---
As we saw in previous exercises, a function declaration binds a function to an identifier.

However, a function declaration does not ask the code inside the function body to run, it just declares the existence of the function. The code inside a function body runs, or _executes_, only when the function is _called_.

To call a function in your code, you type the function name followed by parentheses.

![Diagram showing the syntax of invoking a function](https://content.codecademy.com/courses/learn-javascript-functions/Diagram/name.svg)

This _function call_ executes the function body, or all of the statements between the curly braces in the function declaration.![Function execution diagram](https://content.codecademy.com/courses/learn-javascript-functions/Diagram/function%20execution.svg)

We can call the same function as many times as needed.

Let’s practice calling functions in our code.

To do:
1. Imagine that you manage an online store. When a customer places an order, you send them a thank you note. Let’s create a function to complete this task:

	-   Define a function called `sayThanks()` as a function declaration.
	-   In the function body of `sayThanks()`, add code such that the function writes the following thank you message to the console when called: `'Thank you for your purchase! We appreciate your business.'`
2. Call `sayThanks()` to view the thank you message in the console.
3. Functions can be called as many times as you need them.
	
	Imagine that three customers placed an order and you wanted to send each of them a thank you message. Update your code to call `sayThanks()` three times.

Editor content:

	function sayThanks(){
	  console.log('Thank you for your purchase! We appreciate your business.');
	}

	// let numOfCustomers = 3;

	// for(let i = 0; i < numOfCustomers; i++){
	//   sayThanks();
	// }

	sayThanks();
	sayThanks();
	sayThanks();