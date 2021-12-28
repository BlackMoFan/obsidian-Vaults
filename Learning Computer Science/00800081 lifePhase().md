Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# lifePhase()
---
Initial Editor content:

	// Write your function here:




	// Uncomment the line below when you're ready to try out your function
	// console.log(lifePhase(5)) //should print 'child'

	// We encourage you to add more function calls of your own to test your code!

To do:
1. Write a function, `lifePhase()`, that takes in a person’s `age`, as a number, and returns which phase of life they are in.
	
	Here are the classifications:  
	0-3 should return `'baby'`  
	4-12 should return `'child'`  
	13-19 should return `'teen'`  
	20-64 should return `'adult'`  
	65-140 should return `'senior citizen'`  
	If the number is less than 0 or greater than 140, the program should return `'This is not a valid age'`

Final Editor content:

	// Write your function here:
	const lifePhase = age => {
	  if(age < 0 || age > 140){
		return 'This is not a valid age';
	  } else if(age < 4){
		return 'baby';
	  } else if(age < 13){
		return 'child';
	  } else if(age < 20){
		return 'teen';
	  } else if(age < 65){
		return 'adult';
	  } else if(age < 141){
		return 'senior citizen';
	  } else {
		return 'Input error';
	  }
	}



	// Uncomment the line below when you're ready to try out your function
	console.log(lifePhase(5)) //should print 'child'

	// We encourage you to add more function calls of your own to test your code!
	console.log(lifePhase(3));
	console.log(lifePhase(10));
	console.log(lifePhase(18));
	console.log(lifePhase(20)); 
	console.log(lifePhase(121));
	console.log(lifePhase(1000));

Community Forums:
[When should I use multiple if statements? When should I use if statements with else if statements?](https://discuss.codecademy.com/t/when-should-i-use-multiple-if-statements-when-should-i-use-if-statements-with-else-if-statements/365545)
[How could I use a switch statement for this lesson?](https://discuss.codecademy.com/t/how-could-i-use-a-switch-statement-for-this-lesson/446724)
[Is it better to make my conditionals more simplified?](https://discuss.codecademy.com/t/is-it-better-to-make-my-conditionals-more-simplified/446727)