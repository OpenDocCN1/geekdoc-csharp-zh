![](Image00013.jpg)

![](image/794613.jpg)

CodeWiz RDZ               EZEE Programming

and
R.M.Z.

present:

Design Patterns,

The Easy Way,

w/ C#

Standard Solutions

for Everyday Programming Problems

Design Patterns Series

© Copyright 2015 - All rights reserved.

In no way is it legal to reproduce, duplicate, or transmit any part of this document in either electronic means or in printed format. Recording of this publication is strictly prohibited and any storage of this document is not allowed unless with written permission from the publisher. All rights reserved.

The information provided herein is stated to be truthful and consistent, in that any liability, in terms of inattention or otherwise, by any usage or abuse of any policies, processes, or directions contained within is the solitary and utter responsibility of the recipient reader. Under no circumstances will any legal responsibility or blame be held against the publisher for any reparation, damages, or monetary loss due to the information herein, either directly or indirectly.

Respective authors own all copyrights not held by the publisher.

Legal Notice:

This ebook is copyright protected. This is only for personal use. You cannot amend, distribute, sell, use, quote or paraphrase any part or the content within this ebook without the consent of the author or copyright owner. Legal action will be pursued if this is breached.

Disclaimer Notice:

Please note the information contained within this document is for educational and entertainment purposes only. Every attempt has been made to provide accurate, up to date and reliable complete information. No warranties of any kind are expressed or implied. Readers acknowledge that the author is not engaging in the rendering of legal, financial, medical or professional advice.

By reading this document, the reader agrees that under no circumstances are we responsible for any losses, direct or indirect, which are incurred as a result of the use of information contained within this document, including, but not limited to ,— errors, omissions, or inaccuracies.

The latest info on Web App Development! 

========================= ======

Follow us!

              @CodeWizRDZ

| ![](Image00000.jpg) | ![](Image00001.jpg) | ![](Image00002.jpg) |
| [Facebook](https://www.facebook.com/CodeWIzRDZ/) | [Instagram](https://www.instagram.com/codewizrdz) | [Twitter](https://www.twitter.com/codewizrdz) |

FOLLOW EZEE PROGRAMMING!

========================= ======

              @EzeeProgramming

| ![](Image00000.jpg) | ![](Image00001.jpg) | ![](Image00002.jpg) |
| [Facebook](https://www.facebook.com/EzeeProgramming) | [Instagram](https://www.instagram.com/ezeeprogramming) | [Twitter](https://www.twitter.com/ezeeprogramming) |

Table of Contents

C# Introduction

C#-00: A Quick Important note about C# code

Chapter 1: The Factory Pattern

C#-1a: The Factory Pattern, in C#

C#-1b: Implementing the Factory Pattern

C#-WORKSHOP 1:

Chapter 2: The Composite Pattern

C#-2a: The Composite Pattern, in C#

C#-2b: Implementing the Composite Pattern

C#-WORKSHOP 2:

Chapter 3: The Observer Pattern

C#-3a: The Observer Pattern, in C#

C#-3b: Implementing the Observer Pattern

Chapter 4: The Singleton Pattern

C#-4a: The Singleton Pattern, in C#

C#-4b: Implementing the Singleton Pattern

Chapter 5: The Strategy Pattern

C#-5a: The Strategy Pattern, in C#

C#-5b: Applying The Strategy Pattern (Simple)

Chapter 6: The Decorator Pattern

C#-6a: The Decorator Pattern, in C#

C#-6b: Applying The Decorator Pattern

Chapter 7: The State Pattern

C#-7a: The State Pattern, in C#

C#-7b: Applying The State Pattern

Chapter 8: The Facade Pattern

C#-8a: The Facade Pattern, in C#

C#-8b: Applying The Facade Pattern

Archive A1: Factory Pattern Implementation

Archive A2: Composite Pattern Implementation

Archive A3: Observer Pattern Implementation

Archive A4: Singleton Pattern Implementation

Archive A5: Strategy Pattern Implementation

Archive A6: Decorator Pattern Implementation

Archive A7: State Pattern Implementation

Archive A8: Facade Pattern Implementation

EASIEST WAY TO LEARN C#, Part 1

EASIEST WAY TO LEARN C#, Part 2

EASIEST WAY TO LEARN OBJECT-ORIENTED

THANK YOU!

C# Introduction

========================= ======

C# (pronounced C-sharp) is a programming language specifically developed for Microsoft software development. Much like the major programming languages, a lot of C# code, features, and other capabilities is based the C programming language. One of the key improvements C# has over C is, perhaps one of the most prominently used and important programming paradigms today, object-oriented programming.

And object-oriented programmers will encounter many repeating challenges during software development. What’s important to know is that these challenges have been encountered - and solved - before.

What if you know you have to create some File-Folder relationship within your program? What if you have a component in your program that consistently needs to update itself based on certain events or changes? What if you and your colleague both need to adapt to each other’s older code?

At some point, you’ll notice the patterns: a certain situation will usually require a certain programming solution. These solutions happen to be certain patterns in code (no matter the language)  that apply to certain situations you encounter.

Thus, Design Patterns are created.

What’s important to know is how to promptly and effortlessly implement these patterns - and this book will show you how. Even if you’re just starting out in C# programming, you’ll find great use of all the techniques you’ll find here.

C# Workshops:

Throughout the book, you’ll encounter workshops that will help you apply the various design patterns by putting them to good use. As you do them, think about the situations that require them to be used.

Then, throughout your own coding projects, think carefully about your designs and ask yourself which situations would have a certain design pattern come in handy.

We’ve designed this book to be very hands-on - giving you plenty of chances to use the material.

This is surely NOT a spectator’s book. If you would like to apply a new set of programming designs, then read on.

========================= ======

C#-00: A Quick Important note about C# code

A C# File

Before we get started, be sure to familiarize yourself with the structure of a C# class file, shown below between the dashed lines.

using System;

using System.Collections.Generic;

using System.Linq;

using System.Text.RegularExpressions;

// ADD MORE LIBRARIES HERE

namespace ___ {

              // ADD CLASSES HERE

    public class Program {

        public static void Main(string[] args) {

           // ADD MAIN CODE HERE

        }

    }

}     

    }

}

Chapter 1: The Factory Pattern

==== ==== ==== ==== ====

Are you not sure about which data object to create at a given time?

When creating a data object, are there a lot of complex aspects to keep in mind?

Then you need to use the Factory Method.

How it essentially works:

Depending on the programming language you use, you create a class interface that standardizes the data object creation. However, you would use subclasses (which extend or implement your higher “factory” interface) to actually create the data objects. The subclasses allow for a whole range of flexibility in creating data objects. If your programming language doesn’t have interfaces or abstract classes, simply create your ‘factory’ interface as a class, then have subclasses extend it.

For example, consider having to make a wide range of sports ball data objects, such as basketballs, soccer balls, footballs, volleyballs, etc.. You wouldn’t know what to create at a particular time. So how would you code this? Create an interface that outlines object construction for balls.

Let’s call it interface ‘BallMaker’. Then, for each type of ball we have, create a subclass extending ‘BallMaker’. These subclasses are the ones actually creating the ball data objects - but each of them has their own specifications. So a BasketBallMaker subclass would make basketballs and a FootballMaker subclass would make footballs.

So here’s what the UML diagram would look like:

![](Image00003.jpg)

The Pseudocode implementation for this pattern is also included in the Archive. If you need to implement this pattern in another language,  the pseudocode should help you.

Next, we’ll be using the Factory Pattern.

C#-1a: The Factory Pattern, in C#

==== ==== ==== ==== ====

Here is how the Factory Pattern looks like in C#:

// Factory is implemented by any subclasses that need to use it

    interface Factory {                     

        // INPUT: your choice

            // OUTPUT: your choice (set to Void by default)

        // Constructor for Classes that implement this interface

        void createObject();

    }    

    // SubFactory1:

    // creates distinct objects based on Factory Interface

    class SubFactory1 : Factory {

        // This implements the same function outlined in the interface

         void Factory .createObject() {             

        // include ANY unique distinctions for this creator class

        // any other code here

        }

    }

    // SubFactory2:

    // creates distinct objects based on Factory Interface

    class SubFactory2 : Factory {

        // This implements the same function outlined in the interface

         void Factory.createObject() {             

        // include ANY unique distinctions for this creator class

        // any other code here

        }

    } 

In the next chapter, we’ll do a walkthrough in implementing this design pattern.

C#-1b: Implementing the Factory Pattern

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

Now we’ll see the factory pattern in action. You’ll see first-hand how to use this design pattern through an example, plus a workshop in which you continue with the example.

Sports Ball Creator

Imagine that you had to write code for a build-to-order web app. It specializes in creating sports balls of many different kinds.

Here is what a general ball class would look like:

/*

// A Sports Ball has:

// - the Type of ball it is

// - an array of materials used to manufacture it

// - its size, as a radius (inches)

// - any additional comments required

// - the company brand that made it

// - a product name

*/

class SportsBall {                           

       public String type;

       public String[] materialsUsed;

       public float radius;

       public String comments;

       public String make;

       public String modelName;

}

However, as you can see, there are far too many small details involved when creating data objects for sports balls. So if you had to create, let’s say, a certain basketball, the process would be far more different compared to creating a soccer ball. They both would have different types, materials, and size. They also would probably be created by different brands and would have different features too.

So how would we have sports balls created in a much easier way? And with much less code involved?

You guessed it. The Factory Pattern!

So in this tutorial chapter, let’s go through the steps in setting up the design pattern.

Then, you’ll have a chance to practice what you’ve learned by extending the work.

Step 1: The Factory Interface

First, we’ll create the Interface that all the ball-creating Factory classes will implement.

For now, it will only have one method: creating & returning instances of sports balls.

// the BallFactory interface:

// - interface for how a ball will be created

interface BallFactory {

    /*

    // INPUT: none

    // OUTPUT: a Sports Ball object

    // EFFECT: Creates a Sports Ball;

    // Classes that implement this will have their own distinctions in making one

    */

    SportsBall createBall();

}

Step 2: The First Factory Class

Next, we create a distinct factory class that implements the BallFactory interface we made. For now, all it does is create basketballs. These may be instances of SportsBall objects, but they’ll have the certain characteristics of a basketball.

// The Basketball Maker:

// - creates basketball objects with distinct fields

class BasketballMaker : BallFactory {

    // (method implements the Interface Version)

    // EFFECT: Creates a sports ball as a Basketball

    SportsBall BallFactory.createBall() {

        SportsBall b = new SportsBall();

        b.type = "Basketball";

        b.materialsUsed = new String[3];

        b.materialsUsed[0] = "rubber";

        b.materialsUsed[1] = "fiber";

        b.materialsUsed[2] = "synthetic composite";

        b.radius = 4.8f;

        b.make = "Spalding";

        b.modelName = "Series Basketball";

        return b;

    }   

}

Step 3: Design any additional Factory Classes you need

Afterwards, we create as much distinct factory classes as we need. They all implement the BallFactory interface and they all create sports ball objects with distinct features and characteristics.

Let’s do this by designing a Factory class that creates baseballs.

// The Baseball Maker:

// - creates baseball objects with distinct fields

class BaseballMaker : BallFactory {

    // (method implements the Interface Version)

    // EFFECT: Creates a sports ball as a Basketball

    SportsBall BallFactory.createBall() {

        SportsBall b = new SportsBall();

        b.type = "Baseball";

        b.materialsUsed = new String[6];

        b.materialsUsed[0] = "cork";

        b.materialsUsed[1] = "wool";

        b.materialsUsed[2] = "poly/cotton";

        b.materialsUsed[3] = "cowhide";

        b.materialsUsed[4] = "yarn";

        b.materialsUsed[5] = "composite rubber";

        b.radius = 1.45f;

        b.make = "Rawlings";

        b.modelName = "MLB Official Baseball";       

        return b;

    }   

}

Step 4: Run some Code

Now that you’ve designed the factory classes, it’s time to run them.

On your Main function (the main class that has the public-static-void-main method), or whichever way you want to run your code, create an instance for each factory class you’ve designed. You’ll be calling on these factories to create particular objects for you.

In our example, we’ve created basketball and baseball factories. We’ll be using these to create basketball and baseball objects, respectively.

// Creating the Factories

        BallFactory f1 = new BasketballMaker();

        BallFactory f2 = new BaseballMaker();

        // Creating a basketball object:

        // Use the Basketball Factory to make Basketballs

        SportsBall bb1 = f1.createBall();

        // Creating a baseball object:

        // Use the Baseball Factory to make Baseballs

        SportsBall bb2 = f2.createBall();

        // TESTING:

        // This line should print out "Basketball"                

        Console.WriteLine(bb1.type);

        // This line should print out "Baseball" 

        Console.WriteLine(bb2.type);

C#-WORKSHOP 1:

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

And now it’s your turn to play with the Factory Pattern.

Soccer & Volleyballs

Show what you’ve learned by creating two more factory classes.

One of them will create soccer balls and the other will create volleyballs.

Afterwards, write and run a few lines of code that create instances of each factory and at least one ball from each factory.

Here’s some code to help you get started:

// The Soccerball Maker:

// - creates soccer ball objects with distinct fields

class SoccerballMaker : BallFactory {

    // (method implements the Interface Version)

    // EFFECT: Creates a sports ball as a Soccerball

    SportsBall BallFactory.createBall() {

              SportsBall b = new SportsBall();

              // modify the object fields;

              // they should all resemble what and how a soccer ball is like..

              return b;

              }

}

// The Volleyball Maker:

// - creates volleyball objects with distinct fields

class VolleyballMaker : BallFactory {

    // (method implements the Interface Version)

    // EFFECT: Creates a sports ball as a volleyball

    public SportsBall createBall() {

              SportsBall b = new SportsBall();

              // modify the object fields;

              // they should all resemble what and how a volleyball is like..

              return b;

              }

}

Advanced Coding:

Notice how all the sports balls are still one type of object - sports balls.

How would you change the code so that each of the factory classes create objects of balls they’re supposed to create? For example, how would you have the BasketballMaker create Basketball objects instead of general, modified Sports Balls? Or a BaseballMaker creating Baseball objects?

Chapter 2: The Composite Pattern

==== ==== ==== ==== ====

Picture this scenario: you have to organize your data in a hierarchal manner. They seem to somehow resemble ‘files’ and ‘folders’.

As you and other computer users know, files go into folders and folders can go into other folders as well.

You also want to do this in a way that doesn’t replicate unnecessary code.

So what do you need?

The Composite Pattern.

How it essentially works:

You have two distinct classes: a File class and a Folder class. Or Item and Group. Clothing and Bag. Toys and Box. Any combination of two classes, in which one of them is a collection composed of both types.

However, both classes may have way too many similar traits, methods, and fields. You realize you may need to write twice the code that you would normally do - one for the items and one for the groupings.

The solution here is to have them extend a common superclass or abstract class - a component. This includes one key distinction; the Group class contains a collection of this superclass. And because both classes extend a common superclass, the Group class can have a collection of either items or groups.

For example, let’s say you have two classes: Clothing and Bag. A Bag can contain both clothes and other bags. They both share similar characteristics such as name, description, etc.. You realize how unproductive it is to write separate code when it really should be under the same code (i.e. when getting all the names would need calls from both Clothing.getName() and Bag.getName()).

Therefore, you apply the Composite Pattern. Both Clothing and Bag classes extend a new superclass, Item. The Bag class is modified to have a collection of Items (which can be either Bags or Clothing).

Here’s what the UML diagram would look like:

![](Image00004.jpg)

The main thing to remember here are the item/container classes extend a common superclass - component. The container class will have a list containing components, which can be either files or folders.

Depending on the language you’re coding with, the superclass may also be an abstract class, interface, or any type of abstraction that your programming language comes with.

The Pseudocode implementation for this pattern is also included in the Archive. If you need to implement this pattern in another language,  the pseudocode should help you.

Next,  let’s put the Composite Pattern into use.

C#-2a: The Composite Pattern, in C#

==== ==== ==== ==== ====

Here is how the Composite Pattern looks like in C#:

/*

// Component is the superclass which File and Folder classes extend

// You may define any fields and methods shared by both subclasses

*/

abstract class Component {

    // insert any amount of fields and methods

    // where necessary

    String someField;

   void someMethod() {};

}

// General Item Class (as File):

// contains all fields and methods defined at Component

class File: Component {

}

// General Group Class (as Folder):

// contains all fields and methods defined at Component

// Also has:

// - a List of Components, which can contain either Items or Groups

class Folder : Component {

    List<Component> contents = new List<Component>();

}

In the next chapter, we’ll do a walkthrough in implementing this design pattern.

C#-2b: Implementing the Composite Pattern

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

In this chapter, we encounter a situation which suggests having the Composite Pattern as a viable solution. Then, we’ll be coding the Composite Pattern step-by-step.

File Manager

Imagine you are a software engineer at a very popular social media site.

The next website update will have a really cool feature - enable users to upload and organize data files of their choice. And you’re tasked with implementing this functionality. You know you have to design the File and Folder classes, but you also realize that they share too many traits, such as name, date created, date modified, a thumbnail icon, etc.. So you think to yourself, there must be a more simple way to implement this.

The first thing that comes to your mind is to implement the Composite Pattern. This is an ideal situation to apply it as well.

Step 1: The Component Superclass

First, we’ll create the superclass that the File and Folder classes are based on.

We’re coding in C#, so we have the Abstract Class available.

For now, let’s add the following fields to the superclass: the name, the date created, and the date last modified.

/*

// Component is the superclass which File and Folder classes extend

// It has:

// - Name, as a String

// - the Date Created

// - the Date Last Modified

// It can:

// - rename itself

// - update the Last Modified date

*/

abstract class Component {

    String name;

    DateTime dateCreated;

    DateTime dateLastModified;   

}

Step 2: Customizing the Component Constructor

Next, we’ll code a modified version of the constructor for the Component. When a new component is created, its name will be set and its two date fields will be set to the current date.

The Files and Folders that will later extend this superclass will eventually use the same constructor as well.

abstract class Component {

    public String name;

    public DateTime dateCreated;

    public DateTime dateLastModified;      

        /*

    // INPUT: a String

    // Custom Constructor for the Component Class,

    // Upon creation, the dates created and last modified

    // are set to the current date an object would be created

    */

    public Component(String n) {

        this.name = n;

        this.dateCreated = new DateTime();

        this.dateLastModified = new DateTime();

    }   

} 

Here, you see first-hand how shared methods can save a programmer many lines of code and prevent more coding mistakes along the way. Any essential fields and methods between both the File and Folder classes will be present - programmers won’t have the hassle of coding twice as much as needed, as well as having to change certain fields and methods twice.  Also, the rest of the system will treat data objects from these two classes very similarly.

Step 3: Creating the File Class

Now we create the File class.

As stated before, the File class will have some common fields and methods as the Folder class. It even has a very similar constructor method.

However, the File class here will have more distinctive fields. It will include some indication of the file’s type (i.e. a spreadsheet, letter document, slideshow, picture, video, PDF, etc.). The constructor is further modified to include this.

/*

// General Item Class (a.k.a. File):

// contains all fields and methods defined at Component

// Also has:

// - a file type, as a string

*/

class File : Component {

    public String fileType;

    /*

    // INPUT: a String

    // Custom Constructor for the File Class,

    // Follows the same procedure as the superclass,

    // Then sets the file type

    */

    public File(String n, String f) : base(n) {       

        this.fileType = f;

    }

}

Step 3: Creating the Folder Class

Creating the Folder Class will be a very similar procedure as creating the File class.

However, the difference is that the Folder class will have its key field - a list of components, which can be either Files or SubFolders.

// General Group Class (a.k.a. Folder):

// contains all fields and methods defined at Component

// Also has:

// - a List of Components, which can contain either Items or Groups

class Folder : Component {

    public List<Component> contents = new List<Component>();   

    public Folder(String n) : base(n){

    }

}

Step 4: Running and Testing the Code

Now we’ll test the classes by writing a few lines of code.

We’ll create a handful of Files and Folders, then organize them in a sort of hierarchy.

Run these lines of code in your Main Class, within the Public-Static-Void-Main method (or any other place where the following lines of code will run)

                            Folder top = new Folder("Top Folder");

                            File a = new File("A", "Spreadsheet");

                            File b = new File("B", "Picture");

                            Folder mid = new Folder("Mid Folder");

                            top.contents.Add(a);

                            top.contents.Add(b);

                            top.contents.Add(mid);

                            File c = new File("C", "Video");

                            File d = new File("D", "Letter Document");

                            Folder bot = new Folder("Bottom Folder");

                            mid.contents.Add(c);

                            mid.contents.Add(d);

                            mid.contents.Add(bot);

                            File e = new File("E", "PDF");

                            bot.contents.Add(e);                                       

Afterwards, place these lines of code just after the code above. Then, run the code.

                                    Console.WriteLine(top.name);   

        foreach (var Component in top.contents) {

            Console.WriteLine("    " + Component.name);

        }

        foreach (var Component in mid.contents) {

            Console.WriteLine("        " + Component.name);

        }

        foreach (var Component in bot.contents) {

            Console.WriteLine("            " + Component.name);

        }

After implementing the above steps correctly, the output should be like so:

Top Folder

    A

    B

    Mid Folder

        C

        D

        Bottom Folder

            E

If properly implemented, we can create a hierarchical system of files, folders, and subfolders.

In the next chapter, you’ll have a workshop to implement the Composite Pattern on your own. Good luck!

C#-WORKSHOP 2:

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

MMORPG

You’re a game developer for an online roleplaying game. You’re adding the functionality to store and organize in-game items - such as swords, books, potions, food, etc. -  into ‘bags’.

And yes, you’ll be using the Composite Pattern. Design the classes in a way such that you can use bags to store in-game items and even other bags. Remember: think of ALL the fields and methods that both items and bags will share, as well as the fields and methods unique to each of them.

Here’s the stub for the Composite Pattern to get you started. Good luck!

abstract class Component {

              // Insert Fields and Methods here

}

class Item : Component {

              // Item has all Fields and Methods from Component

              // Insert Unique Fields and Methods here

}

class Bag : Component {

              //  Bag has all Fields and Methods from Component

              // Insert Unique Fields and Methods here

              // Bags also has a List of Components

              // (which can either be Items or other Bags)

    public List<Component> contents = new List<Component>();

}

Advanced Coding:

Since you’re developing a video game, I’m pretty sure you wouldn't want hackers to steal or manipulate players’ in-game items, wouldn't you?

So modify your code to ensure items and bags won’t be accessed so easily (hint: use the modifiers private/public, then add getter/setter functions!)

Chapter 3: The Observer Pattern

==== ==== ==== ==== ====

Let’s say you have to design two classes.

One of those data classes is essentially a data report on the environment around you: the weather, time, date, location, etc.

The other class creates a handful of objects that depend on data from the first class. For example, the latter class could make a list of all your friends nearby, display weather for the next 24 hours, remind you of certain dates or events, and more.

Essentially, one object consistently needs updates from another object.

In the simplest words possible, an object needs to ‘observe’ another object.

This is when you use the Observer Pattern.

How it essentially works:

This happens to be one of the most referenced design patterns out there.

You have two classes: an Observer and a Subject (it’s clear who’s observing who here.)

However, since observing and being a subject are merely ‘behaviours’, we implement Observer and Subject Interfaces. This level of abstraction allows classes in your code to consistently apply Observer and Subject behaviours. So if you have any classes that need either role, you simply have those classes implement their respective interfaces.

All classes that implement the Observer interface have a list of Subject objects to watch out for. These classes also need an update method, which is designed to update their data based on corresponding updates by subject objects.

Likewise, all classes that implement the Subject interface have a list of Observer objects to notify. Also, those classes need notify method, which notifies its list of observers of any changes to its data.

Overall, here is how the update procedure goes. When an observer makes a change to its data, it calls the method notify(), which tells its list of observers about those changes. Those observers then call update(), which makes updates to their own data based on the changes sent.

Here is the UML diagram describing the Class/Interface relationships:

![](Image00005.jpg)

There are two different things to think about when implementing the Observer pattern: the number of observers and the number of subjects. Thus, we will be implementing multi-observer and multi-subject scenarios to show you their dynamics.

C#-3a: The Observer Pattern, in C#

==== ==== ==== ==== ====

Here is how the Observer Pattern looks like in C#.

There are two distinct sets of class/interface pairs.

The first is the Observing pair, including the class and interface.

/*

// All Observing Classes implement an Observer abstraction

// It can:

// - update object data based on subjects

// Observing Classes may need a List of Subjects to access

// (added on Observer Class)

*/

interface Observer {         

    void update();

    // enter any other methods here

}

/*

// Observing Classes have:

// - working version of the update() method

// - any number of additional fields & methods

*/

class ObservingClass : Observer {

     // enter any key fields here;   

    // INPUT: (optional)

    // OUTPUT: none

    // EFFECT: updates data in response to subject

    void Observer.update() {

    // make any changes to observer's key fields here

    }

}

Next is the Subject pair, including the class and interface.

/*

// All Subject Classes implement a Subject abstraction

// It can:

// - notify observers

// - add/remove observers in its update list

// Subject Classes also need a List of Observers to Update

// (added on Subject Class)

*/

interface Subject {

    public void notifyObservers();

    public void addObs(Observer o);

    public void deleteObs(Observer o);

    // enter any other methods here

}

/*

// Subject Classes have:

// - a List of Observers to notify

// - a working version of notifyObservers()

// - any number of additional fields & methods

// Subject Classes also need a List of Observers to Update

// (added on Subject Class)

*/

class SubjectClass : Subject {

     // enter any key fields here;   

    private List<Observer> obs = new List<Observer>();

    // INPUT: (optional)

    // OUTPUT: none

    // EFFECT: updates all observers in list of any changes

    public void notifyObservers(){

        foreach (var o in obs) {

            o.update();

            }

        }

    // Add/Delete Methods:

    // INPUT: - an Observer

    // OUTPUT: none

    // EFFECT: updates data in response to subject   

    public void addObs(Observer o) {

        obs.Add(o);

        }

    public void deleteObs(Observer o) {

        obs.Remove(o);

        }

    }

In the next chapter, we’ll do a walkthrough in implementing this design pattern.

C#-3b: Implementing the Observer Pattern

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

In this chapter, we’ll be adding the Observer Pattern step-by-step based on an appropriate situation you might encounter while coding (because in reality, you really may be good enough to be a hacker serving government intel one day).

Manhunt

Picture yourself as a hacking specialist recruited by the FBI. There is a terrorist group that the FBI are trying to catch. You can somehow easily track the terrorists, but the problem is that several dozen agents need that tracking information immediately. Therefore, you need to modify their device software.

Your first course of action is to create a prototype module that alerts devices if terrorists are near.

Step 1: Identify the Observers & Subjects

First, who or what are the subjects?
And who or what are the observers?

Right. The terrorists will be the Subject to look out for. So you need to represent information about the terrorists in a few lines of code - a class. For now, you need to keep track of their whereabouts - in other words, their location.

// A single terrorist has:

// - a Location, as a String

// - a List of Observer Objects

class Terrorist{

              public String location;

}

The FBI devices will be the Observers. So far, we’ve been given this amount of code for a small module within the device OS. The module pushes alerts on critical notifications.

// A Device module has:

// - an alert status (a Boolean)

// - notification updates (as string)

// - a Location, as a String

// It can:

// - push alerts

// - update alerts & notifications

class Module{

    public String location;

    public boolean alert;

    public String notifications;

//  EFFECT: if alerts is true, print an alert notice   

    void sendAlerts(){

        if (alert) {

            Console.WriteLine("ALERT: "

                               + notifications

                               + "Agents in "

                               + this.location);

        }

    }

}

Step 2: Set up the Observer and Subject Abstractions

In C#, the abstractions for Observer and Subject will be interfaces.

So we will model them as such.

/*

// All Observing Classes implement an Observer abstraction

// It can:

// - update object data based on subjects

// Observing Classes may need a List of Subjects to access

// (added on Observer Class)

*/

interface Observer {         

    void update();

}

/*

// All Subject Classes implement a Subject abstraction

// It can:

// - notify observers

// - add/remove observers in its update list

// Subject Classes also need a List of Observers to Update

// (added on Subject Class)

*/

interface Subject {

    void notifyObservers();

    void addObs(Observer o);

   void deleteObs(Observer o);

}

Step 3: Modify our Subject Class to act as one

Our data object representing a Terrorist will be acting as a Subject Class. Therefore, it will implement the  Subject interface.

However, you also need to add & implement the methods included in the Subject interface.

It will also be changed to include a list of Observer objects to modify. Keep this field as private - just for added protection against hackers.

// A single terrorist has:

// - a Location, as a String

// - a List of Observer Objects

// Also implements the Subject Interface;

// (will need to implement its methods)

class Terrorist : Subject{

              public String location;

              private List<Observer> obs = new List<Observer>();

              // NEW: from Subject Interface

              public void notifyObservers() {};

              public void addObs(Observer o) {};

              public void deleteObs(Observer o) {};

}

For the method notifyObservers, it should iterate through the list of Observers and update each one. Modify the method to do so.

              // NEW: from Subject Interface

              public void notifyObservers() {

                            foreach (var o in obs)  {

                                          o.update();

                            }

              }

Next, we implement the methods addObs() and deleteObs(). All they do is add and remove Observer objects from the List, respectively. 

              public void addObs(Observer o) {

                      obs.Add(o);

                  };

              public void deleteObs(Observer o) {

                                    obs.Remove(o);

                 };

After all the changes, your Terrorist class should look like this:

class Terrorist implements Subject{

              String location;

              private List<Observer> obs = new ArrayList<Observer>();

              // NEW: from Subject Interface

              public void notifyObservers() {

                            for (Observer o: obs)  {

                                          o.update();

                            }

              };

              public void addObs(Observer o) {

                       obs.add(o);

                   };

              public void deleteObs(Observer o) {

                     obs.remove(o);

                  };

}

Step 4: Modify our Observer Class to act as one

The Module data class will act as an Observer. Thus, it will implement the Observer interface and all included methods. 

// A Device module has:

// - an alert status (a Boolean)

// - notification updates (as string)

// - a Location, as a String

// It can:

// - push alerts

// - update alerts & notifications

// Also implements the Observer Interface;

// (will need to implement its methods)

class Module : Observer{

   public String location;

    public boolean alert;

    public String notifications;

    public void update() {};

    //  EFFECT: if alerts is true, print an alert notice             

    void sendAlerts(){

        if (alert) {

            Console.WriteLine("ALERT: "

                               + notifications

                               + "Agents in "

                               + this.location);

        }

    }

}

Before we implement update(), you have to understand the situation and context you are in.

In this situation, ask yourself: “how is the Module class going to work, responding to the Terrorist class?”

Well…

Step 5: Modify the Observing Class to update, based on Subject Classes

The Module class needs to update & send alerts whenever a Terrorist is nearby.

A Terrorist has location fields as a String. So does Module.

So whenever a module has the same location as a Terrorist’s, it will send an alert.

But for Module to receive data from the Terrorist class, you need to change the update() method.

You need it to have a Terrorist as an input.

    // INPUT: a Terrorist Object

    // OUTPUT: none

    // EFFECT: if Terrorist and this module's locations are the same,

    // set Alert to true and update the notification.

    // Afterwards, send the alerts

    public void update(Terrorist t) {               };

You also need the corresponding updates for any other code that has this method. So you’ll need to modify the Observer interface to include the same input…

interface Observer {         

              …

    public void update(Terrorist t);

              …

… as well as the notifying method in the Terrorist class for the same input type. The purpose of the method is to notify its observers based on its Class data. So for this method, you’ll have the class itself as the input.

class Terrorist : Subject{

              …

              public void notifyObservers() {

                            foreach (var o in obs)  {

                                          o.update(this);

                            }

              };

              …

Afterwards, we get the update() method to work.

Step 5: Implementing update()

Based on the information above, we implement the functional code for the update() method within the Module class.

    // INPUT: a Terrorist Object

    // OUTPUT: none

    // EFFECT: if Terrorist and this module's locations are the same,

    // set Alert to true and update the notification.

    // Afterwards, send the alerts

    public void update(Terrorist t) {

        if (this.location == t.location) {

            this.alert = true;

            this.notifications = "Terrorist Nearby ";

        }

        else {

            this.alert = false;

            this.notifications = "";

        }

        sendAlerts();

    };

Running the Code

We’ll have two scenarios to run based on the code we have.

In both scenarios, the Observing classes will signal an alert based on the subject they are ‘observing’.

One scenario is when there are way more observers than subjects:

(Copy and paste the code below inside your Main() method)

// - - - - - - - - - -- - - - -- - - - -- - - - -

// Part 1: Create all Data Objects

            Terrorist t = new Terrorist();

            Module m1 = new Module();

            Module m2 = new Module();

            Module m3 = new Module();

            Module m4 = new Module();

            // Part 2: Add all Observers to Subject's List

            t.addObs(m1);

            t.addObs(m2);

            t.addObs(m3);

            t.addObs(m4);

            // Create all locations

            String[] locs = new String[10];

            locs[0] = "Los Angeles";

            locs[1] = "Chicago";

            locs[2] = "New York";

            locs[3] = "Seattle";

            locs[4] = "Cleveland";

            locs[5] = "Boston";

            locs[6] = "San Francisco";

            locs[7] = "Miami";

            locs[8] = "St. Louis";

            locs[9] = "Dallas";    

            // Part 3: Set Observers to their locations

            m1.location = locs[1];

            m2.location = locs[4];

            m3.location = locs[5];

            m4.location = locs[9];

            // As the Terrorist relocates all over the US,

            // it will notify all Device Modules of its location.

            // Modules will trigger when a Terrorist is nearby.

            for(int i = 0; i < 10; i++) {

                t.location = locs[i];

                t.notifyObservers();

            }

// - - - - - - - - - -- - - - -- - - - -- - - - -

If all the code runs, you should have this as your printed output:

ALERT: Terrorist Nearby Agents in Chicago

ALERT: Terrorist Nearby Agents in Cleveland

ALERT: Terrorist Nearby Agents in Boston

ALERT: Terrorist Nearby Agents in Dallas

The other scenario is when there are way more subjects than observers.

(Copy and paste the code below inside your Main() method)

// - - - - - - - - - -- - - - -- - - - -- - - - -

// Part 1: Create all Data Objects

            Terrorist t1 = new Terrorist();

            Terrorist t2 = new Terrorist();

            Terrorist t3 = new Terrorist();

            Terrorist t4 = new Terrorist();

            Terrorist t5 = new Terrorist();       

            Module m = new Module();

            // Part 2: Add all Observers to Subject's List

            t1.addObs(m);

            t2.addObs(m);

            t3.addObs(m);

            t4.addObs(m);

            t5.addObs(m);  

            // Create all locations

            String[] locs = new String[10];

            locs[0] = "Los Angeles";

            locs[1] = "Chicago";

            locs[2] = "New York";

            locs[3] = "Seattle";

            locs[4] = "Cleveland";

            locs[5] = "Boston";

            locs[6] = "San Francisco";

            locs[7] = "Miami";

            locs[8] = "St. Louis";

            locs[9] = "Dallas";    

            // Part 3: Set Observers to their locations

            t1.location = locs[1];

            t2.location = locs[4];

            t3.location = locs[2];

            t4.location = locs[7];

            t5.location = locs[5];

            // The single agent with the Device Module will travel all over the US,

            // All Terrorists will then notify the observing module.

            // The module will trigger when a Terrorist is nearby.

            for(int i = 0; i < 10; i++) {

                m.location = locs[i];

                t1.notifyObservers();

                t2.notifyObservers();

                t3.notifyObservers();

                t4.notifyObservers();

                t5.notifyObservers();            }

// - - - - - - - - - -- - - - -- - - - -- - - - -

If all the code runs, you should have this as your printed output:

ALERT: Terrorist Nearby Agents in Chicago

ALERT: Terrorist Nearby Agents in New York

ALERT: Terrorist Nearby Agents in Cleveland

ALERT: Terrorist Nearby Agents in Boston

ALERT: Terrorist Nearby Agents in Miami

Chapter 4: The Singleton Pattern

==== ==== ==== ==== ====

Think of ideas and things that can only have one existing object.

Perhaps you’re designing an app and one of the classes should not have multiple instances of it at the same time. Just like the only active Pacman in the game; or the only  ball in a game of pong; or the only Mario playing at a classic Super Mario game.

And you realize that you don’t want to let bugs, exploits, or any sort of hacks exist by giving opportunities to create multiple objects that should really stay single.

There’s a solution to this. It’s called the Singleton pattern.

With it, you can modify your Class to have only one possible object at a time. Or one possible object forever.

How it essentially works:

The Singleton pattern is one of the more simple design patterns. However, when a situation calls for its design, it will prove to be more than helpful.

There are three key components to a Singleton class. First, the class constructor is set in a certain way such that it cannot be used outside the class. This ensures the singleton class remains a singleton by removing the ability to make instances of it except within its own code.

Second, the class itself will contain the only instance based on it. The singleton class has its only object as one of its own fields.

And lastly, the third component is a method that retrieves the actual single object. This method has to be accessible without needing a created class object. In most implementations, it uses the First component (the class-code-only constructor) to create the object if it doesn’t exist yet.

Here is the UML diagram describing the Singleton class:

![](Image00006.jpg)

The Pseudocode implementation for this pattern is also included in the Archive, in case you need to implement this pattern in another language.

Next, we’ll be using applying the Singleton pattern in a scenario.

C#-4a: The Singleton Pattern, in C#

==== ==== ==== ==== ====

Here is how the Singleton Pattern looks like in C#.

/*

// A Singleton Class has:

// - A Singleton Instance

// - any other Fields you need

//

// it can NOT:

// - be instantiated as normal (as if it were a regular class)

// (The constructor is set to Private, just to be sure)

//

// It can:

// - return the ONLY singleton class instance

*/

class Singleton {

    // Singleton Component #1:

    // CONSTRUCTOR:

    // - set to PRIVATE; cannot be accessed outside the class

    private Singleton() { }

    // Singleton Component #2:

    // The Only Singleton Object:

    // - set to PRIVATE; cannot be accessed outside the class  

    private static Singleton obj = null;

    // Singleton Component #3:

    // INPUT: (your choice)

    // OUTPUT: A Singleton Object

    // EFFECT: Returns the ONLY singleton object.

    // Creates one if nonexistent.

    // - set to STATIC; will not require an Object to call this method

    public static Singleton getObject() {

        if (obj == null) {

            obj = new Singleton();

            // Initialize any other fields here

            }

        return obj;

        }

    }

To access your Singleton object, you simply need to call the static method getObject(). Note that the Singleton Object is expected wherever you call the Method.

// Assigning the Singleton to Variable sg

Singleton sg = Singleton.getObject();

Also note that you can assign the same Singleton to multiple variables; they will all refer to the same Singleton

// Assigning the Singleton to multiple Variables

Singleton sg1 = Singleton.getObject();

Singleton sg2 = Singleton.getObject();

Singleton sg3 = Singleton.getObject();

C#-4b: Implementing the Singleton Pattern

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

In this chapter, we’ll encounter a situation that will greatly benefit from a Singleton Pattern implementation.

Championship

Think of any sports leagues out there. In a given season, each team within a league has a set of games against other teams in the league. At the end of the season, the winningest   handful of teams of the season qualify for a single-elimination tournament.

Out of those teams in the tournament, only one will be crowned the Champions.

Champions.

Only one.

If you were programming this, you realize your program might run into problems if two or more Final Championship teams occur within a league in a single season.

So a situation that can only have one of a single component requires the Singleton Pattern.

Step 1:  Identify the Classes and Procedures in your App

In this case, we will keep things simple and only identify and define two classes for now: a Sports Team…

// A Team has:

// - a Name (String)

// - any other fields you want

class Team {

    public String name;

    // CONSTRUCTOR:

    // INPUT: a Team Name (String)

    public Team(String n) {

        this.name = n;

    }

}

…and the Championship.

// A Championship has:

// - a Championship Team

//

// it can:

// - Run a Playoffs Tournament with 8 Teams

class Championship {

    public Team champion;

    // INPUT: 8 Teams

    // OUTPUT: none

    // EFFECT: The Playoffs Simulator:

    // - match up the teams pair by pair,

    // - winning teams advance to the next matches

    // - last team becomes the Champion Team

  // NOTE: if a championship already has a champion team,

    // playoffs() will return without simulating the Playoffs

    public void playoffs(Team t1,

                                Team t2,

                                Team t3,

                                Team t4,

                                Team t5,

                                Team t6,

                                Team t7,

                                Team t8) {

              // return if champion team already present

              if (champion != null) return;

        Random r = new Random();

        // QUARTER -> SEMIFINALS:

        Team semi1 = match(t1, t8, r.Next());

        Team semi2 = match(t2, t7, r.Next());

        Team semi3 = match(t3, t6, r.Next());

        Team semi4 = match(t4, t5, r.Next());

        Console.WriteLine("");

        // SEMIFINALS -> FINALS:

        Team finals1 = match(semi1, semi4, r.Next());

        Team finals2 = match(semi2, semi3, r.Next());

        Console.WriteLine("");

        // FINALS -> CHAMPIONSHIP:

        Team champ = match(finals1, finals2, r.Next());

        this.champion = champ;

        Console.WriteLine("Team " + champ.name + " WIN THE CHAMPIONSHIP!");              }

       /*

        // HELPING FUNCTION to playoffs():

        // INPUT: - Two Teams: a & b

        //        - an integer (to determine winners)

        // OUTPUT: a Team

        // EFFECT: Match between two teams a & b,

        // with the winner as the Output

        */

        private Team match(Team ta, Team tb, int odds) {          

            if (odds %2 == 0) {

                Console.WriteLine(ta.name + " Defeats " + tb.name);

                return ta;               

            }

            else {

                Console.WriteLine(tb.name + " Defeats " + ta.name);

                return tb;               

            }           

        }  

    }

Within the public-static-void main() Method, these following lines create the 8 Teams then run the Championship afterwards.

        // Create 8 Teams:

        Team contender1 = new Team("Archers");

        Team contender2 = new Team("Bobcats");

        Team contender3 = new Team("Centurions");

        Team contender4 = new Team("Danger Zone");

        Team contender5 = new Team("Energy");

        Team contender6 = new Team("Flames");

        Team contender7 = new Team("Guards");

        Team contender8 = new Team("Hunters" );

        // Run the Championship Playoffs:

        Championship c = new Championship();

        c.playoffs(contender1,

                   contender2,

                   contender3,

                   contender4,

                   contender5,

                   contender6,

                   contender7,

                   contender8);

If you run all the code, you should see something similar to below, except that the team names are mixed around:

Hunters Defeats Archers

Guards Defeats Bobcats

Flames Defeats Centurions

Danger Zone Defeats Energy

Danger Zone Defeats Hunters

Guards Defeats Flames

Danger Zone Defeats Guards

Team Danger Zone WIN THE CHAMPIONSHIP!

Step 2: Identify which class should be a Singleton

But there’s a Problem.

We only want one Championship Team and one Playoff every time we run the code.

If these few lines of code are run in the main() method…

Championship[] cc = {new Championship(),

                             new Championship(),

                             new Championship(),

                             new Championship(),};

        foreach (Championship x in cc) {

            x.playoffs(contender1,

                   contender2,

                   contender3,

                   contender4,

                   contender5,

                   contender6,

                   contender7,

                   contender8);

            Console.WriteLine("");            

        }

… there will be way too many champion teams.

So what can we do to restrict the code produce only one champion team?

Convert the Championship class into a Singleton.

We do this by adding the components to a Singleton class one by one. Other than this, everything else about the Championship class remains unchanged.

Component #1: A private Class Constructor

Setting the Constructor to private ensures that objects of the class CANNOT be created - except from code within the class.

For a singleton class, a private constructor (along with the other singleton components) ensure that the object will be a singleton.

Below is the modified constructor for Championship, along with its explanatory comments. Add this code within the Championship class:

    // Singleton Component #1:

    // - Constructor with private modifier

    // (cannot be accessed from outside the Class)

    private Championship() {};

Component #2: The single class object

Your Singleton class will include an exclusive field, which will eventually be the only object constructed by your class.

It will be a private field so it won’t be accessed outside the class.  It will also be one of the two singleton components that will be static - they can be accessed through the class itself, not its objects.

By default, the field will be set to null. It will eventually be assigned once the third component is called.

Below is the field for the class object. Add the code below inside the Championship class:

    // Singleton Component #2:

    // - a class object as a field

    // - has Static Modifier (can access field from the class itself)

    // - has private Modifier (cannot be accessed from outside the Class)

    private static Championship c = null;

Component #3: The getObject() method

The final singleton component for the Championship class will be the getObject() method. As one of the two static components, this method is meant to be accessed from the Championship class, not one of its objects.

What it does is retrieve the only Championship object created in your code. If it’s not created yet, it will call Component #1 (the Custom Constructor) to create one.

Below is the method. Just add the code  within the Championship class:

// Singleton Component #3

    // - a getObject() method 

    // INPUT: none

    // OUTPUT: a Championship object

    // EFFECT: returns the Singleton Championship object

    public static Championship getChamp() {

        if (c == null) {

            c = new Championship();

        }

        return c;

    }

The Singleton Championship Class

Overall, the Singleton version of the Championship class should remain the same, except that you’ve added the three singleton components into it.

The Main Code, Now with the Singleton Championship

Now, we’ll run this code within the main() method:

        // Create 8 Teams:

        Team contender1 = new Team("Archers");

        Team contender2 = new Team("Bobcats");

        Team contender3 = new Team("Centurions");

        Team contender4 = new Team("Danger Zone");

        Team contender5 = new Team("Energy");

        Team contender6 = new Team("Flames");

        Team contender7 = new Team("Guards");

        Team contender8 = new Team("Hunters" );

// Using Singleton: 

        Championship.getChamp().playoffs(contender1,

                   contender2,

                   contender3,

                   contender4,

                   contender5,

                   contender6,

                   contender7,

                   contender8);

If you run all the code, you should still see something similar to below (team names could still be mixed around):

Hunters Defeats Archers

Guards Defeats Bobcats

Flames Defeats Centurions

Danger Zone Defeats Energy

Danger Zone Defeats Hunters

Guards Defeats Flames

Danger Zone Defeats Guards

Team Danger Zone WIN THE CHAMPIONSHIP!

The main difference with the converted Singleton version is that there is now absolutely only one Championship team for every time the entire code is run. Making multiple calls to playoffs() won’t run multiple playoff runs; it can only be run the first time around. Also, there can only be one championship object per code run. Therefore there can only be up to one playoff run and one champion team when the code is run.

You can see the benefits to this. For example, if you were writing code for competitive sport, you can create such restrictions on your code to make it more difficult for hackers to misuse your program. 

Advanced Coding:

The Singleton pattern can also have other unique variants. What would it take to have two distinct champions and playoffs every time the code is run? Modify the code to have exactly two unique Championship objects per run, each calling the playoffs() method exactly once. (hint: two champions = two objects = two get() methods!)

Chapter 5: The Strategy Pattern

==== ==== ==== ==== ====

Picture this scenario.

You have three choices for commuting to work everyday: by bike, by public transit, or by driving your car.

However, there are quite a handful of factors that affect your choice. This includes the weather outside, whether or not you want to work out, how long are you willing to commute, level of vehicle traffic, any construction, car crashes, and more.

How will you know which choice to pick? And even after choosing your commute method, how will your route to and from work be affected?

Now picture an algorithm to your solution to the above. It would probably involve a system of if-statements before picking your commute choice.

The next day, some or all of the factors could be different and you’d have to figure out how you’d like to commute to work and back. You’d run your algorithm again. And again for the day after. And so on.

This looks like a seemingly complex algorithm to figure out. Fortunately, this is a situation which requires a choice of algorithm variants.

This is a scenario fit for the Strategy Pattern.

How it essentially works:

the Strategy Pattern takes advantage of class polymorphism in Object-Oriented Programming. In other words, you can embed the algorithm variants within a set of common classes that can interchange depending on the situation.

The algorithms are accessed through the abstraction, which can either be abstract classes, interfaces, or anything else your programming language allows.

The abstraction object can be any of the subclasses that extend it. Hence, the algorithm variants can be switched around depending on the situation.

Applying the Strategy Pattern:

Here is the step-by-step plan for implementing this design pattern:

1) Figure out when will your process have to change depending on the situation.

2) Create the abstract form of your strategy algorithm.

3) Implement the variants for your strategy algorithm in subclasses.

4) Anything that access your strategy algorithm does it through the abstract form. Through Polymorphishm, the best strategy variant is selected and executed depending on the situation.

Overall, here is the UML diagram describing the Strategy Pattern:

![](Image00007.jpg)

C#-5a: The Strategy Pattern, in C#

==== ==== ==== ==== ====

Here is how the Strategy Pattern looks like in C#:

/*

// ABSTRACT STRATEGY IMPLEMENTATION:

// This has:

// - the signature for the abstract algorithm

*/

interface AbstractStrategy {

        // IN: (Your Choice)

        // OUT: (Your Choice)

        // (effect based on Subclass level)

        void Algorithm();

    }

/*

// CLASSES FOR EACH STRATEGY:

// Use any amount of needed classes based on the Abstract Strategy

// Each Class can:

// - implement the Abstract Algorithm

//   (based on the unique strategy from each class)

*/   

class Strategy1 : AbstractStrategy{

        // Abstract Algorithm,

        // as Strategy1:   

        void AbstractStrategy.Algorithm() {

                // Implement this algorithm uniquely

                // based on this Strategy1 Class

        }

    }

class Strategy2 : AbstractStrategy{   

        // Abstract Algorithm,

        // as Strategy2:

        void AbstractStrategy.Algorithm() {

                // Implement this algorithm uniquely

                // based on this Strategy2 Class           

        }

    }

C#-5b: Applying The Strategy Pattern (Simple)

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

In this chapter, we have a chance to apply the Strategy pattern on a given situation.

Let’s play Rock-Paper-Scissors. In order to win, we would always have the right choice between rock, paper, and scissors.

An instance of the game would usually be based on a class, designed like so:

/*

// A Rock-Paper-Scissors Game has:

// - the String values for Rock, Paper, and Scissors

// It can:

// - generate a random string from either of the three

// - check if a player wins

*/

class RPSGame {

        String[] RPSVals = {"Rock", "Paper", "Scissors"};

    /*

    // INPUT: none

    // OUTPUT: a String

    // EFFECT: randomly return either Rock, Paper, or Scissors

    */

    public String RPSGet() {

        Random rn = new Random();       

        int i = rn.Next(1, 4);

        return RPSVals[i] ;

    }

    /*

    // INPUT: 2 Strings

    // OUTPUT: a Boolean

    // EFFECT: return true if 1st string defeats 2nd string,

    //      false otherwise

    */

    public bool checkWin(String s1, String s2) {

        if (s1 == s2) return false;       

        bool c1 = (s1 == "Paper") && (s2 == "Rock");

        bool c2 = (s1 == "Scissors") && (s2 == "Paper");

        bool c3 = (s1 == "Rock") && (s2 == "Scissors");

        return c1 || c2 || c3;

    }

}

Next, here is the code that goes to the Main() method to be executed:

              RPSGame r = new RPSGame();

                String aiPick = r.RPSGet();                           

                // Enter either "Paper", "Scissors", or "Rock"

                // for the variable myPick

                // (Normally, a player would input a value for this)

                // For now, default pick to Paper

                String myPick = "Paper";

                Console.WriteLine("AI Pick: " + aiPick);

                Console.WriteLine("My Pick: " + myPick);                           

                Console.WriteLine(myPick + " v.s. " + aiPick);

                if (r.checkWin(myPick, aiPick)) Console.WriteLine("YOU WIN!");

When run, the overall code simulates one game of Rock-Paper-Scissors. You would have to enter your choice between Rock, Paper, or Scissors. Afterwards, the program will generate a choice for your opponent, then check whether or not you’ve won.

Fortunately, you can hack this code to ALWAYS have a winning choice. You would therefore always win. This requires a procedure that has the very best outcome given the situation we’re currently in.

This calls for the Strategy Pattern

Applying the Strategy Pattern:

Recall the step-by-step plan mentioned earlier to implement the strategy pattern.

1) Figure out when will your process have to change depending on the situation.

In our Rock-Paper-Scissors code, we want the code to always choose the best option (depending on what a human player pics)

This event occurs once the player makes his/her choice.

Hence, the code will always choose the option that defeats the player.

So:

Player picks Rock -> Code picks Paper

Player picks Paper -> Code picks Scissors

Player picks Scissors -> Code picks Rock

2) Create the abstract form of your strategy algorithm.

Recall the interface for the Abstract Strategy Class. In Java, this abstraction can be made using interfaces:

/*

// ABSTRACT STRATEGY IMPLEMENTATION:

// This has:

// - the signature for the abstract algorithm

*/

interface AbstractStrategy {

        // IN: (Your Choice)

        // OUT: (Your Choice)

        // (effect based on Subclass level)

        void Algorithm();

    }

Based on the prior code, we can create the abstract version of our Rock-Paper-Scissors strategy algorithm. The algorithm can return an option to choose, in the form of a String.

/*

// ABSTRACT STRATEGY IMPLEMENTATION:

*/

interface RPSStrategy  {

        // IN: none

        // OUT: a String (either one of the three picks)

        // (effect based on Subclass level)

        String Algorithm();

    }

3) Implement the variants for your strategy algorithm in subclasses.

Here is the strategy variant subclass from a previous chapter:

class Strategy1 : AbstractStrategy{

        // Abstract Algorithm, as Strategy1:   

        void AbstractStrategy.Algorithm() {

                // Implement this algorithm uniquely

                // based on this Strategy1 Class

        }

    }

We make a class for Rock, Paper, and Scissors. Each class will have a distinct output in their Algorithm implementations. We first start with Rock:

// Subclass Implementation for Rock:

class Rock : RPSStrategy {

        // Abstract Algorithm, as Rock:   

        String RPSStrategy.Algorithm() {

            // (any other code here)           

                      return "Rock";

                  }              

}

Afterwards, we continue implementing the other two options:

// Subclass Implementation for Paper:

class Paper : RPSStrategy {

        // Abstract Algorithm, as Rock:   

        String RPSStrategy.Algorithm() {

            // (any other code here)           

                      return "Paper";

                  }              

}

// Subclass Implementation for Scissors:

class Scissors : RPSStrategy{

        // Abstract Algorithm, as Rock:   

        String RPSStrategy.Algorithm() {

            // (any other code here)

                      return "Scissors";

                  }

}

Now, we can start modifying our earlier code to start using the Strategy Pattern.

4) Anything that access your strategy algorithm does it through the abstract form…

Here is the original Rock-Paper-Scissors code inside main() :

RPSGame r = new RPSGame();

                String aiPick = r.RPSGet();                           

                // Enter either "Paper", "Scissors", or "Rock"

                // for the variable myPick

                // (Normally, a player would input a value for this)

                // For now, default pick to Paper

                String myPick = "Paper";

                Console.WriteLine("AI Pick: " + aiPick);

                Console.WriteLine("My Pick: " + myPick);                           

                Console.WriteLine(myPick + " v.s. " + aiPick);

                if (r.checkWin(myPick, aiPick)) Console.WriteLine("YOU WIN!");

Now we can modify the code to ALWAYS pick a winning choice using our simple implementation of the Strategy Pattern. The variable myPick will then be the winning choice.

First, we’ll upgrade the code inside main() to add an instance of our strategy class, just after we initialize the variable myPick:

                            RPSGame r = new RPSGame();

                            String aiPick = r.RPSGet();             

                            String myPick = "";

                            //- - - - - - - - - -

                            // (Initialize the Pattern to any pick you want;

                            // it might be replaced anyway)

                                    RPSStrategy stratPattern = new Rock();

                            //- - - - - - - - - -             

Through Polymorphishm, the best strategy variant is selected depending on the situation.

Next, we add the code that modifies the strategy pattern to a winning choice. It will be the lines just after we added an instance of the Strategy Pattern:

              //- - - - - - - - - -

              // (Initialize the Pattern to any pick you want;

              // it might be replaced anyway)

        RPSStrategy stratPattern = new Rock();

        if (aiPick == "Rock") {

            stratPattern = new Paper();

        }

        if (aiPick == "Paper") {

            stratPattern = new Scissors();

        }

        if (aiPick == "Scissors") {

            stratPattern = new Rock();

        }

              //- - - - - - - - - -

Lastly, the variable myPick will then be the winning choice from the strategy pattern. A call to Algorithm() from stratPattern, no matter which form it takes after the three if-statements, will return a winning choice.

              //- - - - - - - - - -

              // (Initialize the Pattern to any pick you want;

              // it might be replaced anyway)

        RPSStrategy stratPattern = new Rock();

        if (aiPick == "Rock") {

            stratPattern = new Paper();

        }

        if (aiPick == "Paper") {

            stratPattern = new Scissors();

        }

        if (aiPick == "Scissors") {

            stratPattern = new Rock();

        }

              // NEW LINE:

        myPick = stratPattern.Algorithm();

              //- - - - - - - - - -

And here is the original code just after the new modifications. After running the rest of the code, you should always be winning.

                Console.WriteLine("AI Pick: " + aiPick);

                Console.WriteLine("My Pick: " + myPick);                           

                Console.WriteLine(myPick + " v.s. " + aiPick);

                if (r.checkWin(myPick, aiPick)) Console.WriteLine("YOU WIN!");

And there you have it. This is the process of applying the Strategy Pattern.

========================= ======

Hey, let’s take a break from the content for now. Just sit back and digest all the information you’ve been reading up to now. If you’ve yet to catch up on your code, or even yet to start, feel free to do so now. 

And if you’re enjoying our work so far, can you please leave a review on Amazon?

[Click here to leave a review](https://www.amazon.com/review/create-review/ref=cm_cr_dp_wrt_summary?ie=UTF8&asin=B01ESBD0AS&channel=detail-glance&nodeID=133140011&store=digital-text)

It’ll be much appreciated. Your feedback is crucial to improving our work over time.

Thank you!

Chapter 6: The Decorator Pattern

==== ==== ==== ==== ====

When designing classes, all fields and methods seem as if they have to be as-is. In other words, when you create instances of your classes, they would ALL have the same fields and methods as defined by their class.

But what if there is a way to add more features to data objects DURING runtime? Say, a data object acquires more features over time?

It’s possible.

And it’s made possible thanks to the Decorator Pattern.

How it essentially works:

The Decorator Pattern has a similar structure to the Composite Pattern; two classes sharing the same abstraction, while one of them contains an instance of this abstraction. Due to polymorphism, this abstraction can be either one of the two classes.

There are two main generalized classes to develop: the Default Superclass and the Decorator Superclass.

The Decorator class will have an instance of either the Base Class or previously applied Decorator classes. This is in addition to any other fields or methods a Decorator class may add.

For any method common to all classes, the Decorator class will also call the previous object’s method, which will call its previous object’s method, and so on, until the Default Class object’s method is called too. This creates a recursive pattern in which every Decorator, as well as the one Default Class, applies its effect.

This is how it looks like altogether; a single object from the Default class will apply its behaviours differently compared to an object with multiple Decorators attached to it.

Hence, a data object during runtime may have much more different behaviours than originally intended.

This pattern is commonly used in video dame development and any other apps which require a high amount of modularity.

Creating the Decorator Pattern:

Here is the step-by-step plan for implementing this design pattern:

1) Create a general abstraction that covers ALL subclasses and variants.

2) Create the default subclass. This will directly extend your general abstraction from earlier.

3) Create the decoration subclass. Like the default subclass, this will also directly extend your general abstraction.

4) Make sure the decoration subclass contains the previous decoration or the  default class as one of its fields (set the variable type as the general abstraction!). This, along with the next step, are the key traits that allow multiple decorations to be dynamically added to the default class.

5) Make sure the constructor for the decoration subclass inputs either a Decoration or the Base Object (again, set the input type as the general abstraction!) and this input is set as the previous decoration.

6) Create the third-level decoration subclasses. These directly extend the Decoration class you’ve developed in previous steps.

Applying the Decorator Pattern at Runtime:

1) When creating an instance of the Decorator Pattern, set its data type as the abstraction but initialize it as the default subclass:

abstractclass default = new defaultsubclass();

2) When adding a Decoration to a default subclass object, use the previous Decoration or default object as an input. If you designed the pattern correctly, all the decorations should connect to the the default class like a linked list.

DecoratorOne a = new Decorator(default)

DecoratorTwo b = new Decorator(a)

DecoratorTwo c = new Decorator(b)

Here is the UML Diagram for the Decorator Pattern:

![](Image00008.jpg)

This is perhaps one of the more complex design patterns available. But once mastered, this becomes one of the most useful ones in your programming repertoire.

ENJOYING THE CONTENT SO FAR?

========================= ======

Follow us!

We’ll be more than glad to create MORE great content just for you

              @CodeWizRDZ

| ![](Image00000.jpg) | ![](Image00001.jpg) | ![](Image00002.jpg) |
| [Facebook](https://www.facebook.com/CodeWIzRDZ/) | [Instagram](https://www.instagram.com/codewizrdz) | [Twitter](https://www.twitter.com/codewizrdz) |

              @ EzeeProgramming

| ![](Image00000.jpg) | ![](Image00001.jpg) | ![](Image00002.jpg) |
| [Facebook](https://www.facebook.com/EzeeProgramming) | [Instagram](https://www.instagram.com/ezeeprogramming) | [Twitter](https://www.twitter.com/ezeeprogramming) |

Thanks for the Support!

C#-6a: The Decorator Pattern, in C#

==== ==== ==== ==== ====

Here is how the Decorator Pattern looks like in C#. First, we start with the abstract form:

/*

// DECORATOR IMPLEMENTATION:

// This abstract form has:

// - the signature for any common procedures,

//               algorithms, and traits common to ALL subclasses

*/

public abstract class DecorativeObject {

              // IN & OUT: (Your Choice)

              // (Implementation done by Subclasses)

    public void procedure() {

    }

              // (include any other common fields

              // and procedures as you wish)

}

Next, we have the Base and Additional Functionalities.

The Base Object will include ALL default procedures and traits your abstraction has.

public class BaseObject : DecorativeObject {

              // Common Procedure, implemented as Base Object

              public void procedure() {

                                   base.procedure();

                            // (Implement this procedure here)

              }

              // (include any other fields

              // and procedures as you wish)

}

The Decorations will include any additional modifications you’d like to apply to your decorative object. This will use a structure similar to the Composite Pattern.

Creating an instance of one will require the previous Decorator as a Constructor input (or use the BaseObject if there is none). This way, you pretty much daisy-chain as many Decorators as you wish on top of a default Base Object.

public class Decoration : DecorativeObject{

              // Previously applied Decoration Instance added: 

              public DecorativeObject prevDeco;              

              // Common Procedure, implemented as Decoration

                  // Includes any extra effects added by this Decoration

              public void procedure() {

                                    base.procedure();

                                    // (Implement this procedure here,

                            // Add anything else you’d like as well)

                            prevDeco.procedure();

              }

                  // CONSTRUCTOR:

                  public Decoration(DecorativeObject d) {

                  this.prevDeco = d;      

                  } 

    // (include any other fields

              // and procedures as you wish)

}

Notice how the procedure() method calls the previous Decoration’s method as well. This way, once procedure() has been called, its true effect will be delivered by EVERY Decoration added - plus the effects from the Base Object.

And lastly, you can have as many different decoration classes as you wish. They all extend the Decoration class and may include additional fields and procedures of their own

class DecorationOne : Decoration{

              // Common Procedure, implemented as DecorationOne

              // (also implements procedure() as its superclass)

              public void procedure() {

         base.procedure();    

                            // (Implement this procedure here)

              }

              // (include any other fields

              // and procedures as you wish)

    // CONSTRUCTOR:

                  public DecorationOne(DecorativeObject d) : base(d) {

            this.prevDeco = d;      

                  } 

}

class DecorationX : Decoration{

              // Common Procedure, implemented as DecorationX

              // (also implements procedure() as its superclass)

              public void procedure() {

        base.procedure();

                            // (Implement this procedure here)

              }

              // (include any other fields

              // and procedures as you wish)

    // CONSTRUCTOR:

                  public DecorationX(DecorativeObject d) : base(d) {

            this.prevDeco = d;      

                  } 

}

C#-6b: Applying The Decorator Pattern

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

Here, we encounter a scenario which requires the Decorator pattern.

MMORPG Characters:

In Massively-Multiplayer Online Role-Playing fantasy games before, playable characters often fall into certain character archetypes - i.e., the Healer, the Wizard, the Archer, the Armoured Knight, and so on. And as you play the game longer, your player characters gradually improve and become stronger.

In terms of code, a general MMORPG character would be data objects based on some Data Class similar to this:

/*

// An MMOCharacter can:

// - perform its main skill

*/

public class MMOCharacter {

    public void skill(){

        // some code here

    }

}

Unfortunately, we have a problem. The fact that these characters gradually improve will require these classes to be modified during runtime.

We can’t keep recreating classes for every variant. Not only is this highly cumbersome; we also increase the odds of errors within our code if a variant doesn’t exactly behave as intended.

// (Don’t do this)

public class MMOCharacterLV5 {

    public void skill(){

        // some code here

    }

}

// (Don’t do this)

public class MMOCharacterLV510{

    public void skill(){

        // some code here

    }

    public void skill2(){

        // some code here

    }

}

And we also have some amount of character archetypes to implement as well. It appears that we should re-create our class for every archetype available. However, this isn’t a wise decision as well. This would be highly cumbersome as well - just like our earlier problem. We also increase the odds of running into code errors.

// (Don’t do this)

public class MMOCharacterKnight {

    public void attack(){

        // some code here

    }

}

// (Don’t do this)

public class MMOCharacterHealer {

    public void heal(){

        // some code here

    }

}

The solution to this problem is to apply the Decorator Pattern. Using Polymorphism, we can develop our data classes to allow data objects to be modified while the game is running.

To apply our pattern, we do it using the step-by-step procedure we’ve outlined earlier.

1) Create a general abstraction that covers ALL subclasses and variants.

Let’s recall the abstract form of our Decorator pattern:

/*

// DECORATOR IMPLEMENTATION:

// This abstract form has:

// - the signature for any common procedures,

//               algorithms, and traits common to ALL subclasses

*/

public abstract class DecorativeObject {

              // IN & OUT: (Your Choice)

              // (Implementation done by Subclasses)

    public void procedure() {

    }

              // (include any other common fields

              // and procedures as you wish)

}

This abstraction allows our data classes to progressively change even during runtime. Through polymorphism, we can swap our data classes to include additional functionality.

In our situation. our abstraction can be a generalized MMORPG character with a single skill and a few individual fields. However, because we will be using varied fields, abstract classes will be more suitable than interfaces. Hence, our abstraction will use abstract classes:

/*

// DECORATOR IMPLEMENTATION:

// Character abstraction with:

// -  a single skill

// - health points (int)

// - attack power (int)              */

public abstract class Character {

              // IN: - a Target Character

              // OUT: none

              // (Implementation done by Subclasses)

              abstract public void skill(Character target);

              public int hp;

              public int atk;

} 

2) Create the default subclass. This will directly extend your general abstraction from earlier.

Again, let’s recall the default subclass from our Decorator Pattern:

public class BaseObject : DecorativeObject {

              // Common Procedure, implemented as Base Object

              public void procedure() {

                                    base.procedure();

                            // (Implement this procedure here)

              }

              // (include any other fields

              // and procedures as you wish)

}

When a character is newly created, it will be an instance of our default class . Hence, it needs to be an extension of our main abstraction.

class DefaultChar : Character {

              // Common Procedure, implemented as Base Object

              override public void skill(Character target) {

        // include any code you want

              }

              // (include any other fields

              // and procedures as you wish)

    // CONSTRUCTOR:  

    public DefaultChar() {

    this.hp = 12;   

    this.atk = 1;       

    }       

} 

3) Create the decoration subclass. Like the default subclass, this will also directly extend your general abstraction.

This is the part that gives the Decorator Pattern its gradual upgradability and progression.

First, let’s recall the default Decoration class from the Decorator Pattern earlier:

public class Decoration : DecorativeObject{

              // Previously applied Decoration Instance added: 

              public DecorativeObject prevDeco;               // Common Procedure, implemented as Decoration

    // Includes any extra effects added by this Decoration

              public void procedure() {

        base.procedure();

        // (Implement this procedure here,

                            // Add anything else you’d like as well)

                            prevDeco.procedure();

              }

                  // CONSTRUCTOR:

                  public Decoration(DecorativeObject d) {

                  this.prevDeco = d;      

                  } 

    // (include any other fields

              // and procedures as you wish)

}

                  // CONSTRUCTOR:

                  public Decoration(DecorativeObject d) {

                  this.prevDeco = d;      

                  } 

              // (include any other fields

              // and procedures as you wish)

}

The Decoration class is also an abstraction, which generalizes every augmentation and decoration you’ll apply to your object.

So let’s apply this concept to our situation.

We need to create a generalization for every augmentation to our characters:

class Decoration : Character {

              // Common Procedure, implemented as Decoration

              override public void skill(Character target) {

        // (Implementation done by Subclasses)

        // include any other code you want

        prevDeco.skill(target);

              }

              // (include any other fields

              // and procedures as you wish)              

}

The next few steps give key functionality to the Decorator class

4) Make sure the decoration subclass contains the previous decoration or the  default class as one of its fields

Within your Decoration class, create a field that uses the abstraction as the data type. It’ll also help if you give the field a reasonable, relevant name. In our case, our abstraction is the abstract class Character:

class Decoration : Character {

    public Character prevDeco;              // (NEW LINE)

              // Common Procedure, implemented as Decoration

              override public void skill(Character target) {

        // (Implementation done by Subclasses)

        // include any other code you want

        prevDeco.skill(target);

              }

              // (include any other fields

              // and procedures as you wish)              

} 

To initialize this new field, it will be handled by the Constructor for the Decorator class. This is done in the next step.

5) Make sure the constructor for the decoration subclass inputs either a Decoration or the Base Object. Set this input as the previous decoration.

The input for the custom constructor will be the abstraction, just like the field created earlier. In our case, the input will be an instance of the Character class (which allows either other decorations or the default class as inputs).

Also, we’ll set the field that we’ve created from the previous step to the input from the Constructor.

Overall, the Decorator class should now look like this:

class Decoration : Character {

    public Character prevDeco;              // (NEW LINE)

              // Common Procedure, implemented as Decoration

              override public void skill(Character target) {

        // (Implementation done by Subclasses)

        // include any other code you want

        prevDeco.skill(target);

              }

              // (include any other fields

              // and procedures as you wish)              

    // (NEW LINES) : - - - - - -             

    // CONSTRUCTOR:

    public Decoration(Character c) {

    this.prevDeco = c;      

    }     

    // - - - - - - - - - - - - - - - -

} 

Next is the fun part.

6) Create the third-level decoration subclasses. These directly extend the Decoration class you’ve developed in previous steps.

We can start implementing the finer details outlined by our abstraction.

In MMORPG games, a great example of an object that would ‘decorate’ characters are weapons. Hence, we can start creating weapons and other equipment classes that are recursively attached to a base character.

We can also implement the method skill() to actually do something.  In our case, let’s have the skill() method attack a target.

This Greatsword class is an extension of the Decoration class we’ve developed earlier. It has all the fields and methods of the Decoration Class, plus its own unique traits.

class GreatSword : Decoration {

    // Weapon damage

    int damage = 3;

    // CONSTRUCTOR:

    // (use super() to implement this as its supertype)

    public GreatSword(Character c) : base(c){                        

    }

    // Common Procedure, implemented as GreatSword

    // (will be an Attack)

              override public void skill(Character target) {

        // ATTACK TARGET:

        target.hp -= damage;               

        prevDeco.skill(target);

              }

}

But why not have other weapons too? Let’s also design a Fiery Battle Axe. Like the GreatSword, it also has an attack as its skill() method.

class FieryBattleAxe : Decoration {

    // Weapon damage

    int damage = 2;

    int magicPower = 2;

    // CONSTRUCTOR:

    // (use super() to implement this as its supertype)

    public FieryBattleAxe(Character c) : base(c){

    }

    // Common Procedure, implemented as FieryBattleAxe

    // (will be an Attack)

              override public void skill(Character target) {

        // ATTACK TARGET:       

        target.hp -= damage + magicPower;               

        prevDeco.skill(target);

              }

}

While we’re at it, we can also create a Shield too:

class GoldenShield : Decoration {

    int armorBonus = 10;

    // CONSTRUCTOR:

    // (use super() to implement this as its supertype)

    public GoldenShield(Character c) : base(c){          

    } 

    // Common Procedure, implemented as GoldenShield

              override public void skill(Character target) {

        this.hp += armorBonus;       

        prevDeco.skill(target);

              }

}

Now that we have our classes in place, here is how the code would look like when run.

Creating a New Object:

To create a new character, you’ll set its data type as the abstract class but initialize it as the default class.

Character me = new DefaultChar();

Adding Decorations

To add decorations to a new character, you’ll simply re-initialize that character as a Decorator object with that same character as the input:

me = new GoldenShield(me);

You can even add more decorations simultaneously by creating a Decoration within a Decoration:

me = new GreatSword(new GoldenShield(me));

Using Common Procedures

When you make function calls to common procedures, ALL attached Decorators, as well as the Default object, will be called as well.

Let’s say the below line has just finished executing:

me = new GreatSword(new FieryBattleAxe(me));

In the second line below, we call the function skill(), targeting a character:

Character you = new DefaultChar();

me.skill(you);

What exactly would function skill() do in this situation? Well, let’s recall the code for skill() from one of the Decorator classes:

              override public void skill(Character target) {

        // ATTACK TARGET:       

        target.hp -= damage + magicPower;               

        prevDeco.skill(target);

              }

For each Decorator and Default Class, the function skill() would execute the original code from the class, then call skill() again for the next object.

And the next. This keeps occurring until skill() has been called for all attached Decorators, as well as the Default Class.

In the above code, because we’ve attached two Decorators to the original default class, skill() will execute for both of them. All function calls to skill() will have the original target as the input as well.

Character me = new GreatSword(new FieryBattleAxe(me));

Call to Skill, from object ‘me’:

- GreatSword.Skill() executes

- FieryBattleAxe.Skill() executes

- DefaultChar.Skill() executes

But what if a Default Character with no Decorator objects attached calls skill()?

Character you = new DefaultChar();

you.skill(me);

Because there aren’t any Decorators attached, only the Default class will have its skill() function called.

The Decorator Pattern in a Nutshell

Borrowing a few elements from other Design Patterns, the Decorator pattern is, indeed, one of the more complex patterns to implement.

Just understand its premise; it provides a way to dynamically enhance and augment objects during runtime. Because it’s one of the more essential design patterns to gaming and any other situations which require evolving data objects, implementing this pattern in a sound manner will be a great addition to your repertoire.

Chapter 7: The State Pattern

==== ==== ==== ==== ====

When creating data classes, all fields, methods, and other traits have distinct sets of values. Those values can be initialized when creating data objects. They can also be changed whenever necessary.

But whenever there’s a scenario in which a data object needs to change nearly all of its traits, we encounter a problem. There may be too many traits to change  one-by-one and there may be one too many errors that could emerge.

Therefore, the better way to approach this situation is to use class abstractions and polymorphism to simultaneously change the data object’s many traits.  If the data object consistently changes during runtime, then this approach becomes more appealing.

Essentially, this is the State Pattern in action - a data object that can change its traits during runtime, depending on external factors or anything else that requires a particular behaviour.

How it essentially works:

The data object will include one instance of an interchangeable state. There can be as many different interchangeable states as necessary.

If you change the state, you’ll change the traits and behaviours of the data object. You’ll usually do this to accommodate whatever situation your data class is in.

How the State Pattern differs from the Strategy Pattern:

Both the State and Strategy patterns implement design variants suitable for different scenarios. However, the main difference between them is the situational context.

The Strategy pattern offers different ways to process an algorithm. Its algorithm variants only apply once the procedure is called.

On the other hand, State pattern objects exist continuously during runtime. A change in the environment at any time can prompt a State pattern object to adapt.

Creating the State Pattern:

To implement this design pattern, follow these steps:

1) Identify which class will be the ‘handler’ class. A key part of the functionality from this class will depend on its current state.

2) Create the State abstraction. Define all common fields and procedures here.

3) Create all the different State Subclasses. Implement where necessary

4) Make the Handler include an instance of its current state. Its data type should be the Abstract Class. When initialized with a constructor, the Handler should have a default state.

5) Develop the state-changing methods within the Handler class. There should be a toggling method and a set method.

6) Apply all other code that utilizes the various States the Handler depends on.

Overall, here is the UML Diagram for the State Pattern:

![](Image00009.jpg)

The State pattern is perhaps one of the more frequently used design patterns in existence. If implemented properly, the State pattern will give your data objects a keen sense of adaptability.

Now we’ll explore the code that the State pattern consists of.

C#-7a: The State Pattern, in C#

==== ==== ==== ==== ====

Here is how the State Pattern looks like in C#

First, we start with the Handler Class. This contains a property which can be transformed into distinct states - a scenario suitable for the State Pattern.

/*

// The Handler Class has:

// - an instance of a transforming state class

// Insert any other fields or methods as you wish

*/

class Handler {

    AbstractState currentState;

              /*

        // SIMPLE IMPLEMENTATION:

        // (Toggle currentState into the Next State

        //    via IF-ELSE statements)

        // - make sure to cover all states available

        // - re-implement if necessary       

              */  

void toggleState() {

        if (currentState is StateOne) {

            currentState = new StateTwo();

        }

        if (currentState is StateTwo) {

            currentState = new StateN();

        }

        if (currentState is StateN) {

            currentState = new StateOne();

        }

    }

    void setState(AbstractState input) {

        this.currentState = input;       

    }

    // CONSTRUCTOR:

    public Handler() {

        this.currentState = new StateOne();

    }

}

Next is the State Abstraction. This will be a superclass common to the different states that your handler contains.

class AbstractState {

    String commonField;

    // IN & OUT: (your choice)

    // EFFECT: (your choice)

    public void commonProcedure() {    

         // (add any implementation here)  

    }

    // (add any other fields and methods

    // as you wish)   

}

And lastly, we implement the state subclasses. They are implemented uniquely; their common fields are distinct and their common procedures can be implemented in their own unique ways.

For our generalized version, we’ll have three different states. When applying the State pattern in your code, you may have as many states as you need.

class StateOne : AbstractState {

    String commonField = "ONE";

    // Subclass implementation of

    // commonProcedure()

    // (contains all traits of superclass version,

    // plus any extra effects by subclasses)

    public void commonProcedure(){

        base.commonProcedure();       

        // (add any extra implementation here)

    }

}

class StateTwo : AbstractState {

    String commonField = "TWO";       

    public void commonProcedure(){

        base.commonProcedure();       

        // (add any extra implementation here)

    }   

}

class StateN : AbstractState {

    String commonField = "N";   

    public void commonProcedure(){

        base.commonProcedure();

        // (add any extra implementation here)

    }   

}

C#-7b: Applying The State Pattern

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

Here, we’ll encounter a situation which requires us to apply the State Pattern.

Transformers

Let’s say you’re writing code for a state-of-the-art transforming vehicle.

/*

// A Transformer Mech currently has:

// - a location (in coordinates)

// It can:

// - fire its main weapon

// - move its physical location

*/

class TransformerMech {

    // Coordinates

    Coordinates location;

    public void fireMainWeapon(Coordinates target) {} 

    public void move(double degrees) {}

}

Your code also contains X-Y-Z coordinates in the form of a data class as well:

/*

// Coordinates have:

// - longitude and latitude;

// - height, as meters above current ground level

*/

class Coordinates {

    double lat, longt, height;   

    // CONSTRUCTOR:

    public Coordinates(double lat, double longt, double height){

        this.lat = lat;

        this.longt = longt;

        this.height = height;

    }       }

A Transformer Mech’s ability to move and fire its weapon will depend on what state it’s in. As a bipedal robot, it can move modestly, but it doesn’t have a main weapon. As a tank, it can move faster, have a higher armor rating, and use a standard weapon. As an immobile cannon, it will have an extremely powerful weapon at the cost of its movement ability. And as an airborne flyer, it can move extremely fast in all directions.

Clearly, this situation will require the State Pattern. So let’s apply it step-by-step.

1) Identify which class will be the ‘handler’ class. A key part of the functionality from this class will depend on its current state.

The TransformerMech class will be the ‘handler’ class. Thus, we’ll implement it in a way that utilizes its ever-changing current state.

2) Create the State abstraction. Define all common fields and procedures here.

The abstract form of your various States will include ALL fields and procedures that each one of your states share.

Earlier, we’ve described the various traits that our Transformer Mech will have: some main weapon and a movement ability. Our main weapon has a damage output rating and a firepower rating.

Let’s also include some form of armor to mitigate attacks. So overall, our Mech will have all of these traits, but their values vary depending on the ‘State’ our Mech is in.

Hence, here is what our abstract class can look like:

abstract class AbstractMode {

    public int firePower;

    public double firingRate;

    public int moveSpeed; 

    public int armor;

}

Now we can start developing the different States our Mech can take.

3) Create all the different State Subclasses. Implement where necessary.

We’ve described four different states for our Transformer Mech earlier. The first  state is a bipedal robot with no main weapons and a relatively slower movement speed (it runs to move).

Hence, the State class will look like this:

class RobotMode: AbstractMode {

    // CONSTRUCTOR:

    public RobotMode(){

            this.firePower = 0;

            this.firingRate = 0;

            this.moveSpeed = 10;

            this.armor = 10;

    }   

}

The next State we’ve described is a tank with a main weapon with reasonably fair damage and fire rate, as well as a high armor rating. Its State class will look like this:

class TankMode: AbstractMode {   

    // CONSTRUCTOR:

    public TankMode(){

            this.firePower = 25;

            this.firingRate = 0.75;

            this.moveSpeed = 50;

            this.armor = 50;

    }

}

The third State is an immobile cannon. It has a highly powerful yet slow main weapon. It also has a moderate armor rating. This is what its State class will look like:

class BlasterCannonMode: AbstractMode {      

    // CONSTRUCTOR:

    public BlasterCannonMode(){

            this.firePower = 180;

            this.firingRate = 5.0;

            this.moveSpeed = 0;

            this.armor = 30;

    }

}

And lastly, the Flight State gives the Transformer Mech the ability to fly. Its weapon will have a modest firepower rating but with a high rate of fire.

class FlightMode: AbstractMode {       

    // CONSTRUCTOR:

    public FlightMode(){

            this.firePower = 15;

            this.firingRate = 0.5;

            this.moveSpeed = 105;

            this.armor = 20;       

    }              }

Now that we’ve implemented our different states, we can now integrate them into our Transformer mech in the next step.

4) Make the Handler include an instance of its current state. Its data type should be the Abstract Class. When initialized with a constructor, the Handler should have a default state.

To integrate our various, interchangeable States onto our Transformer Mech, we do two things. The first is to include the current State into our Mech class as a field. Afterwards, we need to initialize this field somehow. The best way to do it is within the Constructor; one of its inputs can be the default state for a Transformer Mech.

class TransformerMech {

    // Coordinates

    Coordinates location;

    // Field for Current State:

    AbstractMode currentMode; // NEW LINE

    void fireMainWeapon(Coordinates target) {} 

   void move(double degrees) {  }

    // NEW LINES: - - - - - -

    // CONSTRUCTOR:

    public TransformerMech(Coordinates c, AbstractMode am) {

        this.location = c;

        this.currentMode = am;

    } 

    // - - - - - - - - - - - -

}

5) Develop the state-changing methods within the Handler class. There should be a toggling method and a set method.

We now need to create the mechanism to change the Mech’s States.

The first method is a simple setter; it switches the Mech’s State to whatever input has been given. Just insert this code inside the TransformerMech class:

    // NEW LINES: - - - - - -     

    // IN: a State

    // OUT: none

    // EFFECT: set Mech's State to the input

    void setMode(AbstractMode s) {

        this.currentMode = s;

    }

    // - - - - - - - - - - - -

The next method to create is a toggle method to change the Mech’s State to the next one This method is optional in most cases, but sometimes it will come in handy. Again, insert this code inside the TransformerMech class:

// NEW LINES: - - - - - -    

    // IN & OUT: none

    // EFFECT: toggle Mech's state to the next one

    public void toggleMode() {

        if (currentMode is RobotMode)

            currentMode = new TankMode();

        if (currentMode is TankMode)

            currentMode = new BlasterCannonMode();

        if (currentMode is BlasterCannonMode)

            currentMode = new FlightMode(); 

        if (currentMode is FlightMode)

            currentMode = new RobotMode();         

    }

    // - - - - - - - - - - - -  

6) Apply all other code that utilizes the various States that the Handler depends on.

Our Transformer Mech has methods that utilize properties from our State classes.

One of the Mech’s methods fires its main weapon at a given target. How this procedure is executed depends on the firepower, firing rate, and movement speed of our Transformer’s current state. It uses  local variables that get its data from whichever state our Mech is in.

Within the Transformer Mech class, replace the empty fireMainWeapon() method with the code below:

(For simplicity’s sake, we can forego the full implementation for now. Comments will describe what it would do.) 

    // UPDATED LINES: -

public void fireMainWeapon(Coordinates target) {

        int damage = currentMode.firePower;

        double cooldown = currentMode.firingRate;

        double timer = 0;

        /*

        // (some other code that:

        // - deals damage to the target

        // - increments the timer from 0 to the cooldown time

        // - if timer reaches the cooldown time,

        //      weapon can fire at the target again

        */

    } 

The method move() also depends on the Transformer Mech’s current state. The Mech’s speed will depend on whichever mode it is currently set to. 

Within the Transformer Mech class, replace the empty move() method with the code below:

(Again, for simplicity’s sake, we can forego the full implementation for now) 

    // UPDATED LINES: -

    public void move(double degrees, double dist) {

        int speed = currentMode.moveSpeed;

        /*

        // some other code that

        // moves this Transformer Mech

        // in the given direction (degrees)

        // until it reaches the given distance (dist).

        //

        // The Transformer Mech will move

        // at its move speed,

        // which depends on its current state

        */   

    }

Trying out the State Pattern Functionality

Now let’s utilize the code we’ve written. Place all the following code within the main() method.

Let’s say we’re planning to deploy a few Mechs to defend New York City from some alien invasion. We’ll have a couple of Mechs in robot mode accompanied with one in tank mode patrolling Westside Manhattan:

        TransformerMech p1tm1 = new TransformerMech(

            new Coordinates(40.7615576,-73.9940587,0), new RobotMode());

        TransformerMech p1tm2 = new TransformerMech(

            new Coordinates(40.7623624,-73.9939141,0), new RobotMode());

        TransformerMech p1tm3 = new TransformerMech(

            new Coordinates(40.7617993,-73.9933656,0), new TankMode());

We’ll also have a blaster cannon stationed at the east side, along with two Mechs in Flight Mode around the perimeters:

        TransformerMech p2tm1 = new TransformerMech(

   new Coordinates(40.7720871,-73.963746, 0), new BlasterCannonMode());

        TransformerMech p2tm2 = new TransformerMech(

            new Coordinates(40.7549617,-73.9696583,8180), new FlightMode());

        TransformerMech p2tm3 = new TransformerMech(

            new Coordinates(40.7483817,-73.9792723,7990), new FlightMode());

If we want to reassign Mechs to take on different combat roles and States, we can easily do so.

For example, let’s get the first group to be air scouts instead of a ground patrol. Let’s also spread them out location-wise to cover a larger area of Manhattan:

        p1tm1.setMode(new FlightMode());

        p1tm1.move(26.6, 0.00036);

        p1tm2.setMode(new FlightMode());

        p1tm2.move(-94.3, 0.000012);

        p1tm3.setMode(new FlightMode());   

        p1tm3.move(132, 0.00045);

Next, suppose the second group received coordinates to an enemy alien mothership north of Manhattan. They’ve been tasked to eliminate it as quickly as possible.

        Coordinates enemyMothership = new

            Coordinates(40.8877895, -73.8721194, 10000);

To execute the order, the second group would quickly fly closer to the enemy mothership. But first, one of the mechs will have to transform to flight mode:

       p2tm1.setMode(new FlightMode());

They will then move towards the mothership…

        p2tm1.move(15.6, 0.00063);

        p2tm2.move(15.6, 0.00064);       

        p2tm2.move(15.6, 0.00062);

… change their states, unloading their most powerful main weapons…

        p2tm1.setMode(new BlasterCannonMode());

        p2tm2.setMode(new BlasterCannonMode());      

        p2tm2.setMode(new BlasterCannonMode());       

… and, finally,  open fire at the enemy threat.

        p2tm1.fireMainWeapon(enemyMothership);       

        p2tm2.fireMainWeapon(enemyMothership);

        p2tm3.fireMainWeapon(enemyMothership);

In summary, the State Pattern allows an immense amount of versatility during runtime. When you encounter scenarios which require consistently malleable data objects, use the State Pattern.

Chapter 8: The Facade Pattern

==== ==== ==== ==== ====

If you’ve ever driven a car before, you would know how simple it is to operate it. Starting the car would take a twist of your keys in the ignition (or nowadays, a press of a button). To go faster, you would press the gas pedal. To slow or stop, you would press the brake pedal. And the steering wheel has an obvious function.

But a car is also a very complex system. Starting a car would require ample power from the battery. Afterwards, it would require enough gasoline from the tank. The spark plugs need to be functional as well. There has to be enough fresh engine oil to move the car engine pistons and other parts. There’s also other things that have yet to be mentioned - and this differs from car to car. If everything is okay, the spark plugs ignite the engine cylinders and create enough  energy in the engine to propel the car.

Also, steering, accelerating, and braking each require a system of components to work together in unison. But we often don’t think about this because, from the driver’s seat, we can only the components visible to us. In other words, a Facade.

How the Facade Pattern Works:

The Facade Pattern gives you a top-level component that oversees the functionality of a complex subsystem. To operate the subsystem, you would only need to do it through the Facade Pattern. The result is a far more simple system where you only need to access the Facade Pattern for functionality.

Looking back at our car analogy, its provided interface in the driver’s seat is Facade pattern; it lets the driver control the system with a set of simple gestures. Meanwhile, it coordinates a complex system of components in response to the driver’s commands.

Creating the Facade Pattern:

To implement this design pattern, first identify the Major Procedures and/or Behaviours we want to simplify.

If using an interface, follow these steps:

1) Create the Facade interface that contains those major procedures

2) Create the general client class that implements the Facade interface

3) The general client should implement ALL the major procedures. Contain as many component instances as necessary.

4) If necessary, you may create multiple Facade interfaces and client classes. If so, repeat steps 1 to 3.

5) Create subclasses for the general client classes whenever necessary. Any code that accesses the system does it as a client subclass.

If using an encompassing class, follow these steps instead:

1) Create the general “Facade” class. This class should implement ALL the Major Procedures mentioned earlier. Contain as many component instances as necessary.

2) Create a general client class. It should contain an instance of the Facade class.

3) If necessary, you may create multiple Facade classes and repeat steps 1 &2.

4) Create subclasses for the general client class whenever necessary. Any code that accesses the system does it through the Facade class within the client subclasses.

Whichever steps you take depends on the situation you encounter. So you’ll have to judge whether it’s better to have one encompassing ‘Facade’ wrapper class.

If you implement the Facade Pattern as a single wrapper class, the UML diagram would look like this:

![](Image00010.jpg)

If, instead, you implement the Facade Pattern as an interface, the UML diagram would look like this:

![](Image00011.jpg)

C#-8a: The Facade Pattern, in C#

==== ==== ==== ==== ====

To first understand the Facade Pattern, we must first look at its environment. The key thing to notice is a collection of components that compose a very complex system.

Here is an example of a component class that contains multiple sub-components. Its methods may also depend on its sub-components.

/*

// Component Class, with Sub-Components

// Methods:

// - one method which accesses the subcomponents

*/

class ComponentOne {

    SubcompOneOne sc11 = new SubcompOneOne();

    SubcompOneTwo sc12 = new SubcompOneTwo();   

    // IN & OUT: (your choice)

    // EFFECT: (your choice)

    public void distinctMethodOne() {

        sc11.distinctMethodOneOne();

        sc12.distinctMethodOneTwo();

    }   

}

class SubcompOneOne {

    // IN & OUT: (your choice)

    // EFFECT: (your choice)

    public void distinctMethodOneOne() {

     }   

}

class SubcompOneTwo {

    // IN & OUT: (your choice)

    // EFFECT: (your choice)

    public void distinctMethodOneTwo() {

   }   

}

Here are examples of two other components within the environment:

class ComponentTwo {

    // IN & OUT: (your choice)

    // EFFECT: (your choice)

    public void distinctMethodTwo() {

                      // (add implementation here)

    }   

}

class ComponentN {

    // IN & OUT: (your choice)

    // EFFECT: (your choice)

    public void distinctMethodN() {

                      // (add implementation here)       

    }   

}

In this system, we need to coordinate all the components together.

Hence, here is how the Facade Pattern would be implemented in C#. If the Facade would be implemented as an interface, it would look like so:

/*

// Facade as an Interface

// (include all major procedures that utilize

//               components within the environment)

*/

interface Facade{

    // MAJOR PROCEDURES:

    // IN & OUT: (your choice)

    // EFFECT: (your choice)

    //              - calls methods from all system components

    void activateA();

    void activateB();

}

/*

// Client Classes

// (Implement all procedures defined within

//               the Facade interface)

*/

class Client : Facade {

    ComponentOne c1 = new ComponentOne();

    ComponentTwo c2 = new ComponentTwo();

    ComponentN cN = new ComponentN();

    // Methods from Facade Interface:

    void Facade.activateA() {

        c1.distinctMethodOne();

    }

    void Facade.activateB() {

        c2.distinctMethodTwo();

        cN.distinctMethodN();

    }

}

In this case, Client classes would then implement the interface:

// Client Subclasses:

// (add whenever necessary)

class ClientA : Client {

}

class ClientB : Client {

}

If the Facade would be implemented as a large superclass instead, it would look like this:

/*

// Facade as a major Class

// - include instances for each component

//               in the environment

// - include all major procedures that utilize

//               components within the environment

*/

class Facade{

    ComponentOne c1 = new ComponentOne();

    ComponentTwo c2 = new ComponentTwo();

              …

    ComponentN cN = new ComponentN(); 

    // MAJOR PROCEDURES:

    // IN & OUT: (your choice)

    // EFFECT: (your choice)

    public void activateA() {

        c1.distinctMethodOne();

    }

    public void activateB() {

        c2.distinctMethodTwo();

        cN.distinctMethodN();

    }

}

In this case, Client classes would have an instance of the Facade class:

// Client Class:

// (rest of software accesses)

class Client {

    Facade f = new Facade();

}

// Client Subclasses:

// (add whenever necessary)

class ClientA extends Client{}

class ClientB extends Client{}

C#-8b: Applying The Facade Pattern

Use an IDE of your choice for the code below. Online IDE’s, such as [codechef.com](http://codechef.com) , [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) are a great choice.

========================= ======

In this chapter, we encounter a scenario which requires the Facade pattern implementation.

Galactic Starship with Warp Drive

Here, we have a small chunk of code from a Galactic Starship system. Each class partly manages the corresponding starship hardware components.

/*

// GALACTIC STARSHIP GSX2013-A4

// Components listed:

// - Positron Engine

// - Ignition Crystal

// - Dark Matter Drive

// - Energy Pre-Igniter

// - Matter Fusion Reactor

// - Warp Drive

// - Galactic Navigation

// - Co-ordinates

// - Warp Igniter

*/

class PositronEngine {

    IgnitionCrystal igc = new IgnitionCrystal();

    DarkMatterDrive dmd = new DarkMatterDrive();

    public void startEngine() {

        igc.lightUp();

        dmd.activate();

    }

}

class IgnitionCrystal {

    public void lightUp() {

        // (some hardware implementation here)       

    }

}

class DarkMatterDrive {

    EnergyPreIgniter epi = new EnergyPreIgniter();

    MatterFusionReactor mfr = new MatterFusionReactor();

    public void activate() {

        epi.ignite();

        mfr.fuse();

    }

}

class EnergyPreIgniter {

    public void ignite(){      

        // (some hardware implementation here)       

    }

}

class MatterFusionReactor {

    public void fuse() {

        // (some hardware implementation here)

    }

}

class WarpDrive {

    WarpIgniter wi = new WarpIgniter();

    MatterFusionReactor mfr = new MatterFusionReactor();   

    public void warpTo(Coordinates c) {

        wi.activate();

        mfr.fuse();       

        // (warp Starship to given location)

    }

}

// NOTE:: make sure the line ‘using System.Collections;’

//                             is near the top of your code

class GalacticNavigation {

    ArrayList points = new ArrayList();

}

class Coordinates {

    int x, y, z;   

    public Coordinates(int x, int y, int z) {

        this.x = x;

        this.y = y;

        this.z = z;

    }

}

class WarpIgniter {

    public void activate() {

        // (some hardware implementation here)

    }  

}

Clearly, this is still a very complex system even though we only have a handful of its components.

But let’s say we’ve been given the task to coordinate these components for a couple of important tasks: starting the main engine and activating the warp drive. We clearly have to simplify these tasks under a common handle.

Hence, we apply the Facade pattern.

Identify the Major Procedures

Given the handful of classes from earlier, our task is to implement the following procedures:

- starting the main engine

- activating the warp drive

We then select an approach for implementing the Facade pattern. For now we’ll apply it as one encompassing Facade wrapper class.

1) Create the general “Facade” class….

We start by creating the Facade Wrapper class, as seen below:

    class Facade {  

    }

This class should implement ALL the Major Procedures mentioned earlier.

    class Facade {  

        // NEW LINES:

        // MAJOR PROCEDURES:

        public void startEngine(){

            pe.startEngine();

            // (rest of implementation)

        }

        public void activateWarpDrive(){

            wd.warpTo(new Coordinates(0, 0, 0));

            // (rest of implementation)

        }

        }

    }

Contain as many component instances as necessary.

This is normally the tricky part of the process. We only have to include instances from the key classes contributing to the major procedures.

If we take a close look at the code, we realize that some components rely on other components in order to function. When mapped out, it would look like so:

PositronEngine relies on:

              -> IgnitionCrystal

              -> DarkMatterDrive (relies on:)

                            - -> EnergyPreIgniter

                            - -> MatterFusionReactor

WarpDrive relies on:

              -> WarpIgniter

              -> MatterFusionReactor

From looking at the code, the PositronEngine and WarpDrive classes seem to have instances of relevant classes or have some sort of reliance on them.

Hence, we would need instances for these two classes. The rest would be linked to them somehow.

    class Facade {

        // NEW LINES:

        PositronEngine pe = new PositronEngine();

        WarpDrive wd = new WarpDrive();

        // MAJOR PROCEDURES:

        public void startEngine(){

            pe.startEngine();

            // (rest of implementation)

        }

        public void activateWarpDrive(){

            wd.warpTo(new Coordinates(0, 0, 0));

            // (rest of implementation)

        } 

    }

2) Create a general client class. It should contain an instance of the Facade class.

The generalization for the Client class is quite simple. It’s simply a class with a Facade instance within it:

    // Client Class:

    // (rest of software accesses this)

    class Client {

        Facade f = new Facade();

    }

Hence, to access the system’s functionality, we would only need to access the Client Class and its underlying facade:

        Client c = new Client();

        // Starting Engine:

        c.f.startEngine();

        // Activating Warp Drive:

        c.f.activateWarpDrive();

4) Create subclasses for the general client class whenever necessary.

You have the option to further develop your client classes by creating specialized subclasses and more.

// Client Subclasses:

// (add whenever necessary)

class ClientA: Client {

}

class ClientB: Client {

}

If you do, your client subclasses would access the Facade procedures similar to the general client:

        Client ca = new ClientA();

        Client cb = new ClientB();

        // Starting Engine:

        ca.f.startEngine();

        cb.f.startEngine();       

        // Activating Warp Drive:

        ca.f.activateWarpDrive();

        cb.f.activateWarpDrive(); 

Overall, we now see how the Facade Pattern would provide a simple nexus for functionality. When facing a similar scenario, consider applying this pattern.

IF MULTIPLE FACADES:

If the procedure leads you to create multiple facades, then it may be worth exploring that option. If our example scenario was a situation where we would use more than one facade, here is what it would look like:

    class EngineFacade {

        PositronEngine pe = new PositronEngine();

        // MAJOR PROCEDURES:

        public void startEngine(){

            pe.startEngine();

            // (rest of implementation)

        }       

    }

    class WarpDriveFacade {

        WarpDrive wd = new WarpDrive();

        // MAJOR PROCEDURES:

        public void activateWarpDrive(){

            wd.warpTo(new Coordinates(0, 0, 0));

            // (rest of implementation)

        }

    }

The general Client class would then reflect this alternate scenario:

    // Client Class:

    // (rest of software accesses this)

    class Client {

        EngineFacade ef = new EngineFacade();

        WarpDriveFacade wdf = new WarpDriveFacade();

    }

Archive A1: Factory Pattern Implementation

Use the pseudocode below to implement the Factory Pattern in a programming language of your choice.

==== ==== ==== ==== ====

// Factory is implemented by any subclasses that need to use it

interface Factory {             

              // INPUT: your choice

              // OUTPUT: your choice

              // Constructor for Classes that implement this interface

              function CreateObject(<any inputs here>) {

              // any code here             

              }

}

// SubFactory1:

// creates distinct objects based on Factory Interface

class SubFactory1 implements Factory {

              // This implements the same function outlined in the interface

              function CreateObject(<any inputs here>) {             

              // include ANY unique distinctions for this creator class

              // any other code here

              }

}

// SubFactory2:

// creates distinct objects based on Factory Interface

class SubFactory2 implements Factory {

              // This implements the same function outlined in the interface             

              function CreateObject(<any inputs here>) {             

              // include ANY unique distinctions for this creator class

              // any other code here

              }

}

Archive A2: Composite Pattern Implementation

Use the pseudocode below to implement the Factory Pattern in a programming language of your choice.

==== ==== ==== ==== ====

// Component is the superclass which File and Folder classes extend

// You may define any fields and methods shared by both subclasses

high class Component {

    // insert any amount of fields and methods

    // where necessary

    String someField;

    public void someMethod()

}

// General Item Class (as File):

// contains all fields and methods defined at Component

class File extends Component {

}

// General Group Class (as Folder):

// contains all fields and methods defined at Component

// Also has:

// - a List of Components, which can contain either Items or Groups

class Folder extends Component {

   contents = new List

}

Archive A3: Observer Pattern Implementation

Use the pseudocode below to implement the Observer Pattern in a programming language of your choice.

==== ==== ==== ==== ====

The first is the Observing pair, including the class and interface.

// All Observing Classes implement an Observer abstraction

// It can:

// - update object data based on subjects

abstract class Observer {         

    update()

    // enter any other methods here

}

// Observing Classes have:

// - working version of the update() method

// - any number of additional fields & methods

// Observing Classes may need a List of Subjects to access

class ObservingClass extends Observer {

     // enter any key fields here

     List of Subjects;

    // INPUT: (optional)

    // OUTPUT: none

    // EFFECT: updates data in response to subject

    public void update() {

    // make any changes to observer's key fields here

    }

}

Next is the Subject pair, including the class and interface.

// All Subject Classes implement a Subject abstraction

// It can:

// - notify observers

// - add/remove observers in its update list

// Subject Classes also need a List of Observers to Update

abstract class Subject {

              notifyObservers()

              addObs(Observer o)

              deleteObs(Observer o)

    // enter any other methods here

}

// Subject Classes have:

// - a List of Observers to notify

// - a working version of notifyObservers()

// - any number of additional fields & methods

// Subject Classes also need a List of Observers to Update

// (added on Subject Class)

class SubjectClass extends Subject {

     // enter any key fields here

   obs = List of Observers

    // INPUT: (optional)

    // OUTPUT: none

    // EFFECT: updates all observers in list of any changes

    public void notifyObservers(){

        for each item in obs: update()             

        }

    // Add/Delete Methods:

    // INPUT: - an Observer

    // OUTPUT: none

    // EFFECT: updates data in response to subject   

    public void addObs(Observer o)

    public void deleteObs(Observer o)

}

Archive A4: Singleton Pattern Implementation

Use the pseudocode below to implement the Single Pattern in a programming language of your choice.

==== ==== ==== ==== ====

// A Singleton Class has:

// - A Singleton Instance

// - any other Fields you need

//

// it can NOT:

// - be instantiated as normal (as if it were a regular class)

// (The constructor is set to Private, just to be sure)

//

// It can:

// - return the ONLY singleton class instance

class Singleton

    // CONSTRUCTOR:

    // - set to PRIVATE; cannot be accessed outside the class

    private Singleton()

    // The Only Singleton Object:

    // - set to PRIVATE; cannot be accessed outside the class  

    // - set to null by default; assigned to Object with call to getObject()

    private static object = null

    // INPUT: (your choice)

    // OUTPUT: A Singleton Object

    // EFFECT: Returns the ONLY singleton object.

    // Creates one if nonexistent.

    // - set to STATIC; will not require an Object to call this method

    public static synchronized Singleton getObject():

        if (object == null) {

            object = new Singleton()

            // Initialize any other fields here

        }

        return object

    }

}

Archive A5: Strategy Pattern Implementation

Use the pseudocode below to implement the Strategy Pattern in a programming language of your choice.

==== ==== ==== ==== ====

// ABSTRACT STRATEGY IMPLEMENTATION:

// This has:

// - the signature for the abstract algorithm

AbstractStrategy {

        IN: (Your Choice)

       OUT: (Your Choice)

        (effect based on Subclass level)

        void Algorithm();

    }

CLASSES FOR EACH STRATEGY:

Use any amount of needed classes based on the Abstract Strategy

Each Class can:

- implement the Abstract Algorithm

(based on the unique strategy from each class)

class Strategy1, extension of AbstractStrategy{

        Abstract Algorithm, as Strategy1:   

        Algorithm() {

               ( Implement this algorithm uniquely )

        }

    }

…

class StrategyN, extension of AbstractStrategy{

        Abstract Algorithm, as StrategyN:   

        Algorithm() {

               ( Implement this algorithm uniquely )

        }

    }

Archive A6: Decorator Pattern Implementation

Use the pseudocode below to implement the Decorator Pattern in a programming language of your choice.

==== ==== ==== ==== ====

DECORATOR IMPLEMENTATION:

This abstract form has:

- the signature for any common procedures,

              algorithms, and traits common to ALL subclasses

abstract class DecorativeObject {

              IN & OUT: (Your Choice)

              (Implementation done by Subclasses)

              procedure()

              (any other common fields

              and procedures)

}

class BaseObject, extension of DecorativeObject {

              Common Procedure, implemented as Base Object:

              procedure() {

                                   (Implement this procedure here)

              }

              (any other common fields

              and procedures)

}

class Decoration, extension of DecorativeObject{

              Previously applied Decoration Instance added: 

              - DecorativeObject prevDeco;              

              ( Common Procedure, implemented as Decoration

                  Includes any extra effects added by this Decoration )

              procedure() {

                                    (Implement this procedure here,

                            Add anything else you’d like as well)

                            prevDeco’s procedure()

              }

              CONSTRUCTOR:

                  Decoration(DecorativeObject d) {

                  this.prevDeco = d;      

                  } 

              (any other common fields

              and procedures)

}

class DecorationOne, extension of Decoration{

              ( Common Procedure, implemented as DecorationOne )

              (also implements procedure() as its superclass)

              procedure() {

                                    Decoration Superclass’s procedure();    

                            // (Implement this procedure here)     

              }

              (any other common fields

              and procedures)

              (SAME CONSTRUCTOR AS SUPERCLASS DECORATION)   

}

class DecorationX, extension of Decoration{

              ( Common Procedure, implemented as DecorationX )

              (also implements procedure() as its superclass)

              procedure() {

                                    Decoration Superclass’s procedure();    

                            // (Implement this procedure here)     

              }

              (any other common fields

              and procedures)

              (SAME CONSTRUCTOR AS SUPERCLASS DECORATION)   

}

Archive A7: State Pattern Implementation

Use the pseudocode below to implement the  State Pattern in a programming language of your choice.

==== ==== ==== ==== ====

The Handler Class has:

- the current state: an instance of a transforming state class

              (Insert any other fields or methods as you wish)

Included methods:

- toggleState()

- setState()

- Constructor

  toggleState():

        SIMPLE IMPLEMENTATION:

       (Toggle currentState into the Next State

                      via IF-ELSE statements)

         - make sure to cover all states available

         - re-implement if necessary

        if currentState is StateOne,

            currentState = new StateTwo()

        if currentState is StateTwo,

            currentState = new StateN()

        if currentState is StateN:

            currentState = new StateOne()

setState(input):

        this.currentState = input;       

     CONSTRUCTOR:

    Handler():

        this.currentState = new StateOne()

AbstractState Class has:

- common fields of your choice

Included Methods:

- (your choice)

    IN & OUT: (your choice)

    EFFECT: (your choice)

    commonProcedure() :

       (add any desired implementation)

Subclasses for AbstractState:

Each has:

- distinct values for common fields

-      any extra fields wherever necessary

-       

Each common method implementation contains:

- all traits of superclass version,

- any extra effects by subclasses

StateOne, StateTwo, StateN are subclasses of AbstractState

Archive A8: Facade Pattern Implementation

Use the pseudocode below to implement the Facade Pattern in a programming language of your choice.

==== ==== ==== ==== ====

Subsystem:

The Subsystem contains:

- a collection of interconnected classes (components)

- class hierarchies and containment may vary

FACADE, AS WRAPPPING CLASS:

The Facade Class has:

- an instance of any major component class from the subsystem

Included Methods:

- every major procedure that utilizes the subsystem components

CLIENT CLASS:

The Client class has:

- an instance of the Facade Class

FACADE, AS INTERFACE:

The Facade Interface has:

- every major procedure that utilizes the subsystem components

CLIENT CLASS, IMPLEMENTS FACADE:

The Client class has:

- an instance of any major component class from the subsystem

Included Methods:

- same as Facade Interface, but fully implemented

EASIEST WAY TO LEARN C#, Part 1

We’ve included a complementary guide to learning programming essentials and to help you become a better programmer.

As a way to help you understand it much more easily, we’ve set it up as simple as possible.

To easily run code, select an IDE (Integrated Development Environment: essentially somewhere that you write and run code) of your choice. You may also use online IDE’s such as [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) .

========================= ======

Prelude: Structure of a C# File

Below are the major components of a C# code file. If you were to start a fresh new C# project, it’s best to copy-paste the code below and start from there.

using System;                            // A)

using System.Collections.Generic;

using System.Linq;

using System.Text.RegularExpressions;

// ADD MORE LIBRARIES HERE

namespace ___ {

              // ADD CLASSES HERE

    public class Program {                                          // B)

        public static void Main(string[] args) {                            // C

           // ADD MAIN CODE HERE              // D

        }

    }

// E

}     

    }

}

Explaining the Parts:

A) Import Statements: These lines of code instruct the computer to include libraries - existing data, pre-written code, and more tools created elsewhere. You can also import code from other C# files. These are best placed as the first lines of code within your file.

NOTE: at the very least, you need to have the four lines of code above in your C# files. These import the most essential C# libraries for use in your code today.

B) The Main Class: Your code file needs to have at least one Class. At least one of all your classes also needs the main() method included (see below).

C) The main() method: This is called the Entry Point. The computer will execute all code within your main() method. Among all classes in your C# project, you need to have at least one Class Method named main(). For now, make sure you have the exact line as above for your main() method.

D) main() method Code: This is the code that the computer will actually execute. If any of the code refers to other classes, libraries, functions, or any other code that it can reach, it will be included.

E) White Space: In a C# file, you can only include either Import Statements, Classes, Interfaces, or Enumerations.

1) The Basic Data Types.

Booleans:

These are essentially on-off switch values. In code, boolean values are going to be either true or false.

In C#, booleans can only be in lower-case (i.e. true, false). Booleans cannot have any upper-case letters in them (i.e. TRUE, True)

Examples:

true, false

Strings:

These are sets of keyboard characters - including letters, numbers, and other symbols - arranged in some order to make a text phrase. They start and end with double quotation marks.

Examples:

" This is a String. "

" This 15 4 &^%$! 5tring t00\. "

Integers:

They’re exactly as they’re defined - whole numbers without any fractions or decimals. Here are some examples:

12

143

19999932

Floats: also called floating-point numbers, they represent the opposite of Integers - they are numbers beyond the decimal point.

In C#, floats have the letter ‘f’ immediately following the number.

Example:

0.12f

.12f

In C#, you can also represent decimal numbers as the type Double. They won’t have the letter ‘f’ in them.

Example:

0.12

.12

2) Variables

Remember in grade school math where you used letters such as X and Y to represent numbers? Textbooks had phrases such as ‘let x = 4’ and ‘let y = 19’. These were called variables.

Variables prevalently exist in programming too. But in programming, you can give your variables a name. And instead of numbers, variables can be whatever data you assign them as. They can be strings, booleans, integers, and more.

Think of variables as one-sentence statements in the form of “(name) is a ____” . Use variables to tell the computer certain facts about your code. The concept is just as simple as telling me that a fire hydrant is red or the sky is blue.

In C#, you can create variables in the following syntax:

(Data Type) (Variable Name) = (Initial Value) ;

Examples:

        String a = "This is a String.";

        int b = 122;

        bool c = true;

        float d = 0.1234f;

        double e = 0.1234;

Keep in mind that the data types in C# have to be written in a particular way. The next few lines explain how.

Strings:               String

Integers:               int

Booleans:               boolean

Decimal Numbers as Floats:               float

Decimal Numbers as Double :               double

NOTE: you need to declare data types in the EXACT wording as above - same spelling and cases.

3) Composite Data

This concept means that a set of individual, lesser data are comprised together to form a whole, singular chunk of data. Put in the simplest way possible, if Variables are sentences, Composite Data are entire paragraphs that can be made of sentences.

The most commonly used composite data concept today are classes. A class can be composed of any amount of variables and functions (we’ll cover functions later).

In C#, you can create classes in the following syntax:

class (Class Name) {

              // some code

}

Example:

class House {

              // insert code here

}

4a) Making Functions

If Variables are sentences, Functions are merely actions or verbs.

In essence, functions are outlined set of instructions. They are carried out by the computer once a line of code calls their names. For example, if a line of code told a computer to walk, the computer would follow the instructions to walk (i.e. one step forward, lean forward, step with other foot, etc.)

To create a function in C#, follow this syntax:

(data type returned) <Function Name>(<data type1> input1, .. <any add’l inputs>)  {

// write code here

// use this next line if the function outputs any data:

// return (variable name with data type, or any data)

}

Here are some example functions in C#:

// Note how the function’s return data type is a String

// AND there’s a line that returns an actual String

       String functionA(String in1, int in2) {

            return "OKAY";

            }

// Note how the function’s return data type is void

// AND the ‘return’ line doesn’t return any data at all

void functionB(boolean in1, float in2 ) {

            return;

            }

Next, a function will either output some data or it won’t.

For now, it is HIGHLY recommended for you to use comments stating whether or not the function outputs anything. When you use the function, you can only call the function wherever its data output is expected.

Examples:

// returns an Integer, has no inputs:

int functionXYZ() {

              //write code here

              return 12;

}

// doesn't return data, has 3 inputs:

void functionABC(int a, int b, int c) {

              //write code here

}

4b) Using Functions

To call a function, you just write its name, along with any inputs (if it needs them)

If the function doesn’t output data (or if it outputs void), follow this syntax - and make sure it’s in its own line:

<Function Name>( input1, input2, …, inputN);

If the function outputs some data, the syntax is similar as above. However, make sure the function is in a place where the output data type is expected:

<data type> (variable name)  = <Function Name>( input1, input2, …, inputN);

In other words, the function’s output data has to be in a place that ‘makes sense’. For example, if a variable expects an integer, the function needs to output an integer.

Examples:

// No Output:

functionABC(2, 4, 5);

// Outputs an Integer:

int varInteger = functionABC(2, 4, 5);

EASIEST WAY TO LEARN C#, Part 2

To easily run code, select an IDE (Integrated Development Environment: essentially somewhere that you write and run code) of your choice. You may also use online IDE’s such as [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) .

========================= ======

Part 5a: Arrays in C#: Traditional Static Array

Arrays are a sequenced list of a certain data type. Those data types can be simple or compound data. If you need to store lists of data, use Arrays.

To declare an array, follow this syntax:

<data type>[] (variable name);

To initialize it as well, simply do this:

<data type>[] (variable name) = new <same data type>[ <# of array items> ];

Example:

int[] aa = new int[5];

You can even initialize every single item within the array data

<data type>[] (variable name) = {<item 1>, <item 2>, … , <item N>, };

Example:

int[] aa = {1,2,3,4,5};

You can also access individual items based on that item’s position within the array. 0 is the first item; the array size minus one is the last item. 

(In programming, the very 1st number is often 0\. Remember this!)

For example, you would get the first item of an array like so:

aa[0]

And you would get the last item of an array like so:

// an Array with room for 10 items:

aa[9]

Just remember: you can only place the code above somewhere where its data type is expected:

int[] zzz = {1,2,3};

int x = zzz[0];

Part 5b: The List Class from the C# Library

The C# Language includes an List class that helps programmers create flexible arrays. 

To use an List, it’s as if you were declaring a new variable with the List data type:

List<data object type> (variable name);

To initialize the variable, you’ll be using the constructor.

(NOTE: we’ll go over constructors later. For now, just create Lists as shown below)

List<data object type> (variable name) = new List<same data object type>();

Example:

List<String> aa = new List<String>();

Overall, you’ll have two approaches to creating arrays. Lists are generally better suited for Objects (see Object-Oriented Programming in the next few chapters)

Part 5c: Iteration, procedure 1

To process each item in an List, use these lines:

        foreach(var <X> in <Y>) {

           // Do something with each List item in <Y>

              // Using <X>

        }

<X> will be the data object type the List is holding. <Y> is the actual List that the iteration will go over.

Example:

        List<String> aaa = new List<String>();

        aaa.add("Arthur");

        aaa.add("Ben");

        aaa.add("Charles");

        foreach (var xx in aaa) {           

            xx = xx.concat(" is happy");       

            Console.WriteLine(xx);

        }

The above will print out the text below:

Arthur is happy

Ben is happy

Charles is happy

Part 5d: Iteration, procedure 2

The line below is a general iteration loop in C#. It repeats the code below the curly braces by the number you’ve set the limit to.

        int limit = ___;// set limit to whatever you want

        for(int i=0; i<limit;i++) {

            // insert code here             

        }

Using the code above, the iteration loop below is a more traditional way of iterating through an array. What happens is that variable ‘i’ will be 0 to the array length. Every single item in the array named will be accessed and processed.

        int limit = (list name).Count;

        for(int i=0; i<limit;i++) {

            (same list name)[i]               // <— access each item in an array,

              // then do something with it             

        }

For example, this code iterates through an array of integers - processing each item in the process:

        int[] zzz = {1,2,3,4,5,6,7,8,9,10};

        int limit = zzz.length;

        for(int i=0; i<limit;i++) {

            Console.WriteLine(zzz[i]);

            }

The above code should print each array item, making the text output count to 10.

Part 6: Logic & Operators

There are three Basic Logic Operators: AND, OR. and NOT.

AND and OR are used to compare two or more statements that are either True or False. They are  used in the form of (x AND y) or (x OR y)

AND is true if all items between it is true. OR is true if either one of its items is true.

NOT returns the opposite of a single statement it’s set to; so ‘NOT true’ would be false and ‘NOT False’ would be true.

In C#, here are how the operators are set up:

AND operator:               &&

OR operator:               ||

NOT operator:               !

Examples:

// print false:

Console.WriteLine(true && false);

// print true:

Console.WriteLine(true || false);

// print false:

Console.WriteLine(!true);

Part 7: IF-ELSE Statements

The concept is simple: There’s a boolean statement to check. If it’s true, do the procedure after the IF line. If it’s false, do the procedure after the ELSE line.

if ( <insert something that would output a boolean> ) {

              // code that happens if true             

              }

else {

              // code that happens if false

}

Note that the conditional procedures start after the IF and ELSE lines. They need the phrase ‘end’ to signify the end of the procedures.

an IF statement also doesn’t need an ELSE statement; it can be by itself:

if ( <insert something that would output a boolean> ) {

              // code that happens if true             

              }

Examples:

// IF-ELSE together:

if (age > 21) {

              drinkingAge = true;

              }

else {

              drinkingAge = false;

              }

// IF-statement alone:

if (happy && knowIt) {

              hands.clap();

              }

EASIEST WAY TO LEARN OBJECT-ORIENTED

We’ve also included a complementary guide to learning Object-Oriented programming -one of the most popular types of programming in use today. 

To easily run code, select an IDE (Integrated Development Environment: essentially somewhere that you write and run code) of your choice. You may also use online IDE’s such as [rextester.com](http://rextester.com) , [ideone.com](http://ideone.com) ,  or [codepad.org](http://codepad.org) .

========================= ======

1) Object Oriented Programming

In the world of programming, you will hear this term very very often.

This is because Object-Oriented Programming (OOP for short) is one of the most widely-used programming styles out there.

Do you remember the concept of “Classes” back in Part 1? You used this form of composite data to group up smaller data into a larger whole.

The main point of Object-Oriented Programming is this:

In object-oriented programming, you create ‘copies’ of those classes you’ve designed. In even simpler terms, A Class is a data structure that acts as “blueprints”. Those “created copies” you’ve made, based on that class ‘blueprints’, are called Objects.

But why? Because as you learn more and more about programming, you will encounter the notion of Abstraction - applying a general idea across multiple times and scenarios - ultimately saving time, confusion, and effort.

Re-coding the same composite data over and over would lead to more effort and frustration, whereas re-using the same idea leads to efficiency and consistency.

2) OOP Terminology

Variables and Functions can take on new roles in OOP. They can be called Fields and Methods, respectively. In some cases, it’s really up to you to use which names you want, just as long as you understand what other programmers mean when they use these terms.

Fields represent variables in OOP because, just like fields in any entry form, data objects can have fields with as many different values as you can think of.

Think of fields as a certain attribute for an object. Each object might have different attributes from each other:

class Cat{             

              public String color;              

}

// these cats are objects based on Cat class:

catA.color = “white”

catB.color = “grey”

catC.color = “orange”

Methods represent the functions that Objects have. Think of Methods as ‘actions’ and ‘behaviours’ that objects do.

In OOP, you can define a method within a class but you need to access the method from an object itself.

For example, if we create a few Cat objects based on some Cat Class, each Cat object would have all the methods defined on the Cat Class:

class Cat{             

              void meow() {}             

}

// these cats are objects based on Cat class:

catA.meow()

catB.meow()

catC.meow()

3) Constructor Methods

Constructors are special class methods. Based on the classes they belong to, they create Objects for you.

To create a data object based on a certain class, follow this syntax:

(variable name) = new <Class Name>();

You’re essentially setting some variable as a data object.

Example:

class House {

              // insert code here

}

h = new House();

To call a class object, simply refer to the variable its set to:

Example:

House h = new House() ;

House jj = h;

THANK YOU!

========================= ======

We hope you’ve had a lot of fun and learned a lot!

![](Image00012.jpg)

It’s YOUR support that helps us continue to work hard at developing our content. If you’ve enjoyed our work, can you please leave a review on Amazon?

[Click here to leave a review](https://www.amazon.com/review/create-review/ref=cm_cr_dp_wrt_summary?ie=UTF8&asin=B01ESBD0AS&channel=detail-glance&nodeID=133140011&store=digital-text)

We’ve put a lot of time and effort to bring you quality work. So if you’ve enjoyed this work as much as we’ve enjoyed creating it, we would REALLY, really appreciate it if you tell the world.

Thank you!

P.S. We’re constantly updating this work. Stay tuned for future editions!

DONT FORGET!

FOLLOW US =)

========================= ======

              @CodeWizRDZ

| ![](Image00000.jpg) | ![](Image00001.jpg) | ![](Image00002.jpg) |
| [Facebook](https://www.facebook.com/CodeWIzRDZ/) | [Instagram](https://www.instagram.com/codewizrdz) | [Twitter](https://www.twitter.com/codewizrdz) |

              @ EzeeProgramming

| ![](Image00000.jpg) | ![](Image00001.jpg) | ![](Image00002.jpg) |
| [Facebook](https://www.facebook.com/EzeeProgramming) | [Instagram](https://www.instagram.com/ezeeprogramming) | [Twitter](https://www.twitter.com/ezeeprogramming) |