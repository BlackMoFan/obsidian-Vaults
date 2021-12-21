Links:  [[008 Web development]]  [[0042 Programming languages]]
(Use 0083)  - for Flutter links
# Flutter
from *Practical Flutter:  Improve your Mobile Development with Google's Latest Open-Source SDK* by Frank Zammeti

---
## Keypoints on Flutter
- Flutter can be conceptualized as being comprised of:  **Dart platform**, **Flutter engine**, **Foundation library**, and **Widgets** (more info about each below)
- Flutter is a platform where you can write a single code base that can work in both Android and iOS

---
### General Information on Flutter:  An Introduction
- Flutter is **created by Google**.  Began its life under the name "Sky" in 2015 at the Dart Developer Summit
- Flutter is a platform that provides a means for you to write a single code base (more or less) that **works on Android and iOS equally well** while delivering native performance and native capabilities
- Various preview versions of Flutter were released subsequent to its initial announcement, culminating in the **December 4th, 2018, release of Flutter 1.0, the first “stable” release.**
	- One of the original stated goal of Flutter, or at least one of the main ones, was **being able to render app UIs at a consistent 120fps** no matter what. Google very much understands that a consistently smooth UI is one that users will be delighted by and want to use, so it was at the forefront of their thinking with Flutter.
- One of the key decisions Google made when designing Flutter is something that differentiates it from most other mobile development options, and that’s the fact that **Flutter renders its own UI components.** Unlike most other frameworks, Flutter does not use native platform components. In other words, when you tell Flutter to display a button, for example, Flutter itself renders that button, it’s not just asking the underlying OS to render the button, which is what most other frameworks do. This represents a big difference between Flutter and nearly anything else out there and is primarily what allows Flutter apps to be consistent across platforms.
- Flutter provides design-specific widgets. What this means is that Flutter offers two sets of widgets: **Material design widgets and Cupertino design widgets.** The former implement Google’s own Material design language, which is the default design language for Android. The latter implements Apple’s iOS design language.

##### Under the covers, Flutter can be conceptualized as being comprised of four main parts:
1. `Dart platform`
2. `Flutter engine` - This is a (mostly) C++-based codebase, so performance is near-native levels at the core, and this codebase uses the Skia graphics engine to do its rendering. Skia is a compact, open-source graphics library, also written in C++, that has evolved to have excellent performance across all supported platforms.
3. `Foundation library` - an interface over the native SDKs of both platforms (Android and iOS).  This library has the goal of obviating the differences between the APIs of the native platforms in favor of a Flutter-supplied API that is consistent. In other words, you don’t need to worry about how to launch the camera app on iOS vs. how you launch it on Android, you don’t need to think about what API to use on one platform vs. another. You merely need to know the Flutter API call to make to launch the camera app, and it’ll work on both platforms.
4. `Widgets`

---
### A Decent Introduction to Dart (its relevance to Flutter)
[[00831 Dart]]

Google decided to go with a language that they themselves had created to create Flutter -- Dart

### General Information about Dart
- Google created Dart back in 2011, and it was initially unveiled at the GOTO conference in Aarhus, Denmark. The initial 1.0 release took place in November 2013, roughly two years before Flutter was released. You have Lars Bak (also the developer of the V8 JavaScript engine underpinning chrome and Node.js) and Kasper Lund to thank for Dart.
- Dart is:
	- Dart is fully object-oriented.
	- It's a garbage-collected language, so no memory allocation/deallocation worries.
	- It has a C-based syntax style that is easy for most developers to pick up.
	- Supports common language features like interfaces, mixins, abstract classes, reified generics, and static typing.
	- A sound typing system (but with flexibility around typing at the same type that makes it not a burden but a genuine help for developers).
	- Isolates for concurrency so that you can have independent workers that do not share memory but instead use message passing for communication, yielding good performance while reducing the risk typically associated with other forms of concurrent programming paradigms.
	- Dart can use ahead-of-time compilation to native code in order to reach the highest levels of performance this side of Assembly. It compiles to ARM and x86 code, but it can also transpile to JavaScript so your Dart code can run, after a fashion, on the web even. Putting aside that transpilation (is that even a word?!), with Flutter targetting a mobile platform, you’ll wind up with AOT-compiled Dart code.
	- Dart supports a rather large package repository that provides additional functionality on top of the core language for virtually anything most developers would need and makes it easy to bring those packages to bear in your projects.
	- Tooling support from a lot of popular developer tools including Visual Studio Code and IntelliJ IDEA.
	- Snapshots as a core part of the Dart VM, which are a method to store and serialize objects and data at runtime (Dart programs can be compiled to snapshots, which contain all the program code and dependencies pre-parsed and ready to execute at startup, and snapshots are also used heavily in the use of isolates).

---
### Glimpse on Widgets
- >In Flutter, everything is a widget. When I say everything is a widget, I mean... well, I mean that almost everything is a widget (it’s far harder to find something that isn’t a widget in Flutter than to find all the things that are!).
- >And what's a widget, you ask? Well, they are chunks of your UI (though it’s true that not all widgets manifest on the screen, though that’s rare). A widget is also, obviously, a chunk of code, like so:
```
Text("Hello!")
```
...and this is also a widget...

```
RaisedButton(
  onPress : function() {
    // Do something.
  },
  child : Text("Click me!")
)
```
...this, too, is a widget...

```
ListView.builder(
  itemCount : cars.length,
  itemBuilder : (inContext, inNum) {
    return new CarDescriptionCard(card[inNum]);
  }
)
```
...and finally, this is also a widget:

```
Center(
  child : Container(
    child : Row(
      Text("Child 1"),
      Text("Child 2"),
      RaisedButton(
        onPress : function() {
          // Do something.
        },
        child : Text("Click me")
      )
    )
  )
)
```
This last one is interesting because it’s actually a hierarchy of widgets: a Center widget, with a Container widget underneath it, and that Container widget with a Row widget underneath it, and two Text children under the Row plus a RaisedButton too. It’s not important what those widgets are (though the names pretty much give them away) but what is important is that the entire hierarchy of widgets you see there is itself considered a widget in the realm of Flutter.


- There are the obvious things, the things that people think of when you say the word widget in the context of a user interface: buttons, lists, images, text form fields, all that sort of stuff. Those are widgets for sure. But, in Flutter, things that you don’t typically think of widgets are still widgets, stuff like the padding around an image, the state of a text form field, the text displayed on the screen, even the theme an app is using, all of those are widgets in Flutter too.
- Given that everything is a widget, a natural consequence is that in Flutter, your code, to a substantial degree, turns out to be nothing but a giant hierarchy of widgets (and this hierarchy has a particular name in Flutter: the “widget tree”). You see, most widgets are containers, meaning they can have children. Some widgets can have but a single child while others can have many. And then, those children can each have one or more children, and so on and so on – its widgets all the way down!
- All widgets are Dart classes
- >Widgets typically have only a single requirement which is they must supply a build() method.  This method must return… wait for it… *other widgets! * There are a very few exceptions to this, some low-level widgets like the Text widget, which returns a primitive type (a String in this case), but most return one or more widgets. Aside from this requirement, at a code level, a widget is just a plain old Dart class (which isn’t any different, minor syntax aside as the next chapter will show, from a class you’ve seen in any other object-oriented language).
- A Flutter widget extends one of a handful of standard classes, classes which Flutter itself provides.  The class extended determines what kind of widget we're dealing with at fundamental level.
	- There are two that you'll use probably 99% of the time: 
		
		** StatelessWidget ** and ** StatefulWidget **
		- A widget that extends *StatelessWidget* never changes and is called a stateless widget because it has no state.  Things like Icon widgets, which display small images, and Text widgets, which of course display strings of text, are said to be stateless widgets.  An example of such a class might be this:
	
				class MyTextWidget extends StatelessWidget {
					Widget build(inContext){
						return new Text("Hello!");
					}
				}
		- By contrast, the *StatefulWidget* base class has the notion of state in it, i.e. it changes in some way when the user interacts with it.  A CheckBox, a Slider, a TextField, these are all well-known examples of stateful widgets (and when you see them written with this sort of capitalization going forward it means that I’m referring to actual Flutter widget class names, not generic fields like a text form field, by contrast)
		- When you code such a widget, you actually have to create two classes: the stateful widget class itself, and a state class to go along with it. Here’s an example of a stateful widget and its associated state class:
		
				class LikesWidget extends StatefulWidget {
					@override
					LikesWidgetState createState() => LikesWidgetState();
				}
				
				class LikesWidgetState extends State<LikesWidget> {
					int likeCount = 0;
					
					void like() {
						setState(() {
							likeCount += 1;
						});
					}
					
					@override
					Widget build(BuildContext inContext) {
						return Row(
							children: [
								RaisedButton(
									onPressed : like,
									child : Text('$likeCount')
								)
							]	
						);
					}
				}
				
	- It should be noted that the term "stateless" is a little bit of a misnomer (|*n*|.  a name that is wrong or not proper or appropriate) here because being Dart classes, which can have properties and data encapsulated in them, stateless widgets do, in a sense, have state.
		- 