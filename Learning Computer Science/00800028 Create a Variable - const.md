Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Create a Variable: const
---
The `const` keyword was also introduced in ES6, and is short for the word constant. Just like with `var` and `let` you can store any value in a `const` variable. The way you declare a `const` variable and assign a value to it follows the same structure as `let` and `var`. Take a look at the following example:

	const myName = 'Gilberto';console.log(myName); // Output: Gilberto

However, a `const` variable cannot be reassigned because it is _constant_. If you try to reassign a `const` variable, you’ll get a `TypeError`.

Constant variables _must_ be assigned a value when declared. If you try to declare a `const` variable without a value, you’ll get a `SyntaxError`.

If you’re trying to decide between which keyword to use, `let` or `const`, think about whether you’ll need to reassign the variable later on. If you do need to reassign the variable use `let`, otherwise, use `const`.

To do:
1. Create a constant variable named `entree` and set it to equal to the string `'Enchiladas'`.
2. Just to check that you’ve saved the value of `'Enchiladas'` to `entree`, log the value of `entree` to the console.
3. Great, let’s see what happens if you try to reassign a constant variable.
	Paste the following code to the bottom of your program.

		entree = 'Tacos'

	This code throws the following error when you run your code:
	
		TypeError: Assignment to constant variable.

After you clear this checkpoint, if you want to see about another quirk of `const` in action open the hint!

Hint:
Since our program stops running after encountering an error, we need to delete the line of code from the previous step:

	entree = 'Tacos'

Now, let’s test what happens when you try to declare a `const` variable _without_ a value. Paste in the following code to your program:

	const testing;

You should see a different error this time:

	SyntaxError: Missing initializer in const declaration

If you read through this error, you’ll see that it’s related to syntax, you need to initialize a `const` variable with a value.

Editor Content:

	const entree = 'Enchiladas';
	console.log(entree);
	entree = 'Tacos';
	
Community Forums:
[ What are the differences between var and let? Are they necessary?](https://discuss.codecademy.com/t/what-are-the-differences-between-var-and-let-are-they-necessary/492237/2)