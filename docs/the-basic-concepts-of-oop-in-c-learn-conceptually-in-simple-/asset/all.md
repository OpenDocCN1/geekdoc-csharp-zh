![](Images/1405.jpg)

THE BASIC CONCEPTS OF OOP IN C#

LEARN CONCEPTUALLY IN SIMPLE LANGUAGE

![Image](Images/kisspng-microsoft-visual-studio-net-framework-visual-stud-5adab7033e9305.4830596915242831392563.jpeg)

University of applied science and technology

Hani Marzban

Copyright © 2018 by Hani Marzban

All rights reserved. No part of these publications may be reproduced, distributed, or transmitted in any form or by any means, including photocopying, recording, or other electronic or mechanical methods, without the prior written permission of the publisher, except in the case of brief quotations embodied in critical reviews and certain other noncommercial uses permitted by copyright law. For permission requests, write to the publisher, addressed “Attention: Permissions Coordinator,” at hani.mrzbn@gmail.com.

Table of Contents

*   [Preface](#index_split_000.html_id_Toc3384495)
*   [Introduction](#index_split_001.html_id_Toc3384496)
*   [The concept of an object](#index_split_001.html_id_Toc3384497)
*   [The Properties of an object](#index_split_001.html_id_Toc3384498)
*   [The Behaviors](#index_split_001.html_id_Toc3384499)
*   [The Methods](#index_split_001.html_id_Toc3384500)
*   [The fields](#index_split_001.html_id_Toc3384501)
*   [The Accessor](#index_split_001.html_id_Toc3384502)
*   [The Namespaces](#index_split_001.html_id_Toc3384503)
*   [The concept of a Class](#index_split_001.html_id_Toc3384504)
*   [The Concept of a struct](#index_split_001.html_id_Toc3384505)
*   [Differences between class and struct](#index_split_001.html_id_Toc3384506)
*   [The constructors](#index_split_001.html_id_Toc3384507)
*   [The destructors](#index_split_001.html_id_Toc3384508)
*   [The re-usability](#index_split_001.html_id_Toc3384509)
*   [The abstraction](#index_split_001.html_id_Toc3384510)
*   [The encapsulation](#index_split_001.html_id_Toc3384511)
*   [The Property](#index_split_001.html_id_Toc3384512)
*   [The Inheritance](#index_split_001.html_id_Toc3384513)
*   [The interface](#index_split_001.html_id_Toc3384514)
*   [The Polymorphism](#index_split_001.html_id_Toc3384515)
*   [Practical exercises](#index_split_002.html_id_Toc3384516)
*   [How to create a class](#index_split_003.html_id_Toc3384517)
*   [Declaration of a class in C#](#index_split_003.html_id_Toc3384518)
*   [Declaration of a method in C#](#index_split_003.html_id_Toc3384519)
*   [Calling Methods in C#](#index_split_003.html_id_Toc3384520)
*   [How to use constructors](#index_split_003.html_id_Toc3384521)
*   [How to use DEstructors](#index_split_003.html_id_Toc3384522)
*   [The Property and encapsulation](#index_split_003.html_id_Toc3384523)
*   [Struct](#index_split_003.html_id_Toc3384524)
*   [“Reference Type” and “Value type”](#index_split_003.html_id_Toc3384525)
*   [The inheritance](#index_split_003.html_id_Toc3384526)
*   [The constructors in inheritance](#index_split_003.html_id_Toc3384527)
*   [The abstraction](#index_split_003.html_id_Toc3384528)
*   [Static and non-static class](#index_split_003.html_id_Toc3384529)
*   [The interface](#index_split_003.html_id_Toc3384530)
*   [The polymorphism](#index_split_003.html_id_Toc3384531)

# Preface

Researching in various areas of computer science has been the author’s most favorite work to do from a long time ago. This time he has decided to write a book about the preliminary topics in the object-oriented programming paradigm in C# programming language, which is considered to be one of the most popular ones thanks to the powerful “**Dot NET framework**.”

This book helps interested audiences to get familiar with the basics of the object-oriented programming paradigm in C# faster, for he has written this book in the simplest possible language, used very simple examples; however, being a mid-level C#.Net developer is a prerequisite. Moreover, the author has **emboldened** and underlined important points too.

Hence, expected that readers find this book useful, although, study without practical practice is worth nothing in programming; therefore, remember that “practice is the key.”

Hopefully, to enjoy reading this book as much as the author enjoyed writing it, and please do not hesitate to send possible suggestions, corrections, and errors at **hani.mrzbn@gmail.com** because the author warmly considers it.

Ultimately, the author would like to present this book to the great soul of the late Professor Maryam Mirzakhani, the legendary Iranian mathematician, and the winner of the Field medal in 2014\. She  is a light in the way of doing scientific investigations, perseverance, and dignity for us.

Hani Marzban, January 19, 2019

# Introduction

Maybe readers have heard about “Object-Oriented,” or have heard that this could be the hardest-to-understand concept in  programming  especially if you are a newbie in this or having a plan to get into the community of coders? So, we assure that this is hard no more.

However, this could be true at the beginning of programming age, but fortunately it has become pretty much easier and understandable more than ever with the advent of HLL^([¹](#index_split_004.html_note_1 "1")) of programming such as C, C++, C#^([²](#index_split_005.html_note_2 "2")), Visual Basic, and etcetera., which helped programmers to comprehend the main concept of OOP^([³](#index_split_006.html_note_3 "3"))  paradigm  more,  like never before.

Well, there are benefits for the programmers using OOP paradigm, such as having a high-performance piece of codes, re-usability, which is considered to be a principle in OOP and literally as the foundation of OOP. Debugging codes are easy to do, so this way, the audience will not get involved with tons of complex lines of codes and also developing and modification of codes are easy to deal with, too.

Ultimately, in this book, we will have a closer look at the OOP paradigm in practice using C# language, and surely by relying on different examples, achieving a high level of ability in OOP paradigm will become true. Do not forget that “practice is the key.” We wish dear readers all the success in this.

# The concept of an object

Whatever we see, whatever we feel or even imagine in the real world is counted as an object. Usually, we work with different types of objects in the daily life, such as Computers, Mobile phones, Televisions, and etcetera. So, it is the same in the world of the computer. As an instance, OS^([⁴](#index_split_007.html_note_4 "4")) applications are called objects like, media players, toolbars, buttons, windows and what we could observe, these are the visible objects; on the other hand, there are hidden objects too, we cannot see, but they are working behind the scene, technically, a bunch of codes letting visible objects to run and be controlled. Each object as an entity contains two main factors, “**properties**” and “**behaviors**,” which I will describe them later. So, for now, let us clear the definition of an object using an example.

Firstly, before creating an object, we need to analyze the essential **properties** and **behaviors** of an object. Imagine we have a plan to build software for managing a library, so surely after analyzing the needs, for example, we find primary **objects** in which to implement as below.

1-Members of the library

2-Operators of the library

3-Category of book

4-Book

Great, so, the next step is recognizing related **properties** and **behaviors**; for instance, consider “**members of the library”** object, it contains **properties** as below.

1-Member ID

2-Name

3-Lastname

4-ID Number

5-Father’s name

6-Gender

Also, each “**member of the library”** has **behaviors,** which could be contemplated to be,

1-Get book

2-Return book

3-Log into the library

4-Exit the library

So, we are expecting audiences to extract the necessary properties and behaviors of the rest objects if they found how it works.

1-Operator of the library

2-Category of book

3-Book

Please try to examine other operational environments like a small shopping or a chain store. Do not rush to get on codes quickly, keep calm, based on my experience, first, you need to learn this perfectly; therefore, to achieve this important you must practice on paper as much as you could, and jot down essential properties and behaviors of objects related to different systems until becoming a master. Do not afraid to try on large systems as it is possible simply **by breaking down the components of enormous structures into small ones**; through this, helps to gain a good level of skill in designing an object.

# The Properties of an object

The “**properties of an object**” are bunches of characteristics concerned an object, which precisely, describe it. For example, consider a human as an object, there are tons of different characteristics for him/her such as eye color, height, weight and many other parameters describing a human, these are all called **properties of a human.**

# The Behaviors

Despite **properties**, there are a series of actions inside an object called “**Behaviors**”, let us clarify this quickly, if we consider a human as an object; hence, we can say “humans can walk, or humans can see”, these are called “**Behaviors**” an object (human) could do.

# The Methods

In fact, methods are the ways to employ function(s) of an object. Let us break down this using an example. Imagine, there is a mobile phone as an object, and there is a method inside this object (mobile phone) called “displaying numbers,” which shows pressed numbers on the display of your mobile phone. So, technically when we press “1” on your mobile phone's keypad, this button invokes “displaying numbers” method and sends “1” to that, and ultimately, the method will show “1” on display. If it is not crystal clear enough, do not worry, later, we will work practically to get it conceptually.

# The fields

A fieldis a normal variable, which can carry different types of data, and are contemplated to be members of a class. It has declared in a class, and to set or get any values to use “**set**” or “**get**” **accessor**.

# The Accessor

In simple language, “**set**” and “**get**” are properties, which let the programmer set or get value(s) to or from a field in a class. We will review it in **practical exercises** **section.**

# The Namespaces

A class can carry tons of members, and a namespace can carry a lot of classes inside. **Namespaces** are containing different pre-defined classes, which let programmers use for variant purposes. For example, in .NET framework^([⁵](#index_split_008.html_note_5 "5")), there is a namespace that contains necessary classes to connect to a database such as SQL, Oracle DB, and etcetera.

# The concept of a Class

Well, in fact, objects are nothing if we do not consider a class as a principle. Let us explain more clearly, a class plays a parent role here and encompasses everything from variables to properties, behaviors, methods, and etcetera. In other words, a class has made of a set of rules to achieve a unique goal, but to make it applicable; we have to create a copy of that, which is called “**Instantiation**”; by this, literally, you have **created an object from a class** that is usable in action.

# The Concept of a struct

The structure, and technically, the functionality of a struct is pretty much similar to a class, although s struct is more limited and could be contemplated to be a light version of a class. Well, in “**Practical exercises**” section, we will try a simple sample of the struct to find out the way it works, for practical example(s) it can help you get a better understanding too.

# Differences between class and struct

Within a struct declaration, fields cannot get initialized unless they get declared as const or static.

A struct cannot declare a default constructor (a constructor without parameters).

Structs get copied on assignment. When a struct has assigned to a new variable, all the data get copied, and any modification to the new copy does not change the data for the original copy. It is important to remember when working with collections of value types such as Dictionary.

A struct is “value type,” and a class is “reference type.”

Unlike classes, a struct gets instantiated without using “new” operator.

Structs can declare constructors, which have parameters.

A struct cannot inherit from another struct or class, and it cannot be the base of a class.

A struct can implement interfaces.

A struct can be used as a nullable type and can be assigned a null value.

# The constructors

Initializing data members of a new object is often the task of a constructor. When a class gets created, in fact, its constructor is called concurrently, too. Constructors have the same name as the class. There are different usages for constructors of which we prevent.

# The destructors

A destructor is the same in name with class and constructor, but there is a bold sign which distinguishes it from a constructor’s or a class’s name, and it is a “**~**” symbol that needs to get implemented as a prefix in the name of a destructor. So, what is the advantage of destructor? Well, it runs when the class runs and ends before the class ends; by this, **it cleans the finished class from memory, which results in managing memory**, although, this task is useful no more in programming languages equipped by garbage-collector^([⁶](#index_split_009.html_note_6 "6")), and also are not suitable to use in big projects too.

# The re-usability

One of the strong points in the OOP paradigm is, “**Re-usability.”** **It lets us use a single object “N” times to do “N” different tasks; instead of, using “N” different objects to do “N” different tasks,**  which results in **reducing the high volume of codes and increasing the execution speed of the codes dramatically**.

In the direction of a deeper comprehension regarding the subject, see the example below.

**Problem:** We need to print the names of 50 people from a database, which solution is preferred? Why?

A) Creating **fifty** different objects to receive the names from the database and print them out.B) Creating **one** object to receive the names from the database and print them out.

Definitely, the option “B” is the key answer, as **it helps reducing tons of repetitive codes, which leads to increasing the speed of execution; by which, the efficiency boosts like never before.**

# The abstraction

When you plan to write a program using OOP paradigm, firstly, you have to analyze a system thoroughly, it means you need to recognize all possible entities such as properties, behaviors, variables, and etcetera., take them into account, but sometimes to run a system working properly, all the suggested entities are not mandatory and we should prevent them.

For example, we are going to buy a car, and we need to arrange a contract between the seller and us, so, it is natural  to write our personal information in it, but surely writing our blood type or the size of our shoes is not a must. These are the properties of us too, in which are not compulsory to mention.

# The encapsulation

Let us begin with an example, we have a mobile phone in hand, and we do make a call using it. Do we know the process by which the mobile phone does to make a call? Absolutely, not. We, as a user of the mobile phone press a few simple buttons to make a call instantly, but surely we are ignorant of the functions that the mobile phone runs behind the scene to make a connection. It is what we named as “**Encapsulation,” to hide function’s complexities of an object from the view of users** in simple language. There is no reason that a user sees how it works but the final consequence.

# The Property

A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field. Propertiescould get used as if they are public data members. Property encapsulates a private field. It provides getters (get{}) to retrieve the value of the underlying field and setters (set{}) to set the value of the underlying field.

# The Inheritance

The inheritance, playing a major role in OOP paradigm. We should practice this technique  as much as possible, as if we do, could safely say that becoming a master in OOP is guaranteed. To perceive this concept better, let us say, from birth, children inherit attributes from their parents, such as eye color, hair color, skin color, special behaviors, and etcetera. It is precisely the same in OOP paradigm too, but how? When we design an entity, we could consider a class as the parent, which the entity could inherit everything from the parent class. Thereupon, re-usability will happen, and entities could inherit necessary attributes; instead of, writing tons of codes, which results in reducing the high volume of codes and actually, rising efficiency.

# The interface

It is similar to a class, but as you might be aware, unlike a class, which cannot inherit from two or more classes at the same time, it could be inherited multiple of times without limitation, so we will try a simple example in the “Practical Exercises” section, to find out how it works.

# The Polymorphism

Many of us complaining about the **polymorphism**, and we always advise them, “**Despite learning ‘Inheritance’ perfectly, relying on very basic samples to find the concept easily is highly recommended**.”

We are going to talk about the polymorphism, and we will try basic practices in the practical section. Imagine an office, in that office; there is a manager, a clerk, and a secretary and their office imports computer stuff. Well, There is a defined class for clerk, which there are different methods defined inside, such as “Log out”, “Log in”, “Payment”, and “Duty.” **So, please pay attention to the behavior of each method defined in the class of “clerk” in below.**

The behaviors of the clerk method,

**Log in: This method logs the time** **of entry to the office.**

**Log out: This method logs the time** **of departure from the office.**

Payment: This method logs a default monthly payment of $900

Duty: This method logs, if the clerk talked to exporters or not?

Okay, this method works like a charm for the clerk, but now, we need to define a class for the manager too. What we need to do is, inheriting a class from the “clerk” and do little changes, for behaviors of clerk and manager are not the same, exactly. **So, please pay attention to the behavior of each method defined in the class of “manager”, after inheritance, in the following.**

The behaviors of the “manager” method,

**Log in: This method logs the time** **of entry to the office.**

**Log out: This method logs the time** **of departure from the office.**

**Payment:** This method logs a default monthly payment of $3K.

**Duty:** This method logs, if the manager has signed letters or not?

Great, we hope it makes sense to readers. What did we do? It is easy, we have just created a new class by inheriting from the “**clerk**” class, called “**manager**”, and **since the required behaviors of both classes were not the same, exactly, we did commit modification in the “Payment” and “Duty” methods of the “manager” class.**

# Practical exercises

# How to create a class

Open the Visual studio software then click on **File**  **New**  **Project**  **Visual C#** **Console Application**, and after changing the name of the project and also the location (optional), click on “OK” button. (Fig 1)

![Image](Images/Untitled-2.png)

Fig 1

Fig 1

![Image](Images/Untitled-2-1.png)Great, we need to add a class to the project, find the project name in the solution explorer window and do a right click on it and follow, Add Class. (Fig 2)

Fig 2

Fig 2

Good, so a new window will be opened as seen in below, containing different items, but what we need, is “class” item, so firstly click on “**Visual C# Items**” then choose “**Class**.”

Finally, it is possible to change the name of the class too, and then click on “**Ok**” button to create it. (Fig 3)

![Image](Images/Untitled-2-2.png)Yes, we did it. We could add a class file to our project successfully. Since now, we can double-click on it to open the file and begin to create different classes.

Fig 3

Fig 3

# Declaration of a class in C#

*[Access modifier][“*class*” keyword][ClassName]*

On second thought, “**Access modifier**” you need to replace items, which mentioned below,

**public:** The type or member could become accessible by any other code in the same assembly or another assembly that references it.

**internal:** The type or member could become accessible by any code in the same assembly, but not from another assembly.

After *[Access modifier]*, you **have to** put the “**class**” keyword, and then a name for your class, please see the example below to see how it works. (Using **access modifiers** is an option).

**Note:** “**Internal” is the default if no access modifier is specified.**

public / internal class Customer

{

Codes go here…

}

So, try to create a class in C# to see the way it works; however, it makes a default class when we add a class file to our project, but rely on putting some classes to understand essential structure.

# Declaration of a method in C#

[Access modifier][Return type][Method Name]([Parameters])

Well, methods are defining inside a class, by this, firstly, we need to have a class. Imagine we have a class named “**math_operation**”, and I am going to create a method inside this class as “**sum**”. Before of everything, let us explain the elements of declaration line in below.

Instead of, “**Access modifier**” you can replace items, which mentioned below.

**public:** The type or member could become accessible by any other code in the same assembly or another assembly that references it.

**private:** The type or member could become accessible only by code in the same class or struct.

**protected:** The type or member could become accessible only by code in the same class, or in a class, which derived from that class.

**internal:** The type or member could become accessible by any code in the same assembly, but not from another assembly.

**protected internal:** The type or member could become accessible by any code in the assembly, which it is declared, or from a derived class in another assembly.

**private protected:** The type or member could become accessible only within its declaring assembly, by code in the same class or in a type that has derived from that class.

Rather “**return type,”** if the method returns any value, you have to write the data type, which method returns such as “**int**”, “**string**”, and etcetera. Else, the return type is **void**, and we need to apply “**void**” keyword.

Note: If we put “void” keyword as a substitute for “return type,” you will not need to write “return” keyword inside the body of the method, but if you use any data type in “return type” then you will need to employ the “return” keyword.

On behalf of, “**Method name,”** you need to set a **unique identifier** for your method rather than other identifiers’, remember, it is CaSe SeNsItIvE.

Instead of, “**Parameter list,”** which enclosed between two parentheses you can insert variables with different types as **inputs** and **outputs** of the method.

Okay, let us get back to the example, imagine we have a class called “**math_opration**”, which contains a method called “**sum**”, and the method uses two parameters to receive two numbers. Please consider the elements and the way it works. (Fig 4)

![Image](Images/5.png)

Fig 4

Fig 4

We could create a class and a method successfully to calculate the sum of the two numbers, but we need to employ it in an operational environment to find the way it works; hence, at first, we need to create an instance of the class, and then call the method.

# Calling Methods in C#

To employ methods, we need to call them. To achieve this important, at first, we should create an instance of the class, which carries the desired method(s). In this example, we create an instance from the “math_operation” class ![Image](Images/6.png)then we will invoke the intended method. Find out how to do that in the following. (Open the “Program.cs” then write the codes shown in below)

Fig 5

Fig 5

Good, after starting the project we will see an outcome like that illustrated in the following. (Fig 6)

![Image](Images/7.png)Congratulations, as we can see, it shows the number “30” as the final result, it means that the method works like a charm, but remember, this is not the whole story, and you need to practice basic  examples more and more to find out the way it works. Do not rush to go on big projects because we are a junior.

Fig 6

Fig 6

# How to use constructors

Well, as we mentioned, the constructors are methods, **which do not return any value**. For example, if we have a class named “**car**”, definitely there is a constructor for it too, called “**car**”. We noted that one of the main tasks of the constructors is initializing data members of a new object.

The general structure of a constructor at a glance.

{Access-modifier} {Class-name}([Parameters])

{

}

See a simple example to get the structure better.

Step 1: Put the below codes in a class file.

1- public class car2- {3- public string color;4- public int max_speed;5- public car ()6- {7- color = "Orange";8- max_speed = 200;9- }10- }

Step 2: Open the “Program.cs” file and put the below codes.

11- public class Program12- {13- static void Main(string[] args)14- {15- **car cr = new car();      **16- **Console.WriteLine(cr.max_speed);**17- **Console.WriteLine(cr.colour);**18- **Console.ReadKey();**19- }20- }

**Step 3: Run the program, and let the CLR**^([⁷](#index_split_010.html_note_7 "7")) **gives out the result.**

The first output is equal to “200”.

The second output is equal to “Orange”.

Okay, Let us trace the lines of codes to see what happened.

**#1:** Define a public class called “car”.

**#3:** Define a public field, inside the class to hold the color name of the car.

**#4:** Define a public field, inside the class to hold the maximum speed of the car.

**#5:** Define a constructor due to set the default values for the fields.

**#7:** Set the default value.

**#8:** Set the default value.

**#15:** Create an instance of the car class called “**cr**”.

**#16:** Show the value of the “color” field using the “**Console.WriteLine”** command line, in an MS-DOS console window.

**#17:** Show the value of the “max_speed” field using the **Console.WriteLine** command in an MS-DOS console window.

**#18:** Obtains the next character or function key pressed by the user. The pressed key is displayed in the MS-DOS console window. It could help us observe the outcome while keeping the window opened.

We may ask ourselves, why use constructors when we can set the default value(s) of fields while defining them? Well, it is a good question, let us see why? Even if we do not create a constructor to initialize the data members of a class or struct, the compiler will do this, initialize the data members, and invoke it by default after creating a class or struct. **Remember, we can define multiple constructors at the same time in a class or struct with input parameters,** **which enables us to set different values for each instance of a class**, for example, we can have five instances of a class with five different values. We could find more information about this in advanced topics of OOP in C#.

# How to use DEstructors

The destructors are methods, which help to clean up finished objects from memory. **However, garbage-collected languages do this easily, and destructors are useful no more**, but at least, knowing the functionality of destructors is useful.

See the example below to find out the way it works.

Step 1: Put the below codes in a class file.

1- class print_command2- {3- public print()4- {

5-       Console.WriteLine ("This is a constructor");

6- }7- ~print()8- {9- Console.WriteLine ("This is a destructor");10- }11- } // End of class

Step 2: Open the “Program.cs” file and put the below codes.

12- class Program13- {14- static void Main(string[] args)15- {16- **print_command prt = new print_command();**17- }18- }

Step 3: Run the program, and let the CLR gives out the result.

The output in the first line is equal to "This is a constructor".

The output in the second line is equal to "This is a destructor".

Well, let us trace the codes, line by line to find out what happened.

#1: Define a class called “print_command”.

**#3:** Define a constructor called “print”.

**#5:** Write a command line, which prints out “This is a constructor” in an MS-DOS console window to find out invoking of the constructor method.

**#7:** Define a destructor. **Remember, the name of destructor needs to be the same as the name of the class, and also a “~” character is needed to get placed before the name of the destructor.**

**#9:** Write a command line, which prints out “This is a destructor” in an MS-DOS console window. When we see the message, it means that the constructor is executed and finished.

#16: Open the “Program.cs” file, and  create an instance of the “print_command” class.

Ultimately, by running the program, we will invoke the constructor and destructor methods.

# The Property and encapsulation

Here we have a very simplified sample of **property**. At first, try to check the following example, trace the lines of codes, and strive to see if we could get it or not.

Step 1: Create a class called “Calculation”, and put the below codes, in order to create a property.

1- public class Calculation

2-      {

3-      private int result;

4-      public int Age

5-      {

6-      get { return result;}

7-      set { result = value; }

8-      }

9-      }

Step 2: Open the “Program.cs” file and put the below codes.

10-      public class Program

11-      {

12-      static void Main(string[] args)

13-      {

**14-      Calculation clc=new Calculation ();**

**15-      clc.Age=50;**

**16-      Console.WriteLine (clc.Age-7);**

**17-      Console.ReadKey();**

18-      }

19-      }

Step 3: Run the program, and let the CLR gives out the result.

The final output is equal to 43.

Okay, great. So, let us see what happened from the first step to the final step by analyzing lines of codes,

**#1**: We have defined a class called “**Calculation”** to put necessary blocks of codes inside, such as methods and fields.

**#3**: **Due to pursuing the encapsulation rule, we** have to  **define the method as private.** This way, the field will remain inaccessible from the attempts of the other users using the same class. So, thereupon, we could fulfill the concept of encapsulation which is important in real meaning.

**#4**: Time to define a property inside the class, called “Age”. Do not insert parenthesis “()” after the name of a property as it leads you to a syntax error. We need to place the **get** and the **set** methods in the property, for **these methods can set or get value(s) from the defined private field in line #3, and technically this is the only way to set or get values(s) from a field which is inaccessible, and is following encapsulation paradigm.**

**#6:** In simple language, this method **get value(s) from the private field** **and pass it to you, when you call it.**

**#7:** **This method sets a value to the private field, remember, the “value” next to the “=” sign is a must keyword to put a value(s) into a field correctly.**

Almost done, the other parts of the codes (**from #10**) are in the“**Program.cs**”.

**#14:** Here we need to create an instance of the defined class called “Calculation”. Well, I do this, and name the instanced class as “clc” (You could put your favored name), then we would have a usable copy of “Calculation” class called “clc”, as you might be aware, **a class can not be used on its own, and needs to get instanced in favor of becoming applicable.**

**#15: Sets the value “50” to the private field named “result” available in “Calculation” class. Well, in fact, it passes the value “50” to the property, and the “set” method in the property grab that value** using “value” keyword  **and simply put it inside the private field called “result”.**

**#16:** This line, reads the available value inside the private field in “Calculation” class. In simple language, this time the “get” method fetches the available value from the private field in “Calculation” class called “result”, and pass it to you, and then the received value will get subtracted by number 7\. Ultimately, this line of command **“Console.WriteLine”**, shows the outcome (fetched value minus by number 7) an MS-DOS console window.

**#17:** Obtains the next character or function key pressed by the user. The pressed key is displayed in the MS-DOS console window. In fact, it could help us observe the final consequence(s) while keeping the window opened.

# Struct

Let us see a basic instance of the struct in the following to find out the structure.

Step 1: Define a struct by putting the below codes in a class file.

1-struct information

2-{

3-public string name;

4-}

Step 2: Create an instance of the defined struct

Open the “Program.cs” file and using the below code, create an instance of the defined struct.

5- public class Program

6- {

7- static void Main(string[] args)

8-  {

**9-  information TheStruct**

**10- TheStruct.name=”Hani”;**

11-  }

12- }

Let us dig into codes line by line,

**#1:** Define a struct, using “struct” keyword you can do it.

**#3:** Define a string field in the struct (Remember, you cannot obtain a value for that field inside the struct, you can define it, this is a rule, which I noted in advance).

**#9:** Time to create an instance of the “information” struct. So, what we need to do is **writing the name of the struct at first**, then writing the name of the object.

**#10:** Well, now we can obtain a value to the field, which defined in the struct, from here.

# “Reference Type” and “Value type”

There is a **fundamental and markable discrepancy** **between class and struct**, which we noted in advance. We should be aware that the **class is “Reference Type”** and struct is “**Value Type**.” So what does it mean? Let us clear by an example in the following to get it more.

Please pay attention to this piece of the code; this is a sample of a class, which we need to guess the output.

1-ProgrammingClass student1=new ProgrammingClass ();

2-student1.score = 20;

3-ProgrammingClass student2 = student1;

4-student2.score = 19;

5-Console.WriteLine (student1.score.ToString ());

Yes, **the output is equal to “19”; instead of, “20”**, but why not **“20”**? The reason is to be the **reference type**, let us explore line by line to find out more.

**#1:** Creating an instance object named **“student1”** of a class called **“ProgrammingClass”**, which containing a field named **“score”.**

**#2:** Set the value of “**20**” in the score field.

**#3:** Creating another instance object named **“student2”** of the **“ProgrammingClass” and put it equals to “student1” the object. Please pay heed, by this**, **these two objects (student1 and student2) will** get linked **together, and their values** will not get copied **in one another; on the other hand, as an instance, if you change the value of the “score” field available in the “student2”, the value of the “score” field existing in the “student1” will get replaced by same as “student2”. It is the meaning of “Reference Type” in simple language.**

**#4:** Set the value of “**19**” in the score field existing in the **“student2”.**

**#5:** Show the value of the “score” field available in the “**student1**” using the **Console.WriteLine** command in an MS-DOS console window.

It was the concept of the “**Reference Type**.” Now let us have an example of the struct to understand the sense of the “**Value Type”** too.

1-ProgrammingStruct student1 ();

2-student1.score = 20;

3- ProgrammingStruct student2 = student1;

4-student2.score = 19;

5-Console.WriteLine (student1.score.ToString ());

**Unlike the class, this time, the output is equal to “20”**; **instead of,** **“19”**. Well, the reason is being a **value type**, let us see how it works line by line.

**#1:** Creating an instance object named **“student1”** of a struct called **“ProgrammingStruct”**, which containing a field named **“score”.** (**Remember, you do not need using “new” keyword while creating an instance object of a struct**).

**#2:** Set the value of “**20**” in the score field.

**#3:** Creating another instance object named **“student2”** of the **“ProgrammingStruct” and put it equals to “student1” the object. Please pay heed, by this**, **these two objects (student1 and student2) will** get linked **together, and their values** will not get copied **in one another; on the other hand, as an instance, if you change the value of the “score” field available in the “student2”, the value of the “score” field existing in the “student1” will get replaced by same as “student2”. It is the meaning of “Reference Type” in simple language.**

**#4:** Set the value of “**19**” in the score field existing in the **“student2”.**

**#5:** Show the value of the “score” field available in the “**student1**” using the **Console.WriteLine** command in an MS-DOS console window.

Moreover, this was the concept of the “**Value Type**” too.

# The inheritance

The word “Inheritance” in the OOP paradigm is the same meaning as in the real world. It is one of the most important, interesting, and applicable concepts in OOP paradigm. Firstly, let us have a closer look by relying on an example to figure it out. Imagine we got two different classes such as below,

**![Image](Images/Untitled.png)Step 1: Here we create the class “First”, and put two methods inside (One private and another one public), also we implement two fields (One private and another one public) too**.

Fig 7

Fig 7

![Image](Images/Untitled2.jpeg)Step 2: Creating a class called “second”, which inheritance members of the “First” class. Remember, now the “Second” the class is considered to be a derived class, and the “First” class is considered to be a base class. To do inheritance, we need to put a “:” character between the names of the classes, while creating the derived class, take a look at the end of Fig 7 to get it.

Fig 8

Fig 8

Good, now the “Second” the class has inherited everything from the “First” the class. To see the result of the made inheritance by the “Second” the class try to create an instance object of the “Second” the class in the “Program.cs”, and see what we got.

It seems we just got a method called “method1” and a field called “Name” (Fig 8), but what about the rest? Because we have a private field named “phoneNumber” and method, which is named “method2” too. Well, we must be aware that the  private members do not get inherit unless we change the “private” access modifier to the “protected” one, then you will be ![Image](Images/3.jpeg)able to access them in the derived class. (Fig 9)

Fig 9

Fig 9

Okay, after changing the access modifier of the “phoneNumber” field from “private” to “protected” (Fig 9), now we can access it in the derived class (“Second”); hence, as you see in (Fig 9), we have created a method called “access_test” having an input parameter, which passes the value to the “phoneNumber” field.

To employ it, we need to invoke it. Like always do this in the “Program.cs”.

See the (Fig 10) and try to trace what happened from the first.

![Image](Images/4.jpeg)That we cannot inherit of two or more classes at the same time, is a considerable point of which in inheritance topic, and we must be aware.

Fig 10

Fig 10

See the example below,

☓  class1:class2:class3:class4:class5:class6

☓  class1:class2, class3, class4, class5, class6

✓  class1:class2       1:1

In the following, we are going to write about constructors in inheritance topic and how to deal with it.

# The constructors in inheritance

There is a vague point here; it is constructors, so what about them? Could we inherit them too? Well, the answer is, “Yes,” but not normally. To make it crystal clear, let us refer to the following example.

Step 1: Create a class called “car1”, and put a private field named “modelName1” in, and a constructor with an input parameter, inside.

1-class car1

2-{

3-private string modelName1;

4-public car1 (string modelName1_param)

5-{

6-modelName1=modelName1_param;

7-}

8-}

Step 2: Create a class called “car2”, and put a private field named “modelName2” in, and a constructor with an input parameter, inside.

9- class car2:car1

10-{

11-private string modelName2;

12-public car2 (string modelName2_param):base(modelName2_param)

13-{

14-modelName2 ="BMW "+ modelName2_param;

15-Console.WriteLine(modelName2);

16-}

17-}

Step 3: Now open the “Program.cs and put the lines 22 and 23 in”.

18- class Program

19-{

20-static void Main(string[] args)

21-{

22-car2 cr = new car2("Z4");

23-**Console.ReadKey();**

24-}

25-}

The output is equal to "BMW Z4".

Okay, time to explore the codes line by line to get **how to deal with constructors in inheritance topic**.

**#1:** Create a class called “car1”.

**#3:** Define a private string field.

**#4:** Create a constructor with the input parameter.

**#6:** Set the value of the defined private string field to the input parameter of the constructor.

**#9:** Now, create the second class called “car2” and do inheritance from “car1” the class by putting the key character “:” in front of the “car2”, and writing the “car1” word.

#11: Please pay attention carefully, to employ constructors in inheritance, we have to create a constructor in the derived class exactly as the one exists in the base class (car1). So, at first, define a private string field.

**#12:** And now create a constructor with an input parameter in the derived class, then we **have to** put the ”**: base()”** key command in front of the constructor. Remember to fill in the parenthesis of **base** key command with the constructor’s input parameter name (“modelName2_param”).

Have to be the same

**public car2 (string** modelName2_param**)**:base(modelName2_param)

**#14:** Set the value of the defined private string field to a string as **“BMW”,** and the input parameter of the constructor.

**#15:** Show the value of the “modelName2” field using the “**Console.WriteLine”** command line, in an MS-DOS console window.

#22: Create an instance object of the “car2” the class (derived class), and pass the “Z4” to its constructor.

**#23:** Obtains the next character or function key pressed by the user. The pressed key is displayed in the MS-DOS console window. It could help us observe the outcome while keeping the window opened.

# The abstraction

Before, we have explained about the nature of abstraction class, but if we have to describe the **abstraction class in practice**, we would say it is a kind of class, which normally, cannot get instanced as an object, but **just could be used in inheritance**. Let us have a deeper focus on it by pursuing an example in the following to find how it works.

**Step 1: Here is the way to create an** abstract class**, we need to put the “abstract” keyword before the “class” keyword.**

abstract class A
{

public string book_name;

public abstract void Go_to();

public void author()

{

Console.WriteLine("I am a GEEK");

}

}

**Step 2**: **As we could see in the above,** **an abstract class** could accept fields, normal methods, and abstract methods too**. Remember, the available abstract method(s) in the class base (A), like the “Go_to()”; in order to, use in derived class (B), need to be** re-created **in the derived class (B)** using the “override” keyword **because unlike the normal methods, you are not allowed to use “{“ and “}” characters to create an abstract method in the base class (A) (**Compare the author() and the Go_to() methods available in class A to detect the differences**). See the example in the following to understand this concept better. Do not forget to practice practically to become familiar with it thoroughly.**

class B:A

{

public override void Go_to()

{

Console.WriteLine("This is a test by Hani"); }}

Step 3: Now, open the “Program.cs” and put the codes in below to see the result.

class Program

{

static void Main(string[] args)

{

B derived = new B();

derived.Go_to();

derived.author();

**Console.ReadKey();**

}

}

The first output is equal to “This is a test by Hani”.

The second output is equal to “I am a GEEK”.

# Static and non-static class

Shortly, the **non-static** classes are the ones that to employ them of which we must create an instance, and unlike it, to use static ones of which we do not need to create an instance. Till now, we have used non-static classes, so now, we intend to have static classes too; hence, let us have an example in the following to get cleared.

A sample of a non-static class,

Step 1: Create a class, place three fields and a method inside.

class nonStatic_sample

{

public int num1;

public int num2;

public int result;

public int sum()

{

num1 = 10;

num2 = 20;

result = num1 + num2;

return result; }}

Step 2: Open the “Program.cs” file, create an instance object of the “nonStatic_sample” class, then employ “sum” method.

nonStatic_sample ns = new nonStatic_sample();

Console.WriteLine(ns.sum());

Console.ReadLine();

As we had non-static classes, we know how to deal with them, but it is necessary to know the functionality of static ones too.

A sample of a static class,

**Step 1: Create a** static **class, place three** static fields **and a** static method **inside.**

class Static_sample

{

public static int num1;

public static int num2;

public static int result;

public static int sum()

{

num1 = 10;

num2 = 20;

result = num1 + num2;

return result; }}

**Step 2: Open the “Program.cs” file, then write the name of the class (**Static_sample**) directly, as it is a static class, of which we do not need to create an instance object. See the below codes to get it.**

int result;

result = Static_sample.sum();

Console.WriteLine(result.ToString());

Console.ReadLine();

As we could see; instead of, creating an instance object, we wrote its name and then called the “sum()” method from its inside. **Remember, we could prevent putting the “static” keyword before of the “class” keyword and still could have static and non-static members inside, although, employing non-static members in static methods are not allowed. See the example in below.**

class Static_sample Prevented to use the “static” keyword

{

public static int num1; Allowed to be used in the sum method

public int num2; Not allowed to be used in the sum method

public static int sum()

{

//Only static members are allowed here.

} }

**Note: Do not forget, if we use the “static” keyword before the “class” keyword, the members of the class** have to **be static too.**

# The interface

As we said, its structure is like the class, which let a class to inheritance multiple times from, while a class cannot inherit from two or more classes simultaneously; thereupon, we could consider this as an advantage of the Interface class. So, let us see an example in the following to understand the difference better.

We go ahead with a throwback to an example of the inheritance topic to see how it works. Well, imagine we got three different classes as below,

class A

{

}

class B

{

}

class C

{

}

Now the class C would inherit from the class B, but how? It is easy, act like the below,

class C:B

{

}

Good, but we need to inheritance from the class A concurrently too, how could we do that? Is it possible? **Definitely, true. But not normally**, for we need to use the **interface class** to gain this important. In the following, we will have normal and interface classes.

Please attention to the following example; it contains normal classes and interface classes,

Note: To create an interface class we need to apply the “interface” keyword; instead of, the “class” one.

class A

{

}

interface A1

{

}

interface B1

{

}

class B

{

}

class C:B,A1,B1

{

}

As we could see above, **unlike always, this time, the** **class C** **could inherit** **from two interface classes, also, a normal class at the same time. There is an important point here, which in inheritance, the normal class has to get defined at first, then interface class(es), else you may get an error. See the below example to get it.**

☓  class C:A1,B,B1 ☓  class C:A1,B1,B ✓  class C:B,A1,B1

How to invoke it? Well, it is a little bit different rather than invoking normal classes, using an example, we could understand this better.

Step 1: Create a class file then put the following classes.

1-interface A1

2-{

3-string show_name();

4-}

5-class B:A1

6-{

7-public string show_name()

8-{

9-return "Hani";

10-}

11-}

Step 2: Open the “Program.cs” file and put the following codes.

12-class Program

13-{

14- static void Main(string[] args)

15-{

16-A1 name = new B();

17-Console.WriteLine(name.show_name());

18-Console.ReadKey();

19-}

20-}

Time to dig the lines one by one to find out the codes,

**#1:** The way to define an interface. Using the **“interface”** keyword; instead of, the “**class**” one. Be aware that the “interface class” is contemplated to be “public” all the time.

#3: Create a string method called “show_name”, but without body braces, for it is not allowed to put on body braces in an interface unless doing that in the derived class.

**#5:** Create a normal class called “**B**” and getting derived from the **interface A1** the class.

**#7:** Exactly, we have to create the method, which we have created in the interface class (**line #3**), but this time you are **allowed to use body braces** to have a class in real meaning.

**#9:** The “**return**” command returns a string (“**Hani**”) as the output of the method. It is **mandatory**, for the type of the method **is not void**.

**#16: Well, as a matter of fact, this is a little bit different. This is the way of creating an instance in this situation. Firstly, write the name of the base class (A1 interface class), then put the name of the derived class at the end.**

**#17:** Show the returned value of the “**show_name**” method using the “**Console.WriteLine”** command line, in an MS-DOS console window.

**#18:** Obtains the next character or function key pressed by the user. The pressed key is displayed in the MS-DOS console window.

# The polymorphism

This topic is considered to be the most complex part in OOP, but not really as we believe no problem or concept is hard-to-understand with step by step practices. Well, let us get back to polymorphism topic, have a short definition of; also, very basic examples, and so on. There are two types of polymorphism, which are called static binding and dynamic binding, but what do these terms mean? Let us see.

**Static binding:** In fact, it is called “**overloading**” too. This situation allows us having **multiple the same-name methods** in a class with **different input parameters in type**. Let us look at an example to find out the concept better.

Step 1: Put the below codes in a class file.

1- class calculation2- {3- public int sum(int N1, int N2)4- {

5-return N1 + N1;

6-}

7-public float sum(int N1, float N2)

8-{

9-return N1 + N2;

10-}

11-public double sum(int N1, double N2)

12-{

13-return N1 + N2;

14-}

15-}

Step 2: Open the “Program.cs” file and put the following codes in.

16- calculation calc = new calculation();

17- Console.WriteLine(calc.sum(4, 0.5));

18- Console.ReadKey();

The output is equal to 4.5.

Well, let us explore the lines to find out the way it works.

**#1:** Create a class called calculation.

**#3:** Create a method called “**sum**” as “**int”**, **which comes with** two input parameters as “int**”.**

**#5:** Returns the sum of the two “int” input parameters.

#7:  Create the second method called “sum” as “float”, which comes with two input parameters as “int” and as “float”.

**#9:** Returns the sum of the two “**int**” and “**float**” input parameters.

**#11:** Create the third method called “**sum**” as “**double”**, **which comes with** two input parameters as “int” and as “double”.

**#13:** Returns the sum of the two “**int**” and “**double**” input parameters.

**#16:** Create an instance from the “calculation” class. Well, now we have access to each three of the same-name methods, but for example, how to use the third method, which uses “int” and “double” input parameters? It is easy, call the method, and put the appropriate input type and amount to work. See the line #17**.**

**#17:** Show the returned value from the **third “sum” method** using the “**Console.WriteLine”** command line, in an MS-DOS console window.

Why the third one? Moreover, why not the first one? Because we passed these amounts “5”, which is an integer, and “0.5”, which is **double**, so technically, spontaneously it will use the third one that benefits from “**integer**” and “**double**” input types.

**#18:** Obtains the next character or function key pressed by the user. The pressed key is displayed in the MS-DOS console window. In fact, it could help us observe the final consequence(s) while keeping the window opened.

**Dynamic binding (Runtime Polymorphism):** Let us begin with an example.

Step 1: Put the below codes in a class file.

1-class A

2-{

3- public virtual void Method_A()

4- {

5- Console.WriteLine("I AM IN CLASS A");

6- }

7-}

8- class B: A

9-{

10- public override void Method_A()

11- {

12- Console.WriteLine("I AM DERIVED FROM B");

13- }

14- }

Step 2: Open the “Program.cs” file and put the following codes in.

15- A inst = new A();

16- inst = new B();

17- inst.Method_A();

18- Console.ReadKey();

The output is equal to “I AM DERIVED FROM B”.

Time to see what happened really?

**#1:** Create a class called **“A”**

**#3:** Create a method called “**Method_A**”, but something is new here. It is the “**virtual**” keyword. If we create a method in a normal class and going to override it, we need to use “**virtual**” keyword.

**#5:** Show the “I AM IN CLASS A” string in an MS-DOS console window using the “**Console.WriteLine”** command line.

**#8:** Create a normal class called “**B**” and getting derived from the class A.

**#10:** Now we **override** the created method in “**class A”** (**line #3**).

**#12:** Show the “I AM DERIVED FROM B” string in an MS-DOS console window using the “**Console.WriteLine”** command line.

**#15:** Now time to invoke the overridden method, here we create an instance called “**inst**” from the base class (**A**).

**#16:** Put the created instance equal to the derived class (**B**).

**#17:** Now, we can invoke the overridden method.

**#18:** Obtains the next character or function key pressed by the user. The pressed key is displayed in the MS-DOS console window. In fact, it could help us observe the final consequence(s) while keeping the window opened.

# References

Visual C# full training- Sayyed Mohammad Hashemiyan 2005

dazhyarco.net - C# training courses

docs.microsoft.com - OOP in C#

tahlildadeh.com - C# training courses

barnamenevisan.org - C# training courses

# Anmerkungen

[[←1](#index_split_001.html_back_note_1 "1")]

High-level language

[[←2](#index_split_001.html_back_note_2 "2")]

C Sharp

[[←3](#index_split_001.html_back_note_3 "3")]

Object-oriented programming

[[←4](#index_split_001.html_back_note_4 "4")]

Operating system

[[←5](#index_split_001.html_back_note_5 "5")]

.  NET Framework is a software framework developed by Microsoft that runs primarily on Microsoft Windows. It includes a large class library named Framework Class Library and provides language interoperability across several programming languages.

[[←6](#index_split_001.html_back_note_6 "6")]

A program that automatically removes unwanted data held temporarily in memory during processing

[[←7](#index_split_003.html_back_note_7 "7")]

Common Language Runtime