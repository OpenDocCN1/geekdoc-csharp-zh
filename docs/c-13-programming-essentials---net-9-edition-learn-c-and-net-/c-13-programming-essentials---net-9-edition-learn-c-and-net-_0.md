# C# 13 编程精要 - .NET 9 版：使用 Visual Studio Code 学习 C# 和 .NET 9 编程



![](img/cover.png)

![](img/image-UZ10XDHW.jpg)


## 核心基础

### .NET 9 版本









![](img/image-CK9IWB0Z.png)


        carManufacturer = "Toyota";
        goto default;
    default:
        Console.WriteLine($"The {carModel} is manufactured by {carManufacturer}");
        break;
}
```

虽然 `goto` 语句也可以跳转到 C# 代码中的标记位置，但强烈建议不要以这种方式使用它。上述用法是像 C# 这样的现代面向对象语言中 `goto` 语句唯一可接受用法。正如任何资深程序员都会告诉你的那样，如果你发现自己处于只有 `goto` 语句才能实现目标的境地，你需要重新思考并重构你的代码，以便你不再需要 `goto`。

# 10.7 在 C# switch 语句中使用 continue

`break` 语句的另一种替代方案是 `continue` 语句。假设 `switch` 语句循环的一部分。在这种情况下，`continue` 语句将导致执行立即返回循环开头，跳过当前循环迭代中任何尚未执行的后续代码。

在循环中使用 `continue` 语句将在“C# 中使用 for 语句循环”章节中介绍。

# 10.8 知识测试

点击下方的链接或扫描二维码来测试你对 C# `switch` 语句的知识和理解：

[`www.answertopia.com/k4uy`](https://www.answertopia.com/k4uy)

![](img/image-04YSW843.jpg)

# 10.9 总结

当只有少数可能的结果时，`if-else` 语句是做出决策的可靠方法。然而，当评估产生许多潜在结果时，这种方法可能会变得繁琐。在这种情况下，`switch` 语句是 C# 中实现流控制逻辑的更好选择。在许多情况下，可以使用 `switch` 表达式进一步简化 `switch` 语句。

# 11 使用 for 语句循环

本章将继续介绍 `for` 语句。

## 11.1 为什么需要循环？

计算机通常擅长重复性任务。如果你需要执行此操作 100 次甚至 10,000 次会发生什么？编写 C# 代码将是不可接受的。

`for` 循环的语法如下：

```csharp
for (initializer; conditional expression; loop expression)
```

`initializer` 初始化计数器变量。例如，将其设置为零。

`conditional expression` 指定用于测试，以验证循环是否已执行了所需的迭代次数。例如，如果我们想循环 100 次：

`loop expression` 指定在计数器上执行的操作。例如，递加 1：

循环每次迭代中要执行的语句体包含在由左大括号 `{` 和右大括号 `}` 定义的代码块中。通过将所有这些整合在一起，我们可以创建一个 for 循环来执行前面示例中概述的任务：

```csharp
long j = 1;
for (int i=0; i<50; i++) {
    j += j;
}
Console.WriteLine("j = " + j);
```

## 11.2 C#

### 循环作用域

创建循环的一个关键点是，循环内部定义的任何变量对循环内部的代码可见。这种概念被称为作用域（scope）。例如，如果在 `for` 循环体内定义了变量 `myCounter`，则该变量在循环终止后将消失：

```csharp
//变量 myCounter 尚未存在
for (int i = 0; i < 10; i++)
{
    int myCounter = 0; //myCounter 在 for 循环的作用域内
    myCounter += i;
}

// 循环结束后 myCounter 超出作用域并消失
```

## 11.3 创建无限 for 循环

可以使用 `for(;;)` 语法构建无限执行的 for 循环。例如，下面的代码将在用户手动终止程序（或关闭或重启计算机）之前，持续输出“Hello from C#”：

```csharp
for (;;)
{
    Console.WriteLine("Hello from C#");
}
```

如果你在 VS Code 中尝试上面的示例并发现陷入了无限循环，可以使用图 11-1 所示的停止按钮停止执行：

![](img/image-WYUHYY24.png)

图 11-1

## 11.4 跳出 for 循环





在创建一个循环后，你可能想在满足完成标准之前，在某些条件下跳出循环（特别是当你创建了无限循环时）。其中一个示例可能涉及持续检查网络套字上的活动。一旦检测到活动，就需要跳出监控循环并执行某些其他任务。

为了跳出循环，C# 提供了 `break` 语句，它可以跳出当前循环并从循环紧后的代码处恢复继续执行。例如：

```csharp
int j = 10;

for (int i = 0; i < 50; i++)
{
    j += j;
    Console.WriteLine("j = " + j);
    if (j > 100)
        break;
}
```

在上面的示例中，循环将继续执行，直到 `j` 的值超过 100，在那个时间点上，循环将退出。

## 11.5 嵌套 for 循环

到目前为止，我们只查看了单层 `for` 循环。也可以嵌套 `for` 循环，即让循环位于另一个循环内部。例如：

```csharp
for (int i = 0; i < 100; i++) {
    Console.WriteLine( "i = " + i);
    for (int j = 0; j < 10; j++) {
        Console.WriteLine( "j = " + j);
    }
}
```

上面的示例将循环 100 次，在每次迭代中显示 `i` 的值。此外，这些迭代中的每一次都将循环 10 次，显示 `j` 的值。

上面的示例显示了两个层嵌套。当然，也可以嵌套更多层级，但层数过多可能会导致代码难以理解。

## 11.6 从嵌套循环中退出

在跳出嵌套 `for` 循环时，需要注意的一个重要点是，`break` 只退出当前层级的循环。例如，下面的 C# 代码示例将在 `j` 等于 5 时退出嵌套循环的当前迭代。然而，外层循环将继续迭代，并反而执行嵌套循环：

```csharp
for (int i = 0; i < 100; i++) {
    Console.WriteLine( "i = " + i);
    for (int j = 0; j < 10; j++) {
        if (j == 5)
            break;
        Console.WriteLine( "j = " + j);
    }
}
```

## 11.7 继续 for 循环

循环中使用的的另一个有用语句是 `continue` 语句。当执行过程在任何循环中找到 `continue` 语句时，它会跳过循环体中所有的剩余代码，并从循环顶部重新开始执行。使用这种技术，我们可以例如构造一个 `for` 循环，只输出 1 到 9 之间的偶数：

```csharp
for (int i = 1; i < 10; i++) {
    if ((i % 2) != 0)
        continue;
    Console.WriteLine($"i = {i}");
}
```

在示例中，如果 `i` 不能被 2 整除且余数为 0，代码将执行 `continue` 操作，将执行发送到 `for` 循环的顶部，从而绕过输出 `i` 值的代码。这导致控制台中只出现偶数。

## 11.8 C# foreach 语句

`foreach` 循环用于迭代集合中的项序列，并提供了一个简单易用的循环选项。

`foreach` 循环的语法如下：

```csharp
foreach <name> in <collection> {
    // 要执行的代码
}
```

在此语法中，`<name>` 是一个常量的名称，该常量包含循环正在迭代的对象中的当前项。循环体中的代码通常会使用此常量名称来引用循环周期中的当前项。`<collection>` 是循环正在迭代的对象。例如，它可以是一个字符串或或数值的数组（集合的主题将在名为“在 C# 中创建 2D、3D 和交错数组”的章节中进行更详细介绍）。

例如，考虑以下 `foreach` 循环结构：

```csharp
string[] myColors = ["red", "green", "yellow", "orange", "blue"];

foreach (string color in myColors)
{
    Console.WriteLine("{0} ", color);
}
```

循环开始时声明当前项将被赋值给一个名为 `color` 的常量。然后我们告诉该语句，它将遍历 `myColors` 集合中的所有元素。循环体向控制面板发送一条消息，指示分配给 `color` 常量的当前值。

正如我们在“在 C# 中创建 2D、3D 和交错数组”章节中看到的，在处理数组和字典等集合时，`foreach` 循环特别特别有益。

## 11.9 接受知识测试

点击下面的链接或扫描二维码，以测试你对 C# 循环的知识和理解：

[`www.answertopia.com/3xzv`](https://www.answertopia.com/3xzv)

![](img/image-SICUB2IT.jpg)

## 11.10 总结

循环控制流是大多数编程语言中发现的一种基础功能。在本章中，我们涵盖了用于多次执行任务的 `for` 和 `foreach` 语句，并探讨了嵌套循环以及如何使用 `break` 和 `continue` 语句管理循环行为。

# 12. 使用 do 和 while 进行 C# 循环

在构造循环的主题上，本章旨在引入两种更多的循环选项：`while` 和 `do...while`。

`for` 循环在预先知道任务需要重复多少次时运行良好。然而，在某些情况下，代码需要重复直到满足特定条件，而不知道重复次数。C# 提供了方案。

## 12.1 while 循环

本质上，`while` 循环重复一组任务直到满足特定条件。`while` 循环的定义如下：

```csharp
while (condition) {
    // 语句
}
```

在上面的示例中，`condition` 是一个返回真或假的表达式，`statements` 代表当条件持续为真时执行的代码。例如：

```csharp
int myCount = 0;

while (myCount < 100) {
    myCount++;
}

Console.WriteLine($"myCount = {myCount}");
```

在上面的示例中，`while` 评估 `myCount` 是否小于 100。如果它已经大于 100，括号中的代码将被跳过，循环将在未执行任何任务的情况下退出。

另一方面，如果 `myCount` 不大于 100，括号中的代码将执行，循环返回 `while` 语句并重复评估。此过程将重复，直到 `myCount` 的值超过 100，在那个时间点循环将退出。

## 12.2 do... while 循环

将 `do...while` 循环类比为反的 `while` 循环通常帮助。`while` 循环在执行循环体代码之前评估表达式。如果表达式在第一次检查时为假，则不执行代码。另一方面，`do...while` 循环适用于知道循环体中的代码至少需要执行一次的情况。例如，你可能想继续遍历数组中的项，直到找到特定的项。你知道你至少必须检查数组中的第一个项才有希望找到所需的条目。`do...while` 循环的语法如下：

```csharp
do {
    // 语句
} while (conditional expression);
```

在下面的 `do...while` 示例中，循环将持续直到名为 `i` 的变量值等于 0：

```csharp
int i = 10;

do {
    i--;
    Console.WriteLine($"i = {i}");
} while (i > 0);
```




与 `for` 循环一样，也可以使用 `break` 语句随时退出 `while` 或 `do ... while` 循环。当执行路径遇到 `while` 语句时，循环将停止，执行将继续到紧随循环后的代码。在接下来的示例中，循环被设置为当 `i` 的值匹配 `j` 的值时退出：

```sharp
int i = 0;

int j = 5;

while (i < 100)
{
    i++;
    Console.WriteLine($"i = {i}");
    if (i == j)
        break;
}
```

与跳出 `for` 循环一样，必须注意的是，在嵌套的 `while` 和 `do ... while` 循环情况下，`while` 语句只会退出当前循环，让外层循环继续执行（并且极可能再次执行内层循环）。

## 12.4 `continue` 语句

`continue` 语句会跳过循环中剩余的所有代码语句，并将执行返回到循环顶部。

在接下来的示例中，只有当变量 `i` 的值为偶数时（即能被 2 整除且无余数），才会调用 `WriteLine()` 方法：

```sharp
int i = 1;

while (i < 20) {
    i++;
    if ((i % 2) != 0)
        continue;
    Console.WriteLine("i = " + i);
}
```

上述示例中的 `continue` 语句除非 `i` 的值能被 2 无余整除，否则将跳过 `WriteLine()` 调用。如果触发了 `continue` 语句，执行将跳转到 `while` 循环顶部，循环体中的语句将重复（直到 `i` 的值超过 19）。

## 12.5 知识测试

点击下方链接或扫描二维码以测试你对 C# `do-while` 循环的知识和理解：

[`www.answertopia.com/t2ji`](https://www.answertopia.com/t2ji)

![](img/image-OJBJDMFY.jpg)

## 12.6 总结

C# 的 `do` 和 `while` 语句是多功能工具，用于重复执行某项任务直到满足特定条件，例如算术运算达到预期结果或数据到达网络端口。当独立使用时，`while` 循环在执行第一次循环迭代之前会检查条件是否已满足，从而允许完全跳过循环。另一方面，`do ... while` 循环在你知道在满足完成标准之前至少需要执行一次循环代码时非常有帮助。这两种循环都支持 `break` 和 `continue` 语句。

# 13. C# 面向对象编程简介

到课程为止，我们已经学习了 C# 编程的基础知识，例如变量类型和控制流。虽然使用这些技术编写功能性程序是可能的，但要成为一名精通的 C# 程序员还有很多工作要做。C# 首先是一种面向对象的编程语言，因此，任何 C# 程序员都被期望使用这种语言创建面向对象的应用程序。

C# 为开发面向对象的应用程序提供了广泛支持。本章将介绍涉及面向对象编程的基本概念，然后解释与使用 C# 进行应用程序开发相关的概念。

## 13.1 什么是对象？

对象是一个自包含的功能模块，可以作为软件应用程序的构建块被易使用和重用。

对象由数据变量（属性）和函数（方法）组成，可以在对象上进行访问和调用以执行任务。这些被统称为成员。

## 13.2 什么是类？

类就像蓝图或建筑师的图纸，描述了对象在创建时的样子。它定义了对象将拥有的方法和将包含的变量。本质上，类决定了对象的属性和行为。

## 13.3 创建 ObjectDemo 项目

启动 VS Code，并打开你的“C# Essentials”工作区文件夹。按下 `Cmd-Shift-P` 显示命令面板并选择 `.NET: New Project...` 命令，如下所示：

![](img/image-XUZJO9EB.png)

图 13-1

从模板列表中选择 `Console App` 选项，在提示时将项目命名为 `ObjectDemo`，然后按 `Enter` 键确认选择：

![](img/image-NI13RAGJ.png)

图 13-2

接受默认的工作区文件夹，以及创建新项目的选项：

![](img/image-0CPU1ABO.png)

图 13-3

从操作栏中选择 `Explorer` 选项（在下方图 13-4 中标记为 A），并确认 `ObjectDemo` 项目现在列在工作区文件夹中 (B)：

![](img/image-R4Z29Z9K.png)

图 13-4

## 13.4 声明 C# 类

在实例化对象之前，我们首先需要为对象定义类蓝图。在本章中，我们将创建一个 `Bank Account` 类来演示 C# 面向对象编程的概念。第一步是使用解决方案管理器（Solution Explorer）向我们的项目添加一个新的类文件。解决方案管理器位于资源管理器的底部，如图 13-5 所示：

![](img/image-RYAR6DW.png)

图 13-5

在解决方案管理器中，将鼠标指针悬停在 `ObjectDemo` 条目上以显示文件文件夹按钮：

![](img/image-YCW7Z4.png)

图 13-6

点击 `New File...` 按钮将显示调面板，如图 13-7 所示：

![](img/image-3CN0NA.png)

图 13-7

选择 `Class` 选项，并在按下 `Enter` 创建文件将类命名为 `BankAccount`。新文件将自动加载到编辑器，内容如下：

```csharp
using System;

namespace ObjectDemo;

public class BankAccount
{

}
```

## 13.5 访问修饰符

当 VS Code 生成我们的 `BankAccount` 类时，它是使用 `public` 访问修饰符声明的。访问修饰符控制是否可以在其他地方访问，并适用于多种类型，包括类、方法、属性和字段。C# 支持以下访问修饰符：

- `public`：无访问限制。
- `protected`：仅对类及其派生类可用。
- `private`：仅对包含类内部可用。
- `file`：仅对包含源文件可用。
- `internal`：仅对当前程序集（通常是编译该类的可执行文件或库）中的代码可用。
- `protected internal`：对当前程序集中的代码或类的派生类可用。
- `private protected`：仅对包含类或当前程序集内的派生类可用。

## 13.6 创建 C# 类成员

类成员、字段或属性上是嵌入类中的变量和方法（方法的概念在本章稍后讨论）。成员可以是 `public`、`private` 或 `protected`。

`public` 成员可以从对象外部访问并在派生类中可见。`private` 成员仅可由类内部的方法访问，对派生类不可见。`protected` 类仅对派生类可用。

这是数据封装的关键。面向对象的编程规定数据应该封装在类中，并通过类的方法（通常称为 getter 和 setter）进行访问和设置。

## 13.7 字段与属性

直接声明为变量的类成员被称为字段。例如，在下面的类中，`firstname` 变量被声明为字段：

```csharp
public class MyClass {
    public string firstname = ""; // 这是一个字段
}
```



[content]

然而，面向对象的编程指南建议字段应该被保护免受直接访问（即私有字段）。在 C# 中，这通过声明属性来实现，属性反过来提供了对底层私有字段的访问。

属性有一个名称，并声明了特殊的 `get` 和 `set` 方法（称为访问器方法），这些方法使用以下语法提供对底层字段的访问：

```csharp
public string <property name="">{</property>
    get {
        return <field name="">;</field>
    }
    set {
        <field name="">= value;</field>
    }
}
```

`get` 方法的代码返回赋值给字段的值。而 `set` 方法传递名为 `value` 的变量，该变量可以被赋值给字段。

使用这种方法，我们现在可以实现一个属性来封装我们的 `firstname` 字段：

```csharp
public class MyClass
{
    private string _firstname = "";
    public string FirstName {
        get {
            return _firstname;
        }
        set {
            _firstname = value;
        }
    }
}
```

当字段与属性关联时，该字段应声明为私有，并且名称通常以下划线 (`_`) 为前缀。

声明访问器的更简洁的方法是使用 lambda 运算符 (`=>`) 来为 get 和 set 表达式赋值（Lambda 主题将在“C# 匿名方法、Lambdas 和本地函数”章节中介绍）：

```csharp
public string <property name="">{</property>
    get => <field name="">;</field>
    set => <field name="">= value;</field>
}
```

使用上述方法，我们可以如下所示简化我们的 `MyClass` 示例：

```csharp
public class MyClass
{
    private string _firstname = "";
    public string FirstName {
        get => _firstname;
        set => _firstname = value;
    }
}
```

是否将所有字段封装在属性中且不设置任何公共字段，取决于个人偏好，取决于你想要在多大程度上严格遵守面向对象的编程规范。即使在微软的 C# 参考文档中，你也会看到这两种方法的示例。为了简洁起见，我们在书中的许多示例将使用公共字段。

## 13.8 为 BankAccount 类添加成员

我们现在可以扩展 `BankAccount` 类，添加字段来存储账户名称和账号。遵循数据封装的理念，我们将这些字段设为私有，并使用属性提供访问：

```csharp
namespace ObjectDemo;

public class BankAccount
{
    private string _accountName = "";
    private int _accountNumber = 0;
    public string AccountName
    {
        get => _accountName;
        set => _accountName = value;
    }
    public int AccountNumber
    {
        get => _accountNumber;
        set => _accountNumber = value;
    }
}
```

在类中添加了一些字段和属性后，我们需要简要检查其他数据成员类型，并学习如何从类创建对象实例。

## 13.9 静态、只读和常量数据成员

除了我们目前看到的数据成员类型外，C# 还支持几种额外的成员类型。

C# 静态成员类型（也称为类属性）存储该类所有对象实例共的数据值。例如，所有银行客户在储蓄账户上获得的利率相同。因此，`interestRate` 成员应声明为静态，因为它是该类所有对象实例共享的。静态成员使用 `static` 关键字声明。例如：

```csharp
public class BankAccount
{
    private static int interestRate;
}
```

静态成员通过类进行访问，而不是通过对象。例如，我们可以通过如下方式引用 `BankAccount` 类来更改所有对象实例的 `interestRate` 成员：

`BankAccount.interestRate = 10;`

对于不能修改的数据成员，使用了 `const` 和 `readonly` 关键字。

## 13.10 从类实例化对象

现在我们已经了如何编写类，需要知道如何从类中创建对象。从类创建对象被称为实例化。第一步是使用 `new` 关键字创建实例：

```csharp
BankAccount accountAccount = new BankAccount();
```

或者，可以在单条语句中声明对象并对其进行初始化：

```csharp
BankAccount accountAccount = new BankAccount();
```

也可以如下所示声明对象变量并为其赋值：

```csharp
using ObjectDemo;
BankAccount accountAccount = new BankAccount();
accountAccount.AccountName = "John Smith";
accountAccount.AccountNumber = 53211;

Console.WriteLine($"Customer Name is {accountAccount.AccountName}");
Console.WriteLine($"Account Number = {accountAccount.AccountNumber}");
```

当属性在对象创建后立即初始化时，可以使用对象初始化器将代码简化如下：

```csharp
BankAccount accountAccount = new()
{
    AccountName = "John Smith",
    AccountNumber = 53211
};
```

## 13.11 访问对象成员

现在我们有了一个 `BankAccount` 类的实例，需要知道如何访问它的成员。首先，你会记得我们将某些成员声明为公共，而另一些声明为私有。公共成员可以使用所谓的“点符号法”（dot notation）从对象外部完全访问。

点符号法是一种通过指定对象和用点 (`.`) 分隔的名称来访问对象的机制。例如，访问名为 `accountAccount` 的对象的 `accountName` 成员，我们将使用 `accountAccount.AccountName`。

修改 `Program.cs` 文件如下，以访问 `BankAccount` 类的公共属性：

```csharp
BankAccount accountAccount = new();
accountAccount.AccountName = "John Smith";
accountAccount.AccountNumber = 53211;

Console.WriteLine($"Customer Name is {accountAccount.AccountName}");
Console.WriteLine($"Account Number = {accountAccount.AccountNumber}");
```

运行应用并检查输出如下：

```
Customer Name is John Smith
Account Number = 53211
```

## 13.12 为 C# 类添加方法

类方法本质上是可以在类上下文中调用的以执行特定任务的代码例程。方法有两种形式：静态方法（也称为类方法）和实例方法。静态方法在类级别操作，例如创建新的类实例。相反，实例方法仅对类的实例操作（例如，对成员变量进行算术运算并返回结果）。

实例方法在所属类的左大右括号内部声明，并使用标准的 C# 方法语法声明。静态方法的声明方式与实例方法相同，只是 `static` 关键字位于声明。

例如，编辑 `BankAccount` 类并添加一个显示名称的方法：

```csharp
public class BankAccount
{
    // ... 现有的字段和属性 ...
    public void DisplayName()
    {
        Console.WriteLine(AccountName);
    }
}
```




```csharp
public void DisplayName()
{
    Console.WriteLine($"Customer name is {AccountName}");
}
```

上面的方法是一个实例方法，因此它前面没有 `static` 关键字，并且可以按照如下方式调用：

```csharp
BankAccount custAccount = new()
{
    AccountName = "John Smith",
    AccountNumber = 53211
};

custAccount.DisplayName();
Console.WriteLine($"Account Number = {custAccount.AccountNumber}");
```

在设计 `BankAccount` 类时，调用类本身的 `static` 方法来识别该类实例可以存储的最大允许余额可能会很有帮助。这将允许应用程序在不创建类实例的情况下识别 `BankAccount` 类是否适合存储新客户的详情。我们将此方法命名为 `GetMaxBalance()` 并对其所示实现：

```csharp
public class BankAccount 
{
    public static double GetMaxBalance()
    {
        return(10000000.00);
    }
}
```

声明方法后，可以直接在类上调用它，而无需创建实例，如下所示：

```csharp
double maxBalance = BankAccount.GetMaxBalance();
Console.WriteLine($"Maximum allowed balance = ${maxBalance}");
BankAccount custAccount = new()
```

运行该程序应该产生以下输出：

```
Maximum allowed balance = $10000000
Customer name is John Smith
Account Number = 53211
```

现在我们已经查看了方法的类成员，下一个任务是查看两个特殊的类方法：构造函数和析构函数。

## 13.13 C# 构造函数

尽管名称听起来很大气，但 C# 类构造函数和析构函数只不过是在对象被实例化和销毁时调用的方法。构造函数特别用于允许在创建时将初始化值传递给对象。假设我们希望在初始化 `custAccount` 对象时初始化 `_accountName` 和 `_accountNumber` 成员。为了实现这一点，我们需要声明一个构造函数。

构造函数的声明方式与其他方法相同，不同之处方法方法必须与类名匹配。例如，如下所示为 `BankAccount` 类添加一个构造函数：

```csharp
public class BankAccount
{
    private string _accountName;
    private int _accountNumber;
    // 构造函数
    public BankAccount(string accountName, int accountNumber)
    {
        _accountName = accountName;
        _accountNumber = accountNumber;
    }
}
```

构造函数可以用于在创建实例时初始化这些成员：

```csharp
BankAccount custAccount = new BankAccount("Fred Wilson", 123456);
custAccount.DisplayName();
```

当需要在为属性赋值之外执行某些任务时，上述构造函数类型特别有用。例如，`BankAccount` 构造函数可能包含一些逻辑来捕获空的客户名称字符串：

```csharp
public BankAccount(string accountName, int accountNumber)
{
    if (accountName == "")
        _accountName = "Anonymous";
    else
        _accountName = accountName;
    _accountNumber = accountNumber;
}
```

一个类可以包含多个构造函数，每个构造函数有一组唯一的参数。考虑对 `BankAccount` 类定义的以下更改：

```csharp
public class BankAccount
{
    private string _accountName;
    private int _accountNumber;
    private bool _isActive = false;
    // 构造函数
    public BankAccount(string accountName, int accountNumber)
    {
        _accountName = accountName;
        _accountNumber = accountNumber;
    }
    public BankAccount(string accountName, int accountNumber, bool isActive)
    {
        _accountName = accountName;
        _accountNumber = accountNumber;
        _isActive = isActive;
    }
    public bool IsActive {
        get => _isActive;
    }
}
```

通过这些更改，可以使用以下方式创建 `BankAccount` 实例：

```csharp
BankAccount custAccount = new("John Smith", 53211);
BankAccount cust2 = new("John Smith", 53211, true);
```

## 13.14 C# 主构造函数

当构造函数的唯一目的是将参数分配类时，建议使用主构造函数。例如，将参数放在类名之后：

```csharp
public class BankAccount(string accountName, int accountNumber)
{
    private string _accountName = accountName;
    private int _accountNumber = accountNumber;
}
```

## 13.15 C# 析构函数

析构函数用于在对象销毁时清理类使用的任何资源。与可以使用 `new` 关键字显式调用的构造函数不同，没有办法可以调用析构函数。它们的定义方式与构造函数相同，不同之处是名称前面有一个波浪号 (`~`）：

```csharp
// 析构函数
~BankAccount() {
}
```

## 13.16 “this” 关键字

在 C# 中构造类时，你可能会遇到某些情况：方法内部局部属性与类属性冲突。这在在使用公共字段时特别常见。例如，下面的示例类，其中参数名称与公共字段匹配：

```csharp
class DemoClass
{
    public string name;
    public int age;
    public DemoClass(string name, int age)
    {
        name = name;
        age = age;
    }
}
```

当运行上述代码时，将没有名称且年龄将为 0，即使在创建类实例时已将年龄设置为 37。

```csharp
DemoClass demo = new("Mark", 37);
Console.WriteLine($"{demo.name} is {demo.age} years old.");
```

此外，编译器会发出警告，内容为：`warning CS1717: 赋值给了同一个变量；你是否是想赋值其他内容?` 这里的问题是编译器不知道在以下初始化代码中引用的是哪个 `name` 和 `age` 变量：

```csharp
public DemoClass(string name, int age) {
    name = name;
    age = age;
}
```

为了解决这个问题，我们需要能够告诉编译器将方法参数值分配给相应的公共字段值。我们可以使用 `this` 关键字来实现。在此范围内，`this` 关键字表示当前的类实例。为了区分冲突的 `name` 和 `age` 变量，我们需要如下使用 `this` 关键字：

```csharp
public DemoClass(string name, int age) {
    this.name = name;
    this.age = age;
}
```

## 13.17 进行知识测试

点击下方链接或扫描二维码测试你对 C# 面对象编程的知识和理解：

[`www.answertopia.com/cnbw`](https://www.answertopia.com/cnbw)




面向对象的编程语言如 `C#` 促进了类的创建，以鼓励代码重用和数据封装。在本章中，我们涵盖了 `C#` 中类和实例的基本概念，并解释了类成员、构造函数、终结器、属性、字段和方法等概念。

# 14. C# 方法

上一章开始介绍 `C#` 中的面向对象编程，并包含了在类内部声明的方法的使用。本章将更详细地探讨 `C#` 方法，包括如何声明和调用它们、传递参数以及返回结果。还将解释通过引用和值传递参数的主题。

C# 方法对于编写结构良好且高效的代码至关重要。它们提供了一种组织程序的方法，同时避免了代码重复。在本章中，我们将研究如何在 `C#` 中声明和使用方法。

## 14.1 什么是方法？

方法是一个具命名的代码块，可以通过调用它来执行特定任务。它可以接收数据以执行该任务，并向结果返回给调用它的代码。例如，如果 `C#` 程序中需要执行特定的算术计算，可以将执行该算术的代码放置在方法中。该方法可以设置为接受要进行算术计算的值（称为参数）并返回计算结果。在程序代码中需要计算的任何点，都可以调用该方法并将值作为参数传递，然后返回结果。

## 14.2 方法与函数

如果你熟悉其他编程语言，可能听过或使用过函数。通常情况下，函数的声明方式与方法相同，目的也相同。区别在于，方法必须在类内部声明，而函数则在类外部声明。在 `C#` 中，只能在类内部声明方法，不存在函数的概念。

## 14.3 参数还是实参？

在讨论方法时，`parameter`（参数）和 `argument`（参数）这两个术语通常互换使用。然而，它们之间存在细微的。方法在被调用时可以接收的值被称为 `parameters`（参数）。当方法被调用并传递这些值时，它们被称为 `arguments`（参数）。

## 14.4 如何声明 C# 函数

`C#` 函数使用以下语法声明：

```
<access><return type=""><method name="">(<para type="">, <para name="">, ...){
    // 方法代码
}
```

函数声明各个各个字段的解释如下：

- `<access>`：定义了从代码其他部分访问方法的访问级别。有效值为 `public`、`private` 或 `protected`，如上一章所解释的。
- `<return type>`：函数返回的结果的数据类型。如果函数不返回结果，则将其设置为 `void`。
- `<method name>`：分配给方法的名称。这是在应用程序代码内部调用方法时引用该方法的名称。
- `<para type>`：对应 `parameter`（参数）的类型。
- `<para name>`：在方法代码中引用该 `parameter`（参数）的名称。
- `Method code`：执行工作的方法代码语句。

例如，以下方法不接受参数，不返回结果，并显示一条消息：

```csharp
public void sayHello() {
    Console.WriteLine("Hello");
}
```

相反，下面的示例函数接受一个 `int` 和一个 `string` 作为参数，并返回一个字符串结果：

```csharp
public string BuildMessage(string name, int count) {
    return($"{name}, you are customer number {count}");
}
```

## 14.5 创建 MethodDemo 项目

启动 VS Code，打开你的“C# Essentials”工作空间文件夹，并创建一个名为 `MethodDemo` 的新 .NET 控制台应用程序。

## 14.6 声明 C# 类文件

遵循“C# 面向对象编程简介”章节中的步骤，使用解决方案管理器（Solutions Explorer）向 `MethodDemo` 项目添加一个名为 `Demo` 的新类文件。添加类文件后，按照如下方式对其进行修改以添加方法：

```csharp
using System;

namespace MethodDemo;

public class Demo
{
    public void SayHello()
    {
        Console.WriteLine("Hello");
    }
}
```

## 14.7 调用 C# 方法

一旦声明，就可以使用点符号通过以下语法在类实例上调用 `C#` 方法：

```
<instance>.<function name>(<arg1>, <arg2>, ... )
```

传递给方法的每个参数必须匹配方法配置为接受的参数。例如，要调用上述名为 `SayHello()` 的不接受参数且不返回值的示例方法，我们需要如下所示修改 `Program.cs` 文件：

```csharp
using MethodDemo;

Demo demo = new();

demo.SayHello();
```

当应用运行时，“Hello”消息将出现在终端中。

## 14.8 处理返回值

`SayHello()` 方法定义包含了 `void` 关键字，表示它不返回结果值。接下来，在 `Demo` 类中添加一个名为 `BuildMessage()` 的方法，它接受两个参数并返回字符串结果如下：

```csharp
public class Demo
{
    public void SayHello()
    {
        Console.WriteLine("Hello");
    }

    public string BuildMessage(string name, int count)
    {
        return($"{name}, you are customer number {count}");
    }
}
```

`SayHello()` 方法定义包含了 `void` 关键字，表示它不返回结果值。接下来，在 `Demo` 类中添加一个名为 `BuildMessage()` 的方法，它接受两个参数并返回字符串结果如下：

```csharp
public class Demo
{
    public void SayHello()
    {
        Console.WriteLine("Hello");
    }

    public string BuildMessage(string name, int count)
    {
        return $"{name}, you are customer number {count}";
    }
}
```
（注：此处原文文本似乎有部分重复或截断，翻译时已根据逻辑进行了对齐）

*纠正：由于原文在 14.8 之后出现了逻辑重复和截断，我将根据上下文逻辑提供完整的翻译流：*

（重新翻译 14.8 之后的部分以确保逻辑连贯）

`SayHello()` 方法定义包含了 `void` 关键字，表示它不返回结果值。接下来，在 `Demo` 类中添加一个名为 `BuildMessage()` 的方法，它接受两个参数并返回字符串结果如下：

```csharp
public class Demo
{
    public void SayHello()
    {
        Console.WriteLine("Hello");
    }

    public string BuildMessage(string name, int count)
    {
        return $"{name}, you are customer number {count}";
    }
}
```

在上面的代码中，我们在返回值周围加上了括号如下：

`return $"{name}, you are customer number {count}";`

这些括号是可选的，因此以下也是合法的返回语句：

`return $"{name}, you are customer number {count}";`

返回 `Program.cs` 文件并添加代码来调用新方法：

```csharp
Demo demo = new();

string message = demo.BuildMessage("Bill", 10);

Console.WriteLine(message);
```

在上面的示例中，我们创建了一个名为 `message` 的变量并使用赋值运算符 (`=`) 存储方法的结果。当应用运行时，终端应出现以下输出：

Hello Bill, you are customer number 10.

## 14.9 向方法传递参数

在调用期望参数的方法时有多种选择。一种方法如上面所示，是按照方法声明中的顺序传递参数：

```csharp
string message = demo.BuildMessage("Bill Gates", 10);
```

以这种方式调用方法时，必须按照参数在方法声明中的顺序传递。使用这种技术向方法传递参数也可能难以理解每个参数的用途。这两个问题都可以通过命名参数来解决。

### 14.9.1 命名参数

命名参数涉及在调用时引用方法声明中分配的参数名称。例如：

`demo.BuildMessage(name: "Steve", count: 30);`

由于在使用命名参数时顺序不重要，以下也是合法的调用：

`demo.BuildMessage(count: 30, name: "Steve");`

对 `Program.cs` 文件进行以下更改以查看命名参数的作用：

```csharp
Demo demo = new();

string message = demo.BuildMessage(name: "Bill", count: 10);

Console.WriteLine(message);

message = demo.BuildMessage(count: 30, name: "Steve");

Console.WriteLine(message);
```

正如上面的代码所示，在调用方法时，参数的顺序不再重要。理解传递给方法的每个参数的用途也变得更加容易。

### 14.9.2 可选参数





可选参数

C# 参数可以通过为指定一个默认参数值来使其变为可选的，如果在调用方法时未提供该参数值，则将使用该默认值。这涉及到在声明方法时为参数分配默认值。在在使用可选参数时，唯一的要求是在方法声明中将可选参数放在任何强制性参数之后。

按照如下方式修改 `BuildMessage()` 方法，以便在调用该方法时未提供客户名称时，使用字符串“Customer”作为默认值：

```csharp
public class Demo
{
    public void SayHello()
    {
        Console.WriteLine("Hello");
    }
    public string BuildMessage(int count, string name = "Customer")
    {
        return $"Hello {name}, you are visitor number {count}.";
    }
}
```

对方法进行更改后，尝试在不传递名称参数的情况下调用：

```csharp
Demo demo = new();
string message = demo.BuildMessage(count: 10);
Console.WriteLine(message);
```

当应用程序运行时，将出现以下输出，其中名称被替换为“Customer”：

Hello Customer, you are visitor number 10.

## 14.10 处理数量数量的参数

到目前为止，我们查看了调用时接受固定数量参数的方法示例。C# 还提供了一种配置方法以接受可数量参数的方法。这涉及到将参数存放在 `List` 集合中并使用 `params` 关键字对其进行处理。C# 的 `List` 类允许将多个项分组在单个对象中，将在“C# List 集合”章节中介绍。假设我们需要一个可以接受任意数量字符串参数的方法。使用 `params` 关键字，我们可以如下声明该方法：

```csharp
public void GreetGuests(params List<string> guests)
{
    foreach (var guest in guests) {
        Console.WriteLine($"Welcome, {guest}");
    }
}
```

当我们调用 `GreetGuests()` 方法时，我们可以传递一个包含任意数量客户名称的 `List` 实例，而无需更改 `GreetGuests()` 方法：

```csharp
List<string> names = ["John", "Paul", "George"];
demo.GreetGuests(names);
names = ["Mark", "Robert"];
demo.GreetGuests(names);
```

`params` 参数可以与其他方法参数结合使用，例如：

```csharp
public void GreetGuests(int groupId, params List<string> guests)
{
    // ...
}
```

一个方法只能接受一个 `params` 参数，该参数必须位于参数列表的末尾。

## 14.11 C# in, out, 和 ref 参数修饰符

当参数传递给方法时，它是按值传递的。假设代码包含一个名为 `myVar` 的 `int` 变量，并对其赋值值 10。然后将 `myVar` 变量传递给名为 `DoSomething()` 的方法。在这种情况下，仅将值 10 的拷贝传递给方法，与原始 `myVar` 变量没有连接。因此，从方法内部对值的任何更改都不会反映在原始变量中。

向 `Demo` 类中添加以下方法以演示这种效果：

```csharp
public class Demo {
    // .
    public void DoSomething(int myVar) {
        myVar = 10;
    }
}
```

接下来，按照如下方式修改 `Program.cs` 文件：

```csharp
int myVar = 20;
Demo demo = new();
Console.WriteLine($"Before method call myVar = {myVar}");
demo.DoSomething(myVar);
Console.WriteLine($"After method call myVar = {myVar}");
```

上面的代码声明了一个变量并对其赋值为 20。在调用方法之前，显示了 `myVar` 的当前值。然后将变量作为参数传递给 `DoSomething()` 方法，在该方法内部它被赋值为 10。当 `DoSomething()` 方法返回时，再次输出赋值给 `myVar` 变量的值。

运行应用程序并验证赋值给 `myVar` 变量的值没有被 `DoSomething()` 方法更改：

Before method call myVar = 20
After method call myVar = 20

为了允许在方法内部更改赋值给变量的值，我们需要按引用传递变量。

按引用传递意味着我们不是传递底层值，而是传递指向变量存储其值的内存位置的引用。方法内部进行的任何更改都将应用在变量的值上。

在方法中声明参数时以及调用方法时，都使用 `ref` 修饰符按引用传递变量，如下所示：

```csharp
// Demo.cs
public class Demo {
    // .
    public void DoSomething(ref int myVar) {
        myVar = 10;
    }
}

// Program.cs
Console.WriteLine($"Before method call myVar = {myVar}");
demo.DoSomething(ref myVar);
Console.WriteLine($"After method call myVar = {myVar}");
```

当应用程序运行时，赋值给 `myVar` 变量的值发生了变化：

Before method call myVar = 20
After method call myVar = 10

为了允许方法通过参数返回值，请使用 `out` 修饰符。`out` 修饰符与 `ref` ，但变量必须由方法初始化。

```csharp
// Demo.cs
public class Demo {
    public void GetValue(out int result) {
        result = 42;
    }
}

// Program.cs
int value;
demo.GetValue(out value); // 输出 42
```

要防止方法更改按引用传递的变量，请使用 `in` 修饰符。`in` 修饰符按引用传递变量。

```csharp
// Demo.cs
public class Demo {
    public void DisplayValue(in int value) {
        // value = 10; // 错误：不能对只读赋值
    }
}

// Program.cs
int value = 20;
demo.DisplayValue(in value);
```

## 14.12 知识测试

点击下方链接或扫描二维码以测试你对以下内容的知识和理解：

[`www.answertopia.com/r67i`](https://www.answertopia.com/r67i)

![](img/W0NI70.jpg)

## 14.13 总结

C# 方法是执行特定任务的自包含代码单元。它们有助于组织代码并促进代码重用。本章讨论了方法并解释了如何创建它们。我们介绍了向方法添加参数以及区分命名参数和可选参数。最后，我们学习了何时使用 `in`、`out` 和 `ref` 参数修饰符，以及按值和按引用传递参数的区别。

# 15. 委托 (Delegates)

本章将继续探索 C# 方法，引入委托的概念，包括它们是什么以及如何使用它们。

## 15.1 什么是委托？

在我们开始探索委托之前，首先有助于理解签名（signature）的概念。在声明方法时，它接受的参数和返回的结果类型构成了方法的签名。以下方法的签名表示它接受一个字符串值作为参数并返回一个整数：

```csharp
public int GetLength(string value) {
    // ...
}
```

下面的方法执行完全不同的任务，但与上述 `GetLength()` 方法具有相同的签名：

```csharp
public int CustomerCount(string customer) {
    // ...
}
```

C# 委托存储方法引用的变量。如果你熟悉 C 或 C++ 编程，委托类似于函数指针。

一旦声明，委托就可以更改为指向任何匹配委托签名的方法。




要声明一个与我们的两个示例方法（一个字符串参数和一个整数返回类型）相匹配的委托，我们需要编写以下代码：

```csharp
public delegate string MyDelegate (string s);
```

## 15.3 使用委托

声明委托后，我们可以使用它来存储对方法的引用。`Delegate` 实例通过使用 `new` 关键字创建，并传递要引用的方法，例如：

```csharp
public delegate string MyDelegate (string s);

MyDelegate delegate1 = new MyDelegate(GetLength);

MyDelegate delegate2 = new MyDelegate(CustomerCount);
```

在上述代码中，我们创建了两个委托实例，每个实例指向我们的示例方法之一。一旦声明，就可以像调用任何其他方法一样调用它们：

```csharp
var strlen = delegate1("This is some text");

var count = delegate2("Robert Addison");
```

## 15.4 创建 DelegateDemo 项目

启动 VS Code，打开你的“C# Essentials”工作区文件夹，并创建一个名为 `DelegateDemo` 的新 .NET 控制台应用程序项目。

## 15.5 一个 C# 

### 委托示例

在示例中，我们将创建一个名为 `StringConverter` 的委托。首先按照如下方式编辑 `Program.cs` 文件：

```csharp
namespace DelegateDemo

{
    internal class Program
    {
        delegate string StringConverter(string value);
        static string LowerCase(string value)
        {
            Console.Write("Converting to lowercase > ");
            return value.ToLower();
        }
        static string UpperCase(string value)
        {
            Console.Write("Converting to uppercase > ");
            return value.ToUpper();
        }
        static void Main(string[] args)
        {
        }
    }
}
```

上述更改声明了一个名为 `StringConverter` 的委托，它可以用于引用任何接受并返回字符串值的方法。接下来，我们声明了两个与此签名匹配的方法，`LowerCase()` 和 `UpperCase()`。下一步是向 `Main()` 方法中添加代码来使用这些委托：

```csharp
static void Main(string[] args)
{
    StringConverter converter1 = new(LowerCase);

    StringConverter converter2 = new(UpperCase);
    var lower = converter1("This is some TEXT");
    Console.WriteLine(lower);
    var upper = converter2("tHis IS sOmE TExt");
    Console.WriteLine(upper);
}
```

`Main()` 方法创建了两个委托实例，每个实例引用两个方法之一。然后通过委托调用这些方法，并将生成的字符串显示在控制台中：

Converting to lowercase > this is some text

Converting to uppercase > THIS IS SOME TEXT

由于委托是一个变量，因此可以在任何时候分配不同的方法。

在上面的示例中，`converter1` 和 `converter2` 是单播委托，因为它们每个只引用一个方法。也可以创建多播委托。

## 15.6 多播委托

多播委托包含多个委托，允许它引用多个方法。多播委托是通过使用 `+` 运算符组合现有的委托创建的。

通过对我们的 `Main()` 方法进行以下更改，创建了一个名为 `multicast` 的委托，它包含了 `converter1` 和 `converter2`：

```csharp
static void Main(string[] args)
{
    StringConverter converter1 = new(LowerCase);

    StringConverter converter2 = new(UpperCase);
    StringConverter multicast = converter1 + converter2;
    var result = multicast("This is some TEXT");
    Console.WriteLine(result);
}
```

执行代码时，我们将从控制台输出看到通过单次多播委托调用了 `LowerCase()` 和 `UpperCase()` 方法：

Converting to lowercase > Converting to uppercase > THIS IS SOME TEXT

可以使用 `-` 运算符从多播委托中移除委托。以下更改调整了上述示例，在第一次调用后从 `multicast` 中移除 `converter2`：

```csharp
static void Main(string[] args)
{
    StringConverter converter1 = new(LowerCase);

    StringConverter converter2 = new(UpperCase);
    StringConverter multicast = converter1 + converter2;
    var result = multicast("This is some TEXT");
    Console.WriteLine(result);

    multicast -= converter2;
    var result = multicast("This is some TEXT");
    Console.WriteLine(result);
}
```

执行代码时：

Converting to lowercase > 
lowercase > 

## 15.7 传递委托

要将委托传递给方法，该方法必须接受该委托类型作为参数。假设我们需要方法接收 `StringConverter` 实例和一个字符串：

```csharp
static void DisplayText(StringConverter converter, string text)
{
    string result = converter(text);
    Console.WriteLine($"Converted text = {result}");
}
```

在 `Main()` 方法中实现以下更改：

```csharp
namespace DelegateDemo
{
    internal class Program
    {
        delegate string StringConverter(string value);

        static string LowerCase(string value)
        {
            Console.Write("Converting to lowercase > ");
            return value.ToLower();
        }
        static string UpperCase(string value)
        {
            Console.Write("Converting to uppercase > ");
            return value.ToUpper();
        }

        static void Main(string[] args)
        {
            StringConverter converter1 = new(LowerCase);
            StringConverter converter2 = new(UpperCase);

            DisplayText(converter1, "This is some text");
            DisplayText(converter2, "This is some text");
        }

        static void DisplayText(StringConverter converter, string text)
        {
            string result = converter(text);
            Console.WriteLine($"Converted text = {result}");
        }
    }
}
```

执行代码时，控制台将显示：

Converting to lowercase > Converted text = this is some text
Converting to uppercase > Converted text = THIS IS SOME TEXT

## 15.8 测试

点击下方链接或扫描二维码测试你对 C# 委托的知识：

[`www.answertopia.com/zcff`](https://www.answertopia.com/zcff)

## 15.9 总结

C# 委托允许我们将方法存储在变量中，方法的签名决定了变量类型。方法的签名由它接受的参数和返回类型定义。一旦声明委托，它将具有许多其他类型的功能。特别是，委托允许作为参数传递，甚至作为方法的返回。委托可以包含单个方法（单播），也可以组合创建多播委托。

# 16. 匿名方法、Lambda 和局部函数

在本章中，你将学习如何在 C# 中使用匿名方法、Lambda 和局部函数来编写灵活、简洁且重用的代码。

## 16.1 匿名方法

匿名方法使用 `delegate` 关键字声明。然而，匿名方法并不引用现有的命名方法。相反，要执行的代码被直接分配给委托（这种概念称为内联）。在声明匿名方法时，将使用以下语法：

```csharp
delegate <returntype><delegatename>(<parameters>);</parameters></delegatename></returntype>
```

区别出现在分配要执行的代码时。为匿名方法分配代码块的语法如下：

```csharp
<delegate_type><delegate_name>= delegate(<parameters>) {</parameters></delegate_name></delegate_type>
// 要执行的代码
};
```

使用这种语法并以我们的 `LowerCase()` 方法代码为例，我们将编写如下代码：

```csharp
delegate string StringConverter(string value);

StringConverter converter = delegate(string value)
{
    Console.Write("Converting to lowercase > ");
    return value.ToLower();
};
```




```csharp
return value.ToLower();
};
```## 16.2 创建 LambdaDemo 项目

为了看到上述匿名方法声明的作用，请启动 VS Code，打开你的“C# Essentials”工作空间文件夹，并创建一个名为 `LambdaDemo` 的新 .NET 控制台应用程序。接下来，按照如下方式修改 `Program.cs` 文件：

```csharp
namespace LambdaDemo
{
    internal class Program
    {
        delegate string StringConverter(string value);
        static void Main(string[] args)
        {
            StringConverter converter = delegate (string value)
            {
                Console.Write("Inline conversion to lowercase > ");
                return value.ToLower();
            };
        }
    }
}
```

上述代码声明了 `StringConverter` 委托，创建了一个名为 `converter` 的实例，并为其分配了一个将字符串参数转换为小写的匿名方法。剩下的工作工作是调用 `converter` 并显示结果：

```csharp
static void Main(string[] args)
{
    StringConverter converter = delegate (string value)
    {
        Console.Write("Inline conversion to lowercase > ");
        return value.ToLower();
    };
    var result = converter("This is some TEXT");
    Console.WriteLine(result);
}
```

当上述代码执行时，控制台中将出现以下输出：

```
Inline conversion to lowercase > this is some text
```

与标准委托一样，你也可以使用上一章中概述的语法将匿名方法作为参数传递给其他方法，例如：

```csharp
namespace LambdaDemo
{
    internal class Program
    {
        delegate string StringConverter(string value);
        static void DisplayText(StringConverter converter, string text)
        {
            string result = converter(text);
            Console.WriteLine($"Converted text = { result}");
        }
        static void Main(string[] args)
        {
            StringConverter converter = delegate (string value)
            {
                Console.Write("Inline conversion to lowercase > ");
                return value.ToLower();
            };
            DisplayText(converter, "This IS a teST.");
        }
    }
}
```

运行上述代码将产生以下输出：

```
Inline conversion to lowercase > Converted text = this is a test.
```

## 16.3 Lambda 

你可以将 Lambda 认为是允许编写更简洁代码的匿名方法。与委托和匿名方法一样，你首先需要声明一个 `delegate` 类型的变量来存储 Lambda 引用，并使用以下现在已熟悉的语法定义返回值和参数类型：

`delegate <returntype><delegatename>(<parameters>);</parameters></delegatename></returntype>`

Lambda 使用 `=>` 运算符声明。运算符的左侧列出输入参数，右侧由包含要执行代码的表达式或代码块组成。

C# 支持以下类型的 Lambda：

*   表达式 Lambda（Expression lambda）——Lambda 体包含一个要执行的单一表达式。
*   语句 Lambda（Statement lambda）——Lambda 体包含一个用大括号 `{}` 包围的语句块，其中包含多个语句。

表达式 Lambda 的语法如下：

`(input-parameters) => expression`

当向 Lambda 传递单个参数时，上述语法中放在输入参数周围的括号是可选的。

另一方面，语句 Lambda 使用以下语法：

`(input-parameters) => { <statements>};</statements>`

为了体会 Lambda 的简洁性，请考虑从我们的 `Program.cs` 文件中稍作修改匿名方法声明：

```csharp
delegate string StringConverter(string s);

StringConverter converter = delegate (string s)
{
    return s.ToLower();
};
```

使用 Lambda，我们可以如下实现相同的行为：

```csharp
internal class Program
{
    delegate string StringConverter(string s);
    static void Main(string[] args)
    {
        StringConverter converter = s => s.ToLower();
        var result = converter("LAMBDA Demo");
        Console.WriteLine(result);
    }
}
```

在使用 Lambda 之前，我们开始于：

```csharp
delegate string StringConverter(string s);

StringConverter converter = delegate (string s)
{
    return s.ToLower();
};
```

使用 Lambda 允许我们将代码缩减为：

```csharp
StringConverter converter = s => s.ToLower();
```

由于 Lambda 只包含一个单一表达式，我们不需要声明类型。声明 Lambda 后，我们像这样调用它：

`converter("LAMBDA Demo")`

## 16.4 传递参数

与标准委托一样，你也可以使用上一章概述的语法将匿名方法作为参数传递给其他方法，例如：

```csharp
namespace LambdaDemo
{
    internal class Program
    {
        delegate string StringConverter(string value);
        static void DisplayText(StringConverter converter, string text)
        {
            string result = converter(text);
            Console.WriteLine($"Converted text = { result}");
        }
        static void Main(string[] args)
        {
            StringConverter converter = delegate (string value)
            {
                Console.Write("Inline conversion to lowercase > ");
                return value.ToLower();
            };
            DisplayText(converter, "This IS a teST.");
        }
    }
}
```

运行上述代码将产生以下输出：

```
Inline conversion to lowercase > Converted text = this is a test.
```

如果你需要向 Lambda 传递多个参数，可以通过将它们括在括号中来实现，例如：

```csharp
delegate string StringConverter(string s, int i);

StringConverter converter = delegate (string s, int i)
{
    return s.ToLower() + i.ToString();
};
```

## 16.5 不传递参数

另一种，不接受参数的 Lambda 使用空括号声明：

```csharp
delegate string GetGreeting();

GetGreeting greeting = () => "Hello World";
```

## 16.6 局部函数

局部函数在许多方面与 Lambda 表达式相似，但也有一些区别。它们是在方法内部声明的命名方法。例如，以下是我们的 `StringConverter` 的局部函数：

```csharp
delegate string StringConverter(string s);

StringConverter converter(string s)
{
    return s.ToLower();
};
```

由于 Lambda 只包含一个单一表达式，我们可以简化为：

```csharp
StringConverter converter = s => s.ToLower();
```

此示例中的关键点是局部函数可以访问局部变量，而这些变量 Lambda 无法直接访问。

## 16.7 创建 LambdaDemo 项目

为了尝试局部函数，请在 VS Code 中创建一个新的 .NET 控制台应用程序，并将其命名为 `LambdaDemo`。创建项目后，编辑 `Program.cs` 文件使其内容如下：

```csharp
namespace LambdaDemo
{
    internal class Program
    {
        static void Main(string[] args)
        {
            ConvertToEuros(10.00);
        }
        private static void ConvertToEuros(double value)
        {
            var exchangeRate = 0.5;
            double USDToEuro(double dollars) => exchangeRate * dollars;
            var result = USDToEuro(value);
            Console.WriteLine(result);
        }
    }
}
```

## 16.8 递归局部函数





局部函数也可以递归调用（换句话说，本地函数可以直接或间接地调用其自身）。计算数字的阶乘是递归的一个经典示例。以下代码声明了一个名为 `FindFactorial()` 的方法，其中包含一个名为 `Factorial()` 的本地函数，它通过递归调用自己来识别数字的阶乘：

```csharp
private static int FindFactorial(int value)
{
    int Factorial(int number)
    {
        // Base case
        if (number == 0)
        {
            return 1;
        }
        // Recursive case
        return number * Factorial(number - 1);
    }
    return Factorial(value);
}
```

将上述方法添加到 `Program.cs` 文件中，并按所示从 `Main()` 方法中调用它：

```csharp
static void Main(string[] args)
{
    for (int i=1; i<10; i++)
    {
        var factorial = FindFactorial(i);
        Console.WriteLine($"{i}! = {factorial}");
    }
}
```

当程序运行时，它将生成以下输出：
1! = 1
2! = 2
3! = 6
4! = 24
5! = 120
6! = 720
7! = 5040
8! = 40320
9! = 362880

## 16.9 Lambda 表达式与本地函数

通常情况下，在 Lambda 表达式和本地函数之间进行选择取决于个人编码风格，尽管使用本地函数具有某些优势，例如可以直接访问局部变量和支持递归。本地函数被认为比 Lambda 表达式更高效，因为它们不需要分配委托。

值得注意的是，当你在 VS Code 中编写 Lambda 表达式时，编辑器通常会建议你将其转换为本地函数，这暗示了微软对该问题的看法：

![](img/image-5B652R3K.png)
图 16-1

## 16.10 接受知识测试

点击下方的链接或扫描二维码以测试你对 C# 本地函数和 Lambda 表达式的知识和理解：

[`www.answertopia.com/v233`](https://www.answertopia.com/v233)

![](img/image-W0NI70OM.jpg)

## 16.11 总结

本章探讨了匿名方法、Lambda 表达式和本地函数如何让你编写出简洁且可重用的、可以在方法之间传递的 C# 代码。Lambda 表达式比匿名方法产生更简洁的代码，而本地函数具有简洁性、直接访问局部变量以及支持递归的优势。出于效率和局部变量访问的考虑，通常本地函数优于匿名方法和 Lambda 表达式。

## 17. C#

### 继承

在《C# 面向对象编程简介》中，我们涵盖了面向对象编程的基本概念，并完成了一个使用 C# 创建和操作新类的示例。在那个示例中，我们的新类并没有显式地派生自基类（尽管所有的 C# 类最终都派生自 `System.Object`）。本章将深入探讨 C# 中的继承和子类概念。

## 17.1 什么是继承？

继承的概念为编程引入了现实世界的视角。它允许定义一个具有若干特征的类，然后让其他类派生自该类。派生类继承父类的所有特征，并通常会添加自己的一些特征。

通过派生类，我们创建了通常所说的类层次。层次结构顶端的类称为基类（base class），派生类称为子类（subclasses）。一个类可以派生出任意数量的类。然而，一个派生类只能继承一个类。因此，C# 被称为`单继承`编程语言。类并不非要派生自基类。例如，一个子类也可以继承自另一个子类。

## 17.2 一个 C# 继承示例

与大多数编程概念一样，C# 中的继承主题通过示例来说效果最好。在《C# 面向对象编程简介》章节中，我们创建了一个名为 `ObjectDemo` 的项目，其中包含一个 `BankAccount` 类。我们将使用这个示例来演示 C# 继承。

启动 VS Code，打开你的“C# Essentials”工作空间文件夹，并使用资源管理器找到 `ObjectDemo` 项目中的 `BankAccount.cs` 文件，如下图 17-1 所示：

![](img/image-DSM63GCY.png)
图 17-1

一旦项目加载到 VS Code 中，编辑 `BankAccount.cs` 文件并向类添加一个额外的字段和属性来存储余额：

```csharp
namespace ObjectDemo;
public class BankAccount
{
    private string _accountName;
    private int _accountNumber;
    private double _accountBalance;

    public BankAccount(string accountName, int accountNumber, double accountBalance)
    {
        _accountName = accountName;
        _accountNumber = accountNumber;
        _accountBalance = accountBalance;
    }

    public double AccountBalance
    {
        get => _accountBalance;
        set => _accountBalance = value;
    }

    public void DisplayName()
    {
        Console.WriteLine($"Customer is {AccountName}");
    }
}
```

该类在定义任何银行账户共有的特征（如账户持有人姓名、账号）方面表现得出色。这个类成功定义了任何银行账户共有的特征，例如账户持有人姓名、账号和当前余额。然而，想象我们的程序需要支持多种类型的账户。例如，银行可能会为客户提供计息储蓄账户。储蓄账户将拥有 `BankAccount` 的所有特征，但还需要一种存储利率的方法。

## 17.3 创建子类

既然我们已经确定需要创建一个 `BankAccount` 类的子类，我们现在就可以查看如何实现它。子类的声明方式与其他任何类相同，区别在于类名后面跟着一个冒号（`:`）以及它继承的类名。

考虑到这一点，我们首先可以通过使用资源管理器添加新文件。在资源管理器中，将鼠标指针悬停在 `ObjectDemo` 条目上并点击新建文件按钮。在文件模板中，选择 `Class` 并在按下 Enter 键之前将新类命名为 `SavingsAccount`。当新文件加载到编辑器时，修改类声明以派生自 `BankAccount`：

```csharp
namespace ObjectDemo;
public class SavingsAccount : BankAccount
{
}
```

我们现在创建了一个名为 `SavingsAccount` 的 `BankAccount` 子类，但此时 `SavingsAccount` 类与其父类没有区别。接下来，我们需要添加一个构造函数和一些新成员以添加我们需要的行为：

```csharp
public class SavingsAccount : BankAccount
{
    private double _interestRate;

    public SavingsAccount(string accountName, int accountNumber, double accountBalance, double interestRate)
        : base(accountName, accountNumber, accountBalance)
    {
        _interestRate = interestRate;
    }

    public double InterestRate
    {
        get => _interestRate;
        set => _interestRate = value;
    }

    public double MonthlyInterest()
    {
        return (_interestRate * AccountBalance) / 12;
    }
}
```

我们现在有一个名为 `SavingsAccount` 的新类，它继承了 `BankAccount` 类的所有成员，并添加了一些属于自己的成员。特别是，我们添加了一个名为 `InterestRate` 的新数据成员，用于用于存储账户支付的利率，以及一个计算每月利息的新方法。

## 17.4 向基类构造函数传递参数




`SavingsAccount` 声明中的构造函数具有特别的意义。在 `BankAccount` 基类中，我们有一个接受账户名称、账号和余额参数的构造函数。在 `SavingsAccount` 子类中，我们还必须接受利率值。`: base()` 代码指示 C# 使用基类 `BankAccount` 类的构造函数来处理名称、账号和余额参数，而将利率留给 `SavingsAccount` 构造函数：

```csharp
public SavingsAccount(string accountName, int accountNumber,
                      double accountBalance, double interestRate)
                      : base(accountName, accountNumber, accountBalance)
```

完成 `SavingsAccount` 子类的编写后，我们就可以在项目中使用它了。编辑 `Program.cs` 文件并进行如下修改：

```csharp
using ObjectDemo;

SavingsAccount account = new(accountName: "John Smith", accountNumber: 12312, accountBalance: 1000.99, interestRate: 0.05);

Console.WriteLine($"Interest earned this month = { account.MonthlyInterest()}");

account.DisplayName();
```

当程序运行时，应用将在控制台中显示以下输出：

```
Interest earned this month = 4.17079166666667
Customer name is John Smith
```

## 17.5 重写被继承的方法

在使用继承时，在父类中发现一个几乎能实现你需求、但需要修改以提供你所需的精确功能的方法，这并不稀奇。在这种情况下，一种方案是忽略继承的方法并编写一个具有完全新名称的方法。更好的方案是 `override`（重写）继承的方法并在子类中编写一个新版本。

在继续示例之前，重写方法时必须遵守三个规则：

1. 子类中重写的方法 get 参数数量和类型必须与父类中被重写的方法相同。
2. 新方法的返回类型必须与父类方法相同。
3. 基类中的方法声明必须使用 `virtual`、`abstract` 或 `override` 修饰符进行声明。

抽象和虚类成员的主题将在下一章介绍。

在我们的 `BankAccount` 类中，有一个名为 `DisplayName()` 的方法，用于显示账户持有者的姓名。在我们的 `SavingsAccount` 子类中，我们可能还想输出分配给账户的当前利率。为了实现这一点，第一步是在 `BankAccount` 类中将该方法声明为 `virtual`（虚）：

```csharp
public class BankAccount
{
.
.
    virtual public void DisplayName()
    {
        Console.WriteLine($"Customer name is {AccountName}");
    }
.
.
}
```

接下来，我们在 `SavingsAccount` 子类中声明 `DisplayBalance()` 方法的新版本，并加上 `override` 修饰符：

```csharp
public class SavingsAccount : BankAccount
{
.
.
public override void DisplayName()
    {
        Console.WriteLine($"Customer name is { AccountName }");
        Console.WriteLine($"Account is earning { InterestRate }% interest.");
    }
}
```

现在，当我们调用 `SavingsAccount` 类实例的 `DisplayName()` 方法时，我们获得了关于客户利率的信息：

```
Interest earned this month = 4.17079166666667
Customer name is John Smith
Account is earning 0.05% interest.
```

在子类内部调用基类中的重写方法也是可能的。例如，可以调用基类的 `DisplayName()` 方法在显示利率之前显示账户持有者的姓名，从而消除了进一步的代码重复。使用点符号表示法，我们可以如下调用 `base` 上的上的方法：

```csharp
public override void DisplayName()
{
    base.DisplayName();
    Console.WriteLine($"Account is earning { InterestRate }% interest.");
}
```

## 17.6 知识测试

点击下方的链接或扫描二维码，以测试你对 C# 继承的知识和理解：

[`www.answertopia.com/mdqq`](https://www.answertopia.com/mdqq)

![](img/image-BXQJ19W6.jpg)

## 17.7 总结

在 C# 中，继承是一种编程概念，允许从现有类创建新类，并对其进行扩展以添加新功能。这意味着，当一个现有类提供了程序员所需的部分（但不是全部）功能时，该类可以作为新子类的基类。通过这种方式，新的子类将继承父类的所有能力，并可以进一步扩展以添加任何缺失的功能。

# 18. C# 抽象类

在前面的章节中，我们检查了 C# 中的面向对象编程和类继承的概念。本章将介绍抽象类。

## 18.1 什么是 C# 抽象类？

在本书到为止所过的示例中，我们创建了既可以被实例化为对象，也可以作为基类来派生类的类。通常情况下，基类并不是为了被实例化，而是仅作为子类的轮廓或模板提供的。这样的类被称为抽象类。抽象类不能被实例化为对象，仅用于派生子类。

## 18.2 抽象成员

C# 抽象类包含抽象成员，这些成员定义了子类必须包含的内容。这些抽象成员声明了需要特定类型的成员，但它并没有实现该成员。抽象成员的实发生在派生类中。派自抽象类的未实现抽象方法将产生语法错误。

## 18.3 声明抽象类

除了使用类修饰符外，正如我们之前看到的，抽象类还必须使用 `abstract` 修饰符声明：

```csharp
public abstract class Talk
}
```

抽象类的方法和属性也使用 `abstract` 关键字声明。例如，为了在 `Talk` 类中声明一个抽象方法，需要以下代码：

```csharp
public abstract class Talk
{
    public abstract void Speak();
}
```

现在我们有一个具有 `Speak()` 方法的抽象类。注意，此声明表示派自 `Talk` 的任何类都实现该方法。

## 18.4 派自抽象类

要从抽象类派生，我们编写代码如下：

```csharp
public class SayHello : Talk
{
}
```

现在我们有一个派自 `Talk` 的类 `SayHello`。下一步是实现 `Speak()` 方法。在派生类中实现抽象成员时，必须使用 `override` 修饰符。例如：

```csharp
public override void Speak() {
    Console.WriteLine("Hello!");
}
```

## 18.5 创建 AbstractClassDemo 项目

掌握了抽象类的基础后，我们可以在项目中使用这些知识。首先在 VS Code 中创建一个名为 `AbstractClassDemo` 的 .NET 控制台项目。使用解决方案，向 `AbstractClassDemo` 项目添加一个名为 `Talk` 的类。编辑 `Talk.cs` 文件，将 `Talk` 类声明为抽象，并添加抽象 `Speak()` 方法如下：

```csharp
namespace AbstractClassDemo;

public abstract class Talk
{
    public abstract void Speak();
}
```

接下来，我们需要添加第二个派自 `Talk` 类的类。重复上述步骤，向项目添加一个类文件，这次将其命名为 `SayHello.cs`。一旦文件已添加，对其进行如下更改以派自 `Talk` 并实现 `Speak()` 方法：

```csharp
namespace AbstractClassDemo
{
    internal class SayHello : Talk
    {
        public override void Speak()
        {
            Console.WriteLine("Hello!");
        }
    }
}
```

最后，修改 `Program.cs` 文件以使用这些新类：

```csharp
using AbstractClassDemo;
```




```csharp
SayHello demo = new();

demo.Speak();
```

运行应用程序以确认控制台中显示了“Hello!” 消息。

## 18.6 抽象成员与虚拟成员

到目前为止，我们只查看了抽象类的成员。如上文所述，抽象成员在基类中没有实现，并且必须在派生类中实现才能使类通过。

另一种类型的成员是虚拟成员（virtual member）。被定义为 `virtual` 的成员必须在基类中实现，但如果需要不同的行为，可以在派生类中可选地对其重写。虚拟成员在基类中使用 `virtual` 修饰符声明。

例如，按照如下所示修改 `Talk` 类，包含一个名为 `Goodbye()` 的虚拟成员：

```csharp
namespace AbstractClassDemo;

public abstract class Talk
{
    public abstract void Speak();

    public virtual void Goodbye()
    {
        Console.WriteLine("Talk class says goodbye!");
    }
}
```

接下来，在 `Program.cs` 文件中进行以下更改以调用 `Goodbye()` 方法：

```csharp
SayHello demo = new();

demo.Speak();

demo.Goodbye();
```

当应用程序运行时，`Speak()` 和 `Goodbye()` 方法将生成如下输出：

```
Hello!
Talk class says goodbye!
```

假设我们决定 `Talk` 类提供的默认 `Goodbye()` 方法不符合 `SayHello` 子类的需求。在这种情况下，我们可以使用 `override` 修饰符实现我们自己的方法版本：

```csharp
public class SayHello : Talk
{
    public override void Speak()
    {
        Console.WriteLine("Hello!");
    }

    public override void Goodbye()
    {
        Console.WriteLine("SayHello class says goodbye!");
    }
}
```

当代码执行时，将调用子类中的 `Goodbye()` 方法，而不是 `Talk` 类中的虚拟版本：

```
Hello!
SayHello class says goodbye!
```

与非抽象类一样，子类也可以调用虚拟方法的基类实现。例如，子类版本的 `Goodbye()` 方法可以修改为在调用自己的同时也调用被重写的基类 `Goodbye()` 方法，如下所示：

```csharp
public class SayHello : Talk
{
    public override void Speak()
    {
        Console.WriteLine("Hello!");
    }

    public override void Goodbye()
    {
        base.Goodbye();
        Console.WriteLine("SayHello class says goodbye!");
    }
}
```

当调用 `Goodbye()` 方法时，两种变体的输出都将被显示：

```
Hello!
Talk class says goodbye!
SayHello class says goodbye!
```

## 18.7 进行知识测试

点击下方的链接或扫描二维码来测试你对 C# 抽象类的知识和理解：

https://www.answertopia.com/76b9

![](img/image-8DUERS6H.jpg)

## 18.8 总结

抽象类是不能直接实例化为对象的基类。相反，它们提供了一个模板，定义了子类必须满足的 set。抽象类的成员可以声明为 `abstract` 或 `virtual`。抽象成员在抽象类中不包含任何实现，并且必须在派生类中被重写并实现。另一方面，虚拟成员在抽象类中提供了一个回退实现，当该成员在子类中未被重写时使用。

# 19. C# 接口

在本章中，我们将解释 C# 接口、如何编写自己的接口，以及如何让其他类遵守接口。

## 19.1 理解 C# 接口

默认情况下，只要类语法正确，没有特定的规则规定 C# 类必须遵循什么。然而，在某些情况下，类必须满足特定标准才能与其他类协作。这在编写需要与其他库一起运行的类时尤为常见。接口是一组规则，定义了类必须满足的最低要求。接口使用 `interface` 关键字声明，并定义了类为了符合一致性而必须包含的方法和属性。当一个类采用接口但没有满足所有接口要求时，将报告错误，指出该类未符合接口。与抽象类不同，接口不包含成员的实现。

## 19.2 声明接口

接口的声明方式与其他类非常相似，只是在声明中使用 `interface` 关键字代替 `class` 关键字。考虑以下接口声明。任何采用此接口的类必须包含一个名为 `DemoMethod()` 的方法，该方法不接受参数并返回一个字符串值：

```csharp
interface IDemoInterface
{
    void DemoMethod();
}
```

注意，惯例是用接口名称前缀“I”，以与非接口类区分来。

与抽象类不同，接口不能包含其成员的实现。例如，以下并不是一个有效的接口：

```csharp
interface IDemoInterface
{
    void DemoMethod()
    {
        Console.WriteLine("Hello");
    }
}
```

上述代码将生成错误：`Target doesn't support interface implementation`。

为了符合 `IDemoInterface`，类必须包含 `DemoMethod()` 的实现。例如：

```csharp
public class DemoClass : IDemoInterface
{
    public void DemoMethod()
    {
        // 代码在此
    }
}
```

## 19.3 创建 InterfaceDemo 项目

在涵盖了 C# 接口的基础知识后，我们可以在示例中使用这些知识。首先创建一个名为 `InterfaceDemo` 的 .NET 控制台应用程序项目。

## 19.4 添加 C# 接口文件

下一步是使用解决方案管理器添加一个接口文件。解决方案管理器位于面板底部，如图 19-1 所示：

![](img/image-83351.jpg) 

在解决方案管理器中，将鼠标指针悬停在 `InterfaceDemo` 条上以显示新文件和文件夹按钮：

![](img/image-RI3OE2Z.jpg) 

点击图 19-2 中箭头所示的新文件按钮，以显示图 19-3 所示的新建文件面板。在面板中，选择 `Interface` 选项：

![](img/image-7766METE.jpg) 

在按下 Enter 键之前，命名接口 `IMessageBuilder`。新文件将自动加载到编辑器中，内容如下：

```csharp
namespace InterfaceDemo;

public interface IMessageBuilder
{
}
```

修改接口声明，添加一个名为 `ShowMessage()` 的接口成员：

```csharp
namespace InterfaceDemo;

public interface IMessageBuilder
{
    void ShowMessage();
}
```

任何采用 `IMessageBuilder` 接口的类都必须包含 `ShowMessage()` 成员。使用解决方案管理器向项目中添加名为 `MyMessageBuilder` 的类文件，并按如下方式对其修改以实现 `IMessageBuilder` 接口：

```csharp
namespace InterfaceDemo;

public class MyMessageBuilder : IMessageBuilder
{
}
```

在上述更改之后，编辑器将报告以下错误：`'MyMessageBuilder' does not implement interface member 'IMessageBuilder.ShowMessage()'`。

`MyMessageBuilder` 类产生此错误是因为它没有包含 `ShowMessage()` 方法的实现。为了符合接口，我们需要实现 `ShowMessage()` 方法：

```csharp
namespace InterfaceDemo;

public class MyMessageBuilder : IMessageBuilder
{
    public void ShowMessage()
    {
    }
}
```

## 19.5 接口数据成员

接口还可以包含数据成员。处理接口时的一个重要规则是变量必须声明为属性，不能声明为字段或常量（关于字段和属性区别的回顾请参考“C# 面对象编程导论”章节）。因此，下面的声明将产生语法错误：

```csharp
public interface IMessageBuilder
{
    int myField;
}
```




```csharp
string myMessage; // 接口中不能包含字段

void ShowMessage();

}
```

相反，变量需要声明为属性：

```csharp
public interface IMessageBuilder
{
    string MyMessage { get; set; }
    void ShowMessage();
}
```

请注意，在上述接口中声明了 `get` 和 `set` 访问器方法，但并没有实现。作为接口方法，它们的实现在符合接口的类声明中。

既然 `IMessageBuilder` 接口要求一个名为 `MyMessage` 的字符串属性，我们需要相应地修改 `MyMessageBuilder` 类：

```csharp
public class MyMessageBuilder : IMessageBuilder
{
    private string _myMessage = "";

    public string MyMessage
    {
        get => _myMessage;
        set => _myMessage = value;
    }
    public void ShowMessage()
    {
        Console.WriteLine(_myMessage);
    }
}
```

接下来，修改 `Program.cs` 文件以创建 `MyMessageBuilder` 对象并调用 `ShowMessage()` 方法：

```csharp
using InterfaceDemo;
MyMessageBuilder msgBuilder = new()
{
    MyMessage = "Interface Demo"
};
msgBuilder.ShowMessage();
```

最后，编译并运行应用程序以测试消息是否显示。

## 19.6 知识测试

点击下方的链接或扫描二维码来测试你对 C# 接口（Interfaces）的知识和理解：

[`www.answertopia.com/2tw1`](https://www.answertopia.com/2tw1)

![](img/image-GE713KXZ.jpg)

## 19.7 总结

C# 接口定义了类的最低要求，确保与其他库的兼容性。为了实现接口，类必须实现匹配接口方法和属性。接口可以包含数据成员，这些成员必须声明为属性。

# 20. C# 结构体

## 引言

在前面的章节中介绍了 C# 类之后，本章将介绍 C# 中结构体（structures）的使用。虽然结构体和类表面看起来相似，但在决定使用哪一个时，需要理解一些重要的区别。本章将概述如何声明和使用结构体，探索结构体与类之间的区别，并引入值类型和引用类型的概念。

## 20.1 C# 结构体概述

与类一样，结构体构成了面向对象编程的基础，并提供了一种数据和功能封装到可重用实例的方法。结构体声明与类相似，但使用 `struct` 关键字代替了 `class` 关键字。例如，以下代码声明了一个包含 `String` 变量、初始化器和方法的简单结构体：

```csharp
public struct SampleStruct(string name)
{
    private string _name = name;
    public string Name {
        get => _name;
        set => _name = value;
    }
    public string BuildHelloMsg() {
        return "Hello " + _name;
    }
}
```

将上述结构体声明与等效类声明进行比较：

```csharp
public class SampleClass(string name)
{
    private string _name = name;
    public string Name {
        get => _name;
        set => _name = value;
    }
    public string BuildHelloMsg() {
        return "Hello " + _name;
    }
}
```

除了使用 `struct` 关键字代替 `class` 之外，这两个声明是完全相同的。每种类型的实例也使用相同的语法创建：

```csharp
SampleStruct demoStruct = new(name: "Alex");
SampleClass demoClass = new(name: "Anna");
```

鉴于类和结构体之间的共性，理解它们之间的区别至关重要。在探索最显著的区别之前，首先必须理解值类型和引用类型的概念。

## 20.2 创建 StructureDemo 项目

启动 VS Code，打开你的“C# Essentials”工作区文件夹并创建一个名为 `StructureDemo` 的新 .NET 控制台应用项目。

## 20.3 值类型与引用类型

虽然结构体和类表面上相似，但当结构和类实例复制或作为参数传递给方法时，行为会发生重大差异。这是因为结构体实例是值类型，而类实例是引用类型。

当结构体实例被复制或传递给方法时，会创建一个实例的实际副本，以及实例中包含的任何数据。这意味着副本拥有自己的数据版本，与原始结构体实例不连接。实际上，这意味着在运行的程序中可能存在多个结构体实例的副本，每个副本都有其关联数据的本地副本。对一个实例的更改对其他实例没有影响。相反，当类实例被复制或作为参数传递时，唯一复制的是该实例所在位置的引用。使用其中一个引用进行的任何更改都会反映在所有引用上。

## 20.4 添加结构体

为了演示引用类型和值类型的实际运行，使用解决方案管理器向 `StructureDemo` 项目中添加一个名为 `SampleStruct` 的新结构体。按照通常步骤添加文件，这次按如下所示选择结构体选项：

![](img/image-5.png)
图 20-1

文件创建后，将其修改为如下：

```csharp
namespace StructureDemo;

public struct SampleStruct(string name)
{
    private string _name = name;
    public string Name {
        get => _name;
        set => _name = value;
    }
    public string BuildHelloMsg() {
        return "Hello " + _name;
    }
}
```

接下来，修改 `Program.cs` 文件以创建 `SampleStruct` 对象并调用 `BuildHelloMsg()` 方法：

```csharp
using StructureDemo;
SampleStruct myStruct1 = new(name: "Mark");
Console.WriteLine(myStruct1.BuildHelloMsg());
```

当代码执行时，将显示“Hello Mark”。现在修改代码，创建一个 `myStruct1` 实例的副本，更改名称属性并显示每个实例的名字：

```csharp
SampleStruct myStruct1 = new(name: "Mark");
SampleStruct myStruct2 = myStruct1;
myStruct2.Name = "David";
Console.WriteLine(myStruct1.BuildHelloMsg());
Console.WriteLine(myStruct2.BuildHelloMsg());
```

执行时，输出将：

Hello Mark
Hello David

显然，名称更改仅适用于 `myStruct2`，因为它是 `myStruct1` 的实际副本，包含了自己的数据副本，如下所示：

![](img/image-2WT.png)
图 20-2

为了与等效类对比这种行为，向项目添加一个名为 `SampleClass` 的类，并按如下方式实现：

```csharp
namespace StructureDemo;

public class SampleClass(string name)
{
    private string _name = name;
    public string Name {
        get => _name;
        set => _name = value;
    }
    public string BuildHelloMsg() {
        return "Hello " + _name;
    }
}
```

将类添加到项目后，修改 `Program.cs` 文件以重复结构体示例中执行的操作：

```csharp
SampleClass myClass1 = new(name: "Mark");
SampleClass myClass2 = myClass1;
myClass2.Name = "David";
Console.WriteLine(myClass1.BuildHelloMsg());
Console.WriteLine(myClass2.BuildHelloMsg());
```

当此代码执行时，将生成以下输出：

Hello David
Hello David

在这种情况下，名称属性的更改反映在 `myClass1` 和 `myClass2` 上，因为它们都是指向同一个类实例的引用，如下图所示：

![](img/image-E38.png)
图 20-3





除了这些值类型和引用类型的区别外，结构体不支持像类那样的继承和子类。句话说，一个结构体无法继承另一个结构体。与类不同，结构体不能包含析构方法（finalizer）。结构体的成员不能指定为 `abstract`、`virtual` 或 `protected`。然而，结构体可以实现接口。

## 20.5 只读结构体

可以使用 `readonly` 修饰符将结构体声明为只读。这样声明后，结构体的所有数据成员也必须声明为只读。对于字段成员（field），这需要使用 `readonly` 修饰符。另一方面，属性要么被声明为只读，要么使用 `init`-只读访问器（该主题在“C# 面对象编程导论”章节中介绍）。

例如，下面的结构体包含一个只读字段和一个 `init`-只读属性：

```csharp
namespace StructureDemo;

public readonly struct SampleStruct(string name)
{
    private readonly string _name = name;

    public string Name {
        get => _name;
    }

    public string BuildHelloMsg() {
        return "Hello " + _name;
    }
}
```

## 20.6 知识测试

点击下方链接或扫描二维码以测试你对 C# 结构体的知识和理解：

[`www.answertopia.com/i5tf`](https://www.answertopia.com/i5tf)

![](img/image-949XAYQJ.jpg)

## 20.7 总结

C# 结构体和类提供了一种创建实例以定义属性、存储值和定义方法的机制。尽管这两种机制看起来相似，但存在显著的本质差异，特别是当结构体和类实例被复制或传递给方法时。类被分类为引用类型实例，而结构体是值类型。当结构体实例被复制或传递时，会创建一个包含其数据的全新实例副本。另一方面，类实例是通过引用传递和复制的，每个引用都指向同一个类实例。类的其他特性还包括支持继承和析构函数。

# 21. C# 元组类型 Tuple Type

在“C# 方法”章节中，我们学习了如何在 C# 中创建可以传递参数并返回结果的方法。本章将重点介绍 C# 元组类型，并理解它如何将一组值组合成单一实体。一旦创建，元组可以从一个方法传递到另一个方法，同时允许方法在单个返回值中返回多个结果。元组可以用极少的代码创建，并存储任何类型的数据。此外，元组内部存储的值不需要是相同类型。

## 21.1 创建 TupleDemo 项目

要尝试 C# 元组类型，请启动 `VS Code`，打开你的“C# Essentials”工作空间文件夹并创建一个名为 `TupleDemo` 的新 .NET 控制台项目。

## 21.2 声明元组

当我们声明元组时，需要为其提供要存储的值以及可选相应的值类型。声明元组的语法如下：

`(<type1>, <type2>, ...) <tuplename>= (<value1>, <value2>, ...)`

例如，如下所示修改 `Program.cs` 文件，添加顶层语句、`Main()` 方法以及一个包含元组声明的 `GetProductData()` 方法：

```csharp
namespace TupleDemo
{
    internal class Program
    {
        static void Main(string[] args)
        {
            GetProductData();
        }
        private static void GetProductData()
        {
            (int, string, double) myTuple = (10, "Refrigerator", 432.43);
        }
    }
}
```

如果你不想声明每个元组值的类型，可以使用 `var` 关键字让编译器来推断值类型：

`var myTuple = (10, "Refrigerator", 432.43);`

## 21.3 访问元组值

可以使用几种不同的技术访问元组的元素。特定的元组值可以使用点符号法来访问 `Item <n>`，其中 `<n>` 是项目的编号（第一个值位于位置 1）。例如，下面的代码从元组中提取第 2 个元素，将其赋值给变量并写入控制台：

```csharp
private static void GetProductData()
{
    var myTuple = (10, "Refrigerator", 432.43);
    Console.WriteLine(myTuple.Item2);
}
```

通过数字访问元组元素的替代方案是使用字段名。

## 21.4 字段名

## 创建元组时，你可以为每个值分配名称。当使用类型推断初始化元组时，字段名将放在每个值之前：

`(Count: 10, Product: "Refrigerator", Price: 432.43)`

一旦分配了字段名，就可以像下面所示访问对应的值：

```csharp
private static void GetProductData()
{
    var myTuple = (Count: 10, Product: "Refrigerator", Price: 432.43);
    Console.WriteLine(myTuple.Price);
    Console.WriteLine(myTuple.Product);
    Console.WriteLine(myTuple.Count);
}
```

应用程序运行时将出现以下输出：
```
Price = 432.43
```

## 21.5 从方法返回元组

元组对于从方法返回多个结果特别别有用。例如，假设我们需要的不是显示信息，而是让 `GetProductData()` 方法返回数据。为了实现这一点，需要在方法声明中包含元组的类型：

```csharp
private static (int, string, double) GetProductData()
{
    return (10, "Refrigerator", 432.43);
}
```

或者，可以将单个值放在 `return` 语句后的括号中：

```csharp
private static (int, string, double) GetProductData()
{
    return (10, "Refrigerator", 432.43);
}
```

调用时，返回的元组可以赋值给变量，并使用点符号访问：

```csharp
static void Main(string[] args)
{
    var myTuple = GetProductData();
    Console.WriteLine($"Price = {myTuple.Item1}");
    Console.WriteLine($"Product = {myTuple.Item2}");
    Console.WriteLine($"Quantity = {myTuple.Item3}");
}
```

如果你喜欢使用字段名而不是默认的 `Item` 名称，一种方法是包含字段名和类型：

```csharp
static void Main(string[] args)
{
    (int Count, string Product, double Price) myTuple = GetProductData();
    Console.WriteLine($"Price = {myTuple.Price}");
    Console.WriteLine($"Product = {myTuple.Product}");
    Console.WriteLine($"Quantity = {myTuple.Count}");
}
```

到目前为止，将元组值赋值给命名变量的最方便方法是使用类型推断：

`var (count, product, price) = GetProductData();`

使用这种方法，我们可以直接访问这些变量，而无需先从元组中提取它们：

```csharp
static void Main(string[] args)
{
    var (count, product, price) = GetProductData();
    Console.WriteLine($"Price = {price}");
    Console.WriteLine($"Product = {product}");
    Console.WriteLine($"Quantity = {count}");
}
```




除了从方法返回元组结果外，你还可以将元组传递给方法。一个设计为接收示例元组作为参数的方法可以声明如下：

```csharp
public static void DisplayProductData((int, string, double) productTuple)
{

}
```

或者，也可以为元组值分配字段名称：

```csharp
public static void DisplayProductData((int count, string description,
                                        double price) productTuple)
{
}
```

一旦声明方法，我们可以多种方式向其传递元组。一种方案是通过字面量值直接传递给方法：

```csharp
DisplayProductData((20, "Water filter", 29.99));
```

另一种方案自然是创建一个元组对象并将其传递给方法：

```csharp
var myTuple = (20, "Water filter", 29.99);
DisplayProductData(myTuple);
```

修改 `Program.cs` 文件以添加 `DisplayProductData()` 方法并向其传递元组参数：

```csharp
static void Main(string[] args)
{
    var myTuple = GetProductData();
    DisplayProductData(myTuple);
}

public static void DisplayProductData((int, string, double) productTuple)
{
    var (count, product, price) = productTuple;
    Console.WriteLine($"Price = {price}");
    Console.WriteLine($"Product = {product}");
    Console.WriteLine($"Quantity = {count}");
}
```

运行程序并验证产品信息是否在控制台中显示。

## 21.7 知识测试

点击下方的链接或扫描二维码，以测试你对 C# Tuple 类型的知识和理解程度：

[`www.answertopia.com/pxci`](https://www.answertopia.com/pxci)

![](img/image-AG3YT80V.jpg)

## 21.8 总结

C# 元组允许我们临时地将多个值分组到单个实体中。一旦声明，元组就可以用于从方法返回一组结果值，或者在单个参数内在方法之间传递多个参数值。元组支持大多数 C# 数据类型（包括自定义对象），并且其项不需要是匹配的类型。我们可以通过项目编号和字段名访问元组项，或者直接将它们赋值给命名变量。

## 22. C#

### 命名空间

在前面的章节中，我们详细涵盖了面向对象的 C# 编程。我们学习了如何使用类和结构来组织代码，从而生成组织良好的的可重用代码。在目前使用的许多代码示例中，我们看到了命名空间声明。现在我们已经理解了面向对象编程，准备好去发现什么是命名空间、它们为什么存在以及如何使用它们。

## 22.1 理解作用域

在讨论命名空间之前，我们首先需要理解与编程语言相关的作用域概念。作用域定义了类声明、方法和变量等实体对于当前作用域之外的代码是否可见可访问。在查看 C# 循环时，我们简要提到过作用域。例如，在 `for` 循环体内声明的变量只属于循环的作用域，在循环执行之前或之后不存在：

```csharp
// 变量 myCounter 尚未存在
for (int i = 0; i < 10; i++)
{
    int myCounter = 0; // 在 for 循环作用域内创建了 myCounter 变量
    myCounter += i;
}
// 循环退出后，变量 myCounter 现在离开了作用域并消失
```

同样，类方法和属性位于它们声明所在的类的作用域内，并且只能通过引用包含它的类来访问。在下面的示例中，我们只能通过引用 `MyClass` 来访问 `IncrementCounter()` 方法：

```csharp
class MyClass
{
    static int myCountr = 0;
    public static void IncrementCounter() {
        myCounter++;
    }
}

MyClass.IncrementCounter();
```

作用域允许我们声明类和结构，而不担心一个类中的方法名可能与其他类中的方法冲突。例如，以下类中相同的方法名不会冲突，因为它们属于不同的作用域：

```csharp
class MyClass
{
    static int myCounter = 0;
    public static void IncrementCounter() {
        myCounter++;
    }
}

class MyOtherClass
{
    static int myCounter = 0;
    public static void IncrementCounter() {
        myCounter++;
    }
}
```

然而，当类和结构等实体本身具有冲突的名称时，就会出现问题。如果上述两个类都命名为 `MyClass`，那么解决方案是使用 `命名空间`。

## 22.2 命名空间概述

与类和结构一样，命名空间提供了一个额外的组织层。正如我们看到的，一个项目包含类和结构。特别是在大型项目中，作用域内声明的名称可能会与内置类发生冲突。下面的示例将触发冲突：

```csharp
class A {
    Console.WriteLine("First");
}

class A {
    Console.WriteLine("Second");
}
```

命名空间允许将代码组织到独立的作用域中，以便名称不冲突。

### 22.3 创建命名空间项目

在本章的剩余部分，启动 VS Code，打开你的“C# Essentials”文件夹，并创建一个名为 `NamespaceDemo` 的新 .NET 项目。在资源管理器中找到新项目，编辑 `Program.cs` 文件，并将现有代码替换为：

```csharp
class A {
    Console.WriteLine("First");
}

class A {
    Console.WriteLine("Second");
}

namespace SampleApp {
    internal class Program {
        static void Main(string[] args) {
        }
    }
}
```

此时，编辑器将报告以下错误：`The namespace '<global>' already contains a definition for 'A'`。这告诉我们两个类都位于相同的命名空间中。

## 22.4 声明命名空间

使用 `namespace` 关键字后跟名称和封装成员的大括号来声明命名空间。为了解决命名冲突，我们可以将第二个 `A` 声明放在单独的命名空间中，将第一个留在全局命名空间：

```csharp
class A {
    Console.WriteLine("First");
}

namespace DemoSpace {
    class A {
        Console.WriteLine("Second");
    }
}
```

进行上述更改后，重复定义的错误应该会被解决：

![](img/image-WOHCDJ5M.png)
图 22-2

单个源文件可以包含多个命名空间。修改示例以包含两个命名空间如下：

```csharp
namespace DemoSpaceOne
{
    class A
    {
```





```csharp
Console.WriteLine("First ClassA OpenFile()");

        }
    }
}

namespace DemoSpaceTwo
{
    class ClassA
    {
        public static void OpenFile()
        {
            Console.WriteLine("Second ClassA OpenFile()");
        }
    }
}
```

通过此更改，我们的项目现在包含了三个命名空间（除了 `Console.WriteLine()` 调用所需的 `System` 命名空间外）：`DemoSpaceOne`、`DemoSpaceTwo` 以及全局命名空间：

![](img/image-GBU31OYY.png)

图 22-3

## 22.5 访问命名空间成员

由于两个 `ClassA` 定义位于不同的命名空间中，我们需要一种方法告诉编译器我们正在访问哪一个类。使用点表示法（dot notation），我们可以通过引用相应的命名空间来区分这些类。按如下方式修改 `Main()` 方法以调用每个 `ClassA` 实现中的 `OpenFile()` 方法：

```csharp
namespace SampleApp
{
    internal class Program
    {
        static void Main(string[] args)
        {
            DemoSpaceOne.ClassA.OpenFile();
            DemoSpaceTwo.ClassA.OpenFile();
        }
    }
}
```

编译并运行该程序，验证终端中是否出现了下列表输出：

```
First ClassA OpenFile()
Second ClassA OpenFile()
```

## 22.6 命名空间与“using” 关键字

点表示法的替代方案是 `using` 关键字，它会告诉编译器在没有显式命名空间声明的情况下默认使用哪个命名空间。例如，当在 `Main()` 方法中未指定命名空间时，以下更改将默认使用 `DemoSpaceTwo`：

```csharp
using DemoSpaceTwo;

namespace DemoSpaceOne
{
.
.
}

namespace DemoSpaceTwo
{
.
.
}

namespace SampleApp
{
    internal class Program
    {
        static void Main(string[] args)
        {
            ClassA.OpenFile();
        }
    }
}
```

当程序运行时，将调用属于 `DemoSpaceTwo` 命名空间的 `ClassA.OpenFile()` 方法：

```
Second ClassA OpenFile()
```

然而，要访问 `DemoSpaceOne` 的 `OpenFile()` 方法，我们仍然必须如下所示覆盖由 `using` 语句指定的默认命名空间：

```csharp
using DemoSpaceTwo;

static void Main(string[] args)
{
    ClassA.OpenFile() // 默认指向 DemoSpaceTwo
    DemoSpaceOne.ClassA.OpenFile(); // 显式选择 DemoSpaceOne
}
```

## 22.7 嵌套命名空间

命名空间可以在其他命名空间内部声明，以创建嵌套层次结构。要体验嵌套命名空间，请在 `Program.cs` 文件中添加以下命名空间声明：

```csharp
namespace DemoOne
{
    namespace DemoTwo
    {
        namespace DemoThree
        {
            class ClassC
            {
                public static string message = "DemoThree message";
            }
        }
    }
}
```

要访问 `message` 字段，我们需要引用包含它的每一个命名空间：

```csharp
static void Main(string[] args)
{
    var message = DemoOne.DemoTwo.DemoThree.ClassC.message;
    Console.WriteLine(message);
}
```

当程序运行时，输出现在将是 `DemoThree message`。

## 22.8 别名与命名空间别名运算符

C# 允许使用 `using` 关键字为命名空间引用分配别名。使用这种技术，我们可以如下为我们的嵌套命名空间分配别名：

```csharp
using DemoSpaceTwo;
using MyAlias = DemoOne.DemoTwo.DemoThree;
.
.
```

要使用别名访问 `ClassC`，我们使用别名运算符（`::`）：

```csharp
static void Main(string[] args)
{
    ClassA.OpenFile();
    DemoSpaceOne.ClassA.OpenFile();
    var message = MyAlias::ClassC.message;
    Console.WriteLine(message);
}
```

注意，别名声明并没有覆盖我们的 `using DemoSpaceTwo` 语句，我们仍然可以访问第二个 `ClassA` 的 `OpenFile()` 方法：

```csharp
ClassA.OpenFile();
```

别名运算符也可以用于显式访问全局命名空间中的对象。考虑以下类代码示例，该类既位于全局命名空间，又位于自定义命名空间中：

```csharp
class MyString
{
    public static string text = "Global string";
}

namespace SampleApp
{
    class MyString
    {
        public static string text = "Local string";
    }
    internal class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine(MyString.text);
        }
    }
}
```

当上述代码执行时，将显示来自本地 `MyString` 类的 `text`。要访问全局类，我们可以使用别名运算符指定全局命名空间：

```csharp
static void Main(string[] args)
{
    Console.WriteLine(MyString.text);
    Console.WriteLine(global::MyString.text);
}
```

## 22.9 文件作用域命名空间

如果源文件的全部内容属于同一个命名空间，可以使用文件作用域声明。在以下代码中，`ClassA` 和 `ClassB` 都声明在 `FileScopeSpace` 命名空间中：

```csharp
namespace FileScopeSpace;

class ClassA

class ClassB
```

文件作用域命名空间不能包含其他命名空间。因此，以下代码是无效的：

```csharp
namespace FileScopeSpace;

class ClassA
{
    public static void OpenFile()
    {
        Console.WriteLine("Class A OpenFile()");
    }
}

namespace SpaceOne // 无效的命名空间声明
{
    class ClassB
    {
        public static void OpenFile()
        {
            Console.WriteLine("Class B OpenFile()");
        }
    }
}
```

## 22.10 测试

点击下方链接或扫描二维码测试你对命名空间的知识和理解：

[`www.answertopia.com/bkx3`](https://www.answertopia.com/bkx3)

![](img/image-F998BJU.jpg)

## 22.11 总结

在本章中，我们探索了 C# 命名空间并学会了如何使用它们组织项目并避免冲突。文件作用域命名空间允许整个源文件被指定属于同一个命名空间。

## 23. C#

### 异常处理

在完美的世界里，C# 代码永远不会遇到错误。由于我们并不生活在完美的世界里，因此无法保证代码在执行时不会发生错误（通常称为异常）。因此，确保代码能够顺利处理可能出现的异常至关重要。

本章介绍了使用 C# 进行异常处理，了异常类型、异常如何抛出以及如何使用 `try-catch` 语句处理异常等主题。





## 23.2 创建 ExceptionDemo 项目

启动 VS Code，打开你的“C# Essentials”工作区文件夹，并创建一个名为 `ExceptionDemo` 的 .NET 控制台应用程序。项目准备好后，按照以下方式修改 `Program.cs` 文件：

```csharp
namespace ExceptionDemo
{
    internal class Program
    {
        static void Main(string[] args)
        {
        }
    }
}
```

该项目是一个控制电机的假设应用程序。在通电诊断期间，该程序会读取当前电压，如果超过 500 伏，则防止电机启动。在 `Program.cs` 文件中，添加一个执行电压检查的方法并在 `Main()` 方法中调用它：

```csharp
namespace ExceptionDemo
{
    internal class Program
    {
        static void Main(string[] args)
        {
            VoltageCheck(501);
        }
        private static void VoltageCheck(int voltage)
        {
            if (voltage > 500)
            {
                Console.WriteLine("Voltage overload.");
            }
            else
            {
                Console.WriteLine("Voltage is safe.");
            }
        }
    }
}
```

运行该程序并检查控制台中是否出现了电压过载消息：

`Voltage overload.`

电压过载是一个严重问题，因此我们不想仅仅显示一条消息并希望用户不要启动电机。相反，我们希望强制程序采取预防措施。为了做到这一点，我们将抛出一个异常。

## 23.3 抛出异常

抛出异常的第一步是选择异常类型。正如我们之前提到的，异常可以使用许多内置类型之一或你创建的自定义类型来抛出。我们将在本章节后面的部分介绍自定义异常类型，因此现在我们将使用 `ArgumentOutOfRangeException` 类型。这种异常类型通常在传递给方法的参数超出接受范围时抛出（在我们的案例中，是电压读数超过 500 伏）。

接下来，创建并初始化异常类型的实例。所有异常类型都必须初始化一个解释问题原因的消息。某些类型（包括 `ArgumentOutOfRangeException`）还需要指定引起异常的参数名称（在我们的案例中，是 `voltage`）。利用这些信息，我们可以如下创建一个新异常：

`ArgumentOutOfRangeException voltageException = new(nameof(voltage), "Voltage exceeds safety parameters.");`

使用 `throw` 语句后跟异常对象来抛出异常，如下：

```csharp
throw voltageException;
```

在上面的示例中，我们分两个步骤创建和抛出异常。然而，这个序列通常在单次操作中完成：

```csharp
throw new ArgumentOutOfRangeException(nameof(voltage), "Voltage exceeds safety parameters.");
```

修改 `VoltageCheck()` 方法以抛出异常，如下：

```csharp
private static void VoltageCheck(int voltage)
{
    if (voltage > 500)
    {
        throw new ArgumentOutOfRangeException(nameof(voltage),
                                            "Voltage exceeds safety parameters.");
    }
    else
    {
        Console.WriteLine("Safe Voltage");
    }
}
```

参考控制台，将出现以下输出：

`Unhandled exception. System.ArgumentOutOfRangeException: Voltage exceeds safety parameters. (Parameter 'voltage')`
`   at ExceptionDemo.Program.VoltageCheck(Int32 voltage) in Program.cs:line`

## 23.4 处理异常

在 C# 中，异常使用 `try-catch` 语句进行处理。为了防止程序崩溃，我们必须在以下位置添加 `try`：

```csharp
static void Main(string[] args)
{
    try
    {
        VoltageCheck(501);
    }
    catch (ArgumentOutOfRangeException)
    {
        Console.WriteLine("Voltage overload");
    }
}
```

到目前为止，我们已经实现了 `catch` 块。也可以访问异常对象，例如：

```csharp
try
{
    VoltageCheck(501);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}
```

当程序运行时，将出现以下输出：

`Voltage overload.`

接下来的示例代码：

```csharp
try
{
    VoltageCheck(501);
}
catch (ArgumentOutOfRangeException ex)
{
    Console.WriteLine("Voltage overload");
}
```

这对于捕获多种类型非常有用。例如：

```csharp
try
{
    VoltageCheck(501);
}
catch (ArgumentOutOfRangeException)
{
    Console.WriteLine("Voltage overload");
}
else if (NullException)
{
    Console.WriteLine("Null reference");
}
```

## 23.5 使用 `when` 创建异常过滤器

在上面的示例中，我们使用 `when` 来控制异常。在 catch 块中使用 `when` 的语法为：

```csharp
try
{
}
catch (exception) when (boolean)
{
}
```

只有当 `when` 后面的布尔表达式求值为真时，catch 块中的代码才会执行。这对于捕获特定类型特别有用。例如，下面的代码：

```csharp
catch (Exception ex) when (ex is ArgumentOutOfRangeException || ex is NullException)
```

异常过滤器可以包含任何布尔表达式，无论是否带有类型匹配。下面的 catch 块仅在异常类型为 `ArgumentException` 且 `motorTemp` 超过 102 时才会执行：

```csharp
try
{
    VoltageCheck(501);
}
catch (Exception ex) when (ex is ArgumentOutOfRangeException && motorTemp > 102)
```

## 23.6 使用 `finally` 块

`finally` 块的目的是在 `try-catch` 语句结束之前指定执行的代码，通常用于执行清理任务，例如：

```csharp
try
{
    VoltageCheck(501);
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
}
finally
{
    Console.WriteLine("Resetting system.");
}
```

## 23.7 使用 `try-finally` 语句

根据之前的经验，我们知道未处理的异常会导致程序崩溃，但尚未解释异常在哪里被捕获。本章涵盖的示例暗示异常必须在发生的地方使用 `try-catch` 语句进行处理。但在实践中，情况并非如此。在深入探讨此主题之前，将运行程序的执行路径视为方法调用的层次结构，从 `Main()` 方法开始是有帮助的。

考虑这种情况：`Main()` 方法调用 `Method A`，随后它又调用 `Method B` 和 `Method C`。然后 `Method C` 调用 `Method D`，以此类推。这种方法调用的层次结构被称为调用树或调用层次结构。在图示中，我们的理论调用层次结构可能如图 23-1 所示：

![](img/image-N29EWYM5.png)

图 23-1

假设在 `Method D` 中抛出了异常。该异常将沿着调用层次结构向上传播，直到被处理。如果异常在到达 `Main()` 方法之前未被捕获，则程序将会崩溃。这意味着即使异常是在 `Method D` 中抛出的，我们也可以在包括 `Main()` 在内的任何直接祖先方法中处理它，以防止程序崩溃。





为了亲身体验，请在 `Main()` 和 `VoltageCheck()` 方法之间添加一个名为 `StartMotor()` 的中间方法，并移除 `try-catch` 语句：

```csharp
namespace ExceptionDemo
{
    internal class Program
    {
        static void Main(string[] args)
        {
            StartMotor();
        }
        private static void StartMotor()
        {
            VoltageCheck(501);
            Console.WriteLine("Clean up after check.");
        }
        private static void VoltageCheck(int voltage)
        {
            if (voltage > 500)
            {
                throw new ArgumentOutOfRangeException(nameof(voltage),
                    "Voltage exceeds safety parameters.");
            }
            else
            {
                Console.WriteLine("Safe Voltage");
            }
        }
    }
}
```

由于异常在三个方法中均未被捕获，应用程序在运行时将会崩溃。然而，我们可以通过在 `VoltageCheck()`、`StartMotor()` 或 `Main()` 中添加 `try-catch` 语句来捕获错误。在本示例中，请使用 `try-catch` 语句在 `Main()` 方法内部调用 `StartMotor()`：

```csharp
static void Main(string[] args)
{
    try
    {
        StartMotor();
    }
    catch (Exception ex) {
        Console.WriteLine(ex.Message);
    }
}
```

重新运行程序，确认异常已向上传播到 `Main()` 方法并被捕获处理：

`Voltage exceeds safety parameters. (Parameter 'voltage')`

请注意，上述控制台输出没有执行电压检查后的清理操作。按照目前的实现方式，`StartMotor()` 将无法感知 `VoltageCheck()` 抛出了异常，`StartMotor()` 中 `VoltageCheck()` 之后的任何代码都将被跳过，控制权将立即返回到 `Main()`。但假设 `StartMotor()` 无论是否抛出异常都需要在电压检查后执行清理工作。我们可以使用 `try-finally` 语句来实现这种行为：

```csharp
private static void StartMotor()
{
    try
    {
        VoltageCheck(501);
    }
    finally
    {
        Console.WriteLine("Clean up whether or not voltage is safe.");
    }
}
```

再次编译并运行程序，验证即使在抛出异常时也会发生清理工作：

`Clean up whether or not voltage is safe.`
`Voltage exceeds safety parameters. (Parameter 'voltage')`

## 23.8 重新抛出异常

有时，异常需要在调用层次结构的多个层级进行捕获。通过在捕获异常后将其重新抛出来实现，使其能够继续在层次结构中向上传递。如下所示，在 `catch` 体中使用 `throw` 语句重新抛出异常：

```csharp
static void Main(string[] args)
{
    try
    {
        StartMotor();
    }
    catch (Exception ex) {
        Console.WriteLine("Caught in Main() " + ex.Message);
    }
}
private static void StartMotor()
{
    try
    {
        VoltageCheck(501);
    }
    catch (Exception ex) {
        Console.WriteLine("Caught in StartMotor " + ex.Message);
        throw;
    }
    finally
    {
        Console.WriteLine("Clean up or not voltage is safe.");
    }
}
```

运行程序并检查控制台以验证重新抛出有效，且异常被两个方法都捕获：

`StartMotor(): Voltage exceeds safety parameters. (Parameter 'voltage')`
`Clean up or not voltage is safe.`
`Main(): Voltage exceeds safety parameters. (Parameter 'voltage')`

## 23.9 创建异常类型

到目前为止，本章节一直使用内置异常类型来演示如何在 C# 中抛出和捕获异常。然而，有时创建自定义异常比使用预定义类型更有意义。自定义类型派自 `Exception` 类，并根据需要应包含构造函数和参数。类型名称也应以“Exception”结尾。以下代码为我们应用程序中的高电压错误声明了一个自定义异常：

```csharp
class HighVoltageException : Exception
{
    public HighVoltageException()
    {
    }
    public HighVoltageException(string message)
        : base(message)
    {
    }
    public HighVoltageException(string message, Exception inner)
        : base(message, inner)
    {
    }
}
```

一旦声明，可以按如下方式抛出异常：

`throw new HighVoltageException("Voltage exceeds safety parameters.");`

`HighVoltageException` 类型不包含属性，因此仅可以使用消息字符串创建实例：

`throw new HighVoltageException("Voltage exceeds safety parameters.");`

我们还可以扩展类型声明，以包含一个属性，用于记录异常发生时的电压水平：

```csharp
class HighVoltageException : Exception
{
    public int Volts;
    public HighVoltageException()
    {
    }
    public HighVoltageException(string message)
        : base(message)
    {
    }
    public HighVoltageException(string message, Exception inner)
        : base(message, inner)
    {
    }
    public HighVoltageException(string message, int Volts)
        : base(message)
    {
        this.Volts = Volts;
    }
}
```

现在可以使用消息字符串和触发异常的电压值来创建一个 `HighVoltageException` 实例：

```csharp
private static void VoltageCheck(int voltage)
{
    if (voltage > 500)
    {
        throw new HighVoltageException("Voltage exceeds safety parameters.", voltage);
    }
    else
    {
        Console.WriteLine("Safe Voltage");
    }
}
```

异常属性可以像消息属性一样在 `catch` 块中访问。在下面的示例中，电压属性包含在通知文本中并据此做出决策：

```csharp
try
{
    StartMotor();
}
catch (HighVoltageException ex)
{
    Console.WriteLine(ex.Message);
    Console.Write("Current voltage: {ex.Volts}");
    if (ex.Volts < 510)
    {
        // 等待并重试
    }
    else
    {
        // 关键。关闭系统
    }
}
```

## 23.10 测试

点击下方链接或扫描二维码以测试你对 C# 异常处理的知识和理解：

[`www.answertopia.com/hy8t`](https://www.answertopia.com/hy8t)

## 23.11 总结

异常处理确保程序能够有效地处理错误，通过捕获、处理和响应问题避免崩溃。当方法无法继续执行时，会“抛出”异常。每个异常都有特定的类型，提供了有关错误的性质的信息。除了预定义的异常类型（如 `ArgumentOutOfRangeException`），有时也可以创建自定义异常类型。使用 `try-catch` 块处理异常。将可能抛出异常的代码放在 `try` 块中，而 `catch` 块包含抛出异常时执行的代码。`catch` 块可以访问异常详细信息，在可能发生多种类型异常的情况下，可以分别处理特定的异常类型。`finally` 块也可用于执行代码（例如清理资源），无论是否发生异常。

## 24 C# 中的异步编程

异步编程允许软件同时执行多个任务。这意味着下载图像或处理大量数据等任务可以比顺序执行更快完成。多任务处理通过在后台执行耗时操作而不影响应用程序的响应速度，提供了更流畅的用户体验。





在本章中，我们将探索 C# 的异步特性，并解释如何使用这些特性将多任务支持整合到你的项目中。

## 24.1 线程概述

线程是现代 CPU 的基础特性，也是操作系统中多任务处理的关键。虽然 CPU 可以处理许多线程，但在给定时间内能够并行运行的实际线程数限于 CPU 核心数（通常取决于 CPU 型号在 4 到 16 个核心之间）。当线程数量超过可用的 CPU 核心数时，操作系统将使用线程调度来决定这些线程如何在可用核心之间进行共享。

线程类似于运行在主进程内部的小型进程。它们允许应用程序内部出现并行执行的现象，但直接在代码中管理它们可能是一个复杂且不可预测的过程。然而，C# 异步特性的伟大之处在于，它们在背后使用线程，并为你处理了所有的复杂性。

## 24.2 主线程

当应用首次启动时，运行时系统通常会创建一个单一线程，应用默认在该线程中运行。应用中任何使用主线程执行耗时任务的代码都会导致整个应用程序看起来像锁死了一，直到任务完成。可以通过将要执行的任务启动在单独的线程中来避免这种情况，允许主线程不受干扰地继续执行其他任务。

## 24.3 C# 中的异步编程

C# 的异步支持由任务异步编程模型（TAP）提供，该模型允许以安全、逻辑且易于编写和理解的方式执行执行。换句话说，异步 C# 代码是从上到下顺序编写的，与同步代码非常相似，使其易于理解逻辑流。

本章介绍 C# 异步编程，深入涵盖用于高效并行执行的关键概念和技术。

## 24.4 创建 AsyncDemo 项目

启动 VS Code，打开你的“C# Essentials”工作空间文件夹，创建一个名为 `AsyncDemo` 的新 .NET 控制台应用项目。

## 24.5 同步代码

在探索异步编程之前，我们先来看同步代码执行的示例。首先打开 `Program.cs` 文件并进行如下修改：

```csharp
namespace AsyncDemo
{
    internal class Program
    {
        static void Main(string[] args)
        {
        }
        private static string ProcessFile(string filename)
        {
            Console.WriteLine($"Start {filename} at {DateTime.Now}");
            Task.Delay(6000).Wait();
            return filename;
        }
    }
}
```

`ProcessFile()` 方法在调用 `Task.Delay()` 和 `Wait()` 方法之前输出一个开始时间戳，以模拟一个阻塞当前线程的 6 秒文件处理任务。延迟结束后，方法返回已完成的文件。

接下来，我们想从 `Main()` 方法中多次调用 `ProcessFile()`。在此，我们还将输出开始时间戳并使用 C# 的 `Stopwatch` 诊断类来记录方法调用的总执行时间：

```csharp
using System.Diagnostics;
namespace AsyncDemo
{
    internal class Program
    {
        static void Main(string[] args)
        {
            Stopwatch stopwatch = Stopwatch.StartNew();
            Console.WriteLine("\n=== Before async task calls ===\n");
            string filename1 = ProcessFile("file1.txt");
            Console.WriteLine($"End {filename1} at {DateTime.Now}\n");
            string filename2 = ProcessFile("file2.txt");
            Console.WriteLine($"End {filename2} at {DateTime.Now}\n");
            string filename3 = ProcessFile("file3.txt");
            Console.WriteLine($"End {filename3} at {DateTime.Now}\n");
            Console.WriteLine("=== After async task calls ===");
            stopwatch.Stop();
            Console.WriteLine($"Elapsed time: {stopwatch.Elapsed.Seconds} seconds");
        }
    }
}
```

运行应用并检查输出：

```=== Before async task calls ===

Start file1.txt at 10/27/2023 10:00:00 AM
End file1.txt at 10/27/2023 10:00:06 AM

Start file2.txt at 10/27/2023 10:00:06 AM
End file2.txt at 10/27/2023 10:00:12 AM

Start file3.txt at 10/27/2023 10:00:12 AM
End file3.txt at 10/27/2023 10:00:18 AM
=== After async task calls ===
Elapsed time: 18 seconds
```

从上面的输出中可以看出，三次 `ProcessFile()` 调用是顺序执行的，导致了 18 秒的结果。将 `ProcessFile()` 转换为异步方法应该将总时间从 18 秒减少到 6 秒。

## 24.6 理解 Task 类

C# 中的异步操作由 `Task` 对象表示。正如我们之前看到的，我们可以直接调用 `Task` 方法，例如 `Delay()`：

```csharp
Task.Delay(6000);
```

上述代码将启动一个异步的 6 秒延迟。换句话说，虽然延迟会执行，但它将在后台进行。为了让执行阻塞当前线程，我们调用了 `Task` 的 `Wait()` 方法：

```csharp
Task.Delay(6000).Wait();
```

## 24.7 异步方法

异步执行可以应用于方法、Lambda 和匿名函数，并通过 `async` 关键字和指定 `Task` 返回类型进行声明。C# 命名规范还建议（并非强制）方法名以 `Async` 结尾。根据这些要求，我们可以对 `ProcessFile()` 方法进行如下修改：

```csharp
private static async Task<string> ProcessFileAsync(string filename)
{
    Console.WriteLine($"Start {filename} at {DateTime.Now}");
    await Task.Delay(6000);
    return filename;
}
```

我们已经声明该方法是异步的，并返回一个包含 `string` 结果参数的 `Task` 对象。注意，由于我们现在在 `async` 方法中工作，我们已经从调用 `Task` 对象的 `Wait()` 方法切换到使用 `await` 运算符。

## 24.8 引入 await 运算符

C# 异步执行的基础是 `Task` 类和 `await` 运算符。`await` 运算符告诉系统挂起调用方法的执行，直到相应的异步操作完成并返回。

通过 `AsyncDemo` 示例，我们知道 `Main()` 方法连续三次调用文件处理方法，并且每次调用都必须等待上一个调用完成后才能执行。除了这种处理多个文件的方式效率低下外，三次调用之后的任何代码在最后一次完成之前都无法执行，这实际上锁定了应用程序。在所有情况下，在等待从 `ProcessFileAsync()` 方法调用返回结果时，`Main()` 方法可能还有正在执行的其他任务。

使用 `Task` 对象和 `await`，我们可以并行运行三个文件处理操作，并在等待异步调用结果的同时，允许 `Main()` 方法中的其他代码运行。




作为第一步，我们将演示为什么异步执行同时需要 `Task` 对象和 `await` 操作符。然而，首先需要注意的一点是，异步方法通常只能在其他异步方法的范围内被调用（尽管正如我们在本章稍后部分将看到的，`Task` 对象可以用作提供同步和异步代码之间的桥梁）。基于此，进行以下更改以将 `Main()` 声明为异步方法：

```csharp
static async Task Main(string[] args)
{
    Stopwatch stopwatch = Stopwatch.StartNew();
// ...
```

接下来，修改异步调用以使用 `await` 操作符，如下所示：

```csharp
static async Task Main(string[] args)
{
    Stopwatch stopwatch = Stopwatch.StartNew();
    Console.WriteLine("\n=== Before async task calls ===\n");
    string filename1 = await ProcessFileAsync("file1.txt");
    Console.WriteLine($"End {filename1} at {DateTime.Now}\n");
    string filename2 = await ProcessFileAsync("file2.txt");
    Console.WriteLine($"End {filename2} at {DateTime.Now}\n");
    string filename3 = await ProcessFileAsync("file3.txt");
    Console.WriteLine($"End {filename3} at {DateTime.Now}");
    Console.WriteLine("\n=== After async tasks calls ===\n");
    stopwatch.Stop();
    TimeSpan timeSpan = stopwatch.Elapsed;
    Console.WriteLine($"Elapsed time: {timeSpan.Seconds} seconds\n");
}
```

一旦完成修改，运行应用程序并检查控制台输出，其结果类似于：：

```
=== Before async task calls ===
Start file1.txt at 9/25/2024 9:53:46 AM
End file1.txt at 9/25/2024 9:53:52 AM
Start file2.txt at 9/25/2024 9:53:52 AM
End file2.txt at 9/25/2024 9:53:58 AM
Start file3.txt at 9/25/2024 9:53:58 AM
End file3.txt at 9/25/2024 9:54:04 AM
=== After async tasks calls ===
Elapsed time: 18 seconds
```

尽管我们已经将文件处理方法变为异步并使用了 `await` 操作符，但控制台输出显示任务仍然是在按顺序执行。通过将 `await` 操作的结果直接赋值给 `string` 变量，我们实际上是承诺等待直到结果返回，从而强制代码以同步方式执行。

为了解决这个问题，我们需要实现以下执行流：

1. 应用程序启动。
2. `Main()` 调用异步方法。
3. 当异步任务在后台运行时，`Main()` 继续执行。
4. 在完成其他工作后，`Main()` 在等待异步任务的结果时挂起。
5. 异步任务完成并返回结果。
6. `Main()` 恢复执行。

挑战在于获取异步任务的引用，以便稍后用于等待结果。我们通过存储异步方法返回的 `Task` 对象，并在代码后部分使用它们来等待结果来实现这一目标。为了看到实际效果，请对 `Main()` 方法进行以下更改：

```csharp
static async Task Main(string[] args)
{
    Stopwatch stopwatch = Stopwatch.StartNew();
    Console.WriteLine("\n=== Before async task calls ===\n");
    Task<string> task1 = ProcessFileAsync("file1.txt");
    Task<string> task2 = ProcessFileAsync("file2.txt");
    Task<string> task3 = ProcessFileAsync("file3.txt");
    Console.WriteLine("=== After async tasks calls ===\n");
    string filename1 = await task1;
    Console.WriteLine($"End {filename1} at {DateTime.Now}");
    string filename2 = await task2;
    Console.WriteLine($"End {filename2} at {DateTime.Now}");
    string filename3 = await task3;
    Console.WriteLine($"End {filename3} at {DateTime.Now}\n");
    stopwatch.Stop();
    TimeSpan timeSpan = stopwatch.Elapsed;
    Console.WriteLine($"Elapsed time: {timeSpan.Seconds} seconds");
}
```

重新运行应用程序并检查控制台输出：

```
=== Before async task calls ===
Start file1.txt at 9/25/2024 1:59:16 PM
Start file2.txt at 9/25/2024 1:59:16 PM
Start file3.txt at 9/25/2024 1:59:16 PM
=== After tasks calls ===
End file1.txt at 9/25/2024 1:59:22 PM
End file2.txt at 9/25/2024 1:59:22 PM
End file3.txt at 9/25/2024 1:59:22 PM
Elapsed time: 6 seconds
```

尽管我们已经将文件处理方法变为异步并使用了 `await` 操作符，但控制台输出显示任务仍然是在按顺序执行。通过将 `await` 操作的结果直接赋值给 `string` 变量，我们实际上是承诺等待直到结果返回，从而强制代码以同步方式执行。

等待，让我重新检查提供的文本。似乎输入文本包含了一些重复或碎片化的部分。我将在保持请求的核心逻辑和结构的同时对其进行清理。

## 24.9 从同步函数进行异步调用

如之前所述，异步方法预计在异步上下文中被调用。然而，可以通过调用 `Task.Run()` 方法在同步上下文中启动异步任务。假设我们有一个名为 `SyncMethod()` 的同步方法，我们需要在其中调用一个异步方法，并尝试如下所示操作：

```csharp
private static void SyncMethod()
{
    await AsyncMethod();
}
```

上述代码将在代码编辑器中产生以下错误：`await` 操作符只能在异步方法中使用。考虑将此方法标记为 `async` 并将其返回类型更改为 `Task`。

我们仅有的选择是让 `SyncMethod()` 成为一个异步方法，或者使用 `Task.Run()` 方法启动任务。假设将 `SyncMethod()` 声明为异步方法不是可行方案，在这种情况下，代码需要更改如下：

```csharp
private static void SyncMethod()
{
    Task.Run(async () {
        await AsyncMethod();
    });
}
```

## 24.10 取消异步任务

激活的异步任务可以使用 `CancellationTokenSource` 类随时进行取消。`CancellationTokenSource` 实例包含一个唯一的 `CancellationToken` 对象，用于向任务发送取消请求。为了向 `AsyncDemo` 项目添加取消支持，首先对 `Main()` 方法进行以下更改：

```csharp
static async Task Main(string[] args)
{
    var tokenSource = new CancellationTokenSource();
    var cancellationToken = tokenSource.Token;
// ...
}
```

现在我们有了取消令牌，需要对 `ProcessFileAsync()` 方法进行更改，以便将其传递给执行 6 秒延迟的任务：

```csharp
private static async Task<string> ProcessFileAsync(string filename, CancellationToken cancellationToken)
{
    Console.WriteLine($"Start {filename} at {DateTime.Now}");
    await Task.Delay(6000, cancellationToken);
    return filename;
}
```

在我们可以添加发送取消请求的代码之前，还需要额外的步骤。按照目前的写法，当任务取消时应用程序将崩溃，控制台输出部分显示：

```
Unhandled exception. System.AggregateException: One or more errors occurred. (A task was canceled.)
   ---> System.Threading.Tasks.TaskCanceledException: A task was canceled.
   at System.Threading.Tasks.Task.GetExceptions(Boolean includeTaskCExceptions)
```

这里的问题是，当任务取消时，它会触发一个异常，如果应用程序没有正确处理该异常，会导致崩溃。此问题的解决方案是配置令牌在任务取消时抛出 `OperationCanceledException` 错误，然后使用 `try-catch` 语句优雅地处理该异常。





```csharp
Console.WriteLine($"Start {filename} at {DateTime.Now}");

try
{
    cancellationToken.ThrowIfCancellationRequested();
    await Task.Delay(6000, cancellationToken);
}
catch (OperationCanceledException)
{
    Console.WriteLine($"{filename} processing cancelled");
}
return filename;
```

在上面的示例中，我们只是输出了一条消息指示任务已取消的消息，但在实际应用中，这里可以采取步骤进行清理，例如删除临时文件或关闭网络连接。

最后一步是为用户提供取消异步任务的方法。我们通过调用 `CancellationTokenSource` 对象的 `Cancel()` 方法来实现这一点：

```csharp
tokenSource.Cancel();
```

为了演示取消文件处理任务，我们将在任务启动后添加代码，以便在按下键时取消任务，如下：

```csharp
static async Task Main(string[] args)
{
    var tokenSource = new CancellationTokenSource();
    var cancellationToken = tokenSource.Token;

    // ...

    Console.WriteLine("\n=== After async tasks calls ===\n");
    Console.Write("Press any key to cancel");
    Console.ReadKey();
    tokenSource.Cancel();
    Task.WaitAll(task1, task2, task3);
    // ...
}
```

重新运行程序，点击控制台窗口，并在 6 秒内按下任意键以取消任务。控制台输出应指示取消异常已被整洁处理，并且任务在完成工作之前已取消：

```text
=== Before async task calls ===
Start file1.txt at 9/26/2024 2:15:04 PM
Start file2.txt at 9/26/2024 2:15:04 PM
Start file3.txt at 9/26/2024 2:15:04 PM
=== After async tasks calls ===
Press any key to cancel
file3.txt processing canceled
file2.txt processing canceled
file1.txt processing canceled
End file1.txt at 9/26/2024 2:15:06 PM
End file2.txt at 9/26/2024 2:15:06 PM
End file3.txt at 9/26/2024 2:15:06 PM
Elapsed time: 1 seconds
```

## 24.11 知识测试

点击下方的链接或扫描二维码来测试你对 C# 异步编程的知识和理解：

[`www.answertopia.com/akfm`](https://www.answertopia.com/akfm)

![](img/image-KRY5XAC2.jpg)

## 24.12 总结

C# 中的异步编程使用 `Task` 类和 `await` 运算符来并行运行任务，提高性能和响应能力。`await` 运算符会挂起执行直到任务完成，允许其他代码并发运行。通过将同步方法转换为异步方法，可以同时执行多个任务，从而缩短整体执行时间。

要实现并发执行，请存储 `async` 方法返回的 `Task` 对象并在稍后等待其结果。异步任务的取消可以使用 `CancellationTokenSource` 对象的 `Cancel()` 方法实现。在取消任务时，应该采取适当的步骤处理异常，以防止程序崩溃。

## 25. 在 C# 中创建二维、三维数组和锯齿数组

数组并不是 C# 特有的。事实上，在 C# 引入之前，几乎每一种之前的编程语言和脚本语言都提供了对数组的支持。数组允许存储一组相同类型的值集合，并通过单个变量进行访问。数组变量中的每个项目都通过数组索引来访问。

C# 数组虽然很有用，但存在一些局限性。可能最重要的局限性是，一旦创建了数组，就无法增大或减小以容纳更多或更少的值。更动态灵活的集合存储能力将从“C# List 集合”章节开始介绍。

## 25.1 在 C# 中创建数组

C# 数组可以通过几种不同的方式创建。一种方法是声明数组但不使用任何值对其初始化。其语法如下：

```cs
type[] arrayname;
```

在上面的示例中，`type` 代表要存储在数组中的数据类型（例如 `string`、`int`、`decimal` 等）。方括号（`[]`）表示这是数组的声明，`arrayname` 是引用该数组的名称。

例如，我们可以如下声明一个名为 `myColors` 的字符串数组：

```cs
string[] myColors;
```

在这个示例中，我们声明了数组但没有给它分配任何值。在声明数组后赋值，请使用以下语法：

```cs
string[] myColors;
myColors = ["red", "green", "yellow", "orange", "blue"];
```

数组也可以通过简单放置逗号分隔的列表来初始化：

```cs
string[] myColors = ["red", "green", "yellow", "orange", "blue"];
```

另一个选项是在创建数组时指定数组的大小：

```cs
string[] myColors = new string[5];
```

这将为 5 个字符串元素留留空间。

## 25.2 多维数组

多维数组通过在方括号内放置逗号来声明。例如，声明一个二维数组：

```cs
char[,] myarray;
```

上述语法中的逗号（`,`）向 C# 表示这是一个二维数组。二维数组的初始化如下：

```cs
char[,] myarray = {
    {'a', 'b', 'c'},
    {'d', 'e'}
};
```

这创建了一个具有行和列的多维数组。也可以在创建数组时指定数组的：

```cs
char[,] myarray = new char[2, 3];
```

三维数组通过使用两个逗号来声明：

```cs
char[,,] myarray;
```

以下内容将初始化三维数组：

```cs
char[,,] myarray = {
    {
        {'a', 'b', 'c'},
        {'d', 'e', 'f'}
    },
    {
        {'g', 'h', 'i'},
        {'j', 'k', 'l'}
    }
};
```

三维数组本质上是一个每个元素都是二维数组的数组。在上面的声明中，该数组包含两个数组，每个数组包含三个元素。

也可以在声明数组时指定维度：

```cs
char[,,] myarray = new char[2, 2, 3] {
    {
        {'a', 'b', 'c'},
        {'d', 'e', 'f'}
    },
    {
        {'g', 'h', 'i'},
        {'j', 'k', 'l'}
    }
};
```

## 25.3 声明锯齿数组

锯齿数组是一种每个元素本身也是数组的数组。在这种语境下使用“锯齿”一词是因为数组元素的长度可以不同。锯齿数组可以被认为是每个元素数量不同的二维数组。

以下是一个用于存储不同大小二维数组的锯齿数组声明示例：

```cs
char[][] myJaggedArray;
```

以下代码声明并初始化相同的锯齿数组：

```cs
char[][] myJaggedArray = [
    ['a', 'b', 'c', 'd', 'e'],
    ['f', 'g', 'h', 'i'],
    ['j', 'j'],
    ['k', 'l', 'm', 'n', 'o', 'p', 'q', 'r']
];
```



C# 数组允许存储相同类型的值集合，并可以通过索引访问每个项。多维数组在方括号内使用逗号声明，而锯齿数组（jagged arrays）是长度不一的数组。

# 26. 访问和排序 C# 数组元素

上一章解释了如何在 C# 中创建 2 维数组、3 维数组和锯齿数组。在本章中，我们将探索如何访问、删除和排序数组的元素。

## 26.1 创建 ArrayDemo 项目

启动 VS Code，打开你的“C# Essentials”工作区文件夹，并创建一个名为 `ArrayDemo` 的新 .NET 控制台应用程序项目。

创建项目后，打开 `Program.cs` 文件并使用它尝试本章其余部分的示例。

## 26.2 获取数组的维度数

数组的维度可以通过数组的 `Rank` 属性获取。例如：

```csharp
char[,] my2Darray = new char[3,3]
{
    {'a', 'b', 'c'},
    {'c', 'd', 'e'},
    {'c', 'd', 'e'}
};

char[,,] my3Darray = new char[2,2,3]
{
    {
        { 'a', 'b', 'c' },
        { 'c', 'd', 'e' }
    },
    {
        { 'f', 'g', 'h' },
        { 'i', 'j', 'k' }
    }
};

Console.WriteLine($"Dimensions in my2Darray = {my2Darray.Rank}");
Console.WriteLine($"Dimensions in my3Darray = {my3Darray.Rank}");
```

输出：
```
Dimensions in my2Darray = 2
Dimensions in my3Darray = 3
```

## 26.3 访问数组元素

一旦值被存储在数组中，很可能在 C# 代码的后续某个需要访问这些值。这通过使用数组访问器符号结合目标值在数组中的索引来实现。数组访问器仅为数组名后跟方括号（`[]`）。方括号内放置一个代表目标值在数组索引的数字（注意 C# 中的第一个数组元素索引为 0）。例如，要访问 `myColors` 数组的第二个元素，将使用以下符号：

```csharp
string[] myColors = {"red", "green", "yellow", "orange", "blue"};
Console.WriteLine($"Element at index 1 = {myColors[1]}");
```

执行上述代码时，它将输出单词“green”，因为这是数组中索引位置 1 包含的字符串。

同样，可以使用访问器符号结合赋值运算符（`=`）来更改数组中特定索引位置的值。例如，要更改数组中第一个项的值：

```csharp
string[] myColors = ["red", "green", "yellow", "orange", "blue"];
myColors[0] = "violet";
Console.WriteLine($"Element at index 0 = {myColors[0]}");
```

多维数组中的值可以通过指定用并用逗号分隔的每个维度的索引值来访问。例如，要访问 `my2Darray` 中第一个数组的第一个元素，将使用以下访问器（注意数组从索引位置 0 开始）：

```csharp
char element = my2Darray[0,0];
```

以下代码演示了如何访问 2D 数组和 3D 数组中的各种元素：

```csharp
char[,] my2Darray = new char[3,3]
{
    {'a', 'b', 'c'},
    {'d', 'e', 'f'},
    {'g', 'h', 'i'}
};

char[,,] my3Darray =
{
    {
        { 'a', 'b', 'c' },
        { 'd', 'e', 'f' }
    },
    {
        { 'g', 'h', 'i' },
        { 'j', 'k', 'l' }
    }
};

// 输出 my2Darray 中第一个数组的第一个元素
Console.WriteLine($"{my2Darray[0,0]}");
// 输出 my2Darray 中最后一个数组的最后一个元素
Console.WriteLine($"{my2Darray[2,2]}");
// 输出 my3Darray 中第一个 2D 数组中第二个数组的第二个元素
Console.WriteLine($"{my3Darray[0,1,1]}");
// 输出 my3Darray 中第二个 2D 数组中第二个数组的第三元素
Console.WriteLine($"{my3Darray[1,1,2]}");
```

输出：
```
a
i
e
l
```

## 26.4 数组迭代

遍历数组中项的最简单方法是使用 `foreach` 语法。例如，下面的代码遍历了整个数组并将每个项输出到控制台：

```csharp
string[] myColors = ["red", "green", "yellow", "orange", "blue"];
foreach (string color in myColors)
{
    Console.Write("{0} ", color);
}
```

输出：
```
red green yellow orange blue
```

你也可以使用 `foreach` 语句来遍历多维数组。在下面的示例中，我们使用 `foreach` 遍历三维数组：

```csharp
char[,,] my3Darray =
{
    {
        { 'a', 'b', 'c' },
        { 'd', 'e', 'f' }
    },
    {
        { 'g', 'h', 'i' },
        { 'j', 'k', 'l' }
    }
};

foreach (char[,] array in my3Darray)
{
    foreach (char element in array)
    {
        Console.Write("{0} ", element);
    }
}
```

输出：
```
a b c d e f g h i j l
```

## 26.5 使用范围

范围（Ranges）允许你创建数组的子集。使用 `..` 运算符可以指定起始索引和结束索引。例如：

```csharp
string[] sentence = ["The", "best", "way", "to", "predict", "the", "future", "is", "to", "it"];
string[] subset = sentence[1..4]; // 包含索引 1, 2, 3 的元素
```

你也可以省略起始或结束索引来表示从开始或到末尾：

```csharp
string[] subset = sentence[..3]; // 从索引 0 到 2
string[] subset = sentence[2..]; // 从索引 2 到最后
string[] subset = sentence[1..²]; // 从索引 1 到倒数第 2 个元素
```

范围运算符可以与 `^` 运算符结合使用，其中 `^` 表示从末尾开始的索引。例如：

```csharp
string[] subset = sentence[³]; // 倒数第 3 个元素
```

## 26.6 C# 从索引开始的运算符

C# 从索引开始运算符（`^`）允许你根据数组末尾的位置数来指定范围的边界。例如，`¹` 代表数组的最后一个项，`²` 代表倒数第二个项，依此类推。索引 `⁰` 已经设置为数组项的总数：

```csharp
string[] myArray = {
    "item 1", // <-- ⁷ - 倒数第 7 个
    "item 2", // <-- ⁶
    "item 3", // <-- ⁵
    "item 4", // <-- ⁴
    "item 5", // <-- ³
    "item 6", // <-- ²
    "item 7" // <-- ¹ - 最后最后一个项
    // ⁰ = 数组长度
};
```

以下代码演示了在处理范围和数组时索引运算符的使用：





```cs
string[] sentence = {"The", "best", "way", "to", "predict", "the", "future", "is", "to", "invent", "it"};

string[] subset1 = sentence[⁷..⁴];

string[] subset2 = sentence[..²];

string[] subset3 = sentence[3..³];

foreach (string word in subset1)
{
    Console.Write("{0} ", word);
}
Console.WriteLine("\n");

foreach (string word in subset2)
{
    Console.Write("{0} ", word);
}
Console.WriteLine("\n");

foreach (string word in subset3)
{
    Console.Write("{0} ", word);
}
```

Output:
predict the future
The best way to predict the future is to
to predict the future is

```

## 26.7 排序 C# 

C# 数组是 `Array` 程序包的一部分，该包还包含了一些用于排序和重排数组的实用方法。

如果你需要对数组进行排序，可以作为参数传递给 `Array.Sort()` 方法，如下所示：

```cs
string[] myColors = [ "red", "green", "yellow", "orange", "blue" ];

Console.WriteLine("Before Sort");
foreach (string color in myColors)
{
    Console.Write("{0} ", color);
}

Array.Sort(myColors);
Console.WriteLine("\n\nAfter Sort");
foreach (string color in myColors)
{
    Console.Write("{0} ", color);
}
```

Output:
Before Sort
red green yellow orange blue
After Sort
blue green orange red yellow

你也可以使用 `Array.Reverse()` 方法反转数组中元素的顺序：

```cs
string[] myColors = ["red", "green", "yellow", "orange", "blue"];
Array.Reverse(myColors);
foreach (string color in myColors)
{
    Console.Write("{0} ", color);
}
```

Output:
blue orange yellow green red

## 26.8 清空 C# 数组

数组中的值可以使用 `Array.Clear()` 方法清空。该方法将数组中的每个项重置为该类型的默认值（布尔值为 false，数值项为 0，字符串为 null）。清空数组元素的语法如下：

`Array.Clear(<array>, <start index>, <count>);`

在上述语法中，`<array>` 是要清空的数组，`<start index>` 是从数组中哪个位置开始清空，`<count>` 是要清空的元素数量。

以下示例演示了从第 1 项开始清空三个元素：

```cs
string[] myColors = ["red", "green", "yellow", "orange", "blue"];
Array.Clear(myColors, 1, 3);
foreach (string color in myColors)
{
    Console.Write("{0} ", color);
}
```

当运行上述代码时，数组中将只剩下 `blue` 和 `red` 元素。

## 26.9 知识测试

点击下方的链接或扫描二维码以测试你对 C# 数组管理的知识和理解程度：

[`www.answertopia.com/ty5r`](https://www.answertopia.com/ty5r)

![](img/image-E70B6G8K.jpg)

## 26.10 总结

本章探讨了 C# 数组中元素的访问、删除和排序。它演示了如何使用 `Rank` 属性确定维度，使用数组访问符号访问元素，以及使用 `foreach` 循环遍历数组。此外，还涵盖了使用范围（ranges）和索引索引运算符（index from end operator）提取元素子集，以及使用 `Array.Sort()`、`Array.Reverse()` 和 `Array.Clear()` 方法分别对数组进行排序、反转和清空。

## 27. C# List 集合

在之前的章节中，我们看了 C# 数组。虽然数组在许多任务中用，但在功能和灵活性方面开始显得过时。C# 集合类提供了更高级的机制来收集对象组。

## 27.1 创建 CollectionDemo 项目

启动 VS Code，打开你的“C# Essentials”工作空间文件夹并创建一个名为 `CollectionDemo` 的新 .NET 控制台应用程序。

创建项目后，打开 `Program.cs` 文件并使用它尝试本章后续部分的示例。

## 27.2 介绍 C# 集合类

C# 集合类专门设计用于对对象进行分组并执行任务。C# 提供了多种集合类，我们将在接下来的章节中查看一些关键类。

## 27.3 使用 List 创建 C# 列表集合

`List<t>` 类的属性与 C# 数组非常相似。该类相比数组的一个关键优势是，它可以随着所存储对象数量的变化而动态增长或缩小。

创建 `List<type>` 集合的语法如下，其中 `type` 被替换为存储在列表中的数据类型：

`List<type>name = new List<type>();`

或者，上述语法可以简化为：

`List<type>name = [];`

考虑到上述语法，我们可以使用以下两个语句之一，创建一个名为 `colorList` 的空 `List<object>`，并配置为存储字符串值：

`List<string>colorList = new List<string>();`
`List<string>colorList = [];`

## 27.4 向列表添加项

一旦创建了 `List` 实例，就可以调用若干方法来对列表执行任务。其中一种方法是 `Add()` 方法，正如其名所示，它用于向列表添加项：

```cs
colorList.Add("Red");
colorList.Add("Green");
colorList.Add("Yellow");
colorList.Add("Purple");
colorList.Add("Orange");
```

`Add()` 方法将新项添加到列表末尾。要在特定索引插入新项，你需要使用后文 `Insert()` 方法。

## 27.5 使用多个值初始化列表

在上面的示例中，我们使用 `Add()` 方法逐个向空列表添加项。但如果你需要大量值初始化列表，可能会发现集合初始化器更高效，其语法如下：

`List<string>colorList = ["Red", "Green", "Yellow", "Purple", "Orange"];`

## 27.6 访问列表项

列表中的单个项可以使用其索引值访问（注意第一个项为 0，第二个为 1，依此类推）。索引值放在列表名称后的方括号中。例如，访问 `colorList` 对象的第二个项：

```cs
Console.WriteLine(colorList[1]);
```

Output:
Green

列表项的值同样可以使用索引结合赋值运算符（=）进行更改。例如，将 `Yellow` 颜色更改为 `Indigo`，代码如下：

```cs
Console.WriteLine($"Color before = {colorList[2]}");
colorList[2] = "Indigo";
Console.WriteLine($"Color after = {colorList[2]}");
```

Output:
Color before = Yellow
Color after = Indigo

与数组一样，你还可以构造 `foreach` 循环列出列表中的所有项。例如：

```cs
foreach (string color in colorList)
{
    Console.Write($"{color} ");
}
```

Output:
Red Green Indigo Purple Orange

## 27.7 从列表中删除项

可以使用 `Remove()` 方法从列表中删除项。该方法接受要删除的值作为参数。例如，要从 `colorList` 对象中删除 `Orange` 字符串，我们可以编写以下代码：

```cs
colorList.Remove("Orange");
foreach (string color in colorList)
{
    Console.Write($"{color} ");
}
```

Output:
Red Green Indigo Purple

注意 C# 列表可以存储重复项。在存在重复项的情况下，`Remove()` 方法只会删除第一个匹配实例。

## 27.8 向列表中插入项




此前，我们使用 `Add()` 方法向列表添加项。然而，`Add()` 方法仅将项添加到列表的末尾。有时，有必要在列表的特定位置插入新项。`Insert()` 方法正是为此特定目的而提供的。

`Insert()` 接收两个参数：一个表示插入位置索引的整数，以及要在该位置插入的项。例如，要在示例列表的位置 2 处插入一个项：

```csharp
List<string>colorList = ["Red", "Green", "Yellow", "Purple", "Orange"];
colorList.Insert(2, "White");

foreach (string color in colorList)
{
    Console.Write($"{color} ");
}
```

输出:
Red Green White Yellow Purple Orange

## 27.9 在 C# 中排序列表

目前无法让 C# 在添加项时自动对列表进行排序。可以通过调用 `Sort()` 方法对列表中的项进行排序：

```csharp
List<string>colorList = ["Red", "Green", "Yellow", "Purple", "Orange"];
colorList.Sort();

foreach (string color in colorList)
{
    Console.Write($"{color} ");
}
```

输出:
Green Orange Purple Red Yellow

上面的示例使用 C# 默认比较委托来组织新的列表顺序。虽然这超出了本书的范围，但值得知道的是，对于更高级的需求，你可以创建你自己的比较委托。

## 27.10 在 C# 列表中查找项

`List` 类提供了几种方法来查找项。最基础的方法是 `Contains()` 方法，当在列表对象上调用由于该方法时，如果指定的项位于列表中，则返回 `true`，否则返回 `false`。

`IndexOf()` 方法返回列表中匹配项的索引值。例如，以下代码示例将输出一个 `true` 结果（表示存在“Red”）以及索引值 `2`（这是字符串“Yellow”的索引位置）：

```csharp
List<string>colorList = ["Red", "Green", "Yellow", "Purple", "Orange"];
Console.WriteLine(colorList.Contains("Red"));
Console.WriteLine(colorList.IndexOf("Yellow"));
```

输出:
True
2

如果在列表中未找到该项，`IndexOf()` 方法将返回值 `-1`。

`LastIndexOf()` 方法返回列表中与指定项匹配的最后一个项的索引值。这对于列表包含重复项特别有用：

```csharp
List<string>colorList = ["Red", "Green", "Yellow", "Purple", "Red"];
Console.WriteLine(colorList.LastIndexOf("Red"));
```

输出:
4

## 27.11 获取有关列表的信息

`List<t>` 类的两个属性对于获取列表对象的信息很有帮助。例如，`Capacity` 属性可以识别集合在不调整大小的情况下可以存储多少项。

然而，`Count` 属性标识当前列表中存储了多少项。通常情况下，`Capacity` 的值将匹配或超过当前的 `Count`：

```csharp
List<string>colorList = ["Red", "Green", "Yellow", "Purple", "Orange"];
Console.WriteLine($"Count = {colorList.Count}");
Console.WriteLine($"Capacity = {colorList.Capacity}");
```

输出:
Count = 5
Capacity = 5

在 `Count` 和 `Capacity` 之间存在差距的情况下，你可以调用 `TrimExcess()` 方法来移除多余容量：

```csharp
colorList.TrimExcess();
```

## 27.12 清除 C# 列表

你可以通过调用 `Clear()` 方法移除列表中的所有项。

`Clear()` 方法会从列表中移除项，并将 `Count` 属性设置为零。然而，在列表清除后，`Capacity` 属性保持不变。要移除列表的容量，请在调用 `Clear()` 方法后紧调用 `TrimExcess()`：

```csharp
List<string>colorList = ["Red", "Green", "Yellow", "Purple", "Orange"];
Console.WriteLine($"Count = {colorList.Count}");
Console.WriteLine($"Capacity = {colorList.Capacity}");
colorList.Clear();
Console.WriteLine($"Count = {colorList.Count}");
Console.WriteLine($"Capacity = {colorList.Capacity}");
colorList.TrimExcess();
Console.WriteLine($"Count = {colorList.Count}");
Console.WriteLine($"Capacity = {colorList.Capacity}");
```

输出:
Count = 5
Capacity = 5
Count = 0
Capacity = 5
Count = 0
Capacity = 0

## 27.13 知识测试

点击下方链接或扫描二维码以测试你对 C# List 集合的知识和理解：

[`www.answertopia.com/tccy`](https://www.answertopia.com/tccy)

![](img/image-F8OS1N2G.jpg)

## 27.14 总结

C# 集合类提供了分组对象的高级机制，其中 `List` 是允许动态调整大小的关键类。可以使用 `Add()`、`Remove()`、`Contains()` 和 `IndexOf()` 等方法创建、修改和查询列表。此外，还可以对列表进行排序、清除，并访问其 `Count` 和 `Capacity` 等属性以获取列表内容的信息。

## 28. C# Dictionary 集合

C# 字典允许以键值对的形式存储和管理数据。字典的作用与数组和列表类似，但字典中的每个项都关联有一个键。

## 28.1 创建 DictionaryDemo

启动 VS，打开“C#”文件夹并创建一个名为 DictionaryDemo 的 .NET 项目。

## 28.2 字典初始化

字典是一种用于存储多个值的数据类型。字典中的每个项由一个键和一个关联的值组成。

可以使用以下语法创建一个空字典：

```csharp
Dictionary<int, string> name = new Dictionary<int, string>();
```

或者，你可以使用 `var` 关键字：

```csharp
var movies = new Dictionary<int, string>();
```

可以使用以下语法使用集合初始化器初始化新字典（注意我们再次使用了隐式类型）：

```csharp
var movies = new Dictionary<int, string>()
{
    { 1212, "The Godfather" },
    { 4433, "Apocalypse Now" },
    { 5465, "The Terminal" },
    { 1659, "Casablanca" }
};
```

在上述实例中，C# 编译器将使用隐式类型判断字典的键和值元素都是字符串，并防止插入其他类型的值或键。

## 28.3 字典计数

可以通过访问字典的 `Count` 属性获取字典中项的计数：

```csharp
var movies = new Dictionary<int, string>()
{
    { 1212, "The Godfather" },
    { 4433, "Apocalypse Now" },
    { 5465, "The Terminal" },
    { 1659, "Casablanca" }
};
Console.WriteLine($"Count = {movies.Count}");
```

输出:
Count = 4

## 28.4 字典迭代

与数组和列表一样，你可以使用 `foreach` 循环语法遍历字典中的所有项。例如，以下代码遍历 movies 字典中的所有项，输出每个项的键和值：

```csharp
foreach (var movie in movies)
{
    Console.WriteLine($"{movie.Key}: {movie.Value}");
}
```




```csharp
{ "CLA-1659", "Casablanca" }
};

foreach (var movie in movies) {
    var key = movie.Key;
    var value = movie.Value;
    Console.WriteLine($"{key} - {value}");
}
```

**输出:**
```
DRA-1212 - The Godfather
WAR-4433 - Apocalypse Now
COM-5465 - The Terminal
CLA-1659 - Casablanca
```

如我们在上面的代码所示，字典中的每个条目都具有 `Key` 和 `Value` 属性。在这种情况下，我们使用这些属性来提取每个字典条目的键名和电影标题。

## 28.5 添加和删除字典条目

可以通过调用实例的 `Add()` 方法并传递键/值对，向现有字典中添加新条目：

```csharp
var movies = new Dictionary<string, string>()()
{
    { "DRA-1212", "The Godfather" },
    { "WAR-4433", "Apocalypse Now" },
    { "COM-5465", "The Terminal" },
    { "CLA-1659", "Casablanca" }
};

movies.Add("SCI-2323", "Prometheus");
Console.WriteLine(movies["SCI-2323"]);
```

**输出:**
```
Prometheus
```

您可以通过调用 `Remove()` 方法并引用与要删除条目匹配的键，从字典中删除条目：

```csharp
var movies = new Dictionary<string, string>()()
{
    { "DRA-1212", "The Godfather" },
    { "WAR-4433", "Apocalypse Now" },
    { "COM-5465", "The Terminal" },
    { "CLA-1659", "Casablanca" }
};

movies.Remove("WAR-4433");

foreach (var movie in movies) {
    var key = movie.Key;
    var value = movie.Value;
    Console.WriteLine($"{key} - {value}");
}
```

**输出:**
```
DRA-1212 - The Godfather
COM-5465 - The Terminal
CLA-1659 - Casablanca
```

## 28.6 访问和更新字典项

可以使用键下标语法引用对应的值，来访问或修改特定的值。以下代码引用了一个已知于 `movies` 字典中的键，并输出了关联的值（在本例中为名为“The Terminal”的电影）：

```csharp
var movies = new Dictionary<string, string>()()
{
    { "DRA-1212", "The Godfather" },
    { "WAR-4433", "Apocalypse Now" },
    { "COM-5465", "The Terminal" },
    { "CLA-1659", "Casablanca" }
};

Console.WriteLine(movies["COM-5465"]);
```

**输出:**
```
The Terminal
```

在更新与指定键关联的值时，也可以使用键进行索引（例如，将同一部电影的标题从“The Terminal”更改为“Caddyshack”）：

```csharp
var movies = new Dictionary<string, string>()()
{
    { "DRA-1212", "The Godfather" },
    { "WAR-4433", "Apocalypse Now" },
    { "COM-5465", "The Terminal" },
    { "CLA-1659", "Casablanca" }
};

movies["COM-5465"] = "Caddyshack";
Console.WriteLine(movies["COM-5465"]);
```

**输出:**
```
Caddyshack
```

## 28.7 检查键或值是否存在

可以通过调用 `ContainsKey()` 方法搜索字典，以查找其是否包含特定键。在向字典中添加新条目之前，您可能希望调用此方法以确保键尚未被使用，以避免运行时异常错误。

您还可以通过调用 `ContainsValue()` 方法检查特定值是否存在于字典。以下示例演示了这两种方法的用法：

```csharp
var movies = new Dictionary<string, string>()()
{
    { "DRA-1212", "The Godfather" },
    { "WAR-4433", "Apocalypse Now" },
    { "COM-5465", "The Terminal" },
    { "CLA-1659", "Casablanca" }
};

if (movies.ContainsKey("CLA-1659")) {
    Console.WriteLine("Key exists in dictionary");
}

if (movies.ContainsValue("The Godfather")) {
    Console.WriteLine("Key exists in dictionary");
}
```

**输出:**
```
Key exists in dictionary
```

## 28.8 总结

字典存储键/值对。它可以用于添加、删除和更新条目。

## 29 文件和目录处理

### 29.1 介绍 System.IO

当我们在 `System.IO` 命名空间下处理文件和目录时，特别是我们将使用以下类：

- `Path`: 提供了一组用于管理路径字符串、构建新路径的方法。
- `Directory`: 提供了一组用于导航目录结构的方法。
- `DirectoryInfo`: 提供了与 `Directory` 类类似的功能。
- `File`: 提供了一组用于创建、删除和打开文件的静态方法。
- `FileInfo`: 提供了与 `File` 类类似的功能，但是非静态方法。
- `StreamReader` / `StreamWriter`: 提供了比 `File` 和 `FileInfo` 更灵活的方案，用于读取和写入文本文件。
- `BinaryReader` / `BinaryWriter`: 功能与 `StreamReader` 和 `StreamWriter` 相同，但用于处理二进制数据。

### 29.2 理解 C# 中的路径

路径由字符串值表示，并根据操作系统类型格式不同。在 Windows 系统上，每个路径组件由反斜杠 (\) 分隔，通常以驱动器号开头。

当程序启动时，工作目录是启动应用程序的目录。可以使用方法更改应用程序的工作目录。标准 UNIX 系统（macOS、Linux 等）使用正斜杠 (/) 来分隔路径组件。

文件系统的顶层目录被称为根目录，由 `/` 或 `\` 分隔符表示。以 `/` 或 `\` 开头的路径被称为绝对路径，因为它们指定了相对于根目录的文件位置。例如，`/home/demo` 和 `C:\Temp\Files` 是绝对路径。

不以斜开头的路径被解释为相对于当前工作目录。例如，如果当前工作目录是 `C:\Users\Demo` 且路径为 `Documents\Letters`，则该路径被具有等效的完整绝对路径 `C:\Users\Demo\Documents\Letters`。

Windows 路径出现了一个问题，因为反斜杠字符在 C# 字符串中表示转义序列。因此，以下路径会导致语法错误：

```csharp
"C:\Users\Demo\Desktop\Profile.txt"
```

一种方案是“转义”反斜杠：

```csharp
"C:\\Users\\Demo\\Desktop\\Profile.txt"
```

或者，Windows 路径也可以用字符串字面量来表示。





`@"C:\Users\Demo\Desktop\Profile.txt"`.

## 29.3 创建 FileDemo 项目

启动 VS Code，打开你的“C# Essentials”工作区文件夹，并创建一个名为 `FileDemo` 的新 .NET 控制台应用程序。项目准备好后，打开 `Program.cs` 文件并使用它来尝试本章其余的代码示例。

## 29.4 当前工作目录

应用程序的初始当前工作目录是启动它时的目录，可以使用 `Directory` 类进行识别。编辑 `Program.cs` 文件并如下所示使用静态方法 `Directory.GetCurrentDirectory()`：

```csharp
string currentDirectory = Directory.GetCurrentDirectory();
Console.WriteLine(currentDirectory);
```

点击运行按钮并检查终端输出，当前目录将在此显示。例如：

`/Users/neilsmyth/Documents/Books/C#_13/C# Essentials/FileDemo`

## 29.5 检查目录是否存在

`Directory` 和 `DirectoryInfo` 类都提供了一种识别指定路径是否存在目录的方法。以下代码检查名为 `MyFiles` 的目录是否存在。请注意，由于我们没有在路径前加上 `/` 或 `\`，该目录名是相对于当前工作目录的：

```csharp
if (Directory.Exists("MyFiles"))
{
    Console.WriteLine("Directory Exists.");
}
else
{
    Console.WriteLine("Directory does not exist.");
}
```

通过创建一个用目录路径的 `DirectoryInfo` 实例并访问 `Exists` 属性也可以实现相同的结果：

```csharp
DirectoryInfo dirInfo = new("MyFiles");
if (dirInfo.Exists)
{
    Console.WriteLine("Directory Exists.");
}
else
{
    Console.WriteLine("Directory does not exist.");
}
```

## 29.6 创建目录

识别出目录不存在后的下一步是创建它。在 C# 中使用 `Directory.CreateDirectory()` 静态方法或 `DirectoryInfo` 对象的 `Create()` 方法创建目录，例如：

```csharp
if (Directory.Exists("MyFiles"))
{
    Console.WriteLine("Directory Exists.");
}
else
{
    Console.WriteLine("Directory does not exist - creating...");
    Directory.CreateDirectory("MyFiles");
}

DirectoryInfo dirInfo = new("MyFiles");
if (dirInfo.Exists)
{
    Console.WriteLine("Directory Exists.");
}
else
{
    Console.WriteLine("Directory does not exist - creating...");
    dirInfo.Create();
}
```

当代码运行时，第一个语句将检测到目录不存在并创建它，第二个语句将报告该目录现在已存在：

Directory does not exist - creating...

Directory Exists.



## 29.7 删除目录

现有目录使用 `Directory` 类的 `Delete()` 方法删除，并将要删除的目录路径作为参数传递，例如：

```csharp
Directory.Delete("/Temp/Images");
```

如果目录包含文件或其他子目录，上述方法调用将触发 I/O 异常，指示目录为空。要覆盖此异常并删除目录及其所有文件和子目录，请如下所示传递布尔值 true：

```csharp
Directory.Delete("/Temp/Images", true);
```

## 29.8 更改当前工作目录

可以通过调用 `Directory.SetCurrentDirectory()` 方法并将目标目录作为参数传递来更改当前工作目录。与所有目录相关操作一样，提供的路径可以是绝对路径或相对路径。向 `Program.cs` 文件添加以下行将目录更改到 `MyFiles` 文件夹：

```csharp
Directory.SetCurrentDirectory("MyFiles");
Console.WriteLine(Directory.GetCurrentDirectory());
```

运行代码并确认当前目录已更改为 `MyFiles` 子目录，例如：

`/Users/neilsmyth/Dropbox/Documents/Books/C#_13/C# Essentials/FileDemo/MyFiles`

## 29.9 处理文件和目录异常

在 C# 中处理文件和目录时，重要的是许多许多操作都有抛出异常的可能。例如，考虑上述更改当前工作目录的代码。该示例之所以有效，是因为我们检查了 `MyFiles` 目录的存在性，并在必要时创建了它。然而，如果目录不存在，结果将不同。要看到这一效果，请向项目添加以下代码：

```csharp
Directory.SetCurrentDirectory("MyFiles1");
```

点击运行按钮，此时程序将带有以下未处理的 `DirectoryNotFoundException` 错误终止：

```
Unhandled exception. System.IO.DirectoryNotFoundException: Could not find a part of the path '/temp/MyFiles1'.
    at Interop.ThrowExceptionForIoErrno(ErrorInfo errorInfo, String path, Boolean isDirError)
```

为了避免未处理的异常，对文件和目录的处理必须进行防御性编码（例如在引用之前检查目录或文件是否存在），或者在类似下面的 try-catch 语句中执行：

```csharp
try
{
    Directory.SetCurrentDirectory("MyFiles1");
}
catch (Exception ex)
{
    Console.WriteLine($"{ex.Message}");
}
```

## 29.10 使用 File 类处理文件

在涵盖了 C# 目录处理的基础知识后，是时候查看文件了。`System.IO.File` 类提供了用于文件的创建、删除、复制和写入等方法。`FileInfo` 类提供了等效的方法。`File` 类提供了一系列用于处理文件的静态方法。

### 29.10.1 检查文件是否存在

与目录一样，我们可以通过调用 `File.Exists()` 方法检查路径的文件是否存在：

```csharp
if (File.Exists("MyFile.txt"))
```

### 29.10.2 创建并打开文件

我们还可以结合 `FileMode` 值使用 `File.Open()` 方法创建并打开文件：

```csharp
var myFile = File.Open(<path>, <mode>);
```

打开文件时可以使用以下模式：
- `Append`: 如果文件存在则打开它，否则创建一个新的。后续的写入操作将追加到现有文件中。
- `Create`: 创建新文件，如果已存在则覆盖它。
- `CreateNew`: 尝试创建一个新文件，如果文件已存在则抛出异常。
- `Open`: 打开现有文件，如果不存在则抛出异常。
- `OpenOrCreate`: 如果文件存在则打开，否则创建一个新的。
- `Truncate`: 打开现有文件并将其截零为零。

要创建一个新文件并覆盖现有文件可以使用以下代码：

```csharp
File.Open("MyFile.txt", FileMode.Create);
```

### 29.10.3 使用 File 类读取和写入

`WriteAllText()` 方法将字符串写入指定的文件。如果文件已存在，它将被覆盖，否则将创建一个新文件。相反，`ReadAllText()` 方法将读取文件的内容并将其作为字符串返回。以下代码在读取之前向名为 `MyFile.txt` 的文件写入字符串：

```csharp
File.WriteAllText("MyFile.txt", "Hello, this is some text.");
string content = File.ReadAllText("MyFile.txt");
Console.WriteLine($"content = {content}");
```

当代码执行时，终端将显示：

`content = Hello, this is some text.`

要向现有文件追加文本，我们调用 `AppendAllText()` 方法：

```csharp
File.WriteAllText("MyFile.txt", "Hello, this is some text.");
File.AppendAllText("MyFile.txt", " This is more text.");
string content = File.ReadAllText("MyFile.txt");
Console.WriteLine($"content = {content}");
```

生成的终端输出将如下：

`Hello, this is some text. This is more text.`

要一次性向文件写入多行文本，将行放在列表集合中并传递给 `WriteAllLines()` 方法：

```csharp
List<string> textList = ["Kia Sorento", "Alfa Romeo GTV6", "Chevy Spark", "Ford Explorer", "Toyota Celica"];
File.WriteAllLines("MyFile.txt", textList);
```




`ReadAllLines()` 方法读取文件的全部内容，并将文本行作为字符串数组返回：

```csharp
string[] readList = File.ReadAllLines("MyFile.txt");

foreach (string line in readList) {
    Console.WriteLine(line);
}
```

运行项目并在终端中检查是否有以下输出：

```
Kia Sorento
Alfa Romeo GTV6
Chevy Spark
Ford Explorer
Toyota Celica
```

## 29.11 删除、复制和移动文件

使用 `File` 类的 `Delete()` 方法删除现有文件（`FileInfo` 类中也提供了类似的选项），调用时传入要删除的文件路径，例如：

```csharp
File.Delete("/Temp/SomeFile.txt");
```

要将现有文件复制到新文件，请按如下方式使用 `File.Copy()` 方法：

```csharp
File.Copy("File1.txt", "/Temp/File2.txt");
```

`File.Move()` 方法将文件从一个位置移动到另一个位置，并包括重命名文件的选项。以下代码在目录之间移动文件：

```csharp
File.Move("MyFile.txt", "/Documents/MyFile.txt");
```

在以下示例中，使用 `Move()` 重命名当前工作目录下的文件：

```csharp
File.Move("oldfilename.txt", "newfilename.txt");
```

## 29.12 使用流进行文件 I/O

`File` 类提供了一种简单的方法将内容作为块或行写入文件。然而，对于更复杂的需求，我们需要使用流（streams）。

`StreamReader` 和 `StreamWriter` 类与 `File` 类相比，在读取文件和写入文件时具有更大的灵活性和控制力，并且更适合处理大文件。

`Stream` 类允许我们按行或按字符读取和写入文本。例如，以下代码使用 `StreamWriter` 的 `Write()` 和 `WriteLine()` 方法分别将单个字符和行写入流中：

```csharp
using (StreamWriter writer = new("MyFile.txt"))
{
    writer.Write('A');
    writer.Write('B');
    writer.Write('C');
    writer.WriteLine("DEFGHIJKLMNOP");
    writer.WriteLine("QRSTUVWXYZ");
}
```

注意上述代码中 `using` 语句的使用。`StreamReader` 和 `StreamWriter` 在创建时会分配资源，工作完成后需要释放这些资源。`using` 语句确保在完成工作后调用对应对象的 `Dispose()` 方法以释放分配的资源。或者，必须在流实例上调用 `Dispose()`：

```csharp
writer.Dispose();
```

以下代码使用 `StreamReader` 的 `ReadLine()` 方法逐行读取 `MyFile.txt` 文件的内容：

```csharp
using (StreamReader reader = new("MyFile.txt"))
{
    string line;
    while ((line = reader.ReadLine()) != null)
    {
        Console.WriteLine(line);
    }
}
```

我们可以使用 `StreamReader` 的 `Read()` 方法从文件中读取范围内的字符。`Read()` 方法有多个重载方法，允许以不同的方式调用它。例如，以下代码读取并显示了我们 `MyFile.txt` 文件中的第一个字符：

```csharp
Console.WriteLine($"Char = {(char)reader.Read()}");
```

输出：
```
Char = A
```

`StreamReader` 实例保留一个指向文件中当前位置的指针。上面的代码不仅读取了文件的第一个字符，还更新了指针以引用下一个位置。因此，第二次读取操作将返回字符 ‘B’。

为了避免读取到文件末尾之外的风险，我们可以使用 `StreamReader` 的 `Peek()` 方法查看下一个字符而不读取它。当 `Peek()` 返回 -1 时，我们知道当前字符是最后一个：

```csharp
while (reader.Peek() >= 0) {
    Console.WriteLine($"Char = {(char)reader.Read()}");
}
```

`Read()` 方法还可以使用以下语法从指定的索引位置读取指定数量的字符：

`Read(<char array>, <index>, <count>)`

在上述语法中，`<index>` 参数是相对于当前流位置的偏移量，而不是从流的开始。例如，如果流指针当前为 2，且给 `Read()` 传递的索引值为 3，则字符将从位置 5 开始读取。

以下代码示例从当前位置开始，每三个字符一个块从文件中读取：

```csharp
using (StreamReader reader = new("MyFile.txt"))
{
    char[] charBuffer;
    while (reader.Peek() >= 0)
    {
        charBuffer = new char[3];
        reader.Read(charBuffer, 0, 3);
        Console.WriteLine(charBuffer);
    }
}
```

执行时，上述代码将生成以下输出：

```
ABC
DEF
GHI
JKL
MNO
P
Q
RST
UVW
XYZ
```

模式在字母 ‘O’ 之后被中断，但请记住这是缓冲区逻辑结束的地方。模式在字母 ‘O’ 之后被中断，但请记住这是缓冲区逻辑结束的地方。（等等，原文此处有重复的句子，我将保持核心逻辑）。



本章探索了使用 `System.IO` 命名空间中的类在 C# 中进行文件和目录处理。我们涵盖了创建、删除、导航以及处理文件和目录的操作，包括检查存在性、更改当前工作目录以及处理异常。`File` 类提供了用于处理文件的静态方法，而 `FileInfo` 类提供了相同目的的非静态方法。我们还通过使用 `StreamReader`、`StreamWriter`、`BinaryReader` 和 `BinaryWriter` 类查看了更复杂的文件处理。

# 30. C# 字符串

字符串是字符的集合，这些字符组合在一起形成单词或句子。如果不是为了人类，计算机可能永远与字符串毫无关系。然而，事实是，计算机的主要工作之一就是接受人类提供的数据并向人类展示数据。因此，任何 C# 程序都可能包含大量专门设计用于处理字符串形式的数据的代码。

## 30.1 创建 StringsDemo 项目

启动 VS Code，打开你的“C# Essentials”工作区文件夹，创建一个名为 `StringsDemo` 的新 .NET 控制台应用程序项目。

创建项目后，打开 `Program.cs` 文件，并使用它尝试本章其余部分的示例。

## 30.2 在 C# 中创建字符串

字符串是由包含在字符串对象中的字符序列组成的。可以使用多种不同的机制创建字符串对象。

可以如下所示声明字符串但不对其进行初始化：

```csharp
string myString;
```

或者，你可以使用赋值运算符在 C# 中为字符串分配字面量值：

```csharp
string myString = "Hello World";
```

当然，也可以使用隐式类型来声明字符串：

```csharp
var myString = "Hello World";
```

同样，可以使用 `new` 关键字并将字面量值传递给构造函数来创建一个新字符串：

```csharp
string myString = new("Hello World");
```

字符串字面量放置在双引号内（如上所示）。如果字符串本身包含双引号，则应该在双引号字符前加上转义字符 `\` `：

```csharp
Console.WriteLine("He shouted \"Can you hear me?\"");
```

输出：
`He shouted "Can you hear me?"`

你还可以通过在字符串前加上 `@` 字符来指示 C# 将字符串中的所有字符视为字面量（verbatim）。使用 `@` 符号时，双引号之间的所有内容都被视为原始字符串，无论文本中是否存在换行符、回车、反斜杠等。例如：

```csharp
Console.WriteLine(@"You can put a backslash \ here

and a new line

and tabs work too.

You can also put in sequences that would normally be seen as escape sequences 转义序列.");
```

输出：
`You can put a backslash \ here
and a new line
and tabs work too.
You can also put in sequences that would normally be seen as escape sequences 转义 序列.`

如果你熟悉其他编程语言的 heredoc 函数，你会很快发现这本质上是 C# 的等效实现。

## 30.3 获取 C# 字符串的长度

如果你需要识别 C# 字符串的长度，可以通过访问字符串对象的 `Length` 属性来实现：

```csharp
string myString = "Hello World";
Console.WriteLine($"myString length = {myString.Length}");
```

输出：
`myString length = 11`

## 30.4 将字符串视为数组

通过使用下标语法 `[]` 指定索引值，可以访问字符串中的单个字符（记住第一个字符位于索引位置 0），并将字符串视为数组（数组在“在 C# 中创建 2D、3D 和交错数组”中介绍过）：

```csharp
string myString = "Hello World";
Console.WriteLine(myString[0]);
Console.WriteLine(myString[2]);
Console.WriteLine(myString[4]);
```

输出：
`H`
`l`
`o`

注意的是，字符串是不可变的（换句话说，虽然可以将全新的字符串字面量分配给变量，但你不能更改字符串中的单个字符）。为了体验体验这种限制，请尝试运行以下代码：

```csharp
string myString = "Hello World";
myString[5] = '-';
```

当尝试运行上述代码时，你将收到编译器的错误，内容如下：
`Property or indexer 'string.this[int]' cannot be assigned to -- it is read only`

还可以通过调用字符串对象的 `ToCharArray()` 方法将字符串转换为字符数组：

```csharp
string myString = "Hello World";
char[] charArray = myString.ToCharArray();
foreach (char c in charArray) {
    Console.WriteLine(c);
}
```

输出：
`H`
`e`
`l`
`l`
`o`
`W`
`o`
`r`
`l`
`d`

## 30.5 字符串字符迭代

既然我们可以将数组中的每个字符视为数组元素，那么了解到我们可以使用 `foreach` 循环如下遍历字符串的字符应该并不意外：

```csharp
string myString = "Hello World";
foreach (char c in myString) {
    Console.WriteLine(c);
}
```

输出：
`G`
`o`
`o`
`d`
`b`
`y`
`e`
`W`
`o`
`r`
`l`
`d`

## 30.6 字符串拼接

可以通过简单使用加运算符 `+` 将字符串相加来进行拼接（即连接在一起）。

因此，我们可以如下组合两个字符串：

```csharp
string myString = "Hello World.";
Console.WriteLine(myString + " How are you?");
```

输出：
`Hello World. How are you?`

或者，你可以使用 `string` 类的 `Concat()` 实例方法拼接字符串。该方法取两个要连接的字符串作为参数，并返回一个包含这两个字符串并集的新字符串：

```csharp
string myString1 = "If at first you don’t succeed, ";
string myString2 = "try, try again.";
string myString3 = string.Concat(myString1, myString2);
Console.WriteLine(myString3);
```

输出：
`If at first you don’t succeed, try, try again.`

## 30.7 比较字符串

如果你需要比较字符串，C# 提供了几种选项。最常用的选项是使用相等运算符，如下所示：

```csharp
string myString1 = "Hello World";
string myString2 = "Hello World";
if (myString1 == myString2)
{
    Console.WriteLine("The strings match.");
}
else
{
    Console.WriteLine("They strings not match.");
}
```

输出：
`The strings match.`

你也可以使用 `string.Equals()` 实例方法以类似的方式比较字符串。该方法取两个字符串作为参数，并返回指示字符串是否匹配的 `Boolean` ：

```csharp
string myString1 = "Hello world";
string myString2 = "Hello world";
if (string.Equals(myString1, myString2))
{
    Console.WriteLine("The strings match.");
}
else
{
    Console.WriteLine("The strings do not match.");
}
```

输出：
`The strings match.`

在上面的示例中，我们在比较时通过 `Equals()` 方法传递了字符串。`Equals()` 方法也可以在字符串字面量或字符串对象调用以获得相同的结果：

```csharp
string myString1 = "Hello world";
string myString2 = "Hello world";
if (myString1.Equals(myString2, StringComparison.Ordinal))
{
    Console.WriteLine("The strings match.");
}
else
{
    Console.WriteLine("The strings do not match.");
}
```

输出：
`The strings match.`

为止，我们探索的所有比较都是执行大小敏感比较。在调用 `Equals()` 方法时，你还可以传递一个比较类型参数。该类型必须取自 C# `StringComparison` 枚举，该枚举在执行文化敏感比较设置的值中，包含了用于忽略大小比较的 `OrdinalIgnoreCase` 值：

```csharp
string myString1 = "HELLO WORLD";
string myString2 = "Hello world";
if (string.Equals(myString1, myString2, StringComparison.OrdinalIgnoreCase))
{
    Console.WriteLine("The strings match.");
}
else
{
    Console.WriteLine("The strings do not match.");
}
```

输出：
`The strings match.`



直接在字符串字面量或对象上调用 `Equals()` 方法时，这种方法同样适用：

```csharp
var result = "My String".Equals("my string", StringComparison.OrdinalIgnoreCase);
```

`string.Compare()` 方法提供了另一种比较字符串的方法，尽管该方法具有一些额外的实用功能。此方法接受两个要比较的字符串作为参数，并返回一个整数值，表示字符串与排序顺序之间的关系。结果为 `0` 表示字符串匹配。小于 `0` 的值表示第一个字符串在排序顺序上于第二个字符串。最后，大于 `0` 的结果表示第二个字符串在排序顺序上于第一个字符串：

```csharp
string myString1 = "Bananas are yellow.";
string myString2 = "Oranges are orange.";
var result = string.Compare(myString1, myString2);

if (result == 0)
{
    Console.WriteLine("Strings match.");
}
else if (result < 0)
{
    Console.WriteLine("myString1 precedes myString2 in sort order.");
}
else if (result > 0)
{
    Console.WriteLine("myString2 precedes myString1 in sort order.");
}
```

输出：
myString1 precedes myString2 in sort order.

## 30.8 修改字符串大小写

可以使用 `ToUpper()` 和 `ToLower()` 方法更改字符串中字符的大小写。这两个方法都会返回一个修改后的字符串，而不是更改实际字符串。例如：

```csharp
string myString = "Hello World";
string newString;
newString = myString.ToUpper();
Console.WriteLine(newString);
newString = myString.ToLower();
Console.WriteLine(newString);
```

输出：
HELLO WORLD
hello world

## 30.9 将字符串拆分为多个部分

可以使用 `Split()` 方法将字符串拆分为多个部分。`Split()` 接受一个字符作为分隔符参数，用以识别拆分字符串的位置。该方法调用返回一个包含字符串各个部分的数组。例如，以下代码使用逗号字符作为分隔符拆分字符串。结果存储在名为 `myColors` 的数组中，然后通过 `foreach` 循环从数组中读取每个项并显示它：

```csharp
string myString = "Red, Green, Blue, Yellow, Pink, Purple";
string[] myColors = myString.Split(',');
foreach (string color in myColors)
{
    Console.WriteLine(color);
}
```

输出：
Red Green Blue Yellow Pink Purple

如我们所示，`Split()` 方法按照要求拆分了字符串，但我们遇到了一个问题，空格仍然存在。幸运的是，C# 提供了一个方法来处理这种情况。

## 30.10 修剪和填充字符串

可以使用 `Trim()` 方法从字符串中删除不需要的开头和结尾空格。调用时，该方法会返回一个修改后的字符串版本，删除了开头和结尾的空格：

```csharp
string myString = " hello ";
Console.WriteLine("[" + myString + "]");
Console.WriteLine("[" + myString.Trim() + "]");
```

输出：
[ hello ]
[hello]

如果你只需要删除开头或结尾空格，请分别使用 `TrimStart()` 或 `TrimEnd()` 方法。

修剪方法的反操作是 `PadLeft()` 和 `PadRight()` 方法。这些方法允许向字符串的开头或结尾添加字符。这些方法接受的参数是字符串需要填充的总字符数以及填充字符：

```csharp
string myString = "hello";
string newString;
newString = myString.PadLeft(10, ' ');
newString = newString.PadRight(20, '*');
Console.WriteLine("[" + newString + "]");
```

输出：
[ hello**********]

## 30.11 字符串替换

可以使用 `Replace()` 方法替换字符串的部分。该方法接受要替换的字符串部分和替换字符串作为参数，并返回一个反映更改的新字符串。`Replace()` 方法将替换字符串中的所有实例：

```csharp
string myString = "Hello World";
string newString;
Console.WriteLine(myString);
newString = myString.Replace("Hello", "Goodbye");
Console.WriteLine(newString);
```

输出：
Hello World
Goodbye World

## 30.12 知识测试

点击下方链接或扫描二维码以测试你对 C# 字符串的知识和理解：

[`www.answertopia.com/nppx`](https://www.answertopia.com/nppx)

![](img/image-G3POG6U1.jpg)

## 30.13 总结

C# 字符串用于人机交互的字符集合。可以使用字面量、`new` 关键字或隐式类型创建字符串。可以使用 `Length()`、`ToCharArray()` 和 `Concat()` 等方法处理字符串，并使用 `foreach` 循环对其进行迭代。

C# 提供了多种比较字符串的方法，包括 `Equals()` 和 `Compare()` 等相等运算符。`ToUpper()` 和 `ToLower()` 方法可以更改字符串大小，而 `Split()` 将字符串拆分为部分。`Trim()` 删除开头和结尾空格，而 `PadLeft()` 和 `PadRight()` 则在字符串的开头或结尾添加字符。

# 31. 字符串格式化

除了上一节概述的广泛的字符串操作函数外，`string` 类还提供了 `Format()` 方法。

除了上一节中概述的多种字符串操作函数外，`string` 类还提供了 `Format()` 方法。

C# `Format()` 方法的主要目的是通过额外的格式控制将字符串、数值或布尔值插入到字符串中。

## 31.1 Format 方法的语法

`Format()` 方法的通用语法如下：

```csharp
string.Format("格式字符串", arg1, arg2, .... );
```

格式字符串是用于插入值的字符串。字符串中的占位符指示了值的位置。占位符的形式为 `{}` 包围一个数字。格式字符串后面是逗号分隔的参数列表。每个占位符对应有一个参数。

## 31.2 创建 StringFormat 项目

启动 VS Code，打开你的“C# Essentials”工作空间文件夹，创建一个名为 `StringFormat` 的 .NET 控制应用程序。

创建项目后，打开 `Program.cs` 文件并使用它尝试本章剩余示例。

## 31.3 简单的字符串格式化示例

下面的代码示例演示了 `Format()` 方法的基本用法：

```csharp
string newString;
newString = string.Format("There are {0} cats in my {1} and no {2}", 2, "house", "dogs");
Console.WriteLine(newString);
```

输出：
There are 2 cats in my house and no dogs

让我们快速回顾上面的 `Format()` 方法调用。格式字符串包含三个占位符 `{0}`、`{1}` 和 `{2}`。格式字符串后面是用于每个占位符的参数。所以，例如，`{0}` 被第一个参数（数字 `2`）替换，`{1}` 被第二个参数（字符串“house”）替换，依此类推。

如果你回想起“C# 变量与常量”章节，你可能会好奇这与我们在书中反复使用的字符串插值技术有何不同。正如下面所示，C# 字符串格式化在结合格式控制时会变得更加有用。

## 31.4 使用格式控制

到为止，我们只是替换了占位符，但还没有在显示之前更改参数的格式。这实际上是指示 `Format()` 方法在显示时使用每个参数类型的默认格式。

格式控制出现在占位符的大括号 (`{}`) 内部。带有格式控制的占位符格式如下：

```
{n:controlx}
```



在上述语法中，`n` 是占位符数字，`control` 是应用于参数的特殊格式控制序列。可选的数字 `x` 进一步对某些控制类型的输出进行格式化。

### 31.5 简单的格式控制示例

以下示例使用了 `X` 格式控制，它用于用十六进制格式显示数字：

```csharp
var newString = string.Format("The number {0} in Hexadecimal is {0:X}.", 432);
Console.WriteLine (newString);
```

输出:
The number 432 in Hexadecimal is 1B0.

上面的示例以两种格式显示了参数 `0` (`432`)。第一种是默认的十进制格式，第二种使用 `X` 格式控制将参数作为十六进制数显示。

`string.Format()` 方法提供了许多格式控制，我们将在下文中进行探索。

### 31.6 C# string Format() 格式控制

下表列出了 C# `string.Format()` 方法支持的格式控制，以及每个控制的示例：

| 控制符 | 类型 | 描述 | 示例 |
| :--- | :--- | :--- | :--- |
| C | 货币 | 显示带有当前区域适当货币符号前缀的数字 | 432.00 的 `{0:C}` 输出 $432.00 |
| D | 十进制 | 以十进制形式显示数字，并可选填充 | 432 的 `{0:D4}` 输出 00432 |
| E | 指数法 | 以科学形式显示数字，并对小数部分可选值 | 432.32 的 `{0:E5}` 输出 4.32320E+002 |
| F | 固定点 | 显示数字，包括指定的小位数 | 432.324343 的 `{0:F3}` 输出 432.324 |
| N | 数字 | 通过插入逗号和四舍五入到最接近的百分位将数字转换为人类友好的格式 | 123432.324343 的 `{0:N}` 输出 123,432.32 |
| X | 十六进制 | 将数字转换为十六进制 | 432 的 `{0:X}` 输出 1B0 |
| 0:0… | 零填充 | 向参数添加零填充 | 43.1 的 `{0:0000.00}` 输出 0043.10 |
| 0:0#… | 空格填充 | 向参数添加空格填充 | 43.1 的 `{0:####.##}` 输出 43.1 |
| % | 百分比 | 将参数乘以 100 并附加百分号 | .432 的 `{0:00.00%}` 输出 43.20% |

表 31-1

在进入下一个章节之前，运行以下代码查看这些格式控制的实际效果：

```csharp
var newString = string.Format("The number {0} fixed to 2 decimal places is {0:F2}.", 109.78799);
Console.WriteLine (newString);

newString = string.Format("The number {0} using human friendly formatting is {0:N}.", 1023429.78799);
Console.WriteLine (newString);

newString = string.Format("The number {0} using exponential formatting is {0:E6}.", 32423.24232);
Console.WriteLine (newString);

newString = string.Format("The number {0} as a percentage to 3 decinal places is {0:00.000%}.", 0.24232);
Console.WriteLine (newString);
```

输出:
The number 109.78799 fixed to 2 decimal places is 109.79.
The number 1023429.78799 using human friendly formatting is 1,023,429.79.
The number 32423.24232 using exponential formatting is 3.242324E+004.
The number 0.24232 as a percentage to 3 decinal places is 24.232%.

### 31.7 知识测试

点击下方的链接或扫描二维码来测试你对 C# 字符串格式化的知识和理解程度：

[`www.answertopia.com/yywc`](https://www.answertopia.com/yywc)

![](img/image-7OJ7GK07.jpg)

### 31.8 总结

C# `string.Format()` 方法允许使用格式控制将值插入字符串。格式控制（如用于货币的 `C` 和用于十六进制的 `X`）可以在占位符中使用以修改输出格式。该方法为各种数据类型提供了广泛的格式控制。

# 32. C# 日期和时间

很少有可以在不需要处理日期和时间的情况下开发。考虑到这一点，负责 C# 的微软工程师为我们提供了 `DateTime` 对象。本章将介绍如何在基于 C# 的应用程序中使用此对象来处理日期和时间。涵盖主题包括加减时间、获取系统日期和时间，以及在 C# 中对日期时间进行格式化和元素提取。

### 32.1 创建 DateTime 项目

启动 VS Code，打开“C# Essentials”文件夹，创建一个名为 `DateTimeDemo` 的新控制台项目。

### 32.2 创建 DateTime

处理 `DateTime` 的第一步是使用 `DateTime` 构造函数。例如：

```csharp
DateTime newDate = new DateTime(2024, 4, 9);
Console.WriteLine(newDate.ToString());
```

输出:
4/9/2024

### 32.3 获取系统日期和时间

可以通过 `DateTime` 类的 `Today` 和 `Now` 静态属性访问系统日期和时间。`Today` 属性将返回当前日期（时间设置为 12:00 AM），而 `Now` 属性返回当前的日期和时间。例如，以下代码演示：

```csharp
Console.WriteLine(DateTime.Today.ToString());
Console.WriteLine(DateTime.Now.ToString());
```

输出:
8/16/2024 12:00:00 AM
8/16/2024 10:32:37 AM

## 32.4 对日期时间进行加减

C# `DateTime` 对象提供了多种方法用于向 `DateTime` 实例添加或减去日期和时间。这些方法列如下所示：

| 方法 | 描述 |
| :--- | :--- |
| Add | 加/减指定的 `TimeSpan` 实例值。 |
| AddDays | 加/减指定的数。 |
| AddHours | 加/减指定的小时。 |
| AddMilliseconds | 加/减指定的毫秒。 |
| AddMinutes | 加/减指定的分钟。 |
| AddMonths | 加/减指定的月份。 |
| AddSeconds | 加/减指定的秒。 |
| AddYears | 加/减指定的年份。 |

表 32-1

需要理解的关键问题是，这些方法不会更改调用该方法的 `DateTime` 对象的值，而是返回一个带有修改后的日期和时间的新 `DateTime` 对象。例如，在我们的示例中中添加五天：

```csharp
DateTime meetingAppt = new(2024, 4, 9, 14, 30, 0);
DateTime newAppt = meetingAppt.AddDays(5);
Console.WriteLine(newAppt.ToString());
```

输出:
4/14/2024 2:30:00 PM

要从日期和时间中减去，请向适当的方法传递负值。例如，我们可以从示例对象中减去十个月：

```csharp
DateTime meetingAppt = new(2024, 4, 9, 14, 30, 0);
DateTime newAppt = meetingAppt.AddMonths(-10);
Console.WriteLine(newAppt.ToString());
```

输出:
6/9/2023 2:30:00 PM

## 32.5 获取日期和时间的部分




日期和时间由不同且独立的数值组成，即日、月、年、小时、分钟、秒和毫秒。C# 的 `DateTime` 对象将每个值存储为对象内部的每个独立属性，允许单独访问每个值。例如，下面的代码示例提取了每个值并在控制台中显示它们：

```csharp
DateTime meetingAppt = new(2024, 4, 9, 14, 30, 0);

Console.WriteLine(meetingAppt.Day);

Console.WriteLine(meetingAppt.Month);

Console.WriteLine(meetingAppt.Year);

Console.WriteLine(meetingAppt.Hour);

Console.WriteLine(meetingAppt.Minute);

Console.WriteLine(meetingAppt.Second);

Console.WriteLine(meetingAppt.Millisecond);
```

输出：
9
4
2023
14
30
0
0

32.6

## 32.6 知识测试

点击下方的链接或扫描二维码来测试你对 C# 日期和时间的知识与理解：

[`www.answertopia.com/ants`](https://www.answertopia.com/ants)

![](img/image-XUU8LYKB.jpg)

## 32.7 总结

在本章中，我们学习了 C# `DateTime` 对象，它用于处理 C# 中的日期和时间。我们讨论了如何通过指定日期或包含时间值来创建 `DateTime` 对象。我们还查看了如何使用 `Today` 和 `Now` 属性访问当前日期和时间。此外，我们探索了 `DateTime` 对象提供的处理日期时间的各种方法，例如加减天、月、年和其他时间单位。最后，我们涵盖了如何使用 `DateTime` 属性提取日、月、年、小时和分钟等单个组件，这允许对日期和时间的特定元素进行操作。

## 索引

### 符号
- `&` 40
- `^` 41
- `^=` 42
- `<<` 41
- `<<=` 42
- `&=` 42
- `>>` 42
- `>>=` 42
- `|` 41
- `|=` 42
- `.NET Framework Class Library` 6
- `.NET SDK` 7, 8
- `installation` 7, 8

### A
- `abstract` 98
- `abstract class` 101
- `abstract members` 102
- `virtual members` 102
- `abstract modifier` 102
- `Access Modifiers` 63
- `file` 63
- `internal` 63
- `private` 63
- `private protected` 63
- `protected` 63
- `protected internal` 63
- `public` 63
- `accessor methods` 64
- `alias operator` 129
- `AND operator` 38, 40
- `anonymous methods` 87
- `arithmetic operators` 34
- `Array.Clear()` 163
- `Array.Reverse()` 163
- `Arrays` 153
- 2-dimensional 153
- 3-dimensional 154
- `accessing elements` 158
- `clearing` 163
- `creating` 153
- `dimensions of` 157
- `index from end` 161
- `iteration` 159
- `jagged` 155
- `multidimensional` 153
- `ranges` 160
- `sorting` 162
- `Array.Sort()` 162
- `assignment operator` 33
- `assignment operators` 35
- `Asynchronous programming` 143
- `async keyword` 145
- `await operator` 146

### B
- `base class` 97
- `Base Class Library` 6
- `BaseStream` 184
- `Length` 184
- `BCL` 6
- `BinaryReader` 185
- `class` 177
- `Read methods` 185
- `BinaryWriter` 177, 185
- `class` 177
- `Write()` 185
- `bit operators` 39
- `Bitwise AND` 40
- `Bitwise Left Shift` 41
- `bitwise OR` 40
- `bitwise right shift` 42
- `bitwise XOR` 41
- `bool` 26
- `Boolean logical operators` 37
- `Boolean variable` 26
- `break` 49, 53
- `byte` 24

### C
- `C#`
- `history of` 3
- `overview` 4
- `call hierarchy` 137
- `call tree` 137
- `CancellationToken` 149
- `CancellationTokenSource` 149
- `Cancel()` 150
- `C# Dev Kit Extension` 11
- `installation` 11
- `char` 27
- `CIL` 5
- `class`
- `vs. struct` 111
- `classes` 62, 74
- `abstract` 101
- `class file`
- `adding to project` 62, 106
- `class hierarchy` 95
- `class methods` 68
- `CLI` 5
- `CLR` 5
- `CLS` 6
- `Command Palette` 14
- `Common Intermediate Language` 5
- `Common Language Infrastructure` 5
- `Common Language Runtime` 5
- `Common Language Specification` 6
- `Common Type System` 6
- `comparison operators` 36
- `compound assignment operators` 35
- `Compound Bitwise Operators` 42
- `const` , 24
- `Constants` 24
- `constructors` 69
- `primary` 71
- `ContainsKey()` 174
- `ContainsValue()` 174
- `continue` 48, 54, 58
- `control flow` 43
- `conditional` 43
- `CTS` 6
- `Current working directory` 178

### D
- `data encapsulation` 64
- `DateTime` 199
- `Add()` 200
- `AddDays()` 200
- `AddHours()` 200
- `AddMilliseconds()` 200
- `AddMinutes()` 200
- `AddMonths()` 200
- `AddSeconds()` 200
- `AddYears()` 200
- `current time and date` 199
- `Now` 199
- `Today` 199
- `ToString()` 199
- `decimal` 26
- `decrement operators` 36
- `delegate` 87
- `Delegates` 81
- `as arguments` 84
- `declaring` 81
- `delegate keyword` 81
- `example` 82
- `multicast` 83
- `single cast` 83
- `Dictionary`
- `accessing items` 174
- `Add()` 173
- `add entry` 173
- `ContainsKey()` 174
- `ContainsValue()` 174
- `Count` 172
- `CreateDirectory()` 179
- `initialization` 171
- `item count` 172
- `iteration` 172
- `Remove()` 166
- `removing items` 166
- `syntax` 171
- `Directories` 177
- `Create()` 179
- `Delete()` 179
- `exception handling` 180
- `FileMode` 181
- `FileInfo` 177
- `Files` 177
- `creating` 181
- `opening` 181
- `finalizers` 69
- `float` 25
- `for`
- `break` 53
- `looping` 51
- `foreach` 54
- `variable scope` 52
- `format controls` 195
- `Framework Class Libraries` 6
- `Functions`
- `declaring` 73
- `vs. Methods` 73

### G
- `garbage collection` 5
- `getters` 64
- `GetType()` 32
- `global namespace` 21, 124
- `goto` 48

### H
- `hered` 188

### I
- `if` 43
- `if else` 44
- `if else if` 44
- `Implicit casting` 30
- `implicit typing` 23
- `increment operators` 36
- `index from end operator` 38
- `index operators` 38
- `Inheritance` 95
- `example` 95
- `inherited methods` 98
- `init-only` 115
- `inline code` 87
- `in modifier` 79
- `Installation`
- `Linux` 10
- `macOS` 9
- `Windows` 9
- `instance methods` 68
- `instantiation` 67
- `int` 23, 24
- `Integer types` 24
- `IntelliCode for C# Dev Kit`
- `installation` 11
- `internal` 64

### J
- `jagged arrays` 155
- `JIT` 5
- `Just in Time compiler` 5

### L
- `Lambdas` 89
- `expression` 89
- `multiple parameters` 90
- `statement` 89
- `syntax` 89
- `Left Shift Operator` 41
- `List<t>165</t>`
- `accessing items` 166
- `Add()` 165
- `Capacity` 168
- `Clear()` 169
- `Count` 168
- `creation` 165
- `finding items` 166
- `initialization` 171
- `Insert()` 165
- `inserting items` 167
- `Last()` 168
- `Remove()` 166
- `removing items` 166
- `Sort()` 167
- `sorting items` 167
- `Trim()` 168
- `List.`
- `literal` 26
- `Local functions` 91
- `long` 24
- `looping` 51
- `loosely typed` 23

### M
- `Main method` 21
- `Main Thread` 143
- `managed code` 5
- `members` 61
- `methods` 61, 68
- `Methods`
- `anonymous-- methods` 87
- `Multicast delegates` 83

### N
- `named arguments` 75
- `Named arguments` 75
- `namespace` 21, 124
- `accessing` 127
- `alias operator` 129
- `declaration` 126
- `file scoped` 130
- `global` 21, 124
- `nesting` 129
- `overview` 124
- `using` 128
- `new` 67, 71
- `NGen` 6
- `Null-coalescing operators` 39

### O
- `object-oriented` 61
- `OperationCanceledException` 150
- `operator precedence` 34
- `Optional arguments` 76
- `OR operator` 37, 40
- `out modifier` 78
- `override` 98

### P
- `params` 76
- `Path class` 177
- `Peek()` 183
- `primary constructor` 71
- `private` 64
- `private protected` 64
- `Projects` 13
- `properties` 61
- `property` 64
- `protected` 64
- `protected internal` 64
- `public` 63, 64
- `public field` 64

### R
- `range operators` 38
- `readonly` 66, 115
- `reference type` 112
- `ref modifier` 77, 78
- `Right Shift Operator` 42

### S
- `sbyte` 24
- `setters` 64
- `short` 24
- `sign bit` 42
- `single cast delegates` 83
- `single inheritance` 95
- `Solution Explorer` 14
- `displaying` 62, 106
- `solution file` 13
- `Solutions` 13
- `Special characters` 27
- `SSCLI` 6
- `static` 66
- `static member` 66
- `static methods` 68
- `Stopwatch` 144
- `StreamReader` 182




## System 命名空间
- `System` 21
- `System.Object` 95
- `System.IO` 177

## BaseStream
- `BaseStream.Length` 184

## class
- `class` 177
- `Read()` 183
- `ReadLine()` 183
- `ReadToEnd()` 184
- `synchronous methods` 184

## StreamWriter
- `class` 177
- `synchronous methods` 184
- `Write()` 182
- `WriteLine()` 182

## string
- `string` 23, 28
- `String 数据类型` 28
- `字符串插值` 29
- `字符串字面量` 28
- `字符串字面量` 187
- `strings`
    - `作为数组` 188
- `更改大小` 192
- `字符迭代` 189
- `Compare()` 191
- `比较` 190
- `拼接` 189
- `声明一个` 187
- `Equals()` 190
- `foreach` 189
- `Format()` 195
- `格式控制符` 195
- `格式化` 195
- `迭代` 189
- `length` 188
- `字面量` 187
- `@` 修饰符 187 
- `填充` 193
- `PadLeft()` 193
- `PadRight()` 193
- `Replace()` 193
- `替换` 193
- `Split()` 192
- `分割` 192
- `StringComparison` 191
- `OrdinalIgnoreCase` 191
- `ToCharArray()` 188
- `ToLower()` 192
- `ToUpper()` 192
- `Trim()` 193
- `TrimEnd()` 193
- `修剪` 193
- `TrimStart()` 193
- `string.Compare()` 191
- `string.Equals()` 190
- `string.Format()` 195

## struct
- `struct` 111
- `vs. class` 111

## Structures
- `Structures` 111

## subclass
- `creating` 96
- `子类化` 95
- `base class` 97

## switch
- `switch` 47
- `break` 49
- `continue` 50
- `example` 48
- `expressions` 49
- `goto` 49
- `syntax` 47
- `switch expressions` 49

## synchronous code
- `synchronous code` 144

### T
- `Task` 类 145
- `Result` 属性 148
- `Run()` 149
- `Wait()` 146
- `WaitAll()` 148
- `Task.Delay()` 144
- `Task.Run()` 149
- `Task.WaitAll()` 148
- `ternary operator` 38
- `this` 72

## Threads
- `overview` 143
- `throw statement` 134
- `TimeSpan` 200
- `try-catch` 135
- `try / catch statement` 150
- `try-finally` 137

## tuple
- `tuple` 117
- `accessing items` 117
- `declaration` 117
- `example` 120
- `field names` 118
- `method parameters` 119
- `tuples`
    - `returning` 118
- `type annotations` 23
- `type casting` 30
- `explicit` 31
- `implicit` 30
- `type-safe` 23

### U
- `uint` 24
- `ulong` 24
- `unary operator` 34
- `Unicode scalars` 27
- `ushort` 24
- `using` 21, 128
- `using statement` 183

### V
- `value type` 112
- `var` 23
- `Variables` 23
- `variable scope` 52
- `Verbatim string literals` 28
- `VES` 5
- `virtual` 98
- `Virtual Execution System` 5
- `virtual members` 102
- `virtual modifier` 102

## Visual Studio Code
- `macOS installation` 9
- `theme` 10
- `Windows installation` 9
- `VS Code`
    - `Command Palette` 14
    - `editor splitting` 15
    - `folders` 13
    - `project` 13
    - `solution file` 13
    - `solutions` 13
    - `workspaces` 13
    - `Zen mode` 16

## W
- `Wait()` 144
- `WaitAll()` 148
- `when keyword` 136
- `while` 57
- `break` 58
- `continue` 58
- `Workspaces` 13
- `WriteLine()` 44

## X
- `XOR operator` 37, 41

### Z
- `Zen mode` 16

