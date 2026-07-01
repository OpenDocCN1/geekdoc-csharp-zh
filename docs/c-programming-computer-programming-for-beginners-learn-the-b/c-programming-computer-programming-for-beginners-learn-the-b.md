# C# 编程：初学者计算机编程指南




[分页]

[分页]


## 引言

首先，感谢你购买本书——《编程：面向初学者的计算机编程：C# 基础入门》。C# 是微软在其 .NET 计划下开发的。

C#，发音为 C Sharp，是一种编程语言。它是一种多范式编程语言，支持多种编程范式，如面向对象编程。因此，你可以灵活地选择适合当前任务的编程风格。此外，C# 被认为是初学者踏入广阔的计算机编程世界的理想入门语言。

学习 C# 为你打开了大量机会的大门。通过 C#，你可以进一步学习强大的 C 语言以及 C++。掌握 C# 还使你能够通过 .NET 平台获取 Web 开发所需的技能。此外，如果你计划将来为微软生态系统开发产品，这门语言也会非常有帮助。

面对这些内容是否感到有些不知所措？对于初学者来说，信息量可能确实很大。不过，你不必过于担心。本书将帮助你获得成为 C# 程序员所需的基础知识。你将学习一些酷炫的新术语，甚至编写几个程序。你会接触到这门语言中使用的一些术语和函数。总之，你将做好充分准备，从而可以开始高级课程并成为一名顶尖程序员。

现在，让我们开始学习 C# 吧！

## 第一章

### C# 简介

当微软最初开发 .NET 框架时，程序员不得不借助 Simple Managed C（一种托管代码编译器系统）来编写类库。然而，使用 C 存在一些问题。因此，C# 作为一种新语言被开发出来，以解决这些问题。

C# 被专门设计得简洁而现代。它是一种面向对象的通用编程语言。如果你已经熟悉编程，你会很容易地发现 C# 借鉴了其他多种编程语言的关键概念，其中最著名的是 Java。

### .NET 框架的重要性

理论上，C# 可以被编译成机器码。然而，在实际应用中，这门语言几乎总是与 .NET 框架配合使用。因此，你需要确保在运行用 C# 编写的应用程序的计算机上已安装 .NET 框架。

.NET 框架兼容多种编程语言。然而，C# 是与该框架最紧密相关的语言。在某些圈子里，它甚至被称为"THE .NET 语言"。这可能是因为该框架和语言的开发是同步进行的。

### 开始 C# 编程需要什么？

在开始编写 C# 程序之前，有几件事你需要先做好准备。确保以下程序已安装在你的计算机上。

- .NET Framework 软件开发工具包
- 一个编辑器

就这些。这些是你开始用 C# 编程所需的全部。目前有各种各样的编辑器可供选择。你甚至可以使用 Notepad 或 DOS Editor，后面会详细介绍。不过，为了更好的学习体验，建议你安装以下任一可选程序。

- Visual C# .NET
- Visual C++ 6.0。它包含在 Microsoft Visual Studio 6.0 套件中。

你的第一步应该是在计算机上安装 .NET SDK。你可以轻松地从微软官方网站下载该程序。你还将获得完整的程序文档。安装此工具包后，你将能够编译和执行 C# 源代码。这得益于工具包内置的命令行编译器（Command Line Compiler）以及运行时即时编译器（Just in Time Compiler）。如果你之前接触过 Java，你可以将它们与 Java 开发工具包（Java Development Kit）中的 Java 编译器和 Java 解释器进行类比。

### 关于编辑器

编辑器是用于编写源代码的程序。C# 在这方面非常灵活，因为几乎任何文本编辑器都可以用来编写它。即使是 Windows 中最基本的 Notepad 也是一个不错的选择。编译方面，你可以轻松使用 .NET 框架中的命令行编译器 csc.exe。

当使用 .NET SDK 开发 C# 程序时，Notepad 是一个热门选择。然而，它并不是最好的编辑器，尤其对于初学者来说。毕竟，Notepad 缺少一些实用功能，如行号显示和语法高亮。

这就是为什么许多开发者更喜欢使用集成开发环境（Integrated Development Environment），即 IDE。目前有很多



微软提供了多种选择，其中最好的是 Visual Studio。该程序可用于处理 .NET 框架的所有方面。这确实是一款非常先进的程序，且有多个版本可供选择。完整版的 Visual Studio 价格相当昂贵，即使对于爱好者来说也可能过于高级。

在 .NET 框架发布时，微软推出了该产品的 Express 版本。这些版本面向爱好编程的初学者以及刚接触 .NET 框架的人群。Express 版本仅能用于单一语言。它们可能不具备 Visual Studio 最高级的功能，但它们是免费的。对于学习你选择的语言（本例中为 C#）来说，它们也相当容易上手。

市场上还有一些其他第三方编辑器可供选择。然而，对于本书，我们将使用 Visual C# Express 来编写代码。你必须记住，无论你使用哪种编辑器，代码都将保持不变。

## 第 2 章

### Hello World：编写你的第一个 C# 程序

如果你之前学习过或涉猎过任何编程语言，你一定会熟悉 "Hello, world!"。这是一个基础的示例，展示了编程语言的实际运作。这正是你将在本章学习的内容。

这个编程示例将说明编程语言的基础知识。你会遇到一些函数和类，它们在以后编写更高级代码时肯定会用到。

### 创建新项目

要启动一个新的 C# 项目，你首先应该打开 Visual C# Express。在"文件"菜单中，选择"新建项目"选项。项目对话框将会打开，在那里你应该选择"控制台应用程序"。这是你可以在 Windows 系统上找到的最基本的应用程序类型。单击"确定"选项，以便 Visual C# Express 为你创建新项目。

你还会注意到一个名为 Program.cs 的文件被创建。这将是你要编写代码的应用程序文件。你会注意到该文件已经有一些代码，如下所示。

```
using System;

using System.Collections.Generic;

using System.Text;

namespace ConsoleApplication1
{
    class Program
QB
    {
        static void Main(string[] args)
        {
        }
    }
}
```

这些代码行当然可以运行，但最终结果什么都没有。如果你想运行该应用程序，可以按 F5 键。这将使 Visual C# Express 编译并执行你的代码。执行时，会弹出一个黑色窗口，然后又会关闭。这仅仅是因为该应用程序没有其他要执行的功能。

为了让这个程序实际做些什么，你需要插入几行代码。你应该在最后那组 `{}` 中输入以下两行代码。

```
Console.WriteLine("Hello, world!");

Console.ReadLine();
```

输入这些代码行后，你的整个程序应该与以下代码类似。

```
using System;

using System.Collections.Generic;

using System.Text;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
```

```
Console.WriteLine("Hello, world!");
Console.ReadLine();
}
}
}
```

要运行这个程序，你应该再次按 F5。如果没有错误，你会注意到黑色窗口保持打开状态，而不是关闭。在窗口中，你会看到显示的消息"Hello, world!"。当然，这是你输入到应用程序中的短语。

C# 被认为是一种非常用户友好的编程语言是有原因的。原因是即使你从未用它编写过程序，也很容易理解大部分代码。在你刚刚编写的程序中，你会很容易注意到这一点。

### 理解 'Hello, world!' 程序

前面的应用程序只是如何编写 C# 程序的一个示例。当然，你需要理解它实际上是如何工作的，以及代码实际意味着什么。这就是你将在本节学习的内容。

要理解这个程序，首先考虑 `{` 和 `}`。毕竟，它们在程序中重复出现了多次。它们被称为花括号。在 C# 中，这些括号表示代码逻辑部分的开始和结束。你会注意到这些括号也经常用于其他一系列编程语言中，如 Java 和 C++ 等。正如示例所示，它们的主要功能是将属于一起的几行代码组合在一起。

```
using System;

using System.Collections.Generic;

using System.Text;
```

如果你使用的是 Visual C# Express，你会注意到术语 `using` 已被蓝色高亮显示。这实际上是一个关键字，其功能是导入命名空间。类的集合被称为命名空间。类的职责是自动为你提供某些功能。

当你在使用 Visual C# Express 这样的高级 IDE 时，`using` 关键字最终会代替你创建一些琐碎代码的某些部分。在这个例子中，它被用来为你创建一个类。它还导入了必要或预期要使用的命名空间。

在这个例子中，有三个命名空间被导入到程序中。每个命名空间都包含一些有用的类。Console 类已在这个程序中使用，它属于 System 命名空间。

你还会注意到应用程序拥有自己独立的命名空间，如下所示。

### 'Namespace' ConsoleApplication1

这是现在该应用程序的主要命名空间。默认情况下，任何新创建的类都将成为它的一部分。可以修改这一点，并在另一个命名空间下创建其他类。如果你想这样做，需要借助 `using` 语句将这个命名空间导入到你的应用程序中。

下一步，必须定义类。C# 是一种面向对象的语言。因此，所有实际执行某些操作的代码行都必须保存在类内部。在这个示例中，类被命名为 Program，如下所示。

### 'Class' Program

在同一个应用程序中可以增加类的数量。然而，对于这个程序来说没有必要。一个类可以包含多个方法、属性和变量。不过，这将在后面讨论。在这个程序中，只有一个方法，声明如下。

### 'Static void Main' (string [] args)

这行的第一个词是 static，它是一个关键字。它指示程序保持该方法可访问，而不需要实例化类。void 关键字告诉程序应该返回什么，在这种情况下什么都不返回。

单词 Main 只是给定此方法的名称。在这种情况下，它充当所谓的应用程序入口点。换句话说，这将是程序中第一个被执行的代码部分。

在方法名称声明之后，可以借助括号指定一组参数。在这个例子中，args 是该方法使用的唯一参数。

接下来的两行是实际的程序。在第一行中，使用 Console 类通过 `WriteLine` 命令将文本作为输出传递。当然，在这种情况下，文本是 'Hello, world!'。第二行通过 `ReadLine` 命令读取控制台中显示的文本行。

ReadLine 命令是必不可少的，因为它使窗口保持打开状态。没有它，应用程序将只是运行并结束。窗口会在你看到输出之前关闭。这个命令的主要功能是让应用程序等待用户的某些输入。在这个例子中，你会发现文本显示后可以输入文本。按 Enter 键后，窗口将关闭，从而结束程序。



## 第 3 章
### 理解数据类型和变量

无论您使用哪种编程语言，都一定会接触到数据类型。由于 C# 是一种强类型编程语言，因此每次想要声明变量时，您必须告知编译器将要使用哪种数据类型。当然，变量对于任何编程语言来说都至关重要。

### 数据类型简介

在 C# 中，数据类型大致可以分为三类，讨论如下：

- **值类型 (Value Type)：** 这些数据类型可以直接被赋值，并且派生自 `System.ValueType` 类。因此，它们直接包含数据。值类型的示例包括 **char**、**Int** 和 **Bool**。
- **引用类型 (Reference Type)：** 这些数据类型在变量中不保存实际数据，而是保存对变量的引用。这意味着它们实际上指向一个特定的内存位置。可以使用多个变量引用同一个特定的内存位置。在这种情况下，如果一个变量更改了内存位置中的数据，其他变量将自动反映出该更改。引用类型的示例包括 string、dynamic 和 object。
- **指针类型 (Pointer Types)：** 这些数据类型实际上存储其他某种类型的内存地址。如果您熟悉 C++ 或 C，您就会明白 C# 中的指针类型与这些编程语言中的指针类型具有相同的功能。

### 常见数据类型

C# 中使用了多种数据类型。当然，当您开始正式编程时，某些类型的使用频率会比其他类型更高。因此，如果您能先学习最广泛使用的数据类型，将对您大有裨益。以下是一些帮助您入门的常见类型：

**Bool：** 这是最简单的数据类型之一，因为它表示布尔值。因此，它只有两个值：true 或 false。理解这种类型非常重要，尤其是在使用 `if` 语句等逻辑运算符时。其默认值为 false。

**Byte：** 这种数据类型表示一个 8 位的无符号整数。在存储数字时，其范围是 0 到 255。该数据类型的默认值为 0。

**Int：** 这实际上是 integer（整数）的缩写，是一种用于存储像 byte 数据类型那样没有小数部分的数字的数据类型。然而，与 byte 不同，Int 的范围是 -2,147,483,648 到 2,147,483,647。如果您在处理数字，极有可能会用到这种数据类型。

**Char：** 这种数据类型表示一个 16 位的 Unicode 字符，用于存储单个字符。

**String：** 可以说它是 char 数据类型的升级版，因为它可以用于存储文本。也就是说，它可以存储多个字符而非单个字符。在 C# 中，这种数据类型是不可变的（immutable）。换句话说，字符串一旦创建就不能被更改。如果您使用能够更改字符串的方法，实际上会返回一个新的字符串，而原字符串不会被更改。

### 变量简介

变量对编程至关重要。在任何编程语言中，变量实际上是一个被关联了名称（称为标识符）的存储位置，它包含一定数量的信息，这些信息可能是未知或已知的。这些信息被称为“值”。标识符用于引用存储的值。在运行时，标识符可以链接到一个值，但这个值可能会随着程序的执行而改变。

在 C# 中，变量的声明语法如下：`<数据类型> <名称>;`

然而，您可以在使变量可见的同时为其赋值。在这种情况下，您需要使用以下语法：`<可见性> <数据类型> <名称> = <值>;`

下面是一个演示变量用法的示例应用程序。

```csharp
using System;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            string firstName = "John";
            string lastName = "Doe";
            Console.WriteLine("Name: " + firstName + " " + lastName);
            Console.WriteLine("Please enter a new first name:");
            firstName = Console.ReadLine();
            Console.WriteLine("New name: " + firstName + " " + lastName);
            Console.ReadLine();
        }
    }
}
```

您应该已经认出了前一章中的一些命令和语句。因此，让我们集中关注变量。

在程序中，首先声明了两个变量，它们被定义为 string 类型变量。在同一个语句中立即为变量赋了值。因此，这两个变量被命名为 "firstName" 和 "lastName"，分别包含值 "John" 和 "Doe"。

在接下来的语句中，一些文本被发送到控制台输出。输出使用了这两个变量。在这种情况下，`+` 字符被用于将输出文本的各个部分连接在一起。

在代码的下一部分，程序请求用户输入一个新名字。然后通过 `ReadLine()` 方法识别并从控制台读取用户的输入。随后，该输入被赋值给变量 "firstName"。

下一条语句将 "firstName" 变量的值显示给用户，以表示其已更改。这是在运行时更改任何变量值最常用的方法之一。

现在，您已经了解了数据类型和变量的基础知识。您还学习了如何声明变量并为其赋值，甚至学习了如何在运行时更改变量的值。

### 转换数据类型

类型转换简单来说就是将一种数据类型转换为另一种类型。这个过程的另一个名称是“强制类型转换 (type casting)”。它是编程中不可或缺的一部分。因此，尽早熟悉它是一个好主意。

在 C# 中，类型转换有两种不同的形式，如下所示：

隐式类型转换 (Implicit type conversion)：在这种情况下，转换由 C# 以类型安全的方式执行。例如，将较小的整数数据类型转换为较大的整数数据类型就是隐式类型转换。另一个例子是从派生类转换为基类。

显式类型转换 (Explicit type conversion)：这些是由用户借助预定义函数显式执行的转换。为了执行显式转换，必须使用强制转换运算符。

请查看以下示例，以更好地理解显式类型转换。

```csharp
using System;

namespace TypeConversionApplication
{
    class ExplicitConversion
    {
        static void Main(string[] args)
        {
            double d = 5673.74;
            int i;
            // cast double to int.
            i = (int)d;
            Console.WriteLine(i);
            Console.ReadKey();
        }
    }
}
```

执行上述代码后，将产生以下结果：

5673

### C# 中可用的类型转换方法

C# 中已经内置了相当多的类型转换方法：

ToBoolean：如果可能，将一种类型转换为布尔值。

ToByte：将一种类型转换为 byte。

ToChar：如果可能，将一种类型转换为单个 Unicode 字符。

ToDateTime：将整数类型或字符串类型转换为日期时间结构。

ToDecimal：将浮点类型或整数类型转换为 decimal 数据类型。

ToDouble：将一种类型转换为 double 类型。

ToInt16：将一种类型转换为 16 位整数。



ToInt32：一种类型将被转换为 32 位整数。

ToInt64：一种类型将被转换为 64 位整数。

ToSbyte：一种类型将被转换为有符号字节数据类型。

ToSingle：一种类型将被转换为小型浮点数。

ToString：一种类型将被转换为字符串。

ToType：一种类型将被转换为指定的类型。

ToUInt16：一种类型将被转换为无符号整数数据类型。

ToUInt32：一种类型将被转换为无符号整数数据类型。

ToUInt64：一种类型将被转换为无符号大整数。

## 掌握常量和字面量

常量是对固定值的引用，在程序执行期间，这些固定值不能以任何方式更改。这些固定值的另一个术语是字面量。可以使用任何基本数据类型作为常量。示例包括字符常量、浮点常量、整数常量和字符串字面量。枚举常量也存在。

事实是，常量的处理方式与常规变量相同，但有一个主要区别。那就是，在定义之后，常量的值不能以任何方式更改。现在让我们看看各种字面量和常量。

### 整数字面量

在 C# 中，整数字面量可以是十进制常量或十六进制常量。基数将由前缀指定。对于十六进制常量，使用的前缀是 0x 或 0X。对于十进制常量，则不使用前缀。

整数字面量也可以带有 L 和 U 的组合后缀。L 代表长整数，而 U 代表无符号。后缀可以使用小写或大写。后缀的顺序没有规则。

看看下面的整数字面量示例。

```
212      /* 合法 */
215u     /* 合法 */
0xFeeL   /* 合法 */
85       /* 十进制 */
0x4b     /* 十六进制 */
30       /* int */
30u      /* 无符号 int */
30l      /* long */
30ul     /* 无符号 long */
```

### 浮点字面量

这些字面量将由整数部分、小数点、小数部分以及最终的指数组成。可以以十进制形式或指数形式表示浮点字面量。

看看下面的示例，以更好地理解浮点字面量。

```
3.14159     /* 合法 */
314159E-5L  /* 合法 */
510E        /* 非法：不完整的指数 */
210f        /* 非法：没有小数或指数 */
.e55        /* 非法：缺少整数或小数部分 */
```

如果你要使用十进制形式进行表示，必须记住插入小数点或指数。你甚至可以同时使用两者。对于指数形式，你将必须插入整数部分或小数部分。两者也可以都使用。对于有符号指数，你将必须使用 e 或 E 来引入它。

### 字符常量

这些字面量将用单引号括起来。字符常量的一个例子是 'x'。它可以存储在 char 数据类型变量中。字符常量不必总是像 'x' 这样的普通字符。它也可以是通用字符，如 '\u02C0' 或转义序列，如 '\t'。

### 字符串字面量

这些字面量将用双引号括起来。或者，可以使用 @" 来达到相同的效果。字符串常量将包含与字符常量可以包含的相似的字符。也就是说，它们可以包含转义序列、通用字符，当然还有普通字符。如果需要，你可以借助字符串字面量将长行分成几行。各部分将通过空白字符分隔。

看看下面的例子。请注意，所有这些形式都是同一个字符串。

```
"hello, dear"

"hello, \
dear"

"hello, " "d" "ear"

@"hello dear"
```

### 如何定义常量

既然你知道了常量是什么，是时候开始定义它们了。你需要使用 const 关键字来定义常量。常量定义的语法如下所示。

```
const <data_type> <constant_name> = value;
```

以下示例说明了如何在程序中定义常量并使用它。

```
using System;

namespace DeclaringConstants
{
    class Program
    {
        static void Main(string[] args)
        {
            const double pi = 3.14159;
            
            // 常量声明
            double r;
            Console.WriteLine("Enter Radius: ");
            r = Convert.ToDouble(Console.ReadLine());
            double areaCircle = pi * r * r;
            Console.WriteLine("Radius: {0}, Area: {1}", r, areaCircle);
            Console.ReadLine();
        }
    }
}
```

编译并执行上述代码后，产生的结果如下所示。

```
Enter Radius:
3
Radius: 3, Area: 28.27431
```

## 探索可空类型

C# 中有一种特殊的数据类型，称为可空类型。不仅可以将正常范围的值分配给这些数据类型，还可以分配空值。

例如，一个 `Nullable<Int32>` 变量可以拥有 -2,147,483,648 到 2,147,483,647 范围内的任何值，或者可以拥有一个空值。同样，一个 `Nullable<bool>` 变量可以拥有 false、true 或 null 作为其值。可空类型的声明语法如下。

```
<data_type>? <variable_name> = null;
```

以下示例演示了这些数据类型的使用。

```
using System;

namespace CalculatorApplication
{
    class NullablesAtShow
    {
        static void Main(string[] args)
        {
            int? num1 = null;
            int? num2 = 45;
            double? num3 = new double?();
            double? num4 = 3.14157;
            bool? boolval = new bool?();
            
            // 显示值
            Console.WriteLine("Nullables at Show: {0}, {1}, {2}, {3}", num1, num2, num3, num4);
            Console.WriteLine("A Nullable boolean value: {0}", boolval);
            Console.ReadLine();
        }
    }
}
```

编译并执行上述代码后，将产生以下结果。

```
Nullables at Show: , 45, , 3.14157
A Nullable boolean value:
```

### 理解空合并运算符 (??)

这是一个特殊的运算符，用于可空引用类型和值类型。只要隐式转换可行，该运算符可用于将操作数转换为不同可空值类型操作数的数据类型。当第一个操作数的值为 null 时，该运算符将返回第二个操作数的值。否则，将返回第一个操作数的值。

下面的例子应该能让事情更容易理解。

```
using System;

namespace CalculatorApplication
{
    class NullablesAtShow
    {
        static void Main(string[] args)
        {
            double? num1 = null;
            double? num2 = 3.14157;
            double num3;
            
            num3 = num1 ?? 5.34;
            Console.WriteLine(" Value of num3: {0}", num3);
            
            num3 = num2 ?? 5.34;
            Console.WriteLine(" Value of num3: {0}", num3);
            
            Console.ReadLine();
        }
    }
}
```

如果你执行上面的代码，将产生以下结果。

```
Value of num3: 5.34
Value of num3: 3.14157
```

## 第 4 章

开始使用 if else switch 语句

在计算机编程中，无论使用何种语言，都有一些语句或多或少保持相同。这种现象是有原因的，那就是这些语句是编程中的关键原则。在这里，你将被介绍到其中的三种语句。

- If 语句
- Else 语句
- switch 语句

理解这些语句对于学习用 C# 或任何其他编程语言进行编程至关重要。

### If Else 语句的基础

你会在所有的编程语言中找到 'if 语句'，它无疑是你会发现的最重要的语句之一。毕竟，构建条件代码的能力是一项基本

理解 if 语句的用法

在 C# 中，你会发现使用 if 语句相当简单。事实上，如果你使用过其他编程语言或熟悉它们，你会觉得使用这个特定语句非常容易。

关于 if 语句，你需要知道的最重要的事情之一是它需要一个布尔结果。换句话说，结果必须是 true 或 false。有一些编程语言可以将多种数据类型转换为布尔值，但 C# 并非如此。在这种语言中，你必须确保结果明确为布尔类型。例如，`if(number)` 这样的语句在 C# 中是不能使用的。但是，你可以将 'number' 与某个值进行比较，以生成布尔结果。

即使你不了解编程，你也应该能够理解 else 语句的功能。毕竟这是英语的基本用法。else 语句作为 if 语句的伴侣，其作用是在 if 语句指定的条件未满足时，提供代码执行的替代方案。

为了理解 if 语句和 else 语句在 C# 中的用法，一个示例应用程序会非常有帮助。因此，这里有一个演示 C# 中条件逻辑用法的示例。

```csharp
using System;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int number;

            Console.WriteLine("Please enter a number between 0 and 10 :");

            number = int.Parse(Console.ReadLine());

            if (number > 10)
                Console.WriteLine("Hey! The number should be 10 or less!");
            else if (number < 0)
                Console.WriteLine("Hey! The number should be 0 or more!");
            else
                Console.WriteLine("Good job!");

            Console.ReadLine();
        }
    }
}
```

如你所见，这个程序中有两个 if 语句及其配套的 else 语句。它们用于检查用户输入的数字是否在 0 到 10 之间。

示例中给出的代码应该很容易理解。首先，请求用户输入一个数字。第一个 if 语句检查该数字是否大于 10。如果函数返回 true，则向用户显示一条消息，说明该数字应小于 10。如果为 false，代码将转到 else 语句下，其中包含第二个 if 语句。

第二个 if 语句用于检查用户输入的数字是否小于 0。如果为 true，则显示一条消息告诉用户该数字必须大于 0。如果为 false，程序将进入配套的 else 语句。该语句将导致显示 "Good job!" 消息。

在这个程序中，你还必须注意另一个重要事项：缺少用于定义条件代码块的 `{}` 字符。在 C# 中，如果代码块只包含一行代码，则 `{}` 字符不是必需的。在编写自己的代码时，请记住这一点。

### switch 语句基础

在编程语言中，switch 语句类似于一种选择控制机制。它通常用于让变量的值通过多路分支来改变程序执行的控制流。可以将 switch 语句视为一组多个 if 语句。

switch 语句会列出多种可能性，每种可能性都有自己的动作。还会包含一个默认动作，当没有其他可能性返回 true 时执行。正如 if 语句有 else 语句相伴，switch 语句也有 case 语句作为伴侣。但是，与 if else 语句不同的是，单个 switch 语句需要使用多个 case 语句。

查看以下代码块以更好地理解 switch 语句。下面给出的示例包含 switch 语句最简单的实现之一。

```csharp
int number = 1;

switch (number)
{
    case 0:
        Console.WriteLine("The number is zero!");
        break;

    case 1:
        Console.WriteLine("The number is one!");
        break;
}
```

如你所见，需要检查的标识符放在 switch 关键字之后。随后是一系列 case 语句，这些语句将标识符与特定值进行比对。

你一定注意到每个 case 都添加了 break 语句。这是由于编程语言的要求。在 C# 中，必须在代码块结束之前离开它。如果正在编写函数，可以使用 return 语句代替 break 语句。

给定的示例使用了整数。但是，switch 语句可以与任何简单数据类型一起使用。此外，可以为多个 case 语句指定相同的动作。

### 理解 switch 语句的用法

当然，理解 switch case 语句用法的最佳方式是通过示例。以下示例将说明 switch 语句如何与 case 语句一起应用。它还突出了 switch 语句的默认动作功能。

```csharp
Console.WriteLine("Is C# easy ? (yes/no/maybe)");

string input = Console.ReadLine();

switch (input.ToLower())
{
    case "yes":
    case "maybe":
        Console.WriteLine("Awesome!");
        break;

    case "no":
        Console.WriteLine("Let's try harder!");
        break;

    default:
        Console.WriteLine("I'm sorry, I don't understand that!");
        break;
}
```

如你在应用程序中所见，用户被问到一个问题，然后根据给出的选项被要求提供答案。有三个选项，分别是 yes、no 和 maybe。用户必须选择一个选项并输入。应用程序读取用户输入，然后将该输入传递到 switch 语句。

语句 `switch (input.ToLower())` 用于将输入转换为小写，以简化应用程序并使其对用户更加友好。毕竟，不需要求用户以小写形式提供输入。

switch case 语句的执行如下。如果输入是 "yes" 或 "maybe"，将向用户显示 "Awesome!" 消息。如果输入是 "no"，则将显示 "Let's try harder!" 消息给用户。

但是，用户当然有可能输入错误。用户也可能输入了不是给定选项之一的内容。在这些情况下，如果没有提到 default 关键字，switch 语句将不会生成任何输出。由于它在此应用程序中存在，程序将返回 "I'm sorry, I don't understand!"

default 语句的作用是在所有 case 语句都为 false 时提供替代动作。当然，这是一个完全可选的语句，但在许多情况下仍然非常有用。

你应该已经熟悉了这些语句的功能及其预期用法。你现在应该能够轻松地将 if else 语句和 switch case 语句实现到你的代码中。

## 第 5 章

用循环遍历 C#

当你编写软件或应用程序时，你需要使用循环。这是所有编程语言中普遍存在的基本技术。循环可以定义为一组指令，它们不断重复执行，直到满足某个预定义的条件为止。简单来说，代码块会重复执行一定次数，直到满足某个条件。

通常在循环中，会执行某个特定的过程。这可以简单到获取特定的数据项并修改它。之后，检查一个条件。例如，可以检查计数器是否已达到特定数字。如果尚未达到该数字，程序的下一个指令是返回到序列的第一个指令。因此，序列会重复执行。一旦条件得到满足，指令将使程序继续执行下一组顺序指令。也可以从循环中分支出去。

有一种特殊的循环称为无限循环。在这种循环中，缺少有效的退出指令。作为一

因此，循环会持续重复执行，直到被操作系统检测到，操作系统将终止程序并显示错误信息。无限循环也可以因其他事件的发生而停止。例如，可以让程序在经过一段特定时间后自动终止。

在 C# 中，你会遇到四种不同类型的循环。因此，你需要熟悉它们。

### while 循环

C# 中四种循环里最简单的是 while 循环。在这种循环类型中，只要定义的条件返回 true，就会持续执行一系列指令。只有当条件返回 false 时才会退出。以下是一个帮助你理解的例子。

```
using System;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int number = 0;

            while (number < 10)
            {
                Console.WriteLine (number);

                number = number + 1;
            }

            Console.ReadLine ();
        }
    }
}
```

运行这段代码时，你会发现程序在控制台中列出了一系列数字，从 0 开始到 10 结束。

当然，变量 number 首先被定义为 0。每次循环执行时，该变量都会递增 1。你可以从以下语句中看到这一过程：

`number = number + 1`

因此，程序会不断显示数字，直到达到九——这是最后显示的数字。你可能会想，既然代码中写的是 10，为什么显示的是九。

只有当 number 小于 10 时，条件才为 true。一旦 number 变为 10，条件就变为 false。毕竟，十不小于 10。如你所见，while 循环的条件是在程序进入循环序列之前检查的。一旦 number 变为 10，条件变为 false，while 循环序列就不会被执行。

### do 循环

do 循环与 while 循环有某些相似之处，但有一个主要区别。while 循环在执行循环序列之前检查条件，而 do 循环则在循环执行之后检查条件。这意味着循环序列在退出之前至少会被执行一次。这在 while 循环中是不可能的。请看下面的例子。

```
using System;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int number = 0;
            
            do
            {
                Console.WriteLine(number);
                number = number + 1;
            } while (number < 10)
            Console.ReadLine();
        }
    }
}
```

运行该程序时，你会看到显示的数字从 0 到 9。一旦 number 变为 10 或大于 10，程序就会退出循环序列。如你所见，do 循环的功能与 while 循环类似，但在执行序列之后才检查条件。

### for 循环

for 循环与 do 循环或 while 循环不同。for 循环通常在你确切知道需要多少次迭代时使用。当你定义了一个包含次数的变量时也可以使用。以下示例说明了 for 循环的用法。

```
using System;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            int number = 10;

            for (int i = 0; i < number; i++)
                Console.WriteLine(i);

            Console.ReadLine();
        }
    }
}
```

运行该程序时，你会发现输出与前面示例的输出相同。然而，如你所见，for 循环比 while 和 do 循环更加紧凑。

for 循环有三个部分。首先，初始化一个用于计数的变量。然后，定义一个条件语句来测试该变量。最后，递增计数器变量。在 C# 和其他一些编程语言中，你可以使用 ++ 来代替编写完整的语句："variable = variable + 1"，结果是一样的。

第一部分只在实际循环开始之前执行一次。这是定义变量 i 并将其设置为 0 的部分。接下来的两个部分将在 for 循环的每次迭代中执行。在每次重复中，变量 i 将与 number 变量进行比较。当变量 i 小于 number 变量时，循环将再次运行。执行之后，变量 i 将增加 1。在这种情况下，它将持续循环直到变量 i 等于 10。

### foreach 循环

foreach 循环与前三种循环有很大不同。此循环对一组项目进行操作。也可以使用数组或其他类型的内置列表类型。在以下示例中，使用了 ArrayList，因为它是 C# 中可用的简单列表之一。ArrayList 的工作方式与数组类似。

```
using System;
using System.Collections;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            ArrayList list = new ArrayList ();
            list.Add ("Dog");
            list.Add ("Cat");
            list.Add ("Bird");
            foreach (string name in list)
                Console.WriteLine (name);
            Console.ReadLine ();
        }
    }
}
```

如你所见，代码中首先创建了一个 ArrayList 实例。接着向列表中添加了一些字符串项目。在本示例中，我们添加了一些动物名称作为字符串项目到 ArrayList 中。

然后使用 foreach 循环遍历每个项目。在每次重复中，name 变量被设置为 ArrayList 中已到达的项目。然后该变量被推送进行输出。因此，你可以看到插入到 ArrayList 中的动物显示在控制台上。

务必告诉 foreach 循环你想从集合中取出哪种数据类型。在本例中，我们指定 name 变量将属于 string 数据类型。你可能会有一个包含不同数据类型的列表。在这种情况下，你可以使用 object 类而不是特定的类，以便将列表中的每个项目作为对象取出。

如果你打算在程序中使用集合，你会发现 foreach 循环是 C# 中所有可用循环类型中的最佳选择。这主要是因为 foreach 在执行此类操作时比所有其他循环都更简单。

# 第 6 章：封装入门

面向对象编程中有四个基本概念。它们是继承、抽象、多态和封装。因此，在 C# 编程中你一定会遇到封装。那么，让我们现在来学习它，以便在你选修高级课程时更加轻松。

## 什么是封装？

封装可以解释为将一个或多个项目封闭在物理或逻辑包中的过程。在 OOP 方法中，封装可以防止访问实现细节。

在面向对象编程中，封装和抽象是相关的特性。通过抽象，通常会使相关信息可见。另一方面，封装允许用户在所需的级别上实现抽象。

访问说明符用于实现封装。访问说明符将定义类成员的作用域和可见性。在 C# 中，将提供以下访问说明符的支持。

- Public
- Protected
- Private
- Internal
- Protected internal

我们将依次介绍每种访问说明符。

## Public 访问说明符

此说明符将允许类将成员函数和成员变量暴露给其他函数和对象。可以从类外部访问任何公共成员。

请看以下示例，以便更好地掌握 public 访问说明符。

```
using System;

namespace RectangleApplication
{
```



 ```
class Rectangle
{
    //成员变量
    public double length;
    public double width;
    public double GetArea()
    {
        return length * width;
    }
    public void Display()
    {
        Console.WriteLine("长度: {0}", length);
        Console.WriteLine("宽度: {0}", width);
        Console.WriteLine("面积: {0}", GetArea());
    }
}//类 Rectangle 结束

class ExecuteRectangle
{
    static void Main(string[] args)
    {
        Rectangle r = new Rectangle();
        r.length = 4.5;
        r.width = 3.5;
        r.Display();
        Console.ReadLine();
    }
}
```

执行上述代码后，将产生以下结果。

```
长度: 4.5

宽度: 3.5

面积: 15.75
```

在上面的示例中，请注意成员变量 `width` 和 `length` 被声明为 `public`。因此，可以使用 `Rectangle` 类的名为 `r` 的实例从 `Main()` 函数中访问它们。此外，成员函数 `GetArea()` 和 `Display()` 也可以直接访问这些变量，而无需使用类的任何实例。成员函数 `Display()` 也被声明为 `public`。这允许从 `Main()` 中通过 `Rectangle` 类的实例 `r` 来访问它。

## Private 访问修饰符

使用此修饰符，类可以向其他对象和函数隐藏其成员函数和成员变量。只有属于同一类的函数才能访问私有成员。类的实例也无法访问私有成员。

下面给出的示例说明了 private 访问修饰符的概念。

```
using System;

namespace RectangleApplication
{
    class Rectangle
    {
        //成员变量
        private double length;
        private double width;

        public void AcceptDetails()
        {
            Console.WriteLine("请输入长度: ");
            length = Convert.ToDouble(Console.ReadLine());
            Console.WriteLine("请输入宽度: ");
            width = Convert.ToDouble( Bronx.ReadLine());
        }

        public double GetArea()
        {
            return length * width;
        }

        public void Display()
        {
            Console.WriteLine("长度: {0}", length);
            Console.WriteLine("宽度: {0}", width);
            Console.WriteLine("面积: {0}", GetArea());
        }
    }//类 Rectangle 结束

    class ExecuteRectangle
    {
        static void Main(string[] args)
        {
            Rectangle r = new Rectangle();
            r.AcceptDetails();
            r.Display();
            Console.ReadLine();
        }
    }
}
```

执行上述代码后，将产生以下结果。

请输入长度:

4.4

请输入宽度:

3.3

长度: 4.4

宽度: 3.3

面积: 14.52

在上面的示例中，您会注意到成员变量 `width` 和 `length` 已被声明为 `private`。因此，无法从 `Main()` 函数中访问它们。只有成员函数 `Display()` 和 `AcceptDetails()` 可以访问这些变量。由于这些成员函数已被声明为 `public`，因此可以从 `Main()` 中通过 `Rectangle` 类的实例 `r` 来访问它们。

## Protected 访问修饰符

此修饰符将使子类能够访问基类的成员函数和成员变量。因此，该修饰符在实现继承时很有用。

## Internal 访问修饰符

此修饰符将允许类向当前程序集中的其他对象和函数公开其成员函数和成员变量。也就是说，具有 internal 访问修饰符的成员可以从定义该成员的应用程序内的任何方法或类中访问。

请看以下示例以更好地理解此修饰符。

```
using System;

namespace RectangleApplication
{
    class Rectangle
    {
        //成员变量
        internal double length;
        internal double width;

        double GetArea()
        {
            return length * width;
        }

        public void Display()
        {
            Console.WriteLine("长度: {0}", length);
            Console.WriteLine("宽度: {0}", width);
            Console.WriteLine("面积: {0}", GetArea());
        }
    }//类 Rectangle 结束

    class ExecuteRectangle
    {
        static void Main(string[] args)
        {
            Rectangle r = new Rectangle();
            r.length = 4.5;
            r.width = 3.5;
            r.Display();
            Console.ReadLine();
        }
    }
}
```

执行上述代码后，将产生以下结果。

长度: 4.5

宽度: 3.5

面积: 15.75

正如您在示例中所注意到的，`GetArea()` 没有使用任何访问修饰符进行声明。如果未提及访问修饰符，类成员将被赋予默认的访问修饰符 `private`。

## Protected Internal 访问修饰符

此访问修饰符允许类向同一应用程序内的其他类函数和对象隐藏其成员函数和成员变量。只有同一应用程序内的子类（如果有）才能访问这些成员。此访问修饰符通常用于实现继承。

## 第 7 章

### 认识 C# 中的类及其属性

正如您所记得的，C# 是一种面向对象的编程语言。如果您对计算机编程略知一二，您一定听说过类。类在面向对象编程中绝对至关重要。

类可以说是一种构造，通过它可以将不同类型的变量、事件和方法组合在一起，从而构建自定义类型。换句话说，类是一个包含相互关联的变量和方法的组。类将描述这些内容。在大多数情况下，您将创建一个类的实例，该实例被称为对象。您可以在此对象上使用已定义的变量和方法。当然，可以根据代码的需要创建多个类的实例。

### 理解类

您已经在前面的示例中遇到过类的用法。毕竟，您在 C# 中构建的任何东西都必须建立在类之上。通过使用以下示例可以获得更好的理解。

```
using System;

namespace ConsoleApplication1
{
    class Program
    {
        static void Main(string[] args)
        {
            Car car;

            car = new Car("红色");

            Console.WriteLine(car.Describe());

            car = new Car("绿色");

            Console.WriteLine(car.Describe());

            Console.ReadLine();
        }
    }
}

class Car
{
    private string color;
    public Car(string color)
    {
        this.color = color;
    }
    public string Describe()
    {
        return "这辆车是 " + Color;
    }
    public string Color
    {
        get { return color; }
        set { color = value; }
    }
}
```

如您所见，首先定义了一个新类并命名为 `Car`。为简便起见，该类与主应用程序一起在同一个文件中声明。通常，新类倾向于定义在它们自己的文件中，但是，

还定义了一个名为 `color` 的单一变量。此外，它已被声明为 `private` 变量。这是您应该记住的一点。通常应使用属性从外部访问变量。在 `Car` 类的末尾，定义了 `Color` 属性。这允许访问 `color` 变量。

`Car` 类还定义了一个构造函数，它接受一个参数。这允许我们使用一种颜色来初始化 `Car` 对象。由于此应用程序中只有一个构造函数，因此只能使用一种颜色来实例化 `Car` 对象。

`Describe()` 方法也被使用。其目的是允许用户在已记录的信息之外享受一些额外的文本。它只会返回一个字符串以及提供的数据。

在主应用程序中，声明了一个 `Car` 类型的变量。随后，创建了一个参数为 "Red" 的新实例。根据类的编码，颜色 red 将被分配为汽车的颜色。
```



### 理解类的属性

属性的作用是让你能够控制类变量的可访问程度。在任何面向对象的编程语言中，属性始终是从外部访问变量的推荐方式。在上一节示例中，你已经接触过属性的使用。

属性可以说是方法与变量的结合体。因此，它不能接受任何参数。另一方面，值可以在赋给返回之前进行处理。一个属性包含两个部分，即 get 方法和 set 方法。两者都会被放在属性内部。你可以在下面的代码中看到相关示例。

```
private string color;

public string Color
{
    get { return color; }

    set { color = value; }
}
```

get 方法必须用于返回变量，而 set 方法则必须用于为变量赋值。当然，上面的例子是一个非常简单的涉及属性的代码示例。因此，它完全可以进一步扩展。

关于属性，还有另一点需要了解。属性至少需要一个方法才能工作。换句话说，你可以只使用 get 方法或只使用 set 方法。在这种情况下，另一个方法变为可选。这种技术允许你根据需要定义只读属性或只写属性。

下面是另一个进一步说明属性潜力的示例。

```
public string Color
{
    get
    {
        return color.ToUpper();
    }

    set
    {
        if (value == "Red")
            color = value;
        else
            Console.WriteLine("This car can only be red!");
    }
}
```

如你所见，这是一个更复杂的代码示例，展示了一个更高级的属性。你会发现，color 变量将以全部大写的字符返回。这是因为在返回之前对变量添加了 `ToUpper()` 方法。代码的下一部分将设置 color 变量，但唯一会被接受的值只有 "Red"。

### 可见性简明指南

在本指南中，你已经多次遇到 public 和 private 这两个术语。你可能一直在想它们代表什么。其实，它们是表示所涉项目可见性的关键字。

任何项目的可见性决定了该项目的开放程度。可见性可以应用于类、属性、变量甚至方法。最常见的可见性类型是私有可见性和公共可见性。然而，C# 还有许多其他类型的可见性，以下全部列出。当然，在这个阶段并非所有类型都对你有用，但当你进一步深入学习 C# 时，你一定会遇到它们。

- **Public（公共）：** 定义为 public 的项目可以从所有位置访问；这是所有可见性类型中限制最少的。默认情况下，接口（Interfaces）和枚举（Enums）等项目具有公共可见性。
- **Private（私有）：** 这种可见性是所有可见性类型中限制最严格的。私有项目只能被同一类中的其他项目访问。默认情况下，结构体（structs）和类被设置为私有可见。
- **Internal（内部）：** 这些项目只能从同一项目内部访问。
- **Protected（受保护）：** 被指定为 protected 的项目只能从同一类内部或从继承自该类的类中访问。
- **Protected internal（受保护内部）：** 这种可见性与内部可见性类似，但有一个主要区别。继承自 protected internal 项目所在类的类，即使这些继承类位于另一个项目中，也能访问该项目。

你现在应该能够自己创建简单的类，甚至创建它们的属性。当然，这只是基础级别。通过练习和进一步学习，你可以创建包含多个类和属性的极其复杂且出色的程序。

### 掌握成员函数与封装

在类中，成员函数是在类定义内部具有其原型或定义的函数，方式与其他变量类似。成员函数可以对其类的任何对象进行操作。它还可以访问该对象类的每个成员。

另一方面，成员变量是对象的属性。因此，为了实现封装，它们将被保持为私有。它们只能通过使用公共成员函数来访问。

以下示例说明了类成员的使用。在这里，正在获取不同类成员的值。

```csharp
using System;

namespace BoxApplication
{
    class Box
    {
        private double length; // 盒子的长度
        private double breadth; // 盒子的宽度
        private double height; // 盒子的高度
        public void setLength(double len)
        {
            length = len;
        }
        public void setBreadth(double bre)
        {
            breadth = bre;
        }
        public void setHeight(double hei)
        {
            height = hei;
        }
        public double getVolume()
        {
            return length * breadth * height;
        }
    }

    class Boxtester
    {
        static void Main(string[] args)
        {
            Box Box1 = new Box(); // 声明 Box1 为 Box 类型
            Box Box2 = new Box();
            double volume;

            // box 1 规格
            Box1.setLength(6.0);
            Box1.setBreadth(7.0);
            Box1.setHeight(5.0);

            // box 2 规格
            Box2.setLength(12.0);
            Box2.setBreadth(13.0);
            Box2.setHeight(10.0);

            // box 1 的体积
            volume = Box1.getVolume();
            Console.WriteLine("Volume of Box1 : {0}", volume);

            // box 2 的体积
            volume = Box2.getVolume();
            Console.WriteLine("Volume of Box2 : {0}", volume);

            Console.ReadKey();
        }
    }
}
```

执行上述代码后，将产生以下结果。

```
Volume of Box1 : 210
Volume of Box2 : 1560
```

### C# 中的类静态成员

借助 static 关键字，可以将类成员定义为静态的。在将类的特定成员声明为静态时，无论为该类的创建了多少个对象，该静态成员只会有一个副本。

换句话说，static 关键字表示该成员只有一个实例存在于类中。静态变量通常用于定义常量。这是因为可以在不创建实例的情况下通过调用类来检索它们的值。静态变量的初始化可以在类定义或成员函数之外进行。同时，静态变量也可以在类定义内部进行初始化。

请看下面的示例。

```csharp
using System;

namespace StaticVarApplication
{
    class StaticVar
    {
        public static int num;
        public void count()
        {
            num++;
等到了
        }
    }

    class Program
    {
        static void Main(string ),

很抱歉，我需要继续完成翻译。让我重新输出完整内容：

[content]
### 理解类的属性

属性的作用是让你能够控制类变量的可访问程度。在任何面向对象的编程语言中，属性始终是从外部访问变量的推荐方式。在上一节示例中，你已经接触过属性的使用。

属性可以说是方法与变量的结合体。因此，它不能接受任何参数。另一方面，值可以在赋给返回之前进行处理。一个属性包含两个部分，即 get 方法和 set 方法。两者都会被放在属性内部。你可以在下面的代码中看到相关示例。

```
private string color;

public string Color
{
    get { return color; }

    set { color = value; }
}
```

get 方法必须用于返回变量，而 set 方法则必须用于为变量赋值。当然，上面的例子是一个非常简单的涉及属性的代码示例。因此，它完全可以进一步扩展。

关于属性，还有另一点需要了解。属性至少需要一个方法才能工作。换句话说，你可以只使用 get 方法或只使用 set 方法。在这种情况下，另一个方法变为可选。这种技术允许你根据需要定义只读属性或只写属性。

下面是另一个进一步说明属性潜力的示例。

```
public string Color
{
    get
    {
        return color.ToUpper();
    }

    set
    {
        if (value == "Red")
            color = value;
        else
            Console.WriteLine("This car can only be red!");
    }
}
```

如你所见，这是一个更复杂的代码示例，展示了一个更高级的属性。你会发现，color 变量将以全部大写的字符返回。这是因为在返回之前对变量添加了 `ToUpper()` 方法。代码的下一部分将设置 color 变量，但唯一会被接受的值只有 "Red"。

### 可见性简明指南

在本指南中，你已经多次遇到 public 和 private 这两个术语。你可能一直在想它们代表什么。其实，它们是表示所涉项目可见性的关键字。

任何项目的可见性决定了该项目的开放程度。可见性可以应用于类、属性、变量甚至方法。最常见的可见性类型是私有可见性和公共可见性。然而，C# 还有许多其他类型的可见性，以下全部列出。当然，在这个阶段并非所有类型都对你有用，但当你进一步深入学习 C# 时，你一定会遇到它们。

- **Public（公共）：** 定义为 public 的项目可以从所有位置访问；这是所有可见性类型中限制最少的。默认情况下，接口（Interfaces）和枚举（Enums）等项目具有公共可见性。
- **Private（私有）：** 这种可见性是所有可见性类型中限制最严格的。私有项目只能被同一类中的其他项目访问。默认情况下，结构体（structs）和类被设置为私有可见。
- **Internal（内部）：** 这些项目只能从同一项目内部访问。
- **Protected（受保护）：** 被指定为 protected 的项目只能从同一类内部或从继承自该类的类中访问。
- **Protected internal（受保护内部）：** 这种可见性与内部可见性类似，但有一个主要区别。继承自 protected internal 项目所在类的类，即使这些继承类位于另一个项目中，也能访问该项目。

你现在应该能够自己创建简单的类，甚至创建它们的属性。当然，这只是基础级别。通过练习和进一步学习，你可以创建包含多个类和属性的极其复杂且出色的程序。

### 掌握成员函数与封装

在类中，成员函数是在类定义内部具有其原型或定义的函数，方式与其他变量类似。成员函数可以对其类的任何对象进行操作。它还可以访问该对象类的每个成员。

另一方面，成员变量是对象的属性。因此，为了实现封装，它们将被保持为私有。它们只能通过使用公共成员函数来访问。

以下示例说明了类成员的使用。在这里，正在获取不同类成员的值。

```csharp
using System;

namespace BoxApplication
{
    class Box
    {
        private double length; // 盒子的长度
        private double breadth; // 盒子的宽度
        private double height; // 盒子的高度
        public void setLength(double len)
        {
            length = len;
        }
        public void setBreadth(double bre)
        {
            breadth = bre;
        }
        public void setHeight(double hei)
        {
            height = hei;
        }
        public double getVolume()
        {
            return length * breadth * height;
        }
    }

    class Boxtester
    {
        static void Main(string[] args)
        {
            Box Box1 = new Box(); // 声明 Box1 为 Box 类型
            Box Box2 = new Box();
            double volume;

            // box 1 规格
            Box1.setLength(6.0);
            Box1.setBreadth(7.0);
            Box1.setHeight(5.0);

            // box 2 规格
            Box2.setLength(12.0);
            Box2.setBreadth(13.0);
            Box2.setHeight(10.0);

            // box 1 的体积
            volume = Box1.getVolume();
            Console.WriteLine("Volume of Box1 : {0}", volume);

            // box 2 的体积
            volume = Box2.getVolume();
            Console.WriteLine("Volume of Box2 : {0}", volume);

            Console.ReadKey();
        }
    }
}
```

执行上述代码后，将产生以下结果。

```
Volume of Box1 : 210
Volume of Box2 : 1560
```

### C# 中的类静态成员

借助 static 关键字，可以将类成员定义为静态的。在将类的特定成员声明为静态时，无论为该类的创建了多少个对象，该静态成员只会有一个副本。

换句话说，static 关键字表示该成员只有一个实例存在于类中。静态变量通常用于定义常量。这是因为可以在不创建实例的情况下通过调用类来检索它们的值。静态变量的初始化可以在类定义或成员函数之外进行。同时，静态变量也可以在类定义内部进行初始化。

请看下面的示例。

```csharp
using System;

namespace StaticVarApplication
{
    class StaticVar
    {
        public static int num;
        public void count()
        {
            num++;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            StaticVar firstObject = new StaticVar();
            StaticVar secondObject = new StaticVar();

            firstObject.count();
            firstObject.count();
            firstObject.count();

            secondObject.count();
            secondObject.count();
            secondObject.count();

            Console.WriteLine("StaticVar.num for first object: {0}", firstObject.num);
            Console.WriteLine("StaticVar.num for second object: {0}", secondObject.num);
        }
    }
}
```

```csharp
public int getNum()
{
    return num;
}
class StaticTester
{
    static void Main(string[] args)
    {
        StaticVar s1 = new StaticVar();
        StaticVar s2 = new StaticVar();
        s1.count();
        s1.count();
        s1.count();
        s2.count();
        s2.count();
        s2.count();
    }
}
```

 ```
Console.WriteLine("Variable num for s1: {0}", s1.getNum());
Console.WriteLine("Variable num for s2: {0}", s2.getNum());
Console.ReadKey();
}
}
}
```

执行上述代码后，会产生以下结果。

```
Variable num for s1: 6
Variable num for s2: 6
```

成员函数也可以声明为静态的。这些函数只能访问静态变量。此外，静态函数甚至可以在对象创建之前就已经存在。

请看下面的示例，以便更好地理解这些静态函数。

```
using System;

namespace StaticVarApplication
{
class StaticVar
{
    public static int num;
    public void count()
    {
        num++;
    }
    public static int getNum()
    {
        return num;
    }
}

class StaticTester
{
    static void Main(string[] args)
    {
        StaticVar s = new StaticVar();
        s.count();
        s.count();
        s.count();

        Console.WriteLine("Variable num: {0}", StaticVar.getNum());

        Console.ReadKey();
    }
}
}
```

编译并执行上述代码后，你会发现产生以下结果。

Variable num: 3

## 第 8 章

### 方法简述

在阅读本书的过程中，你已经多次遇到方法。如果你想知道它们是什么，那么这里就是让你了解它们的地方。方法是编程中你应该了解的基本内容之一。

### 什么是方法？

方法可以说是一组可以共同执行任务的语句。C# 中的所有程序至少会有一个包含名为 Main 的方法的类。你已经遇到过它们了。

为了使用一个方法，必须先定义该方法。然后，再调用该方法。让我们来看看这个过程中的每一步。

### 定义方法

当定义一个方法时，会声明该方法结构的各个元素。C# 语言中定义方法的语法如下所示。

```
<Access Specifier> <Return Type> <Method Name>(Parameter List)
{
    Method Body
}
```

一个方法可以包含各种元素。它们如下所述。

- **访问说明符（Access Specifier）：** 如你所知，访问说明符将决定方法或变量从另一个类中的可见性。

- **返回类型（Return Type）：** 方法可以返回值。返回类型声明了方法将返回的值的**数据类型**。如果方法不返回任何值，那么返回类型将为 void。

- **方法名（Method name）：** 这是方法名的唯一标识符。名称区分大小写。此外，该标识符不能与类中已声明的任何其他标识符相同。

- **参数列表（Parameter list）：** 参数用于向方法传递和接收数据。它们被括在圆括号中。参数列表指的是方法的参数顺序、数量和类型。重要的是，方法可以没有任何参数。

- **方法体（Method Body）：** 方法体包含完成活动所必需的指令集。

请看下面给出的示例。在这段代码片段中，你会注意到一个函数 FindMax。它接受两个整数值并进行比较。较大的值将被返回。该函数具有公共访问说明符。因此，可以通过其实例从类的外部访问它。

```
class NumberManipulator
{
    public int FindMax(int num1, int num2)
    {
        /* local variable declaration */
        int result;
        if (num1 > num2)
            result = num1;
        else
            result = num2;
        return result;
    }
    ...
}
```

### 调用方法

在 C# 中，调用方法非常简单，只需使用其名称即可。请看下面给出的示例。它展示了如何调用方法。

```
using System;
namespace CalculatorApplication
{
    class NumberManipulator
    {
        public int FindMax(int num1, int num2)
        {
            /* local variable declaration */
            int result;
            if (num1 > num2)
                result = num1;
            else
                result = num2;

            return result;
        }

        static void Main(string[] args)
        {
            /* local variable definition */
            int a = 100;
            int b = 200;
            int ret;
            NumberManipulator n = new NumberManipulator();

            //calling the FindMax method
            ret = n.FindMax(a, b);

            Console.WriteLine("Max value is : {0}", ret );
            Console.ReadLine();
        }
    }
}
```

执行上述代码后，会产生以下结果。

Max value is : 200

可以通过使用方法类的实例，从其他类中调用公共方法。下面给出的示例展示了如何操作。在这种情况下，方法 FindMax 是类 NumberManipulator 的一部分。它可以从另一个名为 Test 的类中调用。

```
using System;

namespace CalculatorApplication
{
    class NumberManipulator
    {
        public int FindMax(int num1, int num2)
        {
            /*local variable declaration */
            int result;
            if(num1 > num2)
                result = num1;
            else
                result = num2;
            return result;
        }
    }

    class Test
    {
        static void Main(string[] args)
        {
            /* local variable definition */
            int a = 100;
            int b = 200;
            int ret;
            NumberManipulator n = new NumberManipulator();
            //calling the FindMax method
            ret = n.FindMax(a, b);
            Console.WriteLine("Max value is : {0}", ret );
            Console.ReadLine();
        }
    }
}
```

上述示例产生以下结果。

Max value is : 200

### 理解递归方法调用

方法可以调用自身。这样的过程称为递归。以下示例说明了递归方法调用的使用。这里，借助递归方法调用计算给定数字的阶乘。

```
using System;

namespace CalculatorApplication
{
    class NumberManipulator
    {
        public int factorial(int num)
        {
            /* local variable declaration */
            int result;

            if (num == 1)
            {
                return 1;
            }
            else
            {
                result = factorial(num - 1) * num;
                return result;
            }
        }

        static void Main(string[] args)
        {
            NumberManipulator n = new NumberManipulator();
            //calling the factorial method
            Console.WriteLine("Factorial of 6 is : {0}", n.factorial(6));
            Console.WriteLine("Factorial of 7 is : {0}", n.factorial(7));
            Console.WriteLine("Factorial of 8 is : {0}", n.factorial(8));
            Console.ReadLine();
        }
    }
}
```

编译并执行上述代码后，会产生以下结果。

Factorial of 6 is: 720
Factorial of 7 is: 5040
Factorial of 8 is: 40320

### 如何向方法传递参数？

如果调用一个带有参数的方法，必须将参数传递给该方法。有三种方式可以向方法传递参数。我们将依次介绍每一种。

### 值参数

按值传递参数是需要向方法传递参数时的默认机制。在这种情况下，调用方法时会为每个值参数创建新的存储位置。然后，原始参数的值将被复制到这些新位置中。在方法内部对参数所做的任何更改都不会影响实参。

请看下面给出的示例。

```
using System;

namespace CalculatorApplication
{
	class NumberManipulator
	{
		public void swap(int x, int y)
		{
			int temp;

			temp = x; /* save the value of x */
			x = y;  /* put y into x */
			y = temp; /* put temp into y */
		}

		static void Main(string[] args)
		{
			NumberManipulator n = new NumberManipulator();

			/* local variable definition */
			int a = 100;
			int b = 200;

			Console.WriteLine("Before swap, value of a : {0}", a);
			Console.WriteLine("Before swap, value of b : {0}", b);

			/* calling a function to swap the values */
			n.swap(a, b);

			Console.WriteLine("After swap, value of a : {0}", a);
			Console.WriteLine("After swap, value of b : {0}", b);

			Console.ReadLine();
		}
	}
}
```

执行上述代码后，产生以下结果。

Before swap, value of a :100
Before swap, value of b :200
After swap, value of a :100
After swap, value of b :200
```



交换后，b 的值：200

### 引用参数

这是对变量内存位置的引用。使用这种机制时，不会像值参数那样为参数创建新的存储位置。引用参数将表示已提供给方法的实际参数的精确内存位置。可以借助 **ref** 关键字来声明引用参数。

请看下面的示例。

```csharp
using System;

namespace CalculatorApplication
{
    class NumberManipulator
    {
        public void swap(ref int x, ref int y)
        {
            int temp;
            
            temp = x; /* save the value of x */
            
            x = y;  /* put y into x */
            y = temp; /* put temp into y */
        }

        static void Main(string[] args)
        {
            NumberManipulator n = new NumberManipulator();
            /* local variable definition */
            int a = 100;
            int b = 200;
            Console.WriteLine("Before swap, value of a : {0}", a);
            Console.WriteLine("Before swap, value of b : {0}", b);
            /* calling a function to swap the values */
            n.swap(ref a, ref b);
            Console.WriteLine("After swap, value of a : {0}", a);
            Console.WriteLine("After swap, value of b : {0}", b);
            Console.ReadLine();
        }
    }
}
```

执行上面所示的代码后，将产生以下结果。

Before swap, value of a : 100
Before swap, value of b : 200
After swap, value of a : 200
After swap, value of b : 100

如你所见，swap 函数中的值已经改变。这种变化在 Main 函数中得到了体现。

### 输出参数

return 语句只能从一个函数返回单个值。尽管如此，借助输出参数，可以从函数返回两个值。实际上，输出参数与引用参数相当相似。然而，有一个主要区别。输出参数能够将数据从给定方法中传出，而不是传入。

下面的示例展示了输出参数的使用。

```csharp
using System;

namespace CalculatorApplication
{
    class NumberManipulator
    {
        public void getValue(out int x)
        {
            int temp = 5;
            x = temp;
        }
        static void Main(string[] args)
        {
            NumberManipulator n = new NumberManipulator();
            /* local variable definition */
            int a = 100;

            Console.WriteLine("Before method call, value of a : {0}", a);
            /* calling a function to get the value */
            n.getValue(out a);
            Console.WriteLine("After method call, value of a : {0}", a);
            Console.ReadLine();
        }
    }
}
```

执行上面示例中所示的代码后，将产生以下结果。

Before method call, value of a : 100
After method call, value of a : 5

对于输出参数，所提供的变量不需要为其赋值。因此，当你必须通过参数从方法返回值，而不需要为参数分配初始值时，输出参数非常有用。

下面的示例演示了这一点。

```csharp
using System;

namespace CalculatorApplication
{
   class NumberManipulator
   {
        public void getValues(out int x, out int y )
        {
            Console.WriteLine("Enter the first value: ");
            x = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Enter the second value: ");
            y = Convert.ToInt32(Console.ReadLine());
        }

        static void Main(string[] args)
        {
            NumberManipulator n = new NumberManipulator();
            /* local variable definition */
            int a , b;
            /* calling a function to get the values */
            n.getValues(out a, out b);
            Console.WriteLine("After method call, value of a : {0}", a);
            Console.WriteLine("After method call, value of b : {0}", b);
            Console.ReadLine();
        }
   }
}
```

执行上面的示例后，你将获得以下结果。

```
Enter the first value:
7
Enter the second value:
8
After method call, value of a : 7
After method call, value of b : 8
```

## 第9章：数组与字符串的使用

在使用 C# 时，你肯定会遇到数组和字符串。事实上，在学习 foreach 循环时，你已经使用过数组了。至于字符串，它们在本书的各个示例中都有出现。现在是时候更好地了解这两个概念了。

### 认识数组

数组将存储不同元素的顺序集合。该集合具有固定的大小，并且所有元素都是同一类型。它们用于存储数据集合。然而，更好的定义方式是：它们是在连续内存位置中保持的变量集合。

数组省去了我们声明多个单独变量的麻烦。相反，我们只需要声明一个数组变量，然后将所需的值放入其中。因此，我们不必创建诸如 a0、a1、a2 等变量列表。

相反，我们创建一个数组 a，并使用 a[0]、a[1] 和 a[2] 等。

请记住，数组中存在的特定元素可以通过索引来访问。在 C# 中，所有数组都具有连续的内存位置。最低地址对应于数组的第一个元素，而最高地址属于最后一个元素。

### 声明数组

在 C# 中，如果要声明数组，必须使用以下语法。

```csharp
datatype[] arrayName;
```

语法中的每个元素讨论如下。

- datatype 用于指定数组中元素的数据类型。
- [] 指定数组的秩。数组的秩定义了数组的大小。
- arrayName 是该数组的名称。

### 初始化数组

请记住，声明数组并不会在内存中初始化它。只有在数组变量被初始化之后，你才能为其赋值。由于数组是引用类型，因此必须使用 **new** 关键字来创建给定数组的实例。

下面的示例向你展示了如何操作。

```csharp
double[] balance = new double[10];
```

### 为数组赋值

可以为数组的各个元素赋值。为此，需要使用元素的索引号。下面的示例说明了这一点。

```csharp
double[] balance = new double[10];
balance[0] = 4500.0;
```

也可以在声明数组时为其赋值。

```csharp
double[] balance = { 2340.0, 4523.69, 3421.0};
```

指向完全相同的内存位置。下面的示例演示了这一点。

```csharp
int [] marks = new int[] { 99, 98, 92, 97, 95};
int[] score = marks;
```

创建数组时，C# 编译器将隐式地将其所有元素初始化为特定的默认值。默认值取决于数组的类型。例如，int 数组中的所有元素都将被初始化为 0。

### 访问数组中的元素

可以通过索引数组名称来访问元素。为此，可以将所需元素的索引放在数组名称后面的方括号内。下面的示例展示了这一点。

```csharp
double salary = balance[9];
```

下面所示的示例将说明到目前为止你已经学到的关于数组的概念。即赋值、声明和访问元素。

```csharp
using System;
namespace ArrayApplication
{
    class MyArray
    {
        static void Main(string[] args)
        {
            int [] n = new int[10]; /* n is an array of 10 integers */
            int i,j;

            /* initialize elements of array n */
            for ( i = 0; i < 10; i++ )
            {
                n[ i ] = i + 100;
            }

            /* output each array element's value */
            for (j = 0; j < 10; j++ )
            {
                Console.WriteLine("Element[{0}] = {1}", j, n[j]);
            }

            Console.ReadKey();
        }
    }
}
```



```
}
```

执行上述代码后，将产生以下结果。

Element[0] = 100
Element[1] = 101
Element[2] = 102
Element[3] = 103
Element[4] = 104
Element[5] = 105
Element[6] = 106
Element[7] = 107
Element[8] = 108
Element[9] = 109

### C# 中关于数组的概念

在 C# 中使用数组时，有几个重要的概念您需要了解。它们在高级课程中会非常有用。

### 多维数组
C# 提供了对多维数组的支持。这些数组最常见且最简单的形式是二维数组。

### 锯齿数组 (Jagged Arrays)
简单来说，这类数组就是“数组的数组”。

### Array 类
该类定义在 `System` 命名空间中。它是所有数组的基类。因此，它提供了许多方法和属性，以帮助您处理数组。

### 将数组传递给函数
可以将数组传递给函数。这可以通过指定数组名称但不带索引来实现。

### 参数数组 (Param Arrays)
它们用于向给定的函数传递未知数量的参数。

至此，关于数组的部分就结束了。现在，我们将来看看字符串。

### 字符串介绍

在 C# 中，字符串可以用作字符数组。尽管如此，常见的做法是使用 `string` 关键字来声明存储变量。您必须记住，`string` 关键字仅仅是 `System.String` 类的别名。

### 字符串对象的创建

可以通过以下任何一种方式创建字符串对象：

- 通过将字符串字面量赋值给 `String` 变量
- 使用 `String` 类构造函数
- 通过获取属性或调用能返回字符串的方法
- 通过使用字符串拼接运算符 `+`
- 通过调用可以将对象或值转换为相应字符串表示形式的格式化方法

以下示例演示了字符串对象的创建。

```csharp
using System;

namespace StringApplication
{
    class Program
    {
        static void Main(string[] args)
        {
            //from string literal and string concatenation
            string fname, lname;

            fname = "John";

            lname = "Smith";

            string fullname = fname + lname;

            Console.WriteLine("Full Name: {0}", fullname);

            //by using string constructor
            char[] letters = { 'H', 'e', 'l', 'l','o' };

            string greetings = new string(letters);

            Console.WriteLine("Greetings: {0}", greetings);

            //methods returning string
            string[] sarray = { "Hello", "From", "The", "Earth" };

            string message = String.Join(" ", sarray);

            Console.WriteLine("Message: {0}", message);

            //formatting method to convert a value
            DateTime waiting = new DateTime(2016, 10, 10, 17, 58, 1);

            string chat = String.Format("Message sent at {0:t} on {0:D}", waiting);

            Console.WriteLine("Message: {0}", chat);
        }
    }
}
```

编译并执行上述代码后，产生以下结果。

Full Name: Rowan Atkinson
Greetings: Hello
Message: Hello From The Earth
Message: Message sent at 5:58 PM on Wednesday, October 10, 2016

### String 类属性

`String` 类拥有两个属性，具体描述如下：

- Chars：获取给定 `String` 对象中指定位置的 `Char` 对象。
- Length：获取给定 `String` 对象中字符的总数。

### String 类中存在的方法

`String` 类中提供了多种方法。当您处理字符串对象时，这些方法会非常有帮助。以下是一些常用方法：

`public static int Compare(string strA, string strB)`
比较两个给定的字符串对象。将返回一个整数，指示对象在排序顺序中的相对位置。

`public static int Compare(string strA, string strB, bool ignoreCase)`
比较两个给定的字符串对象，并返回一个指示对象在排序顺序中相对位置的整数。与此同时，当布尔参数为 `true` 时，它将忽略大小写。

`public static string Concat(string str0, string str1)`
拼接两个字符串对象。也可以增加被拼接的字符串对象数量。

`public bool Contains(string value)`
返回一个值，指示给定的字符串是否出现在指定的 `String` 对象中。

`public static string Copy(string str)`
创建一个与给定字符串具有相同值的新 `String` 对象。

`public bool EndsWith(string value)`
判断给定字符串对象的末尾是否与给定的字符串匹配。

`public static bool Equals(string a, string b)`
判断两个给定的 `String` 对象是否具有完全相同的值。

`public int IndexOf(char value)`
返回给定 Unicode 字符在字符串中的索引。将提供该字符首次出现的位置（从零开始的索引）。

`public static string Format(string format, Object argo)`
替换给定字符串中的一个或多个格式项。它们将被替换为给定对象的字符串表示形式。

`public string Insert(int startIndex, string value)`
返回一个新字符串，该字符串在给定 `String` 对象的特定索引位置插入了指定的字符串。

`public static bool IsNullOrEmpty(string value)`
指示给定的字符串是否为 null 字符串或空字符串。

`public static string Join(string separator, params string[] value)`
使用给定的分隔符将字符串数组中的所有元素拼接在一起。

`public static string Join(string separator, string[] value, int startIndex, int count)`
使用给定的分隔符将指定的字符串元素拼接在一起。

`public int LastIndexOf(char value)`
返回当前字符串对象中给定 Unicode 字符的索引位置。使用从零开始的索引，且仅提及最后一次出现的位置。

`public string Remove(int startIndex)`
删除当前实例中从指定位置开始的所有字符，一直持续到最后一个位置。最后返回该字符串。

`String` 类还有广泛的其他方法和构造函数。MSDN 库包含完整列表。现在，让我们看几个示例，演示如何使用上述部分方法。

下面的示例演示了如何比较字符串。

```csharp
using System;

namespace StringApplication
{
    class StringProg
    {
        static void Main(string[] args)
        {
            string str1 = "This is test";
            string str2 = "This is text";
            
            if (String.Compare(str1, str2) == 0)
            {
                Console.WriteLine(str1 + " and " + str2 + " are equal.");
            }
            else
            {
                Console.WriteLine(str1 + " and " + str2 + " are not equal.");
            }

            Console.ReadKey();
        }
    }
}
```

执行上述代码后，将产生以下结果。

> This is a test, and This is text are not equal.

下面的示例演示了一个字符串包含另一个字符串的情况。

```csharp
using System;

namespace StringApplication
{
    class StringProg
    {
        static void Main(string[] args)
        {
            string str = "This is test";

            if(str.Contains("test"))
            {
               Console.WriteLine("The sequence 'test' was found.");
            }

            Console.ReadKey();
        }
    }
}
```

执行上述代码后产生以下结果。

The sequence 'test' was found.

如下示例演示了如何获取子字符串。

```csharp
using System;

namespace StringApplication
{
   class StringProg
   {
```



```markdown
# 第 10 章

### 结构体（Structures）与枚举（Enums）解析

既然你已经学习了数组和字符串，现在是时候来看看结构体和枚举了。它们在各种程序中都起着至关重要的作用。因此，让我们进一步深入了解它们。

### 什么是结构体？

C# 中的结构体是一种值类型（value type）数据类型。通过它，单个变量可以持有不同数据类型的相关数据。要创建结构体，必须使用 `struct` 关键字。结构体通常用于表示一条记录。

让我们以图书馆书籍为例来更好地理解结构体。在图书馆中，你需要记录书籍信息。在追踪每本书时，你可能需要考虑各种属性，例如书名、作者和主题等。我们将在接下来的章节程序中使用这个示例。

### 定义结构体

如前所述，必须使用 `struct` 语句来定义结构体。该语句可以定义一个具有多个成员的新数据类型。

让我们采用关于书籍的例子，据此定义一个 `Book` 结构体。其形式如下：

```csharp
struct Books
{
    public string title;
    public string author;
    public string subject;
    public int book_id;
};
```

下面的示例向你展示了结构体是如何被使用的。

```csharp
using System;
struct Books
{
    public string title;
    public string author;
    public string subject;
    public int book_id;
};

public class testStructure
{
    public static void Main(string[] args)
    {
        Books Book1;  /* 声明 Book 类型的 Book1 */
        Books Book2;  /* 声明 Book 类型的 Book2 */

        /* 书籍 1 详情 */
        Book1.title = "C# Programming";
        Book1.author = "John Smith";
        Book1.subject = "C# Programming Tutorial";
        Book1.book_id = 123456;

        /* 书籍 2 详情 */
        Book2.title = "Java Programming";
        Book2.author = "Jane Smith";
        Book2.subject = "Java Programming Tutorial";
        Book2.book_id = 456789;

        /* 打印 Book1 信息 */
        Console.WriteLine( "Book 1 title : {0}", Book1.title);
        Console.WriteLine("Book 1 author : {0}", Book1.author);
        Console.WriteLine("Book 1 subject : {0}", Book1.subject);
        Console.WriteLine("Book 1 book_id :{0}", Book1.book_id);

        /* 打印 Book2 信息 */
        Console.WriteLine("Book 2 title : {0}", Book2.title);
        Console.WriteLine("Book 2 author : {0}", Book2.author);
        Console.WriteLine("Book 2 subject : {0}", Book2.subject);
        Console.WriteLine("Book 2 book_id : {0}", Book2.book_id);
        Console.ReadKey();
    }
}
```

编译并执行上述代码后，将产生以下结果。

Book 1 title : C# Programming
Book 1 author : John Smith
Book 1 subject : C# Programming Tutorial
Book 1 book_id : 123456

Book 2 title : Java Programming
Book 2 author : Jane Smith
Book 2 subject : Java Programming Tutorial
Book 2 book_id : 456789

### C# 结构体的特点

在上面的示例中，你使用了简单的结构体。如果你已经接触过 C 或 C++ 的结构体，你应该知道 C# 中的结构体与这两种语言中的结构体相当不同。C# 结构体的特点如下：

- 结构体可以拥有字段、方法、属性、索引器、事件和运算符方法。
- 它们可以定义构造函数。但是，它们不能有析构函数。同时，无法为结构体定义默认构造函数。默认构造函数将由系统自动定义，因此无法对其进行修改。
- 与类不同，结构体不能继承自其他结构体或类。
- 同理，结构体也不能作为其他类或结构体的基类。
- 你不能将结构体成员指定为 `virtual`（虚）、`abstract`（抽象）或 `protected`（受保护）。
- 结构体可以实现一个或多个接口。
- 使用 `New` 运算符创建结构体对象时，对象将被创建并调用相应的构造函数。与类不同，结构体对象可以在不使用 `New` 运算符的情况下实例化。
- 如果你不使用 `New` 运算符，字段将保持未赋值状态。因此，在初始化所有字段之前，该对象将无法使用。

### 类与结构体的区别

这两者之间有几个区别点，列举如下：

- 结构体是值类型，而类是引用类型。
- 与类不同，结构体不支持继承。
- 结构体不能拥有自定义的默认构造函数。

现在我们对结构体有了更多了解，让我们重新创建之前关于 `Books` 结构体的示例，以获得更深入的理解。

```csharp
using System;

struct Books
{
   private string title;
   private string author;
   private string subject;
   private int book_id;

   public void getValues(string t, string a, string s, int id)
   {
      title = t;
      author = a;
      subject = s;
      book_id = id;
   }

   public void display()
   {
      Console.WriteLine("Title : {0}", title);
      Console.WriteLine("Author : {0}", author);
      Console.WriteLine("Subject : {0}", subject);
      Console.WriteLine("Book_id : {0}", book_id);
   }
};

public class testStructure
{
    public static void Main(string[] args)
    {
        Books Book1 = new Books(); /* 声明 Book 类型的 Book1 */
        Books Book2 = new Books(); /* 声明 Book 类型的 Book2 */
        
        /* 书籍 1 详情 */
        Book1.getValues("C# Programming", "John Smith", "C# Programming Tutorial", 123456);

        /* 书籍 2 详情 */
        Book2.getValues("Java Programming", "Jane Smith", "Java Programming Tutorial", 456789);

        /* 打印 Book1 信息 */
        Book1.display();

        /* 打印 Book2 信息 */
        Book2.display();

        Console.ReadKey();
    }
}
```

执行上述代码后，结果将与下面所示一致。

Title : C# Programming
Author : John Smith
Subject : C# Programming Tutorial
Book_id : 123456

Title : Java Programming
Author : Jane Smith
Subject : Java Programming Tutorial
Book_id : 456789

至此，关于结构体的部分就结束了。现在，让我们来看看枚举。

### 什么是枚举（Enums）？

Enums 是 enumerations 的缩写。枚举可以说是一组命名的整数常量。`enum` 关键字用于声明枚举类型。在 C# 中，枚举是值数据类型。因此，一个枚举将包含其自身的值。它无法继承，也无法被继承。

### 声明枚举变量

通常，声明枚举需要遵循的语法如下所示。

```csharp
enum <enum_name>
{
    enumeration list
};
```

来看看其中每个元素的含义：

- **enum_name**：指定枚举类型的名称。
```



-   **枚举列表**：这是一个标识符列表，其中每个标识符由逗号分隔。

在枚举列表中，每个符号代表一个整数值。每个符号的值都将大于前一个符号。枚举列表中第一个符号的默认值为0。

以下示例说明了枚举变量的使用。

```csharp
using System;
namespace EnumApplication
{
    class EnumProgram
    {
        enum Days { Sun, Mon, tue, Wed, thu, Fri, Sat };
        static void Main(string[] args)
        {
            int WeekdayStart = (int)Days.Mon;
            int WeekdayEnd = (int)Days.Fri;
            Console.WriteLine("Monday: {0}", WeekdayStart);
            Console.WriteLine("Friday: {0}", WeekdayEnd);
            Console.ReadKey();
        }
    }
}
```

执行上述代码后，可以得到以下结果。

Monday: 1
Friday: 5

## 第11章
### 熟悉继承的概念

如前一章所述，任何面向对象编程语言最重要的方面之一就是类。同样地，继承是面向对象编程中的一个关键概念。

由于C#就是这样一种语言，你将不得不尽早开始使用继承。事实上，整个.NET框架都是建立在继承的概念之上的。它负责体现“一切皆对象”的理念。

简而言之，继承使你能够创建可以从其父类继承特定属性的类。在C#中，甚至一个简单的数字也可以是继承自父类 `System.Object` 的类的实例。

对于一些初学者来说，继承可能有点难理解。但是，最好尽早熟悉它，因为它在C#编程中扮演着重要角色。以下是一个说明继承使用的示例。

```csharp
public class Animal
{
    public void Greet()
    {
        Console.WriteLine ("Hello! I'm some kind of animal.");
    }
}

public class Cat: Animal
{
}
```

如你所见，首先定义了一个 `Animal` 类以及一个向用户发出问候的简单方法。接着定义了一个 `Cat` 类。我们现在使用冒号来告知C#，`Cat` 类将继承自 `Animal` 类。现在，就可以开始使用这些类了。

```csharp
Animal animal = new Animal ();
animal.Greet ();

Dog dog = new Dog ();
dog.Greet ();
```

运行上述示例，你会发现 `Greet()` 方法被执行了，即使它没有在 `Cat` 类中定义。这是因为该方法已由 `Cat` 类从 `Animal` 类继承而来。

当然，上述示例中的问候语相当模糊。可以自定义问候语以包含动物的名字。这将在下一个示例中展示。

```csharp
public class Animal
{
    public virtual void Greet()
    {
        Console.WriteLine ("Hello! I'm some kind of animal.");
    }
}

public class Cat: Animal
{
    public override void Greet()
    {
        Console.WriteLine("Hello! I'm a cat.");
    }
}
```

你可以注意到，上述示例中的代码有一些更改。在 `Cat` 类上添加了一个方法，并且在 `Animal` 类的方法上添加了 `virtual` 关键字。此外，`Cat` 类上还出现了 `override` 关键字。

在C#中，除非一个类项被标记为 `virtual`，否则无法重写它。当然，即使被重写后，也可以借助 `base` 关键字继续访问继承的方法。下面的示例展示了这一点。

```csharp
public override void Greet()
{
    base.Greet();
    Console.WriteLine("Yes! I am - a cat!");
}
```

然而，方法并不是唯一可以继承的东西。事实上，类的几乎所有成员都会被继承。这包括属性和字段。要确保获得正确的结果，你需要做的是使用正确的可见性，如前面章节所述。

另一件你需要记住的事情是，继承不必从一个类到另一个类。可以有一个完整的类继承层级结构。与前面的示例保持一致，可以创建一个继承自 `Cat` 类的 `Kitten` 类，而 `Cat` 类又将继承自 `Animal` 类。

但是，在C#中有一件事你无法做到，那就是多重继承。换句话说，你不能让一个类同时继承多个类。C#不支持此功能。

### 理解基类和派生类的概念

一个类可以从多个类派生。因此，可以从多个基类继承函数和数据。

下面是在C#中创建派生类所使用的语法。

```csharp
<acess-specifier> class <base_class>
{
    ...
}

class <derived_class> : <base_class>
{
    ...
}
```

让我们借助一个示例来更好地理解基类和派生类。在下面的示例中，`Shape` 是基类，而 `Rectangle` 是其派生类。

```csharp
using System;
namespace InheritanceApplication
{
    class Shape
    {
        public void setWidth(int w)
        {
            width = w;
        }
        public void setHeight(int h)
        {
            height = h;
        }
        protected int width;
        protected int height;
    }
    class Rectangle: Shape
    {
        public int getArea()
        {
            return (width * height);
        }
    }
    class RectangleTester
    {
        static void Main(string[] args)
        {
            Rectangle Rect = new Rectangle();
            Rect.setWidth(5);
            Rect.setHeight(7);
            // Print the area of the object.
            Console.WriteLine("Total area: {0}",  Rect.getArea());
            Console.ReadKey();
        }
    }
}
```

执行上述代码后，可以得到以下结果。

Total area: 35

### 基类的初始化

如你所知，派生类将继承基类的成员方法和成员变量。因此，有必要在创建子类之前先创建超类对象。可以在成员初始化列表中提供超类初始化的指令。

以下示例说明了这一点。

```csharp
using System;

namespace RectangleApplication
{
    class Rectangle
    {
        //member variables
        protected double length;
        protected double width;

        public Rectangle(double l, double w)
        {
            length = l;
            width = w;
        }

        public double GetArea()
        {
            return length * width;
        }

        public void Display()
        {
            Console.WriteLine("Length: {0}", length);
            Console.WriteLine("Width: {0}", width);
            Console.WriteLine("Area: {0}", GetArea());
        }
    } //end class Rectangle

    class Tabletop : Rectangle
    {
        private double cost;

        public Tabletop(double l, double w) : base(l, w)
        {}

        public double GetCost()
        {
            double cost;
            cost = GetArea() * 70;
            return cost;
        }

        public void Display()
        {
            base.Display();
            Console.WriteLine("Cost: {0}", GetCost());
        }
    }

    class ExecuteRectangle
    {
        static void Main(string[] args)
        {
            Tabletop t = new Tabletop(4.5, 7.5);
            t.Display();
            Console.ReadLine();
        }
    }
}
```

执行上述代码后，将得到以下结果。



### C# 与多重继承

C# 不支持多重继承。但是，可以使用接口来实现多重继承。下面的示例将对此进行演示。

```csharp
using System;
namespace InheritanceApplication
{
    class Shape
    {
        public void setWidth(int w)
        {
            width = w;
        }

        public void setHeight(int h)
        {
            height = h;
        }

        protected int width;
        protected int height;
    }

    // Base class PaintCost
    public interface PaintCost
    {
        int getCost(int area);
    }

    // Derived class
    class Rectangle : Shape, PaintCost
    {
        public int getArea()
        {
            return (width * height);
        }

        public int getCost(int area)
        {
            return area * 70;
        }
    }

    class RectangleTester
    {
        static void Main(string[] args)
        {
            Rectangle Rect = new Rectangle();
            int area;
            Rect.setWidth(5);
            Rect.setHeight(7);
            area = Rect.getArea();

            // Print the area of the object.
            Console.WriteLine("Total area: {0}", Rect.getArea());
            Console.WriteLine("Total paint cost: {0}", Rect.getCost(area));

            Console.ReadKey();
        }
    }
}
```

执行上述代码后，产生如下结果。

Total area: 35

Total paint cost: $2450

# 第 12 章
使用构造函数和析构函数

在本书中，你已经遇到过这两个术语。实际上，它们并不难理解。下面我们将逐一进行介绍。

### C# 中的构造函数

类构造函数可以说是类的一个特殊成员函数。每当该类创建新对象时，构造函数就会被执行。构造函数的名称与类名完全相同。构造函数没有返回类型。

下面的示例演示了构造函数。

```csharp
using System;
namespace LineApplication
{
    class Line
    {
        private double length; // Length of a line

        public Line()
        {
            Console.WriteLine("Object is being created");
        }

        public void setLength( double len )
        {
            length = len;
        }

        public double getLength()
        {
            return length;
        }

        static void Main(string[] args)
        {
            Line line = new Line();

            // set line length
            line.setLength(6.0);

            Console.WriteLine("Length of line : {0}", line.getLength());

            Console.ReadKey();
        }
    }
}
```

执行上述代码后，产生如下结果。

> Object is being created

Length of line : 6

### 带参数的构造函数

默认情况下，构造函数没有任何参数。即便如此，你也可以为构造函数添加参数。这类构造函数被称为带参数的构造函数。借助这种技术，你可以在创建特定对象时为其赋一个初始值。下面的示例将向你展示如何实现。

```csharp
using System;

namespace LineApplication
{
    class Line
    {
        private double length; // Length of a line
        public Line(double len) // Parameterized constructor
        {
            Console.WriteLine("Object is being created, length = {0}", len);
            length = len;
        }
        public void setLength( double len )
        {
            length = len;
        }
        public double getLength()
        {
            return length;
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            Line line = new Line(10.0);

            Console.WriteLine("Length of line : {0}", line.getLength());

            // set line length
            line.setLength(6.0);

            Console.WriteLine("Length of line : {0}", line.getLength());

            Console.ReadKey();
        }
    }
}
```

执行上述代码后，产生如下结果。

Object is being created; length = 10

Length of line : 10

Length of line : 6

### C# 中的析构函数

与构造函数类似，析构函数也是类的一个特殊成员函数。然而，它仅在类的某个对象超出其指定作用域时才会执行。析构函数的名称与类名完全相同，但前面会加上一个波浪号（~）前缀。析构函数不能返回值，也不能接受任何参数。析构函数非常有用，因为它们可以在程序退出前释放内存资源。析构函数不能被继承。

下面的示例演示了析构函数的使用。

```csharp
using System;

namespace LineApplication
{
    class Line
    {
        private double length;   // Length of a line
        public Line() // constructor
        {
            Console.WriteLine("Object is being created");
        }

        ~Line() //destructor
        {
            Console.WriteLine("Object is being deleted");
        }

        public void setLength( double len )
        {
            length = len;
        }

        public double getLength()
        {
            return length;
        }

        static void Main(string[] args)
        {
            Line line = new Line();
            // set line length
            line.setLength(6.0);

            Console.WriteLine("Length of line : {0}", line.getLength());
        }
    }
}
```

执行上述示例中的代码后，产生如下结果。

Object is being created

Length of line : 6

Object is being deleted

现在你已经了解了构造函数和析构函数的概念。当你开始编写复杂程序时，一定会发现它们非常有用。因此，务必确保你对它们有透彻的理解。

# 第 13 章
深入接口与多态

这两个概念是你需要尽早熟悉的。它们在后续的 C# 程序开发中将大有裨益。

### 接口简介

接口可以定义为所有继承该接口的类都必须遵循的语法契约。接口定义了契约中的"做什么"部分，而派生类则定义契约中"怎么做"的部分。

接口将定义属于其成员的方法、属性和事件。需要注意的是，接口只包含成员的声明。定义成员的职责交由派生类来完成。因此，接口确保了一种标准结构的存在，派生类都可以遵循该结构。

### 声明接口

接口可以使用 `interface` 关键字来声明。实际上，它与类的声明有相似之处。默认情况下，接口声明为 `public`。下面的示例演示了如何声明接口。

```csharp
public interface ITransactions
{
    // interface members
    void showTransaction();
    double getAmount();
}
```

现在让我们通过一个示例来了解如何实现上述接口。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace InterfaceApplication
{
    public interface ITransactions
    {
        // interface members
        void showTransaction();
        double getAmount();
    }

    public class Transaction : ITransactions
    {
        private string tCode;
        private string date;
        private double amount;

        public Transaction()
        {
            tCode = " ";
            date = " ";
            amount = 0.0;
        }

        public Transaction(string c, string d, double a)
        {
            tCode = c;
            date = d;
            amount = a;
        }

        public double getAmount()
        {
            return amount;
        }

        public void showTransaction()
        {
            Console.WriteLine("Transaction: {0}", tCode);
            Console.WriteLine("Date: {0}", date);
            Console.WriteLine("Amount: {0}", getAmount());
        }
    }

    class Tester
    {
        static void Main(string[] args)
        {
            Transaction t1 = new Transaction("001", "8/10/2012", 78900.00);
            Transaction t2 = new Transaction("002", "9/10/2012", 451900.00);
            t1.showTransaction();
            t2.showTransaction();
            Console.ReadKey();
        }
    }
}
```

执行上述代码后，产生如下结果。

Transaction: 001
Date: 8/10/2012
Amount: 78900
Transaction: 002
Date: 9/10/2012
Amount: 451900



数量：451900

### 从多态性开始

从字面上看，多态性可以被定义为具有多种形式。然而，在面向对象编程方法中，多态性通常被描述为具有一个接口但多个功能。现在，多态性可以是静态的或动态的。

### 静态多态性

静态绑定是指在程序编译时将函数与对象链接起来的机制。换句话说，决策是在编译时做出的。在 C# 中，有两种技术可以实现静态多态性。

- 函数重载
- 运算符重载

以下示例演示了函数重载。

以下示例展示了使用 `print()` 函数来打印不同的数据类型：

```csharp
using System;

namespace PolymorphismApplication
{
    class Printdata
    {
        void print(int i)
        {
            Console.WriteLine("Printing int: {0}", i);
        }

        void print(double f)
        {
            Console.WriteLine("Printing float: {0}", f);
        }

        void print(string s)
        {
            Console.WriteLine("Printing string: {0}", s);
        }

        static void Main(string[] args)
        {
            Printdata p = new Printdata();
            // Call print to print integer
            p.print(5);

            // Call print to print float
            p.print(500.263);

            // Call print to print string
            p.print("Hello C++");

            Console.ReadKey();
        }
    }
}
```

执行上述代码后，将获得以下结果。

Printing int: 5

Printing float: 500.263

Printing string: Hello C++

### 动态多态性

在这种多态性中，决策将在运行时做出。这是通过方法重写来实现的。

通过方法重写，可以在派生类和基类中具有相同参数和相同名称的方法。因此，可以在运行时通过基类的对象指向派生类。

以下示例说明了动态多态性的使用。

```csharp
using System;

namespace PolymorphismApplication
{
    class Shape
    {
        protected int width, height;

        public Shape( int a=0, int b=0)
        {
            width = a;
            height = b;
        }

        public virtual int area()
        {
            Console.WriteLine("Parent class area :");
            return 0;
        }
    }

    class Rectangle: Shape
    {
        public Rectangle( int a=0, int b=0): base(a, b)
        {
        }

        public override int area ()
        {
            Console.WriteLine("Rectangle class area :");
            return (width * height);
        }
    }

    class Triangle: Shape
    {
        public Triangle(int a = 0, int b = 0): base(a, b)
        {
        }

        public override int area()
        {
            Console.WriteLine("Triangle class area :");
            return (width * height / 2);
        }
    }

    class Caller
    {
        public void CallArea(Shape sh)
        {
            int a;
            a = sh.area();
            Console.WriteLine("Area: {0}", a);
        }
    }

    class Tester
    {
        static void Main(string[] args)
        {
            Caller c = new Caller();

            Rectangle r = new Rectangle(10, 7);

            Triangle t = new Triangle(10, 5);

            c.CallArea(r);

            c.CallArea(t);

            Console.ReadKey();
        }
    }
}
```

编译并执行上述代码后产生的结果如下。

Rectangle class area:

Area: 70

Triangle class area:

Area: 25

这结束了关于接口和多态性的章节。暂时不要担心使用它们。先巩固你的 C# 基础。

## 第 15 章

### 学习调试的基础知识

即使你对计算机编程只有一点了解，你也应该听说过调试。这是所有类型软件和应用程序编程中至关重要的过程。你看，程序中可能存在错误。这些错误可以简单到只是一个打字错误或不正确的语句。它们都被称为**bug（漏洞/错误）**，它们会阻止你的程序正确执行。因此，这些 bug 需要被移除，而这正是通过调试来实现的。

当你编写像本书中所示示例那样的几行简单应用程序时，你很容易识别错误。你可以简单地执行程序并找出 bug。然而，随着时间的推移，你肯定会开始编写更复杂的代码，这些代码长达数百行，充满了复杂的语句。由于涉及的高度复杂性，确定 bug 变得非常困难。

在这些情况下，调试成为一项极其有用的工具。因此，你必须花时间了解这个工具，以成为一名更好的程序员。没有它，你几乎不可能纠正复杂代码中发现的错误。

### 了解打印调试

最常用的调试类型被称为**打印调试**。虽然这是最基本的调试类型，但由于其在某些情况下的有效性，高级程序员也经常使用它。

在打印调试中，应用程序被设置为打印数字或文本。这使你可以了解代码的哪些部分已被执行，以及变量中包含什么内容。在 C# 中，可以使用 `Console.Write()` 方法来打印状态消息或在控制台上显示特定变量的内容。

对于某些情况，这就足够了。另一方面，当你使用 Visual Studio 等良好的 IDE 甚至是 Express 版本时，你将有更好的工具可以使用。好处是，一旦你知道了基本原理，它们就很容易使用。

### 断点简介

**断点**是你需要了解的关于调试的第一件事。顾名思义，断点标记了代码中的一个特定点，在该点执行将暂停。应用程序不会因此变得无用。相反，断点只是简单地暂停应用程序的执行。

如果你使用 Visual Studio 甚至是 Express 版本，实现断点非常容易。在这些 IDE 中，你会注意到代码左侧有一个灰色区域。这被称为**装订线（gutter）**，在此区域上单击左键会出现一个红色圆圈。这就是**断点**，调试器将在此点停止应用程序的执行。

这些只是调试的基础。随着你作为 C# 程序员的进步，你会自动了解到各种其他类型的调试工具和方法，以及调试最复杂的方面。

# 第 16 章

### C# 初学者技巧

和所有编程语言一样，C# 有其自身的细微差别和特点。因此，初学者很容易感到不知所措。因此，这里有一些技巧可以帮助你克服作为初学者面临的一些问题，并迈出成为全职 C# 程序员的下一步。

### 坚持练习

没有人一夜之间成为任何领域的专家。计算机编程当然也是如此。培养技能和获取知识以称自己为专家 certainly 需要很长时间。因此，你应该保持耐心，继续练习 C#。同时，你应该在 C# 中练习各种任务。

### 不要钻牛角尖

这是程序员中相当常见的问题，即使是高级程序员也是如此。事实是，在像 C# 这样的面向对象编程语言中，很少有一种最佳做法。因此，你不应该执着于某个特定过程或技术。 certainly 可能有其他更好的方法。

### 巩固你的基础

你可能学会了编写代码，但你也必须了解每个概念或功能如何组合在一起使代码工作。换句话说，你需要彻底理解基本原理和基础知识。这将使你能够理解一段代码为什么以这种方式工作，以及哪些可能的 bug 导致了执行中的问题。因此，你将成为一名更好的开发人员。

### 深入学习一些高级概念

当然，你不应该期望在开始学习 C# 的几个月内掌握所有高级技术和概念。然而，如果你花时间详细学习几个概念，这将大大有助于你的进步。你应该非常擅长使用那几个概念。你可以自由选择要专注的概念。它们可以是你在工作中经常遇到的东西，也可以是你非常感兴趣的东西。试图成为少数技术的专家比试图掌握所有技术要容易。

### 查看资深程序员写的代码

学习 C# 概念和技术的最佳方法之一是查看更有经验的程序员编写的代码。



程序员。如果你在某处工作，可以轻松地向资深程序员请教，让他们展示他们的代码。别忘了去理解他们为何采用某种特定技术以及如何运用它。或者，你也可以在线浏览开源项目。他们未必都是顶尖程序员，但你仍能学到很多。当然，你必须避免盲目模仿他人。只需理解其思路，并尝试在自己的代码中加以运用。

### 结论

本书到此结束。你现在已掌握了被称为 C# 的面向对象编程语言的基础知识。你也已学习了如何用这种语言编写一些基础程序，以及开始编程所需的知识。

你现在可以在代码中开始使用一些基本语句和方法了。当然，你已学习了如何声明和定义变量。更重要的是，你知道了如何创建类，甚至在其中实现继承以构建代码块的层次结构。如果愿意，你还可以开始在代码中应用条件逻辑，使其更为高级，特别是借助循环和多个类。

你从本书中获取的信息足以帮助你入门 C# 编程。当然，还有很多需要了解和学习的内容。作为一门流行的编程语言，它会定期持续更新。因此，总有新的、令人兴奋的内容值得学习。在熟练掌握这门编程语言后，你可以轻松地开始学习其他出色的编程语言，如 C、Java 甚至 Ruby。你甚至可以迈入 Web 开发领域，因为 C# 是 .NET 框架的一部分。

衷心感谢你选择本书，希望它对你有所帮助。我也希望你已建立起坚实的基础，能够将 C# 作为你的职业或爱好。祝你在 C# 的学习和未来中一切顺利！

### 想学习更多编程知识？

查看 Joseph Connor 的其他书籍：

- **最新发布（2016年10月）**：《编程：初学者计算机编程：学习 HTML5、JavaScript 和 CSS 基础》或点击链接 https://www.amazon.com/dp/B01LYZGZKN
- **Python**：《权威指南：初学者学习 Python 编程》或点击链接 https://www.amazon.com/dp/B013NLBA9C
- **Raspberry Pi 2**：《权威初学者指南：开始 Raspberry 项目》或点击链接 https://www.amazon.com/dp/B013NKMD2Q
- **黑客技术**：《初学者黑客技术：计算机病毒、破解、恶意软件、IT 安全》或点击链接 https://www.amazon.com/dp/B010K7BVOQ
- **亚马逊畅销书**：《编程：初学者计算机编程：学习 Java、SQL 和 C++ 基础 - 第3版》或点击链接 https://www.amazon.com/Programming-Computer-Beginners-Basics-JavaScript-ebook/dp/B014361TOM

查看我们的 Facebook 和 Instagram，获取最新发布更新！

美国制造
加利福尼亚州圣贝纳迪诺
2016年11月29日

### 一本用大约100页教你 C# 的书？

快速高效地学习编程语言对于初学者和专业人士都至关重要。

无论你是经验丰富的 C++ 程序员，还是致力于成为全能程序员的初学者，C# 编程都是一项必备技能。C# 是一种通用编程语言，拥有大量现实应用。它用于 Windows Silverlight、移动开发、游戏开发和第三方 Windows 应用程序。它设计精良、易于学习且使用愉快。

通过 **《初学者计算机编程：学习 C# 基础》**，你将获得成为 C# 程序员所需的一切，包括：

- 如何设置计算机并启动新的 C# 项目
- 对数据类型和变量的基本理解
- 关键编程原理的介绍
- 软件或应用开发的基本技术
- 面向对象编程的基本概念
- 如何使用方法、数组、字符串、结构体和枚举
- 对继承、接口和多态性的总体理解

**Joseph Connor** 逐章带你掌握 C# 基础所需的所有关键概念。但本指南并未止步于此。你还将学习调试的基础知识，并从精通所有特性和细微差别的专家那里获得大量专业建议。

不要因为尚未学习 C# 而错过这个绝佳机会。今天就开始使用 **《初学者计算机编程：学习 C# 基础》** 吧。

向上滚动，立即购买你的副本。
