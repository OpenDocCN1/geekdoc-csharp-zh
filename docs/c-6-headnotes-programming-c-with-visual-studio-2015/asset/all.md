![](images/00228.jpeg)

C# 6 HEADNOTES, PROGRAMMING C# WITH VISUAL STUDIO 2015

ALL RIGHTS RESERVED. NO PART OF THIS BOOK MAY BE REPRODUCED, IN ANY FORM OR BY ANY MEANS, WITHOUT PERMISSION IN WRITING FROM THE PUBLISHER.

Table of Contents

[I. Getting Started with C#](#part0000_split_002.html__Toc438114308)

[1. What can I do with C#?](#part0000_split_003.html__Toc438114309)

[2. What is .NET?](#part0000_split_004.html__Toc438114310)

[II. Language Guide](#part0000_split_005.html__Toc438114311)

[1. First Steps](#part0000_split_005.html__Toc438114312)

[1.1. Your First Program](#part0000_split_005.html__Toc438114313)

[1.2. C# Coding Conventions](#part0000_split_005.html__Toc438114314)

[2. Constants and Variables](#part0000_split_006.html__Toc438114315)

[2.1. Declaring Constants and Variables](#part0000_split_006.html__Toc438114316)

[3. Primitive Types](#part0000_split_007.html__Toc438114317)

[3.1. Using Mathematical and Logical Operators](#part0000_split_007.html__Toc438114318)

[4. Making Decisions](#part0000_split_008.html__Toc438114319)

[4.1. Making decisions using the if Statement](#part0000_split_008.html__Toc438114320)

[4.2. Making decisions using the if-else Statement](#part0000_split_008.html__Toc438114321)

[4.3. Using Relational Operators in if Statements](#part0000_split_008.html__Toc438114322)

[4.4. Using Logical Condition Operators in if Statements](#part0000_split_008.html__Toc438114323)

[4.5. Making decisions using the switch Statement](#part0000_split_008.html__Toc438114324)

[4.6. Increment and Decrement Operators](#part0000_split_008.html__Toc438114325)

[5. Arrays](#part0000_split_009.html__Toc438114326)

[5.1. Arrays as objects](#part0000_split_009.html__Toc438114327)

[5.2. Single-dimensional Arrays](#part0000_split_009.html__Toc438114328)

[5.3. Multidimensional Arrays](#part0000_split_009.html__Toc438114329)

[5.4. Jagged Arrays](#part0000_split_009.html__Toc438114330)

[5.5. Passing Arrays as arguments](#part0000_split_009.html__Toc438114331)

[6. Looping](#part0000_split_010.html__Toc438114332)

[6.1. Using the for loop](#part0000_split_010.html__Toc438114333)

[6.2. Using the foreach loop](#part0000_split_010.html__Toc438114334)

[Using the while loop](#part0000_split_010.html__Toc438114335)

[6.3. Using the do-while loop](#part0000_split_010.html__Toc438114336)

[7. Classes and Structs](#part0000_split_011.html__Toc438114337)

[7.1. Classes](#part0000_split_011.html__Toc438114338)

[7.2. Structs](#part0000_split_011.html__Toc438114339)

[7.3. Objects](#part0000_split_011.html__Toc438114340)

[7.4. Members](#part0000_split_011.html__Toc438114341)

[7.5. Encapsulation](#part0000_split_011.html__Toc438114342)

[7.6. Inheritance](#part0000_split_011.html__Toc438114343)

[7.7. Polymorphism](#part0000_split_011.html__Toc438114344)

[7.8. Abstract and Sealed Classes and Class Members](#part0000_split_011.html__Toc438114345)

[7.9. Static Classes and Static Class Members](#part0000_split_011.html__Toc438114346)

[7.10. Access Modifiers](#part0000_split_011.html__Toc438114347)

[8. Delegates](#part0000_split_012.html__Toc438114348)

[9. Events](#part0000_split_013.html__Toc438114349)

[10. Lambdas](#part0000_split_014.html__Toc438114350)

[11. Enumeration Types](#part0000_split_015.html__Toc438114351)

[12. Exceptions and Exception Handling](#part0000_split_016.html__Toc438114352)

[12.1. Using Exceptions](#part0000_split_016.html__Toc438114353)

[12.2. Exception Handling](#part0000_split_016.html__Toc438114354)

[12.3. Creating and Throwing Exceptions](#part0000_split_016.html__Toc438114355)

[12.4. Compiler-Generated Exceptions](#part0000_split_016.html__Toc438114356)

[12.5. Handle an Exception using try/catch](#part0000_split_016.html__Toc438114357)

[12.6. Execute Cleanup code using finally](#part0000_split_016.html__Toc438114358)

[13. File System and Registry](#part0000_split_017.html__Toc438114359)

[13.1. Iterating Through a Directory Tree](#part0000_split_017.html__Toc438114360)

[13.2. Getting Information about Files, Folders, and Drives](#part0000_split_017.html__Toc438114361)

[13.3. Creating a File or Folder](#part0000_split_017.html__Toc438114362)

[13.4. Copy, Delete, and Move Files and Folders](#part0000_split_017.html__Toc438114363)

[13.5. Providing a Progress Dialog Box for File Operations](#part0000_split_017.html__Toc438114364)

[13.6. Writing to a Text File](#part0000_split_017.html__Toc438114365)

[13.7. Reading from a Text File](#part0000_split_017.html__Toc438114366)

[13.8. Reading a Text File One Line at a Time](#part0000_split_017.html__Toc438114367)

[13.9. Creating a Key in the Registry](#part0000_split_017.html__Toc438114368)

[14. Generics](#part0000_split_018.html__Toc438114369)

[14.1. Introduction to Generics](#part0000_split_018.html__Toc438114370)

[14.2. Generic Type Parameters](#part0000_split_018.html__Toc438114371)

[14.3. Constraints on Type Parameters](#part0000_split_018.html__Toc438114372)

[14.4. Generic Classes](#part0000_split_018.html__Toc438114373)

[14.5. Generic Interfaces](#part0000_split_018.html__Toc438114374)

[14.6. Generic Methods](#part0000_split_018.html__Toc438114375)

[14.7. Generics and Arrays](#part0000_split_018.html__Toc438114376)

[14.8. Generic Delegates](#part0000_split_018.html__Toc438114377)

[14.9. Default Keyword](#part0000_split_018.html__Toc438114378)

[15. Indexers](#part0000_split_019.html__Toc438114379)

[15.1. Using Indexers](#part0000_split_019.html__Toc438114380)

[15.2. Indexers in Interfaces](#part0000_split_019.html__Toc438114381)

[16. Interfaces](#part0000_split_020.html__Toc438114382)

[17. LINQ Query Expressions](#part0000_split_021.html__Toc438114383)

[17.1. Querying Collections](#part0000_split_021.html__Toc438114384)

[17.2. Filtering Data](#part0000_split_021.html__Toc438114385)

[17.3. Ordering Collections](#part0000_split_021.html__Toc438114386)

[17.4. Joining Objects](#part0000_split_021.html__Toc438114387)

[18. Main () and Command-Line Arguments](#part0000_split_022.html__Toc438114388)

[19. Namespaces](#part0000_split_023.html__Toc438114389)

[20. Nullable Types](#part0000_split_024.html__Toc438114390)

[20.1. Using Nullable Types](#part0000_split_024.html__Toc438114391)

[20.2. Boxing Nullable Types](#part0000_split_024.html__Toc438114392)

[20.3. Identifying a Nullable Type](#part0000_split_024.html__Toc438114393)

[20.4. Safely Cast from bool? to bool](#part0000_split_024.html__Toc438114394)

[21. Statements, Expression and Operators](#part0000_split_025.html__Toc438114395)

[21.1. Statements](#part0000_split_025.html__Toc438114396)

[21.2. Expressions](#part0000_split_025.html__Toc438114397)

[21.3. Anonymous Functions](#part0000_split_025.html__Toc438114398)

[21.3.1. Lambda Expression](#part0000_split_025.html__Toc438114399)

[21.3.2. Anonymous Methods](#part0000_split_025.html__Toc438114400)

[21.4. Overloadable Operators](#part0000_split_025.html__Toc438114401)

[21.5. Conversion Operators](#part0000_split_025.html__Toc438114402)

[21.6. Using Operator Overloading to Create a Complex Number Class](#part0000_split_025.html__Toc438114403)

[21.7. Equality Comparisons](#part0000_split_025.html__Toc438114404)

[22. Strings](#part0000_split_026.html__Toc438114405)

[22.1. Concatenate Multiple Strings](#part0000_split_026.html__Toc438114406)

[22.2. Modify String Contents](#part0000_split_026.html__Toc438114407)

[22.3. Compare Strings](#part0000_split_026.html__Toc438114408)

[22.4. Parse Strings Using String.Split](#part0000_split_026.html__Toc438114409)

[22.5. Search Strings Using String Methods](#part0000_split_026.html__Toc438114410)

[22.6. Search Strings Using Regular Expressions](#part0000_split_026.html__Toc438114411)

[22.7. Determine Whether a String Represents a Numeric Value](#part0000_split_026.html__Toc438114412)

[22.8. Convert a String to a DateTime](#part0000_split_026.html__Toc438114413)

[22.9. Convert Between Legacy Encodings and Unicode](#part0000_split_026.html__Toc438114414)

[22.10. Convert RTF to Plain Text](#part0000_split_026.html__Toc438114415)

[23. Unsafe Code and Pointers](#part0000_split_027.html__Toc438114416)

[23.1. Fixed Size Buffers](#part0000_split_027.html__Toc438114417)

[23.2. Pointer types](#part0000_split_027.html__Toc438114418)

[24. XML Documentation Comments](#part0000_split_028.html__Toc438114419)

[24.1. Recommended Tags for Documentation Comments](#part0000_split_028.html__Toc438114420)

[24.2. Processing the XML File](#part0000_split_028.html__Toc438114421)

[24.3. Delimiters for Documentation Tags](#part0000_split_028.html__Toc438114422)

[III. Coding standards and naming conventions](#part0000_split_029.html__Toc438114423)

[1. Do](#part0000_split_030.html__Toc438114424)

[2. Don’t](#part0000_split_031.html__Toc438114425)

[3. Avoid](#part0000_split_032.html__Toc438114426)

# I. Getting Started with C#

C# is an elegant and type-safe object-oriented language that enables developers to build a variety of secure and robust applications that run on the .NET Framework. You can use C# to create Windows client applications, XML Web services, distributed components, client-server applications, database applications, and much, much more. Visual C# provides an advanced code editor, convenient user interface designers, integrated debugger, and many other tools to make it easier to develop applications based on the C# language and the .NET Framework.

## 1. What can I do with C#?

C# syntax is highly expressive, yet it is also simple and easy to learn. The curly-brace syntax of C# will be instantly recognizable to anyone familiar with C, C++ or Java. Developers who know any of these languages are typically able to begin to work productively in C# within a very short time. C# syntax simplifies many of the complexities of C++ and provides powerful features such as nullable value types, enumerations, delegates, lambda expressions and direct memory access, which are not found in Java. C# supports generic methods and types, which provide increased type safety and performance, and iterators, which enable implementers of collection classes to define custom iteration behaviors that are simple to use by client code. Language-Integrated Query (LINQ) expressions make the strongly-typed query a first-class language construct.

As an object-oriented language, C# supports the concepts of encapsulation, inheritance, and polymorphism. All variables and methods, including the Main method, the application's entry point, are encapsulated within class definitions. A class may inherit directly from one parent class, but it may implement any number of interfaces. Methods that override virtual methods in a parent class require the override keyword as a way to avoid accidental redefinition. In C#, a struct is like a lightweight class; it is a stack-allocated type that can implement interfaces but does not support inheritance.

In addition to these basic object-oriented principles, C# makes it easy to develop software components through several innovative language constructs, including the following:

*   Encapsulated method signatures called delegates, which enable type-safe event notifications.
*   Properties, which serve as accessors for private member variables.
*   Attributes, which provide declarative metadata about types at run time.
*   Inline XML documentation comments.

Language-Integrated Query (LINQ) which provides built-in query capabilities across a variety of data sources.

If you have to interact with other Windows software such as COM objects or native Win32 DLLs, you can do this in C# through a process called "Interop." Interop enables C# programs to do almost anything that a native C++ application can do. C# even supports pointers and the concept of "unsafe" code for those cases in which direct memory access is absolutely critical.

The C# build process is simple compared to C and C++ and more flexible than in Java. There are no separate header files, and no requirement that methods and types be declared in a particular order. A C# source file may define any number of classes, structs, interfaces, and events.

The following are additional C# resources:

*   For a good general introduction to the language, see Chapter 1 of the C# Language Specification.
*   For detailed information about specific aspects of the C# language, see the C# Reference.
*   For more information about LINQ, see LINQ (Language-Integrated Query).
*   To find the latest articles and resources from the Visual C# team, see the Visual C# Developer Center.

## 2. What is .NET?

C# programs run on the .NET Framework, an integral component of Windows that includes a virtual execution system called the common language runtime (CLR) and a unified set of class libraries. The CLR is the commercial implementation by Microsoft of the common language infrastructure (CLI), an international standard that is the basis for creating execution and development environments in which languages and libraries work together seamlessly.

Source code written in C# is compiled into an intermediate language (IL) that conforms to the CLI specification. The IL code and resources, such as bitmaps and strings, are stored on disk in an executable file called an assembly, typically with an extension of .exe or .dll. An assembly contains a manifest that provides information about the assembly's types, version, culture, and security requirements.

When the C# program is executed, the assembly is loaded into the CLR, which might take various actions based on the information in the manifest. Then, if the security requirements are met, the CLR performs just in time (JIT) compilation to convert the IL code to native machine instructions. The CLR also provides other services related to automatic garbage collection, exception handling, and resource management. Code that is executed by the CLR is sometimes referred to as "managed code," in contrast to "unmanaged code" which is compiled into native machine language that targets a specific system. The following diagram illustrates the compile-time and run-time relationships of C# source code files, the .NET Framework class libraries, assemblies, and the CLR.

Language interoperability is a key feature of the .NET Framework. Because the IL code produced by the C# compiler conforms to the Common Type Specification (CTS), IL code generated from C# can interact with code that was generated from the .NET versions of Visual Basic, Visual C++, or any of more than 20 other CTS-compliant languages. A single assembly may contain multiple modules written in different .NET languages, and the types can reference each other just as if they were written in the same language.

In addition to the run time services, the .NET Framework also includes an extensive library of over 4000 classes organized into namespaces that provide a wide variety of useful functionality for everything from file input and output to string manipulation to XML parsing, to Windows Forms controls. The typical C# application uses the .NET Framework class library extensively to handle common "plumbing" chores.

# II. Language Guide

## 1. First Steps

### 1.1. Your First Program

We will follow the tradition in a new language and start with a first program that prints the words “Hello World!” on the screen. In C# this could be made in a single line:

![](images/00001.jpeg)

And our Main method should look like this, Press F5 to build and run the program:

![](images/00002.jpeg)

![](images/00003.jpeg)To insertConsole.WriteLine(); line, just type the shortcut cw and then Press TAB TAB to invoke the code snippet

### 1.2. C# Coding Conventions

As part of the best practices of the C# Programming Language, to enable readers to understand the code more quickly, create consistent look and facilitate copying and change the code, even if:

Copy and paste is a design error. – David Parnas

We need to have a minimum of knowledge of some of these conventions to be able to write a good code.

#### 1.2.1. Naming Conventions

In short examples, without using directives, use namespace qualifications.

![](images/00004.jpeg)

#### 1.2.2. Commenting Conventions

Place a comment in a separate line, not at the end. It should begin with uppercase letter, each line with one space and it ends with a period.

![](images/00005.jpeg)

## 2. Constants and Variables

Constants and variables associate a name with a value of particular type. The value of a constant cannot be changed once it is set, whereas a variable can be set to a different value in the future.

### 2.1. Declaring Constants and Variables

Constants and variables must be declared before they are used.Useconst  keyword for declaring constants, declare anonymous variable with the keywordvar  and dynamic variable with thedynamic  keyword.

![](images/00006.jpeg)

var  is static typed, the compiler and runtime know the type.

![](images/00007.jpeg)

dynamic  is very different beast, it is most similar to object, but with dynamic dispatch.

![](images/00008.jpeg)

## 3. Primitive Types

The primitive types are identified by keywords predefined under the System namespace.  These keywords are considered as reserved words.

Primitive types permit values to be created literally:

![](images/00009.jpeg)

C# defines the following primitive types:

| Struct / Class | Data Type | Description | Range |
| struct  System.Byte | byte | 8-bit unsigned integer | 0 .. 255 |
| struct  System.SByte | sbyte | 8-bit signed integer | -128 .. 127 |
| struct  System.Int16 | short | 16-bit signed integer | -32,768 .. 32,767 |
| struct  System.UInt16 | ushort | 16-bit unsigned integer | 0 .. 65,535 |
| struct  System.Int32 | int | 32-bit signed integer | -2,147,483,648 .. 2,147,483,647 |
| struct  System.UInt32 | uint | 32-bit unsigned integer | 0 .. 4,294,967,295 |
| struct  System.Int64 | long | 64-bit signed integer | -9,223,372,036,854,775,808 .. 9,223,372,036,854,775,807 |
| struct  System.UInt64 | ulong | 64-bit unsigned integer | 0 .. 18,446,744,073,709,551,615 |
| struct  System.Single | float | A single precision floating point number | -3.402823e38 .. 3.402823e38 |
| struct  System.Double | double | A double precision floating point number | -1.79769313486232 e308 .. 1.79769313486232 e308 |
| struct  System.Decimal | decimal | A Decimal number | -79228162514264337593543950335 .. 79228162514264337593543950335 |
| struct  System.Char | char | A character as UTF-16 code unit | A Unicode character. |
| classSystem.String | string | Text as a series of Unicode characters | A string of Unicode characters. |
| struct  System.Boolean | bool | A Boolean value | True or False. |
| classSystem.Object | object | Supports all classes in the .NET Framework class hierarchy and provides low-levelservices to derived classes. | An object. |

### 3.1. Using Mathematical and Logical Operators

The following is a list of the basic mathematical operators, listed in order of precedence. Use parentheses to force other ordering:

| Operator | Purpose |
| *,/,% | Multiplication, Division, Modulus |
| +,- | Addition , Subtraction |
| & | Logical AND |
| ^ | Logical XOR |
| &#124; | Logical OR |

![](images/00010.jpeg)

![](images/00003.jpeg)Use predefined type names instead of system type names like Int16, Single, UInt64, etc which will makes code more natural to read.

![](images/00011.jpeg)

Floating point puzzle
![](images/00012.jpeg)But always remember, it’s not a bug – it’s an undocumented feature!

![](images/00013.jpeg)

## 4. Making Decisions

You have the ability to change the flow of an application according to a condition that will be tested.

### 4.1. Making decisions using the if Statement

This one is the simplest form of conditional branching. If the condition is verified, then the code inside the if statement will be executes.

![](images/00014.jpeg)

### 4.2. Making decisions using the if-else Statement

You can use if-else statement to verify different possibilities and conditions sequentially:

![](images/00015.jpeg)

![](images/00003.jpeg)If you have only one block of if-else to verify, and the result will be one of two values to return, you can verify that with short notation of this block using the ?: operator.

![](images/00016.jpeg)

### 4.3. Using Relational Operators in if Statements

These operators compare two values and return abool  value:

| Operator | Purpose |
| == | Checks for equality. |
| != | Checks for inequality. |
| > | Greater than. |
| < | Less than. |
| >= | Greater than or equal to. |
| <= | Less than or equal to. |

![](images/00017.jpeg)

### 4.4. Using Logical Condition Operators in if Statements

The logical operators are used to evaluate different conditions at a time in logic statement.

| Operator | Purpose |
| && | Conditional AND |
| &#124;&#124; | Conditional OR |
| ! | Conditional NOT |

#### 4.4.1. Using the Conditional AND Operator

The logical condition operator && is a “short-circuit” evaluation of the logical operator &. Means in a statement x && y if x is falsebecause the result of the AND-Operation is false no matter the value of y. To be clear in a logic statement ofbool  variables a,b,c..z given by a && b && c .. && z at the first false variable, the processor will stop evaluating the expression and the result will be false.

![](images/00018.jpeg)

#### 4.4.2. Using the Conditional OR Operator

The logical condition operator || is a “short-circuit” evaluation of the logical operator |. Means in a statement x || y if x is truebecause the result of the OR-Operation is false no matter the value of y. To be clear in a logic statement ofbool  variables a,b,c..z given by a || b || c .. || z at the first true variable, the processor will stop evaluating the expression and the result will be true.

![](images/00019.jpeg)

#### 4.4.3. Using the Conditional NOT Operator

It’s a unary operator for negation for logic expression orbool  variable return true if it return false and vice versa.![](images/00020.jpeg)

![](images/00021.jpeg)

### 4.5. Making decisions using the switch Statement

A switch statement is used for multiple actions depending on the value of a given expression. The code between the case and the break keywords is executed if the condition is met. To move from one case to another use the keyword goto.

![](images/00022.jpeg)

#### 4.5.1. Using an Enumeration with a switch Statement

Switch can act upon enum values. An enum switch sometimes results in clearer code. It sometimes is faster. This code pattern is often effective.

![](images/00023.jpeg)

![](images/00003.jpeg)To insert these lines of code, just type the shortcut switch and then Press TAB TAB to invoke the code snippet, followed by the enum instance or the enumeration and Press ENTER ENTER.

### 4.6. Increment and Decrement Operators

There are different shortcuts in C# that give you possibility to increase or decrease the value of your variable in postfix and prefix.

| Operator | Purpose |
| v++ | Increment variable v by 1. |
| v-- | Decrement variable v by 1. |
| v+=n | Increment variable v by n. |
| v-=n | Subtract n from variable v. |
| v*=n | Multiply variable v by n. |

![](images/00024.jpeg)

## 5. Arrays

An array is a systematic arrangement of similar objects, it’s recognized also as a data structure. It’s a collection of elements identified by at least one array index or key. At declaration, you need to specify the type of its elements.

![](images/00025.jpeg)

### 5.1. Arrays as objects

In C# Arrays are already objects, not like on C/C++. Therefore, you can use some predefined properties and methods and other class members.

![](images/00026.jpeg)

### 5.2. Single-dimensional Arrays

You can declare an empty single-dimensional array of n elements. The first value has the index of 0, and the last one of n-1.

![](images/00027.jpeg)

Or you can initialize the array with elements, in this case you don’t need to mention the array size.

![](images/00028.jpeg)

### 5.3. Multidimensional Arrays

If need to declare a multidimensional array of n dimension.

![](images/00029.jpeg)

You can still initialize a multidimensional array with values.

![](images/00030.jpeg)

### 5.4. Jagged Arrays

Jagged arrays are “Arrays of Arrays”, means that element of the array are themselves arrays. And in this case, in a multidimensional array, if we consider the main array as row, you can have different column size in each row.

![](images/00031.jpeg)

### 5.5. Passing Arrays as arguments

You can pass a Single-dimensional array or multidimensional one as arguments to method parameters.

![](images/00032.jpeg)

#### 5.5.1. Passing Arrays as parameters

You can use the keyword params if you would like to pass method parameters that you ignore how many arguments it will take. It’s passed as parameters array and you don’t need to declare the array when you call the method, it’s implicitly made by the C# compiler.

![](images/00033.jpeg)

![](images/00034.jpeg)Index initializers
Object and collection initializers are useful for declaratively initializing fields and properties of objects, or giving a collection an initial set of elements. Initializing dictionaries and other objects with indexers is less elegant.

![](images/00035.jpeg)

## 6. Looping

A loop is a set of statements that are repeated for a specified number of time or until a logical condition is met.

### 6.1. Using the for loop

The for-loop allows code to be executed repeatedly. Unlike other kinds of loops, the for-loop is distinguished by an explicit loop counter.

![](images/00036.jpeg)

### 6.2. Using the foreach loop

The foreach-loop gives the possibility for traversing items in a collection. Unlike for-loop, foreach-loop usually maintain no explicit counter. Here, how the same loop could be created with foreach-loop:

![](images/00037.jpeg)

### Using the while loop

![](images/00038.jpeg)

The while-loop allows code to be executed repeatedly based on a given Boolean condition.

![](images/00039.jpeg)

### 6.3. Using the do-while loop

![](images/00040.jpeg)

The do-while loop executes the code at least one time. Then repeatedly continue executing the code, or not, depending on given condition.

![](images/00041.jpeg)

## 7. Classes and Structs

Classes and Structs are two extensible program-code-template, a blueprint, for creating objects; providing initial values for state and implementations of behavior.

There is 4 major principles that a make a language object-oriented: Encapsulation, Data Abstraction, Polymorphism and Inheritance. These principles will be discussed later with examples.

### 7.1. Classes

Classes can be declared by using the keywordclass.All classes inherit fromSystem.Object, so classes are reference types.

![](images/00042.jpeg)

### 7.2. Structs

Structscan be declared by using the keywordstruct. All Structsinherit fromSystem.ValueType  which inherits fromSystem.Object, so Structs are value types.

![](images/00043.jpeg)

With a Struct:

*   Non const or static fields cannot be initialized.
*   Default Constructor (without parameters) or Destructor cannot be declared. But we can declare a Constructor that have parameters.
*   Can instantiate without the keyword new.
*   Can implement interfaces.
*   Can inherit from other Struct or class, but cannot be a base of a class.
*   Unlike other value types, it can be used as Nullable type.

### 7.3. Objects

Objects are instances of Classes or Structs. In the case of Classes they are created by using thenew  operator. With Structsthey can be created by using thenew  operator, but it’s not required.

![](images/00044.jpeg)

### 7.4. Members

#### 7.4.1. Fields

Fields are variables declared at class scope. A field may be a built-in numeric type or an instance of another class.

![](images/00045.jpeg)

#### 7.4.2. Constants

Constants are fields or properties whose value is set at compile time and cannot be changed.

![](images/00046.jpeg)

#### 7.4.3. Properties

Properties are methods on a class that are accessed as if they were fields on that class. A property can provide protection for a class field to keep it from being changed without the knowledge of the object.

![](images/00047.jpeg)

![](images/00048.jpeg)Initializers for auto-properties
You can now add an initializer to an auto-property, just as you can in a field.

![](images/00049.jpeg)

he initializer directly initializes the backing field; it doesn’t work through the setter of the auto-property. The initializers are executed in order as written, just as – and along with – field initializers.

![](images/00048.jpeg)Getter-only auto-properties
Auto-properties can now be declared without a setter.

![](images/00050.jpeg)

The backing field of a getter-only auto-property is implicitly declared as readonly (though this matters only for reflection purposes).

#### 7.4.4. Methods

Methods define the actions that a class can perform. Methods can take parameters that provide input data, and can return output data through parameters. Methods can also return a value directly, without using a parameter.

![](images/00051.jpeg)

![](images/00048.jpeg)Extension methods
Extension methods are static methods, but are intended to be used as instance methods.

![](images/00052.jpeg)

This does mean that it can now be a breaking change to turn an ordinary static method into an extension method, which was not the case before. But extension methods are generally only called as static methods in the rare cases where there is an ambiguity. In those cases, it seems right to require full qualification of the method anyway.

#### 7.4.5. Events

Events provide notifications about occurrences, such as button clicks or the successful completion of a method, to other objects. Events are defined and triggered by using delegates.

#### 7.4.6. Operators

Overloaded operators are considered class members. When you overload an operator, you define it as a public static method in a class. The predefined operators (+, *, <, and so on) are not considered members.

##### 7.4.6.1. Primary Operators

| Expression | Purpose |
| x.y | Member access |
| x?.y | Conditional member access |
| f(x) | Method and delegate invocation |
| a[x] | Array and indexer access |
| a?[x] | Conditional array and indexer access |
| x++ | Post-increment |
| x-- | Post-decrement |
| new T(...) | Object and delegate creation |
| new T(...){...} | Object creation with initializer. |
| new {...} | Anonymous object initializer. |
| new T[...] | Array creation. |
| typeof(T) | Obtain System.Type object for T |
| checked(x) | Evaluate expression in checked context |
| unchecked(x) | Evaluate expression in unchecked context |
| default (T) | Obtain default value of type T |

##### 7.4.6.2. Unary Operators

| Expression | Purpose |
| +x | Identity |
| -x | Negation |
| !x | Logical negation |
| ~x | Bitwise negation |
| ++x | Pre-increment |
| --x | Pre-decrement |
| (T)x | Explicitly convert x to type T |

##### 7.4.6.3. Multiplicative Operators

| Expression | Purpose |
| * | Multiplication |
| / | Division |
| % | Reaminder |

##### 7.4.6.4. Additive Operators

| Expression | Purpose |
| x + y | Addition, string concatenation, delegate combination |
| x – y | Subtraction, delegate removal |

##### 7.4.6.5. Shift Operators

| Expression | Purpose |
| x << y | Shift left |
| x >> y | Shift right |

##### 7.4.6.6. Relational and Type Operators

| Expression | Purpose |
| x < y | Less than |
| x > y | Greater than |
| x <= y | Less than or equal |
| x >= y | Greater than or equal |
| x is T | Return true if x is a T, false otherwise |
| x as T | Return x typed as T, or null if x is not a T |

##### 7.4.6.7. Equality Operators

| Expression | Purpose |
| x == y | Equal |
| x != y | Not Equal |

##### 7.4.6.8. Logical, Conditional, and Null Operators

| Expression | Purpose |
| x & y | Integer bitwise AND, Boolean logical AND |
| x ^ y | Integer bitwise XOR, boolean logical XOR |
| x &#124; y | Integer bitwise OR, boolean logical OR |
| x && y | Evaluates y only if x is true |
| x &#124;&#124; y | Evaluates y only if x is false |
| x ?? y | Evaluates to y if x is null, to x otherwise |
| x ?: y : z | Evaluates to y if x is true, z if x is false |

![](images/00034.jpeg)Null-conditional operators
Sometimes code tends to drown a bit in null-checking. The null-conditional operator lets you access members and elements only when the receiver is not-null, providing a null result otherwise.

![](images/00053.jpeg)

The null-conditional operator is conveniently used together with the null coalescing operator ??:

![](images/00054.jpeg)

The null-conditional operator exhibits short-circuiting behavior, where an immediately following chain of member accesses, element accesses and invocations will only be executed if the original receiver was not null:

![](images/00055.jpeg)

This example is essentially equivalent to:

![](images/00056.jpeg)

Except that customers is only evaluated once. None of the member accesses, element accesses and invocations immediately following the ? are executed unless customers has a non-null value.

Of course null-conditional operators can themselves be chained, in case there is a need to check for null more than once in a chain:

![](images/00057.jpeg)

Note that an invocation (a parenthesized argument list) cannot immediately follow the ? operator – that would lead to too many syntactic ambiguities. Thus, the straightforward way of calling a delegate only if it’s there does not work. However, you can do it via the Invoke method on the delegate:

![](images/00058.jpeg)

We expect that a very common use of this pattern will be for triggering events:

![](images/00059.jpeg)

This is an easy and thread-safe way to check for null before you trigger an event. The reason it’s thread-safe is that the feature evaluates the left-hand side only once, and keeps it in a temporary variable.

##### 7.4.6.9. Assignment and Anonymous Operators

| Expression | Purpose |
| = | Assignment |
| x op= y | Compound assignment. Supports these operators: +=, -=, *=, /=, %=, &=, &#124;=, !=, <<=, >>= |
| (T x) => y | Anonymous function (lambda expression) |

#### 7.4.7. Indexers

Indexers enable an object to be indexed in a manner similar to arrays.

![](images/00060.jpeg)

#### 7.4.8. Constructors

Constructors are methods that are called when the object is first created. They are often used to initialize the data of an object. Structs cannot contain default constructor explicitly, beacause it’s provided by the compiler.

![](images/00061.jpeg)

#### 7.4.9. Destructors

Destructors are used very rarely in C#. They are methods that are called by the runtime execution engine when the object is about to be removed from memory. They are generally used to make sure that any resources which must be released are handled appropriately. You can have only one destructor in a class, structs cannot define it, without any modifiers or parameters and it cannot be called, it’s automatically invoked. To see it in action, build and run this Program without debugging using Ctrl+F5.

![](images/00062.jpeg)

#### 7.4.10. Nested Types

Nested types are types declared within another type. Nested types are often used to describe objects that are used only by the types that contain them.

![](images/00063.jpeg)

You can create a new instance of the Nested class as follows:

![](images/00064.jpeg)

### 7.5. Encapsulation

Encapsulation is one the 4 major principles that make a language object-oriented. It’s about the hiding of data implementation by restricting access to accessors and mutators.

#### 7.5.1. Accessor

An accessor is a method that is used to ask an object about itself. In OOP, these are usually in the form of properties, which have, under normal conditions, a get method, which is an accessor method.

![](images/00065.jpeg)

#### 7.5.2. Mutator

Mutators are public methods that are used to modify the state of an object, while hiding the implementation of exactly how the data gets modified.

![](images/00066.jpeg)

### 7.6. Inheritance

Objects can relate to each other with either a “has a”, “uses a” or an “is a” relationship.  “Is a” is the inheritance way of object relationship.As mentioned before, in C# all classes inherit fromSystem.Object.

![](images/00067.jpeg)

![](images/00068.jpeg)

### 7.7. Polymorphism

Polymorphism means one name, many forms.  Polymorphism manifests itself by having multiple methods all with the same name, but slightly different functionality. There are 2 basic types of polymorphism.  Overridding, also called run-time polymorphism, and overloading, which is referred to as compile-time polymorphism.

![](images/00069.jpeg)

### 7.8. Abstract and Sealed Classes and Class Members

#### 7.8.1. Abstract classes and class members

Data abstraction is the simplest of principles to understand. Data abstraction and Encapsulation are closely tied together, because a simple definition of data abstraction is the development of classes, objects, types in terms of their interfaces and functionality, instead of their implementation details. Abstraction denotes a model, a view, or some other focused representation for an actual item. It’s the development of a software object to represent an object we can find in the real world. Encapsulation hides the details of that implementation.

![](images/00070.jpeg)

Abstract methods have no implementations. You can use the override keyword to implement this method in the derived class. If a class declare a virtual method as abstract, it will virtual to any class inheriting from the abstract class. And a class inheriting an abstract cannot access the original implementation.

![](images/00071.jpeg)

#### 7.8.2. Sealed classes and class members

You can use the keyword sealed to declare a sealed class. A sealed class cannot be used as a base class so they prevent inheritance. If they are used on a derived virtual member, it negates the virtual aspect of this member for further derived classes.

![](images/00072.jpeg)

#### 7.8.3. Difference between Override and New Keywords

To use the keywords override and new, the base class method must be virtual. These keywords can be used also with properties, indexers and events. The difference between override and new is all about polymorphism. If you use the override keyword, the compiler will totally redefine this member regardless of the base class, in the other side by using the new keyword the compiler will hide the definition in at this level of inheritance, but once called by the base class it will reveal the original definition. Without polymorphism, there is no difference.

![](images/00073.jpeg)

### 7.9. Static Classes and Static Class Members

Basically the main characteristic of a static class that we can instantiate, it can contains only static members and it is sealed.  If need to call a public method of this class just do that by using the class name directly as shown:

![](images/00074.jpeg)

A static member is a shared instance of this variable among all instances even in a non-static class.

![](images/00075.jpeg)

![](images/00076.jpeg)Using static
The feature allows all the accessible static members of a type to be imported, making them available without qualification in subsequent code.

![](images/00077.jpeg)

This is great for when you have a set of functions related to a certain domain that you use all the time. System.Math would be a common example of that. It also lets you directly specify the individual named values of an enum type, like the System.DayOfWeek members above.

### 7.10. Access Modifiers

| Access modifier | Purpose |
| public | The type or member can be accessed by any other code in the same assembly or another assembly that references it. |
| private | The type or member can be accessed only by code in the same class or struct. |
| protected | The type or member can be accessed only by code in the same class or struct, or in a class that is derived from that class. |
| internal | The type or member can be accessed by any code in the same assembly, but not from another assembly. |

## 8. Delegates

Delegates are references to methods with particular parameter list and return type. As it’s a particular type, you can instantiate a delegate, associate its instance with an adequate method (same signature and return type), or invoke any defined method through its instance.

Delegates have a few capabilities in C#: referencing methods, dispatching multiple methods, asynchronous execution, and event typing.

Let’s first examine the role of a delegate as a reference to a method. To do this, the delegate specifies the signature of a method that it can reference, like this:

![](images/00078.jpeg)

You might notice that a delegate looks like an abstract method, except it has the delegate type definition keyword. A delegate definition is a reference type, just like a class, struct, or interface. The previous delegate definition is for a delegate type named Add that takes two double arguments and returns a result of type double. Just like other types, delegate accessibility can only be public or internal and is internal by default.

![](images/00079.jpeg)

## 9. Events

The events are declared and raised in a class and associated with the event handlers using delegates within the same class or some other class. The class containing the event is used to publish the event. This is called the publisher class. Some other class that accepts this event is called the subscriber class. Events use the publisher-subscriber model.

A publisher is an object that contains the definition of the event and the delegate. The event-delegate association is also defined in this object. A publisher class object invokes the event and it is notified to other objects.

A subscriber is an object that accepts the event and provides an event handler. The delegate in the publisher class invokes the method (event handler) of the subscriber class.

To declare an event inside a class, first a delegate type for the event must be declared.

![](images/00080.jpeg)

Next, the event itself is declared, using the event keyword:

![](images/00081.jpeg)

The preceding code defines a delegate named MyLogHandler and an event named MyEventLog, which invokes the delegate when it is raised.

![](images/00082.jpeg)

## 10. Lambdas

A lambda is a nameless method. Sometimes you have a block of code that serves one specific purpose and you don’t need to define it as a method. Methods are nice because they let you modularize your code and have something to refer to with delegates and call from multiple places.

Just like methods, lambdas can have parameters, a body, and can return values.

![](images/00083.jpeg)

With a single statement, you don’t need to use curly braces on the body, but you do with multiple statements. Predicate is a generic delegate. The type parameter is set to <string>, meaning that the lambda parameter is type string.

![](images/00084.jpeg)

This shows that Func<T, TResult> accepts a parameter of type T and returns a value of type TResult.

![](images/00085.jpeg)

## 11. Enumeration Types

An enumeration is a complete, ordered listing of all the items in a collection. In C# it provides an efficient way declare a set of named integral constants that could be assigned to a variable.

![](images/00086.jpeg)

To verify the integral value of this type, you can cast it:

![](images/00087.jpeg)

You can assign values to the elements of the enumeration regardless of the order, or also computed values:

![](images/00088.jpeg)

You can use also enumerations to define a bit flag. In this way AND, OR and XOR operations can be performed on them. If an element has the value of zero means “no flags are set”. Don’t do that if it doesn’t mean it.

![](images/00089.jpeg)

## 12. Exceptions and Exception Handling

Exception handling is the process of responding to the occurrence, during computation, of exceptions – anomalous or exceptional conditions requiring special processing – often changing the normal flow of program execution using the try, catch, and finally keywords to try actions that may not succeed,

### 12.1. Using Exceptions

Exceptions are represented by classes derived from System.Exception. This class identifies the type of exception and contains properties that have details about the exception. Throwing an exception involves creating an instance of an exception-derived class, optionally configuring properties of the exception, and then throwing the object by using the throw keyword.

![](images/00090.jpeg)

After an exception is thrown, the runtime checks the current statement to see whether it is within a try block. If it is, any catch blocks associated with the try block are checked to see whether they can catch the exception.

![](images/00091.jpeg)

A try statement can contain more than one catch block. The first catch statement that can handle the exception is executed; any following catch statements, even if they are compatible, are ignored.

![](images/00092.jpeg)

Before the catch block is executed, the runtime checks for finally blocks. Finally blocks enable the programmer to clean up any ambiguous state that could be left over from an aborted try block.

![](images/00093.jpeg)

### 12.2. Exception Handling

A try block is used by C# programmers to partition code that might be affected by an exception. Associated catch blocks are used to handle any resulting exceptions. A finally block contains code that is run regardless of whether or not an exception is thrown in the try block, such as releasing resources that are allocated in the try block. A try block requires one or more associated catch blocks, or a finally block, or both.

The following examples show a try-catch statement: ![](images/00094.jpeg)

A try-finally statement:

![](images/00095.jpeg)

A try-catch-finally statement:

![](images/00096.jpeg)

### 12.3. Creating and Throwing Exceptions

Exceptions are used to indicate that an error has occurred while running the program. Exception objects that describe an error are created and then thrown with the throw keyword.

![](images/00097.jpeg)

### 12.4. Compiler-Generated Exceptions

Some exceptions are thrown automatically by the .NET Framework's common language runtime (CLR) when basic operations fail. These exceptions and their error conditions are listed in the following table:

| Exception | Description |
| ArithmeticException | A base class for exceptions that occur during arithmetic operations, such as DivideByZeroException and OverflowException. |
| ArrayTypeMismatchException | Thrown when an array cannot store a given element because the actual type of the element is incompatible with the actual type of the array. |
| DivideByZeroException | Thrown when an attempt is made to divide an integral value by zero. |
| IndexOutOfRangeException | Thrown when an attempt is made to index an array when the index is less than zero or outside the bounds of the array. |
| InvalidCastException | Thrown when an explicit conversion from a base type to an interface or to a derived type fails at runtime. |
| NullReferenceException | Thrown when you attempt to reference an object whose value is null. |
| OutOfMemoryException | Thrown when an attempt to allocate memory using the new operator fails. This indicates that the memory available to the common language runtime has been exhausted. |
| OverflowException | Thrown when an arithmetic operation in a checked context overflows. |
| StackOverflowException | Thrown when the execution stack is exhausted by having too many pending method calls; usually indicates a very deep or infinite recursion. |
| TypeInitializationException | Thrown when a static constructor throws an exception and no compatible catch clause exists to catch it. |

### 12.5. Handle an Exception using try/catch

The purpose of a try-catch block is to catch and handle an exception generated by working code. Some exceptions can be handled in a catch block and the problem solved without the exception being re-thrown.

![](images/00098.jpeg)

### 12.6. Execute Cleanup code using finally

The purpose of a finally statement is to ensure that the necessary cleanup of objects, usually objects that are holding external resources, occurs immediately, even if an exception is thrown.

![](images/00099.jpeg)

![](images/00076.jpeg)Await in catch and finally blocks
In C# 5 we don’t allow the await keyword in catch and finally blocks, because we’d somehow convinced ourselves that it wasn’t possible to implement.

This has actually been a significant limitation, and people have had to employ unsightly workarounds to compensate. That is no longer necessary:

![](images/00100.jpeg)

The implementation is quite complicated, but you don’t have to worry about that. That’s the whole point of having async in the language.

![](images/00101.gif)Exception filters
VB has them. F# has them. Now C# has them too. This is what they look like:

![](images/00102.jpeg)

If the parenthesized expression evaluates to true, the catch block is run, otherwise the exception keeps going.

Exception filters are preferable to catching and rethrowing because they leave the stack unharmed. If the exception later causes the stack to be dumped, you can see where it originally came from, rather than just the last place it was rethrown.

It is also a common and accepted form of “abuse” to use exception filters for side effects; e.g. logging. They can inspect an exception “flying by” without intercepting its course. In those cases, the filter will often be a call to a false-returning helper function which executes the side effects:

![](images/00103.jpeg)

## 13. File System and Registry

### 13.1. Iterating Through a Directory Tree

The phrase "iterate a directory tree" means to access each file in each nested subdirectory under a specified root folder, to any depth. You do not necessarily have to open each file. You can just retrieve the name of the file or subdirectory as a string, or you can retrieve additional information in the form of a System.IO.FileInfo or System.IO.DirectoryInfo object.

![](images/00104.jpeg)

![](images/00105.jpeg)

### 13.2. Getting Information about Files, Folders, and Drives

You can access file system information by using the following classes:

*   System.IO.FileInfo
*   System.IO.DirectoryInfo
*   System.IO.DriveInfo
*   System.IO.Directory
*   System.IO.File

![](images/00106.jpeg)

![](images/00107.jpeg)

### 13.3. Creating a File or Folder

You can programmatically create a folder on your computer, create a subfolder, create a file in the subfolder, and write data to the file.

![](images/00108.jpeg)

### 13.4. Copy, Delete, and Move Files and Folders

To copy, move, and delete files and folders in a synchronous manner by using the System.IO.File.

![](images/00109.jpeg)

![](images/00110.jpeg)

![](images/00111.jpeg)

### 13.5. Providing a Progress Dialog Box for File Operations

You can provide a standard dialog box that shows progress on file operations in Windows if you use the CopyFile(String, String, UIOption) method in the Microsoft.VisualBasic namespace.

![](images/00112.jpeg)

### 13.6. Writing to a Text File

![](images/00113.jpeg)

### 13.7. Reading from a Text File

You can read the contents of a text file by using the static methods ReadAllText and ReadAllLines from the System.IO.File class.

![](images/00114.jpeg)

### 13.8. Reading a Text File One Line at a Time

You can read the contents of a text file, one line at a time, into a string using the ReadLine method of the StreamReader class. Each text line is stored into the string line and displayed on the screen.

![](images/00115.jpeg)

### 13.9. Creating a Key in the Registry

You can add the value pair, "Name" and "Test", to the current user's registry, under the key "Names".

![](images/00116.jpeg)

## 14. Generics

### 14.1. Introduction to Generics

Generic classes and methods combine reusability, type safety and efficiency in a way that their non-generic counterparts cannot. Generics are most frequently used with collections and the methods that operate on them.

![](images/00117.jpeg)

The following code example shows how client code uses the generic GenericList<T> class to create a list of integers. Simply by changing the type argument, the following code could easily be modified to create lists of strings or any other custom type:

![](images/00118.jpeg)

### 14.2. Generic Type Parameters

In a generic type or method definition, a type parameters is a placeholder for a specific type that a client specifies when they instantiate a variable of the generic type. A generic class, such as GenericList<T> cannot be used as-is because it is not really a type; it is more like a blueprint for a type.

![](images/00003.jpeg)Name generic type parameters with descriptive names, unless a single letter name is completely self-explanatory and a descriptive name would not add value.

![](images/00119.jpeg)

![](images/00003.jpeg)Prefix descriptive type parameter names with "T".
Consider indicating constraints placed on a type parameter in the name of parameter.

![](images/00120.jpeg)

### 14.3. Constraints on Type Parameters

When you define a generic class, you can apply restrictions to the kinds of types that client code can use for type arguments when it instantiates your class. If client code tries to instantiate your class by using a type that is not allowed by a constraint, the result is a compile-time error. These restrictions are called constraints.

| Exception | Description |
| where T: struct | The type argument must be a value type. Any value type except Nullable can be specified. |
| where T : class | The type argument must be a reference type; this applies also to any class, interface, delegate, or array type. |
| where T : new() | The type argument must have a public parameter less constructor. When used together with other constraints, the new () constraint must be specified last. |
| where T : <base class name> | The type argument must be or derive from the specified base class. |
| where T : <interface name> | The type argument must be or implement the specified interface. Multiple interface constraints can be specified. The constraining interface can also be generic. |
| where T : U | The type argument supplied for T must be or derive from the argument supplied for U. |

![](images/00121.jpeg)

### 14.4. Generic Classes

Generic classes encapsulate operations that are not specific to a particular data type. The most common use for generic classes is with collections like linked lists, hash tables, stacks, queues, trees, and so on.

![](images/00122.jpeg)

### 14.5. Generic Interfaces

It is often useful to define interfaces either for generic collection classes, or for the generic classes that represent items in the collection. The preference for generic classes is to use generic interfaces, such as IComparable<T> rather than IComparable, in order to avoid boxing and unboxing operations on value types. The rules of inheritance that apply to classes also apply to interfaces.

![](images/00123.jpeg)

### 14.6. Generic Methods

A generic method is a method that is declared with type parameters, as follows:

![](images/00124.jpeg)

### 14.7. Generics and Arrays

Single-dimensional arrays that have a lower bound of zero automatically implement IList<T>. This enables you to create generic methods that can use the same code to iterate through arrays and other collection types. This technique is primarily useful for reading data in collections.

![](images/00125.jpeg)

### 14.8. Generic Delegates

A delegate can define its own type parameters. Code that references the generic delegate can specify the type argument to create a closed constructed type, just like when instantiating a generic class or calling a generic method.

![](images/00126.jpeg)

### 14.9. Default Keyword

In generic classes and methods, one issue that arises is how to assign a default value to a parameterized type T when you do not know the following in advance:

*   Whether T will be a reference type or a value type.
*   If T is a value type, whether it will be a numeric value or a struct.

![](images/00127.jpeg)

## 15. Indexers

Indexers allow instances of a class or struct to be indexed just like arrays. Indexers resemble properties except that their accessors take parameters.

### 15.1. Using Indexers

Indexers are a syntactic convenience that enable you to create a class, struct, or interface that client applications can access just as an array. Indexers are most frequently implemented in types whose primary purpose is to encapsulate an internal collection or array.

![](images/00128.jpeg)

### 15.2. Indexers in Interfaces

ndexers can be declared on an interface (C# Reference). Accessors of interface indexers differ from the accessors of class indexers in the following ways:

*   Interface accessors do not use modifiers.
*   An interface accessor does not have a body.

![](images/00129.jpeg)

## 16. Interfaces

An interface contains different declarations of members that classes or strucs can implement. You may use interfaces to include behaviors for classes from multiple sources, because they don’t support multiple inheritance. Or if you want to simulate inheritance for structs because they don’t support it at all.

![](images/00130.jpeg)

## 17. LINQ Query Expressions

Language-Integrated Query (LINQ) is the name for a set of technologies based on the integration of query capabilities directly into the C# language.

For a developer who writes queries, the most visible "language-integrated" part of LINQ is the query expression.

### 17.1. Querying Collections

A query is a set of instructions that describes what data to retrieve from a given data source (or sources) and what shape and organization the returned data should have. A query is distinct from the results that it produces.

![](images/00131.jpeg)

Retrieve a sequence of elements as in the previous example but transform them to a new type of object. For example, a query may retrieve only the last names from certain customer records in a data source.

![](images/00132.jpeg)

### 17.2. Filtering Data

In some cases you do not know until run time how many predicates you have to apply to source elements in the where clause. One way to dynamically specify multiple predicate filters is to use the Contains<TSource> method

![](images/00133.jpeg)

![](images/00134.jpeg)

### 17.3. Ordering Collections

You can use an orderby clause with one or more of the source sequences.

![](images/00135.jpeg)

### 17.4. Joining Objects

In relational database terms, an inner join produces a result set in which each element of the first collection appears one time for every matching element in the second collection. If an element in the first collection has no matching elements, it does not appear in the result set.

![](images/00136.jpeg)

![](images/00137.jpeg)

To perform join operations that are not possible with the join clause. In a query expression, the join clause is limited to, and optimized for, equijoins, which are by far the most common type of join operation. When performing an equijoin, you will probably always get the best performance by using the join clause

![](images/00138.jpeg)

![](images/00139.jpeg)

## 18. Main () and Command-Line Arguments

When an application is started, the first method to be invoked is the Main method. So briefly it’s the entry point of an .exe program. It must be static and not public.

It could be declared inside a class or a struct, and with or without string[] arguments.

![](images/00140.jpeg)

## 19. Namespaces

There are various ways to organize code and the choice should be based on the standards of your team and the nature of the project you’re building. One of the common ways to organize code is with the C# namespace feature.

![](images/00141.jpeg)

You can also create/use a namespace alias to shorthand syntax when you need to fully qualify a namespace. In this example you can call the alias Crypto instead of System.Security.Cryptography.

![](images/00142.jpeg)

## 20. Nullable Types

Nullable types are instances of the System.Nullable<T> struct. A nullable type can represent the correct range of values for its underlying value type, plus an additional null value.

 A Nullable<bool> can be assigned the values true  false, or null. The ability to assign null to numeric and Boolean types is especially useful when you are dealing with databases and other data types that contain elements that may not be assigned a value.

Nullable types have the following characteristics:

*   Nullable types represent value-type variables that can be assigned the value of null. You cannot create a nullable type based on a reference type because they already support null value.
*   The syntax T? is shorthand for Nullable<T>, where T is a value type.
*   Assign a value to a nullable type just as you would for an ordinary value type, for example int? x = 10; or double? d = 4.108\. A nullable type can also be assigned the value null: int? x = null.
*   Use the Nullable<T>.GetValueOrDefault method to return either the assigned value, or the default value for the underlying type if the value is null, for example int j = x.GetValueOrDefault();
*   Use the HasValue and Value read-only properties to test for null and retrieve the value, as shown in the following example: if(x.HasValue) j = x.Value;
*   The HasValue property returns true if the variable contains a value, or false if it is null.
*   The Value property returns a value if one is assigned. Otherwise, a System.InvalidOperationException is thrown.
*   The default value for HasValue is false. The Value property has no default value.
*   You can also use the == and != operators with a nullable type, as shown in the following example: if (x != null) y = x;
*   Use the ?? operator to assign a default value that will be applied when a nullable type whose current value is null is assigned to a non-nullable type, for example int? x = null; int y = x ?? -1;
*   Nested nullable types are not allowed. The following line will not compile: Nullable<Nullable<int>> n;

### 20.1. Using Nullable Types

Nullable types can represent all the values of an underlying type, and an additional null value. Nullable types are declared in one of two ways:

System.Nullable<T> variable

-or-

T? variable

![](images/00143.jpeg)

### 20.2. Boxing Nullable Types

Objects based on nullable types are only boxed if the object is non-null. If HasValue is false, the object reference is assigned to null instead of boxing. If the object is non-null -- if HasValue is true -- then boxing occurs, but only the underlying type that the nullable object is based on is boxed.

![](images/00144.jpeg)

### 20.3. Identifying a Nullable Type

You can use the C# typeof operator to create a Type object that represents a Nullable type:

![](images/00145.jpeg)

Calling GetType on a Nullable type causes a boxing operation to be performed when the type is implicitly converted to Object. Therefore GetType always returns a Type object that represents the underlying type, not the Nullable type.

![](images/00146.jpeg)

Use the following code to determine whether a Type object represents a Nullable type:

![](images/00147.jpeg)

### 20.4. Safely Cast from bool? to bool

The bool? nullable type can contain three different values: true, false, and null. Therefore, the bool? type cannot be used in conditionals such as with if, for, or while.

![](images/00148.jpeg)

This is not allowed because it is unclear what null means in the context of a conditional. To use a bool? in a conditional statement, you need to perform these actions:

![](images/00149.jpeg)

## 21. Statements, Expression and Operators

The C# code that comprises an application consists of statements made up of keywords, expressions and operators.

### 21.1. Statements

The actions that a program takes are expressed in statements. Common actions include declaring variables, assigning values, calling methods, looping through collections, and branching to one or another block of code, depending on a given condition.

The order in which statements are executed in a program is called the flow of control or flow of execution.

![](images/00150.jpeg)

There are various types of statements in C# and their associated keyword, mentioned in the following table:

| Exception | Description |
| Declaration statements | A declaration statement introduces a new variable or constant. A variable declaration can optionally assign a value to the variable.![](images/00151.jpeg) |
| Expression statements | Expression statements that calculate a value must store the value in a variable.![](images/00152.jpeg) |
| Selection statements | Selection statements enable you to branch to different sections of code, depending on one or more specified conditions. if-else, switch-case |
| Iteration statements | Iteration statements enable you to loop through collections like arrays, or perform the same set of statements repeatedly until a specified condition is met. do, for, foreach-in, while |
| Jump statements | Jump statements transfer control to another section of code. break, continue, default, goto, return, yield |
| Exception handling statements | Exception handling statements enable you to gracefully recover from exceptional conditions that occur at run time. throw, try-catch, try-finally, try-catch-finally |
| Checked and unchecked | Checked and unchecked statements enable you to specify whether numerical operations are allowed to cause an overflow when the result is stored in a variable that is too small to hold the resulting value.![](images/00153.jpeg) |
| The await statement | If you mark a method with the async modifier, you can use the await operator in the method. When control reaches an await expression in the async method, control returns to the caller, and progress in the method is suspended until the awaited task completes. |
| The yield return statement | An iterator performs a custom iteration over a collection, such as a list or an array. An iterator uses the yield  return statement to return each element one at a time. When a yield  return statement is reached, the current location in code is remembered.![](images/00154.jpeg) |
| The fixed statement | The fixed statement prevents the garbage collector from relocating a movable variable.![](images/00155.jpeg) |
| The lock statement | The lock statement enables you to limit access to blocks of code to only one thread at a time.![](images/00156.jpeg) |
| Labeled statements | You can give a statement a label and then use the goto keyword to jump to the labeled statement.![](images/00157.jpeg) |
| The empty statement | The empty statement consists of a single semicolon. It does nothing and can be used in places where a statement is required but no action needs to be performed.![](images/00158.jpeg) |

### 21.2. Expressions

An expression is a sequence of one or more operands and zero or more operators that can be evaluated to a single value, object, method, or namespace. Expressions can consist of a literal value, a method invocation, an operator and its operands, or a simple name.

![](images/00159.jpeg)

![](images/00160.jpeg)Expression bodies on method-like members
Methods as well as user-defined operators and conversions can be given an expression body by use of the “lambda arrow”:

![](images/00161.jpeg)

The effect is exactly the same as if the methods had had a block body with a single return statement.

![](images/00034.jpeg)nameof expressions
Occasionally you need to provide a string that names some program element: when throwing an ArgumentNullException you want to name the guilty argument; when raising a PropertyChanged event you want to name the property that changed, etc.

Using string literals for this purpose is simple, but error prone. You may spell it wrong, or a refactoring may leave it stale. nameof expressions are essentially a fancy kind of string literal where the compiler checks that you have something of the given name, and Visual Studio knows what it refers to, so navigation and refactoring will work:![](images/00162.jpeg)

You can put more elaborate dotted names in a nameof expression, but that’s just to tell the compiler where to look: only the final identifier will be used:![](images/00163.jpeg)

### 21.3. Anonymous Functions

An anonymous function is an "inline" statement or expression that can be used wherever a delegate type is expected.

### 21.3.1. Lambda Expression

A lambda expression is an anonymous function that you can use to create delegates or expression tree types. By using lambda expressions, you can write local functions that can be passed as arguments or returned as the value of function calls. Lambda expressions are particularly helpful for writing LINQ query expressions.

![](images/00164.jpeg)

### 21.3.2. Anonymous Methods

Creating anonymous methods is essentially a way to pass a code block as a delegate parameter.

![](images/00165.jpeg)

### 21.4. Overloadable Operators

C# allows user-defined types to overload operators by defining static member functions using the operator keyword. Not all operators can be overloaded, however, and others have restrictions.

| Operators | Overloadability |
| +, -, !, ~, ++, --, true, false | These unary operators can be overloaded. |
| +, -, *, /, %, &, &#124;, ^, <<, >> | These binary operators can be overloaded. |
| ==, !=, <, >, <=, >= | The comparison operators can be overloaded (but see the note that follows this table). |
| &&, &#124;&#124; | The conditional logical operators cannot be overloaded, but they are evaluated using & and &#124;, which can be overloaded. |
| [] | The array indexing operator cannot be overloaded, but you can define indexers. |
| (T)x | The cast operator cannot be overloaded, but you can define new conversion operators. |
| +=, -=, *=, /=, %=, &=, &#124;=, ^=, <<=, >>= | Assignment operators cannot be overloaded, but +=, for example, is evaluated using +, which can be overloaded. |
| =, ., ?:, ??, ->, =>, f(x), as, checked, unchecked, default, delegate, is, new, sizeof, typeof | These operators cannot be overloaded. |

![](images/00166.jpeg)

### 21.5. Conversion Operators

C# enables programmers to declare conversions on classes or structs so that classes or structs can be converted to and/or from other classes or structs, or basic types. Conversions are defined like operators and are named for the type to which they convert. Either the type of the argument to be converted, or the type of the result of the conversion, but not both, must be the containing type.

![](images/00167.jpeg)

### 21.6. Using Operator Overloading to Create a Complex Number Class

You can use operator overloading to create a complex number class Complex that defines complex addition. The program displays the imaginary and the real parts of the numbers and the addition result using an override of the ToString() method.

![](images/00168.jpeg)![](images/00169.jpeg)

### 21.7. Equality Comparisons

It is sometimes necessary to compare two values for equality. In some cases, you are testing for value equality, also known as equivalence, which means that the values that are contained by the two variables are equal.

![](images/00170.jpeg)

## 22. Strings

A string is an object of type String whose value is text. Internally, the text is stored as a sequential read-only collection of Char objects.

You can declare and initialize strings in various ways:

![](images/00171.jpeg)

### 22.1. Concatenate Multiple Strings

Concatenation is the process of appending one string to the end of another string. When you concatenate string literals or string constants by using the + operator, the compiler creates a single string.

![](images/00172.jpeg)

![](images/00173.jpeg)

### 22.2. Modify String Contents

Because strings are immutable, it is not possible (without using unsafe code) to modify the value of a string object after it has been created.

![](images/00174.jpeg)

![](images/00034.jpeg)String interpolation
String.Format and its cousins are very versatile and useful, but their use is a little clunky and error prone. Particularly unfortunate is the use of {0} etc. placeholders in the format string, which must line up with arguments supplied separately:

![](images/00175.jpeg)

String interpolation lets you put the expressions right in their place, by having “holes” directly in the string literal:

![](images/00176.jpeg)

Just as with String.Format, optional alignment and format specifiers can be given:

![](images/00177.jpeg)

The contents of the holes can be pretty much any expression, including even other strings:

![](images/00178.jpeg)

Notice that the conditional expression is parenthesized, so that the : "s" doesn’t get confused with a format specifier

### 22.3. Compare Strings

When you compare strings, you are producing a result that says one string is greater than or less than the other, or that the two strings are equal.

![](images/00179.jpeg)

### 22.4. Parse Strings Using String.Split

A string can be parsed using the String.Split method. As input, Split takes an array of characters that indicate which characters separate interesting sub strings of the target string.

![](images/00180.jpeg)

### 22.5. Search Strings Using String Methods

The string type, which is an alias for the System.String class, provides a number of useful methods for searching the contents of a string.

![](images/00181.jpeg)

### 22.6. Search Strings Using Regular Expressions

The System.Text.RegularExpressions.Regex class can be used to search strings. These searches can range in complexity from very simple to making full use of regular expressions.

![](images/00182.jpeg)

You can use regular expressions to validate the format of each string in an array. The validation requires that each string take the form of a telephone number in which three groups of digits are separated by dashes, the first two groups contain three digits, and the third group contains four digits. This is done by using the regular expression ^\\d{3}-\\d{3}-\\d{4}$.

![](images/00183.jpeg)

### 22.7. Determine Whether a String Represents a Numeric Value

To determine whether a string is a valid representation of a specified numeric type, use the static TryParse method that is implemented by all primitive numeric types and also by types such as DateTime and IPAddress.

![](images/00184.jpeg)

You can use TryParse with string representations of long, byte, and decimal values.

![](images/00185.jpeg)

### 22.8. Convert a String to a DateTime

It is common for programs to enable users to enter dates as string values. To convert a string-based date to a System.DateTime object, you can use the Convert.ToDateTime(String) method or the DateTime.Parse(String) static method.

![](images/00186.jpeg)

### 22.9. Convert Between Legacy Encodings and Unicode

All strings in memory are encoded as Unicode (UTF-16). When you bring data from storage into a string object, the data is automatically converted to UTF-16.

![](images/00187.jpeg)

### 22.10. Convert RTF to Plain Text

Rich Text Format (RTF) is a document format developed by Microsoft in the late 1980s to enable the exchange of documents across operating systems.

![](images/00188.jpeg)

## 23. Unsafe Code and Pointers

To maintain type safety and security, C# does not support pointer arithmetic, by default. However, by using the unsafe keyword, you can define an unsafe context in which pointers can be used.

*   Unsafe code has the following properties:
*   Methods, types, and code blocks can be defined as unsafe.
*   In some cases, unsafe code may increase an application's performance by removing array bounds checks.
*   Unsafe code is required when you call native functions that require pointers.
*   Using unsafe code introduces security and stability risks.
*   In order for C# to compile unsafe code, the application must be compiled with /unsafe.

### 23.1. Fixed Size Buffers

You can use the fixed statement to create a buffer with a fixed size array in a data structure. This is useful when you are working with existing code, such as code written in other languages.

The only restriction is that the array type must be bool, byte, char, short, int, long, sbyte, ushort, uint, ulong, float, or double.

![](images/00189.jpeg)

A struct can contain an embedded array. To access the elements of the array, you use a fixed statement to establish a pointer to the first element.

![](images/00190.jpeg)

### 23.2. Pointer types

In an unsafe context, a type may be a pointer type, a value type, or a reference type. A pointer type declaration takes one of the following forms:

![](images/00191.jpeg)

Any of the following types may be a pointer type:

*   sbyte, byte, short, ushort, int, uint, long, ulong, char, float, double, decimal, or bool.
*   Any enum type.
*   Any pointer type.
*   Any user-defined struct type that contains fields of unmanaged types only.

| Example | Description |
| int* p | p is a pointer to an integer. |
| int** p | p is a pointer to a pointer to an integer. |
| int*[] p | p is a single-dimensional array of pointers to integers. |
| char* p | p is a pointer to a char. |
| void* p | p is a pointer to an unknown type. |

## 24. XML Documentation Comments

You can create documentation for your code by including XML elements in special comment fields (indicated by triple slashes) in the source code directly before the code block to which the comments refer.

![](images/00192.jpeg)

When you compile with the /doc option, the compiler will search for all XML tags in the source code and create an XML documentation file. To create the final documentation based on the compiler-generated file.

### 24.1. Recommended Tags for Documentation Comments

The C# compiler processes documentation comments in your code and formats them as XML in a file whose name you specify in the /doc command-line option.

| Tag | Description |
| <c> | The <c> tag gives you a way to indicate that text within a description should be marked as code.![](images/00193.jpeg) |
| <code> | The <code> tag gives you a way to indicate multiple lines as code. |
| <cref> | The cref attribute in an XML documentation tag means "code reference." It specifies that the inner text of the tag is a code element, such as a type, method, or property. ![](images/00194.jpeg) |
| <example> | The <example> tag lets you specify an example of how to use a method or other library member.![](images/00195.jpeg) |
| <exception>* | The <exception> tag lets you specify which exceptions can be thrown.![](images/00196.jpeg) |
| <include>* | The <include> tag lets you refer to comments in another file that describe the types and members in your source code.![](images/00197.jpeg) |
| <list> | The <list> block is used to define the heading row of either a table or definition list.![](images/00198.jpeg) |
| <para> | The <para> tag is for use inside a tag, such as <summary>, <remarks>, or <returns>, and lets you add structure to the text. |
| <param>* | The <param> tag should be used in the comment for a method declaration to describe one of the parameters for the method.![](images/00199.jpeg) |
| <paramref> | The <paramref> tag gives you a way to indicate that a word in the code comments, for example in a <summary> or <remarks> block refers to a parameter.![](images/00200.jpeg) |
| <permission>* | The <permission> tag lets you document the access of a member. The PermissionSet class lets you specify access to a member.![](images/00201.jpeg) |
| <remarks> | The <remarks> tag is used to add information about a type, supplementing the information specified with <summary>.![](images/00202.jpeg) |
| <returns> | The <returns> tag should be used in the comment for a method declaration to describe the return value.![](images/00203.jpeg) |
| <see>* | The <see> tag lets you specify a link from within text. Use <seealso> to indicate that text should be placed in a See Also section. ![](images/00204.jpeg) |
| <seealso>* | The <seealso> tag lets you specify the text that you might want to appear in a See Also section. Use <see> to specify a link from within text. ![](images/00205.jpeg) |
| <summary> | The <summary> tag should be used to describe a type or a type member. Use <remarks> to add supplemental information to a type description![](images/00206.jpeg) |
| <typeparam>* | The <typeparam> tag should be used in the comment for a generic type or method declaration to describe a type parameter.![](images/00207.jpeg) |
| <typeparamref> | Use this tag to enable consumers of the documentation file to format the word in some distinct way, for example in italics. |
| <value> | The <value> tag lets you describe the value that a property represents.![](images/00208.jpeg) |

(* denotes that the compiler verifies syntax.)

### 24.2. Processing the XML File

The compiler generates an ID string for each construct in your code that is tagged to generate documentation.

| Character | Description |
| N | namespace You cannot add documentation comments to a namespace, but you can make cref references to them, where supported. |
| T | type: class, interface, struct, enum, delegate |
| F | Field |
| P | property (including indexers or other indexed properties) |
| M | method (including such special methods as constructors, operators, and so forth) |
| E | event |
| ! | error stringThe rest of the string provides information about the error. The C# compiler generates error information for links that cannot be resolved. |

### 24.3. Delimiters for Documentation Tags

The use of XML doc comments requires delimiters, which indicate to the compiler where a documentation comment begins and ends.

///
Single-line delimiter.

/** */
Multiline delimiters.

![](images/00209.jpeg)

# III. Coding standards and naming conventions

Because it is consistent with Microsoft’s .NET Framework or Microsoft practices and easy to read. There are some instructions to follow:

## 1. Do

Use PascalCasing for class names and methods names.

![](images/00210.jpeg)

Use camelCasing for method arguments and local variables.

![](images/00211.jpeg)

Use PascalCasing for abbreviations 3 characters or more (2 chars are both uppercase)

![](images/00212.jpeg)

Use predefined type names instead of system type names like Int16, Single, UInt64, etc

![](images/00213.jpeg)

Use implicit type var for local variable declarations. Exception: primitive types (int, string, double, etc) use predefined names.

![](images/00214.jpeg)

Use noun or noun phrases to name a class.

![](images/00215.jpeg)

Prefix interfaces with the letter I.  Interface names are noun (phrases) or adjectives.

![](images/00216.jpeg)

Name source files according to their main classes. Exception: file names with partial classes reflect their source or purpose, e.g. designer, generated, etc. Files are alphabetically sorted and partial classes remain adjacent.

![](images/00217.jpeg)

Organize namespaces with a clearly defined structure. It maintains good organization of your code base.

![](images/00218.jpeg)

Vertically align curly brackets.

![](images/00219.jpeg)

Declare all member variables at the top of a class, with static variables at the very top.

![](images/00220.jpeg)

Use singular names for enums. Exception: bit field enums. Plural flags because enum can hold multiple values (using bitwise 'OR').

![](images/00221.jpeg)

## 2. Don’t

Don’t use Hungarian notation or any other type identification in identifiers because it's consistent with the Microsoft's .NET Framework and Visual Studio IDE makes determining types very easy (via tooltips). In general you want to avoid type indicators in any identifier.

![](images/00222.jpeg)

![](images/00223.jpeg)

Don’t use SnailCasing (Underscores in identifiers). Exception: you can prefix private static variables with an underscore. Also avoids underline stress (inability to see underline).

![](images/00224.jpeg)

Explicitly specify a type of an enum or values of enums (except bit fields). It can create confusion when relying on actual types and values.

![](images/00225.jpeg)

Suffix enum names with Enum

![](images/00226.jpeg)

## 3. Avoid

Avoid using Abbreviations. Exceptions: abbreviations commonly used as names, such as Id, Xml, Ftp, Uri

![](images/00227.jpeg)