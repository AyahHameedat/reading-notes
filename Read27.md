# Read: 27 - Intents, Activities, and SharedPreferences

### When doing a job, users engage with a task, which is a set of actions. The activities are stacked in the order in which they are opened in a stack called the back stack. 
![](https://media.geeksforgeeks.org/wp-content/uploads/20210612202233/article-660x339.png)

### Back press behavior for root launcher activities
#### Root launcher activities are activities that declare an Intent filter with both ACTION_MAIN and CATEGORY_LAUNCHER. These activities are unique because they act as entry points into your app from the app launcher and are used to start a task.

# Background and foreground tasks

#### A task is a cohesive unit that can move to the background when a user begins a new task or goes to the Home screen. While in the background, all the activities in the task are stopped, but the back stack for the task remains intact—the task has simply lost focus while another task takes place, as shown in figure
![](https://developer.android.com/images/fundamentals/diagram_multitasking.png)
##### Figure. Two tasks: Task B receives user interaction in the foreground, while Task A is in the background, waiting to be resumed.

* Activities can be instantiated multiple times, even from other tasks.


# Save key-value data
### A SharedPreferences object points to a file containing key-value pairs and provides simple methods to read and write them. Each SharedPreferences file is managed by the framework and can be private or shared.

#### You can create a new shared preference file or access an existing one by calling one of these methods:
* getSharedPreferences() — Use this if you need multiple shared preference files identified by name, which you specify with the first parameter. You can call this from any Context in your app.
* getPreferences() — Use this from an Activity if you need to use only one shared preference file for the activity. Because this retrieves a default shared preference file that belongs to the activity, you don't need to supply a name.

