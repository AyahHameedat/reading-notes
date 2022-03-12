# **Read: 09 - WRRC and Java**



## **Do a Simple HTTP Request in Java**
### The HttpUrlConnection class allows us to perform basic HTTP requests without the use of any additional libraries.

### 1) Creating a Request
#### The HttpUrlConnection class is used for all types of requests by setting the requestMethod attribute to one of the values: GET, POST, HEAD, OPTIONS, PUT, DELETE, TRACE.

```
URL url = new URL("http://example.com");
HttpURLConnection con = (HttpURLConnection) url.openConnection();
con.setRequestMethod("GET");
```

### 2) Adding Request Parameters
#### If we want to add parameters to a request, we have to set the doOutput property to true, then write a String of the form param1=value¶m2=value to the OutputStream of the HttpUrlConnection instance:
```
Map<String, String> parameters = new HashMap<>();
parameters.put("param1", "val");

con.setDoOutput(true);
DataOutputStream out = new DataOutputStream(con.getOutputStream());
out.writeBytes(ParameterStringBuilder.getParamsString(parameters));
out.flush();
out.close();
```

### 3) Setting Request Headers
```
con.setRequestProperty("Content-Type", "application/json");
```


### 4) Configuring Timeouts

### 5) Handling Cookies
```
cookies.forEach(cookie -> cookieManager.getCookieStore().add(null, cookie));
```

### 6) Handling Redirects 
### 7) Reading the Response
### 8) eading the Response on Failed Requests
### 9) Building the Full Response

## ** Link: https://www.baeldung.com/java-http-request**



## The HTTP Request Lifecycle

### **Step 1: Local Processing**
#### We will understand this request is being made by a browser, as opposed to cURL, an API client like Postman, or some other app.
#### The browser has the intended hostname for the request, it needs to resolve an IP address1. The browser will then look through its own cache of recently requested URLs, the operating system’s cache of recent queries, your router’s cache, and your DNS cache.


### **Step 2: Resolve an IP**
#### 1. If the cache lookup fails (we will assume it does), your browser fires off a DNS request using UDP3.
![](https://res.cloudinary.com/practicaldev/image/fetch/s--kNsmK31c--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_66%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/uyaj8ruh6qzs5ay5jgtx.gif)

<br>

#### 2. Your request will now have to travel many network devices to reach its target DNS server. Whenever the packet hits a piece of networking equipment, the device uses a routing table to determine which other device it is connected to that is most likely situated along the shortest path to the destination.
 

### **Step 3: Establish a TCP Connection**


### **Step 4: Send an HTTP Request**

### **Step 5: Tearing Down and Cleaning Up**
