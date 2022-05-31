# **Read: 38 - Notifications**
if you build a social app that can share messages or photos with the user's friends, you should support the ACTION_SEND intent. Then, when users initiate a "share" action from another app, your app appears as an option in the chooser dialog (also known as the "disambiguation dialog"), as shown in figure 1.
![](https://developer.android.com/images/training/basics/intent-chooser.png)

<br>

#### To allow other apps to start your activity in this way, you need to add an <intent-filter> element in your manifest file for the corresponding <activity> element.

  
##  Intents and Intent Filters
#### An Intent is a messaging object you can use to request an action from another app component. Although intents facilitate communication between components in several ways, there are three fundamental use cases:
+ Starting an activity
+ Starting a service
+ Delivering a broadcast

  
## Intent types
#### There are two types of intents:
+ Explicit intents specify which application will satisfy the intent, by supplying either the target app's package name or a fully-qualified component class name. You'll typically use an explicit intent to start a component in your own app, because you know the class name of the activity or service you want to start. 
+ Implicit intents do not name a specific component, but instead declare a general action to perform, which allows a component from another app to handle it.

  <br>
  <br>
  
### Explicit intents VS Implicit intents
  
  
![](https://miro.medium.com/max/800/1*Z48PAV5g7be-otNOJSZRXg.jpeg)
