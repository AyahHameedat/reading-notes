# **Read17: Spring Boot and OAuth2**

## OAuth2 is an authorization framework that enables the application Web Security to access the resources from the client. To build an OAuth2 application, we need to focus on the Grant Type (Authorization code), Client ID and Client secret.


![](https://3.bp.blogspot.com/-uQfvlzSkSf4/WyAhmM46lGI/AAAAAAAAZRc/LAViouUeZmc1WWg9qnwV70W6_Mfqb6CggCLcBGAs/s1600/overall-password-flow-2.png)


### OAuth2 defines the following server-side roles:

+ Resource Owner: The service responsible for controlling resources’ access
+ Resource Server: The service who actually supplies the resources
+ Authorization Server: The service handling authorization process acting as a middleman between client and resource owner

### All samples are implemented using the native OAuth 2.0 support in Spring Boot.

### There are several samples building on each other, adding new features at each step:

+ simple: a very basic static app with just a home page and unconditional login via Spring Boot’s OAuth 2.0 configuration properties (if you visit the home page, you will be automatically redirected to GitHub).

+ click: adds an explicit link that the user has to click to login.

+ logout: adds a logout link as well for authenticated users.

+ two-providers: adds a second login provider so the user can choose on the home page which one to use.

+ custom-error: adds an error message for unauthenticated users, and a custom authentication based on GitHub’s API.

<br>


### The apps all work on localhost:8080 because they’ll use OAuth 2.0 clients registered with GitHub and Google for that address. To run them on a different host or port, you need to register your apps that way. There is no danger of leaking your credentials beyond localhost if you use the default values. But, be careful what you expose on the Internet, and don’t put your own app registrations in public source control.	The apps all work on localhost:8080 because they’ll use OAuth 2.0 clients registered with GitHub and Google for that address. To run them on a different host or port, you need to register your apps that way. There is no danger of leaking your credentials beyond localhost if you use the default values. But, be careful what you expose on the Internet, and don’t put your own app registrations in public source control.
