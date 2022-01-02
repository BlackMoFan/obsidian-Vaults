Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# tipCalculator()
---
Initial Editor content:

	// Write your function here:


	// Uncomment the line below when you're ready to try out your function
	// console.log(tipCalculator('good', 100)) //should return 20

	// We encourage you to add more function calls of your own to test your code!

To do:
1. Create a function, `tipCalculator()`, that has two parameters, a string representing the `quality` of the service received and a number representing the `total` cost.
	
	Return the tip, as a number, based on the following:  
	‘bad’ should return a 5% tip  
	‘ok’ should return a 15% tip  
	‘good’ should return a 20% tip  
	‘excellent’ should return a 30% tip  
	all other inputs should default to 18%  
```
	tipCalculator('good', 100) // Should return 20
```

Final Editor content:

	// Write your function here:
	let tipCalculator = (quality, total) => {
	  switch(quality){
		case 'bad':
		  return total * 0.05;
		case 'ok':
		  return total * 0.15;
		case 'good':
		  return total * 0.2;
		case 'excellent':
		  return total * 0.3;
		default:
		  return total * 0.18;
	  }
	}


	// Uncomment the line below when you're ready to try out your function
	console.log(tipCalculator('good', 100)) //should return 20

	// We encourage you to add more function calls of your own to test your code!

Community Forums:
[How can I set a default return with if/else if/else statements like I do with the default case in a switch statement?](https://discuss.codecademy.com/t/how-can-i-set-a-default-return-with-if-else-if-else-statements-like-i-do-with-the-default-case-in-a-switch-statement/365551)