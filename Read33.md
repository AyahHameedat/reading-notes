# **Read: 33 - GraphQL @connection**

### The @hasOne and @hasMany directives do not support referencing a model which then references the initial model via @hasOne or @hasMany if DataStore is enabled.

How to create a one-directional one-to-many relationship between two models using the @hasMany directive:

```
type Post @model {
  id: ID!
  title: String!
  comments: [Comment] @hasMany
}

type Comment @model {
  id: ID!
  content: String!
}
```

### This generates queries and mutations that allow you to retrieve the related Comment records from the source Post record.

![](https://d33wubrfki0l68.cloudfront.net/ec285142a9a2373c8507849655fc0a6b03f88510/dca96/v3/img/blog/graphql-post.png)


# **Using CompletableFuture as a Simple Future**

### we can create an instance of this class with a no-arg constructor to represent some future result, hand it out to the consumers, and complete it at some time in the future using the complete method. The consumers may use the get method to block the current thread until this result is provided.
```
Future<String> completableFuture = calculateAsync();

// ... 

String result = completableFuture.get();
assertEquals("Hello", result);
```

#### We can use the static completedFuture method with an argument that represents a result of this computation.
