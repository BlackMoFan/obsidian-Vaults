Links:  [[ccc Competitive Programmer's Handbook]]
[[00423 C++]]
# C++ in CP
---
A typical C++ code template for CP looks like this:

	#include <bits/stdc++.h>

	using namespace std;

	int main() {
		// solution comes here
	}

The `#include` line at the beginning of the code is a feature of the g++ compiler that allows us to include the entire standard library. Thus, it is not needed to separately include libraries such as iostream , vector and algorithm , but rather they are available automatically.

The `using` line declares that the classes and functions of the standard library can be used directly in the code. Without the using line we would have to write, for example, std::cout , but now it suffices to write cout. The code can be compiled using the following command:

	g++ -std=c++11 -O2 -Wall test.cpp -o test

This command produces a binary file test from the source code *test.cpp* . The compiler follows the C++11 standard ( `-std=c++11` ), optimizes the code ( `-O2` ) and shows warnings about possible errors ( `-Wall` ).