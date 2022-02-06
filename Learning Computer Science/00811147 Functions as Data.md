Links:  [[008111 Create a Front-End App with React from Codecademy]]
# Functions as Data

---
JavaScript functions behave like any other data type in the language; we can assign functions to variables, and we can reassign them to new variables.

Below, we have an annoyingly long function name that hurts the readability of any code in which it’s used. Let’s pretend this function does important work and needs to be called repeatedly!

	const announceThatIAmDoingImportantWork = () => {  
		console.log("I’m doing very important work!");  
	};

What if we wanted to rename this function without sacrificing the source code? We can re-assign the function to a variable with a suitably short name:

	const busy = announceThatIAmDoingImportantWork;  

	busy(); // This function call barely takes any space!

`busy` is a variable that holds a _reference_ to our original function. If we could look up the address in memory of `busy` and the address in memory of `announceThatIAmDoingImportantWork` they would point to the same place. Our new `busy()` function can be invoked with parentheses as if that was the name we originally gave our function.

Notice how we assign `announceThatIAmDoingImportantWork` without parentheses as the value to the `busy` variable. We want to assign the value of the function itself, not the value it returns when invoked.

In JavaScript, functions are _first class objects_. This means that, like other objects you’ve encountered, JavaScript functions can have properties and methods.

Since functions are a type of object, they have properties such as `.length` and `.name` and methods such as `.toString()`. You can see more about the methods and properties of functions [in the documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function).

Functions are special because we can invoke them, but we can still treat them like any other type of data. Let’s get some practice doing that!

Initial Editor content:

	const checkThatTwoPlusTwoEqualsFourAMillionTimes = () => {
		for(let i = 1; i <= 1000000; i++) {
			if ( (2 + 2) != 4) {
				console.log('Something has gone very wrong :( ');
			}
		}
	}

	// Write your code below

To do:
1. We’ve defined a function with a very long name: `checkThatTwoPlusTwoEqualsFourAMillionTimes`. This function takes a long time to execute. It checks whether 2 + 2 = 4, but it does it a million times (just to be really sure)! Create a shorter-named variable, `is2p2` that will be easier to work with, and assign `checkThatTwoPlusTwoEqualsFourAMillionTimes` as its value.
2. Invoke your `is2p2()` function
3. Hmmm, if we forgot the original name of our function, is there a way we could figure it out? Use `is2p2` to `console.log()` the `name` property of the function we assigned to `is2p2`. Check out [the documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function) if you need a hint.

Final Editor content:

	const checkThatTwoPlusTwoEqualsFourAMillionTimes = () => {
	  for(let i = 1; i <= 1000000; i++) {
		if ( (2 + 2) != 4) {
		  console.log('Something has gone very wrong :( ');
		}
	  }
	}

	// Write your code below
	//1 assign the function to variable is2p2
	const is2p2 = checkThatTwoPlusTwoEqualsFourAMillionTimes;

	//2 Invoke/call is2p2
	is2p2();

	//3 using .name to the reassigned variable function
	console.log(is2p2.name);
	// console.log(is2p2.length);
	// console.log(is2p2.toString());

 Community Forums:
[What are other uses of functions as data?](https://discuss.codecademy.com/t/what-are-other-uses-of-functions-as-data/376842)