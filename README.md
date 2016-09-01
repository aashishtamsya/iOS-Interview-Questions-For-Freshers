# iOS Interview Questions & Answers

<!---
Created by Aashish Tamsya on 01/09/16.
Copyright © 2016 Aashish Tamsya. All rights reserved.
-->

[![Platform](https://img.shields.io/badge/platform-ios-lightgrey.svg)]()
[![Programming Language](https://img.shields.io/badge/language-objective--c-ff69b4.svg)]()
[![license](https://img.shields.io/github/license/mashape/apistatus.svg?maxAge=2592000)](/LICENSE.md)

A curated list of questions and answers asked in interview for a junior iOS Developer position.


# Contents

-	[Prerequisites](#prerequisites)
-	[Interview Question and Answers](#interview-question-and-answers)	
-	[Contribution](#contribution)
-	[Credits](#credits)
-	[License](#license)

## Prerequisites

*	[Basic C/C++ Programming fundamentals](https://github.com/aashishtamsya/Assignments-For-Beginners)
*	[Programming in Objective-C](https://github.com/aashishtamsya/Objective-C-For-Beginners)
*	[How to make an iOS Application](https://github.com/aashishtamsya/iOS-Developement-For-Beginners)
*	Object Oriented Concepts


## Interview Question and Answers

<!---
Created by Aashish Tamsya on 01/09/16.
Copyright © 2016 Aashish Tamsya. All rights reserved.
-->

1.	**How would you create your own custom view?**
>	By Subclassing the UIView class.
	
2.	**What is App Bundle?**
>	When you build your iOS app, Xcode packages it as a bundle. A bundle is a directory in the  le system that groups related resources together in one place. An iOS app bundle contains the app executable  le and supporting resource  les such as app icons, image  les, and localized content.

3.	**Whats fast enumeration?**
>	Fast enumeration is a language feature that allows you to enumerate over the contents of a collection. (Your code will also run faster because the internal implementation reduces message send overhead and increases pipelining potential.)

4.	Whats a struct?
>	A struct is a special C data type that encapsulates other pieces of data into a single cohesive unit. Like an object, but built into C.

5.	Whats the difference between NSArray and NSMutableArray?
>	NSArrayʼs contents can not be modi ed once itʼs been created whereas a NSMutableArray can be modi ed as needed, i.e items can be added/removed from it.

6.	Explain retain counts.
>	Retain counts are the way in which memory is managed in Objective-C. When you create an object, it has a retain count of 1. When you send an object a retain message, its retain count is incremented by 1. When you send an object a release message, its retain count is decremented by 1. When you send an object a autorelease message, its retain count is decremented by 1 at some stage in the future. If an objectʼs retain count is reduced to 0, it is deallocated.

![Retain Count Image](/Resources/memory_management.jpg)

7.	Whats the difference between frame and bounds?
>	The frame of a view is the rectangle, expressed as a location (x,y) and size (width,height) relative to the superview it is contained within. The bounds of a view is the rectangle, expressed as a location (x,y) and size (width,height) relative to its own coordinate system (0,0).

8.	Is a delegate retained?
>	No, the delegate is never retained! Ever!

9.	Outline the class hierarchy for a UIButton until NSObject.
>	UIButton inherits from UIControl, UIControl inherits from UIView, UIView inherits from UIResponder, UIResponder inherits from the root class NSObject.

10.	What are the App states. Explain them?
>	-	**Not running State:** The app has not been launched or was running but was terminated by the system.
	
	-	**Inactive State:** The app is running in the foreground but is currently not receiving events. (It may be executing other code though.) An app usually stays in this state only brie y as it transitions to a different state. The only time it stays inactive for any period of time is when the user locks the screen or the system prompts the user to respond to some event, such as an incoming phone call or SMS message.
	-	**Active State:** The app is running in the foreground and is receiving events. This will normal mode for foreground apps.
	-	**Background State:** The app is in the background and executing code. Most apps enter this state brie y on their way to being suspended. However, an app that requests extra execution time may remain in this state for a period of time. In addition, an app being launched directly into the background enters this state instead of the inactive state. For information about how to execute code while in the background, see “Background Execution and Multitasking.”•
	-	**Suspended State:** The app is in the background but is not executing code.The system moves apps to this state automatically and does not notify them before doing so. While suspended, an app remains in memory but does not execute any code. When a low-memory condition occurs, the system may purge suspended apps without notice to make more space for the foreground app.


## Contribution

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request 😉 😊


## Credits

Aashish Tamsya [@ChiefAashish](https://www.twitter.com/chiefaashish),
aashish.tamsya@gmail.com

## License

The content of [*iOS Interview Questions & Answers*](https://github.com/aashishtamsya/iOS-Interview-Questions-For-Freshers) itself is licensed under the [Creative Commons Attribution 3.0 license](https://creativecommons.org/licenses/by/3.0/us/deed.en_US), and the underlying source code used to format and display that content is licensed under the [MIT license](https://opensource.org/licenses/mit-license.php).

See the [LICENSE](LICENSE.md) file for more info.