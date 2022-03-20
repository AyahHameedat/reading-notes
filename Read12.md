# **Read: 12 - Spring RESTful Routing & Static Files**


## In this quick article, we'll focus on different kinds of Spring Data repository interfaces and their functionality. We'll touch on:

### 1- CrudRepository
### 2- PagingAndSortingRepository
### 3- JpaRepository


<br>


#### Let's start with the JpaRepository – which extends PagingAndSortingRepository and, in turn, the CrudRepository.

<br>

### Each of these defines its own functionality:

<br>

### **1- CrudRepository provides CRUD functions:-**
##### Notice the typical CRUD functionality:
+ save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch
+ findOne(…) – get a single entity based on passed primary key value
+ findAll() – get an Iterable of all available entities in database
+ count() – return the count of total entities in a table
+ delete(…) – delete an entity based on the passed object
+ exists(…) – verify if an entity exists based on the passed primary key value

<br>

### **2- PagingAndSortingRepository provides methods to do pagination and sort records**

<br>

### **3- JpaRepository provides JPA related methods such as flushing the persistence context and deleting records in a batch**

##### let's look at each of these methods in brief:

+ findAll() – get a list of all available entities in the database
+ findAll(…) – get a list of all available entities and sort them using the provided condition
+ save(…) – save an Iterable of entities. Here, we can pass multiple objects to save them in a batch
+ flush() – flush all pending tasks to the database
+ saveAndFlush(…) – save the entity and flush changes immediately
+ deleteInBatch(…) – delete an Iterable of entities. Here, we can pass multiple objects to delete them in a batch


<br>

#### **And so, because of this inheritance relationship, the JpaRepository contains the full API of CrudRepository and PagingAndSortingRepository.**
#### **When we don't need the full functionality provided by JpaRepository and PagingAndSortingRepository, we can simply use the CrudRepository.**

