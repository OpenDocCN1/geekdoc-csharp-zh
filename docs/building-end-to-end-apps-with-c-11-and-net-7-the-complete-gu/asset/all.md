![](images/cover.jpg)

![Cover](images/cover.jpg)

Copyright © 2024 BPB Online

*All rights reserved.* No part of this book may be reproduced, stored in a retrieval system, or transmitted in any form or by any means, without the prior written permission of the publisher, except in the case of brief quotations embedded in critical articles or reviews.

Every effort has been made in the preparation of this book to ensure the accuracy of the information presented. However, the information contained in this book is sold without warranty, either express or implied. Neither the author, nor BPB Online or its dealers and distributors, will be held liable for any damages caused or alleged to have been caused directly or indirectly by this book.

BPB Online has endeavored to provide trademark information about all of the companies and products mentioned in this book by the appropriate use of capitals. However, BPB Online cannot guarantee the accuracy of this information.

First published: 2024

Published by BPB Online

WeWork

119 Marylebone Road

London NW1 5PU

**UK | UAE | INDIA | SINGAPORE**

ISBN 978-93-55516-374

[www.bpbonline.com](https://www.bpbonline.com)

**Dedicated to**

In loving memory of my father, your dedication, tireless work ethic and simple lifestyle continue to inspire me every day. Your life was a shining example of determination and passion, setting a standard that I strive to live up to. Like any devoted parent, you yearned for nothing more than to see your children excel, and you spared no effort to make that dream a reality. Though you are no longer with us, your legacy of love and ambition lives on in everything that I do.

# Foreword

C# has been my true passion for over a decade, shaping my professional path. I've immersed myself in the .NET developer community, sharing insights worldwide on C#-centered app development strategies. From active GitHub contributions to collaborating with top engineers, I have championed feature adoption and innovation. My experience as a Solutions Architect overseeing design decisions for twenty teams resulted in an astonishing 20x speed boost in just 30 days. I am honored to hold titles like Google Developer Expert, two-time Microsoft Valuable Professional (MVP), Twilio Champion, and author of "Learning Blazor: Build Single-Page Apps with WebAssembly and C#" with O’Reilly Media. Co-hosting "On .NET Live" has also been an incredible journey, and I'm deeply grateful for these enriching experiences that celebrate diversified thoughts from amazing people around the .NET community.

App development in C# encompasses a wide array of possibilities, resonating uniquely with each developer. This language serves as a versatile paintbrush, enabling you to craft and collaborate with fellow enthusiasts in the ever-evolving realm of modern software development. What masterpiece will you bring to life, how brilliant will it shine, and whose world will it enhance? Within the pages of this book, you'll delve into the realm of C# development, exploring its real-world applications and the captivating stories it can tell. It is my firm belief that C# developers possess the ability to create truly exquisite and meaningful digital experiences.

C# has continually evolved with each new iteration of .NET over the years. As developers, we’re confronted with the pivotal task of discerning which features to incorporate into our projects and, crucially, why we should do so. This decision-making process necessitates a deep understanding of the trade-offs involved—whether a feature enhances readability, boosts performance, or simplifies complexity. Notably, not all features will tick all these boxes, and that's perfectly acceptable. However, it remains invaluable to grasp the array of available features.

Certain features wield the power to profoundly influence how we craft our code. From libraries and services to frameworks and core functionalities, they can usher in significant shifts. This underscores the importance of cultivating robust development environments anchored by dependable codebases. Our reliance on cutting-edge tools, including world-class integrated development environments, enriched by AI-powered statement completions and language servers, fuels our productivity and ensures we stay at the forefront of innovation. In this book, you'll explore these evolving features, understand their implications, and navigate the dynamic landscape of C# development.

In this book, you'll explore an extensive array of app development scenarios catering to diverse client needs. We begin by thoroughly covering the features of C# 11, progressing into web app development with ASP.NET Core Web app and Web APIs. The journey continues with gRPC Services, the innovation of Blazor WebAssembly, and a nod to TypeScript and SPA development with Angular. We also delve into desktop applications using WPF, WinUI 3, and .NET MAUI. Just when it seems like we've covered it all, we introduce you to ML.NET for machine learning app development. This book is a comprehensive resource that helps you pinpoint which features align with your goals. I'm confident that you'll find tremendous value in this read, and I want to extend my gratitude to Arun for creating this exceptional book.

- David Pine

(Microsoft, Senior Content Developer)

# About the Author

Arun Gupta brings over twenty-five years of valuable experience in software development. He has worked in diverse roles across medium and large organizations in services and product development industry of the likes of erstwhile CMC Limited, Patni Computers and Kronos Solutions. These days, besides technical consulting, he enjoys sharing his expertise by mentoring and helping individuals become better programmers and testers.

# About the Reviewer

Marco Siccardi is a .NET developer with more than 10 years of experience, currently working primarily with Xamarin and .NET MAUI on iOS in his day job for a big Swiss transportation company. He has also worked with server, desktop, web and cloud technologies in the past, completing his expertise.

His side projects have a wide range from mobile apps to cloud based applications and open source libraries, utilising everything the .NET world has to offer (including Azure, ASP.NET, MS SQL). In all projects, Marco is trying to get the cleanest architecture, using established patterns like MVVM, the repository pattern and others.

Recently, he started to explore the Swift programming language to evolve his native knowledge of the Apple ecosystem.

Besides that, he shares his knowledge through his personal blog, is an active runner and loves to take snaps with his iPhone. He is father of two young adults and husband to a patient and understanding wife.

# Acknowledgement

I would like to express my deep gratitude to several individuals whose unwavering support and contributions have played a pivotal role in bringing this book to fruition.

I extend my heartfelt thanks to my wife, Deepika, and my sons, Dhruv and Anmol, your patience, love, and the steadfast belief in my endeavors have been my guiding light. Even during the several missed family occasions and countless stern noes, your understanding and encouragement have kept my spirits high and my determination unshakable.

To my family, friends and colleagues, your encouragement and well-wishes provided the invisible force that propelled me to the finish line. Your belief in me has been a constant source of inspiration.

Special thanks to Marco for his meticulous technical review and invaluable comments, which improved the technical aspects of the content.

Specifically, for the ML.NET chapter, I would like to extend my heartfelt appreciation to my former colleague, Ajay Sharma, a distinguished authority in this domain. Ajay graciously steered me in the right direction on more than one occasion, for which I am grateful.

I am also grateful to the dedicated BPB staff for their professionalism and the process framework of seamlessly transforming individuals from the industry into first-time authors.

To each of you, your collective contributions have been indispensable in making this book a reality, and for that, I am deeply thankful.

# Preface

Welcome to the world of C# programming, where learning is an immersive journey, and knowledge is acquired by doing. This book is not a conventional manual; instead, it is a collection of notes born from the essence of a computer lab experience. As you delve into these pages, you embark on a journey that sets a learning tone reminiscent of a technical blog, where we tackle real-world problems step-by-step, unravelling the intricacies of C# 11 and .NET 7 along the way.

The approach is unique. Instead of diving deep into a single topic, we take a panoramic view, exploring various aspects necessary to build end-to-end applications. Think of it as going breadthwise around a topic, appreciating its nuances, before diving deep. This approach does not negate the value of depth, but it lays a solid foundation by starting from the concrete and progressing towards the abstract rather than the other way around.

This book is not a primer, it assumes you already possess a basic understanding of C# and Visual Studio. However, it serves as a steppingstone for those looking to graduate to the new language features, application types, and ways of working within the Visual Studio IDE.

The vast sea of information scattered across the internet and Microsoft's website can be overwhelming. This book serves as a beacon, synthesizing information from multiple sources into a coherent picture in the context of solving a specific problem. It presents this wealth of knowledge as a concise summary, guiding you towards further exploration through credible resources.

Each chapter in this book is bound together by the project templates found in Visual Studio. We leverage these templates to build a variety of applications, progressing step by step. Throughout these pages, we reinforce key concepts by creating engaging projects centered around interesting topics such as a Digital Bookstore, game of Cows and Bulls, Sudoku, an Image Navigator, and more. We begin with the big picture followed by taking the step-by-step journey into thinking about solving the problem. Once you have mastered the projects detailed within these pages, you will be equipped to apply the same principles to your own projects. The aim is the proverbial "teach you how to fish" – get you started and bring you up to a level where you can find the answers yourself.

In today's world, books are just one of the many resources at our disposal to get information and build knowledge. I commend your determination to excel in this field and implore you not to let your initial enthusiasm wane. I encourage you to fully engage with the text, diligently work through all the examples, ponder over the exercises, and explore the references. This way, by the end you will not only have a deeper understanding of these technologies but also a newfound inquisitiveness to delve further into the subject matter.

So, dear reader, as you embark on this educational journey, remember that this book is your key to unlocking the world of C# programming. Approach it with curiosity, embrace the "learning by doing" philosophy, and let it be your guide to mastering C#, .NET, and Visual Studio, one step at a time. I invite you to explore, experiment, and excel in this exciting field, and may this book be your trusted companion on your path to success.

The chapter-wise details are as follows

[Chapter 1: New Features in C# 11](#ch01.xhtml) - .NET version 6 released in Nov 2021 along with C# 10 since then there have been several advancements both in .NET platform and the C# language. This chapter describes the new features that have made their way in C# language. Also included are the code snippets demonstrating the working and the use of the new features.

[Chapter 2: ASP.NET Core Web App](#ch02.xhtml) - gives an overview of the different web applications that can be created in .NET 7 and then goes on to explain with the example of creating a Digital Book Store, Razor Pages web application end-to-end. Unit testing is demonstrated for the Book Details page and Selenium based functional test is written for the Book Index page.

[Chapter 3: ASP.NET Core Web API](#ch03.xhtml) - focuses on developing Web APIs using ASP.NET Core. It explains the various concepts around API development along with creating a simple Create Read Update and Delete (CRUD) Web API around the Digital Book Store.

[Chapter 4: gRPC Service](#ch04.xhtml) - introduces the ASP.NET Core gRPC services as a logical extension of WCF services and compares it to the other options of building services. It illustrates the concepts around gRPC services by creating one which will download a large file on the client through service method call using server streaming. MSTest based unit-test is written for the Employees Data Service.

[Chapter 5: Blazor WebAssembly](#ch05.xhtml) - introduces the different Blazor applications, describes the concepts around them and goes on to create a simulation for the game of Cows and Bulls using Blazor WebAssembly App project template, to highlight the intricacies of the development process. Unit-testing is demonstrated for the Razor components using the bUnit – a community driven project. For end-to-end testing scenario the use of Playwright .NET is described.

[Chapter 6: SPA with Angular](#ch06.xhtml) - develops a rich single-page application with Angular on the client side supported by ASP.NET core on the server side. The chapter explains the interplay of different technologies in various tiers followed by creating the Angular version of the Digital Book Store application starting with the ASP.NET Core with Angular project template.

[Chapter 7: WPF Application](#ch07.xhtml) - we begin exploration of the Microsoft’s desktop applications starting with Windows Presentation Foundation (WPF). We will understand the different types of Desktop Applications that can be created and where WPF fits in the overall strategy. To understand the controls and layout, we will create a simple custom pizza order form followed by building a real world WPF application around the popular game of Sudoku. Here, to further re-enforce the concepts in building a WPF application we will make use of User Controls to design the UI, implement Model-View-ViewModel (MVVM) pattern, make use of resource dictionaries, and finally publish the application. Unit-testing of the MVVM application is demonstrated by adding MSTest based test for the View-Model.

[Chapter 8: WinUI 3](#ch08.xhtml) - begins by describing the evolution of creating applications for the Windows platform and then goes on to elaborate on developing native Windows applications for Windows 10 and Windows 11 using Windows UI Library (WinUI) 3\. To understand the concepts around building a real-world WinUI application we will create an Image Navigator application.

[Chapter 9: .NET MAUI](#ch09.xhtml) - describes the evolving landscape for mobile application development with .NET followed by an overview of developing cross-platform apps using the .NET MAUI application templates. We will examine the differences in the .NET MAUI App template and the .NET MAUI Blazor Hybrid App template. This will be followed by migrating the Sudoku application that we created using WPF into a .NET MAUI application, to further elaborate the concepts around .NET MAUI.

[Chapter 10: ML.NET](#ch10.xhtml) - gives an overview of building machine learning model in .NET using the ML.NET library. The chapter begins by explaining the overall machine learning process and goes on to illustrate the concepts by creating a program that uses binary classification algorithm to perform sentiment analysis. Another example uses the graphical Visual Studio extension Model Builder, to solve machine learning problems related to regression analysis. This is followed by working end-to-end on an anomaly detection problem with a reasonably large financial dataset including data preparation and model training followed by evaluation and prediction using the model.

# Disclaimer
(Running examples on Mac)

We would like to bring to your attention that the programs developed in this book, along with the related code bundle, have been meticulously crafted using Visual Studio 2022 on a Windows 10 machine. While we have made every effort to ensure compatibility with other environments, it is essential to acknowledge that variances may arise when attempting to execute these programs on a Mac machine.

Our technical reviews have revealed that these differences can encompass a range of aspects, from variations in menu options to the absence of certain features. In such instances, we kindly urge our readers to embrace experimentation while keeping the end-goal in mind. We firmly believe that with some trial and error, you can still derive significant value from the topics discussed in this book.

For further information regarding Visual Studio on Mac and its capabilities, you may refer to the official documentation at [https://visualstudio.microsoft.com/vs/mac/](https://visualstudio.microsoft.com/vs/mac/). Just to add, Microsoft is encouraging the use of Visual Studio Code for development on Mac as outlined at [https://learn.microsoft.com/en-us/visualstudio/mac/what-happened-to-vs-for-mac](https://learn.microsoft.com/en-us/visualstudio/mac/what-happened-to-vs-for-mac).

Furthermore, it is crucial to note that the chapters pertaining to desktop development using WPF and WinUI are exclusively supported on Windows platforms.

We greatly appreciate your understanding and patience as you navigate through the diverse technical landscape, and we remain committed to assisting you in your journey of learning and exploration.

# Code Bundle and the Coloured Images

Please follow the link to download the

***Code Bundle*** and the ***Coloured Images*** of the book:

[https://rebrand.ly/61b4r71](https://rebrand.ly/61b4r71)

The code bundle for the book is also hosted on GitHub at [https://github.com/bpbpublications/Building-End-to-End-Apps-with-CSharp11-and-.NET7](https://github.com/bpbpublications/Building-End-to-End-Apps-with-CSharp11-and-.NET7). In case there’s an update to the code, it will be updated on the existing GitHub repository.

We have code bundles from our rich catalogue of books and videos available at [**https://github.com/bpbpublications**](https://github.com/bpbpublications). Check them out!

Errata

We take immense pride in our work at BPB Publications and follow best practices to ensure the accuracy of our content to provide with an indulging reading experience to our subscribers. Our readers are our mirrors, and we use their inputs to reflect and improve upon human errors, if any, that may have occurred during the publishing processes involved. To let us maintain the quality and help us reach out to any readers who might be having difficulties due to any unforeseen errors, please write to us at :

**[errata@bpbonline.com](mailto:errata@bpbonline.com)**

Your support, suggestions and feedbacks are highly appreciated by the BPB Publications’ Family.

**Join our book’s Discord space**

Join the book’s Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 1New Features in C# 11](#contents.xhtml_ch01a)

[Introduction](#contents.xhtml_sc2_1a)

The previous version of .NET, version 6, was released in Nov 2021 along with C# 10\. Since then, there have been a number of advancements both in the .NET platform and the C# language. These advancements include performance improvements and newer constructs. This chapter explains the latest additions to C# 11, including the new features introduced through updated .NET platform APIs and language improvements within the C# language itself.

The chapter describes the major changes along with code snippets that make use of the new features. The examples are part of the companion source code bundle and can be referred to from there. Not every new enhancement is described here, and readers are encouraged to explore further from the websites given in the reference section at the end of the chapter. The exercise at the end gives the reader an opportunity to apply the newly learned concepts. The solutions to the exercise are also part of the source code bundle.

As we prepare to go to print, it is worth noting that the forthcoming releases of .NET and C# are imminent. Readers are encouraged to access further information regarding these upcoming versions through the provided references.

[Structure](#contents.xhtml_sc2_2a)

The chapter describes the following new features:

*   Auto-default struct
*   Extended nameof scope
*   File-scoped types
*   Generic attributes
*   Generic math
*   List patterns
*   Microsecond and Nanosecond (.NET 7)
*   Newlines in string interpolation expressions
*   Pattern match Span <char> on a constant string
*   Raw string literals
*   Regex source generation (.NET 7)
*   Required members
*   Simplified ordering with System.LINQ (.NET 7)
*   Stream reading - ReadExactly and ReadAtLeast (.NET 7)
*   Tar APIs (.NET 7)
*   Type converters - DateOnly, TimeOnly, Int128, UInt128, and Half (.NET 7)
*   UTF-8 string literals
*   Warning wave 7

[Objectives](#contents.xhtml_sc2_3a)

By the end of this chapter, the readers will be able to develop an understanding of the new features of C# 11 and the common scenarios where these new concepts can be applied. Some references to find more information on the topic has also been provided at the end of the chapter.

Let us now have a look at the new features of C# 11 which have been discussed as follows:

[Auto-default struct](#contents.xhtml_sc2_4a)

In the previous version of C#, structures where the constructor did not assign all the fields gave compile errors, but not anymore. In C# 11 any fields not explicitly initialized are set to their default value:

1.  namespace _01_NewFeatures.Features;

3.  internal  class  AutoDefaultStructure
4.  {
5.  public  void  Demo()
6.  {
7.  Point p = new Point(-5);
8.  Console.WriteLine(p.ToString());
9.  }
10.  }

12.  internal  struct  Point
13.  {
14.  public  int X { get; init; }
15.  public  int Y { get; init; }

17.  public  Point(int  x)
18.  {
19.  X = x;
20.  }

22.  public  override  string  ToString()
23.  {
24.  return  $"[X = {X}, Y = {Y}]";
25.  }
26.  }

In the preceding example, the Point constructor on line 17 gives compile error with C# 10 (.NET 6) - CS0843: Auto-implemented property ‘{0}’ must be fully assigned before control is returned to the caller. Consider updating to language version ‘{1}’ to auto-default the property. However, it works fine in C# 11 and the value of the property Y is set to default zero by the compiler.

[Extended nameof scope](#contents.xhtml_sc2_5a)

A nameof expression produces the name of a variable, type, or member as the string constant. In C# 11 this definition is extended to allow nameof operator to specify the name of a method parameter in an attribute on the method or parameter declaration. This feature is most often useful to add attributes for nullable static analysis.

1.  namespace _01_NewFeatures.Features;

3.  public  class  CustomNullCheck : Attribute
4.  {
5.  private  readonly  string _paramName;
6.  public  CustomNullCheck(string  paramName)
7.  {
8.  _paramName = paramName;
9.  }
10.  }

12.  internal  class  ExtendedNameOfScope
13.  {
14.  [CustomNullCheck(nameof(values))] //C# 11
15.  public  void  Demo(List<int> values)
16.  {
17.  Console.WriteLine(nameof(values)); //output: values
18.  Console.WriteLine(nameof(values.Count)); // output: Count

20.  Name = null; //throws exception: Name cannot be null (Parameter 'value')

22.  [CustomNullCheck(nameof(T))] //C# 11
23.  void  LocalFunction<T>(T param)
24.  { }

26.  var  lambdaExpression = ([CustomNullCheck(nameof(someNumber))] int  someNumber) => someNumber.ToString(); //C# 11
27.  }

29.  private  string _name;
30.  public  string Name
31.  {
32.  get => _name;
33.  set => _name = value ?? throw  new  ArgumentNullException(nameof(value), $"{nameof(Name)} cannot be null");
34.  }
35.  }

In the preceding snippet, lines 17, 18 and 20 demonstrate existing usage of nameof. The new feature allows using CustomNullCheck(nameof(values)) on line 14 instead of CustomNullCheck("values"). Lines 22 and 26 demonstrate the extended scope with local function and parameter declaration, respectively.

[File-scoped types](#contents.xhtml_sc2_6a)

C# 11 introduces a new access modifier file. The visibility of created type is scoped to the source file in which it is declared. This feature helps source generator authors avoid naming collisions. file local types cannot be nested, and no accessibility modifiers (private, public, protected, and so on.) can be used in combination with file on a type as it is treated as an independent concept from accessibility.

1.  //File1.cs

3.  namespace _01_NewFeatures.Features;

5.  internal  class  FileLocalTypes
6.  {
7.  }

9.  file  class  Animal
10.  {
11.  }

13.  // File2.cs

15.  namespace SecondNS;

17.  file  class  Animal  // different symbol than the Animal in File1
18.  {
19.  }

21.  // File3.cs
22.  using SecondNS;

24.  var animal = new Animal(); // error: The type or namespace name 'Animal' could not be found.

The Animal class declared in File1.cs and File2.cs are different because of the file modifier. Trying to access either in File3.cs gives error.

[Generic attributes](#contents.xhtml_sc2_7a)

C# 11 now supports generics for attribute classes as well. Earlier attributes had to accept System.Type as a parameter and users passed a typeof expression to provide the attribute with types that it needs. Attribute can now use the existing system of type parameter constraints to express the requirements for the types they take as input.

1.  namespace _01_NewFeatures.Features;

3.  // Before C# 11 -----------
4.  internal  class  BeforeCSharp11
5.  {
6.  [CustomTypeAttribute(typeof(string))]
7.  public  string? Method() => default;
8.  }

10.  public  class  CustomTypeAttribute : Attribute
11.  {
12.  public  CustomTypeAttribute(Type  t) => ParamType = t;

14.  public  Type ParamType { get; }
15.  }

17.  // ------------------------

19.  internal  class  GenericAttributes
20.  {
21.  [GenericAttribute<string>()]
22.  public  string  Method() => default;
23.  }

25.  public  class  GenericAttribute<T> : Attribute { }

The preceding line, line 10 defines CustomType attribute in the older way. Notice the constructor accepting parameter t of type Type. When this attribute is used on line 6 typeof(string) is passed. The newer way allows defining attributes using generic as on line 25 notice the <T> with GenericAttribute. To use this <string> is passed on line 21.

[Generic math](#contents.xhtml_sc2_8a)

.NET 7 introduces new math-related generic interfaces to the base class library. In addition, C# 11 allows defining static abstract interface members. Together, these innovations enable performing mathematical operations generically — that is, without having to know the exact type. Earlier one had to create an overloaded method for each type. Now a single generic method can be written, where the type of the parameter is constrained to be a number-like type.

1.  using System.Numerics;
2.  namespace _01_NewFeatures.Features;

4.  internal  class  GenericMath
5.  {
6.  public  void  Demo()
7.  {
8.  Console.WriteLine("GenericMath.Demo() ---- ");

10.  //Example 1
11.  Vector  v1 = new() { X = -2, Y = 8 };
12.  Vector  v2 = new() { X = 6, Y = -1 };

14.  Console.WriteLine(v1 + v2); //Outputs: Vector (X: 4; Y: 7)
15.  Console.WriteLine(v1 - v2); //Outputs: Vector (X: -8; Y: 9)

17.  //Example 2
18.  Console.WriteLine(new List<int> { 5, -3, 0, 25 }.AddNumbers<int, long>()); //Outputs: 27
19.  Console.WriteLine(new List<double> { 5.5, 3.2, 4.6, 10.7 }.AddNumbers<double, double>()); //Outputs: 24
20.  Console.WriteLine("----------------------- ");
21.  }
22.  }

24.  public  record  Vector :
25.  IAdditionOperators<Vector, Vector, Vector>,
26.  ISubtractionOperators<Vector, Vector, Vector>
27.  {
28.  public  int X { get; set; }
29.  public  int Y { get; set; }

31.  public  static  Vector  operator +(Vector  self, Vector  other)
32.  {
33.  return  new  Vector { X = self.X + other.X, Y = self.Y + other.Y };
34.  }

36.  public  static  Vector  operator -(Vector  self, Vector  other)
37.  {
38.  return  new  Vector { X = self.X - other.X, Y = self.Y - other.Y };
39.  }

41.  public  override  string  ToString() => $"Vector (X: {X}; Y: {Y})";
42.  }

44.  internal  static  class  MathExtensions
45.  {
46.  public  static  TResult  AddNumbers<T, TResult>(this  IEnumerable<T> values)
47.  where  T : INumber<T>
48.  where  TResult : INumber<TResult>
49.  {
50.  TResult  result = TResult.Zero;

52.  foreach (var value  in values)
53.  {
54.  result += TResult.CreateChecked(value);
55.  }

57.  return result;
58.  }
59.  }

The preceding snippet demonstrates two examples. In the first example, Vector record implements IAdditionOperators which contains the + operator declared as static abstract and is implemented explicitly in the Vector record. Similarly, Vector also implements ISubtractionOperators containing the - operator declared as static abstract and is implemented explicitly.

In the second example, AddNumbers extension method adds a set of values together. The method takes in an IEnumerable<T> where T must be a type that implements the INumber<T> interface. It returns a TResult with a similar constraint (it must be a type that implements INumber<TResult>). Because of the two generic parameters, it is allowed to return a different type than it takes as an input. For example, AddNumbers<int, long> allows summing the values of an int[] and returning a 64-bit result to help avoid overflow. TResult.Zero efficiently gives the value of 0 as a TResult and TResult.CreateChecked converts value from a T into a TResult throwing an OverflowException if it is too large or too small to fit in the destination format.

There may be a question why we cannot do simply as follows:

61.  public  static  T  Sum<T>(this  IEnumerable<T> source)
62.  {
63.  T  sum = default;
64.  foreach (T  v  in source)
65.  {
66.  sum += v;
67.  }

69.  return sum;
70.  }

The preceding code gives error on line 66 - CS0019: Operator '+=' cannot be applied to operands of type 'T' and 'T' because we cannot use addition assignment operators on a generic class T unless it implements the INumber interface which supports the addition operator defined as static abstract member.

[List patterns](#contents.xhtml_sc2_9a)

Patterns are used in C# to match an input expression against some characteristics (or pattern combination). C# supports multiple patterns; list is the latest addition in C# 11\. List patterns evaluate sequence of elements in a list or an array to corresponding constant, type, property, or relational pattern.

1.  namespace _01_NewFeatures.Features;

3.  internal  class  ListPatterns
4.  {
5.  public  void  Demo()
6.  {
7.  var  numbers = new[] { -10, 0, 5, 7 };

9.  // Comparison with constant patterns
10.  Console.WriteLine(numbers is [-10, 0, 5, 7]); // True
11.  Console.WriteLine(numbers is [-10, 0, 5]); // False
12.  Console.WriteLine(numbers is [7, -10, 0, 5]); // False

14.  // Comparison with discard patterns
15.  Console.WriteLine(numbers is [_, 0, _, 7]); // True

17.  // Comparison with range pattern
18.  Console.WriteLine(numbers is [.., 5, _]); // True

20.  // Comparison with logical patterns
21.  Console.WriteLine(numbers is [_, <= 2, _, _]); // True

23.  // Comparison with length pattern
24.  if (numbers is [< 0, .. { Length: 2 or 4 }, > 0]) //true
25.  Console.WriteLine("Valid");
26.  else
27.  Console.WriteLine("Invalid");

29.  // Comparison with var pattern
30.  if ("Curious"  is ['c'  or  'C', 'u', .. var str, 'u', 's'  or  'S']) //true
31.  Console.WriteLine($"Matches, inner string: {str}");
32.  else
33.  Console.WriteLine($"No match");
34.  }
35.  }

The preceding snippet demonstrates comparing numbers which is a list of integers with various combinations of list patterns. The last example on line 30, compares a string with a list pattern and retrieves the value within the string using var pattern.

[Microsecond and Nanosecond (.NET 7)](#contents.xhtml_sc2_10a)

Before .NET 7, the lowest increment of time available in the various date and time structures was the tick, available as the Ticks property, one tick being 100 nanoseconds. To find anything lower than tick, developers had to perform calculations on the tick value. .NET 7 addresses this by introducing both microsecond and nanosecond to the date and time implementations – TimeSpan, TimeOnly, DateTime, and DateTimeOffset.

1.  namespace _01_NewFeatures.Features;

3.  internal  class  MicroAndNanoSeconds
4.  {
5.  public  void  Demo()
6.  {
7.  const  string dt = "0001-01-01"; //yyyy-mm-dd
8.  const  string tm1 = "00:00:00.0001000"; //hh:mm:ss.ticks
9.  const  string tm2 = "00:00:00.0000009"; //hh:mm:ss.ticks

11.  //1 sec = 10^3 milli sec = 10^6 micro sec = 10^7 ticks

13.  //DateTime examples
14.  Console.WriteLine(new  DateTime(0001, 01, 01, 00, 00, 00, 00, 100).Ticks); //1000 (100 micro sec = 1000 ticks)
15.  Console.WriteLine(DateTime.Parse($"{dt} {tm1}").Microsecond); //100 (1000 ticks = 100 micro sec)
16.  Console.WriteLine(DateTime.Parse($"{dt} {tm2}").Nanosecond); //900 (9 ticks = 900 nano sec)
17.  Console.WriteLine(DateTime.MinValue.AddMicroseconds(100).Ticks); //1000 (100 micro sec = 1000 ticks)

19.  //DateTimeOffset examples
20.  Console.WriteLine(new  DateTimeOffset(0001, 01, 01, 00, 00, 00, 00, 999, TimeSpan.FromHours(-8)).Ticks); //9990 (999 micro sec = 9990 ticks)
21.  Console.WriteLine(DateTimeOffset.Parse($"{dt} {tm1} -8").Microsecond); //100 (1000 ticks = 100 micro sec)
22.  Console.WriteLine(DateTimeOffset.Parse($"{dt} {tm2} -8").Nanosecond); //900 (9 ticks = 900 nano sec)
23.  Console.WriteLine(new  DateTimeOffset().AddMicroseconds(100).Ticks); //1000 (100 micro sec = 1000 ticks)

25.  //TimeSpan examples
26.  Console.WriteLine(new  TimeSpan(10 * TimeSpan.TicksPerMicrosecond).Ticks); //100 (10 * 10)
27.  Console.WriteLine(new  TimeSpan(10 * TimeSpan.NanosecondsPerTick).Ticks); //1000 (10 * 100)
28.  Console.WriteLine(new  TimeSpan(0, 0, 0, 1, 1, 1).Ticks); //10010010 (1 sec + 1 milli sec + 1 micro sec = 10^7 + 10^4 + 10 ticks)
29.  Console.WriteLine(TimeSpan.Parse($"{tm1}").Microseconds); //100 (1000 ticks = 100 micro sec)
30.  Console.WriteLine(TimeSpan.Parse($"{tm2}").Nanoseconds); //900 (9 ticks = 900 nano sec)
31.  Console.WriteLine(TimeSpan.FromMicroseconds(100).Ticks); //1000 (100 micro sec = 1000 ticks)

33.  //TimeOnly examples
34.  Console.WriteLine(new  TimeOnly(0, 0, 1, 1, 1).Ticks); //10010010 (1 sec + 1 milli sec + 1 micro sec = 10^7 + 10^4 + 10 ticks)
35.  Console.WriteLine(TimeOnly.Parse($"{tm1}").Microsecond); //100 (1000 ticks = 100 micro sec)
36.  Console.WriteLine(TimeOnly.Parse($"{tm2}").Nanosecond); //900 (9 ticks = 900 nano sec)
37.  }
38.  }

The preceding snippet shows how to use the new Microsecond and Nanosecond properties in the date and time related structures. Also notice the new constructors that accept the microsecond parameter (lines 14, 20, 28 and 34) and the new related methods AddMicroseconds and FromMicroseconds (lines 17, 23 and 31).

[Newlines in string interpolation expressions](#contents.xhtml_sc2_11a)

Starting C# 11, the interpolated expressions can include newlines. The text between the curly braces {} must be valid C# expression including newlines to improve readability.

1.  namespace _01_NewFeatures.Features;

3.  internal  class  NewlineInStringInterpolation
4.  {
5.  public  void  Demo()
6.  {
7.  // Example 1 - switch expression
8.  int  statusCode = 302;
9.  string  message = $"HTTP status code {statusCode} is for {statusCode switch
10.  {
11.  > 599 or < 100 => "Invalid",
12.  > 499 => "Server error",
13.  > 399 => "Client error",
14.  > 299 => "Redirection",
15.  > 199 => "Successful",
16.  > 99 => "Informational response"
17.  }}";
18.  Console.WriteLine(message); //Output: HTTP status code 302 is for Redirection

20.  // Example 2 - LINQ query
21.  int[] numbers = new  int[] { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };

23.  Console.WriteLine($"The even values of {nameof(numbers)} are {string.Join(", ",
24.  numbers.Where(n => n % 2 == 0))}."); //Output: The even values of numbers are 2, 4, 6, 8, 10.
25.  }
26.  }

The preceding code shows examples that use switch statement and LINQ query spread across multiple lines within a string interpolation expression.

[Pattern match Span<char> on a constant string](#contents.xhtml_sc2_12a)

To encourage adoption of ReadOnlySpan<char> and Span<char> (for performance reasons) pattern matching these with a constant string is allowed in C# 11.

1.  namespace _01_NewFeatures.Features;

3.  internal  class  PatternMatchingWithSpanChar
4.  {
5.  public  void  Demo()
6.  {
7.  var  readOnlySpan = "Keep it simple!".AsSpan();
8.  if (readOnlySpan is  "Keep it simple!")
9.  {
10.  Console.WriteLine("Simplicity!");
11.  }

13.  Span<char> spanChar = new  Span<char>(new  char[] { 'a', 'b', 'c' });
14.  if (spanChar is  "abc")
15.  {
16.  Console.WriteLine("Alphabets!");
17.  }
18.  }
19.  }

Line 14 in the preceding code demonstrates the is pattern matching for a Span<char> with a string literal.

[Raw string literals](#contents.xhtml_sc2_13a)

C# 11 allows a new form of string literal that starts with a minimum of three double-quote characters """ followed by the content of the string, and then ends with the same number of quotes that the literal started with. The content can be any arbitrary text including whitespaces, new lines, embedded quotes, and other special characters without requiring escape sequences. Single line raw string literals require the opening and closing quote characters on the same line. Multi-line raw string literals require both opening and closing quote characters on their own line. The newlines following the opening quote and preceding the closing quote are not included in the final content.

If the text contains three (or more) repeated double quotes, then four (or more) double quotes must be used to escape them. Raw string literals can be combined with string interpolation to include braces in the output text. Multiple $ characters denote how many consecutive braces start and end the interpolation.

1.  namespace _01_NewFeatures.Features;

3.  internal  class  RawStringLiterals
4.  {
5.  public  void  Demo()
6.  {
7.  //Example 1: string with quote, newline and tab
8.  var  xml = """
9.  <element attr="content">
10.  <body>
11.  </body>
12.  </element>
13.  """;
14.  Console.WriteLine(xml);

16.  //Example 2: string with four quotes
17.  var  line = """""
18.  This line needs four quotes """" so
19.  should terminate with five.
20.  """"";
21.  Console.WriteLine(line);

23.  //Example 3: string interpolation
24.  string  key = "100", value = "C#";
25.  string  jsonString =
26.  $$"""
27.  {
28.  "Key": {{key}},
29.  "Value": {{value}}
30.  }
31.  """;
32.  Console.WriteLine(jsonString);
33.  }
34.  }

Notice in the preceding three examples, the opening and the closing quote are on their own separate line, but the newline is ignored in the output. The white spaces in the text between is however preserved in the output.

[Regex source generation (.NET 7)](#contents.xhtml_sc2_14a)

The .NET 7 SDK includes a source generator that recognizes the new GeneratedRegex Attribute on a partial method that returns Regex. During compilation source code of regular expression is generated using the Roslyn Source Generator. The source that is emitted is part of the project in a file RegexGenerator.g.cs under System.Text.RegularExpressions.Generator within Analyzers and is easily viewable and debuggable. This code is optimized and provides an implementation of the method that implements all the logic for the Regex.

1.  using System.Text.RegularExpressions;
2.  namespace _01_NewFeatures.Features;

4.  internal  partial  class  RegexSourceGenerator
5.  {
6.  private  static  readonly  Regex VowelRegex =
7.  new(pattern: "[aeiou]",
8.  options: RegexOptions.Compiled | RegexOptions.IgnoreCase);

10.  [GeneratedRegex("[aeiou]", RegexOptions.IgnoreCase | RegexOptions.Compiled, "en-US")]
11.  private  static  partial  Regex  VowelGeneratedRegex();

13.  private  string  IsVowel(char  c)
14.  {
15.  var  d = VowelRegex.IsMatch(c.ToString()) ? "" : " not";
16.  return  $"VowelRegex: {c} is{d} vowel";
17.  }

19.  private  string  IsVowelGeneratedRegex(char  c)
20.  {
21.  var  d = VowelGeneratedRegex().IsMatch(c.ToString()) ? "" : " not";
22.  return  $"VowelGeneratedRegex: {c} is{d} vowel";
23.  }

25.  public  void  Demo()
26.  {
27.  Console.WriteLine(IsVowel('A')); //VowelRegex: A is vowel
28.  Console.WriteLine(IsVowelGeneratedRegex('e')); //VowelGeneratedRegex: e is vowel

30.  Console.WriteLine(IsVowel('c')); //VowelRegex: c is not vowel
31.  Console.WriteLine(IsVowelGeneratedRegex('S')); //VowelGeneratedRegex: S is not vowel

33.  Console.WriteLine(IsVowel('o')); //VowelRegex: o is vowel
34.  Console.WriteLine(IsVowelGeneratedRegex('I')); //VowelGeneratedRegex: I is vowel
35.  }
36.  }

The preceding code uses two different methods to check for vowels. The method IsVowel uses the traditional regular expression VowelRegex whereas IsVowelGeneratedRegex uses the source generated regular expression VowelGeneratedRegex. Both ways are equivalent, but the latter is more optimized.

[Required members](#contents.xhtml_sc2_15a)

Starting C# 11 the required modifier allows to mark fields and properties that must be initialized while declaring a type - class, struct, and record (but not interface types). Any expression that initializes a new instance of the type must initialize all the required members without this there is compilation error.

The required members in a type form a required member list which must be initialized during the construction and initialization of an instance of the type. This list is inherited by the derived types automatically that removes repetitive code.

This modifier cannot be applied on static, private or read-only members. Additionally, the SetsRequiredMembers attribute added to a constructor asserts to the compiler that the constructor does initialize all required members.

1.  using System.Diagnostics.CodeAnalysis;

3.  namespace _01_NewFeatures.Features;

5.  internal  class  RequiredMembers
6.  {
7.  public  void  Demo()
8.  {
9.  //valid
10.  var suzuki = new  Car { Make = "Suzuki", Model = string.Empty, Color = "Blue", Year = 2022 };
11.  Car toyota = new("", "Camry");

13.  //compilation error due to missing required members
14.  Car car = new();
15.  var someCar = new  Car { Model = string.Empty, Color = "Red", Year = 2020 };
16.  }
17.  }
18.  public  class  Car
19.  {
20.  public  Car() { }

22.  [SetsRequiredMembers]
23.  public  Car(string make, string model)
24.  {
25.  Make = make;
26.  Model = model;
27.  }

29.  public  required  string Make { get; init; }
30.  public  required  string Model { get; set; }
31.  public  string? Color { get; set; }
32.  public  int? Year { get; set; }
33.  }

In the preceding code, the Car class has two required properties Make and Model. Not initializing these properties results in compilation error on line numbers 14 and 15.

[Simplified ordering with System.LINQ (.NET 7)](#contents.xhtml_sc2_16a)

System.Linq now has the methods Order and OrderDescending, which are there to order an IEnumerable (and IQueryable) according to T.

1.  namespace _01_NewFeatures.Features;

3.  internal  class  SimplifiedOrdering
4.  {
5.  public  void  Demo()
6.  {
7.  var  data = new[] { 2, 1, 3, 0, -10, 25, 8, -4, 22 };

9.  //Existing way (still supported)
10.  var  sorted = data.OrderBy(e => e);
11.  var  sortedDesc = data.OrderByDescending(e => e);

13.  //New simplified way
14.  var  sortedSimplified = data.Order();
15.  var  sortedDescSimplified = data.OrderDescending();
16.  }
17.  }

The preceding code with the list of integer values is sorted using the existing way which requires passing the lambda expression e => e and the newer simplified way which sorts by the generic type T.

[Stream reading - ReadExactly and ReadAtLeast (.NET 7)](#contents.xhtml_sc2_17a)

There may be occasions when Stream.Read() may return less data than what is available in the stream or size of the buffer being passed. There are two new methods in System.IO.Stream class to help with such a situation. The new ReadExactly method is guaranteed to read exactly the number of bytes requested. If the stream ends before the requested bytes have been read, an EndOfStreamException is thrown. The new ReadAtLeast method will read at least the number of bytes requested. It can read more if more data is readily available, up to the size of the buffer. If the stream ends before the requested bytes have been read, an EndOfStreamException is thrown. Here, it is possible to opt out of throwing the exception to manage the end-of-stream scenario.

1.  namespace _01_NewFeatures.Features;

3.  internal  class  StreamReading
4.  {
5.  public  void  Demo()
6.  {
7.  using  FileStream  f = File.OpenRead("01-NewFeatures.dll");

9.  f.ReadExactly(buffer: new  byte[100]); // guaranteed to read 100 bytes from the file

11.  int  bytesRead = f.ReadAtLeast(buffer: new  byte[100],
12.  minimumBytes: 10,
13.  throwOnEndOfStream: false); // 10 <= bytesRead <= 100
14.  }
15.  }

ReadExactly method, on line 10, reads 100 bytes. ReadAtLeast method on line 11 also reads 100 bytes into buffer. Here since throwOnEndOfStream  ==  false, the return value will always be bytesRead <= buffer.Length. Callers can check for end of the stream by checking bytesRead < minimumBytes. If throwOnEndOfStream was true (which is the default), the return value will always be minimumBytes <= bytesRead <= buffer.Length. If the end of the stream is detected, an EndOfStreamException will be thrown.

[Tar APIs (.NET 7)](#contents.xhtml_sc2_18a)

.NET 7 now supports reading, writing, archiving, and extracting of Tape Archive (TAR) file archives through the newly added System.Formats.Tar assembly. These APIs can be used along with stream-based compression methods from System.IO.Compression.GZipStream to work with compressed tar files.

1.  using System.Formats.Tar;
2.  using System.IO.Compression;
3.  namespace _01_NewFeatures.Features;

5.  ///  <summary>
6.  /// Extended the sample https://learn.microsoft.com/en-us/dotnet/api/system.io.compression.gzipstream?view=net-7.0
7.  ///  </summary>
8.  internal  class  TarAPI
9.  {
10.  public  void  Demo()
11.  {
12.  const  string DemoRootFolder = "./TarApiDemo/";
13.  const  string OriginalFolder = $"{DemoRootFolder}Original/";
14.  const  string DecompressedFolder = $"{DemoRootFolder}Decompressed/";

16.  const  string TarFilePath = $"{DemoRootFolder}TarApiDemo.tar";
17.  const  string GzFilePath = $"{DemoRootFolder}TarApiDemo.tar.gz";
18.  const  string DecompressedFilePath = $"{DemoRootFolder}TarApiDemoDecompressed.tar";

20.  const  string SampleMessage = "I am excited to announce that C# 11 is out! As always, C# opens some entirely new fronts, "
21.  + "even while advancing several themes that have been in motion over past releases. "
22.  + "There are many features and many details, which are beautifully covered under "
23.  + "What’s new in C# 11 on our docs pages. What follows here is an appetizer of some "
24.  + "of the highlights - small and big.";

26.  if (Directory.Exists(DemoRootFolder))
27.  Directory.Delete(DemoRootFolder, true); //Delete any left overs of previous run

29.  //Create sample file
30.  Directory.CreateDirectory(OriginalFolder);
31.  File.WriteAllText($"{OriginalFolder}CSharpFeatures.txt", SampleMessage);

33.  //Create tarball
34.  TarFile.CreateFromDirectory(OriginalFolder, TarFilePath, false);

36.  CompressTar();

38.  DecompressTar();

40.  ReadArchiveEntry();

42.  //Extract tarball
43.  Directory.CreateDirectory(DecompressedFolder);
44.  TarFile.ExtractToDirectory(DecompressedFilePath, DecompressedFolder, true);

46.  static  void  CompressTar()
47.  {
48.  using  FileStream  originalFileStream = File.Open(TarFilePath, FileMode.Open);
49.  using  FileStream  compressedFileStream = File.Create(GzFilePath);
50.  using  GZipStream  compressor = new(compressedFileStream, CompressionMode.Compress);
51.  originalFileStream.CopyTo(compressor);
52.  }

54.  static  void  DecompressTar()
55.  {
56.  using  FileStream  compressedFileStream2 = File.Open(GzFilePath, FileMode.Open);
57.  using  FileStream  outputFileStream = File.Create(DecompressedFilePath);
58.  using  GZipStream  decompressor = new(compressedFileStream2, CompressionMode.Decompress);
59.  decompressor.CopyTo(outputFileStream);
60.  }

62.  static  void  ReadArchiveEntry()
63.  {
64.  FileStream  archiveStream = File.OpenRead(DecompressedFilePath);
65.  TarReader  reader = new(archiveStream, leaveOpen: true);
66.  TarEntry? entry;
67.  while ((entry = reader.GetNextEntry()) != null)
68.  Console.WriteLine(entry.Name);
69.  }
70.  }
71.  }

The preceding code demonstrates working with Tar files along with compression.

[Type converters - DateOnly, TimeOnly, Int128, UInt128, and Half (.NET 7)](#contents.xhtml_sc2_19a)

Type converters are often used to convert value types to and from a string. There are now type converters for the newly added primitive types DateOnly, TimeOnly, Int128, UInt128, and Half.

1.  using System.ComponentModel;
2.  namespace _01_NewFeatures.Features;

4.  internal  class  TypeConverters
5.  {
6.  public  void  Demo()
7.  {
8.  // DateOnly TypeConverter
9.  var  dateOnly = TypeDescriptor.GetConverter(typeof(DateOnly))
10.  .ConvertFromString("2022-11-08") as  DateOnly?;

12.  // TimeOnly TypeConverter
13.  var  timeOnly = TypeDescriptor.GetConverter(typeof(TimeOnly))
14.  .ConvertFromString("19:45:30") as  TimeOnly?;

16.  // Half TypeConverter
17.  var  half = TypeDescriptor.GetConverter(typeof(Half))
18.  .ConvertFromString(((Half)(-100.5)).ToString()) as  Half?;

20.  // Int128 TypeConverter
21.  var  int128 = TypeDescriptor.GetConverter(typeof(Int128))
22.  .ConvertFromString("-1701") as  Int128?;

24.  // UInt128 TypeConverter
25.  var  uint128 = TypeDescriptor.GetConverter(typeof(UInt128))
26.  .ConvertFromString("3402823669209") as  UInt128?;
27.  }
28.  }

In each of the preceding cases, type specific converter is created followed by invoking the ConvertFromString method on that.

[UTF-8 string literals](#contents.xhtml_sc2_20a)

By default, strings are stored using UTF-16 encoding in .NET. Starting C# 11, the u8 suffix can be added to a string literal to specify UTF-8 encoding, which may be useful while working with Web protocols and other libraries.

UTF-8 literals are stored as ReadOnlySpan<byte> objects. Specifying a UTF-8 string literal creates a clearer declaration than declaring the equivalent System.ReadOnlySpan<T>. To store a UTF-8 string literal as an array requires the use of ReadOnlySpan<T>.ToArray() to copy the bytes containing the literal to the mutable array.

UTF-8 string literals are not compile time constants; they are runtime constants. Therefore, they cannot be used as the default value for an optional parameter. UTF-8 string literals cannot be combined with string interpolation. So $ token and the u8 suffix cannot be used on the same string expression.

1.  using System.Text;
2.  namespace _01_NewFeatures.Features;

4.  internal  class  UTF8Strings
5.  {
6.  public  void  Demo()
7.  {
8.  // Option 1
9.  byte[] csharp10HelloWorld = Encoding.UTF8.GetBytes("Hello World");

11.  // Option 2
12.  ReadOnlySpan<byte> arrayHelloWorld = new  byte[] { 0x48, 0x65, 0x6c, 0x6c, 0x6f, 0x20, 0x57, 0x6f, 0x72, 0x6c, 0x64 };

14.  //Option 3 - New way
15.  ReadOnlySpan<byte> span = "Hello World"u8;
16.  byte[] csharp11HelloWorld = span.ToArray();

18.  Console.WriteLine(Encoding.Default.GetString(csharp10HelloWorld)); //Output: Hello World
19.  Console.WriteLine(Encoding.Default.GetString(csharp11HelloWorld)); //Output: Hello World
20.  Console.WriteLine(Encoding.Default.GetString(arrayHelloWorld)); //Output: Hello World
21.  }
22.  }

The preceding example depicts three ways to declare byte array. They produce same results when printing the array. The third option is the new one supported in C# 11.

[Warning wave 7](#contents.xhtml_sc2_21a)

By convention, any new keywords added for C# will be all lower-case ASCII characters. On creating a custom type with an all-lower-case name, a warning is raised - CS8981: The type name '{0}' only contains lower-cased ascii characters. Such names may become reserved for the language.

This can be fixed by renaming the type to include at least one non-lower case ASCII character, such as an upper-case character, a digit, or an underscore.

1.  namespace _01_NewFeatures.Features;

3.  public  class  warningwave
4.  {
5.  //raises warning: CS8981: The type name 'warningwave' only contains lower-cased ascii characters.
6.  //Such names may become reserved for the language.
7.  }

The preceding declaration can avoid the warning by renaming the class such as WarningWave or Warning_Wave or warningwave7 and so on.

[Conclusion](#contents.xhtml_sc2_22a)

This chapter has described some of the important changes that have been included in the recent release of .NET 7 and C# 11\. To review the complete list of changes readers are encouraged to visit the sites given in references.

The remaining chapters in the book explain how to use the latest release of C# and .NET to create the different types of applications in Visual Studio 2022 starting with the built-in application templates.

Just as to learn a new word one should start using it, similarly the best way to get a handle on the new programming concepts is to start using them in programs, happy coding!

[Points to remember](#contents.xhtml_sc2_23a)

*   .NET and .NET language specifications are open source and community driven. Interested developers can submit their issues and feature requests through the respective repository pages on GitHub and participate in discussions to get the feature included in future versions.
*   Microsoft follows a defined release cadence to deliver features to production. There is a new major release of .NET every year in November, enabling developers, the community, and businesses to plan their roadmaps.
*   Even numbered releases are Long Term Support (LTS) releases that get free support and patches for three years. Odd numbered releases are Standard Term Support (STS) releases (previously known as current releases) that get free support and patches for 18 months. The following figure shows the release roadmap for .NET Core:

![](images/Figure_1.1.png)

Figure 1.1: .NET Core release roadmap

[Exercises](#contents.xhtml_sc2_24a)

1.  Create a math library to calculate Standard Deviation. Using this method calculate the standard deviation for following values:

    *   Number of students in different sections of a class are 30, 25, 32, 38, 24
    *   Temperature readings (in degree Celsius) in a week are 25.5, 28.2, 26.2, 24.0, 27.0, 22.1, 23.4

    (Hint: Use the concept of Generic Math and create methods to find sum, average and standard deviation of either integer or real numbers)

2.  An eyewitness remembers that the suspect’s car’s number plate ended with a four-digit number. The first number out of which was either 1 or 2 and the last one was 8\. Create a search method to go through all the numbers and print the matching numbers only. Verify your method with the input of following numbers: XYZ 1034, AB 1038, XY2239, XX 2018, ZZ8321, XYZ 1008

    (Hint: Create suitable List Pattern to match with the list of strings)

[References](#contents.xhtml_sc2_25a)

*   What's new in C# 11 - C# Guide | Microsoft Learn

[https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-11)

*   What's new in .NET 7 | Microsoft Learn

[https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-7](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-7)

*   What's new in .NET 8

[https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-8](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-8)

*   What's new in C# 12

[https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-12](https://learn.microsoft.com/en-us/dotnet/csharp/whats-new/csharp-12)

*   NET Core Releases and Support

[https://devblogs.microsoft.com/dotnet/net-core-releases-and-support/](https://devblogs.microsoft.com/dotnet/net-core-releases-and-support/)

*   Themes of .NET

[https://themesof.net/](https://themesof.net/)

*   Full C# language specification

[https://github.com/dotnet/csharpstandard/tree/draft-v7/standard](https://github.com/dotnet/csharpstandard/tree/draft-v7/standard)

Join our book’s Discord space

Join the book's Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 2ASP.NET Core Web App](#contents.xhtml_ch02a)

[Introduction](#contents.xhtml_sc2_26a)

The focus of this and the next few chapters are going to be ASP.NET Core. Built over Microsoft's .NET Core platform, ASP.NET Core is an open-source, cross-platform technology to build internet-connected applications targeting different devices with different OSs deployed over the cloud or on-premises. The diagram that follows gives a bird’s eye view of the possibilities with ASP.NET core:

![](images/Figure_2.1_.png)

Figure 2.1: Possibilities with ASP.NET Core

The latest version ASP.NET Core 7.0 brings in several new changes, the primary amongst them being the improvement in performance. For specific details of the changes check out the link in the references.

[Structure](#contents.xhtml_sc2_27a)

The chapter describes the following new features:

*   Pre-requisites
*   Getting started with Razor Pages web app
    *   Structure of the (default) Razor Pages app
*   Getting started with MVC web app
    *   Structure of the (default) MVC app
*   MVC vs. Razor Pages web app
*   Developing end-to-end Razor Pages application
    *   Creating web app
    *   Unit testing
    *   Functional testing
    *   Deployment

[Objectives](#contents.xhtml_sc2_28a)

The objectives of this chapter are to develop an understanding of the different options to create a web application in Visual Studio 2022 using C# 11 and .NET 7.0 and where the ASP.NET Core Web App fits. It also gets the readers started with developing ASP.NET Core Razor Pages application end-to-end describing the concepts around it and comparing it with the MVC application. References given at the end of the chapter let the readers find more information on the topics covered in this chapter.

[Pre-requisites](#contents.xhtml_sc2_29a)

To work through the examples in this chapter, Visual Studio 2022 Community Edition or higher preferably with the latest updates is needed. To work with the Web Apps the ASP.NET and web development workload is also required. This workload installs the libraries and runtimes required for web development as well as the templates for the different types of web applications. To get the full list of components installed with this workload refer to the Visual Studio Community component directory page in the references.

[What is ASP.NET Core?](#contents.xhtml_sc2_30a)

ASP.NET Core is the building block for different types of applications. Web applications that can be accessed by any internet-connected device. Services that are consumed by other applications by invoking Application Programming Interfaces (API) over protocols such as Hypertext Protocol (HTTP) or Remote Procedure Call (RPC). Real-time web functionality where the server side invokes functions on the client side in real time.

When it comes to web applications, there are primarily two types – server-rendered and client-rendered applications. The following table compares the two types:

|  | Server rendered | Client rendered |
| Flow | On receiving a request from the user, the server generates the page HTML and styles after processing on the server-side. This page is then sent over to the client. | When a user requests a page, bare-bone static content – HTML and CSS are sent followed by JavaScript which in turn updates the browser DOM dynamically via AJAX. |
| Pros | Initial loading time is faster with better SEO. | Allows rich content and a better user experience after the initial loading. |
| Cons | Compute requirements concentrated with a server, and user interaction require a server round trip. | Initial load time could be a concern, especially for low-end devices. |
| Related ASP.NET Core application types | Razor pages, MVC, Blazor Server | Blazor WebAssembly, Single page application (SPA) using JS frameworks such as Angular or ReactJS. |

Table 2.1: Difference between server-rendered and client-rendered web applications

A hybrid option is also possible combining the server-rendered with client-rendered UI. For example, Razor components are integrated into Razor Pages and MVC apps in a hosted Blazor WebAssembly or Blazor Server solution.

[Getting started with Razor Pages web app](#contents.xhtml_sc2_31a)

To create a Razor Pages application, follow the steps below in Visual Studio 2022:

| New project creation (File &#124; New &#124; Project…) |
| --- |
|  
1.  Create a new project

 |  
1.  To narrow down the list of templates being shown select, Language: C#, Platform: All platforms, Project type: Web.
2.  Select template: ASP.NET Core Web App.
3.  Click Next.

 |
|  
*   B. Configure your new project

 |  
4.  Project name: Enter the name of your choice such as FirstRazorPages.
5.  Location: Select the location of choice.
6.  Solution: Select either Add to the solution or Create a new solution.
7.  Solution name: Provide a name in case a new solution is created.
8.  Place solution and project in the same directory: Normally we keep the solution a level higher so leave it unchecked in case a new solution is created.
9.  Click Next.

 |
|  
*   C. Additional information

 |  
10.  Framework: .NET 7.0 (Standard Term Support)
11.  Authentication type: None
12.  Configure for HTTPS: Checked
13.  Enabled Docker: Unchecked
14.  Docker OS: Applicable if the above is checked
15.  Do not use top-level statement: Unchecked
16.  Click Create

 |

Table 2.2: Steps to create new Razor Page application project.

This created a new Razor Pages project. It is possible to create a new project using dotnet command line interface (CLI) – PowerShell or Command Prompt. The easiest way to launch dotnet CLI is from within Visual Studio via Tools | Command Line or by right clicking the solution and choosing Open in Terminal. These two options launch the developer shell from the solution folder, but it is possible to launch these shells independently also. From the shell execute the following command:

dotnet new  razor --name FirstRazorPages

This creates the Razor Pages project with all the default options. And to add the newly created project to the solution:

dotnet sln  add ./FirstRazorPages/FirstRazorPages.csproj

To execute the project, select Debug | Start Debugging or F5 this launches your default browser and opens the website. Before running you may have to set the project as the start-up project by right-clicking on the project in solution explorer and choosing the option. This shows up as follows:

![](images/Figure_2.2.png)

Figure 2.2: Basic Razor Pages application

Along with this, you will notice a command window is also running. This window is for the webserver Kestrel running in the background:

![](images/Figure_2.3.png)

Figure 2.3: Webserver Kestrel's window

Closing either window or selecting Debug | Stop Debugging stops the execution.

[Structure of the (default) Razor Pages app](#contents.xhtml_sc3_32a)

On creating the new application using the ASP.NET Core web app template following important files and folders can be seen created in the Solution Explorer window:

| Connected Services | Any service dependencies such as Azure services, OpenAPI endpoints, gRPC endpoints, WCF endpoints, or Databases and data providers, show up here. |
| Dependencies &#124; Analyzers | .NET Compiler Platform (Roslyn) Analyzers inspect the code for quality, style, maintainability, design, and other issues. This inspection or analysis happens during design time in all open files. In this case Analyzer Dependencies applicable to a web application are shown here. |
| Dependencies &#124; Frameworks | This includes the list of assemblies that the project requires. By default, Microsoft.AspNetCore.App and Microsoft.NETCore.App is included. |
| Properties &#124; launchSettings.json | This is a JSON file that includes the settings needed to debug and run the .NET core application only on the local development machine and not the production server, which is included in the appsettings.json file. The http and https profiles are to invoke the default Kestrel web server. There are settings for launching with IIS also. |
| wwwroot/ | The static site content such as CSS, images, and JavaScript libraries are included in this folder. |
| Pages/ | This folder includes one or more Razor pages each being a pair of files - a Razor markup *.cshtml file that contains C# code and a PageModel class *.cshtml.cs file that defines page handler methods and data used to render the page. By convention pages having names starting with an underscore (_) are referred from other pages. |
| appsettings.json | This configuration file is used to store application configuration settings such as database connection strings, global variables, etc. This can be overridden by environment-specific settings such as appsettings.Development.json. |
| Program.cs | This file contains the application start-up code. It is here that the request handling pipeline is configured as a series of middleware components and the services required by the app. |
| Project file - *.csproj | The project file is an XML file in SDK format which describes the metadata specific to the project such as the Target .NET framework supported by the project. |
| Solution files | A solution is a structure for organizing projects in Visual Studio. The solution maintains the state information for projects in two files - .sln and .suo file. The .sln file is a text file containing information about projects within the solution and project-persisted data such as the solution folders. The .suo file is a hidden binary file within the .vs folder which contains user-specific solution options such as start-up projects, their window state, and so on. |

Table 2.3: Important files and folders in a Razor Page application

[Getting started with MVC Web App](#contents.xhtml_sc2_33a)

To create an MVC application, the steps to be followed are the same as in creating the Razor Pages app except this time the template chosen is ASP.NET Core Web App (Model-View-Controller). To create the application from dotnet CLI execute the following command:

dotnet new  mvc –name FirstMVC

The basic application when executed looks like the Razor Pages website.

[Structure of the (default) MVC app](#contents.xhtml_sc2_34a)

The structure of the basic MVC application also looks like the Razor Pages application except for the presence of the following folders instead of the Pages folder:

| Controllers | This folder contains one or more Controller classes having the action methods that respond to HTTP requests. The basic application has HomeController.cs |
| Models | This folder contains the model classes in the application which are typically populated in the controller classes and rendered through the views. ErrorViewModel.cs is seen in the basic application. |
| Views | This folder contains Views corresponding to every controller action method within a folder of its own. The shared folder contains views reusable from other views. Like Razor Pages, these views also use the Razor markup which ties together fields of model classes within HTML tags. |

Table 2.4: Important folders in a MVC application

[MVC vs Razor Pages web app](#contents.xhtml_sc2_35a)

The Model-View-Controller (MVC) pattern is a mature UI pattern that Microsoft has supported from early versions of ASP.NET. It offers separation of concerns resulting in more maintainable code. Unfortunately, the pattern as implemented in the default project templates often results in a lot of files and folders which adds to the complexity especially as an application grows.

Razor Pages is useful when there is only a static view or a simple form that just needs to perform a POST-Redirect-GET. These scenarios are the sweet spot for Razor Pages, which avoid a great deal of the convention required by MVC apps. Architecturally, Razor Pages don’t follow the MVC pattern because they lack Controllers. Rather, Razor Pages follows more of a Model-View-ViewModel (MVVM) pattern combining strong architectural design with approachability.

The following table gives specific points of differences between the two approaches to developing web apps in ASP.NET Core:

|  | MVC | Razor Pages |
| --- | --- | --- |
| Code organization | MVC apps use a controller to contain one or more actions. The controller interacts with the domain model and creates an instance of a ViewModel class. This ViewModel is passed to the view associated with that action. | Razor Pages groups together the action handler and the ViewModel (PageModel) in one class and link this class to the view called a Razor Page. All Razor Pages goes into a Pages folder in the root of the ASP.NET Core project. |
| Adding new pages | Adding a new page requires modifying a controller in one folder, a view in a nested subfolder in another folder, and a ViewModel in yet another folder. | Adding a new page only requires adding the page within the Pages folder. The associated handlers and the PageModel are created implicitly along with the page. There is also an option to create a separate model. |
| Routing | ASP.NET Core MVC apps use attributes to define routes, HTTP verbs, and route parameters | Razor Pages is convention-based and matches the page’s location within the /Pages folder hierarchy. Instead of specifying supported HTTP verbs using attributes, Razor Pages use handlers that follow a naming convention of OnVerb, where a Verb is an HTTP verb like Get, Post, and so on. |
| Example | Controllers/StudentController.cs, Models/Student.cs, Views/Student/Index.cshtml | Pages/Student/Index.cshtml &#124; Index.cshtml.cs |
| Best suited for | This is good for web apps with lots of dynamic server views, REST APIs, and AJAX calls. | This is the preferred way to code page-focused scenarios that perform basic input of data or are read-only and where the page model and markup are closely related. |

Table 2.5: Difference between MVC and Razor Pages applications

[Developing end-to-end Razor Pages application](#contents.xhtml_sc2_36a)

As part of creating a Razor Pages application, we will create a simple Digital Book Store which allows for maintaining Books related data. The application will use a SQL LocalDB database and connect to it via the Object Relational Mapper (ORM) Entity Framework Core (EF Core) using the Code First approach. The data model for the entities involved is shown as follows:

![](images/Figure_2.4.png)

Figure 2.4: Data Model

[Creating web app](#contents.xhtml_sc3_37a)

By the end of this section, a basic Razor Pages application that allows Create Read Update and Delete (CRUD) operations on Book and Publisher data should be ready. The final Books index page would look similar to the following:

![](images/Figure_2.5.png)

Figure 2.5: Final Razor Pages application

[Getting started](#contents.xhtml_sc4_38a)

Create a Razor Pages web application named DigitalBookStore choosing all the default options as described for the FirstRazorPages application earlier.

[Create models](#contents.xhtml_sc4_39a)

In the Code First approach, we create classes in our code followed by creating the corresponding database table. The opposite of it would be database first where starting with the database table we reverse engineer the model classes.

Create the model classes under /Models folder with the following code:

Publisher.cs

1.  namespace DigitalBookStore.Models;

3.  public  class  Publisher
4.  {
5.  public  int Id { get; set; }
6.  public  string Name { get; set; }

8.  public  virtual  ICollection<Book>? Books { get; set; }
9.  }

Book.cs

1.  using System.ComponentModel.DataAnnotations;

3.  namespace DigitalBookStore.Models;

5.  public  class  Book
6.  {
7.  public  int Id { get; set; }
8.  public  string Title { get; set; }
9.  public  decimal Price { get; set; }

11.  ///  <summary>
12.  /// List of one or more semi-colon separated authors string
13.  ///  </summary>
14.  public  string Authors { get; set; }

16.  public  int PublisherId { get; set; }
17.  public  virtual  Publisher? Publisher { get; set; }

19.  [DataType(DataType.Date)]
20.  public  DateTime PublishDate { get; set; }
21.  }

The Book and Publisher are related classes (or entities) and the Publisher.Books and Book.Publisher properties are navigational properties.

[Scaffolding – Book pages](#contents.xhtml_sc4_40a)

Scaffolding is the option to use the code generation feature in Visual Studio. Using this option, we will quickly create the CRUD UI pages which use EF Core.

Create a new folder /Pages/Books. Right-click the newly created Books folder and choose Add | New Scaffolded Item. In the Add New Scaffold dialog, select Razor Pages using Entity Framework (CRUD) as shown below:

![](images/Figure_2.6.png)

Figure 2.6: Add new razor pages scaffolded item

Upon clicking Add, in the next dialog choose the Model class as the Book class and create a new Data context class by clicking the + button. All others are left as default. Refer to the following figure:

![](images/Figure_2.7.png)

Figure 2.7: Razor pages scaffolding options

Once the Add button is clicked to initiate the code generation, the following changes are made to the project:

*   Dependency is added to the following packages:
    *   Microsoft.EntityFrameworkCore.SqlServer
    *   Microsoft.EntityFrameworkCore.Tools
    *   Microsoft.VisualStudio.Web.CodeGeneration.Design
*   The data context class Data/DigitalBookStoreContext.cs is created. This class helps the application work with database operations using EF Core objects.
*   A database connection string is added to appsettings.json. This is a SQL LocalDB connection string but the database itself is not yet created. LocalDB is a lightweight version of the SQL Server Express Database Engine and is intended for app development. This database stores data in .mdf files.

"ConnectionStrings": {

"DigitalBookStoreContext": "Server=(localdb)\\mssqllocaldb;Database=DigitalBookStore.Data;Trusted_Connection=True;MultipleActiveResultSets=true"

}

*   A reference to the EF Core database context is added in Program.cs. This is done via the Dependency Injection (DI) feature of ASP.NET Core. Invoked at application start-up this line will effectively instantiate the DigitalBookStoreContext object (using the connection string read from the settings) anywhere in the application where a class accepts this parameter in the constructor and is therefore dependent on the class. Separate code to create and maintain the lifecycle of the object is not required because of the DI feature.

builder.Services.AddDbContext<DigitalBookStoreContext>(options =>

options.UseSqlServer(builder.Configuration.GetConnectionString ("DigitalBookStoreContext") ?? throw  new  InvalidOperationException ("Connection string 'DigitalBookStoreContext' not found.")));

*   CRUD Razor pages (along with their respective model *.cshtml.cs classes) are added in the Pages/Books folder:
    *   Create.cshtml
    *   Delete.cshtml
    *   Details.cshtml
    *   Edit.cshtml
    *   Index.cshtml

Each of the Razor pages is pair of two files – a cshtml file which contains the HTML, CSS, and Razor markup, and a page model cshtml.cs file which combines the data being rendered and one or more page handlers such as OnGet, OnPostAsync, and so on. The page model for the Index page is shown below:

1.  using DigitalBookStore.Models;
2.  using Microsoft.AspNetCore.Mvc.RazorPages;
3.  using Microsoft.EntityFrameworkCore;

5.  namespace DigitalBookStore.Pages.Books;

7.  public  class  IndexModel : PageModel
8.  {
9.  private  readonly Data.DigitalBookStoreContext _context;

11.  public  IndexModel(Data.DigitalBookStoreContext  context)
12.  {
13.  _context = context;
14.  }

16.  public  IList<Book> Book { get;set; } = default!;

18.  public  async  Task  OnGetAsync()
19.  {
20.  if (_context.Book != null)
21.  {
22.  Book = await _context.Book
23.  .Include(b => b.Publisher).ToListAsync();
24.  }
25.  }
26.  }

Razor Pages, in this case, IndexModel, derives from PageModel. In line 11, the constructor uses DI to add the DigitalBookStoreContext to the page. In line 16, the public Book property will hold the data shown on the page and will be used to bind the fields using Razor markup on the cshtml page. Line 18 is an example of the asynchronous Get page handler. This will retrieve the list of books from the database and render them on the corresponding page; the top few lines of which are shown below:

1.  @page
2.  @model DigitalBookStore.Pages.Books.IndexModel

4.  @{
5.  ViewData["Title"] = "Index";
6.  }

8.  <h1>Index</h1>

10.  <p>
11.  <a  asp-page="Create">Create New</a>
12.  </p>
13.  <table  class="table">
14.  <thead>
15.  <tr>
16.  <th>
17.  @Html.DisplayNameFor(model => model.Book[0].Title)
18.  </th>

20.  .....

The first (mandatory) directive @page makes the file an MVC action, which means that it can handle requests. The @model directive makes the PageModel derived class available to the Razor Page. In lines 4 to 6 the @{ and } characters enclose a block of C# code. The PageModel base class contains a ViewData dictionary property that can be used to pass data to a View. Here the Title property is added to the ViewData dictionary. Line 17 shows the HTML helper @Html.DisplayNameFor which inspects the Title property referenced in the lambda expression to determine the display name.

[Scaffolding – Publisher pages](#contents.xhtml_sc4_41a)

Create a new folder /Pages/Publishers and create the CRUD pages for the Publisher model in a manner similar to the Book pages.

[Creating a database using EF Core migration](#contents.xhtml_sc4_42a)

To create the database schema and generate migrations we will use the Entity Framework Core Package Manager Console (PMC) Tools. Launch the PMC in Visual Studio from Tools | NuGet Package Manager | Package Manager Console and run the following command to verify the tools are installed:

Get-Help about_EntityFrameworkCore

In case the tools are not installed following command can be run to install the tools

Install-Package Microsoft.EntityFrameworkCore.Tools

Before starting with the database creation rename DBSet objects in DigitalBookStore Context.cs to their plural names as follows. Do this by right-clicking and selecting Rename to ensure all references are renamed and there are no compilation errors.

public  DbSet<Models.Book> Books { get; set; } = default!;

public  DbSet<Models.Publisher> Publishers { get; set; } = default!;

Values in the DBContext are read to generate the database schema scripts, by making these plurals we will ensure that the tables also follow a similar convention.

Now, run the following command to create the initial schema. Before running the command make sure to set the default project to the DigitalStoreProject in the PMC window.

Add-Migration InitialCreate

![](images/Figure_2.8.png)

Figure 2.8: Package Manager Console

The preceding command creates two files within the Migration folder:

*   <time-stamp>_InitialCreate.cs: This contains the Up and Down methods to apply or revert the database changes.
*   DigitalBookStoreContextModelSnapshot.cs: This file contains a snapshot of the current model and is used to determine what changed when adding the next migration.

With the scripts getting created we are now ready to create the actual database. Execute the following command in PMC:

Update-Database

The database so created can be examined via View | SQL Server Object Explorer in Visual Studio. This is the same database pointed to by our connection string in the appsettings.json.

[Run and verify](#contents.xhtml_sc4_43a)

At this stage, we can run our application and verify that the CRUD for Book and Publisher is working. Make sure to set the project as a start-up project. Once running you should be able to see the index pages by adding /Books and /Publishers to the URL.

[Clean-up](#contents.xhtml_sc4_44a)

Before proceeding further, we will clean up the code generated by scaffolding.

We would like to enforce the file-scoped namespaces instead of block-scoped. Invoke the Tools | Options dialog in Visual Studio and find the Code Style settings for C#. Scroll down to the Namespace  declarations in Code block preferences and set the Preference to File scoped as shown below:

![](images/Figure_2.9.png)

Figure 2.9: Namespace code style

Invoke the code clean-up configuration in Visual Studio via Analyze | Code Cleanup | Configure Code Cleanup and include the Apply  namespace preference in Profile1 as follows:

![](images/Figure_2.10.png)

Figure 2.10: Configure code cleanup

Now right-click on your project in Solution Explorer and choose Analyze | Code Cleanup | Run Code Cleanup (Profile1).

As another example, we will simplify some of the class names. Open the Create.cshtml.cs under /Pages/Books. On the _context variable declaration line hover over the greyed-out namespace and apply the simplification over the project. This is an easy way to change all such occurrences in the project as shown below:

![](images/Figure_2.11.png)

Figure 2.11: Simplify the name throughout the project

Next, we will add links to the Books and Publisher pages on the Index page. Open the _Layout.cshtml file under /Pages/Shared and make the highlighted changes:

1.  <!DOCTYPE html>
2.  <html  lang="en">
3.  <head>
4.  <meta  charset="utf-8"  />
5.  <meta  name="viewport"  content="width=device-width, initial-scale=1.0"  />
6.  <title>@ViewData["Title"] - Digital Book Store</title>
7.  <link  rel="stylesheet"  href="~/lib/bootstrap/dist/css/bootstrap.min.css"  />
8.  <link  rel="stylesheet"  href="~/css/site.css"  asp-append-version="true"  />
9.  <link  rel="stylesheet"  href="~/DigitalBookStore.styles.css"  asp-append-version="true"  />
10.  </head>
11.  <body>
12.  <header>
13.  <nav  class="navbar navbar-expand-sm navbar-toggleable-sm navbar-light bg-white border-bottom box-shadow mb-3">
14.  <div  class="container">
15.  <a  class="navbar-brand"  asp-area=""  asp-page="/Index">Digital Book Store</a>
16.  <button  class="navbar-toggler"  type="button"  data-bs-toggle="collapse"  data-bs-target=".navbar-collapse"  aria-controls="navbarSupportedContent"
17.  aria-expanded="false"  aria-label="Toggle navigation">
18.  <span  class="navbar-toggler-icon"></span>
19.  </button>
20.  <div  class="navbar-collapse collapse d-sm-inline-flex justify-content-between">
21.  <ul  class="navbar-nav flex-grow-1">
22.  <li  class="nav-item">
23.  <a  class="nav-link text-dark"  asp-area=""  asp-page="/Books/Index">Books</a>
24.  </li>
25.  <li  class="nav-item">
26.  <a  class="nav-link text-dark"  asp-area=""  asp-page="Publishers/Index">Publishers</a>
27.  </li>
28.  </ul>
29.  </div>
30.  </div>
31.  </nav>
32.  </header>
33.  @*.....Omitted...*@

Also, change the H1 heading in the Index.cshtml pages for Books and Publisher to their respective names, that is, Books and Publishers respectively instead of Index.

After all the changes the project should compile and run successfully showing up as follows:

![](images/Figure_2.12.png)

Figure 2.12: Refined application

[Seeding](#contents.xhtml_sc4_45a)

So far, we have been running the project without any data. We could create data by using the create screens which are fully functional, but we will programmatically seed some records for our testing purposes. Create a new class /Data/SeedData.cs with the following content:

1.  using DigitalBookStore.Models;

3.  namespace DigitalBookStore.Data;

5.  public  class  SeedData
6.  {
7.  public  static  void  Initialize(DigitalBookStoreContext  context)
8.  {
9.  if (context.Books.Any())
10.  {
11.  return;
12.  }

14.  var  books = new  Book[]
15.  {
16.  new  Book
17.  {
18.  Title="Design Patterns: Elements of Reusable Object-Oriented Software",
19.  Price=1205,
20.  Publisher=new  Publisher
21.  {
22.  Name="Addison-Wesley Professional"
23.  },
24.  PublishDate=new  DateTime(1994,10,31),
25.  Authors = "Richard Helm;Erich Gamma;Ralph Johnson;John Vlissides"
26.  },
27.  new  Book
28.  {
29.  Title="Stranger in a Strange Land",
30.  Price=2290,
31.  Publisher=new  Publisher
32.  {
33.  Name="Penguin Classics"
34.  },
35.  PublishDate=new  DateTime(2016,10,25),
36.  Authors = "Robert Heinlein"
37.  },
38.  new  Book
39.  {
40.  Title="Masala Lab: The Science of Indian Cooking: The Science of Indian Cooking",
41.  Price=277,
42.  Publisher=new  Publisher
43.  {
44.  Name="Penguin Random House India"
45.  },
46.  PublishDate=new  DateTime(2020,12,14),
47.  Authors = "Krish Ashok"
48.  },
49.  new  Book
50.  {
51.  Title="The Lucky List",
52.  Price=1142,
53.  Publisher=new  Publisher
54.  {
55.  Name="Simon & Schuster Books for Young Readers"
56.  },
57.  PublishDate=new  DateTime(2021,6,1),
58.  Authors = "Rachael Lippincott"
59.  },
60.  new  Book
61.  {
62.  Title="Cemetery Boys",
63.  Price=1160,
64.  Publisher=new  Publisher
65.  {
66.  Name="Swoon Reads"
67.  },
68.  PublishDate=new  DateTime(2020,9,1),
69.  Authors = "Aiden Thomas"
70.  },
71.  new  Book
72.  {
73.  Title="Atomic Habits",
74.  Price=468,
75.  Publisher=new  Publisher
76.  {
77.  Name="Random House Business Books"
78.  },
79.  PublishDate=new  DateTime(2018,10,30),
80.  Authors = "Atomic Habits",           
81.  },
82.  new  Book
83.  {
84.  Title="Ikigai: The Japanese secret to a long and happy life",
85.  Price=332,
86.  Publisher=new  Publisher
87.  {
88.  Name="Random House UK"
89.  },
90.  PublishDate=new  DateTime(2017,9,27),
91.  Authors = "Héctor García;Heather Cleary"
92.  }
93.  };
94.  context.Books.AddRange(books);
95.  context.SaveChanges();

97.  var  publishers = new  Publisher[]
98.  {
99.  new  Publisher{Name = "O'Reilly Media"},
100.  new  Publisher{Name="Hutchinson Heinemann"},
101.  new  Publisher{Name="Viking"},
102.  new  Publisher{Name="Manjul Publishing House"}
103.  };
104.  context.Publishers.AddRange(publishers);
105.  context.SaveChanges();
106.  }
107.  }

The SeedData class has a static Initialize method which accepts the database context as a parameter and uses it to save the records in the database in lines 95 and 105\. Before the save, collections of Books and Publisher records are created. The check on line 9 ensures that we run this code only when there are no Books records in database.

We still need to invoke this code during application start-up. To do that, include the highlighted code from the following snippet in Program.cs.

1.  if (!app.Environment.IsDevelopment())
2.  {
3.  app.UseExceptionHandler("/Error");
4.  app.UseHsts();
5.  }

7.  using (var  scope = app.Services.CreateScope())
8.  {
9.  var  services = scope.ServiceProvider;

11.  var  context = services.GetRequiredService<DigitalBookStoreContext>();
12.  context.Database.EnsureCreated();
13.  SeedData.Initialize(context);
14.  }

16.  app.UseHttpsRedirection();
17.  app.UseStaticFiles();

The highlighted code first creates an instance of database context from the DI container in line 11\. The EnsureCreated method in line 12, takes no action if a database for the context exists. If no database exists, it creates the database and schema. In line 13, the SeedData.Initialize method is invoked with the database context instance. The using statement ensures the context is disposed of when the seed method completes.

Running the project now should show the seeded records on the respective index pages. Books index page shows up as follows:

![](images/Figure_2.13.png)

Figure 2.13: Books index page after seeding

The Publisher’s index page shows up as follows:

![](images/Figure_2.14.png)

Figure 2.14: Publishers index page after seeding

These pages are fully functional with the CRUD working. Also, note that the Publisher values related to Books were inserted correctly in the Publishers table even though the seeding data didn’t provide them as part of the Publishers collection as the relationship was handled behind the scenes by EF Core.

[UI refinements](#contents.xhtml_sc4_46a)

A book may have many authors, and since we have limited horizontal space on a page, we may want to show only the first name in the book listing. We can also remove the publisher column from the listing page, which shows the ID. Introduce a new property in /Models/Book.cs that shows the name of the first author when there is more than one author. Also, add the given annotations on the Price and the PublishDate properties to see a currency-formatted price and formatted display name for publish date. The changed Book class with the changes highlighted looks like following:

1.  using Microsoft.EntityFrameworkCore.Metadata.Internal;
2.  using Microsoft.IdentityModel.Tokens;
3.  using System.ComponentModel.DataAnnotations;
4.  using System.ComponentModel.DataAnnotations.Schema;

6.  namespace DigitalBookStore.Models;

8.  public  class  Book
9.  {
10.  public  int Id { get; set; }
11.  public  string Title { get; set; }

13.  [DataType(DataType.Currency), Column(TypeName = "decimal(18, 2)")]
14.  public  decimal Price { get; set; }

16.  ///  <summary>
17.  /// List of one or more semi-colon separated authors string
18.  ///  </summary>
19.  public  string Authors { get; set; }

22.  public  string AuthorsListDisplay
23.  {
24.  get
25.  {
26.  if (!Authors.IsNullOrEmpty())
27.  {
28.  var  authors = Authors.Split(';');
29.  if (authors.Length > 1)
30.  return  $"{authors[0]}, et al.";
31.  else
32.  return Authors;
33.  }
34.  return  string.Empty;
35.  }
36.  }

38.  public  int PublisherId { get; set; }
39.  public  Publisher? Publisher { get; set; }

41.  [Display(Name = "Publish Date"), DataType(DataType.Date)]
42.  [DisplayFormat(DataFormatString = "{0:MMM dd, yyyy}")]

43.  public  DateTime PublishDate { get; set; }
44.  }

To make the changes on the View side, remove the highlighted code from /Pages/Books/Index.cshtml. Also, in line 23 notice the use of the newly created AuthorsListDisplay property instead of Authors.

1.  ... <th>
2.  @Html.DisplayNameFor(model => model.Book[0].Authors)
3.  </th>

4.  <th>
5.  @Html.DisplayNameFor(model => model.Book[0].Publisher)
6.  </th>

7.  <th>
8.  @Html.DisplayNameFor(model => model.Book[0].PublishDate)
9.  </th>
10.  <th></th>
11.  </tr>
12.  </thead>
13.  <tbody>
14.  @foreach (var  item  in Model.Book) {
15.  <tr>
16.  <td>
17.  @Html.DisplayFor(modelItem => item.Title)
18.  </td>
19.  <td>
20.  @Html.DisplayFor(modelItem => item.Price)
21.  </td>
22.  <td>
23.  @Html.DisplayFor(modelItem => item.AuthorsListDisplay)
24.  </td>

25.  <td>
26.  @Html.DisplayFor(modelItem => item.Publisher.Id)
27.  </td>

28.  <td>
29.  @Html.DisplayFor(modelItem => item.PublishDate)
30.  </td>
31.  ...

With these changes the Books Index page looks as follows:

![](images/Figure_2.15.png)

Figure 2.15: Books index page with UI refinements

[Update Publisher model](#contents.xhtml_sc4_47a)

The namespace System.ComponentModel.DataAnnotations includes a set of built-in validation attributes that are applied declaratively to a class or property to help with formatting or validation. Some examples of validation attributes are [Required], [StringLength], [RegularExpression], and [Range].

Here, we will add a new field in the Publisher model and add more annotations for validation purposes. Make the highlighted changes to the /Models/Publisher.cs class:

1.  using System.ComponentModel.DataAnnotations;

3.  namespace DigitalBookStore.Models;

5.  public  class  Publisher
6.  {
7.  public  int Id { get; set; }

9.  [StringLength(100, MinimumLength = 5)]

10.  public  string Name { get; set; }

12.  [DataType(DataType.EmailAddress)]
13.  public  string? Email { get; set; }

15.  public  ICollection<Book>? Books { get; set; }
16.  }

To reflect the changes in the database, enter the command in PMC:

Add-Migration PublisherUpdate

The Up method in the generated /Migrations/<timestamp>_PublisherUpdate.cs reflects the corresponding Alter commands:

1.  protected  override  void  Up(MigrationBuilder migrationBuilder)
2.  {
3.  migrationBuilder.AlterColumn<string>(
4.  name: "Name",
5.  table: "Publishers",
6.  type: "nvarchar(100)",
7.  maxLength: 100,
8.  nullable: false,
9.  oldClrType: typeof(string),
10.  oldType: "nvarchar(max)");

12.  migrationBuilder.AddColumn<string>(
13.  name: "Email",
14.  table: "Publishers",
15.  type: "nvarchar(max)",
16.  nullable: true);
17.  }

Update the database by running following:

Update-Database

Also, update all the cshtml files in /Pages/Publishers folder to include the new Email field. The easy way to make this change is to copy the markup for the Name field and make the corresponding changes. As an example, the Create page with the changes looks as follows:

1.  @*...omitted...*@
2.  <div  class="form-group">
3.  <label  asp-for="Publisher.Name"  class="control-label"></label>
4.  <input  asp-for="Publisher.Name"  class="form-control"  />
5.  <span  asp-validation-for="Publisher.Name"  class="text-danger"></span>
6.  </div>

8.  <div  class="form-group">
9.  <label  asp-for="Publisher.Email"  class="control-label"></label>
10.  <input  asp-for="Publisher.Email"  class="form-control"  />
11.  <span  asp-validation-for="Publisher.Email"  class="text-danger"></span>
12.  </div>

13.  @*...omitted...*@

The Publisher Create page should exhibit the following behavior with these changes:

![](images/Figure_2.16.png)

Figure 2.16: Validations in the updated Publisher

We have seen how to use the annotations to add some simple validations. For more complex systems, separating the validation concern using validator objects is the recommended approach. Please refer to the Fluent Validation link in the references.

[Working with related data](#contents.xhtml_sc4_48a)

Every Book object has a mandatory publisher field but when we look at the details of any book the publisher’s name is not visible. Also, the Create and Edit Book pages show a drop-down of publisher ids we would rather see a drop-down of names to choose from it.

Book object has a navigational property Publisher but by default, it is Lazy loaded by EF. To load the property at the time of showing the details, replace the book data retrieval line of code in the Details page model present in the file /Pages/Books/Details.cshtml.cs with the following:

var  book = await _context.Books.Include(b => b.Publisher).FirstOrDefaultAsync(m => m.Id == id);

The Include method directs EF Core to eager load the related Publisher property. In the view file /Pages/Books/Details.cshtml replace the display of publisher ID with the name property as follows:

@Html.DisplayFor(model => model.Book.Publisher.Name)

With this the publisher should start showing up on the book details page:

![](images/Figure_2.17.png)

Figure 2.17: Book details with publisher name

On the Create and Edit pages to display the publisher names in the drop-down instead of ID, change the second parameter while preparing the SelectList from "Id" to "Name" in /Pages/Books/Create.cshtml.cs  and /Pages/Books/Edit.cshtml.cs:

ViewData["PublisherId"] = new SelectList(_context.Set<Publisher>(), "Id", "Name");

The drop-down can be verified on the two pages.

[Filtering records](#contents.xhtml_sc4_49a)

To add the functionality of filtering records on the Books index page we need to provide for accepting the user search field on the index page. This string should be accepted by the handler method before returning the filtered list of records.

Insert the following snippet to accept the user search string on the index page /Page/Books/Index.cshtml:

1.  <p>
2.  <a  asp-page="Create">Create New</a>
3.  </p>

5.  <form  asp-page="/Books/Index"  method="get">
6.  <div  class="form-actions no-color">
7.  <p>
8.  Search books:
9.  <input  type="text"  name="SearchString"  placeholder="Title or Author"  value="@Model.CurrentFilter"  />
10.  <input  type="submit"  name="SearchButton"  value="Search"  class="btn btn-primary"  /> |
11.  <a  asp-page="/Books/Index">Back to full List</a>
12.  </p>
13.  </div>

15.  </form>
16.  <table  class="table">

Change the corresponding page model /Pages/Books/Index.cshtml.cs as follows:

1.  using DigitalBookStore.Models;
2.  using Microsoft.AspNetCore.Mvc.RazorPages;
3.  using Microsoft.EntityFrameworkCore;

5.  namespace DigitalBookStore.Pages.Books;

7.  public  class  IndexModel : PageModel
8.  {
9.  private  readonly Data.DigitalBookStoreContext _context;

11.  public  IndexModel(Data.DigitalBookStoreContext  context)
12.  {
13.  _context = context;
14.  }

16.  public  IList<Book> Book { get; set; } = default!;

18.  public  string CurrentFilter { get; set; }

20.  public  async Task OnGetAsync(string  searchString)
21.  {
22.  if (_context.Books != null)
23.  {
24.  IQueryable<Book> qryBooks = _context.Books;

26.  CurrentFilter = searchString;

28.  if (!string.IsNullOrEmpty(searchString))
29.  qryBooks = qryBooks.Where(s => s.Title.Contains(searchString) || s.Authors.Contains(searchString));

31.  Book = await qryBooks
32.  .Include(b => b.Publisher).ToListAsync();
33.  }
34.  }
35.  }

The filter should be enabled and show up as follows:

![](images/Figure_2.18.png)

Figure 2.18: Filtering record on Books index page

[Refactor to use Repository Pattern](#contents.xhtml_sc4_50a)

A Repository Pattern is a design pattern that creates an abstraction layer between the UI (Razor Pages) and the data access layer. This additional layer helps in de-coupling the business logic of the application from the pure data access functions helping insulate the application from changes in the data store and facilitating unit testing also.

So far, we have consumed EF Core DBContext methods directly from the page model classes, we will now take a step towards introducing the layer of abstraction by implementing a GenericRepository which can be used for storing or retrieving data for the two entities that we have i.e., Book and Publisher. For a more complex system, we could have a specific repository or a service layer to handle the individual domain entity. In fact, a full n-tiered architecture would like as follows:

![](images/Figure_2.19.png)

Figure 2.19: N-Tiered architecture

Start by creating the IGenericRepository interface as follows within a new folder /Repositories:

1.  using System.Linq.Expressions;

3.  namespace DigitalBookStore.Repositories;

5.  public  interface  IGenericRepository<TEntity> where  TEntity : class
6.  {
7.  IQueryable<TEntity> GetAll();
8.  Task<TEntity> FirstOrDefault(Expression<Func<TEntity, bool>> match,
9.  string  navigationalProperty);

11.  Task  Create(TEntity  entity);
12.  Task  Update(int  id, TEntity  entity);
13.  Task  Delete(int  id);
14.  }

Implement the new interface in a new class  /Repositories/GenericRepository.cs as follows:

1.  using DigitalBookStore.Data;
2.  using Microsoft.EntityFrameworkCore;
3.  using Microsoft.IdentityModel.Tokens;
4.  using System.Linq.Expressions;

6.  namespace DigitalBookStore.Repositories;

8.  public  class  GenericRepository<TEntity> : IGenericRepository<TEntity> where  TEntity : class
9.  {
10.  protected  DigitalBookStoreContext _context;

12.  public  GenericRepository(DigitalBookStoreContext  context)
13.  {
14.  _context = context;
15.  }

17.  public  IQueryable<TEntity> GetAll()
18.  {
19.  return _context.Set<TEntity>().AsNoTracking();
20.  }

22.  public  async  Task<TEntity> FirstOrDefault(Expression<Func<TEntity, bool>> match, string  navigationalProperty)
23.  {
24.  if (navigationalProperty.IsNullOrEmpty())
25.  return  await _context.Set<TEntity>().SingleOrDefaultAsync(match);
26.  else
27.  return  await _context.Set<TEntity>().Include(navigationalProperty).SingleOrDefaultAsync(match);
28.  }

30.  public  async  Task  Create(TEntity  entity)
31.  {
32.  await _context.Set<TEntity>().AddAsync(entity);
33.  await _context.SaveChangesAsync();
34.  }

36.  public  async  Task  Update(int  id, TEntity  entity)
37.  {
38.  _context.Set<TEntity>().Update(entity);
39.  await _context.SaveChangesAsync();
40.  }

42.  public  async  Task  Delete(int  id)
43.  {
44.  var  entity = await _context.Set<TEntity>().FindAsync(id);
45.  _context.Set<TEntity>().Remove(entity);
46.  await _context.SaveChangesAsync();
47.  }
48.  }

We will now refactor the Books detail page model /Pages/Books/Details.cshtml.cs by replacing the DBContext class and its usage with corresponding methods from GenericRepository as follows:

1.  using DigitalBookStore.Models;
2.  using DigitalBookStore.Repositories;
3.  using Microsoft.AspNetCore.Mvc;
4.  using Microsoft.AspNetCore.Mvc.RazorPages;

6.  namespace DigitalBookStore.Pages.Books;

8.  public  class  DetailsModel : PageModel
9.  {
10.  private  readonly  IGenericRepository<Book> BookRepository;

12.  public  DetailsModel(IGenericRepository<Book> bookRepository)
13.  {
14.  BookRepository = bookRepository;
15.  }

17.  public  Book Book { get; set; } = default!;

19.  public  async  Task<IActionResult> OnGetAsync(int? id)
20.  {
21.  if (id == null)
22.  {
23.  return  NotFound();
24.  }

26.  var  book = await BookRepository.FirstOrDefault(m => m.Id == id, "Publisher");
27.  if (book == null)
28.  {
29.  return  NotFound();
30.  }
31.  else
32.  {
33.  Book = book;
34.  }
35.  return  Page();
36.  }
37.  }

Here we have first injected the BookRepository in the DetailsModel constructor (removing the DBContext) and in line 26 we have replaced the call to the DBContext method with the corresponding invocation to the BookRepository method. One important change is needed for this code to work and that is to register GenericRepository during the application start-up, setting up the Dependency Injection to work. Include the following line in the Program.cs:

builder.Services.AddScoped(typeof(IGenericRepository<>), typeof(GenericRepository<>));

Since this is purely a refactoring of code, the behavior of the application would remain the same even though now the implementation is different. Therefore, the book's detail page will continue to function as before.

[Unit testing](#contents.xhtml_sc3_51a)

There are many kinds of automated tests for software applications. The simplest and the lowest level test is the unit test. At a slightly higher level are integration tests followed by functional tests which simulate the perspective of the end-user. A unit test tests a single part of the application's logic without communicating with the file system, the network, or a database. Therefore, they are expected to run extremely fast and often such as upon every commit in the repository.

Here we will focus on unit testing and in the next one we will write functional tests using Web Driver. In the previous section, we introduced an abstraction layer in the form of a repository. This will help us in writing the unit tests, bypassing the EF Core calls entirely by mocking the calls to the repository.

Start by adding a new MSTest project named DigitalDataStore.Test in the solution. Since the System Under Test (SUT) is the DigitalDataStore, add a project dependency on that. Also add a reference to the latest stable version of NuGet package Moq (by authors Daniel Cazzulino, kzu). This package will help us mock the calls to the repository. Rename the UnitTest1.cs file to BookDetailsPageTests.cs and click Yes to the prompt that follows. Doing so will rename the name of the class also. Once done the project looks as follows in the solution explore:

![](images/Figure_2.20.png)

Figure 2.20: DigitalBookStore.Test project

Include the following code in the unit test BookDetailsPageTests.cs:

1.  using DigitalBookStore.Models;
2.  using DigitalBookStore.Repositories;
3.  using Microsoft.AspNetCore.Mvc;
4.  using Moq;
5.  using System.Linq.Expressions;

7.  namespace DigitalBookStore.Test;

9.  [TestClass]
10.  public  class  BookDetailsPageTests
11.  {
12.  Mock<IGenericRepository<Book>> mockBookRepository;

14.  [TestInitialize]
15.  public  void  Setup() //Runs before each test.
16.  {
17.  mockBookRepository = new  Mock<IGenericRepository<Book>>();
18.  mockBookRepository
19.  .Setup(r => r.FirstOrDefault(It.IsAny<Expression<Func<Book, bool>>>(), It.IsAny<string>()))
20.  .Returns(Task.FromResult(new  Book
21.  {
22.  Id = 100,
23.  Title = "Testing",
24.  Authors = "Test",
25.  Price = 123.45m,
26.  PublisherId = 1,
27.  PublishDate = new  DateTime(2023, 1, 1)
28.  }));
29.  }

31.  [TestMethod]
32.  public  void  DetailsPage_BookFound()
33.  {
34.  //Arrange
35.  var  pageModel = new Pages.Books.DetailsModel(mockBookRepository.Object);

37.  //Act
38.  var  result = pageModel.OnGetAsync(100);

40.  //Assert
41.  mockBookRepository.Verify(); //Verify the FirstOrDefault is invoked
42.  Assert.IsTrue(pageModel.Book.Id == 100); //Verify book field
43.  Assert.IsFalse(result.IsFaulted); //No error are generated
44.  }

46.  [TestMethod]
47.  public  void  DetailsPage_BookNotFound()
48.  {
49.  //Arrange
50.  var  pageModel = new Pages.Books.DetailsModel(mockBookRepository.Object);

52.  //Act
53.  var  result = pageModel.OnGetAsync(null);

55.  //Assert
56.  mockBookRepository.Verify(); //Verify the FirstOrDefault is invoked
57.  Assert.IsTrue(pageModel.Book == null); //Verify book is null
58.  Assert.IsTrue(result.Result is  NotFoundResult); //Result is not found
59.  }
60.  }

The test file includes unit tests around the Books details page covering two cases - one when the book data is found and another when it is not. The [TestMethod] annotation over the methods indicates that it is to be treated as a unit-test method. The Setup method with the annotation [TestInitialize] is run before running each test to register the mock call to the repository. The code starting from line 18 says that whenever the method FirstOrDefault is invoked with any parameter, we should return a Book object with a specific value instead of trying to fetch it from a database. The unit test in turn follows the steps in order – arrange to initialize for the test, act to invoke the target method followed by asserting or verifying against the expected.

Right-clicking on the test class name and selecting Run Tests executes both tests and the test run finished message can be seen in the status bar.

[Functional testing](#contents.xhtml_sc3_52a)

We will now focus on functional testing of the application. Add a new project with the name DigitalBookStore.FunctionalTest to the solution of type Web Driver Test for Edge (.NET Core). Right-click the Selenium.WebDriver package and select Update to update the NuGet package to the latest stable version. Rename the EdgeDriverTest.cs file to BookIndexPageTests.cs. The project should appear as follows:

![](images/Figure_2.21.png)

Figure 2.21: DigitalBookStore.FunctionalTest project

Next, include the following code in the BookIndexPageTests.cs file:

1.  using Microsoft.VisualStudio.TestTools.UnitTesting;
2.  using OpenQA.Selenium;
3.  using OpenQA.Selenium.Edge;

5.  namespace DigitalBookStore.FunctionalTest
6.  {
7.  [TestClass]
8.  public  class  BookIndexPageTests
9.  {
10.  private  EdgeDriver edgeDriver;
11.  private  const  string BookPageRoot = "https://localhost:44389"; //
    change suitably

13.  [TestInitialize]
14.  public  void  EdgeDriverInitialize()
15.  {
16.  var  options = new  EdgeOptions
17.  {
18.  PageLoadStrategy = PageLoadStrategy.Normal
19.  };
20.  edgeDriver = new  EdgeDriver(options)
21.  {
22.  Url = $"{BookPageRoot}/Books"
23.  };
24.  }

26.  [TestMethod]
27.  public  void  VerifyPageTitle()
28.  {
29.  Assert.AreEqual("Index - Digital Book Store", edgeDriver.Title);
30.  }

32.  [TestMethod]
33.  public  void  VerifySearch()
34.  {
35.  edgeDriver.FindElement(By.Name("SearchString")).SendKeys("The");
36.  edgeDriver.FindElement(By.Name("SearchButton")).Click();

38.  Assert.AreEqual(3, edgeDriver.FindElements(By.XPath("//table/
    tbody/tr")).Count);
39.  }

41.  [TestCleanup]
42.  public  void  EdgeDriverCleanup()
43.  {
44.  edgeDriver.Quit(); //close browser window
45.  }
46.  }
47.  }

Here, we are testing on the Books index page. The first test, in line 29, verifies that the page title is the expected one, and the second one, in line 35, searches with the text "The" and then, in line 38, verifies that 3 results are found by comparing with the number of table rows.

To see the tests running do as follows:

*   Update to the latest version of Edge browser. This may be required by the latest version of Selenium WebDriver.
*   Download the latest stable version of Microsoft Edge WebDriver for your system from [https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/) and once downloaded, extract the msedgedriver.exe file to a preferred location. Add the folder where the executable is located to the PATH environment variable.
*   Make the project to be tested DigitalBookStore as the start-up project and start it without debugging, that is, Debug | Start Without Debugging in Visual Studio. Note the URL of the website launched and use the value to set the BookPageRoot variable in line 11 of the functional test.
*   With the target website running you can come to Visual Studio, right-click on the BookIndexPageTests test class and choose Run Tests. This should launch the Edge browser twice to execute the two tests and show the Test run finished in the status bar at the end.

[Deployment](#contents.xhtml_sc3_53a)

So far, we have been developing the application on our development machine but to make this application available to the customer for testing or for production use it must be deployed on an accessible server environment. Microsoft Azure cloud environment presents an option for the deployment of our web application. Please follow the tutorial to deploy an ASP.NET Core to Azure App Service given in the references.

[Conclusion](#contents.xhtml_sc2_54a)

Razor Page is a promising option to create modern web applications in ASP.NET Core. It offers a simplified approach to tackle complexity, especially for scenarios that are conceptually page based.

The next chapter will focus on creating Web API using ASP.NET core where using the MVC pattern would make more sense.

[Points to remember](#contents.xhtml_sc2_55a)

*   Razor Pages is the latest offering in ASP.NET Core which started with version 2.0\. It provides developers with a way to create web applications without unnecessary ceremonies.
*   Razor Pages allow consolidating the concept of model, view, and controllers in separate files under separate folders into linked page files in a single folder while still allowing your code to follow logical separation of concerns.
*   If an existing ASP.NET MVC app makes heavy use of views, migrating from actions and views to Razor Pages can be considered.

[Exercises](#contents.xhtml_sc2_56a)

Enhance the Digital Book Store application developed so far in this chapter with the following new changes:

*   Add a new property in the book class named Tags representing one or more categories that a book can have. Multiple semi-colon separated values can be stored in a single string field.
*   Update the database by creating new EF Core migration.
*   Include the new field on all the CRUD UI screens. The field can be skipped from the book listing page but included on the details and delete pages. It should be available for editing on the Create and Edit pages.
*   Replace all the database context calls with Repository based calls, on the remaining pages for Book and all the CRUD pages for Publisher.
*   Write unit tests for the Publisher Details page model.
*   Write functional tests for the Publisher Index page.

[References](#contents.xhtml_sc2_57a)

*   Visual Studio Community component directory > ASP.NET and web development

[https://learn.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2022#aspnet-and-web-development](https://learn.microsoft.com/en-us/visualstudio/install/workload-component-id-vs-community?view=vs-2022#aspnet-and-web-development)

*   An Introduction To ASP.NET Razor Pages

[https://www.learnrazorpages.com/](https://www.learnrazorpages.com/)

*   Simpler ASP.NET MVC Apps with Razor Pages

[https://learn.microsoft.com/en-us/archive/msdn-magazine/2017/september/asp-net-core-simpler-asp-net-mvc-apps-with-razor-pages](https://learn.microsoft.com/en-us/archive/msdn-magazine/2017/september/asp-net-core-simpler-asp-net-mvc-apps-with-razor-pages)

*   Razor Pages with Entity Framework Core in ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/data/ef-rp/intro?view=aspnetcore-7.0&tabs=visual-studio](https://learn.microsoft.com/en-us/aspnet/core/data/ef-rp/intro?view=aspnetcore-7.0&tabs=visual-studio)

*   Testing EF Core Applications

[https://learn.microsoft.com/en-us/ef/core/testing/](https://learn.microsoft.com/en-us/ef/core/testing/)

*   Test ASP.NET Core MVC apps

[https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/test-asp-net-core-mvc-apps](https://learn.microsoft.com/en-us/dotnet/architecture/modern-web-apps-azure/test-asp-net-core-mvc-apps)

*   Razor Pages unit tests in ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/test/razor-pages-tests?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/test/razor-pages-tests?view=aspnetcore-7.0)

*   Design the infrastructure persistence layer

[https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/microservice-ddd-cqrs-patterns/infrastructure-persistence-layer-design)

*   Unit test controller logic in ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/mvc/controllers/testing?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/mvc/controllers/testing?view=aspnetcore-7.0)

*   Use WebDriver to automate Microsoft Edge

[https://learn.microsoft.com/en-us/microsoft-edge/webdriver-chromium](https://learn.microsoft.com/en-us/microsoft-edge/webdriver-chromium)

*   Tutorial: Deploy an ASP.NET Core and Azure SQL Database app to Azure App Service

[https://learn.microsoft.com/en-us/azure/app-service/tutorial-dotnetcore-sqldb-app](https://learn.microsoft.com/en-us/azure/app-service/tutorial-dotnetcore-sqldb-app)

*   Migrations Overview - EF Core

[https://learn.microsoft.com/en-us/ef/core/managing-schemas/migrations/?tabs=dotnet-core-cli](https://learn.microsoft.com/en-us/ef/core/managing-schemas/migrations/?tabs=dotnet-core-cli)

*   FluentValidation

[https://docs.fluentvalidation.net/en/latest/](https://docs.fluentvalidation.net/en/latest/)

*   Use WebDriver to automate Microsoft Edge

[https://learn.microsoft.com/en-us/microsoft-edge/webdriver-chromium](https://learn.microsoft.com/en-us/microsoft-edge/webdriver-chromium)

# [CHAPTER 3ASP.NET Core Web API](#contents.xhtml_ch03a)

[Introduction](#contents.xhtml_sc2_58a)

In the last chapter, we delved into creating web applications that can be accessed over the internet using a browser and where the communication happens over Hypertext Transfer Protocol (HTTP). Besides serving web pages, HTTP can be used to build Application Programming Interface (APIs) that expose services and data accessible from different client applications across OSs - Android, iOS, Windows, or Linux.

![](images/Figure_3.1.png)

Figure 3.1: Need for Web API

This chapter focuses on developing Web APIs using ASP.NET Core. It explains the various concepts around API development along with creating a simple Web API end-to-end.

[Structure](#contents.xhtml_sc2_59a)

The chapter will cover the following topics:

*   Overview of Web API
    *   HTTP
    *   Web API
    *   Web apps vs. Web API
*   Pre-requisites
*   Getting started with ASP.NET Core Web API
    *   Structure of the (default) Web API project
    *   Minimal API with a simplified hosting model
    *   Controller approach vs. Minimal API approach
*   Developing Web API
    *   Creating Web API project
        *   Getting started
        *   Create models
        *   Scaffolding – Books API Controller
        *   Scaffolding – Publishers API Controller
        *   Create a database using EF Core migration
        *   Run and verify
        *   Seeding
        *   JWT authentication and authorization
        *   Consuming API
    *   Unit testing
    *   Deployment

[Objectives](#contents.xhtml_sc2_60a)

The objectives of this chapter are to develop an understanding of the concepts around ASP.NET Core Web API and how to develop them in Visual Studio 2022 using C# 11 and .NET 7.0\. References given at the end of the chapter let the readers find more information on the topics covered in this chapter.

[Overview of Web API](#contents.xhtml_sc2_61a)

Before discussing Web API, let us recapitulate the fundamentals of HTTP.

[HTTP](#contents.xhtml_sc3_62a)

Hypertext Transfer Protocol (HTTP) is a widely used protocol for transmitting data over the web. It is the foundation of the modern web, and it is used to transmit data between a client (such as a web browser) and a server (such as a website).

![](images/Figure_3.2.png)

Figure 3.2: Communication in HTTP

HTTP is a request-response protocol, meaning that the client sends a request to the server, followed by the server sending the response back to the client. The request and response are both in the form of an HTTP message, which consists of a header and a body. It is also a stateless protocol, indicating that the server does not maintain any information about the client between requests. This makes it simple and scalable, but it also means that additional mechanisms are needed to maintain the state and track user sessions.

[Web API](#contents.xhtml_sc3_63a)

A Web API is an application programming interface that is used to expose data and functionality to other applications and systems over the web. It is built using the Web technologies and protocols, such as HTTP. Although not necessary but Web APIs are commonly implemented using RESTful principles. Representational State Transfer (REST) is a set of principles that define how the API should be designed and implemented. These principles include things like the use of HTTP verbs (for example, GET, POST, PUT, DELETE) to indicate the intended action, the use of HTTP status codes to indicate the outcome of the request, and the use of a uniform interface for interacting with the API.

Web APIs can be implemented using a variety of programming languages and frameworks, including ASP.NET, Java, and Python. They can be consumed by a wide range of clients, including web browsers, mobile devices, and other applications. They are designed to be lightweight and fast, with a focus on minimizing overhead and high performance. They are also typically designed to be flexible and extensible, with support for a variety of data formats and authentication mechanisms. There are other ways to expose data and functionality over the web, and the following table compares them:

|  | Web API | SOAP (Simple Object Access Protocol) API | WCF (Windows Communication Foundation) |
| Format of data exchange | JSON (JavaScript Object Notation) or XML (Extensible Markup Language) | XML | JSON, XML, or binary data |
| Protocol for communication | HTTP | HTTP Extension Framework (HTEF) | HTTP, TCP (Trans-mission Control Protocol), and named pipes. |
| REST support | Yes | No | Yes |
| General nature | Simple and lightweight. Easy to customize and extend | Support for complex data types, error handling, and security, so it requires more effort to modify or extend. | More complex and has a steeper learning curve |

Table 3.1: Comparing different ways to expose functionality over the Web

Another way to expose data is Remote Procedure Calls, and this is the subject of the next chapter.

[Web apps vs. Web API](#contents.xhtml_sc3_64a)

A web application is a software program that runs on a web server and is accessed over the internet using a web browser. It can be a standalone application, or it can be part of a larger system, but web applications are usually designed to be used by users and can include interactive features.

On the other hand, a web API is a programming interface that allows different systems to communicate with each other over the internet through a common set of protocols, such as HTTP. A web API is usually accessed by another software program rather than by a human user. The program sends a request to the web API, and the API sends back a response. The response might be data, or it might be an instruction to do something.

[Pre-requisites](#contents.xhtml_sc2_65a)

Visual Studio 2022 Community Edition or higher, preferably with the latest updates, is needed to work through the examples in this chapter. Also required is the ASP.NET and web development workload to work with the Web API.

[Getting started with ASP.NET Core Web API](#contents.xhtml_sc2_66a)

Create a new ASP.NET Core Web API project by following the steps below in Visual Studio 2022:

| New project creation (File &#124; New &#124; Project) |
|  
1.  Create a new project

 |  
1.  Narrow down the list of templates being shown by selecting Language: C#, Platform: All platforms, Project type: Web
2.  Select template: ASP.NET Core Web API
3.  Click Next.

 |
|  
*   B. Configure your new project

 |  
4.  Project name: Enter the name of your choice, such as FirstWebAPI
5.  Location: Select the location of choice
6.  Solution: Select either Add to solution  or Create a new solution
7.  Solution name: Provide a name in case a new solution is created
8.  Place solution and project in the same directory: Normally, we keep the solution a level higher, so leave it unchecked in case a new solution is created.
9.  Click Next.

 |
|  
*   C. Additional information

 |  
10.  Framework: .NET 7.0 (Standard Term Support)
11.  Authentication type: None
12.  Configure for HTTPS: Checked
13.  Enabled Docker: Unchecked
14.  Docker OS: Applicable if the above is checked.
15.  Use controllers (uncheck to use minimal APIs): Checked
16.  Enable OpenAPI support: Checked
17.  Do not use top-level statement: Unchecked
18.  Click Create.

 |

Table 3.2: Adding new ASP.NET Core Web API project

This creates a new Web API project. The new project can be created using the dotnet command line interface (CLI) with the following command.

dotnet new  webapi --name FirstWebAPI

And to add the newly created project to the solution

dotnet sln  add ./FirstWebAPI/FirstWebAPI.csproj

For executing the project, first set the project as the start-up project and then select Debug | Start Debugging or F5 to launch the Swagger UI for the Web API in the default. The UI shows up as follows:

![](images/Figure_3.3.png)

Figure 3.3: Basic Web API swagger UI

The command window for the Kestrel web server, which hosts the API in the development environment, is running in the background. Kestrel is a lightweight, cross-platform web server based on .NET Core that is used to host web applications.

![](images/Figure_3.4.png)

Figure 3.4: Web API’s Kestrel window

For demonstration, the default ASP.NET Core Web API template creates a simple, mock WeatherForecast API that generates a random set of weather forecast data for a few days. The API returns a JSON object that contains an array of forecast objects, each of which includes the forecasted temperature, descriptive summary, and other weather-related information for a specific day.

Swagger UI, which gets launched on executing the project, is a collection of HTML, JavaScript, and CSS assets that dynamically generate documentation from a Swagger-compliant API. It is an open-source tool developed and maintained by SmartBear Software for building APIs that conform to the OpenAPI specification, which is a standard for describing and documenting REST APIs. It provides a way to interact with, explore the API’s resources, and make test requests directly from the browser.

In the Swagger UI, open the GET /WeatherForecast section and click on the Try it out button followed by Execute button. This executes the API request and shows the server response as follows:

![](images/Figure_3.5.png)

Figure 3.5: WeatherForecast server response

[Structure of the (default) Web API project](#contents.xhtml_sc3_67a)

On creating the new application using the ASP.NET Core Web API template following important files and folders can be seen created in the Solution Explorer window:

| Connected Services | Any service dependencies, such as Azure services, OpenAPI endpoints, gRPC endpoints, WCF endpoints, or Databases and data providers, show up here. |
| Dependencies &#124; Analyzers | .NET Compiler Platform (Roslyn) Analyzers inspect the code for quality, style, maintainability, design, and other issues during design time in all open files. In this case, Analyzer Dependencies applicable to a web application are shown here. |
| Dependencies &#124; Frameworks | This includes the list of assemblies that the project requires. By default, Microsoft.AspNetCore.App and Microsoft.NETCore.App is included. |
| Dependencies &#124; Packages | This includes the NuGet packages that the project requires. By default, Microsoft.AspNetCore.OpenApi and Swashbuckle.AspNetCore is included. |
| Properties &#124;  launchSettings.json | This is a JSON file that includes the settings needed to debug and run the .NET core application on the local development machine (and not the production server, which is included in the appsettings.json file). The HTTP and HTTPS profiles are to invoke the default Kestrel web server. There are settings for launching with IIS Express also. |
| Controllers/WeatherForecastController.cs | Since we had initially opted for the Controller approach (instead of the Minimal API approach), this controller file, corresponding to the mock WeatherForecast API, is created. More details about the content of this file are given below. |
| appsettings.json | This configuration file is used to store application configuration settings such as database connection strings, global variables, and so on. This can be overridden by environment-specific settings such as appsettings.Development.json. |
| Program.cs | This file contains the application start-up code. It is here that the request handling pipeline is configured as a series of middleware components and the services required by the app. |
| WeatherForecast.cs | This is the model class corresponding to the mock WeatherForecast API. |
| Project file - *.csproj | The project file is an XML file in SDK format, which describes the metadata specific to the project, such as the Target .NET framework supported by the project. |
| Solution  files | A solution organizes projects in Visual Studio. The solution maintains the state information for projects in two files - .sln and .suo file. The .sln file is a text file containing information about projects within the solution and project-persisted data such as the solution folders. The .suo file is a hidden binary file within the .vs folder, which contains user-specific solution options such as start-up projects, their window state, and so on. |

Table 3.3: Important files and folders in a Web API project

The WeatherForecastController.cs file is a controller class that is created by default when a new Web API project is created in ASP.NET Core using the built-in template. It shows how to create a controller class, define actions, inject dependencies, and return data to the client. Let us examine the contents of the file:

1.  using Microsoft.AspNetCore.Mvc;

3.  namespace FirstWebAPI.Controllers;
4.  [ApiController]
5.  [Route("[controller]")]
6.  public  class  WeatherForecastController : ControllerBase
7.  {
8.  private  static  readonly  string[] Summaries = new[]
9.  {
10.  "Freezing", "Bracing", "Chilly", "Cool", "Mild", "Warm", "Balmy", "Hot", "Sweltering", "Scorching"
11.  };

13.  private  readonly  ILogger<WeatherForecastController> _logger;

15.  public  WeatherForecastController(ILogger<WeatherForecastController> logger)
16.  {
17.  _logger = logger;
18.  }

20.  [HttpGet(Name = "GetWeatherForecast")]
21.  public  IEnumerable<WeatherForecast> Get()
22.  {
23.  return  Enumerable.Range(1, 5).Select(index => new  WeatherForecast
24.  {
25.  Date = DateOnly.FromDateTime(DateTime.Now.AddDays(index)),
26.  TemperatureC = Random.Shared.Next(-20, 55),
27.  Summary = Summaries[Random.Shared.Next(Summaries.Length)]
28.  })
29.  .ToArray();
30.  }
31.  }

Specific points to notice are as follows:

*   The class is decorated with the ApiController attribute, indicating that it is an API controller class.
*   The Route annotation specifies the starting route for all the contained action methods. In this case name of the controller is WeatherForecast.
*   It derives from the ControllerBase class, which is a base class for MVC controllers that do not have view support. (The controller class in an MVC application that supports views derives from the Controller class).
*   It injects an instance of the ILogger interface into its constructor, which is supposed to be used for logging any important message. This is an example of dependency injection, which is a way of decoupling the controller from the service layer.
*   The class method Get, decorated with the HttpGet attribute, is an HTTP GET action responsible for returning the list of weather forecasts to the client in serialized JSON format. The Name parameter of the HttpGet attribute, which is optional, allows you to specify a unique name for the action method in the routing table.

The Program.cs file contains the application start-up code as follows.

1.  var  builder = WebApplication.CreateBuilder(args);

3.  //Add services to the container via DI.
4.  builder.Services.AddControllers();
5.  builder.Services.AddEndpointsApiExplorer();
6.  builder.Services.AddSwaggerGen();

8.  var  app = builder.Build();

10.  //Configure the HTTP request pipeline via middlewares.
11.  if (app.Environment.IsDevelopment())
12.  {
13.  app.UseSwagger();
14.  app.UseSwaggerUI();
15.  }

17.  app.UseHttpsRedirection();

19.  app.UseAuthorization();

21.  app.MapControllers();

23.  app.Run();

The preceding code configures the services required by the app and defines the request pipeline as a series of middleware components. Services are configured and made available throughout the application via dependency injection (DI). In line 1, when the WebApplicationBuilder is instantiated, several framework-provided services are added implicitly behind the scenes. This includes, amongst others ILogger, IConfigureOptions, and so on. Lines 4, 5, and 6 use the builder.Services to add the required services to the DI container.

This is followed by adding one or more middleware components to the pipeline by invoking the extension methods named Use{Feature}. The request handling pipeline is a series of middleware components, each performing operations on an HttpContext followed by invoking the next component in the pipeline or terminating the request.

Line 11 determines the environment the app is running in and conditionally enables the Swagger documentation middleware for a development environment. The environment value is read via the ASPNETCORE_ENVIRONMENT environment variable set in the launchSettings.json file.

[Minimal API with a simplified hosting model](#contents.xhtml_sc3_68a)

An ASP.NET Core minimal API is a simplified approach for building a fast stripped-down version of an ASP.NET Core application that is designed to expose a lightweight HTTP API. This type of application typically only includes the minimum amount of code and dependencies needed to process HTTP requests and return responses. It is possible to build fully functioning REST endpoints with minimal code and configuration, skipping traditional scaffolding and declaring API routes and actions fluently, avoiding unnecessary controllers.

The minimal API approach coupled with the new hosting model simplifies the application start-up code, which means lesser code spread across fewer files. While the newer applications can take advantage of this feature, the older model is still supported, so applications migrating to the recent version of ASP.NET Core do not need to use the new minimal hosting model. The highlights of the new hosting model are summarized below:

*   Reduces the number of files and lines of code required during application start-up. At the minimum, only one file (Program.cs) is needed with a few lines of code.
*   Combines the Startup.cs and Program.cs into a single Program.cs file.
*   An explicit Main method is not used as the entry point for the application (top-level statements).
*   Eliminate or minimize the number of using statement lines by making use of global using directives. This works with the ImplicitUsings setting in the project file, which is set to enable by default.

The following code creates a minimal API using the new hosting model that accepts a parameter and returns the weather forecast string for the day.

1.  var  builder = WebApplication.CreateBuilder(args);

3.  var  app = builder.Build();

5.  var  summaries = new[]
6.  {
7.  "Freezing", "Bracing", "Chilly", "Cool", "Mild", "Warm", "Balmy", "Hot", "Sweltering", "Scorching"
8.  };

10.  app.MapGet("WeatherForecast/{dayno}",
11.  (uint  dayno) => $"The expected weather on day {dayno} is {summaries[Random.Shared.Next(summaries.Length)]}");

13.  app.Run();

When executed, the API endpoint shows up as follows:

![](images/Figure_3.6.png)

Figure 3.6: Minimal API in action

[Controller approach vs. Minimal API approach](#contents.xhtml_sc3_69a)

In ASP.NET Core, you can build a Web API using either controller or a minimal API approach. The main difference between the two approaches is in the level of abstraction and the amount of infrastructure that is provided by the framework. Specific differences between the two approaches are outlined below:

|  | Controller-based approach | Minimal API approach |
| Type of framework | Provides a full featured, high-level framework for building APIs. | Provides a lightweight, low-level framework for building APIs. |
| Consists of | The ASP.NET Core MVC framework and its components, such as controllers, views, and models. | A minimal set of abstractions specifically designed for building APIs. |
| Features | Offers a rich set of features, such as routing, action filters, model binding, and dependency injection. | Offers a bare bone set of features focused on exposing HTTP endpoints. |
| Type of APIs built | It can be used to build APIs that serve as the back end for web applications. | Suitable for building simple APIs or APIs that need more control over the implementation. |
| Suitable for | Suitable for building complex, feature-rich APIs. | It may be faster to build and easier to maintain than a controller-based API, especially for simple APIs. |

Table 3.4: Comparing the two approaches to create Web API

Both approaches have their own advantages and trade-offs, and the choice between them will depend on the specific requirements of your application and the level of complexity and functionality that you need to support.

[Developing Web API](#contents.xhtml_sc2_70a)

We will now create a Web API around the DigitalWebStore that we started in the last chapter. We will expose all the Create, Read, Update, and Delete (CRUD) operations around Books and Publishers entities through the Web API and consume the API from a Razor Pages application that uses HTTPClient to invoke the API.

[Creating Web API project](#contents.xhtml_sc3_71a)

By the end of this section, a Web API application that allows CRUD operations on Book and Publisher data should be ready. The Swagger documentation page for the Web API would look as follows:

![](images/Figure_3.7.png)

Figure 3.7: Swagger UI for finished DigitalBookStoreAPI.

These APIs will be consumed in a Razor Pages web app, which will look as follows when developed.

![](images/Figure_3.8.png)

Figure 3.8: Razor Pages application consuming DigitalBookStoreAPI

[Getting started](#contents.xhtml_sc4_72a)

Create an Asp.NET Core Web API application named DigitalBookStoreAPI, choosing all the default options as described for the FirstWebAPI application earlier. Set the project as the start-up project in the solution and delete the files WeatherForecast.cs and ./Controllers/WeatherForecastController.cs.

[Create models](#contents.xhtml_sc4_73a)

Create the model classes under /Models folder with the following code:

Publisher.cs

1.  namespace DigitalBookStoreAPI.Models;

3.  public  class  Publisher
4.  {
5.  public  int Id { get; set; }
6.  public  string Name { get; set; }
7.  }

Book.cs

1.  namespace DigitalBookStoreAPI.Models;

3.  public  class  Book
4.  {
5.  public  int Id { get; set; }
6.  public  string Title { get; set; }
7.  public  decimal Price { get; set; }

9.  ///  <summary>
10.  /// List of one or more semi-colon separated authors string
11.  ///  </summary>
12.  public  string Authors { get; set; }

14.  ///  <summary>
15.  /// List of one or more semi-colon separated tags string
16.  ///  </summary>
17.  public  string Tags { get; set; }

19.  public  int PublisherId { get; set; }
20.  public  Publisher? Publisher { get; set; }

22.  public  DateTime PublishDate { get; set; }
23.  }

[Scaffolding – Books API Controller](#contents.xhtml_sc4_74a)

We will use the scaffolding option of Visual Studio to create a basic API controller with CRUD actions. Right-click on the Controller folder and choose Add | New Scaffolded Item. In the Add New Scaffolded Item dialog, select API Controller with actions, using Entity Framework as shown below:

![](images/Figure_3.9.png)

Figure 3.9: Add new API controller scaffolded item.

Upon clicking Add, in the next dialog, choose the Model class as the Book class and create a new Data context class by clicking the + button. All others are left as default.

![](images/Figure_3.10.png)

Figure 3.10: API controller scaffolding options

Once the Add button is clicked to initiate the code generation, the following changes are made to the project:

*   Dependency is added to the following packages.
    *   Microsoft.AspNetCore.OpenApi
    *   Microsoft.EntityFrameworkCore.SqlServer
    *   Microsoft.EntityFrameworkCore.Tools
    *   Microsoft.VisualStudio.Web.CodeGeneration.Design
    *   Swashbuckle.AspNetCore
*   The data context class Data/DigitalBookStoreAPIContext.cs are created. This class helps the application work with database operations using EF Core objects.
*   A database connection string is added to appsettings.json. This is a SQL LocalDB connection string, but the database itself is not yet created.

"ConnectionStrings": {

 "DigitalBookStoreContext": "Server=(localdb)\\mssqllocaldb;Database=DigitalBookStoreAPI.Data;Trusted_Connection=True;MultipleActiveResultSets=true"

}

*   A reference to the EF Core database context is added to the Program.cs via Dependency Injection (DI) to instantiate the DigitalBookStoreAPIContext object (using the connection string read from the settings) anywhere in the application.

Builder.Services.AddDbContext<DigitalBookStoreAPIContext>(options =>

    options.UseSqlServer(builder.Configuration.GetConnectionString("DigitalBookStoreAPIContext") ?? throw  new  InvalidOperationException("Connection string 'DigitalBookStoreAPIContext' not found.")));

*   The Books API Controller ./Controllers/BooksController.cs containing action methods corresponding to the CRUD actions is added. The partial contents are as follows:
    1.  using DigitalBookStoreAPI.Data;
    2.  using DigitalBookStoreAPI.Models;
    3.  using Microsoft.AspNetCore.Mvc;
    4.  using Microsoft.EntityFrameworkCore;

    6.  namespace DigitalBookStoreAPI.Controllers;

    8.  [Route("api/[controller]")]
    9.  [ApiController]
    10.  public  class  BooksController : ControllerBase
    11.  {
    12.  private  readonly  DigitalBookStoreAPIContext _context;

    14.  public  BooksController(DigitalBookStoreAPIContext  context)
    15.  {
    16.  _context = context;
    17.  }

    19.  // GET: api/Books
    20.  [HttpGet]
    21.  public  async  Task<ActionResult<IEnumerable<Book>>> GetBook()
    22.  {
    23.  if (_context.Books == null)
    24.  {
    25.  return  NotFound();
    26.  }
    27.  return  await _context.Books.ToListAsync();
    28.  }

    30.  // GET: api/Books/5
    31.  [HttpGet("{id}")]
    32.  public  async  Task<ActionResult<Book>> GetBook(int  id)
    33.  {
    34.  if (_context.Books == null)
    35.  {
    36.  return  NotFound();
    37.  }
    38.  var  book = await _context.Books.FindAsync(id);

    40.  if (book == null)
    41.  {
    42.  return  NotFound();
    43.  }

    45.  return book;
    46.  }
    47.  …

The preceding snippet is for the Books API controller having the action methods to support CRUD operations on the Book entity. There are two GET methods, one on line 21 retrieves all the Books and returns the list as part of the response. The GET method on line 31 fetches a particular Book data accepting the Id as parameter. Notice that all the methods are async methods to support non-blocking API calls. Some important concepts around API are described below.

Routing

REST API controller has one or more action methods. These methods, also known as endpoints, are the application's unit of request handling code. Routing is the process of matching the incoming HTTP requests with an endpoint based on the information in the HTTP request URL, method, header, and body. The matching endpoint gets invoked and it can extract the values available in HTTP request for processing.

![](images/Figure_3.11.png)

Figure 3.11: Routing in Web API

REST APIs make use of attribute routing with HTTP verb attributes. Examples of action methods along with their matching URL is listed below:

1.  using DigitalBookStoreAPI.Models;
2.  using Microsoft.AspNetCore.Mvc;

4.  namespace DigitalBookStoreAPI.Controllers;

6.  [Route("api/[controller]")]
7.  [ApiController]
8.  public  class  BookSearchController : ControllerBase
9.  {
10.  [HttpGet] // GET /api/BookSearch
11.  public  IActionResult  GetAllBooks()
12.  {
13.  return  Ok(new  List<Book>());
14.  }

16.  [HttpGet("{id}")] // GET /api/BookSearch/100
17.  public  IActionResult  SearchById(int id)
18.  {
19.  return  Ok(new  List<Book>());
20.  }

22.  [HttpGet("{year:int}")] // GET /api/BookSearch/2023
23.  public  IActionResult  SearchByYearOfPublish(int year)
24.  {
25.  return  Ok(new  List<Book>());
26.  }

28.  [HttpGet("ByTag/{tag}")] // GET /api/BookSearch/computers
29.  public  IActionResult  SearchByTag(string tag)
30.  {
31.  return  Ok(new  List<Book>());
32.  }
33.  }

Action methods and return types

Web APIs can be synchronous (process one request at a time) or asynchronous (process multiple requests simultaneously by working in a non-blocking way i.e., without waiting for a response before moving on to the next request). ASP.NET Core uses the async - await  pattern together with Task to implement the asynchronous APIs. Following is a comparison of the two declarations:

1.  [HttpGet]
2.  public  ActionResult<IEnumerable<Book>> GetBook()
3.  {
4.  if (_context.Books == null)
5.  {
6.  return  NotFound();
7.  }
8.  return _context.Books.ToList();
9.  }

1.  [HttpGet]
2.  public  async  Task<ActionResult<IEnumerable<Book>>> GetBookAsync()
3.  {
4.  if (_context.Books == null)
5.  {
6.  return  NotFound();
7.  }
8.  return  await _context.Books.ToListAsync();
9.  }

The Web API action methods in ASP.NET core support different return types. To highlight the differences, find below the synchronous versions of GET /Books action method with different return types.

Specific type

Here, we use a primitive data type, complex object, or a collection where we do not have multiple paths and return types in an action. The ProducesResponseType attribute (to help in producing more descriptive response details in Swagger documentation) is not needed because we have defined the return type explicitly. NotFound, Ok, Redirect, and so on, cannot be returned.

1.  [HttpGet("V2")]
2.  public  IEnumerable<Book> GetBook_SpecificType()
3.  {
4.  return _context.Books.ToList();
5.  }

IActionResult

This return type allows to return multiple types of data along with the status code - Ok(), NotFound(), Content(), and so on. As it returns multiple types of data, swagger would not be able to identify the output, so we need to use the ProducesResponseType explicitly as shown below:

1.  [HttpGet("V3")]
2.  [ProducesResponseType(StatusCodes.Status200OK, Type = typeof(Book))]
3.  [ProducesResponseType(StatusCodes.Status404NotFound)]
4.  public  IActionResult  GetBook_IActionResult()
5.  {
6.  if (_context.Books == null)
7.  {
8.  return  NotFound();
9.  }
10.  return  Ok(_context.Books.ToList());
11.  }

ActionResult<T>

Allows to return either an ActionResult or a specific type. ProducesResponseType attribute is not needed as the return type can be inferred from T.

1.  [HttpGet("V4")]
2.  public  ActionResult<IEnumerable<Book>> GetBook_ActionResult()
3.  {
4.  if (_context.Books == null)
5.  {
6.  return  NotFound();
7.  }
8.  return _context.Books.ToList();
9.  }

IResult

This was added in ASP.NET core 6.0 and is similar to IActionResult. Here we use the static class Results to create IResult objects representing different responses. The ProducesResponseType attribute is required for descriptive documentation.

1.  [HttpGet("V5")]
2.  [ProducesResponseType(StatusCodes.Status200OK, Type = typeof(Book))]
3.  [ProducesResponseType(StatusCodes.Status404NotFound)]
4.  public IResult GetBook_IResult()
5.  {
6.  if (_context.Books == null)
7.  {
8.  return  Results.NotFound();
9.  }
10.  return  Results.Ok(_context.Books.ToList());
11.  }

Result<T>

This return type was the recent addition in in ASP.NET Core 7.0\. It works similar to the ActionResult<T>. Here we use the static class TypedResults to return the concrete IResult object. The Results<TResult1, TResultN> union types helps in compile-time checking that a route handler actually only returns the results that it declares it does. Again ProducesResponseType attribute is not needed.

1.  [HttpGet("V6")]
2.  public  Results<NotFound, Ok<IEnumerable<Book>>> GetBook_Results()
3.  {
4.  if (_context.Books == null)
5.  {
6.  return  TypedResults.NotFound();
7.  }
8.  return  TypedResults.Ok(_context.Books.AsEnumerable());
9.  }

Model binding

Model binding in ASP.NET Core is the process of mapping data from a source in the HTTP request (such as query string, form fields, body, route data or uploaded files) to action method parameters or properties. The framework uses primitive or complex model binders to perform the mapping. The model binder uses the name of the parameter or property to match the data in the request, and it uses the data type of the parameter or property to convert the data to the correct type. By default, HTTP methods like GET and DELETE use primitive type binding whereas POST and PUT, where the model data is sent to the server, use complex type binding. The default source from the HTTP request can be altered by qualifying with attributes such as FromQuery, FromRoute, FromForm, FromBody, FromHeader. Please see a variation of POST /Book below:

1.  [HttpPost("V2")]
2.  public  async  Task<ActionResult<Book>> PostBookV2([FromBody] Book  book, [FromQuery] int  id)
3.  {
4.  if (_context.Books == null)
5.  {
6.  return  Problem("Entity set 'DigitalBookStoreAPIContext.Book'  is null.");
7.  }
8.  _context.Books.Add(book);
9.  await _context.SaveChangesAsync();

11.  return  CreatedAtAction("GetBook", new { id = id }, book);
12.  }

[Create database using EF Core migration](#contents.xhtml_sc2_75a)

To create the database schema and generate migrations we will use the Entity Framework Core Package Manager Console (PMC) Tools. Launch the PMC in Visual Studio from Tools | NuGet Package Manager | Package Manager Console and run the following command to verify the tools are installed:

Get-Help about_EntityFrameworkCore

In case the tools are not installed following command can be run to install the tools:

Install-Package Microsoft.EntityFrameworkCore.Tools

Before starting with the database creation rename DBSet objects in DigitalBook StoreAPIContext.cs to their plural names as follows. Do this by right-clicking and selecting Rename to ensure all references are renamed and there are no compilation errors.

public  DbSet<Models.Book> Books { get; set; } = default!;

public  DbSet<Models.Publisher> Publishers { get; set; } = default!;

Values in the DBContext are read to generate the database schema scripts, by making these plural we will ensure that the tables also follow similar convention. Now run the following command to create the initial schema. Before running the command make sure to set the default project to the DigitalBookStoreAPI project in the PMC window.

Add-Migration InitialCreate

The preceding command creates two files within the Migration folder:

*   <time-stamp>_InitialCreate.cs: This contains the Up and Down methods to apply or revert the database changes.
*   DigitalBookStoreAPIContextModelSnapshot.cs: This file contains a snapshot of the current model and is used to determine what changed when adding the next migration.

With the scripts getting created we are now ready to create the actual database. Execute the following command in PMC:

Update-Database

The database so created can be examined via View | SQL Server Object Explorer in Visual Studio. This is the same database pointed to by our connection string in the appsettings.json.

[Run and verify](#contents.xhtml_sc3_76a)

At this stage we can run our project to view the Swagger UI for the Books API.

![](images/Figure_3.12.png)

Figure 3.12: Initial Swagger UI

Swagger UI can be used to familiarize with the exposed API endpoints.

[Seeding](#contents.xhtml_sc3_77a)

Like database seeding in the ASP.NET Core Web App in the previous chapter, we will programmatically seed records for testing purposes. Create the class /Data/SeedData.cs on the lines of SeedData class in the DigitalBookStore project and then invoke its static Initialize method during application start up in Program.cs as follows:

1.  if (app.Environment.IsDevelopment())
2.  {
3.  app.UseSwagger();
4.  app.UseSwaggerUI();
5.  }

7.  using (var  scope = app.Services.CreateScope())
8.  {
9.  var  services = scope.ServiceProvider;

11.  var  context = services.GetRequiredService<DigitalBookStoreAPIContext>();
12.  context.Database.EnsureCreated();
13.  SeedData.Initialize(context);
14.  }

16.  app.UseHttpsRedirection();

Trying the GET /api/Books endpoint in the Swagger UI should now fetch records inserted in the database.

![](images/Figure_3.13.png)

Figure 3.13: Fetching book records after seeding.

[JWT authentication and authorization](#contents.xhtml_sc3_78a)

There are several ways to manage authentication and authorization for an ASP.NET Core Web API, including:

*   Cookies: Cookies are a common way to manage authentication in web applications. With ASP.NET Core, you can use the built-in cookie middleware to handle cookie-based authentication.
*   JWT: JSON Web Tokens (JWT) allow handling authentication and authorization in API-based applications. JWT can be easily passed in the header of an HTTP request, making it a viable choice for authenticating API calls.
*   OpenID Connect: OpenID Connect is a widely used protocol for authenticating users with an identity provider (such as Microsoft, Google, or Facebook).
*   OAuth2: OAuth2 is an open standard for authorization. Many organizations use OAuth2 to handle authorization in API-based applications.
*   Active Directory: Use Active Directory for Authentication and Authorization. It can be use via LDAP protocol or via the Active Directory Authentication Library (ADAL).
*   Third-party authentication providers: Like Google, Facebook, Twitter, etc.

JWT-based authentication is a good choice for an ASP.NET Core Web API if statelessness, scalability, and ease of use are important considerations. We will now see how to implement authentication and authorization for the DigitalBookStoreAPI using JWT tokens. The basic flow with JWT authentication implemented, will look as follows:

![](images/Figure_3.14.png)

Figure 3.14: Sequence diagram - JWT authentication

Install the Microsoft.AspNetCore.Authentication.JwtBearer package from NuGet. This package provides the JWT bearer authentication handler. Next, add the following code to configure JWT, right above the builder.Services.AddControllers() line in Program.cs:

1.  builder.Services.AddAuthentication(opt =>
2.  {
3.  opt.DefaultAuthenticateScheme = JwtBearerDefaults.AuthenticationScheme;
4.  opt.DefaultChallengeScheme = JwtBearerDefaults.AuthenticationScheme;
5.  }).AddJwtBearer(options =>
6.  {
7.  options.TokenValidationParameters = new  TokenValidationParameters
8.  {
9.  ValidateIssuer = true,
10.  ValidateAudience = true,
11.  ValidateLifetime = true,
12.  ValidateIssuerSigningKey = true,
13.  ValidIssuer = builder.Configuration["JwtAuth:Issuer"],
14.  ValidAudience = builder.Configuration["JwtAuth:Issuer"],
15.  IssuerSigningKey = new  SymmetricSecurityKey(Encoding.UTF8.GetBytes(builder.Configuration["JwtAuth:Key"]))
16.  };
17.  });

By calling the AddJwtBearer method, we are enabling the JWT authentication using the default scheme and passing as parameters the bearer options such as issuer, audience, and the secret key as read from configuration settings, which the server uses to generate the signature for JWT. Include following configuration settings, used in the preceding snippet, in appsettings.json:

1.  "JwtAuth": {
2.  "Issuer": "DemoIssuer",
3.  "Key": "This is a secret key.",
4.  "UserName": "demo",
5.  "Password": "demo"
6.  }

Also add following line in Program.cs above app.UseAuthorization() to enable the use of the JWT bearer authentication scheme:

app.UseAuthentication();

To authenticate anonymous users before they can invoke any secure API, we must provide a login endpoint. A user is going to provide a username and password, and if the credentials are valid, we are going to issue a JSON web token to the requesting client.

Before going on to create the login endpoint, we must create two model classes that will be referred from the login controller.

Create ./Models/Login.cs

1.  namespace DigitalBookStoreAPI.Models;

3.  public  class  Login
4.  {
5.  public  string? UserName { get; set; }
6.  public  string? Password { get; set; }
7.  public  string? Role { get; set; }
8.  }

Create ./Models/JWTReponse.cs

1.  namespace DigitalBookStoreAPI.Models;

3.  public  class  JWTReponse
4.  {
5.  public  string? Token { get; set; }
6.  }

Now add empty API controller ./Controllers/LoginController.cs with following content:

1.  using DigitalBookStoreAPI.Models;
2.  using Microsoft.AspNetCore.Mvc;
3.  using Microsoft.IdentityModel.Tokens;
4.  using System.IdentityModel.Tokens.Jwt;
5.  using System.Security.Claims;
6.  using System.Text;

8.  namespace DigitalBookStoreAPI.Controllers;

10.  [Route("api/[controller]")]
11.  [ApiController]
12.  public  class  LoginController : ControllerBase
13.  {
14.  private  readonly  IConfiguration _configuration;
15.  public  LoginController(IConfiguration  configuration)
16.  {
17.  _configuration = configuration;
18.  }

20.  [HttpPost()]
21.  public  IActionResult  Login([FromBody] Login  login)
22.  {
23.  if (!(login.UserName == _configuration["JwtAuth:UserName"]
24.  && login.Password == _configuration["JwtAuth:Password"])) return  Unauthorized();

26.  var  userClaims = new  List<Claim>();

28.  if (login.Role?.ToLower() is  "admin"  or  "user")
29.  userClaims.Add(new  Claim(ClaimTypes.Role, login.Role));

31.  return  Ok(new  JWTResponse
32.  {
33.  Token = new  JwtSecurityTokenHandler().WriteToken(
34.  new  JwtSecurityToken(
35.  issuer: _configuration["JwtAuth:Issuer"],
36.  audience: _configuration["JwtAuth:Issuer"],
37.  claims: userClaims,
38.  expires: DateTime.Now.AddMinutes(5),
39.  signingCredentials: new  SigningCredentials(
40.  key: new  SymmetricSecurityKey(Encoding.UTF8.GetBytes(_configuration["JwtAuth:Key"])),
41.  algorithm: SecurityAlgorithms.HmacSha256)
42.  ))
43.  });
44.  }
45.  }

The Login action method in the preceding snippet, first validates the credentials (on line 23, 24) and if found okay proceeds to generate the JWT token. On line 28, 29 if the valid role values are passed, they are used to setup the Claim object. JWT response token is generated by using the token options as read from the configuration settings.

To enforce role authorization for the Book endpoints, annotate the action methods in ./Controller/BooksController.cs as follows:

| Action method | Annotation | Remarks |
| PutBook | [HttpPut("{id}"), Authorize(Roles="User,Admin")] | Updating Book data is allowed for both User and Admin roles |
| PostBook | [HttpPost("{id}"), Authorize(Roles="User,Admin")] | Creating new Book data is allowed for both User and Admin roles |
| DeleteBook | [HttpDelete("{id}"), Authorize(Roles="Admin")] | Deleting Book data is allowed only for Admin roles |

Table 3.5: Annotating endpoints to enable authorization.

There are no changes to the Get methods to allow invocation by everyone. Finally, to have the ability to enter the JWT bearer token from the Swagger UI, modify the builder.Services.AddSwaggerGen() call in Program.cs as follows:

1.  builder.Services.AddSwaggerGen(c =>
2.  {
3.  c.AddSecurityDefinition("Bearer", new  OpenApiSecurityScheme()
4.  {
5.  Name = "Authorization",
6.  Type = SecuritySchemeType.ApiKey,
7.  Scheme = "Bearer",
8.  BearerFormat = "JWT",
9.  In = ParameterLocation.Header,
10.  Description = "Bearer JWT Authorization. \r\n\r\n Enter 'Bearer' [space] followed by token value in the text input below.\r\n\r\nExample: \"Bearer eyJhbGciOiJ\"",
11.  });
12.  c.AddSecurityRequirement(new  OpenApiSecurityRequirement {
13.  {
14.  new  OpenApiSecurityScheme {
15.  Reference = new  OpenApiReference {
16.  Type = ReferenceType.SecurityScheme,
17.  Id = "Bearer"
18.  }
19.  },
20.  new  string[] {}
21.  }
22.  });
23.  });

Adds the Bearer security definition and security requirement, describing how the API is protected, to the generated Swagger, in effect allowing the input of Bearer token value.

Now to test the API, run the project to see the Swagger UI. You may verify that you can invoke the GET Book endpoint, as they do not need any special roles. However, trying to create a new Book record by invoking the POST endpoint results in 401 Unauthorized error:

![](images/Figure_3.15.png)

Figure 3.15: POST call fails because we have not logged-in

Invoke the Login endpoint by providing the credentials demo/demo and User role and copy the generated JWT token:

![](images/Figure_3.16.png)

Figure 3.16: Login with User role to generated JWT token.

It is possible to decode and view the contents of the generated token through an online debugger available at [https://jwt.io/](https://jwt.io/). Notice, entering the secret key string in the Verify Signature section results in Signature Verified message at the bottom (without which it reads Invalid Signature).

![](images/Figure_3.17.png)

Figure 3.17: Decode JWT token.

To login using the JWT token, click on the Authorize lock icon on the Swagger UI and give the text Bearer {JWT Token} in the value text box and click on Authorize:

![](images/Figure_3.18.png)

Figure 3.18: Authorize with JWT Bearer token.

Now the Book record creation succeeds.

![](images/Figure_3.19.png)

Figure 3.19: POST call succeeds after authorization.

Trying to delete the newly created record, gives 403 Forbidden error because remember we have allowed deletion only by the Admin role:

![](images/Figure_3.20.png)

Figure 3.20: Deletion fails because Delete call requires Admin role authorization.

To get around this, you should login again, this time with Admin role, copy the generated JWT token, re-authorize, followed by invoking the Delete endpoint to see the deletion to succeed.

So far, we have seen the API authentication and authorization using the built-in JWT middleware package. There are third-party libraries, such as OpenIddict and IdentityServer4, available to implement JWT based authentication. These libraries provide additional functionality over the built-in middleware package but do add complexity to the solution. If the only need is of basic JWT authentication and authorization, the built-in middleware is a good option.

[Consuming API](#contents.xhtml_sc3_79a)

We have created the API with the intention of consuming it from various client applications. As an example, we will create a simple Razor Pages web application that consumes the DigitalBookStoreAPI.

Create a new Razor Pages Web App DigitalBookStoreAPIClient in the solution. Copy the Book and Publisher model classes from DigitalBookStoreAPI into Models folder. Adjust the namespaces to reflect the folder structure. Create BookService under ./Services folder with following content:

1.  using DigitalBookStoreAPIClient.Models;
2.  using System.Text.Json;

4.  namespace DigitalBookStoreAPIClient.Services;

6.  public  class  BookService
7.  {
8.  private  readonly  HttpClient _httpClient;
9.  public  BookService(HttpClient  client)
10.  {
11.  _httpClient = client;
12.  }

14.  public  async  Task<Book[]> GetBooksAsync()
15.  {
16.  var  responseMessage = await  this._httpClient.GetAsync(“/api/Books”);

18.  if (responseMessage != null)
19.  {
20.  var  stream = await responseMessage.Content.ReadAsStreamAsync();
21.  return  await  JsonSerializer.DeserializeAsync<Book[]>(stream,
22.  new  JsonSerializerOptions()
23.  {
24.  PropertyNameCaseInsensitive = true,
25.  PropertyNamingPolicy = JsonNamingPolicy.
    CamelCase,
26.  });
27.  }
28.  return  new  Book[] { };
29.  }
30.  }

The preceding code declares the BookService, which utilizes the HTTPClient injected via constructor DI, setup during program initialization. The list of books is received as a JSON string by invoking Books GET API request, which is then de-serialized into a list of Book objects.

Create an empty Razor Page Index.cshtml under ./Pages/Books and change its content as follows.

Index.cshtml.cs

1.  using DigitalBookStoreAPIClient.Models;
2.  using DigitalBookStoreAPIClient.Services;
3.  using Microsoft.AspNetCore.Mvc;
4.  using Microsoft.AspNetCore.Mvc.RazorPages;

6.  namespace DigitalBookStoreAPIClient.Pages.Books;

8.  public  class  IndexModel : PageModel
9.  {
10.  public  Book[] Books { get; set; }

12.  public  string ErrorMessage { get; set; }

14.  public  async  Task  OnGet([FromServices] BookService  bookService)
15.  {
16.  Books = await bookService.GetBooksAsync();

18.  if (Books.Count() == 0)
19.  ErrorMessage = “We must be sold out. Try again tomorrow.”;
20.  else
21.  ErrorMessage = string.Empty;
22.  }
23.  }

BookService is injected into the GET request handler through the FromServices attribute (as an alternative way to being injected via a constructor). BookService is then used to retrieve the list of books via API.

Index.cshtml

1.  @page
2.  @model IndexModel

4.  @{
5.  ViewData[“Title”] = “Index”;
6.  }

8.  <h1>Books</h1>

10.  <table  class=”table”>
11.  <thead>
12.  <tr>
13.  <th>
14.  @Html.DisplayNameFor(model => model.Books[0].Title)
15.  </th>
16.  <th>
17.  @Html.DisplayNameFor(model => model.Books[0].Price)
18.  </th>
19.  <th>
20.  @Html.DisplayNameFor(model => model.Books[0].Authors)
21.  </th>
22.  <th>
23.  @Html.DisplayNameFor(model => model.Books[0].PublishDate)
24.  </th>
25.  </tr>
26.  </thead>
27.  <tbody>
28.  @foreach (var  item  in Model.Books)
29.  {
30.  <tr>
31.  <td>
32.  @Html.DisplayFor(modelItem => item.Title)
33.  </td>
34.  <td>
35.  @Html.DisplayFor(modelItem => item.Price)
36.  </td>
37.  <td>
38.  @Html.DisplayFor(modelItem => item.Authors)
39.  </td>
40.  <td>
41.  @Html.DisplayFor(modelItem => item.PublishDate)
42.  </td>
43.  </tr>
44.  }
45.  </tbody>
46.  </table>

The Razor view shows the list of books via the Books property of model class IndexModel in a tabular form. We need to inject the BookService into Program.cs above the line var app = builder.Build();:

1.  builder.Services.AddHttpClient<BookService>(service =>
2.  {
3.  service.BaseAddress = new  Uri(builder.Configuration. GetValue<string>("backendUrl"));
4.  });

And the configuration setting in appsettings.json. This should be set to the URL of the DigitalBookStoreAPI on your machine.

"backendUrl": "https://localhost:7205",

We have made all the changes now to see this in action, we need to run the API project and Client project simultaneously. Right-click on the solution and select Set Startup projects… and choose multiple start-up projects as follows:

![](images/Figure_3.21.png)

Figure 3.21: Set multiple startup projects in Visual Studio

Starting the execution now starts both projects. Navigating to the /Books endpoint in the client application shows following:

![](images/Figure_3.22.png)

Figure 3.22: API Client consuming the DigitalBookStoreAPI.

[Unit testing](#contents.xhtml_sc3_80a)

The unit-testing strategy for Web API is like that for Web Apps. We generally test the different action methods in Controllers. But before undertaking that, it is useful, just like web apps, to introduce a layer of abstraction layer for the database calls, instead of directly using the EF Core DBContext. Depending upon the complexity of the application this layer of abstraction can be a Repository layer with or without business logic services. Once such a layer is added, we can mock the database calls generated from the action methods in Controllers and only test around the inputs and the generated responses.

Please refer to the previous chapter for details of introducing the Repository layer, mocking them in unit-tests, and testing the action methods.

[Deployment](#contents.xhtml_sc3_81a)

The DigitalBookStoreAPI web API that we have developed can be deployed to cloud environments such as Microsoft Azure. Please follow the tutorial to publish an ASP.NET Core web API to Azure API Management with Visual Studio given in the references.

[Conclusion](#contents.xhtml_sc2_82a)

In this chapter, we had an overview of developing Web APIs using ASP.NET Core.

The next chapter focuses on developing types of services that use Remote Procedure Calls instead of HTTP.

[Points to remember](#contents.xhtml_sc2_83a)

*   ASP.NET Core provides a simplified framework to develop APIs accessible over HTTP protocol that follow RESTful principles.
*   It also includes features like routing, model binding, and validation, which are essential for building robust web APIs.
*   Experienced developers can write APIs using the Controller approach, while newer developers have the minimal API approach to quickly become productive with fewer ceremonies.

[Exercises](#contents.xhtml_sc2_84a)

Enhance the Digital Book Store API developed so far in this chapter with the following changes:

*   Create the ./Controllers/PublishersController.cs with the CRUD actions for Publishers like the Books controller.
*   Apply role-based authorization using JWT tokens on the Publisher endpoints such that all the endpoints are secure and can be invoked only by the User role.

[Hint: Apply Authorize attribute at the controller level instead of the individual action methods]

*   Consume the Publisher Get endpoint in the DigitalBookStoreAPIClient and show a listing of all the Publishers on the Index page.

[References](#contents.xhtml_sc2_85a)

*   Create web APIs with ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/web-api/?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/web-api/?view=aspnetcore-7.0)

*   Design a microservice-oriented application

[https://learn.microsoft.com/en-us/dotnet/architecture/microservices/multi-container-microservice-net-applications/microservice-application-design](https://learn.microsoft.com/en-us/dotnet/architecture/microservices/multi-container-microservice-net-applications/microservice-application-design)

*   Call a Web API From a .NET Client (C#)

[https://learn.microsoft.com/en-us/aspnet/web-api/overview/advanced/calling-a-web-api-from-a-net-client](https://learn.microsoft.com/en-us/aspnet/web-api/overview/advanced/calling-a-web-api-from-a-net-client)

*   ASP.NET Core security topics

[https://learn.microsoft.com/en-us/aspnet/core/security/?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/security/?view=aspnetcore-7.0)

*   JWT Validation and Authorization in ASP.NET Core

[https://devblogs.microsoft.com/dotnet/jwt-validation-and-authorization-in-asp-net-core/](https://devblogs.microsoft.com/dotnet/jwt-validation-and-authorization-in-asp-net-core/)

*   JWT Authentication in ASP.NET Core Web API

[https://code-maze.com/authentication-aspnetcore-jwt-1/](https://code-maze.com/authentication-aspnetcore-jwt-1/)

*   Routing to controller actions in ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/mvc/controllers/routing?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/mvc/controllers/routing?view=aspnetcore-7.0)

*   Publish an ASP.NET Core web API to Azure API Management with Visual Studio

[https://learn.microsoft.com/en-us/aspnet/core/tutorials/publish-to-azure-api-management-using-vs?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/tutorials/publish-to-azure-api-management-using-vs?view=aspnetcore-7.0)

# [CHAPTER 4gRPC Service](#contents.xhtml_ch04a)

[Introduction](#contents.xhtml_sc2_86a)

In the last chapter, we discussed exposing data and functionality as services specifically using Web Application Programming Interface (API) which depends upon Hypertext Transfer Protocol (HTTP) as the medium of communication. The focus of this chapter is gRPC services which are also APIs but instead of HTTP, they use remote procedure calls for their communication. We will understand the concepts around gRPC services and then build a real-life API.

[Structure](#contents.xhtml_sc2_87a)

*   Overview of gRPC
    *   What is gRPC?
    *   How does gRPC work?
    *   Features of gRPC
    *   gRPC versus other service models
    *   Advantages of gRPC
    *   Disadvantages of gRPC
    *   gRPC use cases
*   Pre-requisites
*   Getting started with ASP.NET Core gRPC Service
    *   Structure of the (default) gRPC Service project
    *   Consuming the gRPC Greeter Service
    *   Test Greeter Service using Postman
    *   Enable browser access through JSON Transcoding
    *   Enable Swagger documentation
*   Developing gRPC Service
    *   Creating gRPC Service and the client
        *   Getting started
        *   Create proto file
        *   Include the sample data set
        *   Install and configure CsvHelper NuGet package
        *   Create the EmployeesDataService
        *   Create the GrpcDownloadClient
    *   Unit testing
    *   Deployment

[Objectives](#contents.xhtml_sc2_88a)

The objective of this chapter is to understand how ASP.NET Core gRPC Service stack up against other options to build services. As we proceed, we will develop an understanding of the important concepts around gRPC services and see how to develop them in Visual Studio 2022 using C# 11 and .NET 7.0.

[Overview of gRPC](#contents.xhtml_sc2_89a)

Before working with gRPC, let us first understand what this technology is and how it works. gRPC was originally created by Google but later it was open-sourced. From 2017, it is maintained by the Cloud Native Computing Foundation (CNCF) as an incubation project. This means the project has healthy number of contributors and is being used in production applications. If you are guessing, g in gRPC does not stand for Google, it is a recursive acronym like GNU (GNU's Not Unix), Curl URL Request Library (cURL) and many more. So, the acronym gRPC stands for gRPC Remote Procedure Calls.

[What is gRPC?](#contents.xhtml_sc3_90a)

gRPC is an open-source, scalable, high-performance framework for building remote procedure call (RPC) APIs. It relies on HTTP/2 using the Protocol Buffers (protobuf) as Interface Definition Language (IDL), to store data and service contracts in the form of a .proto file. There is support for a variety of programming languages, including C#, C++, Dart, Go, Java, JavaScript, Objective-C, PHP, Python and Ruby. gRPC is designed to be efficient, and lightweight, and it supports both unary (one request, one response) and streaming (multiple requests and responses) communication patterns. It can be used for a wide range of applications, including microservices, cloud-native applications, and IoT devices. Some popular applications that use gRPC include Kubernetes, Netflix, Square, CockroachDB, OpenAI, Spotify and Dropbox to name a few.

[How does gRPC work?](#contents.xhtml_sc3_91a)

In gRPC, the flow of communication between a client and a server follows the RPC pattern. The general flow looks as shown in [Figure 4.1](#ch04.xhtml_fig4-1):

![](images/Figure_4.1.png)

Figure 4.1: Communication flow in gRPC

Like RPC systems, gRPC defines services specifying methods that can be invoked remotely. The gRPC server implements the interfaces and listens to client requests. On the client side, a stub provides the same methods as available on server. On receiving the users’ request on client side, a remote out-of-process call is made to the service, under the covers. The response generated on the server side is communicated back to the client. Developers code in their native platform, gRPC does the plumbing work by handling communication, serialization, and execution between computers.

gRPC services and messages are defined in protocol buffer .proto files. Protocol buffers provide a language and platform neutral, extensible mechanism for serializing structured data. The protobuf compiler, protoc, generates the language specific client and server code at build time. This generated code includes loading the message into memory and serialize/deserialize the binary message.

![](images/Figure_4.2.png)

Figure 4.2: Working of Protocol Buffer [1](#ch04.xhtml_footnote-006)

* * *

[1](#ch04.xhtml_footnote-006-backlink) Source: [https://protobuf.dev/overview/](https://protobuf.dev/overview/)

Protocol buffers assumes that entire messages can be loaded into memory at once. If the data exceeds few megabytes and speed is critical (such as for scientific and engineering applications using large, multi-dimensional arrays of floating-point numbers), a different solution should be considered.

[Features of gRPC](#contents.xhtml_sc3_92a)

Some key features of gRPC service are as follows:

*   Interface Definition Language (IDL): gRPC uses an IDL to describe the service and the messages that are available for invocation in a .proto file. This file is used to generate the client and server code in multiple supported languages.
*   Protocol buffers: gRPC uses Protocol Buffers (or protobuf) as the data serialization format for the request and response messages. It is lightweight and can support complex data structures. The latest version being proto3.
*   gRPC protocol: gRPC uses the gRPC protocol, which is based on the HTTP/2 standard which brings many advanced capabilities as compared to HTTP/1.1\. This protocol provides features such as request/response multiplexing, flow control, bi-directional streaming, and header compression. This allows for efficient communication between the client and the server, reducing network overhead and latency.
*   Transport Layer Security (TLS): gRPC supports TLS, which is used for secure communication between the client and the server. This provides encryption for the data being sent over the network, and also verifies the identity of the client and server.
*   Bi-directional streaming: gRPC supports bi-directional streaming, which allows for real-time, low-latency communication between the client and the server. This is useful for cases where the communication is a two-way street and both client and server can be sending and receiving messages at the same time, such as a chat server. 
*   Cross-language compatibility: gRPC supports multiple programming languages, which makes it easy to write and maintain code across different languages and platforms.

[gRPC versus other service models](#contents.xhtml_sc4_93a)

How is gRPC different from other service-based technologies? The [Table 4.1](#ch04.xhtml_tab4-1) compares gRPC with Web API and WCF. Microsoft recommends migrating the Windows Communication Foundation (WCF) based projects to gRPC, as .NET Core does not offer WCF:

|  | gRPC | Web API | WCF |
| Protocol | gRPC uses the gRPC protocol, which is based on the HTTP/2 standard and provides features such as flow control, bi-directional streaming, and flow-level compression | Web API, on the other hand, uses the HTTP protocol and is based on the REST architectural pattern, which uses standard HTTP methods such as GET, POST, PUT and DELETE. | WCF, on the other hand, uses a variety of transport protocols, such as HTTP, TCP, and MSMQ, depending on the configuration. |
| Data serialization | gRPC uses Protocol Buffers for data serialization, which is efficient and lightweight. | Web API uses a variety of data serialization formats, such as JSON and XML, depending on the configuration and the client's request. | WCF uses the XML format for data serialization, which can be more verbose and less efficient. |
| Language support | gRPC supports a variety of programming languages, including C#, C++, Java, Python, and Go. | Web API can be used with a variety of programming languages and frameworks, such as .NET and Java. | WCF is primarily designed for use with the .NET Framework and is primarily used with C# and VB.NET. |
| Streaming | gRPC supports both unary (one request, one response) and streaming (multiple requests and responses) communication patterns. | Web API supports request-response and one-way messaging patterns, but it does not have built-in support for streaming. | WCF supports request-response and one-way messaging patterns, but it does not have built-in support for streaming. |
| Platform support | gRPC is cross-platform, and it can run on Windows, Linux, and macOS. | Web API can run on any platform that supports the language and framework it is built with, such as .NET and Java. It can be hosted on a variety of web servers, including Internet Information Services (IIS) and Apache. | WCF is primarily designed for use with the .NET Framework, and it can be hosted on a variety of platforms, including IIS and Windows Process Activation Service (WAS), but it is not cross-platform, and it is used on Windows. |

Table 4.1: Comparison of gRPC with Web API and WCF

[Advantages of gRPC](#contents.xhtml_sc3_94a)

gRPC offers several advantages as listed as follows:

*   Performance: gRPC offer better performance as compared to REST+JSON communication because of the use of protobuf and HTTP/2\. Protobuf serializes the messages on both server and client sides resulting in compact message payloads. HTTP/2 scales up the performance via multiplexing, server push, and header compression.
*   Streaming: gRPC makes implementation of both client-side and server-side simple. A gRPC service supports different streaming combinations through HTTP/2 as depicted in [Figure 4.3](#ch04.xhtml_fig4-3):

![](images/Figure_4.3.png)

Figure 4.3: Streaming scenarios supported by gRPC

*   Code generation: gRPC framework uses protoc compiler to generate native code from the .proto file. This produces server-side skeletons and client-side stubs, which saves development time in applications with diverse services.
*   Interoperability: gRPC tools and libraries are designed to work with multiple platforms and programming languages, including Java, JavaScript, Ruby, Python, Go, Dart, Objective-C, C#, and more.
*   Security: The use of HTTP/2 over the TLS end-to-end encrypted connection in gRPC ensures API security.

[Disadvantages of gRPC](#contents.xhtml_sc3_95a)

gRPC does have following disadvantages:

*   Limited browser support: It is not possible to invoke a gRPC service directly from a web browser as gRPC communication uses binary serialization and is based on HTTP/2 and browsers today do not provide sufficient API to control HTTP2 frames from JavaScript. A proxy layer along with gRPC-web is required to perform conversions between HTTP/1.1 and HTTP/2\. Another option is to use gRPC JSON transcoding which allows browser apps to call gRPC services as if they were RESTful APIs with JSON.
*   Non-human readable format: Protobuf compresses gRPC messages into a binary format. So, for debugging purposes additional tools are needed to analyze Protobuf messages and to write manual requests.

[gRPC use cases](#contents.xhtml_sc3_96a)

Some of the use cases where gRPC based communication is useful are as follows:

*   gRPC-based communication is suitable when synchronous communication between microservices is required. A representative architecture that uses gRPC for internal communication between microservices is given in [Figure 4.4](#ch04.xhtml_fig4-4).

![](images/Figure_4.4.png)

Figure 4.4: Using gRPC for internal communication between microservices [2](#ch04.xhtml_footnote-005)

* * *

[2](#ch04.xhtml_footnote-005-backlink)  Source:  [https://learn.microsoft.com/en-us/dotnet/architecture/cloud-native/grpc#grpc-implementation](https://learn.microsoft.com/en-us/dotnet/architecture/cloud-native/grpc#grpc-implementation)

*   Since gRPC supports different programming platforms so it is useful in polyglot environments where multiple languages may be at play.
*   gRPC shines in scenarios which require low latency and high throughput communication where performance is critical.
*   It supports uses-cases requiring point-to-point real-time communication including bi-directional streaming.
*   Since gRPC works on binary message, it is useful in bandwidth constrained environments.

[Pre-requisites](#contents.xhtml_sc2_97a)

Visual Studio 2022 Community Edition or higher preferably with the latest updates is needed to work through the examples in this chapter. Also required is the ASP.NET and web development workload to work with the gRPC services. The Postman API testing tool is used to test the gRPC service, it can be downloaded from [https://www.postman.com/downloads/](https://www.postman.com/downloads/) and used after a free sign-up.

[Getting started with ASP.NET Core gRPC Service](#contents.xhtml_sc2_98a)

Create a new ASP.NET Core gRPC Service project by following the steps below in Visual Studio 2022 as shown in [Table 4.2](#ch04.xhtml_tab4-2):

| New project creation (File &#124; New &#124; Project…) |
|  
1.  Create a new project

 |  
1.  Narrow down the list of templates being shown by selecting, Language: C#, Platform: All platforms, Project type: Service
2.  Select template: ASP.NET Core gRPC Service
3.  Click Next.

 |
|  
*   B. Configure your new project

 |  
4.  Project name: Enter name of your choice such as FirstGrpcService
5.  Location: Select location of choice
6.  Solution: Select either Add to solution  or Create new solution
7.  Solution name: Provide name in case a new solution is created
8.  Place solution and project in the same directory: Normally, we keep the solution a level higher so leave it unchecked in case a new solution is created.
9.  Click Next.

 |
|  
*   C. Additional information

 |  
7.  Framework: .NET 7.0 (Standard Term Support)
8.  Enabled Docker: Unchecked
9.  Docker OS: Applicable if above is checked.
10.  Do not use top-level statement: Unchecked
11.  Click Create.

 |

Table 4.2: Steps to create a new ASP.NET Core gRPC Service project

This creates a new gRPC Service project. The new project can be created using dotnet command line interface (CLI) with following command:

dotnet new  grpc --name FirstGrpcService

And to add the newly created project to the solution use:

dotnet sln  add ./FirstGrpcService/FirstGrpcService.csproj

[Structure of the (default) gRPC Service project](#contents.xhtml_sc3_99a)

On creating the new application using the built-in ASP.NET Core gRPC Service template a sample Greeter service is created. Following files and folders have purpose like any other ASP.NET Core Web App or Web API:

*   Connected Services
*   Dependencies | Analyzers
*   Dependencies | Frameworks
*   Dependencies | Packages
*   Properties | launchSettings.json
*   appsettings.json
*   Project file - *.csproj
*   Solution files - .sln and .suo file

By default, there is dependency on the package Grpc.AspNetCore besides this, let us go over the changes which are unique to ASP.NET Core gRPC application.

Protos/greet.proto

1.  syntax = "proto3";

3.  option csharp_namespace = "FirstGrpcService";

5.  package  greet;

7.  // The greeting service definition.
8.  service  Greeter {
9.  // Sends a greeting
10.  rpc  SayHello (HelloRequest) returns (HelloReply);
11.  }

13.  // The request message containing the user's name.
14.  message  HelloRequest {
15.  string name = 1;
16.  }

18.  // The response message containing the greetings.
19.  message  HelloReply {
20.  string message = 1;
21.  }

Protocol buffers file describes the messages and services in .proto files. Line 1 in the preceding code includes the version of Protobuf. Version 3 being the latest one. Line 3 defines the namespace for the generated code. The package is used as the namespace (after converting to Pascal Case), unless option csharp_namespace is provided, so in this case line 5 is not applicable. Line 8 describes the service and remaining are the messages on line 14 and 19 exchanged between client and server.

Services/GreeterService.cs

1.  using Grpc.Core;

3.  namespace FirstGrpcService.Services;
4.  public  class  GreeterService : Greeter.GreeterBase
5.  {
6.  private  readonly  ILogger<GreeterService> _logger;
7.  public  GreeterService(ILogger<GreeterService> logger)
8.  {
9.  _logger = logger;
10.  }

12.  public  override  Task<HelloReply> SayHello(HelloRequest  request, ServerCallContext  context)
13.  {
14.  return  Task.FromResult(new  HelloReply
15.  {
16.  Message = "Hello " + request.Name
17.  });
18.  }
19.  }

The protobuf compiler (for C#) generates a .cs file from each .proto file, with a class for each message type described in your file. The generated classes are referred in the preceding GreeterService. On line 4, GreeterService inherits from Greeter.GreeterBase defined in GreetGrpc.cs and HelloRequest and HelloReply are defined in Greet.cs.

Program.cs

1.  using FirstGrpcService.Services;

3.  var  builder = WebApplication.CreateBuilder(args);

5.  // Additional configuration is required to successfully run gRPC on macOS.
6.  // For instructions on how to configure Kestrel and gRPC clients on macOS, visit https://go.microsoft.com/fwlink/?linkid=2099682

8.  // Add services to the container.
9.  builder.Services.AddGrpc();

11.  var  app = builder.Build();

13.  // Configure the HTTP request pipeline.
14.  app.MapGrpcService<GreeterService>();
15.  app.MapGet("/", () => "Communication with gRPC endpoints must be made through a gRPC client. To learn how to create a client, visit: https://go.microsoft.com/fwlink/?linkid=2086909");

17.  app.Run();

The HTTP request pipeline is initialized and configured on line 9 and 14 during application start up.

A protobuf ItemGroup entry is created in the FirstGrpcService.csproj file as follows:

1.  <ItemGroup>
2.  <Protobuf  Include="Protos\greet.proto"  GrpcServices="Server" />
3.  </ItemGroup>

The GrpcServices attribute controls the assets that are generated during compilation.

[Consuming the gRPC Greeter Service](#contents.xhtml_sc3_100a)

So far, we have created a service, we need to use it in a client program. Let us first try executing the project. Set the project as the start-up project and then select Debug | Start Debugging or F5 to launch the UI in [Figure 4.5](#ch04.xhtml_fig4-5).

![](images/Figure_4.5.png)

Figure 4.5: Kestrel server hosting the gRPC service

Unlike a Web API, where saw the Swagger UI for the endpoints, in this case no other UI is launched. Copying the URL from the preceding UI and trying to navigate in a browser, shows as [Figure 4.6](#ch04.xhtml_fig4-6).

![](images/Figure_4.6.png)

Figure 4.6: Unable to navigate to gRPC endpoint in browser

As we can see, attempting to navigate to a gRPC service URL in a browser does not work. We would expect a hello message from the Greeter service but instead we are seeing the preceding message. This message is in fact coming from the HTTP request pipeline that we had configured in Program.cs. The reason is, gRPC uses a binary protocol over HTTP/2 for communication between clients and servers. The protocol is not designed to be used in a browser to support the binary format used by gRPC. Additionally, gRPC uses a different method of communication than the request-response model used by HTTP, which is not compatible with the way browsers navigate URLs. Therefore, we need to create a custom client application to consume our gRPC Greeter service.

Create a new console application project by following the steps in the [Table 4.3](#ch04.xhtml_tab4-3) in Visual Studio 2022.

| New project creation (File &#124; New &#124; Project…) |
|  
1.  Create a new project

 |  
1.  Narrow down the list of templates being shown by selecting, Language: C#, Platform: All platforms, Project type: Console
2.  Select template: Console App
3.  Click Next.

 |
|  
*   B. Configure your new project

 |  
4.  Project name: Enter name of your choice such as FirstGrpcServiceTestClient
5.  Location: Select location of choice
6.  Solution: Select either Add to solution or Create new solution
7.  Solution name: Provide name in case a new solution is created
8.  Place solution and project in the same directory: Normally we keep the solution a level higher so leave it unchecked in case a new solution is created.
9.  Click Next

 |
|  
*   C. Additional information

 |  
10.  Framework: .NET 7.0 (Standard Term Support)
11.  Do not use top-level statement: Unchecked
12.  Click Create

 |

Table 4.3: Creating a new Console application project

Install following NuGet packages to the newly created console application.

*   Google.Protobuf by Google Inc
*   Grpc.NET.Client by The gRPC Authors
*   Grpc.Tools by The gRPC Authors

Copy the /Protos folder (along with greet.proto file) from the FirstGrpcService project into FirstGrpcServiceTestClient project. Adjust the namespace in the newly copied file greet.proto to following:

option csharp_namespace = "FirstGrpcServiceTestClient";

Double-click the FirstGrpcServiceTestClient project to open the FirstGrpcService TestClient.csproj file for editing. Add an item group with a <Protobuf> element that refers to the greet.proto file in the project file as follows:

1.  <ItemGroup>
2.  <Protobuf  Include="Protos\greet.proto"  GrpcServices="Client" />
3.  </ItemGroup>

The project should appear as in [Figure 4.7](#ch04.xhtml_fig4-7) in solution explorer after all the preceding changes.

![](images/Figure_4.7.png)

Figure 4.7: Test client project in solution explorer

Build the project. The tooling package Grpc.Tools generates the following files based on the contents of greet.proto file under .\FirstGrpcServiceTestClient\obj\Debug\net7.0\Protos folder.

*   Greet.cs containing protocol buffer generated C# code which populates, serializes, deserializes and retrieves the request and response messages.
*   GreetGrpc.cs contains the generated code to invoke the service methods.

Include the following code in the Program.cs file in FirstGrpcServiceTestClient project.

1.  using FirstGrpcServiceTestClient;
2.  using Grpc.NET.Client;

4.  // The port number must match the port of the gRPC server.
5.  using  var  channel = GrpcChannel.ForAddress("https://localhost:7208");
6.  var  client = new  Greeter.GreeterClient(channel);
7.  var  reply = await client.SayHelloAsync(
8.  new  HelloRequest { Name = "GreeterClient" });
9.  Console.WriteLine("Greeting: " + reply.Message);
10.  Console.WriteLine("Press any key to exit...");
11.  Console.ReadKey();

On line 5, we instantiate a GrpcChannel containing the information for creating the connection to the gRPC service. The GrpcChannel is used to create the Greeter client on line 6\. The asynchronous SayHello method is invoked from the Greeter client, and the result of the call is displayed. Right clicking the SayHelloAsync method and choosing Go To Implementation in Visual Studio reveals the code generated in GreetGrpc.cs as shown in [Figure 4.8](#ch04.xhtml_fig4-8).

![](images/Figure_4.8.png)

Figure 4.8: Code generated in GreetGrpc.cs by Grpc.Tools

Similarly, for HelloRequest on line 8 shows the code in Greet.cs as shown in [Figure 4.9](#ch04.xhtml_fig4-9):

![](images/Figure_4.9.png)

Figure 4.9: Code generated in Greet.cs by Grpc.Tools

To see the program in action, we need to run both the projects — server and client. Run the gRPC server project FirstGrpcService by right-clicking in Solution Explorer in Visual Studio and choose Debug | Start Without Debugging. Do the same for the client project FirstGrpcServiceTestClient to see the execution happen successfully with the output in [Figure 4.10](#ch04.xhtml_fig4-10):

![](images/Figure_4.10.png)

Figure 4.10: GRPC test client

[Test Greeter Service using Postman](#contents.xhtml_sc3_101a)

Postman is a popular platform to design, develop and test APIs. It added support for testing gRPC requests with version 9.7.1 released in January, 2022\. We will test the Greeter service using Postman.

For Postman to test the API, it must be made aware of the service definition of the API including the information about the service methods exposed, their request parameters and the response types. This can be done in two ways, importing the .proto file or exposing server reflection. We will see how to expose the server reflection for Greeter service. To do this, add the NuGet package Grpc.AspNetCore.Server.Reflection by The gRPC Authors to the project FirstGrpcService. Include highlighted lines of code in Program.cs as follows:

1.  builder.Services.AddGrpc();

2.  builder.Services.AddGrpcReflection();

4.  var  app = builder.Build();

6.  app.MapGrpcReflectionService();

Run the FirstGrpcService. Now start Postman and open the new request dialog as shown in [Figure 4.11](#ch04.xhtml_fig4-11) and choose gRPC request:

![](images/Figure_4.11.png)

Figure 4.11: Create new request dialog in Postman

The gRPC interface on Postman looks as shown in [Figure 4.12](#ch04.xhtml_fig4-12):

![](images/Figure_4.12.png)

Figure 4.12: gRPC request interface in Postman[3](#ch04.xhtml_footnote-004)

* * *

[3](#ch04.xhtml_footnote-004-backlink) Source: [https://learning.postman.com/docs/sending-requests/grpc/grpc-request-interface/](https://learning.postman.com/docs/sending-requests/grpc/grpc-request-interface/)

Enter the server URL of the Greeter service and click on the TLS toggle button. Select the method Server Reflection and select the SayHello method that gets revealed. When in the Message tab, click on Generate Example Message followed by clicking on Invoke button. The response message is generated as shown in [Figure 4.13](#ch04.xhtml_fig4-13):

![](images/Figure_4.13.png)

Figure 4.13: Testing Greeter service in Postman

[Enable browser access through JSON Transcoding](#contents.xhtml_sc3_102a)

gRPC which is based on HTTP/2 is not accessible using a browser over HTTP/1.1 but we can enable the browser access by using JSON transcoding. Here, we will enable the browser access for Greeter service. Install the NuGet package Microsoft.AspNetCore.Grpc.JsonTranscoding by Microsoft in the project FirstGrpcService. In the Program.cs modify the following line:

builder.Services.AddGrpc().AddJsonTranscoding();

Include the two proto files, annotations.proto and http.proto from GitHub repository folder [https://github.com/googleapis/googleapis/tree/master/google/api](https://github.com/googleapis/googleapis/tree/master/google/api) within the folder google/api in the project.

Modify the greet.proto with highlighted changes.

1.  syntax = "proto3";

2.  import  "google/api/annotations.proto";

3.  option csharp_namespace = "FirstGrpcService";

5.  package  greet;

7.  // The greeting service definition.
8.  service  Greeter {
9.  // Sends a greeting

10.  rpc  SayHello (HelloRequest) returns (HelloReply)
11.  {
12.  option (google.api.http) =
13.  {
14.  get: "/Greeter/{name}"
15.  };

17.  };

18.  }

20.  // The request message containing the user's name.
21.  message  HelloRequest {
22.  string name = 1;
23.  }

25.  // The response message containing the greetings.
26.  message  HelloReply {
27.  string message = 1;
28.  }

Running the FirstGrpcService project and navigating to the URL shows the response in browser as in the [Figure 4.14](#ch04.xhtml_fig4-14).

![](images/Figure_4.14.png)

Figure 4.14: Navigate to gRPC endpoint in browser after JSON transcoding

[Enable Swagger documentation](#contents.xhtml_sc3_103a)

To enable the Open API (Swagger) documentation for the Greeter API, add the NuGet package Microsoft.AspNetCore.Grpc.Swagger by Microsoft and include the highlighted changes in Program.cs to enable the Swagger middleware:

1.  using FirstGrpcService.Services;

3.  var  builder = WebApplication.CreateBuilder(args);

5.  // Add services to the container.
6.  builder.Services.AddGrpc().AddJsonTranscoding();
7.  builder.Services.AddGrpcReflection();

9.  builder.Services.AddGrpcSwagger();
10.  builder.Services.AddSwaggerGen();

12.  var  app = builder.Build();

14.  if (app.Environment.IsDevelopment())
15.  {
16.  app.UseSwagger();
17.  app.UseSwaggerUI();
18.  }

20.  app.MapGrpcReflectionService();

22.  // Configure the HTTP request pipeline.
23.  app.MapGrpcService<GreeterService>();
24.  app.MapGet("/", () => "Communication with gRPC endpoints must be made through a gRPC client. To learn how to create a client, visit: https://go.microsoft.com/fwlink/?linkid=2086909");

26.  app.Run();

The completed FirstGrpcService project looks as in [Figure 4.15](#ch04.xhtml_fig4-15) in Solution Explorer.

![](images/Figure_4.15.png)

Figure 4.15: Completed FirstGrpcService project

With these changes, navigating to the /Swagger endpoint shows up as in [Figure 4.16](#ch04.xhtml_fig4-16) and there is an option to try the Greeter API.

![](images/Figure_4.16.png)

Figure 4.16: Swagger enabled gRPC endpoint

[Developing gRPC Service](#contents.xhtml_sc2_104a)

As part of developing a real life gRPC Service, we will create a GrpcDownloadService which will use server streaming to download a large file on to the requesting client. We will use a CSV file, 265 MB in size and having around 1 million records from [https://excelbianalytics.com/wp/wp-content/uploads/2020/09/Hr1m.zip](https://excelbianalytics.com/wp/wp-content/uploads/2020/09/Hr1m.zip). Client initiates the download, and the response stream will be written record-by-record on the server side and show up on the client side.

[Creating gRPC Service and the Client](#contents.xhtml_sc3_105a)

By the end of this section, a gRPC service shall be ready which will download a large file on the client through service method call using server streaming. The records will show up on the client application as in [Figure 4.17](#ch04.xhtml_fig4-17).

![](images/Figure_4.17.png)

Figure 4.17: gRPC client getting records via server streaming

[Getting started](#contents.xhtml_sc4_106a)

Create a Asp.NET Core gRPC Service named GrpcDownloadService choosing all the default options as described for the FirstGrpcService application earlier. Set the project as the start-up project in the solution and delete the automatically generated files /Protos/greet.proto and /Services/GreeterService.cs. Delete the following line from Program.cs and ensure that the project builds successfully.

app.MapGrpcService<GreeterService>();

[Create proto file](#contents.xhtml_sc4_107a)

Create a protocol buffer file /Protos/employees.proto by right clicking the Protos folder and choosing Add | New Item as shown in [Figure 4.18](#ch04.xhtml_fig4-18):

![](images/Figure_4.18.png)

Figure 4.18: Dialog to add new proto file

Describe the EmployeeService, EmpRequest and EmpResponse in the employees.proto file as follows:

1.  syntax = "proto3";
2.  import  “google/protobuf/timestamp.proto”;
3.  option csharp_namespace = "GrpcDownloadService.Protos";

5.  service  EmployeesService {
6.  rpc  GetEmployeesData(EmpRequest) returns (stream  EmpResponse) {}
7.  }

9.  message  EmpRequest{
10.  }

12.  message  EmpResponse {
13.  int32 EmpID = 1;
14.  string FirstName = 2;
15.  string LastName = 3;
16.  float Age = 4;
17.  google.protobuf.Timestamp DateOfJoining = 5;
18.  float LastHike = 6;
19.  }

Notice in the GetEmployeeData method on line 6, the EmpReponse parameter is qualified with stream, indicating that the method will be used in the server streaming mode. EmpResponse defines some of the fields present in the CSV file that we plan to download.

Include the following in the GrpcDownloadService project file:

1.  <ItemGroup>
2.  <Protobuf  Include="Protos\employees.proto"  GrpcServices="Server" />
3.  </ItemGroup>

Build the project. This should auto-generate Employees.cs and EmployeesGrpc.cs files under .\obj\Debug\net7.0\Protos folder.

[Include the sample data set](#contents.xhtml_sc4_108a)

Download the open-source Human Resources sample dataset file from [https://excelbianalytics.com/wp/wp-content/uploads/2020/09/Hr1m.zip](https://excelbianalytics.com/wp/wp-content/uploads/2020/09/Hr1m.zip). Unzip and add to the project under Data folder. The downloaded CSV file contains the headers in the first row followed by one or more data rows as shown in [Table 4.4](#ch04.xhtml_tab4-4).

| Header | Emp ID,Name Prefix,First Name,Middle Initial,Last Name,Gender,E Mail,Father's Name,Mother's Name,Mother's Maiden Name,Date of Birth,Time of Birth,Age in Yrs.,Weight in Kgs.,Date of Joining,Quarter of Joining,Half of Joining,Year of Joining,Month of Joining,Month Name of Joining,Short Month,Day of Joining,DOW of Joining,Short DOW,Age in Company (Years),Salary,Last % Hike,SSN,Phone No. ,Place Name,County,City,State,Zip,Region,User Name,Password |
| Row | 677509,Drs.,Lois,H,Walker,F,[lois.walker@hotmail.com](mailto:lois.walker@hotmail.com),DonaldWalker,Helen Walker, Lewis, 3/29/1981,02:31:49 AM,36.36,60,11/24/2003,Q4,H2,2003,11,November,Nov,24,Monday,Mon,13.68,168251,21%,467-99-4677,303-572-8492,Denver,Denver,Denver,CO,80224,West,lhwalker,DCa}.T}X:v?NP |

Table 4.4: Sample dataset

[Install and configure CsvHelper NuGet package](#contents.xhtml_sc4_109a)

To parse the CSV file in our service, install the open-source NuGet package CsvHelper by Josh Close. Create a new class file /CsvMaps/EmpMap.cs with following contents:

1.  using CsvHelper;
2.  using CsvHelper.Configuration;
3.  using GrpcDownloadService.Protos;
4.  using System.Globalization;

6.  namespace MyDownloadService.CsvMaps;

8.  public  class  EmpMap : ClassMap<EmpResponse>
9.  {
10.  ///  <summary>
11.  /// Map CSV columns with EmpResponse class properties
12.  ///  </summary>
13.  public  EmpMap()
14.  {
15.  Map(m => m.EmpID).Name("Emp ID");
16.  Map(m => m.FirstName).Name("First Name");
17.  Map(m => m.LastName).Name("Last Name");
18.  Map(m => m.Age).Name("Age in Yrs.");
19.  Map(m => m.DateOfJoining).Name("Date of Joining").TypeConverter<TimeStampConverter>();
20.  Map(m => m.LastHike).Name("Last % Hike").TypeConverter<PercentConverter>();
21.  }

23.  ///  <summary>
24.  /// Convert DateTime into Google.Protobuf.WellKnownTypes.Timestamp
25.  ///  </summary>
26.  private  class  TimeStampConverter : CsvHelper.TypeConversion.DateTimeConverter
27.  {
28.  public  override  object? ConvertFromString(string? text, IReaderRow  row, MemberMapData  memberMapData)
29.  {
30.  DateTime  date = DateTime.Parse(text, CultureInfo.GetCultureInfo("en-US"));
31.  date = DateTime.SpecifyKind(date, DateTimeKind.Utc);
32.  return Google.Protobuf.WellKnownTypes.Timestamp.FromDateTime(date);
33.  }
34.  }

36.  ///  <summary>
37.  /// Parse percentage string value such as "21%" into float 0.21
38.  ///  </summary>
39.  private  class  PercentConverter : CsvHelper.TypeConversion.DoubleConverter
40.  {
41.  public  override  object? ConvertFromString(string? text, IReaderRow  row, MemberMapData  memberMapData)
42.  {
43.  text = text.Replace(CultureInfo.CurrentCulture.NumberFormat.PercentSymbol, "");
44.  return  float.Parse(text) / 100;
45.  }
46.  }
47.  }

This class helps in setting up the CsvHelper to correctly parse the CSV file on the server. The EmpResponse properties are mapped to the CSV columns in the EmpMap constructor between lines 13 and 21\. TimeStampConverter and PercentConverter are custom converters needed to parse the specific fields.

[Create the EmployeesDataService](#contents.xhtml_sc4_110a)

We need to now create service method which will read the CSV file on server side and write to the response stream. Create the class /Services/EmployeesDataService.cs with following content:

1.  using CsvHelper;
2.  using CsvHelper.Configuration;
3.  using Grpc.Core;
4.  using GrpcDownloadService.Protos;
5.  using MyDownloadService.CsvMaps;
6.  using System.Globalization;

8.  namespace GrpcDownloadService.Services;

10.  public  class  EmployeesDataService : EmployeesService.EmployeesServiceBase
11.  {
12.  public  override  async  Task  GetEmployeesData(EmpRequest  request, IServerStreamWriter<EmpResponse> responseStream,
13.  ServerCallContext  context)
14.  {
15.  try
16.  {
17.  //open CSV file
18.  using  var  reader = new  StreamReader(Path.Combine(AppDomain.
    CurrentDomain.BaseDirectory, "Data", "Hr1m.csv"));

20.  //configure CsvHelper
21.  var  csvConfig = new  CsvConfiguration(CultureInfo.InvariantCulture)
22.  {
23.  HeaderValidated = null  //Not throw error for unmapped columns
24.  };
25.  using  var  csv = new  CsvReader(reader, csvConfig);
26.  csv.Context.RegisterClassMap<EmpMap>(); //map

28.  //Parse CSV and read all records
29.  var  records = csv.GetRecordsAsync<EmpResponse>();

31.  //copy records into response stream
32.  var  enumerator = records.GetAsyncEnumerator();
33.  while (!context.CancellationToken.IsCancellationRequested && await enumerator.MoveNextAsync())
34.  _ = responseStream.WriteAsync(enumerator.Current);

36.  }
37.  catch (Exception  ex)
38.  {
39.  throw  new  RpcException(new  Status(StatusCode.Internal, ex.ToString()));
40.  }
41.  }
42.  }

The EmployeesDataService.GetEmployeesData method is the implementation of the EmployeesService.GetEmployeesData method declared in the employees.proto file. This method reads the CSV file (line 18) and parses the content into a list of EmpResponse records (line 21 to 29). On line 33, we are iterating through each record and writing the records one by one to the output response stream (line 34). The while loop condition using the property IsCancellationRequested allows for cancelling the write operation.

Include the following line in Program.cs to wire the gRPC service during application start up:

app.MapGrpcService<EmployeesDataService>();

The GrpcDownloadService is ready and shows up as in the [Figure 4.19](#ch04.xhtml_fig4-19) in solution explorer:

![](images/Figure_4.19.png)

Figure 4.19: GrpcDownloadService project

We need to now create the client application to consume this service.

[Create the GrpcDownloadClient](#contents.xhtml_sc4_111a)

Create a new console application GrpcDownloadClient, the way we created FirstGrpcService TestClient. Install following NuGet packages to the newly created console application.

*   Google.Protobuf by Google Inc
*   Grpc.NET.Client by The gRPC Authors
*   Grpc.Tools by The gRPC Authors

Copy the /Protos folder (along with employees.proto file) from the GrpcDownloadService project into GrpcDownloadClient project. Adjust the namespace in the newly copied file employees.proto to the following:

option csharp_namespace = "  GrpcDownloadClient.Protos";

Double-click the GrpcDownloadClient project to open the GrpcDownloadClient.csproj file for editing. Add an item group with a <Protobuf> element that points to the employees.proto file in the project file as follows:

1.  <ItemGroup>
2.  <Protobuf  Include="Protos\employees.proto"  GrpcServices="Client" />
3.  </ItemGroup>

At this stage, the project should compile successfully and the files Employees.cs and EmployeesGrpc.cs should be auto generated under .\obj\Debug\net7.0\Protos folder.

To invoke the service method to download and view the contents of the CSV file, include following code in Program.cs:

1.  using Grpc.Core;
2.  using Grpc.NET.Client;
3.  using GrpcDownloadClient.Protos;

5.  int  Count = 0;
6.  var  watch = System.Diagnostics.Stopwatch.StartNew();
7.  try
8.  {
9.  var  channel = GrpcChannel.ForAddress(“https://localhost:7181”);
10.  var  empClient = new  EmployeesService.EmployeesServiceClient(channel);

12.  using  var  empCall = empClient.GetEmployeesData(new  EmpRequest(), deadline: DateTime.UtcNow.AddMinutes(10));

14.  await  foreach (var emp  in empCall.ResponseStream.ReadAllAsync())
15.  {
16.  Count++;
17.  Console.WriteLine($"#{Count}|Id: {emp.EmpID}|{emp.FirstName} {emp.LastName}({emp.Age} yrs)|DOJ: {emp.DateOfJoining.ToDateTime():MMM dd, yyyy}|Last Hike: {emp.LastHike * 100}%");
18.  }
19.  }
20.  catch (RpcException  ex) when (ex.StatusCode == StatusCode.DeadlineExceeded)
21.  {
22.  Console.WriteLine("Service timeout.");
23.  }

25.  watch.Stop();

27.  Console.WriteLine($"\nServer stream finished. Fetched {Count} records in {watch.Elapsed.TotalSeconds:F} sec.");
28.  Console.Read();

In the preceding code, we are instantiating the EmployeesServiceClient on line 10, over the channel pointing to the server address. This client object (stub) is then used to invoke the GetEmployeesData service method on server side (line 12). The ResponseStream which is written-to in real time on the server side, between lines 14 and 18, is being read for each employee record and displayed on the console on the client side.

To see the program in action, we need to run both the projects — server and client. Run the gRPC server project GrpcDownloadService by right-clicking in Solution Explorer in Visual Studio and choose Debug | Start Without Debugging. Do the same for the client project GrpcDownloadClient to see the execution happen successfully and view the contents of the CSV file in the client application as read from gRPC server via server streaming.

[Unit testing](#contents.xhtml_sc3_112a)

For unit-testing gRPC services, we focus on writing tests to verify only gRPC service, everything else such as dependencies, infrastructure, routing, authentication is mocked. To test, create a new MSTest Test Project named GrpcDownloadService.Test. Rename the unit test file UnitTest1.cs file to EmployeesDataServiceTests.cs and click on Yes to the prompt asking to rename all references. Add a dependency to the project being tested, that is, GrpcDownloadService. Download two helper files, TestServerCallContext.cs and TestServerStreamWriter.cs, from GitHub from the folder [https://github.com/grpc/grpc-dotnet/tree/master/examples/Tester/Tests/Server/UnitTests/Helpers](https://github.com/grpc/grpc-dotnet/tree/master/examples/Tester/Tests/Server/UnitTests/Helpers) and add to Helper folder. The project would like as in the [Figure 4.20](#ch04.xhtml_fig4-20) in the Solution Explorer:

![](images/Figure_4.20.png)

Figure 4.20: GrpcDownloadService.Test project

Add the following code to EmployeesDataServiceTests.cs:

1.  using GrpcDownloadService.Protos;
2.  using GrpcDownloadService.Services;
3.  using GrpcDownloadService.Test.Helpers;

5.  namespace GrpcDownloadService.Test;

7.  [TestClass]
8.  public  class  EmployeesDataServiceTests
9.  {
10.  [TestMethod]
11.  public  async  Task  GetEmployeesDataTest()
12.  {
13.  // Arrange
14.  var  service = new  EmployeesDataService();
15.  var  cts = new  CancellationTokenSource();
16.  cts.CancelAfter(5000); //cancel (long running) operation after 5 sec

18.  var  callContext = TestServerCallContext.
    Create(cancellationToken: cts.Token);
19.  var  responseStream = new  TestServerStreamWriter<EmpResponse>(callContext);
20.  using  var  taskGetEmployeesDataCall = service.GetEmployeesData(new  EmpRequest(), responseStream, callContext);

22.  // Act
23.  await taskGetEmployeesDataCall;
24.  responseStream.Complete();

26.  var  employees = new  List<EmpResponse>();
27.  await  foreach (var emp  in responseStream.ReadAllAsync())
28.  employees.Add(emp);

30.  // Assert
31.  Assert.IsTrue(taskGetEmployeesDataCall.IsCompletedSuccessfully);
32.  Assert.IsTrue(employees.Count >= 1);
33.  }
34.  }

In the preceding snippet, the test method GetEmployeesDataTest follows the Arrange-Act-Assert pattern. In the Arrange section, we are setting up for invoking the method being tested i.e., GrpcDownloadService.Services.EmployeesDataService.GetEmployeesData. Service is instantiated on line 14 and the parameters for GetEmployeesData method are prepared from lines 15 to 20\. The call context and the response stream are initialized using the helper classes TestServerCallContext and TestServerStreamWriter. In the Act section, the asynchronous call is made to the GetEmployeesData (line 23). This is a time-consuming operation however it will be cancelled after 5 seconds (line 16) with fewer records written to the response stream. After the operation is cancelled, we must mark the response stream as Complete followed by reading the employee list from the stream. Finally in the Assert section, we verify that the operation completed successfully (line 31) and that there is at least one employee record in the response stream (line 32).

[Deployment](#contents.xhtml_sc3_113a)

Microsoft has recently built support for hosting gRPC services on Azure App Service for Linux workloads. To deploy a gRPC app on App Service please follow the tutorial [https://github.com/Azure/app-service-linux-docs/blob/master/HowTo/gRPC/use_gRPC_with_dotnet.md](https://github.com/Azure/app-service-linux-docs/blob/master/HowTo/gRPC/use_gRPC_with_dotnet.md).

[Conclusion](#contents.xhtml_sc2_114a)

In conclusion, ASP.NET Core gRPC Services provide a powerful and efficient communication framework for modern applications. gRPC based communication offers several benefits such as high-performance, language-agnostic communication, and automatic code generation. This chapter has provided an overview of gRPC, explained its distinguishing features, and showcased how to create simple gRPC services using ASP.NET Core and Visual Studio 2022.

In the next chapter, we will focus on exploring Blazor based applications.

[Points to remember](#contents.xhtml_sc2_115a)

*   ASP.NET Core provides a framework to develop remote procedure call APIs accessible over gRPC.
*   gRPC is a language-independent framework where client and server agree on messages and service contracts defined in .proto files. Knowing the service contracts allows a client to invoke the services over the network, the basic plumbing work of transporting the requests, parameters and the responses is handled by the gRPC protocol.
*   As gRPC services are based on HTTP/2 protocol and use a binary streaming approach driven by Protocol Buffer, they score in performance. Refer to [http://www.http2demo.io/](http://www.http2demo.io/) for a demo of HTTP/2.
*   gRPC supports unidirectional and bi-directional streaming of data between a server and client.
*   gRPC services is suited for internal microservices communication where performance may be a key.

[Exercises](#contents.xhtml_sc2_116a)

Create a DownloadService similar to GrpcDownloadService created in this chapter with following requirements:

*   Download the sample CSV dataset having 1 million bank transactions records from [https://excelbianalytics.com/wp/downloads-20-sample-csv-files-data-sets-for-testing-till-2-million-records-bank-transactions/](https://excelbianalytics.com/wp/downloads-20-sample-csv-files-data-sets-for-testing-till-2-million-records-bank-transactions/)

[Tip: Before moving ahead with the dataset having 1 million records, you may want to write the program with the smallest dataset having 100 records.]

*   Create a suitable proto file in the service project having request, response and service definitions corresponding to the fields and their data types for banking transaction record.
*   Create CSV mapping file to parse the dataset using CsvHelper.
*   Create the service with a method that reads the CSV file on the server and writes to the response stream record by record.

[Hint: This will be quite similar to the code created for EmployeesDataService]

*   Finally, create a client console application on the lines of GrpcDownloadClient which invokes the service method and displays the bank Transaction records.
*   Use Postman to test the newly created GrpcDownloadService.

[References](#contents.xhtml_sc2_117a)

*   Overview for gRPC on .NET

[https://learn.microsoft.com/en-us/aspnet/core/grpc/?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/grpc/?view=aspnetcore-7.0)

*   Introduction to gRPC

[https://grpc.io/docs/what-is-grpc/introduction/](https://grpc.io/docs/what-is-grpc/introduction/)

*   What is gRPC? Meaning, Architecture, Advantages

[https://www.wallarm.com/what/the-concept-of-grpc](https://www.wallarm.com/what/the-concept-of-grpc)

*   ASP.NET Core gRPC for WCF Developers

[https://learn.microsoft.com/en-us/dotnet/architecture/grpc-for-wcf-developers/](https://learn.microsoft.com/en-us/dotnet/architecture/grpc-for-wcf-developers/)

*   Compare gRPC services with HTTP APIs

[https://learn.microsoft.com/en-us/aspnet/core/grpc/comparison?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/grpc/comparison?view=aspnetcore-7.0)

*   gRPC Tools

[https://github.com/grpc-ecosystem/awesome-grpc#tools](https://github.com/grpc-ecosystem/awesome-grpc#tools)

*   Overview | Protocol Buffers Documentation

[https://protobuf.dev/overview/](https://protobuf.dev/overview/)

*   Protocol Buffer Basics: C#

[https://protobuf.dev/getting-started/csharptutorial/](https://protobuf.dev/getting-started/csharptutorial/)

*   C# Generated Code Guide

[https://protobuf.dev/reference/csharp/csharp-generated/](https://protobuf.dev/reference/csharp/csharp-generated/)

*   Build High Performance Services using gRPC and .NET7

[https://medium.com/geekculture/build-high-performance-services-using-grpc-and-net7-7c0c434abbb0](https://medium.com/geekculture/build-high-performance-services-using-grpc-and-net7-7c0c434abbb0)

*   gRPC for ASP.NET Core at NDC Sydney, Nov 2019

[https://youtu.be/JpM95-Wplzo](https://youtu.be/JpM95-Wplzo)

*   Test gRPC services in ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/grpc/test-services?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/grpc/test-services?view=aspnetcore-7.0)

*   Postman Now Supports gRPC

[https://blog.postman.com/postman-now-supports-grpc/](https://blog.postman.com/postman-now-supports-grpc/)

# [CHAPTER 5Blazor WebAssembly](#contents.xhtml_ch05a)

[Introduction](#contents.xhtml_sc2_118a)

Continuing with different ways to develop web applications in .NET, in this chapter, we will explore Blazor—a relatively newer open-source web framework developed by Microsoft. It started as an experimental project in 2018 and was officially released in May 2021. Blazor allows the building of interactive web applications using .NET, HTML, and CSS. However, unlike most web applications, instead of using JavaScript, C# is used to write code that runs in the browser. The word Blazor is a combination of browser and Razor. Let us dive in!

[Structure](#contents.xhtml_sc2_119a)

The chapter will cover the following topics:

*   Introduction to Blazor
    *   Types of Blazor Apps
        *   Blazor Server
        *   Blazor WebAssembly
        *   Blazor WebAssembly Hosted
        *   Blazor WebAssembly Progressive Web App (PWA)
        *   Blazor Hybrid
*   Pre-requisites
*   Getting started with Blazor WebAssembly App
    *   Structure of the (default) Blazor WebAssembly project
*   Developing Blazor WebAssembly (Hosted) App
    *   Creating Blazor WebAssembly Client and Server
        *   Getting started
        *   Create the Index page
        *   Create variation one – You Guess
        *   Create variation two – Computer Guesses
        *   Save Game Log
        *   Create UI to view Game Log
    *   Unit testing
        *   Unit-testing using bUnit.
        *   End-to-end testing using Playwright .NET
    *   Deployment

[Objectives](#contents.xhtml_sc2_120a)

The objective of this chapter is to understand how to use Blazor to develop interactive web applications. As we proceed, we will examine the concepts around the app development framework of Blazor and the different types of applications that can be built in Visual Studio 2022 using C# 11 and .NET 7.0.

[Introduction to Blazor](#contents.xhtml_sc2_121a)

Blazor is an open-source and cross-platform web UI framework for building Single-Page Applications (SPAs) using .NET and C# instead of JavaScript on both server and client side. This becomes possible by compiling C# code into WebAssembly (WASM).

WASM is a low-level, bytecode, and assembly-like language designed to run natively in the browser. It was designed to execute efficient modern browser-based apps at high-performance levels without compromising compatibility or security. The ability to compile a high-level language such as C, C++, C#, and Rust into WebAssembly has huge implications for the web platform—it provides a way to run code written in multiple languages on the web at near-native speed, with client apps running on the web that previously could not have done so.

![](images/Figure_5.1.png)

Figure 5.1: Compiling C# code into WebAssembly

The initial version of WebAssembly was launched in 2017 as an open standard created and maintained by W3C, Mozilla, Microsoft, Google, and Apple. It is also widely supported by major browsers like Chrome, Edge, Firefox, Safari, and Opera but not IE 11.

[Types of Blazor Apps](#contents.xhtml_sc3_122a)

Blazor Apps are composed of one or more Razor components. These components are independent pieces of code such as a page, dialog, or form which combine Razor, HTML, CSS, and C# code together in a .razor file. They can be reused and shared between projects. Components use a render tree to represent the Document Object Model (DOM) in memory, helping in updating the UI in a flexible and efficient way. Blazor supports primarily two models to host the components – Blazor Server and Blazor WebAssembly

[Blazor Server](#contents.xhtml_sc4_123a)

With the Blazor Server hosting model, the app is executed on the server from within an ASP.NET Core app that hosts the Razor components. UI updates, event handling, and JavaScript calls are handled in real-time over a SignalR connection using the WebSockets protocol. The bulk of the processing load is on the server.

![](images/Figure_5.2.png)

Figure 5.2: Working of Blazor Server application[1](#ch05.xhtml_footnote-003)

* * *

[1](#ch05.xhtml_footnote-003-backlink) Source: [https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-5.0#blazor-server](https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-5.0#blazor-server)

This is somewhat like the Razor Pages web app that we saw in the chapter on ASP.NET Core Web App. However, there is a difference in the way elements are rendered.

A Razor Pages web app emits pure HTML, and after rendering, the page instance and any state information is destroyed. When a new request is received, the entire page is re-rendered and sent over to the client.

Blazor Server produces a component graph, which is the binary representation of the page markup, including the state and properties of all the UI elements, and is sent over to the client. On the client-side, whenever a UI interaction occurs, the component graph is re-rendered on the server. A diff containing the minimum set of DOM edits required to update the UI is produced and sent over to the client and applied by the browser. The component is disposed of after the user navigates away from the component.

[Blazor WebAssembly](#contents.xhtml_sc4_124a)

Blazor WebAssembly is a client-side hosting model for executing a Blazor app. When a user navigates to a Blazor WebAssembly app in their web browser, the browser downloads the app's resources and .NET runtime. The app then runs on the client's browser and can interact with the browser's APIs, such as the DOM, to update the user interface. The app can also make API calls to a server-side backend if necessary. The UI updates are handled locally, which means that the app can work offline or with a poor network connection. This also enables a faster response time because the app does not need to communicate with the server to handle UI updates. Since the app is self-contained, it can be easily distributed and deployed. The app can be hosted on a variety of hosting platforms, such as static website hosting, a content delivery network (CDN), or a storage service like AWS S3, Azure static web apps or Blob Storage, and so on.

![](images/Figure_5.3.png)

Figure 5.3: Working of Blazor WebAssembly application[2](#ch05.xhtml_footnote-002)

* * *

[2](#ch05.xhtml_footnote-002-backlink) Source: [https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-7.0#blazor-webassembly](https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-7.0#blazor-webassembly)

Thus, Blazor WebAssembly allows developers to create fast, responsive, and offline-capable web apps while still leveraging the full capabilities of the web browser.

[Blazor WebAssembly Hosted](#contents.xhtml_sc4_125a)

In this variation, a Blazor WebAssembly app is hosted within an ASP.NET Core app. The ASP.NET Core app serves as the host for the Blazor WebAssembly app and provides it with additional services such as authentication, authorization, and API calls. The Blazor WebAssembly app runs on the client's browser and can interact with the browser's APIs, such as the DOM, to update the user interface. The app can also make API calls to a server-side backend if necessary. When a user navigates to a Blazor WebAssembly Hosted app in their web browser, the browser first communicates with the host ASP.NET Core app. The ASP.NET Core app then serves the Blazor WebAssembly app as a static file to the browser. The browser then downloads the app's resources and .NET runtime, just like in a standalone Blazor WebAssembly app.

[Blazor WebAssembly Progressive Web App (PWA)](#contents.xhtml_sc4_126a)

This variation of a Blazor WebAssembly app is built to work offline and be installable on a user's device, just like a native mobile app. Progressive Web App (PWAs) are web apps that can be added to the home screen of a user's device, receive push notifications, and work offline. To enable offline functionality, the app uses a caching mechanism called a Service Worker. A Service Worker is a script that runs in the background and allows the app to cache resources and handle requests even when the user is offline. This means that once the user has visited the app and it has been cached, they can still access it and use it even if they lose their internet connection. Additionally, the app can be installed on the user's device, which means that it can be launched like a native app without the need for a browser. This allows for a more seamless user experience and can improve the app's performance. It is also possible to convert an existing Blazor WebAssembly application into a PWA.

[Blazor Hybrid](#contents.xhtml_sc4_127a)

In a Blazor Hybrid app, Razor components are rendered on BlazorWebView control specific for the device through .NET MAUI, WPF, or Windows Forms. Razor components load and execute code quickly, and components have full access to the native capabilities of the device through the .NET platform. We will examine this in more detail in a later chapter.

![](images/Figure_5.4.png)

Figure 5.4: Razor components working within Web View control in Blazor Hybrid app[3](#ch05.xhtml_footnote-001)

* * *

[3](#ch05.xhtml_footnote-001-backlink) Source: [https://learn.microsoft.com/en-us/training/modules/build-blazor-hybrid/2-understand-blazor-hybrid](https://learn.microsoft.com/en-us/training/modules/build-blazor-hybrid/2-understand-blazor-hybrid)

[Pre-requisites](#contents.xhtml_sc2_128a)

Visual Studio 2022 Community Edition or higher, preferably with the latest updates, is needed to work through the examples in this chapter. Also required is the ASP.NET and web development workload to work with the different types of Blazor applications, along with .NET WebAssembly build tools optional component.

Getting started with Blazor WebAssembly App

Create a new Blazor WebAssembly App project by following the steps below in Visual Studio 2022:

| New project creation (File &#124; New &#124; Project…) |
|  
1.  Create a new project

 |  
1.  Narrow down the list of templates being shown by selecting Language: C#, Platform: All platforms, Project type: Blazor
2.  Select template: Blazor WebAssembly App
3.  Click Next

 |
|  
*   B. Configure your new project

 |  
4.  Project name: Enter the name of your choice, such as FirstBlazorWasmApp
5.  Location: Select location of choice
6.  Solution: Select either Add to solution or Create new solution
7.  Solution name: Provide name in case a new solution is created
8.  Place solution and project in the same directory: Normally we keep the solution a level higher so leave it unchecked in case a new solution is created.
9.  Click Next

 |
|  
*   C. Additional information

 |  
10.  Framework: .NET 7.0 (Standard Term Support)
11.  Authentication type: None
12.  Configure for HTTPS: Checked
13.  ASP.NET Core Hosted: Unchecked
14.  Progressive Web Application: Unchecked
15.  Do not use top-level statement: Unchecked
16.  Click Create

 |

Table 5.1: Steps to create a new Blazor WebAssembly App

This creates a new gRPC Service project. The above steps can be performed by using dotnet command line interface (CLI) also. The corresponding command is as follows:

dotnet new  blazorwasm --name FirstBlazorWasmApp

To add the newly created project to the solution following command should be run from CLI

dotnet sln  add ./FirstBlazorWasmApp/FirstBlazorWasmApp.csproj

[Structure of the (default) Blazor WebAssembly project](#contents.xhtml_sc3_129a)

On creating the new application using the built-in Blazor WebAssembly template some sample Razor components are created. Let us examine the folder and the files that are unique in this project type:

| Dependencies &#124; Frameworks | By default there is a dependency on Microsoft.NETCore.App. |
| Dependencies &#124; Packages | There is a dependency on two NuGet packages - Microsoft.AspNetCore.Components.WebAssembly and Microsoft.AspNetCore.Components.WebAssembly.DevServer |
| wwwroot/ | This folder contains the static resources in the web project such as CSS, and images. The sample-data folder contains the weather.json file having the weather data in JSON format. The index.html webpage is the root page of the app implemented as an HTML page. The component is rendered at the location of the div DOM element with an ID of app. |
| Pages/ | This folder contains the Razor components in the project with .razor file extension. FetchData.razor component that demonstrates loading data from weather.json file, Counter.razor that has code for user interaction incrementing value of a counter and Index.razor that implements the home page. |
| Shared/ | Here we have common Razor components such as layout re-used by other components. MainLayout.razor is the component for app's layout with associated stylesheet MainLayout.razor.css. NavMenu.razor implements sidebar navigation including the NavLink to render navigation links on other Razor components. The associated stylesheet is NavMenu.razor.css.  SurveyPrompt.razor is demonstration of shared survey component. |
| _import.razor | Includes @using directives for namespaces common to all the Razor directives in the app's components. |
| App.razor | This is the root component of the app that sets up client-side routing using the Router component which displays the page that matches the requested address by intercepting the browser navigation. |
| Program.cs | This is the entry point for the application and sets up the WebAssembly host. Like other web applications, it is here that the request handling pipeline is configured as a series of middleware components and the services required by the app. |

Table 5.2: Important files and folders in the default Blazor WebAssembly project

To understand the structure of a razor component let us examine the code of the components added in this default project – Counter and FetchData as follows:

Counter.razor

1.  @page "/counter"

3.  <PageTitle>Counter</PageTitle>

5.  <h1>Counter</h1>

7.  <p  role="status">Current count: @currentCount</p>

9.  <button  class="btn btn-primary" @onclick="IncrementCount">Click me</button>

11.  @code {
12.  private  int currentCount = 0;

14.  private  void  IncrementCount()
15.  {
16.  currentCount++;
17.  }
18.  }

The @page directive, on line 1, is special markup that identifies a component as a page and specify a route. We are displaying the value of the variable currentCount on line 7\. On line 9 the onclick event for the button invokes the C# method IncrementCount declared within the @code{} block. So, effectively we are increasing the value of the currentCount variable on every click of the button and displaying it. The Counter page appears as follows:

![](images/Figure_5.5.png)

Figure 5.5: Counter page

FetchData.razor

1.  @page "/fetchdata"
2.  @inject HttpClient  Http

4.  <PageTitle>Weather forecast</PageTitle>

6.  <h1>Weather forecast</h1>

8.  <p>This component demonstrates fetching data from the server.</p>

10.  @if (forecasts == null)
11.  {
12.  <p><em>Loading...</em></p>
13.  }
14.  else
15.  {
16.  <table  class="table">
17.  <thead>
18.  <tr>
19.  <th>Date</th>
20.  <th>Temp. (C)</th>
21.  <th>Temp. (F)</th>
22.  <th>Summary</th>
23.  </tr>
24.  </thead>
25.  <tbody>
26.  @foreach (var  forecast  in forecasts)
27.  {
28.  <tr>
29.  <td>@forecast.Date.ToShortDateString()</td>
30.  <td>@forecast.TemperatureC</td>
31.  <td>@forecast.TemperatureF</td>
32.  <td>@forecast.Summary</td>
33.  </tr>
34.  }
35.  </tbody>
36.  </table>
37.  }

39.  @code {
40.  private  WeatherForecast[]? forecasts;

42.  protected  override  async  Task  OnInitializedAsync()
43.  {
44.  forecasts = await Http.GetFromJsonAsync<WeatherForecast[]>("sample-data/weather.json");
45.  }

47.  public  class  WeatherForecast
48.  {
49.  public  DateOnly Date { get; set; }

51.  public  int TemperatureC { get; set; }

53.  public  string? Summary { get; set; }

55.  public  int  TemperatureF => 32 + (int)(TemperatureC / 0.5556);
56.  }
57.  }

The preceding code is an example to fetch and display data. Line 1 declares the route for the component. Line 2 injects the HttpClient which is later used in the code block on line 44 to fetch the weather data from a static JSON file. The page shows up as follows:

![](images/Figure_5.6.png)

Figure 5.6: Fetch data page

[Developing Blazor WebAssembly (Hosted) App](#contents.xhtml_sc2_130a)

For demonstrating the development of a real-life application, we will create a simulation for the game of Cows and Bulls.

Cows and bulls is a codebreaking, pen and paper game played between two players. It is a numerical version of the board game Mastermind or the popular word game Wordle. In this, opponents aim to decipher other's secret code by trial and error based on the clues given as the number of cows and bulls. A digit is a cow if it is present in the code but is not at its correct position and a bull if it is present at the correct position also. We will create two variations, of this game one where we need to break the code that computer has randomly selected and in the other computer tries to decipher the code that a human opponent has thought.

Like before, we will start with the Blazor WebAssembly App template but this time, we will make it ASP.NET Core hosted. The client project will have the main game application and the server part will expose API, which can be invoked from the client, to save the game log in a database.

[Creating Blazor WebAssembly client and server](#contents.xhtml_sc3_131a)

By the end of this section, we would have created three pages including several Razor components and the API to work with the game log in database. The final UI will look as follows:

![](images/Figure_5.7.png)

Figure 5.7: Final UI - Home page

The UI for the variation of the game where the human opponent has to guess the number that the computer thinks randomly is as follows:

![](images/Figure_5.8.png)

Figure 5.8: Final UI – Game variation one

Refer to the [Figure 5.9](#ch05.xhtml_fig5-9) for the variation where human opponent thinks of the number and the computer tries to decipher.

![](images/Figure_5.9.png)

Figure 5.9: Final UI – Game variation two

The game log appears as follows:

![](images/Figure_5.10.png)

Figure 5.10: Final UI - Game log

[Getting started with Blazor WebAssembly App](#contents.xhtml_sc4_132a)

Create a new project named CowsAndBulls using the Blazor WebAssembly App template choosing all the default options as described for the FirstBlazorWasmApp application earlier. The only difference is the value of the option ASP.NET Core Hosted on the Additional Information dialog will be set as Checked. Doing so creates three projects - CowsAndBulls.Client, CowsAndBulls.Server and CowsAndBulls.Shared. Make following changes in the three projects to remove the default functionality.

CowsAndBulls.Client

*   Delete pages - Counter.razor, FetchData.razor
*   Delete shared component - SurveyPrompt.razor
*   Remove the menu items corresponding to Counter and Fetch Data pages from NavMenu.razor

CowsAndBulls.Server

*   Delete the WeatherForecastController.cs controller.

CowsAndBulls.Shared

*   Delete the WeatherForecast.cs class file.

After these changes, the client project appears as follows in Solution Explorer:

![](images/Figure_5.11.png)

Figure 5.11: The client CowsAndBulls project – intial version

The server project shows up as follows:

![](images/Figure_5.12.png)

Figure 5.12: The server CowsAndBulls project - initial version

And the initial version of the shared CowsAndBulls project is depicted in the following figure:

![](images/Figure_5.13.png)

Figure 5.13: The shared CowsAndBulls project - inital version

Set the CowsAndBulls.Server project as the start-up project and run the project to ensure everything is compiling fine.

[Create the Index page](#contents.xhtml_sc4_133a)

Replace the content of /Pages/Index.razor with following code:

1.  @page "/"

3.  <PageTitle>The Game of Cows and Bulls</PageTitle>

5.  <h1>The Game of Cows and Bulls</h1>

7.  <p>
8.  This is simulation of a pen and paper game that can be played between two players.
9.  One player thinks of a 4-digit number having all different digits.
10.  The other player has to guess that, based on the clues &ndash; the number of <i>cows</i> and <i>bulls</i>.
11.  A digit is a <i>Cow</i> when it is present but not at its correct position,
12.  and a <i>Bull</i> when it is present at its correct position also (remember <i>Bulls Eye</i>).
13.  Here, the two players are you and the computer!
14.  </p>
15.  <p>
16.  Suppose a player thinks of 1729 as the 4-digit number then the playing trail can possibly go as follows:
17.  </p>

19.  <table  class="table">
20.  <thead>
21.  <tr>
22.  <th>Attempt#</th>
23.  <th>Guess</th>
24.  <th>Cows</th>
25.  <th>Bulls</th>
26.  </tr>
27.  </thead>
28.  <tbody>
29.  <tr>
30.  <td>1</td>
31.  <td>1023</td>
32.  <td>0</td>
33.  <td>2 (1, 2)</td>
34.  </tr>
35.  <tr>
36.  <td>2</td>
37.  <td>1045</td>
38.  <td>0</td>
39.  <td>1 (1)</td>
40.  </tr>
41.  <tr>
42.  <td>3</td>
43.  <td>1067</td>
44.  <td>1 (7)</td>
45.  <td>1 (1)</td>
46.  </tr>
47.  <tr>
48.  <td>4</td>
49.  <td>8923</td>
50.  <td>1 (9)</td>
51.  <td>1 (2)</td>
52.  </tr>
53.  <tr>
54.  <td>5</td>
55.  <td>1708</td>
56.  <td>0</td>
57.  <td>2 (1, 7)</td>
58.  </tr>
59.  <tr>
60.  <td>6</td>
61.  <td>1729</td>
62.  <td>0</td>
63.  <td>4 (1, 7, 2, 9)</td>
64.  </tr>
65.  </tbody>
66.  </table>

[Create variation one – You Guess](#contents.xhtml_sc4_134a)

Create a new model class Attempt.cs in CowsAndBulls.Shared with following code:

1.  namespace CowsAndBulls.Shared;
2.  public  class  Attempt
3.  {
4.  public  string? Guess { get; set; }
5.  public  int Cows { get; set; }
6.  public  int Bulls { get; set; }
7.  }

Create a static Helpers.cs class in CowsAndBulls.Shared with following code. This class will contain the common methods for invoking from other classes.

1.  namespace CowsAndBulls.Shared;
2.  public  static  class  Helpers
3.  {
4.  ///  <summary>
5.  /// Generates a numeric code string not starting with 0 and with non-repeating digits
6.  ///  </summary>
7.  ///  <param  name="length"></param>
8.  ///  <returns></returns>
9.  public  static  string? GetRandomCode(int  length = 4)
10.  {
11.  string? code = null;

13.  var  digits = new  List<string> { "0","1","2","3","4","5","6","7","8","9" };

15.  for (var  i = 0; i < length; i++)
16.  {
17.  //generate random number between 0 and count of unused digits
18.  var  randomIndexRandom = new  Random().Next(i == 0 ? 1 : 0, digits.Count - 1);
19.  code += digits[randomIndexRandom];
20.  digits.RemoveAt(randomIndexRandom); //remove the digit since it is used
21.  }

23.  return code;
24.  }

26.  ///  <summary>
27.  /// Compares the code with guessed code and finds the number of cows and bulls
28.  ///  </summary>
29.  ///  <param  name="code"></param>
30.  ///  <param  name="guess"></param>
31.  ///  <returns></returns>
32.  public  static  Attempt  GetCowsAndBulls(string? code, string? guess)
33.  {
34.  var  cows = 0;
35.  var  bulls = 0;

37.  if (code != null && guess != null && code.Length == guess.Length)
38.  {
39.  for (var  i = 0; i < code.Length; i++)
40.  {
41.  for (var  j = 0; j < guess.Length; j++)
42.  {
43.  if (code[i] == guess[j])
44.  {
45.  if (i == j)
46.  bulls++; //increment count of bulls if the position also matches
47.  else
48.  cows++; //increment count of cows if the position does not match
49.  }
50.  }
51.  }
52.  }

54.  return  new  Attempt { Guess = guess, Bulls = bulls, Cows = cows };
55.  }
56.  }

Create a new razor component named PlayTrail.razor under Pages folder with following code:

1.  @using CowsAndBulls.Shared;
2.  <hr  />
3.  <table  class="table">
4.  <thead>
5.  <tr>
6.  <th>Attempt#</th>
7.  <th>Guess</th>
8.  <th>Cows</th>
9.  <th>Bulls</th>
10.  </tr>
11.  </thead>
12.  <tbody>
13.  @{
14.  int  c = 0;
15.  }
16.  @foreach (var  p  in Play)
17.  {
18.  c++;
19.  <tr>
20.  <td>@c</td>
21.  <td>@p.Guess</td>
22.  <td>@p.Cows</td>
23.  <td>@p.Bulls</td>
24.  </tr>
25.  }
26.  </tbody>
27.  </table>

29.  @code {
30.  [Parameter]
31.  public  List<Attempt> Play { get; set; } = new();
32.  }

The purpose of the preceding Razor component is to create reusable code to display the playing trail in the form of number being guessed and the corresponding number of cows and bulls. The list of attempts is exposed as parameter for assigning from the calling section. This list of attempts is shown in a tabular form between lines 16 to 25.

Finally, create a new razor component named YouGuess.razor under Pages folder with following code.

1.  @page "/YouGuess"
2.  @using CowsAndBulls.Shared;

4.  <h3>Cows and Bulls - Computer thinks and you guess</h3>
5.  <h5  class="fst-italic text-primary">Computer thinks of a 4-digit number and you find it based on the number of cows and bulls.</h5>

7.  <p>  <button  class="btn btn-primary" @onclick="GenerateCode">Start new game</button>  </p>

9.  <div  class="alert alert-warning"  role="alert"> @message </div>

11.  <hr  />

13.  Guess:
14.  <input @bind="guess"  maxlength="4"  />
15.  <button  class="btn btn-primary" @onclick="GetCowsAndBulls">Input</button>

17.  <PlayTrail  Play="Play" />

19.  @code {
20.  private  string? num;
21.  private  string? guess;
22.  private  List<Attempt> Play = new();
23.  private  string? message = "";

25.  private  void  GenerateCode()
26.  {
27.  num = Helpers.GetRandomCode();
28.  Play = new();
29.  guess = "";
30.  message = "Start guessing...";
31.  }

33.  private  void  GetCowsAndBulls()
34.  {
35.  var  attempt = Helpers.GetCowsAndBulls(num, guess);
36.  Play.Add(attempt);
37.  if (attempt.Bulls == 4)
38.  {
39.  message = "Found the number, well done!";
40.  }
41.  }
42.  }

At the start of the game when the Start new game button is clicked, the bound method GenerateCode is invoked. This generates a random 4-digit number as the secret code on line 27\. When the player guesses a number by entering in the input box and clicking on Input button, the bound method GetCowsAndBulls determines the number of cows and bulls on line 35\. Game is over when the secret code is discovered, that is, when the number of bulls becomes 4 (line 37). Every attempt is saved in the playing trail list on line 36 and this is passed to the PlayTrail component on line 17 for displaying in tabular form.

To have a link to this variation of the game on the website, include following snippet in /Shared/NavMenu.razor below the home page link:

1.  <div  class="nav-item px-3">
2.  <NavLink  class="nav-link"  href="YouGuess">
3.  <span  class="oi oi-list-rich"  aria-hidden="true"></span>  You Guess!
4.  </NavLink>
5.  </div>

The changes are now complete. Running the project, the UI should show up as follows.

![](images/Figure_5.14.png)

Figure 5.14: Variation one - You Guess

[Create variation two – computer guesses](#contents.xhtml_sc4_135a)

Add following supporting methods in Helper.cs in CowsAndBulls.Shared:

1.  ///  <summary>
2.  /// Generates all possible codes i.e. 4 digit numbers having non-repeating digits
3.  ///  </summary>
4.  ///  <returns></returns>
5.  public  static  List<string> GetAllCodes()
6.  {
7.  var  codes = new  List<string>();
8.  for (var  i = 1; i <= 9; i++)
9.  {
10.  for (var  j = 0; j <= 9; j++)
11.  {
12.  if (j == i) continue;
13.  for (var  k = 0; k <= 9; k++)
14.  {
15.  if (k == j || k == i) continue;
16.  for (var  l = 0; l <= 9; l++)
17.  {
18.  if (l == k || l == j || l == i) continue;
19.  codes.Add($"{i}{j}{k}{l}");
20.  }
21.  }
22.  }
23.  }
24.  return codes;
25.  }

27.  ///  <summary>
28.  /// Selects a string randomly from the source list of strings
29.  ///  </summary>
30.  ///  <param  name="source"></param>
31.  ///  <returns></returns>
32.  public  static  string? SelectRandomCode(List<string> source)
33.  {
34.  string? code = null;
35.  if (source != null && source.Any())
36.  code = source.Count == 1 ? source[0] : source[new  Random().Next(0, source.Count - 1)];

38.  return code;
39.  }

41.  ///  <summary>
42.  /// Creates list of possible codes from the source list of codes,
43.  /// which can have the same number of cows of bulls as in the passed attempt.
44.  ///  </summary>
45.  ///  <param  name="source"></param>
46.  ///  <param  name="attempt"></param>
47.  ///  <returns></returns>
48.  public  static  List<string> GetPossibleCodes(List<string> source, Attempt  attempt)
49.  {
50.  var  possibleCodes = new  List<string>();

52.  foreach (var code  in source)
53.  {
54.  var  possibleAttempt = GetCowsAndBulls(code, attempt.Guess);
55.  if (possibleAttempt.Cows == attempt.Cows && possibleAttempt.Bulls == attempt.Bulls)
56.  possibleCodes.Add(code);
57.  }

59.  return possibleCodes;
60.  }

Create a new razor component ComputerGuesses.razor in the CowsAndBulls.Client project under Pages folder with following code:

1.  @page "/ComputerGuesses"
2.  @using CowsAndBulls.Shared;
3.  <h3>Cows and Bulls - You think and computer guesses</h3>
4.  <h5  class="fst-italic text-primary"> Think of a 4-digit number and computer finds it based on the number of cows and bulls.</h5>
5.  <p>  <button  class="btn btn-primary btn-start-new-game" @onclick="GenerateAllCode">Start new game</button>  </p>
6.  <div  class="alert alert-warning log-message"  role="alert"> @message </div>

8.  <hr  />
9.  <p  class="guess">Guess: @guess (Out of @allCodes.Count possibilities)</p>
10.  <p>
11.  Cows: <input @bind="cows"  type="number"  min="0"  max="4"  step="1"  />
12.  Bulls: <input @bind="bulls"  type="number"  min="0"  max="4"  step="1"  />
13.  <button  class="btn btn-primary btn-input" @onclick="InputCowsAndBulls">Input</button>
14.  </p>

16.  <PlayTrail  Play="Play" />

18.  @code {
19.  private  string? guess;
20.  private  int cows;
21.  private  int bulls;
22.  private  List<Attempt> Play = new();
23.  private  List<string> allCodes = new();
24.  private  string? message = "";

26.  private  void  GenerateAllCode()
27.  {
28.  allCodes = Helpers.GetAllCodes();
29.  guess = Helpers.SelectRandomCode(allCodes);
30.  Play = new();
31.  cows = 0;
32.  bulls = 0;
33.  message = "Let us begin...";
34.  }

36.  private  void  InputCowsAndBulls()
37.  {
38.  var  attempt = new  Attempt { Guess = guess, Bulls = bulls, Cows = cows };
39.  Play.Add(attempt);
40.  allCodes = Helpers.GetPossibleCodes(allCodes, attempt);

42.  guess = Helpers.SelectRandomCode(allCodes);
43.  if (allCodes.Count == 0)
44.  message = "Give up! I think you provided incorrect clues, please verify the count of cows and bulls.";
45.  else  if (allCodes.Count == 1)
46.  {
47.  message = "Game over. Found the number!";
48.  }
49.  }
50.  }

At the click of the button Start new game, all the possible 4-digit codes are generated (line 28) followed by selecting a random code out of this list on line 29. When the number of cows and bulls is entered by the user and the Input button is clicked, the bound method InputCowsAndBulls is invoked. The given clue is used to reduce the number of possibilities on line 40 and a random code is selected from the reduced list of possibilities. If only one number is remaining it indicates that the secret code is discovered, and the game is over. In case no possibilities are remaining it implies user has made a mistake in inputting the number of cows and bulls and appropriate message is shown on line 44.

To include a link to this variation of the game on the website, include following snippet in /Shared/NavMenu.razor below the You Guess variation page link.

1.  <div  class="nav-item px-3">
2.  <NavLink  class="nav-link"  href="ComputerGuesses">
3.  <span  class="oi oi-list-rich"  aria-hidden="true"></span> Computer Guesses!
4.  </NavLink>
5.  </div>

The changes are now complete for this variation. Running the project, the UI should show up as follows:

![](images/Figure_5.15.png)

Figure 5.15: Variation two - Computer Guesses

[Save Game Log](#contents.xhtml_sc4_136a)

Blazor WebAssembly apps connect to a database on the server side using a backend web API. The app can make HTTP requests to the API to retrieve or update data in the database.

Suppose we need to save a log message, summarizing the game, in the database. For this we will expose ASP.NET Core Web APIs to perform the Create, Read, Update, and Delete (CRUD) operations in the CowsAndBulls.Server. This API can be invoked from the WASM client CowsAndBulls.Client.

Create the model class GameLog.cs to represent a log entry as follows. This class is created in CowsAndBulls.Shared project so that it can be accessed both from the client and the server projects.

1.  namespace CowsAndBulls.Shared;

3.  public  class  GameLog
4.  {
5.  public  int Id { get; set; }
6.  public  string? Log { get; set; }
7.  }

In CowsAndBulls.Server project right-click on the Controller folder and select Add | New Scaffolded Item… and choose API Controller  with actions, using Entity Framework from the Add New Scaffolded Item dialog. In the following options dialog select GameLog as the Model class and create a new data context as follows:

![](images/Figure_5.16.png)

Figure 5.16: Creating GameLogs controller via New Scaffolded Item

On clicking Add, following changes are made via the scaffolding.

*   NuGet packages Microsoft.EntityFrameworkCore.SqlServer and Microsoft.EntityFrameworkCore.Tools are added.
*   GameLogsController API controller is created with endpoints to perform basic CRUD on GameLog entity.
*   CowsAndBullsServerContext class is created.
*   appsettings.json has the database connection string.
*   Program.cs has a line to create an instance of CowsAndBullsServerContext using the connection string. This helps in injecting the DBContext anywhere in the application such as in the API Controller.

You may run the code clean up on the CowsAndBulls.Server project to remove unnecessary using statements and perform other basic improvements. To create the database, execute following PowerShell commands one after the other, in the Package Manager Console after selecting CowsAndBulls.Server as the default project.

Add-Migration InitialCreate

Update-Database

The changes on the server side are done. Next step is to invoke the API from the client project. To do this, let us create a razor component to help form the log message once a game is over and to display a button, clicking which initiates the API call to save the record in database. Right-click Pages folder in the CowsAndBulls.Client project and add a new razor component named SaveGameLog.razor including the following code in it.

1.  @using CowsAndBulls.Shared;
2.  @inject HttpClient  http

4.  @if (CanSave)
5.  {
6.  <button  class="btn btn-primary" @onclick="SaveGameMessage">Save Game Log</button>
7.  <div  class="alert alert-warning"  role="alert">
8.  @if (Saved)
9.  {
10.  @message
11.  }
12.  </div>
13.  }

15.  @code {
16.  [Parameter]
17.  public  string? WhoGuessed { get; set; }

19.  [Parameter]
20.  public  string? SecretCode { get; set; }

22.  [Parameter]
23.  public  List<Attempt> Play { get; set; } = new();

25.  [Parameter]
26.  public  bool CanSave { get; set; }

28.  [Parameter]
29.  public  bool Saved { get; set; } = false;

31.  private  string message = "";

33.  private  async  Task  SaveGameMessage()
34.  {
35.  if (!Saved)
36.  {
37.  //E.g. Computer guessed 4120 in 6 attempts - 1234,3456,2317,4128,4129,4120.
38.  message = $"[{DateTime.Now.ToString("d-MMM-yyyy HH:mm")}]: {WhoGuessed} guessed {SecretCode} in {Play.Count} attempts - {string.Join(",",  Play.Select(a  =>  a.Guess))}.";

40.  await http.PostAsJsonAsync("api/GameLogs", new  GameLog { Log = message });

42.  Saved = true;
43.  }
44.  }
45.  }

In the preceding snippet the code between lines 4 and 13 ensures that the Save Game Log button is shown only when the flag CanSave is set to true. CanSave and other properties are exposed as parameters in the @code block between lines 16 and 29. The parameter values passed from the calling section are used to form the log message on line 38\. Code on line 40 invokes the API to add the log entry in the database through a HTTP POST call via the HttpClient injected on line 2.

Modify YouGuess.razor to include the highlighted changes for consuming SaveGameLog component as follows.

1.  @page "/YouGuess"
2.  @using CowsAndBulls.Shared;

4.  <h3>Cows and Bulls - Computer thinks and you guess</h3>
5.  <h5  class="fst-italic text-primary">Computer thinks of a 4-digit number and you find it based on the number of cows and bulls.</h5>

7.  <p>  <button  class="btn btn-primary" @onclick="GenerateCode">Start new game</button>  </p>

9.  <div  class="alert alert-warning"  role="alert"> @message </div>

10.  <SaveGameLog  CanSave="canSave"  Play="Play"  SecretCode="@guess"  WhoGuessed="You"  Saved="@false" />

12.  <hr  />

14.  Guess:
15.  <input @bind="guess"  maxlength="4"  />

16.  <button  class="btn btn-primary" @onclick="GetCowsAndBulls"  disabled="@canSave">Input</button>

18.  <PlayTrail  Play="Play" />

20.  @code {
21.  private  string? num;
22.  private  string? guess;
23.  private  List<Attempt> Play = new();
24.  private  string? message = "";

25.  private  bool canSave = false;

27.  private  void  GenerateCode()
28.  {
29.  num = Helpers.GetRandomCode();
30.  Play = new();
31.  guess = "";
32.  message = "Start guessing...";

33.  canSave = false;

34.  }

36.  private  void  GetCowsAndBulls()
37.  {
38.  var  attempt = Helpers.GetCowsAndBulls(num, guess);
39.  Play.Add(attempt);
40.  if (attempt.Bulls == 4)
41.  {
42.  message = "Found the number, well done!";

43.  canSave = true;

44.  }
45.  }
46.  }

Line 10 includes the SaveGameLog component passing the required parameters. The canSave flag declared on line 25, controls the enablement of Input button on line 16 and ensures that the Save button is available only when the game is over on line 43\. The option to save log will appear as follows;

![](images/Figure_5.17.png)

Figure 5.17: Option to save log in You Guess variation

Likewise, modify ComputerGuesses.razor with the highlighted changes including the SaveGameLog as follows:

1.  @page "/ComputerGuesses"
2.  @using CowsAndBulls.Shared;
3.  <h3>Cows and Bulls - You think and computer guesses</h3>
4.  <h5  class="fst-italic text-primary"> Think of a 4-digit number and computer finds it based on the number of cows and bulls.</h5>
5.  <p>  <button  class="btn btn-primary btn-start-new-game" @onclick="GenerateAllCode">Start new game</button>  </p>
6.  <div  class="alert alert-warning log-message"  role="alert"> @message </div>

8.  <SaveGameLog  CanSave="canSave"  Play="Play"  SecretCode="@guess"  WhoGuessed="Computer"  Saved="@false" />

10.  <hr  />
11.  <p  class="guess">Guess: @guess (Out of @allCodes.Count possibilities)</p>
12.  <p>
13.  Cows: <input @bind="cows"  type="number"  min="0"  max="4"  step="1"  />
14.  Bulls: <input @bind="bulls"  type="number"  min="0"  max="4"  step="1"  />

15.  <button  class="btn btn-primary btn-input" @onclick="InputCowsAndBulls"  disabled="@canSave">Input</button>

16.  </p>

18.  <PlayTrail  Play="Play" />

20.  @code {
21.  private  string? guess;
22.  private  int cows;
23.  private  int bulls;
24.  private  List<Attempt> Play = new();
25.  private  List<string> allCodes = new();
26.  private  string? message = "";

27.  private  bool canSave = false;

29.  private  void  GenerateAllCode()
30.  {
31.  allCodes = Helpers.GetAllCodes();
32.  guess = Helpers.SelectRandomCode(allCodes);
33.  Play = new();
34.  cows = 0;
35.  bulls = 0;
36.  message = "Let us begin...";

37.  canSave = false;

38.  }

40.  private  void  InputCowsAndBulls()
41.  {

42.  if (canSave) return;

44.  var  attempt = new  Attempt { Guess = guess, Bulls = bulls, Cows = cows };
45.  Play.Add(attempt);
46.  allCodes = Helpers.GetPossibleCodes(allCodes, attempt);

48.  guess = Helpers.SelectRandomCode(allCodes);
49.  if (allCodes.Count == 0)
50.  message = "Give up! I think you provided incorrect clues, please verify the count of cows and bulls.";
51.  else  if (allCodes.Count == 1)
52.  {
53.  message = "Game over. Found the number!";

54.  canSave = true;

55.  }
56.  }
57.  }

With the preceding changes, the Save Game Log button will appear once the game is over and clicking that saves the message in database. The message appears as follows on the UI:

![](images/Figure_5.18.png)

Figure 5.18: Option to save log in Computer Guesses variation

At this stage we may verify by checking directly in the database. Let us now provide a UI to view the log entries.

[Create UI to view Game Log](#contents.xhtml_sc4_137a)

Create a new razor component in the CowsAndBulls.Client project named ShowGameLog.razor with following code:

1.  @page "/GameLog"
2.  @using CowsAndBulls.Shared;
3.  @inject HttpClient  http

5.  <h3>Game Log</h3>
6.  @if (Logs == null)
7.  {
8.  <text>Loading...</text>
9.  }
10.  else  if (Logs.Length == 0)
11.  {
12.  <text>No Records Found.</text>
13.  }
14.  else
15.  {
16.  <table  class="table table-striped">
17.  <thead>
18.  <tr>
19.  <th>Log (@Logs.Count())</th>
20.  </tr>
21.  </thead>
22.  <tbody>
23.  @foreach (var  logEntry  in Logs)
24.  {
25.  <tr>
26.  <td>@logEntry.Log</td>
27.  </tr>
28.  }
29.  </tbody>
30.  </table>
31.  }
32.  @code {
33.  GameLog[] Logs { get; set; }

35.  protected  override  async  Task  OnInitializedAsync()
36.  {
37.  Logs = await http.GetFromJsonAsync<GameLog[]>("api/GameLogs");
38.  }
39.  }

The preceding code on line 3 uses @inject to inject a preconfigured HttpClient service registered in Program.cs. This HttpClient is used to make a request back to the server of origin. The API call on line 37 invokes GetFromJsonAsync to send a HTTP GET request and parse the JSON response body to create array of Game Log entries. These entries are iterated from lines 23 to 28 to display in an HTML table.

Add following snippet to NavMenu.razor in CowsAndBulls.Client to include a hyperlink for Game Log.

1.  <div  class="nav-item px-3">
2.  <NavLink  class="nav-link"  href="GameLog">
3.  <span  class="oi oi-list-rich"  aria-hidden="true"></span> Game Log
4.  </NavLink>
5.  </div>

The UI appears as follows:

![](images/Figure_5.19.png)

Figure 5.19: Game log UI

[Create reusable Razor Class library](#contents.xhtml_sc4_138a)

Razor class library (RCL) can be used to share razor views, pages, controllers, page models, razor components, view components, and data models across multiple projects. For demonstration, we will create a simple razor class library and make use of a component defined in it and invoke a JavaScript method from it.

Create a new project named ComponentLibrary based on the Razor Class Library template. Add a new Razor component named CustomMessage.razor with following code.

1.  <div  class="custom-message">
2.  @if (!Hide)
3.  {
4.  <div  class="alert alert-warning log-message"  role="alert"> @Message </div>
5.  }
6.  </div>
7.  @code {
8.  [Parameter]
9.  public  string? Message { get; set; }

11.  [Parameter]
12.  public  bool Hide { get; set; } = false;
13.  }

Add a project reference to ComponentLibrary in CowsAndBulls.Client project. And make the following replacement in the two components – YouGuess.razor and ComputerGuesses.razor

| Old | <div  class="alert alert-warning log-message"  role="alert"> @message </div> |
| New | <ComponentLibrary.CustomMessage  Hide="@false"  Message="@message" /> |

The two variations of the game will work fine with this change. Next, we will demonstrate invoking a JavaScript method from ComponentLibrary. Replace the content of /wwwroot/exampleJsInterop.js in ComponentLibrary with following:

1.  export  function showPrompt(message) {
2.  return console.info(message);
3.  }

Make the highlighted change in YouGuess.razor

1.  @page "/YouGuess"

2.  @inject IJSRuntime  JSRuntime
3.  @using ComponentLibrary;

4.  @using CowsAndBulls.Shared;

6.  <h3>Cows and Bulls – Computer thinks and you guess</h3>

7.  <h5  class="fst-italic text-primary">Computer thinks of a 4-digit <span @ondblclick="RevealNumber">number</span> and you find it based on the number of cows and bulls.</h5>

8.  …

And include the following method in the @code block in YouGuess.razor

1.  private  async  void  RevealNumber()
2.  {
3.  await (new  ExampleJsInterop(JSRuntime)).Prompt($"Secret code revealed --> {num}");
4.  }

In the preceding code we are invoking the Prompt method from ExampleJsInterop in ComponentLibrary which in turn is calling the showPrompt JavaScript method in exampleJsInterop.js to write to the console using the injected JSRuntime. Effectively this is a Cheat Code giving away the secret code in the console as shown below:

![](images/Figure_5.20.png)

Figure 5.20: Invoking JavaScript from Razor Class Library

[Unit testing](#contents.xhtml_sc3_139a)

The strategies to test Blazor applications are centered around testing Razor components. Component is rendered, events are triggered followed by asserting for expected results. The two common approaches to testing are unit-testing by mocking external dependencies and end-to-end testing which involves running the Blazor app in a browser instance together with the dependent infrastructure. We will write tests using both the approaches.

[Unit-testing using bUnit](#contents.xhtml_sc4_140a)

Microsoft does not have a testing framework for Blazor. bUnit is a community driven project which helps in unit-testing the Razor components. It works together with general-purpose testing frameworks, such as MSTest, NUnit, and xUnit.

Add a new MS Test project to the solution named CowsAndBulls.Test. Add references to CowsAndBulls.Client and CowsAndBulls.Shared projects. Add NuGet package bUnit by Egil Hansen. Open the project file and set the SDK entry to following:

<Project  Sdk="Microsoft.NET.Sdk.Razor">

Create a new class ComputerGuessesTests.cs in the project with following code.

1.  using Bunit;
2.  using CowsAndBulls.Client.Pages;

4.  namespace CowsAndBulls.Test;

6.  [TestClass]
7.  public  class  ComputerGuessesTests
8.  {
9.  private Bunit.TestContext ctx;

11.  //Component Under Test
12.  private  IRenderedComponent<ComputerGuesses> cut;

14.  [TestInitialize] // Runs before each test.
15.  public  void  Setup()
16.  {
17.  ctx = new Bunit.TestContext();
18.  cut = ctx.RenderComponent<ComputerGuesses>();
19.  }

21.  [TestCleanup] // Runs after each test.
22.  public  void  Cleanup()
23.  {
24.  cut.Dispose();
25.  ctx.Dispose();
26.  }

28.  [TestMethod]
29.  public  void  ComponentRendersCorrectly()
30.  {
31.  //Verify the presence of heading caption
32.  Assert.IsTrue(cut.Markup.Contains("<h3>Cows and Bulls - You think and computer guesses</h3>"));
33.  }

35.  [TestMethod]
36.  public  void  GameBeginsCorrectly()
37.  {
38.  var  buttonStartNewGame = cut.Find("button.btn-start-new-game");
39.  buttonStartNewGame.Click();

41.  //Verify the presence of labels at start of game
42.  Assert.IsTrue(cut.Markup.Contains("Let us begin..."));
43.  Assert.IsTrue(cut.Markup.Contains("Out of 4536 possibilities"));
44.  }

46.  [TestMethod]
47.  public  void  GamePlayedCorrectly()
48.  {
49.  //Input button clicked twice with 0 Cows and 0 Bulls
50.  var  buttonInput = cut.Find("button.btn-input");
51.  buttonInput.Click();
52.  buttonInput.Click();

54.  //Verify the presence of labels in case of error
55.  Assert.IsTrue(cut.Markup.Contains("Give up! I think you provided incorrect clues, please verify the count of cows and bulls."));
56.  Assert.IsTrue(cut.Markup.Contains("Out of 0 possibilities"));
57.  }
58.  }

In the preceding MSTest unit-test, the initialization of Bunit TestContext is happening on line 17 followed by creating an instance of the Computer Guesses component which is the Component Under Test. Since this is happening in the Setup method having the TestInitialize attribute, this code will be run before executing every test. Similarly, the Cleanup method gets invoked, after executing each test, to dispose the TestContext and the RenderComponent objects. In the first test ComponentRendersCorrectly we are verifying that the component renders correctly by checking for the presence of the specific heading on the page on line 32\. In the next unit-test GameBeginsCorrectly we are first getting a reference to the Start new game button and thereafter invoking the Click event of the button on line 39\. This is followed by verifying the presence of expected strings on the page on lines 42 and 43\. In the next test GamePlayedCorrectly we are clicking the Input button twice to simulate the case of inputting zero cows and zero bulls two times. Since this is an impossible case, we are expecting error related messages on lines 55 and 56\.

[End-to-end testing using Playwright .NET](#contents.xhtml_sc4_141a)

Playwright .NET is a tool like Selenium WebDriver for end-to-end automated testing of web applications. Playwright supports all modern rendering engines including Chromium, WebKit, and Firefox and tests on Windows, Linux, and macOS, locally or on CI, headless (that is, browser window will not open during test execution) or headed with native mobile emulation.

Add the NuGet package Microsoft.Playwright.MSTest by Microsoft to the CowsAndBulls.Test project. Build the project and then right-click the project in Solution Explorer and select Open in Terminal (this should be the last but one option in the list) to open PowerShell terminal in Visual Studio in the project folder. Execute following command to install the mandatory browser integration:

pwsh bin/Debug/net7.0/playwright.ps1 install

We are now ready to create the test file. Create a new class file ComputerGuessesE2ETests.cs with the following code.

1.  using Microsoft.Playwright;
2.  using Microsoft.Playwright.MSTest;

4.  namespace CowsAndBulls.Test;

6.  [TestClass]
7.  public  class  ComputerGuessesE2ETests : PageTest
8.  {
9.  private  const  string BaseUrl = "https://localhost:7017"; //point to the correct base url

11.  [TestMethod]
12.  public  async  Task  CanNavigateToHomePage()
13.  {
14.  await Page.GotoAsync(BaseUrl);
15.  await  Expect(Page).ToHaveTitleAsync("The Game of Cows and Bulls");
16.  }

18.  [TestMethod]
19.  public  async  Task  ComputerGuessesTests()
20.  {
21.  await Page.GotoAsync($"{BaseUrl}/ComputerGuesses");
22.  await  Expect(Page).ToHaveTitleAsync("CowsAndBulls");

24.  //Get locators on the page
25.  var  locatorButtonStartNewGame = Page.GetByRole(AriaRole.Button, new() { Name = "Start new game" });
26.  var  locatorButtonInput = Page.GetByRole(AriaRole.Button, new() { Name = "Input" });
27.  var  locatorLogMessage = Page.Locator(".log-message");
28.  var  locatorGuessPara = Page.Locator(".guess");

30.  await locatorButtonStartNewGame.ClickAsync(); //Start new game by clicking on the button

32.  //Expect the labels on the page at the beginning of the game
33.  await  Expect(locatorLogMessage).ToContainTextAsync("Let us begin...");
34.  await  Expect(locatorGuessPara).ToContainTextAsync("Out of 4536 possibilities");

36.  //Click Input button twice i.e. input 0 cows and 0 bulls
37.  await locatorButtonInput.ClickAsync();
38.  await locatorButtonInput.ClickAsync();

40.  //Expect the labels on the page for the error case
41.  await  Expect(locatorLogMessage).ToContainTextAsync("Give up! I think you provided incorrect clues, please verify the count of cows and bulls.");
42.  await  Expect(locatorGuessPara).ToContainTextAsync("Out of 0 possibilities");
43.  }
44.  }

In the test CanNavigateToHomePage we are navigating to the home page and then verifying the title of the page. In the same way in the next test ComputerGuessesTests, on lines 21 and 22, we navigate to the Computer Guesses variation and then verify the title of the page. Between lines 25 and 28 locaters are setup for use in the test later. On line 30 the click event of the Start new game button is invoked followed by verifying the presence of text on lines 33 and 34\. The Input button is clicked twice on lines 37 and 38, this simulates inputting the value of 0 cows and 0 bulls, as this is impossible, we assert the expected text on lines 41 and 42\. To run these tests, first start the website. Right-click on the CowsAndBulls.Server and choose Debug | Start Without Debugging, after this, right-clicking on the test class name ComputerGuessesE2ETests should show the Run tests option and clicking on that should execute both the tests fine.

[Deployment](#contents.xhtml_sc3_142a)

The deployment for the Blazor apps differs slightly based on the type of app whether it is Blazor Server app or Blazor WebAssembly app. To host and deploy Blazor WebAssembly app, please follow the instructions given at [https://learn.microsoft.com/en-us/aspnet/core/blazor/host-and-deploy/webassembly?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/blazor/host-and-deploy/webassembly?view=aspnetcore-7.0)

[Conclusion](#contents.xhtml_sc2_143a)

In this chapter we have learnt what are Blazor applications, and their different types, and we have built a Blazor WebAssembly application end-to-end.

In the next chapter, we will focus on exploring Single Page Applications that use ASP.NET Core and Angular framework.

[Points to remember](#contents.xhtml_sc2_144a)

*   Blazor is a new Razor component-based UI framework for building rich and interactive web applications that was included in .NET Core 3\.
*   The main difference between Blazor and traditional JavaScript framework-based Single Page Applications is that Blazor components are written entirely in C#, and in Razor, JavaScript is not required.
*   There are two types of Blazor applications – Blazor Server and Blazor WebAssembly
*   WebAssembly runs natively on the client browser and it is now possible to compile many high-level languages into WebAssembly.

[Exercises](#contents.xhtml_sc2_145a)

Enhance the Blazor WebAssembly application built in this chapter with the following changes.

*   The game of Cows and Bulls that we have built in this chapter works with a 4-digit secret code, but it can be played with a different number of digits also. Modify the application to build support for 5-digit numbers. Allow the users to specify the number of digits they want to play with.
*   The game log can grow quickly, providing an option to purge records on the game log page. With this option when the users click the new button, all log entries except for the last 5 entries will be purged.

[Hint: Create a new endpoint in CowsAndBulls.Server.GameLogsController to perform the necessary deletion and invoke this API from the button click in the ShowGameLog.razor component.]

*   Create the bUnit based unit-tests for the You Guess variation. Also create Playwright based end-to-end test for this variation.

[References](#contents.xhtml_sc2_146a)

*   ASP.NET Core Blazor

[https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/blazor/?view=aspnetcore-7.0)

*   Build web applications with Blazor learning path - Training | Microsoft Learn

[https://learn.microsoft.com/en-us/training/paths/build-web-apps-with-blazor/](https://learn.microsoft.com/en-us/training/paths/build-web-apps-with-blazor/)

*   Blazor for Beginners

[https://www.youtube.com/playlist?list=PLdo4fOcmZ0oUJCA3DCzKT79Oe3kdKEceX](https://www.youtube.com/playlist?list=PLdo4fOcmZ0oUJCA3DCzKT79Oe3kdKEceX)

*   Blazor Tutorial - Build your first Blazor app

[https://dotnet.microsoft.com/en-us/learn/aspnet/blazor-tutorial/intro](https://dotnet.microsoft.com/en-us/learn/aspnet/blazor-tutorial/intro)

*   Awesome Blazor

[https://github.com/AdrienTorris/awesome-blazor](https://github.com/AdrienTorris/awesome-blazor)

*   ASP.NET Core Blazor hosting models

[https://learn.microsoft.com/en-us/aspnet/core/blazor/hosting-models?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/blazor/hosting-models?view=aspnetcore-7.0)

*   ASP.NET Core Blazor Hybrid

[https://learn.microsoft.com/en-us/aspnet/core/blazor/hybrid/?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/blazor/hybrid/?view=aspnetcore-7.0)

*   WebAssembly Concepts

[https://developer.mozilla.org/en-US/docs/WebAssembly/Concepts](https://developer.mozilla.org/en-US/docs/WebAssembly/Concepts)

*   A Breakdown of Blazor Project Types

[https://dzone.com/articles/a-breakdown-of-blazor-project-types](https://dzone.com/articles/a-breakdown-of-blazor-project-types)

*   Blazor Server vs. Blazor WebAssembly: Four Ways In Which They Differ

[https://www.roundthecode.com/dotnet/blazor/blazor-server-vs-blazor-webassembly-four-ways-in-which-they-differ](https://www.roundthecode.com/dotnet/blazor/blazor-server-vs-blazor-webassembly-four-ways-in-which-they-differ)

*   ASP.NET Core Blazor Progressive Web Application (PWA)

[https://learn.microsoft.com/en-us/aspnet/core/blazor/progressive-web-app?view=aspnetcore-7.0&tabs=visual-studio](https://learn.microsoft.com/en-us/aspnet/core/blazor/progressive-web-app?view=aspnetcore-7.0&tabs=visual-studio)

*   ASP.NET Core Blazor dependency injection

[https://learn.microsoft.com/en-us/aspnet/core/blazor/fundamentals/dependency-injection?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/blazor/fundamentals/dependency-injection?view=aspnetcore-7.0)

*   Call a web API from ASP.NET Core Blazor

[https://learn.microsoft.com/en-us/aspnet/core/blazor/call-web-api?view=aspnetcore-7.0&pivots=webassembly](https://learn.microsoft.com/en-us/aspnet/core/blazor/call-web-api?view=aspnetcore-7.0&pivots=webassembly)

*   Bulls and Cows

[https://en.wikipedia.org/wiki/Bulls_and_Cows](https://en.wikipedia.org/wiki/Bulls_and_Cows)

*   Create reusable UI using the Razor class library project in ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/razor-pages/ui-class?view=aspnetcore-7.0&tabs=visual-studio](https://learn.microsoft.com/en-us/aspnet/core/razor-pages/ui-class?view=aspnetcore-7.0&tabs=visual-studio)

*   Consume ASP.NET Core Razor components from a Razor class library (RCL)

[https://learn.microsoft.com/en-us/aspnet/core/blazor/components/class-libraries?view=aspnetcore-7.0&tabs=visual-studio](https://learn.microsoft.com/en-us/aspnet/core/blazor/components/class-libraries?view=aspnetcore-7.0&tabs=visual-studio)

*   Test Razor components in ASP.NET Core Blazor

[https://learn.microsoft.com/en-us/aspnet/core/blazor/test?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/blazor/test?view=aspnetcore-7.0)

*   Getting started with bUnit

[https://bunit.dev/docs/getting-started/index.html](https://bunit.dev/docs/getting-started/index.html)

*   Installation | Playwright .NET

[https://playwright.dev/dotnet/docs/intro](https://playwright.dev/dotnet/docs/intro)

*   Publish a Blazor WebAssembly app and .NET API with Azure Static Web Apps

[https://learn.microsoft.com/en-us/training/modules/publish-app-service-static-web-app-api-dotnet/](https://learn.microsoft.com/en-us/training/modules/publish-app-service-static-web-app-api-dotnet/)

# [CHAPTER 6SPA with Angular](#contents.xhtml_ch06a)

[Introduction](#contents.xhtml_sc2_147a)

This chapter is about developing a rich single-page application with Angular on the client side supported by ASP.NET core on the server side. The chapter begins with the big picture explaining the interplay of different technologies in various tiers, followed by a deep dive into a real-life case study solved by this combination. The development begins with the built-in template in Visual Studio and offers the convenience of hosting both projects in one ASP.NET Core project built and published as a single unit.

[Structure](#contents.xhtml_sc2_148a)

This chapter will cover the following topics:

*   Introduction to Single-Page Application
*   Pre-requisites
*   Getting started with SPA using Angular
    *   Structure of the (default) ASP.NET Core Angular project
        *   Working of SPA template application
*   Developing Angular CRUD App
    *   Creating the Angular App
        *   Getting started
        *   Create models
        *   Scaffolding – API Controller
        *   Creating a database using EF Core migration
        *   Add support for Swagger documentation
        *   Seeding
        *   Create Angular components and services
        *   Book List Page
        *   Book Detail Page
        *   Book Edit Page
        *   Book Delete Page
    *   Unit testing
    *   Deployment

[Objectives](#contents.xhtml_sc2_149a)

The objective of this chapter is to understand how to create a single page web application using the popular JavaScript framework Angular on the client side and ASP.NET Core Web API on the server-side in Visual Studio 2022 using C# 11 and .NET 7.0.

[Introduction to Single-Page Application](#contents.xhtml_sc2_150a)

In a traditional web application, the browser re-loads the entire page from the server on every user request. However, in a single-page application (SPA) the current page is dynamically re-written with new data from the server on user interaction. SPAs are built using HTML, JavaScript, and CSS, as well as frameworks such as React, Angular and Vue. SPAs provide a smooth, responsive user experience closer to a native application, as the page loads quickly and requires minimal data exchange with the server.

SPAs have both advantages and disadvantages compared to multiple page applications. Advantages include improved performance, better user experience, and easier SEO optimization. Disadvantages include increased complexity in development and difficulty in debugging.

In the previous chapter, we covered Blazor applications. In contrast to SPAs, Blazor is a component-based, single-page app framework for building client-side web apps using .NET. It uses WebAssembly for client-side Blazor and server-side Blazor for server-side rendering. It also allows developers to write code in C# instead of JavaScript, which makes it easier to develop complex web applications.

[Pre-requisites](#contents.xhtml_sc2_151a)

Visual Studio 2022 Community Edition or higher preferably with the latest updates is needed to work through the examples in this chapter along with the ASP.NET and web development workload. To work with the dependencies in the Angular application, Node JS is required. This can be done either by installing Node JS from [https://nodejs.org/en/download/](https://nodejs.org/en/download/) or by installing Node.js development workload in Visual Studio.

[Getting started with SPA using Angular](#contents.xhtml_sc2_152a)

Create a new ASP.NET Core with Angular project by following the steps below in Visual Studio 2022:

| New project creation (File &#124; New &#124; Project…) |
|  
1.  Create a new project

 |  
1.  Narrow down the list of templates being shown by selecting, Language: C#, Platform: All platforms, Project type: Web
2.  Select template: ASP.NET Core with Angular
3.  Click Next

 |
|  
*   B. Configure your new project

 |  
4.  Project name: Enter name of your choice such as FirstAngularApp
5.  Location: Select location of choice
6.  Solution: Select either Add to solution  or Create new solution
7.  Solution name: Provide name in case a new solution is created
8.  Place solution and project in the same directory: Normally we keep the solution a level higher so leave it unchecked in case a new solution is created.
9.  Click Next

 |
|  
*   C. Additional information

 |  
10.  Framework: .NET 7.0 (Standard Term Support)
11.  Authentication type: None
12.  Configure for HTTPS: Checked
13.  Do not use top-level statements: Unchecked
14.  Click Create

 |

Table 6.1: Steps to create new ASP.NET Core with Angular project

This creates a new SPA that uses Angular at the front-end and ASP.NET core at the back end. The new project can be created using dotnet command line interface (CLI) with following command:

dotnet new  angular --name FirstAngularApp

And to add the newly created project to the solution:

dotnet sln  add ./FirstAngularApp/FirstAngularApp.csproj

[Structure of (default) ASP.NET Core Angular Project](#contents.xhtml_sc3_153a)

On creating the new application using the built-in ASP.NET Core with Angular template the WeatherForecast application is created, this time with ASP.NET Core web API project and Angular CLI project combined into a single csproj file and having the convenience of hosting both via a common project - built and published together. Before examining the working of this project let us examine the folder and the files that are unique in this project type.

| Dependencies &#124; Frameworks | By default, there is a dependency on Microsoft.AspNetCore.App and Microsoft.NETCore.App. |
| Dependencies &#124; Packages | There is a dependency to the NuGet package - Microsoft.AspNetCore.SpaProxy |
| Properties/ | Like the other web projects, in this folder we have the lone file launchSettings.json containing settings that control how the web app is started on development machine. |
| wwwroot/ | Contains the lone favicon.ico image displayed next to the page title in the browser tab. |
| ClientApp/ | This folder contains the entire Angular standard application. |
| Controllers/ | This contains the lone WeatherForecastController.cs for the ASP.NET Core Web API |
| Pages/ | Contains the two files _ViewImports.cshtml and Error.cshtml |
| .gitignore | Git file to ignore Visual Studio temporary files, build results, and files generated by some add-ons. |
| appsettings.json | Like for other projects this file contains the settings for common settings for use through-out the project. |
| Program.cs | Like other web applications, it is here that the request handling pipeline is configured as a series of middleware components and the services required by the app during start up. |
| WeatherForecast.cs | The model class referred in WeatherForecastController.cs |

Table 6.2: Important files and folders in ASP.NET Core Angular Project

The project shows up as follows in the Solution Explorer:

![](images/Figure_6.1.png)

Figure 6.1: Files in default Angular app

As described earlier the ClientApp folder houses the complete Angular application which can run independently along with all its dependencies. Let us examine the important files in this basic application:

| .angular/ | This folder contains the cache used by Angular CLI. |
| node_modules/ | This folder is not visible in Solution Explorer unless Show All Files is chosen. It contains the Node Package Manager (NPM) package dependencies. |
| src/ | This is the root folder for the application project. |
| src/app/ | Contains the component files with application logic and data defined. |
| src/app/app.component.html | Defines the HTML template associated with the root AppComponent. |
| src/app/app.component.ts | This TypeScript file defines the logic for the application's root component, named AppComponent. The view associated with this root component becomes the root of the view hierarchy as new components and services are added to the application. |
| src/app/app.module.ts | Defines the root module, named AppModule, that tells Angular how to assemble the application. Initially declares only the AppComponent. As more components get added, they must be declared here. |
| src/app/app.server.module.ts | This is the server-side application module, applicable in case of server-side rendering (SSR). |
| src/assets/ | Contains image and other asset files to be copied as-is when the application is built. |
| src/environments | Contains files to set up environment specific settings. |
| src/index.html | The main HTML page that is served when someone visits the site. The CLI automatically adds all JavaScript and CSS files when building that app, adding any <script> or <link> tags manually is not necessary. |
| src/main.ts | This is the main entry point for the application. It compiles the application with the JIT compiler and bootstraps the application's root module AppModule to run in the browser. |
| src/Polyfills.ts | This file includes polyfills needed by Angular and is loaded before the app. Extra polyfills can be added to this file. |
| src/styles.css | Lists CSS files that supply styles for a project. The extension reflects the style pre-processor configured for the project. |
| src/tests.ts | This file is required by karma.conf.js and loads recursively all the .spec.ts  and framework files |
| .browserslistrc | This file is used by the build system to adjust CSS and JS output to support the specified browsers |
| .editorconfig | Contains configuration for code editors. |
| .gitignore | Specifies intentionally untracked files that Git should ignore. |
| angular.json | This file contains the configuration defaults for the project that the CLI uses including configuration options to build, serve, and test. |
| aspnetcore-https.js | This script sets up HTTPS for the application using the ASP.NET Core HTTPS certificate. |
| karma.conf.js | This is the Karma unit-test runner’s configuration file. |
| package.json | Configures NPM package dependencies that are available to the project. |
| proxy.conf.js | This file contains the parameters used to setup the SPA proxy |
| README.md | Includes the introductory documentation for the root application. |
| tsconfig.json | The base TypeScript configuration for projects in the workspace. The other configuration files – the application specific (tsconfig.app.json) and test specific (tsconfig.spec.json) configuration files inherit from this base file. |

Table 6.3: Important files and folders in ASP.NET Core Angular Project

Components are the building blocks of an Angular application. A component includes a TypeScript class that has a @Component() decorator to specify metadata - HTML template and styles about a class. The typescript class and the HTML template support two-way binding which means, the class listens for all HTML events from the HTML file and if there is a change in a data element in the class it is reflected on the HTML template.

![](images/Figure_6.2.png)

Figure 6.2: Angular Component

The ClientApp Angular application is made of components - counter, fetch-data, home and nav-menu besides the root app component. Each of these has their own TypeScript class and HTML template. Some of the components also have their own style .css file and a unit-test .spec.ts file. Let us examine the files for the counter component.

Class - counter.component.ts

1.  import { Component } from  '@angular/core';

3.  @Component({
4.  selector: 'app-counter-component',
5.  templateUrl: './counter.component.html'
6.  })
7.  export  class  CounterComponent {
8.  public currentCount = 0;

10.  public incrementCounter() {
11.  this.currentCount++;
12.  }
13.  }

The preceding code creates a component is created with a @Component() decorator that has metadata that tells Angular where to find the HTML template and declares the selector which allows using it as HTML tag for placing within other templates.

HTML Template - counter.component.html

1.  <h1>Counter</h1>

3.  <p>This is a simple example of an Angular component.</p>

5.  <p  aria-live="polite">Current count: <strong>{{  currentCount }}</strong></p>

7.  <button  class="btn btn-primary"  (click)="incrementCounter()">Increment</button>

The preceding code is the HTML template corresponding to the counter component for declaring how the component will render. It can use the properties and the methods in the component class. Line 5 uses the currentCount property in double curly braces {{ }} to replace it dynamically. Line 7 invokes the incrementCounter method on the button click event.

Component testing - counter.component.spec.ts

1.  import { async, ComponentFixture, TestBed } from  '@angular/core/testing';

3.  import { CounterComponent } from  './counter.component';

5.  describe('CounterComponent', () => {
6.  let fixture: ComponentFixture<CounterComponent>;

8.  beforeEach(async(() => {
9.  TestBed.configureTestingModule({
10.  declarations: [CounterComponent]
11.  })
12.  .compileComponents();
13.  }));

15.  beforeEach(() => {
16.  fixture = TestBed.createComponent(CounterComponent);
17.  fixture.detectChanges();
18.  });

20.  it('should display a title', async(() => {
21.  const titleText = fixture.nativeElement.querySelector('h1').textContent;
22.  expect(titleText).toEqual('Counter');
23.  }));

25.  it('should start with count 0, then increments by 1 when clicked', async(() => {
26.  const countElement = fixture.nativeElement.querySelector('strong');
27.  expect(countElement.textContent).toEqual('0');

29.  const incrementButton = fixture.nativeElement.querySelector('button');
30.  incrementButton.click();
31.  fixture.detectChanges();
32.  expect(countElement.textContent).toEqual('1');
33.  }));
34.  });

The preceding is the testing file for counter that uses Jasmine behaviour testing framework. The first test starting from line 20, verifies the title of the page on line 22\. In the second test starting on line 25, we are first ensuring that the counter equals to zero (line 27) and then after clicking the increment button (line 29) we expect the counter to become one on line 32.

Modules are another important building block of an Angular application apart from components. A module class describes how the application parts fit together. Every application has at least one module, the root module bootstraps to launch the application. The ClientApp includes the root module in app.module.ts as shown below.

1.  import { BrowserModule } from  '@angular/platform-browser';
2.  import { NgModule } from  '@angular/core';
3.  import { FormsModule } from  '@angular/forms';
4.  import { HttpClientModule } from  '@angular/common/http';
5.  import { RouterModule } from  '@angular/router';

7.  import { AppComponent } from  './app.component';
8.  import { NavMenuComponent } from  './nav-menu/nav-menu.component';
9.  import { HomeComponent } from  './home/home.component';
10.  import { CounterComponent } from  './counter/counter.component';
11.  import { FetchDataComponent } from  './fetch-data/fetch-data.component';

13.  @NgModule({
14.  declarations: [
15.  AppComponent,
16.  NavMenuComponent,
17.  HomeComponent,
18.  CounterComponent,
19.  FetchDataComponent
20.  ],
21.  imports: [
22.  BrowserModule.withServerTransition({ appId: 'ng-cli-universal' }),
23.  HttpClientModule,
24.  FormsModule,
25.  RouterModule.forRoot([
26.  { path: '', component: HomeComponent, pathMatch: 'full' },
27.  { path: 'counter', component: CounterComponent },
28.  { path: 'fetch-data', component: FetchDataComponent },
29.  ])
30.  ],
31.  providers: [],
32.  bootstrap: [AppComponent]
33.  })
34.  export  class  AppModule { }

The module in the preceding code bootstraps the components within the application and the other required modules. Between lines 25 and 28 the route is declared to access the counter and fetch-data components.

[Working of SPA template application](#contents.xhtml_sc4_154a)

As mentioned in the beginning, the single-page application created using the Visual Studio template for SPA combines the front-end angular application and the back end ASP.NET core application in a single project. Although it is possible to run each of them separately, but this template makes it convenient to execute one project and run both the client and the server applications. This step is identical for both Angular and the React templates shipped with .NET SDK.

During development, the app is configured to use the frontend proxy. React and Angular use the same frontend proxy. The proxy server information is included in the project file as shown in the snippet below on the highlighted lines.

1.  <Project  Sdk="Microsoft.NET.Sdk.Web">
2.  <PropertyGroup>
3.  <TargetFramework>net7.0</TargetFramework>
4.  <Nullable>enable</Nullable>
5.  <IsPackable>false</IsPackable>
6.  <SpaRoot>ClientApp\\cf1 </SpaRoot>

7.  <SpaProxyServerUrl>https://localhost:44418</SpaProxyServerUrl>
8.  <SpaProxyLaunchCommand>npm start</SpaProxyLaunchCommand>

9.  <ImplicitUsings>enable</ImplicitUsings>
10.  </PropertyGroup>

12.  <ItemGroup>

13.  <PackageReference  Include="Microsoft.AspNetCore.SpaProxy"  Version="7.0.2" />

14.  </ItemGroup>
15.  …

The referenced package Microsoft.AspNetCore.SpaProxy on line 13 enables the proxy server using the configurations on line 7 and 8\. SpaProxyServerUrl is the URL of SPA proxy. The server checks to see if the proxy is ready, if not it uses the command in SpaProxyLaunchCommand to launch the proxy.

The client-side setup in the Angular application that enables the working of proxy is spread across package.json, angular.json, and proxy.conf.js, as listed below.

package.json

1.  {
2.  "name": "firstangularapp",
3.  "version": "0.0.0",
4.  "scripts": {
5.  "ng": "ng",

6.  "prestart": "node aspnetcore-https",
7.  "start": "run-script-os",
8.  "start:windows": "ng serve --port 44418 --ssl --ssl-cert \"%APPDATA%\\ASP.NET\\https\\%npm_package_name%.pem\" --ssl-key \"%APPDATA%\\ASP.NET\\https\\%npm_package_name%.key\"",
9.  "start:default": "ng serve --port 44418 --ssl --ssl-cert \"$HOME/.aspnet/https/${npm_package_name}.pem\" --ssl-key \"$HOME/.aspnet/https/${npm_package_name}.key\"",

10.  "build": "ng build",
11.  "build:ssr": "ng run FirstAngularApp:server:dev",
12.  "watch": "ng build --watch --configuration development",
13.  "test": "ng test"
14.  },
15.  …

The highlighted lines in the preceding snippet provide information to launch Angular via ng serve and option to use HTTPS.

angular.json

1.  …
2.  "serve": {
3.  "builder": "@angular-devkit/build-angular:dev-server",
4.  "configurations": {
5.  "production": {
6.  "browserTarget": "FirstAngularApp:build:production"
7.  },
8.  "development": {
9.  "browserTarget": "FirstAngularApp:build:development",
10.  "proxyConfig": "proxy.conf.js"
11.  }
12.  },
13.  …

The proxyconfig element in the development configuration on line 10 indicates that should be used to configure the frontend proxy.

proxy.conf.js

1.  const { env } = require('process');

3.  const target = env.ASPNETCORE_HTTPS_PORT ? `https://localhost:${env.
    ASPNETCORE_HTTPS_PORT}` :
4.  env.ASPNETCORE_URLS ? env.ASPNETCORE_URLS.split(‹;›)[0] : 'http://
    localhost:53066';

6.  const PROXY_CONFIG = [
7.  {
8.  context: [
9.  "/weatherforecast",
10.  ],
11.  target: target,
12.  secure: false,
13.  headers: {
14.  Connection: 'Keep-Alive'
15.  }
16.  }
17.  ]

19.  module.exports = PROXY_CONFIG;

The preceding code defines the routes to proxy, back to the server backend. The flow of information between the client, the proxy and the server ID depicted below:

![](images/Figure_6.3.png)

Figure 6.3: Flow between client, proxy, and server

The ASP.NET Core SPA Proxy middleware intercepts the client request and checks if the front-end proxy specified in the project file with SpaProxyServerUrl setting is running if not it executes the command in SpaProxyLaunchCommand to launch the same. In the interim, a temporary landing page is returned which continues to ping the proxy and once it is up a 301 redirect happens to the URL. The UI during the flow shows up as follows:

![](images/Figure_6.4.png)

Figure 6.4: Accessing the server URL shows temporary page

Take a look at the backend console window as shown in the following figure:

![](images/Figure_6.5.png)

Figure 6.5: Backend console window

Once the redirect is complete and the proxy is running, the UI shows up as follows:

![](images/Figure_6.6.png)

Figure 6.6: Angular UI after the proxy is up

Simultaneously, another console window shows the launch of Angular application via Angular CLI command as follows:

![](images/Figure_6.7.png)

Figure 6.7: Console window of Angular application

The described flow happens only during the development time. At publish time, the files of the Angular app are copied to the wwwroot folder and are served via the static files middleware.

Also, so far, we have launched the front-end and the backend simultaneously (by launching the ASP.NET Core backend) but it is possible to launch them separately by launching the frontend manually with npm run start and avoiding having to start the frontend server every time.

[Developing Angular CRUD App](#contents.xhtml_sc2_155a)

To develop a real-life application, we will create the Angular version of the DigitalBookStore application, which we had created in the chapters on Web App and Web API. The new application will allow us to maintain, that is, perform the CRUD operations with Books data but this time, we will use the ASP.NET Core with Angular template, which as we have seen will help us create an SPA with ASP.NET core back-end API and Angular in the front-end.

[Creating the Angular app](#contents.xhtml_sc3_156a)

After following the steps in this section, a fully functional CRUD application would be ready. The Book List page will look as follows:

![](images/Figure_6.8.png)

Figure 6.8: Final UI – Bookstore list page

The Book Detail page as follows:

![](images/Figure_6.9.png)

Figure 6.9: Final UI – Book detail page

The Book Edit page shows up as follows:

![](images/Figure_6.10.png)

Figure 6.10: Final UI – Book create or edit page

And the Book deletion functionality shows the confirmation dialog as follows:

![](images/Figure_6.11.png)

Figure 6.11: Final UI – Book deletion

[Getting started](#contents.xhtml_sc4_157a)

Create a new project named DigitalBookStoreNgApp using the ASP.NET  Core  with  Angular template choosing all the default options as described for the FirstAngularApp application earlier. Make following changes in the project to remove the default WeatherForecast related functionality.

1.  Server-side changes
    *   Delete the class files WeatherForecast.cs and /Controllers/ WeatherForecastController.cs
2.  Client-side changes within /ClientApp/src/app folder.
    1.  app.server.module.ts – remove import of ModuleMapLoaderModule as it is deprecated in the newer version of Angular.
        1.  import { NgModule } from  '@angular/core';
        2.  import { ServerModule } from  '@angular/platform-server';
        3.  import { ModuleMapLoaderModule } from  '@nguniversal/module-map-ngfactory-loader';
        4.  import { AppComponent } from  './app.component';
        5.  import { AppModule } from  './app.module';

        7.  @NgModule({
        8.  imports: [AppModule, ServerModule, ModuleMapLoaderModule],

        10.  bootstrap: [AppComponent]
        11.  })
        12.  export  class  AppServerModule { }
    2.  app.module.ts – remove lines related to CounterComponent and FetchDataComponent
        1.  import { BrowserModule } from  '@angular/platform-browser';
        2.  import { NgModule } from  '@angular/core';
        3.  import { FormsModule } from  '@angular/forms';
        4.  import { HttpClientModule } from  '@angular/common/http';
        5.  import { RouterModule } from  '@angular/router';

        7.  import { AppComponent } from  './app.component';
        8.  import { NavMenuComponent } from  './nav-menu/nav-menu.component';
        9.  import { HomeComponent } from  './home/home.component';
        10.  import { CounterComponent } from  './counter/counter.component';
        11.  import { FetchDataComponent } from  './fetch-data/fetch-data.component';

        13.  @NgModule({
        14.  declarations: [
        15.  AppComponent,
        16.  NavMenuComponent,
        17.  HomeComponent,
        18.  CounterComponent,
        19.  FetchDataComponent
        20.  ],
        21.  imports: [
        22.  BrowserModule.withServerTransition({ appId: 'ng-cli-universal' }),
        23.  HttpClientModule,
        24.  FormsModule,
        25.  RouterModule.forRoot([
        26.  { path: '', component: HomeComponent, pathMatch: 'full' },
        27.  { path: 'counter', component: CounterComponent },
        28.  { path: 'fetch-data', component: FetchDataComponent },
        29.  ])
        30.  ],
        31.  providers: [],
        32.  bootstrap: [AppComponent]
        33.  })
        34.  export  class  AppModule { }
    3.  remove folders – counter and fetch-data
    4.  nav-menu/nav-menu.component.html – remove lines related to counter and fetch-data routes and change text DigitalBookStoreNgApp to Digital Book Store.
    5.  src/index.html – change page title from DigitalBookStoreNgApp to Digital Book Store.

Set the project as the startup project and run it to ensure project is compiling fine. After all the clean-up, the UI appears as follows:

![](images/Figure_6.12.png)

Figure 6.12: Initial UI after the clean-up

[Create models](#contents.xhtml_sc4_158a)

Create the model classes under /Models folder with following code:

Publisher.cs

1.  namespace DigitalBookStoreNgApp.Models;

3.  public  class  Publisher
4.  {
5.  public  int Id { get; set; }
6.  public  string Name { get; set; }
7.  }

Book.cs

1.  namespace DigitalBookStoreNgApp.Models;

3.  public  class  Book
4.  {
5.  public  int Id { get; set; }
6.  public  string Title { get; set; }
7.  public  decimal Price { get; set; }

9.  ///  <summary>
10.  /// List of one or more semi-colon separated authors string
11.  ///  </summary>
12.  public  string Authors { get; set; }

14.  ///  <summary>
15.  /// List of one or more semi-colon separated tags string
16.  ///  </summary>
17.  public  string Tags { get; set; }

19.  public  int PublisherId { get; set; }
20.  public  Publisher? Publisher { get; set; }

22.  public  DateTime PublishDate { get; set; }
23.  }

[Scaffolding – API controller](#contents.xhtml_sc4_159a)

We will use the scaffolding option of Visual Studio to create a basic API controller with CRUD actions. Right-click on the Controller folder and choose Add | New Scaffolded Item. In the Add New Scaffolded Item dialog, select API Controller with actions, using Entity Framework. Upon clicking Add, in the next dialog choose the Model class as the Book class and create a new DbContext class by clicking the + button. All other are left as default:

![](images/Figure_6.13.png)

Figure 6.13: Books API controller scaffolding options.

On clicking Add the code for BooksController having endpoints related to CRUD actions and the DBContext are created. Suitable dependencies to EF Core are added to the project and the connection string is also added to the appsettings.json. For more details refer to this step in the chapters on Web App and Web API.

In a similar way, create the PublishersController by choosing the Publisher model class.

[Creating database using EF Core migration](#contents.xhtml_sc4_160a)

Before starting with the database creation rename DBSet objects in DigitalBookStore NgAppContext.cs to their plural names as follows. Do this by right-clicking and selecting Rename to ensure all references are renamed and there are no compilation errors:

public  DbSet<Models.Book> Books { get; set; } = default!;

public  DbSet<Models.Publisher> Publishers { get; set; } = default!;

Values in the DBContext are read to generate the database schema scripts, by making these plural we will ensure that the tables also follow similar convention.

Now run the following command to create the initial schema. Before running the command make sure to set the default project to the DigitalBookStoreNgApp project in the PMC window:

Add-Migration InitialCreate

Execute the following command in PMC to create the actual database:

Update-Database

The database so created can be examined via View | SQL Server Object Explorer in Visual Studio. This is the same database pointed to by our connection string in the appsettings.json.

After the code generation and running EF Core migration it is a good idea to run the code clean-up. Right-click the project and choose Analyze and Code Cleanup | Run Code Cleanup (Profile 1).

[Add support for Swagger documentation](#contents.xhtml_sc4_161a)

To verify the API endpoints let us add support for Swagger documentation. Add the NuGet package Swashbuckle.AspNetCore and highlighted lines in Program.cs:

1.  …
2.  builder.Services.AddControllersWithViews();

3.  builder.Services.AddSwaggerGen();

5.  var app = builder.Build();

7.  if (!app.Environment.IsDevelopment())
8.  {
9.  app.UseHsts();
10.  }

11.  else
12.  {
13.  app.UseSwagger();
14.  app.UseSwaggerUI();
15.  }

17.  app.UseHttpsRedirection();
18.  …

Running the project and manually navigating to the server-side host URL with /Swagger endpoint (after the redirect to the SPA proxy has completed) should show the following UI, indicating that the ASP.NET Core web API is working fine, and Swagger is correctly wired:

![](images/Figure_6.14.png)

Figure 6.14: Swagger UI for the API

[Seeding](#contents.xhtml_sc4_162a)

Like database seeding in the ASP.NET Core Web App and ASP.NET Core Web API chapters, we will programmatically seed records for testing purposes. Create the class /Data/SeedData.cs and on the lines of SeedData class in either DigitalBookStore or DigitalBookStoreAPI projects and then invoke its static Initialize method during application start up in Program.cs as follows:

1.  …

2.  using (var scope = app.Services.CreateScope())
3.  {
4.  var services = scope.ServiceProvider;
5.  var context = services.GetRequiredService<DigitalBookStoreNgAppContext>();
6.  context.Database.EnsureCreated();
7.  SeedData.Initialize(context);
8.  }

10.  app.UseHttpsRedirection();
11.  …

Trying the GET /api/Books endpoint in the Swagger UI should now fetch records inserted in the database:

![](images/Figure_6.15.png)

Figure 6.15: Fetching book records after seeding.

[Create Angular components and services](#contents.xhtml_sc4_163a)

To create the different Angular components and services, right-click on the ClientApp/src/app folder in solution explorer and select Open in Terminal to open the Developer PowerShell console at the chosen folder location. Now execute following Angular CLI commands one-by-one.

ng g module books

ng g c books/book-list

ng g c books/book-edit

ng g c books/book-detail

ng g s books/book

ng g class books/book

The preceding commands will create the Books feature module followed by skeleton files for components, service, and book model class along with related files. The newly created files will appear as follows in the solution explorer:

![](images/Figure_6.16.png)

Figure 6.16: Books feature module within ClientApp.

Next, we need to register the Books feature module within the root App module. Add the highlighted changes in app.module.ts:

1.  …
2.  import { HomeComponent } from  './home/home.component';

4.  import { BooksModule } from  './books/books.module';

6.  @NgModule({
7.  declarations: [
8.  AppComponent,
9.  NavMenuComponent,
10.  HomeComponent,
11.  ],
12.  imports: [
13.  BrowserModule.withServerTransition({ appId: 'ng-cli-universal' }),
14.  HttpClientModule,
15.  FormsModule,

16.  BooksModule,

17.  RouterModule.forRoot([
18.  { path: '', component: HomeComponent, pathMatch: 'full' },
19.  ])
20.  ],
21.  …

To register the CRUD routes for Book entity in Books module, add the highlighted changes in books.module.ts.

1.  …
2.  import { BookDetailComponent } from  './book-detail/book-detail.component';

3.  import { RouterModule } from  '@angular/router';
4.  import { FormsModule } from  '@angular/forms';

6.  @NgModule({
7.  declarations: [
8.  BookListComponent,
9.  BookEditComponent,
10.  BookDetailComponent
11.  ],
12.  imports: [
13.  CommonModule,

14.  FormsModule,
15.  RouterModule.forChild([
16.  { path: 'books', component: BookListComponent },
17.  { path: 'books/detail/:id', component: BookDetailComponent, },
18.  { path: 'books/edit/:id', component: BookEditComponent, },
19.  { path: 'books/edit', component: BookEditComponent }
20.  ])

21.  ]
22.  })
23.  export  class  BooksModule { }

To verify that the changes done so far are working, add the following changes in nav-menu.component.html:

1.  …
2.  <ul  class="navbar-nav flex-grow">
3.  <li  class="nav-item"
4.  [routerLinkActive]="['link-active']"
5.  [routerLinkActiveOptions]="{ exact: true }">
6.  <a  class="nav-link text-dark"  [routerLink]="['/']">Home</a>
7.  </li>

8.  <li  class="nav-item">
9.  <a  class="nav-link text-dark"  [routerLink]="['/books']">Books</a>

10.  </li>
11.  </ul>
12.  …

Saving the changes and running the project should now show up the Books link on the home page and clicking on it should show the following Books skeleton list page:

![](images/Figure_6.17.png)

Figure 6.17: Skeleton Books List page

In the following sections we will build the CRUD functionality one by one.

[Book List Page](#contents.xhtml_sc4_164a)

Update the book.ts  model class with following code.

1.  export  class  Book {
2.  id!: number;
3.  title!: string;
4.  price!: number;
5.  authors!: string;
6.  authorsListDisplay!: string;
7.  tags!: string;
8.  publishDate!: Date;
9.  publisherId!: number;
10.  publisherName!: string|null;
11.  }

Add the following code to book.service.ts:

1.  import { Injectable } from  '@angular/core';
2.  import { HttpClient } from  '@angular/common/http';
3.  import { Observable } from  'rxjs';

5.  const baseURL = 'https://localhost:7298/api/books'; //point to server url

7.  @Injectable({
8.  providedIn: 'root'
9.  })
10.  export  class  BookService {

12.  constructor(private httpClient: HttpClient) { }

14.  readAll(): Observable<any> {
15.  return  this.httpClient.get(baseURL);
16.  }

18.  read(id: any): Observable<any> {
19.  return  this.httpClient.get(`${baseURL}/${id}`);
20.  }

22.  create(data: any): Observable<any> {
23.  return  this.httpClient.post(baseURL, data);
24.  }

26.  update(id: any, data: any): Observable<any> {
27.  return  this.httpClient.put(`${baseURL}/${id}`, data);
28.  }

30.  delete(id: any): Observable<any> {
31.  return  this.httpClient.delete(`${baseURL}/${id}`);
32.  }
33.  }

The Book service in the preceding code invokes the ASP.NET Core API from the base URL declared on line 5 via the HttpClient injected in the constructor on line 12\. Each method corresponds to the API endpoint and uses the appropriate method to make the REST call.

Replace the code in book-list.component.ts with following code:

1.  import { Component, OnInit } from  '@angular/core';
2.  import { BookService } from  'src/app/books/book.service';
3.  import { Book } from  "../book";

5.  @Component({
6.  selector: 'app-book-list',
7.  templateUrl: './book-list.component.html',
8.  styleUrls: ['./book-list.component.css']
9.  })
10.  export  class  BookListComponent  implements  OnInit {
11.  books!: Book[];

13.  constructor(private bookService: BookService) { }

15.  ngOnInit(): void {
16.  this.readBooks();
17.  }

19.  readBooks(): void {
20.  this.bookService.readAll()
21.  .subscribe(
22.  books => {
23.  this.books = books;
24.  console.log(books);
25.  },
26.  error => {
27.  console.log(error);
28.  });
29.  }
30.  }

The typescript class BookListComponent populates the books array by invoking the readAll from bookService during initialization on line 16.

Add the following code to book-list.component.html:

1.  <div  class="table-wrapper">
2.  <div  class="table-title">
3.  <div  class="row">
4.  <div  class="col-sm-4">
5.  <h4><b>Books List</b></h4>
6.  <a  href="#"  routerLink="/books/edit"  class="btn btn-success back"><I  class="fas fa-plus-circle"></I>  Create</a>
7.  </div>
8.  </div>
9.  </div>
10.  <table  class="table table-striped table-hover table-bordered table-content">
11.  <thead>
12.  <tr  class="center-align">
13.  <th>Title</th>
14.  <th>Price</th>
15.  <th>Author</th>
16.  <th>Publish Date</th>
17.  <th>Actions</th>
18.  </tr>
19.  </thead>
20.  <tbody>
21.  <tr  *ngFor="let book of books"  class="center-align">
22.  <td  class="text-truncate"  style="max-width: 250px">
    {{book.title}}</td>
23.  <td  style="max-width: 150px">{{book.price  |  currency}}</td>
24.  <td  class="text-truncate"  style="max-width: 250px">
    {{book.authors}}</td>
25.  <td  style="max-width: 150px">{{book.publishDate  |  date}}</td>
26.  <td  style="max-width: 150px">
27.  <a  href="#"  [routerLink]="['/books/detail/', book.id]"  class="btn"><i  class='fas fa-eye view'></i></a>
28.  <a  href="#"  [routerLink]="['/books/edit/', book.id]"  class="btn"><i  class="fa fa-edit edit"></i></a>
29.  </td>
30.  </tr>
31.  <tr>
32.  <td  *ngIf="!books || books.length == 0"  colspan="6">No books Found</td>
33.  </tr>
34.  </tbody>
35.  </table>
36.  </div>

The book list is shown in a tabular form iterating through the books array on line 21, populated in the code-behind class.

Link following stylesheet in ClientApp/src/index.html to include the library Font Awesome as we have used some of the icons from the library on lines 6, 27 and 28:

<link  rel="stylesheet"  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.3.0/css/all.min.css">

We have made all the required changes to view the list page. On running the project, we expect to see the Books List page but following UI shows up instead:

![](images/Figure_6.18.png)

Figure 6.18: Books list not rendered due to CORS issue

The ASP.NET core web API and the Angular front-end are served from different websites due to which the same-origin policy is restricting the invocation of the Books API from the Angular page. The default browser security prevents a malicious site from reading sensitive data from another site. But since we know that it is a legitimate call, we can relax the same-origin policy by explicitly allowing some cross-origin requests while rejecting others. This is done by enabling Cross Origin Resource Sharing (CORS) via ASP.NET Core middleware. Include the highlighted line in Program.cs:

1.  ...
2.  var app = builder.Build();

3.  app.UseCors(x => x.WithOrigins("https://localhost:44497").AllowAnyMethod().AllowAnyHeader());

4.  if (!app.Environment.IsDevelopment())
5.  ...

Running the project now shows the list screen fine:

![](images/Figure_6.19.png)

Figure 6.19: Books list after enabling CORS.

[Book Detail Page](#contents.xhtml_sc4_165a)

Include the highlighted code in BooksController.cs to do the eager loading of the related Publisher entity via the navigational Publisher property of Book:

1.  [HttpGet("{id}")]
2.  public  async  Task<ActionResult<Book>> GetBook(int id)
3.  {
4.  if (_context.Books == null)
5.  {
6.  return  NotFound();
7.  }
8.  var book = await _context.Books.FindAsync(id);

10.  if (book == null)
11.  {
12.  return  NotFound();
13.  }

15.  _context.Entry(book) //load related publisher entity
16.  .Reference(b => b.Publisher)
17.  .Load();

19.  return book;
20.  }

Replace following code in book-detail.component.ts:

1.  import { Component, OnInit } from  '@angular/core';
2.  import { ActivatedRoute, Params } from  '@angular/router';
3.  import { Book } from  "../book";
4.  import { BookService } from  'src/app/books/book.service';

6.  @Component({
7.  selector: 'app-book-detail',
8.  templateUrl: './book-detail.component.html',
9.  styleUrls: ['./book-detail.component.css']
10.  })

12.  export  class  BookDetailComponent  implements  OnInit {
13.  book!: Book;
14.  error: any;

16.  constructor(
17.  private bookService: BookService,
18.  private route: ActivatedRoute) {
19.  }

21.  ngOnInit() {
22.  this.route.params.forEach((params: Params) => {
23.  let id = params['id'];
24.  if (id) {
25.  this.bookService.read(id)
26.  .subscribe(
27.  book => {
28.  this.book = book;
29.  this.book.publisherName = book.publisher.name;
30.  console.log(book);
31.  },
32.  error => {
33.  console.log(error);
34.  });
35.  }
36.  });
37.  }
38.  }

The BookDetailComponent code-behind class reads the book id parameter from the route URL on line 23 and uses it to fetch the book record via the BookService. The Publisher is a related entity for Book and is loaded automatically via EF, on line 29 we are explicitly assigning from the publisherName property of the client’s book object.

Replace following code in book-detail.component.html:

1.  <div  class="table-wrapper">
2.  <div  class="table-title">
3.  <div  class="row">
4.  <div  class="col-sm-6">
5.  <h4><b>Book Detail</b></h4>
6.  <a  href="#"  routerLink="/books"  class="btn btn-success back"><I  class="fas fa-arrow-circle-left"></I>  Back</a>
7.  </div>
8.  </div>
9.  </div>
10.  <table  class="table table-striped table-hover table-bordered table-content">
11.  <tbody>
12.  <tr>
13.  <td><label><b>Title</b></label></td>
14.  <td><span>{{  book.title }}</span></td>
15.  </tr>
16.  <tr>
17.  <td><label><b>Price</b></label>  </td>
18.  <td><span>{{  book.price  |  currency }}</span></td>
19.  </tr>
20.  <tr>
21.  <td>  <label><b>Authors</b></label></td>
22.  <td>  <span>{{  book.authors }}</span></td>
23.  </tr>
24.  <tr>
25.  <td>  <label><b>Tags</b></label></td>
26.  <td><span>{{  book.tags }}</span></td>
27.  </tr>
28.  <tr>
29.  <td>  <label><b>Publisher</b></label></td>
30.  <td>  <span>{{  book.publisherName }}</span></td>
31.  </tr>
32.  <tr>
33.  <td>  <label><b>Publish Date</b></label></td>
34.  <td>  <span>{{  book.publishDate  |  date }}</span></td>
35.  </tr>
36.  </tbody>
37.  </table>
38.  </div>

The preceding code shows the Book data by using Angular one-way data binding from the property such as book.title to the HTML view by enclosing within {{ and }}.

Navigating to the details of the Book should now work and show up as follows:

![](images/Figure_6.20.png)

Figure 6.20: Book Detail

[Book Edit page](#contents.xhtml_sc4_166a)

The Book Edit page will be used to both create a new Book record and update an existing record. To display a drop-down to choose Publisher for a Book, we need to create the Publisher service. Right-click on the ClientApp/src/app folder in solution explorer and select Open in Terminal to open the Developer PowerShell console at the chosen folder location. Now execute following Angular CLI commands one-by-one:

ng g s publishers/publisher

ng g class publishers/publisher

The preceding commands will create the skeleton files for Publisher service and the model class along with related files.

Update publisher.ts with following code:

1.  export  class  Publisher {
2.  id!: number;
3.  name!: string;
4.  }

Update publisher.service.ts with following code:

1.  import { Injectable } from  '@angular/core';
2.  import { HttpClient } from  '@angular/common/http';
3.  import { Observable } from  'rxjs';

5.  const baseURL = 'https://localhost:7298/api/publishers'; //point to server url

7.  @Injectable({
8.  providedIn: 'root'
9.  })
10.  export  class  PublisherService {

12.  constructor(private httpClient: HttpClient) { }

14.  readAll(): Observable<any> {
15.  return  this.httpClient.get(baseURL);
16.  }
17.  }

Add following to book-edit.component.ts:

1.  import { Component, OnInit } from  '@angular/core';
2.  import { ActivatedRoute, Params, Router } from  '@angular/router';
3.  import { Book } from  "../book";
4.  import { BookService } from  'src/app/books/book.service';
5.  import { PublisherService } from  'src/app/publishers/publisher.service';
6.  import { Publisher } from  '../../publishers/publisher';

8.  @Component({
9.  selector: 'app-book-edit',
10.  templateUrl: './book-edit.component.html',
11.  styleUrls: ['./book-edit.component.css']
12.  })

14.  export  class  BookEditComponent  implements  OnInit {
15.  book!: Book;
16.  publishers!: Publisher[];
17.  error: any;

19.  constructor(
20.  private bookService: BookService,
21.  private publisherService: PublisherService,
22.  private route: ActivatedRoute, private router: Router) {
23.  }

25.  ngOnInit() {
26.  this.route.params.forEach((params: Params) => {
27.  let id = params['id'];
28.  if (!id) {
29.  this.book = new  Book();
30.  } else {
31.  this.bookService.read(id)
32.  .subscribe(
33.  book => {
34.  this.book = book;
35.  console.log(book);
36.  },
37.  error => {
38.  console.log(error);
39.  });
40.  }
41.  this.populatePublishers();
42.  });
43.  }

45.  saveBook(): void {
46.  if (!this.book.id) {
47.  this.bookService.create(this.book) //id empty invoke create
48.  .subscribe(
49.  book => {
50.  this.book = book;
51.  console.log(book);
52.  this.router.navigate(['/books']);
53.  },
54.  error => {
55.  console.log(error);
56.  });
57.  }
58.  else {
59.  this.bookService.update(this.book.id, this.book) //id exists invoke update
60.  .subscribe(
61.  book => {
62.  this.book = book;
63.  console.log(book);
64.  this.router.navigate(['/books']);
65.  },
66.  error => {
67.  console.log(error);
68.  });
69.  }
70.  }

72.  populatePublishers(): void {
73.  this.publisherService.readAll()
74.  .subscribe(
75.  publishers => {
76.  this.publishers = publishers;
77.  console.log(publishers);
78.  },
79.  error => {
80.  console.log(error);
81.  });
82.  }
83.  }

In the preceding class during initialization the id parameter is read, if it is empty, which is the case during new record creation, a new Book object is created (line 29). When the id contains a value (during the update record) the Book record is fetched via bookService on line 31. The saveBook method also makes similar distinction to invoke create or update service call, depending upon if the book.id is empty or not (line 47). The populatePublishers method fills the Publisher drop-down by reading values via the publisherService.

Add following code to book-edit.component.html:

1.  <span  class="text-danger"  *ngIf="error">{{error}}</span>
2.  <div  class="table-title">
3.  <div  class="row">
4.  <div  class="col-sm-6">
5.  <h4><b>Edit Book</b></h4>
6.  <a  href="#"  routerLink="/books"  class="btn btn-success back"><I  class="fas fa-arrow-circle-left"></I>  Back</a>
7.  </div>
8.  </div>
9.  </div>
10.  <div  *ngIf="book"  class="form-horizontal"  style="margin-top:10px;">
11.  <div  class="form-group">
12.  <label  class="col-md-3 control-label">Title: </label>
13.  <div  class="col-md-6">
14.  <input  class="form-control"  type="text"  [(ngModel)]="book.title"  />
15.  </div>
16.  </div>
17.  <div  class="form-group">
18.  <label  class="col-md-3 control-label">Price: </label>
19.  <div  class="col-md-6">
20.  <input  class="form-control"  type="number"  [(ngModel)]="book.price"  />
21.  </div>
22.  </div>
23.  <div  class="form-group">
24.  <label  class="col-md-3 control-label">Authors: </label>
25.  <div  class="col-md-6">
26.  <input  class="form-control"  type="text"  [(ngModel)]="book.authors"  />
27.  </div>
28.  </div>
29.  <div  class="form-group">
30.  <label  class=”col-md-3 control-label”>Tags: </label>
31.  <div  class="col-md-6">
32.  <input  class="form-control"  type="text"  [(ngModel)]="book.tags"  />
33.  </div>
34.  </div>
35.  <div  class="form-group">
36.  <label  class="col-md-3 control-label">Publisher: </label>
37.  <div  class="col-md-6">
38.  <select  *ngIf="publishers"  [(ngModel)]="book.publisherId"  class="form-control input-lg">
39.  <option  value="0">Select Publisher</option>
40.  <option  *ngFor="let pub of publishers"  value={{pub.id}}>{{pub.
    name}}</option>
41.  </select>
42.  </div>
43.  </div>
44.  <div  class="form-group">
45.  <label  class="col-md-3 control-label">Publish Date: </label>
46.  <div  class="col-md-6">
47.  <input  type="date"  publishDate="ngModel"  class="form-control"  placeholder="yyyy-MM-dd"
48.  [ngModel]="book.publishDate | date:'yyyy-MM-dd'"  ngModelChange)="book.publishDate=$event"  name="publishDate">
49.  </div>
50.  </div>
51.  <div  class="form-group">
52.  <div  class="col-md-offset-2 col-md-6">
53.  <button  (click)="saveBook()"  class="btn btn-primary">Save</button>
54.  </div>
55.  </div>
56.  </div>

The preceding Edit page uses the two-way binding to bind to properties of book object (created in the code behind class) such as [(ngModel)]="book.price". The saveBook method is invoked on button click on line 53\. After these changes you should be able to create and edit a book record.

[Book Delete page](#contents.xhtml_sc4_167a)

We intend to add a new option for each book record to be deleted on list page. Before deleting the record, we should ask for a confirmation from the user and proceed only if user responds with a yes. We will use Bootstrap modal dialog to ask for delete confirmation. Since Bootstrap is already part of the default template, we only need to include the highlighted line in angular.json to include the Bootstrap JavaScript objects:

1.  …
2.  "styles": [
3.  "node_modules/bootstrap/dist/css/bootstrap.min.css",
4.  "src/styles.css"
5.  ],
6.  "scripts": [

7.  "node_modules/bootstrap/dist/js/bootstrap.min.js"

8.  ]
9.  …

Include the highlighted lines in book-list.component.ts:

1.  import { Component, OnInit } from  '@angular/core';
2.  import { BookService } from  'src/app/books/book.service';
3.  import { Book } from  "../book";

5.  declare  var window: any;

7.  @Component({
8.  selector: 'app-book-list',
9.  templateUrl: './book-list.component.html',
10.  styleUrls: ['./book-list.component.css']
11.  })
12.  export  class  BookListComponent  implements  OnInit {
13.  books!: Book[];

14.  deleteModal: any;
15.  idTodelete: number = 0;
16.  titleToDelete!: string;

18.  constructor(private bookService: BookService) { }

20.  ngOnInit(): void {

21.  this.deleteModal = new window.bootstrap.Modal(
22.  document.getElementById('deleteModal')
23.  );

25.  this.readBooks();
26.  }

28.  readBooks(): void {
29.  this.bookService.readAll()
30.  .subscribe(
31.  books => {
32.  this.books = books;
33.  console.log(books);
34.  },
35.  error => {
36.  console.log(error);
37.  });
38.  }

40.  openDeleteModal(id: number, title: string) {
41.  this.idTodelete = id;
42.  this.titleToDelete = title;

44.  this.deleteModal.show();
45.  }

47.  delete() {
48.  this.bookService.delete(this.idTodelete).subscribe({
49.  next: () => {
50.  this.books = this.books.filter(_ => _.id != this.idTodelete)
51.  this.deleteModal.hide();
52.  },
53.  });
54.  }

55.  }

The modified BookListComponent class instantiates the Bootstrap modal object by using the definition of deleteModal on line 21\. The modal window is shown in the openDeleteModal method and the delete method invokes the delete API from bookService.

Add the highlighted line in book-list.component.html to include the Delete button for each book record in the book list and invoke the openDeleteModal method upon clicking, with the book id and title passed as parameters.

1.  <a  href="#"  [routerLink]="['/books/edit/', book.id]"  class="btn"><i  class="fa fa-edit edit"></i></a>

2.  <button  type="button"  (click)="openDeleteModal(book.id,book.title)"  class="btn"><i  class='fas fa-trash-alt delete'></i></button>

3.  </td>

Also include the following HTML snippet for the modal dialog at the end in book-list.component.html:

1.  <!-- Modal -->
2.  <div  class="modal fade"  id="deleteModal"  tabindex="-1"  aria-labelledby="exampleModalLabel"  aria-hidden="true">
3.  <div  class="modal-dialog">
4.  <div  class="modal-content">
5.  <div  class="modal-header">
6.  <h5  class="modal-title"  id="exampleModalLabel">Confirmation</h5>
7.  <button  type="button"  class="btn-close"  data-bs-dismiss="modal"  aria-label="Close"></button>
8.  </div>
9.  <div  class="modal-body">
10.  Do you really want to delete the book: <span  class=
    "fw-bold">{{titleToDelete}}</span>?
11.  </div>
12.  <div  class="modal-footer">
13.  <button  type="button"  class="btn btn-secondary"  data-bs-dismiss="modal">No</button>
14.  <button  type="button"  class="btn btn-danger"  (click)="delete()">Yes</button>
15.  </div>
16.  </div>
17.  </div>
18.  </div>

With these changes the book list would show the Delete button for each book record. Clicking on the Delete button would show following confirmation modal dialog and clicking on Yes will perform the deletion and take the user back to list UI:

![](images/Figure_6.21.png)

Figure 6.21: Book delete confirmation

[Unit testing](#contents.xhtml_sc3_168a)

The strategies to test an SPA application are centered around testing the server API and client application separately. The back-end web API can be unit-tested following the approach outlined for Web Apps in [Chapter 2](#ch02.xhtml): ASP .NET Core Web App. The front-end Angular application uses the Jasmine behavioral testing framework and the Karma test runner. The skeleton for such tests are generated as .spec.ts file, while creating any item using the Angular CLI. More information can be found at [https://angular.io/guide/testing](https://angular.io/guide/testing).

End-to-end functional testing can also be done using Selenium Webdriver (refer to [Chapter 2](#ch02.xhtml): ASP .NET Core Web App) or Playwright.NET (refer to [Chapter 5](#ch05.xhtml): Blazor WebAssembly)

[Deployment](#contents.xhtml_sc3_169a)

Beginning Visual Studio 2022 version 17.3, the integrated SPA that we have created in this chapter can be deployed to cloud environment such as Microsoft Azure by using the Visual Studio Publish tool. To do so, follow the detailed steps outline at [https://learn.microsoft.com/en-us/visualstudio/javascript/tutorial-asp-net-core-with-angular?view=vs-2022#publish-the-project](https://learn.microsoft.com/en-us/visualstudio/javascript/tutorial-asp-net-core-with-angular?view=vs-2022#publish-the-project).

[Conclusion](#contents.xhtml_sc2_170a)

In this chapter we have explored the option to develop Single Page Application using Angular supported by the ASP.NET Core web API. It is technically possible to use a different JavaScript framework such as React.js or Vue to develop SPA which uses ASP.NET web API at the backend.

This was last of the chapters where we have learnt to develop another variant of a web application, from the next chapter onwards, we will explore the development of Desktop applications.

[Points to remember](#contents.xhtml_sc2_171a)

*   It is possible to combine the power of ASP.NET Core backend with Angular based Single Page Application on the front-end.
*   The built-in project template ASP.NET Core with Angular in Visual Studio provides a seamless way to combine the two in a single project and execute together via a SPA Proxy. It is however possible to develop the two as separate projects too.
*   It is also possible to use React.js instead of Angular to create SPA with ASP.NET core at the back end. Visual Studio comes with ASP.NET Core with React.js template to kickstart such a development.

[Exercises](#contents.xhtml_sc2_172a)

Enhance the Angular application built in this chapter by adding the list, detail, edit and delete pages for the Publisher entity. Make use of the APIs from the PublisherController via the Angular PublisherService to create the new pages on lines of the similar pages for the Book entity.

[References](#contents.xhtml_sc2_173a)

*   Use the Angular project template with ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/client-side/spa/angular?view=aspnetcore-7.0&tabs=visual-studio](https://learn.microsoft.com/en-us/aspnet/core/client-side/spa/angular?view=aspnetcore-7.0&tabs=visual-studio)

*   Tutorial: Create an ASP.NET Core app with Angular in Visual Studio

[https://learn.microsoft.com/en-us/visualstudio/javascript/tutorial-asp-net-core-with-angular?view=vs-2022](https://learn.microsoft.com/en-us/visualstudio/javascript/tutorial-asp-net-core-with-angular?view=vs-2022)

*   Workspace and project file structure

[https://angular.io/guide/file-structure](https://angular.io/guide/file-structure)

*   Overview of Single Page Applications (SPA) in ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/client-side/spa/intro?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/client-side/spa/intro?view=aspnetcore-7.0)

*   Feature modules

[https://angular.io/guide/feature-modules](https://angular.io/guide/feature-modules)

*   Host and deploy ASP.NET Core

[https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/?view=aspnetcore-7.0)

# [CHAPTER 7WPF Application](#contents.xhtml_ch07a)

[Introduction](#contents.xhtml_sc2_174a)

We begin our exploration of the Microsoft’s desktop applications starting with Windows Presentation Foundation (WPF) in this chapter. We will understand the different types of Desktop Applications that can be created and where WPF fits in the overall strategy. This will be followed by understanding the basic structure of a WPF application before creating a real-world application end-to-end.

[Structure](#contents.xhtml_sc2_175a)

This chapter has the following topics:

*   Desktop applications
*   WPF
*   Pre-requisites
*   Getting started with WPF app
    *   Structure of the (default) WPF application project
*   Extending the default application – Custom Pizza Order form
*   Developing real-world WPF App
    *   Creating the Sudoku Buddy WPF app
        *   Getting started
        *   Creating the Sudoku UI
        *   Implementing MVVM to show numbers.
            *   What is Model-View-ViewModel (or MVVM)?
            *   Implementing MVVM
        *   Show candidates or pencil marks.
        *   Allowing user to type digit.
        *   Highlighting incorrect input.
    *   Unit testing
    *   Deployment

[Objectives](#contents.xhtml_sc2_176a)

The objective of this chapter is to understand the concepts around WPF application and to create one step-by-step using C# 11 and .NET 7.0 in Visual Studio 2022.

[Desktop applications](#contents.xhtml_sc2_177a)

Desktop applications are software programs that run locally on personal computer or laptop. Unlike web-based applications which are accessible from a browser, a desktop application requires installation, after which it can be launched via an executable file running stand-alone on the device. They are also different from mobile applications that run on smartphones and tablet devices. Running natively on a device, the desktop applications are relevant even today, as the user-experience and performance that they bring in is hard to replace by any other application type. There are several application areas which are well suited for desktop applications such as standalone business applications (Word, Excel, Outlook), collaborative application (Zoom, Meet), IDE (Visual Studio, VS Code), multimedia applications (Media Player) and so on.

Microsoft offers a wide range of options to build desktop apps targeting Windows only or cross-platform: Windows, Linux and MacOS. [Figure 7.1](#ch07.xhtml_fig7-1) given below summarizes the popular choices available today to create desktop applications:

![](images/Figure_7.1.png)

Figure 7.1: UI framework options for desktop apps

This includes UI frameworks created by other companies to create cross-platform applications that use C# and .NET.

This chapter focuses on WPF applications. In the next chapter we will work with WinUI applications followed by examining the cross-platform option of .NET MAUI in the chapter after that.

[WPF](#contents.xhtml_sc2_178a)

The WPF framework was first released in 2006 as part of .NET Framework 3.0, with the code name Avalon. It was developed with the goal of providing an option to create visually appealing desktop client applications as an alternative to Windows Forms. Over the years it has undergone several enhancement including becoming open source in 2018, supporting .NET Core with a goal of having parity with the .NET Framework version. Over time, the two WPF implementations may diverge.

WPF uses DirectX and provides a consistent programming model for building applications allowing for efficient hardware and software rendering. The high-level architecture of WPF is shown in [Figure 7.2](#ch07.xhtml_fig7-2):

![](images/Figure_7.2.png)

Figure 7.2: WPF architecture

WPF provides a declarative model for application programming favoring a clear separation between UI and code. XML-based Extensible Application Markup Language (XAML) implements an application's appearance in terms of windows, dialog boxes, pages, and user controls; to fill them with controls, shapes, and graphics. The UI interacts with the corresponding code-behind file *.xaml.cs which implements the functionality that responds to user interactions.

XAML offers such capabilities like templating, styling, and binding, which are suited for building large applications. The XAML designer in Visual Studio and Blend for Visual Studio provides a visual interface to help design XAML-based apps. Both IDE share a common set of features, Blend for Visual Studio provides additional tools for designing visual states and creating animations. It is possible to switch back and forth between Visual Studio and Blend for Visual Studio, and the same project can be opened in both the IDEs at the same time.

[Pre-requisites](#contents.xhtml_sc2_179a)

Visual Studio 2022 Community Edition version 17.4 or later along with the .NET desktop development workload is needed to work through the examples in this chapter.

[Getting started with WPF Application](#contents.xhtml_sc2_180a)

Create a new WPF application project by following the steps in Visual Studio 2022, given below in [Table 7.1](#ch07.xhtml_tab7-1):

| New project creation (File &#124; New &#124; Project…) |
|  
1.  Create a new project

 |  
1.  Narrow down the list of templates being shown by selecting, Language: C#, Platform: All platforms, Project type: Desktop.
2.  Select template: WPF Application
3.  Click Next

 |
|  
*   B. Configure your new project

 |  
4.  Project name: Enter name of your choice such as FirstWpfApp.
5.  Location: Select location of choice
6.  Solution: Select either Add to solution  or Create new solution
7.  Solution name: Provide name in case a new solution is created.
8.  Place solution and project in the same directory: Normally we keep the solution a level higher so leave it unchecked in case a new solution is created.
9.  Click Next

 |
|  
*   C. Additional information

 |  
10.  Framework: .NET 7.0 (Standard Term Support)
11.  Click Create

 |

Table 7.1: Steps to create a new WPF application project.

The new project can be created using dotnet command line interface (CLI) with the following command:

dotnet new  angular --name FirstAngularApp

And to add the newly created project to the solution:

dotnet sln  add ./FirstAngularApp/FirstAngularApp.csproj

[Structure of the (default) WPF Application project](#contents.xhtml_sc3_181a)

On creating the new application using the built-in WPF Application template, the following files as shown in [Table 7.2](#ch07.xhtml_tab7-2) are created:

| Dependencies &#124; Frameworks | By default, there is a dependency on Microsoft.NETCore.App and Microsoft.WindowsDesktop.App.WPF |
| App.xaml and App.xaml.cs | This combination of markup (.xaml) and code-behind (.xaml.cs) is the entry point of the application. |
| AssemblyInfo.cs | This contains information about the assembly. For the default WPF app, it specifies the location of XAML resources for the Theme used in the application. |
| MainWindow.xaml and MainWindow.xaml.cs | This is the combination of the UI and the interaction logic of the main application window. |

Table 7.2: Important files in a WPF application project

The project shows up in the Solution Explorer as follows in [Figure 7.3](#ch07.xhtml_fig7-3):

![](images/Figure_7.3.png)

Figure 7.3: Files in default WPF app

Let us examine the contents of some of the files:

App.xaml

1.  <Application x:Class="FirstWpfApp.App"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:local="clr-namespace:FirstWpfApp"
5.  StartupUri="MainWindow.xaml">
6.  <Application.Resources>

8.  </Application.Resources>
9.  </Application>

App.xaml is the declarative starting point of the application. The StartupUri property on line 5 indicates which Window or Page to start up when the application is launched. In this case, MainWindow.xaml will be started. The major purpose for App.xaml is holding resources (style, pens, brushes, and so on.) that could be available through-out the application.

App.xaml.cs

1.  using System.Windows;

3.  namespace FirstWpfApp;
4.  ///  <summary>
5.  /// Interaction logic for App.xaml
6.  ///  </summary>
7.  public  partial  class  App : Application
8.  {
9.  }

The preceding code declares the code-behind App partial class, which extends the Application class. It can contain the startup instructions before instantiating a window or page.

MainWindow.xaml

1.  <Window x:Class="FirstWpfApp.MainWindow"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
5.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
6.  xmlns:local="clr-namespace:FirstWpfApp"
7.  mc:Ignorable="d"
8.  Title="MainWindow" Height="450" Width="800">
9.  <Grid>

11.  </Grid>
12.  </Window>

In the preceding XAML markup, the document root Window represents the type of object being described by the XAML file. The Window component is tied to the code-behind class specified in the x:Class attribute. Between lines 2 and 5, the XML construct xmlns (with qualifiers such as x, d, mc) defines namespaces to resolve XML elements. The main xmlns namespace, defined without a qualifier, defines the default namespace by which an XML element name should be resolved. The xmlns:local namespace, on line 6, declares the local prefix and maps to the objects declared by the project in the Names code namespace. Line 7 sets d: prefix as a mark for attributes used in design and ignored after standard program compilation. On line 8, the title of the window and the default height and width are set.

MainWindow.xaml.cs

1.  using System.Windows;

3.  namespace FirstWpfApp;
4.  ///  <summary>
5.  /// Interaction logic for MainWindow.xaml
6.  ///  </summary>
7.  public  partial  class  MainWindow : Window
8.  {
9.  public  MainWindow()
10.  {
11.  InitializeComponent();
12.  }
13.  }

As the code-behind class for the MainWindow Window element, this must inherit from the Window class (line 7). InitializeComponent is called from the constructor to merge the UI that is defined in markup with the code-behind class. The combination of x:Class in the XAML file and InitializeComponent ensures that your implementation is correctly initialized whenever it is created. If we view the definition of InitializeComponent, the following auto-generated code can be seen:

1.  ///  <summary>
2.  /// InitializeComponent
3.  ///  </summary>
4.  [System.Diagnostics.DebuggerNonUserCodeAttribute()]
5.  [System.CodeDom.Compiler. GeneratedCodeAttribute("PresentationBuildTasks", "7.0.4.0")]
6.  public  void InitializeComponent() {
7.  if (_contentLoaded) {
8.  return;
9.  }
10.  _contentLoaded = true;
11.  System.Uri resourceLocater = new System.Uri("/FirstWpfApp;V1.0.0.0;component/mainwindow.xaml", System.UriKind.Relative);

13.  #line 1 "..\..\..\MainWindow.xaml"
14.  System.Windows.Application.LoadComponent(this, resourceLocater);

16.  #line  default
17.  #line  hidden
18.  }

As seen on line 11 and 12, the Windows component is loaded by reading the corresponding UI definition from the XAML file.

FirstWpfApp.csproj

1.  <Project  Sdk="Microsoft.NET.Sdk">

3.  <PropertyGroup>
4.  <OutputType>WinExe</OutputType>
5.  <TargetFramework>net7.0-windows</TargetFramework>
6.  <Nullable>enable</Nullable>
7.  <UseWPF>true</UseWPF>
8.  </PropertyGroup>

10.  </Project>

The preceding project file is in the latest .NET SDK format. The WinExe option for the OutputType causes the compiler to create an executable (EXE) Windows program. Since WPF is supported only on Windows, the Target Framework Moniker (TFM) is windows specific net7.0-windows, which inherits every API available to their base TFM (net7.0). The additional Windows-specific bindings for WPF UseWPF is set to true to import and use WPF.

[Custom Pizza Order form](#contents.xhtml_sc2_182a)

To understand the controls and layout, we will extend the default FirstWpfApp by adding a simple custom pizza order form which when completed, will appear as shown in [Figure 7.4](#ch07.xhtml_fig7-4):

![](images/Figure_7.4.png)

Figure 7.4: Completed Custom Pizza Order form

Start by adding a new WPF Window named CustomPizzaOrder.xaml to the current project. By default, the WPF Window uses the Grid layout control, which defines rows and columns, and places controls within a specific cell given by zero-based row and column coordinates combination. To create the Custom Pizza Order form, we need two columns and eight rows. Let us start by adding the following in the XAML code editor. Change the title of the window and the startup height and width as shown in the highlighted code:

1.  <Window x:Class="FirstWpfApp.CustomPizzaOrder"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
5.  xmlns:mc="http://schemas.openxmlformats.org/markup-
    compatibility/2006"
6.  xmlns:local="clr-namespace:FirstWpfApp"
7.  mc:Ignorable="d"

8.  Title="Custom Pizza Order" Height="340" Width="330">
9.  <Grid ShowGridLines="True">
10.  <Grid.ColumnDefinitions>
11.  <ColumnDefinition  />
12.  <ColumnDefinition />
13.  </Grid.ColumnDefinitions>
14.  <Grid.RowDefinitions>
15.  <RowDefinition />
16.  <RowDefinition />
17.  <RowDefinition />
18.  <RowDefinition />
19.  <RowDefinition />
20.  <RowDefinition />
21.  <RowDefinition />
22.  <RowDefinition />
23.  </Grid.RowDefinitions>

24.  </Grid>
25.  </Window>

With the preceding code, the rows and the columns appear as following in the XAML designer due to the ShowGridLines attribute set to true for Grid on line 9. Refer [Figure 7.5](#ch07.xhtml_fig7-5) given as follows:

![](images/Figure_7.5.png)

Figure 7.5: Initial rows and columns in the Custom Pizza Order form

Now we will add the controls in each row one by one. In WPF, there are two ways to lay out controls on a window. In absolute positioning we specify the exact location of child elements within their containers while in dynamic positioning, we only specify how they should be arranged and how they should wrap relative to their parent. With absolute positioning the child elements do not move when the parent element is resized but in dynamic layout, the child controls move relative to the parent. For most situations dynamic layouts is the flexible and preferred method. Dynamic layouts allow the content to adapt to different screen sizes, localization and other content changes. Absolute layouts are reserved for cases when precise and unchanging positioning of elements is important. For this reason, we almost never drag and drop control from the Toolbox on to the XAML designer but rather edit directly in the XAML code or change the properties via property window.

Add the pair of Label and Textbox below the closing tag </Grid.RowDefinitions> as follows:

1.  <!-- Name field -->
2.  <Label Grid.Row="0" Grid.Column="0" Content="Your Name: " />
3.  <TextBox x:Name="Name" Grid.Row="0" Grid.Column="1"
4.  Margin="5" Background="LightYellow" VerticalContentAlignment="Center"  />

With this, the Label will come in the first cell and the Textbox in the cell adjacent to it as shown below in [Figure 7.6](#ch07.xhtml_fig7-6):

![](images/Figure_7.6.png)

Figure 7.6: Adding Name field in first row

To give more space to the second column, we will reduce the width of first by making it Auto, which shrinks it to the width of the label. We will also add styles to apply to Grid and Label in the Window.Resources tag as shown in the highlighted snippet:

1.  …  
2.  mc:Ignorable="d"
3.  Title="Custom Pizza Order" Height="340" Width="330">

4.  <Window.Resources>
5.  <Style TargetType="Grid">
6.  <Setter Property="ShowGridLines" Value="True"/>
7.  <Setter Property="Margin" Value="5"/>
8.  <Setter Property="Background" Value="LightSteelBlue" />
9.  </Style>
10.  <Style TargetType="Label">
11.  <Setter Property="Background" Value="LightGray" />
12.  <Setter Property="Margin" Value="5"/>
13.  <Setter Property="HorizontalContentAlignment" Value="Right"/>
14.  <Setter Property="VerticalContentAlignment" Value="Center"/>
15.  </Style>
16.  </Window.Resources>
17.  <Grid>

18.  <Grid.ColumnDefinitions>

19.  <ColumnDefinition Width="Auto" />

20.  <ColumnDefinition />
21.  </Grid.ColumnDefinitions>
22.  <Grid.RowDefinitions>
23.  …

The Style tag defines the appearance for all the Grid and the Label controls and line 19 sets the column width to Auto. Without setting explicitly, the width is set to * which means the available width is evenly spread between the columns or rows. This makes the form look as follows in [Figure 7.7](#ch07.xhtml_fig7-7):

![](images/Figure_7.7.png)

Figure 7.7: Adjust columns and apply styles

Next, we will add the Size  field with the RadioButton options. Add the following code below the Name field:

1.  <!-- Size field -->
2.  <Label Grid.Row="1" Grid.Column="0" Content="Size: " />
3.  <Grid Grid.Row="1" Grid.Column="1" VerticalAlignment="Center">
4.  <Grid.ColumnDefinitions>
5.  <ColumnDefinition Width="Auto"/>
6.  <ColumnDefinition/>
7.  <ColumnDefinition Width="Auto"/>
8.  </Grid.ColumnDefinitions>
9.  <RadioButton x:Name="SizeRegular" Grid.Column="0" Content="Regular" />
10.  <RadioButton x:Name="SizeMedium" Grid.Column="1" HorizontalAlignment="Center" Content="Medium" />
11.  <RadioButton x:Name="SizeLarge" Grid.Column="2" Content="Large" />
12.  </Grid>

The three radio buttons are added inside a Grid in the first row and first column of the parent Grid (line 3). This is done to align the three radio buttons horizontally instead of the default vertical layout. With this change the form appears as shown in [Figure 7.8](#ch07.xhtml_fig7-8):

![](images/Figure_7.8.png)

Figure 7.8: Added Size radio buttons

Next, add the following code to introduce the Crust drop-down box:

1.  <!-- Crust field -->
2.  <Label Grid.Row="2" Grid.Column="0" Content="Crust: " />
3.  <ComboBox x:Name="Crust" Grid.Row="2" Grid.Column="1"
4.  VerticalContentAlignment="Center" Margin="5" Background="LightYellow"  >
5.  <ComboBoxItem IsSelected="True" >-- Select --</ComboBoxItem>
6.  <ComboBoxItem>New Hand Tossed</ComboBoxItem>
7.  <ComboBoxItem>Wheat Thin Crust</ComboBoxItem>
8.  <ComboBoxItem>Cheese Burst</ComboBoxItem>
9.  <ComboBoxItem>Fresh Pan Pizza</ComboBoxItem>
10.  </ComboBox>

With the preceding code we have added a ComboBox with the different values provided in the XAML code itself. This is the static way of providing content for the control. The UI appears with this change as shown in [Figure 7.9](#ch07.xhtml_fig7-9):

![](images/Figure_7.9.png)

Figure 7.9: Added Crust combo box

Next, we will see an example of dynamic binding with the Toppings field. Here we will need to provide the functionality to multi-select from a list of possible topping values. We will make use of the Check Combo Box control from a third-party WPF control library. Add NuGet package Extended WPF Toolkit by Xceed. Also add the highlighted line to reference the library.

1.  xmlns:local="clr-namespace:FirstWpfApp"

2.  xmlns:wpfx="http://schemas.xceed.com/wpf/xaml/toolkit"

3.  mc:Ignorable="d"

Now add the following snippet after the Crust field:

1.  <!-- Toppings field -->
2.  <Label Grid.Row="3" Grid.Column="0" Content="Toppings: " />
3.  <wpfx:CheckComboBox x:Name="Toppings" Grid.Row="3" Grid.Column="1"
4.  Margin="5" />

Include the following line in the code-behind file CustomPizzaOrder.xaml.cs to populate the combo-box from code as shown below:

1.  public  CustomPizzaOrder()
2.  {
3.  InitializeComponent();

4.  Toppings.ItemsSource = new  List<string>
5.  {
6.  "Grilled Mushrooms", "Onion", "Crisp Capsicum", "Fresh Tomato",
7.  "Paneer", "Red Pepper", "Jalapeno","Black Olives"
8.  };

9.  }

Before seeing the window in action, we must set the StartupUri in App.xaml to CustomPizzaOrder.xaml. Running the project now should show the following UI in [Figure 7.10](#ch07.xhtml_fig7-10):

![](images/Figure_7.10.png)

Figure 7.10: Added Toppings multi-select combo-box

The multi-select drop-down can be seen in action, the selected options are displayed in text property. Notice the little debugging application toolbar at the window title, this appears only when executing the application from Visual Studio and has different options to view the code for debugging purposes. This bar will not appear when the project’s executable is run.

Add the three remaining fields and the two buttons by including the following snippet:

1.  <!-- Extra spicy field -->
2.  <Label Grid.Row="4" Grid.Column="0" Content="Extra Spicy: " />
3.  <CheckBox x:Name="Spicy" Grid.Row="4" Grid.Column="1"
4.  HorizontalAlignment="Left" VerticalAlignment="Center" Margin="5" />

6.  <!-- Quantity field -->
7.  <Label Grid.Row="5" Grid.Column="0" Content="Quantity: " />
8.  <wpfx:IntegerUpDown x:Name="Quantity" Grid.Row="5" Grid.Column="1"
9.  Margin="5" Minimum="0" Text="0" Background="LightGoldenrodYellow" />

11.  <!-- Delivery date field -->
12.  <Label Grid.Row="6" Grid.Column="0" Content="Order Date: " />
13.  <wpfx:DateTimePicker x:Name="Date" Grid.Row="6" Grid.Column="1"
14.  Margin="5" Background="LightGoldenrodYellow"/>

16.  <!-- Buttons -->
17.  <Button x:Name="PlaceOrder" Grid.Row="7" Grid.Column="1" Content="Place Order" />
18.  <Button x:Name="Reset" Grid.Row="7" Grid.Column="0" Content="Reset" />

The UI appears in [Figure 7.11](#ch07.xhtml_fig7-11) as follows:

![](images/Figure_7.11.png)

Figure 7.11: Added remaining controls

Add margin around the buttons by including the following style within Window.Resources:

1.  <Style TargetType="Button">
2.  <Setter Property="Margin" Value="5"/>
3.  </Style>

Next, we will add the functionality in the code-behind file for each of the buttons. In the XAML design, double-click each button one by one to include the event handler skeletons in the code behind file and see the Click attribute get added to the buttons as follows:

1.  <Button x:Name="PlaceOrder" Grid.Row="7" Grid.Column="1" Content="Place Order" Click="PlaceOrder_Click" />
2.  <Button x:Name="Reset" Grid.Row="7" Grid.Column="0" Content="Reset" Click="Reset_Click" />

Add the code to the newly added method skeletons in the code-behind file.

1.  private  void  Reset_Click(object sender, RoutedEventArgs e)
2.  {
3.  Name.Text = string.Empty;

5.  SizeRegular.IsChecked = false;
6.  SizeMedium.IsChecked = false;
7.  SizeLarge.IsChecked = false;

9.  Crust.SelectedIndex = 0;
10.  Toppings.SelectedItems.Clear();
11.  Toppings.Text = "-- Select --";
12.  Spicy.IsChecked = false;
13.  Quantity.Text = "0";
14.  Date.Value = DateTime.Now;
15.  }

17.  private  void  PlaceOrder_Click(object sender, RoutedEventArgs e)
18.  {
19.  var spicyText = Spicy.IsChecked.Value ? " Extra Spicy," : " ";

21.  var sizeText = SizeRegular.IsChecked.Value ? SizeRegular.Content :
22.  SizeMedium.IsChecked.Value ? SizeMedium.Content :
23.  SizeLarge.IsChecked.Value ? SizeLarge.Content : "";

25.  var message = $"{Quantity.Text}{spicyText} {sizeText} sized pizza ordered for {Name.Text} on {Date.Text} with following toppings: {Toppings.Text}";

27.  MessageBox.Show(message, "Customize Pizza", MessageBoxButton.OK, MessageBoxImage.Information);
28.  }

Invoke the Reset_Click method from the constructor to do the first-time initialization.

1.  public  CustomPizzaOrder()
2.  {
3.  InitializeComponent();
4.  Toppings.ItemsSource = new  List<string>
5.  {
6.  "Grilled Mushrooms", "Onion", "Crisp Capsicum", "Fresh Tomato",
7.  "Paneer", "Red Pepper", "Jalapeno","Black Olives"
8.  };

10.  Reset_Click(null, null);

10.  }

With changes now complete, you may also set the ShowGridLines property for Grid in the Styles to false. Running the form shows up as follows. Fill the details and click on Place Order button to view the message box. Refer to [Figure 7.12](#ch07.xhtml_fig7-12) for the completed order form:

![](images/Figure_7.12.png)

Figure 7.12: Completed order form

[Developing real-world WPF app](#contents.xhtml_sc2_183a)

To understand the concepts around building a real world WPF application, we will create a simple application around the popular game of Sudoku. We will create the traditional 9x9 grid of Sudoku where a user can enter the digits. Along with the digits, the application will also show the possible candidates or pencil marks in each cell. User will also be alerted when an incorrect number is entered in any of the cells which does not conform to the rules of the game. This way the application helps the user to play a game of Sudoku without giving away too many clues. For this reason, we are calling this application Sudoku Buddy.

[Creating the Sudoku Buddy WPF application](#contents.xhtml_sc3_184a)

As a refresher, the main motive of a game of Sudoku, having a 9x9 grid, is to fill numbers from 1 to 9 in every cell such that each digit is unique in a unit. A unit comprises of a row, a column or a 3x3 box of 9 digits each. The game begins with a partially filled grid and the user is supposed to fill rest of the numbers. When fully built, the UI of the application would appear as follows in [Figure 7.13](#ch07.xhtml_fig7-13):

![](images/Figure_7.13.png)

Figure 7.13: Final UI of Sudoku Buddy application

[Getting started](#contents.xhtml_sc4_185a)

Create a new project named SudokuBuddy using the WPF  Application  template by choosing all the default options as described for the FirstWPFApp application earlier. The goal of this application is to demonstrate the various design choices for a real-world WPF application. So, we will make use of User Controls to design the UI, implement Model-View-ViewModel (MVVM) pattern, write unit-tests, make use of resource dictionaries, and finally publish the application. But first, we will get the UI of Sudoku grid by breaking apart into constituent User Controls.

[Creating the Sudoku UI](#contents.xhtml_sc4_186a)

There are several variations to the game of Sudoku, but the classic version is a 9x9 grid of numbers, which is grouped into 9 rows, 9 columns and 9 boxes; each having 9 cells as shown below in [Figure 7.14](#ch07.xhtml_fig7-14):

![](images/Figure_7.14.png)

Figure 7.14: Classic 9x9 Sudoku grid

For ease of management and simplifying the code, we will create three User Controls. Sudoku is composed of 9 Boxes, each of which in turn is composed of 9 Cells each. When it comes to creating reusable controls there are two options in WPF – custom control or user control. Custom control extends existing controls with additional capabilities along with support for theming. User control composes multiple existing controls into a reusable group, and they do not support theming. Because of several overlapping capabilities, user controls is a simpler option to try when the purpose is to reuse within your own application. However, if the goal is to create a third-party library of controls, custom controls are better suited because of their flexibility and styling capabilities.

Create a new folder named Controls and one by one add three User Control named SudokuView, BoxView and CellView by right clicking the folder and choosing Add | User Control (WPF) option. The convention to use View as a suffix in the User Control names will become evident in subsequent section. It may be a good idea to run the code clean-up on the project. To get rid of those extra using statements in the code-behind files, right click on the project and select Analyze and Code Cleanup | Run Code Cleanup (Profile 1). To create the Sudoku grid, make following changes in the XAML files:

MainWindow.xaml

1.  <Window x:Class="SudokuBuddy.MainWindow"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
5.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
6.  xmlns:local="clr-namespace:SudokuBuddy.Controls"
7.  mc:Ignorable="d"
8.  Title="Sudoku Buddy" Height="450" Width="450" ResizeMode="NoResize">
9.  <Grid>
10.  <local:SudokuView />
11.  </Grid>
12.  </Window>

The preceding code includes the SudokuView control on line 10\. With this, the Sudoku grid should appear in the starting main window.

SudokuView.xaml

1.  <UserControl x:Class="SudokuBuddy.Controls.SudokuView"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
5.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
6.  xmlns:local="clr-namespace:SudokuBuddy.Controls"
7.  mc:Ignorable="d">
8.  <Grid>
9.  <Grid.ColumnDefinitions>
10.  <ColumnDefinition />
11.  <ColumnDefinition />
12.  <ColumnDefinition />
13.  </Grid.ColumnDefinitions>
14.  <Grid.RowDefinitions>
15.  <RowDefinition />
16.  <RowDefinition />
17.  <RowDefinition />
18.  </Grid.RowDefinitions>
19.  <local:BoxView Grid.Column="0" Grid.Row="0" />
20.  <local:BoxView Grid.Column="1" Grid.Row="0" />
21.  <local:BoxView Grid.Column="2" Grid.Row="0" />
22.  <local:BoxView Grid.Column="0" Grid.Row="1" />
23.  <local:BoxView Grid.Column="1" Grid.Row="1" />
24.  <local:BoxView Grid.Column="2" Grid.Row="1" />
25.  <local:BoxView Grid.Column="0" Grid.Row="2" />
26.  <local:BoxView Grid.Column="1" Grid.Row="2" />
27.  <local:BoxView Grid.Column="2" Grid.Row="2" />
28.  </Grid>
29.  </UserControl>

SudokuView is the top-most level of the Sudoku grid. It comprises of 9 boxes. In the preceding code, we are laying out the BoxView control from line 19 to 27 within specified coordinates, in a 3x3 grid defined between lines 9 and 18.

BoxView.xaml

1.  <UserControl x:Class="SudokuBuddy.Controls.BoxView"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-
    compatibility/2006"
5.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
6.  xmlns:local="clr-namespace:SudokuBuddy.Controls"
7.  mc:Ignorable="d">
8.  <Border BorderBrush="Black" BorderThickness="1">
9.  <Grid>
10.  <Grid.ColumnDefinitions>
11.  <ColumnDefinition />
12.  <ColumnDefinition />
13.  <ColumnDefinition />
14.  </Grid.ColumnDefinitions>
15.  <Grid.RowDefinitions>
16.  <RowDefinition />
17.  <RowDefinition />
18.  <RowDefinition />
19.  </Grid.RowDefinitions>
20.  <local:CellView Grid.Column="0" Grid.Row="0" />
21.  <local:CellView Grid.Column="1" Grid.Row="0" />
22.  <local:CellView Grid.Column="2" Grid.Row="0" />
23.  <local:CellView Grid.Column="0" Grid.Row="1" />
24.  <local:CellView Grid.Column="1" Grid.Row="1" />
25.  <local:CellView Grid.Column="2" Grid.Row="1" />
26.  <local:CellView Grid.Column="0" Grid.Row="2" />
27.  <local:CellView Grid.Column="1" Grid.Row="2" />
28.  <local:CellView Grid.Column="2" Grid.Row="2" />
29.  </Grid>
30.  </Border>
31.  </UserControl>

Like SudokuView, BoxView control comprises of 9 CellView controls laid out in a 3x3 grid in the preceding code.

CellView.xaml

1.  <UserControl x:Class="SudokuBuddy.Controls.CellView"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-
    compatibility/2006"
5.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
6.  mc:Ignorable="d">
7.  <Border BorderBrush="Black" BorderThickness="1">
8.  <Grid>
9.  <TextBlock  />
10.  <ItemsControl>
11.  <ItemsControl.ItemsPanel>
12.  <ItemsPanelTemplate>
13.  <UniformGrid Rows="3" Columns="3"/>
14.  </ItemsPanelTemplate>
15.  </ItemsControl.ItemsPanel>
16.  <ItemsControl.ItemTemplate>
17.  <DataTemplate>
18.  <TextBlock />
19.  </DataTemplate>
20.  </ItemsControl.ItemTemplate>
21.  </ItemsControl>
22.  </Grid>
23.  </Border>
24.  </UserControl>

The CellView represents the individual cell in a Sudoku grid. The cell either shows a digit or the candidates (pencil marks). The code on line 9 is to show the digit and the code from line 10 to 21 is to show the candidates in a 3x3 built-in Uniform Grid control.

Set the project as the startup project and then run it. The resulting UI should show the empty Sudoku grid in [Figure 7.15](#ch07.xhtml_fig7-15) as follows:

![](images/Figure_7.15.png)

Figure 7.15: Empty Sudoku grid

[Implementing MVVM to show numbers](#contents.xhtml_sc4_187a)

In the Sudoku Buddy application, we will store the numbers corresponding to each of the 81 grid cells in a two-dimensional byte array. When the user types a digit into any cell in the WPF window, we should be able to update our number data-structure. Also, after performing such an update, we need to verify that the input follows the rules of the games (along with flagging if it does not) and re-calculate the possible candidates in all the affected cells. After doing these calculations, the same needs to be communicated back to the UI. Likewise, when the user clicks on the Clear button, the UI action must lead to an initialization of our grid data-structure and update the UI accordingly. Therefore, we can see that there are two distinct entities, one is the UI and the other is the in-memory copy of the Sudoku grid. There is a requirement to keep them in sync through all the user actions. It is possible to write our own event handling code to maintain the synchronization (like we did for the Custom Pizza Order form) but the recommended approach for a real-life application is to implement the MVVM pattern. Let us first understand what MVVM is, before going on to implementing it for the Sudoku Buddy application.

[What is Model-View-ViewModel?](#contents.xhtml_sc4_188a)

MVVM stands for Model-View-ViewModel, which is a software design pattern that helps developers organize and structure their code, to write maintainable, testable, and extensible applications. It separates the program logic and user interface controls, making it easier to develop, update, and reuse code. The pattern consists of three components: the Model, which holds the data and has no knowledge of the View or ViewModel; the View, which is the user interface that displays the data; and the ViewModel, which acts as a mediator between the Model and the View. The ViewModel exposes the data from the Model to the View and provides commands to update the Model. Refer to [Figure 7.16](#ch07.xhtml_fig7-16) as follows:

![](images/Figure_7.16.png)

Figure 7.16: Components of MVVM

The MVVM pattern is commonly used in XAML-based applications which offer a rich binding mechanism such as WPF, Web UI and MAUI applications, helping reduce code complexity and maintain a clean and reusable structure of code which is easy to unit-test also.

There are several frameworks that can help implement MVVM in your application: Prism, MVVM Cross and Catel, to name a few. We will use Microsoft’s .NET  Community  MVVM  Toolkit whose latest version 8.0 (released in 2022) introduces the feature of Source Generators. This provides a declarative syntax to define the various elements of MVVM, generating the necessary glue code in the background using Reflection and thereby reducing the repetitive boilerplate code required to implement the MVVM architecture.

[Implementing MVVM](#contents.xhtml_sc4_189a)

Create the model class SudokuGrid.cs within Models folder with the following code:

1.  using System.Collections.Generic;

3.  namespace SudokuBuddy.Models;
4.  public  class  SudokuGrid
5.  {
6.  public  SudokuGrid()
7.  {
8.  Data = new  byte[9, 9];
9.  Candidates = new  List<string>[9, 9];
10.  }
11.  public  byte[,] Data { get; }
12.  public  List<string>[,] Candidates { get; set; }
13.  public  byte[] AsLinearArray
14.  {
15.  set
16.  {
17.  for (int i = 0; i < 9; i++)
18.  {
19.  for (int j = 0; j < 9; j++)
20.  {
21.  Data[i, j] = value[i * 9 + j];
22.  }
23.  }
24.  }
25.  }
26.  }

The SudokuGrid class in the preceding code declares two, two-dimensional array properties to store grid numbers and the respective candidates. The AsLinearArray setter helps in reading values into the two-dimensional grid from a linear array of values.

Add the NuGet package CommunityToolkit.Mvvm by Microsoft. Now, under ViewModels folder create three (view model) classes – CellViewModel, BoxViewModel and SudokuViewModel with the following code:

CellViewModel.cs

1.  using CommunityToolkit.Mvvm.ComponentModel;
2.  using System;
3.  using System.Windows;

5.  namespace SudokuBuddy.ViewModels;

7.  public  partial  class  CellViewModel : ObservableObject
8.  {
9.  [ObservableProperty]
10.  string _digit;

12.  [ObservableProperty]
13.  string[] _candidates;

15.  [ObservableProperty]
16.  bool _hasError;

18.  public  CellViewModel()
19.  {
20.  Candidates = Array.Empty<string>();
21.  }
22.  public  int Row { get; set; }
23.  public  int Column { get; set; }

25.  public  BoxViewModel ParentBoxViewModel { get; set; }

27.  public  Visibility CandidatesVisibility { get; set; } = Visibility.Hidden;
28.  }

The CellViewModel class (which must be declared as a partial class) inherits from ObservableObject, provided by MVVM Toolkit. The ObservableObject implements INotifyPropertyChanged and INotifyPropertyChanging along with helper methods for setting properties and raising changes. It handles all the logic needed for raising change notifications by using the SetProperty method in the property setters.

The source generator creates observable properties behind the scenes for the private fields, starting with underscore and a letter in small case, marked with ObservableProperty. This makes it possible to work with Candidates on line 20.

BoxViewModel.cs

1.  using CommunityToolkit.Mvvm.ComponentModel;
2.  using System.Collections.ObjectModel;

4.  namespace SudokuBuddy.ViewModels;

6.  [INotifyPropertyChanged]
7.  public  partial  class  BoxViewModel : ObservableObject
8.  {
9.  [ObservableProperty]
10.  ObservableCollection<CellViewModel> _cells;

12.  public  BoxViewModel()
13.  {
14.  Cells = new  ObservableCollection<CellViewModel>();
15.  }

17.  public  SudokuViewModel ParentSudokuViewModel { get; set; }
18.  }

SudokuViewModel.cs

1.  using CommunityToolkit.Mvvm.ComponentModel;
2.  using CommunityToolkit.Mvvm.Input;
3.  using SudokuBuddy.Models;
4.  using System.Collections.ObjectModel;

6.  namespace SudokuBuddy.ViewModels;

8.  public  partial  class  SudokuViewModel : ObservableObject
9.  {
10.  public  SudokuGrid SudokuBoard;

12.  [ObservableProperty]
13.  ObservableCollection<BoxViewModel> _boxes;

15.  public  SudokuViewModel()
16.  {
17.  Initialize();
18.  }

20.  public  SudokuViewModel(SudokuGrid sudokuBoard)
21.  {
22.  Initialize(sudokuBoard);
23.  }

25.  [RelayCommand]
26.  void  LoadSample()
27.  {
28.  var grid = new  SudokuGrid
29.  {
30.  AsLinearArray = new  byte[81]
31.  {
32.  5, 3, 0, 0, 7, 0, 0, 0, 0,
33.  6, 0, 0, 1, 9, 5, 0, 0, 0,
34.  0, 9, 8, 0, 0, 0, 0, 6, 0,
35.  8, 0, 0, 0, 6, 0, 0, 0, 3,
36.  4, 0, 0, 8, 0, 3, 0, 0, 1,
37.  7, 0, 0, 0, 2, 0, 0, 0, 6,
38.  0, 6, 0, 0, 0, 0, 2, 8, 0,
39.  0, 0, 0, 4, 1, 9, 0, 0, 5,
40.  0, 0, 0, 0, 8, 0, 0, 7, 9
41.  }
42.  };

44.  Initialize(grid);
45.  }

47.  [RelayCommand]
48.  void  Clear()
49.  {
50.  Initialize();
51.  }

53.  private  void  Initialize(SudokuGrid sudokuBoard = null)
54.  {
55.  SudokuBoard = sudokuBoard ?? new  SudokuGrid();
56.  Boxes = new  ObservableCollection<BoxViewModel>();
57.  }
58.  }

Like CellViewModel, SudokuViewModel also uses annotations to mark the class and the properties. Additionally, it marks methods with RelayCommand which are invoked from respective button clicks. This will let the MVVM Toolkit automatically generate commands with the right signature. The generated code can be inspected under Analyzers in Solution Explorer as shown below in [Figure 7.17](#ch07.xhtml_fig7-17):

![](images/Figure_7.17.png)

Figure 7.17: Files generated by MVVM source generators

We must now update the three views to use properties from their respective view models and setup the bindings to display content in the individual cells. Update the three controls as follows:

CellView.xaml

1.  <UserControl x:Class="SudokuBuddy.Controls.CellView"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/
    presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-
    compatibility/2006"
5.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
6.  mc:Ignorable="d">
7.  <Border BorderBrush="Black" BorderThickness="1">
8.  <Grid>
9.  <TextBlock Text="{Binding Digit}" />
10.  <ItemsControl ItemsSource="{Binding Candidates}" Visibility="{Binding CandidatesVisibility}">
11.  <ItemsControl.ItemsPanel>
12.  <ItemsPanelTemplate>
13.  <UniformGrid Rows="3" Columns="3"/>
14.  </ItemsPanelTemplate>
15.  </ItemsControl.ItemsPanel>
16.  <ItemsControl.ItemTemplate>
17.  <DataTemplate>
18.  <TextBlock Text="{Binding}"/>
19.  </DataTemplate>
20.  </ItemsControl.ItemTemplate>
21.  </ItemsControl>
22.  </Grid>
23.  </Border>
24.  </UserControl>

The preceding view is bound to the view-model properties Digit (line 9), Candidates and CandidatesVisibility (line 10). The binding on line 18 effectively shows the candidates from source Candidates array dynamically.

BoxView.xaml

1.  <UserControl x:Class="SudokuBuddy.Controls.BoxView"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
5.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
6.  xmlns:local="clr-namespace:SudokuBuddy.Controls"
7.  mc:Ignorable="d">
8.  <Border BorderBrush="Black" BorderThickness="1">
9.  <Grid>
10.  <ItemsControl ItemsSource="{Binding Cells}">
11.  <ItemsControl.ItemsPanel>
12.  <ItemsPanelTemplate>
13.  <UniformGrid Rows="3" Columns="3"/>
14.  </ItemsPanelTemplate>
15.  </ItemsControl.ItemsPanel>
16.  <ItemsControl.ItemTemplate>
17.  <DataTemplate>
18.  <local:CellView DataContext="{Binding}"/>
19.  </DataTemplate>
20.  </ItemsControl.ItemTemplate>
21.  </ItemsControl>
22.  </Grid>
23.  </Border>
24.  </UserControl>

SudokuView.xaml

1.  <UserControl x:Class="SudokuBuddy.Controls.SudokuView"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
5.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
6.  xmlns:local="clr-namespace:SudokuBuddy.Controls"
7.  xmlns:viewmodels="clr-namespace:SudokuBuddy.ViewModels"
8.  mc:Ignorable="d">
9.  <UserControl.DataContext>
10.  <viewmodels:SudokuViewModel/>
11.  </UserControl.DataContext>
12.  <Grid>
13.  <Grid.RowDefinitions>
14.  <RowDefinition Height="auto" />
15.  <RowDefinition />
16.  </Grid.RowDefinitions>
17.  <Grid.ColumnDefinitions>
18.  <ColumnDefinition />
19.  <ColumnDefinition Width="auto"/>
20.  </Grid.ColumnDefinitions>
21.  <ItemsControl ItemsSource="{Binding Boxes}" Grid.Row="0" Grid.Column="0" Grid.RowSpan="2">
22.  <ItemsControl.ItemsPanel>
23.  <ItemsPanelTemplate>
24.  <UniformGrid Rows="3" Columns="3"/>
25.  </ItemsPanelTemplate>
26.  </ItemsControl.ItemsPanel>
27.  <ItemsControl.ItemTemplate>
28.  <DataTemplate>
29.  <local:BoxView DataContext="{Binding}"/>
30.  </DataTemplate>
31.  </ItemsControl.ItemTemplate>
32.  </ItemsControl>

34.  <Button Command="{Binding LoadSampleCommand}" Grid.Row="0" Grid.Column="1" Content="Load Sample"
35.  Height="30" Width="85" HorizontalAlignment="Left" VerticalAlignment="Top" Margin="10,5" />

37.  <Button Command="{Binding ClearCommand}" Grid.Row="1" Grid.Column="1" Content="Clear"
38.  Height="30" Width="85" HorizontalAlignment="Left" VerticalAlignment="Top" Margin="10,5" />

40.  </Grid>
41.  </UserControl>

SudokuView binds Boxes property of SudokuViewModel, like CellView. Additionally, there is binding to the relay commands on lines 34 and 37.

Update the SudokuViewModel code to include a method to initialize the view models based on the Sudoku grid values and invoke this method from the main initialize method. See the highlighted code below:

1.  private  void  Initialize(SudokuGrid sudokuBoard = null)
2.  {
3.  SudokuBoard = sudokuBoard ?? new  SudokuGrid();
4.  Boxes = new  ObservableCollection<BoxViewModel>();

5.  InitializeBoxes();

6.  }

8.  private  void  InitializeBoxes()
9.  {
10.  if (SudokuBoard == null) return;
11.  Boxes.Clear();
12.  for (int i = 0; i < 9; i += 3)
13.  {
14.  for (int j = 0; j < 9; j += 3)
15.  {
16.  var box = new  BoxViewModel { ParentSudokuViewModel = this };
17.  for (int k = i; k < i + 3; k++)
18.  {
19.  for (int l = j; l < j + 3; l++)
20.  {
21.  var cell = new  CellViewModel { ParentBoxViewModel = box, Row = k, Column = l };

23.  if (SudokuBoard.Data[k, l] != 0)
24.  {
25.  cell.Digit = SudokuBoard.Data[k, l].ToString();
26.  }
27.  else
28.  {
29.  cell.Candidates = SudokuBoard.Candidates[k, l]?.ToArray();
30.  cell.CandidatesVisibility = Visibility.Visible;
31.  }

33.  box.Cells.Add(cell);
34.  }
35.  }
36.  Boxes.Add(box);
37.  }
38.  }
39.  }

Make one final change in MainWindow.xaml to increase the width of the window from 450 to 550, to accommodate the buttons.

With the preceding changes in the model (SudokuGrid), views (CellView, BoxView and SudokuView) and view-models (CellViewModel, BoxViewModel and SudokuViewModel) files, the MVVM setup for the Sudoku grid to start showing the numbers in the cell, is now complete. Running the application and clicking the Load Sample button should show up a sample grid with some cells having numbers as follows. Click on the Clear button to show the empty grid. Refer to [Figure 7.18](#ch07.xhtml_fig7-18) given below:

![](images/Figure_7.18.png)

Figure 7.18: Sudoku grid showing digits after MVVM setup

[Show candidates or pencil marks](#contents.xhtml_sc4_190a)

To calculate the possible candidates let us create extension methods for the SudokuGrid model class. Create SudokuGridExtensions.cs class under Helpers folder with following code.

1.  using SudokuBuddy.Models;
2.  using System.Collections.Generic;

4.  namespace SudokuBuddy.Helpers;
5.  public  static  class  SudokuGridExtensions
6.  {
7.  public  static  void  UpdateAllCandidates(this  SudokuGrid sudokuGrid)
8.  {
9.  for (int c = 0; c < 9; c++)
10.  for (int r = 0; r < 9; r++)
11.  sudokuGrid.Candidates[r, c] = GetCandidates(sudokuGrid.
    Data, r, c);
12.  }

14.  private  static  List<string> GetCandidates(byte[,] data, int row, int col)
15.  {
16.  var candidates = new  List<string>();
17.  if (data[row, col] == 0) //proceed only if cell isn't already occupied
18.  {
19.  candidates.AddRange(new  List<string> { "1", "2", "3", "4", "5", "6", "7", "8", "9" });

21.  //check in the row of the particular number
22.  for (int c = 0; c < 9; c++)
23.  candidates.Remove(data[row, c].ToString());

25.  //check in the column of the particular number
26.  for (int r = 0; r < 9; r++)
27.  candidates.Remove(data[r, col].ToString());

29.  //check in the box
30.  int boxStartRowIndex = (row / 3) * 3;
31.  int boxStartColIndex = (col / 3) * 3;

33.  for (int c = 0; c < 3; c++)
34.  for (int r = 0; r < 3; r++)
35.  candidates.Remove(data[boxStartRowIndex + r, boxStartColIndex + c].ToString());
36.  }

38.  return candidates;
39.  }
40.  }

In the GetCandidates method in the preceding code, for a particular cell (which is empty), we are calculating the candidates by removing the digits which may not conform to the rules of the game. This is done by checking the row, column, and the box for the cell. Candidates are updated by iterating over all the cells in the grid in UpdateAllCandidates method.

Make the highlighted change in SudokuViewModel to invoke the new method:

1.  private  void  Initialize(SudokuGrid sudokuBoard = null)
2.  {
3.  SudokuBoard = sudokuBoard ?? new  SudokuGrid();
4.  Boxes = new  ObservableCollection<BoxViewModel>();

6.  SudokuBoard.UpdateAllCandidates();

7.  InitializeBoxes();
8.  }

Let us also add styles to improve the appearance of digit and candidates shown in a cell. To do that, we will create resource dictionaries and then consume them in the views. Create two resource dictionaries under Resources folder with the following content:

DigitStyle.xaml

1.  <ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
2.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
3.  <Style TargetType="TextBlock" x:Key="DigitStyle" >
4.  <Setter Property="Background" Value="Transparent" />
5.  <Setter Property="Foreground" Value="Blue" />
6.  <Setter Property="FontSize" Value="24" />
7.  <Setter Property="FontWeight" Value="Bold" />
8.  <Setter Property="HorizontalAlignment" Value="Center" />
9.  <Setter Property="VerticalAlignment" Value="Center" />
10.  <Setter Property="Height" Value="26" />
11.  <Setter Property="MinWidth" Value="24" />
12.  </Style>
13.  </ResourceDictionary>

PencilMarkStyle.xaml

1.  <ResourceDictionary xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
2.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
3.  <Style x:Key="PencilMarkStyle" TargetType="TextBlock">
4.  <Setter Property="HorizontalAlignment" Value="Center" />
5.  <Setter Property="VerticalAlignment" Value="Bottom" />
6.  <Setter Property="Foreground" Value="CornflowerBlue" />
7.  <Setter Property="FontSize" Value="12" />
8.  <Setter Property="FontWeight" Value="Normal" />
9.  </Style>
10.  </ResourceDictionary>

The DigitStyle and PencilMarkStyle in the preceding code combine styles as resource dictionaries that can be applied to the respective elements together in one go. Include the new files during application startup in App.xaml.

1.  <Application.Resources>

2.  <ResourceDictionary>
3.  <ResourceDictionary.MergedDictionaries>
4.  <ResourceDictionary Source="/Resources/DigitStyle.xaml"/>
5.  <ResourceDictionary Source="/Resources/PencilMarkStyle.xaml"/>
6.  </ResourceDictionary.MergedDictionaries>
7.  </ResourceDictionary>

8.  </Application.Resources>

And use the new styles in CellView.xaml

1.  …
2.  <Grid>

3.  <TextBlock Text="{Binding Digit}" Style="{StaticResource DigitStyle}" />

4.  …
5.  <DataTemplate>

6.  <TextBlock Text="{Binding}" Style="{StaticResource PencilMarkStyle}"/>

7.  </DataTemplate>
8.  …

The UI should now appear as follows in [Figure 7.19](#ch07.xhtml_fig7-19) upon executing and loading the sample grid values:

![](images/Figure_7.19.png)

Figure 7.19: Cells showing digits and candidates

[Allowing user to type digit](#contents.xhtml_sc4_191a)

So far, the Sudoku grid cell shows a digit, but user is not able to type a digit themselves. To allow a user to edit, we need to replace the Text Block control (which is only to display text) with TextBox control (which allows users to enter text). When a user types a digit in a cell, we should update the possible candidates in the related row, column, and the box. To do this make the highlighted changes in DigitStyle.xaml, and SudokuViewModel.cs files as under:

DigitStyle.xaml

1.  …

2.  <Style TargetType="TextBox" x:Key="DigitStyle" >
3.  <Setter Property="BorderThickness" Value="0" />

4.  <Setter Property="Background" Value="Transparent" />
5.  …

SudokuViewModel.cs

1.  …

2.  public CellViewModel[,] Cells2DArray { get; private  set; }

3.  private  void  Initialize(SudokuGrid sudokuBoard = null)
4.  {
5.  SudokuBoard = sudokuBoard ?? new SudokuGrid();
6.  Boxes = new ObservableCollection<BoxViewModel>();

8.  Cells2DArray = new CellViewModel[9, 9];

10.  SudokuBoard.UpdateAllCandidates();
11.  InitializeBoxes();
12.  }

14.  private  void  InitializeBoxes()
15.  {
16.  …
17.  box.Cells.Add(cell);

18.  Cells2DArray[k, l] = cell;

19.  …
20.  }

Cells are organized within boxes but to provide direct access via a two-dimensional array, the new field Cells2DArray is added. A reference to each CellViewModel is saved in the array property during initialization.

To update the candidates as a digit is typed in a cell, add following methods in the SudokuGridExtensions.cs

1.  public  static  void  UpdateAffectedCandidates(this  SudokuGrid sudokuGrid, int row, int col, SudokuViewModel sudokuViewModel)
2.  {
3.  for (int c = 0; c < 9; c++)
4.  if (c != col)
5.  Update(sudokuGrid, row, c, sudokuViewModel); //update row candidates

7.  for (int r = 0; r < 9; r++)
8.  if (r != row)
9.  Update(sudokuGrid, r, col, sudokuViewModel); //update column candidates

11.  int boxRow = (row / 3) * 3;
12.  int boxColumn = (col / 3) * 3;
13.  for (int c = 0; c < 3; c++)
14.  for (int r = 0; r < 3; r++) //include the current cell here
15.  if (boxRow + r != row && boxColumn + c != col)
16.  Update(sudokuGrid, boxRow + r, boxColumn + c, sudokuViewModel); //update box candidates

18.  Update(sudokuGrid, row, col, sudokuViewModel); //update current cell
19.  }

21.  private  static  void  Update(SudokuGrid sudokuGrid, int r, int c, SudokuViewModel sudokuViewModel)
22.  {
23.  sudokuGrid.Candidates[r, c] = GetCandidates(sudokuGrid.Data, r, c);

25.  if (sudokuViewModel != null)
26.  sudokuViewModel.Cells2DArray[r, c].Candidates = sudokuGrid.Candidates[r, c].ToArray();
27.  }

In the preceding code, we are updating the candidates for a particular cell going over the cells in the row, column, and the box. Candidates are first updated in the grid data structure (line 23) followed by updating the same in the view models (line 26).

To synchronize the typed digit and the corresponding view model, create CellViewModel Extensions.cs under Helpers folder with following method:

1.  using SudokuBuddy.ViewModels;
2.  using System.Windows;

4.  namespace SudokuBuddy.Helpers;
5.  public  static  class  CellViewModelExtensions
6.  {
7.  public  static  void  SyncBoardAndViewModel(this  CellViewModel cell)
8.  {
9.  var sudokuViewModel = cell?.ParentBoxViewModel?.ParentSudokuViewModel;
10.  if (sudokuViewModel == null)
11.  return;

13.  var sudokuGrid = sudokuViewModel.SudokuBoard;

15.  //update the grid cell value
16.  byte.TryParse(cell.Digit, out var digit);
17.  sudokuGrid.Data[cell.Row, cell.Column] = digit;
18.  cell.CandidatesVisibility = Visibility.Hidden;

20.  sudokuGrid.UpdateAffectedCandidates(cell.Row, cell.Column, sudokuViewModel);
21.  if (digit == 0)
22.  cell.CandidatesVisibility = Visibility.Visible;

24.  sudokuViewModel.MarkErrors();
25.  }
26.  }

In the preceding method we update the digit in the grid (line 17) and then invoke the method to update the candidates (line 20). This new method should be invoked when a digit is typed in a cell.

To respond to the text changed event of the textbox, instead of adopting the traditional way of writing an event handler such as OnTextChangedHandler, we will use Microsoft.Xaml.Behaviors.Wpf to add interactivity using XAML Behaviors for WPF. Behaviors encapsulate reusable functionalities for elements that can be included without the need for more imperative code. Add the NuGet package Microsoft.Xaml.Behaviors.Wpf by Microsoft. Add the highlighted code in CellViewModel.cs

1.  ...
2.  public  CellViewModel()
3.  {
4.  Candidates = Array.Empty<string>();

6.  TextChangedCommand = new RelayCommand(TextChangedHandler);

7.  }

9.  public ICommand TextChangedCommand { get; private  set; }

11.  private  void TextChangedHandler()
12.  {
13.  this.SyncBoardAndViewModel();
14.  }

And the CellView.Xaml markup:

1.  <UserControl x:Class="SudokuBuddy.Controls.CellView"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
4.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"

5.  xmlns:i="http://schemas.microsoft.com/xaml/behaviors"

6.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
7.  mc:Ignorable="d">
8.  <Border BorderBrush="Black" BorderThickness="1">
9.  <Grid>

10.  <TextBox Style="{StaticResource DigitStyle}" Text="{Binding Digit, Mode=TwoWay, UpdateSourceTrigger=PropertyChanged}">
11.  <i:Interaction.Triggers>
12.  <i:EventTrigger EventName="TextChanged">
13.  <i:InvokeCommandAction Command="{Binding TextChangedCommand}"
14.  CommandParameter="{Binding RelativeSource={RelativeSource Mode=Self}}" />
15.  </i:EventTrigger>
16.  </i:Interaction.Triggers>

17.  </TextBox>
18.  ...

In the preceding snippet we are marking the Digit property binding as TwoWay (line 10) and since we want the typed text to update the source immediately (instead of the default LostFocus event), set the UpdateSourceTrigger attribute of the binding to PropertyChanged. Interaction.Triggers tag sets up the TextChanged  EventTrigger which is handled by the TextChangedCommand in the CellViewModel.

Now the user will be able to type a digit and the candidates will change accordingly as shown in [Figure 7.20](#ch07.xhtml_fig7-20):

![](images/Figure_7.20.png)

Figure 7.20: Cell allows input and candidates change accordingly

[Highlighting incorrect input](#contents.xhtml_sc4_192a)

When digit types in a cell doesn’t follow the rules of Sudoku, we should visually highlight that and the related digits in the same row, column, and the box. To do that, create SudokuViewModelExtensions.cs under Helpers folder with following code:

1.  using SudokuBuddy.ViewModels;

3.  namespace SudokuBuddy.Helpers;
4.  public  static  class  SudokuViewModelExtensions
5.  {
6.  public  static  void  MarkErrors(this  SudokuViewModel sudokuViewModel)
7.  {
8.  for (int i = 0; i < 9; i++)
9.  for (int j = 0; j < 9; j++)
10.  sudokuViewModel.Cells2DArray[i, j].HasError = CellHasError(sudokuViewModel, i, j);
11.  }

13.  private  static  bool  CellHasError(SudokuViewModel sudokuViewModel, int row, int col)
14.  {
15.  var digit = sudokuViewModel.Cells2DArray[row, col].Digit;

17.  //empty content is not error
18.  if (string.IsNullOrEmpty(digit)) return  false;

20.  //anything except numbers 1 to 9 is error
21.  if (!(int.TryParse(digit, out  int i) && i >= 1 && i <= 9))
22.  return  true;

24.  for (int c = 0; c < 9; c++) //check if digit exists in row
25.  if (c != col && sudokuViewModel.Cells2DArray[row, c].Digit == digit) return  true;

27.  for (int r = 0; r < 9; r++) //check if digit exists in column
28.  if (r != row && sudokuViewModel.Cells2DArray[r, col].Digit == digit) return  true;

30.  int boxRow = (row / 3) * 3;
31.  int boxColumn = (col / 3) * 3;

33.  for (int c = 0; c < 3; c++)
34.  for (int r = 0; r < 3; r++) //check if digit exists in box
35.  if (boxRow + r != row
36.  && boxColumn + c != col
37.  && sudokuViewModel.Cells2DArray[boxRow + r, boxColumn + c].Digit == digit)
38.  {
39.  return  true;
40.  }

42.  return  false;
43.  }
44.  }

In the preceding methods we are iterating through all the cells in the grid and checking if the digit in the cell follows the rules of Sudoku game, if the rule is not followed, we set the HasError flag for the cell. Invoke the new method from SyncBoardAndViewModel method in CellViewModelExtensions.cs:

1.  public  static  void SyncBoardAndViewModel(this CellViewModel cell)
2.  {
3.  ...
4.  if (digit == 0)
5.  cell.CandidatesVisibility = Visibility.Visible;

7.  sudokuViewModel.MarkErrors();

8.  }

DigitStyle.xaml will delete the Foreground property setter and include the following style triggers to toggle between red and blue colors based on the value of HasError flag:

1.  …   

2.  <Setter Property="MinWidth" Value="24" />
3.  <Style.Triggers>
4.  <DataTrigger Binding="{Binding HasError, Mode=OneWay}" Value="True">
5.  <Setter Property="Foreground" Value="Red" />
6.  </DataTrigger>
7.  <DataTrigger Binding="{Binding HasError, Mode=OneWay}" Value="False">
8.  <Setter Property="Foreground" Value="Blue" />
9.  </DataTrigger>
10.  </Style.Triggers>

11.  </Style>

Additionally, to disallow typing anything but the digits from 1 to 9 and highlight the cell on focus, include the following code in the control view CellView.xaml:

1.  ...
2.  <TextBox Style="{StaticResource DigitStyle}" Text="{Binding Digit, Mode=TwoWay, UpdateSourceTrigger=PropertyChanged}"

3.  GotFocus="OnGotFocusHandler" LostFocus="OnLostFocusHandler">

4.  <i:Interaction.Triggers>
5.  <i:EventTrigger EventName="TextChanged">
6.  <i:InvokeCommandAction Command="{Binding TextChangedCommand}"
7.  CommandParameter="{Binding RelativeSource={RelativeSource Mode=Self}}" />
8.  </i:EventTrigger>

10.  <i:EventTrigger EventName="PreviewTextInput">
11.  <i:InvokeCommandAction Command="{Binding PreviewTextInputCommand}" PassEventArgsToCommand="True" />
12.  </i:EventTrigger>

14.  </i:Interaction.Triggers>
15.  </TextBox>
16.  ...

The highlighted supporting code in CellViewModel.cs:

1.  ...
2.  public  CellViewModel()
3.  {
4.  Candidates = Array.Empty<string>();

6.  TextChangedCommand = new  RelayCommand(TextChangedHandler);

7.  PreviewTextInputCommand = new  RelayCommand<TextCompositionEventArgs>(PreviewTextInputHandler);

8.  }
9.  public  ICommand TextChangedCommand { get; private  set; }

10.  public  ICommand PreviewTextInputCommand { get; private  set; }

12.  private  void  TextChangedHandler()
13.  {
14.  this.SyncBoardAndViewModel();
15.  }

16.  private  void  PreviewTextInputHandler(TextCompositionEventArgs e)
17.  {
18.  e.Handled = !IsValid(e.Text);
19.  }
20.  private  static  bool  IsValid(string str)
21.  {
22.  return  int.TryParse(str, out  int i) && i >= 1 && i <= 9;
23.  }

And the code behind file CellView.xaml.cs  has the traditional event hander code.

1.  ...
2.  private  void  OnGotFocusHandler(object sender, RoutedEventArgs e)
3.  {
4.  this.Background = Brushes.LightSteelBlue;
5.  }

7.  private  void  OnLostFocusHandler(object sender, RoutedEventArgs e)
8.  {
9.  this.Background = Brushes.White;
10.  }

With the preceding changes the UI will start flagging the errors in input as follows:

![](images/Figure_7.21.png)

Figure 7.21: Flag incorrect input

This completes the Sudoku Buddy program with the planned capabilities.

[Unit testing](#contents.xhtml_sc3_193a)

Because of the decoupling between the view and the logic, the general approach to unit-test a MVVM application is through the View-Model. Add a new MS Test project named SudokuBuddy.Test. Add a project reference to the SudokuBuddy project. Edit the SudokuBuddy.Test.csproj file and change the target framework. This is necessary to keep the target framework in sync in both the projects.

<TargetFramework>net7.0-windows</TargetFramework>

Rename the default UnitTest1.cs file to ViewModelTests.cs and include following content:

1.  using SudokuBuddy.Models;
2.  using SudokuBuddy.ViewModels;

4.  namespace SudokuBuddy.Test;

6.  [TestClass]
7.  public  class  ViewModelTests
8.  {
9.  [TestMethod]
10.  public  void  VerifyViewModel()
11.  {
12.  var TestSudoku = new  SudokuGrid
13.  {
14.  AsLinearArray = new  byte[81]
15.  {
16.  5, 3, 0, 0, 7, 0, 0, 0, 0,
17.  6, 0, 0, 1, 9, 5, 0, 0, 0,
18.  0, 9, 8, 0, 0, 0, 0, 6, 0,
19.  8, 0, 0, 0, 6, 0, 0, 0, 3,
20.  4, 0, 0, 8, 0, 3, 0, 0, 1,
21.  7, 0, 0, 0, 2, 0, 0, 0, 6,
22.  0, 6, 0, 0, 0, 0, 2, 8, 0,
23.  0, 0, 0, 4, 1, 9, 0, 0, 5,
24.  0, 0, 0, 0, 8, 0, 0, 7, 9
25.  }
26.  };

28.  var vm = new  SudokuViewModel(TestSudoku);
29.  Assert.AreEqual(vm.Boxes.Count, 9);

31.  //Access Cells via Boxes
32.  Assert.AreEqual(vm.Boxes[0].Cells.Count, 9);
33.  Assert.AreEqual(vm.Boxes[0].Cells[0].Digit, "5");
34.  CollectionAssert.AreEqual(Array.Empty<string>(), vm.Boxes[0].Cells[0].Candidates);
35.  CollectionAssert.AreEqual(new  string[] { "1", "3", "4", "6" }, vm.Boxes[8].Cells[6].Candidates);

37.  //Access Cells directly via array
38.  var cellVm = vm.Cells2DArray[7, 7];
39.  CollectionAssert.AreEqual(new  string[] { "3" }, cellVm.Candidates);
40.  cellVm.Digit = "3";
41.  cellVm.SyncBoardAndViewModel();
42.  CollectionAssert.AreEqual(Array.Empty<string>(), cellVm.Candidates);
43.  CollectionAssert.AreEqual(new  string[] { "1", "4", "6" }, vm.Boxes[8].Cells[6].Candidates);
44.  }
45.  }

In the preceding unit-test we are asserting the expected values for digit and candidates after initializing a grid and changing the content of a cell (line 40).

The final structure of the two project shows up as follows in the Solution Explorer:

![](images/Figure_7.22.png)

Figure 7.22: Final project structure

[Deployment](#contents.xhtml_sc3_194a)

A WPF application compiles into an executable file, the easiest way to deploy is via Build | Publish selection menu in Visual Studio. Alternatively, right-click the project and choose Publish. The resulting dialog shows various options to compile the project and copy the binaries to the target. For more information see the Deploy a WPF Application reference.

[Conclusion](#contents.xhtml_sc2_195a)

In this chapter, we have explored the option to develop XAML based WPF desktop application. In the subsequent chapters we will look at other desktop applications such as Web UI and MAUI applications.

[Points to remember](#contents.xhtml_sc2_196a)

*   XAML based WPF applications present a versatile option to create applications for Windows desktop.
*   MVVM helps in separating the user interface from the application logic, which improves application maintenance code reuse and enhances testability.

[Exercises](#contents.xhtml_sc2_197a)

*   Enhance the Sudoku Buddy application to load another sample grid of numbers through a new button like the Load Sample button in the application.
*   There is a little bug in the program, on loading the sample grid, if you remove a pre-loaded digit, the candidates do not appear in that cell. Adding and removing a digit in any other cell shows the candidates expectedly. Try and fix this issue.

[Hint: Make the CandidatesVisibility property in CellViewModel an ObservableProperty]

*   Write additional asserts in the ViewModelTests.cs to verify if the HasError flag is correctly set when the cell is assigned an incorrect value.

[References](#contents.xhtml_sc2_198a)

*   Tutorial: Create a simple WPF application with C#

[https://learn.microsoft.com/en-us/visualstudio/get-started/csharp/tutorial-wpf?view=vs-2022](https://learn.microsoft.com/en-us/visualstudio/get-started/csharp/tutorial-wpf?view=vs-2022)

*   Desktop Guide (WPF .NET)

[https://learn.microsoft.com/en-us/dotnet/desktop/wpf/overview/?view=netdesktop-7.0](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/overview/?view=netdesktop-7.0)

*   Repository for WPF related samples

[https://github.com/microsoft/WPF-Samples](https://github.com/microsoft/WPF-Samples)

*   Layout with Absolute and Dynamic Positioning

[https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/bb514707(v=vs.100)](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/bb514707(v=vs.100))

*   Inspect XAML properties while debugging.

[https://learn.microsoft.com/en-us/visualstudio/xaml-tools/inspect-xaml-properties-while-debugging?view=vs-2022](https://learn.microsoft.com/en-us/visualstudio/xaml-tools/inspect-xaml-properties-while-debugging?view=vs-2022)

*   Tutorial: Create a new WPF app with .NET

[https://learn.microsoft.com/en-us/dotnet/desktop/wpf/get-started/create-app-visual-studio?view=netdesktop-7.0](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/get-started/create-app-visual-studio?view=netdesktop-7.0)

*   Styles and templates (WPF .NET)

[https://learn.microsoft.com/en-us/dotnet/desktop/wpf/controls/styles-templates-overview?view=netdesktop-7.0](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/controls/styles-templates-overview?view=netdesktop-7.0)

*   How to: Construct a Dynamic Layout

[https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/bb514697(v=vs.100)](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/bb514697(v=vs.100))

*   Layout System

[https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/ms745058(v=vs.100)?redirectedfrom=MSDN](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/ms745058(v=vs.100)?redirectedfrom=MSDN)

*   Compile a WPF Application

[https://learn.microsoft.com/en-us/dotnet/desktop/wpf/app-development/building-a-wpf-application-wpf?view=netframeworkdesktop-4.8&viewFallbackFrom=netdesktop-7.0](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/app-development/building-a-wpf-application-wpf?view=netframeworkdesktop-4.8&viewFallbackFrom=netdesktop-7.0)

*   Patterns - WPF Apps With The Model-View-ViewModel Design Pattern

[https://learn.microsoft.com/en-us/archive/msdn-magazine/2009/february/patterns-wpf-apps-with-the-model-view-viewmodel-design-pattern](https://learn.microsoft.com/en-us/archive/msdn-magazine/2009/february/patterns-wpf-apps-with-the-model-view-viewmodel-design-pattern)

*   Introduction to the MVVM Toolkit

[https://learn.microsoft.com/en-us/dotnet/communitytoolkit/mvvm/](https://learn.microsoft.com/en-us/dotnet/communitytoolkit/mvvm/)

*   Deploy a WPF Application

[https://learn.microsoft.com/en-us/dotnet/desktop/wpf/app-development/deploying-a-wpf-application-wpf?view=netframeworkdesktop-4.8&viewFallbackFrom=netdesktop-7.0](https://learn.microsoft.com/en-us/dotnet/desktop/wpf/app-development/deploying-a-wpf-application-wpf?view=netframeworkdesktop-4.8&viewFallbackFrom=netdesktop-7.0)

# [CHAPTER 8WinUI 3](#contents.xhtml_ch08a)

[Introduction](#contents.xhtml_sc2_199a)

We started our exploration of Microsoft’s Desktop Applications with Windows Presentation Foundation (WPF) in the last chapter. In this chapter, we will focus on developing native Windows applications for Windows 10 and Windows 11 using Windows UI Library (WinUI) 3. We will understand the evolution of technology in this area and the concepts around it, followed by creating a real-life application using WinUI.

[Structure](#contents.xhtml_sc2_200a)

This chapter has the following topics:

*   WinUI 3
*   Pre-requisites
*   Getting started with WinUI 3 App
    *   Structure of the (default) WinUI 3 Application project
*   Developing real-world WinUI App
    *   Creating the Image Navigator WinUI app
        *   Getting started
        *   Add folder browsing capability to Main Window
        *   Creating Image View Model class
        *   Creating Image List page
        *   Creating Image Detail page
*   Unit testing
*   Deployment

[Objectives](#contents.xhtml_sc2_201a)

The objective of this chapter is to understand the concepts around WinUI application and how to create such an application step-by-step using C# 11 and .NET 7.0 in Visual Studio 2022.

[WinUI 3](#contents.xhtml_sc2_202a)

The Windows UI (WinUI) Library is a native user experience (UX) framework for Windows desktop and Universal Windows Platform (UWP) applications. It is built for modern hardware and devices, offering the latest Fluent Design System for consistent, intuitive, and accessible experiences using the latest user interface (UI) patterns. It can be used to build rich .NET and C++ apps for modern Windows devices from the ground up, or gradually migrate an existing MFC, WinForms, or WPF apps using familiar languages such as C++, C#, Visual Basic, and JavaScript. It powers the operating system environment and essential experiences of Windows 10 and 11 PC, Xbox One, HoloLens, Surface Hub, and many other platforms such as .NET MAUI and React Native for Windows. Refer to the following figure:

![](images/Figure_8.1.png)

Figure 8.1: Conceptual overview of WinUI 3[1](#ch08.xhtml_footnote-000)

* * *

[1](#ch08.xhtml_footnote-000-backlink)  Source: [https://blogs.windows.com/windowsdeveloper/2019/11/04/developer-platform-updates-at-microsoft-ignite-2019/](https://blogs.windows.com/windowsdeveloper/2019/11/04/developer-platform-updates-at-microsoft-ignite-2019/)

WinUI 3 is the latest third generation of the native UX stack in Windows. It consolidates the UX technologies previously built into Windows into a single decoupled framework that ships as part of the Windows App SDK. The Windows App SDK provides a unified set of APIs and tools to develop rich and engaging Windows desktop applications. The latest release 1.3 of Windows App SDK, previously called Project Reunion, opens the door to shipping production Desktop apps to the Microsoft Store.

WinUI 2 is the previous generation of the native UX stack in Windows built for UWP apps. It consists of the XAML Framework and a library of Fluent-based controls and styles.

[Pre-requisites](#contents.xhtml_sc2_203a)

For C# app development using the Windows App SDK, Visual Studio 2022 Community Edition version 17.4 or later, along with the .NET desktop development workload, is needed. Additionally in the Installation details pane of the installation dialog box, select Windows App SDK C# Templates (at the bottom of the list).

On the Individual components tab of the installation dialog box, in the SDKs, libraries, and frameworks section, make sure Windows 10 SDK (10.0.19041.0 or higher) is selected.

Install the extension Single-project MSIX Packaging Tools for VS 2022 for seamlessly executing the project built in this chapter. Optionally, install the extension Template  Studio  for  WinUI  (C#) to create new .NET WinUI apps using a wizard-based UI.

If you already have Visual Studio 2022 or later installed, then executing the following command will open Visual Studio Installer with any missing workloads selected.

Winget install "Visual Studio Community 2022" --override "—add Microsoft.VisualStudio.Workload.ManagedDesktop Microsoft.VisualStudio.ComponentGroup.WindowsAppSDK.Cs" -s msstore

You can then select Modify in the Visual Studio installer to install the required workloads.

[Getting started with WinUI 3 app](#contents.xhtml_sc2_204a)

Create a new WinUI 3 Application project by following the steps below in Visual Studio 2022:

| New project creation (File &#124; New &#124; Project…) |
|  
1.  Create a new project

 |  
1.  Narrow down the list of templates being shown by selecting Language: C#, Platform: All Platforms, Project type: WinUI.
2.  Select template: Blank App, Packaged (WinUI 3 in Desktop)
3.  Click Next

 |
|  
*   B. Configure your new project

 |  
4.  Project name: Enter name of your choice such as FirstWinUIApp.
5.  Location: Select location of choice
6.  Solution: Select either Add to solution or Create new solution
7.  Solution name: Provide name in case a new solution is created.
8.  Place solution and project in the same directory: Normally we keep the solution a level higher so leave it unchecked in case a new solution is created.
9.  Click Create

 |

Table 8.1: Steps to create a new WinUI 3 application project.

Unlike other project types, building WinUI project is not yet supported by dotnet command line interface (CLI).

[Structure of the (default) WinUI 3 Application project](#contents.xhtml_sc3_205a)

On creating the new application using the built-in Blank  App,  Packaged  (WinUI  3  in  Desktop) template following files are created.

| Dependencies &#124; Frameworks | By default, there is a dependency on .NET (Microsoft.NETCore.App) and Windows SDK (Microsoft.Windows.SDK.NET.Ref) |
| Dependencies &#124; Packages | There is a dependency on the build tools (Microsoft.Windows.SDK.BuildTools) and Windows App SDK (Microsoft.WindowsAppSDK) packages. |
| Properties &#124; PublishProfiles | The publish profiles specify the publishing configuration for the app across a variety of platforms in XML files: win10-arm64.pubxml, win10-x64.pubxml, win10-x86.pubxml |
| Properties &#124; launchSettings.json | This file lets you configure launch profiles that can be used when running your app via dotnet run. |
| Assets | This contains a set of PNG image files shipped with the default template. |
| App.manifest | This app manifest file contains configuration related to the way Windows displays the app when installed on user devices. This file is generated by the Visual Studio build process and is based on the information in the Package.appxmanifest file. If any updates are made to the Package.appxmanifest file, project must be rebuilt to see the updates in the AppxManifest.xml file. |
| App.xaml and App.xaml.cs | This combination of markup (.xaml) and code-behind (.xaml.cs) is the entry point of the application. The App class in the code behind inherits from Microsoft.UI.Xaml.Application. It is also responsible for creating and activating an instance of your MainWindow. |
| MainWindow.xaml and MainWindow.xaml.cs | This is the combination of the UI and the interaction logic of the main application window. The MainWindow class inherits from Microsoft.UI.Xaml.Window |
| Package.appxmanifest | This is an XML style file that is used to configure the details of an app, such as publisher information, logos, processor architectures, and other details that determine how the app appears in the Windows Store. |

Table 8.2: Important files in a WinUI application project.

The choice of packaging type is an important consideration for any Windows App SDK project. The packaged deployment option is a way to deploy a WinUI 3 app using an MSIX package, which is a format that provides a modern packaging experience to all Windows apps. Packaged apps process is isolated having limited access to the file system and system registry and runs inside a lightweight app container. They have a package identity at runtime and opting for it allows additional Windows features, such as custom context menu extensions.

The chosen project template Blank  App, Packaged  (WinUI  3  in  Desktop) creates a packaged project where a single project is generated with application files, the package manifest and other supporting files needed to build the app into an MSIX package. In another variation, we can choose the template Blank  App, Packaged  with  Windows  Packaging  Project  (WinUI  3  in  Desktop)  which creates two projects - the main project containing the project files and a separate Windows Packaging Project which includes the Package.appxmanifest file and references the main project to create the MSIX packages. The single-project MSIX feature (which is enabled by the extension Single-project  MSIX  Packaging  Tools for VS 2022) provides a cleaner project structure and a more straightforward development experience. However, if there is a need to combine multiple executables into a single MSIX package, then a Windows Application Packaging Project should be used. The figure below compares the files structure in the two templates.

![](images/Figure_8.2.png)

Figure 8.2: Comparing the files from the two Packaged templates.

There is an unpackaged deployment option also, which is a way to deploy the WinUI 3 app without packaging it into an MSIX package. Here the Windows App SDK runtime can be installed using its own installer or can reference from an external location, such as a network share. With this option, the app is unrestricted in terms of the APIs it can call, and its access to the registry and file system but an unpackaged app doesn't have package identity at runtime, so it misses out on certain Windows features.

To see the unpackaged version in action for the FirstWinUIApp, exclude the package.appxmanifest file from the project and add following property to the csproj project file.

  <WindowsPackageType>None</WindowsPackageType>

Now, running the project using the FirstWinUIApp (Unpackaged) launch profile should run the application. Each type of app can be published to the Microsoft Store and installed that way or via Windows App Installer. It is recommended to choose the packaged option as it provides a seamless, modern, and reliable installation and update experience for your customers.

Let us examine the contents of some of the files created with the FirstWinUIApp.

App.xaml

1.  <Application
2.  x:Class="FirstWinUIApp.App"
3.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
4.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
5.  <Application.Resources>
6.  <ResourceDictionary>
7.  <ResourceDictionary.MergedDictionaries>
8.  <XamlControlsResources xmlns="using:Microsoft.UI.Xaml.Controls" />
9.  </ResourceDictionary.MergedDictionaries>
10.  </ResourceDictionary>
11.  </Application.Resources>
12.  </Application>

App.xaml markup file specifies the shared, globally accessible resources used by the application. The line includes the WinUI resources element via the XamlControlsResources tag. If there are more resources, they can be specified within XamlControlsResources.MergedDictionaries.

App.xaml.cs

1.  using Microsoft.UI.Xaml;

3.  namespace FirstWinUIApp;
4.  ///  <summary>
5.  /// Provides application-specific behavior to supplement the default Application class.
6.  ///  </summary>
7.  public  partial  class  App : Application
8.  {
9.  private  Window m_window;

11.  ///  <summary>
12.  /// Initializes the singleton application object.  This is the first line of authored code
13.  /// executed, and as such is the logical equivalent of main() or WinMain().
14.  ///  </summary>
15.  public  App()
16.  {
17.  this.InitializeComponent();
18.  }

20.  ///  <summary>
21.  /// Invoked when the application is launched.
22.  ///  </summary>
23.  ///  <param  name="args">Details about the launch request and process.</param>
24.  protected  override  void  OnLaunched(Microsoft.UI.Xaml. LaunchActivatedEventArgs args)
25.  {
26.  m_window = new  MainWindow();
27.  m_window.Activate();
28.  }
29.  }

The preceding code behind file launches the MainWindow (line 27).

MainWindow.xaml

1.  <Window x:Class="FirstWinUIApp.MainWindow"
2.  xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
5.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
6.  mc:Ignorable="d">

8.  <StackPanel HorizontalAlignment="Center" VerticalAlignment="Center" Orientation="Horizontal">
9.  <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
10.  </StackPanel>
11.  </Window>

The markup file for MainWindow includes a single button within a StackPanel container control. Clicking on the button invokes the event handler myButton_Click defined in the code behind.

MainWindow.xaml.cs

1.  using Microsoft.UI.Xaml;

3.  namespace FirstWinUIApp;
4.  ///  <summary>
5.  /// An empty window that can be used on its own or navigated to within a Frame.
6.  ///  </summary>
7.  public  sealed  partial  class  MainWindow : Window
8.  {
9.  public  MainWindow()
10.  {
11.  this.InitializeComponent();
12.  this.Title = "First WinUI Application";
13.  }

15.  private  void  myButton_Click(object sender, RoutedEventArgs e)
16.  {
17.  myButton.Content = "Clicked";
18.  }
19.  }

The code behind for MainWindow handles the click event for the button and initializes the window title (line 12). Running the project via the launch profile FirstWinUIApp (Package) shows the following UI.

![](images/Figure_8.3.png)

Figure 8.3: UI of the First WinUI Application

You may be prompted to enable the Developer Mode as follows.

![](images/Figure_8.4.png)

Figure 8.4: First time prompt to enable developer before executing WinUI project.

Developer mode can be enabled in the Windows settings. Also click Yes in the resulting confirmation message to turn on the Developer Mode:

![](images/Figure_8.5.png)

Figure 8.5: Enabling Developer mode in Windows settings.

[Developing real-world WinUI App](#contents.xhtml_sc2_206a)

To understand the concepts around building a real-world WinUI application we will create an image navigator application. User can browse a folder on their disk and see the image files in the chosen folder in different views.

[Creating the Image Navigator WinUI app](#contents.xhtml_sc3_207a)

When fully built, the UI of the application appears as follows.

![](images/Figure_8.6.png)

Figure 8.6: Image Navigator - main Image view

Another view of the main application screen is as follows:

![](images/Figure_8.7.png)

Figure 8.7: Image Navigator - Image and text view

Clicking on any image shows an enlarged view along with some more details about the picture:

![](images/Figure_8.8.png)

Figure 8.8: Image detail view

[Getting started](#contents.xhtml_sc4_208a)

Create a new project named ImageNavigator this time using the Blank App, Packaged with  Windows Packaging Project (WinUI 3 in Desktop) template choosing all the default options as described for the FirstWinUIApp application earlier. When the Create button is clicked you will see a dialog similar to following. Click Ok to select the defaults:

![](images/Figure_8.9.png)

Figure 8.9: Selecting the target Windows version.

You should now see two projects named - ImageNavigator and ImageNavigator (Package) in the solution explorer. Run the code cleanup on the ImageNavigator project. Set the ImageNavigator (Package) as the startup project (not the main project ImageNavigator) and run it. The default UI of the application should show up.

If you check Configuration Manager for the solution you would notice that the Deploy checkbox is checked for the ImageNavigator (Package) project. Also after the project is executed, you should see a shortcut for the project in your Windows Start menu indicating that the project has been deployed on the local machine and can run independent of Visual Studio.

[Add folder browsing capability to Main Window](#contents.xhtml_sc4_209a)

For navigating the images within a folder, we need to first get the folder path which is to be navigated. Include following code in the MainWindow view and the corresponding code behind.

MainWindow.xaml

1.  <Window x:Class="ImageNavigator.MainWindow" xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
2.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
3.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006" mc:Ignorable="d">
5.  <Grid>
6.  <Grid.RowDefinitions>
7.  <RowDefinition Height="Auto" />
8.  <RowDefinition />
9.  </Grid.RowDefinitions>
10.  <Grid.ColumnDefinitions>
11.  <ColumnDefinition Width="Auto" />
12.  <ColumnDefinition Width="*" />
13.  <ColumnDefinition />
14.  </Grid.ColumnDefinitions>
15.  <TextBlock Grid.Row="0" Grid.Column="0" Padding="10" Text="Image Folder: " />
16.  <TextBox x:Name="PickFolderOutputTextBlock" Grid.Row="0" Grid.Column="1" Height="25" Background="LightGray"
17.  IsReadOnly="True" />
18.  <Button x:Name="PickFolderButton" Grid.Row="0" Grid.Column="2" Margin="10" Click="PickFolderButton_Click"
19.  Content="Browse and Load" />
20.  <Frame x:Name="ImageListFrame" Grid.Row="1" Grid.ColumnSpan="3" Height="750" MinWidth="500" />
21.  </Grid>
22.  </Window>

In the preceding code, we set up a grid of two rows and three columns, then placing the TextBlock label, a textbox, and a button to choose the folder path in the first row. The second row has the image frame spanning across three columns to show the list of images.

MainWindow.cs

1.  using Microsoft.UI.Xaml;
2.  using System;
3.  using Windows.Storage.AccessCache;
4.  using Windows.Storage.Pickers;

6.  namespace ImageNavigator;
7.  ///  <summary>
8.  /// An empty window that can be used on its own or navigated to within a Frame.
9.  ///  </summary>
10.  public  sealed  partial  class  MainWindow : Window
11.  {
12.  public  MainWindow()
13.  {
14.  this.InitializeComponent();
15.  Title = "Image Navigator";
16.  }

18.  private  async  void  PickFolderButton_Click(object sender, RoutedEventArgs e)
19.  {
20.  // Clear previous returned file name, if it exists
21.  PickFolderOutputTextBlock.Text = "";

23.  // Create a folder picker
24.  FolderPicker openPicker = new();

26.  // Retrieve the window handle (HWND) of the current WinUI 3 window.
27.  var hWnd = WinRT.Interop.WindowNative.GetWindowHandle(this);
28.  WinRT.Interop.InitializeWithWindow.Initialize(openPicker, hWnd);

30.  // Initialize the folder picker with the window handle (HWND).
31.  WinRT.Interop.InitializeWithWindow.Initialize(openPicker, hWnd);

33.  // Set options for your folder picker
34.  openPicker.SuggestedStartLocation = PickerLocationId.PicturesLibrary;
35.  openPicker.FileTypeFilter.Add("*");

37.  // Open the picker for the user to pick a folder
38.  var folder = await openPicker.PickSingleFolderAsync();
39.  if (folder != null)
40.  {
41.  StorageApplicationPermissions.FutureAccessList.AddOrReplace("PickedFolderToken", folder);
42.  PickFolderOutputTextBlock.Text = folder.Path;
43.  }
44.  }
45.  }

The click event handler for the button initializes a folder picker between lines 24 to 35 and invokes the dialog on line 38\. The chosen folder is assigned to the text property of the textbox on line 42\. Saving the project and executing ImageNavigator (Package), shows the main Image Navigator window as follows:

![](images/Figure_8.10.png)

Figure 8.10: Main Window with browse folder capability

[Creating Image View Model class](#contents.xhtml_sc4_210a)

We need a class corresponding to each image file having properties which we want to display and with which we want to bind the UI. Create a new class ImageViewModel under ViewModels folder with following code.

ImageViewModel.cs

1.  using System;
2.  using Windows.Storage;
3.  using Windows.Storage.FileProperties;

5.  namespace ImageNavigator.ViewModels;
6.  public  class  ImageViewModel
7.  {
8.  public  ImageViewModel(ImageProperties properties, StorageFile imageFile, string name)
9.  {
10.  ImageName = name;
11.  FilePath = imageFile.Path;
12.  ImageDimensions = $"{properties.Width} x {properties.Height}";

14.  //read rating from properties, and create a random value if it doesn;t exist
15.  var rating = (int)properties.Rating;
16.  ImageRating = rating == 0 ? (new  Random()).Next(1, 5) : rating;

18.  //set DateTaken property as a random date value
19.  DateTaken = DateTime.Today.Subtract(new  TimeSpan((new  Random()).Next(1000), 0, 0, 0)).Date;
20.  }

22.  public  string ImageName { get; }
23.  public  string FilePath { get; }
24.  public  string ImageDimensions { get; }
25.  public  int ImageRating { get; }
26.  public  DateTime DateTaken { get; }
27.  }

The ImageViewModel class has getter properties corresponding to the different attributes of an image file. These properties are used to bind the information on the list and detail pages for the image. Some of the properties are given random values while others are assigned the values from the image properties.

[Creating Image List page](#contents.xhtml_sc4_211a)

Create a new WinUI 3 Blank page under folder Pages with name ImageListPage.xaml.

![](images/Figure_8.11.png)

Figure 8.11: Add Image List Page

Include following code in the view page and the code-behind files.

ImageListPage.xaml

1.  <Page x:Class="ImageNavigator.Pages.ImageListPage" xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
2.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
3.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
5.  xmlns:viewmodel="using:ImageNavigator.ViewModels"
6.  Background="{ThemeResource ApplicationPageBackgroundThemeBrush}" mc:Ignorable="d">
7.  <Page.Resources>
8.  <!--  Data template to show list of images  -->
9.  <DataTemplate x:Key="ImageTemplate" x:DataType="viewmodel:ImageViewModel">
10.  <Image Width="190" Height="130" Source="{x:Bind FilePath}" Stretch="UniformToFill" />
11.  </DataTemplate>
12.  <!--  Data template to show list of images along with some details  -->
13.  <DataTemplate x:Key="ImageTextTemplate" x:DataType="viewmodel:ImageViewModel">
14.  <Grid Width="280">
15.  <Grid.ColumnDefinitions>
16.  <ColumnDefinition Width="Auto" />
17.  <ColumnDefinition Width="*" />
18.  </Grid.ColumnDefinitions>
19.  <Image Width="160" Height="150" VerticalAlignment="Top" Source="{x:Bind FilePath}"
20.  Stretch="UniformToFill" />
21.  <StackPanel Grid.Column="1" Margin="8,0,0,8">
22.  <TextBlock Margin="0,0,0,8" Style="{ThemeResource BodyTextBlockStyle}" Text="{x:Bind ImageName}" />
23.  <StackPanel Orientation="Horizontal">
24.  <TextBlock Style="{ThemeResource CaptionTextBlockStyle}" Text="{x:Bind ImageDimensions}" />
25.  </StackPanel>
26.  </StackPanel>
27.  </Grid>
28.  </DataTemplate>
29.  <Style x:Key="ImageGridView_ItemContainerStyle" TargetType="GridViewItem">
30.  <Setter Property="Background" Value="Gray" />
31.  <Setter Property="Margin" Value="8" />
32.  </Style>
33.  <ItemsPanelTemplate x:Key="ImageGridView_ItemsPanelTemplate">
34.  <ItemsWrapGrid HorizontalAlignment="Center" Orientation="Horizontal" />
35.  </ItemsPanelTemplate>
36.  </Page.Resources>
37.  <Grid>
38.  <Grid.ColumnDefinitions>
39.  <ColumnDefinition Width="*" />
40.  <ColumnDefinition Width="Auto" />
41.  </Grid.ColumnDefinitions>
42.  <GridView x:Name="ContentGridView" Grid.Column="0" IsItemClickEnabled="True"
43.  ItemContainerStyle="{StaticResource ImageGridView_ItemContainerStyle}"
44.  ItemTemplate="{StaticResource ImageTemplate}"
45.  ItemsPanel="{StaticResource ImageGridView_ItemsPanelTemplate}" ItemsSource="{x:Bind Images}"
46.  Loaded="List_Loaded" />
47.  <StackPanel Grid.Column="1">
48.  <RadioButtons>
49.  <RadioButton Checked="ItemTemplate_Checked" Content="Image" GroupName="Template" IsChecked="True"
50.  Tag="ImageTemplate" />
51.  <RadioButton Checked="ItemTemplate_Checked" Content="Image/Text" GroupName="Template"
52.  Tag="ImageTextTemplate" />
53.  </RadioButtons>
54.  </StackPanel>
55.  </Grid>
56.  </Page>

In the preceding ImageListPage view code, we have defined page resources between lines 7 and 36 which is followed by the grid definition including the GridView control and StackPanel having the radio button options between lines 37 and 55\.

The page resource has two data templates defining the layout of pictures in two different ways. In XAML, data templates are used to generate the visual representation of each data item in controls such as ListBox, ComboBox, ListView or GridView. They are defined as resources and can be assigned to the ItemTemplate property of the control. Each data template has an Image control to render the image which in turn binds to the FilePath property of the ImageViewModel (on lines 10 and 19). ItemPanelTemplate resource defined, starting from line 33, is used to control the layout of items in the GridView.

The GridView control binds to the Images property of ImageViewModel via the ItemSource property (line 45). The adjacent StackPanel has the radio buttons to choose the type of view. The Checked event of radio button is handled in the code-behind file to assign the chosen data template at run time.

ImageListPage.xaml.cs

1.  using ImageNavigator.ViewModels;
2.  using Microsoft.UI.Xaml;
3.  using Microsoft.UI.Xaml.Controls;
4.  using Microsoft.UI.Xaml.Navigation;
5.  using System;
6.  using System.Collections.Generic;
7.  using System.Collections.ObjectModel;
8.  using System.Threading.Tasks;
9.  using Windows.Storage;
10.  using Windows.Storage.Search;

12.  namespace ImageNavigator.Pages;
13.  public  sealed  partial  class  ImageListPage : Page
14.  {
15.  public  ObservableCollection<ImageViewModel> Images { get; private  set; }
16.  = new  ObservableCollection<ImageViewModel>();

18.  public  ImageListPage()
19.  {
20.  this.InitializeComponent();
21.  }

23.  protected  override  void  OnNavigatedTo(NavigationEventArgs e)
24.  {
25.  if (e.Parameter is  string @string && !string.IsNullOrWhiteSpace(@string))
26.  _ = GetItemsAsync(e.Parameter.ToString());

28.  base.OnNavigatedTo(e);
29.  }

31.  private  async  Task  GetItemsAsync(string imageFolder)
32.  {
33.  var picturesFolder = await  StorageFolder.GetFolderFromPathAsync(imageFolder);
34.  var result = picturesFolder.CreateFileQueryWithOptions(new  QueryOptions(CommonFileQuery.OrderByName,
35.  new  List<string> { ".jpg", ".jpeg", ".png", ".bmp" }));

37.  foreach (StorageFile file in  await result.GetFilesAsync())
38.  Images.Add(await  LoadImageInfoAsync(file));
39.  }

41.  private  static async Task<ImageViewModel> LoadImageInfoAsync(StorageFile file)
42.  {
43.  var properties = await file.Properties.GetImagePropertiesAsync();
44.  return  new(properties, file, file.DisplayName);
45.  }

47.  private  void  List_Loaded(object sender, RoutedEventArgs e)
48.  {
49.  if (Images != null)
50.  {
51.  // If the connected item appears outside the viewport, scroll it into view.
52.  ContentGridView.ScrollIntoView(Images, ScrollIntoViewAlignment.Default);
53.  ContentGridView.UpdateLayout();

55.  // Set focus on the list
56.  ContentGridView.Focus(FocusState.Programmatic);
57.  }
58.  }

60.  private  void  ItemTemplate_Checked(object sender, RoutedEventArgs e)
61.  {
62.  var tag = (sender as  FrameworkElement).Tag;
63.  if (tag != null)
64.  {
65.  string template = tag.ToString();
66.  ContentGridView.ItemTemplate = (DataTemplate)this.Resources[template];
67.  }
68.  }
69.  }

The preceding code behind file for the ImageListPage loads the items when the page is navigated. This happens in the OnNavigatedTo event. On line 26 GetItemsAsync together with LoadImageInfoAsync populates details of the specific image files as read from the folder chosen by the user. The ItemTemplate_Checked handler assigns the selected item template to the GridView. Notice the interesting use of the Tag property – the property is assigned a value in the radio button definition in the View markup and is later checked and assigned to the GridView  ItemTemplate property on line 66.

To invoke the list page when the user browses a folder on the Main Window, add the highlighted line in the code behind file.

MainWindow.xaml.cs

1.  private  async  void  PickFolderButton_Click(object sender, RoutedEventArgs e)
2.  {
3.  ...

5.  // Open the picker for the user to pick a folder
6.  var folder = await openPicker.PickSingleFolderAsync();
7.  if (folder != null)
8.  {
9.  StorageApplicationPermissions.FutureAccessList.AddOrReplace("PickedFolderToken", folder);
10.  PickFolderOutputTextBlock.Text = folder.Path;

11.  ImageListFrame.Navigate(typeof(ImageListPage), folder.Path);

12.  }
13.  }

The added line navigates to the Image List page, passing the user chosen folder as parameter. Running the project should show the Image List page as follows:

![](images/Figure_8.12.png)

Figure 8.12: Image List - images view

The image and text view shows up as follows:

![](images/Figure_8.13.png)

Figure 8.13: Images list - image and text view

[Creating Image Detail page](#contents.xhtml_sc4_212a)

Next, we will show the image details page when the user clicks on any image on the list page. Add the ImageDetailsPage under Pages folder the way we had added ImageListPage, with following code in the view and code-behind files.

ImageDetailsPage.xaml

1.  <Page x:Class="ImageNavigator.Pages.ImageDetailsPage" xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
2.  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
3.  xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
4.  xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
5.  Background="{ThemeResource ApplicationPageBackgroundThemeBrush}" mc:Ignorable="d">
6.  <Grid>
7.  <Grid.RowDefinitions>
8.  <RowDefinition Height="Auto" />
9.  <RowDefinition Height="*" />
10.  </Grid.RowDefinitions>
11.  <Grid x:Name="headerBackground" HorizontalAlignment="Stretch" VerticalAlignment="Stretch"
12.  Background="{ThemeResource SystemControlAcrylicElementBrush}">
13.  <Button x:Name="GoBackButton" HorizontalAlignment="Left" VerticalAlignment="Top"
14.  Background="{ThemeResource SystemAccentColor}" Click="BackButton_Click" Content="Go Back"
15.  Loaded="GoBackButton_Loaded" />
16.  </Grid>
17.  <Grid x:Name="headerContent" Margin="50">
18.  <Grid.ColumnDefinitions>
19.  <ColumnDefinition Width="Auto" />
20.  <ColumnDefinition Width="*" />
21.  </Grid.ColumnDefinitions>
22.  <Image x:Name="detailedImage" MaxHeight="500" VerticalAlignment="Top" Source="{x:Bind ImageDetail.FilePath}"
23.  Stretch="UniformToFill" />
24.  <StackPanel x:Name="coordinatedPanel" Grid.Column="1" Margin="20,0" VerticalAlignment="Top">
25.  <TextBlock Style="{ThemeResource SubtitleTextBlockStyle}" Text="{x:Bind ImageDetail.ImageName}" />
26.  <StackPanel Orientation="Horizontal">
27.  <RatingControl Margin="5" IsReadOnly="True" Value="{x:Bind ImageDetail.ImageRating}" />
28.  </StackPanel>
29.  <StackPanel Orientation="Horizontal">
30.  <TextBlock Margin="5" Style="{ThemeResource CaptionTextBlockStyle}"
31.  Text=“{x:Bind ImageDetail.ImageDimensions}“ />
32.  </StackPanel>
33.  <StackPanel Orientation="Horizontal">
34.  <TextBlock Margin="5" Style="{ThemeResource CaptionTextBlockStyle}"
35.  Text="{x:Bind ImageDetail.DateTaken.ToShortDateString()}" />
36.  </StackPanel>
37.  </StackPanel>
38.  </Grid>
39.  </Grid>
40.  </Page>

The preceding code in ItemDetailsPage view, defines a grid with two rows (lines 7 to 10) having two sub-grids – one to show the background and the back button and another grid having two columns (lines 18 to 21) which shows the image and image details in a stack panel.

Back button defined on line 13 takes the user back to the list page via the click handler BackButton_Click. The header content grid shows the image via Image control bound to the ImageDetail.FilePath property (line 22). The stack panel shows other image properties between lines 24 and 37 via controls bound to the respective properties of ImageDetail.

Notice the use of ThemeResource markup extension for several controls. Theme resources in XAML are a set of resources that apply different values depending on which system theme is active. There are three themes that the XAML framework supports: Light, Dark, and High Contrast. Unlike StaticResource which is evaluated when the XAML is first loaded by the app, evaluation of a ThemeResource occurs when the app loads and subsequently each time the theme changes at runtime. Each theme resource is part of the XAML file themeresources.xaml. For design purposes, themeresources.xaml is available in the \(Program Files)\Windows Kits\10\DesignTime\CommonConfiguration\Neutral\UAP\<SDK version>\Generic folder from a Windows SDK installation. The resource dictionaries in themeresources.xaml are also reproduced in generic.xaml in the same directory. Right clicking a particular theme resource and selecting View Definition in Visual Studio will open the generic.xaml with the definition of the resource.

ImageDetailsPage.cs

1.  using ImageNavigator.ViewModels;
2.  using Microsoft.UI.Xaml;
3.  using Microsoft.UI.Xaml.Controls;
4.  using Microsoft.UI.Xaml.Navigation;

6.  namespace ImageNavigator.Pages;
7.  public  sealed  partial  class  ImageDetailsPage : Page
8.  {
9.  public  ImageViewModel ImageDetail { get; set; }

11.  public  ImageDetailsPage()
12.  {
13.  this.InitializeComponent();
14.  }

16.  private  void  GoBackButton_Loaded(object sender, RoutedEventArgs e)
17.  {
18.  // When we land in page, put focus on the back button
19.  GoBackButton.Focus(FocusState.Programmatic);
20.  }

22.  protected  override  void  OnNavigatedTo(NavigationEventArgs e)
23.  {
24.  base.OnNavigatedTo(e);

26.  // Store the item to be used in binding to UI
27.  ImageDetail = e.Parameter as  ImageViewModel;
28.  }

30.  private  void  BackButton_Click(object sender, RoutedEventArgs e)
31.  {
32.  Frame.GoBack();
33.  }
34.  }

In the preceding code-behind for ImageDetailPage, the ImageDetail view model object is assigned the value, when the page is navigated, on line 27\. This object is used to bind the respective image information fields on the UI.

To invoke the details when the user clicks on an image in the list view include the highlighted code in the ImageList view and event handling code in the code behind file.

ImageListPage.xaml

1.  ...
2.  </Grid.ColumnDefinitions>
3.  <GridView x:Name="ContentGridView" Grid.Column="0" IsItemClickEnabled="True"
4.  ItemContainerStyle="{StaticResource ImageGridView_ItemContainerStyle}"
5.  ItemTemplate="{StaticResource ImageTemplate}"
6.  ItemsPanel="{StaticResource ImageGridView_ItemsPanelTemplate}" ItemsSource="{x:Bind Images}"

7.  Loaded="List_Loaded" ItemClick="ListItem_Click" />

8.  <StackPanel Grid.Column="1">
9.  ...

ImageListPage.cs

1.  private  void  ListItem_Click(object sender, ItemClickEventArgs e)
2.  {
3.  ImageViewModel detailedImage = e.ClickedItem as  ImageViewModel;
4.  Frame.Navigate(typeof(ImageDetailsPage), detailedImage);
5.  }

The detail page shows up as follows:

![](images/Figure_8.14.png)

Figure 8.14: Image detail page

This completes the Image Navigator application as we had planned.

[Unit testing](#contents.xhtml_sc3_213a)

It is possible to write unit-tests for WinUI applications that test the functional code, taking simple inputs and providing deterministic outputs that can be verified in the unit-test. We can also write end-to-end integration tests which simulate user-inputs and perform validation of UI elements.

The first type of tests is facilitated by having view models free of any UI logic, this was demonstrated in the last chapter on WPF. The same strategy can be used to test the ImageViewModel class in ImageNavigator (see the Exercises).

For more advanced scenarios testing the UI elements refer to the Testing wiki on WindowsCommunityToolkit GitHub repo (check the link in references).

[Deployment](#contents.xhtml_sc3_214a)

After developing the WinUI based Windows app, the next step is to create a deployment package followed by installation via Microsoft Store or (where it must be published beforehand) or Sideloaded via Windows App Installer.

There are several considerations for Windows Apps that determine the precise nature of their deployment. The first is the way the app is packaged. We discussed about the different packaging options earlier in this chapter. Another option to consider is the way Windows App SDK is distributed.

![](images/Figure_8.15.png)

Figure 8.15: Deployment options for WinUI apps

The recommended option is to have a packaged app and opt for framework dependent way where only the app and its other dependencies are distributed, Windows App SDK runtime is installed automatically via the Framework package without any action required from the app. For more details of the different options around deployment please refer to the Windows App SDK deployment overview link in references.

When it comes to installation, Sideloading and installing WinUI apps via Microsoft Store are two different methods of installing the apps on Windows. Sideloading is the process of installing apps that are not from an official source, such as the Microsoft Store. This is typically done for Line of Business (LOB) apps that are developed in-house by an organization. Sideloading requires enabling a setting in Windows and then installing the app manually. On the other hand, installing WinUI apps via Microsoft Store involves downloading and installing the app from the Microsoft Store.

Publishing the apps on Microsoft Stores requires creating a developer account on the Microsoft Partner Center and following a series of prescribed steps. More details can be found in the Publish Windows apps, and games link in references.

To create the package for the first time, select Project | Publish | Create App Packages… in Visual Studio and follow the steps of the wizard.

[Conclusion](#contents.xhtml_sc2_215a)

In this chapter we have explored the option to develop XAML based WinUI 3 application that uses Windows App SDK and runs only on Windows. To build a cross-platform app, consider .NET MAUI, a Progressive Web App (PWA), or React Native for Windows.

We will discuss .NET MAUI in the next chapter.

[Points to remember](#contents.xhtml_sc2_216a)

*   WinUI 3 is the latest UI framework from Microsoft that ships with the Windows App SDK.
*   The Windows App SDK provides a unified set of APIs and tools that can be used to create production desktop apps that target Windows 10 (Version 1809, OS build 17763 or later) and later and can be published to the Microsoft Store using an MSIX package.
*   WinUI 3 is fully decoupled from the OS and released to developers via NuGet packages, meaning that it is possible to create a desktop application using WinUI 3 much like using WPF or WinForms now.
*   WinUI 3 uses XAML (eXtensible Application Markup Language) for defining the user interface.
*   WinUI 3 embraces Microsoft's Fluent Design System, which provides a set of guidelines and controls for creating modern and visually appealing applications.

[Exercises](#contents.xhtml_sc2_217a)

*   Associate the information of number of likes and keywords randomly with all the images and show the likes on image list page and the keywords on the Image Details page.
*   Use the Source Generators feature from Community MVVM Toolkit to create Images as an ObservableProperty in ImageListPage class.

    [Hint: Make the changes on the lines of BoxViewModel.cs in the chapter on WPF]

*   Create a MS Test unit test to verify ImageViewModel class.

    [Hint: Refer to the ViewModelTests in SudokuBuddy.Test project developed in the WPF chapter]

[References](#contents.xhtml_sc2_218a)

*   Windows UI Library (WinUI)

[https://learn.microsoft.com/en-us/windows/apps/winui/](https://learn.microsoft.com/en-us/windows/apps/winui/)

*   WinUI 3 Gallery

[https://apps.microsoft.com/store/detail/winui-3-gallery/9P3JFPWWDZRC](https://apps.microsoft.com/store/detail/winui-3-gallery/9P3JFPWWDZRC)

[https://github.com/microsoft/WinUI-Gallery](https://github.com/microsoft/WinUI-Gallery)

*   Microsoft / WindowsAppSDK-Samples

[https://github.com/microsoft/WindowsAppSDK-Samples](https://github.com/microsoft/WindowsAppSDK-Samples)

*   Building Modern & Performant Desktop Apps—Is WinUI 3.0 the Way to Go?

[https://www.telerik.com/blogs/building-modern-performant-desktop-apps-winui-30-the-way-to-go](https://www.telerik.com/blogs/building-modern-performant-desktop-apps-winui-30-the-way-to-go)

*   Comparing WinUI and Its Predecessors

[https://www.grapecity.com/blogs/comparing-winui-and-its-predecessors](https://www.grapecity.com/blogs/comparing-winui-and-its-predecessors)

*   Design and code Windows apps

[https://learn.microsoft.com/en-us/windows/apps/design](https://learn.microsoft.com/en-us/windows/apps/design)

*   Windows UI Library Overview

[https://github.com/microsoft/microsoft-ui-xaml/blob/main/docs/roadmap.md#winui-30-feature-roadmap](https://github.com/microsoft/microsoft-ui-xaml/blob/main/docs/roadmap.md#winui-30-feature-roadmap)

*   Fluent Design System

[https://www.microsoft.com/design/fluent/](https://www.microsoft.com/design/fluent/)

*   Windows App SDK

[https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/](https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/)

*   Package your app using single project MSIX

[https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/single-project-msix?tabs=csharp](https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/single-project-msix?tabs=csharp)

*   A deep dive into WinUI 3 in desktop apps

[https://blogs.windows.com/windowsdeveloper/2020/07/07/a-deep-dive-into-winui-3-in-desktop-apps/](https://blogs.windows.com/windowsdeveloper/2020/07/07/a-deep-dive-into-winui-3-in-desktop-apps/)

*   WinUI 3 Preview 3

[https://devblogs.microsoft.com/ifdef-windows/winui-3-preview-3/](https://devblogs.microsoft.com/ifdef-windows/winui-3-preview-3/)

*   Writing apps for Windows: Selecting a development technology

[https://learn.microsoft.com/en-us/windows/apps/get-started](https://learn.microsoft.com/en-us/windows/apps/get-started)

*   Advantages and disadvantages of packaging your app

[https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/#advantages-and-disadvantages-of-packaging-your-app](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/#advantages-and-disadvantages-of-packaging-your-app)

*   Testing · CommunityToolkit/WindowsCommunityToolkit Wiki

[https://github.com/CommunityToolkit/WindowsCommunityToolkit/wiki/Testing](https://github.com/CommunityToolkit/WindowsCommunityToolkit/wiki/Testing)

*   WinUI repo

[https://github.com/microsoft/microsoft-ui-xaml](https://github.com/microsoft/microsoft-ui-xaml)

*   XAML theme resources

[https://learn.microsoft.com/en-us/windows/apps/design/style/xaml-theme-resources](https://learn.microsoft.com/en-us/windows/apps/design/style/xaml-theme-resources)

*   Deployment architecture and overview for framework-dependent apps

[https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/deployment-architecture](https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/deployment-architecture)

*   Windows App SDK deployment overview

[https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/deploy-overview](https://learn.microsoft.com/en-us/windows/apps/package-and-deploy/deploy-overview)

*   Publish Windows apps and games

[https://learn.microsoft.com/en-us/windows/apps/publish/](https://learn.microsoft.com/en-us/windows/apps/publish/)

# [CHAPTER 9.NET MAUI](#contents.xhtml_ch09a)

[Introduction](#contents.xhtml_sc2_219a)

In the last two chapters, we have built desktop applications specifically for the Windows platform. This chapter is devoted to understanding a comparatively newer technology .NET Multi-platform App UI (MAUI). We will first understand more about the concepts around this. Later we will create a real-life application using .NET MAUI.

[Structure](#contents.xhtml_sc2_220a)

This chapter has following topics.

*   Evolution of mobile application development
*   .NET MAUI
*   Pre-requisites
*   Getting started with .NET MAUI App
    *   Structure of the (default) .NET MAUI app project
    *   Creating .NET MAUI Blazor Hybrid application
*   Developing real-world .NET MAUI app
    *   Recap – Sudoku Buddy WPF application
    *   WPF Vs .NET MAUI
    *   Migrating Sudoku Buddy from WPF to .NET MAUI
        *   Getting started
        *   Copy files from WPF application
        *   Create Views
        *   Running with Android Simulator
    *   Unit testing
    *   Deployment

[Objectives](#contents.xhtml_sc2_221a)

The objective of this chapter is to understand the concepts around the .NET MAUI application and how to create such an application step-by-step using C# 11 and .NET 7.0 in Visual Studio 2022.

[Evolution of mobile application development](#contents.xhtml_sc2_222a)

The landscape of mobile application development in Microsoft .NET has evolved significantly leading up to the introduction of .NET MAUI (Multi-platform App UI). Initially, Microsoft focused on building mobile apps specifically for Windows Phone using the .NET framework. Developers could leverage their knowledge of C# and the .NET framework to create native Windows Phone apps using frameworks like Silverlight and XNA.

With the launch of Windows Phone 8 and the introduction of Windows Runtime (WinRT), Microsoft expanded its mobile app development capabilities. WinRT allowed developers to build universal apps that could run across various Windows devices, including smartphones, tablets, and desktops. This enabled code reuse and accelerated development cycle.

To address the growing demand for cross-platform app development, Microsoft acquired Xamarin in 2016\. Xamarin allowed developers to use C# and the .NET framework to build mobile apps that could run on iOS, Android, and Windows devices. Xamarin.Forms, a UI framework, facilitated the development of cross-platform user interfaces, while Xamarin.Native enabled the creation of platform-specific experiences.

As the mobile landscape continued to evolve, Microsoft recognized the need for a unified framework that could target multiple platforms. This led to the development of .NET MAUI.

[.NET MAUI](#contents.xhtml_sc2_223a)

.NET MAUI (pronounced m-OW-ee, after the second largest island of Hawaii) is an evolution of Xamarin.Forms, providing a single codebase and a unified framework for building cross-platform apps targeting iOS, Android, Tizen, Windows, and macOS. It offers enhanced performance, improved tooling, and a wide range of UI controls and features. With .NET MAUI, developers can leverage their existing .NET skills and use a single codebase to create stunning and responsive user interfaces that run seamlessly on multiple platforms. At the same time, it is possible to add platform-specific source code and resources if necessary. .NET MAUI integrates with Blazor, so it is possible to reuse existing Blazor web UI components directly in native mobile and desktop apps.

![](images/Figure_9.1.png)

Figure 9.1: NET MAUI targets multiple platforms from a single codebase[1](#ch09.xhtml_footnote-000)

* * *

[1](#ch09.xhtml_footnote-000-backlink) Source: [https://learn.microsoft.com/en-us/dotnet/maui/what-is-maui](https://learn.microsoft.com/en-us/dotnet/maui/what-is-maui)

.NET MAUI provides a single framework for building the UIs for mobile and desktop apps by unifying Android, iOS, macOS, and Windows APIs into a single API that allows a write-once run-anywhere developer experience. That means the app looks and behaves like a native Mac app on Mac (via App Catalyst), a native Android app on Android, or a native Windows app on Windows. Additionally, the cross-platform APIs allow accessing native device features such as the GPS, the accelerometer, file system, notifications, battery, network states, and much more. .NET provides a series of platform-specific frameworks which have access to the .NET Base Class Library (BCL), which abstracts the details of the underlying platform away from the code:

![](images/Figure_9.2.png)

Figure 9.2: Architecture of .NET MAUI^([2](#ch09.xhtml_footnote-0001))

* * *

[2](#ch09.xhtml_footnote-0001-backlink) Source: [https://learn.microsoft.com/en-us/dotnet/maui/what-is-maui](https://learn.microsoft.com/en-us/dotnet/maui/what-is-maui)

By using multi-targeting and the use of SDK-style projects, .NET MAUI’s single project provides a simplified and consistent cross-platform development experience, regardless of the platforms being targeted.

[Pre-requisites](#contents.xhtml_sc2_224a)

Visual Studio 2022 Community Edition version 17.4 or later along with the .NET Multi-platform App UI development workload  with its default optional installation options is needed to work through the examples in this chapter.

[Getting started with .NET MAUI app](#contents.xhtml_sc2_225a)

Create a new .NET MAUI Application project by following the steps below in Visual Studio 2022:

| New project creation (File &#124; New &#124; Project…) |
| Create a new project | 1\. Narrow down the list of templates being shown by selecting Language: C#, Platform: All Platforms, Project type: MAUI.2\. Select template: .NET MAUI App3\. Click Next |
| Configure your new project | 4. Project name: Enter name of your choice such as FirstMauiApp.5. Location: Select the location of choice6. Solution: Select either Add to solution or Create new solution7. Solution name: Provide name in case a new solution is created.8. Place solution and project in the same directory: Normally, we keep the solution a level higher so leave it unchecked in case a new solution is created.9\. Click Create |

Table 9.1: Steps to create a new .NET MAUI application project.

The new project can be created using dotnet command line interface (CLI) with the following command:

dotnet  new maui --name FirstMauiApp

And to add the newly created project to the solution:

dotnet sln add ./FirstMauiApp/FirstMauiApp.csproj

[Structure of the (default) .NET MAUI App project](#contents.xhtml_sc3_226a)

On creating the new application using the built-in .NET  MAUI  App template the project looks as follows in the Solution Explorer.

![](images/Figure_9.3.png)

Figure 9.3: Structure of .NET MAUI project

The following files are created:

| Dependencies | The platform-specific dependencies for Android, iOS, MacCatalyst, and Windows are included here. |
| Properties &#124; launchSettings.json | This file lets you configure launch profiles that can be used when running your app via dotnet run. |
| Platforms | This folder contains child folder for each of the platforms that the .NET MAUI can target - Android, iOS, MacCatalyst, Tizen and Windows. The folders for each platform contain platform-specific resources, and code that starts the app on each platform. |
| Resources | This folder contains shared resources for each platform such as fonts, images, the app icon, the splash screen, raw assets, and CSS files. Each image resource file is used as a source image, from which images of the required resolutions are generated for each platform at build time. |
| App.xaml and App.xaml.cs | The App.xaml file contains app wide XAML resources, such as colors, styles, or templates. The App.xaml.cs file contains code that instantiates the Shell application. |
| AppShell.xaml and AppShell.xaml.cs | AppShell derives from Shell and serves as the single place to define the visual hierarchy of the app. |
| MainPage.xaml and MainPage.xaml.cs | This is the startup page displayed by the app. The MainPage.xaml file defines the UI (user interface) of the page. MainPage.xaml.cs contains the code-behind for the XAML, like code for a button click event. |
| MauiProgram.cs | This class bootstraps the application by exposing a static method CreateMauiApp invoked by each platform and gets an instance of MauiApp which serves as the entry point for the app. |

Table 9.2: Important files and folders in a .NET MAUI application project.

The sequence of invocation during application startup is as follows:

![](images/Figure_9.4.png)

Figure 9.4: Invocation during MAUI application startup

Let us examine the content of the project file FirstMauiApp.csproj below:

1. <Project  Sdk="Microsoft.NET.Sdk">

2.  <PropertyGroup>

3.  <TargetFrameworks>net7.0-android;net7.0-ios;net7.0-maccatalyst</TargetFrameworks>

4\. <TargetFrameworks  Condition="$([MSBuild]::IsOSPlatform('windows'))">$(TargetFrameworks);net7.0-windows10.0.19041.0</TargetFrameworks>

5\.      <!-- Uncomment to also build the tizen app. You will need to install tizen by following this: https://github.com/Samsung/Tizen.NET -->

6\. <!-- <TargetFrameworks>$(TargetFrameworks);net7.0-tizen</TargetFrameworks> -->

7\.      <OutputType>Exe</OutputType>

8\.       <RootNamespace>FirstMauiApp</RootNamespace>

9\.      <UseMaui>true</UseMaui>

10\.       <SingleProject>true</SingleProject>

11\.      <ImplicitUsings>enable</ImplicitUsings>

12. 

13.  <!-- Display name -->

14\.        <ApplicationTitle>FirstMauiApp</ApplicationTitle>

15. 

16\.        <!-- App Identifier -->

17\.      <ApplicationId>com.companyname.firstmauiapp</ApplicationId>

18.  <ApplicationIdGuid>c81b2bdd-8b3a-4127-92d4-
f183bf1de47e</ApplicationIdGuid>

19. 

20\.       <!-- Versions -->

21\.      <ApplicationDisplayVersion>1.0</ApplicationDisplayVersion>

22\.        <ApplicationVersion>1</ApplicationVersion>

23. 

24\. <SupportedOSPlatformVersion  Condition="$([MSBuild]::GetTargetPlatformIdentifier('$(TargetFramework)')) == 'ios'">11.0</SupportedOSPlatformVersion>

25\. <SupportedOSPlatformVersion  Condition="$([MSBuild]::GetTargetPlatformIdentifier('$(TargetFramework)')) == 'maccatalyst'">13.1</SupportedOSPlatformVersion>

26\. <SupportedOSPlatformVersion  Condition="$([MSBuild]::GetTargetPlatformIdentifier('$(TargetFramework)')) == 'android'">21.0</SupportedOSPlatformVersion>

27\. <SupportedOSPlatformVersion  Condition="$([MSBuild]::GetTargetPlatformIdentifier('$(TargetFramework)')) == 'windows'">10.0.17763.0</SupportedOSPlatformVersion>

28\. <TargetPlatformMinVersion  Condition="$([MSBuild]::GetTargetPlatformIdentifier('$(TargetFramework)')) == 'windows'">10.0.17763.0</TargetPlatformMinVersion>

29\.      <SupportedOSPlatformVersion  Condition="$([MSBuild]::GetTargetPlatformIdentifier('$(TargetFramework)')) == 'tizen'">6.5</SupportedOSPlatformVersion>

30\. </PropertyGroup>

31. 

32\. <ItemGroup>

33\.       <!-- App Icon -->

34\. <MauiIcon  Include="Resources\AppIcon\appicon.svg"  ForegroundFile="Resources\AppIcon\appiconfg.svg"  Color="#512BD4" />

35. 

36\.        <!-- Splash Screen -->

37\.      <MauiSplashScreen  Include="Resources\Splash\splash.svg"  Color="#512BD4"  BaseSize="128,128" />

38. 

39\.      <!-- Images -->

40\.       <MauiImage  Include="Resources\Images\*" />

41\.      <MauiImage  Update="Resources\Images\dotnet_bot.svg"  BaseSize="168,208" />

42. 

43\.      <!-- Custom Fonts -->

44\.        <MauiFont  Include="Resources\Fonts\*" />

45. 

46\.        <!-- Raw Assets (also remove the "Resources\Raw" prefix) -->

47\.       <MauiAsset  Include="Resources\Raw\**"  LogicalName="%(RecursiveDir)%(Filename)%(Extension)" />

48\. </ItemGroup>

49. 

50\. <ItemGroup>

51\.       <PackageReference  Include="Microsoft.Extensions.Logging.Debug"  Version="7.0.0" />

52\. </ItemGroup>

53. </Project>

The project file in the preceding code is an SDK style format (line 1) and multi-targets (line 3), using OS specific Target Framework Monikers (TFM). The SupportedOSPlatformVersion property (between lines 24 and 29) indicates the minimum OS version required to run the app. If not specified explicitly, this minimum run-time OS version in the project defaults to the platform version from the TFM. The entries within the ItemGroup section between lines 32 and 48 include different types of resources with specific build action to ensure that the item is accessible at runtime. When more resource files are added within the Resource folder, entries are automatically created in the project file.

To run the project, let us install the Android emulator. In the Visual Studio toolbar, use the Debug Target drop-down to select Android Emulators | Android Emulator. Clicking on Android Emulator for the first time, Visual Studio will start installing the default Android SDK and Android Emulator. Before proceeding, you may be prompted to accept Android license agreement. You may also be required to Enable Developer Mode in Windows settings. Once the Android SDK is downloaded and installed you need to create an Android device as follows:

![](images/Figure_9.5.png)

Figure 9.5: Prompt to create Android device

Clicking on Create will take some time to download and create the device in Android Device Manager:

![](images/Figure_9.6.png)

Figure 9.6: Android Device Manager

Once the device is installed, press the Pixel 5 - API 33 (Android 13.0 - API 33) button to build and run the app. When doing this for the first time it takes some time before showing the UI as follows:

![](images/Figure_9.7.png)

Figure 9.7: Project execution on Android device

Selecting Windows Machine from the Visual Studio toolbar, runs the Windows (WinUI) version of the application and shows up as follows:

![](images/Figure_9.8.png)

Figure 9.8: Project execution on Windows device

To run the application on an iOS device following launch profiles are provided as follows:

| iOS Local Devices | This allows a developer to deploy to a locally connected iOS device via iTunes using Apple Developer account credentials. |
| iOS Remote Devices | This allows to remotely pair with a Mac device and access Apple’s build tools, which only run on a Mac. |
| iOS Simulators | This allows to test apps on an iOS simulator. Once Visual Studio is paired with a Mac, select any simulator from the list to run the app. |

Table 9.3: iOS launch profiles for .NET MAUI application

[Creating .NET MAUI Blazor Hybrid Application](#contents.xhtml_sc3_227a)

In the preceding section we created the FirstMauiApp using the .NET MAUI App template. Another template .NET MAUI Blazor Hybrid App allows to create a blend of .NET MAUI application and Blazor. Such hybrid applications use a BlazorWebView component that enables Blazor within a MAUI application. All code runs as .NET code on the platform’s runtime in a single process. Components do not run in the browser, and WebAssembly is not involved. .NET MAUI Blazor Hybrid apps can run on all the platforms supported by .NET MAUI. However, component styles rendered in a Web View are platform dependent and may require accounting for rendering differences across platforms using custom stylesheets.

Let us now create the default Blazor Hybrid application and examine the major differences. Create a new project named FirstMauiBlazorApp choosing the .NET MAUI Blazor Hybrid App template. The project appears as follows in the Solution Explorer.

![](images/Figure_9.9.png)

Figure 9.9: .NET MAUI Blazor Hybrid App

It is evident from the preceding file and folder structure that the important files of a .NET MAUI program are still intact with the inclusion of the Blazor related razor pages (within Pages and Shared folders), data model classes (under Data folder) and CSS  resources under wwwroot folder. Some of the files which have changed are as follows.

MauiProgram.cs

1. using FirstMauiBlazorApp.Data;

2. using Microsoft.Extensions.Logging;

3. 

4. namespace FirstMauiBlazorApp;

5. public  static  class  MauiProgram

6. {

7\. public  static  MauiApp  CreateMauiApp()

8.   {

9\.       var builder = MauiApp.CreateBuilder();

10. builder

11\.             .UseMauiApp<App>()

12\.             .ConfigureFonts(fonts =>

13.  {

14\.                 fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");

15.  });

16. 

17. builder.Services.AddMauiBlazorWebView();

18.  

19. #if DEBUG

20.          builder.Services.AddBlazorWebViewDeveloperTools();

21\.       builder.Logging.AddDebug();

22. #endif

23.  

24.          builder.Services.AddSingleton<WeatherForecastService>();

25.  

26\. return builder.Build();

27.     }

28. }

The preceding code initializes the BlazorWebView control and registers WeatherForecastService.

MainPage.xaml

1. <?xml version="1.0" encoding="utf-8" ?>

2. <ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"

3.  xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" xmlns:local="clr-namespace:FirstMauiBlazorApp"

4.  x:Class="FirstMauiBlazorApp.MainPage" BackgroundColor="{DynamicResource PageBackgroundColor}">

5.      <BlazorWebView x:Name="blazorWebView" HostPage="wwwroot/index.html">

6. <BlazorWebView.RootComponents>

7.           <RootComponent Selector="#app" ComponentType="{x:Type local:Main}" />

8.          </BlazorWebView.RootComponents>

9\. </BlazorWebView>

10. </ContentPage>

The highlighted snippet in the preceding code adds the BlazorWebView. The RootComponent property ties it to the Blazor for rendering within the control. Running the project with Android device profile shows following UI.

![](images/1.png)

Figure 9.10: .NET MAUI Blazor hybrid application UI

[Developing real-world .NET MAUI App](#contents.xhtml_sc2_228a)

In the chapter on WPF we created a Sudoku Buddy application which demonstrated the key concepts around controls, layouts and MVVM pattern. In this chapter we will create the same application but this time using .NET MAUI. In such a migration we should be able to reuse most of the code within the .NET class files, that is, the Models, ViewModels and the implementation of MVVM based on the CommunityToolkit.MVVM NuGet package. However, the differences in the controls and layouts would force us to create the Views from scratch. This exercise should also lay out the path that any such migration would take in a real-world application. Before getting started, let us recapitulate what we had done for the Sudoku Buddy application using WPF.

[Recap – Sudoku Buddy WPF Application](#contents.xhtml_sc3_229a)

Sudoku Buddy is built around the traditional game of 9x9 Sudoku grid. The application helps the players know the candidates (or pencil marks) in each of the grid cell as new digits are typed. In the WPF implementation we had built the application around the MVVM pattern, creating the SudokuGrid model and three user controls corresponding to the Sudoku Grid, Box and Cell. Each control had their respective ViewModel class. The fields on the UI were bound to the properties in the ViewModel, making use of the helpful annotations from CommunitToolkit.Mvvm and its source generation capabilities which implemented the necessary Observability related glue code in the background. For more details of the working of MVVM, please refer to the WPF chapter.

[WPF vs. .NET MAUI](#contents.xhtml_sc3_230a)

Some of the major differences between WPF and .NET MAUI are summarized below

*   Cross-platform nature: .NET MAUI is designed to be a cross-platform framework that allows you to build applications for multiple platforms, including Windows, macOS, iOS, and Android. WPF, on the other hand, is primarily focused on Windows desktop applications.
*   UI Controls: While WPF offers a rich set of UI controls, not all of them are available in .NET MAUI. .NET MAUI has a more limited set of controls compared to WPF. However, it provides a unified set of controls that work across multiple platforms.
*   XAML Preview: In WPF, you can see a live preview of the UI design within the Visual Studio IDE. However, in .NET MAUI, the IDE does not provide a live preview of the UI screens being designed. You need to rely on the XAML code and executed the program to visualize the UI.
*   Project Structure: The project structure in .NET MAUI is different from WPF. .NET MAUI applications typically have a single project file that contains shared code and platform-specific projects for each target platform. This allows you to share majority of the codebase across platforms while having separate platform-specific projects for customizations. While .NET MAUI reaches mobile and desktop from a single codebase, there are vast differences in form factors, and developers need to cater to varying UX across devices.
*   Layout and Styling: While both WPF and .NET MAUI use XAML for UI design, there might be differences in layout and styling due to the cross-platform nature of .NET MAUI. Certain layout panels or styling features available in WPF may not be available or may behave differently in .NET MAUI.
*   Packaging and Deployment: Packaging and deployment mechanisms can differ between WPF and .NET MAUI. WPF applications are typically deployed as Windows desktop applications, while .NET MAUI applications can be deployed as standalone executables or packaged as platform-specific app packages for distribution.
*   Compatibility: WPF has been around for a while and has a large ecosystem of third-party controls, libraries, and resources. .NET MAUI is a newer framework, so it might not have the same level of compatibility with existing WPF libraries and resources. However, .NET MAUI is designed to be backward-compatible with Xamarin.Forms, which opens a wide range of existing Xamarin libraries.

[Migrating Sudoku Buddy from WPF to .NET MAUI](#contents.xhtml_sc3_231a)

Our basic approach to create the .NET MAUI version will remain the same, the difference being in the way we define the UI controls. Which also has impact on the other code. The UI for Sudoku Buddy when fully developed on .NET MAUI would look as follows on Windows:

![](images/Figure_9.11.png)

Figure 9.11: Empty Sudoku Buddy UI on Windows

When the sample grid is loaded it shows up as follows (on Windows):

![](images/Figure_9.12.png)

Figure 9.12: Sudoku Buddy on Windows

The same UI appears as follows on an Android simulator:

![](images/Figure_9.13.png)

Figure 9.13: Sudoku Buddy on Android

[Getting started](#contents.xhtml_sc4_232a)

Create a new project named SudokuBuddyMauiApp using the .NET MAUI App template choosing all the default options as described for the  FirstMAUIApp application earlier.

[Copy files from WPF application](#contents.xhtml_sc4_233a)

First, add reference to the NuGet package CommunityToolkit.Maui. On doing so you will be prompted to include a line of code in MauiProgram.cs.

MauiProgram.cs

1. using CommunityToolkit.Maui;

2. using Microsoft.Extensions.Logging;

3\.  

4. namespace SudokuBuddyMauiApp;

5. public  static  class  MauiProgram

6\. {

7.  public  static  MauiApp  CreateMauiApp()

8\.      {

9.  var builder = MauiApp.CreateBuilder();

10\.         builder

11.  .UseMauiApp<App>()

12.  .UseMauiCommunityToolkit()

13. .ConfigureFonts(fonts =>

14\. {

15. fonts.AddFont("OpenSans-Regular.ttf", "OpenSansRegular");

16. fonts.AddFont("OpenSans-Semibold.ttf", "OpenSansSemibold");

17\.             });

18.  

19. #if DEBUG

20. builder.Logging.AddDebug();

21\. #endif

22\.  

23.  return builder.Build();

24\.     }

25\. }

The highlighted line in the preceding code initializes the Maui Community Toolkit during application initialization.

Next, add reference to NuGet package CommunityToolkit.Mvvm. The changes to implement MVVM will remain same and can be referred from the WPF chapter. Copy the folders \SudokuBuddy\Helpers, \SudokuBuddy\Models and \SudokuBuddy\ViewModels from the SudokuBuddy WPF project including the files, under the project folder SudokuBuddyMauiApp. Since the namespaces of the copied classes will be different, right-click on the project in the solution explorer and select Sync Namespaces. Also run Code Cleanup. Do make sure that the namespaces in copied classes is in sync with their respective folder structure in the destination, if not, make the changes manually.

At this stage on compiling the project there will be an error in CellViewModel.cs. The class TextCompositionEventArgs is not recognized. To remove this compilation error, remove the changes related to PreviewTextInputCommand and PreviewTextInputHandler. After removing these, the complete file CellViewModel.cs appears as follows:

1. using CommunityToolkit.Mvvm.ComponentModel;

2. using CommunityToolkit.Mvvm.Input;

3. using SudokuBuddyMauiApp.Helpers;

4. using System.Windows.Input;

5\.  

6. namespace SudokuBuddyMauiApp.ViewModels;

7\.  

8. public  partial  class  CellViewModel : ObservableObject

9\. {

10.  [ObservableProperty]

11.  string _digit;

12\.  

13.   [ObservableProperty]

14.  string[] _candidates;

15\.  

16.   [ObservableProperty]

17.  bool _hasError;

18\.  

19.  [ObservableProperty]

20.   Visibility _candidatesVisibility;

21\.  

22.  public  int Row { get; set; }

23.  public  int Column { get; set; }

24.  public  BoxViewModel ParentBoxViewModel { get; set; }

25\.  

26.  public  CellViewModel()

27\.    {

28. Candidates = Array.Empty<string>();

29\.  

30. TextChangedCommand = new  RelayCommand(TextChangedHandler);

31\.    }

32.  public  ICommand TextChangedCommand { get; private  set; }

33\.  

34.  private  void  TextChangedHandler()

35\.    {

36.  this.SyncBoardAndViewModel();

37\.    }

38\. }

With the above changes the project should start compiling fine.

[Create Views](#contents.xhtml_sc4_234a)

In the WPF version we had created three user-controls corresponding to the views for Sudoku Grid, Box and Cell, those are not compatible with .NET MAUI, so we need to re-create the Views as ContentView. Create a new folder named Views and create three XAML based ContentView using the item template .NET MAUI ContentView (XAML) – SudokuView.xaml, BoxView.xaml and CellView.xaml. Now add following code in each of the View files.

CellView.xaml

1. <ContentView

2.  xmlns="http://schemas.microsoft.com/dotnet/2021/maui"

3.  xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"

4.  xmlns:vm="clr-namespace:SudokuBuddyMauiApp.ViewModels"

5.  xmlns:toolkit="http://schemas.microsoft.com/dotnet/2022/maui/toolkit"

6.  x:Class="SudokuBuddyMauiApp.Views.CellView">

7.  <ContentView.BindingContext>

8.  <vm:CellViewModel />

9.  </ContentView.BindingContext>

10.  <Border Stroke="Black" StrokeThickness="1">

11.  <Grid BackgroundColor="White">

12.  <Grid.RowDefinitions>

13. <RowDefinition Height="10" />

14.  <RowDefinition Height="10" />

15. <RowDefinition Height="10" />

16.   <RowDefinition Height="10" />

17. <RowDefinition Height="10" />

18.  </Grid.RowDefinitions>

19. <Grid.ColumnDefinitions>

20.  <ColumnDefinition Width="10" />

21. <ColumnDefinition Width="10" />

22.  <ColumnDefinition Width="10" />

23. <ColumnDefinition Width="10" />

24.  <ColumnDefinition Width="10" />

25. </Grid.ColumnDefinitions>

26.  <!--Digit-->

27. <Entry Style="{StaticResource DigitStyle}" Text="{Binding Digit, Mode=TwoWay}" Grid.Row="0" Grid.Column="1"

28.  Grid.RowSpan="4" Grid.ColumnSpan="4" Focused="OnGotFocusHandler"

29. Unfocused="OnLostFocusHandler" Keyboard="Numeric" MaxLength="1" >

30.  <Entry.Behaviors>

31.  <toolkit:EventToCommandBehavior EventName="TextChanged" Command="{Binding TextChangedCommand}" />

32.  </Entry.Behaviors>

33.  </Entry>

34.  <!--Candidates or Pencil marks-->

35. <Label Grid.Row="0" Grid.Column="0" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[0]}" />

36.  <Label Grid.Row="1" Grid.Column="0" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[1]}" />

37. <Label Grid.Row="2" Grid.Column="0" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[2]}" />

38.  <Label Grid.Row="3" Grid.Column="0" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[3]}" />

39. <Label Grid.Row="4" Grid.Column="0" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[4]}" />

40.  <Label Grid.Row="4" Grid.Column="1" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[5]}" />

41. <Label Grid.Row="4" Grid.Column="2" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[6]}" />

42.  <Label Grid.Row="4" Grid.Column="3" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[7]}" />

43. <Label Grid.Row="4" Grid.Column="4" Style="{StaticResource PencilMarkStyle}" Text="{Binding Candidates[8]}" />

44.  </Grid>

45.  </Border>

46. </ContentView>

In the preceding code we have setup a Grid to arrange the cell Digit and the possible Candidates in each cell. In the WPF version, we were able to use the Uniform Grid control but the same is not available in .NET MAUI. In its place we have defined a 5x5 grid and arranged the digits and candidates in each grid cell as follows:

![](images/Figure_9.14.png)

Figure 9.14: Defining CellView using Grid containing 9 candidates and 1 digit

Another uncommon thing is the specification of row height and column width in Grid definition. Normally, this should not be required but without these hardcoded values the controls do not space out well on the available page; probably this indicates work in progress at .NET MAUI end.

The Entry.Behavior defined between lines 30 and 32 tie the TextChanged event to the TextChangedCommand (copied previously in CellViewModel from the WPF version) via EventToCommandBehavior from the MAUI Toolkit. The attributes Focused and Unfocused on lines 28 and 29, point to the respective event handlers defined in the code-behind file given below:

CellView.cs

1\. ...

2. private  void  OnLostFocusHandler(object sender, FocusEventArgs e)

3\. {

4. ((Entry)sender).BackgroundColor = Color.Parse("White");

5\. }

6\.  

7. private  void  OnGotFocusHandler(object sender, FocusEventArgs e)

8\. {

9. ((Entry)sender).BackgroundColor = Color.Parse("LightSteelBlue");

10\. }

The code behind in the preceding snippet corresponds to changing the background color on entering and moving away from the cell.

BoxView.xaml

1\. <?xml version="1.0" encoding="utf-8" ?>

2. <ContentView x:Class="SudokuBuddyMauiApp.Views.BoxView" xmlns="http://schemas.microsoft.com/dotnet/2021/maui"

3.  xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" xmlns:local="clr-namespace:SudokuBuddyMauiApp.Views"

4.  xmlns:toolkit="http://schemas.microsoft.com/dotnet/2022/maui/toolkit"

5.  xmlns:vm="clr-namespace:SudokuBuddyMauiApp.ViewModels">

6.  <ContentView.BindingContext>

7.  <vm:BoxViewModel />

8.  </ContentView.BindingContext>

9.  <Border Stroke="Black" StrokeThickness="2">

10.  <Grid>

11.  <toolkit:UniformItemsLayout BindableLayout.ItemsSource="{Binding Cells}" MaxColumns="3" MaxRows="3">

12.  <BindableLayout.ItemTemplate>

13.  <DataTemplate>

14.  <local:CellView />

15.  </DataTemplate>

16.  </BindableLayout.ItemTemplate>

17.  </toolkit:UniformItemsLayout>

18.  </Grid>

19.  </Border>

20. </ContentView>

BoxView in the preceding code consumes the CellView and creates the Sudoku box containing 9 cells in a 3x3 arrangement. UniformItemsLayout from the CommunityToolkit.Maui along with BindingLayout is used.

SudokuView.xaml

1\. <?xml version="1.0" encoding="utf-8" ?>

2. <ContentView x:Class="MySudokuBuddyMauiApp.Views.SudokuView" xmlns="http://schemas.microsoft.com/dotnet/2021/maui"

3. xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" xmlns:local="clr-namespace:MySudokuBuddyMauiApp.Views"

4. xmlns:toolkit="http://schemas.microsoft.com/dotnet/2022/maui/toolkit"

5.  xmlns:vm="clr-namespace:MySudokuBuddyMauiApp.ViewModels">

6.  <ContentView.BindingContext>

7.  <vm:SudokuViewModel />

8.  </ContentView.BindingContext>

9.  <Grid>

10.  <Grid.RowDefinitions>

11. <RowDefinition Height="auto" />

12.  <RowDefinition />

13. </Grid.RowDefinitions>

14.  <Grid.ColumnDefinitions>

15. <ColumnDefinition />

16.  <ColumnDefinition Width="auto" />

17. </Grid.ColumnDefinitions>

18.  <toolkit:UniformItemsLayout BindableLayout.ItemsSource="{Binding Boxes}" MaxColumns="3" MaxRows="3" Grid.Row="0"

19.  Grid.Column="0" Grid.RowSpan="2">

20.  <BindableLayout.ItemTemplate>

21.  <DataTemplate>

22.  <local:BoxView />

23.  </DataTemplate>

24.  </BindableLayout.ItemTemplate>

25.  </toolkit:UniformItemsLayout>

26.  <Button Command="{Binding LoadSampleCommand}" Grid.Row="0" Grid.Column="1" Text="Load Sample"

27.  HorizontalOptions="FillAndExpand" VerticalOptions="Start" Margin="10,5" />

28.  <Button Command="{Binding ClearCommand}" Grid.Row="1" Grid.Column="1" Text="Clear"

29.  HorizontalOptions="FillAndExpand" VerticalOptions="Start" Margin="10,5" />

30.  </Grid>

31. </ContentView>

SudokuView also uses UniformItemsLayout and BindingLayout to define 9 boxes between lines 18 and 25\. Along with that there are two buttons to load a sample Sudoku grid values and clear the grid.

MainPage.xaml

1\. <?xml version="1.0" encoding="utf-8" ?>

2. <ContentPage x:Class="SudokuBuddyMauiApp.MainPage" xmlns="http://schemas.microsoft.com/dotnet/2021/maui"

3.  xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml" xmlns:local="clr-namespace:SudokuBuddyMauiApp.Views">

4.  <ScrollView>

5.  <Grid>

6.  <local:SudokuView />

7.  </Grid>

8.  </ScrollView>

9. </ContentPage>

The preceding code includes the SudokuView ContentView on line 6\. Remove the default OnCounterClicked handler and the count private variable from MainPage.cs code behind file.

Create AppStyles.xaml within \Resources\Styles folder with following content:

1\. <?xml version="1.0" encoding="utf-8" ?>

2. <ResourceDictionary xmlns="http://schemas.microsoft.com/dotnet/2021/maui"

3.  xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml">

4.  <Style x:Key="DigitStyle" TargetType="Entry">

5.  <Setter Property="FontSize" Value="18" />

6.  <Setter Property="FontAttributes" Value="Bold" />

7.  <Style.Triggers>

8.  <DataTrigger Binding="{Binding HasError, Mode=OneWay}" Value="True" TargetType="Entry">

9.  <Setter Property="TextColor" Value="Red" />

10.  </DataTrigger>

11. <DataTrigger Binding="{Binding HasError, Mode=OneWay}" Value="False" TargetType="Entry">

12.  <Setter Property="TextColor" Value="Blue" />

13. </DataTrigger>

14.  </Style.Triggers>

15.  </Style>

16.  <Style x:Key="PencilMarkStyle" TargetType="Label">

17.  <Setter Property="HorizontalOptions" Value="Center" />

18.  <Setter Property="VerticalOptions" Value="Center" />

19.  <Setter Property="TextColor" Value="CornflowerBlue" />

20.  <Setter Property="FontSize" Value="9" />

21.  </Style>

22. </ResourceDictionary>

Include the style resource by adding following line in App.xaml.

<ResourceDictionary Source="Resources/Styles/AppStyles.xaml" />

To size the startup window, include following method in App.xaml.cs

1. protected  override  Window  CreateWindow(IActivationState activationState)

2\. {

3.   var window = base.CreateWindow(activationState);

4\.  

5\.  

6.  window.Width = 645;

7.   window.Height = 570;

8\.  

9.  return window;

10\. }

Finally, in AppShell.xaml change the default title from Home to Sudoku Buddy. With the changes done so far, the UI should show up fine on Windows:

![](images/Figure_9.15.png)

Figure 9.15: Sudoku Buddy executing fine with Windows launch profile

[Running with Android Simulator](#contents.xhtml_sc4_235a)

Running the application with Android simulator however throws runtime exception - Index was outside the bounds of the array.

![](images/Figure_9.16.png)

Figure 9.16: Executing with Android simulator throws error

The error is caused by the fact that we are binding individual elements of the Candidates array in the CellView.xaml but of course not all elements may be applicable for a particular cell. This seems to be handled on Windows, but Android simulator may need a work around. We will ensure that instead of a variable number of elements in the Candidates array we will always have 9 elements and out of these only those values will be filled which are actual elements, rest values will remain empty. Make following changes. We can find all the places where changes are required, by doing a Find All References on the Candidates property in CellViewModel.

CellViewModel.cs

1\. ... 

2. public  CellViewModel()

3\. {

4.  Candidates = new  string[9];

5\.  

6. TextChangedCommand = new  RelayCommand(TextChangedHandler);

7\. }

8\. ...

SudokuGridExtensions.cs

1. ...

2. private  static  void  Update(SudokuGrid sudokuGrid, int r, int c, SudokuViewModel  sudokuViewModel)

3\. {

4. sudokuGrid.Candidates[r, c] = GetCandidates(sudokuGrid.Data, r, c);

5. 

6.  if (sudokuViewModel != null)

7.  {

8.   var initialCandidates = new  string[9];

9\.  

10.   var cellCandidates = sudokuGrid.Candidates[r, c].ToArray();

11\.         Array.Copy(cellCandidates, initialCandidates, cellCandidates.Length);

12\.  

13.       sudokuViewModel.Cells2DArray[r, c].Candidates = sudokuGrid.Candidates[r, c].ToArray();

14\.     }

15\. }

In the preceding code we have initialized the candidates array first with 9 empty values (line 8). Thereafter the actual candidates are copied into that (line 11). This will ensure elements are always 9 although some elements may be empty. Similar changes are done in SudokuViewModel.

SudokuViewModel.cs

1\. ...

2. private  void  InitializeBoxes()

3\. {

4.  ... 

5.  if (SudokuBoard.Data[k, l] != 0)

6. {

7. cell.Digit = SudokuBoard.Data[k, l].ToString();

8\.                     }

9.  else

10.                     {

11.  var c = SudokuBoard.Candidates[k, l]?.ToArray();

12.  Array.Copy(c, cell.Candidates, c.Length);

13. cell.CandidatesVisibility = true;

14.                     }

15\. ...

16\. }

The application should now run on Android simulator and show up as follows. To accommodate all the cells, we need to change to the horizontal orientation.

![](images/Figure_9.17.png)

Figure 9.17: Sudoku Buddy running on Android simulator after fixes

[Unit testing](#contents.xhtml_sc3_236a)

A real-world .NET MAUI typically uses MVVM pattern to design an application. This opens the door to unit-test the application at different layers of abstraction – models, view models, services. In the chapter on WPF we wrote unit-tests to verify the ViewModels, similar approach is applicable for the .NET MAUI version of Sudoku Buddy also. The end-to-end integration testing involving the UI components is in experimentation state. Please refer to one such initiative in the links in references.

[Deployment](#contents.xhtml_sc3_237a)

To package, publish, and deploy .NET MAUI applications on different platforms there are several options as summarized below. The choice is usually dependent on factors such as the target audience, distribution channels, update frequency, and deployment requirements specific to each platform.

*   Self-contained deployment: In this approach, the application and all its dependencies, including the .NET runtime, are bundled together as a single package. This package can be published and deployed as an executable file specific to each platform (e.g., APK for Android, IPA for iOS, EXE for Windows). It allows for easy distribution and installation on target devices, ensuring that the required runtime is included.
*   Framework-dependent deployment: With this method, the application is packaged separately from the .NET runtime. The runtime is assumed to be pre-installed on the target device or can be acquired through the operating system’s package manager. The application package includes only the application-specific files, reducing its size and allowing for more efficient updates. This approach is suitable when you can rely on the target device having the required runtime available.
*   App stores: Another option for deploying .NET MAUI applications is to publish them to the respective app stores for each platform—Google Play Store for Android, Apple App Store for iOS or the Microsoft Store for Windows applications. App store deployment provides a centralized distribution platform, allowing users to easily discover and install your application.
*   Side-loading: This method involves manually installing the application package on the target device without using an app store. Side-loading is useful for distributing applications internally within an organization or for testing purposes. You can directly install the application package on Android devices through APK files or on iOS devices through IPA files. Windows supports side-loading through appx or MSIX packages.
*   Continuous Integration and Deployment (CI/CD): CI/CD tools such as Azure DevOps, Jenkins, or GitHub Actions can be used to automate the packaging and deployment process. By integrating your repository with these tools, you can set up build pipelines that build, package, and publish your .NET MAUI application automatically whenever changes are pushed to the repository. This allows for efficient and consistent distribution of the application to multiple platforms.

Application deployment across platforms is an evolving field, so it is important to stay up to date with the latest developments and guidelines from the platform providers to ensure smooth packaging, publishing, and deployment of your .NET MAUI applications. Specific information can be found in the deployment link in the references.

[Conclusion](#contents.xhtml_sc2_238a)

In conclusion, .NET MAUI is a powerful tool for building cross-platform applications that allow developers to leverage their existing C# and .NET skills. This chapter has covered the basics of .NET MAUI, including its role in the .NET ecosystem and its key features. With .NET MAUI, developers can create native desktop and mobile applications with a single codebase, reducing development time and increasing productivity. By following the steps outlined in this chapter, developers can get started with .NET MAUI and begin building their own cross-platform applications today.

[Points to remember](#contents.xhtml_sc2_239a)

Following are some of the important points to remember when working with .NET MAUI:

*   .NET MAUI (Multi-platform App UI) is a cross-platform framework for building native mobile and desktop apps with C# and XAML. With .NET MAUI, you can develop apps that can run on Android, iOS, macOS, and Windows from a single shared codebase. It is possible to add platform-specific source code and resources if necessary.
*   .NET MAUI is open source and is the evolution of Xamarin.Forms, extended from mobile to desktop scenarios, with UI controls rebuilt from the ground up for performance and extensibility
*   The use of MVVM (Model-View-ViewModel) architectural pattern is recommended for building .NET MAUI applications. MVVM promotes separation of concerns, making it easier to maintain and test your codebase.
*   .NET MAUI provides a wide range of UI controls and layouts to create responsive and visually appealing user interfaces.
*   When designing the UI for a .NET MAUI application, keep platform-specific guidelines in mind to ensure a native look and feel on each target platform. Tailor your app’s UI to match the design principles and user expectations of iOS, Android, Windows, and other platforms.
*   Take advantage of .NET MAUI’s cross-platform services and APIs to access platform-specific functionality when needed. This includes accessing device sensors, handling push notifications, working with platform-specific file systems, and more.
*   .NET MAUI and Blazor Hybrid apps provide a single codebase for building native apps and web apps, which can save development time and increase productivity

[Exercises](#contents.xhtml_sc2_240a)

*   Create .NET MAUI Blazor application using the Cows and Bulls application created in the chapter on Blazor.

[Hint: Attempt to create the two variations of the game starting with a new project using .NET MAUI Blazor App template. Copy pages from CowsAndBulls.Client and class files from CowsAndBulls.Shared]

[References](#contents.xhtml_sc2_241a)

*   What is .NET MAUI?

[https://learn.microsoft.com/en-us/dotnet/maui/what-is-maui](https://learn.microsoft.com/en-us/dotnet/maui/what-is-maui)

*   Target multiple platforms from .NET MAUI single project

[https://learn.microsoft.com/en-us/dotnet/maui/fundamentals/single-project](https://learn.microsoft.com/en-us/dotnet/maui/fundamentals/single-project)

*   Introducing .NET Multi-platform App UI

[https://devblogs.microsoft.com/dotnet/introducing-net-multi-platform-app-ui/](https://devblogs.microsoft.com/dotnet/introducing-net-multi-platform-app-ui/)

*   Introducing .NET MAUI – One Codebase, Many Platforms

[https://devblogs.microsoft.com/dotnet/introducing-dotnet-maui-one-codebase-many-platforms/](https://devblogs.microsoft.com/dotnet/introducing-dotnet-maui-one-codebase-many-platforms/)

*   MAUI Sounds Amazing. Is It?

[https://www.leerichardson.com/2022/12/maui-sounds-amazing-is-it.html](https://www.leerichardson.com/2022/12/maui-sounds-amazing-is-it.html)

*   What is .NET MAUI, and How Does it Differ from Xamarin?

[https://ballardchalmers.com/resources/what-is-net-maui-and-how-does-it-differ-from-xamarin/](https://ballardchalmers.com/resources/what-is-net-maui-and-how-does-it-differ-from-xamarin/)

*   Xamarin Versus .NET MAUI

[https://medium.com/syncfusion/xamarin-versus-net-maui-df37727801d2](https://medium.com/syncfusion/xamarin-versus-net-maui-df37727801d2)

*   Going Desktop With .NET MAUI

[https://www.telerik.com/blogs/going-desktop-dotnet-maui](https://www.telerik.com/blogs/going-desktop-dotnet-maui)

*   What’s new in .NET MAUI for .NET 7

[https://learn.microsoft.com/en-us/dotnet/maui/whats-new/dotnet-7?view=net-maui-7.0](https://learn.microsoft.com/en-us/dotnet/maui/whats-new/dotnet-7?view=net-maui-7.0)

*   Build your first app

[https://learn.microsoft.com/en-us/dotnet/maui/get-started/first-app?tabs=vswin&pivots=devices-android](https://learn.microsoft.com/en-us/dotnet/maui/get-started/first-app?tabs=vswin&pivots=devices-android)

*   Create a .NET MAUI app

[https://learn.microsoft.com/en-us/dotnet/maui/tutorials/notes-app/](https://learn.microsoft.com/en-us/dotnet/maui/tutorials/notes-app/)

*   A curated list of awesome .NET MAUI samples

[https://github.com/jsuarezruiz/dotnet-maui-showcase](https://github.com/jsuarezruiz/dotnet-maui-showcase)

*   Align and position .NET MAUI controls

[https://learn.microsoft.com/en-us/dotnet/maui/user-interface/align-position?view=net-maui-7.0](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/align-position?view=net-maui-7.0)

*   Bindable Layout

[https://learn.microsoft.com/en-us/dotnet/maui/user-interface/layouts/bindablelayout](https://learn.microsoft.com/en-us/dotnet/maui/user-interface/layouts/bindablelayout)

*   .NET Multi-platform App UI (.NET MAUI) Community Toolkit documentation

[https://learn.microsoft.com/en-us/dotnet/communitytoolkit/maui/](https://learn.microsoft.com/en-us/dotnet/communitytoolkit/maui/)

*   Uniform Items Layout

[https://learn.microsoft.com/en-us/dotnet/communitytoolkit/maui/layouts/uniformitemslayout](https://learn.microsoft.com/en-us/dotnet/communitytoolkit/maui/layouts/uniformitemslayout)

*   ASP.NET Core Blazor Hybrid

[https://learn.microsoft.com/en-us/aspnet/core/blazor/hybrid/?view=aspnetcore-7.0](https://learn.microsoft.com/en-us/aspnet/core/blazor/hybrid/?view=aspnetcore-7.0)

*   Blazor Hybrid Web Apps with .NET MAUI

[https://www.codemag.com/Article/2111092/Blazor-Hybrid-Web-Apps-with-.NET-MAUI](https://www.codemag.com/Article/2111092/Blazor-Hybrid-Web-Apps-with-.NET-MAUI)

*   Experimenting with UI Testing approaches for .NET / MAUI

[https://github.com/Redth/Maui.UITesting](https://github.com/Redth/Maui.UITesting)

*   Deployment

[https://learn.microsoft.com/en-us/dotnet/maui/deployment/](https://learn.microsoft.com/en-us/dotnet/maui/deployment/)

Join our book’s Discord space

Join the book’s Discord Workspace for Latest updates, Offers, Tech happenings around the world, New Release and Sessions with the Authors:

**[https://discord.bpbonline.com](https://discord.bpbonline.com)**

![](images/fm1.png)

# [CHAPTER 10ML.NET](#contents.xhtml_ch10a)

[Introduction](#contents.xhtml_sc2_242a)

Machine learning has emerged as a transformative technology, involving the use of algorithms and statistical models to enable computers to learn from data and make predictions without requiring explicit programming. ML.NET is an open-source, cross-platform machine learning framework developed by Microsoft that enables developers to build custom machine learning models using C# or F#. This chapter provides an overview of machine learning and how to use ML.NET to solve some real-world problems.

[Structure](#contents.xhtml_sc2_243a)

This chapter has following topics.

*   Overview of machine learning
*   ML.NET
*   Pre-requisites
*   Getting started with ML.NET
    *   Machine Learning Process
    *   Binary classification using ML.NET API
        *   Binary classification
        *   Sentiment dataset
        *   Creating the program
    *   Regression analysis using Model Builder
        *   Model Builder
        *   Regression analysis
        *   Insurance dataset
        *   Creating the program
*   Anomaly detection in financial dataset
    *   Anomaly detection
    *   Synthetic financial dataset for fraud detection
    *   Principal Component Analysis algorithm
    *   Creating the program
        *   Data preparation
        *   Model training
        *   Prediction
    *   Unit testing
        *   Create unit test
    *   Deployment
        *   Deployment considerations
        *   Ways to deploy
        *   Thread-safety of Prediction Engine

[Objectives](#contents.xhtml_sc2_244a)

The objective of this chapter is to understand the concepts of machine learning and explore the capabilities of ML.NET in solving various tasks by building efficient machine learning models. This chapter should get you started solving machine learning problems using ML.NET with C# and Visual Studio as the tools. The aim is to evoke enough curiosity for you to learn in depth about machine learning. To this end, the resources given in the reference section, would be a good starting point in the pursuit of learning further.

[Overview of machine learning](#contents.xhtml_sc2_245a)

Machine learning (ML) is a subset of artificial intelligence (AI) which enables computer systems to learn from data models and improve from experience, without being explicitly programmed. For this reason, it is often referred to as programming the unprogrammed. Unlike traditional programming, where explicit rules and instructions are coded, machine learning involves the development of algorithms and models that can automatically learn and make predictions or decisions based on patterns and relationships in data.

As the broader concept, AI encompasses a broader range of concepts and techniques to create intelligent systems. Machine learning relies heavily on data, while AI can incorporate various approaches, including symbolic reasoning and knowledge representation, in addition to machine learning techniques.

Some of the techniques and scenarios in machine learning are depicted below in [Figure 10.1](#ch10.xhtml_fig10-1):

![](images/Figure_10.1.png)

Figure 10.1: Machine learning scenarios

The field continues to evolve rapidly, with new algorithms and approaches being developed to tackle increasingly complex problems.

[ML.NET](#contents.xhtml_sc2_246a)

ML.NET is an open-source, cross-platform machine learning framework developed by Microsoft that enables developers to integrate machine learning models into their applications using .NET programming languages like C# and F#. ML.NET simplifies the process of building, training, and deploying machine learning models by providing a high-level API and a range of built-in algorithms and data transformation components.

ML.NET was introduced by Microsoft in 2018 as an experimental project, and it has since evolved into a stable and mature framework. It has undergone updates and improvements, expanded its capabilities and become a powerful tool for machine learning tasks in the .NET ecosystem.

ML.NET can be applied to various types of machine learning problems. The different scenarios along with some examples are tabulated below in [Table 10.1](#ch10.xhtml_tab10-1):

| Scenario | Problem example |
| --- | --- |
| Binary classification |  
*   Spam detection: Classify emails as spam or non-spam based on their content and metadata.
*   Fraud detection: Identify fraudulent transactions in a financial dataset.
*   Disease diagnosis: Predict whether a patient has a specific disease based on symptoms and medical history.

 |
| Multiclass classification |  
*   Image classification: Classify images into different categories such as cats, dogs, and birds.
*   Sentiment analysis: Determine the sentiment of a text (positive, negative, or neutral).
*   Handwriting recognition: Recognize handwritten digits or characters.

 |
| Anomaly detection |  
*   Intrusion detection: Detect network intrusions or cyber-attacks by identifying anomalous patterns in network traffic.
*   Equipment failure prediction: Identify anomalies in sensor data to predict potential equipment failures.
*   Fraudulent activity detection: Identify unusual patterns in financial transactions that may indicate fraudulent activity.

 |
| Clustering |  
*   Customer segmentation: Group customers based on their purchasing behavior or demographics for targeted marketing strategies.
*   Document clustering: Cluster similar documents together for document organization or topic extraction.
*   Image segmentation: Group pixels in an image with similar characteristics to identify objects or regions.

 |
| Forecasting |  
*   Sales forecasting: Predict future sales based on historical sales data, seasonality, and external factors.
*   Stock market prediction: Forecast stock prices based on historical price trends and market indicators.
*   Energy demand forecasting: Predict energy consumption for efficient resource planning and energy management.

 |
| Ranking |  
*   Search engine ranking: Rank search results based on relevance and user preferences.
*   Product recommendation  ranking: Rank recommended products based on user preferences and historical data.
*   News article ranking: Rank news articles based on their relevance to a user’s interests.

 |
| Regression |  
*   House price prediction: Predict the selling price of a house based on features like location, size, and amenities.
*   Demand forecasting: Predict the demand for a product based on historical sales data and market factors.
*   Crop yield prediction: Estimate crop yields based on factors like weather conditions, soil quality, and agricultural practices.

 |
| Recommendation |  
*   Movie recommendation: Provide personalized movie recommendations to users based on their viewing history and preferences.
*   Music recommendation: Recommend songs or playlists based on a user’s listening history and music preferences.
*   E-commerce product recommendation: Suggest products to customers based on their browsing history and purchase behavior.

 |
| Time Series |  
*   Stock price prediction: Forecast future stock prices based on historical price patterns and market indicators.
*   Weather forecasting: Predict weather conditions such as temperature, precipitation, and wind speed.
*   Energy load forecasting: Forecast electricity demand to optimize power generation and distribution.

 |

Table 10.1: Machine learning scenarios supported by ML.NET

[Pre-requisites](#contents.xhtml_sc2_247a)

Visual Studio 2022 Community Edition version or higher with the .NET desktop development workload along with the optional ML.NET Model Builder component is needed to work through the examples in this chapter. If you already have Visual Studio 2022, you should update it to the latest release by launching the Visual Studio Installer. Similarly, the ML.NET Model Builder component can be updated from within Visual Studio via Extensions | Manage Extensions menu option or by downloading and re-installing from Visual Studio Marketplace.

[Getting started with ML.NET](#contents.xhtml_sc2_248a)

ML.NET does not have a specific project template in Visual Studio, any project type, desktop or web can include machine learning capabilities by including the NuGet package Microsoft.ML. We will first create two simple programs to understand the overall flow while solving a machine learning problem. One that uses ML.NET API directly and another that uses the Visual Studio’s Model Builder extension. Later we will create a program that uses a large financial dataset and works end-to-end with it. But before going to write any code, let us understand the typical process followed for a machine learning problem.

[Machine learning process](#contents.xhtml_sc3_249a)

For any machine learning problem, the actual implementation can vary depending on the specific task, data and techniques or algorithms used, however at a high level the process for any machine learning task can be summarized in the following steps, also depicted in [Figure 10.2](#ch10.xhtml_fig10-2) as follows:

![](images/Figure_10.2.png)

Figure 10.2: The machine learning process

1.  Define the problem: Clearly articulate the problem you want to solve using machine learning. This involves understanding the desired outcome, the available data, and any constraints or limitations.
2.  Gather and preprocess data: Collect relevant data that will be used to train and evaluate your machine learning model. This data can come from various sources, such as databases, APIs, or manual labeling. Preprocess the data by cleaning it, handling missing values, and transforming it into a suitable format for analysis.
3.  Split the data: Divide the collected data into two or three sets: the training set, the validation set, and the test set. The training set is used to train the model, the validation set helps in tuning hyperparameters and evaluating model performance during development, and the test set is used for the final evaluation of the trained model.
4.  Select a model: Choose an appropriate machine learning algorithm or model that is well-suited for your problem. This choice depends on factors such as the nature of the data, the type of problem (classification, regression, clustering, etc.), and the available computational resources.
5.  Train the model: Use the training set to train the selected model. The model learns from the input data with a goal to minimize the difference between predictions and the actual outcomes in the training set by adjusting its internal parameters. This process typically involves an optimization algorithm that updates the model’s parameters iteratively.
6.  Evaluate the model: Assess the performance of the trained model using the validation set. This step helps in tuning the model’s hyperparameters and selecting the best configuration that generalizes well to unseen data. Common evaluation metrics include accuracy, precision, recall, F1 score, area under ROC, mean squared error, or other domain-specific metrics.
7.  Fine-tune the model: Adjust the hyperparameters of the model based on the performance evaluation on the validation set. This can involve changing learning rates, regularization techniques, or other parameters specific to the chosen algorithm. The goal is to improve the model’s performance and generalization capabilities.
8.  Predict using the model: Once the model has been trained and fine-tuned, evaluate its performance on the test set by doing one or more predictions. This set represents real-world, unseen data, and provides an unbiased assessment of the model’s effectiveness. The results obtained from this step give a final measure of the model’s performance and help in assessing its readiness for deployment.
9.  Deploy the model: If the model performs satisfactorily on the test set, it can be deployed in a production environment. This may involve integrating the model into an application, setting up appropriate infrastructure, and monitoring its performance and predictions over time.
10.  Monitor and maintain the model: Continuously monitor the model’s performance and retrain or update it periodically as new data becomes available. It is important to ensure that the model remains accurate and reliable in the changing environment and that it adapts to any evolving patterns or trends.

[Binary classification using ML.NET API](#contents.xhtml_sc3_250a)

To get started, we will create a simple program that uses binary classification algorithm from ML.NET to perform sentiment analysis. Sentiment analysis characterizes a review comment as a positive or a negative feedback comment.

[Binary classification](#contents.xhtml_sc3_251a)

Binary classification is a supervised machine learning task, meaning that the model gets trained on a labelled dataset having both input and output parameters where the algorithms learn to map points between inputs and correct outputs. The goal in binary classification is to classify data into one or two distinct classes or categories which are mutually exclusive. The two classes are often referred to as positive and negative, or sometimes as class 1 and class 0\. The input data consists of a set of features or attributes that describe each sample, and the output is a binary label indicating which class the sample belongs to.

[Sentiment dataset](#contents.xhtml_sc3_252a)

Download the UCI Sentiment Labeled Sentences dataset from the link given in references. This dataset contains sentences labelled with positive or negative sentiment for three different websites: [imdb.com](https://imdb.com), [amazon.com](https://amazon.com), and [yelp.com](https://yelp.com). Extract the movie review file imdb_labelled.txt which we will use later in our program. The first few rows in the file appear in [Table 10.2](#ch10.xhtml_tab10-2) as follows:

| A very, very, very slow-moving, aimless movie about a distressed, drifting young man. | 0 |
| Not sure who was more lost - the flat characters or the audience, nearly half of whom walked out. | 0 |
| Attempting artiness with black & white and clever camera angles, the movie disappointed - became even more ridiculous - as the acting was poor and the plot and lines almost non-existent. | 0 |
| Very little music or anything to speak of. | 0 |
| The best scene in the movie was when Gerardo is trying to find a song that keeps running through his head. | 1 |

Table 10.2: Preview of IMDB sentiment dataset

The data is tab delimited, without header row and contains a sentence text and the corresponding score which is either 1 for positive or 0 for negative feedback (or sentiment). The file contains 500 positive and 500 negative sentences which were randomly extracted from reviews of movies. The selected sentences have a clearly positive or negative connotation with no neutral sentences being selected.

[Creating the program](#contents.xhtml_sc3_253a)

Create a new Console Application named SentimentAnalysis within your solution at a location of choice and .NET 7.0 as the target framework version. Add the latest stable version of the NuGet package Microsoft.ML by Microsoft to your project. Copy the file imdb_labelled.txt into Datasets folder. Create two new classes under the Models folder as given below:

Sentiment.cs

1. using Microsoft.ML.Data;

2\.  

3. namespace SentimentAnalysis.Models;

4. public  class  Sentiment

5\. {

6.  [LoadColumn(0)]

7.  public  required  string Text { get; set; }

8\.  

9.  [LoadColumn(1)]

10. public  bool Label { get; set; }

11\.  

12. public  override  string  ToString()

13.  {

14.  return  $"Text: {Text}, Label: {(Label ? "Positive" : "Negative")}";

15.  }

16\. }

The preceding code declares a data model corresponding to the data that we plan to load from the dataset file. The LoadColumn attribute over each property maps with the specified source column in the dataset.

SentimentPrediction.cs

1. using Microsoft.ML.Data;

2\.  

3. namespace SentimentAnalysis.Models;

4. public  class  SentimentPrediction

5\. {

6. [ColumnName("PredictedLabel")]

7.  public  bool Prediction { get; set; }

8.  public  float Probability { get; set; }

9.  public  float Score { get; set; }

10\.  

11.  public  override  string  ToString()

12\.     {

13.  return  $"Prediction: {(Prediction ? "Positive" : "Negative")}, "

14.  + $"Probability: {Probability:P2}, Score:{Score}";

15.  }

16\. }

The SentimentPrediction class corresponds to the output class which is generated as part of the prediction step in Binary Classification. ML.NET has pre-defined property names for the prediction entity produced by a model. These properties differ depending on the task.

Now, replace the code in Program.cs with following lines of code as the first part of the program.

1. using Microsoft.ML;

2. using SentimentAnalysis.Models;

3\.  

4\. //Step 1\. Create an ML Context

5. var ctx = new  MLContext();

6\.  

7\. //Step 2\. Read in the input data from a text file for model training

8. var sentimentFile = Path.Combine(Directory.GetCurrentDirectory(), "./Datasets/imdb_labelled.txt");

9. var allData = ctx.Data.LoadFromTextFile<Sentiment>(sentimentFile, hasHeader: false);

10\.  

11\. //Split the dataset into training and test sets according to the given fraction

12. var trainTestSplit = ctx.Data.TrainTestSplit(allData, testFraction: 0.2);

13. var trainingData = trainTestSplit.TrainSet;

14. var testData = trainTestSplit.TestSet;

15\.  

16\. //Step 3: Common data process configuration with pipeline data transformations

17. var dataProcessPipeline = ctx.Transforms.Text.FeaturizeText(outputColumnName: "Features",

18. inputColumnName: nameof(Sentiment.Text));

19\.  

20\. //Add all the available Binary Classification trainers in a List for iterating later

21. var trainers = new  List<IEstimator<ITransformer>>

22\. {

23.   { ctx.BinaryClassification.Trainers.AveragedPerceptron() },

24. { ctx.BinaryClassification.Trainers.FieldAwareFactorizationMachine() },

25. { ctx.BinaryClassification.Trainers.LbfgsLogisticRegression() },

26. { ctx.BinaryClassification.Trainers.LdSvm() },

27. { ctx.BinaryClassification.Trainers.LinearSvm() },

28. { ctx.BinaryClassification.Trainers.Prior() },

29. { ctx.BinaryClassification.Trainers.SdcaLogisticRegression() },

30. { ctx.BinaryClassification.Trainers.SdcaNonCalibrated() },

31. { ctx.BinaryClassification.Trainers.SgdCalibrated() },

32. { ctx.BinaryClassification.Trainers.SgdNonCalibrated() }

33\. };

Line 5 in the preceding code creates the machine learning context which provides an entry point and an environment for any of the machine learning task in ML.NET, much like DBContext in Entity Framework. The next step on line 8 and 9 loads the dataset text files and creates an IDataView. 80% of the records in the dataset will be used for training the model and the remaining 20% to test its accuracy, line 12 splits the dataset accordingly. On line 17, the data processing pipeline is defined which transforms the text data into numerical features using the FeaturizeText method. This is done because machine learning algorithms typically work with numerical data, as they rely on mathematical operations to make predictions. The output column is named Features and it uses the Text property of the Sentiment class as the input. In ML.NET, there are several algorithms available to perform the binary classification, a List is prepared between lines 21 and 33 of all such algorithms (or trainers).

Next add the following, remaining lines of code in the program.

1. var sampleStatement = new  Sentiment { Text = "It was not worth the money", Label = false };

2. Console.WriteLine($"Test data:\n{sampleStatement}\n");

3\.  

4. var count = 0;

5. foreach (var trainer in trainers)

6\. {

7.  //Step 4: Set the training algorithm, then create and config the modelBuilder 

8.  var pipeline = dataProcessPipeline.Append(trainer);

9. 

10.  //Step 5\. Train your model with training data

11.  ITransformer trainedModel = pipeline.Fit(trainingData);

12\.  

13. //Step 6: Evaluate the model to determine accuracy stats

14.  var predictions = trainedModel.Transform(testData);

15.  var metrics = ctx.BinaryClassification.EvaluateNonCalibrated(predictions);

16\.  

17.  //Step 7\. Try making predictions using your trained model

18.   var predictionEngine = ctx.Model.CreatePredictionEngine<Sentiment, SentimentPrediction>(trainedModel);

19.  var prediction = predictionEngine.Predict(sampleStatement);

20\.  

21.  var trainerName = $"{trainer}";

22. trainerName = trainerName[(trainerName.LastIndexOf(".") + 1)..];

23\.  

24.  Console.WriteLine($"======= {++count}. {trainerName} | {prediction} ==");

25.  Console.WriteLine($"Accuracy: {metrics.Accuracy:P2}, ROC: {metrics.AreaUnderRocCurve:P2}, F1Score: {metrics.F1Score:P2}");

26.  Console.WriteLine($"======================================================
=============");

27\. }

28\.  

29. Console.WriteLine($"\nFinished, press any key to exit =======");

30. Console.ReadKey();

A sample statement is created for analysis on line 1 in the preceding code. The list of trainers created earlier is iterated. For each iteration, after setting the specific trainer (line 8), we train the model with the trainer (line 11), evaluate the accuracy of the model using the 20% test dataset (line 14 and 15), and perform the prediction for a sample sentiment value on line 18 and 19\. Line 24 to 26 print the output which shows up as follows when the program is executed:

![](images/Figure_10.3.png)

Figure 10.3: Output of Sentiment Analysis program

In the program output we can see the results for all the trainers. Notice that the prediction of LdSvmTrainer matches the expected Prediction: Negative and has the highest accuracy and other metrices values.

Next, we will use the Visual Studio extension ML.NET Model Builder to introduce automation in choosing the algorithms best suited for our scenario.

[Regression analysis using Model Builder](#contents.xhtml_sc3_254a)

In the previous example we iterated through the available binary classification algorithms (or trainers) to determine which might be a good fit for our scenario to make accurate prediction. In this section, we will work with the graphical Visual Studio extension Model Builder, to solve machine learning problems related to regression analysis.

[Model Builder](#contents.xhtml_sc4_255a)

Model Builder simplifies the process of building machine learning models. It is specifically designed to enable developers with little or no expertise in machine learning to create and train models using datasets. The extension provides a user-friendly interface and a guided workflow that makes it easier to build, train, and deploy models. It covers a wide range of tasks, including classification, regression, object detection, anomaly detection, and recommendation systems. It internally uses Automated Machine Learning (AutoML) that automates the process by making it easier to find the best algorithm for your scenario and dataset.

[Regression analysis](#contents.xhtml_sc4_256a)

Regression analysis is a supervised machine learning, statistical modeling technique used to understand the relationship between a dependent variable (usually referred to as label) and one or more independent variables (usually referred to as features). It is commonly used for prediction and forecasting tasks, including predicting prices. We will use this scenario to predict insurance premium costs determined by a combination of parameters.

[Insurance dataset](#contents.xhtml_sc4_257a)

Download the Insurance Premium Prediction from the popular data platform, Kaggle, via the link provided in references. You may need to register and create a free account before proceeding with the download. Extract the insurance data file insurance.csv to be used later in our program. The first few rows in the file will appear in [Table 10.3](#ch10.xhtml_tab10-3) as follows:

| age | sex | bmi | children | smoker | region | expenses |
| 19 | female | 27.9 | 0 | yes | southwest | 16884.92 |
| 18 | male | 33.8 | 1 | no | southeast | 1725.55 |
| 28 | male | 33 | 3 | no | southeast | 4449.46 |
| 33 | male | 22.7 | 0 | no | northwest | 21984.47 |
| 32 | male | 28.9 | 0 | no | northwest | 3866.86 |

Table 10.3: Preview of insurance dataset

The insurance data includes the expenses column (label) which represents the premium amount whose value is determined by the numerical features (age, bmi, and children) and nominal features (sex, smoker, and region).

[Creating the program](#contents.xhtml_sc4_258a)

Create a new Console Application named InsPremiumPrediction within your solution at a location of choice and .NET 7.0 as the target framework version. Copy the insurance.csv file into Datasets folder. Right-click on the project and click on Add | Machine Learning Model, select Insurance.mbconfig as the name of the file and click on Add button. This will launch the Model Builder UI. Refer to [Figure 10.4](#ch10.xhtml_fig10-4) given below:

![](images/Figure_10.4.png)

Figure 10.4: Model Builder wizard

Select the Value prediction scenario, followed by Local CPU as the training environment. The other option for training is the Azure cloud environment, which is available only for Image Classification and Object Detection scenarios. When training in the cloud, it is possible to scale up the resources to meet the demands of the scenario, especially for large datasets. Next, in the Data step, browse the path of insurance.csv from the project’s Datasets folder. Select expenses as the column to predict (or Label column). Verify the advanced data options which shows up in [Figure 10.5](#ch10.xhtml_fig10-5) as follows:

![](images/Figure_10.5.png)

Figure 10.5: Advanced data options in Model Builder

In the Column settings we can alter the data types for each column and whether it is a Feature or a Label. There is also an option to fine-tune the Data formatting and the training and test Validation data. The default options are good, click on Cancel to close the dialog. Move ahead to the Training step by clicking Next button. Generally, the training time is determined by the size of datasets, here since the dataset is only a few KBs 10 sec training time is fine. The advanced training options allow to select the metrics and the available trainers, the default options are good. Click on Start Training. The training time is taken to iterate through the different trainers (or regression analysis algorithms) while optimizing on the metrics. The process ends with the chosen algorithm and the generation of supporting code-behind files.

![](images/Figure_10.6.png)

Figure 10.6: Training completion in Model Builder

At this stage if the process ended with a model training error, open the log file, scroll towards the end, and notice the presence of message – WARN Model Builder fails to install the following NuGet dependencies. This is a known issue which usually comes when the project is part of a solution folder. Close the error dialog and manually include NuGet packages Microsoft.ML and Microsoft.ML.FastTree in the project. The next step allows to predict for the premium for a chosen set of parameters. You may verify that changing the parameters changes the premium value. The Consume step gives code snippet that can be included in your program to consume the model and use for prediction. Here there is also option to add a new Console or Web API project that consumes the model. Include the following code snippet to consume the model in Program.cs:

1. using InsPremiumPrediction;

2\.  

3\. // Create single instance of sample data from first line of dataset for model input

4. Insurance.ModelInput sampleData = new()

5\. {

6\.     Age = 18F,

7.  Sex = @"male",

8\.     Bmi = 33.8F,

9\.    Children = 1F,

10. Region = @"southeast",

11\. };

12\.  

13. Console.WriteLine("Using model to make single prediction -- " +

14.  "Comparing actual Expenses with predicted Expenses from sample data...\n\n");

15\.  

16. Console.WriteLine($"Age: {18F}");

17. Console.WriteLine($"Sex: {@"male"}");

18. Console.WriteLine($"Bmi: {33.8F}");

19. Console.WriteLine($"Children: {1F}");

20. Console.WriteLine($"Region: {@"southeast"}");

21. Console.WriteLine($"Expenses: {1725.55F}");

22\.  

23. var predictionResult = Insurance.Predict(sampleData);

24. Console.WriteLine($"\n\nPredicted Expenses: {predictionResult.Score}\n\n");

25\.  

26. Console.WriteLine("=============== End of process, hit any key to finish ===============");

27. Console.ReadKey();

After the training step, three files are auto generated by the Model Builder. The Insurance partial class spans across these files corresponding to training, evaluation, and consumption of the machine learning model. The model itself is contained in the file Insurance.mlnet. In the preceding code snippet, the Predict static method accepts the sample data of type ModelInput (line 23) and returns the output result of type ModelOutput. The Score property of the result printed on line 24 represents the predicted value of premium. The project structure is shown below in [Figure 10.7](#ch10.xhtml_fig10-7):

![](images/Figure_10.7.png)

Figure 10.7: Structure of project using Model Builder

Executing the program shows the following output:

![](images/Figure_10.8.png)

Figure 10.8: Single prediction via Model Builder generated model

The difference between the actual and the predicted value highlights the limitation of the model which makes assumptions about the relationship between the independent variables (features) and the dependent variable (label). If these assumptions are violated, such as if there are non-linear relationships or interactions that the model cannot capture, the predicted price may deviate from the actual value.

[Anomaly detection in financial dataset](#contents.xhtml_sc2_259a)

In this section we will work end-to-end on a real-world machine learning problem, that of anomaly detection with a reasonably large financial dataset. We will go through the machine learning tasks data preparation and model training followed by evaluation and prediction using the model. Before getting on to the programming tasks, let us understand the primary concepts around the problem.

[Anomaly detection](#contents.xhtml_sc3_260a)

Anomaly detection, also known as outlier detection, is a technique used to identify data points or patterns that deviate significantly from the expected behavior within a dataset. Anomalies can be defined as observations or events that differ from most of the data, indicating unusual or suspicious behavior. The goal of anomaly detection is to distinguish between normal and anomalous data points. By identifying anomalies, organizations can detect potential fraud, faults, errors, security breaches, or any other abnormal activities that may require attention or investigation.

[Synthetic financial dataset for fraud detection](#contents.xhtml_sc3_261a)

The dataset which we will use in our program is again from Kaggle, and its link can be found in the references. Because of the sensitive nature of financial transactions and lack of availability of good quality data, this dataset was synthesized using PaySim mobile money simulation tool. First few sample rows can be seen below in [Figure 10.9](#ch10.xhtml_fig10-9):

![](images/Figure_10.9.png)

Figure 10.9: Sample rows from the financial dataset

The fields are explained below in [Figure 10.10](#ch10.xhtml_fig10-10):

![](images/Figure_10.10.png)

Figure 10.10: Description of fields in the financial dataset

This dataset has around 6 million records out of which around 8 thousand i.e., approximately 0.1% transactions are fraud transactions with isFraud flag set to 1\. Some examples of scenarios that possibly lead to fraud transactions are as follows:

*   A sudden withdrawal or deposit of an unusually high amount.
*   A series of multiple transactions within a short period.
*   Transactions made during unusual hours, such as late at night or early in the morning.
*   Transactions made to first time recipients.
*   Large cash deposits.

Download the dataset file archive.zip to be used in the program later.

[Principal Component Analysis algorithm](#contents.xhtml_sc3_262a)

ML.NET uses Principal Component Analysis (PCA)  based algorithm named RandomizedPcaTrainer in its Anomaly detection task. PCA is a widely used algorithm which can be applied to anomaly detection tasks. Before applying PCA, it is important to preprocess the data by handling missing values, normalizing features, and addressing outliers. Preprocessing helps in obtaining accurate and meaningful features that are more informative for anomaly detection.

PCA is an unsupervised learning technique, meaning it does not require labeled data. It explores the inherent structure and patterns in the data without any prior knowledge of normal or anomalous instances. PCA assumes that the data follows a linear distribution and that outliers are rare. If the data violates these assumptions, PCA may not effectively capture the anomalies. It is crucial to thoroughly explore the data and understand its characteristics before applying PCA.

To evaluate PCA’s performance for anomaly detection, the following two metrices are used in ML.NET:

*   The area under the ROC curve measures the probability that the algorithm ranks a randomly chosen positive instance higher than a randomly chosen negative one. This value ranges between 0 and 1, with a value closer to 1 indicating a better model.
*   Detection rate at false positive count gives the ratio of correctly identified anomalies given the specified number of false positives. A value closer to 1 indicates a better model.

[Creating the program](#contents.xhtml_sc3_263a)

Create a new Console Application named AnomalyDetection within your solution at a location of choice and .NET 7.0 as the target framework version. Include the latest stable version of the NuGet package Microsoft.ML by Microsoft in your project. Copy the dataset file archive.zip, downloaded earlier, into the Datasets folder.

[Data preparation](#contents.xhtml_sc4_264a)

Create a new class file TransactionData.cs under the DataModels folder with the following code:

1. using Microsoft.ML.Data;

2\.  

3. namespace AnomalyDetection.DataModels;

4\.  

5. ///  <summary>

6. /// Model class for banking transaction data having following CSV header:

7. /// step,type,amount,nameOrig,oldbalanceOrg,newbalanceOrig,nameDest,

8. /// oldbalanceDest,newbalanceDest,isFraud,isFlaggedFraud

9. ///  </summary>

10. public  class  TransactionData

11\. {

12. [LoadColumn(0), ColumnName("step")]

13.  public  float Step;

14\.  

15. [LoadColumn(1), ColumnName("type")]

16.  public  string? TransactionType;

17\.  

18. [LoadColumn(2), ColumnName("amount")]

19. public  float Amount;

20\.  

21. [LoadColumn(3), ColumnName("nameOrig")]

22.  public  string? SourceCustomerName;

23\.  

24.  [LoadColumn(4), ColumnName("oldbalanceOrg")]

25. public  float InitialBalanceSource;

26\.  

27. [LoadColumn(5), ColumnName("newbalanceOrig")]

28.  public  float FinalBalanceSource;

29\.  

30.  [LoadColumn(6), ColumnName("nameDest")]

31.  public  string? TargetCustomerName;

32\.  

33. [LoadColumn(7), ColumnName("oldbalanceDest")]

34.    public  float InitialBalanceTarget;

35\.  

36.   [LoadColumn(8), ColumnName("newbalanceDest")]

37. public  float FinalBalanceTarget;

38\.  

39. [LoadColumn(9), ColumnName("isFraud")]

40.  public  float IsFraud;

41\.  

42.   [LoadColumn(10), ColumnName("isFlaggedFraud")]

43. public  float IsHighValueTransaction;

44\.  

45. public  override  string  ToString()

46\.     {

47.   return  $"Label (IsFraud): {IsFraud}\nFeatures: [type] {TransactionType}, "

48. + $"[amount] {Amount}, [oldbalanceOrg] {InitialBalanceSource},\n[newbalanceOrig] {FinalBalanceSource}, "

49. + $"[oldbalanceDest] {InitialBalanceTarget}, [newbalanceDest] {FinalBalanceTarget}";

50\.     }

51\. }

The TransactionData class in the preceding code is the model class representing each record from the financial dataset. The LoadColumn attribute on each property maps it with the source column and since we have used property names different from the column headers in the dataset, the corresponding column names are provided additionally. Both attributes are needed to correctly load and work with the dataset.

To help with file related common tasks create FileHelper.cs under Helpers folder with the following code:

1. using System.IO.Compression;

2\.  

3. namespace MyAnomalyDetection.Helpers;

4\.  

5. public  static  class  FileHelper

6\. {

7.  public  static  string  GetAbsolutePath(string relativePath)

8\.      {

9.  var assemblyFolderPath = new  FileInfo(typeof(Program).Assembly.Location)?.Directory?.FullName;

10.  return  Path.GetFullPath(Path.Combine(assemblyFolderPath, relativePath));

11\.     }

12\.  

13.  public  static  void  UnzipFile(string zipDataSet, string destinationFile)

14\.      {

15.  if (File.Exists(zipDataSet))

16.          {

17.  using  ZipArchive archive = ZipFile.OpenRead(zipDataSet);

18.   if (archive.Entries.Count > 0)

19\.           {

20.  var entry = archive.Entries[0];

21.  entry.ExtractToFile(destinationFile, true);

22\.      }

23\.         }

24\.     }

25\. }

The GetAbsolutePath method converts a relative path into an absolute one taking the assembly location as reference and UnzipFile method extracts the file from zip archive with a specified name.

For better clarity, we will abstract all the major steps involved within the machine learning process with dedicated classes for each step. Create a new folder MLSteps and in that create the following two classes:

The parent class BaseStep.cs:

1. using Microsoft.ML;

2\.  

3. namespace AnomalyDetection.MLSteps;

4. public  class  BaseStep

5\. {

6.  protected  readonly  MLContext mlContext;

7.  public  BaseStep()

8\.     {

9. mlContext = new  MLContext();

10\.     }

11.    public  BaseStep(MLContext ctx)

12\.     {

13\.         mlContext = ctx;

14\.     }

15\. }

The preceding BaseStep class will allow us to derive a child class and either accept an instance of MLContext object or create a new instance. The child Step1Builder.cs defined below derives from BaseStep class:

1. using AnomalyDetection.DataModels;

2. using Microsoft.ML;

3. using MyAnomalyDetection.Helpers;

4. using  static Microsoft.ML.DataOperationsCatalog;

5\.  

6. namespace AnomalyDetection.MLSteps;

7. public  class  Step1Builder : BaseStep

8\. {

9.  public  Step1Builder() : base() { }

10.  public  Step1Builder(MLContext ctx) : base(ctx) { }

11\.  

12.  public  required  string ZipDatasetFilePath { get; set; }

13.  public  required  string FullDataSetFilePath { get; set; }

14.  public  required  string TrainingDatasetFilePath { get; set; }

15.  public  required  string TestDatasetFilePath { get; set; }

16\.    

17.  public  void  PrepareDatasets()

18\.     {

19.  Console.WriteLine("===== Preparing training and test datasets =========");

20.  FileHelper.UnzipFile(ZipDatasetFilePath, FullDataSetFilePath);

21\.  

22.  // Only prep-datasets if train and test datasets don't exist yet

23.  if (!File.Exists(TrainingDatasetFilePath) &&

24. !File.Exists(TestDatasetFilePath))

25.        {

26.  // Load the original single dataset

27. IDataView originalFullData = mlContext.Data.LoadFromTextFile<TransactionData>(FullDataSetFilePath, ',', true);

28\.  

29.  //down sampling to ensure fraud cases are 25% of total cases

30.  var folds = mlContext.Data.CrossValidationSplit(originalFullData, 2, "isFraud");

31. var fraud1set = mlContext.Data.CreateEnumerable<TransactionData>(folds[1].TestSet, false);

32.   var fraud0set = mlContext.Data.CreateEnumerable<TransactionData>
(folds[1].TrainSet, false)

33.  .Take(fraud1set.Count() * 3);

34.  var downsampledFullData = mlContext.Data.ShuffleRows(mlContext.Data.LoadFromEnumerable(fraud0set.Concat(fraud1set)));

35\.  

36.  // Split the data 80:20 into train and test sets, train and evaluate.

37. TrainTestData trainTestData = mlContext.Data.TrainTestSplit(downsampledFullData, testFraction: 0.2);

38\.  

39. // Save train split

40.  using (var fileStream = File.Create(TrainingDatasetFilePath))

41\.           {

42. mlContext.Data.SaveAsText(mlContext.Data.ShuffleRows(trainTestData.TrainSet), fileStream, ',');

43.           }

44\.  

45. // Save test split

46.  using (var fileStream = File.Create(TestDatasetFilePath))

47.           {

48. mlContext.Data.SaveAsText(mlContext.Data.ShuffleRows(trainTestData.TestSet), fileStream, ',');

49.           }

50\.  

51.  Console.WriteLine("===== Preparing training and test datasets...DONE ==");

52\.         }

53.  else

54\.         {

55.    Console.WriteLine("===== Training and test datasets already exist =====");

56\.         }

57\.     }

58\. }

As the first step in the machine learning task, in the preceding code, we have unzipped the dataset archive on line 20\. After checking if the training and test dataset files do not exist, we proceed further (line 23 and 24). We are loading the full data set CSV file on line 27. The entire dataset will not be loaded immediately, rather this is a lazy operation. In fact, most data transformation and processing operations are not executed immediately when defined, but instead are deferred until the actual data is accessed or consumed. This is done to optimize memory usage and improve overall computational efficiency in machine learning workflows.

We have noted earlier that the chosen dataset contains only 0.1% fraudulent transaction. Using this data as it is may lead to inaccurate training of the model. So, we will down-sample the data by making the fraudulent cases be 25% of the total transaction. This is done between lines 30 and 34\. We finally split the data in 80:20 ratio for training and testing and save the respective files after shuffling the rows.

To run the first step, replace the default code within Program.cs with the following code:

1. using AnomalyDetection.MLSteps;

2. using Microsoft.ML;

3. using MyAnomalyDetection.Helpers;

4\.  

5. bool CleanupPreviousRun = true;

6\.  

7. var datasetsFolder = FileHelper.GetAbsolutePath("../../../Datasets");

8. string zipDatasetFilePath = Path.Combine(datasetsFolder, "archive.zip");

9. var fullDataSetFilePath = Path.Combine(datasetsFolder, "AllData.csv");

10. var trainingDatasetFilePath = Path.Combine(datasetsFolder, "TrainingData.csv");

11. var testDatasetFilePath = Path.Combine(datasetsFolder, "TestData.csv");

12\.  

13. if (CleanupPreviousRun)

14\. {

15.  foreach (var f in  new  List<string>

16\.         {

17.           fullDataSetFilePath,

18\.             trainingDatasetFilePath,

19.           testDatasetFilePath

20. }.Where(f => File.Exists(f)))

21\.     {

22.  File.Delete(f);

23\.     }

24\. }

25\.  

26. MLContext mlContext = new(seed: 1);

27. 

28\. //Step 1: Build ------------

29. new  Step1Builder(mlContext)

30\. {

31.  ZipDatasetFilePath = zipDatasetFilePath,

32\.     FullDataSetFilePath = fullDataSetFilePath,

33.    TrainingDatasetFilePath = trainingDatasetFilePath,

34\.     TestDatasetFilePath = testDatasetFilePath

35. }.PrepareDatasets();

36. 

37. Console.WriteLine("\n===== All tasks completed, press any key to exit ===");

38. Console.ReadKey();

In the calling program, we have first ensured that if there are any leftover files from the previous run, we are deleting them (line 13 to 24). This is followed by instantiating the Step1Builder class, passing in the instance of MLContext and setting the paths required in the step, before invoking the PrepareDatasets method. On running the program, the console shows the following output:

![](images/Figure_10.11.png)

Figure 10.11: Output after step 1 is executed

And new dataset files can be seen created under the Datasets folder along with the other classes. The project shows up in solution explorer, as depicted in [Figure 10.12](#ch10.xhtml_fig10-12):

![](images/Figure_10.12.png)

Figure 10.12: Project structure for anomaly detection after step 1

[Model training](#contents.xhtml_sc4_265a)

For the second step in the machine learning tasks, create a new class file Step2Trainer.cs under MLSteps. Add a method to train the model in this class.

1. private  static  ITransformer  TrainModel(MLContext mlContext, IDataView trainDataView)

2\. {

3.  Console.WriteLine("\n===== Training model ===============================");

4. 

5.  var featureColumnNames = trainDataView.Schema.AsQueryable()

6. .Select(column => column.Name)

7.  .Where(name => !NonFeatureColumns.Append(LabelColumn).Contains(name))

8. .ToArray();

9. 

10.  // Create the data process pipeline

11.  var dataProcessPipeline = mlContext.Transforms.Categorical.OneHotEncoding(new[] { new  InputOutputColumnPair("type", "type") })

12. .Append(mlContext.Transforms.Concatenate("Features", featureColumnNames))

13.   .Append(mlContext.Transforms.DropColumns(NonFeatureColumns.ToArray())

14. .Append(mlContext.Transforms.NormalizeLpNorm(outputColumnName: "NormalizedFeatures", inputColumnName: "Features")));

15. 

16.   var options = new  RandomizedPcaTrainer.Options

17.  {

18.  // The name of the feature column. The column data must be a known-sized vector of Single.

19. FeatureColumnName = "NormalizedFeatures",

20. 

21. // The name of the example weight column (optional). To use the weight column, the column data must be of type Single.

22. ExampleWeightColumnName = "newbalanceDest",

23. 

24.   // The number of components in the PCA.

25. Rank = 1

26. };

27. 

28.  // Create an anomaly detector. Its underlying algorithm is randomized PCA.

29.   IEstimator<ITransformer> trainer = mlContext.AnomalyDetection.Trainers.RandomizedPca(options: options);

30.  var trainingPipeline = dataProcessPipeline.Append(trainer);

31. 

32.  // Filter label 1 because in anomaly detection, the learner learns from normal examples and

33. // assumes all training examples have label 0

34.  var normalTrainDataView = mlContext.Data.FilterRowsByColumn(trainDataView, LabelColumn, 0, 1);

35. 

36.  var model = trainingPipeline.Fit(normalTrainDataView);

37. 

38.  Console.WriteLine("===== End of training process ======================");

39. 

40.  return model;

41. }

The model training method in the preceding code is the primary method which performs the training of the model using the mlContext and trainDataview passed as parameters. On lines 5 to 8, we have first created a list of featureColumnNames, excluding the label column (isFraud) and other columns which we are sure to have little or no impact on the result i.e., step, nameOrig, nameDest, isFlaggedFraud. The feature columns are concatenated and normalized while creating the data process pipeline starting from line 11\. We have also dropped the NonFeatureColumns. Also, the type column (with possible values - CASH_IN, CASH_OUT, DEBIT, PAYMENT, and TRANSFER) is categorical in nature, so we have transformed that into numeric vector using OneHotEncoding transformation. Next, we have specified the trainer options. Notice that we have given weight to the newbalanceDest column (line 22). On line 34, we are intending to train the model only with non-fraud cases. This is because of the way the chosen PCA algorithm works. Invoking the Fit method on line 36 finally performs the model training.

Next, add a method to evaluate the quality of the model and show the accuracy metrics.

1.  private  static  void  EvaluateModel(MLContext mlContext, ITransformer model, IDataView testDataView)

2\. {

3.  // Evaluate the model and show accuracy stats

4.  Console.WriteLine("\n===== Anomaly detection model accuracy =============");

5. 

6.  var predictions = model.Transform(testDataView);

7. 

8.  AnomalyDetectionMetrics metrics = mlContext.AnomalyDetection.Evaluate(predictions, LabelColumn);

9. 

10.  PrintAnomalyDetectionMetrics(metrics);

11\. }

12. 

13. private  static  void  PrintAnomalyDetectionMetrics(AnomalyDetectionMetrics metrics)

14\. {

15.  if (metrics != null)

16. {

17.  Console.WriteLine($"****************************************************");

18.  Console.WriteLine($"*     RandomizedPca Anomaly Detection Metrics");

19.   Console.WriteLine($"*--------------------------------------------------
-----");

20.    Console.WriteLine($"*     Area Under ROC Curve: {metrics.AreaUnderRocCurve:P2}");

21.    Console.WriteLine($"*     Detection rate at false positive count: {metrics.DetectionRateAtFalsePositiveCount:P2}");

22.  Console.WriteLine($"***************************************************
******");

23. }

24. }

The EvaluateModel method uses the test data set to evaluate the model on line 8, the values out of the resulting metrics are then printed.

Include a method to save the model in a zip file and return the path of the zip for subsequent prediction task.

1. private  static  string? SaveModel(MLContext mlContext, ITransformer model, string modelFilePath, DataViewSchema trainingDataSchema)

2. {

3.  mlContext.Model.Save(model, trainingDataSchema, modelFilePath);

4. 

5.  if (File.Exists(modelFilePath))

6. {

7.  Console.WriteLine($"\n===== Machine Learning model saved to ==============\n{modelFilePath}");

8.  return modelFilePath;

9.  }

10. 

11.  Console.WriteLine($"\n===== Error in saving machine learning model. ======");

12.  return  null;

13. }

The top portion of the class file Step2Trainer.cs shows up as follows and includes the GetModel method that invokes all other methods to return the path of the machine learning model zip file:

1. using AnomalyDetection.DataModels;

2. using Microsoft.ML;

3. using Microsoft.ML.Data;

4. using Microsoft.ML.Trainers;

5. 

6. namespace AnomalyDetection.MLSteps;

7. public  class  Step2Trainer : BaseStep

8\. {

9.  public  Step2Trainer() : base() { }

10.  public  Step2Trainer(MLContext ctx) : base(ctx) { }

11. 

12.  public  required  string TrainingDatasetFilePath { get; set; }

13.  public  required  string TestDatasetFilePath { get; set; }

14.  public  required  string ModelFilePath { get; set; }

15. 

16.  private  static  readonly  string LabelColumn = "isFraud";

17.  private  static  readonly  List<string> NonFeatureColumns = new()

18. {

19.  "step", "nameOrig", "nameDest", "isFlaggedFraud"

20. };

21.  public  string? GetModel()

22. {

23.   // Load Datasets

24.  var trainingDataView = mlContext.Data.LoadFromTextFile<TransactionData>(TrainingDatasetFilePath,

25. separatorChar: ',', hasHeader: true);

26. 

27.   var testDataView = mlContext.Data.LoadFromTextFile<TransactionData>(TestDatasetFilePath,

28. separatorChar: ',', hasHeader: true);

29. 

30.  // Train Model

31.    var model = TrainModel(mlContext, trainingDataView);

32. 

33.   // Evaluate quality of Model

34.  EvaluateModel(mlContext, model, testDataView);

35. 

36.  // Save model

37.  return  SaveModel(mlContext, model, ModelFilePath, trainingDataView.Schema);

38. }

39. ...

To invoke the new step, include the highlighted code in Program.cs:

1\. ...

2. var testDatasetFilePath = Path.Combine(datasetsFolder, "TestData.csv");

3.  var modelFilePath = Path.Combine(datasetsFolder, "PredictionModel.zip");

4. 

5. if (CleanupPreviousRun)

6\. {

7.  foreach (var f in  new  List<string>

8.  {

9. fullDataSetFilePath,

10. trainingDatasetFilePath,

11.  testDatasetFilePath,

12.  modelFilePath

13. }.Where(f => File.Exists(f)))

14. {

15.  File.Delete(f);

16. }

17. }

18. 

19. MLContext mlContext = new(seed: 1);

20. 

21\. //Step 1: Build ------------

22. new  Step1Builder(mlContext)

23\. {

24.  ZipDatasetFilePath = zipDatasetFilePath,

25. FullDataSetFilePath = fullDataSetFilePath,

26.  TrainingDatasetFilePath = trainingDatasetFilePath,

27. TestDatasetFilePath = testDatasetFilePath

28. }.PrepareDatasets();

29. 

30\. //Step2: Train --------------

31.  new  Step2Trainer(mlContext)

32\. {

33.  TrainingDatasetFilePath = trainingDatasetFilePath,

34.  TestDatasetFilePath = testDatasetFilePath,

35.   ModelFilePath = modelFilePath

36\. }.GetModel();

37. 

38. Console.WriteLine("\n===== All tasks completed, press any key to exit ===");

39. Console.ReadKey();

The model training step is invoked right after step 1 in the invocation program.

[Prediction](#contents.xhtml_sc4_266a)

To consume the machine learning model and make predictions, first add the FraudPrediction.cs class file under DataModels folder as follows:

1. using Microsoft.ML.Data;

2. 

3. namespace AnomalyDetection.DataModels;

4. 

5. public  class  FraudPrediction

6\. {

7.  ///  <summary>

8.  /// The predicted label, based on the score. A value of true indicates an anomaly.

9.  ///  </summary>

10. [ColumnName("PredictedLabel")]

11.  public  bool IsFraudPredicted { get; set; }

12. 

13.  ///  <summary>

14.    /// The non-negative, unbounded score calculated by the anomaly detection model.

15.  /// Fraudulent transactions (Anomalies) have higher scores than normal transactions

16.   ///  </summary>

17.  public  float Score { get; set; }

18. 

19.  public  override  string  ToString()

20. {

21.  return  $"Predicted Label: {IsFraudPredicted}, (Score: {Score})";

22. }

23\. }

The FraudPrediction class is the output class which will capture the prediction. Next, include the Step3Predictor.cs class file under MLSteps folder as shown:

1. using AnomalyDetection.DataModels;

2. using Microsoft.ML;

3\.  

4. namespace AnomalyDetection.MLSteps;

5. public  class  Step3Predictor : BaseStep

6\. {

7.  public  Step3Predictor() : base() { }

8.  public  Step3Predictor(MLContext ctx) : base(ctx) { }

9. 

10.  public  required  string ModelFilePath { get; set; }

11.  public  required  string TestDatasetFilePath { get; set; }

12. 

13.  public  void RunMultiplePredictions(int numberOfPredictions)

14. {

15. Console.WriteLine($"\n===== Predictions from saved model =================");

16. 

17.  var model = mlContext.Model.Load(ModelFilePath, out var inputSchema);

18. 

19.  var predictionEngine = mlContext.Model.CreatePredictionEngine<TransactionData, FraudPrediction>(model);

20. 

21.  // Load data as input for predictions

22.  var input = mlContext.Data.LoadFromTextFile<TransactionData>(TestDatasetFilePath, ',', true);

23. 

24. PrintTransaction(input, numberOfPredictions, predictionEngine, x => x.IsFraud > 0, true);

25. PrintTransaction(input, numberOfPredictions, predictionEngine, x => x.IsFraud < 1, false);

26. }

27\.  

28.  private  void PrintTransaction(IDataView dataView,

29. int n,

30.  PredictionEngine<TransactionData, FraudPrediction> predictionEngine,

31. Func<TransactionData, bool> predicate,

32.  bool expectedPrediction)

33\.     {

34.   Console.WriteLine($"\nExpected prediction for following {n} transactions: "

35. + $"{(expectedPrediction ? "FRAUD" : "NOT FRAUD")}:");

36\.        

37. mlContext.Data.CreateEnumerable<TransactionData>(dataView, reuseRowObject: false)

38.             .Where(predicate)

39.           .Take(n)

40\.             .ToList()

41.           .ForEach(testData =>

42\.             {

43. Console.WriteLine($"--- Transaction ---");

44.  Console.WriteLine(testData.ToString());

45. Console.WriteLine(predictionEngine.Predict(testData).ToString());

46.  Console.WriteLine($"-------------------");

47.           });

48\.     }

49\. }

In the prediction step, we are running a predefined number of predictions using the test data, including both fraud and non-fraud cases. To invoke the prediction class, include the following code in Program.cs:

1\. ... 

2\. //Step3: Predict ----------

3. new  Step3Predictor()

4\. {

5\.     ModelFilePath = modelFilePath,

6\.     TestDatasetFilePath = testDatasetFilePath

7. }.RunMultiplePredictions(numberOfPredictions: 2);

8\. ...

The completed project appears in the solution explorer as shown in [Figure 10.13](#ch10.xhtml_fig10-13):

![](images/Figure_10.13.png)

Figure 10.13: Completed project structure

Executing the program shows the following output given in [Figure 10.14](#ch10.xhtml_fig10-14):

![](images/Figure_10.14.png)

Figure 10.14: Completed program output

The output shows the metrics for accuracy of our model and the predictions for two cases each, which seem to match the expected result.

[Unit testing](#contents.xhtml_sc3_267a)

Unit tests can be written to validate any of the following stages in the machine learning process:

*   Test data preparation: Verify the correctness of your data preparation pipeline. Ensure that the data is loaded correctly, transformed appropriately, and encoded accurately for training or inference.
*   Model training tests: Verify that the model training process produces the expected output such that the trained model’s accuracy exceeds a certain threshold or the model converges within an acceptable number of iterations.
*   Model evaluation tests: Assess the model’s performance metrics such as accuracy, precision, recall, or F1 score. Ensure that the model meets the desired performance criteria.
*   Prediction tests: Verify that the predictions generated by the trained model align with the expected results.
*   Error handling and edge cases: Verify that the application correctly handles error conditions such as invalid input data, missing files, or other exceptional situations. Additionally, consider testing edge cases that could have a significant impact on model performance.
*   Continuous integration (CI) pipeline can be configured to automatically run the unit tests whenever changes are made to the ML.NET application’s codebase. This helps catch any regressions or issues early on and ensures the stability of your ML.NET application during development.

[Create unit test](#contents.xhtml_sc4_268a)

To demonstrate, we will write simple predication tests for the AnomalyDetection application. Create a new MS Test project named AnomalyDetection.Tests. Copy the model file PredictionModel.zip into the Datasets folder and mark its Copy to Output Directory property to Copy if newer. Add a project reference to the main AnomalyDetection project and add the NuGet package Microsoft.ML. Rename the default unit-test file UnitTest1.cs to PredictionTests.cs and add the following code:

1. using Microsoft.ML;

2. using AnomalyDetection.DataModels;

3\.  

4. namespace AnomalyDetection.Tests;

5\.  

6\. [TestClass]

7. public  class  PredictionTests

8\. {

9.  static  PredictionEngine<TransactionData, FraudPrediction>? predictionEngine = null;

10\.  

11. [ClassInitialize]

12.  public  static  void  Setup(TestContext context)

13\.    {

14. //Arrange - class setup

15. var mlContext = new  MLContext();

16. var modelPath = "./Datasets/PredictionModel.zip";

17. ITransformer model = mlContext.Model.Load(modelPath, out _);

18. predictionEngine = mlContext.Model.CreatePredictionEngine<TransactionData, FraudPrediction>(model);

19\.     }

20\.  

21. [TestMethod]

22.  public  void  SingleTransactionFraudTest()

23\.     {

24.  //Arrange

25.  var sampleFraudData = new  TransactionData

26\.         {

27\.           Step = 328,

28. TransactionType = "CASH_OUT",

29\.           Amount = 2299330.5F,

30. SourceCustomerName = "C1269100700",

31.           InitialBalanceSource = 2299330.5F,

32\.             FinalBalanceSource = 0,

33. TargetCustomerName = "C12644050",

34\.             InitialBalanceTarget = 1403092.2F,

35.           FinalBalanceTarget = 3736457.5F,

36.             IsFraud = 1F,

37.           IsHighValueTransaction = 0F,

38\.         };

39\.  

40.  //Act

41.  var output = predictionEngine?.Predict(sampleFraudData);

42\.  

43.  //Assert

44.   Assert.IsTrue(output?.IsFraudPredicted);

45\.     }

46\. }

In the preceding unit-test we have first created an instance of prediction engine using the model file during the test setup and then used it to predict a fraud case. Similarly, a test around non-fraud transaction is given below:

1. [TestMethod]

2. public  void  SingleTransactionNonFraudTest()

3\. {

4.  //Arrange

5.  var sampleNonFraudData = new  TransactionData

6\.    {

7\.         Step = 1,

8.  TransactionType = "PAYMENT",

9\.         Amount = 3558.79F,

10.  SourceCustomerName = "C369901249",

11\.         InitialBalanceSource = 20791F,

12\.       FinalBalanceSource = 17232.21F,

13. TargetCustomerName = "M405488475",

14\.       InitialBalanceTarget = 0F,

15. FinalBalanceTarget = 0F,

16\.       IsFraud = 0F,

17\.         IsHighValueTransaction = 0F,

18\.     };

19\.  

20.  //Act

21.  var output = predictionEngine?.Predict(sampleNonFraudData);

22\.  

23.  //Assert

24.   Assert.IsFalse(output?.IsFraudPredicted);

25\. }

[Deployment](#contents.xhtml_sc3_269a)

A machine learning model once trained needs to be made available to make predictions. Deploying a machine learning model refers to the process of making a trained model available for use in a production environment, where it can receive inputs and generate predictions. It involves taking the model from a development or research environment and integrating it into a system or application that can leverage its capabilities.

[Deployment considerations](#contents.xhtml_sc4_270a)

To increase the chances of successful deployment and long-term operation of the machine learning model, some areas that require careful consideration are as follows:

*   Scalability: Ensure that your model can handle the expected volume of data and requests. Consider factors such as the model’s computational requirements, memory usage, and response time. Issue related to concurrency involving multi-threading is addressed later in this section.
*   Infrastructure: Determine the infrastructure needed to deploy and run the model effectively. This includes considerations like choosing between cloud-based or on-premises deployment, configuring hardware resources (e.g., GPUs), and setting up a reliable and scalable infrastructure to serve the model.
*   Model versioning and management: Establish a robust system for versioning and managing your models. This allows you to track changes, roll back if necessary, and effectively manage multiple versions for A/B testing or gradual deployment.
*   Data privacy and security: Address privacy concerns when dealing with sensitive data. Ensure that appropriate security measures are in place to protect the data during training, deployment, and inference. Consider encryption, access controls, and compliance with relevant regulations (for example, GDPR).
*   Model performance: Continuously monitor and evaluate model’s performance in the deployment environment. Measure key metrics and set up alerts to identify degradation, drift, or other issues that may require intervention or model retraining. Logging relevant information about input data, predictions, and errors can also help with debugging, auditing, and continuous improvement.
*   Error handling and fallback strategies: Prepare for scenarios where the model encounters unexpected or ambiguous inputs. Implement appropriate error handling mechanisms and define fallback strategies to provide reasonable responses or handle failures gracefully.
*   Documentation and communication: Document your model’s deployment process, dependencies, and any specific considerations or requirements. Clear and concise documentation helps ensure that others can understand and work with your deployed model.

[Ways to deploy](#contents.xhtml_sc4_271a)

ML.NET offers several ways to deploy a machine learning model depending on the specific requirements and the target deployment environment. Here are some common methods for deploying the models:

*   In-app deployment: Directly integrate the ML.NET model into the existing .NET application. This approach is suitable for scenarios where you want to use the model within your application’s logic. You would need to include the trained model file along with your application’s deployment package.
*   Web API deployment: ML.NET models can be exposed as a web API, allowing clients to make HTTP requests to consume the model’s predictions. A separate web service can be built, or an API endpoint can be added to an existing web application. Please refer to the link in references for the steps to deploy a model as an ASP.NET Core Web API.
*   Azure Machine Learning: Azure Machine Learning provides a cloud-based platform for deploying and managing ML.NET models. Azure Machine Learning can be used to packaging and deploying ML.NET models as web services, which can be consumed by various applications and devices. Azure Machine Learning also offers features like scaling, monitoring, and versioning.
*   Azure Functions: ML.NET models can be deployed as Azure Functions, enabling predictions in a serverless environment. This approach is useful when you want to create event-driven workflows or perform lightweight predictions. Please refer to the link in references for the steps to deploy a model as an Azure Function.
*   Docker containers: Docker containers provide a consistent and portable way to deploy ML.NET models along with its dependencies and the runtime environment, across different platforms and infrastructure.
*   ONNX integration: ML.NET supports the Open Neural Network Exchange (ONNX) format, which is a standard for representing machine learning models. ML.NET model can be converted to ONNX format and then deployed using platforms that support ONNX, such as ONNX Runtime, TensorFlow, or PyTorch.
*   Mobile deployment: ML.NET models can be deployed on mobile devices using platforms like MAUI. Once integrated into the MAUI app, the ML.NET model can perform predictions directly on the device.

These are just some of the common methods for deploying ML.NET models. The choice of deployment approach depends on factors such as your application requirements, target platform, scalability needs, and infrastructure preferences. Often, a combination of deployment approaches may be used to meet different requirements within a larger system.

[Thread safety of Prediction Engine](#contents.xhtml_sc4_272a)

ML.NET’s PredictionEngine is not thread-safe, which means that using it concurrently from multiple threads can lead to unexpected behavior or exceptions, especially when the application grows. Depending on the specific deployment scenario and the requirements, there are a few options to handle the thread-safety issue:

*   Create a new instance for each thread: One simple approach is to create a new PredictionEngine instance for each thread that requires predictions. This way, each thread has its own isolated instance, avoiding any potential thread-safety issues. Another way to implement this is to use thread-local storage which provides mechanisms where each thread can have its own instance of a variable However, creating PredictionEngine instances can be resource-intensive, so make sure to manage the instances efficiently.
*   Synchronize the access: If there is a need to share a single PredictionEngine instance across multiple threads, you can synchronize the access to ensure only one thread uses it at a time. You can use locking mechanisms like locks, semaphores, or other synchronization primitives to control the access.
*   Using the PredictionEnginePool: PredictionEnginePool is a thread-safe container that manages a pool of PredictionEngine instances that are ready to make predictions. It manages the acquisition, release, and reuse of PredictionEngine objects, providing a safe and efficient way to make predictions concurrently.

Deploying a model to web API or Azure Functions provides a natural way to handle the thread-safety concerns of the PredictionEngine by leveraging the scoped instances and stateless nature of these deployment options. Each incoming request can have its own PredictionEngine instance, and there is no need to share the instance between requests, reducing the risk of concurrent access and ensuring isolation. However, even in such environments, shared resources or static variables require specific synchronization mechanisms to ensure thread safety.

[Conclusion](#contents.xhtml_sc2_273a)

ML.NET is a powerful framework that empowers .NET developers to leverage the capabilities of machine learning in their applications. With its user-friendly APIs, support for AutoML, and seamless integration with Visual Studio, ML.NET simplifies the process of implementing machine learning tasks. Whether you are building recommendation systems, fraud detection algorithms, or predictive analytics models, ML.NET provides the tools and flexibility to make it happen.

[Points to remember](#contents.xhtml_sc2_274a)

Following are some of the important points to remember when working with ML.NET:

*   Machine learning enables computers to learn from data and improve their performance without being explicitly programmed.
*   ML.NET is an open source framework developed by Microsoft for integrating machine learning into .NET applications.
*   ML.NET offers a wide range of algorithms and APIs to solve problems such as classification, regression, clustering, anomaly detection, recommendation system, and natural language processing problems.
*   ML.NET simplifies the overall machine learning flow, including data preprocessing, model training, evaluation, and prediction through its API, tools (such as Model Builder extension), and support for AutoML.
*   Deployment of machine learning model is an important consideration. Remember to thoroughly test your deployment to ensure that the chosen approach handles the thread-safety issue effectively and meets your performance requirements.

[Exercises](#contents.xhtml_sc2_275a)

*   The Sentiment Analysis program that we developed we used ML.NET API, create the same program with the same dataset using Model Builder. To consume the model, use the Add a Web API project in the Consume step of Model Builder wizard and verify the prediction by providing input by invoking the Swagger documentation for the exposed prediction endpoint.
*   Similarly, create the Insurance Premium Prediction program using the ML.NET API instead of Model Builder.
*   In the Anomaly Detection program, verify how the evaluation metrices and prediction results vary by making the following changes:
    *   We have used the down sampling with 25% fraud transaction, try a different ratio such as 1% or 50%. [Hint: Do this change in Step1Builder class]
    *   Try a different training and test data split ratio from the usual 80:20, such as 50:50 or 20:80\. [Hint: Do this change in Step1Builder class]
    *   Try by altering the feature columns such as include the step column or exclude the oldbalanceDest column. [Hint: Do this change in Step2Trainer class]
    *   While instantiating the RandomizedPca Anomaly Detection trainer, we have given weight to the newbalanceDest column when setting up the RandomizedPcaTrainer options. Try different column values for weight such as keeping it empty or setting a different field for example amount. [Hint: Do this change in Step2Trainer class]
    *   We have done prediction for two values each for fraud and non-fraud cases, try increasing this number to 20 and verify if you see any false positives or false negatives. [Hint: When invoking the Step3Predictor from Program.cs pass a higher number for the numberOfPredictions parameter]

[References](#contents.xhtml_sc2_276a)

*   What is ML.NET and how does it work?

[https://learn.microsoft.com/en-us/dotnet/machine-learning/how-does-mldotnet-work](https://learn.microsoft.com/en-us/dotnet/machine-learning/how-does-mldotnet-work)

*   Machine learning tasks in ML.NET

[https://learn.microsoft.com/en-us/dotnet/machine-learning/resources/tasks](https://learn.microsoft.com/en-us/dotnet/machine-learning/resources/tasks)

*   Which are the Steps to Build a Machine Learning Model?

[https://techspectraa.blogspot.com/2023/05/which-are-steps-to-build-machine.html](https://techspectraa.blogspot.com/2023/05/which-are-steps-to-build-machine.html)

*   Question about predictor output

https://github.com/dotnet/machinelearning/issues/376#issuecomment-399282699

*   Load data from files and other sources

[https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/load-data-ml-net](https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/load-data-ml-net)

*   Samples for ML.NET

[https://github.com/dotnet/machinelearning-samples](https://github.com/dotnet/machinelearning-samples)

*   Tutorial: Analyze sentiment of website comments in a web application using ML.NET Model Builder

[https://learn.microsoft.com/en-us/dotnet/machine-learning/tutorials/sentiment-analysis-model-builder](https://learn.microsoft.com/en-us/dotnet/machine-learning/tutorials/sentiment-analysis-model-builder)

*   Prepare data for building a model

https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/prepare-data-ml-net#work-with-categorical-data

*   ML.NET Model Builder 2022

[https://marketplace.visualstudio.com/items?itemName=MLNET.ModelBuilder2022](https://marketplace.visualstudio.com/items?itemName=MLNET.ModelBuilder2022)

*   What is Model Builder and how does it work?

https://learn.microsoft.com/en-us/dotnet/machine-learning/automate-training-with-model-builder

*   How to use the ML.NET Automated Machine Learning (AutoML) API

[https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/how-to-use-the-automl-api](https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/how-to-use-the-automl-api)

*   UCI Sentiment Labeled Sentences dataset

[https://archive.ics.uci.edu/dataset/331/sentiment+labelled+sentences](https://archive.ics.uci.edu/dataset/331/sentiment+labelled+sentences)

*   Insurance price prediction using Machine Learning (ML.NET)

[https://www.red-gate.com/simple-talk/development/data-science-development/insurance-price-prediction-using-machine-learning-ml-net/](https://www.red-gate.com/simple-talk/development/data-science-development/insurance-price-prediction-using-machine-learning-ml-net/)

*   Insurance Premium Prediction (dataset)

[https://www.kaggle.com/datasets/noordeen/insurance-premium-prediction](https://www.kaggle.com/datasets/noordeen/insurance-premium-prediction)

*   Synthetic Financial Datasets For Fraud Detection (dataset)

[https://www.kaggle.com/datasets/ealaxi/paysim1](https://www.kaggle.com/datasets/ealaxi/paysim1)

*   Deploy a model in an ASP.NET Core Web API

[https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/serve-model-web-api-ml-net](https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/serve-model-web-api-ml-net)

*   Deploy a model to Azure Functions

[https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/serve-model-serverless-azure-functions-ml-net](https://learn.microsoft.com/en-us/dotnet/machine-learning/how-to-guides/serve-model-serverless-azure-functions-ml-net)

# Index

A

action methods and return types, Web API

ActionResult<T> [90](#ch03.xhtml_page90)

IActionResult [89](#ch03.xhtml_page89)

IResult [90](#ch03.xhtml_page90)

Result<T> [90](#ch03.xhtml_page90)

specific type [89](#ch03.xhtml_page89)

Active Directory [95](#ch03.xhtml_page95)

Angular CRUD app

Angular components and services, creating [212](#ch06.xhtml_page212)-[214](#ch06.xhtml_page214)

book delete page [228](#ch06.xhtml_page228)-[230](#ch06.xhtml_page230)

book detail page [219](#ch06.xhtml_page219)-[222](#ch06.xhtml_page222)

book edit page [223](#ch06.xhtml_page223)-[227](#ch06.xhtml_page227)

book list page [214](#ch06.xhtml_page214)-[219](#ch06.xhtml_page219)

creating [203](#ch06.xhtml_page203)-[207](#ch06.xhtml_page207)

database, creating with EF core migration [209](#ch06.xhtml_page209)

deployment [231](#ch06.xhtml_page231)

developing [203](#ch06.xhtml_page203)

models, creating [207](#ch06.xhtml_page207)

scaffolding - API controller [208](#ch06.xhtml_page208), [209](#ch06.xhtml_page209)

seeding [210](#ch06.xhtml_page210), [211](#ch06.xhtml_page211)

Swagger documentation support, adding [209](#ch06.xhtml_page209), [210](#ch06.xhtml_page210)

unit testing [231](#ch06.xhtml_page231)

anomaly detection [365](#ch10.xhtml_page365)

anomaly detection, in financial dataset [365](#ch10.xhtml_page365)

data preparation [367](#ch10.xhtml_page367)-[374](#ch10.xhtml_page374)

deployment [387](#ch10.xhtml_page387)

deployment considerations [387](#ch10.xhtml_page387), [388](#ch10.xhtml_page388)

model deployment [388](#ch10.xhtml_page388), [389](#ch10.xhtml_page389)

model training [374](#ch10.xhtml_page374)-[380](#ch10.xhtml_page380)

prediction [380](#ch10.xhtml_page380)-[384](#ch10.xhtml_page384)

Principal Component Analysis (PCA) algorithm [366](#ch10.xhtml_page366), [367](#ch10.xhtml_page367)

program, creating [367](#ch10.xhtml_page367)

synthetic financial dataset, for fraud detection [365](#ch10.xhtml_page365), [366](#ch10.xhtml_page366)

unit testing [384](#ch10.xhtml_page384)

Application Programming Interfaces (API) [29](#ch02.xhtml_page29), [69](#ch03.xhtml_page69)

artificial intelligence (AI) [348](#ch10.xhtml_page348)

ASP.NET Core [27](#ch02.xhtml_page27)-[29](#ch02.xhtml_page29)

pre-requisites [28](#ch02.xhtml_page28)

ASP.NET Core Angular Project

creating [191](#ch06.xhtml_page191)

structure [192](#ch06.xhtml_page192)-[198](#ch06.xhtml_page198)

ASP.NET Core gRPC Service

browser access, enabling through JSON transcoding [127](#ch04.xhtml_page127), [128](#ch04.xhtml_page128)

creating [118](#ch04.xhtml_page118), [119](#ch04.xhtml_page119)

Greeter Service, testing with Postman [125](#ch04.xhtml_page125)-[127](#ch04.xhtml_page127)

gRPC Greeter Service, consuming [121](#ch04.xhtml_page121)-[125](#ch04.xhtml_page125)

structure [119](#ch04.xhtml_page119)-[121](#ch04.xhtml_page121)

Swagger documentation, enabling [129](#ch04.xhtml_page129), [130](#ch04.xhtml_page130)

ASP.NET Core Web API

controller approach, versus minimal API approach [80](#ch03.xhtml_page80), [81](#ch03.xhtml_page81)

creating [73](#ch03.xhtml_page73)-[75](#ch03.xhtml_page75)

minimal API, with simplified hosting model [79](#ch03.xhtml_page79), [80](#ch03.xhtml_page80)

structure [75](#ch03.xhtml_page75)-[79](#ch03.xhtml_page79)

auto-default struct [2](#ch01.xhtml_page2), [3](#ch01.xhtml_page3)

Automated Machine Learning (AutoML) [360](#ch10.xhtml_page360)

B

bi-directional streaming [114](#ch04.xhtml_page114)

Blazor [146](#ch05.xhtml_page146), [147](#ch05.xhtml_page147)

Blazor Apps [147](#ch05.xhtml_page147)

Blazor Hybrid [149](#ch05.xhtml_page149), [150](#ch05.xhtml_page150)

Blazor Server [147](#ch05.xhtml_page147), [148](#ch05.xhtml_page148)

Blazor WebAssembly [148](#ch05.xhtml_page148)

Blazor WebAssembly Hosted [149](#ch05.xhtml_page149)

Blazor WebAssembly Progressive Web App (PWA) [149](#ch05.xhtml_page149)

pre-requisites [150](#ch05.xhtml_page150)

Blazor WebAssembly App

client and server, creating [156](#ch05.xhtml_page156)-[158](#ch05.xhtml_page158)

creating [150](#ch05.xhtml_page150)-[160](#ch05.xhtml_page160)

deployment [186](#ch05.xhtml_page186)

end-to-end testing, with Playwright .NET [184](#ch05.xhtml_page184)-[186](#ch05.xhtml_page186)

game log, saving [171](#ch05.xhtml_page171)-[177](#ch05.xhtml_page177)

Index page, creating [160](#ch05.xhtml_page160)

reusable Razor Class library, creating [180](#ch05.xhtml_page180), [181](#ch05.xhtml_page181)

structure [151](#ch05.xhtml_page151)-[155](#ch05.xhtml_page155)

UI creation, for viewing game log [178](#ch05.xhtml_page178), [179](#ch05.xhtml_page179)

unit testing [181](#ch05.xhtml_page181)

unit testing, with bUnit [182](#ch05.xhtml_page182)-[184](#ch05.xhtml_page184)

variation one, creating [162](#ch05.xhtml_page162)-[166](#ch05.xhtml_page166)

variation two, creating [167](#ch05.xhtml_page167)-[170](#ch05.xhtml_page170)

Blazor WebAssembly (Hosted) App

developing [155](#ch05.xhtml_page155), [156](#ch05.xhtml_page156)

bUnit [182](#ch05.xhtml_page182)

for unit testing [182](#ch05.xhtml_page182)-[184](#ch05.xhtml_page184)

C

Cloud Native Computing Foundation (CNCF) [112](#ch04.xhtml_page112)

cookies [94](#ch03.xhtml_page94)

cross-language compatibility [115](#ch04.xhtml_page115)

CRUD operations [35](#ch02.xhtml_page35), [81](#ch03.xhtml_page81)

Curl URL Request Library (cURL) [112](#ch04.xhtml_page112)

custom pizza order form

adding, to WPF application [240](#ch07.xhtml_page240)-[250](#ch07.xhtml_page250)

D

database

creating, with EF Core migration [91](#ch03.xhtml_page91), [92](#ch03.xhtml_page92)

dependency injection (DI) [79](#ch03.xhtml_page79)

E

endpoints [87](#ch03.xhtml_page87)

extended nameof scope [3](#ch01.xhtml_page3), [4](#ch01.xhtml_page4)

Extensible Application Markup Language (XAML) [236](#ch07.xhtml_page236)

F

file-scoped types [5](#ch01.xhtml_page5)

functional testing

deployment [66](#ch02.xhtml_page66)

Razor Pages web app [64](#ch02.xhtml_page64), [66](#ch02.xhtml_page66)

G

generic attributes [5](#ch01.xhtml_page5), [6](#ch01.xhtml_page6)

generic math [6](#ch01.xhtml_page6)-[9](#ch01.xhtml_page9)

GNU (GNU's Not Unix) [112](#ch04.xhtml_page112)

gRPC

advantages [116](#ch04.xhtml_page116)

disadvantages [117](#ch04.xhtml_page117)

features [114](#ch04.xhtml_page114), [115](#ch04.xhtml_page115)

overview [112](#ch04.xhtml_page112), [113](#ch04.xhtml_page113)

pre-requisites [118](#ch04.xhtml_page118)

use cases [117](#ch04.xhtml_page117), [118](#ch04.xhtml_page118)

versus other service models [115](#ch04.xhtml_page115)

working [113](#ch04.xhtml_page113), [114](#ch04.xhtml_page114)

gRPC protocol [114](#ch04.xhtml_page114)

gRPC Service

client, creating [131](#ch04.xhtml_page131)

creating [131](#ch04.xhtml_page131)

CsvHelper NuGet package, configuring [134](#ch04.xhtml_page134), [135](#ch04.xhtml_page135)

CsvHelper NuGet package, installing [134](#ch04.xhtml_page134)

deployment [141](#ch04.xhtml_page141)

developing [131](#ch04.xhtml_page131)

EmployeesDataService, creating [135](#ch04.xhtml_page135)-[137](#ch04.xhtml_page137)

GrpcDownloadClient, creating [137](#ch04.xhtml_page137)-[139](#ch04.xhtml_page139)

proto file, creating [132](#ch04.xhtml_page132), [133](#ch04.xhtml_page133)

sample data set, including [133](#ch04.xhtml_page133)

unit testing [139](#ch04.xhtml_page139), [140](#ch04.xhtml_page140)

H

Hypertext Transfer Protocol (HTTP) [29](#ch02.xhtml_page29), [69](#ch03.xhtml_page69), [71](#ch03.xhtml_page71)

I

Image Navigator WinUI app

creating [292](#ch08.xhtml_page292), [293](#ch08.xhtml_page293)

deployment [308](#ch08.xhtml_page308), [309](#ch08.xhtml_page309)

folder browsing capability, adding to Main Window [294](#ch08.xhtml_page294)-[296](#ch08.xhtml_page296)

Image Detail page, creating [304](#ch08.xhtml_page304)-[308](#ch08.xhtml_page308)

Image List page, creating [298](#ch08.xhtml_page298)-[303](#ch08.xhtml_page303)

Image View Model class, creating [296](#ch08.xhtml_page296), [297](#ch08.xhtml_page297)

unit testing [308](#ch08.xhtml_page308)

Interface Definition Language (IDL) [113](#ch04.xhtml_page113), [114](#ch04.xhtml_page114)

J

JSON Web Tokens (JWT) [94](#ch03.xhtml_page94)

K

Kestrel [74](#ch03.xhtml_page74)

L

Line of Business (LOB) apps [309](#ch08.xhtml_page309)

list patterns [9](#ch01.xhtml_page9), [10](#ch01.xhtml_page10)

M

machine learning (ML) [348](#ch10.xhtml_page348), [349](#ch10.xhtml_page349)

ML.NET [347](#ch10.xhtml_page347)-[352](#ch10.xhtml_page352)

binary classification [354](#ch10.xhtml_page354)

machine learning process [352](#ch10.xhtml_page352)-[354](#ch10.xhtml_page354)

pre-requisites [352](#ch10.xhtml_page352)

program, creating [355](#ch10.xhtml_page355)-[359](#ch10.xhtml_page359)

regression analysis, with Model Builder [359](#ch10.xhtml_page359)

sentiment dataset [354](#ch10.xhtml_page354)

ML.NET Model Builder component [352](#ch10.xhtml_page352)

mobile application development

evolution [314](#ch09.xhtml_page314)

Model Builder [359](#ch10.xhtml_page359)

model deployment, ML.NET

Azure Functions [389](#ch10.xhtml_page389)

Azure Machine Learning [389](#ch10.xhtml_page389)

Docker containers [389](#ch10.xhtml_page389)

in-app deployment [388](#ch10.xhtml_page388)

mobile deployment [389](#ch10.xhtml_page389)

ONNX integration [389](#ch10.xhtml_page389)

Web API deployment [388](#ch10.xhtml_page388)

Model-View-ViewModel (MVVM) [33](#ch02.xhtml_page33), [256](#ch07.xhtml_page256), [257](#ch07.xhtml_page257)

implementing, in Sudoku application [257](#ch07.xhtml_page257)-[266](#ch07.xhtml_page266)

MVC Web App

creating [33](#ch02.xhtml_page33)

structure [33](#ch02.xhtml_page33), [34](#ch02.xhtml_page34)

versus Razor Pages web app [33](#ch02.xhtml_page33)

N

.NET 7

microsecond and nanosecond [10](#ch01.xhtml_page10)-[12](#ch01.xhtml_page12)

Regex source generation [15](#ch01.xhtml_page15), [16](#ch01.xhtml_page16)

Tar APIs [19](#ch01.xhtml_page19)-[21](#ch01.xhtml_page21)

.NET Base Class Library (BCL) [315](#ch09.xhtml_page315)

.NET Community MVVM Toolkit [257](#ch07.xhtml_page257)

.NET desktop development [352](#ch10.xhtml_page352)

.NET MAUI [313](#ch09.xhtml_page313)-[315](#ch09.xhtml_page315)

.NET MAUI app

creating [316](#ch09.xhtml_page316), [317](#ch09.xhtml_page317)

pre-requisites [316](#ch09.xhtml_page316)

structure [317](#ch09.xhtml_page317)-[324](#ch09.xhtml_page324)

.NET MAUI Blazor Hybrid Application

creating [324](#ch09.xhtml_page324)-[326](#ch09.xhtml_page326)

.NET MAUI ContentView (XAML) [332](#ch09.xhtml_page332)

O

OAuth2 [95](#ch03.xhtml_page95)

OpenID Connect [95](#ch03.xhtml_page95)

outlier detection [365](#ch10.xhtml_page365)

P

Playwright .NET [184](#ch05.xhtml_page184)

end-to-end testing, with [184](#ch05.xhtml_page184)-[186](#ch05.xhtml_page186)

Postman [125](#ch04.xhtml_page125)

POST-Redirect-GET [33](#ch02.xhtml_page33)

Prediction Engine

thread safety [389](#ch10.xhtml_page389), [390](#ch10.xhtml_page390)

Principal Component Analysis (PCA) algorithm [366](#ch10.xhtml_page366), [367](#ch10.xhtml_page367)

Progressive Web App (PWAs) [149](#ch05.xhtml_page149)

Project Reunion [284](#ch08.xhtml_page284)

proto3 [114](#ch04.xhtml_page114)

Protocol Buffers (protobuf) [113](#ch04.xhtml_page113), [114](#ch04.xhtml_page114)

R

raw string literals [14](#ch01.xhtml_page14), [15](#ch01.xhtml_page15)

Razor Pages web app

cleaning up [42](#ch02.xhtml_page42)-[45](#ch02.xhtml_page45)

creating [29](#ch02.xhtml_page29)-[36](#ch02.xhtml_page36)

database, creating with EF core migration [41](#ch02.xhtml_page41), [42](#ch02.xhtml_page42)

end-to-end application, developing [34](#ch02.xhtml_page34)

functional testing [64](#ch02.xhtml_page64)-[66](#ch02.xhtml_page66)

models, creating [36](#ch02.xhtml_page36), [37](#ch02.xhtml_page37)

Publisher model, updating [52](#ch02.xhtml_page52)-[55](#ch02.xhtml_page55)

records, filtering [56](#ch02.xhtml_page56), [57](#ch02.xhtml_page57)

related data, working with [55](#ch02.xhtml_page55)

Repository Pattern, using [58](#ch02.xhtml_page58)-[61](#ch02.xhtml_page61)

running [42](#ch02.xhtml_page42)

scaffolding - book pages [37](#ch02.xhtml_page37)-[40](#ch02.xhtml_page40)

scaffolding - publisher pages [41](#ch02.xhtml_page41)

seeding [45](#ch02.xhtml_page45)-[50](#ch02.xhtml_page50)

structure [31](#ch02.xhtml_page31), [32](#ch02.xhtml_page32)

UI refinements [50](#ch02.xhtml_page50)-[52](#ch02.xhtml_page52)

unit testing [61](#ch02.xhtml_page61)-[64](#ch02.xhtml_page64)

verifying [42](#ch02.xhtml_page42)

ReadAtLeast method [18](#ch01.xhtml_page18), [19](#ch01.xhtml_page19)

ReadExactly method [18](#ch01.xhtml_page18), [19](#ch01.xhtml_page19)

real-world .NET MAUI app

developing [327](#ch09.xhtml_page327)

real-world WinUI app

developing [291](#ch08.xhtml_page291)

Image Detail page, creating [304](#ch08.xhtml_page304)

Image Navigator WinUI app, creating [292](#ch08.xhtml_page292), [293](#ch08.xhtml_page293)

regression analysis [360](#ch10.xhtml_page360)

regression analysis, with Model Builder [359](#ch10.xhtml_page359)

insurance dataset [360](#ch10.xhtml_page360)

program, creating [360](#ch10.xhtml_page360)-[365](#ch10.xhtml_page365)

Remote Procedure Call (RPC) [29](#ch02.xhtml_page29)

Remote Procedure Call (RPC) APIs [113](#ch04.xhtml_page113)

Repository Pattern [58](#ch02.xhtml_page58)

Representational State Transfer (REST) [71](#ch03.xhtml_page71)

required members [16](#ch01.xhtml_page16), [17](#ch01.xhtml_page17)

Roslyn Source Generator [15](#ch01.xhtml_page15)

S

simplified ordering [18](#ch01.xhtml_page18)

Single-Page Application (SPA) [146](#ch05.xhtml_page146), [190](#ch06.xhtml_page190)

pre-requisites [191](#ch06.xhtml_page191)

Single-project MSIX Packaging Tools [285](#ch08.xhtml_page285)

Span<char> pattern matching

on constant string [13](#ch01.xhtml_page13)

SPA template application

working [198](#ch06.xhtml_page198)-[203](#ch06.xhtml_page203)

SPA with Angular

creating [191](#ch06.xhtml_page191)

SQL LocalDB database [34](#ch02.xhtml_page34)

stream reading [18](#ch01.xhtml_page18)

string interpolation expressions

newlines [12](#ch01.xhtml_page12), [13](#ch01.xhtml_page13)

Sudoku Buddy .NET MAUI app

deployment [342](#ch09.xhtml_page342)

files, copying from WPF application [330](#ch09.xhtml_page330)-[332](#ch09.xhtml_page332)

running, with Android simulator [339](#ch09.xhtml_page339)-[341](#ch09.xhtml_page341)

unit testing [341](#ch09.xhtml_page341)

views, creating [332](#ch09.xhtml_page332)-[338](#ch09.xhtml_page338)

Sudoku Buddy WPF application [327](#ch09.xhtml_page327), [328](#ch09.xhtml_page328)

candidates or pencil marks, showing [266](#ch07.xhtml_page266)-[269](#ch07.xhtml_page269)

creating [251](#ch07.xhtml_page251)

deployment [281](#ch07.xhtml_page281)

file, copying from [330](#ch09.xhtml_page330)-[332](#ch09.xhtml_page332)

incorrect input, highlighting [274](#ch07.xhtml_page274)-[278](#ch07.xhtml_page278)

migrating, to Sudoku Buddy .NET MAUI app [329](#ch09.xhtml_page329), [330](#ch09.xhtml_page330)

MVVM, implementing [257](#ch07.xhtml_page257)-[266](#ch07.xhtml_page266)

MVVM, implementing for showing numbers [256](#ch07.xhtml_page256)

UI, creating [251](#ch07.xhtml_page251)-[256](#ch07.xhtml_page256)

unit testing [279](#ch07.xhtml_page279), [280](#ch07.xhtml_page280)

user, allowing to type digit [270](#ch07.xhtml_page270)-[274](#ch07.xhtml_page274)

Swagger UI [75](#ch03.xhtml_page75)

System.LINQ

simplified ordering, with System.LINQ (.NET 7) [18](#ch01.xhtml_page18)

System Under Test (SUT) [61](#ch02.xhtml_page61)

T

Tar APIs [19](#ch01.xhtml_page19)

Target Framework Monikers (TFM) [321](#ch09.xhtml_page321)

third-party authentication providers [95](#ch03.xhtml_page95)

Transport Layer Security (TLS) [114](#ch04.xhtml_page114)

type converters [21](#ch01.xhtml_page21), [22](#ch01.xhtml_page22)

U

unit testing

anomaly detection, in financial dataset [384](#ch10.xhtml_page384)

Blazor WebAssembly App [181](#ch05.xhtml_page181)

gRPC services [139](#ch04.xhtml_page139)-[141](#ch04.xhtml_page141)

Image Navigator WinUI app [308](#ch08.xhtml_page308)

Razor Pages web app [61](#ch02.xhtml_page61)-[64](#ch02.xhtml_page64)

Sudoku Buddy .NET MAUI app [341](#ch09.xhtml_page341)

Sudoku Buddy WPF application [279](#ch07.xhtml_page279), [280](#ch07.xhtml_page280)

Web API [109](#ch03.xhtml_page109)

unit testing, machine learning process [384](#ch10.xhtml_page384), [385](#ch10.xhtml_page385)

unit test, creating [385](#ch10.xhtml_page385), [386](#ch10.xhtml_page386)

Universal Windows Platform (UWP) [284](#ch08.xhtml_page284)

user experience (UX) framework [284](#ch08.xhtml_page284)

UTF-8 string literals [22](#ch01.xhtml_page22), [23](#ch01.xhtml_page23)

W

warning wave 7 [23](#ch01.xhtml_page23), [24](#ch01.xhtml_page24)

Web API [71](#ch03.xhtml_page71), [72](#ch03.xhtml_page72)

action methods and return types [88](#ch03.xhtml_page88), [89](#ch03.xhtml_page89)

consuming [104](#ch03.xhtml_page104)-[108](#ch03.xhtml_page108)

creating [81](#ch03.xhtml_page81), [82](#ch03.xhtml_page82)

database, creating with EF Core migration [91](#ch03.xhtml_page91), [92](#ch03.xhtml_page92)

deployment [109](#ch03.xhtml_page109)

developing [81](#ch03.xhtml_page81)

JWT authentication and authorization [94](#ch03.xhtml_page94)-[104](#ch03.xhtml_page104)

model binding [91](#ch03.xhtml_page91)

models, creating [82](#ch03.xhtml_page82)

overview [70](#ch03.xhtml_page70)

pre-requisites [72](#ch03.xhtml_page72)

routing [87](#ch03.xhtml_page87)

running [92](#ch03.xhtml_page92)

scaffolding - books API controller [83](#ch03.xhtml_page83)-[87](#ch03.xhtml_page87)

seeding [93](#ch03.xhtml_page93), [94](#ch03.xhtml_page94)

unit testing [109](#ch03.xhtml_page109)

verifying [92](#ch03.xhtml_page92)

Web apps

versus Web API [72](#ch03.xhtml_page72)

WebAssembly (WASM) [146](#ch05.xhtml_page146)

Windows Communication Foundation (WCF) [115](#ch04.xhtml_page115)

Windows Presentation Foundation (WPF) [233](#ch07.xhtml_page233)-[236](#ch07.xhtml_page236)

desktop applications [234](#ch07.xhtml_page234), [235](#ch07.xhtml_page235)

versus, .NET MAUI [328](#ch09.xhtml_page328)

Windows Runtime (WinRT) [314](#ch09.xhtml_page314)

Windows UI Library (WinUI) 3 [283](#ch08.xhtml_page283), [284](#ch08.xhtml_page284)

Windows UI Library (WinUI) [284](#ch08.xhtml_page284)

WinUI 3 app

creating [285](#ch08.xhtml_page285), [286](#ch08.xhtml_page286)

pre-requisites [285](#ch08.xhtml_page285)

structure [286](#ch08.xhtml_page286)-[291](#ch08.xhtml_page291)

WPF Application

creating [236](#ch07.xhtml_page236), [237](#ch07.xhtml_page237)

custom pizza order form, adding [240](#ch07.xhtml_page240)-[250](#ch07.xhtml_page250)

pre-requisites [236](#ch07.xhtml_page236)

structure [237](#ch07.xhtml_page237)-[240](#ch07.xhtml_page240)