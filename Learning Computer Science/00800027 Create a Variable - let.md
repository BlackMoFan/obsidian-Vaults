Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Create a Variable:  let
---
As mentioned in the previous exercise, the `let` keyword was introduced in ES6. The `let` keyword signals that the variable can be reassigned a different value. Take a look at the example:

	let meal = 'Enchiladas';console.log(meal); // Output: Enchiladasmeal = 'Burrito';console.log(meal); // Output: Burrito

Another concept that we should be aware of when using `let` (and even `var`) is that we can declare a variable without assigning the variable a value. In such a case, the variable will be automatically initialized with a value of `undefined`:

	let price;console.log(price); // Output: undefinedprice = 350;console.log(price); // Output: 350

Notice in the example above:

-   If we don’t assign a value to a variable declared using the `let` keyword, it automatically has a value of `undefined`.
-   We can reassign the value of the variable.

To do:
1. Create a `let` variable called `changeMe` and set it equal to the boolean `true`.
2. On the line after `changeMe` is declared, set the value of `changeMe` to be the boolean `false`.
	
	To check if `changeMe` was reassigned, log the value saved to `changeMe` to the console.

Editor Content:

	let changeMe = true;
	changeMe = false;
	console.log(changeMe);
	
Community Forums:
[What are the differences between var and let? Which should I use?](https://discuss.codecademy.com/t/what-are-the-differences-between-var-and-let-which-should-i-use/492201)
[Why don’t we need quotations for numbers or booleans?](https://discuss.codecademy.com/t/why-dont-we-need-quotations-for-numbers-or-booleans/492202)
[ Why would we want to reassign a new value to a variable?](https://discuss.codecademy.com/t/why-would-we-want-to-reassign-a-new-value-to-a-variable/492215)