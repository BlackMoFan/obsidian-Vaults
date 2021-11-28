Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Create a Variable:  var
---
There were a lot of changes introduced in the ES6 version of JavaScript in 2015. One of the biggest changes was two new keywords, `let` and `const`, to create, or _declare_, variables. Prior to the ES6, programmers could only use the `var` keyword to declare variables.

	var myName = 'Arya';console.log(myName);// Output: Arya

Let’s consider the example above:

1.  `var`, short for variable, is a JavaScript _keyword_ that creates, or _declares_, a new variable.
2.  `myName` is the variable’s name. Capitalizing in this way is a standard convention in JavaScript called _camel casing_. In camel casing you group words into one, the first word is lowercase, then every word that follows will have its first letter uppercased. (e.g. camelCaseEverything).
3.  `=` is the _assignment operator_. It assigns the value (`'Arya'`) to the variable (`myName`).
4.  `'Arya'` is the _value_ assigned (`=`) to the variable `myName`. You can also say that the `myName` variable is _initialized_ with a value of `'Arya'`.
5.  After the variable is declared, the string value `'Arya'` is printed to the console by referencing the variable name: `console.log(myName)`.

There are a few general rules for naming variables:

-   Variable names cannot start with numbers.
-   Variable names are case sensitive, so `myName` and `myname` would be different variables. It is bad practice to create two variables that have the same name using different cases.
-   Variable names cannot be the same as _keywords_. For a comprehensive list of keywords check out [MDN’s keyword documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Keywords).

Note: In the next exercises, we will learn why ES6’s `let` and `const` are the preferred variable keywords by many programmers. Because there is still a ton of code written prior to ES6, it’s helpful to be familiar with the pre-ES6 `var` keyword.

If you want to learn more about `var` and the quirks associated with it, check out the [MDN var documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var).

To do:
1. Declare a variable named `favoriteFood` using the `var` keyword and assign to it the string `'pizza'`.
2. Declare a variable named `numOfSlices` using the `var` keyword and assign to it the number `8`.
3. Under the `numOfSlices` variable, use `console.log()` to print the value saved to `favoriteFood`.
	
	On the following line, use `console.log()` to print the value saved to `numOfSlices`.
	
Editor Content:

	var favoriteFood = 'pizza';
	var numOfSlices = 8;
	console.log(favoriteFood);
	console.log(numOfSlices);

Community Forums:
[Do we need apostraphes for number variables?](https://discuss.codecademy.com/t/do-we-need-apostraphes-for-number-variables/491667)
[Why should we use var or let instead of the other?](https://discuss.codecademy.com/t/when-to-use-var-or-let/491677)