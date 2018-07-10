# iOS-12-Notifications-with-Custom-UI
An Xcode 10 **beta** 2 project, written in Swift 4.2, demonstrating how to create an iOS 12 **beta** 2 extension to add a custom user interface to local and push notifications.

In this repo's [corresponding tutorial](http://iosbrain.com/blog/2018/07/10/new-in-ios-12-adding-a-custom-ui-and-interactivity-inside-local-and-push-notifications/), I'm going to show you how to give your local and remote (push) notifications <em>a custom user interface (UI)</em>. Users can now <em>interact</em> with a notification's content area. iOS 12 has given us the ability to add a <code>UIViewController</code> subclass to notifications which we can customize. We can add controls like <code>UIButton</code>, <code>UIImageView</code>, and <code>UISwitch</code> to the view controller, wire up custom functionality using <code>IBOutlet</code> and <code>IBAction</code>, and arrange our custom UI using Auto Layout -- all within the notification itself. We can provide support for more than a single tap. We can develop pretty much any type of user experience we want, within notification space limitations and timing considerations.

I'll show you how a user can take action in response to a notification by interacting <em>only</em> with a customized notification interface, and conveniently <em>not</em> having to open up an app. I'll be showcasing software released to developers just ten days ago (June 19), specifically iOS 12 beta 2 and Xcode 10 beta 2.

By the end of this tutorial, you'll be able allow to your app users to get a notification, see a custom UI, click on a button, and get a confirmation. [Continue reading...](http://iosbrain.com/blog/2018/07/10/new-in-ios-12-adding-a-custom-ui-and-interactivity-inside-local-and-push-notifications/)

## Xcode 10 beta 2 project settings
**To get this project running on the Simulator or a physical device (iPhone, iPad)**, go to the following locations in Xcode and make the suggested changes:

1. Project Navigator -> [Project Name] -> Targets List -> TARGETS -> [Target Name] -> General -> Signing
- [ ] Tick the "Automatically manage signing" box
- [ ] Select a valid name from the "Team" dropdown
  
2. Project Navigator -> [Project Name] -> Targets List -> TARGETS -> [Target Name] -> General -> Identity
- [ ] Change the "com.yourDomainNameHere" portion of the value in the "Bundle Identifier" text field to your real reverse domain name (i.e., "com.yourRealDomainName.Project-Name").
