![](image_rsrc1MK.jpg)

Functional C#: Embracing Functional Programming in a C# World

Carlos Bueno

Copyright © 2024 by Carlos Bueno.

All rights reserved. No part of this book may be used or reproduced in any form whatsoever without written permission except in the case of brief quotations in critical articles or reviews.

For more information, or to book an event, contact :

carlosbueno@sapo.pt

[http://www.github.com/ kinderbueno360](http://www.github.com/%20kinderbueno360)

My Functional Library Functional.DotNet

https://github.com/kinderbueno360/Functional.DotNet

Book design by Carlos Bueno

Cover design by Carlos Bueno

First Edition: 2023

DEDICATION

To my beloved wife Ewa Walęga-Bueno,

Your constant support and source of inspiration have been the cornerstone of this journey. Your unwavering love, encouragement, and patience have been my guiding stars, helping me navigate and overcome every challenge to make this book a reality.

Thank you for always believing in me, for your steadfast faith in my abilities, and for being the light in my darkest moments.

To my cherished children, Luiz Carlos Bueno, Gustavo Bueno, and Mikołaj Walęga-Bueno,

You are my pride and joy, the embodiments of hope and dreams for the future. Your laughter and curiosity fuel my desire to create, inspire, and dream bigger.

To my dear brother Cleber Bueno,

Your companionship and solidarity through the years have been invaluable. Your presence in my life has been a source of strength and joy, reminding me of the unbreakable bond we share.

To my beloved mother Celia Bueno and father Carlos Roberto Bueno,

Your guidance, sacrifices, and unconditional love have shaped the person I am today. You have instilled in me values and virtues that no words can fully express my gratitude for.

And to my late grandmother Anna Fantucci,

Your memory is a treasure I hold close to my heart. More than 25 years since you passed, yet your influence remains a powerful force in my life. You were the most important person in my world, a beacon of wisdom, love, and kindness. Your legacy continues to inspire and guide me every day.

This book is dedicated to all of you as a token of my profound love, gratitude, and respect. Each of you has played a significant role in this journey, and it is with immense honor that I share this achievement with you.

Carlos Bueno

CONTENTS

Contents

[Chapter 1: Introduction to Functional Programming](#part0002.xhtml_a1FB)

[1.1\. What is Functional Programming?](#part0002.xhtml_a1FC)

[1.2\. Comparing Functional and Object-Oriented Programming](#part0002.xhtml_a1FD)

[Fun Examples and Analogies to Contrast OOP and FP](#part0002.xhtml_a1FE)

[Key Takeaways](#part0002.xhtml_a1FF)

[•​1.3\. The Benefits of Functional Programming](#part0002.xhtml_a1FG)

[Chapter 2: C# and Functional Programming: A Growing Friendship](#part0002.xhtml_a1FH)

[2.1\. The Evolution of C# and Its Functional Features](#part0002.xhtml_a1FJ)

[2.2\. The C# Functional Ecosystem](#part0002.xhtml_a1FK)

[2.3\. Hybrid Programming: Combining OO and FP in C](#part0002.xhtml_a1FM)

[When combining OO and FP in C#, consider the following guidelines:](#part0002.xhtml_a1FN)

[Chapter 3: Functional Building Blocks in C](#part0002.xhtml_a1FP)

[3.1\. Pure Functions and Immutability - The Dynamic Duo](#part0002.xhtml_a1FR)

[Pure Functions:](#part0002.xhtml_a1FS)

[Advantages of pure functions:](#part0002.xhtml_a1FT)

[Immutability:](#part0002.xhtml_a1FU)

[Advantages of immutability:](#part0002.xhtml_a1FV)

[3.2\. Higher-Order Functions](#part0002.xhtml_a1FW)

[The Art of Delegation](#part0002.xhtml_a1FX)

[Currying: A Spicy Technique](#part0002.xhtml_a1FY)

[Party Tricks with Higher-Order Functions](#part0002.xhtml_a1FZ)

[Map](#part0002.xhtml_a1G0)

[Filter](#part0002.xhtml_a1G1)

[Reduce](#part0002.xhtml_a1G2)

[Higher-Order Functions: The Encore](#part0002.xhtml_a1G3)

[3.3 Lambda Expressions](#part0002.xhtml_a1G4)

[Lambda Expressions: A Brief History](#part0002.xhtml_a1G5)

[The Art of Lambda Expressions](#part0002.xhtml_a1G6)

[Lambda Expressions in Action](#part0002.xhtml_a1G7)

[Event Handlers](#part0002.xhtml_a1G8)

[LINQ Queries](#part0002.xhtml_a1G9)

[Predicate Functions](#part0002.xhtml_a1GA)

[The Limits of Lambda Expressions](#part0002.xhtml_a1GB)

[Lambda Expressions](#part0002.xhtml_a1GC)

[3.4 Closures](#part0002.xhtml_a1GD)

[Closures: A Quick Introduction](#part0002.xhtml_a1GE)

[Under the Hood: How Closures Work in C](#part0002.xhtml_a1GF)

[Closures in Everyday Code](#part0002.xhtml_a1GG)

[The Grand Send-Off: Onward to Functional Data Structures and Patterns](#part0002.xhtml_a1GH)

[Chapter 4: Functional Data Structures and Patterns](#part0002.xhtml_a1GJ)

[4.1\. Tuples and Records: Data’s Dynamic Duo](#part0002.xhtml_a1GK)

[Tuples: Small but Mighty](#part0002.xhtml_a1GM)

[Records: Immutability’s Dream Team](#part0002.xhtml_a1GN)

[Tuples and Records: Unstoppable Together](#part0002.xhtml_a1GP)

[4.2 Pattern Matching: A Whodunit of Code](#part0002.xhtml_a1GR)

[4.3 Discriminated Unions: The Swiss Army Knife of Data Types](#part0002.xhtml_a1GS)

[What’s in a Name: Introducing Discriminated Unions](#part0002.xhtml_a1GT)

[A Menagerie of Types: Modeling Animals](#part0002.xhtml_a1GU)

[Samples Galore: More Discriminated Union Goodness](#part0002.xhtml_a1GV)

[4.4 Deconstruction](#part0002.xhtml_a1GW)

[4.4.1 Deconstructing Tuples](#part0002.xhtml_a1GX)

[4.4.2 Deconstructing Records](#part0002.xhtml_a1GY)

[4.4.4 Deconstructing with Extension Methods](#part0002.xhtml_a1GZ)

[4.4.5 Deconstruction Gotchas and Tips](#part0002.xhtml_a1H0)

[Chapter 5:  Currying and Partial Application: The Art of Splitting Functions](#part0002.xhtml_a1H1)

[5.3\. Lazy Evaluation: The Art of Procrastination](#part0002.xhtml_a1H2)

[5.3.1\. Using the Lazy Class](#part0002.xhtml_a1H3)

[5.3.2\. Lazy Sequences with LINQ](#part0002.xhtml_a1H4)

[5.4\. Memoization: The Art of Remembering](#part0002.xhtml_a1H5)

[5.4.1\. Memoizing Recursive Functions](#part0002.xhtml_a1H6)

[5.4.2\. Creating a Memoization Decorator](#part0002.xhtml_a1H7)

[Chapter 6: LINQ: The Power of Functional Programming in C](#part0002.xhtml_a1H8)

[6.1\. Introduction to LINQ](#part0002.xhtml_a1H9)

[6.1.1\. Basic LINQ Syntax](#part0002.xhtml_a1HA)

[6.2\. Query Syntax vs. Method Syntax](#part0002.xhtml_a1HB)

[6.2.1\. Query Syntax](#part0002.xhtml_a1HC)

[6.2.3 Extending LINQ with Custom Query Operators](#part0002.xhtml_a1HD)

[6.2.3.1 Custom Map Operator](#part0002.xhtml_a1HE)

[6.3\. Common LINQ Operators](#part0002.xhtml_a1HF)

[Chapter 7: Error Handling and Functional Programming](#part0002.xhtml_a1HG)

[7.1\. Traditional Error Handling in C#: Exceptions](#part0002.xhtml_a1HH)

[7.2\. The Result and Either Types](#part0002.xhtml_a1HJ)

[7.3. Railway-Oriented Programming](#part0002.xhtml_a1HK)

[Chapter 8: Asynchronous Programming in a Functional Style](#part0002.xhtml_a1HM)

[8.1\. Async/Await and Task-Based Asynchronous Pattern](#part0002.xhtml_a1HN)

[8.2\. Asynchronous Functional Pipelines](#part0002.xhtml_a1HP)

[8.3 Handling Errors Asynchronously](#part0002.xhtml_a1HR)

[8.3.1 Asynchronous Error Handling with Result](#part0002.xhtml_a1HS)

[8.3.2 Composing Asynchronous Functions](#part0002.xhtml_a1HT)

[8.3.3 Error Handling with Parallelism](#part0002.xhtml_a1HU)

[8.3.4 Retrying Asynchronous Operations](#part0002.xhtml_a1HV)

[Chapter 9: Functional Design Patterns](#part0002.xhtml_a1HW)

[9.1 Functor, Applicative, and Monad](#part0002.xhtml_a1HX)

[Chapter 10: Usage and Examples](#part0002.xhtml_a1HY)

[10.1 Maybe Example](#part0002.xhtml_a1HZ)

[10.2 IEnumerable Example](#part0002.xhtml_a1J0)

[10.3 Extension Methods for Task Monad](#part0002.xhtml_a1J1)

[Use Case 1: Stock Data API](#part0002.xhtml_a1J2)

[10.4 Semigroups](#part0002.xhtml_a1J3)

[10.5 Monoids](#part0002.xhtml_a1J4)

[10.6  Practical Applications](#part0002.xhtml_a1J5)

[10.7  String Concatenation Monoid](#part0002.xhtml_a1J6)

[10.8 List Merging Monoid](#part0002.xhtml_a1J7)

[10.9 Free Monads](#part0002.xhtml_a1J8)

[10.9.1 Implementing a Free Monad in C](#part0002.xhtml_a1J9)

[10.9.1.1 Console Operations](#part0002.xhtml_a1JA)

[10.9.1.2 Free Monad Data Structure](#part0002.xhtml_a1JB)

[10.9.2 Building Programs with Free Monads](#part0002.xhtml_a1JC)

[10.9.2.1 Creating the Program](#part0002.xhtml_a1JD)

[Chapter 11:  Using Monads with Language-Ext](#part0002.xhtml_a1JE)

[Option Monad](#part0002.xhtml_a1JF)

[Either Monad](#part0002.xhtml_a1JG)

[Try Monad](#part0002.xhtml_a1JH)

[Task Monad](#part0002.xhtml_a1JJ)

[State Monad](#part0002.xhtml_a1JK)

[11.3\. Other Functional Libraries for C](#part0002.xhtml_a1JM)

[11.3.1 FSharpx.Extras](#part0002.xhtml_a1JN)

[11.3.2 CSharpFunctionalExtensions](#part0002.xhtml_a1JP)

[10.3.3 FsCheck](#part0002.xhtml_a1JR)

[11.3.4 MoreLINQ](#part0002.xhtml_a1JS)

[11.4\. MoreLINQ: Practical Examples](#part0002.xhtml_a1JT)

[11.4.1 DistinctBy](#part0002.xhtml_a1JU)

[11.4.2 Partition](#part0002.xhtml_a1JV)

[11.4.3 TakeEvery](#part0002.xhtml_a1JW)

[11.4.4 Scan](#part0002.xhtml_a1JX)

[Chapter 12: Real-World Applications and Case Studies](#part0002.xhtml_a1JY)

[12.1 Functional Programming in Web Development: A Sci-Fi-Inspired Adventure](#part0002.xhtml_a1JZ)

[Language-Ext: The Warp Drive of Functional Programming](#part0002.xhtml_a1K0)

[Event Sourcing: The Temporal Prime Directive](#part0002.xhtml_a1K1)

[MongoDB: The Intergalactic Database](#part0002.xhtml_a1K2)

[The Wallet Agent: A Trusty Tricorder with Event Sourcing](#part0002.xhtml_a1K3)

[The Functional Wallet API: Engaging Warp Speed with Event Sourcing and MongoDB](#part0002.xhtml_a1K4)

[Boldly Going Forward](#part0002.xhtml_a1K5)

# Functional Fun with C#: Embracing Functional Programming in a C# World

I

# Welcome to “Functional Fun with C#: Embracing Functional Programming in a C# World”!

In this book, we’ll dive deep into the world of functional programming (FP) and learn how we can harness its power in C# to write efficient, robust, and maintainable code. You might think of C# as an object-oriented (OO) language, and you’re right! However, C# has evolved over the years, steadily embracing functional programming concepts, making it a powerful hybrid language. This book will guide you through the exciting journey of discovering the functional side of C# and how to incorporate FP principles into your everyday coding.

Functional programming is a programming paradigm that treats computation as the evaluation of mathematical functions, avoiding mutable state and side effects. It has been around for decades, but it has gained traction in recent years due to its inherent advantages in dealing with concurrent and distributed systems. In the age of multicore processors and big data, functional programming is more relevant than ever.

In the early chapters, we’ll explore the fundamental concepts of functional programming and compare them with object-oriented programming. Imagine functional programming as the quiet, introverted cousin of the ever-popular object-oriented programming. While object-oriented programming loves to create objects and mingle them in intricate hierarchies, functional programming prefers to keep things simple, relying on mathematical functions and immutable data structures to get the job done. This difference in approach has profound implications on how we design, write, and reason about code.

As we delve deeper into the book, we’ll discuss the functional features available in C#, such as higher-order functions, lambda expressions, immutability, pattern matching, and more. We’ll see how these features enable us to write code that is more concise, expressive, and less prone to errors. We’ll also learn how to work with popular functional libraries like Language-Ext, which provide additional functional constructs to supercharge our C# code.

To make things more interesting, we’ll use practical examples, exercises, and real-world scenarios to demonstrate the power of functional programming in action. Throughout the book, we’ll be comparing functional and object-oriented approaches to tackle the same problems, highlighting their strengths and weaknesses. The goal is not to prove one paradigm superior to the other, but to help you make informed decisions when choosing the right tool for the job.

We’ll also touch upon advanced topics, such as monads, functional error handling, and asynchronous programming in a functional style. By the end of this book, you’ll have a deep understanding of functional programming concepts, and you’ll be able to wield them effectively in your C# projects.

So, buckle up and prepare for an adventure into the fascinating world of functional programming in C#. Whether you’re an experienced C# developer looking to expand your horizons or a developer from another language curious about functional programming in C#, this book has something for everyone. Let’s embark on this journey together and uncover the functional treasures hidden within C#.

# Chapter 1: Introduction to Functional Programming

## 1.1\. What is Functional Programming?

Functional programming (FP) is a programming paradigm that treats computation as the evaluation of mathematical functions, avoiding mutable state and side effects. The core idea behind functional programming is to build software by composing pure functions, which are functions that always produce the same output for the same input and have no side effects.

In functional programming, functions are first-class citizens, meaning they can be assigned to variables, passed as arguments, and returned from other functions. This enables powerful and expressive programming techniques, such as higher-order functions, which are functions that take other functions as arguments or return them as results.

Functional programming has its roots in lambda calculus, a formal system developed in the 1930s to investigate the foundations of computation and function definition. Lambda calculus has influenced many programming languages and has been the basis for some of the most famous functional languages, such as Lisp, Haskell, and ML.

## 1.2\. Comparing Functional and Object-Oriented Programming

Functional programming and object-oriented programming (OOP) are two of the most popular programming paradigms, and they have fundamentally different approaches to building software.

In object-oriented programming, the focus is on creating objects that represent real-world entities and their interactions. Objects contain both state (data) and behavior (methods), and they communicate by sending messages to each other. Inheritance and polymorphism are two primary mechanisms for creating reusable and extensible code in OOP.

In contrast, functional programming centers around the concept of composing software using pure functions and immutable data structures. Functions do not have state, and they are not tied to any specific object. Instead, they take input and produce output based on that input. This means that functional programming relies heavily on the concept of function composition, which is chaining together multiple functions to create more complex behavior.

Here are some key differences between OOP and FP:

OOP uses mutable state and objects, while FP prefers immutability and pure functions. In OOP, functions (methods) are often tied to objects, whereas in FP, functions are standalone entities that can be easily composed. OOP emphasizes inheritance and polymorphism for code reuse, while FP relies on function composition and higher-order functions. OOP encourages encapsulation, hiding the internal state of objects, while FP promotes transparency and simplicity in function behavior.

### Fun Examples and Analogies to Contrast OOP and FP

To further illustrate the differences between object-oriented programming (OOP) and functional programming (FP), let’s consider a lighthearted and somewhat exaggerated analogy.

The Kitchen Analogy Imagine that you are a chef preparing a meal in two different kitchens: the OOP kitchen and the FP kitchen.

In the OOP kitchen, you have a team of sous-chefs, each specialized in a particular task. Each sous-chef is an object with its own internal state, and they communicate by passing ingredients (data) back and forth. For example, the onion-chopping sous-chef takes an onion and returns it all chopped up. However, this sous-chef is also a bit forgetful, so they might occasionally chop the onion too finely or not enough, due to their mutable internal state.

On the other hand, the FP kitchen is like a well-orchestrated assembly line. Each worker (function) performs a specific task, and the ingredients flow through the pipeline. There is no room for confusion, as each worker receives precise instructions on what to do, and the output is consistent every time. In this kitchen, the onion-chopping function guarantees perfectly chopped onions every time.

Comparing OOP and FP through a Party Scenario Let’s consider another analogy to compare OOP and FP: organizing a party.

In the OOP party, each guest represents an object, and they mingle and interact with one another, sharing stories and changing their moods. The party’s atmosphere is dynamic and ever-changing, as guests (objects) continuously influence each other. Sometimes, guests might even form groups (inheritance) based on shared interests or characteristics.

In contrast, the FP party is more like a potluck dinner, where each guest brings a dish (function) that contributes to the overall feast. The dishes are prepared beforehand and remain unchanged during the party. The success of the party depends on the thoughtful composition of dishes that work well together. There is no mingling or influencing each other’s mood; guests simply enjoy the delicious food in a serene and predictable environment.

### Key Takeaways

These analogies, while not perfect, provide a more accessible and light-hearted understanding of the core differences between OOP and FP:

*   OOP focuses on interactions between objects, leading to dynamic and sometimes unpredictable behavior. In contrast, FP emphasizes the composition of functions to create predictable and consistent results.

*   Mutable state is a core aspect of OOP, while FP prefers immutability and statelessness, leading to fewer surprises and side effects.

*   Code reuse in OOP relies on inheritance and polymorphism, while FP achieves it through function composition and higher-order functions.

*   Keep in mind that these are just fun examples to help you understand the concepts better. In reality, OOP and FP can coexist, and many modern programming languages support both paradigms. As a programmer, you can mix and match these approaches to find the best solution for your specific problem. The key is to understand their strengths and weaknesses and apply them judiciously.

## 1.3\. The Benefits of Functional Programming

Functional programming offers several benefits over other paradigms, such as object-oriented programming. Here are some of the key advantages of using functional programming:

*   Easier to reason about: Pure functions and immutability make it simpler to understand the behavior of code. Since functions have no side effects and always produce the same output for a given input, you can analyze and predict the behavior of your code more easily.

*   Easier to test and debug: With pure functions, testing becomes more straightforward. You only need to test the function with different inputs, without worrying about hidden state or side effects. This makes debugging easier, as you can focus on individual functions rather than complex interactions between objects.

*   Concurrency and parallelism: Functional programming’s emphasis on immutability and lack of shared state makes it inherently suitable for concurrent and parallel programming. Since data is not mutated, there is no need for locks or other synchronization mechanisms, allowing for more efficient and scalable concurrent code.

*   Code reusability and modularity: Functions in functional programming are designed to be small, reusable, and composable. This encourages modularity and allows you to build complex behavior by chaining together simple functions.

*   Expressiveness: Functional programming often leads to more concise and expressive code. Higher-order functions, pattern matching, and other functional programming features allow you to write code that is easier to understand and maintain.

*   Refactoring and maintainability: As functional programming promotes the use of small, pure functions and avoids mutable state, it becomes easier to refactor and maintain the code. This can lead to a more stable and maintainable codebase in the long run.

*   Decreased bug potential: Since functional programming eliminates side effects and mutable state, it reduces the likelihood of introducing bugs caused by unexpected changes in state. This can lead to more reliable and robust software.

*   Adaptable to changing requirements: Functional programming’s modularity and composability make it easier to adapt your code to changing requirements. Small, independent functions can be quickly modified or replaced without affecting the overall system.

While functional programming has many benefits, it’s essential to remember that no programming paradigm is perfect for every situation. Sometimes, a mix of functional and object-oriented programming can lead to the most effective solution. The key is to understand the strengths and weaknesses of each approach and use them appropriately in your projects.

In the next chapters, we’ll dive deeper into the world of functional programming with C#. You’ll learn how to leverage the functional features of C# to write more expressive, maintainable, and robust code, even if you still use object-oriented programming principles for some parts of your application.

# Chapter 2: C# and Functional Programming: A Growing Friendship

## 2.1\. The Evolution of C# and Its Functional Features

C# has come a long way since its inception. Over the years, the language has evolved to incorporate functional programming features, making it easier to write functional code in C#. Let’s take a brief journey through C#’s history to see how its relationship with functional programming has grown.

C# 1.0 - 2.0: The early days of C# were heavily influenced by Java and focused primarily on object-oriented programming. While functional programming was not at the forefront, C# did introduce delegates, laying the groundwork for future functional features.

C# 3.0: The introduction of LINQ (Language Integrated Query) in C# 3.0 marked a significant milestone in the language’s functional evolution. LINQ introduced features like lambda expressions, extension methods, and anonymous types, making it easier to write functional code in C#. Additionally, C# 3.0 incorporated features like implicitly typed local variables (var), object and collection initializers, and automatic properties, further enhancing the language’s expressiveness.

// Example of LINQ
var numbers =  new List<int>  {  1,  2,  3,  4,  5  };
var evenNumbers = numbers.Where(n => n %  2  ==  0);

C# 4.0: C# 4.0 added support for dynamic typing and named and optional parameters, providing greater flexibility when working with functions.

C# 5.0: With the introduction of async and await keywords, C# 5.0 made it easier to write asynchronous code using a functional approach. This led to more expressive and concise asynchronous code, which is often found in functional programming.

// Example of async and await
public async Task<int>  FetchDataAsync()
{
 var result = await SomeApi.GetDataAsync();
 return result.Count;
}

C# 6.0 - 7.x: These versions of C# added many functional features, such as expression-bodied members, pattern matching, and local functions. The introduction of tuples and deconstruction made it easier to work with multiple return values, a common pattern in functional programming.

// Example of pattern matching
public  string  DescribeShape(object shape)
{
    return shape switch
    {
Circle c => $"A circle with a radius of {c.Radius}",
Rectangle r => $"A rectangle with a width of {r.Width} and a height of {r.Height}",
_ =>  "An unknown shape"
    };
}

C# 8.0 - 9.0: With nullable reference types, C# moved closer to functional programming by encouraging the use of explicit nullability, which promotes safer code. Other functional enhancements include switch expressions, records, and init-only properties.

// Example of records
public record Point(int X,  int Y);

## 2.2\. The C# Functional Ecosystem

C#’s growing support for functional programming has led to the development of a rich ecosystem of libraries and tools that further enhance its functional capabilities. Some popular libraries and frameworks include:

F# Core Library: F# is a functional-first programming language that runs on the .NET platform. Its core library offers many functional programming constructs that can be used in C# as well. LanguageExt: LanguageExt is a library that provides a comprehensive set of functional extensions for C#, including options, immutable collections, and monads like Either and Try.

Immutable Collections: The System.Collections.Immutable namespace offers a set of immutable collection types, which are ideal for functional programming scenarios where mutable state should be avoided.

// Example of using an immutable list
using System.Collections.Immutable;

var list = ImmutableList<int>.Empty;
list = list.Add(1);
list = list.Add(2);
list = list.Add(3);

Reactive Extensions (Rx.NET): Reactive Extensions is a library for composing asynchronous and event-based programs using observable sequences and LINQ-style query operators. It allows for a more functional and declarative approach to handling asynchronous and event-driven programming.

// Example of using Reactive Extensions
using System.Reactive.Linq;

IObservable<int> source = Observable.Range(1,  5);
IObservable<int> evenNumbers = source.Where(x => x %  2  ==  0);

evenNumbers.Subscribe(x => Console.WriteLine($"Even number: {x}"));

## 2.3\. Hybrid Programming: Combining OO and FP in C

C#’s versatility as a hybrid programming language allows developers to combine object-oriented and functional programming paradigms, depending on the problem at hand. This can lead to more expressive, maintainable, and robust code.

## When combining OO and FP in C#, consider the following guidelines:

*   Embrace immutability: Make your classes and their properties immutable whenever possible. This helps reduce side effects and makes your code more predictable.

public  class Customer
{
    public  Customer(int id,  string name)
    {
Id = id;
Name = name;
    }

public  int Id {  get;  }
    public  string Name {  get;  }
}

Use pure functions: Favor methods that do not have side effects and depend solely on their input parameters. This makes your code easier to reason about and test.

public  int  Add(int x,  int y)  => x + y;

Take advantage of higher-order functions: Use higher-order functions like Select, Where, and Aggregate from LINQ to manipulate data in a more functional and expressive way.

var totalLength = words.Where(word =>  !string.IsNullOrEmpty(word))
                       .Select(word => word.Length)
                       .Aggregate((sum, length)  => sum + length);

Consider functional constructs: Use functional constructs like Option, Either, and Try from libraries like LanguageExt to model your code in a more functional way and better handle failures and edge cases.

Leverage pattern matching: Use pattern matching to handle complex conditional logic in a more concise and readable manner.

By blending object-oriented and functional programming approaches in C#, you can harness the strengths of both paradigms to write more expressive, maintainable, and robust code. As you dive deeper into the world of functional programming with C#, you may find yourself making jokes like, “Why did the functional programmer get thrown out of school? Because they refused to take classes!” All jokes aside, we hope this chapter has provided you with a solid foundation for exploring the exciting possibilities that C# offers for functional programming.

# Chapter 3: Functional Building Blocks in C

Welcome back, fellow coder! Are you ready to dig deeper into functional programming in C#? You’re in luck, because in this chapter, we’re going to explore the essential building blocks that make functional programming so groovy. We’ll cover pure functions, immutability, higher-order functions, lambda expressions, and closures, all while keeping it relaxed and fun. So, grab a snack, put on your favorite tunes, and let’s dive right in!

## 3.1\. Pure Functions and Immutability - The Dynamic Duo

Let’s dive deeper into the fascinating world of pure functions and immutability, the dynamic duo that keeps functional programming clean and predictable.

### Pure Functions:

Recall that a pure function is a function that always produces the same output for the same input and has no side effects. Side effects can include modifying variables outside the function, interacting with external systems (like file I/O or network communication), or even just printing something to the console. Pure functions are like well-behaved students in a classroom, never causing trouble or making a mess.

### Advantages of pure functions:

*   Easy to reason about: Since they depend only on their input and always produce the same output, you can easily predict what a pure function will do.

*   Easy to test: With no hidden dependencies or side effects, testing pure functions is a breeze. Just provide the input and check the output – simple as that!

*   Cacheable: Since they always return the same output for the same input, you can cache the results of a pure function, making your code faster and more efficient.

Examples of pure functions:

// Length of a string
int  Length(string str)
{
 return str.Length;
}

// Checking if a number is even
bool  IsEven(int number)
{
 return number %  2  ==  0;
}

// Concatenating two strings
string  Concat(string a,  string b)
{
 return a + b;
}

### Immutability:

Immutability is all about keeping data constant and unchangeable. In functional programming, we prefer to work with immutable data structures, which makes our code more predictable and less error-prone. Immutability is like a well-maintained garden, where everything stays in its place, and you don’t have to worry about things getting tangled up.

### Advantages of immutability:

Simplifies code: Immutable data structures reduce the need for error-prone defensive copying and make it easier to reason about the state of your data. Enhances thread safety: Since immutable data structures cannot be changed once they’re created, you don’t have to worry about synchronization issues in multithreaded code. Encourages functional programming: Immutability goes hand in hand with pure functions and other functional programming concepts, promoting a cleaner and more maintainable coding style.

Examples of immutability:

Using readonly fields:

public  class ImmutablePerson
{
    public  readonly  string Name;
    public  readonly  int Age;

public  ImmutablePerson(string name,  int age)
    {
Name = name;
Age = age;
    }
}

Using immutable collections:

using System.Collections.Immutable;

var immutableList = ImmutableList.Create(1, 2, 3);
var newList = immutableList.Add(4); // Creates a new list with 4 added, doesn't modify the original list

Combining pure functions and immutability:

public class ImmutableCircle
{
    public double Radius { get; }

public ImmutableCircle(double radius)
    {
        Radius = radius;
    }

public double GetArea()
    {
        return Math.PI * Math.Pow(Radius, 2);
    }

public ImmutableCircle WithRadius(double newRadius)
    {
        return new ImmutableCircle(newRadius);
    }
}

var circle = new ImmutableCircle(5);
var area = circle.GetArea(); // Calculates the area using the pure function GetArea
var biggerCircle = circle.WithRadius(10); // Creates a new circle with a different radius, without modifying the original circle

Let’s explore an example that demonstrates the thread-safety benefits of using immutable data structures in a multithreaded environment.

Imagine we have a List shared between multiple threads. If one thread is adding elements to the list while another is reading from it, you may encounter synchronization issues, resulting in unexpected behavior or even exceptions.

Using an object-oriented approach (not thread-safe):

using System;
using System.Collections.Generic;
using System.Threading.Tasks;

class UnsafeCounter
{
 private List<int> _numbers =  new List<int>();

public  void  AddNumber(int number)
    {
        _numbers.Add(number);
    }

public  int  GetSum()
    {
        return _numbers.Sum();
    }
}

class Program
{
    static async Task Main()
    {
        var unsafeCounter =  new  UnsafeCounter();

var addTask = Task.Run(()  =>
        {
            for  (int i =  0; i <  1000; i++)
            {
                unsafeCounter.AddNumber(i);
            }
        });

var sumTask = Task.Run(()  =>
        {
            int sum = unsafeCounter.GetSum();
            Console.WriteLine($"Sum: {sum}");
        });

await Task.WhenAll(addTask, sumTask);
    }
}

This example has a race condition because AddNumber and GetSum can be executed concurrently, leading to unpredictable results. To fix this issue, we can use an immutable data structure, such as ImmutableList, which is provided by the System.Collections.Immutable namespace.

Using a functional approach (thread-safe):

using System;
using System.Collections.Immutable;
using System.Linq;
using System.Threading.Tasks;

class SafeCounter
{
    private ImmutableList<int> _numbers = ImmutableList<int>.Empty;

public  void  AddNumber(int number)
    {
_numbers = _numbers.Add(number);
    }

public  int  GetSum()
    {
        return _numbers.Sum();
    }
}

class Program
{
    static async Task Main()
    {
        var safeCounter =  new  SafeCounter();

var addTask = Task.Run(()  =>
        {
            for  (int i =  0; i <  1000; i++)
            {
                safeCounter.AddNumber(i);
            }
        });

var sumTask = Task.Run(()  =>
        {
            int sum = safeCounter.GetSum();
            Console.WriteLine($"Sum: {sum}");
        });

await Task.WhenAll(addTask, sumTask);
    }
}

In this version, we’ve replaced the mutable List with an ImmutableList. When we call AddNumber, a new list is created with the added number, and the _numbers reference is updated atomically. This ensures that GetSum will always work on a consistent state of the _numbers list, making the code thread-safe without needing explicit synchronization mechanisms.

This example demonstrates how using immutable data structures in functional programming can help to avoid synchronization issues in multithreaded code, making it safer and easier to reason about.

As we reach the end of Section 3.1, you’ve now been introduced to some essential functional building blocks in C#. We’ve explored the powerful duo of pure functions and immutability, the magical world of higher-order functions, and the secret handshake of lambda expressions. By understanding these concepts, you’re well on your way to mastering functional programming in C#.

But wait, there’s more! In the next section, we’ll dive into some awesome functional data structures and patterns that will take your functional programming skills to the next level. Get ready to learn about:

Tuples and Records: Compact, efficient data containers that are perfect for functional programming Pattern Matching: A powerful way to destructure and analyze data with ease Discriminated Unions: A fantastic tool for modeling complex data types with limited and well-defined possibilities Deconstruction: A technique to extract values from data structures in a clean, functional way So, grab a snack, take a break, and get ready to continue this amazing journey into the functional programming universe with C#. See you in Section 3.2!

## 3.2\. Higher-Order Functions

Higher-order functions are like the life of the party in functional programming. They can take other functions as arguments or return them as results, creating a dynamic, fun, and composable environment. In this chapter, we’ll explore the fascinating world of higher-order functions in C#, uncovering their secrets and discovering how they can make our code more expressive and flexible.

### The Art of Delegation

In the world of higher-order functions, delegation is key. They allow us to pass around behavior like hors d’oeuvres at a fancy soiree. Let’s start with a simple example:

public  int  ApplyOperation(int x,  int y, Func<int,  int,  int> operation)
{
 return  operation(x, y);
}

var sum =  ApplyOperation(3,  4,  (x, y)  => x + y);  // 7
var product =  ApplyOperation(3,  4,  (x, y)  => x * y);  // 12

In this example, ApplyOperation takes two integers and a function that operates on them. Just like a waiter serving up delicious canapés, it delivers the desired behavior right to your plate.

### Currying: A Spicy Technique

Currying is a technique that adds a dash of functional flair to your code. It involves transforming a function that takes multiple arguments into a series of functions that each take a single argument. Here’s a simple example to whet your appetite:

public Func<int,  int>  Add(int x)
{
 return y => x + y;
}

var addFive =  Add(5);
var result =  addFive(3);  // 8

Now, Add returns a function that takes an integer and adds it to the initial x. It’s like we’ve prepared a delightful curry, and now we can add various ingredients to suit our taste buds.

### Party Tricks with Higher-Order Functions

Let’s learn some new dance moves to impress our functional programming friends! Here are a few handy higher-order functions that you can use in your everyday coding:

### Map

The Map function applies a given function to each element in a collection, creating a new collection with the transformed elements.

public IEnumerable<TResult> Map<TSource, TResult>(IEnumerable<TSource> source, Func<TSource, TResult> selector)
{
    foreach  (var item in source)
   {
        yield  return  selector(item);
    }
}

var numbers =  new List<int>  {  1,  2,  3  };
var squares =  Map(numbers, x => x * x);  // [1, 4, 9]

### Filter

The Filter function filters a collection based on a predicate function, returning only the elements that satisfy the condition.

public IEnumerable<T> Filter<T>(IEnumerable<T> source, Func<T,  bool> predicate)
{
    foreach  (var item in source)
    {
        if  (predicate(item))
        {
            yield  return item;
        }
    }
}

var numbers =  new List<int>  {  1,  2,  3,  4,  5  };
var evenNumbers =  Filter(numbers, x => x %  2  ==  0);  // [2, 4]

### Reduce

The Reduce function accumulates a collection’s elements into a single value using a specified accumulator function.

public T Reduce<T>(IEnumerable<T> source, Func<T, T, T> accumulator)
{
    using  var enumerator = source.GetEnumerator();
    if  (!enumerator.MoveNext())
    {
        throw  new  InvalidOperationException("The collection must have at least one element.");
    }
T result = enumerator.Current;
    while  (enumerator.MoveNext())
    {
result =  accumulator(result, enumerator.Current);
    }

return result;
}

var numbers =  new List<int>  {  1,  2,  3,  4,  5  };
var sum =  Reduce(numbers,  (x, y)  => x + y);  // 15

With these party tricks up your sleeve, you’ll be the star of any functional programming event!

### Higher-Order Functions: The Encore

As our journey through the land of higher-order functions in C# comes to a close, it’s time for a grand finale. Let’s put everything we’ve learned to good use by composing a higher-order function masterpiece:

public Func<T1, TResult> Compose<T1, T2, TResult>(Func<T1, T2> f, Func<T2, TResult> g)
{
 return x =>  g(f(x));
}

var numbers =  new List<int>  {  1,  2,  3,  4,  5  };

var sumOfSquares =  Compose(
 (IEnumerable<int> xs)  =>  Map(xs, x => x * x),
 (IEnumerable<int> xs)  =>  Reduce(xs,  (x, y)  => x + y)
);

var result =  sumOfSquares(numbers);  // 55

In this grand finale, we’ve composed two higher-order functions, Map and Reduce, to create a new function that calculates the sum of squares. It’s a fitting end to our symphony of higher-order functions in C#.

With the power of higher-order functions at your fingertips, you’re well-equipped to tackle complex problems in a flexible, composable, and functional way. So, go forth and spread the joy of functional programming in C# – and don’t forget to have a little fun along the way!

## 3.3 Lambda Expressions

Lambda expressions, the mysterious and magical creatures of the C# world, are like tiny ninjas that sneak into your code to make it more functional and expressive. In this chapter, we’ll unlock the secrets of these enigmatic warriors, exploring their origins, their techniques, and the powerful arsenal of tricks they bring to the functional programming dojo.

## Lambda Expressions: A Brief History

Before diving into lambda expressions, let’s take a quick trip down memory lane to understand their roots. Lambda expressions have their origins in lambda calculus, a mathematical system developed by Alonzo Church in the 1930s. In this system, functions are the stars of the show, and they can be composed, applied, and manipulated just like numbers.

Fast forward to today, and lambda expressions have found their way into the hearts and codebases of C# developers everywhere. They provide a concise way to represent anonymous functions, making it easy to create and pass around small, reusable pieces of behavior.

## The Art of Lambda Expressions

Lambda expressions in C# are like miniature works of art, each one a tiny masterpiece of functional beauty. Here’s a basic example to set the stage:

Func<int,  int> square = x => x * x;

int result =  square(5);  // 25

In this example, we define a simple lambda expression that takes an integer and returns its square. It’s a small but powerful statement, effortlessly capturing the essence of the square function.

## Lambda Expressions in Action

Now that we’ve been introduced to lambda expressions, let’s see them in action. We’ll explore various scenarios where these mini marvels can make our code more expressive and functional.

### Event Handlers

Lambda expressions can make event handlers more concise and readable. Say goodbye to clunky delegate syntax and hello to elegant, one-liners:

button.Click  +=  (sender, e)  => MessageBox.Show("Button clicked!");

### LINQ Queries

As we mentioned earlier, LINQ is a powerful ally in the functional programming arena, and lambda expressions play a starring role:

var numbers =  new List<int>  {  1,  2,  3,  4,  5  };

var evenNumbers = numbers
    .Where(n => n %  2  ==  0)
    .Select(n => n *  2)
    .ToList();

With lambda expressions, our LINQ queries become sleek, functional masterpieces.

### Predicate Functions

Lambda expressions shine when it comes to creating predicate functions on the fly:

bool  isEven(int n)  => n %  2  ==  0;
bool  isOdd(int n)  =>  !isEven(n);

var numbers =  new List<int>  {  1,  2,  3,  4,  5  };
var evenNumbers = numbers.Where(isEven).ToList();  // [2, 4]
var oddNumbers = numbers.Where(isOdd).ToList();  // [1, 3, 5]

### The Limits of Lambda Expressions

Lambda expressions, while undeniably powerful, have their limitations. They cannot be used to define recursive functions, and they are less suitable for complex, multi-statement functions. In these cases, it’s best to stick with traditional methods or local functions.

### Lambda Expressions

As we bid farewell to lambda expressions, let’s celebrate their unique contribution to the C# language. These compact, functional ninjas have made our code more expressive, more reusable, and more fun.

So, go forth and harness the power of lambda expressions in your C# projects. Embrace their functional flair, and immerse yourself in the creative world of functional programming. With lambda expressions by your side, you’ll write code that’s not only more efficient and expressive but also sprinkled with a touch of whimsy and excitement.

Never forget the lessons these tiny warriors have taught us, and may your C# journey be filled with the elegance and simplicity that lambda expressions bring to the table. Keep exploring, keep experimenting, and above all, keep having fun with your code. Lambda expressions may be small, but their impact on your programming style will be mighty.

## 3.4 Closures

Closures are like the cozy corners in the living room of functional programming – warm, inviting, and full of secrets. They allow us to create function instances that remember the context in which they were created, making it possible to elegantly capture and store state. In this chapter, we’ll snuggle up with closures in C#, exploring their inner workings and discovering how they can help us write more expressive and functional code.

### Closures: A Quick Introduction

At their core, closures are functions that remember the environment in which they were created. When you define a function inside another function, the inner function can access the variables of the outer function, even after the outer function has completed execution. Sounds like magic, doesn’t it?

Let’s see closures in action with a simple example:

public Func<int,  int>  MakeAdder(int x)
{
 return y => x + y;
}

var addFive =  MakeAdder(5);
int result =  addFive(3);  // 8

In this example, the MakeAdder function returns a lambda expression that captures the x parameter. The addFive function can still access the value of x even after MakeAdder has finished executing. This is the magic of closures!

Under the Hood: How Closures Work in C# Now that we’ve seen closures in action, let’s take a peek behind the curtain and explore how they work in C#. When the C# compiler encounters a closure, it generates a special hidden class that encapsulates the captured variables. This class has a field for each captured variable, and the lambda expression is transformed into a method of the hidden class.

For example, our MakeAdder function from earlier would be transformed by the compiler into something like this:

public Func<int,  int>  MakeAdder(int x)
{
 return y => x + y;
}

var addFive =  MakeAdder(5);
int result =  addFive(3);  // 8

In this example, the MakeAdder function returns a lambda expression that captures the x parameter. The addFive function can still access the value of x even after MakeAdder has finished executing. This is the magic of closures!

### Under the Hood: How Closures Work in C

Now that we’ve seen closures in action, let’s take a peek behind the curtain and explore how they work in C#. When the C# compiler encounters a closure, it generates a special hidden class that encapsulates the captured variables. This class has a field for each captured variable, and the lambda expression is transformed into a method of the hidden class.

For example, our MakeAdder function from earlier would be transformed by the compiler into something like this:

private  class ClosureClass
{
    public  int x;

public  int  Adder(int y)
    {
        return x + y;
    }
}

public Func<int,  int>  MakeAdder(int x)
{
 var closure =  new ClosureClass { x = x };
 return closure.Adder;
}

With this behind-the-scenes knowledge, we can truly appreciate the power and elegance of closures in C#.

### Closures in Everyday Code

Closures can be found in many places throughout our C# code. Let’s explore some scenarios where closures come in handy and make our code more functional and expressive.

Callbacks and Event Handlers

Closures are particularly useful when working with callbacks and event handlers, as they allow us to capture and maintain state across multiple invocations:

public void RegisterCallback(Action callback)
{
    // ...
}

int counter = 0;
RegisterCallback(() => Console.WriteLine($"Callback invoked {++counter} times"));

In this example, the closure captures the counter variable, allowing it to maintain its state across multiple invocations of the callback.

Lazy Initialization Closures can help us implement lazy initialization in a clean and efficient way:

private  int? _cachedValue;

public  int  ExpensiveComputation()
{
    if  (_cachedValue ==  null)
    {
_cachedValue =  // Perform expensive computation
    }

return _cachedValue.Value;
}

public Func<int> LazyComputation =  ()  =>
{
    if  (_cachedValue ==  null)
    {
_cachedValue =  // Perform expensive computation
    }

return _cachedValue.Value;
};

Using a closure, we can create a LazyComputation function that automatically handles caching the result of the expensive computation.

### The Grand Send-Off: Onward to Functional Data Structures and Patterns

As we leave the warm embrace of closures, we can appreciate the beauty and functionality they bring to our C# code. These magical constructs allow us to elegantly capture and maintain state, making our code more expressive and functional in the process.

Now that we’ve cozied up with closures, it’s time to embark on our next adventure: exploring the world of functional data structures and patterns in Chapter 4\. There, we’ll dive deep into the realm of immutability, persistent data structures, and functional design patterns that will further enhance our mastery of functional programming in C#.

So, grab your favorite cup of tea, wrap yourself in a cozy blanket of functional knowledge, and get ready for the exciting journey ahead. Closures have taught us to embrace the power of captured state, and now it’s time to conquer new challenges with functional data structures and patterns. Onward, brave coder!

# Chapter 4: Functional Data Structures and Patterns

## 4.1\. Tuples and Records: Data’s Dynamic Duo

In the action-packed world of functional programming, two heroes stand out from the crowd: Tuples and Records. These super-powered data structures help us create immutable, expressive, and functional code that’s not only easy on the eyes but also a joy to work with. Let’s join forces with this dynamic duo and learn how they can help us save the day!

### Tuples: Small but Mighty

Tuples are like those tiny candies that pack a big punch of flavor. They’re small, immutable collections of values, perfect for when you need to group together a few related pieces of data. No need for fancy classes or structures, just grab a Tuple and you’re good to go!

Here’s a simple example to get us started:

var person = Tuple.Create("Ada",  "Lovelace",  36);

Console.WriteLine($"{person.Item1} {person.Item2} is {person.Item3} years old.");

In this example, we create a tuple to store the first name, last name, and age of a person. It’s a quick and easy way to bundle together some related data without the overhead of defining a custom class.

But wait, there’s more! C# 7 introduced a new, sleeker syntax for tuples, called ValueTuples:

var person = ("Ada", "Lovelace", 36);

Console.WriteLine($"{person.Item1} {person.Item2} is {person.Item3} years old.");

And for even more readability, we can give our tuple elements custom names:

var person = (FirstName: "Ada", LastName: "Lovelace", Age: 36);

Console.WriteLine($"{person.FirstName} {person.LastName} is {person.Age} years old.");

### Records: Immutability’s Dream Team

While tuples are great for small collections of data, sometimes we need something with a little more oomph. Enter Records – the epitome of immutable data structures in C#. These bad boys provide all the functionality of classes, but with the added benefits of immutability and value-based equality.

Introduced in C# 9, records make it easy to define immutable data structures with minimal boilerplate:

public record Person(string FirstName, string LastName, int Age);

Just like that, we’ve created a record with properties for first name, last name, and age. And thanks to the magic of records, we get immutability, value-based equality, and a whole host of other functional goodies for free:

var ada = new Person("Ada", "Lovelace", 36);
var clone = ada with { Age = 37 };

Console.WriteLine(ada == clone); // False, since they have different ages

In this example, we create a Person record for Ada Lovelace and then use the with keyword to create a new record that’s a clone of the original, but with an updated age. Notice that the original record remains unchanged, showcasing the immutability of records.

## Tuples and Records: Unstoppable Together

Tuples and records are a formidable team in the functional programming universe. They provide us with flexible, immutable data structures that make our code more expressive and easier to reason about. With these heroes at our side, we can boldly conquer the challenges of functional programming in C# and emerge victorious.

So, go forth and harness the power of tuples and records in your projects. With their combined might, you’ll vanquish the forces of complexity and chaos, bringing order and elegance to your code. And always remember: functional programming is not just a set of tools and techniques, but also a mindset that empowers you to tackle problems in a more expressive, maintainable, and robust way.

As we continue our journey through the exciting world of functional C#, we’ll encounter more functional data structures and patterns that will help us level up our skills and unlock new possibilities. Stay tuned for more thrilling adventures, where we’ll explore concepts like immutability, persistent data structures, and functional design patterns that will further enhance our mastery of functional programming in C#.

Now that we’ve teamed up with tuples and records, we’re ready to face any challenge that comes our way. So, buckle up, grab your trusty keyboard, and prepare for the epic quest ahead. With the power of functional data structures and patterns by your side, there’s no limit to what you can achieve.

## 4.2 Pattern Matching: A Whodunit of Code

Imagine you’re a code detective, searching for clues and piecing together information to solve the mystery of complex conditional logic. Enter pattern matching – the Sherlock Holmes of functional programming. With pattern matching, you can express complex conditions in a concise and elegant way, making your code easier to read and maintain. So, grab your magnifying glass and let’s start cracking the case!

Elementary, My Dear Coder: Basic Pattern Matching C# 7 introduced the switch expression, which allows us to perform pattern matching in a more concise and functional way. Say goodbye to the clunky old switch statement and hello to the sleek new switch expression. Here’s a simple example to get us started:

public string GetDayOfWeek(int day)
{
    return day switch
    {
        1 => "Monday",
        2 => "Tuesday",
        3 => "Wednesday",
        4 => "Thursday",
        5 => "Friday",
        6 => "Saturday",
        7 => "Sunday",
        _ => throw new ArgumentOutOfRangeException(nameof(day))
    };
}

In this example, we use the switch expression to map an integer value to a day of the week. Notice how each case is expressed as a simple lambda-like syntax, making the code concise and easy to read.

The Game is Afoot: Advanced Pattern Matching Pattern matching gets even more powerful when combined with other C# features like tuples, records, and nullable types. Let’s explore some advanced pattern matching techniques that will help us solve even the trickiest of code mysteries.

Tuple Patterns Tuple patterns allow us to match on multiple values at once, making it easy to express complex conditions. Here’s an example that demonstrates how to classify a pair of numbers as greater, lesser, or equal:

public  string  CompareNumbers(int a,  int b)
{
    return  (a, b)  switch
    {
        (var x,  var y) when x > y =>  "Greater",
        (var x,  var y) when x < y =>  "Lesser",
        (_, _)  =>  "Equal"
    };
}

In this example, we create a tuple with the two numbers and use pattern matching to compare them. The when keyword lets us add additional conditions to our cases, giving us fine-grained control over the matching process.

Record Patterns Pattern matching with records allows us to match on the shape and properties of objects. Here’s an example that demonstrates how to classify geometric shapes using record patterns:

public record Shape;
public record Circle(double Radius)  : Shape;
public record Rectangle(double Width,  double Height)  : Shape;

public  string  DescribeShape(Shape shape)
{
    return shape switch
    {
Circle { Radius:  0  }  =>  "A point",
Circle c => $"A circle with radius {c.Radius}",
Rectangle r => $"A rectangle with width {r.Width} and height {r.Height}",
_ =>  throw  new  NotSupportedException("Unknown shape")
    };
}

In this example, we use record patterns to match on the type and properties of different shapes. The code is both concise and expressive, allowing us to quickly understand the different cases being handled.

The Adventure Continues: Embracing the Power of Pattern Matching As we close the case on pattern matching, we can appreciate the elegance and expressiveness it brings to our C# code. By combining the power of pattern matching with other functional programming features like tuples, records, and nullable types, we can write code that’s easy to read, maintain, and reason about.

Now that you’ve honed your pattern matching skills, you’re ready to tackle more complex and challenging code mysteries. Embrace the power of pattern matching in your projects and watch as your code becomes cleaner, more expressive, and more maintainable.

As we continue to explore the world of functional C#, we’ll discover even more powerful techniques and patterns to level up our programming skills. From immutability and persistent data structures to higher-order functions and beyond, there’s a treasure trove of functional knowledge waiting to be unlocked.

So, keep your magnifying glass handy, your wit sharp, and your curiosity piqued as we delve deeper into the fascinating realm of functional programming in C#. With pattern matching as one of your many tools, you’ll be well-equipped to solve the most perplexing code conundrums and emerge as a true functional programming detective. Happy sleuthing, dear coder!

## 4.3 Discriminated Unions: The Swiss Army Knife of Data Types

In the realm of functional programming, there’s one data type that truly stands out from the crowd – the discriminated union. It’s like a Swiss Army knife, versatile and powerful, ready to tackle any problem you throw at it. Discriminated unions allow us to represent a choice between several different, yet related data types, making them perfect for modeling complex, hierarchical data structures. So, let’s dive in and see how these nifty data types can enhance our functional C# skills!

### What’s in a Name: Introducing Discriminated Unions

Discriminated unions are a way to represent a value that can be one of several different types, each with its own set of properties. They’re a powerful way to model complex data and are commonly found in functional programming languages like Haskell, F#, and others. While C# doesn’t have a built-in discriminated union type, we can emulate them using some clever tricks and record types.

### A Menagerie of Types: Modeling Animals

To demonstrate the power of discriminated unions, let’s create a small menagerie of animals, each with its own unique set of properties:

public abstract record Animal;

public record Mammal(int Legs, bool HasTail) : Animal;
public record Bird(bool CanFly, string Color) : Animal;
public record Fish(int Fins, bool HasScales) : Animal;

In this example, we’ve defined an abstract Animal record and three derived records for different types of animals. Each derived record has its own set of properties specific to its type. This hierarchy of types emulates a discriminated union, allowing us to represent a value that can be one of several different animal types.

The Lion, the Finch, and the Goldfish: Pattern Matching with Discriminated Unions Now that we’ve got our animal kingdom set up, let’s see how discriminated unions and pattern matching can work together in perfect harmony. Here’s an example of a function that classifies animals based on their properties:

public string ClassifyAnimal(Animal animal)
{
    return animal switch
    {
        Mammal { Legs: 4, HasTail: true } => "Quadruped mammal with a tail",
        Bird { CanFly: true, Color: var color } => $"A flying {color} bird",
        Fish { Fins: var fins, HasScales: true } => $"A fish with {fins} fins and scales",
        _ => "An interesting creature indeed!"
    };
}

In this example, we use pattern matching to classify animals based on their type and properties. The concise and expressive syntax allows us to quickly understand the various cases being handled, showcasing the power of discriminated unions and pattern matching combined.

### Samples Galore: More Discriminated Union Goodness

The possibilities with discriminated unions are endless! You can model anything from expressions in a programming language to the various states of a game character. Here’s an example of modeling arithmetic expressions using discriminated unions:

public abstract record Expr;

public record Constant(int Value) : Expr;
public record Add(Expr Left, Expr Right) : Expr;
public record Subtract(Expr Left, Expr Right) : Expr;
public record Multiply(Expr Left, Expr Right) : Expr;
public record Divide(Expr Left, Expr Right) : Expr;

And here’s an example of modeling game character states:

public abstract record CharacterState;

public record Idle : CharacterState;
public record Running : CharacterState;
public record Jumping(double Height) : CharacterState;
public record Attacking(int Damage) : CharacterState;

Now that we have our character state hierarchy set up, let’s use pattern matching to handle different states and perform actions accordingly:

public void HandleCharacterState(CharacterState state)
{
    switch (state)
    {
        case Idle:
            Console.WriteLine("Character is idle");
            break;
        case Running:
            Console.WriteLine("Character is running");
            break;
        case Jumping(var height):
            Console.WriteLine($"Character is jumping with a height of {height}");
            break;
        case Attacking(var damage):
            Console.WriteLine($"Character is attacking with a damage of {damage}");
            break;
        default:
            Console.WriteLine("Unknown character state");
            break;
    }
}

In this example, we use pattern matching to handle different character states and perform appropriate actions. Discriminated unions and pattern matching together make it easy to express complex behavior in a concise and readable manner.

Unleashing the Power of Discriminated Unions As we wrap up our exploration of discriminated unions, we can see just how versatile and powerful they can be in our functional C# code. By combining discriminated unions with other functional programming techniques like pattern matching, we can model complex data and behavior in a clean, expressive, and maintainable way.

Now that you’ve experienced the awesomeness of discriminated unions, you’re ready to tackle even more challenging and intricate problems with your newfound functional C# prowess. So, go forth and create your own menageries, expressions, and character states – and unleash the full potential of discriminated unions in your projects. Happy coding!

## 4.4 Deconstruction

Deconstruction is a powerful feature in C# that allows you to break down complex data structures into their individual parts. It’s like opening a box of assorted chocolates and picking out your favorite ones. In this chapter, we’ll dive into the world of deconstruction, unraveling the mysteries of tuples, records, and more.

### 4.4.1 Deconstructing Tuples

Tuples in C# are simple, lightweight data structures that can hold multiple values. They are often used to group related data together. Deconstructing a tuple means extracting its individual elements into separate variables. Here’s a simple example:

var person =  (Name:  "Alice", Age:  30);

// Deconstructing the tuple
(string name,  int age)  = person;

Console.WriteLine($"Name: {name}, Age: {age}");

In this example, we created a tuple person with two named elements: Name and Age. We then deconstructed the tuple into two separate variables, name and age, using the deconstruction syntax.

### 4.4.2 Deconstructing Records

Records, like tuples, are data structures in C# that are used to group related data. They were introduced in C# 9 and provide a more sophisticated way of creating immutable data structures. To deconstruct a record, you need to define a Deconstruct method within the record. Let’s see an example:

public record Car(string Make,  string Model,  int Year)
{
    public  void  Deconstruct(out  string make,  out  string model,  out  int year)
    {
make = Make;
model = Model;
year = Year;
    }
}

var myCar =  new  Car("Tesla",  "Model S",  2022);

// Deconstructing the record
(string make,  string model,  int year)  = myCar;

Console.WriteLine($"Make: {make}, Model: {model}, Year: {year}");

In this example, we defined a record Car with a Deconstruct method that takes three out parameters. We then created an instance of Car and deconstructed it into three separate variables: make, model, and year.

4.4.3 Deconstructing with Patterns Pattern matching is a powerful feature in C# that allows you to match and deconstruct data structures based on their shape. Deconstruction can be combined with pattern matching to create more expressive and flexible code. Here’s an example:

public  abstract record Shape;

public record Circle(double Radius)  : Shape;

public record Rectangle(double Width,  double Height)  : Shape;

public  static  double  CalculateArea(Shape shape)  => shape switch
{
 Circle(var radius)  => Math.PI  * radius * radius,
 Rectangle(var width,  var height)  => width * height,
_ =>  throw  new  NotSupportedException("Unknown shape")
};

var myCircle =  new  Circle(5);
var myRectangle =  new  Rectangle(3,  4);

Console.WriteLine($"Circle area: {CalculateArea(myCircle)}");
Console.WriteLine($"Rectangle area: {CalculateArea(myRectangle)}");

In this example, we defined an abstract record Shape and two derived records: Circle and Rectangle. We then created a method CalculateArea that uses pattern matching and deconstruction to calculate the area of a shape based on its type.

### 4.4.4 Deconstructing with Extension Methods

If you want to deconstruct a class or struct that you don’t control, you can use extension methods to add deconstruction functionality. Here’s an example of how to deconstruct a KeyValuePair<TKey, TValue>:

public  static  class KeyValuePairExtensions
{
    public  static  void Deconstruct<TKey, TValue>(this KeyValuePair<TKey, TValue> kvp,  out TKey key,  out TValue value)
    {
key = kvp.Key;
value = kvp.Value;
    }
}

var dictionary =  new Dictionary<string,  int>  {  {  "apple",  5  },  {  "banana",  3  }  };

foreach  (var  (key, value)  in dictionary)
{
    Console.WriteLine($"Key: {key}, Value: {value}");
}

In this example, we defined an extension method Deconstruct for KeyValuePair<TKey, TValue> that takes two out parameters. This allows us to deconstruct instances of KeyValuePair<TKey, TValue> directly within a foreach loop when iterating over a dictionary.

### 4.4.5 Deconstruction Gotchas and Tips

While deconstruction is a handy tool, there are some things to keep in mind when using it:

*   Deconstruction is not limited to tuples and records; you can deconstruct any class or struct that has a suitable Deconstruct method or extension method.

*   When defining a Deconstruct method, always use out parameters for the individual elements. This ensures that the method can be used in deconstruction syntax.

*   Be mindful of the order in which elements are deconstructed. The order of the out parameters in the Deconstruct method must match the order of the variables in the deconstruction syntax.

And that’s a wrap on deconstruction! By combining this powerful feature with tuples, records, pattern matching, and extension methods, you can create more expressive and flexible code. In the next chapter, we’ll explore other functional data structures and patterns to further hone your functional programming skills in C#. Stay tuned for more exciting adventures!

5: Functional Programming Techniques in C#

5.1\. Recursion: Mastering the Art of Self-Reference

Recursion is an essential technique in functional programming, where a function calls itself to solve a problem. It’s similar to how the iconic riff from Led Zeppelin’s “Stairway to Heaven” seems to loop endlessly, drawing you deeper into the song.

To understand recursion, we need to explore its core concepts: the base case and the recursive case. The base case is the simplest scenario where the function stops calling itself and returns a value. The recursive case is when the function calls itself to solve a smaller sub-problem.

Let’s examine the classic example of calculating the factorial of a number using recursion in C#:

using System;

class Program
{
    static  int  Factorial(int n)
    {
        if  (n ==  1)
        {
            return  1;
        }
        else
        {
            return n *  Factorial(n -  1);
        }
    }

static  void  Main()
    {
        int number =  5;
        Console.WriteLine($"The factorial of {number} is {Factorial(number)}");
    }
}

In this example, the Factorial() function calculates the factorial of a given number ‘n’. The base case is when ‘n’ equals 1, and the function returns 1\. The recursive case is when the function calls itself with the argument ‘n - 1’, working towards the base case.

Another example is the Fibonacci sequence, where each number is the sum of the two preceding ones. Here’s a C# implementation using recursion:

using System;

class Program
{
    static  int  Fibonacci(int n)
    {
        if  (n ==  0)
        {
            return  0;
        }
        else  if  (n ==  1)
        {
            return  1;
        }
        else
        {
            return  Fibonacci(n -  1)  +  Fibonacci(n -  2);
        }
    }

static  void  Main()
    {
        int position =  10;
        Console.WriteLine($"The {position}th number in the Fibonacci sequence is {Fibonacci(position)}");
    }
}

In this example, the base cases are when ‘n’ equals 0 or 1, and the function returns the corresponding values. The recursive case is when the function calls itself twice, once with the argument ‘n - 1’ and once with ‘n - 2’, to calculate the sum of the preceding two numbers.

Despite its power, recursion has some drawbacks. It can lead to performance issues due to the overhead of function calls and potential stack overflows. To mitigate these issues, a technique called “tail recursion” can be used, where the recursive call is the last operation performed in the function. This allows the compiler to optimize the code and avoid stack overflows. Here’s the factorial example with tail recursion:

using System;

class Program
{
    static  int  TailRecursiveFactorial(int n,  int accumulator =  1)
    {
        if  (n ==  1)
        {
            return accumulator;
        }
        else
        {
            return  TailRecursiveFactorial(n -  1, accumulator * n);
        }
    }

static  void  Main()
    {
        int number =  5;
        Console.WriteLine($"The factorial of {number} is {TailRecursiveFactorial(number)}");
    }
}

In this example, we introduced an accumulator parameter that holds the result so far. This change allows the compiler to optimize the function calls and prevent stack overflows.

Now that we’ve delved into recursion, we’ll move on to another functional programming technique: Currying and Partial Application.

# Chapter 5: Currying and Partial Application: The Art of Splitting Functions

Currying and Partial Application are like remixing your favorite rock tunes. You take an original track, split it into smaller pieces, and rearrange them to create something fresh and exciting. In functional programming, these techniques enable you to break down complex functions into simpler ones and reuse code more effectively.

Currying is the process of transforming a function that takes multiple arguments into a series of functions that each take a single argument. This technique can make your code more flexible and easier to compose.

Let’s start with a simple example. We’ll create a function that calculates the total price of a product after applying a discount and adding tax. Here’s the original, non-curried version:

using System;

class Program
{
    static  decimal  CalculateTotalPrice(decimal price,  decimal discount,  decimal tax)
    {
        decimal discountedPrice = price *  (1  - discount);
        return discountedPrice *  (1  + tax);
    }

static  void  Main()
    {
        decimal price =  100;
        decimal discount =  0.1m;
        decimal tax =  0.2m;

Console.WriteLine($"The total price is {CalculateTotalPrice(price, discount, tax)}");
    }
}

Now, let’s curry the CalculateTotalPrice() function:

using System;

class Program
{
    static Func<decimal, Func<decimal, Func<decimal,  decimal>>> CurriedCalculateTotalPrice =>
price => discount => tax => price *  (1  - discount)  *  (1  + tax);

static  void  Main()
    {
        decimal price =  100;
        decimal discount =  0.1m;
        decimal tax =  0.2m;

var applyPrice =  CurriedCalculateTotalPrice(price);
        var applyDiscount =  applyPrice(discount);
        var calculateTotal =  applyDiscount(tax);

Console.WriteLine($"The total price is {calculateTotal}");
    }
}

In this example, we transformed the CalculateTotalPrice() function into a series of functions using the currying technique. Each function takes a single argument and returns another function, eventually calculating the total price.

Partial Application is a technique that involves fixing a number of arguments in a function, generating a new function with fewer arguments. This allows you to create reusable and more specialized functions.

Let’s create a library that provides a nice way to use currying with extension methods. We’ll also implement a generic currying method:

public  static  class CurryExtensions
{
    public  static Func<T2, Func<T3, TResult>> Curry<T1, T2, T3, TResult>(this Func<T1, T2, T3, TResult> func, T1 arg1)
    {
        return arg2 => arg3 =>  func(arg1, arg2, arg3);
    }
}

Now, let’s use this extension method to curry the CalculateTotalPrice() function:

using System;
using CurryLibrary;

class Program
{
    static  decimal  CalculateTotalPrice(decimal price,  decimal discount,  decimal tax)
    {
        decimal discountedPrice = price *  (1  - discount);
        return discountedPrice *  (1  + tax);
    }

static  void  Main()
    {
        decimal price =  100;
        decimal discount =  0.1m;
        decimal tax =  0.2m;

var curriedCalculateTotalPrice =  ((Func<decimal,  decimal,  decimal,  decimal>)CalculateTotalPrice).Curry(price);
        var applyDiscount =  curriedCalculateTotalPrice(discount);
        var calculateTotal =  applyDiscount(tax);

Console.WriteLine($"The total price is {calculateTotal}");
    }
}

In this example, we used the Curry() extension method to curry the CalculateTotalPrice() function. The advantage of this approach is that you can curry any function with three arguments without having to change its implementation.

Now, let’s explore a use case for Partial Application. Imagine you have a comic book store, and you want to apply a 10% discount to all Marvel comics. You can use Partial Application to create a specialized function that applies this discount:

public  static  class PartialApplicationExtensions
{
    public  static Func<T2, TResult> Apply<T1, T2, TResult>(this Func<T1, T2, TResult> func, T1 arg1)
    {
        return arg2 =>  func(arg1, arg2);
    }
}

Using the Apply() extension method, we can create a specialized function that applies a 10% discount:

using System;
using CurryLibrary;

class Program
{
    static  decimal  ApplyDiscount(decimal discount,  decimal price)
    {
        return price *  (1  - discount);
    }

static  void  Main()
    {
        decimal price =  100;
        decimal discount =  0.1m;

var applyMarvelDiscount =  ((Func<decimal,  decimal,  decimal>)ApplyDiscount).Apply(discount);
        var discountedPrice =  applyMarvelDiscount(price);

Console.WriteLine($"The discounted price is {discountedPrice}");
    }
}

In this example, we used the Apply() extension method to fix the discount argument in the ApplyDiscount() function, creating a specialized function that applies a 10% discount to any price.

Currying and Partial Application are like the dynamic duo of functional programming, allowing you to break down complex functions into simpler, reusable components. It’s similar to how the legendary partnership of Mick Jagger and Keith Richards in The Rolling Stones produced countless rock anthems. By mastering these techniques, you can create harmony in your code and build more robust, maintainable applications.

In the next section, we’ll explore another powerful functional programming technique: Lazy Evaluation.

## 5.3\. Lazy Evaluation: The Art of Procrastination

In the world of functional programming, Lazy Evaluation is like a favorite pastime, akin to binge-watching your favorite Star Trek series. Just as you might postpone chores to enjoy your favorite show, Lazy Evaluation defers the execution of a computation until its result is actually needed.

Lazy Evaluation can improve performance by avoiding unnecessary calculations and reducing memory usage. In C#, you can achieve Lazy Evaluation using the Lazy class or by working with lazy sequences through LINQ’s deferred execution.

Let’s dive into some examples to see Lazy Evaluation in action.

### 5.3.1\. Using the Lazy Class

The Lazy class allows you to defer the initialization of an object until it’s accessed for the first time. This can be particularly useful when creating expensive resources, like large data structures or network connections.

Consider a scenario where we have a class ComicBookLibrary, which loads a large list of comic books from an external source:

using System;
using System.Collections.Generic;

class ComicBook
{
 public  string Title {  get;  set;  }
 public  int IssueNumber {  get;  set;  }
}

class ComicBookLibrary
{
    private List<ComicBook> _comicBooks;

public  ComicBookLibrary()
    {
_comicBooks =  LoadComicBooks();
    }

private List<ComicBook>  LoadComicBooks()
    {
        // Expensive operation to load comic books from an external source
        Console.WriteLine("Loading comic books...");
        return  new List<ComicBook>  {  new ComicBook { Title =  "Spider-Man", IssueNumber =  1  }  };
    }

public List<ComicBook>  GetComicBooks()
    {
        return _comicBooks;
    }
}

In this example, the LoadComicBooks() method is called during the object’s construction, which could lead to performance issues if the operation is expensive. We can use the Lazy class to defer the loading of comic books until they’re actually needed:

using System;
using System.Collections.Generic;

class ComicBook
{
 public  string Title {  get;  set;  }
 public  int IssueNumber {  get;  set;  }
}

class ComicBookLibrary
{
    private Lazy<List<ComicBook>> _lazyComicBooks;

public  ComicBookLibrary()
    {
_lazyComicBooks =  new Lazy<List<ComicBook>>(LoadComicBooks);
    }

private List<ComicBook>  LoadComicBooks()
    {
        // Expensive operation to load comic books from an external source
        Console.WriteLine("Loading comic books...");
        return  new List<ComicBook>  {  new ComicBook { Title =  "Spider-Man", IssueNumber =  1  }  };
    }

public List<ComicBook>  GetComicBooks()
    {
        return _lazyComicBooks.Value;
    }
}

Now, the LoadComicBooks() method is only called when the GetComicBooks() method is executed for the first time, reducing the overhead during object construction.

### 5.3.2\. Lazy Sequences with LINQ

LINQ (Language Integrated Query) is a powerful querying library in C# that supports Lazy Evaluation through deferred execution. When you chain together a sequence of LINQ operations, the actual execution is postponed until the result is enumerated.

Let’s create a list of integers and filter out the even numbers using LINQ:

using System;
using System.Linq;
using System.Collections.Generic;

class Program
{
    static  void  Main()
    {
        List<int> numbers = Enumerable.Range(1,  100).ToList();

Console.WriteLine("Creating filtered sequence...");
        var evenNumbers = numbers.Where(n => n %  2  ==  0);
        Console.WriteLine("Enumerating filtered sequence...");
        foreach  (var number in evenNumbers)
        {
            Console.WriteLine(number);
        }
    }
}

In this example, the Where() method is a LINQ operation that creates a new sequence of even numbers. However, the actual filtering isn’t executed until the foreach loop enumerates the evenNumbers sequence. This is an example of Lazy Evaluation through deferred execution.

Now, let’s take it a step further and combine Lazy Evaluation with the yield keyword to create an infinite sequence:

using System;
using System.Linq;
using System.Collections.Generic;

class Program
{
    static IEnumerable<int>  GenerateFibonacciSequence()
    {
        int previous =  -1;
        int current =  1;

while  (true)
        {
            int next = previous + current;
previous = current;
current = next;

yield  return next;
        }
    }

static  void  Main()
    {
        Console.WriteLine("Creating Fibonacci sequence...");
        var fibonacciSequence =  GenerateFibonacciSequence();

Console.WriteLine("Enumerating Fibonacci sequence...");
        foreach  (var number in fibonacciSequence.Take(10))
        {
            Console.WriteLine(number);
        }
    }
}

In this example, we used the yield keyword to create an infinite Fibonacci sequence. Due to Lazy Evaluation, only the first 10 numbers are generated when we enumerate the sequence using the Take() method.

Lazy Evaluation is like the art of procrastination, delaying computations until they’re absolutely necessary. By embracing this functional programming technique, you can optimize your C# code for performance and memory usage, much like how binge-watching your favorite Star Trek episodes allows you to maximize your leisure time.

In the next section, we’ll boldly go where no developer has gone before and explore the mysterious realm of Monads. Get ready to unlock the secrets of these enigmatic entities and apply their awesome power in your functional programming journey!

## 5.4\. Memoization: The Art of Remembering

Memoization is like having an eidetic memory, much like Sheldon Cooper from The Big Bang Theory. In functional programming, Memoization allows you to remember and store the results of expensive function calls, so you don’t have to recalculate them if the same inputs are provided again.

Memoization can significantly improve the performance of recursive functions or computations with overlapping subproblems. In C#, you can implement Memoization using dictionaries, caches, or even custom decorators.

Let’s explore some examples to better understand Memoization in action.

### 5.4.1\. Memoizing Recursive Functions

Consider the classic example of computing Fibonacci numbers using a naive recursive implementation:

using System;

class Program
{
    static  int  Fibonacci(int n)
    {
        if  (n <=  1)  return n;
        return  Fibonacci(n -  1)  +  Fibonacci(n -  2);
    }

static  void  Main()
    {
        Console.WriteLine($"The 30th Fibonacci number is {Fibonacci(30)}");
    }
}

The problem with this implementation is that it recalculates the same Fibonacci numbers multiple times, leading to an exponential runtime. We can optimize this code by memoizing the results of previous computations:

using System;
using System.Collections.Generic;

class Program
{
 static Dictionary<int,  int> _memo =  new Dictionary<int,  int>();

static  int  Fibonacci(int n)
    {
        if  (n <=  1)  return n;

if  (!_memo.ContainsKey(n))
        {
            _memo[n]  =  Fibonacci(n -  1)  +  Fibonacci(n -  2);
        }

return _memo[n];
    }

static  void  Main()
    {
        Console.WriteLine($"The 30th Fibonacci number is {Fibonacci(30)}");
    }
}

In this example, we used a dictionary to store the results of previous Fibonacci calculations. When a Fibonacci number is requested, we first check if it’s already in the dictionary. If it is, we return the memoized value, avoiding the need for redundant calculations.

### 5.4.2\. Creating a Memoization Decorator

A more reusable approach to Memoization is to create a custom decorator that can memoize any function. Let’s implement a generic Memoize extension method:

public  static  class MemoizeExtensions
{
    public  static Func<T, TResult> Memoize<T, TResult>(this Func<T, TResult> func)
    {
        var memo =  new Dictionary<T, TResult>();

return arg =>
        {
            if  (!memo.ContainsKey(arg))
            {
                memo[arg]  =  func(arg);
            }

return memo[arg];
        };
    }
}

Now, we can use this decorator to memoize any function. Let’s use it to memoize our original Fibonacci function:

using System;
using MemoizeLibrary;

class Program
{
    static  int  Fibonacci(int n)
    {
        if  (n <=  1)  return n;
        return  MemoizedFibonacci(n -  1)  +  MemoizedFibonacci(n -  2);
    }

static Func<int,  int> MemoizedFibonacci =  ((Func<int,  int>)Fibonacci).Memoize();

static  void  Main()
    {
        Console.WriteLine($"The 30th Fibonacci number is {MemoizedFibonacci(30)}");
    }
}

In this example, we used the Memoize extension method to create a memoized version of the Fibonacci function. This approach is more reusable, as it can be applied to any function with a single input and output.

Memoization is like having a photographic memory in the world of functional programming. By remembering the results of expensive computations, you can optimize your code and eliminate redundant calculations, just like Sheldon Cooper’s remarkable recall ability helps him recall vast amounts of information.

In this section, we’ve explored how to implement Memoization in C# using dictionaries and custom decorators. By applying these techniques, you can unlock significant performance improvements in your code, especially when dealing with recursive functions or computations with overlapping subproblems.

Next up, we’ll explore the fascinating world of LINQ (Language Integrated Query), which brings the power of functional programming to the forefront of C#. LINQ enables you to write expressive, composable, and reusable code using a rich set of query operators. So, grab your favorite manga or comic book, and get ready to embark on an exciting voyage through the universe of functional programming in C# with LINQ as our guide!

# Chapter 6: LINQ: The Power of Functional Programming in C

## 6.1\. Introduction to LINQ

Much like the Force binds the Star Wars universe together, LINQ (Language Integrated Query) unites the world of functional programming in C#. LINQ is a powerful querying library that enables you to work with data in a more expressive, composable, and flexible way. It offers a rich set of query operators to filter, project, and transform data, treating both in-memory collections and external data sources as first-class citizens.

LINQ’s functional nature encourages a declarative programming style, which helps you write cleaner, more maintainable code. LINQ supports various data sources, such as in-memory collections, XML, and databases through its different providers: LINQ to Objects, LINQ to XML, and LINQ to SQL, respectively.

In this section, we’ll introduce you to the fundamentals of LINQ and showcase its power in the realm of functional programming. Let’s embark on this exciting journey, exploring the many ways LINQ can transform your C# code.

### 6.1.1\. Basic LINQ Syntax

LINQ provides two syntax options: query syntax and method syntax. Query syntax, inspired by SQL, offers a familiar and more readable way to write LINQ queries. Method syntax, on the other hand, uses extension methods and lambda expressions for a more functional programming approach.

Let’s look at an example of both syntax styles. Suppose we have a list of Star Wars characters and want to filter those with the “Jedi” profession:

using System;
using System.Linq;
using System.Collections.Generic;

class StarWarsCharacter
{
 public  string Name {  get;  set;  }
 public  string Profession {  get;  set;  }
}

class Program
{
    static  void  Main()
    {
        List<StarWarsCharacter> characters =  new List<StarWarsCharacter>
        {
            new StarWarsCharacter { Name =  "Luke Skywalker", Profession =  "Jedi"  },
            new StarWarsCharacter { Name =  "Han Solo", Profession =  "Smuggler"  },
            new StarWarsCharacter { Name =  "Obi-Wan Kenobi", Profession =  "Jedi"  },
            new StarWarsCharacter { Name =  "Darth Vader", Profession =  "Sith Lord"  }
        };

// Query syntax
        var jediCharactersQuery = from character in characters
                                  where character.Profession  ==  "Jedi"
                                  select character;

// Method syntax
        var jediCharactersMethod = characters.Where(c => c.Profession  ==  "Jedi");

Console.WriteLine("Jedi characters (Query syntax):");
        foreach  (var character in jediCharactersQuery)
        {
            Console.WriteLine(character.Name);
        }

Console.WriteLine("\nJedi characters (Method syntax):");
        foreach  (var character in jediCharactersMethod)
        {
            Console.WriteLine(character.Name);
        }
    }
}

In this example, we used both query syntax and method syntax to filter the list of characters by their profession. The result is the same, but the syntax styles cater to different preferences and programming paradigms.

## 6.2\. Query Syntax vs. Method Syntax

In the world of LINQ, there are two primary ways to express queries: Query Syntax and Method Syntax. Both have their unique advantages, and understanding their differences is crucial for using LINQ effectively. In this section, we’ll compare Query Syntax and Method Syntax, discuss their pros and cons, and provide examples to help you choose the best approach for your specific use case.

### 6.2.1\. Query Syntax

Query Syntax, also known as Query Expression Syntax, resembles SQL and is designed to be more readable and familiar to developers who work with databases. It uses a set of keywords, such as from, where, select, group, orderby, and join, to create a query expression.

Pros:

•           More readable and familiar to SQL developers.

•           Simplifies complex queries with multiple operations.

•           Provides support for transparent identifiers, which can simplify queries with multiple from clauses.

Cons:

•           Limited to a subset of LINQ operators.

•           Less flexible than Method Syntax, as it relies on a predefined set of keywords.

•           May require more code for simple operations. Example:

var highScorePlayers = from p in players
                       where p.Score >= 1000
                       orderby p.Name
                       select p.Name;

6.2.2\. Method Syntax

Method Syntax, also known as Fluent Syntax, relies on extension methods and lambda expressions. It offers a more functional programming approach and provides access to the full range of LINQ operators.

Pros:

More flexible, as it supports all LINQ operators. Encourages a functional programming style with extension methods and lambda expressions. Often results in more concise code for simple operations. Cons:

Less familiar and readable for SQL developers. Can lead to more complex code for queries with multiple operations. Doesn’t support transparent identifiers, which may require additional code for certain scenarios. Example:

var highScorePlayers = players.Where(p => p.Score  >=  1000)
                               .OrderBy(p => p.Name)
                               .Select(p => p.Name);

Let’s compare Query Syntax and Method Syntax using a more complex example. Suppose we want to join a list of authors with a list of books, and then group the books by author:

// Query Syntax
var booksByAuthorQuery = from author in authors
join book in books on author.Id equals book.AuthorId
                         group book by author.Name into bookGroup
select new  { Author = bookGroup.Key, Books = bookGroup.ToList()  };

// Method Syntax
var booksByAuthorMethod = authors.Join(books, a => a.Id, b => b.AuthorId,  (a, b)  =>  new  { a.Name, Book = b })
                                  .GroupBy(x => x.Name, x => x.Book)
                                  .Select(g =>  new  { Author = g.Key, Books = g.ToList()  });

In this example, Query Syntax is more readable and easier to understand for complex queries, whereas Method Syntax is more concise but may be harder to grasp for developers unfamiliar with functional programming.

Ultimately, choosing between Query Syntax and Method Syntax comes down to personal preference, readability, and the specific requirements of your project. It’s essential to understand both syntax styles, as they can be combined within a single query to harness the best of both worlds. So, experiment with both Query Syntax and Method Syntax, and embrace the power of LINQ to elevate your C# code to new heights.

## 6.2.3 Extending LINQ with Custom Query Operators

While LINQ provides a comprehensive set of operators, you may sometimes need custom operators tailored to your specific needs. By leveraging extension methods, you can create custom query operators that can be used seamlessly with both Query Syntax and Method Syntax. In this section, we’ll demonstrate how to create a small library of custom LINQ operators.

### 6.2.3.1 Custom Map Operator

Let’s create a custom Map operator, which behaves like Select. We’ll start by defining an extension method on IEnumerable:

using System;
using System.Collections.Generic;
using System.Linq;

public  static  class LinqExtensions
{
    public  static IEnumerable<TResult> Map<TSource, TResult>(this IEnumerable<TSource> source, Func<TSource, TResult> selector)
    {
        return source.Select(selector);
    }
}

Now we can use our custom Map operator with Method Syntax:

var numbers =  new List<int>  {  1,  2,  3,  4,  5  };
var squaredNumbers = numbers.Map(x => x * x);

To use our custom Map operator with Query Syntax, we need to create a custom query keyword. We’ll define an extension method on the IEnumerable with the map keyword:

public  static  class LinqExtensions
{
    public  static IEnumerable<TResult> map<TSource, TResult>(this IEnumerable<TSource> source, Func<TSource, TResult> selector)
    {
        return source.Select(selector);
    }
}

Now we can use our custom Map operator with Query Syntax:

var squaredNumbersQuery = from n in numbers
select n * n;

6.4.2\. Custom Bind Operator

Let’s create a custom Bind operator, which behaves like SelectMany. We’ll define an extension method on IEnumerable:

public  static  class LinqExtensions
{
    public  static IEnumerable<TResult> Bind<TSource, TResult>(this IEnumerable<TSource> source, Func<TSource, IEnumerable<TResult>> selector)
    {
        return source.SelectMany(selector);
    }
}

Now we can use our custom Bind operator with Method Syntax:

var names =  new List<string>  {  "Luke",  "Leia",  "Han"  };
var letterCombos = names.Bind(name => name.ToCharArray());

To use our custom Bind operator with Query Syntax, we need to create a custom query keyword. We’ll define an extension method on the IEnumerable with the bind keyword:

public  static  class LinqExtensions
{
    public  static IEnumerable<TResult> bind<TSource, TResult>(this IEnumerable<TSource> source, Func<TSource, IEnumerable<TResult>> selector)
    {
        return source.SelectMany(selector);
    }
}

Now we can use our custom Bind operator with Query Syntax:

var letterCombosQuery = from name in names
from letter in name.ToCharArray()
                        select letter;

In this next example, we’ll create a LINQ query to find the best flight fares from two different fake airline companies using Query Syntax. We’ll use extension methods to keep our code functional and clean.

First, let’s create classes to represent flight information:

public  class Flight
{
 public  string Airline {  get;  set;  }
 public  string Origin {  get;  set;  }
 public  string Destination {  get;  set;  }
 public DateTime DepartureDate {  get;  set;  }
 public  decimal Fare {  get;  set;  }
}

Next, we’ll create a static class with extension methods to fetch flight data from our fake airline companies:

using System.Collections.Generic;

public  static  class AirlineExtensions
{
    public  static IEnumerable<Flight>  GetFlightsFromAirline1(this  string origin)
    {
        // Fetch flights from Airline1 API (fake data for demonstration)
        return  new List<Flight>
        {
            new Flight { Airline =  "Airline1", Origin = origin, Destination =  "New York", DepartureDate = DateTime.Now.AddDays(1), Fare =  500  },
            new Flight { Airline =  "Airline1", Origin = origin, Destination =  "Los Angeles", DepartureDate = DateTime.Now.AddDays(2), Fare =  800  }
        };
    }

public  static IEnumerable<Flight>  GetFlightsFromAirline2(this  string origin)
    {
        // Fetch flights from Airline2 API (fake data for demonstration)
        return  new List<Flight>
        {
            new Flight { Airline =  "Airline2", Origin = origin, Destination =  "New York", DepartureDate = DateTime.Now.AddDays(3), Fare =  550  },
            new Flight { Airline =  "Airline2", Origin = origin, Destination =  "Los Angeles", DepartureDate = DateTime.Now.AddDays(4), Fare =  700  }
        };
    }
}

Now, let’s create a LINQ query using Query Syntax to fetch the best flight fares from both airlines:

using System;
using System.Linq;

class Program
{
    static  void  Main()
    {
        string origin =  "San Francisco";
        string destination =  "Los Angeles";

var bestFares = from airline1Flight in origin.GetFlightsFromAirline1()
from airline2Flight in origin.GetFlightsFromAirline2()
                        where airline1Flight.Destination  == destination && airline2Flight.Destination  == destination
let minFare = Math.Min(airline1Flight.Fare, airline2Flight.Fare)
                        orderby minFare
select new  { Airline =  (airline1Flight.Fare  <= airline2Flight.Fare)  ? airline1Flight.Airline  : airline2Flight.Airline, Fare = minFare };

Console.WriteLine($"Best flight fares from {origin} to {destination}:");
        foreach  (var fare in bestFares)
        {
            Console.WriteLine($"Airline: {fare.Airline}, Fare: ${fare.Fare}");
        }
    }
}

In this example, we’ve used Query Syntax to find the best flight fares from two different airlines. We’ve also utilized custom extension methods to fetch flight data and keep our code functional and clean.

To make the previous code work in parallel, we can use the AsParallel() extension method from the System.Linq.ParallelEnumerable class. This method enables parallelization of query execution, which can help to improve performance for large data sets and complex operations.

First, we need to add the System.Linq and System.Threading.Tasks namespaces to our extension methods class:

using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;

Now, let’s modify the AirlineExtensions class to return Task<IEnumerable> instead of IEnumerable. We’ll use Task.Run() to simulate asynchronous API calls for fetching flight data:

public  static  class AirlineExtensions
{
    public  static Task<IEnumerable<Flight>>  GetFlightsFromAirline1Async(this  string origin)
    {
        return Task.Run(()  =>
        {
            // Simulate asynchronous API call with Task.Delay
            Task.Delay(500).Wait();

// Fetch flights from Airline1 API (fake data for demonstration)
            return  new List<Flight>
            {
                new Flight { Airline =  "Airline1", Origin = origin, Destination =  "New York", DepartureDate = DateTime.Now.AddDays(1), Fare =  500  },
                new Flight { Airline =  "Airline1", Origin = origin, Destination =  "Los Angeles", DepartureDate = DateTime.Now.AddDays(2), Fare =  800  }
            }  as IEnumerable<Flight>;
        });
    }

public  static Task<IEnumerable<Flight>>  GetFlightsFromAirline2Async(this  string origin)
    {
        return Task.Run(()  =>
        {
            // Simulate asynchronous API call with Task.Delay
            Task.Delay(500).Wait();

// Fetch flights from Airline2 API (fake data for demonstration)
            return  new List<Flight>
            {
                new Flight { Airline =  "Airline2", Origin = origin, Destination =  "New York", DepartureDate = DateTime.Now.AddDays(3), Fare =  550  },
                new Flight { Airline =  "Airline2", Origin = origin, Destination =  "Los Angeles", DepartureDate = DateTime.Now.AddDays(4), Fare =  700  }
            }  as IEnumerable<Flight>;
        });
    }
}

Finally, let’s update the LINQ query in our Main() method to use the asynchronous extension methods and execute the query in parallel:

using System;
using System.Linq;
using System.Threading.Tasks;

class Program
{
    static async Task Main()
    {
        string origin =  "San Francisco";
        string destination =  "Los Angeles";

var airline1FlightsTask = origin.GetFlightsFromAirline1Async();
        var airline2FlightsTask = origin.GetFlightsFromAirline2Async();

var airline1Flights = await airline1FlightsTask;
        var airline2Flights = await airline2FlightsTask;

var bestFares = from airline1Flight in airline1Flights.AsParallel()
from airline2Flight in airline2Flights.AsParallel()
                        where airline1Flight.Destination  == destination && airline2Flight.Destination  == destination
let minFare = Math.Min(airline1Flight.Fare, airline2Flight.Fare)
                        orderby minFare
select new  { Airline =  (airline1Flight.Fare  <= airline2Flight.Fare)  ? airline1Flight.Airline  : airline2Flight.Airline, Fare = minFare };

Console.WriteLine($"Best flight fares from {origin} to {destination}:");
        foreach  (var fare in bestFares)
        {
            Console.WriteLine($"Airline:{fare.Airline}, Fare: ${fare.Fare}");
        }
    }
}

In this updated example, we’ve made our extension methods asynchronous and used Task.Run() to simulate API calls. In the Main() method, we’ve called these asynchronous methods and used AsParallel() to execute our LINQ query in parallel. This approach can help to improve performance when working with large data sets or complex operations.

## 6.3\. Common LINQ Operators

In this section, we’ll explore some common LINQ operators that you’ll frequently use in your functional programming journey with C#. These operators can be categorized into filtering, projection, aggregation, and ordering operations.

*   Filtering Operators These operators help you filter data based on specific conditions. Some common filtering operators are:

•           Where: Filters a sequence of elements based on a given predicate.

IEnumerable<int> numbers =  new[]  {  1,  2,  3,  4,  5,  6  };
IEnumerable<int> evenNumbers = numbers.Where(n => n %  2  ==  0);

•           OfType: Filters a sequence of elements based on their runtime type.

IEnumerable<object> objects =  new  object[]  {  "string",  42,  3.14  };
IEnumerable<int> integers = objects.OfType<int>();

*   Projection Operators These operators help you transform a sequence of elements. Some common projection operators are:

•           Select: Projects each element of a sequence into a new form.

IEnumerable<int> numbers =  new[]  {  1,  2,  3,  4,  5  };
IEnumerable<int> squaredNumbers = numbers.Select(n => n * n);

•           SelectMany: Projects each element of a sequence to an IEnumerable and flattens the resulting sequences into one sequence.

IEnumerable<string> words =  new[]  {  "Hello",  "World"  };
IEnumerable<char> characters = words.SelectMany(w => w);

*   Aggregation Operators These operators help you compute a single value from a sequence of elements. Some common aggregation operators are:

•           Count: Returns the number of elements in a sequence.

IEnumerable<int> numbers =  new[]  {  1,  2,  3,  4,  5  };
int count = numbers.Count();

•           Sum: Computes the sum of a sequence of numeric values.

IEnumerable<int> numbers =  new[]  {  1,  2,  3,  4,  5  };
int sum = numbers.Sum();

•           Average: Computes the average of a sequence of numeric values.

IEnumerable<int> numbers =  new[]  {  1,  2,  3,  4,  5  };
double average = numbers.Average();

•           Min and Max: Returns the minimum and maximum values in a sequence, respectively.

IEnumerable<int> numbers =  new[]  {  1,  2,  3,  4,  5  };
int minValue = numbers.Min();
int maxValue = numbers.Max();

*   Ordering Operators These operators help you sort a sequence of elements. Some common ordering operators are:

•           OrderBy and OrderByDescending: Sorts the elements of a sequence in ascending or descending order, respectively, according to a key.

IEnumerable<int> numbers =  new[]  {  5,  3,  1,  4,  2  };
IEnumerable<int> ascending = numbers.OrderBy(n => n);
IEnumerable<int> descending = numbers.OrderByDescending(n => n);

• ThenBy and ThenByDescending: Performs a subsequent ordering of the elements in a sequence in ascending or descending order, respectively, according to a key. It’s often used after the OrderBy or OrderByDescending method.

IEnumerable<string> words =  new[]  {  "apple",  "orange",  "banana",  "kiwi"  };
IEnumerable<string> sortedWords = words.OrderBy(w => w.Length).ThenBy(w => w);

These are just a few examples of the powerful LINQ operators available in C#. By combining these operators, you can perform complex data manipulation and transformations in a concise and readable manner.

*   Set Operators These operators help you perform set-based operations on sequences. Some common set operators are:

•           Distinct: Removes duplicate elements from a sequence.

IEnumerable<int> numbers =  new[]  {  1,  2,  2,  3,  3,  3,  4,  4,  4,  4,  5,  5,  5,  5,  5  };
IEnumerable<int> distinctNumbers = numbers.Distinct();

•            Union: Produces the set union of two sequences.

IEnumerable<int> first =  new[]  {  1,  2,  3,  4,  5  };
IEnumerable<int> second =  new[]  {  4,  5,  6,  7,  8  };
IEnumerable<int> union = first.Union(second);

•            Intersect: Produces the set intersection of two sequences.

IEnumerable<int> first =  new[]  {  1,  2,  3,  4,  5  };
IEnumerable<int> second =  new[]  {  4,  5,  6,  7,  8  };
IEnumerable<int> intersection = first.Intersect(second);

•            Except: Produces the set difference of two sequences.

IEnumerable<int> first =  new[]  {  1,  2,  3,  4,  5  };
IEnumerable<int> second =  new[]  {  4,  5,  6,  7,  8  };
IEnumerable<int> difference = first.Except(second);

*   Grouping Operators These operators help you group elements in a sequence based on a specified key. Some common grouping operators are:

•           GroupBy: Groups the elements of a sequence according to a specified key selector function.

IEnumerable<int> numbers =  new[]  {  1,  2,  3,  4,  5,  6,  7,  8,  9,  10  };
IEnumerable<IGrouping<int,  int>> groupedNumbers = numbers.GroupBy(n => n %  2);

By mastering these LINQ operators, you can harness the true power of functional programming in C#. With their help, you can build expressive, efficient, and easy-to-understand code that can tackle even the most challenging data processing tasks.

# Chapter 7: Error Handling and Functional Programming

In this chapter, we’ll explore how to handle errors in functional programming with C#. We’ll start by discussing the traditional error handling approach in C# and then move on to more functional alternatives using the Result and Either types. Finally, we’ll introduce railway-oriented programming, a powerful technique for composing functions with error handling.

## 7.1\. Traditional Error Handling in C#: Exceptions

In C#, the most common way to handle errors is by using exceptions. Exceptions are objects that represent errors or exceptional conditions that occur during program execution. When an error occurs, an exception is thrown, and the normal flow of the program is interrupted. To handle exceptions, you can use try-catch blocks, which allow you to define a block of code to be executed if an exception occurs.

Here’s an example of a function that uses exceptions for error handling:

int  Divide(int numerator,  int denominator)
{
    if  (denominator ==  0)
    {
        throw  new  DivideByZeroException("Cannot divide by zero.");
    }
    return numerator / denominator;
}

Although exceptions are widely used in C#, they have some drawbacks when it comes to functional programming:

•           Exceptions break the referential transparency of functions, making it harder to reason about code.

•           Throwing and catching exceptions can have a negative impact on performance.

•           Handling multiple exceptions can lead to complex, nested try-catch blocks.

## 7.2\. The Result and Either Types

As an alternative to exceptions, functional programming languages often use specialized types to represent errors, like Result and Either. These types can be used in C# to provide a more functional way of handling errors.

The Either type is a more general version of Result. It can represent one of two possible types, often used to represent a successful result or an error. In this section, we will use the Language-Ext library to demonstrate how to handle errors using the Either type. We will discuss the Language-Ext library in more detail in Chapter 10.

To install Language-Ext, add the NuGet package to your project:

Install-Package LanguageExt.Core

Let’s assume we have a Loan Application scenario where we need to fetch the applicant’s data from a MongoDB database. Using Language-Ext’s Either type, we can define a function that returns either a successful result (the applicant’s data) or an error.

First, let’s define an Applicant class:

public  class Applicant
{
 public ObjectId Id {  get;  set;  }
 public  string FullName {  get;  set;  }
 public  string Email {  get;  set;  }
 public  decimal LoanAmount {  get;  set;  }
}

Next, we will define an Error class:

public  class Error
{
 public  string Message {  get;  set;  }
}

Now, let’s create a function that fetches the applicant’s data from the MongoDB database. If an exception occurs, it will return an Error object. Otherwise, it will return the Applicant object.

using LanguageExt;
using MongoDB.Driver;

public async Task<Either<Error, Applicant>>  GetApplicantAsync(ObjectId id)
{
    try
    {
        var client =  new  MongoClient("mongodb://localhost:27017");
        var database = client.GetDatabase("LoanApp");
        var collection = database.GetCollection<Applicant>("Applicants");

var applicant = await collection.Find(app => app.Id  == id).FirstOrDefaultAsync();
        return applicant;
    }
    catch  (Exception ex)
    {
        return  new Error { Message = ex.Message  };
    }
}

With the GetApplicantAsync function, we can now create a Minimal API endpoint that fetches the applicant’s data and handles errors using the Either type:

using Microsoft.AspNetCore.Builder;
using Microsoft.Extensions.DependencyInjection;
using LanguageExt;

var builder = WebApplication.CreateBuilder(args);
builder.Services.AddControllers();
var app = builder.Build();

app.MapGet("/applicants/{id}",  async  (string id)  =>
{
ObjectId objectId = ObjectId.Parse(id);
    var result = await GetApplicantAsync(objectId);

return result.Match<IActionResult>(
        Right: applicant => Results.Ok(applicant),
        Left: error => Results.BadRequest(new  { error = error.Message  }));
});

app.Run();

In the above example, we use the Either type to handle errors in a functional way. Instead of throwing and catching exceptions, we return either a successful result or an error. This approach makes our code easier to reason about and allows us to handle errors in a more functional manner.

In addition to the Either type, there’s another common type used to represent errors in a functional way: the Result type. The Result type is similar to the Either type but is more specialized. It represents either a successful result or a failure. Let’s see how we can refactor our previous example using the Result type from Language-Ext.

First, let’s create a function that fetches the applicant’s data from the MongoDB database. If an exception occurs, it will return an Error object wrapped in a Result. Otherwise, it will return the Applicant object wrapped in a Result.

using LanguageExt;
using MongoDB.Driver;

public async Task<Result<Applicant, Error>>  GetApplicantAsync(ObjectId id)
{
    try
    {
        var client =  new  MongoClient("mongodb://localhost:27017");
        var database = client.GetDatabase("LoanApp");
        var collection = database.GetCollection<Applicant>("Applicants");

var applicant = await collection.Find(app => app.Id  == id).FirstOrDefaultAsync();
        return Result<Applicant, Error>.Success(applicant);
    }
    catch  (Exception ex)
    {
        return Result<Applicant, Error>.Failure(new Error { Message = ex.Message  });
    }
}

With the GetApplicantAsync function, we can now create a Minimal API endpoint that fetches the applicant’s data and handles errors using the Result type:

using Microsoft.AspNetCore.Builder;
using Microsoft.Extensions.DependencyInjection;
using LanguageExt;

var builder = WebApplication.CreateBuilder(args);
builder.Services.AddControllers();
var app = builder.Build();

app.MapGet("/applicants/{id}",  async  (string id)  =>
{
ObjectId objectId = ObjectId.Parse(id);
    var result = await GetApplicantAsync(objectId);

return result.Match<IActionResult>(
        Success: applicant => Results.Ok(applicant),
        Failure: error => Results.BadRequest(new  { error = error.Message  }));
});

app.Run();

In this example, we use the Result type to handle errors in a functional way. It is similar to the Either type but specifically tailored for success or failure scenarios. This approach makes our code easier to reason about and allows us to handle errors in a more functional manner.

## 7.3\. Railway-Oriented Programming

Railway-oriented programming (ROP) is a functional programming pattern that enables you to compose functions in a way that makes error handling more manageable and explicit. The concept is based on the idea of having two parallel “tracks” or “rails” that your code can travel on, one for the success case and the other for the failure case.

In ROP, functions are designed to return a Result or Either type, representing success or failure. These types can be composed and chained together, making it easy to propagate errors through a sequence of function calls without the need for exception handling.

Let’s consider an example of a loan application process at a bank. We will implement this process using railway-oriented programming principles.

First, let’s define our LoanApplication class:

public  class LoanApplication
{
 public Applicant Applicant {  get;  set;  }
 public  decimal LoanAmount {  get;  set;  }
 public  int LoanTermInMonths {  get;  set;  }
}

Next, we will create a few functions that represent the steps in the loan application process. Each function will return a Result type, indicating success or failure:

*   CheckCreditScore: This function checks the applicant’s credit score and returns a Result that indicates whether the credit score is within the acceptable range.

*   EvaluateDebtToIncomeRatio: This function evaluates the applicant’s debt-to-income ratio and returns a Result that indicates whether the ratio is within the acceptable range.

*   ApproveLoan: This function approves the loan based on the applicant’s credit score and debt-to-income ratio. Let’s implement these functions:

public Result<int, Error>  CheckCreditScore(Applicant applicant)
{
 // Simulate checking the credit score (e.g., by calling a credit bureau API)
 int creditScore =  new  Random().Next(300,  850);

if  (creditScore <  620)
    {
        return Result<int, Error>.Failure(new Error { Message =  "Credit score too low."  });
    }

return Result<int, Error>.Success(creditScore);
}

public Result<decimal, Error>  EvaluateDebtToIncomeRatio(Applicant applicant)
{
 // Simulate calculating the debt-to-income ratio
 decimal debtToIncomeRatio =  new  Random().Next(1,  100)  / 100m;

if  (debtToIncomeRatio >  0.43m)
    {
        return Result<decimal, Error>.Failure(new Error { Message =  "Debt-to-income ratio too high."  });
    }

return Result<decimal, Error>.Success(debtToIncomeRatio);
}

public Result<LoanApplication, Error>  ApproveLoan(Applicant applicant,  decimal loanAmount,  int loanTermInMonths)
{
 // Evaluate the applicant's credit score and debt-to-income ratio
 var creditScoreResult =  CheckCreditScore(applicant);
 var debtToIncomeRatioResult =  EvaluateDebtToIncomeRatio(applicant);

// If both evaluations are successful, approve the loan
    if  (creditScoreResult.IsSuccessful  && debtToIncomeRatioResult.IsSuccessful)
    {
        var loanApplication =  new LoanApplication
        {
Applicant = applicant,
LoanAmount = loanAmount,
LoanTermInMonths = loanTermInMonths
        };

return Result<LoanApplication, Error>.Success(loanApplication);
    }

// If either evaluation fails, return the corresponding error
    return creditScoreResult.Match<Result<LoanApplication, Error>>(
        Success: _ => Result<LoanApplication, Error>.Failure(debtToIncomeRatioResult.FailureValue),
        Failure: error => Result<LoanApplication, Error>.Failure(error));
}

Now that we have our functions implemented, let’s use railway-oriented programming principles to compose them together in a ProcessLoanApplication function:

public Result<LoanApplication, Error>  ProcessLoanApplication(Applicant applicant,  decimal loanAmount,  int loanTermInMonths)
{
    return  CheckCreditScore(applicant)
        .Bind(creditScore =>  EvaluateDebtToIncomeRatio(applicant)
        .Map(debtToIncomeRatio =>  ApproveLoan(applicant, loanAmount, loanTermInMonths)));
}

In the ProcessLoanApplication function, we first call CheckCreditScore and then use the Bind method to chain the result of EvaluateDebtToIncomeRatio. If both evaluations are successful, we then use the Map method to call ApproveLoan. If any step in the process fails, the error will be propagated through the chain and returned as the final result.

Let’s now create a sample function that simulates processing a loan application:

public  static async Task Main()
{
 var applicant =  new Applicant { Name =  "Alice", AnnualIncome = 80000m };
 decimal loanAmount = 250000m;
 int loanTermInMonths =  360;

var result =  ProcessLoanApplication(applicant, loanAmount, loanTermInMonths);

result.Match(
        Success: loanApplication => Console.WriteLine("Loan approved!"),
        Failure: error => Console.WriteLine($"Loan denied. Reason: {error.Message}")
    );
}

Let’s extend our loan processing pipeline by adding a few more steps to make the concept of railway-oriented programming even clearer. We will add the following new functions to our pipeline:

*   CheckEmploymentHistory: This function checks the applicant’s employment history and returns a Result that indicates whether they meet the minimum employment duration requirement.

*   VerifyIdentity: This function verifies the applicant’s identity and returns a Result that indicates whether the identity verification was successful.

*   EvaluateLoanRisk: This function evaluates the overall risk of the loan and returns a Result that indicates whether the risk is within the acceptable range.

Now let’s implement these functions:

public Result<bool, Error>  CheckEmploymentHistory(Applicant applicant)
{
 // Simulate checking the employment history (e.g., by calling an employment verification API)
 int employmentDurationInMonths =  new  Random().Next(0,  120);

if  (employmentDurationInMonths <  24)
    {
        return Result<bool, Error>.Failure(new Error { Message =  "Insufficient employment history."  });
    }

return Result<bool, Error>.Success(true);
}

public Result<bool, Error>  VerifyIdentity(Applicant applicant)
{
 // Simulate verifying the applicant's identity (e.g., by calling an identity verification API)
 bool identityVerified =  new  Random().Next(0,  2)  ==  1;

if  (!identityVerified)
    {
        return Result<bool, Error>.Failure(new Error { Message =  "Identity verification failed."  });
    }

return Result<bool, Error>.Success(true);
}

public Result<bool, Error>  EvaluateLoanRisk(Applicant applicant,  decimal loanAmount,  int loanTermInMonths)
{
 // Simulate evaluating the loan risk (e.g., by using a machine learning model)
 bool isAcceptableRisk =  new  Random().Next(0,  2)  ==  1;

if  (!isAcceptableRisk)
    {
        return Result<bool, Error>.Failure(new Error { Message =  "Loan risk too high."  });
    }

return Result<bool, Error>.Success(true);
}

Now, let’s update our ProcessLoanApplication function to include these new steps in the pipeline:

public Result<LoanApplication, Error>  ProcessLoanApplication(Applicant applicant,  decimal loanAmount,  int loanTermInMonths)
{
    return  CheckCreditScore(applicant)
        .Bind(creditScore =>  EvaluateDebtToIncomeRatio(applicant)
        .Bind(debtToIncomeRatio =>  CheckEmploymentHistory(applicant)
        .Bind(employmentHistory =>  VerifyIdentity(applicant)
        .Bind(identityVerified =>  EvaluateLoanRisk(applicant, loanAmount, loanTermInMonths)
        .Map(risk =>  ApproveLoan(applicant, loanAmount, loanTermInMonths))))));
}

In the updated ProcessLoanApplication function, we have extended the pipeline to include CheckEmploymentHistory, VerifyIdentity, and EvaluateLoanRisk functions using the Bind method. If any step in the process fails, the error will be propagated through the chain and returned as the final result.

By extending our pipeline, we have demonstrated how railway-oriented programming can be used to elegantly compose multiple functions with error handling. This approach makes the code more maintainable, easier to understand, and consistent with the principles of functional programming.

# Chapter 8: Asynchronous Programming in a Functional Style

## 8.1\. Async/Await and Task-Based Asynchronous Pattern

In the world of programming, there’s no escaping the need to deal with asynchronous operations, especially when working with I/O-bound tasks like file operations, web requests, or database calls. C# has come a long way in providing tools to manage asynchrony, making it more accessible and manageable. In this chapter, we’ll explore asynchronous programming in C# from a functional programming perspective.

The Task-Based Asynchronous Pattern (TAP) is at the core of C#’s asynchronous programming model. It relies on the Task and Task classes to represent ongoing work that produces a result or simply completes without returning a value.

Let’s start by looking at a simple example of using async/await and TAP to perform an asynchronous operation:

public async Task<string>  FetchDataFromWebAsync()
{
    using  (var httpClient =  new  HttpClient())
    {
        var response = await httpClient.GetAsync("https://api.example.com/data");
        var content = await response.Content.ReadAsStringAsync();
        return content;
    }
}

In this example, we’re fetching data from a web API using HttpClient. The async keyword is used to indicate that the method contains asynchronous code. The await keyword is used to pause the execution of the method until the asynchronous operation represented by the Task is completed. The method returns a Task which represents the ongoing operation that will eventually return a string value.

Now, let’s explore how to apply functional programming concepts to asynchronous programming in C#. One approach is to use monads, specifically the Task monad. Just like Option and Either, the Task monad can be used to chain and compose asynchronous operations in a functional manner.

For example, let’s rewrite the FetchDataFromWebAsync method using the Task monad and functional style:

public Task<string>  FetchDataFromWebFuncAsync()
{
    return  new  HttpClient().GetAsync("https://api.example.com/data")
        .Bind(response => response.Content.ReadAsStringAsync());
}

In this version, we’re using the Bind method to chain the GetAsync and ReadAsStringAsync calls. The Bind method can be thought of as the async equivalent of SelectMany in LINQ. It allows us to compose multiple asynchronous operations in a functional style. The method still returns a Task representing the ongoing operation.

Notice that we no longer need the async and await keywords, as the Bind method handles the asynchrony behind the scenes. This is an example of how functional programming can help us write cleaner and more maintainable code while still taking advantage of the powerful asynchronous features of C#.

## 8.2\. Asynchronous Functional Pipelines

In the previous section, we looked at how to write asynchronous code in a functional style using the Task monad and the Bind method. Now, let’s extend this concept to build asynchronous functional pipelines using LINQ query syntax.

To begin, we’ll create a few extension methods for Task that will allow us to use LINQ query syntax with asynchronous operations:

public  static  class TaskExtensions
{
    public  static async Task<TResult> Select<TSource, TResult>(this Task<TSource> task, Func<TSource, TResult> selector)
    {
        var source = await task.ConfigureAwait(false);
        return  selector(source);
    }

public  static async Task<TResult> SelectMany<TSource, TResult>(this Task<TSource> task, Func<TSource, Task<TResult>> selector)
    {
        var source = await task.ConfigureAwait(false);
        return await selector(source).ConfigureAwait(false);
    }

public  static async Task<TResult> SelectMany<TSource, TCollection, TResult>(this Task<TSource> task, Func<TSource, Task<TCollection>> collectionSelector, Func<TSource, TCollection, TResult> resultSelector)
    {
        var source = await task.ConfigureAwait(false);
        var collection = await collectionSelector(source).ConfigureAwait(false);
        return  resultSelector(source, collection);
    }
}

These extension methods (Select, SelectMany, and the overload of SelectMany with a result selector) enable us to use LINQ query syntax with Task. Now, let’s create a complex bank-related example using these extensions.

Suppose we have a banking system that needs to fetch customer data, account data, and recent transactions asynchronously. We’ll use the following classes to represent our data:

public  class Customer
{
 public  int Id {  get;  set;  }
 public  string Name {  get;  set;  }
}

public  class Account
{
 public  int Id {  get;  set;  }
 public  decimal Balance {  get;  set;  }
}

public  class Transaction
{
 public  int Id {  get;  set;  }
 public  decimal Amount {  get;  set;  }
 public DateTime Date {  get;  set;  }
}

Now, let’s create methods that simulate fetching this data asynchronously:

public async Task<Customer>  GetCustomerAsync(int customerId)
{
 // Simulate fetching customer data asynchronously
    await Task.Delay(100);
 return  new Customer { Id = customerId, Name =  "John Doe"  };
}

public async Task<Account>  GetAccountAsync(int accountId)
{
 // Simulate fetching account data asynchronously
    await Task.Delay(100);
 return  new Account { Id = accountId, Balance =  5000  };
}

public async Task<List<Transaction>>  GetRecentTransactionsAsync(int accountId)
{
    // Simulate fetching recent transactions asynchronously
    await Task.Delay(100);
    return  new List<Transaction>
    {
        new Transaction { Id =  1, Amount =  -100, Date = DateTime.UtcNow.AddDays(-1)  },
        new Transaction { Id =  2, Amount =  200, Date = DateTime.UtcNow.AddDays(-2)  },
        new Transaction { Id =  3, Amount =  -50, Date = DateTime.UtcNow.AddDays(-3)  }
    };
}

Now, let’s build an asynchronous functional pipeline using our Task extension methods and LINQ query syntax:

public async Task<(Customer, Account, List<Transaction>)>  FetchCustomerAccountDataAsync(int customerId,  int accountId)
{
    var result =  await  (from customer in  GetCustomerAsync(customerId)
from account in  GetAccountAsync(accountId)
from transactions in  GetRecentTransactionsAsync(accountId)
                        select  (customer, account, transactions));

return result;
}

In the FetchCustomerAccountDataAsync method, we combined the fetching of customer data, account data, and recent transactions using LINQ query syntax with our Task extension methods. This allows us to create an asynchronous functional pipeline, which is both readable and maintainable.

Now, let’s create another example using our pipeline. This time, we’ll filter the recent transactions to display only the transactions that exceed a certain threshold.

public async Task<(Customer, Account, List<Transaction>)>  FetchFilteredCustomerAccountDataAsync(int customerId,  int accountId,  decimal threshold)
{
    var result =  await  (from customer in  GetCustomerAsync(customerId)
from account in  GetAccountAsync(accountId)
from transactions in  GetRecentTransactionsAsync(accountId)
let filteredTransactions = transactions.Where(t => Math.Abs(t.Amount)  > threshold).ToList()
                        select  (customer, account, filteredTransactions));

return result;
}

In this method, we added a new step in the LINQ query that filters the transactions before returning the result. The let keyword allows us to introduce a new filteredTransactions variable, which holds the filtered transaction list. The Where function is used to filter the transactions based on the given threshold.

Now that we’ve seen how to build asynchronous functional pipelines using LINQ query syntax and Task extension methods, let’s explore how to handle errors in these pipelines. In the functional programming world, the Result type (also known as the Either monad) is commonly used to represent the result of a computation that may fail.

To integrate the Result type in our pipeline, let’s create a Task<Result> class that represents an asynchronous computation that may fail:

public  class TaskResult<T>
{
 public Task<Result<T>> Value {  get;  }

public  TaskResult(Task<Result<T>> value)
    {
Value = value;
    }

}

Now, we can create extension methods for the TaskResult class similar to our Task extension methods. This will allow us to create asynchronous functional pipelines that handle errors in a functional way.

public  static  class TaskResultExtensions
{
    public  static async TaskResult<TResult> Select<TSource, TResult>(this TaskResult<TSource> taskResult, Func<TSource, TResult> selector)
    {
        var result = await taskResult.Value.ConfigureAwait(false);
        return result.IsSuccess
            ?  new TaskResult<TResult>(Task.FromResult(new Result<TResult>(selector(result.Value))))
            :  new TaskResult<TResult>(Task.FromResult(new Result<TResult>(result.ErrorMessage)));
    }

public  static async TaskResult<TResult> SelectMany<TSource, TResult>(this TaskResult<TSource> taskResult, Func<TSource, TaskResult<TResult>> selector)
    {
        var result = await taskResult.Value.ConfigureAwait(false);
        return result.IsSuccess
            ?  selector(result.Value)
            :  new TaskResult<TResult>(Task.FromResult(new Result<TResult>(result.ErrorMessage)));
    }

public  static async TaskResult<TResult> SelectMany<TSource, TCollection, TResult>(this TaskResult<TSource> taskResult, Func<TSource, TaskResult<TCollection>> collectionSelector, Func<TSource, TCollection, TResult> resultSelector)
    {
        var result = await taskResult.Value.ConfigureAwait(false);
         if  (result.IsSuccess)
        {
            var source = result.Value;
            var collectionResult = await collectionSelector(source).Value.ConfigureAwait(false);
            return collectionResult.IsSuccess
                ?  new TaskResult<TResult>(Task.FromResult(new Result<TResult>(resultSelector(source, collectionResult.Value))))
                :  new TaskResult<TResult>(Task.FromResult(new Result<TResult>(collectionResult.ErrorMessage)));
        }
        else
        {
            return  new TaskResult<TResult>(Task.FromResult(new Result<TResult>(result.ErrorMessage)));
        }
    }
}

Now that we have the TaskResultExtensions, let’s create a new example that uses these extension methods to build an asynchronous functional pipeline with error handling.

public async Task<Result<(Customer, Account, List<Transaction>)>>  FetchCustomerAccountDataAsync(int customerId,  int accountId)
{
    var result =  await  (from customerResult in  GetCustomerAsync(customerId)
from accountResult in  GetAccountAsync(accountId)
from transactionsResult in  GetRecentTransactionsAsync(accountId)
                        select  (customerResult, accountResult, transactionsResult));

return result.IsSuccess
        ?  new Result<(Customer, Account, List<Transaction>)>((result.Value.Item1, result.Value.Item2, result.Value.Item3))
        :  new Result<(Customer, Account, List<Transaction>)>(result.ErrorMessage);
}

In this example, we build an asynchronous functional pipeline that fetches customer data, account data, and recent transactions using LINQ query syntax with TaskResult and the TaskResultExtensions. If an error occurs in any of the operations, the pipeline returns a Result<(Customer, Account, List)> with the error message. Otherwise, it returns a successful result with the fetched data.

The TaskResultExtensions enable us to create asynchronous functional pipelines that handle errors in a functional way, making the code more readable and maintainable. It promotes the separation of concerns, as each method in the pipeline is responsible for its error handling, and makes it easier to deal with different types of errors that may occur during asynchronous operations.

In conclusion, building asynchronous functional pipelines using LINQ query syntax and Task extension methods allows for more concise, readable, and maintainable code. It also promotes the separation of concerns and makes it easier to handle errors in a functional way. By extending this approach to handle the Result type, we can create robust and efficient asynchronous pipelines in C#.

## 8.3 Handling Errors Asynchronously

In this section, we will explore handling errors asynchronously in functional C#. Asynchronous programming is an essential aspect of modern software development, allowing us to perform non-blocking I/O operations while freeing up resources. In functional programming, we typically handle errors using monadic structures like Either, Option, or Result.

To facilitate this, we will use the Functional-Ext library, which provides several useful utilities and extensions to make functional programming with C# more convenient. The library will be explained in more detail in Chapter 10.

### 8.3.1 Asynchronous Error Handling with Result

Result is a monadic structure that represents the outcome of a computation that may result in a success or an error. It can hold either a successful value or an error. In asynchronous programming, we can use Result combined with Task to handle errors in an async/await-friendly way.

Consider the following example, where we have a function that might throw an exception:

async Task<string>  LoadDataAsync(string url)
{
 // Load data from the URL and return the result as a string
}

To handle errors in a functional way, we can wrap the return type in a Result:

using Functional;
using System.Threading.Tasks;

async Task<Result<string, Exception>>  LoadDataResultAsync(string url)
{
    try
    {
        var data = await LoadDataAsync(url);
        return Result.Ok<string, Exception>(data);
    }
    catch  (Exception ex)
    {
        return Result.Error<string, Exception>(ex);
    }
}

Now, we can consume the function and handle both success and error cases:

async Task MainAsync()
{
 var result = await LoadDataResultAsync("https://example.com/data");

result.Match(
        ok: data => Console.WriteLine($"Data: {data}"),
        error: ex => Console.WriteLine($"Error: {ex.Message}")
    );
}

### 8.3.2 Composing Asynchronous Functions

One of the main benefits of using Result in asynchronous programming is that we can easily compose multiple functions together, even if they may fail. The Functional-Ext library provides various extensions, such as BindAsync, to help achieve this.

Suppose we have two functions, LoadDataResultAsync and ProcessDataResultAsync:

async Task<Result<string, Exception>>  LoadDataResultAsync(string url)  {  /* ... */  }

async Task<Result<int, Exception>>  ProcessDataResultAsync(string data)  {  /* ... */  }

We can compose these functions using BindAsync:

async Task MainAsync()
{
    var url =  "https://example.com/data";

var result = await LoadDataResultAsync(url)
        .BindAsync(data =>  ProcessDataResultAsync(data));

result.Match(
        ok: processedData => Console.WriteLine($"Processed data: {processedData}"),
        error: ex => Console.WriteLine($"Error: {ex.Message}")
    );
}

In this example, BindAsync composes the functions and short-circuits the error. If LoadDataResultAsync returns an error, the ProcessDataResultAsync function is not called, and the error is propagated to the Match function.

## 8.3.3 Error Handling with Parallelism

The Functional-Ext library also provides facilities to handle errors while performing parallel operations. For example, let’s consider a case where we need to download data from multiple URLs in parallel and process them. The library offers the Traverse extension method to achieve this purpose.

Suppose we have a list of URLs to load data from and process:

using Functional;
using System.Threading.Tasks;

async Task MainAsync()
{
    List<string> urls =  new List<string>
    {
        "https://example.com/data1",
        "https://example.com/data2",
        "https://example.com/data3",
    };

var result = await urls.Traverse(async url => await LoadDataResultAsync(url)
        .BindAsync(data =>  ProcessDataResultAsync(data)));

result.Match(
        ok: processedDataList =>
        {
            Console.WriteLine("Processed data:");
            foreach  (var processedData in processedDataList)
            {
                Console.WriteLine(processedData);
            }
        },
        error: ex => Console.WriteLine($"Error: {ex.Message}")
    );
}

In this example, Traverse applies the given asynchronous function to each element of the urls list in parallel, and then combines the results into a single Result. If any of the operations fail, the Result will hold the first error encountered, and the success case will contain a list of the processed data.

## 8.3.4 Retrying Asynchronous Operations

In some situations, you might want to retry an asynchronous operation if it fails. The Functional-Ext library provides a convenient RetryAsync extension method for this purpose. Here’s an example that demonstrates how to use RetryAsync with our LoadDataResultAsync function:

async Task MainAsync()
{
    var url =  "https://example.com/data";
    int maxRetries =  3;

var result = await LoadDataResultAsync(url)
        .RetryAsync(maxRetries,  async  (url, retryCount)  =>
        {
            Console.WriteLine($"Retrying {retryCount + 1}/{maxRetries}...");
            await Task.Delay(1000);  // Wait for 1 second before retrying
        });

result.Match(
        ok: data => Console.WriteLine($"Data: {data}"),
        error: ex => Console.WriteLine($"Error: {ex.Message}")
    );
}

In this example, the RetryAsync extension method is used to retry the LoadDataResultAsync operation if it fails, up to a maximum of maxRetries times. If the operation continues to fail after all retries, the error will be propagated to the Match function.

In this section, we covered asynchronous error handling in functional C# using the Result monadic structure and the Functional-Ext library. We discussed how to handle errors in a functional way, compose asynchronous functions, perform parallel operations with error handling, and retry asynchronous operations on failure.

Using these concepts and techniques will help you build robust and maintainable error handling strategies in your functional C# applications, enabling you to handle both success and failure cases in a consistent and composable manner.

# Chapter 9: Functional Design Patterns

In this chapter, we will explore functional design patterns commonly used in functional programming. These design patterns help you write cleaner, more reusable, and maintainable code by taking advantage of functional programming concepts.

## 9.1 Functor, Applicative, and Monad

In functional programming, Functor, Applicative, and Monad are design patterns that deal with effectful computations. They help us compose functions that produce values inside a computational context, such as error handling, asynchronous operations, or computations that may have side effects. Let’s discuss each of these patterns in detail and implement them from scratch in C# using various examples.

Functor A Functor is a design pattern that involves using a generic data type that has a map operation. Functors allow you to apply a function to a value inside a computational context without having to explicitly manage the context. In C#, you can think of IEnumerable and Task as examples of functors. The Select method of LINQ is an example of a map operation.

Let’s create a simple Maybe type and implement the map operation as an extension method:

public  abstract  class Maybe<T>
{
 public  static Maybe<T>  None()  =>  new None<T>();
 public  static Maybe<T>  Some(T value)  =>  new Some<T>(value);
}

public  class None<T>  : Maybe<T>  {  }

public  class Some<T>  : Maybe<T>
{
 public T Value {  get;  }

public  Some(T value)
    {
Value = value;
    }
}

public  static  class MaybeExtensions
{
    public  static Maybe<TResult> Map<TSource, TResult>(
        this Maybe<TSource> maybe,
        Func<TSource, TResult> selector)
    {
        return maybe switch
        {
            Some<TSource> some => Maybe<TResult>.Some(selector(some.Value)),
_ => Maybe<TResult>.None(),
        };
    }
}

Now, let’s implement the map operation for the IEnumerable type:

public  static  class EnumerableExtensions
{
    public  static IEnumerable<TResult> Map<TSource, TResult>(
        this IEnumerable<TSource> source,
        Func<TSource, TResult> selector)
    {
        return source.Select(selector);
    }
}

And for the Task type:

public  static  class TaskExtensions
{
    public  static async Task<TResult> Map<TSource, TResult>(
        this Task<TSource> task,
        Func<TSource, TResult> selector)
    {
        return  selector(await task);
    }
}

Applicative An Applicative extends the Functor concept by allowing you to apply a function wrapped in a computational context to a value inside the same context. In C#, we can create an Applicative using the same Maybe type as before and implement an Apply extension method:

public  static  class MaybeExtensions
{
    // ...

public  static Maybe<TResult> Apply<TSource, TResult>(
        this Maybe<Func<TSource, TResult>> maybeFunc,
        Maybe<TSource> maybeValue)
    {
        return maybeFunc switch
        {
            Some<Func<TSource, TResult>> someFunc =>
                maybeValue.Map(value => someFunc.Value(value)),
_ => Maybe<TResult>.None(),
        };
    }
}

Now, let’s implement the Apply operation for the IEnumerable type:

public  static  class EnumerableExtensions
{
    // ...

public  static IEnumerable<TResult> Apply<TSource, TResult>(
        this IEnumerable<Func<TSource, TResult>> sourceFuncs,
        IEnumerable<TSource> sourceValues)
    {
        return from func in sourceFuncs
from value in sourceValues
select func(value);
    }
}

And for the Task type:

public  static async Task<TResult> Apply<TSource, TResult>(
    this Task<Func<TSource, TResult>> taskFunc,
    Task<TSource> taskValue)
{
    var func = await taskFunc;
    var value = await taskValue;
    return  func(value);
}

Monad A Monad is a design pattern that generalizes the concept of chaining operations together. Monads allow you to flatten nested computational contexts and perform actions sequentially. A monad must provide a bind operation (also known as flatMap or SelectMany in C#).

Let’s implement the bind operation for our Maybe type:

public  static  class MaybeExtensions
{
    // ...

public  static Maybe<TResult> Bind<TSource, TResult>(
        this Maybe<TSource> maybe,
        Func<TSource, Maybe<TResult>> selector)
    {
        return maybe switch
        {
            Some<TSource> some =>  selector(some.Value),
_ => Maybe<TResult>.None(),
        };
    }
}

Now, let’s implement the bind operation for the IEnumerable type:

public  static  class EnumerableExtensions
{
    // ...

public  static IEnumerable<TResult> Bind<TSource, TResult>(
        this IEnumerable<TSource> source,
        Func<TSource, IEnumerable<TResult>> selector)
    {
        return source.SelectMany(selector);
    }
}

And for the Task type:

public  static async Task<TResult> Bind<TSource, TResult>(
    this Task<TSource> task,
    Func<TSource, Task<TResult>> selector)
{
    return await selector(await task);
}

Now we have seen how to implement Functor, Applicative, and Monad for three different computational contexts: Maybe, IEnumerable, and Task. With these concepts, you can create more reusable and composable code in a functional programming style.

# Chapter 10: Usage and Examples

Now that we’ve implemented Functor, Applicative, and Monad for Maybe, IEnumerable, and Task, let’s look at how we can use these patterns in real-life examples.

## 10.1 Maybe Example

Imagine we have a list of user IDs and a function to find a user’s email by their ID. However, the function may return None if the user is not found. We can use the Maybe monad to chain multiple operations.

public  class User
{
 public  int Id {  get;  set;  }
 public  string Email {  get;  set;  }
}

public Maybe<User>  FindUserById(int id)
{
    // Find a user by ID (could be from a database, for example)
    // Here, we're simulating the lookup with a hardcoded list
    var users =  new List<User>
    {
        new User { Id =  1, Email =  "john@example.com"  },
        new User { Id =  2, Email =  "jane@example.com"  },
    };

return users.FirstOrDefault(user => user.Id  == id).ToMaybe();
}

public Maybe<string>  GetUserEmail(int userId)
{
 return  FindUserById(userId).Map(user => user.Email);
}

var userIds =  new List<int>  {  1,  2,  3,  4  };
var emails = userIds.Map(GetUserEmail);

## 10.2 IEnumerable Example

Suppose we have a list of customers and a list of orders, and we want to find all the orders placed by a specific group of customers. We can use the IEnumerable monad to achieve this.

public  class Customer
{
 public  int Id {  get;  set;  }
 public  string Name {  get;  set;  }
}

public  class Order
{
 public  int Id {  get;  set;  }
 public  int CustomerId {  get;  set;  }
 public  double Total {  get;  set;  }
}

public IEnumerable<Order>  GetOrdersForCustomers(
    IEnumerable<Customer> customers,
    IEnumerable<Order> orders)
{
    return customers.Bind(customer =>
        orders.Where(order => order.CustomerId  == customer.Id));
}

var customers =  new List<Customer>
{
 new Customer { Id =  1, Name =  "John"  },
 new Customer { Id =  2, Name =  "Jane"  },
};

var orders =  new List<Order>
{
 new Order { Id =  101, CustomerId =  1, Total =  100.0  },
 new Order { Id =  102, CustomerId =  1, Total =  200.0  },
 new Order { Id =  103, CustomerId =  2, Total =  300.0  },
 new Order { Id =  104, CustomerId =  3, Total =  400.0  },
};

var customerOrders =  GetOrdersForCustomers(customers, orders);

Task Example Consider an application that makes multiple API calls to different services, and we want to process the results sequentially. We can use the Task monad to achieve this.

public async Task<string>  FetchDataFromApi(string url)
{
    // Simulating an API call with Task.Delay
    await Task.Delay(1000);
    return $"Data from {url}";
}

public async Task<string>  ProcessData(string data)
{
    // Simulating data processing with Task.Delay
    await Task.Delay(500);
    return $"Processed {data}";
}

public async Task<string>  FetchAndProcessDataAsync(string url)
{
return await FetchDataFromApi(url).Bind(ProcessData);
}

public async Task ExecuteExample()
{
    var urls =  new List<string>  {  "https://api1.example.com",  "https://api2.example.com"  };
    foreach  (var url in urls)
    {
        var result = await FetchAndProcessDataAsync(url);
        Console.WriteLine(result);
    }
}

await ExecuteExample();

In this example, we use the Task<T> monad to chain asynchronous calls and process the results sequentially. This makes the code cleaner and more manageable while preserving the sequential nature of the operations.

In conclusion, understanding and implementing Functor, Applicative, and Monad design patterns can lead to cleaner, more reusable, and more maintainable code in a functional programming style. By leveraging these patterns with different computational contexts such as Maybe<T>, IEnumerable<T>, and Task<T>, you can create composable and versatile code that can handle a wide range of scenarios.

## 10.3 Extension Methods for Task Monad

In this section, we’ll extend the Task monad with some additional extension methods to handle retries and recover from errors. The methods we will implement are OrElse, Recover, Bind, and Map.

Let’s start by creating a new TaskExtensions class that contains the extension methods:

public  static  class TaskExtensions
{
    public  static async Task<TResult> OrElse<TSource, TResult>(
        this Task<TSource> task,
        Func<Task<TResult>> fallback)
where TSource : TResult
    {
        try
        {
            return await task;
        }
        catch
        {
            return await fallback();
        }
    }

public  static async Task<T> Recover<T>(
        this Task<T> task,
        Func<Exception, T> recoverFunc)
    {
        try
        {
            return await task;
        }
        catch  (Exception ex)
        {
            return  recoverFunc(ex);
        }
    }

public  static async Task<TResult> Bind<TSource, TResult>(
        this Task<TSource> task,
        Func<TSource, Task<TResult>> selector)
    {
        return await selector(await task);
    }

public  static async Task<TResult> Map<TSource, TResult>(
        this Task<TSource> task,
        Func<TSource, TResult> selector)
    {
        return  selector(await task);
    }
}

Now, let’s explain each method:

• OrElse: If the task fails, it will execute the fallback function provided, returning a new task. It’s useful for implementing retries or providing an alternative result when an operation fails.

• Recover: If the task fails, it will execute the recoverFunc function, which receives the exception and returns a default value. It’s useful for recovering from errors and providing default values when an operation fails.

•           Bind and Map: These methods were previously explained in the earlier sections as fundamental operations for the Task monad.

Now let’s create some examples demonstrating the usage of these extension methods.

public async Task<string>  FetchDataFromApiWithErrors(string url)
{
    // Simulating an API call that sometimes throws an exception
    if  (url.Contains("error"))
    {
        throw  new  InvalidOperationException("Error fetching data.");
    }

await Task.Delay(1000);
    return $"Data from {url}";
}

public async Task ExecuteExampleWithExtensions()
{
    var urls =  new List<string>
    {
        "https://api1.example.com",
        "https://api2.example.com/error",
        "https://api3.example.com",
    };

foreach  (var url in urls)
    {
        var dataTask =  FetchDataFromApiWithErrors(url);
        var recoveredDataTask = dataTask.Recover(ex => $"Recovered data for {url}");
        var processedDataTask = recoveredDataTask.Map(data => $"Processed {data}");

var result = await processedDataTask;
        Console.WriteLine(result);
    }
}

await ExecuteExampleWithExtensions();

In this example, we use the Recover and Map methods to handle errors and process the data from the API calls. This results in more resilient and cleaner code, taking advantage of the extension methods provided for the Task monad.

## Use Case 1: Stock Data API

Imagine we have an application that fetches stock data from an API. There are two API providers, one primary and one secondary. If the primary API fails, the application should fall back to the secondary API. Additionally, if both APIs fail, we should return a default stock value.

First, let’s create a Stock class and functions for fetching stock data:

public  class Stock
{
 public  string Symbol {  get;  set;  }
 public  double Price {  get;  set;  }
}

public async Task<Stock>  FetchStockFromPrimaryApi(string symbol)
{
    // Simulate an API call with possible failures
    if  (symbol ==  "FAIL")
    {
        throw  new  InvalidOperationException("Primary API failed.");
    }

await Task.Delay(1000);
    return  new Stock { Symbol = symbol, Price =  100.0  };
}

public async Task<Stock>  FetchStockFromSecondaryApi(string symbol)
{
    // Simulate an API call with possible failures
    if  (symbol ==  "FAIL")
    {
        throw  new  InvalidOperationException("Secondary API failed.");
    }

await Task.Delay(1000);
    return  new Stock { Symbol = symbol, Price =  200.0  };
}

public Stock DefaultStock(string symbol)
{
 return  new Stock { Symbol = symbol, Price =  0.0  };
}

Now let’s use the OrElse and Recover methods to create a fault-tolerant function to fetch stock data:

public async Task<Stock>  FetchStockDataAsync(string symbol)
{
    return await FetchStockFromPrimaryApi(symbol)
        .OrElse(()  =>  FetchStockFromSecondaryApi(symbol))
        .Recover(ex =>  DefaultStock(symbol));
}

public async Task ExecuteStockDataExample()
{
 var symbols =  new List<string>  {  "AAPL",  "MSFT",  "FAIL"  };

foreach  (var symbol in symbols)
    {
        var stock = await FetchStockDataAsync(symbol);
        Console.WriteLine($"Symbol: {stock.Symbol}, Price: {stock.Price}");
    }
}

await ExecuteStockDataExample();

Use Case 2: Geocoding and Weather API Suppose we have an application that fetches location coordinates (latitude and longitude) for a given address using a geocoding API and then fetches weather data using a weather API. The application should handle possible API failures and provide default data when necessary.

First, let’s create Location and Weather classes and functions for fetching data from the APIs:

public  class Location
{
 public  string Address {  get;  set;  }
 public  double Latitude {  get;  set;  }
 public  double Longitude {  get;  set;  }
}

public  class Weather
{
 public  string Description {  get;  set;  }
 public  double Temperature {  get;  set;  }
}

public async Task<Location>  FetchLocationAsync(string address)
{
    // Simulate an API call with possible failures
    if  (address ==  "FAIL")
    {
        throw  new  InvalidOperationException("Geocoding API failed.");
    }

await Task.Delay(1000);
 return  new Location { Address = address, Latitude =  40.7128, Longitude =  -74.0060  };
}

public async Task<Weather>  FetchWeatherAsync(double latitude,  double longitude)
{
    // Simulate an API call with possible failures
    if  (latitude ==  0.0  && longitude ==  0.0)
    {
        throw  new  InvalidOperationException("Weather API failed.");
    }

await Task.Delay(1000);
    return  new Weather { Description =  "Sunny", Temperature =  25.0  };
}

public Location DefaultLocation(string address)
{
 return  new Location { Address = address, Latitude =  0.0, Longitude =  0.0  };
}

public Weather DefaultWeather()
{
 return  new Weather { Description =  "Unknown", Temperature =  0.0  };
}

Now let’s use the Bind, Map, OrElse, and Recover methods to create a fault-tolerant function to fetch weather data for a given address:

public async Task<Weather>  FetchWeatherForAddressAsync(string address)
{
    return await FetchLocationAsync(address)
        .Recover(ex =>  DefaultLocation(address))
        .Bind(location =>  FetchWeatherAsync(location.Latitude, location.Longitude))
        .Recover(ex =>  DefaultWeather());
}

public async Task ExecuteWeatherExample()
{
 var addresses =  new List<string>  {  "123 Main St",  "456 Broadway",  "FAIL"  };

foreach  (var address in addresses)
    {
        var weather = await FetchWeatherForAddressAsync(address);
        Console.WriteLine($"Address: {address}, Weather: {weather.Description}, Temperature: {weather.Temperature}");
    }
}

await ExecuteWeatherExample();

In these examples, we used the Map, OrElse, Bind, and Recover methods to handle failures and provide fault tolerance in real-world scenarios involving API calls. By combining these methods, we can create applications that gracefully handle errors and provide fallback data when necessary.

In this section, we explored the Functor, Applicative, and Monad design patterns and their applications in functional programming with C#. We’ve implemented custom extension methods for the Task monad, such as Map, OrElse, Bind, and Recover, to improve error handling and resilience in real-world scenarios.

We demonstrated the power of these patterns through various examples, including stock data fetching, geocoding, and weather information retrieval. These examples showed how to handle errors gracefully, provide fallback data, and maintain the readability and maintainability of the code.

By understanding and implementing these functional design patterns in your projects, you can build more robust, composable, and resilient applications that can handle various computational contexts and scenarios.

In the next chapters, we will continue our journey in functional programming with C#, covering additional topics and concepts to further improve your programming skills and understanding of functional programming principles.

Monoids and Semigroups

In this section, we will explore Monoids and Semigroups, which are fundamental algebraic structures in functional programming. These structures allow you to model and compose operations in a simple and consistent manner. We will start by introducing the concept of Semigroups and then move on to Monoids, providing examples and explaining their practical applications in functional programming with C#.

## 10.4 Semigroups

A Semigroup is an algebraic structure that consists of a set of values and an associative binary operation. The binary operation must satisfy the following rules:

Closure: The result of the binary operation must be a member of the set. Associativity: For all elements a, b, and c in the set, (a _ b) _ c = a _ (b _ c). To better understand Semigroups, let’s implement a simple example in C#. We will create a Sum Semigroup to represent the addition of integers:

public  class SumSemigroup
{
 public  int Value {  get;  }

public  SumSemigroup(int value)
    {
Value = value;
    }

public SumSemigroup Combine(SumSemigroup other)
    {
        return  new  SumSemigroup(Value + other.Value);
    }
}

The SumSemigroup represents integers and has a Combine method that adds two SumSemigroup instances together, producing a new SumSemigroup. The Combine method is associative, which means it satisfies the requirements of a Semigroup.

Let’s create a simple example using the SumSemigroup:

var a =  new  SumSemigroup(1);
var b =  new  SumSemigroup(2);
var c =  new  SumSemigroup(3);

var result1 = a.Combine(b).Combine(c);  // (1 + 2) + 3
var result2 = a.Combine(b.Combine(c));  // 1 + (2 + 3)

Console.WriteLine($"Result1: {result1.Value}, Result2: {result2.Value}");  // Result1: 6, Result2: 6

The example demonstrates the associativity property of the Combine method in the SumSemigroup.

## 10.5 Monoids

A Monoid is an extension of a Semigroup, with the addition of an identity element. The identity element is a value that, when combined with any other element using the binary operation, results in the same element. In other words, for any element a in the set, a _ identity = identity _ a = a.

To create a Monoid in C#, we can inherit from the SumSemigroup class and add an identity element:

public  class SumMonoid : SumSemigroup
{
 public  SumMonoid(int value)  :  base(value)  {  }

public  static SumMonoid Identity =>  new  SumMonoid(0);
}

In this example, the identity element is 0, which means that when we combine any SumMonoid instance with the identity element, the result will be the original value:

var a =  new  SumMonoid(1);
var identity = SumMonoid.Identity;

var result1 = a.Combine(identity);
var result2 = identity.Combine(a);

Console.WriteLine($"Result1: {result1.Value}, Result2: {result2.Value}");  // Result1: 1, Result2: 1

Monoids and Semigroups provide a consistent and composable way to model operations in functional programming. They can be used to represent various data tructures and operations, such as string concatenation, list merging, or other domain-specific requirements.

## 10.6 Practical Applications

Now let’s take a look at some practical applications of Monoids and Semigroups in C#.

## 10.7 String Concatenation Monoid

A classic example of a Monoid is the concatenation of strings. The binary operation is the string concatenation, and the identity element is the empty string ““. Let’s create a StringMonoid class:

public  class StringMonoid
{
 public  string Value {  get;  }

public  StringMonoid(string value)
    {
Value = value;
    }

public StringMonoid Combine(StringMonoid other)
    {
        return  new  StringMonoid(Value + other.Value);
    }

public  static StringMonoid Identity =>  new  StringMonoid("");
}

And here’s a simple example of how to use the StringMonoid:

var a =  new  StringMonoid("Hello, ");
var b =  new  StringMonoid("World");
var identity = StringMonoid.Identity;

var result = a.Combine(b).Combine(identity);

Console.WriteLine($"Result: {result.Value}");  // Result: Hello, World

## 10.8 List Merging Monoid

Another useful example of a Monoid is the merging of lists. The binary operation is the list concatenation, and the identity element is the empty list. Let’s create a generic ListMonoid class:

public  class ListMonoid<T>
{
 public List<T> Value {  get;  }

public  ListMonoid(List<T> value)
    {
Value = value;
    }

public ListMonoid<T>  Combine(ListMonoid<T> other)
    {
        var result =  new List<T>(Value);
        result.AddRange(other.Value);
        return  new ListMonoid<T>(result);
    }

public  static ListMonoid<T> Identity =>  new ListMonoid<T>(new List<T>());
}

Here’s an example of how to use the ListMonoid to merge integer lists:

var a =  new ListMonoid<int>(new List<int>  {  1,  2,  3  });
var b =  new ListMonoid<int>(new List<int>  {  4,  5,  6  });
var identity = ListMonoid<int>.Identity;

var result = a.Combine(identity).Combine(b);

Console.WriteLine($"Result: {string.Join(",  ", result.Value)}");  // Result: 1, 2, 3, 4, 5, 6

In this section, we explored Monoids and Semigroups, which are essential algebraic structures in functional programming. We demonstrated how they can be used to represent different data structures and operations, such as integer addition, string concatenation, or list merging.

We provided practical examples and demonstrated how these structures enable simple, consistent, and composable ways to model operations in functional programming. Understanding and applying Monoids and Semigroups in your projects can lead to more maintainable and robust applications.

In the next sections, we will continue our journey in functional programming with C#, covering additional topics and concepts to further improve your programming skills and understanding of functional programming principles.

## 10.9 Free Monads

In this section, we will explore Free Monads, an advanced functional programming concept that enables building composable, flexible, and extensible programs. Free Monads separate program construction from program interpretation, making it possible to create versatile and reusable code.

Free Monads are based on the idea of algebraic effects, where you define a set of operations without specifying their implementation. This separation of concerns allows you to create reusable and composable programs that can be interpreted differently in different contexts.

### 10.9.1 Implementing a Free Monad in C

To implement a Free Monad in C#, we will use the Functor concept. Let’s create a simple example to demonstrate how to build and work with Free Monads. We will define a console-based program with the following operations: WriteLine and ReadLine.

### 10.9.1.1 Console Operations

First, we will define the abstract base class for console operations, which will implement the IFunctor interface:

public  abstract  class ConsoleOp<A>  : IFunctor<A>
{
 public  abstract IFunctor<TResult> Map<TResult>(Func<A, TResult> f);
}

Now, let’s define the specific implementations of WriteLine and ReadLine that represent writing to and reading from the console, respectively:

public  class WriteLine : ConsoleOp<Unit>
{
 public  string Message {  get;  }

public  WriteLine(string message)
    {
Message = message;
    }

public  override IFunctor<TResult> Map<TResult>(Func<Unit, TResult> f)
    {
        return  new  WriteLine(Message).Map(f);
    }
}

public  class ReadLine : ConsoleOp<string>
{
    public  override IFunctor<TResult> Map<TResult>(Func<string, TResult> f)
    {
        return  new  ReadLine().Map(f);
    }
}

### 10.9.1.2 Free Monad Data Structure

Next, we will define the Free data structure that represents a computation in a Free Monad. It is a recursive data structure that consists of two cases: Pure, which represents a pure value, and Suspend, which represents an effectful operation.

public  abstract  class Free<F, A> where F : IFunctor<A>
{
 public  static Free<F, A>  Pure(A value)  =>  new Pure<F, A>(value);
 public  static Free<F, A>  Suspend(F functor)  =>  new Suspend<F, A>(functor);

private  class Pure : Free<F, A>
    {
        public A Value {  get;  }

public  Pure(A value)
        {
Value = value;
        }
    }

private  class Suspend : Free<F, A>
    {
        public F Functor {  get;  }

public  Suspend(F functor)
        {
Functor = functor;
        }
    }
}

### 10.9.2 Building Programs with Free Monads

With the Free data structure and console operations defined, we can now build a simple console program using Free Monads.

### 10.9.2.1 Creating the Program

Let’s create a simple program that writes a message to the console, reads user input, and then writes the user’s input back to the console:

var program =
    Free<ConsoleOp<Unit>, Unit>.Suspend(new  WriteLine("Please enter your name:"))
        .Bind(_ => Free<ConsoleOp<string>,  string>.Suspend(new  ReadLine())
            .Bind(name => Free<ConsoleOp<Unit>, Unit>.Suspend(new  WriteLine($"Hello, {name}!"))));

Here, we have built a program that uses the WriteLine and ReadLine operations in a composable manner using Free Monads. The Bind function chains these operations together, making it easy to express complex program logic.

Interpreting Free Monads One of the key benefits of Free Monads is the separation of program construction and interpretation. We can define multiple interpreters for a single Free Monad program, allowing us to interpret the program differently in various contexts.

Creating an Interpreter An interpreter is a function that takes a Free Monad program and processes its operations according to the desired behavior. Let’s create an interpreter for our console program that executes the WriteLine and ReadLine operations:

public  static async Task<A> ConsoleInterpreter<F, A>(Free<F, A> program) where F : IFunctor<A>
{
    if  (program is Free<F, A>.Pure pure)
    {
        return pure.Value;
    }
    else  if  (program is Free<F, A>.Suspend suspend)
    {
        var functor = suspend.Functor;

if  (functor is WriteLine writeLine)
        {
            Console.WriteLine(writeLine.Message);
            return await ConsoleInterpreter(writeLine.Map(_ => program));
        }
        else  if  (functor is ReadLine)
        {
            var input = Console.ReadLine();
            return await ConsoleInterpreter(functor.Map(_ => input));
        }
        else
        {
            throw  new  NotSupportedException($"Unsupported functor: {functor.GetType().Name}");
        }
    }
    else
    {
        throw  new  NotSupportedException($"Unsupported program case: {program.GetType().Name}");
    }
}

Running the Interpreter Now that we have an interpreter for our console program, we can execute the program by passing it to the interpreter:

await ConsoleInterpreter(program);

This will run the console program, writing messages to and reading input from the console as defined by the interpreter.

In this section, we introduced Free Monads, a powerful functional programming concept that enables the construction of composable, flexible, and extensible programs. By separating program construction and interpretation, we can create reusable and adaptable programs that can be interpreted in various contexts.

We demonstrated how to define a Free Monad data structure, build a simple console program using Free Monads, and create an interpreter to execute the program.

Chapter 10: Functional Programming Libraries for C# Functional programming in C# has been gaining popularity over the years, and as a result, several libraries have emerged to support functional programming concepts and patterns in the language. In this chapter, we will discuss some of the most popular and widely-used functional programming libraries for C#. We’ll provide an overview of each library, explore their unique features, and examine how they can enhance your functional programming experience in C#.

10.1 Language-Ext: An Introduction Language-Ext is one of the most popular functional programming libraries for C#. It is designed to enhance the core C# language with additional functional programming features, aiming to make C# code more expressive, concise, and safe. The library is inspired by the Haskell programming language and offers a wide range of data types and functions that make it easier to write functional code in C#.

Some of the key features of Language-Ext include:

Persistent data types: Immutable and highly-efficient data structures, such as persistent lists, maps, and sets, which enable safe and performant functional programming. Algebraic data types: Support for sum types (also known as discriminated unions), which allow you to model complex data types and represent data with more precision. Monads and monad transformers: A comprehensive collection of monads and monad transformers, including Option, Either, Try, Task, and State, which help you manage side-effects, errors, and state in a functional way. Higher-order functions: A rich set of higher-order functions, such as Map, Bind, Fold, and Filter, which enable powerful and expressive data manipulation. Lenses and optics: Tools for working with immutable data structures, allowing you to manipulate deeply nested data without the need for excessive boilerplate. To get started with Language-Ext, you can install the

NuGet package:

Install-Package LanguageExt.Core

After installing the package, you can start using the library in your C# code by adding the appropriate using statements. For example, to use the Option monad, you can add:

using LanguageExt;
using  static LanguageExt.Prelude;

Let’s explore a simple example of using Language-Ext in a C# program. We’ll use the Option monad to represent a nullable value and demonstrate how to work with it using the Map and Match functions.

Option<string>  GetName(int id)
{
    if  (id ==  1)  return  Some("Alice");
    if  (id ==  2)  return  Some("Bob");
    return None;
}

var name =  GetName(1);

var upperName = name.Map(s => s.ToUpper());

var result = upperName.Match(
    Some: s => $"Name: {s}",
    None:  ()  =>  "Name not found"
);

Console.WriteLine(result);  // Output: "Name: ALICE"

In this example, we define a GetName function that returns an Option representing a nullable name. We then use the Map function to transform the name to uppercase and the Match function to handle both the Some and None cases.

As we continue through this chapter, we’ll explore more features and libraries that will help you leverage functional programming techniques in C#.

# Chapter 11: Using Monads with Language-Ext

Language-Ext provides a rich set of monads that can help you manage side-effects, errors, and state in a functional way. In this section, we’ll demonstrate the use of various monads available in Language-Ext with practical examples.

Note: We assume that you have already installed the Language-Ext NuGet package and added the appropriate using statements in your code.

## Option Monad

The Option monad represents a nullable value, allowing you to work with potentially missing data in a safe and functional manner.

Option<int>  Divide(int numerator,  int denominator)
{
 return denominator ==  0  ? None :  Some(numerator / denominator);
}

var result =  Divide(10,  2)
    .Map(x => x *  2)
    .Match(
        Some: x => $"Result: {x}",
        None:  ()  =>  "Cannot divide by zero"
    );

Console.WriteLine(result);  // Output: "Result: 10"

## Either Monad

The Either monad represents a value that can be one of two types, typically used for error handling where one type represents an error and the other represents a success.

Either<string,  int>  SafeDivide(int numerator,  int denominator)
{
 return denominator ==  0  ?  Left("Cannot divide by zero")  :  Right(numerator / denominator);
}

var result =  SafeDivide(10,  2)
    .Map(x => x *  2)
    .Match(
        Left: error => $"Error: {error}",
        Right: value => $"Result: {value}"
    );

Console.WriteLine(result);  // Output: "Result: 10"

## Try Monad

The Try monad is used for capturing and managing exceptions in a functional way.

Try<int>  ParseInt(string input)
{
    return  Try(()  =>  int.Parse(input));
}

var result =  ParseInt("42")
    .Map(x => x *  2)
    .Match(
        Fail: ex => $"Error: {ex.Message}",
        Succ: value => $"Result: {value}"
    );

Console.WriteLine(result);  // Output: "Result: 84"

## Task Monad

The Task monad represents asynchronous computations and can be used with Language-Ext to manage asynchronous operations in a functional way.

async Task<Option<string>>  GetNameAsync(int id)
{
    await Task.Delay(1000);
    return id ==  1  ?  Some("Alice")  : None;
}

var result = await GetNameAsync(1)
    .Map(name => name.ToUpper())
    .Match(
        Some: name => $"Name: {name}",
        None:  ()  =>  "Name not found"
    );

Console.WriteLine(result);  // Output: "Name: ALICE"

## State Monad

The State monad allows you to manage mutable state in a functional way.

using LanguageExt.ClassInstances;
using LanguageExt.TypeClasses;

State<Dictionary<string,  int>,  int>  IncrementCounter(string key)
{
    return state =>
    {
        if  (!state.ContainsKey(key))
        {
            state[key]  =  0;
        }
        state[key]++;
        return  (state, state[key]);
    };
}

var initialState =  new Dictionary<string,  int>();

var  (updatedState, counterValue)  =  IncrementCounter("A").Run(initialState).Value;

Console.WriteLine($"Counter value: {counterValue}");  // Output: "Counter value: 1"

In this section, we provided practical examples of using various monads available in Language-Ext, including Option, Either, Try, Task, and State. As you work with functional programming in C#, these monads can help you manage side-effects, errors, and state in a functional manner, leading to safer and more expressive code.

## 11.3\. Other Functional Libraries for C

In addition to Language-Ext, several other functional programming libraries are available for C#. In this section, we’ll briefly introduce some of these libraries and their features, which can further enrich your functional programming experience in C#.

### 11.3.1 FSharpx.Extras

FSharpx.Extras is a library that provides a collection of utility functions and types for both C# and F# developers. It aims to fill the gaps between the two languages and offer additional functional programming features that are not available in C# out of the box. Some of the features of FSharpx.Extras include:

*   Discriminated unions: A type that can represent a value that is one of a number of named cases.

*   Function composition: Tools for composing and manipulating functions, such as compose, curry, and uncurry.

*   Additional monads: Support for the Reader, Writer, and Cont monads.

*   Async extensions: Extensions for working with asynchronous computations using the Task type.

You can install FSharpx.Extras using the NuGet package manager:

Install-Package FSharpx.Extras

### 11.3.2 CSharpFunctionalExtensions

CSharpFunctionalExtensions is a library that focuses on providing a simple and lightweight set of functional programming tools for C#. It includes support for the Result monad for error handling and a set of extension methods for working with nullable types, collections, and other C# language constructs in a more functional manner.

You can install CSharpFunctionalExtensions using the NuGet package manager:

Install-Package CSharpFunctionalExtensions

### 10.3.3 FsCheck

FsCheck is a library for property-based testing, which is a testing technique inspired by the QuickCheck library for Haskell. Property-based testing allows you to express properties that your code should satisfy, and FsCheck will generate test cases to check whether those properties hold. This testing approach can lead to more comprehensive testing with less manual test case creation.

You can install FsCheck using the NuGet package manager:

Install-Package FsCheck

### 11.3.4 MoreLINQ

MoreLINQ is a library that extends the LINQ to Objects operators with additional functionality, providing more powerful and expressive ways to manipulate collections in a functional style. MoreLINQ includes methods for working with sequences, such as DistinctBy, Partition, TakeEvery, and Scan, among many others.

You can install MoreLINQ using the NuGet package manager:

Install-Package MoreLinq

## 11.4\. MoreLINQ: Practical Examples

In this section, we’ll explore practical examples of using MoreLINQ to perform more powerful and expressive operations on collections in a functional style.

Note: To follow the examples, make sure to install the MoreLINQ NuGet package and add the appropriate using statement in your code:

using MoreLinq;

### 11.4.1 DistinctBy

DistinctBy allows you to filter out duplicate elements in a collection based on a key selector function.

class Employee
{
 public  int Id {  get;  set;  }
 public  string Name {  get;  set;  }
}

var employees =  new List<Employee>
{
 new Employee { Id =  1, Name =  "Alice"  },
 new Employee { Id =  2, Name =  "Bob"  },
 new Employee { Id =  1, Name =  "Alice"  }
};

var distinctEmployees = employees.DistinctBy(e => e.Id).ToList();

foreach  (var employee in distinctEmployees)
{
    Console.WriteLine($"Employee Id: {employee.Id}, Name: {employee.Name}");
}
// Output:
// Employee Id: 1, Name: Alice
// Employee Id: 2, Name: Bob

### 11.4.2 Partition

Partition divides a collection into two separate collections based on a predicate function.

var numbers =  new[]  {  1,  2,  3,  4,  5,  6  };

var  (evens, odds)  = numbers.Partition(n => n %  2  ==  0);

Console.WriteLine($"Evens: {string.Join(",  ", evens)}");  // Output: "Evens: 2, 4, 6"
Console.WriteLine($"Odds: {string.Join(",  ", odds)}");  // Output: "Odds: 1, 3, 5"

### 11.4.3 TakeEvery

TakeEvery selects every N-th element from a collection.

var numbers = Enumerable.Range(1,  10);
var everyThirdNumber = numbers.TakeEvery(3);

Console.WriteLine($"Every third number: {string.Join(",  ", everyThirdNumber)}");  // Output: "Every third number: 3, 6, 9"

### 11.4.4 Scan

Scan performs a rolling aggregation on a collection, applying a function to each element and accumulating the results.

var numbers =  new[]  {  1,  2,  3,  4,  5  };
var runningTotals = numbers.Scan(0,  (total, x)  => total + x);

Console.WriteLine($"Running totals: {string.Join(",  ", runningTotals)}");  // Output: "Running totals: 1, 3, 6, 10, 15"

In this section, we briefly introduced several functional programming libraries for C# that complement and extend the core language features. By exploring and incorporating these libraries into your projects, you can further enhance your functional programming skills and take full advantage of the functional programming paradigm in C#.

# Chapter 12: Real-World Applications and Case Studies

## 12.1 Functional Programming in Web Development: A Sci-Fi-Inspired Adventure

In a galaxy not so far away, a group of functional programming pioneers embarked on a mission to boldly go where no developer has gone before. They sought to combine functional programming and event sourcing to create web applications that were more elegant, maintainable, and scalable. With C# as their programming language of choice, they set out to demonstrate the power of functional programming and event sourcing in modern web development.

### Language-Ext: The Warp Drive of Functional Programming

In the C# universe, Language-Ext is a powerful library that brings the best of functional programming to the world of .NET. By utilizing advanced features like immutable data structures, monads, and agents, developers can create expressive and safe web applications. For this journey, we’ll create a wallet API that allows users to add and remove galactic credits from their wallet using a functional approach, agents to avoid concurrency issues, and event sourcing for tracking changes.

### Event Sourcing: The Temporal Prime Directive

Event sourcing is an architectural pattern that represents the state of an application as a sequence of events. Instead of updating the state directly, changes are recorded as events, allowing the state to be recreated by replaying these events. This approach provides many benefits, such as improved scalability, simplified debugging, and a built-in audit trail. By integrating event sourcing into our wallet API, we’ll uphold the Temporal Prime Directive and ensure a proper history of our wallet balance changes.

### MongoDB: The Intergalactic Database

To store our events, we’ll use MongoDB, a popular and flexible NoSQL database. This will allow us to persist our events and recreate the state of our wallet whenever needed. First, let’s set up the MongoDB connection and create a collection to store our wallet events.

Install the MongoDB driver for C# by adding the following package:

dotnet add package MongoDB.Driver

Now, let’s set up our MongoDB connection and create a WalletEventRepository to handle saving and loading events.

using MongoDB.Driver;

public  class WalletEventRepository
{
    private  readonly IMongoCollection<WalletEvent> _walletEvents;

public  WalletEventRepository(string connectionString,  string databaseName,  string collectionName)
    {
        var client =  new  MongoClient(connectionString);
        var database = client.GetDatabase(databaseName);
_walletEvents = database.GetCollection<WalletEvent>(collectionName);
    }

public async Task SaveEventAsync(WalletEvent walletEvent)  =>
        await _walletEvents.InsertOneAsync(walletEvent);

public async Task<List<WalletEvent>>  GetAllEventsAsync()  =>
        await _walletEvents.Find(_ =>  true).ToListAsync();
}

### The Wallet Agent: A Trusty Tricorder with Event Sourcing

First, let’s create our wallet agent using the Actor class from Language-Ext. The agent will handle concurrency issues and ensure that only one operation is executed at a time. We’ll also integrate event sourcing into the wallet agent to track changes to the wallet balance and use our WalletEventRepository to store the events in MongoDB.

using LanguageExt;
using  static LanguageExt.Prelude;
using System.Collections.Immutable;

public  class WalletAgent
{
    private  readonly Actor<ImmutableList<WalletEvent>> agent;
    private  readonly WalletEventRepository eventRepository;

public  WalletAgent(WalletEventRepository eventRepository)
    {
        this.eventRepository  = eventRepository;
agent = Actor<ImmutableList<WalletEvent>>.Create(async  (events, msg)  => msg switch
        {
AddMoney addMoney =>
            {
                var newEvent =  new WalletEvent.Added(addMoneyAmount);
                await eventRepository.SaveEventAsync(newEvent);
                return events.Add(newEvent);
            },
RemoveMoney removeMoney =>
            {
            var newEvent =  new WalletEvent.Removed(removeMoney.Amount);
            await eventRepository.SaveEventAsync(newEvent);
            return events.Add(newEvent);
            },
_ => events
        }, ImmutableList<WalletEvent>.Empty);
    }
    public async Task<ImmutableList<WalletEvent>>  AddMoney(decimal amount)  =>
        await agent.Ask<ImmutableList<WalletEvent>>(new  AddMoney(amount));

public async Task<ImmutableList<WalletEvent>>  RemoveMoney(decimal amount)  =>
        await agent.Ask<ImmutableList<WalletEvent>>(new  RemoveMoney(amount));

public async Task<decimal>  GetBalance()
    {
        var events = await eventRepository.GetAllEventsAsync();
        return events.Aggregate(0m,  (balance, evt)  => evt switch
        {
            WalletEvent.Added added => balance + added.Amount,
            WalletEvent.Removed removed => balance - removed.Amount,
_ => balance
        });
    }
}

Now that we have our wallet agent with event sourcing capabilities and MongoDB integration, let’s define the messages and events it will handle:

public  abstract record WalletMessage;

public record AddMoney(decimal Amount)  : WalletMessage;

public record RemoveMoney(decimal Amount)  : WalletMessage;

public record GetBalance()  : WalletMessage;

public  abstract record WalletEvent;

public  static  class WalletEvent
{
 public record Added(decimal Amount)  : WalletEvent;

public record Removed(decimal Amount)  : WalletEvent;
}

### The Functional Wallet API: Engaging Warp Speed with Event Sourcing and MongoDB

With our wallet agent, event sourcing, and MongoDB in place, it’s time to create the functional wallet API using minimal hosting in ASP.NET Core. This will allow us to harness the power of functional programming, event sourcing, and MongoDB in a concise and expressive manner.

using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Http;
using Microsoft.Extensions.DependencyInjection;

var builder = WebApplication.CreateBuilder(args);
builder.Services.AddSingleton<WalletEventRepository>(new  WalletEventRepository("mongodb://localhost:27017",  "wallet",  "events"));
builder.Services.AddSingleton<WalletAgent>();
var app = builder.Build();

app.MapPost("/api/wallet/add",  async  (WalletAgent walletAgent,  decimal amount)  =>
{
    var newEvents = await walletAgent.AddMoney(amount);
    return Results.Ok(newEvents);
});

app.MapPost("/api/wallet/remove",  async  (WalletAgent walletAgent,  decimal amount)  =>
{
    var newEvents = await walletAgent.RemoveMoney(amount);
    return Results.Ok(newEvents);
});

app.MapGet("/api/wallet/balance",  async  (WalletAgent walletAgent)  =>
{
    var balance = await walletAgent.GetBalance();
    return Results.Ok(balance);
});

app.Run();

In this example, we’ve combined functional programming techniques with minimal hosting, event sourcing, and MongoDB to create a modern and expressive web application. By using event sourcing and functional programming principles, our wallet API can be easily maintained and scaled as needed.

### Boldly Going Forward

As we conclude our sci-fi-inspired adventure into the world of functional web development, remember that functional programming is not just a set of tools or techniques, but a mindset that can help us write more robust, maintainable, and elegant code. So, engage your warp drive, explore the vast universe of functional programming in C#, and let the stars be your guide on this exciting journey.

### 11.2\. Data Processing and Analysis with Functional Programming

In this section, we will explore how functional programming techniques can be applied to data processing and analysis tasks in C#. We’ll be using Language-Ext and the MongoDB C# driver to create a simple data processing pipeline that demonstrates the benefits of functional programming in this context.

Before we begin, ensure that you have installed the necessary NuGet packages:

Install-Package LanguageExt.Core
Install-Package MongoDB.Driver

In this example, we will work with a simple data model representing a collection of products:

public  class Product
{
 public ObjectId Id {  get;  set;  }
 public  string Name {  get;  set;  }
 public  decimal Price {  get;  set;  }
 public  string Category {  get;  set;  }
}

Let’s assume we have a MongoDB collection containing product data, and we want to perform the following tasks:

*   Retrieve all products from the database.
*   Filter products by a specific category.
*   Calculate the average price of the filtered products.

We’ll begin by establishing a connection to the MongoDB database and retrieving the product data:

using MongoDB.Bson;
using MongoDB.Driver;

IMongoClient client =  new  MongoClient("mongodb://localhost:27017");
IMongoDatabase database = client.GetDatabase("test");
IMongoCollection<Product> collection = database.GetCollection<Product>("products");

List<Product> products = await collection.Find(_ =>  true).ToListAsync();

With the product data in hand, we can now use Language-Ext and functional programming techniques to create our data processing pipeline:

using LanguageExt;
using  static LanguageExt.Prelude;

decimal  AveragePrice(IEnumerable<Product> products)
{
 return products.Any()  ? products.Average(p => p.Price)  : 0m;
}

Option<decimal>  CalculateAveragePriceByCategory(IEnumerable<Product> products,  string category)
{
    return products
        .Where(p => p.Category  == category)
        .ToOption()
        .Filter(ps => ps.Any())
        .Map(AveragePrice);
}

var averagePrice =  CalculateAveragePriceByCategory(products,  "Electronics")
    .Match(
        Some: price => $"Average price: {price}",
        None:  ()  =>  "No products found in the specified category"
    );

Console.WriteLine(averagePrice);

In this example, we define a CalculateAveragePriceByCategory function that filters the products by the given category and computes the average price using the AveragePrice helper function. We use Language-Ext’s Option monad to represent the possibility of having no products in the specified category, which allows us to handle the scenario in a safe and functional manner.

Continuing with our data processing and analysis example, we’ll now introduce agents to handle concurrency. Agents are a functional programming pattern for managing shared mutable state in a safe and controlled manner. They can help us avoid race conditions and deadlocks while working with concurrent data processing tasks.

To demonstrate the use of agents in a data processing pipeline, we will use Language-Ext’s Agent type, and we’ll expose the functionality using the .NET 7 minimal API. First, let’s install the necessary NuGet package for the minimal API:

Install-Package Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore

Now, we’ll create an agent that receives requests to calculate the average price by category and processes them concurrently:

using LanguageExt;
using  static LanguageExt.Prelude;

record AveragePriceRequest(string Category, IObserver<decimal?> Response);

Agent<AveragePriceRequest>  CreateAveragePriceAgent(IEnumerable<Product> products)
{
    return Agent.Start<AveragePriceRequest>(async request =>
    {
        var averagePrice =  CalculateAveragePriceByCategory(products, request.Category);
        await request.Response.OnNextAsync(averagePrice.ToNullable());
    });
}

In this example, we define a CreateAveragePriceAgent function that takes an IEnumerable<Product> and returns an agent that can process AveragePriceRequest messages. Each AveragePriceRequest contains the category and an observer that receives the average price result. The agent will process incoming requests concurrently, allowing us to handle multiple requests without blocking or introducing synchronization issues.

Now, let’s create a minimal API that exposes this functionality:

using Microsoft.AspNetCore.Builder;
using Microsoft.Extensions.DependencyInjection;

var builder = WebApplication.CreateBuilder(args);
var app = builder.Build();

app.UseRouting();

var products = await FetchProductsAsync();  // Assume this function fetches products from the database
var averagePriceAgent =  CreateAveragePriceAgent(products);

app.MapGet("/api/average-price/{category}",  async  (string category, IObserver<decimal?> response)  =>
{
    var request =  new  AveragePriceRequest(category, response);
    averagePriceAgent.Tell(request);
    await Task.CompletedTask;
});

app.UseEndpoints(endpoints => endpoints.MapControllers());

await app.RunAsync();

In this example, we create a minimal API with a single GET endpoint that calculates the average price by category using the averagePriceAgent. The agent processes incoming requests concurrently, ensuring that the API remains responsive even under heavy load.

Using agents in the previous example brings several benefits, especially when dealing with concurrent data processing tasks. Some of the main advantages of using agents include:

*   Safe management of shared mutable state: Agents encapsulate the shared state and allow safe access and modification. They process messages sequentially and provide exclusive access to the state, which eliminates race conditions and synchronization issues without the need for locks or complex concurrency mechanisms.

*   Asynchronous processing: Agents run in the background and process incoming requests concurrently. This means that they can handle multiple requests simultaneously without blocking the main execution thread. As a result, the application remains responsive even when processing a large number of requests or performing computationally-intensive tasks.

*   Simplification of error handling and recovery: Agents provide a clean and consistent way to handle errors and recover from failures. By isolating the error handling logic within the agent, the application can continue to process incoming requests while ensuring that the state remains consistent and error-free.

*   Scalability and performance: Agents can help improve the overall performance and scalability of an application by processing requests concurrently and distributing the workload across multiple cores or processors. This allows the application to take full advantage of modern hardware and efficiently process large amounts of data.

*   Functional and declarative programming: Agents align well with the principles of functional and declarative programming. They encourage the use of immutable data structures and promote a clean separation between state management and computation. This leads to more maintainable, testable, and understandable code.

By combining functional programming techniques, agents, and Language-Ext, we can create an efficient and safe data processing pipeline that is easily exposed via a minimal API. This demonstrates the power of functional programming patterns and their practical applications in real-world scenarios.

### Bibliography