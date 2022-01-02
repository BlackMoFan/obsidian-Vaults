Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# sillySentence()

---
	Initial Editor content:

	// Write your function here:


	// Uncomment the line below when you're ready to try out your function
	// console.log(sillySentence('excited', 'love', 'functions')) 

	// We encourage you to add more function calls of your own to test your code!

To do:
1. Write a function, `sillySentence()`, that has 3 string parameters and returns the following silly sentence with the blanks filled in by the arguments passed into the function:

	![](https://content.codecademy.com/courses/js-fundamentals-code-challenge/sillySentence.svg)  

		sillySentence('excited', 'love', 'functions');  
		// Should return 'I am so excited because I love coding! Time to write some more awesome functions!'

Final Editor content:

	// Write your function here:
	let sillySentence = (param1, param2, param3) => `I am so ${param1} because I ${param2} coding! Time to write some more awesome ${param3}!`


	// Uncomment the line below when you're ready to try out your function
	console.log(sillySentence('excited', 'love', 'functions')) 

	// We encourage you to add more function calls of your own to test your code!
	console.log(sillySentence('happy', 'am learning', 'notes')) 

Community Forums:
[Can I concatenate strings with other data types? Can I interpolate strings with other data types?](https://discuss.codecademy.com/t/can-i-concatenate-strings-with-other-data-types-can-i-interpolate-strings-with-other-data-types/365550)