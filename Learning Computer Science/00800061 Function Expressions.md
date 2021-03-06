Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Function Expressions
---
Another way to define a function is to use a _function expression_. To define a function inside an expression, we can use the `function` keyword. In a function expression, the function name is usually omitted. A function with no name is called an _anonymous function_. A function expression is often stored in a variable in order to refer to it.

Consider the following function expression:

![defining a function expression](https://content.codecademy.com/courses/learn-javascript-functions/Diagram/expression.svg)

To declare a function expression:

1.  Declare a variable to make the variable’s name be the name, or identifier, of your function. Since the release of ES6, it is common practice to use `const` as the keyword to declare the variable.
    
2.  Assign as that variable’s value an anonymous function created by using the `function` keyword followed by a set of parentheses with possible parameters. Then a set of curly braces that contain the function body.
    

To invoke a function expression, write the name of the variable in which the function is stored followed by parentheses enclosing any arguments being passed into the function.

```
variableName(argument1, argument2)
```

Unlike function declarations, function expressions are not hoisted so they cannot be called before they are defined.

Let’s define a new function using a function expression.

To do:
1. Let’s say we have a plant that we need to water once a week on Wednesdays. We could define a function expression to help us check the day of the week and the plant needs to be watered:

	-   Create a variable named `plantNeedsWater` using the `const` variable keyword.
	-   Assign an anonymous function that takes in a parameter of `day` to `plantNeedsWater`.

2. Now we need to add some code to the function body of `plantNeedsWater()`:

	-   In the function body add an `if` conditional that checks `day === 'Wednesday'`.
	-   If the conditional is truthy, inside the `if` code block, use the `return` keyword to return `true`.

3. On days that aren’t `'Wednesday'`, `plantNeedsWater()` should return `false`:

	-   Add an `else` statement after the `if` statement.
	-   Inside the `else` statement use the `return` keyword to return `false`.

4. Call the `plantNeedsWater()` and pass in `'Tuesday'` as an argument.
5. Let’s check that `plantNeedsWater()` returned the expected value.
	
	Log `plantNeedsWater('Tuesday')` to the console. If it worked correctly, you should see `false` logged to the console.

Editor content:

	const plantNeedsWater = function(day){
	  if(day === 'Wednesday'){
		return true;
	  }
	  return false;
	}

	console.log(plantNeedsWater('Tuesday'));

Community Forums:
[Can you change parameters on constant functions?](https://discuss.codecademy.com/t/can-you-change-parameters-on-constant-functions/437639)
[What are the advantages of function expressions?](https://discuss.codecademy.com/t/what-are-the-advantages-of-function-expressions/437661)
[Why do I need to call the function vs logging it?](https://discuss.codecademy.com/t/why-do-i-need-to-call-the-function-vs-logging-it/437657)