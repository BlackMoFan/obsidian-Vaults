Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# reportingForDuty()
---
Initial Editor content:

	// Write your function here:



	// Uncomment the line below when you're ready to try out your function
	// console.log(reportingForDuty('Private', 'Fido')) // Should return 'Private Fido reporting for duty!'

	// We encourage you to add more function calls of your own to test your code!

To do:
1. Write a function, `reportingForDuty()`, that has two string parameters, `rank` and `lastName`, and returns a string in the following format: ‘rank lastName reporting for duty!’
	
		reportingForDuty('Private', 'Fido')  
		// Should return 'Private Fido reporting for duty!'

Final Editor content:

	// Write your function here:
	const reportingForDuty = (rank, lastName) => {
	  return `${rank} ${lastName} reporting for duty!`;
	}


	// Uncomment the line below when you're ready to try out your function
	console.log(reportingForDuty('Private', 'Fido')) // Should return 'Private Fido reporting for duty!'

	// We encourage you to add more function calls of your own to test your code!

[Is it best practice to use string concatenation or string interpolation ? Why?](https://discuss.codecademy.com/t/is-it-best-practice-to-use-string-concatenation-or-string-interpolation-why/365547)