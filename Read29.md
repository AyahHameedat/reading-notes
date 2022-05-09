# **Read: 29 - Room**

## **Save data in a local database using Room**  

### The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. In particular, Room provides the following benefits:

* Compile-time verification of SQL queries.
* Convenience annotations that minimize repetitive and error-prone boilerplate code.
* Streamlined database migration paths.

<br>
<br>

###  Diagram of Room library architecture:
 
 
<br>

![Diagram of Room library architecture.](https://developer.android.com/images/training/data-storage/room_architecture.png)


<br>


## Database

* he class must be annotated with a @Database annotation that includes an entities array that lists all of the data entities associated with the database.
* The class must be an abstract class that extends RoomDatabase.

# Accessing data using Room DAOs

#### By using DAOs to access your app's database instead of query builders or direct queries, you can preserve separation of concerns, a critical architectural principle. DAOs also make it easier for you to mock database access when you test your app.

### **Convenience methods**
* Insert -> @Insert
* Update -> @Update
* Delete -> @Delete
