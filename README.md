# Lab01 - Variables and Printing
## Introduction
Welcome to the first lab of CS 163/4! These labs will be integral to your learning of programming. Being able to communicate with those around you and receiving feedback from your TAs is invaluable to furthering your understanding.

`Tuesday labs` will be structured to be a warmup or introduction to what you are currently learning. There will be reading and testing done in these labs to ensure you have a grasp on how mechanics work before applying them.

`Thursday labs` will be where you apply and create concepts learned in lecture and your previous labs. 

**Readings**: You need to have your readings DONE before coming to lab (and lecture). They are essential to understanding content. 

The instructions for this lab follow this explanation.

## Program Structuring

Each module of a program is self-contained within a `class`, so all programming must be within a class. The contents of a class are denoted with curly braces, `{ }`. All contents of classes are contained within these braces.

A class may look like this:
``` java
public class ClassName {
    //Your code here
}
```

These classes may also have a unique portion of code known as a `main`, this is where programs are started. It is also called the entry point to your program / the first method called.

Expanding upon the class example, a `main` within a class will look like:

``` java
public class ClassName {
    public static void main(String[] args) {
        //Your code here
    }
}
```

## Commenting your Program

You may have noticed in the previous two examples the grey lines that began with a double slash, `//`. This is what is known as a comment. These will not affect how your program runs and are used by programmers to leave notes in their code. Commenting is an incredibly useful tool when you want to remind yourself how your program runs, or if someone looks at your code they can refer to comments to figure out what your program is doing.

The double slash, `//`, is a single-line comment.
You can also use a multi-line comment by starting it with `/*`.
``` java
/*
 * A
 * multi-line
 * comment
 */
 
 //How useful! 
```

## Variables

Onto the topic of this lab, variables are a core of Java and programming as a whole. Variables allow you to store data and use within your program.

There are two main parts of creating a variable: the declaration and initialization. The declaration is essentially creating your variable and reserving a spot for its data within the computer's memory.

Before creating a variable it is good to know that there are multiple types of variables, the `int`, `String`, and `double` types are some of the most common. Each variable has only one type. For now, we will only be working with `int`s and `String`s.

To declare a variable, on a single line, you must specify its type and then its name, like so:
``` java
variableType variableName;
```
variableName now has a reserved spot in the computer's memory.

NOTE: Within the Java programming language, you must end each line with a semicolon, `;`, unless you are opening a class or method with curly braces, `{ }`, which we will go over later.

Then you must initialize the created variable, `variableName`, to a value like so:
``` java
variableName = variableValue; //Note the semicolon.
```
The most common approach is combining the declaration and initialization all onto one line:
``` java
variableType variableName = variableValue;
```

Now instead of using `variableType`, we will use an actual type. When you want to store a whole number, the `int` type will be the choice:
``` java
int number = 42;
```
A `String` type is what is used to store a string of characters:
``` java
String word = "Universe";
```
Creating a `String` variable is slightly more intricate than creating an `int` variable, the **S** in `String` must be capitalized, and the variable value must be contained within quotation marks, like "Apple".

## Printing
Now that we have created variables, it would be helpful to print them to the terminal.

`System.out.print()` and `System.out.println()` are used to create output or print data to the terminal.

Using our previously created number and word variables, we can print them out by putting our variable in between the parentheses in `System.out.print()`.
``` java
System.out.print(number);
System.out.print(word);
```
The output would be:
```
42Universe
```

Using `System.out.println()` automatically adds what is known as a newline character to the end of the content printed in the parentheses. Note the additional `ln` part stands for new line.
``` java
System.out.println(number);
System.out.println(word);
```
The output would be:
```
42 //Newline character after the printed content.
Universe //Newline character after the printed content.
//'Cursor' is now here due to the previous newline.
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
The division operation only equals 4 as the decimal (.3333) is essentially chopped off due to `int` types only holding whole numbers.

Modulo is an incredible operation that finds the remainder of a division operation, but an example would best explain it.
``` java
int g = a % b; // g now equals 1
/**
 * 3 goes into 13 a total of 4 times with a remainder of 1, which is what the value of our modulo is.
 */
```
If we had 13 cookies and 4 people to distribute them to, we can easily see how many cookies are left over using the `modulo` operation. Modulo can also be used to find patterns, such as even/odd numbers or if a particular number is divisible by another. 

Now, let's go onto the lab!

## Step 1 - Self-explanation 
There are a number of questions in the comments in `VariablesPrinting.java`. Take a moment to read through the code, and answer those questions as comments within your program. 

Now before the warmup method, you will see a multi-line comment block. Write a paragraph explaining what `WarmUp()` is doing. This is called self-explanation, and research shows just practicing this in every lab will improve your understanding - even if what you write isn't correct! So take your best shot whenever you get a chance.

## Step 2 - Debugging
The purpose of the `debug()` method is to simply print out to the console:

```
We are debugging!
```

However, at this time the program doesn't even compile. Take a moment to get the program compiled, using the develop mode to submit and test. After the program is compiling, change Debugging to debugging - as case matters! 

> Shoutout to Grace Hopper. She designed the first compiler, which is the foundation of taking English and converting it into a language the machine can understand. Fun fact, she is often credited with coming up with the term debugging. The truth is that this term existed before her, but she did pull a moth out of relays which was causing the program to miscalculate, tape it in her coding notebook, and write "the first actual case of a bug being found". [Learn more about Grace Hopper!](https://en.wikipedia.org/wiki/Grace_Hopper)
![Bug Found](https://upload.wikimedia.org/wikipedia/commons/f/ff/First_Computer_Bug%2C_1945.jpg)


## Turning In
Turning in Tuesday labs will always have two parts. The first part will be simply to have the TA look over your comments and sign off that you completed the questions. CSU Online students, will copy their answers into a discussion post in canvas. CSU Online summer students, although you won't submit your explanations to TAs or onto Canvas, it is still highly encouraged that you complete them to enhance your understanding of the code. 

The second part is that you need to submit your code to the autograder. This is done by clicking the submit for grading button. 
