Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# String Interpolation
---
In the ES6 version of JavaScript, we can insert, or _interpolate_, variables into strings using _template literals_. Check out the following example where a template literal is used to log strings together:

	const myPet = 'armadillo';
	console.log(`I own a pet ${myPet}.`);
	// Output: I own a pet armadillo.

Notice that:

-   a template literal is wrapped by backticks `` ` `` (this key is usually located on the top of your keyboard, left of the 1 key).
-   Inside the template literal, you’ll see a placeholder, `${myPet}`. The value of `myPet` is inserted into the template literal.
-   When we interpolate `` `I own a pet ${myPet}.` ``, the output we print is the string: `'I own a pet armadillo.'`

One of the biggest benefits to using template literals is the readability of the code. Using template literals, you can more easily tell what the new string will be. You also don’t have to worry about escaping double quotes or single quotes.

To do:

1. Create a variable called `myName` and assign it your name.
2. Create a variable called `myCity` and assign it your favorite city’s name.
3. Use a single template literal to interpolate your variables into the sentence below. Use `console.log()` to print your sentence to the console in the following format:

		My name is NAME. My favorite city is CITY.

	Replace `NAME` and `CITY` in the string above by interpolating the values saved to `myName` and `myCity`.
	
	Editor content:
	
		let myName = "Black Mo Fan", myCity = "God's Domain";
		let sentence = `My name is ${myName}. My favorite city is ${myCity}`;
		console.log(`My name is ${myName}. My favorite city is ${myCity}`); 
		//or console.log(sentence);

Community Forums:
[Why isn’t string interpolation working? (Check for backticks)](https://discuss.codecademy.com/t/why-isnt-string-interpolation-working-check-for-backticks/492529)
[Why should we use template literals?](https://discuss.codecademy.com/t/why-should-we-use-template-literals/492542)
[Did I spell favourite wrong?](https://discuss.codecademy.com/t/did-i-spell-favourite-wrong/492546)