![](images/cover.jpg)

![image](images/cover.jpg)

![image](images/ifc.jpg)

![image](images/title.jpg)

In easy steps is an imprint of In Easy Steps Limited

16 Hamilton Terrace . Holly Walk . Leamington Spa

Warwickshire . United Kingdom . CV32 4LY

[www.ineasysteps.com](http://www.ineasysteps.com)

Copyright © 2023 by In Easy Steps Limited. All rights reserved. No part of this book may be reproduced or transmitted in any form or by any means, electronic or mechanical, including photocopying, recording, or by any information storage or retrieval system, without prior written permission from the publisher.

Notice of Liability

Every effort has been made to ensure that this book contains accurate and current information. However, In Easy Steps Limited and the author shall not be liable for any loss or damage suffered by readers as a result of any information contained herein.

Trademarks

All trademarks are acknowledged as belonging to their respective companies.

Contents

[1 **Getting started with C**](#chapter01.xhtml)

[Introducing the C language](#chapter01.xhtml_sec1)

[Installing a C compiler](#chapter01.xhtml_sec2)

[Writing a C program](#chapter01.xhtml_sec3)

[Compiling a C program](#chapter01.xhtml_sec4)

[Understanding compilation](#chapter01.xhtml_sec5)

[Summary](#chapter01.xhtml_sec6)

[2 **Storing variable values**](#chapter02.xhtml)

[Creating program variables](#chapter02.xhtml_sec7)

[Displaying variable values](#chapter02.xhtml_sec8)

[Inputting variable values](#chapter02.xhtml_sec9)

[Qualifying data types](#chapter02.xhtml_sec10)

[Using global variables](#chapter02.xhtml_sec11)

[Registering variables](#chapter02.xhtml_sec12)

[Converting data types](#chapter02.xhtml_sec13)

[Creating array variables](#chapter02.xhtml_sec14)

[Describing dimensions](#chapter02.xhtml_sec15)

[Summary](#chapter02.xhtml_sec16)

[3 **Setting constant values**](#chapter03.xhtml)

[Declaring program constants](#chapter03.xhtml_sec17)

[Enumerating constant values](#chapter03.xhtml_sec18)

[Creating a constant type](#chapter03.xhtml_sec19)

[Defining constants](#chapter03.xhtml_sec20)

[Debugging definitions](#chapter03.xhtml_sec21)

[Summary](#chapter03.xhtml_sec22)

[4 **Performing Operations**](#chapter04.xhtml)

[Doing arithmetic](#chapter04.xhtml_sec23)

[Assigning values](#chapter04.xhtml_sec24)

[Comparing values](#chapter04.xhtml_sec25)

[Assessing logic](#chapter04.xhtml_sec26)

[Examining conditions](#chapter04.xhtml_sec27)

[Measuring size](#chapter04.xhtml_sec28)

[Comparing bit values](#chapter04.xhtml_sec29)

[Flagging bits](#chapter04.xhtml_sec30)

[Understanding precedence](#chapter04.xhtml_sec31)

[Summary](#chapter04.xhtml_sec32)

[5 **Making statements**](#chapter05.xhtml)

[Testing expressions](#chapter05.xhtml_sec33)

[Branching switches](#chapter05.xhtml_sec34)

[Looping for a number](#chapter05.xhtml_sec35)

[Looping while true](#chapter05.xhtml_sec36)

[Breaking out of loops](#chapter05.xhtml_sec37)

[Going to labels](#chapter05.xhtml_sec38)

[Summary](#chapter05.xhtml_sec39)

[6 **Employing functions**](#chapter06.xhtml)

[Declaring functions](#chapter06.xhtml_sec40)

[Supplying arguments](#chapter06.xhtml_sec41)

[Calling recursively](#chapter06.xhtml_sec42)

[Placing functions in headers](#chapter06.xhtml_sec43)

[Restricting accessibility](#chapter06.xhtml_sec44)

[Summary](#chapter06.xhtml_sec45)

[7 **Pointing to data**](#chapter07.xhtml)

[Accessing data via pointers](#chapter07.xhtml_sec46)

[Doing pointer arithmetic](#chapter07.xhtml_sec47)

[Passing pointers to functions](#chapter07.xhtml_sec48)

[Creating arrays of pointers](#chapter07.xhtml_sec49)

[Pointing to functions](#chapter07.xhtml_sec50)

[Summary](#chapter07.xhtml_sec51)

[8 **Manipulating strings**](#chapter08.xhtml)

[Reading strings](#chapter08.xhtml_sec52)

[Copying strings](#chapter08.xhtml_sec53)

[Joining strings](#chapter08.xhtml_sec54)

[Finding substrings](#chapter08.xhtml_sec55)

[Validating strings](#chapter08.xhtml_sec56)

[Converting strings](#chapter08.xhtml_sec57)

[Summary](#chapter08.xhtml_sec58)

[9 **Building structures**](#chapter09.xhtml)

[Grouping in a structure](#chapter09.xhtml_sec59)

[Defining type structures](#chapter09.xhtml_sec60)

[Using pointers in structures](#chapter09.xhtml_sec61)

[Pointing to structures](#chapter09.xhtml_sec62)

[Passing structures to functions](#chapter09.xhtml_sec63)

[Grouping in a union](#chapter09.xhtml_sec64)

[Allocating memory](#chapter09.xhtml_sec65)

[Summary](#chapter09.xhtml_sec66)

[10 **Producing results**](#chapter10.xhtml)

[Creating a file](#chapter10.xhtml_sec67)

[Reading & writing characters](#chapter10.xhtml_sec68)

[Reading & writing lines](#chapter10.xhtml_sec69)

[Reading & writing entire files](#chapter10.xhtml_sec70)

[Scanning filestreams](#chapter10.xhtml_sec71)

[Reporting errors](#chapter10.xhtml_sec72)

[Getting the date and time](#chapter10.xhtml_sec73)

[Running a timer](#chapter10.xhtml_sec74)

[Generating random numbers](#chapter10.xhtml_sec75)

[Displaying a dialog box](#chapter10.xhtml_sec76)

[Summary](#chapter10.xhtml_sec77)

[**11 C reference section**](#chapter11.xhtml)

[ASCII character codes](#chapter11.xhtml_sec78)

[Input & output functions](#chapter11.xhtml_sec79)

[Character test functions](#chapter11.xhtml_sec80)

[String functions](#chapter11.xhtml_sec81)

[Math functions](#chapter11.xhtml_sec82)

[Utility functions](#chapter11.xhtml_sec83)

[Diagnostic functions](#chapter11.xhtml_sec84)

[Argument functions](#chapter11.xhtml_sec85)

[Date & time functions](#chapter11.xhtml_sec86)

[Jump functions](#chapter11.xhtml_sec87)

[Signal functions](#chapter11.xhtml_sec88)

[Limit constants](#chapter11.xhtml_sec89)

[Float constants](#chapter11.xhtml_sec90)

[12 **Getting started with C++**](#chapter12.xhtml)

[Introducing C++](#chapter12.xhtml_sec91)

[Installing a compiler](#chapter12.xhtml_sec92)

[Writing your first program](#chapter12.xhtml_sec93)

[Compiling & running programs](#chapter12.xhtml_sec94)

[Creating variables](#chapter12.xhtml_sec95)

[Employing variable arrays](#chapter12.xhtml_sec96)

[Employing vector arrays](#chapter12.xhtml_sec97)

[Declaring constants](#chapter12.xhtml_sec98)

[Summary](#chapter12.xhtml_sec99)

[13 **Performing operations**](#chapter13.xhtml)

[Doing arithmetic](#chapter13.xhtml_sec100)

[Assigning values](#chapter13.xhtml_sec101)

[Comparing values](#chapter13.xhtml_sec102)

[Assessing logic](#chapter13.xhtml_sec103)

[Examining conditions](#chapter13.xhtml_sec104)

[Establishing size](#chapter13.xhtml_sec105)

[Setting precedence](#chapter13.xhtml_sec106)

[Casting data types](#chapter13.xhtml_sec107)

[Summary](#chapter13.xhtml_sec108)

[14 **Making statements**](#chapter14.xhtml)

[Branching with if](#chapter14.xhtml_sec109)

[Switching branches](#chapter14.xhtml_sec110)

[Looping for](#chapter14.xhtml_sec111)

[Looping while](#chapter14.xhtml_sec112)

[Declaring functions](#chapter14.xhtml_sec113)

[Passing arguments](#chapter14.xhtml_sec114)

[Overloading functions](#chapter14.xhtml_sec115)

[Optimizing functions](#chapter14.xhtml_sec116)

[Summary](#chapter14.xhtml_sec117)

[15 **Handling strings**](#chapter15.xhtml)

[Creating string variables](#chapter15.xhtml_sec118)

[Getting string input](#chapter15.xhtml_sec119)

[Solving the string problem](#chapter15.xhtml_sec120)

[Discovering string features](#chapter15.xhtml_sec121)

[Joining & comparing strings](#chapter15.xhtml_sec122)

[Copying & swapping strings](#chapter15.xhtml_sec123)

[Finding substrings](#chapter15.xhtml_sec124)

[Replacing substrings](#chapter15.xhtml_sec125)

[Summary](#chapter15.xhtml_sec126)

[16 **Reading and writing files**](#chapter16.xhtml)

[Writing a file](#chapter16.xhtml_sec127)

[Appending to a file](#chapter16.xhtml_sec128)

[Reading characters & lines](#chapter16.xhtml_sec129)

[Formatting with getline](#chapter16.xhtml_sec130)

[Manipulating input & output](#chapter16.xhtml_sec131)

[Predicting problems](#chapter16.xhtml_sec132)

[Recognizing exceptions](#chapter16.xhtml_sec133)

[Handling errors](#chapter16.xhtml_sec134)

[Summary](#chapter16.xhtml_sec135)

[17 **Pointing to data**](#chapter17.xhtml)

[Understanding data storage](#chapter17.xhtml_sec136)

[Getting values with pointers](#chapter17.xhtml_sec137)

[Doing pointer arithmetic](#chapter17.xhtml_sec138)

[Passing pointers to functions](#chapter17.xhtml_sec139)

[Making arrays of pointers](#chapter17.xhtml_sec140)

[Referencing data](#chapter17.xhtml_sec141)

[Passing references to functions](#chapter17.xhtml_sec142)

[Comparing pointers & references](#chapter17.xhtml_sec143)

[Summary](#chapter17.xhtml_sec144)

[18 **Creating classes and objects**](#chapter18.xhtml)

[Encapsulating data](#chapter18.xhtml_sec145)

[Creating an object](#chapter18.xhtml_sec146)

[Creating multiple objects](#chapter18.xhtml_sec147)

[Initializing class members](#chapter18.xhtml_sec148)

[Overloading methods](#chapter18.xhtml_sec149)

[Inheriting class properties](#chapter18.xhtml_sec150)

[Calling base constructors](#chapter18.xhtml_sec151)

[Overriding base methods](#chapter18.xhtml_sec152)

[Summary](#chapter18.xhtml_sec153)

[19 **Harnessing polymorphism**](#chapter19.xhtml)

[Pointing to classes](#chapter19.xhtml_sec154)

[Calling a virtual method](#chapter19.xhtml_sec155)

[Directing method calls](#chapter19.xhtml_sec156)

[Providing capability classes](#chapter19.xhtml_sec157)

[Making abstract data types](#chapter19.xhtml_sec158)

[Building complex hierarchies](#chapter19.xhtml_sec159)

[Isolating class structures](#chapter19.xhtml_sec160)

[Employing isolated classes](#chapter19.xhtml_sec161)

[Summary](#chapter19.xhtml_sec162)

[20 **Processing macros**](#chapter20.xhtml)

[Exploring compilation](#chapter20.xhtml_sec163)

[Defining substitutes](#chapter20.xhtml_sec164)

[Defining conditions](#chapter20.xhtml_sec165)

[Providing alternatives](#chapter20.xhtml_sec166)

[Guarding inclusions](#chapter20.xhtml_sec167)

[Using macro functions](#chapter20.xhtml_sec168)

[Building strings](#chapter20.xhtml_sec169)

[Debugging assertions](#chapter20.xhtml_sec170)

[Summary](#chapter20.xhtml_sec171)

[21 **Programming visually**](#chapter21.xhtml)

[Starting a Universal project](#chapter21.xhtml_sec172)

[Inserting page components](#chapter21.xhtml_sec173)

[Importing program assets](#chapter21.xhtml_sec174)

[Designing the layout](#chapter21.xhtml_sec175)

[Adding runtime function](#chapter21.xhtml_sec176)

[Testing the program](#chapter21.xhtml_sec177)

[Adjusting the interface](#chapter21.xhtml_sec178)

[Deploying the application](#chapter21.xhtml_sec179)

[Summary](#chapter21.xhtml_sec180)

[22 **Getting started with C#**](#chapter22.xhtml)

[Introducing C#](#chapter22.xhtml_sec181)

[Installing Visual Studio](#chapter22.xhtml_sec182)

[Exploring the IDE](#chapter22.xhtml_sec183)

[Starting a Console project](#chapter22.xhtml_sec184)

[Running a Console project](#chapter22.xhtml_sec185)

[Following the rules](#chapter22.xhtml_sec186)

[Summary](#chapter22.xhtml_sec187)

[23 **Storing values**](#chapter23.xhtml)

[Creating variables](#chapter23.xhtml_sec188)

[Reading input](#chapter23.xhtml_sec189)

[Employing arrays](#chapter23.xhtml_sec190)

[Casting data types](#chapter23.xhtml_sec191)

[Fixing constants](#chapter23.xhtml_sec192)

[Summary](#chapter23.xhtml_sec193)

[24 **Performing operations**](#chapter24.xhtml)

[Doing arithmetic](#chapter24.xhtml_sec194)

[Assigning values](#chapter24.xhtml_sec195)

[Comparing values](#chapter24.xhtml_sec196)

[Assessing logic](#chapter24.xhtml_sec197)

[Examining conditions](#chapter24.xhtml_sec198)

[Setting precedence](#chapter24.xhtml_sec199)

[Summary](#chapter24.xhtml_sec200)

[25 **Making statements**](#chapter25.xhtml)

[Branching with if](#chapter25.xhtml_sec201)

[Switching branches](#chapter25.xhtml_sec202)

[Looping for](#chapter25.xhtml_sec203)

[Looping while](#chapter25.xhtml_sec204)

[Iterating for each](#chapter25.xhtml_sec205)

[Summary](#chapter25.xhtml_sec206)

[26 **Devising methods**](#chapter26.xhtml)

[Creating function](#chapter26.xhtml_sec207)

[Passing arguments](#chapter26.xhtml_sec208)

[Overloading methods](#chapter26.xhtml_sec209)

[Refactoring code](#chapter26.xhtml_sec210)

[Summary](#chapter26.xhtml_sec211)

[27 **Handling strings**](#chapter27.xhtml)

[Discovering string features](#chapter27.xhtml_sec212)

[Manipulating strings](#chapter27.xhtml_sec213)

[Joining and comparing strings](#chapter27.xhtml_sec214)

[Copying and swapping strings](#chapter27.xhtml_sec215)

[Finding substrings](#chapter27.xhtml_sec216)

[Formatting strings](#chapter27.xhtml_sec217)

[Formatting date strings](#chapter27.xhtml_sec218)

[Summary](#chapter27.xhtml_sec219)

[28 **Accessing files**](#chapter28.xhtml)

[Writing a file](#chapter28.xhtml_sec220)

[Appending to a file](#chapter28.xhtml_sec221)

[Reading text and lines](#chapter28.xhtml_sec222)

[Streaming lines](#chapter28.xhtml_sec223)

[Manipulating input and output](#chapter28.xhtml_sec224)

[Summary](#chapter28.xhtml_sec225)

[29 **Solving problems**](#chapter29.xhtml)

[Detecting real-time errors](#chapter29.xhtml_sec226)

[Fixing compile-time errors](#chapter29.xhtml_sec227)

[Debugging code](#chapter29.xhtml_sec228)

[Setting breakpoints](#chapter29.xhtml_sec229)

[Catching runtime errors](#chapter29.xhtml_sec230)

[Getting help](#chapter29.xhtml_sec231)

[Summary](#chapter29.xhtml_sec232)

[30 **Creating objects**](#chapter30.xhtml)

[Encapsulating data](#chapter30.xhtml_sec233)

[Creating multiple objects](#chapter30.xhtml_sec234)

[Initializing class members](#chapter30.xhtml_sec235)

[Inheriting class properties](#chapter30.xhtml_sec236)

[Calling base constructors](#chapter30.xhtml_sec237)

[Hiding base methods](#chapter30.xhtml_sec238)

[Directing method calls](#chapter30.xhtml_sec239)

[Providing capability classes](#chapter30.xhtml_sec240)

[Employing partial classes](#chapter30.xhtml_sec241)

[Summary](#chapter30.xhtml_sec242)

[31 **Controlling events**](#chapter31.xhtml)

[Starting a Forms project](#chapter31.xhtml_sec243)

[Adding visual controls](#chapter31.xhtml_sec244)

[Writing functional code](#chapter31.xhtml_sec245)

[Gathering text entries](#chapter31.xhtml_sec246)

[Ticking option boxes](#chapter31.xhtml_sec247)

[Showing user messages](#chapter31.xhtml_sec248)

[Calling system dialogs](#chapter31.xhtml_sec249)

[Creating application menus](#chapter31.xhtml_sec250)

[Making menus work](#chapter31.xhtml_sec251)

[Importing audio resources](#chapter31.xhtml_sec252)

[Summary](#chapter31.xhtml_sec253)

[32 **Building an application**](#chapter32.xhtml)

[Planning the program](#chapter32.xhtml_sec254)

[Assigning fixed properties](#chapter32.xhtml_sec255)

[Designing the layout](#chapter32.xhtml_sec256)

[Setting dynamic properties](#chapter32.xhtml_sec257)

[Adding runtime function](#chapter32.xhtml_sec258)

[Testing the program](#chapter32.xhtml_sec259)

[Publishing the application](#chapter32.xhtml_sec260)

[Summary](#chapter32.xhtml_sec261)

[33 **Targeting devices**](#chapter33.xhtml)

[Starting a Universal project](#chapter33.xhtml_sec262)

[Inserting page components](#chapter33.xhtml_sec263)

[Importing program assets](#chapter33.xhtml_sec264)

[Designing the layout](#chapter33.xhtml_sec265)

[Adding runtime function](#chapter33.xhtml_sec266)

[Testing the program](#chapter33.xhtml_sec267)

[Adjusting the interface](#chapter33.xhtml_sec268)

[Deploying the application](#chapter33.xhtml_sec269)

[Summary](#chapter33.xhtml_sec270)

**How to use this book**

The creation of this book has provided me, Mike McGrath, a welcome opportunity to update my previous books on coding programs with the C, C++ and C# programming languages. Examples I provide in this book demonstrate C and C++ features supported by current compilers on both Windows and Linux operating systems, and demonstrate C# features in the Microsoft Visual Studio development suite – all **in easy steps**.

**Conventions in this book**

In order to clarify the code listed in the steps, I have adopted certain colorization conventions. Keywords of each language are Blue, numeric and string values are Red, programmer-specified names are Black, comments are Green, C# classes are LightBlue and C# methods are Brown:

**/* Store then output a text string value. */**

**char *myMessage = “Hello from C” ;**

**printf( myMessage ) ;**

**// Store then output a text string value.**

**string myMessage = “Hello from C++!” ;**

**cout << myMessage ;**

**// Store then output a text string value.**

**string myMessage = “Hello from C#!” ;**

**Console.Write( myMessage ) ;**

Additionally, in order to identify each source code file described in the steps a colored icon and file name appears in the margin alongside the steps:

![image](images/commonc.jpg)

hello.c

![image](images/commonc2.jpg)

hello.cpp

![image](images/commonc3.jpg)

Hello

![image](images/pgb6_2.jpg)

header.h

**Grabbing the source code**

For convenience I have placed source code files from all examples featured in this book into a single ZIP archive. To download the archive visit [**www.ineasysteps.com**](http://www.ineasysteps.com) and sign in, then select **Free Resources**, then select **BROWSE NOW** in the **Source code and other book resources** section and choose **All code examples** for the C, C++ & C# book. This book’s screenshots illustrate the actual results produced by compiling and executing the listed code in each example. If you don’t achieve the illustrated result, simply compare your code to that in the original source code to discover where you went wrong.

I sincerely hope you enjoy discovering the powerful expressive possibilities of C, C++ and C# programming and have as much fun with it as I did in writing this book.

![image](images/author.jpg)

1

**Getting started with C**

*Welcome to the world of C. This chapter demonstrates how to create a C program in text, then how to compile it into executable byte form.*

[**Introducing the C language**](#chapter01.xhtml_sec1)

[**Installing a C compiler**](#chapter01.xhtml_sec2)

[**Writing a C program**](#chapter01.xhtml_sec3)

[**Compiling a C program**](#chapter01.xhtml_sec4)

[**Understanding compilation**](#chapter01.xhtml_sec5)

[**Summary**](#chapter01.xhtml_sec6)

**Introducing the C language**

C is a compact, general-purpose computer programming language that was originally developed by Dennis MacAlistair Ritchie for the Unix operating system. It was first implemented on the Digital Equipment Corporation PDP-11 computer in 1972.

![image](images/pg14_1.jpg)

This new programming language was named “C” as it succeeded an earlier programming language named “B” that had been introduced around 1970.

The Unix operating system and virtually all Unix applications are written in the C language. However, C is not limited to a particular platform and programs can be created on any machine that supports C, including those running the Windows platform.

The flexibility and portability of C made it very popular and the language was formalized in 1989 by the American National Standards Institute (ANSI). The ANSI standard unambiguously defined each aspect of C, thereby eliminating previous uncertainty about the precise syntax of the language.

ANSI C has become the recognized standard for the C language and is described, and demonstrated by examples, in this book.

![image](images/pga8_1.jpg)

Dennis M Ritchie, creator of the C programming language.

**Why learn C programming?**

The C language has been around for quite some time and has seen the introduction of newer programming languages like Java, C++, and C#. Many of these new languages are derived, at least in part, from C – but are much larger in size. The more compact C is better to start out in programming because it’s simpler to learn.

It is easier to move on to learn the newer languages once the principles of C programming have been grasped. For instance, C++ is an extension of C and can be difficult to learn unless you have mastered C programming first.

Despite the extra features available in newer languages, C remains popular because it is versatile and efficient. It is used today on a large number of platforms, for everything from micro-controllers to the most advanced scientific systems. Programmers around the world embrace C because it allows them maximum control and efficiency in their programs.

![image](images/forget.jpg)

Programs written 20 years ago in C are still just as valid today as they were back then.

**Standard C libraries**

ANSI C defines a number of standard libraries that contain tried-and-tested functions, which can be used in your own C programs.

The libraries are contained in “header files” that each has a file extension of “.h”. The names of the standard C library header files are listed in the table below with a description of their purpose:

| **Library** | **Description** |
| **stdio.h** | Contains input and output functions, types, and macro definitions. This library is used by most C programs and represents almost one third of the entire C libraries |
| **ctype.h** | Contains functions for testing characters |
| **string.h** | Contains functions for manipulating strings |
| **math.h** | Contains mathematical functions |
| **stdlib.h** | Contains utility functions for number conversion, storage allocation, etc. |
| **assert.h** | Contains a function that can be used to add diagnostics to a program |
| **stdarg.h** | Contains a function that can be used to step through a list of function arguments |
| **setjmp.h** | Contains a function that can be used to avoid the normal call and return sequence |
| **signal.h** | Contains functions for handling exceptional conditions that may arise in a program |
| **time.h** | Contains functions for manipulating date and time components |
| **limits.h** | Contains constant definitions for the size of C data types |
| **float.h** | Contains constant definitions relating to floating-point arithmetic |

![image](images/snake.jpg)

The keywords listed below have special significance in C programming and may not be used for other purposes.

| **C Keywords** |
| **auto** | **int** |
| **break** | **long** |
| **case** | **register** |
| **char** | **return** |
| **const** | **short** |
| **continue** | **signed** |
| **default** | **sizeof** |
| **do** | **static** |
| **double** | **struct** |
| **else** | **switch** |
| **enum** | **typedef** |
| **extern** | **union** |
| **float** | **unsigned** |
| **for** | **void** |
| **goto** | **volatile** |
| **if** | **while** |

**Installing a C compiler**

C programs are initially created as plain text files, saved with a “.c” file extension. These can be written in any plain text editor such as Windows’ Notepad application – no special software is needed.

In order to execute a C program it must first be “compiled” into byte code that can be understood by the computer. A C compiler reads the original text version of the program and translates it into a second file, which is in machine-readable executable byte format.

If the text program contains any syntax errors these will be reported by the compiler, and the executable file will not be built.

One of the most popular C compilers is the GNU C Compiler (GCC) that is available free under the terms of the General Public License (GPL). It is included with almost all distributions of the Linux operating system. The GNU C Compiler is used to compile all the examples in the C and C++ sections of this book into executable byte code.

![image](images/pga10_1.jpg)

“GNU” is a recursive acronym for “Gnu’s Not Unix” and it is pronounced “guh-new”. You can find more details at **[www.gnu.org](http://www.gnu.org)**

To discover if you already have the GNU C Compiler on your system, type **gcc -v** at a command prompt. If it is available the compiler will respond with version information:

![image](images/pg16_1.jpg)

If you are using the Linux operating system and the GNU C Compiler is not available, install it from the distribution disk or online repository, or ask your system administrator to install it.

If you are using the Windows operating system and the GNU C Compiler is not already available, you can download and install the Minimalist GNU for Windows (MinGW) package, which includes the GNU C Compiler, by following the steps opposite.

![image](images/forget.jpg)

When a C compiler is installed the standard C library header files (listed [here](#chapter01.xhtml_clib)) will also be installed.

![image](images/1b.jpg)With an internet connection open, launch a web browser then navigate to **[sourceforge.net/projects/mingw](http://www.sourceforge.net/projects/mingw)** and click the “Download” button to get the MinGW setup installer

![image](images/2b.jpg)Launch the setup installer and accept the suggested location of **C:\MinGW** in the “Installation Manager” dialog

![image](images/3b.jpg)Choose the “Basic” and “C++ Compiler” items then click **Installation**, **Apply Changes** to complete the installation

![image](images/pga11_1.jpg)

The MinGW C++ Compiler is a binary executable file located at **C:\MinGW\bin**. To allow it to be accessible from any system location this folder should now be added to the System Path:

![image](images/4b.jpg)In Windows’ Control Panel, click the **System** icon then select the **Advanced System Settings** item to launch the “System Properties” dialog

![image](images/5b.jpg)In the System Properties dialog, click the **Environment Variables** button, select the **Path** system variable, then click the **Edit** button and add the location **C:\MinGW\bin;**

![image](images/pg17_3.jpg)

![image](images/6b.jpg)Click **OK** to close each dialog, then open a “Command Prompt” window and enter the command **gcc -v** to see the compiler respond with version information

![image](images/pg17_2.jpg)

![image](images/hot.jpg)

Because C++ is an extension of C any C++ development tool can also be used to compile C programs.

![image](images/forget.jpg)

The MinGW installation process may be subject to change, but current guidance can be found at **[mingw.org/wiki/Getting_Started](http://www.mingw.org/wiki/Getting_Started)**

**Writing a C program**

In C programs the code statements to be executed are contained within “functions”, which are defined using this syntax format:

***data-type function-name ( ) { statements-to-be-executed }***

After a function has been called upon to execute the statements it contains, it can return a value to the caller. This value must be of the data type specified before the function name.

A program can contain one or many functions but must always have a function named “main”. The **main()** function is the starting point of all C programs, and the C compiler will not compile the code unless it finds a **main()** function within the program.

Other functions in a program may be given any name you like using letters, digits, and the underscore character, but the name may not begin with a digit. Also, the C keywords, listed in the table on the front inner cover of this book, must be avoided.

The **( )** parentheses that follow the function name may, optionally, contain values to be used by that function. These take the form of a comma-separated list and are known as function “arguments” or “parameters”.

The **{ }** curly brackets (braces) contain the statements to be executed whenever that function is called. Each statement must be terminated by a semicolon, in the same way that English language sentences must be terminated by a period/full stop.

Traditionally, the first program to attempt when learning any programming language is that which simply generates the message “Hello World”.

![image](images/pg18_1.jpg)

hello.c

![image](images/1b.jpg)Open a plain text editor, such as Notepad, then type this line of code at the start of the page, exactly as it is listed

**#include <stdio.h>**

The program begins with an instruction to the C compiler to include information from the standard input/output **stdio.h** library file. This makes the functions contained within that library available for use within this program. The instruction is more properly called a “preprocessor instruction” or “preprocessor directive” and must always appear at the start of the page, before the actual program code is processed.

![image](images/snake.jpg)

Do not use word processor applications to create program code as they store additional formatting information that prevents code compilation.

![image](images/forget.jpg)

Preprocessor instructions begin with a **#** hash character and must enclose standard library names within **< >** angled brackets.

![image](images/2b.jpg)Two lines below the preprocessor instruction, add an empty main function

**int main()**

**{**

**}**

This function declaration specifies that an integer value, of the **int** data type, should be returned by the function upon completion.

![image](images/3b.jpg)Between the braces, insert a line of code that calls upon one of the functions defined in the standard input/output library – made available by the preprocessor instruction
**printf ( “Hello World!\n” ) ;**

Here the **printf()** function specifies a single string argument between its parentheses. In C programming, strings must always be enclosed within double quotes. This string contains the text **Hello World** and the **\n** “newline” escape sequence that moves the print head to the left margin of the next line.

![image](images/4b.jpg)Between the braces, insert a final line of code to return a zero integer value, as required by the function declaration
**return 0 ;**

Traditionally, returning a value of zero after the execution of a program indicates to the operating system that the program executed correctly.

![image](images/5b.jpg)Check that the program code looks exactly like the listing below, then add a final newline character (hit Return after the closing brace) and save the program as “hello.c”

**#include <stdio.h>**

**int main()**

**{**

**printf( “Hello World!\n” ) ;**

**return 0 ;**

**}**

The complete program in text format is now ready to be compiled into machine-readable byte format as an executable file.

![image](images/hot.jpg)

Whitespace between the code is ignored by the C compiler but program code should always end with a newline character.

![image](images/forget.jpg)

Each statement must be terminated by a semicolon character.

**Compiling a C program**

The C source code files for the examples in this book are stored in a directory created expressly for that purpose. The directory is named “MyPrograms” and its absolute address on Windows is **C:\MyPrograms**, whereas on Linux it’s at **/home/user/MyPrograms**. The **hello.c** source code file, created by following the steps [here](#chapter01.xhtml_sec3), is saved in this directory awaiting compilation to produce a version in executable byte code format.

![image](images/1b.jpg)At a command prompt, issue a **cd** command with the path to the **MyPrograms** directory to navigate there

![image](images/2b.jpg)At a command prompt in the **MyPrograms** directory, type **gcc hello.c** then hit Return to compile the program

When the compilation succeeds, the compiler creates an executable file alongside the original source code file. By default, this file will be named **a.out** on Linux systems and **a.exe** on Windows systems. Compiling a different C source code file in the **MyPrograms** directory would now overwrite the first executable file without warning. This is obviously unsatisfactory so a custom name for the executable file must be specified when compiling **hello.c**. This can be achieved by including a **-o** option followed by a custom name in the compiler command.

![image](images/3b.jpg)At a command prompt in the **MyPrograms** directory, type **gcc hello.c -o hello.exe** then hit Return to compile the program once more

On both Linux and Windows systems an executable file named **hello.exe** is now created alongside the C source code file:

![image](images/pga14_1.jpg)

![image](images/pga15_1.jpg)

![image](images/hot.jpg)

At a command prompt, type **gcc --help** then hit Return to see a list of all compiler options.

![image](images/4b.jpg)At a command prompt in Windows, type the executable filename then hit Return to run the program – the text string is output and the print head moves to the next line

![image](images/pga15_2.jpg)

Because Linux does not by default look in the current directory for executable files, unless it is specifically directed to do so, it is necessary to prefix the filename with **./** to execute the program.

![image](images/5b.jpg)At a command prompt in Linux, type **./hello.exe** then hit Return to run the program – the text string is output and the print head moves to the next line

![image](images/pga15_3.jpg)

You have now created, compiled, and executed the simple Hello World program that is the starting point in C programming. All other examples in the C section of this book will be created, compiled, and executed in the same way.

![image](images/forget.jpg)

If the compiler complains that there is no new line at the end of the file add a carriage return to the end of the source code, then save and retry.

![image](images/hot.jpg)

Windows users can even omit the file extension to run programs. In this case, typing just **hello** is sufficient.

**Understanding compilation**

In producing an executable file from an original C source code file, the compilation process actually undergoes four separate stages, which each generate a new file:

![image](images/pga16_1.jpg)

•Preprocessing – The preprocessor substitutes all preprocessor directives in the original source code **.c** file with actual library code that implements those directives. For instance, library code is substituted for **#include** directives. The generated file containing the substitutions is in text format and typically has a **.i** file extension.

•Translating – The compiler translates the high-level instructions in the **.i** file into low-level Assembly language instructions. The generated file containing the translation is in text format and typically has a **.s** file extension.

•Assembling – The assembler converts the Assembly language text instructions in the **.s** file into machine code. The generated object file containing the conversion is in binary format and typically has a **.o** file extension.

•Linking – The linker combines one or more binary object **.o** files into a single executable file. The generated file is in binary format and typically has a **.exe** file extension.

Strictly speaking, “compilation” describes the first three stages above, which operate on a single source code text file and ultimately generate a single binary object file. Where the program source code contains syntax errors, such as a missing semicolon statement terminator or a missing parenthesis, they will be reported by the compiler and compilation will fail.

The linker, on the other hand, can operate on multiple object files and ultimately generates a single executable file. This allows the creation of large programs from modular object files that may each contain reusable functions. Where the linker finds a function of the same name defined in multiple object files it will report an error and the executable file will not be created.

Normally, the temporary files created during the intermediary stages of the compilation process are automatically deleted, but they can be retained for inspection by including a **-save-temps** option in the compiler command:

![image](images/1b.jpg)At a command prompt in the **MyPrograms** directory, type **gcc hello.c -save-temps -o hello.exe** then hit Return to recompile the program and save the temporary files

![image](images/pga17_1.jpg)

![image](images/2b.jpg)Open the **hello.i** file in a plain text editor such as Windows’ Notepad, to see your source code at the very end of the file preceded by substituted **stdio.h** library code

![image](images/3b.jpg)Now, open the **hello.s** file in a plain text editor to see the translation into low-level Assembly code and note how unfriendly that appears in contrast to the C code version

![image](images/pga17_2.jpg)

![image](images/hot.jpg)

Programs tediously written in Assembly language can run faster than those written in C but are more difficult to develop and maintain. For traditional computer programming, C is almost always the first choice.

**Summary**

![image](images/pgc20_1.jpg)

•The American National Standards Institute (ANSI) established the recognized standard for the C programming language.

•Other programming languages, such as C++ and C#, are derived in part from the C language.

•The C language has a number of standard libraries containing tried-and-tested functions that can be used in any program.

•C libraries are contained in header files whose names have a **.h** file extension.

•C programs are created as plain text files whose names have a **.c** file extension.

•The popular GNU C Compiler (GCC) is included in the Minimalist GNU for Windows (MinGW) package.

•Adding the compiler’s host directory to the system path conveniently allows the compiler to be run from any directory.

•Programs have one or more functions containing statements to be executed whenever the function is called.

•Every C program must have a **main()** function.

•A function declaration begins by specifying the data type of the value to be returned after the function has been executed.

•The statements to be executed are contained within **{ }** braces and each statement must end with a **;** semicolon terminator.

•Preprocessor instructions are implemented in the first stage of program compilation and will typically substitute library code.

•The GNU C Compiler is run with the **gcc** command and may include a **-o** option to name the executable output file.

•Temporary files created during the compilation process can be retained using the **-save-temps** compiler command option.

2

**Storing variable values**

***This chapter demonstrates how to store, retrieve, and manipulate various types of data using variable containers in C programs.***

[**Creating program variables**](#chapter02.xhtml_sec7)

[**Displaying variable values**](#chapter02.xhtml_sec8)

[**Inputting variable values**](#chapter02.xhtml_sec9)

[**Qualifying data types**](#chapter02.xhtml_sec10)

[**Using global variables**](#chapter02.xhtml_sec11)

[**Registering variables**](#chapter02.xhtml_sec12)

[**Converting data types**](#chapter02.xhtml_sec13)

[**Creating array variables**](#chapter02.xhtml_sec14)

[**Describing dimensions**](#chapter02.xhtml_sec15)

[**Summary**](#chapter02.xhtml_sec16)

**Creating program variables**

![image](images/pg26_1.jpg)

A variable is a container in a C program in which a data value can be stored inside the computer’s memory. The stored value can be referenced using the variable’s name. The programmer can choose any name for a variable providing it adheres to the naming conventions listed in the table below:

| **Naming Rule** | **Example** |
| CANNOT contain any of the C keywords | **volatile** |
| CANNOT contain arithmetic operators | **a+b*c** |
| CANNOT contain punctuation characters | **%$#@!** |
| CANNOT contain any spaces | **no spaces** |
| CANNOT start with a number | **2bad** |
| CAN contain numbers elsewhere | **good1** |
| CAN contain mixed case | **UPdown** |
| CAN contain underscores | **is_ok** |

It is good practice to choose meaningful names for variables to make the program code more easily understood. To create a variable in the program simply requires it to be “declared”.

A variable declaration has this syntax:

***data-type variable-name ;***

First, the declaration specifies which type of data the variable is permitted to contain. This will be one of the four data types described [here](#chapter02.xhtml_dataty). The data type is followed by a space then the chosen variable name, adhering to the naming conventions in the table above. As with all statements in C programs, the declaration must end with a semicolon terminator. Multiple variables of the same data type can be created in a single declaration as a comma-separated list, like this:

***data-type variable-name-1 , variable-name-2 , variable-name-3 ;***

![image](images/snake.jpg)

Variable names are case-sensitive in C – so variables named “VAR”, “Var”, and “var” would be treated as three separate variables.

![image](images/forget.jpg)

C keywords are listed [here](#chapter01.xhtml_keyw).

There are four basic data types in the C language. These are defined using the C keywords that are listed in the table below, together with a description of each data type:

| **Data Type** | **Description** | **Example** |
| **char** | A single byte, capable of storing just one character | **‘A’** |
| **int** | An integer whole number | **100** |
| **float** | A floating-point number, correct to six decimal places | **0.123456** |
| **double** | A floating-point number, correct to 10 decimal places | **0.0123456789** |

The four data types allocate different amounts of machine memory for storing data. The smallest is the **char** data type, which allocates just a single byte of memory; and the largest is the **double** data type, which typically allocates eight bytes of memory. This is twice the amount of memory allocated by the **float** data type so the **double** data type should only be used when a lengthy, precise floating-point number is a necessity.

Variable declarations should be made before any executable code appears in the program. When a value is assigned to a variable, that variable is said to have been “initialized”. Optionally, a variable may be initialized when it is declared.

The example code fragment below declares and initializes various variables with appropriate values as described in the code comments – descriptive comments between **/*** and ***/** that are ignored by the compiler:

| **int num1 , num2 ;** | **/* Declares two integer variables. */** |
| **char letter ;** | **/* Declares a character variable. */** |
| **float decimal = 7.5 ;** | **/* Declares and initializes** **a floating-point variable. */** |
| **num1 = 100 ;** | **/* Initializes the integer variables. */** |
| **num 2 = 200 ;** |  |
| **letter = ‘A’ ;** | **/* Initializes the character variable. */** |

![image](images/snake.jpg)

Values of the **char** data type must always be enclosed by single quotes – double quotes are incorrect.

![image](images/hot.jpg)

In a variable assignment the part to the left of the **=** operator is known as the L-value object and that to its right is known as the R-value data.

**Displaying variable values**

The value of variables can be displayed using the **printf()** function that was used in [Chapter 1](#chapter01.xhtml) to display the “Hello World” message. The desired format in which to display the variable value must be specified as an argument in the **printf()** function’s parentheses using a suitable “format specifier”, along with the variable name:

| **Specifier** | **Description** | **Example** |
| **%d** | An integer -32768 to +32767 | **100** |
| **%ld** | A long integer -2^(31) to +2^(31) | **123456789** |
| **%f** | A floating-point number | **0.123456** |
| **%c** | A single character | **‘A’** |
| **%s** | A string of characters | **“Hello World”** |
| **%p** | A machine memory address | **0x0022FF34** |

A format specifier can ensure that the output occupies a specific minimum number of spaces by stating the required number immediately after the **%** character – for example, to ensure that an integer always fills at least seven spaces with the specifier **%7d**. If it is preferable for the blank spaces to be filled with zeros just add a zero between the **%** character and the specified number – for example, to ensure that an integer always fills at least seven spaces and that blank spaces are filled with zeros with the specifier **%07d**.

A precision specifier, which is a period (full stop) followed by a number, can be used with the **%f** format specifier to determine how many decimal places to display – for example, to display just two decimal places with the precision specifier **%.2f**. The precision specifier can also be combined with the minimum space specifier to control both the minimum number of spaces and number of decimal places to display – for example, to display seven spaces including two decimal places and empty spaces filled by zeros with **%07.2f**.

By default, empty spaces precede the number so it is right-aligned, but can be added after the number to make it left-aligned by prefixing the minimum space specifier with a minus sign.

![image](images/forget.jpg)

Single **char** character values must be enclosed by single quotes – a string of multiple characters, on the other hand, must be enclosed by double quotes.

![image](images/commoncr.jpg)

vars.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Add a main function that declares and initializes two variables

**int main()**

**{**

**int num = 100 ;**

**double pi = 3.1415926536 ;**

**}**

![image](images/3r.jpg)In the main function, after the variable declarations, insert statements to output the variable values in various formats

**printf( “Integer is %d \n”, num ) ;**

**printf( “Values are %d and %f \n”, num, pi ) ;**

**printf( “%%7d displays %7d \n”, num ) ;**

**printf( “%%07d displays %07d \n”, num ) ;**

**printf( “Pi is approximately %1.10f \n”, pi ) ;**

**printf( “Right-aligned %20.3f rounded pi \n”, pi ) ;**

**printf( “Left-aligned %-20.3f rounded pi \n”, pi ) ;**

![image](images/4r.jpg)At the end of the main function block, insert a final statement to return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/5r.jpg)Save the program file then, at a command prompt, compile and execute the program to see the variable values be output in the specified formats

![image](images/pga23_1.jpg)

![image](images/hot.jpg)

To display a “%” character with the **printf()** function, prefix it with another “%” character, as seen here.

![image](images/snake.jpg)

Notice that the floating-point value is rounded when the format specifier allocates fewer decimal places – it is not simply truncated.

**Inputting variable values**

The standard input/output library **stdio.h** provides a **scanf()** function that can be used to get user input into a program. The **scanf()** function requires two arguments within its parentheses to specify the type of data to be input and the location where the input should be stored.

The first argument to the **scanf()** function must be one of the format specifiers from the table [here](#chapter02.xhtml_spec) between double quotes – for example, **“%d”** where input is an integer value. The second argument to the **scanf()** function must be a variable name preceded by the **&** character, except when the input data is a string of text. The **&** character has several uses in C programming but in this context is the “addressof” operator, which means that the input data should be stored at the memory location reserved for that variable.

When a variable is declared, space is reserved in the machine’s memory to store the data assigned to that variable. The number of bytes reserved depends on the data type of the variable. The allocated memory is referenced by the unique variable name.

Envision the computer’s memory as a very long row of slots. Each slot has a unique address, which is expressed in hexadecimal format. It’s like a long road of houses – each house contains people and has a unique numeric address. In C programs the houses are the slots, and the people are the data contained in those addresses.

The **scanf()** function can simultaneously assign values to multiple variables too. Its first argument must then contain a list of format specifiers, each separated by a space, and the entire list must be enclosed by double quotes. The second argument must contain a comma-separated list of variable names, each preceded by the **&** addressof operator, to which each specified format applies.

The **&** addressof operator can also be used to return the hexadecimal memory address at which the variable data is stored.

Combining output from the **printf()** function and input from the **scanf()** function creates basic interactivity between the user and the program.

![image](images/hot.jpg)

Strings are a special case and are demonstrated with the topic of arrays [here](#chapter02.xhtml_sec14).

![image](images/snake.jpg)

Note that the **scanf()** function stops reading input when it encounters a space.

![image](images/commoncr.jpg)

setvars.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Add a main function that declares three variables

**int main()**

**{**

**char letter ;**

**int num1 , num2 ;**

**}**

![image](images/3r.jpg)In the main function, after the variable declarations, insert statements to get input from the user

**printf( “Enter any one keyboard character: “ ) ;**

**scanf( “%c”, &letter ) ;**

**printf( “Enter two integers separated by a space: “ ) ;**

**scanf( “%d %d” , &num1, &num2 ) ;**

![image](images/4r.jpg)Next, insert statements to output the stored data details

**printf( “Numbers input: %d and %d \n”, num1, num2 ) ;**

**printf( “Letter input: %c “, letter ) ;**

**printf( “ Stored at: %p \n”, &letter ) ;**

![image](images/5r.jpg)At the end of the main function block, insert a final statement to return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/6r.jpg)Save the program file; compile and execute the program; input data when requested; then see the stored data output

![image](images/pga25_1.jpg)

![image](images/forget.jpg)

The format specifier for a machine address is **%p**.

**Qualifying data types**

When an integer variable, of the **int** data type, is created it can by default contain either positive or negative values. These are known as “signed” values. The range of possible values is determined by your system as either “long” or “short”.

If the **int** variable is created by default as a long type (likely) it will typically have a possible range of values from a maximum of +2,147,483,647 down to a minimum of -2,147,483,648.

On the other hand, if the **int** variable is created by default as a short type (unlikely) it will typically have a possible range of values from a maximum of +32,767 to a minimum of -32,768.

The range size can be explicitly specified, however, using the **short** and **long** qualifier keywords in the variable declaration, like this:

| **short int num1 ;** | **/* Saves memory space. */** |
| **long int num2 ;** | **/* Allows bigger range. */** |

The **limits.h** C library header file contains implementation-defined limits for the size of each data type. These can be accessed via constant values named **INT_MAX** and **INT_MIN** for **int** variable declarations of unspecified size. Similarly, **SHRT_MAX** and **SHRT_MIN** contain limits for **short int** variable declarations, and **LONG_MAX** and **LONG_MIN** contain limits for **long int** variable declarations.

A non-negative “unsigned” **int** variable can be declared using the **unsigned** qualifier keyword when the variable will never be assigned a negative value. An **unsigned short int** variable will typically have a possible range from 0 to 65,535 but only occupy the same memory space as a regular **short int** variable. An **unsigned long int** variable will typically have a possible range from 0 to 4,294,967,295 but will only occupy the same memory space as a regular **long int** variable.

The C **sizeof** operator can be used to reveal the amount of memory space reserved by variables of different data types. It is good programming practice to use the smallest amount of memory possible. For example, where a variable will only ever contain positive integer values below 65,535 it is preferable to use an **unsigned short int** variable that reserves just 2 bytes of memory rather than a **long int** variable that reserves 4 bytes of memory.

![image](images/hot.jpg)

Constants are always named entirely in uppercase to distinguish them from variables.

![image](images/forget.jpg)

The memory space allocated to an **int** variable of unspecified size is system-dependent but will often be treated as a **long int** by default.

![image](images/commoncr.jpg)

sizeof.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output functions and constants

**#include <stdio.h>**

**#include <limits.h>**

![image](images/2r.jpg)Add a main function that contains statements to output the size and range of the **short int** data type

**int main()**

**{**

**printf( “short int... \tsize: %d bytes \t”, sizeof( short int ));**

**printf( “%d to %d \n” , SHRT_MAX , SHRT_MIN ) ;**

**}**

![image](images/3r.jpg)Next, insert statements to output the size and range of the **long int** data type

**printf( “long int... \tsize: %d bytes \t” , sizeof( long int ) ) ;**

**printf( “%ld to %ld \n” , LONG_MAX , LONG_MIN ) ;**

![image](images/4r.jpg)Now, insert statements to output the size of other data

**printf( “char... \tsize: %d byte \n” , sizeof( char ) ) ;**

**printf( “float... \tsize: %d bytes \n” , sizeof( float ) ) ;**

**printf( “double... \tsize: %d bytes \n” , sizeof( double ) ) ;**

![image](images/5r.jpg)Insert a final statement to return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/6r.jpg)Save the program file, then compile and execute the program to see the data type sizes and ranges

![image](images/pga27_1.jpg)

![image](images/hot.jpg)

Notice how the **\t** tab escape sequence is used in this example to space the output.

**Using global variables**

The extent to which variables are accessible in a program is called the “variable scope”. Variables declared within a function are known as “local” variables, whereas variables declared outside any function blocks are known as “global” variables.

![image](images/pga28_1.jpg)

Local variables can only be accessed from within the function in which they are declared. This is the default implicit behavior that could be explicitly specified with the seldom-used **auto** keyword in the variable declaration. They come into existence when the function is called, and normally disappear when the function ends.

Global variables, on the other hand, can be accessed from within any function in the program. They come into existence when the program executes, and remain in existence until the program ends.

An external global variable must be defined exactly once at the start of the program. It must also be declared at the start of each function that needs access to it. The declaration should begin with the **extern** keyword to denote that it references an external variable, rather than a regular local variable declaration. These declarations should not be used to initialize the global variable.

Larger C programs often consist of multiple source code files that are compiled together to create a single executable file. Global variables are normally accessible from any function in any of the files being compiled together. All functions are normally accessible globally too, but functions and – more usually – global variables can have their accessibility limited to just the file in which they are created by the use of the **static** keyword in their declaration.

Normally, a program cannot employ multiple variables of the same name but can do so if each is declared to be a **static** variable and is unique within that source code file. Programming with multiple source code files can reveal a common global variable name duplicated in two different files. Declaring these as **static** avoids the need to rename one of the variables in each occurrence within the source code.

Internal local variables can also be declared as **static**. These are only accessible from within the function in which they are declared, as usual, but they do not disappear when the function ends. This allows permanent private storage within a function until the program ends.

![image](images/snake.jpg)

Widespread use of global variables can introduce name conflicts.

![image](images/forget.jpg)

Try to use only local variables. Global variables allow convenient access to values from any function within a program but it is better practice to avoid global variables and pass values between functions as arguments instead.

![image](images/commoncr.jpg)

global_1.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Define and initialize a global static variable that may only be accessed from within this source code file

**static int sum = 100 ;**

![image](images/3r.jpg)Add a main function that declares it wants to use the global static variable and output its value

**int main()**

**{**

**extern int sum ;**

**printf( “Sum is %d \n” , sum ) ;**

**}**

![image](images/4r.jpg)Now, insert a declaration to use a second global variable and output its value

**extern int num ;**

**printf( “Num is %d \n” , num ) ;**

![image](images/5r.jpg)Insert a final statement to return a zero integer value, as required by the function declaration, then save the file

**return 0 ;**

![image](images/6r.jpg)In a separate file define the second global variable, then save that file

**int num = 200 ;**

![image](images/commoncr.jpg)

global_2.c

![image](images/7r.jpg)Compile both source files into one executable program, by supplying each source code filename in the command, then execute the program to see the global values output

![image](images/pga29_1.jpg)

![image](images/hot.jpg)

Adding the **static** keyword to the **num** variable definition in the second file would limit its accessibility to just that file – so compilation would then fail.

**Registering variables**

A variable declaration that includes the **register** keyword advises the compiler that the specified variable will be heavily used by the program. The intention is for the compiler to place **register** variables in the machine registers of the computer to speed up access times. Their usefulness may be questionable, though, as compilers are free to ignore this advice.

Only local internal variables can be declared as **register** variables. In any case, only a few variables can be held in machine registers and they may only be of certain types. The precise limitations vary from machine to machine.

Despite these possible drawbacks, **register** declarations are harmless because the **register** keyword is ignored when the compiler cannot actually use the machine registers to store the variable. Instead, the variable is created as though the **register** keyword was not there.

The complete opposite of a **register** variable is achieved with a variable declaration that includes the **volatile** keyword. This means that the variable must not be stored in a machine register, as its value may change at any time without action being taken by any code the compiler finds nearby. This is particularly relevant to global variables in large programs that may be concurrently modified by multiple threads.

One sort of variable that might benefit from being a **register** variable is a local variable used to store the control value of a loop. On each iteration of the loop, that value must be compared and changed so the variable is being repeatedly accessed. Storing this value in a machine register could then speed up execution of the loop.

On the other hand, if a global variable is used to store the control value of a loop and may also be changed from outside the loop, that global variable might benefit from being a **volatile** variable.

Loop structures are described fully in [Chapter 5](#chapter05.xhtml), but the example listed opposite is included to illustrate the repeated access of a **register** variable.

![image](images/forget.jpg)

The **register** and **volatile** keywords are described here for completeness but are seldom found in reality as most programs simply use regular variables to store data.

![image](images/commoncr.jpg)

register.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Add a main function that declares and initializes a local register variable containing a loop control value of zero

**int main()**

**{**

**register int num = 0 ;**

**}**

![image](images/3r.jpg)Now, insert a conditional test to see if the control value is below five, followed by a pair of braces

**while ( num < 5 )**

**{                          }**

![image](images/4r.jpg)Between the braces of the loop structure, insert statements to increment the control value and output its current value on each iteration of the loop

**++num ;**

**printf( “Pass %d \n” , num ) ;**

![image](images/5r.jpg)At the end of the function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/6r.jpg)Save the program file, then compile and execute the program to see the values retrieved from the register variable on each iteration of the loop

![image](images/pga31_1.jpg)

![image](images/snake.jpg)

If the **&** addressof operator is used on a **register** variable the compiler will place the variable in a memory location rather than in a register.

**Converting data types**

The compiler will implicitly change one type of data into another if it seems logical to do so. For example, where an integer is assigned to a **float** variable, the compiler converts the integer to a floating-point value.

Any data stored in a variable can be explicitly forced (coerced) into a variable of a different data type by a process known as “casting”. A cast just states the data type to which the variable should be converted in parentheses before the name of the variable storing the data in its original data type. The parentheses should also include any modifiers, such as **unsigned**, where appropriate – so the syntax of a cast looks like this:

***variable-name2 = ( modifiers data-type ) variable-name1 ;***

Note that casting does not change the original data type of the variable but merely copies that value as a different data type.

When casting from a **float** variable into an **int** variable the value is simply truncated at the decimal point. There is no rounding to the nearest integer. For example, with **float num = 5.75** the cast to an integer with **(int)num** produces the integer **5**, not **6**.

When casting from a **char** variable to an **int** variable the resulting integer value is the numerical ASCII code value that represents that character. The uppercase alphabet has numerical ASCII values 65-90, whereas the lowercase alphabet has 97-122\. For example, with **char letter = ‘A’** the cast to an integer with **(int) letter** produces the integer **65**. Casting integer values within these ranges to a **char** data type produces the equivalent letter.

It is often necessary to cast integer values into their floating-point equivalents to perform accurate arithmetic. Division can otherwise produce a truncated integer result. For example, with **int x=7,y=5** the statement **float z = x / y** assigns the value of **1.000000**. Accurate arithmetic requires the statement to use casts as **(float)x / (float)y** produces the floating-point value of **1.400000**.

Casting long, precise floating-point numbers from a **double** data type into a shorter **float** data type does not simply truncate the longer value at the sixth decimal place but rounds up or down to the nearest figure. For example, with **double decimal = 0.1234569** the cast to a float with **(float)decimal** produces **0.123457**.

![image](images/hot.jpg)

ASCII (pronounced as “as-kee”) is an acronym for “American Standard Code for Information Interchange” and is the accepted standard for plain text. You can find the full range of standard ASCII codes [here](#chapter11.xhtml_sec78).

![image](images/hot.jpg)

The **/** forward slash character is the division operator in the C language.

![image](images/commoncr.jpg)

cast.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Add a main function that declares and initializes variables of various data types

**int main()**

**{**

**float num = 5.75 ;**

**char letter = ‘A’ ;**

**int zee = 90 ;**

**int x = 7 , y = 5 ;**

**double decimal = 0.12345678 ;**

**}**

![image](images/3r.jpg)Next, insert statements to output the cast equivalents of each variable value

**printf( “Float cast to int: %d \n” , (int)num ) ;**

**printf( “Char cast to int: %d \n” , (int)letter ) ;**

**printf( “Int cast to char: %c \n” , (char)zee ) ;**

**printf( “Float arithmetic: %f \n” , (float)x / (float)y ) ;**

**printf( “Double cast to float: %f \n” , (float)decimal ) ;**

![image](images/4r.jpg)At the end of the function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/5r.jpg)Save the program file, then compile and execute the program to see the resulting equivalent from each cast

![image](images/pga33_1.jpg)

![image](images/forget.jpg)

Values cast from a **float** to an **int** get truncated but those cast from a **double** to a **float** get rounded.

**Creating array variables**

An array variable can store multiple items of data, unlike a regular variable that can only store a single item of data.

![image](images/box1.jpg)

The items of data are stored sequentially in array “elements” that are numbered starting at zero. So, the first array value is stored in array element zero; the second array value is stored in array element one; and so on.

An array variable is declared in a C program in the same way as regular variables but additionally, the size of the array (its number of elements) should be specified in the declaration. This is stated within square brackets following the array name, with this syntax:

***data-type array-name [ number-of-elements ] ;***

Optionally, an array can be initialized when it is declared by assigning values to each element as a comma-separated list enclosed by curly brackets (braces). For example, an array of three integers can be created and initialized with **int arr[3] = { 1,2,3 } ;**.

An array element value can be referenced using the array name followed by square brackets containing the element number. For example, **arr[0]** references the value in the first element.

It is acceptable in an array declaration to omit the number between the square brackets if the elements are being initialized in the declaration – the size will be automatically adjusted to accommodate the number of values being assigned to the array.

One of the most significant uses of arrays in C programming concerns their ability to store strings of text. Each element in an array of the **char** data type can store a single character. Adding a special **\0** null character escape sequence in the array’s final element promotes the array to string status. For example, a string can be created and initialized with **char str[4]={ ‘C’, ’a’, ‘t’, ’\0’ } ;**.

A character array promoted to string status allows the entire string to be referenced using just the array name, and can be displayed with the **print()** function and the **%s** format specifier – for example, to display a string status array **str** with **printf( “%s”, str );**.

![image](images/snake.jpg)

Array elements start numbering at zero, not one.

![image](images/forget.jpg)

When creating an array to hold a string, remember to allow space for an element at the end to contain the **\0** null character.

![image](images/commoncr.jpg)

array.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Add a main function that declares an integer array of three elements

**int main()**

**{**

**int arr[3] ;**

**}**

![image](images/3r.jpg)Next, insert statements to initialize the integer array elements by individually assigning values to each element

**arr[0] = 100 ;**

**arr[1] = 200 ;**

**arr[2] = 300 ;**

![image](images/4r.jpg)Now, insert a statement to create and initialize a character array to hold a string of text

**char str[10] = {‘C’,’ ‘,’P’,’r’,’o’,’g’,’r’,’a’,’m’,’\0’ } ;**

![image](images/5r.jpg)Insert statements to output all element values of the integer array and the string from the character array

**printf( “1st element value: %d \n” , arr[0] ) ;**

**printf( “2nd element value: %d \n” , arr[1] ) ;**

**printf( “3rd element value: %d \n” , arr[2] ) ;**

**printf( “String: %s \n” , str ) ;**

![image](images/6r.jpg)At the end of the function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7r.jpg)Save the program file, then compile and execute the program to see the values stored in the array variables

![image](images/pga35_1.jpg)

![image](images/hot.jpg)

The creation of an array allocates memory for each element according to the data type – one byte per element for **char** arrays. So, arrays cannot be dynamically resized.

**Describing dimensions**

The numbering of array elements is more correctly known as the “array index” and, because element numbering starts at zero, is sometimes referred to as a “zero-based index”. An array created with a single index is a one-dimensional array in which the elements appear in a single row:

|  Element content... |  A |  B |  C |  D |  E |
| Index numbers... | [0] | [1] | [2] | [3] | [4] |

Arrays can also have multiple indices – to represent multiple dimensions. An array created with two indices is a two-dimensional array in which the elements appear in multiple rows:

| First index [0] | [0] | A | B | C | D | E |
|  | [1] | F | G | H | I | J |
|  Second index |  |  [0] |  [1] |  [2] |  [3] |  [4] |

With multi-dimensional arrays the value contained in each element is referenced by stating the number of each index. For example, with the two-dimensional array above, the element at [1] [2] contains the letter H.

Two-dimensional arrays are useful to store grid-based information, such as XY coordinates. Creating a three-dimensional array, with three indices, would allow XYZ coordinates to be stored:

![image](images/pga36_1.jpg)

Additional indices allow the creation of arrays with many dimensions, but in reality multi-dimensional arrays of more than three indices are uncommon as they are difficult to envision.

![image](images/snake.jpg)

Multi-dimensional arrays with more than two indices can produce hard-to-read source code and may lead to errors.

![image](images/commoncr.jpg)

matrix.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Add a main function that declares and initializes a two-dimensional integer array

**int main()**

**{**

**int matrix[2][3] = { { ‘A’, ’B’, ’C’ } , { 1, 2, 3 } } ;**

**}**

![image](images/3r.jpg)Next, insert statements to display the content of all elements in the first index

**printf( “Element [0][0] contains %c \n” , matrix[0][0] ) ;**

**printf( “Element [0][1] contains %c \n” , matrix[0][1] ) ;**

**printf( “Element [0][2] contains %c \n” , matrix[0][2] ) ;**

![image](images/4r.jpg)Now, insert statements to display the content of all elements in the second index

**printf( “Element [1][0] contains %d \n” , matrix[1][0] ) ;**

**printf( “Element [1][1] contains %d \n” , matrix[1][1] ) ;**

**printf( “Element [1][2] contains %d \n” , matrix[1][2] ) ;**

![image](images/5r.jpg)At the end of the function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/6r.jpg)Save the program file, then compile and execute the program to see all the values stored within the two-dimensional array elements

![image](images/pga37_1.jpg)

![image](images/hot.jpg)

Notice here how implicit casting stores the letters’ ASCII code values in the integer array but the **%c** format specifier displays them as letters again.

**Summary**

![image](images/pgb168_1.jpg)

•A variable is a container in a C program in which a data value can be stored in computer memory.

•Variable names must adhere to the C naming conventions.

•The four basic data types in C are **char**, **int**, **float**, and **double**.

•Format specifiers **%d**, **%f**, **%c**, **%s**, and **%p** can be used with the **printf()** function to display variable values of different types.

•User input can be assigned to variables by the **scanf()** function.

•The permissible range of **int** variables can be explicitly qualified using the **short** and **long** keywords.

•Variables that will never hold negative values may be qualified as **unsigned** to extend their positive range.

•The number of memory bytes reserved by any variable can be revealed using the **sizeof** operator.

•Variable scope describes the extent of accessibility to a variable, and may be local or global.

•The **extern** keyword specifies an externally defined variable and the **static** keyword limits accessibility to the same source file.

•Performance of heavily used variables may be improved using the **register** keyword to place the variable in a machine register.

•Variables unsuitable for registers can be marked as **volatile**.

•The compiler may implicitly change data types where that is logical, or they may be changed explicitly by casting.

•Array variables store multiple items of data within individual elements that are sequentially numbered – starting at zero.

•Values in array elements are referenced by the array variable name followed by their element number within square brackets.

•Array variables can have multiple indices to create. multi-dimensional arrays.

3

**Setting constant values**

***This chapter demonstrates how to create and utilize constant values and types within C programs.***

[**Declaring program constants**](#chapter03.xhtml_sec17)

[**Enumerating constant values**](#chapter03.xhtml_sec18)

[**Creating a constant type**](#chapter03.xhtml_sec19)

[**Defining constants**](#chapter03.xhtml_sec20)

[**Debugging definitions**](#chapter03.xhtml_sec21)

[**Summary**](#chapter03.xhtml_sec22)

**Declaring program constants**

Where a program is required to use a fixed constant data value that will never change, it should be declared in the same way as a variable, but including the const keyword in the declaration. For example, a constant representing the unchanging integer value of one million can be declared and initialized, like this:

const int MILLION = 1000000 ;

![image](images/pga40_1.jpg)

Constant declarations must always initialize the constant object with the data value they will contain. The program can never change the value of a constant from its initial value. This safeguards the constant value from accidental alteration, as the compiler will report an error if the program attempts to subsequently alter the initial value.

Constant names are subject to the same naming conventions as variable names (described [here](#chapter02.xhtml_sec7)) but it is traditional to use uppercase characters for constant names – to easily distinguish them from variable names when reading the source code.

The const keyword can also be used in an array declaration if all its initial element values are never to be changed by the program.

![image](images/commoncg.jpg)

constant.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add a main function that declares a constant value approximating the mathematical value of Pi

**int main()**

**{**

**const float PI = 3.141593 ;**

**}**

![image](images/3g.jpg)Next, in the main function block, insert statements declaring four variables

**float diameter ;**

**float radius ;**

**float circ ;**

**float area ;**

![image](images/4g.jpg)Now, insert statements requesting user input to be assigned to a variable

**printf( “Enter the diameter of a circle in millimeters: “ ) ;**

**scanf( “%f” , &diameter ) ;**

![image](images/5g.jpg)Next, add statements to calculate values for the other three variables using the constant value and user input

**circ = PI * diameter ;**

**radius = diameter / 2 ;**

**area = PI * ( radius * radius ) ;**

![image](images/6g.jpg)Now, insert statements to output the calculated values formatted to two decimal places

**printf( “\n\tCircumference is %.2f mm” , circ ) ;**

**printf( “\n\tAnd the area is %.2f sq.mm\n” , area ) ;**

![image](images/7g.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/8g.jpg)Save the program file, then compile and execute the program, entering data when requested, to see the calculated output

![image](images/pg47_1.jpg)

![image](images/hot.jpg)

Here the ***** asterisk character is the arithmetical multiplication operator, and the **/** forward slash character is the division operator. Arithmetical operators are demonstrated fully in the next chapter.

![image](images/forget.jpg)

Remember that the **&** addressof operator must precede the variable name in **scanf()** to assign input to the variable.

**Enumerating constant values**

The enum keyword provides a handy way to create a sequence of integer constants in a concise manner. Optionally, the declaration can include a name for the sequence after the enum keyword. The constant names follow as a comma-separated list within braces.

Each of the constants will, by default, have a value one greater than that of the constant it follows in the list. Unless specified, the first constant will have a value of zero; the next a value of 1; and so on.

For example, named weekday constants can be given a sequence of integer values starting at zero with enum{MON,TUE.WED.THU,FRI}; – in this case, the constant WED has an integer value of 2.

The constants can be assigned any individual integer value in the declaration but the next constant in the list will always increment the preceding value by one, unless it too is assigned a value. For example, to begin the sequence at 1 instead of zero, assign 1 to the first constant with enum{MON=1,TUE,WED,THU,FRI}; – in this case, the constant WED has an integer value of 3.

The list of enumerated constants is also known as an “enumeration set” and may contain duplicate constant values. For example, the value zero could be assigned to constants named NIL and NONE.

In the following example, the enumeration set represents the points value of balls in the game of snooker, and includes an optional name, which appears in uppercase as it too is constant.

![image](images/commoncg.jpg)

enum.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add a main function that declares and initializes an enumerated set of constants starting at 1

**int main()**

**{**

**enum SNOOKER**

**{ RED=1,YELLOW, GREEN, BROWN, BLUE, PINK, BLACK } ;**

**}**

![image](images/3g.jpg)Next, in the main function block, declare an integer variable to store the sum of some constant values

**int total ;**

![image](images/4g.jpg)Now, insert statements to display the value of some of the enumerated constants

**printf( “\nI potted a red worth %d\n” , RED ) ;**

**printf( “Then a black worth %d\n” , BLACK ) ;**

**printf( “Followed by another red worth %d\n” , RED ) ;**

**printf( “And finally a blue worth %d\n” , BLUE ) ;**

![image](images/5g.jpg)Next, add a statement to calculate the sum total of the constant values displayed by the previous step

**total = RED + BLACK + RED + BLUE ;**

![image](images/6g.jpg)Now, add a statement to output the calculated total of the displayed values

**printf( “\nAltogether I scored %d\n” , total ) ;**

![image](images/7g.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/8g.jpg)Save the program file, then compile and execute the program to see the enumerated constant values and the calculated total in the output

![image](images/pga43_1.jpg)

![image](images/snake.jpg)

Assigning a value of 1 to the **BLUE** constant in this example restarts the incrementing process – making the **PINK** constant 2 and the **BLACK** constant 3.

![image](images/forget.jpg)

The enum type name (in this case, **SNOOKER**) is optional – so may be omitted in this example.

**Creating a constant type**

Once an enumerated sequence is declared it can be considered to be like a new data type in its own right, with properties of its specified constant names and their associated values.

Variables of this enum data type can be declared in the same way that variables are declared of other data types – using this syntax:

*data-type variable-name ;*

The example [here](#chapter03.xhtml_sec18) created an enumerated sequence named SNOOKER, which can be regarded as a data type of enum SNOOKER. So a variable named “pair” of that data type can be created with the declaration enum SNOOKER pair ; and can store values of the enumeration set defined by that type.

To explicitly assign an integer value to a variable of an enumerated data type, the C standard recommends that a cast be used to convert the int data type to the enum data type, like this:

pair = ( enum SNOOKER ) 7 ;

In practice this is not needed though, as enumerated values are always integers so are equivalent to the int data type.

An enum declaration can optionally also create a variable by specifying a variable name after the final brace. For example, the declaration enum BOOLEAN { FALSE , TRUE } flag ; defines an enum data type and creates a variable named “flag” of that type.

Custom data types can be defined using the typedef keyword and this syntax:

typedef *definition type-name ;*

Declaration of custom data types can help make the program code more concise. For example, where a program uses a number of unsigned short int variables it would be useful to first create a custom data type with those modifiers, using this declaration:

typedef unsigned short int USINT ;

Each unsigned short int variable declaration can then simply use the custom data type name USINT in place of unsigned short int.

![image](images/hot.jpg)

Although not essential, using the recommended cast to explicitly assign values to an enumerated type variable serves as a reminder of its type.

![image](images/commoncg.jpg)

constype.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add a main function that declares and initializes an enumerated set of constants starting at 1

**int main()**

**{**

**enum SNOOKER**

**{ RED=1,YELLOW, GREEN, BROWN, BLUE, PINK, BLACK } ;**

**}**

![image](images/3g.jpg)Next, in the main function block, declare and initialize a variable of the defined enum type, then display its value

**enum SNOOKER pair = RED + BLACK ;**

**printf( “Pair value: %d \n” , pair ) ;**

![image](images/4g.jpg)Now, add a statement to create a custom data type

**typedef unsigned short int USINT ;**

![image](images/5g.jpg)Then, declare and initialize a variable of the custom data type and display its value

**USINT num = 16 ;**

**printf( “Unsigned short int value: %d \n” , num ) ;**

![image](images/6g.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7g.jpg)Save the program file, then compile and execute the program to see the value assigned to the enumerated type variable and to the custom data type

![image](images/pga45_1.jpg)

![image](images/forget.jpg)

Custom data types must be defined in the program before variables of that type can be created.

**Defining constants**

The preprocessor #define directive can be used to specify constant text values that can be used in a program with this syntax:

**#define *CONSTANT-NAME “text-string”***

Like the #include directive, these should appear at the very start of the program code. Any occurrences of the specified constant name in the program code will be substituted for the associated text string by the preprocessor before compilation.

A conditional preprocessor #ifdef directive can also be used to evaluate whether a definition currently exists. Depending on the result of the evaluation it may be followed by a #define directive to specify a constant text value. This preprocessor routine is known as a “macro” and each macro must end with an #endif directive.

Usefully, a preprocessor macro can examine compiler-defined constants to determine the host operating system. These will vary from machine to machine, but on the Windows platform there will typically be a constant named _WIN32, and on the Linux platform there will typically be a linux constant. An #ifdef preprocessor directive can apply an appropriate text string to identify the host platform.

![image](images/commoncg.jpg)

define.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add three further preprocessor directives that specify text strings for substitution in the source code

**#define LINE “_________________________”**

**#define TITLE “C Programming in easy steps”**

**#define AUTHOR “Mike McGrath”**

![image](images/3g.jpg)Next, add a conditional macro that specifies a text string to identify the Windows host platform

**#ifdef _WIN32**

**#define SYSTEM “Windows”**

**#endif**

![image](images/4g.jpg)Now, add a conditional macro that specifies a text string to identify the Linux host platform

**#ifdef linux**

**#define SYSTEM “Linux”**

**#endif**

![image](images/5g.jpg)Next, add a main function that outputs the text string values substituted by the preprocessor

**int main()**

**{**

**printf( “\n \t %s \n \t %s \n” , LINE , TITLE ) ;**

**printf( “\t by %s \n \t %s \n” , AUTHOR , LINE ) ;**

**printf( “\n Operating System: %s \n” , SYSTEM ) ;**

**}**

![image](images/6g.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7g.jpg)Save the program file, then compile and execute the program to see the string constants output

![image](images/pga47_1.jpg)

![image](images/pga47_2.jpg)

![image](images/forget.jpg)

The LINE string in this example is just a series of underscore characters.

![image](images/hot.jpg)

Try issuing the command cpp -dM define.c to see all the defined constants.

**Debugging definitions**

Alternatives can be offered with #if, #else and #elif (else if) preprocessor directives. These allow conditional branching to execute sections of code according to the result of an evaluation.

![image](images/pga48_1.jpg)

A constant initially defined by a preprocessor #define directive can be subsequently undefined with an #undef directive. An evaluation may also be made to consider whether a constant is undefined with an #ifndef (if not defined) preprocessor directive.

All evaluations can be made in a function block, mixed with regular C statements, and may be nested one within another. Macros of this kind are particularly useful for debugging source code, as whole sections of the code can be easily hidden or revealed, simply by changing the status of a DEBUG macro.

![image](images/commoncg.jpg)

debug.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add a further preprocessor directive to establish a macro

**#define DEBUG 1**

![image](images/3g.jpg)Next, add a main function containing preprocessor directives to evaluate and report the macro status

**#if DEBUG == 1**

**printf( “Debug status is 1 \n” );**

**#elif DEBUG == 2**

**printf( “Debug status is 2 \n” ) ;**

**#else**

**#ifdef DEBUG**

**printf( “Debug is defined! \n” ) ;**

**#endif**

**#ifndef DEBUG**

**printf( “Debug is not defined! \n” ) ;**

**#endif**

**#endif**

![image](images/4g.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/hot.jpg)

The **==** equality operator used in this example means “is equal to”.

![image](images/5g.jpg)Save the program file, then compile and execute the program to see the macro status reported

![image](images/pga49_1.jpg)

![image](images/6g.jpg)Modify the macro value then save, recompile, and execute the program again to see the new macro status reported

**#define DEBUG 2**

![image](images/pga49_2.jpg)

![image](images/7g.jpg)Modify the macro value once more then save, recompile, and execute the program again to see the change

**#define DEBUG 3**

![image](images/pga49_3.jpg)

![image](images/8g.jpg)Insert another preprocessor directive at the start of the function block then save, recompile, and execute the program again to see the macro status reported

**#undef DEBUG**

![image](images/pga49_4.jpg)

![image](images/forget.jpg)

Every preprocessor conditional test must end with an #endif directive.

**Summary**

![image](images/pgc46_1.jpg)

•A fixed data value that will never change should be stored as a constant, declared with the const keyword.

•When declaring a constant the declaration must always initialize the constant with its fixed data value.

•The enum keyword creates a sequentially numbered series of integer constants that, by default, start at zero.

•Any constant in an enumerated series can be explicitly assigned an integer value, which subsequent constants in that series will increment.

•An enumerated series of constants can be regarded as a new data type, from which variables can be created to store values of the enumeration set defined by that type.

•A custom data type can be defined using the typedef keyword, then variables of that type can be created using the same syntax as that used to declare regular variables.

•A preprocessor #define directive can be used to specify a constant text value to be substituted before compilation.

•The conditional preprocessor #ifdef directive evaluates whether a definition currently exists.

•A macro is a preprocessor routine that must end with an #endif directive.

•Compiler-defined constants, such as _WIN32 and linux, can determine the host operating system.

•Macro alternatives can be offered with #if, #else, and #elif preprocessor directives.

•Constant macro definitions can be undefined with the #undef directive, and evaluated as undefined with the #ifndef directive.

•Macros can be useful to aid debugging of source code by easily hiding or revealing sections of code.

4

**Performing operations**

***This chapter demonstrates how the C operators are used to manipulate data within a C program.***

[**Doing arithmetic**](#chapter04.xhtml_sec23)

[**Assigning values**](#chapter04.xhtml_sec24)

[**Comparing values**](#chapter04.xhtml_sec25)

[**Assessing logic**](#chapter04.xhtml_sec26)

[**Examining conditions**](#chapter04.xhtml_sec27)

[**Measuring size**](#chapter04.xhtml_sec28)

[**Comparing bit values**](#chapter04.xhtml_sec29)

[**Flagging bits**](#chapter04.xhtml_sec30)

[**Understanding precedence**](#chapter04.xhtml_sec31)

[**Summary**](#chapter04.xhtml_sec32)

**Doing arithmetic**

![image](images/pga52_1.jpg)

The arithmetic operators commonly used in C programs are listed in the table below, together with the operation they perform:

| **Operator** | **Operation** |
| **+** | Addition |
| **-** | Subtraction |
| ***** | Multiplication |
| **/** | Division |
| **%** | Modulus |
| **++** | Increment |
| **--** | Decrement |

Operators for addition, subtraction, multiplication, and division act as you would expect. Care must be taken, however, to bracket expressions for clarity where more than one operator is used:

a = b * c - d % e / f ;                     /* This is unclear. */

a = ( b * c ) - ( ( d % e ) / f ) ;       /* This is clearer. */

The % modulus operator divides the first given number by the second given number and returns the remainder of the operation. This is useful to determine if a number has an odd or even value.

The ++ increment operator and -- decrement operator alter the given number by one and return the resulting new value. These are most often used to count iterations in a loop. The increment operator increases the value by one and the decrement operator decreases the value by one.

The increment and decrement operators can be placed before or after an operand to different effect. If placed before the operand (prefix) its value is changed immediately; if placed after the operand (postfix) its value is first noted then changed later.

![image](images/hot.jpg)

The numbers used along with operators to form expressions are known as “operands” – in the expression **2 + 3** the numbers **2** and **3** are the operands.

![image](images/commoncp.jpg)

arithmetic.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that declares and initializes several integer variables

int main()

{

int a = 4 , b = 8 , c = 1 , d = 1 ;

}

![image](images/3p.jpg)Next, in the main function block, output the result of arithmetical operations performed on the variable values

printf( “Addition: %d \n” , a + b ) ;

printf( “Subtraction: %d \n” , b - a ) ;

printf( “Multiplication: %d \n” , a * b ) ;

printf( “Division: %d \n” , b / a ) ;

printf( “Modulus: %d \n” , a % b ) ;

![image](images/4p.jpg)Now, in the main function block, output the result of both postfix and prefix increment operations

printf( “Postfix increment: %d \n” , c++ ) ;

printf( “Postfix now: %d \n” , c ) ;

printf( “Prefix increment: %d \n” , ++d ) ;

printf( “Prefix now: %d \n” , d ) ;

![image](images/5p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/6p.jpg)Save the program file, then compile and execute the program to see the results of the arithmetical operations

![image](images/pga53_1.jpg)

![image](images/snake.jpg)

Notice that the variable value is immediately increased only with the prefix increment operator – with the postfix operator it is incremented the next time it is referenced.

**Assigning values**

The operators that are used in C programs to assign values are listed in the table below. All except the simple = assign operator are a shorthand form of a longer expression, so each equivalent is given for clarity.

![image](images/pga54_1.jpg)

| **Operator** | **Example** | **Equivalent** |
| **=** | **a = b** | **a = b** |
| **+=** | **a += b** | **a = ( a + b )** |
| **-=** | **a -= b** | **a = ( a - b )** |
| ***=** | **a *= b** | **a = ( a * b )** |
| **/=** | **a/= b** | **a = ( a / b )** |
| **%=** | **a %= b** | **a = ( a % b )** |

It is important to regard the = operator to mean “assign” rather than “equals” to avoid confusion with the == equality operator.

In the example above, the variable named a is assigned the value that is contained in the variable named b – so that becomes the new value stored in the a variable.

The += operator is useful to add a value onto an existing value that is stored in the a variable. In the table example, the += operator first adds the value stored in the variable a to the value stored in the variable b. It then assigns the result to become the new value stored in the a variable.

All the other operators in the table work in the same way by making the arithmetical operation between the two values first, then assigning the result to the first variable to become its new stored value.

With the %= operator, the first operand a is divided by the second operand b, then the remainder of the operation is assigned to the a variable.

![image](images/snake.jpg)

The **==** equality operator compares operand values. This is described [here](#chapter04.xhtml_sec25).

![image](images/commoncp.jpg)

assign.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that declares two integer variables

int main()

{

int a , b ;

}

![image](images/3p.jpg)Next, in the main function block, output the result of assignment operations performed on the variables

printf( “Assigned: \n” ) ;

printf( “\tVariable a = %d \n” , a = 8 ) ;

printf( “\tVariable b = %d \n” , b = 4 ) ;

printf( “Added & assigned: \n” ) ;

printf( “\tVariable a+=b (8+=4) a= %d \n”, a += b ) ;

printf( “Subtracted & assigned: \n” ) ;

printf( “\tVariable a-=b (12-=4) a= %d \n”, a -= b ) ;

printf( “Multiplied & assigned: \n” ) ;

printf( “\tVariable a*=b (8*=4) a= %d \n”, a *= b ) ;

printf( “Divided & assigned: \n” ) ;

printf( “\tVariable a/=b (32/=4) a= %d \n”, a /= b ) ;

printf( “Modulated & assigned: \n” ) ;

printf( “\tVariable a%%=b (8%%=4) a= %d \n”, a %= b ) ;

![image](images/4p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/5p.jpg)Save the program file, then compile and execute the program to see the results of the assignment operations

![image](images/pga55_1.jpg)

![image](images/hot.jpg)

Notice that **%%** must be used in order to display the **%** character with the **printf()** function.

**Comparing values**

![image](images/pga56_1.jpg)

The operators that are commonly used in C programming to compare two numerical values are listed in the table below:

| **Operator** | **Comparative Test** |
| **==** | Equality |
| **!=** | Inequality |
| **>** | Greater than |
| **<** | Less than |
| **>=** | Greater than or equal to |
| **<=** | Less than or equal to |

The == equality operator compares two operands and will return 1 (true) if both are equal in value, otherwise it will return 0 (false). If both are the same number they are equal, or if both are characters their ASCII code value is compared numerically.

Conversely, the != inequality operator returns 1 (true) if the two operands are not equal, using the same rules as the == equality operator; otherwise it returns 0 (false).

Equality and inequality operators are useful in testing the state of two variables to perform conditional branching in a program.

The > “greater than” operator compares two operands and will return 1 (true) if the first is greater in value than the second, or it will return 0 (false) if it is equal or less in value. The > “greater than” operator is frequently used to test the value of a countdown value in a loop.

The < “less than” operator makes the same comparison but returns 1 (true) if the first operand is less in value than the second, otherwise it returns 0 (false).

Adding the = operator after a > “greater than” or < “less than” operator makes it also return 1 (true) when the two operands are exactly equal in value.

![image](images/hot.jpg)

Further information on ASCII code values can be found in the Reference section [here](#chapter11.xhtml_sec78).

![image](images/commoncp.jpg)

comparison.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that declares and initializes three integer variables and two character variables

int main()

{

int zero = 0 , nil = 0 , one = 1 ;

char upr = ‘A’ , lwr = ‘a’ ;

}

![image](images/3p.jpg)Next, in the main function block, output the result of comparison operations performed on the variables

printf( “Equality (0==0): %d \n” , zero == nil ) ;

printf( “Equality (0==1): %d \n” , zero == one ) ;

printf( “Equality (A==a): %d \n” , upr == lwr ) ;

printf( “Inequality (A!=a): %d \n” , upr != lwr ) ;

printf( “Greater than (1>0): %d \n” , one > nil ) ;

printf( “Less than (1<0): %d \n” , one < nil ) ;

printf( “Greater or equal (0>=0): %d \n” , zero >= nil ) ;

printf( “Less or equal (1<=0): %d \n” , one <= nil ) ;

![image](images/4p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/5p.jpg)Save the program file, then compile and execute the program to see the results of the comparison operations

![image](images/pga57_1.jpg)

![image](images/forget.jpg)

Numerically, **1** represents a true result and **0** represents a false result.

![image](images/hot.jpg)

The ASCII code value for uppercase ‘A’ is 65 and for lowercase ‘a’ it’s 97 – so their comparison here returns **0** (false).

**Assessing logic**

The logical operators most commonly used in C programming are listed in the table below:

![image](images/pga58_1.jpg)

| **Operator** | **Operation** |
| **&&** | Logical AND |
| **&#124;&#124;** | Logical OR |
| **!** | Logical NOT |

The logical operators are used with operands that have the Boolean values of true or false, or an expression that can convert to true or false.

The logical && AND operator will evaluate two operands and return true only if both operands are themselves true. Otherwise, the && AND operator will return false.

This is used in conditional branching, where the direction of a C program is determined by testing two conditions. If both conditions are satisfied, the program will go in a certain direction, otherwise it will take a different direction.

Unlike the && AND operator that needs both operands to be true, the || OR operator will evaluate two operands and return true if either one of the operands is itself true. If neither operand is true then the || OR operator will return false. This is useful in C programming to perform a certain action if either one of two test conditions has been met.

The third logical ! NOT operator is a “unary” operator – that is used before a single operand. It returns the inverse value of the given operand, so if the variable var is a true value then !var would return a false value. The ! NOT operator is useful in C programming to toggle the value of a variable in successive loop iterations with a statement like var = !var. This ensures that on each pass the value is reversed, like flicking a light switch on and off.

In C programming, a zero represents the Boolean false value; and any non-zero value, such as 1, represents the Boolean true value.

![image](images/pga58_2.jpg)

The term “Boolean” refers to a system of logical thought developed by the English mathematician George Boole (1815-1864).

![image](images/commoncp.jpg)

logic.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that declares and initializes two integer variables

int main()

{

int yes = 1 , no = 0 ;

}

![image](images/3p.jpg)Next, in the main function block, output the result of logic operations performed on the variables

printf( “AND (no&&no): %d \n” , no && no ) ;

printf( “AND (yes&&no): %d \n” , yes && no ) ;

printf( “AND (yes&&yes): %d \n” , yes && yes ) ;

printf( “OR (no||no): %d \n” , no || no ) ;

printf( “OR (yes||no): %d \n” , yes || no ) ;

printf( “OR (yes||yes): %d \n” , yes || yes ) ;

printf( “NOT (yes !yes): %d %d\n” , yes , !yes ) ;

printf( “NOT (no !no): %d %d\n” , no , !no ) ;

![image](images/4p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/5p.jpg)Save the program file, then compile and execute the program to see the results of the logic operations

![image](images/pga59_1.jpg)

![image](images/forget.jpg)

Notice that **0 && 0** returns **0** (false) – demonstrating the anecdote “two wrongs don’t make a right”.

**Examining conditions**

Possibly the C programmer’s favorite test operator is the ?: conditional operator, also known as the “ternary” operator. This operator first evaluates an expression for a true or false Boolean value, then executes one of two given statements depending on the result of the evaluation.

![image](images/pga60_1.jpg)

The conditional operator has this syntax:

( *test-expression* ) ? *if-true-do-this* : *if-false-do-this ;*

This operator could, for example, be used to evaluate whether a given number is odd or even by examining if there is any remainder after dividing the number by two, then output an appropriate string, like this:

( 7 % 2 != 0 ) ? printf( “Odd Number” ) : printf( “Even Number” ) ;

In this case, dividing seven by two does not leave a zero remainder – so the expression evaluates as true; therefore the first statement is executed, correctly describing the number as an odd value.

The conditional operator is also useful to ensure correct grammar in output regarding singular and plural items, thus avoiding awkward phrases like “There is 5”. The evaluation can simply be made within the printf() statement to use the appropriate version:

printf( “There %s %d” , ( num == 1 ) ? “is” : “are” , num ) ;

In this case, when it’s true that the num variable has a value of one, the “is” version will be used, otherwise the “are” version will be used.

The conditional operator can also be used to assign an appropriate value to a variable depending on the result of an evaluation. Used in this way its syntax looks like this:

*variable* = ( *test-expression* ) ? *if-true-assign-this* : *if-false-assign-this* ;

This operator could, for example, be used to evaluate whether one given number is greater than another then assign the greater number to a variable, like this:

int num , a = 5 , b = 2 ;

num = ( a > b ) ? a : b ;

In this case, the value of variable **a** is greater than that of variable b, so the num variable is assigned the greater value of 5.

![image](images/snake.jpg)

Although the conditional operator is quick and easy to use it can reduce code readability.

![image](images/commoncp.jpg)

conditional.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that declares and initializes a single integer variable

int main()

{

int num = 7 ;

}

![image](images/3p.jpg)Next, in the main function block, insert a conditional statement to output the variable value’s parity

( num % 2 != 0 ) ?

printf(“%d is odd\n”, num) : printf(“%d is even\n”, num) ;

![image](images/4p.jpg)Now, insert conditional statements to output a phrase using correct grammar for plurals

printf( “There %s “ , ( num == 1 ) ? “is” : ”are” ) ;

printf( “%d %s\n”, num, (num==1) ? ”apple” : ”apples” ) ;

![image](images/5p.jpg)Decrease the variable value then insert conditional statements to output a phrase correct for singularity

num=1;

printf( “There %s “ , (num == 1) ? “is” : ”are” ) ;

printf( “%d %s\n”, num, (num==1) ? ”apple” : ”apples” ) ;

![image](images/6p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/7p.jpg)Save the program file, then compile and execute the program to see the results of the conditional operations

![image](images/pga61_1.jpg)

![image](images/hot.jpg)

The conditional operator is best used for terse statements that offer just two simple alternatives to implement.

**Measuring size**

In C programming, the sizeof operator returns an integer value, which is the number of bytes needed to store the content of its operand in memory.

![image](images/pg68_1.jpg)

Where the operand supplied to the sizeof operator is a data type name, such as int, the operand must be enclosed within parentheses – as with the examples listed earlier [here](#chapter02.xhtml_pggst).

Alternatively, where the supplied operand is a data object name, such as a variable name, the parentheses may optionally be omitted. In practice, many programmers will always enclose the sizeof operator’s operand within parentheses to avoid having to remember this distinction.

The basic storage unit in C is defined by the char data type that stores a single character in a single byte of memory. This means that sizeof( char ) will return 1 (1 byte).

Typically, the int and float data types will each allocate 4 bytes of machine memory, whereas the double data type will typically allocate 8 bytes of machine memory to accommodate its range of possible values. These sizes are not defined by the standards, however, but are implementation-defined so may vary. It is therefore good practice to use the sizeof operator to measure the actual memory allocation rather than assume these typical sizes will be allocated.

The memory space allocated for array variables will simply be the number of bytes allocated for that data type multiplied by the number of elements in that array. So, for example, the expression sizeof( int[3] ) will typically return 12 (3 x 4 bytes).

It is especially important to use the sizeof operator to accurately discover the amount of memory allocated for user-defined structures that have members of different data types, as “padding” is often automatically added. This means that total memory allocation may exceed the sum allocated to each member. It might seem reasonable to expect that a structure comprising member variables int score and char grade will be allocated total memory of 5 bytes (4+1), but the total allocation will typically be 8 bytes. This is because computer systems like to read and write data in “word”-sized chunks of 4 bytes each. So, padding gets added to make the memory allocation a multiple of four.

![image](images/hot.jpg)

Always enclose an operand supplied to the **sizeof** operator within parentheses for code consistency.

![image](images/commoncp.jpg)

size.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that declares and initializes a single integer variable

int main()

{

int num = 1234567890 ;

}

![image](images/3p.jpg)Next, in the main function block, insert statements to reveal the memory allocated to the int data type (in this implementation) by type name and object name

printf( “Size of int data type is %d bytes\n” , sizeof (int) ) ;

printf( “Size of int variable is %d bytes\n” , sizeof (num) ) ;

![image](images/4p.jpg)Now, insert a statement to reveal that an array allocates the same memory for each one of its elements

printf( “Size of an int array is %d bytes\n”, sizeof (int[3]) ) ;

![image](images/5p.jpg)Define a structure comprising one char variable and one int variable then reveal its total memory allocation – including any padding

struct { int score ; char grade ; } result ;

printf(“Size of a structure is %d bytes\n” , sizeof (result) ) ;

![image](images/6p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/7p.jpg)Save the program file, then compile and execute the program to see output from the sizeof operations

![image](images/pga63_1.jpg)

![image](images/forget.jpg)

This example includes code for a **struct** object, which is a list of different variables. Structures are demonstrated in [Chapter 9](#chapter09.xhtml) but a **struct** is included here to demonstrate how the **sizeof** operator can measure its memory size.

**Comparing bit values**

A byte comprises 8 bits that can each contain a 1 or a 0 to store a binary number representing decimal values from 0 to 255\. Each bit contributes a decimal component only when that bit contains a 1. Components are designated right-to-left from the “Least Significant Bit” (LSB) to the “Most Significant Bit” (MSB). The binary number in the bit pattern below represents decimal 50.

| **Bit No.** | **8 MSB** | **7** | **6** | **5** | **4** | **3** | **2** | **1 LSB** |
| **Decimal** | **128** | **64** | **32** | **16** | **8** | **4** | **2** | **1** |
| **Binary** | **0** | **0** | **1** | **1** | **0** | **0** | **1** | **0** |

Although the char data type is the basic 1-byte storage unit in C programming, as described [here](#chapter04.xhtml_sec28), it is possible to manipulate individual parts of a byte using “bitwise” operators.

| **Operator** | **Name** | **Binary Number Operation** |
| **&#124;** | OR | Return a **1** in each bit where either of two compared bits is a **1** Example: **1010 &#124; 0101 = 1111** |
| **&** | AND | Return a **1** in each bit where both of two compared bits is a **1** Example: **1010 & 1100 = 1000** |
| **~** | NOT | Return a **1** in each bit where the bit is not **1**, and return **0** where the bit is **1** Example: **~ 1010 = 0101** |
| **^** | XOR | Return a **1** in each bit where only one of two compared bits is a **1** Example: **1010 ^ 0100 = 1110** |
| **<<** | Shift left | Move each bit that is a **1** a specified number of bits to the left Example: **0010 << 2 = 1000** |
| **>>** | Shift right | Move each bit that is a **1** a specified number of bits to the right Example: **1000 >> 2 = 0010** |

![image](images/forget.jpg)

Many C programmers never use bitwise operators but it is useful to understand what they are and how they may be used.

![image](images/hot.jpg)

Each half of a byte is known as a “nibble” (4 bits). The binary numbers in the examples in the table describe values stored in a nibble.

Unless programming for a device with limited resources there is seldom a need to utilize bitwise operators, but they can be useful. For instance, the XOR (eXclusive OR) operator lets you exchange values between two variables without the need for a third variable.

![image](images/commoncp.jpg)

xor.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that declares and initializes two integer variables, then outputs their initial values

int main()

{

int x = 10 , y = 5 ;

printf( “\nx=%d y=%d\n” , x, y ) ;

}

![image](images/3p.jpg)Next, in the main function block, insert an XOR statement three times to exchange the variable values by binary bit manipulation

x = x ^ y ;     /* 1010 ^ 0101 = 1111 (decimal 15) */

y = x ^ y ;     /* 1111 ^ 0101 = 1010 (decimal 10) */

x = x ^ y ;     /* 1111 ^ 1010 = 0101 (decimal 5) */

![image](images/4p.jpg)Now, insert a statement to output the exchanged values

printf( “\nx=%d y=%d\n” , x, y ) ;

![image](images/5p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/6p.jpg)Save the program file, then compile and execute the program to see the XOR bitwise magic

![image](images/pga65_1.jpg)

![image](images/snake.jpg)

Do not confuse bitwise operators with logical operators. Bitwise operators compare binary numbers whereas logical operators evaluate Boolean values.

**Flagging bits**

By far the most common use of bitwise operators is to manipulate a compact “bit field” containing a set of Boolean “flags”. This is a much more efficient use of memory than storing Boolean flag values in separate variables – a char data type of just 1 byte can hold a bit field of eight flags, one per bit, whereas eight separate char variables would require 8 whole bytes of memory.

![image](images/pga66_1.jpg)

The initial bit flags can be set by assigning a decimal value to the variable whose binary equivalent has a 1 for each bit that is to be turned “on” as a Boolean flag. For example, decimal 8 has a binary equivalent of 1000 (1x8 0x4 0x2 0x1) so turns on the fourth flag, reading from right to left from the least significant bit.

Subsequently, the bit flag values can be reversed using the bitwise NOT ~ operator but care must be taken to mask zeros before the bit flags, otherwise they will each be returned as 1. For example, to reverse a bit field of four flags within the four right bits of a byte, the four left bits must be masked. Decimal 15 is binary 0001111 (0x128 0x64 0x32 0x16 1x8 1x4 1x2 1x1) and can be applied as this mask with the bitwise AND & operator.

The bit flag pattern can also be manipulated by shifting those flags that are turned on by a specified number of bits, using the bitwise Shift left << and Shift right >> operators.

![image](images/commoncp.jpg)

bitflag.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that declares a character variable initialized with a decimal value turning on one bit flag

int main()

{

int flags = 8 ; /* Binary 1000 (1x8 0x4 0x2 0x1) */

}

![image](images/3p.jpg)Next, in the main function block, assign a new value to the variable, to also turn on another flag

flags = flags | 2 ; /* 1000 | 0010 = 1010 (decimal 10) */

![image](images/4p.jpg)Now, insert statements to output all the bit flag settings

printf( “Flag 1: %s\n” , ( (flags & 1) > 0) ? “ON” : “OFF”) ;

printf( “Flag 2: %s\n” , ( (flags & 2) > 0) ? “ON” : “OFF”) ;

printf( “Flag 3: %s\n” , ( (flags & 4) > 0) ? “ON” : “OFF”) ;

printf( “Flag 4: %s\n\n” , ((flags & 8) > 0) ? “ON” : “OFF”) ;

![image](images/5p.jpg)Next, insert statements to mask the first four bits of the byte, then flip all the bit flag settings

char mask = 15 ;          /* Binary 00001111 */

flags = ~flags & mask ; /* ~(1010 & 1111=1010)= 0101 */

![image](images/6p.jpg)Now, insert statements to output the reversed bit flag settings and the decimal value representing this pattern

printf( “Flag 1: %s\n” , ( (flags & 1) > 0) ? “ON” : “OFF”) ;

printf( “Flag 2: %s\n” , ( (flags & 2) > 0) ? “ON” : “OFF”) ;

printf( “Flag 3: %s\n” , ( (flags & 4) > 0) ? “ON” : “OFF”) ;

printf( “Flag 4: %s\n\n” , ((flags & 8) > 0) ? “ON” : “OFF”) ;

printf( “Flags decimal value is %d\n” , flags ) ;

![image](images/7p.jpg)Add a statement to shift the “on” bit flags one bit to the left then output the decimal value of the new pattern

flags = flags << 1 ;       /* 0101 << 1 = 1010\. */

printf( “Flags decimal value is now %d\n” , flags ) ;

![image](images/8p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/9p.jpg)Save the program file, then compile and execute the program to see the bit flag manipulation

![image](images/pga67_1.jpg)

![image](images/hot.jpg)

It’s often convenient to predefine constants to represent each bit flag. For example:
**#define FLAG1 1**
**#define FLAG2 2**
**#define FLAG3 4**
**#define FLAG4 8**

![image](images/forget.jpg)

Larger bit fields with more bit flags can be created using a variable with more memory – an **int** data type of 4 bytes has 32 bits.

**Understanding precedence**

Operator precedence defines the order in which C evaluates expressions. For instance, in the expression a=6+b*3 the order of precedence determines whether the addition or the multiplication is completed first.

![image](images/pg74_1.jpg)

The table below lists operator precedence in decreasing order, where operators on higher rows have precedence over those on lower rows, so their operations get completed first. Operators on the same row have equal precedence but the order of completion is determined by associativity direction. For instance, for “Left to right” associativity the operations on the left get completed first.

| **Operator** | **Associativity** |
| **( )** Function call **[ ]** Array index **->** Struct pointer . Struct member | Left to right |
| **!** NOT **~** Bitwise NOT **++** Increment **--** Decrement **+** Positive sign **sizeof**
**-** Negative sign ***** Pointer **&** Addressof | Right to left |
| ***** Multiply **/** Divide **%** Modulus | Left to right |
| **+** Add **-** Subtract | Left to right |
| **<<** Shift left **>>** Shift right | Left to right |
| **<** Less than **<=** Less than or equal to **>** Greater than **>=** Greater than or equal to | Left to right |
| **==** Equality **!=** Inequality | Left to right |
| **&** Bitwise AND | Left to right |
| **^** Bitwise XOR | Left to right |
| **&#124;** Bitwise OR | Left to right |
| **&&** AND | Left to right |
| **&#124;&#124;** OR | Left to right |
| **?:** Conditional | Right to left |
| **= += -= *= /= %= &= ^= &#124;=** **<<= >>=** Assignment operators | Right to left |
| , Comma | Left to right |

![image](images/hot.jpg)

The ***** multiply operator is on a higher row than the **+** addition operator – so in the expression **a=6+b*3** the multiplication gets completed before the addition operation.

![image](images/forget.jpg)

The **->** and . struct operators are described later in this book but are included here to provide a complete precedence table of all operators.

![image](images/commoncp.jpg)

precedence.c

![image](images/1p.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#include <stdio.h>

![image](images/2p.jpg)Add a main function that outputs an integer from an expression following row-level precedence rules, and another following explicitly determined precedence

int main()

{

printf(“\nDefault precedence ((2*3)+4)-5 : %d\n”, 2*3+4-5 ) ;

printf(“Explicit precedence 2* ((3+4)-5 ): %d\n”, 2*((3+4)-5) ) ;

}

![image](images/3p.jpg)Next, in the main function block, output an integer from following Left-to-right associativity precedence rules then another following explicitly determined precedence

printf( “\nDefault precedence (7*3) %% 2: %d\n” , 7*3%2 );

printf( “Explicit precedence 7* (3%%2) : %d\n” , 7*(3%2) ) ;

![image](images/4p.jpg)Now, output an integer following Right-to-left associativity precedence rules then another from explicit precedence

int num = 9 ;

printf(“\nDefault precedence(8/2)*4:%d\n”, --num/2*sizeof(int));

num = 9 ;

printf(“Explicit precedence 8/(2*4):%d\n”, --num/(2*sizeof(int)));

![image](images/5p.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

return 0 ;

![image](images/6p.jpg)Save the program file, then compile and execute the program to see output following precedence rules

![image](images/pga69_1.jpg)

![image](images/snake.jpg)

In order to output a **%** character the **printf()** statement requires **%%**.

**Summary**

![image](images/pgc168_1.jpg)

•Arithmetical operators can form expressions with two operands for addition +, subtraction -, multiplication *, division /, and modulus %.

•Increment ++ and decrement -- operators modify a single operand by a value of one.

•The assignment = operator can be combined with an arithmetical operator to perform an arithmetical calculation then assign its result.

•Comparison operators can form expressions comparing two operands for equality ==, inequality !=, greater >, < lesser, greater or equal >=, and lesser or equal <= values.

•Logical AND && and OR || operators form expressions evaluating two operands to return a Boolean value of true or false, but the logical NOT ! operator returns the inverse Boolean value of a single operand.

•A conditional ?: operator evaluates a given Boolean expression then returns one of two operands depending on its result.

•The sizeof operator returns the memory byte size of a data type or a data object.

•A single memory byte comprises eight bits, which may each contain a value of one (1) or zero (0).

•Bitwise operators OR |, AND &, NOT ~, and XOR ^ each return a value after comparison of the values within two bits, whereas the Shift left << and Shift right >> operators move the bit values a specified number of bits in their direction.

•The most common use of bitwise operators is to manipulate a compact bit field containing a set of Boolean flags.

•Expressions containing multiple operators will execute their operations in accordance with the default precedence rules unless explicitly determined by the addition of parentheses.

5

**Making statements**

***This chapter demonstrates how statements can evaluate expressions to determine the direction in which a C program should proceed.***

[**Testing expressions**](#chapter05.xhtml_sec33)

[**Branching switches**](#chapter05.xhtml_sec34)

[**Looping for a number**](#chapter05.xhtml_sec35)

[**Looping while true**](#chapter05.xhtml_sec36)

[**Breaking out of loops**](#chapter05.xhtml_sec37)

[**Going to labels**](#chapter05.xhtml_sec38)

[**Summary**](#chapter05.xhtml_sec39)

**Testing expressions**

The if keyword is used to perform the basic conditional test that evaluates a given expression for a Boolean value of true or false. Statements within braces following the evaluation will only be executed when the expression is found to be true. So, the syntax of an if test statement looks like this:

**if ( *test-expression* ) { *statements-to-execute-when-true* }**

![image](images/pga72_1.jpg)

There may be multiple statements to be executed when the test is true, but each statement must be terminated by a semicolon.

Sometimes it may be desirable to evaluate multiple expressions to determine whether following statements should be executed, and this can be achieved in two ways. The logical && AND operator can be used to ensure the statements will only be executed when two expressions are both found to be true, with this syntax:

**if ( ( *test-expression* ) && ( *test-expression* ) ) { *statements-to-execute* }**

Alternatively, multiple if statements can be “nested”, one inside another, to ensure following statements will only be executed when both evaluated expressions are found to be true, like this:

**if ( *test-expression* )**

{

**if ( *test-expression* ) { *statements-to-execute* }**

**}**

When one or more expressions evaluated by an if test statement is found to be false, the statements within its following braces are not executed and the program proceeds to subsequent code.

It is often preferable to extend an if statement by appending an else statement specifying statements within braces to be executed when the expressions evaluated by the if statement are found to be false, with this syntax:

**if ( *test-expression* )**

**{ *statements-to-execute-when-true* }**

**else**

**{ *statements-to-execute-when-false* }**

This is a fundamental programming technique that offers the program two directions in which to proceed, depending on the result of the evaluation, and is known as “conditional branching”.

![image](images/hot.jpg)

When the code to be executed is just a single statement the braces may optionally be omitted.

![image](images/hot.jpg)

Multiple expressions can be evaluated by combining **if** and **else** statements with **if() { ... } else if () { ... }**.

![image](images/commonco.jpg)

ifelse.c

![image](images/1o.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2o.jpg)Add a main function that outputs a statement when a tested expression is found to be true

**int main()**

**{**

**if( 5 > 1 ) { printf( “Yes, 5 is greater than 1\n” ) ; }**

**}**

![image](images/3o.jpg)Next, in the main function block, output a statement when two tested expressions are both found to be true

**if( 5 > 1 )**

**{**

**if( 7 > 2 )**

**{ printf(“5 is greater than 1 and 7 is greater than 2\n”) ; }**

**}**

![image](images/4o.jpg)Now, output a default statement after two tested expressions are both found to be false

**if( 1 > 2 )**

**{ printf( “1st expression is true\n” ) ; }**

**else if( 1 > 3 )**

**{ printf( “2nd expression is true\n” ) ; }**

**else**

**{ printf( “Both expressions are false\n” ) ; }**

![image](images/5o.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/6o.jpg)Save the program file, then compile and execute the program to see output following conditional tests

![image](images/pga73_1.jpg)

![image](images/forget.jpg)

In C, Boolean true is represented numerically as 1 and Boolean false a 0 (zero). So the expression **( 5 > 1 )** is shorthand for **( 5 > 1 == 1 )**.

**Branching switches**

Conditional branching performed by multiple if else statements can often be performed more efficiently by a switch statement when the test expression just evaluates a single condition.

![image](images/pg80_1.jpg)

The switch statement works in an unusual way. It takes a given value as its parameter argument then seeks to match that value from a number of case statements. Code to be executed when a match is found is included in each case statement.

It is important to end each case statement with a break keyword statement so the switch statement will then exit when a match is found without seeking further matches – unless that is the deliberate requirement.

Optionally, the list of case statements can be followed by a single final default statement to specify code to be executed in the event that no matches are found within any of the case statements. So the syntax of a switch statement typically looks like this:

**switch ( *test-value* )**

**{**

***case match-value* : *statements-to-execute-when-matched* ; break** ;

***case match-value* : *statements-to-execute-when-matched* ; break** ;

***case match-value* : *statements-to-execute-when-matched* ; break** ;

**default : *statements-to-execute-when-no-match-found* ;**

**}**

A switch statement can have up to at least 257 case statements according to the ANSI C standard, but no two of its case statements can attempt to match the same value.

Where a number of match-values are to each execute the same statements, only the final case statement need include the statements to be executed and the break statement to exit the switch statement block. For example, to output the same message for match-values of 0, 1, and 2:

**switch ( num )**

**{**

**case 0 :**

**case 1 :**

**case 2 : printf( “Less than 3\n” ) ; break ;**

**case 3 : printf( “Exactly 3\n” ) ; break ;**

**default : printf( “Greater than 3 or less than zero\n” ) ;**

**}**

![image](images/hot.jpg)

It’s always a good idea to include a **default** statement – even if it’s only to output an error message when the **switch** statement fails.

![image](images/forget.jpg)

A **default** statement need not appear at the end of the **switch** block but it is logical to place it there where it needs no **break** statement.

![image](images/commonco.jpg)

switch.c

![image](images/1o.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2o.jpg)Add a main function that declares and initializes one integer variable and one character variable

**int main()**

**{**

**int num = 2 ; char letter = ‘b’ ;**

**}**

![image](images/3o.jpg)Next, in the main function block, insert a switch statement that attempts to match the integer value

**switch( num )**

**{**

**case 1 : printf( “Number is one\n” ) ; break ;**

**case 2 : printf( “Number is two\n” ) ; break ;**

**case 3 : printf( “Number is three\n” ) ; break ;**

**default : printf( “Number is unrecognized\n” ) ;**

**}**

![image](images/4o.jpg)Now, insert a switch statement that attempts to match the character value

**switch( letter )**

**{**

**case ‘a’ : case ‘b’ : case ‘c’ :**

**printf( “Letter is %c\n” , letter ) ; break ;**

**default : printf( “Letter is unrecognized\n” ) ;**

**}**

![image](images/5o.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/6o.jpg)Save the program file, then compile and execute the program to see output from the switch statements

![image](images/pga75_1.jpg)

![image](images/hot.jpg)

In **switch** statements the **case** keyword, match-value, and colon character are regarded as a unique “label”.

**Looping for a number**

A loop is a piece of code in a program that automatically repeats. One complete execution of all statements within a loop is called an “iteration”, or a “pass”. The length of a loop is controlled by a conditional test made within the loop. While the tested expression is found to be true, the loop will continue – until the tested expression is found to be false, at which point the loop ends.

![image](images/pga76_1.jpg)

In C programming there are three types of loop structure – for loops, while loops, and do while loops. Perhaps the most common of these is the for loop, which typically has this syntax:

**for ( *initializer* ; *test-expression* ; *incrementer* ) { *statements* }**

The initializer is used to set a starting value for a counter of the number of iterations made by the loop. An integer variable is used for this purpose and is traditionally named “i”.

Upon each iteration of the loop the test-expression is evaluated and that iteration will only continue while this expression is true. When the test-expression becomes false the loop ends immediately without executing the statements again. With every iteration the counter is incremented then the statements executed.

Loops can be nested, one within another, to allow complete execution of all iterations of an inner nested loop on each iteration of the outer loop.

![image](images/commonco.jpg)

forloop.c

![image](images/1o.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2o.jpg)Add a main function that declares two integer variables to be used later as loop iteration counters

**int main()**

**{**

**int i , j ; }**

**}**

![image](images/3o.jpg)Next, in the main function block, insert a for loop to output the loop counter value on each of three iterations

**for( i = 1 ; i < 4 ; i++ )**

**{**

**printf( “Outer loop iteration %d\n” , i ) ;**

**}**

![image](images/4o.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/5o.jpg)Save the program file, then compile and execute the program to see output from the for loop

![image](images/pga77_1.jpg)

![image](images/6o.jpg)Now, in the loop block, insert a nested loop immediately after the existing output statement, to output the loop counter value on each of three inner loop iterations

**for( j = 1 ; j < 4 ; j++ )**

**{**

**printf( “\tInner loop iteration %d\n” , j ) ;**

**}**

![image](images/7o.jpg)Save the program file, then compile and execute the program once more to see output from both loops

![image](images/pga77_2.jpg)

![image](images/hot.jpg)

A **for** loop counter can also count down – by decrementing the counter value on each iteration using **i--** instead of **i++**.

**Looping while true**

A while loop is an alternative to the for loop described in the previous example. The while loop also requires an initializer, test-expression, and an incrementer, but these are not neatly listed within a single pair of parentheses as they are in a for loop. Instead, the initializer must appear before the start of the loop block, and the test-expression must appear within parentheses after the while keyword, followed by braces containing both an incrementer and the statements to be executed on each iteration.

![image](images/pg84_1.jpg)

***initializer***

**while ( *test-expression* )**

**{ *statements-to-be-executed* ; *incrementer* }**

A do while loop provides a subtle variation on the syntax above by placing the do keyword before the loop block and moving the while statement to after the loop block:

***initializer***

**do { *statements-to-be-executed* ; *incrementer* }**

**while ( *test-expression* ) ;**

Both while loops and do while loops will proceed to make iterations until the test-expression is found to be false, at which point the loop will exit. It is therefore essential that the loop body contains code that will, at some point, change the result of the test-expression evaluation – otherwise an infinite loop is created that will lock the system.

The significant difference between a while loop and a do while loop is that a while loop will not make a single iteration if the test-expression is false on its first evaluation. In contrast, a do while loop will always make at least one iteration because its statements are executed before the evaluation is made. If this is desirable a do while loop is obviously the best choice, otherwise the choice between a for loop and a while loop is largely a matter of personal preference. One rule of thumb suggests that a for loop is best used to perform a specific number of iterations, whereas a while loop is best used to iterate until a certain condition is met.

Loops are the perfect partner to use with arrays as each iteration can effortlessly read or write into successive array elements.

![image](images/snake.jpg)

Notice that a semicolon terminator is required after the **while** statement in the **do while** loop.

![image](images/hot.jpg)

In the event that a program runs an infinite loop, on Windows or Linux systems press the **Ctrl + C** keyboard keys to halt the loop execution.

![image](images/commonco.jpg)

dowhile.c

![image](images/1o.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2o.jpg)Add a main function that declares a counter variable then declares and initializes an array variable of three elements

**int main()**

**{**

**int i , arr[3] = { 10 , 20 , 30 } ;**

**}**

![image](images/3o.jpg)Next, in the main function block, insert a while loop that outputs each element number and the value it contains

**i = 0 ;**

**while( i < 3 )**

**{**

**printf( “While: arr[%d] = %d\n” , i, arr[i] ) ; i++ ;**

**}**

![image](images/4o.jpg)Now, insert a do while loop that also outputs each element number and the value it contains

**i = 0 ;**

**do**

**{**

**printf( “\nDo while: arr[%d] = %d” , i, arr[i] ) ; i++ ;**

**}**

**while( i < 3 ) ;**

![image](images/5o.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/6o.jpg)Save the program file, then compile and execute the program to see apparently identical output from the loops

![image](images/pga79_1.jpg)

![image](images/forget.jpg)

Change the value in this test-expression to zero – so **while (i<0)** in both loops – then recompile and run the program again to see only the first iteration of the **do** **while** loop get executed.

**Breaking out of loops**

The break keyword can be used to prematurely terminate a loop when a specified condition is met. The break statement is situated inside the loop statement block and is preceded by a test-expression. When the test returns true, the loop ends immediately and the program proceeds on to the next task. For example, in a nested inner loop it proceeds to the next iteration of the outer loop.

![image](images/commonco.jpg)

breakcontinue.c

![image](images/1o.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2o.jpg)Add a main function that declares two integer variables to be used later as loop iteration counters

**int main()**

**{**

**int i , j ;**

**}**

![image](images/3o.jpg)Next, in the main function block, insert two nested loops to output their counter values on each of three iterations

**for( i = 1 ; i < 4 ; i++ )**

**{**

**for( j = 1 ; j < 4; j++ )**

**{**

**printf( “Running i=%d j=%d\n”, i, j ) ;**

**}**

**}**

![image](images/4o.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/5o.jpg)Save the program file, then compile and execute the program to see the output from nested loops

![image](images/pga80_1.jpg)

![image](images/6o.jpg)Now, insert this break statement at the very beginning of the inner loop block, to break out of the inner loop – then save, compile, and run the program once more

**if( i == 2 && j == 1 )**

**{**

**printf( “Breaks inner loop when i=%d and j=%d\n” , i, j ) ;**

**break ;**

**}**

![image](images/pga81_1.jpg)

The continue keyword can be used to skip a single iteration of a loop when a specified condition is met. The continue statement is situated inside the loop statement block and is preceded by a test expression. When the test returns true, that single iteration ends.

![image](images/7o.jpg)Insert this continue statement at the beginning of the inner loop block, to skip the first iteration of the inner loop – then save, compile, and run the program again

**if( i == 1 && j == 1 )**

**{**

**printf( “Continues inner loop when i=%d and j=%d\n”, i, j ) ;**

**continue;**

**}**

![image](images/pg87_2.jpg)

![image](images/forget.jpg)

Here the **break** statement halts all three iterations of the inner loop when the outer loop tries to run it the second time.

![image](images/forget.jpg)

Here the **continue** statement just skips the first iteration of the inner loop when the outer loop tries to run it for the first time.

**Going to labels**

The goto keyword supposedly allows the program flow to jump to labels at other points in the program code, much like a hyperlink on a web page. However, in reality this can cause errors; its use is frowned upon; and it is considered bad programming practice.

![image](images/pga82_1.jpg)

The goto keyword jump is a powerful feature that has existed in computer programs for decades, but its power was abused by many early programmers who created programs that jumped around in an unfathomable manner. This produced unreadable program code, so the use of goto became hugely unpopular.

One possible valid use of the goto keyword is to break cleanly from an inner nested loop by jumping to a label just after the end of its outer loop block. This immediately exits both loops so no further iterations of either loop are executed.

![image](images/commonco.jpg)

jump.c

![image](images/1o.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2o.jpg)Add a main function that declares two integer variables to be used later as loop iteration counters

**int main()**

**{**

**int i , j ;**

**}**

![image](images/3o.jpg)Next, in the main function block, insert two nested loops to output their counter values on each of three iterations

**for( i = 1 ; i < 4 ; i++ )**

**{**

**for( j = 1 ; j < 4 ; j++ )**

**{**

**printf( “Running i=%d j=%d\n”, i, j ) ;**

**}**

**}**

![image](images/4o.jpg)Insert a statement as the first line of the inner nested loop, to jump to a label named “end” at a specified counter value

**if( i == 2 && j == 1 ) { goto end ; }**

![image](images/5o.jpg)Now, add the label after the closing brace of the outer loop

**} end:**

![image](images/forget.jpg)

Notice that the **goto** statement specifies the label by name only, but the label itself must have a terminating : colon.

![image](images/6o.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7o.jpg)Save the program file, then compile and execute the program to see the loops exit after the jump

![image](images/pga83_1.jpg)

One alternative, avoiding the goto keyword, might be to check a variable for a Boolean true value (1) on each iteration of each loop:

![image](images/8o.jpg)Add another variable to the existing variable declarations and initialize with a true value of one

**int i , j , flag = 1 ;**

![image](images/9o.jpg)Insert a conditional test of the new variable’s value, both at the start of the outer loop block and at the start of the inner loop block just before the output statement

**if( flag )**

![image](images/10o.jpg)Change the first line of the inner loop to replace the goto statement with one assigning a false value of zero

**if( i == 2 && j == 1 ) { flag = 0 ; }**

![image](images/11o.jpg)Delete the now obsolete end: label after the closing brace then save, compile, and execute the program again to see the same resulting output as before

![image](images/pga83_2.jpg)

![image](images/hot.jpg)

In C, Boolean values are represented numerically as 1 (true) and 0 (false).

![image](images/snake.jpg)

Avoid creating a program executable named “goto.exe” as this would conflict with the internal Windows **GOTO** command.

**Summary**

![image](images/pgb96_1.jpg)

•The if keyword performs a basic conditional test to evaluate a given expression for a Boolean value of true or false.

•The else keyword can be used to provide alternative statements to execute when an if statement evaluates an expression as false.

•Offering a program alternative directions in which to proceed following an evaluation is known as “conditional branching”.

•Conditional branching performed by multiple if else statements can often be performed more efficiently by a switch statement.

•Usually, the case statements within a switch block must each be terminated by a break statement.

•Optionally, a switch block may contain a default statement specifying statements to execute when no match is found.

•The for keyword is followed by parentheses specifying an initializer, test-expression, and incrementer to control a loop.

•The while keyword is followed by parentheses specifying a test expression to determine whether a loop should continue.

•A while loop block must be preceded by an initializer and contain an incrementer within its statement block.

•The do keyword is followed by a statement block after which there must be a while statement terminated by a semicolon.

•A do while loop must be preceded by an initializer and contain an incrementer within its statement block.

•Unlike for loops and while loops, the statements in a do while loop will always be executed at least once.

•The break keyword can be used to terminate a loop, whereas the continue keyword can be used to skip a single iteration.

•Loops may be nested and the goto keyword can be used to exit to a specified label, although its use is not recommended.

6

**Employing functions**

***This chapter demonstrates how statements can be enclosed within a “function” for execution whenever called by the C program.***

[**Declaring functions**](#chapter06.xhtml_sec40)

[**Supplying arguments**](#chapter06.xhtml_sec41)

[**Calling recursively**](#chapter06.xhtml_sec42)

[**Placing functions in headers**](#chapter06.xhtml_sec43)

[**Restricting accessibility**](#chapter06.xhtml_sec44)

[**Summary**](#chapter06.xhtml_sec45)

**Declaring functions**

Previous examples in this book have used the obligatory main() function and standard functions contained in the C header library, such as the printf() function from the stdio.h file. However, most C programs contain a number of custom functions, which can be called as required during the execution of the program.

![image](images/pga86_1.jpg)

A function block simply contains a group of statements that get executed whenever that function is called. Once the function statements have been executed, program flow resumes at the point directly following the function call. This modularity is very useful in C programming to isolate set routines so they can be called upon repeatedly.

To introduce a custom function into a C program it must first be declared, in a similar manner that variables must be declared before they can be used. Function declarations should be added before the main() function block.

Like the main() function, custom functions can return a value. The data type of this return value must be included in the function declaration. If the function is to return no value, its return data type should be declared with the void keyword. The function should be named following the same naming conventions used for variable names.

The function declaration is more correctly known as the “function prototype” and simply informs the compiler about the function. The actual function definition, which includes the statements to be executed, appears after the main() function. The custom function can then be called upon to execute its statements from within the main() function, as required.

If a custom function returns a value this can be assigned to a variable of an appropriate data type, or simply displayed as output using the appropriate format specifier.

![image](images/commoncb.jpg)

first.c

![image](images/1bl.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2bl.jpg)Declare three custom function prototypes

**void first() ;**

**int square5() ;**

**int cube5() ;**

![image](images/hot.jpg)

The function prototype is sometimes referred to as the “function header”.

![image](images/3bl.jpg)Add a main function that declares an integer variable

**int main()**

**{**

**int num ;**

**}**

![image](images/4bl.jpg)After the main function, define the custom functions

**void first()**

**{**

**printf( “Hello from the first function\n” ) ;**

**}**

**int square5()**

**{**

**int square = 5 * 5 ;**

**return square ;**

**}**

**int cube5()**

**{**

**int cube = ( 5 * 5 ) * 5 ;**

**return cube ;**

**}**

![image](images/5bl.jpg)Now, insert calls to the custom functions in the main function block

**first() ;**

**num = square5() ;**

**printf( “5x5= %d\n” , num ) ;**

**printf( “5x5x5= %d\n” , cube5() ) ;**

![image](images/6bl.jpg)At the end of the main function block, return a zero integer value, as required by that function declaration

**return 0 ;**

![image](images/7bl.jpg)Save the program file, then compile and execute the program to see the output from custom functions

![image](images/pga87_1.jpg)

![image](images/snake.jpg)

Notice that each function prototype must end with a semicolon.

![image](images/hot.jpg)

The custom function definitions could technically appear before the **main()** function – but convention is to include prototypes and keep the **main()** function at the beginning of the program code.

**Supplying arguments**

Data can be passed as “arguments” to custom functions, which can then use that data to execute their statements. The function prototype must include the name and data type of each argument.

![image](images/pga86_1.jpg)

It is important to recognize that in C programming, the data is passed “by value” to the variable specified as the function argument. This is different to some other programming languages, such as Pascal, whose arguments are passed “by reference” – where the function operates on the original value, not just a local copy.

The arguments in a function prototype are known as the “formal parameters” of the function. These may be of different data types, and multiple arguments can be specified for a single function if separated by a comma. For example, a function prototype with arguments of each of the four data types could look like this:

**void action( char c , int i , float f , double d ) ;**

The compiler checks that the formal parameters specified in the function prototype match those in the function definition and will report an error if they do not match.

![image](images/commoncb.jpg)

args.c

![image](images/1bl.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2bl.jpg)Declare three custom function prototypes with one argument to be passed to each one when called

**void display( char str[] ) ;**

**int square( int x ) ;**

**int cube( int y ) ;**

![image](images/3bl.jpg)Add a main function that declares an integer variable and a character array variable initialized with a string of text

**int main()**

**{**

**int num ;**

**char msg[50] = “String to be passed to a function” ;**

**}**

![image](images/forget.jpg)

Passing data “by value” assigns the value to a variable in the called function. The function can then manipulate that copy but it does not affect the original data.

![image](images/4bl.jpg)After the main function, define the custom functions

**void display( char str[] )**

**{**

**printf( “%s\n” , str ) ;**

**}**

**int square( int x )**

**{**

**return ( x * x ) ;**

**}**

**int cube( int y )**

**{**

**return ( y * y ) * y ;**

**}**

![image](images/5bl.jpg)Now, in the main function, insert statements calling each of the custom functions and passing argument values

**display( msg ) ;**

**num = square( 4 ) ;**

**printf( “4x4= %d\n” , num ) ;**

**printf( “4x4x4= %d\n” , cube( 4 ) ) ;**

![image](images/6bl.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7bl.jpg)Save the program file, then compile and execute the program to see the output from custom functions using passed argument values

![image](images/pga89_1.jpg)

![image](images/hot.jpg)

The argument names used in the function definition can differ from those used in the function prototype but the argument data types, number, and order must be the same. It is clearer to adopt the same names in both, though.

![image](images/hot.jpg)

A function need not return any value but can still include the **return** keyword without any following value to signify the return of control to the caller.

**Calling recursively**

Statements within custom functions can freely call other custom functions just as readily as they can call standard library functions like printf().

![image](images/pg96_1.jpg)

Additionally, functions can call themselves, and these are known as “recursive functions”. As with loops it is important that recursive functions must modify a tested expression to avoid continuous execution – so the function call ends at some point.

![image](images/commoncb.jpg)

recur.c

![image](images/1bl.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2bl.jpg)Declare a custom function prototype with one argument to be passed when called

**void count_down_from( int num ) ;**

![image](images/3bl.jpg)Add a main function that declares an integer variable

**int main()**

**{**

**int start ;**

**}**

![image](images/4bl.jpg)Next, in the main function block, add a statement requesting the user input an integer value to be assigned to the variable

**printf( “Enter a positive integer to count down from: “ ) ;**

**scanf( “%d” , &start ) ;**

![image](images/5bl.jpg)Now, in the main function block, add a call to the custom function, passing it the value entered by the user

**count_down_from( start ) ;**

![image](images/6bl.jpg)In the main function block, add a statement to output a message when control returns from the custom function

**printf( “Lift Off!\n” ) ;**

![image](images/7bl.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/forget.jpg)

The variable name must be preceded by the & addressof operator in the scanf() function, as described [here](#chapter02.xhtml_sec9).

![image](images/8bl.jpg)After the main function block, begin the custom function definition with a statement to output the argument value passed during the function call

**void count_down_from( int num )**

**{**

**printf( “%d\n” , num ) ;**

**}**

![image](images/9bl.jpg)Next, in the custom function block, decrement the value passed as the argument

**--num ;**

![image](images/10bl.jpg)Now, in the custom function block, add a conditional test to return control to the main function if the decremented value is below zero or pass it as an argument in a recursive call to this function

**if( num < 0 ) return ;**

**else**

**count_down_from( num ) ;**

![image](images/11bl.jpg)Save the program file then compile and execute the program, inputting an integer when requested, to see the output from recursive function calls

![image](images/pga91_1.jpg)

![image](images/pga91_2.jpg)

![image](images/pga91_3.jpg)

![image](images/snake.jpg)

A recursive function can be less efficient than using a loop.

**Placing functions in headers**

The example programs listed throughout the C section of this book are necessarily small due to space considerations but in reality, most C programs will contain significantly more code.

![image](images/pg98_1.jpg)

When developing larger programs, some thought should be given to program structure. Maintaining the entire program code in a single file can become unwieldy as the program grows.

In order to simplify the program structure, a custom header file can be created to contain functions that may be used repeatedly. This should be named with a “.h” file extension, like the standard header files in the C library.

The functions in the custom header file can be made available to the program by adding an #include preprocessor directive at the start of the file containing the main() function. The custom header file name should be enclosed within double quotes in the preprocessor directive though, rather than by the < and > angled brackets that are used to include standard header files.

![image](images/pg98_2.jpg)

utils.h

![image](images/1bl.jpg)Create a custom header file named “utils.h” containing the definition of a single function

**int square( int num )**

**{**

**return ( num * num ) ;**

**}**

![image](images/2bl.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions and the custom header file

**#include <stdio.h>**

**#include “utils.h”**

![image](images/commoncb.jpg)

square.c

![image](images/3bl.jpg)Declare a custom function prototype with no arguments

**void getnum() ;**

![image](images/4bl.jpg)Add a main function to call the other function then return a zero integer as required by the declaration

**int main()**

**{**

**getnum() ;**

**return 0 ;**

**}**

![image](images/5bl.jpg)After the main function block, begin the second function definition by declaring two variables

**void getnum()**

**{**

**int num ;**

**char again ;**

**}**

![image](images/6bl.jpg)Next, in this function definition, add statements to request user input and assign its value to a variable

**printf( “Enter an integer to be squared: “ ) ;**

**scanf( “%d” , &num ) ;**

![image](images/7bl.jpg)Now, output a result by calling the function in the custom header file, passing it the input value as its argument

**printf( “%d squared is %d\n” , num, square(num) ) ;**

![image](images/8bl.jpg)Add a statement requesting further user input and assign its value to a variable

**printf( “Square another number? Y or N: “ ) ;**

**scanf( “%1s” , &again ) ;**

![image](images/9bl.jpg)Finally, add a conditional test to execute this function once more or return control to the main function

**if( ( again == ‘Y’ ) || ( again == ‘y’ ) ) getnum() ;**

**else return ;**

![image](images/10bl.jpg)Save the program file then compile and execute the program, inputting an integer and character when requested, to see the output from the function calls

![image](images/pga93_1.jpg)

![image](images/forget.jpg)

The program file and custom header file must be located in the same directory but are compiled with the usual command – the compiler reads the header file automatically because of the **#include** directive.

![image](images/hot.jpg)

Notice the use of the **%1s** format specifier in this example – to read the next character entered by the user.

**Restricting accessibility**

The static keyword can be used to restrict the accessibility of functions to the file in which they are created, in exactly the same way that static variables have restricted accessibility. This is recommended practice in larger programs that are spread over multiple “.c” files, to safeguard against accidental misuse of functions. For instance, the square() and multiply() functions can’t be directly called from the main() function in this example.

![image](images/pg100_1.jpg)

![image](images/commoncb.jpg)

menu.c

![image](images/1bl.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2bl.jpg)Declare two custom function prototypes

**void menu() ;**

**void action( int option ) ;**

![image](images/3bl.jpg)Add a main function to call the first custom function then return a zero integer as required by the declaration

**int main()**

**{**

**menu() ;**

**return 0 ;**

**}**

![image](images/4bl.jpg)After the main block, define the first custom function to pass a menu option as an argument to another function

**void menu()**

**{**

**int option ;**

**printf( “\n\tWhat would you like to do?” ) ;**

**printf( “\n\t1. Square a number” ) ;**

**printf( “\n\t2. Multiply two numbers” ) ;**

**printf( “\n\t3. Exit\n” ) ;**

**scanf( “%d” , &option ) ;**

**action( option ) ;**

**}**

![image](images/commoncb.jpg)

action.c

![image](images/5bl.jpg)Begin a second program file with a preprocessor to include the standard input/output functions, and declare the custom prototypes once more

**#include <stdio.h>**

**void menu() ;**

**void action( int option ) ;**

![image](images/hot.jpg)

Notice that prototypes are declared here for each file containing calls to those functions – to prevent an “implicit declaration of function” compiler warning.

![image](images/6bl.jpg)Now, define two simple static functions

**static int square( int a ) { return (a * a) ; }**

**static int multiply( int a, int b ){ return a * b ; }**

![image](images/7bl.jpg)Finally, define the function being passed the menu option from the call in the main function to execute an appropriate action – calling upon the static functions created in this file when required

**void action( int option )**

**{**

**int n1 , n2 ;**

**if( option == 1 )**

**{**

**printf( “Enter an integer to be squared: “ ) ;**

**scanf( “%d”, &n1 ) ;**

**printf( “%d x %d = %d \n” , n1 , n1 , square(n1) ) ;**

**menu() ;**

**}**

**else if( option == 2 )**

**{**

**printf( “Enter two integers to multiply “ ) ;**

**printf( “separated by a space: “ ) ;**

**scanf( “%d” , &n1) ; scanf( “%d” , &n2 ) ;**

**printf( “%d x %d = %d\n”, n1, n2, multiply( n1, n2 ) ) ;**

**menu() ;**

**}**

**else return ;**

**}**

![image](images/8bl.jpg)Save both program files, then compile and execute the program to see the output returned from static functions

![image](images/pga95_1.jpg)

![image](images/hot.jpg)

An example demonstrating static variables can be found [here](#chapter02.xhtml_sec11).

![image](images/forget.jpg)

Note that the compiler command specifies both .c source code file names to create a single executable file.

**Summary**

![image](images/pgc84_1.jpg)

•Custom functions are declared by stating that function’s return data type, then its name followed by parentheses, and ending with a semicolon.

•Function declarations are also known as “function prototypes” and should appear before the main function – so the compiler knows of their existence when reading the main() function.

•Function definitions, containing the actual statements to be executed when that function is called, should appear after the main() function block.

•Function declarations may optionally include within their parentheses a comma-separated list of arguments to be passed to the function by its caller, each stating a data type and name.

•Arguments specified in a function definition must match those of its declaration, as these are its formal parameters.

•In C programming, arguments are passed by value – so the function operates on a copy of the original value.

•A function may call itself recursively, but must include a statement to modify a tested expression to exit at some point.

•Custom header files have a “.h” file extension.

•The preprocessor directive to #include a custom header file must specify its file name enclosed within double quotes.

•The static keyword can be used in function declarations and definitions to restrict accessibility by reducing their scope to the file in which they appear.

•Larger programs should declare functions as static unless there is some specific reason they must be visible outside their file.

•Function prototypes are not required for functions outside the file containing the main() function.

7

**Pointing to data**

*This chapter demonstrates how data in a C program can be referenced by pointing to the machine address at which it is stored.*

[**Accessing data via pointers**](#chapter07.xhtml_sec46)

[**Doing pointer arithmetic**](#chapter07.xhtml_sec47)

[**Passing pointers to functions**](#chapter07.xhtml_sec48)

[**Creating arrays of pointers**](#chapter07.xhtml_sec49)

[**Pointing to functions**](#chapter07.xhtml_sec50)

[**Summary**](#chapter07.xhtml_sec51)

**Accessing data via pointers**

Pointers are a very useful part of efficient C programming. They are variables that store the memory address of other variables.

![image](images/pga98_1.jpg)

When a regular variable is declared, memory is allocated, of the size appropriate for its data type, at a vacant memory address. Subsequently, wherever the program finds that variable name, it references the data stored at that memory address. Similarly, wherever the program finds the name of a pointer variable, it references the address it stores. But a pointer variable can be “dereferenced” to reveal the data stored at the address it contains.

Pointer variables are declared in just the same way that other variables are declared but the variable name is prefixed by a “*” . In this case, the * character represents the “dereference operator” and merely denotes that the declared variable is a pointer. The pointer’s data type must match the data type of the variable to which it points.

Once declared, a pointer variable can be assigned the address of another variable using the & addressof operator. The pointer variable should not be prefixed by the * dereference operator in the assignment statement unless the pointer is initialized immediately in the pointer variable declaration itself.

•A pointer variable name, when used alone, references a memory address expressed in hexadecimal.

When the * dereference operator is used in a variable declaration it merely denotes that the variable is a pointer, but prefixing a variable pointer name with the * dereference operator elsewhere in the program references the data stored at the address assigned to that pointer variable.

•A pointer variable name, when prefixed by the * dereference operator after its declaration, references the data stored at the address assigned to that pointer variable.

This means that a program can get the address assigned to a pointer variable just using its name, or it can get the data stored at the address to which it points by prefixing its name with the * dereference operator.

![image](images/hot.jpg)

The ***** dereference operator is alternatively known as the “indirection” operator.

![image](images/snake.jpg)

Be sure to also delete the pointer when deleting the object to which it refers so as not to leave a “dangling pointer” in the program.

![image](images/commoncv.jpg)

point.c

![image](images/1v.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2v.jpg)Add a main function that declares and initializes a regular integer variable and an integer pointer variable

**int main()**

**{**

**int num = 8 ;**

**int *ptr = &num ;**

**}**

![image](images/3v.jpg)Next, in the main function block, output the contents of both variables and the value dereferenced by the pointer

**printf( “Regular variable contains: %d\n” , num ) ;**

**printf( “Pointer variable contains: 0x%p\n” , ptr ) ;**

**printf( “Pointer points to value: %d\n\n” , *ptr ) ;**

![image](images/4v.jpg)Now, in the main function block, assign a new value to the regular variable via the pointer variable, then output the contents and dereferenced value once more

***ptr = 12 ;**

**printf( “Regular variable contains: %d\n” , num ) ;**

**printf( “Pointer variable contains: 0x%p\n” , ptr ) ;**

**printf( “Pointer points to value: %d\n\n” , *ptr ) ;**

![image](images/5v.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/6v.jpg)Save the program file, then compile and execute the program to see variable contents and dereferenced value

![image](images/pga99_1.jpg)

![image](images/forget.jpg)

Declare variables before making other statements – for instance, at the beginning of **main()**.

**Doing pointer arithmetic**

Once a pointer has been created with an assigned memory address it can be reassigned another address, or moved using arithmetic.

![image](images/pg106_1.jpg)

The ++ increment operator and the -- decrement operator will move the pointer forward or back to other memory addresses for that data type – the larger the data type, the bigger the jump.

Even larger jumps can be achieved using the += and -= operators to specify how many places to jump.

Pointer arithmetic is especially useful with arrays because the elements in an array occupy consecutive memory places.

Assigning just the name of an array to a pointer automatically assigns it the memory address of the first element in that array. Incrementing the pointer by one then moves the pointer along to the next element’s address.

![image](images/commoncv.jpg)

movptr.c

![image](images/1v.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2v.jpg)Add a main function that declares an integer variable, then declares and initializes an integer array variable

**int main()**

**{**

**int i ;**

**int nums[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 } ;**

**}**

![image](images/3v.jpg)Next, in the main function block, declare and initialize a pointer variable at the first array element, then output that address and the value dereferenced by that pointer

**int *ptr = nums ;**

**printf( “\nAt Address: %p is Value: %d\n”, ptr , *ptr ) ;**

![image](images/4v.jpg)Now, in the main function block, increment the pointer to move along the array elements one by one

**ptr++ ;**

**printf( “At Address: %p is Value: %d\n”, ptr , *ptr ) ;**

**ptr++ ;**

**printf( “At Address: %p is Value: %d\n”, ptr , *ptr ) ;**

![image](images/snake.jpg)

The ***=** and **/=** operators cannot be used to move a pointer.

![image](images/5v.jpg)Now, jump back two memory places to the address of the first array element

**ptr -= 2 ;**

**printf( “At Address: %p is Value: %d\n\n”, ptr , *ptr ) ;**

![image](images/6v.jpg)Next, add a loop to output each array element index number and the value it contains

**for( i = 0 ; i < 10 ; i++ )**

**{**

**printf( “Element %d Contains Value: %d\n” , i , *ptr ) ;**

**ptr++ ;**

**}**

![image](images/7v.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/8v.jpg)Save the program file, then compile and execute the program to see values output as the pointer moves between array elements

![image](images/pga101_1.jpg)

![image](images/forget.jpg)

The name of an array acts like a pointer to its first element.

**Passing pointers to functions**

In C programs, function arguments pass their data “by value” to a local variable inside the called function. This means that the function is not operating on the original value, but a copy of it.

![image](images/pg108_1.jpg)

Passing a pointer to the original value instead overcomes this to allow the called function to operate on the original value. This technique passes the data “by reference” and is a fundamental advantage provided by pointers.

![image](images/commoncv.jpg)

passptr.c

![image](images/1v.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2v.jpg)Declare two custom function prototypes that each pass a single integer pointer variable to a function

**void twice( int *ptr ) ;**

**void thrice( int *ptr ) ;**

![image](images/3v.jpg)Add a main function that declares and initializes a regular integer variable with a numeric value, and an integer pointer variable with the address of that regular variable

**int main()**

**{**

**int num = 5 ;**

**int *ptr = &num ;**

**}**

![image](images/4v.jpg)Next, in the main function block, output the address stored by the pointer variable and the dereferenced value

**printf( “ptr stores address: %p\n” , ptr ) ;**

**printf( “*ptr dereferences value: %d\n\n” , *ptr ) ;**

![image](images/5v.jpg)Now, output the original value of the regular integer variable

**printf( “The num value is %d\n” , num ) ;**

![image](images/snake.jpg)

Notice that the pointer argument must be included in the function prototype declaration.

![image](images/6v.jpg)After the main function block, define the two custom functions declared by the prototypes that each receive an integer pointer as an argument when called

**void twice( int *number )**

**{**

***number = (*number * 2 ) ;**

**}**

**void thrice( int *number )**

**{**

***number = ( *number * 3 ) ;**

**}**

![image](images/7v.jpg)Back in the main function block, add calls to each custom function, passing the address of the regular variable as a reference, and output the modified original value of the regular variable

**twice( ptr ) ;**

**printf( “The num value is now %d\n”, num ) ;**

**thrice( ptr ) ;**

**printf( “And now the num value is %d\n”, num ) ;**

![image](images/8v.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/9v.jpg)Save the program file, then compile and execute the program to see the values output after passing a reference

![image](images/pga103_1.jpg)

![image](images/forget.jpg)

The ***** character in the definition parentheses denotes that the argument is a pointer, whereas in the statement it dereferences the argument when it appears before the argument name, and represents the multiplication operator in the arithmetic statement.

**Creating arrays of pointers**

A C program can contain arrays of pointers in which each element of an array stores the address of other variables.

![image](images/pg110_1.jpg)

This ability is especially useful for handling strings of characters. A character array that ends with the \0 null character has string status, so can be assigned to a pointer variable. The name of a string char array acts like a pointer to its first element so the & addressof operator is not needed when assigning a string to a pointer variable.

![image](images/commoncv.jpg)

arrptr.c

![image](images/1v.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2v.jpg)Add a main function that declares an integer variable, then declares and initializes an integer array variable

**int main()**

**{**

**int i ;**

**int nums[5] = { 1, 2, 3, 4, 5 } ;**

**}**

![image](images/3v.jpg)Next, in the main function block, declare and initialize integer pointer variables with the address of each element

int *ptr0 = &nums[0] ;

**int *ptr1 = &nums[1] ;**

**int *ptr2 = &nums[2] ;**

**int *ptr3 = &nums[3] ;**

**int *ptr4 = &nums[4] ;**

![image](images/4v.jpg)Now, declare and initialize an integer pointer array, with each element containing one of the integer pointers

**int *ptrs[5] = { ptr0 , ptr1 , ptr2 , ptr3 , ptr4 } ;**

![image](images/5v.jpg)Next, declare and initialize a character array; a pointer to that array; and a character pointer array with a string in each element

**char str[9] = { ‘C’, ’ ‘, ’i’, ’s’, ’ ‘, ’F’, ’u’, ’n’, ’\0’ } ;**

**char *string = str ;**

**char *strings[3] = { “Alpha”, “Bravo”, “Charlie” } ;**

![image](images/hot.jpg)

Notice how the value of the counter **i** is substituted for the element index number on each iteration of the loop.

![image](images/6v.jpg)Add a loop to output the address of each integer pointer array element and their dereferenced values

**for( i = 0 ; i < 5 ; i++ )**

**{**

**printf( “The value at %p is: %d\n” , ptrs[i], *ptrs[i] ) ;**

**}**

![image](images/7v.jpg)Add a statement to output the value stored in the character array

**printf( “\nString is: %s\n\n” , string ) ;**

![image](images/8v.jpg)Add a loop to output the string stored in each character pointer array element

**for( i = 0 ; i < 3 ; i++ )**

**{**

**printf( “String %d is: %s\n” , i , strings[i] ) ;**

**}**

![image](images/9v.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/10v.jpg)Save the program file, then compile and execute the program to see the values output from the pointer array elements

![image](images/pga105_1.jpg)

![image](images/forget.jpg)

The entire string in a **char** array is referenced by the pointer name alone – without the ***** dereference operator.

![image](images/snake.jpg)

To include a space in a string there must actually be a space between the single quotes, like this ‘ ‘ – two single quotes together, such as ‘‘ is seen as an empty element and causes a compiler error.

**Pointing to functions**

Pointers can be created that point to functions, although this ability is used less than pointers that point to data values.

![image](images/pg112_1.jpg)

A pointer to a function is like a pointer to data but must always be enclosed within parentheses when using the * dereference operator to avoid a compiler error. These will also be followed by further parentheses containing any arguments to be passed to the function to which the pointer points.

The function pointer contains the address in memory at which the function to which it points begins. When the function pointer is dereferenced, the function to which it points gets called, and any arguments specified to the function pointer get passed to the called function.

A function pointer can even be passed as an argument to another function – so the receiving function may then call the function to which the function pointer points.

![image](images/commoncv.jpg)

fcnptr.c

![image](images/1v.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2v.jpg)Declare a custom function prototype that has an integer argument, and another that has both a function pointer argument and an integer argument

**int bounce( int a ) ;**

**int caller( int (*function) (int), int b ) ;**

![image](images/3v.jpg)Add a main function that declares an integer variable, then declares and initializes a function pointer variable

**int main()**

**{**

**int num ;**

**int (*fptr)(int) = bounce ;**

**}**

![image](images/4v.jpg)After the main function block, define the first custom function to output a received value and return an integer

**int bounce( int a )**

**{**

**printf( “\nReceived Value: %d\n”, a ) ;**

**return ( ( 3 * a ) + 3 ) ;**

**}**

![image](images/5v.jpg)Next, define the second custom function to call a regular function from a received function pointer, and pass it a received integer value

**int caller( int (*function)(int), int b )**

**{**

**return (*function)(b);**

**}**

![image](images/6v.jpg)Back in the main function block, assign a value to the integer variable by calling the regular function via the function pointer, and output the value it returns

**num = (*fptr)(10);**

**printf( “Returned Value: %d\n” , num ) ;**

![image](images/7v.jpg)Now, assign a new value to the integer variable by passing the function pointer and an integer to another function, which in turn calls the regular function, then output the value it returns

**num = caller( fptr, 5 ) ;**

**printf( “Returned Value: %d\n”, num ) ;**

![image](images/8v.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/9v.jpg)Save the program file, then compile and execute the program to see the values output via function pointers

![image](images/pga107_1.jpg)

![image](images/hot.jpg)

The first argument to the **caller()** function in this example may be a pointer to any function that receives one integer argument and returns an integer value – as specified in the prototype declaration.

![image](images/forget.jpg)

Like other pointers in C programming, a function pointer simply stores a memory address. When a function pointer is dereferenced with ***** the function at that address to which the pointer points gets called.

**Summary**

![image](images/pgb132_1.jpg)

•A pointer is a variable that stores the memory address of another variable expressed in hexadecimal.

•The * dereference operator is used to reference the value contained in the variable to which the pointer points.

•In a pointer variable declaration, the variable name is prefixed by the * character to denote that the variable will be a pointer.

•A pointer variable can be assigned the address of another variable using the & addressof operator.

•Pointer arithmetic allows a pointer to move between consecutive memory places and is especially useful for moving between array elements.

•When an integer variable array name is assigned to a pointer, that pointer automatically stores the memory address of the first element of the array.

•Pointers can be passed as arguments to other functions.

•Passing a pointer as a function argument passes by reference, allowing that function to operate on the original value.

•Each element in an array of pointers can store the address of another variable.

•An array of pointers is especially useful for handling strings of characters.

•When a character string variable array name is assigned to a pointer, that pointer automatically stores the entire string.

•A pointer to a function must always be enclosed within parentheses when using the * dereference operator, to avoid compiler errors.

•Dereferencing a function pointer calls the function to which it points and passes any arguments specified to the pointer.

8

**Manipulating strings**

***This chapter demonstrates how strings of text may be manipulated in C programs.***

[Reading strings](#chapter08.xhtml_sec52)

[Copying strings](#chapter08.xhtml_sec53)

[Joining strings](#chapter08.xhtml_sec54)

[Finding substrings](#chapter08.xhtml_sec55)

[Validating strings](#chapter08.xhtml_sec56)

[Converting strings](#chapter08.xhtml_sec57)

[Summary](#chapter08.xhtml_sec58)

**Reading strings**

![image](images/pga110_1.jpg)

In C programming, a string is an array of characters that has the special \0 null character in its last element. Each character, including punctuation and non-printing characters such as newline, has a unique numerical ASCII code value. This means that characters can be changed arithmetically. For example, where char letter = ‘S’ then letter++ changes the value to ‘T’. ASCII code values for lowercase letters are always 32 higher than those of uppercase letters, so the case of any character can be changed by adding or subtracting a value of 32\. For example, where char letter = ‘M’ then letter+=32 changes the value to ‘m’. As C does not have a dedicated string data type, string variables must be created as character arrays, remembering to add a final element for the \0 null character to promote the array to string constant status. This means that the name of an array then acts like an implied pointer to the entire string of characters. The sizeof operator will return the string’s array length when the string name is supplied as its argument. A string may be assigned to an array or to a pointer of the char data type, like this:

**char arr[6] = { ‘A’, ‘l’, ‘p’, ‘h’, ‘a’ } ;**

| **char *ptr = “Beta” ;** |  |  |
| **printf( “%s” , arr ) ;** | **/* Outputs “Alpha”** | ***/** |
| **printf( “%s” , ptr ) ;** | **/* Outputs “Beta”** | ***/** |

![image](images/hot.jpg)

You can find the standard ASCII character code table [here](#chapter11.xhtml_sec78).

String values can be introduced into a C program by input from the user via the scanf() function described [here](#chapter02.xhtml_sec9). This function works well for single characters or multiple characters forming a single word, but scanf() has a severe limitation in that it stops reading when it encounters a space. This means that the user cannot input a sentence via scanf() as the string gets truncated at the space following the first word. The solution to the scanf() problem is provided by two alternative functions located in the stdio.h header file. The first of these is named fgets() and can be used to read input from the user. This accepts all characters, including spaces, and assigns the string to a character array specified as its first argument. Its second argument must specify the number of characters to read, and its third argument must specify where to read from, such as stdin to read standard input. The fgets() function automatically adds the \0 null character at the end of the string when the user hits the Return key – to ensure the input has string constant status. The companion to fgets() is the puts() function that will output a string specified as its argument and automatically add a newline character at the end.

![image](images/forget.jpg)

In C, character values must be enclosed by single quotes, and strings must be enclosed by double quotes.

![image](images/pg18_1.jpg)

fgetsputs.c

![image](images/1b.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2b.jpg)Add a main function that declares a character array

**int main()**

**{**

**char str[51] ;**

**}**

![image](images/3b.jpg)Next, in the main function block, request input from the user and assign it to the array variable

**printf( “\nEnter up to 50 characters with spaces:\n” ) ;**

**fgets( str , sizeof( str ), stdin ) ;**

![image](images/4b.jpg)Now, in the main function block, output the string stored in the array variable

**printf( “fgets() read: “ ) ;**

**puts( str ) ;**

![image](images/5b.jpg)Repeat the process to see the scanf() limitation

**printf( “\nEnter up to 50 characters with spaces:\n” ) ;**

**scanf( “%s”, str ) ;**

**printf( “scanf() read: %s\n” , str ) ;**

![image](images/6b.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7b.jpg)Save the program file, then compile and execute the program to see the string results

![image](images/pga111_1.jpg)

![image](images/hot.jpg)

If you don’t want a newline added after the output, use **printf()** instead of **puts()**.

**Copying strings**

The standard C libraries include a header file named string.h that contains special string-handling functions. To make these available to a program the string.h header file must be added with an #include directive at the start of the program.

![image](images/pg118_1.jpg)

One of the functions in the string.h file is strlen(), which can be used to find the length of a string supplied as its argument. The strlen() function returns an integer that is the total number of characters in the string – including space “characters”, but excluding the final \0 null character.

The string.h header file also provides two useful functions to copy strings from one array to another. The first of these is strcpy(), which requires two arguments to be specified. The first argument specifies the name of the target array to copy the string into, and the second argument specifies the name of the source array from where the string should be copied. So, its syntax looks like this:

**strcpy( *target-array* , *source-array* ) ;**

All characters in the source array are copied into the target array, including the \0 null terminating character. If there are other elements after the null character these are also padded with \0. This ensures that remnants from a longer original string are removed when a shorter string is copied into an array.

The second string-copying function is the similarly named strncpy() function (with an added “n”). This is used like the strcpy() function but takes a third argument to specify how much of the string to copy. Its syntax therefore looks like this:

**strncpy( *target-array* , *source-array* , *length* ) ;**

The string being copied will begin with the first character of the source array but will end at the position specified by the third argument – so the final \0 null character is not automatically copied. After the characters have been copied, the next element in the target array must be assigned a terminating \0 null character to promote the array to constant string status. Thus it is necessary to ensure that the target array is always one element larger than the actual number of characters being copied into it, including space “characters”, to accommodate the final \0 null character.

![image](images/snake.jpg)

Ensure that the target array is of sufficient size to hold all the characters of the string being copied – including a terminating **\0** null character.

![image](images/pg18_1.jpg)

strcpy.c

![image](images/1b.jpg)Begin a new program with a preprocessor instruction to include the standard input/output and string functions

**#include <stdio.h>**

**#include <string.h>**

![image](images/2b.jpg)Add a main function that declares and initializes two character array variables with strings

**int main()**

**{**

**char s1[] = “Larger text string”, s2[] = “Smaller string” ;**

**}**

![image](images/3b.jpg)Next, in the main function block, output the first array contents together with its size and the string length

**printf( “\n%s: %d elements” , s1 , sizeof(s1) ) ;**

**printf( “, %d characters\n” , strlen(s1) ) ;**

![image](images/4b.jpg)Now, in the main function block, copy the entire contents of the second array into the first array

**strcpy( s1, s2 ) ;**

![image](images/5b.jpg)Repeat Step 3, to output the first array characteristics once more, then copy just the first five characters of the second array into the first array and add a null terminator

**strncpy( s1, s2, 5 ) ;**

**s1[5] = ‘\0’ ;**

![image](images/6b.jpg)Repeat Step 3, to output the first array characteristics again, then finally return the required zero integer value

**return 0 ;**

![image](images/7b.jpg)Save the program file, then compile and execute the program to see the copied strings

![image](images/pga113_1.jpg)

![image](images/hot.jpg)

Notice that the initial size of the arrays need not be specified in their declarations because the declarations also initialize them. Other arrays that are to be initialized later – say, by user input or by copying from another array – must specify a size in their declarations.

![image](images/forget.jpg)

Here the sixth element in the final **s1** string is **s1[5]** – because array index numbering begins at zero, not one.

**Joining strings**

The combining of two strings into one single string is more precisely known as string “concatenation”.

![image](images/pg120.jpg)

The standard C library string.h header file contains two functions that can be used to concatenate strings. To make these available to a program the string.h header file must be added with an #include directive at the start of the program.

The first string concatenation function is strcat(), which requires two arguments to be specified stating the names of the two strings to concatenate. The string named as its second argument is appended after the string named as its first argument, then the function returns the entire concatenated first string. So, the function’s syntax looks like this:

**strcat( *first-string* , *string-to-add-to-first-string* ) ;**

It is important to note that the first string array must be large enough to accommodate all the characters of the concatenated strings to avoid an error.

The second string-concatenation function is the similarly named strncat() function (with an added “n”). This is used like the strcat() function but takes a third argument to specify how many characters of the second string should be appended onto the first string. Its syntax therefore looks like this:

**strncat( *first-string* , *string-to-add-to-first-string* , *length* ) ;**

The string being appended will begin with the first character of the string specified by the second argument by default, and end at the position specified by the third argument. But as the name of the string is an implied pointer to its first character, pointer arithmetic can be used to indicate a different position at which to begin appending, with this syntax:

**strncat( first-string , (string-to-add-to-first-string+places) , length );**

Once again, as with the strcat() function, it is important that the first string array must be large enough to accommodate all the characters of the concatenated strings to avoid an error when using the strncat() function.

![image](images/forget.jpg)

These functions change the original string length as they add characters.

![image](images/pg18_1.jpg)

strcat.c

![image](images/1b.jpg)Begin a new program with a preprocessor instruction to include the standard input/output and string functions

**#include <stdio.h>**

**#include <string.h>**

![image](images/2b.jpg)Add a main function that declares and initializes four character array variables with strings

**int main()**

**{**

**char s1[100] = “A Place for Everything “ ;**

**char s2[] = “and Everything in its Place” ;**

**char s3[100] = “The Truth is Rarely Pure “ ;**

**char s4[] = “and Never Simple. - Oscar Wilde” ;**

**}**

![image](images/3b.jpg)Next, in the main function block, append the second string onto the first and output the concatenated string

**strcat( s1, s2 ) ; printf( “\n%s\n” , s1 ) ;**

![image](images/4b.jpg)Append the first 17 characters of the fourth string onto the third and output the concatenated string

**strncat( s3, s4, 17 ) ; printf( “\n%s\n” , s3 ) ;**

![image](images/5b.jpg)Append the last 14 characters of the fourth string onto the third and output the concatenated string

**strncat( s3, ( s4 + 17 ) , 14 ) ; printf( “\n%s\n” , s3 ) ;**

![image](images/6b.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7b.jpg)Save the program file, then compile and execute the program to see the concatenated strings

![image](images/pga115_1.jpg)

![image](images/snake.jpg)

The string being lengthened must have an array size large enough to accommodate all characters of the combined strings.

**Finding substrings**

A string can be searched to determine if it contains a specified “substring” sequence of characters with a function named strstr(). This is part of the standard library string.h header file, which must be added with an #include directive at the start of the program to make strstr() available.

![image](images/pg122_1.jpg)

The strstr() function takes two arguments – the first specifies the string to be searched, and the second specifies the substring to seek. If the substring is not found, the function returns a NULL value. When the substring is found, the function returns a pointer to the first character of the first occurrence of the substring.

The array index number of the element containing the first character of a located substring can be easily calculated using pointer arithmetic. Subtracting the address of the first character of the substring, returned by the strstr() function, from the address of the searched string’s first character (to which the character array name points) can produce an integer value that is the index number of the first substring character within the searched string.

In C programming, the == and != comparison operators can be used to compare a result against a NULL value but cannot be used to compare two strings. Instead, the string.h standard library header file provides a function named strcmp() for that purpose. This function takes two arguments that are the strings to be compared. The comparison is made based upon the numerical ASCII code value of each character and their position. When the strings are identical in every respect, including matching case, the strcmp() function returns zero. Otherwise, the function returns a positive or negative integer depending on the string values.

![image](images/pg18_1.jpg)

strstr.c

![image](images/1b.jpg)Begin a new program with a preprocessor instruction to include the standard input/output and string functions

**#include <stdio.h>**

**#include <string.h>**

![image](images/2b.jpg)Add a main function that declares and initializes two character array variables with strings

**int main()**

**{**

**char str[] = “No Time Like the Present.” ;**

**char sub[] = “Time” ;**

**}**

![image](images/snake.jpg)

The **strstr()** function stops searching when it finds the first occurrence of a substring. Subsequent occurrences of that substring within the searched string will not be recognized.

![image](images/3b.jpg)Next, in the main function block, output a message if the second string value cannot be found in the first string

**if( strstr( str, sub ) == NULL )**

**{**

**printf( “Substring \”Time\” Not Found\n” ) ;**

**}**

![image](images/4b.jpg)Now, add statements to output the memory address and element index number within the first string at which the first character of the located substring occurs

**else**

**{**

**printf( “Substring \”Time\” Found at %p\n” , strstr( str, sub) ) ;**

**printf( “Element Index Number %d\n\n”, strstr(str,sub) - str ) ;**

**}**

![image](images/5b.jpg)Output the result of three comparisons made against the value of the second string

**printf(“%s Versus \”Time\”: %d\n”,sub, strcmp(sub,”Time”));**

**printf(“%s Versus \”time\”: %d\n”,sub, strcmp(sub,“time”));**

**printf(“%s Versus \”TIME\”: %d\n” ,sub, strcmp(sub,“TIME”));**

![image](images/6b.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7b.jpg)Save the program file, then compile and execute the program to see the result of searching for a substring and the comparison of three string values

![image](images/pga117_1.jpg)

![image](images/forget.jpg)

Notice that the **\** character in this example is used to escape the double-quote characters – to avoid premature termination of the output strings.

![image](images/hot.jpg)

The **string.h** header file also contains two character-searching functions: **strchr()** finds the first occurrence of a character in a string, and **strrchr()** finds the last occurrence – both return **NULL** if the character is not found.

**Validating strings**

The standard library header file named ctype.h contains a number of functions that are useful to perform tests on characters. To make these available to a program, the ctype.h header file must be added with an #include directive at the start of the program.

![image](images/pg124_1.jpg)

Within the ctype.h header file, the isalpha() function tests whether a character is alphabetical, whereas isdigit() tests whether a character is numerical. Similarly, the ispunct() function tests whether a character is any other printable symbol, whereas the isspace() function tests whether a “character” is in fact a space.

Additionally, the ctype.h header provides isupper() and islower() functions to test the character case, along with toupper() and tolower() functions to change the character case.

Each test function returns a non-zero value (not necessarily a 1) when the tested character is as expected, but always returns a zero if it is not as expected.

These testing functions can be used to validate user string input by looping through characters in the string to examine each in turn. Where a character does not meet a required condition, a “flag” variable can be set to advise the user that the entry is invalid.

![image](images/pg18_1.jpg)

isval.c

![image](images/1b.jpg)Begin a new program with a preprocessor instruction to include the standard input/output and string functions

**#include <stdio.h>**

**#include <ctype.h>**

![image](images/2b.jpg)Add a main function that declares three variables, initializing a flag variable with a numeric true value (1)

**int main()**

**{**

**char str[7] ;**

**int i ;**

**int flag = 1 ;**

**}**

![image](images/3b.jpg)Next, in the main function, request user input then assign that input as a string to the array variable

**puts( “Enter six digits without any spaces...” ) ;**

**gets( str ) ;**

![image](images/4b.jpg)Now, in the main function block, add a loop to examine each character in the array variable

**for( i = 0 ; i < 6 ; i++ ) {           }**

![image](images/5b.jpg)Within the loop block, change the flag variable to false (0) if any character is not a digit

**if( !isdigit( str[i] ) )**

**{**

**flag = 0 ;**

**}**

![image](images/6b.jpg)Next, in the if block, describe any non-numeric character

**if( isalpha( str[i] ) )**

**{ printf( “Letter %c Found\n” , toupper(str[i]) ) ; }**

**else if( ispunct( str[i] ) )**

**{ printf( “Punctuation Found\n” ) ; }**

**else if( isspace( str[i] ) )**

**{ printf( “Space Found\n” ) ; }**

![image](images/7b.jpg)After the loop block, output a message describing the flag variable state

**( flag ) ? puts(“Entry Valid”) : puts(“Entry Invalid”) ;**

![image](images/8b.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/9b.jpg)Save the program file, then compile and execute the program to see validation of input strings

![image](images/pga119_1.jpg)

![image](images/forget.jpg)

The **isdigit()** test could alternatively be expressed like this: **isdigit() == 0**.

![image](images/hot.jpg)

The full range of character test functions can be found in the Reference section [here](#chapter11.xhtml_sec80).

**Converting strings**

The standard C library file stdlib.h contains a useful function named atoi() that can be used to convert a string to an integer. To make this function available to a program, the stdlib.h file must be added with an #include directive at the start of the program.

![image](images/pg126_1.jpg)

The atoi() function, alpha-to-integer, takes the string to be converted as its single argument. If the string is empty, or if the string’s first character is not a number or a minus sign, then atoi() will return zero. Otherwise the string, or at least the numeric start of the string, will be converted to an int data type up until atoi() meets a non-numeric character in the string. When atoi() meets a non-numeric character in the string it returns the number so far converted as an int data type.

There is also an itoa() function, integer-to-alpha, that can be used to convert an int data type value to a string. This is widely used but is not part of the standard ANSI C specification. The itoa() function requires three arguments to specify the number to be converted; the string to which the converted number is to be assigned; and finally, the base to be used for the conversion. For example, a specified base of 2 will assign the binary equivalent of the specified numeric argument to the specified string argument.

An ANSI-compliant alternative to the itoa() function is the sprintf() function in the stdlib.h header file. It is less powerful because a base value cannot be specified. The sprintf() function also takes three arguments – the string to which the converted number is to be assigned, a format specifier, and the number to be converted. This function returns an integer that is the number of characters in the converted string.

![image](images/pg18_1.jpg)

conv.c

![image](images/1b.jpg)Begin a new program with a preprocessor instruction to include the standard input/output and conversion functions

**#include <stdio.h>**

**#include <stdlib.h>**

![image](images/2b.jpg)Add a main function that declares three integer variables, then declares and initializes three character arrays

**int main()**

**{**

**int n1, n2, n3 ;**

**char s1[10]= “12eight”, s2[10]= “-65.8”, s3[10]= “x13” ;**

**}**

![image](images/3b.jpg)Now, in the main function block, attempt to convert each string to an integer value and output the results

**n1 = atoi( s1 ) ;**

**printf( “\nString %s converts to Integer: %d\n” , s1 , n1 ) ;**

**n2 = atoi( s2 ) ;**

**printf( “String %s converts to Integer: %d\n” , s2 , n2 ) ;**

**n3 = atoi( s3 ) ;**

**printf( “String %s converts to Integer: %d\n\n” , s3 , n3 ) ;**

![image](images/4b.jpg)Next, in the function block, convert the first integer variable value to a string containing its binary equivalent using a non-standard function and output the result

**itoa( n1, s1, 2 ) ;**

**printf( “Decimal %d is Binary: %s\n” , n1 , s1 ) ;**

![image](images/5b.jpg)Then, convert the first integer variable value to strings containing its octal and hexadecimal equivalents using a standard library function and store their character length

**n2 = sprintf( s3, “%o”, n1 ) ;**

**printf( “Decimal %d is Octal: %s chars: %d\n”, n1, s3, n2) ;**

**n3 = sprintf( s3, “%x”, n1 ) ;**

**printf(“Decimal %d is Hexadecimal: %s chars: %d\n”,n1,s3,n3);**

![image](images/6b.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7b.jpg)Save the program file, then compile and execute the program to see the conversions

![image](images/pga121_1.jpg)

![image](images/snake.jpg)

The **itoa()** function is very useful, but because it is not part of the ANSI standard it is not supported by all compilers – it is, however, supported by the GNU C Compiler featured in this book.

![image](images/forget.jpg)

Unlike the **itoa()** function, **sprintf()** cannot convert to binary because there is no format specifier for binary numbers.

**Summary**

![image](images/pgc20_1.jpg)

•In C programming, a string is an array of characters that has the special \0 null character in its final element.

•Each character also has a numerical ASCII code value.

•A character array name acts like a pointer to the entire string.

•The scanf() function stops reading input at the first space character it encounters, but the gets() function accepts spaces and automatically adds a final \0 null character.

•The puts() function outputs a string specified as its argument and automatically adds a newline at the end of the string.

•Special string-handling functions are available from the standard C library string.h header file, such as the strlen() function that returns the length of a specified string, or the strcpy() and strncpy() functions that can copy strings.

•The string.h header file also provides the strcat() and strncat() functions, which can be used to concatenate strings together.

•Additionally, string.h provides the strstr() function that searches a string for a specified substring, and the strcmp() function that compares two specified strings.

•When strstr() fails to find the substring it seeks, the function returns a value of NULL.

•The standard C library ctype.h header file provides functions to test character types, such as isalpha(), isdigit() and ispunc().

•The ctype.h header file also provides islower(), isupper() and tolower(), toupper() functions that test and set character case.

•The standard library stdlib.h header file provides the atoi() function that can convert a string to an integer.

•The standard library stdlib.h header file provides the sprintf() function that can convert an integer to a string, in much the same way as the more powerful non-standard itoa() function.

9

**Building structures**

***This chapter introduces the “struct” structure and “union” abstract data types, and demonstrates how they can be used in C programs to group together multiple variables of different types.***

[**Grouping in a structure**](#chapter09.xhtml_sec59)

[**Defining type structures**](#chapter09.xhtml_sec60)

[**Using pointers in structures**](#chapter09.xhtml_sec61)

[**Pointing to structures**](#chapter09.xhtml_sec62)

[**Passing structures to functions**](#chapter09.xhtml_sec63)

[**Grouping in a union**](#chapter09.xhtml_sec64)

[**Allocating memory**](#chapter09.xhtml_sec65)

[**Summary**](#chapter09.xhtml_sec66)

**Grouping in a structure**

A structure in a C program can contain one or more variables of the same or different data types. These are grouped together in a single structure and can be conveniently referenced via its name. Variables within structures are known as its “members”.

![image](images/pga124_1.jpg)

Grouping related variables together in a structure is helpful in organizing complicated data, especially in larger programs. For example, a structure could be created to describe a payroll record with variables to store an employee name, address, salary, tax, etc.

A structure is declared in a C program using the struct keyword followed by a given name and braces containing the variable members. Finally, the structure declaration must be terminated by a semicolon after the closing brace; so a structure containing members to describe x and y coordinates of a point in a graph could look like this:

**struct coords**

**{**

**int x ;**

**int y ;**

**} ;**

Optionally, “tag” names can be included just before the terminating semicolon as a comma-separated list. In effect, the structure declaration defines a new data type, and tag names act like variables of that data type. For example, a variable named “point” of the data type “coords” can be declared like this:

**struct coords**

**{**

**int x ;**

**int y ;**

**} point ;**

Each struct member can then be referenced by appending the “.” operator and the member name to the tag name, such as point.x.

Also, a new structure variable can be declared using the name of an existing structure, and that new variable will inherit the original member properties. For example, create a new structure variable named “top” based on the structure named “coords” with members top.x and top.y with this declaration:

struct coords top ;

![image](images/snake.jpg)

Variable members of a structure cannot be immediately initialized in the struct declaration.

![image](images/hot.jpg)

Typically, a struct declaration will appear before the main() function in a C program.

![image](images/commoncr.jpg)

struct.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Declare a structure with two members and one tag

**struct coords**

**{**

**int x ;**

**int y ;**

**} point ;**

![image](images/3r.jpg)Then, create another instance of the structure

**struct coords top ;**

![image](images/4r.jpg)Next, add a main function that initializes both members of each structure

**int main()**

**{**

**point.x = 5 ; point.y = 8 ;**

**top.x = 15 ; top.y = 24 ;**

**}**

![image](images/pg131_3.jpg)

![image](images/5r.jpg)Now, output the value stored in each structure member

**printf( “\npoint x: %d, point y: %d\n”, point.x , point.y ) ;**

**printf( “\ntop x: %d, top y: %d\n” , top.x , top.y ) ;**

![image](images/6r.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7r.jpg)Save the program file, then compile and execute the program to see the values stored in structure members

![image](images/pga125_1.jpg)

**Defining type structures**

A data type defined by a structure can be declared to be an actual data type definition by adding the typedef keyword at the very beginning of the structure declaration. This identifies the structure to be a prototype from which other structures can be declared simply using any of its tag names – without the struct keyword.

![image](images/pg132_1.jpg)

Using typedef may often help simplify the code by not requiring the struct keyword when declaring variables of a data type defined in a structure. It is helpful, however, to capitalize the tag name so it is easily recognizable as a structure-defined data type.

Declarations of variables of data types defined in a structure may optionally initialize all their members by assigning values as a comma-separated list within braces.

Structures may also be nested within other structures. In that case, individual members are referenced using two “.” dot operators, with the syntax *outer-structure.inner-structure.member*.

![image](images/commoncr.jpg)

typedef.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Declare an un-named structure defining a data type with two members and one tag

**typedef struct**

**{**

**int x ;**

**int y ;**

**} Point ;**

![image](images/3r.jpg)Then, create two variables of the structure-defined data type, initializing both members of one variable

**Point top = { 15 , 24 } ;**

**Point btm ;**

![image](images/4r.jpg)Next, add a main function that initializes both members of the other variable of the structure-defined data type

**int main()**

**{**

**btm.x = 5 ;**

**btm.y = 8 ;**

**}**

![image](images/5r.jpg)Now, output the coordinates of both points

**printf( “\nTop x: %d, y: %d\n” , top.x , top.y ) ;**

**printf( “Bottom x: %d, y: %d\n” , btm.x , btm.y ) ;**

![image](images/6r.jpg)Before the main function block, insert a second structure defining a data type with two nested structure members

**typedef struct**

**{**

**Point a ;**

**Point b ;**

**} Box ;**

![image](images/7r.jpg)Next, declare a variable of the second structure-defined data type, initializing all its members

**Box rect = { 6 , 12 , 30 , 20 } ;**

![image](images/8r.jpg)Back in the main function block, output the coordinates of all points contained in the nested structure members

**printf( “\nPoint a x: %d” , rect.a.x ) ;**

**printf( “\nPoint a y: %d” , rect.a.y ) ;**

**printf( “\nPoint b x: %d” , rect.b.x ) ;**

**printf( “\nPoint b y: %d\n” , rect.b.y ) ;**

![image](images/9r.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/10r.jpg)Save the program file, then compile and execute the program to see the values stored in structure members

![image](images/pga127_1.jpg)

![image](images/hot.jpg)

Notice that the structure itself need not be named, as it is the tag name that‘s important.

![image](images/snake.jpg)

Struct members can only be initialized using a comma-separated list in the variable declaration – they must be individually initialized later.

**Using pointers in structures**

There is an advantage in using a character pointer in a structure as a string container over using a character array for the same purpose.

![image](images/pg134_1.jpg)

An entire string can only be assigned to a char array upon its declaration. The only way to subsequently assign a string to a struct char array using the = operator is to assign individual characters to one element at a time.

In each assignation the value to the left of the = operator is known as the “L-value”, representing the memory Location, whereas the value to the right of the = operator is known as the “R-value”, representing the data to Read into that location.

One important rule in C programming is that an R-value cannot appear on the left side of an = operator. An L-value, on the other hand, may appear on either side of an = operator.

Each individual element of a char array is an L-value to which an individual character may be assigned, but a char pointer is also an L-value to which an entire string may be assigned after that pointer has been declared.

![image](images/commoncr.jpg)

strmbr.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Next, declare an un-named structure defining a data type with a single character array member and one tag name

**typedef struct**

**{**

**char str[5] ;**

**} ArrType ;**

![image](images/3r.jpg)Now, declare an un-named structure defining a data type with a single character pointer member and one tag name

**typedef struct**

**{**

**char *str ;**

**} PtrType ;**

![image](images/4r.jpg)Then, declare one variable of each structure-defined data type, initializing the single member of each variable

**ArrType arr = { ‘B’, ’a’, ’d’, ’ ‘, ’\0’ } ;**

**PtrType ptr = { “Good ” } ;**

![image](images/hot.jpg)

L-values are objects whereas R-values are data.

![image](images/5r.jpg)Next, add a main function that outputs the string value of the variable character array member

**int main()**

**{**

**printf( “\nArray string is a %s” , arr.str ) ;**

**}**

![image](images/6r.jpg)Within the main function block, tediously assign new values to each element of the character array and output the new string value

**arr.str[0] = ‘I’ ;**

**arr.str[1] = ‘d’ ;**

**arr.str[2] = ‘e’ ;**

**arr.str[3] = ‘a’ ;**

**arr.str[4] = ‘\0’ ;**

**printf( “%s\n” , arr.str ) ;**

![image](images/7r.jpg)Next, output the string value of the variable character pointer member

**printf( “\nPointer string is a %s” , ptr.str ) ;**

![image](images/8r.jpg)Now, easily assign a new value to the character pointer and output the new string value

**ptr.str = “Idea” ;**

**printf( “%s\n” , ptr.str ) ;**

![image](images/9r.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/10r.jpg)Save the program file, then compile and execute the program to see the values stored in the structure members

![image](images/pga129_1.jpg)

![image](images/hot.jpg)

Notice that the members of different structures can be named alike without conflict.

![image](images/forget.jpg)

The elements of a **char** array can only be initialized using a comma-separated list in its declaration.

**Pointing to structures**

Pointers to struct data types can be created in just the same way as pointers to regular data types. In this case, the pointer holds the address of the beginning of the region of memory used to store the member data.

![image](images/pg136_1.jpg)

The use of pointers to structures is so common in C programs that there is even a special operator to describe it. In a struct pointer the “.” dot operator can be replaced by “->”, which is a hyphen followed by the greater-than operator. This combination is known as the arrow operator. For example, a pointer to a struct member ptr->member is the equivalent of (*ptr).member.

![image](images/commoncr.jpg)

structptr.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Next, declare an un-named structure defining a data type with two character pointer members and one tag name

**typedef struct**

**{**

**char *name; char *popn ;**

**} City ;**

![image](images/3r.jpg)Now, add a main function that declares three regular variables and a pointer variable, all of the struct data type

**int main()**

**{**

**City ny , la , ch , *ptr ;**

**}**

![image](images/4r.jpg)Within the main function block, assign values to members of the first variable then display the stored values, using the dot operator to both store and retrieve the values

**ny.name = “New York City” ;**

**ny.popn = “8,274,527” ;**

**printf( “\n%s , Population: %s\n”, ny.name , ny.popn ) ;**

![image](images/5r.jpg)Assign the address of the second variable to the pointer variable

**ptr = &la ;**

![image](images/hot.jpg)

The arrow operator is useful in C programming to differentiate between structure pointers and other pointers.

![image](images/6r.jpg)Now, assign values to members of the second variable, then display the stored values, using the arrow operator to store the values and the dot operator to retrieve the values

**ptr->name = “Los Angeles” ;**

**ptr->popn = “3,834,340” ;**

**printf( “\n%s, Population: %s\n” , la.name, la.popn ) ;**

![image](images/7r.jpg)Next, assign the address of the third variable to the pointer variable

**ptr = &ch ;**

![image](images/8r.jpg)Now, assign values to members of the third variable, then display the stored values, using the arrow operator to both store and retrieve the values

**ptr->name = “Chicago” ;**

**ptr->popn = “2,836,658” ;**

**printf( “\n%s, Population: %s\n”, ptr->name, ptr->popn ) ;**

![image](images/9r.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/10r.jpg)Save the program file, then compile and execute the program to see the values stored in the structure members

![image](images/pga131_1.jpg)

![image](images/forget.jpg)

The population values in this example are assigned as strings to preserve the comma separations.

**Passing structures to functions**

Structure member values can be stored in an array, just like the values of any other data type. The array is declared as usual, but the method used to assign the values to its elements is slightly different. Each comma-separated list of member values must be enclosed within a pair of braces.

![image](images/pg138_1.jpg)

Similarly, a struct can be passed as an argument to a function, just like any other variable. The structure’s data type must be specified in both the function prototype declaration and its definition, along with a variable name by which the function can address its member values.

But remember that passing by value, simply using a regular variable, means that the function will operate on a copy of the struct – its original member values will remain unchanged. Passing the struct by reference, on the other hand, using a pointer variable, means that the function will operate on the original struct members – so the original member values will get changed.

![image](images/commoncr.jpg)

passstruct.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

#**include <stdio.h>**

![image](images/2r.jpg)Next, declare an un-named structure defining a data type with two members and one tag name

**typedef struct**

**{**

**char *name ;**

**int quantity ;**

**} Item ;**

![image](images/3r.jpg)Now, declare an array of the structure’s data type, initializing each member of three structures

**Item fruits[3] =**

**{ { “Apple” , 10 }, { “Orange” , 20 }, { “Pear” , 30 } } ;**

![image](images/4r.jpg)Add a function prototype that will pass a structure variable and a pointer variable to a structure as arguments

**void display( Item val , Item *ref ) ;**

![image](images/snake.jpg)

Simply assigning all the values as a comma-separated list will not work – each set of values must be enclosed by its own pair of braces.

![image](images/5r.jpg)Now, define the function declared in the prototype that begins by revealing the value of the passed arguments

**void display( Item val , Item *ref )**

**{ printf( “%s: %d\n” , val.name , val.quantity ) ; }**

![image](images/6r.jpg)Next, in the function block, change the values of the struct member copies passed then output the new values

**val.name = “Banana” ; val.quantity = 40 ;**

**printf( “%s: %d\n” , val.name , val.quantity ) ;**

![image](images/7r.jpg)Confirm that the original values are unchanged

**printf( “%s: %d\n” , fruits[0].name , fruits[0].quantity ) ;**

![image](images/8r.jpg)Then, change the original member values and output the new values

**ref->name = “Peach” ;**

**ref->quantity = 50 ;**

**printf( “%s: %d\n” , fruits[0].name , fruits[0].quantity ) ;**

![image](images/9r.jpg)Just before the function block, insert a main function that calls the other function, passing a struct and a pointer as arguments

**int main()**

**{**

**display( fruits[0] , &fruits[0] ) ;**

**}**

![image](images/10r.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/11r.jpg)Save the program file, then compile and execute the program to see the values stored in the structure members

![image](images/pga133_1.jpg)

![image](images/hot.jpg)

Passing large structs by value is inefficient as it creates a copy of the entire struct in memory, whereas passing by reference only requires the size of a pointer.

**Grouping in a union**

In C programming, a “union” allows different pieces of data, of any data type, to be stored at the same memory location as the program proceeds – assigning a value to the union will overwrite that previously stored there. This allows efficient use of memory.

![image](images/pg140_1.jpg)

A union is like a struct but is declared with the union keyword and, because of its nature, its members can only be assigned values individually as the program proceeds.

An array of unions can be created in the same way as an array of structs was created in the previous example, but union members can only be initialized in the declaration if they are all of the same data type. A pointer to a union can be created in exactly the same manner in which a pointer to a struct is created and a union can be passed to a function just like any other variable.

![image](images/commoncr.jpg)

union.c

![image](images/1r.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2r.jpg)Next, declare an un-named structure defining a data type with three members and one tag name

**typedef struct**

**{ int num ; char ltr, *str ; } Distinct ;**

![image](images/3r.jpg)Now, declare an un-named union defining a data type with three members and one tag name

**typedef union { int num ; char ltr , *str ; } Unified ;**

![image](images/4r.jpg)Add a main function that declares a variable of the struct’s data type and initializes each of its members

**int main()**

**{**

**Distinct sdata = { 10 , ‘C’ , “Program” } ;**

**}**

![image](images/5r.jpg)Now, in the main function block, declare a variable of the union data type

**Unified udata ;**

![image](images/forget.jpg)

It is the programmer’s responsibility to understand which type of data is being stored in a union at any point in the execution of a program.

![image](images/6r.jpg)After the variable declarations, output the value and memory address of each struct member

**printf( “\nStructure:\nNumber: %d”, sdata.num ) ;**

**printf( “\tStored at: %p\n” , &sdata.num ) ;**

**printf( “Letter: %c” , sdata.ltr ) ;**

**printf( “\tStored at: %p\n” , &sdata.ltr ) ;**

**printf( “String: %s” , sdata.str ) ;**

**printf( “\tStored at: %p\n” , &sdata.str ) ;**

![image](images/7r.jpg)Now, assign a value to the first union member then output its value and memory address

**udata.num = 16 ;**

**printf( “\nUnion:\nNumber: %d” , udata.num ) ;**

**printf( “\tStored at: %p\n” , &udata.num ) ;**

![image](images/8r.jpg)Next, assign a value to the second union member then output its value and memory address

**udata.ltr = ‘A’ ;**

**printf( “Letter: %c” , udata.ltr ) ;**

**printf( “\tStored at: %p\n” , &udata.ltr ) ;**

![image](images/9r.jpg)Finally, assign a value to the third union member then output its value and memory address

**udata.str = “Union” ;**

**printf( “String: %s”, udata.str ) ;**

**printf( “\tStored at: %p\n” , &udata.str ) ;**

![image](images/10r.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/11r.jpg)Save the program file, then compile and execute the program to see the values stored in the structure, and union members and the addresses where they are stored

![image](images/pga135_1.jpg)

![image](images/hot.jpg)

Unions are mostly useful when memory is very limited.

**Allocating memory**

The standard C stdlib.h library header file provides memory management functions, with which a program can explicitly request memory be made available as the program executes. The malloc() function requires a single integer argument to specify how many bytes of memory to allocate, whereas the calloc() function requires two integer arguments that get multiplied together to specify how many bytes of memory to allocate. Both of these functions return a pointer to the beginning of the memory block when successful, or a NULL value upon failure.

![image](images/pg142_1.jpg)

Memory previously allocated with malloc() or calloc() can be increased with the realloc() function. This requires the pointer to the allocated memory block as its first argument, and an integer specifying the new block size as its second argument. It returns a pointer to the beginning of the enlarged memory block when successful, or a NULL value upon failure.

All memory allocated with these functions should be released when no longer required by specifying the memory block pointer as the argument to the free() function.

There is no standard C function to determine the size of a dynamically allocated memory block but this can be discovered with platform-specific functions. On Windows there is _msize() and on Linux there is malloc_usable_size(). Both these functions require the memory block pointer as their argument.

![image](images/commoncr.jpg)

memory.c

![image](images/1r.jpg)Begin a new program with preprocessor instructions to include the standard library input/output functions and memory management functions

**#include <stdio.h>**

**#include <stdlib.h>**

![image](images/2r.jpg)Declare a Windows-specific function prototype

**int _msize( int *bytes ) ;**

![image](images/3r.jpg)Add a main function that declares an integer variable and an integer pointer variable

**int main()**

**{**

**int size , *mem ;**

**}**

![image](images/hot.jpg)

The **calloc()** function clears all allocated memory space to zero, but **malloc()** leaves whatever values are already there.

![image](images/forget.jpg)

On Linux systems, replace the **_msize** prototype declaration and function calls with the alternative **malloc_usable_size**.

![image](images/4r.jpg)Request memory to accommodate 100 integers

**mem = malloc( 100 * sizeof( int ) ) ;**

![image](images/5r.jpg)Next, output details of the allocated memory block or an advisory message if the request fails

**if( mem != NULL )**

**{**

**size = _msize( mem ) ;**

**printf( “\nSize of block for 100 ints: %d bytes\n”, size ) ;**

**printf( “Beginning at %p\n” , mem ) ;**

**}**

**else { printf( “!!! Insufficient memory\n”) ; return 1 ; }**

![image](images/6r.jpg)Now, attempt to enlarge the allocated memory block and output its details or an advisory message if the request fails

**mem = realloc( mem , size + ( 100 * sizeof( int ) ) ) ;**

**if( mem != NULL )**

**{**

**size = _msize( mem ) ;**

**printf( “\nSize of block for 200 ints: %d bytes\n” , size ) ;**

**printf( “Beginning at %p\n” , mem ) ;**

**}**

**else { printf( “!!! Insufficient memory\n”) ; return 1 ; }**

![image](images/7r.jpg)At the end of the main function block, remember to release the allocated memory, then return the require zero integer value

**free( mem ) ;**

**return 0 ;**

![image](images/8r.jpg)Save the program file, then compile and execute the program to see the allocated memory blocks when the requests are successful

![image](images/pga137_1.jpg)

![image](images/hot.jpg)

Even though an int typically occupies 4 bytes it is good practice to use the sizeof() operator to specify the size in case of variation.

![image](images/snake.jpg)

The implementation of the realloc() function can vary on different platforms.

![image](images/forget.jpg)

The memory request statement could alternatively have used calloc( 100 , sizeof(int) ) .

**Summary**

![image](images/pgb42_1.jpg)

•A struct can contain one or more variables of any data type, which are known as struct members.

•Each struct member can be referenced by appending its name to a tag name with the . dot operator.

•Further instances of a struct will inherit the member properties of the original from which they are derived.

•The struct keyword may be preceded by the typedef keyword to declare the struct to be a data type.

•It is helpful to capitalize tag names to readily identify structure-defined data types.

•Variable declarations may optionally initialize each struct member by assigning a comma-separated list of values.

•A pointer to a struct holds the memory address of the beginning of the region of memory used to store member data.

•In a struct pointer, the . dot operator can be replaced by the -> arrow operator.

•The members in an array of structures may, optionally, be initialized in the declaration – but each list of member values must be enclosed within a pair of braces.

•A struct may be passed as an argument to a function, just like any other variable.

•Passing a struct variable to a function means it will operate on a copy of the struct members, but passing a struct pointer variable means the function operates on the original members.

•A union is like a struct in which different pieces of data are stored at the same memory location as the program proceeds.

•The standard C library stdlib.h header file provides the malloc(), calloc() and realloc() functions, which can allocate memory, and the free() function to release allocated memory.

10

**Producing results**

***This chapter demonstrates how C programs can utilize files, system time, random numbers, and a simple Windows dialog box.***

[Creating a file](#chapter10.xhtml_sec67)

[Reading & writing characters](#chapter10.xhtml_sec68)

[Reading & writing lines](#chapter10.xhtml_sec69)

[Reading & writing entire files](#chapter10.xhtml_sec70)

[Scanning filestreams](#chapter10.xhtml_sec71)

[Reporting errors](#chapter10.xhtml_sec72)

[Getting the date and time](#chapter10.xhtml_sec73)

[Running a timer](#chapter10.xhtml_sec74)

[Generating random numbers](#chapter10.xhtml_sec75)

[Displaying a dialog box](#chapter10.xhtml_sec76)

[Summary](#chapter10.xhtml_sec77)

**Creating a file**

A special data type for handling files is defined in the **stdio.h** header file. It is called a “file pointer” and has the syntax **FILE **fp***. File pointers are used to open, read, write, and close files. In a C program, a file pointer called “file_ptr” can be created with the declaration **FILE *file_ptr ;** .

![image](images/pga140_1.jpg)

A file pointer points to a structure defined in the **stdio.h** header file that contains information about the file. This includes details about the current character and if the file is being read or written.

Before a file can be read or written it firstly must always be opened with the **fopen()** function. This takes two arguments to specify the name and location of the file, and a “mode” in which to open the file. The **fopen()** function returns a file pointer if successful, or a **NULL** value upon failure.

Once a file has been successfully opened it can be read or added to, or new text can be written in the file, depending on the mode specified in the call to the **fopen()** function. Following this, the open file must then always be closed by calling the **fclose()** function and specifying the file pointer as its single argument.

The table below lists all the possible file modes that can be specified as the second argument to the **fopen()** function:

| **File mode** | **Operation**  |
| **r** | Open an existing file to read |
| **w** | Open an existing file to write. Creates a new file if none exists, or opens an existing file and discards all its previous contents |
| **a** | Appends text. Opens or creates a text file for writing at the end of the file |
| **r+** | Opens a text file to read from or write to |
| **w+** | Opens a text file to write to or read from |
| **a+** | Opens or creates a text file to read from or write to at the end of the file |
| Note: Where the mode includes a **b** after any of the file modes listed above, the operation relates to a binary file rather than a text file – for example, **rb** or **w+b** |

![image](images/hot.jpg)

All the standard functions for file input/ output are contained in the **stdio.h** header file.

![image](images/forget.jpg)

For convenience, all the text files in the examples in this chapter are located in the **MyPrograms** folder that also contains the C source code files. On Windows the directory is **C:\MyPrograms**, and on Linux systems it’s at **/** **home/MyPrograms**.

![image](images/commoncg.jpg)

newfile.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add a main function that declares a file pointer

**int main()**

**{**

**FILE *file_ptr ;**

**}**

![image](images/3g.jpg)Next, in the main function block, attempt to create a file for writing to

**file_ptr = fopen( “data.txt”, “w” ) ;**

![image](images/4g.jpg)Now, output a message to confirm the attempt succeeded, then close the file and return a zero integer value as required by the function declaration

**if( file_ptr != NULL )**

**{**

**printf( “File created\n” ) ;**

**fclose( file_ ptr ) ;**

**return 0 ;**

**}**

![image](images/5g.jpg)Finally, output an alternative message if the attempt fails

**else**

**{**

**printf( “Unable to create file\n” ) ; return 1 ;**

**}**

![image](images/6g.jpg)Save the program file, then compile and execute the program to attempt to create a text file

![image](images/pga141_1.jpg)

![image](images/snake.jpg)

Notice that both file name and file mode arguments must be enclosed within double quotes.

![image](images/hot.jpg)

Notice that this program returns a value of 1 to the system when the attempt to open the file fails – this tells the system that all did not go well.

**Reading & writing characters**

**Standard input**

The **scanf()** function, used in previous examples, is the simplified version of a function named **fscanf()** that requires an input filestream as its first argument. This indicates a source from where a series of characters will be introduced into the program.

![image](images/pg148_1.jpg)

In C programming, the filestream named **stdin** represents the keyboard and is the default source for the **scanf()** function. The function call **scanf(...)** is the same as **fscanf( stdin, ... )** .

**Standard output**

Similarly, the **printf()** function is the simplified version of a function named **fprintf()** that requires an output filestream as its first argument. This indicates a destination where a series of characters will be output from the program.

The filestream named **stdout** represents the monitor, and is the default source for the **printf()** function. The function call **printf(...)** is the same as **fprintf( stdout, ... )** .

Other standard functions, which have **stdin** or **stdout** as their default filestreams, also have equivalents allowing an alternative filestream to be specified. These can be used to read files by specifying a file pointer as an alternative to reading from the **stdin** filestream. They can also be used to write files by specifying an alternative to the **stdout** filestream:

•The **fputc()** function can be used to write to a filestream one character at a time – typically by looping through a **char** array. Its companion **fgetc()** can be used to read from a filestream one character at a time.

•The **fputs()** function can be used to write to a filestream one line at a time, and its companion **fgets()** can be used to read from a filestream one line at a time.

•The **fread()** function can be used to read an entire filestream, and its partner **fwrite()** can write an entire filestream.

•The **fscanf()** function and the **fprintf()** functions can be used to read and write filestreams with strings and numbers.

![image](images/hot.jpg)

Another standard output filestream named **stderr** is used to output error messages.

![image](images/commoncg.jpg)

writechars.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add a main function that declares a file pointer, a loop counter variable, and an initialized character array

**int main()**

**{**

**FILE *file_ptr ; int i ;**

**char text[50] = { “Text, one character at a time.” } ;**

**}**

![image](images/3g.jpg)Next, in the main function block, attempt to create a file for writing to

**file_ptr = fopen( “chars.txt” , “w” ) ;**

![image](images/4g.jpg)Now, output a message to confirm the attempt succeeded, write each character from the array, then close the file and return the required zero integer value

**if( file_ptr != NULL )**

**{**

**printf( “File chars.txt created\n” ) ;**

**for( i = 0 ; text[i] ; i++ ) { fputc( text[i], file_ptr ) ; }**

**fclose( file_ ptr ) ;**

**return 0 ;**

**}**

![image](images/5g.jpg)Finally, output an alternative message if the attempt fails

**else { printf( “Unable to create file\n” ) ; return 1 ; }**

![image](images/6g.jpg)Save the program file, then compile and execute the program to attempt to write a text file

![image](images/pga143_1.jpg)

![image](images/pga143_2.jpg)

![image](images/hot.jpg)

The **fputc()** function returns the ASCII code of the current character, or a constant called **EOF** denoting that the end of the file is reached.

**Reading & writing lines**

The **fgetc()** function is not the most efficient way to read text into a program, as it must be called repeatedly to read each character. It is better to employ the **fgets()** function that reads text one whole line at a time.

![image](images/pg150_2.jpg)

The **fgets()** function requires three arguments. The first argument specifies a **char** pointer or **char** array to which the text will be assigned. The second argument must be an integer specifying the maximum number of characters to read per line. The third argument is a file pointer specifying where to read from.

Similarly, the **fputc()** function, which writes text one character at a time, is less efficient than the **fputs()** function that writes text line by line. The **fputs()** function requires two arguments to specify the text to write and a file pointer denoting the file to be written to. A newline character is added by **fputs()** after the line is written. This function returns zero when successful, or the **EOF** constant when an error occurs or the end of the file is reached.

![image](images/commoncg.jpg)

lines.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output and string functions

**#include <stdio.h>**

**#include <string.h>**

![image](images/2g.jpg)Add a main function that declares a file pointer and an uninitialized character array

**int main()**

**{**

**FILE *file_ptr ;**

**char text[50] ;**

**}**

![image](images/3g.jpg)Next, in the main function block, attempt to open a local text file for both reading and appending to

**file_ptr = fopen( “farewell.txt”, “r+a” ) ;**

![image](images/pga144_1.jpg)

![image](images/4g.jpg)Now, output a message to confirm the attempt succeeded

**if( file_ptr != NULL )**

**{**

**printf( “File farewell.txt opened\n” ) ;**

**}**

![image](images/5g.jpg)Next, in the if block, read and output all lines from the file

**while( fgets( text, 50, file_ptr ) ) { printf( “%s”, text ) ; }**

![image](images/6g.jpg)Now, in the if block, copy a new string to the array then append that string to the text file

**strcpy( text , “...by Lord Alfred Tennyson” ) ;**

**fputs( text , file_ptr ) ;**

![image](images/7g.jpg)Finally, in the if block, close the file and return the required zero integer value

**fclose( file_ptr ) ;**

**return 0 ;**

![image](images/8g.jpg)Add an alternative message if the attempt fails

**else { printf( “Unable to open file\n” ) ; return 1 ; }**

![image](images/9g.jpg)Save the program file, then compile and execute the program to open the file and append the text string

![image](images/pg151_1.jpg)

![image](images/hot.jpg)

Notice how the **strcpy()** function is used here to assign a new string to the **char** array.

**Reading & writing entire files**

Whole files can be read with the **fread()** function and written with the **fwrite()** function. Both these functions take the same four arguments. The first is a **char** variable where the text can be stored. The second argument specifies the size of the chunks of text to read or write at a time – normally this will be 1\. The third argument specifies the total number of characters to read or write, and the fourth argument is a file pointer to the file to work with.

![image](images/pg152_2.jpg)

The **fread()** function returns the number of objects it has read, counting characters, spaces, and newlines as one object each. Similarly, **fwrite()** returns the number of objects it has written.

![image](images/commoncg.jpg)

readwrite.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add a main function that declares two file pointers, a character array variable, and an integer variable

**int main()**

**{**

**FILE *orig_ptr** ;

FILE *copy_ptr ;

char buffer[1000] ;

int num ;

**}**

![image](images/3g.jpg)Next, in the main function block, attempt to open an existing local file to read and another file to write to

**orig_ptr = fopen ( “original.txt” , “r” ) ;**

**copy_ptr = fopen( “copy.txt” , “w” ) ;**

![image](images/pga146_1.jpg)

![image](images/4g.jpg)Now, test that both files were successfully opened

**if( ( orig_ptr != NULL ) && ( copy_ptr != NULL ) )**

**{**

**}**

![image](images/forget.jpg)

The **char** array storing the text must be large enough to accommodate the entire content.

![image](images/5g.jpg)In the if block, read the contents from the original file into the character array, counting each object read, then write the contents of the array into the second file

**num = fread( buffer , 1 , 1000, orig_ptr ) ;**

**fwrite( buffer , 1 , num , copy_ptr ) ;**

![image](images/6g.jpg)Remember to close both text files upon completion

**fclose( orig_ptr ) ;**

**fclose( copy_ptr ) ;**

![image](images/7g.jpg)Finally, in the if block, output a confirmation, including the object count, and return the required zero integer value

**printf( “Done: original.txt copied to copy.txt” ) ;**

**printf( “\n%d objects copied.\n” , num ) ;**

**return 0 ;**

![image](images/8g.jpg)Add an alternative message for if the attempt should fail

**else**

**{**

**if(orig_ptr == NULL) printf( “Unable to open original.txt\n”) ;**

**if(copy_ptr == NULL) printf( “Unable to open copy.txt\n” ) ;**

**return 1 ;**

**}**

![image](images/9g.jpg)Save the program file, then compile and execute the program to open a file and copy its contents to a new file

![image](images/pg153_1.jpg)

![image](images/hot.jpg)

Use the number returned by **fread()** as the third argument to **fwrite()** to ensure that the number of objects written will be the same as the number of objects read.

![image](images/snake.jpg)

Ensure that the third argument to **fread()** is big enough to allow all the contents to be copied – changing the value in this example to 100 would then only copy the first 100 objects, omitting the final 70 objects.

**Scanning filestreams**

The **scanf()** function, used to get user input, is a simplified version of the **fscanf()** function with its filestream constantly set to **stdin**. The **fscanf()** function allows you to nominate the filestream to read as its first argument. It also has an advantage when reading files containing just numbers – numbers in a text file are simply seen as a string of characters, but when read by **fscanf()** they can be converted to their numeric type.

![image](images/pg154_2.jpg)

Similarly, the **printf()** function, used for output, is a simplified version of the **fprintf()** function with its filestream constantly set to **stdout**. The **fprintf()** function allows you to nominate the filestream to write to as its first argument.

So **fscanf()** and **fprintf()** offer great flexibility in choosing whether to read from **stdin** or a file, and whether to write to **stdout** or a file.

![image](images/commoncg.jpg)

fscanprint.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions

**#include <stdio.h>**

![image](images/2g.jpg)Add a main function that declares two file pointers, an integer array variable, and two regular integer variables

**int main()**

**{**

**FILE *nums_ptr , *hint_ptr ;**

**int nums[20] , i , j ;**

**}**

![image](images/3g.jpg)Next, in the main function block, attempt to open an existing local file to read and another file to write to

**nums_ptr = fopen ( “nums.txt” , “r” ) ;**

**hint_ptr = fopen( “hint.txt” , “w” ) ;**

![image](images/pga148_1.jpg)

![image](images/4g.jpg)Now, test that both files were successfully opened

**if( ( nums_ptr != NULL ) && ( hint_ptr != NULL ) )**

**{**

**}**

![image](images/5g.jpg)In the if block, scan the integers from the file into the elements of the integer array

**for( i = 0 ; !feof( nums_ptr ) ; i++ )**

**{**

**fscanf( nums_ptr , “%d” , &nums[i] ) ;**

**}**

![image](images/6g.jpg)Next, in the if block, output the array element values

**fprintf( stdout , “\nTotal numbers found: %d\n” , i ) ;**

**for( j=0 ; j<i ; j++ ) { fprintf( stdout , “%d “ , nums[j] ) ; }**

![image](images/7g.jpg)Now, write the array element values into a file

**fprintf( hint_ptr , “fscanf and fprintf are flexible\n” ) ;**

**for( j=0 ; j<i ; j++ ) { fprintf( hint_ptr , “%d “ , nums[j] ) ; }**

![image](images/8g.jpg)Finally, in the if block, close both files upon completion

**fclose( nums_ptr ) ;**

**fclose( hint_ptr ) ; return 0 ;**

![image](images/9g.jpg)Add an alternative message for if the attempt should fail

**else**

**{**

**fprintf( stdout , “Unable to open a file\n” ) ; return 1 ;**

**}**

![image](images/10g.jpg)Save the program file, then compile and execute the program to open a file then output and write its contents

![image](images/pga149_1.jpg)

![image](images/hot.jpg)

Notice that the **feof()** function is used in this example to test if the end of the file has been reached – exiting the loop when it is reached.

![image](images/forget.jpg)

The **fscanf()** and **fprintf()** functions take the same arguments as **scanf()** and **printf()** plus an additional first stream argument.

**Reporting errors**

The C language provides a function named **perror()** in the **stdio.h** header file that can be used to print descriptive error messages. It requires a string as its sole argument, to which **perror()** adds a colon followed by a description of the current error.

![image](images/pg156_1.jpg)

Additionally, the **errno.h** header file defines an integer expression named “errno” that is assigned an error code number when an error occurs. This error code number can be specified as the argument to a **strerror()** function from the **string.h** header file to output its associated error message.

![image](images/commoncg.jpg)

errno.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output functions, error message handling, and string functions

**#include <stdio.h>**

**#include <errno.h>**

**#include <string.h>**

![image](images/2g.jpg)Add a main function that declares a file pointer and an integer variable

**int main()**

**{**

**FILE *f_ptr ;**

**int i ;**

**}**

![image](images/3g.jpg)Next, in the main function block, attempt to open a file that does not actually exist

**f_ptr = fopen( “nosuch.file” , “r” ) ;**

![image](images/4g.jpg)Output a confirmation or an error message as the attempt has failed

**if( f_ptr != NULL ) { printf( “File opened\n” ) ; }**

**else { perror( “Error” ) ; }**

![image](images/5g.jpg)Now, add a loop to output the error message associated with each defined numerical errno error code

**for( i = 0 ; i < 44 ; i++)**

**{**

**printf( “Error %d : %s\n” , i , strerror(i) ) ;**

**}**

![image](images/6g.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/7g.jpg)Save the program file, then compile and execute the program to see the error messages

![image](images/pga151_1.jpg)

![image](images/hot.jpg)

The range of error code messages is implementation-defined. The range is larger on Linux systems than for the Windows platform.

**Getting the date and time**

![image](images/pga152_1.jpg)

Current system time is usually counted as the number of seconds elapsed since the Epoch at 00:00:00 GMT on January 1, 1970\. The total count represents the current date and time according to the Gregorian calendar and is referred to as “Calendar time”. Special functions to handle date and time are provided in the **time.h** header file along with a data type struct named **tm** in which to store date and time components, as below:

| **Component** | **Description**  |
| **int tm_sec** | seconds after the minute, normally 0-59 |
| **int tm_min** | minutes after the hour, 0-59 |
| **int tm_hour** | hours since midnight, 0-23 |
| **int tm_mday** | day of the month, 1-31 |
| **int tm_mon** | months since January, 0-11 |
| **int tm_year** | years since 1900 |
| **int tm_wday** | days since Sunday, 0-6 |
| **int tm_yday** | days since January 1st, 0-365 |
| **int tm_isdst** | is Daylight Saving Time in effect |

The current elapsed seconds count is returned by a **time( NULL )** function as a **time_t** data type. This can then be specified as the argument to a **localtime()** function for conversion to its various **tm** struct components.

The struct components can be output in a standard date and time format using an **asctime()** function. Alternatively, individual components can be output using special time format specifiers with a **strftime()** function. This function requires four arguments to specify a **char** array in which to store the formatted date string, the maximum string length, the text and format specifiers to extract the required components, and the **tm** struct to be used.

![image](images/hot.jpg)

The Daylight Saving component **tm_isdst** is positive if Daylight Saving is in effect; zero if not; or negative if that information is unavailable.

![image](images/forget.jpg)

A complete list of all time format specifiers is included in the Reference section [here](#chapter11.xhtml_page-183).

![image](images/commoncg.jpg)

datetime.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions and the date and time functions

**#include <stdio.h>**

**#include <time.h>**

![image](images/2g.jpg)Add a main function that declares a character array variable, a **time_t** variable, and a **tm** struct

**int main()**

**{**

**char buffer[100] ;**

**time_t elapsed ;**

**struct tm *now ;**

**}**

![image](images/3g.jpg)Next, in the main function block, get the current elapsed seconds count since the Epoch

**elapsed = time(NULL) ;**

![image](images/4g.jpg)Now, convert the count to local time components

**now = localtime( &elapsed ) ;**

![image](images/5g.jpg)Output the date and time in standard format

**printf( “%s\n” , asctime( now ) ) ;**

![image](images/6g.jpg)Then, output individual date and time components

**strftime ( buffer, 100, “Today is %A, %B %d.\n”, now ) ;**

**printf( “%s”, buffer ) ;**

**strftime ( buffer, 100, “The time is %I:%M %p.\n”, now ) ;**

**printf( “%s”, buffer ) ;**

![image](images/7g.jpg)Finally, return the required zero integer then save the program file; compile and execute the program to see the current date and time information

**return 0 ;**

![image](images/pga153_1.jpg)

![image](images/snake.jpg)

Notice that the **&** addressof operator is used in the conversion to local time in order to get the Calendar time from the **time_t** data type.

**Running a timer**

Getting the current time both before and after an event means that the duration of the event can be calculated by their difference. The **time.h** header file contains a **difftime()** function for that particular purpose. This function requires two arguments, both of which are of the **time_t** data type. It subtracts the second argument from the first argument and returns the difference expressed in whole seconds, but as a **double** data type.

![image](images/pg160_1.jpg)

Another way to work with time is offered by the **clock()** function from the **time.h** header file. This returns the processor time used since the program began, expressed in clock “ticks”. This function can be used to “pause” the execution of a program by running an empty loop until a future point in time is reached.

![image](images/commoncg.jpg)

wait.c

![image](images/1g.jpg)Begin a new program with a preprocessor instruction to include the standard input/output library functions and the date and time functions

**#include <stdio.h>**

**#include <time.h>**

![image](images/2g.jpg)Next, declare a function prototype to pause the program

**void wait( int seconds ) ;**

![image](images/3g.jpg)Add a main function that declares two **time_t** variables, and an integer variable

**int main()**

**{**

**time_t go , stop ;**

**int i ;**

**}**

![image](images/4g.jpg)Next, in the main function block, get the current time and output a message

**go = time( NULL ) ;**

**printf ( “\nStarting countdown...\n\n” ) ;**

![image](images/5g.jpg)Add a loop to output a countdown value and call the other function on each iteration

**for( i = 10 ; i > -1 ; i-- )**

**{**

**printf ( “ - %d”, i ) ;**

**wait(1) ;**

**}**

![image](images/6g.jpg)Next, in the main function block, get the current time once more then output the time taken to run the loop

**stop = time( NULL ) ;**

**printf(“\nRuntime: %.0f seconds\n” , difftime( stop, go ) ) ;**

![image](images/7g.jpg)Finally, in the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/8g.jpg)After the main function block, begin the function definition by initializing a **clock_t** variable at a future point beyond the current elapsed running time

**void wait( int seconds )**

**{**

**clock_t end_wait =**

**( clock() + ( seconds * CLOCKS_PER_SEC ) );**

**}**

![image](images/9g.jpg)Finally, in the wait function block, add an empty loop that terminates when the current time reaches the future point, returning control to the loop in the main function

**while ( clock() < end_wait ) {  }**

![image](images/10g.jpg)Save the program file, then compile and execute the program to see the countdown timer and runtime

![image](images/pga155_1.jpg)

![image](images/pga155_2.jpg)

![image](images/snake.jpg)

The number of clock ticks per second is implementation-dependent but is defined in **time.h** by the **CLOCKS_PER_SEC** constant.

![image](images/hot.jpg)

You can find the elapsed runtime expressed in seconds by dividing the value returned by the **clock()** function by the **CLOCKS_PER_SEC** value.

**Generating random numbers**

The **stdlib.h** header file provides a **rand()** function that generates a pseudo-random positive integer when called. This will, by default, return a number in the range from 0 to a large value (at least 32,767). A specific range can be set by using the modulus operator to specify a maximum upper limit – for example, to specify a range from 0 to 9 with the expression **rand() % 9**.

![image](images/pg162_1.jpg)

To set a minimum lower limit for the range, its value can be added to the result of the expression – for example, to specify a range from 1 to 10 with the expression **( rand() % 9 ) + 1**.

The numbers generated by the **rand()** function are not truly random, as the function successively generates the same sequence of numbers each time a program using **rand()** is executed. In order to generate a different sequence of numbers, the “seed” that starts the sequence must be specified. By default, the initial seed value is 1, but this can be changed by specifying an alternative integer argument to the **srand()** function – for example, **srand(8)**. This will cause **rand()** to generate a different sequence of numbers to those generated using the default seed value, but the sequence will still be repeated each time a program using **rand()** is executed.

To generate different random sequences upon successive execution the argument specified to **srand()** must be something other than a static integer. The common solution is to seed the **rand()** function with the current time in elapsed seconds with **srand( time( NULL) ).**

Now, the sequence of numbers generated by **rand()** will be different each time a program using **rand()** is executed.

![image](images/commoncg.jpg)

lotto.c

![image](images/1g.jpg)Begin a new program with preprocessor instructions to include the standard input/output library functions, random number, time, and string functions

**#include <stdio.h>**

**#include <stdlib.h>**

**#include <time.h>**

**#include <string.h>**

![image](images/2g.jpg)Add a main function that declares **int** and **char** variables

**int main()**

**{**

**int i , r , temp , nums[60] ;**

**char buf[4], str[100]= { “Your Six Lucky Numbers Are: “ } ;**

**}**

![image](images/3g.jpg)In the main function block, first seed the random number generator with the current elapsed seconds value

**srand( time(NULL) ) ;**

![image](images/4g.jpg)Next, fill an array with the numbers 0-59 in sequence

**for( i = 0 ; i < 60 ; i++ ) { nums[i] = i ; }**

![image](images/5g.jpg)Now, shuffle the sequence into a random order

**for( i = 1 ; i < 60 ; i++ )**

**{**

**r = ( rand() % 59 ) + 1 ;**

**temp = nums[i] ; nums[i]=nums[r] ; nums[r] = temp ;**

**}**

![image](images/6g.jpg)Add the numbers from six array elements to a string

**for( i = 1 ; i < 7 ; i++ )**

**{**

**sprintf( buf, “%d “, nums[i] ) ;**

**strcat( buf , “ “ ) ; strcat( str , buf ) ;**

**}**

![image](images/7g.jpg)Then, output the string

**printf( “\n%s\n\n” , str ) ;**

![image](images/8g.jpg)At the end of the main function block, return a zero integer value, as required by the function declaration

**return 0 ;**

![image](images/9g.jpg)Save the program file, then compile and execute the program repeatedly to see a selection of six different random numbers in the range 1-59 upon each execution

![image](images/pga157_1.jpg)

![image](images/forget.jpg)

The array element **nums[0]** gets assigned a zero value, but this is not included in the shuffle as only elements 1-59 are eligible for selection.

![image](images/hot.jpg)

Notice how the **sprintf()** function is used here to translate **int** values into **char** values that can then be concatenated to the larger text string.

**Displaying a dialog box**

In the Windows operating system, C programs can easily produce graphical components via special functions provided by the Windows Application Programming Interface (WINAPI). This is made available to the program by adding a compiler directive to include the Windows-specific **windows.h** header file.

![image](images/pg164_1.jpg)

In a C program for Windows, the usual **main()** function program entry point is replaced by this special **WinMain()** function:

**int WINAPI WinMain( HINSTANCE *hInstance*,**

**HINSTANCE *hPrevInstance*, LPSTR *lpCmdLine*, int *nCmdShow* )**

These arguments are always required in order for the program to communicate with the operating system. The *hInstance* argument is a “handle” reference to the program; and the *hPrevInstance* argument, used in earlier Windows programming, can be safely ignored these days. The *lpCmdLine* argument is a string that represents all items used on the command line to compile the application, and the *nCmdShow* argument controls how the window will be displayed.

The most simple graphical component to create in Windows is a basic dialog box with just one “OK” button. This is created by calling this **MessageBox()** function:

**int MessageBox( HWND *hWnd*, LPCTSTR *lpText*,**

**LPCTSTR *lpCaption*, UINT *uType* );**

The ***hWnd*** argument is a “handle” reference to the parent window, if any – without a parent window this value is specified as **NULL**. The *lpText* argument is the message string to be displayed, and the *lpCaption* argument is the title to be displayed on the dialog box. Finally, the *uType* argument can specify icons and buttons using special constant values in a pipe-delimited list. For example, the constant **MB_OK** adds an OK button and an exclamation icon can be added with the constant **MB_ICONEXCLAMATION**.

After compilation, a C program that creates a dialog box can be run as usual from the command line. Additionally, it can be run by a double-click on its executable file icon – but this will open both a Command Prompt window and the dialog box. But the GNU C Compiler has a special **-mwindows** option that can be added at the very end of the compilation command to suppress the Command Prompt window when the program is run by a double-click.

![image](images/forget.jpg)

Notice that the **WinMain()** function requires an integer to be returned upon completion, just like the usual **main()** function.

![image](images/hot.jpg)

Other MessageBox icon constants include **MB_ ICONERROR**, **MB_ICONQUESTION** and **MB_ICONINFORMATION**.

![image](images/commoncg.jpg)

winlotto.c

![image](images/1g.jpg)Make a copy of the previous example, **lotto.c**, and rename it as **winlotto.c**

![image](images/2g.jpg)At the start of the renamed program file, insert a further preprocessor instruction to make the WINAPI available

**#include <windows.h>**

![image](images/3g.jpg)Next, replace the line containing **int main()** with the one that communicates with the Windows operating system

**int WINAPI WinMain( HINSTANCE hInstance, HINSTANCE**

**hPrevInstance, LPSTR lpCmdLine, int nCmdShow)**

![image](images/4g.jpg)Now, replace the call to **printf()** that outputs the selected numbers with a call that displays them in a dialog box

**MessageBox(NULL, str, “Lotto Number Picker”,**

**MB_OK | MB_ICONEXCLAMATION );**

![image](images/5g.jpg)Save the program file, compile the program using the special compiler option, then run the program – both from the command line and by a double-click

![image](images/pga159_1.jpg)

![image](images/pga159_2.jpg)

![image](images/pga159_4.jpg)

![image](images/pga159_3.jpg)

![image](images/pga159_5.jpg)

![image](images/pga159_6.jpg)

**Summary**

![image](images/pgb60_1.jpg)

•A file pointer has the syntax **FILE **fp*** and can be used to open, read, write, and close files.

•The **fopen()** function that opens files must state the file location and a file mode as its two arguments.

•After completing operations on a file, that file must then be closed by the **fclose()** function.

•Individual characters are read and written with **fgetc()** and **fputc()**, but **fgets()** and **fputs()** read and write whole lines.

•The **fread()** and **fwrite()** functions can read and write entire filestreams into and out from character buffers.

•Flexibility is offered by the **fscanf()** and **fprintf()** functions that can read and write to a filestream, **stdin**, or **stdout**.

•Error messages can be written by the **perror()** function, or the **strerror()** function can write a message associated with **errno**.

•The number of seconds elapsed since the Epoch at midnight on January 1, 1970 is returned by calling **time(NULL)**.

•Members of a **tm struct** are initialized by converting the elapsed seconds count with the **localtime()** function.

•A standard date and time format is provided by the **asctime()** function, but individual components can be formatted using format specifiers with the **strftime()** function.

•Time points during the execution of a program can be established using the **difftime()** or **clock()** functions.

•The sequence of pseudo-random numbers generated by **rand()** is best first seeded with the **srand()** function and **time(NULL)**.

•Including the **windows.h** header file in a program makes the Windows API available to create graphical components.

•The entry point of a Windows program is the **WinMain()** function, and **MessageBox()** creates a simple dialog box.

11

**C reference section**

***This section of the book lists the standard ASCII key codes and every function contained in the standard C library, grouped by their header file, and also descriptions of all the standard constants.***

[**ASCII character codes**](#chapter11.xhtml_sec78)

[**Input & output functions <stdio.h>**](#chapter11.xhtml_sec79)

[**Character test functions <ctype.h>**](#chapter11.xhtml_sec80)

[**String functions <string.h>**](#chapter11.xhtml_sec81)

[**Math functions <math.h>**](#chapter11.xhtml_sec82)

[**Utility functions <stdlib.h>**](#chapter11.xhtml_sec83)

[**Diagnostic functions <assert.h>**](#chapter11.xhtml_sec84)

[**Argument functions <stdarg.h>**](#chapter11.xhtml_sec85)

[**Date & time functions <time.h>**](#chapter11.xhtml_sec86)

[**Jump functions <setjmp.h>**](#chapter11.xhtml_sec87)

[**Signal functions <signal.h>**](#chapter11.xhtml_sec88)

[**Limit constants <limits.h>**](#chapter11.xhtml_sec89)

[**Float constants <float.h>**](#chapter11.xhtml_sec90)

ASCII character codes

ASCII (American Standard Code for Information Interchange) is the standard representation of characters by numerical code. The non-printing character codes, originally developed for teletypes, are now rarely used for their intended original purpose.

There are also extended ASCII code sets from 128-255 (not listed) containing accented characters and symbols, but these sets do vary.

Note that the character represented by character code 32 is not missing – it is, in fact, the non-printing space character. Also, the character represented by character code 127 is the delete character.

| **Code** | **Char** | **Description** |
| **0** | NUL | null |
| **1** | SOH | start of heading |
| **2** | STX | start of text |
| **3** | ETX | end of text |
| **4** | EOT | end of transmission |
| **5** | ENQ | enquiry |
| **6** | ACK | acknowledgement |
| **7** | BEL | bell |
| **8** | BS | backspace |
| **9** | TAB | horizontal tab |
| **10** | NL | newline |
| **11** | VT | vertical tab |
| **12** | FF | form feed |
| **13** | CR | carriage return |
| **14** | SO | shift out |
| **15** | SI | shift in |
| **16** | DLE | data link escape |
| **17** | DC1 | device control 1 |
| **18** | DC2 | device control 2 |
| **19** | DC3 | device control 3 |
| **20** | DC4 | device control 4 |
| **21** | NAK | neg. acknowledge |
| **22** | SYN | synchronous file |
| **23** | ETB | end of trans. block |
| **24** | CAN | cancel |
| **25** | EM | end of medium |
| **26** | SUB | substitute |
| **27** | ESC | escape |
| **28** | FS | file separator |
| **29** | GS | group separator |
| **30** | RS | record separator |
| **31** | US | unit separator |

| **Code** | **Char** |
| **32** |  |
| **33** | ! |
| **34** | “ |
| **35** | # |
| **36** | $ |
| **37** | % |
| **38** | & |
| **39** | ‘ |
| **40** | ( |
| **41** | ) |
| **42** | * |
| **43** | + |
| **44** | , |
| **45** | - |
| **46** | . |
| **47** | / |
| **48** | 0 |
| **49** | 1 |
| **50** | 2 |
| **51** | 3 |
| **52** | 4 |
| **53** | 5 |
| **54** | 6 |
| **55** | 7 |
| **56** | 8 |
| **57** | 9 |
| **58** | : |
| **59** | ; |
| **60** | < |
| **61** | = |
| **62** | > |
| **63** | ? |
| **64** | @ |
| **65** | A |
| **66** | B |
| **67** | C |
| **68** | D |
| **69** | E |
| **70** | F |
| **71** | G |
| **72** | H |
| **73** | I |
| **74** | J |
| **75** | K |
| **76** | L |
| **77** | M |
| **78** | N |
| **79** | O |
| **80** | P |
| **81** | Q |
| **82** | R |
| **83** | S |
| **84** | T |
| **85** | U |
| **86** | V |
| **87** | W |
| **88** | X |
| **89** | Y |
| **90** | Z |
| **91** | [ |
| **92** | \ |
| **93** | ] |
| **94** | ^ |
| **95** | _ |
| **96** | ` |
| **97** | a |
| **98** | b |
| **99** | c |
| **100** | d |
| **101** | e |
| **102** | f |
| **103** | g |
| **104** | h |
| **105** | i |
| **106** | j |
| **107** | k |
| **108** | l |
| **109** | m |
| **110** | n |
| **111** | o |
| **112** | p |
| **113** | q |
| **114** | r |
| **115** | s |
| **116** | t |
| **117** | u |
| **118** | v |
| **119** | w |
| **120** | x |
| **121** | y |
| **122** | z |
| **123** | { |
| **124** | &#124; |
| **125** | } |
| **126** | ~ |
| **127** | del |

![image](images/hot.jpg)

To find out more about extended ASCII sets try the website at asciitable.com, or search for “ASCII” online.

![image](images/hot.jpg)

The term “ASCII file” just means a plain text file, such as those produced by Windows’ Notepad application.

**Input & output functions**

**<stdio.h>**

The functions and types defined in the **stdio.h** header file represent almost one third of the C language library. It is used to introduce data into a program and generate output from a program.

A “stream” is a data source terminated by a **\n** newline character. It may be read or written by “opening” the stream, and terminated by “closing” it. Opening a stream returns a **FILE** type pointer in which information needed to control the stream is stored.

**File-handling functions**

The functions listed in the following table perform file operations:

| **FILE fopen( const char **filename* , const char *mode* )** 
The **fopen()** function returns a **FILE** pointer, or **NULL** if the file cannot be opened. Any of the following modes may be specified in the function call: |
| **r** | open a text file for reading only |
| **w** | create a text file to write to, and discard any previous contents |
| **a** | append – open or create a text file for writing at the end of the file |
| **r+** | open a text file to update (read and write) |
| **w+** | open a text file to update (read and write, discarding any previous contents) |
| **a+** | append – open or create a text file for update, for writing at the end of the file |
| If the file being opened is a binary file, a **b** should be added after the file mode – for example, **wb+** |
| **FILE freopen( const char **filename* , const char mode , FILE **stream* )** 
The **freopen()** function opens a file with the specified mode and associates the stream with it. It returns the stream, or **NULL** if an error occurs. This function is normally used to change the files associated **stdin**, **stdout** or **stderr** |
| **int fflush( FILE **stream* )** 
On an output stream this function causes any buffered data to be written immediately. It returns the **EOF** constant for a write error, or zero otherwise. A call to **fflush( NULL )** flushes all output streams |

**<stdio.h>**

| **int fclose( FILE **stream* )** 
A call to **fclose()** flushes any unwritten data from the stream then closes the stream. It returns the **EOF** constant if an error occurs, or zero otherwise |
| **int remove( const char **filename* )** 
This function removes the specified file – so that any subsequent attempt to open that file will fail. It returns a non-zero value if it cannot remove the file |
| **int rename( const char **old-name* , const char **new-name* )** 
The **rename()** function changes the name of the specified file, or it returns a non-zero value if it cannot rename the file |
| **FILE *tmpfile( void )** 
Calling **tmpfile()** creates a temporary file, with the file mode of **wb+**, that is removed when the program ends. This function returns a stream, or **NULL** if the file cannot be created |
| **char *tmpnam( *char arr*[ *L_tmpnam* ] )** 
This function stores a string in an array and returns a unique valid name pointer to that array. The ***arr*** array must have at least ***L_tmpnam*** characters. The **tmpnam()** function generates a different name each time it is called |
| **int setvbuf( FILE **stream* , char **buffer* , int mode , size_t *size* )** 
A call to **setvbuf()** sets buffering for the specified stream. It should be called after a stream has been opened but before any operation has been performed on it. Valid modes are **_IOFBF** to cause full buffering, **_IOLBF** for line buffering, and **_IONBF** for no buffering. The ***size*** sets the buffer size. This function returns a non-zero value if an error occurs |
| **void setbuf( FILE **stream* , char **buffer* )** 
The **setbuf()** function defines how a stream should be buffered. It should be called after a stream has been opened but before any operation has been performed on it. The argument ***buffer*** points to an array to be used as the buffer |

**<stdio.h>**

**Functions that format output**

| **int fprintf( FILE **stream* , const char **format* , ... )** 
The **fprintf()** function converts and writes output to a specified filestream under the control of a format specifier. It returns the number of characters written, or a negative value if an error occurs |
| **int printf( const char **format* , ... )** 
The **printf()** function writes and converts output to **stdout**. It is equivalent to **fprintf( stdout , const char **format* )** |
| **int sprintf( char *s , const char **format* , ... )** 
The **sprintf()** function is the same as **printf()** except the output is written into the specified string, and terminated with a **\0** null character |
| **vprintf( const char **format* va_list *arg* )** **vfprintf( FILE **stream* , const char **format* , va_list *arg* )**
**vsprintf( char **s* , const char **format* , va_list *arg* )**

These three functions are equivalent to the corresponding **printf()** functions except that their variable argument list is replaced by an argument of the **va_list** type. Refer to the **stdarg.h** header file functions [here](#chapter11.xhtml_sec85) for more details |

Functions that format input

| **int fscanf( FILE **stream* , const char **format* , ... )** 
The **fscanf()** function reads from a specified stream under the control of a format specifier and assigns converted values to subsequent arguments. It returns the number of input items converted or the **EOF** constant if the end of the file is met, or if an error occurs |
| **int scanf( const char **format* , ... )** 
The **scanf()** function reads and converts input to **stdin**. It is equivalent to **fscanf( stdin , const char **format* )** |
| **int sscanf( char **s* , const char **format* , ... )**  The **sscanf()** function is the same as **scanf()** except the input is read from the specified string |

**<stdio.h>**

Format specifiers for output

In C, a **%** prefix denotes a format specifier. All **printf()** format specifiers are listed below, and those for **scanf()** [here](#chapter11.xhtml_forsp).

| **Character** | **printf() Converts To** |
| **d , i** | **int** data type, signed decimal |
| **o** | int data type, unsigned octal without a leading zero |
| **x , X** | **int** unsigned hexadecimal. **0x** uses lowercase, such as **0xff**, and **0X** uses uppercase, such as **0XFF** |
| **u** | **int** data type, unsigned decimal |
| **c** | **int** single character, after conversion to **char** data type |
| **s** | **char** pointer to string, ending with the **\0** null character |
| **f** | **double** data type in the form xxx.yyyyyy where the number of digits after the decimal point is set by precision. The default precision is 6 digits |
| **e , E** | **double** data type in the form xx.yyyyyye±zz or xx.yyyyyyE±zz where the number of digits after the decimal point is set by precision. The default precision is 6 digits |
| **g , G** | **double** data type printed as %e or %E conversion or %f conversion, whichever is shorter |
| **p** | the memory address of a pointer |
| **n** | not a conversion, but stores the number of characters written so far by the call to the **printf()** function in an int pointer argument |
| **%** | not a conversion; prints a % |

**<stdio.h>**

**Format specifiers for input**

| **Character** | **scanf() Converts To** |
| **d** | **int** data type, signed decimal integer |
| **i** | **int** data type, which may be in octal (leading **0**) or hexadecimal (leading **0x** or **0X**) |
| **o** | **int** data type, octal integer with or without a leading zero |
| **u** | **int** data type, unsigned decimal |
| **x** | **int** hexadecimal integer, with or without leading **0x** or **0X** |
| **c** | **char** characters, into a specified array. Reads the number of characters stated in its width field (default is 1) without adding a final **\0** null character. Stops reading when a space is met |
| **s** | a string of non-whitespace **char** characters into an array. The array must be big enough for all the characters plus a final **\0** null character |
| **e , f , g** | **float** data type, optionally beginning with a sign, then followed by a string of numbers. These may contain a decimal point, and an optional exponent field containing an “E” or “e” followed by a possibly signed integer |
| **p** | a memory address, in the same form as that output by the **%p** conversion with **printf()** |
| **n** | not a conversion, but stores the number of characters read so far by the call to **scanf()** function in an **int** pointer argument |
| **[...]** | matches a string specified in the square brackets to those in the input stream and adds a **\0** null character |
| **[^...]** | matches all ASCII characters in the input stream except those specified in the square brackets, and adds a **\0** null character |

**<stdio.h>**

**Functions for character input and output**

| **int fgetc( FILE **stream* )** Returns the next character of the specified stream as a **char**, or the **EOF** constant if at the end of the file or if an error occurs |
| **char *fgets( char **s* , int *n* , FILE **stream* )** Reads the next ***n*** -1 characters into the specified stream then adds a **\0** null character at the end of the array. This function returns ***s***, or **NULL** if at the end of the file or if an error occurs |
| **int fputc( int *c* , FILE **stream* )** Writes the character ***c*** to the specified stream and returns the character written or **EOF** if an error occurs |
| **int fputs( const char **s* , FILE **stream* )** Writes the string ***s*** to the specified stream and returns a non-negative value, or **EOF** if an error occurs |
| **int getc( FILE **stream* )** The **getc()** function is the macro equivalent of **fgetc()** |
| **int getchar( void )** The **getchar()** function is equivalent to **getc( stdin )** |
| **char *gets( char **s* )** Reads the next input line into an array, replacing its final newline character with a **\0** null character. It returns ***s***, or **NULL** if at the end of the file or if an error occurs |
| **int putc( int *c* , FILE **stream* )** The **putc()** function is the macro equivalent of **fputc()** |
| **int putchar( int c )** is equivalent to **putc( *c* , stdout )** |
| **int puts( const char **s* )** Writes the string ***s*** and a newline character to **stdout**. It returns a non-negative value, or **EOF** if an error occurs |
| **int ungetc( int *c* , FILE **stream* )** Pushes the character ***c*** back onto the specified stream where it is returned on the next read. Only one pushback character per stream is guaranteed and **EOF** cannot be pushed back. This function returns the character pushed back, or **EOF** if an error occurs |

**<stdio.h>**

**Functions for direct stream input and output**

The **fread()** and **fwrite()** functions contained in the **stdio.h** header file are most effective to read and write entire text files:

| **size_t fread( void **ptr* , size_t *size* , size_t *nobj* , FILE **stream* )** 
The **fread()** function reads from the specified stream into the specified ***ptr*** array pointer at most ***nobj*** objects of ***size*** size. This function returns the number of objects it has read, which may be less than the number requested in the function call.

The status of **fread()** can be tested as it proceeds using the **feof()** function and **ferror()** functions – see the error functions listed [here](#chapter11.xhtml_errf) |
| **size_t fwrite(const void **ptr*, size_t *size*, size_t *nobj*, FILE **stream*)** 
The **fwrite()** function writes from the specified ***ptr*** pointer ***nobj*** objects of ***size*** size. It returns the number of objects that it has written. If an error occurs, the returned value will be less than that requested by ***nobj*** in the function call |

**<stdio.h>**

**Error functions**

Many of the standard functions in the C library set status indicators when an error occurs, or when the end of a file is reached. These indicators can be tested using the error functions listed in the table below. Also, the integer expression **errno**, defined in the **errno.h** header file, may contain an error code giving more information about the most recent error.

| **void clearerr( FILE **stream* )** 
The **clearerr()** function clears the end of file and error indicators for the specified stream |
| **int feof( FILE **stream* )** 
The **feof()** function returns a non-zero value if the end of file indicator is set for the specified stream |
| **int ferror( FILE **stream* )** 
The **ferror()** function returns a non-zero value if the error indicator is set for the specified stream |
| **void perror( const char **s* )** 
The **perror()** function prints an implementation-defined error message associated with the integer value contained in the **errno** expression. See also the **strerror()** function in the **string.h** header file |

**<stdio.h>**

**File-positioning functions**

A filestream is processed by moving through the characters it contains, one by one. The functions in the following table can be used to manipulate the position in the filestream:

| **int fseek( FILE **stream* , long *offset* , int *original* )** 
The **fseek()** function sets the file position in the specified stream. Subsequent reading or writing begins at the new position. The new position is determined by specifying how far to ***offset*** the position from its ***original*** position. Optionally, the third argument of this function can be specified as **SEEK_SET** (beginning), **SEEK_CUR** (current position), or **SEEK_END** (end of file). For a text stream the offset must be either zero or a value returned by the **ftell()** function, with the original position specified as **SEEK_SET**. The **fseek()** function returns non-zero if an error occurs |
| **long ftell( FILE **stream* )** 
The **ftell()** function returns the current file position of the specified stream, or -1 if an error occurs |
| **int fgetpos( FILE **stream* , fpos_t **ptr* )** 
The **fgetpos()** function records the current file position of the specified stream in the specified ***ptr*** pointer as a special **fpos_t** type. This function returns a non-zero value if an error occurs |
| **int fsetpos( FILE **stream* , const fpos_t **ptr* )** 
The **fsetpos()** function positions the file pointer in the specified stream at the position recorded by **fgetpos()** in the ***ptr*** pointer. This function returns a non-zero value if an error occurs |

Character test functions

<ctype.h>

The **ctype.h** header file contains functions for testing characters. In each case, the character must be specified as the function’s argument. The function returns a non-zero value (true) when the tested condition is met, or zero (false) if it is not. Additionally, this header file contains two functions for converting the case of letters. All the functions in the **ctype.h** header file are listed in the table below, together with a description of their purpose:

| **Function** | **Description** |
| **isalpha( *c* )** | is the character a letter? |
| **isalnum( *c* )** | is the character a letter or a number? |
| **iscntrl( *c* )** | is the character a control character? |
| **isdigit( *c* )** | is the character a decimal digit? |
| **isgraph( *c* )** | is the character any printing character except a space? |
| **islower( *c* )** | is the character a lowercase letter? |
| **isprint( *c* )** | is the character any printing character including a space? |
| **ispunct( *c* )** | is the character any printing character except a space, a letter, or a digit? |
| **isspace( *c* )** | is the character a space, formfeed, newline, carriage return, horizontal tab, or vertical tab? |
| **isupper( *c* )** | is the character an uppercase letter? |
| **isxdigit( *c* )** | is the character a hexadecimal digit? |
| **int tolower( int c )** | convert the character to lowercase |
| **int toupper( int *c* )** | convert the character to uppercase |

**String functions**

**<string.h>**

The **string.h** header file contains the following functions that can be used to compare and manipulate text strings:

| **Function** | **Description** |
| **char *strcpy( *s1* , *s2* )** | copy ***s2*** to ***s1***, then return ***s1*** |
| **char *strncpy( *s1* , *s2* , *n* )** | copy ***n*** characters of ***s2*** to ***s1***, then return ***s1*** |
| **char *strcat( *s1* , *s2* )** | concatenate ***s2*** to the end of ***s1***, then return ***s1*** |
| **char *strncat( *s1* , *s2* , *n* )** | concatenate ***n*** characters of ***s2*** to the end of ***s1***, then return ***s1*** |
| **int strcmp( *s1* , *s2* )** | compare ***s1*** to ***s2***, then return **< 0** if ***s1* < *s2***,
or **0** if ***s1* == *s2***,
or **> 0** if ***s1* > *s2*** |
| **int strncmp( *s1* , *s2* , *n* )** | compare ***n*** characters of ***s1*** to ***s2***, then return **< 0** if ***s1* < *s2***,
or **0** if ***s1* == *s2***,
or **> 0** if ***s1* > *s2*** |
| **char *strchr( *s* , *c* )** | return a pointer to the first occurrence of ***c*** in ***s***, or **NULL** if not present |
| **char *strrchr( *s* , *c* )** | return a pointer to the last occurrence of ***c*** in ***s***, or **NULL** if not present |
| **size_t strspn( *s1* , *s2* )** | return length of prefix of ***s1*** consisting of characters in ***s2*** |
| **size_t strcspn( *s1* , *s2* )** | return length of prefix of ***s1*** consisting of characters not in ***s2*** |
| **char *strpbrk( *s1 , s2* )** | return a pointer to the first occurrence in ***s1*** of any character of ***s2***, or **NULL** if none are present |
| **char *strstr( *s1 , s2* )** | return a pointer to the first occurrence of ***s2*** in ***s1***, or **NULL** if not present |
| **size_t strlen( *s* )** | return the length of ***s*** |
| **char *strerror( *n* )** | return a pointer to the implementation-defined string associated with error code ***n*** |
| **char *strtok( *s1 , s2* )** | search ***s1*** for tokens delimited by characters from ***s2*** |
| **void *memcpy( *s1 , s2 , n* )** | copy ***n*** characters from ***s2*** to ***s1***, then return ***s1*** |
| **void *memmove( *s1 , s2 , n* )** | same as **memcpy()** but it also works even when the objects overlap |
| **int memcmp( *s1 , s2 , n* )** | compare the first ***n*** characters of ***s1*** with ***s2***; return as with the **strcmp()** function |
| **void *memchr( *s , c , n* )** | return a pointer to the first occurrence of character ***c*** in ***s***, or return **NULL** if not present in the first ***n*** characters |
| **void *memset( *s , c , n* )** | place character ***c*** into the first ***n*** characters of ***s***, then return ***s*** |

**Math functions**

**<math.h>**

The **math.h** header file contains functions that perform mathematical calculations. All the functions are listed in the table below, together with a description of the calculation they perform. In the table *x* and *y* are double data types, and *n* is an *int* data type. All the functions return the result of their calculation as a *double* data type:

| **Function** | **Description** |
| **sin( *x* )** | return the sine of ***x*** |
| **cos( *x* )** | return the cosine of ***x*** |
| **tan( *x* )** | return the tangent of ***x*** |
| **asin( *x* )** | return the arcsine of ***x*** |
| **acos( *x* )** | return the arccosine of ***x*** |
| **atan( *x* )** | return the arctangent of ***x*** |
| **atan2( *y , x* )** | return the angle (in radians) from the ***x*** axis to a point ***y*** |
| **sinh( *x* )** | return the hyperbolic sine of ***x*** |
| **cosh( *x* )** | return the hyperbolic cosine of ***x*** |
| **tanh( *x* )** | return the hyperbolic tangent of ***x*** |
| **exp( *x* )** | return e (the base of natural logarithms) raised to the power ***x*** |
| **log( *x* )** | return the natural logarithm of ***x*** |
| **log10( *x* )** | return the base 10 logarithm of ***x*** |
| **pow( *x , y* )** | return ***x*** raised to the power ***y*** |
| **sqrt( *x* )** | return the square root of ***x*** |
| **ceil( *x* )** | return the smallest integer not less than ***x*** , as a double |
| **floor( *x* )** | return the largest integer not greater than **x** , as a double |
| **fabs( *x* )** | return the absolute value of ***x*** |
| **ldexp( *x , n* )** | return ***x*** multiplied by 2 and raised to the power ***n*** |
| **frexp( *x* , int **exp* )** | decompose ***x*** into two parts – return a mantissa between 0.5 and 1, and store exponent in ***exp*** |
| **modf( *x* , double **ip* )** | split ***x*** into integer and fraction – return the fractional part, and store the integral part in ***ip*** |
| **fmod( *x , y* )** | return the remainder of ***x*** divided by ***y*** |

**Utility functions**

**<stdlib.h>**

Functions that perform various useful tasks

| **double atof( const char **s* )** Converts ***s*** to a **double** |
| **int atoi( const char **s* )** Converts ***s*** to an **int** |
| **long atol( const char **s* )** Converts ***s*** to a **long** |
| **double strtod( const char **s* , char ***endp* )** Converts the initial part of ***s*** to a **double**, ignoring leading whitespace. A pointer to the rest of ***s*** is stored in ****endp*** |
| **long strtol( const char **s* , char ***endp*, int *b* )** Converts the initial part of ***s*** to a **long** using base ***b***. A pointer to the rest of ***s*** is stored in ****endp*** |
| **unsigned long strtoul( const char **s* , char ***endp* , int *b* )** This function is the same as the **strtol()** function except the returned result is an **unsigned long** |
| **int rand( void )** Returns a pseudo-random number between zero and an implementation-defined maximum of at least 32,767 |
| **void srand( unsigned int *seed* )** Sets the seed for a new sequence of random numbers supplied by **rand()**. The initial seed is 1 |
| **void *calloc( size_t *nobj* , size_t *size* )** Returns a pointer to memory space for an array of ***nobj*** objects of ***size*** size, or **NULL** if the request cannot be met. The space is initialized to zero bytes |
| **void *malloc( size_t *size* )** Returns a pointer to memory space for an object of ***size*** size, or **NULL** if the request fails. This space is uninitialized |
| **void *realloc( void **p* , size_t *size* )** Changes the size of an object pointed to by ***p*** to ***size*** size. This function returns a pointer to the new space, or **NULL** if the request fails |
| **void *free( void **p* )** The **free()** function deallocates the memory space pointed to by ***p***. Note that ***p*** must be a pointer to memory space previously allocated by **calloc()**, **malloc()**, or **realloc()** |
| **void abort( void )** Causes the program to end abnormally |
| **void exit( int *status* )** Causes the program to end normally. The value of ***status*** is returned to the system. Optionally, **EXIT_SUCCESS** and **EXIT_FAILURE** can be used to specify the ***status*** values |
| **int atexit( void ( **fcn* ) ( void ) )** Registers the ***fcn*** function to be called when the program terminates. **atexit()** returns a non-zero value if unsuccessful |
| **int system( const char **s* )** Passes the string ***s*** to the environment for processing. The return value is implementation-dependent |
| **char *getenv( const char **name* )** Returns the environment string associated with ***name***, or **NULL** if no string is associated with ***name*** in that environment. The details are implementation-dependent |
| **void *bsearch( const void **key* , const void **base* , size_t *n* , size_t *size* , int ( *cmp ) , ( const void **keyval* , const void **datum* ) )** 
Searches ***base*[0]**...***base*[ *n*-1 ]** for an item that matches ***key***. It returns a pointer to the matching item if successful, otherwise it returns a **NULL** value. Items in the array base must be in ascending order |
| **void qsort( void **base* , size_t *n* , size_t *size* ,** **int ( *cmp ) ( const void * , const void * ) )** 
Sorts into ascending order an array ***base*[0]**...***base*[ *n*-1 ]** of objects of ***size*** size. The comparison function **cmp()** is the same as that in the **bsearch()** function |
| **int abs( int *n* )** Returns the absolute value of **int *n*** |
| **long labs( long *n* )** Returns the absolute value of **long *n*** |
| **div_t ldiv( long *num* , long *denom* )** Divides ***num*** by ***denom*** and stores the result as members of a structure of type **ldiv_t**. Its **quot** member stores the quotient result and its **rem** member stores the remainder result |

**Diagnostic functions**

**<assert.h>**

The **assert()** function, contained in the **assert.h** header file, can be used to add diagnostics to a program:

**void assert( int *expression* ) ;**

If ***expression*** is zero when **assert( *expression* )** is executed the function will print a message on **stderr**, such as:

**Assertion failed: *expression* , file *filename* , line *n***

The **assert()** function then attempts to terminate the program.

**Argument functions**

**<stdarg.h>**

The **stdarg.h** header file contains functions that can be used to step through a list of function arguments without first knowing their number and type. Due to the nature of these functions they must be implemented as “macros” within the function body.

The list of arguments is assigned to a special data type named **va_list**. The functions listed in the following table manipulate a variable named “args” of the **va_list** type:

| **va_start( va_list *args* , *lastarg* )** 
Must be called once to initialize the **va_list** named ***args*** at the position in the list of the last known argument ***lastarg*** |
| **va_arg( va_list *args* , *data-type* )** 
After **va_list *args*** has been initialized by **va_start()** each successive call to **va_arg()** will return the value of the next argument in the ***args*** list as the specified ***data-type*** |
| **va_end( va_list *args* )** 
Must be called once after the arguments in the **va_list *args*** have been processed, before the function is exited |

**Date & time functions**

**<time.h>**

The **time.h** header file contains functions for manipulating date and time. Some of these functions process “Calendar time”, which is based on the Gregorian calendar. This is stated in seconds elapsed since the Epoch (00:00:00 GMT January 1st, 1970).

Other functions contained in **time.h** process “Local time”, which is the translation of Calendar time accounting for time zone.

The data type **time_t** is used to describe both Calendar time and Local time.

A struct named **tm** contains the components of Calendar time, which are listed in the table below:

| **Component** | **Description** |
| **int tm_sec** | seconds after the minute, 0-61 |
| **int tm_min** | minutes after the hour, 0-59 |
| **int tm_hour** | hours since midnight, 0-23 |
| **int tm_mday** | day of the month, 1-31 |
| **int tm_mon** | months since January, 0-11 |
| **int tm_year** | years since 1900 |
| **int tm_wday** | days since Sunday, 0-6 |
| **int tm_yday** | days since January 1st, 0-365 |
| **int tm_isdst** | Daylight Saving Time flag |

The **tm_isdst** component is positive if Daylight Saving is in effect, zero if it is not, or negative if the information is unavailable.

The functions contained in the **time.h** header file are listed in the table [here](#chapter11.xhtml_page-182).

The **time.h** header file contains the functions listed below that can be used to manipulate date and time:

| **clock_t clock( void )** Returns the processor time used by the program since it started, or -1 if unavailable |
| **time_t time( time_t **tp* )** Returns the current calendar time, or -1 if unavailable |
| **double difftime( time_t *time2* , time_t *time1* )** Returns ***time2*** minus ***time1***, expressed in seconds |
| **time_t mktime( struct tm **tp* )** Converts the local time in the structure ****tp*** into calendar time |
| **char *asctime( const struct tm **tp* )** Converts the time in the struct ****tp*** into a standard string |
| **char *ctime( const time_t **tp* )** Converts calendar time to local time |
| **struct tm *gmtime( const time_t **tp* )** Converts calendar time into Co-ordinated Universal Time (UTC or GMT) |
| **struct tm *localtime( const time_t **tp* )** Converts the calendar time ****tp*** into local time |
| **size_t strftime( char **s* , size_t *smax* , const char **fmt* ,** **const struct tm **tp* )** 
Formats the time ****tp*** into a chosen format *fmt |

The **strftime()** function formats selected components of the **tm** structure according to the stated format specifier. All the possible format specifiers are listed in the table [here](#chapter11.xhtml_page-183).

| **Specifier** | **Description** |
| **%a** | abbreviated weekday name |
| **%A** | full weekday name |
| **%b** | abbreviated month name |
| **%B** | full month name |
| **%c** | local date and time representation |
| **%d** | day of the month, 01-31 |
| **%H** | hour (24-hour clock), 00-23 |
| **%I** | hour (12-hour clock), 01-12 |
| **%j** | day of the year, 001-366 |
| **%m** | month of the year, 01-12 |
| **%M** | minute, 00-59 |
| **%p** | local equivalent of AM or PM |
| **%S** | second, 00-61 (to account for leap seconds) |
| **%U** | week number of the year (Sunday as the first day of the week), 00-53 |
| **%w** | weekday number, 0-6 (Sunday is 0) |
| **%W** | week number of the year (Monday as the first day of the week), 00-53 |
| **%x** | local date representation |
| **%X** | local time representation |
| **%y** | year without century, 00-99 |
| **%Y** | year with century |
| **%Z** | time zone name, if available |

**Jump functions**

**<setjmp.h>**

The **setjmp.h** header is used for controlling low-level calls and provides a means to avoid the normal call and return sequence.

| **int setjmp( jmp_buf *env* )** |
| Low-level function used in conditional tests to save the environment in the ***env*** variable, then return zero |
| **void longjmp( jmp_buf *env* , int *value* )** |
| Restores an environment that has been saved in the ***env*** variable by **setjmp()**, as if **setjmp()** had returned the ***value*** |

**Signal functions**

**<signal.h>**

The **signal.h** header contains functions for handling exceptional conditions that may arise during the execution of a program:

| **void ( *signal ( int *sig* , void ( **handler* ) ( int ) ) ) ( int )** The **signal()** function specifies how subsequent signals will be handled. The handler can be **SIG_DFL**, an implementation-defined default; or **SIG_IGN**, to ignore the signal. Valid ***sig*** signals include: |
| **SIGABRT** : abort termination |
| **SIGFPE** : arithmetic error |
| **SIGILL** : illegal instruction |
| **SIGINT** : external interruption |
| **SIGSEGV** : access outside memory limit |
| **SIGTERM** : termination request sent to the program |
| The function returns the previous value of the handler for that specific signal, or **SIG_ERR** if an error occurs. When a ***sig*** signal next occurs, the signal is restored to its default behavior then the signal handler is called. If this returns, execution resumes at the point where the signal occurred |
| **int raise( int *sig* )** Attempts to send the ***sig*** signal to the program and returns a non-zero value if the attempt is unsuccessful |

**Limit constants**

**<limits.h>**

The table below lists constants related to maximum and minimum numerical limits. Their values vary according to implementation. Where a value is given, in brackets, it indicates a minimum size for that constant – but larger values may, in fact, be imposed. Programs should not assume that any implementation-dependent constant will be of a particular value.

| **Constant** | **Value** |
| **CHAR_BIT** | number of bits in a **char** (8) |
| **CHAR_MAX** | maximum value of **char** (**UCHAR_MAX** or **SCHAR_MAX**) |
| **CHAR_MIN** | minimum value of char (zero or **SCHAR_MIN**) |
| **INT_MAX** | maximum value of **int** (+32,767) |
| **INT_MIN** | minimum value of **int** (-32,767) |
| **LONG_MAX** | maximum value of **long** (+2,147,483,647) |
| **LONG_MIN** | minimum value of **long** (-2,147,483,647) |
| **SCHAR_MAX** | maximum value of **signed char** (+127) |
| **SCHAR_MIN** | minimum value of **signed char** (-127) |
| **SHRT_MAX** | maximum value of **short** (+32,767) |
| **SHRT_MIN** | minimum value of **short** (-32,767) |
| **UCHAR_MAX** | maximum value of **unsigned char** (+255) |
| **UINT_MAX** | maximum value of **unsigned int** (+65,535) |
| **ULONG_MAX** | maximum value of **unsigned long** (+4,294,967,295) |
| **USHRT_MAX** | maximum value of **unsigned short** (+65, 535) |

**Float constants**

**<float.h>**

The table below lists constants related to floating-point arithmetic. Their values vary according to implementation. Where a value is given, in brackets, it indicates a minimum size for that constant.

| **Constant** | **Value** |
| **FLT_RADIX** | radix of float exponent representations (2) |
| **FLT_ROUNDS** | rounding to the nearest number |
| **FLT_DIG** | number of precision digits (5) |
| **FLT_EPSILON** | smallest number x, where 1.0 + x != 1.0 (1E-5) |
| **FLT_MANT_DIG** | number of **FLT_RADIX** mantissa digits |
| **FLT_MAX** | maximum floating-point number (1E+37) |
| **FLT_MAX_EXP** | largest number n, where **FLT_RADIX**^n-1 is a valid number |
| **FLT_MIN** | minimum floating-point number (1E-37) |
| **FLT_MIN_EXP** | smallest number n, where 10^n is valid |
| **DBL_DIG** | number of double-precision digits (10) |
| **DBL_EPSILON** | smallest number x, where 1.0 + x != 1.0 (1E-9) |
| **DBL_MANT_DIG** | number of **FLT_RADIX** mantissa digits |
| **DBL_MAX** | maximum double float number (1E+37) |
| **DBL_MAX_EXP** | largest number n, where **FLT_RADIX**^n-1 is a valid number |
| **DBL_MIN** | minimum double float number (1E-37) |
| **DBL_MIN_EXP** | smallest number n, where 10^n is valid |

12

**Getting started with C++**

***Welcome to the exciting world of C++ programming. This chapter demonstrates how to create a simple C++ program and how to store data within a program.***

[Introducing C++](#chapter12.xhtml_sec91)

[Installing a compiler](#chapter12.xhtml_sec92)

[Writing your first program](#chapter12.xhtml_sec93)

[Compiling & running programs](#chapter12.xhtml_sec94)

[Creating variables](#chapter12.xhtml_sec95)

[Employing variable arrays](#chapter12.xhtml_sec96)

[Employing vector arrays](#chapter12.xhtml_sec97)

[Declaring constants](#chapter12.xhtml_sec98)

[Summary](#chapter12.xhtml_sec99)

**Introducing C++**

C++ is an extension of the C programming language that was first implemented on the UNIX operating system by Dennis Ritchie way back in 1972\. C is a flexible programming language that remains popular today, and is used on a large number of platforms for everything from microcontrollers to the most advanced scientific systems.

![image](images/pgb8_1.jpg)

C++ was developed by Dr. Bjarne Stroustrup between 1983 and 1985 while working at AT&T Bell Labs in New Jersey. He added features to the original C language to produce what he called “C with classes”. These classes define programming objects with specific features that transform the procedural nature of C into the object-oriented programming language of C++.

The C programming language was so named as it succeeded an earlier programming language named “B” that had been introduced around 1970\. The name “C++” displays some programmers’ humor because the programming ++ increment operator denotes that C++ is an extension of the C language.

C++, like C, is not platform-dependent, so programs can be created on any operating system. Most illustrations in this book depict output on the Windows operating system purely because it is the most widely used desktop platform. The examples can also be created on other platforms such as Linux or macOS.

![image](images/hot.jpg)

A powerful programming language (pronounced “see plus plus”), designed to let you express ideas.

Why learn C++ programming?

The C++ language is favored by many professional programmers because it allows them to create fast, compact programs that are robust and portable.

Using a modern C++ Integrated Development Environment (IDE), such as Microsoft’s Visual Studio Community Edition, the programmer can quickly create complex applications. But to use these tools to greatest effect, the programmer must first learn quite a bit about the C++ language itself.

This section of the book is an introduction to programming with C++, giving examples of program code and its output to demonstrate the basics of this powerful language.

![image](images/forget.jpg)

Microsoft’s free Visual Studio Community Edition IDE is used in this book to demonstrate visual programming.

Should I learn C first?

Opinion is divided on the question of whether it is an advantage to be familiar with C programming before moving on to C++. It would seem logical to learn the original language first in order to understand the larger extended language more readily. However, C++ is not simply a larger version of C, as the approach to object-oriented programming with C++ is markedly different to the procedural nature of C. It is, therefore, arguably better to learn C++ without previous knowledge of C to avoid confusion.

This section of the book makes no assumption that the reader has previous knowledge of any programming language, so it is suitable for the beginner to programming in C++, whether they know C or not.

If you do feel that you would benefit from learning to program in C before moving on to C++, we recommend you try the examples in the C section of this book before moving on to this C++ section.

![image](images/snake.jpg)

In addition to the C keywords listed [here](#chapter01.xhtml_keyw), C++ has the extra keywords listed below. All keywords have special significance and may not be used for other purposes.

| **Extra C++ Keywords** |
| **catch** | **private** |
| **class** | **protected** |
| **delete** | **public** |
| **friend** | **template** |
| **mutable** | **this** |
| **new** | **throw** |
| **operator** | **virtual** |

Standardization of C++

As the C++ programming language gained in popularity, it was adopted by many programmers around the world as their programming language of choice. Some of these programmers began to add their own extensions to the language, so it became necessary to agree upon a precise version of C++ that could be commonly shared internationally by all programmers.

A standard version of C++ was defined by a joint committee of the American National Standards Institute (ANSI) and the Industry Organization for Standardization (ISO). This version is sometimes known as ANSI C++, and is portable to any platform and to any development environment.

The examples given in this section conform to ANSI C++. Example programs run in a console window, such as the Command Prompt window on Windows systems or a shell terminal window on Linux systems, to demonstrate the mechanics of the C++ language itself. An example in [Chapter 21](#chapter21.xhtml) illustrates how code generated automatically by a visual development tool on the Windows platform can, once you’re familiar with the C++ language, be edited to create a graphical, windowed application.

![image](images/hot.jpg)

“ISO” is not an acronym but is derived from the Greek word “isos” meaning “equal” – as in “isometric”.

**Installing a compiler**

C++ programs are initially created as plain text files, saved with the file extension of “.cpp”. These can be written in any text editor, such as Windows’ Notepad application or the Vi editor on Linux.

In order to execute a C++ program, it must first be “compiled” into byte code that can be understood by the computer. A C++ compiler reads the text version of the program and translates it into a second file – in machine-readable, executable format.

Should the text program contain any syntax errors, these will be reported by the compiler and the executable file will not be built.

If you are using the Windows platform and have a C++ Integrated Development Environment (IDE) installed, then you will already have a C++ compiler available, as the compiler is an integral part of the visual IDE. The excellent, free Microsoft Visual C++ Express IDE provides an editor window, where the program code can be written, and buttons to compile and execute the program. Visual IDEs can, however, seem unwieldy when starting out with C++ because they always create a large number of “project” files that are used by advanced programs.

The popular free GNU Compiler Collection, which includes a C Compiler, is included with most distributions of the Linux operating system. The GNU C++ Compiler is also available for Windows platforms and is used to compile examples throughout the C and C++ sections of this book.

To discover if you already have the GNU C++ Compiler on your system, type **c++ -v** at a command prompt then hit **Return**. If it’s available, the compiler will respond with version information. If you are using the Linux platform and the GNU C++ Compiler is not available on your computer, install it from the distribution disc, download it from the GNU website, or ask your system administrator to install it.

The GNU (pronounced “guh-new”) Project was launched back in 1984 to develop a complete free Unix-like operating system. Part of GNU is “Minimalist GNU for Windows” (MinGW). MinGW includes the GNU C++ Compiler that can be used on Windows systems to create executable C++ programs. Windows users can download and install the GNU C++ Compiler by following the instructions [here](#chapter12.xhtml_pg197).

![image](images/pgb10_1.jpg)

The GNU C++ compiler is available free under the terms and conditions of the General Public License (GPL) that can be found online at **[gnu.org/copyleft/gpl.html](http://www.gnu.org/copyleft/gpl.html)**

![image](images/hot.jpg)

To open a Windows Command Prompt, press the **Windows** + **R** keys to launch a Run dialog, then type **cmd** into the dialog and hit **Enter**.

![image](images/pgb10_2.jpg)

![image](images/pgb10_3.jpg)

![image](images/pgb10_4.jpg)

![image](images/1o.jpg)With an internet connection, launch a web browser then navigate to **[osdn.net/projects/mingw](http://osdn.net/projects/mingw)** and click the link to download the MinGW installer **mingw-get-setup.exe**

![image](images/pgb11_1.jpg)

![image](images/2o.jpg)Launch the installer setup and accept the suggested location of **C:\MinGW** in the “Installation Manager” dialog

![image](images/3o.jpg)Check the **Basic MinGW** and **C++ Compiler** items, then click **Installation**, **Apply Changes**, **Apply** to install

![image](images/pgb11_2.jpg)

The MinGW C++ Compiler is a binary executable file located at **C:\MinGW\bin**. To allow it to be accessible from any system location, this folder should now be added to the System Path:

![image](images/4o.jpg)Open Windows’ “System Properties” dialog, then select the **Advanced** tab and click the **Environment Variables** button – to open the “Environment Variables” dialog

![image](images/5o.jpg)Select the **Path** system variable, then click the **Edit** button and add the location **C:\MinGW\bin;**

![image](images/6o.jpg)Click **OK** to close each dialog, then open a Command Prompt window and enter the command **c++**. If the installation is successful, the compiler should respond that you have not specified any input files for compilation:

![image](images/pgb11_3.jpg)

![image](images/hot.jpg)

To open a System Properties dialog, press the **Windows** + **R** keys to launch a Run dialog, then type **sysdm.cpl** into the dialog and hit **Enter**.

![image](images/pgb10_2.jpg)

![image](images/pgb10_3.jpg)

![image](images/pgb11_6.jpg)

**Writing your first program**

Follow these steps, copying the code exactly as it is listed, to create a simple C++ program that will output the traditional first program greeting:

![image](images/commono.jpg)

hello.cpp

![image](images/1o.jpg)Open a plain text editor, such as Windows’ Notepad, then type these “preprocessor directives”

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)A few lines below the preprocessor directives, add a “comment” describing the program

**// A C++ Program to output a greeting.**

![image](images/3o.jpg)Below the comment, add a “main function” declaration to contain the program statements

**int main()**

**{**

**}**

![image](images/4o.jpg)Between the curly brackets (braces) of the main function, insert this output “statement”

**cout << “Hello World!” << endl ;**

![image](images/5o.jpg)Next, insert a final “return” statement in the main function

**return 0 ;**

![image](images/6o.jpg)Save the program to any convenient location as “hello.cpp” – the complete program should look like this:

![image](images/pgb12_1.jpg)

![image](images/forget.jpg)

Comments throughout this book are shown in green – to differentiate them from other code.

![image](images/snake.jpg)

After typing the final closing **}** brace of the main method, always hit **Return** to add a newline character – your compiler may insist that a source file should end with a newline character.

The separate parts of the program code [here](#chapter12.xhtml_sec94) can be examined individually to understand each part more clearly:

•**Preprocessor Directives** – these are processed by the compiler before the program code, so must always appear at the start of the page. Here, the **#include** directive instructs the compiler to use the standard C++ input/output library named **iostream**, specifying the library name between **< >** angled brackets. The next line is the “using directive” that allows functions in the specified namespace to be used without their namespace prefix. Functions of the **iostream** library are within the **std** namespace – so this **using** directive allows functions such as **std::cout** and **std::endl** to be simply written as **cout** and **endl**.

•**Comments** – these should be used to make the code more easily understood by others, and by yourself when revisiting the code later. In C++ programming, everything on a single line after a **//** double-slash is ignored by the compiler.

•**Main function** – this is the mandatory entry point of every C++ program. Programs may contain many functions, but they must always contain one named **main**, otherwise the compiler will not compile the program. Optionally, the parentheses after the function name may specify a comma-separated list of “argument” values to be used by that function. Following execution, the function must return a value to the operating system of the data type specified in its declaration – in this case, an **int** (integer) value.

•**Statements** – these are the actions that the program will execute when it runs. Each statement must be terminated by a semicolon, in the same way that English language sentences must be terminated by a period (full stop). Here, the first statement calls upon the **cout** library function to output text and an **endl** carriage return. These are directed to standard output by the **<<** output stream operator. Notice that text strings in C++ must always be enclosed within double quotes. The final statement employs the C++ **return** keyword to return a zero integer value to the operating system – as required by the main function declaration. Traditionally, returning a zero value indicates that the program executed successfully.

![image](images/hot.jpg)

The C++ compiler also supports multiple-line C-style comments between /* and */ – but these should only ever be used in C++ programming to “comment-out” sections of code when debugging.

![image](images/hot.jpg)

Notice how the program code is formatted using spacing and indentation (collectively known as whitespace) to improve readability. All whitespace is ignored by the C++ compiler.

**Compiling & running programs**

The C++ source code files for the examples in this book are stored in a directory created expressly for that purpose. The directory is named “MyPrograms” – its absolute address on a Windows system is **C:\MyPrograms** and on Linux it’s **/home/*user*/MyPrograms**. You can recreate this directory to store programs awaiting compilation:

![image](images/1o.jpg)Move the “hello.cpp” program source code file, created [here](#chapter12.xhtml_sec93), to the “MyPrograms” directory on your system

![image](images/2o.jpg)At a command prompt, use the “cd” command to navigate to the “MyPrograms” directory

![image](images/3o.jpg)Enter a command to attempt to compile the program **c++ hello.cpp**

When the attempt succeeds, the compiler creates an executable file alongside the original source code file. By default, the executable file is named **a.exe** on Windows systems and **a.out** on Linux. Compiling a different source code file in the same directory would now overwrite the first executable file without warning. This is obviously undesirable, so a custom name for the executable file should be specified when compiling programs, using the compiler’s **-o** option in the compile command.

![image](images/4o.jpg)Enter a command to compile the program, creating an executable file named “hello.exe” alongside the source file **c++ hello.cpp -o hello.exe**

![image](images/pgb14_1.jpg)

![image](images/pgb15_1.jpg)

![image](images/hot.jpg)

You can see the compiler version number with the command **c++ --version** and display all its options with **c++ --help**.

![image](images/forget.jpg)

The command **c++** is an alias for the GNU C++ Compiler – the command **g++** can also be used.

![image](images/5o.jpg)To run the generated executable program file in Windows, simply enter the file name at the prompt in the “MyPrograms” directory – optionally, the file extension may be omitted. In Linux, the full file name must be used, preceded by a **./** dot-slash – as Linux does not look in the current directory unless it is explicitly directed to do so:

![image](images/pgb15_2.jpg)

![image](images/pgb15_3.jpg)

![image](images/snake.jpg)

All command line examples in the C and C++ sections of this book have been compiled and tested with the latest GNU C++ Compiler available at the time of writing – they may not replicate exactly with other compilers.

**Creating variables**

A “variable” is like a container in a C++ program in which a data value can be stored inside the computer’s memory. The stored value can be referenced using the variable’s name.

![image](images/pgb16_1.jpg)

The programmer can choose any name for a variable, providing it adheres to the C++ naming conventions – a chosen name may only contain letters, digits, and the underscore character, but cannot begin with a digit. Also, the C++ keywords, listed [here](#chapter12.xhtml_learn) must be avoided. It’s good practice to choose meaningful names to make the code more comprehensible.

To create a new variable in a program it must be “declared”, specifying the type of data it may contain and its chosen name. A variable declaration has this syntax:

***data-type variable-name ;***

Multiple variables of the same data type can be created in a single declaration as a comma-separated list with this syntax:

***data-type variable-name1 , variable-name2 , variable-name3 ;***

The five basic C++ data types are listed in the table below, together with a brief description and example content:

| **Data Type** | **Description** |
| **char** | A single byte, capable of holding one character |
| **int** | An integer whole number |
| **float** | A floating-point number, correct to six decimal places |
| **double** | A floating-point number, correct to 10 decimal places |
| **bool** | A Boolean value of **true** or **false**, or numerically zero is false and any non-zero is true |

Variable declarations must appear before executable statements – so they will be available for reference within statements.

![image](images/snake.jpg)

Names are case-sensitive in C++ – so variables named **VAR**, **Var**, and **var** are treated as three individual variables. Traditionally, C++ variable names are lowercase and seldom begin with an underscore, as some C++ libraries use that convention.

![image](images/snake.jpg)

Character values of the **char** data type must always be enclosed between single quotes – not double quotes.

When a value is assigned to a variable it is said to have been “initialized”. Optionally, a variable may be initialized in its declaration. The value stored in any initialized variable can be displayed on standard output by the **cout** function, which was used [here](#chapter12.xhtml_sec93) to display the “Hello World!” greeting.

![image](images/commono.jpg)

vars.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.
return 0 ;**

**}**

![image](images/3o.jpg)In the main function, insert statements to declare and initialize variables of various data types

**char letter ; letter = ‘A’ ;         // Declared then initialized.**

**int number ; number = 100 ;  // Declared then initialized.**

**float decimal = 7.5 ;                // Declared and initialized.**

**double pi = 3.14159 ;              // Declared and initialized.**

**bool isTrue = false ;               // Declared and initialized.**

![image](images/4o.jpg)Now, insert statements to output each stored value

**cout << “char letter: ” << letter << endl ;**

**cout << “int number: ” << number << endl ;**

**cout << “float decimal: ” << decimal << endl ;**

**cout << “double pi: ” << pi << endl ;**

**cout << “bool isTrue: ” << isTrue << endl ;**

![image](images/5o.jpg)Save, compile, and run the program to see the output

![image](images/pgb17_1.jpg)

![image](images/hot.jpg)

Always begin Boolean variable names with “is” so they are instantly recognizable as Booleans. Also, use “lowerCamelCase” for all variable names that comprise multiple words – where all except the first word begin with uppercase, like “isTrue”.

**Employing variable arrays**

An array is a variable that can store multiple items of data – unlike a regular variable, which can only store one piece of data. The pieces of data are stored sequentially in array “elements” that are numbered, starting at 0\. So, the first value is stored in element 0, the second value is stored in element 1, and so on.

![image](images/pgb18_1.jpg)

An array is declared in the same way as other variables, but additionally the size of the array must also be specified in the declaration, in square brackets following the array name. For example, the syntax to declare an array named “nums” to store six integer numbers looks like this:

**int nums[6] ;**

Optionally, an array can be initialized when it is declared by assigning values to each element as a comma-separated list enclosed by curly brackets (braces). For example:

**int nums[6] = { 0, 1, 2, 3, 4, 5 } ;**

![image](images/forget.jpg)

Array numbering starts at 0 – so the final element in an array of six elements is number 5, not number 6.

![image](images/pgb18_2.jpg)

An individual element can be referenced using the array name followed by square brackets containing the element number. This means that **nums[1]** references the second element in the example above – not the first element, as element numbering starts at 0.

Arrays can be created for any C++ data type, but each element may only contain data of the same data type. An array of characters can be used to store a string of text if the final element contains the special **\0** null character. For example:

**char name[5] = { ‘m’, ‘i’, ‘k’, ‘e’, ‘\0’ } ;**

The entire string to be referenced just by the array name. This is the principle means of working with strings in the C language, but the C++ string class, introduced in [Chapter 15](#chapter15.xhtml), is far simpler.

Collectively, the elements of an array are known as an “index”. Arrays can have more than one index – to represent multiple dimensions, rather than the single dimension of a regular array. Multi-dimensional arrays of three indices and more are uncommon, but two-dimensional arrays are useful to store grid-based information, such as coordinates. For example:

**int coords[2] [3] = { { 1, 2, 3 } , { 4, 5, 6 } } ;**

![image](images/commono.jpg)

arrays.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3o.jpg)In the main function, insert statements to declare and initialize three variable arrays

**// Declared then initialized.**

**float nums[3] ;**

**nums[0] = 1.5 ; nums[1] = 2.75 ; nums[2] = 3.25 ;**

**// Declared and initialized.**

**char name[5] = { ‘m’, ‘i’, ‘k’, ‘e’, ‘\0’ } ;**

**int coords[2] [3] = { { 1, 2, 3 } , { 4, 5, 6 } } ;**

**}**

![image](images/4o.jpg)Now, insert statements to output specific element values

**cout << “nums[0]: ” << nums[0] << endl ;**

**cout << “nums[1]: ” << nums[1] << endl ;**

**cout << “nums[2]: ” << nums[2] << endl ;**

**cout << “name[0]: ” << name[0] << endl ;**

**cout << “Text string: ” << name << endl ;**

**cout << “coords[0][2]: ” << coords[0][2] << endl ;**

**cout << “coords[1][2]: ” << coords[1][2] << endl ;**

![image](images/5o.jpg)Save, compile, and run the program to see the output

![image](images/pgb19_1.jpg)

![image](images/snake.jpg)

Where possible, variable names should not be abbreviations – abbreviated names are only used in this book’s examples due to space limitations.

![image](images/hot.jpg)

The loop structures, introduced in [Chapter 14](#chapter14.xhtml), are often used to iterate array elements.

**Employing vector arrays**

A vector is an alternative to a regular array, and has the advantage that its size can be changed as the program requires. Like regular arrays, vectors can be created for any data type, and their elements are also numbered starting at 0.

![image](images/pgb20_1.jpg)

In order to use vectors in a program, the C++ **vector** library must be added with an **#include <vector>** preprocessor directive at the start of the program. This library contains the predefined functions in the table below, which are used to work with vectors:

| **Function** | **Description** |
| **at(** *number* **)** | Gets the value contained in the specified element number |
| **back()** | Gets the value in the final element |
| **clear()** | Removes all vector elements |
| **empty()** | Returns true (1) if the vector is empty, or returns false (0) otherwise |
| **front()** | Gets the value in the first element |
| **pop_back()** | Removes the final element |
| **push_back(** *value* **)** | Adds a final element to the end of the vector, containing the specified value |
| **size()** | Gets the number of elements |

A declaration to create a vector looks like this:

**vector < *data-type* > *vector-name* ( *size* ) ;**

An **int** vector will, by default, have each element automatically initialized with a zero value. Optionally, a different initial value can be specified after the size in the declaration, with this syntax:

**vector < *data-type* > *vector-name* ( *size , initial-value* ) ;**

The functions to work with vectors are simply appended to the chosen vector name by the dot operator. For example, to get the size of a vector named “vec” you would use **vec.size()**

![image](images/forget.jpg)

Individual vector elements can be referenced using square brackets as with regular arrays, such as **vec[3]**

![image](images/commono.jpg)

vector.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <vector>          // Include vector support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return** **0** ;

**}**

![image](images/3o.jpg)In the main function, insert a statement to declare and initialize a vector array of three elements of the value 100

**vector <int> vec( 3, 100 ) ;**

![image](images/4o.jpg)Now, insert statements to manipulate the vector elements

**cout << “Vector size: ” << vec.size() << endl ;**

**cout << “Is empty?: ” << vec.empty() << endl ;**

**cout << “First element: ” << vec.at(0) << endl ;**

**vec.pop_back() ;            // Remove final element.**

**cout << “Vector size: ” << vec.size() << endl ;**

**cout << “Final element: ” << vec.back() << endl ;**

**vec.clear() ;                    // Remove all elements.**

**cout << “Vector size: ” << vec.size() << endl ;**

**vec.push_back( 200 ) ;   // Add an element.**

**cout << “Vector size: ” << vec.size() << endl ;**

**cout << “First element: ” << vec.front() << endl ;**

![image](images/5o.jpg)Save, compile, and run the program to see the output

![image](images/pgb21_1.jpg)

![image](images/hot.jpg)

The example [here](#chapter14.xhtml_sec112) shows how to use a loop to populate a vector with different initial values in each element.

**Declaring constants**

Data that will not change during the execution of a program should be stored in a constant container, rather than in a variable. This better enables the compiler to check the code for errors – if the program attempts to change the value stored in a constant, the compiler will report an error and the compilation will fail.

![image](images/pgb22_1.jpg)

A constant can be created for any data type by prefixing a variable declaration with the **const** keyword, followed by a space. Typically, constant names appear in uppercase to distinguish them from (lowercase) variable names. Unlike variables, constants must always be initialized in the declaration. For example, the declaration of a constant for the math pi value looks like this:

**const double PI = 3.1415926536 ;**

The **enum** keyword provides a handy way to create a sequence of integer constants in a concise manner. Optionally, the declaration can include a name for the sequence after the **enum** keyword. The constant names follow as a comma-separated list within braces. For example, this declaration creates a sequence of constants:

**enum suit { CLUBS , DIAMONDS , HEARTS , SPADES } ;**

Each of the constants will, by default, have a value one greater than the preceding constant in the list. Unless specified, the first constant will have a value of 0, the next a value of 1, and so on. A constant can be assigned any integer value, but the next constant in the list will always increment it by 1.

It is occasionally convenient to define a list of enumerated constants as a “custom data type” – by using the **typedef** keyword. This can begin the **enum** declaration, and a chosen type name can be added at the end of the declaration. For example, this **typedef** statement creates a custom data type named “charge”:

**typedef enum { NEGATIVE , POSITIVE } charge ;**

Variables can then be created of the custom data type in the usual way, which may legally be assigned any of the listed constants. Essentially, these variables act just like an **int** variable – as they store the numerical integer value the assigned constant represents. For example, with the example above, assigning a **POSITIVE** constant to a **charge** variable actually assigns an integer of 1.

![image](images/forget.jpg)

The **typedef** keyword simply creates a nickname for a structure.

![image](images/commono.jpg)

constant.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.
return 0 ;**

**}**

![image](images/3o.jpg)In the main function, insert statements to declare a constant, and output using the constant value

**const double PI = 3.1415926536 ;**

**cout << “6\” circle circumference: “ << (PI * 6) << endl ;**

![image](images/4o.jpg)Next, insert statements to declare an enumerated list of constants, and output using some of those constant values

**enum**

**{ RED=1, YELLOW, GREEN, BROWN, BLUE, PINK, BLACK } ;**

**cout << “I shot a red worth: ” << RED << endl ;**

**cout << “Then a blue worth: ” << BLUE << endl ;**

**cout << “Total scored: ” << ( RED + BLUE ) << endl ;**

![image](images/5o.jpg)Now, insert statements to declare a custom data type and output its assigned values

**typedef enum { NEGATIVE , POSITIVE } charge ;**

**charge neutral = NEGATIVE , live = POSITIVE ;**

**cout << “Neutral wire: ” << neutral << endl ;**

**cout << “Live wire: ” << live << endl ;**

![image](images/6o.jpg)Save, compile, and run the program to see the output

![image](images/pgb23_1.jpg)

![image](images/hot.jpg)

In the PI declaration, the ***** character is the C++ multiplication operator, and the backslash character in **\”** escapes the quote mark from recognition – so the string does not get terminated prematurely.

**Summary**

![image](images/pgb96_1.jpg)

•C++ is an object-oriented programming language that is an extension of the procedural C programming language.

•The GNU C++ Compiler is available for Windows and Linux.

•Preprocessor directives are used to make functions within the standard C++ libraries available to a program.

•Each C++ program must contain one main method as the entry point to the program.

•Statements define the actions that the program will execute.

•It is recommended that program code should be widely commented to make its purpose clear.

•The **c++** command calls the compiler, and its **-o** option allows the command to specify the name of the generated executable.

•A variable declaration specifies a data type and a chosen name by which the value within that variable can be referenced.

•The **cout** function, which is part of the C++ **iostream** library, writes content to the standard output console.

•An array is a fixed size variable that stores multiple items of data in elements, which are numbered starting at 0.

•The special **\0** character can be assigned to the final element of a **char** array to allow it to be treated as a single text string.

•A vector variable stores multiple items of data in elements, and can be dynamically resized.

•The value stored in an array or vector element can be referenced using that variable’s name and its index number.

•Variable values that are never changed by the program should be stored in a constant.

•A constant list can be automatically numbered by the **enum** keyword and given a type name by the **typedef** keyword.

13

**Performing operations**

***This chapter introduces the C++ operators and demonstrates the operations they can perform.***

[Doing arithmetic](#chapter13.xhtml_sec100)

[Assigning values](#chapter13.xhtml_sec101)

[Comparing values](#chapter13.xhtml_sec102)

[Assessing logic](#chapter13.xhtml_sec103)

[Examining conditions](#chapter13.xhtml_sec104)

[Establishing size](#chapter13.xhtml_sec105)

[Setting precedence](#chapter13.xhtml_sec106)

[Casting data types](#chapter13.xhtml_sec107)

[Summary](#chapter13.xhtml_sec108)

**Doing arithmetic**

![image](images/pgb26_1.jpg)

The arithmetical operators commonly used in C++ programs are listed in the table below, together with the operation they perform:

| **Operator** | **Operation** |
| **+** | Addition |
| **-** | Subtraction |
| ***** | Multiplication |
| **/** | Division |
| **%** | Modulus |
| **++** | Increment |
| **--** | Decrement |

The operators for addition, subtraction, multiplication, and division act as you would expect. Care must be taken, however, to bracket expressions where more than one operator is used to clarify the expression – operations within innermost parentheses are performed first:

**a = b * c - d % e / f ;                     // This is unclear.**

**a = ( b * c ) - ( ( d % e ) / f ) ;       // This is clearer.**

The **%** modulus operator will divide the first given number by the second given number and return the remainder of the operation. This is useful to determine if a number has an odd or even value.

The **++** increment operator and **--** decrement operator alter the given number by 1 and return the resulting value. These are most commonly used to count iterations in a loop. Counting up, the **++** operator increases the value by 1, while counting down, the **--** decrement operator decreases the value by 1.

The increment and decrement operators can be placed before or after a value to different effect. If placed before the operand (prefix), its value is immediately changed; if placed after the operand (postfix), its value is noted first, then the value is changed.

![image](images/hot.jpg)

Values used with operators to form expressions are called “operands” – in the expression **2 + 3** the numerical values **2** and **3** are the operands.

![image](images/commonb1.jpg)

arithmetic.cpp

![image](images/1bl.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3bl.jpg)In the main function, insert a statement to declare and initialize two integer variables

**int a = 8 , b = 4 ;**

![image](images/4bl.jpg)Next, insert statements to output the result of each basic arithmetic operation

**cout << “Addition result: ” << ( a + b ) << endl ;**

**cout << “Subtraction result: ” << ( a - b ) << endl ;**

**cout << “Multiplication result: ” << ( a * b ) << endl ;**

**cout << “Division result: ” << ( a / b ) << endl ;**

**cout << “Modulus result: ” << ( a % b ) << endl ;**

![image](images/5bl.jpg)Now, insert statements to output the result of both postfix and prefix increment operations

**cout << “Postfix increment: ” << a++ << endl ;**

**cout << “Postfix result: ” << a << endl ;**

**cout << “Prefix increment: ” << ++b << endl ;**

**cout << “Prefix result: ” << b << endl ;**

![image](images/6bl.jpg)Save, compile, and run the program to see the output

![image](images/pgb27_1.jpg)

![image](images/forget.jpg)

A prefix operator changes the variable value immediately – a postfix operator changes the value subsequently.

**Assigning values**

![image](images/pgb28_1.jpg)

The operators that are used in C++ programming to assign values are listed in the table below. All except the simple **=** assignment operator are a shorthand form of a longer expression so each equivalent is given for clarity:

| **Operator** | **Example** | **Equivalent** |
| **=** | **a = b** | **a = b** |
| **+=** | **a += b** | **a = ( a + b )** |
| **-=** | **a -= b** | **a = ( a - b )** |
| ***=** | **a *= b** | **a = ( a * b )** |
| **/=** | **a /= b** | **a = ( a / b )** |
| **%=** | **a %= b** | **a = ( a % b )** |

In the example above, the variable named “a” is assigned the value that is contained in the variable named “b” – so *that* becomes the new value stored in the **a** variable.

The **+=** operator is useful to add a value onto an existing value that is stored in the **a** variable.

In the table example, the **+=** operator first adds the value contained in variable **a** to the value contained in variable **b**. It then assigns the result to become the new value stored in variable **a**.

![image](images/forget.jpg)

It is important to regard the = operator to mean “assign” rather than “equals” to avoid confusion with the == equality operator.

All the other operators work in the same way by making the arithmetical operation between the two values first, then assigning the result of that operation to the first variable – to become its new stored value.

With the **%=** operator, the first operand **a** is divided by the second operand **b**, then the remainder of that operation is assigned to the **a** variable.

Each assignment operation is demonstrated in the program [here](#chapter13.xhtml_rogra).

![image](images/commonb1.jpg)

assign.cpp

![image](images/1bl.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3bl.jpg)In the main function, insert a statement declaring two integer variables

**int a , b ;**

![image](images/4bl.jpg)Next, insert statements to output simple assigned values

**cout << “Assign values: ” ;**

**cout << “a = “ << ( a = 8 ) << “ “ ;**

**cout << “b = “ << ( b = 4 ) ;**

![image](images/5bl.jpg)Now, insert statements to output combined assigned values

**cout << endl << “Add & assign: ” ;**

**cout << “a += b (8 += 4 ) a = “ << ( a += b ) ;**

**cout << endl << “Subtract & assign: ” ;**

**cout << “a -= b (12 -= 4 ) a = “ << ( a -= b ) ;**

**cout << endl << “Multiply & assign: ” ;**

**cout << “a *= b (8 *= 4 ) a = “ << ( a *= b ) ;**

**cout << endl << “Divide & assign: ” ;**

**cout << “a /= b (32 /= 4 ) a = “ << ( a /= b ) ;**

**cout << endl << “Modulus & assign: ” ;**

**cout << “a %= b (8 %= 4 ) a = “ << ( a %= b ) ;**

![image](images/6bl.jpg)Save, compile, and run the program to see the output

![image](images/pgb29_1.jpg)

![image](images/snake.jpg)

Unlike the **=** assign operator, the **==** equality operator compares operands and is described [here](#chapter13.xhtml_sec102).

**Comparing values**

![image](images/pgb30_1.jpg)

The operators that are commonly used in C++ programming to compare two numerical values are listed in the table below:

| **Operator** | **Comparative Test** |
| **==** | Equality |
| **!=** | Inequality |
| **>** | Greater than |
| **<** | Less than |
| **>=** | Greater than or equal to |
| **<=** | Less than or equal to |

The **==** equality operator compares two operands and will return **true** (1) if both are equal in value, otherwise it will return a **false** (0) value. If both are the same number, they are equal, or if both are characters, their ASCII code values are compared numerically. Conversely, the **!=** inequality operator returns **true** (1) if two operands are not equal, using the same rules as the **==** equality operator, otherwise it returns **false** (0). Equality and inequality operators are useful in testing the state of two variables to perform conditional branching in a program.

The **>** “greater than” operator compares two operands and will return **true** (1) if the first is greater in value than the second, or it will return **false** (0) if it is equal or less in value. The **<** “less than” operator makes the same comparison but returns **true** (1) if the first operand is less in value than the second, otherwise it returns **false** (0). A **>** “greater than” or **<** “less than” operator is often used to test the value of an iteration counter in a loop.

Adding the **=** operator after a **>** “greater than” or **<** “less than” operator makes it also return **true** (1) if the two operands are exactly equal in value.

Each comparison operation is demonstrated in the program [here](#chapter13.xhtml_gra).

![image](images/hot.jpg)

A-Z uppercase characters have ASCII code values 65-90 and a-z lowercase characters have ASCII code values 97-122, as listed [here](#chapter11.xhtml_chcod).

![image](images/commonb1.jpg)

comparison.cpp

![image](images/1bl.jpg)Start a new program by specifying the C++ library classes to include and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3bl.jpg)In the main function, insert statements to declare and initialize variables that can convert to Booleans

**int nil = 0, num = 0, max = 1 ; char cap = ‘A’, low = ‘a’ ;**

![image](images/4bl.jpg)Next, insert statements to output equality comparisons of integers and characters

**cout << “Equality comparisons: ” ;**

**cout << “(0 == 0) ” << ( nil == num ) << “(true)” ;**

**cout << “(A == a) ” << ( cap == low ) << “(false)” ;**

![image](images/5bl.jpg)Now, insert statements to output all other comparisons

**cout << endl << “Inequality comparison: ” ;**

**cout << “(0 != 1) ” << ( nil != max ) << “(true)” ;**

**cout << endl << “Greater comparison: ” ;**

**cout << “(0 > 1) ” << ( nil > max ) << “(false)” ;**

**cout << endl << “Lesser comparison: ” ;**

**cout << “(0 < 1) ” << ( nil < max ) << “(true)” ;**

**cout << endl << “Greater or equal comparison: ” ;**

**cout << “(0 >= 0) ”<< ( nil >= num ) << “(true)” ;**

**cout << endl << “Lesser or equal comparison: ” ;**

**cout << “(1 <= 0) ” << ( max <= num ) << “(false)” ;**

![image](images/6bl.jpg)Save, compile, and run the program to see the output

![image](images/pgb31_1.jpg)

![image](images/forget.jpg)

The ASCII code value for uppercase “A” is 65, but for lowercase “a” it’s 97 – so their comparison here returns **false** (0).

**Assessing logic**

![image](images/pgb32_1.jpg)

The logical operators most commonly used in C++ programming are listed in the table below:

| **Operator** | **Operation** |
| **&&** | Logical AND |
| **&#124;&#124;** | Logical OR |
| **!** | Logical NOT |

The logical operators are used with operands that have Boolean values of **true** or **false**, or are values that convert to **true** or **false**.

The logical **&&** AND operator will evaluate two operands and return **true** only if both operands themselves are **true**. Otherwise, the **&&** operator will return **false**. This is used in conditional branching where the direction of a program is determined by testing two conditions – if both conditions are satisfied, the program will go in a certain direction, otherwise it will take a different direction.

![image](images/snake.jpg)

Where there is more than one operand, each expression must be enclosed by parentheses.

Unlike the **&&** AND operator that needs both operands to be **true**, the **||** OR operator will evaluate its two operands and return **true** if either one of the operands itself returns **true**. If neither operand returns **true** then the **||** OR operator will return **false**. This is useful in C++ programming to perform a certain action if either one of two test conditions has been met.

The third logical **!** NOT operator is a unary operator that is used before a single operand. It returns the inverse value of the given operand, so if the variable **a** had a value of **true**, then **!a** would have a value of **false**. The **!** NOT operator is useful in C++ programs to toggle the value of a variable in successive loop iterations with a statement like **a = !a**. This ensures that on each pass the value is changed, like flicking a light switch on and off.

In C++ programs, a 0 represents the Boolean **false** value and any non-zero value, such as 1, represents the Boolean **true** value.

Each logical operation is demonstrated in the program [here](#chapter13.xhtml_peci).

![image](images/commonb1.jpg)

logic.cpp

![image](images/1bl.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3bl.jpg)In the main function, declare and initialize two integer variables – with values that can represent Boolean values

**int a = 1 , b = 0 ;**

![image](images/4bl.jpg)Insert statements to output the result of AND evaluations

**cout << “AND logic:” << endl ;**

**cout << “(a && a) ” << ( a && a ) << “(true) ” ;**

**cout << “(a && b) ” << ( a && b ) << “(false) ” ;**

**cout << “(b && b) ” << ( b && b ) << “(false)” << endl ;**

![image](images/5bl.jpg)Insert statements to output the result of OR evaluations

**cout << endl << “OR logic:” << endl ;**

**cout << “(a || a) ” << ( a || a ) << “(true) ” ;**

**cout << “(a || b) ” << ( a || b ) << “(true) ” ;**

**cout << “(b || b) ” << ( b || b ) << “(false)” << endl ;**

![image](images/6bl.jpg)Insert statements to output the result of NOT evaluations

**cout << endl << “NOT logic:” << endl ;**

**cout << “a = “ << a << “ !a = “ << !a << “ “ ;**

**cout << “b = “ << b << “ !b = “ << !b << endl ;**

![image](images/7bl.jpg)Save, compile and run the program to see the output

![image](images/pgb33_1.jpg)

![image](images/forget.jpg)

Notice that **0 && 0** returns **0**, not **1** – demonstrating the maxim “two wrongs don’t make a right”.

**Examining conditions**

Possibly the C++ programmer’s most favorite test operator is the **?:** “ternary” operator. This operator first evaluates an expression for a **true** or **false** condition, then returns one of two specified values depending on the result of the evaluation. For this reason it is also known as the “conditional” operator.

![image](images/pgb34_1.jpg)

The **?:** ternary operator has this syntax:

**( *test-expression* ) ? *if-true-return-this* : *if-false-return-this* ;**

Although the ternary operator can initially appear a little confusing, it is well worth becoming familiar with this operator as it can execute powerful program branching with minimal code. For example, to branch when a variable is not a value of 1:

**( var != 1 ) ? *if-true-do-this* : *if-false-do-this* ;**

The ternary operator is commonly used in C++ programming to assign the maximum or minimum value of two variables to a third variable. For example, to assign a minimum like this:

**c = ( a < b ) ? a : b ;**

The expression in parentheses returns **true** when the value of variable **a** is less than that of variable **b** – so in this case, the lesser value of variable **a** gets assigned to variable **c**.

Similarly, replacing the **<** less than operator in the test expression with the **>** greater than operator would assign the greater value of variable **b** to variable **c**.

Another common use of the ternary operator incorporates the **%** modulus operator in the test expression to determine whether the value of a variable is an odd number or an even number:

**( var % 2 != 0 ) ? *if-true(odd)-do-this* : *if-false(even)-do-this* ;**

Where the result of dividing the variable value by two does leave a remainder, the number is odd – where there is no remainder, the number is even. The test expression **( var % 2 == 1 )** would have the same effect but it is preferable to test for inequality – it’s easier to spot when something is different than when it’s identical.

The ternary operator is demonstrated in the program [here](#chapter13.xhtml_tar).

![image](images/forget.jpg)

The ternary operator has three operands – the one before the **?**, and those before and after the :.

![image](images/commonb1.jpg)

ternary.cpp

![image](images/1bl.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3bl.jpg)In the main function, insert statements declaring three integer variables, and initializing two of them

**int a, b, max ;**

**a = 1, b = 2 ;**

![image](images/4bl.jpg)Insert statements to output the value and parity of the first examined variable

**cout << “Variable a value is: ” ;**

**cout << ( ( a != 1 ) ? “not 1, “ : “1, “ ) ;**

**cout << ( ( a % 2 != 0 ) ? “odd” : “even” ) ;**

![image](images/5bl.jpg)Next, insert statements to output the value and parity of the second examined variable

**cout << endl << “Variable b value is: ” ;**

**cout << ( ( b != 1 ) ? “not 1, “ : “1, “ ) ;**

**cout << ( ( b % 2 != 0 ) ? “odd” : “even” ) ;**

![image](images/6bl.jpg)Now, insert statements to output the greater of the two stored variable values

**max = ( a > b ) ? a : b ;**

**cout << endl << “Greater value is: ” << max << endl ;**

![image](images/7bl.jpg)Save, compile and run the program to see the output

![image](images/pgb35_1.jpg)

![image](images/hot.jpg)

The ternary operator can return values of any data type – numbers, strings, Boolean values, etc.

**Establishing size**

Declaration of a variable allocates system memory where values assigned to that variable will be stored. The amount of memory allocated for this is determined by your system and the data type.

![image](images/pgb36_1.jpg)

Typically, an **int** data type is created as a “long” value by default, which can store values from +2,147,483,647 to -2,147,483,648\. On the other hand, if the **int** data type is created as a “short” value by default, it can only store values from +32,767 to -32,768.

The preferred range can be explicitly specified when declaring the variable by prefixing the **int** keyword with a **short** or **long** qualifier. The **short int** is useful to save memory space when you are sure the limited range will never be exceeded.

When an **int** variable is declared, it can by default contain either positive or negative integers, which are known as “signed” values. If the variable will always contain only positive integers, it can be qualified as **unsigned** to increase its maximum possible value. Typically, an **unsigned short int** has a range from zero to 65,535 and an **unsigned long int** has a range from zero to 4,294,967,295.

The memory size of any variable can be discovered using the C++ **sizeof** operator. The name of the variable to be examined can be specified in optional parentheses following the **sizeof** operator name. For example, to examine a variable named “var”:

**sizeof( var ) ;      // Alternatively you can use “sizeof var ;”.**

The **sizeof** operator will return an integer that is the number of bytes allocated to store data within the named variable.

![image](images/hot.jpg)

Although **sizeof** is an operator that does not strictly need parentheses, it is commonly seen with them – as if it was a function, like **main()**

Simple data types, such as **char** and **bool**, only need a single byte of memory to store just one piece of data. Longer numeric values need more memory, according to their possible range – determined by data type and qualifiers.

The memory allocated to an array is simply a multiple of that allocated to a single variable of its data type, according to its number of elements. For example, an **int** array of 50 elements will allocate 50 times the memory allocated to a single **int** variable.

The **sizeof** operator is demonstrated in the program [here](#chapter13.xhtml_cifyin).

![image](images/commonb1.jpg)

sizeof.cpp

![image](images/1bl.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3bl.jpg) In the main function, insert statements declaring variables of various data types

| **int num ;** | **int nums[50] ;** | **float decimal ;** |
| **bool isTrue ;** | **unsigned int max ;** | **char letter ;** |
| **double pi ;** | **short int number ;** | **char letters[50] ;** |

![image](images/4bl.jpg)Next, insert statements to output the byte size of each integer variable

**cout << “int size:” << sizeof( num ) << endl ;**

**cout << “50 int size: ” << sizeof( nums ) << endl ;**

**cout << “short int size: ” << sizeof( number ) << endl ;**

**cout << “unsigned int size: ” << sizeof( max ) << endl ;**

![image](images/5bl.jpg)Now, insert statements to output the size of other variables

**cout << “double size: ” << sizeof( pi ) << endl ;**

**cout << “float size: ” << sizeof( decimal ) << endl ;**

**cout << “char size: ” << sizeof( letter ) << endl ;**

**cout << “50 char size: ” << sizeof( letters ) << endl ;**

**cout << “bool size: ” << sizeof( isTrue ) << endl ;**

![image](images/6bl.jpg)Save, compile and run the program to see the output

![image](images/pgb37_1.jpg)

![image](images/forget.jpg)

Here, the **int** data type is created as a **long** type by default – your system may be different.

**Setting precedence**

Operator precedence determines the order in which C++ evaluates expressions. For example, in the expression **a = 6 + 8 * 3**, the order of precedence determines that multiplication is completed first.

![image](images/pgb38_1.jpg)

The table below lists operator precedence in descending order – those on the top row have highest precedence; those on lower rows have successively lower precedence. The order in which C++ evaluates expressions containing multiple operators of equal precedence is determined by “operator associativity” – grouping operands with the one on the left (LTR) or on the right (RTL).

| **Operator** | **Direction** |
| **( )** | Function call | **[ ]** | Array index | LTR |
| **->** | Class pointer | . | Class member |
| **!** | Logical NOT | ***** | Pointer | RTL |
| **--** | Decrement | **++** | Increment |
| **+** | Positive sign | **-** | Negative sign |
| **sizeof** | Size of | **&** | Address of |
| ***** | Multiply | **/** | Divide | LTR |
| **%** | Modulus |  |  |
| **+** | Add | **-** | Subtract | LTR |
| **<=** | Less or equal | **<** | Less than | LTR |
| **>=** | Greater or equal | **>** | Greater than |
| **==** | Equality | **!=** | Inequality | LTR |
| **&&** | Logical AND |  |  | LTR |
| **&#124;&#124;** | Logical OR |  |  | LTR |
| **?:** | Ternary |  |  | RTL |
| **+= -= *= /= %=** Assignments | RTL |
| , | Comma |  |  | LTR |

In addition to the operators in this table there are a number of “bitwise” operators, which are used to perform binary arithmetic – see [here](#chapter04.xhtml_sec29). Those operators perform in just the same way in C++.

Operator precedence is demonstrated in the program opposite.

![image](images/forget.jpg)

The ***** multiply operator is on a higher row than the **+** addition operator – so in the expression **a=6+8*3**, multiplication is completed first, before the addition.

![image](images/hot.jpg)

The **->** class pointer and the . class member operators are introduced later in this book – but they are included here for completeness.

![image](images/commonb1.jpg)

precedence.cpp

![image](images/1bl.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2bl.jpg)Add a main function continuing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3bl.jpg)In the main function, declare an integer variable initialized with the result of an expression using default precedence, then output the result

**int num = 1 + 4 * 3 ;**

**cout << endl << “Default order: ” << num << endl ;**

![image](images/4bl.jpg)Next, assign the result of this expression to the variable using explicit precedence, then output the result

**num = ( 1 + 4 ) * 3 ;**

**cout << “Forced order: ” << num << endl << endl ;**

![image](images/5bl.jpg)Assign the result of a different expression to the variable using direction precedence, then output the result

**num = 7 - 4 + 2 ;**

**cout<< “Default direction: ” << num << endl ;**

![image](images/6bl.jpg)Now, assign the result of this expression to the variable using explicit precedence, then output the result

**num = 7 - ( 4 + 2 ) ;**

**cout << “Forced direction: ” << num << endl ;**

![image](images/7bl.jpg)Save, compile and run the program to see the output

![image](images/pgb39_1.jpg)

![image](images/snake.jpg)

Do not rely upon default precedence as it may vary between compilers – always use parentheses to clarify expressions.

**Casting data types**

![image](images/pgb40_1.jpg)

Any data stored in a variable can be forced (coerced) into a variable of a different data type by a process known as “casting”. The cast statement simply states the data type to which the value should be cast in parentheses preceding the name of the variable containing the data to be cast. So casting syntax looks like this:

***variable-name* = ( *data-type* ) *variable-name* ;**

This is the traditional form of casting that is also found in the C programming language. A newer alternative available in C++ uses angled brackets with the **static_cast** keyword, like this:

***variable-name* = static_cast < *data-type* > *variable-name* ;**

The newer version allows casts to be more easily identified in source code by avoiding the use of parentheses, which can easily be confused with parentheses in expressions. The newer form of casting is preferred, but the older form is still widely found.

Casting is often necessary to accurately store the result of an arithmetic operation, because dividing one integer by another integer will always produce an integer result. For example, the integer division **7/2** produces the truncated integer result of **3**.

To store the accurate floating-point result would require the result be cast into a suitable data type, such as a **float**, like this:

**float result = ( float ) 7 / 2 ;**

Or alternatively using the newer form of cast:

**float result = static_cast < float > 7 / 2 ;**

![image](images/forget.jpg)

The result of dividing an integer by another integer is truncated, not rounded – so a result of 9.9 would become 9.

In either case, it should be noted that operator precedence casts the first operand into the specified data type before implementing the arithmetic operation, so the statement can best be written as:

**float result = static_cast < float > ( 7 ) / 2 ;**

Bracketing the expression as **( 7 / 2 )** would perform the arithmetic first on integers, so the integer result would be truncated before being cast into the **float** variable – not the desired effect!

Casting with both the older C-style form and the newer C++ form is demonstrated in the program [here](#chapter13.xhtml_namespa).

![image](images/commonb1.jpg)

cast.cpp

![image](images/1bl.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3bl.jpg)In the main function, insert statements to declare and initialize integer, character, and floating-point variables

**int num = 7, factor = 2 ;**

**char letter = ‘A’ ; float result = 0.0 ;**

![image](images/4bl.jpg)Output the result of a plain integer division

**cout << “Integer division: ” << ( num / factor ) << endl ;**

![image](images/5bl.jpg)Now, cast the same division into a floating-point variable and output that result

**result = (float) ( num ) / factor ;**

**cout << “Cast division float: ” << result << endl ;**

![image](images/6bl.jpg)Next, cast a character variable into an integer variable and output that value

**num = static_cast <int> ( letter ) ;**

**cout << “Cast character int: ” << num << endl ;**

![image](images/7bl.jpg)Cast an integer into a character variable and output it

**letter = static_cast <char> ( 70 ) ;**

**cout << “Cast integer char: ” << letter << endl ;**

![image](images/8bl.jpg)Save, compile and run the program to see the output

![image](images/pgb41_1.jpg)

![image](images/hot.jpg)

ASCII (pronounced “askee”) is the American Standard Code for Information Interchange, which is the accepted standard for plain text. In ASCII, characters are represented numerically within the range 0-127. Uppercase ‘A’ is 65, so that integer value gets cast into an **int** variable – see [here](#chapter11.xhtml_chcod).

**Summary**

![image](images/pgb114_1.jpg)

•Arithmetical operators can form expressions with two operands for addition **+**, subtraction **-**, multiplication *****, division **/**, or modulus **%**.

•Increment **++** and decrement **--** operators modify a single operand by a value of 1.

•The assignment **=** operator can be combined with an arithmetical operator to perform an arithmetical calculation, then assign its result.

•Comparison operators can form expressions comparing two operands for equality **==**, inequality **!=**, greater **>**, lesser **<**, greater or equal **>=**, and lesser or equal **<=** values.

•Logical **&&** and **||** operators form expressions evaluating two operands to return a Boolean value of true or false.

•The logical **!** operator returns the inverse Boolean value of a single operand.

•A ternary **?:** operator evaluates a given Boolean expression, then returns one of two operands depending on its result.

•The **sizeof** operator returns the memory byte size of a variable.

•An **int** variable may be qualified as a **short** type for smaller numbers, or as a **long** type for large numbers.

•Where an **int** variable will only store positive numbers, it may be qualified as **unsigned** to extend its numeric range.

•It is important to explicitly set operator precedence in complex expressions by adding parentheses **( )**.

•Data stored in a variable can be forced into a variable of a different data type by the casting process.

•C++ supports traditional C-style casts and the newer form of casts that use the **static_cast** keyword.

14

**Making statements**

***This chapter demonstrates C++ conditional statements, which allow programs to branch in different directions, and introduces C++ function structures.***

[Branching with if](#chapter14.xhtml_sec109)

[Switching branches](#chapter14.xhtml_sec110)

[Looping for](#chapter14.xhtml_sec111)

[Looping while](#chapter14.xhtml_sec112)

[Declaring functions](#chapter14.xhtml_sec113)

[Passing arguments](#chapter14.xhtml_sec114)

[Overloading functions](#chapter14.xhtml_sec115)

[Optimizing functions](#chapter14.xhtml_sec116)

[Summary](#chapter14.xhtml_sec117)

**Branching with if**

The C++ **if** keyword performs the basic conditional test that evaluates a given expression for a Boolean value of **true** or **false** – and its syntax looks like this:

**if ( *test-expression* ) { *statements-to-execute-when-true* }**

![image](images/pgb44_1.jpg)

The braces following the test may contain one or more statements, each terminated by a semicolon, but these will only be executed when the expression is found to be **true**. When the test is found to be **false**, the program proceeds to its next task.

Optionally, an **if** statement can offer alternative statements to execute when the test fails by appending an **else** statement block after the **if** statement block, like this:

**if ( *test-expression* ) { *statements-to-execute-when-true* }**

**else { *statements-to-execute-when-false* }**

To test two conditions, the test expression may use the **&&** operator – for example, **if ( ( num > 5 ) && ( letter == ‘A’ ) )**. Alternatively, an **if** statement can be “nested” within another **if** statement, so those statements in the inner statement block will only be executed when both tests succeed – but statements in the outer statement block will be executed if the outer test succeeds.

![image](images/commonv.jpg)

ifelse.cpp

![image](images/1v.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2v.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3v.jpg)In the main function, insert statements to declare and initialize two variables

**int num = 8 ;**

**char letter = ‘A’ ;**

![image](images/hot.jpg)

Where there is only one statement to execute when the test succeeds, the braces may be omitted – but retaining them aids code clarity.

![image](images/4v.jpg)Next, insert an **if-else** statement that tests the integer variable value and outputs an appropriate response

**if ( num > 5 )**

**{ cout << “Number exceeds five” << endl ; }**

**else**

**{ cout << “Number is five or less” << endl ; }**

![image](images/5v.jpg)In the **if** statement block, insert a nested **if** statement that tests the character variable value and outputs when matched

**if ( letter == ‘A’ ) { cout << “Letter is A” << endl ; }**

![image](images/6v.jpg)Save, compile and run the program to see both tests succeed

![image](images/pgb45_1.jpg)

![image](images/7v.jpg)Edit the character variable declaration to change its value

**char letter = ‘B’ ;**

![image](images/8v.jpg)Save, compile, and run the program once more to see only the outer test succeed – executing the outer **if** statement

![image](images/pgb45_2.jpg)

![image](images/9v.jpg)Edit the integer variable declaration to change its value

**int num = 3 ;**

![image](images/10v.jpg)Save, compile, and run the program again to see both tests now fail – executing the outer **else** statement

![image](images/pgb45_2.jpg)

![image](images/hot.jpg)

Shorthand can be used when testing a Boolean value – so the expression **if ( flag == true )** can be written as **if ( flag )**

![image](images/snake.jpg)

Avoid nesting more than three levels of **if** statements – to avoid confusion and errors.

**Switching branches**

![image](images/pgb46_1.jpg)

The **if** and **else** keywords, introduced [here](#chapter14.xhtml_sec109), allow programs to branch in a particular direction according to the result of a test condition, and can be used to repeatedly test a variable to match a value – for example, testing for an integer:

**if ( num == 1 ) { cout << “Monday” ; }**

**else**

**if ( num == 2 ) { cout << “Tuesday” ; }**

**else**

**if ( num == 3 ) { cout << “Wednesday” ; }**

**else**

**if ( num == 4 ) { cout << “Thursday” ; }**

**else**

**if ( num == 5 ) { cout << “Friday” ; }**

The program will branch in the direction of the match.

Conditional branching with long **if**-**else** statements can often be more efficiently performed using a **switch** statement instead, especially when the test expression evaluates one variable.

The **switch** statement works in an unusual way. It takes a given variable value, then seeks a matching value among a number of **case** statements. Statements associated with the matching case statement value will then be executed.

When no match is found, no **case** statements will be executed, but you may add a **default** statement after the final **case** statement to specify statements to be executed when no match is found.

It is important to follow each case statement with the **break** keyword, to stop the program proceeding through the switch block after all statements associated with the matched **case** value have been executed – unless that is precisely what you require. For example, one statement for each block of three values, like this:

**switch( *variable-name* )**

**{**

**case *value1* ; case *value2* ; case *value3* ;**

***statements-to-be-executed* ; break ;**

**case *value4* ; case *value5* ; case *value6* ;**

***statements-to-be-executed* ; break ;**

**}**

Usually, each **case** statement will have its own set of statements to execute and be terminated by a **break**, as in the program opposite.

![image](images/snake.jpg)

Missing **break** keywords are not syntax errors – ensure that all intended breaks are present after **case** statements.

![image](images/commonv.jpg)

switch.cpp

![image](images/1v.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2v.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3v.jpg)In the main function, insert a statement to declare and initialize an integer variable with a value to be matched

**int num = 3 ;**

![image](images/4v.jpg)Next, insert a **switch** statement to seek a match

**switch ( num )**

**{**

**case 1 : cout << num << “ : Monday” ; break ;**

**case 2 : cout << num << “ : Tuesday” ; break ;**

**case 3 : cout << num << “ : Wednesday” ; break ;**

**case 4 : cout << num << “ : Thursday” ; break ;**

**case 5 : cout << num << “ : Friday” ; break ;**

**}**

![image](images/5v.jpg)In the **switch** statement, insert a **default** statement after the final **case** statement

**default : cout << num << “ : Weekend day” ;**

![image](images/6v.jpg)Save, compile, and run the program to see the output

![image](images/7v.jpg)Now, edit the integer variable declaration to change its value, then save, compile and run the program once more

**int num = 6 ;**

![image](images/pgb47_1.jpg)

![image](images/hot.jpg)

Notice that a **default** statement does not need to be followed by a **break** keyword – because a **default** statement always appears last in a **switch** statement.

**Looping for**

A loop is a piece of code in a program that automatically repeats. One complete execution of all statements contained within the loop block is known as an “iteration” or “pass”.

![image](images/pgb48_1.jpg)

The number of iterations made by a loop is controlled by a conditional test made within the loop. While the tested expression remains **true**, the loop will continue – until the tested expression becomes **false**, at which time the loop ends.

The three types of loop structures in C++ programming are **for** loops, **while** loops, and **do**-**while** loops. Perhaps the most commonly used loop is the **for** loop, which has this syntax:

**for ( *initializer* ; *test-expression* ; *incrementer* ) { *statements* }**

The initializer sets the starting value for a counter of the number of iterations made by the loop. An integer variable is used for this purpose and is traditionally named “i”.

Upon each iteration of the loop, the test expression is evaluated, and that iteration will only continue while this expression is **true**. When the tested expression becomes **false**, the loop ends immediately without executing the statements again. On each iteration the counter is incremented then the statements executed.

Loops may be nested within other loops – so that the inner loop will fully execute its iterations on each iteration of the outer loop.

![image](images/commonv.jpg)

forloop.cpp

![image](images/1v.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2v.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3v.jpg)In the main function, insert a statement to declare an integer variable to be used as a loop iteration counter

**int i ;**

![image](images/4v.jpg)Next, insert a **for** loop to output the counter value on each of three iterations

**for ( i = 1 ; i < 4 ; i++ )**

**{**

**cout << “Loop iteration: ” << i << endl ;**

**}**

![image](images/5v.jpg)Save, compile, and run the program to see the output

![image](images/pgb49_1.jpg)

![image](images/6v.jpg)Now, edit the variable declaration to add a second counter

**int i , j ;                  // Integer variable “j” added.**

![image](images/7v.jpg)Inside the **for** loop block, after the output statement add an inner loop to output its counter value on each iteration

**for ( j = 1 ; j < 4 ; j++ )**

**{ cout << “    Inner loop iteration: “ << j << endl ; }**

![image](images/8v.jpg)Save, compile, and run the program again to see the inner loop fully execute on each iteration of the outer loop

![image](images/pgb49_2.jpg)

![image](images/hot.jpg)

Alternatively, a **for** loop counter can count down by decrementing the counter value on each iteration using i-- instead of the i++ incrementer.

![image](images/forget.jpg)

On the third iteration of these loops, the incrementer increases the counter value to 4 – so when it is next evaluated, the test returns false and the loop ends.

**Looping while**

An alternative to the **for** loop, introduced [here](#chapter14.xhtml_sec111), uses the **while** keyword, followed by an expression to be evaluated. When the expression is **true**, statements contained within braces following the test expression will be executed. The expression will then be evaluated again, and the **while** loop will continue until the expression is found to be **false**.

![image](images/pgb50_1.jpg)

The loop’s statement block must contain code that will affect the tested expression in order to change the evaluation result to **false**, otherwise an infinite loop is created that will lock the system! When the tested expression is found to be **false** upon its first evaluation, the **while** loop’s statement block will never be executed.

A subtle variation of the **while** loop places the **do** keyword before the loop’s statement block and a **while** test after it, with this syntax:

**do { statements-to-be-executed } while ( test-expression ) ;**

In a **do-while** loop, the statement block will always be executed at least once – because the expression is not evaluated until after the first iteration of the loop.

![image](images/hot.jpg)

If you accidentally start running an infinite loop, press the **Ctrl + C** keys to terminate the process.

A **break** statement can be included in any kind of loop to immediately terminate the loop when a test condition is met. The **break** statement ensures no further iterations of that loop will be executed.

Similarly, a **continue** statement can be included in any kind of loop to immediately terminate that particular iteration of the loop when a test condition is met. The **continue** statement allows the loop to proceed to the next iteration.

![image](images/commonv.jpg)

while.cpp

![image](images/1v.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <vector>                  // Include vector support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2v.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/3v.jpg)In the main function, insert statements to declare an integer vector and an integer variable loop counter

**vector <int> vec( 10 ) ;**

**int i = 0 ;**

![image](images/4v.jpg)Next, insert a **while** loop to assign a counter value to an element of the vector on each iteration

**while ( i < vec.size() )**

**{**

**i++ ;                                       // Increment the counter.**

**vec[ i-1 ] = i ;                        // Assign count to element.**

**cout << “ | ” << vec.at( i-1 ) ;**

**}**

![image](images/5v.jpg)Save compile and run the program to see the output

![image](images/pgb51_1.jpg)

![image](images/6v.jpg)Edit the **while** loop to add a **continue** statement immediately after the incrementer to make the loop skip its third iteration

**if ( i == 3 ) { cout << “ | Skipped” ; continue ; }**

![image](images/7v.jpg)After the **continue** statement, now add a **break** statement, to make the loop quit on its eighth iteration

**if ( i == 8 ) { cout << endl << “Done” ; break ; }**

![image](images/8v.jpg)Save, compile, and run the program once more to see the loop now omits some iterations

![image](images/pgb51_2.jpg)

![image](images/forget.jpg)

The vector library must be included with a preprocessor directive in this example.

![image](images/snake.jpg)

The position of **break** and **continue** statements is important – they must appear after the incrementer, to avoid creating an infinite loop, but before other statements that affect the program to avoid executing those statements.

**Declaring functions**

![image](images/pgb52_1.jpg)

Functions enclose a section of code that provides specific functionality to the program. When a function is called from the main program, its statements are executed and, optionally, a value can be returned to the main program upon completion. There are three main benefits to using functions:

•Functions make program code easier to understand and maintain.

•Tried and tested functions can be re-used by other programs.

•Several programmers can divide the workload in large projects by working on different functions of the program.

Declaring functions

Each function is declared early in the program code as a “prototype”, comprising a data type for the value it will return and the function name followed by parentheses, which may optionally contain a list of “argument” data types of passed values it may use. The syntax of a function prototype declaration looks like this:

***return-data-type function-name ( arguments-data-type-list ) ;***

For example, a function named “computeArea” that returns a **float** value and is passed two **float** arguments is declared as:

**float computeArea( float, float ) ;**

![image](images/hot.jpg)

Strictly speaking, the arguments in a function prototype are known as its “formal parameters”.

Defining functions

The function’s definition appears later in the program code and comprises a repeat of the prototype, plus the actual function body. The function body is the statements to be executed whenever the function is called, contained within a pair of braces.

It is important to recognize that the compiler checks the function definition against the prototype, so the actual returned data type must match that specified in the prototype, and any supplied arguments must match in both number and data type. Compilation fails if the definition does not match the prototype. A simple **computeArea** definition might look like this:

**float computeArea( float width, float height )**

**{**

**return ( width * height ) ;**

**}**

![image](images/forget.jpg)

Use the **void** keyword if the function will return no value to the caller.

Variable scope

Variables that are declared in a function can only be used locally within that function, and are not accessible globally for use in other functions. This limitation is known as “variable scope”.

![image](images/commonv.jpg)

scope.cpp

![image](images/1v.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2v.jpg)Next, declare two simple function prototypes

**float bodyTempC() ;**

**float bodyTempF() ;**

![image](images/3v.jpg)Now, add a main function containing calls to each function and a final **return** statement

**int main()**

**{**

**cout << “Centigrade: ” << bodyTempC() << endl ;**

**cout << “Fahrenheit: ” << bodyTempF() << endl ;**

**return 0 ;**

**}**

![image](images/4v.jpg)After the main function, define both other functions – to each return the value of a local “temperature” variable

**float bodyTempC()**

**{**

**float temperature = 37.0 ;**

**return temperature ;**

**}**

**float bodyTempF()**

**{**

**float temperature = 98.6 ;**

**return temperature ;**

**}**

![image](images/5v.jpg)Save, compile, and run the program to see the output

![image](images/pgb53_1.jpg)

![image](images/hot.jpg)

Variables of the same name do not conflict when they are declared in a different scope – they are not visible to each other.

**Passing arguments**

Function calls frequently supply argument values to a function. These can be of any quantity and data type, but they must agree with those specified in the function prototype declaration.

![image](images/pgb54_1.jpg)

Note that arguments passed to a function only supply a copy of the original value, in a procedure known as “passing by value”.

The values passed to arguments can be “static” values, specified in the program code, or “dynamic” values that are input by the user. At a command prompt, the C++ **cin** function can be used with the **>>** input stream operator to direct a value from standard input to a variable, like this:

**float num ;**

**cout << “Please enter a number: ” ;**

**cin >> num ;**

Input can then be passed to a function as an argument in a function call, such as **workWith( num )**.

![image](images/snake.jpg)

Function prototypes must be declared before they can be defined. Typically, the prototypes appear before the main function, and their definitions appear after the main function.

Optionally, a function prototype can assign default values to arguments, which will be used when a call does not pass an argument value. Multiple arguments can be assigned default values in the prototype but these must always appear at the end of the argument list, after any other arguments.

In the same way that functions can be called from the main function, functions may call other functions and pass arguments.

![image](images/commonv.jpg)

args.cpp

![image](images/1v.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2v.jpg)Next, declare a function prototype that returns a float value and specifies a single float argument, to which a default value is assigned

**float fToC ( float degreesF = 32.0 ) ;**

![image](images/3v.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/4v.jpg)After the main function, define the “fToC” function with statements that will return a converted value

**float fToC( float degreesF )**

**{**

**float degreesC = ( ( 5.0 / 9.0 ) * ( degreesF - 32.0 ) ) ;**

**return degreesC ;**

**}**

![image](images/5v.jpg)In the main function, insert a statement to declare two **float** variables – to store an input Fahrenheit temperature value and its Centigrade equivalent

**float fahrenheit, centigrade ;**

![image](images/6v.jpg)Insert statements to request that user input be stored in the first variable

**cout << “Enter a Fahrenheit temperature:\t” ;**

**cin >> fahrenheit ;**

![image](images/7v.jpg)Next, call the “fToC” function to convert the input value – and assign the conversion to the second variable

**centigrade = fToC( fahrenheit ) ;**

![image](images/8v.jpg)Now, output a message describing the result

**cout << fahrenheit << “F is “ << centigrade << “C” ;**

![image](images/9v.jpg)Finally, add a statement to output a further message using the default argument value of the function prototype

**cout << endl << “Freezing point: “ << fToC() << “C” ;**

![image](images/10v.jpg)Save, compile, and run the program, then enter a numeric value when requested to see the output

![image](images/pgb55_1.jpg)

![image](images/hot.jpg)

In the same way that functions can be called from the main function, functions may call other functions and pass arguments to them.

![image](images/forget.jpg)

The names given to the arguments and variables in the function definition do not need to be the same as the variable names in the calling function – but it helps to clarify the program.

**Overloading functions**

Function “overloading” allows functions of the same name to happily co-exist in the same program, providing their arguments differ in number, data type, or both number and data type. The compiler matches a function call to the correct version of the function by recognizing its argument number and data types – a process known as “function resolution”.

![image](images/pgb56_1.jpg)

It is useful to create overloaded functions when the tasks they are to perform are similar, yet subtly different.

![image](images/commonv.jpg)

overload.cpp

![image](images/1v.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2v.jpg)Below the preprocessor instructions, declare a function prototype that returns a float value and has one argument

**float computeArea ( float ) ;**

![image](images/3v.jpg)Now, declare two overloaded function prototypes – having different arguments to the first prototype

**float computeArea ( float, float ) ;**

**float computeArea ( char, float, float ) ;**

![image](images/4v.jpg)Below the prototype declarations, add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/5v.jpg)After the main function, define the first function that receives just one argument

**float computeArea( float diameter )**

**{**

**float radius = ( diameter / 2 ) ;**

**return ( 3.141593 * ( radius * radius ) ) ;**

**}**

![image](images/snake.jpg)

Functions that only differ by their return data type cannot be overloaded – it’s the arguments that must differ. Function resolution does not take the return data types into consideration.

![image](images/6v.jpg)Below the first function definition, define the overloaded functions that receive different arguments

**float computeArea( float width, float height )**

**{**

**return ( width * height ) ;**

**}**

**float computeArea( char letter, float width , float height )**

**{**

**return ( ( width / 2 ) * height ) ;**

**}**

![image](images/7v.jpg)In the main function, insert statements to declare two variables, and initialize one with user input

**float num, area ;**

**cout << “Enter dimension in feet: “ ;**

**cin >> num ;**

![image](images/8v.jpg)Call the first function and output its returned value

**area = computeArea( num ) ;**

**cout << “Circle: Area = “ << area << “ sq.ft.” << endl ;**

![image](images/9v.jpg)Call the overloaded functions and output their returns

**area = computeArea( num, num ) ;**

**cout << “Square: Area = “<< area << “ sq.ft.” << endl ;**

**area = computeArea( ‘T’, num, num ) ;**

**cout << “Triangle: Area = “<< area << “sq.ft.” << endl ;**

![image](images/10v.jpg)Save, compile, and run the program, then enter a numeric value when requested, to see the output

![image](images/pgb57_1.jpg)

![image](images/forget.jpg)

The value passed to the **char** argument is never used – that argument is included merely to differentiate that overloaded function.

**Optimizing functions**

![image](images/pgb58_1.jpg)

Functions can call themselves recursively, to repeatedly execute the statements contained in their function body – much like a loop. As with loops, a recursive function must contain an incrementer and a conditional test to call itself again, or stop repeating when a condition is met. The syntax of a recursive function looks like this:

***return-data-type function-name* ( *argument-list* )**

**{**

***statements-to-be-executed* ;**

***incrementer* ;**

***conditional-test-to-recall-or-exit* ;**

**}**

The incrementer will change the value of a passed argument – so subsequent calls will pass the adjusted value back to the function.

![image](images/commonv.jpg)

optimize.cpp

![image](images/1v.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2v.jpg)Below the preprocessor instructions, declare two function prototypes that will both be recursive functions

**int computeFactorials ( int, int ) ;**

**int factorial ( int ) ;**

![image](images/3v.jpg)Below the prototype declarations, add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/4v.jpg)After the main function, add the definition for the first function prototype – a recursive function

**int computeFactorials( int num, int max )**

**{**

**cout << “Factorial of “ << num << “: ” ;**

**cout << factorial( num ) << endl ;           // Statements.**

**num++ ;                                                         // Incrementer.**

**if ( num > max ) return 0 ;                   // Exit or call again.**

**else return computeFactorials( num , max ) ;**

**}**

![image](images/hot.jpg)

A recursive function generally uses more system resources than a loop – but it can make for more readable code.

![image](images/5v.jpg)Define a recursive function for the second prototype

**int factorial( int n )**

**{**

**int result ;**

**if ( n == 1 ) result = 1 ;                           // Exit or...**

**else result = ( factorial( n - 1 ) * n ) ;   // Decrement...**

**return result ;                                       // and call again.**

**}**

![image](images/6v.jpg)At the start of the main function, insert a call to the recursive function

**computeFactorials( 1, 8 ) ;**

![image](images/7v.jpg)Save, compile, and run the program to see the output

![image](images/pgb59_1.jpg)

The output lists factorial values (factorial 3 is 3x2x1=6, etc.), but the program can be improved by optimizing the **factorial()** function. This function does not need a variable if written with the ternary operator. It then contains just one statement, so its definition can replace the prototype declaration as an “inline” declaration. This means that the program need not keep checking between the declaration and definition, and so improves efficiency.

![image](images/8v.jpg)Delete the **factorial()** function definition, then replace its prototype declaration with this inline declaration

**inline int factorial( int n )**

**{ return ( n == 1 ) ? 1 : ( factorial( n - 1 ) * n ) ; }**

![image](images/9v.jpg)Save, compile, and run the program again to see the same output, produced more efficiently

![image](images/forget.jpg)

If you accidentally run an infinite recursive function, press the **Ctrl + C** keys to terminate the process.

![image](images/snake.jpg)

Inline declarations may only contain one or two statements, as the compiler recreates them at each calling point – longer inline declarations would, therefore, produce a more unwieldy program.

**Summary**

![image](images/pgc96_1.jpg)

•An **if** statement evaluates a given test expression for a Boolean value of **true** or **false**.

•Statements contained in braces after an **if** statement will only be executed when the evaluation is found to be **true**.

•The **if** and **else** keywords are used to perform conditional branching according to the result of a tested expression.

•A **switch** statement is an alternative form of conditional branching that matches a **case** statement to a given value.

•The **for** loop structure has parameters declaring an initializer, a test expression, and an incrementer or decrementer.

•A **while** loop and **do-while** loop must always have an incrementer or decrementer within their loop body.

•Any type of loop can be immediately terminated by including a **break** statement within the loop body.

•A single iteration of any type of loop can be skipped by including a **continue** statement within the loop body.

•Functions are usually declared as prototypes at the start of the program, and defined after the main function.

•Variables declared in a function are only accessible from within that function, as they only have local scope.

•Values can be passed into functions if arguments are declared in the function prototype and definition.

•Overloaded functions have the same name but a different number or type of declared arguments.

•Recursive functions repeatedly call themselves until a test condition is met.

•Short function definitions of just one or two statements can be declared in place of a prototype using the **inline** keyword.

15

**Handling strings**

***This chapter demonstrates how to manipulate C++ text strings as a simpler, more powerful alternative to character arrays.***

[Creating string variables](#chapter15.xhtml_sec118)

[Getting string input](#chapter15.xhtml_sec119)

[Solving the string problem](#chapter15.xhtml_sec120)

[Discovering string features](#chapter15.xhtml_sec121)

[Joining & comparing strings](#chapter15.xhtml_sec122)

[Copying & swapping strings](#chapter15.xhtml_sec123)

[Finding substrings](#chapter15.xhtml_sec124)

[Replacing substrings](#chapter15.xhtml_sec125)

[Summary](#chapter15.xhtml_sec126)

**Creating string variables**

Unlike the **char**, **int**, **float**, **double**, and **bool** data types, there is no native “string” data type in C++ – but its **<string>** library class provides a **string** object that emulates a string data type. To make this available to a program, the library must be added with an **#include <string>** directive at the start of the program.

![image](images/pgb62_1.jpg)

Like the **<iostream>** class library, the **<string>** library is part of the **std** namespace that is used by the C++ standard library classes. This means that a string object can be referred to as **std::string**, or more simply as **string** when a **using namespace std;** directive is included at the start of the program.

Once the **<string>** library is made available, a **string** “variable” can be declared in the same way as other variables. The declaration may optionally initialize the variable using the **=** assignment operator, or it may be initialized later in the program.

Additionally, a **string** variable may be initialized by including a text string between parentheses after the variable name.

Text strings in C++ must always be enclosed within “ ” double quote characters – ‘ ’ single quotes are only used to surround character values of the **char** data type.

A C++ **string** variable is much easier to work with than the **char** arrays that C programmers must use, as it automatically resizes to accommodate the length of any text string. At a lower level, the text is still stored as a character array, but the **string** variable lets you ignore those details. Consequently, a character array can be assigned to a **string** variable using the **=** assignment operator.

It is important to remember that when numeric values are assigned to a **string** variable, they are no longer a numeric data type, so arithmetic cannot be performed on them. For example, attempting to add **string** values of “7” and “6” with the **+** addition operator produces the concatenated **string** “76”, not the numerical value of 13\. In this case, the **+** operator recognizes that the context is not arithmetical, so adopts the guise of “concatenation operator” to unite the two strings. Similarly, the **+=** operator appends a **string** to another **string** and is useful to build long strings of text.

Several **string** values are built into a single long string in the example program described [here](#chapter15.xhtml_ecif).

![image](images/commonb.jpg)

string.cpp

![image](images/1b.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>              // Include string support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2b.jpg)Add a main function containing four **string** variable declarations and a final **return** statement

**int main()**

**{**

**string text = “9” ;**

**string term( “9 “ ) ;**

**string info = “Toys” ;**

**string color ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3b.jpg)In the main function, after the variable declarations, insert statements to declare and initialize a character array, then assign its value to the uninitialized **string** variable

**char hue[4] = { ‘R’, ’e’, ’d’, ’\0’ } ;**

**color = hue ;**

![image](images/4b.jpg)Assign a longer text **string** to one of the **string** variables

**info = “Balloons” ;**

![image](images/5b.jpg)Build a long **string** by combining all the **string** variable values in the first **string** variable, then output the combined **string** value

**text += ( term + color + info ) ;**

**cout << endl << text << endl ;**

![image](images/6b.jpg)Save, compile, and run the program to see the output

![image](images/pgb63_1.jpg)

![image](images/forget.jpg)

Remember to add the special **\0** character to mark the end of a **string** in a **char** array.

**Getting string input**

The C++ **cin** function, which was introduced in [Chapter 14](#chapter14.xhtml) to input numeric values, can also assign text input to **string** variables. This has a limitation, as it can only be used to input a single word at a time – the **cin** function stops reading the input when it encounters a space, leaving any other text in the “input buffer”.

![image](images/pgb64_1.jpg)

When you want to allow the user to input a string with spaces, such as a sentence, the **getline()** function can be used. This function requires two arguments to specify the source and destination of the string. For example, where the **cin** function is the source, and a string variable named “str” is the destination:

**getline( cin , str ) ;**

The **getline()** function reads from an input “stream” until it encounters a **\n** newline character at the end of the line – created when you hit **Return**.

Care must be taken when mixing **cin** and **getline()** functions, as the **getline()** function will automatically read anything left on the input buffer – giving the impression that the program is skipping an instruction. The **cin.ignore()** function can be used to overcome this problem by ignoring content left in the input buffer.

![image](images/commonb.jpg)

input.cpp

![image](images/1b.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>          // Include string support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2b.jpg)Add a main function containing one string variable declaration and a final **return** statement

**int main()**

**{**

**string name ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3b.jpg)In the main function, insert statements assigning the user name input to a string variable, then outputting its value

**cout << “Please enter your full name: ” ;**

**cin >> name ;**

**cout << “Welcome “ << name << endl ;**

![image](images/4b.jpg)Next, insert a statement requesting the user name again, but this time assigning the input to the **string** variable with the **getline** function before outputting its value

**cout << “Please re-enter your full name: ” ;**

**getline( cin , name ) ;**

**cout << “Thanks, “ << name << endl ;**

![image](images/5b.jpg)Save, compile, and run the program and enter your full name when requested

![image](images/pgb65_1.jpg)

This unsatisfactory result shows that **cin** reads up to the first space, leaving the second name in the input buffer, which is then read by **getline()** and subsequently output. The problem persists even when you enter only your first name, because **cin** leaves the newline character, created when you hit **Return**, on the input buffer.

![image](images/6b.jpg)Edit the program to resolve this issue by inserting a statement, just before the call to the **getline** function, instructing it to ignore content in the input buffer

**cin.ignore( 256, ‘\n’ ) ;**

![image](images/7b.jpg)Save, compile, and run the program again, then re-enter your full name to see the program perform as required

![image](images/pgb65_2.jpg)

![image](images/forget.jpg)

Use the **cin** function for numeric input or single word input, but use the **getline()** function for string input.

![image](images/hot.jpg)

The arguments to the **cin.ignore()** function specify it should discard up to 256 characters and stop when it encounters a newline character.

**Solving the string problem**

A problem arises with **string** variables when you need to convert them to a different data type, perhaps to perform arithmetical operations with those values. As the **string** object is not a native C++ data type, a **string** variable value cannot be converted to an **int** or any other regular data type by casting.

![image](images/pgb66_1.jpg)

The solution is provided by the C++ **<sstream>** library that allows a **stringstream** object to act as an intermediary, through which **string** values can be converted to a numeric data type, and numeric values can be converted to a **string** data type. To make this ability available to a program, the library must be added with an **#include <sstream>** directive at the start of the program.

Values can be loaded into a **stringstream** object with the familiar output stream **<<** operator that is used with **cout** statements. Contents can then be extracted from a **stringstream** object with the **>>** input stream operator that is used with **cin** statements.

In order to re-use a **stringstream** object, it must first be returned to its original state. This requires its contents to be set as an empty **string** and its status bit flags to be cleared.

![image](images/commonb.jpg)

convert.cpp

![image](images/1b.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>          // Include string support.**

**#include <sstream>      // Include stringstream support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2b.jpg)Add a main function containing a final **return** statement and declaring two initialized variables to be converted

**int main()**

**{**

**string term = “100” ;**

**int number = 100 ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3b.jpg)In the main function, insert statements to declare an integer variable, **string** variable, and a **stringstream** object

**int num ;                           // To store a converted string.**

**string text ;                     // To store a converted integer.**

**stringstream stream ;   // To perform conversions.**

![image](images/4b.jpg)Next, use the stream output operator to load the initialized **string** value into the **stringstream** object

**stream << term ;          // Load the string.**

![image](images/5b.jpg)Use the stream input operator to extract content from the **stringstream** object into the uninitialized integer variable

**stream >> num ;          // Extract the integer.**

![image](images/6b.jpg)Perform arithmetic on the integer and output the result

**num /= 4 ;**

**cout << “Integer value: ” << num << endl ;**

![image](images/7b.jpg)Reset the **stringstream** object ready for re-use

**stream.str(“”) ;          // Empty the contents.**

**stream.clear() ;          // Empty the bit flags.**

![image](images/8b.jpg)Now, use the stream output operator to load the initialized integer value into the **stringstream** object

**stream << number ;     // Load the integer.**

![image](images/9b.jpg)Use the stream input operator to extract content from the **stringstream** object into the uninitialized **string** variable

**stream >> text ;          // Extract the string.**

![image](images/10b.jpg)Perform concatenation on the **string** and output the result

**text += “ Per Cent” ;**

**cout << “String value: ” << text << endl ;**

![image](images/11b.jpg)Save, compile, and run the program to see the converted output values

![image](images/pgb67_1.jpg)

![image](images/hot.jpg)

Notice how the **stringstream** object’s **str()** function is used here to reset its contents to an empty string.

![image](images/forget.jpg)

A non-empty **stringstream** object has bit flags indicating its status as good, bad, eof, or fail – these should be cleared before re-use by the **stringstream** object’s **clear()** function, as demonstrated here.

**Discovering string features**

The C++ **<string>** library provides a number of functions that make it easy to work with strings. To use them, simply add the function name after the **string** variable name and a dot. For example, with a **stringstream** variable named “msg” you can call upon the **size()** function, to return its character length, with **msg.size()**.

![image](images/pgb68_1.jpg)

A **string** variable can be emptied of all characters by assigning it an empty string with two double quotes without spacing – as **“”**, or alternatively by calling the **<string>** library’s **clear()** function.

Unlike a **char** array, a **string** variable will dynamically enlarge to accommodate the number of characters assigned to it, and its current memory size can be revealed with the **<string>** library’s **capacity()** function. Once enlarged, the allocated memory size remains, even when a smaller **string** gets assigned to the variable.

The **<string>** library’s **empty()** function returns a Boolean **true** (1) or **false** (0) response to reveal whether the string is empty or not.

![image](images/commonb.jpg)

features.cpp

![image](images/1b.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>          // Include string support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2b.jpg)Below the preprocessor directives, declare a function prototype with a single **string** data type argument

**void computeFeatures( string ) ;**

![image](images/3b.jpg)Add a main function containing a final **return** statement and declaring an initialized **string** variable

**int main()**

**{**

**string text = “C++ is fun” ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/4b.jpg)After the main function, define the declared function to display the **string** variable value when called

**void computeFeatures( string text )**

**{**

**cout << endl << “String: ” << text << endl ;**

**}**

![image](images/hot.jpg)

The **length()** function can be used in place of the **size()** function to reveal the size of a string value.

![image](images/5b.jpg)In the function definition, add statements to output features of the **string** variable

**cout << “Size: ” << text.size() ;**

**cout << “   Capacity: ” << text.capacity() ;**

**cout << “   Empty?: ” << text.empty() << endl ;**

![image](images/6b.jpg)In the main function, insert a call to the defined function

**computeFeatures( text ) ;**

![image](images/7b.jpg)Next, in the main function, insert a statement to enlarge the **string** value and call the function to see its features

**text += “ for everyone” ;**

**computeFeatures( text ) ;**

![image](images/8b.jpg)Now, insert a statement to reduce the **string** value

**text = “C++ Fun” ;**

**computeFeatures( text ) ;**

![image](images/9b.jpg)Finally, insert a statement to empty the **string** variable

**text.clear() ;**

**computeFeatures( text ) ;**

![image](images/10b.jpg)Save, compile, and run the program to see the output

![image](images/pgb69_1.jpg)

![image](images/hot.jpg)

The **empty()** function is useful to check if the user has entered requested input.

![image](images/forget.jpg)

A space occupies one memory element – just like a character does.

**Joining & comparing strings**

When the **+** operator is used to concatenate strings in an assignment, the combined strings get stored in the **string** variable. But when it is used with the **cout** function, the strings are only combined in the output – the variable values are unchanged.

![image](images/pgb70_1.jpg)

The **<string>** library’s **append()** function can also be used to concatenate strings, specifying the **string** value to append as an argument within its parentheses. When this is used with the **cout** function, the strings are combined in the variable, then its value written as output – in this case, the variable value does change.

String comparisons can be made, in the same way as numeric comparisons, with the **==** equality operator. This returns **true** (1) when both strings precisely match, otherwise it returns **false** (0).

Alternatively, the **<string>** library’s **compare()** function can be used to compare a **string** value specified as its argument. Unlike the **==** equality comparison, the **compare()** function returns 0 when the strings are identical, by examining the **string** value’s combined ASCII code values. When the **string** argument totals more than the first string, it returns -1, otherwise it returns 1.

![image](images/commonb.jpg)

compare.cpp

![image](images/1b.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>          // Include string support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2b.jpg)Add a main function containing a final **return** statement and declaring three initialized **string** variables

**int main()**

**{**

**string lang = “C++” ;**

**string term = “ Programming” ;**

**string text = “C++ Programming” ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3b.jpg)In the main function, insert statements to output two **string** values combined with the **+** concatenate operator and the (unchanged) value of the first variable

**cout << “Concatenated: ” << ( lang + term ) << endl ;**

**cout << “Original: ” << lang << endl ;**

![image](images/4b.jpg)Next, insert statements to output two **string** values combined with the **append()** function and the (changed) value of the first variable

**cout << “Appended: ” << lang.append( term ) << endl ;**

**cout << “Original: ” << lang << endl << endl ;**

![image](images/5b.jpg)Use the **==** equality operator to compare two **string** values that differ, then two **string** values that match

**cout << “Differ: ” << ( lang == term ) << endl ;**

**cout << “Match: ” << ( lang == text ) << endl << endl ;**

![image](images/6b.jpg)Now, use the **compare()** function to compare three **string** values, examining their ASCII code total values

**cout << “Match: ” << lang.compare( text ) << endl ;**

**cout << “Differ: ” << lang.compare( term ) << endl ;**

**cout << “Lower ASCII: ” <<** **lang.compare( “zzzzz” ) << endl ;**

![image](images/7b.jpg)Save, compile, and run the program to see the output

![image](images/pgb71_1.jpg)

![image](images/forget.jpg)

The **+=** assignment operator can also be used to append a string.

![image](images/hot.jpg)

In comparisons, character order is taken into account – so comparing “za” to “az” reveals that “za” has a greater total. In terms of ASCII values, ‘a’ is 97, and ‘z’ is 122.

**Copying & swapping strings**

String values can be assigned to a **string** variable by the **=** assignment operator, or by the **<string>** library’s **assign()** function. This function specifies the **string** value to be copied to the variable as an argument within its parentheses.

![image](images/pgb72_1.jpg)

Optionally, the **assign()** function can copy just a part of the specified **string** value by stating the position of the starting character as a second argument, and the number of characters to copy as a third argument.

The contents of a **string** variable can be exchanged for that of another **string** variable by the **<string>** library’s **swap()** function. In this case, the contents of the first variable receives those of the second variable, which in turn receives those of the first variable.

![image](images/commonb.jpg)

swap.cpp

![image](images/1b.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>          // Include string support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2b.jpg)Add a main function containing a final **return** statement and declaring three **string** variables – with one initialized

**int main()**

**{**

**string front ;**

**string back ;**

**string text =**

**“Always laugh when you can. It\’s cheap medicine.” ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3b.jpg)In the main function, insert a statement to assign the entire value of the initialized **string** variable to the first uninitialized **string** variable

**front.assign( text ) ;**

![image](images/4b.jpg)Next, insert a statement to output the newly assigned **string** value

**cout << endl << “Front: ” << front << endl ;**

![image](images/5b.jpg)Now, insert a statement to assign only the first 27 characters of the initialized variable to the first variable

**front.assign( text, 0, 27 ) ;**

![image](images/6b.jpg)Output the newly assigned **string** value

**cout << endl << “Front: ” << front << endl ;**

![image](images/7b.jpg)Next, assign only the last part of the initialized **string** variable to the second uninitialized variable, starting at character (element) 27

**back.assign ( text, 27 , text.size() ) ;**

![image](images/8b.jpg)Now, output this newly assigned **string** value

**cout << “Back: ” << back << endl ;**

![image](images/9b.jpg)Finally, exchange the assigned **string** values contained in the first and second **string** variables, then output the exchanged values

**back.swap( front ) ;**

**cout << endl << “Front: ” << front << endl ;**

**cout << “Back: ” << back << endl ;**

![image](images/10b.jpg)Save, compile, and run the program to see the output

![image](images/pgb73_1.jpg)

![image](images/hot.jpg)

Use the **=** assignment operator to assign complete strings, and the **assign()** function to assign partial strings.

![image](images/hot.jpg)

Use the **swap()** function wherever possible, rather than creating additional string variables.

**Finding substrings**

A **string** value can be searched to see if it contains a specified “substring” using the **find()** function of the **<string>** library. Its parentheses should specify the substring to seek as its first argument, and the index number of the character at which to start searching as its second argument.

![image](images/pgb74_1.jpg)

When a search successfully locates the specified substring, the **find()** function returns the index number of the first occurrence of the substring’s first character within the searched string. When the search fails, **find()** returns a value of -1 to indicate failure.

There are several other functions in the **<string>** library that are related to the **find()** function. Two of these are the **find_first_of()** function and the **find_first_not_of()** function. Instead of seeking the first occurrence of a complete **string**, as **find()** does, the **find_first_of()** function seeks the first occurrence of any of the characters in a specified **string**, and **find_first_not_of()** seeks the first occurrence of a character that is not in the specified **string**.

The **find_last_of()** and **find_last_not_of()** functions work in a similar manner – but begin searching at the end of the **string** then move forward.

![image](images/commonb.jpg)

find.cpp

![image](images/1b.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>          // Include string support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2b.jpg)Add a main function containing a final **return** statement, an initialized string variable declaration, and declaring an integer variable to store search results

**int main()**

**{**

**string text = “I can resist anything but temptation.” ;**

**int num ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3b.jpg)In the main function, insert statements to output the start position of a substring within the entire **string** variable

**num = text.find( “resist”, 0 ) ;**

**cout << “Position: ” << num << endl ;**

![image](images/4b.jpg)Next, insert a statement to seek a non-existent substring within the entire **string** variable and output the result

**num = text.find( “nonsuch” , 0 ) ;**

**cout << “Result: ” << num << endl ;**

![image](images/5b.jpg)Now, insert a statement to output the start position of the first occurrence of any characters in an “If” substring found within the entire **string** variable

**num = text.find_first_of( “If” ) ;**

**cout << “First I: ” << num << endl ;**

![image](images/6b.jpg)Insert a statement to report the string position of the first character not within the “If” substring

**num = text.find_first_not_of( “If” ) ;**

**cout << “First not I: ” << num << endl ;**

![image](images/7b.jpg)Next, insert a statement to seek the last occurrence of the letter “t” within the **string** variable and output its position

**num = text.find_last_of( “t” ) ;**

**cout << “Last t: ” << num << endl ;**

![image](images/8b.jpg)Now, add a statement to report the **string** position of the last character within the **string** variable that is not a “t”

**num = text.find_last_not_of( “t” ) ;**

**cout << “Last not t: ” << num << endl ;**

![image](images/9b.jpg)Save, compile, and run the program to see the search results indicating failure or the positions when located

![image](images/pgb75_1.jpg)

![image](images/snake.jpg)

The searches are case sensitive, so seeking “If” and “if” may produce different results – here, uppercase ‘I’ matches.

![image](images/forget.jpg)

The first character in a string is at position 0, not at position 1.

**Replacing substrings**

The **<string>** library contains a number of useful functions to manipulate substrings. A **string** can be inserted into another **string** using the **insert()** function. This requires the index position at which the **string** should be inserted as its first argument, and the **string** value to be inserted as its second argument.

![image](images/pgb76_1.jpg)

Conversely, a substring can be removed from a **string** using the **erase()** function. This requires the index position at which it should begin erasing as its first argument, and the number of characters to be erased as its second argument.

The **replace()** function neatly combines the **erase()** and **insert()** functions to both remove a substring and insert a replacement. It requires three arguments specifying the position at which it should begin erasing, the number of characters to be erased, and the replacement **string** to be inserted at that position.

A substring can be copied from a **string** using the **substr()** function, stating the index position at which it should begin copying as its first argument, and the number of characters to be copied as its second argument.

The character at any specified position within a **string** can be copied using the **at()** function, which requires the index position as its argument. The final character in a **string** always has an element index number one less than the length of the **string** – because index numbering starts at 0, not 1.

![image](images/commonb.jpg)

sub.cpp

![image](images/1b.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>          // Include string support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2b.jpg)Add a main function containing a final **return** statement, an initialized **string** variable declaration, and a statement outputting the **string** variable value

**int main()**

**{**

**string text = “I do like the seaside” ;**

**cout << “Original: ” << text << endl ;**

**// Add more statements here.**

return **0** ;

**}**

![image](images/3b.jpg)In the main function, insert statements to insert a substring into the variable value at index position 10, and to output the modified **string**

**text.insert( 10, “to be beside “ ) ;**

**cout << “Inserted: ” << text << endl ;**

![image](images/4b.jpg)Next, insert statements to erase two characters from the modified **string** value starting at index position 3, and to output the revised **string**

**text.erase( 2, 3 ) ;**

**cout << “Erased: ” << text << endl ;**

![image](images/5b.jpg)Now, insert statements to remove 25 characters at index position 7, insert a replacement substring, then output the revised **string** again

**text.replace( 7, 25, “strolling by the sea” ) ;**

**cout << “Replaced: ” << text << endl ;**

![image](images/6b.jpg)Finally, insert statements to output nine copied characters at index position 7, and to output the final character in the string

**cout << “Copied: ” << text.substr( 7, 9 ) << endl ;**

**cout << “Last character: ” <<** **text.at( text.size() - 1 ) << endl ;**

![image](images/7b.jpg)Save, compile, and run the program to see the output showing how the **string** has been manipulated

![image](images/pgb77_1.jpg)

![image](images/hot.jpg)

The **insert()** function can optionally have a third and fourth argument – specifying the position in the substring at which to begin copying, and the number of characters to be copied.

![image](images/hot.jpg)

The **replace()** function can optionally have a fourth and fifth argument – specifying the position in the substring at which to begin copying, and the number of characters to be copied.

**Summary**

![image](images/pgb24_1.jpg)

•The C++ **<string>** library provides a “string” object that emulates a data type – so that **string** variables can be created.

•Arithmetic cannot be performed on numeric values assigned to **string** variables until they are converted to a numeric data type.

•The standard **cin** function reads from standard input until it encounters a space, so can be used to input a single word, and provides an **ignore()** function to disregard the input buffer.

•The **getline()** function reads from standard input until it encounters a newline, so can be used to input a string of text.

•The C++ **<sstream>** library provides a “stringstream” object that acts an intermediary to convert strings to other data types.

•A **string** variable can be emptied by assigning it an empty string ( **= “”** ) or by calling its **clear()** function.

•Features of a **string** variable can be revealed by calling its **size()**, **capacity()**, and **empty()** functions.

•Multiple **string** values can be concatenated by the **+** operator.

•A **string** can be appended to another **string** by the **+=** operator or by calling its **append()** function.

•A **string** can be compared to another **string** by the **==** operator or by calling its **compare()** function.

•A **string** value can be assigned to a **string** variable using the **=** operator or by calling its **assign()** function.

•The **swap()** function swaps the values of two **string** variables.

•Substrings of a **string** can be sought with the **find()** function, or specialized functions such as **find_first_of()**, and a character retrieved from a specified index position by the **at()** function.

•A substring can be added to a **string** by its **insert()** function, removed by its **erase()** function, replaced by its **replace()** function, or copied by its **substr()** function.

16

**Reading and writing files**

***This chapter demonstrates how to store and retrieve data in text files, and illustrates how to avoid errors in C++ programs.***

[Writing a file](#chapter16.xhtml_sec127)

[Appending to a file](#chapter16.xhtml_sec128)

[Reading characters & lines](#chapter16.xhtml_sec129)

[Formatting with getline](#chapter16.xhtml_sec130)

[Manipulating input & output](#chapter16.xhtml_sec131)

[Predicting problems](#chapter16.xhtml_sec132)

[Recognizing exceptions](#chapter16.xhtml_sec133)

[Handling errors](#chapter16.xhtml_sec134)

[Summary](#chapter16.xhtml_sec135)

**Writing a file**

The ability to read and write files from a program provides a useful method of maintaining data on the computer’s hard disk. The format of the data may be specified as human-readable plain text format or machine-readable binary format.

![image](images/pgb80_1.jpg)

The standard C++ **<fstream>** library provides functions for working with files, which can be made available by adding an **#include <fstream>** directive at the start of the program.

For each file that is to be opened, a filestream object must first be created. This will be either an “ofstream” (output filestream) object, for writing data to the file, or an “ifstream” (input filestream) object, for reading data from the file. The **ofstream** object is used like the **cout** function that writes to standard output, and the **ifstream** object works like the **cin** function that reads from standard input.

The declaration of a filestream object for writing output begins with the **ofstream** keyword, then a chosen name for that particular filestream object followed by parentheses nominating the text file to write to. So, the declaration syntax looks like this:

**ofstream *object-name* ( *“file-name”* ) ;**

The argument nominating the text file may optionally contain the full file path, such as **“C:\data\log.txt”** or **“/home/user/log.txt”**, otherwise the program will seek the file within the directory in which the program resides.

Before writing output to a file, the program should always first test that the filestream object has actually been created. Typically, this is performed by an **if** statement that allows the program to write output only when the test is successful.

If a nominated file already exists, it will by default be overwritten without warning. Otherwise, a new file will be created and written.

![image](images/snake.jpg)

The nominated file name or path must be enclosed within double quotes, like a **string**.

After writing output to a nominated file, the program should always call the associated filestream object’s **close()** function to close the output filestream.

The program described opposite first builds a string for writing as output. This is written to a nominated file when the filestream object has been successfully created, then the filestream is closed.

![image](images/commonr.jpg)

write.cpp

![image](images/1r.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <fstream>          // Include filestream support.**

**#include <string>**

**#include <iostream>**

**using namespace std ;**

![image](images/2r.jpg)Add a main function containing a final **return** statement and building a lengthy text string in a **string** variable

**int main()**

**{**

**string poem = “\n\tI never saw a man who looked” ;**

**poem.append( “\n\tWith such a wistful eye” ) ;**

**poem.append( “\n\tUpon that little tent of blue” ) ;**

**poem.append( “\n\tWhich prisoners call the sky” ) ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3r.jpg)In the main function, create an output filestream object

**ofstream writer( “poem.txt” ) ;**

![image](images/4r.jpg)Insert statements to write the **string** to a file or exit, then save, compile, and run the program to see the result

**if ( ! writer )**

**{**

**cout << “Error opening file for output” << endl ;**

**return -1 ;        // Signal an error then exit the program.**

**}**

**writer << poem << endl ;          // Write output.**

**writer.close() ;                          // Close filestream.**

![image](images/pgb81_1.jpg)

![image](images/hot.jpg)

String values can contain **\n** newline and **\t** tab escape sequences for formatting lines.

![image](images/forget.jpg)

Notice how the newline and tab characters are preserved in the text file.

**Appending to a file**

![image](images/pgb82_1.jpg)

When a filestream object is created, the parentheses following its chosen name can optionally contain additional arguments, specifying a range of file “modes” to control the behavior of that filestream object. These file modes are part of the **ios** namespace, so must be explicitly addressed using that prefix. Each file mode is listed in the table below, together with a behavior description:

| **Mode** | **Behavior**  |
| **ios::out** | Open a file to write output |
| **ios::in** | Open a file to read input  |
| **ios::app** | Open a file to append output at the end of any existing content  |
| **ios::trunc** | Truncate the existing file (default behavior)  |
| **ios::ate** | Open a file without truncating and allow data to be written anywhere in the file  |
| **ios::binary** | Treat the file as binary format rather than text so the data may be stored in non-text format  |

Multiple modes may be specified if they are separated by a “|” pipe character. For example, the syntax of a statement to open a file for binary output looks like this:

**ofstream *object-name* ( *“file-name”* , ios::out|ios::binary ) ;**

The default behavior when no modes are explicitly specified regards the file as a text file that will be truncated after writing.

The most commonly specified mode is **ios::app**, which ensures existing content will be appended, rather than overwritten, when new output is written to the nominated file.

The program described opposite appends data to the text file created in the previous example.

![image](images/forget.jpg)

The preprocessor directive **using namespace std;** allows the **std** namespace prefix to be omitted – so **cout** refers to the **std::cout** function. The **ios** namespace exists within the **std** namespace – so the file modes can be explicitly addressed using both namespace prefixes – for example, **std::ios::out**

![image](images/commonr.jpg)

append.cpp

![image](images/1r.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <fstream>     // Include filestream support.**

**#include <string>**

**#include <iostream>**

**using namespace std ;**

![image](images/2r.jpg)Add a main function containing a final **return** statement and building a text string in a **string** variable

**int main()**

**{**

**string info = “\n\tThe Ballad of Reading Gaol” ;**

**info.append( “\n\t\t\tOscar Wilde 1898” ) ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3r.jpg)In the main function, create an output filestream object – specifying a file mode that will append to existing text

**ofstream writer( “poem.txt” , ios::app ) ;**

![image](images/4r.jpg)Insert statements to append the **string** to a file or exit, then save, compile, and run the program to see the result

**if ( ! writer )**

**{**

**cout << “Error opening file for output” << endl ;**

**return -1 ;        // Signal an error then exit the program.**

**}**

**writer << info << endl ;          // Append output.**

**writer.close() ;                       // Close filestream.**

![image](images/pgb83_1.jpg)

![image](images/snake.jpg)

The file must allow the program suitable read and write permissions.

**Reading characters & lines**

The **ifstream** filestream object has a **get()** function that can be used in a loop to read a file and assign each character in turn to the **char** variable specified as its argument:

![image](images/commonr.jpg)

read.cpp

![image](images/1r.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <fstream>          // Include filestream support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2r.jpg)Add a main function containing a final **return** statement and two variable declarations – one variable to store a character and another to count loop iterations

**int main()**

**{**

**char letter ;**

**int i ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3r.jpg)In the main function, create an input filestream object to read the text file from the previous example

**ifstream reader( “poem.txt” ) ;**

![image](images/4r.jpg)Insert statements to exit unless the filestream object exists

**if ( ! reader )**

**{**

**cout << “Error opening input file” << endl ;**

**return -1 ;       // Signal an error then exit the program.**

**}**

![image](images/5r.jpg)Next, insert a loop to read the text file, assigning each character in turn to the variable and outputting its value

**else**

**for ( i = 0 ; ! reader.eof() ; i++ )**

**{**

**reader.get( letter ) ;**

**cout << letter ;**

**}**

![image](images/6r.jpg)Finally, insert statements to close the filestream and output the total number of loop iterations

**reader.close() ;**

**cout << “Iterations: ” << i << endl ;**

![image](images/hot.jpg)

Notice how the **ifstream eof()** function is used to check if the “end of file” has been reached.

![image](images/7r.jpg)Save, compile, and run the program to see the text file contents and loop count get displayed on standard output

![image](images/pgb85_2.jpg)

![image](images/pgb85_1.jpg)

This program works well enough but the loop must make many iterations to output the text file contents. Efficiency could be improved by reading a line on each iteration of the loop:

![image](images/8r.jpg)Insert a preprocessor directive to make the C++ string library available to the program

**#include <string>**

![image](images/9r.jpg)Replace the **char** variable declaration with a **string** variable declaration

**string line ;**

![image](images/10r.jpg)Replace both statements in the **for** loop to read lines, then save, compile, and run the program once more

**getline( reader , line ) ;**

**cout << line << endl ;**

![image](images/pgb85_3.jpg)

![image](images/forget.jpg)

Output an **endl** after each line output – because **getline()** stops reading when it meets a **\n** newline character.

**Formatting with getline**

The **getline()** function can optionally have a third argument to specify a delimiter at which to stop reading a line. This can be used to separate text read from a tabulated list in a data file:

![image](images/commonr.jpg)

format.cpp

![image](images/1r.jpg)In a plain text editor, create a text file containing 12 items of data of four items per line, each separated by a tab

![image](images/pgb86_1.jpg)

![image](images/2r.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <fstream>      // Include filestream support.**

**#include <string>**

**#include <iostream>**

**using namespace std ;**

![image](images/3r.jpg)Add a main function containing a final **return** statement and four variable declarations – a fixed number, a **string** array to store data, and two counter variables set to 0

**int main()**

**{**

**const int RANGE = 12 ;**

**string tab[ RANGE ] ;**

**int i = 0 , j = 0 ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/4r.jpg)Insert a statement to create an input filestream object

**ifstream reader( “records.txt” ) ;**

![image](images/5r.jpg)Insert statements to exit unless the filestream object exists

**if ( ! reader )**

**{**

**cout << “Error opening input file” << endl ;**

**return -1 ;**

**}**

![image](images/forget.jpg)

The **string** array must have a sufficient number of elements to store each item of data – it would need to be enlarged to handle more records.

![image](images/6r.jpg)Next, insert a loop that will read each line into the **string** array – reading up to a **\t** tab for the first three items and up to a **\n** newline for the fourth item on each line

**while ( ! reader.eof() )**

**{**

**if ( ( i + 1 ) % 4 == 0 )**

**getline( reader, tab[ i++ ], ‘\n’ ) ;**

**else**

**getline( reader, tab[ i++ ], ‘\t’ ) ;**

**}**

![image](images/pgb87_1.jpg)

![image](images/7r.jpg)Now, close the filestream and reset the counter

**reader.close() ;**

**i = 0 ;**

![image](images/8r.jpg)Insert a second loop to output the data stored in each array element, formatted with descriptions and newlines

**while ( i < RANGE )**

**{**

**cout << endl << “Record Number: ” << ++j << endl ;**

**cout << “Forename: ” << tab[ i++ ] << endl ;**

**cout << “Surname: ” << tab[ i++ ] << endl ;**

**cout << “Department: ” << tab[ i++ ] << endl ;**

**cout << “Telephone: ” << tab[ i++ ] << endl ;**

**}**

![image](images/9r.jpg)Save, compile, and run the program to see the formatted output from the text file

![image](images/pgb87_2.jpg)

![image](images/hot.jpg)

The **if** statement tests if the item number (element number plus 1) is exactly divisible by four, to determine whether to read up to a newline or tab character.

![image](images/snake.jpg)

The record counter must use a prefix incrementer to increase the variable value before it is output.

**Manipulating input & output**

The behavior of input and output streams can be modified using “insertion operators” with the **cout** and **cin** functions. Specifying an integer argument to their **width()** function sets the stream character width. Where the content does not fill the entire stream width, a fill character may be specified as the argument to their **fill()** function to indicate the empty portion. Similarly, the default precision of six decimal places for floating point numbers can be changed by specifying an integer to their **precision()** function. Statements using insertion operators to modify a stream should be made before those using the **<<** or **>>** operators.

![image](images/pgb88_1.jpg)

The **<iostream>** library provides the “manipulators” listed in the table below, which modify a stream using the **<<** or **>>** operators.

| **Manipulator** | **Display** |
| **noboolalpha*** | Boolean values as 1 or 0 |
| **boolalpha** | Boolean values as “true” or “false” |
| **dec*** | Integers as base 10 (decimal) |
| **hex** | Integers as base 16 (hexadecimal) |
| **oct** | Integers as base 8 (octal) |
| **right*** | Text right-justified in the output width |
| **left** | Text left-justified in the output width |
| **internal** | Sign left-justified, number right-justified |
| **noshowbase*** | No prefix indicating numeric base |
| **showbase** | Prefix indicating numeric base |
| **noshowpoint*** | Whole number only when a fraction is 0 |
| **showpoint** | Decimal point for all floating point numbers |
| **noshowpos*** | No + prefix before positive numbers |
| **showpos** | Prefix positive numbers with a + sign |
| **noskipws*** | Do not skip whitespace for >> input |
| **skipws** | Skip whitespace for >> input |
| **fixed*** | Floating point numbers to six decimal places |
| **scientific** | Floating point numbers in scientific notation |
| **nouppercase*** | Scientific as e and hexadecimal number as ff |
| **uppercase** | Scientific as E and hexadecimal number as FF |

![image](images/forget.jpg)

Insertion operators modify just one stream object – subsequent stream objects use the defaults, unless they too get modified first by insertion operators.

![image](images/hot.jpg)

Manipulators marked with an * are the default behaviors.

![image](images/commonr.jpg)

manipulate.cpp

![image](images/1r.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2r.jpg)Add a main function containing a final **return** statement and declaring two initialized variables

**int main()**

**{**

**bool isTrue = 1 ;**

**int num = 255 ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3r.jpg)In the main function, insert statements to set the width and fill of an output stream, then output a text string on it

**cout.width( 40 ) ;**

**cout.fill( ‘.’ ) ;**

**cout << “Output” << endl ;**

![image](images/4r.jpg)Next, insert statements to set the precision of an output stream to stop truncation of decimal places – then output a floating point number showing all its decimal places

**cout.precision( 11 ) ;**

**cout << “Pi: ” << 3.1415926536 << endl ;**

![image](images/5r.jpg)Now, insert statements that use manipulators to output the variable values in modified formats

**cout << isTrue << “: ” << boolalpha << isTrue << endl ;**

**cout << num << “: ” << hex << showbase** **<< uppercase << num << endl ;**

![image](images/6r.jpg)Save, compile, and run the program to see the output

![image](images/pgb89_1.jpg)

![image](images/snake.jpg)

Manipulators affect all input or output on that stream. For example, the **boolalpha** manipulator will display all Boolean values on that stream in written form.

**Predicting problems**

![image](images/pgb90_1.jpg)

Despite the best efforts of the programmer, C++ programs may unfortunately contain one or more of these three types of bugs:

•**Syntax errors** – the code contains incorrect use of the C++ language. For example, an opening brace does not have a matching closing brace.

•**Logic errors** – the code is syntactically correct, but attempts to perform an operation that is illegal. For example, the program may attempt to divide a number by zero, causing an error.

•**Exception errors** – the program runs as expected until an exceptional condition is encountered that crashes the program. For example, the program may request a number, which the user enters in word form rather than in numeric form.

The C++ standards allow the compiler to spot “compile-time” errors involving syntax and logic, but the possibility of exceptional errors is more difficult to locate as they only occur at “run-time”. This means that the programmer must try to predict problems that may arise and prepare to handle those exceptional errors.

The first step is to identify which part of the program code that may, under certain conditions, cause an exception error. This can then be surrounded by a “try” block, which uses the **try** keyword and encloses the suspect code within a pair of braces.

![image](images/hot.jpg)

Always consider that the user will perform the unexpected – then ensure your programs can handle those actions.

When an exception error occurs, the **try** block then “throws” the exception out to a “catch” block, which immediately follows the **try** block. This uses the **catch** keyword and encloses statements to handle the exception error within a pair of braces.

The program described [here](#chapter16.xhtml_osit) has a **try** block containing a loop that increments an integer. When the integer reaches 5, a **throw()** function manually throws an exception to the **catch** block exception handler, passing the integer argument.

![image](images/commonr.jpg)

try.cpp

![image](images/1r.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2r.jpg)Add a main function containing a final **return** statement and declaring an integer variable for increment by a loop

**int main()**

**{**

**int number ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3r.jpg)In the main function, insert **try** and **catch** blocks to handle a “bad number” exception

**try**

**{            }**

**catch ( int num )**

**{            }**

![image](images/4r.jpg)In the **try** block, insert a loop to increment the variable

**for ( number = 1 ; number < 21 ; number++ )**

**{**

**if (number > 4 ) throw ( number ) ;**

**else**

**cout << “Number: ” << number << endl ;**

**}**

![image](images/5r.jpg)In the **catch** block, insert an exception handler statement

**cout << “Exception at: ” << num << endl ;**

![image](images/6r.jpg)Save, compile, and run the program to see the thrown exception get caught by the **catch** block

![image](images/pgb91_1.jpg)

![image](images/forget.jpg)

When an exception occurs, control passes to the **catch** block – in this example, the loop does not complete.

**Recognizing exceptions**

When a program exception occurs within a **try** block, an “exception” object is automatically thrown. A reference to the exception can be passed to the associated **catch** block in the parentheses after the **catch** keyword. This specifies the argument to be an **exception** type, and a chosen exception name prefixed by the **&** reference operator – for example, **exception &error**.

![image](images/pgb92_1.jpg)

Once an exception reference is passed to a **catch** block, an error description can be retrieved by the exception’s **what()** function:

![image](images/commonr.jpg)

what.cpp

![image](images/1r.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>          // Include string support.**

**#include <iostream>**

**using namespace std ;**

![image](images/2r.jpg)Add a main function containing a final **return** statement and declaring an initialized **string** variable

**int main()**

**{**

**string lang = “C++” ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3r.jpg)In the main function, insert a **try** block containing a statement attempting to erase part of the **string** variable

**try { lang.erase( 4, 6 ) ; }**

![image](images/4r.jpg)Next, insert a **catch** block containing a statement to send a description to standard error output by the **cerr** function

**catch ( exception &error )**

**{ cerr << “Exception: ” << error.what() << endl ; }**

![image](images/5r.jpg)Save, compile, and run the program to see the error description of the caught exception

![image](images/pgb92_2.jpg)

![image](images/forget.jpg)

The error description will vary for different compilers – the Visual C++ compiler describes the exception error in this example as an “invalid string position”.

The C++ **<stdexcept>** library defines a number of exception classes. Its base class is named “exception”, from which other classes are derived, categorizing common exceptions.

Each of the exception classes are listed in the table below, illustrating their relationship and describing their exception type:

![image](images/pgb93_1.jpg)

![image](images/hot.jpg)

The **cout** function sends data to standard output, whereas the **cerr** function sends error data to standard error output. These are simply two different data streams.

When the **<stdexcept>** library is made available to a program, by adding an **#include <stdexcept>** preprocessor directive, the exception classes can be used to identify the type of exception thrown to a **catch** block.

The specific exception class name can appear, in place of the general **exception** type, within the **catch** block’s parentheses.

![image](images/hot.jpg)

The example described [here](#chapter16.xhtml_sec134) demonstrates the use of standard exceptions, and you will find more on references in [Chapter 17](#chapter17.xhtml).

Multiple **catch** blocks can be used in succession, much like **case** statements in a **switch** block, to handle several types of exception.

Additionally, exceptions can be produced manually by the **throw** keyword. This can be used to create any of the **logic_error** and **runtime_error** exceptions in the table above. Optionally, a custom error message can be specified for manual exceptions, which can be retrieved by its **what()** function.

**Handling errors**

Exception type information can be provided by including the C++ standard **<typeinfo>** library. Its **typeid()** function accepts an exception argument so its **name()** function can return the type name:

![image](images/commonr.jpg)

except.cpp

![image](images/1r.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <stdexcept>   // Support standard exceptions.**

**#include <typeinfo>      // Support type information.**

**#include <fstream>**

**#include <string>**

**#include <iostream>**

**using namespace std ;**

![image](images/2r.jpg)Add a main function containing a final **return** statement, two initialized variable declarations, and a statement outputting a text message

**int main()**

**{**

**string lang = “C++” ;**

**int num = 1000000000 ; // One billion.**

**// Try-catch block goes here.**

**cout << “Program continues...” << endl ;**

**return 0 ;**

**}**

![image](images/3r.jpg)In the main function, insert a **try** block containing a statement attempting to replace part of the **string** value

**try { lang.replace( 100, 1 , “C” ) ; }**

![image](images/4r.jpg)After the **try** block, add a **catch** block to handle a range exception then save, compile, and run the program

**catch ( out_of_range &e )**

**{**

**cerr << “Range Exception: ” << e.what() << endl ;**

**cerr << “Exception Type: ” << typeid( e ).name() ;**

**cerr << endl << “Program terminated.” << endl ;**

**return -1 ;**

**}**

![image](images/pgb94_1.jpg)

![image](images/forget.jpg)

The **out_of_range** error occurs because the **replace()** function is trying to begin erasing at the 100th character, but the **string** variable has only three characters.

![image](images/5r.jpg)Replace the statement in the **try** block with one attempting to resize the **string** variable

**lang.resize( 3 * num ) ;**

![image](images/pgb95_1.jpg)

![image](images/6r.jpg)After the **catch** block, add a second **catch** block to handle general exceptions

**catch ( exception &e )**

**{**

**cerr << “Exception: ” << e.what() << endl ;**

**cerr << “Exception Type: ” << typeid( e ).name() << endl ;**

**}**

![image](images/7r.jpg)Save, compile, and run the program again to see the exception handled by the second **catch** block

![image](images/pgb95_2.jpg)

![image](images/8r.jpg)Replace the statement in the **try** block with one attempting to open a non-existent file

**ifstream reader( “nonsuch.txt” ) ;**

**if ( ! reader ) throw logic_error( “File not found” ) ;**

![image](images/9r.jpg)Save, compile, and run the program once more to see the exception handled again by the second **catch** block, and the specified custom error message

![image](images/pgb95_3.jpg)

![image](images/snake.jpg)

The order of **catch** blocks can be important – placing the **exception** error handler before the **out_of_range** error handler would allow an **out_of_range** error to be handled by the (higher level) **exception** handler.

![image](images/hot.jpg)

An exception object is typically given the name “e” – as seen here.

**Summary**

![image](images/pgb168_1.jpg)

•The C++ **<fstream>** library provides functions for working with files as **ifstream** input or **ofstream** output stream objects.

•Upon completion, a stream’s **close()** function should be called.

•File modes can be used to control the behavior of a stream.

•An input stream’s **get()** function reads one character at a time.

•The **getline()** function can be used to read a line at a time from an input stream.

•Optionally, the **getline()** function can have a third argument specifying a delimiter character at which to stop reading.

•Insertion operators can be used with the **cin** and **cout** functions to modify their behavior.

•The **cout.width()** function sets the width of the output stream.

•The **cout.fill()** function specifies a character to occupy any empty portion of the output.

•The **cout.precision()** function determines how many decimal places to display when the output is a floating point number.

•A badly performing program may contain syntax errors, logic errors, or exception errors.

•A **try** block can be used to enclose statements that, under certain conditions, may cause an exception error.

•A **catch** block can be used to handle exception errors produced in its associated **try** block.

•Exception errors that occur in a **try** block are automatically thrown to the associated **catch** block, or can be manually thrown using the **throw()** function.

•The C++ **<stdexcept>** library defines a number of exception classes that categorize common exceptions, and the **<typeinfo>** library provides exception type information.

17

**Pointing to data**

***This chapter demonstrates how to produce efficient C++ programs, utilizing pointers and references.***

[Understanding data storage](#chapter17.xhtml_sec136)

[Getting values with pointers](#chapter17.xhtml_sec137)

[Doing pointer arithmetic](#chapter17.xhtml_sec138)

[Passing pointers to functions](#chapter17.xhtml_sec139)

[Making arrays of pointers](#chapter17.xhtml_sec140)

[Referencing data](#chapter17.xhtml_sec141)

[Passing references to functions](#chapter17.xhtml_sec142)

[Comparing pointers & references](#chapter17.xhtml_sec143)

[Summary](#chapter17.xhtml_sec144)

**Understanding data storage**

In order to understand C++ pointers it is helpful to understand how data is stored on your computer. Envision the computer’s memory as a very long row of sequentially-numbered slots, which can each contain one byte of data. When a variable is declared in a program, the machine reserves a number of slots at which to store data assigned to that variable. The number of slots it reserves depends upon the variable’s data type. When the program uses the variable name to retrieve stored data, it actually addresses the number of the variable’s first reserved slot.

![image](images/pgb98_1.jpg)

Comparison can be drawn to a long row of sequentially-numbered houses that can each accommodate a different family. Any family can be explicitly referenced by addressing their house number.

The slot (house) numbers in computer memory are expressed in hexadecimal format and can be revealed by the **&** reference operator.

![image](images/commong.jpg)

address.cpp

![image](images/1g.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>**

**#include <iostream>**

**using namespace std ;**

![image](images/2g.jpg)Add a main function containing a final **return** statement and declaring three initialized variables

**int main()**

**{**

**int num = 100 ;**

**double sum = 0.0123456789 ;**

**string text = “C++ Fun” ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3g.jpg)In the main function, insert statements to output the memory address of the first slot of each variable

**cout << “Integer variable starts at: “ << &num << endl ;**

**cout << “Double variable starts at: “ << &sum << endl ;**

**cout << “String variable starts at: “ << &text << endl ;**

![image](images/4g.jpg)Save, compile, and run the program to see the three memory addresses

![image](images/pgb99_1.jpg)

Once memory space has been reserved by a variable declaration, a value of the appropriate data type can be stored there using the **=** assignment operator. For example, **num = 100** takes the value on its right (**100**) and puts it in the memory referenced by the named variable on its left (**num**).

The operand to the left of the **=** assignment operator is called its “L-value” and the operand to its right is called its “R-value”. Consider the “L” in L-value to mean “Location” and consider the “R” in R-value to mean “Read”.

One important rule in C++ programming insists that an R-value cannot appear to the left of the **=** assignment operator, but an L-value may appear on either side. Code that places an R-value to the left of an **=** assignment operator will not compile:

![image](images/5g.jpg)Just before the **return** statement, insert statements placing R-values incorrectly to the left of assignment operators

**200 = num ;**

**5.5 = sum ;**

**“Bad assignments” = text ;**

![image](images/6g.jpg)Save, and attempt to recompile the program to see the errors caused by incorrectly placed R-values

![image](images/pgb99_2.jpg)

![image](images/forget.jpg)

The location addresses are dynamically allocated – so will vary from those in this screenshot.

![image](images/hot.jpg)

L-values are containers but R-values are data.

**Getting values with pointers**

Pointers are a useful part of efficient C++ programming – they are simply variables that store the memory address of other variables.

![image](images/pgb100_1.jpg)

Pointer variables are declared in the same way that other variables are declared, but the data type is suffixed by a “*****” character. This denotes, in a declaration, that the variable will be a pointer. Always remember that the pointer’s data type must match that of the variable to which it points.

A pointer variable is initialized by assigning it the memory address of another variable, using the **&** reference operator. The assignment can be made either in the declaration statement, or in a separate statement after the declaration. Referencing a pointer variable by its name alone will simply reveal the memory address that it contains.

After a pointer variable has been initialized, either in the declaration or by a subsequent assignment, it “points” to the variable at the address that it contains. Usefully, this means that the value of the variable to which it points can be referenced by prefixing the pointer name with the ***** dereference operator:

![image](images/commong.jpg)

deref.cpp

![image](images/1g.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2g.jpg)Add a main function containing a final **return** statement and declaring two regular initialized integer variables

**int main()**

**{**

**int a = 8 , b = 16 ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3g.jpg)In the main function, insert a statement to declare, and initialize a pointer with the memory address of the first integer variable

**int* aPtr = &a ;          // aPtr assigned address of a.**

![image](images/4g.jpg)Insert a statement to declare a second pointer, then initialize it with the address of the second integer variable

**int* bPtr ;              // bPtr declared.**

**bPtr = &b ;            // bPtr assigned address of b.**

![image](images/5g.jpg)Next, insert statements to output the actual memory address of each pointer

**cout << “Addresses of pointers...” << endl ;**

**cout << “aPtr: ” << &aPtr << endl ;**

**cout << “bPtr: ” << &bPtr << endl << endl ;**

![image](images/6g.jpg)Now, insert statements to output the memory address stored inside each pointer

**cout << “Values in pointers...” << endl ;**

**cout << “aPtr: ” << aPtr << endl ;**

**cout << “bPtr: ” << bPtr << endl << endl ;**

![image](images/7g.jpg)Finally, insert statements to output the values stored at the memory address stored in each pointer – the value of the variables to which the pointers point

**cout << “Values in addresses pointed to...” << endl ;**

**cout << “a: ” << *aPtr << endl ;**

**cout << “b: ” << *bPtr << endl ;**

![image](images/8g.jpg)Save, compile, and run the program to see the pointer addresses and the stored values

![image](images/pgb101_1.jpg)

![image](images/hot.jpg)

The ***** dereference operator is alternatively known as the “indirection” operator.

![image](images/forget.jpg)

The memory addresses are dynamically allocated – so will vary from those in this screenshot.

**Doing pointer arithmetic**

Once a pointer variable has been initialized with a memory address, it can be assigned another address or changed using pointer arithmetic.

![image](images/pgb102_1.jpg)

The **++** increment operator or the **--** decrement operator will move the pointer along to the next or previous address for that data type – the larger the data type, the bigger the jump.

Even larger jumps can be achieved using the **+=** and **-=** operators.

Pointer arithmetic is especially useful with arrays, because the elements in an array occupy consecutive memory addresses. Assigning just the name of an array to a pointer automatically assigns it the address of the first element. Incrementing the pointer by 1 moves the pointer along to the next element.

![image](images/commong.jpg)

point.cpp

![image](images/1g.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2g.jpg)Add a main function containing a final **return** statement and declaring an initialized integer array of 10 elements

**int main()**

**{**

**int nums[] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 } ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3g.jpg)In the main function, insert a statement to declare a pointer, initialized with the memory address of the first element in the integer array

**int* ptr = nums ;**

![image](images/4g.jpg)Next, insert a statement to output the memory address of the first element of the integer array, and its value

**cout << endl << “ptr at: ” << ptr << “ gets: ”<< *ptr ;**

![image](images/5g.jpg)Now, increment the pointer and output its new memory address – that of the second element in the integer array

**ptr++ ;**

**cout << endl << “ptr at: ” << ptr << “ gets: ”<< *ptr ;**

![image](images/6g.jpg)Increment the pointer again, and output its new memory address – that of the third element in the integer array

**ptr++ ;**

**cout << endl << “ptr at: ” << ptr << “ gets: ” << *ptr ;**

![image](images/7g.jpg)Decrement the pointer by two places and output its memory address – that of the first element in the array

**ptr -= 2 ;**

**cout << endl << “ptr at: ” << ptr << “ gets: ” << *ptr ;**

**cout << endl ;**

![image](images/8g.jpg)Now, insert a loop to output the value stored in each element of the integer array

**for ( int i = 0 ; i < 10 ; i++ )**

**{**

**cout << endl << “Element: “ << i ;**

**cout << “ Value: “ << *ptr ;**

**ptr++ ;**

**}**

**cout << endl ;**

![image](images/9g.jpg)Save, compile, and run the program to see the pointer addresses and the stored values

![image](images/pgb103_1.jpg)

![image](images/snake.jpg)

The ***=**, **/=**, and **%=** operators cannot be used to move a pointer.

![image](images/hot.jpg)

The name of an array acts like a pointer to its first element.

**Passing pointers to functions**

Pointers can access the data stored in the variable to which they point using the ***** dereference operator. This can also be used to change the stored data by assigning a new value of the appropriate data type.

![image](images/pgb104_1.jpg)

Additionally, pointers can be passed to functions as arguments – with a subtly different effect to passing variables as arguments:

•When variables are passed to functions, their data is passed “by value” to a local variable inside the function – so that the function operates on a copy of the original value.

•When pointers are passed to functions, their data is passed “by reference” – so that the function operates on the original value.

The benefit of passing by reference allows functions to directly manipulate variable values declared within the calling function.

![image](images/commong.jpg)

fnptr.cpp

![image](images/1g.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2g.jpg)After the preprocessor instructions, declare two function prototypes to each accept a single pointer argument

**void writeOutput ( int* ) ;**

**void computeTriple ( int* ) ;**

![image](images/3g.jpg)Add a main function containing a final **return** statement and declaring an initialized regular integer variable

**int main()**

**{**

**int num = 5 ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/4g.jpg)In the main function, insert a second variable declaration that initializes a pointer with the address of the regular integer variable

**int* ptr = &num ;**

![image](images/5g.jpg)After the main function block, define a function to output the current value of a variable to which a pointer points

**void writeOutput( int* value )**

**{**

**cout << “Current value: ” << *value << endl ;**

**}**

![image](images/6g.jpg)Define another function to multiply the current value of a variable to which a pointer points

**void computeTriple( int* value )**

**{**

***value *= 3 ;    // Multiply and assign dereferenced value.**

**}**

![image](images/7g.jpg)In the main function, pass a pointer argument to a function to output the variable value to which it points

**writeOutput( ptr ) ;**

![image](images/8g.jpg)Next, use the pointer to increase the variable value, then display its new value

***ptr += 15 ;      // Add and assign a dereferenced value.**

**writeOutput( ptr ) ;**

![image](images/9g.jpg)Now, pass a pointer argument to a function to multiply the variable to which it points, then display its new value

**computeTriple( ptr ) ;**

**writeOutput( ptr ) ;**

![image](images/10g.jpg)Save, compile, and run the program to see the computed values output

![image](images/pgb105_1.jpg)

![image](images/forget.jpg)

The function prototype and definition must both contain a pointer argument.

![image](images/hot.jpg)

Functions that operate directly on variables within the calling function need no **return** statement.

**Making arrays of pointers**

A variable of the regular **char** data type can be assigned a single character value, but a pointer to a constant **char** array can usefully be assigned a string of characters. The string is actually stored as an array of characters, with one character per element, but referencing the **char** pointer will automatically retrieve the entire string.

![image](images/pgb106_1.jpg)

This ability to retrieve a string value from a **char** pointer using just its variable name resembles the way that a string can be retrieved from a regular **char** array using its variable name.

Multiple strings can be stored in a constant **char** pointer array, with one string per element. You can even store multiple **char** pointer arrays in a “master” **char** pointer array – one array per element.

![image](images/commong.jpg)

arrptr.cpp

![image](images/1g.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2g.jpg)Add a main function containing a final **return** statement and declaring two initialized variables – a regular character array, and a character pointer with identical **string** values

**int main()**

**{**

**char letters[ 8 ] = { ‘C’, ‘+’ , ‘+’ , ‘ ‘ , ‘F’, ‘u’, ‘n’, ‘\0’ } ;**

**const char* text = “C++ Fun” ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/3g.jpg)In the main function, insert statements to declare, and initialize two further character pointer variables, with unique **string** values

**const char* term = “Element:” ;**

**const char* lang = “C++” ;**

![image](images/4g.jpg)Next, insert a statement to declare a character pointer array, initialized with three **string** values

**const char* ap1[ 3 ] = { “Great ” , “Program” , “Code ” } ;**

![image](images/forget.jpg)

Character values must be enclosed in single quotes, but **string** values must be enclosed in double quotes – even when they are being assigned to a **char** pointer.

![image](images/5g.jpg)Now, insert a statement to declare a second character pointer array, initialized with three string values – making one of the pointer variables its first element value

**const char* ap2[ 3 ] = { lang , “is ” , “Fun” } ;**

![image](images/6g.jpg)Declare two “master” character pointer arrays, each initialized with three elements of the **char** pointer arrays

**const char* ap3[ 3 ] = { ap2[ 0 ] , ap2[ 1 ] , ap1[ 0 ] } ;**

**const char* ap4[ 3 ] = { ap1[ 2 ] , ap2[ 1 ] , ap2[ 2 ] } ;**

![image](images/7g.jpg)After the declarations, insert statements to output the identical **string** values of the first two variables

**cout << letters << endl ;**

**cout << text << endl ;**

![image](images/8g.jpg)Next, insert a loop containing a statement to output the value within a character pointer and the iteration number

**for ( int i = 0 ; i < 3 ; i++ )**

**{**

**cout << term << i << “ “ ;**

**}**

![image](images/9g.jpg)Within the loop block, insert statements to output each element value of the four character pointer arrays

**cout << ap1[ i ] << “ ” ;**

**cout << ap2[ i ] << “ ” ;**

**cout << ap3[ i ] << “ ” ;**

**cout << ap4[ i ] << endl ;**

![image](images/10g.jpg)Save, compile, and run the program to see the character string output

![image](images/pgb107_1.jpg)

![image](images/forget.jpg)

To include a space in a **char** array, the assignment must have a space between the quotes as **‘ ‘** – two single quotes together ( **‘‘** ) is regarded as an empty element and causes a compiler error.

![image](images/snake.jpg)

Remember that the final element of a **char** array must contain the special **\0** character to designate that array as a string.

**Referencing data**

A C++ “reference” is an alias for a variable or an object in a program. A reference must be initialized within its declaration, by assigning it the name of the variable or object to which it refers. From then on, the reference acts as an alternative name for the item to which it refers – anything that happens to the reference is really implemented on the variable or object to which it refers.

![image](images/pgb108_1.jpg)

A reference declaration first states its data type, matching that of the item to which it will refer, suffixed by an **&** character denoting that variable will be a reference, and a chosen name. Finally, the declaration uses the **=** operator to associate a variable or object.

Traditionally, a reference is named with the name of the associated variable or object, but with an uppercase first letter and the whole name prefixed by an “r”. For example, a declaration to create a reference to an integer variable named “num” looks like this:

**int& rNum = num ;**

Note that the purpose of the **&** reference operator is context-sensitive so that it declares a reference when used as an L-value, on the left side of the **=** operator, otherwise it returns a memory address when used as an R-value.

A reference is such a true alias to its associated item that querying its memory address returns the address of its associated item – there is no way to discover the address of the reference itself.

![image](images/commong.jpg)

ref.cpp

![image](images/1g.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2g.jpg)Add a main function containing a final **return** statement and declaring two variables – a regular integer variable and a reference to that variable

**int main()**

**{**

**int num ;**

**int& rNum = num ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/snake.jpg)

Once a reference has been created, it will always refer to the item to which it was initialized – a different item cannot be assigned to that reference.

![image](images/3g.jpg)In the main function, insert a statement assigning an initial value to the integer variable via its reference

**rNum = 400 ;**

![image](images/4g.jpg)Next, insert statements to output the stored value, both directly and via its reference

**cout << “Value direct: ” << num << endl ;**

**cout << “Value via reference: ” << rNum << endl ;**

![image](images/5g.jpg)Now, insert statements to output the memory address, both directly and via its reference

**cout << “Address direct: ” << &num << endl ;**

**cout << “Address via reference: ” << &rNum << endl ;**

![image](images/6g.jpg)Insert a statement to manipulate the value stored in the variable via its reference

**rNum *= 2 ;**

![image](images/7g.jpg)Once more, output the stored value, both directly and via its reference

**cout << “Value direct: ” << num << endl ;**

**cout << “Value via reference: ” << rNum << endl ;**

![image](images/8g.jpg)Save, compile, and run the program to see the values and memory address

![image](images/pgb109_1.jpg)

![image](images/snake.jpg)

The compiler decides how to use the **&** reference operator according to its context.

![image](images/forget.jpg)

A reference is always an alias for the item associated in its declaration statement.

**Passing references to functions**

References provide access to the data stored in the variable to which they refer, just like the variable itself, and can be used to change the stored data by assigning a new value of the appropriate data type.

![image](images/pgb110_1.jpg)

Additionally, references can, like pointers, be passed to functions as arguments:

•When variables are passed to functions, their data is passed “by value” to a local variable inside the function – so that the function operates on a copy of the original value.

•When references are passed to functions, their data is passed “by reference” – so the function operates on the original value.

The benefit of passing by reference allows functions to directly manipulate variable values declared within the calling function.

![image](images/commong.jpg)

fnref.cpp

![image](images/1g.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2g.jpg)After the preprocessor instructions, declare two function prototypes to each accept a single reference argument

**void writeOutput ( int& ) ;**

**void computeTriple ( int& ) ;**

![image](images/3g.jpg)Add a main function containing a final **return** statement and declaring an initialized regular integer variable

**int main()**

**{**

**int num = 5 ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/4g.jpg)In the main function, insert a second variable declaration, initializing a reference as an alias of the integer variable

**int& ref = num ;**

![image](images/forget.jpg)

This example may seem familiar, as it recreates the example [here](#chapter17.xhtml_sec139) – but replaces pointers with references.

![image](images/5g.jpg)After the main function block, define a function to output the current value of a variable to which a reference refers

**void writeOutput( int& value )**

**{**

**cout << “Current value: ” << value << endl ;**

**}**

![image](images/6g.jpg)Define another function to multiply the current value of a variable to which a reference refers

**void computeTriple( int& value )**

**{**

**value *= 3 ;      // Multiply and assign a referenced value.**

**}**

![image](images/7g.jpg)In the main function, pass a reference argument to a function to output the variable value to which it refers

**writeOutput( ref ) ;**

![image](images/8g.jpg)Next, use the reference to increase the variable value, then display its new value

**ref += 15 ;      // Add and assign a referenced value.**

**writeOutput( ref ) ;**

![image](images/9g.jpg)Now, pass a reference argument to a function to multiply the variable to which it refers, then display its new value

**computeTriple( ref ) ;**

**writeOutput( ref ) ;**

![image](images/10g.jpg)Save, compile, and run the program to see the computed values output

![image](images/pgb111_1.jpg)

![image](images/forget.jpg)

The function prototype and definition must both contain a reference argument.

![image](images/hot.jpg)

Functions that operate directly on variables within the calling function need no **return** statement.

**Comparing pointers & references**

Pointers and references can both be used to refer to variable values and to pass them to functions by reference rather than by value. Technically, passing by reference is more efficient than passing by value, so the use of pointers and references is to be encouraged.

![image](images/pgb112_1.jpg)

The decision whether to use a pointer or a reference is determined by the program requirements. C++ programmers generally prefer to use references wherever possible, as they are easier to use and easier to understand than pointers. References must, however, obey certain rules that can make the use of pointers necessary:

| **Rule** | **References** | **Pointers** |
| Can be declared without initialization | No | Yes |
| Can be reassigned  | No | Yes |
| Can contain a 0 (null) value  | No  | Yes  |
| Easiest to use | Yes | No |

As a general rule, the choice between using a reference or a pointer can be determined by following these guidelines:

•If you don’t want to initialize in the declaration, use a pointer;

**or**

•If you want to be able to reassign another variable, use a pointer;

**otherwise**

•Always use a reference.

Pointers are more flexible than references, however, and can even point to functions. In this case, the pointer declaration must precisely match the return data type and arguments to those of the function to which it points. Additionally, the pointer name must be enclosed within parentheses in the declaration to avoid compiler errors. The function pointer can then be assigned a function by name, so that function can be called via the pointer.

![image](images/forget.jpg)

A reference must be initialized in the declaration to refer to a variable or object – then always refers to that item.

![image](images/commong.jpg)

pref.cpp

![image](images/1g.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2g.jpg)After the preprocessor instructions, define an inline function to output the total of two passed arguments

**inline void add ( int& a, int* b )**

**{ cout << “Total: ” << ( a + *b ) << endl ; }**

![image](images/3g.jpg)Add a main function containing a final **return** statement and declarations creating two regular integer variables, one reference, and two pointers

**int main()**

**{**

**int num = 100 , sum = 500 ;**

**int& rNum = num ;**

**int* ptr = &num ;**

**void (* fn ) ( int& a, int* b ) = add ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/4g.jpg)In the main function, insert statements to output the first integer variable values via the reference and pointer

**cout << “Reference: ” << rNum << endl ;**

**cout << “Pointer: ” << *ptr << endl ;**

![image](images/5g.jpg)Now, assign the second integer variable to the pointer and output its value via the pointer, then call the function pointer to output the sum of the variable values

**ptr = &sum ;**

**cout << “Pointer now: ” << *ptr << endl ;**

**fn( rNum , ptr ) ;**

![image](images/6g.jpg)Save, compile, and run the program to see the output

![image](images/pgb113_1.jpg)

![image](images/hot.jpg)

C programmers tend to put the **&** and ***** characters before the variable names, but in C++ it is usual to put them after the data type – as the feature is a property of the data type, not the name.

**Summary**

![image](images/pgb186_1.jpg)

•Data is stored in computer memory within sequentially numbered addresses.

•Operands to the left of an **=** operator are L-values, and those to its right are R-values.

•An R-value may only appear to the right of an **=** operator.

•A pointer is a variable that stores the memory address of another variable – that to which it points.

•The ***** character appears as an L-value in a pointer declaration, indicating that the statement will create a pointer variable.

•Once declared, the ***** dereference operator can be used to reference the value within a variable to which a pointer points.

•Pointer arithmetic can be used to iterate through the values stored in array elements.

•A variable is passed to a function by value, whereas pointers and references are passed by reference.

•Passing by reference allows the receiving function to directly manipulate variables declared within the calling function.

•A string value can be assigned to a pointer of the **char** data type, and the whole string retrieved using the pointer name.

•Each element in a pointer array can store data or a pointer.

•A reference is not a variable, but merely an alias for a variable.

•The **&** character appears as an L-value in a reference declaration, indicating that the statement will create an alias.

•The **&** reference operator can be used to reference the memory address stored within a pointer.

•References are easier to use than pointers but, unlike pointers, a reference must always be initialized in its declaration and can never be assigned a different variable.

18

**Creating classes and objects**

***This chapter introduces the topics of encapsulation and inheritance – the first two principles of C++ Object Oriented Programming.***

[Encapsulating data](#chapter18.xhtml_sec145)

[Creating an object](#chapter18.xhtml_sec146)

[Creating multiple objects](#chapter18.xhtml_sec147)

[Initializing class members](#chapter18.xhtml_sec148)

[Overloading methods](#chapter18.xhtml_sec149)

[Inheriting class properties](#chapter18.xhtml_sec150)

[Calling base constructors](#chapter18.xhtml_sec151)

[Overriding base methods](#chapter18.xhtml_sec152)

[Summary](#chapter18.xhtml_sec153)

**Encapsulating data**

A class is a data structure that can contain both variables and functions in a single entity. These are collectively known as its “members”, and the functions are known as its “methods”.

![image](images/pgb116_1.jpg)

Access to class members from outside the class is controlled by “access specifiers” in the class declaration. Typically, these will deny access to the variable members, but allow access to methods that can store and retrieve data from those variable members. This technique of “data hiding” ensures that stored data is safely encapsulated within the class variable members, and is the first principle of Object Oriented Programming (OOP).

A class declaration begins with the **class** keyword, followed by a space, then a programmer-specified name – adhering to the usual C++ naming conventions, but beginning in uppercase. Next, come the access specifiers and class members, contained within a pair of braces. Every class declaration must end with a semicolon after the closing brace – so the class declaration syntax looks like this:

***class ClassName***

**{**

***access specifier* :**

***member1* ;**

***member2* ;**

***access specifier* :**

***member3* ;**

***member4* ;**

**} ;**

An access specifier may be any one of the keywords **public**, **private**, or **protected** to specify access rights for its listed members:

•Public members are accessible from any place where the class is visible.

•Private members are accessible only to other members of the same class.

•Protected members are accessible only to other members of the same class and to members of classes derived from that class.

By default, all class members have private access – so any members that appear in the class declaration without an access specifier will have private access.

![image](images/forget.jpg)

Derived classes, which use the **protected** access specifier, are introduced later in this chapter.

Any real-world object can be defined by its attributes and by its actions. For example, a dog has attributes such as age, weight, and color, and actions it can perform such as bark. The class mechanism in C++ provides a way to create a virtual dog object within a program, where the variable members of a class can represent its attributes, and the methods represent its actions:

**class Dog**

**{**

**private: // The default access level.**

**int age, weight ;**

**string color ;**

**public :**

**void bark() ;**

**// ... Plus methods to store/retrieve data.**

**} ;**

![image](images/forget.jpg)

While a program class cannot perfectly emulate a real-word object, the aim is to encapsulate all relevant attributes and actions.

It is important to recognize that a class declaration only defines a data structure – in order to create an object you must declare an “instance” of that data structure. This is achieved in just the same way that instances are declared of regular C++ data types:

| **int num ;** | **// Creates an instance named “num”.****// of the regular C++ int data type.** |
| **Dog fido ;** | **// Creates an instance named “fido”.****// of the programmer-defined Dog data structure.** |

Alternatively, an instance object can be created by specifying its name between the class declaration’s closing brace and its final semicolon. Multiple instances can be created this way, by specifying a comma-separated list of object names. For example, the class declaration listed below creates four instance objects of the Dog class named “fido”, “pooch”, “rex”, and “sammy”.

**class Dog**

**{**

**int age, weight ;**

**string color ;**

**public:**

**void bark() ;**

**// ... Plus methods to store/retrieve data.**

**} fido, pooch, rex, sammy ;**

The principle of encapsulation in C++ programming describes the grouping together of data and functionality in class members – age, weight, color attributes and bark action in the Dog class.

![image](images/hot.jpg)

It is conventional to begin class names with an uppercase character and object names with lowercase.

**Creating an object**

In order to assign and retrieve data from private members of a class, special public accessor methods must be added to the class. These are “setter” methods, to assign data, and “getter” methods, to retrieve data. Accessor methods are often named as the variable they address, with the first letter made uppercase, and prefixed by “set” or “get” respectively. For example, accessor methods to address an **age** variable may be named **setAge()** and **getAge()**.

![image](images/pgb118_1.jpg)

![image](images/commonp.jpg)

object.cpp

![image](images/1p.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>**

**#include <iostream>**

**using namespace std ;**

![image](images/2p.jpg)Declare a class named “Dog”

**class Dog**

**{**

**} ;**

![image](images/3p.jpg)Between the braces of the Dog class declaration, declare three **private** variable members

**int age, weight ;**

**string color ;**

![image](images/4p.jpg)After the **private** variables, add a **public** access specifier

**public:**

![image](images/5p.jpg)Begin the **public** members list by adding a method to output a **string** when called

**void bark() { cout << “WOOF!” << endl ; }**

![image](images/6p.jpg)Add **public** setter methods – to assign individual values to each of the **private** variables

**void setAge ( int yrs ) { age = yrs ; }**

**void setWeight ( int lbs ) { weight = lbs ; }**

**void setColor ( string hue ) { color = hue ; }**

![image](images/7p.jpg)Add **public** getter methods – to retrieve individual values from each of the **private** variables

**int getAge()      { return age ; }**

**int getWeight() { return weight ; }**

**string getColor() { return color ; }**

![image](images/forget.jpg)

Members declared before an access specifier are **private** by default, and remember to add a final semicolon after each class declaration.

![image](images/hot.jpg)

In the class declaration, notice that all methods are declared **public** and all variables are declared **private**. This notion of “public interface, private data” is a key concept when creating classes.

![image](images/8p.jpg)After the Dog class declaration, declare a main method containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/9p.jpg)Between the braces of the main method, declare an instance of the Dog class named “fido”

**Dog fido ;**

![image](images/pgb119_1.jpg)

![image](images/10p.jpg)Add statements calling each setter method to assign data

**fido.setAge( 3 ) ;**

**fido.setWeight( 15 ) ;**

**fido.setColor( “brown” ) ;**

![image](images/11p.jpg)Add statements calling each getter method to retrieve the assigned values

**cout << “Fido is a “ << fido.getColor() <<**

**“ dog” << endl ;**

**cout << “Fido is “ << fido.getAge() <<**

**“ years old” << endl ;**

**cout << “Fido weighs “ << fido.getWeight() <<**

**“ pounds” << endl ;**

![image](images/12p.jpg)Now, add a call to the regular output method

**fido.bark() ;**

![image](images/13p.jpg)Save, compile, and run the program to see the output

![image](images/pgb119_2.jpg)

![image](images/hot.jpg)

This program will get modified over the next few pages as new features are incorporated.

**Creating multiple objects**

A program can easily create multiple objects, simply by declaring multiple instances of a class, and each object can have unique attributes by assigning individual values with its setter methods.

![image](images/pgb120_1.jpg)

It is often convenient to combine the setter methods into a single method that accepts arguments for each private variable. This means that all values can be assigned with a single statement in the program, but the method will contain multiple statements.

The class declaration in the previous example contains short methods of just one line, which are created “inline” – entirely within the class declaration block. Where methods have more than two lines, they should not be created inline, but should instead be declared as a “prototype” in the class declaration block and defined separately – after the class declaration. The definition must prefix the method name with the class name and the scope resolution operator :: to identify the class containing its prototype.

![image](images/commonp.jpg)

multiple.cpp

![image](images/1p.jpg)Rename a copy of the previous example “object.cpp” as a new program “multiple.cpp”

![image](images/2p.jpg)In the Dog class declaration, replace the three setter methods with a single combined setter prototype that specifies the argument data types – but not their names

**void setValues ( int, int, string ) ;**

![image](images/3p.jpg)After the Dog class declaration, add a definition block for the prototype using the :: scope resolution operator to identify the class in which it resides

**void Dog::setValues ( int age, int weight, string color )**

**{**

**}**

Notice that, for easy identification, the arguments are named with the same names as the variables to which they will be assigned. Where a class method definition has an argument of the same name as a class member, the **this ->** class pointer can be used to explicitly refer to the class member. For example, **this -> age** refers to the class member variable, whereas **age** refers to the argument.

![image](images/forget.jpg)

Note that a prototype is a statement – so it must end with a semicolon.

![image](images/4p.jpg)In the method definition block, insert three statements to assign values from passed arguments to class variables

**this -> age = age ;**

**this -> weight = weight ;**

**this -> color = color ;**

![image](images/5p.jpg)Between the braces of the main method, replace the calls to the three setter methods by a single call to the combined setter method – passing three arguments

**fido.setValues( 3, 15, “brown” ) ;**

![image](images/6p.jpg)In the main method, declare a second instance of the Dog class named “pooch”

**Dog pooch ;**

![image](images/7p.jpg)Add a second call to the combined setter method – passing three arguments for the new object

**pooch.setValues( 4, 18, “gray” ) ;**

![image](images/8p.jpg)Add statements calling each getter method to retrieve the assigned values

**cout << “Pooch is a “ << pooch.getAge() ;**

**cout << “ year old “ << pooch.getColor() ;**

**cout << “ dog who weighs “ << pooch.getWeight() ;**

**cout << “ pounds .” ;**

![image](images/9p.jpg)Now, add second call to the regular output method

**pooch.bark() ;**

![image](images/10p.jpg)Save, compile, and run the program to see the output

![image](images/pgb121_2.jpg)

![image](images/pgb121_1.jpg)

![image](images/forget.jpg)

Where the argument name and class member names are different, the **this ->** class pointer is not needed in the setter method definitions.

**Initializing class members**

Class variable members can be initialized by a special “constructor” method that is called whenever an instance of the class is created. The constructor method is always named exactly as the class name, and requires arguments to set the initial value of class variables.

![image](images/pgb122_1.jpg)

When a constructor method is declared, an associated “destructor” method should also be declared – that is called whenever an instance of the class is destroyed. The destructor method is always named as the class name, prefixed by a **~** tilde character.

Constructor and destructor methods have no return value, and are called automatically – they cannot be called explicitly.

Values to initialize class variables are passed to the constructor method in the statement creating an object, in parentheses following the object name.

![image](images/commonp.jpg)

constructor.cpp

![image](images/1p.jpg)Rename a copy of the previous example “multiple.cpp” as a new program “constructor.cpp”

![image](images/2p.jpg)In the public section of the Dog class declaration, replace the setValues method prototype with this constructor prototype

**Dog ( int, int, string ) ;**

![image](images/3p.jpg)Now, add an associated destructor prototype

**~Dog() ;**

![image](images/4p.jpg)After the Dog class declaration, replace the setValues definition block with a constructor definition block

**Dog::Dog ( int age, int weight, string color )**

**{**

**}**

![image](images/5p.jpg)In the constructor definition block, insert three statements to assign values from passed arguments to class variables

**this -> age = age ;**

**this -> weight = weight ;**

**this -> color = color ;**

![image](images/hot.jpg)

The definition of a class method is also known as the method “implementation”.

![image](images/6p.jpg)After the constructor definition, add a destructor definition block

**Dog::~Dog()**

**{**

**}**

![image](images/7p.jpg)In the destructor definition, insert a statement to output a confirmation whenever an instance object gets destroyed

**cout << “Object destroyed.” << endl ;**

![image](images/8p.jpg)In the main method, edit the statement creating the “fido” object – to pass values to its constructor method

**Dog fido( 3, 15, “brown” ) ;**

![image](images/9p.jpg)Similarly, edit the statement creating the “pooch” object – to pass values to the constructor method

**Dog pooch( 4, 18, “gray” ) ;**

![image](images/10p.jpg)Delete the statements calling the setValues method of the “fido” and “pooch” objects – the constructor has now replaced that method

![image](images/11p.jpg)Save, compile, and run the program – see the output appear as before, plus confirmation when the objects get destroyed

![image](images/pgb123_1.jpg)

![image](images/snake.jpg)

The destructor definition begins with the class name “Dog”, the scope resolution operator “::”, then the destructor method name “~Dog”.

![image](images/forget.jpg)

Although the initial values of the variable members are set by the constructor, setter methods can be added to subsequently change the values – and those new values can be retrieved by the getter methods.

**Overloading methods**

Just as C++ allows functions to be overloaded, class methods can be overloaded too – including constructor methods. An overloaded constructor method is useful to assign default values to member variables when an object is created without passing values to the constructor.

![image](images/pgb124_1.jpg)

![image](images/commonp.jpg)

overloaded.cpp

![image](images/1p.jpg)Rename a copy of the previous example “constructor.cpp” as a new program “overloaded.cpp”

![image](images/2p.jpg)In the public section of the Dog class declaration, add inline an overloaded bark method – to output a passed string argument when called

**void bark ( string noise ) { cout << noise << endl ; }**

![image](images/3p.jpg)Now, declare a constructor method prototype that takes no arguments (a default constructor method) and an overloaded constructor method prototype that takes two arguments

**Dog() ;**

**Dog ( int, int ) ;**

![image](images/4p.jpg)After the Dog class declaration, add a definition for the default constructor method – assigning default values to class variables when an object is created without passing any arguments

**Dog::Dog()**

**{**

**age = 1 ;**

**weight = 2 ;**

**color = “black” ;**

**}**

![image](images/5p.jpg)Now, add a definition for the overloaded constructor method – assigning default values to class variables when an object is created passing two arguments

**Dog::Dog ( int age, int weight )**

**{**

**this -> age = age ;**

**this -> weight = weight ;**

**color = “white” ;**

**}**

![image](images/forget.jpg)

The **this ->** pointer is used to explicitly identify class members when arguments have the same name as members.

![image](images/6p.jpg)In the main method, insert a statement to create a Dog object without passing any arguments – calling the default constructor

**Dog rex ;**

![image](images/7p.jpg)Add statements calling each getter method to retrieve the default values – set by the default constructor method

**cout << “Rex is a “ << rex.getAge() ;**

**cout << “ year old “ << rex.getColor() ;**

**cout << “ dog who weighs “ << rex.getWeight() ;**

**cout << “ pounds .” ;**

![image](images/8p.jpg)Now, add a call to the overloaded output method

**rex.bark( “GRRR!” ) ;**

![image](images/9p.jpg)Insert a statement to create a Dog object passing two arguments – to call the overloaded constructor

**Dog sammy( 2, 6 ) ;**

![image](images/10p.jpg)Add statements to retrieve the values set by the overloaded constructor method and call the overloaded output method

**cout << “Sammy is a “ << sammy.getAge() ;**

**cout << “ year old “ << sammy.getColor() ;**

**cout << “ dog who weighs “ << sammy.getWeight() ;**

**cout << “ pounds .” ;**

**sammy.bark( “BOWOW!” ) ;**

![image](images/11p.jpg)Save, compile, and run the program

![image](images/pgb125_1.jpg)

![image](images/snake.jpg)

Don’t add parentheses after the object name when creating an object without passing arguments – notice it’s **Dog rex ;** not **Dog rex() ;**

![image](images/hot.jpg)

This is the final rendition of the Dog class. Be sure you can readily identify its public and private members before proceeding.

**Inheriting class properties**

A C++ class can be created as a brand new class, like those in previous examples, or can be “derived” from an existing class. Importantly, a derived class inherits members of the parent (base) class from which it is derived – in addition to its own members.

![image](images/pgb126_1.jpg)

The ability to inherit members from a base class allows derived classes to be created that share certain common properties, which have been defined in the base class. For example, a “Polygon” base class may define width and height properties that are common to all polygons. Classes of “Rectangle” and Triangle” could be derived from the Polygon class – inheriting width and height properties, in addition to their own members defining their unique features.

![image](images/pgb126_2.jpg)

The virtue of inheritance is extremely powerful and is the second principle of Object Oriented Programming (OOP).

A derived class declaration adds a colon : after its class name, followed by an access specifier and the class from which it derives.

![image](images/commonp.jpg)

derived.cpp

![image](images/1p.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2p.jpg)Declare a class named “Polygon” containing two protected variables, accessible only to members of this class and classes derived from this class, along with a public method to assign values to those variables

**class Polygon**

**{**

**protected:**

**int width, height ;**

**public:**

**void setValues( int w, int h ) { width = w; height = h ; }**

**} ;**

![image](images/3p.jpg)After the Polygon class, declare a Rectangle class that derives from the Polygon class and adds a unique method

**class Rectangle : public Polygon**

**{**

**public:**

**int area() { return ( width * height ) ; }**

**} ;**

![image](images/4p.jpg)After the Rectangle class, declare a Triangle class that derives from the Polygon class and adds a unique method

**class Triangle : public Polygon**

**{**

**public:**

**int area() { return ( ( width * height ) / 2 ) ; }**

**} ;**

![image](images/5p.jpg)After the Triangle class, add a main method containing a final **return** statement and creating an instance of each derived class

**int main()**

**{**

**Rectangle rect ; Triangle trgl ;**

**return 0 ;**

**}**

![image](images/6p.jpg)Insert calls to the method inherited from the Polygon base class – to initialize the inherited variables

**rect.setValues( 4, 5 ) ;**

**trgl.setValues( 4, 5 ) ;**

![image](images/7p.jpg)Output the value returned by the unique method of each derived class

**cout << “Rectangle area : “ << rect.area() << endl ;**

**cout << “Triangle area : “ << trgl.area() << endl ;**

![image](images/8p.jpg)Save, compile, and run the program to see the output

![image](images/pgb127_1.jpg)

![image](images/snake.jpg)

Don’t confuse class instances and derived classes – an instance is a copy of a class, whereas a derived class is a new class that inherits properties of the base class from which it is derived.

![image](images/hot.jpg)

A class declaration can derive from more than one class – for example, **class Box : public A, public B, public C { } ;**

**Calling base constructors**

Although derived classes inherit the members of their parent base class, they do not inherit its constructor and destructor. However, it should be noted that the default constructor of the base class is always called when a new object of a derived class is created – and the base class destructor is called when the object gets destroyed. These calls are made in addition to those made to the constructor and destructor methods of the derived class.

![image](images/pgb128_1.jpg)

The default constructor of the base class has no arguments – but that class may also have overloaded constructors that do. If you prefer to call an overloaded constructor of the base class when a new object of a derived class is created, you can create a matching overloaded constructor in the derived class – having the same number and type of arguments.

![image](images/commonp.jpg)

basecon.cpp

![image](images/1p.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2p.jpg)Declare a class named “Parent”, which will be a base class

**class Parent**

**{**

**// Class members go here.**

**} ;**

![image](images/3p.jpg)Between the braces of the Parent class declaration, insert a public access specifier and add a default constructor to output text – identifying when it has been called

**public:**

**Parent()**

**{ cout << “Default Parent constructor called.” ; }**

![image](images/4p.jpg)Add an overloaded constructor, which takes a single integer argument and also outputs identifying text

**Parent ( int a )**

**{ cout << endl <<**

**“Overloaded Parent constructor called.” ; }**

![image](images/5p.jpg)After the Parent class, declare a derived “Daughter” class

**class Daughter : public Parent**

**{**

**} ;**

![image](images/pgb128_2.jpg)

Son – Parent – Daughter

![image](images/6p.jpg)In the Daughter class declaration, insert a public access specifier and add a default constructor to output text – identifying when it has been called

**public :**

**Daughter ()**

**{ cout << endl <<**

**“     Derived Daughter class default constructor called.” ; }**

![image](images/7p.jpg)After the Daughter class, declare a derived “Son” class

**class Son : public Parent**

**{**

**} ;**

![image](images/8p.jpg)In the Son class declaration, insert a public access specifier and add an overloaded constructor that takes a single integer argument, and also outputs identifying text

**public :**

**Son ( int a ) : Parent ( a )**

**{ cout << endl <<**

**“       Derived Son class overloaded constructor called.” ; }**

![image](images/9p.jpg)After the Son class, add a main method containing a final **return** statement and creating an instance of each derived class – calling base class and derived class constructors

**int main()**

**{**

**Daughter emma ;**

**Son andrew(0) ;**

**return 0 ;**

**}**

![image](images/10p.jpg)Save, compile, and run the program to see the output from each constructor in turn as it gets called

![image](images/pgb129_1.jpg)

![image](images/snake.jpg)

Notice that the syntax in the overloaded Son class constructor passes the integer argument to the overloaded base class constructor.

![image](images/forget.jpg)

Each class automatically has an empty default constructor and destructor – for example, **Son( ){ }** and **~Son( ){ }**

**Overriding base methods**

A method can be declared in a derived class to override a matching method in the base class – if both method declarations have the same name, arguments, and return type. This effectively hides the base class method as it becomes inaccessible unless it is called explicitly, using the :: scope resolution operator for precise identification.

![image](images/pgb130_1.jpg)

The technique of overriding base class methods must be used with care, however, to avoid unintentionally hiding overloaded methods – a single overriding method in a derived class will hide all overloaded methods of that name in the base class!

![image](images/commonp.jpg)

override.cpp

![image](images/1p.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <string>**

**#include <iostream>**

**using namespace std ;**

![image](images/2p.jpg)Declare a class named “Man”, which will be a base class

**class Man**

**{**

**// Class members go here.**

**} ;**

![image](images/3p.jpg)Between the braces of the Man class declaration, insert a public access specifier and an inline output method

**public :**

**void speak() { cout << “Hello! ” << endl ; }**

![image](images/4p.jpg)Now, insert an overloaded inline output method

**void speak( string msg )**

**{ cout << “ ” << msg << endl ; }**

![image](images/5p.jpg)After the Man class declaration, declare a class named “Hombre” that is derived from the Man class

**class Hombre : public Man**

**{**

**// Class members go here.**

**} ;**

![image](images/forget.jpg)

The method declaration in the derived class must exactly match that in the base class to override it – including the **const** keyword if it is used.

![image](images/6p.jpg)Between the braces of the Hombre class declaration, insert an access specifier and a method that overrides the overloaded base class method – without a tab output

**public :**

**void speak( string msg ) { cout << msg << endl ; }**

![image](images/7p.jpg)After the Hombre class declaration, add a main method containing a final **return** statement and creating two objects – an instance of the base class and an instance of the derived class

**int main()**

**{**

**Man henry ;**

**Hombre enrique ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/pgb131_1.jpg)

![image](images/8p.jpg)In the main method, insert statements calling both methods of the base class

**henry.speak() ;**

**henry.speak( “It’s a beautiful evening.” ) ;**

![image](images/9p.jpg)Next, insert a statement calling the overriding method in the derived class – producing output without a tab

**enrique.speak( “Hola!” ) ;**

![image](images/10p.jpg)Now, insert a statement explicitly calling the overridden method in the base class

**enrique.Man::speak( “Es una tarde hermosa.” ) ;**

![image](images/11p.jpg)Save, compile, and run the program to see the output from the overriding and overridden methods

![image](images/pgb131_2.jpg)

![image](images/snake.jpg)

The overriding method declared in the derived class hides both overloaded classes in the base class. Try calling **enrique.speak()** – the compiler will complain there is no matching method for that call.

**Summary**

![image](images/pgc58_1.jpg)

•The first principle of Object Oriented Programming is the encapsulation of data and functionality within a single class.

•Access specifiers **public**, **private**, and **protected** control the accessibility of class members from outside the class.

•A class declaration describes a data structure from which instance objects can be created.

•Public setter and getter class methods store and retrieve data from private class variable members.

•The scope resolution operator **::** can explicitly identify a class.

•Class members that have the same name as a passed argument can be explicitly identified by the **this ->** pointer.

•A constructor method is called when an object gets created, and a destructor method is called when it gets destroyed.

•Class variables can be automatically initialized by a constructor.

•Class methods can be overloaded like other functions.

•The second principle of Object Oriented Programming is the virtue of inheritance that allows derived classes to inherit the properties of their parent base class.

•In a derived class declaration, the class name is followed by a : colon character, an access specifier, and its base class name.

•When an instance object of a derived class is created, the default constructor of the base class gets called in addition to the constructor of the derived class.

•A derived class method can override a matching method in its base class – also overriding all overloaded methods of that name within the base class.

19

**Harnessing polymorphism**

***This chapter demonstrates how to separate programs into modular components and introduces the topic of polymorphism – the third principle of C++ Object Oriented Programming.***

[Pointing to classes](#chapter19.xhtml_sec154)

[Calling a virtual method](#chapter19.xhtml_sec155)

[Directing method calls](#chapter19.xhtml_sec156)

[Providing capability classes](#chapter19.xhtml_sec157)

[Making abstract data types](#chapter19.xhtml_sec158)

[Building complex hierarchies](#chapter19.xhtml_sec159)

[Isolating class structures](#chapter19.xhtml_sec160)

[Employing isolated classes](#chapter19.xhtml_sec161)

[Summary](#chapter19.xhtml_sec162)

**Pointing to classes**

The three cornerstones of Object Oriented Programming (OOP) are encapsulation, inheritance, and polymorphism. Examples in [Chapter 18](#chapter18.xhtml) have demonstrated how data can be encapsulated within a C++ class, and how derived classes inherit the properties of their base class. This chapter introduces the final cornerstone principle of polymorphism.

![image](images/pgb134_1.jpg)

The term “polymorphism” (from Greek, meaning “many forms”) describes the ability to assign a different meaning, or purpose, to an entity according to its context.

In C++, overloaded operators can be described as polymorphic. For example, the * character can represent either the multiply operator or the dereference operator, according to its context. Similarly, the + character can represent either the add operator or the concatenate operator, according to its context.

More importantly, C++ class methods can also be polymorphic. The key to understanding polymorphism with classes is to recognize that a base class pointer can be created that is also bound to a particular derived class by association.

A pointer to a base class can be assigned the memory address of a derived class to provide a “context” – to uniquely identify that derived class. For example, with a **Base** base class and a derived **Sub** class, a pointer can be created like this:

**Sub inst ;**

**Base* pSub = &inst ;**

or more simply using the **new** keyword, like this:

**Base* pSub = new Sub ;**

![image](images/forget.jpg)

Turn back to [Chapter 17](#chapter17.xhtml) for more on pointers.

Where there are multiple derived classes, base class pointers can be created binding each derived class by its unique memory address – which can be revealed using the addressof **&** operator.

![image](images/commono.jpg)

classptr.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Declare a **Base** class containing a method to output a passed integer value in hexadecimal format

**class Base**

**{**

**public:**

**void Identify( int adr ) const**

**{**

**cout << “Base class called by 0x”** **<< hex << adr << endl ; }**

**} ;**

![image](images/3o.jpg)Declare two empty derived classes, **SubA** and **SubB**

**class SubA : public Base {        } ;**

**class SubB : public Base {        } ;**

![image](images/4o.jpg)Declare a main method containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/5o.jpg)In the main method, insert statements to create two base class pointers – each binding to a specific derived class

**Base* ptrA = new SubA ;**

**Base* ptrB = new SubB ;**

![image](images/6o.jpg)Now, insert statements that use the pointers to call the base class method, passing the memory address of each for output

**ptrA -> Identify( (int) &ptrA ) ;**

**ptrB -> Identify( (int) &ptrB ) ;**

![image](images/7o.jpg)Save, compile, and run the program to see the addresses

![image](images/pgb135_1.jpg)

![image](images/forget.jpg)

The **->** class pointer operator is used here to call class methods.

![image](images/hot.jpg)

The hexadecimal address is passed as an **int** data type, then displayed in hexadecimal format by the **hex** output manipulator. The addresses will be different each time the program executes – they are assigned dynamically.

**Calling a virtual method**

A base class pointer that is bound to a specific derived class can be used to call derived class methods that have been inherited from the base class. Methods that are unique to the derived class must, however, be called via an instance object.

![image](images/pgb136_1.jpg)

A base class pointer that is bound to a specific derived class can also be used to explicitly call a method in the base class using the :: scope resolution operator.

Most usefully, an inherited method in a derived class can override that in the base class when the base method has been declared as a “virtual” method. This is just a regular method declaration in the base class preceded by the **virtual** keyword. The declaration of a virtual method indicates that the class will be used as a base class from which another class will be derived, which may contain a method to override the virtual base method.

![image](images/commono.jpg)

virtual.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Declare a base class named “Parent”, containing a regular method declaration and a virtual method declaration

**class Parent**

**{**

**public :**

**void Common() const**

**{ cout << “I am part of this family, “ ; }**

**virtual void Identify() const**

**{ cout << “I am the parent” << endl ; }**

**} ;**

![image](images/3o.jpg)Declare a derived class named “Child”, containing a method to override the virtual base method

**class Child : public Parent**

**{**

**public :**

**void Identify() const**

**{ cout << “I am the child” << endl ; }**

**} ;**

![image](images/snake.jpg)

Pointers to a base class cannot be used to call non-inherited methods in a derived class.

![image](images/4o.jpg)Declare a “Grandchild” class, derived from the “Child” class, containing a method to override the virtual base method and a regular method declaration

**class Grandchild : public Child**

**{**

**public :**

**void Identify() const**

**{ cout << “I am the grandchild” << endl ; }**

**void Relate() const**

**{ cout << “Grandchild has parent and grandparent” ; }**

**} ;**

![image](images/pgb137_1.jpg)

![image](images/5o.jpg)Declare a main method containing a final **return** statement and creating instances of each derived class, plus base class pointers binding those derived classes

**int main()**

**{**

**Child son ;**

**Grandchild grandson ;**

**Parent* ptrChild = &son ;**

**Parent* ptrGrandchild = &grandson ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/6o.jpg)In the main method, insert calls to each method

**ptrChild -> Common() ;                  // Inherited.**

**ptrChild -> Identify() ;                    // Overriding.**

**ptrGrandchild -> Common() ;       // Inherited.**

**ptrGrandchild -> Identify() ;         // Overriding.**

**ptrChild -> Parent::Common() ;   // Explicit.**

**ptrChild -> Parent::Identify() ;     // Explicit.**

**grandson.Relate() ;                     // Via instance.**

![image](images/7o.jpg)Save, compile, and run the program to see the output

![image](images/pgb137_2.jpg)

![image](images/forget.jpg)

Here, the Grandchild class inherits the properties of the Child class, which inherits the properties of the Parent class.

**Directing method calls**

The great advantage of polymorphism with multiple derived class objects is that calls to methods of the same name are directed to the appropriate overriding method.

![image](images/pgb138_1.jpg)

A base class may contain only virtual methods that each derived class may override with their own methods, but base class methods can still be called explicitly using the :: scope resolution operator. This can allow inconsistencies, however – this example would seem to imply that chickens can fly!

![image](images/commono.jpg)

birds.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Declare a base class named “Bird”, containing two virtual method declarations

**class Bird**

**{**

**public :**

**virtual void Talk() const**

**{ cout << “A bird talks... ” << endl ; }**

**virtual void Fly() const**

**{ cout << “A bird flies... ” << endl ; }**

**} ;**

![image](images/3o.jpg)Declare a derived class named “Pigeon”, containing two methods to override those in the base class

**class Pigeon : public Bird**

**{**

**public :**

**void Talk() const**

**{ cout << “Coo! Coo!” << endl ; }**

**void Fly() const**

**{ cout << “A pigeon flies away... ” << endl ; }**

**} ;**

![image](images/hot.jpg)

Overriding methods in a derived class may, optionally, include the **virtual** prefix – as a reminder it is overriding a base class method.

![image](images/4o.jpg)Declare a derived class named “Chicken”, containing two methods to override those in the base class

**class Chicken : public Bird**

**{**

**public :**

**void Talk() const**

**{ cout << “Cluck! Cluck!” << endl ; }**

**void Fly() const**

**{ cout << “I\’m just a chicken – I can\’t fly!” << endl ; }**

**} ;**

![image](images/5o.jpg)Declare a main method containing a final **return** statement and creating base class pointers binding derived classes

**int main()**

**{**

**Bird* pPigeon = new Pigeon ;**

**Bird* pChicken = new Chicken ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/pgb139_1.jpg)

![image](images/6o.jpg)In the main method, insert calls to each method

**pPigeon -> Talk() ;**

**pPigeon -> Fly() ;**

**pChicken -> Talk() ;**

**pChicken -> Fly() ;**

**pPigeon -> Bird::Talk() ;**

**pChicken -> Bird::Fly() ;          // Inappropriate call.**

![image](images/7o.jpg)Save, compile, and run the program to see the output

![image](images/pgb139_2.jpg)

![image](images/forget.jpg)

The backslash **\** character is required to escape the apostrophe in strings.

**Providing capability classes**

Classes whose sole purpose is to allow other classes to be derived from them are known as “capability classes” – they provide capabilities to the derived classes.

![image](images/pgb140_1.jpg)

Capability classes generally contain no data, but merely declare a number of virtual methods that can be overridden in their derived classes.

The following example builds upon the previous example to demonstrate how the “Bird” class can be better written as a capability class. Its methods no longer contain output statements, but return a **-1** (error) value if they are called explicitly.

It is necessary to change the return type of those methods from **void** to **int,** and these changes must also be reflected in each overriding method in the derived classes.

![image](images/commono.jpg)

capability.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Declare a base capability class named “Bird”, containing two virtual method declarations that will signal an error if called explicitly

**class Bird**

**{**

**public :**

**virtual int Talk() const { return -1 ; }**

**virtual int Fly() const { return -1 ; }**

**} ;**

![image](images/3o.jpg)Declare a derived class named “Pigeon”, containing two methods to override those in the base class

**class Pigeon : public Bird**

**{**

**public :**

**int Talk() const**

**{ cout << “Coo! Coo!” << endl ; return 0 ; }**

**int Fly() const**

**{ cout << “A pigeon flies away...” << endl ; return 0 ; }**

**} ;**

![image](images/forget.jpg)

The return value of overriding methods in derived classes must match those declared in the base class.

![image](images/4o.jpg)Declare a derived class named “Chicken” containing two methods to override those in the base class

**class Chicken : public Bird**

**{**

**public :**

**int Talk() const**

**{ cout << “Cluck! Cluck!” << endl ; return 0 ; }**

**int Fly() const**

**{ cout << “I\’m just a chicken – I can\’t fly!”** **<< endl ; return 0 ; }**

**} ;**

![image](images/5o.jpg)Declare a main method creating base class pointers binding the derived classes

**int main()**

**{**

**Bird* pPigeon = new Pigeon ;**

**Bird* pChicken = new Chicken ;**

**}**

![image](images/6o.jpg)In the main method, insert method calls and a statement to terminate the program when an error is met by explicitly calling a base class method

**pPigeon -> Talk() ;**

**pChicken -> Talk() ;**

**pPigeon -> Bird::Talk() ;**

**if ( -1 ) { cout << “Error! - Program ended.”**

**<< endl ; return 0 ; }**

**pPigeon -> Fly() ;          // Call will not be made.**

**pChicken -> Fly() ;       // Call will not be made.**

**return 0 ;                      // Statement will not be executed.**

![image](images/7o.jpg)Save, compile, and run the program to see the output

![image](images/pgb141_1.jpg)

![image](images/snake.jpg)

Capability class methods are intended to be overridden in derived classes – they should not be called explicitly.

![image](images/hot.jpg)

Refer back [here](#chapter16.xhtml_sec132) for more details on error handling.

**Making abstract data types**

An Abstract Data Type (ADT) represents a concept, rather than a tangible object, and is always the base to other classes. A base class can be made into an ADT by initializing one or more of its methods with 0\. These are known as “pure virtual methods” and must always be overridden in derived classes.

![image](images/commono.jpg)

adt.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Declare a base ADT class named “Shape”, containing three pure virtual methods

**class Shape**

**{**

**public :**

**virtual int getArea() = 0 ;**

**virtual int getEdge() = 0 ;**

**virtual void Draw() = 0 ;**

**} ;**

![image](images/3o.jpg)Declare a derived class named “Rect”, containing two private variables

**class Rect : public Shape**

**{**

**private :**

**int height, width ;**

**} ;**

![image](images/4o.jpg)In the derived class declaration, insert a public constructor and destructor

**public :**

**Rect( int initWidth, int initHeight )**

**{**

**height = initHeight ;**

**width = initWidth ;**

**}**

**~Rect() ;**

![image](images/snake.jpg)

It is illegal to create an instance object of an ADT – attempting to do so will simply create a compiler error.

![image](images/5o.jpg)In the derived “Rect” class declaration, declare three public methods to override the pure virtual methods declared in the “Shape” base class

**int getArea() { return height * width } ;**

**int getEdge() { return ( 2 * height ) + ( 2 * width ) ; }**

**void Draw()**

**{**

**for ( int i = 0 ; i < height ; i++ ) {**

**for ( int j = 0 ; j < width ; j++ ) { cout << “x ” ; }**

**cout << endl ; }**

**}**

![image](images/pgb143_1.jpg)

![image](images/6o.jpg)Declare a main method containing a final **return** statement and creating two instances of the derived “Rect” class – to represent a Square and a Quadrilateral shape

**int main**

**{**

**Shape* pQuad = new Rect( 3, 7 ) ;**

**Shape* pSquare = new Rect( 5, 5 ) ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/pgb143_2.jpg)

![image](images/7o.jpg)In the main method, insert calls to each method then save, compile, and run the program to see the output

**pQuad -> Draw() ;**

**cout << “Area is ” << pQuad -> getArea() << endl ;**

**cout << “Perimeter is ” << pQuad -> getEdge() << endl ;**

**pSquare -> Draw() ;**

**cout << “Area is ” << pSquare -> getArea() << endl ;**

**cout << “Perimeter is ”<< pSquare -> getEdge() <<endl ;**

![image](images/pgb143_3.jpg)

![image](images/forget.jpg)

A base class need only contain one pure virtual method to create an Abstract Data Type.

**Building complex hierarchies**

It is sometimes desirable to derive an ADT from another ADT to construct a complex hierarchy of classes. This provides great flexibility and is perfectly acceptable, providing each pure method is defined at some point in a derived class.

![image](images/commono.jpg)

hierarchy.cpp

![image](images/1o.jpg)Start a new program by specifying the C++ library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/2o.jpg)Declare a base ADT class named “Boat”, containing a variable and accessor method together with one pure virtual method

**class Boat**

**{**

**protected:**

**int length ;**

**public :**

**int getLength() { return length ; }**

**virtual void Model() = 0 ;**

**} ;**

![image](images/3o.jpg)Declare an ADT class (derived from the Boat class) named “Sailboat” – also containing a variable and accessor method together with one pure virtual method

**class Sailboat : public Boat**

**{**

**protected :**

**int mast ;**

**public :**

**int getMast() { return mast ; }**

**virtual void Boom() = 0 ;**

**} ;**

![image](images/4o.jpg)Declare a regular class (derived from the Sailboat class) named “Laser”, in which all members will allow public access

**class Laser : public Sailboat**

**{**

**public :**

**} ;**

![image](images/pgb144_1.jpg)

![image](images/forget.jpg)

The Boat class has properties common to any boat, whereas the Sailboat class has properties specific to boats that have sails.

![image](images/5o.jpg)In the Laser class, insert a call to its constructor method to assign values to the variables in each class from which this class is derived – and call the destructor method

**Laser() { mast = 19 ; length = 35 ; }**

**~Laser() ;**

![image](images/pgb145_1.jpg)

![image](images/6o.jpg)In the Laser class, define the pure virtual methods declared in each class from which this class is derived

**void Model() { cout << “Laser Classic” << endl ; }**

**void Boom() { cout << “Boom: 14ft” << endl ; }**

![image](images/7o.jpg)Declare a main method containing a final **return** statement and creating an instance of the derived class on the bottom tier of the hierarchy

**int main()**

**{**

**Laser* pLaser = new Laser ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/8o.jpg)In the main method, insert calls to each defined method

**pLaser -> Model() ;**

**cout << “Length: “ <<**

**pLaser -> getLength() << “ft” << endl ;**

**cout << “Height: “<<**

**pLaser -> getMast() << “ft” << endl ;**

**pLaser -> Boom() ;**

![image](images/9o.jpg)Save, compile, and run the program to see the output

![image](images/pgb145_2.jpg)

![image](images/hot.jpg)

Try adding a Powerboat class derived from the Boat class (to contain engine information), and a Cruiser class derived from the Powerboat class – to assign variable values and to define virtual methods.

**Isolating class structures**

![image](images/pgb146_1.jpg)

The source code for each example program in the C# section of this book is generally contained in a single **.cpp** file to save space, but in reality OOP programs are often contained in three separate files:

•Header **.h** file – contains only class declarations.s

•Implementation **.cpp** file – contains class definitions to implement the methods declared in the header file, which is referenced by an **#include** directive.

•Client **.cpp** file – contains a **main** method that employs the class members declared in the header file, which is also referenced by an **#include** directive.

For example, a sum calculator program might comprise three files named **ops.h** (a header file declaring operation classes), **ops.cpp** (an implementation file defining the operation methods), and **sum.cpp** (a client file calling the various operations).

When compiling **sum.cpp**, the compiler incorporates the included header file and implementation file into the program. It first translates the header file and implementation file into a binary object file (**ops.o**), then it translates the header file and client file into a second binary object file (**sum.o**). Finally, the Linker combines both object files into a single executable file (**sum.exe**).

![image](images/pgb146_2.jpg)

Isolating class structures in separate “modular” files has the advantage of improving portability, and makes code maintenance easier by clearly identifying the purpose of each file.

![image](images/hot.jpg)

The client file is sometimes referred to as a “driver” file.

![image](images/hot.jpg)

Using an **#include** directive to reference a header file works in a similar manner to using an **#include** directive to reference a standard C++ library.

To have the compiler combine all three source code files into a single, executable file it is only necessary to explicitly specify the **.cpp** files in the compiler command – an **#include** directive ensures the header file will also be recognized.

For example, with the statement **#include “ops.h”** in both **ops.cpp** and **sum.cpp,** the command to compile the example described opposite need not specify the **ops.h** header in the compiler command, but is just **c++ ops.cpp sum.cpp -o sum.exe**.

![image](images/pgb147_1.jpg)

Calculator

This example will allow the user to input a simple arithmetical expression and output the calculated result. It will provide instructions when first launched and allow the user to make subsequent expressions – or exit by entering a 0 character.

![image](images/pgb147_2.jpg)

ops.h

![image](images/1o.jpg)Start a header file by declaring a class named “Calculator”

**class Calculator**

**{**

**} ;**

![image](images/2o.jpg)In the class declaration, insert public method declarations

**public :**

**Calculator() ;               // (Constructor) To set initial status.**

**void launch() ;            // To display initial instructions.**

**void readInput() ;       // To get expression.**

**void writeOutput() ;   // To display result.**

**bool run() ;                  // (Accessor) To get current status.**

![image](images/3o.jpg)In the class declaration, insert private variable declarations

**private :**

**double num1, num2 ; // To store input numbers.**

**char oper ;                  // To store input operator.**

**bool status ;                // To store current status.**

![image](images/4o.jpg)Save the header file as “ops.h”

![image](images/5o.jpg)Turn [here](#chapter19.xhtml_sec161) to continue this example by creating an implementation file – containing definitions for the Calculator class methods declared in the “ops.h” header file

![image](images/snake.jpg)

Notice that the header file name must be surrounded by quotes in an **#include** directive – not by the < > angled brackets used to include a standard C++ library.

**Employing isolated classes**

![image](images/commono.jpg)

ops.cpp

![image](images/6o.jpg)Start an implementation file with **include** directives for the header file created [here](#chapter19.xhtml_mpile), and the standard C++ library supporting input/output statements

**#include “ops.h”              // Reference header file.**

**#include <iostream>**

**using namespace std ;**

![image](images/7o.jpg)Add the following definitions for each method in the header file, then save the implementation file as “ops.cpp”

**Calculator::Calculator()**

**{ status = true ; }                    // Initialize status.**

**void Calculator::launch()     // Display instructions.**

**{**

**cout << endl << “*** SUM CALCULATOR ***” << endl ;**

**cout << “Enter a number, an operator(+,-,*,/), and**

**another number.” << endl << “Hit Return to**

**calculate. Enter 0 to exit.” << endl ;**

**}**

**void Calculator::readInput()                    // Get expression.**

**{**

**cout << “> “ ; cin >> num1 ;                  // Get 1st number.**

**if ( num1 == 0 ) status = false ;            // Exit if it’s 0.**

**else { cin >> oper ; cin >> num2 ; }     // Or get the rest.**

**}**

**void Calculator::writeOutput()              // Display result.**

**{**

**if ( status ) switch( oper )                  // If continuing.**

**{                                                           // Show result.**

**case ‘+’ : { cout << ( num1 + num2 ) << endl ; break ; }**

**case ‘-’ : { cout << ( num1 - num2 ) << endl ; break ; }**

**case ‘*’ : { cout << ( num1 * num2 ) << endl ; break ; }**

**case ‘/’ : if ( num2 != 0 )**

**cout << ( num1 / num2 ) << endl ;**

**else cout << “Cannot divide by 0” << endl ;**

**}**

**}**

**bool Calculator::run()                    // Get the current status.**

**{ return status ; }**

![image](images/snake.jpg)

Due to space limitation, this program makes barely any attempt at input validation – it assumes the user will enter a valid expression, such as 8 * 3.

![image](images/commono.jpg)

sum.cpp

![image](images/8o.jpg)Start a client file with an include directive to incorporate the header file created [here](#chapter19.xhtml_mpile)

**#include “ops.h”**

![image](images/9o.jpg)Declare a main method containing a final **return** statement, and creating a pointer plus a call to display instructions

**int main()**

**{**

**Calculator* pCalc = new Calculator ;**

**pCalc -> launch() ;**

**// Add more statements here.**

**return 0 ;**

**}**

![image](images/10o.jpg)In the main method, insert a loop to read expressions and write results while the program status permits

**while ( pCalc -> run() )**

**{**

**pCalc -> readInput() ;**

**pCalc -> writeOutput() ;**

**}**

![image](images/11o.jpg)Save the client file as “sum.cpp”, alongside “ops.h” and “ops.cpp”, then compile the program with this command
**c++ ops.cpp sum.cpp -o sum.exe**

![image](images/12o.jpg)Run the program and enter simple expressions to see the results, then enter 0 and hit **Return** to exit the program

![image](images/pgb149_1.jpg)

![image](images/forget.jpg)

This program loops until the user types a 0 and hits Return – changing the “status” control variable to **false,** and so exiting the program.

**Summary**

![image](images/pgb150_1.jpg)

•The three cornerstones of Object Oriented Programming are encapsulation, inheritance, and polymorphism.

•Polymorphic entities have a different meaning, or purpose, according to their context.

•A base class pointer can be used to call inherited methods in the derived class to which it is bound.

•A base class pointer can also be used to explicitly call base class methods using the :: scope resolution operator.

•Virtual base class methods are intended to be overridden in derived classes.

•Polymorphism allows calls to methods of the same name to be directed to the appropriate overriding method.

•Capability classes generally contain no data, but merely declare virtual methods that can be overridden in derived classes.

•Virtual methods that return a **-1** value signal an error to indicate they should not be called directly.

•An Abstract Data Type represents a concept, and is always the base to other classes.

•Declaration of a pure virtual method, with the assignation **=0**, indicates that class is an ADT.

•Classes can be derived from an ADT – but you cannot create an instance of an ADT.

•An ADT can be derived from another ADT to create a complex hierarchy of classes.

•Programs can be separated into header, implementation, and client files to aid portability and to ease code maintenance.

•Header files that are referenced by **#include** directives will be automatically included by the compiler during compilation.

20

**Processing macros**

***This chapter demonstrates how the C++ compiler can be made to perform useful tasks before compiling a program.***

[Exploring compilation](#chapter20.xhtml_sec163)

[Defining substitutes](#chapter20.xhtml_sec164)

[Defining conditions](#chapter20.xhtml_sec165)

[Providing alternatives](#chapter20.xhtml_sec166)

[Guarding inclusions](#chapter20.xhtml_sec167)

[Using macro functions](#chapter20.xhtml_sec168)

[Building strings](#chapter20.xhtml_sec169)

[Debugging assertions](#chapter20.xhtml_sec170)

[Summary](#chapter20.xhtml_sec171)

**Exploring compilation**

Whenever the C++ compiler runs, it first calls upon its preprocessor to seek any compiler directives that may be included in the source code. Each of these begin with the **#** hash character and will be implemented first to effectively modify the source code before it is assembled and compiled.

![image](images/pgb152_1.jpg)

The changes made by compiler directives to the preprocessor create new temporary files that are not normally seen. It is these temporary files that are used to create a binary object file:

•The first temporary file created during compilation expands the original source code by replacing its compiler directives with library code that implements those directives. This text file is named like the source file, but with a **.ii** file extension.

•The second temporary file created during compilation is a translation of the temporary expanded **.ii** file into low-level Assembly language instructions. This text file is named like the source file, but with a **.s** file extension.

•The third temporary file created during compilation is a translation of the temporary Assembly language **.s** file into machine code. This binary object file is named like the source file, but with a **.o** file extension.

So, the compilation process employs the Preprocessor to compile source code, an “Assembler” to translate this into machine code, and a Linker to convert one or more binary objects into an executable program.

You can see the temporary files by instructing the compiler to save them using the **-save-temps** compiler option. Both temporary text files can then be examined by opening them in a plain text editor.

Most significantly, you can see that the temporary file with the **.ii** file extension contains the complete function definitions from any included library. For example, it replaces an **#include <iostream>** directive with definitions for the **cin**, **cout, cerr** functions, and the **clog** function that can be used to redirect error messages to a file. The end of the **.ii** file shows the defined functions to be part of the “std” namespace – so they can appear without the **std::** prefix.

![image](images/commonbb.jpg)

prog.cpp

![image](images/1bl.jpg)Create a simple program named “prog.cpp” that will output a message when it gets executed

**#include <iostream>**

**using namespace std ;**

**int main()**

**{**

**cout << “This is a simple test program” << endl ;**

**return 0 ;**

**}**

![image](images/2bl.jpg)Issue a command using the **-save-temps** option, to save temporary files, and a **-c** option to compile this program’s source files into an object file – with no executable file **c++ prog.cpp -save-temps -c**

![image](images/3bl.jpg)Open the **.ii** file in a plain text editor such as Notepad, then scroll to the end of the file to see the modified source code – notice how the **<iostream>** library functions are defined in the **std** namespace

![image](images/pgb153_1.jpg)

![image](images/4bl.jpg)Open the **.s** file in a plain text editor to see the low-level assembler instructions – notice how the message string is now terminated by the special **\0** character

![image](images/5bl.jpg)Issue a command to output an executable file from the **.o** object file, then run the program to see the message **c++ prog.o -o prog.exe**

![image](images/pgb153_2.jpg)

![image](images/forget.jpg)

One or more object files can be used to create an executable file – as described [here](#chapter19.xhtml_sec160).

![image](images/hot.jpg)

You can combine these steps, creating an executable file and saving temporary files, by issuing the command **c++ prog.cpp** **-save-temps -o prog.exe**.

**Defining substitutes**

Just as the preprocessor substitutes library code for **#include** directives, other preprocessor directives can be used to substitute text or numeric values before assembly and compilation.

![image](images/pgb154_1.jpg)

The **#define** directive specifies a macro, comprising an identifier name and a string or numeric value, to be substituted by the preprocessor for each occurrence of that macro in the source code.

Like **#include** preprocessor directives, **#define** directives can appear at the start of the source code. As with constant variable names, the macro name traditionally uses uppercase, and defined string values should be enclosed within double quotes. For numeric substitutions in expressions, the macro name should be enclosed in parentheses to ensure correct precedence.

![image](images/commonbb.jpg)

define.cpp

![image](images/1bl.jpg)Start a new program by declaring three **define** directives

**#define BOOK “C++ Programming in easy steps”**

**#define NUM 200**

**#define RULE “*******************************”**

![image](images/2bl.jpg)Specify the library classes to include, and the namespace

**#include <iostream>**

**using namespace std ;**

![image](images/3bl.jpg)Add a main function containing a final **return** statement and three statements to output substituted values

**int main()**

**{**

**cout << RULE << endl << BOOK << endl << RULE ;**

**cout << endl << “NUM is: ” << NUM << endl ;**

**cout << “Double NUM: ” << ( ( NUM ) * 2 ) << endl ;**

**return 0 ;**

**}**

![image](images/4bl.jpg)Save, compile, and run the program to see the output

![image](images/pgb154_2.jpg)

![image](images/snake.jpg)

Numeric constants are often best declared as **const** variables – because values substituted by the preprocessor are not subject to type-checking.

![image](images/5bl.jpg)Recompile the program, saving the temporary files **c++ define.cpp -save-temps -o define.exe**

![image](images/6bl.jpg)Open the temporary “define.ii” file in a plain text editor and scroll to the end of the file to see the substitutions

![image](images/pgb155_1.jpg)

Substitutions can alternatively be made from the command-line using a **-D*name*** option to replace macros with specified values. Note that string values within double-quotes must also be enclosed in escaped quotes in the command – so the substitution will include the double-quote characters.

![image](images/7bl.jpg)Delete, or comment-out, the **define** directives for both the **BOOK** and **NUM** identifiers – then save the program file to apply the changes

![image](images/8bl.jpg)Recompile the program, specifying substitute macro values, then run the program once more **c++ -DNUM=50 -DBOOK=\””Java in easy steps”\”**
**define.cpp -o define.exe**

![image](images/pgb155_2.jpg)

![image](images/hot.jpg)

Linux users can employ escaped double quotes **\””*string*”\”** or plain single quotes **‘“*string*”’** to enclose a quoted string in a command.

![image](images/forget.jpg)

Attempting to compile a program in which an identifier has not been defined will produce a “not declared in this scope” error.

**Defining conditions**

The preprocessor can make intelligent insertions to program source code by using macro functions to perform conditional tests. An **#ifdef** directive performs the most common preprocessor function by testing to see if a specified macro has been defined. When the macro has been defined, so the test returns true, the preprocessor will insert all directives, or statements, on subsequent lines up to a corresponding **#endif** directive.

![image](images/pgb156_1.jpg)

Conversely, an **#ifndef** directive tests to see if a specified macro has not been defined. When that test returns true, it will insert all directives, or statements, on subsequent lines up to a corresponding **#endif** directive.

To satisfy either conditional test, it should be noted that a **#define** directive need only specify the macro name to define the identifier – it need not specify a value to substitute.

Any previously defined macro can be removed later using the **#undef** directive – so that subsequent **#ifdef** conditional tests fail. The macro can then be redefined by a further **#define** directive:

![image](images/commonbb.jpg)

ifdef.cpp

![image](images/1bl.jpg)Start a new program with a conditional test to insert a directive when a macro is not already defined

**#ifndef BOOK**

**#define BOOK “C++ Programming in easy steps”**

**#endif**

![image](images/2bl.jpg)Specify the library classes to include, and the namespace

**#include <iostream>**

**using namespace std ;**

![image](images/3bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/4bl.jpg)In the main function, add a conditional preprocessor test to insert an output statement when the test succeeds

**#ifdef BOOK**

**cout << BOOK ;**

**#endif**

![image](images/5bl.jpg)Add another conditional preprocessor test to both define a new macro and insert an output statement when the test succeeds

**#ifndef AUTHOR**

**#define AUTHOR “Mike McGrath”**

**cout << “ by ” << AUTHOR << endl ;**

**#endif**

![image](images/6bl.jpg)Next, add a conditional test to undefine a macro if it has already been defined

**#ifdef BOOK**

**#undef BOOK**

**#endif**

![image](images/7bl.jpg)Now, add a conditional test to redefine a macro if it is no longer defined, and to insert an output statement

**#ifndef BOOK**

**#define BOOK “Linux in easy steps”**

**cout << BOOK “ by “ << AUTHOR << endl ;**

**#endif**

![image](images/8bl.jpg)Save, compile, and run the program to see the insertions

![image](images/pgb157_1.jpg)

![image](images/9bl.jpg)Recompile the program, this time defining the **BOOK** macro in the command, then run the program again to see the specified value appear in the first line of output
**c++ -DBOOK=\”“Python in easy steps”\” ifdef.cpp -o ifdef.exe**

![image](images/pgb157_2.jpg)

![image](images/snake.jpg)

Each preprocessor directive must appear on its own line – you cannot put multiple directives on the same line.

![image](images/forget.jpg)

On Windows systems, string macro values specified in a command must be enclosed in escaped double quotes.

**Providing alternatives**

![image](images/pgb158_1.jpg)

The conditional test performed by **#ifdef** and **#ifndef** can be extended to provide an alternative by adding an **#else** directive. For example:

**#ifdef WEATHER**

**cout << WEATHER ;**

**#else**

**#define WEATHER “Sunny”**

**#endif**

Similarly, **#if**, **#else**, and **#elif** macros can perform multiple conditional tests, much like the regular C++ **if** and **else** keywords.

For testing multiple definitions, the **#ifdef** macro can be expressed as **#if defined**, and further tests made by **#elif defined** macros.

While most macros are defined in the source file with a **#define** directive, or on the command line with the **-D** option, some macros are automatically predefined by the compiler. Typically, these have names beginning with a double underscore __ to avoid accidental confusion with chosen names. The compiler’s predefined macros are platform-specific, so a program can employ a multiple definition test to identify the host platform:

![image](images/commonbb.jpg)

else.cpp

![image](images/1bl.jpg)Launch a plain text editor and save a new file (without any content) as “empty.txt” in your program’s directory

![image](images/2bl.jpg)To see a list of the compiler’s predefined macros, issue a command calling the cpp preprocessor directly with a “-dM” option on the empty file

**cpp -dM empty.txt**

![image](images/3bl.jpg)Scroll through the list to find the “_WIN32” macro on Windows or the “__linux” macro on Linux systems

![image](images/pgb158_2.jpg)

![image](images/pgb158_3.jpg)

![image](images/hot.jpg)

The **#elif** macro simply combines **else** and **if** to offer an alternative test.

![image](images/snake.jpg)

Use the **cpp** command to call the preprocessor directly (not the **c++** command) and ensure the **-dM** option is capitalized correctly.

![image](images/4bl.jpg)Start a new program with a conditional test to seek the _WIN32 and __linux macros – to identify the platform

**#if defined _WIN32**

**#define PLATFORM “Windows”**

**#elif defined __linux**

**#define PLATFORM “Linux”**

**#endif**

![image](images/5bl.jpg)Specify the library classes to include, and the namespace

**#include <iostream>**

**using namespace std ;**

![image](images/6bl.jpg)Now, add a main function containing a final **return** statement and a statement to identify the host platform

**int main()**

**{**

**cout << PLATFORM << “ System” << endl ;**

**return 0 ;**

**}**

![image](images/7bl.jpg)In the main function, insert statements to execute for specific platforms

**if ( PLATFORM == “Windows” )**

**cout << “Performing Windows-only tasks...” << endl ;**

**if ( PLATFORM == “Linux” )**

**cout << “Performing Linux-only tasks...” << endl ;**

![image](images/8bl.jpg)Save, compile, and run the program to see platform-specific output

![image](images/pgb159_1.jpg)

![image](images/pgb159_2.jpg)

![image](images/snake.jpg)

The predefined **_WIN32** macro has one underscore but the **__linux** macro has two underscore characters.

![image](images/forget.jpg)

The conditional test of predefined macros could be extended to seek those of other operating systems, and a final **#else** directive added to specify an “Unknown” default.

**Guarding inclusions**

Typically, a C++ program will have many **.h** header files and a single **.cpp** implementation file containing the main program. Header files may often contain one or more **#include** directives to make other classes or functions available from other header files, and can cause duplication where definitions appear in two files. For example, where a header file includes another header file containing a function definition, the compiler will consider that definition to appear in each file – so compilation will fail.

![image](images/pgb160_1.jpg)

The popular solution to this problem of re-definition employs preprocessor directives to ensure the compiler will only be exposed to a single definition. These are known as “inclusion guards” and create a unique macro name for each header file. Traditionally, the name is an uppercase version of the file name, with the dot changed to an underscore – for example, **RUM_H** for a file **rum.h**.

![image](images/hot.jpg)

Inclusion guards are also known as “macro guards” or simply as “include guards”.

In creating a macro to guard against duplication, an **#ifndef** directive first tests to see if the definition has already been made by another header file included in the same program. If the definition already exists, the compiler ignores the duplicate definition, otherwise a **#define** directive will permit the compiler to use the definition in that header file:

![image](images/commonhr.jpg)

add.h

![image](images/1bl.jpg)Create a header file named “add.h” containing the inline declaration of an “add” function

**inline int add ( int x, int y ) { return ( x + y ) ; }**

![image](images/2bl.jpg)Now, create a header file named “triple.h” containing a processor directive to make the add function available for use in the inline declaration of a “triple” function

**#include “add.h”**

**inline int triple ( x ) { return add( x, add( x, x ) ) ; }**

![image](images/commonhr.jpg)

triple.h

![image](images/3bl.jpg)Start a new program with preprocessor directives to make both the add and triple functions available

**#include “add.h”**

**#include “triple.h”**

![image](images/commonbb.jpg)

guard.cpp

![image](images/4bl.jpg)Specify the library classes to include, and the namespace

**#include <iostream>**

**using namespace std ;**

![image](images/5bl.jpg)Add a main function containing statements that call both the **add()** and **triple()** functions from the included headers

**int main()**

**{**

**cout << “9 + 3 = “ << add( 9, 3 ) << endl ;**

**cout << “ 9 x 3 = “ << triple( 9 ) << endl ;**

**return 0 ;**

**}**

![image](images/6bl.jpg)Save the files, then attempt to compile the program to see compilation fail because the add function appears to be defined twice – in “add.h” and by inclusion in “triple.h”

![image](images/pgb161_1.jpg)

![image](images/7bl.jpg)Edit the header file “add.h” to enclose the inline function declaration within a preprocessor inclusion guard

**#ifndef ADD_H**

**#define ADD_H**

**inline int add ( int x, int y ) { return ( x + y ) ; }**

**#endif**

![image](images/8bl.jpg)Save the modified file, then compile and run the program – compilation now succeeds because the inclusion guard prevents the apparent re-definition of the add function

![image](images/pgb161_2.jpg)

![image](images/snake.jpg)

Use the conventional naming scheme, where the macro name resembles the file name, to avoid conflicts.

![image](images/forget.jpg)

All header files should contain header guards – add a **TRIPLE_H** macro to the **triple.h** file.

**Using macro functions**

The **#define** directive can be used to create macro functions that will be substituted in the source code before compilation.

![image](images/pgb162_1.jpg)

A preprocessor function declaration comprises a macro name, immediately followed by parentheses containing the function’s arguments – it is important not to leave any space between the name and the parentheses. The declaration is then followed by the function definition within another set of parentheses. For example, a preprocessor macro function to half an argument looks like this:

**#define HALF( n ) ( n / 2)**

Care should be taken when using macro functions, because unlike regular C++ functions, they do not perform any kind of type checking – so it’s quite easy to create a macro that causes errors. For this reason, inline functions are usually preferable to macro functions, but because macros directly substitute their code, they avoid the overhead of a function call – so the program runs faster. The resulting difference can be seen in the first temporary file created during the compilation process:

![image](images/commonbb.jpg)

macro.cpp

![image](images/1bl.jpg)Start a new program by defining two macro functions to manipulate a single argument

**#define SQUARE( n ) ( n * n )**

**#define CUBE( n ) ( n * n * n )**

![image](images/2bl.jpg)After the macro function definitions, specify the library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/3bl.jpg)Next, declare two inline functions to manipulate a single argument – just like the macro functions defined above

**inline int square ( int n ) { return ( n * n ) ; }**

**inline int cube ( int n ) { return ( n * n * n ) ; }**

![image](images/4bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/5bl.jpg)At the start of the main function block, declare and initialize an integer variable

**int num = 5 ;**

![image](images/6bl.jpg)Now, insert statements to call each macro function and each comparable inline function

**cout << “Macro SQUARE: ” << SQUARE( num ) << endl ;**

**cout << “Inline square: ” << square( num ) << endl ;**

**cout << “Macro CUBE: ” << CUBE( num ) << endl ;**

**cout << “Inline cube: ” << cube( num ) << endl ;**

![image](images/7bl.jpg)Save the file, then compile the program, saving the temporary files and run the program
**c++ macro.cpp -save-temps -o macro.exe**

![image](images/pgb163_1.jpg)

![image](images/8bl.jpg)Open the temporary “.ii” file in a plain text editor like Notepad, to see that the macro functions have been directly substituted in each output statement

![image](images/pgb163_2.jpg)

![image](images/hot.jpg)

Using uppercase for macro names ensures that macro functions will not conflict with regular lowercase function names.

![image](images/forget.jpg)

An inline function saves the overhead of checking between a function prototype declaration and its definition.

**Building strings**

The preprocessor **#** operator is known as the “stringizing” operator, as it converts a series of characters passed as a macro argument into a string – adding double quotes to enclose the string.

![image](images/pgb164_1.jpg)

All whitespace before or after the series of characters passed as a macro argument to the stringizing operator is ignored, and multiple spaces between characters is reduced to just one space.

The stringizing operator is useful to pass string values to a preprocessor **#define** directive without needing to surround each string with double quotes.

A macro definition can combine two terms into a single term using the **##** merging operator. Where the combined term is a variable name, its value is not expanded by the macro – it simply allows the variable name to be substituted by the macro.

![image](images/commonbb.jpg)

strung.cpp

![image](images/1bl.jpg)Start a new program by defining a macro to create a string from a series of characters passed as its argument, to substitute in an output statement

**#define LINEOUT( str ) cout << #str << endl**

![image](images/2bl.jpg)Define a second macro to combine two terms passed as its arguments into a variable name, to substitute in an output statement

**#define GLUEOUT( a, b ) cout << a##b << endl**

![image](images/3bl.jpg)After the macro definitions, specify the library classes to include, and a namespace prefix to use

**#include <string>**

**#include <iostream>**

**using namespace std ;**

![image](images/4bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/5bl.jpg)At the start of the main function block, declare and initialize a string variable, then append a further string

**string longerline = “They carried a net ” ;**

**longerline += “and their hearts were set” ;**

![image](images/6bl.jpg)Now, add statements to output text using the macros

**LINEOUT(In a bowl to sea went wise men three) ;**

**LINEOUT(On a brilliant night in June) ;**

**GLUEOUT( longer, line ) ;**

**LINEOUT(On fishing up the moon.) ;**

![image](images/7bl.jpg)Save the file, then compile the program, saving the temporary files and run the program
**c++ strung.cpp -save-temps -o strung.exe**

![image](images/pgb165_1.jpg)

![image](images/8bl.jpg)Open the temporary “.ii” file in a plain text editor, like Notepad, to see that the string values and the variable name have been substituted in the output statements

![image](images/pgb165_2.jpg)

![image](images/hot.jpg)

Notice that the second statement contains multiple spaces, which will be removed by the stringizing operator.

![image](images/forget.jpg)

The merging operator is alternatively known as the “token-pasting” operator, as it pastes two “tokens” together.

**Debugging assertions**

It is sometimes helpful to use preprocessor directives to assist with debugging program code – by defining an **ASSERT** macro function to evaluate a specified condition for a Boolean value.

![image](images/pgb166_1.jpg)

The condition to be evaluated will be passed from the caller as the **ASSERT** function argument. The function can then execute appropriate statements according to the result of the evaluation. Multiple statements can be included in the macro function definition by adding a backslash **\** at the end of each line, allowing the definition to continue on the next line.

Numerous statements calling the **ASSERT** function can be added to the program code to monitor a condition as the program proceeds. For example, to check the value of a variable as it changes.

![image](images/forget.jpg)

You can comment-out sections of code when debugging using C-style /* */ comment operators.

Usefully, an **ASSERT** function can be controlled by a **DEBUG** macro. This allows debugging to be easily turned on and off simply by changing the value of the **DEBUG** control macro:

![image](images/commonbb.jpg)

assert.cpp

![image](images/1bl.jpg)Start a new program by defining a DEBUG macro with an “on” value of 1 – to control an ASSERT function

**#define DEBUG 1**

![image](images/2bl.jpg)Next, add a macro **if-elif** statement block to define the ASSERT function according to the control value

**#if( DEBUG == 1 )**

**// Definition for “on” goes here.**

**#elif( DEBUG == 0 )**

**// Definition for “off” goes here.**

**#endif**

![image](images/3bl.jpg)In the top part of the ASSERT function statement block insert a definition for when the debugging control is set to “on” – to output failure details from predefined macros

| **#define ASSERT( expr )** | **\** |
| **cout << #expr << “ ...” << num ;** | **\** |
| **if ( expr != true )** | **\** |
| **{** | **\** |
| **cout << “ Fails in file: ” << __FILE__ ;** | **\** |
| **cout << “ at line: ” << __LINE__ << endl ;** | **\** |
| **}** | **\** |

**else cout << “ Succeeds” << endl ;**

![image](images/snake.jpg)

Do not place a backslash continuation character on the last line of the definition, and remember to use the # stringizing operator to output the expression as a string.

![image](images/4bl.jpg)In the bottom part of the ASSERT function statement block, insert a definition for when the debugging control is set to “off ” – to simply output the current variable value

**#define ASSERT( result ) \**

**cout << “Number is “ << num << endl ;**

![image](images/5bl.jpg)After the macro definitions, specify the library classes to include, and a namespace prefix to use

**#include <iostream>**

**using namespace std ;**

![image](images/6bl.jpg)Add a main function containing a final **return** statement

**int main()**

**{**

**// Program code goes here.**

**return 0 ;**

**}**

![image](images/7bl.jpg)At the start of the main function block, declare and initialize an integer variable, then call the macro ASSERT function to check its value as it gets incremented

| **int num = 9 ;** | **  ASSERT( num < 10 ) ;** |
| **num++ ;** | **  ASSERT( num < 10 ) ;** |

![image](images/8bl.jpg)Save, compile, and run the program to see the output

![image](images/pgb167_1.jpg)

![image](images/9bl.jpg)Edit the program to turn debugging off by changing the control value, then recompile and re-run the program

**#define DEBUG 0**

![image](images/pgb167_2.jpg)

![image](images/forget.jpg)

Predefined macro names are prefixed by a double underscore and suffixed by a double underscore.

![image](images/hot.jpg)

Additionally, the current date and time can be output from the **__DATE__** and **__TIME__** predefined macros.

**Summary**

![image](images/pgb114_1.jpg)

•The C++ compiler’s **-save-temps** option saves the temporary files created during the compilation process for examination.

•Compilation first writes program code and included library code into a single **.ii** text file, which is then translated into low-level Assembly language as a **.s** text file.

•Assembly language **.s** files are translated to machine code as **.o** object files, which are used to create the executable program.

•A **#define** directive defines a macro name and a value that the preprocessor should substitute for that name in program code.

•The preprocessor can be made to perform conditional tests using **#ifdef**, **#ifndef**, and **#endif** directives.

•Preprocessor alternatives can be provided using **#if**, **#else**, and **#elif** directives, and a definition can be removed using **#undef**.

•Each header file should use inclusion guards to prevent accidental multiple definition of the same class or function.

•The macro name of an inclusion guard is an uppercase version of the file name, but with the dot replaced by an underscore.

•A **#define** directive may also define a macro function that will be substituted in program code in place of the macro name.

•Inline functions are usually preferable to macro functions because, unlike macro functions, they perform type checking.

•The preprocessor **#** stringizing operator converts a series of characters passed as a macro argument into a string value.

•Two terms can be combined into a single term by the preprocessor **##** merging operator.

•An **ASSERT** macro function is useful for debugging code, and may be controlled by a **DEBUG** macro to easily turn debugging on or off.

21

**Programming visually**

***This chapter brings together elements from previous chapters to build a complete C++ application in a visual programming environment.***

[Starting a Universal project](#chapter21.xhtml_sec172)

[Inserting page components](#chapter21.xhtml_sec173)

[Importing program assets](#chapter21.xhtml_sec174)

[Designing the layout](#chapter21.xhtml_sec175)

[Adding runtime function](#chapter21.xhtml_sec176)

[Testing the program](#chapter21.xhtml_sec177)

[Adjusting the interface](#chapter21.xhtml_sec178)

[Deploying the application](#chapter21.xhtml_sec179)

[Summary](#chapter21.xhtml_sec180)

**Starting a Universal project**

![image](images/pgb170_1.jpg)

Windows 10 introduced the **Universal Windows Platform** (UWP) that enables you to create a single **Universal Windows Application** (UWA) that will run on any modern Windows-based device. The interface layout of a UWA uses the **eXtensible Application Markup Language** (XAML) to specify components. In order to develop apps for the UWP, you should be running Windows 10 or Windows 11, and your Visual Studio IDE must include the **Universal Windows App Development Tools:**

![image](images/commonv.jpg)

Universal

![image](images/1v.jpg)Go to the Windows apps menu and launch the **Visual Studio Installer**

![image](images/pgb170_2.jpg)

![image](images/2v.jpg)Click the Installer’s **Modify** button to open the “Modifying” dialog

![image](images/pgb170_3.jpg)

![image](images/3v.jpg)Select the “Workloads” menu, then choose **Universal Windows Platform development**

![image](images/pgb170_4.jpg)

![image](images/4v.jpg)Click the dialog’s **Modify** button to download and install the UWP development workload components

![image](images/pgb170_5.jpg)

![image](images/5v.jpg)Click the **Launch** button to open the Visual Studio IDE

![image](images/pgb170_6.jpg)

![image](images/6v.jpg)Select the option to **Create a new project**

![image](images/pgb170_7.jpg)

![image](images/7v.jpg)Scroll down the list of project options and click the option to **Install Windows Universal tools for C++ development** to download the tools

![image](images/pgb170_8.jpg)

![image](images/snake.jpg)

The example in this chapter is described for Visual Studio 2022 on Windows 11 – the instructions may vary for other versions.

![image](images/forget.jpg)

Depending upon your choices when you installed Visual Studio, you may already have the Universal Windows App Development Tools.

![image](images/8v.jpg)Select **Create a new project** again and choose the **Blank App (Universal Windows - C++/CX)** project option

![image](images/pgb171_1.jpg)

![image](images/9v.jpg)Click **Next** to open a **Configure your new project** dialog, then name the project “Universal” and click **Create**

![image](images/pgb171_2.jpg)

![image](images/10v.jpg)When asked to select the target and minimal platform versions, simply click **OK** to accept the default options

![image](images/11v.jpg)After Visual Studio creates the new project, select **View, Solution Explorer** to examine the generated files:

•A set of logo images in an **Assets** folder.

•Internal XAML and C++ **App** files.

•XAML and C++ files for the **MainPage** – here is where you will create interface components and functional code.

•Other miscellaneous **Package** files.

![image](images/pgb171_3.jpg)

![image](images/snake.jpg)

Ensure that the Windows **Developer Mode** and **Device discovery** options are enabled in **Settings, Privacy & security, For developers.**

![image](images/forget.jpg)

These files are essential to all UWP apps using C++, and exist in every project Visual Studio creates to target the Universal Windows Platform with C++.

**Inserting page components**

Visual Studio provides a two-part window to insert interface components into a UWP app. This comprises a **Design** view of the components and a **XAML** view for the XAML code:

![image](images/commonv.jpg)

Universal

![image](images/1v.jpg)Open **Solution Explorer** then double-click on **MainPage.xaml** – to launch the two-part window

![image](images/pgb172_1.jpg)

![image](images/2v.jpg)See that by default, the **Design** view displays a blank canvas in **Landscape** mode

![image](images/pgb172_2.jpg)

There is a pop-out **Toolbox** feature that lets you add components onto the canvas, but you will need to edit them in the XAML code later. In this example, the components are created in XAML code from the very start.

![image](images/hot.jpg)

XAML is pronounced “zammel”.

![image](images/3v.jpg)Now, see that by default, the **XAML** view reveals there are **<Grid> </Grid>** tags – this is the root element of the canvas in which you can add component elements

![image](images/pgb173_1.jpg)

Component elements are best nested within a **<StackPanel>** element, as this can be given an **x:Name** for reference in functional code and an **Orientation** attribute to specify the direction in which the nested elements should appear. Common component elements include **<Image>**, **<TextBox>**, **<TextBlock>** (label), and **<Button>**. Several **<StackPanel>** elements can be nested within each other to determine the **Horizontal** and **Vertical** layout of components:

![image](images/4v.jpg)Insert elements between the root **<Grid> </Grid>** tags so the **XAML** view code looks precisely like this:

![image](images/pgb173_2.jpg)

![image](images/5v.jpg)As you add the component elements in **XAML** view, they appear in the **Design** view until it looks like this:

![image](images/pgb173_3.jpg)

![image](images/hot.jpg)

The outer **<StackPanel>** is a horizontal layout containing an **<Image>** and a nested **<Stackpanel>**. The nested **<StackPanel>** is a vertical layout containing two further **<StackPanel>** elements that each display their components horizontally. The **x:** prefix before the **Name** attribute refers to the XAML schema used by UWP apps. Notice that each **<TextBlock>** element has a **Text** attribute that can be referenced in functional code. For example, **textBlock1->Text**. references the text contained in the first TextBlock element.

**Importing program assets**

In order to have a XAML **<Image>** component display a graphic, an image file first needs to be added to the project’s **Assets** folder. It can then be assigned to a **Source** attribute of the **<Image>** tag:

![image](images/commonv.jpg)

Universal (continued)

![image](images/1v.jpg)Copy an image into the project’s Asset folder, typically at **C:\Users\*username*\source\repos\*project*\*project*\Assets**

![image](images/2v.jpg)Open **Solution Explorer**, then right-click on the **Assets** folder and choose **Add** from the context menu

![image](images/3v.jpg)Now, choose **Existing Item...** from the next context menu – to open an **Add Existing** Item dialog box

![image](images/pgb174_1.jpg)

![image](images/4v.jpg)In the **Add Existing Item** dialog, browse to the location of the image file and click the **Add** button

![image](images/pgb174_2.jpg)

![image](images/hot.jpg)

An image for display may be in any popular file format – such as **.bmp**, **.gif**, **.jpg**, **.png**, or **.tif**.

![image](images/5v.jpg)In **Solution Explorer**, the selected image file now appears in the project’s **Asset** folder

![image](images/pgb175_1.jpg)

![image](images/6v.jpg)Select the Image component in **Designer** view, then click **View**, **Properties** to reveal its properties

![image](images/pgb175_2.jpg)

![image](images/7v.jpg)In the **Properties** window, expand the **Common** category, then click the **Source** item’s arrow button and select the added image from the drop-down list

![image](images/8v.jpg)The image now appears in the **Design** view, and its path gets added to the **XAML** view code and **Source** property

![image](images/pgb175_3.jpg)

![image](images/pgb175_4.jpg)

![image](images/hot.jpg)

Explore the **Appearance** and **Transform** options in an image’s **Properties** window to discover how you can modify how it will be displayed.

**Designing the layout**

To complete the app’s layout, design attributes can be added to the XAML element tags to specify what they will display and precisely where in the interface they will appear:

![image](images/commonv.jpg)

Universal (continued)

![image](images/1v.jpg)Open **MainPage.xaml**, then add two attributes to the outer **<StackPanel>** element to fix its position **HorizontalAlignment = ”Left” VerticalAlignment = ”Top”**

![image](images/2v.jpg)Next, edit the **<Image>** element by modifying the initial assigned value of 200 – to increase its width

**Width = ”300”**

![image](images/3v.jpg)Now, add an attribute to the nested **<StackPanel>** element to fix its position

**VerticalAlignment = ”Center”**

![image](images/4v.jpg)Then, edit all six **<TextBlock>** elements alike, to specify their initial content, width, and margin on all four sides

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

![image](images/5v.jpg)Edit the first **<Button>** element to rename it, specify its button label content, and set its margin on all four sides

**x:Name = “BtnPick” Content = “Get My Lucky Numbers”**

**Margin = “15”**

![image](images/6v.jpg)Edit the second **<Button>** element to rename it and specify its button label content

**x:Name = “BtnReset” Content = “Reset”**

![image](images/7v.jpg)Finally, add an attribute to each respective **<Button>** element to specify their default state

**IsEnabled = “True”**

**IsEnabled = “True”**

![image](images/hot.jpg)

A single **Margin** value sets all four margins around that component. You can specify two values to set left & right, top & bottom margins; e.g. **Margin = “10,30”**. Alternatively, you can specify four values to set left,top,right,bottom margins individually; e.g. **Margin = “10,30,10,50”**

The order in which the attributes appear in each element is unimportant, but the elements within the **MainPage.xaml** file should now look similar to the screenshot below:

![image](images/pgb177_2.jpg)

![image](images/pgb177_1.jpg)

As you make changes to the **XAML** view code, the component layout gets changed accordingly in the **Design** view and should now look like this:

![image](images/pgb177_3.jpg)

![image](images/hot.jpg)

You can optionally add **Margin = “0”** attributes to explicitly require elements to have no margin width.

**Adding runtime function**

Having completed the application component layout with XAML elements [here](#chapter21.xhtml_rde), you are now ready to add functionality with C++ programming code:

![image](images/commonv.jpg)

Universal (continued)

![image](images/1v.jpg)In **Design** view, double-click on the **BtnPick** button

![image](images/2v.jpg)The **MainPage.xaml.cpp** code-behind page opens in the **Code Editor** at a generated **BtnPick_Click** event-handler

![image](images/3v.jpg)In the **BtnPick_Click** event-handler block, insert these statements to create a randomized array of integers between 1 and 59

**int i , j , k , seq[ 60 ] ;**

**srand( ( int ) time( 0 ) ) ;**

**for ( i = 1 ; i < 60 ; i++ ) seq[ i ] = i ;**

**for ( i = 1 ; i < 60 ; i++ )**

**{**

**j = ( ( int ) rand( ) % 59 ) + 1 ;**

**k = seq[ i ] ; seq[ i ] = seq[ j ] ; seq[ j ] = k ;**

**}**

**// Statements to be inserted here (Steps 4-5).**

![image](images/4v.jpg)Next, insert statements to assign six array element values to the **<TextBlock>** components

**textBlock1->Text = seq[ 1 ].ToString( ) ;**

**textBlock2->Text = seq[ 2 ].ToString( ) ;**

**textBlock3->Text = seq[ 3 ].ToString( ) ;**

**textBlock4->Text = seq[ 4 ].ToString( ) ;**

**textBlock5->Text = seq[ 5 ].ToString( ) ;**

**textBlock6->Text = seq[ 6 ].ToString( ) ;**

![image](images/5v.jpg)Next, insert statements to set the **<Button>** states

**BtnPick->IsEnabled = false ;**

**BtnReset->IsEnabled = true ;**

![image](images/6v.jpg)Return to **MainPage.xaml**, then in **Design** view, double-click on the **BtnReset** button

![image](images/7v.jpg)The **MainPage.xaml.cpp** code-behind page opens in the **Code Editor** at a generated **BtnReset_Click** event-handler

![image](images/hot.jpg)

The srand( ) function seeds a random number generator with the current system time, so subsequent calls to the rand( ) function return different pseudo-random numbers.

![image](images/forget.jpg)

There is no **Label** component in UWP apps; it is called a **TextBlock** instead.

![image](images/snake.jpg)

There is no **Enabled** property in UWP apps; it is called **IsEnabled** instead.

![image](images/8v.jpg)In the **BtnReset_Click** event-handler block, insert statements to assign strings to the **<TextBlock>** components

**textBlock1->Text = “...” ;**

**textBlock2->Text = “...” ;**

**textBlock3->Text = “...” ;**

**textBlock4->Text = “...” ;**

**textBlock5->Text = “...” ;**

**textBlock6->Text = “...” ;**

**// Statements to be inserted here (Step 9).**

![image](images/pgb179_1.jpg)

![image](images/9v.jpg)Finally, insert statements to set the **<Button>** states

**BtnPick->IsEnabled = true ;**

**BtnReset->IsEnabled = false ;**

The **MainPage.xaml.cpp** code-behind page should now look like the screenshot below:

![image](images/pgb179_2.jpg)

![image](images/10v.jpg)Return to the **MainPage.xaml** file, then in **XAML** view, see that attributes have been automatically added to the **<Button>** elements to call the event-handler code

![image](images/pgb179_3.jpg)

![image](images/forget.jpg)

The **BtnReset** button simply returns the **<TextBox>** and **<Button>** components to their original states.

![image](images/hot.jpg)

Notice that the first **for** loop contains only one statement to be executed on each iteration, so braces are not required.

**Testing the program**

Having added functionality with C++ code [here](#chapter21.xhtml_sec176), you are now ready to test the program:

![image](images/commonv.jpg)

Universal (continued)

![image](images/1v.jpg)On the Visual Studio standard toolbar, select the **Debug** for **x64** architecture and **Local Machine** options, then click the **Start** button to run the app with debugging enabled

![image](images/pgb180_1.jpg)

![image](images/2v.jpg)Wait while the application gets built and loaded, then click the buttons to try out their functionality

![image](images/pgb180_2.jpg)

![image](images/pgb180_3.jpg)

![image](images/pgb180_4.jpg)

The app looks good – numbers are being randomized and the button states are changing as required.

![image](images/3v.jpg)Now, on the Visual Studio standard toolbar, select **Debug**, **Stop Debugging** to exit the running program

![image](images/pgb180_5.jpg)

![image](images/forget.jpg)

You must have your PC set to **Developer Mode** in **Settings**, **Privacy & security**, **For developers**.

![image](images/4v.jpg)Click the **Start** button to restart the app, then click the buttons and compare the sequences of randomized numbers to those generated in the previous test

![image](images/pgb181_2.jpg)

![image](images/pgb181_3.jpg)

![image](images/pgb181_4.jpg)

![image](images/pgb181_1.jpg)

Great – the random number generator is seeded using the current time to ensure a different sequence each time the app gets run.

![image](images/5v.jpg)Drag the window edge to reduce its width, to simulate how the app would look on a narrower display area

![image](images/pgb181_5.jpg)

This is unsatisfactory – adjustments will be needed to the interface layout so it will adapt to suit narrower display areas.

![image](images/hot.jpg)

Test on the emulator with lowest memory and smallest screen and it should be fine running on those emulators with better features.

![image](images/snake.jpg)

Do not click the **X** button on the emulator window to stop the running program, as that will also close the emulator.

**Adjusting the interface**

The app test for narrow display areas [here](#chapter21.xhtml_lic) failed to satisfactorily present the controls, as the interface is too wide for smaller display areas. Happily, the interface can be made to adapt to different sizes so it can also look good on narrow display areas. The adaptation relies upon recognizing the display area size and changing the orientation of a <StackPanel> element in **XAML** for narrow display areas:

![image](images/commonv.jpg)

Universal (continued)

![image](images/1v.jpg)Open **MainPage.xaml**, then in **XAML** view add these elements immediately below the opening **<Grid>** element and before the component elements

**<VisualStateManager.VisualStateGroups>**

**<VisualStateGroup>**

**<!-- Elements to be inserted here (Steps 2-3) -->**

**</VisualStateGroup>**

**</VisualStateManager.VisualStateGroups>**

![image](images/2v.jpg)Next, insert elements to recognize wide screens

**<VisualState x:Name = “wideState” >**

**<VisualState.StateTriggers>**

**<AdaptiveTrigger MinWindowWidth = “641” />**

**</VisualState.StateTriggers>**

**</VisualState>**

![image](images/3v.jpg)Now, insert elements to recognize narrow screens and to change the **Orientation** of the outer **<StackPanel>**

**<VisualState x:Name = “narrowState” >**

**<VisualState.StateTriggers>**

**<AdaptiveTrigger MinWindowWidth = “0” />**

**</VisualState.StateTriggers>**

**<VisualState.Setters>**

**<Setter**

**Target = “MainStack.Orientation” Value = “Vertical” />**

**</VisualState.Setters>**

**</VisualState>**

![image](images/hot.jpg)

XAML code recognizes the same **<!-- -->** comment tags that are used in HTML code.

![image](images/forget.jpg)

Remember that the outer **<StackPanel>** in this app contains an **<Image>** and a nested **<StackPanel>** displayed horizontally, side-by-side. If displayed vertically, they should appear one above the other.

The beginning of the **MainPage.xaml** file should now look similar to the screenshot opposite, top:

![image](images/pgb183_2.jpg)

![image](images/pgb183_1.jpg)

![image](images/4v.jpg)Select **x64** and **Local Machine** then click Start to run the app once more – it still looks and functions well

![image](images/pgb183_3.jpg)

![image](images/5v.jpg)Now, drag the window edge to reduce its width, and see the interface adapt to suit a narrower screen

![image](images/pgb183_4.jpg)

![image](images/pgb183_5.jpg)

![image](images/pgb183_6.jpg)

![image](images/hot.jpg)

You can have Visual Studio nicely format the XAML code by pressing **Ctrl + K**, **Ctrl + D**.

![image](images/snake.jpg)

Although an app may work well in the Visual Studio emulator, it is recommended you always test on an actual device before deployment.

**Deploying the application**

Having tested the app [here](#chapter21.xhtml_img183), it can now be deployed onto your PC. This will register the app on your PC and add it to the **All apps** menu, so an icon image can usefully be added to the program files to identify the app:

![image](images/commonv.jpg)

Universal (continued)

![image](images/1v.jpg)Add a 400 x 400 pixel icon image into the project’s **Assets** folder on your PC

![image](images/2v.jpg)In **Solution Explorer**, right-click on the **Assets** folder and choose **Add, Existing Item** from the context menu and add the icon image

![image](images/3v.jpg)Next, double-click **Package.appxmanifest** and select the **Visual Assets tab** and **All Visual Assets** item

![image](images/pgb184_1.jpg)

![image](images/4v.jpg)Add the icon image as the **Source**, and click the **Generate** button to produce variously-sized tiles and logo images

![image](images/5v.jpg)Change the build type to **Release**, then click **Build**, **Deploy Solution** to register the app on your PC and see it get added to your PC’s **All apps** menu

![image](images/pgb184_2.jpg)

![image](images/pgb184_3.jpg)

An **App Package** can be created for deployment on other devices running Windows version 1809 or later:

![image](images/1v.jpg)Select **Release** on the toolbar

![image](images/pgb185_2.jpg)

![image](images/pgb185_1.jpg)

![image](images/2v.jpg)In **Solution Explorer**, right-click on the top-level **Universal** project folder, then choose **Publish, Create App Packages** from the context menu to launch a wizard

![image](images/3v.jpg)In the “Create App Packages” wizard, choose the **Sideloading** option, then click **Next**

![image](images/4v.jpg)Select a package signing certificate, then click **Next**

![image](images/5v.jpg)Choose a destination (e.g. a USB drive), version numbering, and architecture – then click **Create**

![image](images/pgb185_3.jpg)

The build creates a folder of several items, including an Application Package file (.msixbundle) and a Security Certificate (.cer) file.

![image](images/6v.jpg)Move the folder to another device, then right-click on the Security Certificate file and **Install** it in the Trusted Root Certification Authorities certificate store on that device

![image](images/7v.jpg)Finally, double-click the Application Package file to **Install** and **Launch** the app on that device

![image](images/pgb185_4.jpg)

![image](images/pgb185_5.jpg)

**Summary**

![image](images/pgb132_1.jpg)

•The **Universal Windows Platform** (UWP) enables a single app to run on any modern Windows-based device.

•The **eXtensible Application Markup Language** (XAML) is used to specify components and layout on UWP apps.

•The **Universal Windows App Development Tools** are needed in order to develop UWP apps.

•The **Blank App (Universal Windows)** template can be used to create a new UWP project.

•Visual Studio provides a graphical **Design** view and a text code **XAML** view for the **MainPage.xaml** file.

•Component elements can be placed within XAML **<StackPanel>** elements to arrange their orientation.

•Image files can be added to the **Assets** folder and assigned to XAML **<Image>** elements for display on the interface.

•Space can be added around a component by adding a **Margin** attribute and assigned value within its element tag.

•Functional C++ programming code can be added to the **MainPage.xaml.cpp** code-behind page.

•The **Developer Mode** setting must be enabled in the Windows settings in order to develop and test UWP apps.

•A UWP app can be tested in **Debug** mode on the **Local Machine**.

•The interface of a UWP app can adapt to different screen sizes by changing the orientation of **<StackPanel>** elements.

•Image files can be added to the **Assets** folder for assignment as logos in the **Package.appxmanifest** window.

•A **Release** version can be deployed on the Local Machine PC using the **Build, Deploy Solution** menu.

•A **Release** version can be deployed on other modern Windows devices using the **Publish, Create App Packages** wizard.

**22**

**Getting started with C#**

***Welcome to the exciting world of C# programming. This chapter introduces the Visual Studio Integrated Development Environment and shows you how to create a real Windows application.***

[**Introducing C#**](#chapter22.xhtml_sec181)

[**Installing Visual Studio**](#chapter22.xhtml_sec182)

[**Exploring the IDE**](#chapter22.xhtml_sec183)

[**Starting a Console project**](#chapter22.xhtml_sec184)

[**Running a Console project**](#chapter22.xhtml_sec185)

[**Following the rules**](#chapter22.xhtml_sec186)

[**Summary**](#chapter22.xhtml_sec187)

**Introducing C#**

The introduction of the Microsoft .NET framework at the Professional Developers Conference in July 2000 also saw Microsoft introduce a new programming language called C# (pronounced “see-sharp”). The name was inspired by musical notation where a # sharp symbol indicates that a written note should be a semitone higher in pitch. This notion is similar to the naming of the C++ programming language where the ++ symbol indicates that a written value should be incremented by 1.

![image](images/pgc8_1.jpg)

•C# is designed to be a simple, modern, general-purpose, object-oriented programming language, borrowing key concepts from several other languages – most notably the Java programming language. Consequently, everything in C# is a class “object” with “properties” and “methods” that can be employed by a program.

•C# is an elegant and “type-safe” programming language that enables developers to build a variety of secure and robust applications. You can use C# to create Windows client applications, XML web services, distributed components, client-server applications, database applications, and much, much more.

•C# is specifically designed to utilize the proven functionality built into the .NET framework “class libraries”. Windows applications written in C# therefore require the Microsoft .NET framework to be installed on the computer running the application – typically, an integral component of the system.

**The Microsoft .NET Framework**

Each version of the Microsoft .NET framework includes a unified set of class libraries and a virtual execution system called the Common Language Runtime (CLR). The CLR allows the C# language and the class libraries to work together seamlessly.

![image](images/pgc8_2.jpg)

To create an executable program, source code written in the C# language is compiled by the C# Compiler into Intermediate Language (IL) code. This is stored on disk, together with other program resources such as images, in an “assembly”. Typically, the assembly will have a file extension of .exe or .dll. Each assembly contains a “manifest” that provides information about that program’s security requirements.

When a C# program is executed, the assembly is loaded into the Common Language Runtime (CLR), and the security requirements specified in its assembly manifest are examined. When the security requirements are satisfied, the CLR performs Just-In-Time (JIT) compilation of the IL code into native machine instructions. The CLR then performs “garbage collection”, exception handling, and resource management tasks before calling upon the operating system to execute the program:

![image](images/pgc9_1.jpg)

As language interoperability is a key feature of the Microsoft .NET framework, the IL code generated by the C# Compiler can interact with code generated by the .NET versions of other languages such as Visual Basic and Visual C++. The examples throughout the C# section of this book demonstrate Visual C# program code.

![image](images/hot.jpg)

Just-In-Time compilation is also known as “Dynamic Translation”.

![image](images/forget.jpg)

Just-In-Time compilation occurs during program execution, rather than prior to its execution.

**Installing Visual Studio**

In order to create Windows applications with the C# programming language, you will first need to install a Visual Studio Integrated Development Environment (IDE).

![image](images/pgc10_1.jpg)

Microsoft Visual Studio is the professional development tool that provides a fully Integrated Development Environment for Visual Basic, Visual C++, Visual J#, and Visual C#. Within its IDE, code can be written in Visual Basic, C++, J#, or the C# programming language to create Windows applications.

Visual Studio Community edition is a streamlined version of Visual Studio, specially created for those people learning programming. It has a simplified user interface and omits advanced features of the professional edition to avoid confusion. C# code can be written within the **Code Editor** of either version of the Visual Studio IDE to create Windows applications.

Both Visual Studio and Visual Studio Community provide an IDE for C# programming but, unlike the fully-featured Visual Studio product, the Visual Studio Community edition is completely free and can be installed on any system meeting the following minimum requirements:

| **Component** | **Requirement** |
| Operating system | Windows 11 Windows 10 (version 1909 or higher)
Windows Server 2016 or 2019
*Must be the 64-bit version of any of the above the operating systems. |
| CPU (processor) | 1.8 GHz or faster, 64-bit processor |
| RAM (memory) | 4 GB (16 GB recommended) |
| HDD (hard drive) | Up to 210 GB available space |
| Video Card | Minimum resolution of 1366 x 768 Optimum resolution of 1920 x 1080 |

The Visual Studio Community edition is used throughout the C# section of this book to demonstrate programming with the C# language, but the examples can also be recreated in Visual Studio. Follow the steps opposite to install the Visual Studio Community edition.

![image](images/1b.jpg)Open your web browser and navigate to the Visual Studio download page – at the time of writing, this can be found at **[visualstudio.microsoft.com/downloads](http://www.visualstudio.microsoft.com/downloads)**

![image](images/pgc11_1.jpg)

![image](images/2b.jpg)Click the button in the Community edition section to download a **VisualStudioSetup.exe** setup file

![image](images/3b.jpg)Click on the ![image](images/pgc11_2.jpg) setup file icon to begin setup and to run the **Visual Studio Installer**

![image](images/4b.jpg)Accept the suggested installation location, then click **Next**

![image](images/5b.jpg)Check the two C# **Installer** options shown below

![image](images/pgc11_3.jpg)

![image](images/6b.jpg)Click the **Install** button at the bottom-right of the installer to begin the download and installation process

![image](images/snake.jpg)

Choosing a different destination folder may require other paths to be adjusted later – it’s simpler to just accept the suggested default.

![image](images/hot.jpg)

Both **Visual Studio** and **Visual Studio Installer** items get added to your **All Apps** menu. You can re-run the installer at a later date to add or remove features.

**Exploring the IDE**

![image](images/pgc12_1.jpg)

![image](images/1b.jpg)Go to your **All apps** menu, then select the Visual Studio 2022 menu item added there by the installer:

![image](images/pgc12_2.jpg)

![image](images/2b.jpg)Sign in with your Microsoft account, or register an account then sign in, to continue

![image](images/3b.jpg)See a default **Start Page** appear where recent projects will be listed alongside several “Get started” options

![image](images/pgc12_3.jpg)

![image](images/hot.jpg)

In the future your recent projects will be listed here so you can easily reopen them.

![image](images/4b.jpg)For now, just click the **Continue without code** link to launch the Visual Studio application

The Visual Studio Integrated Development Environment (IDE) appears, from which you have instant access to everything needed to produce complete Windows applications – from here, you can create exciting visual interfaces, enter code, compile and execute applications, debug errors, and much more.

![image](images/pgc12_4.jpg)

![image](images/snake.jpg)

The first time Visual Studio starts it takes a few minutes as it performs configuration routines.

![image](images/pgc13_1.jpg)

**Visual Studio IDE components**

The Visual Studio IDE initially provides these standard features:

•**Menu Bar** – Where you can select actions to perform on all your project files and to access Help. When a project is open, extra menus of Project and Build are shown in addition to the default menu selection of File, Edit, View, Git, Project, Debug, Analyze, Tools, Extensions, Window, and Help.

•**Toolbar** – Where you can perform the most popular menu actions with a single click on their associated shortcut icons.

•**Toolbox** – Where you can select visual elements to add to a project. Click View, Toolbox or a side bar button to see its contents. When a project is open, “controls” such as Button, Label, CheckBox, RadioButton, and TextBox are shown here.

•**Solution Explorer** – Where you can see at a glance all the files and resource components contained within an open project.

•**Status Bar** – Where you can read the state of the current activity being undertaken. When building an application, a “Build started” message is displayed here, changing to a “Build succeeded” or “Build failed” message upon completion.

![image](images/hot.jpg)

The IDE may have a **Light** color theme by default. To change the color theme, choose the **Tools**, **Options** menu then select **Environment**, **General**, **Color Theme** and select **Blue** or **Dark** theme, or select the **Use system** **setting** option.

**Starting a Console project**

![image](images/commonb.jpg)

GettingStarted

![image](images/1b.jpg)On the Menu Bar, click **File**, **New**, **Project...** or press **Ctrl** + **Shift** + **N**, to open the “Create a new project” dialog

![image](images/pgc14_1.jpg)

![image](images/2b.jpg)In the “Create a new project” dialog box, select the **C# Console App** item (for .NET Core on Windows, Linux and macOS), then click **Next**

![image](images/pgc14_2.jpg)

![image](images/3b.jpg)In the next dialog, enter a project name plus location and click the **Create** button, then select the .NET 6.0 (Long-term support) framework and click **Create** again

![image](images/pgc14_3.jpg)

Visual Studio now creates your new project and loads it into the IDE. A **Code Editor** window appears, containing default skeleton project code generated by Visual Studio.

![image](images/4b.jpg)Drag the **Code Editor** window tab to undock the **Code Editor** window from the Visual Studio IDE frame

![image](images/hot.jpg)

The source code of all examples in this book is available for free download at **[www.ineasysteps.com/downloads](http://www.ineasysteps.com/downloads)**

![image](images/hot.jpg)

The default location for Visual Studio projects is a **C:\Users\*username*\source\repos** directory.

![image](images/hot.jpg)

If the **Code Editor** window does not open automatically, click the **Program.cs** file icon in Solution Explorer to open the **Code Editor**.

The undocked window title displays the project name, and the tab displays the file name of the code as “Program.cs”.

![image](images/pgc15_1.jpg)

The top-left drop-down box indicates the name of the project to which this file belongs – in this case, it’s “GettingStarted”.

![image](images/5b.jpg)Select the **View**, **Solution** **Explorer** menu to open a **Solution Explorer** window, to discover all the items in your project – click the arrow buttons to expand or collapse categories

![image](images/pgc15_2.jpg)

![image](images/6b.jpg)Select the **View**, **Properties Window** menu to open a **Properties** window, then select any item in the **Solution** **Explorer** window to see its properties then appear in the **Properties** window

![image](images/pgc15_3.jpg)

The **Code Editor** window is where you write C# code to create an application. The Visual Studio IDE has now gathered all the resources needed to build a default Console application.

![image](images/hot.jpg)

You can drag the title bar of any window to undock that window from the Visual Studio IDE frame. When dragging, you can drop a window on the “guide diamond” (shown below) to dock the window in your preferred position.

![image](images/pgc15_4.jpg)

**Running a Console project**

In order to run a program, Visual Studio will first build the app then execute the app. This can be done in one of two modes:

•**Debug Mode** – The program is compiled with symbolic debugging information included in the program files. This allows Visual Studio’s built-in debugger to find bugs, but has optimization of Intermediate Language (IL) code disabled.

•**Release Mode** – The program is compiled without debugging information included in the program files, but has optimization of Intermediate Language (IL) code enabled.

![image](images/commonb.jpg)

GettingStarted (continued)

During program development it is generally preferable to run your programs in Debug mode. There is an option to run a program in Debug mode without debugging, but it’s seldom desirable as this executes the program without the possibility of stepping through the code to breakpoints.

![image](images/1b.jpg)On the toolbar, set the solution configuration to **Debug**

![image](images/pgc16_1.jpg)

![image](images/2b.jpg)Now, click the green arrow “**Start**” button to build and run the program with debugging enabled

![image](images/pgc16_2.jpg)

![image](images/3b.jpg)See the app display a traditional greeting in the Console

![image](images/pgc16_3.jpg)

![image](images/4b.jpg)Press any keyboard key to close the Console window, and return to the Visual Studio **Code Editor**

![image](images/pgc17_1.jpg)

![image](images/hot.jpg)

You will discover how to use breakpoints in [Chapter 29](#chapter29.xhtml) (Solving problems).

![image](images/hot.jpg)

Alternatively, select **Debug**, **Start** **Debugging** to build and run a program with debugging enabled.

![image](images/pgc16_4.jpg)

![image](images/hot.jpg)

New in .NET 6 are code templates, which the compiler uses to automatically generate namespace, class, and method elements when building a Console app.

**Code analysis**

Examination of the code helps to understand what is happening:

•The first line is a comment. Anything on a line after **//** is ignored by the compiler. By default, comments are colored green in the Visual Studio **Code Editor**. In this case, the comment includes a hyperlink that will open a page in your web browser. The page explains how the .NET 6 framework uses new templates to simplify the creation of Console apps.

•Console.WriteLine( “Hello, World!” ) ; This is a statement that calls upon the WriteLine( ) method of the Console class to output the text string enclosed in quote marks within its parentheses. Notice that the statement is terminated by a ; semicolon character. By default, class names are colored light blue, method names are colored brown, strings are colored red, and other code here is colored black.

![image](images/5b.jpg)Add another line to the code, as a statement to output a second text string containing your own name such as...

**Console.WriteLine( “Good afternoon, Mike!” ) ;**

![image](images/6b.jpg)Run the modified code in Debug mode to see the result

![image](images/pgc17_2.jpg)

![image](images/hot.jpg)

To edit the default Console window colors and font, right-click its window Titlebar and choose **Properties**. For clarity, all other Console window screenshots in the C# section of this book feature Lucida Console 14-pixel **Font** in black **Screen Text** on a white **Screen Background**.

**Following the rules**

![image](images/pgc18_1.jpg)

As with all programming languages, C# has a number of syntax rules that must be precisely followed to ensure the code is correctly formatted for the C# compiler to clearly understand:

•**Case-sensitivity** – C# is a case-sensitive language, which means that uppercase “A” and lowercase “a” are regarded as totally different items.

•**Termination** – All statements in C# language must be terminated by a ; semicolon character, just as all sentences in English language must be terminated by a . period character. – for example: Console.WriteLine( “Hello World!” ) ;

•**Single-line comments** – Brief comments on a single line must begin with **//** two forward slash characters – for example: // Output the traditional greeting.

•**Block comments** – Extended comments on multiple lines must begin with /* forward slash and asterisk characters, and must end with the reverse */ asterisk and forward slash – for example:

**/***

C# Programming in easy steps.

Getting started with the traditional greeting.

***/**

•**White space** – Spaces, tabs, newline characters, and comments are ignored by the C# compiler, so can be used extensively to organize code without performance penalty.

•**Escape sequences** – The C# compiler recognizes **\n** as a newline character and \t as a tab character, so these can be used to format output –

for example: Console.WriteLine(“Line One \n Line Two”) ;

•**Naming conventions** – A programmer-defined identifier name in C# code may begin with an **_** underscore character or a letter in uppercase or lowercase. The name may also contain underscore, letter, and number characters – for example: class MyNo1_Class

•**Keywords** – The C# language has a number of keywords (listed opposite) that have special syntactic meaning and may not be used to name programmer-defined items in code.

![image](images/hot.jpg)

It is recommended that you comment your code to make it readily understood by others or when revisiting your own code later.

![image](images/forget.jpg)

The **WriteLine( )** method automatically adds a newline after its output.

| **C# Reserved Keywords** |
| **abstract** | **as** | **base** | **bool** |
| **break** | **byte** | **case** | **catch** |
| **char** | **checked** | **class** | **const** |
| **continue** | **decimal** | **default** | **delegate** |
| **do** | **double** | **else** | **enum** |
| **event** | **explicit** | **extern** | **false** |
| **finally** | **fixed** | **float** | **for** |
| **foreach** | **goto** | **if** | **implicit** |
| **in** | **int** | **interface** | **internal** |
| **is** | **lock** | **long** | **namespace** |
| **new** | **null** | **object** | **operator** |
| **out** | **override** | **params** | **private** |
| **protected** | **public** | **readonly** | **ref** |
| **return** | **sbyte** | **sealed** | **short** |
| **sizeof** | **stackalloc** | **static** | **string** |
| **struct** | **switch** | **this** | **throw** |
| **true** | **try** | **typeof** | **uint** |
| **ulong** | **unchecked** | **unsafe** | **ushort** |
| **using** | **virtual** | **void** | **volatile** |
| **while** |  |  |  |

| **C# Contextual Keywords** |
| **add** | **and** | **alias** | **ascending** | **async** |
| **await** | **by** | **descending** | **dynamic** | **equals** |
| **from** | **get** | **global** | **group** | **init** |
| **into** | **join** | **let** | **managed** | **nameof** |
| **nint** | **not** | **notnull** | **nuint** | **on** |
| **or** | **orderby** | **partial** | **record** | **remove** |
| **select** | **set** | **unmanaged** | **value** | **var** |
| **when** | **where** | **with** | **yield** |  |

![image](images/hot.jpg)

If you absolutely must use a keyword to name a programmer defined element, it may be prefixed by an **@** character to distinguish it from the keyword – but this is best avoided.

![image](images/forget.jpg)

Contextual keywords have special significance in certain code – for example, **get** and **set** in method declarations.

**Summary**

![image](images/pgc20_1.jpg)

•**C#** is an object-oriented programming language that utilizes the proven functionality of the Microsoft **.NET** class libraries.

•The C# compiler generates **Intermediate Language (IL)** code that is stored on disk alongside resources in an assembly.

•The **Common Language Runtime (CLR)** examines an assembly’s security requirements before JIT compilation.

•**Just-In-Time** compilation translates IL code into native machine code for execution by the operating system.

•Microsoft Visual Studio provides a fully **Integrated Development Environment (IDE)** for C# programming.

•A new Visual C# **Console** application generates default skeleton project code in the Visual Studio **Code Editor**.

•The Visual Studio **Solution Explorer** shows all files in a project, and the **Properties** window shows their properties.

•The default C# skeleton code provided in the **Code Editor** can create a C# Console program that outputs a text string.

•The Console class has a WriteLine( ) method that can be used to output a quoted text string specified within its parentheses.

•A C# program can be run in the Visual Studio IDE by selecting the **Debug**, **Start Debugging** menu, or by setting a **Debug** solution configuration and clicking the **Start** button.

•C# is a case-sensitive programming language in which all statements must be terminated by a ; semicolon character.

•Single-line // comments and /* */ block comments can be incorporated to explain C# program code.

•C# has keywords that have special syntactic meaning, so cannot be used to name programmer-defined code items.

**23**

**Storing values**

***This chapter demonstrates how to store various types of data within a C# program.***

[**Creating variables**](#chapter23.xhtml_sec188)

[**Reading input**](#chapter23.xhtml_sec189)

[**Employing arrays**](#chapter23.xhtml_sec190)

[**Casting data types**](#chapter23.xhtml_sec191)

[**Fixing constants**](#chapter23.xhtml_sec192)

[**Summary**](#chapter23.xhtml_sec193)

Creating variables

A “variable” is like a container in a C# program in which a data value can be stored inside the computer’s memory. The stored value can be referenced using the variable’s name.

![image](images/pgc22_1.jpg)

The programmer can choose any name for a variable, providing it adheres to the C# naming conventions – a chosen name may only contain letters, numbers, and the underscore character, but must begin with a letter, underscore, or @ character. Also, the C# keywords must be avoided. It’s good practice to choose meaningful names to make the code more comprehensible.

To create a new variable in a program it must be “declared”, specifying the type of data it may contain and its chosen name. A variable declaration has this syntax:

*data-type variable-name ;*

Multiple variables of the same data type can be created in a single declaration as a comma-separated list with this syntax:

*data-type variable-name1 , variable-name2 , variable-name3 ;*

The most common C# data types are listed in the table below, together with a brief description and example content:

| **Data Type** | **Description** |
| **int** | An integer whole number, e.g. **100** |
| **char** | A single character, e.g. **‘A’** |
| **float** | A floating-point number of 7-digit precision |
| **double** | A floating-point number of 15-digit precision |
| **decimal** | A floating-point number of 28-digit precision |
| **bool** | A Boolean value of **true** or **false** |
| **string** | A string of characters, e.g. **“In Easy Steps”** |

Variable declarations must appear before statements that use them – so they will be available for reference within statements.

![image](images/snake.jpg)

Names are case-sensitive in C# – so variables named **num**, **Num**, and **NUM** are treated as three individual variables. Traditionally, C# variable names are created in all lowercase characters.

![image](images/snake.jpg)

Character values of the **char** data type must be enclosed in single quotes, but character strings of the **string** data type must be enclosed between double quotes.

![image](images/hot.jpg)

The **decimal** data type is preferred for storage of monetary values.

When a value is assigned to a variable it is said to have been “initialized”. Optionally, a variable may be initialized in its declaration. The value stored in any initialized variable can be displayed using the WriteLine( ) method, which was used [here](#chapter22.xhtml_sec185) to display the “Hello World!” greeting:

![image](images/commonr.jpg)

Variables

![image](images/1r.jpg)Open the Visual Studio IDE, then start a new **C# Console App** project and name it “Variables”

![image](images/2r.jpg)Remove the default skeleton code, then type this code to name the Console window

**Console.Title = “Variables” ;**

![image](images/3r.jpg)Next, precisely type these statements to declare and initialize variables of common C# data types

**char letter ;     letter = ‘A’ ;               // Declared then initialized.**

**int number ;    number = 100 ;         // Declared then initialized.**

**float body = 98.6f ;                           // Declared and initialized.**

**double pi = 3.14159 ;                       // Declared and initialized.**

**decimal sum = 1000.00m ;              // Declared and initialized.**

**bool flag = false ;                            // Declared and initialized.**

**string text = “C# Is Fun” ;              // Declared and initialized.**

![image](images/4r.jpg)Now, insert statements to display each stored value

**Console.WriteLine( “char letter:\t” + letter ) ;**

**Console.WriteLine( “int number:\t” + number ) ;**

**Console.WriteLine( “float body:\t” + body ) ;**

**Console.WriteLine( “double pi:\t” + pi ) ;**

**Console.WriteLine( “decimal sum:\t” + sum ) ;**

**Console.WriteLine( “bool flag:\t” + flag ) ;**

**Console.WriteLine( “string text:\t” + text ) ;**

**Console.ReadKey( ) ;**

![image](images/5r.jpg)Press **Start** to run the application in Debug mode and see the values stored inside variables

![image](images/pgc23_1.jpg)

![image](images/forget.jpg)

Suffix **f** to a **float** value and **m** to a **decimal** value to distinguish them from a **double** value.

![image](images/hot.jpg)

The **\t** in the string is an “escape sequence” that prints a tab in the output. The **+** symbol is a “concatenation” operator, which adds a stored value to the string.

![image](images/forget.jpg)

Calling the **Readkey( )** method is a little trick to keep the Console window open when the app is published, until the user presses any key.

**Reading input**

In order to interact with the user, C# programs will typically require the user to input some values. The ReadLine( ) method – a companion to the ReadKey( ) method – can be used to read user input. User input within the Console can be assigned to a string data type variable by the ReadLine( ) method when the user hits **Enter** to complete a line.

![image](images/pgc24_1.jpg)

When requesting user input, it’s preferable to prompt the user without adding a newline after the request. This is easily achieved using the Console.Write( ) method:

![image](images/commonr.jpg)

Input

![image](images/1r.jpg)Open the Visual Studio IDE, then start a new **C# Console App** project and name it “Input”

![image](images/2r.jpg)Remove the default skeleton code, then type this code to name the Console window

**Console.Title = “Input” ;**

![image](images/3r.jpg)Next, precisely type these statements to request user input for assignment to a variable

**Console.Write( “Please Enter Your Name: “ ) ;**

**string name = Console.ReadLine( ) ;**

![image](images/4r.jpg)Now, add statements to display a message containing the stored user input value

**Console.WriteLine( “Welcome ” + name + “!” ) ;**

**Console.ReadKey( ) ;**

![image](images/5r.jpg)Press **Start** or **F5** to run the application and see the stored user input value displayed in output

![image](images/pgc24_2.jpg)

Numerical values input by the user are assigned to the string variable as characters – so arithmetic cannot be performed on these.

![image](images/snake.jpg)

It is important to recognize that the **ReadLine( )** method always reads input as a **string** value.

![image](images/hot.jpg)

Notice how two **+** concatenation operators are used here to insert input into a string.

When you require the user to input numerical values it is necessary to convert the string values read by the ReadLine( ) method into numerical data types. The System.Convert class provides a number of useful methods for this purpose, including:

| **Method** | **Returns** |
| **Convert.ToInt32( )** | A 32-bit signed integer |
| **Convert.ToDouble( )** | A floating-point precision number |
| **Convert.ToDecimal( )** | A decimal precision number |

The string value read by the ReadLine( ) method needs simply to be specified within the parentheses of the appropriate method:

![image](images/commonr.jpg)

Conversion

![image](images/1r.jpg)Start a new **C# Console App** and name it “Conversion”

**Console.Title = “Conversion” ;**

![image](images/2r.jpg)Type these statements to request user input for conversion and assignment to two variables

**Console.Write( “Please Enter A Number: “ ) ;**

**double num = Convert.ToDouble( Console.ReadLine( ) ) ;
Console.Write( “Now Enter Another Number: “ ) ;**

**double sum=**

**num + Convert.ToDouble( Console.ReadLine( ) ) ;**

![image](images/3r.jpg)Now, add statements to display a message containing the sum total of the user input values

**Console.WriteLine( “Total = ” + sum ) ;**

**Console.ReadKey( ) ;**

![image](images/4r.jpg)Press **Start** or **F5** to run the application, then enter two values to see the converted input added in output

![image](images/pgc25_1.jpg)

![image](images/hot.jpg)

There is also a useful **Convert.ToString( )** method to translate values to **string** type.

![image](images/forget.jpg)

Here, the second input number gets converted to a numerical value before addition to the first input number.

**Employing arrays**

An array is a variable that can store multiple items of data – unlike a regular variable, which can only store one piece of data. The pieces of data are stored sequentially in array “elements” that are numbered, starting at zero. So, the first value is stored in element 0, the second value is stored in element 1, and so on.

![image](images/pgc26_1.jpg)

An array is declared by stating the data type, suffixed by **[ ]** square brackets to denote an array. This alone does not initialize the array variable in memory until an array “instance” is created by specifying an element size using the **new** keyword, like this:

*data-type* [ ] *array-name* = new *data-type*[ *size* ] ;

Values can then be individually assigned to each available element:

*array-name*[ *element-number* ] = *value* ;

Alternatively, an array can be initialized and values assigned to each element when it is declared by stating values for each element in a comma-separated list, grouped within braces:

*data-type* [ ] *array-name* =

**new *data-type*[ *size* ] { *value , value , value* } ;**

Any individual element’s value can be referenced using the array name followed by square brackets containing the element number – for example, to reference the value within the first element:

***array-name*[ 0 ]**

Collectively, the elements of an array are known as an “index”. Arrays can have more than one index – to represent multiple dimensions, rather than the single dimension of a regular array. Multi-dimensional arrays of three indices and more are uncommon, but two-dimensional arrays are useful to store grid-based information such as coordinates.

To create a multi-dimensional array, the **[ ]** square brackets following the data type in the declaration must contain a comma for each additional index. Similarly, the size of each index must be specified as a comma-separated list, like this:

***data-type* [ , ] *array-name* = new *data-type*[ *size , size* ] ;**

Values can then be individually assigned to each available element:

***array-name*[ *element-number , element-number* ] = *value* ;**

![image](images/forget.jpg)

Array numbering starts at zero – so the final element in an array of six elements is number 5, not number 6\. This numbering is known as a “zero-based index”.

![image](images/snake.jpg)

You can only store within array elements data of the type specified in the array declaration.

![image](images/hot.jpg)

A special **foreach** loop construct allows you to easily iterate through all elements of an array – see [here](#chapter25.xhtml_sec205) for details.

Alternatively, a multi-dimensional array can be initialized when it is declared by stating values for each index in a comma-separated list, grouped within braces – in a comma-separated group enclosed within braces:

***data-type* [ , ] *array-name* = new *data-type*[ *sizeX , sizeY* ]**

**{ { *value , value , value* } , { *value , value , value* } } ;**

Any individual element’s value can be referenced using the array name followed by square brackets containing the element number for each index – for example, to reference the value within the first element of the second index:

***array-name*[ 1 , 0 ]**

![image](images/commonr.jpg)

Arrays

![image](images/1r.jpg)Start a new **C# Console App** and name it “Arrays”

**Console.Title = “Arrays” ;**

![image](images/2r.jpg)Next, type this statement to create a string array

**string [ ] cars = new string[ 3 ] { “BMW”, ”Ford”, ”Opel” } ;**

![image](images/3r.jpg)Now, type this statement to create a 2-dimensional array

**int [ , ] coords = new int[ 2, 3 ] { { 1, 2, 3 } , { 4, 5, 6 } } ;**

![image](images/pgc27_1.jpg)

![image](images/4r.jpg)Add statements to display output containing the stored array element values

**Console.WriteLine( “Second Car: ” + cars[ 1 ] ) ;**

**Console.WriteLine( “X1,Y1: ” + coords[ 0, 0 ] ) ;**

**Console.WriteLine( “X2,Y3: ” + coords[ 1, 2 ] ) ;**

**Console.ReadKey( ) ;**

![image](images/5r.jpg)Press **Start** or **F5** to run the application and see the values stored within array elements

![image](images/pgc27_3.jpg)

![image](images/snake.jpg)

The number of specified values must exactly match the specified array size to avoid an error.

**Casting data types**

A value stored in a variable can be forced (coerced) into a variable of a different data type by converting the value to a different type. This process is known as “casting”, and may be implicit or explicit.

![image](images/pgc28_1.jpg)

•**Implicit** casting is automatically performed by C# in a type-safe manner when converting numbers from smaller to larger precision data types. For example, when adding an **int** to a **double**, the **int** value is automatically converted to a **double**.

•**Explicit** casting, on the other hand, requires a cast operator to be included in a statement to specify the data type to which the value should be cast. The required new data type must be specified in parentheses preceding the name of the variable containing the data to be cast, so its syntax looks like this:

***variable-name* = ( *data-type* ) *variable-name* ;**

This is the traditional form of casting that is also found in the C programming language. Casting is often necessary to accurately store the result of an arithmetic operation to prevent data loss. Division of one integer by another integer will always produce an integer result, which may be truncated. For example, the integer division **7/2** produces the truncated integer result of **3**.

To store the accurate floating-point result would require the result be cast into a suitable data type, such as a **double**, like this:

**double sum = ( double ) 7 / 2 ;           // sum = 3.5**

It should be noted that operator precedence casts the first operand 7 into the specified data type before implementing the arithmetic operation **/2** division, so effectively the statement is:

**double sum = ( double ) ( 7 ) / 2 ;           // sum = 3.5**

Bracketing the expression as ( 7 / 2 ) would perform the arithmetic first on integers, so the integer result would be truncated before being cast into the float variable – not the desired effect!

**double sum = ( double ) ( 7 / 2 ) ;           // sum = 3.0**

Single character values can usefully be explicitly cast to an **int** data type to reveal their Unicode code value. Similarly, the process can be reversed to reveal the character value of an integer.

![image](images/hot.jpg)

Casting is also known as “type conversion”.

![image](images/forget.jpg)

The result of dividing an integer by another integer is truncated, not rounded – so a result of 9.9 would become 9.

![image](images/commonr.jpg)

Cast

![image](images/1r.jpg)Start a new **C# Console App** and name it “Cast”

**Console.Title = “Cast” ;**

![image](images/2r.jpg)Type these statements to create and initialize a double-precision floating-point variable and an integer variable

**double num = 10.5 ;**

**int integer = 2 ;**

![image](images/3r.jpg)Next, add statements to implicitly cast the integer value into a double-precision value, and display the result

**num = num + integer ;**

**Console.WriteLine( “Implicit Cast: ” + num ) ;**

![image](images/4r.jpg)Now, explicitly cast the result of an integer division into a double-precision value, and display that result

**num = ( double ) 7 / integer ;**

**Console.WriteLine( “Explicit Cast: ” + num ) ;**

![image](images/5r.jpg)Cast an integer value into a char data type and display its Unicode equivalent character

**char letter = ( char ) 65 ;**

**Console.WriteLine( “Cast Integer: ” + letter ) ;**

![image](images/6r.jpg)Cast a character value into an **int** data type and display its Unicode equivalent code number

**int unicode = ( int ) ‘A’ ;**

**Console.WriteLine( “Cast Letter: ” + unicode ) ;
Console.ReadKey( ) ;**

![image](images/7r.jpg)Press **Start** or **F5** to run the application and see the values cast into other data types

![image](images/pgc29_1.jpg)

![image](images/hot.jpg)

Remove the **( double** ) cast from Step 4 to see the result become truncated.

**Fixing constants**

Variable declarations explicitly specify their permissible data type using keywords such as string, int, or double to ensure the program cannot accidentally assign inappropriate data. Where you are certain this will never occur, you may use the var (variant) keyword when declaring a variable, to implicitly specify its data type according to the data type of its initial value. In this case, the C# compiler will automatically determine the appropriate data type. The var keyword is most useful to store a value that is other than of the standard C# numerical, Boolean, or string data types. All variable declarations made using the var keyword must assign an initial value to immediately determine that variable’s data type.

![image](images/pgc30_1.jpg)

The data type of any variable can be revealed by dot-suffixing the GetType( ) method onto the variable name. For example, where a num variable is a double data type, calling num.GetType( ) will return a System.Double result.

When a stored value is never intended to be changed, a “constant” container can be created to safeguard it from change. Its declaration is similar to that of a variable, but begins with the const keyword. Each declaration made using the const keyword must assign an initial value to immediately fix its constant value.

Multiple constant values can be defined in an enumerator list using the enum keyword and a specified identifier name. This creates a data type that consists of a comma-separated list of named constants within { } braces. The enumerator list has an underlying default int value that numbers the list names from zero, much like the elements in an array. Any name within the list can be referenced by dot-suffixing it to the list name, and its underlying index number revealed by casting.

The C# **Enum** class provides several methods to work with enumerator lists. Many of these require the data type of the list as an argument, so this can usefully be assigned to a var variable by specifying the list name as an argument to the typeof( ) method. The **Enum** class GetName( ) method can reveal the name at a specified index position, and the IsDefined( ) method can be used to test whether the list contains a specified name. An enumerator list declaration can be written in its own code file, or after all other “top-level” statements in the main “Program.cs” code file.

![image](images/snake.jpg)

Declaring variables using the var keyword can make the program code less readable, as it does not indicate data types.

![image](images/commonr.jpg)

Constant

![image](images/1r.jpg)Start a new **C# Console App** and name it “Constant”

**Console.Title = “Constant” ;**

![image](images/2r.jpg)In Solution Explorer, right-click on the “Constant” project icon and choose **Add**, **New Item** from the menus

![image](images/pgc31_1.jpg)

![image](images/3r.jpg)Select the **Code File** option, then name it “Enums.cs” and click the **Add** button – to add the file to this project

![image](images/4r.jpg)In the **Code Editor**, type this statement within the newly added file – to create an enumerator list

**enum Days { Sat, Sun, Mon, Tue, Wed, Thu, Fri } ;**

![image](images/5r.jpg)Now, turn your attention to the main “Program.cs” file, then declare and initialize a constant and three variables

**const double pi = 3.14159265358979 ;**

**var daysType = typeof( Days ) ;**

**string name = Enum.GetName( daysType , 1 ) ;**

**bool flag = Enum.IsDefined( daysType , “Mon” ) ;**

![image](images/6r.jpg)Next, add statements to reveal the constant’s data type and details of the first two items in the enumerator list

**Console.WriteLine( “Pi Type: ” + pi.GetType( ) ) ;**

**Console.WriteLine( “Circumference: ” + ( pi * 3 ) ) ;**

**Console.WriteLine( “\nFirst Name: ” + Days.Sat ) ;**

**Console.WriteLine( “1st Index: ” + ( int ) Days.Sat ) ;**

**Console.WriteLine( “\n2nd Index: ” + name ) ;**

**Console.WriteLine( “Contains Mon?: ” + flag ) ;**

**Console.ReadKey( ) ;**

![image](images/7r.jpg)Press **Start** or **F5** to run the application and see the constant values in operation

![image](images/pgc31_2.jpg)

![image](images/forget.jpg)

The enumerator list contains names, not strings, so they need not be enclosed in quote marks, but the name must be supplied as a string argument to the **IsDefined( )** method.

![image](images/hot.jpg)

You may want to avoid the **var** keyword where possible to be sure of variable data types. For example, with the line **var id = getID( ) ;** the assigned value (and therefore the variable data type) could be numeric or a string.

**Summary**

![image](images/pgc32_1.jpg)

•A variable stores a data value within the computer’s memory, and the value can be referenced using that variable’s name.

•A variable declaration must specify the type of data it may contain, and a valid programmer-specified name.

•Common C# data types include int, char, float, double, decimal, bool, and string.

•Variables must be declared before they can be referenced.

•A variable becomes initialized when it is assigned a value.

•The Console.ReadLine( ) method can be used to assign user input to a variable.

•The Console.WriteLine( ) method adds a newline after its output, but the Console.Write( ) method does not.

•The System.Convert class provides a number of useful methods to convert string values to numerical data types.

•An array variable can store multiple items of data within sequential elements of a zero-based index.

•An array declaration must specify the type of data it may contain, followed by **[ ]** and a programmer-specified name.

•An array is not initialized until an array instance is created using the new keyword to specify data type and element size.

•Values can be assigned to individual array elements using the array name and the element index number.

•An array declaration can assign values to all of its array elements as a comma-separated list of values within **{ }** braces.

•Arrays can have more than one index, to represent multiple dimensions where each index is separated by a comma.

•Casting is the conversion of one data type to another.

•Implicit casting is performed automatically by C#.

•Explicit casting is performed by including a cast operator within a statement, to specify the required new data type.

•When a stored value is never intended to be changed, a “constant” container can be created using the **const** keyword.

•An enumerator list declaration is created using the **enum** keyword.

**24**

**Performing operations**

***This chapter introduces C# operators and demonstrates the operations they can perform.***

[**Doing arithmetic**](#chapter24.xhtml_sec194)

[**Assigning values**](#chapter24.xhtml_sec195)

[**Comparing values**](#chapter24.xhtml_sec196)

[**Assessing logic**](#chapter24.xhtml_sec197)

[**Examining conditions**](#chapter24.xhtml_sec198)

[**Setting precedence**](#chapter24.xhtml_sec199)

[**Summary**](#chapter24.xhtml_sec200)

Doing arithmetic

![image](images/pgc34_1.jpg)

The arithmetic operators commonly used in C# programs are listed in the table below, together with the operation they perform:

| **Operator** | **Operation** |
| **+** | Addition |
| **-** | Subtraction |
| ***** | Multiplication |
| **/** | Division |
| **%** | Modulus |
| **++** | Increment |
| **--** | Decrement |

The operators for assignment, addition, subtraction, multiplication, and division act as you would expect, but care must be taken to group expressions where more than one operator is used – operations within innermost ( ) parentheses are performed first:

**a = b * c - d % e / f ;                  // This is unclear.**

**a = ( b * c ) - ( ( d % e ) / f ) ;     // This is clearer.**

The % modulus operator will divide the first given number by the second given number and return the remainder of the operation. This is useful to determine if a number has an odd or an even value.

The ++ increment operator and -- decrement operator alter the given number by 1 and return the resulting value. These are most commonly used to count iterations in a loop – counting up on each iteration with the ++ increment operator, or counting down on each iteration with the -- decrement operator.

The ++ increment and -- decrement operators can be placed before or after a value to different effect – placed before the operand (prefix), its value is immediately changed; placed after the operand (postfix), its value is noted first, then the value is changed.

![image](images/hot.jpg)

The **%** modulus operator is also known as the “remainder” operator.

![image](images/forget.jpg)

Values used with operators to form expressions are called “operands” – in the expression **2 + 3** the numerical values **2** and **3** are the operands.

![image](images/hot.jpg)

The **+** operator is dual-purpose – it is also used to concatenate strings.

![image](images/commong.jpg)

Arithmetic

![image](images/1g.jpg)Start a new **C# Console App** and name it “Arithmetic”

**Console.Title = “Arithmetic” ;**

![image](images/2g.jpg)Type these statements to create and initialize two integer variables

**int a = 8 ;**

**int b = 4 ;**

![image](images/3g.jpg)Next, add statements to output the result of each basic arithmetical operation

**Console.WriteLine( “Addition:\t: ” + ( a + b ) ) ;**

**Console.WriteLine( “Subtraction:\t: ” + ( a - b ) ) ;**

**Console.WriteLine( “Multiplication:\t: ” + ( a * b ) ) ;**

**Console.WriteLine( “Division:\t: ” + ( a / b ) ) ;**

**Console.WriteLine( “Modulus:\t: ” + ( a % b ) ) ;**

![image](images/4g.jpg)Now, add statements to output the result of a postfix increment operation

**Console.WriteLine( “\nPostfix Increment:\t: ” + ( a++ ) ) ;**

**Console.WriteLine( “Postfix Result.....:\t: ” + a ) ;**

![image](images/5g.jpg)Finally, add statements to output the result of a prefix increment operation – for comparison with postfix

**Console.WriteLine( “\nPrefix Increment:\t: ” + ( ++b ) ) ;**

**Console.WriteLine( “Prefix Result.....:\t: ” + b ) ;**

**Console.ReadKey( ) ;**

![image](images/6g.jpg)Press **Start** or **F5** to run the application and see the results produced by each arithmetic operator

![images](images/pgc35_1.jpg)

![image](images/forget.jpg)

Here, the **\t** escape sequence is used to output a tab space, and the **\n** escape sequence is used to output additional newlines.

![image](images/snake.jpg)

Remember that a prefix operator changes the variable value immediately but a postfix operator changes the value subsequently.

**Assigning values**

![image](images/pgc36_1.jpg)

The operators that are used in C# programming to assign values are listed in the table below. All except the simple = assignment operator are a shorthand form of a longer expression, so each equivalent is given for clarity:

| **Operator** | **Example** | **Equivalent** |
| **=** | **a = b** | **a = b** |
| **+=** | **a += b** | **a = ( a + b )** |
| **-=** | **a -= b** | **a = ( a - b )** |
| ***=** | **a *= b** | **a = ( a * b )** |
| **/=** | **a /= b** | **a = ( a / b )** |
| **%=** | **a %= b** | **a = ( a % b )** |

In the assignment example above, where a = b, the variable named “a” is assigned the value that is contained in the variable named “b” – so that is then the value stored in the a variable. Technically speaking, the assignment operator stores the value of the right-hand operand in the memory location denoted by the left-hand operand, then returns the value as a result.

The += combined operator is useful to add a value onto an existing value that is stored in the a variable. In the example above, where a += b, the value in variable b is added to that in variable a – so the total is then the value stored in the a variable. The arithmetic operation is performed first with the grouped operands. The result is then stored in the memory location denoted by the first variable and returned.

All the other combined operators work in the same way by making the arithmetical operation between the two values first, then assigning the result of that operation to the first variable – to become its new stored value.

With the %= combined operator, the grouped left-hand operand a is divided by the grouped right-hand operand b, then the remainder of that operation is assigned to the a first variable.

![image](images/forget.jpg)

The += combined operator is dual-purpose – it can also be used to concatenate strings.

![image](images/snake.jpg)

It is important to regard the = operator to mean “assign” rather than “equals” to avoid confusion with the == equality operator that is described [here](#chapter24.xhtml_sec196).

![image](images/commong.jpg)

Assign

![image](images/1g.jpg)Start a new **C# Console App** and name it “Assign”

**Console.Title = **“Assign”** ;**

![image](images/2g.jpg)Type these statements to declare two integer variables

**int a ;**

**int b ;**

![image](images/3g.jpg)Next, add statements to output simple assigned values

**Console.Write( “Assign Values: ” ) ;**

**Console.Write( “\t a = ” + ( a = 8 ) ) ;**

**Console.WriteLine( “\t b = ” + ( b = 4 ) ) ;**

![image](images/4g.jpg)Now, add statements to output combined assigned values

**Console.Write( “\n\nAdd and Assign: ” ) ;**

**Console.Write( “\t a += b (8 += 4)\t a = ” + ( a += b ) ) ;**

**Console.Write( “\n\nSubtract and Assign: ” ) ;**

**Console.Write( “\t a -= b (12 -= 4)\t a = ” + ( a -= b ) ) ;**

**Console.Write( “\n\nMultiply and Assign: ” ) ;**

**Console.Write( “\t a *= b (8 *= 4)\t a = ” + ( a *= b ) ) ;**

**Console.Write( “\n\nDivide and Assign: ” ) ;**

**Console.Write( “\t a /= b (32 /= 4)\t a = ” + ( a /= b ) ) ;**

**Console.Write( “\n\nModulus and Assign: ” ) ;**

**Console.Write( “\t a %= b (8 %= 4)\t a = ” + ( a %= b ) ) ;**

**Console.ReadKey( ) ;**

![image](images/5g.jpg)Press **Start** or **F5** to run the application and see the results produced by each assignment operator

![images](images/pgc37_1.jpg)

![image](images/hot.jpg)

Notice how **\n\n** escape sequences are used here to add two newlines for spacing output.

![image](images/snake.jpg)

The operands must be of the same data type, or the right-hand operand must be implicitly convertible to the type of the left-hand operand.

**Comparing values**

![image](images/pgc38_1.jpg)

The operators that are commonly used in C# programming to compare two numerical values are listed in the table below:

| **Operator** | **Comparative Test** |
| **==** | Equality |
| **!=** | Inequality |
| **>** | Greater than |
| **<** | Less than |
| **>=** | Greater than or equal to |
| **<=** | Less than or equal to |

The == equality operator compares two operands and will return true if both are equal in value, otherwise the == operator will return false. If both are the same number, they are equal, or if both are characters, their Unicode code values are compared numerically.

Conversely, the != inequality operator returns true if two operands are not equal, using the same rules as the == equality operator, otherwise it returns false. Equality and inequality operators are useful in testing the state of two variables to perform conditional branching in a program.

The > “greater than” operator compares two operands and will return true if the first is greater in value than the second, or it will return false if it is equal or less in value. The < “less than” operator makes the same comparison but returns true if the first operand is less in value than the second, otherwise it returns false. Typically, a > “greater than” or < “less than” operator is used to test the value of an iteration counter in a loop structure.

Adding the = assignment operator after a > “greater than” operator or a < “less than” operator makes it also return true if the two operands are exactly equal in value.

![image](images/hot.jpg)

The comparison operators are also known as “relational operators”.

![image](images/hot.jpg)

You can specify a Boolean value to the **Convert**.**ToDouble()** method to discover that **true** is represented numerically as 1, and **false** is represented as 0.

![image](images/commong.jpg)

Comparison

![image](images/1g.jpg)Start a new **C# Console App** and name it “Comparison”

**Console.Title = “Comparison” ;**

![image](images/2g.jpg)Type these statements to declare three integer variables and two character variables to be compared

**int nil = 0 , num = 0 , max = 1 ;**

**char cap = ‘A’ , low = ‘a’ ;**

![image](images/3g.jpg)Next, add statements to output the result of equality comparisons of integers and characters

**Console.Write( “Equality:” ) ;**

**Console.Write( “\t (0 == 0) : ” + ( nil == num ) ) ;**

**Console.Write( “\n\t\t (A == a) : ” + ( cap == low ) ) ;**

![image](images/4g.jpg)Now, add statements to output the result of other integer comparisons

**Console.Write( “\n\nInequality:” ) ;**

**Console.Write( “\t (0 != 1) : ” + ( nil != max ) ) ;**

**Console.Write( “\n\nGreater:” ) ;**

**Console.Write( “\t (0 > 1) : ” + ( nil > max ) ) ;**

**Console.Write( “\nLess:” ) ;**

**Console.Write( “\t\t (0 < 1) : ” + ( nil < max ) ) ;**

**Console.Write( “\n\nGreater/Equal:” ) ;**

**Console.Write( “\t (0 >= 0) : ” + ( nil >= num ) ) ;**

**Console.Write( “\nLess or Equal:” ) ;**

**Console.Write( “\t (1 <= 0) : ” + ( max <= nil ) ) ;**

**Console.ReadKey( ) ;**

![image](images/5g.jpg)Press **Start** or **F5** to run the application and see the results produced by each comparison

![images](images/pgc39_1.jpg)

![image](images/forget.jpg)

The Unicode code value for uppercase **‘A’** is 65 but for lowercase **‘a’** it’s 97 – so their comparison here returns **false**.

![image](images/snake.jpg)

When comparing numbers, remember to test for equality as well as testing for higher and lower values.

**Assessing logic**

![image](images/pgc40_1.jpg)

The logical operators most commonly used in C# programming are listed in the table below:

| **Operator** | **Operation** |
| **&&** | Logical AND |
| **&#124;&#124;** | Logical OR |
| **!** | Logical NOT |

The logical operators are used with operands that have Boolean values of true or false, or are values that convert to true or false.

The && logical AND operator will evaluate two operands and return true only if both operands themselves are true. Otherwise, the && logical AND operator will return false. This is used in conditional branching where the direction of a program is determined by testing two conditions – if both conditions are satisfied, the program will go in a certain direction, otherwise it will take a different direction.

Unlike the && logical AND operator, which needs both operands to be true, the || logical OR operator will evaluate its two operands and return true if either one of the operands itself returns true. If, however, neither operand returns true, then the || logical OR operator will return false. This is useful in C# programming to perform a certain action if either one of two test conditions has been met.

The ! logical NOT operator is a unary operator that is used before a single operand. It returns the inverse value of the given operand, so if the variable a had a value of true then !a would have a value of false. The ! logical NOT operator is useful in C# programs to toggle the value of a variable in successive loop iterations with a statement like a = !a. This ensures that on each pass the value is changed, like flicking a light switch on and off.

![image](images/commong.jpg)

Logic

![image](images/1g.jpg)Start a new **C# Console App** and name it “Logic”

**Console.Title = “Logic” ;**

![image](images/2g.jpg)Type this statement to declare two Boolean variables

**bool yes = true , no = false ;**

![image](images/3g.jpg)Add these statements to output the result of AND logic

**Console.Write( “AND Logic:” ) ;**

**Console.Write( “\t (yes && yes) : ” + ( yes && yes ) ) ;**

**Console.Write( “\n\t\t (yes && no ) : ” + ( yes && no ) ) ;**

**Console.Write( “\n\t\t (no && no ) : ” + ( no && no ) ) ;**

![image](images/4g.jpg)Now, add statements to output the result of OR logic

**Console.Write( “\n\nOR Logic:” ) ;**

**Console.Write( “\t (yes || yes) : ” + ( yes || yes ) ) ;**

**Console.Write( “\n\t\t (yes || no ) : ” + ( yes || no ) ) ;**

**Console.Write( “\n\t\t (no || no ) : ” + ( no || no ) ) ;**

![image](images/5g.jpg)Then, add statements to output the result of NOT logic

**Console.Write( “\n\nNOT Logic:” ) ;**

**Console.Write( “\t yes = ” + yes ) ;
Console.Write( “\t !yes = ” + !yes ) ;
Console.Write( “\n\t\t no = ” + no ) ;
Console.Write( “\t !no = ” + !no ) ;
Console.ReadKey( ) ;**

![image](images/6g.jpg)Press **Start** or **F5** to run the application and see the results produced by each logical operation

![images](images/pgc41_1.jpg)

![image](images/forget.jpg)

The value returned by the **!** logical NOT operator is the inverse of the stored value – the stored value itself remains unchanged.

![image](images/hot.jpg)

Notice that **false** **&&** **false** returns **false**, not **true** – demonstrating the maxim “two wrongs don’t make a right”.

**Examining conditions**

Possibly, the C# programmer’s favorite test operator is the ?: “ternary” operator. This operator first evaluates an expression for a true or false condition, then returns one of two specified values depending on the result of the evaluation. For this reason, it is also known as the “conditional” operator.

![image](images/pgc42_1.jpg)

The ?: ternary operator has this syntax:

**( *test-expression* ) ? *if-true-return-this* : *if-false-return-this* ;**

Although the ternary operator can initially appear a little confusing, it is well worth becoming familiar with this operator as it can execute powerful program branching with minimal code – for example, to branch when a variable is not a value of 1:

**( *variable* != 1 ) ? *if-true-do-this* : *if-false-do-this* ;**

The ternary operator is commonly used in C# programming to assign the maximum or minimum value of two variables to a third variable, for example, to assign a minimum, like this:

**c = ( a < b ) ? a : b ;**

The expression in parentheses returns true when the value of variable a is less than that of variable b – so in this case, the lesser value of variable a gets assigned to variable c.

Similarly, replacing the < less than operator in the test expression with the > greater than operator would assign the greater value of variable b to variable c.

Another common use of the ternary operator incorporates the % modulus operator in the test expression to determine whether the parity value of a variable is an odd number or an even number:

**( *variable* % 2 != 0 ) ? *if-true*(*odd*)-*do-this* : *if-false(even)-do-this* ;**

Where the result of dividing the variable value by 2 does leave a remainder, the number is odd – where there is no remainder, the number is even. The test expression ( variable % 2 == 1 ) would have the same effect, but it is preferable to test for inequality – it’s easier to spot when something is different than when it’s identical.

![image](images/forget.jpg)

The ternary operator has three operands – the one before the **?** and those before and after the :.

![image](images/hot.jpg)

Value equality, where two variables contain an equal value, is also known as “equivalence”.

![image](images/commong.jpg)

Condition

![image](images/1g.jpg)Start a new **C# Console App** and name it “Condition”

**Console.Title = “Condition” ;**

![image](images/2g.jpg)Type these statements to declare and initialize two integer variables

**int a = 8 ;**

**int b = 3 ;**

![image](images/3g.jpg)Next, add these statements to output an appropriate string with correct grammar for quantity

**string verb = ( a != 1 ) ? “ are “ : “ is “ ;**

**Console.WriteLine( “There” + verb + a +”\n” ) ;**

![image](images/4g.jpg)Now, add statements to output an appropriate string correctly describing the parity of each variable value

**string parity = ( a % 2 != 0 ) ? “Odd“ : “Even“ ;**

**Console.WriteLine( a + “ is “ + parity ) ;**

**parity = ( b % 2 != 0 ) ? “Odd“ : “Even“ ;
Console.WriteLine( b + “ is “ + parity ) ;**

![image](images/5g.jpg)Then, add statements to output a string reporting the greater of these two variable values

**int max = ( a > b ) ? a : b ;**

**Console.Write( “\nMaximum is “ + max ) ;**

**Console.ReadKey( ) ;**

![image](images/6g.jpg)Press **Start** or **F5** to run the application and see the results produced by examining each variable value

![images](images/pgc43_1.jpg)

![image](images/hot.jpg)

The **?:** ternary operator can return values of any data type – numbers, strings, Booleans, etc.

**Setting precedence**

Operator precedence determines the order in which C# evaluates expressions. For example, the expression 1 + 5 * 3 evaluates to 16, not 18, because the * multiplication operator has a higher precedence than the + addition operator. Parentheses can be used to specify precedence, so that ( 1 + 5 ) * 3 evaluates to 18.

![image](images/pgc44_1.jpg)

When operators have equal precedence, their “associativity” determines how expressions are grouped. For example, the - subtraction operator is left-associative, grouping left-to-right (LTR), so 8 - 4 - 2 is grouped as ( 8 - 4 ) - 2 and thus evaluates to 2. Other operators are right-associative, grouping right-to-left (RTL).

The table below lists common operators in order of precedence, with the highest-precedence ones at the top. Operators on the same line have equal precedence, so operator associativity determines how expressions are grouped and evaluated.

| **Category** | **Operator** | **Associativity** |
| Postfix | **( ) [ ] . ++ --** | LTR ![images](images/hand.jpg) |
| Unary Sign
Prefix | **[!] + -
++ --** | ![images](images/hand1.jpg) RTL |
| Multiplicative | *** / %** | LTR ![images](images/hand.jpg) |
| Additive | **+ -** | LTR ![images](images/hand.jpg) |
| Comparative | **< <= > >=** | LTR ![images](images/hand.jpg) |
| Equivalence | **== !=** | LTR ![images](images/hand.jpg) |
| Conditional | **&&** | LTR ![images](images/hand.jpg) |
| Conditional | **&#124;&#124;** | LTR ![images](images/hand.jpg) |
| Conditional | **?:** | ![images](images/hand1.jpg) RTL |
| Assignment | **= += -= *= /= %=** | ![images](images/hand1.jpg) RTL |
| Comma | , | LTR ![images](images/hand.jpg) |

![image](images/forget.jpg)

The ***** multiply operator is on a higher row than the **+** addition operator – so in the expression **a=1+5*3**, multiplication is completed first, before the addition.

![image](images/hot.jpg)

There are also a number of “bitwise” operators, which are used to perform binary arithmetic – see [here](#chapter04.xhtml_sec29). Those operators perform in just the same way in C#.

![image](images/commong.jpg)

Precedence

![image](images/1g.jpg)Start a new **C# Console App** and name it “Precedence”

**Console.Title = “Precedence” ;**

![image](images/2g.jpg)Type this statement to declare an integer variable

**int sum ;**

![image](images/3g.jpg)Add these statements to initialize the variable with the result of an ungrouped expression and display that result

**sum = 1 + 4 * 3 ;**

**Console.WriteLine( “Default Order:\t\t” + sum ) ;**

![image](images/4g.jpg)Next, add statements to assign the result of a grouped expression and display that result

**sum = ( 1 + 4 ) * 3 ;**

**Console.WriteLine( “Forced Order:\t\t” + sum ) ;**

![image](images/5g.jpg)Add statements to assign the result of a new ungrouped expression and display that result

**sum = 7 - 4 + 2 ;**

**Console.WriteLine( “\nDefault Direction:\t” + sum ) ;**

![image](images/6g.jpg)Now, add statements to assign the result of the new grouped expression and display that result

**sum = 7 - ( 4 + 2 ) ;**

**Console.WriteLine( “\nForced Direction:\t” + sum ) ;**

**Console.ReadKey( ) ;**

![image](images/7g.jpg)Press **Start** or **F5** to run the application and see the results produced by examining each variable value

![images](images/pgc45_1.jpg)

![image](images/forget.jpg)

The ***** multiplication operator takes precedence over the **+** addition operator – so multiplication is performed first.

![image](images/forget.jpg)

The **-** subtraction operator and the **+** addition operator have equal precedence but also have left-to-right associativity – so subtraction is performed first before addition.

![image](images/snake.jpg)

It is best to clarify all expressions by adding parentheses to group operations.

**Summary**

![image](images/pgc46_1.jpg)

•Arithmetic operators can form expressions with two operands for + addition, - subtraction, * multiplication, and / division.

•The % modulus arithmetic operator divides the first operand by its second operand, then returns the remainder.

•Care must be taken to group expressions within ( ) parentheses where more than one operator is used.

•The ++ increment and -- decrement operators may be postfixed or prefixed to modify a single operand by 1.

•The = assignment operator can be combined with an arithmetic operator to assign the result of an operation.

•Comparison operators can form expressions with two operands for == equality or for != inequality.

•Comparison operators can form expressions with two operands for > greater or for < lesser value comparison.

•Equality can also be recognized in comparisons with the >= greater-or-equal and <= less-or-equal operators.

•The && logical-AND operator will return true only if both operands are themselves true.

•The || logical-OR operator will return true if either of the two operands are themselves true.

•The ! logical-NOT operator returns the inverse Boolean value of a single given operand.

•The ?: ternary operator evaluates a given Boolean expression, then returns one of two operands depending on the result.

•Operator precedence determines the order in which expressions are evaluated.

•When operators have equal precedence, their associativity determines how expressions are grouped for evaluation.

**25**

**Making statements**

***This chapter demonstrates how statements can evaluate expressions to determine the direction in which a C# program will proceed.***

[**Branching with if**](#chapter25.xhtml_sec201)

[**Switching branches**](#chapter25.xhtml_sec202)

[**Looping for**](#chapter25.xhtml_sec203)

[**Looping while**](#chapter25.xhtml_sec204)

[**Iterating for each**](#chapter25.xhtml_sec205)

[**Summary**](#chapter25.xhtml_sec206)

**Branching with if**

![image](images/pgc48_1.jpg)

The C# **if** keyword performs the basic conditional test that evaluates a given expression for a Boolean value of **true** or **false** – and its syntax looks like this:

**if ( *test-expression* ) { *statements-to-execute-when-true* }**

The braces following the test may contain one or more statements, each terminated by a ; semicolon, but these will only be executed when the expression is found to be **true**. When the test is found to be **false**, the program proceeds to its next task.

To allow “conditional branching”, an **if** statement can offer alternative statements to execute when the test fails by appending an **else** statement block after the **if** statement block, like this:

**if ( *test-expression* ) { *statements-to-execute-when-true* }**

**else { *statements-to-execute-when-false* }**

To test two conditions, the test expression may use the **&&** operator – for example, **if ( ( num > 5 ) && ( letter == ‘A’ ) )**.

Alternatively, an **if** statement can be “nested” within another **if** statement, so those statements in the inner statement block will only be executed when both tests succeed – but statements in the outer statement block will be executed if the outer test succeeds:

![image](images/commonap.jpg)

IfElse

![image](images/1p.jpg)Start a new **C# Console App** and name it “IfElse”

**Console.Title = “IfElse” ;**

![image](images/2p.jpg)Type these statements to create and initialize two variables from user input

**Console.Write( “Please Enter A Number: ” ) ;**

**double num = Convert.ToDouble( Console.ReadLine( ) ) ;**

Console.Write( “Thanks. Now Enter A Letter: ” ) ;

**char letter = Convert.ToChar( Console.ReadLine( ) ) ;**

![image](images/3p.jpg)Next, add a statement to output a message if the user’s number input exceeds a specified value

**if ( num >= 6 )**

**{**

**Console.WriteLine( “\nNumber Exceeds 5” ) ;**

**// Nested statement to be inserted here (Step 5).**

**}**

![image](images/hot.jpg)

Shorthand can be used when testing a Boolean value – so the expression **if( flag == true)** can be written as **if( flag )**.

![image](images/snake.jpg)

Avoid nesting more than three levels of **if** statements – to prevent confusion and errors.

![image](images/4p.jpg)Now, add a statement to output an alternative message if the user’s number input is less than the specified value

**else**

**{**

**Console.WriteLine( “\nNumber Is 5 Or Less” ) ;**

**}**

**Console.ReadKey( ) ;**

![image](images/5p.jpg)Insert a statement within the **if** block to output a message when the user’s letter input matches a specified value

**if ( letter == ‘C’ )**

**{**

**Console.WriteLine( “Letter Is ‘C’” ) ;**

**}**

![image](images/6p.jpg)Press **Start** or **F5** to run the application and enter values to see the program branch according to your input

![image](images/pgc49_1.jpg)

![image](images/pgc49_2.jpg)

![image](images/pgc49_3.jpg)

![image](images/pgc49_4.jpg)

![image](images/hot.jpg)

Where there is only one statement to execute when the test succeeds, the **{ }** braces may be omitted – but retaining them aids code clarity.

**Switching branches**

![image](images/pgc50_1.jpg)

The **if** and **else** keywords, introduced [here](#chapter25.xhtml_sec201), allow programs to branch in a particular direction according to the result of a test condition, and can be used to repeatedly test a variable to match a value – for example, testing for an integer:

**if ( num == 1 ) { Console.Write( “Monday” ) ; }**

**else**

**if ( num == 2 ) { Console.Write( “Tuesday” ) ; }**

**else**

**if ( num == 3 ) { Console.Write( “Wednesday” ) ; }**

**else**

**if ( num == 4 ) { Console.Write( “Thursday” ) ; }**

**else**

**if ( num == 5 ) { Console.Write( “Friday” ) ; }**

The program will branch in the direction of the match.

Conditional branching with long **if**-**else** statements can often be more efficiently performed using a **switch** statement instead, especially when the test expression evaluates just one variable.

The **switch** statement works in an unusual way. It takes a given variable value, or expression, then seeks a matching value among a number of **case** statements. One or more statements associated with the matching case statement will then be executed.

When no match is found, no **case** statements will be executed, but you may add a **default** statement after the final **case** statement to specify statements to be executed when no match is found. The syntax of a typical switch statement looks like this:

**switch( *variable-name* )**

**{**

**case *value1* : *statement* ; break ;**

case *value2* : *statement* ; break ;

case *value3* : *statement* ; break ;

default : *statement* ; break ;

**}**

It is important to follow each case statement with the **break** keyword. Unlike other programming languages, C# does not allow fall-through from one **case** statement to another – each **case** statement must allow control to be handed back in order to exit the **switch** block.

![image](images/hot.jpg)

Avoid writing lengthy **if**-**else** statements like the one shown here – where possible, use a **switch** statement instead.

![image](images/snake.jpg)

Missing **break** keywords in C# **case** statements are syntax errors.

![image](images/commonap.jpg)

Switch

![image](images/1p.jpg)Start a new **C# Console App** and name it “Switch”

**Console.Title = “Switch” ;**

![image](images/2p.jpg)Type this statement to create and initialize an integer variable

**int num = 3 ;**

![image](images/3p.jpg)Next, add a statement to declare a string variable

**string day ;**

![image](images/4p.jpg)Now, add a statement to initialize the string variable according to the value of the integer variable

**switch( num )**

**{**

**case 1 : day = “Monday” ; break ;**

**case 2 : day = “Tuesday” ; break ;**

**case 3 : day = “Wednesday” ; break ;**

**case 4 : day = “Thursday” ; break ;**

**case 5 : day = “Friday” ; break ;**

**// Default statement to be inserted here (Step 5).**

**}**

![image](images/5p.jpg)Then, insert a final statement into the **switch** block to initialize the **string** variable when no match is found

**default : day = “Weekend Day” ; break ;**

![image](images/6p.jpg)Finally, add statements to output the assigned value

**Console.WriteLine( “Day ” + num + “ : “ + day ) ;**

Console.ReadKey( ) ;

![image](images/7p.jpg)Press **Start** or **F5** to run the application and see the string result of the switch block assignment

![image](images/pgc51_1.jpg)

![image](images/hot.jpg)

A ****case**** statement can also try to match against a **string** value – for example: ****case** : “ABC”**.

**Looping for**

A loop is a piece of code in a program that automatically repeats. One complete execution of all statements contained within the loop block is known as an “iteration” or “pass”.

![image](images/pgc52_1.jpg)

The number of iterations made by a loop is controlled by a conditional test made within the loop. While the tested expression remains **true**, the loop will continue – until the tested expression becomes **false**, at which time the loop ends.

The three types of loop structures in C# programming are **for** loops, **while** loops, and **do**-**while** loops. Perhaps the most commonly used loop is the **for** loop, which has this syntax:

**for ( *initializer* ; *test-expression* ; *updater* ) { *statements* }**

The initializer sets the starting value for a counter of the number of iterations to be made by the loop. An integer variable is used for this purpose and is traditionally named “i”.

Upon each iteration of the loop, the test expression is evaluated, and that iteration will only continue while this expression is **true**. When the tested expression becomes **false**, the loop ends immediately without executing the statements again. On each iteration, the counter is updated then the statements executed.

![image](images/pgc52_2.jpg)

Loops may be nested within other loops – so that the inner loop will fully execute its iterations on each iteration of the outer loop.

![image](images/hot.jpg)

The updater may increment the counter using the **++** operator to count up, or decrement the counter using the **--** decrement operator to count down.

![image](images/commonap.jpg)

ForLoop

![image](images/1p.jpg)Start a new **C# Console App** and name it “ForLoop”

**Console.Title = “ForLoop” ;**

![image](images/2p.jpg)Type these statements to create a loop that will make three iterations

**for( int i = 1 ; i < 4 ; i++ )**

**{**

**Console.WriteLine( “Loop Iteration: “ + i ) ;**

**// Nested loop to be inserted here (Step 4).**

**}**

**Console.ReadKey( ) ;**

![image](images/3p.jpg)Press **Start** or **F5** to run the application and see the loop counter displayed on each iteration

![image](images/pgc53_1.jpg)

![image](images/4p.jpg)Inside the **for** loop block, insert another **for** loop that will also make three iterations

**for( int j = 1 ; j < 4 ; j++ )**

**{**

Console.WriteLine( “\tInner Loop Iteration: “ + j ) ;

**}**

![image](images/5p.jpg)Press **Start** or **F5** to run the application once more and now see both loop counters displayed on each iteration

![image](images/pgc53_2.jpg)

![image](images/forget.jpg)

On the third iteration of these loops, the updater increments the counter value to **4** – so when it is next evaluated, the test expression returns **false** and the loop ends.

**Looping while**

An alternative to the **for** loop, introduced [here](#chapter25.xhtml_sec203), uses the **while** keyword, followed by an expression to be evaluated. When the expression is **true**, statements contained within braces following the test expression will be executed. The expression will then be evaluated again, and the **while** loop will continue until the expression is found to be **false**.

![image](images/pgc54_1.jpg)

**while ( *test-expression* ) { *statements* }**

The loop’s statement block must contain code that will affect the tested expression in order to change the evaluation result to **false**, otherwise an infinite loop is created that will lock the program! If the tested expression is found to be **false** upon its first evaluation, the **while** loop’s statement block will never be executed.

A subtle variation of the **while** loop places the **do** keyword before the loop’s statement block and a **while** test after it, with this syntax:

**do { *statements* } while ( *test-expression* ) ;**

In a **do-while** loop, the statement block will always be executed at least once – because the expression is not evaluated until after the first iteration of the loop.

![image](images/hot.jpg)

If you accidentally start running an infinite loop – for example:

**while**( **true** )

**{**

**Console**.Write( i ) ;

**i++ ;**

**}**

press the **Ctrl** + **C** keys to terminate the process.

**Breaking out of loops**

A **break** statement can be included in any kind of loop to immediately terminate the loop when a test condition is met. The **break** ensures no further iterations of that loop will be executed.

Similarly, a **continue** statement can be included in any kind of loop to immediately terminate that particular iteration of the loop when a test condition is met. The **continue** statement allows the loop to proceed to the next iteration:

![image](images/commonap.jpg)

WhileLoop

![image](images/1p.jpg)Start a new **C# Console App** and name it “WhileLoop”

**Console.Title = “WhileLoop” ;**

![image](images/2p.jpg)Type these statements to create and initialize an integer array variable and a regular integer counter variable

**int [ ] nums = new int[ 10 ] ;**

**int i = 0 ;**

![image](images/3p.jpg)Next, add a **while** loop to assign its incrementing counter value to an array element and display it on each iteration

**while( i < nums.Length )**

**{**

**nums[ i ] = i ;**

**Console.Write( “ | “ + nums[ i ] ) ;**

**i++ ;**

**}**

**Console.Write( “\n\n“ ) ;**

![image](images/4p.jpg)Now, add a **do-while** loop to display its decrementing counter value on each iteration

**do**

**{**

**i-- ;**

**// Statements to be inserted here (step 6).**

**Console.Write( “ | “ + nums[ i ] ) ;**

**}**

**while( i > 0 ) ;**

Console.ReadKey( ) ;

![image](images/forget.jpg)

Remember that the **while** statement at the end of a **do**-**while** loop must be terminated with a ; semicolon.

![image](images/5p.jpg)Press **Start** or **F5** to run the application and see both loop counters displayed on each iteration

![image](images/pgc55_1.jpg)

![image](images/6p.jpg)In the **do-while** loop, insert a statement to skip a single iteration, and a statement to prematurely exit the loop

**if( i == 8 ) { Console.Write( “ | Skipped” ) ; continue ; }**

if( i == 3 ) { Console.Write( “ | Done” ) ; break ; }

![image](images/7p.jpg)Press **Start** or **F5** to run the application once more, and now see the **do-while** loop iterations skipped

![image](images/pgc55_2.jpg)

![image](images/hot.jpg)

Notice how the array’s **Length** property is used to determine the number of elements it contains.

![image](images/snake.jpg)

The position of **break** and **continue** statements is important – they must appear after the updater, to avoid creating an infinite loop, but before any other statements, to prevent their execution.

**Iterating for each**

![image](images/pgc56_1.jpg)

C# provides a special **foreach-in** statement that allows you to easily traverse all elements in an array to access all stored values. This is an “iterator”, rather than a loop structure, so it cannot be used to assign or modify element values – it can only be used to read their values. Syntax of a **foreach-in** statement looks like this:

**foreach ( *data-type variable-name* in *array-name* ) { *statements* }**

The **foreach** keyword must specify a variable of an appropriate data type to which each element value can be assigned, one by one, and the **in** keyword must specify the name of the array:

![image](images/commonap.jpg)

ForEach

![image](images/1p.jpg)Start a new **C# Console App** and name it “ForEach”

**Console.Title = “ForEach” ;**

![image](images/2p.jpg)Type this statement to create and initialize a **string** array

**string [ ] websites = new string [ 5 ]**

**{** “Google”, “YouTube”, “Facebook”, “Baidu”, “Yahoo!” } ;

![image](images/3p.jpg)Next, add a statement to display a list heading

**Console.WriteLine( “Popular Websites...“ ) ;**

![image](images/4p.jpg)Now, add a foreach statement to display a counter value and list item value on each iteration

**int rank = 1 ;**

**foreach( string site in websites )**

**{**

**Console.WriteLine( “Position: “ + rank + ”\t” + site ) ;**

**rank++ ;**

**}**

**Console.ReadKey( ) ;**

![image](images/5p.jpg)Press **Start** or **F5** to run the application and see the iterator display the counter and element values

![image](images/pgc56_2.jpg)

![image](images/snake.jpg)

Use a **for** loop if you need to assign or modify element values.

![image](images/hot.jpg)

The **break** and **continue keywords** can be used in a **foreach** statement to exit the iteration cycle.

A **foreach-in** statement can also be used to traverse all elements of a C# “dictionary” that contains associated key-value pairs. The data types of the key and value must be specified as a comma-separated pair within **< >** angled brackets in the declaration:

**Dictionary < *data-type, data-type* > *dictionary-name =***

**new Dictionary < *data-type, data-type* > ( ) ;**

The **foreach** keyword must specify a **KeyValuePair** to which each key-value pair value can be assigned, one by one, and the **in** keyword must specify the name of the dictionary:

![image](images/commonap.jpg)

KeyValue

![image](images/1p.jpg)Start a new **C# Console App** and name it “KeyValue”

**Console.Title = “KeyValue” ;**

![image](images/2p.jpg)Type these statements to create and initialize a dictionary named “BookList”

**Dictionary < string, string > BookList =**

new Dictionary < string, string > ( ) ;

BookList.Add( “Michael Price”, “Microsoft 365” ) ;

BookList.Add( “Nick Vandome”,“Windows 11” ) ;

BookList.Add( “Mike McGrath”, “Java” ) ;

![image](images/3p.jpg)Now, add a statement to display a list heading

**Console.WriteLine( “Popular Titles...“ ) ;**

![image](images/4p.jpg)Add a **foreach** statement to display each key-value pair

**foreach( KeyValuePair < string, string > book in BookList )**

**{**

**Console.WriteLine( “Key: “ + book.Key +**

**“\tValue: ”+ book.Value + “ in easy steps” ) ;**

**}**

**Console.ReadKey( ) ;**

![image](images/5p.jpg)Press **Start** or **F5** to run the application and see the iterator display the dictionary’s key-value pairs

![image](images/pgc57_1.jpg)

![image](images/hot.jpg)

Note that a **Dictionary** object has **Add( )** and **Remove( )** methods, and has **Key** and **Value** properties.

**Summary**

![image](images/pgc58_1.jpg)

•An **if** statement evaluates a given test expression for a Boolean value of **true** or **false**.

•Statements contained in braces after an **if** statement will only be executed when the evaluation is found to be **true**.

•Multiple **if** statements can be nested, so statements in the inner loop are only executed when both loop tests return **true**.

•The **if** and **else** keywords are used to perform conditional branching according to the result of a tested expression.

•A **switch** statement is an alternative form of conditional branching that matches a **case** statement to a given value.

•Each **case** statement must be terminated by the **break** keyword, as C# does not allow fall-through.

•The **for** loop structure has parameters declaring an initializer, a test expression, and an updater.

•A loop updater may **++** increment a counter to count up, or may **--** decrement a counter to count down.

•A **while** loop may never execute its statements, but a **do-while** loop will always execute its statements at least once.

•A **while** loop and **do-while** loop must always have an updater within their loop body to avoid creating an infinite loop.

•Any type of loop can be immediately terminated by including a **break** statement within the loop body.

•A single iteration of any type of loop can be skipped by including a **continue** statement within the loop body.

•A **foreach-in** statement is an iterator that can traverse all elements of an array to read their values.

•A **foreach-in** statement can traverse all key-value pairs of a dictionary to read their values.

**26**

**Devising methods**

***This chapter demonstrates how to create methods that can be called to execute statements whenever the C# program requires them.***

[**Creating function**](#chapter26.xhtml_sec207)

[**Passing arguments**](#chapter26.xhtml_sec208)

[**Overloading methods**](#chapter26.xhtml_sec209)

[**Refactoring code**](#chapter26.xhtml_sec210)

[**Summary**](#chapter26.xhtml_sec211)

**Creating function**

A C# programmer-specified “function” encloses a section of reusable code that can be called whenever required by the program. Local functions can be created in the “Program.cs” file and can be called to execute their section of code as needed.

![image](images/pgc60_1.jpg)

Functions can also be created within class structures. These are referred to as “methods” of the class. For example, the **WriteLine()** function is a method of the **Console** class.

Functions (a.k.a. methods) provide these three main benefits:

•Modular program code is easier to understand and maintain.

•Tried and tested code can be re-used by other programs.

•The workload on large programs can be more easily shared.

A function is declared in a C# program by specifying the various elements of its structure with this syntax:

***access-specifier return-data-type function-name ( parameters )***

**{**

***statements***

**}**

The access specifier determines the visibility of the function to other classes. The keyword **public** specifies global accessibility, whereas **private** or **static** keywords specify only local accessibility.

If the function will return a value to the caller, the data type of that value must be specified. If the function will never return a value, the **void** keyword must be specified.

A name must be specified for each programmer-defined function, adhering to the same naming conventions as variable names.

Optionally, parameters may be specified within parentheses after the function name to represent “argument” values passed from the caller. Once defined, a method without parameters may be called simply by stating its name followed by parentheses.

Variables declared within a function are not, by default, visible to other parts of the program. The visibility of variables is known as “variable scope” and variables within a function have only “local” scope. This means that variables declared in different functions may be given the same name without conflict.

![image](images/hot.jpg)

The first part of a function declaration, defining its access, return type, name, and parameters, is known as the function “signature”.

![image](images/hot.jpg)

The use of methods by other classes is described and demonstrated in the chapter on Object Oriented Programming – see [here](#chapter30.xhtml_sec233).

![image](images/hot.jpg)

Parameters and arguments are demonstrated in the example [here](#chapter26.xhtml_sec208).

![image](images/commonao.jpg)

Function

![image](images/1o.jpg)Start a new **C# Console App** and name it “Function”

**Console.Title = “Function” ;**

![image](images/2o.jpg)Type this code to create a function that will output two text strings, but return nothing to the caller

**static void bodyTempC( )**

**{**

**Console.WriteLine( “Body Temperature...” ) ;**

**Console.WriteLine( “Centigrade:\t37ºC” ) ;**

**}**

![image](images/3o.jpg)Next, add a function that outputs nothing, but will return a floating-point value to the caller

**static double bodyTempF( )**

**{**

**double temperature = 98.6 ;**

**return temperature ;**

**}**

![image](images/forget.jpg)

Each variable can have the same name as they have only local scope.

![image](images/4o.jpg)Now, add a function that outputs nothing, but will return an integer value to the caller

**static int bodyTempK( )**

**{**

**int temperature = 310 ;**

**return temperature ;**

**}**

![image](images/5o.jpg)Finally, add statements to call each of the programmer-specified functions created above

**bodyTempC( ) ;**

**Console.WriteLine( “Fahrenheit:\t” + bodyTempF( ) + “ºF” ) ;**

**Console.WriteLine( “Kelvin:\t” + bodyTempK( ) + “K” ) ;**

**Console.ReadKey( ) ;**

![image](images/6o.jpg)Press **Start** or **F5** to run the application and see the output featuring the function calls

![image](images/pgc61_1.jpg)

![image](images/hot.jpg)

You can use the Windows Accessories, Character Map facility to produce the **º** degree symbol.

**Passing arguments**

![image](images/pgc62_1.jpg)

Functions may optionally specify one or more parameters as a comma-separated list within the parentheses of their definition. Each specified parameter must state the data type it may contain, and a name by which it may be referenced within the function – for example, parameters for text and a number, like this:

**static void setUser( string name , int age ) { *statements* }**

When a function with parameters is called, the caller must normally pass the correct number of argument values of the required data type. These are listed within the parentheses of the calling statement – for example, calling the function above:

**setUser( “Alison” , 18 ) ;**

Optionally, the parameter declaration may be assigned a default value to use if no argument value is passed by the caller. In this case, the caller may pass, or omit, an argument value:

**static void setUser( string name , int age = 21 ) { statements }**

**setUser( “Brenda” , 19 ) ;**

**setUser( “Christine” ) ;                         // age = 21.**

There are three ways to pass arguments into functions:

•**By Value** – Arguments passed to functions “by value” assign a copy of the original value to the parameter. Changes made to the parameter inside the function do not affect the original.

•**By Reference** – Arguments passed to functions “by reference” assign the address of the memory location of the original value to the parameter. Changes made to the parameter inside the function do affect the original value. Reference arguments must include the C# **ref** keyword in both the function call parentheses and the function definition parameter list.

•**For Output** – Arguments passed to functions “for output” assign the memory location address of the argument to the parameter, to which the function can assign a value. This is similar to passing by reference except that data is passed from the function, rather than to the function. Output arguments must include the C# **out** keyword in both the function call parentheses and the function definition parameter list. This is useful to return more than one value from a function.

![image](images/snake.jpg)

Calling a function without passing required arguments, or arguments of the wrong data type, will cause an error.

![image](images/hot.jpg)

Most function calls pass arguments by value rather than by reference or for output.

![image](images/commonao.jpg)

Parameter

![image](images/1o.jpg)Start a new **C# Console App** and name it “Parameter”

**Console.Title = “Parameter” ;**

![image](images/2o.jpg)Type these statements to declare two variables

**double weight ;**

**string num ;**

![image](images/3o.jpg)Add this function that will output a double value and return a string value

**static string getWeight( out double theWeight )**

**{**

**theWeight = 10 ;**

**return “Ten” ;**

**}**

![image](images/4o.jpg)Next, add a function that will return a multiplied value of its parameter argument

**static double lbToKg( double pounds = 5 )**

**{ return ( pounds * 0.45359237 ) ; }**

![image](images/forget.jpg)

The default parameter value is not used here, as the caller passes in an argument value.

![image](images/5o.jpg)Now, add a function that will assign a divided value to its parameter reference argument but return nothing

**static void kgToLb( ref double weight )**

**{ weight = ( weight / 0.45359237 ) ; }**

![image](images/6o.jpg)Finally, add statements to pass arguments to each of the functions declared above

**num = getWeight( out weight ) ;**

**Console.WriteLine( num +“ lb = ” + lbToKg(weight) +“ kg” ) ;**

**kgToLb( ref weight ) ;**

**Console.WriteLine( num + “ kg = ” + weight + “ lb” ) ;**

**Console.ReadKey( ) ;**

![image](images/7o.jpg)Press **Start** or **F5** to run the application and see the output featuring arguments passed to method parameters

![image](images/pgc63_1.jpg)

![image](images/hot.jpg)

Both the **num** and **weight** variables are initialized by the **getWeight( )** function. The value of **weight** is set in the function, as it is passed by reference. The variable **num** is initialized using the value returned from the function.

**Overloading methods**

Method “overloading” allows methods of the same name to happily co-exist in the same program, providing their parameters differ in number, data type, or both number and data type. The compiler matches a method call to the correct version of the method by recognizing its parameter number and data types – a process known as “method resolution”.

![image](images/pgc64_1.jpg)

Where a parameter represents the same value as that in another method, the parameters should have the same name. Parameters with the same name should appear in the same position in each method’s parameter list, but you should not use ref or out modifiers to overload methods.

It is useful to create overloaded methods in a custom class when their tasks are similar, yet subtly different. A class is created using the class keyword followed by a name of your choice. The methods of the class can then be added as function declarations within { } curly brackets following the class name.

In order to use methods of a custom class, a new instance of the class object must first be created using this syntax:

***Class-name instance-name = new( ) ;***

The methods can then be called by dot-suffixing the method name to the instance name.

![image](images/commonao.jpg)

Overload

![image](images/1o.jpg)Start a new **C# Console App** and name it “Overload”

**Console.Title = “Overload” ;**

![image](images/2o.jpg)Declare two floating-point variables and an instance of a class named “Compute” (to be created later in Step 7)

**double num ;**

**double area ;**

**Compute size = new( ) ;**

![image](images/3o.jpg)Add statements to initialize the first variable from input

**Console.Write( “Please Enter Dimension In Feet: “ ) ;**

**num = Convert.ToDouble( Console.ReadLine( ) ) ;**

![image](images/4o.jpg)Now, initialize the second variable by calling a method that accepts only one argument, then displays its value

**area = size.Zone( num ) ;**

**Console.WriteLine( “\nCircle:\t\tArea = “+area+“ sq.ft.” ) ;**

![image](images/forget.jpg)

Remember that the **ReadLine( )** method returns a **string** value – so this must be converted in order to perform arithmetic.

![image](images/5o.jpg)Assign a new value to the second variable by calling the function that accepts two arguments, then display its value

**area = size.Zone( num , num ) ;**

**Console.WriteLine( “Square:\t\tArea = “+area+“ sq.ft.” ) ;**

![image](images/6o.jpg)Assign a new value to the second variable by calling the function that accepts three arguments, then display its value

**area = size.Zone( num , num , ‘T’ ) ;**

**Console.WriteLine( “Triangle:\tArea = “+area+“ sq.ft.” ) ;**

**Console.ReadKey( ) ;**

![image](images/7o.jpg)Finally, add the custom class containing the three methods

**class Compute**

**{**

**public double Zone( double width )**

**{**

**double radius = width / 2 ;**

**return ( ( radius * radius ) * 3.141593 ) ;**

**}**

**public double Zone( double width, double height )**

**{**

**return ( width * height ) ;**

**}**

**public double** **Zone( double width, double height , char c )**

**{**

**return ( ( width / 2 ) * height ) ;**

**}**

**}**

![image](images/8o.jpg)Press **Start** or **F5** to run the application, then enter a number and see the output from the overloaded methods

![image](images/pgc65_1.jpg)

![image](images/forget.jpg)

The value passed to the **char c** parameter is never used here – it is included merely to determine which method should be called.

![image](images/snake.jpg)

The class block is a “type declaration”, whereas the rest of the code are “top-level statements”. Order is important, as top-level statements must precede any type declarations – so the class block must appear at the end of this code.

**Refactoring code**

![image](images/pgc66_1.jpg)

Functions can call themselves recursively, to repeatedly execute the statements contained in their function body – much like a loop. As with loops, a recursive function must contain an updater and a conditional test to call itself again, or stop repeating when a condition is met. The syntax of a recursive function looks like this:

***return-data-type function-name ( parameter-list )***

**{**

***statements-to-be-executed ;***

***updater ;***

***conditional-test-to-recall-or-exit ;***

**}**

The updater will change the value of a passed argument – so subsequent calls will pass the adjusted value back to the function:

![image](images/commonao.jpg)

Refactor

![image](images/1o.jpg)Start a new **C# Console App** and name it “Refactor”

Console.Title = “Refactor” ;

![image](images/2o.jpg)Add this recursive function to return the factorial value of a positive integer argument

**static int factorial( int num )**

**{**

**int result ;**

**if( num == 1 )**

**{**

**result = 1 ;**

**}**

**else**

**{**

**result = ( factorial( num - 1 ) * num ) ;**

**}**

**return result ;**

**}**

![image](images/3o.jpg)Next, add a method to display a range of integers and their computed factorial values

**static void computeFactorials( int num, int max )**

**{**

**while( num <= max )**

**{**

**Console.Write( “Factorial Of “ + num + “ : “ ) ;**

**Console.WriteLine( factorial( num ) ) ;**

**num++ ;**

**}**

**}**

![image](images/hot.jpg)

A factorial is the product of multiplying a positive integer by all lesser positive integers.

![image](images/hot.jpg)

The two calls to write output in Step 3 could be refactored into a single **WriteLine( )** call for greater efficiency.

![image](images/4o.jpg)Now, add statements to pass a range of argument values to be computed for display

**computeFactorials( 1 , 8 ) ;**

**Console.ReadKey( ) ;**

![image](images/5o.jpg)Press **Start** or **F5** to run the application to see the output

![image](images/pgc67_1.jpg)

The output lists factorial values (factorial 3 is 3x2x1=6, etc.) but the program can be optimized by refactoring the recursive factorial( ) method. This method does not need a variable if written with the ternary operator:

![image](images/6o.jpg)Edit the factorial( ) method listed in Step 2 to make it more efficient

**static int factorial( int num )**

**{**

**return ( num == 1 ) ? 1 : ( factorial( num - 1 ) * num ) ;**

**}**

![image](images/7o.jpg)Press **Start** or **F5** to run the application once more and see the same output, produced more efficiently

![image](images/pgc67_2.jpg)

![image](images/forget.jpg)

If you accidentally run an infinite recursive function, press the **Ctrl** + **C** keys to terminate the process.

![image](images/hot.jpg)

A recursive method generally uses more system resources than a loop – but it can make the code more readable. Modern compilers perform optimization, so it is better to focus on writing readable code.

**Summary**

![image](images/pgc68_1.jpg)

•A programmer-specified function is a modular section of code that can be called to execute its statements whenever required.

•It is easier to understand, maintain, re-use, and share modular program code that contains methods.

•A function declaration must at least specify a return data type and the function name.

•Methods not intended for use by other classes must be initialized in memory by the static keyword.

•Optionally, a function declaration may include a parameter list.

•Variables declared within a function have local scope, so are not accessible from outside that function.

•Arguments passed by value assign a copy of the original value to the function parameter, so the original will not be affected.

•Arguments passed by reference assign a memory location to the function parameter, so the original value will be affected.

•Arguments passed for output retrieve a value from the function and are useful to return more than one value.

•Method overloading allows methods of the same name to co-exist in the same program if their parameters differ.

•The compiler matches calls to overloaded methods by recognizing their parameter number and data types.

•Parameters representing the same values in overloaded methods should have the same name and the same position.

•The reference ref and output out modifiers should not be used with overloaded methods as their sole difference.

•Code can be refactored for optimum efficiency by reducing the number of variables and function calls.

•Recursive functions repeatedly execute their statements, so must contain an updater to stop repeating at some point.

**27**

**Handling strings**

***This chapter demonstrates how to manipulate and format text strings within C# programs.***

[**Discovering string features**](#chapter27.xhtml_sec212)

[**Manipulating strings**](#chapter27.xhtml_sec213)

[**Joining and comparing strings**](#chapter27.xhtml_sec214)

[**Copying and swapping strings**](#chapter27.xhtml_sec215)

[**Finding substrings**](#chapter27.xhtml_sec216)

[**Formatting strings**](#chapter27.xhtml_sec217)

[**Formatting date strings**](#chapter27.xhtml_sec218)

[**Summary**](#chapter27.xhtml_sec219)

**Discovering string features**

The C# String class library provides properties and methods that enable a program to easily discover features of a text string. Usefully, the String.IsNullOrWhiteSpace( ) and String.IsNullOrEmpty( ) methods can be used to validate user input. These are static methods, so are written dot-suffixed to the String class name.

![image](images/pgc70_1.jpg)

Other properties and methods operate on an “instance” of the class, so are written dot-suffixed to a string variable name. Instance methods can report string size and query its contents. The Length property returns an integer that is the number of characters within the string, including spaces. Additionally, the StartsWith( ), EndsWith( ), and Contains( ) methods can each accept a string argument to match within the string variable value. When a match is found, they return true, otherwise they return false:

![image](images/commonb1.jpg)

Features

![image](images/1bl.jpg)Start a new **C# Console App** and name it “Features”

**Console.Title = “Features” ;**

![image](images/2bl.jpg)Type these statements requesting user input to initialize a string variable

**Console.Write( “Please Enter Text: ” ) ;**

**string text = Console.ReadLine( ) ;**

![image](images/3bl.jpg)Next, add a conditional test to ensure the user entered input before hitting the **Enter** key

**if ( String.IsNullOrWhiteSpace( text ) )**

**{**

**Console.WriteLine( “\nERROR: No Text Found!” ) ;**

**}**

**else**

**{**

**// Statements to be inserted here (Steps 4-7).**

**}**

**Console.ReadKey( ) ;**

![image](images/4bl.jpg)Now, insert statements to report the length of the string

**Console.WriteLine( “\nThanks. You Entered:\n’”+text+”’” ) ;**

**Console.WriteLine( “\nText Length: ” + text.Length ) ;**

![image](images/5bl.jpg)Insert another statement to test how the string begins

**string query = text.StartsWith( “C#” ) ? “Does” : “Does Not” ;**

**Console.WriteLine( “Text ” + query + “ Start With ‘C#’” ) ;**

![image](images/hot.jpg)

String class methods can be written using the **String**. class prefix or its **string.** alias prefix – our examples use **String** to differentiate from the **string** data type.

![image](images/snake.jpg)

Note that some of these strings include **‘** single quotes within the outer **“** double quote marks.

![image](images/6bl.jpg)Next, insert a statement to test how the string ends

**query = text.EndsWith( “steps” ) ? “Does” : “Does Not” ;**

**Console.WriteLine( “Text ” + query + “ End With ‘steps’” ) ;**

![image](images/7bl.jpg)Now, insert a statement to test what the string contains

**query = text.Contains( “easy” ) ? “Does” : “Does Not” ;**

**Console.WriteLine( “Text ” + query + “ Contain ‘easy’” ) ;**

![image](images/8bl.jpg)Press **Start** or **F5** to run the application, and hit **Enter** without input to see the error message

![image](images/pgc71_1.jpg)

![image](images/9bl.jpg)Press **Start** or **F5** to run the application again, type input, then hit **Enter** to discover input string features

![image](images/pgc71_2.jpg)

![image](images/pgc71_3.jpg)

![image](images/forget.jpg)

Notice that the **?:** ternary operator is used here to assign an appropriate **string** value.

![image](images/hot.jpg)

String values are often referred to as “literals”, as they comprise characters to be read literally, as text.

![image](images/hot.jpg)

Methods with a **String.** (or **string.**) prefix are using the **String** class itself, whereas dot-suffixed methods use an “instance” object of the class – see [Chapter 30](#chapter30.xhtml).

**Manipulating strings**

The C# String class library provides methods that enable a program to manipulate text strings. The ToLower( ) and ToUpper( ) methods can be dot-suffixed to a string variable to change all characters within the string to lowercase, or to uppercase.

![image](images/pgc72_1.jpg)

Similarly, the TrimStart( ), TrimEnd( ), and Trim( ) methods can be used to remove whitespace or other characters from a string at its start, end, or both start and end. By default, these methods will remove whitespace from the string, but you can alternatively specify a character to be removed as an argument to the method.

Conversely, the PadLeft( ) and PadRight( ) methods can be used to add whitespace or other characters onto a string at its start or end. Their arguments must specify the total character length of the padded string, and a padding character unless default whitespace padding is required. If you want to add padding onto both start and end, the methods can be “chained” as PadLeft( ).PadRight( ) stating each padding length argument, and character if required:

![image](images/commonb1.jpg)

Manipulate

![image](images/1bl.jpg)Start a new **C# Console App** and name it “Manipulate”

**Console.Title = “Manipulate” ;**

![image](images/2bl.jpg)Type these statements requesting user input to initialize a string variable

**Console.Write( “Please Enter Text: ” ) ;**

**string text = Console.ReadLine( ) ;**

![image](images/3bl.jpg)Add statements to display the user input string and report its length

**Console.Write( “\nThanks. You Entered:\n’” + text + ”’” ) ;**

**Console.WriteLine( “\t\tText Length: ” + text.Length ) ;**

![image](images/4bl.jpg)Remove leading and trailing whitespace, then display the manipulated version and report its length

**text = text.Trim( ) ;**

**Console.Write( “\nTrimmed:\t’” + text + ”’” ) ;**

**Console.WriteLine( “\tText Length: ” + text.Length ) ;**

![image](images/5bl.jpg)Next, add statements to create and display an uppercase version of the trimmed string

**string upper = text.ToUpper( ) ;**

**Console.WriteLine( “\nUpperCase:\t’” + upper + ”’” ) ;**

![image](images/hot.jpg)

It is a good idea to always use **Trim( )** to remove spaces accidentally added by the user when typing input.

![image](images/6bl.jpg)Now, create and display a lowercase version of the trimmed string

**string lower = text.ToLower( ) ;**

**Console.WriteLine( “LowerCase:\t’” + lower + ”’” ) ;**

![image](images/7bl.jpg)Then, further manipulate all three strings to add whitespace and character padding

**upper = upper.PadLeft( 40 ) ;**

**lower = lower.PadRight( 40 , ‘#’ ) ;**

**text = text.PadLeft( 30 , ‘*’ ).PadRight( 40 , ‘*’ ) ;**

![image](images/8bl.jpg)Add statements to display all three strings to see the padded whitespace and padded characters

**Console.WriteLine( “\nPadded Left:\t’” + upper + “’” ) ;**

**Console.WriteLine( “Padded Right:\t’” + lower + “’” ) ;**

**Console.WriteLine( “Padded Both:\t’” + text + “’” ) ;**

![image](images/9bl.jpg)Finally, add statements to display trimmed versions of two padded strings

**Console.WriteLine( “\nTrimmed Start:\t’” +**

**upper.TrimStart( ) + “’” ) ;**

**Console.WriteLine( “Trimmed End:\t’” +**

**text.TrimEnd( ‘*’ ) + “’” ) ;**

**Console.ReadKey( ) ;**

![image](images/10bl.jpg)Press **Start** or **F5** to run the application and enter a string with leading and trailing space to see it manipulated

![image](images/pgc73_1.jpg)

![image](images/forget.jpg)

Here, all three strings are expanded to a total width of 40 characters.

![image](images/hot.jpg)

You can also specify multiple characters to be trimmed as a comma-separated list of arguments to the **TrimStart()**, **TrimEnd()**, or **Trim()** methods.

![image](images/snake.jpg)

When padding both left and right you must individually specify by how much to expand the string in each direction – in this case, expanding from 20 to 30 characters left, then from 30 to 40 characters right.

**Joining and comparing strings**

When the + operator is used to concatenate (join) strings in an assignment, the combined strings get stored in the string variable. But when used in the Write( ) or WriteLine( ) methods, the strings are only combined in output – the variable values are unchanged.

![image](images/pgc74_1.jpg)

The C# String class library provides a String.Concat( ) method that can be used to join strings as an alternative to using the + operator. This method accepts a comma-separated list of string arguments to be joined into a single string.

Similarly, the String.Join( ) method can also be used to join strings as an alternative to using the + operator. This, too, accepts a comma-separated list of string arguments to be joined, but its first argument usefully specifies a separator string. It places this separator between each string argument in the joined string. The separator might be a single space to separate words, or perhaps an HTML tag to separate text, or any other string value.

String comparisons can be made for alphabetic order by specifying two string arguments to the String.Compare( ) method. This returns an integer denoting whether the alphabetic relationship of the first string to the second is before (-1), after (1), or equal (0). There is also a CompareTo( ) method that provides the same results, but this can be dot-suffixed onto the first string, and the second string specified as its argument.

As with numeric comparisons, the == operator can be used to test for string equality. Alternatively, the Equals( ) method can be dot-suffixed onto the first string, and the second string specified as its argument. Either will return a true or false Boolean result.

![image](images/commonb1.jpg)

Joined

![image](images/1bl.jpg)Start a new **C# Console App** and name it “Joined”

**Console.Title = “Joined” ;**

![image](images/2bl.jpg)Type this statement to create and initialize a **string** array variable simply named “a”

**string [ ] a = new string[ 3 ] { “Alpha”, ”Bravo”, ”Charlie” } ;**

![image](images/3bl.jpg)Next, assign a concatenated version of the first two array element values to a string variable and display its value

**string s = String.Concat( a[0] , a[1] ) ;**

**Console.WriteLine( “Concatenated:\t” + s ) ;**

![image](images/hot.jpg)

The examples in the C# section of this book use the **+** operator for concatenation rather than **String.Concat( )** as it provides better readability without any loss of performance.

![image](images/4bl.jpg)Assign a joined version of the first two array elements and space separator to the string variable, then display its value

**s = String.Join( “ “ , a[0] , a[1] ) ;**

**Console.WriteLine( “Joined:\t\t” + s ) ;**

![image](images/5bl.jpg)Assign a joined version of all three array elements and tag separator to the string variable, then display its value

**s = String.Join( “<br>“ , a ) ;**

**Console.WriteLine( “\nHTML:\t” + s +”\n” ) ;**

![image](images/6bl.jpg)Next, add statements to compare, in turn, all three array elements for alphabetic order

**int num = String.Compare( a[0] , a[1] ) ;**

**Console.WriteLine( a[0] + ” v “ + a[1] + ”:\t” + num ) ;**

**num = String.Compare( a[2] , a[1] ) ;**

**Console.WriteLine( a[2] + ” v “ + a[1] + ”:\t” + num ) ;**

**num = a[1].CompareTo( a[1] ) ;**

**Console.WriteLine( a[1]+ ” v “+a[1]+”:\t” + num+“\n” ) ;**

![image](images/7bl.jpg)Finally, test the array element values for equality

**bool flag = ( a[0] == a[1] ) ;**

**Console.WriteLine( a[0]+” == “+a[1]+”:\t\t” + flag ) ;**

**flag = a[2].Equals( a[2] ) ;**

**Console.WriteLine( a[2]+” == “+a[2]+”:\t\t” + flag ) ;**

**Console.ReadKey( ) ;**

![image](images/8bl.jpg)Press **Start** or **F5** to run the application to see the joined strings and comparison results

![image](images/pgc75_1.jpg)

![image](images/hot.jpg)

Notice how only the array name needs to be specified as the argument to join all three array elements.

![image](images/hot.jpg)

You can add or remove the \t escape sequences to format the output to your liking.

![image](images/forget.jpg)

Two alternative methods are used here to compare strings and to test for equality.

**Copying and swapping strings**

The C# String class library provides a String.Copy( ) method that can be used to copy one string to another string as an alternative to using the = assignment operator. This method accepts the string to be copied as its argument. Perhaps more usefully, the CopyTo( ) method can be dot-suffixed onto a string variable to copy its contents into a char character array. This requires four arguments to specify the index number from which to start copying in the source string, the name of the char array, the index number at which to start copying in the destination char array, and the number of characters to copy.

![image](images/pgc76_1.jpg)

Other methods can be dot-suffixed to a string variable to swap its contents. The Remove( ) method requires an integer argument to specify the index number at which to begin removing characters from the string. This will remove all characters from the specified index position up to the end of the string, unless you add a second argument to specify the number of characters to be removed.

Conversely, the Insert( ) method requires an integer argument to specify the index number at which to begin inserting characters into the string, and an argument specifying the string to insert. The Replace( ) method simply requires two string arguments to specify a substring to seek within the string, and a string to replace that substring when a match is found:

![image](images/commonb1.jpg)

Copied

![image](images/1bl.jpg)Start a new **C# Console App** and name it “Copied”

**Console.Title = “Copied” ;**

![image](images/2bl.jpg)Type these statements to create and initialize two string variables with the names of two Maserati car models

**string car1 = “Ghibli” ;**

**string car2 = “GranTurismo” ;**

![image](images/3bl.jpg)Next, display the original values contained in each variable

**Console.Write( “Original:” ) ;**

**Console.WriteLine( “\tCar 1: ”+ car1 +“ \t\tCar 2: “ + car2 ) ;**

![image](images/4bl.jpg)Now, copy the value of the second string variable into the first string variable and display their modified values

**car1 = String.Copy( car2 ) ;**

**Console.Write( “\nCopied:” ) ;**

**Console.WriteLine( “\tCar 1: ”+ car1 + “\tCar 2: “ + car2 ) ;**

![image](images/hot.jpg)

Copying with an **=** assignment produces two **string** variables that contain the same value and reference the same memory location, whereas copying with the **String.Copy( )** method produces two **string** variables that contain the same value but reference different memory locations.

![image](images/5bl.jpg)Initialize an integer variable with the length of the first string variable, then create a character array of that length

**int num = car1.Length ;**

**char [ ] model = new char [ num ] ;**

![image](images/6bl.jpg)Next, copy the first string variable into the character array, then display a space-separated list of the element contents

**car1.CopyTo( 0 , model , 0 , num ) ;**

**Console.Write( “\nCharacter Array:” ) ;**

**foreach( char c in model ) { Console.Write( c + “ “ ) ; }**

![image](images/7bl.jpg)Now, remove the end of the first string variable, starting from its fifth element, and display the modified value

**car1 = car1.Remove( 4 ) ;**

**Console.WriteLine( “\n\nRemoved... \tCar 1: ” + car1 ) ;**

![image](images/8bl.jpg)Insert two strings into the first string variable, at its beginning and end, then display the modified value

**car1 = car1.Insert( 0 , “Maserati ” ) ;**

**car1 = car1.Insert( 13 , “Cabrio” ) ;**

**Console.WriteLine( “\nInserted... \tCar 1: ” + car1 ) ;**

![image](images/9bl.jpg)Finally, replace a substring within the first string variable, and once more display the modified value

**car1 = car1.Replace( “GranCabrio” , “Quattroporte” ) ;**

**Console.WriteLine( “\nReplaced... \tCar 1: ” + car1 ) ;**

**Console.ReadKey( ) ;**

![image](images/10bl.jpg)Press **Start** or **F5** to run the application to see the copied and swapped strings

![image](images/pgc77_1.jpg)

![image](images/snake.jpg)

The **char** array must be of the same size as the **string** to be copied – use the string’s **Length** property to specify the size of the **char** array.

![image](images/forget.jpg)

The fifth element of an array is at index position 4 in a zero-based index.

**Finding substrings**

The C# String class library provides a number of methods that can be dot-suffixed to a string variable to seek a string within a string (i.e. a “substring”). The IndexOf( ) method requires the substring as its argument and, if found, returns the index position of the substring within the searched string. Otherwise, it will return -1. The IndexOf( ) method searches forward, from left-to-right, and returns the index position of the first occurrence of the substring. It has a companion LastIndexOf( ) method that works in just the same way, but searches backward, from right-to-left.

![image](images/pgc78_1.jpg)

Similarly, there is an IndexOfAny( ) method and its companion LastIndexOfAny( ) method that require a character array argument. These seek any character of the specified array within a string, and return the index position of the first occurrence, or -1 otherwise.

You can also dot-suffix a Substring( ) method to a string variable if you want to extract a copy of a substring from within that string. This method requires two arguments to specify the index position at which to begin copying, and the number of characters to copy:

![image](images/commonb1.jpg)

Substring

![image](images/1bl.jpg)Start a new **C# Console App** and name it “Substring”

**Console.Title = “Substring” ;**

![image](images/2bl.jpg)Add this function to report the result of a substring search

**static void report( int pos , string sub )**

**{**

**if( pos != -1 )**

**{ Console.WriteLine( “‘“ + sub + ”’ Found At “ + pos ) ; }**

**else**

**{ Console.WriteLine( “‘“ + sub + ”’ Not Found!“ ) ; }**

**}**

![image](images/3bl.jpg)Now, initialize a string variable, then display its value and length

**string text = “My dog is a cute dog” ;**

**Console.WriteLine( text + ”\tLength: “ + text.Length ) ;**

![image](images/4bl.jpg)Next, request user input to initialize another string variable with a substring to seek

**Console.WriteLine( “\nPlease Enter A Substring To Seek: ” ) ;**

**string sub = Console.ReadLine( ) ;**

![image](images/forget.jpg)

The position reported when a substring is found is the index position of the first character of that substring within the searched string – whether searching forward or backward.

![image](images/5bl.jpg)Create a character array and copy the entire substring value into the character array

**char [ ] arr = new char[ sub.Length ] ;**

**sub.CopyTo( 0 , arr , 0 , sub.Length ) ;**

![image](images/6bl.jpg)Then, seek the first occurrence of the substring and call the function to report the search result

**int pos = text.IndexOf( sub ) ;**

**report( pos , sub ) ;**

![image](images/7bl.jpg)Now, seek the last occurrence of the substring and report the result

**pos = text.LastIndexOf( sub ) ;**

**report( pos , sub ) ;**

![image](images/8bl.jpg)Next, seek the first occurrence of any character of the substring and report the result

**pos = text.IndexOfAny( arr ) ;**

**report( pos , text.Substring( pos , 1 ) ) ;**

![image](images/9bl.jpg)Finally, seek the last occurrence of any character of the substring and report the result

**pos = text.LastIndexOfAny( arr ) ;**

**report( pos , text.Substring( pos , 1 ) ) ;**

**Console.ReadKey( ) ;**

![image](images/10bl.jpg)Press **Start** or **F5** to run the application, then enter a substring to seek and see the reported results

![image](images/pgc79_1.jpg)

![image](images/pgc79_2.jpg)

![image](images/forget.jpg)

The **CopyTo( )** method is described and demonstrated in the previous example [here](#chapter27.xhtml_sec215).

![image](images/hot.jpg)

Notice that a copy of the located character is extracted from the original **string** using the **Substring( )** method for output in the report.

**Formatting strings**

![image](images/pgc80_1.jpg)

In C# every object has a ToString( ) method that returns a string representation of that object. This means that the ToString( ) method can be dot-suffixed to any numeric variable to get its value represented in string format. The ToString( ) method can, optionally, accept a string argument to specify how the string version should be formatted. Common specifiers are listed below:

| **Specifier** | **Returns** |
| **G** | General |
| **F** | Fixed Point |
| **N** | Number (with comma-separated thousands) |
| **C** | Currency (prevailing on your system) |
| **P** | Percentage (multiplied by 100) |
| **00.0000** | Zero Padding |

The C# **String** class library provides a **String.Format( )** method that uses the same specifiers to also produce values represented in **string** format. This requires a **string** argument to specify the format, which may include “placeholders”, and an argument list to be substituted for each placeholder in the output **string**.

Each placeholder can be numbered sequentially (starting at zero) within { } braces, to match the list position of the substitution argument. For example, {0} matches the first argument in the substitution argument list, {1} matches the second, and so on. Additionally, the number may be followed by a : colon and one of the format specifiers in the table above – to specify how the substituted value should appear in its string – for example, {0:G}.

Data strings that contain separators, such as a comma-separated list of data retrieved from a database query, can be easily broken into individual items of data by dot-suffixing the Split( ) method to a string variable. The individual strings can be assigned to a string array variable, and could then be formatted in output by the String.Format( ) method if required.

![image](images/hot.jpg)

The C# specifications provide further string formatting specifier options in addition to the commonly used ones shown here.

![image](images/hot.jpg)

Multiple placeholders in one string can be numbered alike – if you want each one to be substituted by the same list argument value.

![image](images/commonb1.jpg)

Format

![image](images/1bl.jpg)Start a new **C# Console App** and name it “Format”

**Console.Title = “Format” ;**

![image](images/2bl.jpg)Initialize a numeric variable, then use the ToString() method to output its value as a currency string format

**double sum = 2500 ;**

**Console.WriteLine( “Currency String: “ + sum.ToString( “C” ) ) ;**

![image](images/3bl.jpg)Next, use the String.Format() method to output the same numeric value in various common string formats

**Console.Write( String.Format( “\nGeneral:\t {0:G}” , sum ) ) ;**

**Console.Write( String.Format( “\nFixed Point:\t {0:F}”, sum ) ) ;**

**Console.Write( String.Format( “\nNumber:\t\t {0:N}” , sum ) ) ;**

**Console.Write( String.Format( “\nCurrency:\t {0:C}” , sum ) ) ;**

![image](images/4bl.jpg)Now, reduce the numeric value, then output it in a percentage string format and with padded zeros

**sum /= 1000 ;**

**Console.Write( String.Format( “\nPercentage:\t {0:P}”, sum ) ) ;**

**Console.Write**

**( String.Format( “\nZero Padded:\t {0:00.0000} \n”, sum ) ) ;**

![image](images/5bl.jpg)Then, create a comma-separated string list and split it into individual elements of a string array variable for output

**string data = “Mike,McGrath,Author” ;**

**string [ ] items = data.Split( ‘,’ ) ;**

**foreach ( string item in items )**

**{ Console.Write( String.Format( “\n* {0}” , item ) ) ; }**

**Console.ReadKey( ) ;**

![image](images/6bl.jpg)Press **Start** or **F5** to see the formatted string output

![image](images/pgc81_1.jpg)

![image](images/hot.jpg)

The specifier letters may be written as either uppercase or lowercase.

![image](images/snake.jpg)

The argument to the **Split( )** method must be a single **char** character – enclosed in single quotes.

![image](images/forget.jpg)

You can use the **+** concatenation operator for formatting, but many prefer **String.Format( )** for easily readable code.

**Formatting date strings**

The C# DateTime class library provides methods and properties to easily work with dates and times. Its Now property returns a DateTime object of the current local date and time of your system. Alternatively, you can create a DateTime object using the new keyword, and specifying a date and time as a comma-separated list of arguments. Many methods and properties can be dot-suffixed to any DateTime object to specify its format, or to extract specific components of the date or time, or to modify its value. For example, the DayOfWeek property supplies the day name, the ToShortString( ) method supplies the date in number form, and the AddYears( ) method can modify the year component.

![image](images/pgc82_1.jpg)

The String.Format( ) method, introduced in the previous example [here](#chapter27.xhtml_sec217), also has these specifiers that can be used to determine the format of dates and times in output:

| **Specifier** | **Returns** | **Example** |
| **d** | Short date | **7/4/2023** |
| **D** | Long date | **Tuesday, July 4, 2023** |
| **t** | Short time | **8:15 AM** |
| **T** | Long time | **8:15:30 AM** |
| **f** | Full datetime | **Tuesday, July 4, 2023 8:15 AM** |
| **F** | Full+seconds | **Tuesday, July 4, 2023 8:15:30 AM** |
| **M** | Month+day | **July 4** |
| **Y** | Month+year | **July 2023** |
| **dd** | Day number | **04** |
| **dddd** | Day name | **Tuesday** |
| **HH** | Hour 0-23 | **08** |
| **mm** | Minute | **15** |
| **ss** | Second | **30** |
| **YYYY** | Year | **2023** |

![image](images/forget.jpg)

IntelliSense is an intelligent code completion tool that is built into Visual Studio. You can use IntelliSense to choose methods and properties – for example, type **DateTime.Now.** and select from the pop-up list that appears.

![image](images/hot.jpg)

The C# specifications provide further date and time formatting specifier options in addition to the commonly used ones shown here.

![image](images/commonb1.jpg)

DateFormat

![image](images/1bl.jpg)Start a new **C# Console App** and name it “DateFormat”

**Console.Title = “DateFormat” ;**

![image](images/2bl.jpg)Initialize a DateTime object and display its value

**DateTime now = DateTime.Now ;**

**Console.Write( “Current Date And Time: “+ now ) ;**

![image](images/3bl.jpg)Next, display specific components of the DateTime object

**Console.Write( “\nDay Name: “+ now.DayOfWeek ) ;**

**Console.Write( “\nDate Only: “+ now.ToShortDateString( ) ) ;**

**Console.Write( “\nTime Only: “+ now.ToShortTimeString( ) ) ;**

![image](images/4bl.jpg)Modify the DateTime object and display its new value

**now = now.AddYears( 4 ) ;**

**Console.Write( “\n\nFuture Date: “+ now ) ;**

![image](images/5bl.jpg)Now, create a new DateTime object and display its value

**DateTime dt = new DateTime( 2025, 7, 4, 8, 15, 30 ) ;**

**Console.Write( “\n\nSet Date And Time: {0:f}“, dt ) ;**

![image](images/6bl.jpg)Display specific components of the new DateTime object

**Console.Write( “\nDay Name: {0:dddd}“, dt ) ;**

**Console.Write( “\nLong Date: {0:D}“, dt ) ;**

**Console.Write( “\nLong Time: {0:T}“, dt ) ;**

**Console.ReadKey( ) ;**

![image](images/7bl.jpg)Press **Start** or **F5** to run the application and see the formatted date and time output

![image](images/pgc83_1.jpg)

![image](images/hot.jpg)

You need only specify the date components when creating a new **DateTime** object – the time will automatically be set to 12:00 AM (midnight).

**Summary**

![image](images/pgc84_1.jpg)

•Class library static methods, such as String.IsNullOrEmpty( ), are dot-suffixed onto the String class library name.

•String values can be joined using the String.Concat( ) and String. Join( ) methods, or by using the + concatenation operator.

•String comparisons can be made for alphabetic order using the String.Compare( ) method.

•A value can be copied from one string variable to another using the String.Copy( ) method, or the = assignment operator.

•The String.Format( ) method can be used to format both numeric and date strings in output.

•The DateTime class library provides methods and properties, such as Now, to work with date and time strings.

•Instance methods and properties, such as Contains( ) and Length, are dot-suffixed onto string variable names.

•The character case of a string value can be changed using the ToLower( ) and ToUpper( ) methods.

•Whitespace or other characters can be removed from a string value using the TrimStart( ), TrimEnd( ), and Trim( ) methods.

•Whitespace or other characters can be added to a string value using the PadLeft( ) and PadRight( ) methods.

•String comparisons can be made using the CompareTo( ) and Equals( ) methods, or the == equality operator.

•A string value can be copied from a string variable into a char array using the CopyTo( ) method.

•The contents of a string variable can be swapped using the Remove( ), Insert( ), and Replace( ) methods.

•A substring can be sought using IndexOf( ), LastIndexOf( ), IndexOfAny( ), LastIndexOfAny( ), and Substring( ) methods.

•Every object has a ToString( ) method that returns a string representation, which can be formatted in output.

**28**

**Accessing files**

***This chapter demonstrates how C# programs can store data in text files, and retrieve data from text files.***

[**Writing a file**](#chapter28.xhtml_sec220)

[**Appending to a file**](#chapter28.xhtml_sec221)

[**Reading text and lines**](#chapter28.xhtml_sec222)

[**Streaming lines**](#chapter28.xhtml_sec223)

[**Manipulating input and output**](#chapter28.xhtml_sec224)

[**Summary**](#chapter28.xhtml_sec225)

**Writing a file**

The C# **System.IO.File** class library provides methods that enable a program to easily write text into a file on your computer.

![image](images/pgc86_1.jpg)

The File.WriteAllText( ) method simply requires two arguments to specify the text file path and the string to write. Backslash characters in the path string must be escaped to avoid an error.

If you would like to ensure the specified text file does not already exist, you can first test for its existence by specifying its path as the argument to the **File.Exists( )** method. This will return **true** when the file is found, otherwise it will return **false**.

In order to ensure the text file was written successfully, it is worthwhile wrapping the **File.WriteAllText( )** call in a **try**-**catch** block. A statement confirming success can be included in the **try** part of the block, and a statement to advise of failure can be included in the **catch** part of the block:

![image](images/commonav.jpg)

WriteText

![image](images/1v.jpg)Start a new **C# Console App** and name it “WriteText”

****Console.Title** = “WriteText” ;**

![image](images/2v.jpg)Add these statements to initialize two variables – inserting your own user name where indicated in the path

**// Edit the line below to include your own user name.**

**string path = “C:\\Users\\*username*\\Desktop\\poem.txt” ;**

**string poem = “\r\n\tI never saw a man who looked” ;**

**poem += “\r\n\tWith such a wistful eye” ;**

**poem += “\r\n\tUpon that little tent of blue” ;**

**poem += “\r\n\tWhich prisoners call the sky” ;**

![image](images/3v.jpg)Next, add a statement to test if a file already exists of the specified path and filename

**if( File.Exists( path ) )**

**{**

**Console.WriteLine( “File Already Exists: “ + path ) ;**

**}**

**else**

**{**

**// Statements to be inserted here (Step 4).**

**}**

**Console.ReadKey( ) ;**

![image](images/forget.jpg)

The **\r\n\t** escape sequence is a carriage return, a newline, and a tab.

![image](images/4v.jpg)Now, insert statements that attempt to write a text file and confirm success, or advise of failure

**try**

**{**

**File.WriteAllText( path , poem ) ;**

**Console.WriteLine( “File Written: “ + path ) ;**

**}**

**catch( Exception error )**

**{**

**Console.WriteLine( error.Message ) ;**

**}**

![image](images/5v.jpg)Press **Start** or **F5** to run the application and see a text file written on your Desktop

![image](images/pgc87_1.jpg)

![image](images/pgc87_2.jpg)

![image](images/6v.jpg)Run the app again – to see that the file already exists

![image](images/pgc87_3.jpg)

![image](images/7v.jpg)Edit the path to a non-existing location, then run the app once more to see the error message

![image](images/pgc87_4.jpg)

![image](images/hot.jpg)

Catching exceptions with the **try**-**catch** block is fully described in [Chapter 29](#chapter29.xhtml), dealing with problem solving – see [here](#chapter29.xhtml_sec230).

**Appending to a file**

The C# **System.IO.File** class library provides a **WriteAllLines( )** method that can be used to write the contents of a **string** array to a text file, with each element appearing on a separate line, and a **try**-**catch** block can ensure the text file was written successfully.

![image](images/pgc88_1.jpg)

Additionally, the **System.IO.File** class has an **AppendAllText( )** method, which can be used to add text to an existing file, and the **File.Exists( )** method can ensure that the file first exists:

![image](images/commonav.jpg)

AppendText

![image](images/1v.jpg)Start a new **C# Console App** and name it “AppendText”

****Console.Title** = “AppendText” ;**

![image](images/2v.jpg)Add these statements to initialize three variables – inserting your own user name where indicated in the path

**string path = “C:\\Users\\username\\Desktop\\oscar.txt” ;**

**string [ ] poem = new string [ ]**

**{**

**“\tIn Debtors’ Yard the stones are hard” ,**

**“\tAnd the dripping wall is high”**

**} ;**

**string attrib = “\r\n\tThe Ballad Of Reading Gaol ” ;**

**attrib += “(Oscar Wilde 1898)” ;**

![image](images/3v.jpg)Next, add a statement to test if a file already exists of the specified path and filename

**if( File.Exists( path ) )**

**{**

**// Statements to be inserted here (Step 4).**

**}**

**else**

**{**

**// Statements to be inserted here (Step 5).**

**}**

**Console.ReadKey( ) ;**

![image](images/4v.jpg)Now, insert statements that attempt to append text if the file already exists, and advise of success

**File.AppendAllText( path , attrib ) ;**

**Console.WriteLine( “Appended To File: “ + path ) ;**

![image](images/forget.jpg)

The **\r\n** character return, newline escape sequences can be omitted from the **string** array, as the **WriteAllLines( )** method automatically writes each element on new lines.

![image](images/5v.jpg)Then, insert statements that attempt to write a text file and confirm success, or advise of failure

**try**

**{**

**File.WriteAllLines( path , poem ) ;**

**Console.WriteLine( “File Written: “ + path ) ;**

**}**

**catch( Exception error )**

**{**

**Console.WriteLine( error.Message ) ;**

**}**

![image](images/6v.jpg)Press **Start** or **F5** to run the application and see a text file written on your Desktop, or see an error message

![image](images/pgc89_1.jpg)

![image](images/pgc89_2.jpg)

![image](images/7v.jpg)Run the application once more and see a confirmation appear and see text now get appended to the file

![image](images/pgc89_3.jpg)

![image](images/pgc89_4.jpg)

![image](images/hot.jpg)

As with **WriteAllText( )**, the **WriteAllLines( )** method requires the text file path and **string** to write as its arguments.

![image](images/hot.jpg)

There is also an **AppendAllLines( )** method that can be used to add the contents of a **string** array to a file.

![image](images/snake.jpg)

After its first run, this application will append text each time it is run.

**Reading text and lines**

The C# **System.IO.File** class library provides a **ReadAllText( )** method that can be used to read text from an existing file and assign its entire contents to a **string** variable. The **File.Exists( )** method can ensure that the text file first exists, and a **try**-**catch** block can ensure the file was read successfully.

![image](images/pgc90_1.jpg)

Additionally, the **System.IO.File** class has a **ReadAllLines( )** method, which can be used to assign each line of a text file to an individual element of a **string** array:

![image](images/commonav.jpg)

ReadText

![image](images/1v.jpg)Start a new **C# Console App** and name it “ReadText”

**Console.Title = “ReadText” ;**

![image](images/2v.jpg)Add this statement to initialize a variable – inserting your own user name where indicated in the path

**string path = “C:\\Users\\*username*\\Desktop\\word.txt” ;**

![image](images/3v.jpg)Next, add a statement to test if a file already exists of the specified path and filename

**if( File.Exists( path ) )**

**{**

**// Statements to be inserted here (Step 4).**

**}**

**else**

**{**

**Console.WriteLine( “File Not Found: “ + path ) ;**

**}**

**Console.ReadKey( ) ;**

![image](images/4v.jpg)Now, insert a statement to display a message if the file cannot be read successfully

**try**

**{**

**// Statements to be inserted here (Steps 5 and 6).**

**}**

**catch( Exception error )**

**{**

**Console.WriteLine( error.Message ) ;**

**}**

![image](images/snake.jpg)

When a text file is read into a **string** array, the array’s **Length** property, which returns the number of its elements, will represent the number of lines read – including empty lines!

![image](images/5v.jpg)Then, insert statements to assign the text file contents to a variable and display its value

**string text = File.ReadAllText( path ) ;**

**Console.WriteLine( “File Read: “ + path + “\n” ) ;**

**Console.WriteLine( text + “\n” ) ;**

![image](images/6v.jpg)Finally, insert statements to assign the text file contents to an array variable and display each element with a counter

**string [ ] lines = File.ReadAllLines( path ) ;**

**int num = 1 ;**

**foreach( string line in lines )**

**{**

**Console.WriteLine( num + “ : ” + line ) ;**

**num++ ;**

**}**

![image](images/7v.jpg)Open a text editor such as Notepad, and create a multi-line text file named “word.txt” on your Desktop

![image](images/pgc91_1.jpg)

![image](images/8v.jpg)Press **Start** or **F5** to run the application and see a text file read from your Desktop, or see an error message

![image](images/pgc91_2.jpg)

![image](images/forget.jpg)

The text file’s invisible newline and tab characters are preserved when read by the **ReadAllText( )** method, but only the invisible tab characters are preserved when it is read by the **ReadAllLines( )** method.

![image](images/hot.jpg)

Remove the text files’ Read permission on your system and run the application again to see an “Access to path denied” message.

**Streaming lines**

![image](images/pgc92_1.jpg)

The **File.WriteAllText( )** and **File.AppendAllText( )** methods are simple to use but provide few options. The **System.IO.StreamWriter** class also provides object methods that can be used to write text to a file, and these provide more options. An instance of a **StreamWriter** object must first be created using the **new** keyword, and the text file path specified as an argument to its “constructor” method, like this:

**StreamWriter *name* = new StreamWriter( *path* ) ;**

Methods such as **Write( )** and **WriteLine( )** can then be dot-suffixed to the instance name. A **StreamWriter** instance is disposable, so its statements are best enclosed within a **using** construct to ensure it is removed from memory upon completion, like this:

**using ( StreamWriter *name* = new StreamWriter( *path* ) )**

**{**

**// *Statements.***

**}**

The **using** construct can also be wrapped in a **try**-**catch** block, to ensure the text file was written successfully.

Optionally, the **StreamWriter** constructor can accept a second argument of **true** to append to existing text:

![image](images/commonav.jpg)

WriteStream

![image](images/1v.jpg)Start a new **C# Console App** and name it “WriteStream”

**Console.Title = “WriteStream” ;**

![image](images/2v.jpg)Add these statements to initialize three variables – inserting your own user name where indicated in the path

**string path = “C:\\Users\\*username*\\Desktop\\robert.txt” ;**

**string[ ] poem = new string [ ]**

**{**

**“\tThis truth finds honest Tam o’ Shanter” ,**

**“\tAs he from Ayr one night did canter” ,**

**“\tOld Ayr, which never a town surpasses” ,**

**“\tFor honest men and bonny lasses.”**

**} ;**

**string attrib = “\n\tTam o’ Shanter (Robert Burns 1790)” ;**

![image](images/forget.jpg)

The **using** keyword has different meanings according to its context.

![image](images/3v.jpg)Next, add a statement to display a message if the file cannot be written successfully

**try**

**{**

**// Statements to be inserted here (Steps 4 and 5).**

**}**

**catch( Exception error )**

**{ Console.WriteLine( error.Message ) ; }**

**Console.ReadKey( ) ;**

![image](images/4v.jpg)Now, insert statements that attempt to write the contents of the variable array into a text file

**using ( StreamWriter writer = new StreamWriter( path ) )**

**{**

**foreach( string line in poem )**

**{ writer.WriteLine( line ) ; }**

**}**

![image](images/5v.jpg)Finally, insert statements that attempt to append the contents of the regular variable into a text file

**using ( StreamWriter writer =**

**new StreamWriter( path, true ) )**

**{**

**writer.WriteLine( attrib ) ;**

**Console.WriteLine( “File Written: “ + path ) ; }**

**}**

![image](images/6v.jpg)Press **Start** or **F5** to run the application and see a text file written on your Desktop, or see an error message

![image](images/pgc93_1.jpg)

![image](images/pgc93_2.jpg)

![image](images/hot.jpg)

The **using** construct ensures the **StreamWriter** is disposed of when its operations complete, so the same name can be used for the new object.

![image](images/hot.jpg)

Try writing this file into a non-existent folder to see an “Access to path denied” message.

**Manipulating input and output**

![image](images/pgc94_1.jpg)

The **System.IO.StreamReader** class provides object methods that can be used to read text from a file. An instance of a **StreamReader** object must first be created using the **new** keyword, and the text file path specified as an argument to its “constructor”:

**StreamReader *name* = new StreamReader( *path* ) ;**

Methods such as **Read( )** and **ReadLine( )** can then be dot-suffixed to the instance name. A **StreamReader** instance is disposable, so its operation statements are best enclosed within a **using** construct to ensure it is removed from memory when the operation has completed. The **using** construct can also be wrapped in a **try**-**catch** block, to ensure the text file was read successfully.

Text read by a **StreamReader** object can be manipulated to change its format before output, for example, to manipulate cells exported from an Excel spreadsheet as comma-separated values:

![image](images/pgc94_2.jpg)

![image](images/pgc94_3.jpg)

![image](images/commonav.jpg)

ReadStream

![image](images/1v.jpg)Start a new **C# Console App** and name it “ReadStream”

**Console.Title = “ReadStream” ;**

![image](images/2v.jpg)Add a statement to initialize a variable – inserting your own user name where indicated in the path

**string path = “C:\\Users\\*username*\\Desktop\\TopFive.csv” ;**

![image](images/3v.jpg)Next, add a statement to display a message if the file cannot be read successfully

**try**

**{**

**// Statements to be inserted here (Step 4).**

**}**

**catch( Exception error )**

**{ Console.WriteLine( error.Message ) ; }**

**Console.ReadKey( ) ;**

![image](images/4v.jpg)Now, insert statements that attempt to read the contents of the text file into a variable, line by line

**using ( StreamReader reader = new StreamReader( path ) )**

**{**

**string line ;**

**while( ( line = reader.ReadLine( ) ) != null )**

**{**

**// Statements to be inserted here (Steps 5-6).**

**}**

**}**

![image](images/5v.jpg)Insert statements to modify the case of the column headers and amend an artist name

**if( line.IndexOf( “Rank” ) != -1 ) line = line.ToUpper( ) ;**

**if( line.IndexOf( “Sia” ) != -1 ) line += “ ft.Sean Paul” ;**

![image](images/6v.jpg)Finally, insert statements that display the content of just two columns, formatted for alignment

**string [ ] sub = line.Split( ‘,’ ) ;**

**line = String.Format( ( “{0,-30}{1,-20}”, sub[1], sub[2] ) ;**

**Console.WriteLine( line ) ;**

![image](images/7v.jpg)Press **Start** or **F5** to run the application and see the manipulated output from the file content

![image](images/pgc95_1.jpg)

![image](images/hot.jpg)

When the **ReadLine( )** method reaches the end of the file being read, it returns a **null** value.

![image](images/hot.jpg)

The **String.Format( )** placeholders specify character widths as negative numbers to align strings to the left.

**Summary**

![image](images/pgc96_1.jpg)

•The System.IO.File class provides methods to easily read or write text files on your computer.

•The System.IO.File.WriteAllText( ) method requires two arguments to specify a file path and content to write there.

•The System.IO.File.Exists( ) method will determine if the file specified as its argument already exists.

•It is recommended all read or write operations be wrapped in a try-catch block to report when an attempted operation fails.

•The System.IO.File.WriteAllLines( ) method can write the element content of a string array as separate lines of a file.

•The System.IO.File.AppendAllText( ) method requires two arguments to specify a file path and content to append there.

•The System.IO.File.ReadAllText( ) method can be used to assign the entire content of a text file to a string variable.

•The System.IO.File.ReadAllLines( ) method can assign individual lines of a text file to elements of a string array.

•The System.IO.StreamWriter class provides object methods to write text files on your computer.

•The System.IO.StreamReader class provides object methods to read from text files on your computer.

•An instance of a StreamReader object or StreamWriter object is created using the new keyword and by specifying a file path within the parentheses of its constructor.

•A StreamReader object has Read( ) and ReadLine( ) methods that can be dot-suffixed to an instance name.

•A StreamWriter object has Write( ) and WriteLine( ) methods that can be dot-suffixed to an instance name.

•All StreamReader and StreamWriter objects are disposable, so should each be enclosed in a using construct.

**29**

**Solving problems**

***This chapter demonstrates how to detect and manage errors in C# programs.***

[**Detecting real-time errors**](#chapter29.xhtml_sec226)

[**Fixing compile-time errors**](#chapter29.xhtml_sec227)

[**Debugging code**](#chapter29.xhtml_sec228)

[**Setting breakpoints**](#chapter29.xhtml_sec229)

[**Catching runtime errors**](#chapter29.xhtml_sec230)

[**Getting help**](#chapter29.xhtml_sec231)

[**Summary**](#chapter29.xhtml_sec232)

Detecting real-time errors

As you type code in the **Code Editor** window, the Visual Studio IDE is constantly monitoring your code for possible errors. It examines the code you type, and provides real-time feedback of possible errors by adding a wavy underline to questionable code.

![image](images/pgc98_1.jpg)

Warnings of potential problems are indicated by a green wavy underline. These are not critical and will not prevent execution of the application. A rollover tooltip explains the warning:

![image](images/1b.jpg)First, type this variable declaration in the **Code Editor**

**int num**

![image](images/2b.jpg)A green wavy line appears below the num variable name. Place the cursor over the green wavy underline to discover that the warning is merely indicating a potential problem as the variable has not yet been assigned a value

![image](images/pgc98_2.jpg)

![image](images/hot.jpg)

Visual Studio 2022 provides live code analysis, which displays a light bulb icon when the compiler detects an issue with your code, and has a suggestion of how to fix that issue.

Errors are indicated by a red wavy underline. Unlike warnings, these are critical and will prevent execution of the application:

![image](images/1b.jpg)Type this variable declaration in the **Code Editor**

**int num =**

![image](images/2b.jpg)Place the cursor over the red wavy underline to discover that the error is due to a missing value in the expression

![image](images/pgc98_3.jpg)

![image](images/snake.jpg)

Warnings can be accepted but errors must be corrected.

Real-time error detection in the Visual Studio IDE is a fantastic tool to help prevent errors when you are writing code. It not only indicates errors, but can even provide a list of correction options:

![image](images/1b.jpg)Now, type this variable declaration in the **Code Editor**

**intr num = 1 ;**

![image](images/2b.jpg)A red wavy line appears below the **intr** variable type. Place the cursor over the red wavy underline to discover that the error is due to an unknown type specification

![image](images/pgc99_1.jpg)

![image](images/3b.jpg)Click the light bulb icon, or click the **Show potential fixes** link, to see a list of error correction options

![image](images/pgc99_2.jpg)

![image](images/4b.jpg)If this error is simply a spelling error for the **int** data type, select the **Change ‘intr’ to ‘int’** option – see your code get instantly corrected accordingly. Other correction options allow you to create a new data type if that is what you require

**Fixing compile-time errors**

![image](images/pgc100_1.jpg)

While syntax errors like those [here](#chapter29.xhtml_syntax) can be detected by the **Code Editor** in real time, other errors that employ correct syntax cannot be detected until the code is compiled. Compile errors are typically errors of logic, and they cause the execution to halt when an “exception” occurs. For example, when incompatible data types appear in an expression, an **InvalidCastException** occurs and execution stops immediately:

![image](images/1b.jpg)Type the following lines into the **Code Editor**

**bool flag = true ;**

**IConvertible convertible = flag ;**

**char letter = convertible.ToChar( null ) ;**

![image](images/2b.jpg)Press **Start** or **F5** to run the application and see execution is soon halted. The line causing the exception becomes highlighted in the **Code Editor,** and an **Exception Assistant** pop-up window appears with a list of possible solutions

![image](images/pgc100_2.jpg)

To fix this **InvalidCastException**, the code would need amending so both values are of compatible data types.

The cause of other compile errors may be less obvious without some further investigation – for example, when a loop that is reading array elements attempts to address an element index that does not exist, causing an **IndexOutOfRangeException**.

![image](images/hot.jpg)

The **IConvertible** interface provides methods that convert a value to a CLR type, but it cannot meaningfully convert a **bool** to **char.**

![image](images/hot.jpg)

You can click on the **View Detail** link for more error information.

Execution halts immediately, so it is useful to examine the counter value to identify the precise iteration causing the compile error.

![image](images/1b.jpg)In the **Code Editor**, type the following variable array declaration of 10 elements (0-9), and a loop

**int [ ] nums = new int [ 10 ] ;**

**for ( int i = 1 ; i < 20 ; i++ ) { nums [ i ] = i ; }**

![image](images/2b.jpg)Press **Start** or **F5** to run the application and see execution is soon halted. The code causing the exception becomes highlighted in the **Code Editor**, and an **Exception Assistant** pop-up window appears with a list of possible solutions

![image](images/pgc101_1.jpg)

![image](images/3b.jpg)Place the cursor over the assignment to the array variable to see a pop-up appear displaying its current value

![image](images/pgc101_2.jpg)

It’s now clear that execution halted when the loop attempted to address **nums[10]** – beyond the bounds of last element nums[9]. To fix this **IndexOutOfRangeException**, the code would need amending to end the loop after 10 iterations.

![image](images/snake.jpg)

Another common error is the **FileNotFoundException** that occurs when a file is missing or its path name is incorrect.

**Debugging code**

![image](images/pgc102_1.jpg)

It is sometimes useful to closely examine the progression of a program by watching its execution line by line to locate any bugs. Progress is controlled by clicking the ![image](images/pgc102_2.jpg) **Step Into** button on the **Debug** Menu Bar to move through the program one line at a time. When you begin debugging, you can open a **Watch** window to monitor the value of particular variables as execution proceeds:

![image](images/commonab.jpg)

Debug

![image](images/1b.jpg)Type the following code in the **Code Editor**

**int pass = 0 ;**

**int unit = 2 ;**

**for ( int i = 0 ; i < 3 ; i++ )**

**{**

**pass = ( pass + 1 ) ;**

**unit = square( unit ) ;**

**}**

![image](images/2b.jpg)Now, add this simple arithmetic function

**static int square( int num )**

**{**

**return ( num * num ) ;**

**}**

![image](images/3b.jpg)In the **Code Editor**, click in the gray margin against the start of the loop – to set a debug starting “breakpoint”

![image](images/pgc102_3.jpg)

![image](images/4b.jpg)Click the **Start** button to begin debugging and see the code run to the breakpoint then halt

![image](images/pgc102_4.jpg)

![image](images/5b.jpg)Click **Debug**, **Windows**, **Watch**, **Watch1** on the Menu Bar to launch a **Watch** window, then enter the variable names into its **Name** column

![image](images/pgc102_5.jpg)

![image](images/hot.jpg)

If you can’t see the **Step Into** button, right-click on the Menu Bar and select **Debug** to add the debugging buttons.

![image](images/forget.jpg)

You can click the **Stop Debugging** button at any time to return to **Code Editor** mode.

![image](images/6b.jpg)Repeatedly click the **Step** **Into** button to progress through each line of the loop and through the square( ) function one time to see the variable values change in the **Watch** window

![image](images/pgc103_1.jpg)

![image](images/pgc103_2.jpg)

![image](images/7b.jpg)Repeatedly click the **Step Into** button to progress through each line of the loop and through the square( ) function a second time and see the variable values change again

![image](images/pgc103_3.jpg)

![image](images/8b.jpg)Now, repeatedly click the ![image](images/pgc103_4.jpg) **Step Over** button to progress through each line of the loop and call the square( ) function without stepping through the function

![image](images/pgc103_3.jpg)

![image](images/9b.jpg)Click the **Step Over** button to move to the end of the program and see the debugger automatically close, returning to regular **Code Editor** mode

![image](images/10b.jpg)Click the red dot you added in the margin to remove the breakpoint

![image](images/hot.jpg)

The **Step Out** button is used to return to the function caller when you are stepping through lines of a called function.

**Setting breakpoints**

![image](images/pgc104_1.jpg)

In all but the smallest of programs, stepping through each line is very tedious when debugging. Instead, you can quickly reach the part you wish to examine by setting multiple breakpoints to halt execution on particular lines. Setting one or more breakpoints is useful to help you understand how certain C# code constructs work – such as the nested loop construct shown here:

![image](images/commonab.jpg)

Breakpoints

![image](images/1b.jpg)Type this code to create three nested loops that each increment a counter variable within each loop, and a total pass iteration counter in the innermost loop

**int i , j , k ;**

**int pass = 0 ;**

**for ( i = 1 ; i < 4 ; i++ )**

**{**

**for ( j = 1 ; j < 4 ; j++ )**

**{**

**for ( k = 1 ; k < 4 ; k++ )**

**{**

**pass++ ;**

**}**

**}**

**}**

![image](images/2b.jpg)Click in the gray margin against each line containing the closing brace of each loop to set three breakpoints – a red dot will appear in the margin and each closing brace is highlighted to indicate the breakpoints are set

![image](images/pgc104_2.jpg)

![image](images/3b.jpg)Click the **Start** button and see the application run to the first breakpoint it meets

![image](images/pgc104_3.jpg)

![image](images/4b.jpg)Click **Debug**, **Windows**, **Locals** to launch the **Locals** window and notice the current value of each variable

![image](images/pgc105_1.jpg)

![image](images/hot.jpg)

Yellow arrows indicate the current position. Click on the red dot to cancel a breakpoint.

![image](images/5b.jpg)Watch the variable values change as you repeatedly click the **Start** (**Continue**) button to move to each successive breakpoint until you reach the third outer loop breakpoint

![image](images/6b.jpg)Repeatedly click **Step Into** until you reach the last iteration of the outermost loop to see the final values

![image](images/pgc105_2.jpg)

![image](images/pgc105_3.jpg)

At the end of the program, each counter variable has been incremented beyond the upper limit set in the for statements, to exit each loop, and there has been a total of 27 iterations (3x3x3).

![image](images/7b.jpg)Click the **Start** button once more to run to the first breakpoint, then click **Debug**, **Windows**, **Immediate** to launch the **Immediate** window

![image](images/8b.jpg)In the **Immediate** window, type i = 3 and hit **Enter**, then use the **Step Into** button to step through each line of just the final complete outer loop

![image](images/forget.jpg)

The **Locals** window shows all variables in current scope as the program proceeds.

![image](images/hot.jpg)

Any code you type into the **Immediate** window is dynamically applied to the application being debugged, but does not change its code.

**Catching runtime errors**

![image](images/pgc106_1.jpg)

When you are able to predict potential runtime errors by considering all eventualities, you can provide code to handle each Exception class error that may arise – by adding a try-catch construct. Your program can supply information to the user about the error, should you wish to do so, then proceed normally:

![image](images/commonab.jpg)

ErrorHandling

![image](images/1b.jpg)Add this program code to request user input of two numeric values for addition, then display their sum total

**Console.Write( “Please Enter A Number: “ ) ;**

**double num1 = Convert.ToInt16( Console.ReadLine( ) ) ;**

**Console.Write( “Now Enter Another Number: “ ) ;**

**double num2 = Convert.ToInt16( Console.ReadLine( ) ) ;**

**Console.WriteLine( “Total: “ + ( num1 + num2 ) ) ;**

![image](images/2b.jpg)Press **Start** or **F5** to run the application, then enter any six-figure integer and hit **Enter**

![image](images/pgc106_2.jpg)

![image](images/3b.jpg)The compiler reports an **OverflowException** error

![image](images/pgc106_3.jpg)

![image](images/4b.jpg)Click the **Stop Debugging** button so you can edit the code

![image](images/snake.jpg)

An **Int16** is a 16-bit integer within the range -32,768 to +32,767 – whereas an **Int32** is a 32-bit integer within -2,147,483,648 to +2,147,483,647.

![image](images/5b.jpg)Drag the mouse to highlight all statements in Step 1 on the [here](#chapter29.xhtml_stepre), then right-click on the highlighted area and choose **Snippet**, **Insert Snippet:**, **Visual C#**, **try**

![image](images/pgc107_1.jpg)

![image](images/6b.jpg)A **try-catch** construct is added to the code, enclosing the highlighted statements within the try block

![image](images/7b.jpg)Edit the default catch block to display an error message

**catch ( Exception error )**

**{ Console.WriteLine( error.Message ) ; }**

![image](images/8b.jpg)Run the application, then enter any six-figure integer and hit **Enter** to now see a default explanatory error message

![image](images/pgc107_2.jpg)

You can provide your own error messages to handle a specific Exception by stating its type in the catch( ) parentheses:

![image](images/9b.jpg)Edit the default catch block to display a custom message

**catch ( OverflowException )**

**{ Console.WriteLine( ”\nMaximum: “ + Int16.MaxValue ) ; }**

![image](images/10b.jpg)Run the application, then enter any six-figure integer and hit **Enter** to now see a custom explanatory error message

![image](images/pgc107_3.jpg)

![image](images/hot.jpg)

The **Insert Snippet** feature provides lots of useful pieces of code to paste into the **Code Editor** – take some time to explore its contents.

![image](images/hot.jpg)

Each **Exception** has several methods and properties. For example, use **error.GetType()** to see the type of **Exception**.

![image](images/hot.jpg)

You can add multiple **catch** blocks after the **try** block, to handle different types of **Exception**.

**Getting help**

![image](images/pgc108_1.jpg)

The Visual Studio **Help** system provides an extensive source of reference for many programming languages. You can choose to install a Help library on your computer for the C# programming language so you can easily refer to it at any time, but the Help Viewer must first be installed in Visual Studio:

![image](images/1b.jpg)Click **Visual Studio Installer** on the Windows Start menu, then select the **Installed** menu item and click the **Modify** button on the Installer dialog

![image](images/2b.jpg)Select the **Individual components** tab, check the **Help Viewer** option, then click the **Modify** button at the bottom right of this dialog to install the Help Viewer

![image](images/pgc108_2.jpg)

![image](images/3b.jpg)On the Visual Studio Menu Bar, click **Help**, **Add and Remove Help Content** to open the **Help Viewer**

![image](images/pgc108_3.jpg)

![image](images/4b.jpg)On the **Manage Content** tab, expand **Recommended Documentation**, then choose the **Add** link in the **Action** column for the **Visual C#** library

![image](images/5b.jpg)When your selection is added to the **Pending changes** list, click the **Update** button to download that library

![image](images/pgc109_1.jpg)

![image](images/forget.jpg)

The **Help Viewer** may not be installed by default when you install Visual Studio unless you select it from the Individual components list.

![image](images/hot.jpg)

The **Help Viewer** allows you to download **Help** libraries for offline use, check for available updates, and seek help from installed **Help** libraries.

![image](images/6b.jpg)On the Menu Bar, click **Help**, **Set Help Preference**, **Launch in Help Viewer** to use installed library

![image](images/pgc109_2.jpg)

![image](images/7b.jpg)Next, click **Help**, **View Help** to launch **Help Viewer**

![image](images/8b.jpg)Now, select the **Index** tab in the left-hand pane

![image](images/9b.jpg)Type the item for help, such as “data types”, in the **Help Viewer** Search box, then hit **Enter** to see the results

![image](images/pgc109_3.jpg)

![image](images/hot.jpg)

You can **Set Help Preference** to **Launch in Browser** if you want to search online help without installing libraries, but local help is often more convenient.

**Summary**

![image](images/pgc110_1.jpg)

•The **Code Editor** constantly monitors your code to provide real-time error detection.

•Warnings are not critical and are indicated by a green wavy underline – whereas errors are critical and are indicated by a red wavy underline.

•A light bulb icon beside a red wavy underline indicates that a list of potential fixes is available.

•Typically, real-time errors are errors of syntax, and compile errors are errors of logic.

•When a compile error occurs in **Debug Mode**, execution stops and the **Exception Assistant** offers a list of possible fixes.

•In **Debug Mode** you can discover the current value of any variable simply by placing the cursor over the variable name.

•When debugging code, the **Step Into** button lets you walk through a program one line at a time.

•The **Step Over** button lets you bypass the lines of a called method, and the **Step Out** button lets you return to the line where that method is called.

•Variable values can be monitored as a program proceeds, using the **Watch** window or the **Locals** window.

•Breakpoints halt the execution of a program to allow examination of the part of the program where they are set.

•In **Debug Mode**, code can be dynamically applied using the **Immediate** window.

•Runtime errors occur when the user action has not been anticipated by the programmer.

•A **try-catch** block can be used to handle anticipated exceptions.

•The **Help** library system provides extensive reference sources for both offline and online assistance.

**30**

**Creating objects**

***This chapter demonstrates encapsulation, inheritance, and polymorphism – the three principles of C# Object Oriented Programming.***

[**Encapsulating data**](#chapter30.xhtml_sec233)

[**Creating multiple objects**](#chapter30.xhtml_sec234)

[**Initializing class members**](#chapter30.xhtml_sec235)

[**Inheriting class properties**](#chapter30.xhtml_sec236)

[**Calling base constructors**](#chapter30.xhtml_sec237)

[**Hiding base methods**](#chapter30.xhtml_sec238)

[**Directing method calls**](#chapter30.xhtml_sec239)

[**Providing capability classes**](#chapter30.xhtml_sec240)

[**Employing partial classes**](#chapter30.xhtml_sec241)

[**Summary**](#chapter30.xhtml_sec242)

**Encapsulating data**

A class is a data structure that can contain both variables and methods in a single entity. These are collectively known as its “members”, and the variables are also known as its “properties”.

![images](images/pgc112_1.jpg)

If a class is not declared as **static** it can be used to create “instances” that are assigned to a variable for use by other classes.

Access to class members from outside the class is controlled by “access specifiers” in the **class** declaration. Typically, these will deny access to the variable members, but allow access to methods that can store and retrieve data from those variable members. This technique of “data hiding” ensures that stored data is safely encapsulated within the class variable members, and is the first principle of Object Oriented Programming (OOP).

A class declaration comprises a class access specifier, the **class** keyword, and a programmer-specified name – adhering to the usual C# naming conventions, but beginning in uppercase.

The class declaration is followed by a pair of braces containing the variable and method declarations, which typically begin with their own access specifier. So, class syntax looks like this:

***access-specifier* class *ClassName***

**{**

**// Member variable property.**

***access-specifier data-type variable-name ;***

**// Member method.**

***access-specifier return-type method-name ( parameter-list )***

**{**

***statements***

**}**

**}**

![image](images/forget.jpg)

If not specified, the default access specifier for a class declaration is **internal**, and the default access specifier for class members is **private**.

An access specifier may be any one of these keywords:

•public – accessible from any place where the class is visible.

•private – accessible only to other members of the same class.

•protected – accessible only to other members of the same class and members of classes derived from that class.

•internal – accessible only to members of the same assembly.

![image](images/hot.jpg)

Derived classes, which use the **protected** member access specifier, are introduced later – see [here](#chapter30.xhtml_sec236).

Any real-world object can be defined by its attributes and by its actions. For example, a dog has attributes such as name, age, and color, plus actions it can perform such as bark. The class mechanism in C# provides a way to create a virtual dog object within a program, where the variable members of a class can represent its attributes and the methods represent its actions:

**public class Dog**

**{**

**// MEMBER VARIABLES...**

**private string name ;**

**private int age ;**

**private string color ;**

**// MEMBER METHODS...**

**// Setter & Getter Methods:**

**public void setName( string tag )**

**{**

**name = tag ;              // Store the argument value.**

**}**

**public string getName( )**

**{**

**return name ;          // Retrieve the stored value.**

**}**

**public void setAge( int yrs ) { age = yrs ; }**

**public int getAge( ) { return age ; }**

**public void setColor( string coat ) { color = coat ; }**

**public string getColor( ) { return color ; }**

**// Other Methods:**

**public string bark( ) { return “\nWoof, woof!\n” ; }**

**}**

It is important to recognize that a class declaration only defines a data structure – in order to create an object you must declare an “instance” of that data structure, assigned to a variable. This requires the **new** keyword and class name followed by parentheses:

**Dog fido = new Dog( ) ; // Create a “fido”instance of the Dog class.**

The principle of encapsulation in C# programming describes the grouping together of data and functionality in class members – name, age, color attributes, and bark action in the Dog class.

![image](images/hot.jpg)

A program class cannot perfectly emulate a real-world object, but aims to encapsulate all relevant attributes and actions.

![image](images/forget.jpg)

The **public** “setter” and “getter” methods assign values to, and retrieve values from, the **private** variable members.

![image](images/hot.jpg)

It is conventional to begin class names with an uppercase character, and instance names with lowercase.

**Creating multiple objects**

A program can easily create multiple objects simply by declaring multiple new instances of a class, and each object can have unique attributes by assigning individual values with its setter methods.

![images](images/pgc114_1.jpg)

It is often convenient to combine the setter methods into a single method that accepts arguments for each private variable. This means that all values can be assigned with a single statement in the program, but the method will contain multiple statements.

In C# class declarations, the public “setter” methods, which assign data to private variable members, and public “getter” methods, which retrieve data from private variable members, are often named as the variable they address – but with the first letter made uppercase and prefixed by “set” or “get” respectively. For example, methods to access an age variable may be setAge( ) and getAge( ).

Parameters may also be named as the variable they address. The code can differentiate between the parameter and like-named variable member by dot-prefixing this to the variable name:

![image](images/commonar.jpg)

Objects

![image](images/1r.jpg)Start a new **C# Console App** and name it “Objects”

**Console.Title = “Objects” ;**

**// Top-level statements to be inserted here (Steps 6-10).**

![image](images/2r.jpg)Next, declare a class named “Dog” with three variable members, plus setter and getter methods for each variable

**public class Dog**

**{**

**private string name , color ;**

**private int age ;**

**public void setValues( string name, int age, string color )**

**{**

**this.name = name ;**

**this.age = age ;**

**this.color = color ;**

**}**

**public string getName( ) { return name ; }**

**public int getAge( ) { return age ; }**

**public string getColor( ) { return color ; }**

**}**

![image](images/3r.jpg)Then, add a final miscellaneous method in the Dog class

**public string bark( ) { return “\nWoof, woof!\n” ; }**

![image](images/forget.jpg)

In the setter method, the **this** prefixed names reference the **class** variable members, and those without prefix reference the parameters. No prefix is needed to reference the **class** variable members.

![image](images/4r.jpg)Above the class declaration, begin to add top-level statements by creating an instance of the Dog class

**Dog fido = new Dog( ) ;**

![images](images/pgc115_1.jpg)

![image](images/5r.jpg)Next, call the new instance object’s setter method to initialize all its variable members

**fido.setValues( “Fido” , 3 , “Brown” ) ;**

![image](images/6r.jpg)Now, retrieve all properties of the new object

**string tagF = String.Format( “{0} is a {1} year old {2} dog”,**

**fido.getName( ) ,**

**fido.getAge( ) ,**

**fido.getColor( )**

) ;

![image](images/7r.jpg)Display all properties and call the miscellaneous method

**Console.WriteLine( tagF + fido.bark( ) ) ;**

![image](images/8r.jpg)Now, create another instance of the **Dog** class

**Dog lucy = new Dog( ) ;**

**lucy.setValues( “Lucy” , 2 , “Gray” ) ;**

![image](images/9r.jpg)Next, retrieve all properties of this new object

**string tagL = String.Format( “{0} is a {1} year old {2} dog”,**

**lucy.getName( ) ,**

**lucy.getAge( ) ,**

**lucy.getColor( )**

**) ;**

![image](images/10r.jpg)Display all properties and call the miscellaneous method

**Console.WriteLine( tagL + lucy.bark( ) ) ;**

**Console.ReadKey( ) ;**

![image](images/11r.jpg)Press **Start** or **F5** to see each object’s properties

![images](images/pgc115_2.jpg)

![image](images/forget.jpg)

Top-level statements must precede any class declarations in the program code.

![image](images/hot.jpg)

Notice here how the **String.Format( )** method call is coded using newlines to clearly build a **string** value for output.

**Initializing class members**

Class variable members can be initialized by a special “constructor” method that is called whenever an instance of the class is created – allowing you to specify default values for class variable members.

![images](images/pgc116_1.jpg)

The constructor method is always named exactly as the class name, and can contain statements to initialize class variable members – for example, public class Cat has a public Cat( ) constructor.

When all class variables have been initialized by the class constructor method, any instance object of that class will immediately have those initial property values. Individual setter methods can usefully adjust the class variable values as needed:

![image](images/commonar.jpg)

Constructor

![image](images/1r.jpg)Start a new **C# Console App** and name it “Constructor”

**Console.Title = “Constructor” ;**

**// Top-level statements to be inserted here (Steps 6-11).**

![image](images/2r.jpg)Next, declare a class named “Cat” with three variable members

**public class Cat**

**{**

**private string name , color ;**

**private int age ;**

**// Methods to be inserted here (Steps 3-5).**

**}**

![image](images/3r.jpg)Now, insert a class constructor method to set default values for all its variable members

**public Cat( )**

**{**

**name = “Tigger” ; age = 3 ; color = “Brown” ;**

**}**

![image](images/4r.jpg)Then, insert setter and getter methods for each variable

**public void setName( string name ) { this.name = name ; }**

**public void setAge( int age ) { this.age = age ; }**

**public void setColor( string color ) { this.color = color ; }**

**public string getName( ) { return name ; }**

**public int getAge( ) { return age ; }**

**public string getColor( ) { return color ; }**

![image](images/5r.jpg)Add a final miscellaneous method in the Cat class

**public string cry( ) { return “\nMeow, meow!\n” ; }**

![image](images/6r.jpg)Above the class declaration, begin to add top-level statements by creating an instance of the Cat class

**Cat tigger = new Cat( ) ;**

![images](images/pgc117_1.jpg)

![image](images/7r.jpg)Now, retrieve all (default) properties of the new object

**string tagT = String.Format( “{0} is a {1} year old {2} cat”,**

**tigger.getName( ) ,**

**tigger.getAge( ) ,**

**tigger.getColor( )**

**) ;**

![image](images/8r.jpg)Display all properties and call the miscellaneous method

**Console.WriteLine( tagT + tigger.cry( ) ) ;**

![image](images/9r.jpg)Now, create another instance of the **Cat** class and set each property with new values

**Cat smokey = new Cat( ) ;**

**smokey.setName( “Smokey” ) ;**

**smokey.setAge( 2 ) ;**

**smokey.setColor( “Gray” ) ;**

![image](images/10r.jpg)Next, retrieve all (adjusted) properties of this new object

**string tagS = String.Format( “{0} is a {1} year old {2} cat”,**

**smokey.getName( ) ,**

**smokey.getAge( ) ,**

**smokey.getColor( )**

**) ;**

![image](images/11r.jpg)Display all properties and call the miscellaneous method

**Console.WriteLine( tagS + smokey.cry( ) ) ;**

**Console.ReadKey( ) ;**

![image](images/12r.jpg)Press **Start** or **F5** to run the application and see the properties of each object instance and method called

![images](images/pgc117_3.jpg)

![image](images/hot.jpg)

You can also specify parameters to a constructor method in order to allow argument values to be passed when a **new** instance object is created.

**Inheriting class properties**

A C# class can be created as a brand new class, like those in previous examples, or can be “derived” from an existing class. Importantly, a derived class inherits members of the parent (base) class from which it is derived – in addition to its own members.

![images](images/pgc118_1.jpg)

The ability to inherit members from a base class allows derived classes to be created that share certain common properties, which have been defined in the base class. For example, a “Polygon” base class may define width and height properties that are common to all polygons. Classes of “Rectangle” and Triangle” could be derived from the Polygon class – inheriting width and height properties, in addition to their own members defining their unique features.

![images](images/pgc118_2.jpg)

The virtue of inheritance is extremely powerful and is the second principle of Object Oriented Programming (OOP).

A derived class declaration adds a colon : after its class name, followed by the name of the class from which it derives:

![image](images/commonar.jpg)

Inheritance

![image](images/1r.jpg)Start a new **C# Console App** and name it “Inheritance”

**Console.Title = “Inheritance” ;**

**// Top-level statements to be inserted here (Steps 5-7).**

![image](images/2r.jpg)Next, declare a base class named “Polygon”, containing two variable members and one setter method member

**public class Polygon**

**{**

**protected int width , height ;**

**public void setValues( int width , int height )**

**{**

**this.width = width ;**

**this.height = height ;**

**}**

**}**

![image](images/3r.jpg)Now, define a class that derives from the base class, inheriting members and adding a method

**public class Rectangle : Polygon**

**{**

**public int area( ) { return ( width * height ) ; }**

**}**

![image](images/4r.jpg)Then, define another class that derives from the base class, inheriting members and adding a similar method to that in the previous step

**public class Triangle : Polygon**

**{**

**public int area( ) { return ( ( width * height ) / 2 ) ; }**

**}**

![image](images/5r.jpg)Above the class declarations, begin to add top-level statements by creating an instance object from each derived class

**Rectangle rect = new Rectangle( ) ;**

**Triangle cone = new Triangle( ) ;**

![image](images/6r.jpg)Call the inherited setter method of each derived class to initialize all the inherited variable members

**rect.setValues( 4 , 5 ) ;**

**cone.setValues( 4 , 5 ) ;**

![image](images/7r.jpg)Finally, call the added method in each derived class to display their computed values

**Console.WriteLine( “Rectangle Area: “ + rect.area( ) ) ;**

**Console.WriteLine( “\nTriangle Area: “ + cone.area( ) ) ;**

**Console.ReadKey( ) ;**

![image](images/8r.jpg)Press **Start** or **F5** to run the application and see the output from inherited variables

![images](images/pgc119_1.jpg)

![image](images/hot.jpg)

The : operator is used here to create derived classes, and is equivalent to the **extends** keyword in other programming languages – such as Java.

![image](images/forget.jpg)

The methods added to each derived class can be named alike, as they only exist within the scope of their respective class.

![image](images/forget.jpg)

Notice that the setter method and variables are not defined in the derived classes, as they are inherited from the base class.

**Calling base constructors**

Although derived classes inherit the members of their parent base class, they do not inherit its constructor method. Nonetheless, a constructor method of the base class is always called when a new object of a derived class is created. The call to the base class constructor method is made in addition to the call to the constructor method of the derived class.

![images](images/pgc120_1.jpg)

The default constructor method of a base class has no parameters – but the base class may also have one or more “overloaded” constructor methods that do have parameters.

If you prefer to call an overloaded constructor of the base class when a new object of a derived class is created, you can create a matching overloaded constructor in the derived class – having the same number and type of arguments. The matching derived class constructor must then explicitly call the overloaded base class constructor using the base keyword. This is appended to the derived class constructor declaration after a : colon character.

When a new object of a derived class is created, argument values can be passed to an overloaded derived class constructor, and also onwards to its matching overloaded base class constructor in parentheses following the base keyword:

![image](images/commonar.jpg)

Base

![image](images/1r.jpg)Start a new **C# Console App** and name it “Base”

**Console.Title = “Base” ;**

**// Top-level statements to be inserted here (Step 6).**

![image](images/2r.jpg)Next, declare a base class named “Parent”, containing a default constructor method and an overloaded constructor method that requires a single integer argument

**public class Parent**

**{**

**public Parent( )**

**{**

**Console.WriteLine( “Parent Called” ) ;**

**}**

**public Parent( int num )**

**{**

**Console.WriteLine( “Parent+ Called: ” + num ) ;**

**}**

**}**

![image](images/forget.jpg)

An overloaded method is one that has the same name as another method but different parameters.

![image](images/3r.jpg)After the base class, add a derived class containing a default constructor method

**public class Daughter : Parent**

**{**

**public Daughter( )**

**{ Console.WriteLine( “\tDaughter Called\n” ) ; }**

**}**

![images](images/pgc121_1.jpg)

![image](images/4r.jpg)Next, add another derived class, containing a default constructor method

**public class Son : Parent**

**{**

**public Son( )**

**{ Console.WriteLine( “\tSon Called\n” ) ; }**

**// Overloaded constructor to be inserted here (Step 5).**

**}**

![image](images/5r.jpg)Now, insert an overloaded constructor method into the derived class, which requires a single integer argument

**public Son( int num ) : base( num )**

**{**

**Console.WriteLine( “\tSon+ Called: ” + num ) ;**

**}**

![image](images/6r.jpg)Above the class declarations, add top-level statements that create instances of the derived classes

**Daughter anna = new Daughter( ) ;**

**Son brad = new Son( ) ;**

**Son carl = new Son( 100 ) ;
Console.ReadKey( ) ;**

![image](images/7r.jpg)Press **Start** or **F5** to run the application and see the output from base and derived class constructors

![images](images/pgc121_2.jpg)

![image](images/snake.jpg)

The default base constructor method will be called implicitly unless the **base** keyword is used to call explicitly.

![image](images/forget.jpg)

Here, the argument value is passed to the derived class and base class.

**Hiding base methods**

A method can be declared in a derived class to “hide” a similar method in the base class – if both method declarations have matching name, arguments, and return type.

![images](images/pgc122_1.jpg)

Creation of a matching method in a derived class effectively hides the base class method, as it generally becomes inaccessible. To indicate that hiding is intentional, rather than accidental, the hiding method declaration should include the new keyword.

Base class methods can be called explicitly from non-static methods by prefixing their method name with the base keyword. Alternatively, as a derived class is a specialization of its base class, base class methods can be called explicitly using an explicit cast:

![image](images/commonar.jpg)

Hide

![image](images/1r.jpg)Start a new **C# Console App** and name it “Hide”

**Console.Title = “Hide” ;**

**// Top-level statements to be inserted here (Steps 5-10).**

![image](images/2r.jpg)Next, declare a base class named “Man”, containing a simple method without parameters plus an overloaded method with a single parameter

**public class Man**

**{**

**public void speak( )**

**{**

**Console.Write( “Hello: ” ) ;**

**}**

**public void speak( string message )**

**{**

**Console.WriteLine( message + “!\n” ) ;**

**}**

**}**

![image](images/3r.jpg)After the base class, add a derived class containing a method to intentionally hide the overloaded method of the same name and parameters in the base class

**public class Hombre : Man**

**{**

**public new void speak( string message )**

**{**

**// Statement to be inserted here (Step 4).**

**Console.WriteLine( message ) ;**

**}**

**}**

![image](images/4r.jpg)Next, insert a statement in the derived class to explicitly call the simple method in the base class

**base.speak( ) ;**

![image](images/5r.jpg)Above the class declarations, begin to add top-level statements by creating an instance of the base class

**Man henry = new Man( ) ;**

![images](images/pgc123_1.jpg)

![image](images/6r.jpg)Next, create an instance of the derived class

**Hombre enrique = new Hombre( ) ;**

![image](images/7r.jpg)Add a call to the simple method inherited by the instance from the base class

**henry.speak( ) ;**

![image](images/8r.jpg)Now, add a call to the overloaded method inherited from the base class

**henry.speak( “It’s a beautiful evening” ) ;**

![image](images/9r.jpg)Then, add a call to the hiding method in the derived class – that will also explicitly call the simple method in the base class

**enrique.speak( “Hola...” ) ;**

![image](images/10r.jpg)Finally, add a statement using an explicit cast – to explicitly call the overloaded method in the base class

**( (Man) enrique ).speak( “Es una tarde hermosa” ) ;**

**Console.ReadKey( ) ;**

![image](images/11r.jpg)Press **Start** or **F5** to run the application and see the output from base class methods and hiding method

![images](images/pgc123_2.jpg)

![image](images/forget.jpg)

A derived class method name and parameter list must match that in its base class to override it.

**Directing method calls**

The three cornerstones of Object Oriented Programming (OOP) are **encapsulation**, **inheritance**, and **polymorphism**. Previous examples have demonstrated **encapsulation** of data within a class, and **inheritance** of base class members by derived classes. The term **polymorphism** (from Greek, meaning “many forms”) is the ability to have a different behavior according to context. C# class methods can be made to be polymorphic. Method declarations in a base class can include the virtual keyword to allow that method to be overridden in derived classes. Similarly, method definitions in a derived class can include the override keyword to denote it will be overriding a virtual base class method. This lets derived class methods provide their own version of a base class method. The great advantage of polymorphism with multiple derived class objects is that calls to methods of the same name are directed to the appropriate overriding method. This can allow inconsistencies, however – this example seems to imply that chickens can fly!

![image](images/pgc124_1.jpg)

![image](images/commonar.jpg)

Override

![image](images/1r.jpg)Start a new **C# Console App** and name it “Override”

**Console.Title = “Override” ;**

**// Top-level statements to be inserted here (Steps 5-7).**

![image](images/2r.jpg)Next, declare a base class named “Bird”, containing two methods that allow overriding

**public class Bird**

**{**

**public virtual void talk( )**

**{ Console.WriteLine( “A Bird Talks...” ) ; }**

**public virtual void fly( )**

**{ Console.WriteLine( “A Bird Flies...\n” ) ; }**

**}**

![image](images/3r.jpg)After the base class, add a derived class containing two methods that will override the base class methods

**public class Pigeon : Bird**

**{**

**public override void talk( )**

**{ Console.WriteLine( “Pigeon Says: Coo! Coo!” ) ; }**

**public override void fly( )**

**{**

**Console.WriteLine( “A Pigeon Flies Away...” ) ;**

**base.fly( ) ;**

**}**

**}**

![image](images/forget.jpg)

Here, the **fly( )** method in each derived class also calls the base class **fly( )** method directly.

![image](images/hot.jpg)

C# overloaded operators can be described as polymorphic. For example, the + operator can add or concatenate according to its context.

![image](images/4r.jpg)Next, add another derived class containing two methods that will also override the base class methods

**public class Chicken : Bird**

**{**

**public override void talk( )**

**{ Console.WriteLine( “Chicken Says: Cluck! Cluck!” ) ; }**

**public override void fly( )**

**{**

**Console.WriteLine( “I’m A Chicken - I Can’t Fly” ) ;**

**base.fly( ) ;**

**}**

**}**

![image](images/5r.jpg)Above the class declarations, begin to add top-level statements with a function to call both overriding methods

**static void describe( Bird obj )**

**{**

**obj.talk( ) ;**

**obj.fly( ) ;**

**}**

![image](images/6r.jpg)Then, create instances of each non-base class

**Pigeon joey = new Pigeon( ) ;
Chicken lola = new Chicken( ) ;**

![image](images/7r.jpg)Finally, add statements to call appropriate methods

**describe( joey ) ;**

**describe( lola ) ;
Console.ReadKey( ) ;**

![image](images/8r.jpg)Press **Start** or **F5** to run the application and see the output from overriding methods and base class method

![image](images/pgc125_1.jpg)

![image](images/snake.jpg)

You must use the **base** keyword prefix to directly call a base class method from a derived class.

![image](images/hot.jpg)

Each instance is passed as an argument for C# to determine the appropriate overriding method to execute.

![image](images/hot.jpg)

Polymorphism in programming is often called “one interface, multiple functions”.

**Providing capability classes**

Classes whose sole purpose is to allow other classes to be derived from them are known as “capability classes” – they provide capabilities to the derived classes. Capability classes generally contain no data, but merely declare a number of methods that can be overridden in their derived classes.

![images](images/pgc126_1.jpg)

A capability class and its methods can all be declared using the abstract keyword to denote that they can only be implemented in derived classes. In this case, the method signature is followed by a semicolon, rather than a method block containing statements. Method definitions in derived classes can then include the override keyword to implement the capability class methods.

Adding the sealed keyword to a class declaration is a safeguard that prevents that class being used as a base class. Understandably, an abstract capability class cannot be sealed.

The following example builds upon the previous example [here](#chapter30.xhtml_sec239) to demonstrate how the “Bird” class can be better written as a capability class. This now prevents the base class methods being called directly, to avoid inconsistencies:

![image](images/commonar.jpg)

Capability

![image](images/1r.jpg)Start a new **C# Console App** and name it “Capability”

**Console.Title = “Capability” ;**

**// Top-level statements to be inserted here (Steps 6-7).**

![image](images/2r.jpg)Next, define a base capability class named “Bird”, containing two methods

**public abstract class Bird**

**{**

**public abstract void talk( ) ;**

**public abstract void fly( ) ;**

**}**

![image](images/3r.jpg)Add a derived class containing two methods that will override the base class methods

**public sealed class Pigeon : Bird**

**{**

**public override void talk( )**

**{ Console.WriteLine( “Pigeon Says: Coo! Coo!” ) ; }**

**public override void fly( )**

**{ Console.WriteLine( “A Pigeon Flies Away...” ) ; }**

**}**

![image](images/snake.jpg)

You cannot create an instance of an **abstract** class.

![image](images/4r.jpg)Now, add another class that also contains two methods that will override the base class methods

**public sealed class Chicken : Bird**

**{**

**public override void talk( )**

**{ Console.WriteLine( “Chicken Says: Cluck! Cluck!” ) ; }**

**public override void fly( )**

**{ Console.WriteLine( “I’m A Chicken - I Can’t Fly” ) ; }**

**}**

![images](images/pgc127_1.jpg)

![image](images/5r.jpg)Then, add another class containing a single method that accepts an object argument

**public sealed class Caller**

**{**

**public void describe( Bird obj )**

**{**

**obj.talk( ) ;**

**obj.fly( ) ;**

**}**

**}**

![image](images/6r.jpg)Above the class declarations, begin to add top-level statements by creating instances of each non-base class

**Pigeon joey = new Pigeon( ) ;**

**Chicken lola = new Chicken( ) ;**

**Caller call = new Caller( ) ;**

![image](images/7r.jpg)Finally, add statements to call appropriate methods by passing an object as an argument

**call.describe( joey ) ;**

**call.describe( lola ) ;**

**Console.ReadKey( ) ;**

![image](images/8r.jpg)Press **Start** or **F5** to run the application and see the output from the overriding methods of derived classes

![images](images/pgc127_3.jpg)

![image](images/forget.jpg)

Each instance is passed as an argument for C# to determine the appropriate overriding method to execute.

**Employing partial classes**

The source code for each example listed in the C# section of this book is generally contained in a single .cs file, as each one is just a simple program. When working on larger projects it is often desirable to spread the source code over separate files to allow multiple programmers to work on the project at the same time. Visual Studio allows you to easily add one or more code files in which to write classes.

![images](images/pgc128_1.jpg)

Class definitions can also be spread across several files by including the partial keyword in each separate part of the definition. Providing all parts have the same level of accessibility, the C# compiler will combine all parts into a single definition:

![image](images/commonar.jpg)

Parts

![image](images/1r.jpg)Start a new **C# Console App** and name it “Parts”

**Console.Title = “Parts” ;**

**// Top-level statements to be inserted here (Steps 9-10).**

![image](images/2r.jpg)On the Visual Studio menu, select **Project**, **Add Class...** to launch the “Add New Item” dialog box

![images](images/pgc128_2.jpg)

![image](images/3r.jpg)Edit the name field to the name of the class to be added there – in this case, it’s to be a class named “Sailboat”

![image](images/4r.jpg)Click the **Add** button to add the new file to your project

![images](images/pgc128_3.jpg)

![image](images/5r.jpg)Next, select **View**, **Solution Explorer** and double-click on **Sailboat.cs** to open that file in the **Code Editor**

![image](images/snake.jpg)

If any part is declared **abstract**, the whole class will be **abstract**, and if any part is declared **sealed**, the whole class will be **sealed**.

![image](images/hot.jpg)

Alternatively, you can right-click on the project name in Solution Explorer and choose **Add**, **New Item** to launch this dialog.

![image](images/6r.jpg)Replace the default code with this class constructor part

**public partial class Sailboat**

**{**

**private string make ;**

**private string model ;**

**public Sailboat( string make , string model )**

**{**

**this.make = make ;**

**this.model = model ;**

**}**

**}**

![images](images/pgc129_1.jpg)

![image](images/7r.jpg)Now, in **Solution Explorer**, double-click on **Program.cs** to open that file in the **Code Editor**

![images](images/pgc129_2.jpg)

![image](images/8r.jpg)Then, add a class method part

**public partial class Sailboat**

**{**

**public void describe( )**

**{**

**Console.WriteLine( “Sailboat: {0} {1}” , make , model ) ;**

**}**

**}**

![image](images/9r.jpg)Above the class declaration, begin to add top-level statements by creating an instance object

**Sailboat boat = new Sailboat( “Laser” , “Classic” ) ;**

![image](images/10r.jpg)Finally, add a statement to call the added class method

**boat.describe( ) ;**

**Console.ReadKey( ) ;**

![image](images/11r.jpg)Press **Start** or **F5** to run the application and see the output from the class parts spread over two files

![images](images/pgc129_3.jpg)

![image](images/hot.jpg)

Notice how the strings are substituted for output in this example from members declared in another file.

**Summary**

![image](images/pgc130_1.jpg)

•Encapsulation, inheritance, and polymorphism are the three cornerstones of Object Oriented Programming.

•A C# class is a data structure that can contain both variable members and method members.

•Access to class members is controlled by access specifiers.

•An instance object of a class is created using the new keyword followed by the class name and parentheses.

•Typically, public setter and getter methods provide access to private variables to ensure stored data is safely encapsulated.

•Parameters can be named as the variable they address, and the this keyword prefix can be used to differentiate between them.

•The constructor method of a class is named as the class name and is called each time an instance of that class is created.

•Derived classes inherit members of the base parent class from which they are derived.

•A derived class declaration adds a colon after the class name, followed by the name of the class from which it derives.

•An overloaded constructor of a base class can be called using the base keyword in a derived class declaration.

•A derived class can include a new method to hide a method in its parent class if name, arguments, and return type match.

•Base class methods can be called explicitly from a derived class by prefixing the method name with the base keyword.

•The virtual and override keywords can be used to allow base class methods to be overridden by derived class methods.

•Capability classes can include the abstract keyword to denote their methods must be implemented in derived classes.

•Adding the sealed keyword to a class declaration is a safeguard that prevents that class being used as a base class.

•Class definitions can be spread across several files by including the partial keyword in each part of the definition.

**31**

**Controlling events**

***This chapter demonstrates how a C# program can recognize and respond to events that occur in a graphical application.***

[**Starting a Forms project**](#chapter31.xhtml_sec243)

[**Adding visual controls**](#chapter31.xhtml_sec244)

[**Writing functional code**](#chapter31.xhtml_sec245)

[**Gathering text entries**](#chapter31.xhtml_sec246)

[**Ticking option boxes**](#chapter31.xhtml_sec247)

[**Showing user messages**](#chapter31.xhtml_sec248)

[**Calling system dialogs**](#chapter31.xhtml_sec249)

[**Creating application menus**](#chapter31.xhtml_sec250)

[**Making menus work**](#chapter31.xhtml_sec251)

[**Importing audio resources**](#chapter31.xhtml_sec252)

[**Summary**](#chapter31.xhtml_sec253)

**Starting a Forms project**

Visual Studio provides a **Windows Forms App** template that allows you to easily create a C# program that provides a Graphical User Interface (GUI) to interact with the user:

![image](images/commonag.jpg)

FirstGUI

![image](images/1g.jpg)On the Menu Bar, click **File**, **New**, **Project**, to open the “Create a new project” dialog

![image](images/pgc132_1.jpg)

![image](images/2g.jpg)In the “Create a new project” dialog, select **Windows Forms App (.NET Framework)** then click **Next**

![image](images/pgc132_2.jpg)

![image](images/3g.jpg)Enter a project name of your choice in the **Name** field, then click on the **Create** button to create the new project – in this case, the project name will be “FirstGUI”

![image](images/4g.jpg)Select the .NET version, then wait until Visual Studio creates your new project. You should then see a **Form** **Designer** window appear displaying a blank Form

![image](images/5g.jpg)Select the **View**, **Solution Explorer** menu to open a Solution Explorer window and see all files in your project

![image](images/hot.jpg)

Windows GUI applications provide interactive controls that produce “events” in response to user actions, and your program can respond to those actions. This is known as event-driven programming.

![image](images/hot.jpg)

You can open the FormDesigner window from the menu by clicking **View**, **Designer** or by pressing the **Shift + F7** keyboard keys.

![image](images/6g.jpg)Now, select the **View**, **Properties** menu to open a **Properties** window to reveal all properties of your Form

![image](images/pgc133_1.jpg)

![images](images/pgc133_2.jpg)

The **Form Designer** is where you create visual interfaces for your applications, and the **Properties** window contains details of the item that is currently selected in the Form Designer window.

![image](images/7g.jpg)The Visual Studio IDE has now gathered all the resources needed to build a default Windows application – click the **Start** button on the toolbar to launch this application

![image](images/pgc133_4.jpg)

![image](images/pgc133_3.jpg)

The application simply creates a basic window – you can move it, minimize it, maximize it, resize it, and quit the application by closing it. It may not do much, but you have already created a real Windows GUI app!

![image](images/forget.jpg)

Alternatively, you can run applications using the **Debug**, **Start Debugging** menu options or by pressing the **F5** keyboard key.

**Adding visual controls**

The **Toolbox** in the Visual Studio IDE contains a wide range of visual controls, which are the building blocks of your applications. Using the project created [here](#chapter31.xhtml_sec243), follow these steps to start using the Toolbox now:

![image](images/commonag.jpg)

FirstGUI (continued)

![image](images/1g.jpg)Click the vertical **Toolbox** tab at the left edge of the IDE window, or click **View**, **Toolbox** on the Menu Bar, to display the Toolbox contents. The visual controls are contained under various category headings beside an ^(![image](images/pgc134_4.jpg)) expansion arrow

![image](images/pgc134_1.jpg)

![image](images/2g.jpg)Click on the expansion arrow beside the **Common Controls** category heading to expand the list of the most commonly used visual controls. Usefully, each control name appears beside an icon depicting that control as a reminder. You can click on the category heading again to collapse the list, then expand the other categories to explore the range of controls available to build your application interfaces

![image](images/pgc134_2.jpg)

![image](images/forget.jpg)

Any pinned Window in the IDE can be dragged from its usual location to any position you prefer. Drag it back to the initial location to re-dock it.

![image](images/hot.jpg)

The **Toolbox** will automatically hide when you click on another part of the IDE, but it can be fixed in place so it will never hide, using the ![image](images/pgc134_3.jpg) **Pin** button on the Toolbox bar.

![image](images/3g.jpg)Find the **Button** item in the **Common Controls** category of the Toolbox, then drag it onto the Form in the Designer window. Alternatively, double-click the **Button** item to add it to the Form

![image](images/pgc135_1.jpg)

![image](images/pgc135_2.jpg)

![image](images/pgc135_3.jpg)

The **Button** control appears on the Form surrounded by “handles” that can be dragged to resize the button’s width and height.

![image](images/4g.jpg)Click the ![image](images/pgc135_4.jpg) **Start** button to run the application and see the Button control appear in its initial default state

![image](images/5g.jpg)Next, move the pointer over the **Button** control to see its appearance change to its “MouseHover” state

![image](images/pgc135_5.jpg)

![image](images/6g.jpg)Now, click and hold down the **Button** control to see its appearance change to its “MouseDown” state

![image](images/pgc135_6.jpg)

![image](images/7g.jpg)Finally, release the **Button** control to see its appearance change to its “MouseUp” state

![image](images/pgc135_7.jpg)

Each change of appearance is Windows’ default response to an event that occurs on the **Button** control, but your C# program can provide its own response to these, and many more, control events:

![image](images/8g.jpg)Select the **Button** control then open its **Properties** window

![image](images/9g.jpg)Click the **Events** button and scroll down to see all possible **Button** events

![image](images/pgc135_8.jpg)

![image](images/hot.jpg)

A **Button** is one of the most useful interface controls – your program determines what happens when the user clicks it.

![image](images/forget.jpg)

This **Button** control performs no function when it’s clicked – until you add some code.

![image](images/hot.jpg)

Each control can be given a more meaningful name in the **Properties** window, but for simplicity, the default names are used by the examples in the C# section of this book.

**Writing functional code**

The Visual Studio IDE automatically generates code in the background, to incorporate the visual controls you add to your program interface. Additional code can be added manually to the “code-behind” page using the IDE’s integral **Code Editor**, to determine how your program should respond to interface events:

Using the project created [here](#chapter31.xhtml_sec243), follow these steps to add your own responses to user actions that produce events:

![image](images/commonag.jpg)

FirstGUI (continued)

![image](images/1g.jpg)Select the **Button** control named **button1**, then open its **Properties** window and click the **Events** button

![image](images/2g.jpg)Double-click on the **MouseHover** item to open a Form1.cs code-behind page in the **Code Editor** at a generated event-handler method

![image](images/pgc136_1.jpg)

![image](images/3g.jpg)Next, insert this statement within the generated method – to change the **Button**’s background color in response to a **MouseHover** event

**button1.BackColor = Color.Fuchsia ;**

![image](images/pgc136_2.jpg)

![image](images/4g.jpg)Similarly, double-click on the **MouseDown** item and insert this statement within another generated method – to change the **Button**’s background color in response to a **MouseDown** event

**button1.BackColor = Color.Lime ;**

![image](images/5g.jpg)Likewise, double-click on the **MouseUp** item and insert this statement within a further generated method – to change the **Button**’s background color in response to a **MouseUp** event

**button1.BackColor = Color.Aqua ;**

![image](images/hot.jpg)

Use the tabs to switch between the **Code Editor** and the **Form Designer**.

![image](images/hot.jpg)

The **Color** class provides lots of standard color properties – type **Color** then a period and use IntelliSense to see them.

![image](images/snake.jpg)

The lines of code in this example are to be inserted into each individual event-handler method that is automatically generated by Visual Studio.

![image](images/6g.jpg)Now, click the Form1.cs [Design] tab to return to the **Form Designer** window

![images](images/pgc137_1.jpg)

![image](images/7g.jpg)Double-click on the **Button** control on the Form to open the **Form1.cs** code-behind page in the **Code Editor** at yet another generated event-handler method

![image](images/8g.jpg)Finally, insert this statement within the generated method – to open a message box in response to a **Click** event

**MessageBox.Show( “C# Programming in easy steps” ) ;**

![image](images/9g.jpg)Run the application, then click the button to see the **MouseHover**, **MouseDown**, and **Click** event responses

![image](images/pgc137_2.jpg)

![image](images/pgc137_3.jpg)

![image](images/pgc137_4.jpg)

![image](images/pgc137_5.jpg)

![image](images/10g.jpg)Push the **OK** button to close the message box and see the **MouseUp** event response

![image](images/pgc137_6.jpg)

![image](images/pgc137_7.jpg)

![image](images/hot.jpg)

You can use the **View** menu on the Menu Bar to open the **Code Editor**, the **Form Designer**, or any other window you require at any time.

![image](images/hot.jpg)

You can see many more uses for the **MessageBox** class [here](#chapter31.xhtml_sec248).

![image](images/forget.jpg)

Most Windows software works by responding to events. For example, when you press a key, a **KeyPress** event can call its event-handler to respond to that event.

**Gathering text entries**

A **TextBox** control can be added to a Form in a **Windows Forms Application** to allow the user to enter input. The current value within a **TextBox** can be assigned to a variable, typically in response to a **Button** Click event, for use inside the program code.

A new value can be assigned to a **TextBox** as output to the user, but the user can modify this value. Alternatively, output can be assigned to a **Label** control, which the user cannot modify:

![image](images/commonag.jpg)

Entry

![image](images/1g.jpg)Start a new **Windows Forms App**, then add a **TextBox**, a **Button**, and two **Label** controls

![image](images/pgc138_1.jpg)

![image](images/2g.jpg)Select the Form itself, then in the **Properties** window modify its **Appearance, Text** and **Layout, Height** values

![image](images/3g.jpg)Next, modify the **Text** property values of the **Button** control and **Label** controls so they look like this:

![image](images/pgc138_2.jpg)

![image](images/4g.jpg)Now, double-click the **Button** control to open the **Code** **Editor** at a generated **Click** event-handler

![image](images/5g.jpg)At the very beginning of the Form1 class block, add a variable with setter and getter methods

**private int num ;**

**public void setNum( int num ) { this.num = num ; }**

**public int getNum( ) { return num ; }**

![image](images/pgc138_3.jpg)

![image](images/hot.jpg)

A **Label** control is generally used to display static text.

![image](images/snake.jpg)

In the **Layout** property category, you must set **AutoSize** to **False** before you can adjust the **Width** and **Height** values in the **Size** property category. This is needed to allow multiple lines of text on a **Label** control.

![image](images/6g.jpg)In the Form1( ) constructor method block, insert statements to initialize the variable with a random value

**Random rnd = new Random( ) ;**

**setNum( rnd.Next( 1, 21 ) ) ;**

![images](images/pgc139_2.jpg)

![image](images/pgc139_1.jpg)

![image](images/7g.jpg)Then, add a method to compare two arguments and set a Label control’s Text property with an appropriate message

**public void rate( int guess, int num )**

**{**

**if ( guess < num ) label2.text = “Too Low!” ;**

**else**

**if ( guess > num ) label2.text = “Too High!” ;**

**else**

**label2.text = “*** Correct ***” ;**

**}**

![image](images/8g.jpg)Finally, insert statements within the **Button** Click event-handler to compare user input against the random value

**int guess = Convert.ToInt16( textBox1.text ) ;**

**rate( guess, getNum( ) ) ;**

![image](images/pgc139_3.jpg)

![image](images/9g.jpg)Press **Start** or **F5** to run the application and enter input to see the appropriate output messages

![image](images/pgc139_4.jpg)

![image](images/pgc139_5.jpg)

![image](images/pgc139_6.jpg)

![image](images/snake.jpg)

If you specify minimum and maximum arguments to the **Next( )** method, it will return a random integer between the specified minimum and maximum-1 – so specifying 21 will allow a maximum of 20.

![image](images/forget.jpg)

The content of a **TextBox** control is a string value – so it must be converted to a numeric data type for numeric comparison.

**Ticking option boxes**

A **CheckBox** control is a small box with a caption. It lets the user select the caption choice by clicking on the box, and a check mark appears in the box to indicate it has been chosen. Clicking the box once more deselects the choice and unchecks the box. **CheckBox** controls are ideal to present a set of choices from which the user can select none, one, or more than one choice.

A **RadioButton** control is like a **CheckBox**, but with one crucial difference – the user can check only one choice in the group. Checking a **RadioButton** automatically unchecks any others. **RadioButton** controls are ideal to present a set of choices from which the user can select only one choice.

Selected **CheckBox** and **RadioButton** items can usefully be added to the collection displayed in a **ListBox** control:

![image](images/commonag.jpg)

Option

![image](images/1g.jpg)Start a new **Windows Forms App**, then add **RadioButton**, **CheckBox**, **ListBox**, **Button**, and **Label** controls to the Form

![image](images/pgc140_1.jpg)

![image](images/2g.jpg)Modify the **Text** property values of the controls to look like this:

![image](images/pgc140_2.jpg)

![image](images/3g.jpg)Now, double-click the “Show Selection” **Button** control to open the **Code Editor** at its generated Click event-handler

![image](images/snake.jpg)

You must set one **RadioButton** control to **Checked** to specify a default option.

![image](images/forget.jpg)

The name of the **ListBox** control that appears in the Form Designer will not be displayed when the application runs.

![image](images/4g.jpg)In the Form1( ) constructor method block, insert a statement to specify a default option

**radioButton1.Checked = true ;**

![images](images/pgc141_1.jpg)

![image](images/5g.jpg)Next, insert a statement within the “Show Selection” **Button** Click event-handler to empty any listed items

**listBox1.Items.Clear( ) ;**

![image](images/6g.jpg)Insert statements within the “Show Selection” **Button** Click event-handler to add selected options to the list

**if ( radioButton1.Checked )**

**listBox1.Items.Add( radioButton1.Text ) ;**

**if ( radioButton2.Checked )**

**listBox1.Items.Add( radioButton2.Text ) ;**

**if ( checkBox1.Checked )**

**listBox1.Items.Add( checkBox1.Text ) ;**

**if ( checkBox2.Checked )**

**listBox1.Items.Add( checkBox2.Text ) ;**

![image](images/7g.jpg)Now, double-click the “Clear” **Button** control to open the **Code Editor** at its generated Click event-handler

![image](images/8g.jpg)Insert statements within the “Clear” **Button** Click event-handler to reset all the options

**listBox1.Items.Clear( ) ;**

**radioButton1.Checked = true ;**

**checkBox1.Checked = false ;**

**checkBox2.Checked = false ;**

![image](images/9g.jpg)Press **Start** or **F5** to run the application and select options to see them appear in the list – then hit **Clear**

![image](images/pgc141_2.jpg)

![image](images/pgc141_3.jpg)

![image](images/hot.jpg)

The **ListBox** control has an **Items** property that provides methods to add or remove list items from a collection.

**Showing user messages**

The features of a MessageBox dialog can be determined by adding three further arguments after the message string within its Show( ) method. These can specify a caption, which buttons the dialog will display, and which graphic icon will appear on the dialog.

![images](images/pgc142_1.jpg)

| **MessageBoxButtons** | **Constants** |
| **AbortRetryIgnore** |  |
| **OK** |  |
| **OKCancel** |  |
| **RetryCancel** |  |
| **YesNo** |  |
| **YesNoCancel** |  |

The dialog button combinations can be specified using the MessageBoxButtons constant values listed in this table. For example, to have the dialog display **Yes**, **No**, and **Cancel** buttons, specify the MessageBoxButtons. YesNoCancel constant.

| **MessageBoxIcon** | **Constants** |
| **Error Hand Stop** | ![image](images/pgc142_2.jpg) |
| **Question** | ![image](images/pgc142_3.jpg) |
| **Exclamation Warning** | ![image](images/pgc142_4.jpg) |
| **Asterisk Information** | ![image](images/pgc142_5.jpg) |
| **None** |  |

The dialog icon can be specified using the MessageBoxIcon constant values listed in this table. For example, to have the dialog display the question mark icon, specify the MessageBoxIcon.Question constant.

When the user presses a MessageBox dialog button it returns an appropriate DialogResult constant value to the program. These are named exactly as the individual button label they represent. For example, any MessageBox dialog **OK** button returns the DialogResult.OK constant. The program can therefore examine the returned value to determine how to proceed.

![image](images/forget.jpg)

A **MessageBox** is “modal” – the user must deal with its dialog message before the program can proceed.

![image](images/hot.jpg)

Always specify a graphic icon when calling a **MessageBox** dialog to help the user easily understand the nature of the message.

![image](images/commonag.jpg)

Message

![image](images/1g.jpg)Start a new **Windows Forms App**, then add a **Button**, a **TextBox**, and a **Label** control to the Form

![image](images/pgc143_1.jpg)

![image](images/2g.jpg)Double-click the “Show Message” **Button** control to open the **Code Editor** at its generated Click event-handler

![image](images/3g.jpg)Insert a block within the “Show Message” **Button Click** event-handler to deliberately throw an exception

**try**

**{**

**throw new NotImplementedException( ) ;**

**}**

**catch ( NotImplementedException notImp )**

**{**

**// Statements to be inserted here (Steps 4-5 ).**

**}**

![image](images/4g.jpg)Add a statement to assign the user’s decision to a variable

**DialogResult result =**

**MessageBox.Show( “Proceed?”, notImp.Message ,**

**MessageBoxButtons.YesNo , MessageBoxIcon.Error ) ;**

![image](images/5g.jpg)Now, add statements to respond to the user’s decision

**textBox1.Text = result.ToString( ) ;**

**if( result == DialogResult.Yes ) label1.Text = “Proceeding...” ;**

**if( result == DialogResult.No ) label1.Text = “Stopping...” ;**

![image](images/6g.jpg)Press **Start** or **F5** to run the application and use the MessageBox buttons to determine how to proceed

![image](images/pgc143_2.jpg)

![image](images/pgc143_3.jpg)

![image](images/pgc143_4.jpg)

![image](images/hot.jpg)

This technique of throwing a **NotImplementedException** is favored by some programmers as a reminder to complete an unfinished part of the program code.

![image](images/hot.jpg)

Alternatively, this program could stop by calling the form’s **Close( )** method in response to **DialogResult.No**.

**Calling system dialogs**

![images](images/pgc144_1.jpg)

Visual Studio makes it simple to add the ability to call upon the standard Windows selection dialogs so the user can choose options within your applications – for example, calling the Color dialog to pick a color, calling the Font dialog to choose font options, or calling the Open dialog to select an image:

![image](images/commonag.jpg)

Dialog

![image](images/1g.jpg)Start a new **Windows** **Forms App** and add a **PictureBox**, a **TextBox**, and three **Button** controls to the Form

![image](images/pgc144_2.jpg)

![image](images/2g.jpg)From the **Dialogs** section of the **Toolbox**, add a **ColorDialog**, a **FontDialog**, and an **OpenFileDialog** component to the Form – see them appear in the **Component Tray** at the bottom of the Form Designer

![image](images/pgc144_3.jpg)

![image](images/3g.jpg)Double-click the first **Button** to open the **Code Editor** at its generated Click event-handler, then insert this code to change the background color of the **Form**

**if ( colorDialog1.ShowDialog( ) == DialogResult.OK )**

**this.BackColor = colorDialog1.Color ;**

![image](images/4g.jpg)Double-click the second **Button** to open the **Code Editor** at its generated Click event-handler, then insert this code to change the font of the **TextBox** control

**if ( fontDialog1.ShowDialog( ) == DialogResult.OK )**

**textBox1.Font = fontDialog1.Font ;**

![image](images/5g.jpg)Double-click the third **Button** to open the **Code Editor** at its generated Click event-handler, then insert this code to choose an image for the **PictureBox** control

**if ( openFileDialog1.ShowDialog( ) == DialogResult.OK )**

**{**

**// Statements to be inserted here (Step 6).**

**}**

![image](images/forget.jpg)

The **DialogResult.OK** value indicates the user pressed the **OK** button – just as it does in the **MessageBox** example [here](#chapter31.xhtml_step1).

![image](images/hot.jpg)

The **SaveFileDialog** is demonstrated in the example [here](#chapter31.xhtml_step7).

![image](images/6g.jpg)Insert a block to assign a selected image or display an error message

**try**

**{**

**pictureBox1.SizeMode =**

**PictureBoxSizeMode.StretchImage ;**

**pictureBox1.Image =**

**new Bitmap( openFileDialog1.FileName ) ;**

**}**

**catch ( Exception )**

**{**

**MessageBox.Show( “Error: Select An Image File!” , “ “,**

**MessageBoxButtons.OK, MessageBoxIcon.Error ) ;**

**}**

![image](images/7g.jpg)Press **Start** or **F5** to run the application and call the system dialogs to choose program options

![image](images/pgc145_1.jpg)

![image](images/pgc145_2.jpg)

![image](images/pgc145_3.jpg)

![image](images/pgc145_4.jpg)

![image](images/pgc145_5.jpg)

![image](images/pgc145_6.jpg)

![image](images/pgc145_7.jpg)

![image](images/hot.jpg)

The **PictureBoxSizeMode. StretchImage** property will stretch, or shrink, a selected image to fit the **PictureBox** dimensions as a new **Bitmap** image.

**Creating application menus**

Drop-down menus, toolbars, and status bars, like those found in most Windows applications, can easily be added to your own C# GUI applications from the Toolbox:

![image](images/commonag.jpg)

Jotter

![image](images/1g.jpg)Start a new **Windows Forms App** and find the **Menus** **& Toolbars** section of the Toolbox, then double-click the **MenuStrip** item to add it to the Form

![image](images/2g.jpg)Click the MenuStrip control’s ![image](images/pgc146_4.jpg) arrow button to open its **Smart Tag**, then select **Insert Standard Items**

![image](images/pgc146_1.jpg)

![image](images/3g.jpg)Right-click on any of familiar items and use the context menu to edit that item. Also, type new custom items into the **Type Here** box as required

![image](images/pgc146_2.jpg)

![image](images/pgc146_3.jpg)

![image](images/4g.jpg)In the Toolbox, double-click on the **ToolStrip** item to add it to the Form, then open its **Smart Tag** and once more select **Insert Standard Items**

![image](images/hot.jpg)

Alternatively, you can create your own custom menus using the **Type Here** box instead of **Insert Standard Items**.

![image](images/5g.jpg)When the familiar icon buttons have been added to the **ToolStrip**, right-click on any item and use the context menu to edit that item. Also add further custom items from the drop-down list as required

![image](images/pgc147_2.jpg)

![image](images/pgc147_1.jpg)

![image](images/6g.jpg)In the Toolbox, double-click on the **StatusStrip** item to add it to the Form

![image](images/7g.jpg)Select the **StatusLabel** item on the StatusStrip drop-down list, and set its **Text** property to “Ready”

![image](images/pgc147_3.jpg)

![image](images/8g.jpg)Add a **RichTextBox** control to the center of the Form, open its **Smart Tag** and select the option to **Dock in parent container**, then ensure that its **ScrollBars** property is set to **Both**

![image](images/pgc147_4.jpg)

![image](images/pgc147_5.jpg)

![image](images/hot.jpg)

Use **StatusBar** messages to provide feedback to the user.

![image](images/forget.jpg)

The menus are not truly functional until you add some program code – as described [here](#chapter31.xhtml_sec251).

**Making menus work**

The menu items and toolbar buttons created [here](#chapter31.xhtml_sec250) will not truly function until you add code to make them work. For actions that appear both in a menu and on a button, you can create a method that can be called from the Click event-handler of the menu item and that of the button – to avoid duplication:

![image](images/commonag.jpg)

Jotter (continued)

![image](images/1g.jpg)In Form Designer, click the app’s **File** menu item to open its drop-down menu

![image](images/pgc148_1.jpg)

![image](images/2g.jpg)Double-click on the **New** menu item to open the **Code Editor** in its Click event-handler, and add this method call

**newFile( ) ;**

![image](images/3g.jpg)After the Click event-handler block, add this method to clear any existing text and display a status message

**private void newFile( )**

**{**

**richTextBox1.Text = null ;**

**toolStripStatusLabel1.Text = “Ready” ;**

**}**

![image](images/4g.jpg)Return to the **Form Designer**, then double-click on the ![image](images/pgc148_3.jpg) **New** toolbar button to open the **Code Editor** in that event-handler, and add a call to the method above

**newFile( ) ;**

![image](images/5g.jpg)Add an **OpenFileDialog** and **SaveFileDialog** component from the **Dialogs** section of the **Toolbox**

![image](images/pgc148_2.jpg)

![image](images/6g.jpg)In the Click event-handlers of both the **Open** menu item and the **Open** toolbar button, add this method call

**openFile( ) ;**

![image](images/forget.jpg)

When you enable New, Open, and Save dialogs, keyboard shortcuts are already configured – try **Ctrl** + **N**, **Ctrl** + **S**, and **Ctrl** + **O** to test them.

![image](images/7g.jpg)After the Click event-handler blocks, add this method to load a plain text file

**private void openFile( )**

**{**

**openFileDialog1.FileName = ““ ;**

**openFileDialog1.Filter = “Text Files | *.txt” ;**

**if ( openFileDialog1.ShowDialog( ) == DialogResult.OK )**

**{**

**richTextBox1.LoadFile( openFileDialog1.FileName ,**

**RichTextBoxStreamType.PlainText ) ;**

**}**

**}**

![images](images/pgc149_1.jpg)

![image](images/8g.jpg)In the Click event-handlers of both the **Save** menu item and the **Save** toolbar button, add this method call

**saveFile( ) ;**

![image](images/9g.jpg)After the Click event-handler blocks, add this method to save a plain text file

**private void saveFile( )**

**{**

**saveFileDialog1.Filter = “Text Files | *.txt” ;**

**if ( saveFileDialog1.ShowDialog( ) == DialogResult.OK )**

**{**

**richTextBox1.SaveFile( saveFileDialog1.FileName ,**

**RichTextBoxStreamType.PlainText ) ;**

**}**

**}**

![image](images/10g.jpg)Press **Start** or **F5** to run the application and test the functionality of the **New**, **Open**, and **Save** file menu items and toolbar buttons

![image](images/pgc149_2.jpg)

![image](images/pgc149_3.jpg)

![image](images/hot.jpg)

You can change the Filter to **“RichText | *.rtf”** and the **RichTextBoxStreamType** property to **.RichText** for files with embedded objects such as images.

![image](images/hot.jpg)

To make the **File**, **Exit** menu item functional, simply add the call **Application.Exit( ) ;** to its **Click** event-handler.

**Importing audio resources**

Sound files can be imported into an application as a resource, in much the same way that image files can be imported as a resource, to enhance the application. These can then be played as required:

![image](images/commonag.jpg)

Sound

![image](images/1g.jpg)Start a new **Windows** **Forms App**, then add a **Label** and a **Button** control to the Form

![image](images/pgc150_1.jpg)

![image](images/2g.jpg)In Solution Explorer, right-click on the project item and select **Add**, **New Item**

![image](images/3g.jpg)Choose the **Resources File** option and name the file Imported.resx, then click the **Add** button

![image](images/pgc150_2.jpg)

![image](images/4g.jpg)In Solution Explorer, double-click the newly added Imported.resx item to open its resources window

![image](images/5g.jpg)Select **Audio** and **Add Resource**, **Add Existing File...** from the drop-down menus to open a dialog

![image](images/pgc150_3.jpg)

![image](images/snake.jpg)

Only sound files in the WAV format (.wav) can be imported as audio resources.

![image](images/hot.jpg)

You can typically find the Windows sound files in the folder on your computer at **C:\Windows\Media**.

![image](images/6g.jpg)Browse to select an audio file, then click the **Open** button to add it to the project’s Resources – here, it’s chimes.wav

![image](images/pgc151_2.jpg)

![image](images/pgc151_1.jpg)

![image](images/7g.jpg)On the Menu Bar, click **Build**, **Build Solution** to generate an Imported.chimes class that calls a ResourceManager.GetStream() method

![image](images/pgc151_3.jpg)

![image](images/8g.jpg)Double-click the **Button** control, then add this statement above its Click event-handler block to create an object

**System.Media.SoundPlayer chimes =**

**new System.Media.SoundPlayer( Imported.chimes ) ;**

![image](images/9g.jpg)Now, add these statements inside the **Button** control’s Click event-handler to play the sound and show a message

**chimes.Play( ) ;**

**label1.Text = “Playing chimes...” ;**

![image](images/10g.jpg)Press **Start** or **F5** to run the application and push the **Button** to hear the sound play

![image](images/pgc151_4.jpg)

![image](images/hot.jpg)

Notice that the sound file name only is dot-suffixed to **Imported** – without its file extension but the case must match that of the imported file name. A sound can be played repeatedly using the **PlayLooping( )** method – and the loop can be ended with the **Stop( )** method.

**Summary**

![image](images/pgc152_1.jpg)

•The **Windows Forms App** template in the “Create a new project” dialog is used to begin a Windows GUI project.

•The **Form Designer** window of the Visual Studio IDE is where you create the application’s visual interface.

•The **Properties** window contains details of the item that is currently selected in the **Form Designer** window.

•The **Common Controls** section of the **Toolbox** contains a wide range of visual controls to build GUI applications.

•The **Code Editor** is used to create the code-behind page that determines how the application responds to interface events.

•When the user pushes a **Button** control, it creates a Click event to which its event-handler can respond.

•User input into a **TextBox** control can be assigned to a variable for use within the application.

•The user cannot directly enter text on a **Label** control.

•Only one option can be checked in a **RadioButton** group, but any number of options can be checked in a **CheckBox** group.

•A **ListBox** control has an Items property that provides methods to add or remove items from the list it contains.

•The Show( ) method of the MessageBox class accepts arguments to specify a message, caption, buttons, and icon.

•The **Dialogs** section of the **Toolbox** contains components that allow an application to use the Windows system dialogs.

•The **Menus & Toolbars** section of the **Toolbox** contains components that allow an application to include the familiar Windows system menu items.

•The **Menus & Toolbars** components will not truly function until code is added to their Click event-handlers.

•The **Solution Explorer** window can be used to import resources into an application project.

•A SoundPlayer object can be created using the System.Media class, and provides methods to handle audio resources.

**32**

**Building an application**

*This chapter demonstrates how to create, test, and publish a simple C# program application.*

[**Planning the program**](#chapter32.xhtml_sec254)

[**Assigning fixed properties**](#chapter32.xhtml_sec255)

[**Designing the layout**](#chapter32.xhtml_sec256)

[**Setting dynamic properties**](#chapter32.xhtml_sec257)

[**Adding runtime function**](#chapter32.xhtml_sec258)

[**Testing the program**](#chapter32.xhtml_sec259)

[**Publishing the application**](#chapter32.xhtml_sec260)

[**Summary**](#chapter32.xhtml_sec261)

**Planning the program**

When creating a new application it is useful to spend some time planning its design. Clearly define the program’s precise purpose, decide what application functionality will be required, then decide what interface components will be needed.

![images](images/pgc154_1.jpg)

A plan for a simple application to pick numbers for a lottery game entry might look like this:

**Program purpose**

•The program will generate a series of six different random numbers in the range 1–59, and have the ability to be reset.

**Functionality required**

•A random number generator.

•A method to display six different random numbers.

•A method to clear the last series from display.

![image](images/snake.jpg)

Omission of the planning stage can require time-consuming changes to be made later. It’s better to “plan your work, then work your plan”.

**Components needed**

•Six **Label** controls to display the series of numbers – one number per Label.

•One **Button** control to generate and display the numbers in the Label controls when this Button is clicked. This Button will not be enabled when numbers are on display.

•One **Button** control to clear the numbers on display in the Label controls when this Button is clicked. This Button will not be enabled when no numbers are on display.

•One **PictureBox** control to display a static image – just to enhance the appearance of the interface.

![image](images/hot.jpg)

Toggle the value of a Button’s **Enabled** property to steer the user. In this case, the application must be reset before a further series of numbers can be generated.

Having established a program plan means you can now create the application basics by adding the components needed to a Form:

![image](images/commonap.jpg)

Lotto

![image](images/1p.jpg)Open the Visual Studio IDE and create a new **Windows Forms App (.NET Framework)**, then name it “Lotto”

![image](images/pgc155_1.jpg)

![image](images/2p.jpg)In the **Form Designer**, add six **Label** controls to the Form from the **Toolbox**

![image](images/3p.jpg)Now, add two **Button** controls and a **PictureBox** control to the Form

![image](images/pgc155_2.jpg)

![image](images/forget.jpg)

You can drag and drop items from the **Toolbox**, or double-click them to add them to the Form.

**Assigning fixed properties**

Having created the application basics [here](#chapter32.xhtml_program), you can now assign static values using the **Properties** window:

![image](images/commonap.jpg)

Lotto (continued)

![image](images/1p.jpg)Click on the Form to select it, then in the **Properties** window, set the Form’s **Appearance, Text** property to “Lotto Number Picker”

![image](images/pgc156_1.jpg)

![image](images/2p.jpg)Select the first **Button** control, then change its **Design, (Name)** to BtnPick, and its **Appearance,** **Text** to “Get My Lucky Numbers”

![image](images/pgc156_2.jpg)

![image](images/3p.jpg)Select the second **Button** control, then change its **Design, (Name)** to BtnReset, and its **Appearance,** **Text** to “Reset”

![image](images/pgc156_3.jpg)

![image](images/4p.jpg)Select the **PictureBox** control, then click the **Choose** **Image...** link to launch the **Select** **Resource** dialog

![images](images/pgc156_4.jpg)

![image](images/forget.jpg)

You can open the **Properties** window using the **F4** key, or by clicking **View**, **Properties Window** on the Menu Bar.

![image](images/hot.jpg)

The **Label** controls in this program will have their Text property values assigned dynamically at runtime – no initial properties are required.

![image](images/5p.jpg)Select the **Project resource file** option, then click the **Import...** button and browse to the image location

![image](images/pgc157_2.jpg)

![image](images/pgc157_1.jpg)

![image](images/6p.jpg)Click the **OK** button to import the image resource and see it get added to the project

![image](images/pgc157_3.jpg)

![image](images/pgc157_4.jpg)

![image](images/7p.jpg)Click **File, Save All** or press the **Ctrl + Shift + S** keys to save the changes made to the project

![image](images/hot.jpg)

You can use the drop-down list at the top of the **Properties** window to select any control on the form.

![image](images/snake.jpg)

Save your project periodically as you build it using **File**, **Save All** on the Menu Bar or **Ctrl** + **Shift** + **S** keys.

**Designing the layout**

Having assigned fixed property values [here](#chapter32.xhtml_sec255), you can now design the interface layout.

The size of both the **PictureBox** control and the **BtnPick** control first needs to be adjusted to accommodate their content. This can easily be achieved by specifying an **AutoSize** value so that Visual Studio will automatically fit the control neatly around its content:

![image](images/commonap.jpg)

Lotto (continued)

![image](images/1p.jpg)Select the **PictureBox** control, then in the **Properties** window, change its **Behavior, SizeMode** to **AutoSize**

![image](images/pgc158_1.jpg)

![image](images/2p.jpg)Select the BtnPick control, then in the **Properties** window, set its **Layout**, **AutoSize** property to **True** – see that the **PictureBox** control now fits snugly around the image, and the BtnPick control has expanded to fit its text

![images](images/pgc158_2.jpg)

![image](images/3p.jpg)Hold down the left mouse button and drag around the Labels to select all **Label** controls

![image](images/4p.jpg)Now, click **View**, **Toolbars**, **Layout** to ensure that the Layout toolbar is enabled

![image](images/5p.jpg)Click the **Align Tops** button to stack the Labels in a pile

![image](images/pgc158_3.jpg)

![image](images/hot.jpg)

Alternatively, you can use the **Smart Tag** arrow button on a **PictureBox** control to set its **SizeMode** property.

![image](images/snake.jpg)

Ensure that all PictureBox **Margin** properties are set to zero if you do not require margins around the image.

![image](images/6p.jpg)Click the **Make Horizontal Spacing Equal** toolbar button to arrange the pile of Labels into a row

![image](images/pgc159_2.jpg)

![image](images/pgc159_1.jpg)

![image](images/7p.jpg)Use the Form’s right grab handle to extend its width to accommodate the row of Labels and **PictureBox**, then drag the row and both Buttons to the top-right of the Form

![image](images/8p.jpg)Drag the **PictureBox** control to the top-left of the Form, then use the Form’s bottom grab handle to adjust its height to match that of the image

![image](images/pgc159_3.jpg)

![image](images/9p.jpg)Use the **Snap Lines** that appear when you drag controls around the Form to position the row of Labels and the Buttons to make the interface look like the layout below

![image](images/pgc159_4.jpg)

![image](images/10p.jpg)Set the Form’s **Window Style**, **MaximizeBox** and **MinimizeBox** properties to **False**, as **Maximize** and **Minimize** buttons are not required on this interface

![image](images/forget.jpg)

In this case, it does not matter in what order the Labels appear in the row.

![image](images/hot.jpg)

Avoid the temptation to change the default styles of Form controls so they remain familiar to users.

**Setting dynamic properties**

Having designed the interface [here](#chapter32.xhtml_sec256), you can now add some functionality to dynamically set the initial **Text** properties of the **Label** controls and the initial **Button** states:

![image](images/commonap.jpg)

Lotto (continued)

![image](images/1p.jpg)Click **View**, **Code** on the Menu Bar, or press **F7**, to open the **Code Editor** window

![image](images/2p.jpg)After the **Form1( )** constructor method block, add a new method block

**private void Clear( )**

**{**

**// Statements to be inserted here (Steps 4-8).**

**}**

![image](images/3p.jpg)With the cursor inside the new method block, press **Ctrl** + **J**, to open the **IntelliSense** pop-up window

![image](images/4p.jpg)Scroll down the list of items in the **IntelliSense** window and double-click on the **label1** item to add it into the **Clear( )** method block

![image](images/pgc160_1.jpg)

![image](images/5p.jpg)Type a period, then double-click the **Text** item when the **IntelliSense** window reappears, to add that code

![image](images/forget.jpg)

The technique described here demonstrates how to use **IntelliSense** – but you can, of course, just type the code directly.

![image](images/6p.jpg)Now, type = “...” ; to complete the line so it reads like this:

**label1.Text = “...” ;**

![images](images/pgc161_1.jpg)

![image](images/7p.jpg)Repeat this procedure for the other **Label** controls – so that the **Clear( )** method assigns each an ellipsis string

![image](images/8p.jpg)With the cursor inside the **Clear( )** method block, use **IntelliSense** in the same way, to add these two lines:

**BtnPick.Enabled = true ;**

**BtnReset.Enabled = false ;**

This completes the **Clear( )** method functionality by setting the **Button** states. All that remains is to add a call to the **Clear( )** method to execute all of its instructions when the program starts.

![image](images/9p.jpg)In the **Form Designer**, double-click on the Form to open the **Code Editor** in its **Load** event-handler, then press **Ctrl** + **J** to open the **IntelliSense** window

![image](images/10p.jpg)Scroll down the list in the **IntelliSense** window and double-click on the **Clear** item you have just created, to add a call statement in the **Load** event-handler

![image](images/pgc161_2.jpg)

![image](images/hot.jpg)

Type “Intellisense” into the Quick Launch box at the top of the Visual Studio window to discover the IntelliSense Menus and Options.

**Adding runtime function**

Having created code to initialize dynamic properties [here](#chapter32.xhtml_sec257), you can now add runtime functionality to respond to clicks on the **Button** controls:

![image](images/commonap.jpg)

Lotto (continued)

![image](images/1p.jpg)In the **Form Designer**, double-click on the **BtnReset Button** control to open the **Code Editor** in its Click event-handler, then add this method call

**Clear( ) ;**

This is all that is needed to provide dynamic functionality for the **BtnReset** control. The main dynamic functionality of this application is provided by the **BtnPick** control, which requires an instance of a **Random** class, random number generator object:

![image](images/2p.jpg)In the **Form Designer**, double-click on the **BtnPick Button** control to open the **Code Editor** in its Click event-handler

![image](images/3p.jpg)In the **Click** event-handler block, add this statement to create a random number generator object

**Random rnd = new Random( ) ;**

![image](images/4p.jpg)Next, add a statement to create an array of 59 elements to store a sequence of numbers

**int [ ] seq = new int[ 59 ] ;**

![image](images/5p.jpg)Now, add a loop to fill the array elements (index 0 to 58) with integer values 1 to 59

**for ( int i = 1 ; i < 60 ; i++ )**

**{**

**seq[ i - 1 ] = i ;**

**}**

![image](images/6p.jpg)Add a second loop to shuffle the values within all the array elements – an algorithm to randomize their order

**for ( int i = 0 ; i < 59 ; i++ )**

**{**

**int j = ( rnd.Next( ) % 59 ) ;**

**int k = seq[ i ] ; seq[ i ] = seq[ j ] ; seq[ j ] = k ;**

**}**

![image](images/hot.jpg)

The random number generator is used here to generate random values between 0 and 58 to shuffle array elements.

![image](images/forget.jpg)

You don’t need to understand in detail the algorithm that is used to shuffle the values.

![image](images/7p.jpg)Next, add the following lines to display the numbers contained in array elements 1-6 in the **Label** controls

**label1.Text = seq[ 1 ].ToString( ) ;**

**label2.Text = seq[ 2 ].ToString( ) ;
label3.Text = seq[ 3 ].ToString( ) ;
label4.Text = seq[ 4 ].ToString( ) ;
label5.Text = seq[ 5 ].ToString( ) ;
label6.Text = seq[ 6 ].ToString( ) ;**

![images](images/pgc163_1.jpg)

![image](images/8p.jpg)Now, add these two lines to set the **Button** states ready to reset the application

**BtnPick.Enabled = false ;**

**BtnReset.Enabled = true ;**

![image](images/9p.jpg)Add comments for others examining the code, and for yourself when revisiting the code later – for example, maybe to explain the algorithm that shuffles the numbers

![image](images/pgc163_2.jpg)

![image](images/10p.jpg)Click **File, Save All** or press the **Ctrl** + **Shift** + **S** keys to save the changes made to the project code-behind page

![image](images/snake.jpg)

**Label** controls can only contain **string** values, so the **int** numeric values must be converted.

**Testing the program**

Having worked through the program plan on the previous pages, the components needed and functionality required have now been added to the application – so it’s ready to be tested:

![image](images/commonap.jpg)

Lotto (continued)

![image](images/1p.jpg)Click the **Start** button, or press **F5**, to run the application then examine its initial start-up appearance

![image](images/pgc164_1.jpg)

The Form’s **Load** event-handler has set the initial dynamic values of each **Label** control and disabled the reset button as required.

![image](images/2p.jpg)Click the **BtnPick Button** control to execute the instructions within its **Click** event-handler

![image](images/pgc164_2.jpg)

![image](images/hot.jpg)

Notice that no number is repeated in any series.

A series of numbers within the desired range is displayed, and the **Button** states have changed as required – a further series of numbers cannot be generated until the application has been reset.

![image](images/3p.jpg)Make a note of the numbers generated in this first series for comparison later

![image](images/4p.jpg)Click the **BtnReset** control to execute the instructions within that **Click** event-handler and see the application return to its initial start-up appearance as required

![image](images/pgc165_2.jpg)

![image](images/pgc165_1.jpg)

![image](images/5p.jpg)Click the **BtnPick Button** control again to execute its **Click** event-handler code a second time

![image](images/pgc165_3.jpg)

Another series of numbers within the desired range is displayed and are different to those in the first series when compared – good, the numbers are being randomized as required.

![image](images/6p.jpg)Click the **Stop Debugging** button, then click the **Start** button to restart the application and click the **BtnPick Button** control once more

![image](images/pgc165_4.jpg)

The generated numbers in this first series of numbers are different to those noted in the first series the last time the application ran – great, the random number generator is not repeating the same sequence of number series each time the application runs.

![image](images/forget.jpg)

Remember that this application interface has no **Minimize** or **Maximize** buttons because their properties were set to false – see [here](#chapter32.xhtml_cing), Step 10.

![image](images/hot.jpg)

Alternatively, you can click the app’s **X** button to close the application and stop debugging.

**Publishing the application**

Having tested the application [here](#chapter32.xhtml_sec259), you can now create a standalone version for installation outside the Visual Studio IDE, and for deployment elsewhere.

![image](images/commonap.jpg)

Lotto (continued)

![image](images/1p.jpg)On the Menu Bar, click **Build**, **Publish Selection**, then select the **ClickOnce** option and click **Next**

![image](images/pgc166_1.jpg)

![image](images/2p.jpg)Now, use the wizard’s **Browse** button to select a location where you wish to publish the application – for example, into a folder created on a USB drive, then click **Next**

![images](images/pgc166_2.jpg)

![images](images/pgc166_3.jpg)

![image](images/3p.jpg)Then, choose how the app will be installed – for example, from a USB drive, then click **Next**

![image](images/4p.jpg)Choose a version number for the app, then click **Next**

![image](images/5p.jpg)Check the **Sign the ClickOnce manifests** box, then click **Select from store** and choose a certificate, or click **Create** **Test Certificate** for temporary testing only

![image](images/hot.jpg)

Applications signing is optional, but does verify authentication. Find more details online at **[learn.microsoft.com/en-us/visualstudio/ide/how-to-sign-application-and-deployment-manifests](http://www.learn.microsoft.com/en-us/visualstudio/ide/how-to-sign-application-and-deployment-manifests)**

![image](images/forget.jpg)

Each time you publish an application, its version number is automatically incremented – 1.0.0.0, 1.0.0.1, 1.0.0.2, etc.

![image](images/6p.jpg)Click the **Next** button to move to the final dialog page, confirm the listed choices, then click the **Finish** button

![image](images/pgc167_1.jpg)

![image](images/7p.jpg)Finally, click the **Publish** button to publish the application at the specified location

![image](images/pgc167_2.jpg)

The **Publish Wizard** generates a number of files, including a familiar “setup.exe” executable installer.

![image](images/8p.jpg)Move the portable media to the system where it is to be deployed, then run **setup.exe** to install the application

The installer will install the targeted .NET runtime if required and add a shortcut to the **All apps** menu that can be used to launch the application. The user can then run the application just as it performed during testing in the Visual Studio IDE.

![image](images/pgc167_3.jpg)

![image](images/pgc167_4.jpg)

![image](images/pgc167_5.jpg)

The installer also adds an item to the client system’s **Add/Remove** **Programs** list, which can be used to uninstall the application – just like any other Windows program.

**Summary**

![image](images/pgc168_1.jpg)

•Always make an initial program plan, to avoid the need for time-consuming changes later.

•A program plan should clearly define the program purpose, functionality required, and components needed.

•Fixed properties that will not change when the application is running can be set at design time in the **Properties** Window.

•The **Import** button in the **Select Resources** dialog can automatically assign an image to a **PictureBox** control.

•An **AutoSize** property value makes Visual Studio automatically fit a control neatly around its content.

•The Form Designer’s **Layout** toolbar contains useful features to quickly align and space multiple interface controls.

•**Snap Lines** help you to easily align a selected control to others in the interface at design time.

•Setting a Form’s **Window Style**, **MaximizeBox**, and **MinimizeBox** properties to **False** removes those buttons.

•Dynamic properties that will change when the application is running can be initialized with the Form’s **Load** event-handler.

•The pop-up **IntelliSense** window lets you easily add program code when using the **Code Editor**.

•Runtime functionality responds to user actions by changing dynamic properties.

•A **Debug** version of an application allows its functionality to be tested as the application is being created in text format.

•The **Build** process compiles a **Release** version of an application in binary format.

•The **Publish** process creates a final **Release** version with an installer so the application can be deployed elsewhere.

•Applications created with the Visual Studio IDE can be installed and uninstalled just like other Windows applications.

**33**

**Targeting devices**

***This chapter demonstrates how to create a Universal Windows Platform application using C# programming.***

[**Starting a Universal project**](#chapter33.xhtml_sec262)

[**Inserting page components**](#chapter33.xhtml_sec263)

[**Importing program assets**](#chapter33.xhtml_sec264)

[**Designing the layout**](#chapter33.xhtml_sec265)

[**Adding runtime function**](#chapter33.xhtml_sec266)

[**Testing the program**](#chapter33.xhtml_sec267)

[**Adjusting the interface**](#chapter33.xhtml_sec268)

[**Deploying the application**](#chapter33.xhtml_sec269)

[**Summary**](#chapter33.xhtml_sec270)

**Starting a Universal project**

![images](images/pgc170_1.jpg)

Windows 10 introduced the **Universal Windows Platform** (UWP) that enables you to create a single **Universal Windows** **Application** (UWA) that will run on any modern Windows-based device. The interface layout of a UWA uses the **eXtensible** **Application Markup Language** (XAML) to specify components. In order to develop apps for the UWP, you should be running Windows 10 or Windows 11, and your Visual Studio IDE must include the **Universal Windows App Development Tools**:

![image](images/commono.jpg)

Universal

![image](images/1o.jpg)Click **Visual Studio Installer** on the All apps menu, then click the **Modify** button on the Installer dialog

![images](images/pgc170_2.jpg)

![image](images/2o.jpg)See if the **Universal Windows Platform development** option box is checked in the **Desktop & Mobile** category on the **Workloads** tab – indicating this item is installed

![image](images/3o.jpg)If the box is not checked, check it now then click the **Modify** button at the bottom-right of the Installer dialog to download and install the **Universal Windows** **Platform development** tools

![image](images/4o.jpg)Select **File**, **New**, **Project** and create a new **C# Blank** **App (Universal Windows)** and name it “Universal” – for Windows, Desktop, Xbox, etc.

![images](images/pgc170_3.jpg)

![image](images/snake.jpg)

The example in this chapter is for Visual Studio 2022 on Windows 10 or 11 – it won’t work in earlier Windows editions.

![image](images/forget.jpg)

Depending upon your choices when you installed Visual Studio, you may see the options checked when the installer launches, to indicate you already have the **Universal Windows App development** tools.

![image](images/pgc171_1.jpg)

![image](images/5o.jpg)Click **OK** to accept the suggested target versions

![image](images/pgc171_2.jpg)

![image](images/6o.jpg)After Visual Studio creates the new project, select **View**, **Solution Explorer** to examine the generated files:

•A set of logo images in an **Assets** folder.

•Internal XAML and C# files for the **App**.

•XAML and C# files for the **MainPage** – here is where you will create interface components and functional code.

•Other miscellaneous **Package** files.

![image](images/pgc171_3.jpg)

![image](images/snake.jpg)

In Windows you should ensure that the **Developer Mode** option is enabled in **Settings**, **Privacy & Security**, **For developers**.

![image](images/forget.jpg)

These files are essential to all UWP apps using C#, and exist in every project Visual Studio creates to target the Universal Windows Platform with C#.

**Inserting page components**

Visual Studio provides a two-part window to insert interface components into a UWP app. This comprises a **Design** view of the components, and a **XAML** view for the XAML code:

![image](images/commonao.jpg)

Universal (continued)

![image](images/1o.jpg)Open **Solution Explorer** then double-click on **MainPage.xaml** – to launch a two-part window

![image](images/pgc172_1.jpg)

![image](images/2o.jpg)See that, by default, the **Design** view displays a blank canvas in **Landscape** mode, and the **Code** view contains some default code

![image](images/pgc172_2.jpg)

![image](images/hot.jpg)

You can select from a range of device emulators in this menu.

![image](images/hot.jpg)

Explore these buttons to change the magnification and grid characteristics.

There is a pop-out **Toolbox** feature that lets you add components onto the canvas, but you will need to edit them in the XAML code later. In this example, the components are created in XAML code from the very start.

![image](images/hot.jpg)

XAML is pronounced “zammel”. You can write XAML code in the **Code** view to add components to the canvas previewed in **Design** view.

![image](images/3o.jpg)Now, see that by default, the **XAML** view reveals there are <Grid> </Grid> tags – this is the root element of the canvas in which you can add component elements

![images](images/pgc173_1.jpg)

Component elements are best nested within a <StackPanel> element, as this can be given an x:Name for reference in functional code, and an Orientation attribute to specify the direction in which the nested elements should appear. Common component elements include <Image>, <TextBox>, <TextBlock> (label), and <Button>. Several <StackPanel> elements can be nested within each other to determine the Horizontal and Vertical layout of components:

![image](images/4o.jpg)Insert elements between the root <Grid> </Grid> tags, so the **XAML** code looks precisely like this:

**<Grid>**

**<StackPanel x:Name=”MainStack” Orientation=”Horizontal”>**

**<Image x:Name=”Image” Width=”200” Height=”200” />**

**<StackPanel x:Name=”Controls” Orientation=”Vertical”>**

**<StackPanel x:Name=”Labels” Orientation=”Horizontal”>**

**<TextBlock x:Name=”textBlock1” Text=”TextBlock” />**

**<TextBlock x:Name=”textBlock2” Text=”TextBlock” />**

**<TextBlock x:Name=”textBlock3” Text=”TextBlock” />**

**<TextBlock x:Name=”textBlock4” Text=”TextBlock” />**

**<TextBlock x:Name=”textBlock5” Text=”TextBlock” />**

**<TextBlock x:Name=”textBlock6” Text=”TextBlock” />**

**</StackPanel>**

**<StackPanel x:Name=”Buttons” Orientation=”Horizontal”>**

**<Button x:Name=”BtnPick” Content=”Button” />**

**<Button x:Name=”BtnReset” Content=”Button” />**

**</StackPanel>**

**</StackPanel>**

**</StackPanel>**

**</Grid>**

![image](images/5o.jpg)As you add the component elements in **XAML** view, they appear in the **Design** view until it looks like this:

![image](images/pgc173_2.jpg)

![image](images/hot.jpg)

The outer horizontal **<StackPanel>** contains an **<Image>** element, and a nested vertical **<Stackpanel>** containing two further horizontal **<StackPanel>** elements. The **x:** prefix before the **Name** attribute refers to the XAML schema used by UWP apps. Each **<TextBlock>** element has a **Text** attribute that can be referenced in functional code, such as **textBlock1->Text**.

**Importing program assets**

In order to have a XAML <Image> component display a graphic, an image file first needs to be added to the projects **Assets** folder. It can then be assigned to a Source attribute of the <Image> tag:

![image](images/commonao.jpg)

Universal (continued)

![image](images/1o.jpg)Open **Solution Explorer**, then right-click on the **Assets** folder and choose **Add** from the context menu

![image](images/2o.jpg)Now, choose **Existing Item...** from the next context menu – to open an **Add Existing Item** dialog box

![image](images/pgc174_1.jpg)

![image](images/3o.jpg)In the **Add Existing Item** dialog, browse to the location of an image, then select the file and click the **Add** button

![image](images/pgc174_2.jpg)

![image](images/hot.jpg)

An image for display may be in any popular file format – such as **.bmp**, **.gif**, **.jpg**, **.png**, or **.tif**.

![image](images/4o.jpg)In **Solution Explorer**, the selected image file now appears in the project’s **Asset** folder

![images](images/pgc175_1.jpg)

![image](images/5o.jpg)Select the Image component in **Designer** view, then click **View**, **Properties Window** to reveal its properties

![image](images/pgc175_2.jpg)

![image](images/6o.jpg)In the **Properties** window, expand the **Common** category, then click the **Source** item’s arrow button and select the added image from the drop-down list

![image](images/7o.jpg)The image now appears in the **Design** view, and its path gets added to the **XAML** code and **Source** property

![image](images/pgc175_3.jpg)

![image](images/pgc175_4.jpg)

![image](images/hot.jpg)

Explore the **Appearance** and **Transform** options in an image’s **Properties** window, to discover how you can modify how it will be displayed.

**Designing the layout**

To complete the app’s layout, design attributes can be added to the XAML element tags to specify what they will display and precisely where in the interface they will appear.

A single Margin value sets all four margins around a component. You can specify two values to set left and right, and top and bottom margins – for example, Margin = “10,30”. Alternatively, you can specify four values to set left, top, right, bottom margins individually – e.g. Margin = “10,30,10,50”.

![image](images/commonao.jpg)

Universal (continued)

![image](images/1o.jpg)Open **MainPage.xaml**, then add two attributes to the outer MainStack <StackPanel> element to fix its position

**HorizontalAlignment = ”Left” VerticalAlignment = ”Top”**

![image](images/2o.jpg)Next, edit the <Image> element by modifying the initial assigned value of 200 – to increase its width

**Width = ”300”**

![image](images/3o.jpg)Now, add an attribute to the nested Controls <StackPanel> element to fix its position

**VerticalAlignment = ”Center”**

![image](images/4o.jpg)Then, edit all six <TextBlock> elements alike, to specify their initial content, width, and margin on all four sides

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

**Text = ”...” Width = ”20” Margin = ”15”**

![image](images/5o.jpg)Edit the BtnPick **<Button>** element to specify its button label content, margin on all four sides, and initial state

**Content = “Get My Lucky Numbers” Margin = “15”**

**IsEnabled = “True”**

![image](images/6o.jpg)Edit the BtnReset <Button> element to specify its button label content, and initial state

**Content = “Reset” IsEnabled = “False”**

The order in which the attributes appear in each element is unimportant, but the elements within the **MainPage.xaml** file should now look similar to the screenshot below:

![image](images/pgc177_2.jpg)

![images](images/pgc177_1.jpg)

As you make changes to the **XAML** code, the component layout gets changed accordingly in the **Design** view, and should now look like this:

![image](images/pgc177_3.jpg)

![image](images/hot.jpg)

You can optionally add **Margin = “0”** attributes to explicitly require elements to have no margin width.

**Adding runtime function**

Having completed the application component layout with XAML elements [here](#chapter33.xhtml_sec265), you are now ready to add functionality with C# programming code:

![image](images/commonao.jpg)

Universal (continued)

![image](images/1o.jpg)In **Design** view, double-click on the BtnPick button

![image](images/2o.jpg)The **MainPage.xaml.cs** code-behind page opens in the **Code Editor** at a generated BtnPick_Click event-handler

![image](images/3o.jpg)In the BtnPick_Click event-handler block, insert these statements to create a randomized array of integers between 1 and 59

**Random rnd = new Random( ) ;**

**int [ ] seq = new int[ 59 ] ;**

**for ( int i = 1 ; i < 60 ; i++ ) seq[ i - 1 ] = i ;**

**for ( int i = 0 ; i < 59 ; i++ )**

**{**

**int j = ( rnd.Next( ) % 59 ) ;**

**int k = seq[ i ] ; seq[ i ] = seq[ j ] ; seq[ j ] = k ;**

**}**

**// Statements to be inserted here (Steps 4-5).**

![image](images/4o.jpg)Next, insert statements to assign six array element values to the <TextBlock> components

**textBlock1.Text = seq[ 1 ].ToString( ) ;**

**textBlock2.Text = seq[ 2 ].ToString( ) ;**

**textBlock3.Text = seq[ 3 ].ToString( ) ;**

**textBlock4.Text = seq[ 4 ].ToString( ) ;**

**textBlock5.Text = seq[ 5 ].ToString( ) ;**

**textBlock6.Text = seq[ 6 ].ToString( ) ;**

![image](images/5o.jpg)Next, insert statements to set the <Button> states

**BtnPick.IsEnabled = false ;**

**BtnReset.IsEnabled = true ;**

![image](images/6o.jpg)Return to **MainPage.xaml**, then in **Design** view, double-click on the BtnReset button

![image](images/7o.jpg)The **MainPage.xaml.cs** code-behind page opens in the **Code Editor** at a generated BtnReset_Click event-handler

![image](images/hot.jpg)

The randomizer routine uses exactly the same logic as that of the **Windows Forms Application** example – see [here](#chapter32.xhtml_sec258).

![image](images/forget.jpg)

There is no **Label** component in UWP apps; it is called a **TextBlock** instead.

![image](images/snake.jpg)

There is no **Enabled** property in UWP apps; it is called **IsEnabled** instead.

![image](images/8o.jpg)In the BtnReset_Click event-handler block, insert statements to assign strings to the <TextBlock> components

**textBlock1.Text = “...” ;**

**textBlock2.Text = “...” ;**

**textBlock3.Text = “...” ;**

**textBlock4.Text = “...” ;**

**textBlock5.Text = “...” ;**

**textBlock6.Text = “...” ;**

**// Statements to be inserted here (Step 9).**

![images](images/pgc179_1.jpg)

![image](images/9o.jpg)Finally, insert statements to set the <Button> states

**BtnPick.IsEnabled = true ;**

**BtnReset.IsEnabled = false ;**

The functions in the **MainPage.xaml.cs** code-behind page should now look like the screenshot below:

![image](images/pgc179_2.jpg)

![image](images/10o.jpg)Return to the **MainPage.xaml** file, then in **XAML** view, see that attributes have been automatically added to the <Button> elements to call the event-handler code

![image](images/pgc179_3.jpg)

![image](images/snake.jpg)

The **BtnReset** button simply returns the **<TextBox>** and **<Button>** components to their original states.

![image](images/hot.jpg)

Notice that the first **for** loop contains only one statement to be executed on each iteration, so braces are not required.

**Testing the program**

Having added functionality with C# code [here](#chapter33.xhtml_sec266), you are now ready to test the program for two devices:

![image](images/commono.jpg)

Universal (continued)

![image](images/1o.jpg)On the Visual Studio standard toolbar, select **Debug** for **x64** architecture and **Local Machine** options, then click the **Start** button to run the app with debugging enabled

![image](images/pgc180_1.jpg)

![image](images/2o.jpg)Wait while the application gets built and loaded, then click the buttons to try out their functionality

![image](images/pgc180_2.jpg)

![image](images/pgc180_3.jpg)

![image](images/pgc180_4.jpg)

The app looks good – numbers are being randomized and the button states are changing as required.

![image](images/3o.jpg)Now, on the Visual Studio standard toolbar, select **Debug**, **Stop Debugging** to exit the running program

![image](images/pgc180_5.jpg)

![image](images/forget.jpg)

You must have your PC set to **Developer Mode** in **Settings**, **Privacy & Security**, **For developers**.

![image](images/4o.jpg)Click the **Start** button to restart the app, then click the buttons and compare the sequences of randomized numbers to those generated in the previous test

![image](images/pgc181_2.jpg)

![image](images/pgc181_3.jpg)

![image](images/pgc181_4.jpg)

![images](images/pgc181_1.jpg)

Great – the random number generator is seeded with the current time to ensure a different sequence each time the app gets run.

![image](images/5o.jpg)Drag the window edge to reduce its width, to simulate how the app would look on a device with a narrower screen

![images](images/pgc181_5.jpg)

This is unsatisfactory – adjustments will be needed to the interface layout so it will adapt to suit narrower display areas.

![image](images/hot.jpg)

Test on the emulator with lowest memory and smallest screen, and it should be fine running on devices with better features.

**Adjusting the interface**

The app test for mobile devices [here](#chapter33.xhtml_sec267) failed to satisfactorily present the controls, as the interface is too wide for small screen devices. Happily, the interface can be made to adapt to different screen sizes so it can also look good on mobile devices. The adaptation relies upon recognizing the screen size and changing the orientation of a <StackPanel> element in **XAML** for narrow screen devices:

![image](images/commono.jpg)

Universal (continued)

![image](images/1o.jpg)Open **MainPage.xaml**, then in **XAML** view add these elements immediately below the opening <Grid> element and before the component elements

**<VisualStateManager.VisualStateGroups>**

**<VisualStateGroup>**

**<!-- Elements to be inserted here (Steps 2-3) -->**

**</VisualStateGroup>**

**</VisualStateManager.VisualStateGroups>**

![image](images/2o.jpg)Next, insert elements to recognize wide screens

**<VisualState x:Name = “wideState” >**

**<VisualState.StateTriggers>**

**<AdaptiveTrigger MinWindowWidth = “641” />**

**</VisualState.StateTriggers>**

**</VisualState>**

![image](images/3o.jpg)Now, insert elements to recognize narrow screens, and to change the **Orientation** of the outer <StackPanel>

**<VisualState x:Name = “narrowState” >**

**<VisualState.StateTriggers>**

**<AdaptiveTrigger MinWindowWidth = “0” />**

**</VisualState.StateTriggers>**

**<VisualState.Setters>**

**<Setter**

**Target = “MainStack.Orientation” Value = “Vertical” />**

**</VisualState.Setters>**

**</VisualState>**

![image](images/hot.jpg)

XAML code recognizes the same **<!-- -->** comment tags that are used in HTML code.

![image](images/forget.jpg)

Remember that the outer **<StackPanel>** in this app contains an **<Image>** and a nested **<StackPanel>** displayed horizontally, side by side. If displayed vertically, they should appear one above the other.

The beginning of the **MainPage.xaml** file should now look similar to the following screenshot:

![image](images/pgc183_2.jpg)

![image](images/pgc183_1.jpg)

![image](images/4o.jpg)Select **x64** and **Local Machine** to run the app once more – it still looks and functions well

![image](images/pgc183_3.jpg)

![image](images/5o.jpg)Now, drag the window edge to reduce its width, and see the interface adapt to suit a narrower screen

![image](images/pgc183_4.jpg)

![image](images/pgc183_5.jpg)

![image](images/pgc183_6.jpg)

![image](images/hot.jpg)

You can have Visual Studio nicely format the XAML code by pressing **Ctrl** + **K**, **Ctrl** + **D**.

![image](images/snake.jpg)

Although an app may work well on an emulator, it is recommended you always test on actual devices before deployment.

**Deploying the application**

Having tested the app [here](#chapter33.xhtml_img183), it can now be deployed onto your PC. This will register the app on your PC and add it to the **All apps** menu, so an icon image can usefully be added to the program files to identify the app:

![image](images/commonao.jpg)

Universal (continued)

![image](images/1o.jpg)Add a 400 x 400 pixel icon image into the project’s **Assets** folder on your PC

![image](images/2o.jpg)In **Solution Explorer**, right-click on the **Assets** folder and choose **Add, Existing Item** from the context menu and add the icon image

![image](images/3o.jpg)Next, double-click **Package.appxmanifest** and select the **Visual Assets tab** and the **All Visual Assets** item

![image](images/pgc184_1.jpg)

![image](images/4o.jpg)Add the icon image as the **Source** and click the **Generate** button to produce variously-sized tiles and logo images

![image](images/5o.jpg)Change the build type to **Release**, then click **Build**, **Deploy Solution** to register the app on your PC and see it get added to your PC’s **All apps** menu

![image](images/pgc184_2.jpg)

![image](images/pgc184_3.jpg)

![image](images/hot.jpg)

You can choose the **Remote Machine** option to test via a network connection.

An **App Package** can be created for deployment on other devices running Windows version 1809 or later:

![image](images/1o.jpg)Select **Release** on the toolbar

![image](images/pgc185_2.jpg)

![image](images/pgc185_1.jpg)

![image](images/2o.jpg)In **Solution Explorer**, right-click on the top-level **Universal** project folder, then choose **Publish, Create** **App Packages** from the context menu to launch a wizard

![image](images/3o.jpg)In the wizard, choose the **Sideloading** and **Enable** **automatic updates** options, then click **Next**

![image](images/4o.jpg)Select a package signing certificate, then click **Next**

![image](images/5o.jpg)Choose a destination (e.g. a USB drive), version numbering, and architecture – then click **Create**

![image](images/pgc185_3.jpg)

The build creates a folder of several items, including an Application Package file (.msixbundle) and a Security Certificate (.cer) file.

![image](images/6o.jpg)Move the folder to another device, then right-click on the Security Certificate file. Select **Install** then **Local Machine** and **Trusted People** to import the certificate

![image](images/7o.jpg)Finally, double-click the Application Package file to **Install** and **Launch** the app on that device

![images](images/pgc185_4.jpg)

![images](images/pgc185_5.jpg)

**Summary**

![image](images/pgc186_1.jpg)

•The **Universal Windows Platform** (UWP) enables a single app to run on any modern Windows-based device.

•The **Universal Windows App Development Tools** are needed in order to develop UWP apps.

•The **C# Blank App (Universal Windows)** template can be used to create a new UWP project.

•The **Developer Mode** setting must be enabled in the Windows options in order to develop and test UWP apps.

•The **eXtensible Application Markup Language** (XAML) is used to specify components and layout on UWP apps.

•Visual Studio provides a graphical **Design** view and a text code **XAML** view for the **MainPage.xaml** file.

•Component elements can be placed within XAML <StackPanel> elements to control how they are laid out.

•Image files can be added to the **Assets** folder and assigned to XAML <Image> elements for display on the interface.

•Space can be added around a component by adding a Margin attribute and assigned value within its element tag.

•Functional C# programming code can be added to the **MainPage.xaml.cs** code-behind page.

•A UWP app can be tested in **Debug** mode on the **Local** **Machine**, an **Emulator**, and a connected **Device**.

•The interface of a UWP app can adapt to different screen sizes by changing the orientation of <StackPanel> elements.

•Image files can be added to the **Assets** folder for assignment as logos in the **Package.appmanifest** window.

•The **Release** version can be deployed by selecting the target configuration, then using the **Build**, **Deploy Solution** menu.

[![image](images/ibc.jpg)](http://www.ineasysteps.com)

![image](images/bcover.jpg)