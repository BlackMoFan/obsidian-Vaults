Links:  [[008111 Create a Front-End App with React from Codecademy]]
# Introduction to Iterators

---
Imagine you had a grocery list and you wanted to know what each item on the list was. You’d have to scan through each row and check for the item. This common task is similar to what we have to do when we want to iterate over, or loop through, an array. One tool at our disposal is the `for` loop. However, we also have access to built-in array methods which make looping easier.

The built-in JavaScript array methods that help us iterate are called _iteration methods_, at times referred to as _iterators_. Iterators are methods called on arrays to manipulate elements and return values.

In this lesson, you will learn the syntax for these methods, their return values, how to use the documentation to understand them, and how to choose the right iterator method for a given task.

Initial Editor content:

	const artists = ['Picasso', 'Kahlo', 'Matisse', 'Utamaro'];

	artists.forEach(artist => {
	  console.log(artist + ' is one of my favorite artists.');
	});

	const numbers = [1, 2, 3, 4, 5];

	const squareNumbers = numbers.map(number => {
	  return number * number;
	});

	console.log(squareNumbers);

	const things = ['desk', 'chair', 5, 'backpack', 3.14, 100];

	const onlyNumbers = things.filter(thing => {
	  return typeof thing === 'number';
	});

	console.log(onlyNumbers);

To do:
1. Inspect the code in **main.js**. Notice the different methods being called on the arrays:

	-   `.forEach()`
	-   `.map()`
	-   `.filter()`

	Run the code to see the output!