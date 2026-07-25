![](d2d_images/cover.jpg)

Mastering C#: The Ultimate Beginner’s And Intermediate’s Guide to Learn C# Programming

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# In One Day

# with Exercises and Quizzes,

# A Step by Step Guide

![image](d2d_images/chapter_title_below.png)

(Effective Computer Programming Languages)

By

Dennis Sharp

Copyright © 2019

All rights reserved. No part of this publication may be reproduced, distributed, or transmitted in any form or by any means, including photocopying, recording, or other electronic or mechanical methods, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical reviews and certain other noncommercial uses permitted by copyright law.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Preface

![image](d2d_images/chapter_title_below.png)

This book is written to help you learn to code in C# immediately and with a very good understanding of the fundamental principles of programming

In this book, you will learn the fundamentals of C# programming. No prior programming experience is required. You will learn everything from scratch. For an absolute beginner this book explains complex concepts in a simple, clear, concise and step-by-step way manner for easy understanding. If you are already a programmer writing programs in other languages but new to C#, this book will bring you up to speed to start coding in C# immediately.

This is a great book for anyone who wants to get started with C# or programming in general. It is never too early or too late! All you need to learn programming is passion and determination.

The examples in this book are packed with carefully designed exercises that help you learn how to think like a programmer and to demonstrate the concepts being explained and for deeper understanding.

For intermediate C# developers, from Chapter Nine to Thirteen, you will sharpen your skills and knowledge on the principles of object orientation including encapsulation, inheritance and polymorphism. I will show why encapsulation is important and how it helps writing a robust code. I will talk about inheritance ; it is a way to reuse code and unfortunately it is  abused by a lot of amateur designer and developers  I will show the promise in inheritance and introduce you to the concept of composition as a more flexible way to reuse code  we will talk about polymorphism , I will show how use a piece of code that has a lot of if/ else and switch case statements and  refactor it into an object oriented style  you will also learn how to change the behavior of an application by extending it so instead of changing the  existing code which may affect the  quality of your  application behavior instead you  extend it by creating new classes  that  will change the behavior of your application and this is extremely perfect. Finally, we talk about interfaces; I will show how interfaces improve the testability and extensibility of your applications. Also an introduction to unit testing. I hope you will be a better developer after reading this book. .

From Chapter Fourteen  to the end We are  going to be discussing Advance topics like LINQ, Lambda expressions, delegates and events, exception methods, nullable type, Generics, Exception handling etc. As the English proverb said: "The taste of the pudding is in the eating “. Let dive in.

You can download the source code for the exercises and all the sample programs in this book at

[http://dennissharp.aliencoreedge.com/](http://dennissharp.aliencoreedge.com/)

Or send me a mail at dennissharp@aliencoreedge.com

Contact Information

I would love to hear from you.

For feedback or queries, you can contact me at [aliencoreedge@gmail.com](mailto:aliencoreedge@gmail.com).

# TABLE OF CONTENT

[A Step by Step Guide for Absolute Beginners, Intermediate or Advanced Developers with Exercises and Quizzes,](#c002.xhtml__Toc22916570)

[Preface](#c003.xhtml__Toc22916571)

[Chapter one](#c005.xhtml__Toc22916572)

[Introduction to C#](#c006.xhtml__Toc22916573)

[C# Fundamentals](#c007.xhtml__Toc22916574)

[Chapter Two](#c008.xhtml__Toc22916575)

[Primitive Types and Expressions](#c009.xhtml__Toc22916576)

[Chapter Three](#c010.xhtml__Toc22916577)

[Non Primitive Types](#c011.xhtml__Toc22916578)

[CHAPTER FOUR](#c012.xhtml__Toc22916579)

[Control Flow](#c013.xhtml__Toc22916580)

[Conditional Statements](#c014.xhtml__Toc22916581)

[Iteration Statements](#c015.xhtml__Toc22916582)

[Chapter Five](#c016.xhtml__Toc22916583)

[Arrays and Lists](#c017.xhtml__Toc22916584)

[Lists](#c018.xhtml__Toc22916585)

[Chapter Six](#c019.xhtml__Toc22916586)

[Working with Dates](#c020.xhtml__Toc22916587)

[Chapter Seven](#c021.xhtml__Toc22916588)

[Working with Text](#c022.xhtml__Toc22916589)

[Chapter Eight](#c023.xhtml__Toc22916590)

[Working with Files](#c024.xhtml__Toc22916591)

[Chapter Nine](#c025.xhtml__Toc22916592)

[Classes](#c026.xhtml__Toc22916593)

[Chapter Ten](#c027.xhtml__Toc22916594)

[Class Coupling](#c028.xhtml__Toc22916595)

[Chapter Eleven](#c029.xhtml__Toc22916596)

[Access Modifiers](#c030.xhtml__Toc22916597)

[Chapter Twelve](#c031.xhtml__Toc22916598)

[POLYMORPHISM](#c032.xhtml__Toc22916599)

[Chapter Thirteen](#c033.xhtml__Toc22916600)

[INTERFACES](#c034.xhtml__Toc22916601)

[Chapter Fourteen](#c035.xhtml__Toc22916602)

[C# Generics](#c036.xhtml__Toc22916603)

[The Most Useful C# Collections that Every C# Developer must Master](#c037.xhtml__Toc22916604)

[Dictionary<TKey, TValue>](#c038.xhtml__Toc22916605)

[HashSet<T>](#c039.xhtml__Toc22916606)

[Stack<T>](#c040.xhtml__Toc22916607)

[Queue<T>](#c041.xhtml__Toc22916608)

[Chapter Fifteen](#c042.xhtml__Toc22916609)

[C# Delegates](#c043.xhtml__Toc22916610)

[Chapter Sixteen](#c044.xhtml__Toc22916611)

[Events](#c045.xhtml__Toc22916612)

[Chapter Seventeen](#c046.xhtml__Toc22916613)

[Lambda Expressions](#c047.xhtml__Toc22916614)

[Chapter Eighteen](#c048.xhtml__Toc22916615)

[Extension Methods](#c049.xhtml__Toc22916616)

[Chapter Nineteen](#c050.xhtml__Toc22916617)

[LINQ](#c051.xhtml__Toc22916618)

[Chapter Twenty](#c052.xhtml__Toc22916619)

[Nullable Types](#c053.xhtml__Toc22916620)

[Chapter Twenty-One](#c054.xhtml__Toc22916621)

[Dynamics](#c055.xhtml__Toc22916622)

[Chapter Twenty-Two](#c056.xhtml__Toc22916623)

[Exception Handling](#c057.xhtml__Toc22916624)

[Chapter Twenty-Three](#c058.xhtml__Toc22916625)

[Asynchronous Programming](#c059.xhtml__Toc22916626)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter one

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Introduction to C#

![image](d2d_images/chapter_title_below.png)

Welcome to C#! Basic programming and am so glad that you picked up this book!

This book is designed to help both novices and skilled programmers, to learn C# programming fast. The aim of this book is to make Nonprogrammers learn basic skills that underlie good programming in C# and experienced developers to receive a rigorous explanation of the language, which may improve their programming skills

By the end of the book, you should have no challenges writing and debugging your own C# programs. Using Micro soft Visual Studio Ready to start?

We have so much to learn, so let us get started

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# C# Fundamentals

![image](d2d_images/chapter_title_below.png)

### What is C#?

C# (pronounced “C-Sharp”) is a  programming language developed at Microsoft by a team led by Anders Hejlsberg and Scott Waltemath,  it was designed specifically for the .NET platform to aid quicker and easy migration to .NET. C# by programmers who has their roots and previous experiences in C, C++ and Java, adapting the best features of each and adding new features of its own. Because C# has been built upon such widely used and well-developed languages, programmers find learning C# to be easy and enjoyable.

C# is an eventful, object-oriented, Microsoft visual programming language where programs are written with the help of an IDE preferable Microsoft Visual Studio an Integrated Development Environment (IDE). With this IDE, one can write, run, test and debug C# programs conveniently, one of benefit is time reduction in producing a working program as to compare with the fraction of the time it would have taken

Without using the IDE. The concept of rapidly creating an application using an IDE is usually referred to as Rapid Application Development (RAD).

### C# VS NET

C# is a programming language while .Net is a framework. It consist of a run time environment (CLR) and a class library  that we use  for building  applications on windows  The .Net Frameworks are not limited to C#, there are different languages that target .Net Frameworks such as F#, VB.Net. It is also a platform where web based applications can be distributed to a great variety of devices (including tablets, smart phones and computers). It offers a platform where applications written in different programming languages can communicate with each other

### CLR (Common Language Run time)

When a C# application is compiled, C# compiler compiles your code to IL (Intermediate Language) code. IL code is platform independent, which makes it possible to a take a C# program on a different computer with different hardware architecture and operating system and run it. For this to happen, we need CLR. When a C# application is executed, CLR compiles the IL code into the native machine code for the computer on which it is running. This process is called Just-in-time Compilation (JIT).

### Architecture of .NET Applications

From the architecture point of view, C# application consists of building blocks called classes. A class is a container for data (attributes) and methods (functions). Attributes represent the state of the application. Methods include code. They have logic. This contains our algorithms and code.

A namespace is a container for related classes. Therefore, as your application grows in size, you may want to group the related classes into various namespaces for better maintainability.

As the number of classes and namespaces even grow further, you may want to physically separate related namespaces into separate assemblies. An assembly is a file (DLL or EXE) that contains one or more namespaces and classes. An EXE file represents a program that can be executed. While DLL is a file that contains code that can be re-used across different programs.

### Why Learn C#?

C# is a beautiful cross-platform language that can be used to build different kinds of applications.  It has similar features and syntax with C, C++ and Java but easier to learn than them. Moreover, since it is part of .Net framework it has many re-usable libraries that enables you to quickly develop an application without building everything from the scratch With C#, you can build

Mobile apps (for Windows, Android and iOS)

Games

Web sites

Desktop applications

In addition, C# is an object oriented [imperative language](https://en.wikipedia.org/wiki/Imperative_programming)  what that means is that you tell the computer what to do and can wrap those commands into objects modelling your desired world. The versatility of C# brings you many career options.

### Getting Visual Studio

To write C# code, you need Microsoft Visual Studio. Visual Studio comes in different editions:

Community, Professional and Ultimate.

As an individual, or a student or a small team, you can download Visual Studio Community Edition

for free and build your free or paid apps with it. To download Visual Studio Community Edition,

please visit:

[https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx](https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx)

![image](d2d_images/image145.png)

––––––––

![image](d2d_images/scene_break.png)

### Our First C# Application

Let have a quick tour of Visual Studio and build a very simple C# sharp application

Open the Visual studio >File > New > Project

![image](d2d_images/image131.png)

In the above picture on the left side we have templates, here you see the kind of applications we can build with C#, as you see in the list we can build  desktop applications, web, mobile, window, cloud etc.  However, in this book we are going to focus on Console applications.

A Console application is a very simple application that does not a graphical user interface. In addition, it is a great learning tool for learning a new language

So from windows on the left side select console applications give it a name, here we will call it HelloWorld and select Location, you can put it wherever you want, you can create a folder on your desktop for this course and save it there

Note also this concept of solution in visual studio, which means that a solution can have one or more projects, but for now, we do not have to worry about it 

Click ok after giving it a name and the interfaces below are what we have be default

![image](d2d_images/image027.png)

Some Developers, the first time the open visual studio get intimidated by the many panels and icons displayed. But the truth is that 90% of the time all you need is the code editor and the solution explorer and if you can’t find  your  solution explorer just  go to VIEW > Solution Explorer.

The solution Explorer holds our project, in this case named  HelloWorld ,References which is  part of .Net framework  used to add references to the classes you might be using in the application  App.config  is an XML file where  we stored  configurations for this application or connection strings to the database  or any setting you want to store for your application  and lastly program.cs  is a class where we will start writing code ,,

![image](d2d_images/image007.png)

Here in this file program.cs, on the top we have a bunch of using statements

We have a namespace called HelloWorld , which is created by the visual studio using the name we gave our first console application. in C# , we have access  to any class under this namespace, but if we want to access any class outside this namespace we need to import it  using the keyword using and calling the name space where the  class reside , so by default visual studio has these five  using statements ,

System: this is a namespace in .Net Framework that houses all these basic utility classes and primitive types classes

System.Collections.Generics: is used to work with list collections and so on.

System. LINQ: is used to work with data

System. Text: is used to work with text, encoding etc.

System .Threading. Tasks: is used to build multithreading application.

In this application we are going to used only System

Every Console program which we create with visual studio has a class called program inside program, we have a default method called Main () which is the entry point t of the application that is where everything kicks off. This method is declared as static, that is something we will learn later, methods have inputs and outputs what go inside the parenthesis is the input which we called the parameters or arguments. Know that parameters are optional, but in this case in the default template the Main method has a parameter called args which of type string array which we will also learn later what you see before the method name Main () is the return type or the output in this case is void which means that the method does not return any value, it just contain some codes

Note also that C# is case sensitive; hence if you type the Main Method with small letter M the CLR will not find this method as the entry point of the application

Another thing to note in the above interface is the curly braces, so wherever we have a block of codes in C# we need to surround it with curly braces and that is applicable to classes, program and namespaces

Now let write a simple C# program, inside the Main () Method above after the opening curly brace

Type the following statement

Console.WriteLine (“Hello World”);

Then run the program by using Ctrl + F5 to see the output

You are expected to see this screen when you run the application

![image](d2d_images/image088.png)This window that you see above is what we call console and that is why the project is called Console Application. The Console class is used to read data from console or write to it has many methods.

### Quiz

Question-0:

What is a namespace?

a: A type that contains code for the program.

b: A container for classes.

c: A deployable unit of an application.

Answer is: b

Question-1:

What is JIT Compilation?

a: The compilation of IL code to native machine code at runtime.

b: The compilation of C# code to native code.

c: The compilation of C# code to IL code.

Answer is: a

Question-2:

What is an assembly?

a: A piece of code that is executed by CLR

b: Container of one or more classes

c: A single unit of deployment of .NET applications

Answer is: c

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Two

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Primitive Types and Expressions

![image](d2d_images/chapter_title_below.png)

In this chapter , We are going to start our journey  in learning C# , so I will introduce you to variables and constants , various data types  and type conversion , scope and overflowing and finally we  will discuss the  various operators that we have in C#

### Variables and Constants

Variables

Variables are names given to storage locations in memory. We use variables to store values temporarily in memory. In C#, to declare a variable we start with a data type follows by an identifier and end with a semicolon (;) as shown below

![image](d2d_images/image117.png)

Here int represents the integer type, and Number is the identifier for our variable. Note that C# is case Sensitive, therefore, these two variables are different, because one has uppercase N and the other lower case n. when declaring a variable you can optionally initialize it as seen above  but note that you cannot use a variable unless you initialize it as you see in the second example. Otherwise, the code will not compile.

### Constants

Constants are immutable values; values we know that at compile time those values will not change throughout the life of the applications. Why do we use Constants?  The reason is simple; to create safety in our application, especially in situations where we need to ensure that a value does not change.. Imagine in your application, you have this number called Pi = 3.14; which is used to calculate the area of a circle. That number should always be the same in our program we do not want to change it accidentally otherwise our results will be inaccurate. Therefore, we declare this number as a constant.

To declare a constant, we used the keyword const followed by the data type and the identifier and we must initialize like this const float Pi = 3.14;

### Points to Note about Identifiers

❖  Identifier cannot start with a number  for example this cannot be an identifier

1route ![image](d2d_images/image152.png) but this oneRoute is acceptable ![image](d2d_images/image158.png)

❖  It  cannot  include white space  like  this  first Name but firstName  is acceptable

❖  It cannot use a reserved keyword like int but if you are so desperate to used any of the reserved keyword, then you can prefix that with @ sign like this @int.

❖  Use meaningful name avoid doing this fn  instead of firstName

### Naming Conventions in C#

In C#, to name your local variables: Use Camel case like this string firstName= “Dennis”;

And for your constant variables use Pascal case like this const int MAXZoom= 5;

### Primitive Types

Here is the list of the most commonly used primitive types in C#, but the actual list is longer than this but I do not include them because they are almost never used, they are actually there for interoperability with other languages. . In This table they are divided into four types namely; Integral Numbers, real Numbers, Character and Boolean. Note that the C# keywords are written in small letter and each of them are mapped to a data type in .Net Framework as displayed in the second column, so when you compile your application  the compiler internally will  translate the C# keyword to a corresponding data type in Net framework. The third column “Bytes” shows the number of bytes each data type uses and the fourth column “Range” show the number of values each data type can store

![image](d2d_images/image082.png)

### Integral Numbers

In the table above, the Integral numbers are byte, short, int and long. And as you can see in the table byte is the smallest, it takes only 1 byte while long is the largest it takes 8 bytes. the larger the number of bytes, the more storage we have .in that data type  note that in .Net framework

byte maps to Byte

short maps to Int16

int maps to Int32

long maps  to Int64.

Real Numbers

In Real numbers, we have float, double and decimal.

In .Net framework

float maps  to Single Type  and it takes 4 bytes and stores large number 

double maps to Double  and is twice the size of float, it takes 8 bytes

decimal maps to Decimal and it take 16 bytes , the more precision you need the bigger datatype you use

Character and Boolean

In C#, we have character which is represent by the keyword char, and they are Unicode

bool which represent Boolean which can be either be true or false

Data Types Declaration and initialization Examples

Integral Numbers

Int c; // this is only declaration

Int a = 18; // this is declaration and initialization

Int b = 6;

c = a + b; // this is assignment of value to the variable c which is of type integer

Console.WriteLine(c);

### Real Numbers

By default in C#, double is used for real numbers by the C# compilers , so if you want to use the data type  like float and decimal , you need to explicitly tell the compiler  to treat the number you have as a  float or decimal  by declaring it in this  way for example 

float number = 1.2f; // by adding this suffix  f am telling the compiler to treat as a float

decimal number = 1.2m; // the suffix m tells the compiler to treat the number as decimal

Character and Boolean

char chA= ‘A’;

char =chB=’B’;

Console.WriteLine (chaA.Equal( ‘A’)); // output :  “True”

Console.WriteLine (‘b’.Equal(chB)); // output :  “False”

for more information  about C# built in type  just  go to [http://msdn.microssoft.com/en-us/library/cs7y5x0x0x(v=vs.90).aspx](http://msdn.microssoft.com/en-us/library/cs7y5x0x0x(v=vs.90).aspx)

### Overflowing

Let discuss the concept of over flow in C#, look at this example below

byte number = 255;

Number = number + 1; // output: 0

Console.WriteLine (number);  

The output of this snippet of code  will be  zero  instead of 256, this is because byte take only 255 and this is what we call overflowing we have exceeded the boundary of byte data type . In C#, by default there is no check for overflowing, which means that a value of a data type can be modified at runtime. And if we go beyond the boundary of the data type you get overflow. This is not desirable in a program, to avoid that we use the checked keyword as shown below

checked

{

byte number = 255;

Number = number + 1; // exception will occur

}

This code will throw an exception which you can use the exception handling (the Try and catch block) to prevent it.

### Scope

Scope determines where a variable or constant has meaning and is accessible

Take a look at these three blocks of code below

{

byte a = 1;

{

byte b = 2;

{

byte c= 3;

}

}

}

a is accessible anywhere inside this block of code  or any of these child  blocks but outside of its block it is not accessible  b is accessible  to its block and its child block c and c is only accessible in its block. A block is indicated by curly braces ({}).

### Demo Variables and Constants

Ok enough of theory let open visual studio and write some codes

![image](d2d_images/image093.png)

Run the code above to see the output using CTLR + F5

In C#, we have a keyword called var which makes variable declarations easier, for example in the above  code instead of explicitly  putting the data type  I can replace them with var which at runtime will map to its corresponding  datatype.

![image](d2d_images/image135.png)

Run the code above to see the output using CTLR + F5\. It should be the same as the previous example.

Ok now let take a look at constants

![image](d2d_images/image119.png)

We said before that we use the keyword const for a variable that we don’t want its value to change throughout our program. So in the above program we declare a constant, in the second line of the code we tried to modify the value of the constant pi, hence a red line from the compiler refusing to allow us to assign a different value to the const variable

### Type Conversion

There are occasions that you may want to temporarily convert the value of a variable to a different type. Observe that this conversion does not affect the original variable since C# is a statically typed language, which in simple definition means: that once you declare the type of a variable, you cannot change it. However, you may need to convert the "value" of a variable as part of assigning that value to a variable of a different type. We have the following type conversions in C#;

### Implicit Type Conversion (Casting)

If types are compatible (e.g. integral numbers and real numbers) and the type  you are considering is bigger,

you don't need to do anything. The value will be automatically converted by the runtime and

stored in the target type

Here is an example of implicit type conversion,

byte b = 1;

int k = b;

Here as we explained before, byte takes one byte of memory and integer takes four bytes, so we can easily copy the byte in to the integer variable and no data loss will happen.

But if data loss will occur the compiler will not allow implicit type conversion.

### Explicit Type Conversion

float f = 1.0f;

Int k = (int)f;

As you can see even though in converting the float f to an integer, will cause data loss, but we are telling the compiler to go ahead and do the conversion by enclosing the int data type in bracket beside the variable f  to convert its value to integer.

### Non Compatible Types

We may have two incompatible data types like int and string, we can have a number represented as string and we want to convert it to integer, we cannot use explicit type conversion. We have to employ a different mechanism such as using the Convert class and or the Parse method Convert class is part of the .Net framework and is define in the System namespace. It has a bunch of methods that is used to convert various data types to other data types .All the primitive types (int, short, boolean , float etc) that we have explained before they all have their own  parse methods . Check out the example below

string d = “1”;

int k = Convert.ToInt32(s);

int h = int.Parse(s);

Here are some of the methods you can find in the Convert Class;

*   ToByte()- which convert a given value to byte
*   ToInt16: which convert a given value to short.
*   ToInt32 (): which convert a given value to int
*   ToInt64 (): which convert a given value to long

### Another Example of Type Conversion 

![image](d2d_images/image144.png)

If you execute this code, you will get the following output

![image](d2d_images/image010.png)

Why? Because a byte does not have enough storage to take the number 1234, so when we run it the application crash. And here is exception, which is the error reporting mechanism in .Net framework. it is an advance topic and I covered it in my C# sharp advanced course book but for this example I will show you how to handle exception, sometimes exceptions are friendly and easy to understand sometime they are not, but in any case if you have an exception you do not understand enter it into google and you will a lot of answers and solutions for it.

Here in our example above, the exception occurred at the point of conversion from string to byte, so what we need to do is to wrap the code in a try and catch block to prevent the program from crashing like it did

Look at the update code below we put it in try block and the catch block get the exception. What happens is that the code you put in a try block is monitored and if exception occurs the catch block will be executed and display the friendly message to the user instead of crashing

![image](d2d_images/image130.png)

The output

![image](d2d_images/image172.png)

Operators

In C#, we have five following Operators

### Arithmetic Operators

We use arithmetic operators in computations where you are working with numbers. The table below present the arithmetic operators that we have in C#

![image](d2d_images/image176.png)

We also have other two arithmetic operators called increment and decrement, which are shortcuts for adding 1 or subtracting 1 from a variable. it can be used as prefix  increment or decrement or post fix increment or decrement

![image](d2d_images/image028.png)

Example

var a = 10;

var b = 3;

var c = 2;

Console.WriteLine(a+ b*c);

The output of this will 60; because C# follows the natural mathematical arithmetic precedence because division and multiplication have higher precedence than addition or subtraction. So if you want to add a and b before multiplying with c you write it this way

Console.WriteLine((a+ b)*c);

This way the output will be 26

### Comparison Operators

![image](d2d_images/image037.png)

Example

var a = 1;

var b = 2 ;

Console.WriteLine(a > b);

Console.WriteLine(a == b);

The outputs will be false, note that the result of a comparison expression is always a boolean value which is true or false

### Assignment Operators

![image](d2d_images/image091.png)

### Logical Operators

These are used mostly with Boolean expressions which are often used in conditional expressions

![image](d2d_images/image162.png)

Example

var a = 1;

var b = 2 ;

var c= 3;

Console.WriteLine(c > b && c > a); // the output will be true

Console.WriteLine(c> b &&  c == a);  // the output will be false

Console.WriteLine(c > b || c > a); // the output will be true

Console.WriteLine(c> b || c == a); // the output will be true

### Bitwise Operators

They are used in window API, in encryption and in socket programming

![image](d2d_images/image102.png)

### Comments

A comment is a text we put in our code to improve readability and maintainability .In C#, we have two ways to write a comment;

Single Line Comment:  prefix it with double slash

Example: //here is a single line comment

int j = 0;

Multi- line comments:  use /* to start and */ to finish it

Example

/* Here is a multi-line comments */

int j =0;

Note: keep your comments to a minimal use comments to explain whys, not whats.

Summarily, In this chapter we learn that C# is a statically typed language which means that when we declare a variable with a specific data type, that type cannot change during the life time of that variables, we also learn about primitive types like int, Boolean, short , float ,etc. . In the next chapter we will talk about non primitive types such as class, arrays, strings and enums

### Quiz

Question-0:

What would be the value of number after this line is executed?

byte number = 1000;

a: 1000

b: Number will overflow and the value would be something different

like 189.

c: This code cannot be compiled.

Answer is: c

Question-1:

The type long in C# is equivalent to which type in .NET framework?

a: Long

b: Int32

c: Int64

Answer is: c

Question-2:

What would be the output of this program?

byte number = 255;

number += 2;

Console.WriteLine(number);

a: 257

b: 0

c: 1

Answer is: c

Question-3:

What would be the value of number2 after this code is executed?

int number1 = 257;

byte number2 = number1;

a: 257

b: 2

c: This code cannot be compiled.

Answer is: c

Question-4:

What would be the value z?

var x = true;

var y = false;

var z = true && false;

a: True

b: False

Answer is: b

Question-5:

What would be the value of z?

var x = true;

var y = false;

var z = true || false;

a: True

b: False

Answer is: a

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Three

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Non Primitive Types

![image](d2d_images/chapter_title_below.png)

We have the following non-primitive types in C# namely:

Classes, Structs, Arrays, String and Enum

### Classes

Classes are building blocks of an application; these classes combine related variables (fields) and (methods) functions together. So here is an example, in the figure below we have a class called person with four fields Name, Age, Height and Weight. It also has four  methods or functions ; Walk(),Talk(),Eat()and Sleep(). This class is a type from which we create a blue print of an object.  Object is an instance of a class, from this class example we can create three instances of the person class like Mary, John and Scott as seen below. More or less when your application is running, it is actually objects that are talking with each other and collaborating to provide some functionalities

![image](d2d_images/image146.png)

### Declaring Class in C#

To create a class we start with an access modifier the keyword class and an identifier

Public class Person

{

}

In the example, public is what we call an access modifier. It checks whether a class is visible to other

classes or not. Access modifiers are beyond the scope of this book and I’ve covered them in my

my  second book on this course: C# Intermediate. For now just remember that whenever you want to create a class use the keyword public to make it accessible anywhere in the application.

Also, know that when you declare a variable in a class, you have to give it an access modifier, for now we will use public.

Here is another example of  a class with a field and a method:

public class Person

{

public string Name;

public void Introduce()

{

Console.WriteLine(“My name is “ + Name);

}

}

void  indicates that  this method does not return a value. In this method Introduce (), the empty parenthesis means that it does not accept any value or parameter. And what it does is to simply output the name of the person on the console .To create an object, we use the new operator:

Person person = new Person();

A better way of writing the same code is:

var person = new Person();

Tthe new operator is used to allocate memory to an object. In C# you don’t have to worry about

de-allocating the memory. CLR has a component called Garbage Collector, which automatically

removes unused objects from memory.

Once we have an object, we can access its fields and methods with the dot notation:

Person person = new Person();

person.Name = “Dennis”;

person.Introduce();

### Static Modifier

When  a static modifier is used on a class member (field or method), makes that member accessible only via the class, not any objects. So in the earlier example, if the Introduce method was static, we could access it via the Person class:

Person.Introduce();

static members are used in occasions where we want only one instance of that member to exist in memory. As an example, the Main method in every program is declared as static, because we need only one entry point to the application.

Let see another example of class, with static method

public class Calculator

{

public static int Add(int a, int b)

{

return a + b;

}

}

Here we have a static method of type integer that takes two parameters of type integer and return the sum of the two parameters. So to access this method we use the class name like this

int result=Calculator. Add(1,2); // the output  will be 3

In the real-world, it’s best to stay away from static as much as you can because that makes writing automated tests for applications hard. Automated testing is the topic for another course, but for now, just remember how to use members that are already declared as static, and prefer not to declare your own class members as static.

Demo class person example in Visual studio

![image](d2d_images/image045.png)

Notice that the class person is created outside the class program A better way to create class is to create as a separate file by right clicking the project solution file > click on  Add > Class and give it a name person.cs,  or you can use the short form Shift+ Alt+C then you can writes the codes  there ,also remember to add public to the  class declaration to make accessible anywhere in the application.  and from the main method we create an object of the class and use it to access the fields Lastname and firstname  and also the method . Introduce(). The output of this program will be

![image](d2d_images/image134.png)

### Structs

A struct (structure) is a type with similar  characteristics with a class. It combines related fields and methods together. In terms of syntax, it is similar but the difference is that instead of using the class keyword it uses the struct keyword

public struct ColorSpectrum

{

public int Red;

public int Green;

public int Blue;

}

Use structs only when creating small lightweight objects. That is for a subtle performance optimization. In the real-world,  new types  are usually created using classes, not structures.

In .NET, all primitive types are  defined as  structures. They are small and lightweight. The biggest primitive type does not have a  size that is more than 16 bytes.

### Arrays

An array is used to store a collection of variables of the same type. It is a data structure.

For example, imagine you will like to work with three numbers ,instead of declaring three int variables (that are related),  like this

int number1;

int number2;

int number3;

you can create an int array like this:

int[] numbers = new int[3];

Note this curly brackets here, the first one is used to tell the compiler that we want to declare an array and the second curly brace is to define the size of the array.in C#, arrays have a fixed size., Here, the number 3 specifies the size of the array. if an array is created, its size cannot be modified. If you need a list with dynamic size, you need to use the List class (explained later in the course)and the new operator is used to allocate memory for the array.

An array in C# is  an instance of the Array class in .Net. So, that’s why here we have to use the

new operator to allocate memory to this object.

To assign values to the array for example

numbers[0]= 1;

numbers[1] = 1;

numbers[2]= 2;

if you know ahead of time the values you want to store in the array you can make use of the object initialization syntax and  shorten the above code like this

int[] numbers= new int [3] { 2,8,17};

To access elements in an array, we use the square bracket notation:

numbers[0] = 2;

Note that in C# arrays are zero-indexed. So the first element has index 0.

Let go over to Visual Studio to demonstrate this

![image](d2d_images/image049.png)

In the code above, we use the var keyword to replace the datatype of the array numbers being declared note also that we use the Console class of the display the content of the elements in the array. This is basic way of doing it but we can also use loop, but we will talk about that later in this course. The output will be

![image](d2d_images/image168.png)

Look at the output of this code, we assigned a value 1 to the index 0 of the numbers array and no values for index 1 and 2 but from the output you can see that their default values are 0\. This is because by default elements of an array takes the default value of their datatype and in this case integer is their data type and its default value is 0, the same with flags array.

### Strings

A string is a sequence of characters. In C# a string is surrounded by double quotes, whereas a

character is surrounded by a single quote.

string name = “Dennis”;

char ch = ‘A’;

There are a few different ways to create a string in C#:

Using a string literal:

string firstName = “Dennis”;

Using concatenation:

It is useful if you want to combine two or more strings.

string name = firstName + “ “ + lastName;

Using string.Format:

This is cleaner than concatenating multiple strings since you can see the output.

String name = string.Format(“{0} {1}”, firstName, lastName);

At run time the value of the firstName will be placed at the index {0} placeholder and the lastname value will be placed at {1}.

Using string. Join:

This is useful when you have an array and would like to join all elements of that array with a separator like comma, which is a string.

var numbers = new int[3] { 11, 27, 37 }

string list = string.Join(“,”, numbers);

C# strings are immutable, which means once you create them, you cannot change their value or

any of their characters. The String class contain some methods for modifying strings, but these  methods return a new string and do not change the original string.

String vs string

Remember, all types in C# map to a type in .NET Framework. So, the “string” type in C# (all

lowercase), maps to the String class in .NET, which means we can declare a string in either of

the following ways:

string name;

String name;

The only difference is that if you use the String type, you need to import the System namespace

on top of the file, because that’s where the String class is defined. Using System;

### Escape Characters

There are few special characters in C# called escape characters as shown below

![image](d2d_images/image073.png)

So if you want to have a new line in your string, you use \n.

Since the backslash character is used to prefix escape characters, if you want to use the

backslash character itself in your string (eg path to a folder), you need to prefix it with

another backslash: string path = “c:\\folder\\file.txt”;

### Verbatim Strings

When there are many escape characters in a string, that string may become unreadable or hard to read and understand.

var message = “Hello Dennis\nLook into this folder  path:c:\\folder1\\folder2”;

Note the \n and double backslashes (\\) here. We can re-write this string using a

verbatim string, by prefixing our string with an @ sign, and get rid of escape

characters:

var message = @“Hello Dennis”;

Look into this folder path:

c:\folder1\folder2”;

### Demo Examples in Visual studio

![image](d2d_images/image086.png)

Run with Shift + F5 to see the output

### Enums

An enum is a data type that holds a set of name/value pairs.  enums  is used when you need to define multiple related constants.

public enum ShippingMethod

{

Regular = 1,

Express = 2

}

Now we can declare a variable of type ShippingMethod enum and use the dot notation

to initialize it:

var method = ShippingMethod.Express;

Enums are internally integers. So you can easily cast them from one data type to another :

var methodId = 1;

var method = (ShippingMethod)methodId;

var method = ShippingMethod.Express;

var methodId = (int)method;

we convert an enum to a string using the ToString() method. Every object in C# has this

method and can be converted to a string:

var method = ShippingMethod.Express;

8

var methodName = method.ToString();

To convert a string to an enum (called parsing), use Enum.Parse:

var method = (ShippingMethod)Enum.Parse(typeof(ShippingMethod),

methodName);

### Reference Types and Value Types

In C#, we have two main types from which we can create new types: classes and

structures (structs). All primitive data types are structures while arrays and strings are classes.

All classes in C# are reference Types while structures are Value Types.

Value Types

When you create a variable as a value type, a memory is automatically allocated to it on the stack and immediately removed once it is out of scope

When you copy a value type to another variable, a copy of the value stored in the

original variable is taken and stored in the second variable. Hence, these two variables

will be independent.

var i = 10;

var j = i;

j++;

Here, incrementing j does not impact i.

In practical terms, it means: if you pass an argument to a method and that argument is

a value type, its value will be copied. So any changes made to that  method argument in the method will be lost upon returning from that method.

Recall that : Primitive types are structures hence they are value types. Any custom structure you define will also be a value type.

### Reference Types

For classes, which are reference type, you need to allocate the memory for it by yourself using the new operator. In addition, this memory is allocated on heap, which means that even if the object goes out of the scope, it will not be removed immediately it will be removed by the garbage collector in CLR.

With a reference type, however, the reference (or memory address) of the object is

copied to the target variable. This implies that : if you copy a reference type to another

variable, any changes you make to the object referenced by either of these variables,

will be visible through the other variable.

var array1 = new int[3] { 11, 27, 38 };

var array2 = array1;

array2[0] = 0;

Here, both array1 and array2 reference (or point) the same array object in memory. So,

after the third line, the first element of both array1 and array2 will be 0.

Run the following code to appreciate the explanation above

![image](d2d_images/image170.png)

### Quiz

Question-0:

What is the correct way to declare an int array?

a: int numbers = new int[];

b: int[] numbers = new int[];

c: int[] numbers = new int[3];

Answer is: c

Question-1:

What would be the output of this code?

var array1 = new int[3] { 17, 28, 37 };

var array2 = array1;

array2 [0] = 0;

Console.WriteLine(array1[0]);

a: 0

b: 17

Answer is: a

Question-2:

How can we access the first element in this array?

var numbers = new int[3] { 21, 72, 3 };

a: numbers.First

b: numbers(0)

c: numbers[0]

d: numbers[1]

Answer is: c

Question-3:

We have a class as follows:

public class Point

{

public int X;

public int Y;

}

How can we create an object of type Point?

a: var Point;

b: Point p;

c: Point p = new Point;

d: Point p = new Point();

Answer is: d

Question-4:

We have a TaxCalculator class as follows. How can we call the Calculate method?

public class TaxCalculator

{

public static float Calculate()

{

}

}

a: TaxCalculator.Calculate();

b: new TaxCalculator().Calculate();

Answer is: a

Question-5:

The \n escape character in a string represents:

a: A whitespace

b: A line-break

c: A tab

Answer is: b

Question-6:

What would be the result of this program?

var number1 = 1;

var number2 = number1;

number2++;

Console.WriteLine(number1);

a: 1

b: 2

Answer is: a

Question-7:

We have an enum as follows:

public enum CustomerType

{

Bronze,

Silver,

Gold

}

What will be the output of this code?

var type = (int)CustomerType.Bronze;

Console.WriteLine(type):

a: 0

b: 1

c: Bronze

Answer is: a

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# CHAPTER FOUR

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Control Flow

![image](d2d_images/chapter_title_below.png)

In this chapter we are going to explore conditional and iteration statements in C# we use these statements to control the flow of the program. From this section you are going to start writing simple C# program.  And make sure you spend time with the exercises that is the way to train your mind to think like a programmer. So Let get started 

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Conditional Statements

![image](d2d_images/chapter_title_below.png)

We have the following conditional statements in C#:

### If / else Statements

Here is the basic structure in If / else statement

If(condition)

SomeStatement

Else if(anotherCondition)

anotherStatement

else

yetAnotherStatement

so in if we always have a (condition) in parenthesis that will be executed if the condition is true  and we can optionally have the else if  and optionally the else which  will be executed if other earlier conditions are not met .

we can also have nested  If Statements

If(condition)

{

If(anotherCondition)

// some statement

else

Try to avoid using multiple nested if else statements in your code to avoid make your code unreadable and hard to maintain.

### Switch / Case

In switch, we have a variable whose value is used to compare the values of other variables in the cases, in the switch example below the variable is state, which is an enumeration. There are two case statements that is evaluated am comparing the value of state if it is Active the statements or actions within that case is executed , if none of these conditions are met the default is executed .

Switch(state)

{

case State.Active

someStatement

break;

case State.Inactive

someStatements

break;

default:

someStatement

break;

} :

Let see an example of IF /Else statement in action

![image](d2d_images/image055.png)

The above code is quite self-explanatory. Now we can use the conditional operator in place of If/else. Check out the following code snippet

Bool isSuperCustomer=true;

float price;

if(isSuperCustomer)

price =20.12f;

else

price = 30.23f;

The above code can be rewritten using conditional operator like this

float price =(isSuperCustomer )? 20.12f: 30.23f;

––––––––

![image](d2d_images/scene_break.png)

Switch Case Example

Namespace SwitchCaseExample

{

Public enum Season

{

Spring,

Summer,

Autumn,

Winter

}

Class Program {

static void Main(string[] args)

{

var season = Season.Autumn;

switch(season)

{

case Season.Autumn:

Console.WriteLine(“It’s autumn let go swinging “);

break;

case  Season.Summer:

Console .WriteLine(“it’s great weather for relaxation ”);

break;

default:

Console.WriteLine(“Undefined season”);

break;

}

The output of this code will be its autumn let go swinging because season is autumn

We can also have two cases having one action like this

case month.August:

case month.September:

Console.WriteLine(“you got to be on holiday “);

break;

You don't have to repeat “you got to be on holiday” for each of the case .

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Iteration Statements

![image](d2d_images/chapter_title_below.png)

Every programming language has iteration statements that are used to repeatedly execute a sequence of statements. In C# we have four iteration statements 

*   For Loops
*   Foreach Loops
*   While Loops
*   Do-While Loops

Let examin the syntax for each of this iteration statement.

### For Loops

for(var i= 0; i < 10; i++)

{

}

For loops have three parts ,the initialization clause and that is where we create  the counter ,(var i=0;), the second part is  the condition clause , the for loop will be executed as long as the  condition is  valid (I < 10;) and  the third part is the iteration clause  where we increase or decrease the counter as the case may be (i++).  And statements of code within the curly braces will be executed repeatedly. Note that i is just a variable you can use any thing

### Foreach Loops

This is used to iterate over elements of innumerable objects that is anything that has some kind of list or array nature.. The syntax for foreach loop is

foreach (var number in numbers)

{

}

Here we have the temporary variable number, in keyword and list to iterate over numbers. Assuming that numbers is a list of integers, in every iteration the number will hold the current value in the list.

### While Loops

While (k < 10)

{

....

k++;

}

In while loop there is a condition which as long as it is valid the loop will execute. Typically, we have a counter which is initialized and increment or decremented as the loop is executed. It is a bit similar to for loop but the syntax is different.

### Do-While Loops

do{

{

......

i++;

} while (i< 10);

Do- While loop is slightly different from while loop, in that in do while loop, the condition is executed At least once because the condition is evaluated at the end of the loop. So here we have the keyword do and a block of statements to be executed and a counter to be incremented or decremented and we have while keyword followed by a condition to be evaluated. Note you do not always need a counter with a do-while loop. It depends on what you want achieve.

### Break and Continue

break: helps you to jump out of the loop

continue: jumps to the next iteration.

Let see some examples of these iteration statements

For Loop Example let say we want to display the even numbers from 1 to 10\. The following code will do just that

![image](d2d_images/image103.png)

The out put is

![image](d2d_images/image066.png)

A little exercise try writing the above code in a reverse order instead of starting from 1 to 10 start from 10 to 1 to display even numbers

Foreach Loop Example

Let say we have a name of type string we want to iterate and display each character of the string name. As you know, a string is innumerable.

var name =”Dennis Sharp”;

foreach ( var character in name)

{

Console.WriteLine (character);

}

Execute the above code to see the output

Let use an array to show another example

![image](d2d_images/image180.png)

The output will be

![image](d2d_images/image044.png)

While Loop Example

While Loop is best used  when you don’t know how many times the loop will run  for example  let write a program that ask the user to type their name  and  the program terminates only when the  user enter whitespace

![image](d2d_images/image112.png)

Run the above code and see the result

### Random Class

Just before I conclude this chapter, I want to introduce you to a useful class in C# called Random.

We use it to generate random numbers. Let see an example we want to generate random numbers from 1 to 10

![image](d2d_images/image051.png)

### Exercises

1.  Write a program that requires a user to enter a number. The number should be between 1 to 200\. If the user enters a correct number, display "correct" on the console. Otherwise, display "Incorrect". (This logic is used a lot in applications where values entered into input fields need to be validated.).
2.  Write a program, which takes two integer numbers from the console or user and displays the bigger of the two.
3.  Write a program to count how many numbers between 1 and 100 are divisible by 5 with no remainder. Display the count on the console.
4.  Write a program and continuously ask the user to enter a number or "ok" to exit. Calculate the sum of all the previously entered numbers and display it on the console.
5.  Write a program and ask the user to enter a number. Compute the factorial of the number and print it on the console. For example, if the user enters 7, the program should calculate 7x6x5 x 4 x 3 x 2 x 1 and display it as 7! = 5040.
6.  Write a program that randomly picks a number between 1 and 100\. Give the user 5 opportunities to guess the number. If the user correctly guess the number, display “You made it"; otherwise, display “You failed". (To ensure that the program is working well, you can display the secret number on the console first.)
7.  Write a program and ask the user to enter a series of numbers separated by comma. Find the biggest number among the numbers and display it on the console. For instance, if the user enters “7, 31, 18, 11, 24", the program should display 31.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Five

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Arrays and Lists

![image](d2d_images/chapter_title_below.png)

Earlier, we learn a little bit about arrays, here we want to have a deeper look at it.  We said before that array represent a fixed number of variables of a particular type. In C#, we have two types of arrays: Single Dimension array and Multi-Dimensional arrays like a matrix.

### Single Dimension Arrays

var numbers = new int[5];// where the length is 5

var numbers = new int[5]{1,2,3,4,5}; // this was initialized with its elements

### Multi Dimension Arrays

We have two types of multi-dimensional arrays in C#; Rectangular and Jagged arrays

![image](d2d_images/image099.png)

In a rectangular array, each row has the exact number of columns as seen above.

### ![image](d2d_images/image157.png)

In the Jagged array, the number of column in each row can be different. Another way to look at jagged array is to see it as the array of an arrays i.e. a single dimension array where each element is a single dimension array.

Example of Rectangular array (2 Dimensional array) syntax:

var matrix =  new int[3,5]; // this means  array with 3 rows and five columns

var matrix = new int[3,5]

{

{1,2,3,4,5},

{5,10,15,20,25},

{1,5.10,15,20}

};

If the element of the array is known at the point of creating the array, we use the initialization object ({}) to initialize it.

To access element in this array we do it this way

var element = matrix[0,0]; where the 0’s are the index of the row and column respectively

Syntax for rectangular 3 dimensional array

Var colors = new int[3,6,4];

Jagged Syntax

We use two squared brackets to represent a jagged array

var array = new int[3][];

In the first square bracket you specify the number of the elements in the top level array.

Now we need to initialize the top level array

array[0] = new int[4];

array[1]= new int [5];

array[2] = new int[3];

The Array class has property like Length and bunch of methods like Clear ( ), Copy () Index Of ( ), Reverse( ). Sort() etc.

Let see them in action

var numbers  = new[]{3,7,9,2,17,7};

// Length

Console.WriteLine (“Length:”+ numbers. Length); //. To get the length of the array numbers

//IndexOf( )

Var index = Array.IndexOf(numbers,9); // To get the value of the index 9 in numbers

Console.WriteLine(“Index of 9: “ + index);

// Clear()

Array .Clear (numbers, 0, 2); //To clear the values within a range in array in this case from 0 to 2 

foreach (var n in numbers)

{

Console.WriteLine (n);

}

// Copy()

Int[] another = new int[3];

Array.Copy(numbers,another , 3); // copy the first three elements in numbers array to another ;

foreach( var  n in another )

{

Console.WriteLine(n);

//Sort( )

Array.Sort(numbers);

Console.WriteLine(“The sorted array”);

foreach(var n in another)

{

Console.WriteLine (n);

}

// Reverse

Array.Reverse(numbers); // display from the last to the first

Console.WriteLine (“Reverse of array”);

foreach(var k in numbers)

{

Console.WriteLine(k);

}

}

Note that all these methods are static methods that is why we use the class name Array to call them.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Lists

![image](d2d_images/chapter_title_below.png)

This is a data structure like array use in storing a number of objects of the same type. The difference between an array and a list is array have fixed size and the size of a list is dynamic. we use the list when we don’t know ahead of time how many objects we are going to store . we use  the List type which is a generic type  to create a list  as seen below inside the angle bracket we specify a generic data type and the angle bracket specify the type of the List, so int indicate that this is a list of integers. You can create a list of anything. (char, float etc) .

var numbers = new List<int>();

var numbers = new List<int>(){1,2,3,4,5};// you can initialize using the object initialization syntax

There are couple of useful methods that are available in the List class

Add( ) : to add an object to a list

AddRange( ) : to add a list of object  to  a list that can be another list  or array.

Remove( ) : To remove one object from the list .

RemoveAt( ) : to remove object at a given index.

IndexOf( ): it returns  the object value at a given  index .

Contains ( ): it tells us the List contain a given object or not.

Count( ):  This returns the number of object in the list .

Let see these methods in action

![image](d2d_images/image062.png)

The output will be

![image](d2d_images/image012.png)

### Exercises (Ensure that you do these exercises that is the way to become better at coding)

1.  Write a program and ask the user to enter their name. Reverse the name using an array and then store the result in a new string. Display the reversed name on the console.
2.  Write a C# program that prompts the user to enter 7 numbers. If a number has been already entered, display an error message and ask the user to re-try. And when the user has succeeded in entering 7 unique numbers, sort them and display the result on the console.
3.  Write a program that prompts the user to continuously enter a number or type "Stop" to exit. The list of numbers may include duplicates. Print out on the console, only the unique numbers that the user has entered.
4.  Write a program and ask the user to supply a list of comma-separated numbers (e.g 5, 1, 9, 2, 10, 39). If the list is empty or includes less than 6 numbers, display "Incorrect List" and ask the user to re-try; otherwise, display the 3 smallest numbers in the list.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Six

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Working with Dates

![image](d2d_images/chapter_title_below.png)

In this chapter we are going to be looking at how to work with dates and time in C#. we will be looking at DateTime and TimeSpan. One thing you need to know about DateTime object in C# is that they are immutable. Once you create them you cannot change them but there are bunch of methods that you can use to modify them like AddDays (), AddMonths( ) etc. and another thing you need to know is that there are  different  formats  in DateTime  another concept we have in DateTime is format specifier

See the below code snippet

![image](d2d_images/image080.png)

TimeSpan Example

TimeSpan take hour, minutes and second as its parameters it has properties like Minutes, TotalMinutes and methods like FromHours (), AddMinutes () etc. similar to the dateTime object , Timespan objects are also immutable  but  they also have  methods like Add() which can be used to modify them

![image](d2d_images/image104.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Seven

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Working with Text

![image](d2d_images/chapter_title_below.png)

In this section, we want to take a closer look at C# strings. Earlier in this course you learnt that the String keyword maps to a String class in C#  we also learnt that strings re immutable which means that once you create them you cannot change them  so we are going to be looking at useful String methods , converting  a string to a number and vice versa.

### String Formatting

ToLower(): This method converts all characters to a lower case  for example  //”:hello dennis”

ToUpper(): This method converts all character to upper case. //” HELLO DENNIS”

Trim(): This method eliminates whitespace around a string , this is useful  when capturing user input .

### Searching

To search for a character or string in a given string you can use the methods  

IndexOf()  and  LastIndexOf(), they return the index and  the last appearance of a given  character or string  respectively . IndexOf(‘a’) , LastIndexOf(‘Hello’)

### SubStrings

If you want to create a substring from a given string you use the substring method this method has a lot of overload s

Substring(startindex): returns the characters from the starting index to the end of the string.

SubString(startiIndex, length): This takes in a length argument in order to limit the number of characters retrieved.

### Replacing

If you want to replace a given title or a substring in a string you use the Replace method.

Replace (‘á’, ‘! ‘)

### Null Checking

We have a couple methods in C# that checks if an object or a variable is null or empty.

String.IsNullOrEmpty(str)

String.IsNullOrWhiteSpace(str)

### Splitting

To split a string, use the Split () method for example Str. Split (‘’). The split method takes in a delimiter as in this example am splitting a string using a space

### Converting Strings to Numbers

There are different ways to do it as follows:

String s = “1234”;

Int I = int.parse(s);

Int j = Convert.ToInt32(s);

It is better to use Convert class because if the string is null, it will return the default value which in this case 0\. Where as int.parse throws an exception.. it is safer to use Convert methods

### Converting Numbers to Strings

Int k = 1234;

String s = k.ToString(); // “1234”

String t = k.To String(“C “); // “$1,234.00”

String h = i.ToString( “C0”); // “$1,234”

![image](d2d_images/image125.png)

### String Demo

![image](d2d_images/image021.png)

Note we also have a class StringBuilder that is used for string manipulations. it has useful methods  like

Append(): To add something to the end of the string.

Insert(): To insert something at a given index.

Remove(): to remove a character or string at a given index.

Replace() : to replace a character or string  with another character or string and

clear().: To clear the whole text..

### String|Builder Demo

![image](d2d_images/image124.png)

––––––––

![image](d2d_images/scene_break.png)

### Exercise

Spend time to try these exercises before checking out the solutions

1- Write a program that prompts the user to enter a few numbers separated by a hyphen. Check if the numbers are consecutive. For instance, if the input is "3-4-5-6-7-8-9" or "21-20-19-18-17-16", display a message: "It is Consecutive"; otherwise, display "It is not Consecutive".

2- Write a program that prompts the user to enter numbers separated by a hyphen. When the user presses Enter, without any input, exit the program immediately; else, determine if there are duplicates. And if there is, print "There are Duplicates" on the console.

3- Write a program that ask the user to enter a time value in the 24-hour time format (e.g. 17:00). The correct time should be between 00:00 and 23:59\. If the time is correct, display “correct"; else, display "Incorrect Time". If the user does not provide any values, assume that it is an incorrect time.

4- Write a program that prompts the user to enter a few words separated by a space. Use the words to create a variable name with PascalCase. For instance if the user types: "number of rooms", display "NumberOfRooms". Make sure that the program is not dependent on the input. So, if the user types "NUMBER OF ROOMS", the program should still display "NumberOfRooms".

5- Write a program that prompts the user to enter an English word.  The program should be able to Count the number of vowels (a, e, o, u, i) in the word. So, if the user enters "adventure", the program should display 3 on the console.

You can download the source code for the exercises at [http://dennissharp.aliencoreedge.com/](http://dennissharp.aliencoreedge.com/) or send me a mail at dennissharp@aliencoreedge.com

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Eight

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Working with Files

![image](d2d_images/chapter_title_below.png)

In this section, we will be looking at how to work with files and directories in C#.

In .Net we have a namespace called System.IO, and this is where the classes with which to work with file s and directory are located.

We will be looking at the following classes;

File, Fileinfo

Directory, DirectoryInfo

Path

### File, Fileinfo

The two classes provide methods for creating, copying, deleting, moving, and opening files.

They have similar interfaces, the only difference is that fileInfo provides instance methods while file provide static methods so here are some of the methods that are contained in file, fileInfo 

❖  Create(): To create a file

❖  Copy(): To copy a file

❖  Deletes (): To delete a file.

❖  Exists (): To check if a file exist..

❖  GetAttributes(): To return all the attributes of a file

❖  Move (): To move a file from one location to another.

❖  ReadAllText():  To read the text in a file.

### Directory, DirectoryInfo

They are similar to File, FileInfo. DirectoryInfo provides instance methods while Directory provide static methods.  Their methods include

❖  CreateDirectory(): To create directory

❖  Delete(): To delete a directory

❖  Exists (): To check if a directory exist.

❖  GetCurrentDirectory(): Return the current directory.

❖  GetFiles(): Returns the files in a directory

❖  Move(): To move files form one directory to another

❖  GetLogicalDrives(): returns the logical drives of your hard disk like C drive

### Path

It has the following methods

GetDirectoryName():  To get the directory name

GetFileName(): get the file name

GetExtension(): get the extension name of the path or file

GetTemPath(): get the temporary path of a folder  .

### File,FileInfo Demo

![image](d2d_images/image120.png)

### Directory DirectoryInfo Demo

![image](d2d_images/image019.png)

To learn more about this go to google and type file info class C#.

### Path Demo

![image](d2d_images/image064.png)

Exercises

1 Write a program that reads a text file and displays the number of words.

2- Write a program that reads a text file and displays the longest word in the file.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Nine

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Classes

![image](d2d_images/chapter_title_below.png)

We are going to start our journey by learning about Classes, in this section, I will introduce you to bases of classes.

❖  What is a class?

❖  Real=world example of classes

❖  What is an object and how it is different from a class.

❖  Static members

### Class

A class is simply a building block of a software application so in a real world, an application consist of multiple classes. Each responsible for a particular behavior in an application or all these classes together producing the expected behavior from the application. Simply put A class encapsulates data (stored in ﬁelds) and behavior (deﬁned by methods).

![image](d2d_images/image175.png)

### Real World example

Let say we want to implement a web application like Blog engine, a typical software or web application consist at least of three layers; presentation, Business Logic and the data access layer. In each of these layers we can have classes each responsible for something in particular

![image](d2d_images/image123.png)

for example in the presentation layer we can have a class called PostView   which will be purely responsible for exposing posts to the user, in the Business logic we can a class for the post itself and finally the persistence or the data access layer will have a class that will save the post to the database or load the post from a database

### Anatomy of a Class

A class has two parts namely

❖  Data (represented by fields)

❖  Behavior (represented by methods / functions )

Here is how to demonstrate a class in unified model language (UML)

![image](d2d_images/image038.png)![image](d2d_images/image020.png)![image](d2d_images/image034.png)![image](d2d_images/image036.png)

### Another example

![image](d2d_images/image071.png)![image](d2d_images/image072.png)![image](d2d_images/image035.png)![image](d2d_images/image006.png)

### Object

An object is fundamentally different from a class. An object is essentially the instance of a class that reside .in a memory. In the Person class above, we can have objects like John, Mary Ann as the instances of the Person Class. The Person type or the person class define the blueprint by which we can create objects At runtime each of these objects in the memory talks to each other as result the expected result or behavior from the application is obtained.

### Declaring Classes

in C#, classes are declare like this access modifier followed by the keyword class and the name of the class with opening and closing curly braces and the methods and fields of the class are define within the curly braces  as shown below

public class Person

{

Public string Name;

Public void Introduce () // methods are declare with access modifier return type and the name and ()

{

Console.WriteLine(“Hi my name is “+ Name);

}

### Creating Objects

We use the type of the class followed by the identifier and then the new operator to initialize the instance of the class as seen below

Person person -= new Person ();

A shorter way to write the above is to use var keyword

var person = new Person ();

### Using Objects

Now that we have an object, we can access the members of the object.

In our person object we can access the name and give it a value and also access the introduce () method as seen below

var person = new Person();

person.Name = “Dennis”;

person.introduce();

### Class Members

We have two types of members instance and static members

Instance Members:  they are accessible from an object.  For example

var person = new Person();

person.introduce();

Static: members:  are accessible from the class. For example, we don’t have to have an instance of the Console class in order to use the method WriteLine (), instead we call it using the class name Console.

Console.WriteLine();

### Why use static members?

To represent concepts that are singleton that means we should have only one instance of that in the memory. Like DateTime.Now and Console.WriteLine ().

### Declaring Static Members

To define a member as a static, all you have to do is to use the static keyword after the access modifier and you can declare static on any member of the class

Public class Person

{

Public static int peopleCount = 0;

}

### Class Demo

![image](d2d_images/image089.png)

### Constructors

A constructor is a method that is called when an instance of a class is created .we use constructors to put an object in an early state that is to initialize some of the fields in the class. We do not have to always use a constructor, but if we need to initialize an object upon creation. Then we use the constructor to do that.

### Constructor Declaration

A constructor has an exact name as the class, that is a requirement, and it does not have a return type not even void

Public class Customer

{

Public Customer ()// default constructor

{

}

}

Second Example

Public class Customer

{

Public string Name;

Public Customer (string name)

{

This.Name = name;

}

}

### Constructor Overloading

Constructors can be overloaded. Overloading means having a method with the same name but different signatures. A signature is what uniquely identifies a method; its return type, its name and the types and number of its parameters.  In the constructor we can have different signatures as follows

Public class Customer

{

Public Customer () {....} // this takes no parameter it is a default constructor

Public Customer (string name) {....} // this takes only one string parameter

Public Customer (int id, string name) {...} // this takes two parameters

}

The reason why we do overloading is to make the initialization of the class easy.

### Constructor Demo

Let create a separate class called customer in the our Console Application project in visual studio

And define different signatures of the constructor or overload the constructor.

![image](d2d_images/image005.png)

In our program.cs, we can initialize the class and use one of the custom constructor that takes in two parameters {Id and name} to assign value to the members of the class object as seen below

![image](d2d_images/image001.png)

### Object Initializers

This is a syntax for quickly initializing an object without the need to call one of its constructors.

For example

var person = new Person

{

FirstName= “Harry”,

LastName = “White”

};

### Methods

Signature of a method contains the name, number and order of its parameters.

For example,

Public class Point

{‘

Public void Move (int x, int y){}

}

### Overloading Methods

Overloading a method means having a method with the same name but with different signatures. This makes it easier for the callers of the method to choose the more suitable signature depending on the type of data they have to pass to the method.

Public class Point

{

Public void Move (int x, int y) {} //two parameters that are integer

Public void Move (Point newLocation ){} // a class type as a parameter

Public void Move(Point newLocation, int speed){} // a class type and an integer  as parameters

}

### Method Demo

Let create a class Point with some methods overloading

![image](d2d_images/image122.png)

Let go to Program.cs and initialize this class and call the methods above

![image](d2d_images/image024.png)

––––––––

![image](d2d_images/scene_break.png)

Write this snippet of code in your visual studio and run it.

### Fields

A ﬁeld can be initialized in two ways: In a constructor, or directly upon declaration. The beneﬁt of initialising a ﬁeld during declaration is that if your class has one or more constructors, you’ll make sure that the ﬁeld will always be initialised irrespective of which constructor is going to be called Field Initialization

We can initial a field within a constructor like this

Public class customer

{

List<Order> Orders;

Public Customer()

{

Orders = new List<Order> ();

}

}

Another to initialize is outside the constructor

Public class customer

{

List<Order> Orders = new List<Order> ();;

}

Read-only Fields

We can declare a field  with a readonly  modifier to make sure that the field is assigned only once  we use readonly fields to create some kind of safety in application and to improve the  application robustness  for example take a look at  the customer class  I have a list of orders that is readonly ,if as a developer I  accidentally try to initialize this list in another method  the data I have in this order object will not be lost.

We use the readonly modiﬁer to improve the robustness of our code. When a ﬁeld is declared with readonly, it needs to be initialized either during declaration or in a constructor. The value cannot be changed. This prevents you from accidentally overwriting the value of a ﬁeld, which can result in an unexpected state. As an example, think of the Orders in the above example. If we accidentally re-initialize this ﬁeld somewhere else in the class, all the Order objects stored in the list will be lost. So we should declare it as readonly

Public classs Customer

{

Readonly List<Order> Orders = new List<Order> ();

}r

Access Modifiers

Access modifier is a way to control access to a class and /or its members  the reason for this control is to create some kind of safety in our programs and improve robustness for example ,in our Customer class  if we the following

Public class Customer

{

Private string Name;

}

In our program.cs  we have the following code

var john = new Customer

John.Name;.

This won’t compile because the field Name is private and can only be access within the Customer class. So usually fields in a class are private and can be accessed using the public methods called getters and setters. This is also the concept behind encapsulation which is information hiding. We will look at it later in this book

In C# we have 5 access modiﬁers: public, private, protected, internal and protected internal. - A class member declared with public is accessible everywhere. - A class member declared with private is accessible only from inside the class. - We’ll learn about the other access modiﬁers when we get to the inheritance. - We use access modiﬁers to hide the implementation details of a class. So anything that is about “how” a class does its job should be declared as private. This way, we make sure other parts of the code will not touch the implementation detail of a class. And as a result we improve the robustness of our code. If change the implementation of a class, we only need to make changes inside the class. No other parts of the code will need to be changed.

Access Modifiers Demo  with getter and setter methods

![image](d2d_images/image085.png)

Run this code and see the result

Properties

A property is a class member that encapsulates a getter/ setter method for accessing a field.

As a best practice, we must declare ﬁelds as private and create public properties to provide access to them. - A property encapsulates a get and a set method:

We need a property to create a getter and a setter with less code for example in the previous demo we had the code below the getters and the setter for the field _birthdate in the person class

![image](d2d_images/image079.png)

. Imagine we have ten fields in that class we will end up writing like twenty setter and getter methods for each of them and that will make our code too large and that is not very efficient. Instead we can the same thing as the above code with property.. So with property the code will look like this below

![image](d2d_images/image040.png)we can also use the auto implemented properties to rewrite the above like this

![image](d2d_images/image002.png)

When C# compiler see the above code, internally it will create the private field in the class.

### Properties Demo

Let create a class person with some filed that has properties as shown below

![image](d2d_images/image161.png)

In our program.cs we have the following code

![image](d2d_images/image118.png)

Run the codes to see the results

Indexers - Indexer is a special kind of property that allows accessing elements of a list by an index. - If a class has the semantics of a list, or collection, we can deﬁne an indexer property for it. This way it’s easier to get or set items in the collection. 

public class HttpCookie

{

public string this [string key]

{

get {}

set {}

}

}

### Exercise

Design a Stopwatch Design a class called Stopwatch. The job of this class is to simulate a stopwatch. It should provide two methods: Start and Stop. We call the start method ﬁrst, and the stop method next. Then we ask the stopwatch about the duration between start and stop. Duration should be a value in TimeSpan. Display the duration on the console. We should also be able to use a stopwatch multiple times. So we may start and stop it and then start and stop it again. Make sure the duration value each time is calculated properly. We should not be able to start a stopwatch twice in a row (because that may overwrite the initial start time). So the class should throw an InvalidOperationException if it’s started twice.

––––––––

![image](d2d_images/scene_break.png)

Learning tip: The aim of this exercise is to make you understand that a class should be always in a valid state. We use encapsulation and information hiding to achieve that. The class should not reveal its implementation detail. It only reveals a little bit, like a blackbox. From the outside, you should not be able to misuse a class because you should not be able to see the implementation detail.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Ten

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Class Coupling

![image](d2d_images/chapter_title_below.png)

### What is coupling?

In software Engineering, coupling is a measure of how interconnected classes and subsystems are. At the beginning of this course, I explained that software application is composed of many classes that are packaged inside of namespaces and assemblies. Take a look at the picture below

![image](d2d_images/image166.png)

Class A is interconnected to Class B and class F, hence any changes made to A will affect B and F and also Class D and C are dependent on Class B. this means that changes to Class A will affect the application. This is an example of tightly coupled design. The more coupled classes, the harder it is to change them. A change in one class may affect many other classes.

Nevertheless, in loosely coupled software, as opposed to tightly coupled software, is easier to change.

### How Do We Design a Loosely Coupled Application?

There are three things you need to understand to be able to design a loosely coupled application , , first  is Encapsulation, which we have  earlier discussed , secondly , is the relationships between classes which h is the topic of the this section  and  lastly the interfaces

### Relationships Between Classes

We have two types of relationships between classes: Inheritance and Composition.

Inheritance

This is simply a kind of relationship between two classes that allows one to inherit business logics from the other. It is usually referred to as Is-A relationship: for example, you can say that red is a color.

The advantages of inheritance are

Code re-use: which means encapsulating a code in one class and re-use it in another and polymorphic behavior; which is greatly powerful.

Syntax for inheritance

Let say we have a class Vehicle and another class Car that inherits from Vehicle class

public class Vehicle {

// common shared code

}

public class Car : Vehicle  {

// code specific to Car

}

Note that in C#, a class can have only one parent as you can see the car class inheriting the vehicle class as its parent

### Inheritance Demo

![image](d2d_images/image041.png)

![image](d2d_images/image075.png)

![image](d2d_images/image074.png)

We created two classes Vehicle and Car with car inheriting from Vehicle and calling methods in vehicle.

### Composition

This is another kind of relationship that allows one class to contain another.  We refer to composition as Has-A relationship. For example, A Car has an Engine. Look at this UML notation of this example

![image](d2d_images/image133.png)

The Beneﬁts of a composition are: Code re-use, ﬂexibility and a means to achieve loose-coupling.

### Let see Composition in action

![image](d2d_images/image067.png)

As shown in the figure above, Car class has a couple of instance variable and few methods. Maruti is a specific type of Car, which extends Car class means Maruti IS-A Car.

![image](d2d_images/image171.png)

Maruti class uses Engine object’s start () method via composition. We can say that Maruti class HAS-A Engine

![image](d2d_images/image105.png)

in the Program.cs class , the  object of Maruti class is  initialized . Though Maruti class does not have setColor(), setMaxSpeed() and carInfo() methods still we can use it due to IS-A relationship of Maruti class with Car class.

![image](d2d_images/image109.png)

If we run it we can see output like below.

![image](d2d_images/image009.png)

### Composition VS Inheritance

-Problems with inheritance:

›  It is easily abused by amateur designers / developers

›  it Leads to large complex hierarchies of class.

›  Fragility: Such hierarchies are very fragile and a change may affect many classes .

›  It results in tight coupling

Beneﬁts of composition:

Flexible: Any inheritance relationship can be translated to composition.

Leads to loose coupling

Having said all that, it does not mean inheritance should be avoided at all times. In fact, it’s great to use inheritance when dealing with very stable classes on top of small hierarchies. As the hierarchy grows (or variations of classes increase), the hierarchy, however, becomes fragile. Moreover, that’s where composition can give you a better design.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Eleven

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Access Modifiers

![image](d2d_images/chapter_title_below.png)

Your classes should be design like a black box. They should have limited visibility from the outside. The implementation, the detail, should be hidden. In C #, we use access modiﬁers (mostly private) to achieve this. This is referred to as Information Hiding (and sometimes Encapsulation) in object-oriented programming.

Public: A member declared as public is accessible everywhere. Look at the example below, the promote method is visible from the outside of the class Customer

![image](d2d_images/image023.png)

Private: A member declared as private is accessible only from the class. Look at the example below

The method CalculateRating() is visible only within the class , hence the customer object cannot access it the way it was able to access the Promte () method in the previous example rather to call this method you use the class name directly .

![image](d2d_images/image047.png)

Protected: A member declared as protected is accessibly only from the class and its derived classes. Protected breaks encapsulation (because the implementation details of a class will leak into its derived classes) and is better to be avoided.  Use private methods instead

Internal: A member declared as internal is accessibly only from the same assembly. Personally, I do not think it makes any sense to declare a class internal. Look at this example below trying to initialize the object of that class outside the assembly let say in program.cs will throw an error

![image](d2d_images/image153.png)

––––––––

![image](d2d_images/scene_break.png)

Protected Internal: A member declared as protected internal is accessible only from the same assembly or any derived classes. (Sounds weird? Forget it! It’s not really used.) just for you to know all the access modifiers in C#

![image](d2d_images/image178.png)

### Constructors and Inheritance

There are two things you need to know about constructors when it comes to inheritance, first is that at instantiation of an object the base class constructors are always executed first. And the second is base class constructors are not inherited.so you need to explicitly deﬁned the constructors in derived class.  When creating an object of a type that is part of an inheritance hierarchy, base class constructors are always executed ﬁrst. - We can use the base keyword to pass control to a base class constructor. It easy to explain this with an example. So here we have a vehicle class with registration Number as  shown below , the vehicle class has a constructor that initialize the  private field registration Number

![image](d2d_images/image096.png)

Now let say we want to create a car Class that derives from vehicle we will use the base keyword to indicate that derivation as shown below

![image](d2d_images/image149.png)

The base (registrationNumber) method is simply the constructor of the vehicle class. The constructor of the car class receives an argument called the registrationNumber and simply pass it to the base class.

Get the source code of this example

### Upcasting / Downcasting

Upcasting: is conversion from a derived class to a base class

Downcasting:  is conversion from a base class to a derived class. All objects can be implicitly converted to a base class reference.

// Upcasting let say we have a circle class that is derived from the Shape class as shown below

![image](d2d_images/image181.png)

So in upcasting we can do the following implicit conversion

Circle circle= new Circle ();

Shape shape = circle;

Downcasting requires a cast

// Downcasting Circle circle = (Circle)shape;

Casting can throw an exception if the conversion is not successful. We can use the as keyword to prevent this. If conversion is not successful, null is returned.

Circle circle = shape as Circle;

if (circle != null) ......

We can also use the is keyword:

if (shape is Circle)

var circle = (Circle) shape;

let see this concept in action , in our visual studio , let create a class Shape  and a class Text that derive from Shape class

![image](d2d_images/image151.png)

![image](d2d_images/image029.png)

![image](d2d_images/image126.png)

### Boxing and Unboxing

C# types are divided into two categories: value types and reference types. - Value types (e.g. int, char, bool, all primitive types and struct) are stored in the stack. They have a short life time and as soon as they go out of scope are removed from memory. - Reference types (e.g. all classes) are stored in the heap. Every object can be implicitly cast to a base class reference. The object class is the parent of all classes in .NET Framework. So a value type instance (e.g. int) can be implicitly cast to an object reference.

Boxing is the process of converting a value type instance is converted to an object reference

Int number =10;

Object obj = number;

// or

Object obj = 10;

Unboxing is the opposite: when an object reference is converted to a value type.

Object obj = 10;

Int number = (int)obj;

Both boxing and unboxing come with a performance penalty. This is not noticeable when dealing with small number of objects. But if you’re dealing with several thousands or tens of thousands of objects, it’s better to avoid it.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Twelve

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# POLYMORPHISM

![image](d2d_images/chapter_title_below.png)

Poly means many while morph means forms, so poly morphism simply means Many forms .The OOP has  this concept of poly morphism  to  provide an ability for a class to take more than one forms. So in C# polymorphism provides a way for the base classes to implement different methods that are called through the same name

### Method Overriding

Method overriding means modifying the implementation of an inherited method.  If a method is declared as virtual in the base class, we can override it in a derived class. Using the override keyword like seen below

![image](d2d_images/image090.png)

This technique allows us to achieve polymorphism. Polymorphism is a great object-oriented technique that allows use get rid of long procedural switch statements (or conditionals).

### Let see this in action

Look at this base class  Drawing  that has  three  derived classes Circle , Square , and Rectangle  overriding the  method Area() that is  define in the base class Drawing

![image](d2d_images/image042.png)

Each of the three derived classes below have the method Area () having the same name and signature as the parent class but with the keyword override, it defines properties and behaviors that are unique to it

![image](d2d_images/image011.png)

In the program class, the object of each class were defined and the Area method is called as seen below

![image](d2d_images/image015.png)

![image](d2d_images/image100.png)

### Abstract Classes and Members

Abstract modifier

Abstract modiﬁer states that a class or a member misses an implementation.it is easier to explain this with an example. Take for example our shape Class example below

![image](d2d_images/image164.png)

So we have a Shape class with Draw Method that is declared as virtual  and we have a Circle class that  derive  from the Shape class and in the Circle class we override the  Draw ( ) method  and here  we provide the implementation  for drawing a circle  but here we have a problem  of  defining an implementation for drawing a shape . how do we draw a shape, it doesn’t make any sense, when we talked about circle we know how to draw a circle or square but a shape it is almost impossible to define how to draw a shape because the concept of shape is too abstract, in situations like this, the better approach is to use abstract modifier so we can declare the Draw () method as abstract to indicate that this method is missing implementation and we leave it to the derived classes to provide an implementations

So to change abstract modifier, the code above changes to something like this

![image](d2d_images/image140.png)

Note that the Draw ( ) method is declared as abstract and that is why it doesn’t have a body or implementation. It is just a declaration and we terminate the declaration with a semi colon

When you declare a method or property as abstract the class that contains that method or property needs to be declared as abstract as well so here the Shape class is declared as abstract..

So abstract classes are inherently virtual and can provide poly morphic behaviors  just as we have discussed earlier.

### Few Rules you need to know while working with abstract classes and members

The first one is that abstract members cannot include implementation as we have seen in the this example

public abstract void Draw (  ) ;

The second one is that if a member is declared as abstract, the containing class needs to be declared as abstract too like this

![image](d2d_images/image057.png)

The third one is that in the Derived classes you must implement all abstract members in the base abstract class like this

![image](d2d_images/image167.png)

Here the Shape Class has only one method Draw (), supposing it has other methods, you must override them all in the Circle Class just the way the Draw () method was overridden here. Otherwise, that derived class is going to be abstract too

The last one is that abstract classes cannot be instantiated, so when you create a Shape Class as abstract you cannot do this 

![image](d2d_images/image087.png)

### The benefits of using Abstract Classes

❖  We use abstract when we want to provide some common behavior, while forcing other developers to follow our design.

For example in our  Shape class  by declaring the Draw(0 method as abstract we  are making sure  that anytime a developer derive  a class from the Shape method that  they provide an implementation for the Draw () method in  their derived classes . if  we fail to declare the  class Shape as abstract we run the risk of a developer  deriving  a class from the Shape class without  overriding  or providing implementation for the Draw ()  method 

❖  We use abstract members when it doesn’t make sense to implement them in a base class. For example, the concept of drawing a shape is too abstract. We don’t know how to draw a shape. This needs to be implemented in the derived classes.

### Sealed Classes and Members

Sealed classes are the opposites of the abstract classes, if a sealed modifier is applied to a class, prevents derivation of classes from that class. - If applied to a method, prevents overriding of that method in a derived class. for example we can applied the sealed modifier to our circle class that was derived from the Shape class and  what that means is that we cannot create a class that  derive from the circle class  as shown below

![image](d2d_images/image139.png)

We can also decide to apply the sealed modifier only to the method, note that the sealed modifier can only be applied to a virtual method that is being overridden as in the case of the Draw method in Circle class. as shown below

![image](d2d_images/image142.png)

### Why Use Sealed Classes

Sealed classes are slightly faster because of some run-time optimizations. Personally, I don’t think that optimization will make any difference to your application. In fact sealed classes are rarely used in applications. I suggest you avoid using sealed classes in your applications I feel it is anti-pattern and can mess up you inheritance hierarchy designs.

### Exercise

### Design a Database Connection

To access a database, we need to open a connection to it first and close it once our job is done.

Connecting to a database depends on the type of the target database and the database

management system (DBMS). For example, connecting to a SQL Server database is different

from connecting to an Oracle database. But both these connections have a few things in

common:

• They have a connection string

• They can be opened

• They can be closed

• They may have a timeout attribute (so if the connection could not be opened within the

timeout, an exception will be thrown).

Your job is to represent these commonalities in a base class called DbConnection. This class should have two properties:

ConnectionString : string

Timeout : Timespan

A DbConnection will not be in a valid state if it doesn’t have a connection string. So you need to pass a connection string in the constructor of this class. Also, take into account the scenarios where null or an empty string is sent as the connection string. Make sure to throw an exception to guarantee that your class will always be in a valid state.

Our DbConnection should also have two methods for opening and closing a connection. We

don’t know how to open or close a connection in a DbConnection and this should be left to the classes that derive from DbConnection. These classes (eg SqlConnection or OracleConnection) will provide the actual implementation. So you need to declare these methods as abstract.

Derive two classes SqlConnection and PostgreSqlConnection from DbConnection and provide a simple implementation of opening and closing connections using Console.WriteLine(). In the real-world, SQL Server provides an API for opening or closing a connection to a database. But for this exercise, we don’t need to worry about it.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Thirteen

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# INTERFACES

![image](d2d_images/chapter_title_below.png)

An interface is a language construct that is similar to a class (in terms of syntax) but is  fundamentally different.

An interface is simply a declaration of the capabilities (or services) that a class should provide.

Here is how we declare an interface instead of using the class keyword we use the interface keyword and know that in .Net all interfaces starts with the letter I. it is a convention as seen in the below example

public interface ITaxCalculator

{

int Calculate();

}

Unlike a class, interface does not have an implementation. So you see in the example above we have a method called Calculate (), it is simply a decoration, it doesn’t have an implementation and it also doesn’t have an access modifier 

This interface states a class that wants to play the role of a tax calculator, should

provide a method called Calculate() that takes no parameters and returns an int. The

implementation of this class might look like this:

public class TaxCalculator : ITaxCalculator

{

public void Calculate() { ... }

}

- So an interface is purely a declaration. Members of an interface do not have

implementation.

- An interface can only declare methods and properties, but not fields (because fields are about implementation detail).

- Members of an interface do not have access modifiers.

### Why Interface?

- Interfaces help in  building loosely coupled applications. We reduce the coupling between two classes by putting an interface between them. This way, if one of these classes changes, it will have no impact on the class that is dependent on that (as long as the interface is kept the same).

Let Look at this analog to help us understand it better. Think of the concept of a restaurant and a chef Let say the restaurant  needs a chef with certain capabilities , by that definition you can fill that role with anyone that has those capabilities as a chef  in the restaurant, so the dependency between the restaurant and the Chef is loose. If something happens to that chef, like he gets sick or he resigns we can get someone else to fill the role. Now in contrary, if we say a restaurant need John as a Chef that means the restaurant is very dependent on John. If something happen to John or decide not to come to work, then the restaurant is in trouble. So this is a definition of a tightly coupled dependency. That is the restaurant is tightly coupled to John.

But in software development, it is the best practice to build an application that its components or classes are loosely coupled, so that changes made to one class will have minimum or zero impact on other classes or components.  .

### Interfaces and Testability

Unit testing is part of the automated practice which helps improve the quality of our

code. With automated testing, we write code to test our own code. This helps catching bugs early on as we change the code .

In order to unit test a class, we need to isolate it. This means: we need to assume that every other class in our application is working properly and see if the class under test is working as expected.

A class that has tight dependencies to other classes cannot be isolated.

To solve this problem, we use an interface. Here is an example:

public class OrderProcessor

{

private IShippingCalculator _calculator;

public Customer(IShippingCalculator calculator)

{

_calculator = calculator;

}

}

- So here, OrderProcessor is not dependent on the ShippingCalculator class. It’s only dependent on an interface (IShippingCalculator). If we change the code inside the ShippingCalculator (eg add a new method or change the method  implementations) it will have no impact on OrderProcessor (as long as the interface is kept the same).

### Interfaces and Extensibility

We can use interfaces to change our application’s behaviour by “extending” its code(rather than changing the existing code).

If a class is dependent on an interface, we can supply a different implementation of

that interface at runtime. This way, the behaviour of the application changes without

any impact on that class.

For example, let’s assume we created a class DbMigrator for migrating our data base , this class can have a single method called Migrate() which holds the details of migrating the database  and let assume that  we want to log some details as the database is being migrated , for example , we may want to display the time the migration started  and when migration  finish and if any issue we log it too, . now we want to achieve  these behaviours  without  changing the details or the code in  our  method migrate() , instead we are going  extend our DBMigrator class  by creating an interface called ILogger which may  provide methods like LogError and LogInfo  So we inject this interface into our DbMigrator class using a constructor, this technique is called dependency injection. So let create a class that will implement the methods in the ILogger interface let call it ConsoleLogger.our DbMigrator class is dependent on an Ilogger interface. It knows absolutely nothing about the ConsoleLogger class that is implementing the methods in the ILogger interface. it is simply talking to the interface . So we change the behavior of the application at the main program by supplying an implementation that we want in the DbMigrator object. For example, at runtime, we can supply a ConsoleLogger to log the messages on the console. Later, we may decide to log the messages in a file (or a database). We can simply create a new class and call it FileLogger that implements the ILogger interface and inject it intoDbMigrator.. and at runtime  swap the implementation  of the ConsoleLogger with that of FileLogger

![image](d2d_images/image159.png)

The DbMigrator class and the ILogger interface class

![image](d2d_images/image056.png)

The ConsoleLogger Class that implements the methods in the ILogger interface

––––––––

![image](d2d_images/scene_break.png)

![image](d2d_images/image059.png)

Injection of the ILogger interface into the DbMigrator class using a constructor

![image](d2d_images/image137.png)

At runtime the ConsoleLogger is supplied to  display messages

![image](d2d_images/image065.png)

A new class Filelogger implementing Ilogger interface

![image](d2d_images/image003.png)

At runtime, swapping the Consolelogger with FileLogger to write the messages to a file

![image](d2d_images/image114.png)

The output on the notepad

So you can see we do not change one line of code in the DbMigrator class.

### Interfaces and Inheritance

One of the common misconceptions about interfaces is that they are used to

implement multiple inheritance in C#. This is fundamentally wrong, yet many books

and videos make such a false claim.

With inheritance, we write code once and re-use it without the need to type all that

code again.

With interfaces, we simply declare the members the implementing class should

contain. Then we need to type all that declaration along with the actual implementation in that class. So, code is not inherited, even the declaration of the members!

For example let say we have a class called UIControl with attributes and object such as Id, size, TopLeft and a method Draw (), Focus () and let’s create a class TextBox that derive from UIControl and implement two interfaces IDraggable and IDoppable.

I mentioned that interfaces has nothing to do with interfaces , let me clarify that  when you use inheritance for example  when you derive from UIControl , TextBox automatically inherit all the codes we wrote inside the UIControl  but with interfaces like in the case of  IDraggable  and IDroppable  they have  method  Drag () and Drop()  declaration with no implementations  which we have to implement in the TextBox class , so there is no code to inherit  nor is there any reusability , that is why I said that interface  has nothing to do with inheritance. Syntactically they are written the same way as inheritance, but it is fundamentally wrong to say that a class inherit an interface, classes implement interfaces 

![image](d2d_images/image095.png)

![image](d2d_images/image108.png)

![image](d2d_images/image081.png)

![image](d2d_images/image132.png)

Interfaces are used to build loosely coupled testable and extensible applications and not for code reusability

––––––––

![image](d2d_images/scene_break.png)

### Interfaces and polymorphism

Interfaces exhibit polymorphic behaviours. Let take a look at this VideoEncoder class that send a notification to the user once a video is encode by the user. This notification may be through mail, SMS, or any other method. the  VideoEncoder  class  need  not to know  the  mechanism employ  in sending this notification ., so  we don’t want  the VideoEncoder to be tied to a mailService class or SMS class , so interface will be used instead to achieve this notification. We create an interface INotificationChannel. So we create a MailNotificationChannel that will implement this interface. Again let create another  class  SmsNotificationChannel  that implement the same interface  INotificationChannel. So we have one interface and two implementations. So in our VideoEncoder class we will have a list of notification channels and we iterate through each of them to send notifications. We can create several implementations of this interface INotificationChannel. But the VideoEncoder class code will remain unchanged. This also achieve open close principle, which states that a software entity can be open for extension but close to code modification. But there is just one step missing here we need to find a way to tell videoEncoder the actual notification channels at runtime  so how we do that is , because this  ![image](d2d_images/image156.png)

Is define as private and we do not want to expose it to the outside. We need to create another method let call it Register NotificationChannel  that takes in the INotification Channel  object

So in our program.cs class we call that Register NotificationChannel  an d pass  the  MailNotificationChannel to it  and repeat that for SMSNotificationChannel![image](d2d_images/image121.png).The VideoEncoder class

![image](d2d_images/image174.png)

The INotificationChannel interface

![image](d2d_images/image060.png)

The MailNotification class implementing the INotificationChannel interface

![image](d2d_images/image101.png)

The SMSNotification class implementing the INotificationChannel interface

![image](d2d_images/image184.png)

The program.cs class

![image](d2d_images/image097.png)

The program output

### Exercise

### Design a workflow engine

Design a workflow engine that takes a workflow object and runs it. A workflow is a series of steps or activities. The workflow engine class should have one method called Run() that takes a workflow, and then iterates over each activity in the workflow and runs it.

We want our workflows to be extensible, so we can create new activities without impacting the existing activities.

Educational tip: we should represent the concept of an activity using an interface. Each activity should have a method called Execute(). The workflow engine does not care about the concrete implementation of activities. All it cares about is that these activities have a common interface: they provide a method called Execute(). The engine simply calls this method and this way it executes a series of activities in sequence.

The aim of this exercise is to help you understand how you can use interfaces to design

extensible applications. You change the behaviour of your application by creating new classes, rather than changing the existing classes. You’ll also see polymorphic behaviour of interfaces.

Real-world use case: in a real-world application you may use a workflow in a scenario like the following:

1- Upload a video to a cloud storage.

2- Call a web service provided by a third-party video encoding service to tell them you have a video ready for encoding.

3- Send an email to the owner of the video notifying them that the video started processing.

4- Change the status of the video record in the database to “Processing”.

Each of these steps can be represented by an activity. For the purpose of this exercise, do not worry about these complexities. Simply use Console.WriteLine() in each of your activity classes.

Your focus should be on sending a workflow to the workflow engine and having it run the

workflow and all the activities inside it. We don’t care about the actual activities.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Fourteen

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# C# Generics

![image](d2d_images/chapter_title_below.png)

C# Generic feature were added in C# 2.0 as a solution to the problem boxing and unboxing, casting problems which result to performance penalty. Hence, it increases performance, and promotes code reusability, as a result eliminate code duplication and ensure type safety in our applications. To understand this Let say we want to create a list to store a list of numbers. Below is a simple implementation of a basic list. We could have a method Add () to add a given number and a method  Indexer to return the number at a given index.

![image](d2d_images/image061.png)

Now if you want to store a book in the list, the above class will not work. So we have to go and create another class and call it BookList and it will have an Add () method that takes the object of a book  class as its parameter and also an indexer of type Book

![image](d2d_images/image048.png)

Now the problem here is that for every type we have to create a separate list and this sis a lot of code duplication and not productive. More so if there is a bug we have to fix it in multiple places hence one solution to fix this is to use a list of object as shown below

![image](d2d_images/image084.png)

Since object is the parent class for every types in .Net. Therefore, we can easily pass any type to this method and get any object from this indexer. However, there is another problem here, which is performance. If we use this class for storing value, types like integers. Every time we insert a value type inside this list, it has to be boxed to be stored as objects and every time we have to access this value it has to be unboxed .and this has a performance penalty.

Even if you use reference type every time we want to cast an object let say a book to an object or vice versa . This casting again has performance penalty so generic came as a solution to resolve this problem. With generic, we create a class once and re use it multiple times and it does not have the performance penalty as it is with the above object list

Example of a generic List class

Now generic has a parameter and the parameter are specified as <T> short for template as shown below. we also create  our Add ()  but instead of  passing an object of  book class or any other  parameter  we pass T which the user of this class can decide  what value of  T will be

![image](d2d_images/image039.png)

Let see how we can use the above class.

We go to our Program.cs , so here  we use  our generic List class to  generate  a list of numbers  and we can use  the same GenericList to store  books  as shown below . You can also see that at run time the Add () method has int pass as parameter in the case of numbers and has the object of the class Book pass as parameter in the case of Book

![image](d2d_images/image160.png)

So you see we get code reusability without having the performance penalty because at runtime there is no casting or boxing as our GenericList takes directly the actual parameter needed. This is the basis of creating generic classes, but in practical terms, you will be using Generic classes as oppose to creating one. It is rare to come across a situation where you need to create a generic class instead of using the existing generic lists that are part of .Net. In addition, you can find all the Generic collections in .Net in System.Collections.Generic.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# The Most Useful C# Collections that Every C# Developer must Master

![image](d2d_images/chapter_title_below.png)

List<T>

It shows a list of objects that can be accessed by an index. <T> short for Template means that this is a generic list. Lists are different from arrays in terms of size; arrays are fixed in size, while lists can grow in size dynamically.  Hence, they are also referred to as dynamic arrays or vectors. Internally, for storage purposes, a list uses an array. However, when it is filled up. It will create a new larger array, and will transfer the items from the existing array into the new created one. It is better to use a list than arrays these days even if you are working with a fixed number of things.

To create a list:

var list = new List<int>();

If you know ahead of time that you wish to store large number of items in a list, you can initial a size: like this

// creating a list with the size initialized

var list = new List<int>(20000);

Some of the useful operations you can perform with lists are:

// Add an item after the last item in a list

list.Add(4);

// Add an item at 0 index

list.Insert(4, 0);

// Delete an item from list

list.Remove(1);

// Delete the item at index 0

list.RemoveAt(0);

// Return the item at 0 index

var first = list[0];

// Return the index or the position number of an item

var index = list.IndexOf(4);

// Check if an item exist in a list

var contains = list.Contains(4);

// Return the  total number of items in the list

var count = list.Count;

// iterate or loop over all objects in a list

foreach (var item in list)

Console.WriteLine(item);

Now, let us analyze List Performance in these operations

### Adding or Removing Items at the Beginning or Middle of a List

When you add or remove an item at the beginning or middle of a list, it will have to shift the position of one or more items in its internal storage.  We use the Big O notation to specify the cost of this operation.  For the worst-case event, when we remove or add item at the very beginning, it simply means that all elements in the list were shifted from the original position. And the Big O notation is O(n) ,meaning that it is a linear progression .which means that as the size of the input increase, the execution time increase, so the execution time of the algorithm increases in direct proportion to n.

### Adding/Removing Items at the End

To add or remove an item at the end of a list is an operation that is a bit fast and is independent on the size of the list. The existing items are not moved or shifted. Hence, the execution time is relatively constant and is independent of the number of items in the list. The Big O notation: is O(1); Where 1 means constant.

### Searching for an Item

When methods like IndexOf(),Contains() and Find() are  used  for searching for an item in a list . A linear search is performed. Hence, it loops or iterates over all the elements of the list and when a match is found, it returns it. For the worst-case scenario, if this item is placed at the end of the list, all items in the list need to be searched or scanned before  the exact item is found. So the Big O notation is O(n).

### Accessing an Item by an Index

Accessing item using the index is what List is very good at. Hence, the Big O notation O(1). It is constant.

In conclusion, if you need to search for items based on some other criteria other than at the beginning or, middle or end of the list, and not an index (e.g. Order with ID 4567), it is  best  to use a Dictionary.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Dictionary<TKey, TValue>

![image](d2d_images/chapter_title_below.png)

Dictionary is another kind of collection type that is useful when you need to search by keys. For instance, let say you have a list of customers and as part of a job, you need to quickly find a customer by their ID (or some other unique identifier, which we call key). For a list, looking up a customer will involves a linear search and is O (n) in the worst-case scenario, as we have discussed earlier. However, with a dictionary, searching for items are quite fast with O (1), meaning that no matter how large the dictionary is, the look up time will always be relatively constant.

When entering or retrieving an object in a dictionary, you need to supply a key. A key is a value that uniquely identifies an object and cannot be null or empty. For example, to store an order in a Dictionary, you can use OrderID as the key.

To create a dictionary, first you need to specify the type of keys and values:

var dictionary = new Dictionary<int, Order>();

Here, our dictionary uses int keys and Order values. Therefore, you can store an Order object in this dictionary as follows:

dictionary.Add(customer.Id, customer);

You can also add objects to a dictionary during initialization:

var dictionary = new Dictionary<int, Customer>

{

{ order1.Id, order1 },

{ order2.Id, order2 }

}

Later, you can search for orders by their IDs very quickly:

// Return the order with ID 1234

var order = dictionary[1234];

You can remove an object by its key or remove all objects using the Clear() method:

/ /Removing an object by its key

dictionary.Remove(1);

// Removing all objects

dictionary.Clear();

Below are some other important methods that can be found in the Dictionary:

var count = dictionary.Count;

var containsKey = dictionary.ContainsKey(1);

var containsValue = dictionary.ContainsValue(customer1);

/// Iterate over keys

foreach (var key in dictionary.Keys)

Console.WriteLine(dictionary[key]);

// iterate over values

foreach (var value in dictionary.Values)

Console.WriteLine(value);

// Iterate over dictionary

foreach (var keyValuePair in dictionary)

{  Console.WriteLine(keyValuePair.Key);

Console.WriteLine(keyValuePair.Value);

}

Dictionary look-ups are so fast because they stores objects in an array internally, although they differ from a list, in the sense that objects are added  or removed at a particular  index using a hash function. Therefore, when we store an object in a dictionary, it will call the GetHashCode () method on the key of the object to calculate the hash. The hash is then adjusted according to the size of the array to calculate the index into the array to store the object. Later, when we lookup an object by its key, GetHashCode () method is used again to calculate the hash and the index. Looking at figure below, to store an object in a dictionary, the GetHashCode () method on the key is called. Let us take for example that it returns 1234\. This hash value is then adjusted based on the size of the internal array. In this picture below, size of the internal array is 6. So, the remainder of the division of 1234 by 6 is used to calculate the index (in this scenario 4). Later, when we need to look up this object, its key is used again to calculate the index.

![Hashtable in C#](d2d_images/image013.png)

This is just a simplified explanation of how hashing works.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# HashSet<T>

![image](d2d_images/chapter_title_below.png)

A HashSet are a set of unique items, just like a mathematical set (e.g. {1, 2, 3}). A hash set  must not have duplicates and the way in which the items are arrange is not important. Hence, both {1, 2, 3} and {2, 3, 1} are equal.

A HashSet is used when you need super-fast lookups against a list of unique items. For instance, you might be processing a list of orders, and for each order, you need to quickly check the supplier code from a list of valid supplier codes.

A HashSet, like a Dictionary, is a hash-based collection, there accessing items are very fast with O(1).But unlike a dictionary, it doesn’t store key/value pairs; it only stores values. Therefore, every objects should be unique and this is determined by the value returned from the GetHashCode () method. Therefore, if you are going to store custom types in a set, you need to override GetHashCode () and Equals () methods in your type.

To create a HashSet:

var hashSet = new HashSet<int>();

You can add or remove items to a HashSet just like List:

// Add an object to the set

hashSet.Add(4);

// Remove an object

hashSet.Remove(3);

// Remove all objects

hashSet.Clear();

// Check to see if the set contains an object

var contains = hashSet.Contains(1);

// Return the number of objects in the set And here are some other useful methods available in the Dictionary class:

var count = hashSet.Count;

HashSet provides many mathematical set operations:

// change the set to have only the objects present in the set and the other set

hashSet.IntersectWith(another);

// Remove all objects that found in another set other than this set from hashSet

hashSet.ExceptWith(another);

// change the set to contain all objects in itself, in some other set, or both

hashSet.UnionWith(another);

var isSupersetOf = hashSet.IsSupersetOf(another);

var isSubsetOf = hashSet.IsSubsetOf(another);

var equals = hashSet.SetEquals(another);

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Stack<T>

![image](d2d_images/chapter_title_below.png)

Stack has a Last-In-First-Out (LIFO) behavior.  Stacks are used in cases where there is need to provide the user with a way to go back. For example the browser.  When you surf different web sites, the URL addresses that you visit are pushed on a stack. Then, hence when the back button is clicked, the item on the stack (which represents the current URL address in the browser) is popped and now we can get the last address you visited from the item on the stack.  Another example is the undo feature in the applications; it is implemented using a stack.

Here is an example of how Stack can be used:

var stack = new Stack<string>();

// Push items in a stack

stack.Push("http://www.facebook.com");

// Check to see if the stack contains a given item

var contains = stack.Contains("http://www.facebook.com");

//Remove the first item on the top of the stack and remove it

var top = stack.Pop();

// Return the first item on the top of the stack

var top = stack.Peek();

// Get the number of items in stack

var count = stack.Count;

// Remove all items from stack

stack.Clear();

Also like dictionary and list, a stack is internally implemented using an array. However arrays in C# have a fixed size, so as you push items into a stack, there may be need to increase its capacity by re-allocating a larger array and copying existing items into the new array. But if there is no need for re-allocation, push is O(1) operation; otherwise, if re-allocation is required, presuming that the  stack has n elements, all these elements need to be copied to the new array. This has a runtime complexity of O(n).

Pop() method  is an O(1) operation.

Contains () method is a linear search operation with O(n).

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Queue<T>

![image](d2d_images/chapter_title_below.png)

Queue has a First-In-First-Out (FIFO) behavior. Queues are used in situations where there is need to process items as they arrive.

There are three main operations on queue and that include:

*   Enqueue: means  adding an element to the end of a queue
*   Dequeue:  which is used to remove the element at the front of the queue
*   Peek: is used to inspect the element at the front without removing it.

Example of how queue is used:

var queue = new Queue<string> () ;

// Add an item to the queue

queue.Enqueue("transaction1");

// Check to see if the queue contains a given item

var contains = queue.Contains("transaction1");

// Remove and return the item on the front of the queue

var front = queue.Dequeue();

// Return the item on the front without removing it

var top = queue.Peek();

// Remove all items from queue

queue.Clear();

// Get the total number of items in the queue

var count = queue.Count;

In conclusion, use lists when you need to access an item by index, but searching for an item in a list is quite slow because the search is a linear search.

Dictionaries provide fast access or lookups by key. Keys must be unique and cannot be null.

HashSets are great when you need fast access or lookups to check if an element exists in a set or not.

Stacks gives the LIFO (Last-In-First-Out) behavior and are beneficial when you need to provide the user with a way to go back.

Queues give the FIFO (First-In-First-Out) behavior and are beneficial for processing items in the order that they arrived.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Fifteen

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# C# Delegates

![image](d2d_images/chapter_title_below.png)

Delegates are objects that know how to call a method (or a group of methods) you can say that a delegate is a reference or a pointer to a function. Delegates are needed for designing extensible and flexible applications. Often this is used in design frameworks.

Delegates simply offers to the application user of your objects the ability to customize their behavior. However, there other ways to achieve this but delegates are the easiest way in some scenarios to achieve this.

Why do we need delegates?

❖  For designing extensible and flexible applications(e.g framework

❖  It  promotes code reusability

❖  It allows decoupling and generalization of code

❖  It also allows methods to be passed as parameters at runtime.

❖  Delegate provides the ability to specialize the behavior of a class without creating a subclass for that special behavior.

Let take a scenario to demonstrate how delegates work. Imagine you are developing a framework that will be for processing photos. You know that your application need to be extensible

You have define a class for different photo filters as shown below 

![image](d2d_images/image017.png)

And The code below is used to process photo by calling those filters

![image](d2d_images/image033.png)

What if you release the framework but  another developer wants to use the framework  and  apply another filter that you have not define in your code  the problem is you have  recreate that code , recompile and redeploy your code  and this could be very stressful if every time someone  need a feature  you haven’t added  you have to  keep recreating and redeploying your code and this is not the best .So with delegate we can make the application extensible such that a developer can  create their filters without relying on you. The same problem can also be solved using interfaces but here we are going to use delegates to solve this issue.

To use a delegate to make the code above extensible we need to define a delegate type, when defining a delegate we need to define the signature of the method. Now this delegate will be responsible for calling, is of type void, and takes in a parameter of photo like this

Public delegate void Photo FilterHandler(Photo  photo);.

The instance of this delegate can call a pointer to a function or a group of functions that have the signature

![image](d2d_images/image026.png)

Now to make the above method extensible instead of hardcoding these photos there. we get rid of it and pass a delegate to this method and call  instead  the object of the delegate  and pass the photo object as parameter  as shown below.

![image](d2d_images/image143.png)

And what it means that the above method process does not know what photo will be applied and is the responsibility of the user of this code to define whatever photo they want. Maybe a developer want to apply brightness or another wants to apply contrast to the photo. It is up to them. This framework need not to be recompile and redeploy as before.

Now the code below will be like the code the developer who want to use the framework will write. Developer will initiate object of your framework class, create the instance of the delegate, and point it to a method in PhotoFilters()

![image](d2d_images/image165.png)

So if I execute this code this will be the output

![image](d2d_images/image046.png)

We can easily change this code to apply another filter as shown below

![image](d2d_images/image050.png)

If we run the application, again we will get an output of two filters  like this

![image](d2d_images/image018.png)

Now if as a developer I want to create a filter that is not part of the framework, let say a filter to remove red eye.  I will simply add it to my code but the signature must be the same as that of the delegate and I will call my custom filter RemoveRedEyeFilter(Photo photo) just the same way I call the inbuilt filters in the framework as shown below

![image](d2d_images/image068.png)

When you run the application we will get this output

![image](d2d_images/image053.png)

Therefore, delegates are very powerful and allows us to create applications that are flexible and extensible. As you can see, I need not to change the PhotoFilter class in order to add RemoveEyeFilter method

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Sixteen

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Events

![image](d2d_images/chapter_title_below.png)

Event is a mechanism for communication between objects that means when something happens inside an object; event notifies other objects about that .one of the reason why we use event is to help in building loosely coupled applications and loosely coupled applications are easy to extend without breaking or changing one of its capability.

As software engineer, we want to build our application in such manner that if there is need to make changes to it the impact of that change will be minimal to the overall application.

Let take for instance that we have a VideoEncoder application that that encode a video and send it to the user via email as shown below

![image](d2d_images/image147.png)However, let say in the future we want to send a text message to the user. We can go ahead and add a few more line of codes to achieve that

![image](d2d_images/image107.png), but the problem here is that we may need to recompile VideoEncoder class and its dependencies and redeployed .in other to avoid this we can  use event to manage this scenario.

In using event, we can have the VideoEncoder Class to publish an event called sender and the Mail Service as event receiver as shown in this diagram.

![image](d2d_images/image078.png)

What is interesting about this arrangement is that the VideoEncoder knows nothing about mail service, which means in the future if want to extend our application and add SMS capability , we can simply create a new class of MessageService and have it  subscribe to VideoEncoder event  of the Video Encoder and VideoEncoder does not need to be recompile and redeploy.

![image](d2d_images/image000.png)

Since VideoEncoder Class knows absolutely nothing about the Mail Service or the MessageService Class, how does VideoEncoder notifies the subscribers? Well for that notification to happen it needs to send a message to them .in practical coding terms it needs to invoke a method that will send out that notification. Hence, for VideoEncoder to know what method to call since it is ignorance of the existence of MailService or MessageService class, there is usually an agreement between the publisher and the subscribers that will be the mode of communication between them, it is a method with a specific agreed signature. This method is often called event handlers. The publisher calls that method when the event is raised so we need a method like that in MailService and MessageService class. So that when the VideoEncoder needs to notify subscribers it will called this method

![image](d2d_images/image106.png)

The name of this method does not matter but the signature must be same

![image](d2d_images/image004.png)

Remember again that VideoEncoder is not aware of MailService or MessageService class. It is decoupled from them all it knows is a method with the agreed signature. So how do we tell VideoEncoder which method to call that is either to send mail or SMS? This is where a delegate comes in; delegates represent the agreement or the contract between the publisher and the Subscriber and determine the signature of the event handler method in the subscriber.

.let looks at the piece of code to implement this. Let assume we have two classes Video.cs and the VideoEncoder.cs. And the program.cs

![image](d2d_images/image098.png)T

The video class just have a property Title. For the title of that video

In addition, in the VideoEncoder class, to give it the ability to publish an event, we need to define a delegate, define an event on that delegate and raise the event. It will also have a method that encode the video as shown below

![image](d2d_images/image182.png)

Therefore, in the program.cs we have the MailService class with a method that has the agreed signature OnVideoEncoded and is type void. Here also we subscribe the MailService to the VideoEncoder event of the VideoEncoder.

![image](d2d_images/image076.png)

We are done so when we run this we will get

![image](d2d_images/image054.png)

Now if we want to send Text message, we simply define a class MessageService with a method with the same signature that the MailService has

![image](d2d_images/image141.png)

So in the program.cs we will instantiate it and call the event as we did in mail service

![image](d2d_images/image014.png)

This is the output

![image](d2d_images/image083.png)

The beauty of this is that I need not to change anything in the VideoEncoder class in order to send text messages instead of mail. With events you can create publishers and add subscribers without changing the publisher

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Seventeen

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Lambda Expressions

![image](d2d_images/chapter_title_below.png)

A Lambda Expression is just an anonymous method that has no access modifier (public or private), no name and no return statement. We use them for convenience, by writing less code and achieving the same result. In addition, make the code more readable.

For example, let say we want to write a method that takes a number and return the square of the number. Typically, this is how we will write it as shown below

![image](d2d_images/image183.png)

This should return 25.

Now with lambda expression we can achieve the same thing but with less code

The syntax for lambda expression is args = > expression

We read this as args goes to some expression. Therefore, we can write the square method above with lambda expression, assign it to a delegate, and then call the delegate as shown below

![image](d2d_images/image150.png)

If we run this, it will give the same result as the previous one, which is 25

If we do not need any arguments in lambda expression, it could be written like this

//() => ....

And if we have one argument it can be used like this

// x =>...

If we have multiple arguments, it should be surrounded by parenthesis

// (x, y, z) => .....

In terms of scope, the square lambda expression above has access to the parameters passed and as well as all the variables defined within the static void Main (string [] args) method where it is defined

Let see another example, I create a method that takes a number and multiplies it by the constant factor as shown below

![image](d2d_images/image129.png)

Using Lambda Expressions with Anonymous Types

Let say we have a class called Book repository that is responsible for returning a list of book from the database  so in this clas we have a method GetBooks of type generic List that returns a list of books as shown below

![image](d2d_images/image127.png)

and l we can write a code that returns all the cheap book below 10 dollars using lambda expression as shown below

![image](d2d_images/image094.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Eighteen

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Extension Methods

![image](d2d_images/chapter_title_below.png)

Extension Methods are used to add methods to an existing class without changing its source code or creating a new class that inherits from it.  This also work in sealed classes.

To create an extension class we use the static modifier, the name of the class you want to extend and to create the extension method, it has to be a static method in a static class with the first argument being the  this keyword . Look at the example below we created a static class with a name StringExtension and created a static method of type string and the name is shorten with the first argument this String str and int numberOfWords.

![image](d2d_images/image138.png)

The above extension class helps you to shorten your strings.

Let see how to use this class in the Program.cs.

![image](d2d_images/image058.png)

When to Use Extension

Use an extension method only when you have to that is when its functionality is important to the extended type.

Use it on interfaces to add generic functionality to classes that do not have a common base class like in the case of LINQ methods being extension methods to IEnumerable interface

Use extension method when dealing with classes that are not created by you like a class from a 3^(rd) party application or library  for instance extending FileInfo from .Net Framewok

The major difference between the extension method and other static methods is the This keyword that it must have as the first parameter in the method.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Nineteen

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# LINQ

![image](d2d_images/chapter_title_below.png)

LINQ stands for Language Integrated Query. It is one the features that came with C# 3.0

It gives you the capability to query objects in C# natively. With LINQ, you can query Objects in memory, e.g. collections (LINQ to Objects), databases (LINQ to Entities), XML (LINQ to XML), ADO.Net Data Sets (LINQ to Data Sets)

Let see LINQ in actions, let see a simple BookRepository class with two properties Title and price and a method called GetBooks that return I Enumerable of book

![image](d2d_images/image154.png)

In our program.cs ,we simply  instantiate the  BookRepository and call the GetBooks  let say we want to display the  books that are cheaper  than 10 dollars, without using LINQ, we will need to iterate through  the book collection  to get those that meet the condition  and iterates through selected list and  display as shown below

![image](d2d_images/image163.png)

The output will be

![image](d2d_images/image128.png)

But with LINQ we can get rid of the above code and use a fewer lines of code to achieve the above as shown below the yellow painted code shows how LINQ is used in where clause a lambda expression is used to determine those books that are cheaper than 10 dollars

![image](d2d_images/image148.png)

The same output will be given

![image](d2d_images/image052.png)

LINQ also has another method called OrderBy and we can chain LINQ methods together as we can use this OrderBy () method to order the list of books by Title.

![image](d2d_images/image077.png)

Noted that the  list is now sorted by title

![image](d2d_images/image070.png)

LINQ also have another powerful method called Select (). Which is used for projections and transformations. Let say in this our example we to iterates through a list of book and convert it to another object or select one of its property as a string. And output just the title of the books

![image](d2d_images/image179.png)

The output will title of the books

![image](d2d_images/image008.png)

There are two ways to write a LINQ Query

One is using LINQ Extension method like this

![image](d2d_images/image116.png)

The second is using LINQ Query Operators like

![image](d2d_images/image022.png)

The LINQ Query Operators always start with the from and always finish with the select

These two examples will achieve the same result and give the same output.. so the choice on which one to use  just depend on you. It is a personal choice.

Other LINQ Extension methods that make your coding easier. .

Let say I want to get a book with a particular Title I can use the Single () method to achieve this

![image](d2d_images/image063.png)

And when we are not sure if that object exist we can use SIngleOrDefault() method to avoid our  application from crashing  because the default null will be returned .

![image](d2d_images/image030.png)

We use First () to get the first element in the list. And you can use the FirstOrDefault() when  you are not sure if such element exist

![image](d2d_images/image110.png)

We also have Skip() and Take ().. Here in our example we can decide to skip the first two books and return the last three.

![image](d2d_images/image032.png)

We also have a bunch of aggregate functions in LINQ just like in SQL like Count (), Max(), Sum(), Min() etc .

![image](d2d_images/image043.png)

This returns the highest price and the lowest price

![image](d2d_images/image031.png)

This return the total number of books in the list

The beauty of LINQ is that whether you query objects from memory, databases or XML. You keeping using LINQ like this without having to learn Transact SQL for instance to query databases

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Twenty

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Nullable Types 

![image](d2d_images/chapter_title_below.png)

As you know in C#, a value type cannot be null. For example, if you define a bool it can have either a True or False.

bool hasAcess = true; // or false

But there are some situations that you will like to cater for null values, let say you are  working with the database and  you have a table called customers  and a column called Birth Date  which  is type datetime and can be  null; because not everyone will like to put their  birth date. In that case, if you want to map that table to a C# class, you will need a nullable type to do that.

Any Datatype can be declared nullable using the operator "?"

Let see Nullable in action  here we have a nullable DateTime object  assigned a date and to  assing a value type DateTime object  date2  we call a method GetValue Or Default() in the DateTime Library so that  if the  nullable date is null a default value will be assigned to  the date2  without  our application crashing.

![image](d2d_images/image113.png)

Ok let talk about Null Coalescing Operator which is represented using ??

![image](d2d_images/image092.png)

What the above code means is that if date is not null assign date to date2 if not assign it the value of DateTime.Today .  This is a short way of writing the if/ else conditional statement or even the ternary operator method when checking for null value

Note that that you cannot have an operation between a nullable type and the value type because they are not compatible f or example if you have the following code int? k=4;

Int s=3;

Int z = k * s;

Console.WriteLine(z.ToString());

Console.ReadLine();

This will generate an error telling you that “cannot implicitly convert type int?  to int . (Are you missing a cast?)”

In this scenario to avoid the above error you may need to declare the entire variable as nullable

int? k=4;

Int ?s=3;

Int ?z = k * s;

Console.WriteLine(z.ToString());

Console.ReadLine();

This time you get no error and the output will be given.

For recap, these are features of Nullable Types or point to note about Nullable Type

❖  Nullable types are only used with value types.

❖  An InvalidOperationException will be thrown if value is null; otherwise, it will return the value.

❖  The HasValue property returns a value of either true if the variable contains a value, or false if it is null.

❖  Use == and! = operators with a nullable type. For other comparison, use the Nullable static class.

❖  Nesting nullable types in a code are not allowed. For example Nullable<Nullable<float>> k; will give a compile time error.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Twenty-One

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Dynamics  

![image](d2d_images/chapter_title_below.png)

Dynamics are one of the features that came with C# 4.0 that sometimes confuses some of the C# developers. However, it is actually easy. Usually Programming languages are divided in to statically – typed Languages like C#, Java and dynamically – typed Languages like Ruby, JavaScript, and Python. Now what is really the difference between these two? The difference is that in static languages resolution of types, members, methods, properties are done at compile time. Where in the dynamic languages  the resolution of type, methods, property or members are done at run time

The benefit of static languages is early feedback at compile time while the benefit of  dynamic languages is that they are easier and faster to code with. However, on the other side we have to write more unit test to ensure that the code is working properly.

C# started as a static language but. .Net Framework 4.0, they added dynamics capability in order to improve interoperability with

.COM (examples are writing office applications that uses Excel or Word) and  or dynamic languages in .Net like Iron Python

As we said before a dynamic type resolves its type at run time based on the value of the expression at runtime.

Look at the following code

static void Main(string[] args)

{

dynamic a = 100;

Console.WriteLine("Dynamic a value: {0}, Type: {1}",a ,a.GetType().ToString());

a = "Hello World!”;

Console.WriteLine("Dynamic a value: {0}, Type: {1}", a, a.GetType().ToString());

a = true;

Console.WriteLine("Dynamic a value: {0}, Type: {1}", a, a.GetType().ToString());

a = DateTime.Now;

Console.WriteLine("Dynamic a value: {0}, Type: {1}", a a.GetType().ToString());

}

Output:

Dynamic a value: 100, Type: System.Int32

Dynamic a value: Hello World!!, Type: System.String

Dynamic a value: True, Type: System.Boolean

Dynamic a value: 01-01-2014, Type: System.DateTime

For Methods and Properties of Dynamic Type

Let say you assign a class object to a dynamic type, the compiler is not going to throw any exception or check if the correct method or property s of the dynamic  type that holds that  custom class  until at  runtime because  by assigning it a dynamic type , you are instructing the compiler that  the variable type  can change  or that it is not known until  runtime 

Look at the following example

public class Staff

{

public int StaffID { get; set; }

public string StaffName { get; set; }

public int Age { get; set; }

public int StandardID { get; set; }

public void DisplayStaffDetail()

{

Console.WriteLine("Name: {0}", this.StaffName);

Console.WriteLine("Age: {0}", this.Age);

Console.WriteLine("Standard: {0}", this.StandardID);

}

}

class Program

{

static void Main(string[] args)

{

dynamic dynamicStaff = new Staff();

dynamicStaff. DisplayStaffDetail();

dynamicStaff.CreateStaff();

}

}

If you look at the above code you will see that there is no place where we define the  method CreateStaff() , however the compiler will not give any error  because it will skips type checking  because it is dynamic type  but at runtime we will have runtime error.

Using Dynamic Type as a method Parameter

When a method have a dynamic type as its parameter, it can accept any type of parameter at run time.

Look at the following codes

class Program

{ 

static void PrintValue(dynamic obj)

{

Console.WriteLine(obj);

}

static void Main(string[] args)

{

PrintValue(“Hello World!!”);

PrintValue(100);

PrintValue(100.50);

PrintValue(true);

PrintValue(DateTime.Now);

}

}

Output:

Hello World!

100

100.50

True

01-01-2014 10:10:50

Note these about dynamic type:

❖  Dynamic types are resolved at runtime and not at compile time.

❖  The compiler does not do type checking for dynamic type. Therefore, it does not give any error about dynamic types at compile time.

❖  Dynamic types actually shows no intellisense support in visual studio.

❖  A method can have dynamic type as its parameter or one of its parameter.

❖  if a method or property is not compatible at runtime, an exception is thrown.

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Twenty-Two

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Exception Handling  

![image](d2d_images/chapter_title_below.png)

In C#, we use exception handling to deal with unexpected or exceptional situation that arise from the program we write. As C# developers, we need to learn how to handle exceptions effectively.

Let see an example let say we have a calculator class  with a method Divide that gets two arguments and return their division result like this

![image](d2d_images/image025.png)

In the program.cs we will instantiates the object of the calculator class and call the method Divide() and pass 5 as the numerator  and 0  as the  denominator . We expect a division by zero exception. Essentially exception is a class .Net

![image](d2d_images/image115.png)

When we run the application, it will crash

![image](d2d_images/image016.png)

![image](d2d_images/image169.png)

To avoid this from happening we need to handle such exceptions by using Try and Catch blocks. You put the code that is likely to throw an exception inside the Try block, so when an exception is thrown the catch block will be executed. However if there are no exceptions the catch block will not be executed.

![image](d2d_images/image111.png)

So when we run it again

![image](d2d_images/image136.png)

This is better than our application crashing.

So as a guideline we should always have a global Try {} catch () block in our application.

Let take a closer look at the catch block in our example we just have a type Exception and it is the parent of all the exceptions in .Net  it is good to have an argument so that we access the actual exception. In addition, we can have more than one catch block.  We can define specific exception like in our case DivideByZero Exception and you must start from the specific exception to the most generic or parent exception class

![image](d2d_images/image155.png)

The output will show that the first catch is executed which is the specific exception to the scenario so the other two need not to be executed 

![image](d2d_images/image177.png)

In C# we also have a finally block which is used to handle any exceptions that are thrown  by classes that mange resources that are not handle in CLR, hence no garbage collections are applied to them  examples are database connections, network connections etc. so in situations like that a manual cleanup  is  done .

![image](d2d_images/image069.png)

Even if there are no exceptions, the finally block will always be executed. Note also that we used the throw keyword, it is actually use to create a new exception like used in the above code within a try catch finally block

Creating Custom Exceptions

Custom or user defined are derived from the Exception class.  Look at the following example

using System;

namespace CustomDefinedException {

class TemperatureCheck {

static void Main(string[] args) {

Temperature temp = new Temperature();

try {

temp.showTemp();

} catch(TempIsZeroException e) {

Console.WriteLine("TempIsZeroException: {0}", e.Message);

}

Console.ReadKey();

}

}

}

public class TempIsLessThanZeroException: Exception {

public TempIsLessThanZeroException (string message): base(message) {

}

}

public class Temperature {

int temperature = 0;

public void showTemp() {

if(temperature == 0) {

throw (new TempIsLessThanZeroException ("Zero Temperature found"));

} else {

Console.WriteLine("Temperature: {0}", temperature);

}

}

}

When this code is compiled and executed, the output will be

TempIsLessThanZeroException: Zero Temperature found

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Chapter Twenty-Three

![image](d2d_images/chapter_title_below.png)

| ![image](d2d_images/chapter_title_corner_decoration_left.png) |  | ![image](d2d_images/chapter_title_corner_decoration_right.png) |

![image](d2d_images/chapter_title_above.png)

# Asynchronous Programming

![image](d2d_images/chapter_title_below.png)

If you have been designing and writing web application for a long time, then there is a high probability that you must have encountered a lot of bad response time of web applications.  Before AJAX, it is nearly impossible to change a small portion of content without reloading the entire page .The scenario is made worse with a slow internet connection. However, these days, the situation has changed. We can do make any changes without reloading an entire page or without touching another element. Hence, there is an increase in performance and the user's experience. So, how is it done? You are could be thinking AJAX, right? Yes, Ajax is an asynchronous technique to exchange data between the server and the client. Therefore, the major aim of AJAX is to call a server method and exchange data from the server without obstructing any activity that is being carried out by the client. Therefore, clients need not wait for the server's response.

. In C # 5.0, Microsoft introduced asynchronous programming which has given C# Developers, the opportunity to write our own asynchronous code with C#.

Synchronous and Asynchronous Programming?

In synchronous execution model, program is executed line by line, one at a time. When a function is called, and program execution has to wait until the function returns.

For Asynchronous program, when a method is called, program execution continues to the next line, without waiting for the function to complete. Asynchronous programming improves responsiveness for example, in the window media player, when you are playing your video or music. The UI is designed to be responsive, you can resize your window, you can move it around even as your video or music is playing and this is because it is  programmed asynchronously otherwise as you try to move it around the window will freeze.. The same time with your web browser as you download contents from the web the UI is still functioning. It is responsive and that is the benefit of the Asynchronous programming.

When to Use Asynchronous

It is best used if you have blocking operations such as accessing the web, working with files and databases or working with images

How do we use asynchronous technique in our applications?

In C #, we have two common Traditional approaches before .Net 4.5 and that is Multithreading and Callbacks methods  all these approaches are hard and complex to learn. Therefore, in .Net 4.5 Microsoft introduced a new Asynchronous programming model, which was called Task base asynchronous model. There are two major keywords that is used to achieve this asynchronous programming; they are called Async and Await.

Async

This keyword qualify a function as an asynchronous function. Therefore, if a function has async specified in its front, then that function is asynchronous. Look at the syntax for asynchronous method.

Public async Task DrawProcess()

{

}

Here the DrawProcess() method is an asynchronous method because the async keyword is in front of it. Hence, it can be called asynchronously. It also have a return type called Task.. A task is an object that encapsulate a state of an asynchronous operation. It comes into two forms one is of generic form and non-generic forms.

The DrawProcess() method shows the non-generic  form which  means that  it returns void . However, if the method is going to return let say a string, it will use the generic form like this Task <string>

Await

When calling a method that returns the Task<string> we need to put the keyword await in front of the method

It sounds like waiting right. or gives you the impression that the program execution has to wait until the method is executed?  No, putting await operator in front of an  asynchronous  method  is just telling the compiler ,that this operation is a costly one and may take a bit of time to execute. In that case, instead of blocking this thread, it will simply return the control immediately to the caller of the method, so the thread here is not  going to be locked and immediately the control returns to method to continue executing

This is exactly the scenario in the example below; this is window form application that on clicking a button, a HTML page is downloaded. We are using async method to ensure that during the download the window does not freeze and is responsive or can be moved from one place to another on the screen.  since we marked DownloadStringTaskAsync(url) with await operator , the method will be return immediately to the Button_Click() event that  called the  method , eventually when the DownloadStringTaskAsync(url)  has finish executing  control will be  returned to async method DownLoadAsync() to continue execute the rest of the code  which in this case is the StreamWriter. You will also observe that for every synchronous method in the .net Library, there is corresponding an asynchronous method. for instance in our example  the WebClient object called the TaskAsync  method  for  DownloadString() and the StreamWriter called WriteAsync() which  is the  Asynchronous method for the  Writer() which is  a blocking operation or synchronous  way to write .  The idea here is improve the responsiveness of the application and ensure it is asynchronous in its execution ![image](d2d_images/image173.png)

For recap, recall that the return type of an asynchronous function is Task.  That means when it finishes its execution it will complete a Task. The possible return types for an asynchronous method are

Void: Means there is nothing to return

Task: It will perform one operation, and like void, it return nothing

Task<T>: Will return a generic task with a T type parameter. (Which can be string, int or any other data type)

Points to Note

❖  A Main method cannot be asynchronous.

❖  In addition, Main method cannot be invoked by the await operator.

❖  If any asynchronous method is not invoked by the await operator then by nature it will behave like a synchronous method.

❖  Function properties should not be defined as asynchronous.

❖  A try/catch block should not call any asynchronous methods from the catch or finally block.

❖  A class constructor or destructor should not define an asynchronous method nor should be called asynchronously.