Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# toEmoticon()
---
Initial Editor content:

	// Write your function here:

	// Uncomment the line below when you're ready to try out your function
	// console.log(toEmoticon("whatever")) 
	// Should print  '|_(* ~ *)_|'

	// We encourage you to add more function calls of your own to test your code!

To do:
1. Write a function, `toEmoticon()`, that takes in a string and returns the corresponding emoticon as a string. Use a switch/case, and cover these cases:

	`'shrug'` should return `'|_{"}_|'`  
	`'smiley face'` should return `':)'`  
	`'frowny face'` should return`':('`  
	`'winky face'` should return `';)'`  
	`'heart'` should return `'<3'`  
	any other input should return `'|_(* ~ *)_|'`

Final Editor content:

	// Write your function here:
	let toEmoticon = word => {
	  switch(word){
		case 'shrug':
		  return '|_{"}_|';
		case 'smiley face':
		  return ':)';
		case 'frowny face':
		  return ':(';
		case 'winky face':
		  return ';)';
		case 'heart':
		  return '<3';
		default:
		  return '|_(* ~ *)_|';
	  }
	}


	// Uncomment the line below when you're ready to try out your function
	console.log(toEmoticon("whatever")) 
	// Should print  '|_(* ~ *)_|'

	// We encourage you to add more function calls of your own to test your code!

Community Forums:
[What does the break statement do in a switch statement?](https://discuss.codecademy.com/t/what-does-the-break-statement-do-in-a-switch-statement/365552)