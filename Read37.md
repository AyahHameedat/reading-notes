# **Read: 37 - S3**

### What is Amazon S3?
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.

### Features of Amazon S3
+ Storage classes
+ Storage management
+ Access management
+ Data processing
+ Storage logging and monitoring
+ Analytics and insights
+ Strong consistency


### How Amazon S3 works
Amazon S3 is an object storage service that stores data as objects within buckets. An object is a file and any metadata that describes the file. A bucket is a container for objects.

To store your data in Amazon S3, you first create a bucket and specify a bucket name and AWS Region. Then, you upload your data to that bucket as objects in Amazon S3. Each object has a key (or key name), which is the unique identifier for the object within the bucket.

+ Buckets: A bucket is a container for objects stored in Amazon S3. You can store any number of objects in a bucket and can have up to 100 buckets in your account. 

+ Organize the Amazon S3 namespace at the highest level.

+ Identify the account responsible for storage and data transfer charges.

+ Provide access control options, such as bucket policies, access control lists (ACLs), and S3 Access Points, that you can use to manage access to your Amazon S3 resources.

+ Serve as the unit of aggregation for usage reporting.

### Amazon S3 data consistency model

#### Amazon S3 provides strong read-after-write consistency for PUT and DELETE requests of objects in your Amazon S3 bucket in all AWS Regions. This behavior applies to both writes to new objects as well as PUT requests that overwrite existing objects and DELETE requests. In addition, read operations on Amazon S3 Select, Amazon S3 access controls lists (ACLs), Amazon S3 Object Tags, and object metadata (for example, the HEAD object) are strongly consistent.


## To setup and configure your application with Amplify Storage and go through a simple upload file example:

```
1- amplify add storage

2- amplify push
```

### Add these dependencies:
```
dependencies {
    implementation 'com.amplifyframework:aws-storage-s3:1.35.4'
    implementation 'com.amplifyframework:aws-auth-cognito:1.35.4'
}
```


<br>
<br>

![image](https://user-images.githubusercontent.com/97673354/171070049-7ebf5c25-90ad-4aa7-aafc-6834819c8d29.png)
