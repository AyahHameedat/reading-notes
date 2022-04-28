# **Read26: Application Fundamentals**

### Android apps can be written using Kotlin, Java, and C++ languages. The Android SDK tools compile your code along with any data and resource files into an APK or an Android App Bundle.

### An Android App Bundle, which is an archive file with an .aab suffix, contains the contents of an Android app project including some additional metadata that is not required at runtime. 

### - The Android operating system is a multi-user Linux system in which each app is a different user.
### - Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.

# App components:
* Activities: An activity is the entry point for interacting with the user. It represents a single screen with a user interface.
* Services: A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. A service does not provide a user interface. 
* Broadcast receivers: A broadcast receiver is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements.
A broadcast receiver is implemented as a subclass of BroadcastReceiver and each broadcast is delivered as an **Intent** object. 
* Content providers: A content provider manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access. 


# The manifest file
### Before the Android system can start an app component, the system must know that the component exists by reading the app's manifest file, AndroidManifest.xml. Your app must declare all its components in this file, which must be at the root of the app project directory.


# Declaring components
### The primary task of the manifest is to inform the system about the app's components. For example, a manifest file can declare an activity as follows:

```
<?xml version="1.0" encoding="utf-8"?>
<manifest ... >
    <application android:icon="@drawable/app_icon.png" ... >
        <activity android:name="com.example.project.ExampleActivity"
                  android:label="@string/example_label" ... >
        </activity>
        ...
    </application>
</manifest>

```

