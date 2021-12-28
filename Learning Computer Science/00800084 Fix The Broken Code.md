Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Fix The Broken Code
---
Initial Editor content:

	const rollTheDice = () => {
	  // Math.random() gives us a random number from 0 up to, but not including, 1
	  // We multiplied that by 6 to get a number between 0 and up to, but not including, 6
	  // But since we actually wanted numbers from 1 to 6, inclusive, we added 1
		let die1 = Math.random() * 6 + 1
		let die2 = Math.random() * 6 + 1
		return die1 + die2
	}

To do:
1. We wrote a function, `rollTheDice()`, which is supposed to simulate two dice being rolled and totalled. It’s close to doing what we want, but there’s something not quite right. Can you fix our code, please?

Final Editor content:

	const rollTheDice = () => {
	  // Math.random() gives us a random number from 0 up to, but not including, 1
	  // We multiplied that by 6 to get a number between 0 and up to, but not including, 6
	  // But since we actually wanted numbers from 1 to 6, inclusive, we added 1
		let die1 = Math.floor(Math.random() * 6 + 1);
		let die2 = Math.floor(Math.random() * 6 + 1);
		return die1 + die2
	}

	console.log(rollTheDice());
	
Community Forums:
[What does Math.floor() do? How do I use it?](https://discuss.codecademy.com/t/what-does-math-floor-do-how-do-i-use-it/365534)