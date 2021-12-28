Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# finalGrade()
---
Initial Editor content:

	// Write your function here:


	// Uncomment the line below when you're ready to try out your function
	// console.log(finalGrade(99, 92, 95)) // Should print 'A'

	// We encourage you to add more function calls of your own to test your code!

To do:
1. Write a function, `finalGrade()`. It should:

	-   take three arguments of type number
	-   find the `average` of those three numbers
	-   return the letter grade (as a string) that the `average` corresponds to
	-   return ‘You have entered an invalid grade.’ if any of the three grades are less than 0 or greater than 100

	0-59 should return: `'F'`  
	60-69 should return: `'D'`  
	70-79 should return: `'C'`  
	80-89 should return: `'B'`  
	90-100 should return: `'A'`

Final Editor content:

	// Write your function here:
	const finalGrade = (firstGrade, secondGrade, thirdGrade) => {
	  if ((firstGrade < 0 || firstGrade > 100) || (secondGrade < 0 || secondGrade > 100) || (thirdGrade < 0 || thirdGrade > 100)){
		return 'You have entered an invalid grade.';
	  }
	  const average = (firstGrade + secondGrade + thirdGrade) / 3;
	  if(average < 60){
		return 'F';
	  } else if(average < 70){
		return 'D';
	  } else if(average < 80){
		return 'C';
	  } else if(average < 90){
		return 'B';
	  } else if(average < 101){
		return 'A';
	  }
	}





	// Uncomment the line below when you're ready to try out your function
	console.log(finalGrade(99, 92, 95)) // Should print 'A'

	// We encourage you to add more function calls of your own to test your code!
	console.log(finalGrade(99, 92, 101)) // Should print 'You have entered an invalid grade.'
	console.log(finalGrade(80, 85, 87)) // Should print 'B'
	console.log(finalGrade(70, 75, 69)) // Should print 'C'
	console.log(finalGrade(60, 65, 59)) // Should print 'D'
	console.log(finalGrade(50, 55, 49)) // Should print 'F'

Community Forums:
[How to format switch/case?](https://discuss.codecademy.com/t/is-there-logic-behind-this/375351)
[What does the || operator do?](https://discuss.codecademy.com/t/what-does-the-operator-do/365532)
[Defining variables within an if/else block](https://discuss.codecademy.com/t/defining-variables-within-an-if-else-block/434729)