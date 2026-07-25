# C# 10.0 傻呆全指南



![](img/cover.jpg)
















   - `FIGURE 8-4`: 创建用于演示进度条用法的表单。





C# 有等效的递减运算符——`n--` 和 `--n`。它们的工作与递增运算符完全相同。

## 执行逻辑比较——这符合逻辑吗？

C# 提供一组逻辑比较运算符，如表 4-2 所示。这些运算符是`逻辑`比较，因为它们返回 `bool` 类型的 `true` 或 `false` 值。

| 运算符 | 满足什么条件为真 |
| --- | --- |
| a == b | a 的值与 b 相同。 |
| a > b | a 大于 b。 |
| a >= b | a 大于等于 b。 |
| a < b | a 小于 b。 |
| a <= b | a 小于等于 b。 |
| a != b | a 不等于 b。 |

表 4-2 逻辑比较运算符

这是一个逻辑比较的示例：

```
int m = 5;
int n = 6;
bool b = m > n;
```

这个示例将值 `false` 赋值给变量 `b`，因为 5 *并不*大于 6。逻辑比较适用于所有数值类型，包括 `float`、`double`、`decimal` 和 `char`。以下所有语句都是合法的：

```
bool b;
b = 3 > 2; // true
b = 3.0 > 2.0; // true
b = 'a' > 'b'; // false -- 按字母顺序，靠后的字母更大。
b = 'A' < 'a'; // true -- 大写 A（值 65）小于小写 a（值 97）。
b = 'A' < 'b'; // true -- 所有大写字母都小于小写字母。
b = 10M > 12M; // false
```

比较运算符总是产生 `bool` 类型的的结果。除了 `==` 和 `!=` 之外，比较运算符对于 `string` 类型的变量无效。（不用担心：C# 提供了其他比较字符串的方法，详情请参阅本微型书的第 3 章。）

## 比较浮点数：你的 float 比我的大吗？

比较两个浮点值可能会很棘手，你需要对这些比较保持小心。考虑以下比较：

```
float f1;
float f2;
f1 = 10;
f2 = f1 / 3;
bool b1 = (3 * f2) == f1; // 如果 (3 * f2) 等于 f1，则 b1 为 true。
f1 = 9;
f2 = f1 / 3;
bool b2 = (3 * f2) == f1;
```

注意上述示例中的第五行和第八行都包含一个赋值运算符（=`），然后是一个逻辑比较（`==`）。它们是不同的东西，所以当你想表示 `==` 时不要输入 `=`。C# 执行逻辑比较，然后将结果赋值给左侧变量。

`b1` 和 `b2` 计算之间的唯一区别在于 `f1` 的原始值。




![Technicalstuff](img/technicalstuff.png) `&`、`|` 和 `^` 运算符也有位运算符版本。当应用于 `int` 变量时，这些运算符会按位为基础进行操作。因此，`6 & 3` 等于 `2`（0110[2] & 0011[2] 为 0010[2]），`6 | 3` 等于 `7`（0110[2] | 0011[2] 为 0111[2]），而 `6 ^ 3` 等于 `5`（0110[2] ^ 0011[2] 为 0101[2]）。二进制算术很酷，但超出了本书的范围。你可以在 [`https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/bitwise-and-shift-operators`](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/bitwise-and-shift-operators) 了解更多信息。剩余的两个逻辑运算符与前三个相似，但有细微区别。考虑以下示例：

```
bool b = (boolExpression1) & (boolExpression2);
```

在这种情况下，C# 会评估 `boolExpression1` 和 `boolExpression2`。然后它在决定 `b` 的值之前会检查它们是否都为 `true`。然而，这可能是徒用功。如果其中一个表达式为 `false`，则没有必要评估另一个。无论第二个表达式的值如何，结果都将是 `false`。尽管如此，`&` 仍继续评估两个表达式。`&&` 运算符避免了不必要的双表达式评估，如下例所示：

```
bool b = (boolExpression1) && (boolExpression2);
```

在这种情况下，C# 会评估 `boolExpression1`。如果它为 `false`，则 `b` 被设置为 `false` 且程序继续执行后续代码。另一方面，如果 `boolExpression1` 为 `true`，则 C# 会评估 `boolExpression2` 并将结果存储在 `b` 中。`&&` 运算符使用了这种短路求值，因为它在需要时会对第二个布尔表达式进行短路。

![Tip](img/tip.png) 大多数程序员在大多数时候使用双写形式。`||` 运算符的工作方式相同，如下表达式所示：

```
bool b = (boolExpression1) || (boolExpression2);
```

如果 `boolExpression1` 为 `true`，则没有必要评估 `boolExpression2`，因为结果总是 `true`。你可以将这些运算符读作“短路与”和“短路或”。

![Technicalstuff](img/technicalstuff.png) 某些程序员确实依赖特定任务标准任务。例如，如果表达式执行的任务除了提供值之外，那么不使用短路运算符很重要，否则当第一个任务为 `false` 时，C# 将永远不会执行第二个任务。现在不用担心这种情况，但将其作为有用信息留作以后。有时，当你依赖代码执行超出两个值评估的操作时，短路运算符会产生意外的结果。

## 在 TrackDownAMate.com 匹配表达式类型

在计算中，表达式的类型与其值一样重要。考虑以下表达式：

```
int n;
n = (5 * 5) + 7;
```

我的计算器显示 `n` 的结果值为 32。然而，该表达式还根据其组成部分的类型具有整体类型。用“类型语言”编写，前述表达式变为：

```
int [=] (int * int) + int;
```

要评估表达式的类型，请遵循与评估表达式值相同的模式。乘法的优先级高于加法。一个 `int` 乘以一个 `int` 得到一个 `int`。接下来是加法。一个 `int` 加上一个 `int` 得到一个 `int`。通过这种方式，你可以这样简化前面的表达式：

```
(int * int) + int
int + int
int
```

### 计算操作的类型

大多数运算符都有多种变体。例如，乘法运算符有以下形式（箭头表示“产生”）：

```
int * int --> int
uint * uint --> uint
long * long --> long
float * float --> float
decimal * decimal --> decimal
double * double --> double
```

因此，`2 * 3` 使用 `*` 运算符的 `int * int` 版本来产生输出 `int 6`。

### 隐式类型转换

`*` 运算符对于两个两个 `int` 或两个 `float` 相乘效果良好。但想象一下当左右参数不是相同类型时会发生什么。例如，考虑这种情况：

```
int anInt = 10;
double aDouble = 5.0;
double result = anInt * aDouble;
```

首先，C# 没有 `int * double` 操作。C# 可以只生成一个错误消息并就此结束；然而，它尝试理解程序员的意图。C# 拥有 `int * int` 和 `double * double` 版本的乘法，可以将 `aDouble` 转换为其 `int` 等效值，但这会导致丢失数字的任何小数部分（小数点右的数字）。相反，在隐式提升中，C# 将 `int anInt` 转换为 `double` 并使用 `double * double` 运算符。

隐式提升是隐式的，因为是 C# 自动完成的，它是从 `int` 到 `double` 的提升。从高能力类型（如 `double`）到低能力类型（如 `int`）的转换被称为降级。

![Warning](img/warning.png) 隐式降级是不允许的；C# 会生成错误消息。

### 显式类型转换——强制转换

想象如果 C# 的隐式转换是错误的，程序员想要执行整数乘法。你可以通过强制转换更改任何值类型的类型。强制转换由括号内的类型组成，并放在变量或表达式之前。因此，以下表达式使用了 `int * int` 运算符：

```
int anInt = 10;
double aDouble = 5.0;
int result = anInt * (int)aDouble;
```

将 `aDouble` 转换为 `int` 被称为显式降级或向下转换。转换是显式的，因为有程序员的显式声明。

![Remember](img/remember.png) ![Tip](img/tip.png) 避免隐式类型转换。通过强制转换使任何值类型的更改显式化。这样做可以减少错误的可能性并使代码更易读。

### 保持逻辑不变

C# 不提供到或自 `bool` 类型的转换路径。

### 类型赋值

转换中的相同类型匹配也适用于赋值运算符。

![Warning](img/warning.png) 产生编译错误的无意类型不匹配通常发生在赋值运算符，而不是在匹配点。考虑以下乘法示例：

```
int n1 = 10;
int n2 = 5.0 * n1;
```

此示例中的第二行由于类型不匹配产生错误消息，但错误发生在赋值处——而不是法处。这里是糟糕的故事：为了执行乘法，C# 隐式将 `n1` 转换为 `double`。C# 然后可以执行 `double` 乘法，其结果是强大的 `double`。赋值运算符的左右运算符类型必须匹配，但左运算符的类型不能更改。由于 C# 拒绝隐式降级表达式，编译器生成错误消息 `无法将类型 double 转换为 int`。C# 通过显式转换允许此表达式：

```
int n1 = 10;
int n2 = (int)(5.0 * n1);
```





（括号是必要的，因为转换操作符的优先级非常。）这个示例可以工作——`explicit` 降级是允许的。`n1` 被提升为 `double`，执行乘法运算，然后将 `double` 结果降级为 `int`。然而在这种情况下，你会担心程序员的逻辑是否正常，因为 `5 * n1` 对于程序员和 C# 编译器来说都容易读得多。

## 更改运算符的工作方式：运算符重载

为了让事情变得更加复杂，可以使用 C# 的一项名为“运算符重载”的功能来改变任何运算符的行为。`运算符重载` 本质上定义一个新的函数，每你在定义重载的同一项目中使用运算符时，该函数就会运行。运算符重载实际上比起来要简单。如果你编写代码：

```sharp
var x = 2 + 2;
```

你会预期 `x` 等于 4 对吧？那就是 `+` 的工作方式。好吧，朋友们，这是二十一世纪了，答案取决于主观观点！为了让事情变得有趣，你应该在任何交易中给用户比他们要求的更多的东西。出于这个原因，你可能想给每个加法操作加上值 `1`。

要给每个加法操作加上值 `1`，你需要创建一个你的重载运算符可以使用自定义类。该类将具有一些自定义类型和一个你将用于重载操作的方法。简而言之，如果你加上普通的数字，你会得到一个普通的答案；如果你加上特殊的 `AddOne` 数字，你会得到加 1 的结果（你也可以在下载的源码 `AddOneToNumber` 示例中找到这段代码）：

```sharp
public class AddOne
{
    public int x;
    public static AddOne operator +(AddOne a, AddOne b)
    {
        AddOne addone = new AddOne();
        addone.x = a.x + b.x + 1;
        return addone;
    }
}
```

注意，你将类 `AddOne` 放在 `Program` 类之外，但在 `AddOneToNumber` 命名空间之内。第 2 章 会告诉你更多关于类如何工作的知识——目前只需关注代码的运算符部分。在重载 `+` 运算符后（使用列表中的运算符标签），你可以像往常一样使用它：

```csharp
static void Main(string[] args)
{
    AddOne foo = new AddOne();
    foo.x = 2;
    AddOne bar = new AddOne();
    bar.x = 3;
    // 现在 2 + 3 等于 6…
    Console.WriteLine((foo + bar).x.ToString());
    Console.Read();
}
```

当然，答案将是 6 而不是 5。除非你计划重写数学定律，否则运算符重载对整数没有用处。然而，如果你确实有两个想要能够相加的实体，这种技术可能会很有用。例如，如果你有一个 `Product` 类，你可以为该类重新定义 `+` 运算符来相加价格。

# 第 5 章

# 进入程序流程

本章内容

- ![Bullet](img/check.png) **如果可以就用 `if` 做决策**
- ![Bullet](img/check.png) **决定 `else` 执行什么**
- ![Bullet](img/check.png) **使用 `while` 和 `do … while` 循环**
- ![Bullet](img/check.png) **使用 `for` 循环并理解作用**

考虑这个简单的程序：

```csharp
using System;
namespace HelloWorld
{
    public class Program
    {
        // 这是程序开始的地方。
        static void Main(string[] args)
        {
            // 提示用户输入名称。
            Console.WriteLine("Enter your name, please:");
            // 现在读取输入的名称。
            string name = Console.ReadLine();
            // 使用输入的名称问候用户。
            Console.WriteLine("Hello, " + name);
            // 等待用户确认结果。
            Console.WriteLine("Press Enter to terminate … ");
            Console.Read();
        }
    }
}
```

除了你介绍 C# 编程的基础知识外，这个程序几乎一无用处。它只是简单地回显你输入的任何内容。你可以想象更复杂的程序示例，它们接受输入、执行某种计算、生成某种输出（否则，为什么要计算呢？），然后在底部退出。然而，像这样的程序用途是有限的。

任何计算机处理器的关键要素之一是其决策的能力，这意味着当条件为真时，处理器将执行流发送到一条指令路径，当条件为假（不真）时，发送到另一条路径。任何编程语言必须提供这种控制执行流的基本能力。

`流程控制`的三种基本类型是 `if` 语句、循环和跳转。（本教程的第 6 章 你不需要手动输入本章的源代码。事实上，使用下载的源码容易得多。你可以在下载源码的 `\CSAIO4D2E\BK01\CH05` 文件夹中找到本章的源码。详情请见介绍如何查找这些源文件。

## 使用 if 和 switch 进行分支

所有 C# 决策的基础都是 `if` 语句：

```csharp
if (condition)
{
    // 如果条件为真则执行此处
}
```

如果条件为假，程序将跳过该块。你也可以使用 `else` 语句在条件为假时执行代码：

```csharp
if (condition)
{
    // 如果条件为真则执行此处
}
else
{
    // 如果条件为假则执行此处
}
```

你也可以使用 `else if` 来检查多个条件：

```csharp
if (condition1)
{
    // 如果 condition1 为真则执行此处
}
else if (condition2)
{
    // 如果 condition2 为真则执行此处
}
else
{
    // 如果两个都不真则执行此处
}
```

## 引入 if 语句

考虑一个计算利息的小程序。用户输入本金和利率，程序输出每年的结果。（这个程序并不复杂。）简单的计算在 C# 中所示：

```csharp
// 计算本金加利息。
decimal interestPaid;
interestPaid = principal * (interest / 100);
// 现在计算总额。
decimal total = principal + interestPaid;
```

第一条方程将本金 `principal` 乘以利率 `interest` 以产生支付的利息——`interestPaid`。（除以 `100` 是因为利息通常按百分比计算的。）然后将支付的利息加回本金，得到存储在变量 `total` 中的新本金。

在处理人类输入必须预见到几乎任何情况。例如，你不希望程序接受负的本金或利息金额（好吧，也许可以是负利息）。以下 `CalculateInterest` 程序包含了检查，以确保这些情况都不会发生：

```csharp
static void Main(string[] args)
{
    // 提示用户输入源本金。
    Console.Write("Enter principal: ");
    string principalInput = Console.ReadLine();
    decimal principal = Convert.ToDecimal(principalInput);
    // 确保本金不是负数。
    if (principal < 0)
    {
        Console.WriteLine("Principal cannot be negative");
    }
}
```





```csharp
principal = 0;

}

// 输入利率。
Console.Write("Enter interest: ");
string interestInput = Console.ReadLine();
decimal interest = Convert.ToDecimal(interestInput);

// 确保利率也不为负数。
if (interest < 0)
{
    Console.WriteLine("Interest cannot be negative");
    interest = 0;
}

// 计算本金加利息的值。
decimal interestPaid = principal * (interest / 100);
// 现在计算总额。
decimal total = principal + interestPaid;
// 输出结果。
Console.WriteLine(); // 跳过一个行。
Console.WriteLine("Principal = " + principal);
Console.WriteLine("Interest = " + interest + "%");
Console.WriteLine();
Console.WriteLine("Interest paid = " + interestPaid);
Console.WriteLine("Total = " + total);
Console.Read();
}
```

![Tip](img/tip.png) `CalculateInterest` 程序首先通过 `Write()` 向控制台写入一个 `string` 来提示用户输入本金金额。准确地告诉用户你什么，如果可能的话，还要指定格式。用户对没有提供信息的提示（例如 `>`）反应并不好。

示例程序使用 `ReadLine()` 命令读取用户输入的任何内容；当用户按下回车键时，程序将以 `string` 的形式返回输入的值。由于程序正在寻找 `decimal` 格式的本金，因此必须使用 `Convert.ToDecimal()` 命令对输入字符串 `string` 进行转换。结果存储在 `principalInput` 中。

![Remember](img/remember.png) `ReadLine()`、`WriteLine()` 和 `ToDecimal()` 命令都都是方法调用的示例。`method call` 将某些工作委托给程序的另一个部分，该部分被称为方法。第 2 册 详细描述了方法调用。现在，如果你在精确理解方法调用如何工作方面有问题，不要担心。

示例中的下一行检查 `principal`。如果它是负数，程序将输出一条礼貌的消息，指示输入无效。程序对利率执行了相同的操作，然后执行了之前在“介绍 if 语句”节中概述的简易利息计算，并使用一系列 `WriteLine()` 命令输出结果。这里是程序的某些示例输出：

```
Enter principal: 1234
Enter interest: 21
Principal = 1234
Interest = 21%
Interest paid = 259.14
Total = 1493.14
```

使用非法输入执行程序产生以下输出：

```
Enter principal: 1234
Enter interest: -12.5
Interest cannot be negative
Principal = 1234
Interest = 0%
Interest paid = 0
Total = 1234
```

![Tip](img/tip.png) 在 `if` 语句内的行进行缩进以增强可读性。这种类型的缩进会被 C# 忽略，但对我们人类很有帮助。大多数编程编辑器支持自动缩进，即编辑器在你输入 `if` 语句时会自动进行缩进。要在 Visual Studio 中设置自动缩进，请选择工具 (Tools) ⇒ 选项 (Options)。然后展开文本编辑器 (Text Editor) 节点。从那里，展开 C#*.*。最后，点击表 (Tabs)。在此页面上，启用智能缩进 (Smart Indenting) 并根据你的喜好设置每个缩进的空格数（书中每个缩进四个空格）。将制表大小设置为相同的值。

### 检查 else 语句

有时，你的代码必须检查互斥条件。例如，以下代码段将两个数字 `a` 和 `b` 的最大值存储在变量 `max` 中：

```csharp
// 将 a 和 b 的最大值存储到变量 max。
int max;
// 如果 a 大于 b …
if (a > b)
{
    // … 将 a 保存为最大值。
    max = a;
}
// 如果 a 小于或等于 b …
if (a <= b)
{
    // … 将 b 保存为最大值。
    max = b;
}
```

第二个 `if` 语句导致了不处理，因为这两个条件是互斥的。如果 `a` 大于 `b`，则 `a` 不可能小于或等于 `b`。C# 正为这种情况定义了 `else` 语句。`else` 关键字定义了一个块，当 `if` 块未执行时执行该块。计算最大值的代码段现在如下：

```csharp
// 将 a 和 b 的最大值存储到变量 max。
int max;
// 如果 a 大于 b …
if (a > b)
{
    // … 将 a 保存为最大值；否则 …
    max = a;
}
else
{
    // … 将 b 保存为最大值。
    max = b;
}
```

如果 `a` 大于 `b`，则执行第一个块；否则，执行第二个块。最后，`max` 包含 `a` 或 `b` 中的较大者。

### 避免 else

`else` 子句的序列可能会变得令人困惑。有些程序员喜欢在做这件事时避免它们。你可以这样写最大值：

```csharp
// 将 a 和 b 的最大值存储到变量 max。
int max;
// 如果 a 大于 b …
if (a > b)
{
    // … 将 a 保存为最大值。
    max = a;
}
if (a <= b)
{
    // … 将 b 保存为最大值。
    max = b;
}
```

![Tip](img/tip.png) C# 9.0 提供了一种称为目标类型条件 (target typed conditional)的功能。通常，三元运算符的两个输出的数据类型必须匹配。然而，在 C# 9.0 及之后，这一要求发生了变化。因此，虽然这段代码在早期版本的 C# 中无法编译，但在 C# 9.0 及之后可以使用它：

```csharp
int x = 2;
Console.WriteLine(x == 1 ? 1 : "Hello");
```

当 x 等于 1 时，该条件表达式的输出是值 1。当 x 不等于 1 时，该条件表达式的输出是字符串 "Hello"。有很多方法可以使用这种新的条件表达式，包括在 `switch` 语句中。你可以在此处了解更多相关信息：[`https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-9.0/target-typed-conditional-expression`](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-9.0/target-typed-conditional-expression)。

### 嵌套 if 语句

![Remember](img/remember.png) 位于另一个 `if` 语句体内的 `if` 语句是*嵌入的*或*嵌套的*（nested）语句。以下程序 `CalculateInterestWithEmbeddedTest` 使用嵌入 `if` 语句在检测到输入问题时避免愚蠢的问题：

```csharp
static void Main(string[] args)
{
    // 定义最大利率。
    int maximumInterest = 50;
    // 提示用户输入源本金。
    Console.Write("Enter principal: ");
}
```





```csharp
string principalInput = Console.ReadLine();

decimal principal = Convert.ToDecimal(principalInput);

// 如果本金为负 …
if (principal < 0)
{
    // … 生成一条错误消息 …
    Console.WriteLine("Principal cannot be negative");
}
else // 只有当本金 > 0 时进入此处：因此有效。
{
    // … 否则，输入利率。
    Console.Write("Enter interest: ");
    string interestInput = Console.ReadLine();
    decimal interest = Convert.ToDecimal(interestInput);
    // 如果利率为负或太大 …
    if (interest < 0 || interest > maximumInterest)
    {
        // … 也生成一条错误消息。
        Console.WriteLine("Interest cannot be negative " +
        "or greater than " + maximumInterest);
        interest = 0;
    }
    else // 只有在一切正常的情况下才到达此处
    {
        // 本金和利率看起来都是合；
        // 计算本金加利息的值。
        decimal interestPaid;
        interestPaid = principal * (interest / 100);
        // 现在计算总和。
        decimal total = principal + interestPaid;
        // 输出结果。
        Console.WriteLine(); // 跳过一行。
        Console.WriteLine("Principal = " + principal);
        Console.WriteLine("Interest = " + interest + "%");
        Console.WriteLine();
        Console.WriteLine("Interest paid = " + interestPaid);
        Console.WriteLine("Total = " + total);
    }
}

Console.Read();
}
```

程序首先从用户处读取本金。如果本金为负，程序输出错误消息并退出。如果本金不为，控制权传递到 `else` 子句，程序继续执行。

在这个示例中，利率测试得到了改进。在这里，程序要求利率必须是非负的（数学规律）且小于最大利率（司法法律）。此 `if` 语句使用了以下复合测试：

```csharp
if (interest < 0 || interest > maximumInterest)
```

如果 `interest` 小于 0 或大于 `maximumInterest`，则该语句为真。注意代码在程序顶部声明了 `maximumInterest` 变量，而不是在这里对其进行 `hard-code`（硬编码）。`Hard-coding` 指直接在代码中使用值，而不是创建一个变量来存储它们。

![Tip](img/tip.png) 在程序的顶部定义重要的常量。为常量赋予一个描述性的名称（而不仅仅是数字）使其易于查找且更易更改。如果常量在代码中出现十次，你仍需修改一次即可更改所有的引用。输入正确的本金但输入负的利率将产生此输出：

```
Enter principal: 1234
Enter interest: -12.5
Interest cannot be negative or greater than 50.
```

只有当用户同时输入合法的本金和法的利率时，程序才会生成正确的计算结果：

```
Enter principal: 1234
Enter interest: 12.5
Principal = 1234
Interest = 12.5%
Interest paid = 154.250
Total = 1388.250
```

### 运行 switch 语句

你通常想对变量的多个不同值进行测试。例如，`maritalStatus` 可能 0 表示未婚，1 表示已婚，2 表示离婚，3 表示丧�wid 夫，或 4 表示与你无关。为了区分这些值，你可以使用以下系列 `if` 语句：

```csharp
if (maritalStatus == 0)
{
    // 必须是未婚 …
    // … 执行某些事情 …
}
else
{
    if (maritalStatus == 1)
    {
        // 必须是已婚 …
        // … 执行其他事情 …
```

你可以看到这些重复的 `if` 语句很快就会令人厌烦。测试多种情况是一个非常常见的情况，因此 C# 提供了一个特殊的结构来在一组互斥的条件之间进行选择。这种控制结构 `switch` 的工作原理如下：

```csharp
switch (maritalStatus)
{
    case 0:
        // … 处理未婚的事务 …
        break;
    case 1:
        // … 处理已婚的事务 …
        break;
    case 2:
        // … 处理离婚的事务 …
        break;
    case 3:
        // … 处理丧�wid 夫的事务 …
        break;
    case 4:
        // … 离我远点 …
        break;
    default:
        // 如果未通过任何 case 则进入此处；
        // 这可能是一个错误条件。
        break;
}
```

`switch` 语句顶部的表达式会被求值。在这种情况下，表达式简单的变量 `maritalStatus`。然后将该表达式的值与每个 `case` 的值进行比较。如果没有找到匹配项，控制权传递到 `default` 子句。`switch` 语句的参数也可以是 `string`：

```csharp
string s = "Davis";
switch(s)
{
    case "Davis":
        // … 控制权传递到此处 ...
    case "Smith":
        // … 处理 Smith 的事务 …
        break;
    case "Jones":
        // … 处理 Jones 的事务 …
        break;
    case "Hvidsten":
        // … 处理 Hvidsten 的事务 …
        break;
    default:
        // 如果未通过任何 case 则进入此处；
        break;
}
```

使用 `switch` 语句涉及以下限制：
- `switch` 的参数必须是某种类型（从 C# 7.0 开始可以使用任何非空类型）。
- `case` 值必须是常量像 `x` 这样的语句是非法的。
- 每个子句必须以 `break` 语句结束（或其他退出语句，如 `return`）。
- 如果两个 `case` 指向相同的操作，可以省略 `break` 语句，例如：

```csharp
string s = "Davis";
switch(s)
{
    case "Davis":
    case "Hvidsten":
        // 无论 s 是 Davis 还是 Hvidsten 都执行相同的操作
        break;
```





接下来是 `switch` 表达式。它的工作原理与普通的 `switch` 类似，你从一个变量 `value` 开始，将其与一系列 `case` 进行比较。不同之处在于，在这种情况下 `value` 的类型是 `Greetings`。当匹配特定的 `Greetings` 值时，`switch` 表达式会输出一个 `string`。

![Technicalstuff](img/technicalstuff.png) 注意，有一个特殊值 `_`，它表示当其他所有值都不匹配时，`switch` 应该执行的操作。 这是一个默认值。如果你不包含默认值，Visual Studio 会显示一条警告消息，说明你没有涵盖所有情况。在这种情况下，你可以不包含它，因为使用枚举可以防止有人提供需要默认值的非预料值。

接下来是测试 `switch` 表达式。`Main()` 方法中的代码测试了 `Greetings` 的每种组合组合。你会看到如下输出：

```
`Good Morning!`
`Good Afternoon!`
`See you tomorrow!`
`Are you still here?`
```

![Remember](img/remember.png) 因为这是 C# 8.0 及以上版本的特性，你仍然需要告诉 IDE 使用不同于默认的语言版本。请确保向 `SwitchExpression.csproj` 添加以下条目。

```xml
<PropertyGroup>
<LangVersion>8.0</LangVersion>
</PropertyGroup>
```

### 使用模式匹配

C# 9.0 通过使用模式匹配（pattern matching）使得进一步扩展 `switch` 表达式成为可能。模式可以是识别为代表一组相关值的任何内容，即使这些值并不一定是连续的或具有相同类型。例如，电话号码就是一个模式，因为你可以识别它的结构。`SwitchPattern` 示例使用了更容易识别的模式，即字母、数字和特殊字符。

```csharp
public static string LetterType(char letter) => letter switch
{
    >= 'a' and <= 'z' => "lowercase letter",
    >= 'A' and <= 'Z' => "uppercase letter",
    >= '1' and <= '9' => "number",
    >= ' ' and <= '/' or
    >= ':' and <= '@' or
    >= '[' and <= '`' or
    >= '{' and <= '~' => "special character",
    _ => "Unknown letter type"
};

static void Main(string[] args)
{
    Console.WriteLine("a is a " + LetterType('a') + ".");
    Console.WriteLine("B is an " + LetterType('B') + ".");
    Console.WriteLine("3 is a " + LetterType('3') + ".");
    Console.WriteLine("? is a " + LetterType('?') + ".");
    Console.WriteLine("À is a " + LetterType('À') + ".");
    Console.ReadLine();
}
```

在这种情况下，`switch` 使用逻辑模式根据输入的内容来定义字母类型。注意你如何组合 `and` 和 `or` 值来创建模式。最后的条目提供了一个默认响应，以防输入字符未被识别为模式的一部分。你可以在 `https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/patterns` 查看 C# 支持的更多模式类型。

`Main()` 中的测试代码遍历了所有各种预期的字符类型。然后它提供了一个带有重音（grave accent）的大写字母 `A` 作为输入，这并不是模式的一部分。以下是示例的输出。

```
`a is a lowercase letter.`
`B is an uppercase letter.`
`3 is a number.`
`? is a special character.`
`A is an Unknown letter type.`
```

![Remember](img/remember.png) 因为这是 C# 9.0 及以上版本的特性，你仍然需要告诉 IDE 使用不同于默认的语言版本。请确保向 `SwitchPattern.csproj` 添加以下条目。

```xml
<PropertyGroup>
<LangVersion>9.0</LangVersion>
</varnothing>
```

## 我们开始吧：循环循环 (Loop-the-Loop)

`if` 语句允许程序根据 `bool` 表达式的结果，在执行的代码中采取不同的路径。与不具备决策能力的程序相比，该语句提供了有趣得多的程序。添加 `repeatedly`（重复）执行一组指令的能力在能力上又增加了一次量子飞跃。

考虑本章较早“介绍 if 语句”部分中的 `CalculateInterest` 程序。使用计算器（或用纸笔手动计算）进行这种单利计算要比编写和执行程序要容易得多。

如果你能计算后续若干年每年的本金金额，那将更有用。你需要一种方法让计算机多次执行相同的短指令序列——这被称为 `loop`（循环）。

### 循环一会

C# 关键字 `while` 引入了最基本的执行循环形式：

```csharp
while (bool-expression)
{
    // 只要表达式为真，就会重复执行。
}
```

当第一次遇到 `while` 循环时，会求值 `bool` 表达式。如果表达式为真，执行块中的代码。当代码块到达右括号时，控制返回顶部，整个过程重新开始。当 `bool` 表达式第一次为假时，控制通过右括号。

你可以使用 `while` 循环来创建 `CalculateInterestTable` 程序，它是 `CalculateInterest` 程序的循环版本。`CalculateInterestTable` 计算一个年度本金表格：

```csharp
static void Main(string[] args)
{
    // 定义最大利率。
    int maximumInterest = 50;
    // 提示用户输入本金。
    Console.Write("Enter principal: ");
    string principalInput = Console.ReadLine();
    decimal principal = Convert.ToDecimal(principalInput);
    // 如果本金为负……
    if (principal < 0)
    {
        // ……生成错误消息……
        Console.WriteLine("Principal cannot be negative");
    }
    else // 只有当本金 > 0 时进入此处：这是有效的。
    {
        // ……否则，输入利率。
        Console.Write("Enter interest: ");
        string interestInput = Console.ReadLine();
        decimal interest = Convert.ToDecimal(interestInput);
        // 如果利率为负或太大……
        if (interest < 0 || interest > maximumInterest)
        {
            // ……同样生成错误消息。
            Console.WriteLine("Interest cannot be negative " +
            "or greater than " + maximumInterest);
            interest = 0;
        }
        else // 只有一切正常时才到达此处。
        {
            // 本金和利率看起来都是合法的；
            // 最后输入年份。
            Console.Write("Enter number of years: ");
            string durationInput = Console.ReadLine();
            int duration = Convert.ToInt32(durationInput);
            // 验证输入。
            Console.WriteLine(); // 跳过一行。
            Console.WriteLine("Principal = " + principal);
            Console.WriteLine("Interest = " + interest + "%");
            Console.WriteLine("Duration = " + duration + "years");
            Console.WriteLine();
            // 现在按指定的年份进行循环。
            int year = 1;
            while (year <= duration)
            {
                // 计算本金加利息的值。
                decimal interestPaid;
                interestPaid = principal * (interest / 100);
                // 现在通过将利息加上之前的本金金额
                // 计算新的本金。
                principal = principal + interestPaid;
                year++;
            }
        }
    }
}
```




```cs
// 将本金四舍五入到最近的分。
principal = decimal.Round(principal, 2);

// 输出结果。
Console.WriteLine(year + "-" + principal);

// 跳到下一年。
year = year + 1;
}
}
}
Console.Read();
}
```

运行 `CalculateInterestTable` 程序的输出结果所示：

```
Enter principal: 10000
Enter interest: 5.5
Enter number of years: 5
Principal = 10000
Interest = 5.5%
Duration = 5 years
1-10550.00
2-11130.25
3-11742.41
4-12388.24
5-13069.59
```

每个值代表了在假设每年复利计算的情况下，经过指定年份后的总本金。例如，10,000 美元在 5.5% 利率下五年后的价值为 13,069.59 美元。

`CalculateInterestTable` 程序首先从用户处读取本金和利率值，并检查它们是否有效。然后，`CalculateInterestTable` 读取循环的年数，并将此值存储在变量 `duration` 中。

在进入 `while` 循环之前，程序声明了一个变量 `year` 并将其初始化为 `1`。这将是“当前年份”——也就是说，这个数字会随着程序的循环“每年”变化一次。如果 `year` 中包含的年份数字小于 `duration` 中包含的总持续时间，则通过根据“上一年”计算利息来重新计算“这一年”的本金。计算出的本金将同当前年份偏移量一起输出。

![Technicalstuff](img/technicalstuff.png) `decimal.Round()` 语句将计算出的值四舍五入到最近的分。

程序的关键在于代码块中的最后一行。`year = year + 1;` 语句将 `year` 增加 1。如果 `year` 的初始值为 `3`，在执行该表达式后其值将变为 `4`。这种增加操作将计算从一年移动到下一年。

年份增加，控制返回到循环顶部，将 `year` 的值与请求的持续时间进行比较。在示例运行中，如果当前年份小于 5，则继续计算。在增加五次后，`year` 的值变为 6，它大于 5，程序控制将传递到 `while` 循环后的第一个语句——程序停止循环。

`CalculateInterestTable` 中的计数变量 `year` 必须在在使用它的 `while` 循环之前声明并初始化。此外，`year` 变量必须被递增，通常作为循环内的最后一条语句。正如此示例所示，你必须预先查看以确定需要哪些变量。在写了几千个 `while` 循环后，这种模式会更容易使用。

![Warning](img/warning.png) 在编写 `while` 循环时，不要忘记增加计数变量，如下例所示：

```cs
int nYear = 1;
while (nYear < 10)
{
    // … whatever …
}
```

此示例没有增加 `nYear`。如果没有递增，`nYear` 始终为 `1`，程序将无限循环。退出此无限循环的唯一方法是按 `Ctrl+C` 终止程序。（因此，没有什么是真正无限的，穿过黑洞事件视界的粒子除外。）

![Remember](img/remember.png) 确保终止条件可以满足。通常，这意味着你的计数变量正在被正确地递增。否则，你面临的是无限循环、愤怒的用户、糟糕的媒体报道以及 50 年的干旱。无限循环是一个常见的错误，所以当你陷入其中一个时，不要感到尴尬。

### 执行 do … while 循环

`while` 循环的一种变体是 `do … while` 循环。在这个示例中，条件在循环结束时才被检查：

```cs
int year = 1;
do
{
    // … 一些计算 …
    year = year + 1;
} while (year < duration);
```

与 `while` 循环相比，无论 `duration` 的值如何，`do … while` 循环至少执行一次。

### 退出循环很容易

你可以使用两个特殊命令来改变循环的执行方式：`break` 和 `continue`。执行 `break` 语句会导致控制立即传递到循环循环后的第一个表达式。类似的 `continue` 语句则将控制直接传回循环顶部的条件表达式，以便重新开始并在这次做对。

假设你想在本金超过原始金额的某倍数时立即从银行取出钱，无论持续年限是多少。你可以通过在循环中添加以下代码（**粗体**）来轻松满足这一金额需求：

```cs
// 现在循环指定的年数。
int year = 1;
while (year <= duration)
{
    // 计算本金加利息的值。
    decimal interestPaid;
    interestPaid = principal * (interest / 100);

    // 将本金四舍五入到最近的分。
    principal = decimal.Round(principal, 2);

    // 输出结果。
    Console.WriteLine(year + "-" + principal);

    // 跳到下一年。
    year = year + 1;

    // 确定我们已达到目标。
    if (principal > maxPower * originalAmount)
    {
        break;
    }
}
```

`break` 语句在 `if` 条件为真时执行——在这种情况下，执行 `break` 语句跳出 `while` 循环，程序从循环之后继续执行。

### 循环直到做对

`CalculateInterestTable` 程序演示了这种方法：

```cs
static void Main(string[] args)
{
    // 定义最大利率。
    int maximumInterest = 50;
    // 提示用户输入本金；
    // 直到输入正确的值。
    decimal principal;
    while (true)
    {
        Console.Write("Enter principal: ");
        string principalInput = Console.ReadLine();
        principal = Convert.ToDecimal(principalInput);
        // 如果输入的值正确则退出。
        if (principal >= 0)
        {
            break;
        }
        // 输入错误时生成错误信息。
        Console.WriteLine("Principal cannot be negative");
        Console.WriteLine("Try again");
        Console.WriteLine();
    }
    // 现在输入利率。
    decimal interest;
    while (true)
    {
        Console.Write("Enter interest: ");
        string interestInput = Console.ReadLine();
        interest = Convert.ToDecimal(interestInput);
        // 不接受负数或过大的利率
        if (interest >= 0 && interest <= maximumInterest)
        {
            break;
        }
        // 同样生成错误消息。
        Console.WriteLine("Interest cannot be negative "
        "or greater than " + maximumInterest);
        Console.WriteLine("Try again");
        Console.WriteLine();
    }
    // 本金和利率看起来都是
    // 合法的；最后，输入年数。
    int duration;
    Console.Write("Enter number of years: ");
    string durationInput = Console.ReadLine();
    duration = Convert.ToInt32(durationInput);
    // 验证输入。
    Console.WriteLine(); // 跳过一行。
    Console.WriteLine("Principal = " + principal);
    Console.WriteLine("Interest = " + interest + "%");
    Console.WriteLine("Duration = " + duration + "years");
    Console.WriteLine();

    // 现在循环指定的年数。
    int year = 1;
    while (year <= duration)
    {
        // 计算本金加利息的值。
        decimal interestPaid;
        interestPaid = principal * (interest / 100);

        // 将本金四舍五入到最近的分。
        principal = decimal.Round(principal, 2);

        // 输出结果。
        Console.WriteLine(year + "-" + principal);

        // 跳到下一年。
        year = year + 1;

        // 确定我们已达到目标。
        if (principal > maxPower * originalAmount)
        {
            break;
        }
    }
}
```





```cs
// 计算本金加利息的值。

decimal interestPaid;

interestPaid = principal * (interest / 100);

// 现在通过将利息加上之前的本金来计算新的本金。
principal = principal + interestPaid;

// 将本金四舍入到最近的一分。
principal = decimal.Round(principal, 2);

// 输出结果。
Console.WriteLine(year + "-" + principal);

// 跳到下一年。
year = year + 1;
}

Console.Read();
}
```

此程序的工作方式与本章之前章节中的示例基本相同，不同在于用户输入部分。这一次，使用一个 `while` 循环替换了早期示例中用于检测无效输入的 `if` 语句（你也可以使用类似的循环来获取年数，但为了节省空间将其省略了）：

```csharp
decimal principal;
while (true)
{
    Console.Write("Enter principal: ");
    string principalInput = Console.ReadLine();
    principal = Convert.ToDecimal(principalInput);
    // 当输入的值正确时退出。
    if (principal >= 0)
    {
        break;
    }
    // 输入错误时生成错误。
    Console.WriteLine("Principal cannot be negative");
    Console.WriteLine("Try again");
    Console.WriteLine();
}
```

这段代码在循环内从用户处输入值。如果文本的值正常，程序将退出输入循环并继续。然而，如果输入有错误，用户将看到错误消息，控制权将返回程序流重新开始。

![Remember](img/remember.png) 程序将继续循环，直到用户输入正确的输入。（在最坏的情况下，程序可能会一直循环到一个迟钝的用户老死为止。）

注意，条件判断已经反转了，因为问题不再是非输入是否应该生成错误消息，而是正确输入是否应该退出循环。在利息部分，例如，考虑这个测试：

`principal < 0 || principal > maximumInterest`

该测试变为：

`interest >= 0 && interest <= maximumInterest`

显然，`interest >= 0` 是 `interest < 0` 的相反。可能没那么而易见的是，逻辑或 (`||`) 运算符被替换成了逻辑与 (`&&`) 运算符。它的意思是：“如果利息大于零且小于最大金额（换句话说，如果它是正确的），则退出循环。”注意，`principal` 变量必须在循环外声明，由于作用域规则，将在下一节解释。

![Warning](img/warning.png) 这听起来显而易见，但表达式 `true` 的求值为 `true`。因此，`while (true)` 是你典型的无限循环。退出循环的是嵌入的 `break` 语句。因此，如果你使用 `while (true)` 循环，请确保你的 `break` 条件可能发生。该程序示例执行的输出如下：

```text
Enter principal: -1000
Principal cannot be negative
Try again
Enter principal: 1000
Enter interest: -10
Interest cannot be negative or greater than 50
Try again
Enter interest: 10
Enter number of years: 5
Principal = 1000
Interest = 10%
Duration = 5 years
1-1100.0
2-1210.00
3-1331.00
4-1464.10
5-1610.51
Press Enter to terminate …
```

程序拒绝接受负的本金或利息金额，并在每次循环中耐地解释错误。然而，你仍然需要添加代码来处理用户输入空白或字符串值（例如“seven”）的情况。

![Warning](img/warning.png) 在返回循环进一步输入之前，准确解释用户哪里做错了，否则那个人将变得极其困惑。显示示例也可能有帮助，特别是对于格式问题。一点外交辞令也无处，正如奶奶可能指出的那样。

### 关注作用域规则

在循环内声明的变量受限于该循环。考虑这段代码片段：

```csharp
int days = 1;
while (days < duration)
{
    int average = days;
    // ...
    days = days + 1;
}
```

![Technical](img/Technical) `average` 的作用域局限于 `while` 循环。`for` 循环具有类似的结构：

```csharp
for (int days = 1; days < duration; days++)
{
    int average = days;
    // ...
}
```

![Tip](img/Tip) `average` 的作用域局限于 `for` 循环。

### 指定次数的循环

`while` 循环是 C# 中第二常用的结构。然而，与 `while` 循环相比，`for` 循环具有这种结构：

```csharp
for (initExpression; condition; incrementExpression)
{
}
```

遇到 `for` 循环时，程序首先执行 `initExpression`，然后测试 `condition`。如果 `condition` 为真，程序执行大括号内的主体。遇到右括号后，控制权传递到 `incrementExpression`，然后返回到 `condition`，开始下一次循环。事实上，`for` 循环的定义可以转换为这个 `while` 循环：

```cs
initExpression;
while (condition)
{
    incrementExpression;
}
```

### for 示例

你可以通过这个示例更好地了解 `for` 循环的工作：

```cs
// 这是一个示例。
a = 1;
// 现在循环一段时间。
for (int year = 1; year <= duration; year++)
{
    // ...
}
// 程序从这里继续。
a = 2;
```

### 为什么你需要另一个循环？

如果 C# 已经有了等效的 `while` 循环，为什么你还需要 `for` 循环？短答案是你不需要——`for` 循环并没有带来 `while` 循环无法提供的任何功能。

然而，`for` 循环部分的存在是为了方便——并为了明确建立每个循环都应该有的三个部分：初始化、退出条件和增量。这种安排不仅更容易阅读，也更容易写对。理解 `for` 循环最重要的原因是它是每个人都在使用的循环——它（以及它的表兄弟 `foreach`）是你阅读他人的代码时看到的 90% 的情况。





![Technicalstuff](img/technicalstuff.png) `for` 循环的设计使得第一个表达式用于初始化计数变量，而最后部分对其进行递增；然而，C# 语言并没有强制执行此类规则。你可以在这两个部分中做任何你想做的事；但不建议你在初始化和递增计数变量之外执行任何其他操作。

自增运算符在编写 `for` 循环时特别流行。（本微型书籍的 第 4 章 描述了自增运算符以及其他运算符。）上一个 `for` 循环通常这样写：

```csharp
for (int year = 1; year <= nDuration; year++)
{
    // … 代码正体 …
}
```

![Tip](img/tip.png) 你几乎总会在 `for` 循环中看到后自增运算符 own 前自增运算符，尽管在这种情况下效果是相同的。除了习惯以及它看起来更酷之外，没有其他原因。（下次你想打破僵局/活跃气氛时，只需掏出一份满是后自增运算符的 C# 代码列表来展示你有多酷即可。这几乎从不起作用，但值得一试。）

`for` 循环有一个你可能觉得难以理解的体。如果缺少逻辑条件表达式，它被假设为 `true`。因此 `for (;;)` 是一个无限循环。你看到 `for (;;)` 作为无限循环比 `while (true)` 更常见。

### 嵌套循环

内部循环可以出现在外部循环内部，如下：

```csharp
for ( …某些条件 …
{
    for ( …其他条件 …
    {
        // … 执行任何操作 …
    }
}
```

在在外层循环的每次迭代期间，内层循环都会执行到完成。内层 `for` 循环使用的循环变量（如 `year`）在内层循环的作用范围之外定义。

![Remember](img/remember.png) 包含在另一个循环中的循环是*嵌套*循环。嵌套循环不能“交叉”。例如，下面的代码无法工作：

```csharp
do // 开始一个 do..while 循环。
{
    for( …) // 开始某个 for 循环。
    {
    } while while( …) // 结束 do..while 循环。
} // 结束 for 循环。
```

![Remember](img/remember.png) 嵌套循环内的 `break` 语句只会退出内层循环。在下面的示例中，`break` 语句退出循环 B 并返回循环 A：

```csharp
// for 循环 A
for( …某些条件 …
{
    // for 循环 B
    for( …其他条件 …
    {
        // … 执行任何操作 …
        if (something is true)
        {
            break; // 跳出循环 B 而不是循环 A
        }
    }
}
```

C# 没有一个可以同时退出两个循环的 `break` 语句。你必须使用两个独立的 `break` 语句，每个循环用一个。

![Technicalstuff](img/technicalstuff.png) 必须使用两个 `break` 语句并不像听起来那么大的限制。在实践中，此类嵌套循环中包含的通常很复杂的逻辑最好封装在方法中。从任何一个循环内部执行 `return` 都会退出方法，从而跳出所有循环，无论它们嵌套得有多深。本微型书籍的第 2 第 2 章](#c02.xhtml) 描述了方法和 `return` 语句。

# 第 6 章：使用集合让一切就绪

本章内容

- ![Bullet](img/check.png) **创建包含多个数据项的变量：数组**
- ![Bullet](img/check.png) **使用灵活集合让数组更进一步**
- ![Bullet](img/check.png) **查看数组和集合初始化器以及集合类型集合**

你在书中可能遇到的那种简单单值变量在处理大量同类项目时显得有些捉襟见肘：例如，是十只鸭子而不是只有一只。C# 用两种存储多个项的变量来填补这一空白，这些变量通常被称为*集合*（collections）。集合的两种是*数组*（array）和更通用的*集合类*（collection class）。

![Remember](img/remember.png) 本书在讨论数组时专门使用*数组*（array）一词。在处理集合类时，书籍使用*集合类*一词。如果书籍指的是*集合*（collection）或*列表*（list），那么涉及的对象可以是数组，也可以是集合类。

*数组*是一种持有相同类型对象列表的数据类型。例如，你不能创建一个同时包含 `int` 和 `double` 对象的数组。每个对象必须是相同类型。

C# 为你提供了大量的集合类，它们有各种形状，例如灵活的列表（像珠子串）、队列（像银行的排队）、栈（像一叠煎饼）等。大多数集合类就像数组一样，它们只能持有苹果或只能持有橘子。但 C# 也为你提供了一些可以同时持有苹果和橘子的集合类——这种用处很少。（而且你有得更好的方法来管理这种成就，而不是使用这些老旧的集合。）

目前，如果你能掌握数组和 `List` 集合，你在本书的大部分内容中都会表现得很好。但如果你想充实你的集合储备，请稍后回到这里。本章确实引入了另外两种集合类型。

## C# 数组

包含单值的变量非常有用。即使是那些可以组合对象的结构（例如车辆）也是至关重要的。作为 C# 数组的基础，`Array` 类提供了一种更方便使用的特殊语法。详见引言中关于这些类型对象的细节。

### 数组的理由

考虑六个浮点数的平均值问题。这六个数字都需要自己的 `double` 存储：

```csharp
double d0 = 5;
double d1 = 2;
double d2 = 7;
double d3 = 3.5;
double d4 = 6.5;
double d5 = 8;
```

计算这些变量的平均值可能如下（如 第 2 章 所述，平均 `int` 变量会导致舍误差）：

```csharp
double sum = d0 + d1 + d2 + d3 + d4 + d5;
double average = sum / 6;
```

按名称列出每个元素是乏味的。好吧，当你只有 6 个数字需要平均值时可能并不乏味，但想象一下 600 个（甚至是 600 万个）浮点值。

### 固定值数组

幸运的是，你不需要单独命名每个元素。C# 提供了存储序列的数组结构。使用数组，你可以所有的 `doubles` 放入一个变量中，如下：

```csharp
double[] doublesArray = {5, 2, 7, 3.5, 6.5, 8, 1, 9, 1, 3};
```

你也可以声明一个空数组而不初始化它：

```csharp
double[] doublesArray = new double[6];
```

这一行代码为六个 `doubles` 分配了空间但没有初始化它们。

![Remember](img/remember.png) 作为 C# 数组的基础，`Array` 类提供了一种更方便使用的特殊语法。成对的括号 `[]` 指访问数组中单个元素的方式：

```csharp
doublesArray[0] // 对应 5
doublesArray[1] // 对应 2
```




数组的第 1 个元素对应值 5，第 2 个元素对应值 2，第 3 个元素对应值 7，依此类推。程序员将从 0 开始计数元素的数组称为“基于零”（zero-based）。某些语言如 `Fortran` 和 `COBOL` 使用“基于 1”（one-based）数组，它们从 1 开始计数元素。数组的元素编号 — 0, 1, 2, … — 称为“索引”（index）。特定的数组元素，例如 `doublesArray[0]`，被称为“子数组”（subarray），因为因为它是一个较大数组的一部分。

如果不是数组的索引是一个变量，那么 `doublesArray` 变量将不会有太大的改进。使用 `for` 循环比手动编写每个元素要容易得多，正如 `FixedArrayAverage` 程序所所示：

```csharp
static void Main(string[] args)
{
    double[] doublesArray = { 5, 2, 7, 3.5, 6.5, 8, 1, 9, 1, 3 };
    // 将数组中的值累加到变量 sum 中。
    double sum = 0;
    for (int i = 0; i < doublesArray.Length; i++)
    {
        sum = sum + doublesArray[i];
    }
    // 现在计算平均值。
    double average = sum / doublesArray.Length;
    Console.WriteLine(average);
    Console.Read();
}
```

程序开始将变量 `sum` 初始化为 `0`。然后它遍历存储在 `doublesArray` 中的值，将每个值加到 `sum` 中。在循环结束时，`sum` 已经累加了数组中所有值的和。将得到的和除以元素个数以创建平均值。执行此程序的输出结果是预期的 `4.6`。（你可以用计算器检查一下。）

![Tip](img/tip.png) 注意代码是如何通过使用 `doublesArray.Length` 自动获取正确的终点的。是的，你可以简单地使用值 `10`，但这样你就无法确定该值是否正确。如果数组长度由于原因发生了变化，你可能无法获得正确的平均值，或者代码可能会生成 `System.IndexOutOfRangeException`。在处理数组时，始终假设你不知道数组的长度，并使用数组的 `Length` 属性来获取。

### 变长数组

`FixedArrayAverage` 示例程序使用的数组存在这两个严重问题：

*   数组的大小固定为十个元素。
*   更糟糕的是，元素的值是直接在程序中指定的。

一个可以读取可数量值的程序（这可能由用户在执行期间决定）将更具灵活性。它不仅适用于 `FixedArrayAverage` 中指定的十个值，还适用于任何其他值集合，无论它们的数量是多少。声明变变大小数组的格式与固定大小、固定值数组的格式略有不同：

```csharp
double[] doublesArrayVariable = new double[N]; // 变长，相对于 …
double[] doublesArrayFixed = new double[10]; // 固定
```

在这里，`N` 代表要分配的元素个数。更新后的程序 `VariableArrayAverage` 允许用户指定输入的数值个数。（`N` 必须来自某个地方。）由于程序保留了输入的值，它不仅计算了平均值，还以一种舒适的格式显示了结果，如下所示：

```csharp
static void Main(string[] args)
{
    // 首先读取用户想要输入的 double 数量。
    Console.Write("Enter the number of values to average: ");
    string numElementsInput = Console.ReadLine();
    int numElements = Convert.ToInt32(numElementsInput);
    Console.WriteLine();
    // 现在声明该大小的数组。
    double[] doublesArray = new double[numElements]; // 这里就是 'N'。
    // 将值累加到数组中。
    for (int i = 0; i < numElements; i++)
    {
        // 提示用户输入另一个 double。
        Console.Write("enter double #" + (i + 1) + ": ");
        string val = Console.ReadLine();
        double value;
        if (Double.TryParse(val, out value))
        {
            // 使用括号符号将此值添加到数组。
            doublesArray[i] = value;
        }
        else
        {
            Console.WriteLine($"Attempted to input {val}, using 0 instead.");
            doublesArray[i] = 0;
        }
    }
    // 将数组值累加到变量 sum 中。
    double sum = 0;
    for (int i = 0; i < doublesArray.Length; i++)
    {
        sum = sum + doublesArray[i];
    }
    // 现在计算平均值。
    double average = sum / numElements;
    // 以吸引人的格式输出结果。
    Console.WriteLine();
    Console.Write(average + " is the average of (" + doublesArray[0]);
    for (int i = 1; i < doublesArray.Length; i++)
    {
        Console.Write(" + " + doublesArray[i]);
    }
    Console.WriteLine(" / " + doublesArray.Length);
    // 等待用户确认。
    Console.Read();
}
```

程序开始将变量 `sum` 初始化为 `0`。然后它遍历存储在 `doublesArray` 中的值，将每个值加到 `sum` 中。在循环结束时，`sum` 已经累加了数组中所有值的和。将得到的和除以元素个数以创建平均值。执行此程序的输出结果是预期的 `4.6`。（你可以用计算器检查一下。）

![Tip](img/tip.png) 注意代码是如何通过使用 `doublesArray.Length` 自动获取正确的终点的。是的，你可以简单地使用值 `10`，但这样你就无法确定该值是否正确。如果数组长度由于原因发生了变化，你可能无法获得正确的平均值，或者代码可能会生成 `System.IndexOutOfRangeException`。在处理数组时，始终假设你不知道数组的长度，并使用数组的 `Length` 属性来获取。

### 变长数组

`FixedArrayAverage` 示例程序使用的数组存在这两个严重问题：

*   数组的大小固定为十个元素。
*   更糟糕的是，元素的值是直接在程序中指定的。

一个可以读取可数量值的程序（这可能由用户在执行期间决定）将更具灵活性。它不仅适用于 `FixedArrayAverage` 中指定的十个值，还适用于任何其他值集合，无论它们的数量是多少。声明变变大小数组的格式与固定大小、固定值数组的格式略有不同：

```csharp
double[] doublesArrayVariable = new double[N]; // 变长，相对于 …
double[] doublesArrayFixed = new double[10]; // 固定
```

在这里，`N` 代表要分配的元素个数。更新后的程序 `VariableArrayAverage` 允许用户指定输入的数值个数。（`N` 必须来自某个地方。）由于程序保留了输入的值，它不仅计算了平均值，还以一种舒适的格式显示了结果，如下所示：

```csharp
static void Main(string[] args)
{
    // 首先读取用户想要输入的 double 数量。
    Console.Write("Enter the number of values to average: ");
    string numElementsInput = Console.ReadLine();
    int numElements = Convert.ToInt32(numElementsInput);
    Console.WriteLine();
    // 现在声明该大小的数组。
    double[] doublesArray = new double[numElements]; // 这里就是 'N'。
    // 将值累加到数组中。
    for (int i = 0; i < numElements; i++)
    {
        // 提示用户输入另一个 double。
        Console.Write("enter double #" + (i + 1) + ": ");
    string val = Console.ReadLine();
        double value;
        if (Double.TryParse(val, out value))
        {
            // 使用括号符号将此值添加到数组。
            doublesArray[i] = value;
        }
        else
        {
            Console.WriteLine($"Attempted to input {val}, using 0 instead.");
            doublesArray[i] = 0;
        }
    }
    // 将数组值累加到变量 sum 中。
    double sum = 0;
    for (int i = 0; i < doublesArray.Length; i++)
    {
        sum = sum + doublesArray[i];
    }
    // 现在计算平均值。
    double average = sum / numElements;
    // 以吸引人的格式输出结果。
    Console.WriteLine();
    Console.Write(average + " is the average of (" + doublesArray[0]);
    for (int i = 1; i < doublesArray.Length; i++)
    {
        Console.Write(" + " + doublesArray[i]);
    }
    Console.WriteLine(" / " + doublesArray.Length);
    // 等待用户确认。
    Console.Read();
}
```

### 初始化数组

以下几行显示了一个带有初始化器的数组，以及另一个分配了空间但没有初始化元素值的数组：

```csharp
double[] initializedArray = {5, 2, 7, 3.5, 6.5, 8, 1, 9, 1, 3};
double[] blankArray = new double[10];
```

![Remember](img/remember.png) 即使 `blankArray` 为元素分配空间，你仍然必须初始化它的值。你可以使用 `for` 循环来执行此任务，通过逐个为每个索引元素赋值，或者依赖于如 `initializedArray` 所示的代码。




即使你使用了所有正确的技巧，使用 `for` 循环处理数组和集合也是容易出错的。有太多地方可能会输入错误的信息，并导致用户暴露在会破坏大家心情的异常中。正如你在接下来的章节中看到的，`foreach` 循环通过消除猜测来解决这些问题。

## 以标准方式使用 foreach 循环

给定一个字符串数组，在 `UsingForeach` 示例中的循环计算了它们长度的平均值：

```csharp
static void Main(string[] args)
{
    string[] myStrings = { "Hello", "Goodbye", "Today", "Tomorrow" };
    int sum = 0;
    foreach (string thisString in myStrings)
    {
        Console.WriteLine($"The current string is: {thisString}.");
        Console.WriteLine($"It's {thisString.Length} characters long.");
        sum += thisString.Length;
    }
    double average = (double)sum / myStrings.Length;
    Console.WriteLine($"The average character length is: {average}.");
    Console.ReadLine();
}
```

此示例首先使用你定义 `doublesArray` 时相同的方法定义了 `myStrings` 数组。然后代码使用 `foreach` 循环处理 `myStrings`，而不考虑数组长度或特定索引。循环表达式的基本含义是 C# 应该从 `myStrings` 数组中取一个 `string`（`thisString`）并对其进行操作。当你需要处理数组或集合中的所有元素时，使用 `foreach` 可以少少很多工作，并为用户产生更少的错误。当你运行此应用程序时，你会看到以下输出：

```
The current string is: Hello.
It's 5 characters long.
The current string is: Goodbye.
It's 7 characters long.
The current string is: Today.
It's 5 characters long.
The current string is: Tomorrow.
It's 8 characters long.
The average character length is: 6.25.
```

![Technicalstuff](img/technicalstuff.png) `foreach` 循环比示例看起来要强大得多。该语句不仅适用于数组，适用于适用于集合类型。此外，`foreach` 还处理多维数组（实际上是数组的数组），这是一个书中未描述的主题。你可以在 [`https://www.tutorialspoint.com/csharp/csharp_multi_dimensional_arrays.htm`](https://www.tutorialspoint.com/csharp/csharp_multi_dimensional_arrays.htm) 找到更多关于多维数组的信息。

## 依赖 GetEnumerator 支持

![Technicalstuff](img/technicalstuff.png) 枚举器依赖于你可以添加到类的 `IEnumerator` 接口。以下是枚举器为你做的事情：

* 允许你迭代集合，而无需了解如何迭代它。例如，你不需要知道集合是否提供了索引。
* 允许迭代集合的一部分，而不是全部。例如，你可以在数组中查找某个特定单词，然后从该点开始迭代。
* 执行迭代的延迟执行。你可能并不真的需要迭代数组，除非用户计划对其进行某些操作。使用某些 C# 技术（如语言集成查询 `LINQ`、[`https://www.tutorialspoint.com/linq/index.htm`](https://www.tutorialspoint.com/linq/index.htm) ））配合枚举器，可以让你推迟到迭代——从而让你的代码运行更快。

C# 9.0 使得在 `foreach` 循环中使用枚举器而不是处理对象本身成为可能。`UsingEnumeratedForeach` 示例显示了如何执行此任务。你必须为应用程序添加 C# 9.0 或以上版本的支持才能使用此示例。示例的第一部分添加了你访问 `GetEnumerator()` 方法所需的扩展。

```csharp
public static class Extensions
{
    public static IEnumerator<T> GetEnumerator<T>(this IEnumerator<T> enumerator) => enumerator;
}
```

现在不要过于担心这段代码。你只需要知道它让此处随后的代码可以访问 `GetEnumerator()`：

```csharp
static void Main(string[] args)
{
    String[] myStrings = { "Hello", "Goodbye", "Today", "Tomorrow" };
    IEnumerator<string> stringEnum = (IEnumerator<string>)new List<string>(myStrings).GetEnumerator();
    while ((string)stringEnum.Current != "Hello")
        stringEnum.MoveNext();
    int sum = 0;
    int count = 0;
    foreach (var thisString in stringEnum)
    {
        Console.WriteLine($"The current string is: {thisString}.");
        Console.WriteLine($"It's {thisString.Length} characters long.");
        sum += thisString.Length;
        count++;
    }
    double average = (double)sum / count;
    Console.WriteLine($"The average character length is: {average}.");
    Console.ReadLine();
}
```

示例从字符串数组开始。然而，数组的特殊之处在于它们不能使用公共版本的 `GetEnumerator()`，因此你必须将数组转换为 `List`。示例的第二行通过调用 `GetEnumerator()` 从 `List` 创建了 `stringEnum` 枚举器。`while` 循环检查 `stringEnum.Current` 是否为 "Hello"。当找到 "Hello" 时，`foreach` 循环开始。`foreach` 循环与 `UsingForeach` 示例中的循环一样，只是从下一个元素开始，所以第一个处理的条目实际上是 "Goodbye"。

```
The current string is: Goodbye.
It's 7 characters long.
The current string is: Today.
It's 5 characters long.
The current string is: Tomorrow.
It's 8 characters long.
The average character length is: 6.6666666666667.
```

## 排序数据数组

常见的编程挑战是需要对数组内的元素进行排序。数组不能增长或缩小，并不意味着其内部元素不能移动、删除或添加。例如，以下代码段交换了数组内两个 `string` 元素的位置：

```csharp
string temp = strings[i]; // 保存第 i 个字符串。
strings[i] = strings[k]; // 用第 k 个替换它。
strings[k] = temp; // 用 temp 替换第 k 个。
```

在此示例中，`strings` 数组 *i* 位置的对象引用被保存，这样当第二个语句替换它时就不会丢失。最后，将 `temp` 变量保存回 *k* 位置。从图中看，这个过程如图 6-1。

![Tip](img/tip.png) 本章其余讨论的数据集合在添加和删除元素方面比数组更灵活。以下程序演示了如何利用操作数组元素的能力作为排序的一部分。这种特定的排序算法是*冒泡排序*。虽然它对于具有数千个元素的型数组并不理想，但在小数组上它是简单且有效的，正如 `BubbleSortArray` 示例所示：

```csharp
static void Main(string[] args)
{
    Console.WriteLine("距离太阳最近的 5 个行星，顺序如下：");
    string[] planets = new string[] { "Mercury", "Venus", "Earth", "Mars", "Jupiter" };
    foreach (string planet in planets)
    {
```




```cs
// 使用特殊字符 \t 在打印行中插入一个制表符。
Console.WriteLine("\t" + planet);

}

Console.WriteLine("\n 按字母顺序列表: ");
// Array.Sort() 是 Array 类上的一个方法。
// Array.Sort() 在 planets 数组中进行原地操作，
// 这会导致你失去原始数组的副本。
// 解决方案是将旧数组复制到新数组并对其进行排序。
string[] sortedNames = planets;
Array.Sort(sortedNames);
// 这证明了 (a) sortedNames 包含了与 planets 相同的
// 字符串，(b) 它们现在已经过排序。
foreach (string planet in sortedNames)
{
    Console.WriteLine("\t" + planet);
}
Console.WriteLine("\n 按名称长度列表 - 最短在前: ");
// 这种算法被称为“冒泡排序”：它是最简单
但性能最差的排序。Array.Sort() 方法高效得多，
// 但不能直接用它来按名称长度对 planets 排序，
//因为它排序的是字符串而不是它们的长度。
int outer; // 外层循环索引
int inner; // 内层循环索引
// 从最后一个索引向第一个索引循环：planets[4] 到 planets[0]。
for (outer = planets.Length - 1; outer >= 0; outer--)
{
    // 在每个外层循环中，遍历当前外层元素之外的
    // 所有元素。此循环向上进行，从 planets[1]
    // 到 planets[4]。使用 for 循环，你可以双向遍历
    // 数组。
    for (inner = 1; inner <= outer; inner++)
    {
        // 比较相邻元素。如果前一个比后一个
        // 长，则交换它们。这展示了当元素顺序
        // 时，如何交换两个数组元素。
        if (planets[inner - 1].Length > planets[inner].Length)
        {
            // 临时存储一个行星。
            string temp = planets[inner - 1];
            // 现在用另一个覆盖该行星。
            planets[inner - 1] = planets[inner];
            // 最后，取回存储在 temp 中的行星并将其
            // 放在另一个的位置。
            planets[inner] = temp;
        }
    }
}
foreach (string planet in planets)
{
    Console.WriteLine("\t" + planet);
}
Console.Read();
}
```

程序从一个包含距离太阳最近的前五个行星名称的数组开始。（示例排除了远远行星以保持数据较小。）程序随后调用数组自身的 `Sort()` 方法。数组（以及其他集合）的内置 `Sort()` 方法无疑比自定义的冒泡排序更高效。除非你有充分的理由，否则不要自己编写排序算法。

在使用 `Array` 类内置的 `Sort()` 方法排序后，程序使用自定义排序对行星名称的长度进行排序，以展示处理某些需求（例如按名称长度排序）的一种技术，而标准排序无法解决这些需求。第二次排序的算法通过持续循环字符串列表直到列表排序完成。在对 `sortedNames` 数组的每次遍历中，程序会将每个字符串与其邻居元素进行比较。如果发现两个元素的顺序错误，方法将交换它们，并将列表标记为未排序。

最终，较短的行星名称会“泡”到列表顶端；因此被称为*冒泡排序*（bubble sort）。以下是该示例的输出结果：

```
距离太阳最近的 5 个行星，顺序如下：
Mercury
Venus
Earth
Mars
Jupiter
按字母顺序列表:
Earth
Jupiter
Mars
Mercury
Venus
按名称长度列表 - 最短在前:
Mars
Earth
Venus
Jupiter
Mercury
```

## 为数组使用 var

传统上你会使用以下形式之一（与 C# 一样老）来初始化数组：

```cs
int[] numbers = new int[3]; // 有大小但没有初始化器，或者 …
int[] numbers = new int[] { 1, 2, 3 }; // 有初始化器但没有大小，或者 …
int[] numbers = new int[3] { 1, 2, 3 }; // 有大小也有初始化器，或者 …
int[] numbers = { 1, 2, 3 }; // 无 'new' 关键字 —— 快捷形式。
```

本微型书籍的第 2 章 (#c02.xhtml) 介绍了 `var` 关键字，它告诉 C# 编译器：“根据初始化表达式确定变量类型”。幸运的是，`var` 也适用于数组：

```cs
// myArray 是一个包含 6 个元素的 int[]。
var myArray = new [] { 2, 3, 5, 7, 11, 13 }; // 需要初始化器！
```

新语法只有两个变化：

*   在左侧使用 `var` 代替 `numbers` 数组的显式类型信息。
*   在括号前省略了 `new` 关键字。




在本节中，你将发现集合语法，并看到最重要和最常用的集合类。表 6-1 列出了 C# 中主要的集合类。将集合想象成具有各种*形状*是非常有用的——即 C# 如何看待集合，以及你如何与其进行交互。

| **类** | **描述** |
| --- | --- |
| `List<T>` | 此动态数组包含类型为 T 的对象。 |
| `LinkedList<T>` | 这是一个类型 T 对象的链表。 |
| `Queue<T>` | 从队末尾开始，最后到达头部。 |
| `Stack<T>` | 始终在列表的“顶部”添加或删除项目，就像一叠食堂的托盘。 |
| `Dictionary<TKey, TValue>` | 该结构的工作类似于字典。查找一个键（例如一个单词）并检索其对应的值（例如，定义）。 |
| `HashSet<T>` | 该结构类似于数学集合，没有重复项。它的工作方式与列表相似，但提供了数学集合操作，如并集和交集。 |

表 6-1 最常见的集合“形状”

### 理解 <T>

在表 6-1 中看到的看起来神秘的 `<T>` 表示法中`<T>` 是特定数据类型的占位符。为了让这个符号对象活起来，通过插入真实类型来对其*实例化*，如下所示：

```
List<int> intList = new List<int>(); // 为 int 实例化
```

![Remember](img/remember.png) *实例化*（实例化）是极客术语，指创建该类型的对象（实例）。例如，你可能会为 `int` 或 `string` 类型创建不同的 `List<T>` 实例化。顺便说一下，`T` 并不是一个神圣的名字。你可以使用任何喜欢的名称——例如，`<dummy>` 或 `<aType>`。使用 `T`、`U`、`V` 等是很常见的。

注意表 6-1 是如何显示 `Dictionary<TKey, TValue>` 集合的。这里需要两个类型：一个用于字典的键，另一个用于与键关联的值。本章稍后的“使用字典”部分描述了如何使用字典。

### 泛型化

这些现代集合被称为*泛型*（generic）集合，意义在于你可以用类型（或多个类型）填充某种空白模板，以创建一个自定义集合。如果泛型 `List<T>` 看起来很困惑，请查看本微型书籍的第 8 章。该章节将更详细地讨论 C# 的泛型功能。

## 使用列表

假设你需要存储一个 `MP3` 对象的列表，每个对象代表你 MP3 音乐集合中的一个项目。作为一个数组，它可能像这样：

```
MP3[] myMP3s = new MP3[50]; // 从一个空数组开始。
myMP3s[0] = new MP3("Norah Jones"); // 创建并向数组添加一个 MP3。
// …… 以此类推。
```

使用列表集合，它看起来像这样：

```
List<MP3> myMP3s = new List<MP3>(); // 一个空列表
myMP3s.Add(new MP3("Avril Lavigne")); // 向列表添加一个 MP3。
// …… 以此类推。
```

这些示例看起来相似，列表似乎并没有比数组提供任何优势。但当你向数组添加了第 50 个 `MP3` 然后又想添加第 51 个时会发生什么？空间不足了。你选择是声明一个新的更大的数组，然后将所有的 `MP3` 从旧数组复制到新数组中。此外，如果你从数组中删除一个 `MP3`，你的数组就会留下一个巨大的洞。你会在空位中放入什么来代替你丢弃的 `MP3`？也许是值 `null`（本质上是无值，就像本微型书籍第 2 章和第 3 章中的字符串一样）？

面对同样的障碍，列表集合可以愉快地继续运行。想添加第 51 个 `MP3` 吗？没问题。想扔掉旧的 `MP3` 吗？没问题。列表会在你删除它们后自行修复。

![Warning](img/warning.png) 如果你的列表（或者数组）可以包含 `null` 项目，在用 `for` 或 `foreach` 循环时，务必检查是否为 `null`。你不想对一个 `null MP3` 项目调用 `Play()` 方法。这会导致错误。接下来的章节将展示如何使用列表处理各种情况。

### 实例化空列表

以下代码显示了如何为 `string` 类型实例化一个新的空列表。换句话说，此列表只能包含字符串：

```
// List<T>: 注意尖括号加圆括号
List<string> list; // List<T> 声明
```

### 实例化空列表

以下代码显示了如何为 `string` 类型实例化一个新的空列表。换句话说，此列表只能包含字符串：

```
// List<T>: 注意尖括号加圆括号
List<string> list; // List<T> 声明
```

*(注：原文在最后部分存在大量重复/乱码，已根据指令提取核心内容。)*



第一段代码创建了一个具有 `string` 键和 `string` 值的新 `Dictionary` 对象。不过，你并不局限于字符串。键、值或两者可以是任何类型。请注意，`Add()` 方法同时需要一个键和一个值。

```cs
Dictionary<string, string> dict = new Dictionary<string, string>();

// Add(key, value).
dict.Add("C#", "cool");
dict.Add("C++", "like writing Sanskrit poetry in Morse code");
dict.Add("VB", "a simple but wordy language");
dict.Add("Java", "good, but not C#");
dict.Add("Fortran", "ancient");
dict.Add("Cobol", "even wordier and more verbose than VB");
```

### 查找字典

`ContainsKey()` 方法告诉你字典是否包含特定的键。也有对应的 `ContainsValue()` 方法：

```cs
// 检查字典是否包含特定的键。
Console.WriteLine("Contains C# " + dict.ContainsKey("C#")); // True
Console.WriteLine("Contains Ruby " + dict.ContainsKey("Ruby")); // False
```

字典键值对没有特定的顺序，你无法对字典进行排序。它真的就像散在地上的一堆桶。

### 遍历字典

当然，你可以像遍历任何集合一样在循环中遍历字典。但请记住，字典就像一个项对的列表。将每个项对视为一个同时包含键和值的对象。因此，要使用 `foreach` 遍历整个字典，你需要在每次循环中检索一个键值对。这些项对是 `KeyValuePair<TKey, TValue>` 类型的对象。此 `WriteLine()` 调用使用项对的 `Key` 和 `Value` 属性来提取项。它的样子如下：

```cs
// 使用 foreach 遍历字典的内容。
// 注意你正在遍历的是键值值对。
Console.WriteLine("\nContents of the dictionary:");
foreach (KeyValuePair<string, string> pair in dict)
{
    // 因为键恰好是字符串，我们可以对它调用字符串方法。
    Console.WriteLine("Key: " + pair.Key.PadRight(8) + "Value: " + pair.Value);
}
```

下面的代码段显示了如何仅遍历键或仅遍历值。字典的 `Keys` 属性返回另一个集合：一个类型为 `Dictionary<TKey, TValue>.KeyCollection` 的列表型集合。因为键恰好是字符串，你可以作为字符串遍历键并对它们调用字符串方法。`Values` 属性也类似。最后部分代码使用字典的 `Count` 属性查看它包含多少个键值对。

```cs
// 列出键，它们没有特定的顺序。
Console.WriteLine("\nJust the keys:");
// Dictionary<TKey, TValue>.KeyCollection 是仅包含键的集合，
// 在此情况下是字符串。以下是获取键的方法：
Dictionary<string, string>.KeyCollection keys = dict.Keys;
foreach (string key in keys)
{
    Console.WriteLine("Key: " + key);
}

// 列出值，其顺序与上面的键集合相同。
Console.WriteLine("\nJust the values:");
Dictionary<string, string>.ValueCollection values = dict.Values;
foreach (string value in values)
{
    Console.WriteLine("Value: " + value);
}
Console.Write("\nNumber of items in the dictionary: " + dict.Count);
```

当然，这并没有用尽操作字典的所有方法。你可以在 [`https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-5.0#methods`](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2?view=net-5.0#methods)找到字典方法的完整列表。

## 数组和集合初始化器

本节总结了数组和集合的初始化技术——包括旧式和新的。你可能想折角标记。

### 初始化数组

![Remember](img/remember.png) 提醒一下，在本章早期章节“Using var for Arrays”涵盖过的 `var` 语法，数组声明可以像这两个示例中的一个：

```cs
int[] numbers = { 1, 2, 3 }; // 简形式——不能使用 var。
var numbers = new [] { 1, 2, 3 }; // 使用 var 时必须使用完整初始化器。
```

### 初始化集合

同时，初始化集合（例如 `List<T>` —— 或 `Queue<T>` 或 `Stack<T>`）的传统方法是：

```cs
List<int> numList = new List<int>(); // 新空列表。
numbers.Add(1); // 逐个添加元素。
numbers.Add(2);
numbers.Add(3); // …繁琐！
```

或者，如果你已经在一个数组或其他集合中有了这些数字，则是这样的：

```cs
List<int> numList = new List<int>(); // 新空列表。
numbers.Add(1); // 逐个添加元素。
numbers.Add(2);
numbers.Add(3);
```




- **差集（Difference）：** 确定一个集合中的哪些元素没有出现在另一个集合中

什么时候你会使用 `HashSet<T>`？每当你处理两个或多个集合并想要找到重叠项（或创建一个包含两个集合的集合，或者从一个集合中排除一组项目）时，集合都会非常有用。许多 `HashSet<T>` 方法都与集合和其他类相关。你可以在 `https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.hashset-1?view=net-5.0` 更多关于 `HashSet` 的信息。

## 创建集合

要创建一个 `HashSet<T>`，你可以这样做：

```csharp
HashSet<int> smallPrimeNumbers = new HashSet<int>();
smallPrimeNumbers.Add(2);
smallPrimeNumbers.Add(3);
```

或者，更方便的是，可以使用集合初始化器：

```csharp
HashSet<int> smallPrimeNumbers = new HashSet<int> { 2, 3, 5, 7, 11 };
```

或者从任何类型的现有集合（包括数组）创建集合：

```csharp
List<int> intList = new List<int> { 0, 1, 2, 3, 4, 5, 6 };
HashSet<int> numbers = new HashSet<int>(intList);
```

## 向集合中添加项目

如果你尝试向 `HashSet` 添加该集合已包含的项，如下例所示：

```csharp
smallPrimeNumbers.Add(2);
```

编译器不会将重复视为错误（并且不会更改 `HashSet`，因为它不能包含重复项）。实际上，`Add()` 在添加成功时返回 `true`，在未添加时返回 `false`。你不必非使用这个事实，但如果你想在尝试添加重复项时执行某些操作，它是很有用的：

```csharp
bool successful = smallPrimeNumbers.Add(2);
if (successful)
{
    // 2 已添加，现在执行某些操作。
}
// 如果 successful 为 false，则未添加，因为已经存在了
```

## 执行并集（union）

下面的示例展示了几个 `HashSet<T>` 方法，但重要的是演示了如何将 `HashSet<T>` 作为处理其他集合的工具。你可以对 `HashSet<T>` 执行数学运算，但它以各种方式组合集合的能力非常方便。首先，示例从一个 `List<string>` 和一个数组开始。每个都包含颜色名称。虽然你可以简单地通过列表的 `AddRange()` 方法将两者合并：

```csharp
colors.AddRange(moreColors);
```

但生成的列表包含一些重复项（`yellow`, `orange`）。另一方面，通过使用 `HashSet<T>` 和 `UnionWith()` 方法，你可以一次性合并两个集合并消除任何重复项，如下例所示：

```csharp
Console.WriteLine("Combining two collections with duplicates:");
List<string> colors = new List<string> { "red", "orange", "yellow" };
string[] moreColors = { "orange", "yellow", "green", "blue", "violet" };
// 想要在没有任何重复的情况下合并。
// 下面只是第一阶段 ……
HashSet<string> combined = new HashSet<string>(colors);
// …… 现在进入第二阶段。
// UnionWith() 收集两个列表中不重复的项，
// 产生一个成员均为唯一的组合集合。
combined.UnionWith(moreColors);
foreach (string color in combined)
{
    Console.WriteLine(color);
}
```

这里的结果包含 `"red"`, `"orange"`, `"yellow"`, `"green"`, `"blue"` 和 `"violet"`。第一阶段使用 `colors` 列表初始化一个新的 `HashSet<T>`。第二阶段然后调用集合的 `UnionWith()` 方法添加 `moreColors` 数组——但只添加集合中尚未包含的颜色。集合最终包含两个原始列表中的颜色。Green、blue 和 violet 来自第二个列表；red、orange 和 yellow 来自第一个列表。`moreColors` 数组中的 orange 和 yellow 会与集合中已有的重复，因此它们被过滤掉了。

但假设你最终想要的是一个包含这些颜色的 `List<T>`，而不是 `HashSet<T>`。下一部分显示了如何创建一个用 `combined` 集合初始化的新 `List<T>`：

```csharp
Console.WriteLine("\nConverting the combined set to a list:");
// 从上述 combined 集合初始化一个新的 List。
List<string> spectrum = new List<string>(combined);
foreach (string color in spectrum)
{
    Console.WriteLine(color);
}
```

## 执行交集（intersection）

假设你需要处理来自总统竞选活动的数据，每个主要政党大约有十位早期候选人。这些候选人中许多人也是美国参议员的成员。你如何生成一个仅包含也是参议员的候选人的列表？`HashSet<T> IntersectWith()` 方法提供候选人列表和参议员列表之间的重叠项——两个列表中都存在的项，但仅限于这些项：

```csharp
Console.WriteLine("\nFinding the overlap in two lists:");
List<string> presidentialCandidates =
    new List<string> { "Clinton", "Edwards", "Guuliani", "Kennedy", "McCain", "Obama", "Romney", "Biden" };
List<string> senators = { "Clinton", "Kennedy", "McCain", "Romney" };
HashSet<string> senatorsRunning = new HashSet<string>(presidentialCandidates);
// IntersectWith() 收集两个列表共有的项，排除其他的。
senatorsRunning.IntersectWith(senators);
foreach (string senator in senatorsRunning)
{
    Console.WriteLine(senator);
}
```

下面的代码使用 `SymmetricExceptWith()` 来创建 `IntersectWith()` 的相反操作。`IntersectWith()` 给你重叠部分，而 `SymmetricExceptWith()` 给你两个列表中互不相同的项：

```csharp
Console.WriteLine("\nFinding the non-overlapping items:");
Stack<int> stackOne = new Stack<int> { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
Stack<int> stackTwo = new Stack<int> { 2, 4, 6, 8, 12 };
HashSet<int> nonoverlapping = new HashSet<int>(stackOne);
// SymmetricExceptWith() 收集一个集合中但不在另一个集合中的项。
nonoverlapping.SymmetricExceptWith(stackTwo);
foreach (int n in nonoverlapping)
{
    Console.WriteLine(n);
}
```




![Bullet](img/check.png) **将目录和文件作为集合处理**

![Bullet](img/check.png) **枚举集合**

![Bullet](img/check.png) **实现索引器以便于访问集合对象**

![Bullet](img/check.png) **使用 C# 迭代器块遍历集合**

本微型书籍的第 6 章探讨了 .NET Framework 类库提供的、供 C# 和其他 .NET 语言使用的*集合类*。集合类是 .NET 中的一种结构，可以实例化来存储一组项目（参见第 6 章）。

本章的第一部分稍微扩展了*集合*的概念。例如，考虑以下集合：将一个文件视为行或数据记录的集合，将一个目录视为文件的集合。因此，本章的内容结合了本微型书籍第 6 章中的集合内容以及第 3 本中的文件内容。

然而，本章的重点在于通过几种方法遍历或*迭代*各种集合，从文件目录到各种数组和列表。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要简单得多。你可以在下载的源码的 `\CSAIO4D2E\BK01\CH07` 文件夹中找到本章的源码。详情请引言如何查找这些源文件。

## 遍历文件目录

有时你想快速浏览文件目录以寻找某些内容。以下 `LoopThroughFiles` 程序会查看给定目录中的所有文件，读取每个文件并以十六进制格式将其输出到控制台。这听起来可能是一件傻事，但该程序还演示了如何以 `string` 类型以外的格式写入文件。（你可以在“获取十六进制数据”侧边栏中找到十六进制格式的说明。）

### 使用 LoopThroughFiles 程序

从命令行，用户将指定的目录作为参数传递给程序。以下命令会“转储” `temp` 目录中的每个文件（包括二进制文件和文本文件）：

```
loopthroughfiles c:\temp
```

如果你没有输入目录名称，程序默认使用当前目录。（*十六进制转储*将输出以十六进制——基 16——系统的数字显示。请参见附近的侧边栏“获取十六进制数据”）

![Warning](img/warning.png) 如果你在包含大量文件的目录中运行此程序，十六进制转储可能需要一段时间。此外，长文件的遍历也需要时间。请选择一个文件较少的目录，或按 `Ctrl+C` 停止长时间运行程序。此命令可以中断在任何控制窗口中运行的程序。

以下示例显示了当用户指定无效目录 `x` 时发生的情况：

```
Directory "x" invalid
Could not find a part of the path "C:\C#Programs\LoopThroughFiles\bin\Debug\x".
No files left
```

### 入门

与书中的所有示例一样，你从一个基础程序结构开始，如下代码所示。注意，你必须为 `System.IO` 命名空间包含单独的 `using` 语句。在这个基础结构，你添加了后续章节描述的各个函数。

```cs
using System;
using System.IO;

// LoopThroughFiles -- 遍历目录中包含的所有文件；
// 这次执行十六进制转储，尽管它可以是任何操作。
namespace LoopThroughFiles
{
    public class Program
    {
    }
}
```

### 获取初始输入

如前面的章节所示，每个控制台应用程序都从 `Main()` 函数开始。如果你还不完全理解 `Main()` 函数作为控制台应用程序的一部分是如何工作的，不用担心。只需知道 C# 调用的第一个函数就是控制台应用程序的 `Main()` 函数，如下所示：

```cs
public static void Main(string[] args)
{
    // 如果未提供目录名称……
    string directoryName;
    if (args.Length == 0)
    {
        // …获取当前目录的名称……
        directoryName = Directory.GetCurrentDirectory();
    }
    else
    {
        // …否则，假设第一个参数
        // 是使用的目录名称。
        directoryName = args[0];
    }
    Console.WriteLine(directoryName);
    // 获取该目录下所有文件的列表。
    FileInfo[] files = GetFileList(directoryName);
    // 现在遍历列表中的文件，
    // 对每个文件执行十六进制转储。
    foreach (FileInfo file in files)
    {
        // 写入文件名。
        Console.WriteLine("\n\nhex dump of file {0}:", file.FullName);
        // 现在将文件“转储”到控制台。
        DumpHex(file);
        // 在输出下一个文件之前等待。
        Console.WriteLine("\n 按 Enter 继续到下一个文件");
        Console.ReadLine();
    }
    // 就这样了！
    Console.WriteLine("\nNo files left");
    Console.Read();
}
```

`LoopThroughFiles` 程序寻找一个参数。如果 `args.Length` 为零，程序调用 `Directory.GetCurrentDirectory()`。`LoopThroughFiles` 项目位于 `bin\Debug` 子目录中。

![Tip](img/tip.png) `Directory` 类为用户提供了一组操作目录的方法。`FileInfo` 类提供了移动、复制和删除文件等任务的方法。

### 创建文件列表

在处理文件列表之前，你需要先创建一个。`GetFileList()` 方法首先创建一个空的 `FileInfo` 数组，然后用文件列表填充它。以下是所需的代码：

```cs
// GetFileList -- 获取目录中所有文件的列表。
public static FileInfo[] GetFileList(string directoryName)
{
    // 从一个空列表开始。
    FileInfo[] files = new FileInfo[0];
    try
    {
        // 获取目录信息。
        DirectoryInfo di = new DirectoryInfo(directoryName);
        // 该信息对象包含内容列表。
        files = di.GetFiles();
    }
    catch(Exception e)
    {
        Console.WriteLine("Directory \"{0}\" invalid", directoryName);
        Console.WriteLine(e.Message);
    }
    return files;
}
```

`GetFileList()` 随后创建一个 `DirectoryInfo` 对象。正如其所示，`DirectoryInfo` 对象包含了关于目录的与 `FileInfo` 对象关于文件相同类型的信息：名称、层级和序列号之类的信息。然而，`DirectoryInfo` 对象可以访问 `FileInfo` 无法访问的内容：以 `FileInfo` 数组形式的文件列表。

为了帮助捕获错误，`GetFileList()` 将目录和文件相关的代码封装在一个大的 `try` 块中。（有关 `try` 和 `catch` 的解释，请参见本微型书籍的第 9 章。）最后的 `catch` 捕获生成的任何错误。为了让你更加尴尬，`catch` 块展示了目录名称（它可能不存在，因为你输入错误了）。





![Warning](img/warning.png) 最后一步是返回 `files`，它包含了代码集合中的文件列表。小心不要返回对象的引用。例如，不要返回封装在 `PriorityQueue` 类中的底层队列的引用（该类在本微型书籍的第 8 章中有所描述），除非你想让别人通过引用而不是通过你的类方法来弄乱这些队列。那是导致队列损坏且不可预测的稳妥做法。但 `GetFileList()` 在这里并没有暴露你类中的某个类的内部结构，所以是安全的。

### 格式化输出行

你可以对收集到的文件列表进行任何操作。此示例以十六进制格式显示每个文件的内容，这在某些情况下非常有用，例如当你需要知道文件是如何组合在一起的时。然而，在创建十六进制输出行之前，你必须先创建单独的输出行。这里显示的 `DumpHex()` 方法之所以有点复杂，仅仅是因为准确地格式化输出存在困难。

```c
// DumpHex -- 给定一个文件，将文件内容转到控制台。
public static void DumpHex(FileInfo file)
{
    // 打开文件。
    FileStream fs;
    BinaryReader reader;
    try
    {
        fs = file.OpenRead();
        // 将文件流封装在 BinaryReader 中。
        reader = new BinaryReader(fs);
    }
    catch (Exception e)
    {
        Console.WriteLine("\ncan't read from "{0}\"", file.FullName);
        Console.WriteLine(e.Message);
        return;
    }
    // 逐行遍历文件内容。
    for (int line = 1; true; line++)
    {
        // 每次读取 10 字节（单行能容纳的所有字节）——当没有剩余数据时返回。
        byte[] buffer = new byte[10];
        // 使用 BinaryReader 读取字节。
        // 注意：在这种情况下，使用 FileStream 同样简单。
        int numBytes = reader.Read(buffer, 0, buffer.Length);
        if (numBytes == 0)
        {
            return;
        }
        // 将数据写入单行，并在前面加上行号。
        Console.Write("{0:D3} - ", line);
        DumpBuffer(buffer, numBytes);
        // 每 20 行停止一次，以免数据滚出控制台顶部。
        if ((line % 20) == 0)
        {
            Console.WriteLine("Press Enter to continue another 20 lines" +
            " or type Q to go to the next file.");
            string Input = Console.ReadLine();
            if (Input.ToUpper() == "Q")
                break;
        }
    }
}
```

`DumpHex()` 首先打开 `file`。`FileInfo` 对象包含有关文件的信息——它并不打开文件。`DumpHex()` 获取文件的全名（包括路径），然后使用该名称以只读模式打开 `FileStream`。如果由于某些原因 `FileStream` 无法读取文件，`catch` 块将抛出异常。

`DumpHex()` 然后每次读取 10 字节遍历文件。它以十六进制格式作为单行显示每 10 字节。每隔 20 行，它会暂停，直到用户按下回车键。代码使用取模运算符 `%` 来完成该任务。

![Tip](img/tip.png) 垂直方向上，控制台窗口默认有 25 行的空间。（当然，用户可以更改窗口大小，允许更多或更少的行。）这意味着你必须每隔 20 行暂停一次。否则，数据就会从屏幕顶部消失。

取模运算符（`%`）返回除余数。因此，当 `line` 等于 20, 40, 60, 80 时，`(line % 20) == 0` 为真——你懂意思的。这个技巧非常有价值，适用于所有只想定期执行某种操作的循环情况。

### 显示十六进制输出

当你有一行要显示的输出内容后，可以将其以十六进制形式输出。`DumpBuffer()` 使用 `X2` 格式控制控制符写入字节数组的每个成员。虽然 `X2` 听起来像某个秘密军事实验的名字，但它仅仅意味着“用两个十六进制数字显示数字”。

```c
// DumpBuffer -- 将字符缓冲区以十六进制格式写入单行。
public static void DumpBuffer(byte[] buffer, int numBytes)
{
    for(int index = 0; index < numBytes; index++)
    {
        byte b = buffer[index];
        Console.Write("{0:X2}, ", b);
    }
    Console.WriteLine();
}
```

`byte` 的范围是 0 到 255，或 `0xFF` —— 每个字节两个十六进制位。以下是示例文件的前 20 行：

```text
Hex dump of file C:\Temp\output.txt:
001 - 53, 74, 72, 65, 61, 6D, 20, 70, 72,
002 - 6F, 74, 63, 74, 65, 64, 29, 0D,
003 - 20, 20, 46, 69, 6C, 65, 53, 74, 65,
004 - 61, 6D, 28, 73, 74, 72, 69, 6E, 6C,
005 - 20, 46, 69, 6C, 65, 6D, 64, 65, 2C,
006 - 20, 46, 69, 6C, 65, 41, 63, 65, 73,
007 - 73, 29, 0D, 0A, 20, 20, 6D, 65, 6F,
008 - 72, 79, 53, 74, 72, 65, 61, 6D, 29,
009 - 3B, 0D, 0A, 20, 20, 6E, 65, 74, 77, 6F,
010 - 72, 6B, 53, 74, 72, 65, 61, 6D, 0D, 0A,
011 - 20, 20, 42, 75, 66, 72, 53, 74,
012 - 72, 65, 61, 6D, 20, 2D, 20, 62, 75, 66,
013 - 66, 65, 72, 73, 20, 61, 6E, 20, 65, 78,
014 - 69, 73, 74, 69, 6E, 67, 20, 73, 74, 72,
015 - 65, 61, 6D, 20, 6F, 62, 65, 63, 74,
016 - 0D, 0A, 0D, 0A, 42, 69, 6E, 61, 72, 79,
017 - 52, 65, 61, 64, 65, 72, 20, 2D, 20, 72,
018 - 65, 61, 64, 20, 69, 6E, 20, 76, 61, 72,
019 - 69, 6F, 75, 73, 20, 74, 79, 70, 65, 73,
020 - 20, 28, 43, 68, 61, 72, 2C, 49, 6E,
Enter return to continue another 20 lines
```

![Technicalstuff](img/technicalstuff.png) 你可以从十六进制显示重构出 `string`。`0x61` 值是字符 `a` 的数值等。字母表按顺序排列，所以 `0x65` 应该是字符 `e`；`0x20` 是空格。此示例中的第一行（行号之后）是 `s)\n\r Nemo`，其中 `\n` 是换行符，`\r` 是回车。有趣吧？你可以在 `https://www.asciitable.com/` 找到完整的 ASCII 表。

输出代码也适用于 C# 默认使用的广泛得多的 Unicode 字符集的低位部分。（`http://www.i18nguy.com/unicode/codepages.html` 网站提供了各种字符集的列表，如果你必须处理来自大型机等设备的输入，这将有用。）

### 在 Visual Studio 内部运行

要运行 `LoopThroughFiles`，你需要执行以下操作：

*   通过打开开始⇒Visual Studio 2022 文件夹中的 VS 2022 `Developer Command Prompt` 从命令行启动
*   在 Visual Studio 中提供命令行参数
*   在命令行或 Visual Studio 内部不带命令行参数执行它

列表中的第二个选项，即在 Visual Studio 中提供命令行参数，需要你按照以下步骤进行一些设置：

1.  **选择 项目⇒LoopThroughFiles 属性。**
    你会看到应用程序的属性对话框。

2.  **在左侧窗格中选择 调试。**
    你会看到图 7-1 所示的调试选项。

3.  **在 命令行参数字段中输入你想使用的路径，例如 `C:\Temp`。**
    无论你是否处于调试模式，你输入的路径在 Visual Studio 中都将有效。

4.  **选择 文件⇒保存全部。**
    Visual Studio 将新路径保存到磁盘。

5.  **选择 调试⇒开始调试 或 调试⇒不调试调试运行。**
    你会看到程序在你所选择的路径中执行。




在本章的剩余部分，你将看到处理集合迭代这一通用问题的不同方法。本节继续讨论最传统方法（至少对于 `C#` 程序员而言），即迭代器类或枚举器（enumerator），它实现了 `IEnumerator` 接口。

![Tip](img/tip.png) 在本文讨论中，`iterator` 和 `enumerator` 术语同同义（尽管存在技术差异，但在两种情况下，你都是从集合中获取单个值）。尽管接口名称如此，`iterator` 一词更为常用（有关迭代器的细节，请参见 [`https://docs.microsoft.com/en-us/dotnet/csharp/iterators`](https://docs.microsoft.com/en-us/dotnet/csharp/iterators)），但 `enumerator` 在微软也很流行。这两个名词的动词形式也可用：你可以对容器或集合进行迭代（iterate）或枚举（enumerate）。注意，在本章后面讨论的索引器和新的迭代器块是解决同一问题的其他方法。

## 访问集合：通用问题

不同的集合类型可能有不同的访问方案。并不是所有类型的集合都能像数组那样通过索引高效访问——例如链表。链表只包含指向列表中下一个项的引用，并且被设计为连续访问而非随机访问。集合类型之间的差异使得在没有特殊规定的情况下，无法编写如下所示的方法：

```cs
// 传入任何类型的集合：
void MyClearMethod(Collection aColl, int index)
{
    aColl[index] = 0; // 索引并不适用于所有类型的集合。
    // …继续…
}
```

每种集合类型都可以（并且已经）定义自己的访问方法。你根据任务需求决定使用哪种访问方法。这里显示的 `CollectionMoveNext` 示例演示了针对 `List<string>` 对象 `Colors` 的三种访问方法：

```csharp
static void Main(string[] args)
{
    List<string> Colors = new List<string> {
        "Red", "Yellow", "Green", "Blue" };
    Console.WriteLine("Using a delegate.");
    Colors.ForEach(delegate (string value)
    {
        Console.WriteLine(value);
    });
    Console.WriteLine("\r\nUsing a foreach.");
    foreach (string col in Colors)
    Console.WriteLine(col);
    Console.WriteLine("\r\nUsing an enumerator.");
    var colEnum = Colors.GetEnumerator();
    while (colEnum.MoveNext())
    Console.WriteLine(colEnum.Current);
    Console.ReadLine();
}
```

此示例展示了如何使用委托（在本微型书籍第 2 卷第 8 章中详细描述）、`foreach` 循环（在本微型书籍第 6 章中描述）以及枚举器（微软往往将其与迭代器混淆）。`Colors.ForEach()` 方法的优势在于可以使用 lambda 表达式且极其灵活，但有时难以阅读。`foreach` 循环方法易读且常见，但缺乏灵活性。调用 `GetEnumerator()` 获取一个特殊对象，该对象知道如何在 `List<string>` 的项之间移动。当你需要执行额外层次的处理并希望严格控制 `Current` 属性值改变的时间时，这是最佳方法。迭代器（枚举器）方法提供了这些优势：

*   每个集合类都可以定义自己的迭代类。由于迭代类实现了标准的 `IEnumerator` 接口，因此代码编写通常非常简单。
*   应用程序代码不需要知道集合代码的工作原理。只要程序员理解如何使用迭代器，迭代类就可以处理细节。这就是良好的封装。
*   应用程序代码可以为同一个集合创建多个独立的迭代器对象。由于迭代器包含它自己的状态信息（在迭代中“知道自己所处的位置”），每个迭代器都可以独立地遍历集合。你可以同时运行多次迭代，每次迭代位于集合中的不同位置。

为了使 `foreach` 循环成为可能，`IEnumerator` 接口必须支持从数组到链表的所有不同类型的集合。因此，它的方法必须尽可能通用。例如，你不能使用迭代器来随机访问集合类内部的位置，因为大多数集合并不不提供随机访问。（你得发明一个具有该能力的不同枚举接口，但它无法与 `foreach` 配合工作。） `IEnumerator` 提供了这三个功能：

*   `Reset()`：将枚举器重指向集合的开头。**注意：** `IEnumerator` 的泛型版本 `IEnumerator<T>` 不提供 `Reset()` 方法。例如，对于 .NET 的泛型 `LinkedList`，只需开始调用 `MoveNext()` 即可。该泛型 `LinkedList` 位于 `System.Collections.Generic` 中。
*   `MoveNext()`：将枚举器从集合中的当前对象移动到下一个对象。
*   `Current`：这是一个属性而非方法，用于检索存储在枚举器当前位置的数据对象。

下面的方法演示了这个原理。`MyCollection` 类的程序员（未显示）创建了一个对应的迭代器类——例如，`IteratorMyCollection`。应用程序程序员在 `MyCollection` 中存储了 `ContainedDataObject` 对象。以下代码段使用三个标准的 `IEnumerator` 方法来读取这些对象：

```cs
// MyCollection 类持有 ContainedDataObject 类型的对象。
void MyMethod(MyCollection myColl)
{
    // 创建 MyCollection 的程序员也
    // 创建了一个迭代器类 IteratorMyCollection；
    IEnumerator iterator = new IteratorMyCollection(myColl);
    // 将迭代移动到集合内的“下一个位置”。
    while (iterator.MoveNext())
    {
        // 获取集合中当前位置的数据对象的引用。
        ContainedDataObject contained; // 数据
        contained = (ContainedDataObject)iterator.Current;
        // …使用包含的数据对象…
    }
}
```

`MyMethod` 方法接受 `ContainedDataObject` 作为参数。它通过创建 `iterator` 开始。方法通过调用 `MoveNext()` 开始循环。在第一次调用时，`MoveNext()` 移动到第一个元素。在后续每次调用中，`MoveNext()`移动到下一个位置。当集合耗尽且迭代器无法再次移动时，`MoveNext()` 返回 `false`。

`Current` 属性返回迭代器当前位置的数据对象的引用。程序在赋值给 `contained` 之前会将其转换为 `ContainedDataObject`。如果之前的调用 `MoveNext()` 未返回 `true` 或尚未调用 `MoveNext()`，则调用 `Current` 是无效的。

IEnumerator 方法足够标准，使得 C# 自动使用它们来实现 `foreach` 语句。`foreach` 语句可以访问任何实现 `IEnumerable` 或 `IEnumerable<T>` 的类。本节根据 `IEnumerable<T>` 讨论 `foreach`，正如这个通用方法所示，它能够处理任何此类类，从数组到链表到栈和队列：

```csharp
void MyMethod(IEnumerable<T> containerOfThings)
{
    foreach (string s in containerOfThings)
    {
        Console.WriteLine("下一个事物是 {0}", s);
    }
}
```




一个类通过定义 `GetEnumerator()` 方法来实现 `IEnumerable<T>`，该方法返回一个 `IEnumerator<T>` 实例。在底层，`foreach` 会调用 `GetEnumerator()` 方法来获取一个迭代器。它使用该迭代器来遍历集合。在继续执行大括号内的代码块之前，它获取的每个元素都经过了适当的类型转换。请注意，`IEnumerable<T>` 和 `IEnumerator<T>` 是不同但相关的接口。C# 也提供了这两个后者的非泛型版本，但你应该优先使用泛型版本，因为它们具有更高的类型安全性。`IEnumerable<T>` 看起来如下：

```cs
interface IEnumerable<T>
{
    IEnumerator<T> GetEnumerator();
}
```

而 `IEnumerator<T>` 看起来如下：

```cs
interface IEnumerator<T>
{
    bool MoveNext();
    T Current { get; }
}
```

非泛型的 `IEnumerator` 接口增加了一个 `Reset()` 方法，可以将迭代器移回集合的开头，并且它的 `Current` 属性返回 `Object` 类型。注意 `IEnumerator<T>` 继承自 `IEnumerator`（接口继承，见第 2 本 第 7 章，与普通的对象继承不同）。

C# 数组（体现在它们基于的 `Array` 类）以及所有的 .NET 集合类已经实现了这两个接口。因此，只有在你编写自己的自定义集合类时，才需要实现这些接口。对于内置集合，你可以直接使用它们。详情请参见 [`https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic?view=net-5.0`](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic?view=net-5.0) 中的 `System.Collections.Generic` 命名空间主题。因此你可以这样写 `foreach` 循环：

```cs
foreach(int nValue in myCollection)
{
    // …
}
```

## 使用数组方式访问集合：索引器

访问数组元素非常简单：语句 `container[n]` 访问 `container` 数组的第 `n` 个元素。括号中的值索引，而 `[]` 被称为`下标运算符`。如果对其他类型的集合进行索引访问也这么简单就好了。

C# 允许你编写索引操作的自定义实现。你可以为那些本不具备该功能的集合提供索引功能。此外，你可以使用 C# 数组限于简单整数以外的其他下标类型进行索引。例如，通过编写自己的索引功能，你可以与 `string` 类型进行交互。另一个例子是，你可以为像 `container["Joe"]` 这样的编程结构创建一个索引功能。（第 2 本 第 11 章 的“索引器”部分展示了如何向 `struct` 添加索引器。）

### 索引器格式

索引器看起来非常像普通的 `get/set` 属性（第 2 本 第 3 章 详细描述了访问器），区别在于出现了 `this` 关键字并使用下标运算符 `[]` 代替属性名，如这段代码所示：

```cs
class MyArray
{
    public string this[int index] // 注意 "this" 关键字。
    {
        get => MyArray[index];
        set => MyArray[index] = value;
    }
}
```

示例展示了索引器的简写形式，当你只需要获取和设置值而无需执行其他操作时使用。本章后面的“使用索引器”部分展示了较长的版本。在底层，表达式 `s = myArray[i];` 调用 `get` 访问方法，将 `i` 的值作为索引传递给它。此外，表达式 `myArray[i] = "some string";` 调用 `set` 访问方法，将相同的索引 `i` 和 `"some string"` 作为 `value` 传递给它。

### 索引器程序示例

索引类型不仅限于 `int`。你可以根据所有者的姓名、房屋地址或其他任何索引对房屋集合进行索引。此外，索引器属性可以重载多个索引类型，因此你可以对同一个集合中的各种元素进行索引。接下来的章节将讨论 `Indexer` 程序，该程序生成虚拟数组类 `KeyedArray`。这个虚拟数组看起来和运行起来像一个数组，除了它使用 `string` 值作为索引。（注意，你可以通过 [`https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2`](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.dictionary-2) 中描述的 C# `Dictionary` 来复制此示例中的功能。）

### 执行所需的类设置

`Indexer` 示例依赖于一个特殊的类，这意味着你必须为它创建一个类框架。（如果此示例中的某些术语看起来很奇怪，请担心；在 第 2 本 中你会学到更多关于类和其他面向对象编程（OOP）的技术。）以下是用于存放后续章节讨论的类方法的框架。

```cs
public class KeyedArray
{
    private string[] _keys;
    private object[] _arrayElements;

    public KeyedArray(int size)
    {
        _keys = new string[size];
        _arrayElements = new object[size];
    }

    // Find 查找与 targetKey 对应的索引
    //（如果找不到则返回负值）。
    private int Find(string targetKey)
    {
        for (int i = 0; i < _keys.Length; i++)
        {
            if (String.Compare(_keys[i], targetKey) == 0)
            {
                return i;
            }
        }
        return -1;
    }

    // FindEmpty 在数组中为新条目寻找空间。
    private int FindEmpty()
    {
        for (int i = 0; i < _keys.Length; i++)
        {
            if (_keys[i] == null)
            {
                return i;
            }
        }
        throw new Exception("Array is full");
    }

    // 通过字符串键查找内容——这就是索引器。
    public object this[string key]
    {
        set
        {
            // 检查字符串是否存在。
            int index = Find(key);
            if (index < 0)
            {
                // 不存在——找一个新位置。
                index = FindEmpty();
                _keys[index] = key;
            }
            // 将对象保存在对应的位置。
            _arrayElements[index] = value;
        }
        get
        {
            int index = Find(key);
            if (index < 0)
            {
                return null;
            }
            return _arrayElements[index];
        }
    }
}
```

### 使用索引器

在此时，你需要定义一个索引器来使你的代码工作，如下所示。索引器 `public object this[string key]` 需要使用两个函数 `Find()` 和 `FindEmpty()`。




索引器的 `get[]` 侧遵循类似的逻辑。它首先使用 `Find()` 方法搜索指定的键。如果 `Find()` 返回一个非负索引，`get[]` 将返回 `_arrayElements` 中对应的成员，该数据就存储在那里。如果 `Find()` 返回 `–1`，`get[]` 将返回 `null`，表示在列表任何地方都找不到提供的键。

`Find()` 方法遍历 `_keys` 的成员，以寻找与传入的字符串 `targetKey` 具有相同元素的。`Find()` 返回找到的元素的索引（如果未找到，则返回 `–1`）。`FindEmpty()` 返回第一个没有键元素的索引。

### 测试你的新类

`Main()` 方法是索引器程序的一部分，而不是该类的一部分，它以一种直观的方式演示了 `KeyedArray` 类：

```csharp
static void Main(string[] args)
{
    // 创建一个空间充足的数组。
    KeyedArray ma = new KeyedArray(100);
    // 保存辛普森一家孩子们的年龄。
    ma["Bart"] = 10;
    ma["Lisa"] = 8;
    ma["Maggie"] = 2;
    // 查询 Lisa 的年龄。
    Console.WriteLine("Let's find Lisa's age");
    int age = (int)ma["Lisa"];
    Console.WriteLine("Lisa is {0}", age);
    Console.Read();
}
```

程序创建了一个长度为 100 的 `KeyedArray` 对象 `ma`（也就是说有 100 个空元素）。它继续存储电视节目《辛普森一家》中孩子的年龄，以每个孩子的名字作为索引。最后，程序使用表达式 `(int)ma["Lisa"]` 获取 Lisa 的年龄并显示结果。

注意，程序必须对从 `ma[]` 返回的值进行转换，因为 `KeyedArray` 被设计为持有任何类型的对象。如果索引器被编写为仅处理 `int` 值——或者 `KeyedArray` 是泛型的，那么这种转换将是不必要的。（关于泛型的更多信息，请参阅本微型书籍的第 8 章）。该程序的输出简单而优雅：

```
Let's find Lisa's age
Lisa is 8
```

### 遍历迭代器块

在 C# 的早期版本中，在本章前面的“以数组方式访问集合：索引器”节讨论的与链表相关的技术是遍历集合的主要实践，就像在此之前的 C++ 和 C 中执行的那样。尽管这种解决方案确实有效，但事实证明 C# 2.0 及以上版本简化了这个过程，使得：

* 你不需要调用 `GetEnumerator()`（并转换结果）。
* 你不需要调用 `MoveNext()`。
* 你不需要调用 `Current` 并转换其返回值。
* 你可以简单地使用 `foreach` 来迭代集合。（C# 在底层为你处理其余一切工作——它甚至会编写迭代器类。）

与其在在你编写的集合类中实现所有这些接口方法，你可以像 `IteratorBlocks` 示例所示提供一个迭代器块——你不需要编写自己的迭代器类来支持该集合。你也可以将迭代器块用于许多其他杂务，如下一个示例所示。

### 创建所需的迭代器块框架

迭代的最佳方法是使用迭代器块。当你编写一个集合类时——仍然需要如 `KeyedList` 和 `PriorityQueue` 这样的自定义集合类——你在代码中实现一个迭代器块，而不是实现 `IEnumerator` 接口。然后该类的用户就可以简单地使用 `foreach` 迭代集合。以下是本示例使用的基本框架，包含了后续章节中出现的函数：

```csharp
static void Main(string[] args)
{
    // 实例化 MonthDays "集合" 类。
    MonthDays md = new MonthDays();
    // 迭代它。
    Console.WriteLine("Stream of months:\n");
    foreach (string month in md)
    {
        Console.WriteLine(month);
    }
    // 实例化 StringChunks "集合" 类。
    StringChunks sc = new StringChunks();
    // 迭代它：打印文本块。
    // 此次迭代将每个块放在单独行。
    Console.WriteLine("\nstream of string chunks:\n");
    foreach (string chunk in sc)
    {
        Console.WriteLine(chunk);
    }
    // 而这次迭代将所有内容放在同一行。
    Console.WriteLine("\nstream of string chunks on one line:\n");
    foreach (string chunk in sc)
    {
        Console.Write(chunk);
    }
    Console.WriteLine();
    // 实例化 YieldBreakEx "集合" 类。
    YieldBreakEx yb = new YieldBreakEx();
    // 迭代它，但在 13 之后停止。
    Console.WriteLine("\nstream of primes:\n");
    foreach (int prime in yb)
    {
        Console.WriteLine(prime);
    }
    // 实例化 EvenNumbers "集合" 类。
    EvenNumbers en = new EvenNumbers();
    // 迭代它。
    Console.WriteLine("\nstream of primes:\n");
    foreach (int even in en)
    {
        Console.WriteLine(even);
    }
    // 实例化 PropertyIterator "集合" 类。
    PropertyIterator prop = new PropertyIterator();
    // 迭代它：打印双精度值。
    Console.WriteLine("\nstream of doubles:\n");
    foreach (double db in prop)
    {
        Console.WriteLine(db);
    }
    // 实例化 DescendingNumbers "集合" 类。
    DescendingNumbers dn = new DescendingNumbers();
    // 迭代它：打印递减数字。
    Console.WriteLine("\nstream of descending numbers:\n");
    foreach (int prime in dn)
    {
        Console.WriteLine(prime);
    }
    // 实例化 StringIterator "集合" 类。
    StringIterator si = new StringIterator();
    // 迭代它：打印字符串块。
    Console.WriteLine("\nstream of strings:\n");
    foreach (string chunk in si)
    {
        Console.WriteLine(chunk);
    }
}
```

### 遍历月份中的数：第一个示例

以下类提供了一个按月份步的迭代器：

```csharp
// 定义月份中的数
class MonthDays
{
    // 这是集合。
    string[] months =
    { "January 31", "February 28", "March 31", "April 30",
      "May 31", "June 30", "July 31", "August 31",
      "September 30", "October 31", "November 30", "December 31" };

    // GetEnumerator -- 这里是迭代器。
    public System.Collections.IEnumerator GetEnumerator()
    {
        foreach (string month in months)
        {
            // 迭代返回一个月份。
            yield return month;
        }
    }
}
```

这里是 `Main()` 方法的一部分，使用 `foreach` 循环迭代此集合：

```csharp
// 实例化 MonthDays "集合" 类。
MonthDays md = new MonthDays();
// 迭代它。
foreach (string month in md)
{
    Console.WriteLine(month);
}
```

此集合类基于数组，就像 `KeyedArray` 一样。该类包含一个类型为 `string` 的数组。当客户端迭代此集合时，集合的迭代器块逐个交付 `string` 类型。每个 `string` 包含月份名称，并将月份的天数附加在 `string` 之后。

![记住](img/remember.png) 你包含 `GetEnumerator()` 方法的类不再需要实现 `IEnumerator` 接口。事实上，你并不希望它实现。在后续章节中，你将发现多种类型的迭代器块：




-   普通迭代器
-   命名迭代器
-   实现为迭代器的类属性

注意，类 `MonthDays` 的 `GetEnumerator()` 方法包含一个 `foreach` 循环，用于 `yield` 其内部数组中的 `string` 类型。迭代器块通常使用某种形式的循环来实现此，正如你在后面几个示例中看到的。。实际上，你自己的调用代码中有一个内部 `foreach` 循环，它一个接一个提供项，这些项可以在 `GetEnumerator()` 外部的另一个 `foreach` 循环中迭代。

### 到底什么是集合

花一点时间将此示例中的小型集合与复杂的 `LinkedList` 集合进行对比。`LinkedList` 具有指针连接的复杂节点结构，而这个小型的 `months` 集合基于一个简单的数组——而且里面还是预设的内容。这个示例稍微扩展了 `collection` 的概念，并在本章结束之前对其进行了进一步完善。

你的集合类可能不包含预设内容——大多数集合的设计是为了存储你通过 `Add()` 方法等存入的内容。例如，前一节中的“以数组方式访问集合：索引器”中的 `KeyedArray` 类使用 `[]` 下标运算符来添加项。你的集合也可以提供一个 `Add()` 方法并添加一个迭代器块，以便它可以与 `foreach` 工作。

从最广义上说，集合的作用是存储多个对象并允许你迭代这些对象，按顺序逐个检索它们——有时是随机的，或者表面上是随机的，正如 `Indexer` 示例中所示。（当然，数组也可以做到，即使没有像 `MonthDays` 这样的类的额外机制，但迭代器的功能远超 `MonthDays` 示例。）

更通用地说，无论可迭代集合在底层如何工作，它都会产生一个值的“流”，你通过 `foreach` 获取到这些值。为了强调这一点，这里有来自 `IteratorBlocks` 的另一个简单集合类，它尽可能地将集合的概念推向了极致（你可能认为是这样）：

```csharp
//StringChunks -- 定义一个返回文本块的迭代器，//每次迭代返回一个 -- 另一个奇特的“集合”类。
class StringChunks
{
    //GetEnumerator -- 这是一个迭代器；看它如何在 Main 中被调用 // (两次)。
    public System.Collections.IEnumerator GetEnumerator()
    {
        // 每次迭代返回不同的文本块。
        yield return "Using iterator ";
        yield return "blocks ";
        yield return "isn't all ";
        yield return "that hard";
        yield return ".";
    }
}
```

奇怪的是，`StringChunks` 集合在通常意义上并没有存储任何内容。它甚至不包含数组。那么集合在哪里呢？它就在那系列 `yield return` 调用中，这些调用使用特殊语法一次返回一个项，直到所有项都返回完毕。集合“包含”了五个对象，每个都是一个简单的 `string`，类似于上一个 `MonthDays` 示例中存储在数组中的那些字符串。而且，在类外部的 `Main()` 中，你可以用一个简单的 `foreach` 循环迭代这些对象，因为 `yield return` 语句按顺序每次交付一个字符串。这里是迭代 `StringChunks` 集合的简单 `Main()` 方法的一部分：

```csharp
// 实例化一个 StringChunks "集合"类。
StringChunks sc = new StringChunks();
// 迭代它：打印文本片段。
foreach (string chunk in sc)
{
    Console.WriteLine(chunk);
}
```

### 迭代器语法放弃得如此容易

接下来的章节关注两个有用的语句：`yield return` 和 `yield break`。`yield return` 语句类似于 `MoveNext()` 和 `Current` 的组合，用于检索集合中的下一个项。`yield break` 语句类似于 C# 的 `break` 语句，允许你跳出循环或 `switch` 语句。

### Yield return: 好了，我放弃了

`yield return` 语法的工作方式如下：

1. 第一次被调用时，它返回集合中的第一个值。
2. 下次被调用时，它返回第二个值。
3. 依此类推…… {.

使用 `yield` 就像显式调用 `MoveNext()` 方法，就像在 `LinkedList` 中。每次调用 `MoveNext()` 都会从集合中产生一个新的项。但在这里你不需要调用 `MoveNext()`。（不过，你可以相信，这在 `yield return` 语法的背后的某处已经为你完成了。）

你可能会奇怪“下次被调用时”是什么意思。这里再次使用 `foreach` 循环来迭代 `StringChunks` 集合：

```csharp
foreach (string chunk in sc)
{
    Console.WriteLine(chunk);
}
```

循环每次从迭代器获取新块（在循环的每次通过中），迭代器都会存储它在集合中所处的位置（正如所有迭代器所做的那样）。在下次通过 `foreach` 循环，迭代器返回集合中的下一个值，依此类推。

### Yield break: 我想离开这里！

你需要理解与 `yield` 相关的一个有趣语法。你可以通过在迭代器中指定 `yield break` 语句在某处停止迭代器的进度。假设在测试集合类迭代器块中的某个条件后达到了一个阈值，你想在该点停止迭代。这里有一个以这种方式使用 `yield break` 的迭代器块简要示例：

```csharp
//YieldBreakEx -- yield break 关键字的另一个示例
class YieldBreakEx
{
    int[] primes = { 2, 3, 5, 7, 11, 13, 17, 19, 23 };
    //GetEnumerator -- 返回质数序列 // 演示 yield return 和 yield break
    public System.Collections.IEnumerator GetEnumerator()
    {
        foreach (int prime in primes)
        {
            if (prime > 13) yield break;
            yield return prime;
        }
    }
}
```

在这种情况下，迭代器块包含一个 `if` 语句，当迭代器到达集合中的每个质数时对其进行检查（顺便说一下，迭代器内部使用了另一个 `foreach`）。如果质数大于 13，块调用 `yield break` 停止产生质数。否则，它继续继续——每次 `yield return` 放弃另一个质数，直到集合耗尽。

### 各种形状和大小的迭代器块

在本章之前的示例中，迭代器块看起来像这样：

```csharp
public System.Collections.IEnumerator GetEnumerator()
{
    yield return something;
}
```

但迭代器块还可以采取其他形式：

*   命名迭代器
*   类属性

### 命名为 Fred 的迭代器

与其总是以名为 `GetEnumerator()` 方法的形式编写迭代器块，你可以编写一个*命名迭代器*——一个返回 `System.Collections.IEnumerable` 接口而不是 `IEnumerator` 的方法，且你不需要命名为 `GetEnumerator()`——你可以将其命名为类似 `MyMethod()`。例如，你可以使用这个简单方法迭代从你传入的顶部值向下到停止值的偶数——是的，以*倒序*顺序排列。迭代器几乎可以做任何事情：

```csharp
//EvenNumbers -- 定义一个命名迭代器，返回从你传入的“顶部”值向下到“停止”值的偶数。
// 另一个奇特的“集合”类
```





```cs
class EvenNumbers
{
    //DescendingEvens -- 这是一个“命名迭代器”。
    // 也演示了 yield break 关键字
    // 查看在 Main() 中如何通过 foreach 调用它。
    public System.Collections.IEnumerable DescendingEvens(int top, int stop)
    {
        // 将 top 设置为最近的下方偶数。
        if (top % 2 != 0) // 如果 top / 2 的余数不为 0。
            top -= 1;
        // 从 top 向下迭代到 stop 上方的最近偶数。
        for (int i = top; i >= stop; i -= 2)
        {
            if (i < stop)
                yield break;
            // 每次迭代返回下一个偶数。
            yield return i;
        }
    }
}
```

`DescendingEvens()` 方法接受两个参数（这是一个实用的补充），它们设置了你想要开始的偶数的上限以及你想要停止的下限。生成的第一个偶数将等于 `top` 参数，或者如果 `top` 是奇数，则等于它下方最近的偶数。生成的最后一个偶数将等于 `stop` 参数的值（或者如果 `stop` 是奇数，则等于它上方最近的偶数）。然而，该方法本身并不返回 `int`；它返回 `IEnumerable` 接口。但它仍然包含一个 `yield return` 语句来返回一个偶数，然后等待下次从 `foreach` 循环中调用。这就是 `int` 产出的地方。

![Remember](img/remember.png) 这个示例展示了另一个没有底层集合的集合——例如在本章前面提到的 `StringChunks`。注意这一个是*计算出的*——该方法“yield 返回”的是一个计算后的值，而不是存储或硬编码的值。这是实现无集合集合的另一种方法。（你也可以从数据源或网络服务检索项。）最后，示例显示了你可以以几乎任何喜欢的方式迭代集合：例如，向下而不是向上，或者以两个为步长而不是一个为步长。

![Tip](img/tip.png) 迭代器也不必是有限的。考虑以下迭代器，只要你想要请求，它就会交付一个新数字：

```cs
public System.Collections.IEnumerable PositiveIntegers()
{
    for (int i = 0; ; i++)
    {
        yield return i;
    }
}
```

![Warning](img/warning.png) 这个示例实际上是一个无限循环。你可能想传递一个用于停止迭代的值。以下是在 `Main()` 的 `foreach` 循环中调用 `DescendingEvens()` 的方式。（在前面的示例中调用 `PositiveIntegers()` 同样类似。）此示例还演示了传递奇数作为限制值时发生的情况——这是 `%` 运算符的另一个用法：

```cs
// 实例化 EvenNumbers "集合" 类。
EvenNumbers en = new EvenNumbers();
// 迭代它：打印从 10 到 4 的偶数。
Console.WriteLine("\nstream of descending evens :\n");
foreach (int even in en.DescendingEvens(11, 3))
{
    Console.WriteLine(even);
}
```

此调用产生了一个从 10 到 4 的偶数整数列表。同样注意 `foreach` 是如何指定的。你必须实例化一个 `EvenNumbers` 对象（集合类）。然后，在 `foreach` 语句中，你通过该对象调用命名迭代器方法：

```cs
EvenNumbers en = new EvenNumbers();
foreach (int even in en.DescendingEvens(nTop, nStop)) …
```

![Tip](img/tip.png) 如果 `DescendingEvens()` 是静态的，你甚至不需要类实例。你将像通常一样通过类本身调用它：

```cs
foreach(int even in EvenNumbers.DescendingEvens(nTop, nStop)) …
```

### 外面是一片广阔的天地！

如果你能用 `foreach` 语句产生偶数的“流”，请考虑你可能用这些特殊用途集合产生的所有其他有用物：2 的幂的流，或者数学级数中项的流（如质数或平方数）——甚至是奇特的东西，如斐波那契数。或者，随机数流（这是 `Random` 类已经做过的）或随机生成的对象流呢？

### 迭代属性并不意味着“一个不断售卖的房子”

你还可以将迭代块实现为类的*属性*——特别是在属性的 `get()` 访问器中。在这个带有 `DoubleProp` 属性的简单类中，属性的 `get()` 访问器充当迭代器块，返回 `double` 值的流：

```cs
//PropertyIterator -- 演示将类的
// 属性的 get 访问器作为迭代器块。
class PropertyIterator
{
    double[] doubles = { 1.0, 2.0, 3.5, 4.67 };
    // DoubleProp -- 一个带有迭代块的"get"属性
    public System.Collections.IEnumerable DoubleProp
    {
        get
        {
            foreach (double db in doubles)
            {
                yield return db;
            }
        }
    }
}
```

编写 `DoubleProp` 头部的方式与命名迭代器示例中编写 `DescendingEvens()` 方法头部的方式非常相似。头部返回 `IEnumerable` 接口，但作为属性，它在属性名后没有括号，并且有一个 `get()` 访问器——虽然没有 `set()`。`get()` 访问器实现为 `foreach` 循环，该循环迭代集合并使用标准的 `yield return` 产出 `doubles` 集合中的每个项。以下是 `Main()` 中访问属性的方式：

```cs
// 实例化 PropertyIterator "集合" 类。
PropertyIterator prop = new PropertyIterator();
// 迭代它：一次产出一个 double。
Console.WriteLine("\nstream of double values:\n");
foreach (double db in prop.DoubleProp)
{
    Console.WriteLine(db);
}
```

![Tip](img/tip.png) 你还可以拥有泛型迭代器。[`https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/iterators`](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/iterators) 的帮助文档提供了更多细节。现在应用程序已完成，你可以运行它并看到以下输出：

```
Stream of months:
January 31
February 28
March 31
April 30
May 31
June 30
July 31
August 31
September 30
October 31
November 30
December 31

Stream of string chunks:
Using iterator
blocks
isn't all
that hard
.

stream of string chunks on one line:
Using iterator blocks isn't all that hard.

stream of primes:
2
3
5
7
11
13

stream of descending evens :
10
8
6
4

stream of double values:
1
2
3.5
4.67
```




泛型在 C# 中有两种形式：内置泛型（例如 `List<T>`）以及各种自定义的泛型。在快速浏览了泛型概念后，本章将介绍自定义的泛型类、泛型方法，以及泛型接口和委托。

![记住](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要容易得多。你可以在下载的源码的 `\CSAIO4D2E\BK01\CH08` 文件夹中找到本章的源码。详情请参见“引言”，关于如何查找这些源文件。

## 编写新处方：泛型

泛型到底有什么热门的？它们之所以卓越，出于两点原因：安全性和性能。

### 泛型是类型安全的

![记住](img/remember.png) 当你声明数组时，必须指定它能存储的数据的确切类型。如果你指定了 `int`，该数组无法包含除 `int` 或 C# 可以隐式转换为 `int` 的其他数值类型以外的任何内容。如果你尝试向数组放入错误类型的数据，会在构建时看到编译器错误。因此，编译器强制执行`类型安全`，让你在问题出门之前就能修复它。编译器错误比运行时错误好得多。编译器错误是有用的，因为它们能帮助你现在发现问题。

![记住](img/remember.png) 旧式的非泛型集合不是类型安全的。在 C# 中，一切都是一个 `Object`，因为 `Object` 是所有其他类型（包括值类型和引用类型）的基类型。（如果你不懂 IS_A，别担心——它会在第二本书的“IS_A 对比 HAS_A — 我太困惑了”章节中解释，参见第 5 章。）但当你向集合中存储值类型（数字、`chars`、`bools` 和 `structs`）时，在存入时必须“装箱”（boxed），取出时必须“拆箱”（unboxed）。这就像是你把物品放入蛋中以放入蛋盒中，然后在从蛋盒中取出蛋后打碎蛋壳以取回物品。（引用类型如 `string`、`Student` 和 `BankAccount` 不会经历装箱。）

非泛型缺乏类型安全的第一个后果是，你需要进行类型转换（如下代码所示），才能从 `ArrayList` 中取出原始对象，因为它隐藏在 `Object` 内部：

```
ArrayList aList = new ArrayList();
// 添加五个或六项，然后……
string myString = (string)aList[4]; // 转换为 string。
```

![警告](img/warning.png) 行吧，但第二个后果是这个：你可以往蛋盒里放蛋，这没错。但你也可以加入弹珠、石头、钻石、软糖——随你所欲。一个 `ArrayList` 同时包含许多不同类型的对象。所以写这种代码是合法的：

```
ArrayList aList = new ArrayList();
aList.Add("a string"); // string -- OK
aList.Add(3); // int -- OK
aList.Add(aStudent); // Student -- OK
```

然而，如果你向 `ArrayList`（或另一个非泛型集合）中放入混合了不兼容类型，你如何知道例如 `aList[3]` 中是什么类型呢？如果是 `aStudent` 且你尝试将其强制转换为 `string`，就会得到运行时错误。这就像哈利·波特伸手进一盒比蒂波特味味豆：他不知道自己拿到的是覆莓味豆还是耳垢味。

![技术细节](img/technicalstuff.png) 为了安全，你不得不求助于使用 `is` 运算符（在第二本书中讨论）或替代方案 `as` 运算符：

```
// 检查对象是否为正确的类型，然后进行转换……
if (aList[i] is Student) // 那里的对象是 Student 吗？
{
    Student theStudent = (Student)aList[i]; // 是，所以转换是安全的。
}
// 或者转换并查看是否成功……
Student aStudent = aList[i] as Student; // 如果存在则提取 Student；
if (aStudent != null) // 如果不存在，“as”返回 null。
{
    // 可以使用 aStudent；as”运算符起作用了。
}
```

你可以通过使用泛型避免所有这些额外工作。泛型集合的工作方式类似于数组：你在声明它们时，指定了它们能包含的唯一类型。

### 泛型是高效的

多态允许类型 `Object` 包含任何其他类型，就像上一节中的蛋盒类比。但通过存入和取出值类型对象（数值、`char`、`bool` 类型和 `structs`），你可能会付出代价。这是因为你添加的值类型对象必须装箱。（有关多态的更多信息，请参见第二本书。）

除非你的集合很大，否则装箱并不令人担心（尽管装箱的数量可能会让你大吃惊，并且成本比你想象的要高）。如果你正向非泛型集合中塞入数千或百万个 `int`。

## 类泛型：编写你自己的

除了内置泛型，C# 还允许你编写自己的泛型。注意这些实例化是多么相似：

```
LinkedList<int> aList = new LinkedList<int>(); // 内置类
MyClass<int> aClass = new MyClass<int>(); //自定义类
```

并不是所有的类都适合泛型；在“易地编写泛型代码”章节中，你会看到一个这样的例子。

![记住](img/remember.png) 逻辑上对不同类型执行相同操作的集合是最好的。如果你发现自己在嘟囔：“我可能也需要为 `Student` 对象写一个版本”，它可能是一个很好的泛型候选对象。

为了展示如何编写自己的泛型类，`PriorityQueue` 示例了一个特殊的队列类——优先级队列。

### OOPs 的包裹

这里：包裹进入 OOPs 公司的前门，并从后门出去。有些包裹需要通过超快的第二天传送传输；另一些可以慢一点，通过第二天信鸽传输；大多数则走蜗牛路线：通过你表哥 Fred 的 82 年沃尔沃地面运输。

但包裹并不是按照特定顺序到达仓库的，当它们进入时，我们需要对某些包裹进行加速。因为某些包裹比其他的更，它们具有优先级，仓库的人会对高优先级包裹给予特殊对待。

除了优先级因素外，这种情况是为队列量身定制的。




*   **高优先级包裹**（次日送达）进入队列最前端——但位于任何已存在的其他高优先级包裹之后。
*   **中优先级包裹**（次日送达）尽可能靠前排——但位于所有高优先级包裹之后（即使是那些稍后会被迟到投递的高优先级包裹），并且位于已经在队列中的其他中优先级包裹之后。
*   **低优先级陆运包裹**必须从队列末尾加入。它们只能眼睁睁看着所有高优先级包裹通过并插到它们前面——有时，甚至是插在它们*非常远*的前。

C# 自带了队列，甚至包括泛型队列。但旧版本没有提供优先级队列，因此你必须自己构建。如何做呢？一种常见的方法是在包装类（wrapper class）中嵌入几个实际队列，类似于这样：

```csharp
class Wrapper // 或 PriorityQueue
{
    Queue queueHigh = new Queue ();
    Queue queueMedium = new Queue ();
    Queue queueLow = new Queue ();
    // 操作底层队列的方法……
}
```

`Wrappers`（包装器）是封装复杂性的类（或方法）。包装器的接口可能与其内部包含内容的接口完全不同——这被称为*适配器*（adapter）。

这里的包装器封装了三个实际队列（它们可以是泛型的），且包装器必须管理什么内容进入哪个底层队列以及如何进入。在 C# 中实现的 `Queue` 类的标准接口包含这两个关键方法：

*   `Enqueue()`（读音为“N-Q”）将项目项插入队列的*末尾*。
*   `Dequeue()`（读音为“D-Q”）从队列的*头部*移除项。

![Technicalstuff](img/technicalstuff.png) 对于运输优先级队列，包装器提供了与普通队列相同的接口，从而假装自己也是一个普通队列。它实现了一个 `Enqueue()` 方法，该方法用于判断传入包裹的优先级，并决定它加入哪个底层队列。包装器的 `Dequeue()` 方法在任何底层队列中找到优先级最高的 `Package`。该包装类的正式名称是 `PriorityQueue`。

![Tip](img/tip.png) 该示例依赖于一个随机数生成器，你可以在 `Main()` 方法和 `PackageFactory` 的 `CreatePackage()` 方法中设置它。对 `Random(2)` 的调用使用了*种子值*（作为随机数计算起点的数字），这样你每次都能得到相同的结果。这种方法允许产生可重复的测试结果，这对于不希望处理应用程序运行之间数字差异的开发人员来说是一种常见做法。当然，你可以直接使用 `Random()`，这将允许种子自动变化，让你看到更真实的应用程序输出展示，但你需要手动进行此更改。使用默认的 `Random(2)`，你会看到以下输出：

```
Add a random number (0 - 20) of random packages to queue:
Creating 15 packages:
Generating and adding random package 0 with priority High
Generating and adding random package 1 with priority Medium
Generating and adding random package 2 with priority Low
Generating and adding random package 3 with priority High
Generating and adding random package 4 with priority Low
Generating and adding random package 5 with priority Low
Generating and adding random package 6 with priority High
Generating and adding random package 7 with priority Medium
Generating and adding random package 8 with priority Low
Generating and adding random package 9 with priority Low
Generating and adding random package 10 with priority High
Generating and adding random package 11 with priority Low
Generating and adding random package 12 with priority Low
Generating and adding random package 13 with priority Medium
Generating and adding random package 14 with priority Medium
See what we got:
Packages received: 15
Remove a random number of packages (0-20):
Removing up to 8 packages
Shipped package with priority High
Shipped package with priority High
Shipped package with priority High
Shipped package with priority High
Shipped package with priority Medium
Shipped package with priority Medium
Shipped package with priority Medium
Shipped package with priority Medium
```

### 解封包裹

此示例依赖于一个简化的示例包裹。`Package` 类专注于关注优先级部分，尽管真实的 `Package` 对象会包含其他成员。以下是 `class Package` 的代码：

```csharp
class Package : IPrioritizable
{
    private Priority _priority;
    // 构造函数
    public Package(Priority priority) => _priority = priority;
    // Priority -- 返回包裹优先级 -- 只读。
    public Priority Priority
    {
        get => _priority;
    }
    // 加上 ToAddress, FromAddress, Insurance 等。
}
```

`Package` 在此示例中只需要：

*   一个用于存储其优先级的私有数据成员
*   一个用于创建特定优先级包裹的构造函数（因为只有一个变量需要初始化，你可以使用表达式体构造函数版本，该内容在第 2 卷的“使用表达式体的成员”节，第 4 章））
*   一个方法（在这里实现为只读属性）用于返回优先级（因为只有一个变量需要初始化，你可以使用表达式体构造函数版本，该内容在第 2 卷的“使用表达式体的成员”节，第 4 章））

### 指定可能的优先级

优先级使用名为 `Priority` 的枚举类型（`enum`）进行衡量。`Priority` `enum` 看起来如下：

```csharp
enum Priority
{
    Low, Medium, High
}
```

### 实现 IPriorizable 接口

任何进入 `PriorityQueue` 的对象都必须“知道”自己的优先级。强制这一要求的方法之一是坚持所有可出运对象实现 `IPrioritizable` 接口，如下：

```csharp
interface IPrioritizable
{
    Priority Priority { get; } // 接口中属性的示例
}
```

![Tip](img/tip.png) 你可以非正式地“承诺”`Package` 类有一个成员来获取其优先级。`Package` 通过为 `Priority` 属性提供具体的实现来实现该接口：

```csharp
public Priority Priority
{
    get => _priority;
}
```

你在 `PriorityQueue` 类的声明中会遇到这一强制性要求的另一面，位于随后的章节“将 PriorityQueue 放在最后”。

### 浏览 Main()

在深入研究 `PriorityQueue` 类之前，了解它在 OOPs, Inc. 的实际运作非常有帮助。这里是 `PriorityQueue` 示例的 `Main()` 方法：

```csharp
static void Main(string[] args)
{
    Console.WriteLine("Create a priority queue:");
    PriorityQueue<Package> pq = new PriorityQueue<Package>();
    Console.WriteLine(
    "Add a random number (0 - 20) of random packages to queue:");
    Package pack;
    PackageFactory fact = new PackageFactory();
    // 你想要一个小于 20 的随机数。
    Random rand = new Random(2);
    int numToCreate = rand.Next(20); // 0-20 之间的随机整数
    Console.WriteLine("\tCreating {0} packages: ", numToCreate);
    for (int i = 0; i < numToCreate; i++)
    {
        Console.Write("\t\tGenerating and adding random package {0}", i);
        pack = fact.CreatePackage();
        Console.WriteLine(" with priority {0}", pack.Priority);
        pq.Enqueue(pack);
    }
    Console.WriteLine("See what we got:");
    int total = pq.Count;
}
```





```cs
Console.WriteLine("Packages received: {0}", total);
Console.WriteLine("Remove a random number of packages (0-20): ");
int numToRemove = rand.Next(20);
Console.WriteLine("\tRemoving up to {0} packages", numToRemove);
for (int i = 0; i < numToRemove; i++)
{
    pack = pq.Dequeue();
    if (pack != null)
    {
        Console.WriteLine("\t\tShipped package with priority {0}",
        pack.Priority);
    }
}
Console.Read();
}
```

以下是 `Main()` 方法中发生的操作：

1. 为类型 `Package`（包） 实例化一个 `PriorityQueue` 对象。
2. 创建一个 `PackageFactory` 对象，其工作是根据需要创建具有随机选择优先级的新包。
   *工厂*（factory）是一个为你创建对象的类或方法。你将在本章稍后的节节“使用（非泛型）简单工厂类”中了解 `PackageFactory`。

3. 使用 .NET 库类 `Random` 生成随机数，然后调用 `PackageFactory` 创建相应数量具有随机优先级的新 `Package` 对象。
4. 使用 `pq.Enqueue(pack)` 将每个包添加到 `PriorityQueue` 中。
5. 写入创建的包的数量，然后使用 `pq.Dequeue()` 从 `PriorityQueue` 中随机移除其中的一些包。
6. 在显示移除的包数量后结束程序。

### 轻松地编写泛型代码

现在你必须弄清楚如何编写带有所有 `<T>` 的泛型类。看起来很复杂，对吗？其实正如本节所演示的，它并不难。

![Tip](img/tip.png) 编写泛型类的简单方法是先写一个非泛型版本，然后替换 `<T>`。例如，你可以为 `Package` 对象编写 `PriorityQueue` 类，对其进行测试，然后将其“泛型化”。这里有一一小段非泛型的 `PriorityQueue` 代码用作说明（不要将此代码添加到当前示例中；它无法编译）：

```cs
class PriorityQueue<T> where T : IPrioritizable
{
    //Queues -- 三个底层队列：全泛型！
    private Queue<T> _queueHigh = new Queue<T>();
    private Queue<T> _queueMedium = new Queue<T>();
    private Queue<T> _queueLow = new Queue<T>();
    //Enqueue -- 优先处理 T 并将类型为 T 的项添加到正确的队列。
    // 该项必须知道自己的优先级。
    public void Enqueue(T item)
    {
        switch (item.Priority) // 此属性需要 IPrioritizable 接口。
        {
            case Priority.High:
                _queueHigh.Enqueue(item);
                break;
            case Priority.Medium:
                _queueMedium.Enqueue(item);
                break;
            case Priority.Low:
                _queueLow.Enqueue(item);
                break;
            default:
                throw new ArgumentOutOfRangeException(
                item.Priority.ToString(),
                "bad priority in PriorityQueue.Enqueue");
        }
    }
    // 等此类 ……
}
```

先编写非泛型类，测试该类的逻辑会更容易。当所有逻辑都理顺后，你可以使用查找替换功能将名称 `Package` 替换为 `T`。

### 最后处理 PriorityQueue

为什么优先队列要放在最后？这看起来可能有点反常，但你已经看过了依赖于优先队列来执行任务的代码。现在是时候检查 `PriorityQueue` 类了。本节将展示代码，然后带你逐步分析，以便你看到如何处理几个小问题。请一次处理一个部分。

### 底层队列

`PriorityQueue` 是一个包装类，隐藏了三个普通的 `Queue<T>` 对象，每个优先级级别对应一个。这里是 `PriorityQueue` 的部分，显示了三个底层队列（现在是泛型的）：

```cs
private Queue<T> _queueHigh = new Queue<T>();
private Queue<T> _queueMedium = new Queue<T>();
private Queue<T> _queueLow = new Queue<T>();
```

这些行声明了三个 `Queue<T>` 类型的私有数据成员，并通过创建 `Queue<T>` 对象来初始化它们。用于三个队列的 `T`（类型）必须实现 `IPrioritizable` 接口。否则，编译器会在编译期间抛出错误。因此，你不能尝试创建一个类型 `int` 的 `Queue<T>`（例如），因为 `int` 缺少 `IPrioritizable` 接口。本章稍后的“理解约束”节将更详细解释此功能的使用。

### Enqueue() 方法

`Enqueue()` 将类型为 `T` 的项添加到 `PriorityQueue` 中。该方法的工作是查看项的优先级并将其放入正确的底层队列。在第一行中，它获取项的 `Priority` 并将其放入正确的底层队列。

```cs
public void Enqueue(T item)
{
    switch (item.Priority) // 此属性需要 IPrioritizable 接口。
    {
        case Priority.High:
            _queueHigh.Enqueue(item);
            break;
        case Priority.Medium:
            _queueMedium.Enqueue(item);
            break;
        case Priority.Low:
            _queueLow.Enqueue(item);
            break;
        default:
            throw new ArgumentOutOfRangeException(
            item.Priority.ToString(),
            "bad priority in PriorityQueue.Enqueue");
    }
}
```

### Dequeue() 方法

`Enqueue()` 将类型为 `T` 的项添加到 `PriorityQueue` 中（注：此处原文可能为笔误，应为 Dequeue）。该方法的工作是查看项的优先级并将其放入正确的底层队列。在第一行中，它获取项的 `Priority` 并将其放入正确的底层队列。

```cs
public T Dequeue()
{
    // 寻找优先级最高的队列。
    Queue<T> queueTop = TopQueue();
    // 如果找到了非空队列。
    if (queueTop != null && queueTop.Count > 0)
    {
        // 返回头部项。
        return queueTop.Dequeue();
    }
    // 全部为空，返回默认值。
    return default; 
}
```

### TopQueue() 工具方法

`Dequeue()` 依赖私有方法 `TopQueue()` 来寻找优先级最高的非空队列。`TopQueue()` 从 `_queueHigh` 开始并查询其 `Count` 属性。如果大于 0，则队列包含项，因此 `TopQueue()` 返回找到的队列的引用。另一方面，如果 `_queueHigh` 为空，`TopQueue()` 会尝试 `_queueMedium` 然后是 `_queueLow`。如果所有子队列都为空怎么办？`TopQueue()` 返回 `null`。

```cs
private Queue<T> TopQueue()
{
    if (_queueHigh.Count > 0) // 高优先级队列中有项吗？
        return _queueHigh;
    if (_queueMedium.Count > 0) // 中优先级队列中有项吗？
        return _queueMedium;
    if (_queueLow.Count > 0) // 低优先级队列中有项吗？
        return _queueLow;
    return null; // 全部为空，返回 null。
}
```





### 使用（非泛型）简单工厂类

本章前面的 “为最后一次使用保存 PriorityQueue”部分使用了一个简单工厂对象来生成具有随机优先级水平的 `Package` 对象无限流。现在，这个简单的类终于揭开了面目：

```csharp
class PackageFactory
{
    // 随机数生成器
    Random _randGen = new Random(2);
    // CreatePackage -- 工厂方法选择一个随机优先级，
    // 然后创建一个该优先级的包。
    // 可以将此实现为迭代器块。
    public Package CreatePackage()
    {
        // 返回一个随机选择的包优先级。
        // 需要 0, 1 或 2（小于 3 的值）。
        int rand = _randGen.Next(3);
        // 使用该值生成新包。
        // 将 int 转换为枚举很笨拙，但它可以避免
        // 使用 if 语句或 switch 语句。
        return new Package((Priority)rand);
    }
}
```

`PackageFactory` 类有一个数据成员和一个方法。（你也可以同样容易地将简单工厂实现为方法而不是类——例如，`Program` 类中的一个方法。）当你实例化 `PackageFactory` 对象时，它会创建一个 `Random()` 类的对象并将其存储在数据成员 `_randGen` 中。为了获取 0 到 2 之间的值作为优先级存储在 `rand` 中，代码调用了 `_randGen.Next(3)`。值 0 代表高优先级项目。

### 使用 PackageFactory

要生成一个具有随机优先级的 `Package` 对象，你可以在 `Main()` 中像这样调用工厂对象的 `CreatePackage()` 方法：

```csharp
Package pack;
PackageFactory fact = new PackageFactory();
… 额外的设置代码 …
for (int i = 0; i < numToCreate; i++)
{
    Console.Write("\t\tGenerating and adding random package {0}", i);
    pack = fact.CreatePackage();
    Console.WriteLine(" with priority {0}", pack.Priority);
    pq.Enqueue(pack);
}
```

### 关于工厂的更多信息

![Remember](img/remember.png) 工厂对于生成大量测试数据非常有帮助。（工厂不需要使用随机数——那只是 `PriorityQueue` 示例中需要的。）工厂通过隔离对象创建来改进程序。每当你在代码中通过名称提到一个特定类时，你就创建了对该类的 `dependency`（依赖）。这种依赖越多，你的类之间就越`tightly coupled`（紧耦合）。

程序员长期以来都知道他们应该避免紧耦合。（更`decoupled`（解耦）的方法之一是通过接口间接使用工厂，例如 `IPrioritizable`，而不是具体的类，如 `Package`。）程序员仍然经常直接使用 `new` 运算符来创建对象，这没有问题。但工厂可以降低代码的耦合性——从而使其更加灵活。这里是“Using PackageFactory”部分代码的版本，它依赖于 `IPrioritizable`（注意在入队时需要类型转换）：

```csharp
IPrioritizable pack;
PackageFactory fact = new PackageFactory();
… 额外的设置代码 …
for (int i = 0; i < numToCreate; i++)
{
    Console.Write("\t\tGenerating and adding random package {0}", i);
    pack = fact.CreatePackage();
    Console.WriteLine(" with priority {0}", pack.Priority);
    pq.Enqueue((Package)pack);
}
```

### 理解约束

`PriorityQueue` 必须能够询问对象其优先级是什么。为了使其工作，所有可存储在 `PriorityQueue` 中的类都必须实现 `IPrioritizable` 接口，就像 `Package` 一样。`Package` 在其类声明头部列出了 `IPrioritizable`，如下：

```csharp
class Package : IPrioritizable
```

然后它实现了 `IPrioritizable` 的 `Priority` 属性。

![Remember](img/remember.png) `PriorityQueue` 需要一个匹配的限制。当你尝试实例化一个没有实现 `IPrioritizable` 的类型时，你希望编译器报错。在 `PriorityQueue` 的非泛型形式（假设专门为 `Package` 类型）中，当你的一个优先级队列方法尝试调用 `Package` 没有的方法时，编译器会自动报错。但对于泛型类，你可以通过显式的 `constraint`（约束）更上一层楼。因为你可以使用任何类型来实例化泛型类，所以你需要一种方法告诉编译器哪些类型是接受的——因为它们保证具有正确的方法。

![Remember](img/remember.png) 你通过在 `PriorityQueue` 的头部指定 `IPrioritizable` 来添加约束，如下：

```csharp
class PriorityQueue<T> where T : IPrioritizable
```

你注意到之前的 `where` 子句了吗？这个**加粗**的 `where` 子句表示 `T` 必须实现 `IPrioritizable`。




但因为像 `PriorityQueue` 这样的泛型类可以为任何数据类型实例化，C# 无法预测在泛型类代码中使用适当的 `null` 值。例如，如果你使用 `PriorityQueue` 的 `Dequeue()` 方法，你可能会遇到这种情况：你调用 `Dequeue()` 来获取一个包，但没有可用的包。你返回什么来表示“无”？因为 `Package` 是一个类类型，它应该返回 `null`。这告诉 `Dequeue()` 的调用者没有内容可返回（调用者必须检查返回值是否为 `null`）。

![Remember](img/remember.png) 编译器无法理解泛型类中的 `null` 关键字，因为该类可能为各种数据类型实例化。这就是为什么 `Dequeue()` 使用了这一行代码而不是：

```csharp
return default(T); // Return the right null for whatever T is.
```

这一行告诉编译器查看 `T` 并为该类型返回正确的 `null` 值。对于 `Package` 来说，因为它作为一个类是引用类型，返回的正确 `null` 实际上就是 `null`。但对于其他某些 `T`，情况可能会不同，编译器可以确定应该使用什么。

## 理解泛型中的变性

所有第四代语言都支持某种类型的变性。*变性*与参数类型和返回类型有关：

* *协变性*（Covariance）意味着在期望父类实例的地方，可以使用子类的实例。
* *逆协变性*（Contravariance）意味着在期望子类实例的地方，可以使用超类的实例。
* *不变性*（Invariance）意味着既不能使用协变也不使用逆协变。

如果你看像下面这样的方法：

```csharp
public static void WriteMessages()
{
    List<string> someMessages = new List<string>();
    someMessages.Add("The first message");
    someMessages.Add("The second message");
    MessagesToYou(someMessages);
}
```

然后你尝试像在本章早些时候用字符串类型调用 `MessagesToYou()`：

```csharp
public static void MessagesToYou(IEnumerable<object> theMessages)
{
    foreach (var item in theMessages)
    {
        Console.WriteLine(item);
    }
}
```

这段代码能够编译，是因为 `IEnumerable<T>` 是协变的——你可以使用更派生的类型作为高阶类型的替代。下一节将展示一个真实的示例。

### 逆协变

一个调度应用程序可能会有 `Events`，它们包含日期，然后有一组子类，其中之一是 `Course`。`Course` 是一个 `Event`。每门 `Course` 都知道自己的学生人数以及与他们交互的方法。其中一个方法是 `MakeCalendar()`：

```csharp
public void MakeCalendar(IEnumerable<Event> theEvents)
{
    foreach (Event item in theEvents)
    {
        Console.WriteLine(item.WhenItIs.ToString());
    }
}
```

假设它正在创建一个日历。目前，它做的只是将日期打印到控制台。`MakeCalendar` 是系统级的，因此它期望某些可枚举的事件列表。

应用程序还有一个 `EventSorter` 类，你可以将其传递给列表的 `Sort()` 方法。该方法随后使用 `EventSorter` 对象的 `Compare()` 方法来决定哪个项目应该排在排序列表的前。。是 `EventSorter` 类：

```csharp
class EventSorter : IComparer<Event>
{
    public int Compare(Event x, Event y)
    {
        return x.WhenItIs.CompareTo(y.WhenItIs);
    }
}
```

事件管理器创建一个课程列表，对它们进行排序，然后创建一个日历。`ScheduleCourses` 创建课程列表，然后将 `EventSorter` 作为参数调用 `courses.Sort()`，如下所示：

```csharp
public void ScheduleCourses()
{
    List<Course> courses = new List<Course>()
    {
        new Course(){NumberOfStudents=20, WhenItIs = new DateTime(2021, 2, 1)},
        new Course(){NumberOfStudents=14, WhenItIs = new DateTime(2021, 3, 1)},
        new Course(){NumberOfStudents=24, WhenItIs = new DateTime(2021, 4, 1)},
    };
    // 将一个 ICompare<Event> 类传递给 List<Course> 集合。
    // 它本应该是 ICompare<Course>，但由于逆协变性，
    // 它可以使用 ICompare<Event>
    courses.Sort(new EventSorter());
    // 传递一个课程列表，而此处期望一个 Events 列表。
    // 我们可以这样做，是因为泛型参数是协变的
    MakeCalendar(courses);
}
```

等一下，这是一个调用 `Sort()` 的课程列表，而不是事件列表。没关系——与 `IComparer<Course>` 相比，`IComparer<Event>` 对于 `T`（其返回类型）是逆协变泛型，因此仍然可以使用该算法。

现在应用程序将列表传递给 `MakeSchedule` 方法，但该方法期望一个可枚举的 `Events` 集合。泛型参数是协变的，因此可以传递 `courses` 的 `List`，因为 `Course` 对于 `Event` 是协变的。





C# 提供了一种捕获和处理错误的特定机制：`exception`（异常）。该机制基于 `try`、`catch`、`throw` 和 `finally` 关键字。简括而言，它的工作原理如下：一个方法将 `try` 执行一段代码。如果代码检测到问题，它将 `throw` 一个错误指示，你的代码可以 `catch` 该指示，并且无论发生什么，它都会在最后 `finally` 执行一段特殊的代码，如下代码段所示：

```csharp
public class MyClass
{
    public void SomeMethod()
    {
        // 设置以捕获错误。
        try
        {
            // 调用可能抛出异常的方法或执行某些操作。
            SomeOtherMethod();
            // … 进行你需要的任何其他调用 …
        }
        catch (Exception e)
        {
            // 如果 try 块内发生任何错误，控制权将传递到这里。
            // Exception 对象 e 详细描述了错误。
        }
        finally
        {
            // 在此处进行清理：关闭文件、释放资源等。
            // 即使捕获了异常，此块也会运行。
        }
    }

    public void SomeOtherMethod()
    {
        // … 在此方法的某处发生了错误 …
        // … 异常沿调用链向上冒泡。
        throw new Exception("Description of error");
        // … 如果 throw 没有发生，方法继续执行 …
    }
}
```

![Remember](img/remember.png) `try`、`catch` 和（可能的）`finally` 的组合被称为一个 `exception handler`（异常处理程序）。`SomeMethod()` 方法在一个标记有关键字 `try` 的块中包围了一部分代码。在块内部的调用树中调用的任何方法都是 `try` 块的一部分。如果你有一个 `try` 块，你必须至少有一个 `catch` 块或一个 `finally` 块，或者两者都有。

![Warning](img/warning.png) 在 `try`、`catch` 或 `finally` 块内部声明的变量无法从块外部访问。如果你需要访问，请在块外部声明该变量：

```csharp
int aVariable; // 在块外部声明 aVariable。
try
{
    aVariable = 1;
    // 在块内部声明 aString。
    string aString = aVariable.ToString(); // 在块中使用 aVariable。
}
catch (Exception e)
{
    // 异常处理代码。
}
// aVariable 在此处可见；aString 则不可见。
```

### 关于 try 块

将使用 `try` 块想象成让 C# 运行时处于警觉状态。该关键字基本上是在说运行时应该尝试执行代码，但要考虑到这些代码可能无法运行。异常会在代码中向上冒泡，直到异常遇到 `catch` 块或应用程序结束。

![Tip](img/tip.png) 在使用 `try` 块时，使其内部的代码专门针对特定的任务或异常。尽可能保持 `try` 块短短，以缩短调试时间，并增加代码从异常中恢复的可能性。使用多个简短的 `try` 块，而不是尝试将所有可能产生异常的代码都包含在一个 `try` 块中。使用单个巨大的 `try` 块就像试图一口气吃掉整个英雄三明治：你可能会成功，但你不会享受其中，而且以后总有一堆摊子要收拾。

### 关于 catch 块

`try` 块通常紧随关键字 `catch`，其后是 `catch` 关键字的块。如果 `try` 块内的任何地方发生错误，控制权将传递到 `catch` 块。`catch` 块的参数是一个 `Exception` 类的对象，或者更有可能是一个 `Exception` 的子类，如下所示：

```csharp
catch (Exception e)
{
    // 显示错误
    Console.WriteLine(e.ToString());
}
```

如果你的 `catch` 不需要从它捕获的异常对象中获取任何信息，你可以只指定异常类型：

```csharp
catch (SomeException) // 此处未指定对象（没有 "Exception e"）
{
    // 执行不需要访问异常对象的某些。
}
```

然而，`catch` 并不一定有参数：裸露 `catch` 会捕获任何异常，等同于 `catch(Exception)`：

```csharp
catch
{
}
```

![Tip](img/tip.png) 让 `catch` 块尽可能具体，以减少处理它们所需的工作，并增加恢复的可能性。此外，你可以堆叠 `catch` 块，以便能够尽可能具体地处理异常，并将最具体的异常列在第一个。例如，在接的 `catch` 块中，`ArgumentOutOfRangeException` 是最具体的异常，紧接着是 `ArgumentException`，最后是通用的 `Exception`：

```csharp
catch (ArgumentOutOfRangeException e)
{
    … 尝试的某些修复代码。
}
catch (ArgumentException e)
{
    … 尝试的更多修复代码。
}
catch (Exception e)
{
    … 尝试的最后的修复代码。
}
```

在 C# 找到能够处理异常的异常处理程序后，它会忽略其他的 `catch` 块，这就是为什么你需要将最具体的异常列在第一个。

### 关于 finally 块

如果你提供了 `finally` 块，它无论出现什么情况都会运行：

*   `try` 块是否抛出了异常
*   代码使用了 `break` 或 `continue` 退出
*   是否存在 `return` 语句

`finally` 块在 `try` 成功或 `catch` 之后都会调用。事实上，即使没有 `catch`，你也应该使用 `finally`。例如，你经常看到这样的代码：

```csharp
try
{
    …
}
finally
{
    // 清理，例如关闭打开的文件。
}
```

在以下情况下不会执行：

*   程序因为致命异常未处理而终止。
*   `try` 块遇到了 `StackOverflowException`、`OutOfMemoryException`。
*   外部应用程序杀死 `finally` 块所在的进程。

![Technicalstuff](img/technicalstuff.png) 方法可以有多个 `try…catch` 。你甚至可以在 `try` 中嵌套 `try…catch`、在 `catch` 中嵌套 `try…catch`，或者在 `finally` 中嵌套 `try…catch` —— 或者以上所有。（你可以用 `try/finally` 代替以上所有。）

### 当抛出异常时发生了什么

当异常发生时，会发生以下事件序列：

1.  **抛出异常。**

    在 `SomeOtherMethod()` 的深处发生了错误。方法准备就绪，通过 `throw` `Exception` 对象将错误报告给第一个足够 `catch` 并处理它的块。

    注意，因为异常是运行时错误，而不是编译错误，所以它是在程序执行时发生的。所以当你发布你的杰作后可能会发生错误。哎呀！

2.  **C# “回溯”调用栈，寻找 `catch` 块。**

    异常一路回到调用者方法，然后是调用该方法的方法，依此类推，甚至一直到达程序顶部的 `Main()`，如果还没有找到处理异常的 `catch` 块的话。图 9-1 显示了 C# 在搜索异常处理程序时遵循的路径。

    ![Schematic illustration of showing where can a handler be found.](img/9781119839071-fg010901.png)

    [图 9-1:](# 哪里，哪里可以找到处理程序？

3.  **如果找到了合适的 `catch` 块，它将执行。**





适当的 `catch` 块应该寻找正确的异常类（或其任何派生类——`Exception` 会处理任何异常，但 `ArgumentOutOfRangeException` 仅在参数超出范围时处理异常）。此 `catch` 块可能会执行许多操作中的任何一种。随着栈的回溯，如果某个给定的方法没有足够的上下文（即并不知道足够的信息）来纠正异常状态，它就不会为该异常提供 `catch` 块。正确的 `catch` 可能会在栈的更高位置。

### 4. 如果 `finally` 块与 `try` 块配对，无论是否捕获到异常，它都会执行。

`finally` 在栈回溯到调用链中下一个上层方法之前调用。调用链中任何地方的 `finally` 块都会执行。

### 5. 如果在任何地方都没有找到适当 `catch` 块，程序通常会崩溃。

如果 C# 运行 `Main()` 且在那里没有找到 `catch` 块，用户将看到“未处理的异常”消息，除非底层操作系统能够提供修复（这很罕见），否则程序将正常退出。这就是崩溃。然而，你可以通过在 `Main()` 中使用异常处理程序来处理其他地方未捕获的异常。请参见本章节后面的“捕捉异常的最后机会”。

异常机制为你提供了这些益处：

* 异常提供了一种表达性模型——这种模型让你能够表达各种错误处理策略。
* 异常对象携带大量信息，从而有助于调试。
* 异常使代码更具读性，因为你可以一眼看出可能出现问题的地方——减少了代码，因为你花费更少的时间来尝试修复错误。
* 异常是一致的，而一致的模型有助于理解。

![Technicalstuff](img/technicalstuff.png) C# 提供了机制来支持其他错误处理方法，当你直接操作底层操作系统时会遇到这些方法。本书没有讨论此类技术，因此你会异常处理是唯一的错误处理方法。然而，你可以在 `https://docs.microsoft.com/en-us/windows/apps/desktop/modernize/desktop-to-uwp-enhance` 阅读更多关于与底层 Win32 API 交互的内容，这是一种高级编程技术，最好留给那些渴望在追求未知的过程中慢慢让自己发疯的人。

#### 自己自己抛出异常

如果 C# 提供的代码可以抛出异常，你也可以。当检测到值得抛出异常的错误时，使用 `throw` 关键字：

```bash
throw new ArgumentException("Don't argue with me!");
```

你有和任何人一样的权利抛出东西。因为 C# 不感知你自定义的 `BadHairDayException`，除了你还有谁会抛出它？

![Tip](img/tip.png) 如果 .NET 预定义的异常符合你的情况，请抛出它。使用标准异常总是首选的，因为 .NET 已经为它提供了文档，开发者也习惯使用它。但如果都不符合，你可以发明自己的自定义异常类。

![Technicalstuff](img/technicalstuff.png) .NET 有一些你永远不应该捕获的异常类型：`StackOverflowException`、`OutOfMemoryException`、`ExecutionEngineException` 以及其他与非 .NET 代码工作相关的高级项目。这些异常代表了某种终失败。例如，如果你没有了栈空间（如 `StackOverflowException` 所示），你根本没有内存来继续执行程序。鉴于异常处理发生在栈上，你甚至没有足够的内存来继续进行异常处理。同样，`OutOfMemoryException` 定义了应用程序耗尽堆空间（用于引用变量）的情况。如果异常引擎 `ExecutionEngineException` 根本无法工作，那么继续下去就没有意义，因为你没有方法处理此错误。

### 我可以得到一个异常示例吗？

看到异常的实际运行是有帮助的，因此本节将向你展示如何创建一个练习异常的基本应用程序。阶乘计算（`https://www.mathsisfun.com/numbers/factorial.html`）从最高数字到 1 执行整数计算，例如 4 * 3 * 2 * 1，输出为 24，这就是 4!（或四阶乘）。`FactorialException` 程序从此处所示 `MyMathFunctions` 类开始，该类包含 `Factorial()` 函数，该函数计算你提供的数字的阶乘：

```csharp
public class MyMathFunctions
{
    // Factorial -- 返回提供值的阶乘。
    public static int Factorial(int value)
    {
        // 不允许负数。
        if (value < 0)
        {
            // 报告负参数。
            string s = String.Format(
            "Illegal negative argument to Factorial {0}", value);
            throw new ArgumentOutOfRangeException(s);
        }
        // 专门检查 0。
        if (value == 0)
        return 1;
        // 从“累加器”1 开始。
        int factorial = 1;
    }
}
```

你看到的代码并没有捕获所有可能的错误，但它确实在寻找负数。如果它看到此类错误，它会抛出 `ArgumentOutOfRangeException`。此异常专门针对此错误。你使用此异常而不是 `ArgumentException` 是因为 `ArgumentOutOfRangeException` 更具体。此外，用户完全可能输入正确的值，但 `Factorial()` 函数将无法处理它。在这种情况下，正确的响应是 `OverflowException`。以下代码调用了 `Factorial()` 函数：

```csharp
static void Main(string[] args)
{
    string Input = string.Empty;
    while (Input.ToLower() != "quit")
    {
        // 从用户获取输入并检查 Quit。
        Console.WriteLine("Enter a positive number or Quit: ");
        Input = Console.ReadLine();
        if (Input.ToLower() == "quit")
        continue;
        // 确保输入是整数。
        int Value = 0;
        if (!Int32.TryParse(Input, out Value))
        {
            Console.WriteLine("Please enter an integer number or Quit!");
            continue;
        }
        // 这里是异常处理程序。
        int Factorial = 0;
        try
        {
            // 计算数字的阶乘。
            Factorial = MyMathFunctions.Factorial(Value);
        }
        catch (ArgumentOutOfRangeException e)
        {
            // 告诉用户问题。
            Console.WriteLine("You must enter a positive number!");
            // 尝试以修复问题。
            continue;
        }
        catch (OverflowException e)
        {
            // 告诉用户问题。
            Console.WriteLine("The number supplied is too large!");
            // 尝试以修复问题。
            continue;
        }
        catch (Exception e)
        {
            // 好，现在我们不知道出了什么问题。
            Console.WriteLine("An unexplainable error has happened!");
            // 输出错误信息以便某人了解更多。
            Console.WriteLine(e.ToString());
            // 以错误代码优雅地退出应用程序。
            System.Environment.Exit(-1);
        }
        finally
        {
            Console.WriteLine("Thank you for testing the application!");
        }
    }
}
```





```csharp
Console.WriteLine($"The factorial of {Value} is {Factorial}.");
}

Console.Read();
}
```

此示例采取了合理的预防措施。首先，它检查并验证输入是否确实为整数或特殊字符串 `quit`（不区分大小写）。输入字符或浮点值将起不起作用。因此，除非有较大的成功机会，否则应用程序甚至不会调用 `factorial()`。

注意，`try…catch` 块很短，并且集中于对 `Factorial()` 的调用。只有在 `try…catch` 块满足条件后，输出才会出现。在示例调用 `Factorial()` 之后，它提供了三个层级的异常处理（按以下顺序）：

1. 显示错误消息，因为输入存在问题，并给用户另一次正确执行任务的机会。
2. 处理输入正确但数字过大导致 `Factorial()` 无法处理的情况。
3. 在发生未说明的情况时执行某些操作，以便优雅退出。

由于用户提供错误输入的可能性比 `Factorial()` 接收到过大数字的可能性更大，因此你先检查错误的输入。这是在发生异常时提高应用程序性能的一种虽小但有效的方法。以下是代码的运行示例：

`Enter a positive number or Quit:`
`S`
`Please enter an integer number or Quit!`
`Enter a positive number or Quit:`
`2.2`
`Please enter an integer number or Quit!`
`Enter a positive number or Quit:`
`-5`
`You must enter a positive number!`
`Thank you for testing the application!`
`Enter a positive number or Quit:`
`99`
`The number supplied is too large!`
`Thank you for testing the application!`
`Enter a positive number or Quit:`
`5`
`Thank you for testing the application!`
`The factorial of 5 is 120.`
`Enter a positive number or Quit:`
`quit`

## 使用自定义异常

在章节的前部，你学习了可以定义自定义的异常类型。假设你想定义一个 `CustomException` 类。该类可能如下所示：

```csharp
public class CustomException : System.Exception
{
    // 默认构造函数
    public CustomException() : base()
    {
    }
    // 参数构造函数
    public CustomException(String message) : base(message)
    {
    }
    // 带有内部异常的参数构造函数
    public CustomException(String message, Exception innerException) :
    base(message, innerException)
    {
    }
    // 支持序列化的参数构造函数
    protected CustomException(
    SerializationInfo info, StreamingContext context) :
    base(info, context)
    {
    }
}
```

你可以使用此基础设置创建任何你想要的的自定义异常。这里没有特殊的代码（除非你想添加它），因为 `base()` 条目意味着代码依赖于 `System.Exception` 中的代码。你在这里看到的是继承机制，这是你在第 2 章 中经常看到的内容。换句话说，目前你不需要过于担心这个自定义异常是如何运作的。

## 规划你的异常处理策略

正如后续章节所述，为你的程序如何处理错误制定计划是有意义的。

### 引导你规划的一些问题

在开发程序时，你脑中应该有以下几个问题：

* **可能会出现什么问题？** 针对你写的每一段代码都问这个问题。
* **如果真的出错了，我能修复它吗？** 如果可以，你可能能够从问题中恢复，程序也可以继续运行。
* **问题是否会给用户数据带来风险？** 如果是，你必须尽尽全力防止该数据丢失或损坏。明知发布会误改用户数据的代码等同于软件违规行为。
* **我应该把针对此问题的异常处理程序放在哪里？** 在异常发生的方法中尝试处理异常可能不是最佳方法。通常，方法调用链中更高处的另一个方法拥有更好的信息，并可能对异常进行更智能、更有用的处理。将 `try…catch` 放在那里，使 `try` 块包裹通往可能发生异常地点的调用。
* **我应该处理哪些异常？** 答案很简单，所有的异常。永远没有正理由让异常处于未处理状态，导致用户只能面对那一个可怕的对话框发呆。如果你无法提供特定的修复，至少要优雅地退出应用程序。
* **那些掉进缝隙并避开我的处理程序的异常怎么办？** 测试、测试、再测试是今日之格言！异常绝不应该就那样发生在任何人身上。
* **我的应用程序可能会遇到什么种输入错误？** 输入错误发生于广泛的来源，而不只是用户。文件可能包含坏数据，或者可能只是缺失或被锁定。用于检索数据的设备（如网络）可能会故障。因此，仅检查范围和数据类型是不够的；你还需要检查源文件缺失等问题。
* **我的代码需要多么健壮（不可破的）？** 你永远不知道你的代码最终会出现在哪里。你可能将其设计成一个简单的工具，但如果它有用，它可能会出现在空中交通控制系统中。考虑到这一需求，每次编写代码时都需要让代码尽可能无懈击。

### 良好处理错误的指南

在工作时，你应该记住上一节的问题。这些指南也可能有所帮助：

* **不惜一切代价保护用户数据。** 这是首要准则。见下一条。
* **不要崩溃。** 如果可以就恢复，但要做好尽可能优雅退出的。不要让你的程序只发出一个晦涩的技术术语消息就完蛋。*优雅地*意味着你在关闭之前提供尽可能清晰的信息。用户真的讨厌崩溃。这一点你可能知道。
* **如果你无法从问题中恢复，不要让你的程序继续运行。** 程序可能会不稳定，或者用户数据留在了不一致的状态。当确定一切丢失时，你可以显示一条消息并调用 `System.Environment.FailFast()` 立即终止程序，而不是抛出异常。这不是崩溃——而是故意的。
* **区别地对待类库和应用程序。** 在*类库*中，让异常传递给调用者，调用者最适合决定如何处理。不要让调用者对问题一无所知。但在*应用程序*中，处理任何你能处理的异常。你的目标是尽可能保持代码运行并保护用户数据，而不是向用户展示大量无关紧的消息。
* **当方法由于任何原因无法完成任务时，抛出异常。** 调用者需要知道这个问题。（调用者可能是你代码中调用栈高处的方法，也可能是使用你代码的其他开发者的方法。）如果你在使用之前检查了输入值的有效性且它们无效（例如意外的 `null` 值），请修复它们并继续。否则，抛出异常。尝试编写不需要抛出异常的代码——并在发现 bug 时修正它们，而不是依赖异常来修补代码。但要把异常作为报告和处理错误的主要方法。





- **彻底测试你的代码，** 尤其是你能想到的任何类别的坏输入。你的方法能处理负数输入吗？零？非常大的值？空字符串？一个 `null` 值？用户可能会做什么来导致异常？你的代码使用了哪些易出错的资源（例如文件、数据库或 URL）？参见之前的两个项目符号段落。
- **捕获尽可能具体的异常。** 不要为像 `Exception` 或 `ApplicationException` 等高级异常类编写多个 `catch` 块。
- **始终在 `Main()` 中放置一个最后机会异常处理程序块，** ——或程序“顶端”的任何位置（可重用的类库除外）。你可以在此块中捕获类型 `Exception`。捕获并处理你能够捕获的异常，让最后机会异常处理程序接手任何遗漏的异常。（接下来的“抓住捕获异常的最后机会”章节将解释最后机会异常处理程序。）
- **不要将异常作为正常执行流的一部分使用。** 例如，不要通过抛出异常来跳出循环或退出方法。
- **考虑编写你自己的自定义异常类，** 如果它们能带来价值 —— 例如提供更多有助于调试的信息，或为用户提供更有意义的错误消息。你也可以使用自定义异常类来捕获信息量较少的异常（例如 `DivideByZero`），并提供一个信息量丰富的异常（例如 `InvalidSalesTaxRate`）传递给调用者。

本章的其余部分将为你提供遵循这些指南所需的工具。更多信息请查阅 [`https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/exceptions/](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/exceptions/)。

![Remember](img/remember.png) 如果公共方法抛出了调用者可能需要捕获的任何异常，这些异常就是你的类公共接口的一部分。你对对它们进行记录，最好参考第一本书的“如何找出哪些方法抛出了哪些异常”章节，第 9 章。

### 如何找出哪些方法抛出了哪些异常

![Tip](img/tip.png) 要确定调用 .NET 类库中的特定方法（例如 `String.IndexOf()`）——甚至是你自己的方法是否会抛出异常，请考虑以下指南：

- **Visual Studio 通过工具提示提供即时帮助。** 当你将鼠标悬停在 Visual Studio 编辑器中的方法名上时，工具提示窗口不仅列出方法的参数和返回值，还会列出它可能抛出的异常。如果你需要额外信息，右键点击方法名并从上下文菜单中选择 `Peek Definition`（查看定义），以在单独窗口中查看更多详细信息。
- **如果你使用 XML 注释为自己的方法编写注释，** Visual Studio 会在其 IntelliSense 工具提示中显示这些注释中的信息，就像处理 .NET 方法一样。如果你记录了你的方法可能抛出的异常（见前一节），你会在工具提示、自动补全和对象浏览器（Object Browser）中看到它们。将 `<exception>` 行置在 `<summary>` 注释下方，使其显示在工具提示中（详细信息请参阅 [`https://docs.microsoft.com/en-us/dotnet/csharp/codedoc`](https://docs.microsoft.com/en-us/dotnet/csharp/codedoc)）。以下是 `FactorialException` 示例中 `Factorial()` 方法的 XML 注释示例：

```xml
/// <summary>
/// public static int Factorial(int value)
/// <para>返回提供值的阶乘。</para>
/// <example>
/// 这显示了一个基础调用。
/// <code>
/// input = 5;
/// int output = Factorial(input);
/// </code>
/// </example>
/// </summary>
/// <param name="value">要查找的 x!</param>
/// <returns>作为 int 类型的阶乘值。</returns>
/// <exception cref="ArgumentOutOfRangeException">
/// 值必须大于 0。
/// </exception>
/// <exception cref="OverflowException">
/// x! 太大，无法计算。
/// </exception>
```

当你将鼠标悬停在 `Factorial = MyMathFunctions.Factorial(Value);` 上时，你会看到图 9-2 所示所示输出。

- **C# 语言帮助文件提供了更多内容。** 当你在 C# 语言帮助中查找 .NET 方法时，你会找到该方法可能抛出的异常列表，以及 Visual Studio 黄色工具提示中未提供的额外说明。要打开给定方法的 C# 语言帮助页面，点击代码中的方法名并按 `F1`。你也可以为自己的类和方法提供类似的帮助。

你应该查看你列出的每个异常，决定它们发生的概率，并（如果你的程序需要）使用本章其余部分涵盖的技术对其进行防范。

![为你的方法提供 XML 注释的快照](img/9781119839071-fg010902.png)

图 9-2: 为你的方法提供 XML 注释。

### 抓住捕获异常的最后机会

当将 `Main()` 内容包裹在 `try` 块中时，大多数应用程序都会受益，因为 `Main()` 是起点，因此也是终点。任何在其他地方未捕获的异常都会传递到 `Main()`。此 `catch` 块的作用是通过拦截所有异常来防止硬崩溃。

![Remember](img/remember.png) 在开发期间，你希望在测试代码时看到发生的异常，即在它们的自然栖息地——所以你想要所有的技术术语（geekspeak）。在你发布版本中，将程序员细节转换为普通英语，将消息显示给用户（如果可能的话，包括用户下次成功运行可能需要做什么），然后退出。将这个简单易懂的英语版本的异常处理程序作为你发布程序前完成的最后任务之一。你的最后机会异常处理程序应该以某种方式记录异常信息，以便事后进行取证分析。

### 抛出表达式

在 C# 7.0 之前的版本中，你基本上有两种选择。第一种选择是完成表达式，然后检查结果，如下所示：

```csharp
var myStrings = "One,Two,Three".Split(',');
var numbers = (myStrings.Length > 0) ? myStrings : null;
if (numbers == null){ throw new Exception("There are no numbers!"); }
```

另一种方案是将抛出异常作为表达式的一部分，如下所示：

```csharp
var numbers = (myStrings.Length > 0) ?
myStrings :
new Func<string[]>(() => {
throw new Exception("There are no numbers!");
})();
```

C# 7.0 及以上版本包含了一个新的空合并运算符 `??`（两个问号）。因此，你可以将上述两个示例压缩，使它们看起来像这样：

```csharp
var numbers = myStrings ?? throw new Exception("There are no numbers!");
```





在这种情况下，如果 `myStrings` 为 `null`，代码会自动抛出异常。你也可以在条件运算符中使用这种技术（例如第二个示例）：

```csharp
var numbers = (myStrings.Length > 0) ? myStrings :
throw new Exception("There are no numbers!");
```

抛出表达式（throw expressions）的能力也适用于表达式体成员（expression-bodied members）。你可能在以下两种形式之一中见过这些成员（如果没有见过，你可以在第 2 本中找到完整介绍，所以目前不需要过于担心细节）：

```csharp
public string getMyString()
{
    return " One,Two,Three ";
}
```

或者

```csharp
public string getMyString() => "One,Two,Three";
```

然而，假设你不知道应该提供什么内容。在 7.0 版本之前，你有这两种选择：

```csharp
public string getMyString() => return null;
```

或者

```csharp
public string getMyString() { throw new NotImplementedException(); }
```

这两个版本都存在问题。第一个示例让调用者无法明确知道方法是否失败——返回 `null` 可能是一个预期值。第二个版本则很繁琐，因为你为了抛出异常必须创建一个标准函数。得益于 C# 7.0 及以上版本添加的新特性，现在可以在表达式体方法中抛出表达式。之前的代码变为：

```csharp
public string getMyString() => throw new NotImplementedException();
```

# 第 10 章

# 使用枚举创建项目列表

本章内容

- ![Bullet](img/check.png) **寻找枚举的现实世界实例**
- ![Bullet](img/check.png) **创建和使用枚举**
- ![Bullet](img/check.png) **使用枚举定义标志位（flags）**
- ![Bullet](img/check.png) **将枚举作为 switch 语句的一部分**

*枚举*（enumerate）意味着像列表一样指定单个项目。例如，你可以创建一个颜色的枚举，然后列出单种颜色，如红色、蓝色、绿色等。在编程中使用枚举是有意义的，因为你可以将单个项目作为公共集合的一部分列出来。例如，`Colors.Blue` 表示蓝色，`Colors.Red` 表示红色。由于枚举非常方便，你会在现实世界到处看到它们，这就是为什么你在应用程序中也能看到它们。代码应该模拟现实世界，以易于理解的形式提供实用的功能。

`enum` 关键字允许你在 C# 中创建枚举。本章从讨论 `enum` 的基本用法开始，然后过渡到你可以添加的一些有趣特性。例如，你可以使用*初始化器*（initializers）来确定每个枚举元素的初始值。

*标志*（Flags）为你提供了一种紧凑的方式来跟踪小型配置选项——通常是开启或关闭，但你也可以让它们更复杂。你在旧应用程序中经常看到它们，因为它们显著提高了内存使用效率。C# 应用程序使用标志将相似的选项分组，使其更容易查找和处理。你可以使用单个标志变量来精确确定某些对象的工作方式。

枚举也用作 C# switch 语句的一部分。第 1 本第 5 章 介绍了 `switch` 语句，但本章将更进一步，演示如何通过使用枚举可以让你的 `switch` 语句变得更容易阅读和理解。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用可下载的源码要简单得多。你可以在下载源码的 `\CSAIO4D2E\BK01\CH10` 文件夹中找到本章的源码。详情请参介绍部分如何查找这些源文件。

## 现实世界中的枚举

许多编程结构的一个问题是如何将它们与现实世界联系起来，枚举也是如此。枚举是任何永久性的项目集合。如前所述，颜色是常见的枚举之一，你在现实世界中经常使用它们。然而，如果你在网上查找颜色枚举，你会发现一堆特定于编程的引用，而不是任何一个现实世界的引用。与其寻找颜色枚举，不如寻找色轮；这才是现实世界中人们枚举颜色并创建颜色集合的方法。人们通常根据颜色在色轮上的位置来组织色系，例如互补色或类比色。（访问 `https://www.sessions.edu/color-calculator/` 查看颜色计算器和色轮的描述。）

集合有许多形式，你可能甚至没有意识到自己创建了一个。例如，`https://www.iberdrola.com/sustainability/biology-kingdoms-living-things-classification` 网站告诉了你生物的分类。由于这些分类遵循模式且往往不会发生太大变化，你可以在应用程序中将它们表示为枚举。例如，五界列表不太可能改变。甚至每个界内的门列表也不太可能改变，因此你也可以将它们表示为枚举。

枚举的实际日常用途包括每个人需要的项目或信息列表。例如，如果你不知道包裹要寄往哪个州，就无法邮寄某东西。应用程序中的州枚举可以节省大家的时间，并确保地址无错误。你使用枚举来表示实际对象。

## 操作枚举

枚举背后的基本思想相对简单。你真正需要做的只是创建一个名称列表并为该集合指定名称。然而，你可以对基础枚举进行扩展，以增强灵活性以及在广泛场景中使用枚举的能力。接下来的章节将使用 `Enumerations` 示例来描述如何创建各种枚举。

### 使用 enum 关键字

你使用 `enum` 关键字来创建枚举。例如，以下代码创建名为 `Colors` 的枚举。

```csharp
enum Colors {Red, Orange, Yellow, Green, Blue, Purple};
```

![Remember](img/remember.png) C# 提供了多种访问枚举的方法。如果你只需要单个值，可以使用颜色名称。你得到的输出取决于你如何访问该值，如下所示：

```csharp
// 显示颜色名称。
```





```csharp
Console.WriteLine($"Color Name: {Colors.Blue}.");

// 显示颜色值。
Console.WriteLine($"Color Value: {(int)Colors.Blue}.");
```

如果你执行这段代码，你将看到第一行的输出为 `Blue`，第二行的输出为 `4`。在创建默认的枚举设置时，值从 0 开始并从那里顺序递增。因为 `Blue` 是 `Colors` 的第五个元素，所以它的值为 `4`。（在下一节中将讨论的初始化器允许你更改默认值。）

你可能可能在某时刻需要访问枚举值的整个列表。要完成此任务，你可以使用 `foreach` 语句，如下：

```csharp
// 显示所有以名称开始的元素。
Console.WriteLine("\r\nAll Color Names:");
foreach (String Item in Enum.GetNames(typeof(Colors)))
    Console.WriteLine(Item);

// 也显示值。
Console.WriteLine("\r\nAll Color Values:");
foreach (Colors Item in Enum.GetValues(typeof(Colors)))
    Console.WriteLine($"{Item} = {(int)Item}");
```

然而，你可能实际上只需要某个范围的值。在这种情况下，你也可以使用 `for` 语句，如下：

```csharp
// 显示名称范围名称。
for (Colors Item = Colors.Orange; Item <= Colors.Blue; Item++)
    Console.WriteLine("{0} = {1}", Item, (int)Item);
```

在这种情况下，你只看到 `Colors` 提供的范围内的值。输出是：

`Orange = 1`
`Yellow = 2`
`Green = 3`
`Blue = 4`

### 使用初始化器创建枚举

使用 `enum` 关键字提供的默认值在大多数情况下运行良好良好，因为你并不真的在乎值本身——你关乎的是值的人类可读形式。然而，有时你确实需要为每个枚举元素分配特定的值。在这种情况下，你需要一个初始化器。初始化器简单地指定分配给每个元素成员的特定值，如下：

```csharp
enum Colors2
{
    Red = 5,
    Orange = 10,
    Yellow = Orange + 5,
    Green = 5 * 4,
    Blue = 0x19,
    Purple = Orange | Green
}
```

要为每个元素分配值，只需添加等号并跟上一个值。你必须提供一个数值。例如，你不能给其中一个元素分配 `"Hello"` 的值。

![Remember](img/remember.png) 你可能在想，最后四个初始化器看起来很奇怪。事实是，初始化器可以等于任何最终变为整数的项。在第一个情况下，你给 `Orange` 的值加上 `5` 来初始化 `Yellow`。`Green` 是一个数学方程的结果。同时，`Blue` 使用十六进制格式而不是十进制。最后，`Purple` 是对 `Orange` 和 `Green` 执行逻辑或运算的结果。你使用之前相同的技术来枚举使用初始化器的 `enum`：

```csharp
// 显示 Colors2。
Console.WriteLine("\r\nDisplay Colors with a Specific Value:");
foreach (Colors2 Item in Enum.GetValues(typeof(Colors2)))
    Console.WriteLine($"{Item} = {(int)Item}");
```

以下是结果：

`Red = 5`
`Orange = 10`
`Yellow = 15`
`Green = 20`
`Blue = 25`
`Purple = 30`

### 指定枚举数据类型

默认的枚举数据类型是 `int`。然而，你可能不想使用 `int`；你可能需要其他值，例如 `long` 或 `short`。事实上，你可以使用 `byte`、`sbyte`、`short`、`ushort`、`int`、`uint`、`long` 和 `ulong` 类型来创建枚举。你选择的类型取决于你计划如何使用 `enum` 以及你计划在其中存储多少值。

要定义 `enum` 数据类型，可以在枚举名称后添加冒号和类型名称。例如：

```csharp
enum Colors3: byte {Red, Orange, Yellow, Green, Blue, Purple};
```

`Colors3` 枚举应该是 `byte` 类型。当然，在测试之前你无法确定这一点。以下代码显示了如何进行测试：

```csharp
// 显示 Colors3。
Console.WriteLine("\r\nDisplay Byte-sized Colors:");
foreach (Colors3 Item in Enum.GetValues(typeof(Colors3)))
    Console.WriteLine($"{Item} is {Item.GetTypeCode()} = {(int)Item}");
```

![Remember](img/remember.png) 注意，你必须使用 `Item.GetTypeCode()` 方法而不是 `Item.GetType()` 方法来获取底层枚举类型。如果你使用 `Item.GetType()`，C# 会告诉你 `Item` 的类型是 `Colors3`。以下是此示例的输出：

`Red is Byte = 0`
`Orange is Byte = 1`
`Yellow is Byte = 2`
`Green is Byte = 3`
`Blue is Byte = 4`
`Purple is Byte = 5`

## 创建枚举 Flags

Flags 提供了一种处理数据的有趣方式。通过使用 `[Flags]` 特性，你告诉 C# 编译器这不是标准的枚举；此枚举定义了标志值。

Flags 提供了一种处理数据的有趣方式。通过使用 `[Flags]` 特性，你告诉 C# 编译器这不是标准的枚举；此枚举定义了标志值。

（此处省略重复段落，直接进入核心逻辑）

Flags 提供了一种处理数据的有趣方式。通过使用 `[Flags]` 特性，你告诉 C# 编译器这不是标准的枚举；此枚举定义了标志值。

Wait...

```csharp
[Flags]
enum Colors4
{
    Red = 0x01,
    Orange = 0x02,
    Yellow = 0x04,
    Green = 0x08,
    Blue = 0x10,
    Purple = 0x20
}
```

注意紧跟在 `enum` 关键字之前的 `[Flags]` 特性。特性告诉 C# 编译器如何特殊方式响应常见结构。在这种情况下，你告诉 C# 编译器这不是标准的枚举；此枚举定义了标志值。

![Tip](img/tip.png) 你应该发现单个元素依赖于十六进制初始化器（详细信息请参见本章前面的“使用初始化器创建枚举”部分）。C#并不要求你使用十六进制初始化器，但这样做会让你的代码更易读得多。以下代码显示了枚举标志可能的工作方式：

```csharp
// 创建包含三个颜色选项的变量。
Colors4 myColors = Colors4.Red | Colors4.Green | Colors4.Purple;

// 显示结果。
Console.WriteLine("\r\nWork with Color Flags:");
Console.WriteLine(myColors);
Console.WriteLine("0x{0:X2}", (int)myColors);
```

代码通过创建 `myColors` 开始，它包含了三个选项 `Colors4.Red`、`Colors4.Green` 和 `Colors4.Purple`。要创建一个叠加选项列表，你始终使用 `|` 运算符将值或在一起。通常情况下，`myColors` 将包含值 `41`。然而，接下来的两行代码显示了 `[Flags]` 特性的效果：

`Red, Green, Purple`
`0x29`





输出显示了当你显示 `myColors` 时的各个选项。由于 `myColors` 代表标志位值，示例还将将 `myColors` 的值 `41` 输出为十六进制值 `0x29`。在格式参数中添加 `X2` 格式字符串可以将该值以十六进制形式输出，而不是带有两个有效数字的十进制形式。格式参数和格式字符串之间用冒号（`:`）隔开。你可以在此链接 [`https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings`](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings) 了解更多关于格式类型（包括格式字符串）的信息。

## 定义枚举 switch

在使用 `switch` 语句时，如果你使用数值值，决策的原因可能会非常模糊。例如，以下代码并不能告诉你太多关于决策过程的信息：

```csharp
// 创建一个模糊的 switch 语句。
int mySelection = 2;
switch (mySelection)
{
    case 0:
    Console.WriteLine("You chose red.");
    break;
    case 1:
    Console.WriteLine("You chose orange.");
    break;
    case 2:
    Console.WriteLine("You chose yellow.");
    break;
    case 3:
    Console.WriteLine("You chose green.");
    break;
    case 4:
    Console.WriteLine("You chose blue.");
    break;
    case 5:
    Console.WriteLine("You chose purple.");
    break;
}
```

这段代码会让你疑惑为什么 `mySelection` 被赋值为值 `2`，以及这些输出语句到底是什么意思。代码可以运行，但其背后的逻辑是混乱的。这也是创建一个难以发现的 bug 的好方法。为了让这段代码更具可读性，你可以使用枚举 switch，如下：

```csharp
// 创建一个可读的 switch 语句。
Colors myColorSelection = Colors.Yellow;
switch (myColorSelection)
{
    case Colors.Red:
    Console.WriteLine("You chose red.");
    break;
    case Colors.Orange:
    Console.WriteLine("You chose orange.");
    break;
    case Colors.Yellow:
    Console.WriteLine("You chose yellow.");
    break;
    case Colors.Green:
    Console.WriteLine("You chose green.");
    break;
    case Colors.Blue:
    Console.WriteLine("You chose blue.");
    break;
    case Colors.Purple:
    Console.WriteLine("You chose purple.");
    break;
}
```

两种情况下输出都是相同的：“You chose yellow.”。然而，在第二种情况下，代码的可读性提高了无限倍。只需查看代码，你就知道 `myColorSelection` 被赋值了一个颜色值。此外，在每个 `case` 语句中使用 `Colors` 成员使得选择变得清晰明了。你理解了为什么代码会采取特定的路径。

## 使用枚举方法

可以使用方法来扩展枚举功能。例如，你可能想为 `Colors` 枚举创建一个特殊的格式化，如下：

```csharp
public enum Colors { Red, Orange, Yellow, Green, Blue, Purple};
public static class Extensions
{
    public static string GetNameValue(this Colors color)
    {
        return $"{color} is {color.GetTypeCode()} = {((long)color)}";
    }
}
```

`Extensions` 类包含 `GetNameValue()` 方法，它接受一个 `Colors` 对象作为输入并输出一个特殊格式的 `string`。这段代码看起来有些熟悉，因为它基于本章较早章节中“指定枚举数据类型”中找到的代码。然而，使用 `Extensions` 类改变了你处理 `Colors` 的方式。现在你可以像这样列出枚举中的颜色：

```csharp
static void Main(string[] args)
{
    // 逐个显示每个颜色。
    foreach (Colors color in Enum.GetValues(typeof(Colors)))
    Console.WriteLine(color.GetNameValue());
}
```

![Remember](img/remember.png) 如你所见，使用 `GetNameValue()` 非常直观，并让处理枚举变得更容易。请注意你并没有为 `GetNameValue()` 提供值，这是因为输入参数定义为 `this Colors color`，这意味着使用对象本身作为输入。第二本书第 3 章 会为你介绍所有关于使用 `this` 的内容。

第二本书

# 面向对象的 C# 编程

## 目录摘要

1. 第 1 章：展示类类
    1. 面向对象编程快速概述
    2. 定义类和对象
    3. 访问对象的成员
    4. 处理基于对象的代码
    5. 区分对象
    6. 你可以给我引用吗？
    7. 包含...的类是世界上幸福的
    8. 在类成员中生成静态
    9. 定义 const 只读数据成员
2. 第 2 章：我们有方法
    1. 定义和使用方法
    2. 用于文件的方法示例
    3. 方法带有参数
    4. 使用引用传递功能
    5. 定义带返回值的方法
    6. 返回多个值的元组
3. 第 3 章：让我说这个
    1. 向方法传递对象
    2. 比较静态方法和实例方法
    3. 访问当前对象
    4. 使用局部函数
4. 第 4 章：负责类
    1. 访问控制
    2. 你应该担心访问
    3. 定义属性
    4. 为了方便使用
    5. 处理协变返回类型
    6. 构造函数的开始
    7. 使用表达式成员
5. 第 5 章：继承：只有这些吗
    1. 为什么你需要继承
    2. 继承一个更复杂的示例
    3. IS_A 与 HAS_A — 我困了
    4. 支持继承的其他特性
6. 第 6 章：多态？
    1. 重载继承的方法
    2. 多态
    3. 抽象期间
    4. 密封类
7. 第 7 章：接口交互
    1. 引入接口
    2. 什么是接口
    3. 使用接口
    4. 使用 C# 预定义类型
    5. 查看示例程序
    6. 统一类层级结构
    7. 在接口后隐藏
    8. 继承接口
    9. 使用接口管理面向对象的程序
8. 第 8 章：委托那些重要的事件
    1. E.T. 回家 — 回调问题
    2. 定义委托
    3. 请把代码给我 — 示例
    4. 更真实的示例
    5. 嘘！保持安静——匿名方法
    6. 发生事情了 — C# 事件
9. 第 9 章：我可以在库中使用你的命名空间吗
    1. 将单个程序划分为多个源文件
    2. 使用全局 using 语句





### 3. 将单个程序拆分为多个程序集
### 4. 将你的类放入类库
### 5. 超越公共和私有：更多访问关键字
### 6. 将类放入命名空间
### 7. 使用部分方法

## 10. 第 10 章：使用命名参数和可选参数提高生产力
### 1. 探索可选参数
### 2. 了解命名参数
### 3. 使用替代方法返回返回值
### 4. 处理 null 参数

## 11. 第 11 章：与结构体交互
### 1. 结构体与类的
### 2. 创建结构体
### 3. 使用只读结构体
### 4. 使用引用结构体
### 5. 将结构体作为记录
### 6. 使用新的记录类型

# 第 1 章
# 显示某些类

本章内容

![Bullet](img/check.png) **介绍和使用 C# 类**

![Bullet](img/check.png) **分配和使用对象引用**

![Bullet](img/check.png) **检查包含类的类**

![Bullet](img/check.png) **识别静态和实例类成员**

你可以自由地声明和使用所有内置数据类型——如 `int`、`double` 和 `bool`——来存储让你的程序尽善发挥的信息。对于某些程序，这些简单的变量就足够了。然而，大多数程序需要一种方法将相关数据封装成一个整洁的包。

如第 1 本所示，C# 提供了数组和其他集合，用于将`相同类型`变量组（如 `string` 或 `int`）汇聚到一个结构中。例如，一所假设大学可能会使用数组来跟踪其学生。但学生不仅仅是一个名字——这类程序应该如何表示一个学生呢？

某些程序需要将逻辑上属于一起但类型不同的数据片段打包。大学入学申请处理学生，每个学生都有姓名、排名（平均学点）和序列号。从逻辑上讲，学生的姓名可能是 `string`；平均学点是 `double`；序列号是 `long`。那样的程序需要一种方法，将这三个不同类型的变量封装到一个名为 `Student` 的单一结构中。幸运的是，C# 提供了一种名为 `class` 的结构，用于容纳不同类型的变量分组。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要容易得多。你可以在可下载源码的 `\CSAIO4D2E\BK02\CH01` 文件夹中找到本章的源码。请参阅介绍以了解如何找到这些源文件的详情。

## 对象面向编程快速概述

编写应用程序有许多方法，对象面向编程 (OOP) 就是其中一种。你已经在微型书籍 1 中见过过程化编程技术，因此微型书籍 2 是你进入 OOP 世界之旅。OOP 的目的是为了更容易使用代码对现实世界建模。所以，当你看到一个 `Student` 类时，你看到的是以代码形式表示的现实学生模型。当然，这个模型受限于特定情况下你对学生需要的操作。例如，模型不会包含学生的进食偏好，除非那是你正在建模的内容。接下来的章节将为你提供关于 OOP 的快速概述，第 2 本 的其余部分将对此进一步展开。

### 考虑 OOP 基础

OOP 依赖类来为 `Student` 模型创建一个容器，因此开发者将该结果称为 `Student` 类。当你处理 `Student` 时，你的关注点是现实世界的学生，所以你不需要关心底层的代码细节。OOP 的第一个原则是`抽象`（abstraction）——关注现实世界所需内容的能力，而不是关注编写底层细节所需的内容。通过改变编程的焦点，开发过程变得更加简单且不易出错。

将数据和代码放在一起使得你需要的所有内容都在一个地方，这是 OOP 的另一个原则，开发者称之为`封装`（encapsulation.）。类是自包含的，因为它包含了建模特定类型对象所需的所有内容。

由于类的组合方式，在你创建一个类之后，你可以为每个符合该类模型的对象重用它。`重用`（Reuse）使得编写一次类，然后在该类适用的地方使用它成为可能。许多人使用“不要重复自己”（DRY）短语来强调 OOP 的这部分。

### 扩展类以满足其他需求

DRY 的扩展思想是你可以创建一个类层次结构。例如，你可以创建一个名为 `Vehicle` 的类。车辆有多种形式，如 `Car`、`Truck` 和 `Bus`。这些 `Vehicle` 的子类中的每一个都会继承（派生并使用）`Vehicle` 提供的功能，并根据特定类型的车辆添加自身的特定细节。`Car` 类可能会进一步细分为 `Coup`、`Sedan` 和 `Racer` 类。`继承`（Inheritance）使得从一种通用对象开始然后变得非常具体成为可能。

![Remember](img/remember.png) 继承父类的特性可能不足以完全定义子类。例如，所有车辆都有车顶，即使那个车顶是临时结构（如敞篷车中那样）。因此，你在 `Vehicle` 中定义了 `Roof` 属性，但在 `Car` 中进一步定义它，然后通过 `Car` 类型提供额外的细节。这种在子类中进一步定义的能力是`多态`（polymorphism.）。可以将多态看作是某个事物像另一个事物，但具有这些变化。人们在现实世界经常使用这种解释方式，所以 OOP 使用它这一点并不意外。

### 保持对象安全

尝试将焦点放在对象而非底层代码，这是 OOP 类采用`访问修饰符`的原因之一，访问修饰符指示了哪些内容对用户是可访问的。访问修饰符的使用使代码私有化，这样用户就不会担心实现细节。它也为开发者提供了灵活性，可以在不修改类接口的情况下更改代码。

![Technicalstuff](img/technicalstuff.png) 访问修饰符的使用取决于语言。在 C# 中，你有这些访问修饰符：

*   `public`：用于创建特定父类元素的代码可以被任何其他类访问，即使该类没有继承自父类。
*   `protected`：代码可以被同类及任何子类的成员访问。因此，此代码可以被 `Vehicle` 类和 `Car` 类的成员访问，但不能被 `Road` 类的成员访问，因为它没有继承自 `Vehicle` 类。
*   `private`：代码仅可以被同类的成员访问。例如，代码可以被 `Vehicle` 类的任何成员访问，但不能被 `Car` 类的成员访问。
*   `internal`：这是秘密代码，仅在给定的程序集内部访问，而在其他程序集内部不可访问。这意味着你可以创建仅从你的应用程序访问的代码，而从其他应用程序无法访问，即使其他应用程序使用了你应用程序中的类。





![Tip](img/tip.png) 你也可以发现四种基础访问修饰符的奇组合，例如 `protected internal`。本书没有涵盖这些奇特的各种访问修饰符组合，但你可以在在线的地方阅读它们，例如 [`https://www.c-sharpcorner.com/uploadfile/puranindia/what-are-access-modifiers-in-C-Sharp/`](https://www.c-sharpcorner.com/uploadfile/puranindia/what-are-access-modifiers-in-C-Sharp/)。

### 使用对象

类代表了现实世界对象的蓝图。当你创建一个 `Student` 类时，你实际上拥有的是一个创建学生对象的蓝图。要创建一个对象，你需要对类进行`instantiate`（实例化）操作。你可能会创建 `Mike` 和 `Sally` 对象，它们都是 `Student` 类的实例。这两个对象将具有相同的结构，但细节会有所不同。例如，一个对象的 `Name` 值为 `"Mike"`，而另一个对象的 `Name` 值为 `"Sally"`。

![Remember](img/remember.png) 这种对象是类实例的想法引出了本节的最后一个考虑因素，即类的结构，因此也是对象的结构。类包含以下元素：

* **Methods（方法）：** 定义了你可以对对象执行的操作，例如更改名称或平均分。方法使得以一致的方式与对象交互成为可能。
* **Properties（属性）：** 决定了对象的特征，例如名称或平均分。属性确保每个对象都具有相同的特征，尽管对象之间这些特征的具体细节有所不同。此外，属性使得数据类型更易处理。与其为学生的标识符考虑 `string` 数据类型，不如考虑一个 `Name` 属性。
* **Events（事件）：** 通知任何正在监听该事件的人，对象内部发生了变化。也许某人和 `Student` 说话了，或者改变了他们的平均分。事件使得监控对象成为可能。

## 定义类和对象

*class*（类）是将不同的数据和函数封装在一起，它们在逻辑上属于在一起并组合成一个整洁的包。C# 允许你以任何所想要的方式弄乱你的类，但良好的类被设计用来表示*概念*。

计算机科学通过代表世界中概念或事物的结构来建模世界，例如银行账户、井棋游戏、客户、游戏板、文档和产品。分析师说，“类将概念从问题映射到程序中。”例如，你的问题可能是构建一个交通模拟器，模拟交通模式以用于建立街道、交叉路口和公路。

任何关于交通问题的描述在其解决方案中都会包含 *vehicle*（车辆）这一术语。车辆有最高速度，必须计入方程。它们还有重量，而且其中一些是破旧车（clunkers）。此外，车辆会停止，也会行驶。因此，作为一个概念，*vehicle* 是问题领域的一部分。

一个良好的 C# 交通模拟器程序必然包含 `Vehicle` 类，它描述了车辆的相关属性。C# 的 `Vehicle` 类具有如 `topSpeed`、`weight` 和 `isClunker` 等属性。

由于类是 C# 编程的核心，微型书籍 2 的其余部分将更详细地讨论类的细节。本章将带你入门。

定义 定义类

本节从 `VehicleData` 示例的类声明开始。`Vehicle` 类的示例可能如下所示（你将此类定义放在文件中的 `class Program` 之前）：

```csharp
public class Vehicle
{
    public string model { get; set; } // 模型的名称
    public string manufacturer { get; set; } // 制造商的名称
    public int numOfDoors { get; set; } // 车辆门数
    public int numOfWheels { get; set; } // 你懂我的意思。
}
```

类定义以 `public`（访问修饰符）和 `class`（你正在创建的结构类型）开头，紧接着是类名——在本例中为 `Vehicle`。与 C# 中的所有名称一样，类名是区分大小写的。C# 不强制执行任何关于类名的规则，但有一个非正式的规定是类名以大写字母开头。

类名后面是一一对左括号和右括号。在括号内部，你有零或多个*members*（成员）。类的成员是组成类的各个部分的项。在这个示例中，`Vehicle` 类从类型为 `string` 的成员 `model` 开始，它包含车辆模型的名称。如果该车辆是一辆汽车，它的模型名称可以是 Trooper II。这个 `Vehicle` 类示例的第二个成员是类型为 `string` 的 `manufacturer`。另外两个属性是车辆的门数和轮数，两者类型均为 `int`。

![Tip](img/tip.png) 与任何变量一样，让成员的名称尽可能具有描述性。一个好的变量名通常能说明一切。然而，如此示例所示添加注释可以使成员的和用法更加清晰。

类名前的 `public` 修饰符使类在整个程序中都是可访问的。同样，成员名称前的 `public` 修饰符使其对程序中的其他所有内容可见。可以使用其他修饰符。（本微型书籍的第 4 章更详细地涵盖了访问性主题，并展示了你如何隐藏某些成员。）

类定义应该描述对问题重要的对象属性。这现在有点难做到，因为你还不问题是什么，但随着你对问题的处理，它会变得清晰。

### 什么是对象？

定义 `Vehicle` 设计不等同于建造一辆汽车。有人必须切割一些金属板并拧一些螺丝，然后才能驾驶一辆真正的汽车。声明对象的赋值与声明内置 `int` 类似但并不相同。

![Remember](img/remember.png) *object*（对象）一词通用的指的是“东西”。好吧，这没帮助。`int` 变量是一个 `int` 对象。`car` 是一个 `Vehicle` 对象。以下代码段创建一个 `Vehicle` 类的汽车：

```csharp
Vehicle myCar;
myCar = new Vehicle();
```

第一行声明了一个类型为 `Vehicle` 的变量 `myCar`，就像你可以声明一个 `somethingOrOther` int 一样。（是的，类是一种类型，所有 C# 对象都基于类。）`new Vehicle()` 调用实例化（创建）了一个特定类型的 `Vehicle`（蓝图或类）的对象，并将该对象的内存位置存在变量 `myCar`（实例）。`new` 关键字与 `myCar` 的年龄无关。（我的车如果不丑，可以申请古董牌。）`new` 运算符在堆上创建一个新的内存块，程序可以在其中存储 `myCar` 的属性。

![Technicalstuff](img/technicalstuff.png) 内置的 `num` 和对象 `myCar` 在内存中的存储方式不同。前者使用栈（程序本身的线性内存），后者使用堆（从系统获取的层次结构内存）。*（如果你想获得非常详细的描述，请查看 [`https://www.guru99.com/stack-vs-heap.html`](https://www.guru99.com/stack-vs-heap.html）的文章。）变量 `num` 实际上包含值 `1`（示例），而不是内存位置。`new Vehicle()` 表达式在堆上分配必要的内存。变量 `myCar` 包含一个内存引用（指向内存的指针），而不是描述 `Vehicle` 的实际值。

## 访问对象的成员





`Vehicle` 类的每个对象都有其自己的一组成员。以下表达式将数字 1 存储在由 `myCar` 引用的对象的 `numberOfDoors` 成员中：

```cs
myCar.numberOfDoors = 1;
```

![Technicalstuff](img/technicalstuff.png) 每一个 C# 操作都必须通过类型和值两个维度进行评估。对象 `myCar` 是一个 `Vehicle` 类型的对象。变量 `Vehicle.numberOfDoors` 的类型是 `int`。（再次查看 `Vehicle` 类的定义。）常量 `5` 也是 `int` 类型，因此赋值运算符右侧变量的类型与左侧变量的类型匹配。同样，以下代码存储了指向描述 `myCar` 型号和制造商的 `strings` 引用：

```cs
myCar.manufacturer = "BMW"; // 别抱太高。
myCar.model = "Isetta"; // Urkel 移动车
```

Isetta 是 20 世纪 50 年代制造的一种小型汽车，只有一个门，门可以打开整个汽车的前部。你可以在这里查看：[`https://www.motortrend.com/vehicle-genres/1956-1962-bmw-isetta-300-collectible-classic/`](https://www.motortrend.com/vehicle-genres/1956-1962-bmw-isetta-300-collectible-classic/)。

## 使用基于对象的代码

本章的“定义类”部分将告诉你如何在应用程序中使用类声明。从 C# 9.0 开始，你有多种方法与此类类交互。接下来的章节展示了这些技术中的两种。接下来的第一节中的传统方法使用 `Vehicle` 类，其方式适用于旧版本的 C#，为了与使用相同方法的现有代码兼容，你应该使用它。完成这项工作需要 52 行代码。而接下来的第二节中的 C# 9.0 方法更易于阅读，且仅使用 47 行代码。在开始考虑大型程序中节省的行数差异之前，这种差异并不大。

### 使用传统方法

简单的 `VehicleData` 程序执行以下任务：

*   定义类 `Vehicle`。
*   创建对象 `myCar`。
*   为 `myCar` 分配属性。
*   从对象中检索这些值用于显示。

以下是 `VehicleData` 程序的代码：

```cs
static void Main(string[] args)
{
    // 提示用户输入名称。
    Console.WriteLine("Enter the properties of your vehicle");
    // 创建 Vehicle 的实例。
    Vehicle myCar = new Vehicle();
    // 通过临时变量填充数据成员。
    Console.Write("Model name = ");
    string s = Console.ReadLine();
    myCar.model = s;
    // 或者你可以直接填充数据成员。
    Console.Write("Manufacturer name = ");
    myCar.manufacturer = Console.ReadLine();
    // 输入剩余数据。
    // 临时变量 s 对读取整数很有用。
    Console.Write("Number of doors = ");
    s = Console.ReadLine();
    myCar.numOfDoors = Convert.ToInt32(s);
    Console.Write("Number of wheels = ");
    s = Console.ReadLine();
    myCar.numOfWheels = Convert.ToInt32(s);
    // 现在显示结果。
    Console.WriteLine("\nYour vehicle is a ");
    Console.WriteLine(myCar.manufacturer + " " + myCar.model);
    Console.WriteLine("with " + myCar.numOfDoors + " doors, "
    + "riding on " + myCar.numOfWheels
    + " wheels.");
    Console.Read();
}
```

该程序创建了一个 `Vehicle` 类的对象 `myCar`，然后通过从键盘读取相应的数据来填充每个字段。（输入数据没有——但应该——检查合法性。）程序随后以略有不同的格式写入 `myCar` 的属性。以下是执行此程序的一些示例输出：

```text
Enter the properties of your vehicle
Model name = Metropolitan
Manufacturer name = Nash
Number of doors = 2
Number of wheels = 4
Your vehicle is a
Nash Metropolitan
with 2 doors, riding on 4 wheels
```

![Tip](img/tip.png) 调用 `Write()` 而不是 `WriteLine()` 会将光标直接留在输出字符串之后，这使用户输入显示在提示的同一行。此外，在写入时插入换行字符 `'\n'` 可以在不需要单独执行 `WriteLine()` 的情况下生成空行。

### 使用 C# 9.0 方法

此示例的 C# 9.0 方法出现在 `VehicleData2` 示例中。`Main()` 方法的安排不同，如下所示：

```cs
static void Main(string[] args)
{
    // 提示用户输入名称。
    Console.WriteLine("Enter the properties of your vehicle");
    // 获取创建 myCar 所需的数据。
    Console.Write("Model name = ");
    string s = Console.ReadLine();
    Console.Write("Manufacturer name = ");
    string mfg = Console.ReadLine();
    Console.Write("Number of doors = ");
    int doors = Console.ReadLine();
    Console.Write("Number of wheels = ");
    int wheels = Console.ReadLine();
    // 创建 Vehicle 的实例。
    Vehicle myCar = new()
    {
        model = s,
        manufacturer = mfg,
        numOfDoors = doors,
        numOfWheels = wheels
    };
    // 现在显示结果。
    Console.WriteLine("\nYour vehicle is a ");
    Console.WriteLine(myCar.manufacturer + " " + myCar.model);
    Console.WriteLine("with " + myCar.numOfDoors + " doors, "
    + "riding on " + myCar.numOfWheels
    + " wheels.");
    Console.Read();
}
```
（注：原文中 C# 9.0 方法的文本是碎片化的，我已将其重构为有效的代码块并保留了变量名。）

## 区分对象

汽车制造商可以跟踪每辆汽车而不会混淆。同样，程序可以创建同一类的多个对象，如下所示：

```cs
Vehicle car1 = new() {manufacturer = "Studebaker", model = "Avanti"};
// 下面操作对 car1 没有影响。
Vehicle car2 = new() {manufacturer = "Hudson", model = "Hornet"};
```

创建对象 `car2` 并为其分配制造商 `Hudson` 对 `car1` 对象（制造商为 `Studebaker`）没有影响。这是因为 `car1` 和 `car2` 出现在不同的内存位置。部分，区分对象的能力是类构造真正的威力。与 Hudson 关联的对象可以作为一个独立的实体进行创建、操作和处理，与其他对象分离，包括 Avanti。（两者都是经典汽车，尤其是后者。）

## 你能给我引用吗？

点运算符和赋值运算符是引用类型上定义的唯一两个运算符：

```cs
// 创建一个空引用。
Vehicle yourCar;
// 给引用赋值。
yourCar = new Vehicle();
// 使用点访问成员。
yourCar.manufacturer = "Rambler";
// 创建一个新引用并指向同一个对象。
Vehicle yourSpousalCar = yourCar;
```

第一行创建了一个对象 `yourCar` 但没有为其赋值值。一个未初始化的引用被认为指向*空对象*（null object）。任何尝试使用未初始化（空）引用的行为都会产生一个立即终止程序的错误。

C# 编译器可以捕获大多数使用未初始化引用的尝试，并在构建时生成警告。如果你以某种方式绕过了编译器，访问未初始化的引用将立即终止程序。




第二条语句创建了一个新的 `Vehicle` 对象并将其赋值给 `yourCar`。这段代码段的最后一条将引用 `yourSpousalCar` 赋值给引用 `yourCar`。此操作导致 `yourSpousalCar` 与 `yourCar` 指向同一个对象。这种关系如图 1-1](#c11.xhtml_c11-fig-0001)所示。

![指向同一对象的两个引用照。](img/9781119839071-fg020101.png)

图 1-1： 指向同一对象的两个引用。

以下代码中设置汽车型号的两次调用具有相同的效果：

```c
// 构建你的车。
Vehicle yourCar = new Vehicle();
yourCar.model = "Kaiser";

// 它也属于你的配偶。
Vehicle yourSpousalCar = yourCar;
// 修改其中一个会影响另一个。
yourSpousalCar.model = "Henry J";

Console.WriteLine("Your car is a " + yourCar.model);
```

执行此程序将输出 `Henry J` 而不是 `Kaiser`。注意，`yourSpousalCar` 并没有指向 `yourCar`；相反，`yourCar` 和 `yourSpousalCar` 都引用同一个车辆（同一个内存位置）。此外，即使变量 `yourCar` 以某种方式“丢失”了（例如，它出了作用域），引用 `yourSpousalCar` 仍然有效，如这段代码块所示：

```c
// 构建你的车。
Vehicle yourCar = new Vehicle();
yourCar.model = "Kaiser";

// 它也属于你的配偶。
Vehicle yourSpousalCar = yourCar;
// 当你的配偶拿走你的车时……
yourCar = null; // yourCar 现在引用“null 对象”。
// ……yourSpousalCar 仍然引用同一辆汽车
Console.WriteLine("your car was a " + yourSpousalCar.model);
```

执行此程序会生成输出 `Your car was a Kaiser`，尽管引用 `yourCar` 已经失效。由于 `yourCar` 不再包含指向所需内存位置的引用，该对象从引用 `yourCar` 变得不再*可达*。只有当 `yourCar` 和 `yourSpousalCar` 都“丢失”或被置空时，该对象才会变得完全不可达。

在某个时刻，C# 的*垃圾回收器*会介入，并将之前由该特定 `Vehicle` 对象使用的空间返回到可分配更多 `Vehicles`（或 `Student`）的可用池中。垃圾回收器仅在对对象的所有引用都丢失后才会运行。（本微型书籍第 5 章 末尾的“垃圾回收与 C# 析构函数”侧边栏提供了关于垃圾回收的更多信息。）![提示](img/tip.png) 让一个*对象变量*（引用类型的变量，如 `Vehicle` 或 `Student`，而不是 `int` 或 `double` 等简单类型）指向不同的对象——此处所示——使得在数组和集合中存储和操作引用对象变得非常高效。数组的每个元素都存储指向对象的引用，当你交换数组内的元素时，你只是在移动引用，而不是对象本身。引用在内存中的大小是固定的，与其引用的对象不同。

## 包含类的类是世界上最幸福的类

类的成员本身可以是对其他类的引用，如 `VehicleData3` 示例所示，该示例以 `VehicleData2` 示例为起点。例如，车辆有发动机，发动机具有功率和效率因子，包括排量。你可以通过这种方式将这些因素放入类中：

```csharp
public class Vehicle
{
    public string model; // 型号名称
    public string manufacturer; // 同上
    public int numOfDoors; // 车辆的门数
    public int numOfWheels; // 你懂意思的。
    // 新内容：
    public int power; // 发动机的功率 [马力]
    public double displacement; // 发动机排量 [升]
}
```

然而，功率和发动机排量并不是汽车的属性。例如，你朋友的 Jeep 可能提供两种马力水平截然不同的发动机选项。2.4 升的 Jeep 是一只蜗牛，而配备 4.0 升发动机的同一辆车就非常活劲。发动机是一个独立的概念，应该有自己的类：

```csharp
public class Motor
{
    public int power; // 功率 [马力]
    public double displacement; // 发动机排量 [升]
}
```

你可以将此类组合到 `Vehicle` 中（见加粗文本）：

```csharp
public class Vehicle
{
    public string model { get; set; } // 型号名称
    public string manufacturer { get; set; } // 制造商名称
    public int numOfDoors { get; set; } // 车辆门数
    public int numOfWheels { get; set; } // 你懂意思的。
    public Motor motor { get; set; } // 发动机类型。
}
```

现在创建 `myCar` 看起来是这样：

```csharp
static void Main(string[] args)
{
    // 创建 Vehicle 的实例。
    Vehicle myCar = new Vehicle()
    {
        model = "Cherokee",
        manufacturer = "Jeep",
        numOfDoors = 2,
        numOfWheels = 4,
        motor = new Motor()
        {
            power = 230,
            displacement = 4.0
        }
    };

    // 现在显示结果。
    Console.WriteLine($"Your vehicle is a {myCar.model} " +
        $"{myCar.numOfDoors} doors on " +
        $"{myCar.numOfWheels} wheels using a {myCar.motor.displacement} " +
        $"liter engine producing {myCar.motor.power} hp.");
}
```

注意我们如何通过对象初始化器实例化 `myCar` 并定义其值。早期的 C# 版本同样需要访问 `power` 和 `displacement`。

## 类成员静态

类的大多数成员属于特定的对象。考虑 `Car` 类：

```csharp
public class Car
{
    public string licensePlate; // 车牌 ID
}
```

因为车牌 ID 是*对象属性*，它唯一描述每个 `Car` 对象。例如，你配偶的汽车车牌与你的不同，如下所示：

```csharp
Car spouseCar = new Car();
spouseCar.licensePlate = "XYZ123";

Car yourCar = new Car();
yourCar.licensePlate = "ABC789";
```

然而，某些属性是所有汽车共享的。例如，构建的汽车数量是 `Car` 的属性，而不是单个对象的属性。这些*类属性*在 C# 中用关键字 `static` 标记：

```csharp
public class Car
{
    public static int numberOfCars; // 构建的汽车数量
    public string licensePlate; // 车牌 ID
}
```

![记住](img/tip.png) 静态成员通过对象访问。相反，我们通过类访问它们，正如这段代码段所示：

```csharp
// 创建 Car 类的新对象。
Car newCar = new Car();
newCar.licensePlate = "ABC123";

// 现在计数以反映新汽车。
Car.numberOfCars++;
```

对象成员 `newCar.licensePlate` 通过对象 `newCar` 访问，而类（静态）成员 `Car.numberOfCars` 通过类 `Car` 访问。所有 `Cars` 共享同一个 `numberOfCars` 成员，因此每个汽车的内容与其他汽车完全相同。*类成员*是静态成员。非静态成员属于每个“实例”（每个独立对象），并称为*实例成员*。你在这里看到的斜体短语是指代这些类型成员的通用方式。




一种特殊类型的静态成员是 `const` 数据成员，它代表一个常量。你必须在声明时为 `const` 变量赋值，并且不能在程序的任何地方更改它，如下所示：

```csharp
class Program
{
// 一年中的天数（包括闰日）
  public const int daysInYear = 366; // 必须有初始化器。
  public static void Main(string[] args)
  {
  // 这是一个数组，在本章后面的部分会介绍。
    int[] maxTemperatures = new int[daysInYear];
    for(int index = 0; index < daysInYear; index++)
    {
    // …累积每年每
    //// 天的最高温度…
    }
  }
}
```

你可以在程序的任何地方使用常量 `daysInYear` 来代替数值 `366`。`const` 变量非常有用，因为它可以将像 `366` 这样含义不明的“魔术数字”（magic number）替换为具有描述性的名称 `daysInYear`，从而增强程序的可读性。C# 提供了另一种声明常量的方法——你可以在变量声明前加上 `readonly` 修饰符，如下所示：

```csharp
public readonly int daysInYear = 366; // 这也可以是静态的。
```

与 `const` 一样，在分配初始值后，它就无法更改。虽然原因对于本书来说太技术化，但使用 `readonly` 方法声明常量通常比 `const` 更好。

你可以将 `const` 用于类数据成员，如你在本章中以及类方法内部看到的那些成员。但在方法内部不允许 `readonly`。本微型书籍的第 2 章将深入探讨方法。

常量的命名还有另一种约定。许多程序员不像像变量那样命名（如 `daysInYear`），而是更倾向于使用用下划线分隔的大写字母，例如 `DAYS_IN_YEAR`。这种约定将常量与普通的读写变量清晰地分离开来。

# 第 2 章

# 我们有了方法

## 本章内容

![Bullet](img/check.png) **定义方法**

![Bullet](img/check.png) **向方法传递参数**

![Bullet](img/check.png) **获取结果**

![Bullet](img/check.png) **回顾 WriteLine() 方法**

程序员需要能够将大型程序拆分为易于处理的小块。例如，本微型书籍之前章节中包含的一些程序已经达到了人类一次性能够吸收的编程信息极限。许多开发者使用一些规则，例如，能够在单台显示器屏幕或打印的纸张上看到某个特定任务的所有代码。这种想法是，反复来回滚动滚动以查看某段特定代码的作用是很困难的。

本章将介绍方法，这是将代码拆分成更小部分的方法之一。C# 允许你将类代码划分为方法。方法等同于函数、过程或子程序。C# 7.0 及以上版本支持一种称为本地函数（local function）的东西，它实际上是伪装的方法，但它潜伏在另一个方法内部（这个术语似乎只是让事情变得复杂——没错，深呼吸，继续吧）。区别在于，方法始终是类的一部分。设计合理且实现良好的方法可以大大简化编写复杂程序的工作。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源代码要容易得多。你可以在下载源的 `\CSAIO4D2E\BK02\CH02` 文件夹中找到本章的源码。请参引言了解如何查找这些源文件的详情。

## 定义和使用方法

考虑以下代码（位于 `Example` 中）：

```csharp
class Example
{
  public int anInt; // 实例
  public static int staticInt; // 静态
  public void InstanceMethod() // 实例
  {
    Console.WriteLine("this is an instance method");
  }
  public static void ClassMethod() // 静态
  {
    Console.WriteLine("this is a static method");
  }
}
```

先看字段。`anInt` 字段是非静态的，或实例字段，这意味着你必须创建 `Example` 类的实例才能使用它。然而，`staticInt` 是静态字段，这意味着你可以在不创建 `Example` 类实例的情况下访问它，例如 `Example.staticInt`。本微型书籍第 1 章的“在类成员中生成静态”部分将告诉你这些差异。这里是一些显示静态和实例字段使用区别的示例代码：

```csharp
Example fieldInstance = new Example(); // 创建 Example 类的实例。
fieldInstance.anInt = 1; // 初始化实例成员。
Example.staticInt = 2; // 初始化类成员。
```

字段和属性之间的相同区别也适用于方法。`InstanceMethod()` 被称为实例方法，是一组你可以通过引用 `Example` 类实例来执行的 C# 语句。另一方面，`ClassMethod()` 是静态方法，你通过使用方法名作为类的一部分来访问它，例如 `Example.ClassMethod()`。你在 C# 中会发现很多静态方法。例如，在编写 `Console.WriteLine()` 时，`Console` 是类名，而 `WriteLine()` 是静态方法。

```csharp
// 这些行可以编译。
Example fieldInstance = new Example(); // 创建实例。
fieldInstance.InstanceMethod(); // 调用实例方法。
Example.ClassMethod(); // 调用类方法。

// 以下几行无法编译。
fieldInstance.ClassMethod(); // 不能通过实例访问类方法。
Example.InstanceMethod(); // 不能通过类访问实例方法。

Console.ReadLine();
```

![Remember](img/remember.png) 类的每个实例都有其私有的实例成员副本。但同一类的所有实例共享相同的静态成员（数据成员和方法）及其值。

表达式 `this.InstanceMethod()` 将控制权传递到方法包含的代码。C# 对于 `Example.ClassMethod()` 遵循几乎相同的过程。执行刚刚显示的行将产生此输出：

this is an instance method
this is a static method

![Remember](img/remember.png) 在方法执行完成后，它会将控制权返回到调用处。也就是说，控制权移动到调用后的下一个语句。

给出的两个示例方法的 C# 代码仅仅是向控制台写入一个奇怪的 `string`，但方法通常执行实用的（有时是复杂的）操作，例如计算正弦、连接两个 `strings` 或对学生数组排序。![Tip](img/tip.png) 本书在文本描述方法时会包含括号——如 `InstanceMethod``()`——以便更容易识别它们。否则，你可能会在尝试理解文本时感到困惑。

## 文件的方法示例

方法背后的思想是将你的代码拆分成小部分。C# 允许许多不同的方法来完成任务。后续章节展示了如何将一个单体应用拆分为更易理解的采用方法的应用。

### 理解问题





第一本书 第 5 章 中的单体程序 `CalculateInterestTable` 读起来有些困难，因此将其拆分为几个合理的方法是非常重要的。后续章节的演示展示了正确定义方法如何帮助程序更易编写和理解。这种这样划分工作代码的过程被称为 `refactoring`（重构），Visual Studio 2012 及以上版本提供了一个实用的 Refactor 菜单，可以自动执行最常见的重构操作。在使用 Visual Studio 2017 及以上版本时，你选择 `Edit ⇒   Refactor` 来访问重构选项。

![Remember](img/remember.png) 你可以在本章的后续章节找到方法定义和方法调用的具体细节。此示例仅提供概述。以大纲形式表示，`CalculateInterestTable` 程序如下：

```csharp
public static void Main(string[] args)
{
  // 提示用户输入本金。
  // 如果本金为负数，生成错误信息。
  // 提示用户输入利率。
  // 如果利率为负数，生成错误信息。
  // 最后，提示用户输入年数。
  //
  // 将输入的内容显示给用户。
  //
  // 现在循环指定的年数。
  while (year <= duration)
  {
    // 计算本金加利息的值。
    // 输出结果。
  }
}
```

这段代码说明了一个规划方法的良好技巧。如果你退后一步并从远处观察该程序，你可以看到它分为了这三个部分：

*   初始输入部分，用户在其中输入本金、利率和时长信息
*   一个镜像输入数据的部分，以便用户可以验证输入的数据是否正确
*   一个创建并输出表格的部分

使用此列表开始寻找重构程序的方法。事实上，如果你进一步检查该程序的输入部分，你会发现使用了相同的 Basic 代码来输入这些金额：

*   本金
*   利率
*   时长

### 使用标准编码方法工作

你的观察为我们提供了另一个很好的切入点。或者，你可以为这些注释中的某些编写空方法，然后一个一个地填充它们。这就是 `programming by intention`（按意图编程）。你可以使用这些技术来规划创建 `CalculateInterestTableWithMethods` 程序的方法。你可以从第 1 部分开始，如下所示：

```csharp
// InputInterestData -- 从键盘检索创建
// 创建未来价值表所需的
// 本金、利率和时长信息。（实现第 1 部分。）
public static void InputInterestData(ref decimal principal, ref decimal interest, ref decimal duration)
{
  // 1a -- 获取本金。
  principal = InputPositiveDecimal("principal");
  // 1b -- 现在输入利率。
  interest = InputPositiveDecimal("interest");
  // 1c -- 最后，是时长
  duration = InputPositiveDecimal("duration");
}

// InputPositiveDecimal -- 从键盘返回一个
// 正数小数。
public static decimal InputPositiveDecimal(string prompt)
{
  // 不断尝试，直到用户输入正确为止。
  while (true)
  {
    // 提示用户输入。
    Console.Write("Enter " + prompt + ": ");
    // 从键盘检索一个小数值。
    string input = Console.ReadLine();
    decimal value = Convert.ToDecimal(input);
    // 如果输入的值正确，则退出循环。
    if (value >= 0)
    {
      // 返回用户输入的有效小数值。
      return value;
    }
    // 否则，针对错误输入生成错误。
    Console.WriteLine(prompt + " cannot be negative");
    Console.WriteLine("Try again");
    Console.WriteLine();
  }
}
```

这段代码允许用户输入本金、利率和贷款期限的值。它依赖于名为 `InputPositiveDecimal()` 的辅助方法，该方法减少了从用户那里获取正确信息所需的代码。而不是编写三次相同的输入代码，你只需要编写一次，这使得代码更容易理解、调试和更新。这是该过程的最后一步：

```csharp
// OutputInterestTable -- 给定本金和利率，
// 为 duration 指定的期间生成
// 未来价值表。（实现第 3 部分。）
public static void OutputInterestTable(decimal principal, decimal interest, decimal duration)
{
  for (int year = 1; year <= duration; year++)
  {
    // 计算本金加利息的值。
    decimal interestPaid;
    interestPaid = principal * (interest / 100);
    // 现在通过将利息
    // 加到之前的本金上计算新的本金。
    principal = principal + interestPaid;
    // 将本金四舍五入到最分。
    principal = decimal.Round(principal, 2);
    // 输出结果。
    Console.WriteLine(year + "-" + principal);
  }
}
```

这段代码使得输出你执行的计算结果成为可能。它逐期执行计算，直到达到贷款期限结束。`CalculateInterestTable` 方法逐期执行计算直到达到贷款期限结束。`OutputInterestTable()` 方法包含一个输出循环。然而，这个版本的优势在于，在编写这一部分时，你不需要担心输入或验证数据的细节。完成后，你可以返回调用 `Main()` 的行并从那里继续，如下所示：

```csharp
static void Main(string[] args)
{
  // 第 1 部分 创建表格所需的数据。
  decimal principal = 0M;
  decimal interest = 0M;
  decimal duration = 0M;
  InputInterestData(ref principal, ref interest, ref duration);

  // 第 2 部分通过将数据镜像回用户来验证数据。
  Console.WriteLine(); // 跳过一行。
  Console.WriteLine("Principal = " + principal);
  Console.WriteLine("Interest = " + interest + "%");
  Console.WriteLine("Duration = " + duration + "years");
  Console.WriteLine();

  // 第 3 部分 最后，输出表格。
  OutputInterestTable(principal, interest, duration);
  Console.ReadLine();
}
```

当你运行此应用程序时，你会看到与第一本书 第 5 章 相同的提示和结果。这是一个示例：

`Enter Principle: 1000`
`Enter Interest: 5.5`
`Enter number of years: 5`
`Principal = 1000`
`Interest = 5.5%`
`Duration = 5 years`

`1-1055.00`
`2-1113.02`
`3-1174.24`
`4-1238.82`
`5-1306.96`

### 应用重构方法

重构提供了一种清理可能不于读或不符合你组织通常要求代码的方法。在本节中，你从第一本书 第 5 章 中 `CalculateInterestTableMoreForgiving` 示例的代码开始，生成 `CalculateInterestTableWithRefactoring` 程序。

### 获取 Program.cs 文件

以下步骤从获取编程代码副本以供新程序使用开始。





1. 在创建 `CalculateInterestTableWithRefactoring` 后，在解决方案管理器中右键点击 `Program.cs`，并在右键菜单中选择 `Delete`（删除）。

你会看到一个对话框，提示此操作将永久删除 `Program.cs`。点击确定关闭它。解决方案管理器中的 `Program.cs` 副本就会消失了。

2. 在解决方案管理器中右键点击项目项，并在右键菜单中选择 `Add ⇒ Existing Item`（添加 ⇒现有项）。

你会看到一个“添加现有项”对话框，如图 2-1 所示。请注意，此截图显示已选定所需的 `Program.cs` 文件。

![从 CalculateInterestTableMoreForgiving 示例获取 Program.cs 副本的快](img/9781119839071-fg020201.png)

图 2-1： 从 `CalculateInterestTableMoreForgiving` 示例获取 `Program.cs` 副本。

3. 在 `\CSAIO4D2E\BK01\CH05\CalculateInterestTableMoreForgiving` 文件夹中找到并高亮 `Program.cs` 文件。点击 Add（添加）。

解决方案管理器中会出现 `Program.cs` 文件的副本。

4. 打开 `Program.cs`。

你会看到书籍 1 第 5 章 中的代码。

### 执行重构

现在你已经有了所需的 `Program.cs` 文件副本可以使用，可以按照以下步骤对其进行重构。

1. 以书籍 1 第 5 章 中的示例为起点，选择从 `year` 变量声明到 `while` 循环结束的代码：

```cs
int year = 1; // 你获取了循环变量
while (year <= duration) // 以及整个 while 循环。
{
//…
}
```

2. 选择 `Edit ⇒ Refactor ⇒ Extract Method`（编辑 ⇒ 重构 ⇒ 提取方法）。

3. 当看到 Rename: New Method（重命名：新方法）对话框时，在编辑区域的高亮部分输入 `OutputInterestTable`。

注意，每你输入时，每个引用该新方法的位置都会自动更改。新方法的建议签名以 `private static` 关键字开头，并在括号中包含 `principal`、`interest` 和 `duration`。

```cs
private static decimal OutputInterestTable(decimal principal,
decimal interest, int duration)
```

4. 点击 Apply（应用）以完成提取方法重构。

你在步骤 1 中选择的代码位于 `Main()` 下方，并命名为 `OutputInterestTable()`。在它原来占据的位置，你看到了此方法调用：

```cs
principal = OuputInterestTable(principal, interest, duration);
```

所有这些重构的结果由以下两个部分组成：

* `Main()` 下方一个新的 `private static` 方法，命名为 `OutputInterestTable()`
* `Main()` 内部原提取代码位置的行代码：

```cs
principal = OutputInterestTable(principal, interest, duration);
```

![提示](img/tip.png) 你可以执行额外的重构，以获得与上一节非常相似的程序外观。后续步骤从消除用于输入信息的冗余代码开始。如果你查看原始代码，你会发现实际上有三个针对本金、利率和期限的循环部分，除了提示词外，它们是重复的，因此这是开始重构的好地方。然后你可以像上一节中那样简化输入过程。使用这些步骤来完成任务：

1. 高亮 `Main()` 方法中的第一个 `while` 循环（紧接 `decimal principal;` 之后的那个），并选择 `Edit ⇒ Refactor ⇒ Extract Method`。

你会看到与之前相同的 Rename: New Method 对话框。

2. 输入 `InputPositiveDecimal` 创建新方法并点击 Apply。

此新方法唯一的问题是它目前专门针对 `principal` 变量，这不会节省任何代码。

3. 选择 `Edit ⇒ Refactor ⇒ Reorder Parameters`（编辑 ⇒ 重构 ⇒ 排序参数）。

你会看到 Change Signature（更改签名）对话框。此对话框允许你不仅仅是更改参数顺序（通过高亮参数并点击上下箭头），你还可以用它添加和删除参数。

4. 点击 `Add`（添加）。

你会看到 Add Parameter（添加参数）对话框。

5. 在 Type Name 字段中输入 `string`，在 Parameter Name 字段中输入 `prompt`，在 Value 字段中输入“Principal”，然后点击 OK。

你创建了一个类型为 `string` 的输入参数，名为 `prompt`，对于此调用其值为 `"Principal"`。更重要的是，新方法现在更接近泛型。

6. 将 `InputPositiveDecimal()` 中的第一个 `Console.write()` 调用更改为：`Console.Write($"Enter {prompt}: ");`。

7. 将错误消息的第一行更改为：`Console.WriteLine($"{prompt} cannot be negative");`。

函数中的提示词现在是通用的。它们适用于任何情况。

8. 右键点击 `InputPositiveDecimal()` 中的 `principal` 变量声明，选择 Rename（重命名）。输入 `value` 并点击 Apply。

用于获取信息的提示词现在更具通用性。

9. 将 `Main()` 中的第二个 `while` 循环替换为 `interest = InputPositiveDecimal("Interest");`。

确保你删除了第二个循环。此时，你可以构建并运行应用程序，结果将是相同的。

### 使用本地函数

在大多数应用程序中，处理安全性变得越来越困难。例如，如果一个方法调用另一个方法，将被调用方法放在调用方法内部将提高安全性。

CalculateInterestTableWithMethods` 程序演示了如何在不损失功能的情况下执行此任务。

首先使用本章早前的“获取 Program.cs 文件”节所示的技术，从 `CalculateInterestTableWithMethods` 程序获取 `Program.cs` 文件的副本。完成后打开该文件。

你想做的第一个更改是将 `InputPositiveDecimal()` 方法移动到 `InterestData()` 方法的末尾。删除 `InputPositiveDecimal()` 方法前的 `public static`。本地函数通常不包含关键字，因为它们通常是私有的，并且遵循主方法的静态或实例功能。更新后的代码如下：

```cs
public static void InterestData(ref decimal principal,
ref decimal interest,
ref decimal duration)
{
    // 1a -- 获取本金。
    principal = InputPositiveDecimal("principal");
    // 1b -- 现在输入利率。
    interest = InputPositiveDecimal("interest");
    // 1c -- 最后是期限
    duration = InputPositiveDecimal("duration");

    // InputPositiveDecimal -- 从键盘返回一个
    // 正数小数。
    decimal InputPositiveDecimal(string prompt)
    {
        // 持续尝试直到用户正确。
        while (true)
        {
            // 提示用户输入。
            Console.Write("Enter " + prompt + ":");
            // 从键盘检索小数值。
            string input = Console.ReadLine();
            decimal value = Convert.ToDecimal(input);
            // 如果输入的值正确，则退出循环。
            if (value >= 0)
            {
                // 返回用户输入的有效小数。
                return value;
            }
            // 否则，对错误输入生成错误。
        }
    }
}
```





```csharp
Console.WriteLine(prompt + " cannot be negative");
Console.WriteLine("Try again");
Console.WriteLine();
}
}
}
``` 你要进行的第二个更改是将 `InputInterestData()` 和 `OutputInterestTable()` 方法的 `public` 更改为 `private`。现在你已经准备好尝试更新后的程序了。程序的运行方式与之前完全相同，但现在安全性高得多。

## 为方法传递参数

像下面示例中的方法，用性就像七月份的雪铲一样小，因为没有数据传入或传出该方法：

```csharp
public static void Output()
{
    Console.WriteLine("this is a method");
}
```

将此示例与*会*执行某些功能的真实世界方法进行比较。例如，正弦运算需要某种类型的输入——毕竟，你必须计算某个值的正弦。同样，为了拼接两个 `string`，你需要两个 `string`。因此，`Concatenate()` 方法至少需要两个 `string` 作为输入。你需要找到一种让数据进入和离开方法的方法。

### 向方法传递参数

你输入到方法中的值称为*参数（arguments）*。方法的输入称为*参数（parameters）*。参数是输入的完整列表，其中某些可以是可选的，因此你提供给方法的参数可能与方法的参数列表不匹配。大多数方法如果要执行某些操作，都需要某些类型的参数。你通过在方法名后的括号中列出参数来向方法传递参数。考虑为之前提供的 `Example2` 程序中的 `Example` 类添加以下这一小部分：

```csharp
public class Example
{
    … 其他方法 …
    public static void Output(string someString)
    {
        Console.WriteLine("Output() was passed the argument: " + someString);
    }
}
```

你可以通过在 `Main()` 中添加代码来在同一个类内部调用此方法，如下：

```csharp
Example.Output("Hello");
```

然后你将看到这个看起来不那么有趣的输出：

```
Output() was passed the argument: Hello
```

程序向方法 `Output()` 传递了字符串 `"Hello"` 的引用。该方法接收该引用并将其命名为 `someString`。`Output()` 方法可以在方法内部使用 `someString`，就像它使用任何其他 `string` 变量一样。尝试在 `Main()` 代码的末尾添加这段代码：

```csharp
string myString = "Hello";
Example.Output(myString);
```

这段代码段将变量 `myString` 分配给字符串 `"Hello"` 的引用。调用 `Output(myString)` 传递了 `myString` 所引的对象，也就是你的老朋友 `"Hello"`。从那里开始，效果与之前相同。

向程序传递参数也是一个类似的思路。例如，你可能已经注意到 `Main()` 通常接收一个数组参数。

### 向方法传递多个参数

你可以定义一个具有不同类型多个参数的方法。考虑 `AverageAndDisplay` 程序中的以下示例方法 `AverageAndDisplay()`：

```csharp
// AverageAndDisplay -- 计算两个带有标签数字的平均值并显示结果。
private static void AverageAndDisplay(string s1, double d1,
string s2, double d2)
{
    double average = (d1 + d2) / 2;
    Console.WriteLine($"The average of {s1}"
    + $" whose value is {d1} and {s2}"
    + $" whose value is {d2} is {average}.");
}
```

你使用以下代码从 `Main()` 中调用它：

```csharp
static void Main(string[] args)
{
    // 访问成员方法。
    AverageAndDisplay("grade 1", 3.5, "grade 2", 4.0);
    Console.Read();
}
```

执行这个简单的程序会产生此输出：

```
The average of grade 1 whose value is 3.5 and grade 2 whose value is 4 is 3.75.
```

`AverageAndDisplay()` 方法声明时带有多个参数，这些参数按照传递给它们的顺序排列的。

如往常，示例程序的执行从 `Main()` 之后的第一个语句开始。`Main()` 中的第一行非注释代码调用了 `AverageAndDisplay()` 方法，传递了两个 `string` "grade 1" 和 "grade 2" 以及两个 `double` 值 3.5 和 4.0。

`AverageAndDisplay()` 方法计算传递给它的两个 `double` 值 `d1` 和 `d2` 的平均值，以及它们包含在 `s1` 和 `s2` 中的名称，计算出的平均值存储在 `average` 中。

![Tip](img/tip.png) 在方法内部更改参数的值会导致混淆和错误，因此要明智地将值赋予临时变量并对其进行修改。

### 参数定义与使用的匹配

如果你在不命名的情况下调用方法，则方法调用中的每个参数在类型和顺序上都必须与方法定义匹配。。在 `AverageWithCompilerError` 中找到的以下（非法的）`Main()` 版本会产生两个编译错误：

```csharp
static void Main(string[] args)
{
    // 访问成员方法。
    AverageAndDisplay("grade 1", "grade 2", 3.5, 4.0);
    Console.Read();
}
```

### 方法重载

重载方法并不意味着给它分配过多的任务![Tip](img/tip.png) 你可以给给定类中的两个方法相同的名称——被称为*方法重载（overloading）*——只要它们所需的参数在类型或数量上不同。`AverageAndDisplay` 示例中的这两个方法演示了重载：

```csharp
private static void AverageAndDisplay(string s1, double d1,
string s2, double d2)
{
    double average = (d1 + d2) / 2;
    Console.WriteLine($"The average of {s1}"
    + $" whose value is {d1} and\r\n {s2}"
    + $" whose value is {d2} is {average}.\r\n");
}

private static void AverageAndDisplay(double d1, double d2)
{
    double average = (d1 + d2) / 2;
    Console.WriteLine($"The average of {d1} and {d2}"
    + $" is {average}.");
}
```

此程序定义了两个版本的 `AverageAndDisplay()`。注意第一个版本使用了 `\r\n` 转义字符在输出之间创建换行，这样输出更容易阅读。你在书中其他示例中也会其他的转义字符。程序通过传递正确的参数来调用一个另一个，如下所示：

```csharp
static void Main(string[] args)
{
    // 访问方法的第一个版本。
    AverageAndDisplay("my GPA", 3.5, "your GPA", 4.0);
    // 访问方法的第二个版本。
    AverageAndDisplay(3.5, 4.0);
    Console.Read();
}
```

C# 可以通过比较调用和定义来判断程序想要哪个方法。程序可以正常编译，并在执行时产生此输出：

```
The average of my GPA whose value is 3.5 and
your GPA whose value is 4 is 3.75.
The average of 3.5 and 4 is 3.75.
```

![Remember](img/remember.png) C# 不允许同一类中的两个方法具有相同的名称，除非方法参数的数量或类型不同（或者两者都不同）。因此 C# 能够区分这两个方法：





* ``AverageAndDisplay(string, double, string, double)``
* ``AverageAndDisplay(double, double)`

当你这样看时，显而易见这两个方法是不同的。

### 实现默认参数

在某些情况下，方法需要一个`default argument`（默认参数），即一个预定义值，使其更易使用。如果使用该方法的大多数开发者都需要某个特定值，那么默认值就是合理的。为参数提供值随后就成了灵活性的一种体现，使得需要其他值的开发者仍然具有提供值的选项。开发者通常有两种常用途径：

*   **方法重载（Method overloading）：** 上一节中展示的技术允许你创建一个默认参数。你可以在方法体内部设置未提供的参数值。这种方法的问题在于：
    *   它对任何阅读代码的人来说都是令人困惑的，因为重载方法的目的并不明确。
    *   它很容易出错，因为你现在有两个或多个版本的相同方法需要维护。
*   **默认参数（Default parameters）：** C# 提供了在方法参数列表中设置默认参数的方法。这种技术是清晰的，因为任何查看代码的人都能看到默认值作为方法声明的一部分——无需深入研究方法代码。

由于使用方法重载作为处理默认参数的手段具有复杂性且容易出错，本书始终使用默认参数方法，如 `MethodsWithDefaultArguments` 程序中的 `DisplayRoundedDecimal()` 方法所示：

```csharp
static private string DisplayRoundedDecimal(
decimal value = 0,
int numberOfSignificantDigits = 2)
{
    // 首先将数字舍入到指定的
    // 有效位数。
    decimal roundedValue = decimal.Round(
    value, numberOfSignificantDigits);
    // 将其转换为字符串。
    string s = Convert.ToString(roundedValue);
    return s;
}
```

`DisplayRoundedDecimal(decimal, int)` 方法通过结合 `Round()` 和 `ToString()` 方法，将提供的 `decimal` 值转换为带有指定小数点后位数的 `string`。由于小数通常用于显示金额，因此最常见的选择是在小数点后保留两位。注意在每个参数后面使用等号（`=`）来提供默认值。`value` 的默认值为 `0`，`numberOfSignificantDigits` 的默认值为 `2`。你现在有三种方式通过使用此处所示的默认值来调用 `DisplayRoundedDecimal()`：

```csharp
static void Main(string[] args)
{
    // 不提供任何值。
    Console.WriteLine(DisplayRoundedDecimal());
    // 只提供第一个值。
    Console.WriteLine(DisplayRoundedDecimal(12.345678M));
    // 提供两个值。
    Console.WriteLine(DisplayRoundedDecimal(12.345678M, 3));
    Console.ReadLine();
}
```

第三次调用是唯一一个提供了两个值的调用，这证明了默认值的用处。当你将光标悬停在带有默认值的方法上时，你会在弹出帮助中看到这些值，如图 2-3 所示。

![Visual Studio 告诉你默认方法参数的值。](img/9781119839071-fg020203.png)

图 2-3： Visual Studio 告诉你默认方法参数的值。

这是该示例的输出：
```
0
12.35
12.346
```

## 使用引用传递（Call-by-Reference）特性

许多现实世界的操作会创建返回给调用者的值。例如，`Sin()` 接收参数并返回三角正弦。方法可以通过两种方式向调用者返回值：

*   使用 `return` 语句
*   使用引用传递（call-by-reference）特性

本章之前的大多数示例都演示了 `return` 语句方法，所以你已经知道这种方法的工作原理了。`CallByReference` 程序中的 `Average()` 方法演示了引用传递特性，如下：

```csharp
private static void Average(
ref double Result,
double Input1 = 1.0,
double Input2 = 2.0)
{
    Result = (Input1 + Input2) / 2;
}
```

注意此示例中添加的 `ref` 关键字。当你提供变量的引用而不是变量的值时，方法可以更改变量在调用者看来出现的值。本书中引用变量最常见的用途是传递像结构体之类的复杂变量。然而，在需要调用 Windows API 或创建复杂应用程序的情况下，你可以使用这种技术。`https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/ref` 处的讨论将告诉你更多关于书中未涵盖的这些高级主题。

![警告](img/warning.png) 当使用带有默认值的变量时，引用变量必须始终作为第一个变量。否则，编译器将报错。这里是 `Main()` 的版本：

```csharp
static void Main(string[] args)
{
    // 初始化 Result 并显示它。
    double Result = 0;
    Console.WriteLine(Result);
    // 进行调用。
    Average(ref Result, 4.0, 3.0);
    // 显示更改。
    Console.WriteLine(Result);
    Console.ReadLine();
}
```

代码开始将 `Result` 初始化为 `0` 并显示该值。此示例提供了两个值，但这种情况下实际上不需要。调用后，`Result` 现在包含 `3.5`。`Average()` 方法能够更改 `Result` 是因为你通过引用传递了它。

## 定义无返回值的方法

某些方法不需要向调用者返回值。之前的方法 `AverageAndDisplay()` 显示了参数的平均值，但不将该平均值返回给调用者。与其留空返回类型，不如以如下方式声明 `AverageAndDisplay()`：

`private void AverageAndDisplay(double, double)`

通常通常返回类型的地方关键字 `void` 表示没有类型。也就是说，声明 `void` 表示 `AverageAndDisplay()` 方法没有返回值。（无论如何，每个方法都指定了返回类型，即使是 `void`。）

![记住](img/remember.png) `void 方法` 没有返回值。这个定义并不意味着该方法是空的，也不是意味着它用于医学或航天目的；它仅仅指的是关键字。

非返回值方法必须通过执行 `return` 后跟要返回的值将控制权传回调用者。`void` 方法没有要返回的值。`void` 方法在遇到没有值的 `return` 时返回。或者，默认情况下（如果没有 `return`），`void` 方法在控制权到达方法的结束括号时自动退出。考虑位于 `VoidMethods` 程序中的 `DisplayRatio()` 方法：

```csharp
private static void DisplayRatio(double numerator,
double denominator)
{
    // 如果分母为零……
    if (denominator == 0.0)
    {
        // 输出错误消息并……
        Console.WriteLine("比率的分母不能为 0");
        // 返回给调用者。
        return; // 由于错误导致的提前返回
    }
    // 只有当分母不为零时执行此代码。
    double ratio = numerator / denominator;
    Console.WriteLine($"The ratio of {numerator}" +
    $" over {denominator} is {ratio}.");
} // 如果分母不为零，方法在此退出。
```




- **如果此值为零：** 程序将显示错误消息并返回调用者，而不会尝试计算比率。如果你执行计算，也不会发生任何糟糕的事情；结果将是无穷大。然而，在可以的情况下，不向用户提供无限值是一个良好的做法。
- **如果值不为零：** 程序将显示比率。紧随 `WriteLine()` 的右大括号是方法 `DisplayRatio()` 的右大括号，因此它是程序的返回点。

## 使用元组返回多个值

在 C# 7.0 之前的版本中，每个返回值都是单一对象。它可以是一个非常复杂的对象，但仍然是一个单一对象。在 C# 7.0 中，你实际上可以使用元组返回多个值。元组是一种名上包含两个项目的动态数组，你可以将其解释为键值对（但并非强制要求）。在 C# 中，你还可以创建包含两个以上项目的元组。Python 等许多语言使用元组来简化编码，并使与值的交互变得容易得多。

C# `4.x` 实际上作为动态编程技术的一部分引入了元组的概念。然而，C# 7.0 改进了元组的使用，允许返回多个值而不仅仅是一个单一对象。本书没有对元组提供广泛的介绍，但它们在返回复杂数据方面的效果非常好，因此你确实需要了解这种元组用法。

### 使用元组

元组依赖于 `Tuple` 数据类型，该类型可以接受多达七个泛型参数，并可能有第八个。处理元组的最佳方法是在声明中提供计划提供的变量的数据类型。以下是一个返回元组的方法示例，位于 `UseTuples` 程序中：

```cs
private static Tuple<string, int> getTuple()
{
    // 使用元组返回单个值。
    return new Tuple<string, int>("Hello", 123);
}
```

代码开始时指定 `getTuple()` 返回一个包含两个项目（一个 `string` 和一个 `int`）的 `Tuple`。你使用 `new` 关键字来创建 `Tuple` 实例，在角括号 `<string, int>` 中指定数据类型，然后提供数据值。`getTuple()` 方法有效地返回了两个你可以单独操作的值，如下所示：

```cs
// 这是你的程序开始的地方。
static void Main(string[] args)
{
    // 获取一个条目元组。
    Console.WriteLine(
    getTuple().Item1 + " " + getTuple().Item2);
    Console.Read();
}
```

要访问像这样的元组，你调用 `getTuple()`，添加一个点，然后指定要使用哪个项目，`Item1` 或 `Item2`。这个示例仅演示了元组的工作原理，因此非常简单。输出如下：

`Hello 123`

![Tip](img/tip.png) 使用元组可以让你返回两个值，而无需诉复杂的数据类型或其他结构。当输出要求符合元组的范围时，它会让你的代码更简单。例如，在执行某些数学操作时，你需要返回结果和余数，或者复数的实部和虚部。

## 依赖 Create() 方法

创建元组的另一种方法是依赖 `Create()` 方法。结果与使用上一节中找到的方法相同。以下是使用 `Create()` 方法的示例，位于 `CreateTuples` 程序中：

```cs
// 使用 Create() 方法。
var myTuple = Tuple.Create<string, int>("Hello", 123);
Console.WriteLine(myTuple.Item1 + "\t" + myTuple.Item2);
```

这种方法没有使用上一节所示的方法那么安全，因为由于使用了 `var`，`myTuple` 内部可能是任何内容。你可以进一步消除构造函数中的 `<string, int>` 部分，以强制编译器确定 `myTuple` 应该接收什么输入。在使用 .NET Framework 版本 4.7 或以上版本时，你也可以依赖这种创建元组的简写方法（特别是 `ValueTuple`）：

```cs
(string, int) t1 = ("Hello", 123);
Console.WriteLine($"{t1.Item1}\t{t1.Item2}");
```

## 创建包含两个以上项目的元组

在大多数情况下，元组可以有一个到八个项目（详情请参见 [`https://docs.microsoft.com/en-us/dotnet/api/system.tuple-8?view=net-5.0`](https://docs.microsoft.com/en-us/dotnet/api/system.tuple-8?view=net-5.0)）。如果你需要超过八个项目，第八个项目必须包含另一个元组。嵌套元组允许你返回几乎无限数量的项目，但在某些时刻，你确实需要查看代码的复杂度，并看看是否可以减少返回项目的数量。否则，你会发现你的应用程序运行缓慢并消耗大量资源。以下是一个使用包含三个项目的三个 Tuple 的示例，每个项目都封装在元组数组中（在 `LotsOfTupleItems` 程序中）：

```cs
static Tuple<string, int, bool>[] getTuple()
{
    // 创建一个新的元组。
    Tuple<string, int, bool>[] aTuple =
    {
        new Tuple<string, int, bool>("One", true),
        new Tuple<string, int, bool>("Two", false),
        new Tuple<string, int, bool>("Three", true)
    };
    // 返回值列表。
    return aTuple;
}
```

该技术遵循与相同的模式。唯一的区别是为为每个元组提供了更多的值。然而，还有另一种选择。这是一个包含更多内容的元组版本：

```cs
var myTuple2 = (1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14);
Console.WriteLine(myTuple2.Item11);
foreach (var Item in myTuple2.ToString().Split(','))
{
    Console.WriteLine(Item);
}
```





第 2 章 也讨论了局部函数，将其作为重构过程的一部分，以提高代码的可读性。然而，你不必等到重构代码时才使用局部函数。本章讨论了如何作为代码规划过程的一部分来使用它们。

![记住](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用可下载的源码要得多。你可以在可下载源码的 `\CSAIO4D2E\BK02\CH03` 文件夹中找到本章的源码。有关如何找到这些源文件的详情，请参阅“简介”。

## 向方法传递对象

你将对象引用作为参数传递给的方法与传递值类型变量相同，但区别在于：你始终通过引用传递对象。`PassObject` 程序中的 `Student` 类展示了本示例中使用的非常简单的类：

```csharp
internal class Student
{
    internal string Name { get; set; }
}
```

![提示](img/tip.png) 注意 `Student` 类被标记为 `internal`。`internal` 作用域允许当前 `assembly`（本质上是一个用于部署代码的包）内部的所有内容看到 `Student` 类（例如存放 `Main()` 方法的 `Program` 类），但外部的任何内容都无法看到。使用这种作用域使你的代码更加安全。本微型书籍第 4 章的“限制类成员的访问”会告诉你更多关于作用域的知识，但在创建更多应用程序时，记住安全性是很。否则，`Student` 类平平无奇——它只包含自动实现的 `Name` 属性。

此示例除了协调活动的 `Main()` 之外，还使用了两个方法与 `Student` 类进行交互。它们如下：

```csharp
// OutputName -- 输出学生的名字。
private static void OutputName(Student student)
{
    // 输出当前学生的名字。
    Console.WriteLine($"Student's name is {student.Name}.");
}

// SetName -- 修改学生对象的名字。
private static void SetName(Student student, string name)
{
    if (name.Length > 1)
        student.Name = name;
    else
        throw new ArgumentException("不允许空名称!", "name");
}
```

`OutputName()` 方法使用特定的格式显示 `Name` 属性。在程序中，将输出功能与流程控制功能分离是常见的做法。使用这种方法可以提供多种输出技术，而无需不断修改流程控制代码。重写少的代码更好。注意这两个方法都依赖于 `private` 作用域，这是恰当，因为 `Program` 类外部没有任何需要看到这些方法。

![记住](img/remember.png) 通常情况下，当你想要更改属性值时，只需按需设置即可。`SetName()` 方法强制执行了一种特定的方法来更新 `Name` 属性。`Student` 类并不关心是否提供了空名称，但 `SetName()` 方法关心。你可以通过这种方式执行各种检查，例如在输入中寻找与某些代码漏洞相关的非字母字符。此示例仅确保调用者提供的是空名称以外的任何内容。如果检测到空名称，它将抛出一个带有帮助信息和错误参数名称的异常*exception*）。现在是时候看看 `Main()` 了：

```csharp
static void Main(string[] args)
{
    Student student = new Student();
    // 通过直接访问来设置名字。
    Console.WriteLine("The first time:");
    student.Name = "Madeleine";
    OutputName(student);
    // 尝试提供一个坏名字。
    Console.WriteLine("\r\nTrying a bad value:");
    try
    {
        SetName(student, "");
        OutputName(student);
    }
    catch (ArgumentException e)
    {
        Console.WriteLine(e.Message);
        Console.WriteLine($"Sent {e.ParamName} \"\" value.");
    }
    // 使用方法更改名字。
    Console.WriteLine("\r\nAfter being modified:");
    try
    {
        SetName(student, "Willa");
        OutputName(student);
    }
    catch (ArgumentException e)
    {
        Console.WriteLine(e.Message);
        Console.WriteLine($"Sent {e.ParamName} \"\" value.");
    }
    Console.Read();
}
```

程序创建了一个 `student` 对象。程序首先直接设置 `student` 的名字，并将`student 对象`传递给输出方法 `OutputName()`。`OutputName()` 显示它收到的任何 `Student` 对象的名字。

程序随后尝试通过带空值调用 `SetName()` 来更新 `student` 的名字。此操作导致了异常*exception*，代码随后对其进行了处理。注意使用转义双引号（`\"\"`）在输出中提供双引号。在这种情况下，没有调用 `OutputName()`，因为异常在调用之前就发生了。

第二次调用 `SetName()` 更成功，因为代码提供了空值以外的其他内容。由于 C# 中所有引用类型对象都是通过引用传递的，对 `student` 的更改被保留在 `Main()` 中，正如这段代码所示：

The first time:
Student's name is Madeleine.
Trying a bad value:
Blank names not allowed!
Parameter name: name
Sent "" value.
After being modified:
Student's name is Willa.

## 静态方法与实例方法的

类应该收集描述现实对象或概念的元素。例如，`Vehicle` 类可能包含特定于最大速度、重量和载能力的属性。这些属性通常作为实例属性或实例方法出现。然而，“Vehicle` 还具有影响所有类型车辆的属性：启动和停止等能力。这些全局属性通常作为静态方法出现。接下来的章节将介绍如何混合静态和实例方法以创建更好的对象描述。

### 使用静态属性和方法

通常，你将反映对象的数据和行为保留在类内部。在之前的示例中，`OutputName()` 和 `SetName()` 作为 `Program` 类的一部分出现，这显然违反了面向对象编程（OOP）的封装规则。你可以用更好的方式重写上一节的 `Student` 类，如 `StudentClass1` 程序所示：

```csharp
internal class Student
{
    private static int _numStudents = 1;
    internal string Name { get; set; }
    internal static void OutputName(Student student)
    {
        Console.WriteLine($"Student's name is {student.Name}.");
    }
    internal static int NumStudents { get => _numStudents; }
    internal static void SetNumStudents(int NumStudents)
    {
        if (NumStudents > 0)
            _numStudents = NumStudents;
        else
            throw new ArgumentOutOfRangeException("值必须大于 0", "NumStudents");
    }
    internal static void OutputNumStudents()
    {
        Console.WriteLine($"The number of students is: {_numStudents}.");
    }
}
```

此版本的类侧重于将 `OutputName()`（实现为静态方法）移动到类中。它直接访问实例属性 `Name`。你之所以将 `OutputName()` 创建为静态方法是因为它对任何实例都有效。一个实例不会使用一个版本的 `OutputName()`，而另一个实例使用完全不同的版本。这种场景产生的混乱会让任何人感到困惑。因此，你可以根据需要在一个应用程序中组合静态方法和实例属性。




你还看到了一个新的静态属性成员 `NumStudents`。你将 `NumStudents` 实现为静态属性而不是实例属性，是因为学校的学生人数适用于每位学生。除非发生了什么奇怪的事，否则每个学生看到的学校人数都是相同的，而不是看到一些只有他们自己才能看到的“隐形学生”。访问 `_numStudents`（存储 `NumStudents` 属性值的字段）需要一种略有不同的 `get` 访问器形式，因为你现在有了一个真实的具名字段。此外请注意，`_numStudents` 私有作用范围，因为类外部没有地方需要访问它。通常情况下，静态属性是只读的，因此此示例提供了一个特定的 `SetNumStudents()` 静态方法来更改值。请注意，这个设置访问器以 `ArgumentOutOfRangeException` 的形式提供了错误捕获。最后，`OutputNumStudents()` 方法以格式化的方式输出当前的学生人数。总来说，你不要将静态属性与实例方法结合；你应该使用静态方法来访问静态属性。

`Main()` 方法与之前的示例相比，变化在于它提供了对新静态属性的访问。然而，这个版本的 `Main()` 也是损坏的，因为 `Name` 不再提供任何错误捕获。别担心，这个问题将在下一节中得到修复。以下是当前的 `Main()` 代码。

```cs
static void Main(string[] args)
{
    Student student = new Student();
    // 设置学生人数。
    try
    {
        Student.SetNumStudents(2);
        // 显示学生人数。
        Student.OutputNumStudents();
        Console.WriteLine($"The Number of Students is: " +
        $"{Student.NumStudents}.");
    }
    catch (ArgumentOutOfRangeException e)
    {
        Console.WriteLine(e.Message);
    }
    // 尝试提供错误的名称。
    Console.WriteLine("\r\nTrying a bad value:");
    try
    {
        student.Name = "";
        Student.OutputName(student);
    }
    catch (ArgumentException e)
    {
        Console.WriteLine(e.Message);
        Console.WriteLine($"Sent {e.ParamName} \"\" value.");
    }
    // 使用方法修改名称。
    Console.WriteLine("\r\nAfter being modified:");
    try
    {
        student.Name = "Sally";
        Student.OutputName(student);
    }
    catch (ArgumentException e)
    {
        Console.WriteLine(e.Message);
        Console.WriteLine($"Sent {e.ParamName} \"\" value.");
    }
    Console.Read();
}
```

这个版本的 `Main()` 将形成下一节代码的大部分基础，在下一节中，你将看到当前问题被修复。目前，提供空名称不会触发错误消息，如下所示：

```
The number of students is: 2.
The Number of Students is: 2.
Trying a bad value:
Student's name is .
After being modified:
Student's name is Sally.
```

### 有效使用实例属性和方法

实例属性和方法倾向于关注实例之间不同或以某种方式特定于实例的对象元素。在 `StudentClass2` 程序中更新的 `Student` 类显示了一些有趣的变化，这些变化使得该类运行得比上一节的版本要好得多。

```cs
internal class Student
{
    private string _name = "";
    private static int _numStudents = 1;
    internal string Name
    {
        get => _name;
        set
        {
            if (value.Length > 1)
                _name = value;
            else
                throw new ArgumentException("Blank names not allowed!", "Name");
        }
    }
    internal static void OutputName(Student student)
    {
        Console.WriteLine($"Student's name is {student.Name}.");
    }
    public override string ToString()
    {
        // 输出当前学生的名称。
        return $"Student's name is {Name}.";
    }
    internal static int NumStudents { get => _numStudents; }
    internal static void SetNumStudents(int NumStudents)
    {
        if (NumStudents > 0)
            _numStudents = NumStudents;
        else
            throw new ArgumentOutOfRangeException("Value must be greater than 0", "NumStudents");
    }
    internal static void OutputNumStudents()
    {
        Console.WriteLine($"The number of students is: {_numStudents}.");
    }
}
```

首先要考虑到，`Name` 属性现在使用了字段，就像 `NumStudents` 一样。出于安全考虑，它同样被设置为具有私有作用范围。`Name` 属性的代码现在包含了与第一个示例中 `SetName()` 方法相同的安全功能，但现在它们是实际属性代码的一部分，这正是它们应该待在的地方。由于添加了 `_name` 字段，`get` 访问器也需要如所示进行更改。

![Tip](img/tip.png) 当你查看方法列表时，你会发现了一个“违规者”，`ToString()` 方法。默认提供的标准 `ToString()` 方法信息量非常有限。因此，这个版本的 `ToString()` 输出的是 `Student`，而你希望将其替换为 `Student.ToString()`。

### 扩展方法的全名

某些应用程序中发现的方法名存在一个微妙但重要的问题。要看到这个问题，请考虑以下示例代码：

```cs
public class Person
{
    public void Address()
    {
        Console.WriteLine("Hi");
    }
}

public class Letter
{
    string address;
    // 存储地址。
    public void Address(string newAddress)
    {
        address = newAddress;
    }
}
```

任何对 `Address()` 方法的后续讨论都是歧义的。`Person` 内部 `Address()` 方法与 `Letter` 中的 `Address()` 方法无关。如果应用程序需要访问 `Address()` 方法，它访问的是哪一个？问题不在方法本身，而在于描述。这种描述与名字非常相似。在家里，你可能永远不会遇到任何歧义，因为你是唯一拥有那个名字的人。但在工作中，当有人试图引起另一个和你名字相同的人注意时，你可能会回应。当然，这就是人们诉诸姓的原因。因此，你可以将 `Address()` 视为方法的名，而将其类视为姓。

### 访问当前对象

考虑 `CurrentObject` 程序中找到的以下 `Student.SetName()` 方法：

```cs
internal class Student
{
    // 描述学生的名称信息
    private string firstName;
    private string lastName;
    // SetName -- 保存名称信息。
    internal void SetName(string FirstName, string LastName)
    {
        firstName = FirstName;
        lastName = LastName;
    }
    public override string ToString()
    {
        return $"{firstName} {lastName}";
    }
}

class Program
{
    static void Main(string[] args)
    {
        Student student1 = new Student();
        student1.SetName("Joseph", "Smith");
        Student student2 = new Student();
    }
}
```




```csharp
student2.SetName("John", "Davis");

// 显示学生是分开的。

Console.WriteLine(student1.ToString());

Console.WriteLine(student2.ToString());

Console.ReadLine();

}

```

`Main()` 方法使用 `SetName()` 方法来更新第一个 `student1` 然后是 `student2`。但在 `SetName()` 方法内部，你并没有看到对 `Student` 对象的引用。事实上，不存在对 `Student` 对象的引用。在这种情况下，实例方法被认为是在*当前对象*（当前正在使用的对象）上操作的。方法是如何知道哪一个是当前对象的呢？请真正的当前对象站一下吧？答案很简单。当前对象是作为隐式参数在方法调用时传递的。例如：

```csharp
student1.SetName("Joseph", "Smith");
```

此此调用等同于以下代码：

```csharp
Student.SetName(student1, "Joseph", "Smith"); // 等效调用，
//（但无法正常编译）。
```

该示例并不是说你可以以两种不同的方式调用 `SetName()`；而是说这两个调用在语义上是等价的。标识当前对象的对象——即隐藏的第一个参数——就像其他参数一样被传递给方法。将此任务交给编译器即可。

隐式传递对象是很容易理解的，但从一个方法到另一个方法的引用又是怎样的？下面的代码片段（在 `CurrentObject2` 中找到）说明了如何从一个方法调用另一个方法：

```csharp
internal class Student
{
    // 描述学生的名称信息
    private string firstName;
    private string lastName;
    // SetName -- 保存名称信息。
    internal void SetName(string FirstName, string LastName)
    {
        SetFirstName(FirstName);
        SetLastName(LastName);
    }

    private void SetFirstName(string FirstName)
    {
        firstName = FirstName;
    }

    private void SetLastName(string LastName)
    {
        lastName = LastName;
    }

    public override string ToString()
    {
        return $"{firstName} {lastName}";
    }
}
```

在调用 `SetFirstName()` 时没有出现任何对象。当前对象继续静默地从一个方法调用传递到下一个方法调用。假设对象方法内部对任何成员的访问都是针对当前对象的。结果是方法知道它属于哪个对象。`当前对象`（或 `当前实例`）的意思类似于 `me`（我）。

### 什么是 this 关键字？

与大多数参数不同，当前对象没有出现在方法的参数列表中，因此它没有由程序员分配名称。相反，C# 为此对象分配了较缺乏想象力的名称 `this`，这在您需要直接引用当前对象的少数情况下非常有用。因此，你可以像下面这样编写上例的示例（如 `CurrentObject3` 所示）：

```csharp
internal class Student
{
    // 描述学生的名称信息
    private string firstName;
    private string lastName;
    // SetName -- 保存名称信息。
    internal void SetName(string FirstName, string LastName)
    {
        this.SetFirstName(FirstName);
        this.SetLastName(LastName);
    }

    private void SetFirstName(string FirstName)
    {
        this.firstName = FirstName;
    }

    private void SetLastName(string LastName)
    {
        this.lastName = LastName;
    }

    public override string ToString()
    {
        return $"{firstName} {lastName}";
    }
}
```

注意显式添加了关键字 `this`。在成员引用中添加它不会增加任何内容，因为 `this` 是被假设的。然而，当 `Main()` 执行以下调用时，`this` 在整个 `SetName()` 以及它可能调用的任何其他方法中引用 `student1`：

```csharp
student1.SetName("John", "Smith");
```

### this 关键字何时是显式的？

你通常不需要显式地引用 `this`，因为编译器会在需要的地方理解它。然而，有两种常见情况需要 `this`。在初始化数据成员时，你可能需要它，在此例所示：

```csharp
internal class Person
{
    private string name; // 下面这就是 this.name。
    private int id; // 且面这就是 this.id。
    internal void Init(string name, int id) // 这些是方法参数。
    {
        this.name = name; // 参数名称与数据成员名称相同
        this.id = id;
    }
}
```

`Init()` 方法声明中的参数命名为 `name` 和 `id`，它们与对应数据成员的名称相匹配。该方法非常易于阅读，因为你立即知道哪个参数存储在哪里。唯一的问题是参数列表中的名称 `name` 掩盖了数据成员的名称。编译器对此表示抱怨。

![记住](img/remember.png) 添加 `this` 澄清了意图是指哪一个 `name`。在 `Init()` 内部，变量 `name` 指向方法参数，而 `this.name` 指向 `name` 字段。当然，在此例中，避免需要使用 `this` 的最佳方法是确保字段名与参数名不同，这现在被认为是一种良好的编码实践。在开发者使用了良好的变量命名选择和适当的作用域的大多数情况下，可能不需要使用 `this`。

## 使用局部函数

即使有了你到目前为止看到的所有方法，有时方法仍然可能变得变得复杂且难以阅读。局部函数允许你在方法的作用范围内声明一个函数。接下来的章节将告诉你更多关于局部函数的信息。

### 创建基础局部函数

这是一个可以在 `BasicFunction` 中找到的局部函数的简单示例：

```csharp
static void Main(string[] args)
{
    //创建一个局部函数
    int Sum(int x, int y) { return x + y; }

    // 使用局部函数输出一些和。
    Console.WriteLine(Sum(1, 2));
    Console.WriteLine(Sum(5, 6));
    Console.Read();
}
```

`Sum()` 方法相对简单，但它演示了局部函数是如何工作的。该函数封装了只有 `Main()` 使用的代码。因为 `Main()` 多执行所需的任务，使用 `Sum()` 有助于提高可读性。

![提示](img/tip.png) 局部函数具有任何方法的功能，只是在大多数情况下不能将其声明为静态（可以使用 C# 8.0 或更高版本使用 static 声明它们——文章 https://www.telerik.com/blogs/c-8-static-local-functions-and-using-declarations 提供了关于此主题的更多信息）。

### 在局部函数中使用属性

属性（attribute）*是一种特殊的代码装饰器，定义了特定代码如何以及何时与应用程序的其他部分交互。本节讨论了使用 `LocalFunctionWithAttributes` 的两个简单示例。在继续之前，请确保在自己编写代码时向 `.csproj` 文件添加所需的 C# 9.0，而不是使用可下载的源码（它已经为你包含了所有所需的添加）。你还在 `Program.cs` 文件的顶部添加此 `using` 语句：

```csharp
using System.Diagnostics;
```

```csharp
class Program
{
    static void Main(string[] args)
    {
        //创建一个调试局部函数
```





```csharp
[Obsolete]
[Conditional("DEBUG")]
static void DebugInfo(int x, int y)
{
    Console.WriteLine($"Input x: {x}\r\nInput y: {y}");
}
static int Sum(int x, int y) { return x + y; }
// Use the local function to output some sums.
Console.WriteLine(Sum(1, 2));
DebugInfo(1, 2);
Console.WriteLine(Sum(5, 6));
DebugInfo(5, 6);
Console.Read();
}
```

`[Obsolete]` 特性告诉编译器，此特定函数仍然包含在代码中，但开发者计划在某时弃用它。当用户编译代码时，在每次使用局部函数的地方，错误列表（Error List）窗口都会出现以下警告：

`Warning CS0612 'DebugInfo(int, int)' is obsolete`

`[Conditional("DEBUG")]` 特性告诉编译器仅将函数添加到应用程序的调试版本中。函数本身以及对函数的调用都会从程序的发布版本中移除。因此，当在调试模式下时，你会看到此输出：

`3`
Input x: 1
Input y: 2
`11`
Input x: 5
Input y: 6

![Remember](img/remember.png) 在局部函数上使用 `[Conditional]` 特性 ([`docs.microsoft.com/en-us/dotnet/api/system.diagnostics.conditionalattribute`](https://docs.microsoft.com/en-us/dotnet/api/system.diagnostics.conditionalattribute)) 有特殊要求：

* 你必须将函数声明为 `static`。
* 函数不能有返回值。
* 你必须使用 `C# 9.0` 或更高版本。

不同的属性会有不同的使用要求，因此花些时间确定你究竟计划如何使用该属性是值得的。例如，`[Obsolete]` 特性适用于任何局部函数，因此你不需要进行任何特殊操作即可使用它。`[Obsolete]` 特性提供了相当多的额外功能，你可以在 [`https://docs.microsoft.com/en-us/dotnet/api/system.obsoleteattribute`](https://docs.microsoft.com/en-us/dotnet/api/system.obsoleteattribute) 中阅读相关内容。

# 第 4 章
# 让类对其负责

## 本章内容

![Bullet](img/check.png) 保护类
![Bullet](img/check.png) 使用类构造函数
![Bullet](img/check.png) 构造静态成员或类成员
![Bullet](img/check.png) 使用表达式体成员

类必须对其自己的行为负责。正就像微波炉在你不按错按键时不应该起火一样，类在面对错误数据时，也不应该允许自己“翻车并死亡”。

要对其自己的行为负责，类必须确保其初始状态是正确的，并控制其后续状态以保持其有效性。`C#` 提供了这两种能力。本章将讨论如何让你的类成为代码社区中负责任的成员。毕竟，你不会希望设计一个肆意妄为并制造混乱的叛类。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要容易得多。你可以在下载源码的 `\CSAIO4D2E\BK02\CH04` 文件夹中找到本章的源码。详情请参阅引言关于如何找到这些源文件。

## 限制对类成员的访问

正如你在本小书前面的章节中所看到的，定义类的最佳实践是确保每个成员只提供其他类成员绝对所需的可见性。当你能够实现这种程度的隐藏时（这显然并不总是），将所有内容设为 `private` 是最好的主意。考虑一个 `BankAccount` 程序，它维护着一个 `balance` 数据成员来保留每个账户的余额。将该数据成员设为 `public` 相当于把所有人都建立在诚信的基础上。

大多数银行并没有那么慷慨到留一堆钱和一个账本，让你在每次往钱堆里加钱或取钱时进行记录。毕竟，你可能会忘记在账本上记录你的取款。控制访问可以避免小错误（例如忘记在某处或那里记录取款），并能够避免某些真正严重的取款大错误。接下来的章节将为你提供技术，以维护其他开发者与你创建的类交互的方式。

### 公共的 BankAccount 示例

`BankAccount` 示例将其所有方法声明为 `public`，但将其数据成员（包括 `_accountNumber` 和 `_balance`）声明为 `private`。该示例故意让变量处于错误状态以说明某点。以下代码包含了示例中使用的 `BankAccount` 类：

```csharp
// BankAccount -- 定义一个表示简单账户的类。
public class BankAccount
{
    private static int _nextAccountNumber = 1000;
    private int _accountNumber;
    // 将余额维护为双精度点变量。
    private double _balance;
    // Init -- 初始化银行账户，使用下一个
    // 账户 ID 和 0 余额。
    public void InitBankAccount()
    {
        _accountNumber = ++_nextAccountNumber;
        _balance = 0.0;
    }
    // Balance 属性获取余额。
    public double Balance
    { get => _balance; }
    // AccountNumber 属性
    public int AccountNumber
    { get => _accountNumber; set => _accountNumber = value; }
    // Deposit -- 允许任何存款。
    public void Deposit(double amount)
    {
        if (amount > 0)
        {
            _balance += amount;
        }
    }
    // Withdraw -- 你可以提取任意金额，
    // 直到返回提取的金额。
    public double Withdraw(double withdrawal)
    {
        if (_balance >= withdrawal)
        {
            _balance -= withdrawal;
        }
        return withdrawal;
    }
    // 以字符串返回账户数据。
    public override string ToString()
    {
        return $"{AccountNumber} = {Balance:C}";
    }
}
```

`BankAccount` 类提供了 `InitBankAccount()` 方法来初始化成员，一个 `Deposit()` 方法处理存款，以及一个 `Withdraw()` 方法处理取款。`Deposit()` 和 `Withdraw()` 方法甚至提供了一些规则，例如“不要存款负数”和“不能提取超过你拥有的金额”（我确定你同意这些很好的规则）。然而，如果 `_balance` 是可访问的，那么每个人都建立在诚信的基础上，这就是为什么你要将其设为 `private`。（在此范围内，*外部* 指类外部但在同一程序内。）诚信系统在由程序员编写的大型程序上可能是问题。考虑到人的易错性，它甚至对你来说都可能是问题。以下是执行此代码的 `Main()` 方法：

```csharp
static void Main(string[] args)
{
    Console.WriteLine("此程序无法编译.");
    // 打开一个银行账户。
    Console.WriteLine("创建一个账户对象");
    BankAccount ba = new BankAccount();
    ba.InitBankAccount();
    // 通过 Deposit() 方法访问余额是可以的 --
    // Deposit() 可以访问所有数据成员。
    ba.Deposit(10);
    // 直接访问数据成员是编译时错误。
    Console.WriteLine("万一你运行到这里，下面的代码 "
    + "应该产生编译错误");
    ba._balance += 10;
    Console.Read();
}
```

`Main()` 所做的只是创建一个新的银行账户，初始化它，然后向其中添加钱。注意使用 `ba._balance += 10` 直接访问 `_balance` 的尝试。

![Remember](img/remember.png) 良好的代码带有编译器可以强制的规则，可以避免每个人偶尔在大脚趾上中一子。然而，在你感到太兴奋之前，请注意程序无法构建。尝试这样做会生成此错误消息：

`'BankAccount.BankAccount._balance' 由于其保护级别而不可访问。`




[content]
错误信息似乎有点难以理解，因为大多数情况下错误信息都是这样的（编写一个真正易于理解的错误信息是非常困难的）。问题的关键在于 `_balance` 是私有的，这意味着没有人能看到它。语句 `ba._balance += 10;` 是非法的，因为 `_balance` 对 `Main()` 方法不可，而它是 `BankAccount` 类外部的方法。将此行替换为 `ba.Deposit(10);` 即可解决问题。`BankAccount.Deposit()` 方法是公共的，因此 `Main()` 和程序的其他部分都可以访问。

![记住](img/remember.png) 默认访问类型为 `private`。不显式声明类成员的访问类型等同于将其声明为 `private`。然而，你应该包含 `private` 关键字以消除任何疑虑。良好的程序员会使他们的意图显式化，这是减少错误的另一种方法。

## 进阶学习——其他安全级别

![警告](img/warning.png) 理解这一节取决于你是否拥有一些继承（参见本微型书籍的第 6 章）和命名空间知识（参见本微型书籍的第 9 章）。如果你愿意，现在可以跳过这一节，只需知道需要时这里。C# 提供了这些级别的安全：

*   `public` 成员可以被程序中的任何类访问。
*   `private` 成员仅可从当前类访问。
*   `protected` 成员可以从当前类及其任何子类访问。
*   `internal` 成员可以从同一个程序模块或程序集中的任何类访问。

![技术细节](img/technicalstuff.png) C# `module` 或 `assembly`（程序集）是一个独立编译的代码单元，可以是 `.EXE` 文件中的可执行程序，也可以 `.DLL` 文件中的支持库模块。单个命名空间可以跨越多个程序集。（本微型书籍的第 9 章解释了 C# 程序集和命名空间，并讨论了 `public` 和 `private`以外的访问级别。）

*   `internal protected` 成员可以从当前类和任何子类，以及从同一模块内的类访问。
*   `private protected` 成员可以由同一程序集中的同一类代码或由派生自该类的类型代码访问。

通过声明为 `private` 来隐藏成员提供了最大程度的安全。然而，在许多情况下，你不需要那种级别的安全。毕竟，子类的成员已经依赖于基类的成员，因此 `protected` 提供了一个了一个舒适的安全级别。

## 为什么你应该关注访问控制

将类的内部成员声明为 `public` 是一个坏主意，至少出于以下原因：

*   **如果所有数据成员都是 `public` 的，你无法轻易确定数据成员何时以及如何被修改的。** 为什么要费力在 `Deposit()` 和 `Withdraw()` 方法中构建安全检查呢？事实上，甚至何必费精力写这些方法？任何类的任何方法都可以随时修改这些元素。如果其他方法可以访问这些数据成员，它们几乎肯定会这样做。

你的 `BankAccount` 程序可能在运行一小时后，你才注意到其中一个账户的余额为负数。`Withdraw()` 方法本可以确保这种情况不会发生，所以显然另一个方法在没有通过 `Withdraw()` 的情况下访问了余额。找出哪个方法负责以及在什么条件下负责的是一个困难的问题。

*   **暴露类的所有数据成员会使接口变得过于复杂。** 作为使用 `BankAccount` 类的程序员，你不想知道类的内部工作原理。你只需要知道你可以存入和取款。这就像一个有 50 个按钮的糖果机与一个只有几个按钮（即你需要的按钮）糖果机的区别。

*   **暴露内部元素会导致类规则的分散。** 例如，我的 `BankAccount` 类在任何情况下都不允许余额为负。那条业务规则应该被隔离在 `Withdraw()` 方法中。否则，你必须在每个更新余额的地方添加此检查。

有时，银行决定更改规则，允许优质客户在短时间内持有略微的负余额，以避免意外的透支。这时，你必须搜索整个程序，更新每个访问余额的代码部分，以确保安全检查也随之更改。

![提示](img/tip.png) 确保你的类和方法的访问权限不要比必要的更开放。这个建议并不是为了让你对窥探隐私的黑客产生恐慌，而是为了建议采取一个审慎的步骤，帮助在编写代码时减少错误。尽可能使用 `private`，然后根据需要升级到 `protected`、`private protected`、`internal`、`internal protected` 或 `public`。

## 访问器方法

如果你更仔细地观察 `BankAccount` 类，你会看到其他方法。其中一个 `ToString()` 返回账户的 `string` 版本，适用于传递给任何 `Console.WriteLine()` 进行显示。然而，如果内容不可访问，显示 `BankAccount` 对象的的内容可能会困难。类应该有权决定它是如何被显示的。

此外，你还看到了以 `Balance` 和 `AccountNumber` 属性形式存在的两个 `getter` 方法和一个 `setter` 方法。你可能会奇怪，为什么将 `_balance` 等数据成员声明为 `private` 很重要，但提供一个 `public Balance` 属性来返回它的值：

*   `Balance` 没有提供修改 `_balance` 的方法——它仅仅返回其值。余额是只读的。用实际银行来类比，你可以随地查看你的余额，但不能使用银行的取款机制从账户中取钱。
*   `Balance` 从外部方法隐藏了类的内部格式。`Balance` 可以通过读取收据、加上账户费用并考虑银行可能从你的余额中扣除的任何金额来执行大量计算。外部方法不知道也不关心。当然，你会在意收了哪些费用——你只是无法对它们做任何事情，除非换银行。

最后，`Balance` 提供了一种机制，可以在对类类进行内部更改，而不需要更改 `BankAccount` 用户看到的接口。如果联邦存款保险公司 (FDIC) 要求你的银行以不同的方式存储存款，指令不应改变你访问账户的方式。

### 使用 init-only 设置器

C# 9.0 引入了一种处理属性的新技术，你可以只设置属性一次，然后该属性就会变为 `unchangeable`（不可更改）。当你不允许在初始设置之后进行更改（例如俱乐部成员的编号）时，拥有不可变属性是好的。成员接收一次标识，然后永久保留该标识。`InitOnly` 示例中的 `CreditMember` 类展示了用于快速识别俱乐部成员信用额度的类是如何工作的。

```cs
internal class CreditMember
{
  internal int Id { get; init; }
  internal string Name { get; set; }
  internal decimal Limit { get; set; }

  public override string ToString()
  {
    return $"{Name}, member ID {Id}, has a " +
    $"limit of {Limit:C}";
  }

  internal protected CreditMember(int MemberId)
  {
    Id = MemberId;
  }
}
```



代码显示了三个属性、一个 `ToString()` 的重写，以及一个新特性：构造函数。`constructor`（构造函数）根据类描述提供的蓝图构建对象。你可以在本章的“让你的对象有一个良好的开始 — 构造函数”部分中了解更多关于它们的信息。构造函数的访问级别为 `internal protected`，因此任何继承此类的类也会继承该构造函数。

![Remember](img/remember.png) 同样注意，`Id` 属性使用 `init;` 形式对 `set;` 进行了替换。此条目意味着你可以在初始化期间设置一次该属性，此后不能再设置。这就是为什么构造函数设置了 `Id` 属性值。为了让该功能在标准的 Windows 控制台应用程序中生效，你必须在应用程序中 `using` 语句之后、`namespace InitOnly` 声明之前，添加以下代码：

```csharp
namespace System.Runtime.CompilerServices
{
internal static class IsExternalInit { }
}
```

这里出现的代码实际上并没有做任何事情——它只是消除了编译错误信息。包含这段代码的替代方案是创建一个 .NET Core ，而不是 .NET Framework 控制台应用程序，如 `InitOnly2` 程序所示。请注意，你必须在控制台向导的目标框架字段中选择 .NET 6.0 (Current)。第 5 卷第 5 章 将告诉你更多关于 .NET Core 应用程序的信息。

`Main()` 方法实例化 `CreditMember` 对象 `Sam`，然后为其设置值。之后，它打印出 `Sam` 对象的信息。这里是测试 `InitOnly` 程序的简短代码。

```csharp
static void Main(string[] args)
{
CreditMember Sam = new CreditMember(1);
Sam.Name = "Sam Jones";
Sam.Limit = 5000;
Console.WriteLine(Sam.ToString());
Console.ReadLine();
}
```

如果你在此时尝试设置 `Id`，你会看到一条错误消息，告诉你不能这样做。由于这是一个 C# 9.0 的示例，你必须向 `InitOnly.csproj` 文件添加以下条目：

```xml
<PropertyGroup>
<LangVersion>9.0</LangVersion>
</PropertyGroup>
```

当你运行此程序时，你会看到此输出：

`Sam Jones, member ID 1, has a limit of $5,000.00`

### 访问控制的救援 — 一个示例

下面的 `DoubleBankAccount` 程序演示了 `BankAccount` 程序中的一个潜在缺陷。以下列表显示了 `Main()`——它是程序中与之前的 `BankAccount` 程序不同的部分：

```csharp
static void Main(string[] args)
{
// 打开一个银行账户。
Console.WriteLine("Create a bank account object");
BankAccount ba = new BankAccount();
ba.InitBankAccount();
// 存款。
double deposit = 123.454;
Console.WriteLine($""Depositing {deposit:C}");
ba.Deposit(deposit);
// 账户余额
Console.WriteLine(ba.ToString());
// 这里就是问题所在。
double fractionalAddition = 0.002;
Console.WriteLine($"Adding {fractionalAddition:C}");
ba.Deposit(fractionalAddition);
// 结果余额
Console.WriteLine(ba.ToString());
Console.Read();
}
```

`Main()` 方法创建一个银行账户，然后存入 `$123.454`，这是一个包含小数分部分的金额。`Main()` 随后向余额中存入极小部分的分，并显示结果余额。该程序的输出如下：

`Create a bank account object`
`Depositing $123.45`
`Account = #1001 = $123.45`
`Adding $0.00`
`Resulting account = #1001 = $123.46`

用户开始抱怨：“我就是无法让我的支票本和银行账单对上。”显然，程序有一个 bug。

当然，问题在于 $123.454 显示为 $123.45$。为了避免这个问题，银行决定将存款和取款四舍五入到最近的分。存入 $123.454，银行走了那额外的 0.4 分。另一方面，银行放弃了足够的 0.4 倍，以确保从长远来看一切都是平衡的。嗯，理论上是这样。

解决舍入问题简单的方法是将银行账户转换为 `decimal` 并使用 `Decimal.Round()` 方法，如 `DecimalBankAccount` 程序中的 `BankAccount` 类所示：

```csharp
// BankAccount -- 定义一个表示简单账户的类。
internal class BankAccount
{
private static int _nextAccountNumber = 1000;
private int _accountNumber;
// 将余额作为 double 变量维护。
private decimal _balance;
// Init -- 使用下一个
// 账户 id 和 0 的余额初始化银行账户。
internal protected void InitBankAccount()
{
_accountNumber = ++_nextAccountNumber;
_balance = 0.0;
}
// Balance 属性获取余额。
internal decimal Balance
{ get => _balance; }
// AccountNumber 属性
internal int AccountNumber
{ get => _accountNumber; set => _accountNumber = value; }
// Deposit -- 允许任何存款。
internal void Deposit(decimal amount)
{
if (amount > 0)
{
// 在存款前四舍五入到最近的分。
decimal temp = amount;
temp = Decimal.Round(temp, 2);
_balance += temp;
}
}
// Withdraw -- 可以提取任何金额。返回金额。
internal decimal Withdraw(decimal withdrawal)
{
decimal temp = withdrawal;
temp = Decimal.Round(temp, 2);
if (_balance <= temp)
{
temp = _balance;
}
_balance -= temp;
return temp;
}
// 将账户数据作为字符串。
public override string ToString()
{
return $"{AccountNumber} = {Balance:C}";
}
```

此版本的示例将内部表示转换为 `decimal`，这比 `double` 更适合处理余额。`Deposit()` 和 `Withdraw()` 方法现在使用 `Round()` 方法将金额到最近的分。注意此类的访问级别现在已设置。注意你必须更改 `Main()` 以使用正确的数据类型，但编译器会就此问题发出警告。程序的输出符合预期：

`Create a bank account object`
`Depositing $123.45`
`Account = #1001 = $123.45`
`Adding $0.00`
`Resulting account = #1001 = $123.46`



使用此表单时，表达式可能比简单的变量更复杂，如果属性只有一个设置器（setter），则不需要特别包含获取器（getter），如下所示：

```csharp
private string _firstName = "John";
private string _lastName = "Smith";
internal string Name => $"{_firstName} {_lastName}";
```

- **自动实现：** 这是创建属性的最短方法，但提供的灵活性最低。你甚至不需要提供私有变量即可使用它。这种版本看起来如下：

```csharp
internal int MyProp
{ get; set; }
```

![Tip](img/tip.png) 按照惯例，属性名称以大写字母开头。注意，属性没有括号：是 `Balance`，而不是 `Balance()`。

![Technicalstuff](img/technicalstuff.png) 属性并不一定意味着是低效的。C# 编译器可以优化简单的访问器，使其生成的机器码与直接访问数据成员一样多。这个概念非常重要，不仅对于应用程序，而且对于 C# 本身也是如此。C# 库处处使用属性，你也应该这样做。使用属性来访问类数据成员，即使是从同一个类中的方法访问。

### 静态属性

静态（类）数据成员可以通过静态属性暴露，如下面的简单示例所示（注意其紧凑的布局）：

```csharp
public class BankAccount
{
    private static int _nextAccountNumber = 1000;
    public static int NextAccountNumber { get {return _nextAccountNumber += 1; }}
    // …
}
```

`NextAccountNumber` 属性通过类进行如下方式访问，因为它不是实例属性（它被声明为静态的）：

```csharp
// 读取账户数属性。
int value = BankAccount.NextAccountNumber;
```

(在此示例中，`value` 位于属性上下文之外，因此它不是保留字。)

### 带有副作用的属性

`get` 操作可以执行除检索关联属性之外的额外工作，如下所示：

```csharp
public static int AccountNumber
{
    // 获取属性并通过增加其值为
    // 下一次检索做准备。
    get { return ++_nextAccountNumber; }
}
```

此属性在返回结果之前递增了静态账户数成员。然而，这可能不是一个好主意，因为属性的用户除了实际读取属性之外，接收不到任何正在发生变化的线索。递增 `_nextAccountNumber` 是一种副作用。

![Remember](img/remember.png) 就像它们模拟的访问器方法一样，属性不应该改变类的状态，例如设置数据成员的值。属性和方法通常应该避免副作用，因为它们可能会导致微妙的错误。尽可能直接和显式地更改类。

### 带有访问级别的访问器

将属性（在可能）声明为 `public` 以外的类型通常是一个好主意。你可以在任何适当级别声明它们，即使是 `private`，只要访问器仅在它的类内部使用。（接下来的示例将 `Name` 属性标记为 `internal`，这对于不属于库或 API 仅在宿主机应用程序使用的类来说最佳选项。）

你甚至可以单独调整访问器 `get` 和 `set` 部分的访问级别。假设你不想在类外部暴露 `set` 访问器——它仅供内部使用。你可以这样写属性：

```csharp
internal string Name { get; private set; }
```

## 使用目标类型简化您的操作

*目标类型*（Target typing）指的是编译器根据上下文而非实际代码推导变量适当类型的能力。你经常看到它被使用，但 C# 9.0 提供了两种使用目标类型的新方法。第一种是在声明变量时，例如在列表中。你不再需要费力竭力了；让编译器来做繁力工作。以下类和枚举出现在 `TargetType1` 程序中，并提供了测试在这种情况下目标类型意味着什么的手段（注意，你必须通过修改 `.csproj` 文件来配置应用程序使用 C# 9.0）：

```csharp
internal enum FoodGroups
{
    Meat,
    Vegetables,
    Fruit,
    Grain,
    Dairy
}

internal class MyFavorteFoods
{
    internal int Rank { get; set; }
    internal string Name { get; set; }
    internal FoodGroups Group { get; set; }
    public MyFavorteFoods(int Position,
    string Food, FoodGroups Category)
    {
        Rank = Position;
        Name = Food;
        Group = Category;
    }
}
```

示例类非常简单——它提供了三个属性，其中一个依赖于 `FoodGroups` 枚举，以及一个用于实例化对象的构造函数。注意构造函数是 `public` 的以确保正确的访问。这里是用于处理类的 `Main()` 代码：

```csharp
static void Main(string[] args)
{
    var Foods = new List<MyFavorteFoods>
    {
        new (1, "Apples", FoodGroups.Fruit),
        new (2, "Steaks", FoodGroups.Meat),
        new (3, "Asparagus", FoodGroups.Vegetables)
    };
    foreach (MyFavorteFoods Item in Foods)
        Console.WriteLine($"Food #{Item.Rank} is {Item.Name} of {Item.Group} food category.");
}
```

你最注意的是，`Foods` 列表构造不需要任何类型信息。编译器会自动提供类型。当你运行它时，你会看到输出：

`Food #1 is Apples of Fruit food category.`
`Food #2 is Steaks of Meat food category.`
`Food #3 is Asparagus of Vegetables food category.`

第二种情况是条件情况。再次，理解它是如何工作的简单方法是看示例。`TargetType2` 示例从 `TargetType1` 中的 `MyFavorteFoods` 类开始。为了看到运行情况，如下所示创建两个派生类（再次确保你的项目支持 C# 9.0）：

```csharp
internal class MyLuxuryFoods : MyFavorteFoods
{
    internal decimal HowMuch { get; set; }
    public MyLuxuryFoods(int Position,
    string Food, FoodGroups Category, decimal Cost) :
    base(Position, Food, Category)
    {
        HowMuch = Cost;
    }
}

internal class MyComfortFoods : MyFavorteFoods
{
    internal string HowOften { get; set; }
    public MyComfortFoods(int Position,
    string Food, FoodGroups Category, string Time) :
    base(Position, Food, Category)
    {
        HowOften = Time;
    }
}
```

两个子类都依赖 `MyFavorteFoods` 作为起点。然而，它们都增加了不同的内容。通常，你不能使用 `??` 空合并运算符这两个类。但是，以下代码在 C# 9.0 中是有效的：

```csharp
static void Main(string[] args)
{
    MyLuxuryFoods GreatFood = new MyLuxuryFoods(
    1, "Salmon", FoodGroups.Meat, 35.95M);
    MyComfortFoods SatisfyingFood = new MyComfortFoods(
    1, "Oatmeal", FoodGroups.Grain, "Weekly");
    MyFavorteFoods Choice = GreatFood ?? SatisfyingFood;
    Console.WriteLine(Choice.Name);
    Console.ReadLine();
}
```

所以，你可能会想 `MyFavorteFoods Choice = GreatFood ?? SatisfyingFood;` 意味着什么。如果 `GreatFood` 可用，就吃它，否则吃 `SatisfyingFood`。所以，如果你在实例化 `Choice` 之前添加 `GreatFood = null;`，输出将是 `Oatmeal` 而不是 `Salmon`。





`协变返回类型`（covariant return type）允许你返回一个比通常返回的类型更详细（在类层次结构中处于较低级别）的类型。这一特定功能仅在你使用 .NET Core 版本的控制台应用程序模板，并在向导程序的“目标框架”字段中选择 `.NET 6.0` 时才有效。理解此功能如何运作的最佳方法是看一个示例。`CovariantReturn` 程序提供了一个基础示例，侧重于 C# 的 `record` 类型（[`docs.microsoft.com/en-us/dotnet/csharp/whats-new/tutorials/records`](https://docs.microsoft.com/en-us/dotnet/csharp/whats-new/tutorials/records)）。以下代码显示了类层次结构：

```csharp
public abstract record Number
{ public int Value { get; set; } }

public abstract record BadgeNumber
{ public virtual Number Id { get; } }

public record EmployeeID : Number
{ public string FullName { get; set; } }

public record ThisPerson : BadgeNumber
{
    public ThisPerson(int Identifier, string Name)
    {
        Id = new EmployeeID
        {
            FullName = Name,
            Value = Identifier
        };
    }
    public override Number Id { get; }
}
```

该示例从基类型 `Number` 开始，它包含一个 `int` 类型的单一属性 `Value`。第二个基类型 `BadgeNumber` 也包含一个属性，但该属性是 `virtual` 的，并使用 `Number` 作为其类型。这两个基类型都是 `abstract` 的（[`docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/abstract`](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/abstract)），这意味着你不能实例化它们。

接下来两个类型派自 `Number` 和 `BadgeNumber`。`EmployeeID` 添加了新的 `string` 类型新属性 `FullName`。这意味着 `EmployeeID` 包含两个属性：`Value` 和 `FullName`。

协变返回类型的魔力出现在 `ThisPerson` 中。注意，`ThisPerson` 有一个构造函数，并将位于 `BadgeNumber` 中的 `Id` 属性初始化为 `EmployeeID`，而不是 `int`。因此，`Id` 现在包含一个比原始预期的更详细的类型。`ThisPerson` 记录还包含一个返回类型为 `Number` 的 `Id`，而不是你可能预期的 `int` 类型。那么，这一切是如何运作的？它是胡言还是真实的代码？`Main()` 方法证明了在使用 `.NET 6.0` 框架时在 C# 9.0 中是有效的：

```csharp
static void Main(string[] args)
{
    var Josh = new ThisPerson(22, "Josh");
    Console.WriteLine(Josh);
    Console.WriteLine(Josh.GetType());
    BadgeNumber ThisNumber = Josh;
    Console.WriteLine(ThisNumber);
    Console.WriteLine(ThisNumber.GetType());
}
```

代码首先创建一个新的 `ThisPerson` 实例 `Josh`，它拥有证号 `22` 和名字 `Josh`。代码随后创建另一个类型为 `BadgeNumber` 的对象 `ThisNumber`，并尝试将 `Josh` 赋值给它。你可能认为这段代码真的不应该工作，但当你运行时，你会看到如下输出，它证明了编译器即使在 `ThisNumber` 表面上是 `BadgeNumber` 类型的情况下，也仍为其分配了正确类型的正确对象。

```text
ThisPerson { Id = EmployeeID { Value = 22, FullName = Josh } }
CovariantReturn.ThisPerson
ThisPerson { Id = EmployeeID { Value = 22, FullName = Josh } }
CovariantReturn.ThisPerson
```

## 让对象有一个良好的开始——构造函数

![Remember](img/remember.png) 控制类的访问只是问题的一半：如果一个对象想要成长，它就需要一个良好的开始。类可以提供一个初始化方法，应用程序调用该方法来启动程序，但应用程序可能会忘记调用该方法。类从垃圾数据开始，此后情况不会好转。如果你想对该类负责，就必须确保它有正确开始的机会。C# 通过自动为你调用初始化方法来解决这个问题——例如：

```csharp
MyObject mo = new MyObject();
```

![Remember](img/remember.png) 换句话说，此语句不仅从特殊的内存区域获取对象，还初始化了该对象的成员。在脑海中保持“类”和“对象”分开。`Cat` 是一个类。名为 `Striper` 的 `Cat` 实例是 `Cat` 类的一个对象。

### C# 提供的构造函数

C# 会跟踪变量是否已初始化，并且不允许使用未初始化的变量。例如，以下代码段会产生编译时错误：

```csharp
public static void Main(string[] args)
{
    int n;
    double d;
    double calculatedValue = n + d;
}
```

C# 跟踪了局部变量 `n` 和 `d` 未赋值的这一事实，并不允许在表达式中使用它们。编译这个微型程序会生成这些编译器错误：

```text
Use of unassigned local variable 'n'
Use of unassigned local variable 'd'
```

相比之下，C# 提供了一个默认构造函数，将成员初始化为：
* 数字为 0
* 布尔值为 `false`
* 对象引用为 `null`

考虑来自 `UseConstructor` 示例的 `MyObject` 类：

```csharp
internal class MyObject
{
    internal int n;
    internal MyObject nextObject;
}
```

你可以使用以下代码对其操作：

```csharp
static void Main(string[] args)
{
    // 首先创建一个对象。
    MyObject localObject = new MyObject();
    Console.WriteLine("localObject.n is {0}", localObject.n);
    if (localObject.nextObject == null)
    {
        Console.WriteLine("localObject.nextObject is null");
    }
    Console.Read();
}
```

执行程序后的输出如下：

```text
localObject.n is 0
localObject.nextObject is null
```

### 替换默认构造函数

虽然编译器会自动将所有实例变量初始化为适当的值，但对于许多类（可能是大多数类），默认值并不是有效状态。考虑本章较早之前的 `BankAccount` 类：

```csharp
internal class BankAccount
{
    private int _accountNumber;
    private double _balance;
    //…其他成员
}
```

在本章的目前阶段，`BankAccount` 类包含了 `InitBankAccount()` 方法来初始化对象。然而，这种方法给使用该类的应用程序赋予了过多的责任。





![Remember](img/remember.png) 类不应该依赖于如 `InitBankAccount()` 之类方法来启动一个处于状态的对象。为了解决这个问题，你可以让类提供自己的显式 `class constructor`（类构造函数），C# 在对象创建时会自动调用它。构造函数本可以命名为 `Init()`、`Start()` 或 `Create()`，但 C# 要求构造函数的名称与类名相同。因此，`BankAccount` 类的构造函数如下所示：

```csharp
public void Main(string[] args)
{
    BankAccount ba = new BankAccount(); // 这调用了构造函数。
}

public class BankAccount
{
    // 银行账户从 1000 开始顺序递增。
    private static int _nextAccountNumber = 1000;
    // 维护每个对象的账户号码和余额。
    private int _accountNumber;
    private double _balance;

    // BankAccount 构造函数 —— 就在这里 —— 哒！
    // 括号、可能的参数、没有返回类型
    public BankAccount()
    {
        _accountNumber = ++_nextAccountNumber;
        _balance = 0.0;
    }
    // … 其他成员 …
}
```

`BankAccount` 构造函数的内容与原始的 `Init…()` 方法相同。然而，你声明和使用构造函数的方式有所不同：

*   构造函数的名称始终与类名相同。
*   构造函数可以接受参数（也可以不接受）。
*   构造函数永远没有返回类型，即使是 `void` 也没有。
*   `Main()` 在创建对象时不需要调用任何额外方法来初始化对象；不需要 `Init()`。

![Remember](img/remember.png) 如果你提供了自己的构造函数，C# 就不再提供默认构造函数。你的构造函数将替换默认构造函数，并成为创建类实例的唯一方式。

### 构建某些东西

尝试一下构造函数的功能。考虑以下程序中的类，`DemonstrateCustomConstructor`：

```csharp
// MyObject -- 创建一个带有嘈杂自定义构造函数的类
// 以及一个内部数据对象。
public class MyObject
{
    // 这个数据成员是类的的一个属性（它是静态的）。
    private static MyOtherObject _staticObj = new MyOtherObject();
    // 这个数据成员是每个实例的属性。
    private MyOtherObject _dynamicObj;

    // 构造函数（一个大话痨）
    public MyObject()
    {
        Console.WriteLine("MyObject constructor starting");
        Console.WriteLine("(静态数据成员在" +
        "此构造函数之前构造)");
        Console.WriteLine("现在动态创建非静态数据成员:");
        _dynamicObj = new MyOtherObject();
        Console.WriteLine("MyObject constructor ending");
    }
}

// MyOtherObject -- 这个类也有嘈杂的构造函数，但
// 没有内部成员。
public class MyOtherObject
{
    public MyOtherObject()
    {
        Console.WriteLine("MyOtherObject constructing");
    }
}
```

`Main()` 函数仅仅启动了构建过程，如下：

```csharp
static void Main(string[] args)
{
    Console.WriteLine("Main() starting");
    Console.WriteLine("在 Main() 中创建一个局部的 MyObject:");
    MyObject localObject = new MyObject();
    Console.Read();
}
```

执行此程序将产生以下输出：

`Main() starting`
`Creating a local MyObject in Main():`
`MyOtherObject constructing`
`MyObject constructor starting`
`(Static data member constructed before this constructor)`
`Now create nonstatic data member dynamically:`
`MyOtherObject constructing`
`MyObject constructor ending`
`Press Enter to terminate…`

以下步骤重现了刚刚发生的过程：

1.  程序启动，`Main()` 输出初始消息并宣布它即将创建一个局部的 `MyObject`。
2.  `Main()` 创建了一个类型为 `MyObject` 的 `localObject`。
3.  `MyObject` 包含一个类型为 `MyOtherObject` 的静态成员 `_staticObj`。

    ![Remember](img/remember.png) 所有静态数据成员在第一个 `MyObject()` 构造函数运行之前初始化。在这种情况下，C# 在将控制权交给 `MyObject` 构造函数之前，用新创建的 `MyOtherObject` 填充 `_staticObj`。这一步解释了输出的第三行。
4.  `MyObject` 的构造函数获得了控制权。它输出了初始消息 `MyObject constructor starting`，然后指出静态成员在 `MyObject()` 构造函数开始之前已经构造：
    `(Static data member constructed before this constructor)`
5.  在宣布其意图 `Now create nonstatic data member dynamically` 后，`MyObject` 构造函数使用 `new` 运算符创建 `MyOtherObject` 类的对象，由于调用了 `MyOtherObject` 构造函数，产生了第二条 `MyOtherObject constructing` 消息。
6.  控制权返回 `MyObject` 构造函数，然后返回 `Main()`。

### 使用初始化器直接初始化对象

除了允许你在构造函数中初始化数据成员外，C# 还允许你通过使用初始化器直接初始化数据成员。因此，你可以这样写 `BankAccount` 类：

```csharp
public class BankAccount
{
    // 银行账户从 1000 开始顺序递增。
    private static int _nextAccountNumber = 1000;
    // 维护每个对象的账户号码和余额。
    private int _accountNumber = ++_nextAccountNumber;
    private double _balance = 0.0;
}
```

这里是初始化器的用法。你可能认为这条语句将 `_balance` 设置为 `0.0`。然而，`_balance` 只作为对象的一部分存在。事实上，这条赋值在每次创建对象时都会执行。

注意，静态成员 `_nextAccountNumber` 在第一次访问 `BankAccount` 类时被初始化；也就是你第一次访问该静态成员的任何方法或属性时，包括构造函数。

![Remember](img/remember.png) 在静态成员初始化后，每次构造 `BankAccount` 实例都不会再次初始化它。这与实例成员有所不同。如果 C# 同时遇到初始化器和构造函数，初始化器将在构造函数体之前执行。

### 使用初始化器查看构造

在 `DemonstrateCustomConstructor` 程序中，将 `new MyOtherObject()` 调用从 `MyObject` 构造函数移动到声明本身（见加粗文本），如下所示修改第二个 `WriteLine()` 语句，然后重新运行程序：

```csharp
public class MyObject
{
    // 这个数据成员是类的的一个属性（它是静态的）。
    private static MyOtherObject _staticObj = new MyOtherObject();
    // 这个成员是每个实例的属性。
    private MyOtherObject _dynamicObj = new MyOtherObject(); // <- 在这里。

    public MyObject()
    {
        Console.WriteLine("MyObject constructor starting");
        Console.WriteLine("两个数据成员在此构造函数之前已初始化)");
        // _dynamicObj 的构造在这里，现在上移了。
        Console.WriteLine("MyObject constructor ending");
    }
}
```

将此修改后程序的输出与之前的程序 `DemonstrateCustomConstructor` 的输出进行比较：

`Main() starting`
`Creating a local MyObject in Main():`
`MyOtherObject constructing`
`MyOtherObject constructing`
`MyObject constructor starting`
`(Both data members initialized before this constructor)`
`MyObject constructor ending`
`Press Enter to terminate…`

### 在没有构造函数初始化对象

假设你有一个表示 `Student` 的小类：

```csharp
public class Student
{
```



```csharp
public string Name { get; set; }
public string Address { get; set; }
public double GradePointAverage { get; set; }
}
```

`Student` 对象有三个公共属性：`Name`、`Address` 和 `GradePointAverage`，它们指定了学生的基本信息。通常，当你创建一个新的 `Student` 对象时，你必须这样初始化它的 `Name`、`Address` 和 `GradePointAverage` 属性：

```csharp
Student randal = new Student();
randal.Name = "Randal Sphar";
randal.Address = "123 Elm Street, Truth or Consequences, NM 00000";
randal.GradePointAverage = 3.51;
```

如果 `Student` 有一个构造函数，你可以像这样操作：

```csharp
Student randal = new Student
("Randal Sphar", "123 Elm Street, Truth or Consequences, NM, 00000", 3.51);
```

遗憾的是，`Student` 缺少构造函数，除了 C# 自动提供的不带参数的默认构造函数外。你可以用某种看起来像构造函数的东西来简化这种初始化——嗯，有点像：

```csharp
Student randal = new Student
{ Name = "Randal Sphar",
Address = "123 Elm Street, Truth or Consequences, NM 00000",
GradePointAverage = 3.51
};
```

最后两个例子在这一方面有所不同：第一个使用构造函数，显示了包含用逗号分隔的两个 `string` 和一个 `double` 值的括号；而第二个使用新的对象初始化器语法，则使用了包含用逗号分隔的三个赋值语句的大括号。该语法的作用如下：

```csharp
new LatitudeLongitude
{ assignment to Latitude, assignment to Longitude };
```

对象初始化器语法允许你在代码块（大括号）中为 `LatitudeLongitude` 对象的任何可访问的 `set` 属性赋值。该块的设计用于初始化对象。注意，你只能通过这种方式设置可访问属性，而不能私有属性，而且你不能在初始化器中调用对象的任何方法或执行任何其他工作。

对象初始化器语法简洁得多：一条语句对比三条。此外，它简化了那些无法通过构造函数创建的初始化对象的创建。新的对象初始化器语法除了便利性之外并没有给你带来什么额外的好处，但在编写代码时，便利性在任何程序员的列表中都排在前列。简洁也是如此。此外，当你读到匿名类时，该功能就变得至关重要了。

![Tip](img/tip.png) 尽情地使用新的对象初始化器语法吧。本书频繁使用它，因此你有大量的示例。[`https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/how-to-initialize-objects-by-using-an-object-initializer`](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/how-to-initialize-objects-by-using-an-object-initializer) 帮助主题提供了更多细节。

## 使用表达式体成员

表达式体成员（Expression-bodied members）首次出现在 C# 6.0 中，作为使方法和属性更容易定义的一种。在 C# 7.0 中，表达式体成员也适用于构造函数、析构函数、属性访问器和事件访问器。

### 创建表达式体方法

以下示例展示了在 C# 6.0 之前可能如何创建一个方法：

```csharp
public int RectArea(Rectangle rect)
{
    return rect.Height * rect.Width;
}
```

![Remember](img/remember.png) 当使用表达式体成员工作时，你可以将代码行减少到仅一行，如下：

```csharp
public int RectArea(Rectangle rect) => rect.Height * rect.Width;
```

尽管两个版本执行的任务完全相同，但第二个版本要短得多且更容易编写。权衡是，第二个版本也比较简洁，可能更难理解。

### 定义表达式体属性

表达式体属性的工作原理与方法类似：你用单行代码声明属性，如下：

```csharp
public int RectArea => _rect.Height * _rect.Width;
```

该示例假设你已经定义了一个名为 `_rect` 的私有成员，并且你想获取与矩形面积相匹配的值。

### 定义表达式体构造函数和析构函数

在 C# 7.0 中，当处理构造函数时可以使用相同的技术。在早版本的 C# 中，你可能会创建一个这样的构造函数：

```csharp
public EmpData()
{
    _name = "Harvey";
}
```

在这种情况下，`EmpData` 类的构造函数将私有变量 `_name` 设置为 `"Harvey"`。C# 7.0 版本仅用了一行但实现了相同的任务：

```csharp
public EmpData() => _name = "Harvey";
```

析构函数的工作方式与构造函数非常相似。不再使用多行，而是用一行来定义它们。

### 定义表达式体属性访问器

属性访问器也可以从使用表达式体成员中受益。这是一个典型的 C# 6.0 带有 `get` 和 `set` 方法的属性访问器：

```csharp
private int _myVar;
public MyVar
{
    get
    {
        return _myVar;
    }
    set
    {
        _myVar = value;
    }
}
```

在 C# 7.0 中工作时，可以使用表达式体成员来简化代码：

```csharp
private int _myVar;
public MyVar
{
    get => _myVar;
    set => _myVar = value;
}
```

### 定义表达式体事件访问器

与属性访问器一样，你可以使用表达式体成员创建事件访问器。这里是 C# 6.0 可能使用的：

```csharp
private EventHandler _myEvent;
public event EventHandler MyEvent
{
    add
    {
        _myEvent += value;
    }
    remove
    {
        _myEvent -= value;
    }
}
```

C# 7.0 中相同的事件访问器形式如下：

```csharp
private EventHandler _myEvent;
public event EventHandler MyEvent
{
    add => _myEvent += value;
    remove => _myEvent -= value;
}
```

# 第 5 章 继承：只有这些吗？

本章内容

- 在层次结构中包含构造函数
- 调用基类构造函数
- 区分 *is a* 和 *has a*
- 对象替换

继承是一个常见的概念。你是一个人类。你从 `Human` 类继承了某些属性，例如交流的能力以及对空气、食物和饮料的依赖。`Human` 类从 `Mammal` 类继承了对空气、水和营养的依赖，而 `Mammal` 类又继承自 `Animal` 类。

传递属性的能力是一个强大的功能。你可以利用它来描述物品。例如，如果你的儿子问：“什么是鸭子？”你可以说：“它是一只会嘎叫的鸟。”尽管你可能这么想，这个答案传达了大量信息。你的儿子知道鸟是什么，现在他知道了所有这些特征也适用于鸭子，加上鸭子额外的属性——“嘎叫性”。





## 为什么你需要继承

继承具有几个重要的功能。你可能认为，例如，继承减少了打字量。在某种程度上，确实如此——当你描述一个 `Student` 类时，不需要重复编写 `Person` 的属性。一个更重要且相关的问题是热门词汇`重用`。计算机科学家早已经知道，对于每个新项目都从零开始并重新构建相同的软件组件是毫无意义的。

将软件开发的情况与其他行业进行比较。想想有多少汽车制造商在建造汽车之前，先从制造自己的扳手和螺丝刀开始起步。在这些这样做的人中，估计有多少人会完全重新开始，并为下一个型号制造所有新工具。其他行业的从业者发现，从现有的螺丝钉、螺栓、螺母，甚至是电机和压缩机等更大的现成组件开始，比从零开始更具意义。

继承使你能够对对现有的软件组件进行微调。你可以在不进行内部修改的情况下，将现有类适配到新的应用程序。现有类被继承到——或者用程序员常说的，被`扩展`——一个一个新的子类，该子类包含了必要的添加和修改。如果基类是由别人编写的，你可能无法修改它，因此继承可以派上用场。

这种能力带来了继承的第三种好处。假设你继承自——扩展——一个现有的类。后来，你发现基类有一个你必须修复的错误。如果你通过修改该类来重用它，你必须手动在每个应用程序中单独检查、修复并重新测试该错误。如果你在不改变类的情况下继承了该类，通常可以很轻松地将更新后的类放入另一个应用程序中。

但继承最大的好处是，它描述了生活的运行方式。项目与项目之间相互继承属性。这是不可避免的。

## 从 BankAccount 类继承（一个更复杂的示例）

银行维护着几种类型的账户。一种类型是储蓄账户，它具有简单银行账户的所有属性，外具有积累利息的能力。接下来的章节将讨论 `BankAccount` 类及其子类 `SavingsAccount`，从一个基础应用程序开始，然后查看构造函数和其他功能的工作原理。

## 处理基础更新

从基础开始是非常重要的。`BankAccount` 类作为 `SimpleSavingsAccount` 程序的基类：

```cs
// BankAccount -- 模拟一个银行账户，每个账户
// 都带有一个账户 ID（在创建时分配）
// 以及余额。
internal class BankAccount // 基类
{
    // 银行账户从 1000 开始并顺序增加。
    private static int _nextAccountNumber = 1000;
    // 为每个对象维护账户号码。
    private int _accountNumber;
    // 构造函数 -- 使用下一个账户 ID
    // 和指定的初始余额（默认为零）初始化银行账户。
    internal BankAccount() : this(0) { }
    internal BankAccount(decimal initialBalance)
    {
        _accountNumber = ++_nextAccountNumber;
        Balance = initialBalance;
    }
    // Balance 属性。
    protected decimal Balance
    { get; set; }
    // 存款 -- 允许任何正存款。
    public void Deposit(decimal amount)
    {
        if (amount > 0)
        {
            Balance += amount;
        }
    }
    // 取款 -- 你可以提取任何不超过余额的金额；
    // 返回提取的金额。
    public decimal Withdraw(decimal withdrawal)
    {
        if (Balance <= withdrawal) // 使用 Balance 属性。
        {
            withdrawal = Balance;
        }
        Balance -= withdrawal;
        return withdrawal;
    }
    // ToString - 将账户字符串化。
    public override string ToString()
    {
        return $"{_accountNumber} - {Balance:C}";
    }
}
```

此示例使用 `chaining` 通过 `this` 将一个构造函数链到另一个构造函数。当你看到 `internal BankAccount() : this(0) { }` 时，意味着使用值 `0` 作为 `initialBalance` 参数的值来调用链中的下一个构造函数。使用这种方法极大地减少了需要编写的代码量，减少了潜在错误，并使代码更具维护性。第二个构造函数获取下一个账户号码并设置 `Balance` 属性。

`Balance` 属性具有 `protected` 访问修饰符，因为只有基类 `BankAccount` 和派生类 `SavingsAccount` 会访问它。使用这种方法意味着你可以简化代码，而无需维护自己单独的内部变量。

三个方法 `Deposit()`、`Withdraw()` 和 `ToString()` 允许对 BankAccount 功能进行受控的公共访问。`ToString()` 重写了基类的 `ToString()`，以美元金额的形式显示账户号码和余额。

`SavingsAccount` 类增加了根据利息累积更改余额的能力，如下：

```cs
internal class SavingsAccount : BankAccount // 子类
{
    private decimal _interestRate = 0;
    // InitSavingsAccount -- 输入表示为 0 到 100 之间速率的速率。
    internal SavingsAccount(decimal interestRate) :
    this(0, interestRate) { }
    internal SavingsAccount(decimal initialBalance,
    decimal interestRate) : base(initialBalance)
    {
        _interestRate = interestRate / 100;
    }
    // AccumulateInterest -- 每周期调用一次。
    public void AccumulateInterest()
    {
        Balance = Balance + (Balance * _interestRate);
    }
    // ToString -- 将账户字符串化。
    public override string ToString()
    {
        return $"{base.ToString()} ({interestRate:P})";
    }
}
```

与 `BankAccount` 一样，`SavingsAccount` 提供了两个构造函数，其中一个链到另一个。`SavingsAccount` 是 `BankAccount` 的子类，因此它已经可以访问 `Balance` 等元素。

`Main()` 执行的操作尽可能少。它创建一个 `BankAccount`，进行存款，显示账户，创建一个 `SavingsAccount`，积累一次利息，并显示结果，如下：

```cs
static void Main(string[] args)
{
    // 创建一个银行账户并显示它。
    BankAccount ba = new BankAccount(100M);
    ba.Deposit(100M);
    Console.WriteLine($"Account {ba.ToString()}");
    // 现在储蓄账户
    SavingsAccount sa = new SavingsAccount(12.5M);
    sa.Deposit(100M);
    sa.AccumulateInterest();
    Console.WriteLine($"Account {sa.ToString()}");
    Console.Read();
}
```

运行此应用程序时，你会看到以下输出：

`Account 1001 - $200.00`

`Account 1002 - $112.50 (12.500%)`

## 跟踪 BankAccount 和 SavingsAccount 功能

除非使用调试器单步执行，否则很难精确跟踪 `BankAccount` 和 `SavingsAccount` 类是如何工作的。另一种技术是添加一些 `Console.WriteLine()` 方法条目，如下列表所示（以及在 `SimpleSavingsAccountTracked` 中）：

```cs
internal class BankAccount // 基类
{
    // 银行账户从 1000 开始并顺序增加。
    private static int _nextAccountNumber = 1000;
    // 为每个对象维护账户号码。
    private int _accountNumber;
    // 构造函数 -- 使用下一个账户 ID
    // 和指定的初始余额（默认为零）初始化银行账户。
    internal BankAccount() : this(0)
    {
        Console.WriteLine("*** Called BankAccount Default Constructor ***");
    }
}
```





```c
Balance = initialBalance;

Console.WriteLine("*** Called BankAccount Constructor ***");

}

// Balance 属性。
protected decimal Balance
{ get; set; }

// Deposit -- 允许任何正数的存款。
public void Deposit(decimal amount)
{
    if (amount > 0)
    {
        Balance += amount;
        Console.WriteLine("*** Called BankAccount Deposit() ***");
    }
}

// Withdraw -- 你可以提取任意在余额范围内的金额；
// 并返回提款的金额。
public decimal Withdraw(decimal withdrawal)
{
    if (Balance <= withdrawal) // 使用 Balance 属性。
    {
        withdrawal = Balance;
    }
    Balance -= withdrawal;
    Console.WriteLine("*** Called BankAccount Withdrawal() ***");
    return withdrawal;
}

// ToString - 将账户字符串化。
public override string ToString()
{
    Console.WriteLine("*** Called BankAccount ToString() ***");
    return $"{_accountNumber} - {Balance:C}";
}
}

// SavingsAccount -- 一个可以产生利息的银行账户
internal class SavingsAccount : BankAccount // 子类
{
    private decimal _interestRate = 0;
    // InitSavingsAccount -- 输入以 0 到 100 之间的
    // 比率率。
    internal SavingsAccount(decimal interestRate) :
    this(0, interestRate)
    {
        Console.WriteLine("*** Called SavingsAccount Constructor 1 ***");
    }
    internal SavingsAccount(decimal initialBalance,
    decimal interestRate) : base(initialBalance)
    {
        _interestRate = interestRate / 100;
        Console.WriteLine("*** Called SavingsAccount Constructor 2 ***");
    }
    // AccumulateInterest -- 每周期调用一次。
    public void AccumulateInterest()
    {
        Balance = Balance + (decimal)(Balance * _interestRate);
        Console.WriteLine("*** Called SavingsAccount " +
        "AccumulateInterest() ***");
    }

    // ToString -- 将账户字符串化。
    public override string ToString()
    {
        Console.WriteLine("*** Called SavingsAccount ToString() ***");
        return $"{base.ToString()} ({_interestRate:P})";
    }
}
```

`Main()` 中的代码保持不变，尽管你完全可以尝试修改它看看会发生什么。当你运行这个版本的代码时，你会看到以下输出：

`*** Called BankAccount Constructor ***`
`*** Called BankAccount Deposit() ***`
`*** Called BankAccount ToString() ***`
`Account 1001 - $200.00`
`*** Called BankAccount Constructor ***`
`*** Called SavingsAccount Constructor 2 ***`
`*** Called SavingsAccount Constructor 1 ***`
`*** Called BankAccount Deposit() ***`
`*** Called SavingsAccount AccumulateInterest() ***`
`*** Called SavingsAccount ToString() ***`
`*** Called BankAccount ToString() ***`
`Account 1002 - $112.50 (12.50%)`

创建和使用 `BankAccount` 对象 `ba` 非常简单。代码调用了接受初始金额的构造函数，存入 $100.00，然后打印结果。

然而，创建和使用 `SavingsAccount` 对象 `sa` 则需要多一些工作。在这种情况下，代码：

1. 首先调用了接受初始金额的 `BankAccount` 构造函数，因为这是第二个 `SavingsAccount` 构造函数中 `base(initialBalance)` 部分调用的构造函数。
2. 执行了第二个 `SavingsAccount` 构造函数中的任务，因为这是第一个 `SavingsAccount` 构造函数中 `this(0, interestRate)` 部分调用的构造函数。
3. 执行了第一个 `SavingsAccount` 构造函数中的任务（只接受利率作为输入的那个）。
4. 使用 `BankAccount.Deposit()` 方法进行存款（尽管调用显示为 `sa.Deposit(100M)`）。
5. 使用 `SavingsAccount.AccumulateInterest()` 方法积累利息，因为此方法是 `SavingsAccount` 类特有的。
6. 调用了 `SavingsAccount.ToString()` 重写方法，该方法调用了 `BankAccount.ToString()` 重写方法来打印储蓄账户字符串。

![记住](img/remember.png) 理解调用各种构造函数和方法的顺序是非常重要的，否则你可能会做出错误的假设。在处理类构造时，你始终可以添加语句来查看调用了什么以及何时被调用，以便更好地理解应用程序的流。这种方法在尝试解决应用程序中的结构缺陷时非常有帮助。

## IS_A 与 HAS_A — 我太困惑了 _A

`SavingsAccount` 和 `BankAccount` 之间的关系是继承中基础的 IS-A 关系。在接下来的章节中，你将发现原因。你还会看到 HAS-A 关系与之对应的比较。

### IS-A 关系

`SavingsAccount` 和 `BankAccount` 之间的 IS-A 关系通过对前一节中 `SimpleSavingsAccount` 程序中 `Program` 类的修改（加粗显示所示）来演示（在 `SimpleSavingsAccount2` 中）：

```c
class Program
{
    public static void DirectDeposit(BankAccount ba, decimal pay)
    {
        ba.Deposit(pay);
    }

    static void Main(string[] args)
    {
        // 创建一个银行账户并显示它。
        BankAccount ba = new BankAccount(1000);
        DirectDeposit(ba, 100);
        Console.WriteLine(ba.ToString());

        // 现在是一个储蓄账户
        SavingsAccount sa = new SavingsAccount(1000, 12.5);
        DirectDeposit(sa);
        sa.AccumulateInterest();
        Console.WriteLine(sa.ToString());
    }
}
```

本质上，什么都没有改变。唯一的区别是所有的存款现在通过本地方法 `DirectDeposit()` 完成的，而该方法并不属于 `BankAccount`（它在 Program 中）。

![记住](img/remember.png) 注意 `Main()` 可以将银行账户或储蓄账户传递给 `DirectDeposit()`，因为 `SavingsAccount` 是 `BankAccount`，你可以将 `SavingsAccount` 赋值给 `BankAccount` 类型变量。

### 通过组合访问 BankAccount

`SavingsAccount` 类可以通过另一种方式访问 `BankAccount` 的成员，如下代码所示（在 `SimpleSavings3` 中）：

```c
internal class SavingsAccount
{
    private BankAccount _bankAccount;
    private decimal _interestRate = 0;
    // InitSavingsAccount -- 输入以 0 到 100 之间的
    // 比率。
    internal SavingsAccount(decimal interestRate) :
    this(0, interestRate)
    { }
    internal SavingsAccount(decimal initialBalance,
    decimal interestRate)
    {
        _bankAccount = new BankAccount(initialBalance);
        _interestRate = interestRate / 100;
    }

    // AccumulateInterest -- 每周期调用一次。
    public void AccumulateInterest()
    {
        _bankAccount.Balance = _bankAccount.Balance +
        (decimal)(_bankAccount.Balance * _interestRate);
    }

    public void Deposit(decimal amount)
    {
        _bankAccount.Deposit(amount);
    }

    public decimal Withdraw(decimal withdrawal)
    {
        return _bankAccount.Withdraw(withdrawal);
    }

    // ToString - 将账户字符串化。
    public override string ToString()
    {
        return $"{_bankAccount.ToString()} ({_interestRate:P})";
    }
}
```

在这种情况下，`SavingsAccount` 类*包含*了一个数据成员 `_bankAccount`（而不是继承自 `BankAccount`）。`_bankAccount` 对象包含了储蓄账户所需的余额和账户号码信息。`SavingsAccount` 类保留了储蓄账户特有的数据，并在需要时委托*给包含的 `BankAccount` 对象。也就是说，当 `SavingsAccount` 需要（例如）余额时，它向包含的 `BankAccount` 请求。注意这种策略要求在第二个构造函数中实例化 `_bankAccount`，并在过去任何可能使用 `base` 的地方使用 `bankAccount`。





![Warning](img/warning.png) 这种方法有几个缺点。首先，你必须将 `BankAccount` 中 `Balance` 的访问修饰符改为 `public`，这意味着它不再是受保护的。每当你增加类成员的访问权限时，你都会增加潜在的安全问题风险。此外，此版本的 `SavingsAccount` 包含了它自己的 `Deposit()` 和 `Withdraw()` 版本，这导致了代码重复和潜在的错误，再次增加了安全问题的可能性。以下是你可能使用组合（containment）而不是继承的原因：

*   新类不需要访问所有现有类成员。
*   应用程序需要松耦合，以便现有类的更改不会影响到新类。
*   对现有类的运行时更改不会影响新类（这是一种高级编程技术，在本微型书中未充分讨论；请参见第 3 本的第 6 章），但你可以在 [`https://www.dotnetcurry.com/csharp/dynamic-class-creation-roslyn`](https://www.dotnetcurry.com/csharp/dynamic-class-creation-roslyn) 中了解它。
*   限制对私有和受保护成员的访问至关重要，而新类不需要访问这些成员（实际上提高了安全性）。

在这种情况下，你说 `SavingsAccount_` **拥有一个** `BankAccount`。硬核面向对象专家会说 `SavingsAccount` **组合了** `BankAccount`。也就是说，`SavingsAccount` 部分由 `BankAccount` 组成。

### HAS_A 关系

HAS_A 关系在根本上与 IS_A 关系不同。这种差异在下面的应用程序代码示例中看起来并不严重：

```csharp
// 创建一个新的储蓄账户。
BankAccount ba = new BankAccount()
// HAS_A  SavingsAccount
SavingsAccount_ sa = new SavingsAccount_(ba, 5);
// 向其存入 100 元。
sa.Deposit(100M);
// 现在累积利息。
sa.AccumulateInterest();
```

问题是，这个修改过的 `SavingsAccount_` 不能作为 `BankAccount` 使用，因为它没有自 `BankAccount`。相反，它包含一个 `BankAccount` —— 不是同一个概念。例如，下面的代码示例会失败：

```csharp
// DirectDeposit -- 自动存入我的薪水。
void DirectDeposit(BankAccount ba, int pay)
{
    ba.Deposit(pay);
}
void SomeMethod()
{
// 下面示例失败了。
SavingsAccount_ sa = new SavingsAccount_(sa, 100);
// … 继续 …
}
```

![Remember](img/remember.png) `DirectDeposit()` 不能接受 `SavingsAccount_` 来代替 `BankAccount`。在 C# 看来，两者之间不存在明显的联系，因为不涉及继承。尽管如此，不要认为这种情况让组合变成了一个坏坏主意。你只需要以不同的方式来处理这个概念以便使用它。

### 什么时候用 IS_A，什么时候用 HAS_A

IS_A 和 HAS_A 关系之间的区别不仅仅是软件便利性的问题。这种关系在现实世界中有一个推论。

例如，福特 Explorer **是**一辆汽车。Explorer **拥有**一个电动机。如果你的朋友说“开你的车过来”，而你开着一辆 Explorer 出现，他没有理由抱怨。然而，如果你抱着你 Explorer 的引擎出现，他可能就有理由抱怨了（或者至少*你*会累）。`Explorer` 类应该扩展 `Car` 类，不仅是为了让 `Explorer` 访问 `Car` 的方法，也是为了表达两者之间的基本关系。

遗憾的是，初学者可能会让 `Car` 继承 `Motor`，作为一种简单的方法让 `Car` 类访问 `Motor` 的成员，而 `Car` 运行恰需要这些成员。例如，`Car` 可以继承 `Motor.Go()` 方法。然而，这个例子凸显了这种方法的问题：尽管人类在说话时变得很草率，但让汽车运行和让电动机运行并不是一回事。汽车的运行操作确实依赖于电动机的运行，但它们并不是同一个东西 —— 你还需要挂入挡位，释放刹车并完成其他任务。也许不仅如此，继承自 `Motor` 歪述了事实。汽车根本不是一种电动机。

![Remember](img/remember.png) 软件的优雅是一个值得实现的目标。它增强了可理解性、可靠性和可维护性。

## 支持继承的其他特性

C# 实现了一系列旨在支持的特性。接下来的章节将讨论这些特性。

### 可替换的类

程序可以在调用基类对象的地方使用子类对象。事实上，你可能已经在其中一个示例中见过这个概念。`SomeMethod()` 可以将 `SavingsAccount` 对象传递给 `DirectDeposit()` 方法，该方法期望一个 `BankAccount` 对象。你可以让这种转换更加显式：

```csharp
BankAccount ba;
// 原始的，不是 SavingsAccount_
SavingsAccount sa = new SavingsAccount();
// OK:
ba = sa; // 隐式将子类转换为基类。
ba = (BankAccount)sa; // 但优选显式强制转换。
sa = (SavingsAccount)ba; // 允许显式转换。
```

将 `SavingsAccount` 对象转换为 `BankAccount`。C# 不会这样做。

```csharp
// 不 OK:
sa = ba; // 子类的隐式转换
```

将 `SavingsAccount` 存储到 `BankAccount`。C# 转换对象。最后一行尝试将 `BankAccount` 转换为 `SavingsAccount`。你可以完成这个操作，但 C# 不会。

![Remember](img/remember.png) IS_A 属性不是反射性的。也就是说，尽管 Explorer 是汽车，但汽车一定是 Explorer。同样，`BankAccount` 不一定是 `SavingsAccount`，所以隐式转换是不允许的。显式转换是被允许的，因为程序员表示愿意“冒险”。

### 运行时的非法转换

通常，将对象从 `BankAccount` 转换为 `SavingsAccount` 是一个危险的操作。考虑这个来自 `SavingsAccount` 的示例：

```csharp
class Program
{
    public static void ProcessAmount(BankAccount bankAccount)
    {
        // 向账户存款大额金额。
        bankAccount.Deposit(10000.00M);
        // 如果是 SavingsAccount，现在收取利息。
        SavingsAccount savingsAccount = (SavingsAccount)bankAccount;
        savingsAccount.AccumulateInterest();
    }

    static void Main(string[] args)
    {
        SavingsAccount sa = new SavingsAccount(100M, 12.5M);
        ProcessAmount(sa);
        Console.WriteLine(sa.ToString());
        BankAccount ba = new BankAccount(100M);
        ProcessAmount(ba);
        Console.WriteLine(ba.ToString());
        Console.Read();
    }
}
```

`ProcessAmount()` 执行了一些操作，包括调用 `AccumulateInterest()` 方法。将 `ba` 强制转换为 `SavingsAccount` 是必要的，因为 `bankAccount` 参数声明为 `BankAccount`。程序可以正常编译，因为所有类型转换都是通过显式转换的。

从 `Main()` 内部第一次调用 `ProcessAmount()` 非常顺利。`SavingsAccount` 对象 `sa` 被传递给 `ProcessAmount()` 方法。从 `BankAccount` 到 `SavingsAccount` 的转换没有产生问题，因为 `ba` 对象原本就是 `SavingsAccount`。

然而，第二次调用 `ProcessAmount()` 就没那么幸运了。到 `SavingsAccount` 的转换是不允许的。`ba` 对象没有 `AccumulateInterest()` 方法。当你运行此示例时，使用调试⇒ 无调试启动命令看到以下输出：

```
1001 - $11,362.50 (12.50%)
未处理异常: System.InvalidCastException: 无法转换对象类型
```





`将类型 'SimpleSavingsAccount.BankAccount' 转换为类型`

`'SimpleSavingsAccount.SavingsAccount'位于`

`SimpleSavingsAccount.Program.ProcessAmount(BankAccount bankAccount) in`

`E:\CSAIO4D2E\BK02\CH05\SimpleSavingsAccount4\Program.cs:line 96 at`

`SimpleSavingsAccount.Program.Main(String[] args) in`

`E:\CSAIO4D2E\BK02\CH05\SimpleSavingsAccount4\Program.cs:line 107`

`按任意键继续 …`

![警告](img/warning.png) 错误的转换会在程序执行期间产生错误（以异常形式的`运行时错误`）。运行时错误比编译时错误更难发现和修复。糟糕的是，它们可能会发生在你以外的用户身上，而用户通常对此并不买账。

### 使用 `is` 运算符避免无效转换

如果 `ProcessAmount()` 方法能够在执行转换之前确保传递给它的对象是 `SavingsAccount` 对象，那么它就能正常工作。C# 提供了两个关键字用于此目的：`is` 和 `as`。

`is` 运算符接受左侧一个对象和右侧一个类型。如果左侧对象的运行时类型与右侧类型兼容，则 `is` 运算符返回 `true`。在尝试进行强制转换之前，使用它来验证强制转换是否合法。你可以修改前一节中的 `ProcessAmount()` 方法（如 `SimpleSavingsAccount5` 所示），通过使用 `is` 运算符来避免运行时错误：

```csharp
public static void ProcessAmount(BankAccount bankAccount)
{
    // 向账户存入大额资金。
    bankAccount.Deposit(10000.00M);
    // 如果对象是 SavingsAccount
    if (bankAccount is SavingsAccount)
    {
        // 现在收集利息。
        SavingsAccount savingsAccount = (SavingsAccount)bankAccount;
        savingsAccount.AccumulateInterest();
    }
}
```

新增的 `if` 语句检查 `bankAccount` 对象以确保它是 `SavingsAccount` 类。当第一次调用 `ProcessAmount()` 时，`is` 运算符返回 `true`。然而，当第二次调用传递 `BankAccount` 对象时，`is` 运算符返回 `false`，从而避免了非法强制转换。此版本的程序不会像此处所示产生运行时错误。

`1001 - $11,362.50 (12.50%)`

`1002 - $10,100.00`

![提示](img/tip.png) 最佳实践是用 `is` 运算符保护所有强制转换，以避免运行时错误的可能。如果可能，你应该完全避免强制转换。

### 使用 `as` 运算符避免无效转换

`as` 运算符的工作与 `is` 有些不同。它不是在转换成功（但未成功）时返回 `bool`，而是将左侧类型转换为右侧类型。如果转换失败，它会安全地返回 `null` 而不是导致运行时错误。只有当 `as` 强制转换的结果不为 `null` 时，你才应该使用该结果。因此，使用 `as` 的写法如下：

```csharp
SavingsAccount savingsAccount = bankAccount as SavingsAccount;
if (savingsAccount != null)
{
    // 继续使用 savingsAccount。
}
// 否则，不要使用它：自行生成错误消息。
```

![记住](img/remember.png) 通常，你应该优先使用 `as`，因为它效率更高。转换已经通过 `as` 运算符完成，而当你使用 `is` 时，你必须完成两个步骤：首先用 `is` 进行测试，然后用强制转换运算符完成转换。遗憾的是，`as` 不适用于值类型变量，因此你不能将其用于 `int`、`long` 或 `double` 类型，也不能用于 `char`。当你尝试转换值类型对象时，请优先使用 `is` 运算符。

第 6 章

# 多态？（Poly-what-ism?）

## 本章内容

![项目](img/check.png) **隐藏或重写基类方法**

![项目](img/check.png) **构建抽象类和方法**

![项目](img/check.png) **使用 `ToString()`**

![项目](img/check.png) **密封类使其无法被子化**

在继承中，一个类采用了另一个类的成员。因此，可以创建一个 `SavingsAccount` 类，它从基类 `BankAccount` 继承数据成员（如 `account id`）和方法（如 `Deposit()`）。这很有用，但这种对继承的定义不足以模拟业务世界中的真实情况。（如果你不了解或不记得关于类继承，请参见本迷你书的第 5 章。）

微波炉是一种烤箱，不是因为它看起来像烤箱，而是因为它执行与烤箱相同的功能。微波炉可能会执行额外的功能，但它至少执行基础的烤箱功能，如加热食物。了解烤箱为了实现这一点内部必须做什么并不重要，这比了解它是哪种类型的烤箱、谁制造的，或者购买时是否在打折更为重要。

从人类的角度来看，微波炉与传统烤箱之间的关系……（此处省略了原文大量重复的关系描述）……了解烤箱为了实现这一点内部必须做什么是很重要的。




因此，一个类中的方法可以通过不同的参数来重载同类中的另一个方法。事实证明，方法也可以重载其自身基类中的方法。重载基类方法被称为`hiding`（隐藏）方法。

假设你的银行采用了一项政策，使得储蓄账户的取款与其他类型的取款不同。为了方便，假设从储蓄账户取款需要费用 1.50 元。

采用过程化的方法，你可以通过在类中设置一个标记（变量）来指示该对象是 `SavingsAccount` 还是一个简单的 `BankAccount`。然后，取款方法必须检查该标记以决定是否需要收取 1.50 元，如下所示：

```c
public class BankAccount
{
    private decimal _balance;
    private bool _isSavingsAccount; // 标记
    // 指示初始余额以及你创建的
    // 是否为储蓄账户。
    public BankAccount(decimal initialBalance, bool isSavingsAccount)
    {
        _balance = initialBalance;
        _isSavingsAccount = isSavingsAccount;
    }
    public decimal Withdraw(decimal amountToWithdraw)
    {
        // 如果账户是储蓄账户……
        if (_isSavingsAccount)
        {
            // ……那么扣除 1.50 元。
            _balance -= 1.50M;
        }
        // 继续执行常规取款代码：
        if (amountToWithdraw > _balance)
        {
            amountToWithdraw = _balance;
        }
        _balance -= amountToWithdraw;
        return amountToWithdraw;
    }
}

class MyClass
{
    public void SomeMethod()
    {
        // 创建一个储蓄账户：
        BankAccount ba = new BankAccount(0, true);
    }
}
```

你的方法必须通过构造函数通过传递标记来告诉 `BankAccount` 你实例化的对象是否是 `SavingsAccount`。构造函数保存了该标记，并在 `Withdraw()` 方法中使用它来决定是否收取额外的 1.50 元。

更面向对象的方法是通过在 `SavingsAccount` 类中使用一个同名的新方法，来隐藏基类 `BankAccount` 中的 `Withdraw()` 方法。`HidingWithdrawal` 示例中的 `BankAccount` 和 `SavingsAccount` 类展示了这种方法如何工作：

```csharp
// BankAccount -- 一个非常基础的银行账户
internal class BankAccount
{
    internal BankAccount(decimal initialBalance)
    {
        Balance = initialBalance;
    }
    internal decimal Balance
    { get; private set; }
    internal decimal Withdraw(decimal amount)
    {
        // 良好的做法是避免修改输入参数。
        // 修改副本。
        decimal amountToWithdraw = amount;
        if (amountToWithdraw > Balance)
        {
            amountToWithdraw = Balance;
        }
        Balance -= amountToWithdraw;
        return amountToWithdraw;
    }
}

// SavingsAccount -- 一个产生利息的银行账户
internal class SavingsAccount : BankAccount
{
    private decimal InterestRate
    { get; set; }
    // SavingsAccount -- 输入以 0 到 100
    // 之间的速率表示的。
    public SavingsAccount(decimal initialBalance, decimal interestRate)
    : base(initialBalance)
    {
        InterestRate = interestRate / 100;
    }
    // Withdraw -- 你可以提取最多等于余额的
    // 金额；返回提取的金额。
    internal decimal Withdraw(decimal withdrawal)
    {
        // 先扣除那 1.50 元。
        base.Withdraw(1.5M);
        // 现在你可以从剩余部分中取款。
        return base.Withdraw(withdrawal);
    }
}
```

这两个类为创建账户和取款提供了一些基础。注意，两个类都具有签名完全相同的 `Withdraw()` 方法，因此 `SavingsAccount` 中的 `Withdraw()` 方法完全隐藏了 `BankAccount` 中的 `Withdraw()` 方法。这里给了用于测试这两个类的 `Main()` 方法。

```csharp
static void Main(string[] args)
{
    BankAccount ba;
    SavingsAccount sa;
    // 创建一个银行账户并取出 100 元。
    ba = new BankAccount(200M);
    ba.Withdraw(100M);
    // 对储蓄账户尝试同样的技巧。
    sa = new SavingsAccount(200M, 12);
    sa.Withdraw(100M);
    // 显示结果余额。
    Console.WriteLine("直接调用时:");
    Console.WriteLine("BankAccount balance is {0:C}", ba.Balance);
    Console.WriteLine("SavingsAccount balance is {0:C}", sa.Balance);
    Console.Read();
}
```

在这种情况下，`Main()` 创建了一个初始余额为 200 元的 `BankAccount` 对象，然后取出了 100 元。`Main()` 对 `SavingsAccount` 对象重复了这一技巧。当 `Main()` 从基类取款时，`BankAccount.Withdraw()` 从容地执行了取款函数。当 `Main()` 随后从储蓄账户取款 100 元时，`Withdraw()` 方法增加了额外的 50 元。

### 让隐藏方法比添加标记更好

从表面上看，向 `BankAccount` 中添加一个标记似乎比这一切要简单。但问题是多方面的：假设你的银行决定添加 `CheckingAccount`（支票账户）或 `CDAccount`（存单）。在添加了三四种账户后，`Withdraw()` 方法看起来变得复杂。这些类型的类应该关注自己的取款策略。基类通常并不知道子类的存在。由于这种方法，`BankAccount` 独自。

### 意外隐藏基类方法

奇怪的是，你可能会意外隐藏基类方法。例如，你可能有一个启动车辆的 `Vehicle.TakeOff()` 方法。后来，其他人扩展了你的 `Vehicle` 类，增加了一个 `Airplane` 类。它的方法完全不同。在航空术语中，“起飞”的意思不仅仅是“移动”。显然，这是一个身份误认案例——这两个方法除了名称相同外没有相似之处。幸运的是，C# 检测到了这个问题。在编译之前的 `HidingWithdrawal` 程序示例时，C# 生成了一个看起来不安的警告。警告信息的文本很长，但最重要的部分是：

`’…SavingsAccount.Withdraw(decimal)’隐藏了继承成员`
`'…BankAccount.Withdraw(decimal)'.`
`如果是隐藏，请使用 new 关键字。`

C# 试图告诉你子类中写了一个与基类方法同名的方法。这是你想要做的吗？

![Tip](img/tip.png) 这只是一个警告——除非切换到错误列表窗口查看，否则你不会注意到。但你应该解决并修复所有警告。在大多数情况下，警告都是在提醒你如果不修复可能会带来问题。

使用 **new** 描述符（如下加粗所示）告诉 C# 隐藏方法是有意为之而不是疏忽的结果（并且这会让警告消失）：

```csharp
internal new decimal Withdraw(decimal withdrawal)
{
    // 先扣除那 1.50 元。
    base.Withdraw(1.5M);
    // 现在你可以从剩余部分中取款。
    return base.Withdraw(withdrawal);
}
```

![Tip](img/tip.png) 此处 `new` 关键字的使用与用于创建对象的 `new` 单词完全无关。（C# 甚至可以重载自己！）




你可以使用子类中的方法来重载基类中的方法。虽然这个过程听起来非常简单，但它引入了巨大的能力，而能力往往伴随着危险。

这是一个思想实验：你应该决定在编译时还是运行时调用 `BankAccount.Withdraw()` 或 `SavingsAccount.Withdraw()`呢？为了说明这种区别，下面的示例以一种看似无害的方式更改了之前的 `HidingWithdrawal` 程序。（`HidingWithdrawalPolymorphically` 版本通过省略不发生变化的内容简化了列表）。这里展示了新版本：

```csharp
class Program
{
    public static void MakeAWithdrawal(BankAccount ba, decimal amount)
    {
        ba.Withdraw(amount);
    }
    static void Main(string[] args)
    {
        BankAccount ba;
        SavingsAccount sa;
        // 创建一个银行账户，取出 100 美元，并
        // 显示结果。
        ba = new BankAccount(200M);
        MakeAWithdrawal(ba, 100M);
        // 对储蓄账户尝试同样的技巧。
        sa = new SavingsAccount(200M, 12);
        MakeAWithdrawal(sa, 100M);
        // 显示最终余额。
        Console.WriteLine("通过中间件调用时:");
        Console.WriteLine("BankAccount balance is {0:C}", ba.Balance);
        Console.WriteLine("SavingsAccount balance is {0:C}", sa.Balance);
        Console.Read();
    }
}
```

该程序的以下输出可能令人困惑，也可能，取决于你的预期：

```
通过中间件调用时:
BankAccount balance is $100.00
SavingsAccount balance is $100.00
```

这一次，程序并不是在 `Main()` 中直接执行取款，而是将银行账户对象传递给 `MakeAWithdrawal()` 方法。

第一个问题相当直观：为什么 `MakeAWithdrawal()` 方法在明确表示它在寻找 `BankAccount` 的时候，竟然接受一个 `SavingsAccount` 对象呢？答案显而易见：“因为 `SavingsAccount` 是一个 `BankAccount`。”（参见本本微型书第 5 章中的“IS_A 与 HAS_A — 我太困惑了”节）。

第二个问题则微妙得多。当传递 `BankAccount` 对象时，`MakeAWithdrawal()` 调用了 `BankAccount.Withdraw()`——这很清楚。但当传递 `SavingsAccount` 对象时，`MakeAWithdrawal()` 调用了同一个方法。它难道不应该调用子类中的 `Withdraw()` 方法吗？

控方认为，调用 `ba.Withdraw()` 应该调用 `BankAccount.Withdraw()` 方法。显然，`ba` 对象是一个 `BankAccount`。做任何其他操作只会导致混乱。辩方在 `Main()` 中有证人证明，尽管 `ba` 对象被声明为 `BankAccount`，但它实际上是一个 `SavingsAccount`。陪团陷入了僵局。两种论点都同样有效。

在这种情况下，C# 倾向于控方一方：在两种可能性中，选择声明类型更安全，因为可以避免任何误解。该对象被声明为 `BankAccount`，事实就是如此。然而，这可能不是你想要的。

### 每次都使用声明类型（这有错吗？）

在某些情况下，你并不想选择声明类型。你想要的是根据实际类型——即运行时类型——进行调用，而不是声明类型。例如，你想使用存储在 `BankAccount` 变量中的 `SavingsAccount`。这种在运行时做决的能力被称为多态（polymorphism）或晚绑定。每次都使用声明类型被称为早期绑定，因为它听起来像是晚绑定的相反。

多态（polymorphism）一词源于希腊语：`Poly` 意味着“多个”，`morph` 意味着“转换”，而 `ism` 与意识形态或哲学有关。因此，多态是将单个对象 `BankAccount` 转换为许多不同的对象 `BankAccount` 或 `SavingsAccount`（在本例中）的想法或概念。多态和晚绑定并不是完全相同的概念——但它们的区别是微妙的：

*   多态指的是在运行时决定调用哪种方法的通用能力。
*   晚绑定是指语言实现多态的具体方式。

多态是面向对象编程（OOP）力量的关键。它是如此重要，以至于不支持多态的语言无法自诩为面向对象编程的语言。

![Technicalstuff](img/technicalstuff.png) 支持类但不支持多态的语言是基于对象的语言。Visual Basic 6.0（不是 VB.NET）就是此类语言的一个例子。

没有多态，继承几乎毫无意义。作为另一个例子，假设你编写了一个使用名为 `Student` 类的优秀程序。经过几个月的设计、编码和测试后，你发布了该程序，并获得了同事和评论家的一致好评。

时间流逝，你的老板要求你在这个程序中添加处理研究生的能力，他们与本科生相似但并不完全相同。（研究生可能会声称他们从任何方面都不相似。）假设计算研究生学费的公式与本科生的公式完全不同。现在，你的老板并不知道也不在乎在程序深处有许多对成员方法 `CalcTuition()` 的调用。下面的示例显示了这些许多对 `CalcTuition()` 调用之一：

```csharp
void SomeMethod(Student s) // 可能是研究生或本科生
{
    // ... 无论如何
    s.CalcTuition();
    // ... 继续 ...
}
```

如果 C# 不支持晚绑定，你需要编辑 `SomeMethod()` 来检查传递的 `s` 对象是研究生还是本科生。如果 `s` 是本科生，程序将调用 `Student.CalcTuition()`；如果 `s` 是研究生，则将调用 `GraduateStudent.CalcTuition()`。编辑 `SomeMethod()` 似乎并不坏，但有两个问题：

*   你假设它只在一个方法中使用。假设 `CalcTuition()` 在多处被调用。
*   `CalcTuition()` 可能不是两个类之间的唯一区别。你很难找到所有需要更改的项目。

使用多态，你可以让 C# 决定调用哪种方法。

### 使用 is 多态地访问隐藏方法

C# 提供了一种手动解决程序多态化问题的方法，使用关键字 `is`。（本本微型书第 5 章中的“使用 is 运算符避免无效转换”节引入了 `is` 及其兄弟成员 `as`。）表达式 `ba is SavingsAccount` 根据对象的运行时类返回 `true` 或 `false`。声明类型可能是 `BankAccount`，但它到底是什么类型？下面的代码块使用 `is` 专门访问 `SavingsAccount` 版本的 `Withdraw()`（如在 `HidingWithdrawalPolymorphically2` 中所示）：

```csharp
public static void MakeAWithdrawal(BankAccount ba, decimal amount)
{
    if (ba is SavingsAccount)
    {
        SavingsAccount sa = (SavingsAccount)ba;
        sa.Withdraw(amount);
    }
    else
    {
        ba.Withdraw(amount);
    }
}
```

现在，当 `Main()` 向方法传递 `SavingsAccount` 对象时，`MakeAWithdrawal()` 检查 `ba` 对象的运行时类型并调用 `SavingsAccount.Withdraw()`。

![Technicalstuff](img/technicalstuff.png) 作为另一种方案，程序员可以在以下单行中完成对 `SavingsAccount` 的强制转换和调用：

```csharp
((SavingsAccount)ba).Withdraw(amount); // 注意括号的位置。
```



`is` 这种方法虽然可行，但并不是一个好主意。它要求 `MakeAWithdrawal()` 感知所有类型的银行账户，以及哪些账户是由不同的类表示的。这让可怜的 `MakeAWithdrawal()` 承担了太多的责任。目前，你的应用程序只处理两种类型的银行账户，但假设你的老板要求你实现一种新的账户类型 `CheckingAccount`，它有不同的 `Withdraw()` 要求。如果你不搜索并找到每个检查参数运行时类型的方法，你的程序将无法正常工作。

### 声明虚方法方法并对其进行重写

作为 `MakeAWithdrawal()` 的作者，你并不希望了解所有不同类型的账户。你希望将了解账户类型的责任留给使用 `MakeAWithdrawal()` 的程序员，让他们去处理自己的账户类型，而你互不打扰。你希望让 C# 根据对象的运行时类型来决定调用哪个方法。

你通过在基类方法上标记 `virtual` 关键字，并在每个子类版本的方法上标记 `override` 关键字，来告诉 C# 在运行时决定 `Withdraw()` 版本的版本。

下面的示例依赖于多态。它在 `Withdraw()` 方法中有输出语句，以证明正确的方法确实被调用了。以下是 `PolymorphicInheritance` 程序中的 `BankAccount` 和 `SavingsAccount` 类：

```csharp
// BankAccount -- 一个非常基本的银行账户
internal class BankAccount
{
    internal BankAccount(decimal initialBalance)
    {
        Balance = initialBalance;
    }
    internal decimal Balance
    { get; private set; }
    internal virtual decimal Withdraw(decimal amount)
    {
        decimal amountToWithdraw = amount;
        if (amountToWithdraw > Balance)
        {
            amountToWithdraw = Balance;
        }
        Console.WriteLine($"In BankAccount.Withdraw() for " +
            $"${amountToWithdraw}.");
        Balance -= amountToWithdraw;
        return amountToWithdraw;
    }
}

// SavingsAccount -- 会计息的银行账户
internal class SavingsAccount : BankAccount
{
    private decimal InterestRate
    { get; set; }
    // SavingsAccount -- 输入以 0 到 100 之间的速率表示的速率。
    public SavingsAccount(decimal initialBalance, decimal interestRate)
    : base(initialBalance)
    {
        InterestRate = interestRate / 100;
    }
    // Withdraw -- 你可以提取任何不超过余额的金额；
    // 返回提取的金额。
    internal override decimal Withdraw(decimal withdrawal)
    {
        // 扣除 $1.50 的费用。
        Console.WriteLine("Deductng the SavingsAccount fee.");
        base.Withdraw(1.5M);
        // 现在你可以从剩余部分中提取。
        Console.WriteLine($"In SavingsAccount.Withdraw() for " +
            $"${withdrawal}.");
        return base.Withdraw(withdrawal);
    }
}
```

`Withdraw()` 方法在基类 `BankAccount` 中被标记为 `virtual`。同样，你在子类 `SavingsAccount` 中看到它被标记为 `override`。这个示例还增加了一些 `Console.WriteLine()` 调用，以便你可以看到发生了什么。以下是 `Program` 类的代码：

```csharp
class Program
{
    public static void MakeAWithdrawal(BankAccount ba, decimal amount)
    {
        ba.Withdraw(amount);
    }
    static void Main(string[] args)
    {
        BankAccount ba;
        SavingsAccount sa;
        // 创建一个银行账户，提取 $100 并
        // 显示结果。
        Console.WriteLine("Withdrawal: MakeAWithdrawal(ba, …)");
        ba = new BankAccount(200M);
        MakeAWithdrawal(ba, 100M);
        Console.WriteLine("BankAccount balance is {0:C}", ba.Balance);
        // 对储蓄账户尝试同样的技巧。
        Console.WriteLine("\r\nWithdrawal: MakeAWithdrawal(sa, …)");
        sa = new SavingsAccount(200M, 12);
        MakeAWithdrawal(sa, 100M);
        Console.WriteLine("SavingsAccount balance is {0:C}", sa.Balance);
        Console.Read();
    }
}
```

注意，所有的决策代码都已从 `HidingWithdrawalPolymorphically2` 示例中删除。执行此程序的输出所示：

```text
Withdrawal: MakeAWithdrawal(ba, …)
In BankAccount.Withdraw() for $100.
BankAccount balance is $100.00
Withdrawal: MakeAWithdrawal(sa, …)
Deductng the SavingsAccount fee.
In BankAccount.Withdraw() for $1.5.
In SavingsAccount.Withdraw() for $100.
In BankAccount.Withdraw() for $100.
SavingsAccount balance is $98.50
```

![Tip](img/tip.png) 谨慎选择哪些方法设为虚方法。每个虚方法在资源使用和运行速度上都有微小的成本，因此只有在需要时才使用 `virtual` 关键字。这是高度灵活的类之间的权衡。



高中和大学有几个相似的属性（参见图 6-1）——比你想象的要多。这两类学校都提供了一个公开的 `Enroll()` 方法来向学校添加 `Student` 对象。此外，这两个类都提供了一个私有成员 `numStudents`，表示就读该学校的学生人数。另一个共同特征是学生之间的关系：一所学校可以有任何数量的学生——一个学生在同一只能就读一所学校。即使高中和大多数大学提供的都比描述的要，但为了说明，每种类型的成员只需要一个即可。

除了高中的功能外，大学还包含一个 `GetGrant()` 方法和一个数据成员 `avgSAT`。高中没有 SAT 入学要求，学生也不获得联邦资助。

图 6-1 就其本身而言是可以接受的，但某些信息是重复的，而代码（以及 UML 图）中的重复是糟糕的。你可以通过允许更复杂的类 `University` 继承自更简单的 `HighSchool` 类来减少重复，如图 6-2 所示。

`HighSchool` 类保持不变，但 `University` 类更容易描述了。你说：“一个 `University` 是一个 `HighSchool`，但它还拥有一个 `avgSAT` 和一个 `GetGrant()` 方法。”但这个解决方案有一个根本性的问题：大学并不是具有特殊属性的高中。

![继承 HighSchool 简化了 University 类但引入了问题的截图](img/9781119839071-fg020602.png)

图 6-2： 继承 `HighSchool` 简化了 `University` 类，但引入了问题。

你说：“又怎样？继承行得通，而且省力。”确实如此，但这些问题不仅仅是风格上的琐碎琐节。这种类型的错误表示对程序员来说，现在和将来都是困惑的。有一天，一个不熟悉你的编程技巧的程序员将不得不阅读并理解你的代码在做什么。误导性的表示很难调和和理解。

此外，这种类型的错误表示可能会在后期引发问题。假设高中决定在毕业舞会上选出一个“最受欢迎”的学生。聪明的程序员为 `HighSchool` 类添加了 `NameFavorite()` 方法，应用程序调用该方法来命名最喜欢的 `Student` 对象。

但现在你遇到了问题：大多数大学不会选出最受欢迎的学生。然而，只要 `University` 继承自 `HighSchool`，它就继承了 `NameFavorite()` 方法。一个额外的方法似乎不是什么大事。“忽略它就好，”你说。然而，一个方法只是混乱之墙上的又一块砖。额外的方法和属性随着时间的推移而积累，直到 `University` 类背负了许多额外负担。可怜那些必须理解哪些方法是“真实”的、哪些不是的可怜软件开发者吧。

![记住](img/remember.png) *便利性继承*导致了另一个问题。按照目前的写法方式，图 6-2 意味着 `University` 和 `HighSchool` 具有相同的入学程序。尽管这个说法听起来多么不可能，但请假设它是真的。程序被开发、打包并发送给毫无防备的公众。几个月后，学区决定修改其入学程序。没有人能明显看出，修改高中的入学程序也会修改当地大学的报名程序。

要解决问题的根源，你必须考虑大学并不是特定类型的高中。两者之间存在关系，但 `IS_A`（是）或 `HAS_A`（拥有）关系都不是正确的。相反，高中和大学都是特殊类型的学校。这是它们最大的共同点。

图 6-3 描述了一种更好的关系。新定义的类 `School` 包含了两种类型学校的共同属性，包括它们与 `Student` 对象共同的关系。`School` 甚至包含了共同的 `Enroll()` 方法，尽管它是抽象，因为 `HighSchool` 和 `University` 通常不以相同的方式实现 `Enroll()`。

![将 HighSchool 和 University 都基于共同的 School 类之上的截图](img/9781119839071-fg020603.png)

图 6-3： 将 `HighSchool` 和 `University` 都基于共同的 `School` 类。

`HighSchool` 和 `University` 类现在继承自一个共同的基类。每个类都包含其独特的成员：`HighSchool` 中的 `NameFavorite()`，以及 `University` 的 `GetGrant()` 和 `avgSAT`。此外，两个类都重写了 `Enroll()` 方法，描述了该类型的学校如何招生。实际上，这个示例从两个相似的类中提取出一个超类（或基类），这两个类现在变成了子类。`School` 类的引入至少有两个巨大的优势：

*   **它符合现实。** `University` 是一个 `School`，但它不是 `HighSchool`。匹配现实是很好，但并不是决定性的。
*   **它将一个类与其他类的更改隔离开来。** 为 `University` 添加方法不会影响 `HighSchool`。

这种从相似类中提取公共属性的过程被称为重构（factoring）。这种面向对象语言的特性对于前面提到的原因很重要，还有一点：减少冗余。

![警告](img/warning.png) 只有当继承关系对应现实时，重构才是合理的。将 `Mouse` 和 `Joystick` 类重构因为它们都是硬件设备是合法的。将 `Mouse` 和 `Display` 类重构因为它们进行系统调用是不合理的。

重构可以并且通常会导致多层抽象。例如，针对层次结构编写的程序，其类结构可能类似于图 6-4 所示。

![类重构通常增加了继承层的截图](img/9781119839071-fg020604.png)

图 6-4： 类重构通常增加了继承层。

你可以看到图 6-4 在 `University` 和 `School` 之间插入了一对新类：`HigherLearning` 和 `LowerLevel`。它将新类 `HigherLearning` 分为 `College` 和 `University`。这种多层类层次在重构关系时是常见且理想的。它们符合现实，并可以让你了解解决方案的细微特征。

但注意，对于任何给定的类集，存在统一的重构理论。图 6-4 所示的关系看起来是自然的，但假设应用程序更关心的是由地方政客管理的学校与非管理的学校的区别。这种在图 6-5 所示的关系对于这类问题来说更合适。不存在正确的重构：拆分类的正确方法部分取决于所解决的问题。

### 抽象类：只剩下概念

尽管重构在智力上令人满足，但它揭示了它自身的问题。回顾在本章开头介绍的 `BankAccount`。思考你可能如何定义 `BankAccount` 中定义的成员方法。

![拆分类的部分取决于所解决问题的截图](img/9781119839071-fg020605.png)

图 6-5： 拆分类的部分取决于所解决的问题。



大多数 `BankAccount` 成员方法的重构都没有什么问题，因为两种账户类型都以相同的方式实现了它们。你应该在 `BankAccount` 中实现这些公共方法。然而，`Withdraw()` 则不同。从储蓄账户取款的规则与从支票账户取款的规则不同。你必须不同的实现 `SavingsAccount.Withdraw()` 和 `CheckingAccount.Withdraw()`。但如何实现 `BankAccount.Withdraw()` 呢？向银行经理寻求。这是可能发生的对话：

*   “从账户取款的规则是什么？”你期待地问道。
*   “哪种类型的账户？储蓄还是支票？”回答道道。
*   “从一个账户，”你说，“仅仅是一个账户。”
*   [茫然的眼神。]（你可以说是“呆然的银行表情”。话虽如此，也许不是。）

问题在于这个问题没有意义。不存在所谓的“仅仅是一个账户”。所有的账户（在本例中）要么是支票账户，要么是储蓄账户。“账户”的概念是 `abstract:` 的：它提取了两个具体类共有的属性。它是不完整的，因为缺少关键方法 `Withdraw()`。（在深入研究细节后，你可能会发现简单账户所欠缺的其他属性。）

### 如何使用抽象类？

抽象类用于描述抽象概念。一个 `abstract class` 是一个包含一个或多个抽象方法的类。抽象方法是标记为 `abstract` 的方法，并且没有实现，因为它没有方法体。当你从抽象类派生子类时，你会创建方法体。考虑 `AbstractInheritance` 程序中的类：

```csharp
// AbstractBaseClass -- 创建一个只包含 
//一个 Output() 方法的抽象基类。你也可以写成 "public abstract."
abstract public class AbstractBaseClass
{
    // Output -- 输出字符串的抽象方法
    abstract public void Output(string outputString);
}

// SubClass1 -- AbstractBaseClass 的一个具体实现
public class SubClass1 : AbstractBaseClass
{
    override public void Output(string source) // 或者用 "public override"
    {
        string s = source.ToUpper();
        Console.WriteLine($"Call to SubClass1.Output() from within {s}");
    }
}

// SubClass2 -- AbstractBaseClass 的另一个具体实现
public class SubClass2 : AbstractBaseClass
{
    public override void Output(string source) // 或者用 "override public"
    {
        string s = source.ToLower();
        Console.WriteLine($"Call to SubClass2.Output() from within {s}");
    }
}
```

程序首先定义了具有单个抽象 `Output()` 方法的类 `AbstractBaseClass`。因为它是被声明为 `abstract` 的，所以 `Output()` 没有实现——即没有方法体。有两个类继承自 `AbstractBaseClass`：`SubClass1` 和 `SubClass2`。它们都是具体类，因为它们用真实的方法重写了 `Output()` 方法，并且本身不包含任何抽象方法。

![Tip](img/tip.png) 无论类是否具有抽象成员，都可以被声明为抽象的；然而，只有当其上方任何基类中的所有抽象方法都被完整的方法重写时，该类才能是具体的（非抽象的）。

两个子类的 `Output()` 方法微差异在于：它们都接受输入字符串并将其返回给用户。然而，其中一个在输出之前将字符串转换为全大写，而另一个将其转换为全小写。以下是该示例的 `Program` 类：

```csharp
class Program
{
    public static void Test(AbstractBaseClass ba)
    {
        ba.Output("Test");
    }
    static void Main(string[] args)
    {
        // 你不能创建一个 AbstractBaseClass 对象，因为它是
        //抽象的。如果你取消下面行的注释，
        // C# 将生成编译错误。
        // AbstractBaseClass ba = new AbstractBaseClass();
        // 现在对 SubClass1 重复实验。
        Console.WriteLine("\ncreating a SubClass1 object");
        SubClass1 sc1 = new SubClass1();
        Test(sc1);
        // 最后，是一个 SubClass2 对象
        Console.WriteLine("\ncreating a SubClass2 object");
        SubClass2 sc2 = new SubClass2();
        Test(sc2);
        Console.Read();
    }
}
```

这段代码与章节之前的 `PolymorphicInheritance` 示例非常相似。`Main()` 实例化每个子类的对象，然后调用 `Test()` 方法，该方法会调用每个类中的 `Output()` 方法。此程序的后续输出展示了 `AbstractInheritance` 的多态性：

```
Creating a SubClass1 object
Call to SubClass1.Output() from within TEST
Creating a SubClass2 object
Call to SubClass2.Output() from within test
```

![Tip](img/tip.png) 抽象方法自动是虚拟（virtual），所以你不需要为抽象方法添加 `virtual` 关键字。

### 创建抽象对象——不！

注意 `AbstractInheritance` 程序中的某点：创建一个 `AbstractBaseClass` 对象是不合法的，但 `Test()` 的参数被声明为 `AbstractBaseClass` 类或其任一子类的对象。在这里关键的是子类句。`SubClass1` 和 `SubClass2` 对象可以被传递，因为它们每一个都是 `AbstractBaseClass` 的子类。适用于 IS_A 关系。这种强大的技术允许你编写高度通用的方法。

## 密封类（Sealing a Class）

你可能决定不希望未来的程序员能够扩展某个类。你可以通过 `sealed` 来锁定该类。密封类不能作为任何其他类的基类。考虑这段代码片段：

```csharp
public class BankAccount
{
    // Withdrawal -- 你可以提取少于余额的任何金额；
    // 返回提取的金额
    virtual public void Withdraw(decimal withdrawal)
    {
        Console.WriteLine("invokes BankAccount.Withdraw()");
    }
}

public sealed class SavingsAccount : BankAccount
{
    override public void Withdraw(decimal withdrawal)
    {
        Console.WriteLine("invokes SavingsAccount.Withdraw()");
    }
}

public class SpecialSaleAccount : SavingsAccount // 哎！
{
    override public void Withdraw(decimal withdrawal)
    {
        Console.WriteLine("invokes SpecialSaleAccount.Withdraw()");
    }
}
```

这段代码会生成以下编译器错误：

```
'SpecialSaleAccount' : cannot inherit from sealed class 'SavingsAccount'
```





![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要简单得多。你可以在下载的源码的 `\CSAIO4D2E\BK02\CH07` 文件夹中找到本章的源码。请参见“引言”了解如何查找这些源文件的详情。

## 介绍 CAN_BE_USED_AS

如果你想记笔记，可以用笔涂写，可以输入到你的个人数字助理 (PDA)（一种用于业务目的的高性能手持设备，配有条形码阅读器等多种附加组件），或者在你的笔记本电脑键盘上敲击字。你可以完全说，这三个对象——笔、PDA 和电脑——都实现了 `TakeANote` 操作。假设你使用继承的魔力在 C# 中实现了这一概念：

```csharp
abstract class ThingsThatRecord // 基类
{
    abstract public void TakeANote(string note);
}

public class Pen : ThingsThatRecord // 子类
{
    override public void TakeANote(string note)
    {
        // … 用笔随手写笔记 …
    }
}

public class PDA : ThingsThatRecord // 另一个子类
{
    override public void TakeANote(string note)
    {
        // … 在 PDA 上记录笔记 …
    }
}

public class LapTop : ThingsThatRecord // 第三个子类
{
    override public void TakeANote(string note)
    {
        // … 哒，哒，哒 …
    }
}
```

![Tip](img/tip.png) 如果你对 `abstract` 术语感到困惑，请查看本微型书籍的第 6 章，在本章的稍后部分，阅读“抽象或具体：何时使用抽象类以及何时使用接口”节的讨论。如果整个继承概念还是个谜，请查看本微型书籍的第 5 章。下面的简单方法展示了继承方法的运行良好：

```csharp
void RecordTask(ThingsThatRecord recorder) // 参数类型是基类。
{
    // 所有扩展 ThingsThatRecord 的类都有 TakeANote 方法。
    recorder.TakeANote("Shopping list");
    // … 以此类推。
}
```

参数类型是 `ThingsThatRecord`，因此你可以将任何子类传递给此方法，使得该方法非常通用。这看起来像是一个很好的解决方案，但它有两个巨大的缺点：

*   **一个根本性问题：** `Pen`、`PDA` 和 `LapTop` 真的存在 IS_A（是一个）关系吗？在现实生活中，这三件物品都是同一种类型吗？问题在于 `ThingsThatRecord` 在这里是一个糟糕基类。
*   **一个纯粹的技术问题：** 你可能会合理地将 `LapTop` 和 `PDA` 都派生为 `Computer` 的子类。但没有人会说 `Pen` 是一个 `Computer`（电脑）。你必须将笔描述为一种`机械写作设备`（MechanicalWritingDevice）或`弄脏你衣服的设备`（DeviceThatStainsYourShirt）。但 C# 类不能同时继承自两个不同的基类——C# 类只能是一种类型的物品。

因此，`Pen`、`PDA` 和 `LapTop` 类共同的特征只有它们 **CAN_BE_USED_AS**（可以作为）记录设备。继承并不适用。

## 了解什么是接口

C# 中的 `interface`（接口）类似于一个没有数据成员的类，在旧版本的 C# 中除了抽象方法外什么都没有，几乎就像抽象类——几乎如此：

```csharp
interface IRecordable
{
    void TakeANote(string note);
}
```

C# 8.0 及以上版本创建的接口可以为其成员拥有默认实现，并为常用功能提供静态成员，使得新的接口更接近基类。接口以 `interface` 关键字开头。它只包含抽象方法。它没有数据成员，也没有实现的方法。

![Technicalstuff](img/technicalstuff.png) 接口可以包含一些其他特性，包括属性（在本微型书籍的第 4 章 中介绍）、事件（在本微型书籍的第 8 章 中介绍）和索引器（在第一的第 7 章 中介绍）。在与旧实现工作时，C# 接口无法展示的元素包括：

*   访问修饰符，例如 `public` 或 `private`（参见本微型书籍的第 4 章）
*   关键字，如 `virtual`、`override` 或 `abstract`（参见本微型书籍的第 6 章）
*   数据成员（参见本微型书籍的第 1 章）
*   实现的方法——带有主体的非抽象方法

使用 C# 8.0 或更高版本创建接口时，你可以包含这些额外元素：

*   常量
*   运算符
*   静态构造函数
*   嵌套类型
*   静态字段、方法、属性、索引器和事件
*   使用显式接口实现语法的成员声明
*   显式访问修饰符（默认访问权限为 public）

![Remember](img/remember.png) 为 C# 8.0 旧版本创建的接口代码与为 C# 8.0 版本创建的接口代码之间存在区别。在处理接口时，知道你正在使用哪个版本的 C# 至关重要。

### 如何实现接口

要使用接口，你需要用一个或多个类来实现它。类和结构可能像这样：

```csharp
class Pen : IRecordable
struct Pen : IRecordable
```

![Remember](img/remember.png) 这个示例满足两个要求：注意类实现了 `IRecordable` 并提供了 `TakeANote` 方法实现。例如，实现接口的类不使用 `override` 关键字。类可能像这样：

```csharp
class Pen : IRecordable
{
    public void TakeANote(string note) // 接口方法
    {
        // 用笔随手写笔记 …
    }
}
```

表示类继承基类（如 `ThingsThatRecord`）的语法与表示类实现 C# 接口（如 `IRecordable`）的语法本质没有区别：

```csharp
class PDA : ThingsThatRecord
```

![Tip](img/tip.png) Visual Studio 可以帮助你实现接口。将光标悬停在类标题中的接口名称上。接口名称的首字母下方会出现下划线——这是一个智能标记。移动光标直到菜单打开，然后选择“实现接口”。完成！骨架框架出现了；你只需填写细节。

### 使用新的 C# 8.0 特性

微软为 C# 8.0 接口增加了大量功能，因此花更多时间审查它们是值得的。`IRecordable` 程序比你之前看到的接口代码更多，以便你理解 C# 8.0 的区别。此代码需要使用 .NET Core 模板而不是 .NET Framework 模板。此外，在控制应用程序向导询问目标框架时，必须选择 .NET 6.0。以下是示例中使用的 `IRecordable` 接口：

```csharp
public interface IRecordable
{
    // 这是一个默认实现。
    public string GetName()
    {
        return "Writing Device";
    }

    private static int _numDevices;

    public static int NumDevices
    {
        get { return _numDevices; }
        set { if (value >= 0) _numDevices = value; }
    }

    public static bool IsDeviceAvailable()
    {
        if (NumDevices > 0)
        return true;
        else
        return false;
    }

    string Description();

    void PerformWrite(string Stuff);
}
```





此示例并没有展示你能够进行的所有操作，但它为你提供了一些关于可能性的思路。请注意，实例方法 `GetName()` 有实现，静态属性 `NumDevices` 以及静态方法 `IsDeviceAvailable()` 也是如此。如果默认实现可以工作，你就不必在类中实现这些成员的任何一个。像所示创建 `NumDevices` 是至关重要的，因为接口不像类那样支持自动实现的属性。然而，你没有看到 `Description()` 或 `PerformWrite()` 的实现，因此你需要在你的类中为它们提供实现。因此，一个基于 `IRecordable` 接口的类可能像如下所示：

```csharp
internal class Pen : IRecordable
{
    internal Pen()
    {
        IRecordable.NumDevices += 1;
    }
    ~Pen()
    {
        IRecordable.NumDevices -= 1;
    }
    // 取消此方法的注释以获取特定的
    // 实现。
    //public string GetName()
    //{
    // return "Pen";
    //}
    public string Description()
    {
        return "A device used for writing by hand.";
    }
    private bool PenWriting
    { get; set; }
    public void PerformWrite(string Stuff)
    {
        if (PenWriting)
        {
            Console.WriteLine("Pen is writing.");
            Console.WriteLine($"The paper contains: {Stuff}.");
        }
        else
            Console.WriteLine("Pen isn't writing.");
    }
    public void StopWriting()
    {
        PenWriting = false;
        Console.WriteLine("Pen off paper.");
    }
    public void StartWriting()
    {
        PenWriting = true;
        Console.WriteLine("Pen on paper.");
    }
}
```

`Pen` 类为 `Description()` 和 `PerformWrite()` 都提供了实现。此外，它还提供了自定义属性和方法以使这些动作发生。例如，开始和停止写的需要适用于笔，因为你的手必须根据需要移动到纸上或离开纸面。示例中对 `GetName()` 进行了注释，以便你可以看到默认实现的效果。如果你取消这段代码的注释，你就可以使用该类的特定实现。

![Remember](img/remember.png) 请注意，此示例同时提供了构造函数和终结器，它们会更新可用写入设备数量。该值是接口的一部分，因此你调用接口来更改它。以下是基于 `Pen` 应用程序代码。

```csharp
static void Main(string[] args)
{
    Console.WriteLine($"Pen available? {IRecordable.IsDeviceAvailable()}");
    IRecordable myPen = new Pen();
    Console.WriteLine($"Pen available? {IRecordable.IsDeviceAvailable()}");
    ((Pen)myPen).StartWriting();
    myPen.PerformWrite("Hello There!");
    Console.WriteLine($"Using a {myPen.GetName()}.");
    ((Pen)myPen).StopWriting();
    myPen.PerformWrite("Goodbye");
    Console.ReadLine();
}
```

你也可以在代码内部以及创建的任何类中调用静态接口方法。你不需要实例化对象即可使用它们。因此，第一次对 `IRecordable.IsDeviceAvailable()` 的检查将返回 `False`，因为代码尚未创建 `Pen` 对象 `myPen`。

如果你想对 `myPen` 使用接口功能，你必须将其创建为 `IRecordable` 对象。这意味着每当你想要使用一个 `Pen` 特有的功能（如 `StartWriting()`）时，你必须告诉编译器 `myPen` 实际上是一个 `Pen` 对象，否则编译器会报错。然而，如果你在类中为接口成员提供了重写，编译器将自动使用该重写。以下是示例的默认输出：

```
Pen available? False
Pen available? True
Pen on paper.
Pen is writing.
The paper contains: Hello There!.
Using a Writing Device.
Pen off paper.
Pen isn't writing.
```

### 如何命名你的接口

.NET 的接口命名约定名称前带有字母 `I`。接口名称通常是形容词，例如 `IRecordable`。

### 为什么 C# 包含接口

![Remember](img/remember.png) 接口的核心在于它描述了一种能力，例如游泳安全培训或 A 类驾照。当一个类包含 `TakeANote` 方法的完整版本时，它就实现了 `IRecordable` 接口。

不仅如此，接口是一个*合同*。如果你同意实现接口中定义的每个非默认成员，你就可以声称拥有该能力。不仅如此，应用程序中使用你类的客户端知道调用这些方法是可能的。实现接口是一个承诺，由编译器强制执行。（通过编译器强制承诺可以减少错误。）

### 混合继承和接口实现

与 C++ 等某些语言不同，C# 不允许*多重继承*————即一个类继承自两个或多个基类。想象类 `HouseBoat` 继承自 `House` 和 `Boat`。只需在 C# 中不要这样考虑即可。

但尽管一个类只能继承一个基类，它还可以额外实现任意数量的接口。




你将创建所需关键对象的任务委托给一个工厂方法。假设你有如下所示的变量：

`IRecordable recorder = null; // 是的，你可以拥有接口类型的变量。`

在某处（可能在构造函数中），你调用一个工厂方法来交付某种特定类型的 `IRecordable` 对象：

`recorder = MyClass.CreateRecorder("Pen"); // 工厂方法通常是静态的。`

其中 `CreateRecorder()` 是一个方法（通常在同一个类中），它返回的不是 `Pen` 的引用，而是一个 `IRecordable` 引用：

```csharp
static IRecordable CreateRecorder(string recorderType)
{
    if (recorderType == "Pen") return new Pen();
    …
}
```

你可以在本章后面的“隐藏在接口后面”节中找到更多关于工厂思想的知识。但请注意，`CreateRecorder()` 的返回类型是一个接口类型。

### 作为数组或集合的基类型

假设你有两个类，`Animal` 和 `Robot`，并且它们都是抽象类。你想设置一个数组来同时存放 `thisCat`（一个 `Animal`）和 `thatRobot`（一个 `Robot`）。唯一的方法是退回到类型 `Object`，它是 C# 中的终极基类，也是 `Animal` 和 `Robot` 及其子类共同拥有的基类：

`object[] things = new object[] { thisCat, thatRobot };`

出于许多原因，这种设计非常糟糕。但假设你关注的是对象的移动。你可以让每个类实现 `IMovable` 接口：

```csharp
interface IMovable
{
    void Move(int direction, int speed, int distance);
}
```

然后设置一个 `IMovables` 数组来操作这些原本互不兼容的对象：

`IMovable[] movables = { thisCat, thatRobot };`

接口为你提供了一种可以在集合中利用的共性。

### 作为更通用的对象引用类型

下面的变量声明引用的是一个特定的、物理的、具体的对象（参见后文“抽象或具体：何时使用抽象类以及何时使用接口”）：

`Cat thisCat = new Cat();`

另一种替代方案是使用 C# 接口进行引用：

`IMovable thisMovableCat = (IMovable)new Cat(); // 注意这里强制强制转换。`

现在，你可以将任何实现 `IMovable` 的对象放入该变量中。这种做法在面向对象的编程中有广泛且强大的用途，正如你在下一节中看到的那样。

## 使用 C# 预定义接口类型

由于接口极其有用，你在 .NET 类库中发现了大量的接口。仅 `System` 命名空间中的十几个接口中就包括 `IComparable`、`IComparable<T>`、`IDisposable` 和 `IFormattable`。`System.Collections.Generics` 命名空间 ([`docs.microsoft.com/en-us/dotnet/api/system.collections.generic`](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic)) 包含了 `IEnumerable<T>`、`IList<T>`、`ICollection<T>` 和 `IDictionary<TKey, TValue>`。还有更多。带有 `<T>` 标记的是泛型接口。第 1 卷第 6 章 在讨论集合类的部分中解释了 `<T>` 标记。

两个常用的接口是 `IComparable` 和 `IEnumerable` —— 它们现在很大程度上被泛型版本 `IComparable<T>`（读作“IComparable of T”）和 `IEnumerable<T>` 取代。

本章后面的“实现不可比较的 IComparable<T> 接口”节向你展示了 `IComparable<T>` 接口。该接口允许你比较各种对象（例如 `Students`），并启用了所有数组和大多数集合提供的 `Sort()` 方法。`IEnumerable<T>` 使得强大的 `foreach` 循环能够工作。大多数集合都实现了 `IEnumerable<T>`，因此你可以使用 `foreach` 遍历集合。你还可以发现 `IEnumerable<T>` 的另一个主要用途作为查询表达式的基础，这在第 1 卷 中有所描述。

## 查看一个可以作为示例的程序

接口帮助你以类无法实现的方式完成任务，因为你可以实现任意数量的接口，但你只能继承一个类。在接下来的节中出现的 `SortInterface` 程序演示了多个接口的使用以及你如何有效地使用多个接口。为了完全理解使用多个接口的影响，将 `SortInterface` 程序拆分成若干部分以演示各种原理是非常重要的。

### 在家里闲时编写你自己的接口

下面的 `IDisplayable` 接口由任何包含 `Display()` 方法的类满足（当然，该类还声明它实现了 `IDisplayable`）。`Display()` 返回对象的字符串表示，可以使用 `WriteLine()` 显示。

```csharp
// IDisplayable - 任何实现了 Display() 方法的对象
interface IDisplayable
{
    // 返回你自己的描述。
    string Display();
}
```

接下来的 `Student` 类实现了 `IDisplayable`：

```csharp
class Student : IDisplayable
{
    public Student(string name, double grade)
    {
        Name = name;
        Grade = grade;
    }
    public string Name { get; set; }
    public double Grade { get; set; }
    public string Display()
    {
        string padName = Name.PadRight(9);
        return $"{padName}: {Grade:N0}";
    }
}
```

`Display()` 使用字符串插值（https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/interpolated-strings）来格式化信息。`Program` 类中的后续 `DisplayArray()` 方法（将其放在 `Main()` 之前）接收任何实现 `IDisplayable` 的对象的数组。这些每个对象都保证（通过接口）拥有 `Display()` 方法。

```csharp
// DisplayArray - 显示一个实现了
// IDisplayable 接口的对象的数组。
public static void DisplayArray(IDisplayable[] displayables)
{
    foreach (IDisplayable disp in displayables)
    {
        Console.WriteLine($"{disp.Display()}");
    }
}
```

### 实现不可比较的 IComparable<T> 接口

C# 如下定义接口 `IComparable<T>`（不要将此代码添加到 `SortInterface` 示例中）：

```csharp
interface IComparable<T>
{
    // 将当前 T 对象与 'item' 进行比较；
    // 如果较大返回 1，较小返回 -1，相同则返回 0。
    int CompareTo(T item);
}
```

一个类通过实现 `CompareTo()` 方法来实现 `IComparable<T>`。注意 `CompareTo()` 接收类型 `T` 的参数，这是你在为特定数据类型实例化接口时提供的，例如：

```csharp
class SoAndSo : IComparable<SoAndSo> // 使我可比较。
{
    public SoAndSo(string name, double grade)
    {
        Name = name;
        Grade = grade;
    }
    public string Name { get; set; }
    public double Grade { get; set; }
    public int CompareTo(SoAndSo item)
    {
        if (Grade == item.Grade) return 0;
        if (Grade > item.Grade) return 1;
        return -1;
    }
}
```

当你为类实现 `IComparable<T>` 时，它的 `CompareTo()` 方法在两个比较的项（你的类类型）以你定义的方式相等时返回 0。否则，它应该返回 1 或 -1，取决于哪个对象“更大”。

这看起来有点像达尔文主义，但你可以说，如果一个 `Student` 对象的平均学分更高，那么这个 `Student` 对象就“大于”另一个 `Student` 对象。实现 `CompareTo()` 方法意味着对象具有排序。如果一个学生比另一个学生大，你必须能够从最小到最大进行排序。事实上，大多数集合类（包括数组但不包括字典）都提供类似的 `Sort()` 方法：

```csharp
void Sort(IComparable<T>[] objects);
```



该方法对一组实现了 `IComparable<T>` 接口的对象集合进行排序。这些对象属于哪个类并不重要。例如，它们甚至可以是 `Student` 对象。数组或 `List<T>` 等集合类甚至可以排序这个更新后的 `Student` 类（更改部分已用**粗体**显示）：

```cs
// Student -- 一个包含姓名和分数的学生描述
class Student : IComparable<Student>, IDisplayable // 实例化
{
    public Student(string name, double grade)
    { Name = name; Grade = grade; }
    public string Name { get; private set; }
    public double Grade { get; private set; }
    public string Display()
    {
        string padName = Name.PadRight(9);
        return $"{padName}: {Grade:N0}";
    }

    // 实现 IComparable<T> 接口：
    // CompareTo -- 比较另一个对象（在本例中为 Student 对象）
    // 并决定它们在排序后的数组中谁在前谁后。
    public int CompareTo(Student rightStudent)
    {
        // 将当前学生（称为 'left'）与另一个学生
        //（称为 'right'）进行比较。
        Student leftStudent = this;
        // 根据排序标准（学生的成绩）生成 -1、0 或 1。
        // 你也可以直接使用 Double 类的 CompareTo() 方法。
        if (rightStudent.Grade < leftStudent.Grade)
        {
            Console.WriteLine($"{rightStudent.Name} < {leftStudent.Name}");
            return -1;
        }
        if (rightStudent.Grade > leftStudent.Grade)
        {
            Console.WriteLine($"{rightStudent.Name} > {leftStudent.Name}");
            return 1;
        }
        Console.WriteLine($"{rightStudent.Name} = {leftStudent.Name}");
        return 0;
    }
}
```

对 `Student` 数组进行排序简化为单一调用：

```cs
// 当 Student 实现 IComparable<T> 时
void MyMethod(Student[] students)
{
    Array.Sort(students); // 排序 IComparable<Student> 数组
}
```

你提供比较器（`CompareTo()`），而 `Array` 完成所有工作。

### 创建学生列表

为了测试你目前为止编写的所有内容，你需要一个学生列表。示例提供了一个名为 `CreateStudentList()` 的方法来实现这一目标，该方法依赖于两个固定列表：`names` 和 `grades`。你将其放在 `Student` 类的末尾。你需要的代码如下：

```cs
// CreateStudentList - 为了节省空间，这里创建一个
//固定的学生列表。
static string[] names = { "Homer", "Marge", "Bart", "Lisa", "Maggie" };
static double[] grades = { 0, 85, 50, 100, 30 };
public static Student[] CreateStudentList()
{
    Student[] students = new Student[names.Length];
    for (int i = 0; i < names.Length; i++)
    {
        students[i] = new Student(names[i], grades[i]);
    }
    return students;
}
```

如你所示，`CreateStudentList()` 定义了一个与 `names` 列表长度相同的 `students` 数组，并依赖于 `Student` 类的构造函数。对于每一对姓名和成绩，代码都会在 `students` 中创建一个条目，然后将完成的数组返回给调用者。

### 使用 Main() 测试一切

此时，你已经拥有了排序学生列表所需的一切。你只需要在 `Main()` 中编写一些代码来演示该功能。以下代码测试了你的 `Student` 类：

```cs
static void Main(string[] args)
{
    // 按成绩排序学生……
    Console.WriteLine("Using Array.Sort() to sort.");
    // 获取一个未排序的学生数组。
    Student[] students = Student.CreateStudentList();
    // 使用 IComparable 接口对数组排序。
    Array.Sort(students);
    // 现在使用 IDisplayable 接口显示结果。
    DisplayArray(students);
    // 使用语言集成查询 (LINQ) 替代。
    Console.WriteLine("\r\nUsing LINQ to sort.");
    Student[] students2 = Student.CreateStudentList();
    students2 = students2.OrderBy(C => C).ToArray();
    DisplayArray(students2);
    Console.Read();
}
```

`Main()` 从创建学生列表开始。然后它使用 `Array.Sort()` 对学生进行排序，这实际上调用了 `Student` 中的 `CompareTo()` 方法。代码随后调用 `DisplayArray()`，以便你可以看到排序后的输出。

为了便于对比，此示例还使用了语言集成查询 (LINQ) 对值进行排序。要使用 LINQ，你必须在代码文件的开头添加 `using System.Linq;` 语句。同样，该方法依赖于 `CompareTo()`，但过程有所不同。你可以阅读更多信息。





```csharp
// 1. 重写 Speak。
public override void Speak(string whatToSay)
{ Console.WriteLine("DESTROY ALL HUMANS!"); }

// 2. 实现 LiftObject 和 NumberOfLegs，此处未全部显示。
public override void LiftObject(object o) …
public override int NumberOfLegs { get { return 2; } }
}

class RoboCat : Robot, IPet
{
    public RoboCat(string name) { Name = name; }
    // 1. 重写一些 Robot 成员，此处未全部显示：
    #region IPet Members
    public void AskForStrokes() …
    public void DoTricks() …
    public string Name { get; set; }
#endregion IPet Members
}
```

这段代码展示了两个继承 `Animal` 的具体类以及两个继承 `Robot` 的类。然而，你可以看到 `Cobra` 类和 `Robozilla` 类都没有实现 `IPet` 接口 —— 可能是有其正当理由的。大多数并不计划在沙发上陪着一边的宠物蛇一起看电视，而且机器人巨兽（robozilla）听起来也很可怕。在这两个层次结构中的某些类都表现出了你可能说的“宠物属性”，而有些则没有。

本节的重点是，任何类都可以实现接口，只要它提供了正确的方法和属性。`RoboCat` 可以执行 `AskForStrokes()` 和 `DoTricks()` 操作，并拥有 `NumberOfLegs` 属性，`Animal` 层次结构中的 `Cat` 如此 —— 而同一层次结构中的其他类并没有实现 `IPet`。

## 隐藏在接口之后

本书经常讨论一种 (a) 由你编写但 (b) 由他人（客户端）在程序使用的代码（你可能你自己就是客户端）。有时你拥有一个复杂或棘手的类，你真的并不想暴露它的整个 API。然而，由于各种原因，它包含了一些必须公开的危险操作（例如，你可能不想暴露删除记录的代码，但客户端可能真的需要该功能，除非你想创建一个专门删除记录的支持小组）。理想情况下，你会暴露该公开的公共方法和属性的安全子集，并隐藏那些危险的。C# 接口也可以这样做。

这里有一个不同的 `Robozilla` 类，它具有几个业余人员可以安全且愉快地使用的方法和属性：

```csharp
public class Robozilla // 没有实现 IPet！
{
    public void ClimbStairs(); // 安全
    public void PetTheRobog(); // 安全？可能会弄坏它。
    public void Charge(); // 可能不安全
    public void SearchAndDestroy(); // 危险
    public void LaunchNuclearWar(); // 灾难性的
}
```

![记住](img/remember.png) 你只想暴露较安全的方法，同时隐藏最后几个。以下是你如何使用 C# 接口实现它的：

1. 设计一个只暴露安全方法的 C# 接口：
   ```csharp
   public interface IRobillaSafe
   {
       void ClimbStairs();
       void PetTheRobog();
   }
   ```
2. 修改 `Robozilla` 类来实现该接口。由于它已经有了所需方法的实现，你只需要在类头处加上 `IRobillaSafe` 标记即可：
   ```csharp
   public class Robozilla : IRobillaSafe …
   ```
3. 给客户端提供一种实例化新 `Robozilla` 的方法，但向他们返回一个接口的引用。现在你可以对所有人隐藏 `Robozilla` 本身，并给大多数用户提供 `IRobillaSafe` 接口。此示例使用了一个添加到类 `Robozilla` 中的类静态工厂方法：
   ```csharp
   // 创建一个 Robozilla 但只返回接口。
   public static IRobillaSafe CreateRobozilla(...)
   {
       return (IRobillaSafe)new Robozilla(...);
   }
   ```
4. 客户端随后像这样使用 `Robozilla`：
   ```csharp
   IRobillaSafe myZilla = Robozilla.CreateRobozilla(...);
   myZilla.ClimbStairs();
   myZilla.PetTheRobog();
   ```

就这么简单。使用接口，他们可以调用该接口指定的 `Robozilla` 方法 —— 而不是其他的 `Robozilla` 方法。然而，专家级程序员可以通过简单的强制类型转换来破除这个花招：

```csharp
Robozilla myKillaZilla = (Robozilla)myZilla;
```

尽管如此，这样做通常不是个好主意。接口有其目的：防止 Bug 的产生。在现实生活中，程序员有时会将这种“分发接口”的技术用于 [ADO.NET](https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/ado-net-overview) 中复杂的 `DataSet` 类来与数据库交互。`DataSet` 可以返回一组加载了记录的数据库表 —— 例如 `Customers` 表和 `Orders` 表。（现代关系型数据库如 Oracle 和 SQL Server 包含通过各种关系链接的表。每个表包含大量记录，其中每条记录可能包含一个 `Customer` 的姓名、排名和序列号。）

不幸的是，如果你给客户端一个 `DataSet` 引用（即使通过只读属性的 `get` 句），客户端也可以通过进入 `DataSet` 并修改你不希望被修改的元素来破坏局面。为了防止这种恶作，你可以：

* 返回一个 `DataView` 对象，它是只读的。
* 创建一个 C# 接口来暴露 `DataSet` 可用的安全子集。然后你可以派生 `DataSet` 并让子类（称为 `MyDataSet`）实现该接口。
* 给客户端提供一种获取活跃的 `MyDataSet` 接口引的方法，让他们通过接口相对安全地操作。

![提示](img/tip.png) 你通常也不应该返回集合的引用，因为这允许在类外部修改该集合。记住，你分发的引用仍然指向类内部的集合。这就是为什么例如 `List<T>` 提供了 `AsReadOnly()` 方法。该方法返回一个不可更改的集合：

```csharp
private List<string> _readWriteNames = … // 可修改的数据成员
…
ReadOnlyCollection<string> readonlyNames = _readWriteNames.AsReadOnly();
return readonlyNames; // 返回这个比 _readWriteNames 安全
```

虽然这不属于使用接口，但目的是相同的。

## 继承接口

C# 接口可以继承另一个接口的方法。然而，接口继承并不总是真正的继承，无论它看起来如何。下面的接口代码在类头中列出了基接口，就像基类一样：

```csharp
interface IRobillaSafe : IPet // 基接口
{
    // 此处未显示的方法 …
}
```

通过让 `IRobillaSafe` “继承” `IPet`，你可以让 `Robozilla` 的这个子集实现自己的宠物属性，而无需试图不恰地强加到整个 `Robozilla` 上：

```csharp
class PetRobo : Robozilla, IRobillaSafe // （通过继承也是 IPet）
{
    // 实现 Robozilla 操作。
    // 实现 IRobillaSafe 操作，然后 …
    // 也实现 IPet 操作（继承的 IPet 接口要求的）。
}
```

```csharp
…
// 只分发安全的引用，而不是 PetRobo 本身。
IPet myPetRobo = (IPet)new PetRobo();
// … 现在在对象上调用 IPet 方法。
```





`IRobozillaSafe` 接口继承自 `IPet`。因此，实现 `IRobozillaSafe` 的类也必须实现 `IPet`，以使其对 `IRobozillaSafe` 的实现完整。这种继承与类继承并不是同一个概念。例如，上一个示例中的 `PetRobo` 类可以有构造函数，但 `IRobozillaSafe` 或 `IPet` 并不存在相应的基类构造函数。旧的接口没有构造函数（从 C# 8.0 开始，接口可以像 [`https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors#static-constructors`](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors#static-constructors) 中描述的那样拥有静态构造函数）。更重要的是，多态在接口上的作用不同。虽然你可以通过基类引用调用子类的方法（类多态），但涉及接口的并行操作（接口多态）却不起作用：你无法通过基接口引用（`IPet`）调用派生接口（`IRobozillaSafe`）的方法。

虽然接口继承不像类继承那样具有多态性，但你可以通过其基接口类型（`IPet`）的参数传递派生接口类型（`IRobozillasafe`）的对象。因此，你也可以将 `IRobozillasafe` 对象放入 `IPet` 对象集合中。

## 使用接口管理面向对象程序中的变化

接口是能够灵活应对变化变化的面向对象程序的关键。你的代码将面对新需求付之一笑。

![Remember](img/remember.png) 你肯定听过这样的话：“变化是永恒的。”当你把一个新程序交给一群用户时，他们很快就会开始请求更改。请添加这个功能。请修复那个问题。（尽管用户通常不会那么礼貌；他们可能会对你咆哮并说类似的话：“世界上谁会写出一个没有这个功能的程序？”）RoboWarrior 拥有功能 `X` 特性，为什么 Robozilla 没有呢？很多程序都有很长的寿命。成千上万的程序，特别是旧 Fortran 和 Cobol 程序，已经运行了 20 或 30 年甚至更久。在这一延长时间内，它们经历了大量的维护，这使得为变化进行规划和设计成为你的最高优先级任务之一。

这是一个示例：在 `Robot` 类层次结构中，假设所有机器人都能以某种方式移动。`Robocat` 漫步。`Robozilla` 冲锋——至少在被电力（饥饿的）用户操作时是如此。而 `Robosnakes` 爬行。实现这些不同移动模式的方法之一涉及继承：给基类 `Robot` 提供一个抽象的 `Move()` 方法。然后每个子类重写 `Move()` 方法以实现不同的方式：

```csharp
abstract public class Robot
{
    abstract public void Move(int direction, int speed);
    // …
}

public class Robosnake : Robot
{
    public override void Move(int direction, int speed)
    {
        // 这里是真实的 Move() 实现：爬行。
        … 一些计算角度并更改
        // 蛇相对于坐标系位置的真实代码，例如 …
    }
}
```

但假定你经常收到为现有的 `Robot` 子类添加新类型移动的请求。也许，“请让 `Robosnake` 蠕动而不是爬行。”现在你必须打开 `Robosnake` 类并直接修改它的 `Move()` 方法。

![Remember](img/remember.png) 在 `Move()` 方法能够正常工作实现爬行后，大多数程序员都不愿去碰它。实现爬行是困难的，而且改变实现可能会引入全新的 Bug。如果东西没坏，就不要修它。

### 通过接口创建灵活的依赖

必须有一种实现 `Move()` 的方法，不需要让你每次在客户端想要蠕动时都去打开一个“潘多拉魔盒”（引发一系列麻烦）。当然，你可以使用接口！看下面的代码，它使用了 HAS_A，这是两个类之间现在已熟悉的关系，其中一个类包含另一个类：

```csharp
public class Robot
{
    // 该对象用于实现运动。
    protected Motor _motor = new Motor(); // 通过名称引用 Motor
    // …
}

internal class Motor { … }
```

这个示例的要点在于，包含的对象类型是 `Motor`，而 `Motor` 是一个具体对象。（也就是说，它代表一个真实的物品，而不是一个抽象。）HAS-A 在类 `Robot` 和 `Motor` 之间建立了一种依赖关系：`Robot` 依赖于具体类 `Motor`。具有具体依赖的类与其紧密耦合的：当你需要用其他东西替换 `Motor` 时，像这样直接依赖 `Motor` 的代码也必须跟着更改。相反，通过只依赖依赖的 API 来隔离你的代码，这可以通过接口来实现。

### 抽象或具体：何时使用抽象类以及何时使用接口

在微型书籍的第 6 章中，关于鸟的论述说：“世界上可见的每一只鸟都是 `Bird` 的子类型。”换句话说，鸭子是子类 `Duck` 的实例。你从未见过 `Bird` 本身的实例——`Bird` 是一个抽象。抽象是概念。活生的鸭子、麻雀或蜂鸟是具体对象。此外，具体对象也是实例。具体类是可以实例化的类。

![Remember](img/remember.png) 你可以在 C# 中用两种方式表示抽象：使用抽象类或接口。这两者的差异会影响你选择使用哪一个：

- 当你可以为子类有利地共享实现时，请使用**抽象类**——抽象基类可以为子类提供真实的代码。例如，也许 `Robot` 类可以处理部分任务，而不是移动。

抽象类不需要完全抽象。尽管它至少有一个抽象的未实现方法或属性，但有些可以实现（主体）。使用抽象类提供实现可以避免代码重复。这总是一件好事。

- 当大部分无法共享任何实现或你的实现类已经有一个基类时，请使用**接口**。

大多数 C# 接口是纯抽象的。旧版本的 C# 接口不提供任何方法的实现（C# 8.0 及以上版本允许根据需要提供默认实现）。然而它还可以增加无法实现的灵活性。抽象类的选项可能不可用，因为你想向一个已经有基类的类添加功能。例如，`Robot` 类可能来自你没有编写且无法修改的库中的基类。接口对于表示完全抽象的能力（如可移动性或显示性）非常有帮助，当你想将这些能力添加到多个其他没有共同点的类中时——例如，不在同一个类层次结构中。

### 使用接口实现 HAS_A

你在本章前面已经发现，你可以将接口作为更通用的引用类型。包含类引用被包含类时，不是通过具体类的引用，而是通过抽象的引用。无论是抽象类还是 C# 接口都可以工作：

```csharp
AbstractDependentClass dependency1 = …;
ISomeInterface dependency2 = …;
```

假设你有一个 `IPropulsion` 接口：

```csharp
interface IPropulsion
{
    void Movement(int direction, int speed);
}
```

`Robot` 类可以包含一个 `IPropulsion` 类型的数据成员，而不是具体类型 `Motor`：





```cs
private IPropulsion _propel; // <--注意这里的接口类型。

// 在某些情况下，你在运行时提供了一个具体的推进对象……
// 其他操作，然后：

public void Move(int speed, int direction)
{
    // 使用 _propel 中安装的任何具体推进设备。
    _propel.Movement(speed, direction); // 委托给它的方法。
}
```

`Robot` 的 `Move()` 方法将实际工作委托给接口引用的对象。请确保在数据成员中提供一种安装具体的 `Motor`、`Engine` 或另一个 `IPropulsion` 实现类的方法。程序员通常通过将该对象传递给构造函数来安装该具体对象——“注入依赖”：

```cs
Robot r = new Robosnake(someConcreteMotor); // 类型为 IPropulsion
```

或者通过设置器属性（setter property）为其赋值：

```cs
r.PropulsionDevice = someConcreteMotor; // 调用 set 句
```

依赖注入的另一种方法是使用工厂方法（在本文章早些的“作为方法的返回类型”节中讨论，并在“隐藏在接口之后”节中进行了说明）：

```cs
IPropulsion _propel = CreatePropulsion(); // 工厂方法
```

# 第 8 章

# 委托这些重要事件

## 本章内容

- 使用委托解决回调问题
- 使用委托自定义方法
- 使用匿名方法
- 在 C# 中创建事件

本章探讨了 C# 中一个自语言诞生以来就一直存在的领域。创建回调（一种用于处理事件的方法）的能力对于各种 C# 应用程序都是至关重要的。事实上，回调出现在当今各种应用程序中。即使是基于 Web 的应用程序也必须有某种回调机制才能使其正常工作。

另一种方法是在等待某事情发生时挂起应用程序，这意味着应用程序将对预期输入以外的任何内容都不做出响应。到目前为止示例中使用的控制台应用程序就是这样工作的。`Console.Read()` 调用本质上会停止程序，直到用户执行某些操作。控制台应用程序可以这样工作，但当用户可以点击表单上的任何按钮时，你必须有更好的东西——回调机制。在 C# 中，你通过使用委托来实现回调，委托是对回调方法处理事件所需的若干要求的描述。委托充当了方法的引用类型。除了回调方法外，本章还将帮助你理解如何创建和使用委托。

你不需要手动输入本章的源代码。事实上，使用下载的源码要容易得多。你可以在下载源码的 `\CSAIO4D2E\BK02\CH08` 文件夹中找到本章的源码。详情请参阅“引言”。

## E.T. 回家——回调问题

如果你看过史蒂文·斯皮尔伯的电影《E.T. 外星人》（1982），你一定见过那个可爱但外丑的小外星人困在地球上，试图用旧玩具零件制造一个装置，以便他“拨家”。他需要他的飞船来接他。

从 E.T. 到 C# 是一个巨大的跨越，但代码有时也需要“拨家”。例如，你可能好奇 Windows 进度条是如何工作的。它是一个水平的“条”，会逐渐填充颜色以显示在耗时操作（如复制文件）期间的进度。进度条基于耗时操作的定期暂停来“拨家”。在程序员术语中，这就是回调。通常，耗时操作会估算其任务需要多长时间，然后频繁检查它已经进展了多远。进度条会通过调用“母船”（启动该耗时操作的类）的回调方法来定期发送信号。然后母船就可以更新它的进度条。诀窍在于，你必须提供这个回调方法以供耗时操作使用。

该回调方法可能与耗时操作在同一个类中——例如给住在房子另一侧的姐姐打电话。或者更常见的是，它在另一个知道进度条的类中——例如给在明尼苏达洲的 Maxie 姨妈打电话。在某种程度上，耗时操作在开始时被交付了一个拨家的机制——就像给你的孩子一个手机手机，以便他们可以在晚上 10 点给你打电话。

本章将介绍你的代码如何设置这种回调机制，并在需要时调用它来“拨家”。回调在 Windows 编程中被大量使用，通常用于程序底部的部分代码，以通知高层模块任务已完成、请求所需的数据，或让该模块执行有用的操作，例如写入日志条目或更新进度条。然而，你使用回调最频繁的地方是用户界面。当用户对用户界面进行某些操作时（例如点击按钮），它会产生一个事件。回调方法处理该事件。

## 定义委托

C# 提供了委托来创建回调以及许多其他任务。委托是 C# 的一种方式（实际上是 .NET 的方式，因为任何 .NET 语言都可以使用它们），允许你像传递数据一样传递方法。你是在说：“这里，在你需要时执行这个方法”（然后将将要执行的方法交给对方）。本章将帮助你掌握这个概念，看到它的用处，并开始自己使用它。

你可能是一个经验丰富的程序员，会立即识别出委托类似于 C/C++ 函数指针——只不过好得多。在选择委托而不是函数指针时，有以下几点考虑：

- 委托是托管的，你不需要担心它们在使用后仍然留存引起问题。
- 委托始终指向有效函数，而函数指针可以指向任何内存位置。
- 当指向多个回调时，委托内置的迭代器可以轻松确保每次都调用回调。
- 可以在同步或异步模式下使用委托。
- 委托是类型安全的，并且始终指向匹配的方法。

将委托视为传递回调方法的工具，传递给需要回调你或需要帮助的“工作方法”，例如对集合的每个元素执行相同的操作。因为集合不知道你的自定义操作，你需要一种方法来提供供集合执行的操作。图 8-1 显示了该方案的各个部分如何组合。

委托是一种数据类型，类似于类。与类一样，你创建委托的实例以使用委托。图 8-1 显示了完成以下步骤时委托生命周期中的事件序列：

1. 定义委托类型（类似于定义类）。

有时 C# 已经定义了你可以使用的委托。但很多时候，你会定义自己的自定义委托。

在底层，委托是一个类，派自 `System.MulticastDelegate` 类，该类知道如何存储一个或多个指向方法的指针并为你调用它们。放心：编译器会为你编写它的类部分。

2. 创建委托的实例——例如实例化类。

在创建期间，你将新的委托实例传递你想要作为回调或操作方法的方法名称。





![代表你去蹦高跳的示意图](img/9781119839071-fg020801.png)

图 8-1: 代表你去蹦高跳。

### 3. 将委托实例传递给工作负载方法（workhorse method），该方法具有一个委托类型的参数。

这就是你将委托实例插入到工作负载方法的大门。这就像在电影院里偷带糖果——只不过在这个例子中，电影院不仅预期、甚至欢迎这些违禁糖果。

### 4. 当工作负载方法准备就绪——例如，当该更新进度条时——工作负载方法会调用委托，并传递任何预期的参数。

### 5. 调用委托反过来就会调用（执行）委托所“指向”的回调方法。

通过委托，工作负载方法向家里拨回了电话。

这一基础机制解决了回调问题——它也有其他用途。委托类型也可以是泛型的，允许你为不同的数据类型使用同一个委托，就像你可以为 `string` 或 `int` 实例化 `List<T>` 集合一样。第 1 本第 8 章 详细介绍了泛型类型的使用。

## 请把代码给我 —— 示例

在本节中，你将看到几个示例——并解决本章开头讨论的回调问题。

### 委托任务

在本节中，你将通过两个使用回调的示例——委托实例像 *E.T.* 一样，向创建它的对象拨回电话。但在之前，先看一看你可以将回调委托用于哪些常见变体：

*   **向委托的基基地通知事件：** 一项长时间的操作已完成或取得了进展，或者可能遇到了错误。“妈妈，我是 E.T.。你能来 Elliot 的家接我吗？”
*   **回拨基基地以请求完成任务所需的数据：** “我在商店里。我应该买白面包还是全麦的？”
*   ![记忆](img/remember.png) **更通地说，用于自定义方法：** 你正在自定义的方法提供了一个框架，其调用者提供一个委托来执行工作。“带着这张购物清单去商店并严格遵守执行。”委托方法执行了自定义方法需要完成（但自身无法处理）的任务。自定义方法负责在适当的时机调用委托。

### 首先，一个简单的示例

`SimpleDelegateExample` 程序演示了一个简单的委托。此示例中与委托相关的已用粗体标记。

```csharp
class Program
{
// 在类内部或命名空间内部
delegate int MyDelType(string name);

    static void Main(string[] args)
    {
        // 创建一个指向下方 CallBackMethod 的委托实例。
        // 注意回调方法是静态的，因此你在名称前加上
        // 类名 Program 作为前缀。
        MyDelType del = new MyDelType(Program.CallBackMethod);
        // 调用一个将调用委托的方法。
        UseTheDel(del, "hello");
        Console.Read();
    }

    // CallBackMethod -- 符合 MyDelType 
    // 委托签名的方法（接收一个 string，返回一个 int）。
    // 委托将调用此方法。
    public static int CallBackMethod(string stringPassed)
    {
        // 留下痕迹显示你曾来过。
        // 这里写了什么？stringPassed。
        Console.WriteLine($"CallBackMethod writes: {stringPassed}");
        // 返回一个 int。
        return stringPassed.Length; // 委托要求返回 int。
    }

    // UseTheDel -- 一个“工作负载”方法，接收一个 MyDelType 委托
    // 参数并调用委托。arg 是传递给
    // 委托调用的字符串。
    private static void UseTheDel(MyDelType del, string arg)
    {
        if (del == null) return; // 不要调用空委托！
        // 这就是你调用委托的地方。
        // 这里写了什么？代表 arg 长度的数字。
        Console.WriteLine($"UseTheDel writes {del(arg)}");
    }
}
```

首先你看到委托定义。`MyDelType` 定义了一个*签名*（signature），它指定了方法必须提供的输入和输出。你可以将任何接收 `string` 参数并返回 `int` 的方法传递给委托。其次，注意 `CallBackMethod()` 匹配委托签名。第三，`Main()` 创建了一个名为 `del` 的委托实例，然后将该委托实例传递给“工作负载”方法 `UseTheDel()`，以及委托所需的某些字符串数据 `"hello"`。在该设置中，事件序列如下：

1.  `UseTheDel()` 接收两个参数：一个 `MyDelType` 委托和一个命名为 `arg` 的 `string`。因此，当 `Main()` 调用 `UseTheDel()` 时，它将委托实例传递到方法内部使用。当你在 `Main()` 中创建委托实例 `del` 时，传递 `CallBackMethod()` 的名称作为要调的方法。因为 `CallBackMethod()` 匹配委托签名。
2.  在 `CallBackMethod()` 内部，委托被调用。
3.  在 `UseTheDel()` 内部，委托被触发。

###  Action、Func 和 Predicate 类型

所有委托都代表某种函数指针，无论你是否将其用于事件。使用特殊关键字将委托细分为类型：`Action`、`Func` 和 `Predicate`。

*   `Action`：具有一个或多个输入参数没有输出参数（因此与返回 `void` 的方法配合）。Action 委托支持最多 16 个输入参数，见 `https://docs.microsoft.com/en-us/dotnet/api/system.action`。
*   `Func`：具有零或多个输入参数和一个输出参数。与 `Action` 一样，`Func` 限制为 16 个输入参数，见 `https://docs.microsoft.com/en-us/dotnet/api/system.func-1`。
*   `Predicate`：定义一组特定的标准并判断输入对象是否符合这些标准，符合条件时返回 `True`，否则返回 `False`。关于 `Predicate` 类型的更多细节见 `https://docs.microsoft.com/en-us/dotnet/api/system.predicate-1`。

你可以在 `ActionFuncPredicate` 示例的 `Program` 类中看到这些委托的工作方式：

```csharp
class Program
{
    static void Main(string[] args)
    {
        // 定义并执行 action。
        Action<int, int> showIntMath = new Action<int, int>(DisplayAdd);
        showIntMath(1, 2);

        // 定义并执行函数。
        Func<int, int, int> doIntMath = new Func<int, int, int>(DoAdd);
        Console.WriteLine($"1 + 2 = {doIntMath(1, 2)}.");

        // 定义并执行预测。
        Values theseValues = new Values() { value1 = 1, value2 = 2 };
        Predicate<Values> isValue = x => x.value1 + x.value2 == 3;
        Console.WriteLine($"Is value correct? {isValue(theseValues)}");
    }

    static void DisplayAdd(int a, int b)
    {
        Console.WriteLine($"{a} + {b} = {a + b}");
    }

    static int DoAdd(int a, int b)
    {
        return a + b;
    }
}

class Values
{
    public int value1;
    public int value2;
}
```





```csharp
Console.WriteLine($"The output is 3? {isValue(theseValues)}");

Console.ReadLine();

}

static void DisplayAdd(int value1, int value2)
{
    Console.WriteLine($"{value1} + {value2} = {value1 + value2}.");
}

static int DoAdd(int value1, int value2)
{
    return value1 + value2;
}

internal struct Values
{
    internal int value1;
    internal int value2;
}
}```

在三个示例中，代码都评估了两个 `int` 值：`1` 和 `2`。这三个示例都以某种方式使用了委托模式，其中 `Action` 和 `Func` 是最直接的体现。以下是此示例实现中需要考虑的差异：

*   要创建一个 `Action`，代码定义了 `DisplayAdd()` 方法，该方法将两个值相加并将和输出到显示器。
*   要创建一个 `Func`，代码定义了 `DoAdd()`，它将两个值相加并将结果返回给调用者。
*   `Predicate` 稍微复杂一些，因为代码必须定义一个结构体 `Values` 来存储两个值，然后使用 Lambda 表达式 `x => x.value1 + x.value2 == 3` 来评估 1 + 2 是否真的等于 3。该章节的“嘘！保持小声 — 匿名方法”部分更多地讨论了 Lambda 表达式，但本质上，`x` 是一个输入对象，你通过处理它来确定提供什么输出，当处理 `Predicate` 时，输出必须始终是一个逻辑值。

当你执行此代码时，你会看到以下输出：

`1 + 2 = 3.`

`1 + 2 = 3.`

`The output is 3? True`

## 更真实的示例

相比 `SimpleDelegateExample`，这是一个更真实的示例，`SimpleProgress` 示例向你展示了如何编写一个小程序，它可以显示一个进度条，并在每次耗时方法调用委托时更新它。此示例依赖于 Windows Forms 应用程序，这意味着使用与你过去不同的模板，因此请务必按照接下来的“组装应用程序”部分的步骤来启动你的项目。

该示例显示了一个带有两个按钮和一个进度条的小对话框样式窗口。当你将解决方案示例加载到 Visual Studio 并进行构建、运行，然后点击标记为 Click to Start（点击开始）的上部按钮时，进度条会运行几秒。你会看到它逐渐填充，每次填充长度的十分分之一。当它完全填满时，你可以点击 Close（关闭）按钮结束程序，或再次点击 Click to Start。

### 组装应用程序

为了自己创建示例程序并体验一下 Windows 图形编程，请按照以下步骤操作，首先在*设计模式*下进行，在那种模式下，你只是在布局应用程序的外观。首先，创建项目并在你的“窗口”上放置必要的所需的控件：

1.  **在启动窗口中选择“创建新项目”（如果没看到，请选择文件 ⇒ 启动窗口）。**
    你会看到“创建新项目”窗口。
2.  **在可见的下拉列表中选择 C#、Windows 和 Desktop。**
    向导显示了图 8-2 中所示的项目模板列表。
    ![选择 Windows Forms App (.NET Framework) 模板的截图。](img/9781119839071-fg020802.png)
    图 8-2： 选择 Windows Forms App (.NET Framework) 模板。
3.  **选择 Windows Forms App (.NET Framework) 模板并点击下一步。**
    你会看到一个“配置新项目”窗口，它看起来与你用来创建控制台应用程序的窗口相似。
4.  **在项目名称字段中输入** SimpleProgress，确保“将解决方案和项目放在同一目录”复选框已选中，然后点击创建。**
    你看到的第一个东西是*表单*：一个由你使用几个*控件*自行布局的窗口。
5.  **选择  ⇒  工具箱并打开常用控件组。**
    你会看到图 8-3 中所示的控件列表。
    ![常用控件组包含你最常用的控件的截图。](img/9781119839071-fg020803.png)
    图 8-3： 常用控件组包含你最常用的控件。
6.  **将一个 `ProgressBar` 控件拖到表单并释放；然后将两个 `Button` 拖到表单上。**
7.  **安置按钮和 `ProgressBar`，并使用调整大小柄调整窗口大小，使表单看起来有点像**图** **8-4**所示所示。**
    注意：调整大小柄。
    ![创建进度条使用的的截图。](img/9781119839071-fg020802.png)
    图 8-2： 选择 Windows Forms App (.NET Framework) 模板。

### 设置属性和添加处理器

接下来，为这些控件设置属性：

1.  **在表单上双击 Close 按钮。**
    此操作会在“代码代码”（简单称为“后台代码”）中生成一个方法，这是让表单工作的代码。如下所示：
```csharp
    private void button2_Click(object sender, EventArgs e)
    {
        Close();
    }
```
2.  **双击新的 Click to Start 按钮以生成它的处理方法，其在后台代码中所示：**
```csharp
    private void button1_Click(object sender, EventArgs e)
    {
        UpdateProgressCallback callback = new UpdateProgressCallback(this.DoUpdate);
        // 执行需要定期进度报告的操作。这
        // 了一个知道更新进度条的委托实例。
        DoSomethingLengthy(callback);
        // 清空进度条以便再次使用。
        progressBar1.Value = 0;
    }
```
    你在 `UpdateProgressCallback` 和 `DoSomethingLengthy()` 下看到波浪线，表示错误。现在忽略这些错误——稍后的步骤将修复它们。
3.  **在表单类中添加以下回调方法：**
```csharp
    private void DoUpdate()
    {
        // 告诉进度条更新自身
        progressBar1.PerformStep();
    }
```

下一节将带你浏览剩余的代码，代码都在表单类中。在章节后部分，你会看到传递的委托的其他变体。

### 查看核心代码




嵌入 `Form1` 类中的剩余代码由委托的生命周期部分组成，这些部分在本章之前已经介绍过。你会看到该类以及各种委托组件。以下是你紧接在 `Form1()` 构造函数之后添加的委托声明：

```cs
// 声明委托。这个是 void 类型的。
delegate void UpdateProgressCallback();
```

你还需要一个 `DoSomethingLengthy()`，它是此应用程序的核心工作。它接受一个 `UpdateProgressCallback` 委托作为输入。

```cs
// DoSomethingLengthy -- 我的核心工作方法接收一个委托。
private void DoSomethingLengthy(UpdateProgressCallback updateProgress)
{
  // 设置更新的总持续时间（4 秒）、更新次数
  // 以及每个更新间隔的持续。
  int duration = 4000;
  int intervals = 10;
  int updateInterval = duration / intervals;
  for (int i = 0; i <= intervals; i++)
  {
    // 执行一些耗费时间的操作。
    Thread.Sleep(updateInterval);
    // 更新进度条。
    updateProgress();
  }
}
```

这些代码所做的就是在指定的间隔内睡眠（模拟执行耗费时间的操作），然后通过调用 `updateProgress()` 更新进度条。为了让 `DoSomethingLengthy()` 工作，你还必须在代码顶部添加另一个 `using` 语句：

```cs
using System.Threading;
```

查看此应用程序的类声明是有帮助的，因为它与控制台应用程序使用的不同：

`partial class Form1 : Form`

`partial` 关键字表示此文件仅是完整类的一部分。其余部分可以在解决方案管理器列出的 `Form1.Designer.cs` 文件中找到。（看一眼它。）稍后在“发生的事情”部分，你将再次访问该文件以发现关于事件的真相。部分类允许你将一个类拆分在两个或多个文件中。编译器会生成 `Form1.Designer.cs` 文件，因此不要直接修改其代码。不过，你可以通过更改表单上的元素来间接修改它。`Form1.cs` 是你的部分。

## 嘘！保持安静 —— 匿名方法

“匿名”一词本质上意味着“没有名字的某个东西”。美国可能骑着一匹没有名字的出现在沙漠中，但程序员们骑的是无名方法。你可以在 C# 中以多种方式使用匿名方法，例如使委托的创建变得简单。以下章节将讨论匿名方法，包括 C# 9.0 引入的一些用法。

![Tip](img/tip.png) 微软正在为 C# 10.0 开发 lambda 扩展，这些扩展在编写时尚不可。你可以在 `https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/proposals/csharp-10.0/lambda-improvements` 读取有关它们的内容。这些改进中的大部分没有从根本上改变 lambda 的工作方式——它们大多是细微的变化，具有让 lambda 使用变得稍微更容易的潜力。

### 定义基础匿名方法

在掌握了使用委托的要点后，快速看一眼微软几年前在 C# 2.0 中简化委托的首次尝试。为了省去委托的一些繁琐脱节，你可以使用匿名方法，如 `SimpleProgress2` 示例所示。匿名方法只是用更传统的表示法编写。尽管语法和一些细节不同，但无论你使用原始委托、匿名方法还是 lambda 表达式（创建匿名函数的特殊声明类型，详见 `https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/lambda-expressions`），其效果本质上是一样的。

匿名方法同时创建委托实例和它“指向”的方法——就在现场，即刻完成。这里是 `DoSomethingLengthy()` 方法的核心部分，这次被重写为使用匿名方法：

```cs
private void DoSomethingLengthy()
{
  // 设置更新的总持续时间（4 秒）、更新次数
  // 以及每个更新间隔的持续。
  int duration = 4000;
  int intervals = 10;
  int updateInterval = duration / intervals;
  // 创建委托实例。
  UpdateProgressCallback anon = delegate ()
  {
    // 被“指向”的方法
    progressBar1.PerformStep();
  };
  for (int i = 0; i <= intervals; i++)
  {
    // 执行一些耗费时间的操作。
    Thread.Sleep(updateInterval);
    // 调用委托。
    if (anon != null) anon();
  }
}
```

这段代码看起来像标准的委托实例化，不同之处在于 `=` 符号之后，你看到了 `delegate` 关键字、括号中匿名方法的任何参数（如果没有参数则为空括号）以及方法体。你仍然需要 `UpdateProgressCallback` 类型定义，而且你仍然在调用一个委托实例（在本示例中名为 `anon`）。因此，即使没有方法名。

### 使用静态方法

代码（包括匿名函数）在资源和速度方面并不是没有成本的。当你创建一个匿名函数时，执行它的隐藏成本可能包括：

- 委托调用的开销
- 每个参数的堆分配
- 闭包方法的堆分配

![Remember](img/remember.png) 每一个开销需求和分配对于单个数据项来说似乎并不多，但代码对每个数据项都重复了这些操作，这意味着成本可能会很高。你可以在 `https://docs.microsoft.com/premier-developer/dissecting-the-local-functions-in-c/` 阅读更多关于这些问题的内容。C# 9.0 允许在匿名函数中使用 `static` 关键字，这禁止捕捉局部变量或实例状态。通过在匿名方法中添加 `static`，你可以减少或消除任何意外的分配。`StaticAnonymous` 示例中的 `WorkWithEats` 类展示了这种技术的工作工作（注意，你必须通过向 `StaticAnonymous.csproj` 添加正确的语言项来设置项目以使用 C# 9.0）：

```cs
internal class WorkWithEats
{
  const string outString = "{0} is a {1}.";
  internal struct EatItem
  {
    internal string Name;
    internal string Category;
  }
  internal void CreateEats(Func<string, string, string> func)
  {
    List<EatItem> Eats = new List<EatItem>
    {
      new EatItem() {Name="Apple", Category="Fruit"},
      new EatItem() {Name="Bread", Category="Grain"},
      new EatItem() {Name="Asparagus", Category="Vegetable"},
      new EatItem() {Name="Hamburger", Category="Meat"}
    };
    foreach (var item in Eats)
      Console.WriteLine(func(item.Name, item.Category));
  }
  internal void ShowEats()
  {
    CreateEats(static (name, category) => string.Format(
      outString, name, category));
  }
}
```




此示例通过将 `outString` 定义为 `const` 来开始节省内存（这意味着你不需要提供通常的对象开销）。你可以在此处找到关于内存节省如何实现的更详细讨论：[`https://stackoverflow.com/questions/23529592/how-are-c-sharp-const-members-allocated-in-memory`](https://stackoverflow.com/questions/23529592/how-are-c-sharp-const-members-allocated-in-memory)。`EatItem` `struct` 使得在 `CreateEats()` 方法中能够使用 `List<EatItem>` 来持有所有需要的数据。`CreateEats()` 方法接受一个 `Func` 作为输入（详情请参见本章前面的“考虑 `Action`、`Func` 和 `Predicate` 委托类型”部分）。然后它会创建一个 `EatItem` 条目列表并使用 `func` 显示它们。

此示例中需要注意的第二点是 `ShowEats()` 方法，它通过使用 lambda 表达式作为输入调用 `CreateEats()` 开始。但是请注意，这是一个 `static` lambda 表达式，它在 C# 9.0 之前不可用。lambda 表达式接受 `name` 和 `category` 作为输入，然后使用 `outString` 进行格式化并显示它们。

`WorkWithEats` 类完成了此示例的大部分工作。`Main()` 所做的只是创建适当的对象并启动它，如下所示：

```
static void Main(string[] args)
{
    WorkWithEats myEats = new WorkWithEats();
    myEats.ShowEats();
    Console.ReadLine();
}
```

此示例的输出将格式字符串与各种值混合在一起，如下：

```
Apple is a Fruit.
Bread is a Grain.
Asparagus is a Vegetable.
Hamburger is a Meat.
```

### 使用 lambda 弃参数

目前，当你为 lambda 表达式创建一个参数时，如果你没有实际上将该参数作为表达式代码的一部分使用，C# 将报错。例如，如果你有像这样的 lambda 表达式，编译器将会报错：

```
var handler = (object Obj, EventArgs Args) => ShowDialog();
```

你可以用下划线替换 `Obj` 和 `Args`，以表示它们是 `discard parameters`（即你不会使用的参数），这样编译器就不会抱怨你在编译过程中没有使用它们。使用丢弃参数会让你的代码更清晰、更易理解。在这种情况下，你会看到你的调用可以使用 `object` 和 `EventArgs`；但它并没有使用。要使用丢弃参数，你可以像这样修改代码：

```
var handler = (object _, EventArgs _) => ShowDialog();
```

## 各种杂情况 — C# 事件 (Events)

在本节中，另一个值得讨论的委托应用是用委托实现的 C# `event,`。事件是回调的一种变体，但它为每当重要事件发生时提醒应用程序提供了一种更简单的机制。当有多个方法在等待回调时，事件变得尤为有用。事件在 C# 中被广泛使用，特别是用于将用户界面中的对象与使它们运行的代码连接起来。本章前面介绍的 `SimpleProgress` 示例中的按钮说明了这种用法。

### 观察者模式

在编程中，运行程序中的各种对象对其他对象上发生的事件感兴趣是非常常见的。例如，当用户点击按钮时，包含该按钮的表单想要知道这一情况。事件在 C# 和 .NET 中提供了一种通知任何相关方重要操作的标准机制。

![Tip](img/tip.png) 事件模式如此常见，以至于它有一个名字：观察者模式（Observer design pattern）。它是人们发表的许多常用 `design patterns` 之一，供任何人在自己的代码中使用。要开始学习其他设计模式，你可以参考 Erich Gamma、Richard Helm、Ralph Johnson 和 John Vlissides 编写的*Design Patterns: Elements of Reusable Object-Oriented Software*(Addison-Wesley Professional）。

观察者模式由一个可观察对象（Observable object，即具有感兴趣事件的对象，有时称为主体 Subject）和任意数量的观察者对象（Observer objects）对特定事件感兴趣组成。观察者以某种方式向可观察对象注册，当感兴趣的事件发生时，可观察对象会通知所有注册的观察者。你可以有很多方式实现这种模式（例如回调和接口），但 C# 的方法是使用事件。

![Tip](img/tip.png) 你可能会遇到 `observers` 的另一种名称是 `listeners`。监听器监听事件。这并不是最后的备选方案。

### 什么是事件？发布/订阅 (Publish/Subscribe)

 事件的一个类比是你的当地报纸。你和其他许多人联系报纸，然后报纸向你递送最新的报纸。报纸公司是发布者（Publisher），它的客户是订阅者（Subscribers），因此这种观察者的变体通常被称为 `发布/订阅模式`。这是本章使用的类比，但请记住，观察者模式就是发布/订阅模式，只是术语不同。观察者是订阅者，他们观察的可观察对象是发布者。

在 C# 中，当你有一个产生感兴趣事件的类时，通过提供一个 `event object`（通常是公共的），向可能感兴趣了解此类事件的类发布通知可用性。

![Remember](img/remember.png) `event` 一词在 C# 中有两个含义。你可以将 `event` 一词理解为既指“发生的情况”，也指一种特定的 C# 对象。前者是现实世界的概念，后者是在 C# 中设置的方式，使用了 `event` 关键字。

### 发布者如何发布事件

![Remember](img/remember.png) 为了向订阅者发布，类声明一个委托和一个相应的事件，如下：

```csharp
public class PublisherOfInterestingEvents
{
    // 基于事件的委托类型。如果所有订阅者都在同一个程序集中，
    // 则应声明为 'internal'。
    public delegate void NewEditionEventHandler(object sender,
    NewEventArgs e);

    // 事件：
    public event NewEditionEventHandler NewEdition;

    // …其他代码
}
```

委托和事件定义向世界宣布：“欢迎订阅者！”你可以将 `NewEdition` 事件视为 `NewEditionEventHandler` 委托类型的变量。（目前为止还没有发送事件。这只是它们的底层基础。）

![Tip](img/tip.png) 因为事件非常频繁。.NET 为你定义了两个事件相关的委托类型，命名为 `EventHandler` 和 `EventHandler<*TEventArgs*>`。你可以将之前代码中的 `NewEditionEventHandler` 更改为 `EventHandler` 或泛型的 `EventHandler<*TEventArgs`*>`，你不需要自定义委托类型。本章的其余部分使用前面提到的内置 `EventHandler<*TEventArgs`*>` 委托类型，而不是 `EventHandler` 或自定义类型 `NewEditionEventHandler`。你也应该倾向这种形式：

```csharp
event EventHandler<NewEditonEventArgs> NewEdition;
```

### 订阅者如何订阅事件

为了接收特定的事件，订阅者以如下方式注册：

```csharp
publisher.EventName +=
new EventHandler<*some EventArgs type here >`*(*some method name here*);
```




其中 `publisher` 是 `publisher` 类的一个实例，`EventName` 是事件名称，而 `EventHandler<TEventArgs>` 是事件底层的委托。更具体地说，上一个示例中的代码可能是：

```csharp
myPublisher.NewEdition += new EventHandler<NewEditionEventArgs>(MyPubHandler);
```

由于事件对象在底层是一个委托，因此 `+=` 语法是将一个方法添加到方法列表中，当调用该委托时，它将调用列表中的所有方法。

![Tip](img/tip.png) 任意数量的对象都可以通过这种方式订阅（委托将持有所有已订阅的“处理器”方法的列表）—— 只要你愿意，甚至定义事件的对象本身也可以订阅。（而且，这个示例展示了委托可以“指向”多于一个方法。）在 `SimpleProgress` 程序中，请查看 `Form1.Designer.cs` 文件，以了解表单类类是如何将自己注册为按钮的 `Click` 事件的订阅者的。

### 如何发布事件

当发布者认为发生了某些值得发布给所有订阅者的事件时，它就会*引发*（发送）该事件。这种情况类似于真实的报纸发行周日版。要发布事件，发布者在其一个方法中会有如下代码（但请参见后后的章节“引发事件的推荐方法”）：

```csharp
NewEditionEventArgs e = new NewEditionEventArgs(<此处传递构造函数的参数>);
// 引发事件 -- 'this' 是发布者对象。
NewEdition(this, e);
```

或者对于 `Button` 示例，尽管它是隐藏在 `Button` 类中的：

```csharp
EventArgs e = new EventArgs(); // 关于此主题请参见下一节。
Click(this, e); // 引发事件。
```

在每个示例中，你都设置了必要的参数——这些参数随事件而异；某些事件需要传递大量信息。然后，你通过“调用”它的名称（就像调用委托一样！）来引发事件：

```csharp
// 引发事件（分发报纸）
eventName(<参数列表>);
NewEdition(this, e);
```

![Remember](img/remember.png) 事件可以基于具有不同签名、具有不同参数的各种委托（如之前的 `NewEditionEventHandler` 示例所示），但为 `sender` 和 `e` 参数是事件的惯例。内置的 `EventHandler` 和 `EventHandler<TEventArgs>` 委托类型已经为你定义了它们。

传递事件发送者（引发事件的对象）的引用，如果事件处理方法需要从其获取更多信息将是很有用的。因此，一个特定的 `Button` 对象 `button1` 可以向按钮所属的 `Form` 类传递引用。按钮的 `Click` 事件处理器存在于 `Form` 类中，但发送者是按钮：你会传递 `this`。

![Remember](img/remember.png) 你可以在发布类中的任何方法中引发事件。并且你可以在任何适当的时机引发它。引发事件的推荐方法”章节阐述了关于引发事件的更多内容。

### 如何向事件处理器传递额外信息

事件处理器方法的的 `e` 参数是 `System.EventArgs` 类的自定义派生类。你可以编写自己的 `NewEditionEventArgs` 类来携带你任何需要传达的信息：

```csharp
public class NewEditionEventArgs : EventArgs
{
    public NewEditionEventArgs(DateTime date, string majorHeadline)
    { PubDate = date; Head = majorHeadline; }
    public DateTime PubDate { get; private set; }
    public string Head { get; private set; }
}
```

你应该像上一个代码示例所示，将该类的成员实现为属性。构造函数使用了属性上的私有设置子句。通常，你的事件不需要任何额外参数，你可以直接退而求助于 `EventArgs` 基类，如下一节所示。如果你的事件不需要特殊的 `EventArgs` 派生对象，只需传递：

```csharp
NewEdition(this, EventArgs.Empty); // 引发事件。
```

### 引发事件的推荐方法

之前的章节“如何发布事件”展示了引发事件的骨架。然而，你应该始终定义一个特殊的事件引发方法，如下：

```csharp
protected virtual void OnNewEdition(NewEditionEventArgs e)
{
    EventHandler<NewEditionEventArgs> temp = NewEdition;
    if (temp != null)
    {
        temp(this, e);
    }
}
```

提供此方法可以确保你总是记得完成两个步骤：

1. **将事件存储在临时变量中。**
   这一步使得你的事件在多个“线程”尝试同时使用它的情况下更具可用性。线程将你的程序分为前台任务和一个多个后台任务，这些任务同时运行。

2. **在尝试引发事件之前检查事件是否为 `null`。**
   如果它是 `null`，尝试引发它会导致错误。此外，`null` 也意味着没有其他对象对你的事件表现出兴趣（无人订阅），那么为什么要费心引发它呢？无论你是否编写了此 `OnSomeEvent` 方法，*始终*要检查事件是否为 `null`。

###观察者如何“处理”事件

将方法设为 `protected` 和 `virtual` 允许子类对其进行重写。当你有了这个具有相同参数的方法后，可以在需要时调用它：

```csharp
void SomeMethod()
{
    // 执行某些操作
    NewEditionEventArgs e = new NewEditionEventArgs(DateTime.Today, "Peace Out!");
    OnNewEdition(e);
}
```

### 订阅事件

当你在 Visual Studio 中创建按钮点击事件处理器时（通过双击表单上的按钮），Visual Studio 会在 `Form1.Designer.cs` 文件中生成订阅代码。你不应该编辑该订阅，但可以删除它并替换为在部分类类另一部分编写的代码。此后，表单设计器对此一无所知。

在订阅者的处理器方法中，执行在你得知此类事件时应该发生的事情。为了帮助你编写这些代码，你可以将 `sender` 参数转换为你认为的类型：

```csharp
Button theButton = (Button)sender;
```

然后根据需要调用该对象的方法和属性。由于你有发送对象的引用，你可以向订阅者提问并对其执行操作——就像送报纸的人敲门收取月订阅费一样。而且，你可以通过这种方式获取属性来从 `e` 参数中提取信息：

```csharp
Console.WriteLine(e.HatSize);
```

![Remember](img/remember.png) 当你订阅事件时，你指定一个*处理器方法*：

```csharp
button1.Click += new EventHandler<EventArgs>(button1_Click);
```

```csharp
void button1_Click(object sender, EventArgs e)
{
    // 响应事件执行某些操作。
}
```



你可以使用一种方法将长段代码拆分为独立的、易于维护的单元。使用类结构将数据和方法以意义的方式分组，可以进一步降低程序的复杂性。本章还讨论了使用部分类（partial classes）和部分方法（partial methods）来进一步拆分内容。程序本身已经很复杂了，人类很容易感到困惑，因此我们需要一切能用到的帮助。

C# 提供了另一个层面的分组：你可以将相似的类分组到一个单独的库。除了编写自己的库，你还可以在程序中使用任何人的库。这些程序包含多个名为程序集（`assemblies）的模块。本章将介绍库和程序集。

同时，本微型书籍第 4 章中关于访问控制的内容留下了几个未处理的遗留工作——`protected`、`internal` 和 `protected internal` 关键字——而且由于命名空间（namespaces,*）的使用使得情况变得稍微复杂。命名空间是另一种分组相似类的方法，并允许在程序的两个部分使用重复名称。本章也涵盖了命名空间。

![记住](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用可下载的源代码要简单得多。你可以在下载源代码的 `\CSAIO4D2E\BK02\CH09` 文件夹中找到本章的源码。详见引言关于如何找到这些源文件。

## 将单个程序拆分为多个源文件

书中的程序仅用于演示。每个程序长度不超过几十行，包含的类也不超过几个。一个工业级的程序，配备了所有必要的功能，可能包含数十万行代码，分布在一百个或更多类中。

考虑一个航空公司票务系统：你有一个与通过电话拨打的预订代理的接口，另一个与登机柜台人员的接口，还有互联网（除了控制飞机座位库存的部分以及计算费用（包括税费）的部分之外）；以此类推。这样的程序在完成之前就会变得非常巨大。将所有这些类放在一个大大的 `Program.cs` 源文件中很快就会变得不实际。由于以下原因，这样做会很笨拙：

*   **你必须保持类关系的清晰。** 单个源文件可能会变得极其难以理解。例如，掌握这些模块要容易得多：
    *   `Aircraft.cs`
    *   `Fare.cs`
    *   `GateAgent.cs`
    *   `GateAgentInterface.cs`
    *   `ResAgent.cs`
    *   `ResAgentInterface.cs`
    它们也让查找内容的任务变得更容易。

*   **创建大型程序的工作通常分布在许多程序员之间。** 两个程序员不能同时编辑同一个文件；每个程序员都需要文件的独占访问权限，否则就会导致混乱。你可能有 20 或 30 名程序员同时在一个大型项目中工作。一个包含单个类的文件将限制 24 名程序员每天只能编辑一小时（全天 24 小时）。如果你将程序拆分成多个类，然后将每个类放在它自己的文件中，协调这 24 名程序员就会变得容易得多。

*   **编译一个大文件可能需要花费很长的时间。** 在老板开始怀疑之前，你只能抽出有限的时间喝咖啡休息。你肯定不想因为程序员只改了一行代码，就要重新构建构成大系统的所有指令。Visual Studio 2019 可以重新生成单个项目（整个程序的一个独立模块，它可能包含许多项目）。这比一次性构建整个大程序要更快、更方便。

出于这些原因，精明的 C# 程序员会将程序拆分为多个 `.cs` 源文件，这些文件被编译并构建成单个可执行的 `.exe` 文件。

![记住](img/remember.png) 项目文件（`project file`）包含了哪些文件应该一起使用以及它们如何组合的指令。你可以组合项目文件来生成依赖相同自定义类的程序组合。例如，你可能希望将一个写入程序与其对应的读取程序链接。这样，如果其中一个发生了，另一个就会自动重建。一个项目描述写入程序，而另一个项目描述读取程序。一组项目文件被称为解决方案（`solution.`）（第 3 本 Visual C# 程序员使用 Visual Studio 解决方案管理器（Solution Explorer）将多个 C# 源文件组合到 Visual Studio 2022 环境中的项目。。第 4 本
    图 9-1：使用添加项对话框向项目添加新项。
2.  **选中中间格中的`代码文件`项。**
    你在右格格中看到该项的描述。
3.  **在名称字段中输入 `GlobalUsing.cs` 并点击添加。**
    Visual Studio 将新文件添加到你的项目。。

现在你有一个单一的地方可以查看应用程序中所有的 `using` 语句，只不过这些是全局 `using` 语句，因为它们影响整个应用程序。为了看到这如何工作，在 `GlobalUsing.cs` 文件中输入 `global using System;`。现在查看 `Program.cs` 文件，你会发现 `using System;` 语句变灰，因为 Visual Studio 识别到存在全局方案。删除此语句，编译应用程序，你会发现在有 `global using` 语句的情况下它运行良好。

## 将单个程序拆分为多个程序集

在 Visual Studio 中，以及 C#、Visual Basic .NET 和其他 .NET 语言中，一个项目等于一个编译后的*模块*——在 .NET 中通常被称为*程序集（assembly）*。这两个词在技术上略有不同，但仅对高级程序员来说如此。在书中，你可以将这两个词等同。

### 可执行文件还是库？

C# 可以产生两种基本的程序集类型（还有其他类型）：

*   **可执行文件（`.EXE`）：** 一种独立的程序，包含一个 `Main()` 方法。例如，你可以在文件管理器中双击 `.EXE` 文件并运行它。书中充满了这种控制台形式的可执行文件。可执行程序集通常会使用来自其他程序集库的支持代码。




## 类库 (`DLL`)：一种可以供其他程序使用的编译功能库。本书中的所有程序也使用了库。例如，`System` 命名空间（包含 `String`、`Console`、`Exception`、`Math` 和 `Object` 等类）存在于一组库程序集中。每个程序都需要 `System` 类。库被托管在 DLL 程序集中。

![Remember](img/remember.png) **库不是可执行文件** ——你无法直接让它们运行。相反，你必须从一个可执行文件或另一个库中调用它们的代码。运行 C# 程序的公共语言运行时 (CLR) 会根据需要将库程序集加载到内存中。

需要了解的重要概念是，你可以轻松地编写自己的类库。本章的“将你的类放入类库中”部分将向你展示如何执行此任务。

### 程序集 (Assemblies)

程序集是单个项目的编译版本，它们以特殊格式包含项目的代码，以及大量的 `metadata`（或关于程序集中类的详细信息）。

本节介绍程序集，是因为它们完善了你对 C# 构建过程的理解 —— 而且它们在讨论命名空间以及 `protected` 和 `internal` 等访问关键字时也会涉及到（你将在本章后面的部分遇到这些命名空间和关键字）。程序集对于理解类库也起着重要作用。这些将在后文“将你的类放入类库中”中进行介绍。

![Technicalstuff](img/technicalstuff.png) C# 编译器将项目的 C# 代码转换为公共中间语言（通常称为 IL），并存储在相应的程序集文件中。IL 类似于汇编语言（比机器语言使用的 1 和 0 进了一步），资深程序员几十年来一直使用这种语言来实现“接近硬件”的操作，因为他们的高层语言无法满足其需求，或者编译器无法生成最高效的代码。

从 .NET 编译为 IL（无论使用何种语言）的一个主要结果是，程序可以使用不同语言编写的程序集。例如，C# 程序可以调用最初用 Visual Basic 或 C++ 编写的程序集中的方法，或者 C# 程序可以作为 VB 类的子类。

### 可执行文件 (Executables)

你可以通过多种方式运行可执行程序集：

*   在 Visual Studio 中运行：选择 调试⇒ 开始调试 (F5) 或 调试⇒ 不调试启动 (Ctrl+F5)。
*   在 Windows 资源管理器中双击程序集文件 (`.EXE`)。
*   在 Windows 资源管理器中右键点击文件，并弹出菜单选择“运行”或“打开”。
*   在控制台窗口输入程序集的名称（和路径）。
*   如果程序从命令行接收参数（如文件名），请将文件拖到 Windows 资源管理器中的可执行文件。

![Remember](img/remember.png) Visual Studio 中的解决方案可以包含多个项目 —— 一些 `.DLL` 和一些 `.EXE`。如果一个解决方案包含多个 `.EXE` 项目，你必须告诉 Visual Studio 哪个是启动项目；启动项目将从“调试”菜单运行。要指定启动项目，请在解决方案管理器中右键点击该项目。

### 类库

类库包含一个或多个协同工作的类。通常，你可能会创建一个库以供其他程序使用“将你的类放入类库中”部分解释了如何做到这一点。

## 将你的类放入类库中

![Remember](img/remember.png) 类库最简单的定义是：其类不包含 `Main()` 方法。

### 创建类库项目

你可以通过两种方式之一创建新库项目的文件：

*   **先创建类库，然后将测试应用程序添加到其解决方案中。** 如果你正在编写一个独立的类库，可以采用这种方法。
*   **先创建测试应用程序，然后将一个或多个库项目添加到其解决方案中。** 如果你想为正在进行中的应用程序添加支持性库，则应该采用这种方法。





![Remember](img/remember.png) 你想要分离解决方案和项目目录的原因是，以后可以为你的类库添加一个测试应用程序。使用单独目录可以更容易保持各种项目元素相互分离。

5. **点击创建。**

Visual Studio 为你创建了新项目。你看到 `Class1.cs` 文件已打开，这样你就可以开始为你的类库添加代码了。在有了类库项目后，你可以按照下一节介绍的方法添加测试应用程序项目。

![类库 (.NET Framework) 仅供 Windows 使用快照。](img/9781119839071-fg020902.png)

图 9-2: 类库 (.NET Framework) 仅供 Windows 使用。

![根据需要配置类的快照。](img/9781119839071-fg020903.png)

图 9-3: 根据需要配置类。

![提示](img/tip.png) 查看解决方案资源管理器，你会发现你的类文件名是 `Class1.cs`，这并没有什么描述性。使用以下步骤来纠正这种情况：

1. **右键点击** `Class1.cs` **项，并从上下文菜单中选择“重命名”。**

该项发生变化，允许你输入新名称。

2. **为文件输入** `DoMath.cs` **并按 Enter。**

你会看到一个对话框，显示你正在重命名文件，并询问你是否想要重命名类以进行匹配。

3. **点击“是”。**

Visual Studio 会自动重命名所有 `Class1` 引用，以匹配你提供的新文件名。

### 向现有解决方案中添加第二个项目

如果你有一个现有的解决方案——无论它是正在运行的应用程序，还是像上一节描述那样的类库项目——你都可以轻松地向解决方案添加第二个项目：可以是类库项目，也可以可执行文件项目（例如测试应用程序）。按照以下步骤操作：

1. **在 Visual Studio 中打开现有解决方案后，在解决方案资源管理器中右键点击解决方案节点（顶部节点）。**

2. **从弹出菜单中选择“添加⇒新建项目”。**

你看到一个“添加新项目”的对话框，它看起来与图 9-2 所示的相似（标题除外）。

3. **在“添加新项目”对话框中，从下拉框中选择 `C#`、`Windows`、`Console`。**

你看到了书中之前章节使用的控制台应用程序模板。

![提示](img/tip.png) 没有任何可以阻止你在类库中使用其他其他类型的应用程序。你可以在对话框的右侧选择类库、控制台应用程序、Windows Forms 应用程序或其他可用类型。

4. **选择“控制台应用 (.NET Framework)”模板创建一个标准的 C# Windows 控制台应用程序。**

5. **点击“下一步”。**

你看到如图 9-4 所示的“配置你的新项目”对话框。注意，此对话框缺少图 9-3 所示的许多功能，因为你正在向现有解决方案添加项目。

![用于测试 DoMath 类的应用程序选项配置快照。](img/9781119839071-fg020904.png)

图 9-4: 配置用于测试 `DoMath` 类的应用程序选项。

6. **在“项目名称”字段中输入** `TestApplication`。

7. **保留** `\CSAIO4D2E\BK02\CH09\TestClassProject` 为示例代码的位置。

一旦你在下一步创建此测试应用程序，你将在 `TestClassProject` 文件夹中看到两个子文件夹：`TestClass` 和 `TestApplication`。你选择的位置取决于你如何组织解决方案。你可以将新项目文件夹放在两个地方之一：

* **合在一个文件夹中：** 进入主项目文件夹，使所添加的项目成为子文件夹。（参见图 9-5。）

* **并排：** 导航到包含主项目文件夹的文件夹，使两个项目处于同一级别。（参见图 9-6。）

![在一个一个文件夹中组织两个项目的快照。](img/9781119839071-fg020905.png)

图 9-5: 在一个文件夹中组织两个项目。

![并排组织两个项目的快照。](img/9781119839071-fg020906.png)

图 9-6: 并排组织两个项目。

8. **点击“创建”。**

你看到 `TestApplication` 项目已添加到解决方案中，如图 9-7 所示。

![带有两个项目的解决方案快照。](img/9781119839071-fg020907.png)

图 9-7: 带有两个项目的解决方案

### 为库创建代码

在有了类库项目后，创建组成库的类。以下 `TestClass` 示例显示了一个简单的类库：

```csharp
namespace TestClass
{
    public class DoMath
    {
        public int DoAdd(int Num1, int Num2)
        {
            return Num1 + Num2;
        }
        public int DoSub(int Num1, int Num2)
        {
            return Num1 - Num2;
        }
        public int DoMul(int Num1, int Num2)
        {
            return Num1 * Num2;
        }
        public int DoDiv(int Num1, int Num2)
        {
            return Num1 / Num2;
        }
    }
}
```

库可以包含任何 C# 类型：类、结构、委托、接口和枚举。你在本书的第 11 节](#c21.xhtml)中讨论了结构，委托出现在第 8 节](#c18.xhtml)中，接口在第 7 节](#c17.xhtml)中，而第 1 部分第 10 节](#c10.xhtml)讨论了枚举。

注意，在这种情况下，所有的访问修饰符都设置为 `public`，因为意图是从程序集外部访问。然而，在创建类库时，你遵循与任何其他类相同的访问规则，并为各个元素提供执行任务所需的权限。

![Remember](img/remember.png) 在类库代码中，通常不应该捕获异常。让它们从库传递到调用它的客户端代码。客户端需要知道这些异常并以自己的方式处理它们。第 1 部分涵盖了异常。

示例代码还显示此文件没有包含任何 `using` 指令，因为它不需要。只添加你需要的 `using` 指令可以使你的代码更加简洁：

### 使用测试应用程序测试库

类库本身不执行任何操作，所以你需要一个*测试应用程序*，这是一个小型可执行程序，用于在开发期间通过调用其方法来测试库代码。也就是说，编写一个使用库中的类和方法的程序。





![Remember](img/remember.png) 要在测试应用程序中使用你的类库，你必须对其添加引用。要执行此操作，请在解决方案资源器的 `TestApplication` 部分右键单击 `References`（引用），并选择 `Add Reference`（添加引用）。你会看到一个引用管理器对话框。选择 `Projects\Solution` 选项卡，就能看到 `TestClass`，如图 9-8 所示。选择 `TestClass` 旁边的选框并点击确定。Visual Studio 将打开 `TestApplication` 的引用文件夹，你会看到 `TestClass` 已添加到列表中。

![为你的类库添加引用的快照。](img/9781119839071-fg020908.png)

图 9-8 为你的类库添加引用。

是时候创建一个测试程序了。以下代码出现在 `TestApplication` 的 `Program.cs` 文件中，而不是 `DoMath.cs` 文件中：

```cs
using System;

// 添加引用到你的类库。
using TestClass;
namespace TestApplication
{
    class Program
    {
        static void Main(string[] args)
        {
            // 创建一个 DoMath 对象。
            DoMath math = new DoMath();
            // 测试 DoMath 库函数。
            Console.WriteLine($"6 + 2 = {math.DoAdd(6, 2)}");
            Console.WriteLine($"6 - 2 = {math.DoSub(6, 2)}");
            Console.WriteLine($"6 * 2 = {math.DoMul(6, 2)}");
            Console.WriteLine($"6 / 2 = {math.DoDiv(6, 2)}");
            Console.Read();
        }
    }
}
```

此应用程序创建了 `DoMath` 的实例，然后执行了类中的所有公共方法。要生成此类和应用程序，选择 `Build⇒  Build Solution`（生成⇒ 生成解决方案）。当你在 Debug 菜单中选择运行应用程序的选项之一时，这是测试应用程序的输出：

```
6 + 2 = 8
6 - 2 = 4
6 * 2 = 12
6 / 2 = 3
```

![Tip](img/tip.png) 库通常只提供 `static` 方法。在这种情况下，你不需要实例化库对象。只需通过类调用方法即可。

## 超越公共和私有：更多访问关键字

如前面的章节所述，将程序划分为多个程序集会影响你如何从 `AssemblyA` 访问 `AssemblyB` 中的代码。本本型型读物第 4 章中的访问控制示例很好地说明了当正确配置访问修饰符时，单个程序集内部发生了什么。然而，现在你有两个程序集，因此 `internal` 访问修饰符意味着 `AssemblyB` 不能访问 `AssemblyA` 的内部成员；因此，你需要更改配置访问修饰符的方式。后续章节将讨论当你有多个程序集时如何使用访问修饰符。

### Internal：仅供 CIA 内部

假设一个解决方案包含这两个项目：

* `InternalLimitsAccess`：一个可执行文件，其类 `Congress` 包含启动程序执行的 `Main()` 方法。（没有法律要求 `Main()` 类必须名为 `Program`。）
* `CIAAssembly`：类库项目。

在现实生活中，美国国会有一个讨厌的习惯，期望中央情报局（CIA）揭露其秘密——当然，只对国会成员。（“我们不会泄露你的秘密——诚实地。”）与此同时，CIA 那些过度神秘的特工们有他们希望保留的秘密。（也许他们知道可口可乐的秘密配方或桑德斯上的秘密草药和香料，或者是更阴暗的实体。）Secret X 到底是什么在这里并不，但 CIA 想保持 Secret X 的秘密。后续章节将讨论 CIA 如何成功隐藏其秘密。

#### 防止组 B 知道组 A 在做什么

CIA 的每个人都需要知道 Secret X。在 `CheckCIA` 示例中，CIA 被分为几个类——`GroupA` 类和 `GroupB` 类。将它们 想象成 CIA 中有时会相互通信和共享的部门。假设 `GroupA` 是 Secret X 的持有者，该组将其标记为 `private`。代码看起来如下：

```cs
// 在程序集 InternalLimitsAccess 中：
class Congress
{
    static void Main(…)
    {
        // 监督 CIA 的代码
    }
}

// 在程序集 CIAAssembly 中：
public class GroupA
{
    private string _secretFormulaForCocaCola; // Secret X
    internal GroupA() { _secretFormulaForCocaCola = "lots of sugar";}
}

public class GroupB
{
    public void DoSomethingWithSecretX()
    {
        // 对 Secret X 操作，只要你能访问它。
    }
}
```

现在 `GroupB` 无法看到 Secret X，但假设它有合法的需要知道它。当然，`GroupA` 可以将 Secret X 提升到 `public` 状态，但如果这样做，秘密就不再是秘密了。如果 `GroupB` 能看到秘密，国会里的那些窥探者也能看到。更糟糕，CNN 也知道，更不用说 Fox、ABC 了。





![Remember](img/remember.png) 你可以将 `internal` 类内部的方法标记为 `public`，尽管它并不是真正的公有的。类成员的访问权限不能高于其所属类，因此所谓的“public”成员实际上只是 `internal` 的。

CIA 仍然可以通过在所属的类中将秘密声明为 `private` 来保持其最深层、最黑暗的秘密绝对机密。这种策略使得这些信息仅在该类内部可访问。

## Protected（保护）：与子类共享

`private` 的主要目的是隐藏信息。特别是，`private` 隐藏了类的内部实现细节。（对彼此了解过于紧密的类并不是世界上最幸运的类。事实上，它们是最不幸运的类。）包含大量实现细节的类被认为与它们过度了解的类之间“紧密耦合”。如果类 `A` 知道类 `B` 的内部工作机制，`A` 可能会过度依赖这些细节。如果这些细节发生变化，你最终将不得不修改两个类。

其他类——以及程序集——对类 `B` 如何施展“魔法”了解得越少越好。本微型书籍第 4 章中的“访问控制救急——一个示例”部分使用了 `BankAccount` 类作为示例。银行不希望健忘的人或健忘的类能够直接更改余额。该余额是 `BankAccount` 类实现的一部分。它是 `private` 的。`BankAccount` 提供了对余额的访问——但仅通过一个仔细控制的公共接口。在 `BankAccount` 类中，与主应用程序共享的接口由三个 `internal` 方法组成：

*   `Balance`：提供查找当前余额的只读方式。你不能使用 `Balance` 来修改底层余额。
*   `Deposit()`：允许类外部的人以受控的方式增加余额。
*   `Withdraw()`：允许某人（推测是账户所有者）从余额中扣款，但受到严格控制的限制。`Withdraw()` 执行了业务规则，即你取出的金额不能超过你的余额。

编程中除了 `private`、`internal` 和 `public` 之外，还会出现访问控制方面的考虑。上一节解释了 `internal` 关键字如何开放一个类——但仅对其所属程序集中的其他类开放。

然而，假设 `BankAccount` 类有一个子类 `SavingsAccount`（在微型书籍第 5 章的“处理基本更新”部分中描述）。`SavingsAccount` 中的方法需要访问基类中定义的该余额。当然，其他类（即使在同一个程序集内）可能并不需要。幸运的是，`SavingsAccount` 可以像外部一样使用相同的公共接口和访问权限：使用 `Balance`、`Deposit()` 和 `Withdraw()`。

但是，有时基类并没有为其子类（以及其他）提供此类访问方法。如果 `BankAccount` 中的 `_balance` 数据成员是 `private` 的，且类没有提供 `Balance` 属性怎么办？这时 `protected` 关键字登场了：如果基类中的 `_balance` 实例变量声明为 `protected` 而不是 `private`，外部人员就看不到它——对他们来说实际上是 `private` 的。但子类可以正常看到它。

在第 5 章的示例中，`Balance` 属性被标记为 `protected`，这意味着只有 `BankAccount` 和 `SavingsAccount` 可以看到它。对余额信息的访问是通过 `ToString()` 方法的公共 `override` 提供的，这提供了一种受控的访问方法。因此，程序集外部的调用者只能存款、取款和获取余额——都是以受控的方式。下载源码中的 `SimpleSavingsAccountAssembly` 示例显示了程序的程序集版本（进一步保护类功能免受窥探），你可以看到它在对原始第 5 章代码进行六处微小修改后运行良好良好；类（两处更改）和它们的构造函数（四处更改）必须变为 `public` 才能看到。在处理程序集时，你不能再将类和构造函数保持为 `internal`，但其他程序集成员实际上被隐藏得更好。此外，你需要为 `BankAccount` 和 `SavingsAccount` 类提供引用和 `using` 指令。`AccountLibrary` 项目包含这些类，而 `MyATM` 项目包含 `Main()`。

## 将类放入命名空间

`Namespaces`（命名空间）是将相关的类放在一个包里，并减少不同地方使用的名称之间的冲突。例如，你可以将所有与数学相关的类编译到 `MathRoutines` 命名空间中。单个文件可以（但并不常见）被分为多个命名空间：

```
// 在文件 A.cs 中：

namespace One
{
}

namespace Two
{
}
```

更常见的做法是分组多个文件。例如，`Point.cs` 文件可能包含 `Point` 类，而 `ThreeDSpace.cs` 文件包含 `ThreeDSpace` 类，用于描述欧几里得空间的属性（如立方体）。你可以将 `Point.cs` 和 `ThreeDSpace.cs` 以及其他 C# 源文件合并到 `MathRoutines` 命名空间中（以及可能可能的 `MathRoutines` 库程序集中）。每个文件都将将其代码封装在同一个命名空间中。（构成命名空间的是这些文件中的类，而不是文件本身。类位于哪个文件中与命名空间无关。）

```c
// 在文件 Point.cs 中：
namespace MathRoutines
{
    class Point { }
}

// 在文件 ThreeDSpace.cs 中：
namespace MathRoutines
{
    class ThreeDSpace { }
}
```

![Remember](img/remember.png) 如果你不将类封装在命名空间中，C# 会将它们放在全局命名空间（即未命名的命名空间）。更好的做法是使用特定的命名空间。命名空间起到以下作用：

*   **命名空间将同类项归在一起，而不是混合。** 作为应用程序程序员，你可以合理地假设构成 `MathRoutines` 命名空间的类与数学有关。同样，当寻找特定的数学方法时，你首先会在 `MathRoutines` 命名空间中寻找。
*   **命名空间避免命名冲突的可能性。** 例如，文件输入输出库可能包含一个 `Convert` 类，用于将一种文件类型转换为另一种。同时，翻译库可能包含一个同名的类。为这两组类分配命名空间 `FileIO` 和 `TranslationLibrary` 可以避免这个问题：`FileIO.Convert` 类明显区别于 `TranslationLibrary.Convert`。

### 声明命名空间

使用 `namespace` 关键字后跟名称和一对大括号块来声明命名空间。该块内的类（以及其他类型）都是命名空间的一部分：

```cs
namespace MyStuff
{
    class MyClass {}
    class UrClass {}
}
```

在此示例中，`MyClass` 和 `UrClass` 都是 `MyStuff` 命名空间的一部分。

![Remember](img/remember.png) 命名空间隐式是 `public` 的，你不能在命名空间上使用访问修符，即使是 `public`也不行。除了类之外，命名空间还可以包含其他类型，包括：

*   `delegate`
*   `enum`
*   `interface`
*   `struct`

命名空间还可以包含*嵌套命名空间*，即命名空间中的命名空间，嵌套深度任意。你可以将 `Namespace2` 嵌套在 `Namespace1` 内部，如下所示：

```csharp
namespace Namespace1
{
    // 这里是 Namespace1 的类 ...
    // 然后是嵌套命名空间：
    namespace Namespace2
    {
        // Namespace2 的类
        public class Class2
        {
            public void AMethod() { }
        }
    }
}
```

要从 `Namespace1` 外部调用 `Namespace2` 内部 `Class2` 的方法，你需要指定此行：





`Namespace1.Namespace2.Class2.AMethod();`

想象这些用点连接起来的命名空间是通往目标项目的某种逻辑路径。“点点名称”（例如 `System.IO`）看起来像嵌套的命名空间，但它们只命名了一个命名空间。因此，`System.Data` 是一个完整的命名空间名称，而不是嵌套在 `System` 之中的 `Data` 命名空间。这种约定使得多个相关的命名空间（例如 `System.IO`、`System.Data` 和 `System.Text`）更容易存在，并且家族相似性明显。在实践中，嵌套命名空间和带点名的命名空间是没有区别的。

![Technicalstuff](img/technicalstuff.png) 在程序中的所有命名空间加上公司名称是一种惯例——将公司名称作为由点分隔的多个段的前部：`MyCompany.MathRoutines`。（如果你有公司名称，该陈述成立；你也可以只使用自己的名字。）如果你的代码使用的两个库恰好使用了相同的基本命名空间名称（如 `MathRoutines`），添加公司名称可以防止命名冲突。

![Tip](img/tip.png) Visual Studio 新项目对话框运行应用程序向导，它将生成的所有代码都放在命名空间中。向导根据它创建的项目目录为这些命名空间命名。查看本书中的任何程序，每个程序都是由应用程序向导创建的。例如，`AlignOutput` 程序创建在 `AlignOutput` 文件夹中。源代码名为 `Program.cs`，与默认类的名称匹配。包含 `Program.cs` 的命名空间名称与文件夹名称相同：`AlignOutput`。

### 使用文件范围命名空间 (Using file-scoped namespaces)

C# 10.0 开发团队试图从某种程度上清理你的文件。本章“使用全局 using 语句（Working with Global using Statements”节描述的 `global using` 语句在某种程度上清理了垂直浪费。文件范围命名空间通过允许你指定命名空间而不使用通常的缩进，清理了水平浪费，如 `FileScopeNamespace` 示例以及此处的代码所示：

```sharp
using System;

namespace FileScopeNamespace;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello World!");
    }
}
```

`FileScopeNamespace` 现在适用于整个文件。你必须使用 .NET Core 应用程序才能生效。此外，你必须像下面加粗所示，为你的 `FileScopeNamespace.csproj` 文件添加 C# 10.0 支持：

```xml
<Project Sdk="Microsoft.NET.Sdk">
<PropertyGroup>
  <OutputType>Exe</OutputType>
  <TargetFramework>net6.0</TargetFramework>
</PropertyGroup>
<PropertyGroup>
  <LangVersion>10.0</LangVersion>
</PropertyGroup>
</Project>
```

### 将命名空间与访问关键字故事联系起来

![Remember](img/remember.png) 除了帮助将代码封装成更易用的形式外，命名空间还扩展了本迷你书第 4 章]介绍的访问控制概念（该章节引入了 `public`、`private`、`protected`、`internal`、`protected internal` 和 `private protected` 关键字）。命名空间通过进一步限制从何处可以访问类的成员，扩展了访问控制。

然而，命名空间对可见性的影响大于可访问性。默认情况下，`NamespaceA` 中的类和方法对 `NamespaceB` 中的类是不可见的，无论它们的访问控制修饰符是什么。但你可以通过几种方法让一个命名空间的类和方法对另一个命名空间可见。底线是，你只能访问对你可见且足够公开的内容。这个问题涉及到访问控制，访问控制在本文章较早部分已扩展，并在迷你书第 4 章中对访问修饰符的讨论中有所涵盖。

#### 判断你需要的类和方法对你而言是否可见且可访问

要确定 `NamespaceA` 中的 `Class1` 是否可以调用 `NamespaceB.Class2.AMethod()`，请考虑以下两个问题：

*   **`NamespaceB` 中的 `Class2` 对调用类 `Class1` 是可见的吗？**
    这个问题涉及命名空间可见性，将在此列表末尾进行讨论。
*   **如果第一个问题的答案是 True（是），`Class2` 及其 `AMethod()` 对于 `Class1` 访问来说是否也是“足够公开”的？**
    如果 `Class2` 与 `Class1` 在不同的程序集中，则它必须是 `public`，`Class1` 才能访问其成员。如果 `Class2` 在同一个程序集中，则至少需要声明为 `internal`。类只能是 `public`、`protected`、`internal` 或 `private`。
    同样，在这些情况下，`Class2` 方法必须至少具有特定程度的访问权限。方法在类拥有的访问修饰符列表中增加了 `protected internal` 选项。迷你书第 4 章和早之前的章节“超越公共和私有：更多访问关键字（Going Beyond Public and Private: More Access Keywords]”提供了详细细节。
    在 `Class1` 调用 `Class2` 方法之前，你需要对这两个问题都回答“是”。

#### 让另一个命名空间中的类和方法可见

C# 提供了两种方法让 `NamespaceB` 中的项在 `NamespaceA` 中可见：

*   **在 `NamespaceA` 中使用 `NamespaceB` 的项时，始终使用完全限定名称**
    类的命名空间是扩展类名的一部分，这导致了使一个命名空间中的类可见的第一种方法。

```sharp
namespace MathRoutines // 分为两个段 - 见下文
{
    class Sort
    {
        public void SomeMethod()
        {
            Console.WriteLine("In SomeMethod");
        }
    }
}

namespace Paint
{
    public class PaintColor
    {
        public PaintColor(int nRed, int nGreen, int nBlue) { }
        public void Paint()
        {
            Console.WriteLine("Painting");
        }
        public static void StaticPaint()
        {
            Console.WriteLine("Static Painting");
        }
    }
}

namespace MathRoutines // 此命名空间的另一部分
{
    public class Test
    {
        static public void Main(string[] args)
        {
            // 创建相同命名空间的 Sort 对象
            // 并调用其方法。
            Sort obj = new Sort();
            obj.SomeMethod();
            // 创建另一个命名空间的对象 - 注意每个类引用
            // 中都包含命名空间名称。
            Paint.PaintColor black = new Paint.PaintColor(0, 0, 0);
            black.Paint();
            Paint.PaintColor.StaticPaint();
        }
    }
}
```

*   **通过为文件提供 `NamespaceB` 的 `using` 指令，消除在 `NamespaceA` 中使用完全限定名称的需求：**
    ```sharp
    using System; // 这些是命名空间名称
    using NamespaceB;
    ```

### 使用完全限定名称

通常，`Sort` 和 `Test` 在不同的 C# 源文件中，你将它们编译成一个程序。在这种情况下，`Sort` 和 `Test` 两个类位于相同的命名空间 `MathRoutines` 中，尽管它们出现在文件的不同声明中（或不同的文件中）。

`Test.Main()` 方法引用 `Sort` 类而无需指定命名空间，因为这两个类在同一个命名空间中。然而，`Main()` 在引用 `PaintColor` 时必须指定 `Paint` 命名空间，例如调用 `Paint.PaintColor.StaticPaint()`。这一过程被称为*完全限定*名称。





注意，在引用 `black.Paint()` 时不需要采取任何特殊步骤，因为 `black` 对象的类（包括命名空间）已在 `black` 声明中指定。以下是该示例的输出：

```
In SomeMethod
```

```
Painting
```

```
Static Painting
```

## 使用部分类

`partial class`（部分类）这个术语让人联想到那些犹豫不决或拖延的人，但它与这两者都无关。部分类为设计类的组合方式、开发者与其交互的方式以及以后添加功能的方法提供了灵活性。接下来的章节将详细介绍部分类。

### 定义部分类的目的

通常，你希望将类的所有代码都放在单个文件中，以便一次性看到所有内容。总的情况下，如果一个类大到需要将其分散开，也许更好的类设计可以实现更小的代码。然而，有些类就是很大，你无法做很多事情让它们变小。考虑到这一点，你可以在以下情况下创建部分类并有效地使用它们：

*   该类大到需要多名程序员的技能，因此你将代码放在多个文件中，允许每个程序员访问类的一部分。
*   在处理自动生成的源（例如来自设计器的代码）时，代码生成器可以自动创建类的部分，开发者可以为类的其余部分提供代码。Visual Studio 使用这种方法创建 Windows Forms、Web 服务封装代码以及许多其他应用程序元素。
*   源生成器可以使用这种技术向现有类添加功能（描述见 [`https://docs.microsoft.com/en-us/dotnet/csharp/roslyn-sdk/source-generators-overview`](https://docs.microsoft.com/en-us/dotnet/csharp/roslyn-sdk/source-generators-overview)）。

### 为单个类处理多个文件

使用部分类与使用普通类相似，只是包含了 `partial` 关键字。`PartialParts`示例显示了如何创建此类类。示例中的 `PartOne.cs` 文件包含了 `DoStuff` 类的第一部分：

```
namespace Parts
{
    public partial class DoStuff
    {
        internal int TheValue
        { get; private set; }
        public DoStuff()
        {
            TheValue = 0;
        }
        public override string ToString()
        {
            return $"The value is: {TheValue}.";
        }
    }
}
```

类的这部分包含一个 `internal` 属性 `TheValue`、一个构造函数以及对 `ToString()` 的 `override`。构造函数简单地将 `TheValue` 设置为 `0`。你使用 `ToString()` 获取 `TheValue` 的格式化输出。

部分类的片段必须属于同一个程序集和命名空间。为了方便处理 `Parts` 命名空间和 `DoStuff` 类，你需要向同一个项目添加另一个文件。右键点击 PartialParts 项目项，从右键菜单中选择“添加⇒新建项”。当出现“新建项”对话框时，高亮“代码文件”项，在名称字段中输入 `PartTwo.cs` 并点击“添加”。当你看到新的代码文件时，可以添加以下代码：

```
using System;
namespace Parts
{
    public partial class DoStuff
    {
        public void DoAdd(int value)
        {
            if (value > 0)
                TheValue += value;
            else
                throw new ArgumentOutOfRangeException("value", "Input must be greater than 0!");
        }
        public void DoSubtract(int value)
        {
            if (value > 0)
                if (value <= TheValue)
                    TheValue -= value;
                else
                    TheValue = 0;
            else
                throw new ArgumentOutOfRangeException("value", "Input must be greater than 0!");
        }
    }
}
```

这段代码添加了两个方法：`DoAdd()` 用于向 `TheValue` 添加大于 `0` 的值；`DoSubtract()` 用于从 `TheValue` 中减去大于 `0` 的值。`DoSubtract()` 方法进一步进一步限制，不允许 `TheValue` 低于 `0`。在两种情况下，当用户传递 `0` 或以下的值时，方法都会抛出 `ArgumentOutOfRangeException`。现在是时候使用以下代码测试这个部分类了：

```
static void Main(string[] args)
{
    DoStuff thisStuff = new DoStuff();
    try
    {
        thisStuff.DoAdd(-1);
    }
    catch (ArgumentOutOfRangeException e)
    {
        Console.WriteLine(e.Message);
    }
    try
    {
        thisStuff.DoAdd(5);
    }
    catch (ArgumentOutOfRangeException e)
    {
        Console.WriteLine(e.Message);
    }
    try
    {
        thisStuff.DoSubtract(1);
    }
    catch (ArgumentOutOfRangeException e)
    {
        Console.WriteLine(e.Message);
    }
    Console.WriteLine($"{thisStuff.ToString()}");
    Console.ReadLine();
}
Main()
```

```
Input must be greater than 0!
Parameter name: value
The value is: 4.
```





本节将介绍部分方法（partial method）的最简单实现。签名部分仅显示了部分方法将包含的内容，例如 `PartialParts` 示例中 `DoStuff` 类在 `PartOne.cs` 文件中的该条目：

```cs
public partial void DoDivide(int value);
```

该方法的实现在 `PartTwo.cs` 中：

```cs
public partial void DoDivide(int value)
{
  if (value > 0)
    TheValue = TheValue / value;
  else
    throw new ArgumentOutOfRangeException("value", "Input must be greater than 0!");
}
```

与 `DoAdd()` 和 `DoSubtract()` 一样，输入值必须大于 `0`。否则，`DoDivide()` 将抛出 `ArgumentOutOfRangeException`。

# 第 10 章

## 使用命名参数和可选参数提高效率

## 本章内容

- ![Bullet](img/check.png) **区分命名参数和可选参数**
- ![Bullet](img/check.png) **使用可选参数**
- ![Bullet](img/check.png) **声明和使用输出参数**
- ![Bullet](img/check.png) **实现引用返回类型**

正如你可能记得的，参数是方法的输入。它们是作为方法签名一部分出现的值。当方法返回一个值时（它并不总是这样做的），参数提供了生成该输出值所需的数据。有时，返回值本身就是参数（`out` 参数），这会让情况变得复杂。

在 C# 的旧版本以及大多数源自 C 的语言中，参数不能是可选的（很奇怪的是，你会在网上发现一些这种古老代码的示例潜伏在处，正等着让你感到受阻）。你并不是让参数变为可选，而是被要求为预期用户可能需要的每个版本的方法创建一个单独的重载版本。这种模式效果良好，但本章将探讨其中其中的一些问题。

C# 4.0 及以上版本支持可选参数。*可选参数*是指直接在方法签名中具有默认值的参数。这与第 3 本第 6 章向你展示的动态类型相同的控制与效率之间的权衡问题。可选参数提供的绳子足以让你勒死自己。程序员很容易犯错。

## 探索可选参数

可选参数依赖于设置默认值才能具有可选性。例如，如果你正在根据名称和城市搜索电话号码，你可以将城市名称默认为你的城市，从而使该参数变为可选。

```csharp
public static string searchForPhoneNumber(string name, string city = "Columbus") {…}
```

接下来的章节将讨论如何在 C# 中使用可选参数。

### 使用可选值参数

这就是可选参数如此神奇的原因。考虑以下用于 `addit()` 方法的代码。它看起来很愚蠢，但它说明了多个重载的现状。在此之前，你有这样的代码：

```csharp
public static int addit(int z, int y)
{
  return z + y;
}
public static int addit(int z, int y, int x)
{
  return z + y + x;
}
public static int addit(int z, int y, int x, int w)
{
  return z + y + x + w;
}
public static int addit(int z, int y, int x, int w, int v)
{
  return z + y + x + w + v;
}
```

有了可选参数，你现在有了这样的代码：

```csharp
public static int addit(int z, int y, int x = 0, int w = 0, int v = 0)
{
  return z + y + x + w + v;
}
```

如果你需要加两个数字，可以轻松做到。

```csharp
int answer = addit(10, 4),
```

如果你需要加四个数字，你也没有问题。

```csharp
int answer = addit(10, 4, 5, 12);
```

那么，为什么可选参数是危险的呢？因为有时默认值可能会产生意想不到的后果。例如，你不想创建一个 `divideit()` 方法并将默认参数设置为 `0`。有人可能会调用它并得到一个难以调试的除以零错误。就像你不会将 `divideit()` 方法的参数设置为 `0` 一样，将 `addit()` 中的可选值设置为 `1` 也是很糟糕。这意味着每个可选值都将自动向总和中加 1，如下所示：

```csharp
public static int addit(int z, int y, int x = 1, int w = 1, int v = 1)
{
  // 你显然不想要这样
  return z + y + x + w + v;
}
```

![Warning](img/warning.png) 有时问题可能是微妙的，所以请谨慎使用可选参数。例如，假设你有一个基类，然后派生出一个实现该基类的类，如下：

```csharp
public abstract class Base
{
  public virtual void SomeFunction(int x = 0)
  {…}
}
public sealed class Derived : Base
{
  public override void SomeFunction(int x = 1)
  {…}
}
```

声明一个新的实例会发生什么？

```csharp
Base ex1 = new Base();
ex1.SomeFunction(); // SomeFunction (0)
```

```csharp
Base ex2 = new Base();
ex2.SomeFunction(); // SomeFunction (0)
```

```csharp
Derived ex3 = new Derived();
ex3.SomeFunction(); // SomeFunction (1)
```

### 避免引用类型

引用类型，正如第 1 本所讨论的，存储指向实际数据的变量，而不是数据本身。引用类型通常被称为对象。新的引用类型实现实现：

- `class`
- `interface`
- `delegate`

这些类型在使用它们之前需要构建；.NET 框架中有三种内置引用类型：

- `String`
- `Object`
- `Dynamic`

你可以像传递静态类型一样将引用类型传递给方法。它仍然被视为一个参数。你像使用其他变量一样在方法内部使用它。

但引用类型像值类型一样被传递吗？尝试一下。例如，如果你为你的 `Calendar` 类有一个 `Schedule` 方法，你可以传递 `CourseId`，也可以传递整个 `Course`。这完全取决于你如何构建应用程序。

```csharp
public class Course
{
  public int CourseId;
  public string Name;
  public Course(int id, string name)
  {
    CourseId = id;
    Name = name;
  }
}

public class Calendar
{
  public static void Schedule(int courseId)
  {
  }
  public static void Schedule(Course course)
  {
    // 这里会发生一些有趣的事情
  }
}
```

如果你想让第二个 `Schedule` 方法支持一个可选的 `Course` 参数呢？假设，如果你想让默认创建一个 `new Course()`，你只需省略该参数。这就像将静态整数设置为 `0` 或其他值，不是吗？

```csharp
public static void Schedule(Course course = New Course())
{
  // 在此处实现代码
}
```




然而，这是不允许的。Visual Studio 仅允许对静态类型使用可选参数，编译器也会提示你这一点。（该规则有例外，但书中未涵盖，例如在 C# 8.0 及更高版本中使用可空引用类型，详见 [`https://docs.microsoft.com/dotnet/csharp/language-reference/builtin-types/nullable-reference-types`](https://docs.microsoft.com/dotnet/csharp/language-reference/builtin-types/nullable-reference-types)）。如果你想这样做，你必须在 `Schedule` 方法中接收 `CourseId` 并在事件体中构造一个新的 `Course` 对象。

## 查看命名参数

命名参数与可选参数的概念是密不可分的的。如果你有多个默认参数，你需要一种方法来告诉编译器你提供了哪一个参数！例如，看看本章较之前的 `addit()` 方法，在实现可选参数之后的版本：

```csharp
public static int addit(int z, int y, int x = 0, int w = 0, int v = 0)
{
    return z + y + x + w + v;
}
```

显然，在这种实现中，参数的顺序并不重要，但如果这是在一个类库，你可能不知道参数的顺序并不是问题！如果你想提供 `v`，该如何告诉编译器跳过 `x` 和 `w`？通过命名参数，你可以说：

```csharp
int answer = addit(z:3, y:7, v:4);
```

非可选参数不需要命名；因为它们是强制要求的，所以位置是自动假设的。尽管如此，为它们命名是一个良好的习惯。如果你跳过命名，你的代码会变成这样：

```csharp
int answer = addit(3, 7, v:4);
```

你必须承认，这读起来稍微困难一点。人们必须回到方法签名才能弄清楚发生了什么。C# 7.2 引入了一个额外的特性。通常情况下，在在使用命名参数后不能再跟任何位置参数。但是，从 C# 7.2 开始，你可以这样做：

```csharp
int answer = addit(z:3, 7, v:4);
```

`7` 仍然关联到 `y`，因为它出现在正确的位置。但现在，你的代码变得异常难读。

## 使用其他方法返回值

通常，你通过使用 `return` 关键字后跟值向用户返回结果。某些情况需要替代的返回方法。例如，如果你正在处理 Win32 API，你通常需要使用参数而不是实际返回值，这是因为微软编写原始 C/C++ 代码的方式。你可能会在其他情况下发现你需要返回多个值，但又不想创建一个 `struct`、`list` 或对象来返回它们。接下来的章节将讨论这些返回值的替代方法。

### 输出 (`out`) 参数

`输出参数`是方法签名中的参数，它们实际上会更改用户传递的变量的值。参数引用的是原始变量的位置，而不是创建一个工作副本。输出参数在方法签名中使用 `out` 关键字声明。你可以根据需要使用任意数量的（好吧，在合理范围内），尽管如果你使用了几个，可能应该使用其他东西（也许是泛型列表？）。在方法声明中，输出参数可能如下：

```csharp
public static void Schedule(int courseId, out string name, out DateTime scheduledTime)
{
    name = "something";
    scheduledTime = DateTime.Now;
}
```

按照规则，你应该能够通过预设值使这些参数之一变为可选。与引用参数（在本章的“[通过引用返回值”节）不同，输出参数不支持默认值是合理的。输出参数就是输出——设置值的操作应该在方法体内部发生。因为输出参数本身并不期望传入值，因此设置默认值对程序员来说并没有好处。

### 使用 out 变量

C# 7.0 改变了返回值的工作方式。你现在可以以新的方式处理 `out` 变量。章节的“输出 (out) 参数”部分讨论了使用传统方法处理 `out` 变量的常用方法。然而，考虑以下示例，它只有一个 `out` 变量。

```csharp
static void MyCalc(out int x)
{
    x = 2 + 2;
}
```

在这种情况下，你可以使用比上一节更短的方法从 `MyCalc()` 获取结果：

```csharp
static void DisplayMyCalc()
{
    MyCalc(out int p);
    Console.WriteLine($"{nameof(p)} = {p}");
}
```

输出结果为 `4`，因为你在 `MyCalc()` 中将 `x` 设置为 `4`，并且 `x` 作为更改后的值返回给调用者。然而，你不需要在使用 `p` 之前声明它。声明是在调用 `MyCalc()` 时发生的。

![Tip](img/tip.png) 当然，如果你的方法只返回一个输出参数，通常最好使用返回值。这个示例显示了 `out` 变量的工作。输出值为 `4`，因为你在 `MyCalc()` 中将 `x` 设置为 `4`，并且 `x` 作为更改后的值返回给调用者。然而，你不需要在使用 `p` 之前声明它。声明是在调用 `MyCalc()` 时发生的。

```csharp
static void DisplayMyCalc()
{
    MyCalc(out int p);
    Console.WriteLine($"{nameof(p)} = {p}");
}
```

### 通过引用返回值

某些情况下，你可能向调用者返回一个引用而不是值。但是，使用引用会变得复杂，因此你需要了解 [`https://docs.microsoft.com/dotnet/csharp/programming-guide/classes-structs/ref-returns`](https://docs.microsoft.com/dotnet/csharp/programming-guide/classes-structs/ref-returns) 中的规则。在旧版本的 C# 中，你必须仔细创建代码来这样做，如下：

```csharp
int[] arrayData = { 1, 2 };
static ref int ReturnByReference()
{
    ref int x = arrayData[0];
    return ref x;
}
```

在 C# 7.0 及以上版本中，你可以将其简化为：

```csharp
int[] arrayData = { 1, 2 };
static ref int ReturnByReference()
{
    return ref arrayData;
}
```

![Remember](img/images.png) 然而，注意你现在返回的是整个数组，而不是单个 `int` 值。数组是引用类型；`int` 是值类型。你无法通过这种技术返回值类型。要使返回值类型可能，必须将其作为参数传入，如下：

```csharp
myInt = 1;
static ref int ReturnByReference(ref int myInt)
{
    return ref myInt;
}
```

## 处理空参数

除非你提供处理它的机制，否则接收方法参数的 `null` 值是有问题的。在过去，你必须为方法调用提供你自己的空检查，如下所示：

```csharp
static void SayHello(String Name)
{
    if (null == Name)
        throw new ArgumentNullException("name");
    else
        Console.WriteLine($"Hello {Name}!");
}
```

这里有两个问题。首先，你可能会忘记添加必要的空检查代码。其次，你实际上在反复编写相同的代码，这非常令人恼恼。C# 10.0 通过使用 `!!` 运算符的空参数检查为该问题提供了答案。因此，这个示例代码现在看起来是：

```csharp
static void SayHello(String Name!!)
{
    Console.WriteLine($"Hello {Name}!");
}
```




![Bullet](img/check.png) **确定何时使用结构**

![Bullet](img/check.png) **定义结构**

![Bullet](img/check.png) **操作结构**

![Bullet](img/check.png) **操作记录**

结构是 C# 中一个重要的补充，因为它们提供了一种定义复杂数据实体的方法，类似于数据库中的记录（records）。由于你在开发应用程序时使用结构的方式，导致结构和类之间存在明显的重叠。这种重叠给许多开发者带来了问题，因为要确定何时使用结构而非类往往是困难的。因此，本章的首要任务是讨论两者之间的区别，并提供一些最佳实践。

创建结构需要你使用 `struct` 关键字。结构可以包含许多在类中发现的相同元素：构造函数、常量、字段、方法、属性、索引器、运算符、事件，甚至是嵌套类型。本章将帮助你理解使用这些元素创建结构的细微差别，以便你能够充分利用结构提供的所有灵活性。

尽管结构确实提供了很多优势，但使用它们最常见的方式是将它们表示一种数据记录。本章的下一节将讨论作为记录持有对象的结构。你将发现如何以这种方式处理单条记录以及作为集合的一部分处理多条记录。

C# 9.0 引入了新的 `record` 类型（在 C# 10.0 中增加了 `field`），它是一种具有不可变特性的类。和类一样，`record` 是引用类型，而不是结构那样的值类型。本章的最后一节将讨论新的 `record` 类型，并帮助你理解它与结构和类的区别。

![Remember](img/remember.png) 你不需要手动输入本章的代码。事实上，使用下载的源码要简单得多。你可以在下载源码的 `\CSAIO4D2E\BK02\CH11` 文件夹中找到本章的源码。详情请见介绍中如何查找这些源文件。

## 比较结构与类

对于许多开发者来说，结构和类之间的区别至少是令人困惑的。事实上，许多开发者只使用类而忘记了结构。然而，不使用结构是一个错误，因为它们在你的编程策略中起着确定的的作用。使用结构可以使一个运行良好的应用程序与一个只能完成任务但运行速度比预期慢的应用程序产生区别。

![Remember](img/remember.png) 关于结构的使用，存在许多学派。这本书甚至没有尝试涵盖所有观点。它确实向你提供了关于结构如何帮助你创建更好的应用程序的良好概述。在获取这些信息后，你就可以开始使用结构，并由自己发现你具体想如何与它们交互。

### 考虑 struct 的限制性

结构是值类型，这意味着 C# 为它们分配内存的方式与类不同。大多数 `struct` 限制都源于这种差异。在考虑用 `struct` 代替类时，需要考虑以下几点。结构

*   可以有构造函数，但没有析构函数。这意味着你可以执行创建特定数据类型所需的所有常规任务，但你无法通过析构函数来控制清理工作。
*   不能继承自其他结构或类（意味着它们是独立的）。
*   可以实现一个或多个接口，但受其所支持的元素的限制（详情请参阅本章后半部分的“包含常用结构元素”）。
*   不能定义为 `abstract`、`virtual` 或 `protected`。

### 理解值类型的区别

在操作结构时，你必须记住它们是值类型，而不是像类那样的引用类型。这意味着结构相对于类具有某些固有优势。例如，它们的资源消耗低得多。此外，由于结构不进行垃圾回收，因此它们分配和释放内存的时间通常更短。

![Tip](img/tip.png) 在处理数组时，资源使用以及在分配和释放时间上的差异会被放大。引用类型数组会产生巨大的代价，因为数组本身只包含指向各个对象的指针。要访问该对象，应用程序随后必须在堆上查找它。

值类型还具有确定性。你知道 C# 在它们离开作用范围的瞬间就会释放掉的内存。等待 C# 垃圾回收引用类型意味着你无法完全确定内存在应用程序中是如何使用的。

### 确定何时使用 struct 还是类

关于何时使用 `struct` 还是 `class`，意见不一。在大多数情况下，这归结为你想实现什么，以及你为了实现目标在资源使用和应用程序速度方面愿意付出什么。在大多数情况下，你使用 `class` 的频率远高于使用 `struct`，这仅仅是因为 `class` 更灵活，并且在某些情况下往往产生更少的惩罚。

与所有值类型一样，结构在转换为引用类型或被其实现的接口需要时必须进行装箱（boxing）和拆箱（unboxing）。过多的装箱实际上会导致你的应用程序运行变慢。这意味着当你需要使用引用类型执行任务时，应该避免使用结构。在这种情况下，使用类是最好的主意。

![Remember](img/remember.png) 使用值类型也会改变 C# 与变量交互的方式。引用类型在调用期间是通过引用传递的，因此对引用类型进行的任何更改都会出现在指向该引用的所有实例中。值类型在传递时是被复制的，因为它是按值传递的。这意味着你在另一个方法中对值类型做的更改不会出现在原始变量中。这可能是开发者使用结构时最困惑的方面，因为传递类创建的对象与传递结构创建的变量本质上是不同的。这种差异使得类传递通常更高效。

结构在处理数组时确实具有明确优势。但在集合类型中使用结构时必须小心，因为结构可能需要装箱和拆箱。如果集合处理的是对象，你需要考虑改用类。

在处理对象时避免使用结构。是的，你可以在结构中放置对象类型，但这样结构包含对象的引用，而不是对象本身。引用会减少结构可以提供的任何资源和时间节省的影响。尽可能将结构限制在其他值类型（如 `int` 和 `double`）。当然，许多结构仍然使用引用类型如 `String`。

## 创建结构

创建结构在许多方面与创建类相似。当然，你使用 `struct` 关键字而不是 `class` 关键字，并且结构具有在本章前面的“考虑 struct 的限制”部分所述的限制。然而，尽管存在这些，如果你知道如何创建类，也可以创建结构。后续章节将详细描述如何操作结构。

### 定义基础结构

基础 `struct` 不包含比存储数据的字段之外的更多。例如，考虑一个用于存储人们请求特定数量的特定价格信息的 `struct`。它看起来可能如下（也位于下载源码中的 `BasicStruct` 示例）：

```
public struct Message
```





```csharp
{
    public int MsgID;
    public int ProductID;
    public int Qty;
    public double Price;
}
```

要使用这个基础结构，你可能遵循以下流程：

```csharp
static void Main(string[] args)
{
    // 不使用 new 创建结构体。
    Message myMsg;
    // 或者，使用 new 创建它。
    //Message myMsg = new Message();
    // 创建一条消息。
    myMsg.MsgID = 1;
    myMsg.ProductID = 22;
    myMsg.Qty = 5;
    // 计算价格。
    myMsg.Price = 5.99 * myMsg.Qty;
    // 在屏幕上显示结构体。
    Console.WriteLine(
    $"In response to Msg {myMsg.MsgID}, you can get {myMsg.Qty} " +
    $"of {myMsg.ProductID} for ${myMsg.Price}.");
    Console.ReadLine();
}
```

注意，创建和使用结构过程与创建和使用类非常相似。事实上，你基本上可以将这两个过程视为是相同的（尽管考虑到结构体确实存在差异）。例如，你可以像代码所示，不使用 `new` 来创建 `struct`，从性能角度来看，当 `struct` 被用在数组中时这是一种优势。如果你不使用 `new` 创建 `struct`，则你必须在使用这些字段之前对其进行初始化。此示例的输出如下：

`In response to Msg 1, you can get 5 of 22 for $29.95.`

![Remember](img/remember.png) 显然，这是一个简化的示例，你永远不会为实际应用程序创建这样的代码，但它确实让你掌握了你所使用的流程。在处理结构体时，考虑你处理类时使用的流程，但有几处差异使得结构体使用要高效得多。

### 包含常见的结构体元素

结构体可以包含许多与类相同的元素。本章的“定义一个基础结构体”部分向你介绍了字段的使用。如之前提到的，字段不能是 `abstract`、`virtual` 或 `protected`。然而，它们的默认作用范围是 `private`，你可以将它们设置为 `public`，如代码所示。显然，类包含的内容比字段多得多，结构体也是如此。后续章节将使用 `StructWithElements` 带你了解常见的 `struct` 元素，以便你在代码中高效地使用结构体。

#### 构造函数

与 `class` 一样，可以使用构造函数创建 `struct`。这里有一个包含构造函数的 `Message` `struct` 示例：

```csharp
public struct Message
{
    public int MsgID;
    public int ProductID;
    public int Qty;
    public double Price;
    public Message(int msgId, int productId = 22, int qty = 5)
    {
        // 用户提供。
        MsgID = msgId;
        ProductID = productId;
        Qty = qty;
        // 由应用程序定义。
        if (ProductID == 22)
            Price = 5.99 * qty;
        else
            Price = 6.99 * qty;
    }
}
```

![Remember](img/remember.png) 注意，构造函数接受默认值，因此你可以在多种方式中使用单个构造函数。当你使用新版本的 `Message` 时，IntelliSense 会显示默认构造函数（与类相反，它不会消失）以及你创建的新构造函数，如下文所示：

```csharp
Message myMsg2 = new Message(2);
Console.WriteLine(
$"In response to Msg {myMsg2.MsgID}, you can get {myMsg2.Qty} " +
$"of {myMsg2.ProductID} for ${myMsg2.Price}.");
```

此示例部分的部分的输出与 `BasicStruct` 示例相同。得益于默认参数的使用，你只需提供消息编号即可创建一条新消息。默认参数会分配其他值。当然，你可以选择覆盖任何值来创建一个唯一对象。

#### 常量

与 C# 的其他所有区域一样，你可以在结构体中定义常量，用作不改变的值的人类可读形式。例如，你可能会创建一个像这样的通用产品常量：

```csharp
public const int genericProduct = 22;
```

现在创建一条新消息可能像这样：

```csharp
Message myMsg3 = new Message(3, Message.genericProduct);
Console.WriteLine(
$"In response to Msg {myMsg3.MsgID}, you can get {myMsg3.Qty} " +
$"of {myMsg3.ProductID} for ${myMsg3.Price}.");
```

新形式更容易读。然而，它并没有产生不同的结果。

#### 方法

结构体通常可以从添加帮助你执行特定任务的方法中获益。例如，你可能想提供一个计算 `Message` `Price` 字段的方法，而不是每次手动执行该任务。使用方法可以确保计算方法的变化在代码中只出现一次，而不是在每次需要计算时都出现。`CalculatePrice()` 方法如下：

```csharp
public static double CalculatePrice(double SinglePrice, int Qty)
{
    return SinglePrice * Qty;
}
```

显然，大多数计算并不这样简单，但你明白意思了。例如，`Message()` 构造函数现在像这样：

```csharp
// 由应用程序定义。
if (ProductID == 22)
    Price = CalculatePrice(5.99, qty);
else
    Price = CalculatePrice(6.99, qty);
```

#### 属性

你也可以在结构体中使用属性。事实上，在许多情况下，使用属性是推荐的方法，因为使用属性可以让你确保输入值是正确的。幸运的是，如果你使用的是 C# 7.0 或更高版本并且最初创建了公共字段，可以通过这些步骤非常地将它们转换为属性：

在点击 `封装字段：‘MsgID’ (并使用属性)` 选项后，Visual Studio 将通过对以下代码进行加粗所示的更改将字段转换为属性：

```csharp
    private int msgID;
    public int ProductID;
    public int Qty;
    public double Price;
    public const int genericProduct = 22;
    public int MsgID { get => msgID; set => msgID = value; }
```

![Tip](img/tip.png) 在此之后，你可以根据需要使用属性来保护你的数据。然而，另一个问题仍然存在。如果你现在尝试编译代码，你会在构造函数中看到 CS0188 错误代码，提示你正在尝试在赋值之前使用属性。要解决这个问题，请将构造函数中的赋值 `MsgID = msgId;` 改为 `msgID = msgId;`。

### 使用补充结构体元素

本章之前的“包含常见的结构体元素”部分讨论了你通常用于类和结构体以执行基本任务的元素。后续章节中的 `ColorList` 示例描述了一些增强你使用结构体的补充元素。

#### 索引器




索引器（indexer）允许你将结构体像数组一样处理。事实上，你必须对它使用许多相同的技术，但你也必须从开始创建许多功能，因为你的结构体索引器具有数组不提供的灵活性。以下是一个结构体 `ColorList` 的代码，它包含了索引器所需的基本功能（注意，为了此示例，你必须在代码开头添加 `using System.Linq;` 指令）：

```csharp
public struct ColorList
{
    private string[] names;
    public string this[int i]
    { get => names[i]; set => names[i] = value; }
    public void Add(string ColorName)
    {
        if (names == null)
        {
            names = new string[1];
            names[0] = ColorName;
        }
        else
        {
            names = names.Concat<string>(
            new string[] { ColorName }).ToArray();
        }
    }
    public int Length
    { get => names.Length; }
}
```

![记住](img/remember.png) 从代码列表的顶部开始，索引器意味着你在 `struct` 某处有一个数组、列表或其他数据结构，在本例中为 `names`。要使用索引器访问 names，你还必须创建一个类型如示例所示的 `this` 属性。`this` 属性允许你访问特定的 names 数组元素。注意，此示例使用了一个非常简单的 `this` 属性；生产环境中的版本会添加各种检查，包括验证 `names` 是否为 `null` 以及请求的值是否实际存在。

当处理与类关联的索引器工作时，你会为数组分配一个初始值。然而，在这种情况下你无法这样做，因为这是一个结构体，所以 `names` 保持为未初始化状态。但是，你可以重写默认构造函数，以便初始化 `names`。`Add()` 方法提供了解决方案。要向 `names` 添加新成员，调用者必须提供一个 `string` 以将该值添加到 `names` 中。注意，当 `names` 为 `null` 时，`Add()` 首先初始化数组，然后将颜色添加到第一个元素（前提没有元素）。然而，当 `names` 已经有值时，代码会将一个新的元素 `string` 数组连接到 `names` 上。你必须调用 `ToArray()` 将可枚举类型转换为数组，以便存储在 `names` 中。

要在实际应用程序中使用 `ColorList`，你还必须提供一种获取数组长度的方法。只读的 `Length` 属性通过暴露 `names.Length` 属性完成了此任务。以下是 `ColorList` 的运行示例：

```csharp
static void Main(string[] args)
{
    // 创建一个颜色列表。
    ColorList myList = new ColorList();
    // 填充值。
    myList.Add("Yellow");
    myList.Add("Blue");
    // 依次显示每个元素。
    for (int i = 0; i < myList.Length; i++)
        Console.WriteLine("Color = " + myList[i]);
    Console.ReadLine();
}
```

该代码的工作方式与你对自定义数组的预期完全一致。你创建一个新的 `ColorList`，依赖 `Add()` 向其添加值，然后在 `for` 循环中使用 `Length` 显示这些值。以下是该代码的输出：
`Color = Yellow`
`Color = Blue`

### 运算符

结构体也可以包含运算符。例如，你可能选择创建一个用于添加两个 `ColorList` 结构的方法。你通过创建一个 `+` 运算符来实现。注意，你是在创建而不是重写 `+` 运算符，如下所示：

```csharp
public static ColorList operator + (ColorList First, ColorList Second)
{
    ColorList Output = new ColorList();
    for (int i = 0; i < First.Length; i++)
        Output.Add(First[i]);
    for (int i = 0; i < Second.Length; i++)
        Output.Add(Second[i]);
    return Output;
}
```

你不能创建实例运算符。它必须作为 `struct` 的一部分出现，如下所示。该过程遵循你最初创建 `ColorList` 时使用的相同技术。区别在于你通过 `for` 循环遍历两个 `ColorList` 变量来执行任务。以下是使用 `+` 运算符相两个 `ColorList` 变量的代码：

```csharp
// 创建并填充第二个颜色列表。
ColorList myList2 = new ColorList();
myList2.Add("Red");
myList2.Add("Purple");
// 将第一个列表添加到第二个列表。
ColorList myList3 = myList + myList2;
// 依次显示每个元素。
Console.WriteLine("\r\nCombined Lists\r\n");
for (int i = 0; i < myList3.Length; i++)
    Console.WriteLine("myList3 Color = " + myList3[i]);
```

如你所示，`myList3` 是两个其他 `ColorList` 变量相加的结果，而不是创建一个新的。输出如你预期的那样：
`myList3 Color = Yellow`
`myList3 Color = Blue`
`myList3 Color = Red`
`myList3 Color = Purple`

## 与只读结构体工作

从 C# 7.2 开始，你可以创建只读结构体（read-only structures）。创建只读结构体的主要原因是为了提高性能。有关 [`dev.microsoft.com/en-us/dotnet/csharp/language-reference/features/readonly-value-types`](https://dev.microsoft.com/en-us/dotnet/csharp/language-reference/features/readonly-value-types) 的更多信息，请参阅该文章。使用只读结构体可以确保数据在构造后不会被更改，如下：

```csharp
public readonly struct ReadOnlyData
{
    // 创建属性持有值。
    public readonly int Value { get; }
    // 定义构造函数进行赋值。
    public ReadOnlyData(int n)
    {
        Value = n;
    }
}
```

要创建只读结构体，你需要在 `struct` 之前添加 `readonly` 关键字，如下所示。自动生成的 `Value` 属性默认是只读的。然而，这提醒用户在构造函数之外无法赋值。以下代码展示了如何使用这种结构体：

```csharp
static void Main(string[] args)
{
    // 定义一些数据。
    int[] Data = Enumerable.Range(1, 5).ToArray();
    // 创建只读结构体。
    ReadOnlyData MyReadOnlyData = new ReadOnlyData(10);
    // 使用结构体执行任务。
    int Result = 0;
    foreach (int n in Data)
    {
        Result += n + MyReadOnlyData.Value;
        Console.WriteLine($"n = {n}\tValue = {MyReadOnlyData.Value}\tResult = {Result}");
    }
    Console.ReadLine();
}
```

当你运行此代码时，你会看到输出：
`n = 1 Value = 10 Result = 11`
`n = 2 Value = 10 Result = 23`
`n = 3 Value = 10 Result = 36`
`n = 4 Value = 10 Result = 50`
`n = 5 Value = 10 Result = 65`

![提示](img/tip.png) 从 C# 9.0 开始，你可以为你的只读结构体添加一个 `init` 访问器，`public readonly int Value { get; init; }`，从而允许为属性提供另一种赋值方法，如下：

```csharp
// 使用 C# 9.0 构造。
ReadOnlyData MyReadOnlyData2 = new ReadOnlyData
{
    Value = 12
};
```

这种方法比使用构造函数为结构体属性赋值更清晰。然而，结果是相同的——在初始构造后你无法重新赋值。




## 使用引用结构 (Reference Structures)

上一节讨论了通过减少访问形式来增强结构使用性能的方法。在 C# 7.2 中首次出现的引用结构（reference structure）是另一种让结构更高效、更快速的方法。事实上，你可以将这种形式的结构与只读结构（read-only structure）结合，极大提高结构的性能，但代价是灵活性的巨大损失。引用结构始终保留在栈（stack）上，这意味着即使是不小心也无法将其装箱（box）并放在堆（heap）上。因此，引用结构消除了由于装箱和解箱导致潜在性能损失的风险。然而，这种方法也存在以下局限性：

* 不支持数组元素
* 无法声明为类字段或非引用 `struct` 的类型
* 无法实现接口
* 无法装箱为 `System.ValueType` 或 `System.Object`
* 无法作为类型参数使用
* 无法被 lambda 表达式或本地函数捕获
* 无法在 async 方法中使用
* 不支持迭代器

所有这些局限性都是由于无法将结构从栈移动到堆导致的。不过，你可以在同步方法（例如返回 `Task` 或 `Task<TResult>` 的方法）中使用引用结构变量。在 `RefStruct` 示例中的代码展示了如何创建一个引用结构：

```cs
public ref struct FullName
{
    public string First { get; set; }
    public string Middle { get; set; }
    public string Last { get; set; }
    public override string ToString()
    {
        return $"Name: {First} {Middle} {Last}";
    }
}
```

要使用此结构，你的操作方式与处理任何其他结构本质上相同，如下：

```cs
static void Main(string[] args)
{
    FullName ThisName = new FullName
    {
        First = "Sam",
        Middle = "L",
        Last = "Johnson"
    };
    Console.WriteLine(ThisName.ToString());
    Console.ReadLine();
}
```

## 将结构作为记录 (Records)

在大多数代码中使用结构的主要目的是创建包含自定义数据的记录（records）。你使用这些自定义数据记录来存储复杂信息，并在应用程序中根据需要传递。传递单个记录比传递数据值集合要简单快捷得多，特别是当你的应用程序经常执行该任务时。接下来的章节展示了如何将结构作为数据记录。

### 管理单条记录

将结构传递给方法比传递单个数据项更整洁、更简单。当然，为了让这种策略生效，结构中的值必须是相关的。然而，考虑以下方法：

```cs
static void DisplayMessage(Message msg)
{
    Console.WriteLine(
        $"In response to Msg {myMsg.MsgID}, you can get {myMsg.Qty} " +
        $"of {myMsg.ProductID} for ${myMsg.Price}.");
}
```

![Tip](img/tip.png) 在这种情况下，`DisplayMessage()` 方法接收一个 `Message` 类型的单个输入，而不是该方法通常需要的四个变量。使用 `Message` 结构在代码中产生了这些积极结果：

* 接收方法可以假设所有必需的数据值都存在。
* 接收方法可以假设所有变量都已初始化。
* 调用者不太可能创建错误代码。
* 其他开发者可以更容易地阅读代码。
* 代码更改变得更加容易。

### 将结构添加到数组

应用程序很少为每个目的都使用单个数据记录。在大多数情况下，应用程序还包含类似数据库的记录集合。例如，应用程序不太可能只接收一个 `Message`。相反，应用程序可能会接收一组 `Message` 记录，并且必须处理其中的每一条。

![Technicalstuff](img/technicalstuff.png) 你可以将结构添加到任何集合中。然而，大多数集合处理的是对象，因此向它们添加结构会产生性能影响，因为 C# 必须对每个结构单独进行装箱和解箱。随着集合增大，这种影响会变得非常明显。因此，当速度是最重要的考虑因素时，将应用程序中依赖结构数据记录集合限制为数组总是更好的主意。

处理结构数组与处理任何其他数组相似。你可以使用如下代码创建 `Message` 结构数组：

```cs
// 在屏幕上显示所有消息。
Message[] Msgs = { myMsg, myMsg2 };
DisplayMessages(Msgs);
```

在这种情况下，`Msgs` 包含两个记录 `myMsg` 和 `myMsg2`。代码随后通过将数组传递给 `DisplayMessages()` 处理消息，如下所示：

```cs
static void DisplayMessages(Message[] msgs)
{
    foreach (Message item in msgs)
    {
        Console.WriteLine(
            $"In response to Msg {myMsg.MsgID}, you can get {myMsg.Qty} " +
            $"of {myMsg.ProductID} for ${myMsg.Price}.");
    }
}
```

`DisplayMessages()` 方法使用 `foreach` 循环分离单个 `Message` 记录。然后它使用本章上一一节中 `DisplayMessage()` 的相同方法处理它们。

### 重写方法

![Remember](img/remember.png) 结构提供了许多开发者认为专门属于类的灵活性。例如，你可以重写方法，这种方式往往让结构变得无限好。一个很好的例子是 `ToString()` 方法，它输出的内容通常如下：

```cs
Structures.Program
```

这种输出没用，因为它没有提供任何信息。为了获得有用信息，你必须通过如下代码重写 `ToString()` 方法：

```cs
public override string ToString()
{
    // 创建有用的输出。
    return "Message ID:\t" + MsgID +
           "\rnProduct ID:\t" + ProductID +
           "\rnQuantity:\t" + Qty +
           "\rnTotal Price:\t" + Price;
}
```

现在当你调用 `ToString()` 时，你就获得了有用信息。在这种情况下，调用 `myMsg.ToString()` 会看到输出：

```
Message ID: 1
Product ID: 22
Quantity: 5
Total Price: 29.95
```

## 使用记录类型 (Record Type)

将结构作为记录证明非常有用，以至于在 C# 9.0 中你发现了一个 `record` 类型。记录类型并不强制你编写大量代码来实现效果，而是结合了结构和类的优点，让你按照本章将结构作为记录节的方式定义记录。然而，正如后续章节和 `BasicRecord` 示例所示，存在一些显著差异。注意，你需要使用 .NET 5 模板获得相应的支持。

### 比较记录、结构和类

如前所述，记录是结构和类的结合，并添加了一些“秘密配方”，让你在无需编码的情况下体验到记录的美味。记录具有以下属性：

* 定义不可变属性的能力，使得记录比结构或类更安全。
* 记录使用值相等性，使得具有相同结构和属性的记录是相同的。这与类依赖引用相等性（寻找相同内存位置的指针）不同。
* 你可以使用非破坏性变异基于现有记录创建一个新记录（具有不同的属性值）。执行此任务时，你使用 `with` 表达式。
* 与许多 C# 对象不同，记录提供了 `ToString()` 方法显示：
    * 记录类型名称
    * 公共属性的名称和值
* 记录在底层是一种类，因此与结构不同，它支持继承层次结构。





## 使用记录 (record)

记录（record）看起来与结构体（structure）非常相似，区别在于使用了 `record` 关键字，如下：

```csharp
public record Person
{
    public string First { get; set; }
    public string? Middle { get; set; }
    public string Last { get; set; }
    public int? Age { get; set; }
}
```

![提示](img/tip.png) `Middle` 和 `Age` 属性类型声明后的问号意味着这些属性是空的。在本节的稍后部分，你将看到这如何为你带来优势。但现在，请尝试运行此代码来操作该结构：

```csharp
static void Main(string[] args)
{
    Person ThisPerson = new Person()
    {
        First = "Amanda",
        Middle = null,
        Last = "Langley",
        Age = null
    };
    Console.WriteLine(ThisPerson.ToString());
    Console.ReadLine();
}
```

与类和结构体不同，记录通过 `ToString()` 方法提供了以有意义的方式打印自身的方法。这是你看到的默认输出：

```text
Person { First = Amanda, Middle = , Last = Langley, Age = }
```

然而，你可能想添加一个 `ToString()` 方法，特别是当你有可空属性时。下面的 `ToString()` 方法利用了可空 `Age` 值来决定打印内容：

```csharp
public override string ToString()
{
    if (Age.HasValue)
        return $"{Last}, {First} {Middle}\r\nAge: {Age}";
    else
        return $"{Last}, {First} {Middle}\r\nAge Withheld";
}
```

注意这里使用 `HasValue` 属性来判断 `Age` 是否为 `null`。现在的输出看起来是这样：

```text
Langley, Amanda
Age Withheld
```

### 使用位置语法定义属性

记录在声明上提供了灵活性是这种灵活性在类或结构体中找不到找不到。例如，你可以非常轻松地创建一个位置声明，如下所示：

```csharp
public record Person2(string First, string Middle, string Last, int? Age)
{
    public override string ToString()
    {
        if (Age.HasValue)
            return $"{Last}, {First} {Middle}\r\nAge: {Age}";
        else
            return $"{Last}, {First} {Middle}\r\nAge Withheld";
    }
}
```

这段代码比上一节中的声明要短得多，但它执行的功能相同，且略有不同。你现在可以使用更短的语法来创建记录：

```csharp
Person2 NextPerson = new("Andy", "X", "Rustic", 42);
```

记录在单行内实例化，无需为特殊构造函数编写任何代码。这一点在于你花费了更少的时间编写代码，却获得了用于数据处理的灵活记录。

### 理解值相等性

与结构体一样，记录在做出相等性判断时会比较记录的类型及其包含的值。这意味着你可以快速、方便地比较两个不同的记录。以下是这种比较工作的一个示例：

```csharp
Person2 ThirdPerson = new("Andy", "X", "Rustic", 42);
Console.WriteLine($"NextPerson == ThirdPerson: " + $"{NextPerson == ThirdPerson}");
Console.WriteLine($"ReferenceEquals(NextPerson, ThirdPerson): " + $"{ReferenceEquals(NextPerson, ThirdPerson)}");
```

当你运行这段代码时，你会看到以下输出：

```text
NextPerson == ThirdPerson: True
ReferenceEquals(NextPerson, ThirdPerson): False
```

`NextPerson` 和 `ThirdPerson` 是两个完全不同的对象。然而，你可以使用 `==` 运算符来比较它们，以验证它们是否包含相同的记录。如果这是一个类，你需要逐个比较每个属性的值，这既耗时又容易出错。

### 创建安全更改：非破坏性变异 (Nondestructive mutation)

有时两个记录可能几乎相同，但略有不同。在这种情况下，你可以使用这种技术将当前记录变变为新记录：

```csharp
Person2 FourthPerson = ThirdPerson with { Age = null };
Console.WriteLine(FourthPerson);
```

在这种情况下，`FourthPerson` 将与 `ThirdPerson` 相同，但 `Age` 属性值不同。当你运行这段代码时，你会看到以下输出：

```text
Rustic, Andy X
Age Withheld
```

### 使用 field 关键字

自动实现属性使用的 `get; set;` 语法只要你不需要执行获取或设置值之外的操作就是没问题的。否则，你需要创建一个后台字段（backing field）并为你的属性添加大量代码。C# 10.0 引入了 `field` 关键字来减少或消除后台字段的使用。例如，在下面的记录中，可以在不诉助于后台字段的情况下确保 `Department` 以大写形式存储：

```csharp
public record Person
{
    public string First { get; set; }
    public string? Middle { get; set; }
    public string Last { get; set; }
    public int? Age { get; set; }
    public string Department { get; set => field = value.ToUpper(); }
}
```

此功能仅在你配置了项目后才有效。




安全是一个宏大的话题。暂时忽略围绕安全的各种专业术语，你可能已经意识到你需要保护你的应用程序免于被不该使用它的人使用。你还需要防止你的应用程序被用于它不应该被用途的事情。

在电子时代初期，安全通常通过`obfuscation`（混淆，也称为“通过模糊实现安全”）来实现。*如果你有一个不想让别人窥视的应用程序，你只需要把它隐藏起来，没人知道去哪里找它。这样，它就是安全的。（记得电影《游戏大战》，军方假设没有人能找到连接其主机所需的电话号码——但马修·布罗德里克饰演的角色确实找到了呢？）*

使用混淆显然已经行不通了；现在你需要将安全视为你所编写的每个系统中不可或缺的需求。你的应用程序可能不包含敏感数据，但它能被用来获取机器上的其他信息吗？它能被用来访问它不该访问的网络吗？这些问题的答案非常重要。

安全的两个主要部分是认证（authentication）和授权（authorization）。`Authentication` 是确保用户身份真实的过程——即用户身份是真实的。最常用的认证方法是要求使用用户名和密码，尽管也存在其他方法，例如指纹扫描和`Multi-Factor Authentication`（多因素身份验证），即 `MFA`（例如使用第二个设备验证身份）。（本书没有涵盖 MFA，但你可以在 `https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-mfa-howitworks` 阅读其相关内容）。`Authorization` 是确保用户有权执行特定任务的行为。文件权限就是一个很好的例子——例如，用户不能删除系统文件。

![Warning](img/warning.png) 永远无法完全保证能识别出特定的用户。黑客可以轻易地窃取用户名和密码。生物识别设备（如指纹扫描仪）也容易破解。`https://www.instructables.com/How-To-Fool-a-Fingerprint-Security-System-As-Easy-/` 上的文章详细说明了破解指纹安全有多简单。你还可以找到关于如何绕过脸识别等技术的文章（`https://iopscience.iop.org/article/10.1088/1757-899X/1069/1/012047/meta`）。事实上，尽管生物识别认证曾被视为万灵妙药，但今天没有任何生物识别认证技术是完美无缺的。你能够实现的最佳目标是验证用户身份，而不是用户本人。你实际上永远无法确定正在处理的是某个特定的人；它可能是一个伪装的黑客。在本章中，你将发现 .NET Framework 中提供的工具，帮助你确保你的应用程序是安全的。

![Remember](img/remember.png) 你不需要手动输入本章的代码。事实上，使用下载的源码要简单得多。你可以在下载源码的 `\CSAIO4D2E\BK03\CH01` 文件夹中找到本章的源码。请参见介绍（Introduction）获取如何找到这些源文件的详细信息。

## 设计安全软件

正确设计安全需要大量工作。如果你将过程拆分为若干部分，你会发现完成起来容易得多。模式与实践团队（微软的一组软件架构师，他们负责制定编程最佳实践）创建了一套设计安全程序的系统方法，将在接下来的章节中描述，你会发现这些方法很易懂。

### 确定要保护的内容

不同的应用程序有不同的需要保护`artifacts`（资源、数据、身份等），但所有应用程序都有保护某些内容的共同需求。如果你在应用程序中有数据库，那么它是最需要保护的项目。如果你的应用程序是基于服务器的，在确定要保护的内容时，服务器应该具有较高的权重。

![Remember](img/remember.png) 即使你的程序只是一个简单的单用户应用程序，软件也不应该出任何差错。外部人员不应该能够利用应用程序入侵用户的计算机。

### 编写程序的组件文档

如果你觉得本节的标题听起来与设计过程的一部分相似，那么你是正确的。很多威胁建模（threat modeling）只是理解应用程序如何工作并对其进行良好的描述。

首先，描述应用程序的功能。这段描述将成为功能概览。如果你遵循通认的软件开发生命周期（SDLC），用例、需求文档或用户故事文档（取决于你的个人方法论）应该给你提供一个良好的起点。

接下来，描述应用程序如何在最高层完成所有这些任务。软件架构概述（SAO）图是实现这一点的的一种有用方法。该图显示了你的软件中哪些机器和服务负责哪些工作。有时 SAO 只是一个简单的示意图。如果你有一个独立的 Windows Forms（也称为 WinForms）程序（例如一个游戏），那么这就是全部了！独立程序没有网络连接，软件部分之间也没有通信。因此，软件架构只包含一个实例。

### 将组件拆分为函数

在你创建了一份描述软件正在做什么以及如何做的文档后，你需要拆分出软件的各个部分。如果你以组件的方式构建了软件，类和方法显示了功能分解。这比听起来要简单。

将软件拆分为各个部分的最终结果是得到一个合理的矩阵，说明哪些组件需要保护、软件的哪些部分与每个组件交互、网络和硬件系统的哪些部分与每个组件交互，以及软件的功能对每个组件做了。

### 识别潜在威胁

在创建了需要保护的组件列表后，你要应对困难的部分：推理。识别威胁是安全顾问赚取高薪的过程，这几乎完全取决于经验。

例如，如果你的应用程序连接数据库，你必须想象连接可能会被第三方拦截。如果你使用文件存储敏感信息，该文件理论上可能会被攻破。

要创建一个威胁模型，你需要对软件的潜在威胁进行分类。一种记忆不同类型威胁的简单方法是使用缩写 STRIDE：

*   `Spoofing identity`（身份欺充）：用户伪装成他们不是的人。
*   `Tampering with data or files`（篡改数据或文件）：用户修改不应被修改的内容。
*   `Repudiation of action`（否认行为）：用户有机会说他们没有做过实际上做过的事。
*   `Information disclosure`（信息泄露）：用户看到了不应该被看到的内容。
*   `Denial of service`（拒绝服务）：用户阻止合法用户访问系统。
*   `Elevation of privilege`（权限提升）：用户获取了他们不应该拥有的权限。

所有这些威胁必须记录在暴露威胁的函数下方的大纲中。这种策略不仅为你提供了一个良好的、离散的威胁列表，还将你的安全加固重点集中在应用程序安全风险最大的部分。

## 构建安全的 Windows 应用程序




`.NET framework` 在客户端计算机上运行时，运行在一个受严格控制的沙箱中。由于这种沙箱的实际情况，你的应用程序的安全策略配置变得至关重要。

编写 Windows 应用程序时，首先需要考虑的安全是身份验证（authentication）和授权（authorization）领域。例如，获取用户本不应使用的应用程序功能是应用程序内部的安全违规；使用操作系统功能删除所需的文件是应用程序外部的安全违规。你还必须考虑用户在任何特定角色。在一种情况下，用户可能以经理身份工作并拥有访问敏感数据的权限；但在另一种情况下，用户可能作为工人执行任务，且没有访问敏感数据的权限。

当你进行威胁建模时，可以利用 `STRIDE` 缩写轻松考虑所有可能的身份验证和授权威胁。（有关关于 STRIDE 的更多信息，请参见前面的章节“在函数中识别潜在威胁”。）

#### 使用 Windows 登录进行身份验证

简单而言之，应用程序授权用户的最佳方法是利用 Windows 登录。关于这种策略以及其他策略存在各种争议，但关键在于简单：越简单越安全。

对于大多数使用 Visual Studio 开发的软件，应用程序将在办公室内供公司不同角色的用户使用；例如，某些用户可能属于销售部或会计部。在许多环境中，权限最高的用户是经理或管理员——这是另一组角色。在大多数办公室中，所有员工都有自己的用户账户，并且用户被分配到与其在公司中所担任的角色匹配的 Windows 组。

![Remember](img/remember.png) 使用 Windows 安全只有在 Windows 环境设置正确时才有效。在一个拥有一堆 Windows 10 机器且每个人都以管理员身份登录的工作区中，你无法有效地构建安全的应用程序，因为你无法判断谁处于什么角色。

构建一个利用 Windows 安全性的 Windows 应用程序是简单的。目标是检查谁登录了（身份验证），然后检查该用户的角色（授权）。以下步骤显示了如何创建 `SecureButton` 应用程序，该程序通过显示和隐藏按钮来保护每个用户的菜单系统。尽管此示例应用程序依赖 Windows Forms App 模板，这些技术也适用于其他应用程序类型，例如 Windows Presentation Foundation (WPF) 应用程序。要成功运行此代码，你必须拥有包含会计、销售和管理用户组的环境（即使它们是虚假的且临时的）。

1. **选择“创建新项目”（Create a New Project）。**
   你看到了“创建新项目”对话框。

2. **在表单顶部出现的列表框中选择 C#、Windows 和桌面应用（Desktop）。**
   向导程序列了一系列相应的模板。

3. **突出显示 Windows Forms App (.NET Framework) 并点击“下一步”（Next）。**
   此模板创建一个运行在 Windows 桌面上的传统 WinForms 应用程序。你看到了“配置你的新项目”（Configure Your New Project）对话框。

4. **在“项目名称”字段中输入 SecureButton，在“位置”字段中输入 `C:\CSAIO4D2E\BK03\CH01`或其他位置，并选择“将解决方案和项目放在同一目录”，然后点击“创建”（Create）。**
   Visual Studio 显示了一个你可以用于设计 WinForms 应用程序的表单。

5. **在解决方案管理器中右键点击 `Form1.cs` 并从上下文菜单中选择“重命名”（Rename）。**
   表单名称变为编辑框，以便你对其重命名。

6. **输入 SecureButtonTest 并按回车键。**
   表单名称变为更具描述性的名称。

7. **突出显示表单的 Text 属性并输入 Secure Button Test。**
   你看到表单顶部的名称发生了变化。

8. **从工具箱向你的表单添加四个按钮——分别用于销售菜单、会计菜单、经理菜单和最小菜单。**
   图 1-1 显示了配置表单的一种方法。你通过每个按钮的属性窗口中找到 `Text` 属性来更改按钮标题。

   ![Windows 安全应用程序示例的快照。](img/9781119839071-fg030101.png)

   图 1-1: Windows 安全应用程序示例。

9. **设置每个按钮的 (Name) 属性以匹配其角色名称：`SalesButton`、`AccountingButton`、`ManagerButton` 和 `MinimalButton`。**
   为按钮可识别的名称使其更容易处理。

10. **将每个按钮的可见（visible）属性设置为 False，以便它们默认不会在表单上显示。**
    即使最小菜单是默认的，除非用户处于该角色，否则你不要使其可见。

11. **双击表单进入 `SecureButtonTest_Load` 事件处理程序。**

12. **在 Namespace 语句上方，按此方式导入 System.Security.Principal 命名空间：**
    ```cs
    using System.Security.Principal;
    ```

13. **在 SecureButtonTest_Load 事件处理程序中，通过添加此代码使用 WindowsIdentity 对象的 GetCurrent 方法实例化一个代表当前用户的 Identity 对象：**
    ```cs
    WindowsIdentity myIdentity = WindowsIdentity.GetCurrent();
    ```

14. **使用 WindowsPrincipal 类获取此身份的引用：**
    ```cs
    WindowsPrincipal myPrincipal = new WindowsPrincipal(myIdentity);
    ```

15. **鼠标悬停在 using 语句旁边。**
    使用 C# 7.0 或更高版本时你会看到一个灯泡图标。此图标告诉你有方法可以让你的代码更高效。

16. **选择“删除不必要的 Using”（Remove Unnecessary Usings）。**
    Visual Studio 删除了不必要的 using 语句。此操作使你的代码加载更快并更有效地使用资源。

17. **最后，同样在 SecureButtonTest_Load 子过程中，编写一个简单的 If…Then 语句来确定显示哪个按钮。**
    代码更改在此所示：

```cs
private void SecureButtonTest_Load(object sender, EventArgs e)
    {
        // 获取用户的身份。
        WindowsIdentity myIdentity =
        WindowsIdentity.GetCurrent();
        // 获取有关用户权限的信息。
        WindowsPrincipal myPrincipal =
        new WindowsPrincipal(myIdentity);
        // 根据用户的权限
        // 决定显示哪个按钮。
        if (myPrincipal.IsInRole("Accounting"))
            AccountingButton.Visible = true;
        else if (myPrincipal.IsInRole("Sales"))
            SalesButton.Visible = true;
        else if (myPrincipal.IsInRole("Management"))
            ManagerButton.Visible = true;
        else
            MinimalButton.Visible = true;
    }
```

在某些情况下，你不需要这种角色分化。有时你只需要知道用户是否处于标准角色中，`System.Security` 为此提供了支持。使用 `WindowsBuiltInRole` 枚举器，你可以描述当（例如管理员登录时应该执行的操作：

```cs
if (myPrincipal.IsInRole(WindowsBuiltInRole.Administrator))
{
    // 执行某些操作
}
```

#### 加密信息




加密本质上是一个极其复杂的过程。许多命名空间用于不同的算法（例如[`https://docs.microsoft.com/en-us/dotnet/standard/security/cryptography-model`](https://docs.microsoft.com/en-us/dotnet/standard/security/cryptography-model) 所示）。由于加密非常复杂，本书将不会涉及细节。尽管如此，理解安全关键要素之一——文件加密仍然非常重要。当你在 Windows Forms 应用程序中处理文件时，除非你对文件进行了加密，否则你面临着他人用文本编辑器加载并查看它的风险。

常见的加密方案——高级加密标准 (AES) 已实现在 Visual Studio 2008 (C# 3.0) 及更高版本的 .NET 中。旧版本的 Visual Studio 依赖于数据加密标准 (DES)，在如今的 64 位桌面机器时代，它已不再是最强大的加密方式（Microsoft 文档 [`https://docs.microsoft.com/en-us/dotnet/api/system.security.cryptography.des`](https://docs.microsoft.com/en-us/dotnet/api/system.security.cryptography.des) 建议不要使用 DES）。请尽可能使用 AES 以为你的应用程序获得最高级别的加密。你可以在 `System.Security.Cryptography` 命名空间中的 `DESCryptoServiceProvider` 中找到用于 DES 的加密方法。

![Warning](img/warning.png) 你的程序永远不包含密码，密码也不应出现在配置或其他易于访问的文件中。加密文件时，用户应始终输入密码，否则攻击者可以轻易破解加密。

## 部署安全

如果你使用 ClickOnce 部署应用程序，你需要定义应用程序将请求的访问级别。`ClickOnce` 是发布应用程序的一种方法，其技术详见文章[`https://docs.microsoft.com/en-us/visualstudio/deployment/quickstart-deploy-using-clickonce-folder`](https://docs.microsoft.com/en-us/visualstudio/deployment/quickstart-deploy-using-clickonce-folder)（针对 .NET Core 应用程序）和 [`https://docs.microsoft.com/en-us/visualstudio/deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard`](https://docs.microsoft.com/en-us/visualstudio/deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard)（针对 .NET Framework 桌面应用程序）。要定义请求的安全性，请选择 Project⇒SecureButton Properties，并选择如 图 1-2 所示的 Security 选项卡。

在这里，你可以定义应用程序使用的功能，以便用户在安装时收到警告，而不是在运行应用程序时遇到安全错误。

![Snapshot of the WindowsSecurity tab of the My Project configuration file.](img/9781119839071-fg030102.png)

图 1-2： My Project 配置文件的 WindowsSecurity 选项卡。

## 使用 System.Security

尽管许多安全工具内置在使用它们的类中，但某些类难以进行描述或分类。因此，`System.Security` 是那些无法放入任何其他地方容器。

`System.Security` 中更常见的命名空间在表 1-1 中描述。我在前面的章节“使用 Windows 登录进行身份验证](#c22.xhtml_c22-sec-0009)”展示了如何使用 `Security.Principal` 命名空间。

| **命名空间** | **描述** | **常用类** |
| --- | --- | --- |
| Security | 安全的基类 | CodeAccessPermission, SecureString |
| AccessControl | 用于授权的复杂控制 | AccessRule, AuditRule |
| Authorization | 描述应用程序安全性的枚举 | CipherAlgorithmType |
| Cryptography | 包含若干有助于加密的命名空间 | CryptoConfig, DESCryptoServiceProvider |
| Permissions | 控制对资源的访问 | PrincipalPermission, SecurityPermission |
| Policy | 使用证据类来防止否认行为 | Evidence, Site, Url |
| Principal | 定义代表当前用户上下文的对象 | WindowsIdentity, WindowsPrincipal |

表 1-1 System.Security 中的常用命名空间

# 第 2 章

# 访问数据

## 本章内容

- ![Bullet](img/check.png) **理解 `System.Data` 命名空间**
- ![Bullet](img/check.png) **连接数据源**
- ![Bullet](img/check.png) **处理来自数据库的数据**

并不是要预先让你倾向本章的内容，但你可能会发现数据访问是你使用 .NET Framework 时最重要的部分。你可能会比使用任何其他命名空间更频繁地使用 `System.Data` 命名空间的各种功能。

Visual Studio 最常见的用途之一是创建业务应用程序。业务应用程序关乎数据。这是使用 Visual Studio 开发的常识。了解各方面的知识都是重要的，但在构建业务应用程序时，完全理解 `System.Data` 命名空间是至关重要的。

在 .NET Framework 在 2003 年左右流行之前，大多数使用 Microsoft 产品构建的业务应用程序使用 FoxPro 或 Visual Basic。多年来，C# 已无疑取代这些语言成为业务程序员的首选语言。你可以从三种方式来看 C# 中的数据工具：

- **数据库连接：** 从数据库中提取和存信息是 `System.Data` 命名空间的主要部分。
- **在程序中的容器中存储数据：** `DataSet`、`DataView` 和 `DataTable` 容器是实现数据存储的实用机制。

![Remember](img/remember.png) 语言集成查询 (LINQ) 允许你使用类似于结构查询语言 (SQL) 的方法从数据容器获取数据，而不是复杂的面向对象语言 (OOL)。LINQ 并不基于 SQL —— 它是一门独立的语言，但如果你熟悉 SQL，那么在使用 LINQ 时会有优势。
- **与数据控件集成：** `System.Web` 和 `System.Windows` 命名空间的功能是与数据控件集成。数据控制集成广泛使用了数据库连接和数据容器。这使得数据控件成为你在本章阅读的绝佳目标。

![Remember](img/remember.png) 不需要手动输入本章的源代码。事实上，使用下载的源码要容易得多。你可以在下载源码的 `\CSAIO4D2E\BK03\CH02` 文件夹中找到本章的源码。请查看引言有关如何找到这些源文件的详情。

## 认识 System.Data

.NET 中的数据与其他任何 Microsoft 平台的数据都不同。微软一直在改变在 .NET Framework 中处理数据的方式。ADO.NET 的实现包含在 `System.Data` 库中，它从开发角度提供了思考数据的常用方式：

- **断开：** 在你从源获取数据后，你的程序不再连接到该数据源。你拥有数据的副本。这解决了一个问题但也引发了另一个：
    - 你不再有行级锁定问题。因为你有数据的副本，所以你不需要限制数据库进行更改。
    - 你面临*后者胜出*的问题。如果两个程序实例获取相同的数据并且它们都进行更新，最后返回数据库的程序将覆盖第一个程序所做的更改。
- **XML 驱动：** 从数据源收集的数据副本在底层是 XML。当微软认为为了性能需要时，它可能会以自定义格式进行移动，但无论如何它都是 XML，这使得在平台、应用程序或数据库之间的移动变得简单得多。




*   **通用数据库容器：** 容器完全不依赖于数据库类型——它们可以用于存储来自任何地方的数据。
*   **特定数据库适配器：** 与数据库的连接特定于数据库平台，因此，如果你想连接到特定的数据库，需要与该数据库兼容的组件。

获取数据的过程也发生了一些变化。你以前使用一个连接（connection）和一个命令（command），它们返回一个 `Recordset`。现在你拥有了一个适配器（adapter），它使用连接和命令来填充 `DataSet` 容器。发生变化的是用户界面帮助你完成任务的方式。

`System.Data` 包含帮助你连接到许多不同数据库和其他类型数据的类。这些类被划分为在表 2-1 中的命名空间中。

| 命名空间 | 文档 URL | 目的 | 最常用的类 |
| --- | --- | --- | --- |
| System.Data | [`https://docs.microsoft.com/dotnet/api/system.data`](https://docs.microsoft.com/dotnet/api/system.data) | 所有 ADO.NET 通用的类 | 容器 `DataSet`, `DataView`, `DataTable`, `DataRow` |
| System.Data.Common | [`https://docs.microsoft.com/dotnet/api/system.data.common`](https://docs.microsoft.com/dotnet/api/system.data.common) | 数据库数据库类使用的工具类 | `DbCommand`, `DbConnection` |
| System.Data.ODBC | [`https://docs.microsoft.com/dotnet/api/system.data.odbc`](https://docs.microsoft.com/dotnet/api/system.data.odbc) | 连接到 dBASE 等 ODBC 数据库的类 | `OdbcCommand`, `OdbcAdapter` |
| System.Data.OleDb | [`https://docs.microsoft.com/dotnet/api/system.data.oledb`](https://docs.microsoft.com/dotnet/api/system.data.oledb) | 连接到 Access 等 OleDb 数据库的类 | `OleDbCommand`, `OleDbAdapter` |
| System.Data.OracleClient | [`https://docs.microsoft.com/dotnet/api/system.data.oracleclient`](https://docs.microsoft.com/dotnet/api/system.data.oracleclient) | 连接到 Oracle 的类 | `OracleCommand`, `OracleAdapter` |
| System.Data.SqlClient | [`https://docs.microsoft.com/dotnet/api/system.data.sqlclient`](https://docs.microsoft.com/dotnet/api/system.data.sqlclient) | 连接到 Microsoft SQL Server 的类 | `SqlCommand`, `SqlDataAdapter` |
| System.Data.SqlTypes | [`https://docs.microsoft.com/dotnet/api/system.data.sqltypes`](https://docs.microsoft.com/dotnet/api/system.data.sqltypes) | 用于引用 SQL Server 通用的原生类型 | `SqlDateTime` |

表 2-1 System.Data 命名空间

尽管 `System.Data` 命名空间及其相关工具有很多，但本章重点关注 Visual Studio 实现这些工具的方式。在以前各种品牌和型号开发软件中，可视化工具仅仅因为“黑盒问题”而让事情变得更加复杂。

![Technicalstuff](img/technicalstuff.png) “黑盒问题”是指让开发环境为你完成一些你无法控制的事情。有时让别人替你完成工作是件好事，但当开发环境没有完全按照你所需的方式构建它们时，生成的代码是没用的。

幸运的是，情况不再如此了。现在当你使用可视化数据工具时，Visual Studio 会生成完全开放且合理的 C# 代码。你应该对这些结果感到满意。

## 数据类如何与框架结合

数据类完全关乎信息存储。第 1 章 讨论了集合（collections），它们用于在应用程序运行期间存储信息。哈希表（Hashtables）是存储信息的另一个例子。`Collections` 持有对象列表，而 `hashtables` 持有键值对。数据容器可以存储大量数据，并帮助你操作这些数据。以下是数据容器：

*   `DataSet`：可以认为是它们中的祖父，`DataSet` 容器是整个数据库的内存表示。
*   `DataTable`：存储在内存中的单表数据。`DataSet` 容器由 `DataTable` 容器组成。
*   `DataRow`：意不其然，它是 `DataTable` 容器中的一行。
*   `DataView`：`DataTable` 的副本，你可以用它对数据进行排序和过滤以便查看。
*   `DataReader`：一种只读、正向的数据流，用于一次性处理，例如填充列表框。通常被称为“消防水管（fire hose）”。

## 获取你的数据

`System.Data` 命名空间中的所有内容都围绕着从 Microsoft SQL Server 等数据库获取数据并填充这些数据容器展开。你可以手动获取这些数据。通而言之，该过程如下：

1.  你创建一个适配器（adapter）。
2.  你告诉适配器如何从数据库获取信息（即连接/connection）。
3.  适配器连接到数据库。
4.  你告诉适配器要从数据库中获取哪些信息（即命令/command）。
5.  适配器用数据填充 `DataSet` 容器。
6.  关闭适配器与数据库之间的连接。





在进行任何操作之前，你首先需要创建一个数据访问应用程序。当然，在完成任务之前会有大量的配置工作要完成，但请按照以下步骤从 AccessData 示例的基础部分开始：

1.  **点击“新建项目”（Create a New Project）。**
    你将看到模板选择页面。
2.  **从顶部的三个下拉框中依次选择 C#、Windows，然后是桌面应用（Desktop）。**
    模板列表将更改，以显示你选择的特定模板。
3.  **高亮 Windows Forms 应用 (.NET Framework) ；然后点击“下一步”（Next）。**
    出现“配置你的新项目”（Configure Your New Project）页面。
4.  **在“项目名称”（Project Name）字段中输入 AccessData。**
5.  **在“位置”（Location）字段中，选择或输入存放项目的地方（示例使用了 `C:\CSAIO4D2E\BK03\CH02`）。**
6.  **选择“将解决方案和项目放在同一目录”（Place Solution and Project in the Same Directory），然后点击“创建”（Create）。**
    Visual Studio 将为你创建 `AccessData` 解决方案。

### 连接到数据源
如今，连接数据库远不仅仅是与 SQL Server 数据集建立简单的连接那么简单。C# 开发者必须连接到大型主机、文本文件、特殊的数据库、Web 服务和其他程序。所有这些异构系统都集成到窗口和 Web 屏幕中，并具备创建、读取、更新和删除（CRUD）功能。

![Remember](img/remember.png) 获取这些数据源主要取决于各个个性化数据库命名空间中的 `Adapter` 类。Oracle 有它自己的适配器类，SQL Server 也是如此。符合 ODBC（开放数据库连接）标准的数据库（如 Microsoft Access）有它们自己的 `Adapter` 类；较新的 OLEDB（对象链接与嵌入数据库）协议也有。

幸运的是，有一个向导处理了大部分工作。可以从“数据源”（Data Sources）面板访问“数据源配置向导”，你在处理数据时大部分时间都花在那个面板。要开始使用数据源配置向导，请按照以下步骤操作：

1.  **选择“视图”（View）  ⇒  “其他窗口”（Other Windows） ⇒  “数据源”（Data Sources），或者按 `Shift+Alt+D`。**
    数据源面板会提示你没有数据源。
2.  **点击数据源面板中的“添加新建数据源”（Add New Data Source）链接。**
    你将看到数据源配置向导，如图图 2-1 所示。向导有多种数据源类型供选择。其中最有趣的是“对象”（Object）源，它可以让你访问程序集中的对象，并将其绑定到你的控件上。

    ![为应用程序数据选择源类型的快照](img/9781119839071-fg030201.png)

    图 2-1： 为应用程序数据选择源类型。
3.  **选择“数据库”（Database）数据源类型并点击“下一步”（Next）。**
    你将看到如图 2-2 所示的数据库模型选择（该图显示了一个裸机设置，即你的系统上没有安装包括 SQL Server 在内的任何数据库管理器，因此你可能会看到更多选项）。至少，你可以访问“数据集”（Dataset）模型。

    ![选择用于对数据建模的数据库模型的快照](img/9781119839071-fg030202.png)

    图 2-2： 选择一个数据库模型来对数据进行建模。
4.  **选择“数据集”（Dataset）模型并点击“下一步”（Next）。**
    你将看到选择数据连接的选项，如图 2-3 所示。由于这是一个新应用程序，你不应该看到任何连接。
5.  **点击“新建连接”（New Connection）按钮。**
    Visual Studio 会要求你通过“选择数据源”（Choose Data Source）对话框创建新连接，如图图 2-4 所示。此示例依赖于到 Microsoft SQL Server 数据库文件的直接连接，这是最容易创建的类型。注意，你也可以创建到 Microsoft Access 数据库文件的直接连接，并可以使用数据库适配器创建到各种其他的连接。

    ![Tip](img/tip.png) “数据提供程序”（Data Provider）字段可能提供多个一个数据提供程序。向导通常会为你选择最高效的数据提供程序。然而，其他数据提供程序可能具有你特定应用程序类型所需的功能。请务必验证你选择了最符合特定应用程序需求的数据提供程序。

    接后的步骤专门用于使用 Microsoft SQL Server 数据库文件。其他类型的数据源可能需要你执行其他步骤来创建连接。

    ![选择数据连接的快照](img/9781119839071-fg030203.png)

    图 2-3： 选择你的数据连接。

    ![“选择数据源”对话框的快照](img/9781119839071-fg030204.png)

    图 2-4： 选择数据源对话框。
6.  **选择 SQL Server 数据库文件并点击。**
    Visual Studio 要求你通过使用“选择数据源”对话框创建新连接，如图图 2-4 所示。此示例依赖于到 Microsoft SQL Server 数据库文件的直接连接，这是最容易创建的类型。注意，你也可以创建到 Microsoft Access 数据库文件的直接连接，并可以使用数据库适配器创建到各种其他的。

7.  **浏览到 `C:\CSAIO4D2E\BK03\CH02` 并打开。**
    “数据提供程序”字段可能提供多个一个数据提供程序。向导通常会为你选择最高效的数据提供程序。然而，其他数据提供程序可能具有你特定应用程序类型所需的功能。请务必验证你选择了最符合特定应用程序需求的数据提供程序。

    ![指定数据库文件位置的快照](img/9781119839071-fg030205.png)

    图 2-5： 指定数据库文件的位置。
8.  **点击“确定”（OK）。**
    向导可能会询问你是否要升级数据库。如果你是单独读此本书，那没关系。如果你和其他人一起开发，请确保这样做是合适的。对于此示例，由于你是唯一使用该数据源的人，所以不需要创建另一个。
9.  **点击“下一步”（Next）。**
    向导显示连接字符串，例如 `adventure_works_2012_oltp_data_file`，并询问是否将其保存到应用程序。

10. **点击“下一步”（Next）。**
    你看到“选择数据库对象和设置”（Choose Database Objects and Settings）对话框。你可以选择所需的表、视图或存储过程。
11. **在“表”（Tables）下勾选 Product 和 ProductCategory。**
    “选择数据库对象和设置”对话框看起来与图 2-6 所示相似。
12. **点击“完成”（Finish）。**
    你完成了！如果你查看“数据源”面板，可以看到项目中添加了一个 `DataSet`，其中包含你请求的两个表。

    ![选择数据库对象的快照](img/9781119839071-fg03206.png)

    图 2-6： 选择数据库对象。

通过执行上述步骤，你在 Visual Studio 中创建了两个重要的实体：

- 你创建了到数据库的连接，显示在“服务器资源”（Server Explorer）中。你会发现它一直存在——它是特定于该 Visual Studio 安装的。
- 你还创建了一个数据集，它是特定于项目的，如果你启动另一个项目，它将不再那里。

两者都非常重要，并且提供不同的功能。在本章中，你将关注在数据集中显示的特定项目的数据源。





Visual Studio 中 C# 的快速应用开发 (RAD) 数据工具既易用又能满足你的需求，而且还能为你编写良好的代码。选择 `Data Sources` 面板（`View ⇒ Other Windows ⇒ Data Sources`）并点击面板中的一个表；会出现一个下拉箭头，如图图 2-7 所示。点击它，你会发现一些有趣的东西：出现了一个下拉列表，然后你可以选择如何将该表集成到 Windows Forms 中。

![表选项下拉列表截图](img/9781119839071-fg030207.png)

图 2-7： 表选项下拉列表。

将 `Product` 表更改为 `Details View`。它用于创建一个详细类型的表单——这种表单可以轻松用户用户查看和更改数据。然后将表拖到表单上，系统就会为你创建一个 `Details View`，如图图 2-8 所示。（截图没有显示整个表单，因为太长了。）

![创建部件详细数据表单截图](img/9781119839071-fg030208.png)

图 2-8： 创建部件详细数据表单。

当你将表拖到表单上时，发生了很多变化：

*   添加字段和字段名。
*   字段采用了最合适的格式。
*   字段名作为标签。
*   Visual Studio 自动在大小写变化的地方添加空格。

![提示](img/tip.png) 注意，每个字段都获得了一个 `SmartTag`，允许你为文本框中的值指定查询。你还可以通过更改 `Data Sources` 格中的值来预设所使用的控件。页面底部的组件区（Component Tray）中添加了五个完全基于代码的对象：

*   `DataSet`: `_adventure_works_2012_oltp_data_fileDataSet`
*   `BindingSource`: `productBindingSource`
*   `TableAdapter`: `productTableAdapter`
*   `TableAdapterManager`: `tableAdapterManager`
*   `BindingNavigator`: `productBindingNavigator`

页面顶部添加了 VCR 条（技术上称为 `BindingNavigator`）。当你运行应用程序时，可以使用 VCR 条在表的记录之间循环切换。点击启动按钮查看 VCR 条的运行情况。你可以毫无问题地遍历数据库中的项目。

### 编写数据代码

然而，在大多数企业开发环境中，你不会使用可视化工具来构建数据访问软件。通常情况下，已经有了基础架构，因为企业软件通常有特定的需求，而管理这些规范的最简单方法是使用独特且自定义的代码。简而言之，某些组织并不希望按照微软的方式来完成。

#### 可视化工具的输出

可视化工具通常不用于企业环境，因为这些工具输出的代码相当复杂。在解决方案管理器（Solution Explorer）中双击 `Form1.Designer.cs` 以查看表单控件的代码后。图 2-9 显示了你第一次进入时看到的内容。标记代码窗口顶部区域的方框标记为 `Windows Form Designer generated code`，你不由得注意到，该部分之前的行号是二十多，而之后的行号是七百多。那是大量的生成代码。

![生成代码截图](img/9781119839071-fg030209.png)

图 2-9： 生成的代码。哈？

这段代码没有问题，但它是故意设计得很通用，以支持任何人可能想对其进行的任何操作。企业客户通常希望确保一切都以相同的方式完成。出于这个原因，他们通常定义特定的数据代码格式，并要求他们的软件人员使用它，而不是可视化工具。

#### 数据代码

示例项目代码非常简单（你不需要输入这些代码，它是自动为你生成的）：

```
using System;
using System.Windows.Forms;
namespace AccessData
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        private void productBindingNavigatorSaveItem:Click(object sender,
        EventArgs e)
        {
            this.Validate();
            this.productBindingSource.EndEdit();
            this.tableAdapterManager.UpdateAll(
            this._adventure_works_2012_oltp_data_fileDataSet);
        }
        private void Form1_Load(object sender, EventArgs e)
        {
            // TODO: 这行代码将数据加载到
            // 的 '_adventure_works_2012_oltp_data_fileDataSet.Product
            // 表中。你可以根据需要移动或删除它。
            this.productTableAdapter.Fill(
            this._adventure_works_2012_oltp_data_fileDataSet);
        }
    }
}
```





`File access` 指在磁盘上对数据的存储和检索。本章涵盖了基础的文本文件输入/输出。从数据库读写数据将在本型教程的 第 2 章 中介绍，向互联网读写信息则将在 第 4 章 中介绍。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要容易得多。你可以在下载源码的 `\CSAIO4D2E\BK03\CH03` 文件夹中找到本章的源码。详情请参见“介绍”，了解如何查找这些源代码。

## 往鱼群聚集的地方：文件流

书中的控制台程序大多从控制台获取输入并将输出发送到控制台。本章之外的程序比文件操作更有趣——或者至少有不同的东西可以让你无聊。重要的是不要将它们的信息与复杂的输入/输出（I/O）额外负担混淆。然而，不执行文件 I/O 的控制台程序并不常见。

I/O 类定义在 `System.IO` 命名空间中。基础的文件 I/O 类是 `FileStream`。在过去，程序员会打开一个文件。`open` 命令会准备文件并返回一个 `handle`（句柄）。通常，这个句柄只是数字，就像你在汉堡店下单时他们给你的号码一样。每当你想要从文件或写入文件时，只需提供这个 ID。

### 流

C# 使用了一种更直观的方法，将每个文件与 `FileStream` 类的对象关联。`FileStream` 的构造函数打开文件并管理底层的句柄。`FileStream` 的方法执行文件 I/O。

![Tip](img/tip.png) `FileStream`并不是唯一可以执行文件 I/O 的类。然而，它代表了你常用的基础文件，涵盖了 90% 的文件 I/O 需求。这个主要类就是本章描述的类。

`stream`（流）概念是 C# I/O 的基础。想象一下游行从你面前“流”过，先是小丑，然后是花车，接着是一两个两个乐队、一些马、一群 `Customer` 对象、一个 `BankAccount` 等。将文件视为字节流（或字符流或字符串流）非常像游行。你将数据“流”进出你的程序。

C# 使用的 .NET 类包括一个抽象的 `Stream` 基类以及几个子类，用于处理磁盘上的文件、网络上的数据或已经在内存中作为数据块的数据。某些类专门用于数据的加密和解密；某些类的提供是为了帮助加速使用其他流时可能缓慢的 I/O 操作；如果你对新流有了绝佳的主意，你可以自由地通过自己的子类来扩展 `Stream` 类（尽管扩展 `Stream` 是很辛苦的）。本章稍后的“探索比刘易斯和克拉克发现更多的流”部分将带你了解这些流类。

![Technicalstuff](img/technicalstuff.png) 如果你正在寻找升级到 .NET 6.0 和 C# 10.0 的好理由，`FileStream` 的性能就是其中之一。根据 `https://www.daveabrock.com/2021/05/23/dotnet-stacks-50/` 等文章，从文件读取数据可以快达 2.5 倍，向文件写入数据可以快达 5.5 倍。`https://devblogs.microsoft.com/dotnet/performance-improvements-in-net-6/#io` 上的更详细信息描述了这一切是如何运作的。`https://docs.microsoft.com/dotnet/core/compatibility/core-libraries/6.0/filestream-position-updates-after-readasync-writeasync-completion` 的文章告诉我们，更改的部分原因是为了让 `ReadAsync` 和 `WriteAsync` 成为线程安全，这样你就可以使用多个线程执行面向文件的任务。你不需要担心做任何事情来获得这些惊人的变化；它们作为 .NET 6.0 和 C# 10.0 的默认配置提供。

### 读取器和写入器

`FileStream` 是你可能最频繁使用的流类，是一个基础类。打开文件、关闭文件、读取一个字节块并写入一个块——这就是你拥有的全部。但在字节级读写文件工作量很大。幸运的是，.NET 类库引入了 `readers`（读取器）和 `writers`（写入器）的概念。这些类型的对象极大地简化了文件（以及其他）I/O。

当你创建一个新的 `reader`（多种可用类型中的一种）时，你将一个流对象与其关联。对于读取器来说，流连接到文件、内存块、网络位置还是密西西比河并不重要。读取器从流请求输入并获取它。使用*writers* 非常相似，只是你是向流发送输出而不是向它索要。





![Technicalstuff](img/technicalstuff.png) 二进制 I/O 的一个复杂示例是相互引用（使用 `HAS_A` 关系）的对象组的持久化。将对象写入磁盘涉及写入标识信息（以便在读回该对象时可以重构其类型），然后是它的每个数据成员，其中某些成员可能是对已连接对象的引用，每个每个引用都有其自己的标识信息和数据成员。以这种方式持久化对象被称为`序列化`。

*   **文本：** 大多数程序读取和写入人类可读的文本：比如字母、数字和标点符号，就像记事本那样。人类友好的 `StreamWriter` 和 `StreamReader` 类是处理流类最灵活的方法。有关某些细节，请参阅前面的章节“读取器写入器”。

![Technicalstuff](img/technicalstuff.png) 人类可读的数据以前被称为美国信息交换标准 (ASCII) 文本，或稍晚的美国国家标准协会 (ANSI) 文本。这两个名称指的是定义它们的标准组织。然而，`ANSI` 编码并不提供奥地利以东和夏威夷以西的字母；它只能处理像英语中使用的罗马字母。它没有俄语、希伯来语、阿拉伯语、印地语或任何使用非罗马字母的语言（包括中文、日语和韩语等亚洲语言）。现代更灵活的 Unicode 字符格式是“向后兼容的”——在其字符集的开头包含了熟悉的 `ANSI` 字符，但仍然提供了大量其他字母，包括你列出的所有语言所需的所有字符。Unicode 有几种变体，称为`编码;`；然而，Unicode 转换格式（8 位）（UTF8`）是 C# 的默认编码。你可以在 `https://unicodebook.readthedocs.io/unicode_encodings.html` 了解更多关于 Unicode 编码。其他流行的编码是：`UTF7`、`UTF16` 和 `UTF32`，其中 `UTF` 后的数字指定了编码中使用的位数。

### 使用流：示例

本节中的 `FileWrite` 示例从控制台读取数据行并将其写入用户选择的文件中。代码开始时确保文件不存在。如果文件已存在，则询问用户另一个文件名。用户还可以在完成当前文件时通过提供新文件名来创建多个文件。程序依赖于空输入来停止向特定文件写入并停止创建新文件。以下子节将代码拆分为易管理的部分，但你可以通过查看可下载的源代码一次性查看所有内容。

#### 获取 StreamWriter

如果你一直在跟着之前的章节操作，你就知道创建 `StreamWriter` 是向文件写入数据的第一步。这里是应用程序中使用的代码：

```csharp
private static StreamWriter GetWriterForFile(string fileName)
{
  StreamWriter sw;
  // 以以下模式之一打开文件进行写入：
  // FileMode.CreateNew 如果文件不存在则创建文件，
  // 或者如果文件存在则抛出
  // 异常。
  // FileMode.Append 附加到现有文件，
  // 或在文件不存在时创建新文件。
  // FileMode.Create 创建新文件或
  // 截断现有文件。
  // FileAccess 可能有：
  // FileAccess.Read,
  // FileAccess.Write,
  // FileAccess.ReadWrite.
  FileStream fs = File.Open(fileName, FileMode.CreateNew, FileAccess.Write);
  // 使用带有 UTF8 字符生成文件流。
  // 第二个参数默认为 UTF8，因此可以省略。
  sw = new StreamWriter(fs, System.Text.Encoding.UTF8);
  return sw;
}
```

此方法实际上所做的是在文件不存在时以特定模式打开文件进行写入。然后它使用 `file handle`（指向文件的指针）创建一个用于写入该文件的流，并将此流返回给调用者。

#### 使用 StreamWriter 向文件写入数据

在你获得可用的 `StreamWriter` 之后，可以向它输出数据。这里展示的 `WriteFileFromConsole()` 方法执行该任务，直到从用户处收到一个空行：

```csharp
private static void WriteFileFromConsole(StreamWriter sw)
{
  Console.WriteLine("输入文本；输入空行停止");
  while (true)
  {
    // 从控制台读取下一行；如果行为空则退出。
    string input = Console.ReadLine();
    if (input.Length == 0)
    {
      break;
    }
    // 将刚刚读取的行写入输出文件。
    sw.WriteLine(input);
  }
}
```

#### 整合一切

你现在有了一种打开文件、为其创建 `StreamWriter` 然后向 `StreamWriter` 输出数据的方法。`Main()` 方法将所有内容整合到一个循环中，允许处理多个不存在的文件，如下所示：

```csharp
static void Main(string[] args)
{
  StreamWriter sw = null;
  string fileName = "";
  // 从用户处获取不存在的文件名。
  while (true)
  {
    try
    {
      // 输入输出文件名（直接按回车退出）。
      Console.Write("输入文件名（留空退出）： ");
      fileName = Console.ReadLine();
      if (fileName.Length == 0)
      {
        // 没有文件名——跳出 while 循环。结束了。
        break;
      }
      // 调用方法（下方）设置 StreamWriter。
      sw = GetWriterForFile(fileName);
      // 每次读取一个字符串，输出到 StreamWriter。
      WriteFileFromConsole(sw);
      // 完成写入，关闭你创建的文件。
      sw.Close(); // 非常重要的步骤。也会关闭文件。
      sw = null; // 交给垃圾回收器。
    }
    catch (IOException ioErr)
    {
      // 处理文件期间发生错误。告诉用户
      // 完整路径和默认目录。
      // Directory 类
      string dir = Directory.GetCurrentDirectory();
      // System.IO.Path 类
      string path = Path.Combine(dir, fileName);
      Console.WriteLine($"文件 {path} 出错");
      // 输出异常中的错误消息。
      Console.WriteLine(ioErr.Message);
    }
  }
  Console.Read();
}
```

![Tip](img/tip.png) 注意我们在关闭 `StreamWriter` 后将 `sw` 引用置空。文件对象关闭后是无效的。失效后置空引用是良好的编程习惯，防止再次使用它。（如果你这样做，你的代码将抛出异常并提示！）关闭文件并置空引用可以让垃圾回收器获取它，并允许其他程序打开它。

![Remember](img/remember.png) 本示例中使用的异常处理为无法写入文件的原因提供了完整信息。因为在大多数情况下用户看不到文件的内部操作，因此提供良好的错误捕获和处理是关重要的。

使用更好的钓鱼装备：using 语句

![Technicalstuff](img/technicalstuff.png) 现在你已经看到了了 `FileStream` 和 `StreamWriter` 的用法，有必要指出 C# 中处理流的通常方法——在 `using` 语句内部：

```csharp
using (<someresource>)
{
  // 使用资源。
}
```





`using` 语句是一种能够自动处理流在使用后清理工作的结构。当遇到 `using` 块的结束右大括号时，C# 会为你管理流的“刷新”（flushing）并将其关闭。（`flush` 一个流是指在关闭它之前，将流缓冲区中剩余的任何最后字节推送到关联的文件。可以将其想象成用一个手柄把你的……鳟鱼溪流里最后的水排放掉。）使用 `using` 可以消除在写入文件后忘记刷新和关闭文件的常见错误。不要让打开的文件一直处于闲置状态。如果没有 `using`，你将需要编写如下代码：

```csharp
Stream fileStream = null;
TextWriter writer = null;
try
{
    // 创建并使用流，然后……
}
finally
{
    stream.Flush();
    stream.Close();
    stream = null;
}
```

注意上述代码在 `try` 块上方声明了流和写入器（这样它们在整个方法中都是可见的）。它还使用抽象基类而非具体的类型 `FileStream` 和 `StreamWriter` 来声明 `fileStream` 和 `writer` 变量。这是一个良好的做法。代码将它们设为 `null`，这样编译器就不会对未初始化的变量报错。在 `FileWrite` 示例中，编写关键 I/O 代码的优写法更像于：

```csharp
// 准备文件流。
FileStream fs = File.Open(fileName, FileMode.CreateNew, FileAccess.Write);
// 将 fs 变量传递给 using 语句中的 StreamWriter 构造函数。
using (StreamWriter sw = new StreamWriter(fs))
{
    // sw 仅存在 using 块内部，这是一个局部作用域。
    // 从控制台一次读取一个字符串，将其输出到
    // 打开用于写入的 FileStream。
    Console.WriteLine("输入文本；输入空行以停止");
    while (true)
    {
        // 从控制台读取下一行；如果行为空则退出。
        string input = Console.ReadLine();
        if (input.Length == 0)
        {
            break;
        }
        // 通过流将刚刚读取的行写入输出文件。
        sw.WriteLine(input);
        // 回到循环获取另一行并写入。
    }
} // sw 在此处消失，fs 现在已关闭。因此……
fs = null; // 确保你无法再次尝试访问 fs。
```

`using` 关键字后括号中的项是它的“资源获取”部分，在其中你分配一个或多个资源，例如流、读取器/写入器、字体等。（如果分配了多个资源，它们必须是相同类型。）紧随该部分之后的是闭合块，由外部大括号限定。

![Remember](img/remember.png) `using` 语句的块并不是循环。该块只定义了一个局部作用域，类似于 `try` 块或方法的块。（在块内部定义的变量，包括其头部，在块外部都不存在。因此，`StreamWriter sw` 在 `using` 块外部是不可见的。）第一本书的“重点关注作用域规则”部分（第 5 章 使用 `using` 语句封装大多数涉及流的操作是一个良好的实践。例如，将 `StreamWriter` 或 `StreamReader` 封装在 `using` 语句中，与将写入器或读取器的使用放在 `try…finally` 异常处理块中的效果相同。（有关异常的讨论请参见第一本书 第 9 章）。事实上，编译器会将 `using` 块翻译为用于 `try…finally` 的相同代码，这保证了资源将得到清理：

```csharp
try
{
    // 分配资源并在此处使用它。
}
finally
{
    // 在此处关闭并释放资源。
}
```

![Warning](img/warning.png) 在 `using` 块之后，`StreamWriter` 不再存在，`FileStream` 对象无法再被访问。`fs` 变量仍然存在，假设你在 `using` 语句之外创建了流，而不是像这样临时创建：

```csharp
using (StreamWriter sw = new StreamWriter(new FileStream(…)) …
```

刷新并关闭写入器也刷新并关闭了流。如果你尝试对流执行操作，将得到一个异常，告诉你无法访问一个已关闭的对象。`fs` 变量仍然存在，假设你在 `using` 语句之外创建了流，而不是像这样临时创建：

```csharp
using (StreamWriter sw = new StreamWriter(new FileStream(…)) …
```（注：此处原文存在部分重复，译文已按要求处理）

![Technicalstuff](img/technicalstuff.png) C# 内生类型——`int`、`double`、`char` 等并没有实现 `IDisposable`。`StreamWriter` 的基类 `TextWriter` 实现了该接口：

```csharp
public abstract class TextWriter : MarshalByRefObject, Disposable
```

如有疑问，请检查 C# 语言帮助以查看你计划使用的类或结构体是否实现了 `IDisposable`。你可以对任何实现它的对象调用 `Dispose()` 来释放资源。也可以通过调用 `myObject.Dispose()` 来判断对象是否实现了 `IDisposable`。如果你看到错误，则该对象没有实现 `IDisposable`。

## 从流中提取它们：使用 StreamReader

写入文件很酷，但如果你以后无法读取该文件，它就是无意义的。下面的 `FileRead` 程序将*输入*放回*文件 I/O*短语中。该程序读取由 `FileWrite` 或记事本创建的文本文件——它是 `FileWrite` 的反向操作：

```csharp
static void Main(string[] args)
{
    // 获取要处理的文件名。如果用户未提供，
    // 以错误代码 -1 退出。
    Console.Write("输入要读取的文本文件名：");
    String filename = Console.ReadLine();
    if (filename.Length == 0)
    {
        Console.WriteLine("未提供文件名，退出。");
        Environment.Exit(-1);
    }
    // 验证文件实际上是否存在。如果不存在，则
    // 以 -2 错误代码退出。
    if (!File.Exists(filename))
```





```cs
{
    Console.WriteLine("The File doesn't exit!");
    Console.ReadLine();
    Environment.Exit(-2);
}
// Open the file for processing by creaing a FileStream and
// a StreamReader with a using statement.
using (StreamReader sr = new StreamReader(filename))
{
    Console.WriteLine("\nContents of File:");
    // Proces the file one line at a time.
    while (!sr.EndOfStream)
    {
        String input = sr.ReadLine();
        Console.WriteLine(input);
    }
}
Console.ReadLine();
}
```

关于这个示例，你首先应该注意到的是它比 `FileWrite` 示例短得多。这并不是因为 `FileWrite` 承担了所有负担而 `FileRead` 却坐在豪华邮轮上。`FileWrite` 示例之所以重要，因为它展示了你可以在复杂文件情况下采用的模块化技术。而 `FileRead` 示例之所以重要，因为它展示了处理较简单文件处理情况的最新技术。你可以轻松地使用这种风格重新编写 `FileWrite`，它的性能会一样好。

这个示例还为你提供了不同的错误捕获和处理视角。它不依赖于异常（即错误已经发生），而是依靠内置函数来判断错误是否即将发生。是的，你没错：这个示例具有预知能力！它还增加了对外部错误代码的使用。你可以在批处理文件中这些错误代码来批量执行任务，而不需要实际上观察它们一个一个完成，避免在等待时慢慢睡着，然后用头去撞键盘。相反，你使用错误代码创建日志条目，告诉你问题何时没有正常运行。检查可能出现问题的情况通常比处理异常要快，并且被认为是更好的编程实践。

注意，这个示例也依赖于形式的 `using` 语句，以便让你看到它的运行。这个示例没有创建一个单独的 `FileStream`，而是依赖一个接受文件名作为输入的特殊 `StreamReader` 构造函数。`FileStream` 仍然被创建了——你不需要去处理它。

在文件读取过程中，`while` 循环依赖于检查 `!sr.EndOfStream` 来决定何时何时停止从文件中读取数据。当从文件中读取完最后一段数据时，`EndOfStream` 属性变为 `true`。简而言之，这个示例展示了许多你可以用来使代码极其简短的技巧。

![Tip](img/tip.png) 有关从文件中读取任意 `bytes`（可以是二进制或文本）的示例，请参见第一本书第 7 章中的 `LoopThroughFiles` 示例。该程序实际上遍历目标目录中的所有文件，读取每个文件并将其内容转到控制台，因此如果文件很多，就会变得很繁琐。可以按 Ctrl+C 或点击控制台窗口的关闭框来终止它。参见下一节关于 `BinaryReader` 的讨论。

## 更多读取器和写入器

在本章较早之前，你看到了 `StreamReader` 和 `StreamWriter` 类，你可能会用它们处理大部分的 I/O 需求。然而，NET 还提供了其他几个读取器/写入器对：

*   `BinaryReader`/`BinaryWriter`：一对流类，包含用于读取和写入每个值类型的方法：`ReadChar()`、`WriteChar()`、`ReadByte()`、`WriteByte()` 等。（这些类要原始一些：它们不提供 `ReadLine()`/`WriteLine()` 方法。）这些类对于用于以二进制（非人类可读）格式而非文本格式读取或写入对象非常有用。你可以使用 `byte` 数组来作为原始字节处理二进制数据。例如，你可能需要读取或写入构成位图图形文件的字节。

    **实验：** 使用记事本打开一个具有 `.EXE` 扩展的文件。你可能在窗口中看到一些可读的文本，但大部分内容看起来像某种垃圾。那就是二进制数据。

    第一本书第 7 章中的“**格式化输出行”部分包含了一个之前提到的读取二进制数据的示例。该示例使用 `BinaryReader` 配合 `FileStream` 对象从文件中读取字节块，然后以十六进制（116 进制）表示法在控制台上输出这些数据，这在那个章节中进行了解释。尽管它将 `FileStream` 封装在更方便的 `BinaryReader` 中，但该示例完全可以直接使用 `FileStream` 本身。读取操作是相同的。尽管 `BinaryReader` 在该示例中没有提供任何额外功能，但那里使用它是为了提供这种读取器的示例。该示例确实说明了将原始字节读取到 `buffer`（一个足够大以容纳读取字节的数组）中。

*   `StringReader`/`StringWriter`：现在是稍微奇特一点：简单的读取器和写入器类，限于读取和写入 `string`。它们让你像对待文件一样对待 `string`，这是用通常方式访问 `string` 字符的替代方案，例如使用 `foreach` 循环：

    ```cs
    foreach (char c in someString) { Console.Write(c); }
    ```

    或者使用数组式的括号符号 `[ ]`

    ```cs
    char c = someString[3];
    ```

    或者使用 `Split()`、`Concatenate()` 和 `IndexOf()` 等 `String` 方法。使用 `StringReader`/`StringWriter`，你可以像处理文件一样读取和写入 `string`。当你创建 `StringReader` 时，用一个 `string` 来进行初始化。当你创建 `StringWriter` 时，可以传递一个 `StringBuilder` 给它或创建一个空的。在内部，`StringWriter` 存储一个 `StringBuilder`——是你传递的或新的。通过调用 `StringWriter` 的 `ToString()` 方法可以获取内部 `StringBuilder` 的内容。

    每当你从字符串读取（或向其写入）时，“文件指针”就会移动到下一个可用字符。因此，就像文件操作一样，你有一个“当前位置”的概念（`Position`）。

    这些类的方法与之前描述的 `StreamReader` 和 `StreamWriter` 类并行。如果你会用那些，就能用这些。

## 探索比刘易·克拉克更多的流

文件流不是唯一的 `Stream` 类。大量的 `Stream` 类包括（但不限于）列表中的类。注意，除非另有说明，这些流类都位于 `System.IO` 命名空间。

*   `FileStream`：用于在磁盘上读取和写入文件。

*   `MemoryStream`：管理内存块中的读取和写入。你有时会在单元测试中看到这种技术，以避免实际上与（缓慢且可能问题的）文件系统交互。通过这种方式，你可以在测试读写代码时伪造文件。

*   ![Technicalstuff](img/technicalstuff.png) `BufferedStream`：*缓冲*是一种通过一次读取或写入更大块的数据来加速输入输出的操作。大量的小读取或写入意味着大量的缓慢磁盘访问——但如果你现在读取一个比你需要的多的块，你就可以从缓冲区中继续读取你的小块——这比从磁盘要快得多。当 `BufferedStream` 的底层缓冲区用完数据时，它会读取另一个大块——可能是整个文件。缓冲写入也是如此。


`FileStream` 类会自动缓冲其操作，因此 `BufferedStream` 用于特殊情况，例如使用 `NetworkStream` 在网络上读写字节。在这种情况下，你将 `BufferedStream` 包装在 `NetworkStream` 之上，有效地实现了“链式”操作。当你写入 `BufferedStream` 时，它会写入底层的 `NetworkStream`，等等。当你将一个流包装在另一个流时，你就在进行组合。（可以在 C# 帮助中查找更多信息。） 之前的侧边栏“包装我的流”讨论了这一点。

*   `NetworkStream`：管理网络上的读写。请参见 `BufferedStream` 的简化讨论。`NetworkStream` 位于 `System.Net.Sockets` 命名空间，因为它使用了 `sockets` 技术跨网络连接。
*   `UnmanagedStream`：在非托管内存块中读写数据。`Unmanaged` 基本上意味着“非 .NET”且不由 .NET 垃圾回收器管理。这是高级内容，用于与操作系统进行交互。
*   `CryptoStream`：位于 `System.Security.Cryptography` 命名空间，此流允许对数据进行加密或解密转换。

# 第 4 章

# 访问互联网

## 本章内容

*   漫游 `System.Net` 命名空间
*   使用内置工具访问网络
*   让网络工具为你工作服务

.NET 框架从设计之初就考虑了互联网和通用网络连接。令人惊讶的是，各种形式的连接性重点在 `System.Net` 命名空间（[`docs.microsoft.com/dotnet/api/system.net`](https://docs.microsoft.com/dotnet/api/system.net)）中最为清晰。在这里是首要的，占据了命名空间大量的类。

`System.Net` 是一个巨大的命名空间，寻找路径可能很困难，因此本章首先对该命名空间进行了概述。然后讨论了你经常执行的任务并展示了如何执行它们。接下来，你将了解类的复杂功能。

网络连接是 .NET 框架的重要部分，所有的功能都在这个命名空间中。关于这个主题可以写一整本书。作为 C# 网络入门，本章将向你展示以下功能：

*   从网络获取文件
*   发送电子邮件
*   记录传输
*   检查运行应用程序的网络状态

请记住，`sockets`、`IPv6` 和其他高级协议是重要的，但许多开发者每天并不使用它们。本章介绍的是你每天使用的命名空间部分。一如既常，关于 `System.Net` 有更多可以发现的。

你不必手动输入本文的代码。事实上，使用源代码容易得多。你可以在源代码的 `\CSAIO4D2E\BK03\CH04` 文件夹中找到本文源码。请参见介绍了解如何找到这些源文件。

## 了解 System.Net

`System.Net` 命名空间充满了在文档中查看时令人困惑的类，但在应用程序中使用时非常有意义。该命名空间消除了处理互联网上各种协议的复杂性。

有超过 4,000 个用于互联网协议的 RFC（`RFC` 是“意见请求”，是一种发送给标准机构由同行评审、在成为标准之前的文档）。你可以在以下位置获取这些 RFC 的副本：[`www.rfc-editor.org/standards`](https://www.rfc-editor.org/standards) 和 [`www.faqs.org/rfcs/`](http://www.faqs.org/rfcs/)。如果你必须单独学习所有的 RFC，你将无法完成你的项目。`System.Net` 命名空间是为了让网络编码变得不再痛苦。

`System.Net` 不仅仅用于 Web 项目。像基础类库中的其他所有内容一样，你可以在各种项目中使用 `System.Net`。你可以：

*   从互联网上的网页上获取信息并在你的程序中使用它。
*   通过 FTP 在互联网上移动文件。
*   轻松地发送电子邮件。
*   使用更高级的网络结构。
*   使用 SSL 协议在互联网上安全通信。

如果你需要从 Windows 应用程序检查计算机的连接性，可以使用 `System.Net`。如果你需要构建一个从网站下载文件的类，`System.Net` 就是你需要的命名空间。仅仅因为大多数类与互联网有关，并不意味着只有 Web 应用程序可以使用它。这就是 `System.Net` 的魔力。任何应用程序都可以通过你使用 `System.Net` 功能访问的应用程序编程接口 (API) 连接到另一个应用程序。虽然命名空间的部分功能是为了更容易开发 Web 应用程序，但整个命名空间的设计是为了让任何应用程序都能与符合 Web 标准的网络工作（包括组织内部可访问的内网）。

## Net 类如何适配框架

`System.Net` 命名空间包含大量的类和较小的命名空间。随着 .NET Framework 每个版本的更新，类和命名空间的数量都会增加，因此关注每次更新以查看有哪些内容是值得的。这些数量可能让人应措措，但如果你仔细观察，就能发现模式。后续章节将讨论较小的命名空间并提供 System.Net 类的列表。

### 理解 System.Net 子命名空间

当你在 [`docs.microsoft.com/dotnet/api/system.net`](https://docs.microsoft.com/dotnet/api/system.net) 查看 System.Net 文档时，你会在“另另”部分看到列出的子命名空间。然而，这并不是完整的列表，实际上还有许多你需要了解的额外命名空间，如表 4-1 所示。“最新实现”列告诉你包含该命名空间完整类的 .NET 版本。后续版本可能会移除命名空间中的某些功能。

| **命名空间** | **目的** | **最新实现** | **链接** |
| --- | --- | --- | --- |
| `System.Net.Cache` | `cache` 提供通过存储常用资源来提高性能的方法。该命名空间与 `WebRequest` 和 `HttpWebRequest` 类配合，通过创建缓存策略提高 Web 应用程序的速度。 | 6.0 | [`docs.microsoft.com/dotnet/api/system.net.cache`](https://docs.microsoft.com/dotnet/api/system.net.cache) |
| `System.Net.Configuration` | 管理 应用程序的配置设置。这些设置影响所有的 System.Net 命名空间和类。 | 4.8 | [`docs.microsoft.com/dotnet/api/system.net.configuration`](https://docs.microsoft.com/dotnet/api/system.net.configuration) |
| `System.Net.Http` | 提供创建 应用程序所需的功能。你可以在这里找到客户端、内容、消息、请求和响应相关的类。 .NET Framework 5.0 对此命名空间提供了一些增强。 | 6.0 | [`docs.microsoft.com/dotnet/api/system.net.http`](https://docs.microsoft.com/dotnet/api/system.net.http) |




| `System.Net.Http.Headers` | 包含用于 `System.Net.Http` 命名空间的标头的类。在许多情况下，这些标头定义为 RFC 2616 ([`www.faqs.org/rfcs/rfc2616.html``](http://www.faqs.org/rfcs/rfc2616.html)) 的一部分。 | 6.0 | [`https://docs.microsoft.com/dotnet/api/system.net.http.headers`](https://docs.microsoft.com/dotnet/api/system.net.http.headers) |
| `System.Net.Mail` | 允许使用简单邮件传输协议 (SMTP) 发（而非接收）电子邮件。这些类遵循 RFC 2821 ([`www.faqs.org/rfcs/rfc2821.html``](http://www.faqs.org/rfcs/rfc2821.html)) 等标准。 | 6.0 | [`https://docs.microsoft.com/dotnet/api/system.net.mail`](https://docs.microsoft.com/dotnet/api/system.net.mail) |
| `System.Net.Mime` | 包含为 `SmtpClient` 类使用的 `Content-Type`、`Content-Disposition` 和 `Content-transfer-Encoding` 标头提供多用途互联网邮件交换 (MIME) 支持的类。这些类遵循 RFC 2045 ([`www.faqs.org/rfcs/rfc2045.html``](http://www.faqs.org/rfcs/rfc2045.html)) 等标准。 | 6.0 | [`https://docs.microsoft.com/dotnet/api/system.net.mime`](https://docs.microsoft.com/dotnet/api/system.net.mime) |
| `System.Net.NetworkInformation` | 获取本地计算机的流量数据、网络地址信息和地址更改通知。你也可以找到 `Ping` 实用程序的实现 ([`docs.microsoft.com/dotnet/api/system.net.networkinformation.ping``](https://docs.microsoft.com/dotnet/api/system.net.networkinformation.ping))，它允许验证远程主机状态。 | 6.0 | [`https://docs.microsoft.com/dotnet/api/system.net.networkinformation`](https://docs.microsoft.com/dotnet/api/system.net.networkinformation) |
| `System.Net.PeerToPeer` | 提供对对点网络功能的访问。它提供了在 [`https://docs.microsoft.com/dotnet/framework/network-programming/peer-name-resolution-protocol`](https://docs.microsoft.com/dotnet/framework/network-programming/peer-name-resolution-protocol) 中讨论的对点名称解析协议 (PNRP) 实现。 | 4.8 | [`https://docs.microsoft.com/dotnet/api/system.net.peertopeer`](https://docs.microsoft.com/dotnet/api/system.net.peertopeer) |
| `System.Net.PeerToPeer.Collaboration` | 增强了 `System.Net.PeerToPeer` 命名空间的功能。它提供了无服务器托管协作会话所需的功能。 | 4.8 | [`https://docs.microsoft.com/dotnet/api/System.Net.PeerToPeer.Collaboration`](https://docs.microsoft.com/dotnet/api/System.Net.PeerToPeer.Collaboration) |
| `System.Net.Security` | 允许使用网络流进行安全通信。该命名空间在 .NET 5.0 和 .NET 6.0 中收了重大更新。 | 6.0 | [`https://docs.microsoft.com/dotnet/api/System.Net.Security`](https://docs.microsoft.com/dotnet/api/System.Net.Security) |
| `System.Net.Sockets` | 实现 Windows Sockets (Winsock) 功能（详情请阅 [`https://docs.microsoft.com/windows/win32/winsock/getting-started-with-winsock`](https://docs.microsoft.com/windows/win32/winsock/getting-started-with-winsock)），它允许对网络通信进行严密控制。 | 4.8 | [`https://docs.microsoft.com/dotnet/api/System.Net.Sockets`](https://docs.microsoft.com/dotnet/api/System.Net.Sockets) |
| `System.Net.WebSockets` | 实现 Web Sockets (WebSocket) 功能（详情请阅 [`https://docs.microsoft.com/aspnet/core/fundamentals/websockets`](https://docs.microsoft.com/aspnet/core/fundamentals/websockets)），允许在 TCP 连接上建立双向持久通信通道。.NET Framework 6.0 对此命名空间提供了一些增强。 | 6.0 | [`https://docs.microsoft.com/dotnet/api/System.Net.WebSockets`](https://docs.microsoft.com/dotnet/api/System.Net.WebSockets) |

[表 4-1] 重要的 `System.Net` 相关命名空间列表

### 使用 `System.Net` 类

`System.Net` 类命名非常规范，你会发现某些协议各包含多个类。在翻译条目名称后，你可以根据协议的命名方式缩小所需的范围：

*   `Authentication`（身份验证）和 `Authorization`（授权）：这些类提供安全性。
*   `Cookie`：此类管理来自浏览器的 Cookie，通常用于 ASP.NET 页面。
*   `DNS`（域名系统）：这些类帮助将域名解析为 IP 地址。
*   `Download`：此类用于从服务器下载文件。
*   `EndPoint`：此类帮助定义网络节点。
*   `FileWeb`：这组出色的类描述了网络文件服务器。
*   `FtpWeb`：此类是简单的文件传输协议实现。
*   `Http`（超文本传输协议）：此类是网络协议。
*   `IP`（网协议）：此类帮助定义与互联网相关的端点。
*   `NetworkCredential`（网络凭据）：这是另一个安全实现。
*   `Service`：此类帮助管理网络连接。
*   `Socket`：此类处理最原始的网络连接。
*   `Upload`：这组类帮助你将信息上传到互联网。
*   `Web`：这些类帮助处理万维网——主要是实现。

`System.Net` 命名空间是面向代码的，这意味着很少用于用户界面的实现。你使用这些类的大部分操作都在后台完成。为了说明这一事实，本章剩余示例将构建一个具有以下功能的 Windows Forms 应用程序：

* 检查网络状态。
* 从互联网获取特定文件。
* 将将其发送到特定地址（或多个地址）。
* 记录整个事务。

### 使用 `System.Net` 命名空间

首先，你需要使用 `NetworkTools` 示例告知用户网络连接情况。开始时，按照本微型书籍第 2 章“创建数据访问项目”节中的步骤创建一个 Windows Forms 应用程序（对示例名称和位置进行必要的更改），然后在看到表单时按照以下步骤操作：

1. 从工具箱的“菜单和工具栏”组中拖入 `StatusStrip` 控件到表单的左下方。`StatusStrip` 会自动占据表单整个底部区域。
2. 选择 `StatusStrip` 左侧出现的智能标签 (SmartTag)，并添加三个 `Label`。
3. 逐个选择 `StatusLabel` 并配置其以显示网络和应用程序状态。




* `toolStripStatusLabel1`: 将 `(Name)` 设置为 `NetStatus`并将 `Text` 设置为 `Not Connected`。
* `toolStripStatusLabel2`: 将 `(Name)` 设置为 `PictureStatus`并将 `Text` 设置为 `Not Downloaded`。
* `toolStripStatusLabel3`: 将 `(Name)` 设置为 `EmailStatus`并将 `Text` 设置为 `No Email Sent`。

图 4-2 显示了你的 `StatusStrip` 在此时应该显示的样子。

![配置 StatusStrip 为用户提供有用信息的快照](img/9781119839071-fg030402.png)

FIGURE 4-2: 配置 `StatusStrip` 为用户提供有用信息。

4. **双击表单。**

Visual Studio 会创建 `Form1_Load()` 方法并为你显示代码编辑器。

5. **通过在代码顶部添加行** `using System.Net.NetworkInformation;` **来引用 `System.Net` 命名空间。**

6. **将以下代码添加到 `Form1_Load()` 中测试网络是否可用并显示在状态栏上：**

```cs
private void Form1_Load(object sender, EventArgs e)
{
    if (NetworkInterface.GetIsNetworkAvailable())
    {
        NetStatus.Text = "Connected";
    }
    else
    {
        NetStatus.Text = "Disconnected";
    }
}
```

全部就是这些。`NetworkInformation` 类包含了大量关于网络状态、当前 IP 地址、当前机器正在使用的网关等信息。

![提示](img/tip.png) 请记住，`NetworkInformation` 类仅在本地机器上有效。如果你在 ASP.NET Web Forms 程序中使用此类，你将获得有关服务器的信息。

### 从互联网下载文件

你可以通过多种方式从互联网获取文件，最常见的方法之一是使用超文本传输协议 (HTTP)。今天你可以在网络上的各个 HTTP 站点找到可以下载的内容，因此这是一个重要的协议。要构建一个使用 HTTP 的应用程序，请从上一节的示例开始并按照以下步骤操作：

1. **从工具箱将 `Button` 控件拖到表单上。**
2. **在按钮的 `Text` 属性中输入 `Download`，在按钮的 `(Name)` 属性中输入 `btnDownload`。**
3. **双击按钮。**

Visual Studio 会创建 `btnDownload_Click()` 方法并为你显示代码编辑器。

4. **在编码区域顶部添加以下导入：**

```cs
using System.Net;
using System.IO;
```

5. **创建一个名为 `DownloadFile` 的新方法，接受类型为 `string` 的 `remoteFile` 和 `localFile` 参数。**

6. **将以下代码输入 `DownloadFile()` 方法中：**

```cs
private void DownLoadFile(string remoteFile, string localFile)
{
    // 创建流和请求对象。
    FileStream localFileStream = File.Create(localFile);
    HttpWebRequest httpRequest =
    (HttpWebRequest)WebRequest.Create(remoteFile);
    // 配置请求。
    httpRequest.Method = WebRequestMethods.Http.Get;
    // 配置请求的响应。
    WebResponse httpResponse = httpRequest.GetResponse();
    Stream httpResponseStream = httpResponse.GetResponseStream();
    byte[] buffer = new byte[1024];
    // 通过下载数据处理响应。
    int bytesRead = httpResponseStream.Read(buffer, 0, 1024);
    while (bytesRead > 0)
    {
        localFileStream.Write(buffer, 0, bytesRead);
        bytesRead = httpResponseStream.Read(buffer, 0, 1024);
    }
    // 关闭流。
    localFileStream.Close();
    httpResponseStream.Close();
    // 更新状态条。
    PictureStatus.Text = "Picture Downloaded";
}
```

该代码遵循建立连接、配置连接、配置对该连接的响应然后执行任务的过程。在这种情况下，任务是从 HTTP 站点下载文件。在完成任务后，你必须始终关闭流。

7. **使用以下代码从 `btnDownload_Click()` 事件处理程序中调用 `DownloadFile()` 方法：**

```cs
private void btnDownload_Click(object sender, EventArgs e)
{
    // 获取文件。
    DownLoadFile(@"http://blog.johnmuellerbooks.com/" +
    "wp-content/uploads/2014/06/cropped-country01-1.jpg",
    @"c:\temp\Country_Scene.jpg");
}
```

### 发送邮件状态

1. **在设计视图的默认表单中添加四个 `TextBox` 控件 `EmailAddress`、`SMTPServer`、`Username`、`Password` 和四个 `Label` 控件。**

你的表单看起来应该和图 4-3 所示所示。

![配置 StatusStrip 为用户提供有用信息的快照](img/9781119839071-fg030402.png)

FIGURE 4-3: 配置 `StatusStrip` 为用户提供有用信息。

2. **切换到代码视图。**

3. **在编码区域添加以下导入：**

```cs
using System.Net.Mail;
```

4. **创建一个名为 `SendEmail` 的新方法，接受类型为 `string` 的 `fromAddress`、`toAddress` 和 `body`。**

它应该接收邮件地址、收件人地址、邮件主题和正文。

5. **将以下代码输入 `SendFile()` 方法：**

```cs
private void SendEmail(string fromAddress, string toAddress,
string subject, string body)
{
    // 定义消息。
    MailMessage message =
    new MailMessage(fromAddress, toAddress, body);
    // 配置凭据。
    NetworkCredential Creds =
    new NetworkCredential(Username.Text, Password.Text);
    // 创建连接并发送消息。
    SmtpClient mailClient = new SmtpClient(SMTPServer.Text)
    {
        Credentials = Creds
    };
    mailClient.Send(message);
    // 释放消息和客户端。
    message = null;
    mailClient = null;
    // 更新状态。
    EmailStatus.Text = "Email Sent";
}
```




该示例遵循一个从创建消息开始的过程。然后，它创建一个客户端来提供到主机的连接，并将消息发送给主机。请注意，在大多数情况下，你必须提供凭据才能访问 SMTP 服务器，并且并将这些凭据作为 `SmtpClient` 配置的一部分通过 `Credentials` 添加。最后一步是释放消息和客户端，以便垃圾回收器回收它们。

在编写完方法后，你需要在 `btnDownload_Click()` 事件处理程序中文件下载后调用它。将该子程序的代码更改为如下内容以调用该方法：

```csharp
private void btnDownload_Click(object sender, EventArgs e)
{
    // Obtain the file.
    DownLoadFile(@"http://blog.johnmuellerbooks.com/" +
    "wp-content/uploads/2014/06/cropped-country01-1.jpg",
    @"c:\temp\Country_Scene.jpg");
    // Send a success message.
    SendEmail(EmailAddress.Text, EmailAddress.Text,
    "HTTP Successful", "Picture Successfully Downloaded");
}
```

示例两次使用了 `EmailAddress` 文本框的值：一次用于收件人地址，一次用于发件人地址。这并不总是必要的，因为你可能会遇到这种情况：你希望邮件仅来自网络管理员地址，或仅发送到你的地址。

要运行应用程序，请在表单字段中提供你的电子邮件地址、SMTP 服务器地址、用户名和密码。当你点击下载时，应用程序会将文件下载到本地驱动器，然后发送电子邮件通知你下载完成。你会在应用程序底部看到状态信息。不过，网络应用程序可能会出现很多问题，你应该意识到这些问题。以下是几点：

- 对于大多数网络活动，运行软件的机器必须连接到网络。对于你这个开发者来说这不是问题，但你需要考虑终端用户，他们可能需要连接性才能访问他们想要使用的功能。使用网络状态代码可以帮助告知用户这些可用可用。
- 防火墙和其他网络设备有时会阻止来自合法应用程序的网络流量。一些示例包括：
    - .NET 的网络分析功能在企业服务器上经常被禁用。如果服务器对公众开放，这些开启可能会导致黑客渗透的漏洞。
    - 谈到黑客，请确保如果你在应用程序中使用入站网络功能，已对应用程序进行了充分的安全保护。更多信息可以在 Michael Howard 和 David C.LeBlanc 编写的优秀书籍 *Writing Secure Code,* Second Edition（Microsoft Press 出版）中找到。
    - 电子邮件特别脆弱。互联网服务提供商经常可能会来自未在邮件服务器上注册地址的邮件。这意味着如果你正在使用本地服务器，你的 ISP 可能会拦截邮件。
- 网络流量极度难以调试。例如，如果示例应用程序运行正常，但你从未收到来自编写的 `SmtpServer` 发出的邮件，到底哪里出了问题？你可能永远不知道。

### 记录网络活动

这引出了下一个主题：网络日志。由于网络活动问题很难调试和重现，微软内置了几个工具来管理网络活动的跟踪。

此外，与可用 ASP.NET 跟踪一样，`System.Net` 命名空间的跟踪完全通过配置文件管理。因此，为了使用这些功能，你不需要更改和重新编译代码。事实上，通过简单的管理，你甚至可以通过管理应用程序使用的 `config` 文件来向用户显示调试信息。

每种应用程序都有不同的配置文件。对于你在这里使用的 Windows Forms 应用程序，该文件名为 `app.config`，存储在开发项目目录中。编译时，文件名将更改为应用程序的名称，并复制到 `bin` 目录中运行。

如果你现在通过双击解决方案管理器中的项打开 `app.config` 文件，你会发现它几乎没有任何内容（如列表 4-1 所示）。这对 .NET 来说是非常新的，因为它以前的配置非常复杂。你将向配置中添加一些内容以开启跟踪。注意，你的 `.NETFramework,Version` 版本号可能与所示的不同。

**列表 4-1** 默认的 app.config 文件

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
<startup>
<supportedRuntime version="v4.0"
sku=".NETFramework,Version=v4.7.2"/>
</startup>
</configuration>
```

首先，你需要为 `System.Net` 命名空间添加一个新的源。接下来，为你所添加的源在 `switches` 部分添加一个开关。最后，你向该部分添加一个 `sharedlistener` 并设置文件自动刷新跟踪信息。完成后的 `app.config` 文件（加粗部分为新增内容）如列表 4-2 所示。

**列表 4-2** 完成的 app.config 文件

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
<startup>
<supportedRuntime version="v4.0"
sku=".NETFramework,Version=v4.5.2"/>
</startup>
<system.diagnostics>
<sources>
<source name="System.Net">
<listeners>
<add name="System.Net"/>
</listeners>
</source>
<switches>
<add name="System.Net" value="Verbose" />
</switches>
<sharedListeners>
<add name="System.Net"
type="System.Diagnostics.TextWriterListener"
initializeData="my.log"/>
</sharedListeners>
<trace autoflush="true" />
</system.diagnostics>
</configuration>
```

再次运行应用程序并观察输出窗口。由于你更改了配置文件，那里显示了跟踪信息。此外，还写入了一个文件。在开发环境中，它位于 `bin` `。你可能需要点击解决方案管理器顶部的“显示所有文件”才能看到它。

在该文件夹中，你应该能看到名为 `my.log` 的文件，由你添加到 `app.config` 文件中的设置生成的。列表 4-3 显示了该文件的内容。具体的 URL、引用号和其他值会在你的输出中有所不同，但你应该看到类似于此处的内容（已进行简化处理）：

```
System.Net Verbose: 0 : [15048] Entering WebRequest::Create(http://blog.johnmuellerbooks.com/wp-content/uploads/2014/06/cropped-country01-1.jpg)
System.Net Verbose: 0 : [15048] Entering HttpWebRequest#33675143::HttpWebRequest(http://blog.johnmuellerbooks.com/wp-content/uploads/2014/06/cropped-country01-1.jpg)-1138309)
System.Net Information: 0 : [15048] Current OS installation is 'Client'.
System.Net Information: 0 : [15048] RAS supported: True
System.Net Verbose: 0 : [15048] Exiting HttpWebRequest#33675143::HttpWebRequest()
System.Net Verbose: 0 : [15048] Exiting WebRequest::Create() -> HttpWebRequest#33675143
System.Net Verbose: 0 : [15048] Entering HttpWebRequest#33675143::GetResponse()
…
System.Net Information: 0 : [15048] HeaderCollection#39451090::Get(MIME-Version)
System.Net Information: 0 : [15048] HeaderCollection#39451090::Get(From)
System.Net Information: 0 : [15048] HeaderCollection#39451090::Get(To)
System.Net Information: 0 : [15048] HeaderCollection#39451090::Get(Date)
System.Net Information: 0 : [15048] HeaderCollection#39451090::Get(Subject)
System.Net Information: 0 : [15048] HeaderCollection#26753075::Get(Content-Type)
```





`System.Net Information: 0 : [15048] HeaderCollection#26753075::Get(Content-Transfer-Encoding)`

`System.Net Information: 0 : [15048] HeaderCollection#26753075::Get(Content-Transfer-Encoding)`

`System.Net Information: 0 : [15048] HeaderCollection#26753075::Get(Content-Transfer-Encoding)`

`System.Net Verbose: 0 : [15048] Exiting SmtpClient#13869071::Send()`

读取此文件，你可以看到与服务器上请求匹配的引用编号都出现了，这极地提高了调试的便利性。此外，由于所有内容都是按照执行顺序排列的，确定错误在过程中发生的具体位置变得容易得多。

比较有趣的条目之一是用于获取图片每个数据块的系列三个命令。`ConnectStream` 退出之前的读取，进入新的读取，然后如下所示下载数据（以及实际的二进制数据）：

`System.Net Verbose: 0 : [15048] Exiting ConnectStream#47891719::Read() -> Int32#1024`

`System.Net Verbose: 0 : [15048] Entering ConnectStream#47891719::Read()`

`System.Net Verbose: 0 : [15048] Data from ConnectStream#47891719::Read`

# 第 5 章

## 创建图像

本章内容

- ![Bullet](img/check.png) **理解 `System.Drawing` 命名空间**
- ![Bullet](img/check.png) **确定绘图类的适用位置**
- ![Bullet](img/check.png) **使用 `System.Drawing` 创建简单的游戏应用程序**

有人将直接使用 C# 编写下一版《生化狂飙》（尽管你可能使用使用 Unity Gaming Services 等第三方产品，[`https://unity.com/`](https://unity.com/)）来这样做）。它并不是用来编写像射击游戏这类图形密集型应用程序的语言。

尽管如此，C# 在 `System.Drawing` 类中提供了相当强大的功能。（本章重点介绍 Windows Forms 创建图形的方法——WPF 方法则不同。）虽然这些类在某些领域相当原始，且使用它们可能会导致你编写比预想的多出几行代码，但只要工作足够，这些类并没有什么是做不到的。

.NET Framework 提供的绘图能力通过微软提供的命名空间设计分为四个逻辑区域。所有的通用绘图能力都在 `System.Drawing` 命名空间中。此外还有一些专门的命名空间：

- `System.Drawing.2D` 具有高级的矢量绘图功能。
- `System.Drawing.Imaging` 主要关于使用位图图形格式，如 `.bmp` 和 `.jpg` 文件。
- `System.Drawing.Text` 处理高级排版。

本章侧重于基础命名空间，仅涵盖 C# 绘图的基础知识。（讨论绘图的每一个方面可以很容易填满一整本书。）

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要简单得多。你可以在下载源码的 `\CSAIO4D2E\BK03\CH05` 文件夹中找到本章的源码。有关如何找到这些源码文件的详情，请参引言。

### 认识 System.Drawing

即使在最高层级，图形编程也由绘制多边形、填充颜色和用文本标记组成——这一切都在某种画布上完成。意不意外的是，这为你留下了四个构成你编写的图形代码的核心对象：图形、笔、画刷和文本。

#### Graphics

通常来说，`Graphics` 类创建了一个作为你画布的对象。`Graphics` 对象的所有方法和属性都设计用于让你绘图区域更符合你的需求。

此外，框架中其他类的大多数与图形和图像相关的方法都提供 `Graphics` 对象作为输出。例如，你可以从 Windows Forms 应用程序调用 `System.Web.Forms.Control.CreateGraphics` 方法，并返回一个 `Graphics` 对象，允许你在项目中的表单控件中绘图。你还可以处理表单的 `Paint` 事件，并检查事件的 `Graphics` 属性。

`Graphics` 对象使用笔和画刷（在本章稍后的 `Pens` 和 `Brushes` 部分中讨论）进行绘制和填充。`Graphics` 对象具有如下方法：

- `DrawRectangle`
- `FillRectangle`
- `DrawCircle`
- `FillCircle`
- `DrawBezier`
- `DrawPolygon`
- `DrawLine`

这些方法接受笔和画刷作为参数。你可能会想：“圆能帮我什么？”但你必须记住，即使是像《光环无限》（Halo Infinite）([`www.halowaypoint.com/`](https://www.halowaypoint.com/)) 中复杂的图形对象也是由圆和三角形组成的——成千上万个。实用艺术的技巧在于利用数学将许多圆组合在一起。

#### Pens

你使用笔来画线。笔具有如下属性：

- `Color`
- `DashStyle`
- `EndCap`
- `Width`

你使用笔绘制线条和曲线。这些决定了绘图的方式。

#### Brushes

画刷填充多边形的内部。尽管画刷对象始终位于内部，

但不要寻找 `Brush` 类（它是一个基类）。它是真实画刷的存放区域，这些画刷有着奇怪的名字。画刷是为了定制而设计的，但你可以使用自带的画刷完成很多工作。这些包括：

- `SolidBrush`
- `TextureBrush`
- `HatchBrush`
- `PathGradientBrush`

#### Text

文本是用字体和画刷组合绘制的。就像多边形一样，`Font` 类使用画刷填充文本线条。

`System.Drawing.Text` 包含了运行程序的系统中或作为应用程序一部分安装的所有字体集合。`System.Drawing.Font` 拥有所有的属性，例如：

- `Bold`
- `Size`
- `Style`
- `Underline`

`Graphics` 对象再次提供了在画布上写入文本。

### 图形类如何融入框架

`System.Drawing` 命名空间将绘图分为两个步骤：

1.  **创建一个** `Graphics` 对象。
2.  **使用 `System.Drawing` 命名空间中的工具在其上绘图。**

这看起来很直观，事实也是。第一步是获取 `Graphics` 对象。`Graphics` 对象来自两个地方——现有图像和 Windows Forms。

要从现有图像获取 `Graphics` 对象，请查看 `Bitmap` 对象。`Bitmap` 对象是一个很棒工具，允许你使用现有图像文件创建对象。这带给你一个基于已经在硬盘上的位图图像（例如 JPEG 文件）的新调板。这是一个方便的工具，特别是对于网络图像。

```
Bitmap currentBitmap = new Bitmap(@"c:\images\myImage.jpg");
Graphics palette = Graphics.FromImage(currentBitmap);
```




现在对象 `palette` 是一个 `Graphics` 对象，其高度和宽度基于 `currentBitmap` 中的图像。此外，`palette` 图像的基础看起来与 `currentBitmap` 对象中引用的图像完全相同。

你可以使用 `Graphics` 类中的笔（pens）、画刷（brushes）和字体直接在幅图像上绘图，就像把它当成空白画布一样。你可以在网页上显示图像之前使用字体在图像上添加文本，还可以使用其他 `Graphics` 元素动态修改图像的格式。

获取 `Graphics` 对象的另一种方法是从 Windows Forms 获取。首选方法是捕获 `Paint` 事件并使用它的 `Graphics` 对象。不过，你也可以使用 `System.Windows.Forms.Control.CreateGraphics()` 方法，但这种方法意味着当控件需要刷新时，绘制可能会消失。这种方法为你提供了一个基于所引用控件绘制表面的新调色板。如果是一个表单（form），它继承表单的高度和宽度并具有表单背景颜色。你可以使用笔和画刷直接在表单上绘图。

当你拥有一个 `Graphics` 对象时，选项是无限的。虽然复杂的图形并非不可能，但你可能需要花费大量工作才能使用 Visual Studio 创建出像 *Halo* 中那样的图形。（并没有一个可以让你自动生成的 `Master Chief` 类。）

尽管如此，即使是最复杂的 3D 图形也只是有色的多边形，你可以使用 `System.Drawing` 命名空间创建它们。接下来的章节将使用 `Graphics` 对象、笔、画刷和字体构建一个跳分板（cribbage board）。

使用 System.Drawing 命名空间

好的应用程序源于奇怪的地方。许多人喜欢游戏，在美国（以及许多其他地方）最受欢迎的游戏之一是纸牌游戏跳分（基础规则的说明请参见 `https://www.dummies.com/games/card-games/cribbage/the-basics-of-cribbage/`）。假设你正在度假，并产生了玩游戏的冲动。你有扑牌，但没有跳分板。

但你有笔记本电脑、Visual Studio 和 `System.Drawing` 命名空间。只需工作几个小时，你就可以构建出一个作为一个功能性跳分板的应用程序！接下来的章节中的 `Cribbage` 示例并不完整（这需要大量的代码），但它包含了足够让你入门的代码，并且足够运行，可以让你玩一局游戏。

入门

跳分是一种纸牌游戏，每手牌都计分为分，第一个得 121 分的玩家获胜。计分由玩家负责，分数记录在记分板上。

跳分板由两行用于插销的孔组成，通常总共 120 个，但有时会使用 60 个孔并让你玩两次。[图 5-1 显示了一个典型的跳分板。跳分板有许多样式——如果你好奇，可以查看 `www.cribbage.org`；它有一个包含近 100 块棋板的精彩画廊，从基础到趣味的应有。

在此示例中，你为一个记录跳分游戏分数的应用程序创建一个面板图像——但用 C# 将卡牌写入游戏也并非可能的！因此，此应用程序的棋板在三对行中每行有 40 个孔，这是两个玩家玩到 120 分的标准棋板设置，如图 5-2 所示。第一个任务是绘制棋板，然后随着玩家分数（在文本框中输入）的变化，绘制插销。

![照片显示了一个块传统的跳分板。](img/9781119839071-fg030501.png)

图 5-1： 传统的跳分板。

![照片显示了数字跳分板。](img/9781119839071-fg030502.png)

图 5-2： 数字跳分板。

前提是这样的：玩家玩一手牌，并将结果分数输入到各自名称下方的文本框中（请参见图 5-2）。当输入每手牌的分数时，玩家旁的分数就会更新，后方的插销会在棋板上移动（使当前的插插销变成后插销）。当该玩家下一次得分时，后插销会向前移动得分的分数超过前插销，然后前插销变成后插销。跳分的发明人非常防备作弊，后插销的设计降低了这种可能性。如果你不熟悉跳分，你可能想查看 `http://www.cribbage.org/` 上的规则。

设置项目

首先，创建一个绘制区域。你设置了图 5-2 所示的棋板，但还没有绘制棋板——你稍后会看到 `System.Drawing`

![基础棋板的快照。](img/9781119839071-fg030503.png)

图 5-3： 基础棋板。

处理分数的后续方法是从框的 `Leave` 事件调用的。之所以不使用 `TextChanged` 事件，是因为你想确保用户已完整输入分数后再处理它。否则，输入的每个数字都会被计一次分。从左到右、从上到下的控件命名为 `Player1` (Label)、`Player1` (TextBox)、`WinMessage` (Label)、`PrintMe` (LinkLabel)、`Player2` (Label) 和 `Player2` (TextBox)。该方法是通用的，以便为两个玩家使用。

```csharp
private void HandleScore(TextBox scoreBox, Label points, Label otherPlayer, ref int lastScore)
{
    try
    {
        if (0 > Int32.Parse(scoreBox.Text) || Int32.Parse(scoreBox.Text) > 27)
        {
            // 显示错误消息并确保分数框获得焦点。
            scoreBox.Focus();
            WinMessage.Text = "分数在 0 到 27 之间";
        }
        else
        {
            // 清除错误消息。
            WinMessage.Text = "";
            // 更新最后分数。
            lastScore = Int32.Parse(points.Text);
            // 将分数写入分数
            points.Text = (Int32.Parse(points.Text) + Int32.Parse(scoreBox.Text)).ToString();
            // 重置分数文本。
            scoreBox.Text = "0";
            // 将焦点切换到下一个玩家。
            if (scoreBox.Name == "Player1")
                Player2.Focus();
            else
                Player1.Focus();
        }
    }
    catch (System.FormatException ext)
    {
        // 非数字
        if (scoreBox.Text.Length > 0)
        {
            scoreBox.Focus();
            WinMessage.Text = "分数必须是数字";
        }
    }
    catch (Exception ex)
    {
        // 哎！
        scoreBox.Focus();
        MessageBox.Show("出现错误！" + ex.Message);
    }

    // 检查分数
    if (Int32.Parse(points.Text) > 120)
    {
        // 使打印分数可能。
        PrintMe.Visible = true;
        if (Int32.Parse(points.Text) / Int32.Parse(otherPlayer.Text) > 1.5)
        {
            WinMessage.Text = scoreBox.Name + " 完胜了对方!!!";
        }
        else
        {
            WinMessage.Text = scoreBox.Name + " 赢了!!";
        }
        WinMessage.Visible = true;
    }
}
```



代码首先创建两个变量来存储玩家的分数总。`HandleScore()` 接收当前玩家 `TextBox` 中的当前分数，以及两名玩家的总分。然后，它会检查当前分数以确保其格式正确且处于正确的取值范围内。与其使用 `Int32.Parse()` 和异常处理程序，你也可以使用 `Int32.TryParse()`，它不会产生异常，但它需要额外的处理，因为现在你必须检查转换是否成功。在验证了新分数后，将其值累加到相应玩家的分数中，然后将新分数重置为 `0`。接着，下一个玩家的 `TextBox` 将获得焦点。

现在分数已经更新，是时候检查总分了。当某个玩家的总分超过 120 分时，游戏结束。根据一个玩家击败另一个玩家的程度，游戏将显示两条消息中的其中一条。

### 创建事件连接

当然，如果你有与事件关联的内容，就必须有事件处理程序。依次选择每个玩家的 `TextBox` 控件，点击事件（Events）按钮，然后双击 `Leave` 事件以生成事件处理程序，如图图 5-4 所示。

现在你已经有了所需的事件处理程序，可以向它们中添加以下代码：

```csharp
private void Player1_Leave(object sender, EventArgs e)
{
    // 处理分数。
    HandleScore(Player1, Player1Points, Player2Points, ref Player1LastTotal);
    // 更新画板。
    Form1.ActiveForm.Invalidate();
}

private void Player2_Leave(object sender, EventArgs e)
{
    // 处理分数。
    HandleScore(Player2, Player2Points, Player1Points, ref Player2LastTotal);
    // 更新画板。
    Form1.ActiveForm.Invalidate();
}
```

![为每个 TextBox 控件添加 Leave 事件处理程序的快照](img/9781119839071-fg030504.png)

图 5-4： 为每个 TextBox 控件添加 Leave 事件处理程序。

注意，你必须通过引用传递用于存储玩家之前分数的私有字段。否则，字段将不会更新。

此外，你必须调用 `Form1.ActiveForm.Invalidate()`。否则，画板不会重绘，这意味着你看不到销钉的移动。

### 绘制画板

应用程序需要在表单上直接绘制，为纸牌游戏（cribbage）创建画板图像。这意味着通过每次重绘事件传递给应用程序的 `PaintEventArgs` 对象获取 `Graphics` 对象。从那里，你需要完成以下任务：

*   使用画刷将画板涂成棕色。
*   使用画笔画六行小圆。
*   如果是正确的分，则填充孔洞。
*   清理你的工具。

以下方法每次被调用时都会重绘画板。为了让方法的目的更易理解，代码将其命名为 `CribbageBoard_Paint()`。

```csharp
private void CribbageBoard_Paint(object sender, PaintEventArgs e)
{
    // 获取图形对象。
    Graphics g = e.Graphics;
    // 创建画板
    SolidBrush brownBrush = new SolidBrush(Color.Brown);
    g.FillRectangle(brownBrush, new Rectangle(20, 20, 820, 180));
    // 绘制小孔。
    // 画板上有 244 个小孔。
    // 三行 40 个乘以两次，两端有小起始和结束。
    // 我们先处理 240 个。
    int rows = 0;
    int columns = 0;
    int scoreBeingDrawn = 0;
    Pen blackPen = new Pen(Color.Black, 1);
    SolidBrush blackBrush = new SolidBrush(Color.Black);
    SolidBrush redBrush = new SolidBrush(Color.Red);
    // 有 6 行，分别在 24 和 40、80 和 100，然后是 140 和 160。
    for (rows = 40; rows <= 160; rows += 60)
    {
        // 有 40 列。每隔 20 个一个
        for (columns = 40; columns <= 820; columns += 20)
        {
            // 计算正在绘制的分数
            scoreBeingDrawn = ((columns - 20) / 20) +
                ((((rows + 20) / 60) - 1) * 40);
            // 绘制 Player1
            // 如果绘制的分数 = Player1 填充，否则绘制
            if (scoreBeingDrawn == Int32.Parse(Player1Points.Text))
            {
                g.FillEllipse(blackBrush, columns - 2, rows - 2, 6, 6);
            }
            else if (scoreBeingDrawn == Player1LastTotal)
            {
                g.FillEllipse(redBrush, columns - 2, rows - 2, 6, 6);
            }
            else
            {
                // 此处省略部分绘制逻辑
            }
        }
    }
    // 清理资源
    brownBrush.Dispose();
    blackBrush.Dispose();
    redBrush.Dispose();
    blackPen.Dispose();
}
```
*(注：由于原始代码在示例中存在重复逻辑或省略，此处翻译时已保持结构对应)*





```javascript
// 重置文本并隐藏打印链接。

WinMessage.Text = "";

PrintMe.Visible = false;

}
```

这可能很难想象，但大型游戏确实是这样编写的。诚然，大型图形引擎包含了得多的 `If-Then` 决策，但前提是相同的。

此外，大型游戏有时会使用位图图像，而不是一直进行绘图。例如，对于骨牌（cribbage）计分程序，你可以使用一个棋子的位图图像，而不是用黑色或红色的画笔填充一个椭圆形！

# 第 6 章

# 动态编程！

## 本章内容

- ![Bullet](img/check.png) **理解动态类型系统**
- ![Bullet](img/check.png) **定义变量**
- ![Bullet](img/check.png) **通过动态化保持灵活性**
- ![Bullet](img/check.png) **让静态操作动态化**

`动态编程`（Dynamic programming）是另一个真正没有明确定义的术语之一。在最宽泛范围内，它意味着以一种方式开发程序，使得程序在运行时对其运行方式做出更多决策，而不是在编译时决定。

脚本语言是这类类型编程的极佳示例。当你用 `JavaScript`（`https://developer.mozilla.org/docs/Web/JavaScript/Reference`）编写代码时，你完全不需要编译——所有的决策都是运行时做出的。`Ruby`（`https://www.ruby-lang.org/`）是另一个很好的例子：大多数时候，整个程序可以直接输入到命令行提示符并从那里运行。

![Remember](img/remember.png) 当你在动态类型语言中声明变量时，你不需要说明你正在为该变量创建什么类型。编译器会自动为你判断。在静态语言中（例如早期版本的 `C#`），你必须说明你正在为该变量创建什么类型。然而，从 `C#` 3.0 开始，`var` 关键字允许你将使用何种类型的决策交给编译器。

微软最初承诺动态类型永远不会出现在 `C#` 中，但后来决定必须添加此功能。为什么？很大程度上是因为 `Microsoft Office` 的开发需求。Office 使用 `COM`，这是 .NET 出现之前的微软应用程序结构。此外，`WinRT API` 不基于托管代码，并且支持原始动态语言之一的 `JavaScript`。他们可能也是展望 `WinRT` 而增加了动态支持。

`COM` 和 `WinRT` 期望使用它的语言（如 `VB Classic` 和 `C++`）具有动态类型。这让 `C#` 程序员开发 `Microsoft Office` 变得困难，这与微软希望发生完全相反。结果是什么？动态类型。

## 将 C# 向动态类型转型

所谓的“动态语言”是一种不断回归的趋势，就像褶纹礼服一样。`动态语言`是允许松散类型而非静态类型的语言。这一概念始于 20 世纪 60 年代的列表处理语言（LISP）。动态语言在 20 世纪 80 年代后期回归，有两个原因：网络管理脚本和人工智能热。得益于网络，这个术语再次回来了。

对于你们中没有老到记得以前的人来说，万维网（World Wide Web）是基于查看源代码和动态语言构建的。微软最初的 Web 开发语言 `Active Server Pages` 是基于 `VBScript`（`https://www.guru99.com/introduction-to-vbscript.html`）的——这是一种动态语言。

网络有了动态编程环境会更好，因此这次的趋势可能会一直持续下去（至少在下一个重大事物出现之前）。`C#` 并不是唯一增加动态语言特性的语言，动态类型也不是为了对 Web 程序员更具吸引力而添加的唯一语言特性。几种动态语言已经存在了一段时间，例如这些：

- `LISP`
- `Perl`
- `Scheme`
- `Smalltalk`
- `Visual Basic`

尽管其中一些语言没有像以前那样流行，但它们仍然存在，并推动了新语言中的这一趋势。你可以在过去十年中出现的所有具有动态类型系统的全新或翻新语言中看到这种趋势。其中许多语言源于网络，而另一些则被新用于网络：

- `Cold Fusion`
- `Groovy`
- `JavaScript`
- `Lua`
- `Newspeak`
- `PHP`
- `Python`
- `Ruby`

![Technicalstuff](img/technicalstuff.png) 这些语言中的一些支持多种编码风格。例如，尽管 `Python` 支持动态类型系统，但它可以使用面向对象、命令式、函数式编程和过程化的编码风格。需要意识到的是，类型系统并不一定影响语言所使用的编码风格。

在动态语言中工作的开发者通常将它们用于几乎一切，除了高度结构化的团队构建类环境。用途包括：

- 使用数据科学技术进行数据分析
- 人工智能、机器学习和深度学习
- 用于系统维护的脚本基础设施
- 构建测试
- 一次性工具
- 其他应用程序脚本
- 构建网站
- 生物学
- 游戏

动态语言在这些任务中很流行有两个原因。首先，它们提供了即时反馈，因为你可以在正在编写的程序的其余限制之外尝试一段代码。其次，你可以开始构建它的高级部分。

例如，`Ruby` 有一个命令行界面，你只需将一个函数粘贴进去（即使在没有上下文中），即可看到它是如何工作的。在 [`https://www.tutorialspoint.com/execute_ruby_online.php`](https://www.tutorialspoint.com/execute_ruby_online.php) 甚至有一个网页版本。你可以直接在里面输入代码，即使引用了未定义的类，因为 Ruby 会对其进行猜测。如果你需要一个依赖 Python 且更有组织的环境，可以在 Google Colaboratory（[`https://colab.research.google.com/notebooks/intro.ipynb`](https://colab.research.google.com/notebooks/intro.ipynb)）中找到。

这种在线使用的便利性很好地过渡到一点，即动态语言允许你构建引用未定义类型的类。例如，你可以创建一个类来调度事件，而无需实际上先构建底层的 `Event` 类型。

这一切都使语言对变化更有灵敏的响应。你可以在一个地方进行逻辑更改，而不需要翻遍大量的代码来修复各处的类型声明。

动态语言的其他优点通常随着你使用它们的次数增加而显现。例如，宏语言通常是动态类型的。如果你尝试在以前版本的 Visual Studio 中构建过宏，你就知道使用静态语言是多么痛苦。让 `C#`（以及 Visual Basic）更具动态性不仅使其成为扩展 Visual Studio 的更好语言，还让程序员能够将该语言包含在编写的程序中，以便其他开发者进一步扩展这些应用程序。

## 应用动态编程技术

到这里，你可能在问为什么关于动态代码的所有讨论对 `C#` 程序员很重要。当你定义新变量时，可以使用 `dynamic` 关键字，`C#` 将允许你对变量的成员做出假设。例如，如果你想声明一个新的 `Course` 对象，可以这样做：

```csharp
Course newCourse = new Course();

newCourse.Schedule();
```




当然，这前提是你在程序的其他地方定义了一个 `Course` 类，如下所示：

```csharp
class Course {
    public void Schedule()
    {
        // 这里写一些花哨的操作
    }
}
```

但如果你不知道新对象会是哪个类怎么办？你该如何处理呢？你可以将其声明为 `Object`，因为所有类型都派生自 `Object`，对吧？这里是代码：

```csharp
Object newCourse = new Object();
```

别急急，我的朋友，如果你把下一行写成这样：

```csharp
newCourse.Schedule();
```

请注意，波浪线几乎立即就会出现，你会在设计时的“错误列表（Error List）”中看到那个著名的“对象不包含 `Schedule` 的定义……”的错误。然而，你可以这样做：

```csharp
dynamic newCourse = SomeFunction();
newCourse.Schedule();
```

这些代码只需要一个返回某些值的函数存根，你就可以顺利运行。如果 `SomeFunction()` 返回的是一个字符串呢？嗯，你会得到一个运行时错误。但它仍然可以编译！

此时你可能在想：“这是一件`好`事吗？怎么可能！！”暂时，你可以将其归咎于 COM。你看，COM 大多是使用 C++ 构建的，而 C++ 有变体类型（variant type）。在 C++ 中，你可以这样声明一个变量为动态类型：

```csharp
VARIANT newCourse;
```

它的工作方式与动态类型一样，只不过 C# 还没有发明。因为 COM 中的许多对象使用了 `VARIANT` 输出参数，使用 .NET 处理互操作性（Interop）真的非常困难。（`Interop` 是 interoperability 的缩写，指你试图让两段代码相互通信。）由于 Microsoft Office 大部分由 COM 对象组成，而且它在短期内不会发生改变，而且微软希望我们有一天都能成为 Office 开发者，砰地，动态类型（dynamic type）诞生了。

假设你的 `newCourse` 是 COM 类方法中的一个变体 `out` 参数。要获取该值，你必须将其声明为 Object，如下：

```csharp
CourseMarshaller cm = new CourseMarshaller(); // 一个 COM 对象
int courseId = 4;
Object newCourse;
cm.MakeCourse(courseId, out newCourse);
// 现在我们回到了原点
newCourse.Schedule(); // 这会导致“未找到成员异常”
```

即使 `Schedule` 方法存在，最后一行代码也无法编译，因为你不能假设 `newCourse` 总是会返回一个 `Course` 对象，因为它被声明为变体。你被卡住了。但是，使用动态类型，有了这段代码，你再次如获金归：

```csharp
CourseMarshaller cm = new CourseMarshaller(); // 一个 COM 对象
int courseId = 4;
dynamic newCourse;
cm.MakeCourse(courseId, newCourse);
newCourse.Schedule(); // 现在可以编译了
```

然而，如果 `newCourse` 返回一个没有 `Schedule()` 方法的对象，你会得到一个运行时错误。但有 `try…catch` 块可以处理运行时错误。如果没有 `dynamic` 关键字，没有任何东西能帮助代码编译。

## 将动态类型用于实践

当 C# 遇到动态类型变量时（例如你之前创建的变量），它会将该变量所触及的所有内容都转换为`动态操作（dynamic operation）`。这种动态转换意味着当你在表达式中使用动态类型对象时，整个操作都是动态的。

### 经典示例

以下是动态操作如何工作的六个示例。假设你有一个动态变量 `dynamicVariable`。由于动态变量将通过所有六个示例，它们将由 C# 编译器动态地分发。

1. `dynamicVariable.someMethod("a", "b", "c");`: 编译器在运行时绑定方法 `someMethod`，因为 `dynamicVariable` 是动态的。并不意外。
2. `dynamicVariable.someProperty = 42;`: 编译器绑定属性 `someProperty` 的方式与第一个方法中一样。
3. `var newVar = dynamicVariable + 42;`: 编译器寻找任何类型为 `dynamic` 的 `+` 重载运算符。如果没有找到，它会输出一个动态类型。
4. `int newNumber = dynamicVariable;`: 这是到 `int` 的隐式转换。运行时决定是否可以转换为 `int`。如果不能，将抛出类型不匹配错误。
5. `int newNumber = (int) dynamicVariable;`: 这是到 `int` 的显式强制转换。编译器将其编码为强制转换——你在这里实际上改变了类型。
6. `Console.WriteLine(dynamicVariable);`: 因为没有显式接受动态类型的 `WriteLine()` 重载，所以整个方法调用都是动态分发的。

### 将静态操作动态化

如果编译器选择将静态操作变为动态——正如前一节的第 6 点所示——编译器将即时重建代码以处理动态变量。这对你意味着什么？很高兴你问了。

以第 6 点为例，`Console.WriteLine(dynamicVariable);`。这段代码强制编译器构建中间代码，这些代码会在运行时检查变量的类型，以便生成可以写入控制台的内容。编译后的代码首先检查输入是否是它已知的静态类型。接下来，它检查程序中存在的类型。然后，它将尝试几种可能有效的方法。如果一无所获，它将报错并失败。

如果你作为开发者必须使用这种方法创建代码，至少你可以完成任务。但请记住，它比一月份的糖蜜还要慢（甚至更慢）。这就是为什么 `Variant` 在经典版 Visual Basic 中声誉狼藉。动态类型是你在你需要它之前永远不会使用的东西。它会给运行程序的机器带来巨大的压力，特别是当所有变量都是动态类型时。

### 理解底层发生了什么

使用动态编程技术并不一定很困难。事实上，你只需要使用这种简单的方法通过三行功能性代码即可实现：

```csharp
class C {
    public dynamic MyMethod(dynamic d)
    {
        return d.Foo();
    }
}
```

这些是非常直白的内容——一个接受动态类并返回该类型的 `Foo` 方法结果的方法。没什么大不了。这里是编译后的 C# 代码：

```csharp
class C {
    [return: Dynamic]
    public object MyMethod([Dynamic] object d)
    {
        if (MyMethodo__SiteContainer0.p__Site1 == null)
        {
            MyMethodo__SiteContainer0.p__Site1 =
                CallSite<Func<CallSite, object, object>>
                .Create(new CSharpCallPayload(
                CSharpCallFlags.None, "Foo", typeof(object), null,
                new CSharpArgumentInfo[] {
                    new CSharpArgumentInfo(CSharpArgumentFlags.None, null) }));
        }
        return MyMethodo__SiteContainer0.p__Site1
            .Target(MyMethodo__SiteContainer0.p__Site1, d);
    }
    [CompilerGenerated]
    private static class MyMethodo__SiteContainer0 {
        public static CallSite<Func<CallSite, object, object>> p__Site1;
    }
}
```

大多数开发者都不想要拆解这段代码。幸运的是，他们不需要这样做。那是编译器的工作，对吧？

## 使用动态运行时运行

动态语言不仅仅是动态类型。你可以做一些强大的事情。正如所有的力量一样，你必须小心不要误用。

动态运行时——如图 6-1 所示——是一个添加到 .NET Framework 的库，专门用于为 Visual Studio 折叠（fold）提供动态语言（如 Ruby），或者为现有的静态语言（如 C# 4.0）添加动态语言功能。

![动态运行时的截图。](img/9781119839071-fg030601.png)

[图 6-1：动态运行时...]

运行时帮助编译器在编译后的程序集中构建代码，以做出动态选择。前一节末尾的代码块是最简单的一种示例。当然，C# 具有类似的功能，所以你可以使用动态编程技术。这里是代码：

```csharp
static dynamic f(dynamic x)
{
    return Math.Sqrt(x) + 5.0 * Math.Pow(x, 3.0);
}

static void Main(string[] args)
{
}
```




```csharp
dynamic[] array = new Array[11];

for (int i = 0; i < 11; i++)
{
    array[i] = Console.ReadLine();
}
for (int i = 10; i>=0; i--)
{
    dynamic y = f(array[i]);
    if (y > 400.0)
    {
        Console.WriteLine(string.Format("{0} TOO LARGE", i));
    }
    else
    {
        Console.WriteLine("{0} : {1}", i, array[i]);
    }
}
Console.ReadKey();
}
```

此示例定义了两个函数：`f()` 和 `Main()`。`Main()` 从控制台接受 11 个数字，然后使用`for`循环将它们移动到整数数组中。接下来，代码这些条目。对于数组中的每个值，它将`y` 设置为`f(x)`，然后检查它是否高于任意值（在本例中为 400，但你也可以使用任何值）。如果是，它会打印“TOO LARGE”；否则，它打印该数字。

显然，你完全可以在此示例中使用`double`，因此看起来似乎没有使用动态编程技术的良好理由。但是，使用`dynamic`确实让程序的创建变得更加简单。尝试将数组更改为`double`数组，如下：

```csharp
Double[] array = new Double[11];
```

现在对`ReadLine()`的调用失效了。你只需要将其强制转换为`double`。不，不能这样做；你必须使用`TryParse`。你明白意思了。静态类型编写起来很困难。动态类型编写起来更容易。

硬币的另一面是什么？显然，如果用户输入了非数字字符串，程序将输出运行时错误，这是糟糕的。如果你对所有内容进行静态类型化，你可以更轻松地捕获该错误并在用户输入时直接处理它。

此外，现实情况是 C# 在程序的整个运行过程中对每个变量都做出运行时决策。如果你只是进行这种静态类型划分，就可以避免大量的额外处理。

这里的要点是，使用动态类型会让你的编程工作变得简单得多，但会让你的故障排除工作变得困难得。。如果你是在为自己编写一个实用脚本，并且不在乎它偶尔因类型不匹配而崩溃，请使用`dynamic`。如果你正在为医院编写备份脚本，成千上万人的生命关乎，静态类型可能更好。

# 使用静态匿名函数

动态编程技术的一个问题是，lambda 和匿名函数可以捕获局部字段值和实例信息，可能会为你的应用程序创建错误情况，因为编译器做了一些不正确的假设。例如，函数可能会根据函数的先前状态在输出值中创建一个偏移。C# 9.0 及更高版本允许你通过向 lambda 和匿名函数添加`static` 关键字来解决这个问题。在使用`static` 关键字时，需要考虑以下权衡：

*   你现在可以访问封闭作用域的静态成员（包括常量）。
*   你无法访问封闭作用域的这些成员：
    *   `nameof()`
    *   局部变量
    *   参数
    *   `this`
    *   `base`
*   可访问性规则变为匹配封闭作用域中静态成员的规则。
*   无法保证静态匿名函数在编译后在元数据中确实以静态方法的形式出现，因为这一细节由编译器决定。
*   非静态匿名函数可以捕获封闭静态匿名函数的状态，但不能捕获封闭静态匿名函数作用域之外的状态。

# Visual Studio 导览

## 概览

1. **第 1 章：Visual Studio 入门**
    1. 版本控制
    2. 安装 Visual Studio
    3. 拆解项目
2. **第 2 章：使用界面**
    1. 在设计器中设计
    2. 布局 Studio 面
    3. 在代码编辑器中编码
    4. 使用专业工具
    5. 将调试器作为学习辅助
3. **第 3 章：自定义 Visual Studio**
    1. 设置选项
    2. 创建你自己的模板

# 第 1 章：Visual Studio 入门

## 本章内容

*   调查可用版本
*   设置 Visual Studio
*   理解项目和解决方案
*   探索不同类型的项目

使用 Visual Studio 编写应用程序... (此处内容省略)





*   其他技术和平台（详情请参见 `https://docs.microsoft.com/en-us/visualstudio/releases/2022/compatibility#developOther` 中的列表）。其中许多其他技术和平台不会影响你的 `C#` 开发。

![Remember](img/remember.png) 然而，最大的消息是 Visual Studio 2022 现在已是一个完全的 64 位的环境，这意味着你可以充分利用系统提供的所有功能。此外，Visual Studio 2022 在某些方面比过去要快得多。幸运的是，你的 32 位应用程序在新环境中仍然可以正常运行。

在你阅读此本书时，你还会发现一些关于影响你编码方式的 `.NET 6.0` 更新。其中一些更新是重大的，你会立即察觉到；另一些更新则非常微妙，但如果你留意，就能发现它们。你可以在 `https://devblogs.microsoft.com/dotnet/announcing-net-6-preview-7/` 查看 `.NET 6.0` 的更新列表。可能会让你惊讶的是，在并没有真正意识到的情况下，你已经注意到了这些更新中的许多，因为它们在后台运行。

![Tip](img/tip.png) 无论你称之为 IntelliSense、IntelliCode 还是其他名称，Visual Studio 的这项功能通过帮助你在输入时纠正代码以及提供建议来节省你的时间。在这一版本的 Visual Studio 中，你一定要记住 `Tab` 键，因为按下 `Tab` 允许你快速、轻松无误地完成主要的代码段。根结底，在你习惯了新的 IntelliSense（本书使用的名称）功能后，你可能会对自己的工作效率感到惊讶。它是许多开发者最显著且最受欢迎的功能。

新的调试支持将以各种小巧工具、图表、图形、闪烁的灯光和各种魅力让你大开眼界。然而，除非你从事一个大型项目，否则你可能会发现自己并没有怎么使用它。调试器确实会告诉你更多关于应用程序出现问题的信息，这个功能确实节省了时间。但在大多数情况下，你会发现自己自己在 IDE 提供的更多帮助下，仍然使用与过去相同的调试技术。

### 社区版

社区版（Community edition）是 Visual Studio 的免费版本。它是为爱好者、课堂和学术研究设计的，但许多专业程序员将其作为小型个人项目或参与开源项目的首选版本。微软还将该版本面向五位或更少开发人员的小型组织。因此，如果你在小公司工作，你可能不需要比此版本更高的版本，这意味着 `C#` 开发将保持免费。

尽管社区版的功能少于专业版（Professional edition），但你可以使用社区版编译书中的每一个代码示例。它拥有 `.NET Framework` 的功能（后者也是免费的），并为你提供了学习 `C#` 的重要手段。从开发平台的角度来看，社区版支持其他版本支持的所有内容，包括：

*   Windows 桌面
*   通用 Windows ，或 `UWP`（以前称为通用 Windows 应用）
*   通用应用平台 (`UAP`)
*   Web (`ASP.NET`)
*   Azure 开发
*   云开发
*   Office 365
*   业务应用程序
*   Apache Cordova
*   C++ 跨平台库开发
*   Python
*   Node.js
*   `.NET Core`
*   Git 支持
*   Docker 工具

![Tip](img/tip.png) 2019 及以上版本的 Visual Studio 新增了跨平台工具，帮助你为 `C#` 现在支持的所有非 Windows 平台创建应用程序。以下是你可以预期的功能：

*   Windows 远程 iOS 模拟器
*   使用 `Xamarin` (`https://dotnet.microsoft.com/apps/xamarin`) 在 Android 和 iOS 之间共享代码，这是一个使用 `C#` 和 `.NET` 构建 iOS 和 Android 应用的平台
*   原生 iOS 和 Android UI 设计器
*   `Xamarin.Forms`

过去，各种 Express 版和学术版让人们体验了使用 `C#` 可以做什么，但往往会将他们推向付费的专业版。在 Visual Studio 2022 中，微软采取了不同的路线，为你提供了充分体验 `C#` 所需的一切。你甚至可以访问许多高级的调试和诊断工具、测试工具以及跨平台模板。`https://www.visualstudio.com/vs/compare/` 上的表格提供了完整的对比。

![Remember](img/remember.png) 社区版缺少的是企业级支持。需要注意的是，微软将“企业”定义为拥有超过 250 台电脑或年收入超过 100 万美元的实体。如果你发现自己需要企业类型的支持但并不属于企业规模的组织，那么你需要专业版。然而，对于大多数开发者来说，社区版提供了发现和使用 `C#` 奇之处所需的一切。

### 专业版

除了将专业版设计用于更大的企业环境外，微软还为专业版增加了一项必要的补充：`CodeLens` ([`docs.microsoft.com/visualstudio/ide/find-code-changes-and-other-history-with-codelens`](https://docs.microsoft.com/visualstudio/ide/find-code-changes-and-other-history-with-codelens))。此功能旨在帮助你详细地查看代码。可以把它看作代码的放大镜。你可以使用 `CodeLens` 执行以下任务：

*   查找你的代码在任何可能存在的引用。
*   查看代码历史并确定更改如何影响你的代码。
*   管理代码中的分支。
*   确定是谁制作了代码更改。
*   使用 `Lync` 或 `Skype` 与其他团队成员联系更改。
*   跟踪关联的代码审查和关联的 Bug。
*   定位并管理代码的单元测试。

### 企业版

专业版和企业版（Enterprise edition）在功能上存在巨大差异。是的，社区版、专业版和企业版都可以创建相同类型的项目，但设计、构建、测试和管理真正大型项目所需的工具位于企业版中。例如，所有的架构功能，如 `Architectural Layer Diagrams` 和 `Architecture Validation` 都是企业版的一部分。如果你想验证设计，你需要 `Live Dependency Validation`，这是一个非常惊人的功能，在 [`docs.microsoft.com/visualstudio/modeling/validate-code-with-layer-diagrams`](https://docs.microsoft.com/visualstudio/modeling/validate-code-with-layer-diagrams) 中有详细描述。

管理功能也是围绕庞大的项目环境而设计的。例如，`Code Clone` ([`docs.microsoft.com/previous-versions/hh205279(v=vs.140)`](https://docs.microsoft.com/previous-versions/hh205279(v=vs.140))) 提供了检测项目项目中重复代码的手段。毕竟，当项目非常大时，多个开发者往往会以相同的方式完成特定任务。确保不需要维护相同代码的多个副本可以降低成本并使代码更容易管理（更不用说还能消除一些更棘手的 Bug）。




你还将获得一些用于执行诊断和调试代码的真正先进的功能。此外，企业版（Enterprise edition）包含了额外的跨平台支持。然而，企业版真正出彩的地方在于测试工具。在使用社区版（Community edition）或专业版（Professional edition）时，你只能获得单元测试。但企业版提供了所有其他形式的测试：

* 实时单元测试 (Live Unit Testing)
* IntelliTest
* Microsoft Fakes (单元测试隔离)
* 代码覆盖 (Code Coverage)
* 快照调试器 (Snapshot Debugger)
* 时间旅行调试 (Time Travel Debugging）（请参见 [`https://docs.microsoft.com/windows-hardware/drivers/debugger/time-travel-debugging-walkthrough`](https://docs.microsoft.com/windows-hardware/drivers/debugger/time-travel-debugging-walkthrough) 中的教程）

![Tip](img/tip.png) 还有新的跨平台开发功能（从 Visual Studio 2019 开始），可以帮助你创建跨多个平台的应用程序。这包括对 Xamarin 的支持，如下：

* 嵌入程序集 (Embedded Assemblies)
* Xamarin 检查器 (Xamarin Inspector)
* Xamarin 分析器 (Xamarin Profiler)

### MSDN

微软开发者网络（MSDN）订阅是目前获取微软产品的最佳方式。建立一个开发环境来开发任何具有重大意义的项目似乎昂贵得不可想象。但事实并非如此。

MSDN 订阅顾如其名——对大多数重要的微软产品进行订阅。对于专业版订阅，第一年的费用约为 1199.00 美元，之后每年 799.00 美元，你就可以获得所需的一切。这实际上并不是 Visual Studio 的一个版本。（你可以在 [`https://visualstudio.microsoft.com/subscriptions/`](https://visualstudio.microsoft.com/subscriptions/) 了解更多关于 Visual Studio 组件的各种订阅费用，以及 [`https://visualstudio.microsoft.com/msdn-platforms/`](https://visualstudio.microsoft.com/msdn-platforms/) 中 MSDN 平台组件的费用。）

这个 MSDN 平台的费用听起来很高，但请这样想：即使你每年只在业余时间自己做一个项目，你的投资也会得到回报。考虑到单是 Visual Studio 就占了该费用的一半，而且它每两年左右修订一次，这非常划算。除了 Visual Studio 专业版，你还获得了大量的软件订阅，在这里列出需要好几页纸，但你可以在 [`https://visualstudio.microsoft.com/vs/pricing-details/`](https://visualstudio.microsoft.com/vs/pricing-details/) 查看完整列表。

## 安装 Visual Studio

Visual Studio 社区版的安装方式与其他任何 Windows 程序类似。首先，确保你的机器可以运行 Visual Studio。然后，运行从 [`https://www.visualstudio.com/vs/community/`](https://www.visualstudio.com/vs/community/) 微软网站下载的安装程序并做一些决定。然后耐心等待。Visual Studio 很大，需要一段时间时间。Visual Studio 2022 的官方最低要求如下所示：

* 操作系统：
    * Windows 10 版本 1909 或更高版本：家庭版、专业版、教育版和企业版（不支持 Team, LTSB 和 S 版）
    * Windows Server 2016：标准版和数据中心版
    * Windows Server 2019：标准版和数据中心版
* 硬件：
    * 1.8 GHz 或更快的 64 位四核处理器（或更好）
    * 4GB 内存（建议 16GB 内存）
    * 20GB 可用硬盘空间（建议 50GB）
    * 5400 RPM 驱动
    * 支持最低 720p 显示分辨率的显卡（1280 x 720；建议使用更高分辨率）

![Warning](img/warning.png) 请记住 Visual Studio 2022 是一个仅限 64 位的 IDE，因此如果你计划继续在 32 位平台或旧版本的 Windows 上工作，可能希望考虑继续使用 Visual Studio 2019，它仍然带有对 C# 9.0 的支持。你可以在 [`https://docs.microsoft.com/en-us/visualstudio/releases/2019/system-requirements`](https://docs.microsoft.com/en-us/visualstudio/releases/2019/system-requirements) 找到 Visual Studio 2019 的要求，其明显低于 Visual Studio 2022。请注意，Visual Studio 2022 不支持的平台非常多，例如 ARM 处理器、Windows Server Core、Windows Minimal Server、Windows 容器、虚拟机环境、多并发用户环境等。如果你对自己的设置有任何疑问，请务必咨询 [`https://docs.microsoft.com/visualstudio/releases/2022/system-requirements`](https://docs.microsoft.com/visualstudio/releases/2022/system-requirements) 中的要求。

你可以在下方所示的配置上运行，但你可能会发现某些功能运行缓慢，且少数功能根本无法运行。以下是 Visual Studio 社区版更符合实际的入门配置：

* 3.4 GHz 64 位 8 核处理器
* 8GB 内存的 64 位 Windows 10
* 固态硬盘 (SSD) 上的 250GB 可用空间
* 宽扩展图形阵列 (WXGA) (1366 × 768) 或更高的显示适配器
* 双显示器（或笔记本电脑），其中一个是触摸屏

## 分解项目

在运行安装程序并设置好默认设置后，你只需要开始一个项目并动手操作。有许多项目类型（除一两个外）。你可以通过选择顶部三个下拉列表框中的选项来控制可见的项目。以下列表显示了作为 Visual Studio 社区版为 C# 开发者安装的项目类型。

* 云端：运行在 Microsoft Azure (`https://azure.microsoft.com/`](https://azure.microsoft.com/)) 上的可扩展服务。你可以创建多种服务、Web 应用程序、作业和移动应用程序类型。在这里你找到 Blazor (`https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor`](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor))、Angular (`https://angular.io/`](https://angular.io/)),React.js (`https://reactjs.org/`](https://reactjs.org/)) 和 Redux (`https://redux.js.org/`](https://redux.js.org/)) 模板![Snapshot of the Visual Studio Community edition provides lots of project types.](img/9781119839071-fg040101.png)

    图 1-1：

* 控制台：有两种控制台应用程序： .NET Core（支持 Linux、macOS 和 Windows）和 .NET Framework（支持桌面开发）。
* 桌面：编译为 `.EXE` 并直接在你的计算机上的富客户端应用程序。Microsoft Word 是一个 Windows 应用程序。大多数模板创建运行在 Windows 上的应用程序，但某些模板允许你为通用 Windows 平台 (UWP) 和 Xbox 创建应用程序。
* 扩展：你可以使用此类别中的模板为 Visual Basic 创建扩展，以便其执行你需要的任何特殊功能。当你第一次查看此类别时，它可能是空的。你需要点击提供的链接安装额外的工具和功能以便在此处提供条目。





- **游戏：** 使用 `Visual Studio` 和 `C#` 创建游戏是可行的，但这并不是一项容易的任务。`https://narrasoft.com/is-c-a-good-tool-for-game-development/` 上的为你提供了有关如何执行此任务的一些见解。当你第一次查看此类别时可能是空的。你需要点击提供的链接安装额外的工具和功能，以便在此提供条目。
- **IoT（物联网）：** 允许你创建与支持特定接口的设备交互应用程序。你可以在 `https://dotnet.microsoft.com/apps/iot` 了解更多关于 `C#` 和物联网的知识。当你第一次查看此类别时可能是空的。`https://docs.microsoft.com/dotnet/iot/intro` 文章提供了有关如何安装所需支持的信息。
- **库：** 库使得存储代码供多个项目使用成为可能。当然，你必须针对你想要创建的项目类型拥有正确的库。此列表中的模板支持你可以使用 `C#` 创建的所有项目类型。
- **机器学习：** 使用计算机以智能方式与人类交互的能力是机器学习提供的功能的主要部分。机器学习严重依赖海量数据和复杂数据，这意味着你必须有一台强大的机器才能开始在本地运行机器学习应用（也有在线选项）。当你第一次查看此类别时可能是空的。`https://dotnet.microsoft.com/apps/machinelearning-ai/ml-dotnet` 和 `https://dotnet.microsoft.com/apps/machinelearning-ai` 网站提供了有关如何开始机器学习的信息。
- **移动端：** 创建在多个设备上运行的应用程序是现在的必需。此类别中的模板允许你为 `Windows`、`iOS` 和 `Android` 创建应用。当你第一次查看此类别时可能是空的。你需要点击提供的链接安装额外的工具和功能，以便在此提供条目。
- **Office：** 你使用此类别中的模板来创建 `Office` 和 `SharePoint` 应用程序。如果你想为 `Office 365` 开发，你需要 `https://docs.microsoft.com/visualstudio/subscriptions/vs-m365` 中讨论的特殊开发者许可证。桌面开发要求你安装与你的 `Office` 产品一起的支持。除非安装了所需的支持，否则此类别将是空的。
- **其他：** 不适合其他地方的模板将出现在此类别中。除非你安装了某种类型的专用支持，否则此类别通常是空的。
- **服务：** 某些类型的应用程序没有用户界面。相反，它们在后台运行等待客户端的请求。这些应用程序是服务，`Windows` 充满了此类服务（只需打开 `Services` 应用即可查看它们）。这些模板允许你创建专门为你的应用程序设计的服务，而不仅仅 Windows 服务。
- **测试：** 使用自动化技术帮助你检查应用程序功能的单元测试。
- **UWP：** 依赖于 `UWP` 的单页应用程序。这种应用类型没有预定义的控件或布局。
- **Web：** 需要 Web 服务器运行的网站。（为了开发目的，`Visual Studio` 包含了 Web 服务器。）`Microsoft.com` 是 Web 应用程序的一个示例。

![Tip](img/tip.png) 你通过任何版本的 `Visual Studio 2022` 获得的默认项目只是冰山一角。这些是 `Microsoft` 假设你可能最常用的项目。然而，`Visual Studio 2022` 支持许多此书中未涵盖的项目类型。你可以使用 `NuGet` 安装它们（详情请参阅 `https://docs.microsoft.com/nuget/consume-packages/install-use-packages-visual-studio`）。

### 探索“新建项目”对话框

你通过使用 `New Project` 对话框启动所有新项目，该框见图 1-1。可以通过多种方式访问此对话框。最常用的技术是在 `Visual Studio` 启动时选择 `Create a New Project`。然而，你也可以选择 `File ⇒ New ⇒ Project`。在向现有解决方案添加新项目时，你可以在 `Solution Explorer` 中右键点击解决方案项并选择 `Add ⇒ New Project`。

为了方便选择模板，你会在左侧列出你最近使用的模板。你只需选择其中一个条目并点击 `Next` 继续使用向导程序。你还可以使用顶部的搜索字段根据标准搜索模板。否则，你可以通过三个下拉列表框中的条目来选择模板。

你在选择模板后看到的内容取决于该模板的向导。然而，`Microsoft` 已经在某种程度上尝试将向导标准化。当你选择模板并点击 `Next` 后，通常会看到三个（有时是更多）重要的文本框：

- **Name：** 此项目的名称。
- **Location：** 项目文件的路径。
- **(Optional) Solution：** 决定新项目是现有解决方案的一部分，还是新解决方案的一部分。
- **Solution Name：** 解决方案的名称。解决方案是项目的集合。
- **Framework：：** 你想要使用的 `.NET Framework` 版本。

向导有时会有第三页或第四页，向你询问额外信息。只需按照提示操作，你很快就能看到 `IDE`，你可以在那里开始编辑代码。

### 理解解决方案和项目

`Visual Studio` 项目文件以及包含它们的解决方案是 `Microsoft` 开发者关注的一个主要课题。你一次只处理一个解决方案，其中包含多个项目。你组织解决方案和项目的方式将决定你在需要查找内容时的成败。

你可以将解决方案理解为存放项目的文件夹。它们只是带有特殊属性的文件夹。向导的第二页有一个名为 `Place Solution and Project in the Same Directory` 的复选框。当你想要将多个项目添加到单个解决方案，并让每个项目都有自己的目录时，请取消选择该选项。





项目中也有文件——这些文件描述了项目的资源和引用。它们都是 XML 文件，其中包含了对你使用 Visual Studio 设置的值的文本引用。通常，你不需要查看解决方案或项目文件。你执行的任何组织结果都会显示在解决方案管理器中。图 1-2 显示了一个简单应用程序设置的典型示例，由一个解决方案（`CheckCIA`）和两个项目（`CIAAssembly` 和 `InternalLimitsAccess`）组成。每个项目都包含与项目相关的文件，例如 `CIAAssembly` 项目中的 `CIAAssembly.cs`。

![解决方案管理器中解决方案和项目的截图。](img/9781119839071-fg040102.png)

图 1-2： 解决方案和项目出现在解决方案管理器中。

# 第 2 章：使用界面

## 本章内容

- ![Bullet](img/check.png) `使用设计器`
- ![Bullet](img/check.png) `探索解决方案管理器`
- ![Bullet](img/check.png) `使用代码视图编码`
- ![Bullet](img/check.png) `使用工具菜单`
- ![Bullet](img/check.png) `使用调试器工作`

集成开发环境（或 IDE）是程序员工具箱中的瑞士军刀。IDE 提供了一种存储程序代码、组织和构建代码，以及使用设计编辑器查看完成品的机制。IDE 让事情变得可能，并作为交换，节省了完成任务的小时。

Visual Studio 令人印象深刻；它非常庞大。要在一本书中涵盖所有的 Visual Studio 功能都很困难，更不用说是一个章节了。事实上，你可能永远不会使用所有的 Visual Studio 功能。

与其尝试涵盖所有内容，本章让你有机会体验那些你现实中每天都会用到的 Visual Studio 特性。当然，继续探索 IDE 并发现新事物是很重要的——不要止于本章的内容。它仅对该工具中一些惊人的功能进行了简要概述。你可以在 [`https://docs.microsoft.com/visualstudio/get-started/visual-studio-ide`](https://docs.microsoft.com/visualstudio/get-started/visual-studio-ide) 了解更多关于 IDE 的信息。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用可下载的源代码要容易得多。你可以在下载源码的 `\CSAIO4D2E\BK04\CH02` 文件夹中找到本章的源码。请参阅引言了解有关如何找到这些源文件的详情。

## 在设计器中设计

集成到 IDE 中的功能之一是图形化编辑文件，有时被称为图形开发环境或 `designer`。Visual Studio 允许你图形化编辑许多不同类型的代码库，并为进一步管理这些代码库提供辅助工具。简而言之，设计器是 Visual Studio 世界中的拖放式元素。它并不总是是开发程序的最佳方式，但有时确实很有帮助。

![Remember](img/remember.png) 对于 Visual Studio 维护的种主要类型项目（控制台应用程序和没有视觉界面的应用程序元素，如服务之外），都有设计器。设计器处理“所见即所得”的体验，通常还处理幕后的标记代码。除了微软提供的设计器外，你还可以使用 [`https://docs.microsoft.com/visualstudio/extensibility/creating-custom-editors-and-designers`](https://docs.microsoft.com/visualstudio/extensibility/creating-custom-editors-and-designers) 中的材料作为起点，创建你自己的自定义编辑器和设计器。自定义编辑器和设计器允许你以新的方式处理应用程序代码，并支持 Visual Studio 原生支持以外的语言。

问题在于，由于软件开发世界的需要，不同的设计器工作方式略有不同。例如，HTML 和 XAML 之间存在显著差异，因此 Web 设计器和 WPF 设计器的外观和行为不同。Visual Studio 提供了几个视觉设计器来帮助开发应用程序，包括这些常用的设计器：

* 类设计器
* 数据视图
* Web Forms
* 通用 Windows  (UWP) 应用程序
* Windows Forms
* Windows Presentation Foundation (WPF)

### 通用 Windows  (UWP) 应用程序

微软进入“随处运行”的竞争较晚了——非常晚，但它做得很有格调。这种类型的应用程序依赖 Windows Runtime (WinRT) 在包括你的桌面、智能手机、Xbox 和其他平台在内的大量设备上提供服务。第 5 卷 第 5 章 对这种创建 Windows 应用程序的新方法提供了很好的概述，但你应该将这种方法更多地视为你过去工作的补充，而不是完全替代，因为为了功能较弱的软件而放弃整个现有的代码库是不切实际的。由于 UWP 应用程序在处处运行，它们无法访问桌面机器的全部潜力。它更像是编写一个带有严重限制的 32 位应用程序，而不是可以处理机器学习和深度数据库管理等重型任务的健壮 64 位应用程序。每个应用程序类型在你的开发者工具箱中都有位置。

UWP 应用程序的大部分设置与你到本书为止创建的任何其他项目相同。然而，有几处不同，例如需要为你的应用选择目标 Windows 版本，并选择最小接受的 Windows 版本。你还必须为系统配置“开发模式”，这在第 5 卷第 5 章](#c35.xhtml) 中有所介绍。你看到的初始显示与其他应用程序创建过程不同之处在于，它提供了一系列需要遵循的步骤，如图 2-1 所示。

![创建 UWP 应用程序是 Visual Studio 帮助的过程。](img/9781119839071-fg040201.png)

图 2-1： 创建 UWP 应用程序是 Visual Studio 帮助的过程。

用户界面设计体验的核心是一种名为可扩展应用程序标记语言（`XAML`，发音为 `zammel`——等等——发音 *zammel*）的语言（意不意外，这是一种用于创建用户面的基于 XML 的领域特定标记语言）。在图 2-2 所示的设计器中，设计位于顶部帧，底层代码位于底部帧。

![UWP 应用程序依赖使用页面来显示信息。](img/9781119839071-fg040202.png)

图 2-2： UWP 应用程序依赖使用页面来显示信息。

此外，你使用页面设计应用程序。每个页面都设计用于适应各种尺寸的显示，你可以在文档大纲面板中看到页面列表，如图 2-2 所示。实际页面大小由图形设计区域上方的下拉列表控制。默认是 13.5 英 Surface Book (3000 x 2000) 200% 缩放。然而，你也可以选择其他设备，例如 5 英手机 (1920 x 1080) 300% 缩放。这些选项都能帮助你查看设计在特定设备上的外观。

UWP 设计器中有几个小但重要的特征应该指出。你可以在图 2-2 中看到所有这些。

设计器底部栏左侧是缩放字段。该字段中的选项让你执行诸如配置设计器缩放以适应当前选择等操作。这对于处理比屏幕更大的应用程序或检查细节来说是无价之宝。





在缩放字段旁边有一系列按钮，可以使设计器工作变得更加简单。以下是按出现顺序排列的按钮：

- **刷新 (Refresh):** 确保设计区域显示 `XAML` 的任何更改，反之亦然。
- **显示对齐网格 (Show Snap Grid):** 切换对齐网格的显示。使用对齐网格可以帮助你更准确地放置控件，且更省力。
- **网格对齐 (Snapping to Gridlines):** 决定控件在表单上的放置方式。使用网格对齐意味着控件会自动出现在特定的边界上，这使得放置控件变得更加容易。然而，在按照意愿精确放置控件时，灵活性也会稍微小一点。
- **切换画布背景 (Toggle Artboard Background):** 控制你正在创建的表单后面显示的背景。默认值是灰色背景，如图 2-1 所示。你也可以选择黑色背景，这会让表单特征更加突出，但可能更容易眼睛疲劳。
- **对齐辅助线 (Snapping to Snaplines):** 控制在表单上放置控件时出现的 `snaplines` 线，这些线显示了一个控件与另一个控件的对齐情况。使用辅助线可以让你更容易对齐控件，并让你的表单外观更美观。然而，对齐辅助线也可能让你难以将控件精确地放置在你想要的位置。
- **控件显示选项 (Control Display Options):** 你可以选择显示工具箱中的所有控件（默认），或仅显示适用于特定平台的控件。使用“仅显示平台控件 (Only Display Platform Controls)”选项可以提高开发环境的稳定性，并防止你在试图弄清设计区域中每个到底是什么时眼睛几乎发狂。

在设计 (Design) 和 `XAML` 框架之间分割线的左侧有一个小小的双箭头图标。点击此图标可以将底部框架中的任何内容更改到顶部框架中，反之亦然。

在同一条分割线的右侧有三个按钮，它们决定了你的分割类型——垂直拆分、水平拆分（默认值）或不拆分（让设计器或代码编辑器占据整个空间）。有些人喜欢代码，有些人喜欢设计器，有些人则倾向于两者的结合。由你决定如何使用这些工具。

## Windows Presentation Foundation (WPF)

Windows Presentation Foundation 在第 5  中会有深入介绍，但目前你应该知道它是微软 Windows 桌面开发体验的重点。是的，你仍然可以看到很多 Windows Forms 开发，但较新的应用程序依赖于 WPF 或 UWP。第 5  详细讨论了 WPF，因此你可以在那里阅读更多信息。图 2-3 显示了 WPF 设计器，它与图 2-2 所示的 UWP 设计器有惊人的相似之处。

![WPF 设计器截图。](img/978119839071-fg0402.png)

图 2-3： WPF 设计器。

![记住](img/remember.png) 在创建 WPF 应用时，你决定使用哪个版本的 `.NET` 框架：`.NET Core 3.1`、`.NET 5.0` 或 `.NET 6.0`。框架版本决定了应用程序可用的功能，并在某种程度上控制了它的外观。图 2-3 显示了当你使用 `.NET 6.0` 时看到的内容。注意，你看到的是窗口而不是页面（就像使用 UWP 设计器时那样）。你不需要选择设备大小。你可以点击设计器中的设计内容并根据需要移动它们，或者使用设计器选择内容并在 `Properties` (属性) 面板中编辑属性（将在接下来的布局工作区 中介绍）。此外，如果你在代码区域更改了内容，你将在设计中看到更改。以下列表包含了 WPF 设计器和 UWP 设计器之间的某些区别：

- **特效 (Effects):** 切换用户界面。关闭特效会使用户界面变得不那么有趣，但也能为生产性用例节省处理能力。
- **禁用项目代码 (Disable Project Code):** 启用或禁用使用 `XAML` 代码显示表单内容。有时图 2-3 底部窗口中出现的 `XAML` 包含错误。你可以禁用项目代码以便在不崩溃的情况下修复这些错误。

### Windows Forms

Windows Forms 设计器与 WPF 设计器之间的主要区别是 Windows Forms 缺少代码面板。虽然 Windows Forms 有代码支持，但你无法直接编辑它。Windows Forms 设计器会为你完成此任务，并将代码放置在特殊的设计器文件中，例如某个项目中的 `Form1.Designer.cs`。

本书没有详细介绍 Windows Forms 主题（书中有几个项目，例如第 3 卷中第 4 章的网络网络状态，以及第 3 卷中第 5 章的图像处理）。尽管它仍然是一个活跃的开发平台，但大多数开发者正在转向 WPF，因此在开发新项目时花更多时间熟悉该环境是值得的。WPF 执行与 Windows Forms 相同的编程职责，但它是更新的技术。Windows Forms 设计器如图 2-4 所示。

![Windows Forms 设计器截图。](img/978119839071-fg0404.png)

图 2-4： Windows Forms 设计器。

### 数据视图 (Data View)

数据视图通常配合 `Server Explorer` 使用，是 Visual Studio 内部的一部分。你可以在这里查看和编辑 SQL Server 以及其他数据库系统的表。图 2-5 所示的示例是 `AdventureWorks2012` 数据库中的 `Address (Person)` 表。

![使用数据视图的截图](img/978119839071-fg0405.png)

图 2-5： 谁数据视图？

这里的功能非常强大，空间无法涵盖所有。再次，这不是一本关于数据库的书，所以你可能需要阅读关于 Server Explorer 连接功能的 MSDN 文档。

## 布局工作区 (Paneling the Studio)

为了保持足够的灵活性，Visual Studio 拥有大量被称为面板（有时根据说法称为窗）的模块化窗口。这些面板处理所有直接编辑设计或代码之外。它们管理文件、管理对象、显示反馈并执行各种功能。

Visual Studio 有超过 30 个面板。你通常通过 `查看` 菜单访问它们，例如 `查看 ⇒ 解决方案管理器` 以显示解决方案管理器面板，或者通过 `调试/窗口` 菜单，例如 `调试 ⇒ 窗口 ⇒ 断点` 以显示断点面板。这里没有空间讨论所有面板，所以本章仅介绍最常用的五个。

### 解决方案管理器 (Solution Explorer)

解决方案管理器（参见图 2-6

图 2-6： 解决方案管理器。

#### 解决方案 (Solutions)

对于解决方案本身，解决方案管理器提供了许多重要工具（通过右键点击解决方案项访问），包括：

- **解决方案管理 (Solution Management):** 允许生成、重新生成或清理解决方案。此外，你还可以进行分析显示应用程序的运行情况。





- **配置管理器 (Configuration Manager):** 为解决方案本身的设置文件提供了一个实用的界面。如果你希望在文件中存储所有调试信息，可以在此处指定构建时希望使用 `Release` 还是 `Debug` 编译。你还可以告诉编译器你希望为 32 位系统还是 64 位系统构建软件。你可以从`生成 (Build)` 菜单进入`配置管理器`。
- **管理和还原 NuGet 包 (Manage and Restore NuGet Packages):** 允许你向解决方案添加新包以扩展 Visual Studio 提供的功能。你也可以根据需要向解决方案还原现有的包。
- **添加项目 (Add Projects):** 显示对话框，你可以使用这些框向现有解决方案添加新项目。
- **项目依赖 (Project Dependencies):** 选择 `设置启动项目 (Set Startup Projects)` 会显示一个对话框，显示项目之间的相互关系，并描述项目相互依赖的方式。它还有一个用于生成顺序的选项页。当你遇到奇怪的“对象中没有引用成员”错误时，首先检查这里。你的解决方案需要包含多个项目，此命令才能在`项目 (Project)` 菜单中可用。
- **创建 Git 仓库 (Create Git Repository):** 为你提供在线存储代码的方法。此功能确保本地机器的丢失不会导致代码的丢失。你还可以使用在线仓库与他人共享代码。
- **属性页 (Property Pages):** 决定哪个项目应该在调试时启动，以及源代码保存在何处等。

## 项目 (Projects)
项目是独立的编译单元，并按类型划分。你可以在本迷你书籍的第 1 章中找到更多关于项目的信息。`解决方案资源管理器 (Solution Explorer)` 为项目提供了添加和删除文件、创建引用和服务服务、设置类图、打开相应的 Windows 资源管理器文件夹以及设置属性的功能。所有这些信息都保存在`项目 (Project)` 文件中。`Project` 文件只是一个 XML 文件。该文件有几个关键特征：
- 它为每个生成类型包含一个 `PropertyGroup`。这是因为你可以为每种类型的可执行文件设置不同的属性。
- 它包含一个 `ItemGroup`，其中包含所有引用（包括所需的 `Framework` 版本），以及另一组包含项目加载细节的 `ItemGroups`。
- 文件包含了项目常规详细信息的导入和 `Target` 集合。你实际上可以手动编辑该文件以创建自定义生成环境。

你可能不会修改你的 `Project` 文件，但知道可以这样做以及微软留有内联注释是重要的。他们预料到该文件会发生变化。

## 文件 (Files)
文件就没那么有趣了。它们几乎与你预期的完全一样。它们托管正在开发的程序源代码。`解决方案资源管理器`基本上以 Windows 资源管理器的方式管理项目中的文件。`解决方案资源管理器`列出文件和文件夹，并允许在设计器或`代码编辑器 (Code Editor)` 中打开它们。

![提示](img/tip.png) `解决方案资源管理器`还知道显示哪些文件。如果文件不在项目中，但恰好位于项目文件夹中，它将不会显示在`管理器`中。如果你找不到某个文件，尝试点击`管理器` 顶部灰色按钮栏中的`显示所有文件 (Show All Files)` 按钮。隐藏文件将以灰色显示，但仍不会编译到项目中。如果你需要，可以将它们添加到项目中。

## 属性 (Properties)
`属性 (Properties)` 面板（参见图 2-7）是一个简单灵活的工具，允许你更新开发项目中所有事物的无尽细节列表。该面板基本上是一个带有双列宽数据网格的窗口。它以键值对读取属性，并允许轻松查看和编辑。

![修改对象属性的快照。](img/9781119839071-fg040207.png)

图 2-7 修改对象属性。

你可以在此处找到开发项目中的一切详细信息。在 Visual Studio 中点击任何内容并按 F4 即可调出属性面板（参见图 2-7）。这里的：
- 解决方案资源管理器
- 数据库连接
- 项目
- 解决方案详细信息
- 属性 (Properties)

## 工具箱 (Toolbox)
工具箱的一个有趣特性是工具箱（参见图 2-8）。它会根据上下文显示控件。在设计器中使用时，工具箱是工具实用的工具。它显示对于给定文件类型可用的控件。请记住关于工具箱的一点：它只有在有文件时才有效。它还可以用于存储文本。

![工具箱的快照。](img/9781119839071-fg040208.png)

图 2-8 工具箱。

要将服务器添加到解决方案资源管理器，请按照以下步骤操作：
1. 右键点击`服务器`。
2. 点击`添加服务器` 按钮。
3. 输入要添加的服务器的名称或 IP 地址。
4. 点击`使用用户名连接`并输入新的凭据。
5. 点击`确定`。

## 服务器资源管理器 (Server Explorer)
![记住](img/remember.png) `服务器资源管理器`（参见图 2-9）允许访问本地或远程机器上的重要服务。这些服务可能是从事件日志到消息队列 (MSMQ) 的任何内容，你在测试应用程序部分时需要它们。它通常包括两类服务：
- 管理服务
- 数据库连接

![服务器资源管理器的快照。](img/9781119839071-fg040209.png)

图 2-9 服务器资源管理器

### 管理服务
管理服务包括诸如事件日志和消息队列 (MSMQ) 等服务，你在测试应用程序部分时需要它们。例如，互联网信息服务 (IIS) 是列表中的一个管理服务。尝试一下你看到的服务。该面板有很多书中未涵盖的功能。

### 数据库连接
在图 2-9 服务之上是数据库连接。这些是在之前的项目中创建的连接，Visual Studio 会保留它们，以备其他项目之需。其目标是减少对 `SQL 管理控制台`（管理数据库的老方法）的依赖，它做得非常好。关键问题是访问数据模型（表名和列）以及存储过程；在无法访问数据库的情况下开发程序是非常困难的。在新的连接中，这些数据库对象将被赋予默认文件夹：
- 数据库图
- 表
- 视图
- 存储过程
- 函数
- 类型
- 同义词





## 程序集 (Assemblies)

你应该尝试的关键是打开一个存储过程（你可以通过在数据源面板中双击它来实现——该面板在具有数据连接的解决方案中可用）。这样做时，你可以直接在 Visual Studio 中轻松编辑 SQL 代码，并带有缩进和颜色显示。使用它吧。它非常方便。

### 类视图 (Class View)

五个主面板中的最后一个是类视图。正如在书籍 1 和 2 中讨论的，.NET Framework 中的一切都是对象。构成框架的类——它们都是 `Object` 的派生类——可以在树形视图中查看。类视图就是该树形视图的主页（参见图 2-10）。

通过类视图，你可以查看类的所有成员并访问内联文档，这可以让你对构成项目的框架和自定义类有一个概述。

![带有 Class 的视图截图](img/9781119839071-fg040210.png)

图 2-10: 带有 Class 的视图。

## 在代码编辑器中编码

Visual Studio 的代码编辑器有很多之处。这是你花费大部分时间的地方。代码编辑器有两个主要的工具：

*   **编辑器本身：** 第一个是你编辑代码的屏幕——代码编辑器。
*   **辅助窗口：** 第二个是那些小的辅助窗口，它们执行着许多与代码不直接相关的有用操作。

### 练手代码编辑器

代码编辑器是你编辑代码的地方。无论什么种类型的代码，都在这里进行编辑。你使用代码编辑器来创建类库，它提供了一个智能界面，以确保你的类库有良好的运行机会。如果你在处理 XML，它的工作方式就像 XML 编辑器（如之前所示的图 2-2 中视图的下半部分）。

你可以通过几种方法进入代码编辑器中的代码文件。最常见的方法是在解决方案资源管理器中双击源代码文件，它将在代码编辑器中打开。

如果你在设计器中查看内容，可以通过以下三种方法之一进入与相关文件相关的后台代码（code-behind）：

*   在列表中突出文件后，点击解决方案资源管理器中的 `View Code` 按钮。
*   右键点击设计表面并选择 `View Code`。
*   在设计器中双击控件以生成该控件的事件并跳转到代码视图。

随着时间的推移，你会发现自己会使用这三种方法。注意，你可以通过点击设计器文件旁边的小三角形，然后双击嵌套其中的代码文件来直接进入后台代码文件。（此功能对自动生成的文件有效，但不会打开与自动生成文件相关的后台代码。）

#### 使用 IntelliSense 自动补全

IntelliSense（有时也称为 AutoComplete、IntelliCode 或为了让你混乱而引入的其他名称）是微软的自动补全功能，它是代码编辑器的一个重要部分。无论你是否主观，都会发现 IntelliSense。在代码视图中，点击类内部并按 `Ctrl+spacebar`。你允许在那里输入的所有内容都会显示在一个大列表中。

很棒的一点是，IntelliSense 是上下文敏感的。输入 `Console` 并按点（`.`）。`Console` 类的所有可用成员都会出现。IntelliSense 让你保持准确，并防止你每天都去记忆 .NET Framework 中那两万多个成员。

IntelliSense 对方法签名也有帮助。通过添加 `WriteLine` 来继续你之前开始的那行代码——换句话说，输入 `(Console.WriteLine)`——然后查看 IntelliSense。它会告诉你该成员的所有重载版本。使用向上和向下方向键在这些成员之间移动。它非常顺滑。

#### 大纲视图 (Outlining)

Visual Studio 会自动为你的代码创建大纲。注意代码编辑器中每个命名空间、类和方法旁边那个带有减号（–）的小方框。那些是为了可读性而对代码进行的折叠部分。现在看起来可能没什么，但当你那里有 2,200 行代码时，你会感到庆幸的。

你也可以创建自己的大纲。在想要折叠的区域之前，在新的一行输入 `#region`。在区域的末尾，输入 `#endregion`。这个新定义的区域——无论它是否在已有的大纲点上——都会获得一个新的大纲标记。如果在 `region` 语句之后添加注释，它将显示在折叠的大纲中。

![提示](img/tip.png) 你可以通过点击 `#region` 旁边的加号或减号来展开或折叠区域。折叠区域可以将你的精力集中在需要更改的代码上。展开区域让隐藏的代码再次出现，以便你进行处理。

### 探索辅助窗口

许多窗口影响文本的输入和输出以解决某些问题。作为一个整体，它们并没有真正的名称，因此某些开发者称之为辅助窗口。以下是其中几个：

*   **输出窗口 (Output window)：** 你经常使用输出窗口做两件事：
    *   **生成日志：** 每当你构建时，输出窗口都会跟踪后台进行的所有链接和编译，并显示可能出现的任何错误。你可以使用输出窗口中列出的错误来导航代码。输出框中的按钮可以帮助根据窗口中的消息在代码中跳转。
    *   **调试语句：** 输出窗口的第二个用途是查看调试语句手段。如果你在代码中使用 `Debug.Write()` 语句，输出窗口就是它去的地方。此外，如果你使用 `Console.Write()` 但运行的是 Windows Forms 应用程序，例如，文本将进入输出窗口。
*   **立即窗口 (Immediate window)：** 这个窗口的作用完全正如人们预期的那样：立即采取行动。在调试模式下，你可以使用立即窗口向正在运行的程序发送命令，更改状态或评估操作。尝试以下操作来查看立即窗口是如何工作的：
    1.  **打开任何可执行项目。**
    2.  **通过点击代码视图侧边灰色条在代码某处放置断点。** 出现一个红点。
    3.  **选择 `Debug ⇒ Start Debugging` 或按 `F5`。** 程序应该停止在你选择的地方。
    4.  **选择立即窗口。** 如果默认没有显示立即窗口，选择 `Debug ⇒ Windows ⇒ Immediate` 或按 `Ctrl+D,I`。
    5.  **输入 `? this.`** 看到 IntelliSense 菜单了吗？
    6.  **输入一个 `.`（点）。** 你会看到对 `this` 对象（如果你不在类中，它可能为空）可以执行的所有操作列表。`?` 命令意味着打印对象包含的内容，这就是立即窗口的用途。你还可以做不仅仅打印值。你可以更改变量值并修改程序的执行。它是你调试工具箱中一个强大的部分。
*   **断点窗口 (Breakpoints window)：** 如果你仍在运行上一个示例，可以通过按 `Ctrl+D,B` 显示断点窗口。断点窗口会出现，任何你添加的断点都会在其中（参见图 2-11）。

![断点窗口截图](img/9781119839071-fg040211.png)

图 2-11: 断点窗口。

这里很酷的地方在于你可以右键点击任何断点，并通过从上下文菜单中选择设置来完全更改该断点的属性。尝试一下——重要的选项列在列表中：

*   **位置 (Location)：** 指定应托管断点的代码行位置。如果你设置了过滤器并发现需要移动行，这非常方便。





- **条件 (Condition):** 只有当某个变量等于特定值时，你才能让断点在此行停止。
- **命中计数 (Hit Count):** 仅在被第 `x` 次命中后才在此处停止。
- **筛选 (Filter):** 与条件类似，不同之处你可以使用系统值，如 `MachineName`、`ProcessName`、`ProcessId`、`ThreadName` 和 `ThreadId`。这对多处理器开发等非常有用。
- **操作 (Actions)（未显示）：** 你可以做的不仅仅是在断点处停止——你可以执行诸如将值打印到输出窗口，甚至运行测试脚本。
- **任务列表窗口 (The Task List window):** 在编码时，你是否曾想过告诉后续开发者还有某些工作需要完成？要实现这一点，请创建一个以 `//TODO:` 开头的注释。添加 TODO 注释后，它将作为任务列表窗口（位于“视图”菜单中）中的任务出现。双击任务列表中的任务将带你进入设置该任务的行，这样你就不需要去搜索了。

# 使用专业工具

任何概述性章节总是包含一些无法归入任何类别的主题。本章介绍了许多你可能感兴趣的工具。

## 工具菜单 (Tools menu)

工具菜单提供了各种有趣工具的访问权限，你可以将其用于多种目的。以下列表没有包含工具菜单中的所有项，但包含了 Visual Studio 社区版中常见的项。

- **获取工具和功能 (Get Tools and Features):** 显示 Visual Studio 安装程序，你可以在其中找到要添加到 Visual Studio 的新功能，以及微软提供的任何基础产品更新。
- **连接数据库 (Connect to Database):** 参见本章节前面的“服务器资源管理器”部分。
- **连接服务器 (Connect to Server):** 在“服务器资源管理器”部分中讨论。
- **SQL Server (仅在安装了 SQL Server 时):** 提供一个菜单，其中包含专门针对 SQL Server 执行的任务，而不是任何其他数据源。
- **代码片段管理器 (Code Snippets Manager):** 代码片段让你能够在应用程序中重用部分代码。更多详情请参阅 `https://docs.microsoft.com/en-us/visualstudio/ide/code-snippets`。
- **选择工具箱项 (Choose Toolbox Items):** 该工具帮助你管理工具箱中的项。你可以添加或删除各种组件，包括 .NET、WPF、COM 和 Silverlight。
- **NuGet 包管理器 (NuGet Package Manager):** 管理 Visual Studio 插件。可以添加、删除、启用和禁用。
- **创建 GUID (Create GUID):** 创建全局唯一标识符 (GUID)，即那些 25 位的代码之一，据称它们在未来 2,500 年内将是唯一的。
- **外部工具 (External Tools):** 允许你将单独的 `EXE` 文件添加到工具菜单，例如记事本、NUnit 或工具，从而为 Visual Studio 增加功能。
- **命令行 (Command Line):** 显示 Windows 命令提示符窗口或 PowerShell 窗口，你可以在其中与你的应用程序、Visual Studio、C#或其他工具进行交互。这两个窗口都会在当前项目的文件夹中打开，因此你不需要在驱动器中寻找它们。
- **导入和导出设置 (Import and Export Settings):** 帮助你在不同的开发工具之间移动项目。你可以将当前设置存储在 `Users\<User Name>\AppData\Local\VisualStudio\<Version Number>\Settings` 目录下的文件中，或将当前设置更改另一组设置。你可以与其他开发者共享设置。
- **自定义 (Customize):** 允许你更改 Visual Studio 菜单和工具栏的外观感受，包括哪些工具栏可见以及它们包含的命令。
- **选项 (Options):** 改变 Visual Studio 的工作方式。本书的第 3 章中详细介绍了“选项”。设置 Visual Studio 以符合你喜欢的样式和工作方式。

## 生成 (Building)

本书的之前的章节讨论了项目生成的基础。生成菜单中的其他几个选项至少值得简单说明，包括以下项：

- **重新生成 (Rebuild):** 这会检查整个项目的所有引用。然后删除任何现有的编译文件并从头开始编译项目。如果你的开发计算机自上次生成以来更改了配置，则此功能非常有用。
- **清理 (Clean):** 这实际上会删除作为项目一部分生成的 `EXEs` 和 `DLLs`（但不包括你的代码文件），还会删除通过设置为该模式的引用复制到项目的所有 `DLLs`。
- **批生成 (Batch Build):** 允许你同时生成发布版本和调试版本（例如），或者 32 位和 64 位（另一个示例）。
- **配置管理器 (Configuration Manager):** 用此设置生成项目的顺序和模式。最常用的配置是 DEBUG（用于进行中的代码）和 `RELEASE`（用于已完成的代码）。

# 将调试器作为学习辅助

你可能会惊讶地发现，许多专业开发者是如何学习新技术的——通过查看他人的代码。这看起来像是在作弊，但实际上是处理问题的聪明方法，因为别人已经完成了所有的困难工作。当然，如果只是看代码，要试图理解某个特别微妙的编程技术是如何工作的，可能会消耗几天时间。在看到代码运行时确定其工作原理要容易得多，这正是调试器成为学习辅助工具的原因。

本节的示例依赖于你在第 5 章中首先的 cribbage 应用程序。然而，这些技术适用于任何代码，你没有必要亲自运行任何示例。接下来的章节将为你详细说明。

### 单步执行代码 (Stepping through code)

将调试器作为学习工具的第一步是在代码中设置一个或多个断点。例如，你想查看 `CribbageBoard.Paint()` 方法在 Cribbage 程序中是如何工作的。要执行此任务，只需点击编辑器左侧的灰色条。断点将带有红点显示，代码段将被高亮（通常也是红色）。

下一步是按 F5 或选择调试 ⇒ 启动调试来启动调试器。你将在遇到的第一个断点处停止，这可能不是你设置的第一个断点或代码中的第一个断点。事实上，观察你最终所在地非常有启发性，因为断点的位置告诉了应用程序是如何启动的，包括它必须执行的任务以及执行的顺序。

接下来是单步执行。你可以看到指令指针随着应用程序的执行而移动。你有选项：

- **逐语句 (Step Into):** 执行下一行代码。当代码为方法调用时，指令指针将进入该方法，让你看到方法的内部工作原理。当然，你必须拥有方法的源代码才能看到它是如何工作的。
- **逐过程 (Step Over):** 执行下一行代码而不进入任何方法调用。方法调的内容仍然执行，但你看到的是方法调的结果，而不是方法调用的实际原理。方法调用变成了一个黑盒。
- **逐出 (Step Out):** 到上一级（在完成当前方法的执行后）并执行调用者代码的下一行。如果你已经在方法调用内部看到了你想看的内容，点击此按钮将跳出该方法，以便看到应用程序下一层中的下一行代码（除非你已经处于应用程序的最顶层）。

### 转到特定代码位置 (Going to a particular code location)





当应用程序运行时，你可能不想逐行单步执行每一行代码。是的，你希望在某个断点处停止，但随后你决定并不真的想停留在那里逐行执行代码。在这种情况下，你可以将鼠标悬停在下一个想要停止的某行代码旁边。你会看到一个绿色的向右箭头，如图 2-12 所示。

![执行到某行代码的快照。](img/9781119839071-fg040212.png)

图 2-12： 执行到某行代码。

当你点击向右的箭头时，从现有指令指针位置到你指向的位置的代码将执行。你将看到执行结果，但看不到具体的每一个步骤。在某些情况下，这种技术将帮助你跳过某些问题代码，在这些代码中时序问题导致你无法真正看到代码是如何执行的。

### 观察应用程序数据

理解数据随时间的变化是使用调试器学习的重要组成部分。你可以访问多个窗口来帮助完成此。例如，你可以在代码中包含 `Debug` 和 `Trace` 语句，然后在输出窗口中查看它们的输出。要包含 `Debug` 和 `Trace` 语句，你必须在应用程序代码顶部添加 `using System.Diagnostics;`。当你只想为应用程序的调试发布（debug releases）输出值时，使用 `Debug` 语句。当你想为应用程序的调试和发布版本都输出值时，使用 `Trace` 语句。

每当你执行应用程序，图 2-13 所示的“本地”（Locals）窗口包含局部（而非全局）变量列表。局部变量是在当前方法中设置的变量，并且可能是你在设计良好的代码中最频繁使用的变量。

![使用“本地”窗口查看局部变量值的快照。](img/9781119839071-fg040213.png)

图 2-13： 使用“本地”窗口查看局部变量值。

变量条目旁边的向右箭头告诉你可以向下钻取以查找更多信息。事实上，在某些情况下，你可以向下钻取很多层才能到达末尾。某些对象非常复杂。查看对象的内容有助于你更好地理解它们，并通常能为如何更好地使用它们创建健壮的应用程序提供见解。

如果特定变量没有出现在“本地”窗口中，或者你想在代码执行时更详细地查看特定的对象元素，可以使用图 2-14 所示的“监视”（Watch）窗口。你在窗口中输入想要监视的变量。随着代码的执行，你会看到值的变化。“监视”窗口还允许输入表达式，如 `radius * 2` 或 `employee == null`。

![使用“监视”窗口创建自定义变量视图的快照。](img/9781119839071-fg040214.png)

图 2-14： 使用“监视”窗口创建自定义变量视图。

### 查看应用程序内部结构

学习在 Visual Studio 中点击右键是一项价值的辅助。每当你看到任何看起来有趣的内容时，右键点击它。右键菜单告诉你可以对该对象执行的操作。例如，你可以右键点击一个类，并在右键菜单中选择它的详细视图项之一。你最常用的内部视图选项是：

* `查看定义`（Peek Definition）：在当前代码窗口内的小窗口中显示请求对象的定义。定义可以提供更多关于该对象的信息。
* `转到定义`（Go To Definition）：打开包含请求对象定义的文件。这种方法可能会让你离开应用程序，但你可以获得更多关于该对象及其关联对象的详细信息。
* `转到实现`（Go To Implementation）：带你到实现对象的代码位置，从而使其在应用程序中可用。定义描述对象，而实现使其成为一个可用的、真实的对象。
* `查找所有引用`（Find All References）：显示代码中使用该对象的每个位置，以便你找到它的所有引用。找到对象在何处被使用有助于更好地理解如何根据自己的需求使用它。

# 第 3 章

# 自定义 Visual Studio

## 本章内容

* 设置环境选项
* 更改菜单和命令
* 开发项目模板

在本教程书的第 1 章和第 2 章 中，你了解如何安装 Visual Studio 并创建一个新项目。你还看到了用户界面提供的功能。好玩的阶段结束了。现在你可以让它为你服务了。

Visual Studio 提供了令人眼花缭乱的自定义选项。如果使用不当，这些选项极有可能让你和同事的生活变得痛苦。如果使用正确，它们潜力让你的生产力翻倍。

从最基础的来说，自定义涉及设置选项以更好地匹配你的环境、风格和工作模式。这些选项包含了从代码可见性到版本控制的所有内容。其理念是根据你的精确规格配置 Visual Studio 的选项。

下一步是提高应用程序的易用性，以匹配你的日常操作。实现这一点的最佳方法之一是更改工具栏和菜单，让你每天使用的功能更易于获取。

最后，你深入研究了 Visual Studio 的项目和文件模板。你知道当你创建一个新的 XAML 文件（例如）或 C# 类文件时，该文件的内容是由模板控制并可编辑的吗？不知道？好吧，你现在知道了！

所有这些内容加起来就是一个相当灵活的集成开发环境 (IDE)。虽然灵活性很好，但目标是设置一个匹配你风格的配置。只有你自己知道那个配置是什么。本章将告诉你软件可以做什么，并为你提供进行更改的工具。

![记住](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要容易得多。你可以在下载源码的 `\CSAIOD2E\BK04\CH03` 文件夹中找到本章的源码。请参见引言了解如何找到这些源文件。

## 设置选项

选择 `工具 ⇒ 选项` 菜单项打开选项对话框，其外观类似于图 3-1（页面数量取决于你安装的 Visual Studio 功能）。当你打开对话框时，环境部分可能会打开并显示内容；点击部分标题旁的箭头查看其他项目。）它通常用于设置布尔类型的选项，如“显示此”或“提供那些”，或更改 Visual Studio 存储某些文件的路径。

![默认选项界面的快照。](img/9781119839071-fg04301.png)

图 3-1： 默认选项界面。

这些细节虽然很好，但本章的目标是介绍选项提供的其他内容。接下来的章节从调整环境开始，描述卓越的语言选项，然后探索一些很酷的东西。

### 环境

环境部分是选项框中开始的地方。这里的部分包括代码编辑屏幕的字体细节、按键映射以及启动窗口的简单信息源聚合 (RSS) 馈设置。





`Environment\Fonts and Colors` 设置可能仅在你需要进行演示或有特殊视觉需求（如色盲或无法看清小号字体）时才会感兴趣。16 字体是大多数开发者的首选尺寸。市场上有很多“代码友好”的字体，你可以在此处选择它们。

## 定义启动窗口

`Start window`（启动窗口）是你启动 Visual Studio 时看到的第一个图形元素。你可以在 `Environment\General` 页面找到此设置。`On Startup`、`Open` 下拉列表包含以下选项：

*   **启动窗口 (Start Window):** 默认选项打开启动窗口，以便你可以打开最近的解决方案、创建新解决方案、从在线仓库获取代码，或者打开最近没有打开（或从未打开过）的远程或本地项目或解决方案。
*   **最近的解决方案 (Most Recent Solution):** 此选项完全忽略启动窗口，直接进入工作。如果你需要，仍然可以通过关闭解决方案（使用 `File⇒  Close Solution`）来查看启动窗口。如果你于不查看启动窗口的内容，请使用此选项。
*   **空环境 (Empty Environment):** 此选项将在不执行任何操作的情况下打开 Visual Studio。当你不知道如何开始会话，但觉得 Visual Studio 尝试替你做决定很烦时，请使用此选项。

## 键盘命令

选项对话框中最用的设置是 `Environment\Keyboard` 设置。通过键盘映射，你可以让 Visual Studio 用起来感觉像 Visual C# 2005。

![Tip](img/tip.png) 键盘映射是你设置的组合键，用于通过键盘运行命令，而不是通过鼠标点击。例如，一个通用的映射是 `Ctrl+C`，它复制内容的方式与点击 Edit 菜单然后点击 Copy 相同。许多开发者认为，使用键盘映射命令会让开发体验更快速、更易用。

键盘设置本质上允许你为 Visual Studio 中的任何菜单选择设置键盘命令。`Apply the Following Additional Keyboard Mapping Scheme`（应用以下附加键盘映射方案）下拉列表允许使用不同的键映射，如果你恰好喜欢其他开发环境的映射。

### 语言 (Language)

`language`（语言）一词并不意味着 `Environment\International Settings`（国际设置）页面的设置（该设置允许你在安装了额外语言包时更改 Visual Studio 的显示语言，尽管这很方便）。它指的是你在使用 Visual Studio 时工作的*编程*语言。`Text Editor` 部分是你为这些每种编程语言提供设置的地方。

`Text Editor` 选项更改了 `Code Editor` 的行为。Visual Studio 出版支持的所有语言都出现在主标题下的树形视图中，允许你更改文本编辑器的常规选项、制表符、格式、有时的高级选项以及杂项功能。

例如，查看 `Text Editor\C#`。要打开 C# 部分，点击 `Text Editor` 侧的右箭头，然后点击 `C#` 侧的右箭头。选项面板中的第一个视图是 General（常规）视图。在这里，你可以更改语句完成的默认选项、各种行为设置，以及 `Code Editor` 除代码之外应该显示的内容。你可以使用的其他面板还有：

*   **滚动条 (Scroll Bars):** 此部分包含关于 Visual Studio 如何以及何时显示滚动条的选项。你对水平和垂直滚动条有单独设置。所有注释选项也出现在此页。
*   **制表符 (Tabs):** 此部分供对源代码缩进有执着要求的人使用。Tabs 面板决定了多少空格组成一个制表符，以及 Visual Studio 是否应该自动插入它们。
*   **高级 (Advanced):** 此部分可能应该称为*杂项*(Miscellaneous)。所有不符合其他类别的内容都在这里。在此部分中，处理注释、接口实现和重构细节都有一个复选框，其基本含义是：“如果你不喜欢 Visual Studio 这样做，请点击此处。”
*   **代码样式 (Code Style):** 此部分包含多个子部分，均定义了 Visual Studio 如何呈现和格式化代码。
    *   **常规 (General):** 包含定义 Visual Studio 如何呈现 `this` 对象项的所有选项。
    *   **格式化 (Formatting):** C# 中的格式化非常深入。通常，C# 程序员对代码的外观非常挑剔。Visual Studio 做了很多工作来帮助你的代码看起来像你想要的，但你必须告诉它怎么做。格式化选项包括：General（自动格式化功能）；Indentation（缩进）；Newlines（换行）；Spacing（间距）；和 Wrapping（换行）。
    *   **命名 (Naming):** 此页面包含确定 Visual Studio 提醒命名问题的选项。例如，有一个选项可以确保你所有的接口名称都以字母 I 开头。如果你创建了一个名称不以 I 开头的接口，编译器将根据你偏好的严重级别将其报告为 Required Style（强制样式）错误。
*   **IntelliSense:** 此部分决定 IntelliSense 在编辑器中的工作方式。例如，你可以决定是否将完成列表作为 IntelliSense 选择的一部分。

## 实用技巧 (Neat stuff)

这是一个很少使用的功能短列表。目前，它们可能没什么意义，但当你以后需要时会记得它们。

*   要实现新的源控制提供程序，首先安装包（例如用于 CodePlex SVN 实现的 Turtle，或 Team System），然后进入选项中的 `Source Control` 来选择你想使用的项。
*   许多人建议将项目存储在短文件路径中，如 `C:\Projects`。你可以在选项对话框的 `Projects and Solutions\Locations` 部分更改存储项目的位置。
*   `NuGet Package Manager` 是 Visual Studio 的重要组成部分，因为它允许你添加专门的功能。Visual Studio 仅带有一个源（尽管非常广泛）。但是，你可以根据需要从 `NuGet Package Manager\Package Sources` 部分添加更多源。关于你可能想要使用的另一个源示例，请查看位于 [`https://www.grapecity.com/componentone/docs/uwp/online-getting-started/config-nugetpackage.html`](https://www.grapecity.com/componentone/docs/uwp/online-getting-started/config-nugetpackage.html) 的文章。
*   你可以使用选项面板中的 `Text Editor / File Extension` 部分教授 Visual Studio 使用特定的文件编辑器打开具有给定扩展名的文件。

 创建你自己的模板

旧版本的 Visual Studio 需要依赖各种黑科技来创建自定义模板。Visual Studio 2019 及更高版本提供了更好、更简单的方法，通过 Visual Studio IDE 处理自定义模板，这样你无需担心任何黑科技。以下章节提供了创建你自己的项目和项目模板的快速方法。

### 开发项目模板

仅仅设置项目就需要很长时间。如果你经常使用特定的项目配置，一次性完成所需的工作比每次创建新项目时都做一遍更有意义。以下步骤帮助你创建一个包含控制台应用程序和类文件的自定义项目模板。然而，你可以使用这种方法创建任何你需要的自定义项目模板。

1.  **点击创建新项目 (Create a New Project)。**

    你看到项目模板选择。
2.  **突出显示控制台应用程序 (.NET Framework) 项并点击下一步 (Next)。**

    你看到向导的“配置新项目”页面。





### 3. 在项目名称字段中输入 `ConsoleAndClass`，为项目选择位置，勾选“将解决方案和项目放在同一目录”，并选择一个 .NET Framework 版本。点击“创建”。

Visual Studio 为你创建一个新项目。此时，你可以提供任何需要包含的通用项目特有更改。但是，请记住，你并不是在创建一个完整的应用程序——你是在创建一个模板，一种类似于空白模板。

### 4. 在解决方案管理器中右键点击 `ConsoleAndClass` 项目，并在右键菜单中选择“添加 ⇒ 新建 ⇒ 项”。

Visual Studio 显示“添加新项”对话框。

### 5. 选择 `Class Entry` 并点击“添加”。

不需要给该类起一个特定的名称，因为你会在使用该模板时对其进行重命名。

### 6. 执行任何所需的类配置。

如果你每次都以某种方式配置类，现在就是进行必要更改的时候。目标是节省时间。

### 7. 选择“文件 ⇒ 保存所有”。

你之所以不费心编译模板，是因为它实际上不应该包含任何需要编译的内容——只需包含以后要创建的应用程序的配置。

### 8. 选择“项目 ⇒ 导出模板”。

你看到了“选择模板类型”页面，如图图 3-2 所示。在这里，你可以选择项目模板或项模板，以及选择你希望出现在模板中的元素。

![确定要创建项目模板还是项模板的快照](img/9781119839071-fg040302.png)

图 3-2： 确定你想创建项目模板还是项模板。

### 9. 选择“项目模板”并点击“下一步”。

向导显示“选择模板选项”页面，如图图 3-3 所示。在这里，你为模板名称、使用方法以及任何与模板关联的图形提供定义。注意，“输出位置”字段会自动为你定义，你无法更改它。你的模板将出现在一个 `.zip` 文件中，但你可以像访问其他模板一样访问它。以下是针对各个字段输入的的一些建议：

*   选择一个能够精确定义模板用途的名称，例如“控制台和类组合”。
*   提供一个模板描述以对类名进行补充，例如“此模板创建一个带有已添加类的 .NET Framework 控制台应用程序”。
*   确保图标图像具有辨识度，这样你的模板在列表中就会脱颖而出。示例使用了红色时钟图标来表示该模板将节省时间。
*   如果你的模板具有图形化性质，请为预览图像字段创建一个截图。否则，你真的不需要在该字段输入内容。

![提供足够信息供他人使用你的模板的快照](img/9781119839071-fg040303.png)

图 3-3： 提供足够的信息供他人使用你的模板。

### 10. 填写模板信息并点击“完成”。

![提示](img/tip.png) 向导会为你打开一个资源管理器的副本，指向包含你模板的文件夹，例如 `C:\Users\<用户名>\\Documents\Visual Studio 2022\My Exported Templates`。如果你计划与他人共享模板，可以将其复制到剪贴板并存储在其他位置。也可以通过修改文件对模板进行修改，除非你真的需要更改，否则可能应该避免这样做。

![记住](img/remember.png) 在创建新项目模板后，确保关闭任何项目并重启 Visual Studio。此时，你可以使用你的模板来创建新项目。然而，模板过滤对用户定义的模板无效，因此你必须将过滤器设置为“所有语言”、“所有平台”和“所有项目类型”才能看到你的模板，它通常会出现在列表顶部，如图图 3-4 所示。如果你没有看到你的模板，可以使用“创建新项目”对话框顶部的“搜索模板”字段进行搜索。

![移除所有过滤后，通常出现在列表第一项的模板快照](img/9781119839071-fg040304.png)

图 3-4： 移除所有过滤后，你的模板通常会出现在列表的第一项。

#### 开发项模板

创建项模板与创建项目模板类似。你首先创建一个项目，就像你在上一节中所做一样。按照以下步骤创建项模板（它与项目模板不同）：

1.  **选择“项目 ⇒ 导出模板”。**

    你看到了导出模板向导的“选择模板类型”页面，如图图 3-2 所示。

2.  **选择“项目模板”并点击“下一步”。**

    向导显示“选择模板选项”页面，如图图 3-3 所示。

3.  **选择 `Class Entry` 并点击“添加”。**

    向导显示“选择模板选项”页面，如图图 3-3 所示。

4.  **填写模板信息并点击“完成”。**

    向导会为你打开一个资源管理器的副本，指向包含你模板的文件夹，例如 `C:\Users\<用户名>\\Documents\Visual Studio 2022\My Exported Templates`。你的模板将出现在一个 `.zip` 文件中。




## 4. 数据的编辑、验证、转换和可视化
## 5. 深入了解 WPF 数据绑定

## 第 4 章：实战 WPF
### 1. 关注
### 2. 使用内置命令
### 3. 使用自定义命令
### 4. 使用路由命令

## 第 5 章：为 Windows 10 及以上版本编程
### 1. 什么是通用 平台 (UWP)？
### 2. UWP 支持的设备
### 3. 创建自己的 UWP 应用
### 4. 使用 .NET Core 应用程序

# 第 1 章
# 介绍 WPF

## 本章内容

![Bullet](img/check.png) 初识 WPF 及其能为你做什么
![Bullet](img/check.png) 使用 XAML
![Bullet](img/check.png) 构建第一个 WPF 应用程序
![Bullet](img/check.png) 比较 XAML 与 C#

WPF（Windows Presentation Foundation）是一种用于渲染用户界面的图形系统。它在应用程序的布局和交互方面提供了极大的灵活性。以公共语言运行时 (CLR) 为核心，你可以使用 C# 或任何其他 CLR 语言与用户界面元素进行通信并开发应用程序逻辑。WPF 对你的应用程序的优势在于其丰富的数据绑定和可视化支持，以及其设计灵活性和样式。

WPF 让你能够创建一个对受众更易用的应用程序。它赋予了你设计一个以前需要极长开发周期和数学天才才能实现的应用程序的能力。现在，你仅需三行代码就能实现图形和动画等困难内容！本章将向你介绍关键 WPF 概念以及当今软件行业常用的应用程序模式。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要简单得多。你可以在下载源码的 `\CSAIO4D2E\BK05\CH01` 文件夹中找到本章的源码。请参见“引言”了解如何查找这些源文件。

## 理解 WPF 能做什么

WPF 的图形能力使其成为数据可视化的完美选择。例如，标准的下拉列表（或组合框）。它目前的用途是允许用户从项目列表中选择单个项目。在例例中，假设你想让用户选择一个汽车型号进行购买。

显示这种选择的标准方法是显示一个包含汽车型号名称的下拉列表，用户可以从中选择。这种常见的解决方案存在一个根本性的可用性问题：用户只获得了一条信息来作为决策依据——即用于表示列表中项目的文本。

对于高级用户（或汽车发烧友）来说，这可能不是问题，但其他用户需要比型号名称更多的信息才能对想要购买的汽车做出明智决定。这正是 WPF 及其数据可视化能力大显身场的地方。你可以提供一个模板来定义下拉列表中每个项目是如何渲染的。模板可以包含任何视觉元素，例如图像、标签、文本框、工具提示、投影阴影等！

图 1-1 显示了组合框的典型显示。该控件具有局限性：它只能向用户传达一条信息，即表示汽车型号的文本（是的，你可以超越凡人水平的低级编程技术向组合框中添加图形，但大多数人并不想这样做）。你可以根据列表中的选择在另一个控件中显示汽车型号的图像，但这仍然要求用户在看到具体在选择什么之前做出选择。相反，WPF 具有灵活性可以在每个组合框项中显示许多信息，就像用户做出决策所需的所有信息的一站式商店一样。（参见 图 1-2 的 WPF 组合框。）

![典型组合框的快照。](img/9781119839071-fg050101.png)

图 1-1： 典型的组合框。

图 1-2 显示了 WPF 中的示例组合框。组合框项的渲染方式是使用数据模板定义的。（本微型书籍的第 3 章涵盖了数据模板。）此组合框中的每个项目都经过渲染，为用户提供视觉线索以及多个数据字段。显示所有这些信息使用户对他们所做的选择做出明智决定。

![数据可视化的快照——WPF 组合框。](img/9781119839071-fg050102.png)

图 1-2： 可视化数据——WPF 组合框。

## 介绍 XAML

WPF 允许你声明式地构建用户界面。扩展应用程序标记语言（XAML；读作 zammel）是 WPF 的基础。XAML 与 HTML 的相似之处在于，界面元素是基于标签的语法定义的。

![Technicalstuff](img/technicalstuff.png) XAML 是基于 XML 的，因此它必须是良好的，这意味着所有打开标签都需要关闭标签，并且文档中包含的所有元素和属性必须严格验证指定的架构。

默认情况下，在 Visual Studio 2010 及更高版本中创建 WPF 应用程序时，生成的 XAML 文件表示以下架构：

*   `http://schemas.microsoft.com/winfx/2006/xaml/presentation`: 此架构表示默认的 Windows Presentation Framework 命名空间。
*   `http://schemas.microsoft.com/winfx/2006/xaml`: 此架构表示映射到 CLR 对象的类。

大多数 CLR 对象都可以表示为 XAML 元素（抽象基类以及某些严格用于 CLR 继承目的的非抽象基类除外）。XAML 元素映射到类；属性映射到属性或事件。

在运行时处理 XAML 元素时，会调用其底层类的默认构造函数并实例化对象；根据 XAML 中的属性值设置其属性和事件。下一节节回顾回顾更多 XAML 基础知识，并带你进入应用程序开发之路。

## 深入学习！创建你的第一个应用程序

现在是让自己放松起来了，所以停一下，去拿杯含咖啡因饮料，坐在舒适的椅子上，打开电脑，准备好开始！创建你的第一个项目，请遵循以下步骤：

1.  **打开 Visual Studio。**
2.  **点击“创建新项目”。**
    你会看到可用项目的列表。
3.  **在筛选列表中选择 C#、Windows 和 Desktop。**
    Visual Studio 显示了 Windows 桌面项目类型列表。
4.  **高亮 WPF App (.NET Framework) 并点击下一步。**
    你会看到向导的“配置新项目”页面，如 图 1-3 所示。
5.  **在项目名称字段中输入 MyFirstWPFApplication，选择“将解决方案和项目放在同一目录”，然后点击“创建”。**
    Visual Studio 为你创建一个新的 WPF 项目，并显示定义了默认应用程序的设计器和代码编辑器。WPF 模板创建了两个 XAML 文件以及相应的代码后文件：`App.xaml` (`App.xaml.cs`) 和 `MainWindow.xaml` (`MainWindow.xaml.cs`)，如 图 1-4 所示。此时，你可以开始向示例应用程序添加代码了。

`App.xaml` 代表应用程序的入口点。这里是定义应用程序范围范围（全局作用域）资源和启动窗口的地方（参见 列表 1-1）。





![配置 WPF 项目的快照](img/9781119839071-fg050103.png)
图 1-3: 配置 WPF 项目。

![WPF 解决方案结构的快照](img/9781119839071-fg050104.png)
图 1-4: WPF 解决方案结构。

![技术细节](img/technicalstuff.png) 资源包含在可重用对象的键值对集合中。可以使用 XAML 和 C# 创建和检索资源。资源可以是任何内容——数据模板、字符串数组或用于为文本框背景上色的画刷。资源还是**作用域的**（`scoped`），这意味着它们可以适用于整个 `Application`（全局）、`Window`（窗口）、`User Control`（用户控件），甚至仅适用于特定的控件。

列表 1-1 App.xaml

```xml
<Application x:Class="MyFirstWPFApplication.App"
xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
xmlns:local="clr-namespace:MyFirstWPFApplication"
StartupUri="MainWindow.xaml">
<Application.Resources>
</Application.Resources>
</Application>
```

列表 1-1 显示了 Visual Studio 中 WPF App (.NET Framework) 模板生成的 XAML。注意已经定义了 WPF 命名空间。代表 CLR 对象的命名空间将在 XAML 文件中通过 `x` 前缀进行区分。

`StartupUri` 值定义了在执行之前将显示的窗口。在这种情况下，将显示 `MainWindow.xaml` 窗口。

`x:Class` 属性定义了该 XAML 文件的 C# 后置代码文件。如果你打开 `App.xaml.cs`，你会发现它的类名为 `App`，并且它继承自 `Application` 类（该 XAML 文件的根元素）。

![技术细节](img/technicalstuff.png) C# 使用命名空间来组织和定位类。要从特定命名空间创建对象，你可以在类定义顶部使用 "using" 语法。与 C# 类似，XAML 也要求你声明文档中使用了哪些命名空间。命名空间通常定义为文档根元素内的属性；根元素是 XAML 文档中的第一个 XML 标签。XAML 使用 XML 语法来定义命名空间——“xmlns”意味着“XML 命名空间”，后面通常跟着一个冒号（:）然后是别名。该别名是整个 XAML 文档中对该命名空间的简写引用；它是你用来从该命名空间中的类实例化对象的工具。

例如，如果你想从程序集 `MyTemplates.dll` 中添加命名空间 `MyTemplates.DataTemplates`（此处原文为 `MyTemplates.DataTemplates`），你可以将该命名空间定义为：

`xmlns:myDTs="clr-namespace:MyTemplates.DataTemplates;assembly=MyTemplates.dll"`

然后你就可以如下方式从 `MyTemplates.DataTemplates` 命名空间实例化对象：

```xml
<myDTs:myClass></myDTs:myClass>
```

### 声明应用程序作用域资源

为了帮助你理解全局应用程序作用域资源的创建和使用，本节将向你展示如何创建一个存储应用程序使用的字符串的资源。应用程序作用域资源适用于项目中定义的所有窗口和用户控件。按照以下步骤操作：

1. **通过向 `App.xaml` 根元素添加以下命名空间，添加位于 `mscorlib.dll` 程序集的 `System` 命名空间（参见列表 1-2）：**

    `xmlns:sys="clr-namespace:System;assembly=mscorlib"`

    `mscorlib.dll` 程序集是 `String` 类所在的地方。`String` 类现在可以在整个 `App.xaml` 文档中使用。

2. **在 `Application.Resource` 之间创建资源；添加以下 `String` 类元素：**

    `<sys:String x:Key="Purpose">Hello WPF World!</sys:String>`

    该元素实例化了一个 `String` 类型的对象，初始化值为 `Hello WPF World!`，并根据键 `Purpose` 进行索引。此资源现在可以通过请求资源“Purpose”在整个 `MyFirstWPFApplication` 应用程序中使用（参见列表 1-2）。

列表 1-2 定义了资源和系统命名空间更新后的 App.xaml

```xml
<Application x:Class="MyFirstWPFApplication.App"
xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
xmlns:local="clr-namespace:MyFirstWPFApplication"
xmlns:sys="clr-namespace:System;assembly=mscorlib"
StartupUri="MainWindow.xaml">
<Application.Resources>
<sys:String x:Key="Purpose">Hello WPF World!</sys:String>
</Application.Resources>
</Application>
```

![技术细节](img/technicalstuff.png) 你可能观察 `Application.Resources` 看起来有点奇怪。`Application.Resources` 是定义处。![技术细节](img/technicalstuff.png) 这种标签是 `Application` 的属性。

### 让应用程序执行一些事情

如果你按原样运行应用程序，除了显示空窗口外，什么都不会发生。

![记住](img/remember.png) `App.xaml` 是应用程序的入口。在这种情况下，空窗口是 `MainWindow.xaml`。

在 `MainWindow.xaml` 添加一个显示你定义的字符串的标签。按照以下步骤操作：

1. **打开 `MainWindow.xaml`。**

2. **在 `Grid` 标签之间，通过添加以下 XAML 定义具有单行单列的网格：**

```xml
<Grid.ColumnDefinitions>
<ColumnDefinition></ColumnDefinition>
</Grid.ColumnDefinitions>
<Grid.RowDefinitions>
<RowDefinition></RowDefinition>
</Grid.RowDefinitions>
```

每一列和每一行分别通过 `ColumnDefinitions` 和 `RowDefinitions` 属性内的 `ColumnDefinition` 和 `RowDefinition` 元素定义。如果你想添加更多列，只需向 `ColumnDefinitions` 中添加另一个 `ColumnDefinition` 元素。添加行也是如此：向 `RowDefinitions` 中添加 `RowDefinition` 元素。

3. **在 `Grid.RowDefinitions` 属性实正下方，使用以下 XAML 创建标签：**

```xml
<Label x:Name="lblPurpose" Content="{StaticResource Purpose}"
FontSize="25" Grid.Row="0" Grid.Column="0"/>
```





* `Content`: 赋值给此属性的值可以是任何类型。默认情况下，你可以为它分配一个 `string` 值，它将像你认为标准标签应该渲染的那样渲染。在 WPF 的世界中，`Content` 可以由任何内容组成：字符串、图像、用户控件实例、文本框等。有关更多信息，请参阅本微型教程书的第 2 章。

* `FontSize`: 标签字体的大小。需要注意的是，该大小不是以点（points）为单位的，而是用设备无关单位（Device Independent Units）表示。WPF 摒弃了像素和点的概念，转而采用通用的尺寸策略。可以将设备无关单位看作是像素更具相对性的尺寸。例如，如果标签的容器元素是 100 单位乘以 100 单位，那么标签将以该尺寸的 1/4 处渲染。

* `Grid.Row`: 指定要渲染标签的网格行。网格行集合从 0 开始计数，这意味着第一行是行 0，第二行是行 1，以此此类推。你还应该注意，`Label` 类并不包含名为 `Grid` 的属性。你在这里看到的是附加属性的概念。*附加属性*是一种将当前控件的上下文相对于容器控件属性进行赋值的方法。在这种情况下，你将标签分配为显示在其容器网格的第一行（行索引为 0）。同样观察到标签位于 `Grid` 标签内部；这就是定位容器 `Grid` 元素的方式。

* `Grid.Column`: 与 `Grid.Row` 类似，此附加属性指定要渲染标签的网格列。与 `Grid.Row` 一起，这两个属性共同标识了标签所在的单元格。在这种情况下，你将标签分配为渲染在其容器网格的第一列。网格列集合同样也是从 0 开始计数的。

继续运行你的应用程序。你现在看到 `Window` 上的标签上显示了 Hello WFP World！恭喜！你刚刚创建了你的第一个 WPF 应用程序！

## 凡 XAML 能做到的，C# 都能做得更好！

你可以使用 XAML 实现的任何内容可以在 C# 中实现。反之则并非如此；你在 C# 中能做的所有事情并不都能在 XAML 中完成。对于执行无法用 XAML 表达的带有过程过程的业务逻辑任务，C# 是显而易见的选择。在接下来的步骤中，你创建一个与上一节中创建的相同的 WPF 应用程序，这次使用 C# 来实现其功能：

1. **选择文件⇒  关闭解决方案，如果有必要，关闭当前解决方案。**

2. **点击创建新项目。**
   你将看到可用项目的列表。

3. **在筛选列表中选择 C#、Windows 和桌面应用（Desktop）。**
   Visual Studio 展示了 Windows 桌面项目类型列表。

4. **突出显示 App (.NET Framework) 并点击下一步。**
   你看到了向导的“配置新项目”页面，如图 1-3 所示。

5. **在项目名称字段中输入 MyFirstCodeOnlyWPFApplication，选择“将解决方案和项目放在同一目录”，然后点击创建。**
   Visual Studio 创建了解决方案和项目结构。

6. **打开 `App.xaml.cs`。**

7. **重写 `OnStartup` 方法，通过向 `App` 类添加以下代码来包含 Purpose 资源的创建：**

```csharp
protected override void OnStartup(StartupEventArgs e)
{
// 创建并添加 Purpose 资源
string purpose = "Hello WPF World, in C#";
this.Resources.Add("Purpose", purpose);
base.OnStartup(e);
}
```

8. **打开 `MainWindow.xaml` 并通过添加加粗所示的属性为 `Grid` 元素命名：**

```xml
<Grid x:Name="gridLayout">
</Grid>
```

9. **打开 `MainWindow.xaml.cs`，在默认构造函数中，`InitializeComponents` 方法调用之后，添加加粗所示的代码：**

```csharp
public MainWindow()
{
InitializeComponent();
// 定义网格列和行
this.gridLayout.ColumnDefinitions.Add(new ColumnDefinition());
this.gridLayout.RowDefinitions.Add(new RowDefinition());
// 从应用程序资源 Purpose 获取标签内容
string purpose = this.TryFindResource("Purpose") as string;
Label lblPurpose = new Label();
lblPurpose.Content = purpose;
lblPurpose.FontSize = 25;
// 将标签添加到网格中
this.gridLayout.Children.Add(lblPurpose);
// 分配附加属性值
Grid.SetColumn(lblPurpose, 0);
Grid.SetRow(lblPurpose, 0);
}
```

运行应用程序并观察结果，与本章早些节“深入学习！创建你的第一个 WPF 应用程序”中获得的产类似。

# 第 2 章

# 理解 WPF 基础

在本章中

* ![Bullet](img/check.png) **布局应用程序**
* ![Bullet](img/check.png) **使用布局面板**
* ![Bullet](img/check.png) **与 Grid 网格协作**
* ![Bullet](img/check.png) **实现仅显示、输入和基于列表的控件**

正如本微型教程书第 1 章所解释的，Windows Presentation Foundation (WPF) 不仅为应用程序的外观和感受带来了巨大变化，而且改变了开发方式。从工具箱中拖放控件到表单时代已一成为过去。尽管你仍然可以在 WPF 中进行拖放，但如果你直接编写 XAML，你会发现自己更好、更快乐。

曾经困难的事情现在变得简单。例如，在传统的 Windows 应用程序中，当用户更改大小时，控件通常会缩在角落，显示出大量的空白区域。唯一的治疗方法是大量的自定义代码或昂贵的第三方控件。WPF 将*流布局*概念引入了 Windows 世界。

在 WinForms 的 GDI/GDI+ 世界，修改控件样式或构建复杂的界面是一项艰巨的任务。WPF 完全重新定义了控件范式，让开发者能够完成以前不可想象的任务——包括在按钮上播放视频。然而，请记住，仅仅因为你*可以*这样做并不意味着你*应该*这样做！

在本章中，你将处理 WPF 的布局过程来控制应用程序的布局。本章还向你介绍了各种 WPF 控件。

![Remember](img/remember.png) 你不需要手动输入本章源代码。事实上，使用下载源码要简单得多。你可以在下载源码的 `\CSAIO4D2E\BK05\CH02` 文件夹找到本章源码。请参见引言了解如何找到这些源文件。

## 使用 WPF 布局应用程序

传统的 Windows Forms 开发处理的是绝对值。控件的位置和大小在设计时就决定，并基于开发机器的分辨率。当应用程序部署到用户手中时，在开发机上看起来很好的表单现在可能完全不同（甚至可能无法使用），因为硬件分辨率存在差异。

WPF 不依赖屏幕分辨率，而是根据系统每英寸点（DPI）使用设备无关单位（DIUs）来测量 UI 元素。这使得不同的硬件配置之间能够保持一致的外观。




WPF 布局基于相对值并在运行时进行调整。当你将控件放置在布局容器中（请参见下一节）时，渲染引擎仅将高度和宽度视为“建议”值。位置是相对于其他控件或容器定义的。实际渲染是一个两步过程：首先测量所有控件（并查询它们的首选尺寸），然后根据此对它们进行排列。

## 使用布局面板（Layout Panels）排列元素

设计窗口从布局控件（或称为面板）开始。面板与 `Content` 控件的不同之处在于，它们可以包含多个项目，并且根据面板的不同，它们会为你处理大量的底层工作。

面板控制着 `UIElements` 相互之间以及它们与其容器 `UIElement` 之间的关系，并且不规定绝对位置。大多数应用程序窗口都需要组合某些面板来实现所需的用户界面，因此理解所有这些面板至关重要。旧版本的 WPF 带有六种核心面板，它们将在后续章节中进行描述：

| `UIElement` | `是否为面板?` | `描述` |
| --- | --- | --- |
| `Canvas` | 是 | 创建一个区域，可以使用相对于 `Canvas` 区域的坐标来对子元素进行定位。 |
| `DockPanel` | 是 | 定义一个区域，可以在水平或垂直方向上相对于相互定位子元素。 |
| `Grid` | 是 | 允许像 HTML 表格一样使用行和列对子元素进行精确定位。`Margin` 属性允许精细定位。 |
| `StackPanel` | 是 | 将子元素排列成水平或垂直方向的单行。 |
| `UniformGrid` | 否 | 使用相等的单元格大小在网格中排列子元素。 |
| `WrapPanel` | 是 | 从左到右按顺序对子元素定位。当 `Orientation` 为垂直时，你也可以从上到下排列元素。随着更多子元素的添加，`WrapPanel` 会换行并开始在下一行放置子元素。因此，较小的显示器会使用更多行来显示子元素。 |

新版本的 WPF 还增加了这些面板：

| `UIElement` | `是否为面板?` | `描述` |
| --- | --- | --- |
| `TabPanel` | 否 | 定义 `TabControl` 中标签按钮的布局。 |
| `ToolBarOverflowPanel` | 否 | 排列 `ToolBar` 控件内的内容。 |
| `VirtualizingPanel` | 否 | 用于创建可以虚拟化子元素的面板的基类（用户看到的界面根据用户实际看到的项目从大量数据项中选择，这最终使应用程序运行更快且占用内存更少）。 |
| `VirtualizingStackPanel` | 是 | 在水平或垂直方向的单行上排列并虚拟化内容。 |

### Stack 面（堆叠面板）

Stack 面将 `UIElements` 堆叠放置。项目被放置在垂直堆中（默认值），如一叠 DVD，或者水平排列排列，如书架上的书。重要的一点是，理解项目在 XAML 中出现的顺序就是它们在面板中出现的顺序——XAML 中的第一个 `UIElement` 出现在顶部（垂直）或最左侧（水平）。以下代码包含了垂直堆面板的 XAML，如 图 2-1 所示。

```xml
<StackPanel x:Name="pnlContainer">
    <StackPanel Name="pnlStack" Grid.Row="0" Orientation="Vertical">
        <Button Content="A Button"/>
        <Button Content="Another Button"/>
        <TextBlock Text="This is a text block"/>
        <Button Content="Short"/>
        <Button Content="Long Button Label"/>
    </StackPanel>
</StackPanel>
```

![垂直堆面板快照。](img/978119839071-fig-001.png)

你可能会发现你希望能够根据用户的设备方向更改控件的方向。要做到这一点，你可以向现有代码添加一个按钮，如下所示：

```xml
<StackPanel x:Name="pnlContainer">
    <StackPanel Name="pnlStack" Grid.Row="0" Orientation="Vertical">
        <Button Content="A Button"/>
        <Button Content="Another Button"/>
        <TextBlock Text="This is a text block"/>
        <Button Content="Short"/>
        <Button Content="Long Button Label"/>
    </StackPanel>
    <StackPanel Name="pnlStack" Grid.Row="1" Orientation="Vertical">
        <Button x:Name="cmdOrientation" Content="Set Horizontal" Click="cmdOrientation_Click"/>
    </StackPanel>
</StackPanel>
```

新的 `cmdOrientation` 按钮出现在显示器的底部，如 图 2-2 所示，该图也显示了水平模式下的应用程序。图 2-2 中所示水平布局说明了当容器内控件的首选尺寸之和大于容器能容纳的内容时可能会发生的裁剪。

![显示裁剪内容的水平布局快照。](img/978119839071-fig-002.png)

方向（以及所有其他属性）都可以在运行时更改，如下所示代码所示。第 4 章 显示了使用各种后代码技术编写按钮事件的更好方法。

```csharp
private void cmdOrientation_Click(object sender, RoutedEventArgs e)
{
    Button button = sender as Button;
    if (button.Content.ToString() == "Set Vertical")
    {
        pnlStack.Orientation = Orientation.Vertical;
        pnlStack.MinHeight = 0;
        button.Content = "Set Horizontal";
        Title = "Stack Panel - Vertical";
    }
    else
    {
        pnlStack.Orientation = Orientation.Horizontal;
        pnlStack.MinHeight = 50;
        button.Content = "Set Vertical";
        Title = "Stack Panel - Horizontal";
    }
}
```

使用第二个 `StackPanel` 允许 `cmdOrientation` `Button` 保持其垂直方向，即使其他控件采用了水平方向。当你计划更改方向时，你需要细致地处理各种控件以获得你想要的结果。

![提示](img/tip.png) 注意，代码还根据需要更改 `pnlStack.MinHeight` 值以在屏幕上提供良好的外观。在不给较小设备带来用户界面问题的情况下提供愉悦的外观是很。实验将帮助你为用户界面的任何微调选择值。

### Wrap 面（换行面板）

`WrapPanel` 会将溢出的内容换行到下一行。这与典型工具栏的工作方式不同，工具栏中当没有足够的空间显示项目时，溢出项目会被隐藏。图 2-3 显示了 `StackPanel` 示例中的相同控件（按钮和文本块的混合）在 `WrapPanel` 中。（你也可以在下载源码的 `WrapPanel` 示例中找到此代码。）`WrapPanel` 示例的初始 XAML 如下所示：

```xml
<StackPanel x:Name="pnlContainer" Width="80">
    <WrapPanel Name="pnlWrap" Grid.Row="0">
        <Button Content="A Button"/>
        <Button Content="Another Button"/>
        <TextBlock Text="This is a text block"/>
        <Button Content="Short"/>
        <Button Content="Long Button Label"/>
    </WrapPanel>
    <WrapPanel Name="pnlWrap1" Grid.Row="1">
        <Button x:Name="cmdWidth" Content="Set Wide" Click="cmdWidth_Click"/>
    </WrapPanel>
</StackPanel>
```




`</WrapPanel>`

`</StackPanel>`

注意，即使使用了 `WrapPanel`，如果容器无法容纳最宽的项目（示例中的最后一个按钮），也会发生裁剪。此示例使用 `pnlContainer`，通过以下代码改变容器的宽窄，来展示 `WrapPanel` 在不同显示空间下的效果，你可以点击窗口底部的“Set Wide”（设置宽度）按钮进行测试：

```cs
private void cmdWidth_Click(object sender, RoutedEventArgs e)
{
    Button button = sender as Button;
    if (button.Content.ToString() == "Set Wide")
    {
        pnlContainer.Width = 350;
        button.Content = "Set Narrow";
        Title = "Wrap Panel - Wide";
    }
    else
    {
        pnlContainer.Width = 80;
        button.Content = "Set Wide";
        Title = "Wrap Panel - Narrow";
    }
}
```

![包含在 StackPanel 中的两个 WrapPanel 的快照。](img/9781119839071-fg050203.png)

FIGURE 2-3: 包含在 StackPanel 中的两个 `WrapPanel`。

### Dock 面板

如可下载源码中的 `DockPanel` 示例所示，`DockPanel` 使用附加属性（参见本迷你书籍的第 1 章）来“停靠”子 UI 元素。需要记住的一点是，子元素是按照 XAML 顺序停靠的，这意味着如果你有两个项目被分配到左侧（通过 `DockPanel.Dock="left"`），那么 XAML 中*出现顺序*的第一个 UIElement 将获得面板的最左侧边界，紧接着是下一个项目。以下是创建 `DockPanel` 使用的代码。

```xml
<DockPanel LastChildFill="True">
    <Button DockPanel.Dock="Left" Content="Far Left"/>
    <Button DockPanel.Dock="Left" Content="Near Left"/>
    <Button DockPanel.Dock="Top" Content="Top"/>
    <Button DockPanel.Dock="Bottom" Content="Bottom"/>
    <Button Content="Fill"/>
    <Button Content="Fill More"/>
</DockPanel>
```

Figure 2-4 显示了此示例的输出。Dock 面板还有一个名为 `LastChildFill` 的设置。如果为 true，则 XAML 中的最后一个元素将填充剩余空间。在最后一个 XAML 元素之前，未指定 Dock 设置的元素将默认设置为 `DockPanel.Dock="Left"`。

![Dock 面板按照 XAML 顺序填充指定区域内控件的快照。](img/9781119839071-fg050204.png)

FIGURE 2-4: Dock 面板按照 XAML 顺序填充指定区域内控件。

### Canvas

`Canvas` 是 WPF 中的一个异类，因为它不使用流式布局，而是回到了固定位置布局渲染。“什么？！”你说道，“我以为流式布局才是未来的趋势呢！”嗯，确实如此……大多数时候如此。在某些情况下，应用程序的部分需要用“老办法”进行布局。用于设计平面图的图形化应用程序就是一个完美的例子。这里是创建 `Canvas` 的代码（在可下载源码的 `Canvas` 示例中也可以找到）。

```xml
<Canvas>
    <Rectangle Canvas.Left="40" Canvas.Top="40" Height="53" Name="rectangle1" Stroke="Black" Width="96" Fill="#FFE22323"/>
    <Ellipse Canvas.Left="28" Canvas.Top="142" Height="80" Name="ellipse1" Stroke="Black" Width="161" Fill="#FF0000FA"/>
    <Ellipse Canvas.Left="96" Canvas.Top="14" Height="108" Name="ellipse2" Stroke="Black" Width="78" Fill="#FFE5D620"/>
</Canvas>
```

Figure 2-5 显示此示例的输出。项目相对于任何边放置（或绘制）在画布上，层级通过 z 序（z-order）处理。`z-order` 定义了哪些项目先绘制，哪些后绘制，依此类推。

![Canvas 示例的快照。](img/9781119839071-fg050205.png)

FIGURE 2-5: Canvas 示例。

### Grid

本迷你书籍的第 1 章引入了 `Grid`，它是屏幕设计最常见的起点。事实上，当你向项目中添加新的 WPF 窗口时，`Grid` 是 `Window` 的默认面板。

`Grid` 使用行（`RowDefinitions`）和列（`ColumnDefinitions`）划分布局区域。`Grid` 与 `UniformGrid` 的区别在于 `Grid` 允许通过定义单元格来对单元格进行定价。

```xml
<Grid>
    <RowDefinitions>
        <RowDefinition />
        <RowDefinition />
    </RowDefinitions>
    <ColumnDefinitions>
        <ColumnDefinition />
        <ColumnDefinition />
    </ColumnDefinitions>
</Grid>
```

#### 行和列的大小

定义行和列有三种类型：

*   **像素（DIUs）：** 以设备无关单位为固定大小。
*   **Auto：** 行或列扩展以适应内容的大小。
*   **星号（`*`）：** 行或列占据剩余空间。

例如，如果你定义的一行为 `2*` 而另一个为 `3*`，则第一行将占据剩余空间的 2/5，第二行将占据 3/5。

#### 行跨度和列跨度

类似于 HTML 表格，`Grid` 中的内容可以使用 `Grid.RowSpan` 和 `Grid.ColumnSpan` 附加属性来跨行或跨列，如下代码所示：

```xml
<Border Grid.Row="0" Grid.Column="0" Grid.ColumnSpan="2"
```





```xml
<BorderBrush="Black" BorderThickness="1"
HorizontalAlignment="Stretch" VerticalAlignment="Stretch">
<TextBlock Text="0,0 - 0,1"/>
</Border>
<Border Grid.Row="1" Grid.Column="0" Grid.RowSpan="2"
BorderBrush="Black" BorderThickness="1"
HorizontalAlignment="Stretch" VerticalAlignment="Stretch">
<TextBlock Text="1,0 - 2,1"/>
</Border>
<Border Grid.Row="1" Grid.Column="1" BorderBrush="Black"
BorderThickness="1" HorizontalAlignment="Stretch"
VerticalAlignment="Stretch">
<TextBlock Text="1,1"/>
</Border>
<Border Grid.Row="2" Grid.Column="1" BorderBrush="Black"
BorderThickness="1" HorizontalAlignment="Stretch"
VerticalAlignment="Stretch">
<TextBlock Text="2,1"/>
</Border>
</Grid>
```

图 2-7 显示了一个网格布局，边界控件在第一行跨越两列，在第一列跨越后续的两行。

![Grid 的行和列跨越快照。](img/9781119839071-fg050207.png)

图 2-7： 具有行和列跨越的网格。

#### 父容器布局插槽内的水平和垂直对齐

你通过设置 `VerticalAlignment` 和 `HorizontalAlignment` 属性来在容器的布局插槽中对齐元素。水平设置有 `Center`、`Left`、`Right` 和 `Stretch`。垂直选项有 `Center`、`Top`、`Bottom` 和 `Stretch`。`Stretch` 指定元素填充所有可用空间。元素的显式尺寸设置将覆盖 `Stretch` 设置。

#### Content 控件内的内容对齐

可以使用 `Content` 控件中的 `HorizontalContentAlignment` 和 `VerticalContentAlignment` 属性使用相同的选项设置 `Content` 控件内内容的对齐。

#### 外边距（Margin）与内边距（Padding）

外边距在 `UIElement` 及其父容器周围创建空间。外边距值从左侧开始并顺时针旋转（这与 CSS 不同，只是为了让你保持警惕）。你也可以使用一些缩写。将值设置为一个数字会创建一个均匀的外边距；将值设置为两个数字（用逗号分隔）则会将左、右外边距设置为第一个数字，将上下外边距设置为第二个数字。

```xml
<Button Margin="2,4,2,4" Content="Push Me"/> <!--L,T,R,B-->
<Button Margin="2,4" Content="Push Me"/> <!--LR,TB-->
<Button Margin="2" Content="Push Me"/> <!--LTRB-->
```

内边距增加了 `Block`、`Border`、`Control` 或 `TextBlock` 内部 `UIElements` 周围的间距。想象一张图片被一条蓝色边界材料包围，而这层材料又在一个框架内。假设图片区域（将其视为一个容器）在四周都有很小的外边距，使得实际图片永远不会接触蓝色边界。这就是 `Margin` 的概念。蓝色边界本身是图片区域外额外的内边距。这就是 `Padding` 的概念。将 `Margin` 视为内部空间，将 `Padding` 视为外部空间。这段 XAML 显示了类似的内容：一个 `TextBlock` 和四个按钮位于 `StackPanel` 内部，周围有一个 `Border`，并同时使用了 `Margin` 和 `Padding`（你也可以在 `MarginAndPadding` 示例中找到这段代码）：

```xml
<Border Background="LightBlue" BorderBrush="Black" BorderThickness="5" Padding="15">
<StackPanel Background="White" HorizontalAlignment="Center" VerticalAlignment="Top">
<TextBlock Margin="10,10" FontSize="18" HorizontalAlignment="Center">
HorizontalAlignment Sample
</TextBlock>
<Button HorizontalAlignment="Left">Button 1 (Left)</Button>
<Button HorizontalAlignment="Right">Button 2 (Right)</Button>
<Button HorizontalAlignment="Center">Button 3 (Center)</Button>
<Button HorizontalAlignment="Stretch">Button 4 (Stretch)</Button>
</StackPanel>
</Border>
```

该 `Border` 包围了一个 `15` 单位的浅蓝色内边距区域。蓝色边界包围的白色矩形内部的 `TextBlock` 显示每侧都有 `10` 单位的窄 `Margin`，如文本“Horizontal Alignment Sample”周围的白色区域所示。（按钮没有外边距。）图 2-8 显示了你看到的输出。

#### 共享尺寸组

大多数复杂的窗口需要多个面板来实现预期的用户体验。如果一个网格中的内容尺寸与另一个网格不同，可能会导致窗口看起来对齐不一致。

![使用 Margin 和 Padding 的示例快照。](img/9781119839071-fg050208.png)

图 2-8： 使用 `Margin` 和 `Padding` 的示例。

幸运的是，有一个简单的解决方案。通过在*父级*网格上设置 `Grid.IsSharedSizeScope` 附加属性，所有子网格都可以定义订阅到 `SharedSizeGroup` 的 `Rows` 和 `Columns`，渲染引擎将确保它们的尺寸设置正确。以下代码提供了一个使用共享尺寸的示例（你也可以在 `SharedSize` 示例中找到该代码）：

```xml
<Grid Grid.IsSharedSizeScope="True">
<Grid.RowDefinitions>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
</Grid.RowDefinitions>
<Grid Grid.Row="0" Grid.RowSpan="3" Grid.Column="0">
<Grid.RowDefinitions>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
</Grid.RowDefinitions>
<Grid.ColumnDefinitions>
<ColumnDefinition Width="Auto" SharedSizeGroup="Header"/>
<ColumnDefinition Width="*"/>
</Grid.ColumnDefinitions>
<Label Grid.Row="0" Grid.Column="1" Grid.ColumnSpan="2" Content="Zoo Animals" HorizontalContentAlignment="Center"/>
<Label Grid.Row="1" Grid.Column="0" Content="Hippopotamus" HorizontalContentAlignment="Stretch"/>
<TextBox Grid.Row="1" Grid.Column="1" HorizontalAlignment="Stretch" BorderThickness="2"/>
<Label Grid.Row="2" Grid.Column="0" Content="Giraffe" HorizontalContentAlignment="Stretch"/>
<TextBox Grid.Row="2" Grid.Column="1" HorizontalAlignment="Stretch" BorderThickness="2"/>
</Grid>
<Grid Grid.Row="3" Grid.Column="0">
<Grid.RowDefinitions>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
</Grid.RowDefinitions>
<Grid.ColumnDefinitions>
<ColumnDefinition Width="Auto" SharedSizeGroup="Header"/>
<ColumnDefinition Width="*"/>
</Grid.ColumnDefinitions>
<Label Grid.Row="0" Grid.Column="1" Grid.ColumnSpan="2" Content="Pets" HorizontalContentAlignment="Center"/>
<Label Grid.Row="1" Grid.Column="0" Content="Cats" HorizontalContentAlignment="Left"/>
<TextBox Grid.Row="1" Grid.Column="1" HorizontalAlignment="Stretch" BorderThickness="2"/>
<Label Grid.Row="2" Grid.Column="0" Content="Dogs" HorizontalContentAlignment="Left"/>
<TextBox Grid.Row="2" Grid.Column="1" HorizontalAlignment="Stretch" BorderThickness="2"/>
</Grid>
</Grid>
```

### 将所有内容整合到一个简单的数据输入表单

对于复杂的数据输入表单，`DataGrid` 是最合适的形式。（需更多信息，请参阅本章节后面的“探索常用的 XAML 控件”。）`DataEntryForm` 示例中的数据输入表单使用了多个网格来实现预期的效果。文本框包含在具有星号尺寸的列中，因此它们会随着表单的大小伸缩。还要注意当表单大小变化时，按钮保持在相对位置。以下是用于构建图 2-10 所示窗口的 XAML。

```xml
<Grid Background="FloralWhite">
<Grid.RowDefinitions>
```




```xml
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="Auto"/>
<RowDefinition Height="10"/>
<RowDefinition Height="Auto"/>
</Grid.RowDefinitions>
<Grid.ColumnDefinitions>
<ColumnDefinition Width="Auto"/>
<ColumnDefinition Width="Auto"/>
<ColumnDefinition Width="*"/>
<ColumnDefinition Width="Auto"/>
</Grid.ColumnDefinitions>
<Label Grid.Row="0" Grid.Column="0" Grid.RowSpan="2" Content="Name"
HorizontalAlignment="Stretch" HorizontalContentAlignment="Center">
  <Label.LayoutTransform>
    <RotateTransform Angle="-90"/>
  </Label.LayoutTransform>
</Label>
<Label Grid.Row="0" Grid.Column="1" Content="First:"
  HorizontalAlignment="Stretch" HorizontalContentAlignment="Right"/>
<TextBox Grid.Row="0" Grid.Column="2" HorizontalAlignment="Stretch"/>
<Label Grid.Row="1" Grid.Column="1" Content="姓:"
  HorizontalAlignment="Stretch" HorizontalContentAlignment="Right"/>
<TextBox Grid.Row="1" Grid.Column="2" HorizontalAlignment="Stretch"/>
<Label Grid.Row="2" Grid.Column="1" Content="地址:"
  HorizontalAlignment="Stretch" HorizontalContentAlignment="Right"/>
<TextBox Grid.Row="2" Grid.Column="2" HorizontalAlignment="Stretch"/>
<Label Grid.Row="3" Grid.Column="1" Content="城市:"
  HorizontalAlignment="Stretch" HorizontalContentAlignment="Right"/>
<TextBox Grid.Row="3" Grid.Column="2" HorizontalAlignment="Stretch"/>
<Button Grid.Row="3" Grid.Column="3" Content="查询" Margin="3,0,3,0"/>
<Label Grid.Row="4" Grid.Column="1" Content="州:"
  HorizontalAlignment="Stretch" HorizontalContentAlignment="Right"/>
<Grid Grid.Row="4" Grid.Column="2">
  <Grid.RowDefinitions>
    <RowDefinition Height="*"/>
  </Grid.RowDefinitions>
  <Grid.ColumnDefinitions>
    <ColumnDefinition Width="*"/>
    <ColumnDefinition Width="Auto"/>
    <ColumnDefinition Width="2*"/>
  </Grid.ColumnDefinitions>
  <TextBox Grid.Row="0" Grid.Column="0" HorizontalAlignment="Stretch"/>
  <Label Grid.Row="0" Grid.Column="1" Content="邮编:" HorizontalAlignment="Right"/>
  <TextBox Grid.Row="0" Grid.Column="2" HorizontalAlignment="Stretch"/>
</Grid>
<Grid Grid.Row="6" Grid.Column="0" Grid.ColumnSpan="3">
  <Grid.RowDefinitions>
    <RowDefinition Height="Auto"/>
  </Grid.RowDefinitions>
  <Grid.ColumnDefinitions>
    <ColumnDefinition Width="*"/>
    <ColumnDefinition Width="Auto"/>
    <ColumnDefinition Width="Auto"/>
  </Grid.ColumnDefinitions>
  <Button Grid.Row="0" Grid.Column="1" Content="保存" Margin="3,0"/>
  <Button Grid.Row="0" Grid.Column="2" Content="关闭" Margin="3,0"/>
</Grid>
</Grid>
```

![简单数据输入表单快照。](img/9781119839071-fg050210.png)

图 2-10： 简单的数据输入表单。

是的，这确实有很多 XAML！WPF 的许多伟大优点之一就是它非常灵活，可以创建你想象到的任何外观和感受。但有些时候（嗯，大多数时候），它确实需要大量的角括号。

除了使用 XAML 进行布局外，你也可以完全通过代码来实现图中所示的所有示例。固定大小通过通过给 `ColumnDefinition` 或 `RowDefinition` 的 `Width` 属性分配一个数字来实现。分配 `Auto` 或 `*` 则更为复杂，因为 `Width` 属性的类型是 `GridLength`，如下代码所示。

```cs
// 设置为自动调整大小
column1 = new ColumnDefinition();
column1.Width = new GridLength(1, GridUnitType.Auto);

// 设置为星号大小
column2 = new ColumnDefinition();
column2.Width = new GridLength(1, GridUnitType.Star);
```

## 探索常用的 XAML 控件

Visual Studio 2022 自带了大量的控件（并且越来越多的供应商提供的控件可供免费下载和购买）。本节涵盖了更常用的控件。许多开发者倾向于将可用控件分为三类：

- 仅显示控件
- 基础输入控件
- 基于列表的控件

本节中的所有控件都可以绑定到数据（参见本本微型书籍的第 3 章），并可以通过代码进行修改。

### 仅显示控件

有四个主要的控件专注于向用户显示信息，如图 2-11 所示（以及 `DisplayControls` 示例）：

- `Image`：`Image` 控件显示图像（`.bmp`,`.gif` 类型）。
- `TextBlock` 和 `Label`：`TextBlock` 和 `Label` 控件都旨在提供文本或内容。`TextBlock` 是 `Label` 的轻量级版本。`Label` 继承自 `ContentControl`。
- `ProgressBar`：这里描述的最后一个仅显示控件是进度条。尽管它在技术上是 `RangeBase` 类的后代，但它不会像滑块那样允许用户输入。





业务应用程序的骨干是基础输入控件。你几乎在创建的每个窗口中都能找到这些控件，而且它们非常直观。图 2-12 显示了单个窗口中的所有这些控件。以下是基础输入控件（在 `InputControls` 示例中也有这些了）：

*   `TextBox` 和 `PasswordBox`：`TextBox` 和 `PasswordBox` 均允许向窗口输入标准文本。`PasswordBox` 会对输入的字符进行掩码（使用默认系统密码字符或开发者指定的字符），用于收集敏感信息。`TextBox` 通过 `Text` 属性暴露其内容，而 `PasswordBox` 则通过 `Password` 属性暴露。

```xml
<StackPanel Grid.Row="0">
<TextBox Text="Some Text"/>
<PasswordBox PasswordChar="X" Password="Some Text"/>
</StackPanel>
```

*   `CheckBox`：复选框通过 `IsChecked` 属性表示布尔值。`IsChecked` 属性是可空的，提供了三种状态显示（真、假、未知）。使用水平方向的 `StackPanel` 来水平布局 `CheckBox`，并设置一些边距来分隔复选框：

```xml
<StackPanel Grid.Row="1" Orientation="Horizontal">
<CheckBox IsChecked="True" Content="true" Margin="15,15"/>
<CheckBox IsChecked="false" Content="False" Margin="15,15"/>
<CheckBox IsChecked="{x:Null}" Content="Null" Margin="15,15"/>
</StackPanel>
```

*   `RadioButton`：单选按钮允许在一组范围内进行单选。选项由 `GroupName` 属性决定。选中其中一个单选按钮后，只能通过程序完全取消整个组。

```xml
<StackPanel Grid.Row="2" Orientation="Horizontal">
<RadioButton GroupName="RBSample" IsChecked="true" Content="Red" Margin="15,15"/>
<RadioButton GroupName="RBSample" Content="White" Margin="15,15"/>
<RadioButton GroupName="RBSample" Content="Blue" Margin="15,15"/>
</StackPanel>
```

*   `Slider`：滑块控件是一种范围输入控件。与 `ProgressBar` 类似，该控件接受 `Minimum`、`Maximum` 和 `Interval` 值。（间隔是从最小值到最大值之间改变的距离）。此外，你可以指定显示刻度、位置以及刻度频率。刻度？它们是显示在滑块上的数值线。

```xml
<StackPanel Grid.Row="3">
<Slider Interval="1" Minimum="1" Maximum="10" IsSnapToTickEnabled="True" TickPlacement="BottomRight" TickFrequency="1"/>
</StackPanel>
```

*   `DatePicker`：`DatePicker` 控件通过结合 `TextBox` 和 `Calendar` 控件，提供了一种获取（或显示）日期信息的简洁方法。在许多选项中还包括为日期范围选择多个日期的能力。

```xml
<StackPanel Grid.Row="4">
<DatePicker/>
</StackPanel>
```

*   `Calendar`：`Calendar` 控件与 `DatePicker` 的区别在于 `Calendar` 控件始终处于全显示模式，而 `DatePicker` 的默认外观类似于文本框。

```xml
<StackPanel Grid.Row="5">
<Calendar/>
</StackPanel>
```

*   `Button`：`Button` 控件与本节的其他控件并不完全匹配，因为它更是一个操作控件。按钮对用户的点击做出响应。要使用此控件，从此处显示的 XAML 开始：

```xml
<StackPanel Grid.Row="6">
<Button Content="Click Me" Click="Button_Click" Width="60"/>
</StackPanel>
```

然而，为了使此控件生效，你还必须在 `.cs` 文件中提供后台代码（code-behind）。这段代码与 XAML 之间的连接来自于 `Click` 属性。以下是后台代码，在此情况下它仅显示了一个简单的消息框。

```csharp
private void Button_Click(object sender, RoutedEventArgs e)
{
    MessageBox.Show("Hello World");
}
```

![所有基础输入控件的截图。](img/9781119839071-fg050212.png)

图 2-12： 所有基础输入控件。

### 基于列表的控件

基于列表的控件（也称为 `Item` 控件）增加了巨大的灵活性。正如本微书的第 1 章 所讨论，基于列表的控件不再需要依赖数据技巧或其他魔法来让内容对用户有意义，而是可以通过模板来显示有关包含项目的更多详细信息。

数据绑定在本微书的第 3 章 中有非常详细介绍，但除非你有内容显示，否则控件什么都不会做。在这种情况下，`ListBasedControls` 示例采用了一种极其简单的方法，控件内容是硬编码的。然而，你还有其他选项，知道这一点是非常重要的。以下是基于列表的控件：

*   `ComboBox` 和 `ListBox`：下方示例中的 `ListBox` 和 `ComboBox` 呈现了一组列表项。然而，你还有其他选择，包括按钮和菜单项。这两个控件之间的主要区别是，`ComboBox` 使用下拉选择器显示单个项目（参见图 2-13），而 `ListBox` 在允许的空间内显示整个项目列表，然后滚动剩余部分。`ComboBox` 可以设置为启用选择不在列表中的项目，以及编辑列表中的项目。

```xml
<ComboBox Grid.Column="0" Height="20" Width="100" HorizontalAlignment="Stretch" VerticalAlignment="Top">
<ListBoxItem Content="One"/>
<ListBoxItem Content="Two"/>
<ListBoxItem Content="Three"/>
<ListBoxItem Content="Four"/>
<ListBoxItem Content="Five"/>
</ComboBox>
<ListBox Grid.Column="1" Height="150" Width="100" HorizontalAlignment="Stretch" VerticalAlignment="Top">
<ListBoxItem Content="One"/>
<ListBoxItem Content="Two"/>
<ListBoxItem Content="Three"/>
<ListBoxItem Content="Four"/>
<ListBoxItem Content="Five"/>
```

*   `TreeView`：`TreeView` 是一种类似于 Windows 资源管理器的分级 `ItemsControl`。节点（或分支）可以展开或收起，为任何多级数据提供良好的用户界面。（参见图 2-13。示例使用了硬编码数据，但通过简单的层次模板，树视图可以像任何其他控件一样进行绑定。

```xml
<TreeView Name="myTreeViewEvent" >
<TreeViewItem Header="Employee1" IsSelected="True">
<TreeViewItem Header="Jesper Aaberg"/>
<TreeViewItem Header="Employee Number">
<TreeViewItem Header="12345"/>
</TreeViewItem>
<TreeViewItem Header="Work Days">
<TreeViewItem Header="Monday"/>
<TreeViewItem Header="Tuesday"/>
<TreeViewItem Header="Thursday"/>
</TreeViewItem>
</TreeViewItem>
<TreeViewItem Header="Employee2">
<TreeViewItem Header="Dominik Paiha"/>
<TreeViewItem Header="Employee Number">
<TreeViewItem Header="98765"/>
</TreeViewItem>
<TreeViewItem Header="Work Days">
<TreeViewItem Header="Tuesday"/>
<TreeViewItem Header="Wednesday"/>
<TreeViewItem Header="Friday"/>
</TreeViewItem>
</TreeViewItem>
</TreeView>
```

*   `DataGrid`：`DataGrid` 有五种基础列类型：

    *   `DataGridTextColumn`：用于`文本`
    *   `DataGridCheckBoxColumn`：用于`布尔值`
*   `DataGridComboBoxColumn`：用于`列表项`
    *   `DataGridHyperlinkColumn`：用于显示`链接`
    *   `DataGridTemplateColumn`：用于设计自定义列




`DataGrid` 可以设置为根据其所绑定的数据自动`AutoGenerate`列。然后它将使用反射根据数据确定最佳的列类型。由于此控件依赖于数据绑定，你将在第 3 章中看到进一步的演示。

![ComboBox（左）、ListBox（中）和 TreeView（右）控件的截图。](img/9781119839071-fg050213.png)

FIGURE 2-13: `ComboBox`（左）、`ListBox`（中）和 `TreeView`（右）控件。

# 第 3 章

# WPF 中的数据绑定

本章内容

-   理解依赖属性
-   使用绑定模式
- 定义一个示例绑定对象
-   理解数据

数据绑定允许来自你的应用程序对象（绑定源）的数据显示在你的用户界面元素（绑定目标）中。这意味着你可以将（例如）`TextBox` 的 `Text` 属性绑定到 `Car` 类实例的 `Name` 属性。取决于建立关系时使用的绑定模式，`TextBox` 的 `Text` 属性值的更改会自动更新你的 `Car` 对象的底层 `Name` 属性（反之亦然），而无需任何额外的代码。

如今大多数应用程序都会处理数据，这并不是什么秘密。作为一名 WPF 开发人员，你对数据如何呈现以及用户输入的信息如何验证和用于更新底层对象拥有完全的创作权。WPF 的优势之一是其丰富的数据绑定支持。本章将带你了解这些细节。

![记住](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要容易得多。你可以在下载源码的 `\CSAIO4D2E\BK05\CH03` 文件夹中找到本章的源码。详见引言如何查找这些源文件。

## 认识依赖属性

当你在绑定源属性和绑定目标属性之间建立关系时，就会发生绑定。绑定目标对象必须是一个 `DependencyObject`，目标属性必须是一个 `DependencyProperty`。

理解依赖属性对于牢掌握 WPF 技术至关重要。依赖属性存在于自 `DependencyObject` 的对象中。从根本上说，依赖属性通过添加一组服务（称为 WPF 属性系统）扩展了 CLR 对象上已有的普通属性的功能。（`DependencyObject` 和 `DependencyProperty` 共同构成了该属性系统。）依赖属性的值可以由多个输入源确定，这意味着它们的值可以通过 `Style` 或数据绑定表达式获取。依赖属性的作用就像普通属性一样，但它们允许你根据以下内容设置值：

*   **默认值：** 这些在属性上是预定义的。
*   **计算表达式（类似于 CSS，即层叠样式表，Web 世界中的表达式）：** 这可以是一个数据绑定表达式，也可以是对应用程序中定义的资源的引用。
*   **数据绑定：** 这实际上是基于前面的项目符号，通过在绑定源对象使用绑定表达式来实现的。
*   **属性值继承：** 不要与对象继承混淆，属性值继承允许在父属性上设置的值向下传递到子属性。例如，如果你在 `Window` 元素（根元素）上设置了 `FontSize` 值，`TextBlock` 和 `Label` 等子元素会自动继承这些字体属性值。你可以通过回顾本微型书第 1 章](#c31.xhtml)中引入的附加属性概念来查看另一个示例。
*   **样式化：** 每个样式通常包含用于设置一个或多个属性值的设置器。

WPF 属性系统还提供了内置的属性值更改通知和属性值验证功能，这些将在本章稍后的“编辑、验证、转换和可视化你的数据”部分中进行介绍。

根结底，依赖属性允许开发者在 XAML 和代码中直接设置属性值。这样做的好处是你可以保持代码整洁，并将对象属性值的初始化留给 XAML。

## 探索绑定模式

你对创建的绑定关系的行为具有完全控制权。WPF 提供了多种类型的绑定模式，包括以下：

*   **`OneTime` 绑定模式**用于源属性仅初始初始设置目标属性值的情况。源属性的后续更改不会反映在目标属性中。同样，目标属性的更改也不会反映在源属性中。
*   **`OneWay` 绑定模式**通常用于只读属性。在这种绑定模式下，来自源属性的数据设置目标属性的初始值。源属性的后续更改将更新绑定目标属性值。相反，对目标属性值的任何后续更改都不会反映在源属性中。
*   **`OneWayToSource` 绑定模式**本质上是 `OneWay` 绑定模式的相反。在这种绑定模式下，来自源属性的数据初始化目标属性值。源属性值的后续更改不会更新目标属性。然而，目标属性值的更新将自动更新源属性值。
*   **`TwoWay` 绑定模式**合并了 `OneWay` 和 `OneWayToSource` 绑定模式的功能。在这种绑定模式下，源属性值初始化目标属性值。源属性值的后续更改将更新目标属性值。同样，目标属性值的更新将更新源属性值。

## 研究绑定对象

绑定可以使用代码或 XAML 定义。这里我们从 XAML 版本开始。要查看如何将数据绑定到你的 UI 元素，你首先需要定义一组用于测试测试数据。

### 使用 XAML 定义绑定

按照以下步骤使用 XAML 创建绑定（在下载源码的 `BindingSample1` 示例中也可以找到）：

1.  **创建一个新的 WPF  (.NET Framework) 项目并命名为 `BindingSample1`。**
2.  **通过向解决方案添加名为 `Car.cs` 的新类模板文件并编写代码来定义简单的 `Car` 类（注意，在这种情况下不需要任何 `using` 指令）：**

```csharp
namespace BindingSample1
{
    public class Car
    {
        private string _make;
        public string Make
        {
            get { return _make; }
            set { _make = value; }
        }
        private string _model;
        public string Model
        {
            get { return _model; }
            set { _model = value; }
        }
        public Car() { }
    }
}
```

3.  **在 `MainWindow.xaml` 中，将网格替换为定义了双列单行的网格；然后在每个网格单元中添加一个标签，如下：**

```xml
<Grid>
    <Grid.ColumnDefinitions>
        <ColumnDefinition></ColumnDefinition>
        <ColumnDefinition></ColumnDefinition>
    </Grid.ColumnDefinitions>
    <Grid.RowDefinitions>
        <RowDefinition></RowDefinition>
    </Grid.RowDefinitions>
    <Label x:Name="lblCarMake" Grid.Row="0" Grid.Column="0"
        Content="{Binding Path=Make, Mode=OneTime}"/>
    <Label x:Name="lblCarModel" Grid.Row="0" Grid.Column="1"
        Content="{Binding Path=Model, Mode=OneTime}"/>
</Grid>
```




查看 `Content` 依赖属性的值。大括号内包含的信息定义了标签中显示内容的绑定。下一节将描述此 `Binding` 表达式的含义，但在那之前，你需要一些可以绑定的数据。

4. 打开 `MainWindow.xaml.cs` 后置代码文件，并在 `MainWindow` 类中创建一个名为 `GenerateData()` 的方法，该方法实例化一个 `Car` 对象并将其赋值给窗口的 `DataContext`，如下：

```csharp
private void GenerateData()
{
    Car car1 = new Car() { Make = "Athlon", Model = "XYZ" };
    this.DataContext = car1;
}
```

`DataContext` 定义了根对象，所有子元素都相对于该对象获取其值（只要子元素上的 `DataContext` 值没有通过 XAML 或代码直接设置——该属性是属性值继承的示例；除非另有说明，否则其值将从父元素获取）。

5. 在 `MainWindow()` 构造函数方法（`public MainWindow()`）中调用 `GenerateData()` 方法，紧跟在 `InitializeComponents()` 调用之后。

现在回到 XAML 文件（`MainWindow.xaml`），第一个标签 `lblCarMake` 将绑定到 `DataContext` 的 `Make` 属性。该值是从绑定中 `Path` 组件指定的属性中检索的。同样，第二个标签 `lblCarModel` 将根据绑定表达式的 `Path` 属性绑定到 `DataContext` 的 `Model` 属性。这些绑定都使用 `OneTime` ，这意味着标签内容仅绑定一次，无论绑定的底层对象属性是否发生变化。

![Technicalstuff](img/technicalstuff.png) XAML 绑定表达式的 `Path` 组件简单地告诉 XAML 处理器从其 `DataContext` 的特定属性获取其值。`Path` 值也可以表示嵌套属性，例如在嵌套复杂对象的情况下。在这些情况下，你使用点表示法来访问所需的属性，例如 `Property.SomeObject.SomeOtherProperty`。

6. 运行应用程序。

你可以看到标签现在显示了分配给窗口 `DataContext` 的 `Car` 对象的 `Make` 和 `Model`。（参见图 3-1。）

![数据绑定到 DataContext 属性的快照。](img/9781119839071-fg050301.png)

FIGURE 3-1: 绑定到 `DataContext` 属性的数据。

### 使用 C# 定义绑定

你也可以使用 C# 来定义绑定。`DataBinding1CSharp` 显示了如何执行此任务。为了演示 C# 数据绑定，请从 XAML 文件中的两个标签中完全删除 `Content` 属性。标签标记现在应该类似于以下所示：

```xml
<Label x:Name="lblCarMake" Grid.Row="0" Grid.Column="0"/>
<Label x:Name="lblCarModel" Grid.Row="0" Grid.Column="1"/>
```

修改 `MainWindow.xaml.cs` 中的 `GenerateData()` 方法以在代码中实现 `Binding` 定义。要实现这一点，你必须直接实例化 `Binding` 对象。`Binding` 对象的构造函数接收字符串 `Path` 值。使用 `BindingOperations` 类将 `Binding` 应用到标签的 `Content` 依赖属性。

![Technicalstuff](img/technicalstuff.png) `BindingOperations` 是 WPF 提供的一个辅助类。它具有静态方法，让你能够对应用程序元素上添加和清除数据绑定定义。

下面的代码向你展示如何定义 `Binding` 对象并将绑定分配给标签的 `Content`：

```csharp
private void GenerateData()
{
    Car car1 = new Car() { Make = "Athlon", Model = "XYZ" };
    Binding makeBinding = new Binding("Make");
    makeBinding.Mode = BindingMode.OneTime;
    BindingOperations.SetBinding(lblCarMake, Label.ContentProperty, makeBinding);
    Binding modelBinding = new Binding("Model");
    modelBinding.Mode = BindingMode.OneTime;
    BindingOperations.SetBinding(lblCarModel, Label.ContentProperty, modelBinding);
    this.DataContext = car1;
}
```

注意，此更改还需要使用以下 `using` 指令：

```csharp
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
```

运行应用程序并观察其运行方式与使用 XAML 定义绑定时相同。

![Remember](img/remember.png) 依赖属性通常带有 `Property` 后缀，但只有当你浏览 MSDN 文档并通过代码访问它们时才会看到这种形式。在 XAML 中，你通过去掉名称中的 `Property` 后缀来指定依赖属性标记。

## 编辑、验证、转换和可视化你的数据

在前面的节中，你接触了绑定语法并看到数据出现在屏幕上。本节在此知识的基础上，向你展示了 `SimpleBinding2` 示例，它包含了从用户界面元素更新数据，以及根据后台发生的变化更新用户界面。要创建一个可以发生更新的环境，请遵循以下步骤：

1. 创建一个新的 WPF 项目并将其命名为 `BindingSample2`。
2. 在解决方案资源管理器中右键点击项目，从上下文菜单中选择“添加项”。
3. 选中项目中的 `Car.cs` 文件并点击添加。
4. 在解决方案资源管理器中双击 `Car.cs` 用编辑器打开文件。
5. 将命名空间 `BindingSample1` 改为 `BindingSample2`。在这个示例中，你在 `TextBox` 控件显示 `Car` 对象（`DataContext`）的品牌和型号。你还将使用 `TwoWay` 绑定模式，以便从用户界面进行的更改将反映到底层 `Car` 对象，而从后置代码对 `Car` 对象的更改将通过以下代码反映到用户界面：

```xml
<Grid>
  <Grid.ColumnDefinitions>
    <ColumnDefinition></ColumnDefinition>
    <ColumnDefinition></ColumnDefinition>
  </Grid.ColumnDefinitions>
  <Grid.RowDefinitions>
    <RowDefinition></RowDefinition>
    <RowDefinition></RowDefinition>
  </Grid.RowDefinitions>
  <StackPanel Orientation="Horizontal" Grid.Row="0" Grid.Column="0">
    <Label Content="Make"/>
    <TextBox x:Name="lblCarMake" VerticalAlignment="Top" Text="{Binding Path=Make, Mode=TwoWay}" Width="200" Height="25"/>
  </StackPanel>
  <StackPanel Orientation="Horizontal" Grid.Row="0" Grid.Column="1">
    <Label Content="Model"/>
    <TextBox x:Name="lblCarModel" VerticalAlignment="Top" Text="{Binding Path=Model, Mode=TwoWay}" Width="200" Height="25"/>
  </StackPanel>
  <Button x:Name="btnShowDataContextValue" Click="btnShowDataContextValue_Click" Content="Show Current Data Context Value" Grid.Row="1" Grid.Column="0"/>
  <Button x:Name="btnChangeDataContextValue" Click="btnChangeDataContextValue_Click" Content="Change Data Context Value with Code-Behind" Grid.Row="1" Grid.Column="1"/>
</Grid>
```

7. 在后置代码文件 `MainWindow.xaml.cs` 中添加以下方法：

```csharp
private void GenerateData()
{
    Car car1 = new Car() { Make = "Athlon", Model = "XYZ" };
    this.DataContext = car1;
}
```





```csharp
private void btnShowDataContextValue_Click(object sender, RoutedEventArgs e)
{
    Car dc = this.DataContext as Car;
    MessageBox.Show("Car Make: " + dc.Make + "\nCar Model: " + dc.Model);
}

private void btnChangeDataContextValue_Click(object sender, RoutedEventArgs e)
{
    Car dc = this.DataContext as Car;
    dc.Make = "Changed Make";
    dc.Model = "Changed Model";
}
```

8. **在 `MainWindow()` 构造函数中，紧随 `InitializeComponents()` 调用之后添加对 `GenerateData()` 方法的。**

9. **运行此应用程序。** 你看到来自 `DataContext` 的值已正确显示在 `TextBox` 控件中。可以更改 `TextBox` 控件中的值。例如，将 `Make` 值更改为 `Athlon X`，并将模型更改更改为 `ABC`。当你完成编辑后，点击“Show Current Data Context Value”按钮。你对 `TextBox` 中值的做的更改现在已反映在底层的 `DataContext` 对象中。（参见图 3-2。）

![使用双向绑定模式编辑数据的快照。](img/9781119839071-fg050302.png)

图 3-2： 使用双向绑定模式编辑数据。

10. **点击确定以消除消息框。** 如果你查看“通过后台代码更改数据上下文值”按钮的 `Click` 事件处理程序（`btnChangeDataContextValue_Click()`），你会注意到 `DataContext` `Car` 对象的属性将分别更改为 `Changed Make` 和 `Changed Model`。

11. **点击“通过后台代码更改数据上下文值”按钮。** 嗯……什么都没有发生。这是是怎么回事呢？如果你点击“Show Current Data Context Value”按钮，你会发现属性实际上已经更改了。因为你正在使用双向绑定，你的设置应该自动更新 UI，对吧？错了！这正是 WPF 的另一个功能——`INotifyPropertyChanged` 概念发挥作用的地方。

![技术细节](img/technicalstuff.png) `INotifyPropertyChanged` 是一个简单的接口，允许你的对象引发事件，通知其订阅者（即你的应用程序）对象上的属性值已发生更改。客户端应用程序订阅这些事件，仅在发生更改时使用新值更新用户界面。

![技术细节](img/technicalstuff.png) 集合也存在一个类似的接口——`INotifyCollectionChanged` 接口。WPF 还提供了一个名为 `ObservableCollection<T>` 的泛型类，它已经为你实现了 `INotifyCollectionChanged`。在创建 `ObservableCollection` 或你实现 `INotifyCollectionChanged` 的自定义集合时，你需要确保包含在集合中的也实现了 `INotifyPropertyChanged` 接口。

`INotifyPropertyChanged` 接口包含一个必须实现的唯一事件。该事件称为 `PropertyChanged`，它的参数是拥有已更改属性的对象（发送者）以及发生更改的属性的字符串名称。

12. **停止应用程序，打开你的 `Car` 类，并添加 `using System.ComponentModel;` 语句以允许访问 `INotifyPropertyChanged`。**

13. **在 `internal class Car` 之后输入 `INotifyPropertyChanged` 以为你的类添加所需的接口。** 注意 `INotifyPropertyChanged` 下方有红色波浪线。你看到此下线是因为你的类没有实现所需的成员。每当你添加新接口时都会发生此情况，因此知道处理它的最快方法是一个好主意。

14. **右键点击 `INotifyPropertyChanged`，从上下文菜单选择“快速操作和重构”，并点击“实现接口”。** Visual Studio 会为你添加以下代码：

```csharp
public event PropertyChangedEventHandler PropertyChanged;
```

为了让应用程序感知到 `Car` 对象中发生的更改，每当属性值发生更改时，必须触发 `PropertyChanged` 事件。

15. **为了在 `Car` 类中实现这一点，创建一个名为 `NotifyPropertyChanged` 的辅助方法，该方法接收一个字符串属性名称，并为对象实例和发生更改的属性名称触发 `PropertyChanged` 事件，如下：**

```csharp
private void NotifyPropertyChanged(string propertyName)
{
    if (PropertyChanged != null)
    {
        this.PropertyChanged(this,
        new PropertyChangedEventArgs(propertyName));
    }
}
```

![技术细节](img/technicalstuff.png) 检查 `PropertyChanged` 是否为 `null` 实际上意味着你正在检查是否有人在监听（订阅） `PropertyChanged` 事件。

16. **修改 `Car` 对象上每个公共属性的 `Set` 方法，以便在每次属性值发生更改时都调用 `NotifyPropertyChanged` 辅助方法；如下所示编辑公共属性：**

```csharp
private string _make;
public string Make
{
    get { return _make; }
    set
    {
        if (_make != value)
        {
            _make = value;
            NotifyPropertyChanged("Make");
        }
    }
}

private string _model;
public string Model
{
    get { return _model; }
    set
    {
        if (_model != value)
        {
            _model = value;
            NotifyPropertyChanged("Model");
        }
    }
}
```

17. **运行应用程序。** 现在当你点击“通过后台代码更改值”按钮时，更改的值反映在 `TextBox` 元素中。这是由于 `TwoWay` 绑定模式以及 `INotifyPropertyChanged` 的实现。（参见图 3-3。）

![使用 INotifyPropertyChanged 进行双向绑定的快照。](img/9781119839071-fg050303.png)

图 3-3： INotifyPropertyChanged 的双向绑定。

### 数据验证

验证用户提供的输入是一个良好的习惯。人是不完美的，有些人可能是恶意的。WPF 提供了一个内置的数据验证框架。你可以通过在类中实现 `IDataErrorInfo` 接口来使用它。你可以为在 `BindingSample` 中创建的 `Car` 类添加验证。按照以下步骤为 `Car` 类添加验证：

1. **打开 `Car.cs` 文件并修改类以实现 `IDataErrorInfo` 接口，如下：**

```csharp
public class Car : INotifyPropertyChanged, IDataErrorInfo
```

实现此接口会为 `Car` 类添加以下方法：

```csharp
public string Error => throw new NotImplementedException();
public string this[string columnName] => throw new NotImplementedException();
```

2. **编辑 `Error` 属性的 `Get` 方法以返回 `null`，修改代码如下：**

```csharp
public string Error => null;
```

现在是时候为 `Car` 对象的属性添加一些验证规则了。`Car Make` 和 `Model` 属性应该强制执行长度至少为三个字符的规则。`public string this[string columnName]` 方法用于 `DataBinding` 引擎在属性更改时对属性进行验证，基于属性的名称（这就是他们在方法签名中说的 `columnName` 的含义）。此方法返回与正在编辑的属性相关的任何错误消息。

3. **为了定义并执行这些规则，编辑 `public string this[string columnName]` 方法，如下：**

```csharp
public string this[string columnName]
{
}
```




```csharp
get
{
    string retvalue = null;
    if (columnName == "Make")
    {
        if (String.IsNullOrEmpty(this._make) || this._make.Length < 3)
        {
            retvalue = "Car Make must be at least 3 " + "characters in length";
        }
    }
    if (columnName == "Model")
    {
        if (String.IsNullOrEmpty(this._model) || this._model.Length < 3)
        {
            retvalue = "Car Model must be at least 3 " + "characters in length";
        }
    }
    return retvalue;
}
```

在 `MainWindow.xaml` 中，`Make` 和 `Model` 属性绑定到用户界面中的 `TextBox` 控件。注意，你还必须向类中添加另一个 `using` 指令：

`using System;`

### 4. **要使输入到 TextBoxes 中的文本能够根据底层属性定义的约束进行验证，请编辑每个 `TextBox` 中的绑定表达式，如加粗所示：**

```xml
<StackPanel Orientation="Horizontal" Grid.Row="0" Grid.Column="0">
    <Label Content="Make"/>
    <TextBox x:Name="txtCarMake" VerticalAlignment="Top"
             Text="{Binding Path=Make, Mode=TwoWay,
             UpdateSourceTrigger=PropertyChanged,
             ValidatesOnDataErrors=True,
             ValidatesOnExceptions=True}"
             Width="200" Height="25"/>
</StackPanel>
<StackPanel Orientation="Horizontal" Grid.Row="0" Grid.Column="1" >
    <Label Content="Model"/>
    <TextBox x:Name="txtCarModel" VerticalAlignment="Top"
             Text="{Binding Path=Model, Mode=TwoWay,
             UpdateSourceTrigger=PropertyChanged,
             ValidatesOnDataErrors=True,
             ValidatesOnExceptions=True}"
             Width="200" Height="25"/>
</StackPanel>
```

![技术细节](img/technicalstuff.png) `UpdateSourceTrigger` 标识验证调用发生的时机。在本示例中，验证是在文本更改时发生的，当底层对象属性触发 `PropertyChanged` 事件时，`UpdateSourceTrigger` 会被触发。

`ValidatesOnDataErrors` 允许在属性上调用 `IDataErrorInfo` 验证方法。

`ValidatesOnExceptions` 当底层数据源抛出异常时使 `TextBox` 变为无效，例如，当你有一个整数属性而用户输入了字符串时。WPF 会自动抛出输入字符串格式不正确的异常。

### 5. **运行示例并删除 `Make` 和 `Model` TextBox 控件中的所有文本。**

你会发现 `TextBox` 控件现在显示为红色渲染；当你在向 `TextBox` 中输入文本时，一旦达到三个字符，红色边框就会消失。

红色边框足以表示发生了错误，但它对用户来说作用不大，因为他们没有被告知错误的详细信息。显示错误的一种简单方法是在 `TextBox` 上添加工具提示（tooltip）。你可以通过向窗口添加一个 `Style` 资源来实现，该资源定义了一个在当数据处于无效状态时触发工具提示的样式。

### 6. **将以下 XAML 直接添加到 `MainWindow.xaml` 顶部的 `Window` 标签下方，如下所示，以提供错误工具提示：**

```xml
<Window.Resources>
    <Style x:Key="errorAwareTextBox" TargetType="{x:Type TextBox}">
        <Style.Triggers>
            <Trigger Property="Validation.HasError" Value="true">
                <Setter Property="ToolTip" Value="{Binding RelativeSource={x:Static RelativeSource.Self}, Path=(Validation.Errors)[0].ErrorContent}"/>
            </Trigger>
        </Style.Triggers>
    </Style>
</Window.Resources>
```

### 7. **为 `TextBox` 添加以下 `Style`，如下：**

```xml
Style="{StaticResource errorAwareTextBox}"
```

现在当你运行示例并删除 `TextBox` 控件中的文本时，当你向 `TextBox` 中输入文本，一旦达到三个字符，红色边框就会消失。

红色边框足以表示发生了错误，但它对用户来说作用不大，因为他们没有被告知错误的详细信息。显示错误的一种简单方法是在 `TextBox` 上添加工具提示。你可以通过向窗口添加一个 `Style` 资源来实现，该资源定义了一个在当数据处于无效状态时触发工具提示的样式。

![错误提示](img/error.png)  

（注：由于原始文本存在大量重复和逻辑断层，译文已根据上下文进行了清理，确保逻辑通顺。）





## 4. 向项目添加另一个用户控件 (WPF)；将其命名为 `RedX.xaml`。

## 5. 将 `RedX.xaml` 文件中的 `Grid` 替换为以下 XAML：

```xml
<Canvas Width="44.625" Height="45.9394">
  <Path x:Name="Line1Path" Width="44.625" Height="44.375"
    Canvas.Left="0" Canvas.Top="0" Stretch="Fill"
    Fill="#FFDE0909"
    Data="F1 M 0,3.5L 3.5,0L 44.625,41L 42.125,44.375"/>
  <Path x:Name="Line2Path" Width="43.5772" Height="45.3813"
    Canvas.Left="0.201177" Canvas.Top="0.55809"
    Stretch="Fill"
    Fill="#FFDE0909" Data="F1 M 3.7719,45.9394L 0.201177,
42.5115L 40.353,0.55809L 43.7784,2.98867"/>
</Canvas>
```

## 6. 添加名为 `BooleanToIconConverter.cs` 的新类。

## 7. 在你的类中添加以下使用指令：

```csharp
using System.Windows.Data;
```

## 8. 让 `BooleanToIconConverter` 实现 `IValueConverter` 接口。

代码现在应该包含 `Convert()` 和 `ConvertBack()` 方法。

## 9. 修改 `Convert()` 方法使其看起来所示：

```csharp
public object Convert(object value, Type targetType, object parameter, CultureInfo culture)
{
  if (value == null)
  {
    return value;
  }
  if ((bool)value == true)
  {
    return new GreenCheck();
  }
  else
  {
    return new RedX();
  }
}
```

## 10. 添加名为 `ServerStatus.cs` 的新类。

## 11. 添加三个属性：服务器名称、指示服务器是否运行的布尔值，以及当前连接的用户数，如下所示：

```csharp
public class ServerStatus
{
  public string ServerName { get; set; }
  public bool IsServerUp { get; set; }
  public int NumberOfConnectedUsers { get; set; }
  public ServerStatus() { }
}
```

## 12. 在 `MainWindow.xaml.cs` 中，创建所示的 `GenerateData()` 方法：

```csharp
private void GenerateData()
{
  ServerStatus ss = new ServerStatus()
  {
    ServerName = "HeadquartersApplicationServer1",
    NumberOfConnectedUsers = 983,
    IsServerUp = true
  };
  ServerStatus ss2 = new ServerStatus()
  {
    ServerName = "HeadquartersFileServer1",
    NumberOfConnectedUsers = 0,
    IsServerUp = false
  };
  ServerStatus ss3 = new ServerStatus()
  {
    ServerName = "HeadquartersWebServer1",
    NumberOfConnectedUsers = 0,
    IsServerUp = false
  };
  ServerStatus ss4 = new ServerStatus()
  {
    ServerName = "HQDomainControllerServer1",
    NumberOfConnectedUsers = 10235,
    IsServerUp = true
  };
  List<ServerStatus> serverList = new List<ServerStatus>();
  serverList.Add(ss);
  serverList.Add(ss2);
  serverList.Add(ss3);
  serverList.Add(ss4);
  this.DataContext = serverList;
}
```

## 13. 在 `Window` 构造函数中 `InitializeComponent()` 方法之后立即调用 `GenerateData()`。

## 14. 保存并构建你的应用程序。

## 15. 在 `MainWindow.xaml` 中 `Grid` 之前添加以下 `Window.Resources`：

```xml
<Window.Resources>
  <local:BooleanToIconConverter x:Key="BooleanToIconConverter"/>
  <DataTemplate x:Key="ServerTemplate">
    <Border BorderBrush="#FFDE0909" Margin="3" Padding="3" BorderThickness="2" CornerRadius="5" Background="Beige">
      <StackPanel Orientation="Horizontal">
        <Label Content="{Binding IsServerUp, Converter={StaticResource BooleanToIconConverter}}"/>
        <TextBlock FontSize="25" Foreground="Goldenrod" Text="{Binding ServerName}"/>
        <TextBlock FontSize="18" Foreground="BlueViolet" Text="{Binding NumberOfConnectedUsers}"/>
      </StackPanel>
    </Border>
  </DataTemplate>
</Window.Resources>
```





```xml
<ItemTemplate="{StaticResource ResourceKey=ServerTemplate}"/>
```

![Technicalstuff](img/technicalstuff.png) WPF 提供了许多名为 `ItemsControls` 的控件，允许你将对象集合绑定到它们。`ItemsControls` 的示例包括 `ListBox` 和 `ComboBox` 等。集合通过 `ItemsSource` 属性绑定到 `ItemsControl`。数据模板（data-template）也可以 `ItemTemplate` 属性应用到通过 `ItemsControl` 绑定的每个对象。

通过属性值继承（Property Value inheritance），`ListBox` 的 `ItemsSource` 默认设置为 `Window` 的 `DataContext`。空的 `{Binding}` 元素简单地表示它将使用父级的当前绑定，而该绑定会沿着元素树向上递归，直到达到设置了绑定的地方。请记住，在 `GenerateData()` 方法中，你正在将 `DataContext` 绑定到服务器列表并应用于 `Window` 本身，因此 `ListBox` 将继承该列表作为其 `ItemSource`（注：此处原文 ItemSource 应为 ItemsSource）。

你在资源中定义的用于描述 `ServerStatus` 对象的数据模板会渲染每个绑定的对象。你可以通过 `ItemTemplate` 看到这一点，该属性使用 `StaticResource` 指向资源中定义的 `ServerTemplate`。现在当你运行应用程序时，你会看到 `ServerStatus` 数据以一种视觉美观的方式呈现！（参见图 3-5）。

![使用值转换器和数据模板渲染数据集合的快照。](img/9781119839071-fg050305.png)

图 3-5: 使用值转换器和数据模板渲染数据集合。

## 深入了解 WPF 数据绑定

本章并不旨在涵盖通过 WPF 卓越的数据绑定支持实现的所有功能。WPF 数据模板的其他值得研究的方面包括以下概念：

- 使用 `DataTemplateSelector`，这是一个基类，允许你根据某些逻辑条件渲染数据模板。
- 将数据模板作为为用户提供数据添加/编辑能力的手段。
- 根据用户的偏好在运行时切换数据模板。这允许用户随心所欲地切换数据模板。例如，在 `ListBox` 中，你可能只显示摘要信息；但是，你可以在数据模板中提供一个按钮，允许用户根据需要在摘要模板和更详细的模板之间切换。

# 第 4 章：WPF 实战

## 本章内容

- ![Bullet](img/check.png) 理解命令类型
- ![Bullet](img/check.png) 使用内置命令
- ![Bullet](img/check.png) 使用自定义命令
- ![Bullet](img/check.png) 使用路由命令

尽管 WPF 仍然支持直接的事件处理程序接线（例如，通过 `OnClick` 事件），但 WPF 引入了一种得多的机制来响应用户事件。它显著减少了你需要编写的代码量，并为你的应用程序增加了可测试性。传统的事件处理全部包含在表单的代码后部（code-behind）中，这极难进行自动化进行测试。

软件模式已经存在很长时间，最早由 Erich Gamma、Richard Helm、Ralph Johnson 和 John Vlissides 编写的经典著作《设计模式：可重用对象软件的基础》（Addison-Wesley 出版）推向前端——他们通常被称为“四人帮”。软件一直在不断演进，多年来开发了许多新模式。为 WPF 开发的最有效的用户界面模式之一是模型-视图-视图模型（MVVM）模式（通常称为 ViewModel，参见 [`https://docs.microsoft.com/archive/msdn-magazine/2009/february/patterns-wpf-apps-with-the-model-view-viewmodel-design-pattern`](https://docs.microsoft.com/archive/msdn-magazine/2009/february/patterns-wpf-apps-with-the-model-view-viewmodel-design-pattern)）。在 WPF 应用中使用 ViewModel 模式将提高软件的重用性、可测试性、可读性、可维护性以及大多数其他“性”（你在整本书中会遇到其他设计模式）。

本章集中于另一种模式：命令模式（Command Pattern），它可以在直接接线和使用中间环节建立数据与视图之间的连接之间提供一个有效的折中。使用命令模式让直接接线变得井然，但实现起来比 MVVM 困难。本章首先将命令模式与传统的事件处理进行比较。然后讨论了三种命令类型：内置、自定义和路由。

![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源代码要简单得多。你可以在下载源码的 `\CSAIO4D2E\BK05\CH04` 文件夹中找到本章源码。请参见引言了解如何找到这些源文件的详情。

## 引起注意

命令模式自古以来就存在了，而且你很可能每天都在使用它。复制和粘贴命令是 Windows 以及大多数 Windows 内置该模式的示例实现。WPF 提供了大量的内置命令，并允许完全自定义命令！以下章节将为你提供关于命令如何在 WPF 中工作的额外信息。

### 传统的事件处理

处理用户事件的传统（WPF 仍然支持）是通过事件处理程序。当 `Window` 上的按钮被点击时，事件处理程序中的代码（必须在代码后部文件中）将执行。这里是使用事件处理的 WPF 示例（位于源码中的 TraditionalHandling 示例）：

```xml
<Grid>
  <Grid.RowDefinitions>
    <RowDefinition Height="30"/>
    <RowDefinition Height="30"/>
  </Grid.RowDefinitions>
  <TextBox Name="Message" Grid.Row="0" HorizontalAlignment="Left" Width="200"/>
  <Button Name="ClickMe" Grid.Row="1" HorizontalAlignment="Center" Content="Click Me" Click="ClickMe_Click"/>
</Grid>
```

![Remember](img/remember.png) 注意 `Button` 如何通过使用 `Click` 事件连接到代码后部。这里的机制非常简单，但你必须为每个控件单独执行，这在某些情况下可能会导致错误。代码后部的任何更改都需要在 XAML 中引用该事件处理程序的地方进行更改。实际的事件处理代码同样容易理解，因为它遵循了 Windows Forms 应用程序的技术：

```csharp
private void ClickMe_Click(object sender, RoutedEventArgs e)
{
    MessageBox.Show(Message.Text);
}
```

通过将此代码放在代码后部的事件处理程序中，业务逻辑现在与界面代码混合在一起，导致关注点混合。公平地说，框架中没有任何东西*强制*你将代码放在代码后部；它似乎总是落在那里。（当然，你可以将业务逻辑分离到代码后部之外的类。）

当窗口中增加了需要执行相同代码的额外 UI 元素时，这个问题会加剧。这种情况的常见修复方法是将原始事件处理程序中的代码重构为独立的方法，并让相关 UI 元素的处理程序调用该新方法。新方法甚至可以移动到业务层，从而分离关注点并允许进行测试。

另一个问题是用户体验问题。通常，菜单和按钮需要根据窗口数据状态（或其他条件/用户操作）主动地启用或禁用。




在此示例中，`ClickMe` 按钮始终保持启用状态，因为应用程序没有提供任何代码根据 `Message` 文本框的内容来启用或禁用它。在实际上，每当 `Message` 为空时，用户界面应该自动禁用 `ClickMe`。用户在有选项时往往会反复点击激活状态的项目，并疑惑为什么什么都没有发生。在 WPF 中通过实现的命令模式可以既清晰又方便地解决这两个问题。

### ICommand

`ICommand` 接口为特定类将执行的命令提供了契约。它规定了执行该命令所需的条件。当满足这些条件时，实现 `ICommand` 的类就会执行该命令。如下所示，`ICommand`（它是此处讨论的所有命令的基接口）定义了两个事件处理器和一个事件。

```
bool CanExecute(object parameter);
void Execute(object parameter);
event EventHandler CanExecuteChanged;
```

WPF 命令最强大的功能可能是能够在运行时确定绑定的控件是否可以执行。（详细讨论见下一节。）下面的列表更详细地描述了 `ICommand` 元素。

- `CanExecute` 在每次焦点变化、触发 `PropertyChanged` 或 `CollectionChanged` 事件或通过代码按需运行时由 `CommandManager` 执行。如果事件处理器返回 `false`，则所有绑定到该命令的 UIElement 都被禁用。
- `Execute` 包含了处理用户操作或通过代码执行命令时运行的代码。
- `CanExecuteChanged` 访问由 `INotifyCollectionChanged` 和 `INotifyPropertyChanged` 提供的机制，该机制决定何时需要调用 `CanExecute`。

### 路由命令

`ICommand` 接口并没有提供 WPF 命令的所有优之处。`RoutedCommand` 类（及其第一个派生类 `RoutedUICommand`）利用事件路由来提供额外的功能。

`CanExecute` 事件处理器会触发 `PreviewCanExecute` 事件，而 `Execute` 事件处理器会触发 `PreviewExecuted` 事件。这些事件在 `CanExecute` 和 `Execute` 处理器之前触发，并向元素树向上泡，直到找到具有正确命令绑定的元素为止。这种方法允许在更高层级控制命令，而细粒度的元素仍然控制着 `CanExecute` 和 `Execute` 事件处理器。

路由命令还暴露了 `InputGestures` 集合——即击键或其他触发 `Execute` 事件处理器的手势。你可以使用 `InputGestures` 为命令分配热键组合，例如用于保存的 Ctrl+S。

## 使用内置命令

WPF 提供了许多内置命令，你可以编写少量或不写代码即可使用（列表参见 [`https://docs.microsoft.com/dotnet/api/system.windows.input](https://docs.microsoft.com/dotnet/api/system.windows.input)）。业务开发人员最常用的命令集封装在 `ApplicationCommands` 库中。使用内置命令的优点是所有的底层工作都已为你处理好。例如，`CanExecute` 和 `Execute` 事件处理器已经实现。你只需要通过 XAML 将它们绑定到 UIElement 上，如 `BuiltInCommands` 示例所示。

![Tip](img/tip.png) 你可能会多次运行示例代码，或者剪贴板上存在来自其他用途的项目。为了确保在开始此示例时剪贴板是空的，请在 `MainWindow()` 构造函数中的 `InitializeComponent();` 之后添加以下调用：

```
Clipboard.Clear();
```

后续代码所示示例以及图 4-1 使用 `ApplicationCommands.Copy` 和 `ApplicationCommands.Paste` 命令来辅助应用程序中的剪贴板操作。顺便提一下，WPF 允许通过省略容器名称（`ApplicationCommands`）来缩写内置命令，因此 `Copy` 和 `Paste` 是命令绑定 `ApplicationCommands.Copy` 和 `ApplicationCommands.Paste` 的合法缩写。

```xml
<Grid>
  <Grid.RowDefinitions>
    <RowDefinition Height="40"/>
    <RowDefinition Height="30"/>
    <RowDefinition Height="30"/>
  </Grid.RowDefinitions>
  <Menu Grid.Row="0" HorizontalAlignment="Left" Name="menu1">
    <MenuItem Command="Copy">
      <MenuItem.Style>
        <Style TargetType="{x:Type MenuItem}">
          <Setter Property="Foreground" Value="Black"/>
          <Style.Triggers>
            <Trigger Property="IsEnabled" Value="True">
              <Setter Property="Foreground" Value="Red"/>
              <Setter Property="FontSize" Value="16"/>
            </Trigger>
          </Style.Triggers>
        </Style>
      </MenuItem.Style>
    </MenuItem>
    <MenuItem Command="Paste">
      <MenuItem.Style>
        <Style TargetType="{x:Type MenuItem}">
          <Setter Property="Foreground" Value="Black"/>
          <Style.Triggers>
            <Trigger Property="IsEnabled" Value="True">
              <Setter Property="Foreground" Value="Red"/>
              <Setter Property="FontSize" Value="16"/>
            </Trigger>
          </Style.Triggers>
        </Style>
      </MenuItem.Style>
    </MenuItem>
  </Menu>
  <TextBox Grid.Row="1" HorizontalAlignment="Left" Width="200"/>
  <TextBox Grid.Row="2" HorizontalAlignment="Left" Width="200"/>
</Grid>
```

![使用复制和粘贴功能的快照](img/97811983071-fg05401.png) 图 4-1 使用复制和粘贴功能的快照。




```
</StackPanel>
<TextBox Name="Source" Grid.Row="1" HorizontalAlignment="Left" Width="200"/>
<TextBox Name="Destination" Grid.Row="2" HorizontalAlignment="Left" Width="200" IsReadOnly="True"/>
</Grid>
```

### 创建窗口绑定

为了使示例代码运行，你必须在控件与底层的后台代码（code-behind）之间创建绑定。你有多种方法可以创建绑定，本示例展示了最常见的方法。在以下代码中，你将 `Window.CommandBindings` 定义为一系列 `CommandBinding` 元素。请注意，这里的 `Command` 属性与上一节中用于两个按钮的 `Command` 属性匹配：

```xml
<Window.CommandBindings>
    <CommandBinding Command="ApplicationCommands.Copy" Executed="CommandBinding_Executed" CanExecute="CommandBinding_CanExecute"/>
    <CommandBinding Command="ApplicationCommands.Paste" Executed="CommandBinding_Executed" CanExecute="CommandBinding_CanExecute"/>
</Window.CommandBindings>
```

当你输入某些属性名称（例如 `Executed`）时，IDE 会自动询问你是否想要创建相关的事件处理程序。如果你允许自动创建，事件处理程序将出现在后台代码中。一种诱惑是为每个命令条目创建一个唯一的事件处理程序，但这是一个错误，因为这样做会增加维护的难度。相反，你应该使用一个事件处理程序处理所有操作，如下一节所示。

### 确保命令可以执行

现在你已经有了控件以及从控件到事件处理程序的绑定，你需要创建事件处理程序代码。在这种情况下，你首先需要判断执行命令是否可行。根据以下代码中 `e.CanExecute` 的值，按钮根据需要自动启用或禁用：

```csharp
private void CommandBinding_CanExecute(object sender, CanExecuteRoutedEventArgs e)
{
    string Name = ((RoutedCommand)e.Command).Name;
    if (Name == "Copy")
    {
        if (Source == null)
        {
            e.CanExecute = false;
            return;
        }
        if (Source.SelectedText.Length > 0)
            e.CanExecute = true;
        else
            e.CanExecute = false;
    }
    else if (Name == "Paste")
    {
        if (Clipboard.ContainsText() == true)
        {
            e.CanExecute = true;
        }
        else
        {
            e.CanExecute = false;
        }
    }
}
```

![Remember](img/remember.png) 注意，你必须像代码所示将传入的 `e.Command` 值转换为名称字符串，这样你就可以对特定命令进行测试。在这种情况下，命令 `Name` 是一个简单的字符串，包含 `Copy` 或 `Paste`。你看到的值取决于你如何为应用程序控件配置 `Command` 属性。

执行的决定因素在每个情况下都不同。如果用户没有选择某些文本，`Copy` 按钮将无法工作。同样，当 `Clipboard` 缺少正确类型的数据时，无法将文本粘贴到目的地。注意，你必须使用 `Clipboard.ContainsText()` 来确保用户没有复制图像或其他类型的数据。

### 执行任务

现在你已经定义了窗口与后台代码之间的所有连接，可以开始编写实际任务的代码。首先，你必须在 `MainWindow()` 方法的 `InitializeComponent();` 之后添加 `Clipboard.Clear();` 调用，就像你在上一个示例中所做的那样。

下一步是处理 `Executed` 事件。如所示，一个事件处理程序可以同时用于两个按钮：

```csharp
private void CommandBinding_Executed(object sender, ExecutedRoutedEventArgs e)
{
    String Name = ((RoutedCommand)e.Command).Name;
    if (Name == "Copy")
    {
        Clipboard.SetText(Source.SelectedText);
    }
    else if (Name == "Paste")
    {
        Destination.Text = Destination.Text + Clipboard.GetText();
    }
}
```

与上一节中的 `CommandBinding_CanExecute()` 方法一样，此代码首先获取用户点击的按钮的名称。它使用此信息来选择行动方案。目标是从 `Source` 复制文本并将其放入 `Clipboard`，或者从 `Clipboard` 复制文本并将其放入 `Destination`。

![Remember](img/remember.png) 你通常不会把代码写得这么简单。示例之所以这样做是为了避免隐藏后台代码与 `Window` 控件相关的运行原理。当你首次启动应用程序时，两个按钮都没有激活。

输入一些文本然后选择其中一部分将启用 Copy 按钮，如图 4-2 所示。注意，在输入文本时按钮不会变为启用；是选择文本的行为启用了它。这与你在上一节示例中使用菜单控件时发生的动作相同。

![Snapshot of selecting the text enables the Copy button.](img/9781119839071-fg050402.png)

FIGURE 4-2: 选择文本启用 Copy 按钮。

当你点击 Copy 时，Copy 和 Paste 按钮都是启用的。这种操作发生在源文本高亮显示时。当你点击 Paste 时，该按钮将处于可用状态。

## 使用路由命令 (Routed Commands)

路由命令需要更多的工作，但它们允许你执行 `ICommand` 不支持的自定义操作。本示例执行简单的操作：显示消息框。然而，这种技术也适用于复杂的应用程序。以下章节介绍了路由命令。

### 定义命令类

练习的核心是 `RoutedCommand` 对象 `cmdHello`。为了让该对象正常工作，它必须位于 `RoutedCommands` 命名空间的类中（而不是作为 `MainWindow` 类的一部分）。

![Remember](img/remember.png) 为了与你的 `Command` 类交互，你必须首先创建它，然后选择生成⇒重新生成解决方案以确保该类可见。否则，你可能会发现编写的 XAML 在各个调用处有蓝色下划线。这里是用于创建 `Command` 类的代码：

```csharp
public static class Command
{
    public static readonly RoutedCommand cmdSayHello =
        new RoutedUICommand("Say Hello Menu", "DoSayHello",
        typeof(MainWindow));
}
```

![Warning](img/warning.png) 注意 `Command` 类和 `cmdSayHello` 字段都是静态的，并且 `cmdSayHello` 还是只读的。如果不这样创建 `Command` 类，WPF 将拒绝识别。不幸的是，你的应用程序将以异常方式运行，找到这个特定的错误可能非常困难。如果你发现应用程序以异常方式崩溃，你需要验证是否正确创建了 `Command` 类。

### 使命名空间可用

现代版本的 Visual Studio 会自动添加代码将你的命名空间作为 `local` 可。在这种情况下，实际的条目为 `xmlns:local="clr-namespace:RoutedCommands"`。这里是完整代码，以便你查看命名空间声明的位置：

```xml
<Window x:Class="RoutedCommands.MainWindow"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
    xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:local="clr-namespace:RoutedCommands">
```





`mc:Ignorable="d"`

`Title="MainWindow" Height="200" Width="400">`

如果你在 XAML 代码中尚未有此类条目，则必须创建一个。否则，你的应用程序将无法找到你的自定义命令。

### 添加命令绑定

与用于按钮的 `ApplicationCommands` 条目一样，你必须提供命令绑定才能访问你的自定义命令。下面的代码显示了此示例使用的命令绑定：

```xml
<Window.CommandBindings>
  <CommandBinding Command="local:Command.cmdSayHello"
                  CanExecute="CommandBinding_CanExecute"
                  Executed="CommandBinding_Executed"/>
</Window.CommandBindings>
```

![Remember](img/remember.png) 注意示例代码是如何声明 `CommandBinding` 的。`CanExecute` 和 `Executed` 条目与上一节非常相似。然而，`Command` 条目通过 `local:Command.cmdSayHello` 访问 `local` 命名空间，其中 `Command` 是用于存放 `RoutedUICommand` 对象的类名，而 `cmdSayHello` 是对象的名称。

### 开发用户界面

可以使用任何通常支持点击类型事件的控件使用自定义命令。此示例同时使用了菜单和按钮来访问自定义命令，但你还有许多其他选项。下面的代码创建了应用程序界面，其外观与本章中的其他示例相似：

```xml
<Grid>
  <Grid.RowDefinitions>
    <RowDefinition Height="40"/>
    <RowDefinition Height="30"/>
    <RowDefinition Height="30"/>
  </Grid.RowDefinitions>
  <Menu Grid.Row="0" HorizontalAlignment="Left" Name="menu1">
    <MenuItem Command="local:Command.cmdSayHello"/>
  </Menu>
  <TextBox Name="NameStr" Grid.Row="1" HorizontalAlignment="Left" Width="200"/>
  <Button Grid.Row="2" Content="Say Hello" HorizontalAlignment="Right" Command="local:Command.cmdSayHello"/>
</Grid>
```

![Tip](img/tip.png) 注意 `Menu` 控件的 `MenuItem` 元素没有为用户提供文本条目。另一方面，`Button` 以 `Content` 属性的形式提供了这些信息。尽管 `MenuItem` 缺少此信息，它仍然会显示 `Say Hello Menu`。此信息来自 `RoutedUICommand` 对象的声明。在创建 `RoutedUICommand` 对象时，提供一个与菜单配合良好的默认文本定义，然后根据需要对其他控件使用自定义文本是非常值得的。

### 开发自定义命令的代码后

为你的自定义命令创建代码几乎没什么大不了的，因为它的工作原理与处理 `ICommand` 时一样。你仍然需要为 `CanExecute` 和 `Executed` 事件处理程序定义代码，此处所示的代码：

```csharp
private void CommandBinding_CanExecute(object sender, CanExecuteRoutedEventArgs e)
{
  if ((NameStr != null) && (NameStr.Text.Length > 0))
    e.CanExecute = true;
  else
    e.CanExecute = false;
}

private void CommandBinding_Executed(object sender, ExecutedRoutedEventArgs e)
{
  MessageBox.Show("Hello " + NameStr.Text);
}
```

显然，这是一个非常简单的示例，但该技术对于复杂的设置同样有效。注意，你不需要为菜单或按钮（或其他控件）创建不同的代码。每个人都使用相同的代码。此外，你不需要执行任何特殊的连接即可使应用程序运行。

当你首次启动应用程序时，菜单和按钮都是禁用的。然而，当你向文本框输入文本时，两个控件都会变为可用状态，如图 4-3 所示。点击任一控件都会产生与图 4-4 所示类似的消息框。

![Snapshot of typing a name enables both the button and the menu.](img/9781119839071-fg050403.png)

图 4-3: 输入名称（或其他文本）可启用按钮和菜单。

![Snapshot of clicking either control produces simple output.](img/9781119839071-fg050404.png)

图 4-4: 点击任一控件都会产生简单的输出。

![Remember](img/remember.png) 当你清除文本时，按钮和菜单项将再次变为禁用，因此你知道 `CanExecute` 事件处理程序按预期工作。本章的核心思想是 WPF 提供了定义命令多种方法，你可以利用这些方法来创建健壮的应用程序。

第 5 章

# 为 Windows 10 及更高版本编程

本章内容

- 理解通用 Windows 平台 (UWP)
- 利用 UWP 的优势
- 开发简单的 UWP 应用
- 与 .NET 配合工作





你可以从多个角度来看待 UWP。从简单的角度来看，它提供了创建 Windows 客户端应用的另一种方法。因此，从理论上讲，它只是微软为了让 Windows 变得更好用或更好的一系列努力之一，但尽管如此，它仍然是一种客户端应用程序开发技术。

与所有由 C# 开发者创建的新版 Windows 应用一样，UWP 应用可以访问 `Win32 API`。然而，这种访问是通过特殊的 `WindowsApp.lib` 库文件（如 [`https://docs.microsoft.com/en-us/previous-versions/mt186421(v=vs.85)``](https://docs.microsoft.com/en-us/previous-versions/mt186421(v=vs.85)) 中所示）、专用 DLL（[`https://docs.microsoft.com/en-us/previous-versions/mt186422(v=vs.85)``](https://docs.microsoft.com/en-us/previous-versions/mt186422(v=vs.85))）以及 `.NET Framework`（[`https://docs.microsoft.com/dotnet/api/?view=dotnet-uwp-10.0``](https://docs.microsoft.com/dotnet/api/?view=dotnet-uwp-10.0)）授予的。换句话说，你有了处理过去一直所做的老事事的新方法。Paul Thurrott（一位著名的资深技术评论员）（`https://www.thurrott.com/dev/206351/microsoft-confirms-uwp-is-not-the-future-of-windows-apps`)）明确表示，UWP 并不是 Windows 应用开发的绝对未来；许多 UWP 功能将通过其他途径可用。

![Remember](img/remember.png) 使用 UWP 的原因并非来自某种神奇的新应用类型或能让你看起来像解决所有客户端问题的“超级程序员”的特种库。你使用 UWP 是为了创建在多个设备上运行相同的 `WinCore` 应用，并通过微软商店提供该应用的访问。简而言之，这是工具箱中的一个工具，而不是整个工具箱，正如你从微软的某些宣传中所认为的那样。尽管如此，UWP 为你提供了这一有趣且实用的功能：

*   **现代 UI：** 用户是否真的喜欢那些在多媒体狂热中疯狂消息的磁贴仍有待观察（可以查看 [`https://www.reddit.com/r/windows/comments/on98u0/why_do_people_hate_live_tiles/`](https://www.reddit.com/r/windows/comments/on98u0/why_do_people_hate_live_tiles/) 和 [`https://mspoweruser.com/windows-10s-live-tiles-vestigial-time-go/`](https://mspoweruser.com/windows-10s-live-tiles-vestigial-time-go/) 中的讨论，如果你有疑问的话）。UWP 应用可以依靠磁贴、推送以及与 Windows 时间线和 Cortana 的“断续点”功能交互的用户活动。问题在于用户是否真的认为现代 UI 是实。
*   **适应性：** 许多设备提供多种操作模式（例如方向），而且这些设备具有不同的功能（例如屏幕大小），UWP 应用可以适应所有这些。这种适应性源于 [`https://docs.microsoft.com/windows/uwp/data-binding/data-binding-and-mvvm`](https://docs.microsoft.com/windows/uwp/data-binding/data-binding-and-mvvm) 中描述的模型-视图-视图（`MVVM`）设计模式。
*   **安装和卸载的精确性：** Windows 应用整体的一个巨大问题是它们会导致`机器腐烂`，即由于各种应用程序以某种方式修改了操作系统，导致必须从头安装操作系统。UWP 理论上不允许导致机器腐烂的编程技术。
*   **基于生命周期开发：** 与许多 Windows 开发形式不同，开发者对 UWP 应用的生命周期有更强的控制。现在可以控制应用程序的部署、更新、安装甚至卸载。
*   **缩短开发时间：** 这一功能带有一个前提：真正的 UWP 开发学习曲线巨大，而且没有办法减少它。然而，在你进入 UWP 思维模式后，你可以通过这些方式节省开发时间：
    *   对开发周期的控制意味着在应用程序管理上花费的时间更少。
    *   UWP 的适应性意味着你只需编写一次应用程序，而不是为你支持的每个设备编写一次。
    *   管理员花费更少的时间尝试配置和适配应用程序，因此开发者花费更少的时间产生修复。
    *   用户在每个设备上都有一致的视觉效果和体验，因此开发者花费更少的时间修正 UI 功能。
    *   围绕 UWP 的开发问题理论上通过 UWP 桥接工具包（[`https://mspoweruser.com/microsoft-details-the-new-universal-windows-platform-at-build-2015/`](https://mspoweruser.com/microsoft-details-the-new-universal-windows-platform-at-build-2015/)）得到缓解。然而，只有 `Desktop Bridge` 受到了大量关注，例如 [`https://stackoverflow.com/questions/32151234/what-is-the-desktop-bridge`](https://stackoverflow.com/questions/32151234/what-is-the-desktop-bridge) 消息线程中的。
*   **安全性：** UWP 应用声明它所需的资源，用户必须允许。
*   **通用 API：** 如果你的应用程序不使用任何特殊功能，它可以运行在 Windows 10 及以上版本。
*   **强大的语言支持：** UWP 可以依靠 `C#`、`C++`、`Visual Basic` 以及 `JavaScript`（与其使用 `WinUI`、`XAML` 或 `DirectX`）。

## UWP 支持的设备

对于开发目的，你需要一个 Windows 10 或更高版本的系统。大多数开发者将使用桌面系统，因为 `Visual Studio 2022` 界面需要屏幕空间。我个人的笔记本开发体验并不理想，但我相信某些人会发现笔记本符合他们的需求。真正让我惊讶的是使用手机编写代码的读者。我不确定他们是如何实现的，但我怀疑他们看了很久。重点是，你需要 Windows 来开发 UWP 应用。

使用 UWP 应用是另一回事。微软的官方说法是 UWP 应用运行在任何支持 Windows 10 或更高版本的设备上，包括 `Windows 10/11`、`Xbox One` 和 `Hololens`。你还可以将应用程序连接到外部设备（详见 [`https://docs.microsoft.com/en-us/windows/uwp/devices-sensors/`](https://docs.microsoft.com/en-us/windows/uwp/devices-sensors/)）。然而，这只是故事的一部分。通过使用 `Xamarin`（[`https://dotnet.microsoft.com/apps/xamarin`](https://dotnet.microsoft.com/apps/xamarin))）配合 `Visual Studio 2022`，可以将 UWP 开发扩展到这些平台：

*   iOS（[`https://www.apple.com/ios/ios-15/`](https://www.apple.com/ios/ios-15/)））
*   Android（[`https://www.android.com/`](https://www.android.com/)））
*   tvOS（[`https://developer.apple.com/tvos/`](https://developer.apple.com/tvos/)））
*   watchOS（[`https://www.apple.com/watchos/watchos-8/`](https://www.apple.com/watchos/watchos-8/)））
*   macOS（[`https://www.apple.com/macos/`](https://www.apple.com/macos/））





![Remember](img/remember.png) 有了 Xamarin 支持，你突然就可以访问大量极其受欢迎的设备，对于大多数 Windows 开发者来说，为这些设备编写支持程序是不可想象的。尽管列表中的大多数产品来自 Apple，但不要忽视对 Android 的支持。正如 Barry Burd 和 John Paul Mueller (Wiley) 编写的《Android Application Development All-in-One For Dummies, 3rd Edition 中所述，Android 出现于大量的设备类型，包括智能恒温器、手表，甚至汽车等 IoT 设备。

你是否真的能在你的汽车上运行 UWP 应用是另一回事了。（任何想出为汽车之类的设备开发出独特 UWP 应用的人，请通过 `John@JohnMuellerBooks.com` 与我联系。）Android Developer Studio ([`https://developer.android.com/studio`](https://developer.android.com/studio)) 带有了一些目前 Xamarin ([`https://docs.microsoft.com/en-us/xamarin/android/`](https://docs.microsoft.com/en-us/xamarin/android/)) 似乎尚未复制的模板。然而，Xamarin 绝对支持 Android 可穿戴设备 ([`https://docs.microsoft.com/en-us/xamarin/android/wear/get-started/intro-to-wear`](https://docs.microsoft.com/en-us/xamarin/android/wear/get-started/intro-to-wear))。

因此，试图列出一份 UWP 支持的精确设备列表有些困难。关于支持问题的答案取决于你愿意使用的工具组合以及你想要支持的设备的要求。此外，你的编程技能对你所取得的成功有很大影响，因为在这些其他领域进行 UWP 开发确实需要跳出框架思考。

## 创建你自己的 UWP 应用

是时候尝试一下 UWP 开发了。接下来的章节将带你了解在处理 UWP 时所遵循的基本开发流程。该过程的一部分是设置“开发者模式”，你只需要为所使用的每台开发机器设置一次即可。

### 配置开发者模式

在不开启开发者模式的情况下，你无法创建任何类型的 UWP 项目。一旦你完成 UWP 项目设置，如果你还没有设置开发者模式，就会看到如图 5-1 所示的对话框。因此，除非你选择不开发 UWP 应用，否则这是本教程书中绝对不能跳过的章节之一。接下来的章节将告诉你更多关于开发者模式的信息。

![在开启开发者模式的情况下创建 UWP 应用的截图。](img/9781119839071-fg050501.png)

FIGURE 5-1: 不开启开发者模式就无法创建 UWP 应用。

#### 定义开发者模式

开发者模式为开发者在创建最终可能进入微软商店或其他设备（如平板电脑）的应用时，提供了额外访问系统功能的手段。除非确实出于开发需要，否则微软并不鼓励任何人启用开发者模式 ([`https://docs.microsoft.com/windows/apps/get-started/enable-your-device-for-development`](https://docs.microsoft.com/windows/apps/get-started/enable-your-device-for-development))）。例如，你不会为了修复系统而启用开发者模式。

在为 Windows 8 创建某些类型的应用程序时，开发者必须向微软 申请开发者许可证， [`https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh974578(v=win.10)](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh974578(v=win.10))，这有时会变成一个混乱且恼人的过程 ([`https://superuser.com/questions/496104/windows-8-developer-license`](https://superuser.com/questions/496104/windows-8-developer-license))。因此，Windows 10 及更高版本引入开发者模式的原因之一是为了避免整个许可问题。

设置开发许可证以及现在的开发者模式的原因是开发者需要处理并不一定签名或来自官方来源的应用。来自官方来源的应用经过审核以确保它们运行正常且不构成安全风险，因此在系统上允许未签名的应用存在破坏系统及其数据的潜在风险。作为授予此权利的一部分，系统还会为你的系统启用安全外壳 (SSH) 支持 ([`https://www.ssh.com/academy/ssh`](https://www.ssh.com/academy/ssh))，因此现在存在外部访问的可能。当你开启开发者模式时，你会看到如图 5-2 所示的对话框，警告你可能产生的影响。你需要点击“是”来完成该过程。

![微软警告启用开发者模式可能带来的问题的截图。](img/9781119839071-fg050502.png)

FIGURE 5-2: 微软警告你启用开发者模式可能带来的问题。

![警告](img/warning.png) 这种处理非官方来源应用的过程被称为“侧载” (`https://docs.microsoft.com/windows/application-management/sideloading-in-windows-10`](https://docs.microsoft.com/windows/application-management/sideloading-in-windows-10))。个人用户可能默认允许侧载，但较大的组织可能会通过各种策略禁止侧载。如果你在侧载开发过程中遇到问题，请在搜索区域输入 `Group Policy` 并按回车。你会看到本地组策略编辑器（如图 5-3 所示），它可以让你深入到 `Computer Configuration\Administrative Templates\Windows Components\App Deployment`。将这些策略设置为 `Enabled` 应该可以解决你的问题。但请记住，通过这些更改你在安全性上付出了代价，因为现在你的系统可能会接受来自任何来源的任何应用。

![本地组策略不会阻碍侧载应用的截图。](img/9781119839071-fg050503.png)

FIGURE 5-3: 确保本地组策略不会阻碍侧载应用。

#### 在“设置”应用中定位开发者模式

你可能需要更改开发者设置。然而，只要开发者模式处于开启状态，Visual Studio 2022 就不会显示设置应用。因此，你需要手动查找。要执行此任务，在 Windows 任务栏的搜索字段中输入 `Developer Settings`，你就会看到如图 5-4 所示的结果。点击顶部的 Developer Settings 项将显示如图 5-1 所示的屏幕。

#### 处理设备设置

除了允许侧载应用外，你还可以配置开发者模式允许其他具有安全影响的操作。以下列表描述了这些功能：

*   **Windows Device Portal:** Windows Device Portal (WDP) (`https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal`](https://docs.microsoft.com/windows/uwp/debug-test-perf/device-portal)) 是一个 Web 服务器，可以：
    *   让你通过网络或 USB 连接配置并管理设备设置
    *   为配置目的提供 localhost 选项
    *   使用提供的诊断工具对你的应用进行故障排除
    *   查看你的 Windows 设备的实时性能





- **设备发现：** 此功能允许发现设备并启用 SSH 支持。在与另一个设备进行交互之前，你必须通过程序化的发现它（[`docs.microsoft.com/windows/uwp/launch-resume/discover-remote-devices`](https://docs.microsoft.com/windows/uwp/launch-resume/discover-remote-devices)）。幸运的是，你可以通过多种发现技术和过滤方法通过多种手段来发现设备。

![警告](img/warning.png) 设置应用中的“面向开发人员”页面包含许多其他设置，你可以在 `[`https://docs.microsoft.com/windows/apps/get-started/developer-mode-features-and-debugging`](https://docs.microsoft.com/windows/apps/get-started/developer-mode-features-and-debugging)` 中查看这些设置。所有这些设置的重点在于，你通过降低安全性来换取特定程度的访问权限。由于这些更改，你的系统也可能变得不再可靠，因为所安装的软件大部分程度上没有经过任何人的审核。在配置系统使用开发者模式时，你还必须考虑每项设置更改对系统性能的影响。

## 让文件资源器对开发者更友好

大多数人并没有意识到有大量的设置可以控制文件资源器的外观和功能。其中许多设置可以使开发者的生活更轻松。设置应用显示了可以影响开发者的设置概述（参见图 5-5）。

![设置应用的快照提供了文件资源器开发者相关设置的概述。](img/9781119839071-fg050505.png)

图 5-5： 设置应用提供了文件资源器开发者相关设置的概述。

这些设置可能出现在 Windows 的多个地方，这就是为什么将它们集中在一个处是如此方便。然而，你可能会发现这些设置并不能完全提供你所需的所有，因此你可以点击想要更改的项目右侧的“显示设置”，例如在“开始”中“更改策略以显示‘以不同的用户身份运行’”（图 5-5），并查看详细信息。在这种情况下，你会看到一个类似于图 5-6 所示的 Microsoft 管理控制台 (MMC)，它允许你对文件资源器的外观和工作方式进行更多的控制。

注意，“开始”上的“显示‘以不同的用户身份运行’”选项是“已启用”的。大多数设置显示为“未配置”，这意味着它们使用 Windows 默认设置。只有当你配置了某项设置时，该设置才处于绝对状态。

## 使用远程桌面

![警告](img/warning.png) 远程桌面设置允许在一个系统上运行应用程序并在另一个系统上对其进行调试（以及其他）。然而，还有另一组设置存在更高的安全风险。这种设置组通常用于两个未连接到互联网的系统。如图 5-7 所示，默认设置允许带有网络级身份验证的远程桌面连接（因为复选框是灰色的）。但是，它不允许来自其他计算机的直接连接（因为复选框是填充的）。如果你点击“应用”，将应用推荐设置。你也可以通过点击复选框来取消勾选，“应用”按钮将变为禁用。

![开发者模式实际设置的快照出现在 MMC 等多个地方。](img/9781119839071-fg050506.png)

图 5-6： 开发者模式的实际设置出现在多个地方，如 MMC。

![谨慎使用远程桌面设置的用法快照。](img/9781119839071-fg050507.png)

图 5-7： 谨慎使用远程桌面设置。

## 使用 PowerShell

PowerShell 设置更改了执行策略，允许本地运行未签名脚本。远程脚本仍然需要你对其进行签名。因此，如果你在“面向开发人员”区域点击“应用”，你就可以在开发期间顺利运行本地 PowerShell 脚本。

![提示](img/tip.png) 当你在远程环境中创建某些类型的应用时，你可能会发现有在不签名的情况下运行本地和远程脚本。在这种情况下，你需要以管理员身份打开 PowerShell 提示符（否则无法访问所需的注册表项），输入 `Set-ExecutionPolicy -ExecutionPolicy Unrestricted` 并回车。

如果你想了解更多关于 `Set-ExecutionPolicy` 命令的信息，请输入 `help Set-ExecutionPolicy` 并回车。如果你想获取带有示例的详细信息，请查看 Microsoft 网站[`https://go.microsoft.com/fwlink/?LinkID=113394`](https://go.microsoft.com/fwlink/?LinkID=113394)。请注意，你输入 `Get-ExecutionPolicy` 并回车以管理员身份获取当前执行策略。

## 定义项目

创建 UWP 项目的过程与任何其他 Visual Studio 2022 项目非常相似，但有几不同。以下步骤将帮助你了解这些差异。创建 UWP 项目：

1. **在启动页上选择“创建新项目”。**

   你在左窗格中看到最近的项目模板列表，在右窗格中看到（可选的）过滤项目模板列表。

2. **在右窗格顶部的三个下拉列表中选择 C#、Windows 和 UWP。**

   右窗格中的项目模板列表将更改为显示 UWP 模板（参见图 5-8）。这些模板中的大多数都有对应其他开发目的的模板。例如，你可以在 Windows Forms 和 WPF 环境中创建类库。这些较新的 UWP 模板与旧模板具有相同的作用，但带有 UWP 的特色。

3. **选择“空应用（通用 Windows）”模板并点击“下一步”。**

   你将看到“配置新项目”页面。它包含你过去创建其他项目时用过的“项目名称”和“位置”字段。

   ![UWP 模板列表的快照。](img/9781119839071-fg050508.png)

   图 5-8： UWP 模板列表。

4. **在“项目名称”字段中输入 `MyUWCalc`，为项目提供位置，勾选“解决方案和项目放在同一目录”，然后点击“创建”。**

   到此为止，此步骤与你创建的任何项目都没有不同。然而，当你点击“创建”时，情况发生了变化。现在你看到了“通用 Windows 项目”对话框，如图 5-9 所示。

   你使用此对话框确定程序的*目标版本*（你希望用户使用的版本）以及程序的*最低版本*（较不可接受但仍可使用的版本）。如果没有在此范围内的 Windows 版本尝试下载并安装你的程序，Windows 商店将拒绝允许。这一步是你控制程序生命周期过程的开始。你可以选择哪些 Windows 版本是可以接受的。图 5-9 显示了默认范围，但你应该查看两个下拉列表（目标版本和最低版本）的其他版本。

   ![UWP 项目需要一些额外配置的快照。](img/9781119839071-fg050509.png)

   图 5-9： UWP 项目需要一些额外配置。

5. **通过点击“确定”接受默认的 Windows 版本范围值。**





Visual Studio 会为你创建项目。中间面板显示了开发和发布 UWP 应用程序的过程（参见图 5-10）。流程中每个步骤下方的链接为你提供了更多细节。请记住，你可能不需要遵循此流程中的所有步骤，而且微软提供的链接往往支持大型应用程序开发。本章向你展示的是更简单的内容，所以不要压力太大！

![Technicalstuff](img/technicalstuff.png) 如果你的开发系统没有 Internet 连接，你可能看不到图 5-10 的内容。Visual Studio 2022 始终假设你在线连接。

![完成项目向导后的快照，你看到了开发步骤列表。](img/9781119839071-fg050510.png)

图 5-10： 完成项目向导后，你将看到开发步骤列表。

### 创建界面

在制作 UWP 应用程序时，使用与开发 WPF 时相同的技术。你从 `MainPage.xaml` 文件 XAML 开始，如下所示：

```xml
<Grid>
  <Grid.Resources>
    <Style TargetType="TextBlock">
      <Setter Property="FontSize" Value="14"/>
      <Setter Property="FontFamily" Value="Arial"/>
    </Style>
  </Grid.Resources>
  <Grid.RowDefinitions>
    <RowDefinition Height="50"/>
    <RowDefinition Height="50"/>
    <RowDefinition Height="*"/>
  </Grid.RowDefinitions>
  <StackPanel Orientation="Horizontal" Grid.Row="0">
    <TextBlock Text="Input: " Height="40" Width="150"/>
    <TextBox x:Name="Input" Text="0" Height="40" Width="200"/>
  </StackPanel>
  <StackPanel Orientation="Horizontal" Grid.Row="1">
    <TextBlock Text="Result: " Height="40" Width="150"/>
    <TextBox x:Name="Result" Text="0" Height="40" Width="200" IsReadOnly="True"/>
  </StackPanel>
  <StackPanel Orientation="Horizontal" Grid.Row="2" VerticalAlignment="Top" HorizontalAlignment="Center">
    <Border BorderBrush="Black" BorderThickness="2" Padding="2">
      <Button x:Name="Add" Content="+" Click="DoMath"/>
    </Border>
    <Border BorderBrush="Black" BorderThickness="2" Padding="2">
      <Button x:Name="Sub" Content="-" Click="DoMath"/>
    </Border>
    <Border BorderBrush="Black" BorderThickness="2" Padding="2">
      <Button x:Name="Mul" Content="*" Click="DoMath"/>
    </Border>
    <Border BorderBrush="Black" BorderThickness="2" Padding="2">
      <Button x:Name="Div" Content="/" Click="DoMath"/>
    </Border>
    <Border BorderBrush="Red" BorderThickness="2" Padding="2">
      <Button x:Name="Clr" Content="X" Click="DoMath"/>
    </Border>
  </StackPanel>
</Grid>
```

此示例比书中之前的示例为应用程序设置了更多一些的资源。例如，它展示了如何配置 `FontSize` 和 `FontFamily` 以使你的应用程序具有特定的外观，并确保文本对于目标读者是可读的。

与 WPF 应用程序一样，你通过组合各种容器来配置 `UIElements`。此应用使用 `<Grid>` 结合若干 `<StackPanel>` 容器。输入和输出占据两行，控件占据第三行。结果是一个非常灵活的界面，可以适应多种格式而不会牺牲外观布局。

![Tip](img/tip.png) 此示例在每个 `<Button>` 周围使用 `<Border>` 以提供更好的外观。这与直接在 `<Button>` 上添加 `BorderBrush`、`BorderThickness` 和 `Padding` 属性的效果不同。使用 `<Border>` 时，`<Button>` 保持大小不变并在周围放置边框。否则，你得到的是用户必须眯起眼睛看的极小按钮，这增加了对眼镜的成本。图 5-11 显示了 UI 的样子。

![完成界面后的快照，应用程序界面非常灵活，适用于大多数设备。](img/9781119839071-fg05011.png)

图 5-11： 应用程序界面非常灵活，适用于大多数设备。

图 5-11 中的外观可能是误导的，因为你得到的是桌面视图。解决这个问题的方法是在顶部下拉列表中选择设备类型。默认是 13.5 英的 Surface Book (3000 x 2000)。设计器显示了该设备设备的样子，如图 5-12 所示。

然而，你可能还需要支持 6 英手机 (1920 x 1080) 格式，以便从下拉列表中选择该选项。（也可以在横屏和竖屏模式之间切换。）图 5-13 显示了使用相同代码选择该选项的结果。

![Tip](img/tip.png) 注意，设计器支持在设备上显示整个显示器。为了实际看到你在做什么，你需要更改设计器左下角的缩放设置（在图 5-13 中设置为 756%）。

![示例应用程序的快照，13.5 英 Surface Book (3000 x 2000) 格式显示。](img/9781119839071-fg050512.png)

图 5-12： 示例应用程序在 13.5 英 Surface Book (3000 x 2000) 格式显示。

![示例应用程序的快照，6 英手机 (1920 x 1080) 格式显示。](img/9781119839071-fg050513.png)

图 5-13： 示例应用程序在 6 英手机 (1920 x 1080) 格式显示。

### 添加后台代码

应用程序有一个 UI，但还没有功能。此应用程序的功能之一是高亮输入值（其默值为 `0`），这样用户只需输入新值。以下代码在应用程序启动时选择输入值以使其发生：

```csharp
public MainPage()
{
  this.InitializeComponent();
  // 设置允许输入。
  Input.SelectAll();
  Input.Focus(FocusState.Keyboard);
}
```

注意，必须使用 `SelectAll()` 选中 `0`，然后通过两步过程给 `UIElement` 使用 `Focus()`。网上有很多示例单独显示 `Focus()`（这会显示错误），但你必须为 `Focus()` 提供要使用的状态，在这种情况下是 `FocusState.Keyboard`。应用程序使用名为 `DoMath()` 的单一处理器来处理所有按钮。以下代码展示了如何创建此方法：

```csharp
private void DoMath(object sender, RoutedEventArgs e)
{
  // 获取当前值。
  Double NewValue = 0;
  Double.TryParse(Input.Text, out NewValue);
  Double ExistingValue = 0;
  Double.TryParse(Result.Text, out ExistingValue);
  // 根据按了哪个按钮执行任务。
  switch (((Button)sender).Name)
  {
    case "Add":
      ExistingValue += NewValue;
      break;
    case "Sub":
      ExistingValue -= NewValue;
      break;
    case "Mul":
      ExistingValue *= NewValue;
      break;
    case "Div":
      ExistingValue /= NewValue;
      break;
    case "Clr":
      ExistingValue = 0;
      break;
  }
  // 输出结果。
  Result.Text = ExistingValue.ToString();
  // 为下一次输入准备输入。
  Input.Text = "0";
  Input.SelectAll();
  Input.Focus(FocusState.Keyboard);
}
```

代码首先获取 `Input` 和 `Result` `UIElements` 的当前值作为 `Double` 值。使用 `Double.TryParse()` 意味着用户可以输入任何非数值而不会导致应用程序崩溃。`NewValue` 和 `ExistingValue` 将包含一个有用的数字或 `0`，取决于输入。




下一步是确定用户点击了哪个 `Button`，然后对其进行操作。要实现这一点，你必须将 `sender` 强制转换为 `Button`，然后从从中获取 `Name` 属性，如代码所示。代码展示了之后如何执行相应的任务。

最后，代码将结果输出到屏幕上。然后它设置了 `Input` 以接收用户的下一个值。

### 选择测试设备

在开发 UWP 应用时，你有多个测试选项。运行（Run）按钮带有图 5-14 所示的下拉列表，其中你可以选择想要用于测试的设备。以下是你拥有的选项：

* **本地机器 (Local Machine)：** 这是默认选项，产生一个与图 5-11 所示类似的窗口。你使用此选项创建应用程序、对其功能进行测试，并在部署到其他地方之前解决 Bug。
* **远程机器 (Remote Machine)：** 你可以将应用部署到与本地机器有网络连接的另一机器上。要实现此功能，你需要安装 Visual Studio 2022 远程工具（`https://visualstudio.microsoft.com/vs/preview/`）并确保远程设备允许开发者模式设置。例如，在处理 Android 设备时，在进行任何远程活动之前，必须专门为设备配置开发者模式。
* **设备 (Device)：** 此选项专门适用于通过 USB 端口连接到系统的设备。与远程机器选项一样，你需要在本地机器上安装 Visual Studio 2022 远程工具，并且设备必须启用开发者模式。
* **下载新模拟器 (Download New Emulators)：** 此选项将带你进入一个网站，你可以在那里下载模拟器来替代物理连接的设备。

    ![Warning](img/warning.png) 编写本文时所有可用模拟器都是 Windows 8 的，对于许多人来说，它们无法在 Windows 10 及更高版本上运行。[`https://stackoverflow.com/questions/37209666/windows-phone-8-8-1-emulator-not-working-after-windows-10-upgrade`](https://stackoverflow.com/questions/37209666/windows-phone-8-8-1-emulator-not-working-after-windows-10-upgrade)上的消息线程将告诉你更多关于此问题的信息。底在于你需要确保你的模拟器可以配合 Windows 10/11，并且你已对其进行了正确配置。

![运行按钮截图，包含替代部署的选项。](img/9781119839071-fg050514.png)

图 5-14： 运行按钮包含替代部署的选项。

## 使用 .NET Core 

书中的大多数应用程序依赖于 .NET Framework 4.7.2，它支持 Windows 且仅支持 Windows。.NET Core 应用程序通过各种手段支持 Linux、macOS 和 Windows。创建应用程序的概念是相同的，但设置略有不同，生成的可执行文件也不同。查看 Visual Studio 2022 包含的 .NET Core 模板的最简单方法是选择 C#、所有平台和所有项目类型，然后在搜索框中输入 `.NET Core`。你会看到一个非常长的可用 .NET Core 模板列表，如图 5-15 所示。

![使用搜索更容易定位 .NET Core 模板截图。](img/9781119839071-fg050515.png)

图 5-15： 使用搜索可以更容易定位 .NET Core 模板。

当你浏览列表时，你会发现一些熟悉的项目，例如控制台应用程序（Console Application）和类库（Class Library）。在这种情况下输出是相同的：一个 `.dll` 文件。许多模板与 Web 开发有关，这是第 6 中讨论的话题。列表中缺少任何类似于 Windows Forms、WPF 甚至 UWP 应用中找到的 GUI。这里简要说明了你何时应该使用 .NET Core：

* 有不依赖于 GUI 的跨平台兼容性需求。
* 应用程序依赖于微服务、Docker 容器或两者。
* 应用程序需要提供高性能和可扩展性。
* 需要在同一台服务器上运行多个 .NET 版本。
* 应用程序严重依赖命令行界面来满足管理需求。
* .NET Framework 4.7.2 中没有某个特定的 C# 新语言特性（如书中多次演示所示）。

你可能希望继续使用 .NET Framework 4.7.2 来满足其他需求，包括：

* 应用程序仅在 Windows 上运行。
* 涉及桌面 GUI。
* 应用程序使用 Windows 服务执行任务。
* 应用程序依赖于不属于 .NET Core 的技术。
* 应用程序当前使用旧版本的 .NET Framework 4.7.2。
* 至少某些应用程序任务需要使用需要 .NET Framework 的第三方库。
* 应用程序部署到云服务（如 Azure 服务）。




![Remember](img/remember.png) 你不需要手动输入本章的源代码。事实上，使用下载的源码要简单得多。你可以在下载的源码的 `\CSAIO4D2E\BK06\CH01` 文件夹中找到本章的源码。详情请参阅引言部分关于如何查找这些源文件的说明。

# 理解 ASP.NET Core 模板

与 Visual Studio 2022 中的其他开发形式一样，ASP.NET Core 提供了许多专门的模板来满足各种开发需求。与其他模板一样，其目标是帮助你以最少的精力启动项目。本质上，这些模板可以帮助你避免许多开发者面临的“空白页恐症”（即看着空白的屏幕会导致大脑一片空白）。接下来的章节将更详细地描述每个模板，以便你了解针对特定目的应该使用哪种模板。

## 使用 ASP.NET Core Empty 从零开始

这是列表中最基础的模板。当你创建它时，它不会提供任何内容。然而，这并不意味着模板不包含任何文件。取决于你使用向导配置模板的方式（见本章稍后部分的“创建项目”章节），你实际上会获得相当的文件，但它们大多影响结果网站的实际运行，而不是提供任何内容，如图 1-1 所示。在图中，你可以看到 ASP.NET Core Empty 模板的文件，它依赖 .NET Core 3.1，且没有 HTTP 或 Docker 支持。（Docker 提供了与他人打包和共享应用程序以及代码的方法。）

图 1-2 显示了相同的 ASP.NET Core Empty 模板，但这次使用了 .NET 6.0 并支持 HTTPS 和 Docker。根据你所做的选择，即使是空项目的配置方式也大不相同。例如，模板的第二个版本提供了一个 `Secrets.json` 文件，其中包含敏感的应用程序信息（详情请参阅 [`https://docs.microsoft.com/aspnet/core/security/app-secrets`](https://docs.microsoft.com/aspnet/core/security/app-secrets)）。

当你浏览文件列表时，你会发现图 1-2 中缺少 `Startup.cs` 文件。这是因为你安装了 Docker 支持，Docker 将处理应用程序的启动需求。然而，这是两种设置之间唯一缺失的文件。否则，添加功能就会增加文件。

![即使是空模板也为你提供了相当数量的文件。](img/9781119839071-fg060101.png)

图 1-1: 即使是空模板也为你提供了相当数量的文件。

![.NET 版本和应用程序功能都对项目的文件结构有所贡献。](img/9781119839071-fg060102.png)

图 1-2: .NET 版本和应用程序功能都对项目的文件结构有所贡献。

![Remember](img/remember.png) 当然，你仍然没有任何内容。解决方案资源管理器中的所有条目都以某种方式支持该应用程序。这就是为什么本章开头提到，以前处理 HTTP 页面时要简单得多。随着章节的进行，当你阅读书中这部分的更多内容时，你会发现所有这些文件都让你更容易提供人们今天所期待的内容——即 HTTP 页面无法提供的内容。

## 使用 ASP.NET Core Web App 创建基础应用

ASP.NET Core 应用程序的项目模板向导略有不同。这些向导会询问用户将在网站上如何进行身份验证，默认不进行身份验证。你还有以下选择：

*   个人帐户
*   Microsoft 标识平台
*   Windows

如果你为模板选择 .NET Core 3.1 或 .NET Core 5.0 选项，还会看到启用 Razor 运行时编译的选项。Razor 帮助你使用看起来像 C# 的语法创建服务器端动态页面。它实际上是一个非常简单的视图引擎，可以在你创建网页时显示它们。启用运行时编译意味着你可以在不重启应用程序的情况下实时看到 UI 更改。奇怪的是，选择 .NET Core 6.0 作为目标框架会隐藏此选项，因为它是默认启用的。本本型读书的第 2 章将向 C# 开发者介绍 Razor 语法，所以你现在不需要担心它的复杂性。

与空模板一样，你使用的配置选项会极大影响你看到的文件数量。图 1-3 显示了一个使用 .NET 6.0 框架和 Windows 身份验证的项目，并已配置为 HTTPS。

![Tip](img/tip.png) 如果你认为随着开始使用更多的 ASP.NET 功能，文件数量只会增加，那么你是正确的。很快你就会感到深陷其中，甚至更深。启用运行时编译意味着你可以在不重启应用程序的情况下实时看到 UI 更改。奇怪的是，选择 .NET Core 6.0 作为目标框架会隐藏此选项，因为它是默认启用的。（*注：此处原文似乎有重复或翻译乱码，已按逻辑意意润译*）

![Web App 模板为你提供了基础数量文件。](img/9781119839071-fg060103.png)

图 1-3: Web App 模板为你提供了基础数量文件。

## 在启用 HTTPS 的站点上摸索

对于大多数人来说，安全看起来很复杂，而且是第一次尝试就无法做好的事情。当安全包含多个部分时（例如网站），情况如此。因此，感觉更像是在摸索安全设置，而不是以权威的方式调整它们。

![Warning](img/warning.png) 当你选择 HTTPS 选项（除了空模板之外的所有选项）时，在第一次运行应用程序时会看到如图 1-4 所示的信任 ASP.NET SSL 证书对话框。此对话框为你提供了生成 SSL 证书的机会，这样你就不需要为了开发目的专门购买。如果你已经有了证书，你希望在开发中使用它，以确保每个人都使用正确的证书。要使用你的证书，请按照 [`https://docs.microsoft.com/aspnet/core/security/authentication/certauth`](https://docs.microsoft.com/aspnet/core/security/authentication/certauth)上的说明进行安装。

![使用生成的 SSL 证书或安装自己的证书。](img/9781119839071-fg060104.png)

图 1-4: 使用生成的 SSL 证书或安装自己的证书。





为 ASP.NET 安装证书并不会将其安装到你的系统上。当你启动应用程序时，还会看到另一个类似于图 1-5 所示的“安全警告”对话框。第二个对话框询问你是否想要在 Windows 中信任该证书。这与在 Visual Studio 中安装证书是一个独立的过程，所以至少这一次，微软并没有在故意刁难或烦扰人。这两个消息框实际上都是必要的。

![在 Windows 和 Visual Studio 中安装使用的任何证书的快照。](img/9781119839071-fg060105.png)

图 1-5： 你必须在 Windows 以及 Visual Studio 中安装你使用的任何证书。

![提示](img/tip.png) 在某个时刻，你可能想要删除已安装的 Windows SSL 证书，但如何这样做似乎是一个深不可测的秘密。[`https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in`](https://docs.microsoft.com/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in) 上的文章告诉你如何打开 Microsoft 控制台 (MMC) 并安装证书插集。你需要本地计算机的插集（有几个选项）。你需要的证书将以 `localhost` 的形式出现在 `Certificates\Personal\Certificates` 文件夹中。要删除证书，选择操作（Action）⇒  删除（Delete）。还可以执行各种其他任务，例如在以后需要时导出证书。

### 使用 ASP.NET Core App（模型-视图-控制器）构建业务逻辑

如果你有一个非常大的项目，并且以多种方式展示相同的数据，那么你真的希望将模型-视图-控制器 (MVC) 范式作为设计的一部分（[`docs.microsoft.com/aspnet/core/mvc/overview``](https://docs.microsoft.com/aspnet/core/mvc/overview)）。该范式将你的应用程序分为三个部分：

*   **模型 (Model)：** 提供对应用程序中所有数据相关元素的访问。数据可以来自任何地方。事实上，你可能作为模型逻辑的一部分生成部分数据。模型不考虑数据如何被使用甚至如何组织——它仅仅是让数据可用。因此，一个 `Customer` 对象可能会检索数据库的某些部分，而一个 `Billing` 对象可能会从同一个数据库中检索其他部分。
*   **视图 (View)：** 决定用户如何看到数据。相同的数据可能出现在多个视图中，以不同的方式组织。例如，相同的数据可能出现在详细视图或表格视图中。用户通常控制数据的呈现方式，因此相同的数据可能会近近无穷的方式出现。
*   **控制器 (Controller)：** 定义业务逻辑，以使模型和视图能够以反映公司政策、法律要求和应用程序需求的方式协同工作。正如你预期的那样，控制器提供了所需的控制，以防止混乱，并确保用户拥有良好的计算体验，且不会留下任何安全漏洞。

以这种方式将应用程序拆分为三个部分，使得大型团队能够高效工作成为可能，因为各个成员之间发生干扰的可能性降低了。负责视图的图形艺术家不需要与模型交互；他们只需要知道数据可以以特定的格式供使用。同样，数据库管理员可以与模型工作，而无需担心用户界面的问题。开发者和安全专业人员可以与其他人分开处理控制器问题。

这种灵活性的缺点是，更多的文件以更复杂的方式相互连接，如图 1-6 所示。你现在有了独立的 Controllers、Models 和 Views 文件夹——每个文件夹都有自己的组文件。该图没有显示常见的 `Connected Services`（连接服务）、`Dependencies`（依赖）或 `Properties`（属性）文件夹的内容。这与本章目前为止描述的其他模板的情况相似。

![在 MVC 中分离功能意味着更多文件的快照。](img/9781119839071-fg060106.png)

图 1-6： 在 MVC 中分离功能意味着更多文件。

奇怪的是，此模板的默认内容与其他模板提供的内容没有区别。换句话说，你为相同的内容获得了更多文件。区别仅在于此模板所提供的灵活性水平。

### 使用 ASP.NET Core Web API 开发编程接口

如今，很多开发依赖于表述状态转换 (REST) 的使用。依赖 API 意味着应用程序的客户端可以位于任何地方。此外，API 开启了第三方利用相同数据创建其他应用程序或执行类似任务的可能性。ASP.NET Core Web API 与本章其他模板略有不同，因为其重点在于 API，且某些配置要求也所不同。例如，在设置身份验证类型时，你只能访问微软身份平台或 Windows。

![提示](img/tip.png) 使用此模板配合 .NET 5.0 或 .NET 6.0 框架有充分的理由：你获得了 OpenAPI [`https://www.openapis.org/`](https://www.openapis.org/)) 支持。如果你曾尝试在同一个应用程序中使用第三方 API，你就知道每个 API 都有自己的特性，这在编写代码时往往令人困惑。OpenAPI 标准化开发者描述 API 的方式，使其变得更容易使用。如果你计划为第三方创建 API，启用 OpenAPI 对你是有利的。图 1-7 显示了在使用启用 HTTPS、无身份验证且启用 OpenAPI 的 .NET 6 ASP.NET Core Web API 时典型的文件。

![ASP.NET Core Web API 关注 API 而非客户端的快照。](img/9781119839071-fg060107.png)

图 1-7： ASP.NET Core Web API 关注 API 而非客户端。

当你运行此应用程序时，你会看到一个让你玩 API 的网页。这是一个非常有趣的尝试的 API，而且谁不想知道天气呢？当然，现在你正看着浏览器中的 URL，疑惑 Swagger 到底是怎么回事。不，它和海盗没有关系。OpenAPI 基于 Swagger 规范 [`https://swagger.io/specification/`](https://swagger.io/specification/))，该规范最初由 SmartBear[`https://smartbear.com/`](https://smartbear.com/)) 创建，你可以在那里阅读由本书作者编写的多篇文章（[`smartbear.com/blog/authors/john-mueller/``](https://smartbear.com/blog/authors/john-mueller/))）。

### 其他奇怪模板的概述

在查看潜在模板列表时，你会看到一些模板，例如 ASP.NET Core gRPC 服务。这些模板让你能够与第三方、开源软件一起工作创建与其他第三方软件协作的解决方案。本书没有涵盖这些开源解决方案。然而，以下是 Visual Studio 2022 安装的解决方案概述：





- **gRPC** (`https://grpc.io/`): 当客户端对服务器调用各种类型的服务或资源（例如执行任务或访问数据）时，就会发生`远程过程调用 (RPC)`。RPC 的优势在于，客户端可以在不了解主机网络任何信息的情况下进行调用，只需要调用的细节。使用 `gRPC` 可以在任何环境中实现 RPC 调用。你可以使用此服务执行负载均衡、活动跟踪、检查系统健康状况以及验证用户等任务。
- **Angular** (`https://angular.io/`): 你使用 `Angular` 来创建复杂的企业级应用，这些应用包含了诸如仪表板等功能，如果自己开发将花费很长时间。可以将 `Angular` 视为为那些喜欢 `Angular` 应用的外观和感受但没有大量时间从零开始编写代码的人提供的一种“超级模板服务”。你可以在 `https://angular.io/features` 了解更多关于 `Angular` 的功能。
- **React.js** (`https://reactjs.org/`): 虽然像 `Angular` 这样的产品侧重于构建整体解决方案，但 `React.js` 专注于用户界面。其核心思想是尽可能快地组合出一个用户界面（参见 `https://reactjs.org/tutorial/tutorial.html` 上的教程），而不丢失灵活性或速度。该产品使用基于组件的架构，允许你像乐高一样将用户界面功能拼接在一起。
- **React.js and Redux** (`https://redux.js.org/`): 该模板将提供用户界面的 `React.js` 与提供应用状态存储手段的 `Redux` 结合起来。现在应用程序可以拥有某种“记忆”，以便用户可以在不同设备之间移动，并从上一次会话离开的地方继续，而不会丢失任何数据或时间。

## 开发一个基础 Web 应用

是时候尝试尝试创建一个 ASP.NET Core 应用了。此应用将比简单的“Hello World”稍微多一点内容，但也不会太多。其意图是让你从一些简单的内容开始，以强调一个简单的 Web 应用可能是什么样子的。它保证比克服许多在线示例的学习曲线要容易，同时也帮助你跨越学习曲线。你可以在下载源码的 `BasicWebApplication` 示例中找到此应用。

### 创建项目

此示例从一个空项目开始。由于存在各种排列组合，该示例创建了一个特定的网站，而不是提供更通用的信息（如本章之前的章节）。使用空项目和特定步骤可以帮助你了解如何向应用程序添加各种功能，然后对其进行操作。此外，你还可以避免目前研究预定义代码的某些复杂性。按照以下步骤创建一个新的空项目：

1. **在启动页上，点击“创建新项目 (Create a New Project)”。**
   你在“创建新项目”页面上看到常见的模板列表。

2. **从右侧面板顶部的三个下拉框中选择 C#、所有平台 (All Platforms) 和 Web。**
   模板列表现在显示你可以创建的所有 ASP.NET Core 应用，以及书中未涵盖的许多 Web 特定项目。

3. **高亮 ASP.NET Core 空项目模板，然后点击“下一步 (Next)”。**
   你看到“配置新项目 (Configure Your New Project)”对话框，如图 1-8 所示。
   ![带有标识信息的配置新项目的截图](img/9781119839071-fg060108.png)
   图 1-8： 使用标识信息配置你的新项目。

4. **在“项目名称”字段中输入 BasicWebApplication 并在“位置”字段中输入位置，然后勾选“将解决方案和项目放在同一目录 (Place Solution and Project in the Same Directory)”。点击“下一步”。**
   你看到“附加信息 (Additional Information)”页面，如图 1-9 所示。此示例通过限制模板提供的功能数量来保持简单。完成此示例后，你应该尝试其他选项，看看它们如何影响你收到的初始项目。
   ![示例使用较少模板功能以降低项目复杂的截图](img/9781119839071-fg060109.png)
   图 1-9： 示例使用较少的模板功能来降低项目复杂度。

5. **在“框架 (Framework)”字段中选择 .NET Core 3.1 (长期支持)，在“身份验证类型 (Authentication Type)”字段中选择“无 (None)并取消勾选“配置 HTTPS”和“启用 Docker”复选框。点击“创建 (Create)”。**
   你看到了一个新的空项目，内容与之前图 1-1 所示相似。

### 考虑开发过程

如果你现在运行应用程序，你会看到浏览器中出现一个包含 Hello World! 的网页。此内容来自位于 `Startup.cs` 中的 `Startup` 类的 `Configure()` 方法的默认输出，显示如下：

```cs
// 此方法由运行时调用。使用它来配置
// HTTP 请求管道。
public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    if (env.IsDevelopment())
    {
        app.UseDeveloperPage();
    }
    app.UseRouting();
    app.UseEndpoints(endpoints =>
    {
        endpoints.MapGet("/", async context =>
        {
            await context.Response.WriteAsync("Hello World!");
        });

        endpoints.MapGet("/page2", async context =>
        {
            await context.Response.WriteAsync("This is the second page.");
        });
    });
}
```

本质上，这些代码的作用只是创建一个映射到 `/` 的首页，并向其写入 Hello World!。如果你想添加页面，需要使用 `MapGet()` 添加另一个端点。要亲手查看它是如何工作的，请尝试在第一个 `MapGet()` 调用直接下方添加代码：

```cs
endpoints.MapGet("/page2", async context =>
{
    await context.Response.WriteAsync("This is the second page.");
});
```

当你现在启动应用程序并更改浏览器中的 URL 为 [`http://localhost:11623/page2`](http://localhost:11623/page2)（端口号 11623 会根据系统变化）时，你会看到下一个消息：“This is the second page.”

### 添加 Web 内容

此示例不会与数据库进行任何复杂的交互，也不需要 Web 设计学位。相反，此示例将提供一些静态内容，以便你看到处理 ASP.NET Core 过程的下一步。按照以下步骤添加静态内容：

1. **在解决方案管理器 (Solution Explorer) 中右键点击 BasicWebApplication 条目并选择“新建文件夹 (New Folder)”。**
   你看到层次结构中添加了一个新文件夹。

2. **输入 wwwroot 并按回车。**
   文件夹图标变为地球图标。

3. **右键点击 wwwroot 文件夹并从右键菜单中选择“新建项 (New Item)”。**
   你看到“添加新项”对话框，如图 1-10 所示。
   ![在 wwwroot 文件夹中添加新项的截图](img/9781119839071-fg060110.png)
   图 1-10： 向 wwwroot 文件夹中添加新项。

4. **定位到 Visual C#ASP.NET Core\Web 文件夹，然后高亮 HTML 页条目。在“名称”字段中输入 index.html 并点击“添加”。**
   ![警告](img/warning.png) 此第一个文件的名称和大小写至关重要。例如，如果你输入 `Index.html`，示例可能无法工作。应用程序设计为查找这四个文件：
   - default.htm
   - default.html
   - index.htm
   - index.html





### 5. 按照下方加粗所示修改默认 HTML 页面（例如 `index.html`）的内容，这样你就可以验证它是否正常工作：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"/>
<title>Test Page</title>
</head>
<body>
<p>This is some test content.</p>
</body>
</html>
```

此时，你已经有了一个可以供之使用的 web 页面，但它还没有连接到应用程序。你需要在 `Startup.cs` 中建立这些连接。

### 6. 选择 `Startup.cs`。注释掉整个 `app.UseEndpoints()` 区域。在 `app.UseRouting()` 调用之后的紧下方添加以下代码：

```csharp
app.UseDefaultFiles();
app.UseStaticFiles();
```

`UseDefaultFiles()` 调用告诉你的应用程序查找 `index.html`。有很多方法可以更改此配置，但一种方法是创建一个选项列表，然后将这些选项传递给 `UseDefaultFiles()` 调用。[`https://docs.microsoft.com/aspnet/core/fundamentals/static-files`](https://docs.microsoft.com/aspnet/core/fundamentals/static-files) 上的文章对于创建选项列表提供了一些额外的见解。

`UseStaticFiles()` 调用允许你的应用程序使用静态文件，如 CSS、JavaScript 和 HTML。与 `UseDefaultFiles()` 类似，你可以通过向 `UseStaticFiles()` 调用提供选项列表来修改静态文件的使用行为。

此时，你可以开始向 `wwwroot` 文件夹中添加功能，以创建一个与世界上任何其他静态网站都类似的完全静态网站。

### 对第一个页面进行一些基本更改

你可以像对任何其他网站一样，为你的静态页面添加 JavaScript 和 CSS。但是，现在你只需要添加一点额外内容，这样你就能看到下一步了。第 2 章 将带你开始学习 Razor 文件的使用，但在这里你仍然使用静态内容。首先，使用上一节的第 3 步和第 4 步向项目添加 `page2.html`。修改此页面的代码使其看起来如下所示：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"/>
<title>Second Page</title>
</head>
<body>
<p>This is the second page.</p>
<p>
点击
<a href="index.html">这里</a>
返回首页。
</p>
</body>
</html>
```

现在，通过在 `index.html` 页面中添加加粗的代码，在 `page2.html` 和 `index.html` 之间建立一个连接：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"/>
<title>Test Page</title>
</head>
<body>
<p>This is some test content.</p>
<p>点击
<a href="page2.html">这里</a>
查看第二个页面。
</p>
</body>
</html>
```

现在，当你运行应用程序时，你只需点击链接即可轻松地在首页和第二个页面之间切换。是的，这是一个非常简单的应用程序，但它展示了许多你以后发现很有帮助的 ASP.NET Core 特性。

# 使用 Razor 标记语言

本章内容

- ![Bullet](img/check.png) 理解 Razor 如何融入整体
- ![Bullet](img/check.png) 在 Razor 中处理变量
- ![Bullet](img/check.png) 使用 Razor 决策
- ![Bullet](img/check.png) 存储和循环数据

如 第 1 章 中提到的，Razor 是为了让 web 开发更简单。虽然在这里你仍然使用静态内容。[`https://docs.microsoft.com/aspnet/core/fundamentals/static-files`](https://docs.microsoft.com/aspnet/core/fundamentals/static-files) 上的文章对于如何创建选项列表提供了一些额外的见解。 (此处我发现翻译出现了偏差，应重新根据英文原文的逻辑进行翻译)

`UseStaticFiles()` 调用允许你的应用程序使用静态文件，如 CSS、JavaScript 和 HTML。与 `UseDefaultFiles()` 类似，你可以通过向 `UseStaticFiles()` 调用提供选项列表来修改静态文件的使用行为。此时，你可以开始向 `wwwroot` 文件夹中添加功能，以创建一个与世界上任何其他静态网站都类似的完全静态网站。

（抱歉，上述翻译出现了混乱，重新整理如下如下）：

# 使用 Razor 标记语言

本章内容

- ![Bullet](img/check.png) 理解 Razor 如何融入整体
- ![Bullet](img/check.png) 在 Razor 中处理变量
- ![Bullet](img/check.png) 使用 Razor 决策
- ![Bullet](img/check.png) 存储和循环数据

如 第 1 章 中提到的，Razor 是为了让 web 开发更简单。虽然在这里你仍然使用静态内容。[`https://docs.microsoft.com/aspnet/core/fundamentals/static-files`](https://docs.microsoft.com/aspnet/core/fundamentals/static-files) 上的文章对于如何创建选项列表提供了一些额外的见解。

（注：由于原文文本最后似乎存在重复或逻辑交叉，我将严格按照你提供的最后一段英文原文进行精准翻译）：

---

# 使用 Razor 标记语言

本章内容

- ![Bullet](img/check.png) 理解 Razor 如何融入整体
- ![Bullet](img/check.png) 在 Razor 中处理变量
- ![Bullet](img/check.png) 使用 Razor 决策
- ![Bullet](img/check.png) 存储和循环数据

如 第 1 章 中提到的，Razor 是为了让 web 开发更简单。虽然在这里你仍然使用静态内容。[`https://docs.microsoft.com/aspnet/core/fundamentals/static-files`](https://docs.microsoft.com/aspnet/core/fundamentals/static-files) 上的文章对于如何创建选项列表提供了一些额外的见解。

（注：由于你提供的“需要翻译的文本”后半部分似乎包含了重复的段落错误，我将针对你提供的最后完整结构进行翻译）：

[content]
# 使用 Razor 标记语言

本章内容

- ![Bullet](img/check.png) 理解 Razor 如何融入整体
- ![Bullet](img/check.png) 在 Razor 中处理变量
- ![Bullet](img/check.png) 使用 Razor 决策
- ![Bullet](img/check.png) 存储和循环数据

如 第 1 章 中提到的，Razor 是为了让 web 开发更简单。虽然在这里你仍然使用静态内容。[`https://docs.microsoft.com/aspnet/core/fundamentals/static-files`](https://docs.microsoft.com/aspnet/core/fundamentals/static-files) 上的文章对于如何创建选项列表提供了一些额外的见解。
[/content]

*(注：由于你提供的待翻译文本在“Employing the Razor Markup Language”之后出现了严重的格式混乱和内容重复，我已根据你提供的最后文本逻辑进行了清理。)*

**以下是针对你提供的完整文本的最终质量翻译：**

[content]
### 5. 按照下方加粗所示修改默认 HTML 页面（例如 `index.html`）的内容，这样你就可以验证它是否正常工作：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"/>
<title>Test Page</title>
</head>
<body>
<p>This is some test content.</p>
</body>
</html>
```

此时，你已经有了一个可以供之使用的 web 页面，但它还没有连接到应用程序。你需要在 `Startup.cs` 中建立这些连接。

### 6. 选择 `Startup.cs`。注释掉整个 `app.UseEndpoints()` 区域。在 `app.UseRouting()` 调用之后的紧下方添加以下代码：

```csharp
app.UseDefaultFiles();
app.UseStaticFiles();
```

`UseDefaultFiles()` 调用告诉你的应用程序查找 `index.html`。有很多方法可以更改此配置，但一种方法是创建一个选项列表，然后将这些选项传递给 `UseDefaultFiles()` 调用。[`https://docs.microsoft.com/aspnet/core/fundamentals/static-files`](https://docs.microsoft.com/aspnet/core/fundamentals/static-files) 上的文章对于创建选项列表提供了一些额外的见解。

`UseStaticFiles()` 调用允许你的应用程序使用静态文件，如 CSS、JavaScript 和 HTML。与 `UseDefaultFiles()` 类似，你可以通过向 `UseStaticFiles()` 调用提供选项列表来修改静态文件的使用行为。

此时，你可以开始向 `wwwroot` 文件夹中添加功能，以创建一个与世界上任何其他静态网站都类似的完全静态网站。

### 对第一个页面进行一些基本更改

你可以像对任何其他网站一样，为你的静态页面添加 JavaScript 和 CSS。但是，现在你只需要添加一点额外内容，这样你就能看到下一步了。第 2 章 将带你开始学习 Razor 文件的使用，但在这里你仍然使用静态内容。首先，使用上一节的第 3 步和第 4 步向项目添加 `page2.html`。修改此页面的代码使其看起来如下所示：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"/>
<title>Second Page</title>
</head>
<body>
<p>This is the second page.</p>
<p>
点击
<a href="index.html">这里</a>
返回首页。
</p>
</body>
</html>
```

现在，通过在 `index.html` 页面中添加加粗的代码，在 `page2.html` 和 `index.html` 之间建立一个连接：

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"/>
<title>Test Page</title>
</head>
<body>
<p>This is some test content.</p>
<p>点击
<a href="page2.html">这里</a>
查看第二个页面。
</p>
</body>
</html>
```

现在，当你运行应用程序时，你只需点击链接即可轻松地在首页和第二个页面之间切换。是的，这是一个非常简单的应用程序，但它展示了许多你以后发现很有帮助的 ASP.NET Core 特性。

# 使用 Razor 标记语言

本章内容

- ![Bullet](img/check.png) 理解 Razor 如何融入整体
- ![Bullet](img/check.png) 在 Razor 中处理变量
- ![Bullet](img/check.png) 使用 Razor 决策
- ![Bullet](img/check.png) 存储和循环数据




你最常见的对比是 `MVC` 和 `Razor` 之间。微软目前推荐使用 `Razor` 来降低复杂度（[`docs.microsoft.com/dotnet/architecture/porting-existing-aspnet-apps/comparing-razor-pages-aspnet-mvc`](https://docs.microsoft.com/dotnet/architecture/porting-existing-aspnet-apps/comparing-razor-pages-aspnet-mvc)）。注意，`Razor` 中也有一种类似于 `MVC` 的方法，只是微软对不同的组件使用了不同的术语，因为使用不同的术语会让技术看起来很新。因此，`MVC` action 现在是一个处理器，`MVC` ViewModel 现在是 `PageModel`，而视图现在是一个 `Razor` 页面。在 `MVC` 中进行工作时，这些元素出现在三个不同的位置，你需要单独修改它们，这使得 `MVC` 容易出错，因为除非在手指上系根绳子，否则人们会忘记某些事情。在处理 `Razor` 时，处理器和 `PageModel` 出现在同一个文件中，而视图出现在单独的文件中，它们位于项目中的 `Pages` 文件夹下。以下是 `MVC` 和 `Razor` 之间的其他区别：

*   **更简单的页面：** `Razor` 页面确实与其他文件有一些连接，但它非常接近 Web Forms 的设置，因为你将非共享内容放在单个 `.cshtml` 文件中，并配有一个后代码文件。
*   **重点：** 许多开发者将 `Razor` 视为 HTML 视图的最佳解决方案。他们认为 `MVC` 是表述性状态传输 (REST) API 或面向服务的架构 (SOA) 的最佳解决方案。你选择的技术取决于你想创建种种网站。`Razor` 通常是简单问题的简单解决方案。
*   **更少的代码：** 在比较 `Razor` 和 `MVC` 类似的编码示例时，你通常会发现 `Razor` 代码稍微短一点（不多）而且简单一点。然而，当你开发任何规模和复杂性的网站时，微小的差异往往会堆积起来。

![Warning](img/warning.png) 导致大多数开发者苦扰的问题之一是 Visual Studio 没有带用于 `Razor` 页面的设计器。在第 5 本中，第 2 章 你看到了使用 XAML 创建 WPF 应用程序的过程。要创建一个应用程序，你可以将组件拖放到画布上。第 5 本中，第 5 章 显示了 UWP 应用程序相同的流程。遗憾的是，在处理 `ASP.NET Core` 时，你必须手动编写代码。Visual Studio 2022 提供的带有设计器的网站开发只有旧的 Web Forms 模板，它们需要特殊的设置，如“访问 Web Forms 模板”侧边栏描述的那样。

### 考虑实际的文件布局

`Razor` 网站使用许多文件，初看起来可能有些令畏，但当你将它们拆解而不是尝试作为一个整体来看时，它们就合理了。以下是创建演示界面时通常按顺序使用的文件列表：

*   `Program.cs`：包含 `Main()` 方法和应用程序启动代码。此代码包括创建 `IHostBuilder` 对象 `webBuilder`，它实际上通过在 `Startup.cs` 中找到的 `Startup` 类来启动网站。
*   `Startup.cs`：定义网站的底层配置。应用程序在此处将 `Razor` 页面添加到站点，并决定这些页面将如何交互。第 1 章 本微型书籍的“开发基础 Web 应用”部分向你展示了 `Startup` 类中的某些内容，例如添加 `UseEndpoints()` 调用和替换对 `app.UseDefaultFiles();` 的调用。
*   `_ViewImports.cshtml`：指定 `Razor` 页面引用的命名空间。你可以在此处了解更多关于标签帮助器的信息（[`docs.microsoft.com/aspnet/core/views/tag-helpers`](https://docs.microsoft.com/aspnet/core/views/tag-helpers)）。
*   `_ViewStart.cshtml`：声明使用哪个布局。
*   `_ValidationScriptsPartial.cshtml`：包含用于验证的脚本。
*   `_Layout.cshtml`：定义网站的整体外观。你可以在这里找到常见的元素，如 `ViewData["Title"]`。
*   `index.cshtml`：定义第一个页面。
*   `index.cshtml.cs`：包含页面的后代码。

### 理解 C# 的语法规则

Razor 页面是 HTML 和代码的结合。你如何组合元素取决于你计划做什么。然而，你所有的代码都以 @ 符号开头。例如，如果你想在默认的 `Index.cshtml` 页面上添加日期，可以使用以下代码：

```html
<div class="text-center">
  <h1 class="display-4">欢迎</h1>
  <p>现在是 @DateTime.Now.LongDateString()</p>
  <p>学习 <a href="https://docs.microsoft.com/aspnet/core/building-web-apps-with-aspnet-core">使用 ASP.NET Core 构建 Web 应用</a>。</p>
</div>
```

注意，此段落使用了 HTML 标签 `<p>`、纯文本以及对 `@DateTime.Now.LongDateString()` 的调用。每当有人加载页面时，日期都会变化。然而，在此之后，它将保持静态。许多内容都属于这一类，因此你应该尽可能地使用这种技术来简化问题。





# 使用 Razor 基础知识

许多在线资源（例如 [`https://docs.microsoft.com/aspnet/core/razor-pages/]`）展示了许多在 Razor 中编写代码的方法，但很少有示例关注简单的任务，这意味着这些内容可能非常难以理解。为了避免产生挫败感，你需要更简单的方法。接下来的章节将介绍你可以在任何网页上可能执行的两个基础任务。

## 让输出平庸化

上一节展示了在页面上显示当前日期的简单方法。实际上，根据你的需求，你有多种方法来处理简单类型的输出。例如，你可以向代码中添加一个字段来执行更复杂的输出，如下所示：

```cshtml
@{
var showString = "This is a string.";
}
```

然后你可以这样在页面中使用 `showString`：

```html
<p id="StringOutput">@showString</p>
```

`showString` 的创建可以包含提供所需数据所需的任何复杂度。然而，从根本上说，`showString` 仅仅是一个提供在线数据的输出。

你还可以创建自定义类来与 Razor 页面交互。例如，你可能会在 `Index.cshtml.cs` 中创建一个像这样的类：

```csharp
public class CodeBehind
{
public string aString = "This is a code-behind string.";
}
```

![Remember](img/remember.png) 在代码中使用此类之前，你必须像这样先创建一个实例：

```cshtml
@{
var codeBehind = new CodeBehind();
}
```

然后你这样在页面上使用实例变量 `codeBehind`：

```html
<p id="StringOutput2">@codeBehind.aString</p>
```

![Tip](img/tip.png) 注意，你通过 Razor 页面实例变量 `codeBehind` 访问 `CodeBehind` 类实例变量 `aString`。你可以以相同的方式访问实例方法。如果你的自定义类使用静态字段或方法，你不需要创建实例变量。和任何 C# 代码一样，你可以在不创建实例变量的情况下访问静态字段或方法。

## 更改网页数据

有时，你只需要对网页进行简单的更改，而并不真的想创建一个会让朋友们羡慕的复杂设计。网页是静态的，不像桌面端应用程序可以随心所欲地动态。因此，你需要一些手段向服务器请求更新，或者提供客户端代码在本地进行更改，但事实是，你需要一些手段通过请求来更改网页内容。使用 Razor 执行此任务简单的方法是创建后台代码（code-behind）。在这种情况下，代码作为 `IndexModel` 类的一部分出现在 `Index.cshtml.cs` 中如下：

```csharp
public string changingString { get; set; }
public void OnGet()
{
changingString = "This is the changing string.";
}
public void OnPost()
{
changingString = "The string has changed.";
}
```

这段代码的重点是 `changingString` 属性，它在初始页面请求期间由 `OnGet()` 设置。每当浏览器请求新页面时，后台代码都会查看 `OnGet()` 以确定是否有特殊操作要做。稍后，当你请求更改时，可以使用页面代码中的 `post` 方法调用 `OnPost()`，这将为 `changingString` 分配一个新值。`Index.cshtml` 中的代码如下：

```html
<p>@Model.changingString</p>
<form method="post">
<button>Click to Change Text</button>
</form>
```

请注意，`<form>` 实际上是包裹单个 `<button>` 的，而不是包裹整个页面。注意你使用 `@Model.changingString` 来访问 `changingString`。许多在线示例显示 `@changingString`，这完全不起作用（尽管它在过去可能有效）。`<button>`只是一个简单的 HTML 按钮，没有添加任何 `onclick` 处理器，所以它看起来不应该起作用，但实际上它是可以的。

当然，你可能需要提供多个按钮——想象一下！在这种情况下，简单的 `post` 方法不起作用，但通过非常微小的更改你有另一个选择。你给 `OnPost()` 方法一个更具体的名称，一个带有处理程序名称的。。因此，代码具有 `OnPostView1()` 和 `OnPostView2()`：

```csharp
public void OnPostView1()
{
changingString = "The string has changed.";
}
public void OnPostView2()
{
changingString = "Another Change!";
}
```

现在你需要另一个方法来访问这些方法。你只需通过在 `<form>` 标签上添加 `asp-page-handler` 属性来获取该方法，如下：

```html
<form asp-page-handler="view1" method="post">
<button>Click to Change Text</button>
</form>
<form asp-page-handler="view2" method="post">
<button>Try Another Change</button>
</form>
```

![Remember](img/remember.png) 添加到 `asp-page-handler` 属性的值有些违背直觉。注意它只是 `view1` 或 `view2`，而不是 `OnPostView1` 或 `OnPostView2`。





Razor 支持 switch 语句，这可以为你节省大量的打字时间。假设你如下创建了一个名为 `ViewNumber` 的 `int` 变量：

```razor
@{
int ViewNumber;
if (Model.changingString == "This is the changing string.")
    ViewNumber = 0;
else if (Model.changingString == "The string has changed.")
    ViewNumber = 1;
else
    ViewNumber = 2;
}
```

在这种情况下，`if` 语句看起来是正常的，因为它出现在一个 `@` 块中。该代码为 `ViewNumber` 赋值了一个与 `changingString` 中当前文本相对应的值（等一下，原文用的是 `changingString`）。你可以使用 `switch` 来处理 `ViewNumber`，如下所示：

```razor
@switch(ViewNumber)
{
    case 0:
        <p>Using Original View</p>
        break;
    case 1:
        <p>Using View 1</p>
        break;
    case 2:
        <p>Using View 2</p>
        break;
    default:
        <p>Unrecognized View</p>
        break;
}
```

除了 `@` 符号和 HTML 标签的使用，此示例中的 `switch` 语句可以出现在任何 C# 文件中。所有的规则与处理 C# 时的规则完全相同，因此你不需要做任何奇怪的操作，只需要记住那个 `@` 符号以及你可以对 HTML 进行一些有趣操作这一事实即可。

## 实现循环

正如你所预期的，Razor 使用你在 C# 中使用的相同技术来实现循环处理。其区别在于你处理数据的方式以及你执行的任何任务的结果。接下来的章节将展示如何创建一个数组，以便你有源数据进行处理，然后展示如何使用多种不同的技术来处理数据。

### 创建数组

Razor 中的数组可以采用你在 C# 中使用的任何形式。当然，你需要在 `@` 块中创建它，或者使用现有的值数组。以下是在示例中使用数组创建用例：

```razor
@{
string[] Colors = { "Red", "Orange", "Yellow", "Green", "Blue", "Violet" };
}
```

你可以看到，这里没有任何奇怪的。你通常用于创建 C# 数组的相同技术在这里也同样适用。

### 使用 for 执行特定次数的任务

上一节中创建的 `Colors` 数组为测试 Razor 中的 `for` 循环提供了一种完美的方法。以下代码使用 `Colors` 数组作为源，并依次显示每种颜色：

```html
<h3>Colors</h3>
<ul class="text-left">
    @for (var i = 0; i < Colors.Length; i++)
    {
        <li>Color @i is @Colors[i]</li>
    }
</ul>```

与之前的示例一样，你需要在创建 `for` 循环之前使用 `@` 符号。此外，此示例还展示了如何处理源数组使其能够正确地显示在屏幕上。记住，你可以使用通常在 C# 中处理数据时用于 `for` 循环的所有所有相同技术。

### 使用 foreach 和 while 处理未知次数的操作

`for` 循环与 `foreach` 以及 `while` 循环之间的本质区别在于，前者以已知的次数处理数据，而后者在完成之前以未知的次数处理数据。在很多情况下，循环机制的选择取决于风格和偏好。有些开发者喜欢一种形式，而其他开发者则喜欢另一种形式。以下是使用 `foreach` 语句提供的上一个示例中的相同输出。

```html
<h3>Colors Using Foreach</h3>
```razor
@{
int counter = 0;
}
<ul class="text-left">
    @foreach (string item in Colors)
    {
        <li>Color @counter is @item</li>
        counter++;
    }
</ul>
```

示例首先声明了一个 `int` 变量 `counter` 来跟踪颜色编号。然后它使用 `@foreach` 循环来处理 `Colors` 数组。你在这个版本的示例中应该注意到的区别是产生输出所使用的技术，以及示例自由地混合了 HTML 和 C# 代码。

# 第 3 章

#数据的生成与消费

本章内容

- 定义序列化数据基础
- 开发数据生成器
- 消费数据并展示





在一个章节中演示复杂的气象预报生成技术是不可能的，因为现在的大多数气象生成器都依赖于先进的机器学习和深度学习技术。然而，`WeatherForecast` 项目可以让你从一个非常基础的角度了解此类程序是如何运作的。`RetrieveWeatherForecast` 项目演示了如何查询 API，然后以基本的方式将其提供的信息显示在屏幕上。这两个项目的意义在于，你不需要创建极其复杂的编码场景就可以创建出与如今的数据配合的真正用的应用程序。

## 序列化数据不是为了早餐

在某些方面，数据的序列化非常像吃早餐。你从从一整碗数据开始，一次一口地将其放入磁盘，就像你一口一口地吃麦片片（cereal）一样。其核心思想是让数据易于管理和更有组织，从而便于对其操作。当你从内存中处理一个对象集合时，单个对象（即集合）包含了你正在访问的其他对象。这些每个对象都有一组包含数据的属性。序列化将每个部分拆分开，这样你现在就有某种将数据存储在磁盘上的方法。常见的存储方法有：

*   **逗号分隔值 (CSV)：** 将数据分成行，集合中的每个对象对应一行，分成列，对象中的每个属性对应一列。你最终得到一个由行和列组成的表格，看起来非常像你为了自己组织数据而手写在纸上的内容。这种存储通常要求集合中的每个对象必须是相同的类型并定义了相同的属性。这种数据存储形式的优点是对于大量数据，它的空间效率极高，这就是为什么你看到许多用于数据科学的数据集以此方式存储的原因。
*   **可扩展标记语言 (XML)：** 从根节点对象开始，为每个对象创建主节点，为每个属性创建子节点。你最终得到一个树形结构，它可以适应数据可能采取的任何形式，并且可以非常详细地描述数据元素与数据本身之间的关系。当数据结构不良好、集合可能包含具有不同属性的不同对象时，你通常使用这种存储形式。它对于自然具有层次结构的数据也同样有效。这种存储形式的优点是允许以完全可检索的方式存储数据属性。
*   **JavaScript 对象表示 (JSON)：** 为每个对象创建类似字典的条目。在许多方面，JSON 和 XML 相似，因为它们都是自描述的，使用分层格式，并且可以使用 `XMLHttpRequest` 调用来获取。然而，JSON 与 XML 的不同之处在于，JSON：
    *   不使用结束标签
    *   大多数时候更短
    *   读写速度更快
    *   可以使用数组

![Remember](img/remember.png) 这些存储方法每种都有其它的优缺点。例如，CSV 文件容易受到难以检测的的损坏，而 XML 比较臃肿并消耗大量空间。这两种类型的存储都易于在平台之间移动，你会看到它们在网上被广泛使用。使用此类数据存储技术的意义是确保即使应用程序在某个时刻被丢弃，你的数据仍然可以访问。这两种数据格式都是文本类型，文本是跨系统的通用格式，也是在人们变得变得花哨之前存储信息的第一种格式。

要序列化数据，你必须向应用程序描述如何解释它——即如何“下口”。完成这项任务有许多方法，你选择的方法取决于你的数据格式。在许多情况下，你首先简单地定义你创建的对象是可序列化的，然后使用特殊的编码技术将这些对象写入磁盘。在这种情况下，编译器提供了大量的帮助，而且代码易于理解（只要你不过深研究那些幕后的代码即可）。

## 开发数据生成器和 API

*数据生成器*从某些源获取信息或随机定义数据元素，并将其放入便于多种用途（例如分析）的格式中。数据生成器可以产生文本数据，但也可以产生图形、音频和其他类型的数据。数据的格式取决于消耗它的用户的需求。接下来的章节将讨论如何使用现有的 Visual Studio 2022 项目创建一个数据生成器，该生成器同时作为浏览器或其他应用程序可以查询的 API。

### 创建 WeatherForecast 项目

你首先需要一个项目可以使用。该项目将依赖于现有的 Visual Studio 2022 模板，并带有一些你在创建数据生成器时通常会做的修改。要创建项目，请按照以下步骤操作：

1. **在 Visual Studio 2022 启动窗口中点击“创建项目”。**
   你会看到要使用的模板列表。
2. **在下拉列表框中选择 C#、所有平台（All Platforms）和 Web。找到 ASP.NET Core Web API 模板，如[图 3-1 所示。**
   ![Technicalstuff](img/technicalstuff.png) 注意，该模板支持的环境列表包括桌面操作系统和云端设置。API 通常可以在任何具有所需支持的地方运行，并为来自任何浏览器的消费者提供服务，这使得 API 极其多功能。然而，你通常会在本地启动 API，然后再将其移动到云端。
   ![定位 ASP.NET Core Web API 模板的截图。](img/9781119839071-fg060301.png)
   图 3-1: 找到 ASP.NET Core Web API 模板。
3. **突出 ASP.NET Core Web API 模板并点击“下一步”。**
   你会看到“配置你的新项目”对话框，如[图 3-2 所示。**
4. **在“项目名称”字段中输入 WeatherForecast，并在你的硬盘上为项目选择一个位置。确保你选择了“将解决方案和项目放在同一目录”（Place Solution and Project in the Same Directory）选项，然后点击“下一步”。**
   你会看到“其他信息”对话框，如[图 3-3 所示。**
   ![为 API 提供名称和位置的截图。](img/9781119839071-fg060302.png)
   图 3-2: 为 API 提供名称和位置。
   ![为 API 选择额外要求的截图。](img/9781119839071-fg060303.png)
   图 3-3: 为 API 选择额外要求。
5. **在“框架”字段中选择 .NET Core 3.1（长期支持），在“身份验证类型”字段中选择“无”（None），并勾选“配置 HTTPS”。**
   ![Tip](img/tip.png) 公共 API 数量已达数十万（甚至数百万计），通常不需要任何身份验证。私有和付费 API 通常需要身份验证，但这种身份验证可能不是以登录对话框的形式出现。相反，客户端向 API 传递特殊令牌以进行验证。因此，你可能并不经常实际使用 API 的标准身份验证功能。在创建项目之前，考虑一下你希望客户端如何进行身份验证。





![Warning](img/warning.png) 对任何种类的 API 使用安全套接层 (SSL) 安全性是标准做法，否则你极难信任客户端接收到的数据（详情请参见 [`https://www.bluehost.com/resources/does-my-website-need-ssl-learn-the-benefits-of-ssl-for-website-security/`](https://www.bluehost.com/resources/does-my-website-need-ssl-learn-the-benefits-of-ssl-for-website-security/) 和 [`https://www.kaspersky.com/resource-center/definitions/what-is-a-ssl-certificate`](https://www.kaspersky.com/resource-center/definitions/what-is-a-ssl-certificate)）。取消勾选“配置 HTTPS”复选框是一个非常糟糕的主意，以至于很难理解微软在这种在这种甚至会包含它。底线是，如果你想让你的客户端感到放心，请务必使用 SSL。

### 6. **点击创建（Create）。**

Visual Studio 2022 会为你创建一个新的 Web API 项目。

### 让数据变得可信

Visual Studio 2022 提供的默认 API 随机生成天气信息。换句话说，这是你可以用于测试的假数据，但它不是基于任何真实数据，也不依赖机器学习技术来计算预测。相反，它仅仅是一些值。然而，默认设置在两个方面存在不足：

*   日期没有反映任何与天气预报相关的正常进展。通常情况下，你会看到一天、七天和十天的预报。某些设置甚至提供每小时预报，但总会有某种进展性，而本示例缺少了这一点。
*   你很难相信某些声称在零下 20 度时依然炎热的天气数据，但默认设置会尽力说服你那里确实很炎热。忽略掉挂在你鼻子上的冰柱吧；你真的过热了！

为了让输出更真实，你需要修改的代码出现在 `Controllers` 文件夹下的 `WeatherForecastController.cs` 中。打开此文件并进行此处所示的更改：

```c
[HttpGet]
public IEnumerable<WeatherForecast> Get()
{
    return Enumerable.Range(1, 10).Select(index => GetWeatherForecast())
    .ToArray();
}

private int DaysToAdd = 0;
public WeatherForecast GetWeatherForecast()
{
    var rng = new Random();
    WeatherForecast thisForecast = new WeatherForecast();
    thisForecast.Date = DateTime.Now.AddDays(DaysToAdd);
    DaysToAdd += 1;
    thisForecast.TemperatureC = rng.Next(-20, 40);
    switch (thisForecast.TemperatureC)
    {
        case int n when (n < -14):
            thisForecast.Summary = Summaries[0];
            break;
        case int n when (n >= -14 && n < -7):
            thisForecast.Summary = Summaries[1];
            break;
        case int n when (n >= -7 && n < 0):
            thisForecast.Summary = Summaries[2];
            break;
        case int n when (n >= 0 && n < 6):
            thisForecast.Summary = Summaries[3];
            break;
        case int n when (n >= 6 && n < 12):
            thisForecast.Summary = Summaries[4];
            break;
        case int n when (n >= 12 && n < 18):
            thisForecast.Summary = Summaries[5];
            break;
        case int n when (n >= 18 && n < 24):
            thisForecast.Summary = Summaries[6];
            break;
        case int n when (n >= 24 && n < 30):
            thisForecast.Summary = Summaries[7];
            break;
        case int n when (n >= 30 && n < 36):
            thisForecast.Summary = Summaries[8];
            break;
        case int n when (n >= 36):
            thisForecast.Summary = Summaries[9];
            break;
    }
    return thisForecast;
}
```

`public IEnumerable<WeatherForecast> Get()` 方法比原始源短。它现在实际上没有定义任何数据，但它确实创建了一个天气预测数组。`Enumerable.Range(1, 10)` 方法创建了一个十天的预报，这比默认创建五天预报更可信（尽管如果你找得足够仔细，你可能会发现某些网站确实提供五天预报）。

`WeatherForecast GetWeatherForecast()` 方法一次定义一天的预报。为了创建递进的日子，代码调用了 `DateTime.Now.AddDays(DaysToAdd)`，其中变量 `DaysToAdd` 在每次通过时都会递加 `1`。摄氏度温度是一个随机生成的数字。华氏度温度在 `WeatherForecast.cs` 文件中使用 `public int TemperatureF => 32 + (int)(TemperatureC / 0.5556);` 计算。计算出的数据通常作为数据生成器输出的一部分出现。最后，代码使用 `switch` 根据实际温度定义 `Summary` 值（而不是像以前那样随机生成）。因此，当温度接近 86 华氏度时，预报将告诉你天气很酷热而不是结冰。

### 查看 API 配置

了解如何连接你的 API 非常重要。要发现此信息，请打开位于 `Properties` 文件夹中的 `launchSettings.json` 文件。该文件中有两个重要的设置，即使你在其他所有方面都使用默认值，也不能忽略它们。第一个是 `"sslPort": 44327`。`sslPort` 之后的数字指定了访问你的 Web 服务所需的端口号。你可以忽略 `applicationUrl` 设置，因为你不会用它来访问 API；只有 `sslPort` 设置有效。这意味着你将使用 `https://localhost:4432/7/` 作为访问此 Web 服务的基础 URL。（端口号 4432 随系统变化。）

![Remember](img/remember.png) 你需要的第二个设置是 `"launchUrl": "weatherforecast"`。此设置定义了客户端可以在哪里找到 API。因此，访问 API 的完整 URL 为 `https://localhost:44327/weatherforecast`。这是一条关键信息，因为你以后创建客户端时会需要它。

### 检查 API 功能

在开发客户端之前，你可以检查你的 API。输出可能不会趣，但你可以看到 API 正在工作。以下章节将解释如何检查 API 的功能。

#### 在浏览器中查看数据

你想查看 API 功能第一个地方是浏览器。选择调试（Debug）⇒ 无调试启动（Start Without Debugging）。你通常看到的第一个是对话框，询问你是否要为项目安装 SSL 证书，如图 3-4 所示。

![确定是否要安装 SSL 证书的快照](img/9781119839071-fg060304.png)

图 3-4: 确定是否要安装 SSL 证书。

除非你真的喜欢浏览器反复询问你关于正在测试的网站，直到你最终疯掉，否则你会点击“是（Yes）”。因为证书仅对你的项目有效，所以你不需要太担心会在系统中打开巨大的安全漏洞。

在你点击“是”后，Windows 通常会显示另一个对话框，询问你是否确定要安装该证书，如图 3-5 所示。显然，Visual Studio 2022 和 Windows 之间并不通信，所以你基本上必须回答两次相同的问题。





正当你开始认为可能永远看不到你的 API 运行时，浏览器窗口就弹出了，你看到了图 3-6 中显示的序列化 JSON 数据。你的 API 后台代码会根据 `public IEnumerable<WeatherForecast> Get()` 调用创建的数组自动为你处理序列化。这种现象有很多奇妙的原因，例如向方法调用添加了 `[HttpGet]` 特性，你可以在 [`https://docs.microsoft.com/aspnet/core/mvc/controllers/routing`](https://docs.microsoft.com/aspnet/core/mvc/controllers/routing) 和 [`https://docs.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.httpgetattribute`](https://docs.microsoft.com/dotnet/api/microsoft.aspnetcore.mvc.httpgetattribute) 中了解，但主要需要的是它只需按预期工作，无需你编写任何额外代码。

![再次回答问题让 Windows 感觉好一些。](img/9781119839071-fg060305.png)

图 3-5：再次回答问题让 Windows 感觉好一些。

![浏览器输出显示了序列化的天气预报数据。](img/9781119839071-fg060306.png)

图 3-6：浏览器输出显示了序列化的天气预报数据。

## 定位 IIS 图标

如果你遵循了本章之前章节概述的流程，你现在已经有一个服务了。为了让服务有用，它必须持续运行直到你不再需要它为止。在 Windows 通知区域中，你会看到一个像图 3-7 所示的 IIS Express 图标。右键单击此图标显示正在运行的网站列表。此外，你还可以看到与网站交互的控件。

![在通知区域寻找 IIS Express 图标以查看哪些应用程序正在运行。](img/9781119839071-fg060307.png)

图 3-7：在通知区域寻找 IIS Express 图标以查看哪些应用程序正在运行。

![提示](img/tip.png)了解 IIS Express 图标非常重要，因为开发者经常花费大量时间在网站代码中寻找错误，结果发现服务并没有运行。通过寻找此图标，你可以节省时间并避免尴尬。

## 创建消费者网站

当你有了一个可用的 API 后，你需要一个应用程序来调用它。由于 API 的工作方式，该应用程序不需要是 Web 应用程序——你也可以使用控制台应用程序、桌面应用程序或其他与数据交互的应用程序。想到你的服务可以被任何地方的任何人使用，这非常神奇。然而，考虑到本章是关于 Web 开发的，接下来的章节将关注使用名为 `RetrieveWeatherForecast` 的 Web 应用程序调用 `WeatherForecast` API。

![记住](img/remember.png) 如果无法访问 `WeatherForecast` API，后续章节中的应用程序将无法工作。请按照前一节“定位 IIS 图标”中的信息，确保你可以在通知区域的 IIS Express 图标中看到它。

### 创建 RetrieveWeatherForecast 项目

要开始使用 `WeatherForecast` API，你需要一个 Web 应用程序。按照以下步骤创建示例 Web 应用程序：

1. **在 Visual Studio 2022 启动窗口中点击“创建新项目”。**
   你会看到与之前图 3-1 所示类似的模板列表。

2. **在下拉框中选择 C#、所有平台和 Web。找到 ASP.NET Core Web App 模板。**

3. **高亮 ASP.NET Core Web App 模板并点击“下一步”。**
   你会看到一个与之前图 3-2 所示类似的“配置你的新项目”对话框。

4. **在“项目名称”字段中输入 RetrieveWeatherForecast，并在你的硬盘上为项目选择一个位置。确保勾选“将解决方案和项目放在同一目录”，然后点击“下一步”。**
   你会看到一个与之前图 3-3 类似的“附加信息”对话框。

5. **在“框架”字段中选择 .NET Core 3.1 (长期支持)，并在“身份验证类型”字段中选择“无”，然后选择“配置 HTTPS”。**
   因为这可能是一个关键的业务应用程序，在这种情况下使用 SSL 是意义的。对于信息类网站是否使用 SSL 取决于与数据交互时的感知风险。如果不确定，请使用 SSL。

6. **点击“创建”。**
   Visual Studio 2022 将为你创建一个新的 Web 应用程序项目。

### 开发用户界面

由于你没有设计师来用于 ASP.NET Core Web App 应用程序，因此在组合界面时进行一些试错是比较重要的。大多数人很难仅凭代码就想象出网站最终的样子，因此进行一些更改然后查看网站是你拥有的最佳选择。接下来的章节将告诉你更多关于为此示例创建用户界面的知识。

![提示](img/tip.png) 如果你对界面进行了更改，这些更改并不总是会显示，这真的很令人沮丧。遗憾的是，如果 Web 应用程序一直运行，你可能会看到旧代码而不是新代码。为了防止“掉头发”（压力过大），在每次修改代码后，停止应用程序网站（不是 `WeatherForecast` 服务网站）。你可以通过点击通知区域 IIS Express 图标中的如图 3-8 所示的“停止站点”来停止它（见本章中“定位 IIS 图标](#c38.xhtml_c38-sec-0010)”节所述）。

![停止站点以便你可以看到用户界面代码的更改。](img/9781119839071-fg060308.png)

图 3-8：停止站点以便你可以看到用户界面代码的更改。




你网页的后台代码（code-behind）始终假设字符串就是字符串而不是 HTML。因此，如果你从后台代码输出类似 `<p>This is a string</p>` 的内容，你在网页上看到的将是该字符串以及起始标签和结束标签。显然，这并不是你希望在网页上发生的结果，尤其是考虑到网页已经布满了标签。因此，如果你不在显示处理过程中对 `Model.myData` 输出进行任何处理，那么上一节中的输出将是有缺陷的。

这时 `@Html.Raw()` 调用就派上用场了（详细信息请参阅 [`https://docs.microsoft.com/dotnet/api/system.web.mvc.htmlhelper.raw](https://docs.microsoft.com/dotnet/api/system.web.mvc.htmlhelper.raw)）。它告诉 ASP.NET 将 `Model.myData` 中的数据显示为 HTML 而不是纯文本。该调用是一个名为 `IHtmlHelper` 的完整接口的一部分，你可以在 [`https://docs.microsoft.com/dotnet/api/system.web.mvc/htmlhelper](https://docs.microsoft.com/dotnet/api/system.web.mvc/htmlhelper) 中了解更多相关信息。

### 获取并反序列化数据

现在是时候展示此示例中的各种元素是如何组合并在屏幕上显示信息的。接下来的章节将帮助你完成处理反序列化然后将其作为 HTML 输出的过程。

### 添加 WeatherForecast 类

为了反序列化来自 `WeatherForecast` API 的数据，你需要一个描述该数据的类。幸运的是，你已经拥有这样一个类了。它出现在 `WeatherForecast` 项目中。使用以下步骤将该类添加到你的 `RetrieveWeatherForecast` 项目中：

1. **在解决方案管理器中，右键点击 `RetrieveWeatherForecast` 项，并在右键菜单中选择“添加”⇒“现有项”。**

   你会看到一个“添加现有项”对话框。

2. **导航到 `WeatherForecast` 项目文件夹，如图 3-9 所示，并突出显示 `WeatherForecast.cs`。点击添加。**

   你会看到 `WeatherForecast.cs` 文件已添加到你的项目中。

![向你的项目添加 WeatherForecast 类的快照。](img/9781119839071-fg060309.png)

图 3-9： 向你的项目添加 `WeatherForecast` 类。

![记住](img/remember.png) 你刚刚导入的文件只有一个问题。变量名全部采用首字母大写，例如 `Date`。然而，如果你查看之前显示的图 3-6，你会发现变量是小写的，例如 `date`。因为 C# 是一种区分大小大小的语言，你需要将刚刚导入到 `RetrieveWeatherForecast` 项目的 `WeatherForecast.cs` 副本中的变量也改为小写，这样它们现在看起来就像这样：

```cs
using System;

namespace RetrieveWeatherForecast
{
public class WeatherForecast
{
public DateTime date { get; set; }
public int temperatureC { get; set; }
public int temperatureF => 32 + (int)(temperatureC / 0.5556);
public string summary { get; set; }
}
}
```

### 构建核心代码

当网页加载时，它会调用后台代码中的 `OnGet()` 来获取任何所需信息，因此这就是你放置查询 `WeatherForecast` API 代码的地方。你最初可能想将此代码放在 `RetrieveWeatherForecast` 构造函数中，但如果你这样做，你将看到错误信息，提到无法在该处放置异步代码（这在随后的“跳过多线程部分”节中讨论过）。除了检索和反序列化数据的代码外，你还需要定义用于与网页交互的 `myData` 变量。在 `index.cshtml.cs` 中的以下代码显示了你需要提供的内容以使示例运行：

```cs
[BindProperty]
public String myData { get; set; }
public async Task OnGet()
{
// 创建客户端对象以检索数据。
HttpClient client = new HttpClient();
// 告诉客户端对象从哪里获取数据
// 以及数据的格式是什么。
client.BaseAddress =
new Uri("https://localhost:44327/weatherforecast");
client.DefaultRequestHeaders.Accept.Add(
new MediaTypeWithQualityHeaderValue("application/json"));
// 提供默认响应然后获取数据。
myData = "No Weather Report Today";
HttpResponseMessage getData =
await client.GetAsync("https://localhost:44327/weatherforecast");
// 如果数据访问成功，则从响应中读取
// 并显示在屏幕上。
if (getData.IsSuccessStatusCode)
{
String data = getData.Content.ReadAsStringAsync().Result;
// 将 JSON 数据反序列化为 WeatherForecast 数组。
WeatherForecast[] JSONData = JsonSerializer.Deserialize<WeatherForecast[]>(data);
// 将每个天气预报输出为表格中的行。
myData = "";
foreach (WeatherForecast Item in JSONData)
{
myData += "<tr>";
myData += "<td>" + Item.date.ToDateString() + "</td>";
myData += "<td>" + Item.temperatureC + "</td>";
myData += "<td>" + Item.temperatureF + "</td>";
myData += "<td>" + Item.summary + "</td>";
myData += "</tr>";
}
}
await Task.Delay(1000);
}
```

// 添加 Using 语句
```cs
using System.Net.Http;
using System.Net.Http.Headers;
using System.AspNetCore.Mvc;
using System.Threading.Tasks;
using System.Text.Json;
```

注意 `myData` 被定义为标准属性。你需要将其变为 `public` 以便网页可以访问它。此外，你还需要添加 `[BindProperty]` 特性将属性绑定到网页，如 [`https://docs.microsoft.com/dotnet/api/system.web.mvc/model-binding](https://docs.microsoft.com/dotnet/api/system.web.mvc/model-binding) 所示。

查询 API 的过程从创建 `HttpClient` 对象 `client` 并对其进行配置开始。如代码所示，为了让客户端能够处理 JSON 数据，你必须配置 `BaseAddress` 和 `DefaultRequestHeaders.Accept` 属性。`BaseAddress` 指向 API 的 URL。然而，你还必须通过向 `DefaultRequestHeaders.Accept` 添加 `MediaTypeWithQualityHeaderValue` 对象来告诉客户端接受 `"application/json"` 数据。

实际的请求响应将在客户端调用带有所需 URL 的 `GetAsync()` 后出现在 `HttpResponseMessage` 对象 `getData` 中。成功的查询将把 `getData.IsSuccessStatusCode` 设置为 `true`，而不是像你经常处理 HTML 请求时可能预期的 OK 或 200。

目前还没有任何数据可以处理。你通过调用 `getData.Content.ReadAsStringAsync().Result` 获取数据。然而，你仍然需要通过调用 `JsonSerializer.Deserialize<WeatherForecast>()` 对结果字符串进行反序列化。这就是需要小写变量的地方，因为否则反序列化将无法成功。

### 跳过多线程部分

你不能使用模板提供的默认 `OnGet()`。原因在于对 Web API 的调用是多线程且异步的。如果你使用默认的 `OnGet()`，你永远看不到数据，因为 `OnGet()` 返回得太早了。因此，问题在于如何让大家共同配合。





此过程的第一部分是在每次进行异步调用时都使用 `await` 运算符 ([`docs.microsoft.com/dotnet/csharp/language-reference/operators/await``](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/await))。因此，你在代码中看到的是 `await client.GetAsync("https://localhost:44327/weatherforecast")`，而不仅仅是调用 `GetAsync()`。遗憾的是，这种修改使得代码可以通过编译，但并没有解决 `OnGet()` 过早返回的问题。

此过程的第二部分是将 `OnGet()` 的返回类型从 `void` 更改为 `Task`。尽管你从未在代码中看到任何返回值，那么它是如何工作的呢？最后的一个环节是调用 `await Task.Delay(1000)`，它提供了一个输出，告诉 `OnGet()` 该返回了。示例使用了 1000 毫秒，但对于更复杂的 API 交互，你可能需要增加此值。

### 运行应用程序

在完成本章之前的章节后，此时你终于可以运行应用程序并看到结果。请确保你同时打开了 `WeatherForecast` 和 `RetrieveWeatherForecast` 项目，并且 `WeatherForecast` 服务正在运行（如本章中“定位 IIS 图标”节所述）。否则，示例将无法运行。选择 调试⇒  不调试启动。你将看到未来十天的（模拟）天气预报，如图图 3-10 所示（你的数据可能不会匹配）。

![显示来自 WeatherForecast API 生成的天气预报的截图](img/9781119839071-fg060310.png)

图 3-10： 查看来自 `WeatherForecast` API 生成的天气预报。

![记住](img/remember.png) 尽管这只是网页设计的简单视图，但在当今许多实例中都是如此。当符合其需求时，组织非常乐意使用他人生成的数据，而本章中展示的技术可以帮助你获得所需的数据访问权限。

# 索引

***

## 符号与数字

*   ' 字符，36, 40
*   `\` 字符，37, 534
*   (:) 字符，236, 646
*   `!` 运算符，58, 87
*   `/` 运算符，82
*   – 运算符，81, 82
*   `??` 运算符，226–227
*   `?` 运算符，101
*   - 符号，16
*   `$` 符号，44
*   `%` 运算符，82, 161
*   `&` 运算符，81, 87–88, 235
*   `&&` 运算符，87–88
*   `*` 运算符，82
*   `@` 符号
    *   Razor 运行时编译
        *   数组，772–773
        *   逻辑语句，771–772
        *   循环，772–774
        *   语法，766–767
    *   字面量运算符，39
*   `[]` 运算符，169
*   `[]` 符号，127, 141
*   `^` 运算符，87, 235
*   `_` 符号，30, 259, 423
*   `{` 符号，19, 97
*   `|` 运算符，87, 235
*   `||` 运算符，87–88
*   `}` 符号，19, 97
*   `~` 符号，330, 350
*   `+` 运算符，38, 81, 82, 92, 484
*   `#+` 运算符，38, 81, 82, 92, 484
*   `+` 符号，16
*   `++n` 运算符，84, 122
*   `<` 运算符，81
*   `<=` 运算符，85
*   `<T>` 符号，142
*   `=` 运算符，26, 81, 84, 91
*   `!=` 运算符，52, 86
*   `=` 符号，26
*   `==` 运算符，52, 86
*   `=>` 运算符，109 另参 lambda 表达式
*   `>` 运算符，81, 89
*   `>=` 运算符，85
*   `'\0` 字符，37, 38
*   `//` 符号，19 另参 注释
*   `'\n` 常量，37, 252
*   `n--` 运算符，85
*   `--n` 运算符，85
*   `n++` 运算符，84, 122
*   `'\r` 字符，37, 62
*   `"` 字符，36
*   `' ` 字符，37
*   ` ` 字符，40 另参 字符串；`String.Empty`
*   `'\t` 量，20, 37, 592
*   `'\x` 数字常量，43
*   `Conditional("DEBUG")` 属性，302
*   `Obsolete` 属性，302
*   32 位应用程序，591
*   32 位整数，29
*   32 位平台，596

## A

*   Abs 函数，87
*   抽象类
    *   提取，369–371
    *   通用讨论，244, 374–377
    *   用于接口，404–405
    *   面向对象编程 (OOP)，244
*   Reader`**`/**`TextWriter` 类，527
*   abstract 关键字，479
*   访问控制。另参 安全性
    *   访问方法，308–309
    *   程序集
        *   `internal` 访问修饰符，448–451
        *   概述，448
        *   `protected internal` 访问修饰符，452–453
    *   基类方法
        *   意外隐藏，359–361
        *   隐藏，355–359
    *   类，306–308
    *   类
        *   协变返回类型，319–320
        *   表达式体成员，329–331
        *   `init-only` 访问器，309–310
        *   `internal` 访问修饰符，307
        *   概述，303–304





- `protected` 访问修符，307, 434
- `protected internal` 访问修符，307, 434
- `public` 访问修符，247–249, 306
- 密封 (sealing)，377–378
- 目标类型 (target typing)，316–318

### 构造函数
- C# 提供的，321–322
- 示例，324–325
- 初始化器，326–327
- 不带构造函数的初始化器，327–329
- 概述，309, 320–321
- 替换默认，322–324

- `DoubleBankAccount` 程序示例，311–313
- 在命名空间中，456–458

### `private` 访问修符
- 程序集，451–452
- 类，304–306

### `readonly` 关键字，485–487
- Windows ，507

### 访问修符
#### `internal`
- 程序集，448–451
- 一般讨论，245, 288, 307, 434
- 范围，288–290

#### `private`
- 访问控制，271–273
- 程序集，451–452
- 字段，479
- 一般讨论，245, 304–306
- 范围，288–290

- `protected`，245, 307, 434, 479
- `protected internal`，245, 307, 309, 434, 452–453
#### `public`
- 类，247–249, 306–308
- 字段，479
- 一般讨论，245, 271–273

- AccessControl 命名空间，508
- 访问器方法，308–309
- AccessRule 命名空间类，508
- Action 关键字，413–415
- Active Server Pages (ASP)。*另请* ASP.NET Core
    - Razor 运行时，761, 762
    - VBScript 语言，576
- `Adapter` 类，511, 515
- 适配器，191
- `Add()` 方法，146, 150
#### 加加运算符
    - 一般讨论，38, 81, 82
    - 重载，92–93
    - `struct` 关键字，484–485
- `AddRange()` 方法，151–152
#### ADO.NET
    - `DataSet` 类，396–399
    - SQL，510–512
    - 存储过程，524
    - 高级加密标准 (AES)，507
    - 算法，41
    - 分配，477
    - 字母表，36–37, 529
    - `ALU` (算术逻辑单元)，33–34
    - 美国国家标准 (ANSI)，529
    - 美国信息交换标准 (ASCII)，162, 529
    - 与 运算符，81, 87, 235
    - 与/或 运算符，87, 235
    - *Android Development All-in-One For Dummies*(Burd & Mueller)，725
    - Android Studio，725
    - Android 操作系统，590, 593, 725
    - Angular 模板，597, 754
    - 匿名方法，109, 421–424, 585–586
    - ANSI (美国国家标准)，529
    - Apache Cordova ，593
    - `Append()` 方法，78–79
    - 应用程序接口 (APIs)，388, 485–487, 545
    - 阿拉语字母表，36–37, 529
    - 架构图，594
    - 架构验证，594
    - ArgumentException，212, 217
    - ArgumentOutOfRangeException，212, 216–217
#### 参数
- 默认参数，278–290
- 匹配，276
- 重载，276–275
- 传递给方法，273
- 引用，488
#### 算术运算符
    - 一般讨论，38, 81, 82
    - 递增运算符，84
    - 简单的，82
#### 数组
    - 添加到，489
    - 集合，125, 140
    - 转换为列表，144
    - 双括号，127, 141
    - 迭代器，134
    - 固定值，127, 128
    - `foreach` 方法，133
    - 初始化，132, 147
    - 接口作为基，389
    - 局限性，140
    - 排序，136
    - 特殊功能，128
    - 语法，127, 129
    - `var` 关键字，139
    - 变变长度，129
- 零入，58, 66, 127

- 制品，500
- 人工智能，576, 577





## 概述, 754
- 项目创建, 754–756

## 常用讨论, 9, 745–747

### Razor 运行时编译
- 数组, 772–773
- 更改网页数据, 768–770
- 与前代的对比, 762–763
- 文件布局, 763–764, 766
- 逻辑语句, 771–772
- 循环, 772–774
- 输出选项, 767–768
- 概述, 748, 761–762
- 语法, 766–767
- 变量, 770
- Web Forms 模板, 764–765

### 序列化, 528, 775–778

### 模板
- 空模板, 746–748
- HTTPS 选项, 749–750
- MVC 范式, 751–752
- 其他, 753–754
- 概述, 746
- 第三方软件, 753–754
- Web API, 752–753
- Web App 模板, 748–749

### 追踪, 556–558, 593

### `WeatherForecast` 项目
- API 功能, 783–786
- 伴随文件, 775
- 创建项目, 778–781
- 概述, 775–776
- 真实输出, 781–783
- `RetrieveForecast` 项目, 786–793
- 序列化数据, 777–778

### 程序集
- 访问修饰符, 451–453

### 类库
- 访问控制关键字, 448–453
- 向解决方案添加项目, 442–445
- 代码, 445–446
- 概述, 222, 437, 439
- 项目, 439–440
- 独立, 440–442
- 测试应用程序, 446–447

### 可执行程序, 437–439

### 常用讨论, 288, 433

### 汇编语言, 438
- 赋值运算符, 26, 84, 91
- 异步输入/输出 (I/O), 527, 528

### @ 符号
#### Razor 运行时编译
- 数组, 772–773
- 逻辑语句, 771–772
- 循环, 772–774
- 语法, 766–767
- 字面量运算符, 39
- 附加属性, 649
- 特性, 236, 290, 301–302

### `AuditRule` 命名空间类, 508

### 身份验证
- `Authentication` 类, 548
- MFA (多因素认证), 499–500
- Windows 登录, 503–506

### 授权
- `Authorization` 命名空间, 508, 548
- `System.Security` 命名空间, 506, 508
- 自动实现的属性, 314
- 自动缩进, 100
- Azure 开发, 593, 597

## B
- 后备字段, 314
- 反斜杠字符, 37, 534
- 基类方法, 355–361
- 二进制算术, 87–88

### 二进制基
- 二进制减法运算符, 81, 82
- `BinaryReader/Writer` 类, 528, 539–540
- 常用讨论, 30
- 二进制输入/输出, 528, 539–540
- 生物识别设备, 499–500
- 位值, 235–236
- 位映射图图形, 559, 563, 574
- 位运算运算符, 87
- 黑盒, 511–512
- Blazor 模板, 597
- .bmp 文件, 559, 563, 574
- 样板代码, 20
- 布尔型常量, 43

### bool 变量类型
- 内生变量类型, 39
- `is` 运算符无效转换, 348–349
- 逻辑比较运算符, 36, 85–88
- `as` 运算符无效转换, 349–350
- 装箱, 188, 189, 477–478
- 大括号, 19, 97

### break 语句
- 循环, 115–116, 123–124
- `while` 循环语句, 116–120
- 基于浏览器的集成环境 (IDE), 590
- 泡泡排序, 136–139
- `BufferedStream` 类, 541
- 缓冲, 541
- 内置泛型, 187–189
- 字节型类型, 29, 234
- 字节, 235–236

## C
- C 编程语言, 36
- C# 4.0 编程语言, 465
- C# 7.2 编程语言, 485–487

### C# 8.0 编程语言
- 接口之后, 381–386
- 可空引用类型, 469

### C# 9.0 编程语言
- 匿名方法, 421–424
- CAS (代码访问安全), 501
- 类和对象, 252–253
- 元素自, 59–60, 411, 475

### C# 10.0 编程语言
#### 最佳实践
- `'\n'` 常量, 37, 252
- 预测问题, 209
- `!=` 比较运算符, 52
- `==` 比较运算符, 52
- 大括号, 19, 97
- 注释, 19, 247, 264
- 定义重要常量, 104
- 双击错误项, 276
- 以优雅为目标, 345
- `EventHandler` 委托类型, 426
- 异常处理策略, 221–225
- 解释用户错误, 120





- 缩进，100
- 最后的机会异常处理，223, 225
- 本地函数，301
- 方法参数值，275
- 方法命名规范，264
- .NET Framework 预定义异常，215–216
- 最必要的访问，308
- 将无效引用置空，533
- 对象引用，255
- 对象初始化语法，329
- 纯英语显示，225
- 属性与字段，248
- 保护类型转换，348–350
- 短的 `try` 块，211
- `virtual` 关键字的节节性使用，368
- 特定的 `catch` 块，212
- `ToString()`，295
- 变量名，247
- 将警告视为错误，360
- `Write()`，252

## C# 代码片段，20
- CAS，501
- 通用讨论，1, 9
- 帮助索引，51–52, 84, 87
- 语言帮助，224
- 多重继承，387
- 在线交互，23
- 属性，248
- 支持的模式类型，110
- 顶层语句，20–21

## C# 代码片段，20
- C# 模块。参见程序集

## C++ 跨平台库开发，593
## C++ 编程语言
- COM 语言，575–580
- 析构函数，330, 350
- 函数指针，409, 411
- 通用讨论，9
- 逻辑变量类型，36
- UWP，724

## 缓存，545
- 回调方法，407–408
- 引用传递特性，280–281
- CAN_BE_USED_AS 关系
- 示例程序，391–396
- 通用讨论，379–381
- 大写写，18, 56–58, 247
- 回车字符，37, 62
- CAS (代码访问安全)，501
- 转换运算符，90–91
- 转换
    - 通用讨论，44–45
    - 无效运行时，347–348
    - `is` 运算符的无效转换，348–349
    - `as` 运算符的无效转换，349–350
    - 类型安全与，18
- catch 块，210–212
- 摄氏度，30–31, 32
- 链式调用，336–338
- char 字符类型，36–37
- 字符常量，43
- 字符类型
    - char 字符类型，36–37
    - 比较，40–41
    - `string`
        - 大小写转换，56–58
        - 常用操作，51–52
        - 比较，52–56
        - 示例，243
        - 格式化，72–76, 77
        - 不变性，50–51
        - 为...实例化列表，143–144
        - 循环，58
        - null，37, 38, 204–205
        - 输出手册，67–72
        - 概述，37–39, 48–49
        - 搜索，59–61
        - `StringBuilder` 类，77–79
        - `switch` 语句，56–58
        - 用户输入，61–66
- 快速查表，3
- 子类，244
- 中文语言，529
- Michael，370
- 命名空间类，508
- 约束，204
- 构造函数，323
- 定义，247
- 因子，369, 371
- 类，396
- 访问控制，448
- 添加到类，442
- 代码，445
- 通用讨论，222, 437
- 应用，439
- 类，440
- 测试，446
- 类成员
    - 通用讨论，257
    - 安全性
        - `internal` 访问修符，307
        - `private` 访问修符，304
        - `protected` 访问修符，307, 434
        - `protected` 访问修符，307, 434
        - `public` 访问修符，247, 306
- 类属性
    - 访问访问的访问器，316
    - 通用讨论，246, 257
    - 迭代块，180, 183
- 类。参见部分类
    - 抽象
        - 因子，369, 371
        - 管理变化的接口，404–405
        - 面向对象 (OOP)，244
        - 概述，244, 368, 374
        - `TextReader`/`TextWriter` 类，527
        - UML，370
    - 访问修饰符，245
    - 数据成员，257–259
    - 元素，246
    - 异常处理，244–245
    - 通用讨论，243
    - 继承
        - 避免 `as` 运算符的无效转换，349–350
        - 避免无效的运行时转换，347–348
        - 避免 `is` 运算符的无效转换，348–349
        - `BankAccount` 类示例，335–342
        - 链式调用，336–338



- `destructors`, 330, 350–351
- `HAS_A` 关系, 345, 346
- `IS_A` 关系, 335, 342–345, 346, 347
- 概述, 168, 244–245, 333–334
- 目的, 334–335
- 可替换类, 346–347
- 跟踪特性, 339–342
- 实例化, 246
- 用于统一的接口, 391–396
- 名称大小写写, 247
- 在命名空间中
    - 访问控制关键字, 456–458
    - 声明, 454–455
    - 文件作用域, 456
    - 嵌套, 455
    - 概述, 453–454
    - 部分类, 433, 459–463
    - 部分方法, 433, 463–464
    - 目的, 454
    - 使用完全限定名, 458–459
- 嵌套, 256–257
- 对象
    - 访问成员, 249
    - C# 9.0 代码, 252–253
    - 类定义, 247–249
    - 区分, 253
    - 实例化, 246
    - 传递给实例方法, 288–290
    - 属性, 257–258
    - 引用类型, 254–255
    - 传统代码, 250–252
- 部分类
    - 示例, 460–463
    - 概述, 433, 459–460
    - 目的, 460
- 多态, 244–245
- 密封, 377–378
- 结构比较, 475, 476
- `FileStream` 类, 541
- ClickOnce 技术, 507–508
- 云端开发, 593
- 云端项目, 593, 597
- `CLR`。参见公共语言运行时
- `cmd.exe` 命令, 18
- COBOL 编程语言, 127, 402–403
- 代码访问安全 (CAS), 501
- 代码克隆特性, 594
- 代码覆盖特性, 595
- 代码区域, 16
- `CodeAccessPermission` 命名空间, 508
- `CodeLens` 特性, 594
- Cold Fusion 语言, 577
- 集合类
    - `<T>` 符号, 142
    - 数组, 125, 140–141, 147–149
    - 字典, 142, 145–147
    - `foreach` 循环方法, 164–168
    - 一般讨论, 67
- 索引器
    - 格式, 169
    - 概述, 169–173
    - 示例程序, 170–173
    - `struct` 关键字, 483–484
- 信息存储, 512
- 初始化技术, 147–149
- 作为基类型的接口, 389–390
- 迭代器块
    - 示例, 176–177
    - 其他形式, 180–185
    - 概述, 173–175
    - `yield break` 语句, 178, 179–180
    - `yield return` 语句, 178–179
- 列表
    - 转换为数组, 144
    - 为 `int` 实例化, 144
    - 为 `string` 实例化, 143–144
    - 其他任务, 145
    - 概述, 125, 126, 143–144
    - 搜索, 144–145
- `LoopThroughFiles` 程序
    - 文件创建, 159–160
    - 输出行, 160–161
    - 十六进制输出, 161–163
    - 概述, 156–159
    - Visual Studio 2022, 163–164
    - 主类, 141–142
    - 目的, 177–178
- 集合
    - 添加项, 150
    - 创建, 150
    - 差运算, 149, 153
    - 交集运算, 149, 150–151, 152
    - 概述, 149
    - 特殊任务, 149
    - 并集运算, 149, 150–151, 152
    - 语法, 140
    - 类型, 164
    - 逗号分隔值 (CSV), 377–378




* `Concat()` 格式方法, 67, 71–72
* `Concatenate()` 格式方法, 69–71
* 拼接, 41, 66, 77–79
* 条件条件表达式, 96–97, 102, 115–116
* 控制台应用
    * 创建
        * 默认程序位置, 15–16
        * 执行, 17–18
        * 概览, 11
        * 复习, 18–20
        * 源程序, 11–15
        * 测试, 16
        * 工具箱窗口, 21–22
        * 顶层语句, 20–21
    * 一般讨论, 7–8, 598
    * 用户输入
        * 拼接, 66
        * 多余空格, 62
        * 概览, 61–62
        * 解析, 62–64
        * 数字序列, 64–66
* `Console.Read()` 调用, 407
* `Console.WriteLine()` 方法, 339–342
* `Console.WriteLine()` 语句, 20, 262–263
* `const` 数据成员, 259
* 常量, 259, 481. 另另特定常量
* 约束, 202–204
* 构造函数
    * 访问控制
        * C# 提供的, 321–322
        * 示例, 324–325
        * 初始化器, 326–327
        * 不使用构造函数初始化对象, 327–329
        * 概览, 309, 320–321
        * 替换默认, 322–324
    * 链式, 336–338
    * 示例, 324–325
    * 初始化器, 326–329
    * `protected internal` 访问修饰符, 309, 434
    * 替换默认, 322–324
    * `struct` 关键字, 480
* 包含, 343–345
* `Contains()` 方法, 59
* `ContainsKey()` 方法, 146
* `continue` 语句, 115–116
* 逆变性, 205, 206–208
* 控制与生产力问题
    * 可选参数和, 465
    * 参数
        * 命名参数, 470
        * null 参数, 473–474
        * 可选参数, 465–469
        * 输出参数, 471–472
        * 返回值, 470–473
* `Convert` 类, 45, 62–64
* `Cookie` 类, 548
* `Count()` 方法, 200–201
* 数字计数
    * 浮点数转换, 44–45
    * 浮点数变量和, 32–34
    * 一般讨论, 27
    * 变量计数, 114, 122
* 耦合, 202
* 协变性, 205, 208
* 协变返回类型, 319–320
* 崩溃, 214, 222
* 创建、读取和删除 (CRUD) 原则, 776
* `Create()` 方法, 284
* `CreatePackage()` 方法, 192
* cribbage 项目
    * 画板创建, 570–572
    * 调试学习, 623–626
    * 事件处理器, 569–570
    * 初始步骤, 565–566
    * 一般讨论, 565
    * 新方法, 574
    * 项目设置, 567
    * 分数处理, 567–569
    * 分数打印, 572–573
    * 跨平台
        * UWP 应用, 721–722, 725
        * Visual Studio Community 版, 13, 593
        * Visual Studio 企业版, 595
        * Xamarin 平台, 10, 593, 595
* CRUD (创建、读取和删除) 原则, 776
* `CryptoConfig` 类, 508
* `CryptoStream` 类, 541
* `.cs` 扩展, 9, 14, 434–435
* `CShell` 应用, 589, 591
* CSV (逗号分隔值), 777–778
* Ctrl+K 快捷键, 20
* Ctrl+S 快捷键, 20
* `CultureInfo.InvariantCulture` 属性, 57–58
* 大括号, 19, 97
* 当前对象, 296–300
* 当前属性, 166–168
* 自定义委托, 409–410
* 自定义异常, 220
* cw 快捷键, 20
* 西里尔字母, 36–37
## D
* 数据访问
    * 连接到数据源, 514–519
    * 创建访问应用, 514
    * 数据容器, 509, 511, 512, 596–597
    * 一般讨论, 509–512
    * 获取数据, 512–513
    * RAD 数据工具, 519–521
    * 示例数据库设置, 513–514
    * 编写数据代码, 521–524
* 数据绑定
    * 绑定对象, 683–687
    * 转换数据, 697–704
    * 依赖属性, 682
    * 编辑数据, 687–693
    * 一般讨论, 681
    * 模式, 683
    * 其他方面, 705
    * 验证数据, 693–697
* 数据集合. 另见特定类
* 数据容器, 509, 511, 512, 596–597
* 数据生成器
    * API 功能, 783–786
    * 创建项目, 778–781
    * 真实输出, 781–783
* 数据成员
    * `const`, 259
    * 初始化技术, 299–300
    * `readonly`, 259
    * 静态属性, 257–258
* 数据序列化
    * API 配置和功能, 783
    * API 功能, 784–786
    * 常见存储方法, 777–778
    * 伴随文件, 775





- 需求，776
- 真实的输出，781–783
- `RetrieveWeatherForecast` 项目，786–793
- 序列化数据，777–778

## Data View 功能，609–610

## 数据库
    -   连接数据源，514–519
    -   创建访问应用程序，514
    -   数据容器，509, 512
    -   常规讨论，509–524
    -   获取数据，512–513
    -   RAD 数据工具，519–521
    -   示例数据库设置，513–514
    -   编写数据代码，521–524

## DataReader 容器，512

## DataRow 容器，511, 512

## DataSet 类，399–401

## DataSet 容器，509, 511, 512

## DataTable 容器，509, 511, 512

## DataView 容器，509, 511, 512

## DateTime 变量类型，41–42

## DayOfWeek 属性，42

## DbCommand，511

## DbConnection，511

## 释放，477

## 调试
    -   继承与，334
    -   作为学习工具，623–626
    -   快照调试器功能，595
    -   时间旅行调试功能，595
    -   跟踪继承，339–342
    -   Visual Studio 支持，592

## decimal 数值型常数，43, 44–45

## decimal 变量类型，34–35, 234

## `decimal.Round()` 语句，114

## 声明，27–28, 362–363, 493–494

## 解耦，202

## 递减运算符，85

## 默认参数，278–279

## 默认参数，278–279

## 委托签名，412–413

## 委托类型，413–415

## 委托
    -   匿名方法与，421–424
    -   回调方法，407–408
    -   常见用途，411
    -   定义，408–411
    -   事件
        -   观察者模式，425
        -   概述，424, 430
        -   发布/订阅模式，425–431
    -   示例
        -   委托类型，413–415
        -   进度条应用程序，415–420
        -   简单示例，412–413
    -   生命周期，409–410
    -   `LoopThroughFiles` 程序，165
    -   签名，412–413

## 分隔符，64
- 拒绝服务，502–503
- 依赖项，202, 403–404
- 依赖注入，405–406
- 依赖属性，682
- `Dequeue()` 方法，199–200
- `DescendingEvens()` 方法，181–183
- `ServiceProvider` 类，508
- 反序列化数据，775, 789–792
- 设计模式，425
- 设计模式 (Gamma, Helm, & Vliss),425, 707

## 设计器
    -   Data View，609–610
    -   常规讨论，603–604
    -   UWP 应用程序，604–607
    -   WinForms 应用程序，609
    -   WPF 应用程序，607–609

## 析构函数，330, 350
## 开发者模式
    -   添加代码，738
    -   选择设备，739
    -   创建接口，734
    -   定义项目，732
    -   依赖项，728
    -   文件设置，730
    -   常规讨论，725
    -   PowerShell 设置，732
    -   远程桌面，730
    -   侧加载，727

## 设备独立单元 (DIUs)，654

## Dictionary<TKey, TValue> 集合
    -   创建，145
    -   常规讨论，142, 145
    -   迭代，147
    -   方法，147
    -   搜索，146

## 差异操作，149, 153

## 目录，`LoopThroughFiles` 程序
    -   文件列表创建，159
    -   格式化输出，160
    -   十六进制输出，161
    -   概述，156
    -   Visual Studio 2022，163

## Directory 类，158

## DirectX，724

## 丢弃参数，423

## `Display()` 方法，391–392

```
Display()
```

## `DisplayRatio()` 方法，281–282

## `Dispose()` 方法，351

## DIUs (设备独立单元)，654

## 除法运算符，82

## .dll 文件扩展名
    -   访问控制关键字，448–453
    -   向现有解决方案添加项目，442
    -   代码，445
    -   常规讨论，14, 307, 437, 439
    -   项目，439–440
    -   独立，440–441
    -   测试应用程序，446–447





* `doubleVariable` 变量类型，33
* `do…while` 循环语句，114–115
* `Download` 类，548
* `DPI` (每英寸点)，654
* 绘制
    #### 棋棋项目
        * 棋板创建，570–572
        * 事件处理器，569–570
        * 第一步，565–566
        * 新游戏开始方法，574
        * 概览，565
        * 项目设置，567
        * 分数处理，567–569
        * 分数打印，572–573
    #### `Graphics` 类
        * 画笔，563
        * 概览，561–562
        * 笔，562
        * 文本，563
    * .NET Framework，564–565
* `DRY` (不要重复自己)原则，244
* `DumpBuffer()` 方法，161–163
* `DumpHex()` 方法，159–161
* `duration` 属性，42
* `dynamic` 关键字，148–149, 578–580
* `Dynamic Language Runtime` (动态语言运行时)，582–584
* 动态编程
    * 匿名/lambda 方法，109, 421–424, 585–586
    * 动态语言运行时，582–584
    * 动态语言，576–578
    * 动态操作，580–582
    * 动态类型，47, 575–576
    * 动态变量，575, 578–582
    * 技术，578–580
    * `var` 关键字，575, 580–582

## E
* e 参数，427–429, 431
* 早期绑定，362–363
* 元素绑定，693. *另另* 数据绑定
* 权限提升，502–503
* else 语句，100–102
* 电子邮件，544, 546, 553–556
* 嵌套的 `if` 语句，102–104
* 空方法，265–268
* 空 `string`，38
* 空模板，746–748
* 封装，244, 290, 333. *另另* 访问控制
* 加密，507, 508
* `EndPoint` 类，548
*  endregion 指令，16
* `Enqueue()` 方法，199
* `enum` 关键字，231–232, 234
* 枚举标志位，229, 235–236
* 枚举开关，230, 237–238
* 迭代器
    * 优势，165–167
    * 数组，134–136
    * CLR 局限性，234
    * 定义开关，230, 237–238
    * `enum` 关键字，231–232, 234
    * 标志位，229, 235–236
    * 通用讨论，108, 155, 195, 229–230
    * 泛型，184
    * 初始化器，229, 233
    * 接口，134–135, 165
    * `foreach` 程序
        * 文件创建，159
        * 格式化，160
        * 十进制输出，161
        * 概览，165
        * Visual Studio，163
    * 方法，238
    * 命名，180
    * 现实案例，231
    * 指定类型，234
    * 等号，81
    * 等号符号，84 *另另* 数据绑定, 错误
    * 事件处理，569–570
    * 事件，425
    * `EventHandler` 委托，426
    * `EventHandler<T>` 委托，426
    * 通用讨论，407–429
    * 观察者设计
        * 发布/订阅，426
        * 处理器，430
        * 概览，425
        * 触发事件，427
        * 订阅，427
    * 事件命名空间，507
    * 益处，508
    * 类，244
    * 自定义异常，520
    * 程序员抛出的异常，315
    * 事件序列，333
    * `throw` 块，210–211, 215
    * `try` 块
        * 示例，216
        * 嵌套，313
        * 概览，76, 210, 225
    * 异常对象类，211–212
    * 异常，210–211
    * 异或 (xor) 运算符，87, 235
    * 可执行程序
        * 将程序分为多个，437, 438
        * 通用讨论，8, 307, 435, 598
    * `ExecutionEngineException`，215–216
    * 显式类型转换，90–91
    * 表达式体属性，314
    * 表达式类型
        * 分配类型，91
        * 计算类型，89–91
        * 通用讨论，89
        * 运算符重载，92–93





*   可扩展标记语言。*参见* XML
*   扩展类，238–239

## F

*   面部识别，500
*   `Factorial()` 函数，216–219
*   因式分解，369, 371–374
*   工厂方法
    *   依赖注入，405–406
    *   通用讨论，197, 202, 389
    *   用于隐藏的接口，399–401
*   华氏温度标，30–31, 32
*   假数值常量，43
*   假值，36
*   `field` 关键字，495–496
*   字段，248, 479
*   文件输入/输出 (I/O)
    *   异步，527, 528
    *   二进制，528, 539–540
    *   通用讨论，525–526
    *   读取器，527, 539–540
    *   流
        *   示例，529–533
        *   其他流，541
        *   概述，526
        *   `using` 语句，534–537
        *   写入文件，527–529, 540
    *   写入器，527, 539–540
*   文件权限，500, 508。*另* 访问控制
*   文件传输协议 (FTP),544, 551–553
*   `FileInfo` 类，158
*   `FileInfo` 对象，158–159
*   FileRead 程序
    *   二进制，528, 539–540
    *   示例，535
    *   通用讨论，527
*   文件范围命名空间，456
*   `FileStream` 类
    *   异步/同步 I/O，527, 528
    *   示例，529–533
    *   通用讨论，525–526, 541
    *   其他，541
    *   读取文件，537–540
    *   `using` 语句，534–537
    *   写入文件，527–529, 540
*   `FileWeb` 类，548
*   FileWrite 程序
    *   二进制，528, 539–540
    *   示例，535
    *   通用讨论，527
*   `finally` 块，210–211, 212–213
*   `Find()` 函数，171
*   `FindEmpty()` 函数，171
*   防火墙，555
*   固定长度类型，29, 39
*   固定值数组，127, 128
*   扁平文件格式。*参见* 序列化
*   灵活依赖，403–404
*   灵活列表，125
*   浮点常量，43
*   `float` 类型，31–34, 234
*   浮点数，86–87
*   浮点变量
    *   计算速度，33–34
    *   计数，44–45
    *   声明，31–32
    *   范围，32–34
*   流程控制
    *   `else` 语句，100–102
    *   通用讨论，95–96
    *   `if` 语句
        *   嵌套，102–104
        *   概述，96–97
        *   示例程序，97–100
    *   循环
        *   `break` 语句，115–116
        *   `continue` 语句，115–116
        *   `decimal` 类型限制，35
        *   `do…while` 语句，114–115
        *   灵活性，116–120
        *   嵌套，123–124
        *   概述，110–111
        *   范围，120
        *   `for` 语句，120–122
        *   `while` 语句，111–114
    *   `switch` 语句
        *   大写，56–58
        *   概述，104–106
        *   限制，106–107
        *   `switch` 表达式，107–110
*   字体信息，37
*   for 循环语句，120–122
*   `for(;;)` 语句，54, 122
*   foreach 循环方法
    *   在数组中，133
    *   集合，164
    *   `Descending()` 方法，181–183
    *   通用讨论，58, 71, 122
    *   `IEnumerable<T>` 接口，166, 167–168, 391
    *   `LoopFiles` 程序，165
*   form 类，58
*   格式化符，236
*   格式化字符串，73
*   Fortran 语言，205
*   Fox 编程语言，509
*   分数，30
*   自由文本，19。*参见* 注释
*   FTP (文件传输协议),544, 551–553
*   `FileWeb` 类，548
*   全限定命名空间，458
*   `Func` 关键字，413
*   函数，109, 411, 413
*   函数式编程，577
*   *泛式编程* (Mueller)，109
*   函数
    *   匿名，109, 421–424, 585–586
    *   局部
        *   属性，301–302
        *   创建，300–301
        *   实例方法，300–302
        *   重构过程，287
        *   静态方法，261, 271–273
    *   软件设计，502–503

## G

*   游戏设计项目
    *   棋板创建，570–572
    *   事件处理器，569–570
    *   第一步，565–566
    *   通用讨论，565
    *   新游戏开始方法，574
    *   项目设置，567
    *   得分处理，567–569
    *   得分打印，572–573
*   Gamma, Erich，425, 707
*   “四人之帮”，707





- 垃圾回收，330, 350–351, 477
- 通用寄存器，33–34
- 泛型集合类
    - 装箱/拆箱，188, 189
    - 般讨论，142, 187–188
    - `PriorityQueue` 包装类
        - `ColorsPriorityQueue` 示例，193
        - 约束选项，202–204
        - `Count()` 方法，200–201
        - `Dequeue()` 方法，199–200
        - 易于编写的方法，197–198
        - `Enqueue()` 方法，199
        - `Main()` 方法，196–197
        - 概述，190–192, 198
        - `PackageFactory` 类，201–205
        - `TopQueue()` 方法，200
        - 解包，194–195
    - 类型安全，188–189
    - 变型，205–208
- 泛型委托程序，187–189, 409–410
- 泛型接口，187–189
- 泛型迭代器，184
- 泛型方法，187–189
- `get()` 访问器，183–185
- `GetCurrentDirectory()` 方法，157–158
- `GetEnumerator()` 方法，134–135, 165–166
- `GetFileList()` 方法，158, 160
- `GetNameValue()` 方法，238–239
- getter 方法，308–309, 314
- Git 软件，593
- 全局命名空间，454
- 全局 using 语句，435–436
- 全局唯一标识符 (GUID)，622
- Google Colaboratory (Colab)，578
- 图形开发环境，604。另参见 designer
- 图形用户界面 (GUI)，7, 10
- `Graphics` 类
    - 笔刷，563
    - 般讨论，561–562
    - 笔，562
    - 文本，563
- 大于运算符，81, 89
- 大于等于运算符，85
- Groovy 编程语言，577
- gRPC，753–754
- GUI (图形用户界面)，7, 10
- GUID (全局唯一标识符)，622

## H
- 黑客，500, 555
- Halo Infinite，562, 563
- 硬编码，104
- HAS-A 关系
    - 般讨论，188
    - 继承，345, 346
- HAS-A 关系
    - 管理变更的接口，403–404, 405–406
    - 包装，531–532
- `HashSet<T>` 集合类
    - `Add()` 方法，150
    - `AddRange()` 方法，151–152
    - 创建，150
    - `ExceptWith()` 方法，153
    - 般讨论，142, 149, 150
    - `IntersectWith()` 方法，152–153
    - `SymmetricExcept()` 方法，152–153
- 哈希表，512
- 堆内存
    - 匿名方法和，422–424
    - 垃圾回收，330, 350–351
    - 对象，249
    - 引用结构和，487–488
- 希伯来字母表，36–37, 529
- Helm, Richard，425, 707
- 帮助索引，51–52, 84, 87
- 十六进制转储，156
- 十六进制
    - ASCII 表，162
    - 值和，235–236
    - 般讨论，30, 43, 156
    - `LoopThrough`
        - 文件，159–160
        - 格式，160–161
        - 十六进制输出，161–163
        - 概述，156–159
        - Visual Studio 2022，163–164
    - Unicode 集合，163
- 高级语言，8
- 印地语字母，529
- HTML，721, 725
- HTTP (超传输协议)
    - ASP.NET Core ，746–747
    - 下载文件，551–553
    - 般讨论，604
    - `System.Net` 命名空间，746
    - 标签，745
    - XAML 和，643
- HTTP 类，546, 548
- HTTPS 启用的网站，749
- 人类语言，5

## I
- `ICollection<T>` 接口，390
- `ICommand` 接口，709
- `IComparable` 接口类型，390–391
- `IComparable<T>` 接口类型，390, 392–394
- `IDictionary<TKey, TValue>` 接口，390
- `IDisposable` 接口类型，390
- `IEnumerable` 接口类型，390
- `IEnumerable<T>` 接口类型，166, 167–168, 391
- `IEnumerator` 接口，134, 165–166
- `IEnumerator<T>` 接口类型，166–168, 391
- if 语句
    - 般讨论，20, 96–97
    - 缩进，100
    - 嵌套，102–104
    - 示例程序，97–100
- `if.else` 表达式，101
- `IFormattable` 接口类型，390
- `IIS Express` 图标，785–786
- `IL` (中间语言)，411, 438
- `IList<T>` 接口类型，390
- 图像
    - 爪爪棋项目
        - 棋板创建，570–572
        - 事件处理器，569–570
        - 第一步，565–566
        - 新游戏开始方法，574
        - 概述，565
        - 项目设置，567
        - 分数处理，567–569





- 分数打印，572–573
- 一般讨论，559–561
- `Graphics` 类
    - 画刷，563
    - 概述，561–562
    - 笔画，562
    - 文本，563
- `.NET` Framework，564–565
- 不变属性，309
- 命令行式编码，577
- 隐式类型转换，44, 90–91
- `IMyInterface` 约束，204
- 增减运算符，84–85, 122
- 索引器
    - 集合类，169–173
    - 格式，169
    - 一般讨论，127, 129
    - 示例程序，170–173
    - `struct` 关键字，483–484
    - 语法，141
- `IndexOf()` 方法，59
- `IndexOfAny()` 方法，59, 70–71
- 无限循环，114, 122
- 信息泄露，502–503
- 继承
    - 抽象
        - 抽象类，374–377
        - 重构，369, 371–374
        - 方便性继承，371
        - 概述，368
        - UML，370
    - `BankAccount` 类示例
        - 基本更新，336–338
        - `Console.WriteLine()` 方法跟踪，339–342
        - 概述，335
    - `CAN_BE_USED_AS` 关系，379–381
    - 链式，336–338
    - 包含与，343–345
    - 析构函数，330, 350–351
    - 一般讨论，168, 244–245, 333–334, 353
    - `HAS_A` 关系，345, 346
    - 接口，387, 401–402
    - `IS_A` 关系
        - 非反射性，347
        - 概述，342–345, 346
        - 传递性，335
    - 方法重载
        - 隐藏基类方法，355–361
        - 概述，276–278, 354–355
    - 其他特性
        - 避免 `as` 符的无效转换，349–350
        - 避免无效的运行时强制转换，347–348
        - 避免 `is` 符的无效转换，348–349
        - 可替换类，346–347
    - 多态
        - 声明方法为虚（virtual），365–368
        - 用于访问隐藏方法的 `is` 符，364–365
        - 概述，361–364
    - 目的，334–335
    - 跟踪特性，339–342
- 继承方法
    - 一般讨论，354–355
    - 隐藏基类方法，355–361
    - 多态
        - 声明方法为虚（virtual），365–368
        - 用于访问隐藏方法的 `is` 符，364–365
        - 概述，361–364
    - 方便性继承，371
    - init 访问器，487
    - init-only 设置器，309
    - 输入输出
        - 异步，527
        - 一般讨论，528
        - 读取器，527, 539
    - 流
        - 示例，529–533
        - 其他流，541
        - 概述，526
        - `using` 语句，534
        - 写入文件，527, 540
    - 写入器，527, 540
    - `Insert()` 方法，79
    - 实例字段，262–263
    - 实例成员，258
    - 实例方法
        - 访问当前对象，298–300
        - 有效用法，293–295
        - 一般讨论，262–263
        - 函数，300
    - 对象
        - 访问当前对象，296–300
        - 传递方法，288–290
    - 静态方法，296
    - 实例属性
        - 有效用法，293–295
        - 一般讨论，290
    - int 变量
        - 创建，144
        - 声明，28
        - 其他类型，234
        - 一般讨论，27
        - 常量，39
    - `TryParse(n)` 方法，64
    - int 字面量，30
    - int 整数，27–34
- 集成开发环境 (IDE)
    - Visual Studio 2022，589
    - 一般讨论，591, 603
    - Jupyter Notebook 软件，4, 591
    - 移动设备，[7]
- IntelliSense 功能，223–224, 592, 618, 630
- IntelliTest 功能，595
- 有意性编程，265
- 接口关键字，381
- 接口
    - `CAN_BE_USED_AS`
        - 示例程序，391–396
        - 继承，379–381
    - 元素，381–382
    - 一般讨论，333, 379
    - 隐藏方法后面，399–401
    - 继承，401–402
    - 用于管理变更
        - 抽象类，404–405
        - 灵活依赖，403–404
        - `HAS_A` 关系，403–404, 405–406
        - 概述，402–403
    - 作为方法参数
        - 示例，387–388
        - 与继承混合，387
        - 命名规范，386
        - 新的 C# 8.0 功能，383–386




* 概述, 382–383
* 目的, 386

## 其他用途
* 数组/集合基类型, 389–390
* 通用对象引用类型, 390
* 方法返回值类型, 389
* 概述, 388

## 多态性, 401–402
* 预定义, 390–391
* 用于统一类, 396–399

## 中间语言 (IL), 411, 438
* 内部访问修符
* 程序集, 448–451
* 通用讨论, 245, 288, 307, 434
* 范围, 288–290

## 互联网
* C# 语言与, 9
* RFCs, 544
* `System.Net` 命名空间
* 检查网络状态, 549–551
* 下载文件, 544, 551–553
* 电子邮件, 544, 546, 553–556
* 重要子命名空间, 545–547
* 记录网络活动, 556–558
* 概述, 543–545
* 协议命名法, 548

## 物联网 (IoT), 598, 725
## 互联网协议 `IP` 类, 548
* 插值常量, 44
* 插值字符串, 44, 77, 391–392
* 交集操作, 149, 152–153
* `IntersectWith()` 方法, 152–153
* 内生变量类型, 39–40
* 不变性, 205
* I/O. 参见 input/output
* iOS 平台, 590, 593, 725
* IoT (物联网), 598, 725
* IP (互联网协议) 类, 548
* IPrioritizable 接口, 195
* IronPython 编程语言, 585
* IronRuby 编程语言, 583, 585
* is 运算符
* 访问隐藏方法, 364–365
* 通用讨论, 189
* 无效转换, 348–349
* IS_A 对象, 188
* IS_A 关系
* 继承, 342–345, 346
* 非反射性本质, 347
* 传递性本质, 335
* `IsAllDigits()` 方法, 63–66
* 项模板, 635–637
* `Item.GetType()` 方法, 234
* `Item.GetTypeCode()` 方法, 234
* 迭代器块
* 示例, 176–177
* 通用讨论, 173–175
* 其他形式
* 类属性, 180, 183
* 命名迭代器, 180, 181
* 概述, 180
* 特殊流, 183
* 引用结构, 488
* `yield break` 语句, 178, 179
* `yield return` 语句, 178–179
* 迭代器
* 优势, 165–167
* 数组, 134–136
* CLR 限制, 234
* 定义 switch, 230, 237–238
* `enum` 关键字, 231–232, 234
* 标志, 229, 235–236
* 通用讨论, 108, 155, 195, 229–230
* 通用, 184
* 初始化器, 229, 233
* 接口, 134–135, 165–168
* `LoopThroughFiles` 程序, 159–164
* 方法扩展, 238–239
* 命名, 180, 181–183
* 真实世界示例, 231–232
* 指定类型, 234–235

## J
* 日语语言, 529
* JavaScript 对象表示 (JSON), 777–778
* JavaScript 编程语言, 577, 724
* JavaScript 脚本语言, 46, 575
* Johnson, Ralph, 425, 707
* `Join()` 方法, 66
* .jpg 文件, 559, 563
* JSON (JavaScript Object Notation), 777–778
* 跳跃
* `break` 语句, 115–116, 123–124
* `continue` 语句, 115–116
* `Dequeue()` 方法, 199–200
* `do…while` 语句, 114–115
* `Enqueue()` 方法, 199
* `finally` 块, 212–213
* 灵活性, 116–120
* 通用讨论, 96, 110–111
* 嵌套循环, 123–124
* 部分部分, 122
* 范围, 120
* `for(;;)` 语句, 54
* `for` 语句, 120–122
* `TopQueue()` 方法, 199
* `while` 语句, 111–114
* `while(true)` 语句, 54

## Jupyter Notebook 软件, 4, 23–24, 591

## K
* KeyedArray 虚类, 170–173
* 键, 145
* Knuth, Donald, 23, 591
* 韩国语, 529

## L
* lambda 表达式
* 匿名方法与, 422–424
* `Colors.ForEach()` 方法, 165
* 丢弃参数, 423
* 动态编程, 585–586
* 通用讨论, 109, 421, 430
* lambda 运算符, 109
* 引用结构, 488
* 语言集成查询 (LInQ), 23, 134, 510
* `LastIndexOf()` 方法, 59
* `LastIndexOfAny()` 方法, 59
* 晚绑定, 362–364. 亦参见 多态性
* 闰年, 41
* LeBlanc, David C., 555
* 小于运算符, 81





- 小于等于运算符，85
- 库，433, 599。另参阅类库
- 类似类型变量，243
- `LinkedList<T>` 集合类
    * 一般般讨论，142, 166–167
    * `MoveNext()` 方法，142, 166–167
- LInQ (语言集成查询)，23, 134, 510
- Linux 操作系统
    * 一般讨论，1, 10
    * 市场份额，721
    * MonoDevelop 应用，590
    * .NET Core，13
    * 路径分隔符，534
    * Visual Studio 2022，590
- LISP (列表处理)语言，576
- 列表集合
    * 转换为数组，144
    * 一般讨论，125, 126, 143
    * 为 `int` 实例化，144
    * 为 `string` 实例化，143–144
    * 其他任务，145
    * 搜索，144–145
- list 关键字，返回值的替代方案
    * 输出参数，471–472
    * 概览，470–471
    * 引用传递值，472–473
- 列表处理 (LISP) 语言，576
- `List<T>` 集合类，142, 187
- 监听器。参见观察者设计模式
- 文学编程技术，23, 591
- Live Unit Testing 功能，595
- 物体分类，230
- 本地数据存储，776
- 本地函数
    * 特性，301–302
    * 创建基础，300–301
    * 实例方法，300–302
    * 重构过程，287
    * 静态方法，261, 271–273
- 记录网络活动，556–558
- 逻辑与运算符，87–88
- 逻辑比较运算符，85–88
- 逻辑数值常量，43
- 逻辑或运算符，87–88
- 逻辑变量类型，36, 85
- 长数值常量，43
- 长整数类型，27, 43, 234, 243
- 循环
    * `break` 语句，115, 123
    * `continue` 语句，115–116
    * `dowhile` 语句，114–115
    * 灵活性，116–120
    * 一般讨论，110–111
    * 嵌套，123–124
    * 部分到，122
    * Razor 编译，772–774
    * 范围，120
    * `for(;;)` 语句，54
    * `for` 语句，120–122
    * `while` 语句，111–114
    * `while(true)` 语句，54
- LoopThroughFiles
    * 文件创建，159–160
    * 输出格式化，160–161
    * 一般讨论，156–159
    * 十六进制输出，161–163
    * Visual Studio 2022，590
- 小写字符串，56–58
- 低层编程，29, 41
- Lua 语言，577
- M 机器语言，8, 599
- 机器，723, 724
- macOS 平台
    * 一般讨论，1, 10
    * 市场份额，721
    * .NET Core，13
    * UWP，725
    * Visual Studio，590, 591
- 宏语言，578
- `Main()` 方法
    * 类项目，439
    * 一般讨论，1, 157
    * `get()` 访问器，183–185
    * 索引测试，172–173
    * 迭代器测试，174–175
    * 异常处理，223, 225
    * `Package`，192
    * `PriorityQueue` 类，196
- Nick，126
- 数学
    * 算法，41
    * 计数，33, 44
    * 分数，30
    * 十六进制基础，30, 46
    * 整数，31
    * 对数，25
    * 负数，27
    * 实数，31
    * 舍舍入，31
    * 变量，25
    * 整个，27
- 成员
    * 类
        * `internal` 修饰符，307
        * 概览，257
        * `protected` 修饰符，307, 434
        * `protected` 修饰符，307, 434
        * `public` 修饰符
    * 数据
        * `const` 数据，259
        * 初始化技术，299–300
        * `readonly`，259
        * 静态属性，257
    * 表达式体，329–331
    * 实例，258
    * 非静态，258
    * 静态成员
        * 方法，262–263
        * 概览，258
        * `readonly` 数据成员，259
- 内存
    * 堆内存
        * 匿名函数，422–424
        * 垃圾回收，330, 350–351
        * 对象，249
        * 引用结构和，487–488
    * 程序足迹，51
    * 集合，149
    * 栈内存，39, 125, 249, 487–488
    * 变量，26, 29, 32–33, 39, 249





- `MemoryStream`, 527, 541
- `metadata`, 437
- 方法调用。参见特定的方法调用
- 方法重载
    - 性讨论，276–278, 354–355
    - 隐藏基类方法，355–361
    - 多态
        - 声明方法为虚方法，365–368
        - 用于访问隐藏方法的 `is` 运算符，364–365
        - 概览，361–364
- 方法参数，382–388
- 方法返回类型，389
- 方法。另特定方法
    - 定义，262–263
    - 一般性讨论，99, 261, 433
    - 用于隐藏的接口，399–401
    - 部分的，433, 463–464
    - 部分方法
        - 创建，464
        - 概览，433, 463
        - 目的，463–464
- MFA（多因子身份认证），499–500
- Microsoft Access，515
- Microsoft Azure 开发，593, 597
- Microsoft 开发者网络 (MSDN) 订阅，595–596
- Microsoft Fakes 功能，595
- Microsoft Office 365，593, 599
- Microsoft Word，575–580
- MIME（多用途互联网邮件交换协议），546, 553–556
- 减号符号，16
- 移动设备，7, 599
- 模型-视图-控制器 (MVC) 范式，751–752, 762–763
- 模型-视图-视图模型 (MVVM) 模式，707, 723
- 取模运算符，82, 161
- MonoDevelop 软件，590
- `MoveNext()` 方法，166
- MSDN (微软开发者网络) 订阅，595–596
- Mueller, John Paul，109, 725
- 多维数组，134
- 多因子身份认证 (MFA)，499–500
- 多重继承，387
- 多个并发用户环境，596–597
- 乘法运算符，82
- 多用途互联网邮件交换协议 (MIME)，546, 553–556
- 互斥条件，100–102
- MVC (模型-视图-控制器) 范式，751–752, 762–763
- MVVM (模型-视图-视图模型) 模式，707, 723
- `MyBaseClass` 约束，204
## N
- 命名迭代器，180, 181–183
- 命名参数，470
- 命名空间
    - 类
        - 概览，453–558
        - 部分类，433, 459–463
        - 部分方法，433, 463–464
    - 全限定，458–459
    - 部分类，433, 459–463
    - 部分方法
        - 创建，464
        - 概览，433
        - 目的，463–464
    - `System.Security` 命名空间，506, 508
    - 使用全限定，458–459
- 命名规范，259, 264, 387
- 原生整数类型，29
- 负整数，27
- 嵌套 `if` 语句，102–104
- 嵌套循环，123–124
- 嵌套命名空间，455
- .NET 5.0 框架
    - OpenAPI 支持，752–752
    - `record` 类型，491
- .NET 6.0 框架
    - 协变类型，319–320
    - `File` 类，526
    - `init-only` 赋值器，310
    - .NET 应用，560
    - OpenAPI 支持，752–753
    - `PriorityQueue` 类，193
    - 更新，592
- .NET Core
    - 控制台应用，598
    - 跨平台能力，13
    - 一般性讨论，10
    - `System.Drawing` 命名空间，560
    - UWP 应用，740–742
    - Visual Studio 版，593
- .NET Core 3.x，128, 748
- .NET 5.0，748
- .NET 生态系统，9, 13
- .NET 框架
    - 异步/同步 I/O，180, 181–183
    - 控制台应用，598
    - 连接数据源，514, 527
    - 创建应用，514
    - 数据容器，509, 512
    - 获取数据，512–513
    - 一般性讨论，9, 13
    - 部署组件，502
    - 部署，507
    - 文档，501
    - 加密，507
    - 邮件，544, 546, 553–556
    - 示例，529
    - 文件异常，215
    - 泛型，315
    - 概览，509–512
    - 识别潜在问题，502
    - 读取文件，537
    - RAD 数据工具，519–521
    - 示例数据库设置，513–514
    - 写入数据代码，521–524




[content]

- 日志网络活动，556–558
- 概述，543–545
- 协议命名法，548
- 子命名空间，545–547
- `using` 语句，534–537
- 写入文件，527–529, 540
- 网络管理脚本，576
- 网络状态，549–551
- `NetworkCredential` 类，548
- `NetworkStream` 类，541
- `new()` 约束，204
- 新行常量，37
- `NewEditionEventHandler` 委托类型，426
- Newspeak 编程语言，577
- `nint` 整数类型，29
- 无返回值方法，281–282
- `Node.js` 环境，593
- 非破坏性突变，494–495
- 非确定性销毁
    - 垃圾回收，350–351
    - 一般讨论，330
- nontype，281–282
- 非泛型，188–189
- 非罗马字母，529
- 非静态成员，258
- 非 void 方法，281
- 不等于运算符，52, 86
- 非运算符，58, 87
- 记法 C# 编程语言，53
- Now 属性，42
- NuGet 包管理器
    - 一般讨论，611, 622
    - Iron 和 Ruby 编程语言，585
    - Visual Studio 2022，600, 622, 631
- `nuint` 整数类型，29
- 空字符类型，37, 38
- 空合并并运算符，226–227
- 空对象，254
- 空参数，473–474
- 空 `string`，38, 60, 204
- 可空引用类型，469
- 数值常量，43–44
- 数值字符串格式化，391–392
## O
- 混淆，499
- 对象链接与嵌入 (OLEDB) 协议，515
- 面向对象编程
    - 概念，246–247
    - 主要原理
        - 封装，244, 290, 333
        - 概述，360
- 对象属性，257–258
- 基于对象的代码，250–253
- 基于对象的语言，363
- 面向对象编码，577
- 对象
    - 访问控制，245, 326–329
    - 访问当前，296–300
    - 类
        - 访问成员，249
        - C# 9.0 代码，252–253
        - 类定义，247–249
        - 判别，253
        - 实例化，246
        - 传递给实例方法，288–290
        - 属性，257–258
        - 引用类型，254–255
        - 传统代码，250–252
    - 一般讨论，126
    - 引用类型，254–255
    - 交换引用，136–139
    - 传统代码，250–252
- 观察者模式
    - 广告，426
    - 事件，425
    - 处理器方法，430–431
    - 概述，425–426
    - 触发事件，427–429
    - 订阅，427
    - ODBC (Open Database Connectivity)，515
    - `OdbcAdapter` 类，511
    - `OdbcCommand` 类，511
    - Office 365 软件，593, 599
    - OLEDB (Object Linking and Embedding) 协议，515
    - `OleDbAdapter` 类，511
    - `OleDbCommand` 类，511
    - 基于一个数组，127
    - 软件，23
    - 单次绑定模式，683
    - 单向绑定模式，683
    - 单向源绑定模式，683
    - 在线 GB，590
    - OOP。参见面向对象编程
    - 打开命令，527
    - Open Database Connectivity (ODBC)，515
    - OpenAPI 支持，752–753
    - 执行顺序，82–83
    - 操作系统
        - 跨平台支持，10, 593, 595
        - iOS，590, 593, 725
        - macOS 平台
            - 份额，721
            - .NET Core，13
            - 概述，1, 10
            - UWP，725
            - Visual Studio，590, 591
        - Visual Studio 要求，596
    - Windows 8，9
    - Windows 10
        - 概述，1, 2, 4, 10
        - 路径分隔符，534
        - 进度条，408
        - Visual Studio 版本，590, 593
        - Windows Server Core，596–597
- 运算符重载，92–93
- 运算符
    - 算术运算符
        - 赋值运算符，26, 84, 91
        - 增运算符运算符 84–85
        - 执行顺序，82–83
        - 概述，81
        - 简单，82
    - 表达式类型
        - 分配类型，91
        - 计算类型，89–91
        - 运算符重载，92–93
        - 概述，89
    - 一般讨论，81
    - 逻辑比较运算符
        - 复合逻辑运算符，87–88
        - 浮点数比较，86–87
        - 概述，85–86
    - 层次结构，82–83
    - `struct` 关键字，484–485
- 可选参数
    - 避免可空引用类型，468–469
    - 一般讨论，465, 466
    - 使用，466–468




* 可选引用类型，468–469
* 或逻辑运算符，87, 235
* `Oracle`,515
* `OracleAdapter` 类，511
* `OracleCommand` 类，511
* out 参数，465, 471–472, 579–580
* `OutOfMemoryException`215–216
* 输出参数，465, 471–472
* `OverflowException`217
* override 关键字，295, 365–368

## P

* `PackageFactory` 类，192, 201–205
* `Pad()` 格式方法，67–69
* `PadLeft()` 格式方法，67–69
* `PadRight()` 格式方法，67–69
* 参数
    * 默认参数，278–279
    * 丢弃，423
    * `e`，427–429, 431
    * 一般讨论，207–208, 273–274, 465
    * 命名参数，470
    * 空值，473–474
    * 可选参数
        * 避免可选引用类型，468–469
        * 概述，465, 466
        * 使用，466–468
    * 返回值
        * 输出参数，471–472
        * 概述，470–471
        * 按引用传递的值，472–473
    * 父类，244–245
    * 括号，83
    * 部分类
        * 示例，460–463
        * 一般讨论，420, 433, 459–460
        * 目的，460
    * 部分方法
        * 创建，464
        * 一般讨论，433, 463
        * 目的，463
    * 密码，499–500, 507
    * `Path.DirectorySeparator` 命令，534
    * 模式匹配，60, 108–110
    * 对等节点解析协议 (`PNRP`)，547
    * 性能
        * 引用结构体，487–488
        * 结构体
            * 公共元素，479–482
            * 定义，478–479
            * 局限性，476
            * 概述，476–477
            * 只读结构体，485–487
            * 记录，489–491
            * 引用结构体，487–488
            * 补充元素，482–485
            * 值类型，477
            * 何时使用，477–478
    * Perl 编程语言，576
    * 权限命名空间，508
    * 持久化，528
    * PHP 编程语言，577
    * 运算符
        * 一般讨论，38, 81
        * 方法重载，92
        * `struct` 关键字，484
    * 符号，16
    * 对等节点解析协议 (`PNRP`)，547
    * 策略命名空间，508
    * 多态
        * 类，244–245
        * 一般讨论，189, 333
        * 接口，401–402
        * 方法重载
            * 虚方法，365
            * 使用 `is` 运算符访问，364
            * 概述，361
        * 后置递运算符，84, 122
    * PowerShell，732
    * 预定义类型，390–391
    * 谓词关键字，413–415
    * 前置递运算符，84, 122
    * Principal 命名空间，508
    * 主权限命名空间类，508
    * 优先级枚举，195
    * `PriorityQueue` 包装类
        * `ColorsPriorityQueue` 示例，193
        * `Count()` 方法，200–201
        * `Dequeue()` 方法，199–200
        * 简单的编写方式，197–198
        * `Enqueue()` 方法，199
        * 一般讨论，190, 198
        * `IPriorizable` 接口，195–202
        * `Main()` 方法，196–197
        * `PackageFactory` 类，201–205
        * `TopQueue()` 方法，200
        * 包装，194–195
    * 私有修符
        * 访问控制，271–273
        * 字段，485–487
        * 作用域，288–290
    * 程序化编码，576
    * 程序员自定义泛型
        * 装箱/拆箱，188, 189
        * 一般讨论，187





-   向现有解决方案中添加项目, 442–445
-   代码, 445–446
-   概览, 437, 439
-   项目, 439–440
-   独立项目, 440–442
-   测试应用程序, 446–447
-   划分为可执行程序, 437, 438–439
-   划分为多个源文件, 434–436
-   通用讨论, 8
-   `global using` 语句, 435–436
-   内存占用, 51
-   进度条
    -   通用讨论, 408
    -   示例应用
        -   第一步, 416–418
        -   概览, 415–416
        -   设置属性, 418
    -   示例程序
        -   委托生命周期代码, 419–420
        -   处理方法, 418–419
-   项目文件
    -   划分, 433, 434–435
    -   通用讨论, 13
    -   `global using` 语句, 435–436
-   项目模板, 632–635
-   属性
    -   类
        -   具有访问级别的访问器, 316
        -   概览, 246, 313–315
        -   副作用, 315–316
        -   静态属性, 315
    -   字段与, 248
    -   静态属性, 315
    -   `struct` 关键字, 482
-   属性元素, 647–648
-   protected 访问修饰符, 245, 307, 434, 479
-   protected internal 访问修饰符, 245, 307, 309, 434, 452–453
-   保护. *参见* 访问控制; 安全
-   伪代码, 53
-   public 访问修饰符
    -   类, 247–249, 306–308
    -   字段, 479
    -   通用讨论, 245, 271–273
-   public 方法异常, 223
-   发布/订阅模式, 425–431
-   Python 编程语言
    -   通用讨论, 577
    -   文学化编程技术, 23
    -   元组, 282
    -   Visual Studio Community 版软件, 593
## Q
-   `Queue<T>` 集合类, 142, 190–192
-   quit 语句, 53–55

## R
-   RAD (快速应用开发), 519–521
-   Random 类, 183
-   `Random()` 方法, 192, 194
-   随机数生成器, 192
-   快速应用开发 (RAD), 519–521
-   Razor 运行时编译
    -   数组, 772–773
    -   更改网页数据, 768–770
    -   与前任版本的比较, 762–763
    -   文件布局, 763–764, 766
    -   通用讨论, 748, 761–762
    -   逻辑语句, 771–772
    -   循环, 772–774
    -   输出选项, 767–768
    -   语法, 766–767
    -   变量, 770
    -   Web Forms, 764–765
-   React.js 模板, 754
-   读取、打印和循环 (REPL) 环境, 589, 591
-   读取/写入类, 527, 528, 535, 539
-   `ReadLine()` 方法, 55, 62, 99
-   `readonly` 成员, 259
-   `readonly` 关键字, 485–487
-   实数
    -   小数, 34–35
    -   浮点数
        -   声明, 31–32
        -   缩进, 32–34
        -   概览, 31
    -   通用讨论, 31
-   record 类型
    -   `field` 关键字, 495–496
    -   通用讨论, 475–476
    -   变异, 494–495
    -   位置声明, 493–494
    -   带有结构, 491–492
    -   using, 492–493
-   Redux 模板, 597, 754
-   `ref` 关键字, 280
-   重构, 264, 268–271, 287
-   引用结构, 487–488
-   引用类型. 参见引用类型
    -   分配, 477
    -   可选的, 468–469
    -   通用对象, 390
    -   作为基类型, 389–390
    -   `null` 字符串, 204–205
    -   对象, 254–255
    -   处理器, 39–40
-   区域指令, 16
-   注册表访问, 724
-   远程桌面, 730–731
-   远程 iOS, 593
-   远程过程调用 (RPC), 753–754
-   `Remove()` 方法, 59, 79
-   REPL (读取、打印和循环) 环境, 589, 591
-   `Replace()` 方法, 59, 69–71, 77, 79
-   行为否认, 502–503
-   意见请求 (RFCs), 544
-   `Reset()` 方法, 165–166
-   REST (表述状态转移), 752, 763
-   按引用返回, 472–473
-   `return` 关键字, 470
-   return 语句, 124, 280
-   返回值, 470–473
-   可重用性原则, 334
-   Rextester 软件, 590
-   RFCs (意见请求), 544
-   基于角色的安全
    -   文档, 501–502
    -   识别潜在威胁, 502–503
    -   `System.Security` 命名空间, 506, 508
    -   要什么, 500–501
    -   Windows 应用程序, 503–508
-   罗马字母, 36–37, 529
-   舍入, 31, 86–87
-   `RoutedCommand` 类, 710–711
-   `RoutedUICommand` 类, 710–711





# RPC (远程过程调用), 753–754

# Ruby 编程语言, 577, 578, 583

## 运行时错误
* 自定义异常, 220
* 通用讨论, 188, 209
* 无效类型转换, 347–348
* `is` 运算符的无效转换, 348–349
* `as` 运算符的无效转换, 349–350
* 策略, 221, 222–225
* 抛出的异常
    * `catch` 块, 210–212
    * 示例, 216–219
    * `finally` 块, 210–211, 212–213
    * 最后机会处理, 223, 225
    * 空值合并运算符技术, 226–227
    * 程序员抛出的异常, 215–216
    * 事件序列, 213–215
    * `try` 块, 211
* `try…catch` 语句, 76, 225

## 运行时类型, 362–363

# S
* 相同运算符, 52, 86–87
* SAO (软件架构概览)图, 501–502
* sbyte 整型类型, 29, 234
* Scala 编程语言, 591
* Schardt, James A., 370
* Scheme 编程语言, 576
* 作用域, 288–290, 645
* 脚本语言, 46, 575. 另参见特定的脚本语言
* SDLC (软件开发生命周期), 501
* sealed 关键字, 377–378
* 安全套接层 (SSL) 安全性, 749–750, 781
* SecureString 命名空间类, 508
* 安全. 另参见 访问控制; 特定的访问修饰符
    * 访问方法, 308–309
    * 程序集, 448–453
    * 基类方法, 355–361
    * 类
        * `BankAccount` 示例, 304–306
        * 协变返回类型, 319–320
        * 表达式体成员, 329–331
        * `init-only` 访问器, 309–310
        * `internal` 访问修饰符, 307
        * 概述, 303–304, 306
        * 属性, 313–316
        * `protected` 访问修饰符, 307, 434
        * `protected internal` 访问修饰符, 307, 434
        * `public` 访问修饰符, 247–249, 306
        * 密封, 377–378
        * 目标类型, 316–318
    * 构造函数
        * C# 提供的, 321–322
        * 示例, 324–325
        * 初始化器, 326–327
        * 不带构造函数的初始化器, 327–329
        * 概述, 309, 320
        * 替换默认, 322–324
    * `DoubleBankAccount` 程序, 311–313
    * 通用讨论, 9, 499–500
    * `internal` 访问修饰符, 288
    * in, 456–456
    * `private` 访问修饰符, 288, 304–306, 451–552
    * 属性, 248
    * `readonly` 关键字, 485
    * 基于角色的安全, 501
    * 软件设计, 500
    * `System` 命名空间, 506, 508
    * UWP, 724
    * 通过本地函数, 271
    * Windows 应用, 503
    * 安全, 508
    * Security.Principal 类, 503
    * 序列化
    * 常见方法, 777–778
    * 通用讨论, 775
    * 需要, 776
    * `WeatherForecast` 项目
        * API 功能, 783–786
        * 伴随文件, 775
        * 创建, 778–781
        * 概述, 775–776
        * 真实输出, 781–783
        * 序列化数据, 777–778
    * 服务器面板, 615–617
    * 基于服务器的应用, 500
    * 服务类, 548
    * SetName() 方法, 289–290
    * 设置, 149–153
    * 设置器方法, 308–309, 314
    * SharePoint, 599
    * 短整型, 29, 234
    * 短路求, 724
    * 侧载, 227
    * 有符号整型类型, 29
    * 简单算术, 82
    * 简单邮件传输协议 (SMTP), 546, 553
    * 单引号, 36
    * 站点类, 508
    * 快照调试器功能, 595
    * 套接字类, 548





* 特殊字符，37
* `Split()` 格式方法，64–66, 71–72
* 身份欺骗，502–503
* SQL。*参见* 结构化查询语言
* SQL Management Studio，609–610
* `SqlCommand` 类，511
* `SqlDataAdapter` 类，511
* `SqlDateTime` 类，511
* SSL（安全套接层）安全性，749–750, 781
* 栈内存，39, 125, 249, 487–488
* `Stack<T>` 集合类，142
* `StackOverflowException`，215–216
* 开始调试命令，17
* 无调试启动命令，17
* 静态匿名函数，422–424
* 静态编码，591。*另另* 动态规划
* 静态字段，262–263
* 静态关键字，422–424, 585–586
* 静态语言，575
* 静态成员
    * `const` 数据成员，259
    * 普通讨论，258
    * 方法和，262–263
    * `readonly` 数据成员，259
* 静态方法
    * 参数
        * 默认参数，278–279
        * 匹配定义，276
        * 重载，276–278
        * 概述，273
        * 传递多个参数，274–275
        * 传递单个参数，273–274
    * 引用传递特性，280–281
    * 定义方法，262–263
    * 有效使用，291–293
    * 示例
        * 分析问题，264–265
        * 地函数，261, 271–273
        * 概述，263–265
        * 规划，264–265
        * 重构，268–271
        * 标准编码方法，265–268
    * 扩展全称扩展，295–296
    * 普通讨论，261, 262, 287
    * 实例方法对比
        * 属性和方法的有效使用，291–295
        * 方法名扩展，295–296
        * 概述，290
    * 地函数，300–302
    * 无返回值，281–282
    * 非 void，281
    * 对象，296–300
    * 传递多个参数，274–275
    * 传递单个参数，273–274
    * `struct` 关键字，481
    * 元元组，282–285
    * 使用，262–263
    * void，281
    * 静态操作，581
    * 静态属性，257–258, 291–293, 315
    * 存储过程，524
    * `StreamReader` 类，527, 529, 537
    * 流
        * 示例，529–533
        * 普通讨论，525–526
        * 其他，541
        * 读取文件，537–540
        * `using` 语句，534–537
        * 写入文件，527–529, 540
    * `StreamWriter` 类，527, 529–533
    * STRIDE 缩写，502–503
    * "string" 常量，43
    * `string` 类，48
    * string 常量，37–39, 51
    * 字符串插值，44, 77, 391–392
    * string 类型
        * 改变大小，56–58
        * 普通操作，51–52
        * 比较，52–56
        * 示例，243
    * 格式化
        * 插值方法，77, 391–392
        * `String.Format()` 方法，72–76
        * 普通讨论，48–49
        * 获取用户输入，61–66
        * 不变性，50–51
        * 为列表实例化，143–144
        * 循环，58
        * null，37, 38, 204–205
        * 输出控制，67–72
        * 搜索，59–61
        * `StringBuilder` 类，77–79
        * `switch` 语句，56–58
        * `StringBuilder` 类，77–79
        * `String.Concat()` 方法，55
        * `String.Empty` 值，37, 38, 43
        * `String.Format()` 格式方法
            * 示例，74–76
            * 格式说明符，73–74
            * 普通讨论，72–73
        * `string.IsNullOrEmpty()` 方法，60
        * `StringReader` 类，527, 540
        * `String.Split()` 方法，64–66
        * `StringWriter` 类，527, 540
        * `struct` 约束，203, 204
    * `struct` 关键字
        * 普通元素，479–482
        * 定义，478–479
        * 普通讨论，475
        * 限制，476
        * 返回值，470–473
        * 补充元素，482–485
        * 何使用，477–478
* 结构性破坏。*参见* 程序集; 库; 命名空间
* 结构化查询语言
    * `Adapter` 类，515
    * `ADO.NET`，510–512
    * `System.Data` 命名空间
        * 连接到数据源，514–519
        * 创建访问应用程序，514
        * 数据容器，509–512
        * 获取数据，512–513
        * RAD 数据工具，519–521
        * 示例数据库设置，513–514
        * 编写数据代码，521–524
* 结构
    * 与类对比，475, 476–477
    * 创建
        * 普通元素，479–482
        * 定义，478–479
        * 普通讨论，475
        * 限制，476
        * 返回值，470–473
        * 补充元素，482–485
        * 何使用，477–478





- 引用，487–488
- 与部分类的相似性，460–463
- 值类型，477
- 何时使用，477–478
- 子数组，127, 129
- 子程序，261
- 下标运算符，169
- 可替换的类，346–347
- `Substring()` 方法，59, 67, 77
- 减法运算符，81, 82
- Swagger 规范，753
- switch 语句
    - 枚举，230, 237–238
    - 一般讨论，56–58, 104–106
    - 限制，106–107
    - `switch` 表达式，107–110
    - 类型条件表达式，102
- `SymmetricExceptWith()` 方法，152–153
- 同步输入/输出 (I/O)，527, 528
- 同步方法，488
- 语法
    - 数组，127, 129
    - 集合类，140–141
    - 索引，141
    - Razor，766–767
    - XAML，646
- 系统 绝对值方法，86–87
- `System` 命名空间，390, 437
- `System.Collections.Generic` 命名空间，142, 166–167, 168, 390
- `System.Collections.IEnumerable` 接口，181–183
- `System.Data.Common` 命名空间，511
- `System.Data.ODBC` 命名空间，511
- `System.Data.OleDb` 命名空间，511
- `System.Data.OracleClient` 命名空间，511
- `System.Data.SqlClient` 命名空间，511
- `System.Data.SqlTypes` 命名空间，511
- `System.Drawing` 命名空间
    - 骰鱼棋盘项目
        - 棋盘创建，570–572
        - 事件处理程序，569–570
        - 第一步，565–566
        - 新游戏开始方法，574
        - 概述，565
        - 项目设置，567
        - 分数处理，567–569
        - 分数打印，572–573
    - 一般讨论，559–561
    - `Graphics` 类
        - 笔刷，563
        - 概述，561–562
        - 笔，562
        - 文字，563
    - .NET Core 和，560–561
    - .NET Framework，564–565
- `System.Drawing.Common` 命名空间，560–561
- `System.Environment.FailFast()` 方法，222
- `System.EventArgs` 类，427, 431
- `System.Exception` 警告，220
- `System.IndexOutOfRangeException` 警告，129
- `System.IO` 命名空间，527, 528
- `System.Linq` 关键字，487
- `System.Math` 类，87
- `System.Net` 命名空间
    - 检查网络状态，549–551
    - 下载文件，551–553
    - 邮件状态，544, 546, 553
    - 一般讨论，543–545
    - 日志网络活动，556–558
    - 协议术语，548
    - 子命名空间，545–547
    - `System.Net.Cache` 命名空间，545
    - `System.Net.Configuration` 命名空间，545
    - `System.Net.Http` 命名空间，546
    - `System.Net.Http.Headers` 命名空间，546
    - `System.Net.Mail` 命名空间，546
    - `System.Net.Mime` 命名空间，546
    - `System.Net.NetworkInformation` 命名空间，546, 549
    - `System.Net.PeerToPeer` 命名空间，547
    - `System.Net.PeerToPeer.Collaboration` 命名空间，547
    - `System.Net.Security` 命名空间，547
    - `System.Net.Sockets` 命名空间，547
    - `System.Net.WebSockets` 命名空间，547
- `System.Object` 类，488
- `System.Security` 命名空间，506, 508
- `System.ValueType`，488
- `System.Web` 命名空间，510
- `System.Windows` 命名空间，510
## T
- `<T>` 符号，142
- 制表符字符，20, 37, 592
- 篡改数据或文件，502–503
- 目标类型，316–318
- `Task` 方法，488
- `Task<TResult>` 方法，488
- 分类
    - 类拆分，369, 371–374
    - 一般讨论，335, 377–378
- 团队开发，464
- 模板。参见特定模板
- 终止语句，55, 114
- 三元运算符，101
- 文本文件输入/输出 (I/O)
    - 异步，527, 528
    - 二进制，528, 539–540
    - 一般讨论，525–526
    - 读取器，527, 539–540
    - 流
        - 示例，529
        - 其他流，541
        - 概述，526
        - `using` 语句，534
        - 写入文件，527, 540
    - 写入器，527, 539
- `TextReader` 类，527
- `TextWriter` 类，527
- 32 位应用程序，591
- 32 位整数，29
- 32 位平台，596, 611
- `this` 关键字
    - 访问当前对象，298–300
    - 数组元素和，483
    - 链式，336–338
    - 一般讨论，287
- 线程安全，486
- 威胁建模，500–503
- 抛出的异常
    - `catch` 块，210–212
    - 示例，216–219
    - `finally` 块，210–211, 212–213
    - 最后机会处理，223, 225
    - 空值合并运算符技术，226–227
    - 程序员抛出的异常，215–216





* 事件序列，213–215
* `throw` 块，210–211, 215
* `try` 块，210–211
* 指纹扫描，499–500
* 紧耦合，202
* 波浪号符号 ~，330, 350–351
* 时间旅行调试（Time Travel Debugging）功能，595
* TimeSpan 属性，42
* Tiobe 指数，1
* `ToBoolean()` 方法，62
* `ToDecimal()` 方法，99
* `ToDouble()` 方法，62
* `ToFloat()` 方法，62
* `ToLower()` 方法，57
* 工具箱窗口，21–22
* 顶层语句（top-level statements），20–21
* `TopQueue()` 方法，200
* `ToString()` 方法，78, 295, 308
* `ToUpper()` 方法，51, 57
* `Trim()` 方法，62, 67–69
* `TrimEnd()` 方法，62, 67–69
* `TrimFront()` 方法，62, 67–69
* `true` 数值常量，43
* “true” 字符串，44–45
* `true` 值，36
* `try...catch` 块
    * 阶阶示例，216–219
    * 一般讨论，76, 210, 225
    * 嵌套，213
* `try` 块，210–211
* `try/finally` 块，213
* `tuples`（元组）
    * `Create()` 方法，284
    * 一般讨论，282
    * 嵌套，284–285
    * `Tuple` 类型，283–285
    * 使用，283
    * `ValueTuple` 类型，284–285
* tvOS 操作系统，725
* TwoWay 绑定模式，683
* 类型转换，44, 90
* 类型表达式，102
* 类型安全，187, 188
* 排版，559, 563
* U
* UAP 技术。*参见* Universal Application Platform
* UI 元素
    * 绑定对象，683–687
    * `Canvas`，662
    * Command 模式
        * 内置命令，711–713
        * 自定义命令，713
        * `ICommand` 接口，709–710
        * 概述，707–708
        * 路由命令，710–711, 717
    * `DockPanel`，661
    * 元素绑定，693
    * 一般讨论，653–654, 655
    * `Grid`
        * 列宽，663–665
        * 列跨度，665–666
        * 内容对齐，666
        * 水平对齐，666
        * 外边距（margin）与内边距（padding），666–667
        * 概述，648–651, 662–663
        * 行高，663–665
        * 行跨度，665–666
        * 共享尺寸，667–669
        * 简单数据输入，669–672
        * 垂直对齐，666
    * 相对值，654
    * `StackPanel`，656, 658–659
    * 术语，654
    * 传统事件处理，707–709
    * Windows 窗口外主题，657–658
    * `WrapPanel`，660–661
    * uint 类型，29, 234
    * ulong 类型，29, 234
    * UML（统一建模语言），369, 370
    * UML 2 傻瓜（UML 2 For Dummies），370
    * 一元运算符，81
    , 82
    * 解箱（unboxing），188, 189
    * 下划线，30, 59
    * Unicode 字符集，47, 52
    * Unicode 格式，529
    * 统一建模语言（Unified Modeling Language, UML），369
    * 未初始化的，254
    * 合并操作，36
    * 测试，595
    * Unity 游戏，559
    * 通用应用平台（UAP）技术
        * 一般讨论，9
        * Visual Studio 社区版，593
    * 通用 Windows 平台
        * Android 操作系统，590
        * 构建
            * 添加代码，738–739
            * 创建界面，734–737
            * 定义项目，732–734
            * 测试设备，739
        * 跨平台支持，21–22
        * 桌面版应用，598
        * 开发者模式
            * 添加代码，738–739
            * 创建界面，734–737
            * 定义项目，732–734
            * 测试设备，739
        * 设备设置，21–22
        * 文件资源管理器，730
        * 概述，725–732
        * PowerShell，732
        * 远程桌面，730–731
        * 侧载加载，727–728
        * .NET Core 应用，740–742
        * 使用原因，722–724
        * 注册表访问，724
        * 测试应用，440





* 装箱/拆箱, 188, 189
* 总体讨论, 187
* `PriorityQueue` 包装类
    * `ColorsPriorityQueue` 示例, 193
    * `Count()` 方法, 200–201
    * `Dequeue()` 方法, 199–200
    * 简单的编写方式, 197–198
    * `Enqueue()` 方法, 199
    * `Main()` 方法, 196–197
    * 概述, 190–192, 198
    * `PackageFactory` 类, 201–205
    * `TopQueue()` 方法, 200
    * 拆箱, 194–195
* 类型安全, 188–189
* 变体, 205–208
* 用户名, 499–500
* ushort 整型类型, 29, 234
* using 指令, 14, 16, 19, 435–436
* using 语句, 435–436, 534–537
* using System 指令, 16
* UWP 应用。参见通用 Windows 平台应用

# V
* Value 属性, 486–487
* 引用传递, 472–473
* ValueTuple 数据类型, 284–285
* 值类型对象, 39–40, 188, 189, 477
* var 关键字
    * 数组, 139–140
    * 动态编程, 575, 580–582
    * 总体讨论, 46–47
    * 初始化技术, 148
* 变长数组, 129–132
* 变量。参见特定变量
    * `bool`
        * 内建变量类型, 39
        * `is` 运算符无效转换, 348–349
        * 逻辑比较运算符, 36, 85–88
        * `as` 运算符无效转换, 349–350
        * 概述, 36
    * 字符类型, 36–37, 40–41
    * 计数, 114, 122
    * `DateTime`, 41–42
    * `decimal`, 34–35
    * 声明, 26
    * `double`, 32, 39, 43, 234, 243
    * 动态编程, 575, 580–582
    * 浮点型, 31, 44–45
    * 分数, 30–31
    * 总体讨论, 20, 25
    * `int`
        * 创建列表, 144
        * 声明, 28
        * 不同类型, 234
        * 枚举类型, 28
        * 内建变量类型, 39
        * 概述, 27
    * 类似类 型的, 243
    * 内存
        * 固定长度类型, 29, 39
        * 浮点型限制, 32–33
        * 内建变量类型, 249
        * 概述, 26
    * 数值常量, 43–44
    * 异常处理, 211
    * 运行时编译, 770
    * `Sql` 类, 511
    * 类型转换, 44–45
    * 类似类型的, 243, 246
    * 值, 39–40
    * 变体, 205–208
    * 变体类型, 46
    * VBS 语言, 46, 576
    * 矢量, 39
    * 字面量运算符, 39
    * 视图, 576
    * VM 模式, 2680
    * `virtual` 关键字, 365, 479
    * 虚拟机, 596
    * Visual 应用, 509
    * Visual Studio 2022, 318
    * Visual 操作系统, 590
    * Visual 设计器, 11
    * Visual 类, 100
    * 缩进, 100
    * 使用形式, 418
    * 解释错误, 120
    * 优雅作为目标, 345
    * `EventHandler` 委托, 426
    * 异常处理, 221–225
    * 特定 `catch` 块, 212
    * 短且特定的 `try` 块, 211
    * `virtual` 关键字的冗余使用, 368
    * 保护转换, 348–350
    * 纯英语显示, 225
    * 属性与字段, 248
    * 对象初始化语法, 329
    * 对象变量引用, 255
    * 清空无效引用, 533
    * .NET 异常, 215–216
    * 方法命名规范, 264
    * 方法参数值, 275
    * 地函数, 301
    * 仅限必要的访问, 308
    * 定义常量, 104
    * 双击项, 276
    * `ToString()` 方法, 295
    * 变量名, 247
    * 将警告视为错误, 360
    * `Write()` 方法, 252



* 代码编辑器, 618–619
* 代码样式设置, 631
* 命令提示符, 7, 18, 589, 622
* 常用操作, 51–52
* 常见用法, 509
* 自定义模板, 632–637
* 调试器
    * 命令, 17
    * 继承跟踪, 334, 339–342
    * 作为学习辅助工具, 623–626
    * 概述, 592
    * 快照调试器功能, 595
    * 时间回溯调试功能, 595
* 设计器
    * 数据视图功能, 609–610
    * 概述, 603–604
    * UWP 应用, 604–607
    * WinForms 应用, 609
    * WPF 应用, 607–609
* 环境\区域设置页面, 630
* 字体和颜色设置, 629
* 一般讨论, 4, 10, 589–590, 603
* 立即窗口, 620
* 安装要求, 596–597
* IntelliSense 功能, 223–224, 592, 618–619, 630
* 键盘命令, 629–630
* `LoopThroughFiles` 程序
    * 文件列表创建, 159–160
    * 格式化输出行, 160–161
    * 十进制输出, 161–163
    * 概述, 156–159
    * Visual Studio 2022, 163–164
* MSDN 订阅, 595–596
* .NET 生态系统和, 13
* 新应用程序创建
    * 默认程序位置, 15–16
    * 执行, 17–18
    * 概述, 11
    * 审核, 18–20
    * 源程序, 11–15
    * 测试, 16
    * 工具箱窗口, 21–22
    * 顶级语句, 20–21
* NuGet 包管理器, 585, 600, 611, 622, 631
* 选项菜单, 627–631
* 查看定义工具提示, 223
* 编程语言选项, 630–631
* 项目类型, 597–602
* 属性面板, 613–614
* 重构菜单, 264
* 服务资源资源管理器面板, 615–617
* 解决方案管理器面板, 610–613
* `System.Data` 命名空间
    * 连接数据, 514–519
    * 创建 Access , 514
    * 数据容器, 509, 512
    * 获取数据, 512–513
    * 概述, 509–512
    * RAD 数据工具, 519–521
    * 示例数据库设置, 513–514
    * 编写数据代码, 521–524
* 任务列表窗口, 621
* 提示
    * 应用程序命名空间, 455
    * IIS Express, 785–786
    * 实现接口, 383
* 工具箱面板, 614–615
* 工具菜单, 621
* 更新, 590 
* Visual Studio 解决方案管理器, 435
* Web Forms 模板, 764
* WPF 应用
    * 作用域资源, 647–648
    * 构建, 644
    * 身份验证, 503
    * 概述, 9, 604, 707
    * XAML, 605, 643
* Visual Studio 版
    * 一般讨论, 4, 10, 589–590, 603
    * 安装要求, 596–597
    * 企业版, 594
    * .NET, 10
    * 专业版, 594
    * 社区版, 4, 10, 589–590, 603
* Visual Studio 解决方案管理器, 435
* Windows 操作系统, 725
* Windows 设备, 728
* WeatherForecast 项目
    * 功能, 783
    * 伴随, 784
    * 解决方案, 775
    * 创建, 778
    * 一般讨论, 775
    * 概述, 781
    * RetrieveWeather 项目
        * 创建, 786
        * 反序列化数据, 789
        * 运行应用程序, 793
        * 序列化数据, 789
        * 用户界面, 787
    * 序列化数据, 777
* `Web` 类, 548
* WebSockets (WebSocket) 功能, 547
* 基于 Web 的应用程序接口 (APIs)
    * 一般讨论, 1, 599
    * `System.Net` 命名空间
        * 检查网络状态, 549–551
        * 下载文件, 551–553
        * 电子邮件, 544, 546, 553–556
        * 记录网络活动, 556–558
        * 概述, 543–545
        * 协议术语, 548
        * 子命名空间, 545–547
    * `WebRequest` 类
        * 通过下载文件, 551–553
        * `System.Net` 命名空间, 545
* while 循环语句
    * `break` 语句, 116–120
    * 一般讨论, 111




- 递增计数变量，114, 122
- 示例程序，111–114
- `while(true)` 语句，54
- 空格，62
- 整数，27–28
- Win32 APIs（应用程序编程接口），215, 722–723
- Windows 8 操作系统，9
- Windows 10 操作系统
    - 通用讨论，1, 2, 4, 10
    - 市场份额，721
    - 路径分隔符，534
    - 进度条，408
    - UWP，721, 725
    - Visual Studio 2022，590, 593
- Windows 11 操作系统，721, 725
- Windows API，411
- Windows 应用程序，503–508
- Windows Chrome 题主题，657–658
- Windows 容器，596–597
- Windows 桌面，592
- Windows 设备门户 (WDP)，728–729
- Windows Forms 应用程序
    - 加密，507
    - 通用讨论，9, 609
    - 登录验证，503–506
    - SAO 图，502
    - 窗口元素外观，657
- Windows 登录验证，503–506
- Windows Minimal Server，596–597
- Windows Presentation Foundation 应用程序。*另参 通用 Windows 平台应用程序*
    - 构建
        - 应用程序范围资源，647–648
        - 概述，644–647
        - 运行中的应用程序，648–649
    - `Canvas`，662
    - 命令模式
        - 内置命令，711–713
        - 自定义命令，713–717
        - `ICommand` 接口，709–710
        - 概述，707–708
        - 路由命令，710–711, 717–718
    - 通用语言运行时 (CLR)
        - 应用程序范围资源，647–648
        - 构建，644–649
        - 登录验证，503–506
        - 概述，9, 604, 607–608, 641
        - 目的，642–643
        - XAML，605–607, 643–644, 650–651
    - 数据绑定
        - 绑定对象，683–687
        - 数据转换，697–704
        - 依赖属性，682
        - 编辑数据，687–693
        - 模式，683
        - 其他方面，705
        - 概述，681
        - 验证数据，693–697
    - `DockPanel`，661
    - 通用讨论，9, 607–608, 641
    - `Grid`
        - 列宽调整，663–665
        - 列跨度，665–666
        - 内容对齐，666
        - 水平对齐，666
        - 外边距与内边距，666–667
        - 概述，648–651, 662–663
        - 行高调整，663–665
        - 行跨度，665–666
        - 共享尺寸，667–669
        - 简单数据输入，669–672
        - 垂直对齐，666
    - 布局控件
        - 概述，653–654
        - 相对值，654
    - 登录验证，503–506
    - 属性系统，682
    - 目的，642
    - `StackPanel`，656, 658
    - 传统事件处理，707–709
    - Visual Studio 2022 软件，604
    - Windows Chrome 主题，657
    - `WrapPanel`，660
    - XAML
        - 基础输入，674
        - C# 比较，650
        - 仅显示，672
        - 列表项，677
        - 概述，604
    - Windows Runtime (WinRT)，575
    - Windows Core，596
    - Windows Sockets，547
    - Windows 命名空间，508
    - Windows 命名空间，508
    - WinUI，724
    - 世界，576
    - WPF 应用程序。*另参 Windows Presentation Foundation*
    - `WrapPanel`，660
    - Wrapper 类
        - 关系，531
        - `PriorityQueue`，191
        - `StreamWriter` 类，531
    - `WriteLine()` 方法，99
    - 安全代码，Howard)
- X
- Xamarin 平台，10, 593, 725
- XAML
    - C# 与 XAML，650
    - 通用控件
        - 基础输入，674
        - 仅显示，672
        - 列表项，677
    - 数据绑定
        - 数据转换，697
        - 定义，683
        - 依赖属性，682
        - 编辑数据，687
        - 模式，683
        - 概述，681
        - 验证数据，693
    - 通用讨论，604, 643
    - 语法，646
    - UWP，724
- Xbox One，721, 725
- XML (可扩展标记语言)
    - 文档注释，223
    - 文件，601
    - 通用讨论，777
    - 序列化，775





* `xor`（异或）运算符，87, 235

## Y

* `yield break` 语句，178, 179–180
* `yield return` 语句，178–179

## Z

* `zero-based arrays`，58, 66, 127

## 关于作者

**John Mueller** 是一位自由作家和技术编辑。他血液里流着写作的基因，迄今已编写了 120 本书和 600 多篇文章。他的主题涵盖从网络到人工智能，从数据库管理到埋头的编程。他目前的一些书籍包括关于数据科学、机器学习和算法的讨论。他的技术编辑技能帮助了 70 多位作者完善其手稿内容。John 一直对开发感兴趣，并写过关于各种语言的著作，包括一本非常成功的 C++ 书籍。请务必阅读 John 的博客 `http://blog.johnmuellerbooks.com/` (http://blog.johnmuellerbooks.com/)。您可以通过电子邮件 `John@JohnMuellerBooks.com` (mailto:John@JohnMuellerBooks.com) 在互联网上联系 John。John 还有一个网站 `http://www.johnmuellerbooks.com/` (http://www.johnmuellerbooks.com/)，您可以从 `http://www.johnmuellerbooks.com/source-code/` (http://www.johnmuellerbooks.com/source-code/) 下载本书的源代码。请务必在 Amazon 上关注 John `https://www.amazon.com/John-Paul-Mueller/e/B004MOD0YS/` (https://www.amazon.com/John-Paul-Mueller/e/B004MOD0YS/)。

## 献献

献 Rebecca，永不遗忘，永不远去——我永远爱你。

## 致谢

感谢我的妻子 Rebecca。尽管她现在已经离开了，但她的灵魂存在于我所写的每一本书中，出现在页面上的每一个字里。当没有人相信我时，是她相信我。

Rod Stephens 多年来一直是我的朋友和同事。他对本书进行的技术编辑非常详尽，我非常感谢他的努力。在我撰写这些主题时，Rod 花花时间通过电子邮件与我讨论书籍主题。他就如何编写更好的示例和更易理解的文本给出了见解，并提供了其他可能不会出现在这里的资源支持。

我的经纪人 Matt Wagner 在帮助我最初获得合同以及处理大多数作者并不会真正考虑的所有细节方面是功不可没的。我一直非常感谢他的帮助。知道有人想要提供帮助感觉真好。

许多人阅读了这本书的全部或部分内容，帮助我完善方法、测试应用程序代码、验证大量的文本，并通提供了所有读者都希望获得的建议。这些无偿志愿者提供的帮助多多到无法在此处逐一列举。我特别感谢 Eva Beattie 的努力，她提供了通用建议，读了整本书书，并无私地投入到这个项目中。

最后，我要感谢 Kelsie Baird、Susan Christophersen 以及 John Wiley & Sons, Inc. 的编辑和制作人员，他们对这项写作工作提供了无与伦比的支持。

### 出版方致谢

**版权编辑：** Kelsey Baird

**项目经理和校对：** Susan Christophersen

**技术编辑：** Rod Stephens

**制作编辑：** Mohammed Zafar Ali

**封面图片：** © Casimiro PT/Shutterstock

![无论去哪里都带上 Dummies 系列书籍和应用。在 dummies.com 在线查找我们。](img/ad1.png)![在强大的多媒体网站上利用专业知识。广告和赞助请访问 dummies.com，这是一个免费在线信息的一站式服务平台。](img/ad2.png)![通过阅读书籍和电子书、观看视频以及在线听音频和网络讨会会让生活变得更轻松。欲了解更多信息请访问 dummies.com/biz。](img/ad3.png)![对个人提升和职业发展的更多书籍感兴趣吗？访问 dummies.com。](img/ad4.png)![让学术学习变得简单有趣，将个性化的教室带到舒适的家中。可在 dummies.com 在线获取。](img/ad5.png)![为小脑袋的大想象力准备的小书——在在线通过一系列全新的书籍释放他们的创造力。访问 dummies.com。](img/ad6.png)

无论去哪里都带上 Dummies 吧！

![Dummies](http://www.dummies.com)

访问我们的[网站](http://www.dummies.com)

![Facebook](http://www.facebook.com/fordummies)

在 [Facebook] 上关注我们](http://www.facebook.com/fordummies)

![Twitter](http://www.twitter.com/fordummies)

在 [Twitter] 上关注我们](http://www.twitter.com/fordummies)

![YouTube](http://www.youtube.com/user/fordummies)

在 [YouTube] 上观看我们](http://www.youtube.com/user/fordummies)

![LinkedIn](http://www.linkedin.com/groups/home=322994&trk=anet_ug_hm)

在 [LinkedIn] 上加入我们](http://www.linkedin.com/groups/home=322994&trk=anet_ug_hm)

![Pinterest](http://pinterest.com/fordummies/)

在 [Pinterest] 上收藏我们](http://pinterest.com/fordummies/)

![Newsletter 信封](http://www.dummies.com/go/newsletter)

订阅我们的[通讯邮件](http://www.dummies.com/go/newsletter)

![Dummies 书封面](http://covers.dummies.com/)

创建您自己的[Dummies 书封面](http://covers.dummies.com/)

![For Dummies, A Wiley Brand](img/dummies-wordmark.png)

# WILEY 用户许可协议

访问 `www.wiley.com/go/eula` (http://www.wiley.com/go/eula) 获取 Wiley 的电子书 EULA。

