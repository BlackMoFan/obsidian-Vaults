Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# typeof operator
---
While writing code, it can be useful to keep track of the data types of the variables in your program. If you need to check the data type of a variable’s value, you can use the `typeof` operator.

The `typeof` operator checks the value to its right and _returns_, or passes back, a string of the data type.

	const unknown1 = 'foo';
	console.log(typeof unknown1); // Output: string
	const unknown2 = 10;
	console.log(typeof unknown2); // Output: number
	const unknown3 = true;
	console.log(typeof unknown3); // Output: boolean

Let’s break down the first example. Since the value `unknown1` is `'foo'`, a string, `typeof unknown1` will return `'string'`.

To do:
1. Use `console.log()` to print the `typeof newVariable`.
2. Great, now let’s check what happens if we reassign the variable. Below the `console.log()` statement, reassign `newVariable` to `1`.
3. Since you assigned this new value to `newVariable`, it has a new type! On the line below your reassignment, use `console.log()` to print `typeof newVariable` again.

Editor content:

	let newVariable = 'Playing around with typeof.';

	console.log(typeof newVariable);

	newVariable = 1;
	console.log(typeof newVariable);

Community Forums:
[Why is the typeof operator formatted differently from other operators?	](https://discuss.codecademy.com/t/why-is-the-typeof-operator-formatted-differently-from-other-operators/492565)