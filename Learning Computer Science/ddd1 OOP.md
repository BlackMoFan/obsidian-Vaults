Links:  [[ddd terminologies and explanations]]
# OOP

---
[source](https://www.quora.com/How-is-object-oriented-programming-useful) - by Michael Bryant, 

Consider for a moment that you are keeping track of ten people. We need to keep track of their name, age, weight, height, current occupation, spouse (if any), home address, and the kind of car they drive. Okay? Without objects we get code that looks something like this (Java used as an example):

	String name1; 
	String name2; 
	String name3; 
	String name4; 
	String name5; 
	String name6; 
	String name7; 
	String name8; 
	String name9; 
	String name10; 
	int age1; 
	int age2; 
	int age3; 
	int age4; 
	int age5; 
	int age6; 
	int age7; 
	int age8; 
	int age9; 
	int age10; 
	double weight1; 
	double weight2; 
	double weight3; 
	double weight4; 
	double weight5; 
	double weight6; 
	double weight7; 
	double weight8; 
	double weight9; 
	double weight10; 
	double height1; 
	double height2; 
	double height3; 
	double height4; 
	double height5; 
	double height6; 
	double height7; 
	double height8; 
	double height9; 
	double height10; 
	/* And so on... */

I only did four of the eight things I said we need to keep track of. Now this looks ridiculous and it is. Technically we can shorten it by declaring all variables of the same type on one line like so:

	String name1, name2, name3, name4, name5, name6, name7, name8, name9, name10; 
	int age1, age2, age3, age4, age5, age6, age7, age8, age9, age10; 
	double weight1, weight2, weight3, weight4, weight5, weight6, weight7, weight8, weight9, weight10, height1, height2, height3, height4, height5, height6, height7, height8, height9, height10; 
	/* And so on... */
	
That’s more readable, but still ugly, and we can’t initialize them all with different values like we could in the first, long, example.

So we get a little smarter. We use arrays. Let’s even create a variable for the number of people we are keeping track of.

	int NUM_PEOPLE = 10; 
	String[] names = new String[NUM_PEOPLE]; 
	int[] ages = new int[NUM_PEOPLE]; 
	double[] weight = new double[NUM_PEOPLE]; 
	double height[NUM_PEOPLE]; 
	/* And so on... */

This works, but it’s ugly. And think about if we want to pass one of these people to a function so that we can access their data:

	public static void useData(String name, int age, double weight, double height...){}

What if we want to modify mutiple pieces of data in the person in our function? We’d have to pass all of the arrays in plus the index of that person in each array.

And what about that spouse? Let’s get rid of any potential mutual dependency and say these are all men and “spouse” now reads “wife”. If we want to access her information, how are we going to do that? Is there another set of arrays that we need to look up data from? Do we store her index in the “wives” array at the index for her husband?

You can see at this point that everything is needlessly complex and confusing. This is readily fixed with objects:

	Person[] people = new Person[10]; // Person array 
	// Elsewhere we have created a Person object named susan 
	Person bob = new Person("Bob", 35, 170.4, 5.9, "Lumberjack", susan, "1234 Address Way NE", "Chevy Silverado something or other"); 
	people[0] = bob;

We now have an easy way of creating a new person and keeping track of all of their information in one place. We have one array that stores Person objects and each Person holds all of their own data. Now when we want to use someone’s data, it’s merely a matter of passing in a Person object:

	public static void useData(Person person){ /* Do stuff here */ }

We can even create a new Person and return it as the result of a function:

	public static Person makeBaby(Person mother, Person father){ 
	/* Use mommy and daddy's information to make baby */ 
	}

Really, I don’t understand what you mean by making things more complex. True you are making your own data type by making object classes, but in the end it makes things much simpler by keeping related information together in a unit that can be referenced much easier than each of the contained data can be while keeping them all together.