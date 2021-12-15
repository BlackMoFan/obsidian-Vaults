Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Concise Body Arrow Functions
---
JavaScript also provides several ways to refactor arrow function syntax. The most condensed form of the function is known as _concise body_. We’ll explore a few of these techniques below:

1.  Functions that take only a single parameter do not need that parameter to be enclosed in parentheses. However, if a function takes zero or multiple parameters, parentheses are required.
    
    ![showcasing how arrow functions parameters differ for different amounts of parameters](https://content.codecademy.com/courses/learn-javascript-functions/Diagram/parameters.svg)
2.  A function body composed of a single-line block does not need curly braces. Without the curly braces, whatever that line evaluates will be automatically returned. The contents of the block should immediately follow the arrow `=>` and the `return` keyword can be removed. This is referred to as _implicit return_.
    

![comparing single line and multiline arrow functions](https://content.codecademy.com/courses/learn-javascript-functions/Diagram/return.svg)

So if we have a function:

	const squareNum = (num) => {  
	 return num * num;  
	};

We can refactor the function to:

```
const squareNum = num => num * num;
```

Notice the following changes:

-   The parentheses around `num` have been removed, since it has a single parameter.
-   The curly braces `{ }` have been removed since the function consists of a single-line block.
-   The `return` keyword has been removed since the function consists of a single-line block.

To do:
1. Let’s refactor `plantNeedsWater()` to be a concise body. Notice that we’ve already converted the `if`/`else` statement to a ternary operator to make the code fit on one line.

Editor content:

	const plantNeedsWater = day => day === 'Wednesday' ? true : false;

	console.log(plantNeedsWater('Wednesday'));