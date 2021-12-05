Links:  [[008000 Full-Stack Engineer Path from Codecademy]]
# Ternary Operator
---
In the spirit of using short-hand syntax, we can use a _ternary operator_ to simplify an `if...else` statement.

Take a look at the `if...else` statement example:

```
let isNightTime = true;

if (isNightTime) {
	console.log('Turn on the lights!');
} else {
	console.log('Turn off the lights!');
}
```

We can use a _ternary operator_ to perform the same functionality:

```
isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
```

In the example above:

-   The condition, `isNightTime`, is provided before the `?`.
-   Two expressions follow the `?` and are separated by a colon `:`.
-   If the condition evaluates to `true`, the first expression executes.
-   If the condition evaluates to `false`, the second expression executes.

Like `if...else` statements, ternary operators can be used for conditions which evaluate to `true` or `false`.

To do:
1. Refactor, or edit, the first `if...else` block to use a ternary operator.
2. Refactor the second `if...else` block to use a ternary operator.
3. Refactor the third `if...else` block to use a ternary operator.

Editor content:

	let isLocked = false;

	// if (isLocked) {
	//   console.log('You will need a key to open the door.');
	// } else {
	//   console.log('You will not need a key to open the door.');
	// }

	isLocked ? console.log('You will need a key to open the door.') : console.log('You will not need a key to open the door.');

	let isCorrect = true;

	// if (isCorrect) {
	//   console.log('Correct!');
	// } else {
	//   console.log('Incorrect!');
	// }

	isCorrect ? console.log('Correct!') : console.log('Incorrect!');
	let favoritePhrase = 'Love That!';

	// if (favoritePhrase === 'Love That!') {
	//   console.log('I love that!');
	// } else {
	//   console.log("I don't love that!");
	// }

	favoritePhrase === 'Love That!' ? console.log('I love that!') : console.log("I don't love that!");

Community Forums:
[Why is favorite_Phase === 'Love That!' required?](https://discuss.codecademy.com/t/why-is-favorite-phase-love-that-required/428482)
[Can ternary operators contain multiple actions?](https://discuss.codecademy.com/t/can-ternary-operators-contain-multiple-actions/428487)
[If ternary operators are the same as if/else, why use them at all?](https://discuss.codecademy.com/t/if-ternary-operators-are-the-same-as-if-else-why-use-them-at-all/428491)