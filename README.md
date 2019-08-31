# Notes-On-Java
Much learn (wow) so study

---
## Boilerplate Purpose  

This repo and its files will host my self-study on Java, to be used later as reference material, or a quick 'how-to' guide for working with IDEs such as Eclipse or IntelliJ, while doubling as good practice to keep my understanding of Git commands up to date. I will be primarily referencing the textbook 'Starting Out With Java' (6th Ed) by Tony Gaddis. Any additional reference material (blogposts, how-to guides) will be documented in the Acknowledgements/References subheader. This repo is not meant to be a comprehensive overview on Java nor computer programming, either conceptually or practically. A Table Of Contents will be added eventually to facilitate access to specific subheaders, and condensed, information-heavy subheaders may be spun off into seperate files.

---
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

```
public class Sample {
    public static void main(String[] args) {
        System.out.println("Hello World, from a very simple Java program!");
    }
}
```

The `class` is the most basic "unit" of Java. A Java file may have more than one `class` but it can only have one `public class`. Each `public class` of a Java file must be the same name as the file. The code block above must be named `Sample.java`, por ejemplo.

An `object` descends from a `class`. When a program is run, it creates `object`s based on the parameters set by a `class`. Every `object` created from a class is called an `instance` of that class. 

`Class`es must be *imported* in order to be used by Java programs, and are by convention imported at the very top of the program, before any other declarations.

### Naming conventions
`variables` begin with lowercase and follow camelCase.

`primitive data types` also begin with lowercase

`class`es begin with uppercase

### Assignment

Assignment must follow `variable` `=` `value` convention. `myVar = 12` is valid, but `12 = myVar` will throw an error. Assignment CAN be done at initialization, por ejemplo: `int myVar = 12, days = 28`

### Casting
The `cast operator` allows a manual conversion of a `variable`'s value, even if it leads to a narrowing conversion. The syntax is:

`varName` = `(newDataType) previousValue`

Por ejemplo:

`myStringVar` = `(int) 3345` <-this converts the literal string '3345' into the integer 3345 

### The Strange Tale of The String Class

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

** BE AWARE THAT `.equals()` AND `.compareTo()` ARE *CASE SENSITIVE* !!**

### Demonstrating Objects and Classes with `Scanner`

`System.out` is an `object`. Its twin, `System.in` is also an `object`. However `System.in` only takes in data as *bytes*, so it must be partnered with a baked-in `class` called `Scanner` to have practical functionality.

`Scanner myScannerObject = new Scanner(System.in);`

* `Scanner` calls the `class` 
* `myScannerObject` is the name of the `object` of the `Scanner` `class`
* `= new Scanner(System.in)` creates a `Scanner` `object` *in memory*, and gives it the functionality to *read input* from `System.in`

### If-else conditonal syntax in Java

```
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

A `method header` marks the beginning of a `method`. *Every* Java app must have a `main method`. **IntelliJ** has a keyboard macro for quickly construction a `main method` - `psvm`

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
| \'              | Single quote   | (prints the single quote char)
| \"              | Double quote   | (prints the double quote char)

