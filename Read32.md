# **Read: 32 - Serverless and Amplify**

**“Focus on your application, not the infrastructure”**

## What is Serverless?
##### Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers. A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider. Pricing is based on the number of executions rather than pre-purchased compute capacity, isn’t it the ideal framework for that project you have been planning since a long time? Well, go ahead do it.
*  Here are some of the currently available cloud services:
![](https://hackernoon.com/hn-images/1*t4O4UXpdG68MQboNKC6bBw.jpeg)


<br>

# Traditional vs. Serverless Architecture
![](https://hackernoon.com/hn-images/1*x_v5NRC3TTMt1MaYl1gMUg.jpeg)

<br>

# The Serverless App
- A Serverless solution consists of a web server, Lambda functions (FaaS), security token service (STS), user authentication and database.
![](https://hackernoon.com/hn-images/1*TIrjN7EjLUVJmJ6YvHR7Dg.png)

+ Client Application — The UI of your application is rendered client side in Modern Frontend Javascript App which allows us to use a simple, static web server.
+ Web Server — Amazon S3 provides a robust and simple web server. All of the static HTML, CSS and JS files for our application can be served from S3.
+ Lambda functions (FaaS) — They are the key enablers in Serverless architecture. Some popular examples of FaaS are AWS Lambda, Google Cloud Functions and Microsoft Azure Functions. AWS Lambda is used in this framework. The application services for logging in and accessing data will be built as Lambda functions. These functions will read and write from your database and provide JSON responses.
+ Security Token Service (STS) — generates temporary AWS credentials (API key and secret key) for users of the application. These temporary credentials are used by the client application to invoke the AWS API (and thus invoke Lambda).
+ User Authentication — AWS Cognito is an identity service which is integrated with AWS Lambda. With Amazon Cognito, you can easily add user sign-up and sign-in to your mobile and web apps. It also has the options to authenticate users through social identity providers such as Facebook, Twitter or Amazon, with SAML identity solutions, or using your own identity system.
+ Database — AWS DynamoDB provides a fully managed NoSQL database. DynamoDB is not essential for a serverless application but is used as an example here.



<br>
<br>

### Serverless architecture is certainly very exciting, but it comes with a bunch of limitations. As the validity and success of architectures depend on the business requirements and by no means solely on technology. In the same way, Serverless can shine when used in proper place.

<br>
<br>

# Data modeling
#### Amplify automatically creates Amazon DynamoDB database tables for GraphQL types annotated with the @model directive in your GraphQL schema. You can create relations between the data models via the @hasOne, @hasMany, @belongsTo, and @manyToMany directives.
