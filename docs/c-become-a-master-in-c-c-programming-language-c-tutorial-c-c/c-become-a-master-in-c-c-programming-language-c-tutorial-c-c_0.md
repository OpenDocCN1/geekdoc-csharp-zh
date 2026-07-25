# C#：成为 C# 大师（C# 编程语言、C# 教程、C# 编码、.NET、Visual Studio、C# 运算符、Python、Powershell、Javascript）





# 引言

![](img/00001.jpeg)

每当你使用 C#，以下电子书的重制如下，其目的是提供尽可能准确和可靠的信息。无论如何，购买此电子书均被视为同意：此书的出版者和作者对书中讨论的话题均非相关专家，且此处提出的任何建议或指示仅供娱乐之用。在采取本文此处支持的任何行动之前，应根据需要咨询专业人士。

此声明被美国律师协会（American Bar Association）和出版商协会委员会（Committee of Publishers Association）认为是公平且有效的，并在整个美国范围内具有法律约束力。

此外，传输、复制或重制以下任何作品（包括特定信息）都将被视为非法行为，无论是以电子形式还是印刷质形式进行。这包括创建作品的二次或三级副本或录制副本，并且只有在获得出版者的明确书面同意后才允许。保留所有其他权利。

后续页面中的信息被广泛认为是对事实的真实准确描述，因此读者对相关信息的任何疏忽、使用或误用将导致任何产生的结果完全由其个人负责。在任何情况下，本作品的出版者或原作者均不对在采取本文此处描述的信息后可能遭受的任何困难或损害承担责任。

此外，后续页面中的信息仅供参考之用，因此应被视为通用的。根据其性质，其呈现时不对对其长期有效性或中间质量提供保证。文中提到的商标是在未获得书面同意的情况下使用的，不能被视为商标持有者的背书。


![](img/00001.jpeg)

每当 .Net 框架正在开发时，类库是使用托管代码编译器编写的，这被称为 `Simple Managed C`。直到 99 年 1 月，Hejberg 才建立了一个团队开发了这种新语言，简称为 `Cool`，但实际上是 `C like Object Oriented Language`。当时微软曾考虑将 `Cool` 作为其项目的最终名称，但由于版权原因未采用。

在 2000 年专业开发者会议上，.Net 项目向业界宣布该语言被更名为 `C#`，类库被命名为 `ASP.Net`，而运行时被移植到了该语言中。

C# 语言的主要设计师也是微软的首席架构师，并参与了 `Turbo Pascal`、`Embarcadero Delphi`（曾名为 `CodeGear Delphi`）、`Inpris Delphi` 和 `BorlandDelphi` 的设计，还参与了 `Visual C++`。

当你开始使用 C# 时，你会注意到它是由 ECMA（欧洲计算机制造商协会）以及 ISO（国际标准组织）批准、由微软创建的语言，它是为了 CLI（通用语言基础设施）而设计的。

它的它的原因：

1. 你可以作为 .Net 框架的一部分使用它
2. 它是一种通用语言
3. 你可以跨平台使用
4. 它是一个面向对象的程序
5. 它将产生高效的程序
6. 它是组件化的
7. 这种语言结构化且易于学习

虽然 C# 看起来只是 C 语言的另一种变体，但由于以下事实，它更像 Java。

程序员发现的一些特性：

1. 它可以与 Windows 集成
2. 布尔条件
3. 用于 `LINQ` 和 `Lambda` 的表达式
4. 自动垃圾回收
5. 简单的多线程
6. 标准库
7. 条件编译
8. 程序集
9. 索引器
10. 属性和事件
11. 易于使用泛型
12. 委托和事件管理






1994 年，James Gosling 创建了 `Java` 语言，而 Sun Microsystems 的联合创始人 Bill Joy 则认为 `C#` 仅仅是 `Java` 语言的模仿。他甚至说道：“C# 就像是删除了可靠性、生产力和安全性的 Java。” Kreft 和 Langer 则反驳道，“Java` 和 `C#` 几乎是完全相同的编程语言。这种缺乏创新的无聊重复。几乎没有人会声称 `Java` 或 `C#` 是改变了我们编写程序方式的革命性编程语言。而且，`C#` 从 `Java` 中借鉴了很多，反之亦然。既然 `C#` 支持装箱和拆箱，我们将在 `Java` 中拥有一个非常相似的功能。”

2000 年后期，Hejlsberg 站出来并表示：“C# 不是 Java 的克隆版本，在设计上更接近 `C++`。”

自 2005 年发布 2.0 版本以来，`C#` 和 `Java` 沿着不同的轨迹演进，这使得它们彼此不再那么相似。最大的区别之一是语言中引入了泛型，这使得它们与众不同。`C#` 使用具现化（reification）来提供一等泛型对象，这些对象在类加载时生成代码以执行，能够在其他类中使用。此外，`C#` 还具有许多特性，使其成为一种函数式编程语言，并与 `C#` 3.0 版本发布的 `LINQ` 扩展协同工作。

以下是 `C#` 各版本发布时所添加的功能。

## 版本 2.0

1. 委托推断
2. 泛型
3. 静态类
4. 部分类
5. 委托的协变与逆协变
6. 匿名方法
7. 方法组转换
8. 迭代器
9. Getter/setter 独立访问访问性
10. 可空类

## 版本 3.0

1. 部分方法
2. 隐式类级局部变量
3. 表达式树
4. 对象和集合初始化器
5. Lambda 表达式
6. 自动实现属性
7. 查询表达式
8. 匿名类
9. 扩展方法

## 版本 4.0

1. 嵌入式互操作类
2. 动态绑定
3. 泛型协变与逆协变
4. 命名参数和可选参数

## 版本 5.0

1. 调用者信息属性
2. 异步方法

## 版本 6.0

1. 字典初始化器
2. 编译器服务
3. 运算符命名
4. 将静态类成员导入到命名空间
5. 字符串插值
6. 异常过滤器
7. 空传播器
8. 在 catch/finally 块中使用 Await
9. 表达式体成员
10. 自动属性初始化器
11. 仅限 getter 属性的默认值

## 版本 7.0

1. 表达式体 getter 和 setter
2. out 变量
3. 表达式体构造函数和终结器
4. 模式匹配
5. 泛型异步返回类型
6. 元组
7. ref 返回值和局部变量
8. 解构
9. 二进制字面量
10. 局地函数
11. 数字分隔符

## 版本 7.1

1. 默认表达式
2. 异步 main


![](img/00001.jpeg)

# C# 环境

`.Net` 是一个运行在自身平台上的框架，旨在帮助你编写 Windows 应用程序、Web 服务和 Web 应用程序。由于该框架设计用于用于几乎任何编程语言，因此它的应用程序可以在多个平台上运行。每种语言都有访问该框架的选项，以便相互通信。

`.Net` 框架通过包含大量代码库工作，你可以使用 `C#` 使用它们。`.Net` 框架的一些组件包括：

1. `LINQ`
2. `CLR`（通用语言运行时）
3. `WCF`（Windows 通信基础）
4. .Net Framework 类库
5. Windows Presentation Foundation
6. 通用语言规范
7. `WF`（Windows 工作流基础）
8. 通用类系统
9. `ADO. Net`
10. 元数据和程序集
11. `ASP. NET` 和 `ASP. Net AJAX`
12. Windows Forms

每个组件都会执行不同的任务，你可以通过使用该组件或查看微软提供的文档来了解它们。

## 集成开发环境

还有更多仅凭 `C Sharp` 就可以使用的开发工具，这些是：

1. Visual Web creator
2. `VS` (Visual Studio 2010)
3. `VCE` (Visual C# 2010 Express)

Web Creator 和 `VCE` 可以在微软官方网站找到。当你使用这些工具时，你将能够编写几乎任何类型的 `C#` 程序。你还可以选择编写源文件，并配合如 `Notepad` 等基础文本编辑器，这样可以使用命令行提示符（它是 .Net Framework 的一部分）将代码建模成程序集。

`VCE` 和 Web Creator 是比 Visual Studio 小的版本，并且具有相同的外观。

安装 Visual Studio 快速版时需要保持稳定的连接。

## 在 Linux 和 Mac 上编写程序

由于 `.Net` 框架是一个 Windows 系统软件功能；当你处理其他系统软件时，还可以使用其他版本。`Mono` 是 `.Net` 框架的一个变体，它可以与 `C#` 编译器配合工作并在 Linux 和 Mac OS 等多个不同的系统上运行。

`Mono` 的完全目的是能够运行为 Microsoft `.Net` 构建的应用程序，以便它们能够与其他系统软件（如 Android、iOS、Linux 和 Unix）开发的工具一起工作。

# 第四章

![](img/00001.jpeg)

## C# 的程序结构

在学习构建 `C#` 程序需要什么之前，你必须先了解编程语言是如何构建的。程序中的某些部分对于确保你在创建 `C#` 程序时添加了它们至关重要。

1. 注释
2. 命名空间声明
3. 语句和表达式
4. 类
5. `main` 方法
6. 类方法
7. 类属性

示例

```csharp
using system;

Namespace helloouterspaceapplication
{

Class helloouterspace
{Static void main (tuple [] para)
{
/* 你的第一个 C # 程序 */
Console. Write line (“hello outer space”);
Console. Ready key ();
}
}

}
```

一旦代码执行，你将得到“Hello outer space”的结果。

你程序中的第一行是代码中的 `using system` 部分。`using` 关键字为程序包含一个系统的命名空间。大多数 `C#` 程序使用多个 `using` 语句。

你的命名空间声明是你所使用的类的集合。你的应用程序名称将是该应用程序的类。

你的类声明将包含程序最终使用的所有数据和定义。类将包含多个方法，这些方法最终将定义类的行为。但示例中使用的类只有一个名为 `main` 的方法。

你的 `main` 方法是所有 `C#` 程序的入口点。该方法将规定类何时被执行。

星号和斜杠会被编译器忽略，因为它们是程序的注释。

你的 `main` 方法将告诉你你的语句将遵循什么行为。

`Write line` 是 `console` 类在命名空间中完整写时将使用的方法。这条语句将导致你的结果显示在你面前的屏幕上。




对于 VS.Net 用户来说，底线在于。这将导致程序等待按下某个键，最终这将阻止你的页面在每次从 visual studio 启动程序时自动打开和关闭。

你需要记住以下几点：

1. 文件名必须与类名不同
2. `C#` 是区分大小写的
3. 你的执行将从 `main` 方法开始
4. 你的所有语句和表达式必须以分号结尾

## 编译并运行你的程序

如果你打算在 Visual Studio 中使用 .Net，你需要执行以下步骤。

1. 你需要打开 visual studio
2. 移动到菜单栏，进入 `file`、`new`、`project`
3. 选择一个模板，然后选择 `Windows`
4. 进入控制台应用程序（console application）
5. 选择你想为项目命名的名称
6. 你的新项目将在解决方案管理器中创建
7. 现在你可以用代码编辑器编写代码
8. 选择运行按钮来执行你的项目。命令提示符将会出现并显示你的输出。

当你使用命令行而不是 visual studio 使用 `C#` 编译程序时，请遵循以下步骤：

1. 选择你喜欢的文本编辑器并插入你将使用的代码
2. 使用你的文件名保存文件并添加 `.cs` 后缀
3. 需要打开命令提示符，以便定位到存放文件的目录
4. 输入 `CSC` 和你的文件名，然后按回车键强制编译你的代码
5. 如果没有错误，下一行将引起你的注意，该行是生成可执行文件的行
6. 输入你的代码来运行程序
7. 你的输出应该打印在屏幕上。

# 第五章

![](img/00001.jpeg)

## C# 语法

由于 `C#` 是一种面向对象的编程语言，你将需要使用对象来与其他对象交互，从而创建动作。这些动作在每次使用时都会创建方法。相同的对象将具有同一个类或位于同一个类中。

以矩形为例。长度和宽度是矩形的属性。根据矩形的设计，在计算面积和显示细节时，这些属性会接受特定的值。

**示例：**

```csharp
using system;

Namespace circle application

{

Class circle
{

    // variables
    Double width;
    Double circumference

    Open void accept details ()
    {
        Width = 3.4
        Circumference = 3.2
    }

    Open double ()
    {
        Return width * circumference
    }

    Open void display ()
    {
        Console.WriteLine("width: {0}", width);
        Console.WriteLine (circumference: {0}, circumference);
    }
}

Class perform
{
    Static void main (string [] para)
    {
        Circle c = new circle ();
        accept details ();
        display ();
    }
}
```

对于上面的示例，是 circle。

**Using**
在 `C#` 中，你的第一个语句总是 `using system;`。`using` 关键字用于命名空间（namespaces）。

**Class**
当你声明类时使用 `class` 关键字。

**注释**
当你需要解释你的代码时使用注释。`C#` 编译器将忽略你编写的注释。多行注释以 `/*` 开始，以 `*/` 结束。单行注释使用双斜杠。

**成员变量**
这些变量是类的成员属性。当使用时，它们可以存储数据。

**成员函数**
成员函数是执行任务的语句。这些函数通常在类内部声明。

**实例化**
类包含 `main` 方法中的类名。

**标识符**
标识符是用于标识类、变量和函数的单词。在 `C#` 中创建标识符有三个规则：

1. 不能使用 `C#` 中找到关键字
2. 必须以字母开头，然后是字母、数字或下划线。但不能以数字开头。
3. 可以使用任何字符但下划线。

**C# 中的关键字**
关键字是 `C#` 保留的单词。但如果你想将这些单词作为标识符，可以在单词前使用 `@` 符号以使其有效。`C#` 中找到的标识符具有特殊含义，导致某些被称为上下文关键字（contextual keywords）。

**保留关键字**
`Abstract`, `Catch`, `Default`, `Explicit`, `Foreach`, `Interface`, `Null`, `Private`, `Sealed`, `Switch`, `Ulong`, `Volatile`, `While`, `Unchecked`, `This`, `Short`, `Protected`, `Internal`, `Goto`, `Extern`, `Delegate`, `Char`, `As`, `Base`, `Checked`, `Do`, `False`, `If`, `Is`, `Operator`, `Open`, `Sizeof`, `Throw`, `Unsafe`, `Ushort`, `True`, `Stackalloc`, `Readonly`, `Out`, `Lock`, `Implicit`, `Finally`, `Double`, `Class`, `Bool`, `Break`, `Const`, `Else`, `Fixed`, `In`, `Long`, `Out`, `Ref`, `Static`, `Try`, `Using`, `Virtual`, `Classof`, `String`, `Return`, `Override`, `Namespace`, `In`, `Float`, `Enum`, `Continue`, `Byte`, `Case`, `Decimal`, `Event`, `For`, `Int`, `New`, `Params`, `Sbyte`, `Struct`, `Uint`, `Void`。

**上下文关键字**
`Partial`, `Get`, `From`, `Orderby`, `Let`, `Dynamic`, `Set`, `Join`, `Descending`, `Ascending`, `Into`, `Select`, `Remove`, `Group`, `Alias`, `Partial`, `Global`, `Add`。

# 第六章

![](img/00001.jpeg)

## 数据类

`C#` 中有三种不同的数据类：

1. `Pointer`（指针）
2. `Value`（值）
3. `Reference`（引用）

## 值类

值类是你直接赋值给值的变量。这些派自 `system.value.class`。

值类直接包含数据，如 `char`、`int` 和 `float`。每当声明 `int` 类时，系统都会留出空间。

**值类：**
1. `Bool`:布尔值
2. `Byte`:8 位无符号整数
3. `Char`:16 位 Unicode 字符
4. `Decimal`:128 位高精度小数值，最多有 29 位有效数字
5. `Double`:64 位双精度浮点类
6. `Float`:32 位单精度浮点类
7. `Int`:32 位有符号整数
8. `Long`:64 位有符号整数
9. `Sbyte`:有符号 8 位整数
10. `Short`:16 位有符号整数
11. `Uint`:32 位无符号整数
12. `Ulong`:64 位无符号整数
13. `Ushort`:16 位无符号整数

变量的具体大小取决于所使用的平台，可以通过使用 `Sizeof` 方法找到。此表达式将产生以字节为单位的对象所需的存储大小。

**语法**
```csharp
using system;

Namespace dataclass application

{

Class program
{

    Static void main (string [] args)
    {
        Console.Write line (size of int: {0}, Sizeof (int));
        Console. ReadiLine ()
    }
}

}
```



你并不会在引用类（reference class）中实际存储任何数据。基本上，你只是在引用程序内存中的一个位置。当你使用多个变量时，你的引用类将指向这些类所处的位置。如果该位置上的数据被某个变量修改，那么另一个变量将自动反映该变化。

## 对象类 (OBJECT CLASS)

此类将成为你在 C# 中找到的每个数据类的基类。CTS（公共类系统）在使用系统时会使用一个别名：`Object class`。只要该类是由程序预定义的或由用户定义的，此对象类就有被赋值给本章将要讨论的其他类的选项。在你有赋值选项之前，它需要进行转换。

每当对象类被转换时，它将被称为“装箱”（boxing），当它被转换为值类时，它被称为“拆箱”（unboxing）。

## 动态 (DYNAMIC)

任何类的任何值都可以存储在 `dynamic` 类中。你需要检查这些类型的变量，因为它们发生在运行时。`dynamic` 类与对象类类似，但对象的类检查是在编译时进行的。

### 语法

```
Dynamic < variable_ name> = value;
```

## 字符串类 (STRING CLASS)

此类允许你为任何变量分配任何字符串值。字符串类在系统字符串类中包含一个别名。此类也继承自对象类。你会发现字符串类的值是通过字符串字面量赋值的，字符串字面量有两种形式：带引号的和带 `@` 符号的（quoted）。

用户定义的引用类被称为接口（interface）、委托（delegate）和类（class）。

## 指针类 (POINTER CLASS)

指针变量将存储其他类的内存地址。这些指针具有与其它 C 语言中的指针相同的能力。

### 语法

```
Class * identifier;
```

# 第七章

![](img/00001.jpeg)

## C# 中的类转换

C# 类转换是将将一个数据类转换为另一个数据类的行为。你可能也知道这些转换称为类强制转换（class casting）。你会发现有两种不同类型的强制转换。

1. `隐式转换` (Implicit conversion)：在此转换下转换的类将由 C# 以与被转换类相同的方式进行执行。例如，当 `convariations` 从最小到最大转换时，这将使你的 `convariations` 派类转换为基类。
2. `显式转换` (Explicit conversion)：显式转换由用户在处理预定义函数时完成。这些转换需要强制转换运算符。

### 语法

```c
using System;

namespace TypeClassConversionApplication
{

class ExplicitConversion
{

static void Main (string [] args)
{

double d = 5673.74;

int i;

// 将 double 转换为 int.
i = (int)d;

Console.WriteLine(i);

Console.ReadKey();

}

}

}
```

## 转换方法

1. `Toboolean`：布尔类将进行转换
2. `To byte`：字节将被转换
3. `Tochar`：单个 Unicode 字符中的字符将被转换
4. `Todatime`：你的日期时间结构将进行转换
5. `Todecimal`：浮点数或整数将转换为小数类。
6. `Todouble`：类将转换为 double 类
7. `Toint16`：类将转换为 16 位整数
8. `Toint32`：类将转换为 32 位整数
9. `Toin64`：类将转换为 64 位整数
10. `Tosbyte`：你的类将转换为有符号字节类
11. `Tosingle`：类将转换为浮点数，但它很小
12. `To string`：你的类将转换为字符串
13. `To class`：你的类将转换为你指定的类
14. `Touint16`：你将拥有无符号 int 类
15. `Touint32`：你将拥有无符号 long 类
16. `Touint64`：你将得到一个无符号整数。

**示例：**

```csharp
using System;

namespace ClassConversionApplication
{

class StringConversion
{

static void Main (string [] args)
{

int i = 75;

float f = 53.005f;

double d = 2345.7652;

bool b = true;

Console.WriteLine(i.ToString());

Console.WriteLine(f.ToString());

Console.WriteLine(d.ToString());

Console.WriteLine(b.ToString());

Console.ReadKey();

}

}

}
```


![](img/00001.jpeg)

# C# 中的变量

变量本质上除了被放置在用于操作的存储区域中的一个名称外，什么也不是的。每个变量都将包含一个特定的类，其中大小将被确定，以及变量内存的布局。每块内存都都有一个存储在内部的值范围，以及一组可以应用于每个变量的操作。

C# 提供的某些基本值类包括：

1. `整数类`：`char`, `ulong`, `long`, `uint`, `int`, `ushort`, `short`, `byte`, `sbyte`
2. `浮点数`：`double` 和 `float`
3. `小数类`：`decimal`
4. `布尔`：`true`, `false`, `assigned`
5. `可空类`：`nullable`

C# 让你能够使用 `class` 和 `enum` 等变量来定义值类。

## 定义变量

### 语法

```
<data_class> <variable_lists>;
```

数据类必须是 C# 数据类的一部分并且必须是有效的。你的变量列表必须包含至少一个标识符，并用逗号分隔。

**变量定义：**

`int i, j, k;`
`char c, ch;`
`float f, salary;`
`double d;`

### 初始化变量

在初始化变量时，将有一个等号，后面跟着一个常量表达式。

### 语法

```
Variable_name = value;
```

你可以在声明内部初始化变量。此初始化器将有一个等号，后面跟着一个常量表达式

### 语法

```
<data_class> <variable_name> = value;
```

**示例：**

```csharp
int d = 3, f = 5; /* 初始化 d 和 f. */
byte z = 22; /* 初始化 z. */
double pi = 3.14159; /* 声明 pi。 */
char x = 'x'; /* 变量 x 的值为 'x'. */
```

你需要正确的方式初始化变量，否则程序将给你非预期的结果。

**示例：**

```csharp
using System;

namespace VariableDefinition
{

class Program
{

static void Main(string[] args)
{

short a;

int b;

double c;

/* 实际初始化 */
a = 10;

b = 20;

c = a + b;

Console. WriteLine("a = {0}, b = {1}, c = {2}", a, b, c);

Console.ReadLine();

}

}


**从用户接受值**

你的 `console` 类可以在 `system` 命名空间中找到，它将提供一个名为 `readline()` 的函数，可以使用它来接受来自用户的输入并存储在变量中。

**示例：**

```csharp
int num;
num = Convert.ToInt32(Console.ReadLine());
```

## 左值和右值表达式

在 C# 中你会发现两种不同的表达式

1. `右值` (Rvalue)：此表达式将出现在工作的右侧，而不是左侧。
2. `左值` (Lvalue)：这将在出现在工作时的左侧或右侧。

`lvalues` 的变量将使它们出现在左侧。数字字面量将是 `r values`，这解释了为什么它们无法赋值，因此不能出现在大脑的左侧。




你的常量将引用一个在程序执行代码期间固定且无法更改的值。这些固定的值被称为字面量。常量可以是任何数据类型，例如整数或字符。你也可以拥有枚举常量。

你可以像普通变量一样对待你的常量，区别在于你的值在定义后将不会改变。

## 整数字面量

整数字面量是指如十进制或十六进制等内容。前缀会告诉你基数或进制制。当你处理十六进制时，前缀将是 `0x` 或 `0X`，但十进制没有前缀。

你的整数字面量还可以使用 `U` 和 `L` 作为无符号（unsigned）和长型（long）的后缀。后缀可以是大写或小写。

### 示例

```
85 /* decimal */
0x4b /* hexadecimal */
30 /* int */
30u /* unsigned int */
30l /* long */
30ul /* unsigned long */
```

## 浮点数字面量

浮点字面量由四个部分组成：指数、小数部分、整数、小数点。你还可以用指数形式或十进制形式表示这些字面量。

### 示例

```
3.14159 /* Legal */
314159E-5F /* Legal */
510E /* Illegal: incomplete exponent */
210f /* Illegal: no decimal or exponent */
.e55 /* Illegal: missing integer or fraction */
```

当使用十进制形式时，你需要确保包含小数点、指数，甚至两者都有。对于指数形式，你需要包含整数部分、小数部分，或者如果你愿意，也可以都包含。对于符号指数，你将使用 `e` 或 `E`。

## 字符常量

字符字面量由单引号包围并存储在 `char` 类中。这些字面量可以是普通字符甚至是转义序列，你甚至可能会看到通用字符。

在 C# 中使用的某些字符前面会有反斜杠，这意味着它们具有特殊含义并以不同的方式表示。

转义序列有：

1. `\xhh`: 带有位数的十六进制
2. `\\`: \字符
3. `\v`: 垂直制表符
4. `\’`: ‘字符
5. `\t`: 水平制表符
6. `\”`: “字符
7. `\r`: 回车符
8. `\?`: ?字符
9. `\n`: 换行符
10. `\a`: 警报
11. `\f`: 分页符
12. `\b`: 退格

### 示例

```csharp
using System;

namespace EscapeChar
{
class Program
{
static void Main(string[] args)
{
Console.WriteLine("Hello\tWorld\n\n");
Console.ReadLine();
}
}
}
```
## 字符串字面量

字符串字面量或常量由双引号包围，或包含 @ 符号。这些字符串充满了与字符字面量类似的字符。

只要使用空格进行分离处理，长行可以通过字符串字面量拆分为多行。

### 示例

```
"hello, dear"
"hello, \
dear"
"hello, " "d" "ear"
@"hello dear"
```

## 定义常量

常量通过使用 `const` 关键字定义。

### 语法

`const <data_class> <constant_name> = value;`

### 示例

```csharp
using System;

namespace DeclaringConstants
{
class Program
{
static void Main(string[] args)
{
const double pi = 3.14159;
// constant declaration
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


![](img/00001.jpeg)

# C# 运算符

运算符是告知编译器在数学或逻辑表达式中执行什么操作的符号。C# 内置了某些运算符，例如：

1. 杂项
2. 算术
3. 赋值
4. 关系
5. 位运算
6. 逻辑

## 算术运算符

1. 加法 (`+`)
2. 减法 (`-`)
3. 乘法 (`*`)
4. 除法 (`/`)
5. 取模 (`%`)
6. 加一 (`++`)
7. 减一 (`--`)

## 关系运算符

1. 值是否为真？ (`==`)
2. 值是否相等 (`!=`)
3. 大于 (`>`)
4. 小于 (`<`)
5. 大于或 (` (`>=`)
6. 小于等于 (`<=`)

## 逻辑运算符

1. 逻辑与 (`&&`)
2. 逻辑或 (`||`)
3. 逻辑非 (`!`)

## 位运算

1. 二进制与 (`&`)
2. 二进制或 (`|`)
3. 二进制异或 (`^`)
4. 二进制按位取反 (`~`)
5. 二进制左移 (`<<`)
6. 二进制右移 (`>>`)

## 赋值运算符

1. 赋值 (`=`)
2. 相加并赋值 (`+=`)
3. 减法并赋值 (`-=`)
4. 乘法并赋值 (`*=`)
5. 除法并赋值 (`/=`)
6. 取模并赋值 (`%=`)
7. 左移并赋值 (`<<=`)
8. 右移并赋值 (`>>=`)
9. 位与并赋值 (`&=`)
10. 位异或并赋值 (`^=`)
11. 位或并赋值 (`|=`)  *(注：原文!=此处为误，应为|=，此处保留原文意图或修正逻辑)*

## 杂项

1. `Sizeof()`
2. `Classof()`
3. 变量地址 (`&`)
4. 变量指针 (`*`)
5. 三元表达式 (`? :`)
6. 对象类型判断 (`is`)
7. 如果类型转换失败时不抛出异常 (`as`)

## 运算符优先级

C# 中的优先级会告诉你哪一组项先求值。某些运算符的优先级高于其他运算符，例如乘法的优先级高于加法。

这里是 C# 的优先级：

1. 后置：`()`, `[]`, `.`, `++`, `--`
2. 一元：`+`, `-`, `!`,`~`, `++`, `--`, `(class)*`, `&`, `Sizeof`
3. 乘法：`*`, `/`, `%`
4. 加法：`+`, `-`
5. 移位：`<<`, `>>`
6. 关系：`<`, `<=`, `>`, `>=`
7. 等：==`, `!=`
8. 位与：`&`
9. 位异或：`^`
10. 位或：`|`
11. 逻辑与：`&&`
12. 逻辑或：`||`
13. 三元：`?:`
14. 赋值： `=`, `+=`, `-=`, `^=`, `/=`, `%=`, `=>`, `>=`, `<<=`, `&=`, `^=`, `|=`
15. 逗号：`,`


![](img/00001.jpeg)

# 使用 C# 进行决策

你将使用 C# 中的决策机制来学习程序是如何工作的。决策的结构意味着你需要告诉程序哪些条件需要评估和测试，以及在条件为真或假时需要执行的语句。

## 决策语句

1. If 语句：有一个布尔表达式。
2. If-else 语句：这是一个后面跟着 else 语句的 if 语句。
3. 嵌套语句：嵌套在另一个语句内部的语句。
4. Switch 语句：此语句允许对变量进行相等性测试。
5. 嵌套 switch 语句：放在另一个 switch 语句内部的 switch 语句。

### ? : 运算符

该运算符可以代替 if-else 语句。

### 语法

`Expression one ? expression two : expression three;`

该表达式的值取决于 expression one 的评估结果是否为真。如果是，则将评估 expression 二 并作为问号的值。然而，如果 expression one 被判断为假，则 expression 三 将求值并成为你的表达式的值。

# 第十二章

![](img/00001.jpeg)

## 循环

在某些情况下，你会发现自己需要连续执行多次特定的代码块。语句是按照它们编写的顺序执行的。

大多数编程语言都会提供控制结构，允许你处理更复杂的执行路径。循环允许语句执行多次，而不需要不断编写需要执行的语句。

1. While 循环：如果条件为真，则重复所选语句。
2. For 循环：语句将执行并缩写，以便管理循环变量。





3. `while loop`：条件将在循环体结束时进行测试。

4. `Nested loop`：和其他嵌套语句一样，这是在一个循环内部的另一个循环。

## 循环控制语句

控制语句将改变循环的执行方式，使其脱离正常执行。每当执行离开作用范围时，任何自动对象将被销毁。

1. `Break statement`：循环或 `switch` 语句将终止，同时执行循环或 switch 之后的语句。

2. `Continue statement`：循环将跳过其所有的循环体，并在再次迭代之前测试条件。

## 死循环

当循环的条件从未被判定为假时，循环就会属于这一类别。`for` 循环通常属于这一类。由于三个表达式中的任何一个都不是要求的，你可以通过留空条件表达式来导致死循环的发生。

### 示例

```csharp
using System;

namespace Loops

{

class Program
{

static void Main(string[] args)
{

for (; ; )
{

Console.WriteLine("Hey! I am Trapped");

}

}

}

}
```

只要条件表达式不存在，就会被假设为真。你可能会发现你必须初始化增量表达式。然而，许多程序员使用 `for (; ; )` 来构建一个死循环。

# 第十三章

![](img/00001.jpeg)

## C# 中的封装

你将封装定义为将一个或多个项目封装在一个逻辑或物理包内部。封装是在面向对象的编程语言内部完成的，这种方法最终防止了对实现细节的访问。

抽象和封装是你只能在面向对象编程中找到的。然而，抽象将代码中的相关信息变为可见的代码，而封装允许程序员在代码中实现他们想要的抽象级别。
访问修饰符可以实现封装。访问修饰符定义了类成员的作用范围和可见性。这些是 C# 支持的标识符。

1. `Protected internal`
2. `Open`
3. `Internal`
4. `Private`
5. `Protected`

## OPEN

这些修饰符允许类显示成员变量和函数，以便其他对象和函数可见。当成员为 `Open` 时，可以从外部访问它。

### 示例

```csharp
using System;

namespace RectangleApplication

{

class Rectangle
{

//member variables

Open double length;

Open double width;

Open double GetArea()
{

return length * width;

}

Open void Display()
{

Console.WriteLine("Length: {0}", length);

Console.WriteLine("Width: {0}", width);

Console.WriteLine("Area: {0}", GetArea());

}

}//end class Rectangle

class PerformRectangle
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

在这个示例中，你可以看到成员变量 `length` 和 `width` 将是 `Open` 的，以便可以通过类名从你的函数中访问它们。你的成员函数只有直接访问变量的能力，而无需使用任何类实例。它们还通过使用 `main()` 函数声明为 `Open`。

## PRIVATE

`Private` 修饰符允许类向代码中的其他内容隐藏成员变量和函数。只有在同一个类中的函数才有权访问私有成员。甚至存在类无法访问私有成员的情况。

### 示例

```csharp
using System;

namespace RectangleApplication

{

class Rectangle
{

//member variables
private double length;

private double width;

Open void Acceptdetails()

{

Console.WriteLine("Enter Length: ");

length = Convert.ToDouble(Console.ReadLine());

Console.WriteLine("Enter Width: ");

width = Convert.ToDouble(Console.ReadLine());

}

Open double GetArea()
{

return length * width;

}

Open void Display()
{

Console.WriteLine("Length: {0}", length);

Console.WriteLine("Width: {0}", width);

Console.WriteLine("Area: {0}", GetArea());

}

}//end class Rectangle

class PerformRectangle
{

static void Main(string[] args)
{

Rectangle r = new Rectangle();

r.Acceptdetails();

r.Display();

Console.ReadLine();

}

}

}
```

在上面的示例中，成员变量被声明为 `private`，因此函数无法访问它们。然而，成员函数将显示这些变量。由于成员函数是 `open` 的，因此可以通过使用类名的实例从主函数中访问它们。

## PROTECTED 访问修符

此修饰符允许子类访问其基类中的成员变量和函数。这在你处理继承时会非常有帮助。

## INTERNAL 访问修饰符

`internal` 访问修饰符允许成员函数和变量暴露给你正在工作的程序集中的其他函数和对象。因此，只要它定义在定义成员的应用程序中，你就可以访问任何类或方法。

### 示例

```csharp
using System;

namespace RectangleApplication

{

class Rectangle
{

//member variables

internal double length;

internal double width;

double GetArea()
{

return length * width;

}

Open void Display()
{

Console.WriteLine("Length: {0}", length);

Console.WriteLine("Width: {0}", width);

Console.WriteLine("Area: {0}", GetArea());

}

}//end class Rectangle

class PerformRectangle
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

此示例显示成员函数没有使用提供访问的修饰符声明。因此，由于它是私有的，没有提到类成员的默认访问修饰符。

## PROTECTED INTERNAL 访问修饰符

此修饰符将一个类的成员变量和函数从其他类对象和函数隐藏，除了同一应用程序中的子类情况外。你在实现继承时将使用这种方法。

# 第十四章

![](img/00001.jpeg)

## C# 中使用的方法

方法是按顺序工作的以执行任务的语句组。C# 中的每个程序都将有一个类方法 `main`。

为了使用方法，你必须：

1. 定义你的方法
2. 调用你的方法

## 定义方法

每当定义方法时，你必须声明该结构的元素。

**语法**

```
<access specifier> <return class> <method name> (parameter list)

{

Method body
}
```

方法的某些元素是：

1. `access specifier`：变量的可见性将由另一个类决定。
2. `return class`：方法将返回一个值。这个返回的类将返回给你的值的数据类型。如果方法不返回值，则返回类将是 `void`。
3. `method name`：方法名是区分大小写的标识符。它不会与类中声明的其他标识符相同。
4. `parameter list`：在括号之间的参数将用于从正在使用的方法中传递和获取数据。参数是指方法正在使用的参数的顺序、数量和类型。参数并不必须使用。





## 5. 方法体：这里将是你的指令，你需要它们来完成需要执行的步骤。

### 示例

```csharp
class NumberManipulator
{
    Open int FindMax(int num1, int num2)
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

## 调用方法

通过使用你想要调方法的名称来调用方法。

### 示例

```csharp
using System;
namespace CalculatorApplication
{
class NumberManipulator
{
    Open int FindMax(int num1, int num2)
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
        //调用 FindMax 方法
        ret = n.FindMax(a, b);
        Console. WriteLine("Max value is : {0}", ret);
        Console.ReadLine();
    }
}
```你还可以从其他类调用 Open 方法的方法。

### 示例

```csharp
using System;
namespace CalculatorApplication
{
class NumberManipulator
{
    Open int FindMax(int num1, int num2)
    {
        /* local variable declaration */
        int result;
        if (num1 > num2)
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
        //调用 FindMax 方法
        ret = n.FindMax(a, b);
        Console. WriteLine("Max value is : {0}", ret);
        Console.ReadLine();
    }
}
```

## 递归调用

这种方法是它自身的调用，被称为递归。

### 示例

```csharp
using System;
namespace CalculatorApplication
{
class NumberManipulator
{
    Open int factorial(int num)
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
        //调用 factorial 方法
        Console. WriteLine("Factorial of 6 is : {0}", n.factorial(6));
        Console. WriteLine("Factorial of 7 is : {0}", n.factorial(7));
        Console. WriteLine("Factorial of 8 is : {0}", n.factorial(8));
        Console.ReadLine();
    }
}
```

## 向方法传递参数

每当调用参数时，必须将参数传递到方法。至少有三种方法可以传递：

1. 值参数：将参数的值复制到函数的形式参数中。这样做后，对参数的任何更改都不会影响参数。
2. 引用参数：你的引用将复制到形式参数的内存位置。这意味着你对参数所做的更改将影响参数。
3. 输出参数：你将获得多一个值。


![](img/00001.jpeg)

# C# 中的可空类型

可空类型是特殊数据类型，可以将范围赋值为 null。

你可以存储从 -2,147,483,648 到 2,147,483,647 之间的任何值。你也可以分配 true、false 或 null 输出。

### 语法

`<data_class> ? <variable_name> = null;`

### 示例

```csharp
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
        //显示值
        Console. WriteLine("Nullables at Show: {0}, {1}, {2}, {3}", num1, num2, num3, num4);
        Console. WriteLine("A Nullable boolean value: {0}", boolval);
        Console.ReadLine();
    }
}
}
```

# 合并运算符 ( ?? )

当使用可空类型和引用类型时可以使用合并运算符。你使用合并运算符将操作数转换为另一个可能的可空类型操作数。

如果第一个操作数为 null，那么当运算符返回第二个操作数时，它将返回第一个操作数的值。

### 示例

```csharp
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
        Console. WriteLine(" Value of num3: {0}", num3);
        num3 = num2 ?? 5.34;
        Console. WriteLine(" Value of num3: {0}", num3);
        Console.ReadLine();
    }
}
}
```


![](img/00001.jpeg)

# C# 中的数组

数组存储固定大小顺序的对象或数据类型集合。数组可以用于存储作为数组比不同数据类型更有用的数据集合。它还使其存储在连续的内存位置上。

与其声明单独变量，你可以在数组中声明一个数字变量，并使用方括号表示单独变量。你的变量将有一个索引，用于访问该元素。数组由连续内存位置组成，最低地址指向第一个元素。

## 声明数组

### 语法

`<dataclass>[] name;`

1. `dataclass` 告诉你是什么类。
2. 方括号 `[]` 告诉你秩（rank）。秩告诉大小。
3. `name` 显然告诉你数组的名称。

### 示例

```csharp
Double [ ] hello
```

## 数组初始化

当声明数组时，需要在内存中初始化数组。数组被称为引用类型，这意味着你需要使用 `new` 关键字来实例化。

### 示例

```csharp
Double [ ] hello = new double [ 3 ]
```

## 给数组赋值

值可以通过索引分配给数组元素。你可以通过在数组名称后的一组方括号内放置元素的索引来这样做。

### 示例

```csharp
using System;
namespace CalculatorApplication
{
class MyArray
{
    static void Main(string[] args)
    {
        int [] n = new int[10]; /* n 是一个 10 个整数数组 */
        int i,j;
        /* 初始化数组 n 的元素 */
        for ( i = 0; i < 10; i++ )
        {
            n[ i ] = i + 100;
        }
        /* 输出每个数组元素的值 */
        for(j = 0; j < 10; j++ )
        {
            Console. WriteLine("Element[{0}] = {1}", j, n[j]);
        }
        Console.ReadKey();
    }
}
}
```

## for each 循环

for each 语句将用于遍历数组。

### 示例

```csharp
using System;
namespace CalculatorApplication
{
class MyArray
{
    static void Main(string[] args)
    {
```





```cs
int [] n = new int[10]; /* n 是一个包含 10 个整数的数组 */

/* 初始化数组 n 的元素 */
for ( int i = 0; i < 10; i++ )
{
    n[i] = i + 100;
}

/* 输出每个数组元素的值 */
foreach (int j in n )
{
    int i = j-100;
    Console. WriteLine("Element[{0}] = {1}", i, j);
}
Console.ReadKey();
}
}
}
```

# 数组

1. 多维数组
2. 锯齿数组
3. 将数组传递给函数
4. 参数数组 (Param array)
5. 数组类

# 第十七章

![](img/00001.jpeg)

## C# 中的字符串

在 C# 中，你可以将字符串当作数组使用。但更常用的操作之一是使用 `string` 关键字来声明字符串变量。`string` 关键字是 `System.String` 的别名。

## 创建字符串对象可以通过以下方式创建 `String` 对象：

1. 调用格式化方法以将值或对象转换为字符串表示
2. 将字符串字面量赋值给 `string` 变量、获取属性或调用将返回字符串的方法
3. 使用 `String` 类的构造函数
4. 使用字符串拼接运算符。

### 示例

```cs
using System;
namespace StringApplication
{
class Program
{
static void Main(string[] args)
{
// 来自字符串字面量和字符串拼接
string fname, lname;
fname = "Rowan";
lname = "Atkinson";
string fullname = fname + lname;
Console. WriteLine("Full Name: {0}", fullname);
// 使用字符串构造函数
char[] letters = { 'H', 'e', 'l', 'l','o' };
string greetings = new string(letters);
Console. WriteLine("Greetings: {0}", greetings);
// 返回字符串的方法
string[] sarray = { "Hello", "From", "Tutorials", "Point" };
Console. WriteLine("Message: {0}", message);
// 用于转换值的格式化方法
DateTime waiting = new DateTime(2012, 10, 10, 17, 58, 1);
string chat = String.Format("Message sent at {0:t} on {0:D}", waiting);
Console. WriteLine("Message: {0}", chat);
}
}
}
```

## 字符串类的属性

1. Chars：在 `string` 对象的特定位置获取 `char` 对象
2. `Length`：你的 `string` 对象中的字符数量

## 字符串类的方法

`String` 类有许多方法，可以帮助你处理 `string` 对象的工作更加轻松。

1. `Open static int compare (string strA, string strB)`
2. `Open static int compare (string strA, string strB, bool ignoreCase )`
3. `Open static string concat (string str0, string str 1)`
4. `Open static string concat( string str0, string str1, string str 2)`
5. `Open static string concat (string str0,string str1, string str2, string str 3)`
6. `Open bool contains (string value)`
7. `Open static string copy (string str)`
8. `Open void copyto (int sourceindex, char [] destination, int destinationindex, int count)`
9. `Open bool endswith (string value)`
10. `Open bool equals (string value)`
11. `Open static bool equals (string a, string b)`
12. `Open static string format (string format, object arg 0)`
13. `Open int index of (char value)`
14. `Open int index of (string value)`
15. `Open int indexof (char value, int startindex)`
16. `Open int indexof (string value, int start index)`
17. `Open int indexof any (char [] anyof)`
18. `Open int index of any (char [] anyof, int start index)`
19. `Open string insert (int startindex, string value)`
20. `Open static bool is null or empty (string value)`
21. `Open static string join (string separator, params string [] value)`
22. `Open static string join (string, string [] value, int start index, int count)`
23. `Open int last index of (char value)`
24. `Open int last index of (string value)`
25. `Open string remove (int start index)`
26. `Open string remove (int start index, int count)`
27. `Open string replace (char old char, cha new char)`
28. `Open string replace (string old value, string new value)`
29. `Open string [] split (params char [] separator)`
30. `Open string [] split (char [] separator, int count)`
31. `Open bool starts with (string value)`
32. `Open char [] to char ()`
33. `Open char [] to char array (int start index, int length)`
34. `Open string to lower ()`
35. `Open string to upper ()`
36. `Open string trim ()`

### 示例

```cs
using System;
namespace StringApplication
{
{
static void Main(string[] args)
{
string str1 = "This is test";
string str2 = "This is text";
if (String.Compare(str1, str2) == 0)
{
Console. WriteLine(str1 + " and " + str2 + " are equal.");
}
else
{
Console. WriteLine(str1 + " and " + str2 + " are not equal.");
}
Console.ReadKey() ;
}
}
```

### 字符串包含包含示例

```cs
using System;
namespace StringApplication
{
class StringProg
{
static void Main(string[] args)
{
string str = "This is test";
if (str.Contains("test"))
{
Console. WriteLine("The sequence 'test' was found.");
}
Console.ReadKey() ;
}
}
```

### 获取子字符串示例

```cs
using System;
namespace StringApplication
{
class StringProg
{
static void Main(string[] args)
{
string str = "Last night I dreamt of San Pedro";
Console. WriteLine(str);
string substr = str.Substring(23);
Console. WriteLine(substr);
}
}
```

### 合并字符串示例

```cs
using System;
namespace StringApplication
{
class StringProg
{
static void Main(string[] args)
{
string[] starray = new string[]{"Down the way nights are dark",
"And the sun shines daily on the mountain top",
"I took a trip on a sailing ship",
"And when I reached Jamaica",
"I made a stop"};
string str = String.Join("\n", starray);
Console. WriteLine(str);
}
}
```


![](img/00001.jpeg)

# C# 结构 (STRUCTURES)

在 C# 中，值类可以帮助你创建与该数据类相关的单个变量。使用 `struct` 关键字来创建结构。结构用于表示记录。

## 定义结构

要定义结构，你需要使用 `struct` 语句。该语句用于在程序中定义一个具有多个成员的新数据类。

### 示例

```cs
using System;
struct Books
{
string title;
string author;
string subject;
int book_id;
};

class testStructure
{
static void Main(string[] args)
{
Books Book1; /* 声明 Books1 类 */
Books Book2; /* 声明 Books2 类 */
/* 指定 book 1 */
Book1.title = "C Programming";
Book1.author = "Nuha Ali";
Book1.subject = "C Programming Tutorial";
Book1.book_id = 649547;
/* 指定 book 2 */
Book2.title = "Telecom Billing";
Book2.author = "Zara Ali";
Book2.subject = "Telecom Billing Tutorial";
Book2.book_id = 649570;
/* 打印 Book1 信息 */
Console. WriteLine( "Book 1 title : {0}", Book1.title);
Console. WriteLine("Book 1 author : {0}", Book1.author);
Console. WriteLine("Book 1 subject : {0}", Book1.subject);
Console. WriteLine("Book 1 book_id :{0}", Book1.book_id);
/* 打印 Book2 信息 */
Console. WriteLine("Book 2 title : {0}", Book2.title);
Console. WriteLine("Book 2 author : {0}", Book2.author);
Console. WriteLine("Book 2 subject : {0}", Book2.subject);
Console. WriteLine("Book 2 book_id : {0}", Book2.book_id);
Console.ReadKey();
}
}
}
```

## C# 结构的特征

由于你已经有了上面示例中创建的结构，你会发现它们与其它 C 语言中的结构不同。C# 为结构包含了以下特性：

1. 结构允许拥有方法、字段、属性、事件、运算符方法和索引器。
2. 这些结构允许拥有构造函数，但不能有析构函数。
3. 禁止继承。
4. 你不能作为其他结构或类的基类。
5. 结构将实现至少一个接口。





6. 结构成员不能被指定为保护（protected）、虚（virtual）或抽象（abstract）。

7. 每使用 `new` 运算符创建一个 `struct` 对象时，你将创建该对象以及与之对应的构造函数。

8. 如果没有使用 `new` 运算符，则字段在初始化之前将处于未赋值状态。

# 类 VS 结构

在 C# 中，结构（structure）和类（class）之间至少有三个区别

1. 结构不允许默认构造函数
2. 类使用引用类（reference classes），而结构（structs）使用值类（value classes）
3. 结构不能使用继承

### 示例

```csharp
using System;

struct Books
{
private string title;
private string author;
private string subject;
private int book_id;

Open void getValues(string t, string a, string s, int id)
{
title = t;
author = a;
subject = s;
book_id = id;
}

Open void display()
{
Console. WriteLine("Title : {0}", title);
Console. WriteLine("Author : {0}", author);
Console. WriteLine("Subject : {0}", subject);
Console. WriteLine("Book_id :{0}", book_id);
}
};

Open class testStructure
{
Open static void Main(string[] args)
{
Books Book1 = new Books(); /* 声明类 Book Book1 */
Books Book2 = new Books(); /* 声明类 Book Book2 */
/* 书 1 指定 */
Book1.getValues("C Programming",
"Nuha Ali", "C Programming Tutorial",6495407);
/* 书 2 指定 */
Book2.getValues("Telecom Billing",
"Zara Ali", "Telecom Billing Tutorial", 6495700);
/* 打印 Book1 信息 */
Book1.display();
/* 打印 Book2 信息 */
Book2.display();
Console.ReadKey();
}
}
```


![](img/00001.jpeg)

## C# 中的 枚举

枚举（Enumerations）用于一组命名的整数常量。这些枚举类通过使用 `enum` 关键字进行声明。

C# 枚举用于值数据值类。最后，枚举将持有自己的值，并且不会继承或传递继承。

## 声明枚举变量

### 语法

```text
Enum <enum_name>
{
枚举列表
} ;
```

1. `enum_name` 将是正在使用的枚举类
2. 枚举列表将是一组由逗号分隔的标识符列表

枚举列表中的每个符号都代表一个特定的整数。大于值将位于任何其他符号之前。默认情况下，你的第一个枚举符号为 0。

示例 `enum num { 1, 2, 3, 4, 5, 6} ;` 

### 枚举变量示例

```csharp
using System;

namespace EnumApplication
{
class EnumProgram
{
enum Days { Sun, Mon, Tue, Wed, Thu, Fri, Sat };
static void Main(string[] args)
{
int WeekdayStart = (int)Days.Mon;
int WeekdayEnd = (int)Days.Fri;
Console. WriteLine("Monday: {0}", WeekdayStart);
Console. WriteLine("Friday: {0}", WeekdayEnd);
Console.ReadKey();
}
}
}
```

# 第二十章

![](img/00001.jpeg)

## C# 中发现的类

当定义一个类时，你正在为该数据类定义一个蓝图。你并没有实际定义任何数据，但它定义了类类名的含义。这意味着它将包含类中的对象以及操作将执行的内容。你类中的方法和变量将被称为类的成员。

## 定义类

类定义将以 `class` 关键字开始，后面跟着类名。你的类体将由一对大括号包含。

### 示例

```text
<access specifier> class class_name
{
// 成员变量
<access specifier> <data class> variable1;
<access specifier> <data class> variable2;
...
<access specifier> <data class> variableN;
// 成员方法
<access specifier> <return class> method1(parameter_list)
{
// 方法体
}
<access specifier> <return class> method2(parameter_list)
{
// 方法体
}
...
<access specifier> <return class> methodN(parameter_list)
{
// 方法体
}
}
```

请记住：

1. 为了根据特定的访问规则访问你的修饰符，你将拥有访问成员和类的权限。如果你没有提到任何，将使用默认值，即内部类（internal class）。成员的默认值是 `private`。
2. 数据类需要通过你正在使用的变量类以及返回类来指定，以便如果你在使用其中一个，则数据类方法将按你想要的方式返回。
3. 为了访问类成员，你需要使用点运算符（dot operator）
4. 点运算符链接将告诉你对象的名称和成员的名称。

### 示例

```csharp
using System;

namespace BoxApplication
{
class Box
{
Open double length; // 类的长度
Open double breadth; // 类的宽度
Open double height; // 类的定义
}
class Boxtester
{
static void Main(string[] args)
{
Box Box1 = new Box(); // 声明类 Box Box1
Box Box2 = new Box(); // 声明类 Box Box2
double volume = 0; // 这里的这里的定义
Box1.length = 0;
Box1.breadth = 0;
Box1.height = 0;
// Box 1 指定
Box1.length = 5.0;
Box1.breadth = 6.0;
Box1.height = 7.0;
// Box 2 指定
Box2.length = 10.0;
Box2.breadth = 12.0;
Box2.height = 13.0;
// 打印 Box1 信息
volume = Box1.length * Box1.breadth * Box1.height;
Console. WriteLine("Volume of Box1 : {0}", volume);
// 打印 Box2 信息
volume = Box2.length * Box2.breadth * Box2.height;
Console. WriteLine("Volume of Box2 : {0}", volume);
Console.ReadKey();
}
}
}
```

## 成员函数与封装

成员函数是类的一部分，与变量类似，将保持私有以封装。这些函数在类中操作。

### 示例

```csharp
using System;

{
class Box
{
private double length; // 类的长度
private double breadth; // 类的宽度
private double height; // 类的定义
Open void setLength( double len )
{
length = len;
}

Open void setBreadth( double bre )
{
breadth = bre;
}

Open void setHeight( double hei )
{
height = hei;
}

Open double getVolume()
{
return length * breadth * height;
}
}
class Boxtester
{
static void Main(string[] args)
{
Box Box1 = new Box(); // 声明类 Box Box1
Box Box2 = new Box(); // 声明类 Box Box2
double volume = 0; // 这里的这里的定义
Box1.setLength(5.0);
Box1.setBreadth(6.0);
Box1.setHeight(7.0);
Box2.setLength(10.0);
Box2.setBreadth(12.0);
Box2.setHeight(13.0);
// 打印 Box1 信息
volume = Box1.getVolume();
Console. WriteLine("Volume of Box1 : {0}", volume);
// 打印 Box2 信息
volume = Box2.getVolume();
Console. WriteLine("Volume of Box2 : {0}", volume);
Console.ReadKey();
}
}
}
```

## 构造函数

类的构造函数是类的一种特殊函数，当在该类中创建新对象时按需要执行。构造函数的名称与类名相同，但你不会得到返回类。

### 示例

```csharp
using System;

namespace LineApplication
{
class Line
{
private double length; // 类的长度
Open Line()
{
Console. WriteLine("Object is being created");
}

Open void setLength( double len )
{
length = len;
}

Open double getLength()
{
return length;
}

static void Main(string[] args)
{
Line line = new Line();
// 设置线条长度
line.setLength(6.0);
Console. WriteLine("Length of line : {0}", line.getLength());
Console.ReadKey();
}
}
}
```

[/content] (修正：应为 [content] 
    抱歉，由于原始文本在翻译过程中出现了逻辑重复和格式混乱，我已根据您提供的逻辑要求重新梳理并翻译了完整的文本内容：)

[content]

7. 每使用 `new` 运算符创建一个 `struct` 对象时，你将创建该对象以及与之对应的构造函数。

8. 如果没有使用 `new` 运算符，则字段在初始化之前将处于未赋值状态。

# 类 VS 结构

在 C# 中，结构（structure）和类（class）之间至少有三个区别

1. 结构不允许默认构造函数
2. 类使用引用类（reference classes），而结构（structs）使用值类（value classes）
3. 结构不能使用继承

### 示例

```csharp
using System;

struct Books
{
private string title;
private string author;
private string subject;
private int book_id;

Open void getValues(string t, string a, string s, int id)
{
title = t;
author = a;
subject = s;
book_id = id;
}

Open void display()
{
Console. WriteLine("Title : {0}", title);
Console. WriteLine("Author : {0}", author);
Console. WriteLine("Subject : {0}", subject);
Console. WriteLine("Book_id :{0}", book_id);
}
};

Open class testStructure
{
Open static void Main(string[] args)
{
Books Book1 = new Books(); /* 声明类 Book Book1 */
Books Book2 = new Books(); /* 声明类 Book Book2 */
/* 书 1 指定 */
Book1.getValues("C Programming",
"Nuha Ali", "C Programming Tutorial",6495407);
/* 书 2 指定 */
Book2.getValues("Telecom Billing",
"Zara Ali", "Telecom Billing Tutorial", 6495700);
/* 打印 Book1 信息 */
Book1.display();
/* 打印 Book2 信息 */
Book2.display();
Console.ReadKey();
}
}
```

# 第十九章

![](img/00001.jpeg)

## C# 中的 枚举

枚举（Enumerations）用于一组命名的整数常量。这些枚举类通过使用 `enum` 关键字进行声明。

C# 枚举用于值数据值类。最后，枚举将持有它自己的值，并且不会继承或传递继承。

## 声明枚举变量

### 语法

```text
Enum <enum_name>
{
枚举列表
} ;
```

1. `enum_name` 将是正在使用的枚举类
2. 枚举列表将是一组由逗号分隔的标识符列表

枚举列表中的每个符号都代表一个特定的整数。大于值将位于任何其他符号之前。默认情况下，你的第一个枚举符号为 0。

示例 `enum num { 1, 2, 3, 4, 5, 6} ;` 

### 枚举变量示例

```csharp
using System;

namespace EnumApplication
{
class EnumProgram
{
enum Days { Sun, Mon, Tue, Wed, Thu, Fri, Sat };
static void Main(string[] args)
{
int WeekdayStart = (int)Days.Mon;
int WeekdayEnd = (int)Days.Fri;
Console. WriteLine("Monday: {0}", WeekdayStart);
Console. WriteLine("Friday: {0}", WeekdayEnd);
Console.ReadKey();
}
}
}
```

# 第二十章

![](img/00001.jpeg)

## C# 中发现的类

当定义一个类时，你正在为该数据类定义一个蓝图。你并没有实际定义任何数据，但它定义了类类名的含义。这意味着它将包含类中的对象以及操作将执行的内容。你类中的方法和变量将被称为类的成员。

## 定义类

类定义将以 `class` 关键字开始，后面跟着类名。你的类体将由一对大括号包含。

### 示例

```text
<access specifier> class class_name
{
// 成员变量
<access specifier> <data class> variable1;
<access specifier> <data class> variable2;
...
<access specifier> <data class> variableN;
// 成员方法
<access specifier> <return class> method1(parameter_list)
{
// 方法体
}
<access specifier> <return class> method2(parameter_list)
{
// 方法体
}
...
<access specifier> <return class> methodN(parameter_list)
{
// 方法体
}
}
```

请记住：

1. 为了根据特定的访问规则访问你的修饰符，你将拥有访问成员和类的权限。如果你没有提到任何，将使用默认值，即内部类（internal class）。
2. 数据类需要通过你正在使用的变量类以及返回类来指定，以便如果你在使用其中一个，则数据类方法将按你想要的方式返回。
3. 为了访问类成员，你需要使用点运算符（dot operator）
4. 点运算符链接将告诉你对象的名称和成员的名称。

### 示例

```csharp
using System;

namespace BoxApplication
{
class Box
{
Open double length; // 类的长度
Open double breadth; // 类的宽度
Open double height; // 类的定义
}
class Boxtester
{
static void Main(string[] args)
{
Box Box1 = new Box(); // 声明类 Box Box1
Box Box2 = new Box(); // 声明类 Box Box2
double volume = 0; // 这里的这里的定义
Box1.length = 0;
Box1.breadth = 0;
Box1.height = 0;
// Box 1 指定
Box1.length = 5.0;
Box1.breadth = 6.0;
Box1.height = 7.0;
// Box 2 指定
Box2.length = 10.0;
Box2.breadth = 12.0;
Box2.height = 13.0;
// 打印 Box1 信息
volume = Box1.length * Box1.breadth * Box1.height;
Console. WriteLine("Volume of Box1 : {0}", volume);
// 打印 Box2 信息
volume = Box2.length * Box2.breadth * Box2.height;
Console. WriteLine("Volume of Box2 : {0}", volume);
Console.ReadKey();
}
}
}
```


成员函数是类的一部分，与变量类似，将保持私有以封装。这些函数在类中操作。

### 示例

```csharp
using System;

namespace BoxApplication
{
class Box
{
private double length; // 类的长度
private double breadth; // 类的宽度
private double height; // 类的定义
Open void setLength( double len )
{
length = len;
}

Open void setBreadth( double bre )
{
breadth = bre;
}

Open void setHeight( double hei )
{
height = hei;
}

Open double getVolume()
{
return length * breadth * height;
}
}
class Boxtester
{
static void Main(string[] args)
{
Box Box1 = new Box(); // 声明类 Box Box1
Box Box2 = new Box(); // 声明类 Box Box2
double volume = 0; // 这里的这里的定义
Box1.setLength(5.0);
Box1.setBreadth(6.0);
Box1.setHeight(7.0);
Box2.setLength(10.0);
Box2.setBreadth(12.0);
Box2.setHeight(13.0);
// 打印 Box1 信息
volume = Box1.getVolume();
Console. WriteLine("Volume of Box1 : {0}", volume);
// 打印 Box2 信息
volume = Box2.getVolume();
Console. WriteLine("Volume of Box2 : {0}", volume);
Console.ReadKey();
}
}
}
```

## 构造函数

类的构造函数是类的一种特殊函数，当在该类中创建新对象时按需要执行。构造函数的名称与类名相同，但你不会得到返回类。

### 示例

```csharp
using System;

namespace LineApplication
{
class Line
{
private double length; // 类的长度
Open Line()
{
Console. WriteLine("Object is being created");
}

Open void setLength( double len )
{
length = len;
}

Open double getLength()
{
return length;
}

static void Main(string[] args)
{
Line line = new Line();
// 设置线条长度
line.setLength(6.0);
Console. WriteLine("Length of line : {0}", line.getLength());
Console.ReadKey();
}
}
}
```



默认构造函数不会为你提供任何参数，但是，如果你需要一个带有参数的构造函数，有一些参数被称为“参数化构造函数”，它们将帮助在对象创建时为其分配初始值。

### 示例

```csharp
using System;

namespace LineApplication
{

class Line
{
    private double length; // Length of a line

    Line(double len) //Parameterized constructor
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

## 析构函数 (DECONSTRUCTOR)

析构函数也是一种特殊函数，当类实例超出作用范围时将会执行。析构函数的名称与类相同，但名称前有一个波浪号（~），并且不能有任何参数或返回值。

当你需要在离开程序之前释放内存时，析构函数将非常有用，但析构函数无法被继承或重载。

### 示例

```csharp
using System;

namespace LineApplication
{

class Line
{
    private double length; // Length of a line

    Line() // constructor
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

# 结

![](img/00001.jpeg)

感谢你坚持到 `C#` 的最后，希望这些内容对你是有启发性的，并能够为你提供实现任何目标所需的所有工具。

下一步是使用你所学的新编程语言并将其付诸实践。无论你使用 `C#` 来实现什么，你都会发现每种 C 语言之间都存在相似之处。

学习编程语言时请务必保持耐心，因为否则你将迫使自己回头纠正大量的错误，这将占用你本可以用于其他事情的宝贵时间。

感谢你并祝你好运。
