Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# agreeOrDisagree()
---
Initial Editor content:

	// Write your function here:



	// Uncomment the line below when you're ready to try out your function
	// console.log(agreeOrDisagree("yep", "yep")) 
	// Should print 'You agree!'

	// We encourage you to add more function call of your own to test your code!

To do:
1. Write a function, `agreeOrDisagree()`, that takes in two strings, and returns `'You agree!'` if the two strings are the same and `'You disagree!'` if the two strings are different.

Final Editor content:

	// Write your function here:
	const agreeOrDisagree = (string1, string2) => {
	  return string1 === string2 ? 'You agree!' : 'You disagree!';

	  // or
	  // if(string1 === string2){
	  //   return 'You agree!';
	  // }
	  // return 'You disagree!';
	}

	//or
	// function agreeOrDisagree(string1, string2){
	//   return string1 === string2 ? 'You agree!' : 'You disagree!';

	//   //or
	//   // if(string1 === string2){
	//   //   return 'You agree!';
	//   // }
	//   // return 'You disagree!';
	// }



	// Uncomment the line below when you're ready to try out your function
	console.log(agreeOrDisagree("yep", "yep")) 
	// Should print 'You agree!'

	// We encourage you to add more function call of your own to test your code!
	console.log(agreeOrDisagree('Hello','World'));

Community Forums:
[What is the difference between triple equals, === , and double equals, == , in JavaScript?](https://discuss.codecademy.com/t/what-is-the-difference-between-triple-equals-and-double-equals-in-javascript/365528)