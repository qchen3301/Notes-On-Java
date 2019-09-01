# Notes-On-Java
Much learn (wow) so study

                   ▄              ▄
                  ▌▒█           ▄▀▒▌
                  ▌▒▒█        ▄▀▒▒▒▐
                 ▐▄▀▒▒▀▀▀▀▄▄▄▀▒▒▒▒▒▐
               ▄▄▀▒░▒▒▒▒▒▒▒▒▒█▒▒▄█▒▐
             ▄▀▒▒▒░░░▒▒▒░░░▒▒▒▀██▀▒▌
            ▐▒▒▒▄▄▒▒▒▒░░░▒▒▒▒▒▒▒▀▄▒▒▌
            ▌░░▌█▀▒▒▒▒▒▄▀█▄▒▒▒▒▒▒▒█▒▐
           ▐░░░▒▒▒▒▒▒▒▒▌██▀▒▒░░░▒▒▒▀▄▌
           ▌░▒▄██▄▒▒▒▒▒▒▒▒▒░░░░░░▒▒▒▒▌
          ▌▒▀▐▄█▄█▌▄░▀▒▒░░░░░░░░░░▒▒▒▐
          ▐▒▒▐▀▐▀▒░▄▄▒▄▒▒▒▒▒▒░▒░▒░▒▒▒▒▌
          ▐▒▒▒▀▀▄▄▒▒▒▄▒▒▒▒▒▒▒▒░▒░▒░▒▒▐
           ▌▒▒▒▒▒▒▀▀▀▒▒▒▒▒▒░▒░▒░▒░▒▒▒▌
           ▐▒▒▒▒▒▒▒▒▒▒▒▒▒▒░▒░▒░▒▒▄▒▒▐
            ▀▄▒▒▒▒▒▒▒▒▒▒▒░▒░▒░▒▄▒▒▒▒▌
              ▀▄▒▒▒▒▒▒▒▒▒▒▄▄▄▀▒▒▒▒▄▀
                ▀▄▄▄▄▄▄▀▀▀▒▒▒▒▒▄▄▀
                   ▒▒▒▒▒▒▒▒▒▒▀▀

## Boilerplate Purpose  

This repo and its files will host my self-study on Java, to be used later as reference material, or a quick 'how-to' guide for working with IDEs such as Eclipse or IntelliJ, while doubling as good practice to keep my understanding of Git commands up to date. I will be primarily referencing the textbook 'Starting Out With Java' (6th Ed) by Tony Gaddis. Any additional reference material (blogposts, how-to guides) will be documented in the Acknowledgements/References subheader. 

This repo is not meant to be a comprehensive overview on Java nor computer programming, either conceptually or practically. A Table Of Contents will be added eventually to facilitate access to specific subheaders, and condensed, information-heavy subheaders may be spun off into seperate files.

## Hardware

**Random Access Memory**: RAM holds the sequence of instructions, coded in binary, that programs references for its instructions.

Memory is divided into sections that hold an equal amount of data, known as *switches*. *Switch On* is 1, *Switch Off* is 0. Each *switch* is a *bit*, or *binary digit*, with 8 *bits* making up a *byte*. Each *byte* is assigned a unique number known as an *address*, ordered from lowest to highest. 

## The History and Utility of Java

The first incarnation of Java was developed at Sun Microsystems as a precursor platform to what we would now call The Internet Of Things (*IoT*): a generic programming language that would not be constrained by different processors used by different consumer devices. While a market for an *IoT* did not emerge in the 90s or millenium, the nascent consumer-oriented *Information Super-highway* proved to be an applicable testbed for the Java team's theories on a universal programming language. 

## Compilers and the Java Virtual Machine

Java is a *compiled* language. The *source code* contains the instructions written by the Java programmer, ending in a *.java* extension. These *source files* are then executed by the *Java compiler*, a baked-in program that translates *source code* into *executable* instructions. 

### The Need For A Compiler

Because Java is designed as a universal language, its *source code* cannot be directly read by a computer's CPU (not without a lot of extra overhead, anyway). The *JVM*, or *Java Virtual Machine*, executes *compiled* source code as Java-specific *byte* instructions. 

### Integrated Development Environments (IDEs)

IDEs bundle together text editing, compiling, debugging and other utilities into a single program for ease of development. 

## Object-Oriented Programming (OOP)

**Encapsulation**: the combining of data and code into a single *object*.

**Data hiding**: the ability of an *object* to hide its data from code outside the object. Only an *object's methods* may directly access and make changes to its data. An *object* may allow outside code to access the *methods* that operate on its data. When an object's data allows only selective access through methods, it can protect is data from accidental corruption.

## The Structure and Syntax of Java

```java
public class Sample {
    public static void main(String[] args) {
        System.out.println("Hello World, from a very simple Java program!");
    }
}
```

The `class` is the most basic "unit" of Java. A Java file may have more than one `class` but it can only have one `public class`. Each `public class` of a Java file must be the same name as the file. Por ejemplo, the code block above must be in a file named `Sample.java`

An `object` descends from a `class`. When a program is run, it creates `object`s based on the parameters set by a `class`. Every `object` created from a class is called an `instance` of that class. 

`Class`es must be *imported* in order to be used by Java programs, and are by convention imported at the very top of the program file, before any other declarations.

### Naming conventions in general
`variables` begin with lowercase and follow camelCase.

`primitive data types` also begin with lowercase

`class`es begin with uppercase

### The structure and syntax of a Java class

```java
AccessSpecifier class Name {
    Members
} 
```

`public` or `private` *AccessSpecifiers* defines the scope of a `class`. A `public` class is available to to code outside its file. A `private` class is accessible only within its own file. Likewise, all *fields* (aka `variables`) and `method`s contained within a `class`'s curly-bois are its `members`, and those can also be defined as `public` or `private`. Un ejemplo por a `class` de Java, con `method`es y commentarios, es

```java
//this class has methods to return the length and width of a rectangle

public class MyClassDemo { 
    private double length;
    private double width;

    public MyClassDemo(double len, double wid) { 
        length = len;
        width = wid;
        //this is a constructor, see explanation below
        //@param len - the length of a rectangle
        //@param wid - the width of a rectangle
    }

    public void setLength(double len) {
        length = len;
        //@param len stores the value of the length field (or variable)
        //this method is void because there is no value being returned
    }

    public void setWidth(double wid) {
        width = wid;
        //@param wid stores the value of the width field/variable
        //this method, like its partner setLength, is void because
        //there is no value being returned
    }

    public double getLength() {
        return length;
        //@return length variable, as a double
    }

    public double getWidth() {
        return width;
        //@return width variable, also as a double
    }

    public double getArea() {
        return length * width;
        //@return the product of the length and width variables
    }
}
```

Per convention, a class should contain a `constructor` `method` in its *fields*. `Constructor` `method`s perform setup and initializing operations, such as but not limited to storing initial values in instance *fields*. This allows access to a class as an object *reference*. Por ejemplo:

`MyClassDemo aRectangle = new MyClassDemo(15, 20)`
`MyClassDemo yetAnotherRectangle = new MyClassDemo(777, 4444)`

^ the above creates two `object` of the `class` `MyClassDemo`, stored in the `variable`s called `aRectangle` and `yetAnotherRectangle`, with the *values* of 15 and 20 in `aRectangle`, and the *values* 777 and 4444 in `yetAnotherRectangle`, thanks to `MyClassDemo`'s `constructor` `method`. By convention and syntax, a `constructor method` must be the same name as the `class`. A `class` named *MyClassDemo* would not have a `constructor method` named *MyClassDemoConstructor*

#### A Special Case: the default, and the no-args constructors!

Exactly what it says on the tin. A `class` without an explicitly defined `constructor method` will be given one by Java at compilation, with all numeric values set to 0, `booleans` set to `false`, and *reference* `variables` set to `null`. However, there may be use cases where a `class` does not need to accept input when being instansiated as an `object`, but comes with its own pre-defined values. The syntax for a `no-args constructor` may be as simple as 

```java
public MyClassDemo() {
    length = 1.0;
    width = 1.0;
} 
```

Two important things to note: any `constructor method`, `no-args` or otherwise, will override Java's `default constructor`, and a `no-args` constructor does not need `@params` if it is setting *fields*. 


Also per convention, a class's *fields* (I don't like that word) should be private, and `accessor` and `mutator` methods should be written so that those *fields* must be accessed explicitly using dot notation. En lo ejemplo anterior, los `accessor` methods es `getLength()` and `getWidth()`, while the `mutator` methods `setLength()` and `setWidth()` allow a change to the *fields* from outside the scope of the class. 

* `Accessor` = `getter`
* `Mutator` = `setter`


### Assignment

Assignment must follow `variable` `=` `value` convention. `myVar = 12` is valid, but `12 = myVar` will throw an error. Assignment CAN be done at initialization, por ejemplo: `int myVar = 12, days = 28`

### Casting
The `cast operator` allows a manual conversion of a `variable`'s value, even if it leads to a narrowing conversion. The syntax is:

`varName` = `(newDataType) previousValue`

Por ejemplo:

`myStringVar` = `(int) 3345` <-this converts the literal string '3345' into the integer 3345 

### The Strange Case of The String Class

The `String` class (always capitalized, following proper naming convention) has a few baked-in `methods` for quality of life operations.

`.length()` returns the length, in `int`s, of a `var`

`.charAt(someNumber)` returns the char at that position of a `String`. Por ejemplo:

```
String name = "Herman";
name.charAt(3); //returns 'm'
```

`.toLowerCase()` renders anything `String` with *UpPErCaSE* to all *lowercase*

`.toUpperCase()` returns the opposite, transforming `String` to all *UPPERCASE*

`.equals()` can be used to compare either `String` *literals* or `String` `variables`, and will return a `boolean`

`.compareTo()` is similar to `.equals()` but will return either `0`, `1`, or `-1` to determine whether or not a `String` *literal* or `variable` is equal, longer, or shorter. This `method` can be used in conjunction with *relational operators*, such as `==`, `<`, `>`, etc 

**BE AWARE THAT `.equals()` AND `.compareTo()` ARE *CASE SENSITIVE* !!**

#### The toString() Horror

##### Why override toString()?

Printing out any `object` in Java invokes `toString()` automatically on that `object`. However, the values returned are not `String literals`, but `hashcode values`. Overriding the `String` `class`'s baked-in `toString()` method (in conjunction with a `class`'s `constructor method`s) will return end-user usable values. Por ejemplo:

```java
//example of a Student class that returns the ID and name of a student
public class Student {
    private String studentID;
    private String studentName;

    //constructor method
    public Student (String studentID, String studentName) {
        this.studentID = studentID;
        this.studentName = studentName;
    }

    //toString() overriding method
    public String toString() {
        return studentID + " " + studentName;
    }
}
```
Without `toString()` overriding this class would return "Student@1fee6fc Student@1eed745" or something similar, as opposed to the expected values of "77AD Qingis Khan" 

### Demonstrating Objects and Classes with `Scanner`

`System.out` is an `object`. Its twin, `System.in` is also an `object`. However `System.in` only takes in data as *bytes*, so it must be partnered with a baked-in `class` called `Scanner` to have practical functionality.

`Scanner myScannerObject = new Scanner(System.in);`

* `Scanner` calls the `class` 
* `myScannerObject` is the name of the `object` of the `Scanner` `class`
* `= new Scanner(System.in)` creates a `Scanner` `object` *in memory*, and gives it the functionality to *read input* from `System.in`

### If-else conditonal syntax in Java

```java
if (conditions =/</>/!=/etc) {
    performAction;
    performSecondAction;
    performThirdAction;
    andSoForth;
    if (nestedCondition) {
        performNestedAction;
        performSecondNestedAction;
        andBeAwareThatTheyMustEndInSemicolons;
    } else {
        performNestedElseAction;
    }
} else {
    performElseAction;
    andDontForgetAboutElseIfs;
}
```

### Methods and method headers

A `method header` marks the beginning of a `method`. *Every* Java app must have a `main method`. **IntelliJ** has a keyboard macro for quickly construction a `main method`: `psvm`

The `method header` can be broken down into four distinct parts. They are, sequentially:

* the method modifiers
* the return type
* the method name
* parentheses

*Method modifiers* define the scope of the method. 
* `public` methods are available to code outside the scope of the `class`.
* `static` methods belong to a `class`, and not a specific `object`

*return type* is self-explanatory.
* `void` methods do NOT return values.
* Any other *type* of return must be defined: por ejemplo, `public static int myMethod()`, or `public static String myMethod2`

*method name* is also self-explanatory.

*parentheses* are where `variables` are set to receive `arguments`. A `void` method still needs *parentheses*, as a matter of consistency.

#### Parameters and Arguments

A value *passed **into*** a `method` is its `argument`. A `variable` that **receives** an `argument` is a `parameter`. Por ejemplo:

```java
public static void showSum(double num1, double num2) {
    double sumDouble; 
    sumDouble = num1 + num2; //num1 and num2 are PARAMETERS
    System.out.println("The sum is " + sumDouble);
}

showSum(5, 10); // 5 and 10 are ARGUMENTS
```

As a matter of convention, when commenting on `parameters`, use `@param` to denote when a `variable` is a `parameter` of a `method`, and `@return` to define the value a `method` returns.

#### Method Overloading

When a `class` has multiple `methods` with the same name, that method is *overloaded*. This has some useful applications. For example, a `constructor method` may want to have both an input option, but also a default option. An `add` method may want to allow for the addition of both numeric values and `String` or `char` values. 

## Application Programmer Interfaces (APIs) and Java

`APIs` have a slightly different connotation in Java than they do with web frameworks. The textbook boilerplate for a `Java API` is: *a standard library of prewritten classes for performing specific operations.* Por ejemplo, `print` and `println` are `methods` that are part of the `System` class that is part of the `Java API`. `System` contians objects and methods that perform system-level operations. An `object` of the `System` class is `out`, that has internal `methods` such as `print` and `println`.

## Escape! Some common escape sequences

| Escape Sequence | Name           | Description                                           |
| --------------  |:--------------:|:-----------------------------------------------------:|
| \n              | Newline        | (advances cursor to the next line)
| \t              | Horizontal tab | (causes the cursor to skip over to the next tab stop)
| \b              | Backspace      | (moves the cursor back either up OR left, one position)
| \r              | Return         | (moves the cursor to the beginning of the current line)
| \\\\            | Backslash      | (prints the backslash char)
| \\'              | Single quote   | (prints the single quote char)
| \\"              | Double quote   | (prints the double quote char)

## References

[Javatpoint.com's article 'Understanding toString()](https://www.javatpoint.com/understanding-toString()-method)