Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# numImaginaryFriends()

---
Initial Editor content

	// Write your function here:



	// Uncomment the lines below when you're ready to try out your function
	// console.log(numImaginaryFriends(20)) // Should print 5
	// console.log(numImaginaryFriends(10)) // Should print 3 (2.5 rounded up!)

	// We encourage you to add more function calls of your own to test your code!

To do:
1. A person’s number of imaginary friends are always 25% (or 1/4) of their total friends.
	
	Write a function, `numImaginaryFriends()`, that takes in the total number of friends a person has and returns the number of imaginary friends they have.
	
	Since friends can only come in whole numbers, be sure to round your result up to the nearest whole number before returning it.
	
	The JavaScript `Math.ceil()` function will come in handy. Check out [the documentation here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/ceil) to figure out how it works.

Final Editor content:

	// Write your function here:
	let numImaginaryFriends = totalFriends => Math.ceil(totalFriends * .25);


	// Uncomment the lines below when you're ready to try out your function
	console.log(numImaginaryFriends(20)) // Should print 5
	console.log(numImaginaryFriends(10)) // Should print 3 (2.5 rounded up!)

	// We encourage you to add more function calls of your own to test your code!
	console.log(numImaginaryFriends(100)) // Should print 25

Community Forums:
[What other JavaScript Math methods can I use?](https://discuss.codecademy.com/t/what-other-javascript-math-methods-can-i-use/365546)