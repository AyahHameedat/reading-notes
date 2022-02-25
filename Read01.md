# Java Basics

#### Java is defined by a specification and consists of a programming language, a compiler, core libraries, and a runtime (Java virtual machine) The Java runtime allows software developers to write program code in other languages than the Java programming language which still runs on the Java virtual machine. The target of Java is to write a program once and then run this program on multiple operating systems.
### let's start with The basics of this amazing Language!
<br>
 

+ ### **Variables**

 
##### Variable in Java is a data container that saves the data values during Java program execution. Every variable is assigned a data type that designates the type and quantity of value it can hold. Variable is a memory location name of the data.

##### A variable is a name given to a memory location. It is the basic unit of storage in a program.

##### The Java programming language defines the following kinds of variables:

### fokmfdkmfd
+ #### **Instance Variables (Non-Static Fields):**

##### Instance variables are non-static variables and are declared in a class outside any method, constructor, or block.



+ #### **Class Variables (Static Fields):**


##### These variables are declared similarly as instance variables. The difference is that static variables are declared using the static keyword within a class outside any method constructor or block.
Example of Instance Variables & Class Variables:      
```
class AYA         
     {      
    
    // Static variable
        static int a; 
    
    
    // Instance variable    
        int b;        
    
}
```

+ #### **Local Variables:**

##### A variable defined within a block or method or constructor is called a local variable.


+ #### **Parameters:**     

##### The important thing to remember is that parameters are always classified as "variables" not "fields".


+ #### **Naming:**   

#### Rules:
##### 1) Always begin your variables' names with a letter, not allowed to begin with symbols like ($, _,....).
##### 2) White space is not permitted.
##### 3) If name consists of more than one word, capitalize the first letter of each subsequent word. The names gearRatio and currentGear are prime examples of this convention
##### 4) If your variable stores a constant value, such as static final int NUM_GEARS = 6, the convention changes slightly, capitalizing every letter and separating subsequent words with the underscore character.


+ ### **Operators**

#### Java provides many types of operators which can be used according to the need. They are classified based on the functionality they provide. Some of the types are:
 ![Precedence and Associativity of Operators](https://media.geeksforgeeks.org/wp-content/uploads/operators.png) .



+ #### **Expressions, Statements, and Blocks**

+ #####  **Expression** is a line of code that holds some information
```
Example: int result = 1 + 2; // result is now 3      
```
+ ##### A **statement** is a single command that performs some activity when executed by the Java interpreter:      
```
Examples: 
      // assignment statement
      aValue = 8933.234;
      // increment statement
      aValue++;
      // method invocation statement
      System.out.println("Hello World!");
      // object creation statement
      Bicycle myBike = new Bicycle();     
```
+ ##### **Block**: A group of statements is called a block or statement block. A block of statements is enclosed in braces. Variables and classes declared in the block are called local variables and local classes, respectively. The scope of local variables and classes is the block in which they are declared.
```
Example:   
       class AYA {
       public static void main(String[] args) {
          boolean condition = true;
          if (condition) { // begin block 1
               System.out.println("Condition is true.");
          } // end block one
       }
    }      
``` 
##### In blocks, one statement is interpreted at a time in the order in which ...
<br>
+ ### **Control Flow Statements**      

##### A programming language uses control statements to control the flow of execution of a program based on certain conditions. These are used to cause the flow of execution to advance and branch based on changes to the state of a program. 

```Java’s Selection statements: 
    if
    if-else
    nested-if
    if-else-if
    switch-case
    jump – break, continue, return
```
<br>
    
### Note => you can read more from: 
    https://www.geeksforgeeks.org/
