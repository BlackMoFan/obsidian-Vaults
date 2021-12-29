Links:  [[000 Index]]
# Competitive Programmer's Handbook
By Antti Laaksonen, _July 3, 2018_

---
### Keypoints


---
### General Info
- CP combines two topics:  (1) the design of algorithms and (2) the implementation of algorithms
	-	**design of algorithms** consists of problem solving and mathematical thinking.  Skills for analyzing problems and solving them creatively are needed.  An algorithm for solving a problem has to be both correct and efficient, and the core of the problem is often about inventing an efficent algorithm.  Theoretical knowledge of algorithms is important to competitive programmers.  Typically, a solution to a problem is a combination of well-known techniques and new insights.  The techniques that appear in CP also form the basis for the scientific research of algorithms.
	-	**implementation of algorithms** requires good programming skills.  In CP, the solutions are graded by testing an implemented algorithm using a set of test cases.  Thus, it is not enought that the idea of the algorithm is correct, but the implementation also has to be correct.  A good coding style in contest is straightforward and concise.  Programs should be written quickly , because there is not much time available.  Unlike in traditional software engineering, the programs are short (usually at most a few hundred lines of code), and they do not need to be maintained after the contest.

---
### Programming languages in CP
- at the moment, the most popular programming languages used in contests are C++, Python, and Java.
- Many people think that C++ is the best choice for a competitive programmer, and C++ is nearly always available in contest sytems.  The benefits of using C++ are that it is a very efficient language and its standard library contains a large collection of data structures and algorithms.  On the other hand, it is good to master several languages and understand their strengths.  For example, if large integers are needed in the problem, Python can be a good choice, because it contains built-in operations for calculating with large integers.  Still, most problems in programming contests are set so that using a specific programming language is not an unfair advantage.

C++ in CP [[cccaaa C++ in CP]]

---
### Input and output
- In most contests, standard streams are used for reading input and writing output.  In C++, the standard streams are `cin` for input and `cout` for output. In addition, the C functions `scanf` and `printf` can be used.
- The input for the program usually consists of numbers and strings that are separated with spaces and newlines. They can be read from the cin stream as follows:

		int a, b;
		string x;
		cin >> a >> b >> x;
- This kind of code always works, assuming that there is at least one space or newline between each element in the input. For example, the above code can read both of the following inputs:

	```
	123 456 monkey
	```
	```
	123		456
	monkey
	```

	The cout stream is used for output as follows:

	```
	int a = 123, b = 456;
	string x = "monkey";
	cout << a << " " << b << " " << x << "\n";
	```

>Note that the newline "\n" works faster than endl , because endl always causes a flush operation.

- The C functions scanf and printf are an alternative to the C++ standard streams. They are usually a bit faster, but they are also more difficult to use. The following code reads two integers from the input:
	```
	int a, b;
	scanf("%d %d", &a, &b);
	```
	The following code prints two integers:
	```
	int a = 123, b = 456;
	printf("%d %d\n", a, b);
	```