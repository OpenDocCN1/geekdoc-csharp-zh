# 开发者应该了解的 50 个 C# 概念



![](img/image_rsrc7CJ.jpg)








# 33. C# 设计模式
## 创建模式
## 结构型模式
## 行为模式

# 34. Windows Forms 和 WPF 应用程序
## Windows Forms (WinForms)
## Windows Presentation Foundation (WPF)
## WinForms 和 WPF 的主要区别

# 35. 使用 ASP.NET 创建 Web 应用
## ASP.NET MVC 简介
## ASP.NET Core 和 Razor Pages
## ASP.NET 核心概念

# 36. 用于开发的 Blazor 简介
## 理解 Blazor
## 创建 Blazor 应用
## Blazor 的核心特性
## Blazor 与其他框架的对比

# 37. 使用 Web API 创建 RESTful 服务
## Web API 简介
## 创建简单的 Web API
## 在 Web API 中处理数据
## Web API 安全性

# 38. 使用 ADO.NET 操作数据库
## ADO.NET 简介
## 连接数据库
## 执行 SQL 查询
## 执行存储过程
## 使用 DataSets 和 DataAdapters
## 处理事务

# 39. 在 C# 中操作 NoSQL 数据库
## NoSQL 数据库简介
## 连接到 MongoDB
## 操作集合 (Collections)
## 使用对象文档映射 (ODM)

# 40. C# 中的 Docker 和容器化
## Docker 和容器简介
## 使用 Docker 将 C# 容器化
## 用于多容器应用程序的 Docker Compose

# 41. 微服务架构简介
## 微服务与 C#

# 42. 创建和消费 WCF 服务
## 创建 WCF 服务
## 消费 WCF 服务

# 43. C# 与云计算 (Azure, AWS, GCP)
## 云计算简介
## C# 与 Microsoft Azure
## C# 与 Amazon Web Services (AWS)
## C# 与 Google Cloud Platform (GCP)
## C# 中常见的云开发任务

# 44. 用于跨平台开发的 Xamarin 简介
## Xamarin 概览
## Xamarin.Forms
## Xamarin.Native
## Xamarin.Essentials
## Xamarin.Forms vs. Xamarin.Native
## Xamarin 社区与工具链

# 45. 使用 Unity 和 C# 进行游戏开发
## Unity 简介
## Unity 中的 C# 脚本
## Unity 物理与动画
## Unity UI 与输入
## Unity 资产与资源
## 构建与部署游戏
## Unity 和 C# 脚本最佳实践
## Unity 与协作开发

# 46. 使用 ML.NET 进行机器学习与 AI 
## 机器学习简介
## ML.NET 数据流水线
## 使用 ML.NET 进行训练
## ML.NET 消费
## 高级 ML.NET 特性
## ML.NET 与 .NET 应用的集成

# 47. C# 与原生代码的互操作性
## 互操作性简介
## P/Invoke (平台调用)
## C++/CLI (托管 C++)
## COM 互操作
## 安全考量
## 调试与诊断

# 48. C# 中的国际化与本地化
## 理解国际化
## 为本地化准备您的应用程序
## 处理复数和性别
## 动态语言切换
## 测试与质量保证

# 49. C# 代码最佳实践
## 代码结构与组织
## 错误处理与日志记录
## 性能优化
## 代码注释与文档
## 单元测试与测试驱动开发 (TDD)
## 版本控制与协作
## 安全最佳实践
## 持续集成与部署 (CI/CD)

# 50. C# 中的持续集成与部署 (CI/CD)
## CI/CD 简介
## 设置持续集成
## 实现自动化测试
## 持续部署
## 处理密钥与安全性
## 监控与回滚

# 引言
这本书非常出色，因为它不仅包含了基础概念，还涵盖中级和高级概念。

* 基础数据类型
* C# 中的持续集成与部署 (CI/CD)
* C# 代码最佳实践
* C# 中的国际化与本地化
* C# 与原生代码的互操作性
* C# 设计模式

以及许多其他概念，这些概念将帮助你对 C# 编程语言更有信心。
通过了解这些概念，你将开始更高效地处理 `# Syntax`，并能帮助你快速处理大部分的 `Code`。

# 1. 基础数据类型
### 什么是 C#？
`C# (读作 C-sharp)` 是一种由微软开发的现代面向对象编程语言。它最初为构建 Windows 应用程序而设计，但已演变为一种多用途语言，用于各种软件开发，包括 Web 应用、移动应用等。

### C# 的核心特性
* 面向对象：`C#` 支持面向对象编程原则，使得代码的组织和结构更加容易。
* 类型安全：`C#` 是一种静态类型语言，意味着变量必须声明特定的数据类型，增强了代码安全性。
* 互操作性：`C#` 可以与其他语言无缝互操作，特别是 `.NET` 生态系统中的语言。
* 内存管理：它通过垃圾回收实现了自动内存管理，减少了内存泄漏的风险。

### .NET Framework
`C#` 与 `.NET Framework` 密切相关，这是一个用于构建、部署和运行应用程序的综合平台。`.NET Framework` 为 `C#` 和其他语言提供了运行时环境、大型类库以及各种开发工具。

### C# 和 .NET Framework 版本
`C#` 和 `.NET Framework` 在多年来一直在演进，每个版本都引入了新功能和改进。开发者应该注意他们正在使用的版本，因为这可能会影响语言特性和兼容性。

### 设置开发环境





要开始编写 C# 代码，你需要一个开发环境。Microsoft Visual Studio 是一个用于 C# 开发的流行集成开发环境 (IDE)。它提供了一个用户友好的界面、强大的调试工具以及与 .NET Framework 的无缝集成。

## 你的第一个 C# 程序

让我们写一个简单的“Hello, World!”程序来开始你的 C# 之旅：

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, World!");
    }
}
```

这个基础示例演示了 C# 程序的结构，包括 `using` 指令和 `Main` 方法，后者是程序的入口。

这段介绍为理解 C# 及其与 .NET Framework 的关系奠定了基础。当你深入学习后续主题时，你将探索该语言的特性及其构建各种应用程序的庞大生态系统。

# 2. C# 数据类型与变量

## 数据类型

在 C# 中，每个变量都有一个数据类型，规定了它可以存储的数据种类。C# 中常见的数据类型包括：

- 整数类型：`int`、`long`、`short`、`byte`
- 浮点类型：`float`、`double`
- 小数类型：`decimal`
- 字符类型：`char`
- 布尔类型：`bool`
- 字符串类型：`string`

选择正确的数据类型对于高效的内存使用和数据的准确表示至关重要。

## 声明变量

变量用于存储程序中的数据。在 C# 中，你通过指定数据类型和名称来声明变量。

例如：

```csharp
int age;
float price;
string name;
```

## 变量初始化

变量可以在声明时或程序稍后进行初始化（赋一个初始值）。

以下是两种者的示例：

```csharp
int quantity = 10; // 声明时初始化
float temperature; // 声明但不初始化
temperature = 98.6f; // 程序中稍后初始化
```

## 类型推断 (var 关键字)

C# 支持使用 `var` 关键字进行类型推断，允许编译器根据赋值的值自动确定数据类型。

例如：

```csharp
var count = 5; // 编译器推断为 int
var price = 19.99; // 编译器推断为 double
```

## 常量

常量是在赋值后值无法更改的变量。它们使用 `const` 关键字声明：

```csharp
const double PI = 3.14159;
```

## 数据类型之间的转换

C# 支持兼容数据类型之间的隐式和显式转换。隐式转换自动完成，而显式转换需要使用强制类型转换。

例如：

```csharp
int numInt = 10;
double numDouble = numInt; // 隐式转换
int newInt = (int)numDouble; // 显式转换（强制转换）
```

## 可空类型

在 C# 中，值类型不能赋予 `null` 值。然而，通过使用可空类型，你可以显式允许值类型为 `null`。

例如：

```csharp
int? nullableInt = null;
```

理解 C# 数据类型和变量是编写健壮且高效程序的基础。随着学习的深入，你会遇到选择正确的数据类型和有效管理变量对于成功应用开发至关重要的情况。

# 3. C# 中的运算符与表达式

## 运算符简介

C# 中的运算符是是对变量和值执行操作的符号。理解这些运算符对于在程序中处理数据和执行计算至关重要。

## 算术运算符

算术运算符用于基础数学运算。它们包括：

- 加法 (`+`)：将两个操作数相加。
- 减法 (`-`)：从左操作数减去右操作数。
- 乘法 (`*`)：两个操作数相乘。
- 除法 (`/`)：将左操作数除以右操作数。
- 取模 (`%`)：返回除法的余数。

```csharp
int a = 10;
int b = 3;
int sum = a + b; // 13
int difference = a - b; // 7
int product = a * b; // 30
int quotient = a / b; // 3
int remainder = a % b; // 1
```

## 比较运算符

比较运算符用于比较值。它们包括：

- 等于 (`==`)：检查两个操作数是否相等。
- 不等于 (`!=`)：检查两个操作数是否不等。
- 大于 (`>`)：检查左操作数是否大于右操作数。
- 小于 (`<`)：检查左操作数是否小于右操作数。
- 大于等于 (`>=`)：检查左操作数是否大于或等于右操作数。
- 小于等于 (`<=`)：检查左操作数是否小于或等于右操作数。

```csharp
int x = 5;
int y = 8;
bool isEqual = x == y; // false
bool isNotEqual = x != y; // true
bool isGreaterThan = x > y; // false
bool isLessThan = x < y; // true
bool isGreaterOrEqual = x >= y; // false
bool isLessOrEqual = x <= y; // true
```

## 逻辑运算符

逻辑运算符用于执行逻辑操作。它们包括：

- 逻辑与 (`&&`)：如果两个操作数都为真则返回真。
- 逻辑或 (`||`)：如果至少有一个操作数为真则返回真。
- 逻辑非 (`!`)：如果操作数为假则返回真，反之亦然。

```csharp
bool condition1 = true;
bool condition2 = false;
bool resultAnd = condition1 && condition2; // false
bool resultOr = condition1 || condition2; // true
bool resultNot = !condition1; // false
```

## 赋值运算符

赋值运算符用于赋予值。它们包括：

- 赋值 (`=`)：将右值赋给变量。
- 加赋值 (`+=`)：将右值加到变量。

```csharp
int num = 10;
num += 5; // num 为 15
```

## 增减运算符

增减运算符用于将变量增加或减少 1。

- 递增 (`++`)：增加 1。
- 递减 (`--`)：减少 1。

```csharp
int counter = 5;
counter++; // counter 为 6
counter--; // counter 为 5
```

## 条件运算符 (三元运算符)

条件运算符 (`? :`) 是 `if-else` 语句的简写。它根据条件的求值返回两个值之一。

```csharp
int a = 10;
int b = 5;
int max = (a > b) ? a : b; // max 为 10
```

运算符是 C# 中执行操作的基础构建块。通过掌握这些运算符，你将获得创建复杂表达式、决策和有效管理变量的能力。

# 4. 控制结构 (if-else, 循环)

C# 中的控制结构用于管理程序的执行流。它们允许根据条件进行决策。两种主要的控制结构是 if-else 语句和循环。

### if-else 语句

if-else 语句用于条件执行。它们允许程序根据条件的真假采取不同的路径。

### if 语句

```csharp
int num = 10;
if (num > 0) {
    Console.WriteLine("这是一个正数.");
}
```

### if-else 语句

```csharp
int num = -5;
if (num > 0) {
    Console.WriteLine("这是一个正数.");
}
else {
    Console.WriteLine("这不是正数.");
}
```

### if-else-else 语句

```csharp
int num = 0;
if (num > 0) {
    Console.WriteLine("这是一个正数.");
} else if (num < 0) {
    Console.WriteLine("这是一个负数.");
} else {
    Console.WriteLine("这是一个零.");
}
```

## 循环

循环允许重复执行某个代码块。C# 中有多种类型的循环。

### for 循环

`for` 循环在迭代次数已知时使用。

```csharp
for (int i = 1; i <= 5; i++) {
    Console.WriteLine($"迭代 {i}");
}
```

### while 循环

`while` 循环在迭代次数预先知时使用。

```csharp
int count = 0;
while (count < 3) {
    Console.WriteLine($"计数: {count}");
    count++;
}
```





### do-While 循环
do-while 循环类似于 while 循环，但它保证循环体至少执行一次。

```csharp
int attempt = 0;

do
{
    Console.WriteLine($"Attempt: {attempt}");
    attempt++;
} while (attempt < 3);
```

### foreach 循环
foreach 循环用于遍历集合（例如数组或列表）中的元素。

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };

foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```

### 嵌套控制结构
你可以将控制结构嵌套彼此以创建更复杂的逻辑。

```csharp
int x = 10;
int y = 5;
if (x > 0)
{
    if (y > 0)
    {
        Console.WriteLine("Both x and y are positive.");
    }
    else
    {
        Console.WriteLine("x is positive, but y is non-positive.");
    }
}
else
{
    Console.WriteLine("x is non-positive.");
}
```

控制结构对于确定 C# 程序的流至关重要。掌握 if-else 语句和循环让你能够创建动态且响应的应用程序。

# 5. 方法和函数

在 C# 中，方法是执行特定任务的代码块，可以从程序的其他部分调用。方法促进了代码重用、可读性和模块化。

## 方法的声明与调用

### 方法声明
```csharp
public class Calculator
{
    // 方法声明
    public int Add(int a, int b)
    {
        return a + b;
    }
}
```

### 调用方法
```csharp
Calculator calculator = new Calculator();
int result = calculator.Add(3, 5);
Console.WriteLine(result); // 输出: 8
```

### 方法参数

### 必需参数
```csharp
public class MathOperations
{
    public int Multiply(int x, int y)
    {
        return x * y;
    }
}
```

### 可选参数
```csharp
public class Printer
{
    // 带有默认值的可选参数
    public void PrintMessage(string message, bool uppercase = false)
    {
        if (uppercase)
        {
            Console.WriteLine(message.ToUpper());
        }
        else
        {
            Console.WriteLine(message);
        }
    }
}
```

### 返回类型

### 有返回值的方法
```csharp
public class Circle
{
    public double CalculateArea(double radius)
    {
        return Math.PI * radius * radius;
    }
}
```

### Void 方法
```csharp
public class Logger
{
    // Void 方法（无返回值）
    public void LogError(string errorMessage)
    {
        Console.WriteLine($"Error: {errorMessage}");
    }
}
```

### 方法重载
方法重载允许你定义多个具有相同名称但不同参数列表方法。

```csharp
public class OverloadedMethods
{
    public int Add(int a, int b)
    {
        return a + b;
    }
    public double Add(double a, double b)
    {
        return a + b;
    }
}
```

### 递归方法
方法可以调用自己，创建一个递归函数。

```csharp
public class FactorialCalculator
{
    public int CalculateFactorial(int n)
    {
        if (n == 0 || n == 1)
        {
            return 1;
        }
        else
        {
            return n * CalculateFactorial(n - 1);
        }
    }
}
```

方法和函数在构建 C# 程序结构中起着关键作用。它们允许你封装逻辑、提高重用性并增强代码的可读性。在你继续 C# 之旅时，掌握方法声明、参数处理以及理解返回类型将使你能够设计出稳健且模块化的应用程序。

# 6. 类和对象

在 C# 中，类是面向对象编程的基石。类是创建对象的蓝图，而对象是类的实例。这种范式允许你对现实世界的实体和行为进行建模。

## 类声明

##### 基础结构
```csharp
public class Car
{
    // 字段（属性）
    public string Model;
    public string Color;
    // 构造函数
    public Car(string model, string color)
    {
        Model = model;
        Color = color;
    }
    // 方法（行为）
    public void Start()
    {
        Console.WriteLine($"{Color} is starting.");
    }
    public void Drive()
    {
        Console.WriteLine($"{Color} is on the move.");
    }
}
```

##### 创建对象（实例化）
```csharp
class Program
{
    static void Main()
    {
        // 创建对象
        Car myCar = new Car("Toyota", "Blue");
        Car anotherCar = new Car("Honda", "Red");
        // 访问字段
        Console.WriteLine($"My car is {myCar.Color} {myCar.Model}.");
        // 调用方法
        myCar.Start();
        anotherCar.Drive();
    }
}
```

### 构造函数
构造函数是在对象创建时调用的特殊方法。它们初始化对象的的状态。

##### 默认构造函数
```csharp
public class Person
{
    public string Name;
    // 默认构造函数
    public Person()
    {
        Name = "John Doe";
    }
}
```

##### 参数构造函数
```csharp
public class Book
{
    public string Title;
    public string Author;
    // 参数构造函数
    public Book(string title, string author)
    {
        Title = title;
        Author = author;
    }
}
```

### 属性
属性提供了对类字段的控制访问。

```csharp
public class Student
{
    // 私有字段
    private int _age;
    // 带有 get 和 set 访问器的公共属性
    public int Age
    {
        get { return _age; }
        set
        {
            if (value >= 0 && value <= 120)
            {
                _age = value;
            }
            else
            {
                Console.WriteLine("Invalid age value.");
            }
        }
    }
}
```

### 封装
封装是将数据（字段）和操作数据的方法封装在单个单元（类）中的实践。

```csharp
public class BankAccount
{
    private decimal _balance;
    public void Deposit(decimal amount)
    {
        _balance += amount;
    }
    public void Withdraw(decimal amount)
    {
        if (amount <= _balance)
        {
            _balance -= amount;
        }
        else
        {
            Console.WriteLine("Insufficient funds.");
        }
    }
    public decimal GetBalance()
    {
        return _balance;
    }
}
```




多态允许将对象被视为其基类的实例，即使它们实际上是派生类的实例。

### 方法重写

```csharp
public class Cat : Animal
{
    // 方法重写
    public override void Eat()
    {
        Console.WriteLine("Cat is eating.");
    }
}
```

### 使用多态

```csharp
Animal myAnimal = new Dog();
myAnimal.Eat(); // 调用 Dog 类中重写的 Eat 方法
myAnimal = new Cat();
myAnimal.Eat(); // 调用 Cat 类中重写的 Eat 方法
```

### virtual 和 override 关键字

```csharp
public class Shape
{
    // 虚方法
    public virtual void Draw()
    {
        Console.WriteLine("Drawing a shape.");
    }
}

public class Circle : Shape
{
    // 重写方法
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle.");
    }
}
```

### 抽象类和方法

```csharp
public abstract class Shape
{
    // 抽象方法
    public abstract void Draw();
}

public class Circle : Shape
{
    // 抽象方法的实现
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle.");
    }
}
```

继承和多态是强大的概念，它们增强了你 C# 代码的结构和灵活性。利用这些特性允许你构建类层次结构、创建可重用的代码并设计能够适应不断变化的系统。

# 8. 接口和抽象类

接口和抽象类是 C# 面向对象编程的核心组件。它们提供了一种为类定义约的方法，强制执行共同行为并确保代码库的一致性。

## 接口

接口是一种约，定义了类必须实现的一组方法和属性。它允许多继承，使一个类可以实现多个接口。

#### 声明接口

```csharp
public interface ILogger
{
    void LogMessage(string message);
    void LogError(string errorMessage);
}
```

### 实现接口

```csharp
public class ConsoleLogger : ILogger
{
    public void LogMessage(string message)
    {
        Console.WriteLine($"Message: {message}");
    }

    public void LogError(string errorMessage)
    {
        Console.WriteLine($"Error: {errorMessage}");
    }
}
```

### 使用接口

```csharp
ILogger logger = new ConsoleLogger();
logger.LogMessage("Informational message");
logger.LogError("Critical error");
```

### 抽象类

抽象类是一种不能独立实例化的类，它可能包含抽象方法（没有体的方法），这些方法必须由派生类实现。

#### 声明抽象类

```csharp
public abstract class Shape
{
    // 抽象方法
    public abstract void Draw();
    // 普通方法
    public void Move()
    {
        Console.WriteLine("Moving the shape.");
    }
}
```

#### 实现抽象类

```csharp
public class Circle : Shape
{
    // 实现抽象方法
    public override void Draw()
    {
        Console.WriteLine("Drawing a circle.");
    }
}
```

#### 抽象属性

```csharp
public abstract class Animal
{
    // 抽象属性
    public abstract string Species { get; }
    // 普通方法
    public void Eat()
    {
        Console.WriteLine("Animal is eating.");
    }
}
```

#### 使用抽象类

```csharp
Shape myShape = new Circle();
myShape.Draw(); // 调用 Circle 类中重写的 Draw 方法
myShape.Move(); // 调用抽象类中的 Move 方法

Animal myAnimal = new Dog();
Console.WriteLine($"Species: {myAnimal.Species}"); // 调用 Dog 类中重写的属性
myAnimal.Eat(); // 调用抽象类中的 Eat 方法

### 什么时候使用接口和抽象类

接口：当你想要定义一个多个类都可以实现的约时（无论继承关系如何），请使用它。
抽象类：当你想要为基类提供共享功能并强制派生类实现某些方法时，请使用它。

# 9. 异常处理

异常处理是编写健壮且可靠的 C# 应用程序的关键部分。通过使用 try-catch 块、在需要时抛出异常以及实施适当的错误处理策略，你可以确保代码能够优雅地处理意外情况。

## 理解异常

在 C# 中，异常是破坏程序正常执行流的运行时错误。

### Try-Catch 块

`try-catch` 块用于处理异常。

```csharp
try
{
    // 可能抛出异常的代码
    int result = 10 / int.Parse("0");
}
catch (DivideZeroException ex)
{
    // 处理特定异常
    Console.WriteLine($"Error: {ex.Message}");
}
catch (Exception ex)
{
    // 处理任何其他异常
    Console.WriteLine($"Unexpected error: {ex.Message}");
}
finally
{
    // 始终执行的代码
    Console.WriteLine("This always executes.");
}
```

### 抛出异常

你可以使用 `throw` 关键字手动抛出异常。当你想要指示发生了某些特定条件或错误时，这非常有用。

```csharp
public class Calculator
{
    public int Divide(int dividend, int divisor)
    {
        if (divisor == 0)
        {
            throw new DivideZeroException("Cannot divide by zero.");
        }
        return dividend / divisor;
    }
}
```

### 自定义异常

你可以通过派生 `Exception` 类来创建自己的异常类。这使你能够为应用程序定义特定的异常类型。

```csharp
public class CustomException : Exception
{
    public CustomException(string message) : base(message)
    {
    }
}
```

### 异常过滤器

异常过滤器允许你根据特定条件捕获异常。此功能在 C# 6.0 中引入。

```csharp
try
{
    // 可能抛出异常的代码
    int result = 10 / int.Parse("0");
}
catch (DivideZeroException ex) when (ex.Message == "Attempted to divide by zero.")
{
    // 使用过滤器处理特定异常
    Console.WriteLine($"Error: {ex.Message}");
}
```

### 全局异常处理

在较大的应用程序中，你可以实现全局异常处理来捕获未处理的异常并记录或显示它们的信息。

```csharp
static void Main()
{
    AppDomain.CurrentDomain.UnhandledException += GlobalExceptionHandler;
    // 程序的其余代码
}

private static void GlobalExceptionHandler(object sender, UnhandledExceptionEventArgs e)
{
    Exception exception = (Exception)e.ExceptionObject;
    Console.WriteLine($"Global Exception Handler: {exception.Message}");
}
```

# 10. C# 数组和列表

数组和列表是 C# 中的基础数据结构，允许你存储和操作元素集合。理解它们的用法对于程序中处理结构化数据至关重要。

## 数组

声明和初始化：C# 中的数组是相同数据类型的固定大小集合。





```csharp
int[] numbers = new int[5] { 1, 2, 3, 4, 5 };
```

### 访问元素

### 访问元素
```csharp
int firstElement = numbers[0]; // 访问第一个元素 (索引 0)
```

## 遍历数组

### 遍历数组
```csharp
foreach (int number in numbers)
{
    Console.WriteLine(number);
}
```

### 多维数组

### 多维数组
```csharp
int[,] matrix = new int[3, 3]
{
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

## 列表

### 声明与初始化
列表提供了具有额外功能的动态数组。

### 声明与初始化
```csharp
List<string> names = new List<string>() { "Alice", "Bob", "Charlie" };
```

### 添加和删除元素

### 添加和删除元素
```csharp
names.Add("David"); // 添加一个元素
names.Remove("Bob"); // 按值删除元素
names.RemoveAt(0); // 按索引删除元素
```

### 访问元素

### 访问元素
```csharp
string firstElement = names[0]; // 访问第一个元素 (索引 0)
```

### 遍历列表

### 遍历列表
```csharp
foreach (string name in names)
{
    Console.WriteLine(name);
}
```

## 数组 vs. 列表

- **数组**：固定大小，灵活性较低，通过索引直接访问。
- **列表**：动态大小，功能更多，通过索引访问较慢。

## 结合列表的 LINQ

### 结合列表的 LINQ
LINQ（语言集成查询）为集合提供了强大的查询能力。

### 结合列表的 LINQ
```csharp
var result = names.Where(n => n.Length > 4).ToList();
```

数组和列表对于管理 C# 中的数据至关重要。数组提供了固定大小的低级结构，而列表提供了动态大小调整和额外功能。何时使用每种结构取决于你的具体需求。在你处理这些结构时，你会发现它们在 C# 编程的各种场景中不可不可缺的。

# 11. C# 字典和 HashSet

字典和 HashSet 是 C# 中重要的数据结构，允许高效地存储和检索数据。它们提供了不同的功能并适用于不同的用场景。

## 字典

C# 中的字典是存储键值对的集合，允许根据关联的键快速访问值。

### 声明与初始化

### 声明与初始化
```csharp
Dictionary<string, int> ages = new Dictionary<string, int>()
{
    {"Alice", 25},
    {"Bob", 30},
    {"Charlie", 22}
};
```

### 添加和访问元素

### 添加和访问元素
```csharp
ages["David"] = 28; // 添加一个新的键值对
int bobAge = ages["Bob"]; // 使用键访问值
```

### 遍历字典

### 遍历字典
```csharp
foreach (var pair in ages)
{
    Console.WriteLine($"{pair.Key}: {pair.Value}");
}
```

### 检查键是否存在

### 检查键是否存在
```csharp
bool hasAlice = ages.ContainsKey("Alice"); // true
bool hasEve = ages.ContainsKey("Eve"); // false
```

## HashSet

C# 中的 HashSet 是存储唯一元素且无任何特定顺序的集合。它们基于哈希码，提供了快速的成员身份测试。

### 声明与初始化

### 声明与初始化
```csharp
HashSet<int> uniqueNumbers = new HashSet<int>() { 1, 2, 3, 4, 5 };
```

### 添加和删除元素

### 添加和删除元素
```csharp
uniqueNumbers.Add(6); // 添加一个新元素
uniqueNumbers.Remove(3); // 删除一个元素
```

### 检查元素是否存在

### 检查元素是否存在
```csharp
bool hasThree = uniqueNumbers.Contains(3); // false
bool hasFive = uniqueNumbers.Contains(5); // true
```

### 集操作

### 集操作
```csharp
HashSet<int> otherNumbers = new HashSet<int>() { 4, 5, 6, 7, 8 };

// 并集
HashSet<int> unionSet = new HashSet<int>(uniqueNumbers);
unionSet.UnionWith(otherNumbers); // {1, 2, 3, 4, 5, 6, 7, 8}

// 交集
HashSet<int> intersectionSet = new HashSet<int>(uniqueNumbers);
intersectionSet.IntersectWith(otherNumbers); // {4, 5}

// 差集
HashSet<int> differenceSet = new HashSet<int>(uniqueNumbers);
differenceSet.ExceptWith(otherNumbers); // {1, 2, 3}
```

字典和 HashSet 为 C# 提供了高效管理和查询数据的方法。字典适用于根据键快速访问的键值对，而 HashSet 则是维护唯一元素和执行集操作的理想选择。选择正确的数据结构取决于你应用程序的具体需求。在你处理这些结构时，你将增强在 C# 中有效存储和操作数据的能力。

# 12. 泛型

C# 中的泛型为创建类、接口和方法提供了一种强大的机制，使其能够在保持类型安全的同时与任何数据类型协同工作。它们允许你编写灵活且可重用的代码。

### 泛型简介
泛型提供了一种机制，用于创建与任何数据类型协同工作的同时保持类型安全的类、接口和方法。它们允许你编写灵活且可重用的代码。

### 泛型类
### 泛型类
```csharp
public class Box<T>
{
    private T _value;
    public Box(T value)
    {
        _value = value;
    }

    public T GetValue()
    {
        return _value;
    }
}
```

### 使用泛型
约束可以应用于泛型，以限制可以使用的类型。

### 泛型方法
```csharp
public T Maximum<T>(T a, T b) where T : IComparable<T>
{
    return a.CompareTo(b) > 0 ? a : b;
}
```

### 协变与逆变
泛型支持协变和逆变，能够建立类型之间的灵活关系。

### 协变
```csharp
public interface ICariant<out T>
{
    T GetItem();
}
```

### 泛型可空值类型
泛型可空值类型
```csharp
public class Nullable<T> where T : struct
{
    private T _value;
    public Nullable(T value)
    {
        _value = value;
    }

    public T GetValue()
    {
        return _value;
    }
}
```

C# 中的泛型通过提供创建灵活且类型安全的机制提高了代码的可用性和维护性。无论是处理泛型类、方法还是接口，理解泛型对于构建高效适应的软件至关重要。

# 13. 委托和事件

委托和事件是 C# 中的基本概念，促进了事件驱动编程的实现。它们提供了一种解耦且扩展的方式来处理和响应事件。

## 委托

C# 中的委托是一种方法签的类型，允许将方法作为对象对待。委托通常用于实现回调和事件处理。

### 委托声明

### 委托声明
```csharp
delegate void MyDelegate(string message);
```

### 使用委托

### 使用委托
```csharp
public class MessageProcessor
{
    public void ProcessMessage(string message)
    {
        Console.WriteLine($"Processing message: {message}");
    }
}
```
MessageProcessor processor = new MessageProcessor();
MyDelegate delegateInstance = processor.ProcessMessage;
delegateInstance("Hello, Delegate!"); // 运行委托

### 多播委托

### 多播委托
```csharp
public class Calculator
{
    public void Add(int a, int b)
    {
        Console.WriteLine($"Sum: {a + b}");
    }
    public void Multiply(int a, int b)
    {
        Console.WriteLine($"Product: {a * b}");
    }
}
```
Calculator calculator = new Calculator();
MyDelegate addDelegate = calculator.Add;
MyDelegate multiplyDelegate = calculator.Multiply;
MyDelegate multicastDelegate = addDelegate + multiplyDelegate;

multicastDelegate(3, 4); // 调用两个方法

## 事件





事件（Events）了一种类在发生感兴趣事件时通知其他类或对象机制。它们基于委托，并遵循发布-订阅模式。

### 事件声明

```csharp
// Event declaration

public class EventPublisher
{
    public event MyDelegate MyEvent;
}
```

### 订阅事件

```csharp
// Subscribing to events
public class EventSubscriber
{
    public void Subscribe(EventPublisher publisher)
    {
        publisher.MyEvent += HandleEvent;
    }
    public void HandleEvent(string message)
    {
        Console.WriteLine($"Event handled: {message}");
    }
}
```

### 发布事件

```csharp
// Publishing events
EventPublisher publisher = new EventPublisher();
EventSubscriber subscriber = new EventSubscriber();
subscriber.Subscribe(publisher);
publisher.MyEvent?.Invoke("Event message"); // Raising the event
```

### 事件处理器和 EventArgs

```csharp
// Event handlers and EventArgs
public class CustomEventArgs : EventArgs
{
    public string EventMessage { get; }
    public CustomEventArgs(string message)
    {
        EventMessage = message;
    }
}

public class EventPublisher
{
    public event EventHandler<CustomEventArgs> MyEvent;
    public void RaiseEvent(string message)
    {
        OnMyEvent(new CustomEventArgs(message));
    }
    protected virtual void OnMyEvent(CustomEventArgs e)
    {
        MyEvent?.Invoke(this, e);
    }
}
```

委托和事件在实现 C# 事件驱动编程中起着至关重要的作用。委托允许你创建灵活且可扩展的回调机制，而事件提供了一种处理和响应通知的标准方式。理解并使用委托和事件是构建响应式模块化 C# 应用程序的关键技能。

# 14. Lambda 和 LINQ

Lambdas 和 LINQ（语言集成查询）是 C# 中强大的特性，它们增强了代码的简洁性并方便了数据的查询和操作。

### Lambdas

Lambdas 是简洁的匿名函数，允许你为短生命周期的操作编写内联代码，对于委托类型特别有用。

#### Lambda 表达式语法

```csharp
// Lambda expression syntax
Func<int, int, int> add = (a, b) => a + b;
Console.WriteLine(add(3, 5)); // Output: 8
```

#### Lambda 语句

```csharp
// Lambda with statements
Func<int, int> square = x =>
{
    int result = x * x;
    return result;
};
Console.WriteLine(square(4)); // Output: 16
```

#### 在 LINQ 中使用 Lambda

```csharp
// Using Lambdas with LINQ
List<int> numbers = new List<int> { 1, 2, 3, 4, 5 };
var squaredNumbers = numbers.Select(x => x * x);
```

### LINQ (语言集成查询)

LINQ 提供了一种声明性语法，用于从各种来源（如集合、数据库、XML 等）查询和操作数据。

#### LINQ 查询语法

```csharp
// LINQ query syntax
var evenNumbers = from number in numbers
                  where number % 2 == 0
                  select number;
```

#### LINQ 方法语法

```csharp
// LINQ method syntax
var oddNumbers = numbers.Where(x => x % 2 != 0);
```

#### LINQ 中的投影

```csharp
// Projection in LINQ
var squaredAndFiltered = numbers
    .Select(x => x * x)
    .Where(x => x > 10);
```

#### LINQ 中的连接

```csharp
// Joining in LINQ
var persons = new List<Person> { /* ... */ };
var orders = new List<Order> { /* ... */ };
var query = from person in persons
              join order in orders on person.Id equals order.PersonId
              select new { person.Name, order.ProductName };
```

#### 结合 Lambda 表达式的 LINQ

```csharp
// LINQ with lambda expressions
var products = new List<Product> { /* ... */ };
var expensiveProducts = products.Where(p => p.Price > 1000);
```

Lambda 和 LINQ 为 C# 带来了表现力且简洁的语法，使代码更具可读性和维护性。Lambda 允许创建内联函数，而 LINQ 则简化了查询和转换。

# 15. 类型系统

委托和事件在实现 C# 事件驱动编程中起着至关重要的作用。委托允许你创建灵活且可扩展的回调机制，而事件提供了一种处理和响应通知的标准方式。理解并使用委托和事件是构建响应式模块化 C# 应用程序的关键技能。

### 值类型与 引用类型

值类型：值类型直接包含数据并存储在栈上。
引用类型：引用类型存储数据的引用，位于堆上。

### 隐式和显式类型转换

隐式转换：隐式转换自动将一种类型转换为另一种。
显式转换需要手动强制转换。

### 可空值类型

可空类型表示值的缺失。

### 类型推断 (var 和 dynamic)

`var` 关键字：编译器推断变量的类型。
`dynamic` 关键字：将类型确定推到运行时。

## 类型系统中的泛型

泛型引入了一种创建灵活可重用代码的方法。

### 装箱与拆箱

装箱涉及将值类型转换为引用类型，拆箱是反向操作。

### 类型别名 (using 指令)

类型别名允许为类型创建更短的名称，提高代码的可读性。

理解 C# 类型系统对于编写高效且无错误的代码至关重要。无论是处理值类型、引用类型、泛型还是类型转换，牢固掌握这些概念都能让开发者设计出稳健灵活的应用程序。

# 16. 字符串与正则表达式

处理字符串和正则表达式是 C# 编程中常见且重要的方面。字符串操作和模式匹配是各种应用程序中频繁使用的任务。

## 处理字符串

#### 字符串声明与初始化

```csharp
// String declaration and initialization
string greeting = "Hello, C#!";
```

### 字符串拼接

```csharp
// String concatenation
string firstName = "John";
string lastName = "Doe";
string fullName = firstName + " " + lastName;
```

### 字符串插值

```csharp
// String interpolation
string interpolatedGreeting = $"Welcome, {firstName}!";
```

### 常用字符串方法

```csharp
// Common string methods
string text = "  C# Programming  ";
string trimmedText = text.Trim();
string upperCaseText = text.ToUpper();
string lowerCaseText = text.ToLower();
```

#### 字符串比较

```csharp
// String comparison
string apple = "apple";
string orange = "orange";
bool areEqual = String.Equals(apple, orange, StringComparison.OrdinalIgnoreCase);
```

## 正则表达式

#### 正则表达式基础

```csharp
// Regular expression basics
using System.Text.RegularExpressions;
string input = "C# is powerful!";
string pattern = @"\bC#\b";
bool isMatch = Regex.IsMatch(input, pattern);
```

#### 正则表达式匹配

```csharp
// Regular expression matching
string input = "123-456-7890";
string pattern = @"\d{3}-\d{3}-\d{4}";
bool isPhoneNumber = Regex.IsMatch(input, pattern);
```





```c
// 正则表达式替换
string input = "C# is awesome!";
string pattern = @"C#";
string replacement = "CSharp";
string result = Regex.Replace(input, pattern, replacement);
```

### 正则表达式组

```c
// 正则表达式组
string input = "Name: John, Age: 30";
string pattern = @"Name: (?<Name>\w+), Age: (?<Age>\d+)";
Match match = Regex.Match(input, pattern);
string name = match.Groups["Name"].Value;
string age = match.Groups["Age"].Value;
```

处理字符串和正则表达式是 C# 开发中不可或缺的一部分。无论是操作字符串、执行模式匹配，还是利用正则表达式进行复杂的文本处理，掌握这些概念都能增强你在 C# 中有效处理和操作文本数据的能力。

# 17. 文件 I/O 与序列化

文件 I/O（输入/输出）和序列化是 C# 编程中的重要方面，涉及对文件的读取和写入，以及将对象转换为适用于存储或传输的格式。

## 文件 I/O

### 从文件中读取文本
```c
// 从文件中读取文本
string filePath = "example.txt";
string content = File.ReadAllText(filePath);
```

### 向文件写入文本
```c
// 向文件写入文本
string filePath = "example.txt";
string content = "Hello, File I/O!";
File.WriteAllText(filePath, content);
```

### 从文件中读取行
```c
// 从文件中读取行
string filePath = "example.txt";
string[] lines = File.ReadAllLines(filePath);
```

### 向文件写入行
```c
// 向文件写入行
string filePath = "example.txt";
string[] lines = { "Line 1", "Line 2", "Line 3" };
File.WriteAllLines(filePath, lines);
```

### 检查文件是否存在
```c
// 检查文件是否存在
string filePath = "example.txt";
bool fileExists = File.Exists(filePath);
```

### 删除文件
```c
// 删除文件
string filePath = "example.txt";
File.Delete(filePath);
```

## 序列化

序列化是将对象或数据结构转换为易于存储或传输的格式的过程。

### 二进制序列化
```c
// 二进制序列化
using System.Runtime.Serialization.Formatters.Binary;
[Serializable]
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
}
Person person = new Person { Name = "John", Age = 30 };
BinaryFormatter binaryFormatter = new BinaryFormatter();
using (FileStream stream = new FileStream("person.bin", FileMode.Create))
{
    binaryFormatter.Serialize(stream, person);
}
```

### 二进制反序列化
```c
// 二进制反序列化
using System.Runtime.Serialization.Formatters.Binary;
BinaryFormatter binaryFormatter = new BinaryFormatter();
using (FileStream stream = new FileStream("person.bin", FileMode.Open))
{
    Person deserializedPerson = (Person)binaryFormatter.Deserialize(stream);
    Console.WriteLine($"Name: {deserializedPerson.Name}, Age: {deserializedPerson.Age}");
}
```

### JSON 序列化
```c
// JSON 序列化
using System.Text.Json;
Person person = new Person { Name = "Alice", Age = 25 };
string jsonString = JsonSerializer.Serialize(person);
File.WriteAllText("person.json", jsonString);
```

文件 I/O 和序列化对于与外部存储交互以及应用程序之间的数据交换至关重要。无论是读取或写入文件，还是对对象的序列化和反序列化，这些技术能够在 C# 应用程序中实现有效的数据处理。

# 18. C# 多线程与并行编程

C# 中的多线程和并行编程允许你同时执行多个线程，从而提高应用程序的和响应速度。这些概念对于高效利用多核现代硬件至关重要。

## 多线程基础

### 创建线程
```c
// 创建线程
using System.Threading;
void MyThreadFunction()
{
    // 线程逻辑
}
Thread myThread = new Thread(MyThreadFunction);
myThread.Start();
```

### 线程同步
```c
// 线程同步
lock (lockObject)
{
    // 受 lock 保护的代码
}
```

### 线程睡眠
```csharp
// 线程睡眠
Thread.Sleep(1000); // 睡眠 1 秒
```

## 使用 async 和 await 进行异步编程

## 异步方法
```csharp
// 异步方法
async Task MyAsyncMethod()
{
    // 异步逻辑
}
```

### await 运算符
```csharp
// await 运算符
await MyAsyncMethod();
```

### 任务并行库 (TPL)
```csharp
// 任务并行库
using System.Threading.Tasks;
List<Task> tasks = new List<Task>();
tasks.Add(Task.Run(() => MyMethod1()));
tasks.Add(Task.Run(() => MyMethod2()));
await Task.WhenAll(tasks);
```

## 并行编程

### 并行 For 循环
```csharp
// 并行 For 循环
Parallel.For(0, 10, i =>
{
    // 并行的循环体
});
```

### 并行 ForEach 循环
```csharp
// 并行 ForEach 循环
List<int> numbers = new List<int> { /* ... */ };
Parallel.ForEach(numbers, number =>
{
    // 并行的循环体
});
```

### PLINQ (并行 LINQ)
```csharp
// PLINQ
List<int> numbers = new List<int> { /* ... */ };
numbers.AsParallel().Where(n => n > 0);
```

# 19. 使用 async 和 await 进行异步编程

C# 中的 async 和 await 异步编程允许你编写响应式且高效的代码，特别适用于涉及 I/O 的任务。

## 异步方法
```csharp
// 异步方法
async Task MyAsyncMethod()
{
    // 异步逻辑
}
```

### await 运算符
```csharp
// await 运算符
await MyAsyncMethod();
```

### await 与任务延续
```csharp
// 使用 await 和任务延续
async Task<int> MyAsyncMethod()
{
    int result = await SomeOperation();
    // 继续逻辑
    return result;
}
```

### 异步方法中的错误处理
```csharp
// 异步方法中的 try/catch
async Task<int> MyAsyncMethod()
{
    try
    {
        int result = await SomeOperation();
        return result;
    }
    catch (Exception ex)
    {
        // 处理异常
        return -1;
    }
}
```

### 异步流（C# 8 及更高版本）
```csharp
// 异步流
async IAsyncEnumerable<int> GenerateNumbersAsync()
{
    for (int i = 0; i < 10; i++)
    {
        await Task.Delay(100); // 模拟异步操作
        yield return i;
    }
}
```

### Task.WhenAll 和 Task.WhenAny
```csharp
// Task.WhenAll
async Task MyAsyncMethod()
{
    Task<int> task1 = SomeAsyncOperation1();
    Task<string> task2 = SomeAsyncOperation2();
    await Task.WhenAll(task1, task2);
    int result1 = task1.Result;
    string result2 = task2.Result;
}

// Task.WhenAny
async Task MyAsyncMethod()
{
    Task<int> task1 = SomeAsyncOperation1();
    Task<int> task2 = SomeAsyncOperation2();
    Task<int> completedTask = await Task.WhenAny(task1, task2);
    int result = completedTask.Result;
}
```





.NET Core 是一个免费、开源、跨平台的框架，用于构建现代、云端和连接的应用程序。它是各种应用程序类型的基础，包括 Web、桌面、移动、云、游戏、物联网（IoT）和人工智能（AI）应用。

## 主要特性

- **跨平台**：`.NET Core` 设计用于运行在多个平台上，包括 Windows、macOS 和 Linux，允许开发者构建可以在不同操作系统上无缝运行的应用程序。
- **开源**：该框架是开源的，鼓励社区贡献并提供开发过程的度。开发者可以访问源代码、对其改进做出贡献，并探索其内部机制。
- **命令行界面 (CLI)**：`.NET Core` 包含一个强大的命令行界面 (`CLI`)，允许开发者直接从命令行构建、运行、测试和发布应用程序，提供灵活且高效的开发体验。
- **微服务架构**：`.NET Core` 非常适合基于微服务的架构，使开发者能够构建和部署可扩展的模块化应用程序，这些应用程序由小型、独立部署的服务组成。

## 创建 .NET Core 应用程序

### 安装 .NET Core SDK
从官方网站下载并安装 `.NET Core SDK`：`https://dotnet.microsoft.com/download`

### 创建控制台应用程序
#### 创建一个新的控制台应用程序
```bash
dotnet new console -n MyConsoleApp
```

#### 运行应用程序
#### 到应用程序目录
```bash
cd MyConsoleApp
```
#### 运行应用程序
```bash
dotnet run
```

## .NET Core 与 .NET Framework
`.NET Core` 与传统的 `.NET Framework` 在多个方面有所不同。`.NET Framework` 主要为 Windows 应用程序设计，而 `.NET Core` 是跨平台的。`.NET Core` 还是模块化的，允许开发者仅包含他们需要的组件，从而减小部署应用程序体积。

## .NET 5 及更高版本
`.NET 5` 是 `.NET Core` 之后的下一个框架版本，它统一了之前分开的 `.NET Core` 和 `.NET Framework`。它继续改进跨平台支持、性能和开发者生产力。

`.NET Core` 是一个多功能且现代的框架，赋予开发者创建高性能、可扩展和跨平台的应用程序。其开源特性、跨平台能力以及对微服务架构的支持使其成为广泛开发场景的流行选择。

# 21. 内存管理与垃圾回收

内存管理是编程的一个关键方面，确保内存资源的高效分配和释放。在 `C#` 中，`.NET` 运行时通过名为 `Garbage Collection`（垃圾回收）的过程提供内存管理。

## C# 中的自动内存管理

- **栈与堆**：在 `C#` 中，内存分为两个主要区域：栈 (`stack`) 和堆 (`heap`)。`stack` 用于存储值类型和方法调用信息，而 `heap` 用于动态分配的内存，主要用于引用类型。
- **值类型与引用类型**：值类型（例如 `int`、`float`）存储在栈上，而引用类型（例如 `classes`、`arrays`）分配在堆上。引用类型存储的是指向堆上实际数据的引用。

## 垃圾回收
`Garbage Collection` (`GC`) 是一个运行时自动收回不再使用的对象所占内存的过程，防止内存泄漏并促进高效的内存利用。

- **基于代的垃圾回收**：`.NET` 中的 `GC` 是分代的，它将对象分为三代（年轻代、中期和老年代）。新创建的对象从年轻代开始，如果它们存过了多次回收，则会被提升到较老的代。
- **垃圾回收算法**：`.NET` `GC` 使用不同的算法，包括：
    - **标记-清除 (Mark-and-Sweep)**：识别并标记仍然可达的对象。
    - **压缩 (Compact)**：通过将存活对象移动来压缩内存，减少碎片。

## IDisposable 接口与 using 语句

**管理非托管资源**：`IDisposable` 接口用于释放非托管资源，如文件句柄、数据库连接或网络接字。

```csharp
public class MyResource : IDisposable
{
    private bool disposed = false;

    protected virtual void Dispose(bool disposing)
    {
        if (disposing)
        {
            // Release managed resources
        }
        // Release unmanaged resources
        disposed = true;
    }

    public void Dispose()
    {
        Dispose(true);
    }
}
```

**using 语句**：确保即使发生异常也会调用 `Dispose`。

```csharp
using (MyResource resource = new MyResource())
{
    // 使用资源
}
```

## 内存分析与优化
内存分析工具：如 Visual Studio Profiler 等第三方分析工具有助于分析内存使用。

### 内存管理最佳实践
- 减少全局变量的使用。
- 避免创建不必要的对象。
- 使用 `using` 语句释放资源。
- 注意大型对象图和循环引用。

有效的内存管理对于创建高性能应用程序至关重要。`C#` 的垃圾回收结合通过 `IDisposable` 和 `using` 语句进行资源管理，有助于构建健壮的软件。

# 22. 处理日期和时间

处理日期和时间是软件开发中的常见需求，`C#` 的相关类提供了丰富的功能来处理这些场景。

## DateTime 结构

### 创建 DateTime 对象
```csharp
DateTime currentDateTime = DateTime.Now;
DateTime specificDateTime = new DateTime(2024, 2, 3, 12, 30, 0);
```

### 格式化与解析
```csharp
string formattedDate = currentDateTime.ToString("yyyy-MM-dd HH:mm:ss");
DateTime parsedDate = DateTime.Parse("2024-02-03 12:30:00");
```

### 时间的加减
```csharp
DateTime futureDate = currentDateTime.AddHours(24);
DateTime pastDate = currentDateTime.AddMonths(-1);
```

## TimeSpan 结构

### 创建 TimeSpan 对象
```csharp
TimeSpan duration = new TimeSpan(1, 30, 0); // 1 小时 30 分钟
```

### 与 TimeSpan 的运算
```csharp
DateTime futureTime = currentDateTime + duration;
DateTime pastTime = currentDateTime - duration;
```

## DateTimeOffset 结构

### 处理时区
```csharp
DateTimeOffset utcDateTime = DateTimeOffset.UtcNow;
DateTimeOffset specificDateTimeZone = new DateTimeOffset(2024, 2, 3, 12, 30, 0, TimeSpan.FromHours(5));
```




处理日期和时间是软件开发中不可或的一部分。无论是操作 `DateTime`、`TimeSpan`，还是使用 `DateTimeOffset` 和 `TimeZoneInfo` 处理时区，C# 都提供了一套全面的特性来满足各种需求。理解这些特性允许开发者创建能够有效管理、显示和操作日期时间信息的应用程序。

# 23. 反射与特性

C# 中的反射（Reflection）和特性（Attributes）提供了在运行时检查和操作代码的强大机制。反射允许你动态检查并交互类型、成员和对象，而特性允许你向代码中附加元数据。

## 反射

### 获取类型信息
```csharp
// 获取类型信息
Type type = typeof(MyClass);
Type anotherType = obj.GetType();
```

### 获取类型的成员
```csharp
// 获取类型的成员
MethodInfo[] methods = type.GetMethods();
FieldInfo[] fields = type.GetFields();
PropertyInfo[] properties = type.GetProperties();
```

### 动态创建实例
```csharp
// 动态创建实例
object instance = Activator.CreateInstance(type);
```

### 动态调用方法
```csharp
// 动态调用方法
MethodInfo method = type.GetMethod("MyMethod");
method.Invoke(instance, parameters);
```

### 访问并修改字段和属性
```csharp
// 访问并修改字段和属性
FieldInfo field = type.GetField("myField");
field.SetValue(instance, value);

PropertyInfo property = type.GetProperty("MyProperty");
property.SetValue(instance, value);
```

### 检查特性
```csharp
// 检查特性
object[] attributes = type.GetCustomAttributes(typeof(MyAttribute), true);
```

## 特性

### 创建自定义特性
```csharp
// 创建自定义特性
[AttributeUsage(AttributeTargets.Class | AttributeTargets.Method, AllowMultiple = true)]
public class MyAttribute : Attribute
{
    public string Description { get; }
    public MyAttribute(string description)
    {
        Description = description;
    }
}
```

### 应用特性
```csharp
// 应用特性
[My("This is my class")]
public class MyClass
{
    [My("This is my method")]
    public void MyMethod() { /* Method logic */ }

    [My("This is my property")]
    public string MyProperty { get; set; }
}
```

### 获取特性信息
```csharp
// 获取特性信息
MyAttribute classAttribute = (MyAttribute)Attribute.GetCustomAttribute(type, typeof(MyAttribute));
MyAttribute methodAttribute = (MyAttribute)Attribute.GetCustomAttribute(method, typeof(MyAttribute));
```

反射和特性提供了一种运行时处理代码的动态且可扩展的方式。反射允许动态检查和操作类型、成员和对象，而特性允许你向代码中附加元数据以提供额外信息或行为。适当使用反射和特性可以在各种场景下产生更灵活、可复用的代码。然而，应该注意以确保性能和可维护性。

# 24. C# 网络与 Web 开发

C# 为网络和 Web 开发提供了强大的能力，能够创建与互联网交互、与远程服务器通信以及构建动态 Web 解决方案的应用程序。

## 网络基础

**System.Net 命名空间**：C# 网络功能主要由 `System.Net` 命名空间提供，提供了用于处理 `HTTP`、`FTP`、`TCP` 和 `UDP` 等协议的类。

```csharp
using System.Net;
using System.Net.Sockets;
```

### 使用 IP 地址
```csharp
// 使用 IP 地址
IPAddress ipAddress = IPAddress.Parse("192.168.1.1");
IPAddress localAddress = IPAddress.Loopback;
```

### TCP 客户端与服务器
```csharp
// TCP 客户端和服务器
TcpListener tcpListener = new TcpListener(IPAddress.Any, 12345);
tcpListener.Start();
TcpClient tcpClient = new TcpClient("localhost", 12345);
```

## 使用 ASP.NET 进行 Web 开发

- **ASP.NET 简介**：ASP.NET 是一个 Web 开发框架，允许开发者构建动态的数据驱动 Web 应用程序。
- **ASP.NET MVC**：ASP.NET MVC（模型-视图-控制器）是一个遵循 MVC 架构模式构建 Web 应用程序的框架。
- **ASP.NET Core**：ASP.NET Core 是 ASP.NET 框架的下一代跨平台版本，专为现代 Web 开发设计。

## 消费与创建 Web API

## 消费 Web API
```csharp
// 消费 Web API
using (HttpClient httpClient = new HttpClient())
{
    HttpResponseMessage response = await httpClient.GetAsync("https://api.example.com/data");
    if (response.IsSuccessStatusCode)
    {
        string content = await response.Content.ReadAsStringAsync();
        // 处理内容
    }
}
```

### 使用 ASP.NET Core 创建 Web API
```csharp
// 使用 ASP.NET Core 创建简单的 Web API
[ApiController]
[Route("api/[controller]")]
public class MyController : ControllerBase
{
    [HttpGet]
    public IActionResult Get()
    {
        return Ok("Hello, API!");
    }
}
```

## C# 库

- **SignalR**：`SignalR` 是一个为 Web 应用程序添加实时功能的库。
- **gRPC**：`gRPC` 是一个用于远程过程调用 (RPC)的高性能框架。

## 最佳实践

- **安全套接层 (SSL/TLS)**：使用 `SSL/TLS` 确保网络安全通信。
- **数据加密**：在传输过程中加密敏感数据。
- **输入验证**：验证输入以防止 SQL 注入等漏洞。

# 25. 消费与创建 Web API

Web API（应用程序接口）在现代软件开发中起着至关重要的作用，允许应用程序交互并共享数据。

## 消费 Web API

### 使用 HttpClient 进行请求
```csharp
// 使用 HttpClient 进行请求
using (HttpClient httpClient = new HttpClient())
{
    HttpResponseMessage response = await httpClient.GetAsync("https://api.example.com/data");
    if (response.IsSuccessStatusCode)
    {
        string content = await response.Content.ReadAsStringAsync();
    }
}
```

#### 反序列化 JSON 响应
```csharp
// 反序列化 JSON 响应
using (HttpClient httpClient = new HttpClient())
{
    HttpResponseMessage response = await httpClient.GetAsync("https://api.example.com/data");
    if (response.IsSuccessStatusCode)
    {
        string jsonContent = await response.Content.ReadAsStringAsync();
        MyObject myObject = JsonConvert.DeserializeObject<MyObject>(jsonContent);
    }
}
```

## 使用 ASP.NET Core 创建 Web API

#### 设置 ASP.NET Core Web API
```csharp
// 设置 ASP.NET Core Web API
[ApiController]
[Route("api/[controller]")]
public class MyController : ControllerBase
{
    [HttpGet]
    public IActionResult Get()
    {
        return Ok("Hello, API!");
    }
}
```

#### 处理 HTTP 请求和响应
```csharp
// 在 Web API 中处理 HTTP 请求和响应
[ApiController]
[Route("api/[controller]")]
public class MyController : ControllerBase
{
    [HttpGet]
    public IActionResult Get()
    {
        return Ok("Hello, API!");
    }

    [HttpPost]
    public IActionResult Post([FromBody] MyObject myObject)
    {
        // 处理迁入的数据
        return CreatedAtAction(nameof(Get), new { id = myObject.Id }, myObject);
    }
}
```

## 为 API 文档添加 Swagger





```csharp
// 为 API 文添加 Swagger

services.AddSwaggerGen(c =>
{
    c.SwaggerDoc("v1", new OpenApiInfo { Title = "My API", Version = "v1" });
});
```

# C# Web API 库

用于实时通信的 SignalR：`SignalR`允许 Web 应用中客户端与服务器之间的实时通信。

类型安全的 API 消费：`Refit` 通过提供一种类型安全的定义和调用 RESTful API 的方式，简化了消费 Web API 的过程。

## 安全考虑

认证与授权：实现安全的身份验证和授权机制，例如 `OAuth` 或 `API keys`，以控制对 API 的访问。

HTTPS 的使用：始终使用 `HTTPS` 在传输过程中加密数据，并增强 Web API 的整体安全性。

消费和创建 Web API 是 C# 开发人员的必备技能。无论是使用 `HttpClient` 进行 HTTP 请求、反序列化 `JSON` 响应、构建 `ASP.NET Core Web APIs`，还是利用 `SignalR` 和 `Refit` 等库，C# 均提供了一套全面的工具用于有效的 API 交互。安全考虑（如身份验证、授权和 `HTTPS` 的使用）对于确保 API 通信中数据的完整性和机密性关重要。

# 26. Entity Framework 简介

Entity Framework (`EF`) 是 .NET 生态系统中一种强大且广泛的对象关系映射 (`ORM`) 框架。它通过允许开发者使用 `.NET` 对象与数据库交互，从而消除了对复杂 `SQL` 查询的需求。

## 核心概念

DbContext：`DbContext` 是 Entity Framework 中的核心类，代表与数据库的会话并允许开发者查询和交互数据。

```csharp
public class MyDbContext : DbContext
{
    public DbSet<MyEntity> MyEntities { get; set; }
}
```

DbSet：`DbSet` 是 `DbContext` 的一个属性，代表数据库中的实体集合。

```csharp
public class MyDbContext : DbContext
{
    public DbSet<Product> Products { get; set; }
}
```

代码优先和数据库优先方法：Entity Framework 支持 `Code-First`（代码优先，即根据你的 C# `classes` 生成数据库架构）和 `Database-First`（数据库优先，即根据现有的数据库架构生成 C# `classes`）。

迁移（Migrations）：Entity Framework 中的 `Migrations` 允许开发者通过应用增量更改来随时间演进数据库架构。

## 创建新的迁移

```bash
dotnet ef migrations add InitialCreate
```

# 将待处理的迁移应用到数据库

```bash
dotnet ef database update
```

## 代码优先示例

### 定义实体类

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
}
```

### 创建 DbContext

```csharp
public class MyDbContext : DbContext
{
    public DbSet<Product> Products { get; set; }
}
```

### 配置连接字符串

```csharp
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        services.AddDbContext<MyDbContext>(options =>
            options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));
    }
}
```

### 查询数据

LINQ 查询：Entity Framework 支持使用 `LINQ`（集成语言查询）以强类型方式查询数据。

```csharp
var expensiveProducts = dbContext.Products.Where(p => p.Price > 100);
```

### 更新数据

#### 添加和更新实体

```csharp
// 添加新实体
var newProduct = new Product { Name = "New Product", Price = 50 };
dbContext.Products.Add(newProduct);

// 更新现有实体
var existingProduct = dbContext.Products.Find(1);
existingProduct.Price = 75;
```

#### 删除实体

```csharp
var productToDelete = dbContext.Products.Find(2);
dbContext.Products.Remove(productToDelete);
```

Entity Framework 简化了 C# 中的数据库交互，让开发者能够关注应用程序逻辑，而不是处理原始的 `SQL` 查询。通过对 `Code-First`、`Database-First`、迁移和 `LINQ` 查询的支持，Entity Framework 为 .NET 生态系统处理数据库提供了一种灵活且高效的方式。

# 27. 依赖注入与控制反转

依赖注入 (`DI`) 和控制反转 (`IoC`) 是软件开发中的基础性概念，它们通过解耦组件和更有效地管理依赖关系来促进模块化、可测试性和维护性。在 C# 和 .NET 中，这些概念经常结合使用以实现松耦合和可扩展的架构。

## 控制反转 (IoC)

在 `IoC` 中，程序流的控制被反转了，这意味着管理对象创建和生命期的责任被委托给了外部容器。

依赖倒置原则 (`DIP`)：`DIP` 规定高级模块不应该依赖于低级模块，两者都应该依赖于抽象。此外，抽象不应该依赖于细节；细节应该依赖于抽象。

## 依赖注入 (DI)

依赖注入是一种模式以及 `IoC` 的特定实现，组件（类或函数）的依赖从外部注入，通常通过构造函数参数或属性设置器实现。

### 优势：

- **解耦**：组件变得独立，使其更容易替换或扩展功能。
- **可测试性**：由于能够用 mock 或 stub 替换依赖，更易进行单元测试。
- **可维护性**：对一个组件的更改影响是最小的。

### C# .NET 中的依赖注入

服务集合（Service Collection）：在 .NET 中，内置的 `IServiceCollection` 用于注册和解析依赖。

```csharp
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        services.AddDbContext<MyDbContext>(options =>
            options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));
    }
}
```

### 构造函数注入

```csharp
public class MyClass
{
    private readonly IMyService _myService;
    private readonly IOtherService _otherService;

    public MyClass(IMyService myService, IOtherService otherService)
    {
        _myService = myService;
        _otherService = otherService;
    }
    // 在类中使用 _myService 和 _otherService
}
```

## 控制反转容器

流行的 IoC 容器

- `Microsoft.Extensions.DependencyInjection`：内置于 .NET。
- `Autofac`：流行的第三方容器。
- `Unity`：来自微软模式实践。

## 注册与解析依赖

```csharp
// Microsoft.Extensions.DependencyInjection
IServiceCollection services = new ServiceCollection();
services.AddTransient<IMyService, MyService>();
services.AddScoped<IOtherService, OtherService>();
```

```csharp
// Autofac
ContainerBuilder builder = new ContainerBuilder();
builder.RegisterType<MyService>().As<IMyService>().InstancePerDependency();
builder.RegisterType<OtherService>().As<IOtherService>().InstancePerLifetimeScope();
```

```csharp
// Unity
IUnityContainer container = new UnityContainer();
container.RegisterType<IMyService, MyService>();
container.RegisterType<IOtherService, OtherService>();

# 28. 使用 NUnit 和 MSTest 进行单元测试

单元测试是软件开发中至关重要的实践，用于确保单个组件或代码单元的可靠性和正确性。NUnit 和 MSTest 是 C# 生态系统中两种流行的测试框架，为编写和执行测试提供了结构化且高效的方式。

## 单元测试简介





## 单元测试概述

单元测试的目的：单元测试涉及对代码各个单元或函数进行隔离测试，以验证它们是否按预期工作。它有助于早期发现 Bug，确保代码质量并便于重构。

测试驱动开发 (TDD)：TDD 是一种开发方法，在编写实际代码之前编写测试。该循环通常包括：编写一个失败的测试、实现代码以使测试通过，然后在必要时进行重构。

# NUnit

## 开始使用 NUnit

安装 NUnit NuGet 包：

```bash
dotnet add package NUnit
dotnet add package NUnit3TestAdapter
```

编写一个简单的测试：

```csharp
using NUnit.Framework;

[TestFixture]
public class MyTests
{
    [Test]
    public void MyTestMethod()
    {
        // Arrange
        int a = 2, b = 3;
        // Act
        int result = a + b;
        // Assert
        Assert.AreEqual(5, result);
    }
}
```

运行测试：

```bash
dotnet test
```

## 关键 NUnit 特性

- `[TestFixture]`: 标记一个类包含 NUnit 测试。
- `[Test]`: 标记一个方法为测试方法。
- `[SetUp]` 和 `[TearDown]`: 在每个测试方法之前和之后运行的方法。

# MSTest

## 开始使用 MSTest

MSTest 包含在 .NET Core SDK 中，因此不需要安装额外的包。

编写一个简单的测试：

```csharp
using Microsoft.VisualStudio.TestTools.UnitTesting;

[TestClass]
public class MyTests
{
    [TestMethod]
    public void MyTestMethod()
    {
        // Arrange
        int a = 2, b = 3;
        // Act
        int result = a + b;
        // Assert
        Assert.AreEqual(5, result);
    }
}
```

运行测试：

```bash
dotnet test
```

## 关键 MSTest 特性

- `[TestClass]`: 标记一个类包含 MSTest 测试。
- `[TestMethod]`: 标记一个方法为测试方法。
- `[TestInitialize]` 和 `[TestCleanup]`: 在每个测试方法之前和之后运行的方法。

# 在 NUnit 和 MSTest 之间选择

- `NUnit`: 因其简单性、灵性和对并行测试执行的支持而流行。适用于简单和复杂的测试场景。
- `MSTest`: 与 Visual Studio 集成，通常被使用 Visual Studio 的开发者选择。它随着时间的推移而改进，并提供了一个功能丰富的测试框架。

单元测试是软件开发中的一项基本实践，NUnit 和 MSTest 都提供了在 C# 中编写和执行测试的有效方法。无论你喜欢 NUnit 的简单性，还是 MSTest 提供的 Visual Studio 集成，关键是将稳健的测试策略整合到你的开发过程中，以确保代码的可靠性和维护性。

# 29. C# 程序的调试与性能分析

调试和性能分析（Profiling）是软件开发中的基本过程，用于识别并修复问题、优化性能并确保 C# 程序的整体健康。本指南涵盖了有效调试和分析 C# 程序的关键概念和技术。

## 调试 C# 程序

调试简介：调试是识别和修复代码中问题（Bug）的过程。调试器提供了检查变量、设置断点和单步执行代码的工具。

### 使用 Visual Studio 调试器

- 设置断点：点击行号旁侧的边缘区域。
- 单步执行代码：使用 `F10`（逐过程）、`F11`（进入）和 `Shift+F11`（调出）。
- 检查变量：悬停在变量上查看其值或使用 `Watch` 监视窗口。
- 条件断点：设置仅在特定条件下触发的断点：

```csharp
int i = 0;
while (i < 10)
{
    // Some code
    i++;
}
```
设置条件 `i == 5` 的断点，仅在 `i` 等于 5 时中断。

异常处理：
- 启用异常时中断：调试 -> 窗口 -> 异常设置。
- 使用 `try-catch` 块处理异常。

## 性能分析 C# 程序

性能分析简介：性能分析涉及分析应用程序的性能，以识别瓶颈、内存泄漏和优化区域。

### Visual Studio 性能分析工具

- CPU 性能分析：分析 CPU 使用情况以识别性能瓶颈。
- 内存分析：检测并分析内存泄漏和过度内存使用。

### 性能计数器

- 性能监器 (`PerfMon`)：监控系统级性能计数器。
- Windows 性能分析器 (`WPA`)：分析跟踪数据以获得详细见解。

## 有效调试与性能分析的技巧

- 使用版本控制：使用 `Git` 跟踪代码更改。
- 日志：实现日志记录记录行为信息。
- 单元测试：编写全面的测试以捕获问题。
- 代码审查：与团队成员定期审查代码。
- 静态代码分析：使用 `Roslyn Analyzers` 或 `ReSharper` 等工具。

调试和性能分析是软件开发中的关键方面，帮助开发者识别和解决问题。无论使用 Visual Studio 调试器还是性能分析工具，全面的方法都有益于此。

# 30. C# 中的性能

性能优化是软件开发的一个关键方面，确保应用程序运行高效并响应迅速。本指南涵盖了改进 C# 程序性能的关键考虑和技术。

## 通用性能提示

使用高效的数据结构：根据你的特定需求选择合适的数据结构。使用 `List<T>` 处理动态列表，使用 `Dictionary<K, V>` 处理键值对，并根据性能特性选择其他集合。

最小化循环中的字符串拼接：循环中的字符串拼接会导致性能问题。相反，使用 `StringBuilder` 进行高效字符串构建：

```csharp
StringBuilder sb = new StringBuilder();
for (int i = 0; i < 1000; i++)
{
    sb.Append(i);
}
string result = sb.ToString();
```

针对小缓冲区使用 `stackalloc`：对于小型缓冲区分配，考虑使用 `stackalloc` 关键字在栈上而不是堆上分配内存：

```csharp
void ExampleMethod()
{
    Span<int> numbers = stackalloc int[100];
    // 使用 numbers
}
```

## 内存管理

注意垃圾回收：频繁的垃圾回收会影响性能。减少不必要的对象分配，特别是在性能关键的代码区域。

使用对象池：重用对象而不是创建新对象。对象池通过回收对象进行用来减少垃圾回收的开销。

```csharp
ObjectPool<MyObject> objectPool = new ObjectPool<MyObject>(() => new MyObject(), 100);
// 从池中借用对象
MyObject obj = objectPool.Borrow();
// 使用对象
// 将对象返回池中
objectPool.Return(obj);
```

## 算法优化

优化算法：根据特定需求选择具有最优空间复杂度的算法。理解大 O 表示法算法的效率。

使用并行化：利用并行编程将工作分配到多个核心上，特别是对于计算密集型任务。

```csharp
Parallel.For(0, 1000000, i =>
{
    // 执行并行工作
});
```

## 性能分析与基准测试

识别性能瓶颈：使用 `Visual Studio Profiler` 或第三方工具识别应用程序中的性能瓶颈。

代码基准测试：使用 `BenchmarkDotNet` 等基准测试库测量并比较代码不同实现的性能。





C# 中的性能优化涉及通用编程实践、内存管理、算法效率和性能分析的结合。通过审慎地应用这些技术并考虑应用的特定需求，你可以显著提高 C# 代码的整体性能。定期测量和分析应用程序的性能，以识别优化区域并确保持续的效性。

# 31. 在 C# 中处理 XML 和 JSON

处理 XML 和 JSON 是现代软件开发中的常见需求。在 C# 中，你可以利用各种库和 API 来解析、操作和创建 XML 和 JSON 数据。本指南涵盖了在 C# 中处理 XML 和 JSON 的核心概念和技术。

## 在 C# 中处理 XML

### 读取 XML 数据

使用 `XmlDocument`：
```csharp
XmlDocument xmlDoc = new XmlDocument();
xmlDoc.Load("path/to/file.xml");
XmlNodeList nodes = xmlDoc.SelectNodes("/root/node");
foreach (XmlNode node in nodes)
{
    // 访问节点数据
    string value = node.InnerText;
}
```

使用 LINQ to XML (`XDocument`):
```csharp
XDocument xDoc = XDocument.Load("path/to/file.xml");
var elements = xDoc.Descendants("node");
foreach (var element in elements)
{
    // 访问元素数据
    string value = element.Value;
}
```

### 写入 XML 数据

使用 `XmlDocument`：
```csharp
XmlDocument xmlDoc = new XmlDocument();
XmlElement root = xmlDoc.CreateElement("root");
xmlDoc.AppendChild(root);
XmlElement node = xmlDoc.CreateElement("node");
node.InnerText = "Node value";
root.AppendChild(node);
xmlDoc.Save("output.xml");
```

使用 LINQ to XML (`XDocument`):
```csharp
XDocument xDoc = new XDocument(
    new XElement("root",
        new XElement("node", "Node value")
    )
);
xDoc.Save("output.xml");
```

## 在 C# 中处理 JSON

### 读取 JSON 数据

使用 `Newtonsoft.Json`：
```csharp
using Newtonsoft.Json;
using Newtonsoft.Json.Linq;
string json = File.ReadAllText("path/to/file.json");
JObject jsonObj = JObject.Parse(json);
JToken nodeValue = jsonObj.SelectToken("root.node");
string value = nodeValue.Value<string>();
```

使用 `System.Text.Json` (.NET Core):
```csharp
using System.Text.Json;
string json = File.ReadAllText("path/to/file.json");
JsonDocument jsonDoc = JsonDocument.Parse(json);
JsonElement root = jsonDoc.RootElement;
JsonElement nodeValue = root.GetProperty("node");
string value = nodeValue.GetString();
```

### 写入 JSON 数据

使用 `Newtonsoft.Json`：
```csharp
using Newtonsoft.Json;
var data = new { root = new { node = "Node value" } };
string json = JsonConvert.SerializeObject(data, Formatting.Indented);
File.WriteAllText("output.json", json);
```

使用 `System.Text.Json` (.NET Core):
```csharp
using System.Text.Json;
var data = new { root = new { node = "Node value" } };
string json = JsonSerializer.Serialize(data, new JsonSerializerOptions { WriteIndented = true });
File.WriteAllText("output.json", json);
```

## 常见注意事项

- **错误处理**：始终处理在 XML 和 JSON 处理过程中可能发生的异常和错误。
- **性能**：考虑性能影响，特别是对于大型 XML 或 JSON 数据集。
- **验证**：验证输入数据，以确保其符合预期的 XML 或 JSON 结构。

在 C# 中处理 XML 和 JSON 涉及根据项目需求选择合适的 API 和库。无论是使用 `XmlDocument` 和 LINQ to XML 处理 XML，还是使用 `Newtonsoft.Json` 和 `System.Text.Json` 处理 JSON，理解这些库的能力都能让你在 C# 应用中高效地处理数据交换。

# 32. C# 安全最佳实践

确保 C# 应用程序的安全对于防止各种威胁和漏洞至关重要。本指南概述了关键的安全最佳实践，帮助你构建稳健且安全的 C# 应用程序。

## 控制反转 (IoC)

在 `IoC` 中，程序的流控制被反转，这意味着管理对象创建和生命周期的责任被委托给了外部容器。

依赖倒置原则 (`DIP`)：`DIP` 是一个原则，规定高层模块不应该依赖于低层模块，两者都应该依赖于抽象。此外，抽象不应该依赖于细节；细节应该依赖于抽象。

## 依赖注入 (DI)

依赖注入是一种设计模式，也是 `IoC` 的具体实现，其中组件（类或函数）的依赖从外部注入，通常通过构造函数参数或属性设置器实现。

### 益处：

- **解耦**：组件变得相互独立，使其更容易替换或扩展功能。
- **可测试性**：通过能够 mock（模拟）或 stub（桩）替换依赖，更容易进行单元测试。
- **可维护性**：对一个组件的更改对其他组件的影响最小。

## .NET Core 中的 C# 依赖注入

服务集合：在 .NET Core 中，内置的 `IServiceCollection` 用于注册和解析依赖。

```csharp
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        // 注册依赖
        services.AddTransient<IMyService, MyService>();
        services.AddScoped<IOtherService, OtherService>();
    }
}
```

构造函数注入
```csharp
public class MyClass
{
    private readonly IMyService _myService;
    private readonly IOtherService _otherService;

    public MyClass(IMyService myService, IOtherService otherService)
    {
        _myService = myService;
        _otherService = otherService;
    }
}
```

### 控制反转容器

- `Microsoft.Extensions.DependencyInjection`：内置。
- `Autofac`：流行的第三方容器。
- `Unity`：来自微软模式与实践。

### 注册和解析依赖

```csharp
// Microsoft.Extensions.DependencyInjection
IServiceCollection services = new ServiceCollection();
services.AddTransient<IMyService, MyService>();
services.AddScoped<IOtherService, OtherService>();

// Autofac
ContainerBuilder builder = new ContainerBuilder();
builder.RegisterType<MyService>().As<IMyService>().InstancePerDependency();
builder.RegisterType<OtherService>().As<IOtherService>().InstancePerLifetime();

// Unity
IUnityContainer container = new UnityContainer();
container.RegisterType<IMyService, MyService>();
container.RegisterType<IOtherService, OtherService>();
```

依赖注入和控制反转是增强系统灵活性、可测试性和维护性的强大概念。在 C# 和 .NET 中，这些概念被广泛使用，并有相应的内置及第三方支持。

# 33. C# 设计模式

设计模式是解决软件设计中常见问题的重用方案。它们为解决特定问题提供了结构化的方法，并使代码更加模块化、易于维护且可扩展。在 C# 中，可以使用多种设计模式来应对不同的挑战。以下是一些常用设计模式的概述。

## 创建模式

单例模式：确保一个类只有一个实例，并为该实例提供全局访问点。
```csharp
public class Singleton
{
    private static Singleton instance;
    private Singleton() { }
    public static Singleton Instance
    {
        get
        {
            if (instance == null)
            {
                instance = new Singleton();
            }
            return instance;
        }
    }
}
```

工厂方法模式：定义一个创建对象的接口，但让子类更改将创建的对象的类型。
```csharp
public interface IProduct
{
    void Produce();
}

public class ConcreteProductA : IProduct
{
    public void Produce()
    {
}
```





```csharp
Console.WriteLine("Producing Product A");

    }
}

public class ConcreteProductB : IProduct
{
    public void Produce()
    {
        Console.WriteLine("Producing Product B");
    }
}

public interface IFactory
{
    IProduct CreateProduct();
}

public class ConcreteFactoryA : IFactory
{
    public IProduct CreateProduct()
    {
        return new ConcreteProductA();
    }
}

public class ConcreteFactoryB : IFactory
{
    public IProduct CreateProduct()
    {
        return new ConcreteProductB();
    }
}
```

# 结构模式

### 适配器模式 (Adapter Pattern)
适配器模式：允许现有类的接口被另一个接口使用。

```csharp
public interface ITarget
{
    void Request();
}

public class Adaptee
{
    public void SpecificRequest()
    {
        Console.WriteLine("Specific Request");
    }
}

public class Adapter : ITarget
{
    private readonly Adaptee adaptee;
    public Adapter(Adaptee adaptee)
    {
        this.adaptee = adaptee;
    }
    public void Request()
    {
        adaptee.SpecificRequest();
    }
}
```

### 装饰器模式 (Decorator Pattern)
装饰器模式：动态地将职责附加到对象上。装饰器为扩展功能提供了比子类化更灵活的替代方案。

```csharp
public interface IComponent
{
    void Operation();
}

public class ConcreteComponent : IComponent
{
    public void Operation()
    {
        Console.WriteLine("Concrete Component Operation");
    }
}

public abstract class Decorator : IComponent
{
    protected IComponent component;
    public Decorator(IComponent component)
    {
        this.component = component;
    }
    public virtual void Operation()
    {
        if (component != null)
        {
            component.Operation();
        }
    }
}

public class ConcreteDecoratorA : Decorator
{
    public ConcreteDecoratorA(IComponent component) : base(component) { }
    public override void Operation()
    {
        base.Operation();
        Console.WriteLine("Concrete Decorator A Operation");
    }
}

public class ConcreteDecoratorB : Decorator
{
    public ConcreteDecoratorB(IComponent component) : base(component) { }
    public override void Operation()
    {
        base.Operation();
        Console.WriteLine("Concrete Decorator B Operation");
    }
}
```

## 行为模式

### 观察者模式 (Observer Pattern)
观察者模式：在对象之间建立一种一对多的依赖关系，当一个对象的状态发生变化时，所有的依赖者都会得到通知并自动更新。

```csharp
public interface IObserver
{
    void Update(string message);
}

public class ConcreteObserver : IObserver
{
    private readonly string name;
    public ConcreteObserver(string name)
    {
        this.name = name;
    }
    public void Update(string message)
    {
        Console.WriteLine($"{name} received message: {message}");
    }
}

public interface ISubject
{
    void Attach(IObserver observer);
    void Detach(IObserver observer);
    void Notify(string message);
}

public class ConcreteSubject : ISubject
{
    private readonly List<IObserver> observers = new List<IObserver>();
    public void Attach(IObserver observer)
    {
        observers.Add(observer);
    }
    public void Detach(IObserver observer)
    {
        observers.Remove(observer);
    }
    public void Notify(string message)
    {
        foreach (var observer in observers)
        {
            observer.Update(message);
        }
    }
}
```

### 策略模式 (Strategy Pattern)
策略模式：定义一个算法族，将每个算法封装起来并使其可相互替。策略允许算法随使用它的客户端变化。

```csharp
using System;
public interface IStrategy
{
    void Execute();
}
public class ConcreteStrategyA : IStrategy
{
    public void Execute()
    {
        Console.WriteLine("Executing A");
    }
}

public class ConcreteStrategyB : IStrategy
{
    public void Execute()
    {
        Console.WriteLine("Executing B");
    }
}

public class Context
{
    private IStrategy _strategy;
    public Context(IStrategy strategy)
    {
        _strategy = strategy;
    }
    public void SetStrategy(IStrategy strategy)
    {
        _strategy = strategy;
    }
    public void ExecuteStrategy()
    {
        _strategy.Execute();
    }
}
class Program
{
    static void Main(string[] args)
    {
        // 创建带有 A 的上下文
        var context = new Context(new ConcreteStrategyA());
        context.ExecuteStrategy();
        // 将策略更改为 B
        context.SetStrategy(new ConcreteStrategyB());
        context.ExecuteStrategy();
    }
}
```

# 34. Windows Forms 和 WPF 

Windows Forms (WinForms) 和 Windows Presentation Foundation (WPF) 是 C# 中开发图形用户界面 (GUI) 的两种流行框架。本指南概述了这两种技术的核心概念。

## Windows Forms (WinForms)
Windows Forms 简介：Windows Forms 是微软的一种用于为 Windows 操作系统开发应用程序的图形应用程序接口 (API)。它提供了一套控件和库，用于通过传统的事件驱动编程模型构建桌面应用程序。

创建一个简单的 WinForms 应用程序
```csharp
using System;
using Windows.Forms;

public class MainForm : Form
{
    private Button myButton;
    public MainForm()
    {
        InitializeComponents();
    }
    private void InitializeComponents()
    {
        myButton = new Button
        {
            Text = "Click me!",
            Location = new System.Drawing.Point(50, 50)
        };
        myButton.Click += MyButton_Click;
        Controls.Add(myButton);
    }
    private void MyButton_Click(object sender, EventArgs e)
    {
        MessageBox.Show("Button clicked!");
    }
    [STAThread]
    public static void Main()
    {
        Application.EnableStyles();
        Application.Run(new MainForm());
    }
}
```

## Windows Presentation Foundation (WPF)
Windows Presentation Foundation 是构建 Windows 桌面应用程序的 UI 框架。与 WinForms 相比，它提供了更现代灵活的用户界面设计方法。WPF 使用扩展应用程序标记语言 (XAML) 来定义 UI 元素及其关系。

创建一个简单的 WPF 应用程序
```xml
<Window x:Class="WpfApp.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        Title="WPF App" Height="200" Width="300">
    <Grid>
        <Button Content="Click me!" HorizontalAlignment="Center" VerticalAlignment="Center" Click="Button_Click"/>
    </Grid>
</Window>
```
```csharp
using System;
using System.Windows;

namespace WpfApp
{
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }
        private void Button_Click(object sender, RoutedEventArgs e)
        {
            MessageBox.Show("Button clicked!");
        }
    }

    public class App
    {
        [STAThread]
        public static void Main()
        {
            Application app = new Application();
            app.Run(new MainWindow());
        }
    }
}
```

## WinForms 和 WPF 的主要区别

### UI 定义
*   **WinForms**：UI 元素使用 C# 程序化定义。
*   **WPF**：UI 元素使用 XAML，允许 UI 设计与逻辑分离。

### 样式与主题
*   **WinForms**：样式选项有限。
*   **WPF**：通过 XAML 提供丰富的样式和主题能力。

### 布局系统
*   **WinForms**：使用基于控件的布局系统。
*   **WPF**：采用更先进布局系统，支持数据绑定和控件模板等功能。

### 图形与动画
*   **WinForms**：具有基础图形能力。
*   **WPF**：支持高级图形和动画处理。





* `WinForms`: 数据绑定有限。
* `WPF`: 强大的数据绑定能力。

Windows Forms 和 WPF 都提供了在 `C#` 中创建桌面应用程序的方法，但它们在 UI 设计、样式和功能方面有所不同。Windows Forms 更加简单，适用于快速开发，而 WPF 则为创建复杂的用户界面提供了一种更现代、功能更丰富的方法。在 `WinForms` 和 `WPF` 之间进行选择取决于你正在开发的应用程序的具体需求和复杂性。

# 35. 使用 ASP.NET 创建 Web 应用程序

ASP.NET 是微软开发的一个用于构建动态 Web 应用程序的框架。它支持多种编程语言，包括 `C#`。本指南概述了如何使用模型-视图-控制器 (`MVC`) 模式使用 ASP.NET 创建 Web 应用程序。

## ASP.NET MVC 简介

### MVC 架构

* `Model`（模型）：代表应用程序的数据和业务逻辑。
* `View`（视图）：显示用户界面并向用户呈现数据。
* `Controller`（控制器）：处理用户输入、处理请求并管理模型与视图之间的数据流。

### 创建简单的 ASP.NET MVC 

创建一个新的 ASP.NET `MVC` 项目：

1. 打开 `Visual Studio`。
2. 选择“创建新项目”。
3. 选择“ASP.NET Web 应用程序”并选择“MVC”。

理解项目结构：

* `Models`：包含表示数据和业务逻辑的类。
* `Views`：包含用户界面组件。
* `Controllers`：包含处理用户输入和请求的类。

添加控制器：

1. 右键点击 `Controllers` 文件夹。
2. 选择“添加” -> “控制器”。
3. 选择“MVC 5 `Controller` - 空”并对其进行命名，例如 `HomeController`。
4. 实现处理请求的动作（方法）。

```csharp
public class HomeController : Controller
{
    public ActionResult Index()
    {
        return View();
    }
}
```

添加视图：

* 右键点击 `Home` 文件夹内的 `Views` 文件夹。
* 选择“添加” -> “视图”。
* 为其命名，例如 `Index.cshtml`。
* 编写 HTML 并使用 Razor 语法显示动态数据。

```html
<h2>Welcome to ASP.NET MVC!</h>
```

配置路由：

* 打开 `App_Start` 文件夹中的 `RouteConfig.cs` 文件。
* 定义路由将 URL 映射到控制器和动作。

```csharp
public class RouteConfig
{
    public static void RegisterRoutes(RouteCollection routes)
    {
        routes.IgnoreRoute("{resource}.axd/{*pathInfo}");
        routes.MapRoute(
            name: "Default",
            url: "{controller}/{action}/{id}",
            defaults: new { controller = "Home", action = "Index", id = UrlParameter.Optional }
        );
    }
}
```

运行应用程序：

* 按 `F5` 或使用“启动”按钮运行应用程序。
* 在网络浏览器中访问应用程序，例如 `http://localhost:port/`。

## ASP.NET Core 和 Razor Pages

### ASP.NET Core 简介

ASP.NET Core 是一个跨平台、高性能且开源的框架，用于构建现代、云和连接互联网的应用程序。它是 `ASP.NET` 的演进，并支持跨平台开发。

### 创建简单的 ASP.NET Core Razor Pages 应用程序

1. 创建一个新的 `ASP.NET Core Razor Pages` 项目：
* 打开 `Visual Studio`。
* 选择“创建新项目”。
* 选择“ASP.NET Core Web 应用程序”并选择“Razor Pages”。

2. 理解项目结构：
* `Pages`：包含 Razor Pages，类似于 `MVC` 中的视图。
* `Model`：包含表示数据和业务逻辑的类。

3. 添加一个 Razor Page：
* 右键点击 `Pages` 文件夹。
* 选择“添加” -> “Razor 页”。
* 为其命名，例如 `Index.cshtml`。

4. 编写内容：
* 打开 `Index.cshtml`。
* 编写 HTML 并使用 Razor 语法显示动态数据。

```html
<h2>Welcome to ASP.NET Core Razor Pages!</h2>
```

5. 运行应用程序：
* 按 `F5` 或使用“启动”按钮运行应用程序。
* 在 Web 浏览器中访问应用程序，例如 `http://localhost:port/`。

## ASP.NET Core 核心概念

* **Middleware**（中间件）：用于处理请求和响应的软件组件。
* **Dependency Injection**（依赖注入）：允许将服务和依赖注入组件中，提高模块化和可测试性。
* **ASP.NET Identity**：为应用程序添加登录功能，包括注册、密码恢复和角色授权。

# 36. 使用 Blazor 进行 Web 开发

Blazor 是一个使用 `C#` 代替 JavaScript 构建交互式 Web 应用程序的框架。本指南提供了 Blazor 的概述。

## 理解 Blazor

### Blazor 托管模型

Blazor 支持两种托管模型：

* `Blazor WebAssembly (Wasm)`：客户端模型，在浏览器中通过 `WebAssembly` 运行。
* `Blazor Server`：服务端模型，通过 `SignalR` 向浏览器发送 UI 更新。

### 组件与页面

* `Components`：Blazor 应用程序的可复用构建块，可以相互嵌套。
* `Pages`：用于定义 Web 应用程序的特殊组件。
* `Razor Syntax`：Blazor 使用 Razor 语法创建动态内容。该语法允许在 HTML 中嵌入 `C#` 代码。

```html
<!-- Blazor 组件中的 Razor 语法 -->
<h1>Hello, @name!</h1>

@code {
    string name = "Blazor";
}
```

## 创建 Blazor 

### 创建 Blazor WebAssembly 应用程序

* 使用 `Visual Studio`：
* 打开 `Visual Studio`。
* 选择“创建新项目”。
* 选择“Blazor App”并选择“Blazor WebAssembly App”。

* 使用 `.NET CLI`：
* 打开命令行。
* 运行以下命令：

```bash
dotnet new blazorsasm -n MyBlazorApp
cd MyBlazorApp
dotnet run
```

## Blazor 的关键特性

* **代码共享**：`Blazor` 允许客户端和服务组件之间共享代码。共享代码可以包括模型、和服务和其他逻辑。
* **组件架构**：`Blazor` 应用程序基于组件架构构建，便于创建可复用的模块化 UI 组件。
* **依赖注入**：`Blazor` 支持依赖注入，允许开发者将服务和依赖项注入组件。
* **Blazor WebAssembly**：`Blazor WebAssembly` 允许通过 `WebAssembly` 直接在浏览器中运行 `C#` 代码，提供完整的客户端开发体验。
* **实时通信**：`Blazor Server` 支持通过 `SignalR` 实现服务器与客户端之间的实时通信，实现实时更新和动态内容。

## Blazor 与其他框架对比

* **Blazor vs. Angular/React/Vue**：`Blazor` 允许客户端和服务端使用 `C#`，而 `Angular`、`React` 和 `Vue` 主要是基于 JavaScript 的框架。
* **Blazor vs. ASP.NET MVC**：`Blazor` 是用于构建交互式 Web 应用程序的组件化框架，而 `ASP.NET MVC` 设计用于构建服务器渲染的 Web 应用程序。





Blazor 是一个多功能的 Web 开发框架，在客户端和服务器端都提供了 C# 的优势。无论是使用 Blazor WebAssembly 构建 Web 应用，还是利用 Blazor Server 的实时能力，开发者都可以使用熟悉的工具和语言创建现代且交互式的 Web 。

# 37. 使用 Web API 创建 RESTful 服务

ASP.NET Web API 是一个用于构建 HTTP 框架，它可以被多种客户端（包括 Web 浏览器、移动设备和桌面应用程序）消费。本指南概述了如何使用 C# 通过 ASP.NET Web API 创建 RESTful 服务。

## Web API 简介

### 什么是 REST？

表现层转移（REST）是一种设计网络的架构风格。RESTful 服务使用标准的 HTTP 方法（`GET`、`POST`、`PUT`、`DELETE`）对资源执行操作，数据通常以 JSON 或 XML 格式交换。

### RESTful 服务的主要特性

* **无状态**：客户端的每个请求都包含理解和满足请求所需的所有信息。
* **基于资源**：资源通过 URI 标识，客户端使用标准的 HTTP 方法与资源进行交互。
* **表现层**：资源可以有多种表现形式（如 JSON 或 XML），客户端可以选择它们偏好的表现形式。

## 创建一个简单的 Web API

### 创建新的 Web API 项目

#### 使用 Visual Studio：

* 打开 Visual Studio。
* 选择“创建新项目”。
* 选择“ASP.NET Core Web Application”。
* 选择“API”模板并点击“创建”。

#### 使用 .NET CLI：

* 打开命令提示符。
* 运行以下命令：

```bash
dotnet new webapi -n MyWebApi
cd MyWebApi
dotnet run
```

### 创建控制器 (Controller)

添加一个新控制器：

* 右键点击 `Controllers` 文件夹。
* 选择“添加” -> “控制器”。
* 选择“API 控制器 - 空”并进行命名，例如 `ValuesController`。
* 实现处理 HTTP 方法的操作（Actions）。

```csharp
[ApiController]
[Route("api/[controller]")]
public class ValuesController : ControllerBase
{
    // GET api/values
    [HttpGet]
    public ActionResult<IEnumerable<string>> Get()
    {
        return new string[] { "value1", "value2" };
    }

    // GET api/values/5
    [HttpGet("{id}")]
    public ActionResult<string> Get(int id)
    {
        return "value";
    }

    // POST api/values
    [HttpPost]
    public void Post([FromBody] string value)
    {
        // 处理 POST 请求
    }

    // PUT api/values/5
    [HttpPut("{id}")]
    public void Put(int id, [FromBody] string value)
    {
        // 处理 PUT 请求
    }

    // DELETE api/values/5
    [HttpDelete("{id}")]
    public void Delete(int id)
    {
        // 处理 DELETE 请求
    }
}
```

### 运行 Web API

运行应用程序：

* 按 F5 或使用“启动”按钮运行应用程序。
* 在 Web 浏览器或使用 Postman 等工具访问 API。

测试 API 端点：

* 使用类似 `http://localhost:port/api/values` 的 URL 进行 `GET` 请求。
* 向相应的端点发送 `POST`、`PUT` 和 `DELETE` 请求。

## 在 Web API 中处理数据

### 模型类 (Model Classes)：创建模型类来表示 API 所处理的数据。

```csharp
public class Item
{
    public int Id { get; set; }
    public string Name { get; set; }
}
```

### 使用依赖注入 (Dependency Injection)：将服务注入控制器中以处理数据操作。

```csharp
[ApiController]
[Route("api/[controller]")]
public class ItemsController : ControllerBase
{
    private readonly IItemService _itemService;

    public ItemsController(IItemService itemService)
    {
        _itemService = itemService;
    }

    // GET api/items
    [HttpGet]
    public ActionResult<IEnumerable<Item>> Get()
    {
        var items = _itemService.GetItems();
        return Ok(items);
    }

    // GET api/items/5
    [HttpGet("{id}")]
    public ActionResult<Item> Get(int id)
    {
        var item = _itemService.GetItemById(id);
        if (item == null)
        {
            return NotFound();
        }
        return Ok(item);
    }

    // POST api/items
    [HttpPost]
    public ActionResult<Item> Post([FromBody] Item item)
    {
        _itemService.AddItem(item);
        return CreatedAtAction(nameof(Get), new { id = item.Id }, item);
    }

    // PUT api/items/5
    [HttpPut("{id}")]
    public IActionResult Put(int id, [FromBody] Item item)
    {
        if (id != item.Id)
        {
            return BadRequest();
        }
        _itemService.UpdateItem(item);
        return NoContent();
    }

    // DELETE api/items/5
    [HttpDelete("{id}")]
    public IActionResult Delete(int id)
    {
        _itemService.DeleteItem(id);
        return NoContent();
    }
}
```

### 服务接口与实现：为服务定义接口并提供一个实现。

```csharp
public interface IItemService
{
    IEnumerable<Item> GetItems();
    Item GetItemById(int id);
    void AddItem(Item item);
    void UpdateItem(Item item);
    void DeleteItem(int id);
}

public class ItemService : IItemService
{
    private readonly List<Item> _items = new List<Item>
    {
        new Item { Id = 1, Name = "Item 1" },
        new Item { Id = 2, Name = "Item 2" }
    };

    public IEnumerable<Item> GetItems()
    {
        return _items;
    }

    public Item GetItemById(int id)
    {
        return _items.FirstOrDefault(item => item.Id == id);
    }

    public void AddItem(Item item)
    {
        item.Id = _items.Count + 1;
        _items.Add(item);
    }

    public void UpdateItem(Item item)
    {
        var existingItem = _items.FirstOrDefault(i => i.Id == item.Id);
        if (existingItem != null)
        {
            existingItem.Name = item.Name;
        }
    }

    public void DeleteItem(int id)
    {
        var itemToRemove = _items.FirstOrDefault(item => item.Id == id);
        if (itemToRemove != null)
        {
            _items.Remove(itemToRemove);
        }
    }
}
```

### 安全 Web API

**身份验证与授权**：通过实现身份验证和授权机制来保护您的 Web API。ASP.NET Core 支持多种方案的身份验证和授权，例如 JWT（JSON Token）和 OAuth。

**基于角色的授权**：实现基于角色的授权，根据用户的角色控制对特定端点的访问。

```csharp
[Authorize(Roles = "Admin")]
[ApiController]
[Route("api/[controller]")]
public class AdminController : ControllerBase
{
    // 仅允许“Admin”角色的用户访问的控制器
}
```

# 38. 使用 ADO.NET 操作数据库

ADO.NET（ActiveX Data Objects for .NET）是 .NET Framework 中一组用于从关系型数据库访问和操作数据的类。本指南概述了如何使用 C# 通过 ADO.NET 操作数据库。

## ADO.NET 简介

### ADO.NET 的组件

* **连接 (Connection)**：管理与数据库的连接。
* **命令 (Command)**：执行 SQL 查询或存储过程。
* **读取器 (DataReader)**：从数据库读取只读的行数据流。
* **适配器 (DataAdapter)**：为 DataSet 填充数据并更新数据库。
* **数据集 (DataSet)**：表示内存中的数据缓存。
* **数据表 (DataTable)**：表示内存中的单张表。
* **数据视图 (DataView)**：表示 DataTable 的可绑定的、自定义视图。

### ADO.NET 工作流

**建立连接**：使用 `SqlConnection` 对象打开与数据库的连接。

**执行命令**：使用 `SqlCommand` 对象执行 SQL 查询或存储过程。





# 获取数据
使用 `SqlDataReader` 从数据库读取数据。

# 更新数据库
使用 `SqlDataAdapter` 根据 `DataSet` 中的更改更新数据库。

# 连接到数据库

### 连接字符串
```csharp
string connectionString = "Data Source=ServerName;Initial Catalog=DatabaseName;User Id=Username;Password=Password;";
```

### 开启和关闭连接
```csharp
using (SqlConnection connection = new SqlConnection(connectionString))
{
    connection.Open();
    // 执行数据库操作
} // 离开 using 块时连接会自动关闭
```

# 执行 SQL 查询查询

### SqlCommand
```csharp
string queryString = "SELECT * FROM Customers";
using (SqlConnection connection = new SqlConnection(connectionString))
{
    connection.Open();
    using (SqlCommand command = new SqlCommand(queryString, connection))
    {
        using (SqlDataReader reader = command.ExecuteReader())
        {
            while (reader.Read())
            {
                // 处理数据
                string customerName = reader["CustomerName"].ToString();
            }
        }
    }
}
```

## 执行存储过程

### 带参数调用存储过程
```csharp
string procedureName = "GetCustomerById";
int customerId = 1;
using (SqlConnection connection = new SqlConnection(connectionString))
{
    connection.Open();
    using (SqlCommand command = new SqlCommand(procedureName, connection))
    {
        command.CommandType = CommandType.StoredProcedure;
        command.Parameters.Add(new SqlParameter("@CustomerId", customerId));
        using (SqlDataReader reader = command.ExecuteReader())
        {
            while (reader.Read())
            {
                // 处理数据
            }
        }
    }
}
```

# 使用 DataSet 和 DataAdapters

### 使用 DataAdapter 填充 DataSet
```csharp
string queryString = "SELECT * FROM Customers";
using (SqlConnection connection = new SqlConnection(connectionString))
{
    connection.Open();
    using (SqlDataAdapter adapter = new SqlDataAdapter(queryString, connection))
    {
        DataSet dataSet = new DataSet();
        adapter.Fill(dataSet, "Customers");
        // 访问 DataSet 中的数据
        DataTable customersTable = dataSet.Tables["Customers"];
        foreach (DataRow row in customersTable.Rows)
        {
            // 处理数据
            string customerName = row["CustomerName"].ToString();
        }
    }
}
```

### 使用 DataAdapter 更新数据库
```csharp
string queryString = "SELECT * FROM Customers";
using (SqlConnection connection = new SqlConnection(connectionString))
{
    connection.Open();
    using (SqlDataAdapter adapter = new SqlDataAdapter(queryString, connection))
    {
        DataSet dataSet = new DataSet();
        adapter.Fill(dataSet, "Customers");
        // 修改 DataSet 中的数据
        // 将更改更新到数据库
        adapter.Update(dataSet, "Customers");
    }
}
```

# 事务

### 事务管理
```csharp
using (SqlConnection connection = new SqlConnection(connectionString))
{
    connection.Open();
    SqlTransaction transaction = connection.BeginTransaction();
    try
    {
        // 在事务内执行多个数据库操作
        transaction.Commit();
    }
    catch (Exception ex)
    {
        // 处理异常并回滚事务
    }
}
```




容器是轻量级、独立且可执行的软件包，它们包含了运行某个软件所需的所有内容，包括代码、运行时、库和系统工具。它们提供了跨环境的一致性，使得应用程序的部署和扩展变得更容易。

## Docker 基础

- `Docker Image`（镜像镜像）：一个轻量级、独立且可执行的包，包含了运行软件所需的所有内容。
- `Docker Container`（Docker 容器）：`Docker image`的一个实例，作为进程在宿主机上运行。
- `Dockerfile`：一个定义了 `Docker image` 内容、配置和运行时的脚本。

## 使用 Docker 将 C# 应用程序容器化

### 创建简单的 C# 应用程序

在 Visual Studio 中或使用 `.NET` CLI 创建一个新的 C# 控制台应用程序。

```
dotnet new console -n MyCSharpApp
cd MyCSharpApp
```

在 `Program.cs` 中编写代码。

```csharp
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, Docker!");
    }
}
```

### 创建一个 Dockerfile

在项目目录中创建一个名为 `Dockerfile` 的文件，内容如下：

```dockerfile
# 使用官方的 .NET SDK 镜像
FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build

# 设置工作目录
WORKDIR /app

# 将项目文件复制到容器中
COPY . ./

# 构建应用程序
RUN dotnet publish -c Release -o out

# 使用官方的 .NET 运行时镜像
FROM mcr.microsoft.com/dotnet/runtime:6.0 AS runtime

# 设置工作目录
WORKDIR /app

# 从构建阶段复制发布的应用程序
COPY --from=build /app/out ./

# 运行应用程序
CMD ["./MyCSharpApp"]
```

### 构建并运行 Docker 镜像

构建 Docker 镜像。

```
docker build -t my-csharp-app .
```

运行 Docker 容器。

```
docker run my-csharp-app
```

## 用于多容器应用程序的 Docker Compose

### Docker Compose 简介

`Docker Compose` 是一个用于定义和运行多容器 Docker 应用程序的工具。它允许你在 `docker-compose.yml` 文件中定义服务、网络和卷。

### 创建 Docker Compose 文件

在项目目录中创建一个名为 `docker-compose.yml` 的文件，内容如下：

```yaml
version: '3'
services:
  my-csharp-app:
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - "8080:80"
```

### 使用 Docker Compose 构建和运行

构建并运行 Docker Compose 服务。

```
docker-compose up
```

在浏览器中访问 `http://localhost:8080` 应用程序。

使用 Docker 进行容器化为运行 C# 应用程序提供了一个一致且可重现的环境。通过创建 `Dockerfile` 并使用 `Docker Compose`，开发者可以以标准化的方式在不同环境中轻松打包、部署和扩展 C# 应用程序。理解容器化对于现代软件开发实践至关重要，它促进了灵活性、可移植性和易用性。



```csharp
public class Service1 : IService1
{
    public string GetData(int value)
    {
        return $"You entered: {value}";
    }
    public CompositeType GetDataUsingDataContract(CompositeType composite)
    {
        if (composite == null)
        {
            throw new ArgumentNullException(nameof(composite));
        }
        if (composite.BoolValue)
        {
            composite.StringValue += "Suffix";
        }
        return composite;
    }
}
```

## 4. 配置服务

打开 `Web.config` 文件并配置服务端点。

```xml
<services>
    <service name="WcfServiceLibrary1.Service1">
        <endpoint address="" binding="basicHttpBinding" contract="WcfServiceLibrary1.IService1" />
        <endpoint address="mex" binding="mexHttpBinding" contract="IMetadataExchange" />
        <host>
            <baseAddresses>
                <add baseAddress="http://localhost:8733/Design_Time_Addresses/WcfServiceLibrary1/Service1/" />
            </baseAddresses>
        </host>
    </service>
</services>
```

## 5. 服务

按下 `F5` 启动 `WCF Test Client` 并测试服务方法。

## 消费 WCF 服务

### 添加服务引用

1. 打开一个新或现有的 C# 项目。
2. 在 `Solution Explorer`（解决方案资源管理器）中右键点击项目。
3. 添加服务引用。
* 选择 `"Add"` -> `"Service Reference."。
* 输入服务端点地址（例如，`http://localhost:8733/Design_Time_Addresses/WcfServiceLibrary1/Service1/`）并点击 `"Go."。
* 提供命名空间并点击 `"OK."。

### 使用生成的代理类

* 在你的代码中，创建生成代理类的实例并调用服务方法。

```csharp
using (ServiceReference1.Service1Client client = new ServiceReference1.Service1Client())
{
    string result = client.GetData(42);
    Console.WriteLine(result);
    ServiceReference1.CompositeType composite = new ServiceReference1.CompositeType
    {
        BoolValue = true,
        StringValue = "Hello"
    };
    ServiceReference1.CompositeType resultComposite = client.GetDataUsingDataContract(composite);
    Console.WriteLine($"Result: {resultComposite.StringValue}");
}
```

### 运行客户端应用程序

* 执行客户端应用程序并观察结果。

在 C# 中创建和消费 WCF 服务允许开发者构建可扩展和互操作的分布式系统。服务合约定义了服务提供的操作，客户端可以生成代理类与服务进行交互。配置服务端点并使用生成的代理类使得在 C# 中构建和消费 WCF 服务变得简单。

# 43. C# 与云计算 (Azure, AWS, GCP)

`Azure`、`AWS` (Amazon Web Services) 和 `GCP` (Google Cloud Platform) 等云平台提供了用于构建、部署和管理应用程序各种服务。本指南介绍了如何利用 C# 在这些平台上进行云开发。

## 云计算简介

### 关键云概念

* `基础设施即服务 (IaaS)`：通过互联网提供虚拟化的计算资源。
* `平台即服务 (PaaS)`：提供一个包含基础设施、运行时和中间件组件的平台。
* `软件即服务 (SaaS)`：以订阅方式通过互联网交付软件应用程序。

### 云服务模型

* `计算服务`：虚拟机、容器和无服务器计算。
* `存储服务`：Blob 存储、文件存储和数据库。
* `网络服务`：虚拟网络、负载均衡器和内容分发。




# 用于 UI 的 XAML
`XAML` (可扩展应用程序标记语言) 用于以声明式方式定义 UI。它允许创建 UI 元素并定义它们的属性。

```xml
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="MyApp.MainPage">
    <StackLayout>
        <Label Text="Welcome to Xamarin.Forms!"
               VerticalOptions="CenterAndExpand"
               HorizontalOptions="CenterAndExpand" />
        <Button Text="Click me" Clicked="OnButtonClicked" />
    </StackLayout>
</ContentPage>
```

# 数据绑定
Xamarin.Forms 支持数据绑定，允许根据底层数据的变化动态更新 UI 元素。

```xml
<Label Text="{Binding WelcomeMessage}" />
```

```csharp
public class MyViewModel : INotifyPropertyChanged
{
    private string welcomeMessage;
    public string WelcomeMessage
    {
        get { return welcomeMessage; }
        set
        {
            welcomeMessage = value;
            OnPropertyChanged(nameof(WelcomeMessage));
        }
    }
    public event PropertyChangedEventHandler PropertyChanged;
    protected virtual void OnPropertyChanged(string propertyName)
    {
        PropertyChanged?.Invoke(this, new PropertyChangedEventArgs(propertyName));
    }
}
```

## Xamarin.Native
## Xamarin.iOS 和 Xamarin.Android
针对特定平台的需求，Xamarin 允许开发者使用 `Xamarin.iOS` 进行 iOS 开发使用 `Xamarin.Android` 进行 Android 开发编写原生代码。

### iOS 示例
```csharp
public class MyiOSViewController : UIViewController
{
    public override void ViewDidLoad()
    {
        base.ViewDidLoad();
        var label = new UILabel
        {
            Text = "Welcome to Xamarin.iOS!",
            Frame = new CoreGraphics.CGRect(50, 50, 200, 20)
        };
        View.AddSubview(label);
    }
}
```

### Android 示例
```csharp
[Activity(Label = "MyAndroidActivity", MainLauncher = true, Icon = "@mipmap/icon")]
public class MyAndroidActivity : Activity
{
    protected override void OnCreate(Bundle savedInstanceState)
    {
        base.OnCreate(savedInstanceState);
        SetContentView(Resource.Layout.Main);
        var label = FindViewById<TextView>(Resource.Id.myLabel);
        label.Text = "Welcome to Xamarin.Android!";
    }
}
```

## Xamarin.Essentials
`Xamarin.Essentials` 是一个为常用设备功能提供跨平台 API 的库。它简化了对相机、GPS、联系人等功能的访问。

### 示例：定位
```csharp
var location = await Geolocation.GetLastKnownLocationAsync();
```

## Xamarin.Forms vs. Xamarin.Native
- `Xamarin.Forms`: 跨平台共享 UI 和业务逻辑，适用于简单的应用程序。
- `Xamarin.Native`: 适用于具有复杂且特定 UI 需求的应用程序。

# Xamarin 社区与工具
Xamarin 拥有活跃的社区，开发者可以使用带有 `Xamarin` 扩展的 `Visual Studio` 或 `Visual Studio Code` 进行开发。`Xamarin.Forms` 提供了一系列预构建的 UI 控件，社区社区贡献。

# Unity 引擎
Unity 是一个使用 C# 创建游戏的强大引擎。

## GameObject 与组件
`GameObject` 代表场景中的实体。`Transform` 组件管理位置、旋转和缩放。`Collider` 组件启用碰撞检测。`Rigidbody` 组件添加物理行为。

## 物理与动画
### Unity 中的物理
物理交互。`Physics.Raycast` 发射射线以检测物体。当碰撞器发生作用时，会触发 `Collision Events`（碰撞事件）。
```csharp
void OnCollisionEnter(Collision collision)
{
}
```

### Unity 中的动画
`Animator` 组件控制动画。`Animation Clips` 定义了单个动画片段。`Blend Trees`（混合树）根据参数混合多个动画。

## UI 与用户输入
### Unity UI 系统
`Canvas`: UI 元素的容器。`UI Text`、`Image`、`Button`: 普通 UI 组件。`Event System` 处理用户输入。

### Unity 中的用户输入
`Input` 类捕获用户输入。`Input Manager` 为输入提供可配置设置。
```csharp
void Update()
{
    float horizontalInput = Input.GetAxis("Horizontal");
    float verticalInput = Input.GetAxis("Vertical");
}
```

## 场景与预制体 (Prefabs)
`Scenes`: 代表 Unity 的关卡或章节。`Prefabs`: 可复用的游戏对象模板。

## C# 脚本
`MonoBehaviour`: Unity 脚本的基类。`Start` 和 `Update` 等生命周期方法每帧调用一次。
```csharp
using UnityEngine;

public class MyScript : MonoBehaviour
{
    void Start()
    {
    }
    void Update()
    {
    }
}
```

## 最佳实践
### 代码组织
- `Separation of Concerns`（关注分离）：将代码分为逻辑组件。
- `ScriptableObjects`: 独立于 `MonoBehaviour` 实例存储数据。

## 性能优化
- `Object Pooling`（对象池）：重用对象而不是实例化和销毁它们。
- `Batching`（批）：将多次渲染调用合并到一个批次。

## 协作开发
### 版本控制
- `Unity Collaborate`: Unity 内置的版本控制。
- `Git`、`SVN`: 外部版本控制系统。

### 工具
- `Unity Collab`: 基于云的协作开发。
- `Photon Unity Networking (PUN)`: 多人网络解决方案。

# 构建与部署
### 平台构建
- `Build Settings`: 配置目标平台。
- `Build Process`: 生成用于部署的可执行文件。

### 平台
- PC/Mac/Linux 独立
- iOS 和 Android
- WebGL
- 主机平台 (PlayStation, Xbox)

# 46. 使用 ML.NET 进行机器学习与人工智能




ML.NET 是由微软开发的一个开源机器学习框架，用于使用 `C#` 和 `.NET` 构建自定义机器学习模型。本指南将介绍如何使用 `ML.NET` 引入机器学习和人工智能（AI）。

## 机器学习简介

## 什么是机器学习？

* `机器学习 (ML)`：人工智能的一个子集，使系统能够从经验中学习并不断改进。
* `监督学习`：在带有标记的数据上进行训练模型。
* `无监督学习`：从未标记的数据中提取模式。
* `强化学习`：通过基于奖励的系统来训练模型。

## ML.NET 基础知识

* `ML.NET` 库：为机器学习任务提供工具和库。
* `数据流水线 (Data Pipeline)`：为模型训练对数据进行预处理和转换。
* `模型训练`：创建并训练机器学习模型。
* `模型评估`：评估已训练模型的性能。

## ML.NET 数据流水线

### 数据加载与准备

* `IDataView` 接口：表示对数据集的可变、惰性视图。
* `LoadFromEnumerable`：从内存集合中加载数据。
* `数据预处理`：清洗和转换数据。

```sharp
var data = new List<MyData>
{
    new MyData { Feature1 = 1.2F, Feature2 = 2.3F, Label = true },
    // 添加更多数据...
};

var context = new MLContext();
var dataView = context.Data.LoadFromEnumerable(data);
```

### 数据转换

* `特征化`：将原始数据转换为特征。
* `归一化`：缩放特征以保持范围一致性。

```csharp
var pipeline = context.Transforms.Conversion.MapValueToKey("Label")
    .Append(context.Transforms.Concatenate("Features", "Feature1", "Feature2"))
    .Append(context.Transforms.NormalizeMinMax("Features"));
```

## 使用 ML.NET 进行模型训练

### 选择模型

* `算法`：`ML.NET` 支持用于分类、回归、聚类等的各种算法。
* `模型配置`：设置超参数和选项。

```csharp
var trainer = context.BinaryClassification.Trainers.SdcaLogisticRegression();
```

### 模型训练与评估

* `Fit` 方法：使用训练数据训练模型。
* `Evaluate` 方法：评估模型的性能。

```csharp
var model = pipeline.Append(trainer)
    .Fit(dataView);

var metrics = context.BinaryClassification.Evaluate(model.Transform(dataView));
```

## ML.NET 模型消费

### 模型保存与加载

* `保存模型`：持久化已训练的模型以供将来使用。
* `加载模型`：加载预训练模型。

```csharp
context.Model.Save(model, data.Schema, "model.zip");
var loadedModel = context.Model.Load("model.zip", out var modelSchema);
```

### 进行预测

* `预测引擎 (Prediction Engine)`：创建一个用于进行预测的引擎。
* `Predict` 方法：从新数据获取预测结果。

```csharp
var predictionEngine = context.Model.CreatePredictionEngine<MyData, MyPrediction>(model);
var prediction = predictionEngine.Predict(new MyData { Feature1 = 0.8F, Feature2 = 1.5F });
```

## 高级 ML.NET 功能

### 模型可解释性

* `解释性`：理解和解释模型的预测结果。
* `全局与局部解释性`：对模型行为的洞察。

```csharp
var explainer = context.Model.LoadTreeEnsembleClassificationModel(modelPath);
var globalExplanation = explainer.GetOverallFeatureContribution();
var localExplanation = explainer.GetPerInstanceFeatureContribution(dataView, 0);
```

### 自动机器学习 (AutoML)

* `AutoML 实验`：自动模型选择和调优。
* `探索与利用`：在搜索空间中平衡探索与利用。

```csharp
var experiment = context.Auto().CreateBinaryClassificationExperiment(500);
var result = experiment.Execute(dataView);
```

## ML.NET 与 .NET 应用的集成

### .NET Core 和 ASP.NET 集成

* Web 应用中的 `ML.NET`：在 `ASP.NET` 中嵌入 `ML.NET` 模型。
* `实时预测`：实时提供预测服务。

```csharp
public IActionResult Predict([FromBody] MyData input)
{
    var prediction = predictionEngine.Predict(input);
    return Ok(prediction);
}
```

### 与 Azure 集成

* `Azure 机器学习服务`：在 `Azure` 上部署和管理 `ML.NET` 模型。
* `Azure Functions`：`ML.NET` 模型的无服务器执行。

```csharp
[FunctionName("PredictFunction")]
public static async Task<IActionResult> Run(
    [HttpTrigger(AuthorizationLevel.Function, "post", Route = null)] HttpRequest req,
    ILogger log)
{
    // ML.NET 预测逻辑
    return new OkObjectResult(prediction);
}
```

`ML.NET` 简化了将机器学习和人工智能能力整合到 `.NET` 应用的过程。理解机器学习的基础知识、数据准备、模型训练和模型消费，对于在现实场景中成功实现 `ML.NET` 至关重要。利用模型可解释性和自动机器学习等高级功能可以增强 `ML.NET` 的能力。与 `.NET Core`、`ASP.NET` 以及云服务的集成进一步扩展了 `ML.NET` 在不同应用场景中的覆盖范围和适用性。

# 47. C# 与原生代码的互操作性

`C#` 提供了与原生代码互操作的强大功能，允许开发者无缝集成并使用用 `C` 或 `C++` 等语言编写的组件。本指南将探索 `C#` 与原生代码互操作各个方面。

## 互操作性简介

### 为什么需要互操作性？

* `重用现有代码`：引入原生编写的遗留代码或性能关键代码。
* `平台集成`：与系统 API 交互。
* `跨语言开发`：与其他项目协作。

## 互操作性方法

* `平台调用服务 (P/Invoke)`：从托管代码中调用原生函数。
* `C++/CLI (托管 C++)`：创建混合模式集。
* `COM 互操作性`：与组件交互。

## P/Invoke (平台调用服务)

### P/Invoke 基础

* `DllImport` 特性：将原生函数导入 `C#`。
* `调用约定`：指定参数在托管代码和原生代码之间传递的方式。

```csharp
using System.InteropServices;

class Program
{
    [DllImport("User32.dll")]
    public static extern int MessageBox(IntPtr hWnd, string text, string caption, uint type);

    static void Main()
    {
        MessageBox(IntPtr.Zero, "Hello from P/Invoke!", "Greetings", 0);
    
```

### 处理数据类型

* `原始类型`：传递整数、布尔值、字符串和结构体。
* `数组与指针`：在原生代码中处理数组和指针。
* `结构体布局`：确保内存对齐。

```csharp
[StructLayout(LayoutKind.Sequential)]
public struct Point
{
    public int X;
    public int Y;
}

[DllImport("NativeLibrary.dll")]
public static void ProcessPoint(Point point);
```

## C++/CLI (托管 C++)

### 混合模式集

* `创建混合模式项目`：融合 `C#` 和 `C++`。
* `托管与未托管代码`：在两者之间进行交互。

```cpp
// NativeCode.cpp
extern "C" __declspec(dllexport) int AddNumbers(int a, int b)
{
    return a + b;
}
```

```csharp
// ManagedCode.cs
class Program
{
    [DllImport("NativeCode.dll")]
    public static extern int AddNumbers(int a, int b);

    static void Main()
    {
        int result = AddNumbers(3, 4);
        Console.WriteLine(result); // 输出: 7
    }
}
```

### Ref 类与值类

* `引用类 (Ref Classes)`：具有原生功能的托管类。
* `值类 (Value Classes)`：用于互操作的轻量级结构体。

```cpp
// NativeClass.h
public ref class NativeRefClass
{
public:
    int AddNumbers(int a, int b);
};

// NativeStruct.h
public value struct NativeValueStruct
{
    int X;
    int Y;
};
```

```csharp
// ManagedCode.cs
NativeRefClass^ nativeRefInstance = gcnew NativeRefClass();
int result = nativeRefInstance->AddNumbers(3, 4);

NativeValueStruct valueStruct;
valueStruct.X = 10;
valueStruct.Y = 20;
```

## COM 互操作性

### COM 组件

* `组件对象模型 (COM)`：Windows 上的软件组件的标准。





## 基于接口的通信
通过接口访问功能。

## C# 与 COM 的互操作

```csharp
Type comType = Type.GetTypeFromProgID("SomeCOMComponent");

dynamic comInstance = Activator.CreateInstance(comType);

comInstance.SomeMethod();
```

## 生成互操作程序集

- `tlbimp` 工具：从 COM 类型库生成互操作程序集。

## 安全性考量

### 代码访问安全
- `Permissions`：为程序集授予必要的权限。
- `Security Levels`：理解信任级别和安全策略。

### SafeHandle 类
- `SafeHandle`：操作系统句柄的包装器。
- `Automatic Cleanup`：确保资源的正确释放。

```csharp
public class SafeFileHandle : SafeHandle
{
    // SafeHandle 的实现
}
```

## 调试与诊断

### 调试原生代码
- `Debug Symbols`：在原生代码中包含调试信息。
- `Attach to Process`：在调试托管代码的同时调试原生代码。

### 诊断工具
- `Performance Profiling`：识别混合模式应用中的瓶颈。
- `Memory Analysis`：分析托管和原生组件的内存使用情况。

C# 与原生代码的互操作开启了广泛的可能性，从集成现有库到增强应用程序中性能关键的部分。理解 `P/Invoke`、`C++/CLI` 和 `COM Interop` 允许开发者根据其场景选择最合适的方法。安全性考量、调试技术和诊断工具是成功互操作的关键方面。无论是缩小托管与原生代码之间的差距，还是与 COM 组件集成，掌握这些互操作技术对于构建健壮且功能丰富的应用程序至关重要。

# 48. C# 中的国际化与本地化

国际化 (`i18n`) 和本地化 (`l10n`) 是软件开发的关键方面，允许应用程序支持多种语言并适应区域偏好。本指南探讨了 C# 中国际化本地化的原理和实现。

## 理解国际化

### 什么是国际化？
- 国际化 (`i18n`)：设计和准备软件的过程，使其能够在不更改代码的情况下适应不同的语言和区域。
- `Culture`：语言和区域偏好的组合。

## 核心概念
- `Resource Files`：存储本地化的字符串、图像和其他资源。
- `CultureInfo` 类：代表有关特定文化的信息。

```csharp
CultureInfo usCulture = new CultureInfo("en-US");
CultureInfo frCulture = new CultureInfo("fr-FR");
```

## 为本地化准备您的应用程序

### 字符串外部化
- `String Resources`：将字符串移动到资源文件中以便翻译。
- `ResourceManager` 类：在运行时检索资源。

```csharp
ResourceManager rm = new ResourceManager("MyApp.Strings", typeof(Program).Assembly);
string greeting = rm.GetString("Hello", usCulture);
```

### 日期和数字格式
- `DateTime` 和 `Number Formats`：使用特定文化的格式。
- `ToString` 方法：应用特定文化的格式化。

```csharp
DateTime now = DateTime.Now;
string formattedDate = now.ToString("D", frCulture);
```

### 本地化用户界面
#### 使用资源文件
- `UI Elements`：翻译标签、按钮和消息。
- `Resource Files for UI`：为不同的语言分离不同的资源文件。

#### 卫星程序集
- `Satellite Assemblies`：单独存储特定语言的资源。
- `Resgen` 工具：生成卫星程序集。

```bash
resgen MyResources.fr-FR.resx
al /t:lib /embed:MyResources.fr-FR.resources.dll /culture:fr-FR /out:fr-FR\MyResources.resources.dll
```

## 处理复数和性别
#### 复数规则
- `PluralizationService`：处理复数规则。

```csharp
PluralizationService pluralizationService = PluralizationService.CreateService(usCulture);
string apples = pluralizationService.Pluralize("apple", 2);
```

#### 针对性别的翻译
- `Custom Resource Keys`：为不同性别使用不同的键。
- `Resource File Organization`：为性别结构化资源文件。

## 动态语言切换

### 检测用户偏好
- `HttpContext` 或 `Thread.CurrentThread`：检测用户偏好。
- `User Profile Information`：允许用户设置偏好语言。

```csharp
Thread.CurrentThread.CurrentCulture = new CultureInfo("fr-FR");
Thread.CurrentThread.CurrentUICulture = new CultureInfo("fr-FR");
```

### 存储用户偏好
- `User Profiles`：在用户配置文件中存储语言偏好。
- `Cookies` 或 `Session Storage`：持久化用户偏好。

## 测试与质量保证

### 本地化测试
- `Automated Tests`：验证翻译和格式。
- `Localization Tools`：使用用于翻译和测试的工具。

### 用户反馈
- `Feedback Mechanisms`：鼓励用户报告翻译问题。
- `Community Contributions`：允许用户贡献翻译。

国际化和本地化是创建面向全球观众软件不可不可缺的一部分。C# 提供了强大的工具和功能，使这一过程变得高效有效。通过字符串外部化、使用资源文件、处理日期和数字格式，以及考虑复数和性别特定翻译，开发者可以创建无缝适应不同语言和文化的应用程序。动态语言切换和适当的测试程序进一步增强了本地化应用程序的质量。采用这些做法可以确保在不同语言和文化背景下提供良好的用户体验。

# 49. C# 代码最佳实践

编写整洁、可维护且高效的代码对于构建健壮可扩展的应用程序至关重要。本指南提供了一套 C# 开发最佳实践，帮助您生成高质量代码。

## 代码结构与组织

### 清晰且一致的命名
- `Descriptive Names`：为变量、方法使用有意义且清晰的名字。
- `Consistent Naming`：遵循一致的命名约定。

### 将代码组织为小函数
- `Single Responsibility Principle (SRP)`：保持函数小并专注于单一任务。
- `Avoid Large Methods`：将复杂逻辑分解为更易管理的函数。

### 一致的代码风格
- `Consistent Formatting`：遵循一致的编码风格（例如括号的位置、缩进）。
- `Use Code Analyzers`：利用 `Roslyn Analyzers` 等工具强制执行标准。

```csharp
// 好
if (condition)
{
    // 代码块
}

// 不好
if (condition) {
    // 代码块
}
```

## 异常处理与日志

### 谨慎使用异常
- `Throw Specific Exceptions`：明确异常类型。
- `Avoid Catch-All Blocks`：只捕获你可以处理的异常。

```csharp
// 好
try
{
    // 可能抛出异常的代码
}
catch (SpecificException ex)
{
    // 处理特定异常
}

// 不好
try
{
    // 可能抛出任何异常的代码
}
catch (Exception ex)
{
    // 处理任何异常
}
```

### 日志最佳实践
- `Use Logging Libraries`：利用成熟的日志框架如 `Serilog` 或 `NLog`。
- `Include Context Information`：记录相关的上下文信息以便调试。

```csharp
_logger.LogInformation("Processing order {OrderId} for customer {CustomerId}.", orderId, customerId);
```

## 性能优化

### 优化前测量
- `Profile Code`：使用性能分析工具识别性能瓶颈。
- `Optimize Where Needed`：将优化放在关键部分。

### 高效的数据结构与算法
- `Choose the Right Collection Types`：根据所需的操作选择集合（例如 `List<T>` 与 `Dictionary<TKey, TValue>`）。
- `Use Appropriate Algorithms`：在选择算法时考虑算法复杂度。

```csharp
// 好
var list = new List<int>();
var dictionary = new Dictionary<string, int>();

// 不好
var array = new int[1000];
var hashSet = new HashSet<int>();
```





## 代码注释与文档

## 编写自文档化代码

- **使用具描述性的方法名和变量名**：通过使用清晰的名称尽量减少对注释的需求。
- **可读性强的代码**：确保代码易于理解，而不依赖注释。

## 文化公共 API

- **XML 注释**：使用 XML 注释文档化公共 API，以便自动生成文档。
- **提供示例**：为方法和类包含用法示例。

```csharp
/// <summary>
/// 计算两个数字之和。
/// </summary>
/// <param name="a">第一个数字。</param>
/// <param name="b">第二个数字。</param>
/// <returns>两个数字之和。</returns>
public int Add(int a, int b)
{
    return a + b;
}
```

## 单元测试与测试驱动开发 (TDD)

### 编写单元测试

- **测试公共接口**：确保公共方法和类经过彻底测试。
- **边界情况**：在测试中涵盖边界情况和特殊情况。

### 拥抱测试驱动开发
- **先写测试**：在实现功能之前从编写测试开始。
- **有信心的重构**：在现有测试的安全防护网下对代码进行重构。

## 版本控制与协作

### 使用版本控制

- **Git, SVN 等**：利用版本控制系统跟踪更改。
- **定期提交**：频繁地提交具有意义消息的原子化提交。

### 高效协作
- **拉取请求 (Pull Requests)**：使用拉取请求进行代码审查和协作。
- **沟通**：与团队成员清晰地沟通代码更改更改。

## 安全最佳实践

### 输入验证

- **验证用户输入**：始终对用户输入进行验证和清理，以防止安全漏洞。
- **避免硬编码机密**：使用安全的存储机制来处理密钥（例如，`Azure Key Vault`）。

### 防止 SQL 注入

- **参数化查询**：使用参数化查询防止 SQL 注入攻击。
- **ORM 和预处理语句**：利用对象关系映射 (ORM) 或预处理语句。

```csharp
// 良好
var command = new SqlCommand("SELECT * FROM Users WHERE Username = @Username", connection);
command.Parameters.AddWithValue("@Username", username);

// 糟糕
var command = new SqlCommand($"SELECT * FROM Users WHERE Username = '{username}'", connection);
```

## 持续集成与部署 (CI/CD)

## 设置持续集成

- **自动化构建**：使用 CI 工具（例如，`Jenkins`，`Azure DevOps`）进行自动化构建。
- **运行测试**：将单元测试集成到 CI 流水线中。

### 自动化部署

- **持续部署**：自动化部署过程，以实现更快、更可靠的发布。
- **回滚机制**：在出现部署问题时实现回滚机制。

遵循 C# 开发中的最佳实践可以使代码更具可维护性、可扩展性和安全性。通过关注代码组织、错误处理、性能优化和协作，开发者可以创建高质量的应用程序。定期的测试、文档编写以及将最佳实践集成到开发工作流中，有助于软件项目的整体成功。根据不断的需求不断演进和适应这些实践，可以确保您的代码库持续卓越。

# 50. C# 中的持续集成与部署 (CI/CD)

持续集成 (CI) 和持续部署 (CD) 是现代软件开发中不可或缺的实践。本指南介绍了 C# 项目的 CI/CD 实现，通过自动化构建和部署过程来确保快速且可靠的软件交付。

## CI/CD 简介

### 什么是 CI/CD？

- **持续集成 (CI)**：每天多次自动将代码更改集成到共享仓库的实践。
- **持续部署 (CD)**：CI 的扩展，在通过自动化测试后自动将代码更改部署到生产环境。

### 核心优势

- **及早发现问题**：在开发过程早期识别并修复问题。
- **快速的发布周期**：加速新功能和错误修复补的交付。
- **一致的部署**：确保部署过程的一致性。

## 设置持续集成

### 选择 CI 服务

- **Azure DevOps, Jenkins, Travis CI 等**：选择适用于项目的 CI 服务。
- **GitHub Actions**：利用 GitHub 功能。

### 配置步骤

- **定义构建步骤**：指定构建所需的步骤。
- **版本控制**：使用版本控制来构建。

```yaml
name: CI
on:
  push:
    branches:
      - main
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2
      - name: Setup .NET
        uses: actions/setup-dotnet@v1
        with:
          dotnet-version: 3.x
      - name: Restore Dependencies
        run: dotnet restore
      - name: Build
        run: dotnet build --configuration Release
```

## 实现自动化测试

### 包含单元测试

- **xUnit, NUnit, MSTest**：选择测试框架。
- **运行测试**：将测试集成到 CI 流水线。

```yaml
      - name: Run Tests
        run: dotnet test
```

### 集成代码覆盖率

- **Coverlet, OpenCover**：衡量代码覆盖率。
- **发布覆盖率报告**：使覆盖率可用。

```yaml
      - name: Test
        run: dotnet test /p:CollectCoverage=true /p:CoverletOutput=opencover
      - name: Publish Code Coverage
        uses: codecov/codecov-action@v2
```

## 持续部署

### 选择部署目标

- **Azure App Service, AWS Elastic Beanstalk, Docker**：选择部署平台。
- **无服务器架构**：如果适用，探索无服务器选项。

### 配置部署步骤

- **定义部署步骤**：指定部署所需的步骤。
- **使用部署槽**：利用部署槽进行渐进式发布。

```yaml
      - name: Deploy to Azure
        uses: azure/webapps-deploy@v2
        with:
          publish-profile: ${{ secrets.AZURE_APP_PUBLISH_PROFILE

## 处理密钥与安全

### 使用密钥管理

- **GitHub Secrets, Azure Key Vault 等**：安全地存储敏感信息。
- **令牌化**：避免在代码中硬编码密钥。

### 实现持续安全扫描

- **静态应用安全测试 (SAST)**：在 CI/CD 流水线中集成安全扫描工具。
- **依赖扫描**：定期检查依赖中的漏洞。

```yaml
      - name: Run Security Scan
        run: |
          # 您的安全扫描命令
```

## 监控与回滚

### 实现监控

- **Application Insights, ELK Stack 等**：设置监控工具以检测并响应问题。
- **自定义指标**：为特定的应用程序行为定义自定义指标。

### 回滚机制

- **自动回滚**：在部署失败时实现自动回滚机制。
- **健康检查**：包含健康检查以监控部署应用程序的状态。

在 C# 项目中实施 CI/CD 可以简化开发流程，实现更快、更可靠的发布。通过自动化构建、测试和部署过程，开发者可以尽早发现问题、确保部署的一致性并更快速地交付功能。利用 CI/CD 服务并集成安全措施可以提高软件的整体质量安全性。定期监控应用程序并配备回滚机制有助于构建稳健的部署管道。拥抱 CI/CD 实践以实现 C# 开发的持续改进和效率提升。





在每一行代码中，他们都编织了一个关于创新与创造的故事。这本书一直是你在 C# 广阔世界中的指南针。

合上这一章时，请记住：克服的每一项挑战都是一项成就，每一个解决方案都是通往精通的一步。

你的代码是赋予项目生命的旋律。愿你继续满怀激情地创作与编程！

感谢你让我成为这段旅程的一员。

致以谢意，

Hernando Abella
《开发者应该掌握的 50 个 C# 概念》作者

探索其他实用资源：

www.hernandoabella.com
