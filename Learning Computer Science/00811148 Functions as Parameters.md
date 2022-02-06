Links:  [[008111 Create a Front-End App with React from Codecademy]]
# Functions as Parameters

---
Since functions can behave like any other type of data in JavaScript, it might not surprise you to learn that we can also pass functions (into other functions) as parameters. A _higher-order function_ is a function that either accepts functions as parameters, returns a function, or both! We call the functions that get passed in as parameters and invoked _callback functions_ because they get called during the execution of the higher-order function.

When we pass a function in as an argument to another function, we don’t invoke it. Invoking the function would evaluate to the return value of that function call. With callbacks, we pass in the function itself by typing the function name _without_ the parentheses (that would evaluate to the result of calling the function):

	const timeFuncRuntime = funcParameter => {  
		let t1 = Date.now();  
		funcParameter();  
		let t2 = Date.now();  
		return t2 - t1;  
	}  

	const addOneToOne = () => 1 + 1;  

	timeFuncRuntime(addOneToOne);

We wrote a higher-order function, `timeFuncRuntime()`. It takes in a function as an argument, saves a starting time, invokes the callback function, records the time after the function was called, and returns the time the function took to run by subtracting the starting time from the ending time.

This higher-order function could be used with any callback function which makes it a potentially powerful piece of code.

We then invoked `timeFuncRuntime()` first with the `addOneToOne()` function - note how we passed in `addOneToOne` and did not invoke it.

	timeFuncRuntime(() => {  
		for (let i = 10; i>0; i--){  
			console.log(i);  
		}  
	});

In this example, we invoked `timeFuncRuntime()` with an anonymous function that counts backwards from 10. Anonymous functions can be arguments too!

Let’s get some practice using functions and writing higher-order functions.

Initial Editor content:

	const checkThatTwoPlusTwoEqualsFourAMillionTimes = () => {
	  for(let i = 1; i <= 1000000; i++) {
		if ( (2 + 2) != 4) {
		  console.log('Something has gone very wrong :( ');
		}
	  }
	};

	const addTwo = num => num + 2;

	const timeFuncRuntime = funcParameter => {
	  let t1 = Date.now();
	  funcParameter();
	  let t2 = Date.now();
	  return t2 - t1;
	};

	// Write your code below

To do:
1. Save a variable, `time2p2`. Assign as its value the result of invoking the `timeFuncRuntime()` function with the `checkThatTwoPlusTwoEqualsFourAMillionTimes()` function.
2. Write a higher-order function, `checkConsistentOutput()`. This function should have two parameters: a function and a value. It should call the argument function with the value two times. If the callback function produces the same result twice, it should return the result of the function call, otherwise, it should return the string `'This function returned inconsistent results'`
3. Invoke your `checkConsistentOutput()` with the `addTwo()` function we wrote and a number as arguments.

Final Editor content:

	const checkThatTwoPlusTwoEqualsFourAMillionTimes = () => {
	  for(let i = 1; i <= 1000000; i++) {
		if ( (2 + 2) != 4) {
		  console.log('Something has gone very wrong :( ');
		}
	  }
	};

	const addTwo = num => num + 2;

	const timeFuncRuntime = funcParameter => {
	  let t1 = Date.now();
	  funcParameter();
	  let t2 = Date.now();
	  return t2 - t1;
	};

	// Write your code below
	//1 pass in the first function to timeFuncRuntime
	let time2p2 = timeFuncRuntime(checkThatTwoPlusTwoEqualsFourAMillionTimes);

	//2 create function
	const checkConsistentOutput = (func, value) => {
	  let firstResult = func(value), secondResult = func(value);
	  if(firstResult === secondResult){
		return firstResult;
	  }
	  return 'This function returned inconsistent results';
	}

	//3 invoke created function
	// checkConsistentOutput(addTwo, 23);
	console.log(checkConsistentOutput(addTwo, 23));
	
Community Forums:
[When should we use callbacks vs directly calling a function?](https://discuss.codecademy.com/t/when-should-we-use-callbacks-vs-directly-calling-a-function/376857)
[Why does the exercise say not to invoke the function when it’s called as an argument?](https://discuss.codecademy.com/t/crossing-wires-somewhere-with-callbacks-and-hof-s/395283)
[Better understanding higher order functions - helpful resources](https://discuss.codecademy.com/t/better-understanding-higher-order-functions-helpful-resources/395377)