# Spring Security Architecture

### Application security boils down to two more or less independent problems:
#### 1. authentication **(who are you?)**
#### 2. authorization **(what are you allowed to do?)**


<br>


# Authentication

### The main strategy interface for authentication is **AuthenticationManager**

```
public interface AuthenticationManager {

  Authentication authenticate(Authentication authentication)
    throws AuthenticationException;
}

```

### An AuthenticationManager can do one of 3 things in its authenticate() method:

#### Return an Authentication (normally with authenticated=true) if it can verify that the input represents a valid principal.

#### Throw an AuthenticationException if it believes that the input represents an invalid principal.

#### Return null if it cannot decide.

<br>

# Authorization

### Once authentication is successful, we can move on to authorization, and the core strategy here is **AccessDecisionManager**.

#### There are three implementations provided by the framework:
+ AccessDecisionVoter.
+ ProviderManager.
+ AuthenticationProviders.

<br>

![](https://www.prplbx.com/static/dc04e41e7f8614d51c02209156193a48/4c4fe/figure1-differences-authentication-vs-authorization.png)

<br>

