# The Syntax and Boilerplate of a Java Class

---
## The Basic Structure

    imports

    class

        private vars

        constructor method(s)

        getter/accessor methods

        setter/mutatotor methods

        other methods    
---

## Code Example With Comments

```java
//imports (if applicable) are instansiated at the beginning of the file
import.java.* 
import.java.util.*

public class ClassName {     //the className must be the same as the name of the .java file
    private String myString; //variables that are not @params are instansiated INSIDE the class' curly-bois
    private int myInt;

    //constructor method - overwrites Java's default constructor. 
    //If no constructor method is explicitly declared, Java defaults to its baked-in constructor
    public ClassName (String myString, int myInt) {
        this.myString = myString; 
        this.myInt = myInt;
        //this.someVar references the @param 
        //useful shortcut if a class's private vars are named the same as its @params
    }

    //getter(aka accessor) methods: these simply return the private vars
    public int getMyInt() {
        return myInt;
    }
    public String getMyString() {
        return myString;
    }

    //setter(aka mutator) methods: these allow changes to the private vars from outside the class
    //Unlike getter/accessor methods, these methods are declared VOID 
    //because they do NOT *return* any values, and require @param variables
    public void setMyInt(int myInt) {
        this.myInt = myInt;
    }
    public void setMyString(String myString){
        this.myString = myString;
    }

    //other methods
    //these will be called outside of the class with dot notation 
    //(ex: objectOfMyClass.convertType(4444);)
    public String convertType(String intToString) {
        intToString = Integer.toString(myInt);
        return intToString;
    }
}
```