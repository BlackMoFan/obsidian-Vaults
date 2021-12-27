Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Blocks and Scope
---
Before we talk more about scope, we first need to talk about _blocks_.

We’ve seen blocks used before in functions and `if` statements. A block is the code found inside a set of curly braces `{}`. Blocks help us group one or more statements together and serve as an important structural marker for our code.

A block of code could be a function, like this:

	const logSkyColor = () => {  
	 let color = 'blue';  
	 console.log(color); // blue  
	}

Notice that the function body is actually a block of code.

Observe the block in an `if` statement:

	if (dusk) {  
	 let color = 'pink';  
	 console.log(color); // pink  
	}

In the next few exercises, we’ll see how blocks define the scope of variables.

To do:
1. At the top of **main.js**, declare a `const` variable, named `city` set equal to `'New York City'`. This variable will exist _outside_ of the block.
2. Below the `city` variable, write a function named `logCitySkyline`.
3. Inside of the function body of `logCitySkyline()`, write another variable using `let` named `skyscraper` and set it equal to `'Empire State Building'`.
4. Inside the function, include a return statement like this:

	```
	return 'The stars over the ' + skyscraper + ' in ' + city;
	```
5. Beneath the `logCitySkyline()` function, use `console.log()` to log the value of `logCitySkyline()` to the console.


Editor content:

	const city = 'New York City';

	const logCitySkyline = () => {
	  let skyscraper = 'Empire State Building';
	  return 'The stars over the ' + skyscraper + ' in ' + city;
	}

	console.log(logCitySkyline());