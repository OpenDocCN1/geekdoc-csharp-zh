![](images/00043.jpeg)

![](images/00001.jpeg)

## A Beginner’s Guide To C# Programming

### *PROGRAMMING MADE EASY TO LEARN*

By

### *FAISAL NAZEER*

Copyright © 2016

## ABOUT AUTHOR:

Faisal has more than 4 years of
experience in *Programming*...He started To learn to code at the age of 14.he is currently making games for mobile platform.

## TABLE OF CONTENTS

Introduction
Legal Notes
Chapter 1\. (Intro To C#)

Chapter 2\. ( Primitive Types and Expressions )

**Chapter 3\. Non-Primitive Types Chapter 4.** Control Flow
**About The Author**

## LEGAL NOTES

Any Part of this book can not be reused or distributed anywhere and never download this from any unknown source if you find such activity plz let us know at

Faisalnaziarali@gmail.com

## **CHAPTER 1**.
(INTRO TO C#)

C# ( PRONOUNCED "CSHARP") IS AN OBJECT- ORIENTED PROGRAMMING LANGUAGE FROM MICROSOFT THAT AIMS TO COMBINE THE COMPUTING POWER OF C++ WITH THE PROGRAMMINGEASE OF VISUAL BASIC. C# IS BASED ON C++ AND CONTAINS FEATURES SIMILAR TO THOSE OF JAVA. C# IS DESIGNED TO WORK WITH MICROSOFT'S .NET PLATFORM.

## WHY C#.

### C# IS AN ELEGANT, SIMPLE, TYPE-SAFE, OBJECT-*•*

ORIENTED LANGUAGE THAT ALLOWS ENTERPRISE

### PROGRAMMERS TO BUILD A BREADTH OF APPLICATIONS.

C# is used in famous game engines[**•
•**] C# is used Worldwide

**• Simple command line utilities. Input stuff. Convert stuff. Output stuff.
•Desktop applications.
•Windows service
•Web services And many more.**

## C# VS .NET

**C#
C# is a programming language
.NET** .**Net is framework for Building applications on windows**

## History OF C Language

Before c# we had two languages in c family c and c++ and when we compile our code compiler converts our code into the native code of the machine on which we were running on.

It means if I wrote a application on windows machine it will no longer run on other os (linux ,mac etc).

When Microsoft was designing c# they came with the idea to borrow from java community. In java code is First translated into byte code and then into machine code

In c# code is first translated into il(intermediate language) and then translated into the machine code independent of computer we are running on . It’s the job of clr(Common
language runtime) to translate il code to machine code.

## Architecture of .NET applications

Application is consist of classes and these classes are the main building blocks of applications . These classes interact with each other to give us desired functionality

# What is a class.

A class is a container which has data which is also called attributes and functions which is also called methods

# Functions Or Methods

Functions and methods have behaviors and they do things for us

# Data.

Data represents state of our application

# Example:

## Car A car can have attributes alike model Color Brand Speed And a car can have functionality alike Start() Break() Take this car as a class In real world applications we have many classes each for some specific task and these classes Interact with each other to provide desired functionality.

# Namespaces.

As number of classes grow in our project we need a way to organize related classes so we use namespace. namespace is a container of same classes

# Assembly.

As number of namespaces grow we need a way to partition our application so here assemblies come handy. Assembly is a container of same namespaces

Physically it is a file on disk it could be (exe or dll).

# Our First C Program.

In this book we will use visual studio so open visual studio

On top go to file
>new>project>installed>templates>visual c#>windows>console application

And here we have 3 fields we can give name to our project just name the project HelloWorld

We can also set the location of the project by clicking browse button
Third we can name solution in visual studio we have solutions one solution can have more than one project

Finally click ok to create console application
See the screen shoot below

![](images/00002.jpeg)**Lets look at some windows and tabs of visual studio**

## Few common windows and tabs
Solution Explorer
Coding Editior
start with solution explorer to show solution explorer or any window go to view on the top and select that window you want to show in solution explorer window first we have Solution name and number of projects in this solution
properties>Assemblyinfo.cs

assemblyinfo is produced when application will compile it is the identification of application

## References

Under references we see assemblies linked with this project to do some job . these assemblies comes with console application template in visual studio.

## App.config

Here the configurations of the application is stored
it has fields like title, description, ![](images/00003.jpeg)

## Program.cs

Here in program.cs we can start coding

THIS FILE PROGRAM.CS WE HAVE BUNCH OF USING STATEMENTS ON TOP. Our Project Name is HELLOWORLD so visual studio by default creates a namespace HELLOWORLD. When we write code in this namespace we have access to all classes defined in this namespace. If we want to use a class from different namespace we have to import that in our code file that is why we use using statement by default visual studio adds 5 using statements

using System;
using System.Collections.Generic; using System.Linq;
using System.Text;
using System.Threading.Tasks;

**System is namespace in .NET framework where we have all handy utility classes**

![](images/00004.jpeg)**Every console application we create in visual studios has one class called program.cs
In this class we have one method/function and this is the entery point of our application**

static void Main(string[] args)
{
}

This method starts with static which we will later cover in this course

Then return type which is void and void means this function returns nothing.

And then the Name of the function Main .note that c# is a case sensitive language So Main has to Start With upper Case M.

Functions can have input and output which we are called arguments this function takes a string[] array input which we will cover later

And finally we close a code block with curly braces{}.
Now lets write helloworld to the console

## Console Application

A console application is a simple application with no graphics . To Display Heloworld to the console we can use Console Class which is used to write on console and take input from console.

So inside Main Method Type the code below Console.WriteLine("HelloWorld");

Console is a class and WriteLine is the function of Console Class. we can access a method of class with . (dot) and the name of the function . WriteLine is used to write a line on console .in () we give the input to that function . we can write anything inside to print on console in this case we will print helloworld to the console.

To run and see the result press shortcut key to run application in visual studio is
Ctrl + F5
Finished Code :

static void Main(string[] args) {
Console.WriteLine("HelloWorld"); }

**Congrats you have just finished the first chapter.**

## CHAPTER 2\. PRIMITIVE TYPES AND EXPRESSIONS

Now we will dive into some basic c# stuff

## **VARIABLES AND CONSTANTS** :
**VARIABLE**.

A name given to a storage location in memory
Declaring a variable
Datatype Name of the variable =value we want to assign ;
Every statement in c sharp ends with ;
Example
Int a =10;
Int is datatype , a is name and we assign value 10 with equal sign =

## **Constant**.

An immutable value. This value will not change throughout the lifetime of the application Example
pi =3.14 which we use to calculate area of circle it should be constant.
Declaring a constant
Const keyword Datatype Name of the constant =value we want to assign ;
Example of pi.
Const float pi=3.14f;

Name of variables and constants also called identifiers and a identifier cannot start with a number, A identifiers cannot have white spaces, identifier cannot be reserved keyword which already defined in c language ie(int ,bool ,float). Always use meaningful names .

## NamingConventions .Camel Case: [firstName]

First Word of camel case starts with lowercase and after all words start with uppercase

## .Pascal Case: [FirstName]

All letters of all words are uppercase

## .Hungarian Notation: [strFirstName]

First we prefix datatype and then**All letters of all words are uppercase**

## Primitive Types in C

![](images/00005.jpeg)

Working with real numbers

When we want to use float or double datatype we need to explicitly tell that treat this number as float or double to do that follow the syntax:

float number=1.4f;
double number=12.4m;
F and m keywords explicitly tells the compiler to treat number as flaot or double
In c we can have variables with same name but of different datatype .

## Non primitive Types

.String
.Array
. Enum . Class

# Scope:

Scope means where a variable/constant has meaning

![](images/00006.jpeg)**Here we have 3 blocks of code with 3 variables
So a variable a is accessible in any of its child block and in anywhere in this block
So a variable b is accessible in any of its child block and in anywhere in this block
Abd c variable can only be accesed in this same block**

## Practice variables in visual studio:

Open visual studio and create new console project

in main function of the program declare some values and show them on console see the code below

![](images/00007.jpeg)

To declare character data type we will enter a character inside ‘A’ and for string we enter string in “string”.

We also use keyword var instead of declaring the data type c compileir automatically detects the data type. Now change all the data types to var

It should look like this

![](images/00008.jpeg)

## **Format String**

![](images/00009.jpeg)

In this way we visualize the output . {0} will be replaced by byte.minValue which is the minimum value of byte and {1} will replaced by
byte.maxvalue which is the maximum value of byte can store.

## C# Operators

![](images/00010.jpeg)

## **.Arithmetic opertaors**

![](images/00011.jpeg)**These operators are used for mathematical calculations**

![](images/00012.jpeg)**Increment operator increases value by one (1) and decrement operator decreases by one**

# Comparison Operators

![](images/00013.jpeg)**One thing to note here is that equal (=) sign is used to assign value and == is used to test equality**

## Logical Operators

These are used in conditional statements which we will discuss later

![](images/00014.jpeg)

# Bitwise Operators:

These are used in low level programming

![](images/00015.jpeg)

## Practice operators :

In main method declare two variables and to display their value of sum just use

![](images/00016.jpeg)**Run application and see the result on console
We also use / ,- or any Arithmetic operators
Example 2**

![](images/00017.jpeg)

In this we case declared our variables as int to show division result in floating point number we have to explicitly tell compliler to treat these variables as flaot by casting (flaot) to both variables

Example 3

![](images/00018.jpeg)

Here we have three variables a,b,c if we want to add a and b first and then multiply with c we can do it by writing a+b inside (a+b) so now a and b first added then multiplied with c.

Examppe 4

![](images/00019.jpeg)**We can check for equality and in equality with compareon and logical operators
Here a is not equal to b so result will be true
Example 5:**

![](images/00020.jpeg)

With and operator we can now check that both conditions are true .here c>b which is true and c==a which is false so one of the condition is not true then result will be false

Example 6:

![](images/00021.jpeg)

We can use or operator if any of these condition is true result will be true

# Comments

Comments are used to describe what , why , how , constrains etc….
Comments are not executed
Types of comments

## Multiline comments:

These are used to write comments on multiple lines ![](images/00022.jpeg)

## Single line comment:

These are used to write comments on single line ![](images/00023.jpeg)

# Congrats chapter is finished……………… ………………………… ………………………… …….

## CHAPTER 3\. NON-PRIMITIVE TYPES

Chapter Text

## **CLASSES.**

Combines related variables(fields) and
functions(methods)
Let lear classes with a example

![](images/00024.jpeg)Here we a class named person with four fields and four methods
Classes are blueprint from which we create objects

## Object

Object is a instance of a class
With this example we can create three instance of persons
Marry
John
Ali

## Create A Class.

Access modifier class keyword name of class {
}
Example of person class

![](images/00025.jpeg)**Access modifier means who can access it public modifier means anyone can access it
A class can contain fields and methods. In this example method has no parameter or takes no input or output**

Calculator class example

![](images/00026.jpeg)

In this example add() function takes input and return a+b output.

## Creating Objects

We declare objects like variables but we explicitly have to allocate memory for it
Example of person class which from we now create a object

![](images/00027.jpeg)![](images/00028.jpeg)

We can use var keyword to make our code cleaner We can access fields and function of that object by using the object name and with. Dot and the function and field name

Person.name=”faisal”; Person.introduce();

# Static

We can add static keyword to Add() function of calculator class

![](images/00029.jpeg)**Now we can access Add() function directly from Calculator class itself**

![](images/00030.jpeg)

When we create objects there are multiple instances of Add method in memory but static Add function only exists at one place in memory.

# Practice Classes:

First create a class in visual studio by pressing
Shit+alt+c
Name that class Person
And now add first name and last name string fields
And a introduce() method which outputs the first and last name on console
See the cod below

![](images/00031.jpeg)**And now create a person object in main method and assign first and last name and call introduce() method
See the code below**

![](images/00032.jpeg)

Create a another class named Calculator and fill it with Add ()Method
This method takes input of two int variables and return them after adding them

Now come back to main method and create object of calculator class and finally call Add() function and store that value in a variable to print the result on console.

This function takes two arguments/inputs and add them. ![](images/00033.jpeg)**Result should be 3.**

# Arrays

A data structure to store a collection of variables of the same type
Why use array?

Example:
In this example instead of declaring 3 int variables we can declare one int[] array

Notice the square brackets[] .first brackets tells that it’s a array and 2^(nd) brackets tells the number of elements in the array. At the time of declaring we need to initialize it with number of elements.

Accessing the element of a array

![](images/00034.jpeg)

To access the first element we start with zero(0) index and second element is index 1 and so on and so forth .we pass the index in square brackets[].and can assign the value.

We can initialize array with object initialization syntax ![](images/00035.jpeg)

# Practice Arrays

Open up visual studio and in main method create a numbers array with three element assign index 0 to 1 then display all of them into console

And also create a Boolean array and set index 0 to true and finally display all of them onto console
If we don’t initialize index of array element default value of data type will be assigned , in this case Boolean default value is false and int has default value of 0

See the code below ![](images/00036.jpeg)**Now run the application and see the result.**

# Strings

A string is sequence of characters and we

surround them with **double quotes helloworld**

## string concatenation

we can concatenating strings together with syntax below

![](images/00037.jpeg)

In this example
We are concatenating first name and last anme strings together with string string literal which is empty string and with + sign.

# Practice Strings

Open visual studio
To create a string
String keyword name of string =string” Example
String firstname=faisal”
String secondname=nazeer”
//now we can concatenate two strings
Var fullname=firstname + +secondname” Now display it on console Console.WriteLine(fullname);

## CHAPTER 4\. CONTROL FLOW

### CONDITIONAL STATEMENTS

![](images/00038.jpeg)

### **IF/ELSE STATEMENST**

![](images/00039.jpeg)

### ON FIRST LINE WE HAVE A CONDITION IF CONDITION IS TRUE THEN IF CODE BLOCK WILL RUN. IF CONDITION IS FALSE THEN ELSE IF BLOCK WILL BE CHECKED IF ELSE IF CONDITION IS TRUE THEN ELSE IF BLOCK WILL RUN OTHERWISE ELSE STATEMENT WILL BE EXECUTED.

## SWITCH CASE STATEMENTS

![](images/00040.jpeg)

In switch case statement we compare the value of a variable in cases and if condition is true that code block will run , if not then skip to next and if none of them is true then default block will be executed

## Syntax of switch/case statements

First we create a variable and then we create cases and compare value of the variable and we can have as many cases we want and finally we can execute default block.

## Practice Switch Case:

char grade = 'A';

switch (grade)

{
case 'A':
Console.WriteLine("Excellent!"); break;

case 'B':

Console.WriteLine("nice");

break;

case 'C':
Console.WriteLine("Well done"); break;

case 'D':
Console.WriteLine("You passed"); break;

case 'F':
Console.WriteLine("Better try again"); break;
default:

Console .WriteLine("Invalid grade");
break;
}
Console.WriteLine("Your grade is {0}", grade);

Here we are checking the grade in every case which is A if any case is equal to a that will run and in this case first case is A so first block of the code will run.

## Iteration Statements

These statements are used to repeat sequence of statements un till given condition is true.
Types of itteration statements

![](images/00041.jpeg)

# For loop

## SYNTAX

The syntax of a **for** loop in C# is:

for ( init; condition; increment )

{
statement(s);
}

Here is the flow of control in a for loop:

 The **init** step is executed first, and only once. This step allows you to declare and initialize any loop control variables. You are not required to put a statement here, as long as a semicolon appears.

 Next, the **condition** is evaluated. If it is true, the body of the loop is executed. If it is false, the body of the loop does not execute and flow of control jumps to the next statement just after the for loop.

 After the body of the for loop executes, the flow of control jumps back up to the **increment** statement. This statement allows you to update any loop control variables. This statement can be left blank, as long as a semicolon appears after the condition.

 The condition is now evaluated again. If it is true, the loop executes and the process repeats itself (body of loop, then increment step, and then again testing for a condition). After the condition becomes false, the for loop terminates.

## **EXAMPLE**

using System;
namespace Loops {

class Program {
static void Main(string[] args) {
/* for loop execution */ for (int a = 10; a < 20; a = a + 1) {
Console.WriteLine("value of a: {0}", a); }
Console.ReadLine();
}
}
}

When the above code is compiled and executed, it produces the following result:

value of a: 10
value of a: 11
value of a: 12
value of a: 13
value of a: 14
value of a: 15
value of a: 16
value of a: 17

value of a: 19

## While loop

A **while** loop statement in C# repeatedly executes a target statement as long as a given condition is true.

## **SYNTAX**

The syntax of a **while** loop in C# is:

while(condition)

{
statement(s);
}

Here, **statement(s)** may be a single statement or a block of statements. The **condition** may be any expression, and true is any non-zero value. The loop iterates while the condition is true.

When the condition becomes false, program control passes to the line immediately following the loop.

## **EXAMPLE**

using System;
namespace Loops {

class Program

{ static void Main(string[] args) {

/* local variable definition */ int a = 10;

/* while loop execution */ while (a < 20)
{

Console .WriteLine("value of a: {0}", a); a++;
}
Console.ReadLine();
}
}
}

When the above code is compiled and executed, it produces the following result:

value of a: 10
value of a: 11
value of a: 12
value of a: 13
value of a: 14
value of a: 15
value of a: 16
value of a: 17
value of a: 18

## **Do While Loop**

Unlike **for** and **while** loops, which test the loop condition at the start of the loop, the **do...while** loop checks its condition at the end of the loop.

A **do...while** loop is similar to a while loop, except that a do...while loop is guaranteed to execute at least one time.

## **SYNTAX**

The syntax of a **do...while** loop in C# is:

do

{

statement(s);
}while( condition );

Notice that the conditional expression appears at the end of the loop, so the statement(s) in the loop execute once before the condition is tested.

If the condition is true, the flow of control jumps back up to do, and the statement(s) in the loop execute again. This process repeats until the given condition becomes false.

## **EXAMPLE**

using System; namespace Loops {

class Program { static void Main(string[] args) {
/* local variable definition */ int a = 10;

/* do loop execution */ do
{

Console .WriteLine("value of a: {0}", a); a = a + 1;
}
while (a < 20);
Console.ReadLine();
}
}
}

When the above code is compiled and executed, it produces the following result:

value of a: 10
value of a: 11
value of a: 12
value of a: 13
value of a: 14

value of a: 16
value of a: 17
value of a: 18
value of a: 19

## Foreach loop

Foreach loop is used to iterate from the elemenst of object which have list nature ie arrays.

![](images/00042.jpeg)First we create a local variable and then iterate the object whose elements we want to access

In this example we are iterating all the element of the array and displaying it onto console

# **Congrats book is finished**