Links:  [[008111 Create a Front-End App with React from Codecademy]]
# Secret Message

---
Using array methods, you will transform an array of strings into a secret message!

You should consult the [Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) for reference on any method with which you are not familiar.

If you get stuck during this project or would like to see an experienced developer work through it, click “**Get Unstuck**“ to see a **project walkthrough video**.

Initial Editor content:

	let secretMessage = ['Learning', 'is', 'not', 'about', 'what', 'you', 'get', 'easily', 'the', 'first', 'time,', 'it', 'is', 'about', 'what', 'you', 'can', 'figure', 'out.', '-2015,', 'Chris', 'Pine,', 'Learn', 'JavaScript'];

To do:
1. Use an array method to remove the last string of the array `secretMessage`.
2. Great! You can check your work by logging the `.length` of the array.
	
	At this point, the length should be 1 less than the original length.

3. Use an array method to add the words `to` and `Program` as separate strings to the end of the `secretMessage` array.
4. Change the word `easily` to the word `right` by accessing the index and replacing it.
5. Use an array method to remove the first string of the array.
6. Use an array method to add the string `Programming` to the beginning of the array.
7. Use an array method to remove the strings `get`, `right`, `the`, `first`, `time,`, and replace them with the single string `know,`.
8. On one line, use `console.log()` and `.join()` to print the secret message as a sentence.

Final Editor content:

	let secretMessage = ['Learning', 'is', 'not', 'about', 'what', 'you', 'get', 'easily', 'the', 'first', 'time,', 'it', 'is', 'about', 'what', 'you', 'can', 'figure', 'out.', '-2015,', 'Chris', 'Pine,', 'Learn', 'JavaScript'];
	
	//check initial length
	console.log(secretMessage.length);

	//1. removing last string in the array
	secretMessage.pop();
	//2. checking the resulting array length after removal. should be 1 less
	console.log(secretMessage.length);

	//3. pushing/adding two separate strings
	secretMessage.push('to', 'Program');

	//4. changing 'easily' to 'right'. index 7
	secretMessage[7] = 'right';

	//5. remove first string by using .shift
	secretMessage.shift();

	//6. add string 'Programming' to the beginning of array using .unshift
	secretMessage.unshift('Programming');

	//7. remove 5 contiguous elements from index 6 using splice
	//then replace with single string 'know'
	secretMessage.splice(6, 5, 'know,');

	// check array content
	console.log(secretMessage);

	//print the array content as a sentence
	console.log(secretMessage.join(' '));