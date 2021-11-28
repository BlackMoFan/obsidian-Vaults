Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Arithmetic Operators
---
Basic arithmetic often comes in handy when programming.

An _operator_ is a character that performs a task in our code. JavaScript has several built-in _arithmetic operators_, that allow us to perform mathematical calculations on numbers. These include the following operators and their corresponding symbols:

1.  Add: `+`
2.  Subtract: `-`
3.  Multiply: `*`
4.  Divide: `/`
5.  Remainder: `%`

The first four work how you might guess:

	console.log(3 + 4); // Prints 7console.log(5 - 1); // Prints 4console.log(4 * 2); // Prints 8console.log(9 / 3); // Prints 3

Note that when we `console.log()` the computer will evaluate the expression inside the parentheses and print that result to the console. If we wanted to print the characters `3 + 4`, we would wrap them in quotes and print them as a string.

	console.log(11 % 3); // Prints 2console.log(12 % 3); // Prints 0

The remainder operator, sometimes called _modulo_, returns the number that remains after the right-hand number divides into the left-hand number as many times as it evenly can: `11 % 3` equals 2 because 3 fits into 11 three times, leaving 2 as the remainder.

To do:
1. Inside of a `console.log()`, add `3.5` to your age.
	This is the age you’ll be when we start sending people to live on Mars.
2. On a new line write another `console.log()`. Inside the parentheses, take the current year and subtract `1969`.
	The answer is how many years it’s been since the 1969 moon landing.
3. Create another `console.log()`. Inside the parentheses divide `65` by `240`.
4. Create one last `console.log()`. Inside the parentheses, multiply `0.2708` by `100`.
	That’s the percent of the sun that is made up of helium. Assuming we could stand on the sun, we’d all sound like chipmunks!
	
Editor content:

	console.log(20 + 3.5);
	console.log(2021 - 1969);
	console.log(65 / 240);
	console.log(0.2708 * 100);

Community Forums:
[What is the difference between printing 3 + 4 and '3 + 4'?](https://discuss.codecademy.com/t/what-is-the-difference-between-printing-3-4-and-3-4/489337)
[ How does Javascript handle a negative modulo? (-5 % 20)](https://discuss.codecademy.com/t/how-does-javascript-handle-a-negative-modulo-5-20/489339)