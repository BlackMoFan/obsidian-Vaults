Links:  [[008 Web development]]
# Angular
---
[from here](https://lms.simplilearn.com/courses/4329/Full-Stack-Development-for-Beginners/syllabus)

Content:

- *Why Angular?*
- *What is Angular?*
- *Features of Angular*
- *Angular Architecture*
- *Advantages of Angular*
- *Limitations of Angular*
- *Angular Learning Curve*
- *Companies Using Angular*
---
- *Why Angular?*

---
- *What is Angular?*
	-	Angular is an open-source, JavaScript framework, written completely in TypeScript.  It is designed for web, desktop, and mobile platforms
	-	Primarily aimed to develop Single Page Applications (SPAs)
	-	Uses HTML's syntax to express your application's components clearly
	-	Maintained by Google

---
- *Features of Angular*
	- Document Object Model (DOM)
		- Treats an XML or HTML document as a tree structure in which each node is an object representing a part of the document
		- Angular uses regular DOM.  This will update the entire tree structure of HTML tags until it reaches the data to be updated.
			- ```
			Consider about 100s of updates on the same HTML page and the HTML block is replaced for each request.```
	- TypeScript
		- Angular is written in TypeScript.  It is a superset of JavaScript and offers excellent consistency.
		- TypeScript is installed as an NPM package, and thus can be installed with the following command:
		- `npm install -g typescript`
	- Data binding
		- Data binding allows an Internet user to manipulate Web page elements using a Web browser.  It is used for Web pages that contain interactive components such as forms, calculators, tutorials, and games.
		- Angular uses two-way binding.  (any changes made in the UI element is reflected in the corresponding model state.  And vice versa)
	- Testing
		- Angular uses Jasmine to run various tests
		- The Jasmine framework allows various functionalities to write different kinds of test cases
		- Karma is the task-runner for the tests

---
- *Angular Architecture*
	- Angular is a full-fledged MVC (Model-View-Controller) framework.
	- MVC is an architectural pattern that separates the application layer into Model, View, and Controller
		- Model - relates to all data-related logic
		- View - UI logic of the application
		- Controller - brain of the setup.  Interface between Model and View

---
- *Advantages of Angular*
	- Custom components - allows to build your own components
	- Data binding
	- Dependency injection
	- Testing
	- Comprehensive
	- Browser compatibility

	Releases of Angular
	- **Angular 1**:  Built on JavaScript and completely based on controllers
	- **Angular 2**:  Incorporated the component-based approach
	- **Angular 4**:  Included router updation.  Angular CLI 1.0 was introduced
	- **Angular 5, 6**:  Angular CLI was optimized and the commands ng-update and ng-add were added
	- **Angular 7**:  Prompts were introduced which provide tips in CLI about the functions.
	- **Angular 8**:  Ivy renderer and Bazel were introduced
	- **Angular 9**:  Came with better framework and Angular material.  Included full switch to **the Ivy renderer** as a default compiler.

---
- *Limitations of Angular*
	- Steep learning curve
	- Limited SEO (Search Engine Optimization) options
	- Verbose and complex
	- Migration - difficult to code legacy code to Angular style architecture

---
- *Angular Learning Curve*

	Basic topics in Angular to be learnt are:
	
	- Directives
	- Modules
	- Decorators
	- Components
	- Services
	- Dependency injection
	- Pipes and Templates

	Advanced topics include:
	- Change detection
	- Zones
	- AoT compilation
	- Rx.js

	However, the learning curve is clear-cut (sharply defined; easy to perceive or understand) with Angular development

---
- *Companies Using Angular*
	- Nike
	- Forbes
	- Google
	- Upwork
	- HBO
	- Sony
	- General Motors

---
- *Angular Prerequisites*
	- **NodeJS**:  Angular uses Node.js as its base for a large part of its build environment
	- **Angular CLI**:  Angular team has created a command-line interface (CLI) tool to make it easier to bootstrap and develop Angular applications
		- ```
		In the terminal:
		Installation
			npm install -g @angular/cli
		Confirmation: 
			ng --version
			```
	- **Text Editor**:  Visual Studio Code is a powerful source code editor that is available on Windows, MacOS, and Linux platforms