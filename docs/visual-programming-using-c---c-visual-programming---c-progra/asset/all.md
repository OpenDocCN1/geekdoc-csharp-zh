![](Image00017.jpg)

**For soft copy visit www.cs.aagasc.edu.in**
![](Image00000.jpg) **VISUAL PROGRAMMING USING C#
MODULE– I**

Introduction - C, C++, Objective-C, Java and C# - Extensible Markup Language (XML) - Introduction to Microsoft .NET - The .NET Framework and the Common Language Runtime Introduction to Object Technology - Introduction to C# Applications - Creating a Simple Application in Visual C# Express - Formatting Text with Console.Write and Console. WriteLine - Another C# Application: Adding Integers
– Arithmetic - Decision Making: Equality and Relational Operators– Strings and Characters.

**Introduction to C & C++**

C is a high-level structured oriented programming language, used in general purpose programming, developed by Dennis Ritchie at AT&T Bell Labs, the USA between 1969 and 1973.

In 1988, the American National Standards Institute (ANSI) had formalized the C language. C was invented to write UNIX operating system. C is a successor of 'Basic Combined Programming Language' (BCPL) called B language. Linux OS, PHP, and MySQL are written in C. C has been written in assembly language. Simula (1967)

The very first object-oriented programming language C++ (1983) The first object-oriented programming language in the C family of languages Java (1995) Sun's object-oriented programming language C# (2001) programming language

**Java**
Java is a general purpose, high-level programming Microsystems. The Java programming language was developed by a small team of engineers, known as the Green Team, who initiated the language in 1991\. Later, in 2009, Oracle Corporation acquired Sun Microsystems and took ownership of two key Sun software assets: Java and Solaris. In 2006 Sun started to make Java available under the GNU General Public License (GPL). Oracle continues this project called Open-JDK Sun Microsystems was acquired by the Oracle Corporation in 2010\. Oracle has now the steermanship for Java.
Microsoft's object-oriented

language developed by Sun

What is XML?
 XML stands for eXtensible Markup Language  XML is a markup language much like HTML  XML was designed to store and transport data  XML was designed to be self-descriptive

XML Simplifies Things
 It simplifies data sharing  It simplifies data transport  It simplifies platform changes  It simplifies data availability

Many computer systems contain data in incompatible formats. Exchanging data between incompatible systems (or upgraded systems) is a time-consuming task for web developers. Large amounts of data must be converted, and incompatible data is often lost.

XML stores data in plain text format. This provides a software- and hardwareindependent way of storing, transporting, and sharing data. XML also makes it easier to expand or upgrade to new operating systems, new applications, or new browsers, without losing data. With XML, data can be available to all kinds of "reading machines" like people, computers, voice machines, news feeds, etc.

**Introduction to C#**

C# was created at Microsoft late in the 1990s and was part of Microsoft’s overall .NET strategy. It was first released in its alphaversion in the middle of 2000\. C#’s chief architect was Anders Hejlsberg.

**.NET Framework**
It defines two very important entities.

The first is the Common Language Runtime. This is the system that manages the execution of your program. Along with other benefits, the Common Language Runtime is the part of the .NET Framework that enables programs to be portable, supports mixed-language programming, and provides for security.

The second entity is the .NET class library. This library gives your program access to the runtime environment. For example, if you want to perform I/O, such as displaying something on the screen, you will use the .NET class library to do it.

**The Common Language Runtime (CLR)** manages the execution of .NET code. It is the job of the CLR to translate the intermediate code into executable code when a program is run. Microsoft Intermediate Language is turned into executable code using a JIT compiler. JITstands for ―just in time.‖ The process works like this: When a .NET program is executed, the CLR activates the JIT compiler. The JIT compiler converts (Microsoft Intermediate Language) MSIL into native code on a demand basis, as each part of your program is needed.

## **Functions of .NET CLR**

 Convert code into CLI
 Exception handling
 Type safety
 Memory management (using the Garbage Collector)  Security
 Improved performance

 Language independency  Platform independency  Architecture independency

## **Components of .NET CLR**

The key components of CLR includes the following:
 Class Loader - Used to load all classes at run time.

 MSIL to Native code - The Just In Time (JTI) compiler will convert MSIL code into native code.
 Code Manager - It manages the code at run time.
 Garbage Collector - It manages the memory. Collect all unused objects and deallocate them to reduce memory.
 Thread Support - It supports multithreading of our application.
 Exception Handler - It handles exceptions at run time.

## **Benefits of .NET CLR**

The runtime provides the following benefits:

 Performance improvements.
 The ability to easily use components developed in other languages.
 Extensible types provided by a class library.
 Language features such as inheritance, interfaces, and overloading for object-oriented

programming.
 Support for explicit free threading that allows creation of multithreaded, scalable applications.  Support for structured exception handling.
 Support for custom attributes.
 Garbage collection.
 Use of delegates instead of function pointers for increased type safety and security.

![](Image00001.jpg) **Object-Oriented Programming**

At the center of C# is object-oriented programming (OOP). The object-oriented methodology is inseparable from C#, and all C# programs are, at least to some extent, object-oriented. Becauseof its importance to C#, it is useful to understand OOP’s basic principles before you write even a simple C# program.

Encapsulation is a programming mechanism that binds together code and the data it manipulates, and keeps both safe from outside interference and misuse. In an objectoriented language, code and data can be bound together in such a way that a selfcontained black box is created.

Polymorphism (from G reek, meaning ―many forms‖) is the quality that allows one interface to access a general class of actions. A simple example of polymorphism is found in the steering wheel of an automobile. The steering wheel (the interface) is the same, no matter what type of actual steering mechanism is used.

Inheritance is the process by which one object can acquire the properties of another object. This is important because it supports the concept of hierarchical classification. If you think about it, most knowledge is made manageable by hierarchical (that is, top-down) classifications.

**Visual Studio IDE(Integrated Development Environment)**

Visual Studio is Microsoft’s integrated programming environment. It lets us edit, compile, run, and debug a C# program, all without leaving its well thought-out environment. Visual Studio offers convenience and helps manage your programs. It is most effective for larger projects,

**New C# Project**
Create a new, empty C# project by selecting File | New Project. Next, select Empty Project.

Visual C# - Project
Console Application
Windows Forms Application

Console Application
This application of C# program shows the output in command window. **Example**

## class MyClass { static void Main() { Console.Write(―Welcome‖); } }

Where Console.Write() method is used to display output on screen Console.ReadLine() method is used to read data at run time **Data Types**

## The following table shows the supported data types, including
storage sizes and ranges. **byte (1), Boolean (true / false), integer (+/**

**32,767), long (10 digit integer), single (4 bytes float), double (8 bytes float), decimal (14 bytes 29 digit integer), date ( year 1 to 9999), string**
![](Image00002.gif)  **Data type Storage size Range
byte** 1 byte 0 to 255
**boolean** 2 bytes **True** or **False
integer** 2 bytes
-32,768 to 32,767
**long** (long integer) 4 bytes +/- 10 Digit Integer
**longlong** (longlong integer) 8 bytes +/- 19 Digit Integer **single** (single-precision floating[4 bytespoint)]
-3.4 E38 to -1.4E-45
**double**
(double-precision floating
8 bytes point)
-1.7E308 to-4.9E-324 for negative values; 4.9E-324 to 1.7E308 for positive values
**currency** (scaled integer) 8 bytes +/- 15 Digits **decimal** 14 bytes +/-29 Digits
**date** 8 bytes January 1, 100 to December 31, 9999
**object** 4 bytes
Any **Object** reference
**Data type Storage size Range**

**string** (variable-length) 10 bytes + string length
0 to approximately 2 billion

**string** (fixed-length) Length of string 1 to approximately 65,400 **variant** (with numbers)

## **Arithmetic Operators**

+ Addition
− Subtraction
* Multiplication
/ Division

Using the above arithmetic operators we can do lot of calculation in c-sharp language.
int num1, num2, add;
num1 = Convert.ToInt32(Console.ReadLine());
num2 = Convert.ToInt32(Console.ReadLine());
add = num1 + num2;
Console.Write(add);

## **Relational Operators**

Operator Meaning
< Less than
<= Less than or equal to
> Greater than
>= Greater than or equal to
= = Equal to
!= Not equal to

16 bytes Any numeric value up to the range of a **Double**

int a, b, c;
a = 2;
b = 3;
if(a < b)
Console.WriteLine("a is less than b");

The above code test a is less than b and show the result.

## **String and Characters**

The common practice is to use the string keyword to declare a string variable. The String class has methods to clone a string, compare strings, concatenate strings, and copy strings. This class also provides methods to find a substring in a string, find the index of a character or substring, replace characters, spilt a string, trim a string, and add padding to a string. The string class also provides methods to convert a string characters to uppercase or lowercase.

string fname, lname;
fname = "Rowan";
lname = "Atkinson";

fname.Length .ToCharArray() .Empty
.Substring(index)
- returns number of character in the given string
- it convert the given string into character array
- it check the given string is empty
- returns sub string from the given index

.Join(string,string) - combine two strings
+ operator also used to combile more than one strings.
string authorDetails = firstName + " " + lastName + " is " + age + " years";

The char data type represents a character in .NET. In .NET, text is stored as a sequential read-only collection of Char objects. There is no null-terminating character at the end of a C# string; therefore a C# string can contain any number of embedded null characters ('\0').

char ch=’A’;
char[] chars = { 'M', 'a', 'h', 'e', 's', 'h' };

**Factorial program in C#**
using System;
public class FactorialExample
{
public static void Main(string[] args)
{
int i,fact=1,number;
Console.Write("Enter any Number: ");
number= int.Parse(Console.ReadLine());
for(i=1;i<=number;i++){
fact=fact*i;
}
Console.Write("Factorial of " +number+" is: "+fact); }
}

Output
Enter any Number: 6
Factorial of 6 is: 720

**MODULE– II**

Introduction to Classes and Objects – Introduction - Classes, Objects, Methods, Properties and Instance Variables - Declaring a Class with a Method and Instantiating an Object of a Class - Declaring a Method with a Parameter - UML Class Diagram with a Property Software Engineering with Properties and set and get Accessors - Initializing Objects with Constructors - Floating-Point Numbers and Type decimal Control Statements

## **Classes, Objects, Methods, Properties and Instance Variables**

Let’s begin with a simple drive a car, someone has to design it. A car typically begins as engineering drawings, similar to the blueprints used to design a house. These engineering drawings include the design for an accelerator pedal to make the car go faster. The pedal ―hides‖ the complex mechanisms that actually make the car go faster, just as the brake pedal ―hides‖ the mechanisms that slow the car and the steering wheel ―hides‖ the mechanisms that turn the car.

This enables people with little or no knowledge of how engines work to drive a car easily.

## **Methods**

Now let’s use our car example to introduce the key progr amming concepts of this section. Performing a task in an application requires a method. The method describes the mechanisms that actually perform its tasks. The method hides from its user the complex tasks that it performs, just as the accelerator pedal of a car hides from the driver the complex mechanisms of making the car go faster.

## **Classes**

In C#, we begin by creating an application unit called a class to house (among otherthings) a method, just as a car’s engineering drawings house (among other things) the design of an accelerator pedal. In a class, you provide one or more methods that are designedto perform the class’s tasks.

For example, a class that represents a bank account might contain one method to deposit money in an account, another to withdraw money from an account and a third to inquire what the current account balance is. Objects Just as you cannot drive an engineering drawing of a car, you cannot ―drive‖ a class. Just as someone has to build a car from its engineering drawings before you can actually drive it, you must build an object of a class before you can make an application perform the tasks the class describes. That’s one reason C# is known as an object-oriented programming language.

## **Method Calls**

When you drive a car, pressing its gas pedal sends a message to the car to perform a task make the car go faster. Similarly, you send messages to an object—each message is known as a method call and tells a method of the object to perform its task.

## **Attributes**

Thus far, we’ve used the car a nalogy to introduce classes, objects and methods. In additionto a car’s capabilities, it also has many attributes, such as its color, the number of doors, the amount of gas in its tank, its current speed and its total miles driven (i.e., its odometer reading).

**Declaration of Class and Methods**
Let us see the following example show the simple object with class Product

{
public int pid;
public string pname; public Product()
{

pid = 40;
pname = "Lux"; }
public void show()
{
Console.WriteLine(pid); Console.WriteLine(pname);
}
static void Main(string[] args)
{
Product p = new Product();
p.show();
p.pid = 34;

^(p.pname = "Hai"; Where p is thep.show(); instance variable) Console.ReadKey();
}
}
In the above class pid and pname are the member variable, show() is the method. **Declaring a method with parameter**
void add(int a, int b)

{
int c;
c = a + b;
Console.WriteLine(c);

}

## Adding the Constructor to Class Product **UML Class Diagram**

The UML class diagram models class, which has a constructor that has a name parameter of type string. Like operations, the UML models constructors in the third compartment of a class in a class diagram. Class diagrams basically represent the object-oriented view of a system, which is static in nature.

**Bank Account** + Owner : String +Balance : Decimal deposit()
withdrawal()

In the above diagram Bank Account is the class, owner and balance are the member variable deposit() and withdrawal() are the member function. +) sign— preceded by

the word ―property‖ i
Dependency

A dependency means the relation between two or more classes in which a change in one may force changes in the other. However, it will always create a weaker relationship. Dependency indicates that one class depends on another.

**Customer Bank**

### **Software Engineering with Properties and set and get Accessors**

Using properties as described earlier in this chapter would seem to violate the notion of private data. Although providing a property with get and set accessors may appear to be the same as making its corresponding instance variable public, this is not the case. A public instance variable can be read or written by any property or method in the program. If an instance variable is private, the client code can access the instance variable only indirectlythrough the class’s non-private properties or methods. This allows the class to control the manner in which the data is set or returned. For example, get and set accessors can translate between the format of the data stored in the private instance variable and the format of the data preferred by the client.

## **Control Structures**

Normally, statements in an application are executed one after the other in the order inwhich they’re written—this process is called sequential execution. Various C# statements enable you to specify that the next statement to execute is not necessarily the next one in sequence—this is called transfer of control.

![](Image00003.jpg)

It contains two action states that represent actions to perform. Each action state contains an action expression—for example, ―add grade to total‖ or ―add 1 to counter‖—that specifies an action to perform. Other actions might include calculations or input/output operations. The arrows in the activity diagram represent transitions, which indicate the order in which the actions occur.

### **if Single-Selection Statement**

Applications use selection statements to choose among alternative courses of action. For example, suppose that the passing grade on an exam is 60.
**if** ( grade >= **60** )
Console.WriteLine( **"Passed"** );

The above C# statement determines whether the condition grade >= 60 is true or false. If the condition is true, "Passed" is displayed, and the next C# statement in order is performed. If the condition is false, the output statement is ignored, and the next C# statement in order is performed.

![](Image00004.jpg)

### **if…else Double-Selection Statement**

The if single-selection statement performs an indicated action only when the conditionis true; otherwise, the action is skipped. The if…else double-selection statement allows you to specify an action to perform when the condition is true and a different action when the condition is false.

**if** ( grade >= **60** )
Console.WriteLine( **"Passed"** );
**else**
Console.WriteLine( **"Failed"** );

For example, the C# statement displays "Passed" if grade >= 60 is true, but displays "Failed" if grade < 60 is true. In either case, after displaying occurs, the next statement in sequence is performed. The body of the else part is also indented. Whatever indentation convention you choose should be applied consistently throughout your applications. It’s difficult to read applications that do not obey uniform spacing conventions.

![](Image00005.jpg) **Conditional Operator (?:)**

C# provides the conditional operator (?:), which can be used in place of an if…else statement. This is C#’s only ternary operator—it takes three operands. Together, the operands and the ?: symbols form a conditional expression. The first operand (to the left of the ?) is a boolean expression (i.e., an expression that evaluates to a bool-type value—true or false), the second operand (between the ? and :) is the value of the conditional expression if the boolean expression is true and the third operand (to the right of the :) is the value of the conditional expression if the boolean expression is false.

Console.WriteLine( grade >= **60** ? **"Passed"** : **"Failed"** );

For example, the statementdisplays the value of WriteLine’s conditional- expression argument. The conditional expression in the preceding statement evaluates to the string "Passed" if the boolean expression grade >= 60 is true and evaluates to the string "Failed" if the boolean expression is false.

## **Nested if…else Statements**

![](Image00006.gif)

An application can test multiple cases by placing if…else statements inside other if…else statements to create nested if…else statements. For example, the following nested if…else statement displays A for exam grades greater than or equal to 90, B for grades in the range 80 to 89, C for grades in the range 70 to 79, D for grades in the range 60 to 69 and F for all other grades:

**if** ( grade >= **90** )

Console.WriteLine( **"A"** );
**else
if** ( grade >= **80** )
Console.WriteLine( **"B"** );
**else
if** ( grade >= **70** )
Console.WriteLine( **"C"** ); **else**

**if** ( grade >= **60** )

Console.WriteLine( **"D"** ); **else**
Console.WriteLine( **"F"** );

**MODULE– III**

Classes and Objects: A Deeper Look – Introduction - Controlling Access to Members - Referringto the Current Object’s Members with the this Reference – Indexers - Default and Parameterless Constructors– Composition - Garbage Collection and Destructors- static Class Members - Data Abstraction and Encapsulation – Object Initializers– Delegates Object-Oriented Programming: Inheritance - Polymorphism, Interfaces and Operator Overloading-Exception Handling

## **Controlling Access to Members**

We can use the following access modifiers to specify the accessibility of a type or member
**public :** The type or member can be accessed by any other code in the same assembly or another assembly that references it.
**private:** The type or member can be accessed only by code in the same class or struct. **protected:** The type or member can be accessed only by code in the same class, or in a class that is derived from that class.

**Internal:** The type or member can be accessed by any code in the same assembly, but not from another assembly.

Class members (including nested classes and structs) can be declared with any of the six types of access. Struct members cannot be declared as protected because structs do not support inheritance.

## **This** Reference

# The **this** keyword refers to the current instance of the class and is also used as a

modifier of the first parameter of an extension method.
**public class Employee
{**

**private string alias; private string name;**

**public Employee(string name, string alias) {
// Use this to qualify the members of the class // instead of the constructor parameters. this.name = name;
this.alias = alias;
}
}**

 To qualify members hidden by similar names, for example:

## **Default and Parameterless Constructors**

The compiler will not create a default constructor for a class that explicitly declares at least one constructor. In this case, if you want to be able to invoke the constructor with no arguments, we must declare a parameterless constructor, a default constructor, a parameterless constructor is invoked with empty parentheses.

class Product {
public int pid;
public string pname; Empty or Parameterless constructor

public Product() {

} public Product(int pid=10,string pname="Hammam") {

this.pid = pid;
this.pname = pname; }
public void show()
{
Console.WriteLine(pid); Console.WriteLine(pname);
}
static void Main(string[] args)
{
Product p = new Product(); p.show();
p.pid = 34;
Product p2 = new Product(23); p2.show();
Console.ReadKey();
}
}
In p2 instance pid takes 23 and pname takes default value from the constructor.

### **Garbage Collection and Destructors**

The Common Language Runtime (CLR) performs automatic memory management by using a garbage collector to reclaim the memory occupied by objects that are no longer in use, so the memory can be used for other objects. When there are no more references to an object, the object becomes eligible for destruction. Every object has a special member, called a destructor, that is invoked by the garbage collector to perform termination housekeeping on an object before the garbage collector reclaims theobject’s memory. A destructor is declared like a parameterless constructor, except that its name is the class name, preceded by a tilde (~), and it has no access modifier in its header.After the garbage collector calls the object’s destructor, the object becomes eligible for garbage collection.

~ public Product()
{
}

A problem with the garbage collector is t hat it doesn’t guarantee that it will perform its tasks at a specified time. Therefore, the garbage collector may call the destructor any
time after the object becomes eligible for destruction, and may reclaim the memory any time after the destructor executes.

### **static Class Members**

Every object has its own copy of all the instance variables of the class. In certain cases, only one copy of a particular variable should be shared by all objects of a class. A static variable is used in such cases. A static variable represents class wide information—all objects of the class share the same piece of data. The declaration of a static variable begins with the keyword static.

public class Employee {
public static int count = 0; // number of objects in memory

public static void showLine()
{
Console.WriteLine(―------------------------------------------―); }

}
In the above example count is the static variable showLine() is the static function.

### **Data Abstraction and Encapsulation**

Classes normally hide the details of their implementation from their clients. The abstract member has no detailed coding. This will be code later in program.

It is used to display only necessary and essential features of an object to ouside the world.Means displaying what is necessary and encapsulate the unnecessary things to outside the world.Hiding can be achieved by using "private" access modifiers.

Lets have a look of this code!

abstract class animal {
public abstract void eat(); public void sound()
{
Console.WriteLine("dog can sound");
}
}
In the above class animal is the generic class in which different kinds of animal takes different food. The eat() method is the abstract method that will code later. The method overriding could be done by putting the keyword 'new' before that overridden method.
class dog : animal
{
public override void eat() { Console.WriteLine("dog can eat"); }
}
The above dog class we override the eat() method.

## **Encapsulation** is defined 'as the process of enclosing one or more items within a

physical or logical package'. Encapsulation, in object oriented programming methodology, prevents access to implementation details. Abstraction and encapsulation are related features in object oriented programming.

## **Inheritance**

Inheritance allows us to define a class in terms of another class, which makes it easier to create and maintain an application. This also provides an opportunity to reuse the code functionality and speeds up implementation time. This existing class is called the base class, and the new class is referred to as the derived class. In the following class Rectangle is the Base class and Tabletop is the Derived class

class Rectangle {

//member variables
protected double length; protected double width;

public Rectangle(double l, double w) { length = l;
width = w;

}
public double GetArea() {
return length * width;

}
public void Display() {
Console.WriteLine("Length: {0}", length);
Console.WriteLine("Width: {0}", width);
Console.WriteLine("Area: {0}", GetArea()); }
}//end class Rectangle

class Tabletop : Rectangle {
private double cost;
public Tabletop(double l, double w) : base(l, w) { }

public double GetCost() {
double cost;
cost = GetArea() * 70;
return cost;

}
public void Display() {
base.Display();
Console.WriteLine("Cost: {0}", GetCost()); }
}

## Polymorphism

The word polymorphism means having many forms. In object-oriented programming paradigm, polymorphism is often expressed as 'one interface, multiple functions'.

Polymorphism can be static or dynamic. In **static polymorphism** , the response to a function is determined at the compile time. In **dynamic polymorphism** , it is decided at run-time.

## **Static Polymorphism**

The mechanism of linking a function with an object during compile time is called early binding. It is also called static binding. C# provides two techniques to implement static polymorphism. They are −

 Function overloading
 Operator overloading
class Printdata {
void print(int i) {

Console.WriteLine("Printing ", i );
}
void print(double f) {

Console.WriteLine("Printing " , f);
}
void print(string s) {

Console.WriteLine("Printing ", s);
}
static void Main(string[] args) {

Printdata p = new Printdata();
// Call print to print integer p.print(5);
// Call print to print float p.print(500.263);

// Call print to print string
p.print("Hello C++");
Console.ReadKey();

}
}
In the above example we written the print() function for integer, float and string data.

## **Dynamic Polymorphism**

C# allows you to create abstract classes that are used to provide partial class implementation of an interface. Implementation is completed when a derived class inherits from it. Abstract classes contain abstract methods, which are implemented by the derived class. The derived classes have more specialized functionality.

Here are the rules about abstract classes −
 We cannot create an instance of an abstract class
 We cannot declare an abstract method outside an abstract class

abstract class Shape {
public abstract int area();

}
class Rectangle: Shape {
private int length;
private int width;

public Rectangle( int a = 0, int b = 0) { length = a;
width = b;

}
public override int area () {

The method area() present in base class Shape as a abstract member. That will be redefined in derived class called dynamic polymorphism.

Console.WriteLine("Rectangle class area :"); return (width * length);

}
static void Main(string[] args) {
Rectangle r = new Rectangle(10, 7); double a = r.area();
Console.WriteLine("Area: {0}",a); Console.ReadKey();

} }
**MODULE– IV**

Graphical User Interfaces with Windows Forms – Introduction - Windows Forms
- Control Properties and Layout - Labels, TextBoxes and Buttons - GroupBoxes and Panels - CheckBoxes and RadioButtons - NumericUpDown Control - Mouse-Event Handling- Keyboard-Event Handling– Menus- various controls - Multiple Document Interface (MDI) Windows - Visual Inheritance - User-Defined Controls.

**Graphical User Interfaces**

Near the top of the window, there’s a menu bar containing the menus File, Edit, View, Project, Build, Debug, Data, Tools, Window, and Help. Below the menu bar is a tool bar of buttons, each with a defined task, such as creating a new project or opening an existing project. There are two tabs below the tool bar—these present information in a tabbed view and allow users to switch between them.

These controls form a user-friendly interface through which you have been interacting with the IDE.
![](Image00007.gif)  ntrol Description
**Label** - Labels are one of the most frequently used C# control. We can use the Label control to display text in a set location on the page.

label1.Text = "This is my first Label";
In addition to display an image using the Image property, or a combination of the ImageIndex and ImageList properties.

label1.Image = Image.FromFile("C:\\testimage.jpg");

**TextBox** - Enables the user to enter data via the keyboard. It can also be used to display editable or uneditable text. For displaying a text in a TextBox control , you can
code like this.
textBox1.Text = "welcome to our college";
**Button** - Windows Forms controls are reusable components that encapsulate user interface functionality and are used in client side Windows applications. A button is a control, which is an interactive component that enables users to communicate with an application. The Button class inherits directly from the ButtonBase class. A Button can be clicked by using the mouse, ENTER key, or SPACEBAR if the button has focus.

button1.Text = "Click Here";
**CheckBox** Specifies an option that can be selected (checked) or unselected (not checked).
![](Image00008.jpg) checkBox1.Text = "Net-informations.com";
checkBox1.ThreeState = true;
**ComboBox** Provides a drop-down list of items from which the user can make a selection either by clicking an item in the list or by typing in a box.

comboBox1.Items.Add("Sunday");
comboBox1.Items.Add("Monday");
comboBox1.Items.Add("Tuesday");

**ListBox** Provides a list of items from which the user can make a selection by clicking one or more items.

listBox1.Items.Add("Sunday");
listBox1.Items.Add("Monday");
listBox1.Items.Add("Tueday");

**Radio Button** A radio button or option button enables the user to select a single option from a group of choices when paired with other RadioButton controls. When a user clicks on a radio button, it becomes checked, and all other radio buttons with same group become unchecked.

![](Image00009.jpg)

radioButton1.Checked = true; **NumericUpDown** A NumericUpDown control allows users to provide a spin (up/down) interface to move through pre-defined numbers using up and down arrows.

For example **cud** is the **NumericUpDown** control

cud.Maximum = 100 cud.Minimum = 0 cud.Value = 10;

**C# Mouse Events**
An essential aspect of Windows programming is the use of the mouse.

 Click
This event occurs when the mouse button is released, typically before the MouseUp event. The handler for this event receives an argument of type EventArgs. Handle this event when you only need to determine when a click occurs.

 MouseClick
This event occurs when the user clicks the control with the mouse. The handler for this event receives an argument of type MouseEventArgs. Handle this event when you need to get information about the mouse when a click occurs.

 DoubleClick
This event occurs when the control is double-clicked. The handler for this event receives an argument of type EventArgs. Handle this event when you only need to determine when a double-click occurs.

 MouseDoubleClick
This event occurs when the user double-clicks the control with the mouse. The handler for this event receives an argument of type MouseEventArgs. Handle this event when you need to get information about the mouse when a double-click occurs.

 MouseDown
This event occurs when the mouse pointer is over the control and the user presses a mouse button. The handler for this event receives an argument of type MouseEventArgs.

 MouseEnter
This event occurs when the mouse pointer enters the border or client area of the control, depending on the type of control. The handler for this event receives an argument of type EventArgs.

[] MouseHover
This event occurs when the mouse pointer stops and rests over the control. The handler for this event receives an argument of type EventArgs.

 MouseLeave
This event occurs when the mouse pointer leaves the border or client area of the control, depending on the type of the control. The handler for this event receives an argument of type EventArgs.

 MouseMove
This event occurs when the mouse pointer moves while it is over a control. The handler for this event receives an argument of type MouseEventArgs.

[] MouseUp
This event occurs when the mouse pointer is over the control and the user releases a mouse button. The handler for this event receives an argument of type MouseEventArgs.

 MouseWheel
This event occurs when the user rotates the mouse wheel while the control has focus. The handler for this event receives an argument of type MouseEventArgs. You can use the Delta property of MouseEventArgs to determine how far the mouse has scrolled.

**MouseEventArgs Class**
This gives us information about what has just happened with the mouse.
There is a constructor, but it does not seem useful.
Properties: (all "get" only)

 X = x-coordinate of the mouse (integer)
 Y = y-coordinate of the house (integer)
 Location = location of the mouse (Point, hence an x-y pair)
 Button = which mouse button was pressed (a member of the MouseButtons

enumeration: Left, Right, Middle, None, etc.)
 Clicks = number of times the button was pressed and released (integer)  Delta = the number of notches ("detents") by which the mouse has been

rotated (integer)
We will need a using statement for System.Windows.Forms.
In the InitializeComponent method, we need a line:
**this.MouseDown += new MouseEventHandler(this.Form_MouseDown);**
The event handler might look like this:

private void Form_MouseDown(object sender, MouseEventArgs e) {
switch (e.Button)
{

case MouseButtons.Left:
MessageBox.Show("Left Button Click");
break;

case MouseButtons.Right:
MessageBox.Show("Right Button Click");
break;

default:
break;
}
}
**Keyboard Events
There are three key events:**

 **KeyDown**
This event is raised once when a user presses a key.
The second argument of the event handler is of type KeyEventsArgs.

 **KeyPress**
This event is raised when the key or keys pressed result in a character. For instance, "Shift" plus "a" produces the character "A".
If the keys are held down, the KeyPress event may be generated repeated, as in "AAAAAAAAA".
The second argument of the event handler is of type KeyPressEventsArgs.

 **KeyUp**
This event is raised when a key is released.
The second argument of the event handler is of type KeyEventsArgs.

Thus the sequence of events is: KeyDOwn, KeyPress, KeyUp.
In the Designer file, we need a line to attach the handler to the event:
this.KeyDown +=

new System.Windows.Forms.KeyEventHandler(this.KeyDemo_KeyDown);
**C# Menu Control**

A Menu on a Windows Form is created with a MainMenu object, which is a collection of MenuItem objects. MainMenu is the container for the Menu structure of the form and menus are made of MenuItem objects that represent individual parts of a menu.

![](Image00010.gif)

We can add menus to Windows Forms at design time by adding the MainMenu component and then appending menu items to it using the Menu Designer.
After drag the Menustrip on your form you can directly create the menu items by type a value into the "Type Here" box on the menubar part of your form. From the following picture you can understand how to create each menu items on mainmenu Object.

![](Image00011.gif) **Other Controls**

**Font Dialog Box**
Font dialog box represents a common dialog box that displays a list of fonts that are currently
installed on the system.

**OpenFile Dialog Box**

The OpenFileDialog component allows users to browse the folders of their computer or any computer on the network and select one or more files to open. The dialog box returns the path and name of the file the user selected in the dialog box.

**Print Dialog Box**

A user can use the Print dialog box to select a printer, configure it, and perform a print job. Print dialog boxes provide an easy way to implement Print and Print Setup dialog boxes in a manner consistent with Windows standards.

### **Implementing an MDI Form**

A Multiple Document Interface (MDI) programs can display multiple child windows inside them. This is in contrast to single document interface (SDI) applications, which can manipulate only one document at a time. Visual Studio Environment is an example of Multiple Document Interface (MDI) and notepad is an example of an SDI application. MDI applications often have a Window menu item with submenus for switching between windows or documents.

![](Image00012.gif) Any windows can become an MDI parent, if you set the IsMdiContainer property to True. **IsMdiContainer = true;**

Create a new C# project, then you will get a default form Form1 . Then add two mnore forms in the project (Form2 , Form 3) . Create a Menu on your form and call these two forms on menu click event. Follow this small step by step walkthrough to make a small MDI application.

1\. Goto File->New->Blank Solution
2\. Select Visual C# Projects in Project Types
3\. Select WindowsApplication in Templates
4\. Type for eg. myBestMDI in the Name textbox
5\. By Clicking the browse button select the location & Click OK

**Creating the Main MDI Form(frmMDIMain) to Act as a Container**
1\. In the View->Solution Explorer click Form1 only once
2\. Locate the property FileName and type "frmMDIMain.cs"
3\. In the Solution Explorer now doubleclick frmMDIMain
4\. Locate the property (Name) and type "frmMDIMain"
5\. Locate the property Text and type "This is the Parent"
6\. Locate the property IsMDIContainer and set it to true
7\. Locate the property WindowState and set it to Maximized

**Creating the Child form (frmMChild) to Demonstrate Multiple Instance**
1\. Goto Project Menu-Add Windows Forms & type frmMChild
2\. In the Solution Explorer now doubleclick frmMChild
3\. Locate the property Text and type "This is the Multi Instance Child"
4\. Locate the property size & set it to 568, 464

**MODULE– V**

Databases and LINQ - Introduction - relational Databases - LINQ to SQL – Querying a Database with LINQ - Dynamically Binding Query Results - Retrieving Data from Multiple Tables with LINQ - Creating a Master/Detail View Application Tools and Web Resources Case Study

**What is LINQ?**

LINQ (Language Integrated Query) is uniform query syntax in C# and VB.NET to retrieve data from different sources and formats. It is integrated in C# or VB, thereby eliminating the mismatch between programming languages and databases, as well as providing a single querying interface for different types of data sources.

LINQ (Language Integrated Query) is uniform query syntax in C# and VB.NET to retrieve data from different sources and formats. It is integrated in C# or VB, thereby eliminating the mismatch between programming languages and databases, as well as providing a single querying interface for different types of data sources.

For example, SQL is a Structured Query Language used to save and retrieve data from a database. In the same way, LINQ is a structured query syntax built in C# and VB.NET to retrieve data from different types of data sources such as collections, ADO.Net DataSet, XML Docs, web service and MS SQL Server and other databases.
The following example demonstrates a simple LINQ query that gets all strings from an array which contains 'a'.

![](Image00013.jpg)  LINQ Usage
LINQ queries return results as objects. It enables you to uses object-oriented approach on the result set and not to worry about transforming diffent formats of results into objects.
![](Image00014.jpg)
// Data source
string[] names = {"Bill", "Steve", "James", "Mohan" };

// LINQ Query
var myLinqQuery = from nm in names where nm.Contains('a')
select nm;

// Query execution
foreach(var nm in myLinqQuery) Console.Write(nm + " ");

## **Standard Query & Operators**

Standard Query Operators in LINQ are actually extension methods for the IEnumerable<T> and IQueryable<T> types. They are defined in the System.Linq.Enumerable and
System.Linq.Queryable classes. There are over 50 standard query operators available in LINQ that provide different functionalities like filtering, sorting, grouping, aggregation, concatenation, etc.

![](Image00015.jpg)  Standard Query Operators in Query Syntax

## **Standard Query Operators in Method Syntax**

![](Image00016.jpg) Standard query operators in query syntax is converted into extension methods at compile time, so both are same.
**OrderBy**

OrderBy sorts the values of a collection in ascending or descending order. It sorts the collection in ascending order by default because ascending keyword is optional here. Use descending keyword to sort collection in descending order.

**IList<Student> studentList = new List<Student>() {
new Student() { StudentID = 1, StudentName = "John", Age = 18 } , new Student() { StudentID = 2, StudentName = "Steve", Age = 15 } , new Student() { StudentID = 3, StudentName = "Bill", Age = 25 } ,**

**new Student() { StudentID = 4, StudentName = "Ram" , Age = 20 } , new Student() { StudentID = 5, StudentName = "Ron" , Age = 19 } };**

**var orderByResult = from s in studentList orderby s.StudentName select s;**

**Console.WriteLine("Ascending Order:");
foreach (var std in orderByResult)**

**Console.WriteLine(std.StudentName);** **Output**
Ascending Order:
Bill
John
Ram
Ron
Steve

## **GroupBy**

The GroupBy operator returns a group of elements from the given collection based on some key value.

var groupedResult = from s in studentList
group s by s.Age;
//iterate each group
foreach (var ageGroup in groupedResult)
{

Console.WriteLine("Age Group: {0}", ageGroup.Key); //Each group has a key
foreach(Student s in ageGroup) // Each group has inner collection Console.WriteLine("Student Name: {0}", s.StudentName); }
Output

AgeGroup: 18
StudentName: John
StudentName: Bill
AgeGroup: 21
StudentName: Steve
StudentName: Abram
AgeGroup: 20
StudentName: Ram

As you can see in the above example, you can iterate the group using a 'foreach' loop, where each group contains a key and inner collection. The following figure shows the result in debug view. Notice that each group will have a property name on which group is performed. In the above example, we have used Age to form a group so each group will have "Age" property name instead of "Key" as a property name.

// Student collection

IList<Student> studentList = new List<Student>() {
new Student() { StudentID = 1, StudentName = "John", Age = 18, StandardID = 1 } , new Student() { StudentID = 2, StudentName = "Steve", Age = 21, StandardID = 1 } , new Student() { StudentID = 3, StudentName = "Bill", Age = 18, StandardID = 2 } , new Student() { StudentID = 4, StudentName = "Ram" , Age = 20, StandardID = 2 } , new Student() { StudentID = 5, StudentName = "Ron" , Age = 21 }

};

IList<Standard> standardList = new List<Standard>() {
new Standard(){ StandardID = 1, StandardName="Standard 1"}, new Standard(){ StandardID = 2, StandardName="Standard 2"}, new Standard(){ StandardID = 3, StandardName="Standard 3"}

};
var innerJoinResult = studentList.Join(// outer sequence
standardList, // inner sequence
student => student.StandardID, // outerKeySelector
standard => standard.StandardID, // innerKeySelector
(student, standard) => new // result selector
{
StudentName = student.StudentName, StandardName = standard.StandardName });
foreach (var obj in innerJoinResult)
{
Console.WriteLine("{0} - {1}", obj.StudentName, obj.StandardName);
}
}
Output
John - Standard 1
Steve - Standard 1
Bill - Standard 2
Ram - Standard 2