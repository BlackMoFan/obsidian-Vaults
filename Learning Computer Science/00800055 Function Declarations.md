Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Function Declarations
---
In JavaScript, there are many ways to create a function. One way to create a function is by using a _function declaration_. Just like how a variable declaration binds a value to a variable name, a function declaration binds a function to a name, or an _identifier_. Take a look at the anatomy of a function declaration below:

![Diagram showing the syntax of a function declaration](https://content.codecademy.com/courses/learn-javascript-functions/Diagram/declaration.svg)

A function declaration consists of:

-   The `function` keyword.
-   The name of the function, or its identifier, followed by parentheses.
-   A function body, or the block of statements required to perform a specific task, enclosed in the function’s curly brackets, `{ }`.

A function declaration is a function that is bound to an identifier, or name. In the next exercise we’ll go over how to run the code inside the function body.

We should also be aware of the _hoisting_ feature in JavaScript which allows access to function declarations before they’re defined.

Take a look at example of hoisting:

	greetWorld(); // Output: Hello, World!  

	function greetWorld() {  
	 console.log('Hello, World!');  
	}

Notice how hoisting allowed `greetWorld()` to be called before the `greetWorld()` function was defined! Since hoisting isn’t considered good practice, we simply want you to be aware of this feature.

If you want to read more about hoisting, check out [MDN documentation on hoisting](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting).

To do:
1. Let’s create a function that prints a reminder to the console. Using a function declaration, create a function called `getReminder()`.
2. In the function body of `getReminder()`, log the following reminder to the console: `'Water the plants.'`
3. Let’s create another function that prints a useful Spanish travel phrase to the console.
	
	Using a function declaration, create a function called `greetInSpanish()`.

4. Add code to the function body of `greetInSpanish()`:

	-   In the function body `console.log()` the following Spanish phrase to the console: `'Buenas Tardes.'`

Editor Content:

	function getReminder(){
	  console.log('Water the plants.');
	}

	function greetInSpanish(){
	  console.log('Buenas Tardes.');
	}

	greetInSpanish();
	getReminder();