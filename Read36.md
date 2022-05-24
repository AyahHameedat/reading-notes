# **Read: 36 - Cognito**

### The Amplify Auth category provides an interface for authenticating a user. Behind the scenes, it provides the necessary authorization to the other Amplify categories. It comes with default, built-in support for Amazon Cognito User Pool and Identity Pool. The Amplify CLI helps you to create and configure the auth category with an authentication provider.

### **Goal**
To setup and configure your application with Amplify Auth and go through a simple api to check the current auth session



## Configure Auth Category steps:
+ amplify add auth
+ amplify push
+ add dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.35.4'
}

+ Add the Auth plugin before calling Amplify.configure. Update the code you added in Prerequisites:
```
// Add this line, to include the Auth plugin.
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
```
+ For testing purposes, you can run this from your MainActivity's onCreate method.

```

Amplify.Auth.fetchAuthSession(
    result -> Log.i("AmplifyQuickstart", result.toString()),
    error -> Log.e("AmplifyQuickstart", error.toString())
);

```
