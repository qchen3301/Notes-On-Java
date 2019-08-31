# Notes-On-Java
Much learn (wow) so study

---
## Boilerplate Purpose  

This repo and its files will host my self-study on Java, to be used later as reference material, or 
a quick 'how-to' guide for working with IDEs such as Eclipse or IntelliJ, while doubling as good practice to keep my understanding of Git commands up to date. I will be primarily referencing the textbook 'Starting Out With Java' (6th Ed) by Tony Gaddis. Any additional reference material (blogposts, how-to guides) will be documented in the Acknowledgements/References subheader. 

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

