# Arrays, Loops, Imports

## **Packages**

#### Package in Java is a mechanism to encapsulate a group of classes, sub packages and interfaces.
```
Packages are used for:
1- Preventing naming conflicts.
2- Providing controlled access.

```

### Package declaration syntax:
```
package illustration;  //1) Package statment (optional).

import java.awt.*;     //2) Imports (optional).

public class Drawing {// 3) Class or interface definitions.
    . . .
}
```

## **Imports**

#### Import statement in Java is helpful to take a class or all classes visible for a program specified under a package.

#### The JOptionPane class is in the swing package, which is located in the javax package. The wildcard character (*) is used to specify that all classes with that package are available to your program. This is the most common programming style.

#### for Example :
#### **Make all classes visible altho only one is used.**
```
import javax.swing.*;  
class ImportTest {
    public static void main(String[] args) {
        JOptionPane.showMessageDialog(null, "Hi");
        System.exit(0);
    }
}
```


# **Loops**

###Looping in programming languages is a feature which facilitates the execution of a set of instructions/functions repeatedly while some condition evaluates to true.

#### Java provides three ways for executing the loops:
### **1- for loop:**
```
for (initialization condition; testing condition; 
                              increment/decrement)
{
    statement(s)
}
```

### **2- while loop:**
```
while (boolean condition)
{
   loop statements...
}
```

### **3- do while loop:**
```
do
{
    statements..
}
while (condition);
```

