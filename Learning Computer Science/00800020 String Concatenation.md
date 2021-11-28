Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# String Concatenation
---
Operators aren’t just for numbers! When a `+` operator is used on two strings, it appends the right string to the left string:

	console.log('hi' + 'ya'); // Prints 'hiya'console.log('wo' + 'ah'); // Prints 'woah'console.log('I love to ' + 'code.')// Prints 'I love to code.'

This process of appending one string to another is called _concatenation_. Notice in the third example we had to make sure to include a space at the end of the first string. The computer will join the strings exactly, so we needed to make sure to include the space we wanted between the two strings.

	console.log('front ' + 'space'); // Prints 'front space'console.log('back' + ' space'); // Prints 'back space'console.log('no' + 'space'); // Prints 'nospace'console.log('middle' + ' ' + 'space'); // Prints 'middle space'
	
Just like with regular math, we can combine, or chain, our operations to get a final result:

	console.log('One' + ', ' + 'two' + ', ' + 'three!'); // Prints 'One, two, three!'

To do:
1. Inside a `console.log()` statement, concatenate the two strings `'Hello'` and `'World'`.
	Note: You should concatenate the two strings exactly (without introducing any additional characters).
2. We left off the space last time. Create a second `console.log()` statement in which you concatenate the strings `'Hello'` and `'World'`, but this time make sure to also include a space (`' '`) between the two words.

Editor content:

console.log('Hello' + 'World');
console.log('Hello' + ' ' + 'World');

Community Forums:
[Why would we use string concatenation?](https://discuss.codecademy.com/t/why-would-we-use-string-concatenation/489677)
[ Can a space be at the beginning or end of a string?](https://discuss.codecademy.com/t/can-a-space-be-at-the-beginning-or-end-of-a-string/489680)