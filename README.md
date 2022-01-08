# Introduction
Welcome to the first lab of CS 163/4! these labs will be integral to your learning of programming, being able to communicate with those around you and receiving feedback from your TA's is invaluable to furthering your understanding.

Tuesday labs will be structured to be a warmup or introduction to what you are currently learning. There will be reading and testing done in these labs to ensure you have a grasp on how mechanics work before applying them.
Thursday labs will be where you apply and create concepts learned in lecture and your previous labs.
Many labs will be built upon each other and will require you to fully complete a previous lab before continuing, so remember to stay up to date on lab content.

## Steps for this lab
For this lab, you will follow along the code given to you and answer questions outlined as comments. You may store these answers in a notebook or in a text editor to present to your TA for grading.

## Program Structuring

Each module of a program is self-contained within a **class**, so all programming must be within a class. The contents of a class are denoted with curly braces, "{ }", all contents of classes are contained within these braces.

A class may look like this:
``` java
public class ClassName {
    //Your code here
}
```

These classes may also have a unique portion of code known as a **main**, this is where programs are spurred up or started.

Expanding upon the class example, a **main** within a class will look like:

``` java
public class ClassName {
    public static void main(String[] args) {
        //Your code here
    }
}
```

## Commenting your Program

You may have noticed in the previous two examples the grey lines that began with a double slash, //.
This is what is known as a comment, in no way will these affect how your program runs and are use by programmers to leave notes in their code. Commenting is an incredibly useful tool when you want to remind yourself how your program runs, or if someone looks at your code without you they can refer to comments to discern what your program is doing.

The double slash, //, is a single line comment.
You can also use a multi line comment starting it with /**.
``` java
/**
 * A
 * multi-line
 * comment
 * How useful!
 ** 
```

## Variables

Onto the topic of this lab, variables are a core of Java and programming as a whole. Variables allow you to store data for later and repeated use within your program.

There are two main parts of creating a variable, the declaration and initialization. The declaration is essentially creating your variable and reserving a spot for its data within the computers memory.

Before creating a variable it is good to know that there are multiple types of variables, the **int**, **String**, and **double** types are some of the most common. Each variable has only one type. For now we will only be working with ints and Strings.

To declare a variable, on a single line, you must specify its type and then its name, like so:
``` java
variableType variableName;
```
variableName now has a reserved spot in the computer's memory.

NOTE: Within the Java programming language, you must end each line with a semicolon, ;. Unless you are opening a class or method with curly braces, { & }, which we will go over later.

Then you must initialize the created variable, variableName, to a value like so:
``` java
variableName = variableValue; //Note the semicolon.
```
The most common approach is combinining the declaration and initialization all onto one line:
``` java
variableType variableName = variableValue;
```

Now instead of using variableType, we will use an actual type. When you want to store a whole number, the int type will be the choice:
``` java
int number = 42;
```
A String type is what is used to store a "String" of characters:
``` java
String word = "Universe";
```
Creating a String variable is slightly more intricate than creating an int variable, the **S** in **String** must be capitalized, and the variable value must be contained within quotation marks, like "Apple".

## Printing
Now that we have created variables, it would be helpful to print them to the terminal.

System.out.print() and System.out.println() are used to create output or print data to the terminal.

Using our previously created number and word variables, we can print them out by putting out variable in between the parentheses in System.out.print().
``` java
System.out.print(number);
System.out.print(word);
```
The output would be:
```
42Universe
```

Using System.out.print**ln**() automatically adds what is known as a newline character to the end of the content printed in the parentheses.
``` java
System.out.println(number);
System.out.println(word);
```
The output would be:
```
42 //Newline character after the printed content.
Universe //Newline character after the printed content.
//A blank line here due to the previous newline.
```

You can also print content without using variables:
``` java
System.out.println("This is a printed line!");
```

## Operations
With the int type, we can perform a large number of operations on these types of variables.
Say:
``` java
int a = 13;
int b = 3;
```
We have two int types, and we can perform many operations on these two variables, such as addition, subtraction, division, multiplication, and modulo.
``` java
int c = a + b; // c now eqauls 16
int d = a - b; // d now equals 10
int e = a / b; // e now equals 4
int f = a * b; // f now equals 39
```
The division operation only equals 4 as the decimal (.3333) is essentially chopped off due to int types only holding whole numbers.

All of these examples so far should make some sense as they are operations we have worked with before.

The odd operation out would be modulo, which is seldom used outside of Computer Science. Modulo is an incredible operation that finds the remainder of a division operation, but an example would best explain it.
``` java
int g = a % b; // g now equals 1
/**
 * 3 goes into 13 a total of 4 times, which leaves a remainder of 1, which is what the value of our modulo is.
 */
```
If we had 51 and wanted 51 modulo 11, it would yield 6 as that is the remainder of 51 being wholly divisible by 11, 4 times. Leaving the remainder being 6.