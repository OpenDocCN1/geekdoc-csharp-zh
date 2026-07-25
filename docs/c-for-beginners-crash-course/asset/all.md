![](Images/cover00332.jpeg)

C#

For Beginners

Crash Course

Master C# Programming

Fast and Easy Today

By

Raj Ali

© Copyright 2014 - All rights reserved.

In no way is it legal to reproduce, duplicate, or transmit any part of this document in either electronic means or in printed format. Recording of this publication is strictly prohibited and any storage of this document is not allowed unless with written permission from the publisher. All rights reserved.

The information provided herein is stated to be truthful and consistent, in that any liability, in terms of inattention or otherwise, by any usage or abuse of any policies, processes, or directions contained within is the solitary and utter responsibility of the recipient reader. Under no circumstances will any legal responsibility or blame be held against the publisher for any reparation, damages, or monetary loss due to the information herein, either directly or indirectly.

Respective authors own all copyrights not held by the publisher.

Legal Notice:

This book is copyright protected. This is only for personal use. You cannot amend, distribute, sell, use, quote or paraphrase any part or the content within this book without the consent of the author or copyright owner. Legal action will be pursued if this is breached.

Disclaimer Notice:

Please note the information contained within this document is for educational and entertainment purposes only. Every attempt has been made to provide accurate, up to date and reliable complete information. No warranties of any kind are expressed or implied. Readers acknowledge that the author is not engaging in the rendering of legal, financial, medical or professional advice.

By reading this document, the reader agrees that under no circumstances are we responsible for any losses, direct or indirect, which are incurred as a result of the use of information contained within this document, including, but not limited to, —errors, omissions, or inaccuracies.

Table of Contents

[Chapter 1 Introduction to C#](#part0000.xhtml__Toc422767436)

[1.1 Overview of C#](#part0000.xhtml__Toc422767437)

[1.2 Programming features of C#](#part0000.xhtml__Toc422767438)

[1.3 C# Environment](#part0000.xhtml__Toc422767439)

[Components of .NET framework](#part0000.xhtml__Toc422767440)

[Chapter 2 Program Structure in C#](#part0000.xhtml__Toc422767441)

[2.1 Introduction to C# Program structure](#part0000.xhtml__Toc422767442)

[Namespace declaration](#part0000.xhtml__Toc422767443)

[Class](#part0000.xhtml__Toc422767444)

[Class Methods](#part0000.xhtml__Toc422767445)

[Comments](#part0000.xhtml__Toc422767446)

[2.2 User Interface elements](#part0000.xhtml__Toc422767447)

[Start Page](#part0000.xhtml__Toc422767448)

[Standard Toolbar](#part0000.xhtml__Toc422767449)

[Solution Explorer](#part0000.xhtml__Toc422767450)

[Output window](#part0000.xhtml__Toc422767451)

[Error List](#part0000.xhtml__Toc422767452)

[Class View Window](#part0000.xhtml__Toc422767453)

[Code Editor](#part0000.xhtml__Toc422767454)

[2.3 Compiling and executing C# program](#part0000.xhtml__Toc422767455)

[Chapter 3 Syntax, Data Types, and conversion](#part0000.xhtml__Toc422767456)

[3.1 Different keywords in C#](#part0000.xhtml__Toc422767457)

[1) Keywords for class, method, field and property](#part0000.xhtml__Toc422767458)

[2) Keywords for type conversions](#part0000.xhtml__Toc422767459)

[3) Keywords useful for program flow control](#part0000.xhtml__Toc422767460)

[4) Keywords used for built in types and enumerations](#part0000.xhtml__Toc422767461)

[5) Keywords used for exception handling](#part0000.xhtml__Toc422767462)

[6) Keywords used as literals, method passing parameters](#part0000.xhtml__Toc422767463)

[7) Keywords useful in function pointers, object allocation, unmanaged code](#part0000.xhtml__Toc422767464)

[3.2 Data Types in C#](#part0000.xhtml__Toc422767465)

[3.3 Type conversion in C#](#part0000.xhtml__Toc422767466)

[Implicit type conversion](#part0000.xhtml__Toc422767467)

[Explicit type conversion](#part0000.xhtml__Toc422767468)

[Chapter 4 Variables and Constants](#part0000.xhtml__Toc422767469)

[4.1 Exploring variables in C#](#part0000.xhtml__Toc422767470)

[4.2 Constants and literals in C#](#part0000.xhtml__Toc422767471)

[Chapter 5 Operators in C#](#part0000.xhtml__Toc422767472)

[5.1 Introduction to operators](#part0000.xhtml__Toc422767473)

[5.2 Arithmetic operators](#part0000.xhtml__Toc422767474)

[5.3 Relational operators](#part0000.xhtml__Toc422767475)

[5.4 Logical operators](#part0000.xhtml__Toc422767476)

[5.5 Bitwise operators](#part0000.xhtml__Toc422767477)

[5.6 Assignment operators](#part0000.xhtml__Toc422767478)

[5.7 Miscellaneous operators](#part0000.xhtml__Toc422767479)

[Chapter 6 C# Decision making statements](#part0000.xhtml__Toc422767480)

[6.1 If Statement](#part0000.xhtml__Toc422767481)

[6.2 If else statement](#part0000.xhtml__Toc422767482)

[6.3 Nested if statement](#part0000.xhtml__Toc422767483)

[6.4 Switch statement](#part0000.xhtml__Toc422767484)

[6.5 Nested switch statement](#part0000.xhtml__Toc422767485)

[Chapter 7 Loops in C#](#part0000.xhtml__Toc422767486)

[7.1 While loop](#part0000.xhtml__Toc422767487)

[7.2 For loop](#part0000.xhtml__Toc422767488)

[7.3 Do while loop](#part0000.xhtml__Toc422767489)

[7.4 Break statement](#part0000.xhtml__Toc422767490)

[7.5 Continue statement](#part0000.xhtml__Toc422767491)

[Chapter 8 Classes and Methods in C#](#part0000.xhtml__Toc422767492)

[8.1 Class declaration](#part0000.xhtml__Toc422767493)

[C# constructors](#part0000.xhtml__Toc422767494)

[C# destructors](#part0000.xhtml__Toc422767495)

[8.2 Defining methods](#part0000.xhtml__Toc422767496)

[8.3 Calling methods](#part0000.xhtml__Toc422767497)

[8.5 Recursive method call](#part0000.xhtml__Toc422767498)

[8.4 Passing parameters to method](#part0000.xhtml__Toc422767499)

[Chapter 9 Arrays in C#](#part0000.xhtml__Toc422767500)

[9.1 Introduction to arrays](#part0000.xhtml__Toc422767501)

[9.2 Arrays declaration](#part0000.xhtml__Toc422767502)

[9.3 Initializing and adding values](#part0000.xhtml__Toc422767503)

[9.4 Accessing array elements](#part0000.xhtml__Toc422767504)

[9.5 Foreach loop](#part0000.xhtml__Toc422767505)

[9.6 Different C# arrays](#part0000.xhtml__Toc422767506)

[Chapter 10 Strings in C#](#part0000.xhtml__Toc422767507)

[10.1 Creation of string](#part0000.xhtml__Toc422767508)

[10.2 Properties and methods of string class](#part0000.xhtml__Toc422767509)

[10.3 Examples demonstrating the string functionality](#part0000.xhtml__Toc422767510)

[Chapter 11 Encapsulation and Polymorphism](#part0000.xhtml__Toc422767511)

[11.1 Introduction to encapsulation](#part0000.xhtml__Toc422767512)

[11.2 Access specifier in C#](#part0000.xhtml__Toc422767513)

[11.3 Polymorphism](#part0000.xhtml__Toc422767514)

[11.4 Static Polymorphism](#part0000.xhtml__Toc422767515)

[11.5 Dynamic Polymorphism](#part0000.xhtml__Toc422767516)

[Chapter 12 Inheritance and Interfaces](#part0000.xhtml__Toc422767517)

[12.1 Introduction to Inheritance](#part0000.xhtml__Toc422767518)

[12.2 Base and derived classes](#part0000.xhtml__Toc422767519)

[12.3 Base class initialization](#part0000.xhtml__Toc422767520)

[12.4 Interfaces in C#](#part0000.xhtml__Toc422767521)

[12.5 Multiple inheritance in C#](#part0000.xhtml__Toc422767522)

[Chapter 13 Operator overloading and exception handling](#part0000.xhtml__Toc422767523)

[13.1 Introduction to Operator Overloading](#part0000.xhtml__Toc422767524)

[13.2 Different operators in overloading](#part0000.xhtml__Toc422767525)

[13.3 Introduction to exception handling](#part0000.xhtml__Toc422767526)

[13.4 Exception classes in C#](#part0000.xhtml__Toc422767527)

[13.5 Exception handling](#part0000.xhtml__Toc422767528)

[13.6 User defined exceptions](#part0000.xhtml__Toc422767529)

[Chapter 14 Multithreading](#part0000.xhtml__Toc422767530)

[14.1 Thread in C#](#part0000.xhtml__Toc422767531)

[14.2 Life cycle of a thread](#part0000.xhtml__Toc422767532)

[14.3 Main thread](#part0000.xhtml__Toc422767533)

[14.4 Properties and methods of the Thread class](#part0000.xhtml__Toc422767534)

[14.5 Creating and managing threads](#part0000.xhtml__Toc422767535)

[14.6 Destroying threads](#part0000.xhtml__Toc422767536)

[Reference links on C#](#part0000.xhtml__Toc422767537)

[Conclusion](#part0000.xhtml__Toc422767538)

Chapter 1 Introduction to C#

## 1.1 Overview of C#

C# is an object oriented, type safe high level programming language. It has been developed by Microsoft during the development of the .NET framework. C# was developed for the Common Language Infrastructure (CLI), this infrastructure was created to allow programs from various other high level languages to work together without the need to rewrite those programs entirely. The CLI contains a various executable programs referred simply as executables and are housed and ran in a system called the runtime environment.

All the programs created in .Net framework execute in an environment that handles the runtime requirements. The Common Language Runtime (CLR) provides the virtual machine, which helps the programmers not to consider the CPU specifications. The class library and CLR make the .NET framework.

## 1.2 Programming features of C#

*   It is simple, advanced, object oriented language
*   It contains data types and classes common for all the .NET languages
*   The Common Language Runtime (CLR) is similar to the Java Virtual Machine (JVM)
*   C# provides support for encapsulation, inheritance, polymorphism, and interfaces
*   Visual Studio provides support to VC++, Visual Basic, Vbscript, and Jscript
*   .NET consists of class library and common execution engine
*   Garbage collection, automatic memory management, interoperability are inbuilt in C#
*   User can develop console, windows and web applications using C#

## 1.3 C# Environment

C# is a part of .NET framework. It is used for creating .NET applications. Using .NET framework, user can design, deploy and develop the applications. Robust applications can be easily built using the simple programming model.

### Components of .NET framework

The .NET framework diagram containing several components is as shown:

![](Images/image00304.jpeg)

The .NET framework consists of the following components:

*   Common Language Runtime
*   .NET framework base class library
*   Common Language Specification
*   User and Program interfaces

Common Language Runtime (CLR)

The core component of the .NET framework is the CLR. It is an environment where the programs are executed. The code in CLR is translated into Intermediate Language (IL). This IL code is then used across different platforms.

The IL code is converted into machine language by the Just in Time (JIT) compiler. The complier checks for the type safety. This ensures objects are accessed in a compatible way.

.NET framework class library

The class library works with any .NET languages like VB.NET, VC# and VC++.NET. The library provides classes used in the code for performing different programming tasks like data collection, string management, file access and connecting to the database.

Common Language Specification

CLR contains set of common rules used by all the programming languages in .NET framework. They are known Common Language Specification (CLS). CLS helps an object to interact with objects or applications of other languages.

User and Program Interfaces

.NET framework provides three different types of user interfaces:-

*   Windows Forms: They are windows based applications.
*   Web Forms: They are used for creating web based applications.
*   Console Applications: They are useful for creating console based applications which are executed by the command line.

Chapter 2 Program Structure in C#

## 2.1 Introduction to C# Program structure

C# Program consists of various parts. We shall explore all the components needed for a C# program.

Consider the code demonstrating the C# program.

| ![](Images/image00305.jpeg)Example 1: |
| using System;namespace welcomepublic  class WelcomeUser{ static  void Main(  string[] args) {        Console.WriteLine("WelcomeUser");        Console.Read(); }} |

The code consists of several parts. They are as mentioned below:

### Namespace declaration

The namespace consists of collection of classes used in programming. Theusing  keyword is used for adding the System namespace. The System class consists of classes and methods useful for the user.

In the above code, namespace welcome is added.

### Class

The class consists of data and method definitions used by the program. The class can have one or many methods. Every class must have a Main method, which is the first method run in the code. In the above code, WelcomeUser class is declared.

### Class Methods

Methods in a class specify the behavior of the statement. In the above code, WriteLine method is used for writing the value in the console. It is defined in the Console class inside the  System namespace.

The Read method of the Console class is used for waiting till the user hits a key. Thus prevents the screen from closing too quickly.

### Comments

Comments are text useful for providing additional information about the code. The compiler ignores any code that is placed inside a comment block. There are two types of comments; one comment is used for single line entries and the other for multi line entries.

For example:

| ![](Images/image00305.jpeg)Example 2: |
| using System;namespace comment/*It is a simple codeUsed for writing value to the console*/class Demo{ static  void Main() { //It is added inside Main method        Console.WriteLine("Demonstration of code"); }} |

## 2.2 User Interface elements

There are various user interface elements present in the Visual Studio application that can be used in a project. We shall explore the user interface elements in detail.

### Start Page

The Start Page is the initial page that gets displayed when the user opens the Microsoft Visual Studio application.

![](Images/image00306.jpeg)

The Visual Studio IDE provides the start page as the default home page. Through the start page user can specify the preferences, developer communication using the .NET platform, exploring new .NET features.

In Visual Studio .NET, the Projects tab displays the recent projects and the latest modification date. User can use any of the existing projects from the list. Click on the New Project button when you need to work for a new project. Click on the Open project button when user wants to open the existing project.

### Standard Toolbar

The standard toolbar is used to provide the shortcut menu commands. There are several buttons on the toolbar that help user to perform tasks related to opening, closing, saving, editing, pasting on the file.

There are functions related to the tools present in the standard toolbar. They are as listed below.

*   New Project: A new project can be created in the application. The ![](Images/image00307.gif)button is used.
*   Add New Item: A new item is added to the project. The ![](Images/image00308.gif)button is used
*   Save: All the programs created in a particular solution are saved. The ![](Images/image00309.gif) button is used
*   Save All: It saves all the unsaved items in an application. The ![](Images/image00310.gif) button is used

*   Cut: The selected objects are placed on the clipboard using this option. The ![](Images/image00311.gif)icon is used
*   Copy: The copy of the selected item is kept on the clipboard. The ![](Images/image00312.gif) icon is used
*   Paste: It is used to paste the contents in the document. The ![](Images/image00313.gif) icon is used
*   Debugging: The compilation and execution of the project is done. The ![](Images/image00314.gif) icon is used.

### Solution Explorer

In the solution explorer window, classes, project and solution name used in the project gets displayed. Double click the file in the solution explorer for opening the file.

The following figure shows the solution explorer window in application.

![](Images/image00315.jpeg)

### Output window

The messages for the status of the features of Visual Studio .NET IDE are provided by the output window. The current status of the application is displayed when the user compiles it. The number of errors present during compilation is displayed in the window. The View -> Output Window option is used to open the window.

The following figure shows the output window in Visual Studio application.

![](Images/image00316.jpeg)

### Error List

The list of errors present in the application is displayed in the error list window. The user can locate errors as soon as the code is compiled. Double click the error and the source for it is located. Click View, Error List Window option to open the error list window.

The following figure shows the error list window.

![](Images/image00317.jpeg)

### Class View Window

The class view window is useful in displaying classes, properties and methods associated with a file. The tree view structure is used to display the items. The code editor window can be viewed by double clicking the item.

The window contains two buttons, one for sorting the items, other for new folder creation. The View, Class View option is used for opening the class view window.

![](Images/image00318.jpeg)

### Code Editor

User can enter or edit code in the code editor. User can add code to the editor for the class.

The following window shows the code editor.

![](Images/image00319.jpeg)

## 2.3 Compiling and executing C# program

There are some steps involved in compiling and executing the program as mentioned below:

1) Open Visual Studio application

2) Click File, New, Project option from the list

3) Select the Visual C# template and select Windows option

4) Select the console application template from the template list

5) Add a project name and click OK button

6) A new project is created in the solution explorer window

7) Add the needed code in the code editor window

8) Press F5 or click the Run button for project execution. User can view the output for the code

The compiling of the code of C# program using the command line of the Visual Studio IDE is possible.

1) Add the code in the text editor and save the file with .cs extension

2) Open the command prompt and navigate to the file

3) The csc filename.cs and compile the code

4) The command prompt moves to the next line and creates an executable file

5) Add the filename and execute the program

Chapter 3 Syntax, Data Types, and conversion

## 3.1 Different keywords in C#

Keywords are special predefined reserved words and are each assigned with a unique meaning. These keywords can be organized in to categories useful for better understanding. Below is a list of keywords categorized into different types.

### 1) Keywords for class, method, field and property

*   abstract
*   extern
*   internal
*   new
*   const
*   override
*   protected
*   private
*   public
*   sealed
*   readonly
*   static
*   virtual
*   void

### 2) Keywords for type conversions

*   explicit
*   implicit
*   as
*   is
*   operator
*   sizeof
*   typeof

### 3) Keywords useful for program flow control

*   if
*   else
*   for
*   foreach
*   in
*   case
*   break
*   continue
*   return
*   while
*   goto
*   default
*   do
*   switch

### 4) Keywords used for built in types and enumerations

*   bool
*   char
*   class
*   byte
*   decimal
*   enum
*   double
*   float
*   interface
*   long
*   int
*   object
*   sbyte
*   short
*   string
*   uint
*   struct
*   ulong
*   ushort

### 5) Keywords used for exception handling

*   try
*   catch
*   throw
*   finally
*   checked
*   unchecked

### 6) Keywords used as literals, method passing parameters

*   true
*   false
*   null
*   this
*   value
*   out
*   params
*   ref

### 7) Keywords useful in function pointers, object allocation, unmanaged code

*   delegate
*   event
*   new
*   stackalloc
*   unsafe

## 3.2 Data Types in C#

Data types are used to store the data in a specific type. There are several built in data types that are used by the programmers for declaring data.

Every data type has a limited set of options it can be, these limited number of options are called the data range for the data type. Listed below are the different data types present and the data range that they can be:

*   bool: Used to represent the Boolean value. The values that can be assigned are true or false.

*   byte: 8 – bit unsigned integer. The range of value for a byte data type is from 0 to 255

*   char: 16 – bit Unicode character. The range of values is from U +0000 to U + ffff

*   double: 64 – bit double precision floating point type. The range of values is from (+/-) 5.0 x 10-324 to (+/-) 1.7 x 10308

*   decimal: 128 bit precise decimal values with significant digits. The range of values is from ( -7.9 x 1028 to 7.9 x 1028 ) / 100 to 28

*   float: 32 bit single precision floating point. The range of values is from -3.4 x 1038 to + 3.4 x 1038

*   int: 32 – bit signed integer type. It has range of values from -2,147,483,648 to 2,147,483,647

*   long: 64 – bit signed integer type. It has range of values from -923,372,036,854,775,808 to 9,223,372,036,854,775,807

*   sbyte: 8 – bit signed integer type. It has range of values from -128 to 127

*   short: 16 – bit signed integer type. It has range of values from -32,768 to 32,767

*   unit: 32 – bit unsigned integer type. It has range of values from 0 to 4,294,967,295

*   ulong: 64 – bit unsigned integer type. It has range of values from 0 to 18,446,744,073,709,551,615

*   ushort: 16 – bit unsigned integer type. It has range of values from 0 to 65,535

## 3.3 Type conversion in C#

Type conversion is useful when the programmer needs to convert from one data type to another. The type conversion is also known as type casting. There are two types of type casting in C#. They are implicit type conversion and explicit type conversion.

### Implicit type conversion

The implicit keyword is used for implicit conversions. They do not need any casting operator. These conversions include small to large integral type, from derived class to base class.

### Explicit type conversion

The explicit conversions are done explicitly by users through the use of the pre-defined functions. In these conversions, a cast operator is needed.

| ![](Images/image00305.jpeg)Example 3: |
| using System;namespace TypeConversion{ class Conversion { static  void Main(string[  ] args) { double d=10.243; int i;i =  int  (d);            Console.WriteLine(i);            Console.Read(); } }} |

C# consists of type conversion methods that are useful for users.

The following list shows the type conversion methods.

*   ToByte: Used for converting a type to byte
*   ToBoolean: Used for converting Boolean value
*   ToDateTime: Used for converting a type to the date time type
*   ToDouble: Converts a type to double
*   ToDecimal: Converts the floating point or integer to decimal type
*   ToInt64: Converts the a type to 64 bit integer
*   ToSingle: Converts the type to floating point number
*   ToString: Converts the type to string type
*   ToUInt64: Converts a type to an unsigned big integer

The following code snippet shows the conversion of value type to Double type.

| ![](Images/image00305.jpeg)Example 4: |
| using System;namespace type{ class DoubleConversion { int a=10; float f=30.05f; bool b=false;        Console.WriteLine(a.ToDouble());        Console.WriteLine(f.ToDouble());        Console.WriteLine(b.ToDouble());        Console.Read(); }} |

Chapter 4 Variables and Constants

## 4.1 Exploring variables in C#

A variable is name assigned to the memory location used by the programs. Every variable has a data type associated with it. The data type determines the size of the variable’s memory used for storing within the memory.

The data types provided by C# are distinguished as:

1.  Integral types: int, unit, short, byte, sbyte, long, ulong, and char
2.  Floating point types: double, float
3.  Decimal types: decimal
4.  Boolean type: true or false values
5.  Nullable type: nullable data type
6.  Reference type: class

Defining Variables

The syntax for declaring the variables is:

<data_type> <variable_list>;

Where, data_type is a valid C# data type. It can be int, char, float, double, or a user defined type. The variable_list contains one or more identifiers.

Examples of variables

int a,b,c;

char x,y;

float price, totolcost;

double area;

Initializing Variables

The variables are initialized using an equal sign and followed by an expression. The syntax for initializing variable is:

variable_name = value;

The variables can be initialized in the declaration. The general form for initializing the variable is:

<data_type> <variable_name> = value;

Examples of variable initialization are:

int a = 4;

char z=’z’;

double y = 12.145;

Example for demonstrating variable types:

| ![](Images/image00305.jpeg)Example 5: |
| using System;namespace VariableDeclareclass Program{ static  void Main(string[] args) { int a; short s; double d; /*initializing variables*/        a=20;        s=5;        d=a+s;        Console.WriteLine("a={0},b={1},d={2}",a,s,d);        Console.Read(); }} |

Accepting values from user

The Console class present in the System namespace provides ReadLine() function. The function is used for accepting input from the user and stored into variable.

Example:

int no;

no=Convert.ToInt32(Console.ReadLine());

The Convert.ToInt32() function converts the data entered by the user to integer data type. The function accepts the data in string format.

LValue and RValue Expressions

The two types of expressions in C# are:

*   lvalue: The expression is an lvalue appears on the left side of the assignment.
*   rvalue: The expression is an rvalue that appears on the right side but not on the left side of the assignment.

The variables are lvalues and hence appear on the left side of the assignment. The numeric values are rvalues and hence appear on the right side.

int a=50;

## 4.2 Constants and literals in C#

Constant is a class member that represents a fixed value. Constant value can be computed at compile time but cannot be modified. Constants are declared using the const keyword.

Syntax:

const<data_type> <constant_name> = value;

Example of Constant:

| ![](Images/image00305.jpeg)Example 6: |
| using System;namespace constcclass Program{ static  void Main(string[] args) { const  int i=3; int x;        Console.WriteLine("The value for x is");        x=Convert.ToInt(Console.ReadLine()); int mult = x*i;        Console.WriteLine("Value of multiplication is:{0}",mult);        Console.ReadLine(); }} |

Literals

A literal is a source code representation of a value. There are different types of literals in C#.

Integer Literals

Integer literal is used to write values of type int, long, unit, and ulong. It can be represented as decimal, octal, or hexadecimal constant. The base or radix is specified by the prefix. The value 0x or 0X represents the hexadecimal, 0 defines octal and decimal is used without prefix.

Some of the examples of integer literals are 15, 0321, 0x5b, 30l.

Floating point literals

Floating point literal consist of integer part, fraction part, decimal part, and an exponent part. The floating point literals can be represented in exponent or decimal form.

Floating point literals can be mentioned as 3.1415, 1423E-6L.

Character Literals

Character literals represent a single character. They are enclosed in single quotes. Characters that are preceded with a backslash are called escape characters and some of these escape characters have special meanings when used in a string to designate a special function such as creating a tab or a carriage return. Below is a list of some of these special escape characters:

*   \’                A single quote
*   \”                Double quote
*   \\                Backslash
*   \0              null
*   \a              Alert
*   \b              Backspace
*   \f               Form feed
*   \t              Horizontal tab
*   \v              Vertical tab
*   \r              Carriage return

String Literals

There are two string literals types supported by C#: regular string literals and verbatim string literals. Regular string literals contain zero or more characters enclosed in double quotes.

A verbatim string literals contains @ character followed by a double quote character, zero or more character. A verbatim string literal can span multiple lines.

Examples showing string literals.

“welcome user”

“welcome, \

user”

@”welcome user”

Chapter 5 Operators in C#

## 5.1 Introduction to operators

Operator is used to define the meaning of an expression. It is a set of one or more characters used for computations or comparisons. Operators can change one or more data values, called operands into a new value.

## 5.2 Arithmetic operators

Arithmetic operators are used for performing the arithmetic operations on variables. The table shows the arithmetic operators in C#.

| Operator | Description | Example |
| + | Add two operands | c=a+bIf a=10, b=20, c=10+20=30 |
| - | Subtracts second operand from the first | c=a-bIf a=10, b=5, c=10-5=5 |
| * | Multiplies both the operands | c=a*bIf a=10, b=5, c=10*5=50 |
| / | Divides the numerator by denominator | c=a/bIf a=21, b=2, c=21/2=10 |
| % | Modulus operator and remainder after integer division | c=a%bIf a=21, b=2, c=21%2=1 |
| ++ | Increment operator. User for increasing value by one | If a=10,a++=11 |
| -- | Decrement. The value can be decreased by one | If a=10a--=9 |

## 5.3 Relational operators

The relational operators are used for relational operations and type comparisons.

| Operator | Description | Example |
| == | It checks if values of the operands are equal or not. | If x=10, y=20,(x==y) is not true |
| != | If the values of the two operands are not equal then condition is true | If x=11, y=12,(x!=y) is true |
| > | If the left operand is greater than right, condition is true | If x=13, y=17,(x>y) is not true |
| < | If the right operand is greater than left, condition is true | If x>10, y=15,(x<y) is true |
| >= | If the value of the left operand is greater or equal to right, condition is true | If x=5, y=3,(x>=y) is true |
| <= | If the value of the left operand is less or equal to right, condition is true | If x=10, y=4,(x<=y) is not true |

## 5.4 Logical operators

Logical operators are used for evaluating an expression and return a Boolean value.

| Operator | Description | Example |
| && | Logical AND operator. If both the expressions are true, result is true | X has Boolean value as true and Y has Boolean value false,(A&&B) is false |
| ! | Logical NOT operator. If the expression is false, returns true | X has Boolean value true,!(X) = false |
| &#124;&#124; | Logical OR operator. If either of the expression is true, result is true | X has Boolean value true, Y has Boolean value false,(X&#124;&#124;Y)  is true |
| ^ | If either of the expression is true, returns true. It returns false if both the expressions are true or false | X has Boolean value true, Y has value false,(X^Y) is true |

## 5.5 Bitwise operators

Bitwise operators are used on bits. They perform bit operation.

| a | b | a&b | a&#124;b | a^b |
| 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 0 |

## 5.6 Assignment operators

Assignment operators are used for performing arithmetic operations on the operands. The resultant value is assigned to any one of them.

| Operator | Description | Example |
| = | Assigns value from right side operands to the left side operand | z=x+y assigns value pf x+y to z |
| += | Add AND assignment operator. Adds the right operand to the left operand and the result is assigned to left operand | x+=y is similar to x=x+y |
| -= | Subtract AND assignment operator. Subtracts the right operand from the left. | x-=y is similar to x=x-y |
| *= | Multiply AND assignment operator. Multiplies right operand with the left | x*=y is similar to x=x*y |
| /= | Divide AND assignment operator. Divides left operand with the right | x/=y is similar to x=x/y |
| %= | Modulus AND assignment operator. It takes the modulus of both the operands | x%=y is similar to x=x%y |
| <<= | Left shift AND assignment operator | a<<=2 is similar to a=a<<2 |
| >>= | Right shift AND assignment operator | a>>=2 is similar to a=a>>2 |
| &= | Bitwise AND assignment operator | a&=3 is similar to a=a&3 |
| ^= | Bitwise exclusive OR assignment operator | a^=4 is similar to a=a^4 |
| &#124;= | Bitwise inclusive OR assignment operator | a&#124;=5 is similar to a=a &#124; 5 |

## 5.7 Miscellaneous operators

| Operator | Description | Example |
| sizeof() | It returns the data size | sizeof(int), returns 4 |
| typeof() | The type of class is provided | typeof(StreamWriter); |
| & | Address of an variable | &x, actual address of the variable |
| ?: | Conditional expression | If condition is true? X value else Y |
| as | If the cast is not success, cast without raising exception | Object o1 = new StringReader(“Welcome”);StringReader s = obj as StringReader; |
| is | It checks if the object is of specific type | If(Maths is Subject) ,Checks for the subject maths |

Chapter 6 C# Decision making statements

Decision making is structured in the following way:

*   There must be at least one condition for the statements to meet
*   There must be at least two end outcomes

Looking at the diagram below, we can see a general representation of the decision making logic.

![](Images/image00320.jpeg)

In the diagram above, the arrows represent the flow of statements executing in the system. When the statement reaches a conditional logic (diamond shape) the statement is matched to the condition. This condition has two outcomes True or False.

If the statement matches the condition then it will be declared as True and the statement will then run a set of code (rectangle) before reaching the end. If the statement does not match the condition then it will be declared as false and will directly proceed to the end point.

C# has various types of decision making statements. They are explained in detail.

## 6.1 If Statement

If statement contains a Boolean expression True or False. It is followed by one or more statements.

Syntax:

if (boolean_expression)

{

              //if the Boolean expression is true, statement executed

}

If the expression contains value true, the statements in the block of code will be executed. If the expression has value false, the set of code after the end of if statement is executed.

Flow Diagram

![](Images/image00321.jpeg)

Example of if statement

| ![](Images/image00305.jpeg)Example 7: |
| using System;namespace decision{ class Program { static  void Main(string[] args) { /*local variables*/ int i = 15; /*boolean condition is checked*/ if(i < 15) {                Console.WriteLine("The value of i is less than 15"); }            Console.WriteLine("Value of i is{0}",i);            Console.Read(); } }} |

In this code example we can see that the condition is  if(i<15).So here the variable i must meet the condition to be less than 15 for the condition to be True or else it is False.

## 6.2 If else statement

An if statement can be added with an optional else statement. The else statement is executed when the expression value is false.

Syntax:

if(boolean_expression)

{

              /* If the Boolean expression is true, this  statement is executed

}

else

{

              /* If the Boolean expression is false, this statement will be executed

}

If the expression has value true then the if block is executed, otherwise else block is executed.

Flow Diagram

![](Images/image00322.jpeg)

Example of if else statement:

| ![](Images/image00305.jpeg)Example 8: |
| using System;namespace ifelseconstructclass User{ static  void Main(string[] args) { int age;        Console.WriteLine("Enter the age of the user");        age=Convert.ToInt32(Console.ReadLine()); if(age < 18) {            Console.WriteLine("Not an adult"); } else {            Console.WriteLine("User is an adult"); } }} |

In the code example, the condition ( age < 18 ) is specified. So here the variable age must meet the condition less than 18 for the condition to be True, otherwise the else block is executed.

The else if else statement

An if statement is also followed by an else if else construct. Many conditions can be checked using if else if statement.

Syntax

if (boolean_expression 1)

{

              /*If the Boolean expression 1 is true, the statement is executed*/

}

else if(boolean_expression 2)

{

              /* If the Boolean expression 2 is true, the statement is executed*/

}

else if(boolean_expression 3)

{

              /* If the Boolean expression 3 is true, the statement is executed*/

}

else

{

              /* executes if none of the condition is true*/

}

Example of else if else statement

| ![](Images/image00305.jpeg)Example 8: |
| using System;namespace ifelse{ class Program { static  void Main(string[] args) { int x = 30; if(x == 100) {                Console.WriteLine("The value is 100"); } else  if(x == 20) {                Console.WriteLine("The value is 20"); } else  if(x == 10) {                Console.WriteLine("The value is 10"); } else {                Console.WriteLine("No matching value found"); }            Console.WriteLine("Value of x is:{0}",x);            Console.Read(); } }} |

In the above example, the value x = 30 is specified. If there is an expression that matches the value of x, the appropriate block is executed. If none of the expression matches, the else block is executed.

## 6.3 Nested if statement

The nested if statement contains one if or else if statement inside another if or else statement.

Syntax for nested if statement

if(boolean_expression1)

{

              /*If the expression 1 is true, statement is executed*/

if(boolean_expression2)

{

              /*If the expression 2 is true, statement is executed*/

}

}

Example for nested if statement

| ![](Images/image00305.jpeg)Example 9: |
| using System;namespace nestedif{ class Program { static  void Main(string[] args) { int x = 20; int y = 40; if(x == 20) { if(y == 40) {                    Console.WriteLine("Value of x is 20 and y is 40"); } }            Console.WriteLine("Value of x is:{0}",x);            Console.WriteLine("Value of y is:{0}",y);            Console.Read(); } }} |

In the above code, the value for x and y variables is assigned. The value inside if statement is checked. If it is same, the inner statements are executed, else the control moves out of the loop.

## 6.4 Switch statement

A switch statement helps to evaluate a variable for multiple conditions efficiently. Every condition is known as a case and the variable switched is checked for the switch case.

Syntax:

switch(Expression)

{

              case ConstantExpression1:

                            statements;

              break;

              case ConstantExpression2:

                            statements;

              break;

              …..

              case ConstantExpression_n:

                            statements;

              break;

              default:

                            statements;

                            break;

}

The rules added in the switch statement are:

*   Expression in a switch statement must be an integer or of a class type.

*   A user can add any number of case statements in a switch statement.

*   The ConstantExpression must be of the data type similar to the expression in the switch.

*   When the Expression matches the ConstantExpression, the code inside that case will be executed and will hit the break keyword which will force the execution out of the switch statement.

*   Every case does not need a break keyword.

*   The optional default case appears at the end of the switch and acts as a backup in case the expression does not match any of the ConstantExpressions.

Flow Diagram

![](Images/image00323.jpeg)

Example of switch statement

| ![](Images/image00305.jpeg)Example 10: |
| using System;namespace switchcase{ class Program { static  void Main(string[] args) { char grade ='A+'; switch(grade) { case C:                        Console.WriteLine("Fair"); break; case B:                        Console.WriteLine("Good"); break; case A+:                        Console.WriteLine("Excellent"); break;    default:                        Console.WriteLine("No matching grade"); break; }            Console.WriteLine("Grade is {0}",grade);            Console.ReadLine(); } }} |

In the above code, the value of grade is assigned. It is matched with the different switch cases. If the value matches from among the declared cases, the corresponding message is displayed. If none of the expression matches, the default caseis executed.

## 6.5 Nested switch statement

User can switch part of the statement sequence of the outer switch. The common values in the switches do not conflict.

Syntax:

switch(c1)

{

              case ‘A’:

                            Console.WriteLine(“A is the part of outer switch”);

                            break;

              switch(c2)

              {

                            case ‘A’:

                                          Console.WriteLine(“ A is the part of inner switch”);

                                          break;

                            case ‘B’:

              }

              break;

              case ‘B’:

}

Example of nested switch statement

| ![](Images/image00305.jpeg)Example 11: |
| using System;namespace switchcase{ class Program { static  void Main(string[] args) { char grade ='A+'; switch(grade) { case C:                        Console.WriteLine("Fair"); break; case B:                        Console.WriteLine("Good"); break; case A+:                        Console.WriteLine("Excellent"); break;    default:                        Console.WriteLine("No matching grade"); break; }            Console.WriteLine("Grade is {0}",grade);            Console.ReadLine(); } }} |

| ![](Images/image00305.jpeg)Example 12: |
| using System;namespace nestedswitch{ class Program { static  void Main(string[] args) { int x = 20; int y = 40; switch(x) { case  20:                Console.WriteLine("Part of outer switch"); switch(y) { case  40:                    Console.WriteLine("Part of inner switch"); break; } break; }            Console.WriteLine("Value of x is :{0}",x);            Console.WriteLine("Value of y is: {0}",y);            Console.Read(); } }} |

In the above code, the value of variable x and y is assigned. If the value for variable x matches the expression, the statements inside the switch case are executed, else the control moves out of the case structure.

Chapter 7 Loops in C#

Loop structures are used for executing one or more lines again and again. Various control structures are provided for complicated execution.

![](Images/image00324.jpeg)

## 7.1 While loop

A while loop consists of a conditional expression that must be matched before the logical statements inside the while loop can be executed. If a statement matches the expression then it will run the code inside the loop and then return back to the conditional expression to re-check whether the statement still matches the expression. If it matches again then the loop will execute again otherwise it will skip the loop completely.

Let us visit the syntax of a while loop.

Syntax:

while (expression)

{

              statements;

}

Flow Diagram

![](Images/image00325.jpeg)

Example of while loop

| ![](Images/image00305.jpeg)Example 13: |
| using System;namespace whileloop{ class Program { static  void Main(string[] args) { int var;            var=50; while(var<150) {                Console.WriteLine("Value of variable is:{0}",var);                var=var+10; } } }} |

In the preceding code, the variable var is initialized with value 50\. The while loop checks for the condition. If the condition is less than 150, the statements inside the loop are executed. If false, the control does not enter the while loop.

## 7.2 For loop

A for loop is used to execute a block of statements for a specific number of times.

Syntax:

for (initialization; condition; increment/decrement)

{

              statement(s);

}

Where,

*   initialization is used to declare and initialize the loop control variables. It is executed at the beginning of the loop
*   condition checks for the expression. If the value is true, the body of the loop is executed. If false, the control jumps out from the loop
*   increment/decrement is used for increasing or decreasing the variable value.

Flow Diagram

![](Images/image00326.jpeg)

Example of for loop

| ![](Images/image00305.jpeg)Example 14: |
| using System;namespace forloop{ class Program { static  void Main(string[] args) { int i; for(int i=1;i<=10;i++) {                Console.WriteLine("Value of variable is:{0}",i); } } }} |

In the above code, value for variable i is declared. For loop contains assignment, condition, increment. If the condition is true, the value is incremented. The statement inside for loop is executed. Once the condition is false, the control moves out of the loop. 

## 7.3 Do while loop

The do…while loop construct is similar to the while loop. Both the loops will continue until the condition is false. The difference is that the statements in a do…while loop are executed at least once, as the statements in the block are executed before the condition is checked.

Syntax:

do

{

              Statements;

}while(expression);

Flow Diagram

![](Images/image00327.jpeg)

Example of do while loop

| ![](Images/image00305.jpeg)Example 15: |
| using System;namespace dowhile{ class Program { static  void Main(string[] args) { int x=1; do {                Console.WriteLine("Value of x is:{0}",x);                x=x+1; }while(i<10);            Console.ReadLine(); } }} |

In the above code, the variable x is assigned with value 1\. The do loop prints the statements inside the block. Once the condition in the while loop is false, the statements in the do while loop will not be executed.

## 7.4 Break statement

The break statement is used to exit from the loop. When this  statement is encountered, the loop is terminated, the control resumes to the next statement following loop.

Syntax:

break;

Flow Diagram

![](Images/image00328.jpeg)

Example of break statement

| ![](Images/image00305.jpeg)Example 16: |
| using System;namespace  break;{ class Program { static  void Main(string[] args) { int i=11; while(i<15) {                Console.WriteLine("value of i:{0}",i);                i++; if(i>13) { break; } }            Console.ReadLine(); } }} |

In the code example, value of variable i is assigned to 11\. The while loop checks for the condition of i. If the condition is true, the statements in the while loop are executed. The value for i is incremented.

If loop checks for value i. Once the value of i is greater than 13, the break statement is executed and the control is moves out of the loop.

## 7.5 Continue statement

The continue statement is similar to the break statement, but instead of breaking out of the loop the continue forces the next iteration of the loop to take place, skipping any code in between.

Syntax:

continue;

Flow Chart

![](Images/image00329.jpeg)

Example of Continue statement

| ![](Images/image00305.jpeg)Example 17: |
| using System;namespace  continue{ class Program { int i=45; do { if(i==50) {                i=i+1; continue; }            Console.WriteLine("Value of i is:{0}",i);            i++; } while(i<60);        Console.ReadLine(); }} |

So in the code example above we can see a combination of the do-while loop and continue in action. We can see thati is initially set as a 45 when it enters the statements inside the do. At this pointichecked to see if it matches 50, it doesn’t so the value ofiis outputted in a message andi is incremented by one.

This process happens untiliis 50, at which pointi will be incremented by one and hit the continue keyword which will skip the rest of the code in the do section and move straight to the while conditional expression.

Oncei reaches 61 the while conditional statement will not match and the execution will leave the loop.

Chapter 8 Classes and Methods in C#

## 8.1 Class declaration

In C# classes are the primary building blocks of the language. It provides predefined set of variables and methods. Objects are defined as an instance of a class, therefore the methods inside the class determine what can be executed on the object. 

Class Definition

A class definition starts with keyword class followed by the actual class name. The class variables and methods are all enclosed in between the curly brackets; this area is also called the class body.

Syntax:

<access specifier>class class_name

{

              //member variables

              <access specifier> <data type> variable1;

              <access specifier> <data type> variable2;

              ……

              <access specifier><data type> variableN;

              //member methods

              <access specifier><return type>method1(parameter_list)

              {

                            //method body

              }

              <access specifier><return type>method2(parameter_list)

              {

                            //method body

              }

              ….

              <access specifier><return type>methodN(parameter_list)

              {

                            //method body

              }

}

*   Access specifiers define the level of contact for other methods and members to be able to interact with methods and members of the given class. If no access specifier is specified, the default access specifier is private.
*   The date type specifies the variable type and the return type is used to state what type of data is returned from the method, although it should be noted that a method does not need to always return anything.
*   The dot(.) operator is used for accessing the class member
*   The dot operator is used to link the object name and member name

Example to demonstrate class

| ![](Images/image00305.jpeg)Example 18: |
| using System;namespace demo{ class Calculate { public  int len; public  int bread; } class Program { static  void Main(string[] args) {Calculate c1 = new Calculate();Calculate c2 = new Calculate(); int area =  0; int area1 =  0;            c1.len = 10;            c1.bread = 5;            c2.len = 15;            c2.bread = 10;area = c1.len*c1.bread;            Console.WriteLine("area of rectangle1 is:{0}",area);area1 = c2.len*c2.bread;            Console.WriteLine("area of rectangle2 is:{0}",area1)            Console.ReadLine(); } }} |

When compiled the result of this class will be:

area of rectangle2 is:50

area of rectangle2 is:150

## C# constructors

A constructor is a special type of method invoked automatically when the instance of the class is created. The members of the class are initialized inside the constructors. The constructor has to have the same name as the class itself.

Example of Constructor

| ![](Images/image00305.jpeg)Example 19: |
| using System;namespace construct{ class Calculate { int number1,number2,sum;        Calculate() {number1 = 20;number2 = 40; } public  void Addition() {sum = number1+number2; } public  void Show() {            Console.WriteLine("The total is:{0}",sum); } public  static  void Main(string[] args) {Calculate c1 = new Calculate();            c1.Addition();            c1.Show(); } }} |

When compiled the result of this class will be:

The total is: 60

In the example above every time the classCalculateis instantiated, the constructor manually assigns a fixed value tonumber1andnumber2. However what if you wanted to make the values ofnumber1andnumber2 different and dynamic? How would this be achieved?

Well this is where a concept of a parameterized constructor comes in. Essentially what this fancy term means is that we pass in parameters directly in to the constructor, this allows us to pass in values at the point of instantiation of the class. Lets look at an example:

Example of parameterized constructor

| ![](Images/image00305.jpeg)Example 20: |
| using System;namespace construct{ class Calculate { int number1,number2,sum;  // Parameters are added in to here inside the constructor        Calculate(int num1,int num2) {                            // We assign the parameters to the class variablesnumber1 = num1;number2 = num2; } public  void Addition() {            sum=number1+number2; } public  void Show() {            Console.WriteLine("The total is:{0}",sum); } public  static  void Main(string[] args) {            int a,b;            Console.WriteLine("Enter value of a");a = Convert.ToInt32(Console.ReadLine());            Console.WriteLine("Enter the value of b");b = Convert.ToInt32(Console.ReadLine()); // a and b are passed through to the class constructorCalculate c1 = new Calculate(a,b);c1.Addition();            c1.Show();Console.ReadLine(); } }} |

When compiled the result of the class is:

Enter value of a

10

Enter value of b

20

The total is: 30

## C# destructors

A destructor is a special function in a class that is used very rarely to usually release unmanaged resources before exiting the class. The destructor has several limitations on how it can be used:

*   It cannot be inherited.
*   It cannot be overloaded.
*   There can only be one destructor in any given class.
*   The destructor cannot be directly called by the programmer; it is instead called by the Garbage Collector.

Destructor has the same name as its class and is prefixed with ~ symbol which is represented by a tilde.

Example of Destructors

| ![](Images/image00305.jpeg)Example 21: |
| using System;namespace destruct{ class Calculate { int number1,number2,sum;        Calculate() {            number1=15;            number2=4; } public  void Addition() {            sum=number1+number2; } public  void Show() {            Console.WriteLine("The total is:{0}",sum); }                // Destructor is defined here and is called when the class  // goes out of scope. ~Calculate() {            Console.WriteLine("Destructor invoked"); } public  static  void Main(string[] args) {            Calculate c1=new Calculate();            c1.Addition();            c1.Show(); } }} |

When compiled the result of the class will be:

The total is: 19

## 8.2 Defining methods

Method is a set of one or more program statements, which can be executed by calling the method name. For using a method, the user first needs to define a method and then call the method.

Defining a method means declaring the element of its structure. The following syntax is used for defining the method.

<Access Specifier> <Return Type> <Method Name> ( Parameter List)

{

              Method Body

}

The different elements of a method are:

*   Access specifier: It checks the extent to which the variable or method can be accessed.

*   Return Type: This defines what the type is for the value returned by the method. If the type is set as void then this would mean that the method does not return anything.

*   Method Name: It is a unique identifier and case sensitive. The method name cannot be the same as a variable name.

*   Parameter List: The values that are passed and received by the method. After the method name, they are written in parentheses.

*   Method Body: The set of instructions for performing the function of the actual method.

Example:

| ![](Images/image00305.jpeg)Example 22: |
| class Average{ public  int Number(int no1,  int no2) { int output;output = no1+no2/2; return output; }  } |

## 8.3 Calling methods

Once the method is defined, a user can call the method using the method name. The method name is followed by the parentheses.

Example:

| ![](Images/image00305.jpeg)Example 23: |
| using System;class Average{ public  int Number(int no1,  int no2) { int output;output = no1+no2/2; return output; }   static  void Main(string[] args) {Average a =  new Average();                // calling method Number from object class a int value = a.Number(20,30);        Console.WriteLine("The result is {0}",value); }} |

When the code is compiled the result is:

The result is 25

## 8.5 Recursive method call

A method can call itself this  is known as recursion.

| ![](Images/image00305.jpeg)Example 24: |
| using System;namespace recursive{ class recursivecall { public  int factorial(int no) { int result; if(no == 1) { return  1; } else {result = factorial(no-1)*no; return result; } } static  void Main(string[] args) {recursivecall r =  new recursivecall();            Console.WriteLine("Factorial of no is {0}",n.factorial(2));            Console.WriteLine("Factorial of no is {0}",n.factorial(3));            Console.Read(); } }} |

When the code is complied the result will be:

Factorial of no is 2

Factorial of no is 6

## 8.4 Passing parameters to method

When a user calls a method, if the method accepts parameters then these will have to be passed through at the time the method is called. There are three types of parameters passed to the method.

Value parameter

With a value parameter, the method creates a copy of this passed in parameter as a variable for use inside the method. If the value of this variable is changed, it will be only changed in the scope of the method itself and not of the original variable that was passed in as a parameter to the method.

Example:

| ![](Images/image00305.jpeg)Example 25: |
| class Program{ void Increaseno(int no) {        no++; } public  static  void Main() {Program p = new Program(); int number =  2;        p.Increaseno(number);        Console.WriteLine(number); }} |

When the code is complied the result will be:

2

Reference Parameter

The reference parameter is the same as the value parameter except that when the parameter is passed to the method, instead of creating a copy of the parameter value, it instead directly points to the original stored value in memory. Thus, if the value is changed in the scope of the method then it will also change the value of the original variable that was passed in as a parameter.

The ref keyword is used for declaring the reference parameter.

Example:

| ![](Images/image00305.jpeg)Example 26: |
| class Program{ void Increaseno(int no) {        no++; } public  static  void Main() {        Program p=new Program(); int number =  2;        p.Increaseno(ref number);        Console.WriteLine(number); }} |

When the code is complied the result will be:

3

Output parameter

The return statement is used for returning value from the method. Only a single variable can be returned using return statement. The output parameter provides this purpose.

They are similar to reference parameters, except they transfer data out of the method.

Example:

| ![](Images/image00305.jpeg)Example 27: |
| class Program{ void Demo(out  int no) {        no=10; } public  static  void Main() {        Program p=new Program(); int number;        p.Demo(out number);        Console.WriteLine(number); }} |

When the code is complied the result will be:

10

Chapter 9 Arrays in C#

## 9.1 Introduction to arrays

An array is a collection of values of similar data type. The variables in the array are known as the elements of the array. The array elements are accessed using a single name and an index number representing the position of the element within the array.

An array has a rank that determines the number of indices associated with every array element. The rank of the array is also referred to as the dimensions of the array. The following figure shows the array structure in the system.

![](Images/image00330.jpeg)

## 9.2 Arrays declaration

An array is declared before it is used in any program. The following syntax is used to declare an array.

 datatype[ ] ArrayName;

The syntax of an array involves the components mentioned below:

*   datatype: Used for specifying the data type for elements. It will be stored in an array.
*   [ ] : Specify the size of the array and is referred to as rank.
*   ArrayName: States the name of the array.

## 9.3 Initializing and adding values

The new keyword is used to create an instance of the array. The size of array is specified when it is initialized. The following code snippet is used to initialize the array.

int [ ] x ;

x = new int [15];

The array can be initialized by combining the two statements and is written as:

int [ ] x = new int [15];

Assigning values to an array

The values can be assigned to each element of the array using the index number. It is also known as subscript of the element. The following code snippet is used for assigning the values to an array.

int [ ] amount = new int [5];

int [0] = 50;

The array can be created and initialized using the following code:

              int [ ] amount = { 40,60,70,80};

The size of an array can be removed.

              int [ ] age = new int[ ] { 21,31,40};

When a user copies the data from one array into another, the source and target array refer to same location. The following code snippet shows the copying of one array to another.

int [ ]  age = new int[ ] { 12,14,15,16};

int [ ] amount = age;

The two arrays as age and amount are created. They point to same memory location.

## 9.4 Accessing array elements

To access an element in an array, you will need to use an index. An index is the number that represents the position of elements in the array. Indexes always start from zero, so to access the first element in an array we would do so in this format:

array_name[index]

In this case the value of index will be zero.

Example:

| ![](Images/image00305.jpeg)Example 28: |
| using System;namespace arraydeclare{ class Arraydemo { static  void Main(string[] args) { int  [] a =  new  int[5]; int x,y; for(int x = 0;x <5;x++) {                a[x]=x + 10; } for(y = 0;y < 5;y++) {                Console.WriteLine("Element [{0}]={1}",y,a[y]); }            Console.ReadLine(); } }} |

When the code is compiled and executed, the output is:

Element [0] = 10

Element [1] = 11

Element [2] = 12

Element [3] = 13

Element [4] = 14

## 9.5 Foreach loop

This loop is specifically designed to iterate through all elements of an array. It is great for retrieving elements of an array efficiently.

Syntax:

 foreach(type identifier in expression)

              statement – block

Example:

| ![](Images/image00305.jpeg)Example 29: |
| using System;namespace arraydeclare{ class Arraydemo { static  void Main(string[] args) { int  [] a =  new  int[5]; for(int x = 0;x < 5;x++) {                a[x] = x + 10; } foreach(int y in a) { int x = y - 10;                Console.WriteLine("Element[{0}]",x,y);                x++; }            Console.ReadLine(); } }} |

The code is compiled and executed, the output is:

Element [0] = 10

Element [1] = 11

Element [2] = 12

Element [3] = 13

Element [4] = 14

## 9.6 Different C# arrays

The following are various types of C# arrays that are used for developing code.

Multi-dimensional arrays

A multi-dimensional array stores data in more than one row dimension. It is also known as rectangular array. User can declare two-dimensional array of integer as:

int [ , ] no;

A two-dimensional array can be considered as table. It has x rows and y columns. A two-dimensional array contains 2 rows and 4 columns.

![](Images/image00331.jpeg)

Initializing two dimensional arrays

The following array has 3 rows and 3 columns.

int [ , ] x = int [ 3, 3] = {

{1, 2, 3},

{4, 5, 6},

{7, 8, 9}

};

Accessing elements of multidimensional array

An element from the multi dimensional array can be accessed using the subscripts. They are row and column index of the array.

Example:

int output = a [1, 2];

In the above statement, the element from second row and third column is accessed.

Example:

| ![](Images/image00305.jpeg)Example 30: |
| using System;namespace twodimension{ class multiarray { static  void Main(string[] args) {int  [  ,  ] x =  new  int[3,2]{{1,1},{2,2},{3,3}}; int a,b; for(a = 0;a < 3;a++) { for(b = 0;b < 2;b++) {                Console.WriteLine("x[{0},{1}={2}",a,b,x[a,b]); } }        Console.ReadLine(); } }} |

The code is compiled and executed, the output is:

x[0,0] = 1

x[0,1] = 1

x[1,0] = 2

x[1,1] = 2

x[2,0] = 3

x[2,1] = 3

Jagged Array

A jagged array is an array of arrays. The jagged array of int type is declared as:

int [ ] [ ] marks;

An array can be initialized as:

              int [ ] [ ] marks = new int [3] [ ] { new int [ ] {45,57,78}, new int [ ] { 60, 75, 86,45,35}};

The marks array is of two arrays of integers as marks[0] with 3 integers and marks[1] with 5 integers.

Example:

| ![](Images/image00305.jpeg)Example 31: |
| using System;namespace Jaggedarray{ class jagged { static  void Main(string[] args) {int[][] x =  new  int[][]{new  int[]{0,0},new  int[]{2,2},new int[]{3,4},new  int[]{4,2},new  int[]{1,3}}; int a,b; for(a = 0;a < 5;a++) { for(b = 0;b < 2;b++) {                                                                                            Console.WriteLine("x[{0},{1}]={2}",a,b,x[a][b]); } }                      Console.ReadLine(); } }} |

The code is compiled and executed, the output is:

x[0,0] = 0

x[0,1] = 0

x[1,0] = 2

x[1,1] = 2

x[2,0] = 3

x[2,1] = 4

x[3,0] = 4

x[3,1] = 2

x[4,0] = 1

x[4,1] = 3

Param Arrays

When a method is declared, the number of arguments to be passed as parameter is not decided. The Param array is used.

Example:

| ![](Images/image00305.jpeg)Example 32: |
| using System;namespace ParamArray{ class ParamArray { public  int AddValues(params  int[] data) { int total =  0; foreach(int a in data) {                total+ = a; } return total; } } class Test { static  void Main(string[] args) {ParamArray pa =  new ParamArray(); int total=pa.AddValues(2,3,4,5,6);            Console.WriteLine("The sum is {0}",total);            Console.Read(); } }} |

When the code is compiled and executed, the output is:

The sum is 20

Array Class

The array class is the base class for all arrays in C#. The System namespace contains the  array class. There are various properties and methods used in the array class.

Properties of Array class

*   Length: The total number of items in all dimensions of an array are returned
*   Rank: It returns the rank of an array
*   IsFixedSize: It is a value indicating an array has fixed size or not
*   IsReadOnly: Value stating the array is read only or not

Methods of Array class

*   Sort: The sort operation on an array passed to it as a parameter
*   Clear: It removes all the items in an array and sets range of items to 0
*   GetLength: The number of items in an array are returned
*   GetValue: The value of the specified item in an array
*   IndexOf: The index of the first occurrence of a value in one dimensional array is returned
*   Reverse: It reverses the sequence of elements in the array

Example:

| ![](Images/image00305.jpeg)Example 33: |
| using System;namespace Array{ class Array1 { static  void Main(string[] args) { int[] item = {12,34,23,55,64}; int[] value = item;                            Console.Write(“Original  Array:”); foreach(int x in item) {                Console.Write(x+" "); }            Console.WriteLine();                            //reverse the array            Array.Reverse(value);            Console.Write("Array reversed:"); foreach(int x in value) {                Console.Write(x+" "); }            Console.WriteLine();                            //sort the array            Array.Sort(item);            Console.Write("Array sorted:");            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Original  Array: 12 34 23 55 64

Array reversed: 64 55 23 34 12

Array sorted: 12 23 34 55 64

Chapter 10 Strings in C#

## 10.1 Creation of string

A  string in C# is an array of characters. The string keyword is used for declaring the variable. The keyword is an alias for System.String class.

String Object creation

There are various methods used for string creation. They are:

*   Retrieving a property or calling a method returning a string
*   Use of string class constructor
*   Use of string concatenation operator (+)
*   Calling formatted method for converting a value or an object to the string representation
*   Assigning a string literal to the string variable

Example:

| ![](Images/image00305.jpeg)Example 34: |
| using System;namespace StringType{ class Program { static  void Main(string[] args) { //string literal and concatenation string name,location;name = "Harry";location = "USA"; string value = name + location;            Console.WriteLine("The value is:{0}",value); //string constructor char[] vowels = {'a','e','i','o','u'}; string item =  new  string(vowels);            Console.WriteLine("The item contains values:{0}",item); //formatting method for value conversionDateTime dt = new DateTime(2014,12,10,15,34,1);string msg = string.Format("Message sent at {0:t} on {0:D}",dt); //method returning value string[] array = {"Welcome","User"}; string result = String.Join("",array);            Console.WriteLine("Message is:{0}",result); } }} |

When the code is compiled and executed, the output is:

The value is: Harry USA

The item contains values: aeiou

Message sent at 2.30 PM on Tuesday, June 02, 2015

Message is: Welcome User

## 10.2 Properties and methods of string class

Properties of string class

*   Chars: Gets the Char object at specific position in the String object
*   Length: Gets the number of characters in the String object

Methods of string class

*   public bool Equals(string value)

Checks whether the current String object and the specified object have same value

*   public string Insert(int startIndex, string value)

Returns a new string in which the specified one is inserted at a specific index position

*   public string Replace(char oldchar, string newValue)

All the occurrences of a specific character in the string object are replaced with Unicode character and a new string is returned.

*   public int LastIndexOf(string value)

The zero based index position of the last occurrence of the Unicode character in the string object is returned

*   public string Trim()

All leading and trailing white space characters from the object are returned.

*   public static Compare(string str1, string str2, bool IgnoreCase)

Compares the two strings and an integer value stating the relative position in sort order

*   public static string Concat(string str1, string str2)

Concatenates the two string objects

*   public string[] Split (char[] separator, int count)

A string array containing the substrings in the current string object is returned. It is delimited by the elements of a specific Unicode character array. The number of substrings returned is specified by the int parameter.

*   public bool Contains(string value)

Returns value stating the specified string object occurs in the string

*   public static string Copy(string str)

Creates a new String object with the same value as the specified string

*   public string ToUpper()

Copy of the string converted into uppercase is returned

*   public int IndexOf(string value)

Returns the zero – based index of the first occurrence of the specified string in the instance

*   public string Remove(int startindex)

It removes the characters in the current instance, beginning at the specified position and moving to the last one. It returns a string.

*   public char[] ToCharArray()

A Unicode character array with all the characters in the current string object is returned

*   public string ToLower()

Copy of the string converted into lowercase is returned

## 10.3 Examples demonstrating the string functionality

String Comparison

| ![](Images/image00305.jpeg)Example 35: |
| using System;namespace string1{ class Program { static  void Main(string[] args) { string string1 = "A string named as string1"; string string2 = "A string named as string2"; if(String.Compare(string1,string2) == 0) {                Console.WriteLine(string1+"and"+string2+"equal"); } else {                Console.WriteLine(string1+"and"+string2+" not equal"); }            Console.Read(); } }} |

When the code is compiled and executed, the output is:

A string named as string1 and A string named as string2 are not equal

Joining strings

| ![](Images/image00305.jpeg)Example 36: |
| using System;namespace string1{ class Program { static  void Main(string[] args) { string[] str1 =  new  string[]{"Set your aims high", "Rome was not built in a day", "Save Time"}; string str = String.Join("\n",str1);            Console.WriteLine(str);            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Set your aims high

Rome was not built in a day

Save Time

String containing value

| ![](Images/image00305.jpeg)Example 37: |
| using System;namespace string1{ class Program { static  void Main(string[] args) { string str = "A new user"; if(str.Contains("user")) {                Console.WriteLine("The value 'user' is present"); }            Console.Read(); } }} |

When the code is compiled and executed, the output is:

The value 'user' is present”

Chapter 11 Encapsulation and Polymorphism

## 11.1 Introduction to encapsulation

Encapsulation is the process of enclosing data and function within a physical or logical package. It helps the developers to prevent the access to the essential details of an application. It binds the code and data together.

Abstraction states that all the information is present, but only relevant information is provided to the user.

Abstraction and encapsulation are related features. Encapsulation assists abstraction by providing means of hiding the non-essential details. Using encapsulation some information is visible and others are hidden.

## 11.2 Access specifier in C#

An access specifier defines the scope of a class member. The member is used for referring the functions and variables of a class. A program consists of one or more classes. Some member of the class needs to be accessed by other classes.

Types of Access Specifier

The following access specifiers are supported by C#.

*   public
*   private
*   protected
*   internal
*   protected internal

Public Access Specifier

Public access specifier allows the class to expose the member variables and functions with other classes. The member declared as public can be accessed from outside the class.

Example of public access specifier

| ![](Images/image00305.jpeg)Example 38: |
| using System;namespace public1{ class User { //member variables public  string name; public  int age; public  void AddValue() {            Console.WriteLine("Enter the user name:");name = Console.ReadLine();            Console.WriteLine("Enter the age:");age = Convert.ToInt32(Console.ReadLine()); } public  void Show() {            Console.WriteLine("User name is:{0}",name);            Console.WriteLine("Age is:{0}",age); } } class Program { static  void Main(string[] args) {User u =  new User();                u.AddValue();                u.Show();                Console.Read(); } }} |

When the code is compiled and executed, the output is:

Enter the user name:

Mark

Enter the age:

20

User name is: Mark

Age is: 20

Private Access Specifier

The private access specifier allows the user to hide classes’ member variables and functions from other class objects and functions. The private members are not visible from outside the class. Only the class functions based within the class itself can access the private entity. Objects or instances of the class cannot access any private variables or functions as they are declared as external to the class.

Example:

| ![](Images/image00305.jpeg)Example 39: |
| using System;namespace private1{ class Student { //member variables private  string name; private  int age; public  void AddValue() {            Console.WriteLine("Enter the student name:");name = Console.ReadLine();            Console.WriteLine("Enter the age:");age = Convert.ToInt32(Console.ReadLine()); } public  void Show() {            Console.WriteLine("Student name is:{0}",name);            Console.WriteLine("Age is:{0}",age); } } class Program { static  void Main(string[] args) {Student s =  new Student();                s.AddValue();                s.Show();                Console.Read(); } }} |

When the code is compiled and executed, the output is:

Enter the student name:

Harry

Enter the age:

15

Student name is: Harry

Enter the age: 15

Protected access specifier

Protected access specifier allows the class to hide the member variables and functions from other class objects and functions, except from child classes. The specifier is useful during the implementation of inheritance.

Example:

| ![](Images/image00305.jpeg)Example 40: |
| using System;namespace protected1{ class Employee { //member variables protected  string name; public  void AddValue() {            Console.WriteLine("Enter the employee name:");name = Console.ReadLine(); } public  void Show() {            Console.WriteLine("Employee name is:{0}",name); } } class Program { static  void Main(string[] args) {Employee e =  new Employee();                e.AddValue();                e.Show();                Console.Read(); } }} |

When the code is compiled and executed, the output is:

Enter the employee name:

Ajay

Employee name is: Ajay

Internal access specifier

Internal access specifier allows a class to expose its member functions and variables to the containing child classes or classes within the same application.

Example:

| ![](Images/image00305.jpeg)Example 41: |
| using System;namespace internal1{ class Location { //member variables internal  string city; public  void AddValue() {            Console.WriteLine("Enter the city name:");name = Console.ReadLine(); } public  void Show() {            Console.WriteLine("City name is:{0}",name); } } class Program { static  void Main(string[] args) {Location l =  new Location();                l.AddValue();                l.Show();                Console.Read(); } }} |

When the code is compiled and executed, the output is:

Enter the city name:

London 

City name is: London

Protected Internal access specifier

The protected internal access specifier allows a class to expose the member functions and variables to the containing class, child class, or classes in same application. The access to the derived classes outside the application is allowed.

Example:

| ![](Images/image00305.jpeg)Example 42: |
| using System;namespace protectedinternal1{ class number { //member variables protected  internal  int no; public  void AddValue() {            Console.WriteLine("Enter the number:");no = Convert.ToInt32(Console.ReadLine()); } public  void Show() {            Console.WriteLine("Number is:{0}",no); } } class Program { static  void Main(string[] args) {number n =  new number();                n.AddValue();                n.Show();                Console.Read(); } }} |

When the code is compiled and executed, the output is:

Enter the number:

10

Number is: 10

## 11.3 Polymorphism

Polymorphism is the ability of the function to exist in different forms. The word ‘poly’ means many and ‘morphos’ means forms.

There are two types of polymorphism:

*   Static: The response to a function is decided at compile time
*   Dynamic: The response to function is decided at run time

## 11.4 Static Polymorphism

The static polymorphism refers to entity which exists in different forms. C# has two approaches for implementing polymorphism.

*   Function overloading
*   Operator overloading

Function overloading

Function overloading helps a user to use the similar name for two or more functions. The function definition must be different from each other by type or number of arguments in the list.

Example:

| ![](Images/image00305.jpeg)Example 43: |
| using system;namespace calculate{ class calculate { public  int Min(int no1,  int no2) { if(no1 < no2) { return no1; } else { return no2; } } public  float Min(int no1,  int no2) { if(no1 < no2) { return no1; } else { return no2; } } class Program { static  void Main(string[] args) {Program p =  new Program();                Console.WriteLine("Minimum value is:{0}",p.Min(3,4));    Console.WriteLine("Minimum value is:{0}",     p.Min(3.2F,1.2F));                Console.ReadLine(); } } }} |

When the code is compiled and executed, the output is:

Minimum value is: 3

Minimum value is: 1.2

## 11.5 Dynamic Polymorphism

C# has two approaches for implementing dynamic polymorphism. They are:

*   Abstract classes: They are unique type of base classes containing abstract class members. The class members derived from the abstract class must implement abstract functions and properties.
*   Virtual functions: They do not really exist. They appear to be present in some parts.

Abstract class

An abstract class provides partial implementation of the class. When the derived class inherits it, the implementation is completed. There are abstract methods which are implemented using derived class.

Rules for abstract class creation

*   User cannot declare an abstract method outside the abstract class
*   The instance of the abstract class cannot be created
*   A class derived from an abstract class must override all the methods of the class
*   The abstract class cannot be declared as sealed

Example:

| ![](Images/image00305.jpeg)Example 44: |
| using Systemnamespace poly{ abstract  class Result { public  abstract  int average(); } class Data: Result { private  int sub1; private  int sub2; public Data(int x,  int y) {sub1 = x;sub2 = y; } public  override  int average() {            Console.WriteLine("The average is:"); return  (x + y /  2); } } class Program { static  void Main(string[] args) {Data d =  new Data(30,  70); int a = d.average();            Console.WriteLine("Average:{0}",a);            Console.Read(); } }} |

When the code is compiled and executed, the output is:

The average is:

Average: 50

Virtual Functions

If you need a function that is defined in a class and needs to be implemented by an  inherited class, the virtual function is used. The inherited class modifies the functionality of the inherited class depending on the requirement. The call to method is at runtime.

The virtual keyword is used before the return type of the function.

Example:

| ![](Images/image00305.jpeg)Example 45: |
| using System;namespace virtual1{ class Calculate { protected  int x, y; public Calculate(int l =  0,  int m =  0) {x = l;y = m; } public  virtual  int operation { return  0; } } classMultiplication : Calculate { public Multiplication (int l =  0,  int m =  0):base(l,m) { } public  override  int operation() {            Console.WriteLine("Multiplication is:"); return x * y; } } classAddition : Calculate { public Addition (int l =  0,  int m =  0):base(l,m) { } public  override  int operation() {            Console.WriteLine("Addition is:"); return x + y; } } class call { public  void callvalue(Calculate c) { int z;z = c.operation();            Console.WriteLine("Result:{0}",z); } } class Program { static  void Main(string[] args) {call p =  new call();Multiplication m =  new Multiplication(10,2);Addition t =  new Addition(15,16);            p.callvalue(m);            p.callvalue(t);            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Multiplication is:

Result: 20

Addition is:

Result: 31

Chapter 12 Inheritance and Interfaces

## 12.1 Introduction to Inheritance

The concept of inheritance is fundamental to not only C# but also to most other programming languages. It allows the user to create classes that inherit data members and methods from other classes. Inheritance can save the user time by allowing them to create several popular and well-used methods in a core class and have other classes inherit that core class and all its methods. This stops the user from repeating the same method in every class.

## 12.2 Base and derived classes

The structure of inheritance can be summed up in a few ways, for this example we have three classes A, B and C. The class B is derived from the class A. The class C is derived from class B. So what does this mean?

If we symbolize the relationship of these classes then we could show it like this:

Class A Class B   Class C

*   Since class B is derived from class A, we say that class A is the parent of class B. We can also say that class B is the child of class A.

*   Since class C is derived from class B, we say that class B is the parent of class C. We can also say that class C is the child of class B.

*   Since class C is derived from class B, which in turn is derived from class A, we say that class A is the grandparent of class C. We can also say that class C is the grandchild of class A.

*   In this instance since class A does not inherit from other classes, this class would be called the base class. Class B and class C would be declared as derived classes.

In this instance we have used the metaphor of parent and child to represent the relationship between the different classes but you will also encounter other metaphors such as super class (base class) and sub classes (derived classes) that describe the same relations.

The following is the way we would declare these relationships in code:

<access – specifier> class <base_class>

{

              …..

}

class <derived_class> : <base_class>

{

              …..

}

Example:

| ![](Images/image00305.jpeg)Example 46: |
| using System;namespace inheritance1{ class Demo { public  void side(int s) {side = s; } protected  int side; } //Derived class class Area : Demo { public  int  getAreaOfSquare() { return  s  * s; } }    clas Program { static  void Main(string[] args) {Area a =  new Area();            a.side(4);//Display the area of square            Console.WriteLine("Area is: {0}",a.getAreaOfSquare());            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Area is: 16

## 12.3 Base class initialization

When creating an inheritance structure the user must start with the base class (super class) first. Below is an example of how a base class is set up and how derived classes inherit from it.

Example:

| ![](Images/image00305.jpeg)Example 47: |
| using System;namespace Base1{ class Square { //member variables protected  int side; public Square(int s) {side = s; } public  int CalculateArea() { return side * side; } public  void Show() {            Console.WriteLine("The value of side is:{0}",side);            Console.WriteLine("Area is:{0}",CalculateArea()); } } class Paint : Square { private  int amount; public Paint(int side):base(s) { } public  int Totalamount() { int amount;amount = CalculateArea *  50; return amount; } public  void Show() { base.Show();            Console.WriteLine("Total amount is:{0}",Totalamount()); } } class Program { static  void Main(string[] args) {Paint p =  new Paint(7);            p.Show();            Console.Read(); } }} |

When the code is compiled and executed, the output is:

The value of side is: 3

Area is: 9

Total amount is: 450

## 12.4 Interfaces in C#

An interface is an abstract base class that declares methods but do not declare any logic within the methods. Essentially interfaces can be described as contracts, which all classes that inherit it the interface must follow. Interfaces spell out what methods and attributes every derived class must have. If these methods are not present in the derived classes then an error will occur.

Declaring Interfaces

The interface keyword is used for declaring the interface. They have public as their default data type.

Example of interface declaration

public interface IInterface1

{

              void MethodToImplement();

}

Example:

| ![](Images/image00305.jpeg)Example 48: |
| using System;namespace interface1{ public  interface IStudentInfo { //interface members void ShowData(); } public  class StudentInfo : IStudentInfo { private  int srno; private  string name; private  string subject; public StudentInfo() {srno =  "";name =  "";subject =  ""; } public StudentInfo(int s,  string n,  string b) {srno = s;name = n;subject = b; } public  void ShowData() {            Console.WriteLine("Student no is:{0}",srno);            Console.WriteLine("Student name is:{0}",name);            Console.WriteLine("Subject is:{0}",subject); } } class Program { static  void Main(string[] args) {StudentInfo s =  new StudentInfo(10,"Alex","Maths");StudentInfo s1 =  new StudentInfo(20,"Adam","Science");            s.ShowData();            s1.ShowData();            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Student no is: 10

Student name is: Alex

Subject is: Maths

Student no is: 20

Student name is: Adam

Subject is: Science

## 12.5 Multiple inheritance in C#

Multiple inheritance is the practice of derived classes inheriting from two unrelated classes. This practice is not naturally supported in C#, however with the use of interfaces we can mimic the behavior of multiple inheritance to a certain degree.

Below is an example of this use of interfaces to simulate multiple inheritance:

| ![](Images/image00305.jpeg)Example 49: |
| using System;namespace multiple1{ class Area { protected  int  base; protected  int height; public  void setbase(int b) { base  = b; } public  void setheight(int h) {height = h; } } //Base class public  interface Paint { int amount(int area); } //Derived class class Triangle : Area,Paint { public  int getValue() { return  (  1/2  * b * h ); } public  int amount(int area) { return area *  50; } } class Program {Triangle t =  new Triangle(); int area;        t.setbase(4);        t.setheight(5);area = t.getValue(); //Display the area        Console.WriteLine("Area is:{0}",t.getValue());        Console.WriteLine("Total Paint cost is:{0}",t.amount());        Console.Read(); }} |

When the code is compiled and executed, the output is:

Area is: 10

Total Pain cost is: 500

Chapter 13 Operator overloading and exception handling

## 13.1 Introduction to Operator Overloading

The built in operators can be redefined or overloaded in C#. The overloaded operators are functions having an operator keyword. It is followed by the symbol for the operator to be defined. The overloaded operator has a return type and a parameter list.

Example:

| ![](Images/image00305.jpeg)Example 50: |
| using System;namespace operator1{ class Room { private  int length; private  int breadth; public  int getArea() { return length * breadth; } public  void setlen (int len) {length = len; } public  void setbread(int bread) {breadth = bread; } //+ operator is overloaded public  static Room operator  +  (Room r, Room s) {Room o =  new Room();            o.length = r.length + s.length;            o.breadth = r.bread + s.bread; return o; } } class Program {   public  static  void Main(string[] args) {Room o1 =  new Room();Room o2 =  new Room();Room o3 =  new Room(); int area =  0; //Room 1 specification                o1.setlen(10);                o1.setbread(5); //Room 2 specification                o2.setlen(5);                o2.setbread(10); //area of room 1area = o1.getArea();                Console.WriteLine("Area of Room 1 is:{0}",area); //area of room2area = o2.getArea();                Console.WriteLine("Area of Room 2 is:{0}",area); //Adding two objectso3 = o1 + o2; //Area of Room 3area = o3.getArea();                Console.WriteLine("Area of Room 3 is:{0}",area);                Console.Read(); } }} |

When the code is compiled and executed, the output is:

Area of Room 1 is: 50

Area of Room 2 is: 150

Area of Room 3 is: 225

## 13.2 Different operators in overloading

The operators that can be overloaded in C# are as mentioned below:

| Operators | Description |
| +, -,*,/,% | Binary operators has two operands and can be overloaded |
| +,-,!,~,++,-- | Unary operators take one operand and can be overloaded |
| &&, &#124;&#124; | Conditional logical operators. They cannot be overloaded directly |
| ==, !=, <,>,<=,>= | Comparison operators. They cannot be overloaded |
| =, . , ?: , new, is, sizeof, typeof | They cannot be overloaded |
| +=, -=, *=, /=, %= | Assignment operators and cannot be overloaded |

## 13.3 Introduction to exception handling

An exception is an error that occurs during the execution of a program. The exception occurs when an operation is not completed normally, thus the system throws an error when an exception occurs.

C #exception handling is based on four keywords: try, catch, finally and throw.

*   try: Try block checks the block of code for a particular exception when activated. One or more catch blocks are present.
*   catch: The catch keyword is used to catch the exceptions. A program catches an exception at a place in the program where user wants to handle the issue.
*   finally: The finally block is used to execute statements even if the exception is thrown or not.
*   throw: The throw keyword is used to throw an exception.

Syntax:

try

{

     //statements causing exception

}

catch( ExceptionName e1 )

{

     //error handling code

}

catch( ExceptionName e2 )

{

     //error handling code

}

catch( ExceptionName eN )

{

     //error handling code

}

finally

{

      //statements to be executed

}

## 13.4 Exception classes in C#

There are several exception classes which are directly or indirectly derived from the System.Exception class. Some of the classes that are derived from the System.Exception class are System.ApplicationException and System.SystemException classes.

For a user-defined application having its own exception, the exception must be inherited from the ApplicationException class.

The System.SystemException class is the base class for all exceptions.

| Exception class | Description |
| System.IO.IOException | It handles the I/O Errors |
| System.NullReferenceException | Errors generated during the process of dereferencing a null object |
| System.IndexOutOfRangeException | Errors generated when a method refers an array element out of bound |
| System.DivideByZeroException | Errors generated during the process of dividing the dividend by zero |
| System.OutOfMemoryException | Memory allocation to the application errors |
| System.InvalidCastException | Errors due to type casting |
| System.StackOverflowException | The errors generated due to stack overflow |

## 13.5 Exception handling

The structured solution in the form of try and catch block is provided by C#. The core program statements are divided from the error handling statements. The finally block is used to handle errors.

Example:

| ![](Images/image00305.jpeg)Example 51: |
| using System;namespace DivNumbers{ class Divide { int output;        Divide() {output =  0; } public  void division(int no1,  int no2) { try {output = no1 / no2; } catch(DivideByZeroException e) {                Console.WriteLine("Exception handled:{0}",e); } finally {                Console.WriteLine("Output is:{0}",output); } } public  static  void Main(string[] args) {Divide d =  new Divide();            d.division(5,0);            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Exception handled: System.DivideByZeroException: Attempted to divide by zero

Output is: 0

## 13.6 User defined exceptions

Users can create their own exception classes when the situation arises where the user needs to handle an exception in a special way using custom code. These exceptions are known as user defined exceptions.

The user defined exceptions classes are derived from the ApplicationException class.

| ![](Images/image00305.jpeg)Example 52: |
| using System;namespace userdefined{ class Average { static  void Main(string[] args) {Perform p =  new Perform(); try {                p.CalAverage(); } catch(CountZeroException e) {                Console.WriteLine("CountZeroException: {0}",e.Message); }            Console.Read(); } }}public  class CountZeroException:ApplicationException{ public CountZeroException(string message):base(message) { }}public  class Perform{ int no1 =  0; int count =  0; float average; public  void CalAverage() { if(count ==  0) { throw(new CountZeroException("Count is zero in calculation")); else {average = no1 / count; } } }} |

When the code is compiled and executed, the output is:

CountZeroException: Count is zero in calculation

Chapter 14 Multithreading

## 14.1 Thread in C#

A thread defines a control flow. Thread is a basic unit to which the operating system allocates a thread. The execution of a thread is independent within a program.

A single process is executed using one thread. Such process is known as single – threaded process. Only one task can be performed at a time. The user has to wait for the task to complete before executing new task.

For executing more than one thread at a time, multiple threads are created. The process creating two or more threads is known as multithreading.

## 14.2 Life cycle of a thread

The life cycle of a thread starts when the object of System.Threading.Thread class is created. The life ends as soon as the task is completed. There are various states in the life cycle of a thread.

*   Unstarted State: When the instance of the Thread class is created, the thread enters in unstarted state.

*   Ready State: The thread is in this state till the program calls the Start() method.

*   Not Runnable State: A thread is not in the runnable state if:

1.  1.  Waiting: The Wait() method is called to make the thread for a specified condition
    2.  Blocked: The thread is blocked by an I/O operation
    3.  Sleeping: The Sleep() method is called to put the thread in sleeping mode.

*   Dead State: Once the thread completes its execution or aborted, it is placed in a dead state

## 14.3 Main thread

The System.Threading.Thread class is used for working with threads. The main thread is created as soon as program starts execution. The Thread class is used for creating threads. They are known as child threads. The user can access the main thread by using the CurrentThread property of the Thread class.

Example:

| ![](Images/image00305.jpeg)Example 53: |
| using System;namespace thread{ class MainThread { static  void Main(string[] args) {Thread t1 =  new Thread();            t1.Name="Thread1";            Console.WriteLine("Thread is:{0}",t1.Name);            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Thread is: Thread1

## 14.4 Properties and methods of the Thread class

Properties:

*   IsAlive: The value showing the execution status of the current thread
*   CurrentThread: The current running thread is retrieved
*   CurrentContext: The current context in which the thread is executing is retrieved
*   ExecutionContext: The ExecutionContext object contains information about different contexts
*   Name: Gets or sets name of the thread
*   ThreadState: The value containing states of the current thread
*   Priority: It gets or sets the value showing the scheduling priority of a thread

Methods:

*   public static void BeginThreadAffinity(): The host is to about to execute instructions depending on the current physical operating system thread.
*   public void Abort(): The ThreadAbortException is raised in thread on which it is invoked.
*   public void interrupt(): The thread present in the WaitSleepJoin state is interrupted
*   public static AppDomain GetDomain(): A unique domain identifier is returned
*   public static void MemoryBarrier(): The processor executes the current thread. The instructions cannot be reordered.
*   public void Start(): It starts the thread
*   public static bool Yield(): The calling thread to yield execution to another thread which is ready to run on the processor

## 14.5 Creating and managing threads

The extended thread class creates a thread. The extended thread class calls the Start() method to start the child thread execution.

Example:

| ![](Images/image00305.jpeg)Example 54: |
| using System;using System.Threading;namespace MultipleThread{ class ThreadProgram { public  static  void CallChild() {            Console.WriteLine("Start child thread"); } static  void Main(string[] args) {ThreadStart child1 =  new ThreadStart(CallChild);            Console.WriteLine("Creating child thread");Thread child2 =  new Thread(child1);            child2.Start();            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Start child thread

Creating child thread

Managing Threads

When there is a need to pause a thread for a period of time so that another thread can execute, the Thread.Sleep() method is used. The method takes a single argument stating time in milliseconds.

Example:

| ![](Images/image00305.jpeg)Example 55: |
| using System;using System.Threading;namespace Multithreaded{ class Program { public  static  void ChildThread() {                Console.WriteLine("Start child thread"); int sleeptime =  4000;    Console.WriteLine("Thread sleeping for {0}   seconds",sleeptime /  1000);                Thread.Sleep(sleeptime);                Console.WriteLine("Resume child thread"); } public  static  void Main() {ThreadStart t1 =  new ThreadStart(ChildThread);            Console.WriteLine("child thread created");Thread child1 =  new Thread(t1);            child1.Start();            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Start child thread

Thread sleeping for 4 seconds

Resume child thread

child thread created

## 14.6 Destroying threads

The Thread.Abort() method is used to destroy the thread. The ThreadAbortException is thrown when the thread is destroyed. The exception is not caught and is sent to the finally block.

Example:

| ![](Images/image00305.jpeg)Example 56: |
| using System;using System.Threading;namespace ThreadDemo{ class Program { public  static  void ChildThread() { try {                Console.WriteLine("Child Thread started"); for(int j =  0; j <  =  10; j ++) {                    Thread.Sleep(1000);                    Console.WriteLine("Child thread finished"); } } catch(ThreadAbortException e) {                Console.WriteLine("Exception caught"); } finally {                Console.WriteLine("Exception is not handled"); } } public  static  void Main() {ThreadStart t1 =  new ThreadStart(ChildThread);            Console.WriteLine("Creating child thread");Thread t2 =  new Thread(t1);            t1.Start(); //main thread is stopped            Thread.Sleep(2000); //child thread aborted            Console.WriteLine("Aborting child thread");            t2.Abort();            Console.Read(); } }} |

When the code is compiled and executed, the output is:

Creating child thread

Child Thread started

0

1

Aborting child thread

Exception caught

Exception is not handled

Reference links on C#

User can get more detailed information about the C# language using the following reference links.

*   [Visual Studio Application](https://www.visualstudio.com/downloads/download-visual-studio-vs) – The IDE for creating C# applications.
*   [C# ( Programming guide )](https://en.wikipedia.org/wiki/C_Sharp_(programming_language)) – An overview of C# programming language
*   [C# Programming](https://msdn.microsoft.com/en-us/library/67ef8sbd.aspx) – The information about the C# features using .NET framework is explained
*   [Mono](http://www.mono-project.com/) – Cross platform applications can be easily created using the software.
*   [C# Complete tutorial](http://www.csharp-station.com/tutorial.aspx) – It contains lessons useful for beginners to learn C# language

Conclusion

This brings us to the end of this book. We hope that this guide has been thoroughly comprehensible and easy for you to understand and follow. The book should not end your journey on the road to learning C#, instead it should only serve as the beginning. There is a vast amount of information that you can learn on C# therefore once you are done with this book, explore further boundaries of C#.

C# has a growing popularity and is steadily being used more and more. Many famous sites and enterprise level applications are powered by C#. You can find C# in the scientific computing being run on supercomputers. System administration tasks such as package management and configuration use C# as well. No matter what your programming interests, the possibilities for learning, exploring, and growing are endless.