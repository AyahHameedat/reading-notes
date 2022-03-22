# Working with Relationships in Spring Data REST

### 1. One-to-One Relationship

```
@OneToOne
@JoinColumn(name = "secondary_address_id")
@RestResource(path = "libraryAddress", rel="address")
private Address secondaryAddress;

```

### 2. One-to-Many Relationship

```

public class Library {
 
    //...
 
    @OneToMany(mappedBy = "library")
    private List<Book> books;
 
    //...
 }

```

### 3. Many-to-Many Relationship

```

public class Book {
 
    //...
 
    @ManyToMany(mappedBy = "books")
    private List<Author> authors;
 
    //...
}

```



### Note: There is a lot of information but I left it to the lecture to understand more then I will add more information about the WebApplicationContext and MockMvc object creation.
