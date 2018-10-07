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

4.	**Whats a struct?**
	>	A struct is a special C data type that encapsulates other pieces of data into a single cohesive unit. Like an object, but built into C.

5.	**Whats the difference between NSArray and NSMutableArray?**
	>	NSArrayʼs contents can not be modi ed once itʼs been created whereas a NSMutableArray can be modi ed as needed, i.e items can be added/removed from it.

6.	**Explain retain counts.**
	>	Retain counts are the way in which memory is managed in Objective-C. When you create an object, it has a retain count of 1. When you send an object a retain message, its retain count is incremented by 1. When you send an object a release message, its retain count is decremented by 1. When you send an object a autorelease message, its retain count is decremented by 1 at some stage in the future. If an objectʼs retain count is reduced to 0, it is deallocated.
	>	![Retain Count Image](/Resources/memory_management.jpg)

7.	**Whats the difference between frame and bounds?**
	>	The frame of a view is the rectangle, expressed as a location (x,y) and size (width,height) relative to the superview it is contained within. The bounds of a view is the rectangle, expressed as a location (x,y) and size (width,height) relative to its own coordinate system (0,0).

8.	**Is a delegate retained?**
	>	No, the delegate is never retained! Ever!

9.	**Outline the class hierarchy for a UIButton until NSObject.**
	>	UIButton inherits from UIControl, UIControl inherits from UIView, UIView inherits from UIResponder, UIResponder inherits from the root class NSObject.

10.	**What are the App states. Explain them?**
	>	-	**Not running State:** The app has not been launched or was running but was terminated by the system.	
	>	-	**Inactive State:** The app is running in the foreground but is currently not receiving events. (It may be executing other code though.) An app usually stays in this state only brie y as it transitions to a different state. The only time it stays inactive for any period of time is when the user locks the screen or the system prompts the user to respond to some event, such as an incoming phone call or SMS message.
	>	-	**Active State:** The app is running in the foreground and is receiving events. This will normal mode for foreground apps.
	>	-	**Background State:** The app is in the background and executing code. Most apps enter this state brie y on their way to being suspended. However, an app that requests extra execution time may remain in this state for a period of time. In addition, an app being launched directly into the background enters this state instead of the inactive state. For information about how to execute code while in the background, see “Background Execution and Multitasking.”
•
	>	-	**Suspended State:** The app is in the background but is not executing code.The system moves apps to this state automatically and does not notify them before doing so. While suspended, an app remains in memory but does not execute any code. When a low-memory condition occurs, the system may purge suspended apps without notice to make more space for the foreground app.

11. **Explain how the push notification works.**
	>	![APNS Image](/Resources/apns.jpg)

12. **Explain the steps involved in submitting the App to App-Store.**
	>	![Appstore Submission Process](/Resources/appstore1.png)
	>	Apple provides the tools you need to develop, test, and submit your iOS app to the App Store. To run an app on a device, the device needs to be provisioned for development, and later provisioned for testing. You also need to provide information about your app that the App Store displays to customers and upload screenshots. Then you submit the app to Apple for approval. After the app is approved, you set a date the app should appear in the App Store as well as its price. Finally, you use Apple’s tools to monitor the sales of the app, customer reviews, and crash reports. Then you repeat the entire process again to submit updates to your app. Ref : [AppStore Review Guidelines](https://github.com/aashishtamsya/Appstore-Review-Guidelines)
	>	![Appstore Submission Process](/Resources/appstore2.png)


13. **Why do we need to use @Synthesize?**

	>	We can use generated code like `nonatomic`, `atmoic`, `retain` without writing any lines of code. We also have getter and setter methods. To use this, you have 2 other ways: `@synthesize` or `@dynamic`. 
	>	-	`@synthesize` : compiler will generate the getter and setter automatically for you. 
	>	-	`@dynamic` : you have to write them yourself.
	>	-	@property is really good for memory management, for example: `retain`. How can you do `retain` without `@property`? 

	>	```objective-c
	>	if (_variable != object)
	>	{
	>            	[_variable release];
	>		_variable = nil;
	>		_variable = [object retain];
	>	}
	>	```
	>	How can you use it with `@property` ? `self.variable = object;` When we are calling the above line, we actually call the setter like `[self setVariable: object]` and then the generated setter will do its job.


14. **Multitasking support is available from which version?**
	>	iOS 4.0.

15. **How many bytes we can send to apple push-notifcation server?**

	>	Earlier 256 bytes, as of now (from iOS 9 onwards) it has been increased to 2 MB.

16. **What is code signing?**

	>	Signing an application allows the system to identify who signed the application and to verify that the application has not been modi ed since it was signed. Signing is a requirement for submitting to the App Store (both for iOS and Mac apps). OS X and iOS verify the signature of applications downloaded from the App Store to ensure that they they do not run applications with invalid signatures. This lets users trust that the application was signed by an Apple source and hasn’t been modi ed since it was signed.

	>	Xcode uses your digital identity to sign your application during the build process. This digital identity consists of a public-private key pair and a certi cate. The private key is used by cryptographic functions to generate the signature. The certi cate is issued by Apple; it contains the public key and identi es you as the owner of the key pair.

	>	In order to sign applications, you must have both parts of your digital identity installed. Use Xcode or Keychain Access to manage your digital identities. Depending on your role in your development team, you may have multiple digital identities for use in different contexts. For example, the identity you use for signing during development is different from the identity you user for distribution on the App Store. Different digital identities are also used for development on OS X and on iOS.

	>	An application’s executable code is protected by its signature because the signature becomes invalid if any of the executable code in the application bundle changes. Resources such as images and nib  les are not signed; a change to these  les does not invalidate the signature.

	>	An application’s signature can be removed, and the application can be re-signed using another digital identity. For example, Apple re-signs all applications sold on the App Store. Also, a fully- tested development build of your application can be re-signed for submission to the App Store. Thus the signature is best understood not as indelible proof of the application’s origins but as a variable mark placed by the signer.

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
