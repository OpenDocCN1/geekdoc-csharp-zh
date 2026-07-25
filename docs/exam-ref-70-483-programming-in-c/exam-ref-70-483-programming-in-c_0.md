# Exam Ref 70-483：C# 编程



![](img/orm_front_cover.jpg)

![考试参考 70-483：C# 编程](img/orm_front_cover.jpg)



> 献给我的父母，他们在我 7 岁时就鼓励我开始编程。
> —WOUTER DE KORT

# 特别升级优惠

如果您直接从 [oreilly.com](http://oreilly.com) 购买此电子书，您将获得以下福利：

* 无 DRM 限制电子书——无需任何限制或约束，即可跨设备使用您的电子书
* 多格式支持——可在笔记本电脑、平板电脑或手机上使用
* 终身访问，并提供免费更新
* Dropbox 同步——您的文件，随处可用

如果您是从其他零售商购买的本电子书，只需 4.99 美元即可升级您的电子书以享受所有这些福利。点击此处 访问您的电子书升级。

*请注意，示例内容不提供升级优惠。*

# 引言

微软 70-483 考试涵盖了广泛的主题，这些主题可以应用于您的 C# 开发工作中。本书帮助您理解 C# 语言的基础和更高级的。它向您展示了如何使用 C# 语言创建强大的软件应用程序。这本书还向您展示了如何使用添加到 C# 语言的新功能，例如对异步代码的支持。本书面向具有某些 C# 经验但希望加深知识并确保准备好考试的开发者。要使用书中的示例，您应该熟悉使用 `Visual Studio` 创建基础的 `Console Application`。

本书涵盖了每一个考试目标，但并没有涵盖每一个考试题。只有微软考试团队有权访问考试本身，微软定期向考试中添加新题，因此无法涵盖特定的题目。您应该将本书作为您相关实战经验和其他学习材料的补充。如果您在书中遇到自己不完全熟悉的课题，可以使用链接查找更多信息，并花时间研究和学习该主题。MSDN、TechNet、博客和论坛上都有优质信息。

# 微软认证

微软认证通过证明您对当前微软产品和技术的广泛技能和经验的掌握，使您脱颖而出。考试和相应的认证旨在验证您在本地和云端使用微软产品和技术设计、开发或实施和支持解决方案时，对关键胜能力的掌握程度。认证为个人、雇主和组织带来了各种利益。

## 更多信息：所有微软认证

有关微软认证的信息（包括可用认证的完整列表），请访问 [`www.microsoft.com/learning/en/us/certification/cert-default.aspx`](http://www.microsoft.com/learning/en/us/certification/cert-default.aspx)。

# 谁应该读本书

本书面向想要获得 C# 编程语言认证的开发者。本书帮助您准备并通过“70-483 考试：C# 编程”考试。成功通过 70-483 考试也可以被视为获得微软认证解决方案开发 (MCSD)：使用 C# 的 Windows Store 应用程序的学分之一。

阅读本书的开发者应该对编写简单的 C# 程序有基本的了解。您可以使用 `Visual Studio` 创建并运行应用程序。

## 假设

您至少拥有一年或以上的经验，使用 C# 为各种应用程序类型和硬件/软件平台编写核心业务/应用程序逻辑。随着您通过本书和其他学习资源的不断学习，您将精通开发复杂的应用程序。您将能够使用 C# 提供的所有功能。本书侧重于帮助那些目标是成为 C# 开发者的人。

您可以在考试准备指南中找到关于考试 70-483 受众的信息，该指南位于 [`www.microsoft.com/learning/en/us/exam-70-483.aspx#fbid=x2KPCL1L6z8`](http://www.microsoft.com/learning/en/us/exam-70-483.aspx#fbid=x2KPCL1L6z8)。

# 本书结构

本书分为四章。每章都关注于与“70-483 考试：C# 编程”相关的不同考试领域。每章进一步细分为由微软发布的特定考试目标；它们可以在“70-483 考试：C# 编程”网站的“正在衡量的技能”部分找到：[`www.microsoft.com/learning/en/us/exam-70-483.aspx#fbid=x2KPCL1L6z8`](http://www.microsoft.com/learning/en/us/exam-70-483.aspx#fbid=x2KPCL1L6z8)。

考试领域和目标涵盖的内容已整合到书中，使您拥有简洁的、按目标划分的内容，结合策略性的真实场景、思维实验和章末复习题，为读者提供专业级别的考试准备。

# 系统要求

当您对书中涵盖的课题不熟悉时，应该在您的学习电脑上练习该概念。您需要以下硬件和软件来完成书中的练习题：

* 一台可以安装 `Visual Studio` 的学习电脑（见下文硬件）或一台允许安装 `Visual Studio 2012` 的电脑。如果您拥有这些版本之一的许可，可以使用 `Visual Studio 2012` 专业版、高级版或终极版。如果没有授权版本，您也可以从 [`www.microsoft.com/visualstudio/eng/downloads`](http://www.microsoft.com/visualstudio/eng/downloads) 下载 Windows 桌面 Express 版。
* `Visual Studio 2012` 支持以下操作系统：Windows 7 SP1 (x86 和 x64)，Windows 8 (x86 和 x64)，Windows Server 2008 R2 SP1 (x64)，Windows Server 2012 (x64)。
* `Visual Studio 2012` 的最低硬件要求：1.6 GHz 或更高的处理器，1 GB 内存（在虚拟机运行时为 1.5 GB），5 GB 可用磁盘空间，100 MB 可用磁盘空间（语言包），5400 转硬盘、支持 1024 x768 或更高分辨率的 DirectX 显卡。
* 如果您计划在虚拟环境中安装 `Visual Studio 2012`，应考虑使用 Hyper-V 并确保满足以下最低硬件要求：x64 基处理器（包含硬件辅助虚拟化 AMD-V 或 Intel VT 以及硬件数据执行保护）；4 GB 内存（建议更多）；网卡；显卡；DVD-ROM 驱动器以及至少 100 GB 的可用磁盘空间用于存储多个虚拟机。

# 书中的约定

本书使用以下约定呈现信息，以使信息易于阅读和遵循：

* 每个练习由一系列任务组成，以编号步骤的形式列出，列出完成练习必须采取的每个操作。
* 带有“注意”等标签的框元素提供了额外信息或成功完成步骤的替代方法。
* 带有考试提示标签的框元素提供了额外信息，可能提供有用的提示或有关考试预期内容的额外信息。
* 您输入的文本（代码块除外）以加粗形式显示。
* 两个键名之间的加号 (+) 意味着必须同时按下这些按键。例如，“按下 Alt+Tab”意味着您在按住 Alt 键的同时按下 Tab 键。





*   两个或多个菜单项之间的垂直线（例如，File | Close）意味着你应该先选择第一个菜单或菜单项，然后是下一个，依此类推。

# 致谢

我想感谢以下人员：

* 感谢 Jeff Riley 为我提供编写这本书的机会。
* 感谢 Ginny Munroe 帮助我完成了整个编辑过程。我从你的反馈和建议中汲益了很多知识。
* 感谢 Auri Rahimzadeh 提供的技术评审技能。
* 感谢我的妻子 Elise 的支持。

还要感谢所有其他在本书准备过程中发挥过作用的人。感谢你们的辛勤工作！

# 勘误与书籍支持

我们已尽一切努力确保本书及其配套内容的准确性。自本书出版以来，报告的任何错误都已列在我们位于 oreilly.com 的 Microsoft Press 网站上：

*[`aka.ms/ER70-483/errata`](http://aka.ms/ER70-483/errata)

如果您发现了未列出的错误，可以通过同一页面向我们提交报告。

如果您需要额外的支持，请发送电子邮件至 `mspinput@microsoft.com`。

请注意，上述地址不提供 Microsoft 软件的产品支持。

# 我们希望听取您的意见

在 Microsoft Press，您的满意度是我们的首要任务，您的反馈是我们最宝贵的资产。请通过以下链接告诉我们您对这本书的看法：

*[`www.microsoft.com/learning/booksurvey`](http://www.microsoft.com/learning/booksurvey)

调查非常短，我们会阅读您的每一条评论和想法。提前感谢参与！

# 保持联系

让我们继续交流吧！可以在 Twitter 上关注我们：`[`twitter.com/MicrosoftPress`](http://twitter.com/MicrosoftPress)`。

# 准备考试

Microsoft 认证考试是建立简历的绝佳方式，也能让世界了解您的专业水平。认证考试验证了您的工作经验和产品知识。虽然工作经验无法被替代，但通过学习和实际操作进行准备可以帮助您应对考试。我们建议您结合使用现有的学习材料和课程来完善您的备考计划。例如，您可以使用本 `Exam Ref` 和另一本学习指南进行“在家”备考，并参加 Microsoft 官方课程以获得课堂体验。请选择您认为最适合您的组合。

请注意，本 `Exam Ref` 是基于关于考试的公开信息以及作者的经验。为了确保考试的完整性，作者无法接触真实的考试内容。

# 第 1 章 管理程序流

如果您只能构建从上到下执行所有逻辑的程序，那么构建复杂的应用程序将是不可能的。幸运的是，`C#` 和 `.NET Framework` 为您提供了许多选项来创建没有固定程序的复杂程序。

本章从研究如何创建 `multithreaded`（多线程）应用程序开始。这些应用程序具有良好的扩展性，并在执行工作的同时能够保持对用户的响应。您还将学习添加到 `C#` 5 中的新语言特性 `async/await`。

## 重要提示

您读过 准备考试 吗？

它其中包含了关于通过考试所需技能的宝贵信息。

您将学习基础的 `C#` 语言结构，用于根据情况做出决策并多次执行代码。这些结构构成了每个应用程序的基础语言块，您将经常使用它们。

之后，您将学习如何使用 `delegates`（委托）和 `events`（事件）创建松耦合的应用程序。通过事件，您可以构建在发生某些事情时相互通知并对这些通知做出响应的对象。诸如 `ASP.NET`、`Windows Presentation Foundation (WPF)` 和 `WinForms` 等框架大量使用了事件；彻底理解事件将帮助您构建出色的应用程序。

遗憾的是，您的程序流也可能被错误中断。此类错误可能发生在您无法控制但需要响应的区域。有时您可能想自己抛出此类错误。您将学习异常（exceptions）如何帮助您在应用程序中实现健壮的错误处理策略。

## 本章目标：

* 目标 1.1: 实现多线程和异步处理
* 目标 1.2: 管理多线程
* 目标 1.3: 实现程序流
* 目标 1.4: 创建并实现事件和回调
* 目标 1.5: 实现异常处理

## 目标 1.1: 实现多线程和异步处理

随着用户期望的提高，应用程序变得日益复杂。为了充分利用多核系统并保持响应，您需要创建使用多个线程的应用程序，这通常被称为 `parallelism`（并行）。

`.NET Framework` 和 `C#` 语言提供了许多选项供您创建多线程应用程序。

本目标涵盖了如何：

* 理解线程。
* 使用任务库（Task Library）。
* 使用 `Parallel` 类。
* 使用 `async` 和 `await` 关键字。
* 使用并行集成查询（Parallel LINQ）。
* 使用并发集合。

## 理解线程

假设您的计算机只有一个 `central processing unit`（中央处理器，CPU），且它一次只能执行一个操作。现在，想象一下如果 CPU 必须努力执行一个耗时很的任务会发生什么。

当该操作运行时，所有其他操作都将暂停。这意味着整个机器将死机并对用户没有响应。当该长时间运行的操作包含一个永远不会结束的错误时，情况更加糟糕。因为机器的其他部分无法使用，您只能重启机器。

为了解决这个问题，使用了 `thread`（线程）的概念。在当前的 Windows 版本中，每个应用程序运行在自己的 `process`（进程）中。进程通过为应用程序提供独立的 `virtual memory`（虚拟内存）并确保不同进程互不影响来隔离应用程序。每个进程运行在自己的 `thread` 中。线程 就像是虚拟化的 CPU。如果应用程序崩溃或陷入无限循环，只有该应用程序进程受到影响。

Windows 必须管理所有线程以确保它们能够完成工作。这些管理任务会产生开销。Windows 允许线程执行一段时间。当这段时间结束，线程会被暂停并切换到另一个线程。这被称为 `context switching`（上下文切换）。




尽管会有某些性能损耗，但使用线程确实可以确保每个进程都能获得执行时间，而无需等待所有其他操作完成。这提高了系统的响应能力，并产生一种一个 CPU 可以同时执行多个任务的错觉。通过这种方式，你可以创建一个使用 `parallelism`（并行）的应用程序，这意味着它可以在不同的 CPU 上并行执行多个线程。

你今天购买的几乎任何设备都拥有多核心的 CPU，这类似于拥有多个 CPU。某些服务器不仅有多核 CPU，而且还有多个 CPU。为了利用所有这些核心，你需要多个线程。Windows 会确保这些线程分发在你可用的核心上。通过这种方式，你可以同时执行多个任务并提高可扩展性。

由于与线程相关的开销，你应该仔细判断是否需要多线程。但如果你想使用线程来提高可扩展性或响应速度，C# 和 `.NET Framework` 为你提供了许多可能性。

### 使用 `Thread` 类

`Thread` 类可以在 `System.Threading` 命名空间中找到。该类允许你创建新线程、管理它们的优先级并获取它们的状态。

除非你有特殊需求，否则你不应该在应用程序中使用 `Thread` 类。然而，当使用 `Thread` 类时，你可以控制所有的配置选项。例如，你可以指定线程的优先级，告诉 Windows 你的线程是长时间运行的，或者配置其他高级选项。

示例 1-1 显示了使用 `Thread` 类在另一个线程上运行方法的示例。`Console` 类为你同步了输出流的使用，因此你可以从多个线程向其写入内容。`Synchronization`（同步）是确保两个线程不会同时执行程序特定部分的机制。在控制台应用程序中，这意味着没有两个线程可以在同一时刻向屏幕写入数据。如果一个线程正在处理输出流，其他线程必须在它完成之前等待。

示例 1-1. 使用 `Thread` 类创建线程

```csharp
using System;
using System.Threading;

namespace Chapter1
{
    public static class Program
    {
        public static void ThreadMethod()
        {
            for (int i = 0; i < 10; i++)
            {
                Console.WriteLine("ThreadProc: {0}", i);
                Thread.Sleep(0);
            }
        }

        public static void Main()
        {
            Thread t = new Thread(new ThreadStart(ThreadMethod));
            t.Start();

            for (int i = 0; i < 4; i++)
            {
                Console.WriteLine("Main thread: Do some work.");
                Thread.Sleep(0);
            }

            t.Join();

        }

    }
}

// Displays
//Main thread: Do some work.
//ThreadProc: 0
//Main thread: Do some work.
//ThreadProc: 1
//Main thread: Do some work.
//ThreadProc: 2
//Main thread: Do some work.
//ThreadProc: 3
//ThreadProc: 4
//ThreadProc: 5
//ThreadProc: 6
//ThreadProc: 7
//ThreadProc: 8
//ThreadProc: 9
//ThreadProc: 10
```

如你所示，两个线程都在运行并将它们的消息打印到控制台。在主线程上调用了 `Thread.Join` 方法，让它等待直到另一个线程完成。

为什么要使用 `Thread.Sleep(0)`？它被用于向 Windows 信号该线程已完成。它不会等待整个线程的时间片结束，而是会立即切换到另一个线程。

你的进程和线程都有一个 `priority`（优先级）。分配低优先级对于像屏幕保护程序之类的应用程序是有用的。此类应用程序不与其他与其他竞争 CPU 时间。只有在绝对必要时才使用高优先级线程。新线程被分配的优先级为 `Normal`，这对于几乎所有场景都是可以的。

关于线程的另一个重要点是 `foreground`（前台）线程和 `background`（后台）线程的区别。前台线程可以保持应用程序运行。只有当所有前台线程结束时，公共语言运行时 (`CLR`) 才会关闭你的应用程序。随后后台线程会被终止。

示例 1-2 显示了这种差异。

示例 1-2. 使用后台线程

```csharp
using System;
using System.Threading;

namespace Chapter1
{
    public static class Program
    {
        public static void ThreadMethod()
        {
            for (int i = 0; i < 10; i++)
            {
                Console.WriteLine("ThreadProc: {0}", i);
                Thread.Sleep(1000);
            }
        }

        public static void Main()
        {
            Thread t = new Thread(new ThreadStart(ThreadMethod));
            t.IsBackground = true;
            t.Start();
        }
    }
}
```

如果你将 `IsBackground` 属性设置为 `true` 并运行此应用程序，应用程序将立即退出。如果你将其设置为 `false`（创建一个前台线程），应用程序将打印 10 次 `ThreadProc` 消息。

`Thread` 构造函数还有另一个重载，接受一个 `ParameterizedStart` 委托的实例。如果你想通过启动方法向你的工作方法传递某些数据，可以使用此重载，如示例 1-3 所示。

示例 1-3. 使用 `ParameterizedStart`

```csharp
public static void ThreadMethod(object o)
{
    for (int i = 0; i < (int)o; i++)
    {
        Console.WriteLine("ThreadProc: {0}", i);
        Thread.Sleep(0);
    }
}

public static void Main()
{
    Thread t = new Thread(new ParameterizedStart(ThreadMethod));
    t.Start(5);
    t.Join();
}
```

在这种情况下，值 `5` 作为对象传递给 `ThreadMethod`。你可以将其强制转换为预期的类型以便在方法中使用。

要停止线程，可以使用 `Thread.Abort` 方法。然而，由于该方法是由另一个线程执行的，它可以随时时候发生。当它发生时，目标线程上会抛出 `ThreadAbortException`。这可能会导致状态损坏并使你的应用程序无法使用。

停止线程更好的方法是使用目标线程和调用线程都可以访问的共享变量。示例 1-4 显示了一个示例。

示例 1-4. 停止线程

```csharp
using System;
using System.Threading;

namespace Chapter1
{
    public static class Program
    {
        public static void ThreadMethod(object o)
        {
            for (int i = 0; i < (int)o; i++)
            {
                Console.WriteLine("ThreadProc: {0}", i);
                Thread.Sleep(0);
            }
        }

        public static void Main()
        {
            bool stopped = false;

            Thread t = new Thread(new ThreadStart(() => 
            {                
                while (!stopped)
                {
                    Console.WriteLine("Running...");
                    Thread.Sleep(1000);
                }
            }));

            t.Start();
            Console.WriteLine("Press any key to exit");
            Console.ReadKey();

            stopped  = true;
            t.Join();
        }
    }
}
```

在这种情况下，线程使用 Lambda 表达式初始化（这反过来只是委托的简写形式）。线程在 `stopped` 变为 `true` 之前一直运行。之后，`t.Join` 方法导致控制台应用程序等待直到线程完成执行。



每个线程都有自己的调用栈，其中存储了所有执行的方法。局部变量存储在调用栈上，并且对线程是私有的。

线程也可以拥有自己的非局部变量数据。通过对字段标记 `ThreadStatic` 属性，每个线程都会获得该字段的独立份（（参见示例 1-5）。

### 示例 1-5. 使用 `ThreadStaticAttribute`

```csharp
using System;
using System.Threading;

namespace Chapter1
{
    public static class Program
    {
        [ThreadStatic]
        public static int _field;
        public static void Main()
        {
            new Thread(() =>
               { 
                    for(int x = 0; x < 10; x++)
                    {
                        _field++;
                        Console.WriteLine("Thread A: {0}", _field);
                    }
                }).Start();

            new Thread(() =>
                { 
                    for(int x = 0; x < 10; x++)
                    {
                        _field++;
                        Console.WriteLine("Thread B: {0}", _field);
                    }
                }).Start();

            Console.ReadKey();
        }
    }
}
```

应用 `ThreadStaticAttribute` 后，`_field` 的最大值变为 `10`。如果你将其移除，你会发现两个线程访问的是同一个值，且该值会变为 `20`。

如果你想在线程中使用本地数据并为每个线程进行初始化，可以使用 `ThreadLocal<T>` 类。该类接收一个用于初始化值的方法委托（delegate）。示例 1-6）展示了一个示例。

### 示例 1-6. 使用 `ThreadLocal<T>`

```csharp
using System;
using System.Threading;

namespace Chapter1
{
    public static class Program
    {
        public static ThreadLocal<int> _field = 
            new ThreadLocal<int>(() => 
            {
                return Thread.CurrentThread.ManagedThreadId;

            });

        public static void Main()
        {
            new Thread(() =>
                { 
                    for(int x = 0; x < _field.Value; x++)
                    {
                        Console.WriteLine("Thread A: {0}", x);
                    }

                }).Start();
            new Thread(() =>
                {
                    for (int x = 0; x < _field.Value; x++)
                    {
                        Console.WriteLine("Thread B: {0}", x);
                    }
                }).Start();

            Console.ReadKey();
        }
    }
}

// Displays
// Thread B: 0
// Thread B: 1
// Thread B: 2
// Thread B: 3
// Thread A: 0
// Thread A: 1
// Thread A: 2
```

在这里你看到了 .NET Framework 的另一个特性。你可以使用 `Thread.CurrentThread` 类来获取正在执行的线程的信息。这被称为线程的`执行上下文`（execution context）。该属性允许你访问许多属性，例如线程的`当前文化`（current culture，与当前线程关联的 `CultureInfo`，用于格式化日期、时间、数字、货币值、文本排序顺序、大小写约定和字符串比较）、`主节点`（principal，代表当前的安全上下文）、`优先级`（priority，指示操作系统如何调度线程的值）以及其他信息。

当创建一个线程时，运行时环境会确保启动线程的执行上下文流到新线程。这样，新线程就拥有与父线程相同的权限。

然而，这种数据的复制会消耗一些资源。如果你不需要这些数据，可以通过 `ExecutionContext.SuppressFlow` 方法禁用此行为。

### 线程池

当直接与 `Thread` 类工作时，你每次都会创建一个新线程，并在完成工作后该线程就会死亡。然而，线程的创建是需要花费时间和资源的。

创建一个`线程池` 是为了重用这些线程，类似于数据库连接池的工作方式。与其让线程死亡，不如将其发送回池中，以便在请求进入时可以被重用。

当你使用 .NET 中的线程池工作时，你队列一个工作项（work item），该工作项会被池中的可用线程提取。示例 1-7 展示了如何实现这一点。

### 示例 1-7. 向线程池队列某些工作

```csharp
using System;
using System.Threading;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            ThreadPool.QueueUserWorkItem((s) =>
            {
                Console.WriteLine("Working on a thread from threadpool");
            });

            Console.ReadLine();
        }
    }
}
```

由于线程池限制了可用线程的数量，因此你获得的并行程度确实比使用普通的 `Thread` 类要低。但线程池也有许多优势。

例如，一个处理传入请求的 Web 服务器。所有这些请求都在未知的时间和频率进入。线程池的创建是为了重用这些线程……与其让线程死亡，不如将其发送回池中……（此处此处重复逻辑）……当你与 .NET 线程池工作时，你队列一个工作项，该工作项会被池中的可用线程提取……由于线程池限制了可用线程的数量，因此你获得的并行程度确实比使用普通的 `Thread` 类要低。但线程池也有许多优势。

例如，一个处理传入请求的 Web 服务器。所有这些请求都在未知的时间和频率进入。线程池的创建是为了重用这些线程，类似于数据库连接池的工作方式。与其让线程死亡，不如将其发送回池中，以便在请求进入时可以被重用。

当你与 .NET 线程池工作时，你队列一个工作项，该工作项会被池中的可用线程提取。示例 1-7）展示了如何实现这一点。

由于线程池限制了可用线程的数量，因此你获得的并行程度确实比使用普通的 `Thread` 类要低。但线程池也有许多优势。

例如，一个处理传入请求的 Web 服务器。所有这些请求都在未知的时间和频率进入。线程池的创建是为了重用这些线程，类似于数据库连接池的工作方式。与其让线程死亡，不如将其发送回池中，以便在请求进入时可以被重用。

当你与 .NET 线程池工作时，你队列一个工作项，该工作项会被池中的可用线程提取。示例 1-7）展示了如何实现这一点。

由于线程池限制了可用线程的数量，因此你获得的并行程度确实比使用普通的 `Thread` 类要低。但线程池也有许多优势。

例如，一个处理传入请求的 Web 服务器。所有这些请求都在未知的时间和频率进入。线程池的创建是为了重用这些线程，类似于数据库连接池的工作方式。与其让线程死亡，不如将其发送回池中，以便在请求进入时可以被重用。

当你与 .NET 线程池工作时，你队列一个工作项，该工作项会被池中的可用线程提取。示例 1-7）展示了如何实现这一点。

由于线程池限制了可用线程的数量，因此你获得的并行程度确实比使用普通的 `Thread` 类要低。但线程池也有许多优势。

例如，一个处理传入请求的 Web 服务器。所有这些请求都在未知的时间和频率进入。线程池的创建是为了重用这些线程，类似于数据库连接池的工作方式。与其让线程死亡，不如将其发送回池中，以便在请求进入时可以被重用。

当你与 .NET 线程池工作时，你队列一个工作项，该工作项会被池中的可用线程提取。示例 1-7）展示了如何实现这一点。

由于线程池限制了可用线程的数量，因此你获得的并行程度确实比使用普通的 `Thread` 类要低。但线程池也有许多优势。

例如，一个处理传入请求的 Web 服务器。所有这些请求都在未知的时间和频率进入。线程池的创建是为了重用这些线程……（注：原文后部分存在逻辑重复，翻译已按原文结构进行逻辑对齐）

线程池自动管理它维护的线程数量。当它被首次创建时，它是空的。当请求进入时，它会创建额外的线程。只要它能在新请求到来之前完成操作，就不需要创建新线程。如果线程一段时间后不再使用，线程池可以杀死这些线程以便它们不再消耗资源。

### 更多信息：线程池

有关线程池如何工作以及你如何配置它的更多信息，请参阅 [`msdn.microsoft.com/en-us/library/system.threading.threadpool.aspx`](http://msdn.microsoft.com/en-us/library/system.threading.threadpool.aspx)。

需要注意的是，由于线程被重用，它们也会重用本地状态。你可能无法依赖多个操作之间共享的状态。

## 使用 Task

向线程池队列工作项可能有用，但它也有其局限性。没有内置方法可以知道操作何时完成以及返回值是什么。

这就是为什么 .NET Framework 引入了 `Task` 概念，它是一个代表应该执行的工作的对象。`Task` 可以告诉你工作是否已完成，如果操作返回结果，`Task` 会给你提供该结果。

`任务调度器`（task scheduler）负责启动并管理 `Task`。默认情况下，任务调度器使用线程池中的线程来执行 `Task`。

*Task 可以用来提高应用程序的响应能力。如果管理用户界面的线程将工作卸载到线程池中的另一个线程，它可以继续处理用户事件并确保应用程序仍然可用。但这并不能帮助扩展性。如果一个线程接收到 Web 请求并启动一个新的 *Task*，它只会从线程池中消耗另一个线程，而原始线程在等待结果。*





在另一个线程上执行 `Task` 只有在你想要保持用户界面线程空闲以处理其他工作，或者想要将工作并行化到多个处理器上时才有意义的。

示例 1-8 显示了如何启动一个新的 `Task` 并等待它完成。

### 示例 1-8. 启动一个新的 `Task`

```c
using System;
using System.Threading.Tasks;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            Task t = Task.Run(() =>
            {
                for (int x = 0; x < 100; x++)
                {
                    Console.Write('*');
                }
            });

            t.Wait();
        }
    }
}
```

此示例创建了一个新的 `Task` 并立即启动它。调用 `Wait` 等同于在线程上调用 `Join`。它会在退出应用程序之前等待 `Task` 完成。

除了 `Task` 之外，.NET Framework 还有 `Task<T>` 类，如果 `Task` 需要返回一个值，你就可以使用它。示例 1-9 显示了它是如何工作的。

### 示例 1-9. 使用返回返回的 `Task`。

```csharp
using System;
using System.Threading.Tasks;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            Task<int> t = Task.Run(() =>
            {
                return 42;
            });
            Console.WriteLine(t.Result); // 显示 42
        }
    }
}
```

尝试在 `Task` 上读取 `Result` 属性将强制尝试读取结果的线程等待直到 `Task` 完成后继续。只要 `Task` 尚未完成，就不可能提供结果。如果 `Task` 未完成，此调用将阻塞当前线程。

由于 `Task` 对象的面向对象特性，你可以做的一件事是添加一个“延续任务”（continuation task）。这意味着你希望在 `Task` 完成后执行另一个操作。

示例 1-10 显示了创建此类延续的示例。

### 示例 1-10. 添加延续

```csharp
Task<int> t = Task.Run(() =>
{
    return 42;
}).ContinueWith((i) =>
{
    return i.Result * 2;
});

Console.WriteLine(t.Result); // 显示 84
```

`ContinueWith` 方法有几个重载，你可以使用它们来配置延续何时运行。通过这种方式，你可以添加不同的延续方法，它们会在异常发生、`Task` 被取消或 `Task` 成功完成时运行。示例 1-11 显示了如何执行。

### 示例 1-11. 调度不同的延续任务

```csharp
Task<int> t = Task.Run(() =>
{
    return 42;
});

t.ContinueWith((i) =>
{
    Console.WriteLine("Canceled");
}, TaskContinuationOptions.OnlyOnCanceled);

t.ContinueWith((i) =>
{
    Console.WriteLine("Faulted");
}, TaskContinuationOptions.OnlyOnFaulted);

var completedTask = t.ContinueWith((i) =>
 {
     Console.WriteLine("Completed");
 }, TaskContinuationOptions.OnlyOnRanToCompletion);

completedTask.Wait();
```

除了延续 `Tasks` 之外，`Task` 还可以有几个“子 `Tasks`”。当所有子任务就绪时，父 `Task` 就会完成。示例 1-12 显示了它是如何工作的。

### 示例 1-12. 将子任务附加到父任务

```csharp
using System;
using System.Threading.Tasks;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            Task<Int32[]> parent = Task.Run(() =>
            {
                var results = new Int32[3];
                new Task(() => results[0] = 0, 
                    TaskCreationOptions.AttachedToParent).Start();
                new Task(() => results[1] = 1, 
                    TaskCreationOptions.AttachedToParent).Start();
                new Task(() => results[2] = 2, 
                    TaskCreationOptions.AttachedToParent).Start();

                return results;
            });

            var finalTask = parent.ContinueWith(
               parentTask => {
                   foreach(int i in parentTask.Result)
                       Console.WriteLine(i);
               });

            finalTask.Wait();
        }
    }
}
```

`finalTask` 只有在 `parent` 完成后才会运行，当所有子任务完成后，`parent` 就会完成。在上一个示例中，你可以使用 `TaskFactory` 创建带有不同选项的 `Tasks`。为了让过程变得简单，可以使用 `TaskFactory`。`TaskFactory` 是根据配置创建的，然后可以用于创建带有该配置的 `Tasks`。示例 1-13 显示了如何简化之前的示例。

### 示例 1-13. 使用 `TaskFactory`

```csharp
using System;
using System.Threading;
using System.Threading.Tasks;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            Task[] tasks = new Task[3];

            tasks[0] = Task.Run(() => { 
                                          Thread.Sleep(1000); 
                                          Console.WriteLine("1");
                                          return 1; 
                                      });
            tasks[1] = Task.Run(() => {  
                                          Thread.Sleep(1000); 
                                          Console.WriteLine("2"); 
                                          return 2; 
                                      });
            tasks[2] = Task.Run(() => { 
                                          Thread.Sleep(1000); 
                                          Console.WriteLine("3");
                                          return 3; }
                                      );

           Task.WaitAll(tasks);
        }
    }
}
```

除了在单个 `Task` 上调用 `Wait` 之外，你还可以使用 `WaitAll` 方法等待多个 `Tasks` 完成后再继续执行。在这种情况下，所有三个 `Tasks` 同时执行，整个运行时间大约为 1000ms，而不是 3000ms。除了 `WaitAll` 之外，你还有一个 `WhenAll` 方法，你可以用它在所有 `Tasks` 完成后调度一个延续方法。

与其等待所有任务完成，你也可以也可以等待其中一个任务完成。你使用 `WaitAny` 方法来实现这一点。示例 1-15 显示了它是如何工作的。





### 示例 1-15. 使用 `Task.WaitAny`

```csharp
using System;
using System.Linq;
using System.Threading;
using System.Threading.Tasks;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            Task<int>[] tasks = new Task<int>[3];

            tasks[0] = Task.Run(() => { Thread.Sleep(2000); return 1; });
            tasks[1] = Task.Run(() => { Thread.Sleep(1000); return 2; });
            tasks[2] = Task.Run(() => { Thread.Sleep(3000); return 3; });

            while (tasks.Length > 0)
            {
                int i = Task.WaitAny(tasks);
                Task<int> completedTask = tasks[i];

                Console.WriteLine(completedTask.Result);

                var temp = tasks.ToList();
                temp.RemoveAt(i);
                tasks = temp.ToArray();

            }
        }
    }
}
```

在这个示例中，一旦某个 `Task` 完成，你就会对其进行处理。通过跟踪哪些 `Tasks` 已经完成，你不需要等待所有 `Tasks` 都完成。

## 使用 `Parallel` 类

`System.Threading.Tasks` 命名空间还包含了另一个用于并行处理的类。`Parallel` 类有几个静态方法——`For`、`ForEach` 和 `Invoke`——你可以使用它们来并行化工作。

`并行性` 涉及采取某个任务并将其分解为可以并发执行的相关任务。这意味着你不应该遍历代码并将所有的循环替换为并行循环。只有当你的代码不需要顺序执行时，才应该使用 `Parallel` 类。

只有当你有大量可以并行执行的工作需要完成时，并行处理才能提高性能。对于较小的工作集或必须同步访问资源的工作，使用 `Parallel` 类可能会损害性能。

了解它在你的情况下是否有效的最优方法是测量结果。

[示例 1-16] 显示了使用 `Parallel.For` 和 `Parallel.ForEach` 的示例。

### 示例 1-16. 使用 `Parallel.For` 和 `Parallel.ForEach`

```csharp
Parallel.For(0, 10, i =>
{
    Thread.Sleep(1000);
});

var numbers = Enumerable.Range(0, 10);
Parallel.ForEach(numbers, i =>
{
    Thread.Sleep(1000);
});
```

你可以通过 `ParallelLoopState` 对象来取消循环。你有两种方法来实现：`Break` 或 `Stop`。`Break` 确保所有正在运行的迭代将完成。`Stop` 则直接终止一切。[示例 1-17] 显示了一个示例。

### 示例 1-17. 使用 `Parallel.Break`

```csharp
ParallelLoopResult result = Parallel.
    For(0, 1000, (int i, ParallelLoopState loopState) =>
{
    if (i == 500)
    {
          Console.WriteLine("Breaking loop");
       loopState.Break();

 }
    return;
});
```

当跳出并行循环时，`result` 变量的 `IsCompleted` 值为 `false`，且 `LowestBreakIteration` 值为 `500`。当你使用 `Stop` 方法时，`LowestBreakIteration` 为 `null`。

## 使用 `async` 和 `await`

正如你所看到的，长时间的 CPU 密集型任务可以通过 `Task` 对象交给另一个线程。但在处理输入/输出（I/O）密集型工作时，情况会有所不同。

当你的应用程序在主应用程序线程上执行 I/O 操作时，Windows 注意到你的线程正在等待 I/O 操作完成。你可能正在访问磁盘或网络上的某些文件，这可能需要一些时间。

正因如此，Windows 会暂停你的线程，使其不占用任何 CPU 资源。在此期间，它仍然占用内存，且该线程无法用于处理其他请求，反过来会导致在新请求进入时创建新线程。

异步代码解决了这个问题。你不再阻塞线程直到 I/O 操作完成，而是获得一个表示异步操作结果的 `Task` 对象。通过在该 `Task` 上设置延续任务，你可以在 I/O 完成后继续执行。在此期间，你的线程可以用于其他工作。当 I/O 操作完成时，Windows 通知运行时，延续的 `Task` 被调度到线程池上。

但编写异步代码并不容易。你必须确保处理了所有边界情况，并确保不会出错。由于这种困境，C# 5 增加了两个新关键字来简化异步代码的编写。这两个关键字是 `async` 和 `await`。

你使用 `async` 关键字标记一个用于异步操作的方法。通过这样，你向编译器信号将发生异步操作。`async` 关键字允许你编写看起来像同步但行为上是异步的代码。`await` 关键字允许编译器将你的代码转换为`状态机`。

手动编写正确的异步代码是非常困难的，特别是在尝试实现异常处理时。添加延续任务也会破坏代码的逻辑流。你的代码不再是从上到下读取的。[示例 1-18] 显示了一个异步方法的简单示例。

### 示例 1-18. 使用 `async` 和 `await`

```csharp
using System;
using System.Net.Http;
using System.Threading.Tasks;

namespace Chapter1.Threads
{
    public static class Program
    {
        public static void Main()
        {
            string result = DownloadContent().Result;
            Console.WriteLine(result);
        }

        public static async Task<string> DownloadContent()
        {
            using(HttpClient client = new HttpClient())
            {

                string result = await client.GetStringAsync("http://www.microsoft.com");
                return result;
            }
        }
    }
}
```



如果你正在构建一个在后台操作运行时仍需保持响应的客户端应用程序，可以使用 `await` 关键字将耗时操作卸载到另一个线程。虽然这不会提高性能，但它确实可以提高响应能力。`await` 关键字还能确保你的方法的剩余部分在正确的用户界面线程上运行，这样你就可以更新用户界面。

创建一个使用更少线程的可扩展性应用程序是另一回事。提高代码的可扩展性性关于更改代码的实际实现方式。示例 1-19 展示了此类示例。

### 示例 1-19. 可扩展性与响应性

```c
public Task SleepAsyncA(int millisecondsTimeout)
{
    return Task.Run(() => Thread.Sleep(millisecondsTimeout));
}

public Task SleepAsyncB(int millisecondsTimeout)
{
    TaskCompletionSource<bool> tcs = null;
    var t = new Timer(delegate { tcs.TrySetResult(true); }, null, -1, -1);
    tcs = new TaskCompletionSource<bool>(t);
    t.Change(millisecondsTimeout, -1);
    return tcs.Task;
}
```

`SleepAsyncA` 方法在睡眠时使用了线程池中的线程。然而，第二个方法具有完全不同的实现，在等待计时器运行时不会占用线程。第二个方法为你提供了可扩展性。

在使用 `async` 和 `await` 关键字时，你应该记住这一点。仅仅将每个操作都封装在任务中并等待它们不会让你的应用程序性能变得更好。然而，它可能提高响应能力，这在客户端应用程序中是非常重要的。

例如，`FileStream` 类暴露了如 `WriteAsync` 和 `ReadAsync` 等异步方法。它们使用了利用实际异步 I/O 的实现。通过这种方式，它们在等待系统硬盘读取或写入某些数据时，不会使用线程。

当异步方法中发生异常时，你通常会预期得到一个 `AggregateException`。然而，生成的代码会帮助你解开 `AggregateException` 并抛出其内部异常中的第一个。这使得代码使用更加直观且易于调试。

在处理异步代码时，另一个重要的点是 `SynchronizationContext`（同步上下文）的概念，它将其应用程序模型与其线程模型连接起来。例如，WPF 应用程序使用单个用户界面线程和可能的多个后台线程来提高响应能力并将工作分发到多个 CPU 上。然而，ASP.NET 应用程序使用线程池中的线程，这些线程使用正确的数据（如当前用户和文化）初始化以处理传入的请求。

`SynchronizationContext` 抽象了这些不同应用程序的工作方式，并确保你在需要更新 UI 上的或处理网络请求时位于正确的线程上。

`await` 关键字确保在任务完成时保存并恢复当前的 `SynchronizationContext`。在 WPF 应用程序中使用 `await` 时，这意味着在你的 `Task` 完成后，你的程序将在用户界面线程上继续运行。在 ASP.NET 应用程序中，剩余代码将在设置了客户端文化、主体和其他信息的线程上运行。

如果你愿意，可以禁用 `SynchronizationContext` 的流。也许你的后续执行代码可以在任何线程上运行，因为它在完成后不需要更新 UI。通过禁用 `SynchronizationContext`，你的代码运行得更好。示例 1-20 展示了一个 WPF 应用程序中的按钮事件处理程序，该程序下载网站并将结果放在标签中。

### 示例 1-20. 使用 ConfigureAwait

```csharp
private async void Button_Click(object sender, RoutedEventArgs e)
{
    HttpClient httpClient = new HttpClient();

    string content = await httpClient
        .GetStringAsync("http://www.microsoft.com")
        .ConfigureAwait(false);

    Output.Content = content;
}
```

此示例会抛出一个异常；由于 `ConfigureAwait(false)`，`Output.Content` 那一行不在 UI 线程上执行。如果你执行其他操作（例如将内容写入文件），则就不需要设置 `SynchronizationContext`（参见 示例 1-21）。

### 示例 1-21. 在线程池而非 UI 线程上继续

```csharp
private async void Button_Click(object sender, RoutedEventArgs e)
{
    HttpClient httpClient = new HttpClient();

    string content = await httpClient
        .GetStringAsync("http://www.microsoft.com")
        .ConfigureAwait(false);

    using (FileStream sourceStream = new FileStream("temp.html",
            FileMode.Create, FileAccess.Write, FileShare.None, 
            4096, useAsync: true))
    {
        byte[] encodedText = Encoding.Unicode.GetBytes(content);
        await sourceStream.WriteAsync(encodedText, 0, encodedText.Length)
            .ConfigureAwait(false);
    };
}
```

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

两个 `await` 都使用了 `ConfigureAwait(false)` 方法，因为如果第一个方法在 `awaiter` 检查之前已经完成，代码仍然会在 UI 线程上运行。

等待，`async` 和 `await` 关键字的使用让编写异步代码变得容易得多。在当今多核且对响应性要求的世界上，寻找使用这些关键字的机会是非常。

### 考试提示

在使用 `async` 和 `await` 时，请记住，你不应该有一个标记为 `async` 但内部没有任何 `await` 语句的方法。除非是事件处理程序，否则应避免从 `async` 方法返回 `void`。

## 使用语言集成查询 (PLINQ)

*语言集成查询* (LINQ) 是 C# 语言的一种流行扩展。你可以用它对所有类型的数据执行查询。

*并行语言集成查询* (PLINQ) 可以用于对象，潜在地将顺序查询转换为并行查询。

用于 PLINQ 的扩展方法定义在 `System.Linq.ParallelEnumerable` 类中。可以使用 LINQ 操作符的并行版本，如 `Where`、`Select`、`SelectMany`、`GroupBy`、`Join`、`OrderBy`、`Skip` 和 `Take`。

示例 1-22 展示了你如何将查询转换为并行查询。

### 示例 1-22. 使用 AsParallel

```csharp
var numbers = Enumerable.Range(0, 10000000);
var parallelResult = numbers.AsParallel()
    .Where(i => i % 2 == 0)
    .ToArray();
```

运行时决定将你的查询转换为并行查询是否有意义。这样做时，它生成 `Task` 对象并开始执行它们。如果你想强制 PLINQ 进入并行查询，可以使用 `WithExecutionMode` 方法并指定它始终并行执行查询。

你还可以使用 `WithDegreeOfParallelism` 方法限制使用的并行度。你向该方法传递一个表示你想要使用的处理器数量的整数。通常，PLINQ 使用所有处理器（最多 64 个），但你可以通过此方法进行限制。

需要记住的一点是，并行处理不保证任何特定的顺序。示例 1-23 展示了可能发生的情况。





### 示例 1-23. 无序并行查询

```assembly
using System;
using System.Linq;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            var numbers = Enumerable.Range(0, 10);
            var parallelResult = numbers.AsParallel()
                .Where(i => i % 2 == 0)
                .ToArray();

            foreach (int i in parallelResult)
                Console.WriteLine(i);
        }
    }
}

// 显示
// 2
// 0
// 4
// 6
// 8
```

如你所见，此查询返回的结果没有特定的顺序。这段代码的结果取决于可用 CPU 的数量。如果你想确保结果是有序的，可以添加 `AsOrdered` 操作符。你的查询仍然以并行方式处理，但结果会被缓冲并排序。示例 1-24 展示了它是如何工作的。

### 示例 1-24. 有序并行查询

```assembly
using System;
using System.Linq;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            var numbers = Enumerable.Range(0, 10);
            var parallelResult = numbers.AsParallel().AsOrdered()
                .Where(i => i % 2 == 0)
                .ToArray();

            foreach (int i in parallelResult)
                Console.WriteLine(i);
        }
    }
}

// 显示
// 0
// 2
// 4
// 6
// 8
```

如果你有一个复杂的查询，可以从并行处理中受益，但某些部分应该按顺序执行，你可以使用 `AsSequential` 来停止查询的并行处理。

需要这种要求的场景之一是保留查询的顺序。示例 1-25 展示了你如何使用 `AsSequential` 操作符来确保 `Take` 方法不会打乱你的顺序。

### 示例 1-25. 将并行查询顺序化

```assembly
var numbers = Enumerable.Range(0, 20);

var parallelResult = numbers.AsParallel().AsOrdered()
    .Where(i => i % 2 == 0).AsSequential();

foreach (int i in parallelResult.Take(5))
    Console.WriteLine(i);

// 显示
// 0
// 2
// 4
// 6
// 8
```

在使用 PLINQ 时，当迭代也可以以并行方式进行时，你可以使用 `ForAll` 操作符来遍历集合。示例 1-26 展示了如何这样做。

### 示例 1-26. 使用 ForAll

```assembly
var numbers = Enumerable.Range(0, 20);

var parallelResult = numbers.AsParallel()
    .Where(i => i % 2 == 0);

parallelResult.ForAll(e => Console.WriteLine(e));
```

与 `foreach` 相，`ForAll` 在开始执行之前不需要所有结果。但在本例中，`ForAll` 确实会移除任何指定的排序顺序。

当然，你的并行查询中的某些操作可能会抛出异常。.NET Framework 通过将所有异常聚合到一个 `AggregateException` 中来处理这个问题。此异常暴露了并行执行期间发生的所有异常的列表。示例 1-27 展示了你如何处理它。

### 示例 1-27. 捕获 AggregateException

```assembly
using System;
using System.Linq;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()

        {
            var numbers = Enumerable.Range(0, 20);

            try
            {

                var parallelResult = numbers.AsParallel()
                    .Where(i => IsEven(i));

                parallelResult.ForAll(e => Console.WriteLine(e));
            }
            catch (AggregateException e)
            {
                Console.WriteLine("There where {0} exceptions", 
                                    e.InnerExceptions.Count);
            }
        }

        public static bool IsEven(int i)
        {
            if (i % 10 == 0) throw new ArgumentException("i");

            return i % 2 == 0;
        }
    }
}

// 显示
// 4
// 6
// 8
// 2
// 12
// 14
// 16
// 18
// There where 2 exceptions
```

如你所见，在处理数据时发生了两个异常。你可以通过遍历 `InnerExceptions` 属性来检查这些异常。

## 使用并发集合

在多线程环境中工作时，你需要确保在没有同步访问的情况下没有同时操作共享数据。.NET Framework 提供了一些专门为并发环境而创建的集合类，这正是你在使用多线程时所拥有的。这些集合是线程安全的。这些集合包括：

* `BlockingCollection<T>`
* `ConcurrentBag<T>`
* `ConcurrentDictionary<TKey,T>`
* `ConcurrentQueue<T>`
* `ConcurrentStack<T>`

### BlockingCollection

该集合对于添加和移除是安全的。从集合中移除项可能会阻塞，直到数据可用。添加数据非常快，但你可以设置一个上限限制。如果达到限制，添加操作将阻塞调用线程，直到有空间。`BlockingCollection` 实际上是其他集合类型的封装。如果你不给它任何特定指令，它默认使用 `ConcurrentQueue`。普通集合在多线程场景中使用会崩溃，因为一个线程在移除项时另一个线程正在读取。示例 1-28 展示了使用 `BlockingCollection` 的示例。一个 `Task` 监听添加到集合中的项。如果没有可用项，它会阻塞。另一个 `Task` 向集合添加项。

### 示例 1-28. 使用 BlockingCollection<T>

```assembly
using System;
using System.Collections.Concurrent;
using System.Threading.Tasks;

namespace Chapter1
{
    public static class Program
    {
        public static void Main()
        {
            BlockingCollection<string> col = new BlockingCollection<string>();
            Task read = Task.Run(() =>
                {
                    while (true)
                    {
                        Console.WriteLine(col.Take());
                    }
                });

            Task write = Task.Run(() =>
                {
                    while (true)
                    {
                        string s = Console.ReadLine();
                        if (string.IsNullOrWhiteSpace(s)) break;
                        col.Add(s);
                    }
                });

            write.Wait();
        }
    }
}
```

程序在用户不输入任何数据时终止。在此之前，输入的每个字符串都由 `write Task` 添加并由 `read Task` 移除。

你可以使用 `CompleteAdding` 方法向 `BlockingCollection` 信号不再将添加更多项。如果其他线程正在等待新项，它们将不再被阻塞。

你甚至可以从 示例 1-28 中移除 `while(true)` 语句。通过使用 `GetConsumingEnumerable` 方法，你可以获得一个在找到新项之前阻塞的 `IEnumerable`。这样你就可以使用 `foreach` 遍历 `BlockingCollection`（参见 示例 1-29）。

### 示例 1-29. 使用 GetConsumingEnumerable on a BlockingCollection

```assembly
Task read = Task.Run(() =>
    {

        foreach (string v in col.GetConsumingEnumerable())
            Console.WriteLine(v);
    });
```




## 更多信息：IEnumerable

关于使用 `IEnumerable` 的更多信息，请参阅第 2 章。

## ConcurrentBag

`ConcurrentBag` 只是一个项目包。它允许重复且没有特定的顺序。重要的方法有 `Add`、`TryTake()` 和 `TryPeek()`。

示例 1-30 显示了如何使用 `ConcurrentBag`。

### 示例 1-30. 使用 `ConcurrentBag`

```csharp
ConcurrentBag<int> bag = new ConcurrentBag<int>();

bag.Add(42);
bag.Add(21);

int result;
if (bag.TryTake(out result)) 
    Console.WriteLine(result);

if (bag.TryPeek(out result))
    Console.WriteLine("There is a next item: {0}", result);
```

需要记住的一是，`TryPeek` 方法在多线程环境中并不有用。另一个线程可能会在你访问它之前就删除了该项目。

`ConcurrentBag` 也实现了 `IEnumerable<T>`，所以你可以对其进行迭代。此操作通过在开始迭代时创建集合的快照来确保线程安全，因此在你开始迭代后添加到集合中的项目将是不可见的。示例 1-31 在实践中展示了这一点。

### 示例 1-31. 遍历 `ConcurrentBag`

```csharp
ConcurrentBag<int> bag = new ConcurrentBag<int>();
Task.Run(() =>
{
    bag.Add(42);
    Thread.Sleep(1000);
    bag.Add(21);
});
Task.Run(() =>
{
    foreach (int i in bag)
        Console.WriteLine(i);
}).Wait();

// Displays
// 42
```

这段代码只显示了 `42`，因为另一个值是在迭代 bag 开始后添加的。

## ConcurrentStack 和 ConcurrentQueue

栈（Stack）是一个`后进先出`（LIFO）集合。队列（Queue）是一个`先进先出`（FIFO）集合。

`ConcurrentStack` 有两个重要方法：`Push()` 和 `TryPop()`。`Push` 用于向栈中添加项目；`TryPop()` 尝试从栈中获取一个项目。你永远无法确定栈上是否有项目，因为多个线程可能同时访问你的集合。

你还可以使用 `PushRange()` 和 `TryPopRange()` 同时添加和删除多个项目。当你枚举集合时，会拍摄一个快照。

示例 1-32 显示了这些方法是如何工作的。

### 示例 1-32. 使用 `ConcurrentStack`

```csharp
ConcurrentStack<int> stack = new ConcurrentStack<int>();

stack.Push(42);

int result;
if (stack.TryPop(out result))
    Console.WriteLine("Popped: {0}", result);

stack.PushRange(new int[] { 1, 2, 3 });

int[] values = new int[2];
stack.TryPopRange(values);

foreach (int i in values)
    Console.WriteLine(i);

// Popped: 42
// 3
// 2
```

`ConcurrentQueue` 提供了 `Enqueue()` 和 `TryDequeue()` 方法来向集合中添加和删除项目。它还有一个 `TryPeek()` 方法，并通过创建数据的快照来实现 `IEnumerable`。示例 1-33 显示了如何使用 `ConcurrentQueue`。

### 示例 1-33. 使用 `ConcurrentQueue`

```csharp
ConcurrentQueue<int> queue = new ConcurrentQueue<int>();
queue.Enqueue(42);

int result;
if (queue.TryDequeue(out result))
    Console.WriteLine("Dequeued: {0}", result);

// Dequeued: 42
```

## ConcurrentDictionary

`ConcurrentDictionary` 以线程安全的方式存储键值对。你可以使用方法来添加和删除项目，并在项目存在时对项目进行就地更新。

示例 1-34 显示了你可以在 `ConcurrentDictionary` 上使用的方法。

### 示例 1-34. 使用 `ConcurrentDictionary`

```csharp
var dict = new ConcurrentDictionary<string, int>();
if (dict.TryAdd("k1", 42))
{
    Console.WriteLine("Added");
}

if (dict.TryUpdate("k1", 21, 42))
{
    Console.WriteLine("42 updated to 21");
}

dict["k1"] = 42; // 无条件覆盖

int r1 = dict.AddOrUpdate("k1", 3, (s, i) => i * 2);
```




虽然多线程可以给你带来很多优势，但编写多线程应用程序并不是易事。当不同的线程访问某些共享数据时，可能会出现问题。当两个线程都尝试同时更改某些内容时，会发生什么？为了让这成功工作，同步资源至关重要。

本目标涵盖了如何：
* 同步资源。
* 取消运行时间长的任务。

## 同步资源

正如你所看到的，在 .NET 的 TPL 支持下，创建一个多线程应用程序是非常容易的。但当你使用多线程构建真实世界的应用程序时，当你想要从多个线程同时访问相同的数据时，就会遇到问题。示例 1-35 展示了一个可能出现问题的示例。

示例 1-35. 在多线程应用程序中访问共享数据

```
using System;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            int n = 0;

            var up = Task.Run(() =>
            {
                for (int i = 0; i < 1000000; i++)
                    n++;
            });

            for (int i = 0; i < 1000000; i++)
                n--;

            up.Wait();
            Console.WriteLine(n);
        }
    }
}
```

示例 1-35 的输出会是什么？答案是，这取决于情况。当你运行这个应用程序时，每次得到的输出都不同。变量 `n` 的递增和递减这个看似简单的操作，实际上包含了查找（检查 `n` 的值）以及对 `n` 进行加 1 或减 1。但如果第一个任务读取了值并加 1，而任务 2 正好读取了该值并减了 1 呢？这就是示例中发生的情况，这也是为什么你永远得不到预期的 `0` 输出。

这是因为该操作不是**原子性的**。它由发生在不同时刻的读取和写入操作组成。这就是为什么对你正在工作的数据访问需要同步，这样你才能可靠地预测你的数据是如何受到影响的。

同步共享数据的访问是非常重要的。C# 语言提供的一个特性是 `lock` 运算符，它是编译器翻译为对 `System.Thread.Monitor` 调用的某种语法糖。示例 1-36 展示了如何使用 `lock` 运算符来修复之前的示例。

示例 1-36. 使用 `lock` 关键字

```
using System;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            int n = 0;

            object _lock = new object();

            var up = Task.Run(() =>
            {

                for (int i = 0; i < 1000000; i++)
                    lock (_lock)
                        n++;
            });

            for (int i = 0; i < 1000000; i++)
                lock (_lock)
                    n--;

            up.Wait();
            Console.WriteLine(n);
        }
    }
}
```

在此更改之后，程序始终输出 `0`，因为现在对变量 `n` 的访问是同步的。

同步共享数据的访问是非常重要的。虽然对变量 `n` 的访问现在是同步的，但对你正在工作的数据访问仍然需要同步。

然而，不当访问可能会导致一个线程在等待另一个，这可能导致死锁。示例 1-37 展示了一个死锁。

示例 1-37. 创建死锁

```
using System;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            int n = 0;

            object _lock = new object();

            var up = Task.Run(() =>
            {

                for (int i = 0; i < 1000000; i++)
                {
                    lock (_lock)
                    {
                        n++;
                    }
                }
            });

            for (int i = 0; i < 1000000; i++)
            {
                lock (_lock)
                {
                    n--;
                }
            }

            up.Wait();
            Console.WriteLine(n);
        }
    }
}
```

在此更改之后，程序始终输出 `0`，因为对变量 `n` 的访问现在是同步的。

然而，不当访问可能会导致一个线程在等待另一个，这可能导致死锁。示例 1-37 展示了一个死锁。

示例 1-37. 创建死锁

```
using System;
using System.Threading;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            object lockA = new object();
            object lockB = new object();

            var up = Task.Run(() =>
            {
                lock (lockA)
                {
                    Thread.Sleep(1000);
                    lock (lockB)
                    {
                        Console.WriteLine("Thread 1");
                    }
                }
            });

            lock (lockB)
            {
                Thread.Sleep(1000);
                lock (lockA)
                {
                    Console.WriteLine("Thread 2");
                }
            }

            up.Wait();
        }
    }
}
```

在此更改之后，程序始终输出 `0`，因为对变量 `n` 的访问现在是同步的。

然而，不当访问可能会导致一个线程在等待另一个，这可能导致死锁。示例 1-37 展示了一个死锁。

示例 1-37. 创建死锁

```
using System;
using System.Threading;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            object lockA = new object();
            object lockB = new object();

            var up = Task.Run(() =>
            {
                lock (lockA)
                {
                    Thread.Sleep(1000);
                    lock (lockB)
                    {
                        Console.WriteLine("Thread 1");
                    }
                }
            });

            lock (lockB)
            {
                Thread.Sleep(1000);
                lock (lockA)
                {
                    Console.WriteLine("Thread 2");
                }
            }

            up.Wait();
        }
    }
}
```

在此更改之后，程序始终输出 `0`，因为对变量 `n` 的访问现在是同步的。

然而，不当访问可能会导致一个线程在等待另一个，这可能导致死锁。示例 1-37 展示了一个死锁。

示例 1-37. 创建死锁

```
using System;
using System.Threading;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            object lockA = new object();
            object lockB = new object();

            var up = Task.Run(() =>
            {
                lock (lockA)
                {
                    Thread.Sleep(1000);
                    lock (lockB)
                    {
                        Console.WriteLine("Thread 1");
                    }
                }
            });

            lock (lockB)
            {
                Thread.Sleep(1000);
                lock (lockA)
                {
                    Console.WriteLine("Thread 2");
                }
            }

            up.Wait();
        }
    }
}
```

(抱歉，由于系统处理逻辑出现了重复，上述部分中包含了多次重复内容。我将根据您提供的原始文本提供简洁、准确的翻译：)

[content]
虽然多线程可以给你带来很多优势，但编写多线程应用程序并不是易事。当不同的线程访问某些共享数据时，可能会出现问题。当两个线程都尝试同时更改某些内容时，会发生什么？为了让这成功工作，同步资源至关重要。

本目标涵盖了如何：
* 同步资源。
* 取消运行时间长的任务。

## 同步资源

正如你所看到的，在 .NET 的 TPL 支持下，创建一个多线程应用程序是非常容易的。但当你使用多线程构建真实世界的应用程序时，当你想要从多个线程同时访问相同的数据时，就会遇到问题。示例 1-35 展示了一个可能出现问题的示例。

示例 1-35. 在多线程应用程序中访问共享数据

```
using System;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            int n = 0;

            var up = Task.Run(() =>
            {
                for (int i = 0; i < 1000000; i++)
                    n++;
            });

            for (int i = 0; i < 1000000; i++)
                n--;

            up.Wait();
            Console.WriteLine(n);
        }
    }
}
```

示例 1-35 的输出会是什么？答案是，这取决于情况。当你运行这个应用程序时，每次得到的输出都不同。变量 `n` 的递增和递减这个看似简单的操作，实际上包含了查找（检查 `n` 的值）以及对 `n` 进行加 1 或减 1。但如果第一个任务读取了值并加 1，而任务 2 正好读取了该值并减了 1 呢？这就是示例中发生的情况，这也是为什么你永远得不到预期的 `0` 输出。

这是因为该操作不是原子性的。它由发生在不同时刻的读取和写入操作组成。这就是为什么对你正在工作的数据访问需要同步，这样你才能可靠地预测你的数据是如何受到影响的。

同步共享数据的访问是非常重要的。C# 语言提供的一个特性是 `lock` 运算符，它是编译器翻译为对 `System.Thread.Monitor` 调用的某种语法糖。示例 1-36 展示了如何使用 `lock` 运算符来修复之前的示例。

示例 1-36. 使用 `lock` 关键字

```
using System;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            int n = 0;

            object _lock = new object();

            var up = Task.Run(() =>
            {

                for (int i = 0; i < 1000000; i++)
                    lock (_lock)
                        n++;
            });

            for (int i = 0; i < 1000000; i++)
                lock (_lock)
                    n--;

            up.Wait();
            Console.WriteLine(n);
        }
    }
}
```

在此更改之后，程序始终输出 `0`，因为对变量 `n` 的访问现在是同步的。

然而，不当访问可能会导致一个线程在等待另一个，这可能导致死锁。示例 1-37 展示了一个死锁。

示例 1-37. 创建死锁

```
using System;
using System.Threading;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            object lockA = new object();
            object lockB = new object();

            var up = Task.Run(() =>
            {
                lock (lockA)
                {
                    Thread.Sleep(1000);
                    lock (lockB)
                    {
                        Console.WriteLine("Thread 1");
                    }
                }
            });

            lock (lockB)
            {
                Thread.Sleep(1000);
                lock (lockA)
                {
                    Console.WriteLine("Thread 2");
                }
            }

            up.Wait();
        }
    }
}
```



你可以使用锁（locking）来修复这个问题，但 .NET Framework 中还有另一个类可以使用可以使用：`System.Threading.Volatile`。该类具有特殊的 `Write` 和 `Read` 方法，这些方法会禁用编译器优化，从而让你能够在代码中强制执行正确的顺序。按照正确的顺序使用这些方法可能会非常复杂，因此 .NET 提供了 `volatile` 关键字，你可以将其应用于字段。你只需要将字段的声明更改为如下所示：

```
private static volatile int _flag = 0;
```

意识到 `volatile` 关键字的存在是件好事，但你应该只在真的需要它时才使用它。因为它禁用了某些编译器优化，它会损害性能。此外，它并不是所有 .NET 语言都支持（Visual Basic 不支持），因此会阻碍语言之间的互操作性。

## `Interlocked` 类

参考示例 1-35，其核心问题在于加法和减法操作不是原子的。这是因为 `n++` 被翻译为 `n = n + 1`，包含一次读取一次写入。

使操作原子化是 `System.Threading` 命名空间下 `Interlocked` 类的工作。当使用 `Interlocked.Increment` 和 `Interlocked.Decrement()` 时，你创建了一个原子操作，如示例 1-40 所示。

示例 1-40. 使用 `Interlocked` 类

```
using System;
using System.Threading;
using System.Threading.Tasks;

namespace Chapter1
{
    public class Program
    {
        static void Main()
        {
            int n = 0;

            var up = Task.Run(() =>
            {
                for (int i = 0; i < 1000000; i++)
                    Interlocked.Increment(ref n);
            });

            for (int i = 0; i < 1000000; i++)
                Interlocked.Decrement(ref n);

            up.Wait();
            Console.WriteLine(n);

        }

    }
}
```

`Interlocked` 保证递增和递减操作是原子执行的。其他线程不会看到任何中间结果。当然，加减是非常简单的操作。如果你有更复杂的操作，仍然必须使用锁（lock）。

`Interlocked` 还支持通过 `Exchange` 方法切换值。你如下所示使用该方法：

```
if ( Interlocked.Exchange(ref isInUse, 1) == 0) { }
```

这段代码在同一次操作中获取当前值，并立即将其设置为新值。它在更改值之前返回旧值。

你还可以使用 `CompareExchange` 方法。该方法首先检查期望值是否存在；如果存在，则用另一个值替换它。

示例 1-41 显示了在非原子操作中比较和交换值可能会什么问题。

示例 1-41. 作为非原子操作的比较和交换

```
using System;
using System.Threading;
using System.Threading.Tasks;

public static class Program
{
    static int value = 1;

    public static void Main()
    {
        Task t1 = Task.Run(() =>
        {
            if (value == 1)
            {
                // 删除下面这一行将改变输出
                Thread.Sleep(1000);
                value = 2;
            }
        });

        Task t2 = Task.Run(() =>
        {
            value = 3;
        });

        Task.WaitAll(t1, t2);
        Console.WriteLine(value); // 显示 2
    }
}
```

`Task t1` 开始运行并看到 `value` 等于 `1`。同时，`t2` 将值更改为 `3`，然后 `t1` 将其改回 `2`。为了避免这种情况，你可以使用以下 `Interlocked` 语句：

```
Interlocked.CompareExchange(ref value, newValue, compareTo);
```

这确保了比较值并将其交换为新值是一个原子操作。这样，没有其他线程可以在比较和交换之间更改该值。

## 取消任务

在处理如 TPL、`Parallel` 类或 PLINQ 等多线程代码时，你通常会有长时间运行的任务 .NET Framework 提供了一个特殊的类可以帮助你取消这些任务：`CancellationToken`。

你将 `CancellationToken` 传递给 `Task`，然后 `Task` 会期监控令牌以查看是否请求了取消。

示例 1-42 显示了你如何使用 `CancellationToken` 来结束任务。

示例 1-42. 使用 `CancellationToken`

```
CancellationTokenSource cancellationSource =
    new CancellationTokenSource();
CancellationToken token = cancellationSource.Token;

Task task = Task.Run(() =>
{
    while(!token.IsCancellationRequested)   
    {

        Console.Write("*");
        Thread.Sleep(1000);
    }

}, token);

Console.WriteLine("按回车停止任务");
Console.ReadLine();

cancellationTokenSource.Cancel();

Console.WriteLine("按回车结束应用程序");
Console.ReadLine();
```

`CancellationToken` 用于异步 `Task`。`CancellationTokenSource` 用于信号 `Task` 应该取消。在这种情况下，当请求取消时，操作将结束。*Task* 的外部用户看不到任何内容，因为 *Task* 只会处于 `RanCompletion` 状态。如果你想向外部用户信号你的任务已取消，可以通过抛出 `OperationCanceledException` 来。示例 1-43 显示了如何这样做。

示例 1-43. 抛出 `OperationCanceledException`

```
using System;
using System.Threading;
using System.Threading.Tasks;

namespace Chapter1.Threads
{
    public class Program
    {
        static void Main()
        {
            CancellationTokenSource cancellationSource =
                new CancellationTokenSource();
            CancellationToken token = cancellationSource.Token;

            Task task = Task.Run(() =>
            {
                while (!token.IsCancellationRequested)
                {

                    Console.Write("*");
                    Thread.Sleep(1000);
                }

                token.ThrowIfCancellationRequested();

            }, token);

            Console.WriteLine("按回车停止任务");
            Console.ReadLine();

            try
            {

                cancellationTokenSource.Cancel();
                task.Wait();
            }
            catch (AggregateException e)
            {
                Console.WriteLine(e.InnerExceptions[0].Message);
            }
            Console.WriteLine("按回车结束应用程序");
            Console.ReadLine();

        }

    }
}
// 显示
// 按回车停止任务
// **
// 操作已取消。
// 按回车结束应用程序
```

除了捕获异常外，你还可以添加一个仅在 `Task` 取消时执行的延续 `Task`。在这个 `Task` 中，你可以访问抛出的异常，并可以根据情况选择处理它。示例 1-44 显示了这样的延续任务看起来是样子的。

示例 1-44. 为取消的任务添加延续任务

```
Task task = Task.Run(() =>
{
    while (!token.IsCancellationRequested)
    {
        Console.Write("*");
        Thread.Sleep(1000);
    }

}, token).ContinueWith((t) =>
{
    t.Exception.Handle((e) => true);
    Console.WriteLine("你已取消任务");
}, TaskContinuationOptions.OnlyOnCanceled);
```





如果你想在一定时间后取消一个 `Task`，可以使用带有超时参数的 `Task.WaitAny` 重载方法。示例 1-45 显示了一个示例。

示例 1-45. 为任务设置超时

```
Task longRunning = Task.Run(() =>
{
    Thread.Sleep(10000);
});

int index = Task.WaitAny(new[] { longRunning }, 1000);

if (index == -1)
    Console.WriteLine("Task timed out");
```

如果返回的 `index` 为 `-1`，则任务已超时。检查其他任务中可能出现的任何错误是非常重要的。如果你不捕获这些错误，它们将处于未处理状态。

## 思考实验

#### 实现多线程

在这个思考实验中，请运用你关于本目标中学到的知识。你可以在章节末的答案部分找到这些问题的答案。

你在代码中遇到了死锁。确实，你使用了大量的 `lock` 语句，并且正试图改进代码以避免死锁。

1. 你如何编排你的锁定代码以避免死锁？
2. `Interlocked` 类如何能帮助你？

## 目标总结

* 当在多线程环境中访问共享数据时，你需要同步访问以避免错误或数据损坏。
* 在私有对象上使用 `lock` 语句来同步对某段代码的访问。
* 你可以使用 `Interlocked` 类来执行简单的原子操作。
* 你可以使用带有 `CancellationToken` 的 `CancellationTokenSource` 类来取消任务。

## 目标复习

回答以下问题以测试你对本目标中信息的掌握情况。你可以在章节末的答案部分找到这些问题的答案，以及对每个选项为何正确或错误的解释。

1. 你想通过使用 `lock` 语句来同步访问。你会在哪个成员上进行锁定？
    1. `this`
22. `string _lock = “mylock”`
    3. `int _lock = 42;`
    4. `object _lock = new object();`

2. 你需要为一个长时间运行的任务实现取消。你将哪个对象传递给任务？
    1. `CancellationTokenSource`
    2. `CancellationToken`
    3. 布尔变量 `isCancelled` 
    4. `Volatile`

3. 你正在一个多线程类中实现状态机。你需要检查当前状态并在每一步将其更改为新状态。你使用哪种方法？
    1. `Volatile.Write(ref currentState)`
    2. `Interlocked.CompareExchange(ref currentState, ref newState, expectedState)`
    3. `Interlocked.Exchange(ref currentState, newState)`
    4. `Interlocked.Decrement(ref newState)`

## 目标 1.3：实现程序流

管理程序流的一个重要方面是在你的应用程序中做出决策，包括检查用户是否输入了正确的密码、确保某个值在范围内，或者其他无数种可能性之一。C# 提供了几个语句，可以在需要做决策时使用。

除了做出决策，另一个常见任务是处理集合。C# 提供的语言特性可以帮助你处理集合，允许你遍历集合并访问单个项目。

本目标涵盖了如何：
* 处理布尔表达式。
* 在你的应用程序中做出决策。
* 遍历集合。
* 使用显式的 `jump` 语句。

## 处理布尔表达式

在处理流控制语句时，你会自动处理`布尔表达式`（Boolean expressions）。布尔表达式的结果始终应该是 `true` 或 `false`，但在执行过程中，通过使用不同的`运算符`（operators），它们变得非常复杂。

其中一个运算符是相等运算符 (`==`）。你用它来测试两个值是否相等。示例 1-46 显示了一些示例。

示例 1-46. 一个可读性更好的嵌套 `if` 语句

```
int x = 42;
int y = 1;
int z = 42;

Console.WriteLine(x == y); // 显示 false
Console.WriteLine(x == z); // 显示 true
```

表 1-1 显示了可以在 C# 中使用的运算符。

表 1-1. C# 关系和相等运算符

| 运算符 | 描述 | 示例 |
| --- | --- | --- |
| < | 小于 | x < 42; |
| > | 大于 | x > 42; |
| <= | 小于等于 | x <= 42; |
| >= | 大于等于 | x >= 42; |
| == | 等于 | x == 42; |
| != | 不等于 | x != 42; |

你可以通过使用 `OR` (`||`)、`AND` (`&&`) 和异异 (`^`) 来组合这些运算符。这些运算符使用左操作数和右操作数。`OR` 运算符在其中一个操作数为 `true` 时返回 `true`。如果两者都为 `false`，则返回 `false`。示例 1-47 显示了一个示例。

示例 1-47. 布尔 `OR` 运算符

```
bool x = true;
bool y = false;

bool result = x || y;
```

如果运行时发现你的表达式的左部分为 `true`，则它不需要评估右部分。这被称为短路（short-circuiting）。示例 1-48](#ch01.html_short-circuiting_the_or_operator "示例 1-48. OR 运算符的短路") 显示了一个示例。

示例 1-48. `OR` 运算符的短路

```c
public void OrCircuit()
{
    bool x = true;
    bool result = x || GetY();
}

private bool GetY()
{
    Console.WriteLine("此方法没有被调用");
    return true;
}
```

在这种情况下，`GetY` 方法没有被调用，控制台也没有写入该内容。

`AND` 运算符用于表达式的所有部分都为 `true`的情况。如果其中任一操作数为 `false`，整个表达式的结果为 `false`。示例 1-49 使用 `AND` 运算符检查值是否在特定范围内。

示例 1-49. 使用 `AND` 运算符

```c
int value = 42;
bool result = (0 < value) && (value < 100)
```

在这种情况下，并不要求在左右操作数周围添加额外的括号，但这有助于增加代码的可读性。与 `OR` 运算符一样，运行时应用了短路。除了性能优化外，你在处理 `null` 值时也可以利用这一点。示例 1-50 例如使用 `AND` 运算符检查 `input` 参数不为 `null` 并对其执行方法。如果在这种情况下不使用短路，每当 `input` 参数为 `null` 时，代码都会抛出异常。

示例 1-50. 使用 `AND` 运算符

```csharp
public void Process(string input)
{
    bool result = (input != null) && (input.StartsWith("v"));
    // 对结果执行某些操作
}
```

异异运算符 (`^`) 仅当两个操作数中恰好有一个为 `true` 时返回 `true`。表 1-2 给出了 `XOR` 运算符的所有可能性。

表 1-2. *XOR* 运算符的可能值

| 左操作数 | 右操作数 | 结果 |
| --- | --- | --- |
| True | True | False |
| True | False | True |
| False | True | True |
| False | False | False |





由于 `XOR` 运算符必须检查操作数是否恰好有一个为 `true`，因此它不支持短路机制。示例 1-51 展示了如何使用 `XOR` 运算符。

示例 1-51. 使用 `XOR` 运算符

```c
bool a = true;
bool b = false;

Console.WriteLine(a ^ a); // False
Console.WriteLine(a ^ b); // True
Console.WriteLine(b ^ b); // False
```

## 做出决策

C# 提供了多种`流程控制语句`，可以帮助你确定应用程序遵循的路径。你可以使用以下语句：

* `if`
* `while`
* `do while`
* `for`
* `foreach`
* `switch`
* `break`
* `continue`
* `goto`
* 空值合并运算符 `(??)`
* 条件运算符 `(?::)`

通过使用这些结构，你可以创建灵活的应用程序，使能够根据不同的情况执行不同的行为。了解这些语句并能够在它们之间进行选择是非常重要的。

## `if` 语句

最广泛使用的流程控制语句是 `if` 语句。`if` 语句允许你根据特定条件执行一段代码。`if 语句`的通用语法如下：

```
if (boolean-expression)
   要执行的语句
```

只有当 `boolean` 表达式求值为 `true` 时，才会执行该语句。示例 1-52 展示了使用 `if` 的示例。

示例 1-52. 基础 `if` 语句

```csharp
bool b = true;
if (b)
    Console.WriteLine("True");
```

在这种情况下，应用程序输出“True”，因为 `if 语句`的条件为 `true`。如果 `b` 为 `false`，则不会执行 `Console.WriteLine` 语句。

当然，向 `if 语句` 传递一个硬编码的值没有太大用。通常，你会使用 `if 语句`配合一个在应用程序执行过程中可以变化的动态值。

在处理程序流程语句时，了解`代码块`的概念很重要，它允许你在只允许单条语句的上下文中编写多条语句。块使用大括号来表示其开始和结束：

```
{
    语句
}
```

示例 1-52 展示了一个`if 语句`，它只在条件为 `true` 时执行单行代码。然而，你也可以在 `if 语句` 之后使用`代码块`。块中的所有代码都根据 `if 语句`的结果执行。你可以在示例 1-53 中看到此示例。

示例 1-53. 带有代码块的 `if` 语句

```csharp
bool b = true;
if (b)
{
    Console.WriteLine("Both these lines");
    Console.WriteLine("Will be executed");
}
```

在代码块内定义的变量仅在代码块内可用，并在块结束时超出作用域。这意味着你可以在块内部声明变量并在块内使用它们，但在块外部无法。示例 1-54 展示了作用域的差异。变量 `b` 定义在块外部，可以在外部块和 `if` 语句中访问。然而，变量 `r` 只能在 `if` 语句中访问。

示例 1-54. 代码块与作用域

```csharp
bool b = true;
if (b)
{
    int r = 42;
    b = false;
}

// r 无法访问
// b 现在是 false
```

你还可以在 `if 语句` 求值为 `false` 时执行某些代码。你可以通过使用 `else` 块来实现这一点。通用语法如下：

```
if (boolean-expression)
    语句
else
    语句
```

示例 1-55 展示了使用 `else` 语句的示例。它输出“False”。

示例 1-55. 使用 `else` 语句

```csharp
bool b = false;

if (b)
{
    Console.WriteLine("True");
}
else
{
    Console.WriteLine("False");
}
```

你可以使用多个 `if/else` 语句，如示例 1-56 所示。

示例 1-56. 使用多个 `if/else` 语句

```csharp
bool b = false;

if (b)
{
    Console.WriteLine("True");
}
else if (someOtherCondition)
{
    Console.WriteLine("Other");
}
else
{
    // 略
}
```

## 空值合并运算符

`??` 运算符被称为`空值合并运算符`。你可以使用它为可空类型或引用类型提供默认值。如果左操作数不是 `null`，则返回左操作数；否则返回右操作数。示例 1-58 展示了该运算符的使用示例。

示例 1-58. 空值合并运算符

```csharp
int? x = null;
int y = x ?? -1;
```

你还可以嵌套空值合并运算符，如示例 1-59 所示。

示例 1-59. 嵌套空值合并运算符

```csharp
int? x = null;
int? z = null;
int y = x ?? z ?? -1;
```

## 条件运算符

`运算符` `?:` 根据布尔表达式返回两个值之一。如果表达式为 `true`，返回第一个值；否则返回第二个。示例 1-60 展示了如何使用该运算符简化代码的示例。在这种情况下，`if` 语句可以用条件运算符替换。

示例 1-60. 条件运算符

```csharp
private static int GetValue(bool p)
{
    if (p)
        return 1;
    else
        return 0;

    return p ? 1 : 0;
}
```

## `switch` 语句

你可以使用 `switch` 语句来简化复杂的 `if` 语句。参考示例 1-61。

示例 1-61. 复杂的 `if` 语句

```csharp
void Check(char input)
{
    if (input == 'a'
        || input == 'e'
        || input == 'i'
        || input == 'o'
        || input == 'u')
    {
        Console.WriteLine("Input is a vowel");
    }
    else
    {
        Console.WriteLine("Input is a consonant");
    }
}
```





`switch` 语句可以用来使这段代码更全面。`switch` 语句检查其参数的值，然后寻找匹配的标签。示例 1-62 显示了将示例 1-59 中的代码转换为 `switch` 语句的形式。

### 示例 1-62. 一个 `switch` 语句

```cpp
void CheckWithSwitch(char input)
{
    switch (input)
    {
        case 'a':
        case 'e':
        case 'i':
        case 'o':
        case 'u':
            {
                Console.WriteLine("Input is a vowel");
                break;
            }
        case 'y':
            {
                Console.WriteLine("Input is sometimes a vowel.");
                break;
            }
        default:
            {
                Console.WriteLine("Input is a consonant");
                break;
            }
    }
}
```

`switch` 可以使用一个或多个 `switch-sections`，这些部分可以包含一个或多个 `switchlabels`。在示例 1-62 中，所有的元音都属于同一个 `switch-section`。如果你需要，你也可以添加一个 `default label`，它在其他其他标签都不匹配时被使用。

`switch` 语句的终点不应该是可达的。你需要一个诸如 `break` 或 `return` 的语句来显式地退出 `switch` 语句，或者你需要抛出一个异常。这避免了 C++ 中有的穿透（fall-through）行为。这使得 `switch` 部分可以按任何顺序出现而不影响行为。

与其隐式地穿透到另一个标签，你可以使用 `goto 语句`（参见示例 1-63）。

### 示例 1-63. `switch` 语句中的 `goto`

```cpp
int i = 1;
switch (i)
{
    case 1:
        {
            Console.WriteLine("Case 1");
            goto case 2;
        }
    case 2:
        {
            Console.WriteLine("Case 2");
            break;
        }
}

// Displays
// Case 1
// Case 2
```

## 遍历集合

另一个与程序流相关的主题是遍历集合。集合在 C# 中被广泛使用，该语言提供了你可以与它们一起使用的结构：

* `for`
* `foreach`
* `while`
* `do while`

### `for` 循环

当你需要遍历集合直到达到特定条件时（例如，你已经到达集合的末尾），可以使用 `for 循环`。示例 1-64 显示了一个循环数组中所有项的示例。

#### 示例 1-64. 一个基础 `forfor 循环

```cpp
int[] values = { 1, 2, 3, 4, 5, 6 };
for (int index = 0; index < values.Length; index++)
{
    Console.Write(values[index]);
}

// Displays
// 123456
```

如你所见，`for` 循环由三个部分组成：

```cpp
for(initial; condition; loop)
```

* 初始部分在第一次迭代之前执行，并声明和初始化循环中使用的变量。
* 条件在每次迭代时进行评估。当条件等于 `false` 时，退出循环。
* 循环部分在每次迭代期间运行，通常用于更改用于遍历集合的计数器。

这些部分都不是必须的。你可以使用 `for(;;) {}` 作为一个完全合法的、永远不会结束的 `for` 循环。你还可以在 `for` 循环的每个部分中使用多个语句（参见示例 1-65）。

### 示例 1-65. 带有多个循环变量的 `for` 循环

```cpp
int[] values = { 1, 2, 3, 4, 5, 6 };
for (int x = 0, y = values.Length - 1; 
    ((x < values.Length) && (y >= 0)); 
    x++, y--)
{
    Console.Write(values[x]);
    Console.Write(values[y]);
}

// Displays
// 162534435261
```

并不要求循环值按 1 递增或递减。例如，你可以修改示例 1-64，使 `index` 递增 2 以仅显示奇数，如示例 1-66 所示。

### 示例 1-66. 自增的 `for` 循环

```cpp
int[] values = { 1, 2, 3, 4, 5, 6 };
for (int index = 0; index < values.Length; index += 2)
{
    Console.Write(values[index]);
}

// Displays
// 135
```

通常，`for` 循环在条件变为 `false` 时结束，但你也可以使用 `break` 语句来退出循环。示例 1-67 显示了 `break` 语句。

### 示例 1-67. 带有 `break` 的 `for` 循环

```cpp
int[] values = { 1, 2, 3, 4, 5, 6 };
for (int index = 0; index < values.Length; index++)
{
    if (values[index] == 4) break;
    Console.Write(values[index]);
}

// Displays
// 123
```

接下来，为了完全跳循环，你可以使用 `goto 语句`。示例 1-68 显示了使用 `continue` 语句。

### 示例 1-68. 带有 `continue` 的 `for` 循环

```cpp
int[] values = { 1, 2, 3, 4, 5, 6 };
for (int index = 0; index < values.Length; index++)
{
    if (values[index] == 3) continue;
    Console.Write(values[index]);
}

// Displays
// 12456
```

另一种循环结构是 `while` 循环。`for` 循环仅仅是编写 `while` 循环检查并增加计数器的方便方式。示例 1-69 显示了一个示例。注意变量的范围。

### 示例 1-69. 带有 `while` 的 `for` 循环

```cpp
int[] values = { 1, 2, 3, 4, 5, 6 };

{
    int index = 0;
    while (index < values.Length)
    {
        Console.Write(values[index]);
        index++;
    }
}
```

`while` 循环在表达式为 `true` 时执行。当你提前知道迭代次数时应该使用 `for` 循环。如果 `while` 循环条件为 `false`，它不会执行循环内部的代码。这在使用 `do-while` 循环时不同。`do-while` 循环至少执行一次，即使表达式为 `false` 也是如此。示例 1-70 显示了使用 `do-while` 循环的示例。

### 示例 1-70. `do-while` 循环

```cpp
do
{
    Console.WriteLine("Executed once!");
}
while (false);
```

`foreach` 循环用于遍历集合并自动将当前项存储在 `loop` 变量中。`foreach` 循环跟踪它在集合中的位置并防止你越过集合的末尾。示例 1-71 显示了如何使用 `foreach` 循环的示例。

### 示例 1-71. 一个 `foreach` 循环

```cpp
int[] values = { 1, 2, 3, 4, 5, 6 };

foreach (int i in values)
{
    Console.Write(i);
}

// Displays 123456
```



正如你所看到的，`foreach` 循环会自动将当前项存储在强类型变量中。你可以使用 `continue` 和 `break` 语句来影响 `foreach` 循环的工作方式。

`loop` 变量是不可修改的。你可以对变量指向的对象进行修改，但不能给它赋值一个新值。示例 1-72 演示了这些差异。

### 示例 1-72. 在 `foreach` 中更改项

```
class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
}

void CannotChangeForeachIterationVariable()
{
    var people = new List<Person>
    {
        new Person() { FirstName = "John", LastName = "Doe"},
        new Person() { FirstName = "Jane", LastName = "Doe"},
    };

    foreach (Person p in people)
    {
        p.LastName = "Changed"; // 这是允许的
        // p = new Person(); // 这将导致编译错误
    }
}
```

当你知道 `foreach` 实际上是如何工作时，你就能理解这种行为。当编译器遇到 `foreach` 语句时，它会代表你生成一些代码；`foreach` 是一种语法糖，让你能够以优雅的方式编写代码。示例 1-73 演示了正在发生什么。

### 示例 1-73. 为 `foreach` 循环生成的编译器代码

```
List<Person>.Enumerator e = people.GetEnumerator();

try
{
    Person v;
    while (e.MoveNext())
    {
        v = e.Current;
   }
}
finally
{
    System.IDisposable d = e as System.IDisposable;
    if (d != null) d.Dispose();
}
```

如果你将 `e.Current` 的值改为其他内容，迭代器模式将无法确定在调用 `e.MoveNext` 时该做什么。这就是为什么在 `foreach` 语句中不允许更改迭代变量的值的原因。

### 更多信息：枚举器 (Enumerators)

关于 `GetEnumerator` 方法如何工作以及你如何实现自己的枚举器的更多信息，请参见第 2 章。

### 跳转语句

另一种可以影响程序流的语句是`跳转语句`。你已经看过了其中两种语句：`break` 和 `continue`。`跳转语句` 无条件地将控制转移到代码的另一个位置。

另一种可以改变程序流的跳转语句是 `goto`。`goto` 语句将控制移动到标记有标签的语句。如果找不到标签，或者标签不在 `goto` 语句的作用范围内，就会发生编译错误。示例 1-74 显示了使用 `goto` 和 `label` 的示例。

### 示例 1-74. 带有标签的 `goto` 语句

```
int x = 3;
if ( x == 3) goto customLabel;
x++;

customLabel:
Console.WriteLine(x);
// 显示 3
```

你不能跳转到不在作用内的标签。这意味着你不能将控制转移到当前块之外的另一个代码块。编译器还会确保任何介入其中的 `finally` 块都会被执行。

`break` 和 `continue` 等`跳转语句`在某些情况下是有其用途的。然而，如果可能的话，你应该尝试避免它们。通过重构你的代码，你可以在大多数情况下移除它们，这将提高你代码的可读性。

`goto` 语句更为糟糕。它被认为是一种坏习惯。尽管 C# 限制了 `goto` 运算符的行为方式，但作为指南，你应该尽量避免使用 `goto`。`goto` 使用的一个区域是在生成的代码中，例如你在 C# 5 中使用新的 `async`/await` 特性时编译器生成的代码。

### 更多信息：跳转语句

关于`跳转语句`的更多信息，*请参阅 [`msdn.microsoft.com/en-us/library/d96yfwee.aspx`](http://msdn.microsoft.com/en-us/library/d96yfwee.aspx)*。

## 思考实验

#### 选择你的程序流语句

在这个思考实验中，应用你关于本目标所学的知识。你可以在本章末最后的答案 部分找到这些问题的答案。

你正在将一个旧的 C#2 控制台应用程序更新为 WPF C#5 应用程序。该应用程序被酒店用于跟踪预订以及客人的进出。你正在检阅旧代码库，以确定是否有可以轻松重用的代码。你注意到几点：

*   代码使用 `goto` 语句来管理流。
*   有许多长的 `if` 语句来映射用户输入。

1. 使用 `goto` 的缺点是什么？
2. 你可以使用什么来改进你的代码？
3. 什么时候应该使用？

## 目标总结

*   布尔表达式可以使用 `==`、`!=`、`<>`。
*   `if-else` 语句根据条件执行代码。
*   `switch` 语句用于匹配一个值。
*   `for` 循环用于你知道迭代次数的情况。
*   `while` 循环用于条件为真时执行代码；`do-while` 循环应至少执行一次。
*   `foreach` 可用于遍历集合。
*   `break`、`goto` 和 `continue` 等`跳转语句`用于转移控制。

### 目标回顾

回答以下问题以测试你对目标的掌握。答案以及每个选项正确或错误的解释可以在本章末最后的答案 部分找到。

1. 你需要遍历一个已知数量的集合。你需要从集合中移除项。你使用什么语句？
    *   `switch`
    *   `foreach`
    *   `for`
    *   `goto`
2. 你的应用程序中有许多对 `null` 的检查。如果值不为 `null`，你想对其调用方法。你想简化代码。你使用哪种技术？
    *   `for`
    *   条件运算符
    *   空合并运算符
    *   与运算符的短路行为
3. 你正在处理来自网络的一些数据。你使用 `HasNext` 和 `Read` 方法检索数据。你需要对每个项运行某些代码。你使用什么？
    *   `for`
    *   `foreach`
    *   `while`
    *   `do-while`

## 目标 1.4：创建和实现事件和回调

*事件*可以用于提供通知。如果你对这些通知感兴趣，可以订阅事件。你还可以创建自己的事件并在发生有趣事件时引发它们以提供通知。.NET Framework 提供了你可以创建事件的内置类型。通过使用委托、Lambda 表达式和匿名方法，你可以以舒适的方式创建和使用事件。

本目标涵盖了：

*   理解委托。
*   使用 Lambda 表达式。
*   创建和引发事件。

## 理解委托

在 C# 中，*委托* 是事件的基础构建块。*委托* 是一个定义方法签名的类型。例如在 C++ 中，你会使用函数指针来实现。在 C# 中，你可以实例化*委托*并让它指向另一个方法。你可以通过*委托*调用该方法。



示例 1-75 展示了声明 `delegate` 并通过它调用方法的示例。

### 示例 1-75. 使用 delegate

```
public delegate int Calculate(int x, int y);

public int Add(int x, int y) { return x + y; }
public int Multiply(int x, int y) { return x * y; }

public void UseDelegate()
{
    Calculate calc = Add;
    Console.WriteLine(calc(3, 4)); // Displays 7

    calc = Multiply;
    Console.WriteLine(calc(3, 4)); // Displays 12
}
```

如你所见，你使用特殊的 `delegate` 关键字告诉编译器你正在创建一个 `delegate` 类型。`Delegates` 可以嵌套在其他类型中，然后作为嵌套类型使用。

实例化 `delegates` 是很容易的，因为 C# 2.0 添加了当将方法组赋值给 `delegate` 类型时，自动创建一个新的 `delegate`。实例化的 `delegate` 是一个对象；你可以传递它并将其作为参数传递给其他方法。

`delegates` 的另一个特性是你可以将它们组合。这被称为 `multicasting`（多委托）。你可以使用 `+` 或 `+=` 运算符向现有 `delegate` 实例的 `invocation list`（调用列表）添加另一个方法。示例 1-76 展示了一个示例。

### 示例 1-76. 多委托 delegate

```
public void MethodOne() 
{ 
    Console.WriteLine("MethodOne"); 
}

public void MethodTwo()
{
    Console.WriteLine("MethodTwo");
}

public delegate void Del();

public void Multicast()
{
    Del d = MethodOne;
    d += MethodTwo;

    d();
}
// Displays
// MethodOne
// MethodTwo
```

你也可以使用减赋值运算符 `-` 或 `-=` 从调用列表中移除方法。

这一切之所以可能，是因为 `delegates` 继承自 `System.MulticastDelegate` 类，而该类又继承自 `System.Delegate`。正因如此，你可以在你的 `delegate` 上使用这些基类中定义的成员。

例如，要找出多委托将调用多少个方法，你可以使用以下代码：

```
int invocationCount = del.GetInvocationList().GetLength(0);
```

当你将方法赋值给 `delegate` 时，方法的签名并不非完全匹配 `delegate`。这被称为 `covariance`（协变）和 `contravariance`（逆变）。`Covariance` 使得方法的返回类型比 `delegate` 中定义的类型更派生成为。`Contravariance` 则允许方法的参数类型比 `delegate` 类型中的类型更派生。

示例 1-77 展示了 `covariance` 的示例。

### 示例 1-77. delegate 的协变

```c
public delegate TextWriter CovarianceDel();

public StreamWriter MethodStream() { return null; }
public StringWriter MethodString() { return null; }

CovarianceDel del;
del = MethodStream;
del = MethodString;
```

由于 `StreamWriter` 和 `StringWriter` 都继承自 `TextWriter`，你可以在两个方法都使用 `CovarianceDel`。逆变的示例可以在 示例 1-78 中看到。

### 示例 1-78. delegate 的逆变

```c
void DoSomething(TextWriter tw) { }
public delegate void ContravarianceDel(StreamWriter tw);

ContravarianceDel del = DoSomething;
```

由于方法 `DoSomething` 可以处理 `TextWriter`，它理然也能处理 `StreamWriter`。由于 `contravariance`，你可以调用该 `delegate` 并将 `StreamWriter` 实例传递给 `DoSomething` 方法。

### More 信息：协变与逆变

关于协变、逆变以及它们在 C# 中如何实现的更多信息，请参见 Eric Lippert 在 `http://blogs.msdn.com/b/ericlippert/archive/tags/covariance+and+contravariance/` (http://blogs.msdn.com/b/ericlippert/archive/tags/covariance+and+contravariance/) 上编写的系列博客文章。

## 使用 lambda 表达式

有时，方法的整个签名比方法体的代码还要。在某些情况下，你需要创建一个完整的方法仅是为了在 `delegate` 中使用。

对于这些情况，Microsoft 为 C# 添加了一些新功能。在 C# 2.0 中，添加了 `anonymous methods`（匿名方法）。在 C# 3.0 中，随着 `lambda expressions`（lambda 表达式）的添加，情况变得更好。Lambda expressions` 是编写新代码的首选方式。

示例 1-79 展示了如何使用 lambda 语法编写 示例 1-73 中的示例。

#### 示例 1-79. 创建 delegate 的 lambda 表达式

```
Calculate calc = (x, y) => x + y;
Console.WriteLine(calc(3, 4)); // Displays 7

calc = (x, y) => x * y;
Console.WriteLine(calc(3, 4)); // Displays 12
```

如你所见，你使用特殊的 `delegate` 关键字告诉编译器你正在创建一个 `delegate` 类型。`Delegates` 可以嵌套在其他类型中，然后作为嵌套类型使用。

实例化 `delegates` 是很容易的，因为 C# 2.0 添加了当将方法组赋值给 `delegate` 类型时，自动创建一个新的 `delegate`。实例化的 `delegate` 是一个对象；你可以传递它并将其作为参数传递给其他方法。

`delegates` 的另一个特性是你可以将它们组合。这被称为 `multicasting`。你可以使用 `+` 或 `+=` 运算符向现有 `delegate` 实例的 `invocation list` 添加另一个方法。

你也可以使用减赋值运算符 `-` 或 `-=` 从调用列表中移除方法。

这一切之所以可能，是因为 `delegates` 继承自 `System.MulticastDelegate` 类，而该类又继承自 `System.Delegate`。正因如此，你可以在你的 `delegate` 上使用这些基类中定义的成员。

例如，要找出多委托将调用多少个方法，你可以使用以下代码：

```
int invocationCount = del.GetInvocationList().GetLength(0);
```

当你将方法赋值给 `delegate` 时，方法的签名并不非完全匹配 `delegate`。这被称为 `covariance` 和 `contravariance`。`Covariance` 使得方法的返回类型比 `delegate` 中定义的类型更派生成为。`Contravariance` 则允许方法的参数类型比 `delegate` 类型中的类型更派生。

示例 1-77 展示了 `covariance` 的示例。

### 示例 1-77. delegate 的协变

```c
public delegate TextWriter CovarianceDel();

public StreamWriter MethodStream() { return null; }
public StringWriter MethodString() { return null; }

CovarianceDel del;
del = MethodStream;
del = MethodString;
```

由于 `StreamWriter` 和 `StringWriter` 都继承自 `TextWriter`，你可以在两个方法都使用 `CovarianceDel`。逆变的示例可以在 示例 1-78 中看到。

### 示例 1-78. delegate 的逆变

```c
void DoSomething(TextWriter tw) { }
public delegate void ContravarianceDel(StreamWriter tw);

ContravarianceDel del = DoSomething;
```

由于方法 `DoSomething` 可以处理 `TextWriter`，它理然也能处理 `StreamWriter`。由于 `contravariance`，你可以调用该 `delegate` 并将 `StreamWriter` 实例传递给 `DoSomething` 方法。

（注：由于原始文本存在大量重复内容，译文已根据逻辑结构进行了合并与精简，确保了所有核心概念如 delegate、协变、逆变以及 lambda 表达式的准确翻译。）



当你的 `lambda` 函数开始引用在 `lambda` 表达式之外声明的变量（或 `this` ）时，情况就会变得复杂。通常情况下，当控制离开变量的作用范围时，该变量就不再有效。但如果一个 `delegate` 引用了一个局部变量并被返回给调用方法会怎样？现在，`delegate` 的寿命比该变量长。为了解决这个问题，编译器会生成代码，使得被捕获变量的寿命至少与生存最长的 `delegate` 一样。这被称为 `closure`（闭包）。

## 使用事件

应用程序开发中一种流行的 `design pattern`（解决反复出现问题的重用方案）是 `publish-subscribe`（发布-订阅）。你可以订阅一个 `event`，然后当该 `event` 的发布者触发新 `event` 时，你就会收到通知。这用于在应用程序的组件之间建立松耦合。

`Delegates` 成了 C# 事件系统的基础。示例 1-82 显示了类如何公开公共的 `delegate` 并触发它。

示例 1-82. 使用 `Action` 暴露事件

```csharp
public class Pub
{
    public Action OnChange { get; set; }

    public void Raise()
    {
        if (OnChange != null)
        {
            OnChange();
        }
    }
}

public void CreateAndRaise()
{
    Pub p = new Pub();
    p.OnChange += () => Console.WriteLine("Event raised to method 1");
    p.OnChange += () => Console.WriteLine("Event raised to method 2");
    p.Raise();
}
```

当调用 `CreateAndRaise` 时，你的代码创建了 `Pub` 的新实例，用两个不同的方法订阅了事件，然后通过调用 `p.Raise` 触发事件。`Pub` 类完全不知道任何订阅者的存在。它只是触发了 `event`。

如果一个 `event` 没有订阅者，那么 `OnChange` 属性将为 `null`。这就是为什么 `Raise` 方法需要检查 `OnChange` 是否为 `null`。

尽管这个系统可以工作，但它存在一些缺点。如果你将方法 2 的订阅行改为以下内容，你通过使用 `*=` 而不是 `+=` 实际上移除了第一个订阅者：

```csharp
p.OnChange = () => Console.WriteLine("Event raised to method 2");
```

在示例 1-82 的示例中，`Pub` 类触发了 `event`。然而，没有任何机制阻止该类的外部用户触发该 `event`。通过直接调用 `p.OnChange()`，该类的每个用户都可以向所有订阅者触发该 `event`。

为了克服这些缺点，C# 语言使用了特殊的 `event` 关键字。示例 1-83 显示了使用 `event` 语法的修改后的 `Pub` 类示例。

示例 1-83. 使用 `event` 关键字

```csharp
public class Pub
{
    public event Action OnChange = delegate { };

    public void Raise()
    {
        OnChange();
    }
}
```

通过使用 `event` 语法，发生了几个有趣的变化。首先，你使用的不再是公共属性而是公共字段。通常情况下，这是一种退步。但通过 `event` 语法，编译器会保护你的字段免受意外访问。

`event` 不能直接赋值给赋值运算符（使用 `*=` 而不是 `+=`）。因此，你不必担心像使用 delegate 语法那样有人会移除之前所有的订阅。

另一个变化是，任何外部用户无法触发你的 `event`。它只能由定义该 `event` 的类的内部代码触发。

示例 1-83 还使用了一些特殊语法将 `event` 初始化为空 `delegate`。这样，你就可以移除触发 `event` 周围的 `null` 检查，因为你可以确定 `event` 永远不会为 `null`。你类的外部用户 无法将 `event` 设置为 `null`；只有你类的成员可以这样做。只要你的其他类成员没有将 `event` 设置为 `null`，你就可以安全地假设它始终有一个值。

然而，为了遵循 .NET Framework 的编码规范，你仍然需要进行更改。你不应该使用 `Action` 类型作为事件，而应该使用 `EventHandler` 或 `EventHandler<T>`。`EventHandler` 声明如下 delegate：

```csharp
public delegate void EventHandler(object sender, EventArgs e);
```

默认情况下，它接收一个 `sender object` 和一些 `event arguments`。按照约定，`sender` 是触发 `event` 的对象（如果来自静态方法，则为 `null`）。通过使用 `EventHandler<T>`，你可以指定想要使用的 `event` 参数类型。示例 1-84 显示了一个示例。

示例 1-84. 自定义事件参数

```csharp
public class MyArgs : EventArgs
{
    public MyArgs(int value)
    {
        Value = value;
    }

    public int Value { get; set; }
}

public class Pub
{
    public event EventHandler<MyArgs> OnChange = delegate { };

    public void Raise()
    {
        OnChange(this, new MyArgs(42));
    }
}

public void CreateAndRaise()
{
    Pub p = new Pub();

    p.OnChange += (sender, e) => Console.WriteLine("Event raised: {0}", e.Value);

    p.Raise();
}
```

`Pub` 类使用了 `EventHandler<T>`，它指定了 `event` 参数的类型。`event` 的订阅者可以访问并使用参数。尽管 `event` 的实现使用了公共字段，但你仍然可以自定义订阅者的添加移除。这被称为 `custom event accessor`（自定义事件访问器）。示例 1-85 显示了为事件创建 `custom event accessor` 的示例。

示例 1-85. 自定义事件访问器

```csharp
public class Pub
{
    private event EventHandler<MyArgs> onChange = delegate { };
    public event EventHandler<MyArgs> OnChange
    {
        add
        {
            lock (onChange)
            {
                onChange += value;
            }
        }
        remove
        {
            lock (onChange)
            {
                onChange -= value;
            }
        }
    }

    public void Raise()
    {
        onChange(this, new MyArgs(42));
    }
}
```

`custom event accessor` 看起来非常像具有 *get* 和 *set* 访问器的属性。你用 *add* 和 *remove* 代替 *get* 和 *set*。在添加和移除订阅者时使用 `lock` 以确保操作线程安全。

### 更多信息：使用 Lock

关于何时以及如何使用锁，请参阅本章前面的“目标 1.2：管理多线程”部分。

如果你使用常规 `event` 语法，编译器会为你生成访问器。这清楚地说明 `events` 不是 `delegates`；它们是 `delegates` 的便捷封装。

`Delegates` 按照顺序执行。通常，`delegates` 按照它们被添加的顺序执行，尽管通用语言体系 (CLI) 并没有规定，因此你不应该依赖它。

顺序执行的一个直接结果是异常处理方式。示例 1-86 显示了一个其中一个 `event` 订阅者抛出错误的示例。

示例 1-86. 触发事件时的异常





```cs
public class Pub
{
    public event EventHandler OnChange = delegate { };
    public void Raise()
    {
        OnChange(this, EventArgs.Empty);
    }
}

public void CreateAndRaise()
{
    Pub p = new Pub();

    p.OnChange += (sender,e )
        => Console.WriteLine("Subscriber 1 called");

    p.OnChange += (sender, e)
        => { throw new Exception(); };

    p.OnChange += (sender,e )
        => Console.WriteLine("Subscriber 3 called");

    p.Raise();
}

// Displays
// Subscriber 1 called
```

如你所见，第一个订阅者成功执行，第二个抛出了异常，而第三个则永远不会被调用。

如果这并不是你想要的行为，你需要手动触发 `events` 并处理发生的任何异常。你可以通过使用在 `System.Delegate` 基类上声明的 `GetInvocationList` 方法来实现这一点。示例 1-87 展示了获取订阅者并手动枚举它们的示例。

示例 1-87. 手动触发带异常处理的事件

```cs
public class Pub
{
    public event EventHandler OnChange = delegate { };
    public void Raise()
    {
        var exceptions = new List<Exception>();

        foreach (Delegate handler in OnChange.GetInvocationList())
        {
            try
            {
                handler.DynamicInvoke(this, EventArgs.Empty);
            }
            catch (Exception ex)
            {
                exceptions.Add(ex);
            }
        }

        if (exceptions.Any())
        {
            throw new AggregateException(exceptions);
        }
    }
}

public void CreateAndRaise()
{
    Pub p = new Pub();

    p.OnChange += (sender, e)
        => Console.WriteLine("Subscriber 1 called");

    p.OnChange += (sender, e)
        => { throw new Exception(); };

    p.OnChange += (sender, e)
        => Console.WriteLine("Subscriber 3 called");

    try
    {
        p.Raise();
    }
    catch (AggregateException ex)
    {
        Console.WriteLine(ex.InnerExceptions.Count);
    }
}

// Displays
// Subscriber 1 called
// Subscriber 3 called
// 1
```

### 更多信息：异常处理

有关如何处理异常的更多信息，请参见本章节后面标题为 目标 1.5: 实现异常处理 的章节。

## 思考实验

#### 构建一个松耦合系统

在思考实验中，请运用你关于该目标所学的知识。你可以在本章末的 答案 部分找到这些问题的答案。

你正在开发一个包含多个表单的桌面应用程序。这些表单显示相同数据的视图，并且它们应该实时更新。你的应用程序是可扩展的，第三方可以添加包含自己的数据视图的插件。

1. 在这个系统中，你应该使用委托还是事件？
2. 这如何帮助到你？

## 目标总结

- 委托是一种定义了方法签名并可以包含方法引用的类型。
- 委托可以实例化、传递和调用。
- Lambda 表达式（也称为匿名方法）使用 `=>` 运算符，形成了一种创建内联方法的紧凑方式。
- 事件是委托之上的一层语法糖，用于轻松实现发布-订阅模式。
- 事件只能从声明它的类中触发。事件的使用者只能向调用列表中添加或删除方法。
- 你可以通过添加自定义事件访问器并直接使用底层的委托类型来自定义事件。

### 目标回顾

回答以下问题以测试你对本目标中信息的掌握情况。你可以在本章末的 答案 部分找到这些问题的答案，以及对每个选项正确或错误的解释。

1. 你在类中有一个私有方法，并让某些调用者能够调用该方法。你应该做什么？
    1. 将该方法设为公共（public）。
    2. 使用事件，以便在方法执行时可以通知外部用户。
    3. 使用一个返回委托的方法提供给授权的调用者。
    4. 将私有方法声明为 lambda 表达式。

2. 你在类中声明了一个事件，并希望该类的外部用户能够触发此事件。你应该做什么？
    1. 将事件设为公共（public）。
    2. 在你的类中添加一个触发该事件的公共方法。
    3. 使用公共委托代替事件。
    4. 使用自定义事件访问器以给外部用户访问权限。

3. 你正在使用一个带有多个订阅者的多路委托。你想确保即使抛出异常，所有订阅者都能收到通知。你应该做什么？
    1. 使用 `GetInvocationList` 手动触发事件。
    2. 将触发事件的操作封装在 `try`/catch` 中。
    3. 什么都不做。这是默认行为。
    4. 让订阅者返回 `true` 或 `false` 而不是抛出异常。

# 目标 1.5: 实现异常处理

构建应用程序时，有时会发生错误。可能你想向磁盘写入文件，但磁盘满了。你尝试连接数据库，但服务器不可用或存在意外状况。.NET 框架不使用错误代码，而是使用异常来信号错误。你也可以这些异常来信号你应用程序中发生的错误，甚至可以自定义异常类型来信号特定错误。

了解如何处理异常是非常重要的，以便你实施良好的处理或引发错误的策略。

本目标涵盖了：

- 处理异常。
- 抛出异常。
- 创建自定义异常。

## 处理异常

当应用程序的某处发生错误时，会抛出 `exception`。与错误代码相比，`Exceptions` 本身就是一个对象，包含了发生错误的数据。它不仅有一个友好的消息，还包含发生的位置，甚至可以存储额外数据，例如指向帮助页面的地址。

如果 `exception` 未被处理，它将导致当前进程终止。示例 1-88 展示了一个抛出错误并关闭的应用程序示例。





为了处理 `exception`，你可以使用 `try/catch 语句`。示例 1-89 展示了捕获 `FormatException` 的示例。

### 示例 1-89. 捕获 `FormatException`

```c
using System;
namespace ExceptionHandling
{
    public static class Program
    {
        public static void Main()
        {
            while (true)
            {
                string s = Console.ReadLine();

                if (string.IsNullOrWhiteSpace(s)) break;

                try
                {
                    int i = int.Parse(s);
                    break;
                }
                catch (FormatException)
                {
                    Console.WriteLine("{0} is not a valid number. Please try again", s);
                }
            }
        }
    }
}
```

你需要将可能抛出异常的代码封装在 `try` 语句中。在 `try` 语句之后，你可以添加多个不同的 `catch 块`。在每个 `try 块` 中放置多少代码取决于具体情况。如果你有多个语句可能会抛出相同的异常但需要进行不同的处理，那么它们应该被放在不同的 `try 块` 中。

`catch 块` 可以指定它想要捕获的异常类型。由于 .NET Framework 中的所有异常都继承自 `System.Exception`，因此你可以通过捕获这个基类类型来捕获所有可能的 `exception`。你可以通过添加额外的 `catch 块` 来捕获更具体的 `exception` 类型。

`catch 块` 应该按照从最具体到最具体的顺序进行指定，因为运行时会按此顺序检查它们的。当抛出一个 `exception` 时，将执行第一个匹配的 `catch 块`。如果没有找到匹配的 `catch 块`，则异常将向下传递。示例 1-90 展示了捕获两种不同 `exception` 类型的示例。

如果 `string s` 为 `null`，则将抛出 `ArgumentNullException`。如果 `string` 不是数字，则将抛出 `FormatException`。通过使用不同的 `catch 块`，你可以以自己的方式处理这些异常。

### 示例 1-90. 捕获不同的 `exception` 类型

```c
try
{
    int i = int.Parse(s);
}
catch (ArgumentNullException)
{

    Console.WriteLine("You need to enter a value");
}
catch (FormatException)
{
    Console.WriteLine("{0} is not a valid number. Please try again", s);
}
```

在 C# 1 中，你也可以使用不带 `exception` 类型的 `catch 块`。这可以用于捕获从像 C++ 等语言抛出的异常，这些语言并不继承自 `System.Exception`（在 C++ 中你可以抛出任何类型的异常）。现在，每个不继承自 `System.Exception` 的异常都会被自动包装在 `System.Runtime.CompilerServices.RuntimeWrappedException` 中。由于此异常继承自 `System.Exception`，因此不再需要空的 catch 块了。

确保你的应用程序在 `catch 块` 完成时处于正确的状态是重要的。这可能意味着你需要撤销 `try 块` 在抛出异常之前所所的更改。

异常处理另一个重要功能是能够指定在发生异常时始终运行某些代码。这可以通过使用 `finally 块` 配合 `try` 或 `try/catch` 语句来实现。`finally 块` 无论是否发生异常都会执行。示例 1-91 展示了一个 `finally 块` 的示例。

### 示例 1-91. 使用 finally 块

```c
using System;

namespace ExceptionHandling
{
    public static class Program
    {
        public static void Main()
        {
            string s = Console.ReadLine();

            try
            {
                int i = int.Parse(s);
            }
            catch (ArgumentNullException)
            {
                Console.WriteLine("You need to enter a value");
            }
            catch (FormatException)

            {
                Console.WriteLine("{0} is not a valid number. Please try again", s);
            }
            finally
            {

                Console.WriteLine("Program complete.");
            }
        }
    }
}

// Displays
// a
// a is not a valid number. Please try again
// Program complete.
```

当然，仍然存在 `finally 块` 不会运行的情况。例如，当 `try 块` 进入无限循环时，它将永远不会退出 `try 块` 也永远不会进入 `finally 块`。在断电等情况下，没有其他代码将运行。整个操作系统将直接终止。

还有一种情况可以利用来防止 `finally 块` 运行。当然，这不是你想要经常使用的，但你可能会遇到这种情况，即直接关闭应用程序比运行 `finally 块` 更安全。

通过使用 `Environment.FailFast` 可以防止 `finally 块` 运行。该方法有两个不同的重载，一个只接受 `string`，另一个也接受 `exception`。当调用此方法时，消息（以及可选的异常）会被写入事件日志。示例 1-92 展示了你如何使用它。

### 示例 1-92. 使用 `Environment.FailFast`

```c
using System;
namespace ExceptionHandling
{
    public static class Program
    {
        public static void Main()
        {
            string s = Console.ReadLine();

            try
            {
                int i = int.Parse(s);
                if (i == 42) Environment.FailFast("Special number entered");
            }
            finally
            {
                Console.WriteLine("Program complete.");
            }
        }
    }
}
```

如果输入 `42`，则不会执行 `Program Complete`。相反，应用程序将关闭。

当你捕获异常时，可以使用一些属性来检查发生了什么。表 1-3 列出了基类 `System.Exception` 类的属性。

#### 表 1-3. `System.Exception` 属性

| 名称 | 描述 |
| --- | --- |
| `StackTrace` | 描述当前执行的所有方法的字符串。它为你提供了一种跟踪哪个方法抛出了异常以及如何到达该方法的方法。 |
| `InnerException` | 当由于另一个异常发生而抛出新异常时，这两个异常通过 `InnerException` 属性连接在一起。 |
| `Message` | 描述异常的（希望）人类友好的消息。 |
| `HelpLink` | 指向帮助文件的统一资源名称 (URN) 或统一资源定位符 (URL)。 |
| `HResult` | 一个描述错误严重程度、异常发生区域以及异常唯一数字的 32 位值。此值仅在跨越托管代码和非托管代码的界限时使用。 |
| `Source` | 引起错误的应用程序名称。如果未显式设置 `Source`，则使用程序集名称。 |
| `TargetSite` | 包含引起异常的方法名称。如果此数据不可用，该属性将为 `null`。 |
| `Data` | 键/值对字典，你可以用它为异常存储额外数据。这些数据可以被其他 catch 块读取，并用于控制对异常的处理。 |





在使用 `catch` 块时，你可以同时使用异常类型和命名标识符。通过这种方式，你实际上创建了一个变量来存储异常，以便你可以检查它的属性。示例 1-93 展示了如何进行操作。

### 示例 1-93. 检查异常

```c
using System;

namespace ExceptionHandling
{
    public static class Program
    {
        public static void Main()
        {
            try
            {
                int i = ReadAndParse();
                Console.WriteLine("Parsed: {0}", i);
            }
            catch (FormatException e)
            {
                Console.WriteLine("Message: {0}",e.Message);
                Console.WriteLine("StackTrace: {0}", e.StackTrace);
                Console.WriteLine("HelpLink: {0}", e.HelpLink);
                Console.WriteLine("InnerException: {0}", e.InnerException);
                Console.WriteLine("TargetSite: {0}", e.TargetSite);
                Console.WriteLine("Source: {0}", e.Source);
            }

        }

        private static int ReadAndParse()
        {
            string s = Console.ReadLine();
            int i = int.Parse(s);
            return i;
        }
    }
}

//Displays
//Message: Input string was not in a correct format.
//StackTrace:    at System.Number.StringToNumber(String str, NumberStyles options,
// NumberBuffer& number, NumberFormatInfo info, Boolean parseDecimal)
//   at System.Number.ParseInt32(String s, NumberStyles style,
//        NumberFormatInfo info)
//   at System.Int32.Parse(String s)
//   at ExceptionHandling.Program.ReadAndParse() in 
//      c:\Users\Wouter\Documents\Visual Studio 2012\Projects\
//        ExamRefProgrammingInCSharp\Chapter1\Program.cs:line 27
//   at ExceptionHandling.Program.Main() in c:\Users\Wouter\Documents\
//        Visual Studio 2012\Projects\ExamRefProgrammingInCSharp\
//        Chapter1\Program.cs:line 10
// HelpLink:
// InnerException:
// TargetSite: Void StringToNumber(System.String, System.Globalization.NumberStyles
// , NumberBuffer ByRef, System.Globalization.NumberFormatInfo, Boolean)
// Source: mscorlib
```

确保你的 `finally block` 不会导致任何异常是非常关重要的。当这种情况发生时，控制流会立即离开 `finally block` 并移动到下一个外层的 `try block`（如果存在）。原始异常将会丢失，你将无法再次访问它。

只有当你能够解决问题或想要记录错误时，才应该捕获异常。因此，避免在应用程序的底层使用通用的 `catch` 块是非常重要的。否则，你可能会在无意中吞掉一个重要的异常而甚至不知道它的发生。日志记录也应该在应用程序的较高位置进行。这样，你就可以避免在应用程序的多个层中重复记录错误。

## 抛出异常

当你想要抛出一个错误时，首先需要创建一个异常的新实例。然后你可以使用特殊的 `throw` 关键字来抛出该异常。之后，运行时将开始寻找 `catch` 和 `finally` 块。

示例 1-94 展示了你如何可以抛出异常。

### 示例 1-94. 抛出一个 `ArgumentNullException`

```c
public static string OpenAndParse(string fileName)
{
    if (string.IsNullOrWhiteSpace(fileName))
        throw new ArgumentNullException("fileName", "Filename is required");

    return File.ReadAllText(fileName);
}
```

你不应该尝试重用异常对象。每次抛出异常时，都应该创建一个新的异常，特别是在多线程环境中，因为异常的堆栈跟踪可能会被另一个线程更改。

在捕获异常时，你可以选择重新抛出（`rethrow`）异常。你有三种方法：

*   使用不带标识符的 `throw` 关键字。
*   使用带有原始异常的 `throw` 关键字。
*   使用带有新异常的 `throw` 关键字。

第一种选项在不修改调用栈的情况下重新抛出异常。当你不想对异常进行任何修改时，应该使用此选项。示例 1-95 展示了使用这种机制的示例。

### 示例 1-95. 重新抛出异常

```c
try
{
    SomeOperation();
}
catch (Exception logEx)
{
    Log(logEx);
    throw; // 抛出原始异常
}
```

当你选择第二种选项时，调用栈会被重置为代码中的当前位置。因此，你无法看到异常最初来自哪里，调试错误也会变得困难。

当你想要向代码的调用者抛出另一个异常时，使用第三种选项可能会有用。

例如，假设你正在开发一个订单应用程序。当用户下单时，你立即将此订单放入消息队列，以便另一个应用程序可以处理它。

当消息队列发生内部错误时，会抛出一个类型为 `MessageQueueException` 的异常。对于订单应用程序的用户来说，这没有任何意义。他们并不了解内部工作原理。

相反，你可以抛出另一个异常，例如自定义的 `OrderProcessingException`，并将 `InnerException` 设置为原始异常。在你的 `OrderProcessingException` 中，你可以为代码的用户放置额外信息，以提供上下文并帮助他们解决问题。示例 1-96 展示了一个示例。原始异常被保留（包括堆栈跟踪），并添加了包含额外信息的新异常。

### 示例 1-96. 抛出一个指向原始的异常

```c
try
{
    ProcessOrder();
}
catch (MessageQueueException ex)
{
    throw new OrderProcessingException("处理订单时出错", ex);
}
```

### 提示

在重新抛出异常时，确保不要吞掉任何异常细节。当你想添加额外信息时，抛出一个指向原始异常的新异常；否则，使用不带标识符的 `throw` 关键字来保留原始异常细节。

在 C# 5 中，增加了一种重新抛出异常的方法。你可以使用 `ExceptionDispatchInfo.Throw` 方法，它位于 `System.Runtime.ExceptionServices` 命名空间。该方法可以抛出异常并保留原始堆栈跟踪。你甚至可以在 `catch` 块之外使用此方法，如示例 1-97 所示。

### 示例 1-97. 使用 `ExceptionDispatchInfo.Throw`





```csharp
ExceptionDispatchInfo possibleException = null;

try
{
    string s = Console.ReadLine();
    int.Parse(s);
}
catch (FormatException ex)
{
    possibleException =  ExceptionDispatchInfo.Capture(ex);
}

if (possibleException != null)
{
    possibleException.Throw();
}

// Displays
// Unhandled Exception: System.FormatException: 
// Input string was not in a correct format.
//   at System.Number.StringToNumber(String str, NumberStyles options, 
//         NumberBuffer& number, NumberFormatInfo info, Boolean parseDecimal)
//   at System.Number.ParseInt32(String s, NumberStyles style, 
//         NumberFormatInfo info)
//   at System.Int32.Parse(String s)
//   at ExceptionHandling.Program.Main() in c:\Users\Wouter\Documents\
//      Visual Studio 2012\Projects\ExamRefProgrammingInCSharp\Chapter1\    
//         Program.cs:line  17
//--- End of stack trace from previous location where exception was thrown ---
//   at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
//   at ExceptionHandling.Program.Main() in c:\Users\Wouter\Documents\
//      Visual Studio 2012\Projects\ExamRefProgrammingInCSharp\Chapter1\
//         Program.cs:line 6
```

查看堆栈跟踪时，你会看到这一行，它显示了原始异常堆栈跟踪结束以及使用 `ExceptionDispatchInfo.Throw` 的地方：

```
--- End of stack trace from previous location where exception was thrown ---
```

当你想要在一个线程中捕获异常并在另一个线程中抛出时，可以使用此功能。通过使用 `ExceptionDispatchInfo` 类，你可以在线程之间移动异常数据并将其抛出。.NET Framework 在处理 C# 5 添加的 `async/await` 特性时使用了它。在 `async` 线程上抛出的异常会被并在执行线程上重新抛出。

### 更多信息：线程和 Async/Await

关于处理线程和新的 `async/await` 特性的更多信息，请参阅本章前面的章节目标 1.1: 实现多线程和异步处理。

在处理预期情况时，你不应该抛出异常。你知道当用户开始向你的应用程序输入信息时，他们会犯错。他们可能输入了格式错误的数字，或者忘记输入必填字段。对于这类预期的情况抛出异常是不推荐的。

异常处理改变了程序的正常预期流。这使得使用异常的代码更难以阅读和维护，特别是当它们在正常情况下被使用时。

使用异常还会会带来轻微的性能影响。因为运行时必须搜索所有外部 catch 块直到找到匹配的块，当未找到时，还必须检查是否附加了调试器，因此处理需要花费更多的时间。当发生会导致终止应用程序的真实意外情况时，这不是问题。但对于常规程序流，应该避免这样做。相反，你应该进行适当的验证，而不是仅仅依赖异常。

当你需要抛出自己的异常时，了解 .NET Framework 中已经定义了哪些异常非常重要。因为开发者会熟悉这些异常，所以应该尽可能使用它们。

某些异常仅由运行时抛出。你不应该在自己的代码中使用这些异常。表 1-4 列出了这些异常。

### 表 1-4. .NET Framework 中的运行时异常

| 名称 | 说明 |
| --- | --- |
| `ArithmeticException` | 算术运算期间发生的其他异常的基类。 |
| `ArrayTypeMismatchException` | 当你想在数组中存储不兼容的元素时抛出。 |
| `DivideByZeroException` | 当你尝试将值除以零时抛出。 |
| `IndexOutOfRangeException` | 当你尝试使用小于零或大于数组大小的索引访问数组时抛出。 |
| `InvalidCastException` | 当你尝试将元素转换为不兼容的类型时抛出。 |
| `NullReferenceException` | 当你尝试引用空元素时抛出。 |
| `OutOfMemoryException` | 创建新对象失败，因为 CLR 没有足够的可用内存时抛出。 |
| `OverflowException` | 在检查上下文（checked context）下算术运算溢出时抛出。 |
| `StackOverflowException` | 执行栈已满时抛出。这可能发生在没有退出的递归操作中。 |
| `TypeInitializationException` | 当静态构造函数抛出未处理的异常时抛出。 |

你不应该在自己的应用程序中抛出这些异常。表 1-5 显示了你可以使用的 .NET Framework 中的常用异常。

### 表 1-5. .NET Framework 中的常用异常

| 名称 | 说明 |
| --- | --- |
| `Exception` | 所有异常的基类。尝试避免抛出和捕获此异常，因为它太太通用了。 |
| `ArgumentException` | 当方法的参数无效时，抛出此异常。 |
| `ArgumentNullException` | `ArgumentException` 的特殊形式，当你的其中一个参数为空且不允许时，可以抛出异常。 |
| `ArgumentOutOfRangeException` | `ArgumentException` 的特殊形式，当参数超出允许的值范围时，可以抛出异常。 |
| `FormatException` | 当参数没有有效格式时，抛出此异常。 |
| `InvalidOperationException` | 当调用的方法对于对象的当前状态无效时，抛出此异常。 |
| `NotImplementedException` | 此异常通常用于生成的代码，其中方法尚未实现实现。 |
| `NotSupportedException` | 当调用了你不支持的方法时，抛出此异常。 |
| `ObjectDisposedException` | 当类的类的用户在 Dispose 已调用的情况下尝试访问方法时，抛出此异常。 |

在捕获和抛出异常时，你都应该避免直接使用 `Exception` 基类。相反，你应该尝试使用可的最特定异常。

### 创建自定义异常

一旦抛出异常变得很有必要，最好的办法是使用 .NET Framework 中定义的异常。但在某些情况下，你想要使用自定义异常。当编写你代码的开发者了解这些异常并能以比框架异常更特定的方式处理它们时，这尤为有用。

自定义异常应该继承自 `System.Exception`。你需要提供至少一个无参数构造函数。良好的实践做法是添加另外几个构造函数：一个接收 `string` 的，一个同时接收 `string` 和 `exception` 的，以及一个用于 `serialization` 的。示例 1-98 显示了自定义异常的示例。

示例 1-98. 创建自定义异常




```cs
[Serializable]
public class OrderProcessingException : Exception, ISerializable
{
    public OrderProcessingException(int orderId)
    {
        OrderId = orderId;
        this.HelpLink = "http://www.mydomain.com/infoaboutexception";
    }
    public OrderProcessingException(int orderId, string message)
        : base(message)
    {
        OrderId = orderId;
        this.HelpLink = "http://www.mydomain.com/infoaboutexception";
    }

    public OrderProcessingException(int orderId, string message, 
                                     Exception innerException)
        : base(message, innerException)
    {
        OrderId = orderId;
        this.HelpLink = "http://www.mydomain.com/infoaboutexception";
    }

    protected OrderProcessingException(SerializationInfo info, StreamingContext context)
    {
        OrderId = (int)info.GetValue("OrderId", typeof(int));
    }

    public int OrderId { get; private set; }

    public void GetObjectData(SerializationInfo info, StreamingContext context)
    {
        info.AddValue("OrderId", OrderId, typeof(int));
    }
}
```

按照惯例，命名所有自定义异常时，你应该使用 `Exception` 后缀。添加 `Serializable` 属性也是重要的，它确保了你的异常可以被序列化，并能在跨应用程序域之间正常工作（例如，当 Web 服务返回异常时）。

在创建自定义异常时，你可以决定想要存储哪些额外数据。通过属性暴露这些数据可以帮助异常的使用者检查发生了什么错误。

你不应该永远继承自 `System.ApplicationException`。最初的理念是所有 C# 运行时异常都应该继承自 `System.Exception`，而所有自定义异常都继承自 `System.ApplicationException`。然而，由于 .NET Framework 并没有遵循这种模式，该类变得毫无用并失去了意义。

## 思考实验

### 规划你的错误策略

在这个思考实验中，请应用你对本目标所学的知识。你可以在章节末尾的答案 部分找到这些问题的答案。

你正在设计一个新应用程序，并希望实现一种适当的错误处理策略。你正在与一些同事讨论这个话题，其中一人说你应该使用普通的错误代码来信号错误，因为那样速度更快，而且你的公司过去一直是这样做。

你还在讨论何时应该创建自定义异常，何时应该使用内置的 .NET Framework 异常。

1. 向你的同事解释异常与错误代码相比的优势。
2. 你在什么时候应该创建自定义异常？

## 目标总结

- 在 .NET Framework 中，你应该使用异常来报告错误，而不是错误代码。
- 异常是对象，其中包含了关于异常发生原因的数据。
- 你可以使用带有一个或多个 `catch` 块的 `try` 块来处理处理不同类型的异常。
- 你可以使用 `finally` 块来指定无论是否发生异常，都应该在之后始终运行的代码。
- 你可以使用 `throw` 关键字来抛出异常。
- 当你确定代码的使用者会以不同的方式处理异常时，你就可以定义自己的自定义异常。否则，你应该使用标准的 .NET Framework 异常。

### 目标复

回答以下问题以测试你对本目标信息的知识掌握情况。你可以在章节末尾的答案 部分找到这些问题的答案，以及对每个选项为何正确或错误的解释。

1. 你正在检查方法的参数是否存在非法的 `null` 值。如果你遇到了 `null` 值，你会抛出哪种异常？
    1. `ArgumentException`。
    2. `InvalidOperationException`。
    3. `NullReferenceException`。
    4. `ArgumentNullException`。

2. 当无法访问文件时，你的代码捕到了 `IOException`。你想给调用者提供更多信息。你应该做什么？
    1. 修改异常的消息并重新抛出异常。
    2. 抛出一个带有额外信息的新异常，并将 `IOException` 作为 `InnerException`。
    3. 抛出一个带有更详细信息的异常异常。
    4. 使用 `throw` 重新抛出异常并保存调用栈。

3. 你正在创建一个名为 `LogonFailedException` 的自定义异常。你至少应该添加哪些构造函数？（选择所有适用）
    1. `LogonFailed()`
    2. `LogonFailed(string message)`
    3. `LogonFailed(string message, Exception innerException)`
    4. `LogonFailed(Exception innerException)`

## 章节总结

- 多线程可以帮助你创建响应迅速且可扩展的程序。你可以使用 `TPL`、`Parallel` 类和 `PLINQ` 来实现这一点。新的 `async`/`await` 关键字帮助你编写异步代码。
- 在多线程环境中，管理共享数据的同步至关重要。你可以通过使用 `lock` 语句来实现。
- C# 提供了用于决策的语句——`if`、`switch`、条件运算符（`?`）和空合并运算符（`??`）；迭代（`for`、`foreach`、`while`、`do-while`），以及跳转语句（`break`、`continue`、`goto`、`return` 和 `throw`）。
- 委托是指方法的对象。Lambda 表达式是创建匿名方法的简化语法。
- 事件是基于委托的。
异常是 .NET Framework 处理错误的首选方式。

## 答案

本节包含思考实验的解决方案和课程复习的答案。

### 目标 1.1: 思考实验

1. 多线程可以提高客户端应用程序的响应能力。UI 线程可以处理用户请求，而后台线程执行操作。
2. CPU 密集型操作需要线程执行。在客户端应用程序中，将 CPU 密集型操作放在另一个线程执行是合理的。在服务器应用程序中，你不希望为 CPU 密集型操作准备额外的线程。异步 I/O 操作在执行时不需要线程。释放当前线程执行其他工作可以提高可扩展性。

### 目标 1.1: 复

1. 正确答案：B。手动创建和管理任务是不必要的。`Parallel` 类会处理这些并使用最佳配置选项。
2. 正确答案：A。`For` 适用于对执行大量工作的项目集执行并行操作。
3. 正确答案：C。`async`/`await` 并不并发处理项目。相反，它等待当前任务完成后继续执行代码。




4. **错误：** `WithDegreeOfParallelism` 用于指定并行查询应该使用的线程数。

3. **正确答案：** C

1. **错误：** 因为你必须等待外部因素（数据库和 Web 响应），所以你应该使用 `async/await` 来释放你的线程。这样，你的线程可以在等待外部响应返回的同时执行其他工作。
2. **错误：** `async/await` 可以用于提高客户端的响应性，但也可以用于服务器场景。特别是在等待 I/O 密集型操作时，你可以使用异步代码来释放线程免于等待。
3. **正确：** 操作系统等待 I/O 请求完成，然后激活一个可以处理响应的线程。在此期间，线程可以执行其他工作。
4. **错误：** 在 I/O 密集型情况下，`async/await` 不会让你的线程睡眠。相反，当操作系统监控请求状态时，你的线程可以处理其他工作。当请求完成时，将使用一个线程处理响应。对于 CPU 密集型操作，你的线程会等待另一个线程上的操作完成。

### 目标 1.2: 思考实验

1. 确保在锁定多个对象时，所有的锁定都遵循相同的顺序是非常重要的。一旦你开始以不同的顺序锁定依赖对象，就会开始出现死锁。
2. `Interlocked` 类可以帮助你执行微小的、原子的操作，而不需要锁定。当你对这类操作频繁使用锁时，可以将它们替换为 `Interlocked` 语句。

## 目标 1.2: 复习

1. **正确答案：** D

1. **错误：** 你永远不应该在此上进行锁定。你代码的其他部分可能已经在使用你的对象来执行锁。
2. **错误：** 你不应该使用字符串进行锁定。由于字符串内插（string-interning），一个对象可以用于多个字符串，因此你锁定的对象可能在其他地方也被使用。
3. **错误：** 在值类型上锁定将产生编译错误。值类型每次被锁定时都会被装箱（boxed），导致每次产生一个唯一的锁。
4. **正确：** `object` 类型的私有锁是最佳选择。

2. **正确答案：** B

1. **错误：** `CancellationTokenSource` 用于生成 `CancellationToken`。令牌应该传递给任务，然后可以使用 `CancellationTokenSource` 请求取消该令牌。
2. **正确：** 由 `CancellationTokenSource` 生成的 `CancellationToken` 应该传递给任务。
3. **错误：** 布尔变量可以用于取消任务，但这不是首选方法。`CancellationToken` 提供了更大的灵活性并应该被使用。
4. **错误：** 应该使用 `volatile` 关键字向编译器信号，字段上的读写顺序是重要的，并且编译器不应该改变它。

3. **正确答案：** B

1. **错误：** `Volatile.Write` 用于向编译器信号，向字段写入值应该发生在那个精确的位置。
2. **正确：** `CompareExchange` 将检查当前状态是否正确，然后会在一个原子操作中将其更改为新状态。
3. **错误：** `Exchange` 只更改值；它不会检查当前状态是否正确。
4. **错误：** `Decrement` 用于在原子操作中将值减去 1。

### 目标 1.3: 思考实验

1. 使用 `goto` 语句会让你的代码变得难以阅读，因为应用程序流会来处跳转。`goto` 主要用于循环语句。你随后可以将 `goto` 替换为 `while` 或 `do-while`。
2. `switch` 语句可以改进长长的 `if` 语句。
3. `for` 语句可以使用 `index` 遍历集合。你可以在迭代时修改集合。你需要使用 `index` 来检索每个项。`foreach` 是迭代器模式的语法糖。你不使用 `index`；相反，编译器给你一个指向每次迭代项的变量。

## 目标 1.3: 复习

1. **正确答案：** C

1. **错误：** `switch` 用作决策语句。你将值映射到某些标签以执行特定的代码；它不会遍历集合。
2. **错误：** 虽然 `foreach` 语句可以用于遍历集合，但它不允许在迭代期间更改集合。
3. **正确：** 使用 `for`，你可以在修改集合的同时遍历它。确保 `index` 保持正确是你自己的工作。
4. **错误：** `goto` 是一个应该避免的跳转语句。

2. **正确答案：** D

1. **错误：** `for` 是一个迭代语句，不能用于检查 `null` 值。
2. **错误：** 条件运算符可以用于缩短 `if` 语句。条件地调用方法没有用处。
3. **错误：** 空合并运算符确实会检查 `null` 值，但它是用于提供默认值的。当值不为 `null` 时，调用方法它没有用处。
4. **正确：** 短路允许你查看左侧是否为 `null`。如果左侧为 `null`，右侧操作数将不会执行。

3. **正确答案：** B

1. **错误：** `for` 在遍历已知数量集合时最有用。
2. **错误：** `foreach` 只能用于实现 `IEnumerable` 的类型。
3. **正确：**
```
while (o.Next) {
    var i = o.Read();
}
```
当 `o.Next` 返回 `false` 时，循环自动结束。
4. **错误：** `Do-while` 至少执行一次代码。如果没有项目，代码将不需要执行。

### 目标 1.4: 思考实验

1. 事件是委托之上的一个很好的层，使得它们更易用、更安全。在这种情况下，你应该使用事件来确保其他用户无法清除订阅。它还确保了他们无法引发事件。他们只能监听变化。
2. 在此类应用程序中使用事件的优势是可以实现松散耦合。你的表单不需要了解对方的任何信息。监控数据变化并引发事件的类不需要知道有多少表单在监听以及它们长什么样。第三方插件可以在运行时轻松订阅事件，以便响应变化而不与现有系统紧密耦合。

## 目标 1.4: 复习

1. **正确答案：** C

1. **错误：** 将方法设为公有会给类的所有用户访问权限。
2. **错误：** 这没有给类用户提供执行方法的能力。
3. **正确：** 方法可以查看调用者是否授权，然后返回一个指向私有方法的委托，可以随意调用。
4. **错误：** 将方法更改为 lambda 并没有改变外部用户无法访问该方法的事。

2. **正确答案：** B

1. **错误：** 编译器限制了事件在其定义类之外的使用。它们只能添加和删除订阅者。只有类本身可以引发事件。
2. **正确：** 公有方法可以由类的外部用户调用。在内部它可以引发事件。
3. **错误：** 使用委托允许它从类外部被调用。然而，你丢失了事件为你提供的保护。公有委托可以被外部用户无限制地完全修改。





4. **错误：** 规范名称（CNAME）记录将别名或昵号映射到可能位于当前区域之外实际或规范名称。

3. **正确答案：** A
    1. **正确：** 你可以处理每个单独的错误并确保所有订阅者都被调用。
    2. **错误：** 将触发事件的语句封装在一个 `try`/`catch` 块中仍然会导致调用在第一个异常处停止。后续的订阅者将收不到通知。
    3. **错误：** 默认情况下，当其中一个订阅者发生第一个未处理的异常时，订阅者的调用将停止。
    4. **错误：** 异常是处理错误的首选方式。从每个事件返回值仍然需要你手动逐一调用它们以检查返回值。

## 目标 1.5：思想实验

1. 异常是对象，因此它们可以存储仅凭错误代码无法实现的额外信息。.NET Framework 还为处理异常提供了特殊支持。例如，你可以使用 `catch` 块来处理特定类型的异常，并可以使用 `finally` 块来确保某些代码始终运行。
2. 只有当你预计开发者会处理它或执行自定义日志时，你应该创建自定义异常。如果开发者无法修复特定错误，那么创建一个更具体的异常是没有意义的。抛出更详细的异常时可以进行自定义日志，以便开发者区分不同发生的错误。

## 目标 1.5：复习

1. **正确答案：** D
    1. **错误：** 虽然异常与你方法的参数有关，但你应该抛出更具体的 `ArgumentNullException`。
    2. **错误：** 当你的类不处于处理请求的正确状态时，应该使用 `InvalidOperationException`。
    3. **错误：** 当你尝试引用 `null` 值时，运行时会抛出 `NullReferenceException`。
    4. **正确：** `ArgumentNullException` 是你可以使用的最专门的异常，用于告诉 string 哪个参数是 `null` 以及你期望什么。
2. **正确答案：** B
    1. **错误：** 异常的 `Message` 属性是只读的。你无法在异常创建后更改它。
    2. **正确：** 新异常可以包含额外信息。设置 `InnerException` 可以确保原始异常仍然可用。
    3. **错误：** 抛出一个全新的异常会丢失原始异常及其包含的信息。
    4. **错误：** 使用不带标识符的 `throw` 将重新抛出原始异常并保持堆栈跟踪，但它不会添加任何额外信息。
3. **正确答案：** A, B, C
    1. **正确：** 你应该始终添加一个默认的空构造函数。
    2. **正确：** 第二个构造函数应该接收一个关于错误原因的描述性消息。
    3. **正确：** 可以设置 `InnerException` 来关联两个异常并显示原始 `error` 是什么。
    4. **错误：** 你不需要定义一个只接受 `InnerException` 而不带消息的构造函数。

# 第 2 章：创建和使用类型

作为一名工匠，了解你的工具对于完成工作非常重要。在构建面向对象的软件时，类型就是你的工具。熟练创建实用的类型可以是成功项目与灾难之间的区别。C# 提供了创建类型所需的所有基本构建模块，这些类型可以作为任何软件项目的基础。

在本章中，你将学习 C# 在创建类型方面提供的功能。你将学习如何创建你和同事易于使用的类型，这些类型封装了内部工作机制，以便你专注于以最佳方式使用它们。

在学习了如何创建类型之后，你将检查 C# 作为受托管环境意味着什么，以及在使用未管理的外部资源时如何与其良好共处。最后，你将查看如何使用 .NET Framework 某些类型，并与内置的字符串类型一起工作。

**本章目标：**

* 目标 2.1：创建类型
* 目标 2.2：消费类型
* 目标 2.3：强制封装
* 目标 2.4：创建并实现类层次结构
* 目标 2.5：通过反射在运行时查找、执行和创建类型
* 目标 2.6：管理对象生命周期
* 目标 2.7：操作字符串

## 目标 2.1：创建类型

编写应用程序由类型组成。在 C# 中，创建类型有很多选项。了解你的选项将使你能够明智地做出选择。在本节中将学习 C# 提供了哪些功能以及何时使用。本目标涵盖了如何：

* 选择类型。
* 创建易于使用的类型。
* 扩展现有类型。

## 选择类型

在像 C# 这样的面向对象的语言中，对象和类型是基础块。类型可以被视为构建对象的蓝图。它展示了可以使用哪些数据以及哪些行为。创建这些蓝图并使用它们构造新对象使你能够构建复杂的应用程序。C# 允许你根据情况选择类型。

### C# 中的类型

C# 类型系统包含三个不同的类别：

* 值类型
* 引用类型
* 指针类型

指针类型很少使用。只有当你处理不安全代码并需要使用指针运算时才会使用它们。

### 更多信息：指针和不安全代码

有关更多信息，请阅读 `http://msdn.microsoft.com/en-us/library/chfa2zb8.aspx` 中的“unsafe (C# Reference)”。

## 创建枚举

一种基本类型是枚举 `enum`。它为你提供了一种创建可选列表的好方法。

```
public enum Gender { Male, Female }
```

当然，你可以使用布尔值（如 `IsMale` 为 `true` 或 `false`）来表示性别。但当你读取和处理使用该布尔值的代码时，你必须将真假值映射到性别的实际含义。使用枚举可以提高代码的可读性。

默认情况下，第一个元素的值为 0，随后的每个元素递增 1，但你可以更改起始索引和底层类型。在以下示例中，你定义了一个具有字节类型且从 1 开始的枚举。当然，这是你应该告知团队的事情，让他们知道更改了默认行为：

```
enum Days : byte { Sat = 1, Sun, Mon, Tue, Wed, Thu, Fri };
```





如果你想将 `Days` 枚举与底层的 `byte` 值进行比较，你必须将其强制转换为 `byte`：

```
Days day = Days.Sat;
if ((byte)day == 1) { }
```

枚举也可以配合特殊的 `Flags` 属性使用；你可以使用一个枚举来设置多个值的组合。示例 2-1 展示了如何进行此操作。

示例 2-1. 为枚举使用 `FlagAttribute`

```csharp
[Flags]
enum Days
{
    None = 0x0,
    Sunday = 0x1,
    Monday = 0x2,
    Tuesday = 0x4,
    Wednesday = 0x8,
    Thursday = 0x10,
    Friday = 0x20,
    Saturday = 0x40
}
Days readingDays = Days.Monday | Days.Saturday;
```

### 更多信息：使用和创建属性

关于如何使用属性的更多信息，请参阅本文后后的“目标 2.5：通过反射在运行时查找、执行和创建类型”。

### 值类型和引用类型

枚举只是开始。枚举是一种特殊的`value type`。C# 拥有值类型和引用类型。两者在 C# 编程语言和 .NET Framework 中都被广泛使用。创建新类型时，了解它们之间的区别很重要，这样你才能做出明智的决定。

你可能已经编程了一段时间并习惯了使用引用类型，但还没有创建过自定义的值类型。因此，关于值类型与引用类型之间存在很多误解。引用类型顾如其名，包含指向真实值的引用；值类型直接包含该值。引用类型的一个示例是统一资源定位符 (`URL`)）。如果你在网上读到一些有趣的内容，可以将 `URL` 发给朋友，指向存储信息的正确位置。值类型则不同。如果你在杂志上读到一篇有趣的文章并想把它给朋友，你需要复制文章并直接交给他们。

这种行为在值类型和引用类型中也可以看到。在支持 C# 的公共语言运行时 (`CLR`) 中，类型可以存储在内存中的两个位置：`heap`（堆）和`stack`（栈）。引用类型的值存储在堆上，而指向该值的地址存储在栈上。虽然值类型通常存储在栈上，但也有例外（例如，包含值类型作为其字段之一的类、闭获值类型的 lambda 表达式，或被装箱的值类型），但这就是大致的概念。在栈上存储数据的好处是它速度更快、占用空间更小，且不需要垃圾回收器的关注。

### 更多信息：垃圾回收器和堆

更多信息，请阅读本文后章节的目标 2.6：管理对象的生命周期 部分。

对于属于在一起的小数据结构，值类型非常有用。例如，具有 x 和 y 坐标的点就是值类型的候选对象。根据经验法则，你可以通过检查以下三个标准来判断是否想要创建一个值类型：

*   对象很小。
*   对象在逻辑上是不可变的。
*   对象有很多。

当然，这些仍然是模糊的要求。唯一能决定你是否需要值类型的是你自己。如果你正在针对速度或内存使用进行优化，那么确定值类型是否能提高性能的方法就是测量。

C# 中的所有对象都继承自 `System.Object`。然而，值类型继承自 `System.ValueType`（该类型继承自 `System.Object`）。`System.ValueType` 重写了某些默认函数（如 `GetHashCode`、`Equals` 和 `ToString`），为值类型提供了了更有意义的实现。

在 C# 中，你不能直接继承自 `System.ValueType`。相反，你可以使用 `struct` 关键字创建一个新的值类型。示例 2-2 展示了你如何创建一个包含点坐标的 `struct`。

示例 2-2. 创建自定义结构体

```csharp
public struct Point
{
    public int x, y;

    public Point(int p1, int p2)
    {
        x = p1;
        y = p2;   
   }
}
```

结构体和类可以拥有方法、字段、属性、构造函数和其他功能。然而，你不能为结构体声明自己的空构造函数。此外，结构体不能用于继承层次结构（这可以为你节省一些内存字节！）。

### 考试提示

了解 C# 中可用的不同类型是重要的。值类型应该用于小型、不可变且被频繁使用的对象。在所有其他情况下，请使用引用类型。

### 为你的类型添加主体内容

在你决定了想要创建值类型还是引用类型之后，就可以开始考虑你的类型主体了。你可能并不是一开始就创建一个空结构体。你的新类型的目标是封装数据，以便供程序的其他部分使用。你创建的类型就像一个蓝图。

### 添加行为

代码的其他部分可以调用方法来执行行为。例如，如示例 2-3 所示所示展示了它是如何工作的。

示例 2-3. 调用方法

```csharp
namespace CallingAMethod
{
    class Program
    {
        static void Main(string[] args)
        {
            System.Console.WriteLine("I'm calling a method!");
        }
    }
}
```

对 `Console.WriteLine` 的调用执行了 `Console` 类上的 `WriteLine` 函数，并传递了一个字符串参数。在你自己的类型中添加方法时，重要的步骤如下：

1.  为你的方法选择一个名称。
2.  决定哪些数据应该传递给你的方法。
3.  决定你想返回给调用者哪些数据。
4.  决定你方法的可见性。

如果你想创建一个能够将两个数字相加的 `Calculator` 类，你的方法签名看起来是什么样的？示例 2-4 展示了 `Calculator` 的基本实现。

示例 2-4. 创建方法

```csharp
class Calculator
{
    public int Add(int x, int y)
    {
        return x + y;
    }
}
```

`Add` 名字清楚地说明了该方法的作用。在阅读类的方法名时，你应该能够在不看实现代码的情况下理解它的作用。

### 注意：“函数”与“方法”

有时使用“函数”（function），有时使用“方法”（method）。函数意味着它返回一个值且不修改任何内容。这是系统的“读”部分。这在 F# 等函数式语言中仍然流行。

方法允许修改数据且不返回任何数据。这是系统的“写”部分。你可以在 .NET Framework 添加的 `Func<T>` 和 `Action` 类型中看到这种区别。`Func<T>` 始终有一个返回类型，而 `Action` 不返回内容。在 C# 中，不使用这种区分。首选术语是“方法”。




这可以提高你代码的质量。在使用过程式风格编写代码时，你可能会掉入陷阱，创建一个运行所有各种操作的巨型方法。这会导致代码的可读性和维护性降低。面向对象的软件是相对于过程式编码的范式转变。通过使用对象，你可以创建出更有意义的代码，并且应该更容易维护。但仍然可能出现你像编写过程式代码一样编写面向对象的应用程序的情况。将大型、复杂的方法拆分为各个部分，并明智地为这些方法命名，是你在面向对象系统中避免过程式方法时可以采取的步骤之一。确保你的方法名专注于一件事。如果你的方法开始变得臃肿且你很难为它命名，请考虑通过将其拆分为多个具有各自特定目标的方法来简化你的方法。

`Add` 方法有两个`arguments`：`x` 和 `y`。为你的参数命名也很重要。当使用 Visual Studio 时，你方法的使用者（可能是几天、几周或几个月后的你！）通常依赖 IntelliSense 来检查你的方法期望接收哪些参数。良好的参数名称有助于他人使用你的方法，因为对他们来说，你期望什么是清晰可见的。

在决定接收哪些参数时，考虑你将如何处理这些数据非常重要。查看示例 2-5 和示例 2-6 所示示例。

#### Example 2-5. 将一个完整的客户传递给方法

```
public Distance CalculateDistanceTo(Customer customer)
{
    Distance result =  ... // 使用 customer.Address 的某些复杂计算
    return result;
}
```

####  2-6. 仅将地址传递给方法

```
public Distance CalculateDistanceTo(Address address)
{
    Distance result = ... // 使用 address 的某些复杂计算
    return result;
}
```

你应该选择哪种方法？示例 2-5 中方法的问题在于 `Customer` 对象仅被用于检索地址。突然之间，距离计算算法耦合到了 `Customer` 上。`Customer` 类的更改（例如添加收货地址和账单地址）将影响到这个类。

示例 2-6 只请求了它需要的数据。这是一个更清晰、更简单的设计，提高了可维护性。

### 更多信息：职责忧律 (Law of Demeter)

这种模式被称为职责忧律。有关如何选择参数的更多信息，请阅读位于**[`msdn.microsoft.com/en-us/magazine/cc947917.aspx#id0070040`](http://msdn.microsoft.com/en-us/magazine/cc947917.aspx#id0070040)*。

### 命名参数、可选参数和重载可见性

C# 4 的一个新特性是使用`named`（命名）和`optional`（可选）参数。可选参数允许你省略某些参数的参数。命名参数用于指定你想要为哪些参数传递值。命名参数和可选参数可以用于方法、索引器、构造函数和委托。当你想要为某些参数指定默认值时，可选参数非常有用。示例 2-7 显示了如何使用命名和可选参数。

#### Example 2-7. 使用命名参数和可选参数

```
void MyMethod(int firstArgument, string secondArgument = "default value",
    bool thirdArgument = false) { }

void CallingMethod()
{
    MyMethod(1, thirdArgument: true);
}
```

同样可以创建名称相同但接收参数不同的方法，这被称为`overloading`（重载）。.NET Framework 中的一个示例是 `Console.WriteLine`。该方法有 19 种不同的重载，接收不同的参数。你通过使用完全相同的名称和返回类型，但在期望的参数上不同，来为方法创建一个重载。

在创建方法时，你可以选择是否向调用者返回一个值。如果你不想返回一个值，可以将方法的返回类型声明为 `void`。如果你想返回一个值，则需要指定你想返回的类型。示例 2-8 显示了如何创建一个 `void` 方法和一个返回数据的方法。

### Example 2-8. 从方法返回数据

```
public void MethodWithoutAnyReturnValue()
{ /* 不向调用者返回任何值 */ }

public int MethodWithReturnValue()
{
    return 42;
}
```

在创建方法时，决定方法的可见性至关重要。当你没有声明访问修饰符时，你的方法默认是 `private`（私有的）。其他选项包括 `public`（公共的）、`internal`（内部的）。

##### 更多信息：访问修饰符

有关访问修饰符的更多信息，请阅读本章后面的目标 2.3：封装。

### 添加数据

`Calculator` 类中像 `Add` 这样的方法只使用传递的数据。然而，类可以包含行为和数据。在类内部存储数据最简单的方法是使用 `field`（字段），它提供了对值的访问。示例 2-9 显示了如何使用字段。

### Example 2-9. 定义并使用字段

```
public class MyClass
{
     public string MyInstanceField;

     public string Concatenate(string valueToAppend)
     {
         return MyInstanceField + valueToAppend;
     }
}

MyClass instance = new MyClass();
instance.MyInstanceField = "Some New Value";
```

与方法一样，字段可以拥有访问修饰符、类型和名称。命名与方法的命名同样重要。清晰的描述性名称可以提高代码质量。字段可以标记为 `read-only`，允许在对象构造期间设置一次。你可以在构造函数或声明变量时进行设置。之后，字段的值无法更改。

如果字段的值在编译时设置，你还可以将其标记为 `const`（常量）。这样，编译器就能确定该值永远不会改变，并可以进行优化。这还确保你不会意外覆盖字段的值。代码中对字段的所有赋值都会导致编译错误。




如果你想访问特定的卡片，可以通过 `Cards` 属性来访问，但这并不总是很方便。这就是为什么 C# 有了*索引器属性（indexer properties）*。索引器属性允许你的类像普通数组一样通过索引进行访问。在 .NET Framework 中，可以在 `List<T>` 集合类型找到索引器属性的示例。你可以声明一个新的 `List<int>`，用一些值对其进行初始化，并按照以下方式访问第一个元素：

```
List<int> myList = new List<int>() { 1, 3, 5 };
myList[0] = 1;
```

你可以使用 `[]` 符号来访问列表内部的元素。你也可以在自己的类中实现这一功能。对于 `Deck` 类，使用以下代码：

```
public Card this[int index]
{
    get { return Cards.ElementAt(index); }
}
```

到到目前为止，所有属性都声明为实例字段。每个对象实例都有它自己的属性，且每个属性的值都与其他实例相互独立。当你想要存储不特定于实例的数据时，可以将其标记为静态的（static），如下所示：

```
class MyClass
{
    public static int MyStaticField = 42;
}
```

`MyStaticField` 与 `MyClass` 的特定实例解耦。要访问该字段，不需要创建新实例。相反，你可以直接访问它：

```
MyClass.MyStaticField = 43;
```

静态字段或属性会被所有访问它的代码共享。这可能会导致一些危险的副作用，因为如果你在某处更改了静态值，所有访问该字段的代码都会随之改变。

静态也可以用于方法。同样的原理适用于：你不需要创建类的实例即可访问静态方法。如果一个类中的所有方法都是静态的，那么整个类都可以声明为静态的。

### 使用蓝图

在你创建了带有所有属性和方法的类型后，就可以开始使用它了。创建类的实例是通过使用 `new` 操作符完成的。在对象上调用 `new` 会执行该对象的*构造函数（constructor）*。默认情况下，每个类都有一个可以调用的空构造函数。你也可以定义自己的构造函数。你这样做有两个原因：

* 用数据初始化该类型
* 运行一些初始化代码

查看示例 2-11*中的卡片示例。

示例 2-11. 为你的类型添加构造函数

```
class Deck
{
    private int _maximumNumberOfCards;

    public List<Card> Cards { get; set; }

    public Deck(int maximumNumberOfCards)
    {
        this.maximumNumberOfCards = maximumNumberOfCards;
        Cards = new List<Card>();
    }

    // 类的其余部分
}
```

正如你在示例 2-11*中所示，构造函数接受一个 `int` 类型的参数。当你想要实例化该类的新实例时，你需要向构造函数传递一个值：

```
Deck deck = new Deck(5);
```

构造函数还会运行一些代码以确保对象处于可用状态。设计构造函数时的一些良好实践如下：

* 如果类需要这样的公共默认构造函数，请显式声明它。
* 确保你的构造函数参数的尽可能少。
* 将构造函数参数映射到类中的属性。
* 在适当的情况下从实例构造函数中抛出异常。
* 不要从对象的构造函数内部调用虚拟成员。

### 更多信息：设计构造函数的最佳实践

如果你想了解更多设计构造函数的最佳实践，请参考*[`msdn.microsoft.com/en-us/library/vstudio/ms229060(v=vs.100).aspx`](http://msdn.microsoft.com/en-us/library/vstudio/ms229060(v=vs.100).aspx)*。

类也可以有多个构造函数，这些构造函数可以相互链接（chain），这样就可以避免重复代码。示例 2-12*展示了你如何链接多个构造函数。

示例 2-12. 构造函数链

```
class ConstructorChaining
{
    private int _p;

    public ConstructorChaining() : this(3) { }
    public ConstructorChaining(int p)
    {
        this._p = p;
    }
}
```

在生产代码中，明确你类的类的使用者应该使用哪个构造函数是重要的。你可以通过选择有意义的参数名称并添加解释每个构造函数用途的注释来实现。

### 设计类

在设计新类时，你应该记住几个关键的设计原则。这些原则可以帮助你设计出易于使用、维护和扩展的类。不遵守这些原则会导致代码库开始*腐烂（rot）*，并最终变成一个*大泥球（big ball of mud）*——一个缺乏可感知架构的系统。

所有原则都归结为确保你的代码具有两个特征：

* 高内聚（High cohesion）
* 低耦合（Low coupling）

这些原则意味着代码在不需要时不应该依赖于其他代码。

一个重要的原则列表由缩写 SOLID 表示。表 2-1*解释了每个字母的含义。

表 2-1. SOLID 设计原则

| 字母 | 代表 | 描述 |
| --- | --- | --- |
| S | 单一职责原则 | 类应该只有一个职责。例如，一个类不应既负责保存到数据库又负责显示用户。 |
| O | 开闭原则 | 对扩展开放，对修改关闭。例如，通过通用接口，新对象可以与现有代码集成。 |
| L | 氏夫替换原则 | 基类在任何情况下都应该是子类的替换。例如，鸭子可以游泳，而电动鸭只有在电池充足时才能游泳。 |
| I | 接口隔离原则 | 使用特定的接口而不是一个通用接口。接口的用户不需要实现所有用到的方法。 |
| D | 依赖倒置原则 | 依赖抽象而不是具体实现。例如，当你在类中使用 `SomeServiceType` 时，你不应该依赖于具体实现。相反，你应该依赖接口或抽象类。 |

### 更多信息：设计原则

如果你想了解更多关于大泥球原则的内容，请查看*[`www.codinghorror.com/blog/2007/11/the-big-ball-of-mud-and-other-architectural-disasters.html`](http://www.codinghorror.com/blog/2007/11/the-big-ball-of-mud-and-other-architectural-disasters.html)*。

关于设计高内聚和低耦合系统的更多信息可以在[`msdn.microsoft.com/en-us/magazine/cc94717.aspx`](http://msdn.microsoft.com/en-us/magazine/cc94717.aspx)找到。

## 使用泛型类型

C# 2.0 添加的一新功能是*泛型（generics）*。泛型类型使用*类型参数（Type parameter）*而不是硬编码所有类型。





在 .NET Framework 中，泛泛型应用的一个领域是对 `Nullables`（可空类型）的支持。引用类型可以有一个实际的空值 null，意味着它没有值。然而，值类型不能具有 `null` 值。例如，你如何表达某个 `Boolean` 值为真、假或未定义呢？普通的 `Boolean` 只能是真或假。

这就是为什么 .NET Framework 添加了 `Nullables` 的原因。`Nullable` 是对值类型的包装，并带有一个 `Boolean` 标志，用于指示该 `Nullable` 是否设置了值。示例 2-13 是 .NET Framework 中 `Nullable` 支持的简化版本。

示例 2-13. 泛型 `Nullable<T>` 的实现

```
struct Nullable<T> where T : struct
{
  private bool hasValue;
  private T value;

  public Nullable(T value)
  {
    this.hasValue = true;
    this.value = value;
  }

  public bool HasValue { get { return this.hasValue; } }

  public T Value
  {
    get
    {
      if (!this.HasValue) throw new ArgumentException();
         return this.value;
    }
  }

  public T GetValueOrDefault()
  {
    return this.value;
  }
}
```

现在不再需要为每种可能的值类型创建一个 `Nullable` 类型，而是只有一个使用泛型类型参数的实现，使其更具活性。通过这种方式，可以使用泛型来促进代码复用。

通常，值类型需要装箱（boxed）才能在非泛型集合中使用。通过使用泛型，你可以避免装箱和拆箱带来的性能开销。

### 更多信息：装箱和拆箱

欲需更多信息，请参阅本章后后的 目标 2.2: 使用类型。

.NET Framework 在 `System.Collections.Generic` 命名空间中提供了多个集合类的泛型实现。只要可能，就应该使用这些泛型集合而不是它们的非泛型对应项。

C# 使用泛型有许多可能性。它们可以用于 `structs`、`classes`、`interfaces`、`methods`、`properties` 和 `delegates`。在必要时，你甚至指定多个泛型类型参数。

正如 `Nullable<T>` 示例所示，泛型类型参数也可以被“约束（constrained）”。在 `Nullable<T>` 的情况下，如果 `T` 可以是引用类型，将没有任何意义。引用类型根据其本质已经具有了为 null 的选项。

C# 允许你添加简单的 `where 子句` 来约束类型参数。在表 2-2 中，你可以看到可以使用的不同约束。

表 2-2. 泛型类型参数的可能约束

| 约束 | 描述 |
| --- | --- |
| `where T: struct` | 类型参数必须是值类型（仅不允许 `Nullable`）。 |
| `where T : class` | 类型参数必须是引用类型：例如，`class`、`interface`、`delegate` 或 `array`。 |
| `where T : new()` | 类型必须具有公有的默认构造函数。 |
| `where T : <base class name>` | 类型参数必须是或派自指定的基类。 |
| `where T : <interface name>` | 类型参数必须是或实现指定的接口。可以指定多个接口约束。约束接口也可以泛型的。 |
| `where T : U` | 为 `T` 提供的类型参数必须是或派自为 `U` 提供的参数。 |

示例 2-14 显示了如何向你的类定义中添加此类子句。

示例 2-14. 在类定义中使用 `where` 子句

```
class MyClass<T> 
    where T : class, new()
{
    public MyClass()
    {
        MyProperty = new T();
    }

    T MyProperty { get; set; }
}
```

当处理引用类型时，默认值是 `null`；对于像 `int` 这样的值类型，它们是 `0`。但当处理泛型类型参数时，默认值是什么？在这种情况下，你可以使用特殊的 `default(T)` 关键字。这为你提供了特定 `T` 类型的默认值。示例 2-15") 显示了如何使用它。

 示例 2-15. 在泛型类型参数上使用 `default(T)`

```
public void MyGenericMethod<T>()
{
    T defaultValue = default(T);
}
```

## 扩展现有类型

C# 提供了几种方法来扩展现有类型，而无需修改现有代码。在本节中，你将查看两种不同的方法：扩展方法和覆盖（overriding）。

### 扩展方法

在 .NET 4.0 中，增加了一种名为“扩展方法（extension methods）”的新功能，它允许你向现有类型添加新功能。你不需要对现有类型进行任何修改；只需将扩展方法引入作用域，就可以像调用普通实例方法一样调用它。

扩展方法需要声明在一个非泛型的、非嵌套的静态类中。示例 2-16 显示了扩展方法的创建。

示例 2-16. 创建扩展方法

```
public class Product
{
    public decimal Price { get; set; }
}

public static class MyExtensions
{
    public static decimal Discount(this Product product)
    {
        return product.Price * .9M;
    }
}

public class Calculator
{
    public decimal CalculateDiscount(Product p)
    {
        return p.Discount();
    }
}
```

注意，`Discount` 方法将 `this Product` 作为其第一个参数。特殊的 `this` 关键字使得该方法成为扩展方法。

### 考试提示

记住，普通静态方法与扩展方法的区别在于第一个参数的 `this` 关键字。

很棒的地方在于，扩展方法不能仅在类或结构体上声明。它也可以在 `interface`（如 `IEnumerable<T>`）上声明。通常，接口没有任何实现。但通过扩展方法，你可以为接口的每个实现添加方法。

语言集成查询（LINQ）是如何使用这种技术增强现有代码的最佳示例之一。你无需将所有 LINQ 运算符添加到每个类中，它们被创建为每个类型基接口的扩展方法。通过这种方式，所有集合突然可以使用 LINQ。

### 更多信息：LINQ

欲需更多关于 LINQ 的信息，请参阅第 4 章

## 方法覆盖

扩展现有类型的另一种方法是使用继承和覆盖。当类中的方法声明为 `virtual` 时，你可以在派生类中覆盖该方法。你可以完全替换现有功能，也可以增加基类的行为。示例 2-17 显示了如何在派生类中覆盖方法以更改某些功能。

示例 2-17. 覆盖虚方法

```
class Base
{
    public virtual int MyMethod()
    {
        return 42;
    }
}

class Derived : Base
{
    public override int MyMethod()
    {
        return base.MyMethod() * 2;
    }
}
```

现在你可以在不修改原始代码的情况下扩展类。在设计你的类时，为这些扩展点进行计划是非常重要的。你可以通过在类或方法上使用 `sealed` 关键字来禁用继承。当用于类上时，你不能从它派生其他类。当用于方法上时，派生类不能覆盖该方法。示例 2-18 显示了它是如何工作的。





# 示例 2-18. 在方法上使用 `sealed` 关键字

```cpp
class Base
{
    public virtual int MyMethod()
    {
        return 42;
    }
}

class Derived : Base
{
    public sealed override int MyMethod()
    {
        return base.MyMethod() * 2;
    }
}

class Derived2 : Derived
{
    // 这行将导致编译错误
    // public override int MyMethod() { return 1;}
}
```

### 更多信息：继承与重写

有关使用继承的更多信息，请参阅本章节稍后的目标 2.4：创建并实现类层次结构。

## 思考实验

**创建一个新的网上商店**

在这个思考实验中，应用你从该目标中学到的知识。你可以在章节末尾的答案部分找到这些问题的答案。

你的任务是为一个新的网上商店创建基本类型。作为客户，你可以搜索现有的产品数据库，并通过查看规格说明和其他用户的评论来比较不同的商品。系统应该跟踪热门产品，并向客户提供建议。当然，客户随后可以选择他们想要的商品并下单。这里还有一些你需要注意的业务规则：新客户不允许下单超过 500 美元的订单。订单至少要达到 10 美元才能获得免运费。未来还会添加更多业务规则，但目前尚不明确。请为你的经理回答以下问题：

1. 你将使用哪些基本类型来构建你的网上商店？
2. 你如何确保你的类型既包含行为又包含数据？
3. 你如何提高类型的易用性？

## 目标总结

*   `C#` 中的类型可以是值类型，也可以是引用类型。
*   泛型使用类型参数来使代码更具活性。
*   可以使用构造函数、方法、属性、字段和索引器属性来创建类型。
*   在创建和调用方法时，可以使用可选参数和命名参数。
*   方法重载允许方法接受不同的参数。
*   扩展方法可以用于为现有类型添加新功能。
*   重写允许你在派生类中重新定义来自基类的功能。

### 目标回顾

回答以下问题以测试你对该目标信息的掌握情况。你可以在章节末尾的答案部分找到这些问题的答案以及每个备选项正确或错误的解释。

1. 你正在创建一个新的集合类型，并希望确保其中的元素可以被轻松访问。你应该在类型中添加什么？
    1. 构造函数
    2. 索引属性
    3. 泛型类型参数
    4. 静态属性
2. 你正在创建一个只对引用类型有效的泛型类。你应该添加什么种类型约束？
    1. `where T : class`
    2. `where T : struct`
    3. `where T : new()`
    4. `where T : IDisposable`
3. 你将一个结构体变量作为参数传递给方法。方法更改了变量；但当方法返回时，变量并没有变化。发生了什么？
    1. 变量在传递之前没有初始化。
    2. 值类型在方法内部无法被更改。
    3. 传递值类型会创建数据的副本。原始数据没有被更改。
    4. 方法没有返回更改。

## 目标 2.2：使用类型

`C#` 在很大程度上是一种静态类型语言。这意味着 `C#` 编译器将检查每个表达式的类型。这有助于你发现错误，例如尝试将一种类型存储到另一种类型中（例如将字符串存储到 int 中）。你可能知道某个类型可以作为另一种类型使用，并且你想告诉编译器。由于由于，你有时需要在类型之间进行转换。但 `C#` 的部分并不是静态类型的。`C#` 4.0 中新的 `dynamic` 关键字允许你覆盖编译时检查，并像弱类型语言一样使用 `C#`。

本目标涵盖了如何：

*   装箱和拆箱值类型。
*   在不同类型之间转换。
*   使用 `dynamic` 关键字。

## 装箱与拆箱

在 `C#` 中处理值类型时，有时你希望将值类型存储在引用类型内部。例如，NET 库包含一个 `string.Concat` 方法，它将接收到的参数相加并将其作为字符串返回。

假设你使用以下参数调用 `string.Concat`：

```cs
string.Concat("To box or not box", 42, true);
```

如果你在 Visual Studio 中放入此代码并将鼠标悬停在 `Concat` 函数上，你会看到它接受三个参数，所有类型都是 `object`。

你可能会注意到你正在处理一个字符串、一个 int 和布尔值。这就是装箱发生的地方。

示例 2-19 中的示例将 int 放入对象中，然后取回来。

```cpp
int i = 42;
object o = i;
int x = (int)o;
```

值类型和引用类型的重要区别是，值类型直接存储值。引用类型存储指向堆上对象的引用。装箱是将值类型放入对象内部并存储其引用的过程。拆箱恰相反：它从堆中获取项并返回值类型。

如果你执行了无效的拆箱操作，运行时将抛出 `InvalidCastException`。

另一个需要知道的重要点是，当装箱和拆箱发生时（如示例所示，拆箱是清晰），你需要显式地将对象转换为值类型。相反，装箱并不那么明显。例如，调用 `GetType()`总是会对你的值类型装箱，因为 `GetType()` 只在 object 上定义且无法重写。装箱也发生在其他情况下。一个让你意外的情况是，当你将值类型作为接口使用时，它会被装箱。

```cs
IFormattable x = 3;
```

使用非泛型集合存储值类型时，会有很多这样的操作。装箱和拆箱操作会影响性能；但由于现在 .NET 支持泛型，这个问题就不那么大了，因为你可以在不装箱的情况下将值类型存储在集合中。

## 在不同类型之间转换

由于 `C#` 主要是静态类型语言，你不能在声明后更改变量的类型。除非存在显式转换，否则无法将一个项目转换为另一个。例如，将 int 转换为 double 是允许的，但将 `Address` 转换为 `Person` 是不允许的。

将一种类型转换为另一种类型的过程被称为*类型转换*。有几种不同的转换类型：

*   隐式转换
*   显式转换
*   用户自定义转换
*   使用辅助类转换

### 隐式转换

隐式转换不需要特殊的语法。它可以执行，是因为编译器知道这种转换是允许的，而且转换是安全的。




像 `int` 这样的值类型可以存储为 `double`，因为 `int` 可以放入 `double` 中而不会丢失任何精度。反之则是不可能隐式转换的。在将 `double` 转换为 `int` 时，你必须对 `double` 进行截断或舍入，这可能会导致某些数据丢失。示例 2-20 演示了从 `int` 到 `double` 的隐式转换。

#### 示例 2-20. 将整数隐式转换为 double

```
int i = 42;
double d = i;
```

另一种隐式转换是从引用类型转换为其基类类型之一。例如，每个引用类型都可以存储在 `object` 内部，因为每个引用类型最终都继承自 `object`。如果一个 `object` 实现了一个接口，它也可以被隐式转换为该接口。示例 2-21 演示了从 `object` 到其基类类型之一的隐式转换。

#### 示例 2-21. 将对象隐式转换为基类型

```
HttpClient client = new HttpClient();
object o = client;
IDisposable d = client;
```

### 显式转换

由于 C# 语言的类型安全性，编译器保护你免受所有不安全的隐式转换，例如将 `double` 转换为 `int`。如果你确实想进行这种转换，你需要显式进行。这被称为`强制转换`。示例 2-22 演示了如何显式地将 `double` 转换为 `int`。

#### 示例 2-22. 将 double 转换为 int

```
double x = 1234.7;
int a;
// 将 double 转换为 int
a = (int)x; // a = 1234
```

与隐式转换一样，引用类型也存在显式转换。在你可以隐式地从派生类型转到基类型的地方，你需要从派生类型到基类型进行强制转换，如 示例 2-23 所示。

#### 示例 2-23. 将基类型强制转换为派生类型

```
Object stream = new MemoryStream();
MemoryStream memoryStream = (MemoryStream)stream;
```

### 考试小贴士

请确保你了解隐式转换和显式转换之间的区别。显式转换被称为`强制转换`，并且总是需要某些特殊的语法。

### 用户定义转换

在创建自己的类型时，你可以添加对隐式转换和显式转换的支持。

假设你正在编写一个 `Money` 类，该类封装了用于处理不同货币的各种舍入算法。示例 2-24 演示了你可以添加的一些隐式和显式转换。

#### 示例 2-24. 实现隐式和显式转换运算符

```cs
class Money
{
    public Money(decimal amount)
    {
        Amount = amount;
    }

    public decimal Amount { get; set; }

    public static implicit operator decimal(Money money)
    {
        return money.Amount;
    }

    public static explicit operator int(Money money)
    {
        return (int)money.Amount;
    }
}
```

现在，在处理 `Money` 类时，你可以使用隐式转换转换为 `decimal` 并使用显式转换转换为 `int`，如 示例 2-25 所示。

#### 示例 2-25. 在自定义类型上使用隐式和显式强制转换运算符

```cs
Money m = new Money(42.42M);
decimal amount = m;
int truncatedAmount = (int)m;
```

添加此类转换可以极大提高你类型的易用性。如你所见，隐性和显式运算符应该声明为类中的 `public static` 方法。你需要指定返回类型（你正在转换的目标类型）以及你正在转换的源类型（你的类实例）。

### 使用辅助类进行转换

.NET Framework 还提供了用于类型转换的辅助类。对于不兼容类型之间的转换，你可以使用 `System.BitConverter`。对于兼容类型之间的转换，可以使用 `System.Convert` 以及各种类型上的 `Parse` 或 `TryParse` 方法。示例 2-26 演示了如何使用 `Parse` 和 `TryParse`。

#### 示例 2-26. 使用内置的 `Convert` 和 `Parse` 方法

```cs
int value = Convert.ToInt32("42");
value = int.Parse("42");
bool success = int.TryParse("42", out value);
```




在与组件对象模型（COM）应用程序集成时，你会使用主互操作程序集（PIA）。PIA 是桥接 .NET 和 COM 之间差距的 .NET 程序集。例如，Microsoft Office 拥有此类程序集，使你能够从 .NET 应用程序与 Word、Excel 以及其他 Office 应用程序集成。

在添加 `dynamic` 关键字之前，进行某些 Office 自动化并不是你想要作为业爱好去做的事情。但有了有了新的 `dynamic` 关键字后，访问 Office 变得简单得多。示例 2-28 显示了 `dynamic` 关键字如何允许你将某些数据导出到 Excel。

示例 2-28. 将某些数据导出到 Excel

```
static void DisplayInExcel(IEnumerable<dynamic> entities)
{
    var excelApp = new Excel.Application();
    excelApp.Visible = true;

    excelApp.Workbooks.Add();

    dynamic workSheet = excelApp.ActiveSheet;

    workSheet.Cells[1, "A"] = "Header A";
    workSheet.Cells[1, "B"] = "Header B";

    var row = 1;
    foreach (var entity in entities)
    {
        row++;
        workSheet.Cells[row, "A"] = entity.ColumnA;
        workSheet.Cells[row, "B"] = entity.ColumnB;
    }

    workSheet.Columns[1].AutoFit();
    workSheet.Columns[2].AutoFit();
}

var entities = new List<dynamic> {
                new
                {
                    ColumnA = 1,
                    ColumnB = "Foo"
                },
                new
                {
                    ColumnA= 2,
                    ColumnB= "Bar"
                }
    };

DisplayInExcel(entities);
```

在此示例中，`workSheet` 的类型是 `dynamic`。使用工作表变量的语句将在运行时评估并分发到 Office 应用程序编程接口（APIs）。所有的类型检查和必要的转换都在运行时完成。

## DynamicObject 和 ExpandoObject

在处理动态类型时，.NET Framework 提供了两个特殊类：`DynamicObject` 和 `ExpandoObject`。`DynamicObject` 是最灵活的。继承自 `DynamicObject` 时，你可以重写成员，允许你重写操作，例如获取或设置成员、调用方法或执行转换。通过使用 `DynamicObject`，你可以创建真正的动态对象，并对它们在运行时的操作方式进行完全控制。示例 2-29 显示了如何继承自 `DynamicObject`。

示例 2-29. 创建自定义的 DynamicObject

```
public class SampleObject : DynamicObject
{
    public override bool TryGetMember(GetMemberBinder binder, out object result)
    {
        result = binder.Name;
        return true;
    }
}

dynamic obj = new SampleObject();
Console.WriteLine(obj.SomeProperty); // 显示 'SomeProperty'
```

`ExpandoObject` 是密封实现，允许你在类型上获取和设置属性。例如，在 ASP.NET 模型-视图-控制器（MVC）中，有一个 `ViewBag` 可以用于将数据从 `Controller` 传递到 `View`。`ViewBag` 是一个 `ExpandoObject`。无需为你每个想要传递的数据元素创建一个新的静态类型属性，你可以使用 `ViewBag`，如 示例 2-30 所示。

示例 2-30. ASP.NET MVC 中的 dynamic 关键字

```sharp
public ActionResult Index()
{
    ViewBag.MyDynamicValue = "此属性不是静态类型的";
    return View();
}
```

应谨慎使用 `dynamic` 关键字。它赋予了你极大的活性，但因为你失去了静态类型，它也容易导致只能在运行时发现的错误。但在与其他语言集成或替换反射时，动态支持是 .NET Framework 的一个非常好的补充。

## 思考实验

### 优化你的代码

在思考实验中，应用你对这一目标所学的知识。你可以在本书末尾的 答案 章节找到这些问题的答案。

你正在开发一个用于复杂计算的可重用库。你的应用程序正越来越受欢迎，但你开始听到一些负面反馈。有人说你的类型无法方便使用。在向最终用户显示计算的最终结果时，涉及到大量的手工工作。其他人遇到了性能问题，并希望你对此做些处理。你从 C# 1.0 开始开发应用程序，你的应用程序使用 `ArrayLists` 来跟踪计算所需的所有参数。你的参数被实现为结构体（struct）。你的算法实现在一个类层次结构中，并且你经常需要将基类型转换为派生类型。由于这并不总是可能的，你增加了大量的 `try/catch` 语句来从错误中恢复。回答以下问题：

1. 泛型集合如何提高性能？
2. 有什么你可以做来避免装箱（boxing）？
3. 如何确保你的类型得到更好的转换？

## 目标总结

* 当值类型被视为引用类型时就会发生装箱。
* 在类型之间进行转换时，你可以进行隐式或显式转换。
* 显式转换被称为转换，需要特殊的语法。
* 你可以创建自己的隐式和显式转换。
* .NET Framework 提供了用于转换的辅助方法。
* `dynamic` 关键字可以提高与其他语言的互操作性。

### 目标回顾

回答以下问题以测试你对本目标信息的理解。你可以在本书末尾的 答案 章节找到答案。

1. 你正在创建一个 `Distance` 类。你想简化从你的 `Distance` 类到 double 的转换。你应该添加什么？
   - 无，这是可能的。
   - 隐式转换运算符。
   - 显式转换运算符。
   - 静态 `Parse` 方法。

2. 你想确定对象引用的值是否派生自特定类型。你可以使用哪些 C# 语言特性？（选择所有适用）
   - `as` 运算符
   - 隐式转换
   - `is` 运算符
   - `dynamic` 关键字

3. 你使用 `ArrayList` 作为 `Points` 集合（`Point` 是自定义结构体）。你在处理大量 `Points` 时遇到了性能问题。你需要做什么？
   - 使用泛型集合代替 `ArrayList`。
   - 将 `Point` 更改为引用类型。
   - 添加 `Point` 到 `object` 的隐式转换。
   - 将集合类型改为 `dynamic`。

### 目标 2.3: 强制封装

封装是面向对象开发的支柱之一。在面向对象的系统中隐藏对象内部私有元素可以创建更好的软件。当你想要执行某个操作时，请求另一个对象执行此操作。你只需要知道外部接口。实现对你是隐藏的，只要它符合接口，你就不需要理解它是工作的。C# 通过提供属性、访问修饰符和接口帮助封装对象的内部机制。

本目标涵盖了如何：

* 使用访问修饰符。
* 使用属性。
* 使用显式接口实现。





封装的核心概念之一是隐藏信息。这正是 C# `access modifiers`（访问修饰符）用用场。访问修饰符允许你限制对所有类型和类型成员的访问。示例 2-31 显示了如何在类和方法上使用 `public` 访问修饰符。

示例 2-31. 使用访问修饰符

```
public class Dog
{
    public void Bark() { }
}
```

由于 `Dog` 类使用了 `public` 访问修饰符，所有人都可以创建它的新实例。`Bark` 方法也是 `public` 的，这意味着每个人都可以调用它。C# 中还有其他限制更严格访问修饰符。表 2-3 显示了你可以在 C# 中使用的哪些访问修饰符。

表 2-3. C# 中的访问修饰符

| 访问修饰符 | 描述 |
| --- | --- |
| public | 无限制；受限访问 |
| internal | 限于当前程序集 |
| protected | 限于包含类及其派生类 |
| protected internal | 限于当前程序集或派生类型 |
| private | 限于当前类型 |

### 使用 private 隐藏

`private` 成员只能由同一类型中的成员访问。这是限制最严格的访问修饰符。对于属性和方法等嵌套成员，`private` 是默认的访问修饰符。然而，在代码中显式地提到它可以帮助其他开发者理解你的意图。示例 2-32 显示了如何在字段上使用 `private` 访问修饰符。

示例 2-32. 使用 private 访问修饰符

```
public class Accessibility
{
    private string _myField;

    public string MyProperty
    {
        get { return _myField;  }
        set{ _myField = value;  }
    }
}
```

字段 `_myField` 的可访问性为 `private`。这意味着它只能在类内部访问。公共属性 `MyProperty` 封装了对字段的访问。

当类的用户尝试更改你的属性值时，这可以帮助你执行业务规则。在你的 `set` 访问器中，你可以检查是否允许使用新值，并确保没有人将其更改为非法值。

该类的用户也受到了类内部实现机制更改的封装。例如，当实现更改为对 `MyProperty` 值的查找时，外部用户不会察觉，正如 示例 2-33 所示。

示例 2-33. 在不让外部用户察觉的情况下更改私有字段

```
public class Accessibility
{
    // 省略初始化代码和错误检查
    private string[] _myField;

    public string MyProperty
    {
        get { return _myField[0]; }
        set { _myField[0] = value; }
    }
}
```

你类的用户仍然可以在不知道实现已发生更改的情况下访问 `MyProperty`。

### 在继承层次结构中保护访问权限

在处理对象层次结构时，可以使用另一种访问修饰符：`protected`。`protected` 限制对该类型以及所有派生自该类型的类的成员的访问。它可以用于类的所有成员。标记为 `private` 的成员无法被派生类型访问。示例 2-34 显示了继承层次结构中 `private` 和 `protected` 的区别。

示例 2-34. 在继承中使用 protected 访问修饰符

```csharp
public class Base
{
    private int _privateField = 42;
    protected int _protectedField = 42;

    private void MyPrivateMethod() { }
    protected void MyProtectedMethod() { }
}

public class Derived : Base
{
    public void MyDerivedMethod()
    {
        // _privateField = 41; // 不行，这将产生编译错误
        _protectedField = 43; // 可以，可以访问受保护字段

        // MyPrivateMethod(); // 不行，这将产生编译错误
        MyProtectedMethod(); // 可以，可以访问受保护方法
    }
}
```

### 更多信息：继承

关于使用继承的更多信息，请参阅本章节后部分的 目标 2.4：创建并实现类层次结构。

### 将类型保持在程序集内部

C# 代码包含在 `assemblies`（程序集）中。在 Visual Studio 中，你可以将程序集看作一个项目。这里是另一种访问修饰符的使用之处：`internal`。`internal` 将类型或类型成员的访问限制在同一个程序集内。它比 `public` 严格，但比 `private` 宽松。当你有一个类型（例如辅助类或实现细节）不应该在程序集外部可访问时，`internal` 是非常有用的。示例 2-35 显示了如何使用 `internal` 访问修饰符。

```
internal class MyInternalClass
{
    public void MyMethod() { }
}
```

`MyInternalClass` 类只能在声明它的程序集内部使用。类内部公共方法受其封装类型的限制。因此，只有能够访问内部类的用户才能调用该方法。

你还可以结合 `protected` 和 `internal` 访问修饰符。在使用 `protected internal` 访问修饰符时，请记住它是“或”而不是“与”。在实践中，这意味着访问限于当前程序集或派生自类的类型，即使这些类型在另一个程序集中。

当你想要将内部类型或类型成员暴露给另一个程序集时，可以使用特殊的属性：`InternalsVisibleToAttribute`。你可以使用此属性指定另一个也可以访问内部类型的程序集。这种情况下用用的场景之一是你编写单元测试时。可能你有一个封装了复杂算法的内部类，你想为它编写单元测试。通常，你将此属性包含在项目 `Properties` 文件夹下的 `AssemblyInfo.cs` 文件中：

```
[assembly:InternalsVisibleTo("Friend1a")]
[assembly:InternalsVisibleTo("Friend1b")]
```

你可以根据需要使用多个属性。在这个示例中，`Friend1a` 和 `Friend1b` 程序集现在被允许访问你程序集的内部类型和成员。表 2-4 总结了在特定情况下可以使用哪些访问修饰符。

| 成员所属类型 | 默认成员访问权限 | 允许声明的成员访问权限 | 
| --- | --- | --- |
| enum | public | 无 |
| class | private | publicprotectedinternalprotected internal |
| interface | public | 无 |
| struct | private | publicinternalprivate |

### 更多信息：属性

关于使用属性的更多信息，请参阅本章节后部分的 目标 2.5：使用反射在运行时查找、执行和创建类型。




需要注意的是，包含类型的访问修饰符始终会被在在。例如，`internal` 类内部的 `public` 方法的访问性为 `internal`。这种情况下存在例外（例如，当 `internal` 类实现 `public` 接口，或者当类重写了基类的 `public virtual` 成员时），因此在确定你需要的类型访问性时，你需要跟踪这些情况。

始终显式地选择尽可能低的可见性是一个良好的做法，因为你希望尽可能地隐藏信息。如果不声明任何访问修饰符，`C#` 将分配默认的成员访问性，具体定义见表 2-4。

## 使用属性

字段对其包含的数据提供直接访问。然而，在面向对象开发中，你通常倾向于对数据进行某些控制。在某些语言中，这会导致示例 2-36 中所示的模式。

示例 2-36. 使用自定义方法封装字段

```
private int _field;
public void SetValue(int value) { _field = value; }
public int GetValue() { return _field; }
```

通过这种方式，你可以在设置和获取值时运行自定义代码。例如，你可以检查新值是否被允许，或者实时计算结果。

`C#` 提供了一种使用这种模式的简洁简洁方式：*属性*。属性看起来像一个普通的字段。它有类型、名称和访问修饰符。区别在于它添加了*访问器*。

示例 2-37 展示了如何创建属性。

示例 2-37. 创建属性

```
class Person
{
    private string _firstName;

    public string FirstName
    {
        get { return _firstName; }
        set
        {
            if (string.IsNullOrWhiteSpace(value))
                throw new ArgumentException();
            _firstName = value;
        }
    }
}
```

如你所见，`get` 和 `set` 方法是属性定义的一部分。包含实际数据的字段是私有的，只能通过属性访问（在类内部除外）。

使用带有默认 `get` 和 `set` 方法的属性是非常常见的，以至于 `C#` 为其添加了简写符号：

```
public int Value { get; set; }
```

这被称为*自动实现属性*。编译器将其翻译为具有私有、匿名备用字段的属性。当你编写大量属性时，这可以为你节省一些时间。当你需要执行额外的代码时，可以很容易地更改为使用 `get` 和 `set` 方法。

`get` 和 `set` 访问器可以有不同的访问修饰符。例如，你可以拥有一个 `public get` 和一个 `private set` 方法。对于外部用户来说，这创建了一个只读字段的幻象。你也可以拥有只有 `get` 或只有 `set` 访问器的属性。在创建真正的只读属性或创建动态计算其取值的属性时，单个的 `get` 访问器会非常有用。只有 `set` 访问器的属性并不常见，但你可以将其用于“只管后不忘”的场景，即用户设置一个值但从不检查。

### 考试提示

对于公共成员，始终优先使用属性而不是字段。自动实现的属性在外部世界看起来像字段，但你可以在需要时随时添加额外的行为。

## 使用显式接口实现

接口在用封装时非常有用。在下一个目标中，你将查看如何设计和使用接口。但关于封装这个主题，你需要了解*显式接口实现*。

作为显式接口实现的一个示例，请查看 Entity Framework（它是 .NET Framework 的一个对象关系映射器）。在使用 Entity Framework 时，你操作的是 `DbContext` 类，它是 `ObjectContext` 的封装器，并暴露了更易使用的接口。

`DbContext`实现了以下接口（参见示例 2-38）。

示例 2-38. `IObjectContextAdapter` 接口

```
public interface IObjectContextAdapter
{
    ObjectContext ObjectContext { get; }
}
```

尽管接口显示了一个 `ObjectContext` 属性，但以下代码无法编译：

```
DbContext ctx = ...; // 创建新上下文
var context = ctx.ObjectContext;
```

以下代码可以编译：

```
var adaptedContext = ((IObjectContextAdapter)ctx).ObjectContext;
```

这是如何可能的？这是因为 `DbContext` 显式地实现了 `IObjectContextAdapter` 接口。*显式接口实现*意味着只有在直接使用接口时才能访问接口类型元素。你可以通过在实现中添加接口名称和点号来创建显式接口实现。

示例 2-39. 显式实现接口

```
interface IInterfaceA
{
    void MyMethod();
}

class Implementation : IInterfaceA
{
    void IInterfaceA.MyMethod() { }
}
```

还有一种需要显式接口实现的情况：当一个类实现了两个包含重复签名的接口，但希望对两者有不同的实现时。当隐式实现这些接口时，实现中只存在一个方法。通过显式接口实现，两个接口都有自己的方法。示例 2-40 展示了如何显式实现接口。

示例 2-40. 显式实现接口

```
interface ILeft
{
    void Move();
}

interface IRight
{
    void Move();
}

class MoveableObject : ILeft, IRight
{
    void ILeft.Move() { }
    void IRight.Move() { }
}
```

## 思考实验

**正确地封装类型**

在这个思考实验中，应用你对本目标学到的知识。你可以在本书末尾的答案部分找到这些问题的答案。

你正在与一个团队合作创建一个新的应用程序，用于跟踪化学实验室的库存。你的应用程序由许多类型组成，它们都参与确保物品不被不合格的人员使用、危险化学品不在同一个房间内，以及在库存不足时及时订购。

目前，系统中的所有类型都有不同的访问修饰符。某些类型是完全不可变的；另一些类型暴露了所有数据。你正在与同事讨论当前的问题。他认为所有类型和所有类型成员都应该是公共的。

1. 向你的同事解释为什么将所有成员变为公共并不是解决方案。
2. 举一个属性如何帮助封装数据同时提高可用性的例子。
3. 接口如何用于改进设计？

## 目标总结

* 封装在面向对象的软件中非常重要。它隐藏了细节并改进了类型的可用性。
* 数据可以使用属性进行封装。
* 属性可以同时具有 get 和 set 访问器，并运行额外的代码，通常被称为 getter 和 setter。
* 类型和类型元素可以有访问修饰符以限制访问性。





- 访问修饰符有 `public`、`internal`、`protected`、`protected`、`internal` 和 `private`。
- 显式接口实现可以隐藏信息或实现具有重复成员签名的接口。

##set

回答以下问题以测试你对本目标信息的掌握情况。你可以在章节末尾的答案部分找到这些问题的答案，以及对每个备选项正确或错误的解释。

1. 你应该使用哪种访问修饰符来确保类中的某个方法只能被同一程序集内部的派生类型访问？
    1. 将类设为 `public` 并将其成员设为 `public`。
    2. 将类设为 `public` 并将其设为 `protected`。
    3. 将类设为 `internal` 并将其设为 `internal`。
    4. 将类设为 `internal` 并将其设为 `protected`。

2. 你需要从类中暴露某些数据。这些数据可以被其他类型读取，但只能由派生类型更改。你应该使用什么？
    1. 一个 `protected` 字段
    2. 一个带有 `protected` set 修饰符的 `public` 属性
    3. 一个 `protected` 属性
    4. 一个带有 `public` get 修饰符的 `protected` 属性

3. 你有一个类实现了两个接口，这两个接口都具有同名的方法。接口 `IA` 应该是默认实现。接口 `IB` 仅在特殊情况下使用。你如何实现这些接口？
    1. 隐式实现 `IA` 并显式实现 `IB`。
    2. 同时显式实现 `IA` 和 `IB`。
    3. 同时隐式实现 `IA` 和 `IB`。
    4. 显式实现 `IA` 并隐式实现 `IB`。

### 目标 2.4：创建并实现类层次结构

继承是面向对象开发的另一个支柱。“继承” 是让一个类派生自另一个类的过程。基类和派生类之间的继承建立了一种“是一种”（is-a-kind-of）的关系。例如，孩子是一个人类，而 `SqlConnection` 是一个 `DbConnection`。这允许你创建对象的层次结构，以便更好地模拟现实世界的场景。它还鼓励了代码复用。C# 是一种典型的面向对象语言，因为它提供了你所需的所有支持，以创建自己的类层次结构并以最有效的方式使用它们。你将看到如何使用接口和基类可以帮助你创建可以与多个实现的通用代码，并将将看到基类如何帮助代码复用以及 .NET Framework 的一些标准接口。

本目标涵盖了：
- 设计和实现接口。
- 创建和使用基类。
- 使用一些标准的 .NET Framework 接口。

## 设计和实现接口

接口是 C# 内部的核心概念。`interface` 包含方法、属性、事件和索引器的公共签名。类型（包括类和结构体）都可以 `implement an interface.`。示例 2-41 显示了如何实现自定义接口。

示例 2-41. 创建并实现接口

```
interface IExample
{
    string GetResult();
    int Value { get; set; }
    event EventHandler ResultRetrieved;
    int this[string index] { get; set; }
}

class ExampleImplementation : IExample
{
    public string GetResult()
    {
        return "result";
    }

    public int Value { get; set; }

    public event EventHandler CalculationPerformed;

    public event EventHandler ResultRetrieved;

    public int this[string index]
    {
        get
        {
            return 42;
        }
        set { }
    }
}
```

C# 的惯是让接口名称以大写 `I` 开头。这有助于你在使用 IntelliSense 时查看某个类型是否为接口。正如示例所示，接口的元素没有提到任何访问修饰符，因为所有接口成员默认都是公共的。无法在实现接口时将访问修饰符更改为公共以外的任何内容。

需要注意的是，接口可能定义一个仅带有 get 访问器的属性，而实现该类型也有一个 set 访问器（查看 示例 2-42）。

示例 2-42. 为已实现的接口属性添加 set 访问器

```
interface IReadOnlyInterface
{
    int Value { get; }
}

struct ReadAndWriteImplementation:IReadOnlyInterface
{
    public int Value { get;  set; }
}
```

在这种情况下，实现类添加了一个额外的 set 访问器。使用这种模式的优势是，如果用户通过接口访问你的类，只会看到 get 访问器。类的直接用户将同时看到 get 和 set 访问器。

接口还可以继承其他接口。这样，你可以有一个接口链，每个接口都增加类型的公共签名。继承自派生接口之一的类必须实现整个层次结构中的所有签名。

在定义接口时也可以使用泛型。例如，如果你正在实现存储库模式（存储库提供了对存储数据库或其他存储类型中对象的访问），你可以使用泛型类型参数，这样就不必为想要存储的每个实体创建不同的接口，正如 示例 2-43 所示。

示例 2-43. 使用泛型类型参数创建接口

```
interface IRepository<T>
{
    T FindById(int id);
    IEnumerable<T> All();
}
```

现在你可以为不同的类创建 `Repository<T>` 的具体实现。例如，你可以拥有 `IRepository<Product>` 和 `IRepository<Order>`。泛型接口可以具有多个类型参数和类型约束。

### 使用接口

由于接口没有实现，无法无法实例化。你只能实例化实现了接口的具体类型，正如 示例 2-44 所示。

示例 2-44. 实现接口的具体类型

```
interface IAnimal
{
    void Move();
}

class Dog : IAnimal
{
    public void Move() {}
    public void Bark() {}
}

IAnimal animal = new Dog();
```

你的代码现在持有 `IAnimal` 接口的引用。尽管你知道它实际上指向 `Dog`，但你无法在上面调用 `Bark` 方法。如果你想从接口 `IAnimal` 转换为类型 `Dog`，你需要对其进行强制转换。

### 更多信息：强制转换和转换

有关将接口转换为其他类型的更多信息，请查看本章节后面的 目标 2.2：使用类型。

接口还可以作为方法的参数。这样，你可以创建可以针对各种不同实现的通用代码：

```
void MoveAnimimal(IAnimal animal)
{
    animal.Move();
}
```

面向对象开发的重要概念之一是面向合同编程而不是实现。接口保证了某些功能可用（合同）。你不需要关心它是如何实现的，只要它有效即可。这有助于编写松耦合且更易维护的代码。

### 注意：不支持多重继承





某些语言如 `C++` 提供了多继承的概念。这意味着一个类可以拥有多个基类。通过这种方式，`Bat`（蝙蝠）可以是 `Mammal`（哺乳动物，继承自 `Animal`）的 `DrawableObject`（绘制对象）。`C#` 不支持多继承。`C#` 的创建者决定不实现多继承，是因为这可能会带来相关的困难。在使用多继承时，当两个基类具有相同签名的方法时，你会遇到冲突。`C#` 确实提供了多接口继承，并允许显式实现接口以分离不同的实现。它不支持多类继承。

## 创建和使用基类

接口只定义了类型的公共签名。从接口派生不会继承任何实现代码。派生类型在如何实现接口方面是完全自由的。当你确实想要继承实现代码时，可以继承另一个类。示例 2-45 显示了如何创建一个基类。

示例 2-45. 创建基类

```
interface IEntity
{
    int Id { get; }
}

class Repository<T>
    where T : IEntity
{
    protected IEnumerable<T> _elements;

    public Repository(IEnumerable<T> elements)
    {
        _elements = elements;
    }

    public T FindById(int id)
    {
        return _elements.SingleOrDefault(e => e.Id == id);
    }
}
```

`Repository` 基类提供了一个通过 ID 查找实体的方法。这段代码是泛型的，可以被所有实体使用。如果你想添加一个特定的查询来按日期和金额过滤订单怎么办？那将不再适用于所有实体；只适用于订单（Order）实体。使用继承可以帮助你在重用代码的同时添加一些额外的行为。示例 2-46 显示了如何继承一个类。

示例 2-46. 继承基类

```
class Order : IEntity
{
    public int Id { get; }
    // 省略其他实现细节
    // ...    
}

class OrderRepository : Repository<Order>
{
    public OrderRepository(IEnumerable<Order> orders)
        : base(orders) { }

    public IEnumerable<Order> FilterOrdersOnAmount(decimal amount)
    {
        List<Order> result = null;
        // 过滤代码
        return result;
    }
}
```

`OrderRepository` 现在既有一个通过 ID 查找订单的方法，也有按金额过滤订单的特定方法。你可以以类似的方式使用为现有类型添加成员。如你所示，你可以使用 `base` 关键字来调用基类的构造函数。当你想要调用基类的方法或其他成员时，也可以使用 `base` 关键字。

### 注意：子与父或基类与派生类

在谈论继承时，经常使用 `parent`（父）和 `child`（子）类。但在思考继承时，这是正确的术语吗？例如，`Dog`（狗）是一种 `Animal`（动物）。这可以通过继承关系来建模。但是，你会说 `Dog` 是 `Animal` 的 `Child`（子）吗？`Child` 并不是 `Parent`（父）的一种。在支持多继承的语言中，情况变得更加混乱。在定义继承关系时，与其使用 `Parent` 和 `Child`不如使用 `base`（基类）和 `derived class`（派生类），以避免与现实世界中的继承产生混淆。

### 更改行为

在构建类层次结构时，你有时想要替换或扩展基类的行为。假设你想为你创建的存储库添加一些日志功能。你不想重写所有的过滤代码；相反，你只想添加一些额外的行为。

这就是 `virtual`（虚）和 `override`（重写）关键字派用用场。将方法标记为 `virtual` 允许派生类重写该方法。派生类可以选择完全替换或扩展基类的行为。示例 2-47 显示了如何通过重写方法来扩展基类。

示例 2-47. 重写虚方法

```
class Base
{
    protected virtual void Execute()
    {}
}

class Derived : Base
{
    protected override void Execute()
    {
        Log("执行前");
        base.Execute();
        Log("执行后");
    }
    private void Log(string message) { /* 一些日志代码 */ }
}
```

通过将基类中的方法标记为 `virtual`，派生类可以重写它。通过在方法名前加上 `base`，派生类可以执行基类上的方法。通过跳过对 `base` 的调用，派生类完全替换了功能。

如果基类没有将方法声明为 `virtual`，派生类就无法重写该方法。然而，它可以使用 `new` 关键字，这会显式地隐藏基类的成员（这与使用 `new` 关键字创建对象的新实例不同）。这会导致一些棘手的情况，如示例 2-48 所示。

示例 2-48. 使用 new 关键字隐藏方法

```
class Base
{
    public void Execute() { Console.WriteLine("Base.Execute"); }
}

class Derived : Base
{
    public new void Execute() { Console.WriteLine("Derived.Execute"); }
}

class Program
{
    static void Main(string[] args)
    {
        Base b = new Base();
        b.Execute();
        b = new Derived();
        b.Execute();
    }
}
```

运行此代码将两次输出 `Base.Execute`。如果你将基类方法声明为 `virtual`，派生类使用 `override` 而不是隐藏，代码将显示 `Base.Execute` 和 `Derived.Execute`。你应该尽量避免使用 `new` 关键字来隐藏方法。

### 抽象和密封类

如果你不想允许基类被实例化，可以将其声明为 `abstract`（抽象）类。`abstract` 类可以拥有成员的实现代码，但并不是要求的。因为类是抽象的，你无法使用 `new` 运算符对其创建新实例。示例 2-49 显示了如何创建一个抽象类。

示例 2-49. 创建抽象类

```
abstract class Base
{
    public virtual void MethodWithImplementation() {/*具有实现的方法*/}

    public abstract void AbstractMethod();
}

class Derived : Base
{
    public override void AbstractMethod() { }
}
```

如你所示，抽象类可以有完全实现的成员，也可以有抽象成员。具体的派生类型要求实现所有抽象成员（就像接口一样）。抽象类可以是共享接口和某些实现细节的好方法，特别是当只有派生类型应该是实例化的时。示例 2-49 使用 `override` 关键字来实现基类定义的抽象方法。它也可以用于抽象或虚方法、属性、索引器和事件以扩展或修改实现。

抽象类的反面是 `sealed`（密封）类，它不能被派生。因此，它不能标记为抽象，且所有成员都应该实现。结构体（struct）在 `C#` 中是隐含密封的。永远无法从结构体继承。标记类为 `sealed` 是一种良好的做法。如果你不这样做，其他人可能会在你没有考虑过的情况下继承你的类。如果继承是必要的，你可以移除 `sealed` 关键字并考虑其影响。

### 考试提示





请确保你了解接口和抽象类之间的区别。接口没有实现代码。抽象类可以选择实现某些方法，也可以将其留给派生类。

### 里斯科夫替换原则

继承是一项强大的技术，但应该谨慎使用。正如前面提到的，只有当你处理的是“是一种（is-a-kind-of）”关系时，才应该使用继承。`里斯科夫替换原则`规定，在任何可以使用基类的地方，子类都应该是可用的。子类不应该突然改变用户所依赖的行为。

违反这一原则非常容易。请考虑 示例 2-50 中的代码。

示例 2-50. 带有 `Area` 计算的 `Rectangle` 类

```sharp
class Rectangle
{
    public Rectangle(int width, int height)
    {
        Width = width;
        Height = height;
    }

    public int Height { get; set; }

    public int Width { get; set; }

    public int Area
    {
        get
        {
            return Height * Width;
        }
    }
}
```

观察这个 `Rectangle` 类时，你会说 `Square` 是一种 `Rectangle` 吗？在数学中，这是成立的。我们知道正方形是特殊的矩形。你可以使用继承关系来对其进行建模，如 示例 2-51 所示。

示例 2-51. 继承自 `Rectangle` 的 `Square` 类

```sharp
class Square : Rectangle
{
    public override int Width
    {
        get
        {
            return base.Width;
        }
        set
        {
            base.Width = value;
            base.Height= value;
        }
    }

    public override int Height
    {
        get
        {
            return base.Height;
        }
        set
        {
            base.Height = value;
            base.Width = value;
        }
    }
}
```

因为你知道你处理的是一个正方形，你通过同时修改 `Width` 和 `Height` 属性来帮助该类的用户。这样一来，矩形始终是一个正方形。

假设你想像 示例 2-52 所示那样使用该类。

示例 2-52. 使用 `Square` 类

```sharp
Rectangle rectangle = new Square();
rectangle.Width = 10;
rectangle.Height = 5;

Console.WriteLine(rectangle.Area);
```

这段代码将输出 `25`。用户认为他正在处理一个具有计算 `Area` 的 `Rectangle`，但由于 `Rectangle` 指向一个 `Square`，因此只存储了最新的 `Height` 值。

这是一个违反里斯科夫替换原则的典型示例。`Square` 类无法在所有通常会使用 `Rectangle` 的地方使用。

### 实现标准的 .NET Framework 接口

.NET Framework 有几个标准接口，你可以将其应用于你自己的类型。在实现这些接口时，你的类可以用于 .NET Framework 提供的基础设施中。

### IComparable

`IComparable` 接口包含一个方法，如 示例 2-53 所示。

示例 2-53. `IComparable` 接口

```csharp
public interface IComparable
{
    int CompareTo(object obj);
}
```

该接口用于排序元素。`CompareTo` 方法返回一个 int 值，显示两个元素之间的关系。表 2-5 显示了 `CompareTo` 方法可能返回的值。

表 2-5. CompareTo 的返回值

| 数值 | 含义 |
| --- | --- |
| 小于零 | 当前实例在排序顺序中位于 `CompareTo` 方法指定的对象之前。 |
| 零 | 当前实例在排序顺序中的位置与 `CompareTo` 方法指定的对象相同。 |
| 大于零 | 当前实例在排序顺序中位于 `CompareTo` 方法指定的对象之后。 |

例如，如果你正在创建一个 `Order` 类，并且它有一个你想排序的 `DateTime Created` 属性，你可以在 `Order` 类上实现 `IComparable` 并比较两个订单的 `Created` 日期。示例 2-54 显示了如何做。

示例 2-54. 实现 `IComparable` 接口

```csharp
class Order : IComparable
{
     public DateTime Created { get; set; }

     public int CompareTo(object obj)
     {
         if (obj == null) return 1;

         Order other = obj as Order;
         if (other == null) return -1;

         return Created.CompareTo(other.Created);
     }
}
```

### IEnumerable

.NET 中的 `IEnumerable` 和 `IEnumerator` 接口帮助你实现迭代器模式，这让你能够访问集合中的元素，而不关心其实现方式。你可以在 `System.Collection` 和 `System.Collections.Generic` 中找到这些接口。使用迭代器模式时，你可以轻松地遍历数组、列表或自定义集合。它在 LINQ 中被广泛使用，LINQ 可以以通用的方式访问各种集合。





```cs
class Person
{
    public Person(string firstName, string lastName)
    {
        FirstName = firstName;
        LastName = lastName;
    }

    public string FirstName { get; set; }
    public string LastName { get; set; }

    public override string ToString()
    {
        return FirstName + " " + LastName;
    }
}

class People : IEnumerable<Person>
{
    public People(Person[] people)
    {
        this.people = people;
    }

    Person[] people;

    public IEnumerator<Person> GetEnumerator()
    {
        for (int index = 0; index < people.Length; index++)
        {
            yield return people[index];
        }
    }
    IEnumerator IEnumerable.GetEnumerator()
    {
        return GetEnumerator();
    }
}
```

注意 `GetEnumerator` 函数中的 `yield` 返回。`yield` 是一个特殊的关键字，只能在迭代器上下文中使用。它指示编译器将这段普通代码转换为状态机。生成的代码会跟踪你在集合中的位置，并实现 `MoveNext` 和 `Current` 等方法。

因为现在创建迭代器变得非常简单，它突然变成了一个你可以很容易在自己的代码中使用的特性。每当你对同一个数据结构进行大量手动循环时，请考虑迭代器模式以及它如何帮助你创建出更优雅的代码。

### IDisposable

.NET Framework 中另一个实用的接口是 `IDisposable`。该接口用于便于与外部未托管资源的操作。正如目标 2.6 节讨论的，C# 是一种托管语言，使用垃圾回收器来清理内存。然而，你仍然会访问数据库连接或文件句柄等外部未托管资源。这就是 `IDisposable` 发挥用场的地方。示例 2-57 显示了 `IDisposable` 接口的定义。

示例 2-57. IDisposable 接口

```cs
public interface IDisposable
{
        void Dispose();
}
```

`IDisposable` 接口只有一个方法 `Dispose()`。该方法用于释放任何未托管资源。

### 更多信息：实现 IDisposable

关于实现 `IDisposable` 的更多信息，请参见本章末后的目标 2.6：管理对象的生命周期。

### IUnknown

在 .NET 存在之前，第一代 Windows API 是基于动态链接库（DLL）中的函数库的。后续代将这些函数收集到组件对象模型（COM）接口中。.NET Framework 提供了类，将这些 API 的大部分封装在托管版本中，以便在日常生活中你几乎永远不会触碰任何 COM 组件。

通常情况下，你只需要为 COM 对象添加引用，编译器就会生成必要的称为 `COM Interop` 类的包装类。如果由于某些原因导致失败，你就必须手动创建包装类；这就是 `IUnknown` 接口用用的地方。

### 更多信息：实现 IUnknown

关于实现 `IUnknown` 的更多信息，请访问 `[`msdn.microsoft.com/en-us/library/aa645712(v=vs.71).aspx`](http://msdn.microsoft.com/en-us/library/aa645712(v=vs.71).aspx)`。

## 思考实验

**优化你的代码**

在这个思考实验中，应用你从本目标中学到的知识。你可以在本章末尾的答案 章节找到这些问题的答案。

你正在为一个房地产中介开发一个全新的 Web 应用程序。该中介人希望在网站上展示他的房产，并确保用户可以轻松地搜索。例如，用户将能够根据位置、大小、房产类型和价格进行过滤结果。你需要创建一个使用所有所选标准来过滤可用房屋列表的底层架构。

你想看看是否可以使用 .NET Framework 中的一些标准接口来实现你的底基础架构。

1. 为什么 .NET Framework 提了一些没有任何具体实现的接口？如果 .NET Framework 使用抽象基类难道不是更简单吗？
2. 你会使用接口继承还是类继承来创建你的搜索标准？
3. 你会使用以下哪些接口？
   * `IComparable`
   * `IEnumerable`
   * `IDisposable`
   * `IUnknown`

## 目标总结

* 继承是一个类派自另一个类或派自接口的过程。
* 接口指定了类型必须实现的公共元素。
* 类可以实现多个接口。
* 基类可以将方法标记为虚（virtual）；派生类随后可以重写（override）这些方法以添加或替换行为。
* 类可以被标记为抽象（abstract），这样它不能被实例化，只能作为基类使用。
* 类可以被标记为密封（sealed），这样它不能被继承。
* .NET Framework 提供了默认接口，如 `IComparable`、`IEnumerable`、`IDisposable` 和 `IUnknown`。

### 目标回顾

回答以下问题以测试你对本目标信息的掌握情况。你可以在本章末尾的答案 章节找到这些问题的答案，以及对每个选项为何正确或错误的解释。

1. 你想创建一个类型层级结构，因为你有一些想要在所有类型之间共享的实现代码。你还有一些想要共享的方法签名。你应该使用什么？
   1. 接口
   2. 带有虚方法的类
   3. 抽象类
   4. 密封类
2. 你想创建一个可以轻松排序的类型。你应该实现哪个接口？
   1. `IEnumerable`
   2. `IComparable`
   3. `IDisposable`
   4. `IUnknown`
3. 你想继承一个现有的类并向方法添加一些行为。你需要采取哪些步骤？（选择所有适用）
   1. 在基类型上使用 `abstract` 关键字。
   2. 在基方法上使用 `virtual` 关键字。
   3. 在派生方法上使用 `new` 关键字。
   4. 在派生方法上使用 `override` 关键字。

### 目标 2.5：通过反射在运行时查找、执行和创建类型

.NET 应用不仅包含代码和数据，还包含*元数据*，即数据的信息。在 .NET 中，这意味着应用程序包含了定义应用程序的代码和描述代码的数据。*特性*（attribute）是存储在 .NET 中的元数据的一种类型。其他元数据包含了有关类型、代码、程序集以及应用程序中所有其他元素的信息。*反射*（Reflection）是在运行时检索这些元数据的过程。这些数据可以被检查并用于做出决策。在本节中，你将学习如何在自己的代码中使用特性以及如何使用反射。你还将学习通过使用 CodeDom 和表达式树在运行时生成代码。

本目标涵盖了：

* 创建和使用特性。
* 使用反射在运行时检查和执行代码。
* 生成代码。

## 创建和使用特性

*使用特性*是向应用程序添加数据的强大方式。特性可以添加到各种类型：程序集、类型、方法、参数和属性。在运行时，你可以查询特性的存在及其设置，然后采取相应的行动。

特性用于多种原因。它们可以存储你想要的任何类型的数据。

### 应用特性

在 C# 中，你通过将特性名称放在方括号（[]）中并放在要应用的特性声明上方来应用特性。





.NET Framework 中属性的一个示例是 `System`.`SerializableAttribute`。此属性表示一个类型是可以被序列化的。.NET Framework 在序列化类型时会检查此属性是否存在，并确保该类型的所有成员也可以被序列化。示例 2-58") 演示了如何应用 `Serializable` 属性。

### 示例 2-58. 应用一个属性
```cs
[Serializable]
class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
}
```

如你所见，.NET Framework 中的实际类名为 `SerializableAttribute`。按照惯例，名称以 `Attribute` 结尾，这样你就可以轻松地区分 .NET Framework 中的属性和其他类型。然而，在使用该属性时，你可以跳过 `Attribute` 后缀。

一个类型可以根据需要应用任意数量的属性。某些属性甚至可以应用多次。例如，你可以使用 `ConditionalAttribute` 来告知编译器，除非指定了特定的编译器选项，否则将忽略某个方法调用。示例 2-59") 演示了如何应用此属性。

### 示例 2-59. 使用多个属性
```cs
[Conditional("CONDITION1"), Conditional("CONDITION2")]
static void MyMethod(){ }
```

如列表所示，属性可以拥有参数。与普通类型一样，这些参数可以被命名为可选的。设置在属性上的值稍可以在运行时进行检查。

属性还有一个特定的应用目标（target）。它可以是应用于整个程序集（assembly）、类、特定方法，甚至是方法的参数的属性。

如果你查看新类库的 `AssemblyInfo.cs`，你可以看到如何显式指定目标的（请参见 示例 2-60")）。

### 示例 2-60. 显式指定属性的目标
```cs
[assembly: AssemblyTitle("ClassLibrary1")]
[assembly: AssemblyDescription("")]
[assembly: AssemblyConfiguration("")]
[assembly: AssemblyCompany("")]
[assembly: AssemblyProduct("ClassLibrary1")]
[assembly: AssemblyCopyright("Copyright ©  2013")]
[assembly: AssemblyTrademark("")]
[assembly: AssemblyCulture("")]
```

这些属性都应用于当前程序集，并描述了关于程序集的某些元数据。

### 读取属性
如果无法检索属性，那么应用属性就没有用了。幸运的是，.NET Framework 支持通过名为 `reflection`（反射）的过程来读取属性。所有其他属性都继承自 `System.Attribute` 类，它定义了一些静态方法，可以检查是否应用了某个属性，并获取属性的当前实例以便进一步检查。

假设你想检查一个类是否应用了 `Serializable` 属性。你可以通过调用 `Attribute` 上的静态方法 `IsDefined`get，如 示例 2-61")所示。

### 示例 2-61. 查看属性是否已定义
```cs
[Serializable]
class Person { }
if (Attribute.IsDefined(typeof(Person), typeof(SerializableAttribute))) { }
```

你也可以检索属性的特定实例，以便查看其属性。示例 2-62") 演示了你如何从 示例 2-59") 获取 `ConditionalAttribute`。

### 示例 2-62. 获取特定的属性实例
```cs
ConditionalAttribute conditionalAttribute =
    (ConditionalAttribute)Attribute.GetCustomAttribute(
    typeof(ConditionalClass),
    typeof(ConditionalAttribute));
string condition = conditionalAttribute.ConditionString; // 返回 CONDITION1
```

`GetAttribute` 和 `GetAttributes` 方法有多个重载，以便你可以检查程序集、方法、模块或参数的属性。

### 创建自定义属性
除了 .NET Framework 内置的属性，你还可以创建自己的属性。自定义属性类必须派自 `System.Attribute`（直接或间接）。例如，xUnit（一个流行的单元测试框架）允许你通过向单元测试上应用属性来对它们进行分类。

### 示例 2-63. 在 xUnit 中使用类别属性
```cs
[Fact]
[Trait("Category", "Unit Test")]
public void MyUnitTest()
{ }

[Fact]
[Trait("Category", "Integration Test")]
public void MyIntegrationTest()
{ }
```

使用 `Trait` 属性的效果非常完美，只是你每次都手动输入 `Category` 和 `Value`。这是容易出错且重复的工作，你希望尽可能避免它。幸运的是，xUnit 为你提供了创建继承自 `Trait` 的属性的选项。示例 2-64") 演示了如何创建一个可以更方便使用的派生属性。

### 示例 2-64. 创建自定义属性
```cs
public class CategoryAttribute : TraitAttribute
{
    public CategoryAttribute(string value)
        : base(value)
    { }
}

public class UnitTestAttribute : CategoryAttribute
{
    public UnitTestAttribute()
        : base("Unit Test")
    { }
}
```

如 示例 2-65")所示，新的 `UnitTestAttribute` 可以轻松地应用到方法上，并将它们标记为 `Unit Test`。

### 示例 2-65. 使用自定义属性
```cs
[Fact]
[UnitTest]
public void MySecondUnitTest()
```

当从头创建自己的自定义属性时，你还必须定义属性可以使用的目标。例如，你可能希望你的属性只被用于方法和参数。

定义属性的使用是通过应用属性来完成的。你可以组合任意数量的目标。你还可以使用 `AllowMultiple` 参数允许在单个类型上应用多个属性实例（请参见 示例 2-67")）。

### 示例 2-67. 为自定义属性设置 AllowMultiple 参数
```cs
[AttributeUsage(AttributeTargets.Class, AllowMultiple = true)]
class MyMultipleUsageAttribute : Attribute{ }
```





在读取属性时，你已经查看了 `reflection`（反射）提供的某些功能。反射允许应用程序收集有关自身的信息并根据这些信息采取行动。反射的执行速度比通常执行静态代码要慢。然而，它可以为你提供静态代码无法提供的灵活性。

反射最基础的示例是获取你拥有的对象的当前类型：

```
int i = 42;
System.Type type = i.GetType();
```

这返回 `System.Int32` 作为 `int` 的类型。`System.Type` 是 .NET Framework 中的一个类，你可以用它来获取任何给定类型的各种元数据。

你什么时候会使用反射？假设你想创建一个插件系统，并且你的系统中有一个包含所有插件的目录。如果有一个新的程序集被放入该位置，你会检查该程序集以它包含的插件，然后将它们添加到你的应用程序中。如果没有反射，这是无法可能的。

## 更多信息：托管扩展性框架 (Managed Extensibility Framework)

如果你正在考虑构建这样一个插件系统，请查看位于 `[`msdn.microsoft.com/en-us/library/dd460648.aspx`](http://msdn.microsoft.com/en-us/library/dd460648.aspx)` 的托管扩展性框架 (MEF)。

在创建插件系统时，你需要某种方法发现插件、获取信息并执行它们。一种方案是创建一个自定义的 `IPlugin` 接口，该接口暴露出可以提供插件信息以及加载插件能力的成员（参见 示例 2-69）。

示例 2-69. 创建一个可以通过反射找到的接口

```
public interface IPlugin
{
    string Name { get; }
    string Description { get; }
    bool Load(MyApplication application);
}
```

现在你已经有了一个自定义的基接口，你可以通过特定的插件类继承此接口来创建一个插件，如 示例 2-70 所示。

示例 2-70. 创建一个自定义插件类

```
public class MyPlugin : IPlugin
{
    public string Name
    {
        get { return "MyPlugin"; }
    }

    public string Description
    {
        get { return "My Sample Plugin"; }
    }

    public bool Load(MyApplication application)
    {
        return true;           
    }
}
```

使用反射，你现在可以检查程序集并检查是否有任何可用插件。你获取的类型可以用于创建插件的实例并使用它。`System.Reflection` 命名空间定义了反射所需的元素。

示例 2-71 演示了如何使用 LINQ 查询从程序集中获取所有插件并构造它们。

示例 2-71. 检查程序集以实现自定义接口的类型

```
Assembly pluginAssembly = Assembly.Load("assemblyname");

var plugins = from type in pluginAssembly.GetTypes()
              where typeof(IPlugin).IsAssignableFrom(type) && !type.IsInterface
              select type;

foreach (Type pluginType in plugins)
{
    IPlugin plugin = Activator.CreateInstance(pluginType) as IPlugin;
}
```

第一行通过名称加载程序集。需要注意的是，如果你多次调用此操作，运行时只会加载一次该程序集。如果你想重新加载程序集，则必须重启你的应用程序。在获取程序集后，你可以检查其中定义了哪些插件，然后构造你的 `IPlugin` 对象。

反射还可以用于检查属性或字段的值。假设你需要创建一个方法，遍历一个对象并选择所有的私有整数字段将它们显示在屏幕上。你可以轻松地通过反射实现此点（参见 示例 2-72）。你使用 `BindingFlags` 枚举来控制反射搜索成员的方式。

示例 2-72. 通过反射获取字段的值

```
static void DumpObject(object obj)
{
    FieldInfo[] fields = obj.GetType().GetFields(BindingFlags.Instance | BindingFlags.NonPublic);

    foreach (FieldInfo field in fields)
    {
        if (field.FieldType == typeof(int))
        {
            Console.WriteLine(field.GetValue(obj));
        }
    }
}
```

反射还可以用于在类型上执行方法。你可以指定方法所需的参数，在运行时 .NET Framework 将检查参数是否匹配，并执行该方法（参见 示例 2-73）。

示例 2-73. 通过反射执行方法

```
int i = 42;
MethodInfo compareToMethod = i.GetType().GetMethod("CompareTo");
int result = (int)compareToMethod.Invoke(i, new object {});

```## 使用 Dom 生成代码

除了在运行时检查类型外，C# 还支持生成代码。这种实现是通过 `CodeDom` 完成的。使用 Dom 的典型场景包括为 ASP.NET、Web 服务、向导或设计器生成代码。CodeDom 位于 `System.CodeDom` 命名空间。你可以将源文件想象为带有容器的树。你有一个顶层容器（称为 `CodeCompileUnit`），它包含了命名空间、类、方法和单个语句。如果你想输出简单的 Hello World 应用程序，你需要创建一个 `CodeCompileUnit`、一个命名空间、一个类以及程序的入口 `Main` 方法，它将调用 `Console.WriteLine`（参见 示例 2-74 "通过 CodeDom 生成 Hello World!")）。

示例 2-74. 通过 CodeDom 生成 Hello World!

```
CodeCompileUnit compileUnit = new CodeCompileUnit();
CodeNamespace myNamespace= new CodeNamespace("MyNamespace");
myNamespace.Imports.Add(new CodeNamespaceImport("System"));
CodeTypeDeclaration myClass = new CodeTypeDeclaration("MyClass");
CodeEntryPointMethod start = new CodeEntryPointMethod();
CodeMethodInvokeExpression cs1 = new CodeMethodInvokeExpression(
    new CodeTypeReferenceExpression("Console"),
    "WriteLine", new CodePrimitiveExpression("Hello World!"));

compileUnit.Namespaces.Add(myNamespace);
myNamespace.Types.Add(myClass);
myClass.Members.Add(start);
start.Statements.Add(cs1);
```

现在编译单元已经完成，你可以使用 `CSharpCodeProvider` 类从它创建源文件，该类位于 `Microsoft.CSharp` 命名空间（参见 示例 2-75）。

示例 2-75. 从 `CodeCompileUnit` 生成源文件

```
CSharpCodeProvider provider = new CSharpCodeProvider();

using (StreamWriter sw = new StreamWriter("HelloWorld.cs", false))
{
    IndentedTextWriter tw = new IndentedTextWriter(sw, "    ");
    provider.GenerateCodeFromCompileUnit(compileUnit, tw,
        new CodeGeneratorOptions());
    tw.Close();
}
```



`HelloWorld.cs` 中生成的输出可见示例 2-76。

示例 2-76. 自动生成的源文件

```
//------------------------------------------------------------------------------
// <auto-generated>
//     此代码由工具生成。
//     Runtime Version:4.0.30319.18010
//
//     对此文件的更改可能会导致不正确的行为，并在重新生成
//     代码时这些更改将会丢失。
// </auto-generated>
//------------------------------------------------------------------------------

namespace MyNamespace {
    using System;

    public class MyClass {       
        public static void Main() {
            Console.WriteLine("Hello World!");
        }
    }
}
```

### Lambda 表达式

`Lambda 函数` 在 C# 3.0 中引入。你可以将 Lambda 表达式认为是创建匿名方法的紧凑方法。

### 更多信息：匿名方法

有关匿名方法的更多信息，请参阅 `[`msdn.microsoft.com/en-us/library/0yw3tz5k.aspx`](http://msdn.microsoft.com/en-us/library/0yw3tz5k.aspx)`。

在处理 lambda 时，你还需要了解 `Func<..>` 和 `Action` 类型。添加这些泛型类型是为了在 .NET Framework 中提供一些预定义的委托类型。当你有一个不返回返回的委托时，使用 `Action`；当你想要返回一个值时，使用 `Func`。在 .NET Framework 4.0 中，两者都可以接受最多 16 个类型参数。

当将 lambda 和 `Func` 类型结合使用时，你可以轻松地创建一个返回两个整数之和的类型，如示例 2-77 所示。

示例 2-77. 使用 lambda 创建 Func 类型

```
Func<int, int, int> addFunc = (x, y) => x + y;
Console.WriteLine(addFunc(2, 3));
```

该 lambda 的类型为 `type Func<int, int, int>`，这意味着它接受两个整数参数并返回一个 `int` 结果。奇怪的 `=>` 符号可以读作“变为”或“对于”。`addFunc` 类型可以读作“x, y 变为 x + y”。

### 表达式树

在使用 lambda 时，你将遇到 `expression trees`（表达式树），它们是以树状数据结构表示的代码。就像 `CodeDom` 可以以树状表示代码一样，表达式树也可以做同样；它们还可以被用于生成代码。

表达式树描述代码，而不是代码本身。表达式树在 LINQ 中被广泛使用。当使用 `Linq To Entities` 查询数据库时，查询并不会执行（如 `Linq To Objects` 所示）。相反，是表达式树描述了查询。随后，该表达式树会被翻译成可以发送到数据库的 SQL 语句。

`System.Linq.Expressions` 空间包含了创建表达式所需的所有类型。你拥有用于调用方法、创建新对象，甚至是用于加法或减法等基本操作的表达式。

来自 `CodeDOM` 的 Hello World 示例也可以作为表达式树创建（参见示例 2-78）。

示例 2-78. 使用表达式树创建“Hello World!”

```
BlockExpression blockExpr = Expression.Block(
 Expression.Call(
      null,
      typeof(Console).GetMethod("Write", new Type[] { typeof(String) }),
      Expression.Constant("Hello ")
     ),
  Expression.Call(
      null,
      typeof(Console).GetMethod("WriteLine", new Type[] { typeof(String) }),
      Expression.Constant("World!")
      )
 );

Expression.Lambda<Action>(blockExpr).Compile()();
```

该表达式首先通过调用 `Console.Write` 和 `Console.WriteLine` 来构建。构建完成后，该表达式被编译为 `Action`（因为不返回任何内容）并被执行。

### 更多信息：表达式树

有关表达式树的更多信息，请参阅 `[`msdn.microsoft.com/en-us/library/bb397951.aspx`](http://msdn.microsoft.com/en-us/library/bb397951.aspx)`。

## 思考实验

### 优化你的代码

在这个思考实验中，应用你关于此目标中学到的知识。你可以在本书末尾的答案 部分找到这些问题的答案。

你正在创建自己的优化的对象关系映射器。你允许用户将类型一对一地映射到数据库中的表。出于安全考虑，你还使用了特殊的属性。例如，可以为类型装饰 `AuthorizeAttribute` 属性，以确保只有特定用户可以访问某个表。你在应用程序中使用了大量反射，并开始看到一些性能问题。你还在考虑一个生成器来创建精确映射到数据库的类型。

1. 为什么你使用属性而不是继承接口？
2. 针对性能问题，你可以做什么？
3. 你将使用什么技术来创建生成器？

## 目标总结

- C# 程序集存储代码和元数据。
- 属性是在运行时应用的元数据类型。
- 反射是检查元数据的过程。
- 通过反射你可以创建类型、调用方法、读取属性等。
- 表达式树描述代码并可以被编译。

### 目标回顾

回答以下问题以测试你对目标的掌握。

1. 你想读取类上的私有字段。你需要哪些 `BindingFlag`？（选择所有适用项）
   - Instance
   - DeclaredOnly
   - Static
   - NonPublic

2. 你需要创建一个可以多次应用于方法或参数的属性。你应该使用哪种语法？
   - `[AttributeUsage(AttributeTargets.GenericParameter | AttributeTargets.Method,AllowMultiple = true)]`
   - `[AttributeUsage(AttributeTargets.Method | AttributeTargets.Parameter, AllowMultiple = true)]`
   - `[AttributeUsage(AttributeTargets.All)]`
   - `[AttributeUsage(AttributeTargets.Method | AttributeTargets.Parameter)]`

3. 你想创建一个根据特定值过滤字符串列表的委托。你应该使用什么种类型？
   - `Action<bool, IEnumerable<string>>`
   - `Func<IEnumerable<string>, IEnumerable<string>>`
   - `Func<string, IEnumerable<string>, IEnumerable<string>>`
   - `Func<IEnumerable<string>>`

### 目标 2.6: 管理对象的生命周期

在 C++ 等语言中，你必须担心内存管理。使用指针并尽可能管理内存对于编写应用程序是必要的。忘记释放某些内存会导致内存泄漏。在 C# 中，情况不同。C# 是一种托管语言，使用垃圾回收器在需要时释放内存。只要你只使用托管对象，垃圾回收器就会让你无需担心内存管理。然而，在编写应用程序时，你经常会跨越边界使用非托管资源，如数据库连接或文件句柄。在这种情况下，你需要尽快释放这些资源。在本目标中，你将学习如何处理非托管资源，以及在需要时影响垃圾回收。





本目标涵盖了如何：

* 管理未托管资源。
* 实现并使用 `IDisposable`。
* 管理终结和垃圾回收。

## 了解垃圾回收

在 `C#` 中构建应用程序时，你依赖于 `C#` 为你管理所有内存这一事实。当你创建一个新对象时——无论是字符串、`int` 还是自定义类型——你知道 `.NET Framework` 会以某种方式分配内存并将你的对象放入其中。大多数时候，这个过程完全在后台（通过 `CLR`）完成的，你完全不需要理会它。但对其工作原理有基本的了解有助于你理解为什么会发生这些情况，并在必要时优化你的代码。

在你的代码执行期间，`CLR` 在内存中有两个地方可以存储项。一个是 `stack`（栈），另一个是 `heap`（堆）。`stack` 跟踪你代码中正在执行的内容，而 `heap` 跟踪你的对象。

当然，这是一种过度简化。值类型可以同时存储在 `stack` 和 `heap` 中。对于 `heap` 上的对象，`stack` 上总有一个指向它的引用。大对象存放在 `heap` 的特殊部分。但基本上，这就是两种内存类型之间的区别。

`stack` 在方法结束时会自动清除。`CLR` 负责处理这一点，你不需要担心。

`heap` 则是另一回事——它由 `garbage collector`（垃圾回收器）管理。在没有垃圾回收器的未托管环境中，你必须不断跟踪哪些对象被分配在 `heap` 上，并且你需要显式地释放它们。在 `.NET Framework` 中，这是通过 `garbage collector` 完成的。

`garbage collector` 使用`标记-压缩算法`（mark and compact algorithm）工作。收集的 `mark`（标记）阶段会检查 `heap` 上的哪些项仍被 `root item`（根项）引用。`root` 可以是静态字段、方法参数、局部变量或 CPU 寄存器。如果 `garbage collector` 在 `heap` 上发现了一个“存活”的项，它就会标记该项。在检查整个 `heap` 后，开始 `compact`（压缩）操作。然后 `garbage collector` 将所有存活的堆对象移动在一起，释放所有其他对象的内存。

为了做到这一点，`garbage collector` 必须确保在执行所有标记和压缩操作期间没有状态发生变化。正因如此，在执行收集操作时所有线程都会冻结。它还需要确保所有指向存活对象的引用都是正确的。在移动对象后，`garbage collector` 将修复所有现有的对象引用。

这可能会产生巨大的性能影响。当你正在执行一个复杂的、应该尽可能快返回给用户的重要操作时，突然 `garbage collector` 介入了，你必须等待它完成后才能继续。

但对我们幸运的是，`garbage collector` 是非常聪明的。只有当 `heap` 上没有足够的空间构造新对象时（或当 `Windows` 发出内存不足信号时），`garbage collector` 才会开始清理。所以只要内存中有足够的空间，你就永远不会察觉到垃圾回收的任何迹。当它发生时，它会尝试在应用程序使用率较低的时刻进行。

当垃圾回收开始时，它只收集 `Generation 0`（第 0 代）。这意味着什么？嗯，当执行清理时，存活项（因为它们仍被引用）会被提升到更高的 `generation`（代）。它们是寿命更长的对象，`garbage collector` 假设寿命较长的对象可能会留存一段时间。因此，`garbage collector` 关注 `Generation 0` 中的对象。它们是刚刚创建的，可能在短时间内就不再需要。只有当 `garbage collector` 无法通过清理 `Generation 0` 释放足够的内存时，才会触及其他代。

简之，这就是垃圾回收的工作原理：它从 `heap` 中移除不再需要的项，并确保如果对象未被使用，就无法存活并占用内存。

## 管理未托管资源

如果你只与托管资源一起，这些就足够了。保持如字符串、数字和其他托管类型等对象完全由 `garbage collector` 处理。但当你开始访问 `unmanaged resources`（未托管资源）时，情况就变了。

未托管资源可以是网络连接、文件句柄、窗口句柄等。你必须显式地释放这些项。否则，你将得到诸如“文件正在使用中”的错误，或者因为所有连接都在使用中而无法连接到数据库。

由于由于，`C#` 支持 `finalization`（终结）的概念。这种机制允许类型在垃圾回收之前进行清理。理解的是，`C#` 终结器（finalizer）等同于 `C++` 析构函数。`C++` 析构函数是可以确定性调用的。你知道它们何时将执行。但在 `C#` 中，你无法确定终结器何时被调用。它只会在 `garbage collector` 确定你的对象准备好被清理时才会发生。

`C#` 中的 `finalizer` 需要一些特殊的语法，就像构造函数一样。你需要在类名前加上波号（`~`）来创建一个终结器。示例 2-79 显示了如何声明终结器。

示例 2-79. 添加终结器

```
public class SomeType
{
    ~SomeType()
    {
        // 当 finalize 方法执行时调用此代码
    }
}
```

在终结器内部，你可以清理其他资源并确保释放所有内存。例如，在 `C#` 中处理 `File` 时，你必须在删除文件之前释放任何未托管资源，如示例 2-80 所示。

示例 2-80 不关闭文件将导致错误

```
StreamWriter stream = File.CreateText("temp.dat");
stream.Write("some data");

File.Delete("temp.dat"); // 因为文件已打开，将抛出异常
```

如所述，终结器仅在发生垃圾回收时才被调用。你可以通过添加 `GC.Collect` 调用来强制执行，如示例 2-81 所示。`WaitForFinalizers` 行确保在代码继续之前所有终结器已运行。`garbage collector` 管理内存非常智能，不建议你自己调用 `GC.Collect`。

示例 2-81. 强制垃圾回收

```
StreamWriter stream = File.CreateText("temp.dat");
stream.Write("some data");
GC.Collect();
GC.WaitForFinalizers();
File.Delete("temp.dat");
```

在 `Release` 模式下运行这段代码时，`garbage collector` 将发现没有指向 `stream` 的引用，并将释放与 `Stream-Writer` 实例相关的内存。这将运行终结器，从而释放对 `temp.dat` 文件的任何句柄（在调试模式下，编译器将确保引用在方法结束之前不会被垃圾回收）。

重要的是，终结器会增加对象的寿命。因为终结代码也必须运行，`.NET Framework` 将对象的引用保留在一个特殊的终结队列中。一个额外的线程会根据执行上下文在认为合适的时间运行所有终结器。这延迟了具有终结器的类型的垃圾回收。





这并不是一种理想的情况。你不应该依赖垃圾收集器在某个时刻运行终结器来关闭你的文件。相反，你应该自己执行此操作。为了给你提供显式释放非托管资源的机会，C# 提供了 `IDisposable` 接口的概念，你可以在示例 2-82 中看到它。

示例 2-82.`IDisposable` 接口

```
public interface IDisposable
{
     void Dispose();
}
```

`IDisposable` 接口提供了一个方法：`Dispose`，它将立即释放任何非托管资源。示例 2-82 中的示例也可以写像示例 2-83 中那样所示。

示例 2-83.调用 `Dispose` 释放非托管资源

```
StreamWriter stream = File.CreateText("temp.dat");
stream.Write("some data");
stream.Dispose();
File.Delete("temp.dat");
```

但如果在调用 `stream.Dispose()` 之前发生异常怎么办？为了确保你的资源始终能被清理，你需要将所有实现 `IDisposable` 的类型封装在 `try/finally 语句`中。因为这非常常见，C# 有一个专门的语句用于此：`using 语句`。`using` 语句会被编译器翻译成一个 `try/finally` 语句，该语句会对对象调用 `Dispose`。正因如此，`using` 语句只能与实现 `IDisposable` 的类型配合。

```
using (StreamWriter sw = File.CreateText("temp.dat"))
{ }
```

`using` 语句确保 `Dispose` 总是被调用。只要可能，每个实现 `IDisposable` 的类型都应该在 `using` 语句中使用。这样你就可以确保清理了所有非托管资源。

在释放一个项后，你就不能再使用它了。使用已释放的项将导致 `ObjectDisposedException`。

如果你在处理 `IDisposable` 对象时也想使用 `catch` 语句，你需要通过手动编写 `try`/`catch`/`finally` 语句来实现，并在 `finally` 子句中调用 `Dispose`。

### 更多信息：异常处理

有关如何使用异常处理的更多信息，请参见目标 1.5：实现异常处理。

### 实现 `IDisposable` 和终结器

正确地创建一个实现 `IDisposable` 和终结器的自定义类型类型并不是一项轻易的任务。

例如，假设你有一个围绕非托管文件资源的包装类。你实现了 `IDisposable`，这样你类的类的用户就可以在他们想要时立即进行清理工作。你还实现了一个终结器，以防他们忘记调用 `Dispose`。示例 2-84 展示了如何这样做。

示例 2-84.实现 `IDisposable` 和终结器

```
using System;
using System.IO;

class UnmangedWrapper : IDisposable
{
    public FileStream Stream { get; private set; }

    public UnmangedWrapper()
    {
        this.Stream = File.Open("temp.dat", FileMode.Create);
    }

    ~UnmangedWrapper()
    {
        Dispose(false);
    }

    public void Close()
    {
        Dispose();
    }

    public void Dispose()
    {
        Dispose(true);
        System.GC.SuppressFinalize(this);
    }

    public void Dispose(bool disposing)
    {
        if (disposing)
        {
            if (Stream != null)
            {
                Stream.Close();
            }
        }
    }
}
```

关于此实现有几点需要注意：

* 终结器只调用 `Dispose` 并向 `disposing` 传递 `false`。

* 带有布尔值参数的额外 `Dispose` 方法执行实际工作。此方法检查它是在显式 `Dispose` 中调用的，还是从终结器调用的：

    * 如果终结器调用了 `Dispose`，你什么都不需要做，因为 `Stream` 对象也实现了终结器，垃圾收集器会负责调用 `Stream` 实例的终结器。你无法确定它是否已经被调用，所以最好交给垃圾收集器处理。

    * 如果显式调用 `Dispose`，你就关闭底层的 `FIleStream`。在编写此方法时保持防御性很重要；始终检查任何可能的异常源。`Dispose` 可能会被多次调用，这不应该引起任何错误。

* 普通的 `Dispose` 方法调用 `GC.SuppressFinalize(this)` 以确保对象被移除。

### 考试贴士

了解实现 `IDisposable` 和终结器之间的区别是重要的。两者都会清理你的对象，但终结器是由垃圾收集器调用的，而 `Dispose` 方法可以从代码调用。

### 弱引用

有时你必须处理创建非常耗时的大对象。例如，从数据库检索的列表。如果能将这些项留在内存中就太好了；但这增加了你应用程序的内存负载，而且该列表可能不再被需要。

这就是 `WeakReference` 类型可以用的地方。`WeakReference` 正如其名所示，并不持有堆上对象的真实引用，因此它可以被垃圾收集。但在垃圾回收尚未发生时，你仍然可以通过 `WeakReference` 访问该项。示例 2-85 展示了如何使用。

示例 2-85.使用 `WeakReference`

```
static WeakReference data;
public static void Run()
{
    object result = GetData();
    // GC.Collect(); 注消此行将使 data.Target 为空
    result = GetData();
}

private static object GetData()
{
    if (data == null)
    {
        data = new WeakReference(LoadLargeList());
    }

    if (data.Target == null)
    {
        data.Target = LoadLargeList();
    }
    return data.Target;
}
```

使用 `WeakReference` 缓存场景的完整解决方案。如果你想实现缓存，应该定义一个算法来决定哪些项应该从缓存中移除。在移除时，将引用转换为 `WeakReference` 并交给垃圾收集器。

## 思考实验

**清理你的东西**

在思考实验中，应用你对本目标所学的知识。你可以在本章末尾的答案部分找到这些问题的答案。

你创建了第一个 Windows 8 应用程序。这是一个有趣的游戏，允许用户拍摄一段自己描述某个单词的视频。其他人来猜；这样他们就能获得积分，从而创建更长的视频。





有一天，你醒来时突然发现微软选择了你的应用程序作为它们的“每周应用”。你运行游戏所有逻辑的 Web 服务器正因为突然的走红而在用户负载下颤抖。内存和 CPU 的压力远高于你的预期。你本有一些类型完全可以作为值类型，但在创建应用程序时，你只使用了类（classes）。

1. 尽可能使用值类型如何提高你的性能？或者，你的性能是否会进一步恶化？
2. 为什么实现 `IDisposable` 对于减少内存压力很重要？在完成对元素的操作后立即对其调用 `Dispose` 总是最佳选择吗？
3. 你是否应该对所有实现了 `IDisposable` 的类型都实现终析器（finalizer）？
4. 你有一些被频繁使用的项。将它们放在静态字段中以避免每次都重新创建它们，这样做是明智的吗？

## 目标总结

* C# 中的内存由栈（stack）和堆（heap）组成。
* 堆由垃圾回收器（garbage collector）管理。
* 垃圾回收器释放任何不再被引用的内存。
* 终析器是一种特殊的代码，当垃圾回收器删除一个对象时会运行它。
* 可以实现 `IDisposable` 以确定性的方式释放任何非托管资源。
* 实现 `IDisposable` 的对象可以使用 `using` 语句，以确保它们始终被释放。
* 可以使用 `WeakReference` 来维护对项的引用，这些项在需要时可以被垃圾回收。

### 目标回顾

回答以下问题以测试你对本目标中信息的掌握情况。你可以在章节末尾的 答案 部分找到这些问题的答案以及每个每个选项为何正确或错误的解释。

1. 你正准备执行一段对性能敏感的代码。你担心在代码执行期间会发生垃圾回收。在执行代码之前，你应该调用哪种方法？
    1. `GC.RemoveMemoryPressure()`
    2. `GC.SuppressFinalize()`
    3. `GC.Collect()`
    4. `GC.WaitForPendingFinalizers()`

2. 一个实现了 `IDisposable` 的对象被作为参数传递给你的类。你应该将该元素封装在 `using` 语句中吗？
    1. 是的，否则可能会发生内存泄漏。
    2. 否，你应该对该对象调用 `Close`。
    3. 否，你应该使用 `try`/`finally` 语句并亲自调用 `Dispose`。
    4. 否，调用方法应该使用 `using` 语句。

3. 你的应用程序在使用大量内存。你应该使用哪种解决方案？
    1. 将所有引用转换为 `WeakReferences`。
    2. 在完成使用后将所有引用都置为 `null`。
    3. 使用缓存算法来决定哪些对象可以释放。
    4. 使用后台线程按计划间隔调用 `GC.Collect()`。

### 目标 2.7：操作字符串

文本是几乎每个应用程序中最重要的概念之一，因此 C# 在处理文本时提供了非常多的支持。所有这些支持都围绕内置类型 `System.String` 展开。在创建应用程序时，你经常需要处理字符串。例如，将字符串相加、在另一个字符串中搜索特定的字符串或字符、遍历字符串，最后对其进行格式化以显示，都是常见做法。你将学习如何在执行这些步骤的同时，兼顾易用性和性能。

本目标涵盖了如何：
* 操作字符串。
* 搜索字符串。
* 穷举字符串。
* 格式化字符串。

## 在 .NET Framework 中使用字符串

C# 中的 `string` 是一个 `String` 类型的对象，其值为文本。`string` 对象内部包含一个 `Char` 对象数组。`string` 有一个 `Length` 属性，显示它包含的 `Char` 对象的数量。`String` 是一个**引用类型**，但看起来看起来像值类型（例如，相等运算符 `==` 和 `!=` 被重载为按值进行比较，而不是按引用）。

在 C# 中，你可以同时用 `String` 和 `string` 来引用 `string`。你可以使用任何适合你的命名规范。`string` 关键字只是 .NET Framework 中 `String` 的别名。

字符串的特殊特性之一是它是**不可变的**（immutable），因此它在创建后无法被更改。对字符串的任何更改都会创建一个新字符串。这就是为什么所有的 `String` 操作方法都返回一个 `string`。

不可变性在许多场景中非常有用。如果你知道一个结构永远不会改变，对其进行推理会更容易。由于它无法被修改，因此它本质上是线程安全的。它更安全，因为没有人可以捣乱它。突然创建像撤销/重做的功能变得简单得多，因为你的数据结构是不可变的，你只需要维护状态的快照。

但不可变数据结构也有负面影响。示例 2-86 中的代码看起来很无害，但它会为循环中的每次迭代创建一个新字符串。它消耗了大量不必要的内存，并说明了为什么在处理字符串时必须小心。

示例 2-86. 创建大量字符串

```
string s = string.Empty;

for (int i = 0; i < 10000; i++)
{
    s += "x";
}
```




需要记住的一点是，`StringBuilder` 并不总是能提供更好的性能。在拼接一组固定字符串时，编译器可以对此进行优化，并将单独的拼接操作合并为单次操作。当你处理任意数量的字符串时（例如循环示例所示），`StringBuilder` 是一个更好的选择（在这个示例中，你也可以使用 `new String("x", 10000)` 来创建字符串；但在处理更多样化的数据时，这是无法实现的）。

### `StringWriter` 和 `StringReader`

.NET Framework 中的某些 API 要求使用 `TextWriter` 或 `TextReader` 才能工作。这些 API 无法直接与字符串或 `StringBuilder` 协作。因如此，.NET Framework 增加了 `StringReader` 和 `StringWriter` 类。这些类`适配`了 `StringBuilder` 的接口，以便它们可以使用在需要 `TextWriter` 或 `TextReader` 的地方。

在内部，`StringWriter` 和 `StringReader` 使用 `StringBuilder`。它们所做的仅仅是将 `StringBuilder` 的接口适配为 `TextWriter` 和 `TextReader` 的接口。

.NET Framework 中期望 `TextWriter` 实例的方法之一是 `XmlWriter.Create`。通常，你会传递一个 `StreamWriter` 实例以便创建一个新的 XML 文件。但当你只需要在内存中获取生成的 XML 时，可以传递一个 `StringWriter`（参见 示例 2-89）。

示例 2-89. 使用 `StringWriter` 作为 `XmlWriter` 的输出

```
var stringWriter = new StringWriter();
using (XmlWriter writer = XmlWriter.Create(stringWriter))
{
    writer.WriteStartElement("book");
    writer.WriteElementString("price", "19.95");
    writer.WriteEndElement();
    writer.Flush();
}
string xml = stringWriter.ToString();
```

此时 `xml` 的值为：

```
<?xml version=\"1.0\" encoding=\"utf-16\"?>
    <book>
        <price>19.95</price>
    </book>
```

当使用 `XmlReader` 时，你可以解析某些 XML 并访问各个元素。`XmlReader` 期望 `TextWriter` 实例，因此你可以向它传递一个 `StringReader`（参见 示例 2-90）。

示例 2-90. 使用 `StringReader` 作为 `XmlReader` 的输入

```
var stringReader = new StringReader(xml);
using (XmlReader reader = XmlReader.Create(stringReader))
{
    reader.ReadToFollowing("price");
    decimal price = decimal.Parse(reader.ReadInnerXml(),
        new CultureInfo("en-US")); // 确保正确读取小数部分
}
```

### 搜索字符串

处理字符串时，你经常会在另一个字符串内部查找 `substring`（以解析某些内容或检查有效的用户输入或其他场景）。

`String` 类提供了几个方法，可以帮助你执行各种搜索操作。最常用 `IndexOf`、`LastIndexOf`、`StartsWith`、`EndsWith` 和 `SubString`。

需要记住的一点是，字符串方法可能是`文化敏感的`。这就是为什么大多数方法都接受 `StringComparison` 枚举的实例。在处理字符串时，务必避免使用不使用显式 `StringComparison` 值的方法。

#### 更多信息：处理字符串时的最佳实践

有关处理字符串时的最佳实践的更多信息，请参阅 MSDN 文档：[`msdn.microsoft.com/en-us/library/dd465121.aspx`](http://msdn.microsoft.com/en-us/library/dd465121.aspx)。

`IndexOf` 返回字符或子字符串在字符串中首次出现的的索引。如果找不到该值，它返回 `-1`。`LastIndexOf` 也是如此，只不过该方法从字符串的末尾开始搜索并向开头移动。查看 示例 2-91 获取 `IndexOf` 和 `LastIndexOf` 的示例。

示例 2-91. 使用 `IndexOf` 和 `LastIndexOf`

```
string value = "My Sample Value";
int indexOfp = value.IndexOf('p'); // 返回 6
int lastIndexOfm = value.LastIndexOf('m'); // 返回 5
```

`StartsWith` 和 `EndsWith` 分别检查字符串是否以某个特定值开头或结束。它根据结果返回 `true` 或 `false`。示例 2-92 显示了如何使用它们。

示例 2-92. 使用 `StartsWith` 和 `EndsWith`

```csharp
string value = "<mycustominput>";
if (value.StartsWith("<")) { }
if (value.EndsWith(">")) { }
```

`Substring` 可用于从字符串中提取部分字符串。你可以通过 `IndexOf` 或 `LastIndexOf` 来计算这些索引。示例 2-93 显示了如何使用它们。

示例 2-93. 使用子字符串

```csharp
string value = "My Sample Value";
string subString = value.Substring(3, 6); // 返回 'Sample'
```

另一种搜索字符串的方法是使用正则表达式。正则表达式在验证用户输入时（如电子邮件地址、邮政编码或日期）非常有用。示例 2-94 显示了如何使用它们。

示例 2-94. 使用正则表达式更改字符串

```csharp
string pattern = "(Mr\\? |Mrs\\? |Miss |Ms\\? )";
string[] names = { "Mr. Henry Hunt", "Ms. Sara Samuels", "Abraham Adams", "Ms. Nicole Norris" };

foreach (string name in names)
    // 替换逻辑...
```

### 枚举字符串

字符串是字符数组。你可以像对待典型的集合一样枚举字符串。由于字符串实现了 `IEnumerable` 和 `IEnumerable<char>`，它暴露了你可以使用的 `GetEnumerator` 方法。

你可以使用 `foreach` 循环遍历字符串以检查所有字符，示例 2-95 所示。

示例 2-95. 枚举字符串

```csharp
string value = "My Custom Value";
foreach (char c in value)
    Console.WriteLine(c);
```

将字符串拆分为单词并对它们进行迭代也是可能的。下面的代码按空格分割句子；它返回一个可以迭代的 `IEnumerable`：

```csharp
foreach (string word in "My sentence separated by spaces".Split(' ')) { }
```




```
class Person
{
    public Person(string firstName, string lastName)
    {
        this.FirstName = firstName;
        this.LastName = lastName;
    }

    public string FirstName { get; set; }
    public string LastName { get; set; }

    public override string ToString()
    {
        return FirstName + LastName;
    }
}

Person p = new Person("John", "Doe");
Console.WriteLine(p); // Displays 'John Doe'
```

当一个对象有多种字符串表示时，仅重写 `ToString` 是是不够的。例如，`Temperature` 对象可以以华氏度、摄度或开尔文显示其温度。整数值也可以以多种方式显示。它可能代表一个电话号码或一个金额。

为了实现这种行为，你可以使用格式化字符串，格式化字符串是描述对象应该如何显示的字符串。`.NET Framework` 将它们用于数值类型、日期、时间以及枚举，如示例 2-97 所示。

示例 2-97. 使用货币格式字符串显示数字

```
double cost = 1234.56;
Console.WriteLine(cost.ToString("C",
                  new System.Globalization.CultureInfo("en-US")));
// Displays $1,234.56
```

在显示日期和时间值时，可以使用相同的方法。根据文化（culture），格式化输出可能完全不同。示例 2-98 显示了如何针对英语文化为 `DateTime` 使用不同的格式化字符串。

示例 2-98. 使用不同的格式字符串显示 `DateTime`

```
DateTime d = new DateTime(2013, 4, 22);
CultureInfo provider = new CultureInfo("en-US");
Console.WriteLine(d.ToString("d", provider)); // Displays 4/22/2013
Console.WriteLine(d.ToString("D", provider)); // Displays Monday, April 22, 2013
Console.WriteLine(d.ToString("M", provider)); // Displays April 22
```

在格式化值时，提供正确的 `CultureInfo` 是重要的。它包含了关于特定类型在特定文化中显示的所有必要信息。同样，确保在将值保存到数据库时（例如，以一种与文化无关（culture-insensitive）的方式进行操作）也是重要的。如果加载的是文化无关的数据，它可以根据查看数据的用户对其进行格式化。

你还可以在你自己的类型上实现这种自定义格式化。你通过在你的类型上创建一个 `ToString(string)` 方法来实现这一点。在这样做时，请确保你符合 `.NET Framework` 中的标准格式化字符串。

例如，`G` 格式化字符串应该代表你的对象的通用格式（与调用 `ToString()` 相同），且格式化字符串的 `null` 值也应该显示通用格式。示例 2-99 显示了如何这样做。

示例 2-99. 在类型上实现自定义格式化

```
class Person
{
 ...
    public string ToString(string format)
    {
        if (string.IsNullOrWhiteSpace(format) || format = "G") format = "FL";

        format = format.Trim().ToUpperInvariant();

        switch (format)
        {
            case "FL":
                return FirstName + " " + LastName;
            case "LF":
                return LastName + " " + FirstName;
            case "FSL":
                return FirstName + ", " + LastName;
            case "LSF":
                return LastName + ", " + FirstName;
            default:
                throw new FormatException(String.Format(
                        "The '{0}' format string is not supported.", format));
        }
    }
}
```

### `IFormatProvider` 和 `IFormattable`

在格式化字符串时，你还可以使用 `IFormatProvider`。`IFormatProvider` 有方法 `GetFormat(Type)`，它返回用于格式化类型的特定格式信息。所有的 `CultureInfo` 对象都实现了 `IFormatProvider`。当格式化字符串或 `DateTime` 时，`CultureInfo` 对象会返回特定文化的 `NumberFormatInfo` 或 `DateTimeFormatInfo`。这样，你就可以通过向 `ToString` 方法传递 `CultureInfo` 对象将字符串格式化为特定文化。

在类型上实现你自己的 `ToString` 格式化方法时，你也可以选择接受 `IFormatProvider`。这样做时，你可以实现 `IFormattable` 接口。使用 `IFormattable` 可以确保你在格式化字符串时可以与 `.NET Framework` 集成。

在实现 `IFormattable` 时，你可以通过 `Convert` 类支持字符串转换（该类有一个接受对象和 `IFormatProvider` 的重载）。你还可以支持复合格式化，其中你的类型被用于与其他类型一起创建复合字符串（参见示例 2-100）。

示例 2-100. 创建复合字符串

```
int a = 1;
int b = 2;
string result = string.Format("a: {0}, b: {1}", a, b);
Console.WriteLine(result); // Displays 'a: 1, b: 2'
```

## 思考实验

**显示某些文本**

在思考实验中，应用你对本目标的所学。这些问题的答案可以在末尾的答案 部分找到。

你正在开发一个本地化的应用程序，用于时间跟踪。团队可以使用它跟踪各种项目和任务，并确保计费时间是正确的。该应用程序由基于 ASP.NET 的前端和使用 C# 的桌面程序组成。突然，你的经理宣布应用程序要走向全球化。你目前只支持英语；在最初设计应用程序时没有考虑到全球化。现在你需要支持西班牙语和德语。

1. 列出更新应用程序程序的注意事项。

## 目标总结

- 字符串是不可变的引用类型。
- 在进行大量字符串操作时，你应该使用 `StringBuilder`。
- `String` 类提供了许多处理字符串的方法，如 `IndexOf`、`LastIndexOf`、`StartsWith`、`EndsWith` 和 `Substring`。
- 字符串可以作为字符集合进行枚举。
- 格式化是将对象转换为字符串的过程。
- 你可以使用格式字符串更改对象转换为字符串的方式。
- 你可以为自己的类型实现格式化。

## 目标复习

回答以下问题以测试你对本目标的掌握。这些问题的答案以及每个选项为何正确或错误的解释可以在末尾的答案 部分找到。

1. 你想根据法语显示 `DateTime` 的日期部分。你应该使用哪种方法？
   - `dt.ToString(new CultureInfo("fr-FR"))`
   - `dt.ToString("M", new CultureInfo("fr-FR"))`
   - `dt.ToString("d")`
   - `dt.ToString("d", new CultureInfo("fr-FR"))`

2. 你希望你的类型能够从字符串进行转换。你应该实现哪个接口？
   - `IFormattable`
   - `IFormatProvider`
   - `IComparable`
   - `IConvertible`

3. 你正在解析一段大型文本并根据复杂的算法替换值。你应该使用哪个类？





1. `StringReader`
2. `StringBuilder`
3. `StringWriter`
4. `String`

## 章节总结

* C# 使用如 `class`、`struct`、`interface` 和 `enum` 等类型。类型可以拥有如 `methods`、`events`、`fields`、`properties`、`indexed properties` 和 `constructors` 等成员。

* 在处理类型时，你有时需要在它们之间进行转换。可以通过隐式或显式的方式完成。在创建自定义类型时，你可以添加对这些类型转换的支持。

* 你使用如 `public`、`private`、`protected`、`internal` 和 `protected internal` 等访问器来强制封装和可访问性。属性可以用于封装数据。

* 可以通过继承创建对象层次结构，你可以同时拥有接口继承和类继承。通过将成员标记为 `virtual`，派生类可以重写该成员。

* 反射（Reflection）是在运行时检查元数据的过程。特性（Attributes）可以为类型添加元数据。

* C# 是一种托管语言，这意味着垃圾回收器会确保在所有托管对象不再使用时，它们都会从内存中释放。

* 字符串可用于文本。`string` 类型是不可变的。`.NET Framework` 提供了 `StringBuilder` 来处理大量文本。字符串可以被搜索、枚举和格式化显示。

## 答案

本节包含本章中思维实验的解决方案以及课后复习问题的答案。

## 目标 2.1: 思维实验

1. 在构建网商店时可以使用的一些类型有：`Order`、`OrderLine`、`Product`、`Customer`、`Review`、`SearchCriteria`、`BusinessRule`。

2. 在设计系统时，你应该关注行为，然后确保你有相应的数据来支持它。例如，与其公开暴露订单包含的 `OrderLines`，你应该暴露一个方法 `AddProduct(product, amount)`，该方法在内部创建一个 `OrderLine` 并确保 `Order` 遵循所有的业务规则。

3. 通过确保你拥有正确的构造函数，你类型的用户可以很容易地看到需要哪些数据。通过使用枚举 `enums`（例如用于 `Order` 状态和 `Customer` 状态），你可以提高代码的可读性。通过为业务规则使用基类，你可以使系统更具扩展性，从而轻松定义其他业务规则。

## 目标 2.1: 复习

1. **正确答案：** B

    1. **错误：** 构造函数用于创建新类型的实例。
    2. **正确：** 索引器属性允许类型的用户轻松访问表示类数组集合的类型。
    3. **错误：** 使类型泛型化允许你在你的集合中存储多个不同的类型。
    4. **错误：** 静态属性无法访问集合的实例数据。

2. **正确答案：** A

    1. **正确：** 将你的泛型类型参数限制为 `class` 允许类仅与引用类型一起。
    2. **错误：** 这将限制类仅与值类型一起，而不是引用类型。
    3. **错误：** 这将限制类与具有空默认构造函数的类型一起。它既可以是值类型也可以是引用类型。
    4. **错误：** 这限制类仅与实现了 `IDisposable` 接口的类型一起。

3. **正确答案：** C

    1. **错误：** 传递未初始化的 `struct` 将导致使用未赋值本地变量的编译错误。
    2. **错误：** 传递未初始化的 `struct` 将导致使用未赋值本地变量的编译错误。
    3. **正确：** 传递未初始化的 `struct` 将导致使用未赋值本地变量的编译错误。
    4. **错误：** 传递未初始化的 `struct` 将导致使用未赋值本地变量的编译错误。

## 目标 2.2: 思维实验

1. `ArrayList` 是非泛型的；它们可以到并且。
2. 使用泛型集合将避免装箱和拆箱。

## 目标 2.2: 复习

1. **正确答案：** B

    1. **错误：** 自定义类型之间的转换默认不存在。
    2. **正确：** 添加运算符 operator 将允许用户使用。





3. 因为一个类型可以实现多个接口，所以你可以使用接口来暴露该类型的部分成员。通过使用显式接口实现，你还可以隐藏某些仅在特定情况下才可见的成员。通过这种方式，你可以在特定时刻暴露较少成员来增强类型的公共接口。

## 目标 2.3: 复习

1. **正确答案：** D
    - **错误：** 具有 `public` 成员的 `public` 类可以从其他程序集访问，不受任何限制。
    - **错误：** 其他程序集中的类型可以派生该类并访问 `protected` 方法。
    - **错误：** 其他程序集中的类型无法派生该类，但同一程序集中的其他类型可以访问该方法。
    - **正确：** `internal` 类不能在程序集之外被访问。`protected` 方法只能由派生类型访问。

2. **正确答案：** B
    - **错误：** `protected` 字段无法被类外的其他类型读取。
    - **正确：** `public` 属性可以被所有其他类型读取。`protected set` 修饰符将更改限制在派生类型中。
    - **错误：** `protected` 属性无法被类外的其他类型读取。
    - **错误：** 这将产生编译错误，因为 `get` 访问器的访问修饰符必须比属性更严格。`public` 的限制性比 `protected` 小。

3. **正确答案：** A
    - **正确：** 隐式实现 `IA` 将使其成为默认实现。当处理该类的引用时，将调用此方法。显式实现 `IB` 则会在处理对 `IB` 接口的引用时调用针对 `IB` 的实现。
    - **错误：** 当同时显式实现 `IA` 和 `IB` 时，你需要将类的类的引用强制转换为一个或两个接口类型，以调用该方法。
    - **错误：** 同时隐式实现 `IA` 和 `IB` 不会允许为 `IB` 提供不同的实现。
    - **错误：** 隐式实现 `IB` 会使 `IB` 成为默认实现，而不是 `IA`。

## 目标 2.4: 思想实验

1. 问题在于 C# 类不支持多重继承，但你可以拥有多个接口继承。当像 `IDisposable` 这样的类型被实现为基类时，你只能派生自该类。派生自其他自定义类型是不可能的。

2. 实现搜索标准的最佳方法是使用类继承。通过创建一个接受输入并在条目上执行特定过滤的 `abstract` 类，你可以尽可能地重用代码。派生的标准只需要指定过滤表达式（可能通过 lambda 表达式）以及通过构造函数指定它们的精确参数即可。

3. `IUnknown` 在此场景下是不可用的；它只用于处理非托管代码。当你处理想要释放的非托管资源时，应该使用 `IDisposable`。在这种情况下，没有必要。当你想要对标准进行排序时（例如，某个标准应该在其他任何标准之前执行），`IComparable` 可能会大有用场。`IEnumerable` 可用于在你的标准上实现迭代器模式。这可以给你带来性能优势。你不需要一次性处理所有房屋，而是返回一个迭代器并逐个过滤整个集合。

## 目标 2.4: 复习

1. **正确答案：** C
    - **错误：** 接口不会让你共享任何实现代码，只能共享公共成员的签名。
    - **错误：** 类要求你为每个成员提供实现。它没有给你提供一个仅声明成员签名的选项。
    - **正确：** `abstract` 类允许你共享已实现的方法以及派生类需要实现的方法签名。
    - **错误：** `sealed` 类不能被继承。

2. **正确答案：** B
    - **错误：** `IEnumerable` 应该在类集合的类型上实现，以便它们可以被容易地进行迭代。
    - **正确：** `IComparable` 允许对象之间进行比较。它返回一个整数值，表示相对位置小于 0、等于 0 或大于 0。
    - **错误：** `IDisposable` 应该在访问非托管资源并需要释放它们的类型上实现。
    - **错误：** `IUnknown` 仅用于与 COM 工作。

3. **正确答案：** B, D
    - **错误：** 当你将基类型标记为 `abstract` 时，你无法创建它的实例。你不能在代码中同时将基类型和派生类型作为具体类型。
    - **正确：** 将基类中的方法标记为 `virtual` 允许它被派生类重写。
    - **错误：** `new` 关键字隐藏了基类中的方法。当你想要扩展基类的行为时，不应该使用它。
    - **正确：** `override` 关键字允许你重写基类中标记为 `virtual` 的方法。

## 目标 2.5: 思想实验

1. 虽然接口继承描述的是一种“是一种”（is-a-kind-of）的关系，但你不能说你的类型是“一种 `AuthorizedObject`”。相反，你使用属性来描述另一个类型的某些信息，这就是为什么 C# 包含了元数据。继承不应被用来装饰类型的某些信息。

2. 反射可能是一个非常慢的过程。你可以用表达式树替换反射。当你将数据映射到自定义类型时，可以构建一个表达式树（并缓存它！）。表达式树可以编译为原生代码。

3. 对于生成代码，你可以使用 CodeDOM。由 CodeDOM 创建的 `CompilationUnit` 可以输出为源文件。

## 目标 2.5: 复习

1. **正确答案：** A, D
    - **正确：** 字段是非静态字段。
    - **错误：** `DeclaredOnly` 用于当你不想包含继承的成员时。
    - **错误：** 字段不是静态的；它是一个实例字段。
    - **正确：** 因为字段是私有的，所以需要 `Nonpublic`。

2. **正确答案：** B
    - **错误：** `AttributeTargets.GenericParameter` 可以应用于泛型参数。它不用于方法参数。
    - **正确：** 该属性同时针对 `Methods` 和 `Parameters`。它也可以被多次应用。
    - **错误：** 使用 `AttributeTargets.All` 时，该属性可以应用于所有类型。它也可以被多次应用。
    - **错误：** 因为 `AllowMultiple` 默认为 `false`，此属性不能被多次应用。

3. **正确答案：** C
    - **错误：** `Action` 不返回值。它还接收一个布尔值输入，而不是字符串列表和过滤值。
    - **错误：** 该委托没有用于过滤的值的参数。
    - **正确：** 它接收输入列表和用于过滤的值，并返回过滤后的列表。
    - **错误：** 它只返回字符串列表。它没有用于过滤参数或原始列表的参数。

## 目标 2.6: 思想实验

1. 引用类型位于堆上并由垃圾回收器管理。值类型大多数时候位于栈上，并在当前方法结束时释放。当值类型在栈上时，它占用的内存比在堆上要少。然而，如果一个值类型被封装在引用类型中，它仍然在堆上。将类型更改为 `struct` 并保证你的内存压力会降低。




2. `IDisposable` 为你提供了一种显式释放非托管资源的方法，你无需等待垃圾回收器来释放内存。然而，调用 `Dispose` 是消耗 CPU 时间的。当将任务交给垃圾回收器时，垃圾回收器会决定何时是调用终结器的最佳时间。在显式释放或隐式释放资源之间需要进行某种权衡。

3. 实现 `IDisposable` 的类应该包含一些非托管资源。终结器（Finalizer）对于确保项即使在未调用 `Dispose` 的情况下始终释放非托管资源至关重要。然而，带有终结器的类以以特殊的方式进行线程处理：对象会被添加到终结器队列中，并保留在内存中，直到终结器运行。确保在调用 `Dispose` 时将对象显式地从终结器队列中移除，是十分重要的。

4. 静态字段是一个根引用；垃圾回收器永远不会释放被静态字段引用的对象。在这种情况下，使用一个跟踪哪些对象应该保留在内存中的缓存会更好。一个可以决定对象被访问频率的缓存算法可以确保你的对象一直存在。然而，当内存不足时，缓存可以将某些对象转换为 `WeakReferences` 并确保它们可以被垃圾回收。

## 目标 2.6：回顾

1. **正确答案：** C

    1. **错误：** `RemoveMemoryPressure` 应该在调用 `AddMemoryPressure` 之后才调用，以通知运行时某个托管对象使用了大量的非托管内存。
    2. **错误：** `SuppressFinalize` 应该在对象的 `Dispose` 方法中调用，以通知运行时该对象不再需要进行终结化。
    3. **正确：** `Collect` 将执行垃圾回收，在当时释放尽可能多的内存，这可能是一个非常昂贵的过程。这不会阻止垃圾回收器在你的时间敏感代码期间执行，但它会降低其发生的概率。
    4. **错误：** `WaitForPendingFinalizers` 会挂起当前线程，以便终结器队列上的所有终结器都能运行。这将释放一些内存（针对所有等待终结的对象）。但通常，如果你想确保所有终结器都已运行，会在调用 `Collect` 之后调用这段代码。

2. **正确答案：** D

    1. **错误：** 不会发生内存泄漏，因为类的终结器最终会执行并释放元素。在你的方法中释放对象会导致使用该对象的其他代码抛出 `ObjectDisposedException`。
    2. **错误：** `Close` 方法有时用作次要方法，在内部调用 `Dispose`。它实现在 `File` 等类型上。理由与答案 A 相同。
    3. **错误：** `using` 语句等同于带有 `Dispose` 用的 `try/finally` 语句。然而，你不想释放该项，因为调用代码可能依赖于对象的可用状态。
    4. **正确：** 调用代码知道对象的生命周期应该是什么，并应该决定何时释放对象。

3. **正确答案：** C

    1. **错误：** `WeakReference` 并不等同于高效的缓存策略。将所有项转换为 `WeakReferences` 会增加代码的复杂性（你必须检查内存是否被清除）。它可能会增加你的内存占用，因为 `WeakReference` 本身也会占用内存。
    2. **错误：** 将引用设置为 `null` 会被编译器优化掉。与某些其他语言不同，它不会显式地释放任何内存。
    3. **正确：** 缓存策略是最佳解决方案。你可以根据使用情况、时间戳或其他标准来决定是否要释放内存。
    4. **错误：** 按计划间隔调用 `GC.Collect` 不会提高你的内存效率。只有当对对象没有根引用时，内存才会释放。`GC.Collect` 会阻塞你的执行线程，导致速度变慢，而释放的内存并不比等待常规 `Collect` 发生的多。

## 目标 2.7：思维实验

这并不是一项易事的任务。在现有应用程序中构建全球化支持比从一开始就考虑它需要更多精力。

你必须重点关注的领域是文本显示。特别是由于这是一个时间跟踪应用程序，会有很多日期和时间需要显示。

你必须关注以下几个领域：

* 确保所有字符串比较都使用接收 `StringComparison` 对象的显式重载。
* 在以与文化无关的方式比较字符串时，使用 `StringComparison.Ordinal` 或 `StringComparison.OrdinalIgnoreCase`。
* 在向用户显示文本时，使用 `StringComparison.CurrentCulture`。
* 确保所有持久化的文本都是使用不变文化（invariant culture）进行持久化的。
* 确保你没有使用 `String.Compare` 或 `CompareTo` 进行相等性测试。
* 为显示给用户的自定义类型实现 `IFormattable`，以确保所有的文化设置都得到尊重。
* 向用户显示数字、日期和时间时，使用正确的格式字符串。

## 目标 2.7：回顾

1. **正确答案：** D

    1. **错误：** 仅指定文化将无法给你完整的日期时间。
    2. **错误：** 将“M”作为格式字符串会导致产生“2 avril”而没有年份。
    3. **错误：** 这将提供正确格式的日期，但不是法语文化。
    4. **正确：** 这将提供正确格式的日期。

2. **正确答案：** A

    1. **正确：** `IFormattable` 提供将对象的值格式化为字符串的功能。它也被 `Convert` 类用于相反的操作。
    2. **错误：** `IFormatProvider` 用于获取控制格式的对象，而不是格式本身。
    3. **错误：** `IComparable` 用于排序项。
    4. **错误：** `IConvertible` 定义了将类型转换为等效 CLR 类型的方法。

3. **正确答案：** B

    1. **错误：** `StringReader` 是 `StringBuilder` 类的适配器，以便在需要 `TextReader` 的地方使用。
    2. **正确：** `StringBuilder` 类在更改大量字符串时最高。
    3. **错误：** `StringWriter` 用在需要 `TextWriter` 的地方。它是 `StringBuilder` 的适配器。
    4. **错误：** 普通的 `String` 类是不可变的，因此在更改大量字符串时使用它并不高效。

# 第 3 章 调试应用程序并实现安全

在构建应用程序时，你总是会遇到不可预的问题。也许你看到了错误并开始寻找问题，或者用户在应用程序测试或已上线期间报告了错误。

调试是发现软件错误并消除它们的过程。C# 编译器和 .NET 框架帮助你识别这些 bug，无论是在开发机还是生产环境中。在本章中，你将学习如何使用编译器输出额外信息以帮助你发现 bug。你还将学习在应用程序中实现诊断，以输出关于其健康的关键信息。





在构建真实世界的应用程序时，确保你的应用程序是安全的同样重要。你需要考虑验证应用程序输入，以确保数据是正确的，并避免恶意操作。另一个安全领域与代码本身有关。如果用户可以更改你的程序集（assemblies）并将其部署到生产环境中，他可以在你完全不知情的情况下更改你应用程序的行为。在本章中，你将了解保护自己免受此类攻击的各种选项。

## 本章目标：

* 目标 3.1: 验证应用程序输入
* 目标 3.2: 执行对称和非对称加密
* 目标 3.3: 管理程序集
* 目标 3.4: 调试应用程序
* 目标 3.5: 在应用程序中实现诊断

# 目标 3.1: 验证应用程序输入

如果你的应用程序在完全隔离的状态下运行并且只处理自己的数据，你可以确信你的应用程序是按照预期运行的。

但在现实世界中，你必须处理外部输入。这些输入可能来自另一个系统，但大多数时候来自你的用户。验证应用程序接收的所有输入是一个有时会被忽视的领域，但它至关重要。

本目标涵盖了如何：

* 解释为什么验证应用程序输入很重要。
* 管理数据完整性。
* 使用 `Parse`、`TryParse` 和 `Convert`。
* 使用正则表达式进行输入验证。
* 验证 JSON 和 XML。

## 为什么验证应用程序输入很重要

当你的应用程序处于生产环境中时，它必须处理各种类型的输入。某些输入来自它集成的其他系统，而大多数输入由用户生成。这些用户分为两类：

* `无辜用户`
* `恶意用户`

`无辜用户`是那些尝试使用你的应用程序来完成工作的人。他们在与你的应用程序交互时没有恶意，但他们仍然可能犯错。也许他们忘记输入某些必填数据，或者他们打错了字并插入了无效数据。

`恶意用户`是另一类人。他们积极寻找你应用程序中的漏洞并试图利用它们。也许他们想访问某些特权信息，或者尝试添加或删除信息。这些用户会尝试插入无效数据、反编译你的代码查看其工作原理，或者只是开始寻找你系统中的隐藏区域。

即使你的应用程序集成了其他没有恶意的应用程序，你仍然必须验证你所消耗的数据。也许你已经开发了应用程序、测试了它并确保了一切运行正常，但突然另一个系统升级到了新版本。你预期的字段消失了或移动到了其他地方，并且突然添加了新数据。如果你不保护自己免受此类情况的影响，会导致你的应用程序崩溃或损坏你系统中的数据。

在构建真实世界的应用程序时，你可能会使用诸如 Windows Presentation Foundation (WPF)、ASP.NET 或 Entity Framework 等框架。这些框架内置了验证数据的功能，但确保你了解如何执行自己的验证仍然很重要。

## 管理数据完整性

当无效数据进入你的应用程序时，可能会导致你的应用程序崩溃。也许你期望一个有效的日期，但用户输错了字。当你尝试对该日期执行某些计算时，会抛出异常，你的应用程序就会崩溃。

当然，这对于用户来说是不方便的，绝对是你应该避免的。但崩溃并不是发生的最糟糕情况。如果无效数据没有被识别并保存到了你的数据库中？这会导致数据损坏并危及你数据的完整性。

例如，假设你构建了一个在线购物应用程序。其中一个管理员决定进行一些清理，删除了两个他认为不再使用的用户账户。但他忘记了这些账户拥有购买记录。突然，你的数据处于不一致状态。你的数据库中出现了孤立订单，这些订单无法再关联到特定的用户。

当发生停电或硬件故障时，可能会出现另一种情况。也许你为银行开发了一个应用程序。你收到一条消息，应该从一个账户扣除某些金额并加入另一个账户。在扣除资金后，你的应用程序突然终止，钱突然消失了。

避免这类问题属于`管理数据完整性`的领域。数据完整性有四种：

* `实体完整性`。规定每个实体（数据库中的记录）都应该是唯一标识的。在数据库中，这是通过使用主键（primary key）列实现的。主键唯一标识每行数据。它可以由数据库生成，也可以由你的应用程序生成。
* `域完整性`。指的是实体所包含的数据的有效性。这可能涉及数据类型以及允许的可能值（例如，有效的邮政编码、特定范围内的数字或默认值）。
* `引用完整性`。实体之间的关系，例如订单与客户之间的关系。
* `用户定义完整性`。包括你需要强制的特定业务规则。网店的一项业务规则可能涉及新客户不允许下单超过特定金额的。

大多数这些完整性检查都集成在现代数据库系统中。你可以使用`主键和外键`让数据库对你的数据执行某些检查。主键唯一标识每行数据。定义它们可以确保没有行具有相同的 ID。外键用于指向另一个记录（例如，某个人的经理或订单行的订单）。你可以配置数据库，在不删除订单行的情况下删除订单。

在与数据库交互时，你可能会使用对象关系映射器（ORM），如 Entity Framework，它提供了处理数据库的多种方式。一种方法是在代码中定义对象模型，然后让 Entity Framework 生成一个可以存储该模型的数据库。你可以在类上添加属性（attributes）来指定某些验证规则，或者可以使用特殊的映射语法来配置数据库架构的方式。

### 更多信息：Entity Framework

有关 Entity Framework 以及你使用它的不同方式的更多信息，请参见第 4 章。

例如，在处理网店时，你拥有订单、客户、订单行和产品的类。

你需要实体完整性来确保每个实体都能被唯一标识。你通过为每个实体添加 ID 属性来实现这一点。当你向数据库添加实体时，数据库会帮助你为 ID 生成唯一值。

引用完整性对于维护订单、订单行、客户和产品之间的关系是必要的。外键约束显示了哪些关系是强制的，哪些是可选的。





域完整性也起了作用。你有特定的数据类型，例如用于订单日期和发货日期的 `DateTime`。某些字段是必需的，例如客户名称和想要订购的产品。

用户定义的完整性是另一个问题。Entity Framework 无法自动处理它。你可以在代码中定义这些检查，或者编写由数据库执行的自定义代码。另一种方法是使用 `trigger`（触发器）。触发器是特殊的方法，当数据库中的数据被更新、插入或删除时就会运行。此类操作会触发你的方法的执行。你还可以使用 `stored procedures`（存储过程），它们是存储在数据库中的子程序，可以执行它们来验证日期或控制对数据的访问。

示例 3-1 (#ch03.html_customer_and_address_classes 是描述 `Customer` 和 `Address` 类的代码示例。如你所见，某些属性带有特殊特性的标记。这些特性可以在 `System.ComponentModel.DataAnnotations.dll` 中找到，该文件包含在 Entity Framework 中。可以通过安装 Entity Framework NuGet 包将 Entity Framework 添加到你的应用程序中。

### 更多信息：NuGet

NuGet 是一个免费的开源包管理器。它作为 Visual Studio 扩展安装，可以用来轻松下载软件包并将其添加到你的应用程序中。你可以在 [`nuget.org/`](http://nuget.org/ ) 处找到关于 NuGet 的更多信息。

示例 3-1. `Customer` 和 `Address` 类

```
public class Customer
{
    public int Id { get; set; }

    [Required, MaxLength(20)]
    public string FirstName { get; set; }

    [Required, MaxLength(20)]
    public string LastName { get; set; }

    [Required]
    public Address ShippingAddress { get; set; }

    [Required]
    public Address BillingAddress { get; set; }
}

public class Address
{
    public int Id { get; set; }

    [Required, MaxLength(20)]
    public string AddressLine1 { get; set; }

    [Required, MaxLength(20)]
    public string AddressLine2 { get; set; }

    [Required, MaxLength(20)]
    public string City { get; set; }

    [RegularExpression(@"^[1-9][0-9]{3}\s?[a-zA-Z]{2}$")]
    public string ZipCode { get; set; }
}
```

你可以使用以下预定义的特性：

* `DataTypeAttribute`
* `RangeAttribute`
* `RegularExpressionAttribute`
* `RequiredAttribute`
* `StringLengthAttribute`
* `CustomValidationAttribute`
* `MaxLengthAttribute`
* `MinLengthAttribute`

你可以将这些特性应用于类成员，并且当你将更改保存到数据库中时，验证代码就会运行。

示例 3-2 (#ch03.html_saving_a_new_customer_to_the_database) 显示了使用 Entity Framework 上下将新客户保存到数据库的示例。

示例 3-2. 向数据库中保存新客户

```
public class ShopContext : DbContext
{
    public IDbSet<Customer> Customers { get; set; }

    protected override void OnModelCreating(DbModelBuilder modelBuilder)
    {
        // 确保数据库知道如何处理重复的地址属性
        modelBuilder.Entity<Customer>().HasRequired(bm => bm.BillingAddress)
            .WithMany().WillCascadeOnDelete(false);
    }
}

using (ShopContext ctx = new ShopContext())
{
    Address a = new Address
    {
        AddressLine1 = "Somewhere 1",
        AddressLine2 = "At some floor",
        City = "SomeCity",
        ZipCode = "1111AA"
    };

    Customer c = new Customer()
    {
        FirstName = "John",
        LastName = "Doe",
        BillingAddress = a,
        ShippingAddress = a,
    };

    ctx.Customers.Add(c);
    ctx.SaveChanges();
}
```

如果你忘记设置 `FirstName` 属性，Entity Framework 会抛出以下异常：

```
System.Data.Entity.Validation.DbEntityValidationException : Validation failed for one or
more entities. See 'EntityValidationErrors' property for more details.
```

查看 `EntityValidationErrors` 属性告诉你 `FirstName` 字段是必需的。你可以在 Entity Framework 之外手动运行此验证代码。示例 3-3 (#ch03.html_running_manual_validation) 显示了一个可以对实体运行验证并报告错误的类。

示例 3-3. 手动运行验证

```go
public static class GenericValidator<T>
{
    public static IList<ValidationResult> Validate(T entity)
    {
        var results = new List<ValidationResult>();
        var context = new ValidationContext(entity, null, null);
        Validator.TryValidateObject(entity, context, results);
        return results;
    }
}
```

Entity Framework 还会在数据库中为你的实体创建外键和主键。它们确保你的实体具有相同的 ID。

### 更多信息：Entity Framework

有关 Entity Framework 的更多信息，请参见 [`msdn.microsoft.com/en-us/data/ef`](http://msdn.microsoft.com/en-us/data/ef )。你也可以阅读 *Programming Entity Framework: DbContext*（Julia Lerman 和 Rowan Miller 著）。

管理数据完整性时，另一个重要课题是使用 `transactions`（事务）。事务可以帮助你分组一组操作。如果其中一个失败，所有的都会回滚。通过使用事务，你可以配置哪些更新应该生效。这有助于你维护数据。

### 更多信息：事务

有关事务的更多信息，请参见第 4 章

## 使用 Parse、TryParse 和 Convert

应用程序的大部分输入以简单字符串的形式进入。可能你知道它代表一个数字或有效日期，但你必须进行检查以确保数据有效。

.NET 框架具有一些内置类型可以帮助你将数据从一种类型转换为另一种类型。当你有一个字符串转换为特定类型时，可以使用 `Parse` 方法。例如，如果你知道一个字符串是一个 `Boolean` 值，你可以使用 `bool.Parse` 方法，如示例 3-4 所示。

示例 3-4. 使用 Parse

```go
string value = "true";
bool b = bool.Parse(value);
Console.WriteLine(b); // 显示 True
```

`bool.Parse` 方法使用 `static readonly` 字段 `TrueString` 和 `FalseString` 来判断你的字符串是否为 `true` 或 `false`。如果你的字符串包含无效值，`Parse` 会抛出 `FormatException`。如果你为字符串传递 `null` 值，将得到 `ArgumentNullException`。当你确定解析将会成功时，应该使用 `Parse`。如果抛出异常，这表示应用程序存在真实错误。

`TryParse` 的方式不同。如果你不确定解析是否成功，请使用 `TryParse`。你不希望抛出异常，并且希望优雅地处理无效转换。查看示例 3-5 获取使用 `int.TryParse` 方法的示例，该方法尝试将字符串解析为有效的数字。





```
string value = "1";
int result;
bool success = int.TryParse(value, out result);

if (success)
{ 
    // value is a valid integer, result contains the value
}
else
{ 
    // value is not a valid integer
}
```

如 示例 3-5 所示，`TryParse` 返回一个布尔值，指示该值是否可以被解析。`out` 参数在操作成功时包含结果值。如果解析成功，变量将持有转换后的值；否则，它包含初始值。

当你解析某些用户输入时，可以使用 `TryParse`。如果用户提供了无效数据，你可以显示一条友好的错误信息并让他重试。

当使用 `bool.Parse` 或 `bool.TryParse` 方法时，你没有任何额外的解析选项。在解析数字时，你可以为数字格式和你想使用的特定文化设置提供额外选项。示例 3-6 显示了你如何解析一个包含货币符号和小数点分隔符的字符串。`CultureInfo` 类可以在 `System.Globalization` 命名空间找到。

#### 示例 3-6. 在解析数字时使用配置选项

```
CultureInfo english = new CultureInfo("En");
CultureInfo dutch = new CultureInfo("Nl");

string value = "€19,95";
decimal d = decimal.Parse(value, NumberStyles.Currency, dutch);
Console.WriteLine(d.ToString(english)); // Displays 19.95
```

一个复杂的的话题是解析日期和时间。你可以使用 `DateTime.Parse` 方法来实现，它提供了几个 `overloads`（同名但参数不同的方法）：

*   `Parse(string)` 使用当前线程文化和 `DateTimeStyles.AllowWhiteSpaces`。
*   `Parse(string, IFormatProvider)` 使用指定的文化和 `DateTimeStyles.AllowWhiteSpaces`。
*   `Parse(string, IFormatProvider, DateTimeStyles)`。

在解析 `DateTime` 时，你必须考虑时区差异和文化差异等因素，特别是在开发使用全球化的应用程序时。使用正确的文化设置解析用户输入是非常重要的。

##### 更多信息：解析 Datetime

有关解析日期和时间的更多信息，请参阅 MSDN 文档：`[`msdn.microsoft.com/en-us/library/system.datetime.parse.aspx`](http://msdn.microsoft.com/en-us/library/system.datetime.parse.aspx)`。

.NET Framework 还提供了 `Convert` 类来在基本类型之间转换。支持的基本类型包括 `Boolean, Char, SByte, Byte, Int16, Int32, Int64, UInt16, Uint32, Uint64, Single, Double, Decimal, DateTime,` 和 `String`。`Parse/TryParse` 与 `Convert` 的区别在于 `Convert` 允许 `null` 值。它不会抛出 `ArgumentNullException`；而是返回所提供类型的默认值，如 示例 3-7 所示。

#### 示例 3-7. 使用空值使用 Convert

```
int i = Convert.ToInt32(null);
Console.WriteLine(i); // Displays 0
```

`Convert` 和 `Parse` 方法之间的区别是 `Parse` 仅接受字符串作为输入，而 `Convert` 还可以接受其他基本类型作为输入。示例 3-8 显示了一个将 double 转换为 int 的示例。该 double 值会被四舍五入。

#### 示例 3-8. 使用 Convert 将 double 转换为 int

```
double d = 23.15;
int i = Convert.ToInt32(d);
Console.WriteLine(i); // Displays 23
```

当解析或转换的值对于目标类型来说过大时，此类方法会抛出 `OverflowException`。

### 考试提示

要重要的是，当你解析用户输入时，最佳选择是使用 `TryParse` 方法。为“正常”错误抛出异常并不是最佳实践。当值无法解析时，`TryParse` 仅返回 `false`。

## 使用正则表达式

`regular expression`（正则表达式）是一种用于在字符串中解析和查找匹配的特定模式。正则表达式有时被称为 `regex` 或 `regexp`。

正则表达式是灵活的。例如，正则表达式 `^(\(\d{3}\)|^\d{3}[.-]?)?\d{3}[.-]?\d{4}$` 可以匹配北美电话号码，区号可以带或不带括号，数字之间带或不带连字符或点。

正则表达式有一段编写和使用困难的历史。幸运的是，许多模式已经由别人写好了。像 `[`regexlib.com/`](http://regexlib.com/)` 等网站包含许多你可以使用或根据自己需求调整的示例。正则表达式在以下情况下非常……（注意：提供的文本在此处中断，或需要根据上下文进一步的逻辑）。




虽然正则表达式（regex）看起来比用纯 C# 编写验证代码复杂，但学习它的工作原理绝对是的。正则表达式可以极大地简化你的代码，如果你处于需要验证的情况，它值得你研究一下。

## 验证 JSON 和 XML

在与其他应用程序交换数据时，你经常会接收 `JavaScript Object Notation (JSON)` 或 `Extensible Markup Language (XML)` 数据。JSON 是一种流行的格式，根源于 JavaScript 世界。它是表示某些数据的紧凑方式。XML 有更严格的模式并且被认为更冗长，但无疑有其用处。在使用这些数据之前，确保这些数据是有效的至关重要的。

有效的 JSON 以 `{` 或 `[` 开头并以 `}` 或 `]` 结尾。你可以使用 示例 3-12 中的代码来轻松地判断字符串是否以这些字符开头。

示例 3-12. 检查字符串是否包含可能的 JSON 数据

```csharp
public static bool IsJson(string input)
{
    input = input.Trim();
    return input.StartsWith("{") && input.EndsWith("}")
           || input.StartsWith("[") && input.EndsWith("]");
}
```

当然，仅检查起始和结束字符不足以判断整个对象是否可以解析为 JSON。.NET Framework 提供了 `JavaScriptSerializer`，你可以用它将 JSON 字符串反序列化为对象。你可以在 `System.Web.Extensions` 动态链接库（DLL）中的 `System.Web.Script.Serialization` 命名空间找到 `JavaScriptSerializer`。

示例 3-13 显示了你如何使用 `JavaScriptSerializer`。在这种情况下，你正在将数据反序列化为 `Dictionary<string,object>`。然后你可以遍历字典来查看属性名及其对应的值。

示例 3-13. 使用 `JavaScriptSerializer` 反序列化对象

```csharp
var serializer = new JavaScriptSerializer();
var result = serializer.Deserialize<Dictionary<string, object>>(json);
```

如果你向此函数传递一些无效的 JSON，将抛出一个 `ArgumentException`，其消息以“Invalid object passed in”开头。

一个 XML 文件可以使用 `XML Schema Definition (XSD)` 来描述。该 XSD 可用于验证 XML 文件。

例如，参考 示例 3-14 中描述的 XML 文件。

示例 3-14. 包含人员数据的示例 XML

```xml
<?xml version="1.0" encoding="utf-16" ?>
<Person xmlns:xsi="http://www.w3.org/2001/XMLSchema-           
        instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <FirstName>John</FirstName>
  <LastName>Doe</LastName>
  <Age>42</Age>
</Person>
```

你可以使用 Visual Studio 部分的 `XML Schema Definition Tool (Xsd.exe)` 为此模式创建一个 XSD 文件。该工具可以生成 XML Schema 文件或 C# 类。

接下来的行将为 `person.xml` 文件生成一个 XSD 文件：

```bash
Xsd.exe person.xml
```

该工具会创建一个名为 `person.xsd` 的文件。你可以在 示例 3-15 中查看该 XSD 文件的内容。

示例 3-15. 示例 XSD 文件

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="NewDataSet" xmlns="" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
  xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">
  <xs:element name="Person">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="FirstName" type="xs:string" minOccurs="0" />
        <xs:element name="LastName" type="xs:string" minOccurs="0" />
        <xs:element name="Age" type="xs:string" minOccurs="0" />
      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <xs:element name="NewDataSet" msdata:IsDataSet="true" msdata:UseCurrentLocale="true">
    <xs:complexType>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element ref="Person" />
      </xs:choice>
    </xs:complexType>
  </xs:element>
</xs:schema>
```

默认情况下，文件中的任何项目都不是必须的。然而，它记录了哪些元素是可能的以及文件的结构应该是怎样的。

你现在可以使用此 XSD 文件来验证 XML 文件。示例 3-16 显示了你如何这样做。

```csharp
public void Validate()
{
    string xsdPath = "person.xsd";
    string xmlPath = "person.xml";

    XmlReader reader = XmlReader.Create(xmlPath);
    XmlDocument document = new XmlDocument();
    document.Schemas.Add("", xsdPath);

    ValidationEventHandler eventHandler = new ValidationEventHandler();
    document.Validate("", eventHandler);

    document.Load(reader);
}

public static void ValidationEventHandler(object sender, ValidationEventArgs e)
{
    switch (e.Severity)
    {
        case XmlSeverityType.Error:
            Console.WriteLine("Error: {0}", e.Message);
            break;
        case XmlSeverityType.Warning:
            Console.WriteLine("Warning: {0}", e.Message);
            break;
    }
}
```

如果 XML 文件有误（例如元素不存在），将调用 `ValidationEventHandler`。根据错误的类型，你可以决定采取什么行动。

### 总结

- 验证输入对于保护应用程序非常重要。
- 数据完整性应该由应用程序和数据存储共同维护。
- `Parse`、`TryParse` 和 `Convert` 函数用于类型之间的转换。
- 正则表达式（regex）可匹配输入或替换指定的字符。
- 在接收 JSON 和 XML 文件时，使用内置类型（如 `JavaScriptSerializer` 和 XML Schema）进行验证至关重要。

## 习题回顾

回答以下问题以测试你对本节知识的掌握情况。你可以在章节最后的答案 部分找到这些问题的答案以及选项的解释。

1. 用户需要在文本字段中输入 `DateTime`。你需要在代码中解析该值。你使用哪种方法？
   - `DateTime.Parse`
   - `DateTime.TryParse`
   - `Convert.ToDateTime`
   - `Regex.Match`

2. 你正在开发一个全球化的应用程序。你需要解析用户输入金额的文本字段。你使用哪种方法？
   - `int.TryParse(value, NumberStyles.Currency, UICulture);`
   - `decimal.TryParse(value, NumberStyles.Currency, UICulture);`
   - `decimal.TryParse(value, ServerCulture);`
   - `decimal.TryParse(value)`

3. 你需要验证 XML 文件。你使用什么？
   - `JavaScriptSerializer`
   - `RegEx`
   - `StringBuilder`
   - `XSD`




# 目标 3.2 执行对称加密和非对称加密

安全与密码学彼此紧密相关。构建安全应用程序的某些重要步骤包括用户身份验证、确保你的数据机密性，以及确保没有人能篡改你的数据。 .NET Framework 提供了流行算法的多种实现，你可以使用它们来保护应用程序。

此目标涵盖了如何：

* 使用对称和非对称加密算法。
* 在 .NET Framework 中进行加密工作。
* 使用哈希处理。
* 管理和创建证书。
* 使用来自 `System.Security` 命名空间的代码访问权限。
* 保护字符串数据。

## 使用对称和非对称加密

安全关乎保持秘密。你可以使用复杂的算法对数据进行加密，但如果你无法保持密码和代码的秘密，每个人都能读取你的私有数据。

`Cryptography`（密码学）关于数据的 `encrypting`（加密）和 `decrypting`（解密）。通过加密，你获取一段 `plain text`（人类可读的普通文本），然后对其运行一种 `algorithm`（算法）。生成的数据看起来像是一段随机字节序列，通常称为 `ciphertext`（密文）。解密是相反的过程：字节序列被转换回原始的明文数据。

在密码学中，你可以保持你的算法秘密，也可以使用公开算法并保持你的密钥秘密。

保持算法秘密通常是不现实的，因为每当有人泄露算法时，你就需要切换算法。相反，`key`（密钥）是被保持秘密。算法使用密钥来控制加密过程。加密密钥与普通密码相同：你不应该容易被猜中你选择的密钥。

将算法公开的另一个优势是它经过了广泛的测试。当广泛使用的数据加密标准（DES）算法需要继任者时，美国国家标准与技术研究院（NIST）邀请任何人提交新算法。在提交期结束后，NIST 公开了这些算法的源代码，并邀请所有人破解它们。某些算法在几天内就被破解了，只有极少数进入了决赛。将这些算法公开提高了安全性。

由于算法是公开的，密钥才是应该保持私密的。`symmetric`（对称）和 `asymmetric encryption`（非对称加密）策略的区别在于密钥的使用方式。对称算法使用单一密钥来加密和解密数据。你需要将原始密钥传递给接收者以便以便解密你的数据。这自动导致了安全交换密钥的问题。

这就是非对称算法可以用场的地方。非对称算法使用两个在数学上相关的不同密钥。尽管它们相关，但在已知其中一个密钥的情况下，确定另一个是不行的。一个密钥完全是 `public`（公开的），所有人都可以读取和使用。另一部分是 `private`（私有的），绝不应与他人共享。当你用公钥加密某些内容时，可以使用私钥进行解密，反之亦然。

对称加密与非对称加密的另一个区别在于性能和消息大小。对称加密比非对称加密快，非常适合较大的数据集。非对称加密没有针对长消息加密进行优化，但对于解密一个小密钥可能非常有用。结合这两种技术可以帮助你以加密的方式传输大量数据。

假设 Bob 和 Alice 想要互相发送消息。他们采取了以下步骤：

1. Alice 和 Bob 都生成自己的非对称密钥对。
2. 他们互相发送公钥并保持自己的私钥私密。
3. 他们都生成一个对称密钥，并仅使用对方的公钥对其加密（这样可以使用对方的私钥进行解密）。
4. 他们将各自加密后的对称密钥发送对方，并用自己的私钥解密对方的对称密钥。
5. 为了发送机密消息，他们使用对方的对称密钥并用其加密消息。
6. 接收者使用自己的对称密钥解密消息。

如你所见，非对称加密用于加密对称密钥。在密钥安全传输后……（此处原文在此中断）





`SymmetricAlgorithm` 类同时包含创建加密器（encryptor`）和解密器`decryptor`）的方法。通过使用 `CryptoStream` 类，你可以对字节序列进行加密或解密。

.NET Framework 还支持非对称加密。你可以使用 `RSACryptoServiceProvider` 和 `DSACryptoServiceProvider` 类。在使用非对称加密时，你通常使用来自另一方的公钥。你使用公钥对数据进行加密，这样对方才能使用他们的私钥解密该数据。

示例 3-18 展示了如何创建 `RSACryptoServiceProvider` 的新实例并将公钥导出为 XML 格式。通过向 `ToXmlString` 方法传递 `true`，你还可以导出密钥的私有部分（private part`）。

### 示例 3-18. 导出公钥

```
RSACryptoServiceProvider rsa = new RSACryptoServiceProvider();
string publicKeyXML = rsa.ToXmlString(false);
string privateKeyXML = rsa.ToXmlString(true);

Console.WriteLine(publicKeyXML);
Console.WriteLine(privateKeyXML);
 // Displays:
//<RSAKeyValue>
//  <Modulus>
//    tYo35ywT0Q0KCNhFPu207bS8rrTk91YaxNcD2ElQ1eoWpdYnoCsdj1KaW/
as9zFLYW5slg5Qq8ltdkxZuU//
fh0j2t+7ZFH8RRAD808GkZTrUi1zv3yqMjQDphHOcNfWh+dQrPmp1ShFxEGuA9Y4Ij9RINU5jcfviPa
//    B1ClLXaGbc=
//  </Modulus>
//  <Exponent>AQAB</Exponent>
//</RSAKeyValue>
//<RSAKeyValue>
//  <Modulus>
//    tYo35ywT0Q0KCNhFPu207bS8rrTk91YaxNcD2ElQ1eoWpdYnoCsdj1KaW/as9zFLYW5slg5Qq8ltdkxZuU
//    fh0j2t+7ZFH8RRAD808GkZTrUi1zv3yqMjQDphHOcNfWh+dQrPmp1ShFxEGuA9Y4Ij9RINU5jcfviPa
//    B1ClLXaGbc=
//  </Modulus>
//  <Exponent>AQAB</Exponent>
//  <P>
//    4uhNaN3cPSUzr+KxHmpKyeaD39RT+kWjjDcn/9sTAV/HmDzFzjsiov3KyJ+3XCXucx5TU0lhDOLc/
//    cO+Xrquqw==
//  </P>
//  <Q>
//       zNDVw6oL7YNglrFAeqmgIL3Oj2PkUxrWvoYHCbuFwJKpkWvFBRwZfKXHzzU0zaU5bGdX7M24hW8z5s0
//       eF9CRJQ==
//  </Q>
//  <DP>
//       jkS+/GhWxZPEw5vsF7jnaY3502ZqvPna4HhYwQgX832dRKueDn9vaSidc4sIyWMTDeTOs+LHUfAQRZ/
//       shbKg/w==
//  </DP>
//  <DQ>
//       HV4QWJboUO0Wi2Ts/umViTxOAudq1LOzeOwU1ENsITmmULCoNlxaFzJaHQ7e/GGlgzKqO80fmRph0c
//       U1fGqudQ==
//  </DQ>
//  <InverseQ>
//       BW1VUOgXpkRnn2twvb72uxcbK6+o9ns3xa4Ypm+++7vzlg6t/Iyvk94xNJWjjgR+XsSpN6JEtztWol8
//       bv8HEyA==
//  </InverseQ>
//  <D>
//       IOZUrUNyr+8iA2pWWkowAOhBTZQg7qYfIc8ptjfLO4k544IFGmTVTVZR1vvbcb8vyMk0Vxrf/bLKLcOX
//       zWL2rMeWYGuoTbZEeUbr0SlmesHARL7X/feCm9MIyPjhlhJieRVG3h4f+TyAVo70jmYVcSou+xAaad3
//       7o3Pa8Vny6qIk=
//  </D>
//</RSAKeyValue>
```

公钥是你想要发布的部分，以便其他人可以使用它来加密数据。你可以直接将其发送给某人，或者将其发布在你自己的网站上。示例 3-19 展示了使用公钥和私钥对数据进行加密和解密的示例。

### 示例 3-19. 使用公钥和私钥对数据进行加密解密

```
UnicodeEncoding ByteConverter = new UnicodeEncoding();
byte[] dataToEncrypt = ByteConverter.GetBytes("My Data!");

byte[] encryptedData;
using (RSACryptoServiceProvider RSA = new RSACryptoServiceProvider())
{
    RSA.FromXmlString(publicKeyXML);
    encryptedData = RSA.Encrypt(dataToEncrypt, false);
}

byte[] decryptedData = RSA.Decrypt(encryptedData, false);
string result = ByteConverter.GetString(decryptedData);
Console.WriteLine(result);
```




如果你查看 `Contains` 方法，你会发现它使用了每个项目的 `GetHashCode` 方法。该方法定义在基类 `Object` 上。在每个类型中，你都可以重写此方法并为你的类型提供特定的实现。此方法应该输出一个描述你特定对象的整数代码。作为一条通用指南，哈希值的分布必须尽可能随机。这就是为什么集合（set）的实现使用每个对象的 `GetHashCode` 方法来计算它应该放在哪个桶（bucket）中。

现在，你的项目分布在了一百个桶中，而不是存储在单个桶里。当你检查某个项目是否存在时，你首先计算哈希值，转到对应的桶，然后查找该项目。

这种技术被 .NET Framework 中的 `Hashtable` 和 `Dictionary` 类使用。它们都使用哈希值来存储和访问项目。`Hashtable` 是非泛型集合；`Dictionary` 是泛型集合。

从这里可以推出几个重要的原则。首先，相等的项目应该具有相同的哈希值。这意味着你可以通过检查哈希值来判断两个项目是否相等。这也意味着你对 `GetHashCode` 的实现在任何时候都应该返回相同的值。它不应该依赖于当前日期或时间等变化的值。

### 更多信息：实现 GetHashCode

有关如何正确实现 `GetHashCode` 的更多信息，请参阅 `[`msdn.microsoft.com/en-us/library/system.object.gethashcode(v=vs.110).aspx`](http://msdn.microsoft.com/en-us/library/system.object.gethashcode(v=vs.110).aspx)`。

在安全上下文中查看哈希时，这些属性非常重要。如果你对一段文本进行哈希并仅更改一个字母，哈希值就会改变，因此哈希用于检查消息的完整性。

例如，假设 Alice 和 Bob 想互相发送消息。Alice 创建消息创建哈希，并将哈希值和消息一并发送给 Bob。Bob 对从 Alice 那里收到的消息创建哈希，并将两个哈希值进行比较。如果它们匹配，Bob 就知道他收到了正确的消息。

当然，在没有任何额外加密的情况下，第三方仍然可以通过同时更改消息和哈希值来篡改消息。结合 .NET Framework 提供的加密技术，哈希是验证消息真实性的一种重要技术。

.NET Framework 提供了几个生成哈希值的类。.NET Framework 提供的算法是优化的哈希算法，数据发生微小变化时会输出显著不同的哈希值。

示例 3-23` 展示了使用 `SHA256Managed` 算法为文本计算哈希值的示例。

示例 3-23. 使用 SHA256Managed 计算哈希值

```
UnicodeEncoding byteConverter = new UnicodeEncoding();
SHA256 sha256 = SHA256.Create();

string data = "A paragraph of text";
byte[] hashA = sha256.ComputeHash(byteConverter.GetBytes(data));

data = "A paragraph of changed text";
byte[] hashB = sha256.ComputeHash(byteConverter.GetBytes(data));

data = "A paragraph of text";
byte[] hashC = sha256.ComputeHash(byteConverter.GetBytes(data));

Console.WriteLine(hashA.SequenceEqual(hashB)); // 显示: false
Console.WriteLine(hashA.SequenceEqual(hashC)); // 显示: true
```

如你所见，不同的字符串产生不同的哈希值，而相同的字符串产生完全相同的哈希值。这让你能够通过比较哈希值来查看字符串是否被更改过。

## 管理和创建证书

数字证书是哈希和非对称加密结合的领域。数字证书用于验证由该证书签名的任何对象的身份。它也有助于保护数据的完整性。

如果 Alice 向 Bob 发送消息，她首先对消息进行哈希处理以生成哈希值。然后 Alice 用她的私钥加密哈希值以创建个人签名。Bob 接收到 Alice 的消息和签名。他使用 Alice 的公钥解密签名，现在同时拥有消息和哈希值。然后他可以对消息进行哈希，查看他的哈希值与 Alice 的哈希值是否匹配。

数字证书是 `公钥基础设施`（PKI）的一部分。PKI 是一个由数字证书、证书权威和其他注册机构组成的系统，用于身份和验证每个参与方的有效性。

`证书颁发机构`（CA）是受所有方信任的证书第三方颁发机构。CA 颁发证书（或 `certs`），其中包含公钥、证书颁发给的主体以及 CA 的详细信息。

在你的开发或测试环境进行工作时，你可以使用 `Makecert.exe` 工具创建证书。该工具为了测试目的生成 `X.509 证书`。X.509 证书是定义数字证书的广泛标准。

如果你以管理员身份打开开发命令提示符，可以运行以下命令来生成测试证书：

```
makecert testCert.cer
```

此命令生成一个名为 `testCert.cer` 的文件，你可以将其作为证书使用。你首先需要在你的计算机上安装此证书才能使用它。




数字证书的一个用途是保护网络通信。流行的 HTTPS 通信协议用于保护 Web 服务器与客户端之间的通信。数字证书用于确保客户端连接的是正确的 Web 服务器，而不是冒充者。

## 使用代码访问权限

那种通过使用软盘将程序安装到硬盘来在计算机上获取程序的唯一时代早已一去不复了。今天，你可以从各种来源安装程序，这可能会导致一些安全问题。你的计算机可能正运行着病毒扫描程序，而且你已经养成了在打开附件之前确认邮件发送件者的习惯。

.NET Framework 通过一种名为 `code access security (CAS)`（代码访问安全）的机制帮助你保护计算机免受恶意代码的侵害。它并不是赋予每个应用程序完全信任，而是对它们可以访问的资源类型和可以执行的操作进行限制。

使用 CAS 时，你的代码是不受信任的方。你需要请求权限来执行某些操作或访问受保护的资源。`common language runtime (CLR)` 对托管代码执行安全限制，并确保你的代码具有访问特权资源的正确权限。

安装在你的计算机或本地局域网上的应用程序具有完全信任。它们可以访问资源并执行各种操作。当在 Internet Explorer 或 SQL Server 等沙箱环境中运行时，CAS 会限制应用程序可以执行的操作。

每个代码访问权限代表了以下权利之一：

* 访问受保护资源（例如文件）的权利
* 执行受保护操作（例如访问未托管代码）的权利

此外，你可能正在创建一个插件系统，并希望确保第三方插件不会破坏你的安全。此时，可以使用 CAS 来限制插件被允许执行的事情。

CAS 在 .NET Framework 中执行以下功能：

* 定义访问系统资源的权限。
* 允许代码要求其调用者具有特定的权限。例如，一个暴露创建文件方法的库应该强制要求调用者具有文件输入/输出的权利。
* 允许代码要求其调用者拥有数字签名。通过这种方式，代码可以确保只被来自特定组织或位置的调用者调用。
* 在运行时执行所有这些限制。

CAS 的一个重要概念是当前调用栈上的每一个元素都会被检查。`call stack`（调用栈）是一个数据结构，存储了特定时刻所有活动方法的信息。因此，如果你的应用程序从 `Main` 方法启动，然后调用方法 `A`，方法 `A` 又调用方法 `B`，那么这三个方法都会在调用栈上。当方法 `B` 返回时，只有 `Main` 和 `A` 在调用栈上。

CAS 遍历调用栈并检查栈上的每个元素是否具有所需的权限。通过这种方式，你可以确保一个低信任度的方法无法通过一个高信任的方法调用某些受限代码。

与所有 CAS 相关内容的基类是 `System.Security.CodeAccessPermission`。继承自 `CodeAccessPermission` 的权限如 `FileIOPermission`、`ReflectionPermission` 或 `SecurityPermission`。在应用这些权限中的一种时，你向 CLR 请求执行受保护操作或访问资源的权限。

你可以通过两种方式指定 CAS：`declarative`（声明式）或 `imperative`（命令式）。

声明式意味着你使用属性将安全信息应用到你的代码中。示例 3-25 展示了使用 `FileIOPermissionAttribute` 请求读取所有本地文件权限的示例。

### 示例 3-25. 声明式 CAS

```
[FileIOPermission(SecurityAction.Demand,
    AllLocalFiles = FileIOPermissionAccess.Read)]
public void DeclarativeCAS()
{
    // 方法体
}
```

你也可以以命令式方式这样做，这意味着你在代码中显式地请求权限。示例 3-26 展示了你如何创建一个 `FileIOPermission` 的新实例并请求某些权利。

### 示例 3-26. 命令式 CAS

```
FileIOPermission f = new FileIOPermission(PermissionState.None);
f.AllLocalFiles = FileIOPermissionAccess.Read;
try
{
    f.Demand();
}
catch (SecurityException s)
{
    Console.WriteLine(s.Message);
}
```

### 更多信息：代码访问安全

有关 CAS 的更多信息，请参阅 [`msdn.microsoft.com/en-us/library/c5tk9z76.aspx`](http://msdn.microsoft.com/en-us/library/c5tk9z76.aspx)。

## 保护字符串数据

你应用程序中的大量数据由简单的字符串组成。例如，密码和信用卡号都是字符串。但默认的 `System.String` 实现并没有针对安全进行优化。使用字符串存储敏感数据会有几个问题：

* 字符串值可能会被垃圾回收器在内存中移动，从而留下多个副本。
* 字符串值没有被加密。如果你的内存不足，你的字符串可能会以明文形式写入磁盘上的页文件。当你的应用程序崩溃并生成内存转储时，也可能发生相同的情况。
* `System.String` 是不可变的。每次更改都会创建数据的副本，在内存中留下多个副本。
* 无法强制垃圾回收器移除字符串的所有副本。

.NET Framework 提供了一个特殊类来帮助你减少攻击者的攻击面：`System.Security.SecureString`。

`SecureString` 会加密其值，因此减少了攻击者找到字符串明文的可能性。`SecureString` 还被固定在特定的内存位置。垃圾回收器不会移动字符串，因此避免了存在多个副本的问题。`SecureString` 是可变字符串，可以在需要时变为只读。最后，`SecureString` 实现了 `IDisposable`，以便在你用完它时可以确保将其内容从内存中移除。

### 更多信息：IDisposable 和垃圾收集

有关 `IDisposable` 是以及如何使用的更多信息，请参见第 2 章。第 2 章 还讨论了垃圾回收器的工作原理。

`SecureString` 并不能完全解决所有安全问题。因为它需要在某个时刻进行初始化，初始化 `SecureString` 的数据仍在内存中。为了降低这种风险并强制你考虑这个问题，`SecureString` 只能处理单个字符。无法直接将字符串传递给 `SecureString。示例 3-27 展示了使用 `SecureString` 的示例。应用程序从用户处一次读取一个字符，并将这些字符添加到 `SecureString` 中。

### 示例 3-27. 初始化 *SecureString*

```
using (SecureString ss = new SecureString())
{
    Console.Write("请输入密码: ");
    while (true)
    {
        ConsoleKeyInfo cki = Console.ReadKey(true);
        if (cki.Key == ConsoleKey.Enter) break;

        ss.AppendChar(cki.KeyChar);
        Console.Write("*");
    }
    ss.MakeReadOnly();
}
```

如你所见，`SecureString` 使用 `using` 语句，因此在你用完字符串时会调用 `Dispose` 方法，从而使其不会在内存中停留超过需要的时间。




在某个时刻，你可能想要将 `SecureString` 转换回普通字符串以便使用。.NET Framework 提供了了一些特殊功能来实现此目的。确保普通字符串尽快地从内存中清除是非常重要的。这就是为什么在代码周围有一个 `try`/`finally` 语句的原因。`finally` 语句可以确保即使代码中抛出异常，字符串也会从内存中移除。示例 3-28 展示了如何操作的示例。

示例 3-28. 获取 `SecureString` 的值

```
public static void ConvertToUnsecureString(SecureString securePassword)
{
    IntPtr unmanagedString = IntPtr.Zero;
    try
    {
        unmanagedString = Marshal.SecureStringToGlobalAllocUnicode(securePassword);
        Console.WriteLine(Marshal.PtrToStringUni(unmanagedString));
    }
    finally
    {
        Marshal.ZeroFreeGlobalAllocUnicode(unmanagedString);
    }
}
```

`Marshal` 类位于 `System.Runtime.InteropServices` 命名空间。它提供了在解密 `SecureString` 时可以使用五个方法。这些方法接受一个 `SecureString` 并返回一个 `IntPtr`。每个方法都有一个对应的需要调的方法以清零内部缓冲区。表 3-1 显示了这些方法。

表 3-1. 处理 `SecureString` 的方法

| 解密方法 | 清除内存方法 |
| --- | --- |
| `SecureStringToBSTR` | `ZeroFreeBSTR` |
| `SecureStringToCoTaskMemAnsi` | `ZeroFreeCoTaskMemAnsi` |
| `SecureStringToCoTaskMemUnicode` | `ZeroFreeCoTaskMemUnicode` |
| `SecureStringToGlobalAllocAnsi` | `ZeroFreeGlobalAllocAnsi` |
| `SecureStringToGlobalAllocUnicode` | `ZeroFreeGlobalAllocUnicode` |

必须意识到，`SecureString` 并不是完全安全的。你可以创建一个全速运行的应用程序，该程序能够读取 `SecureString` 内容。然而，它*确实*增加了黑客攻击你应用程序的复杂度。你为了提高应用程序安全而采取的每一个小步骤都会为攻击者带来更大的障碍。

## 思考实验

### 选择你的技术

在这个思考实验中，应用你关于此目标所学到的知识。你可以在本书末尾的答案 部分找到这些问题的答案。

你正在开发一个应用程序，帮助用户跟踪时间并向他们展示何时生产力最高。该应用程序运行在服务器上，网页、桌面和移动端前端均使用 .NET Framework 开发。

你被分配的任务是确定在应用程序中应该使用哪些安全特性。

列出可以用于保护应用程序的可能技术。

## 目标总结

*   对称算法使用相同的密钥来加密和解密数据。
*   非对称算法使用数学上关联的公钥和私钥。
*   哈希是将大量数据转换为较小哈希值的过程。
*   数字证书可验证作者的真实性。
*   CAS 用于限制应用程序可以访问和执行的资源和操作。
*   `System.Security.SecureString` 可用于将敏感字符串数据保留在内存中。

### 目标回顾

回答以下问题以测试你对此目标中信息的掌握情况。你可以在本书末尾的答案 部分找到这些问题的答案，以及每个答案选项为何正确或错误的解释。

1. Bob 和 Alice 正在使用非对称算法交换数据。他们应该向对方发送哪个密钥来实现这一点？
    1. Bob 向 Alice 发送他的私钥，Alice 向 Bob 发送她的公钥。
    2. Bob 向 Alice 发送他的私钥，Alice 向 Bob 发送她的私钥。
    3. Bob 向 Alice 发送他的公钥，Alice 向 Bob 发送她的公钥。
    4. Bob 向 Alice 发送他的公钥，其私钥。

2. 你需要加密大量数据。你使用哪种算法？
    1. SHA256
    2. RSACryptoServiceProvider
    3. MD5CryptoServiceProvider
    4. AesManaged

3. 你需要向另一方发送敏感数据，并确保无人篡改数据。你使用哪种方法？
    1. `X509Certificate2.SignHash`
    2. `RSACryptoServiceProvider.Encrypt`
    3. `UnicodeEncoding.GetBytes`
    4. `Marshal.ZeroFreeBSTR`

## 目标 3.3 管理程序集

在构建应用程序时，你处理的是源代码文件和项目，但并不是你的应用程序部署的方式。C# 编译器获取你的源代码并生成 `assemblies`（程序集）。当你将应用程序部署到生产环境或将其分发给其他方时，管理这些程序集是非常重要的。

此目标涵盖：
*   解释什么是程序集。
*   使用强名称对程序集进行签名。
*   将程序集存入 GAC。
*   对程序集进行版本控制并实现并存托管（side-by-side hosting）。
*   创建一个 WinMD 程序集。

## 什么是程序集？

在微软发布 .NET Framework 之前，`Component Object Model (COM)` 占据主地位，但存在几个问题。

其中一个被称为“DLL 地狱”。微软和其他软件公司分发可供其他应用程序作为构建块使用的 `DLLs`。当一家公司分发新版本的 DLL，但没有针对所有依赖它的应用程序（可能是大量应用程序，导致详尽测试不可能）进行完全测试时，问题就开始出现。更新一个应用程序可能会导致另一个看似无关的应用程序出现问题。

另一个问题与应用程序的安装方式有关。通常，应用程序必须对你系统的多个部分进行更改。当然，会有应用程序目录复制到你的系统中，但还会对注册表进行更改并部署快捷方式。这使得安装过程变得困难，因为卸载应用程序是困难的，有时会留下应用程序的痕迹。

第三个问题是安全问题。由于应用程序在安装期间执行了许多更改，用户很难确定到底安装了什么。可能一个应用程序又安装了其他形成安全风险的组件。

.NET Framework 解决了这些问题，并尝试通过一些激进的变化来解决它们。这些变化中的重要组件之一是 `assembly`（程序集）概念。程序集仍然具有与之前的 Windows 组件相同的 `.dll`（或 `.exe`）扩展名。但在内部，它们完全不同。

程序集是完全独立的；它们不需要向注册或其他位置写入任何信息。程序集包含了运行所需的所有信息。这就是程序集的清单（manifest）。

另一个重要方面是程序集与语言无关的。你可以编写一些 C# 代码，将其编译为程序集，然后从其他 .NET 语言（如 F# 或 Visual Basic）直接使用该程序集。

与旧 DLL 相比，程序集可以进行版本，这允许你在同一系统上拥有特定版本的程序集而不会引起冲突。




另一个重要的变化是程序集的 `deployed`（部署）方式。如果你需要，可以简单地将应用程序复制到新机器来部署它。所有需要的程序集都会本地部署在新的应用程序文件夹中。程序集甚至可以包含资源文件（如图像），这些文件被直接嵌入到程序集中。你还可以选择以共享的方式部署程序集，以便多个应用程序使用。

## 使用强名称对程序集进行签名

`CLR` 支持两种类型的程序集：`strong-named assemblies`（强命名程序集）和 `regular assemblies`（普通程序集）。

普通程序集是 Visual Studio 默认为你生成的。它在结构上与强命名程序集相同。它们都包含元数据、头文件、清单以及程序集中的所有类型。

强命名程序集使用公钥/私钥对进行签名，该密钥对可以唯一标识程序集的发布者及其内容。强名称由程序集的简单文本名称、版本号和文化信息组成。它还包含公钥和数字签名。

对程序集进行强命名有多个优点：

*   **强名称保证了唯一性。** 你的唯一私钥被用于生成程序集的名称。没有其他程序集具有完全相同的强名称。
*   **强名称保护了你的版本谱系。** 因为你控制着私钥，所以你是唯一可以向程序集发布更新的人。用户可以确定新版本源自同一个发布者。
*   **强名称提供了强力的完整性检查。** `.NET Framework` 会检查强命名程序集自签名那一刻起是否发生了变化。

总而言之，你可以看到强命名程序集确保了用户可以信任程序集的来源和内容。

你通过使用自己的私钥对程序集进行签名来生成强命名程序集。其他用户可以使用随程序集分发的公钥来验证该程序集。

### 更多信息：公钥和私钥的使用

有关使用私钥和公钥生成数字签名的更多信息，请参阅本章节前面的“目标 3.2：执行对称和非对称加密”部分。

对程序集进行签名可以在命令行完成，也可以通过使用 Visual Studio 完成。你需要采取的第一步是生成一个 `key pair`（密钥对）。密钥对通常是一个扩展名为 `.snk` 的文件，包含你的公/私钥信息。

使用开发者命令提示符时，你可以运行以下命令来生成新的密钥对文件：

```
sn -k myKey.snk
```

更简单的方法是使用 Visual Studio 为你生成密钥对文件。你可以打开想要签名的项目属性页，然后转到到 `Signing`（签名）选项卡，如图 3-1 所示。

![Visual Studio 中的签名页](img/httpatomoreillycomsourcemspimages1722810.png.jpg)

图 3-1. Visual Studio 中的签名页

通过启用程序集签名，你可以让 Visual Studio 生成一个新的密钥文件，该文件随后被添加到你的项目中，并在编译步骤中用于强签名你的程序集。

强命名程序集只能引用其他也是强命名的程序集。这样做是为了避免安全漏洞，防止依赖的程序集被更改以影响强命名程序集的行为。当你添加普通程序集的引用并尝试调用该程序集中的代码时，编译器会发出错误：

```
Assembly generation failed -- Referenced assembly 'MyLib' does not have a strong name
```

对程序集进行签名后，你可以使用随 Visual Studio 安装的 `Strong Name tool (Sn.exe)` 查看公钥。随 `.NET Framework` 安装的强命名程序集之一是 `System.Data`。示例 3-29 显示了如何获取此程序集的公钥。

示例 3-29. 检查已签名程序集的公钥

```
C:\>sn -Tp C:\Windows\Microsoft.NET\Framework\v4.0.30319\System.Data.dll

Microsoft (R) .NET Framework Strong Name Utility  Version 4.0.30319.17929
Copyright (c) Microsoft Corporation.  All rights reserved.

Identity public key (hash algorithm: Unknown):
00000000000000000400000000000000

Signature public key (hash algorithm: sha256):
002400000c800000140100000602000000240000525341310008000001000100613399aff18ef1
a2c2514a273a42d9042b72321f1757102df9ebada69923e2738406c21e5b801552ab8d200a65a2
35e001ac9adc25f2d811eb0
```




在 GAC（全局程序集缓存）中部署程序集可以通过两种方式实现：

- 对于生产场景，使用具有 GAC 权限的特定安装程序，例如 `Windows Installer 2.0`。
- 对于开发场景，使用一个名为 `Global Assembly Cache tool (Gacutil.exe)` 的工具。

你可以通过在开发命令提示符中运行以下命令来查看 GAC 的内容：

```
gacutil -l
```

这将返回已在 GAC 中安装的所有程序集的列表。

可以使用以下命令在 GAC 中安装程序集：

```
gacutil –i [assembly name]
```

你还可以从 GAC 中删除程序集：

```
gacutil –u [assembly name]
```

当从你的项目引用共享程序集时，你可以对位于 GAC 中的文件添加引用，或者对该句的本地副本添加引用。当 Visual Studio 检测到你正在引用的 `DLL` 存在 GAC 版本时，它将添加指向 GAC 的引用，而不是指向本地版本。

## 程序集版本控制

与 .NET Framework 之前的 `DLLs` 工作方式截然不同，程序集具有`版本号`。在程序集清单文件中，程序集记录了它自己的版本号以及它引用的所有程序集的版本号。

每个程序集都有一个遵循以下格式的版本号：

`*{Major Version}.{Minor Version}.{Build Number}.{Revision}`

- `Major Version`（主版本）在每次重大发布时手动增加。一个重大发布应该包含许多新功能或破坏性更改。
- `Minor Version`（次要版本）在仅对现有功能引入细微更改的次要发布时增加。
- `Build Number`（生成号）由生成服务器每次生成时自动增加。这样，每个生成版本都有一个唯一的标识号，可以用于跟踪。
- `Revision`（修订号）用于对生产环境进行补丁。

在生成程序集时，你需要考虑两个版本号：文件版本号和 .NET 程序集版本号。

如果你在 Visual Studio 中创建一个新项目，它会自动向你的项目属性添加一个 `AssemblyInfo.cs` 文件。

该文件包含以下两行：

```
[assembly: AssemblyVersion("1.0.0.0")]
[assembly: AssemblyFileVersion("1.0.0.0")]
```

`AssemblyFileVersionAttribute` 是在每次生成时应该增加的那个。这并不是你希望在客户端执行的操作，因为在那里它会随着开发者的每次生成而增加。相反，你应该将其集成到你生成服务器上的生成处理过程中。

`AssemblyVersionAttribute` 应该手动增加。这应该在你计划将特定版本部署到生产环境时完成。

由于当运行时尝试定位程序集时程序集的版本非常重要，你可以将同一程序集的多个版本部署到 GAC，并避免普通 DLL 文件中发生的 DLL 问题。这被称为 `side-by-side hosting`（并存托管），即多个版本的程序集共同托管在同一台计算机上。

寻找正确程序集的过程从原始程序集清单文件中提到的版本号开始，以确定加载哪个程序集。然而，这些绑定可以受到特定配置文件的影响。

使用了三种配置文件：

- 应用程序配置文件
- 发布者策略文件
- 机器配置文件

这些配置文件可以用来影响被引用程序集的绑定。例如，你已经将一个程序集部署到 GAC，并且有两个应用程序依赖于它。突然发现了一个错误，你为它创建了修复。新程序集有一个新的版本号，你想确保所有应用程序都使用新程序集。

你可以通过使用 `publisher policy file`（发布者策略文件）来实现。在此类配置文件，指定如果 `CLR` 查找特定的程序集，它应该绑定到新版本。示例 3-30 显示了此类文件的示例。

示例 3-30. 重定向程序集绑定到较新版本

```
<configuration>
   <runtime>
      <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
       <dependentAssembly>
         <assemblyIdentity name="myAssembly"
                           publicKeyToken="32ab4ba45e0a69a1"
                           culture="en-us" />
         <!-- 重定向到程序集的 2.0.0.0 版本。 -->
         <bindingRedirect oldVersion="1.0.0.0"
                          newVersion="2.0.0.0"/>
       </dependentAssembly>
      </assemblyBinding>
   </runtime>
</configuration>
```

此文件指示 `CLR` 绑定到程序集的版本 2 而不是版本 1。你需要将此类发布者策略部署到 GAC，以便 `CLR` 在绑定程序集时可以使用它。

### 更多信息：发布者策略文件

有关如何创建和部署发布者配置文件的更多信息，请参阅 `[`msdn.microsoft.com/en-us/library/8f6988ab.aspx`](http://msdn.microsoft.com/en-us/library/8f6988ab.aspx)`。

如果你将程序集与应用程序私有部署，`CLR` 开始在当前应用程序目录中查找它。如果找不到程序集，它将抛出 `FileNotFoundException`。

你可以在应用程序的配置文件中指定 `CLR` 应该查找的额外位置。示例 3-31 所示。

示例 3-31. 为程序集提供额外的位置

```
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <runtime>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <probing privatePath="MyLibraries"/>
    </assemblyBinding>
  </runtime>
</configuration>
```

另一个选项是使用 `codebase` 元素。`codebase` 元素可以指定应用程序之外的位置。通过这种方式，你可以定位位于网络上另一台计算机或互联网上的程序集。如果程序集不在当前应用程序文件夹中，它们必须经过强命名。当程序集位于另一台计算机时，会被下载到 GAC 中的特殊文件夹。示例 3-32 显示了使用 `codebase` 元素指定网络上程序集位置的示例。

示例 3-32. 为程序集提供额外的位置

```
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <runtime>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <dependentAssembly>
        <codeBase version="1.0.0.0"
          href= "http://www.mydomain.com/ReferencedAssembly.dll"/>
      </dependentAssembly>
    </assemblyBinding>
  </runtime>
</configuration>
```

### 考试提示

`probing` 选项只能用于指向相对于应用程序路径的位置。如果你想在其他地方定位程序集，则必须使用 `codebase` 元素。

## 创建 WinMD 程序集

随着 Windows 8 的推出，微软引入了新的 `WinRT 运行时`。WinRT 完全由原生 C++ 编写。没有托管环境，没有 `CLR`，也没有即时编译 (`JIT`) 编译器。

### 注意：Winrt 与 Windows RT

尽管 WinRT 和 Windows RT 看起来相似，但它们是两个完全不同的东西。WinRT 是 Windows Runtime。Windows RT 是适用于 ARM 处理器的 Windows 8 特版本。该 Windows 版本部署在如 Microsoft Surface 等平板设备上。它只能运行 Windows Store 应用程序。




然而，为 Windows 8 开发应用程序可以使用 JavaScript 和 C# 等语言。普通的 C++ `native component` 不包含元数据。但是，为了在原生组件与其他语言之间创建正确的映射，元数据是必须的。为了实现这一点，微软创建了一种名为 `Windows Metadata (WinMD) files` 的新文件类型。

如果你正在运行 Windows 8，你可以在 `C:\Windows\System32\WinMetadata` 找到这些文件。这些文件的格式与 .NET Framework 用于 `Common Language Infrastructure (CLI)` 的格式是完全的。

WinMD 文件可以同时包含代码和元数据。然而，你在 `System32` 目录中找到的文件仅包含元数据。这些元数据供 Visual Studio 用于提供 IntelliSense。在运行时，元数据会告诉 `CLI`，其中找到的所有方法的实现都由运行时提供。这就是为什么这些文件不需要包含实际代码；它们确保方法被映射到 WinRT 中正确的方法。

需要注意的一点是，WinRT 并没有提供对 .NET Framework 4.5 所有功能的访问。相反，它移除了许多重复、遗留或设计不当的应用程序接口 (APIs)。这有助于确保 WinRT 应用可以移植到其他平台，并仅使用提供的最佳 API。

如果你想创建自己的 WinMD 程序集，可以通过在 Visual Studio 中创建一个 `Windows Runtime component` 来实现。只有当你创建一个应该被 JavaScript 和 C# 等不同编程语言使用的组件时，才应该这样做。如果你只使用 C# 工作，则应该创建一个新的 `“Class Library (Windows Store apps)” project`。

Windows Runtime component 会编译成一个你可以使用的 `.winmd file`。

关于你的 Windows Runtime component，有几点限制是你需要注意的：

*   你的组件中所有公开类型和成员的字段、参数和返回值必须是 Windows Runtime 类型。
*   公开类和接口可以包含方法、属性和事件。然而，公开类或接口不能执行以下操作：
    *   定义为泛型
    *   实现不是 Windows Runtime 接口的接口
    *   继承自不在 Windows Runtime 内部的类型
*   公开类必须是密封的 (sealed)。
*   公开结构体（structures）只能有公开字段作为成员，这些字段必须是值类型或字符串。
*   所有公开类型必须有一个与程序集名称匹配的根命名空间，且不以 `Windows` 开头。

如果你创建了一个有效的 Windows Runtime Component，你就可以在构建 Windows 8 应用时使用此库。通过这种方式，例如你可以用 C# 构建一些复杂代码，然后从你的 JavaScript Windows Store 应用中调用它。

## 思考实验

### 选择你的技术

在这个思考实验中，请应用你关于本目标中学到的知识。你可以在章节末尾的 Answers 章节找到这些问题的答案。

你正在讨论为什么想要对你构建的程序集签名。该程序集将与你正在构建的桌面应用程序一起发布。该程序集不会被其他应用程序共享。

1. 你应该对程序集签名吗？
2. 签名的优缺点是什么？

## 目标总结

*   程序集是一个包含元数据的编译后的代码单元。
*   程序集可以进行强签名，以确保没有人可以篡改内容。
*   已签名的程序集可以放在全局程序缓存 (GAC) 中。
*   程序集可以版本化，应用程序将使用它们开发时使用的程序集版本。可以使用配置文件来更改这些绑定。
*   WinMD 程序集是一种特殊的程序集类型，用于 WinRT 用于将非原生语言映射到原生 WinRT 组件。

### 目标回顾

回答以下问题以测试你对本目标信息的掌握情况。你可以在章节末尾的 Answers 章节找到这些问题的答案以及每个选项正确或错误的解释。

1. 你正在构建一个强名称程序集，并想要引用一个普通程序集来重用你构建的一些代码。你需要做什么？
    1. 你首先需要将程序集放入 GAC。
    2. 不需要。引用另一个程序集来使用某些代码总是可能的。
    3. 你需要在使用另一个程序集之前对其进行签名。
    4. 你需要使用另一个程序集的公钥令牌来引用它。
2. 你正在构建一个将被几个服务器应用程序使用的程序集。你希望此程序集的更新过程尽可能顺利。你应该采取哪些步骤？（多选）
    1. 创建一个 WinMD 元数据文件。
    2. 将程序集部署到 GAC。
    3. 在每个客户端应用程序中添加 `assemblyBinding` 部分，指向程序集的位置。
    4. 为程序集进行强命名。
3. 你想将程序集部署到内网上的共享位置。你应该采取哪些步骤？（多选）
    1. 为程序集进行强命名。
    2. 在使用程序集的应用程序中使用 codebase 配置元素。
    3. 将程序集部署到 GAC。
    4. 使用带有探测 (probing) 选项的 `assemblyBinding` 配置元素。# 目标 3.4 调试应用程序

无论你的开发流程有多完美，你的应用程序中不时会出现 `bug`。`Debugging` 是从应用程序中移除这些错误的过程。C# 编译器和 Visual Studio 在查找和修复 方面非常有帮助。

本目标涵盖了如何：

*   选择合适的生成类型。
*   创建并管理编译指令。
*   管理程序数据库文件。

## 生成配置

如果你在 Visual Studio 中创建一个新项目，它会为你创建两个默认配置：

*   Release 模式
*   Debug 模式

如果你编译项目，这些配置中的设置将用于配置编译器的行为。在 `release mode` 中，编译后的代码经过了完全优化，并且不会创建用于调试目的的额外信息。

在 `debug mode` 中，没有应用优化，并且会输出额外信息。当在 Example 3-33 中执行程序时，这些配置之间的区别显而易见的。

示例 3-33. 一个简单的控制台应用程序

```
using System;
using System.Threading;

public static class Program
{
    public static void Main()
    {
        Timer t = new Timer(TimerCallback, null, 0, 2000);
        Console.ReadLine();
    }

    private static void TimerCallback(Object o)
    {
        Console.WriteLine("In TimerCallback: " + DateTime.Now);
        GC.Collect();
    }
}
```

此控制台应用程序创建了一个 `Timer` 对象的实例，并设置每 2 秒触发一次。当触发时，它输出当前日期和时间。它还调用了 `GC.Collect()` 来强制运行垃圾回收。通常你永远不会这样做，但在示例中它显示了一些有趣的行为。

当你在 debug 模式下运行此应用程序时，它很好地每 2 秒输出一次时间，并一直持续直到你终止应用程序。

当你在 release 模式下执行此应用程序时，它只输出一次日期和时间。这演示了 debug 和 release 构建之间的区别。在执行 release 构建时，编译器会优化代码。在这种场景下，它看到 `Timer` 对象不再被使用，因此它不再被视为根对象，垃圾回收器将其从内存中移除。

### 更多信息：垃圾回收器





有关垃圾收集器的更多信息，请参见第 2 章。

在调试配置中，编译器会插入额外的`no-operation (NOP)` 指令和`branch instructions`。`NOP` 指令是实际上不执行任何操作的指令（例如，对一个从未使用的变量进行赋值）。`branch instruction` 是条件执行的代码段（例如，当某个变量为 `true` 或 `false` 时）。当编译器发现某个分支从未被执行时，它可以将其从编译后的输出中移除。在优化代码时，编译器还可以选择内联短方法，从而有效地从输出中移除该方法。

在现实世界中，你不需要突然担心你的对象被垃圾回收以及代码在发布模式下出错。`Timer` 对象是一个特殊情况，通常你不会遇到这个问题。但它确实说明了发布（release）构建和调试（debug）构建之间的区别。编译器在调试构建中输出的额外信息可以在 Visual Studio 中用于调试你的应用程序。

你可以做的一件事是设置断点。图 3-2 显示了在示例 3-31 所示应用程序中设置断点的示例。

![在 Visual Studio 中设置断点](img/httpatomoreillycomsourcemspimages1722812.png.jpg)

图 3-2. 在 Visual Studio 中设置断点

如你所见，第 14 行的断点目前处于激活状态。这意味着调试器已暂停了应用程序，你现在可以使用 Visual Studio 检查并编辑值，并影响程序的流。

### 更多信息：使用 Visual Studio 进行调试

有关如何在 Visual Studio 中使用调试器的更多信息，请参阅 [[`msdn.microsoft.com/en-us/library/k0k771bt.aspx`](http://msdn.microsoft.com/en-us/library/k0k771bt.aspx)]。

当你正在开发应用程序时，调试配置是最实用的。但当你准备好将应用程序部署到生产环境时，确保你使用发布配置以获得最佳性能就非常重要。

## 创建和管理编译器指令

某些编程语言具有`preprocessor`（预处理器）的概念，它是一个在将代码交给编译器之前处理你的代码并对其应用某些更改的程序。

C# 并没有专门的预处理器，但它确实支持`preprocessor compiler directives`（预处理器编译器指令），这些是发送给编译器的特殊指令，用于帮助编译过程。

预处理器指令的一个示例是 `#if`。示例 3-34 显示了一个示例。

示例 3-34. 检查调试符号

```csharp
public void DebugDirective()
{
    #if DEBUG
        Console.WriteLine("Debug mode");
    #else
        Console.WriteLine("Not debug");
    #endif
}
```

该方法的输出取决于你所使用的构建配置。如果你将构建配置设置为 `Debug`，它将输出“Debug mode”；否则，它将显示“Not debug”。

在使用在使用 `#if` 指令时，你可以使用你在 C# 中熟悉的运算符：`==`（相等）、`!=`（不相等）、`&&`（和）、`||`（或）和 `!`（非）来测试 `true` 或 `false`。

`debug symbol`（调试符号）是在使用默认配置进行调试时由 Visual Studio 定义的。它通过向编译器传递 `debug` 命令来实现。你可以使用 `#define` 指令定义你自己的符号。示例 3-35 显示了如何定义你自己的符号并在以后使用它来检查其是否存在。定义必须出现在文件中任何其他代码之前，这是非常重要的。

示例 3-35. 定义自定义符号

```csharp
#define MySymbol

// ...

public void UseCustomSymbol()
{
    #if MySymbol
        Console.WriteLine("Custom symbol is defined");
    #endif
}
```

像这样使用指令可能会让你的代码更难理解，你应该尽量避免使用它们。使用预处理器指令可能是必要的场景是当你正在构建一个针对多个平台的库时。在构建针对 Silverlight、WinRT 和不同版本的 .NET Framework 等平台的 .NET 库时，你可以使用预处理器指令来平滑平台之间的差异。

示例 3-36 显示了 WinRT 和 .NET 4.5 差异的示例。在 .NET 4.5 中，你可以直接从 `Assembly` 属性获取类型的程序集。但在 WinRT 中，此 API 已经发生了变化，你需要调用 `GetTypeInfo`。通过使用预处理器指令，你可以重用大量的代码并调整你的代码。

示例 3-36. 使用预处理器指令针对多个平台

```csharp
public Assembly LoadAssembly<T>()
{ 
    #if !WINRT
        Assembly assembly = typeof(T).Assembly;
    #else
        Assembly assembly = typeof(T).GetTypeInfo();
    #endif

    return assembly;
}
```

另一个预处理器指令是 `#undef`，用于移除符号。两个指令是 `#warning` 和 `#error`。你可以将它们包含在代码中以报告错误或警告。示例 3-37 显示了一个示例。

示例 3-37. 警告和错误

```csharp
#warning This code is obsolete

#if DEBUG
#error Debug build is not allowed
#endif
```

如果你将此代码粘贴到 Visual Studio 项目并构建，你会看到一个警告和一个错误（参见图 3-3）。

![警告和错误](img/httpatomoreillycomsourcemspimages1722814.png.jpg)

图 3-3. 警告和错误

在使用代码生成功能时，我们有时会在编译之前源文件中删除或添加行。如果代码发生错误，编译器报告的行号与你看到的代码不同。`#line` 指令用于修改行号甚至文件名。你还可以从调试器中隐藏代码。如果你使用 `#line hide` 指令进行调试，调试器将跳过隐藏部分。示例 3-38 显示了使用 `#line` 指令的示例。

示例 3-38. 行指令

```csharp
#line 200 "OtherFileName"
    int a;    // 行 200
#line default
    int b;   // 行 4
#line hidden 
    int c; // 隐藏
    int d; // 行 7
```

在构建应用程序时，你有时会故意编写一些触发警告的代码。你不想更改代码，但你想隐藏该警告。你可以通过 `#pragma` 警告指令来实现这一点。示例 3-39 显示了禁用和启用所有警告的示例。

示例 3-39. pragma 警告指令

```csharp
#pragma warning disable 
 while (false)
{
    Console.WriteLine("Unreachable code");
}
#pragma warning restore
```




你也可以选择禁用或恢复特定的警告，如示例 3-40 所示。编译器不会对 `int i` 语句报告警告，但它会为不可达的代码报告警告。你可以在 Visual Studio 的“输出”窗口中找到特定的错误代码。

### 示例 3-40. 禁用和启用特定警告

```cpp
#pragma warning disable 0162, 0168
int i;
#pragma warning restore 0162
while (false)
{
    Console.WriteLine("Unreachable code");
}
#pragma warning restore 
```

通常，预处理器指令被用于根据构建配置包含或排除某些代码。.NET Framework 具有 `ConditionalAttribute` 特性，你可以将其作为替代方案。也许你希望只在构建调试配置时才调用某个函数。示例 3-41 显示了如何使用预处理器指令实现此功能。

### 示例 3-41. 仅在调试构建中调用方法

```csharp
public void SomeMethod()
{ 
    #if DEBUG
    Log("Step1");
    #endif
}
private static void Log(string message)
{
    Console.WriteLine("message");
}
```

每个每个方法的调用都封装在预处理器指令中是不方便的。相反，你可以使用 `ConditionalAttribute`，它告诉编译器只有当条件为 `true` 时，对方法的调用才会被包含在编译后的程序中。示例 3-42 显示了一个示例。

### 示例 3-42. 应用 ConditionalAttribute

```csharp
[Conditional("DEBUG")]
private static void Log(string message)
{
    Console.WriteLine("message");
}
```

另一个在调试时很有用的特性是 `DebuggerDisplayAttribute`。默认情况下，Visual Studio 调试器会对你想要检查其值的每个对象调用 `ToString`。对于简单对象（如 `ints` 或 `strings`），这没有问题，因为它们有一个显示其值的 `ToString` 重载方法。但对于没有重写 `ToString` 的类型，默认实现会显示类型的名称，这在调试时是没有用的。当然，你可以开始重写所有的 `ToString` 方法并为它们提供适用于调试目的的实现，但该实现也会出现在你的发布版本构建中。

作为替代方案，你可以使用 `System.Diagnostics` 命名空间下的 `DebuggerDisplayAttribute`。该特性被 Visual Studio 调试器用于显示对象。示例 3-43 显示了一个示例。

### 示例 3-43. 应用 DebuggerDisplayAttribute

```csharp
[DebuggerDisplay("Name = {FirstName} {LastName}")]
public class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
}
```

## 管理程序数据库文件和符号

在编译程序时，你可以选择创建一个扩展名为 `*.pdb` 的额外文件。该文件被称为`程序数据库 (PDB) 文件`，这是一个额外的数据源，用于为你的应用程序代码附加信息，这些信息在调试期间非常有用。

你可以通过指定 `/debug:full` 或 `/debug:pdbonly` 选项来构造编译器创建 PDB 文件。当你指定全量标志时，会创建一个 PDB 文件，并且特定的程序集包含调试信息。使用 `pdbonly` 标志时，生成的程序集不会被修改，只生成 PDB 文件。在进行发布构建时，建议使用后者选项。

.NET PDB 文件包含两部分信息：

*   源文件名及其行号
*   局部变量名

这些数据没有包含在 .NET 程序集中，但你可以想象一下它们对调试有多大的帮助。

当你加载一个模块时，调试器开始寻找对应的 PDB 文件。它通过查找与应用程序或库位于相同目录下的同名 PDB 文件来实现这一点。因此，当你有一个 `MyApp.dll` 时，调试器会寻找 `MyApp.pdb`。当它找到名称匹配的文件时，会比较由编译器创建的内部 ID。该 ID 是一个`全局唯一标识符 (GUID)`，它应该完全匹配。这样，调试器就知道你正在使用正确的 PDB 文件，并且在调试期间可以为你的应用程序显示正确的源代码。

重要的一点是此 GUID 是在编译时创建的，所以如果你重新编译应用程序，你将获得一个与重新编译构建完全匹配的新 PDB 文件。因此，你不能使用今天创建的 PDB 文件来调试昨天的构建；GUID 将不会匹配，调试器也不会接受该 PDB 文件。

在 Visual Studio 中执行调试会话时，大多数情况下没有问题。你的代码和运行的应用程序完全匹配，Visual Studio 允许你调试应用程序。但当你想要调试当前正在生产环境中的应用程序时，你需要 PDB 文件。

当你运行控制台应用程序示例 3-44 时，你可以看到缺少 PDB 文件的影响。

### 示例 3-44. 检查 PDB 文件

```csharp
using System;

namespace PdbFiles
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World");
            Console.ReadKey();
        }
    }
}
```





当你现在开始调试时，调试器将从微软符号服务器（Microsoft Symbol Server）下载 `PDB` 文件。如果你查看 `Modules` 窗口，你会看到所有模块都加载了符号。你还会发现 `Call Stack` 窗口显示的信息比以前多得多（参见 图 3-6）。

![加载了所有模块的调用栈窗口](img/httpatomoreillycomsourcemspimages1722820.png.jpg)

图 3-6.加载了所有模块的调用栈窗口

在构建自己的项目时，为内部使用设置符号服务器是非常重要的。最简单的方法是使用 `Team Foundation Server (TFS)` 来管理你的源代码和构建。`TFS` 有一个选项，可以将构建中生成的所有 `PDB` 文件发布到共享位置，该位置可以作为 Visual Studio 的符号服务器，允许你在没有源代码的情况下调试应用程序的所有以前版本。

### 更多信息：符号服务器

有关如何设置自己的符号服务器的更多信息，请参阅 `[`msdn.microsoft.com/en-us/library/ms680693(VS.85).aspx`](http://msdn.microsoft.com/en-us/library/ms680693(VS.85).aspx)`。

### 考试贴士

记住保存你的 `PDB` 文件有多重要。如果你丢弃了它们，将立即失去调试该应用程序特定构建版本的机会。

当编译器构建全尺寸的 `PDB` 文件时，它包含了两个不同的信息集合：私有符号数据和公共符号数据。公共符号文件包含的数据较少。它只暴露从一个源文件到另一个文件可以访问的项目。仅在一个对象文件中可见的项目（例如局部变量）不在公共符号部分。

在向外部发布符号文件时（如微软所的那样），你可以选择移除私有信息。当你处理不希望暴露的知识产权时，这是一个重要的步骤。

你可以通过使用 `PDBCopy` 工具来实现。`PDBCopy` 是 Windows 调试工具（Debugging Tools for Windows）的一部分，作为 Windows 软件开发工具包 (SDK) 的一部分安装。以下行显示了从 `PDB` 文件中剥离私有数据的示例：

```
pdbcopy mysymbols.pdb publicsymbols.pdb –p
```

此代码获取 `mysymbols.pdb` 文件并创建一个不包含私有符号数据的 `publicsymbols.pdb` 文件。

### 更多信息：PDBCopy

有关如何使用 `PDBCopy` 的更多信息，请参阅 `[`msdn.microsoft.com/en-us/library/windows/hardware/ff560131(v=vs.85).aspx`](http://msdn.microsoft.com/en-us/library/windows/hardware/ff560131(v=vs.85).aspx)`。

## 思考实验

### 调试应用程序

在这个思考实验中，应用你对本目标中学到的知识。你可以在章节末尾的答案](#ch03.html_answers-id00084 "Answers") 部分找到这些问题的答案。

你在组织的支持部门工作。一个客户给你打电话，报告你托管在自己服务器上的一个 Web 应用程序出现错误。

1. 你想远程调试此应用程序。
2. 你是否需要向服务器部署调试版本？
3. 你需要什么才能实现这一点？
4. 符号服务器如何帮助你？

## 目标总结

* Visual Studio 构建配置可用于配置编译器。
* 调试构建（debug build）输出未优化的代码版本，其中包含有助于调试的额外指令。
* 发布构建（release build）输出优化后的代码，可以部署到生产环境。
* 编译器指令可用于向编译器提供额外指令。例如，你可以使用它们在某些构建配置中包含代码或抑制某些警告。
* 程序数据库 (`PDB`) 文件包含调试应用程序所需的额外信息。

### 目标回顾

回答以下问题以测试你对本目标信息的掌握情况。你可以在章节末尾的答案](#ch03.html_answers-id00084 "Answers") 部分找到这些问题的答案，以及对每个选项正确或错误的解释。

1. 你准备好将代码部署到生产服务器了。你部署了哪种配置？
   1. 调试配置 (Debug configuration)
   2. 发布配置 (Release configuration)
   3. 带有 `PDB` 文件的自定义配置
   4. 使用 `/debug:full` 编译器标志构建的发布配置

2. 你正在调试一个网商店的应用程序，并检查许多 `Order` 类。你可以做什么来让调试变得更容易？
   1. 在 `Order` 类上使用 `DebuggerDisplayAttribute`。
   2. 在 `Order` 类上重写 `ToString`。
   3. 在 `Order` 类上使用 `ConditionalAttribute`。
   4. 使用 `#line` 编译器指令以确保在发生异常时可以找到正确的位置。

3. 你正在使用自定义代码生成向你的类中插入安全检查。当发生异常时，你很难在源代码中找到正确的行。你应该怎么办？
   1. 使用 `#error` 信号错误以便更容易找到。
   2. 使用 `#line` 从调试器中隐藏不必要的行。
   3. 使用 `ConditionalAttribute` 从你的调试构建中移除安全检查。
   4. 使用 `#line` 恢复生成代码中的原始行号。

## 目标 3.5 在应用程序中实现诊断

当你的应用程序在生产环境中运行时，你仍然希望确保一切都按预期方式运行。也许客户报告某个区域的错误，而你找不到原因。可能是你的应用程序运行性能低于预期，你收到了用户的投诉。.NET Framework 提供了可以帮助你解决这些问题的功能。

本目标涵盖了：
* 实现日志记录（logging）和跟踪。
* 对你的应用程序进行性能分析（profile）。
* 创建并监控性能计数器。

## 日志记录和跟踪

当你的应用程序在生产服务器运行时，由于安全限制或应用程序的性质，有时无法调试调试。如果应用程序运行在 Windows Azure 等分布式环境的多服务器上，普通的调试器并不总是能帮你找到错误。

因此，从开始就实现`日志记录和跟踪策略`是非常重要的。`Tracing` 是你在应用程序运行时监控其执行情况的一种。跟踪信息可以非常详细；它可以显示进入了哪些方法、做了哪些决策以及应用程序运行期间发生了错误或警告。

跟踪会产生大量信息，你在调查生产应用程序中的问题时需要它。

日志记录始终开启，并用于错误报告。你可以配置日志记录以某种集中的方式收集数据。也许当出现严重问题时你希望收到电子邮件或短信。其他错误可以记录到文件或数据库中。

.NET Framework 在 `System.Diagnostics` 命名空间提供了可以帮助你进行日志记录和跟踪的类。其中一个类是 `Debug` 类，正如其名称所示，它只能用于调试构建。这是因为值为 `DEBUG` 的 `ConditionalAttribute` 被应用到了 `Debug` 类上。你可以使用它进行基础日志记录，并对你的代码执行断言。示例 3-45 显示了使用 `Debug` 类的示例。





```
Debug.WriteLine("Starting application");
Debug.Indent();
int i = 1 + 2;
Debug.Assert(i == 3);
Debug.WriteLineIf(i > 0, "i is greater than 0");
```

默认情况下，`Debug` 类将其输出写入 Visual Studio 的“输出”（Output）窗口。如果 `Debug.Assert` 语句失败，你将看到一个显示应用程序当前堆栈跟踪的对话框。该消息框会要求你重试、中止或忽略断言失败。你可以使用 `Debug.Assert` 来指示代码中的错误，以便在开发应用程序时让系统指出这些问题。

你可以使用的另一个类是 `TraceSource` 类，它在 .NET 2.0 中引入，应该代替静态的 `Trace` 类。

示例 3-46 显示了如何使用 `TraceSource` 类。

### 示例 3-46. 使用 TraceSource 类

```
TraceSource traceSource = new TraceSource("myTraceSource",
    SourceLevels.All);

traceSource.TraceInformation("Tracing application..");
traceSource.TraceEvent(TraceEventType.Critical, 0, "Critical trace");
traceSource.TraceData(TraceEventType.Information, 1, 
    new object[] { "a", "b", "c" });

traceSource.Flush();
traceSource.Close();

// 输出:
// myTraceSource Information: 0 : Tracing application..
// myTraceSource Critical: 0 : Critical trace
// myTraceSource Information: 1 : a, b, c
```

如你所见，你可以向跟踪方法传递 `TraceEventType` 类型的参数。你使用它来指定正在发生的事件的严重程度。这些信息随后会被 `TraceSource` 用于确定确定应该输出哪些信息。

你可以对 `TraceEventType` 枚举使用几种不同的选项：

*   `Critical`（严重）。这是最严重的选项。应该节节使用，仅用于非常严重且无法恢复的错误。
*   `Error`（错误）。此枚举成员的优先级略低于 `Critical`，但它仍然表示应用程序出现了问题。它通常用于标记已处理或已恢复的问题。
*   `Warning`（警告）。此值表示发生了异常情况，可能值得进一步调查。例如，你注意到某个操作的处理时间突然比正常情况下长，或者你标记了服务器内存不足的警告。
*   `Information`（信息）。此值表示进程正在正确执行，但在跟踪输出文件中仍可以包含一些有趣的信息。这可能是关于用户登录系统的信息，或者是数据库中添加了某些内容的信息。
*   `Verbose`（详细）。这是枚举中所有与严重程度相关的值中最宽松的。它应该用于那些不指示应用程序出现任何问题、且可能大量出现的信息。例如，当对某个类型中的所有方法进行插桩以跟踪它们的开始和结束时，通常会使用详细事件类型。
*   `Stop, Start, Suspend, Resume, Transfer`（停止、开始、挂起、恢复、传输）。这些事件类型不是严重程度指示，而是将跟踪事件标记为与应用程序逻辑流相关。它们被称为 `activity event types`（活动事件类型），标记逻辑操作的开始或停止，或将控制转移到另一个逻辑操作。

跟踪方法的第二个参数是 `event ID 数字`。此数字没有任何预定义的含义；它只是将你的事件分组在一起的另一种方式。例如，你可以将数据库调用分组为数字 10000–10999，将 Web 服务调用分组为 11000–11999，以便更容易地判断跟踪条目与应用程序的哪个区域相关。

第三个参数是一个包含要跟踪消息的字符串。当你使用 `TraceData` 方法时，可以传递本应输出到跟踪中的额外参数。

在调试期间，将所有信息写入“输出”窗口可能很有用，但在生产环境中并不如此。要更改此行为，`Debug` 和 `TraceSource` 类都有一个 `Listeners` 属性。该属性包含 `TraceListeners` 集合，这些监听器处理来自 `Write`、`Fail` 和 `Trace` 方法的信息。

默认情况下，`Debug` 和 `TraceSource` 类都使用 `DefaultTraceListener` 类的实例。`DefaultTraceListener` 写入“输出”窗口并在断言失败时显示消息框。

你可以使用 .NET Framework 部分的其他几个 `TraceListeners`。表 3-2 显示了可用监听器的列表。

### 表 3-2. .NET Framework 中的 TraceListeners

| 名称 | 输出 |
| --- | --- |
| `ConsoleTraceListener` | 标准输出或错误流 |
| `DelimitedListTraceListener` | `TextWriter` |
| `EventLogTraceListener` | `EventLog` |
| `EventSchemaTraceListener` | XML 编码的、符合模式的日志文件 |
| `TextWriterTraceListener` | `TextWriter` |
| `XmlWriterTraceListener` | 写入 `TextWriter` 或流的 XML 编码数据 |

如果你不想让 `DefaultTraceListener` 激活，则需要清空当前的监听器集合。你可以添加任意数量的监听器。在示例 3-47 的示例中，移除了 `DefaultTraceListener` 并配置了 `TextWriterTraceListener`。运行此代码后会创建一个名为 `tracefile.txt` 的输出文件，其中包含跟踪内容。

### 示例 3-47. 配置 TraceListener

```
Stream outputFile = File.Create("tracefile.txt");
TextWriterTraceListener textListener =
    new TextWriterTraceListener(outputFile);

TraceSource traceSource = new TraceSource("myTraceSource",
    SourceLevels.All);

traceSource.Listeners.Clear();
traceSource.Listeners.Add(textListener);

traceSource.TraceInformation("Trace output");

traceSource.Flush();
traceSource.Close();
```

你可以通过继承 `TraceListener` 基类并为跟踪方法指定自己的实现来自自定义跟踪监听器。

通过代码指定监听器可能有用，但这不是应用程序部署后容易更改的内容。与其通过代码配置监听器，你还可以使用配置文件。示例 3-48 显示 显示了如何从配置文件配置你的跟踪源的示例。

### 示例 3-48. 使用配置文件进行跟踪

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
  <system.diagnostics>
    <sources>
      <source name="myTraceSource" switchName="defaultSwitch">
        <listeners>
          <add initializeData="output.txt" 
               type="System.Diagnostics.TextWriterListener"            
               name="myLocalListener">
               <filter type="System.Diagnostics.EventTypeFilter"
                initializeData="Warning"/>
          </add>
          <add name="consoleListener" />
          <remove name="Default"/>
        </listeners>
      </source>
    </sources>
    <sharedListeners>
      <add initializeData="output.xml" type="System.Diagnostics.XmlWriterTraceListener"
         name="xmlListener" traceOutputOptions="None" />
      <add type="System.Diagnostics.ConsoleTraceListener" name="consoleListener"
          traceOutputOptions="None" />
    </sharedListeners>
    <switches>
      <add name="defaultSwitch" value="All" />
    </switches>
  </system.diagnostics>
</configuration>
```

通过配置文件，你有很大的灵活性。在这种情况下，你配置了一个名为 `myTraceSource` 的跟踪源使用两个监听器：一个指向文件，另一个指向控制台。控制台监听器被定义为共享监听器，以便供多个跟踪源使用。





配置文件还定义了一个 `switch`，跟踪源（trace source）利用它来决定是否应该对接收到的跟踪消息进行处理。通过这种方式，你可以确定想要查看哪些跟踪消息。减少消息数量可以提高性能并产生更小的输出文件。当你找到想要关注的特定区域后，可以将开关设置为到更详细的级别。

虽然 `switch` 适用于整个跟踪源，但 `filter`（过滤器）是应用于单个监听器（listener）。当你为单个跟踪源准备了多个监听器时，可以使用过滤器来决定哪些跟踪事件实际上由监听器处理。例如，你可以设置一个监听器仅为跟踪源中的关键事件发送文本消息。

除了将跟踪信息写入文件或数据库外，你还可以将事件写入 `Windows Event Log`。你可以通过使用 `System.Diagnostics` 命名空间中的 `EventLog` 类来实现这一点。要使用 `EventLog` 类，你需要使用具有创建事件日志相应权限的账户运行。如果要在 Visual Studio 中运行它，则必须以管理员身份运行 Visual Studio。

示例 3-49 显示了如何创建一个新日志并向其写入数据。

示例 3-49. 将数据写入事件日志

```csharp
using System;
using System.Diagnostics;

class MySample
{
    public static void Main()
    {
        if (!EventLog.SourceExists("MySource"))
        {
            EventLog.CreateEventSource("MySource", "MyNewLog");
            Console.WriteLine("CreatedEventSource");
            Console.WriteLine("Please restart application");
            Console.ReadKey();
            return;
        }

        EventLog myLog = new EventLog();
        myLog.Source = "MySource";
        myLog.WriteEntry("Log event!");
    }
}
```

这些消息随后可以通过 Windows 事件查看器查看。图 3-7 显示了带有新记录日志消息的事件查看器。

![带有新自定义事件的 Windows 事件查看器](img/httpatomoreillycomsourcemspimages1722822.png.jpg)

图 3-7. 带有新自定义事件的 Windows 事件查看器

也可以通过程序方式读取事件日志。你可以通过从 `EventLog` 的 `Entries` 属性获取 `Event-LogEntry` 来实现。示例 3-50 显示了你如何读取事件日志“MyNewLog”中的最新条目。

示例 3-50. 从事件日志读取数据。

```csharp
EventLog log = new EventLog("MyNewLog");

Console.WriteLine("Total entries: " + log.Entries.Count);
EventLogEntry last = log.Entries[log.Entries.Count - 1];
Console.WriteLine("Index:   " + last.Index);
Console.WriteLine("Source:  " + last.Source);
Console.WriteLine("Type:    " + last.EntryType);
Console.WriteLine("Time:    " + last.TimeWritten);
Console.WriteLine("Message: " + last.Message);
```

`EventLog` 还提供了订阅事件日志更改的选项。它暴露了一个特殊的 `EntryWritten` 事件，你可以订阅该事件以获取更改。例如，你可以用此向系统管理员警报关键情况，这样他们就不需要手动监控日志。示例 3-51 显示了如何订阅事件日志的变化。

示例 3-51. 将数据写入事件日志

```csharp
using System;
using System.Diagnostics;

class EventLogSample
{
    public static void Main()
    {
        EventLog applicationLog = new EventLog("Application", ".", "testEventLogEvent");
        applicationLog.EntryWritten += (sender, e) =>
        {

            Console.WriteLine(e.Entry.Message);
        };
        applicationLog.EnableRaisingEvents = true;
        applicationLog.WriteEntry("Test message", EventLogEntryType.Information);

        Console.ReadKey();

    }
}
```

## 你的应用程序性能分析

在寻找性能问题时，找到它的唯一真实方法是测量，而不是猜测。也许你直觉问题出在哪里，但通过进行一些随机更改然后验证应用程序性能是否得到提高是非常困难的。

大多数时候，性能被视为某项操作所需的时间。然而，这并不是唯一的性能标准。也许你正在开发一个处理大量数据的应用程序，其限制不在于时间，而可能在于内存占用。

`Profiling`（性能分析）是确定你的应用程序如何使用某些资源的过程。例如，你可以检查程序使用了多少内存、调用了哪些方法，以及每个方法执行需要多长时间。当你遇到性能问题时，就需要这些信息。




*   `Instrumentation`（插桩）。此方法向你编译后的文件注入代码，以捕获每个被调用函数的时间信息。通过插桩，你可以找到与输入/输出（I/O）有关的问题，或者仔细检查某个特定方法。
*   `.NET memory allocation`（.NET 内存分配）。此方法会在应用程序分配新对象或对象被垃圾收集器回收中断你的程序，以便让你直观地了解程序是如何使用内存的。
*   `Resource contention data`（资源竞争数据）。此方法可以用于多线程应用程序，以找出为什么方法在访问共享资源之前必须相互等待。

如果你在不带 `Stopwatch` 代码的情况下从示例 3-49 运行应用程序，并使用 CPU 采样（CPU Sampling）选项对其进行性能剖析，你将看到一个类似于图 3-9 所示的报告。

![Profiler report](img/httpatomoreillycomsourcemspimages1722826.png.jpg)

图 3-9. 性能分析器报告

在这种情况下，大量时间消耗在 `Mscorlib.dll` 中，其中包含了 `string` 和 `StringBuilder` 类的实现。但你也可以看到第二名的函数是 `Algorithm2`。你可以使用此报告深入分析单个方法并检查哪些方法应该进行优化。

### 更多信息：Visual Studio 性能分析器

有关如何使用 Visual Studio 性能分析器的更多信息，请参阅*[`msdn.microsoft.com/en-us/library/z9z62c29.aspx`](http://msdn.microsoft.com/en-us/library/z9z62c29.aspx)*。

## 创建和监控性能计数器

Windows 提供了大量的分类性能计数器，你可以使用它们来监控硬件、服务、应用程序和驱动程序。性能计数器的示例包括显示 CPU 使用率和内存占用，以及特定应用的计数器，例如 SQL Server 查询的长度。

Windows 提供的性能计数器可以使用名为 `Perfmon.exe` 的特殊程序进行查看。图 3-10 显示了检查 CPU 数据时性能监视器的界面。

![Windows Performance Monitor](img/httpatomoreillycomsourcemspimages1722828.png.jpg)

图 3-10. Windows 性能监视器

你可以使用 `System.Diagnostics` 命名空间下的 `PerformanceCounter` 类从代码中读取性能计数器的值。示例 3-50 展示了访问性能计数器以读取可用内存并将其显示在屏幕上的示例。

示例 3-53. 从性能计数器读取数据

```
using System;
using System.Diagnostics;

namespace PerformanceCounters
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Press escape key to stop");
            using (PerformanceCounter pc = 
                         new PerformanceCounter("Memory", "Available Bytes"))
            {
                string text = "Available memory: ";
                Console.Write(text);
                do
                {
                    while (!Console.KeyAvailable)
                    {
                        Console.Write(pc.RawValue);
                        Console.SetCursorPosition(text.Length, Console.CursorTop);
                    }
                } while (Console.ReadKey(true).Key != ConsoleKey.Escape);
            }
        }
    }
}
```

所有性能计数器都是某个类别的部，并且在该类别内它们具有唯一的名称。要访问性能计数器，你的应用程序必须在全信任下运行，或者其运行的账户应该是管理员或 Performance Monitor Users 组的一员。

所有性能计数器都实现了 `IDisposable`，因为它们访问了未托管资源。在完成性能计数器后，最好立即销毁它。

### 更多信息：IDisposable

有关实现和使用 `IDisposable` 的更多信息，请参阅第 2 章。

性能计数器有多种类型。类型定义决定了计数器与监控应用程序的交互方式。以下是一些可能用的类型：

*   `NumberOfItems32/NumberOfItems64`。这些类型可用于计算操作或项的数量。`NumberOfItems64` 与 `NumberOfItems32` 相同，只是它使用更大的字段来容纳更大的值。
*   `RateOfCountsPerSecond32/RateOfCountsPerSecond64`。这些类型可用于计算每秒某个项或操作的数量。`RateOfCountsPerSecond64` 与 `RateOfCountsPerSecond32` 相同，只是它使用更大的字段来容纳更大的值。
*   `AvergateTimer32`。计算执行过程或处理项的平均时间。

示例 3-54 展示了创建和使用你自定义性能计数器的示例。第一次，应用程序将创建两个性能计数器。第二次，它将计数计数器加 1。如果你以管理员身份运行此程序并关注性能监控工具，你将看到计数器在更新。

示例 3-54. 从性能计数器读取数据

```
using System;
using System.Diagnostics;

namespace PerformanceCounters
{
    class Program
    {

        static void Main(string[] args)
        {
            if (CreatePerformanceCounters())
            {
                Console.WriteLine("Created performance counters");
                Console.WriteLine("Please restart application");
                Console.ReadKey();
                return;
            }
            var totalOperationsCounter = new PerformanceCounter(
                "MyCategory",
                "# operations executed",
                "",                
                false);
            var operationsPerSecondCounter = new PerformanceCounter(
                "MyCategory",
                "# operations / sec",
                "",
               false);

            totalOperationsCounter.Increment();
            operationsPerSecondCounter.Increment();
        }
        private static bool CreatePerformanceCounters()
        {
            if (!PerformanceCounterCategory.Exists("MyCategory"))
            {
                CounterCreationDataCollection counters = 
                    new CounterDataCollection
                {
                    new CounterCreationData(
                        "# operations executed",
                        "Total number of operations executed",
                        PerformanceCounterType.NumberOfItems32),
                    new CounterCreationData(
                        "# operations / sec",
                        "Number of operations executed per second",
                        PerformanceCounterType.RateOfCountsPerSecond32)
                };

                PerformanceCounterCategory.Create("MyCategory",
                        "Sample category for Codiproject", counters);

                return true;
            }

            return false;
        }
    }
}
```




在这一思维实验中，请应用你在本目标中学到的知识。你可以在章节末的答案]部分找到这些问题的答案。

你正在构建一个托管在分布式环境中的在线网商店。你的网商店需要良好的扩展性，因此性能是一个重要的概念。

1. 你会在网商店中将哪些事件写入跟踪源（trace source）？
2. 你可以如何使用性能计数器（performance counters）来监控你的性能？

## 目标总结

* 日志记录和跟踪对于监控生产环境中的应用程序非常重要，并且应该从开始就开始实现。
* 你可以使用 `Debug` 和 `TraceSource` 类来记录日志和跟踪消息。通过配置不同的监听器（listeners），你可以配置应用程序以将哪些数据发送到何处。
* 当你遇到性能问题时，可以对应用程序进行性能分析以找到根原因并修复它。
* 性能计数器可以持续监控应用程序的健康状况。

### 目标回顾

回答以下问题以测试对本目标信息的掌握情况。你可以在这些问题的答案以及对每个选项正确或错误的解释，可以在章节末尾的答案]部分找到。

1. 你正在使用 `TraceSource` 类为应用程序跟踪数据。当订单无法提交到数据库且你准备进行重试时，你应该使用哪个 `TraceEventType`？
   1. `Information`
   2. `Verbose`
   3. `Critical`
   4. `Error`

2. 用户报告了你应用程序中的中的错误，你想配置应用程序输出更多的跟踪数据。你应该更改哪个配置设置？
   1. `NumberOfItems32`
   2. `Listener`
   3. `Filter`
   4. `Switch`

3. 你正在开发一个拥有大量用户的全球化应用程序。运维人员请求有关每秒用户登录次数的信息。你应该做什么？
   1. 添加一个 `TraceSource` 并将每次登录写入文本文件。
   2. 使用 `RateOfCountsPerSecond64` 类型实现性能计数器。
   3. 使用性能分析器（profiler）对应用程序进行插桩，以便确切看到登录方法被调用了多少次。
   4. 使用 `EventLog` 类为每次登录向事件日志写入一个事件。

## 章节总结

* 验证应用程序输入对于确保应用程序的稳定性和至关重要。你可以使用 `Parse`、`TryParse` 和 `Convert` 函数来解析用户输入。正则表达式（Regular Expressions）可用于模式匹配。
* 密码学结合使用对称、非对称算法以及哈希算法来保护数据。
* 代码访问权限可以限制程序可能执行的操作类型。
* 程序集（assembly）是一个包含应用程序代码和元数据的自包含单元。程序集可以进行签名、版本控制，并通过将其放入全局程序缓存（GAC）进行共享。
* 通过选择正确的构建配置，你可以输出额外信息以创建程序数据库文件，并用于调试应用程序。
* 通过使用日志记录、跟踪和性能计数器，你可以在应用程序运行期间对其进行监控。

## 答案

本节包含本章思维实验的解决方案以及课程回顾问题的答案。

## 目标 3.1：思维实验

1. 看起来恶意用户正在文本字段中输入 HTML 脚本。这些数据被提交到服务器，并在下次查看页面时进行渲染。
2. 你需要使用正则表达式来限制用户输入。通过明确允许哪些字符，你可以剔除输入中的 HTML 字符并确保它们不会出现在页面布局中。

### 目标 3.1：回顾

1. **正确答案：** B
   1. **错误：** `Parse` 在用户输入无效日期时会抛出异常，这并不罕见。
   2. **正确：** `TryParse` 会检查输入的值是否为有效日期。如果不是，它将优雅返回而不是抛出异常。
   3. **错误：** `Convert.ToDateTime` 内部使用 `Parse`。当输入数据格式错误时，它会抛出异常。
   4. **错误：** `RegEx.Match` 可用于检查是否为有效日期。它无法将输入字符串转换为 `DateTime` 对象。

2. **正确答案：** B
   1. **错误：** 货币不应该存储在整数，因为无法存储小数。
   2. **正确：** 你需要指定 `NumberStyles.Currency` 和用户使用的区域设置（culture）来正确解析 `DateTime`。
   3. **错误：** 使用服务器区域设置没有考虑到用户文化的差异。你还需要 `NumberStyles.Currency` 参数来确保用户可以输入货币符号。
   4. **错误：** 留空区域设置默认为操作系统的区域设置。你还需要 `NumberStyles.Currency` 参数来确保用户可以输入货币符号。

## 目标 3.2：思维实验

你可以使用许多安全特性，包括以下：

* 使用数字证书确保应用程序可以安全地安装在桌面机器上。
* 使用非对称加密，通过公钥加密数据将数据发送到服务器。
* 使用非对称加密从服务器发送数据到客户端。服务器使用私钥加密；客户端使用公钥解密。
* 代码访问权限可以确保你的应用程序可以在沙箱环境中运行

### 目标 3.2：回顾

1. **正确答案：** C
   1. **错误：** 私钥应该保持保密。
   2. **错误：** 私钥应该保持保密。
   3. **正确：** 通过向对方发送公钥，他们可以使用对方的公钥加密数据发送给对方。
   4. **错误：** 私钥应该保持保密。

2. **正确答案：** D
   1. **错误：** `SHA256` 是哈希算法。它不能用于加密数据。
   2. **错误：** `RSACryptoServiceProvider` 是非对称加密算法。非对称算法不适用于加密大量数据。
   3. **错误：** `MD5CryptoServiceProvider` 是哈希算法。它不能用于加密数据。
   4. **正确：** `AesManaged` 是一种对称算法，用于加密大量数据。

3. **正确答案：** A, C
   1. **正确：** 使用数字证书 X509 可对哈希数据进行签名。如果对方使用 `Verify` 方法，它可以检查哈希是否发生了更改。
   2. **错误：** 该方法使用非对称算法加密数据。它不能确保数据未被篡改。
   3. **正确：** `UnicodeEncoding.GetBytes` 将字符串转换为字节序列。它并不保护数据。
   4. **错误：** 在处理 `System.SecureString` 时应使用 `Marshal` 类。`ZeroFreeBSTR` 方法可清空包含不安全字符串的内存区域。

## 目标 3.3：思维实验

1. 是的，你应该对程序集进行签名。
2. 对程序集进行签名可以防止程序集被篡改。.NET 框架会检查程序集在签名和运行之间是否被更改。
3. 签名也是使用数字证书的要求，这样应用程序的用户就知道你是该应用程序的发布者。





4. 缺点可能是你无法再次引用其他未签名的程序集了。如果你拥有这些程序集，你可以对它们进行自签名。如果没有，你必须要求其发布者对其进行签名。

## 目标 3.3: 复习

1. **正确答案：** C
    - **错误：** `GAC` 中的程序集需要经过强命名。你的程序集仍然无法引用未签名的程序集。
    - **错误：** 强名称程序集无法引用未强名称的程序集。
    - **正确：** 在引用另一个程序集之前，你需要先对其进行强命名。
    - **错误：** 公钥令牌（public key token）是强名称程序集清单的一部分。未强名称程序集没有此密钥信息。它需要先进行强命名。

2. **正确答案：** B
    - **错误：** `WinMD` 文件被 Windows 8 中的 `WinRT` 使用。它不应该在此语境之外使用。
    - **正确：** 共享程序集可以部署在 `GAC` 中。其他应用程序可以在那里引用它。当你想要更新它时，可以通过将新版本部署到 `GAC` 来实现。通过使用配置文件，你可以让其他应用程序引用你的新程序集。
    - **错误：** 你可以使用 `assemblyBinding` 配置元素为程序集添加额外的搜索位置。然而这将要求每个客户端应用程序进行更改。`GAC` 是共享程序集需要部署的位置。
    - **错误：** 对程序集进行强命名并不会使其成为共享程序集。每个应用程序仍然需要自己的副本。

3. **正确答案：** A, B
    - **正确：** 为了能够在内网上引用程序集，必须对程序集进行强命名。
    - **正确：** `codebase` 配置元素可以让本地应用程序知道它们可以在其他位置（如内网）找到程序集。
    - **错误：** 将其部署到 `GAC` 不会将程序集放在内网中。
    - **错误：** 探测选项（probing option）只能用于提供相对于应用程序路径的额外位置。它不能用于指向内网。

## 目标 3.4: 思考实验

1. 不，你不必这样做。虽然调试版本包含更多信息，但如果你有正确的 `PDB` 文件，你也可以调试发布版本。
2. 你需要确保拥有与服务器上运行的构建匹配的正确 `PDB` 文件。你需要该文件启动调试会话。
3. `Symbol Server`（符号服务器）存储你的 `PDB` 文件并帮助你的调试器找到正确的版本。如果你部署了 `Symbol Server`，你可以轻松地启动到服务器的调试会话，你的调试器会自动找到正确的 `PDB` 文件。

## 目标 3.4: 复习

1. **正确答案：** B
    - **错误：** 调试配置没有完全优化，不适用于生产环境。
    - **正确：** 发布配置经过了完全优化，将在生产环境中产生最佳结果。
    - **错误：** `PDB` 文件仅在调试应用程序时才是必要的。
    - **错误：** `/debug:full` 标志为了调试目的向你的应用程序添加额外信息。

2. **正确答案：** A
    - **正确：** `DebuggerDisplayAttribute` 属性帮助你在通过调试器检查项目时提供更有有帮助的描述。
    - **错误：** 重写 `ToString` 确实有帮助，但更好的解决方案是使用 `DebuggerDisplayAttribute`，因为这不会影响你生产环境中的代码。
    - **错误：** `ConditionalAttribute` 可用于从编译后的应用程序中移除代码。大多数情况下，它用于在进行发布构建时移除某些调用。
    - **错误：** `#line` 指令用于更改代码的行号。通常情况下，这是没有的。

3. **正确答案：** D
    - **错误：** `#error`将在编译时发出错误。
    - **错误：** `#line hidden` 会从调试器中移除额外的生成的行，但它不会恢复你的行号。
    - **错误：** 这是一个危险的解决方案，因为它在调试和发布构建之间创建了不同的行为。在处理调试构建时，你将无法测试安全检查。
    - **正确：** `#line` 指令可以告诉编译器更改代码代码的行号。这样，你可以移除生成代码的行号，以便异常与原始代码匹配。

## 目标 3.5: 思考实验

1. 示例可能包括：
    - **Critical (严重)**：发生了不可恢复的错误，例如数据库宕机导致用户无法下任何订单。
    - **Error (错误)**：在提交订单时，系统发现无法访问数据库并尝试重新提交订单。
    - **Warning (警告)**：提交订单所需的时间突然长于预期。
    - **Information (信息)**：新订单已成功提交。
    - **Verbose (详细)**：在此你可以跟踪所有的应用程序事件，例如订单流程的开始、用户如何在你线网店中导航，以及他做出了哪些决策。
2. 你可以使用性能计数器跟踪提交了多少订单，以及将它们保存到数据库需要多长时间。

## 目标 3.5: 复习

1. **正确答案：** D
    - **错误：** 订单失败不应该被仅仅视为信息性事件。它应该被视为严重的。
    - **错误：** Verbose 应仅用于详细的跟踪消息。
    - **错误：** 你仍然从错误中恢复，使其属于 Error 而不是 Critical。
    - **正确：**你应该让操作人员知道出现了问题以及你正在尝试恢复。如果恢复失败，你应该记录一个 Critical 事件。

2. **正确答案：** D
    - **错误：** `NumberOfItems32` 是创建性能计数器的选项。
    - **错误：** 监听器（listener）决定如何处理跟踪事件。它不影响哪些事件被跟踪。
    - **错误：** 过滤器（filter）用于过滤监听器处理的消息。它不影响哪些事件被跟踪。
    - **正确：** 开关（switch）值决定了处理哪些跟踪事件。通过降低开关的级别，你将在输出中看到更多的跟踪事件。

3. **正确答案：** B
    - **错误：** 将事件写入文本文件仍然需要工具来解析文本文件并向操作人员提供结果。
    - **正确：** 此性能计数器将帮助操作人员精确查看每秒钟发生的情况。
    - **错误：** 剖析器插桩（Profiler instrumentation）会显著减慢应用程序的性能。它也不是操作人员易于阅读的内容。
    - **错误：** 虽然操作人员可以读取事件日志，但他们必须手动计算所有事件来计算每秒登录数。





在处理数据时，你还需要了解数据的 `serializing`（序列化）。在本章中，你将学习不同类型的序列化以及如何配置它们以满足你的需求。

当你谈论数据时，你还需要内存构造结构来处理它。这就是 `collections`（集合）大显用场的地方。在本章，你将查看 .NET Framework 为不同场景提供的集合，以及你如何创建自己的集合。

## 本章目标：

* 目标 4.1：执行 I/O 操作
* 目标 4.2：消费数据
* 目标 4.3：使用 LINQ 查询和操作数据及对象
* 目标 4.4：序列化和反序列化数据
* 目标 4.5：在集合中存储和从集合中检索数据

## 目标 4.1：执行 I/O 操作

构建应用程序时处理文件是一项常见任务。有时你必须创建一个文件来存储数据，或者解析文件并从中提取某些内容。你可能正在写入纯文本或二进制数据——这时就可以使用 `Stream` 对象。你可能正在使用流通过网络将字节发送到另一个应用程序。.NET Framework 也为这些场景提供了支持。

在处理输入/输出（I/O）时，另一个重要主题是性能。C# 中新的 `async` 关键字可以轻松实现异步操作，从而提高应用程序的用性和扩展性。

本目标涵盖了如何：

* 处理文件。
* 处理流。
* 从网络读写数据。
* 实现异步 I/O 操作。

## 处理文件

`Files` 是几乎每个应用程序的一个重要方面。这就是为什么 .NET Framework 提供了一套可以帮助你完成所有文件相关工作的基础。所有必要的类型都可以在 `System.IO` 命名空间找到。

### 驱动器

在处理文件系统时，你显然从存储介质开始，这可以是硬盘、CD 播放器或其他存储类型。.NET Framework 提供了 `DriveInfo` 类来访问计算机上的驱动器。`DriveInfo` 对象没有用于处理驱动器的特定方法（例如，CD 播放器没有 `eject` 方法）。但它有几个属性可以访问信息，如驱动器名称、大小和可用空空间。示例 4-1 显示了如何枚举当前驱动器并显示关于它们的一些信息。

示例 4-1. 列出驱动器信息

```
DriveInfo[] drivesInfo = DriveInfo.GetDrives();

foreach (DriveInfo driveInfo in drivesInfo)
{
    Console.WriteLine("Drive {0}", driveInfo.Name);
    Console.WriteLine("  File type: {0}", driveInfo.DriveType);

    if (driveInfo.IsReady == true)
    {
        Console.WriteLine("  Volume label: {0}", driveInfo.VolumeLabel);
        Console.WriteLine("  File system: {0}", driveInfo.DriveFormat);
        Console.WriteLine(
            "  Available space to current user:{0, 15} bytes",
            driveInfo.AvailableFreeSpace);

        Console.WriteLine(
            "  Total available space:          {0, 15} bytes",
            driveInfo.TotalFreeSpace);

        Console.WriteLine(
            "  Total size of drive:            {0, 15} bytes ",
            driveInfo.TotalSize);
    }
}
```

# 目录

驱动器包含目录和文件列表。要处理这些项，你可以使用 `DirectoryInfo` 对象或静态 `Directory` 类。这两个类都提供了对你的文件夹结构的访问。当对文件系统执行单个操作时，使用静态 `Directory` 类可能更高效。当你想要对一个文件夹执行多个操作时，`DirectoryInfo` 是更好的选择。

你可以使用这两个类来创建新文件夹。当你创建一个新文件夹时，你自动拥有该文件夹的读写权限。示例 4-2 显示了如何使用静态 `Directory` 类或 `DirectoryInfo` 创建新目录。

示例 4-2. 创建新目录

```
var directory = Directory.CreateDirectory(@"C:\Temp\ProgrammingInCSharp\Directory");

var directoryInfo = new DirectoryInfo(@"C:\Temp\ProgrammingInCSharp\DirectoryInfo");
directoryInfo.Create();
```

如你所见，`DirectoryInfo` 对象可以使用不存在的文件夹进行初始化。调用 `Create` 将创建该目录。创建文件夹后，你可以调用 `DirectoryInfo` 对象的实例成员，该对象现在指向新创建的文件夹。

你可能会尝试在一个你不具有足够权限的位置创建新目录。在这种情况下，将抛出 `UnauthorizedAccessException`。

你也可以删除文件夹，但尝试删除一个不存在的文件夹会抛出 `DirectoryNotFoundException`。你可以使用静态 `Directory` 类上的 `Exists` 方法或 `DirectoryInfo` 对象上的 `Exists` 属性来判断文件夹是否存在（参见示例 4-3）。

示例 4-3. 删除已存在的目录

```
if (Directory.Exists(@"C:\Temp\ProgrammingInCSharp\Directory"))
{
    Directory.Delete(@"C:\Temp\ProgrammingInCSharp\Directory");
}

var directoryInfo = new DirectoryInfo(@"C:\Temp\ProgrammingInCSharp\DirectoryInfo");
if (directoryInfo.Exists)
{
    directoryInfo.Delete();
}
```

在处理目录和文件时需要记住的一点是，操作系统控制对你本地计算机或共享网络驱动器上所有元素的访问。可以使用 `System.Security.AccessControl` 命名空间中的 `DirectorySecurity` 类来安排文件夹的访问。示例 4-4 显示了你可以如何使用这些工具允许所有人访问文件夹。当然，这需要执行程序具有进行此修改的权限。

示例 4-4. 设置目录的访问控制

```
DirectoryInfo directoryInfo = new DirectoryInfo("TestDirectory");
directoryInfo.Create();
DirectorySecurity directorySecurity = directoryInfo.GetAccessControl();
directorySecurity.AddAccessRule(
            new FileSystemAccessRule("everyone", 
                                     FileSystemRights.ReadAndExecute, 
                                     AccessControlType.Allow));
directoryInfo.SetAccessControl(directorySecurity);
```

除了创建和删除目录的方法外，还可以查询属性、子目录或文件的方法。

`Directory` 和 `DirectoryInfo` 类都具有获取给定目录所有子目录的方法。这返回一个 `DirectoryInfo` 对象的数组。




你可以指定一个搜索模式和一个 `SearchOption` 类型的枚举，这允许你自动仅搜索顶层文件夹或所有子文件夹。在遍历所有文件夹时，可能会尝试访问一个没有所需访问权限的文件夹。这将抛出 `UnauthorizedAccessException`。当你使用 `SearchOption.AllDirectories` 且抛出异常时，你将无法获得任何结果。示例 4-5 展示了手动遍历目录树并处理可能发生的任何异常的示例。它还展示了如何使用搜索模式将将搜索结果限制在所有包含字符 `a` 的文件夹中。它限制了函数的递归深度，以确保你可以控制该方法执行的时间。

#### 示例 4-5. 构建目录树

```
private static void ListDirectories(DirectoryInfo directoryInfo,
    string searchPattern, int maxLevel, int currentLevel)
{
    if (currentLevel >= maxLevel )
    {
        return;
    }

    string indent = new string('-', currentLevel);

    try
    {
        DirectoryInfo[] subDirectories = directoryInfo.GetDirectories(searchPattern);

        foreach (DirectoryInfo subDirectory in subDirectories)
        {
            Console.WriteLine(indent + subDirectory.Name);
            ListDirectories(subDirectory, searchPattern,maxLevel, currentLevel + 1);
        }
    }
    catch (UnauthorizedAccessException)
    {
        // 你没有访问此文件夹的权限。 
        Console.WriteLine(indent + "Can't access: " + directoryInfo.Name);
        return;
    }
    catch (DirectoryNotFoundException)
    {
        // 文件夹在迭代时被删除了
        Console.WriteLine(indent + "Can't find: " + directoryInfo.Name);
        return;
    }
}

// 列出包含字符 'a' 的 Program Files 子目录，最大深度为 5

DirectoryInfo directoryInfo = new DirectoryInfo(@"C:\Program Files");
ListDirectories(directoryInfo, "*a*", 5, 0);
```

搜索模式可以由几个通配符组成，形成一个搜索模式，如表 4-1 所示。

#### 表 4-1. 搜索模式的通配符

| 通配符 | 描述 | 示例 |
| --- | --- | --- |
| `*` | 零或多个字符 | `m` 匹配 Common Files 和 Media，但不匹配 Windows |
| `?` | 任意一个字符 | `?edia` 匹配 Media，但不匹配 Windows Media Player |

在处理巨大的目录树时，使用 `EnumerateDirectories` 而不是 `GetDirectories` 可能更高效。使用 `EnumerateDirectories` 时，你可以在集合完全检索之前开始枚举。使用 `GetDirectories` 时，你会得到一个文件夹列表，并且必须等待整个列表准备好。

另一个实用的方法是当你想要将现有目录移动到新位置时，使用 `DirectoryInfo` 类上的 `MoveTo` 方法或 `Directory` 类上的 `Move` 方法。示例 4-6 展示了如何使用它们。

#### 示例 4-6. 移动目录

```
Directory.Move(@"C:\source", @"c:\destination");

DirectoryInfo directoryInfo = new DirectoryInfo(@"C:\Source");
directoryInfo.MoveTo(@"C:\destination");
```

除了检查某个目录包含哪些子目录外，你还可以处理目录中包含的文件。如示例 4-7 所示，静态函数 `Directory.GetFiles(string path)` 返回一个字符串数组，而 `DirectoryInfo.GetFiles()` 返回一个 `FileInfo` 对象的数组。这引出了我们下一个下一个话题。

#### 示例 4-7. 列出目录中的所有文件

```
foreach (string file in Directory.GetFiles(@"C:\Windows"))
{
    Console.WriteLine(file);
}

DirectoryInfo directoryInfo = new DirectoryInfo(@"C:\Windows");
foreach (FileInfo fileInfo in directoryInfo.GetFiles())
{
    Console.WriteLine(fileInfo.FullName);
}
```

## 处理文件

目录的必要性是为了为它们需要存储的文件提供某种结构。与目录一样，你可以使用静态的 `File` 类和 `FileInfo` 对象来访问文件。

你可以确定文件是否存在，当文件存在时，你可以采取行动，例如删除它。示例 4-8 展示了如何查看文件是否存在，并在其存在时删除它。

#### 示例 4-8. 删除文件

```
string path = @"c:\temp\test.txt";

if (File.Exists(path))
{
    File.Delete(path);
}

FileInfo fileInfo = new FileInfo(path);

if (fileInfo.Exists)
{
    fileInfo.Delete();
}
```

你还可以通过 `File.Move(string source, string destination)` 或 `FileInfo.MoveTo(string destination)` 来移动文件。如果通过手动拼接字符串无法实现这一点，你可以使用这些方法，如后文所示。示例 4-9 展示了如何使用它们。示例 4-10 展示了如何复制文件。

### 处理路径

在访问文件时，你经常需要组合目录和文件名。手动拼接它们虽然可行，但很容易出错。例如，如示例 4-11](#ch04.html_manually_concatenate_strings "示例 4-11. 手动拼接字符串")所示会导致无效路径。

#### 示例 4-11. 手动拼接字符串

```
string folder = @"C:\temp";
string fileName = "test.dat";

string fullPath = folder + fileName; // 结果为 C:\temptest.dat
```

静态类 `Path` 可以帮助你处理这些情况。这些方法之一是 `Combine` 方法，它有接受多个字符串参数的重载。示例 4-12 展示了 `Combine` 方法如何得到正确的路径。

#### 示例 4-12. 使用 Path.Combine

```cs
string folder = @"C:\temp";
string fileName = "test.dat";

string fullPath = Path.Combine(folder, fileName); // 结果为 C:\temp\test.dat
```

`Path` 类还提供了其他有帮助的方法：`GetDirectoryName`、`GetExtension`、`GetFileName` 和 `GetPathRoot`。示例 4-13 展示了你如何对包含完整路径的字符串使用这些方法。

#### 示例 4-13. 使用其他 Path 方法解析路径

```cs
string path = @"C:\temp\subdir\file.txt";

Console.WriteLine(Path.GetDirectoryName(path)); // 输出 C:\temp\subdir
Console.WriteLine(Path.GetExtension(path)); // 输出 .txt
Console.WriteLine(Path.GetFileName(path)); // 输出 file.txt
Console.WriteLine(Path.GetPathRoot(path)); // 输出 C:\
```

`Path` 类在你需要临时存储某些数据时也可以提供帮助。你可以使用 `GetRandomFileName` 创建随机的文件或目录名称。`GetTempPath` 返回当前用户临时文件夹的位置，而 `GetTempFileName` 则创建一个临时文件，然后可以使用它来存储某些数据。

### 考试提示





永远不要尝试手动拼接字符串来形成路径。在组合多个字符串以形成合法路径时，请务必使用 `Path` 类。

### 处理流（streams）

当然，你对文件进行的最有趣的操作就是创建和读取它们。在 .NET Framework 中处理文件时，了解 `Stream` 类非常重要，它是 .NET Framework 中用于 I/O 操作的基类。它是字节序列的抽象。例如，文件本质上是存储在你的硬盘或 DVD 上的字节序列，但网络套接字（socket）也像进程间通信管道一样处理字节序列。`Stream` 类为所有这些类型的输入/输出提供了一个通用接口。

### 基 `Stream` 类

流有三个基本操作：

*   读取（Reading）
*   写入（Writing）
*   寻址（Seeking）

从流中`Reading` 意味着你获取了一系列字节。然后你可以将这些字节转换为某些有意义的数据（如文本），或将它们反序列化为对象。

`Writing` 是相反的操作：你将一个对象转换为一系列字节，然后将其发送到流中。随后它可以通过网络发送，或持久化到其他存储介质（如硬盘）的文件中。

`Seeking` 指某些流具有当前位置的概念。你可以查询光标的当前位置并移动它。并不是所有流都支持`Seeking`。文件大多支持 `seeking`（取决于文件类型）。但 `network socket` 并没有当前位置的概念。你无法在网络电缆发送给你的字节流中向前或向后移动。

在使用 `File` 和 `FileInfo` 类时，你经常会遇到 `FileStream`，它支持在文件中读取和写入字节的方法，以及通过执行寻址（seek）操作设置当前位置的方法。示例 4-14 显示了如何使用 `FileStream` 创建文件。

示例 4-14. 创建并使用 `FileStream`

```csharp
string path = @»c:\temp\test.dat»;

using (FileStream fileStream = File.Create(path))
{
    string myValue = "MyValue";
    byte[] data = Encoding.UTF8.GetBytes(myValue);
    fileStream.Write(data, 0, data.Length);
}
```

在向 `FileStream` 写入时，你可以使用同步方法 `Write`，它期望一个 `byte array`。一个简单的 `File` 对象并不直接存储文本。如前提到的，`Stream` 是基于字节工作的，因此你需要将文本转换为字节。

### 更多信息：使用同步和异步 I/O 操作

有关异步和同步 I/O 操作之间区别的更多信息，请参阅本章后半部分的章节 实现异步 I/O 操作。

### 编码与解码

将字符转换为字节（以及反之）的过程被称为 `encoding`（编码）和 `decoding`（解码）。Unicode 联盟负责维护描述这种过程如何发生的标准。

`char` 是最基础的字符类型，等于内存中占用 2 个字节的单个 Unicode 字符。`string` 仅仅是 `char` 的序列。`System.Text.Encoding` 是帮助你在字节和字符串之间转换的类。

.NET Framework 提供了你可以使用的多种编码标准。`UTF-8` 是适用于通用用途的一种。它可以表示所有的 Unicode 字符，并被用许多 .NET Framework 类的默认编码。其他编码包括 `ASCII`、`BigEndianUnicode`、`Unicode`、`UTF32` 和 `UTF7`。

为了在处理文本时更加方便，`File` 类还支持 `CreateText` 方法，它可以为你创建一个带有 UTF-8 编码的文件。`CreateText` 返回一个 `StreamWriter`，该类继承自 `TextWriter`，并允许你使用特定的编码直接向 `Stream` 写入字符，如示例 4-15 所示。

示例 4-15. 使用 `StreamWriter` 使用 `File.CreateText`

```csharp
string path = @»c:\temp\test.dat»;

using (StreamWriter streamWriter = File.CreateText(path))
{
    string myValue = «MyValue»;
    streamWriter.Write(myValue);
}
```

当然，你也会想从文件中读取数据。你可以通过直接使用 `FileStream` 对象读取字节，并使用正确的编码将其转换回字符串。示例 4-16 显示了如何从文件中读取字节并将其转换为 UTF-8 编码的字符串。

示例 4-16. 打开 `FileStream`并将字节解码为字符串

```csharp
using (FileStream fileStream = File.OpenRead(path))
```

如果你知道自己正在解析文本，也可以使用 `StreamReader`（作为 `StreamWriter` 的反操作）来读取文本。`StreamReader` 使用默认编码并返回。示例 4-17。

示例 4-17. 打开 `FileStream`并将字节解码为字符串

```csharp
using (FileStream fileStream = File.OpenRead(path))
```
```// Displays:
```

### 使用不同类型的流

由于 `Streams` 的设计方式，你可以将多个 `Stream` 对象组合起来执行更复杂的操作。这种原理被称为装饰模式（decorator pattern）。例如，当你想要压缩某些数据时，可以使用 `GZipStream`，它的构造函数接收另一个 `Stream` 对象。通过给它一个 `FileStream` 对象，你可以轻松地压缩数据（例如另一个文件）并将其存储到磁盘。你也可以使用 `MemoryStream` 作为 `GZipStream` 的输入或输出。你可以在 `System.IO.Compression` 命名空间找到 `GZipStream`。示例 4-18 创建了一些数据，写入文件，然后压缩该文件。

示例 4-18. 使用 `GZipStream`

```csharp
string folder = @»c:\temp»;
uncompressedFilePath = Path.Combine(folder, "uncompressed.dat");
compressedFilePath = Path.Combine(folder, "compressed.gz");
byte[] dataToCompress = Enumerable.Repeat((byte)'a', 1024 * 1024).ToArray();

using (FileStream uncompressedFileStream = File.Create(uncompressedFilePath))
{
    uncompressedFileStream.Write(dataToCompress, 0, dataToCompress.Length);
}
using (FileStream compressedFileStream = File.Create(compressedFilePath))
{
    using (GZipStream compressionStream = new GZipStream(
                compressedFileStream, CompressionMode.Compress))
    {
        compressionStream.Write(dataToCompress, 0, dataToCompress.Length);
    }
}

FileInfo uncompressedFile = new FileInfo(uncompressedFilePath);
FileInfo compressedFile = new FileInfo(compressedFilePath);

Console.WriteLine(uncompressedFile.Length); // Displays 1048576
Console.WriteLine(compressedFile.Length); // Displays 1052
```





如示例 4-18 所示，你可以将另一个 `Stream` 传递给 `GZipStream` 的构造函数。当向 `GZipStream` 写入数据时，它会压缩数据并立即将其转发到 `FileStream`。

另一个可以使用此项的示例是使用 `BufferedStream`。硬盘针对读取更大块的数据进行了优化。按字节读取文件可能比读取大块数据并逐逐字节处理它们要慢。与 `GZipStream` 一样，`BufferedStream` 在其构造函数中接收另一个 `Stream`。`BufferedStream` 帮助你检查是否可以一次读取或写入更大块的数据。示例 4-19 展示了如何向封装了 `FileStream` 的 `BufferedStream` 写入一些数据。

### 示例 4-19. 使用 `BufferedStream`

```
string path = @»c:\temp\bufferedStream.txt»;

using (FileStream fileStream = File.Create(path))
{
    using (BufferedStream bufferedStream = new BufferedStream(fileStream))
    {
        using (StreamWriter streamWriter = new StreamWriter(bufferedStream))
        {
            streamWriter.WriteLine(«A line of text.»);
        }
    }
}
```

## 文件系统不仅仅属于你个人

在这一章中，你已经多次看到程序会进行检查以确定磁盘上是否存在文件。你还创建了文件、打开了文件，并移动了一些数据。但是，如果 `File.Exists` 返回 `false`，那么在你想要创建文件时，是否可以安全地假设该文件不存在了？

不，因为你不是唯一访问文件系统的用户。当你正在操作文件系统时，其他用户正在进行完全相同的操作。也许他们删除了你想要用来创建新文件的文件夹。或者他们突然更改了某个文件的权限，导致你无法再访问它。

通常，在处理多个用户访问共享资源的情况时，我们开始使用锁定机制来同步资源的使用。C# 有一种锁定机制，你可以用它在涉及多个线程时同步对代码的访问。这确保了特定的代码不会在同一时刻被同时执行。

### 更多信息：锁定

有关如何使用锁定机制同步资源访问的更多信息，请参阅第 1 章。

然而，文件系统并没有这些机制。它是一个多线程系统，但没有任何你希望看到的安全规程。

请参考示例 4-20 中的代码，它判断文件是否存在，然后读取其中所有的文本。

### 示例 4-20. 在读取文件内容时依赖 `File.Exists`

```
private static string ReadAllText()
{
    string path = @"C:\temp\test.txt";

    if (File.Exists(path))
    {
        return File.ReadAllText(path);
    }
    return string.Empty;
}
```

另一个用户可能会调用 `Exists` 和 `ReadAllText` 之间删除该文件，这将抛出异常。然而，你可以预判可能抛出的异常，并确保你的应用程序知道如何处理它们。请参阅示例 4-21。

### 示例 4-21. 打开文件时使用异常处理

```
string path = @"C:\temp\test.txt";

try
{
    return File.ReadAllText(path);
}
catch (DirectoryNotFoundException) { }
catch (FileNotFoundException) { }

return string.Empty;
```

在操作文件系统时，你需要提醒自己异常是可能且将会发生。。对于一个处理文件的健壮应用程序来说，良好的异常处理至关重要。

### 更多信息：异常处理

有关如何处理异常以及创建健壮应用程序的更多信息，请参阅第 1 章。

## 通过网络进行通信

.NET Framework 支持让你的应用程序能够跨网络进行通信。`System.Net` 命名空间定义了大量类，这些类隐藏了执行网络操作的复杂性，同时提供了易于使用的接口。

在所有这些成员中，你可能最常用的是 `WebRequest` 和 `WebResponse`。这些类是抽象基类，提供了网络通信的支持。具体的实现定义了用于通信的协议。例如，当使用 HTTP 协议时，可以使用 `HttpWebRequest` 和 `HttpWebResponse`。

### `WebRequest` 和 `WebResponse`

`WebRequest` 和 `WebResponse` 构成了一对类，你可以结合使用它们发送信息请求，然后接收包含你请求数据的响应。

`WebRequest` 是通过使用 `WebRequest` 类上的静态方法 `Create` 创建的。`Create` 方法检查传递给它的地址，然后选择正确的协议。如果你向它传递 `[`www.microsoft.com`](http://www.microsoft.com)` 地址，它会看到你正在使用 HTTP 协议并返回一个 `HttpWebRequest`。在创建正确的 `WebRequest` 后，你可以设置其他属性，如身份验证或缓存指令。

当你完成请求组合后，调用 `GetResponse` 方法执行请求并检索响应（参见示例 4-22）。

### 示例 4-22. 执行网络请求

```
WebRequest request = WebRequest.Create("http://www.microsoft.com");
WebResponse response = request.GetResponse();

StreamReader responseStream = new StreamReader(response.GetResponseStream());
string responseText = responseStream.ReadToEnd();

Console.WriteLine(responseText); // 显示网站的 HTML

response.Close();
```

## 实现异步 I/O 操作

在处理 I/O 时，你通常必须等待操作完成。也许你必须在从硬盘读取文件之前等待，或者在网络请求从世界某处返回之前等待。

到目前为止，在本章中看到的所有代码都是*同步*代码。代码按行执行，并等待每个方法完成。一行看起来很无害的代码在等待它完成时，可能会突然花费大量时间。这可能会对用户体验和应用程序的可扩展性产生严重影响。

当你创建一个桌面应用程序（如 Windows Presentation Foundation (WPF)、WinForm 或 Windows Store 应用程序）时，你的应用程序有一个主线程负责更新用户界面。该线程负责处理所有的用户活动。如果该线程忙于其他事情，应用程序就会显得无响应。大多数用户会尝试关闭此类应用程序，因为他们认为出了问题。在另一个线程上执行耗时操作是非常重要的，这确保了你的应用程序在后台执行耗时操作时保持保持响应。




对于服务器应用程序，情况略有不同。当用户访问你的 ASP.NET Web 服务器时，他必须等待请求完成才能继续。如果页面加载时间很长，用户就会认为性能很差。在服务器上发生的情况是：一个线程接管请求并开始为用户创建响应。服务器开始收集数据、生成 HTML 并执行各种其他操作。服务器处理传入请求的线程数量是有限的。当一个线程等待 I/O 操作发生时，它无法处理任何其他请求。当所有线程都忙碌且新请求进来时，新请求将会被队列。这种问题被称为“线程池饥饿”。所有线程都在等待某些 I/O 发生，但 CPU 负载为 0%，且新请求的响应时间将急升。

这就是异步操作大显身手的地方。当你的应用程序等待某些非 CPU 密集型的外部响应时，你可以让代码异步运行，以保持响应能力，并释放主线程来处理其他请求。

在 C# 5 之前，就已经可以使用异步代码。你可以使用“基于事件的异步编程”（Event-based Asynchronous Programming）模式来将代码连接起来，以便在外部请求完成后继续处理。然而，完全手动编写异步代码并处理所有细微细节是非常困难的，尤其是当你需要异常处理时。确保你的代码能够良好地处理所有情况并非易事。

### Async/await

C# 5 引入了新的 `async`/`await` 关键字。`async`/`await` 向编译器信号你想要执行某些异步代码。编译器随后负责将你“看起来是同步的”的代码转换为处理所有可能情况的状态机。

I/O 是 .NET Framework 中从 `async`/`await` 新支持中受益匪浅的领域之一。当你查看本章中的 I/O 方法时，你会发现许多方法都有异步等效方法，返回 `Task` 或 `Task<T>`。

重要的一点是，静态的 `File` 类不支持真正的异步 I/O。如果你调用异步方法，它会通过使用线程池中的另一个线程来处理文件，从而伪造成这种异步。对于真正的异步 I/O，你需要使用 `FileStream` 对象并为 `useAsync` 参数传递一个真值。

示例 4-23 显示了如何异步写入文件的示例。`Write` 方法被 `WriteAsync` 取代，该方法被标记了 `async` 修饰符，以告知编译器你想要在转换代码方面获得帮助，最后你在你在返回的任务上使用 `await` 关键字。

示例 4-23. 异步写入文件

```csharp
public async Task CreateAndWriteAsyncToFile()
{
    using (FileStream stream = new FileStream("test.dat", FileMode.Create, 
        FileAccess.Write, FileShare.None, 4096, true))
    {
        byte[] data = new byte[100000];
        new Random().NextBytes(data);

        await stream.WriteAsync(data, 0, data.Length);
    }
}
```

返回的 `Task` 对象通过封装异步操作的状态来表示某些正在进行的工作。最终，`Task` 对象将返回操作的结果或异步抛出的异常。

在示例 4-23 的情况下，该方法没有返回给调用者的任何值。这就是为什么 `WriteAsync` 返回一个普通的 `Task` 对象。当方法确实有返回值时，它返回 `Task<T>`，其中 `T` 是所返回值的类型。

在示例 4-24 中，使用了 `GetStringAsync` 方法。该方法返回 `Task<string>`，这意味着当进程结束时，最终可以使用字符串值（或是一个异常）。

示例 4-24. 执行异步 HTTP 请求

```csharp
public async Task ReadAsyncHttpRequest()
{
    HttpClient client = new HttpClient();
    string result = await client.GetStringAsync("http://www.microsoft.com");
}
```

每当 .NET Framework 提供同步方法的异步等效方法时，使用它是是最佳的。它能提供更好的用户体验和更具扩展性的应用程序。然而，当你开发一个对性能极其敏感的应用程序时，了解编译器为你做了些什么是有价值的。如果你不确定，请使用性能分析器来实际测量差异，以便你做出明智的决策。

### 并行运行 I/O 操作

真正的异步 I/O 确保你的线程在操作系统通知应用程序 I/O 已就绪之前，可以执行其他工作。多个异步 I/O 操作仍然可以一个接一个执行。

当你查看示例 4-25 时，你会看到一个方法使用了多个 `await`。在当前的代码中，每个 Web 请求在上一个请求完成后才开始。线程在运行这些请求时不会被阻塞，但方法所花费的时间是三个请求的时间总和。

示例 4-25. 执行多个 await

```csharp
public async Task ExecuteMultipleRequests()
{
    HttpClient client = new HttpClient();

    string microsoft = await client.GetStringAsync("http://www.microsoft.com");
    string msdn = await client.GetStringAsync("http://msdn.microsoft.com");
    string blogs = await client.GetStringAsync("http://blogs.msdn.com/");
}
```

但你也可以编写并行执行这些操作的代码。如果你并行执行这些请求，你只需要等待最耗时的请求即可（另外两个已经完成了）。你可以通过使用静态方法 `Task.WhenAll` 来实现。

示例 4-26. 并行执行多个请求

```csharp
public async Task ExecuteRequestsInParallel()
{
    HttpClient client = new HttpClient();

    Task microsoft = client.GetStringAsync("http://www.microsoft.com");
    Task msdn = client.GetStringAsync("http://msdn.microsoft.com");
    Task blogs = client.GetStringAsync("http://blogs.msdn.com/");

    await Task.WhenAll(microsoft, msdn, blogs);
}
```

使用 `Tasks` 和 `async/await` 让使用异步代码变得简单得多。尽可能，要判断一个操作是否耗时很长且不是 CPU 密集型的。如果是或很可能是，异步运行它是一个好主意。

思考实验

**构建文件资源管理器**

你需要为客户创建一个使用 WPF 的自定义文件资源管理器。团队的其他成员负责资源管理器的用户界面。你的任务是创建处理所有 I/O 的代码。资源管理器应该是文件系统的抽象。它不应该显示任何驱动器；相反，根据位置和文件类型将文件分组。例如，你有一个“管理”类别，包含来自多个位置的 Microsoft Office 文档。

1. 你计划使用哪些类？
2. 你如何根据特定的文件类型过滤文件？
3. 你需要异步代码吗？

目标总结

*   你可以使用 `Drive` 和 `DriveInfo` 来驱动器。

*   对于文件夹，你可以使用 `Directory` 和 `DirectoryInfo`。





*   `File` 和 `FileInfo` 提供了处理文件的方法。
*   静态的 `Path` 类可以帮助你创建和解析文件路径。
*   `Streams` 是处理系列字节的抽象方式。
*   有许多 `Stream` 实现用于处理文件、网络操作以及任何其他类型的 I/O。
*   请记住，文件系统可以被多个用户同时访问和更改。在创建可靠的应用程序时，你需要记住这一点。
*   在执行网络请求时，你可以使用 `System.Net` 命名空间下的 `WebRequest` 和 `WebResponse` 类。
*   异步 I/O 可以帮助你创建更好的用户体验和更具扩展性的应用程序。

### 目标回顾

回答以下问题以测试你对本目标中信息的掌握情况。你可以在本章末尾的答案 部分找到这些问题的答案，以及对每个备选项为何正确或不错误的解释。

1.  你正在创建一个新文件来存储某些日志数据。每当需要新的日志条目时，都会向文件中写入一个字符串。你使用哪种方法？
    1.  `File.CreateText`
    2.  `FileInfo.Create`
    3.  `File.Create`
    4.  `File.AppendText`

2.  你构建了一个复杂的计算算法。它完成需要相当长的时间，你想要确保你的应用程序保持响应状态。你会做什么？
    1.  使用 `async/await`。
    2.  同步运行代码。
    3.  使用 `Task.Run`。
    4.  使用 `BackgroundWorker`。

3.  你正在编写一个部署到西方国家的应用程序。它将用户活动输出到文本文件中。你应该使用哪种编码？
    1.  `UTF-8`
    2.  `UTF-7`
    3.  `ASCII`
    4.  `UTF-32`

## 目标 4.2：消费数据

数据管理是应用程序最重要的方面之一。想象一下你只能创建将数据存储在内存中的应用程序。用户一退出，所有数据就会丢失，随后的启动需要重新输入所有必要的数据。当然，这种情况在实际工作中是不可能的，这就是为什么 .NET Framework 帮助你以持久的方式存储数据。这可以通过直接使用 `ADO.NET` 或 `Entity Framework` 在数据库中实现。你也可以从外部 Web 服务存储并请求数据，并以 `JavaScript Object Notation`(JSON) 或 `Extensible Markup Language`(XML) 格式检索响应。.NET Framework 帮助你执行这些请求并解析返回的数据。

本目标涵盖了如何：
*   在数据库中检索和更新数据。
*   消费 JSON 和 XML。
*   访问 Web 服务。

## 与数据库工作

在 .NET Framework 中，你可以在 `System.Data.dll` 中找到各种类型的数据相关类。.NET Framework 中的数据访问代码属于 `ADO.NET` 范畴，它由两个概念部分组成：连接数据和断开数据。

当使用 `ADO.NET` 的连接部分时，你显式地连接到数据库并将其作为底层数据存储。你通过使用结构化查询语言 (`SQL`) 执行查询，以创建、读取、更新和删除数据（通常称为 `CRUD` 操作）。这些查询由 `ADO.NET` 基础设施使用并转发到你选择的数据库。在以连接方式工作时，你使用了 `Connection` 对象、`Command` 对象和 `DataReader` 对象等。

在断开连接的世界，你与 `DataSets` 和 `DataTables` 工作，它们在内存中模拟了关系型数据库的结构。你可以使用它们处理离线数据，并在在线后将它们同步到数据库。在对连接数据库执行查询后创建的 `DataSet` 可以在内存中对其进行操作，并通过 `DataAdapter` 将更改发送回数据存储。

### 更多信息：断开连接的数据

有关以断开连接的方式处理数据的更多信息，请参阅 [`msdn.microsoft.com/en-us/library/zb0sdh0b.aspx`](http://msdn.microsoft.com/en-us/library/zb0sdh0b.aspx)。

### 提供程序

在你周围的世界中有许多不同类型的数据库。你可以使用 Microsoft SQL Server、Oracle 和 MySQL 等。.NET Framework 提供了以标准方式在这些所有类型数据库中处理数据的功能。

.NET Framework `data provider`（数据提供程序）用于连接数据库、执行命令和处理产生的数据。.NET Framework 数据提供程序提供了一个薄层，与特定数据库集成，因此你可以创建可以与不同数据库工作的程序，而无需更改任何代码。

### 连接到数据库

当你处理数据库中的数据时，必须采取的第一步是创建到特定数据库的 `connection`（连接）。连接通过使用 `connection string`（连接字符串）建立，它包含了 .NET Framework 需要的所有信息：数据库类型、数据库位置以及如何对数据库进行身份验证。

.NET Framework 中的连接都继承自 `DbConnection` 基类。`SqlConnection` 可用于建立到 Microsoft SQL Server 数据库的连接。由于 `DbConnection` 类使用真实的、未管理的数据库连接，确保在完成后妥善关闭连接非常重要。由于由于，`DbConnection` 类实现了 `IDisposable`，因此你可以确定性地关闭连接。正如第 2 章 中讨论的，`using` 句将调用 `DbConnection` Dispose 方法，自动关闭连接。示例 4-27 显示了如何这样做。

示例 4-27. 使用 using 语句的 `SqlConnection` 自动关闭

```
using (SqlConnection connection = new SqlConnection(connectionString))
{
    // 对数据库执行操作
} // 连接自动关闭
```

典型的连接字符串可能如下所示：

```
"Persist Security Info=False;Integrated Security=true;Initial Catalog=Northwind;server=(local)"
```

此连接字符串描述了数据库的位置、名称以及如何对数据库进行身份验证的细节。连接字符串的基本格式是由等号 (=) 连接的键值对，并由分号 (;) 分隔。

### 更多信息：连接字符串

如果你正在寻找创建自己的连接字符串的具体信息，可以查看 [`www.connectionstrings.com/`](http://www.connectionstrings.com/)。在这里你可以找到不同提供程序的不同设置的连接字符串示例。

当你需要动态构建连接字符串时，可以使用多个 `DbConnectionStringBuilder` 类之一。例如，你可以使用 `OracleConnectionStringBuilder` 为 Oracle 数据库构建连接字符串，使用 `SqlConnectionStringBuilder` 为 Microsoft SQL Server 数据库构建。示例 4-28 显示了如何通过编程使用 `SqlConnectionStringBuilder` 创建新的连接字符串。

示例 4-28. 使用 `SqlConnectionStringBuilder` 创建连接字符串

```cs
var sqlConnectionStringBuilder = new SqlConnectionStringBuilder();

sqlConnectionStringBuilder.DataSource = @"(localdb)\v11.0";
sqlConnectionStringBuilder.InitialCatalog = "ProgrammingInCSharp";

string connectionString = sqlConnectionStringBuilder.ToString();
```





硬编码连接字符串通常不是配置应用程序的最佳方式。当你将应用程序部署到测试、分阶段或生产环境时，连接字符串通常需要更改，而大多数情况下，这种工作是由 IT 专业人员完成的，他们可能没有（也不想有！）任何编程经验。

正如此，你可以轻松地将连接字符串存储在外部配置文件中。根据应用程序的类型，使用 `app.config` 或 `web.config` 文件。这些文件可以用于存储应用程序的各种配置设置。你还可以使用其他配置文件，并在这些文件中引用它们。

应用程序 `app.config` 文件中连接字符串的示例参见示例 4-29。

示例 4-29. 在 `app.config` 文件中放置连接字符串

```xml
<?xml version="1.0" encoding="utf-8" ?>
<configuration>
    <connectionStrings>
        <add name="ProgrammingInCSharpConnection" 
     providerName="System.Data.SqlClient" 
     connectionString="Data Source=(localdb)\v11.0;Initial Catalog=ProgrammingInCSharp;"
/>
    </connectionStrings>
</configuration>
```

如果你想在应用程序中使用连接字符串，可以使用来自 `System.Configuration.dll` 的 `ConfigurationManager.ConnectionStrings` 属性。你可以通过索引或名称来访问连接字符串。示例 4-30 显示演示了如何通过名称访问连接字符串并使用它打开数据库连接。

示例 4-30. 从外部配置文件使用连接字符串

```csharp
string connectionString = ConfigurationManager.
                ConnectionStrings["ProgrammingInCSharpConnection"].ConnectionString;

using (SqlConnection connection = new SqlConnection(connectionString))
{
    connection.Open();
}
```

### 更多信息：针对不同配置的连接字符串

当你需要为不同的配置（如分阶段、测试和生产）准备不同的连接字符串时，可以使用特殊的转换语法，该语法根据你想要构建的配置来更改你的配置文件。更多信息请参阅 *[`msdn.microsoft.com/en-us/library/dd465326.aspx`](http://msdn.microsoft.com/en-us/library/dd465326.aspx)*。

连接到数据库是一项耗时的操作。保持连接过久也是一个问题，因为可能导致其他用户无法连接。为了最小化重复打开和关闭连接的成本，ADO.NET 采用了一种名为 `connection pooling`（连接池）的优化。

使用 SQL Server 时，你的应用程序会维护一个连接池。当请求新连接时，. Framework 会检查池中是否存在已打开的连接。如果有，它就不需要打开新连接并执行所有的初始设置步骤。默认情况下，连接池是启用的，这可以为你带来巨大的性能提升。

### 读取数据

建立连接后，你可以开始向数据库发送查询。查询使用 SQL 构建，SQL 是一种针对处理数据库而优化的特殊语法。

### 更多信息：SQL

有关 SQL 的更多信息，请参阅 *[`msdn.microsoft.com/en-us/library/bb510741.aspx`](http://msdn.microsoft.com/en-us/library/bb510741.aspx)*。

假设你正在处理一个类似于表 4-2 中的数据库表。

表 4-2. 示例表结构

| 列名 | 数据类型 | 是否可空 |
| --- | --- | --- |
| id | int, Primary Key | False |
| FirstName | varchar(30) | False |
| MiddleName | varchar(30) | True |
| LastName | varchar(30) | False |

你可以使用示例 4-31 中的 SQL 创建此表。

示例 4-31. 使用 SQL 脚本创建表

```sql
CREATE TABLE dbo.People
(
  [id]     INT         NOT NULL IDENTITY,
  [FirstName] VARCHAR(30) NOT NULL,
  [MiddleName] VARCHAR(30) NULL,
  [LastName]  VARCHAR(30) NOT NULL
);
```

如果你想从此表中选择几行，首先需要定义一个 SQL 语句。然后可以使用 `SqlCommand` 对象执行 SQL 查询。`SqlCommand` 可以返回一个 `SqlDataReader`，该读取器会跟踪你在结果集中的位置。它让你能够访问每一行以及其中包含的列。

示例 4-32 显示了你可以如何使用此方法遍历 `People` 表中的行并显示结果。ADO.NET 还支持新的 `async/await` 关键字，以便你可以执行查询。

示例 4-32. 执行 SQL select 命令

```csharp
public async Task SelectDataFromTable()
{
    string connectionString = ConfigurationManager.
                   ConnectionStrings["ProgrammingInCSharpConnection"].ConnectionString;

    using (SqlConnection connection = new SqlConnection(connectionString))
    {
        SqlCommand command = new SqlCommand("SELECT * FROM People", connection);
        await connection.OpenAsync();

        SqlDataReader dataReader = await command.ExecuteReaderAsync();

        while (await dataReader.ReadAsync())
        {
            string formatStringWithName = "Person ({0}) is named {1} {2} {3}";
            string formatStringWithoutName = "Person ({0}) is named {1} {3}";

            if ((dataReader["middlename"] == null))
            {
                Console.WriteLine(formatStringWithoutName, 
                    dataReader["id"], 
                    dataReader["firstname"], 
                    dataReader["lastname"]);
            }
            else
            {
                Console.WriteLine(formatStringWithName, 
                    dataReader["id"], 
                    dataReader["firstname"], 
                    dataReader["middlename"], 
                    dataReader["lastname"]);
            }
        }
        dataReader.Close();
    }
}
```

`SqlDataReader` 是一个前向的数据流。在读取时你无法后退；只能向前。你可以通过索引或名称访问结果中的每列。`SqlDataReader` 提供了几个方法，可以将列的值映射到相应的 `CLR` 类型。例如，你可以调用 `GetInt32(int index)`、`GetGuid(int index)`、`GetString(int index)` 等方法。

在执行查询时，你还可以批量处理多个 SQL 语句。返回的 `SqlDataReader` 包含多个结果集。你可以通过调用 `SqlDataReader` 对象上的 `NextResult` 或 `NextResultAsync` 来移动下一个结果集。示例 4-33 显示了如何执行一个运行两个结果集的查询。

示例 4-33. 执行具有多个结果集的 SQL 查询





```sharp
public async Task SelectMultipleResultSets()
{
    string connectionString = ConfigurationManager.
          ConnectionStrings["ProgrammingInCSharpConnection"].ConnectionString;

    using (SqlConnection connection = new SqlConnection(connectionString))
    {
        SqlCommand command = new SqlCommand("SELECT * FROM People; 
               SELECT TOP 1 * FROM People ORDER BY LastName", connection);

        await connection.OpenAsync();
        SqlDataReader dataReader = await command.ExecuteReaderAsync();
        await ReadQueryResults(dataReader);
        await dataReader.NextResultAsync(); // Move to the next result set
        await ReadQueryResults(dataReader);
       dataReader.Close();
    }
}
private static async Task ReadQueryResults(SqlDataReader dataReader)
{
    while (await dataReader.ReadAsync())
    {
        string formatStringWithMiddleName = "Person ({0}) is named {1} {2} {3}";
        string formatStringWithoutMiddleName = "Person ({0}) is named {1} {3}";
        if ((dataReader["middlename"] == null))
        {
            Console.WriteLine(formatStringWithoutMiddleName,
                dataReader["id"],
                dataReader["firstname"],
                dataReader["lastname"]);
        }
        else
        {
            Console.WriteLine(formatStringWithMiddleName,
                dataReader["id"],
                dataReader["firstname"],
                dataReader["middlename"],
                dataReader["lastname"]);
        }
    }
}
```

### 更新数据

除了查询数据并将其发送到客户端外，你还可以更新数据库中的数据。你可以创建新记录、更新现有记录或完全删除记录。

你可以通过使用连接和命令对象来实现所有这些操作。但与返回一个包含结果行的读取器不同，你将获得一个整数值，显示最后一次查询受影响的行数。这意味着如果你执行一个存储过程或将多个 SQL 语句链在一起，你只会得到最后一个查询受影响的记录数，而不是存储过程中所有查询的记录数。通过检查结果，你可以确定受影响的行数是否正确。你使用 `ExecuteNonQuery` 或 `ExecuteNonQuery-Async` 方法来执行此操作，如示例 4-34 所示。

示例 4-34. 使用 `ExecuteNonQuery` 更新行

```sharp
public async Task UpdateRows()
{
    string connectionString = ConfigurationManager.
        ConnectionStrings["ProgrammingInCSharpConnection"].ConnectionString;

    using (SqlConnection connection = new SqlConnection(connectionString))
    {
        SqlCommand command = new SqlCommand(
            "UPDATE People SET FirstName='John'",
            connection);

        await connection.OpenAsync();
        int numberOfUpdatedRows = await command.ExecuteNonQueryAsync();
        Console.WriteLine("Updated {0} rows", numberOfUpdatedRows);
    }
}
```

### 使用参数

到目前为止，你只见过在编译时已完全构建的查询。然而在现实世界中，当你执行查询时通常需要使用动态值。

由于 SQL 查询仅仅是一个简单的字符串，你可能会倾向于将多个字符串拼接起来以创建你的查询。然而，请注意，这是一个巨大的安全风险。例如，假设你有一个表单，人们可以在其中填写姓名，然后将其插入到 People 表中。你的查询看起来像这样：

```sql
INSERT INTO People VALUES('John', 'Doe', null)
```

现在，你可以读取用户输入的值，然后手动构建此字符串。但如果用户在中间名处输入以下内容会发生什么？

```sql
'); DELETE FROM People; --
```

执行此查询后，你 People 表中的所有数据将被删除。这个安全漏洞被称为 SQL 注入。

### 更多信息：SQL 注入

有关 SQL 注入的更多信息，请参阅 *[`msdn.microsoft.com/en-us/library/ms161953(v=sql.105).aspx`](http://msdn.microsoft.com/en-us/library/ms161953(v=sql.105).aspx)*。

为了防止 SQL 注入，你不应该直接在 SQL 字符串中使用用户输入。与其手动构建正确的 SQL 查询，不如使用参数化 SQL 语句（参见示例 4-35）。

示例 4-35. 使用参数化查询插入值

```sharp
public async Task InsertRowWithParameterizedQuery()
{
    string connectionString = ConfigurationManager.
        ConnectionStrings["ProgrammingInCSharpConnection"].ConnectionString;

    using (SqlConnection connection = new SqlConnection(connectionString))
    {
        SqlCommand command = new SqlCommand(
            "INSERT INTO People([FirstName], [LastName], [MiddleName]) VALUES(@
firstName, @lastName, @middleName)",
            connection);
        await connection.OpenAsync();

        command.Parameters.AddWithValue("@firstName", "John");
        command.Parameters.AddWithValue("@lastName", "Doe");
        command.Parameters.AddWithValue("@middleName", "Little");

        int numberOfInsertedRows = await command.ExecuteNonQueryAsync();
        Console.WriteLine("Inserted {0} rows", numberOfInsertedRows);
    }
}
```

这些参数化查询可以用于运行选择、更新、插入和删除查询。除了更安全之外，它们还提供了更好的性能。因为数据库获取了更具通用性的内容，它可以更容易地找到预编译的执行计划。

### 更多信息：执行计划

有关执行计划的更多信息，请参阅 *[`msdn.microsoft.com/en-us/library/ms17550.aspx`](http://msdn.microsoft.com/en-us/library/ms17550.aspx)*。

### 使用事务

在处理数据库时，可能会出现问题。也许你正在执行多个组合在一起的查询。如果最后一个执行失败，之前的查询已经执行了，导致你的数据可能会损坏。

由于由于.NET Framework 会帮助你处理事务。事务具有四个关键属性，被称为 ACID：

- **原子性 (Atomicity)**：所有操作都组合在一起。如果一个失败，则全部失败。
- **一致性 (Consistency)**：事务将数据库从一个有效状态变为另一个有效状态。
- **隔离性 (Isolation)**：事务可以独立运行。多个并发事务不会相互影响。它们就像是串行执行的一样。
- **持久性 (Durability)**：提交事务的结果将始终永久存储，即使之后立即崩溃。

在处理事务时，最简单的方法是使用 `TransactionScope` 类。`TransactionScope` 提供了一种简单处理事务的方法，无需你与事务本身交互（参见示例 4-36）。

示例 4-36. 使用 `TransactionScope`

```sharp
string connectionString = ConfigurationManager.
    ConnectionStrings["ProgrammingInCSharpConnection"].ConnectionString;

using (TransactionScope transactionScope = new TransactionScope())
{
    using (SqlConnection connection = new SqlConnection(connectionString))
    {
        connection.Open();

        SqlCommand command1 = new SqlCommand(
            "INSERT INTO People ([FirstName], [LastName], [MiddleInitial])
VALUES('John', 'Doe', null)", 
            connection);
        SqlCommand command2 = new SqlCommand(
            "INSERT INTO People ([FirstName], [LastName], [MiddleInitial])
VALUES('Jane', 'Doe', null)", 
            connection);

        command1.ExecuteNonQuery();
        command2.ExecuteNonQuery();
    }
    transactionScope.Complete();
} 
```





如果在 `TransactionScope` 内部发生异常，整个事务将回滚。如果没有发生任何错误，你使用 `TransactionScope.Complete` 来完成事务。在 `using` 语句中使用 `TransactionScope` 是重要的，这样它在不再需要时就会自动释放。

也可以通过向 `TransactionScope` 传递一个 `TransactionScopeOption` 枚举来构造它。通过使用此枚举，你可以定义 `TransactionScope` 的行为。

`TransactionScope` 可以使用三个选项进行构造：

*   `Required`。加入环境事务，如果不存在，则创建一个新的。如果存在环境事务，则由该事务控制事务何时完成。这是默认的作用范围。
*   `RequiresNew`。启动一个新事务。
*   `Suppress`。不参与任何事务。

使用 `TransactionScope` 时，.NET Framework 会自动为你管理事务。如果你的事务使用了嵌套连接、多个数据库或多个资源类型，你的事务将提升为`分布式事务`。如果没有必要，提升为分布式事务可能会对性能产生巨大影响。如果可能，请尽量避免分布式事务。如果你需要它们，.NET Framework 会为你进行管理。

### 使用对象关系映射器 (ORM)

关系型数据库的一个问题是，它本质上与你想在应用程序中使用的面向对象的结构不同。你使用的是与其他对象具有关系或继承自其他对象的对象。而数据库使用带有列和指向其他表的外键的表。这就是所谓的`对象-关系阻抗匹配`。

你可以通过手动编写 SQL 查询并在数据库上执行它们来创建复杂的应用程序。但当你的应用程序增长，并且想要使用面向对象的设计时，你就会开始遇到问题。当然，你可以将查询结果映射到对象，并根据对象的变化创建查询，但这是一项艰巨的任务。即使你喜欢这种挑战，这也不是为你的客户增加价值的东西。

这就是对象关系映射 (ORM) 软件大显身场的地方。其中一种 ORM 是微软开源的 `Entity Framework`，它减轻了映射对象、构建查询以及跟踪所有更改等繁燥工作的负担。

`Entity Framework` 可以通过几种不同的方法使用：

*   `Database First`（数据库优先）。你想要将现有数据库映射到你的对象结构。
*   `Model First`（模型优先）。你想要使用图形设计器设计你的对象模型，然后创建一个支持它的数据库。
*   `Code First`（代码优先）。你在代码中创建对象模型，然后生成一个可以存储数据的数据库。

使用 ORM 是性能和开发速度之间的权衡。你可以想象 `Entity Framework` 如何使用反射从 SQL 查询结果映射到对象，这总是比手动操作要慢。然而，使用 `Entity Framework` 将极地提高你的开发速度。它允许你通过优先考虑需要更好性能的部分来快速创建应用程序。`Entity Framework` 通常对于大多数情况来说都是足够的。如果不是，你可以为有问题的查询添加一个简单的存储过程。

假设你有一个 `Person` 类，例如 示例 4-37 所示所示。

```csharp
public class Person
{
    public int Id { get; set; }
    public string Name { get; set; }
}
```

### 更多信息：Entity Framework

关于 `Entity Framework` 的更多信息，请参阅 [`learn.microsoft.com/en-us/ef/entityframework/`](https://learn.microsoft.com/en-us/ef/entityframework/)。

## 使用 Web 服务

除了将数据存储在关系型数据库或文件中之外，另一个选项是使用外部服务。它可以可能是你创建的 Web 服务，也可以来自第三方。

通过此类服务，你可以以松耦合的方式在应用程序之间交换数据。你只需要知道服务的地址以及如何向其发送请求即可。服务如何获取数据对你来说是完全隐藏的，你通常不需要担心这些。

.NET Framework 对创建 Web 服务有坚实的支持。你可以使用另一种名为 Windows 通信基础框架 (WCF) 的技术来构建高度灵活的服务。

### 创建 WCF 服务

在过去，在构建服务时你有许多选择。你可以使用 .NET Remoting、XML Web 服务（包括基于 SOAP 的服务）或微软消息队列 (Microsoft Message Queues)，它们都有自己的选项和功能。WCF 用一个单一的、扩展的编程模型取代了所有这些技术。

一个 WCF 服务看起来像一个普通类。它可以拥有具有返回类型的方法、构造函数和其他成员。与普通类的唯一区别在于类本身及其方法之上的属性，这些属性告诉 .NET Framework 你想要将你的类作为服务暴露。

示例 4-39 显示了一个简单 WCF 服务的示例。如你所见，该类被 `ServiceContract` 属性装饰，方法被 `OperationContract` 属性装饰。

```csharp
[ServiceContract]
public class MyService
{
    [OperationContract]
    public string DoWork(string left, string right)
    {
        return left + right;
    }
}
```

你可以通过创建一个新的 ASP.NET 项目并向其中添加 WCF 服务来创建此服务。一个 WCF 服务由一个 `.svc` 文件和一个包含实际服务代码的后台代码文件组成。`.svc` 文件包含了如何在 Internet 信息服务 (IIS) 中托管你的服务的指令，因此你可以将 `.svc` 文件与关联的代码文件一起放在由 IIS 托管的网站中，以便你的用户可以使用它。

代码文件不包含任何关于如何调用该服务的信息——它没有指定地址或协议。这就是 WCF 优于以前技术的地方，因为它使用了所谓的 ABC 模型：

*   Address（地址）
*   Binding（绑定）
*   Contract（契约）





构建 WCF 服务时，你通常从 `contract`（合约）开始，它定义了你的服务暴露哪些操作。合约就是外部世界对你服务的期望。在指定了 `contract` 之后，你需要指定 `bindings`（绑定）。绑定配置了用于调用你服务的协议和传输方式。可能你的服务 1 可以通过 HTTP、HTTPS 和命名管道连接进行使用。接下来，你需要指定 `address`（地址），它是你的服务暴露的端点。这样做可以确保有一个物理网络地址，以便使用特定的 `binding` 来调用你的服务。

在与之前创建的 WCF 服务一起工作时，你可以使用 Visual Studio 为你创建一个 `service reference`（服务引用）。它会在你的客户端项目中创建一个代理类，使你能够访问外部服务。你可以在 示例 4-40 中看到 `MyService` 服务的代理类示例。

示例 4-40. 一个生成的 WCF 代理客户端

```
namespace Service.Client.ExternalService
{
    [System.CodeDom.Compiler.GeneratedCodeAttribute(«System.ServiceModel», «4.0.0.0»)]
    [System.ServiceModel.ServiceContractAttribute(
        ConfigurationName = «ExternalService.MyService»)]

    public interface MyService
    {
        [System.ServiceModel.OperationContractAttribute(
              Action = "http://tempuri.org/MyService/DoWork",
              ReplyAction = «http://tempuri.org/MyService/DoWorkResponse»)]
        string DoWork(string left, string right);

        [System.ServiceModel.OperationContractAttribute(
              Action = "http://tempuri.org/MyService/DoWork",
              ReplyAction = «http://tempuri.org/MyService/DoWorkResponse»)]
        System.Threading.Tasks.Task<string> DoWorkAsync(string left, string right);
    }

    [System.CodeDom.Compiler.GeneratedCodeAttribute(«System.ServiceModel», «4.0.0.0»)]
    public interface MyServiceChannel : Service.Client.ExternalService.MyService, 
                                          System.ServiceModel.IClientChannel
    { }

    [System.Diagnostics.DebuggerStepThroughAttribute()]
    [System.CodeDom.Compiler.GeneratedCodeAttribute(«System.ServiceModel», «4.0.0.0»)]
    public partial class MyServiceClient : 
               System.ServiceModel.ClientBase<Service.Client.ExternalService.MyService>,
               Service.Client.ExternalService.MyService
    {
        public MyServiceClient()
        { }

         public MyServiceClient(string endpointConfigurationName) :
            base(endpointConfigurationName)
        { }

        public MyServiceClient(string endpointConfigurationName, string remoteAddress) :
            base(endpointConfigurationName, remoteAddress)
        { }

         public MyServiceClient(string endpointConfigurationName,
            System.ServiceModel.EndpointAddress remoteAddress) :
                base(endpointConfigurationName, remoteAddress)
        { }

        public MyServiceClient(System.ServiceModel.Channels.Binding binding,
            System.ServiceModel.EndpointAddress remoteAddress) :
            base(binding, remoteAddress)
        { }

        public string DoWork(string left, string right) 
        {
            return base.Channel.DoWork(left, right);
        }

        public System.Threading.Tasks.Task<string> DoWorkAsync(
                              string left,
                              string right)
        {
            return base.Channel.DoWorkAsync(left, right);
        }
    }
}
```

你可以像使用普通类一样使用这个客户端。唯一的区别是，在后台，代理客户端使用来自 `app.config` 文件的配置设置来查找 `ABC` 设置。示例 4-41 展示了如何构造客户端并调用其上的方法。

示例 4-41. 使用 WCF 代理客户端

```
ExternalService.MyServiceClient client = new ExternalService.MyServiceClient();
string result = client.DoWork("John", "Doe");
Console.WriteLine(result); // Displays JohnDoe
```

通过使用客户端代理使用 WCF 服务时，`DoWork` 方法的结果会自动转换为字符串。然而，当与其他服务一起工作时，你得到的结果可能是完全不同的格式。

### 更多信息：WCF

如果你想了解更多关于 WCF 以及你如何在各种场景中使用它的信息，请参见 *[`msdn.microsoft.com/en-us/library/ms731082.aspx`](http://msdn.microsoft.com/en-us/library/ms731082.aspx).*

## 消费 XML

可扩展标记语言 (XML) 是一种标记语言，由一组定义文档如何格式化的规则组成。XML 的优势是人类和计算机程序都可以都可以读取它。它最初创建是为了作为不同应用程序之间互联网通信的唯一解决方案。

示例 4-42 显示了一个 XML 文档示例。

示例 4-42. XML 文件

```xml
<?xml version="1.0" encoding="utf-8" ?>
<people>
  <person firstName="John" lastName="Doe">
    <contactdetails>
      <email>john@unknown.com</email>
    </contactdetails>
  </person>
  <person firstName="Jane" lastName="Doe">
    <contactdetails>
      <email>jane@unknown.com</email>
      <phone>001122334455</phone>
    </contactdetails>
  </person>
</people>
```

正如你所见，XML 文档由元素组成。首先，有一行可选的行说明你正在查看 XML。这一行被称为引导（prolog）。它包含了关于使用的编码的信息并可以包含元数据。

引导之后是内容。应该有一个根元素包含其余信息。通过这种方式，你创建一个定义所有元素之间关系的树。

根元素之下是其他子元素。子元素可以包含属性，它是与元素的键值对。XML 文档还可以包含注释和特殊指令。特殊指令通常包含在类型定义（DTD）文件中，该文件存储在 XML 外部并在引导中引用。

### 更多信息：XML

关于 XML 的更多信息，请参见 *[`msdn.microsoft.com/en-us/library/ms256177.aspx`](http://msdn.microsoft.com/en-us/library/ms256177.aspx).*

### .NET Framework 中的 XML

将 XML 文件解析为文本文件是一项大量的工作。.NET Framework 通过提供可以解析、创建和编辑 XML 文件（在在内存中和磁盘上）的类来帮助你。

这些类位于 `System.Xml` 命名空间。重要的类列在表 4-3](#ch04.html_classes_for_working_with_xml "表 4-3. 用于 XML 的类") 中。

表 4-3. 用于 XML 的类

| 名称 | 描述 |
| --- | --- |
| `XmlReader` | 读取 XML 文件的快速方法。你只能向前移动，没有任何缓存。 |
| `XmlWriter` | 创建 XML 文件的快速方法。与 `XmlReader` 类似，它是只读且非缓存的。 |
| `XmlDocument` | 代表内存中的 XML 文档。它支持导航和编辑文档。 |
| `XPathNavigator` | 帮助导航 XML 文档以查找特定信息。 |

LINQ to XML

另一种处理 XML 的方法是使用 LINQ to XML。更多信息可以在本章稍后的目标 4.3，“使用 LINQ 查询和操作数据及对象”中找到。





`XmlReader` 类提供了处理 XML 数据最快的选项。它是一个抽象基类，`XmlTextReader`、`XmlNodeReader` 和 `XmlValidatingReader` 等类都继承自它。

你可以通过使用静态方法 `Create` 创建 `XmlReader` 的新实例。你可以向此方法传递一个 `XmlReaderSettings` 实例来配置如何解析 XML。通过这种方式，你可以选择跳过 XML 文件中的某些数据（如空格和注释），或者从特定位置开始。示例 4-43 展示了如何使用 `XmlReader` 解析一个包含 示例 4-42 中 XML 数据的字符串的示例。

示例 4-43. 使用 `XmlReader` 解析 XML 文件

```
string xml = @"<?xml version=""1.0"" encoding=""utf-8"" ?>
                <people>
                  <person firstname=""john"" lastname=""doe"">
                    <contactdetails>
                      <emailaddress>john@unknown.com</emailaddress>
                    </contactdetails>
                  </person>
                  <person firstname=""jane"" lastname=""doe"">
                    <contactdetails>
                      <emailaddress>jane@unknown.com</emailaddress>
                      <phonenumber>001122334455</phonenumber>
                    </contactdetails>
                  </person>
                </people>";

using (StringReader stringReader = new StringReader(xml))
{
    using (XmlReader xmlReader = XmlReader.Create(stringReader,
        new XmlReaderSettings() { IgnoreWhitespace = true }))
    {
        xmlReader.MoveToContent();
        xmlReader.ReadStartElement("People");

        string firstName = xmlReader.GetAttribute("firstName");
        string lastName = xmlReader.GetAttribute("lastName");

        Console.WriteLine("Person: {0} {1}", firstName, lastName);
        xmlReader.ReadStartElement("Person");

        Console.WriteLine("ContactDetails");

        xmlReader.ReadStartElement("ContactDetails");
        string emailAddress = xmlReader.ReadString();

        Console.WriteLine("Email address: {0}", emailAddress);
    }
}
```

如你所见，`XmlReader` 将 XML 视为层次化的节点结构。这比将 XML 视为扁平文件要容易。通过移动到节点、子节点和属性，你可以解析文档以获取所需的内容。

## XmlWriter

当你想要创建一个 XML 文件时，可以使用 `XmlWriter` 类。该类通过使用静态 `Create` 方法创建，并可以使用 `XmlWriterSettings` 类的实例进行配置。示例 4-44 展示了如何创建一个新的 XML 文件。如你所见，你有用于写入单个元素和属性的方法。

示例 4-44. 使用 `XmlWriter` 创建 XML 文件

```
StringWriter stream = new StringWriter();

using (XmlWriter writer = XmlWriter.Create(
    stream, 
    new XmlWriterSettings() { Indent = true }))
{
    writer.WriteStartDocument();
    writer.WriteStartElement("People");
    writer.WriteStartElement("Person");
    writer.WriteAttributeString("firstName", "John");
    writer.WriteAttributeString("lastName", "Doe");
    writer.WriteStartElement("ContactDetails");
    writer.WriteElementString("EmailAddress", "john@unknown.com");
    writer.WriteEndElement();
    writer.WriteEndElement();
    writer.Flush();
}

Console.WriteLine(stream.ToString());
```

与 `XmlReader` 类一样，`XmlWriter` 类也能感知 XML 的层次结构。然而，你需要确保同时写出每个元素的起始标签和结束标签。你可以选择添加属性，或者添加带有字符串值作为其内容的元素。

### XmlDocument

尽管 `XmlReader` 和 `XmlWriter` 是最快的选项，但它们绝对不是最容易使用的。当你处理相对较小的文档且对性能要求不是那么高时，可以使用 `XmlDocument` 类。它的主要功能允许你编辑 XML 文件，它在内存中以层次化的方式表示 XML，并允许你轻松地导航文档并就地编辑元素。完成文档编辑后，你可以将其保存回文件或流。

`XmlDocument` 使用一组 `XmlNode` 对象来表示组成文档各种元素。`XmlDocument` 继承自 `XmlNode` 并添加了加载和保存特定特定功能。`XmlNode` 帮助你读取内容和属性，并提供了添加子节点的方法，以便你轻松地构建文档结构。示例 4-45 展示了一个示例，在该示例中`XmlDocument` 的读取和编辑能力被用于 示例 4-43 中的 XML。

示例 4-45. 使用 `XmlDocument`

```
XmlDocument doc = new XmlDocument();

doc.LoadXml(xml);

// 输出文档中人的姓名
foreach (XmlNode node in doc.GetElementsByTagName("Person"))
{
    string firstName = node.Attributes["firstName"].Value;
    string lastName = node.Attributes["lastName"].Value;
    Console.WriteLine("Name: {0} {1}", firstName, lastName);
}

// 开始创建一个新节点
XmlNode newNode = doc.CreateNode(XmlNodeType.Element, "Person", "");

XmlAttribute firstNameAttribute = doc.CreateAttribute("firstName");
firstNameAttribute.Value = "Foo";

XmlAttribute lastNameAttribute = doc.CreateAttribute("lastName");
lastNameAttribute.Value = "Bar";

newNode.Attributes.Append(firstNameAttribute);
newNode.Attributes.Append(lastNameAttribute);

doc.DocumentElement.AppendChild(newNode);

Console.WriteLine("Modified xml...");

// Displays:
//Name: john doe
//Name: jane doe
//Modified xml...
//<?xml version="1.0" encoding="utf-8"?>
//<people>
//  <person firstname="john" lastname="doe">
//    <contactdetails>
//      <emailaddress>john@unknown.com</emailaddress>
//    </contactdetails>
//  </person>
//  <person firstname="jane" lastname="doe">
//    <contactdetails>
//      <emailaddress>jane@unknown.com</emailaddress>
//      <phonenumber>001122334455</phonenumber>
//    </contactdetails>
//  </person>
//  <person firstname="Foo" lastname="Bar" />
//</people>
```

遍历文档的一种巧妙功能是 `XPath`，它是用于 XML 文档的查询语言。`XmlDocument` 实现了 `IXPathNavigable` 接口，因此你可以从中获取 `XPathNavigator` 对象。`XPathNavigator` 提供了导航文档的简单方法。你可以使用与 `XmlDocument` 的方法从一个节点移动到另一个节点，或者使用 XPath 查询。这允许你选择具有特定值的元素或属性，类似于 SQL 在数据库中选择数据。示例 4-46 展示了如何使用 XPath 查询按姓名选择 `Person` 的示例。

示例 4-46. 使用 XPath 查询

```
XmlDocument doc = new XmlDocument();
doc.LoadXml(xml); // 可以在列表 4-43 中找到

XPathNavigator nav = doc.CreateNavigator();
string query = "//People/Person[@firstName='Jane']";
XPathNodeIterator iterator = nav.Select(query);

Console.WriteLine(iterator.Count); // 显示 1

while(iterator.MoveNext())
{
    string firstName = iterator.Current.GetAttribute("firstName","");
    string lastName = iterator.Current.GetAttribute("lastName","");
    Console.WriteLine("Name: {0} {1}", firstName, lastName);
}
```





另一种被许多 Web 服务使用的流行格式是 JavaScript 对象表示（JSON）。虽然 XML 很有用，但它非常冗长，并且关于文档结构有许多规则。JSON 被称为 XML 的“无脂肪版”替代方案。它的语法更简单，而且通常携带的重量要轻得多。示例 4-47 中的示例展示了如何使用 JSON 表示之前示例中的 `People` XML。

```
{
  "People": {
    "Person": [
      {
        "firstName": "John",
        "lastName": "Doe",
        "ContactDetails": { "EmailAddress": "john@unknown.com" }
      },
      {
        "firstName": "Jane",
        "lastName": "Doe",
        "ContactDetails": {
          "EmailAddress": "jane@unknown.com",
          "PhoneNumber": "001122334455"
        }
      }
    ]
  }
}
```

在使用 XML 时，你会使用如 `XmlWriter`、`XmlReader` 和 `XmlDocument` 等类；而 JSON 没有此类的类。通常，在处理 JSON 时，你会使用一个序列化库来帮助你将对象转换为 JSON，反之亦然。其中一个流行的库是 `Newtonsoft.Json`，可以在 *[`json.codeplex.com/`](http://json.codeplex.com/)* 获取。JSON 最常用于异步 JavaScript 和 XML (AJAX) 场景。实际上，AJAX 应该被称为 AJAJ，因为现在用 JSON 替换了 XML。AJAX 是一种允许网站向 Web 服务器执行后台调用的技术。这种技术使网站无需完全刷新页面即可进行更新。JSON 对此特别有用，因为所有 JavaScript 引擎都能通过一个相对简单的命令将 JSON 字符串解析为对象。

### 更多信息：序列化 JSON

关于序列化 JSON 的更多信息，请参阅本章节后面的目标 4.4 节，“序列化和反序列化数据”。

## 思考实验

#### 数据交换

你正在设计一个新的应用程序，用于存储全球天气状况的数据。你的业务模型依赖于将这些数据卖给客户，以便他们自己的应用程序中使用。你使用关系型数据库来存储数据，并通过授权用户可以访问的 Web 服务来访问数据。你还为想要数据本地副本的用户创建定期的 XML 导出文件。

1. 使用实体框架（Entity Framework）的优缺点是什么？
2. 你计划为你的 Web 服务使用哪些技术？
3. 你将如何以 XML 形式公开你的数据？

## 目标总结

* ADO.NET 使用程序模型，让你连接到不同类型的数据库。
* 你使用 `DbConnection` 对象创建到数据库的连接。
* 你可以执行查询来创建、更新、读取和删除（CRUD）数据库中的数据。
* 创建查询时，使用参数化查询很重要，这样可以避免 SQL 注入。
* 你可以通过为 Web 服务创建代理来从应用程序中消费它。
* 你可以通过 `XmlReader`、`XmlWriter`、`XPathNavigator` 和 `XmlDocument` 类来处理 XML。

### 目标回顾

回答以下问题以测试你对本目标信息的掌握情况。你可以在本章节末尾的答案 部分找到这些问题的答案以及对每个选项为何正确或错误的解释。

1. 你想要更新数据库中的特定行。你应该使用哪些对象？（选择所有适用项。）
   1. `SqlCommand`
   2. `SqlDataReader`
   3. `SqlConnection`
   4. `TransactionScope`
2. 你计划构建一个将使用面向对象设计的应用程序。它将被多个用户同时使用。你应该使用哪种技术？
   1. XML 文件
   2. 实体框架
   3. ADO.NET
   4. Web 服务
3. 你需要在计划服务中处理大量 XML 文件以提取某些数据。你应该使用哪个类？
   1. `XmlReader`
   2. `XmlDocument`
   3. `XmlWriter`
   4. `FileStream`

## 目标 4.3：使用 LINQ 查询和操作数据及对象

在 .NET 3.5 中，C# 增加了一个新功能：LINQ。LINQ 让你以极其强大的方式处理数据。它由一组标准的、易于学习的模式组成，让你能够查询数据。妙之处在于，LINQ 可以被扩展以处理不同类型的数据。这让你能够编写出易于理解和维护的强大查询。

本目标涵盖了如何：
* 使用标准的 LINQ 算符。
* 以最优方式使用 LINQ。
* 使用 LINQ to XML。

## 使 LINQ 取可能的语言特性

为了支持 LINQ，C# 增加了一些语言特性。这些特性本身是有用的，但当它们组合成 LINQ 时，它们就大放异彩。这些语言特性中的某些可以帮助你以优雅的方式构建查询，但其他特性有时即使为了能够创建查询也是强制性的。

这些语言构造结构如下：
* 隐式类型变量
* 对象初始化语法
* Lambda 表达式
* 扩展方法
* 匿名类型

### 隐式类型变量

在处理 C# 时，大多数时候你使用静态类型。这意味着编译器知道变量的类型，并看到你是否正确使用它。

例如，以下代码会导致编译错误：

```
int i = 42;
Stream m = new MemoryStream();
string s = i + m; // 这一行编译错误
```

你在这里看到的是显式类型。你告诉编译器变量的类型。在 C# 3 中引入了一个新特性：隐式类型。当使用隐式类型时，编译器会为你推断变量的类型，然后将其强类型为该类型。隐式类型变量只能用于局部变量。你可以通过使用 `var` 关键字使用隐式类型：

```
var i = 42;
var m = new MemoryStream();
//string s = i + m; // 这一行仍然编译错误
```

在这个代码中，编译器为你推断 `i` 的类型是 int，`m` 是 MemoryStream。类型仍然是强类型的，但你不需要指定类型。

为什么这在 LINQ 中是必要的？有时在用 LINQ 查询时，返回类型是在编译时确定的，因此你无法显式指定，因为你不知道。当你学习第一个 LINQ 查询时就会看到这样的例子。

除了在这些情况下是强制性的之外，隐式类型还可以提高代码的可读性。如果代码的用户可以很容易看到变量的类型，可以使用隐式类型来避免重复。在以下情况下，`var` 可以提高可读性：

```
Dictionary<string, IEnumerable<Tuple<Type, int>>> data = 
    new Dictionary<string, IEnumerable<Tuple<Type, int>>>();
var implicitData = new Dictionary<string, IEnumerable<Tuple<Type, int>>>();
```

在这种情况下，你避免了大型类型声明的重复。代码读者会立即看到 `implicitData` 的类型是 Dictionary。当变量的类型不明确时，最好避免隐式类型：

```sharp
var whatsMyType = GetData();
```

在这种情况下，代码读者将不得不检查 `GetData()` 方法或使用 Visual Studio 中的智能提示来查看 `whatsMyType` 的类型。

### 对象初始化语法

在 C# 增加对象初始化器之前，你必须将创建新对象和设置其属性分开，如示例 4-48 所示。

示例 4-48. 创建并初始化对象





```sharp
public class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
}

// 创建并初始化新对象
Person p = new Person();
p.FirstName = "John";
p.LastName = "Doe";
```

新的对象初始化语法允许你在一条语句中组合创建新对象和设置其属性。示例 4-49 展示了这种新语法。

示例 4-49. 使用对象初始化器

```sharp
// 一步到位创建并初始化新对象
Person p = new Person
{ 
    FirstName ="John",
    LastName = "Doe"
};
```

虽然不是严格必要的，但在使用对象初始化器时，它可以提高你代码的可读性（参见 示例 4-50）。在创建集合时也可以使用相同的语法。

示例 4-50. 使用集合初始化器

```sharp
var people = new List<Person>
{
    new Person
    {
        FirstName = "John",
        LastName = "Doe"
    },  
    new Person
    {
        FirstName = "Jane",
        LastName = "Doe"
    }
};
```

大多数情况下，对象初始化语法是一种很好用的语法糖，但在处理匿名类型时，它是实际上强制的。通过使用对象初始化语法，你定义了匿名类型所拥有的属性。

### Lambda 表达式

要理解 Lambda 表达式是什么，首先了解什么是匿名方法是非常重要的。匿名方法是在 C# 2.0 中引入的，允许你在某些代码中内联创建一个方法，将其赋值给变量并进行传递。示例 4-51 展示了如何创建匿名方法。

示例 4-51. 使用匿名方法

```csharp
Func<int, int> myDelegate =
    delegate(int x)
    {
        return x * 2;
    };
Console.WriteLine(myDelegate(21)); // 显示 42
```

`Func<T,T>` 是 .NET Framework 内置类型之一。它是接收一个 `int` 并返回一个 `int` 的委托简写表示。你也可以使用 `Action<...>` 来指定没有返回值的委托。

`Lambdas` 为创建匿名函数引入了简写表示。使用 lambda 可以编写相同的代码：

```sharp
Func<int, int> myDelegate = x => x * 2;
Console.WriteLine(myDelegate(21)); // 显示 42
```

如你所示，结果是相同的，但表示法要短得多。Lambda 使用特殊的 `=>` 符号，你可以将其读为“变为”或“对于……”。在处理 LINQ 工作时，你通常需要向方法传递一个 `Func<>` 委托。通过使用 lambda，你可以简化代码并节省大量的打字时间。当你处理多个参数或 lambda 包含多个语句时，语法会变得稍微冗长一些，但仍然比使用匿名方法要紧凑得多。

### 扩展方法

`扩展方法` 可用于在不使用继承的情况下为现有类型扩展新行为。扩展方法定义在静态类中，并使用特殊的 `this` 关键字将自己标记为扩展方法。示例 4-52 展示了如何为 `int` 创建扩展方法。

示例 4-52. 使用扩展方法

```csharp
public static class IntExtensions
{
    public static int Multiply(this int x, int y)
    {
        return x * y;
    }
}

int x = 2;
Console.WriteLine(x.Multiply(3)); // 显示 6
```

LINQ 完全基于扩展方法。它们定义在 `System.Linq.Enumerables` 类中，并允许你在所有可枚举类型上调用 LINQ 函数。

### 更多信息：扩展方法

有关扩展方法的更多信息，请参见 第 2 章。

### 匿名类型

当你创建`匿名类型`时，你同时使用了对象初始化器和隐式类型。匿名类型是一种在编译时确定形状但没有正式类定义的类型。编译器通过为你创建一个类型并通重写 `System.Object` 的虚成员来提供默认实现从而帮助你。

你通过使用 `var` 关键字作为类型并在不指定类型的情况下使用 `new` 运算符来创建匿名类型，如示例 4-53 所示。

示例 4-53. 创建匿名类型

```csharp
var person = new
{
    FirstName = "John",
    LastName = "Doe"
};

Console.WriteLine(person.GetType().Name); // 显示 "<>f__AnonymousType0`2"
```

在这里你可以看到 `person.GetType().Name` 是如何工作的。（此处省略了原文中重复的说明文字）。

`对象初始化器`可用于`匿名`类型。

## 使用 LINQ

在处理 LINQ 时（无论是在内存中、从数据库或其他其他地方），查询总是包含以下步骤：

1.  获取数据。
2.  创建查询。
3.  执行查询。示例 4-54 展示了一个来自数组的简单 LINQ 示例。

示例 4-54. 一个 LINQ 查询

```sharp
int[] data = { 1, 2, 5, 8, 11 };

var result = from d in data
             where d % 2
             select d;

foreach (int i in result)
{
    Console.WriteLine(i);
}
```

如你所示，结果是相同的，但表示法要短得多。Lambda 使用特殊的 `=>` 符号，你可以将其读为“变为”或“对于……”。在处理 LINQ 工作时，你通常需要向方法传递一个 `Func<>` 委托。通过使用 lambda，你可以简化代码并节省大量的打字时间。当你处理多个参数或 lambda 包含多个语句时，语法会变得稍微冗长一些，但仍然比使用匿名方法要紧凑得多。

### 标准 LINQ 查询运算符

LINQ 有一些处理数据时可以使用的标准查询运算符。LINQ 提供程序将你的查询映射到特定的数据存储，例如 LINQ to XML、LINQ to Entities 或 LINQ to Objects。鼓励每个 LINQ 提供程序实现标准查询运算符，以便你始终可以使用它们。这意味着你可以在所有数据源上使用这些标准运算符，提供一致的体验。

### 更多信息：LINQ 示例

有关使用所有 LINQ 运算符的示例，请参见 [`code.msdn.microsoft.com/101-LINQ-Samples-3fb9811`](http://code.msdn.microsoft.com/101-LINQ-Samples-3fb9811)。

标准查询运算符有：*All, Any, Average, Cast, Count, Distinct, GroupBy, Join, Max, Min, OrderBy, OrderByDescending, Select, SelectMany, Skip, SkipWhile, Sum, Take, Take-While, ThenBy, ThenByDescending* 以及 *Where*。

你可以创建的最基本的查询如示例 4-55 所示。

示例 4-55. LINQ *Select* 运算符

```sharp
int[] data = { 1, 2, 5, 8, 11 };
var result = from d in data 
             select d;
Console.WriteLine(string.Join(", ", result)); // 显示 1, 2, 5, 8, 11
```



在这种情况下，查询并没有执行任何特殊操作。你可以直接使用数据数组，它将产生相同的结果。然而，这个查询展示了 LINQ 是如何工作的。首先，你从一个 `from 语句` 开始，然后是一个数据源。这有助于编译器，因为现在它能立即知道你正在处理什么内容。正因如此，它可以在下一行提供 IntelliSense（智能感应）提示。这与你所习惯的普通 SQL 不同，在普通 SQL 中，你先从 `SELECT` 子句开始，然后是 `FROM` 子句。

现在，你可以通过添加过滤器让查询变得稍微有趣一点。这是通过添加 `where` 语句来实现的。该语句应该返回一个布尔值，表示该值是否应该包含在最终结果中。示例 4-56 展示了如何过滤列表以找到大于 5 的项。

### 示例 4-56. LINQ `where` 运算符

```csharp
int[] data = { 1, 2, 5, 8, 11 };
var result = from d in data
             where d > 5
             select d;
Console.WriteLine(string.Join(", ", result)); // 显示 8, 11
```

另一个有用的运算符是 `orderby`，它可以用于根据特定值对集合进行排序。你可以使用 `orderby` 按升序或降序对数据进行排序。示例 4-57 展示了如何按降序排序数据。

### 示例 4-57. LINQ `orderby` 运算符

```csharp
int[] data = { 1, 2, 5, 8, 11 };
var result = from d in data
             where d > 5
             orderby d descending
             select d;
Console.WriteLine(string.Join(", ", result)); // 显示 11, 8
```

你还可以组合来自多个源的数据。假设你有两个包含数字的数组，并且你想将它们相乘。在你的 LINQ 查询中，你使用多个 `from` 语句来合并数据，如 示例 4-58 所示。

### 示例 4-58. LINQ 多个 `from` 语句

```csharp
int[] data1 = { 1, 2, 5 };
int[] data2 = { 2, 4, 6};

var result = from d1 in data1
             from d2 in data2
             select d1 * d2;

Console.WriteLine(string.Join(", ", result)); // 显示 2, 4, 6, 4, 8, 12, 10, 20, 30
```

当你处理更有趣的类型时，LINQ 展示了它的威力。假设你正在处理一个 `Order` 类，该类包含一些指向 `Product` 的 `OrderLine` 对象（参见 示例 4-59）。

### 示例 4-59. 用于 LINQ 查询的示例 `Order` 类

```csharp
public class Product
{
    public string Description { get; set; }
    public decimal Price { get; set; }
}

public class OrderLine
{
    public int Amount { get; set; }
    public Product Product { get; set; }
}

public class Order
{
    public List<OrderLine> OrderLines { get; set; }
}
```

现在，假设你想知道一组 `Orders` 中 `OrderLines` 的平均数量。你可以使用 LINQ 查询轻松地计算此值：

```csharp
var averageNumberOfOrderLines = orders.Average(o => o.OrderLines.Count);
```

正如你所看到的，`Average` 方法没有查询语法，这就是为什么你需要使用方法语法。尝试在不使用 LINQ 的情况下编写这个查询。这难，但代码确实多很多。

其他有用的 LINQ 操作是 `projection`（投影）和 `grouping`（分组）。当使用 `projection` 时，你选择另一个类型或匿名类型作为查询的结果。你将结果投影到其中，以便只关注你真正需要的属性。当使用 `grouping` 时，你通过某个属性对数据进行分组，然后处理该结果。这很有用的一个例子是你想知道售出了每种 `product` 多少商品。你可以使用 示例 4-60 中的查询来进行。

### 示例 4-60. 使用 `group by` 和 `projection`

```csharp
var result = from o in orders
             from l in o.OrderLines
             group l by l.Product into p
             select new
                 {
                    Product = p.Key,
                    Amount = p.Sum(x => x.Amount)
                 };
```

另一个标准运算符是 `join` 运算符。`Join` 可用于合并来自两个或多个源的数据。当使用 `join` 时，如 示例 4-61 所示。

### 示例 4-61. 使用 `join`

```csharp
string[] popularNames = { "A", "B" };
var popularProducts = from p in products
                      join n in popularNames on p.Description equals n.Description
                      select p;
```

当你处理较大的数据集时，你可能想要实现分页（paging）。当使用分页时，你不会一次性向用户显示所有数据。相反，你每次加载一页。为了实现分页，你可以使用 `Skip` 和 `Take` 运算符。

```csharp
var pagedOrders = orders
                .Skip((pageIndex - 1) * pageSize)
                .Take(pageSize);
```




当你与其它针对数据库的 LINQ 提供程序工作时（例如 LINQ to Entities 或 LINQ to SQL），这一点尤为重要（像 LINQ to Entities 这样的 LINQ 提供程序会解析查询并将其转换为 SQL）。在迭代结果之前，查询不会发送到数据库。这意味着多次执行查询会多次访问数据库。因此，最好将查询结果保存在本地变量中，并在处理数据时使用该变量。

当你在调用诸如 `ToList` 的方法，或者在 `for each` 语句中对结果进行迭代时（这会调用迭代器上的 `MoveNext` 方法），就会发生迭代。当然，其他方法更为复杂，但它们都遵循相同的理念。

### 更多信息：Yield

有关 `yield` 和迭代器模式的更多信息，请参见第 2 章。

### 使用 LINQ to XML

.NET Framework 的另一个提供程序是 `LINQ to XML`。通常情况下，你通过 `XmlWriter`、`XmlReader` 和 `XmlDocument` 类来处理 XML 文件。LINQ to XML 的优势在于，你可以使用与 LINQ to Objects 或其它 LINQ 提供程序相同的查询体验。

LINQ to XML 帮助你创建、编辑和解析 XML 文件。如果你只需要从 XML 文件中获取某些信息，LINQ to XML 为你提供了简单的查询体验。如果你需要更强大的功能，LINQ 可以帮助你编写比其他 XML 类更简洁的强大查询。

#### 查询 XML

如果你想用 LINQ to XML 查询 XML 文件，可以使用 `XDocument` 类将文件或包含 XML 的字符串加载到内存中。`XDocument` 类与 `XNode` 类型的对象配合工作。`XNode` 是一个抽象类，代表文档中持有的某些内容片段。你可以使用 `XDocument.Nodes` 访问构成 XML 文件的节点，或者使用 `XDocument.Descendants` 或 `XDocument.Elements` 搜索特定的节点集。`XDocument` 类的一个非常棒的功能是它以层级化的方式表示 XML 文件。因此，你可以从一个节点移动到子节点，再回到父节点。属性不被视为节点；相反，它们是属于节点的键值对。

示例 4-64 显示了一些包含一组人的示例 XML，这些人每个人都具有某些属性和联系方式。

示例 4-64. 示例 XML

```
String xml = @"<?xml version=""1.0"" encoding=""utf-8"" ?>
                    <people>
                      <person firstname=""john"" lastname=""doe"">
                        <contactdetails>
                          <emailaddress>john@unknown.com</emailaddress>
                        </contactdetails>
                      </person>
                      <person firstname=""jane"" lastname=""doe"">
                        <contactdetails>
                          <emailaddress>jane@unknown.com</emailaddress>
                          <phonenumber>001122334455</phonenumber>
                        </contactdetails>
                      </person>
                    </people>";
```

你可以使用 LINQ to XML 执行从 XML 字符串中加载人员姓的查询。要使用 LINQ to XML，你必须添加 `System.Xml.Linq` 命名空间的引用。示例 4-65 显示了你如何使用 `Descendants` 方法和 `Attribute` 方法来加载这些数据。

示例 4-65. 使用 LINQ to XML 查询某些 XML

```
XDocument doc = XDocument.Parse(xml);
IEnumerable<string> personNames = from p in doc.Descendants("Person")
                                  select (string)p.Attribute("firstName") 
                                     + " " + (string)p.Attribute("lastName");
foreach (string s in personNames)
{
    Console.WriteLine(s);
}

// 显示:
// John Doe
// Jane Doe
```

需要注意的是，`Attribute` 方法返回 `XAttribute` 实例。`XAttribute` 具有类型为字符串的 `Value` 属性，但它也实现了显式转换运算符，因此你可以将其转换为 C# 中的大多数基本类型。

### 更多信息：显式强制转换运算符

有关显式强制转换运算符的更多信息，请参见第 2 章。

由于 LINQ to XML 支持标准的 LINQ 运算符，你可以轻松在 XML 查询中使用如 `Where` 和 `OrderBy` 等运算符。示例 4-66 显示了你如何过滤所有人员，仅保留有电话号码的人，然后按字母顺序选择他们的全名。你还看到了如何轻松地混合使用方法语法和查询语法。

示例 4-66. 在 LINQ to XML 查询中使用 `Where` 和 `OrderBy`

```
XDocument doc = XDocument.Parse(xml);
IEnumerable<string> personNames = from p in doc.Descendants("Person")
                                  where p.Descendants("PhoneNumber").Any()
                                  select (string)p.Attribute("firstName")
                                              + " " + (string)p.Attribute("lastName");
```

### 创建 XML

除了查询 XML，LINQ to XML 还可以以很好的方式帮助你创建 XML。你使用 `XElement` 来创建你的 XML。你使用接收对象数组的 `XElement` 构造函数。示例 4-67 显示了创建某些 XML 的示例。

示例 4-67. 使用 `XElement` 创建 XML

```
XElement root = new XElement("Root",
            new List<XElement>
            {
                new XElement("Child1"),
                new XElement("Child2"),
                new XElement("Child3")
            },
            new XAttribute("MyAttribute", 42));
root.Save("test.xml");

// 输出:
//<Root MyAttribute="42">
//    <Child1 />
//    <Child2 />
//    <Child3 />
//</Root>

### 更新 XML

当你想要修改 XML 时，通常将其加载到内存中，通过删除和插入节点或更改现有节点来修改 XML。完成后，将 XML 保存回文件。

LINQ to XML 使用另一种称为*函数式构造*的方法。函数式构造将修改数据视为转换问题，而不是详细的数据操作。转换可能会消耗更多的处理器资源，但它更容易编写和维护，在大多数情况下，这些收益远大于成本。

假设你正在处理示例 4-64 中的 XML，并且需要为 *Joe* 添加电话号码，并为所有人添加 *IsMale* 属性。

你可以使用过程化代码来完成此，如示例 4-68 所示。

示例 4-68. 过程化的更新 XML

```
XElement root = XElement.Parse(xml);

foreach (XElement p in root.Descendants("Person"))
{
    string name = (string)p.Attribute("firstName") + (string)p.Attribute("lastName");
    p.Add(new XAttribute("IsMale", name.Contains("John")));
    XElement contactDetails = p.Element("ContactDetails");
    if (!contactDetails.Descendants("PhoneNumber").Any())
    {
        contactDetails.Add(new XElement("PhoneNumber", "001122334455"));
    }
}
```




你可以使用函数式构造通过 LINQ to XML 查询将此树转换为新树，并添加添加新的属性和元素。示例 4-69 展示了如何实现。

示例 4-69. 使用函数式创建转换 XML

```
XElement root = XElement.Parse(xml);

XElement newTree = new XElement("People",
    from p in root.Descendants("Person")
    let name = (string)p.Attribute("firstName") + (string)p.Attribute("lastName")
    let contactDetails = p.Element("ContactDetails")
    select new XElement("Person",
        new XAttribute("IsMale", name.Contains("John")),
        p.Attributes(),
        new XElement("ContactDetails",
            contactDetails.Element("EmailAddress"),
            contactDetails.Element("PhoneNumber") 
                ?? new XElement("PhoneNumber", "112233455")
        )));
```

取决于你修改的难度，决定了是使用常规的过程方法还是函数式方法。特别是当 XML 文档结构发生变化时，函数式方法会有很多优势。

## 思考实验

### 切换到 LINQ

你正在开始一个新项目，你可以第一次使用 LINQ。你以前从未工作过 LINQ，但你自己在空闲学习了它，并看到了它的优点。

你看到了在项目中中使用 LINQ to Entities、LINQ to Objects 和 LINQ to XML 的可能性，并尝试在公司内部引入它们。

然而，你的一些同事有些疑问。LINQ 的速度足够快吗？它易于维护吗？我们需要使用方法语法还是查询语法？

尝试通过回答这些问题来帮助你的同事：

1. LINQ 是否存在性能问题？如果有，应该避免使用吗？
2. LINQ 易于维护吗？
3. 方法语法和查询语法之间有什么区别？应该使用哪一个？

## 目标总结

* `LINQ` 代表语言集成查询（Language Integrated Query），它是针对多个数据源编写查询的统一方式。
* 在处理 `LINQ` 查询时，重要的语言特性包括隐式类型、对象初始化语法、lambda 表达式、扩展方法和匿名类型。
* 你可以使用基于方法的语法和查询语法使用 `LINQ`。
* `LINQ` 查询是延迟执行的，这意味着查询在第一次被迭代时才会执行。
* 你可以使用 LINQ to XML 来查询、创建和更新 `XML`。

### 目标回顾

回答以下问题以测试你对本目标信息的掌握情况。你可以在章节末尾的 答案 部分找到这些问题的答案，以及对每个选项选择正确或错误的解释。

1. 你有一个日期列表。你想将日期过滤为当前年份，然后选择最高日期。你使用哪个查询？
    1. `DateTime result = dates.Where(d => d == DateTime.Now).OrderBy(d => d).First();`
    2. `DateTime result = dates.Where(d => d.Year == DateTime.Now.Year).OrderByDescending(d => d).FirstOrDefault();`
    3. `DateTime result = dates.Where(d => d.Year == DateTime.Now.Year).OrderByDescending(d => d).First();`
    4. `DateTime result = dates.Where(d => d.Year == DateTime.Now.Year).OrderByDescending(d => d).Single();`

2. 你正尝试使用 `LINQ` 查询，但你收到了编译错误，提示找不到 `Where` 方法。你应该怎么办？（选择所有适用项）
    1. 添加 `using System.Linq` 语句。
    2. 检查你使用的是实现了 `IEnumerable` 的类型。
    3. 将你的查询从查询语法更改为方法语法。
    4. 将你的查询类型更改为 `var`。

3. 你在使用以下 LINQ to Entities 查询：
```
var query = from p in myContext.Products
            where p.Price < 50
            select p;
int numberOfItems = query.Count();
var products = query.ToList();
```
你正面临性能问题。如何改进你的查询？（选择所有适用项）
    1. 避免多次访问数据库。
    2. 不要对查询执行 `ToList()`。
    3. 使用分页。
    4. 将查询更改为方法语法。

## 目标 4.4：数据的序列化与反序列化

在构建应用程序时，你经常与其他应用程序交换数据。在向 Web 服务或通过网络流发送数据时，你必须首先将数据转换为扁平化或二进制形式。当你接收数据时，你必须将扁平或二进制数据转换为你想要操作的对象。这个过程被称为序列化和反序列化。

本目标涵盖：
* 使用序列化和反序列化。
* 使用不同类型的序列化器。
* 为序列化配置你的对象。

## 使用序列化和反序列化

`序列`是将内存中的对象或对象图转换为字节流或文本的过程。反序列化是相反的。你获取一些字节或文本将其转换为对象。

当你需要与另一个应用程序交换数据时，使用序列化。这种交换可以通过网络进行，也可以在将数据存储到数据库或文件中进行。

序列化可能变成一个复杂的过程，特别是当你处理具有循环引用的对象图（即最后一个对象引用第一个对象）时。序列化对象并不是一项简单的任务。

另一个需要注意的是序列化只序列化对象存储的数据。方法不会被序列化。当你反序列化对象时，你需要原始类的定义。当你想要优化需要序列化的数据量，可以创建一个只包含特定数据的 `DTO`。

.NET Framework 提供了帮助序列化对象的类，可以在 `System.Runtime.Serialization` 和 `System.Xml.Serialization` 命名空间中找到。这些类可以帮助你序列化和反序列化对象，还可以配置对象以便进行序列化。

.NET Framework 提供了你可以默认使用的序列化机制：
* `XmlSerializer`
* `DataContractSerializer`
* `BinaryFormatter`

### 使用 `XmlSerializer`

`XmlSerializer` 的设计是为了是为了简单对象访问协议（SOAP）消息。SOAP 是一种与 Web 服务交换信息的协议。它使用 `XML` 作为消息格式。`XML` 人机均可读，并且独立于它使用的环境。

`XmlSerializer` 与你的对象松耦合。如果你在对象中添加了新属性或方法，`XmlSerializer` 不会注意到。通过简单的配置更改，你可以将 `XML` 节点映射到对象的属性，从而使两者都能独立修改。但 `XmlSerializer` 的性能最高；它也不会维护你拥有的对象引用，并且无法处理私有字段。

在使用 `XmlSerializer` 时，重要的是为你的类型标记 `[Serializable]` 特性，该特性属于 `SerializableAttribute` 类。这告知 .NET Framework 你的类型应该是可序列化的。它会检查你的对象以及它引用的所有对象，以确保可以序列化整个图。如果不可能，将在运行时得到异常。





示例 4-70 展示了如何序列化对象并从 XML 恢复它的示例。如你所见，`Person` 类标记为 `Serializable`。如果该类型的成员未被排除，则所有成员都将被自动序列化。

### 示例 4-70. 使用 `XmlSerializer` 序列化对象

```sharp
[Serializable]
public class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
    public int Age { get; set; }
}

XmlSerializer serializer = new XmlSerializer(typeof(Person));
string xml;
using (StringWriter stringWriter = new StringWriter())
{
    Person p = new Person
    {
        FirstName = "John",
        LastName = "Doe",
        Age = 42
    };
    serializer.Serialize(stringWriter, p);
    xml = stringWriter.ToString();
}

Console.WriteLine(xml);

using (StringReader stringReader = new StringReader(xml))
{
    Person p = (Person)serializer.Deserialize(stringReader);
    Console.WriteLine("{0} {1} is {2} years old", p.FirstName, p.LastName, p.Age);
}

// Displays
//<?xml version="1.0" encoding="utf-16"?>
//<Person xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
// xmlns:xsd="http://www.w3.org/2001/XMLSchema">
//  <FirstName>John</FirstName>
//  <LastName>Doe</LastName>
//  <Age>42</Age>
//</Person>
//John Doe is 42 years old
```

你可以通过特性来配置 `XmlSerializer` 如何序列化你的类型。这些特性定义在 `System.Xml.Serialization` 命名空间中。以下是你经常会使用的重要特性：

* `XmlIgnore`
* `XmlAttribute`
* `XmlElement`
* `XmlArray`
* `XmlArrayItem`

默认情况下，每个成员都被序列化为 `XmlElement`。这意味着它们最终成为 XML 中的节点。通过使用 `XmlAttribute`，你可以将成员映射到其父节点上的属性。`XmlIgnore` 可以确保某个元素不被序列化。在序列化集合时使用 `XmlArray` 和 `XmlArrayItem`。示例 4-71 展示了一个使用了这些特性的示例。

### 示例 4-71. 使用 XML 特性配置序列化

```sharp
[Serializable]
public class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
    public int Age { get; set; }
}

[Serializable]
public class Order
{
    [XmlAttribute]
    public int ID { get; set; }

    [XmlIgnore]
    public bool IsDirty { get; set; }

    [XmlArray("Lines")]
    [XmlArrayItem("OrderLine")]
    public List<OrderLine> OrderLines { get; set; }
}

[Serializable]
public class VIPOrder : Order
{
    public string Description { get; set; }
}

[Serializable]
public class OrderLine
{
    [XmlAttribute]
    public int ID { get; set; }

    [XmlAttribute]
    public int Amount { get; set; }

    [XmlElement("OrderedProduct")]
    public Product Product { get; set; }
}

[Serializable]
public class Product
{
    [XmlAttribute]
    public int ID { get; set; }
    public decimal Price { get; set; }
    public string Description { get; set; }
}
```

当你序列化这段代码时，必须确保 .NET Framework 知道你正在使用继承层次结构。示例 4-72 展示了一个 `VIPOrder` 示例以及你如何序列化和反序列化它。

### 示例 4-72. 将派生复杂类序列化为 XML

```sharp
private static Order CreateOrder()
{
    Product p1 = new Product { ID = 1, Description = "p2", Price = 9 };
    Product p2 = new Product { ID = 2, Description = "p3", Price = 6 };

    Order order = new VIPOrder
    {
        ID = 4,
        Description = "Order for John Doe. Use the nice giftwrap",
        OrderLines = new List<OrderLine>
        { 
            new OrderLine { ID = 5, Amount = 1, Product = p1},
            new OrderLine { ID = 6 ,Amount = 10, Product = p2},
        }
    };

    return order;
}

XmlSerializer serializer = new XmlSerializer(typeof(Order), 
   new Type[] { typeof(VIPOrder) });
string xml;
using (StringWriter stringWriter = new StringWriter())
{
    serializer.Serialize(stringWriter, order);
    xml = stringWriter.ToString();
}
```

## 使用二进制序列化

## 二进制序列化

二进制序列化会创建一个紧凑的字节流。与 XML 序列化相比，不同点在于私有字段默认会被序列化。另一个点是，在反序列化期间，不会执行构造函数。在处理二进制序列化时，你必须考虑到这一点。

与 `XmlSerializer` 一样，你可以防止字段被序列化。你通过使用 `[NonSerialized]` 特性来实现这一点。假设你不想序列化 `Person` 类中的 `IsDirty` 字段。你可以通过 示例 4-74 中的代码来实现这一点。

```sharp
[Serializable]
public class Person
{
    public int Id { get; set; }
    public string Name { get; set; }

    [NonSerialized]
    private bool isDirty = false;
}
```

二进制序列化比 XML 序列化更严格。当 XML 序列化器找不到特定字段时，它不会抛出异常；它只会将属性设置为默认值。二进制序列化器没有那么宽容。因此，能够影响序列化过程是非常关重要的。你可以使用 `OptionalFieldAttribute` 来确保二进制序列化器知道某个字段是在后续版本中添加的，例如早期的序列化对象不包含此字段。

你可以在四个特定的阶段影响序列化和反序列化过程，即在操作开始和结束时阶段。你可以通过使用以下四个特性来实现这一点：

* `OnDeserializedAttribute`
* `OnDeserializingAttribute`
* `OnSerializedAttribute`
* `OnSerializingAttribute`





你将这些属性添加到类内部的方法中，这些方法接收一个 `StreamingContext` 作为参数。示例 4-75 展示了你如何向 `Person` 类添加这些方法。

示例 4-75. 影响序列化与反序列化

```java
[Serializable]
public class Person
{
    public int Id { get; set; }
    public string Name { get; set; }

    [NonSerialized]
    private bool isDirty = false;

    [OnSerializing()]
    internal void OnSerializingMethod(StreamingContext context)
    {
        Console.WriteLine("OnSerializing.");
    }

    [OnSerialized()]
    internal void OnSerializedMethod(StreamingContext context)
    {
        Console.WriteLine("OnSerialized.");
    }

    [OnDeserializing()]
    internal void OnDeserializingMethod(StreamingContext context)
    {
        Console.WriteLine("OnDeserializing.");
    }

    [OnDeserialized()]
    internal void OnDeserializedMethod(StreamingContext context)
    {
        Console.WriteLine("OnSerialized.");
    }
}
```

当序列化和反序列化 `Person` 对象时，你将获得以下输出：

```
OnSerializing..
OnSerialized..
OnDeserializing..
OnSerialized..
```

需要记住的一点是，序列化对象可能会暴露对安全敏感的私有数据。任何有权限反序列化该文件的人都可以访问你的敏感数据。如果你有一个敏感类，应该实现 `ISerializable` 接口。在实现此接口时，你对哪些值被序列化拥有控制权。你可以选择不序列化敏感数据，或者可能在序列化之前进行加密。示例 4-76 展示了如何实现此接口。

示例 4-76. 实现 `ISerializable`

```java
[Serializable]
public class PersonComplex : ISerializable
{
    public int Id { get; set; }
    public string Name { get; set; }
    private bool isDirty = false;

    public PersonComplex() { }
    protected PersonComplex(SerializationInfo info, StreamingContext context)
    {
        Id = info.GetInt32("Value1");
        Name = info.GetString("Value2");
        isDirty = info.GetBoolean("Value3");
    }

    [System.Security.Permissions.SecurityPermission(SecurityAction.Demand, 
                                                    SerializationFormatter = true)]
    public void GetObjectData(SerializationInfo info, StreamingContext context)
    {
        info.AddValue("Value1", Id);
        info.AddValue("Value2", Name);
        info.AddValue("Value3", isDirty);
    }
}
```

如你所示，实现 `ISerializable` 包含两个重要部分。第一个是 `GetObjectData` 方法。该方法在对象被序列化时被调用。它应该将你想序列化的值作为键值对添加到传递给方法的 `SerializationInfo` 对象中。重要的一点是，你应该用 `SecurityPermission` 属性标记此方法（你可以在 `System.Security.Permissions` 命名空间中找到此属性），以便允许执行序列化和反序列化代码。

另一个重要步骤是添加一个特殊的保护构造函数，它接收 `SerializationInfo` 和 `StreamingContext`。该构造函数在反序列化期间被调用，你用它来检索值并初始化你的对象。如你所示，你可以自由选择添加到 `SerializationInfo` 中的值的名称。

在构造函数中实现安全检查是非常重要的。通过这样，你可以确保没有人篡改序列化数据。

## 使用 `DataContract`

你现在已经了解了 XML 和二进制序列化。当你使用 WCF 时，会使用另一种类型的序列化。当你的类型被 WCF 使用时，它们会被序列化以便发送到其他应用程序。WCF 使用 `Data Contract Serializer` 将你的对象序列化为 XML 或 JSON。

最明显的区别是你可以使用 `DataContractAttribute` 而不是 `SerializableAttribute`。另一个重要区别是成员默认不会被序列化。你必须显式地用 `DataMember` 属性标记它们。

与二进制序列化一样，你可以使用 `OnDeserializedAttribute`、`OnDeserializingAttribute`、`OnSerializedAttribute` 和 `OnSerializingAttribute` 来配置序列化和反序列化过程的四个阶段。

示例 4-77 展示了你如何为 `Person` 类创建一个 `DataContract`。`isDirty` 字段被忽略，`Id` 和 `Name` 属性都将被序列化。

示例 4-77. 使用 `DataContract`

```java
[DataContract]
public class PersonDataContract
{
    [DataMember]
    public int Id { get; set; }

    [DataMember]
    public string Name { get; set; }

    private bool isDirty = false;
}
```

你可以像使用 `XmlSerializer` 和 `BinarySerializer` 一样，使用 `System.Runtime.Serialization` 命名空间下的 `DataContractSerializer`。在序列化或反序列化时，你需要为输入或输出指定 `Stream`。示例 4-78 展示了一个示例。

示例 4-78. 使用 `DataContract`

```java
PersonDataContract p = new PersonDataContract
{
    Id = 1,
    Name = "John Doe"
};

using (Stream stream = new FileStream("data.xml", FileMode.Create))
{
    DataContractSerializer ser = new DataContractSerializer(typeof(PersonDataContract));
    ser.WriteObject(stream, p);
}

using (Stream stream = new FileStream("data.xml", FileMode.Open))
{
    DataContractSerializer ser = new DataContractSerializer(typeof(PersonDataContract));
    PersonDataContract result = (PersonDataContract)ser.ReadObject(stream);
}
```

## 使用 JSON 序列化

JSON 是一种特殊格式，当通过异步 JavaScript 和 XML (AJAX) 在 Web 服务器和客户端之间发送少量数据时特别有用。通常，当你使用 WCF 端点或 ASP.NET WebApi 时，你的数据会自动为你进行序列化。当你想要手动执行此序列化时，可以使用 `DataContractJsonSerializer`。示例 4-79 展示了如何手动序列化对象。

示例 4-79. 使用 `DataContractJsonSerializer`

```java
[DataContract]
public class Person
{
    [DataMember]
    public int Id { get; set; }
    [DataMember]
    public string Name { get; set; }
}

Person p = new Person
{
    Id = 1,
    Name = "John Doe"
};

using (MemoryStream stream = new MemoryStream())
{
    DataContractJsonSerializer ser = new DataContractJsonSerializer(typeof(Person));
    ser.WriteObject(stream, p);

    stream.Position = 0;
    StreamReader streamReader = new StreamReader(stream);
    Console.WriteLine(streamReader.ReadToEnd()); // 显示 {"Id":1,"Name":"John Doe"}

    stream.Position = 0;
    Person result = (Person)ser.ReadObject(stream);
}
```

## 思考

**选择正确的序列化**

你需要将数据序列化到文件中。该文件可以由另一个 .NET 处理。你的数据由个人记录组成，存储名称、地址、登录凭据和联系方式等重要信息。

你正在考虑哪种序列化最好。你考虑了 XML 二进制、JSON 或使用 Data Contract。

1.  你应该将数据序列化为哪种格式？

2.  你应该使用哪种序列化器？

3.  你的类型是否需要实现任何特定的序列化方法？

## 目标总结

*   序列化是将对象转换为扁平文件或字节流的过程。





*   反序列化（Deserialization）将一系列字节或一个扁平文件转换为一个对象。
*   可以使用 `XmlSerializer` 完成 XML 序列化。
*   你可以使用特殊属性来配置 `XmlSerializer`。
*   可以使用 `BinaryFormatter` 类完成二进制序列化。
*   WCF 使用另一种类型的序列化，由 `DataContractSerializer` 执行。
*   JSON 是一种紧凑的文本格式，可以通过使用 `DataContractJsonSerializer` 来创建。

## 目标复习

回答以下问题以测试你对本目标中信息的掌握程度。你可以在章节末尾的答案部分找到这些问题的答案，以及对每个备选答案正确或错误的解释。

1. 你需要存储大量数据，并希望以最优化的方式进行操作。你应该使用哪种序列化器？

    1. `XmlSerializer`
    2. `BinaryFormatter`
    3. `DataContractSerializer`
    4. `DataContractJsonSerializer`

2. 你正在将某些敏感数据序列化为二进制格式。你应该使用什么？（选择适用项。）

    1. `XmlSerializer`
    2. `ISerializable`
    3. `DataContractSerializer`
    4. `BinaryFormatter`

3. 你想将某些数据序列化为 XML，并确保某个属性不被序列化。你应该使用哪种属性？

    1. `XmlElement`
    2. `XmlAttribute`
    3. `XmlIgnore`
    4. `NonSerialized`

# 目标 4.5：在集合中存储和从集合中检索数据

当你处理一组数据时，通常会使用集合（Collection）。当你想要灵活地处理数据时，集合对象非常有用。你可能需要从集合中添加和删除元素，可能有特殊的性能需求，或者可能需要访问项。这就是为什么 .NET Framework 为你提供了大量的集合供你使用。

本目标涵盖了：

* 使用 .NET Framework 部分的集合。
* 选择使用哪种集合。
* 实现你自己的集合。

## 使用数组

你可以用于存储一组实体的最基本类型是 `array`（数组）。当你处理一组具有相同类型的固定数量对象时，数组非常有用。

你通过特殊语法声明数组：`type[] arrayName`。方括号表示该类型为数组。在创建数组时，你需要指定它将包含的项数。

示例 4-80 显示了如何声明数组、填充数组并对其进行迭代。

示例 4-80. 使用数组

```
int[] arrayOfInt = new int[10];

for (int x = 0; x < arrayOfInt.Length; x++)
{
    arrayOfInt[x] = x;
}

foreach (int i in arrayOfInt)
{
    Console.Write(i); // 显示 0123456789
}
```

如你所示，数组是固定大小创建的。数组是基于零的，这意味着第一个元素可以在索引 0 处找到，最后一个元素位于长度减 1 的处。你可以通过使用 `Length` 属性和 `for` 循环遍历数组。数组是继承自 `Array` 类的引用类型。数组实现了 `IEnumerable`，因此你可以在 `foreach` 循环中使用它。

数组也可以直接初始化。编译器随后将为你检查长度并创建一个适当数组。

```
int[] arrayOfInt = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 };
```

除了声明一维数组外，你还可以创建`multidimensional`（多维）数组和`jagged arrays`（交数组）。

例如，二维数组意味着数组具有特定数量的行和列。你通过在数组声明中使用逗号（`,`）来声明它。行和列的数量可以不同。示例 4-81 显示了如何声明二维数组。

示例 4-81. 使用二维数组

```
string[,] array2D = new string[3, 2] { { "one", "two" }, { "three", "four" },
                        { "five", "six" } };

Console.WriteLine(array2D[0, 0]); // one
Console.WriteLine(array2D[0, 1]); // two
Console.WriteLine(array2D[1, 0]); // three
Console.WriteLine(array2D[1, 1]); // four
Console.WriteLine(array2D[2, 0]); // five
Console.WriteLine(array2D[2, 1]); // six
```

`jagged array`（交数组）是一个元素为数组的数组。因为数组是引用类型，所以交数组的值具有默认值 `null`。示例 4-82 显示了你如何通过初始化创建交数组。

示例 4-82. 创建交数组

```
int[][] jaggedArray = {new int[] {1, 2, 3}, new int[] {4, 5}, new int[] {6}};
```

 数组最大的问题是它们是固定大小的。当你处理一组对象时，通常需要添加项。

## 理解泛型与非泛型

大多数集合类型都有泛型和非泛型版本。当你处理一种类型的对象时，使用泛型集合。

非泛型集合可以在 `System.Collections` 中找到，而泛型集合可以在 `System.Generic` 中找到。

如果你使用值类型作为参数，将消除所有可能装箱（boxing）的情况。例如，`Equatable<T>`。

## 使用 *List*

你可能最常用的集合类型是泛型 `List<T>` 集合。`List` 类型提供了添加、删除和搜索列表的方法。

`List` 类型确保有足够的空间存储额外的项。`List<T>` 可以存储引用类型，且项可以为空。它还可以存储重复项。

`List<T>` 的类定义如下：

```
public class List<T> : IList<T>, ICollection<T>, IList, ICollection,
       IReadOnlyList<T>, IReadOnlyCollection<T>, IEnumerable<T>, IEnumerable
```

`List<T>` 实现了相当接口。当然，它实现了 `IEnumerable<T>` 和 `IEnumerable`，因此你可以在 `foreach` 模式中使用它而不必担心实现。`IList` 和 `ICollection` 是定义该集合实际用的接口。`IList<T>` 和 `ICollection<T>` 可以在示例 4-83 中找到。

示例 4-83. 使用 *IList<T>* 和 *ICollection<T>*

``````
public interface IList<T> : ICollection<T>, IEnumerable<T>, IEnumerable
{
        T this[int index] { get; set; }
        int IndexOf(T item);
        void Insert(int index, T item);
        void RemoveAt(int index);
}

public interface ICollection<T> : IEnumerable<T>, IEnumerable
{
        int Count { get; }    
        bool IsReadOnly { get; }
        void Add(T item);    
        void Clear();    
        bool Contains(T item);    
        void CopyTo(T[] array, int arrayIndex);    
        bool Remove(T item);
}
```

示例 4-84 显示了一个你如何通过添加、删除、搜索和迭代项来使用 *List* 的示例。





# 示例 4-84. 使用 `List<T>`

```
List<string> listOfStrings =
    new List<string> { "A", "B", "C", "D", "E" };

for (int x = 0; x < listOfStrings.Count; x++)
    Console.Write(listOfStrings[x]); // Displays: ABCDE

listOfStrings.Remove("A");

Console.WriteLine(listOfStrings[0]); // Displays: B

listOfStrings.Add("F");

Console.WriteLine(listOfStrings.Count); // Displays: 5

bool hasC = listOfStrings.Contains("C");

Console.WriteLine(hasC); // Displays: true
```

## 使用 `Dictionary`

`List<T>` 仅存储一组项目。它允许重复项并可以快速查找项。

`Dictionary<TKey,TValue>` 可用于希望存储项并通过键检索项的场景，因此它不允许重复的键。它接受两个类型参数：一个用于键的类型，另一个用于值的类型。

`Dictionary` 类被实现为哈希表，这使得检索速度非常快，接近 O(1)。键的哈希值在过程中不应改变，且不能为空。值可以为空（如果它是引用类型）。

`Dictionary<TKey,TValue>` 类的签名如下：

```
public class Dictionary<TKey, TValue> : IDictionary<TKey, TValue>,        
    ICollection<KeyValuePair<TKey, TValue>>, IDictionary, ICollection,   
    IReadOnlyDictionary<TKey, TValue>, IReadOnlyCollection<KeyValuePair<TKey, TValue>>,       
    IEnumerable<KeyValuePair<TKey, TValue>>, IEnumerable, ISerializable,
    IDeserializationCallback
```

`Dictionary` 类与 `KeyValuePair<TKey,TValue>` 结构一起工作。示例 4-85 展示了你如何使用 `Dictionary`。

### 示例 4-85. 使用 `Dictionary<TKey, T Value>`

```
Person p1 = new Person { Id = 1, Name = "Name1" };
Person p2 = new Person { Id = 2, Name = "Name2" };
Person p3 = new Person { Id = 3, Name = "Name3" };

var dict = new Dictionary<int, Person>();
dict.Add(p1.Id, p1);
dict.Add(p2.Id, p2);
dict.Add(p3.Id, p3);

foreach (KeyValuePair<int, Person> v in dict)
{
    Console.WriteLine("{0}: {1}", v.Key, v.Value.Name);
}

dict[0] = new Person { Id = 4, Name = "Name4" };

Person result;
if (!dict.TryGetValue(5, out result))
{
    Console.WriteLine("No person with a key of 5 can be found");
}
```

## 使用集合

在某些语言中（如 Java），有一种特殊的 `set` 类型。在 C# 中，`set` 是一个保留关键字，但如果你需要，可以使用 `HashSet<T>`。集合是一个不包含重复元素且没有特定顺序的集合。

在数学中，你通常会对集合执行操作，例如查看一个集合是否是另一个集合的子集、选择两个集合共有或不共有的元素以及合并两个集合。`HashSet` 实现了 `ISet<T>` 接口，该接口包含可以在 示例 4-86 中找到的成员。

### 示例 4-86. 使用 `ISet<T>` 接口

```
public interface ISet<T> : ICollection<T>, IEnumerable<T>, IEnumerable
{
        bool Add(T item);
        void ExceptWith(IEnumerable<T> other);
        void IntersectWith(IEnumerable<T> other);
        bool IsProperSubsetOf(IEnumerable<T> other);
        bool IsProperSupersetOf(IEnumerable<T> other);
        bool IsSubsetOf(IEnumerable<T> other);
        bool IsSupersetOf(IEnumerable<T> other);
        bool Overlaps(IEnumerable<T> other);
        bool SetEquals(IEnumerable<T> other);
        void SymmetricExceptWith(IEnumerable<T> other);
        void UnionWith(IEnumerable<T> other);
}
```

与与其他集合一样，你可以轻松地向其添加新对象并对其进行迭代。示例 4-87 展示了一个关于如何使用 `HashSet<T>` 的示例。

### 示例 4-87. 使用 `HashSet<T>`

```csharp
public void UseHashSet()
{
    HashSet<int> oddSet = new HashSet<int>();
    HashSet<int> evenSet = new HashSet<int>();

    for (int x = 1; x <= 10; x++)
    {
        if (x % 2 == 0)
            evenSet.Add(x);
        else
            oddSet.Add(x);
    }
}
```





`.NET` `Framework` 提供了更多专门的集合。如果你想了解更多关于这些集合类型，请参见 [`msdn.microsoft.com/en-us/library/7y3x785f.aspx`](http://msdn.microsoft.com/en-us/library/7y3x785f.aspx)。

## 创建自定义集合

可以通过实现 `IEnumerable` 或 `IEnumerable<T>` 来实现基础集合。通过这种方式，你实现了迭代器模式，你的集合就可以在 `foreach` 语句中使用。

如果你需要更多功能，可以查看 `.NET` 中现有集合所实现的接口。你在在本章中回顾过的类所使用的接口有这些：

*   `IList<T>`
*   `ICollection<T>`
*   `IDictionary<TKey,TValue>`
*   `ICollection<TKey,TValue>`
*   `ISet<T>`

当然，你也可以选择直接继承自现有的集合。示例 4-90 展示了如何通过继承 `List<T>` 来添加特定功能的示例。

示例 4-90. 继承 `List<T>` 以形成自定义集合

```sharp
public class PeopleCollection : List<Person>
{
    public void RemoveByAge(int age)
    {
        for (int index = this.Count - 1; index >= 0; index--)
        {
            if (this[index].Age == age)
            {
                this.RemoveAt(index);
            }
        }
    }

    public override string ToString()
    {
        StringBuilder sb = new StringBuilder();
        foreach (Person p in this)
        {
            sb.AppendFormat("{0} {1} is {2}", p.FirstName, p.LastName, p.Age);
        }
        return sb.ToString();
    }
}
```

然后你可以像使用其他集合一样使用这个集合。示例 4-91 展示了你如何初始化它，然后使用你的自定义函数来操作它。

示例 4-91. 使用自定义集合

```sharp
public class Person
{
    public string FirstName { get; set; }
    public string LastName { get; set; }
    public int Age { get; set; }
}
Person p1 = new Person
{
    FirstName = "John",
    LastName = "Doe",
    Age = 42
};
Person p2 = new Person
{
    FirstName = "Jane",
    LastName = "Doe",
    Age = 21
};

PeopleCollection people = new PeopleCollection { p1, p2 };
people.RemoveByAge(42);
Console.WriteLine(people.Count); // Displays: 1
```

## 思考实验

### 选择正确的集合

你正尝试确定 `.NET` 使用的不同集合。你尝试根据性能和用例对不同的集合类型进行比较。

1.  什么时候应该使用泛型集合或非泛型集合？
2.  基于 `Dictionary` 和基于 `List` 的集合之间有什么区别？什么时候应该使用其中一个？
3.  `Stack`、`Queue` 和 `List` 集合之间有什么区别？

## 目标总结

*   `.NET` `Framework` 提供了泛型和非泛型集合。在可能的情况下，你应该使用泛型版本。
*   `Array` 是存储项目最基础的类型。它具有固定的大小。
*   `List` 是一个可以在需要时增长的集合。它是最常用的集合。
*   `Dictionary` 使用键/值对来存储和访问项目。
*   `HashSet` 存储唯一项目，并提供了可以对它们使用的集合操作。
*   `Queue` 是一个先进先出（FIFO）集合。
*   `Stack` 是一个后进先出（FILO）集合。
*   你可以通过继承集合类或继承其中一个集合接口来创建自定义集合。

### 目标回顾

回答以下问题以测试你对本目标中信息的掌握情况。你可以在本章末的 答案 部分找到这些问题的答案，以及对每个选项为何正确或错误的解释。

1.  你想存储一组订单，并确保用户可以根据订单号轻松地选择订单。你使用哪个集合？
    1.  `List<Order>`
    2.  `Dictionary<int,Order>`
    3.  `HashSet<Order>`
    4.  `Queue<Order>`
2.  你正在使用队列并想添加一个新项目。你使用哪个方法？
    1.  `Push`
    2.  `Add`
    3.  `Dequeue`
    4.  `Enqueue`
3.  你正在处理大量的姓氏对象。你需要删除所有重复项并按姓氏进行分组。你应该使用哪些集合？（选择所有适用项）
    1.  `List<T>`
    2.  `HashSet<T>`
    3.  `Dictionary<T>`
    4.  `Stack<T>`

## 答案

本部分包含思考实验的解答和回顾的答案。

### 目标 4.1 思考实验

1.  什么时候应该使用泛型集合或非泛型集合？
    尽可能使用泛型集合以确保类型安全并避免装箱/拆箱开销。
2.  基于 `Dictionary` 和基于 `List` 的集合之间有什么区别？什么时候应该使用其中一个？
    `Dictionary` 使用键/值对并提供快速查找，而 `List` 是按索引访问的集合。当你需要唯一标识符检索数据时使用 `Dictionary`，当需要顺序时使用 `List`。
3.  `Stack`、`Queue` 和 `List` 集合之间有什么区别？
    `Stack` 是 FILO（后进先出），`Queue` 是 FIFO（先进先出），而 `List` 是允许随机访问的通用集合。

### 目标 4.1 目标回顾

1.  **正确答案是 2**。`Dictionary<int,Order>` 允许你根据订单号选择订单。
2.  **正确答案是 4**。`Enqueue` 是向 `Queue` 添加项目的方法。
3.  **正确答案是 2**。`HashSet<T>` 用于删除重复项。





3. **错误：** 因为 `ASCII` 只支持有限的字符范围，在大多数国际化应用中是不够的。

4. **错误：** `UTF-32` 需要大量的空间来存储字符（每个字符占 4 字节）。它用于应用程序希望将 Unicode 补充字符（例如中文字符）编码为单个字形的情况。只有当此类字符的编码空间对你很重要时，你才需要它。如果你不需要 Unicode 补充字符，可以使用 `UTF-8`。如果你需要它们，可以使用 `UTF-16`，除非你有非常严格的空间限制。

### 目标 4.2：思考性实验

1. 使用 `Entity Framework` 可以提高你的开发速度。你不需要考虑如何将数据从数据库转换为对象。它还会替你管理更改跟踪，并将你的 `LINQ` 查询转换为 `SQL`。然而，这会带来（有时是巨大的）性能开销。如果你确实不需要对象模型来向客户端暴露数据，可以使用原始的 `SQL` 查询来获得更高的性能。

2. 针对你的 Web 服务，你可以使用 `WCF.to` 编写普通类，并在类上使用某些属性将它们暴露为服务。通过分离配置，你可以为不同的用户类型暴露多个端点。例如，你可以使用 `JSON` 端点或 `XML` 端点。

3. 你可以使用 `XmlWriter` 类来实现此功能。因为你正在处理大量数据，`XmlDocument` 可能太慢。当你不需要编辑数据而只需要输出它时，`XmlWriter` 是一个很好的选择。

### 目标 4.2：客观题

1. **正确答案：** A, C
    1. **正确：** 你需要一个 `SqlCommand` 来在数据库上执行更新查询。
    2. **错误：** 从数据库中选择某些数据时使用 `SqlDataReader`。在执行更新命令时不需要使用它。
    3. **正确：** 你需要一个 `SqlConnection` 来建立与数据库的连接。`SqlCommand` 使用该连接来执行更新查询。
    4. **错误：** 当仅执行单个命令时，不需要 `Transaction`。如果发生异常，不需要取消其他查询。

2. **正确答案：** B
    1. **错误：** 将数据存储在原始的 `XML` 文件中不允许多个用户同时读取和更新它。
    2. **正确：** 使用 `Entity Framework` 存储数据并映射到对象的关系型数据库有助于你快速开发应用程序。
    3. **错误：** 关系型数据库是存储数据的最佳选择。使用原始的 `ADO.NET` 代码需要你手动将对象映射到数据库，反之亦然。
    4. **错误：** `dynamic` 关键字可以用于需要弱类型的场景。如果某个操作不可用，它在运行时仍然会抛错误。

3. **正确答案：** A
    1. **正确：** 在处理大量数据时，`XmlReader` 是最快的选项。因为你只需要读取它而不进行任何更改，所以这是最佳选择。
    2. **错误：** 在处理大型 `XML` 文件时，`XmlDocument` 的速度不够快。
    3. **错误：** `XmlWriter` 用于创建 `XML` 文件，而不是读取它们。
    4. **错误：** 使用 `FileStream` 会将 `XML` 文件视为纯文本。你丢失了文档层次化结构带来的优势。此外，将其作为纯文本解析并不是一项简单的任务。

### 目标 4.3：思考性实验

1. 虽然 `LINQ` 并不总是像手动循环或过滤那样快，但你获得了许多其他益处。`LINQ to Entities` 将你的 `LINQ` 查询转换为 `SQL`，这使得你能够对数据库创建强类型查询。`LINQ to XML` 使用它来处理 `XML` 文件，其语法比手动操作更具流式感。使用 `LINQ` 的最大优势是你可以使用统一的、强类型的方法对多个不同的数据源进行查询。大多数情况下，开发时间比过早优化更重要。如果你确实遇到性能瓶颈，可以衡量你的代码并针对性地优化查询。

2. `LINQ` 是强类型的，并且比手写的循环或查询更容易读。`LINQ` 提供了如 `Sum`、`Average` 和 `GroupBy` 等运算符，这些运算符可以让编写复杂查询变得简单得多。

3. 查询语法会被编译器翻译为方法语法。并不是所有的运算符都支持查询语法支持。如果你需要一个仅在方法语法中可用的特殊运算符，你就被迫使用方法语法。查询语法更具可读性，应该尽可能使用它。

### 目标 4.3：客观题

1. **正确答案：** B, D
    1. **错误：** 将 `DateTime.Now` 与日期比较将只给你今天的日期，而不是整年的日期。此外，使用 `OrderBy` 而不是 `OrderByDescending` 将给你最小日期，而不是最大日期。
    2. **正确：** 这将返回当前最大的日期。如果你的过滤器找不到当年的值，它将返回 `‘1-1-0001 00:00:00’ (DateTime.Min-Value)`。
    3. **错误：** 如果你的过滤器没有返回值，你将得到错误。你应该改用 `FirstOrDefault`。
    4. **正确：** 如果当年有多个日期，使用 `Single` 将会抛出异常。

2. **正确答案：** A, B
    1. **正确：** `LINQ to Entities` 需要一个 `using` 语句。
    2. **正确：** `LINQ` 是实现为 `IEnumerable` 上的扩展方法。
    3. **错误：** 使用其中任何一个都不会改变任何。
    4. **错误：** 使用隐式类型允许编译器确定你查询的结果。

3. **正确答案：** A, C
    1. **正确：** 由于 `LINQ` 的延迟执行，你执行了两次查询——一次获取项目数量，一次获取所有产品。
    2. **错误：** 如果你从未迭代查询，你将无法获得任何结果。
    3. **正确：** 分页可以帮助限制检索的项目数量。
    4. **错误：** 方法语法被编译为查询语法。这在功能上没有任何区别。

### 目标 4.4：思考性实验

1. 你可以使用 `Binary` 格式，它是最小且高效的。`XML` 和 `JSON` 是人类可读的，但它们会导致更大的文件，序列化到它们也更慢。

2. 你可以使用 `BinaryFormatter` 将数据序列化到 `Stream` 中。

3. 因为你有一些敏感数据（登录凭据），所以实现 `ISerializable` 接口很重要，这样你就可以对这些属性拥有完全控制。否则，某些可能会打开你的二进制文件并从中提取所有的登录凭据。

### 目标 4.4：客观题

1. **正确答案：** B
    1. **错误：** 虽然 `XML` 是人类可读的，但它不是最优化的格式。它产生的文件比二进制格式大。
    2. **正确：** 二进制格式是存储大量数据最高的方式。
    3. **错误：** WCF 使用 `DataContractSerializer` 将数据序列化为 `XML`。
    4. **错误：** `DataContractJsonSerializer` 将你的对象序列化为 `JSON`。`JSON` 用于浏览器和服务器之间的通信。

2. **正确答案：** B, D
    1. **错误：** `XmlSerializer` 输出的是 `XML` 文本，而不是二进制数据。
    2. **正确：** 对于某些敏感数据的类型应该实现 `ISerializable`。





## 习习题

3. **错误：** WCF 使用 `DataContractSerializer` 将数据序列化为 XML。
4. **正确：** 可以使用 `BinaryFormatter` 将数据序列化为二进制格式。

3. **正确答案:** C

1. **错误：** `XmlElement` 用于配置如何将成员序列化为 XML 元素。
2. **错误：** `XmlAttribute` 将成员输出为其父节点上的属性，而不是单独的节点。
3. **正确：** `XmlIgnore` 确保成员不被序列化。
4. **错误：** `NonSerialized` 属性与 `BinaryFormatter` 或 `Soap-Formatter` 一起使用。

## 目标 4.5：思维实验

1. 当你处理一组具有相同类型的项目时，应该使用泛型集合。它能为你提供更好的性能，并允许你在不进行强制类型转换的情况下访问项目。当你想要混合不同类型的对象时，可以使用非泛型集合。
2. 基于字典的集合为其存储的每个值都提供一个键（key），因此检索项的速度非常快。它们不能存储重复项。`List` 以不特定的顺序存储项目。你可以通过索引访问项目。
3. 当你需要按照特殊顺序（后进先出 FILO 或先进先出 FIFO）检索项目时，可以使用 `Stack` 和 `Queue` 集合。它们在检索项目后会将其移除。`List` 提供对所有元素的随机访问。

### 目标 4.5：目标回顾

1. **正确答案：** B, D
1. **错误：** `List<Order>` 为元素提供随机访问。它通过 id 选择特定 `Order` 项目的速度并不快。
2. **正确：** 通过使用 `Dictionary<int,Order>`，你可以轻松地通过 id 选择 `Order`。
3. **错误：** `HashSet` 不对其项目提供随机访问。你需要枚举整个集合才能获取某个订单。
4. **正确：** `Queue` 提供一个先进先出（FIFO）集合。你无法随机访问项目，并且项目在检索后会被被丢弃。
2. **正确答案：** B, D
1. **错误：** `Push` 用于向 `Stack` 中添加项目。
2. **正确：** `Add` 用于自自 `ICollection<T>` 的类型。`Queue` 不继承自 `ICollection<T>`，而是继承自 `ICollection`。
3. **错误：** `Dequeue` 用于从 `Queue` 中移除项目。
4. **正确：** `Enqueue` 用于向 `Queue` 中添加项目。
3. **正确答案：** A, C
1. **正确：** 你需要一个列表来存储所有重复的姓氏项目。
2. **错误：** `Stack` 在后进先出（LIFO）的基础上存储项目。它不适合存储重复或不重复的项目。
3. **正确：** `Dictionary<string,T>` 可用于存储姓氏不重复的项目。
4. **错误：** 你不能从普通数组中移除项目。

# 附录 A. 关于作者

**WOUTER DE KORT** 是 Seize IT 的独立技术教练、培训师和开发人员。他拥有 MCSD 认证。作为软件架构师，他指导过复杂的 Web 应用程序开发。他还担任过技术宣教员，帮助组织处于 Web 开发的最前沿。Wouter 从 C# 和 .NET 诞生起一直使用它们；他的专业知识还 Visual Studio、Team Foundation Server、Entity Framework、单元测试、设计模式、ASP.NET 和 JavaScript。

![image with no caption](img/httpatomoreillycomsourcemspimages1722830.png.jpg)

# 索引

### 关于数字索引的说明

索引项中的链接显示为该条目所在的章节标题。由于某些章节有多个索引标记，一个条目有多个指向同一章节的链接并不稀见。点击任何链接都将直接带你到正文中标记出现的位置。

### A

- 抽象基类（abstract base classes），更改行为
- 访问修饰符，目标 2.3: 强制封装, 目标 2.3: 强制封装, 使用 private 隐藏, 在继承层次结构中保护可访问性, 在继承层次结构中保护可访问性
- internal，在继承层次结构中保护可访问性
- private，使用 private 隐藏
- protected，在继承层次结构中保护可访问性
- public，目标 2.3: 强制封装
- 访问数据，目标回顾 (参见数据访问)
- 访问共享数据，多线程应用程序，目标回顾
- Action 类型，Lambda 表达式
- Add 方法，ConcurrentBag，BlockingCollection<T>
- 添加（adding），使用 Tasks, 值类型和引用类型
- 任务的行为（behaviors to），值类型和引用类型
- 任务的延续（continuations），使用 Tasks
- 传递项目数据（data to），命名参数和可可见性
- AddOrUpdate 方法，ConcurrentDictionary，ConcurrentDictionary
- 地址（address），WCF，创建 WCF
- 高级加密标准（AES algorithm），使用加密
- AES 高级加密标准（AES algorithm），使用加密
- AesManaged 类，使用加密
- 聚合异常（AggregateExceptions），使用 async 和 await, 并行语言查询 (PLINQ)
- AJAX（异步 XML），使用 JSON
- 算法（algorithms），加密，使用加密, 使用加密
- .NET 框架，使用加密
- 对称和加密，使用加密
- 允许多个参数（AllowMultiple），自定义属性
- AND 运算符，布尔表达式
- 匿名函数（anonymous functions），Lambda 表达式
- 匿名方法（anonymous methods），Lambda 表达式
- 匿名类型（anonymous types），LINQ，Lambda 表达式
- API（应用程序接口），自动化，使用动态类型
- app.config 文件，连接字符串，连接数据库
- 应用程序配置文件，程序集版本](#ch03.html_iddle1031)
- 应用程序接口（APIs），自动化，使用动态类型
- 应用程序（applications），目标 1.1: 多线程和异步处理, 目标 1.1: 多线程和异步处理
- 线程池，ch01.html_iddle1046)
- 使用 Tasks，ch01.html_iddle1044)
- 使用 Parallel 类，ch01.html_iddle1042)
- 使用 async 和 await，ch01.html_iddle1045)
- 使用并行语言查询 (PLINQ)，ch01.html_iddle1043)
- 调试应用程序和实现安全，ch03.html_iddle1040)
- 编译配置，ch03.html_iddle1035)
- 创建和管理编译指令，ch03.html_iddle1039)





# 调试
- 调试应用程序并实现安全
- 目标回顾
- 目标回顾
- 目标 3.4 调试应用程序
- 目标 3.4 调试应用程序
- 生成配置
- 创建和管理编译器指令
- 目标回顾

## 程序集管理
- 目标回顾

## 编译器指令
- 生成配置

## 配置、诊断与加密
### 配置
- 目标 3.4 调试应用程序

### 诊断
- 目标回顾

# 加密
- 目标回顾

## PDB 文件与符号
- 创建和管理编译器指令

## 验证应用程序输入
- 调试应用程序并实现安全

## 多线程与异步处理
### 多线程
- 目标 1.1: 实现多线程和异步处理
- 目标 1.1: 实现多线程和异步处理
- 线程池
- 使用 Tasks
- 使用 Parallel 类
- 使用 async 和 await
- 使用并行语言集成查询 (PLINQ)

### 异步处理
- 使用 Parallel 类

### 并发集合
- 使用并行语言集成查询 (PLINQ)

### Parallel 类
- 使用 Tasks

### PLINQ
- 使用 async 和 await

### Tasks
- 线程池

### 线程
- 目标 1.1: 实现多线程和异步处理

## 反射与属性
- 应用属性 目标 2.5: 使用反射在运行时查找、执行和创建类型

## 异常与参数
### `ArgumentException`
- 验证 JSON 和 XML

### `ArgumentNullException`
- 处理异常
- 使用 Parse、TryParse 和 Convert

### 参数
- 添加行为
- 添加行为
- 添加行为
- 具名添加行为](#ch02.html_iddle1052)
- 可选添加行为](#ch02.html_iddle1053)
- 重载添加行为](#ch02.html_iddle1054)

## 集合与数据存储
### `Array` 类
- 目标 4.5: 在集合中存储和从集合中检索数据

## 数组、集合
- 目标 4.5: 在集合中存储和从集合中检索数据

### 转换与流
- `as` 运算符 使用辅助类进行转换
- `ASCII` 基础 Stream 类

## 异步方法
- `AsParallel` 方法 使用 async 和 await

## 程序集管理
### 程序集
- 在继承层次结构中保护可访问性
- 目标回顾
- 什么是程序集？
- 使用强名称对程序集签名
- 将程序集放入 GAC
- 将程序集放入 GAC
- 程序集版本控制

### 内部访问修饰符
- 在继承层次结构中保护可访问性

### 管理
- 目标回顾
- 什么是程序集？
- 使用强名称对程序集签名
- 将程序集放入 GAC
- 将程序集放入 GAC
- 程序集版本控制

### 创建程序集
- 程序集版本控制

### 定义程序集
- 什么是程序集？

### 将程序集放入 GAC
- 将程序集放入 GAC

### 使用强名称签名
- 使用强名称对程序集签名

## 程序集版本
- 将程序集放入 GAC

### 程序集元数据
- `FileVersionAttribute` 程序集版本控制
- `AssemblyInfo.cs` 类
- `AssemblyInfo.cs` 文件 程序集版本控制
- `VersionAttribute` 程序集版本控制

## 异步编程
- `AsSequential` 方法 使用并行语言集成查询 (PLINQ)
- 非对称加密 对称和非对称加密
- `async` 关键字 实现异步 I/O
- `async` 关键字，异步处理 使用 Parallel 类
- 异步 I/O 实现异步 I/O
- 异步 JavaScript 和 XML (AJAX) 消费 JSON
- 异步处理，多线程应用 使用 Parallel 类

## 原子操作
- `ConcurrentDictionary` (#ch01.html_iddle1079)
- 原子性属性（事务）使用参数

## 属性详情
- 属性 使用 Thread 类
- Flags、枚举与 创建枚举
- `InternalsVisibleAttribute` 保持类型对程序集内部
- `OnDeserializedAttribute` 使用序列化
- `OnDeserializingAttribute` 使用序列化
- `OnSerializedAttribute` 使用序列化
- `OnSerializingAttribute` 使用序列化
- `OperationContract` 使用对象关系映射 (ORM)
- `OptionalFieldAttribute` 使用序列化
- `SecurityPermission` 使用序列化
- `SerializableAttribute` 目标 2.5: 使用反射在运行时查找、执行和创建类型
- `ServiceContract` 使用对象关系映射 (ORM)
- `ThreadStatic` 使用 Thread 类
- `Trait` 读取属性
- `XmlSerializer` 使用 XmlSerializer





用户身份验证，目标回顾（参见加密）

自动实现属性，使用属性

自动化 API，使用动态类型

`AverageTimer32`（性能计数器），创建和监控性能计数器

`await` 关键字，实现异步 I/O 操作

`await` 关键字，异步处理，使用 Parallel 类

### B

后台线程，使用 Thread 类

基类，创建和使用基类, 创建和使用基类, 更改行为, 更改行为

抽象，更改行为

行为，创建和使用基类

密封，更改行为

行为，值类型和引用类型, 创建和使用基类

在类型体中添加，值类型和引用类型

基类，创建和使用基类

`BigEndianUnicode`，基 Stream 类

二进制序列化，使用二进制序列化

`BindingFlags` 枚举，使用反射

WCF 服务绑定，创建 WCF 服务

`BlockingCollection` 集合，使用并行语言查询 (PLINQ)

蓝图，创建类型，添加一些数据

体（创建类型），值类型和引用类型, 值类型和引用类型, 添加行为, 命名参数、可选参数和重载可见性, 添加一些数据

添加行为，值类型和引用类型

添加数据，命名参数、可选参数和重载可见性

蓝图，添加一些数据

命名和可选参数，添加行为

布尔表达式，程序流，目标回顾

装箱值类型，目标 2.2: 使用类型

分支指令，生成配置

断点，在 Visual Studio 中设置，生成配置

`BufferedStream`，一起使用不同类型的流](#ch04.html_iddle1128)

版本号（程序集），程序集版本控制

### C

C# 类型，创建和使用类型, 目标 2.2: 消费类型, 目标 2.3: 强制封装, 目标回顾, 目标 2.5: 使用反射在运行时查找、执行和创建类型, 目标 2.6: 管理对象生命周期, 目标回顾

类层次结构，目标回顾

消费，目标 2.2: 消费类型

创建，创建和使用类型

强制封装，目标 2.3: 强制封装

管理对象生命周期，目标 2.6: 管理对象生命周期

处理字符串，目标回顾

反射，目标 2.5: 使用反射在运行时查找、执行和创建类型

CA（证书颁发机构），管理和创建证书

调用堆窗口，管理程序数据库文件和符号

调用栈，使用 Thread 类, 使用代码访问权限

调用方法，添加行为

取消任务，Interlocked 类

`CancellationToken` 方法，Interlocked 类

`CancellationTokenSource` 方法，取消任务

CAS（代码访问安全），管理和创建证书

catch 块，处理异常

处理器（CPU）和线程，目标 1.1: 实现多线程和异步处理

证书颁发机构 (CA)，管理和创建证书

证书，数字，管理和创建证书

链式构造函数，使用蓝图

子类，创建和使用基类

子元素，XML 文档，消费 XML

子任务，使用 Tasks

密文，使用对称和非对称加密

类层次结构，目标回顾, 目标 2.4: 创建和实现类层次结构, 创建和使用基类, Liskov 替换原则

.NET Framework 标准接口，Liskov 替换原则

基类，创建和使用基类

设计和实现接口，目标 2.4: 创建和实现类层次结构





# 核心技术主题索引

## 线程与并发 (Threads and Concurrency)
- 理解线程
- 理解线程
- 使用 Thread 类
- 使用 Thread 类
- 使用 Tasks
- 使用 async 和 await
- 使用 async 和 await
- 同步资源
- Volatile 类
- 控制台同步
- **关键组件**: `Thread`, `Task`, `async`, `await`, `Volatile`, `Console`

## 面向对象与基础结构 (OOP and Basics)
- 使用蓝图
- Office 自动化 API
- Office 自动化 API
- 使用属性
- 创建并使用基类
- 创建基类
- 设计原则
- **关键组件**: `base classes`, `properties`, `DbContext`

## 数据处理与转换 (Data Processing and Conversion)
- 在 .NET Framework 中使用字符串
- 使用 Parse, TryParse 和 Convert
- CultureInfo
- **关键组件**: `string`, `Parse`, `TryParse`, `Convert`, `CultureInfo`

## 安全与加密 (Security)
- 使用对称和非对称加密
- 在 .NET Framework 中处理加密
- 在 .NET Framework 中处理加密
- 在 .NET Framework 中处理加密
- 使用哈希
- 使用哈希
- 保护字符串数据
- **关键组件**: `AesManaged`, `symmetric encryption`, `asymmetric encryption`, `hashing`, `RSACryptoServiceProvider`

## 诊断与性能 (Logging and Performance)
- 日志记录与追踪
- 日志记录与追踪
- 日志记录与追踪
- 分析您的应用程序
- 创建并监控性能计数器
- **关键组件**: `Debug`, `TraceSource`, `PerformanceCounter`, `Stopwatch`

## I/O 与文件系统 (I/O and File System)
- 目标 4.1: 执行 I/O 操作
- 目录
- 目录
- 处理文件
- 处理路径
- 处理路径
- 文件系统不仅仅是为了你存在
- 文件系统不仅仅是为了你存在
- **关键组件**: `Directory`, `DirectoryInfo`, `Path`, `Stream`

## 数据库 (Databases)
- 操作数据库
- 连接数据库
- 连接数据库
- 连接数据库
- **关键组件**: `DbConnection`, `DbConnectionStringBuilder`, `SqlConnectionStringBuilder`, `TransactionScope`

## XML 与序列化 (XML and Serialization)
- 消费 XML
- 消费 XML
- 消费 XML
- XmlReader
- XmlWriter
- XmlDocument
- 创建 XML
- **关键组件**: `XmlReader`, `XmlWriter`, `XmlDocument`, `XElement`, `XPathNavigator`

## 集合操作 (Collections)
- 目标 4.5: 在集合中存储和检索数据
- 使用 List
- 使用 Dictionary
- 使用队列和栈
- **关键组件**: `Array`, `Dictionary`, `Queue`, `Stack`

## 高级特性 (Advanced Features)
- 理解委托
- 使用 Lambda 表达式
- 处理异常
- **关键组件**: `delegate`, `lambda expressions`, `exception`, `closures`





# 集合

- 使用并行语言集成查询 (PLINQ)
- BlockingCollection<T
- ConcurrentStack 和 ConcurrentQueue
- ConcurrentStack 和 ConcurrentQueue
- ConcurrentStack 和 ConcurrentQueue
- ConcurrentStack 和 ConcurrentQueue
- ConcurrentDictionary
- 遍历集合
- 遍历集合
- while 和 do-while 循环
- foreach 循环
- foreach 循环
- 目标回顾
- 目标 4.5：在集合中存储和检索数据
- 使用数组
- 使用数组
- 使用 Dictionary
- 使用集合
- 使用队列和栈
- 使用队列和栈
- 使用队列和栈

### BlockingCollection
- 使用并行语言集成查询 (PLINQ)

## ConcurrentBag
- BlockingCollection<T

## ConcurrentDictionary
- ConcurrentDictionary

## ConcurrentQueue
- ConcurrentStack 和 ConcurrentQueue

## ConcurrentStack
- ConcurrentStack 和 ConcurrentQueue

## 数据访问
- 目标回顾
- 目标 4.5：在集合中存储和检索数据
- 使用数组
- 使用数组
- 使用 Dictionary
- 使用集合
- 使用队列和栈
- 使用队列和栈
- 使用队列和栈

## 数组
- 目标 4.5：在集合中存储和检索数据

## 选择集合类型
- 使用队列和栈

## 创建自定义集合
- 使用队列和栈

## Dictionary
- 使用 Dictionary

## 泛型与非泛型版本
- 使用数组

## List
- 使用数组

## 队列和栈
- 使用队列和栈

## 集合
- 使用集合

## FIFO（先进先出）
- ConcurrentStack 和 ConcurrentQueue

## 遍历
- 遍历集合
- 遍历集合
- while 和 do-while 循环
- foreach 循环
- foreach 循环

## for each 循环
- foreach 循环

## for 循环
- 遍历集合

### 跳转语句
- foreach 循环

## while 和 do-while 循环
- while 和 do-while 循环

## LIFO（后进先出）
- ConcurrentStack 和 ConcurrentQueue

## 使用 PIA 集成 COM（组件对象模型）
- 使用动态类型

## COM 交互类，IUnknown 接口
- IUnknown

## Combine 方法
- 使用路径

## 通用语言运行时 (CLR) 类型
- 值类型和引用类型

## CompareExchange 方法
- Interlocked 类

## CompareTo 方法
- Liskov 替换原则

## 编译器指令
- 构建

## Complete 方法
- BlockingCollection<T

## 使用 PIA 集成 COM（组件对象模型）
- 使用动态类型

## 并发集合，多线程应用程序
- 并行语言集成查询 (PLINQ)

## ConcurrentBag 集合
- BlockingCollection<T

## ConcurrentDictionary 集合
- ConcurrentDictionary

## ConcurrentQueue 集合
- ConcurrentStack 和 ConcurrentQueue

## ConcurrentStack 集合
- ConcurrentStack 和 ConcurrentQueue

## 条件运算符
- if 语句

## ConditionalAttribute
- 属性
- 创建和管理编译器指令

## ConfigurationManager.ConnectionStrings 属性
- 连接数据库

## 配置，调试应用程序
- 3.4

## ConfigureAwait 方法
- 使用 async 和 await

## 配置 TraceListener
- 日志和跟踪

## 确认类型转换
- 使用辅助类

## 连接到数据 (ADO.NET)
- 使用数据库

### 连接到数据库
- 使用数据库

## 连接池
- 连接数据库

## 连接字符串
- 使用数据库

## Consistency 属性 (事务)
- 使用参数

## Console 类，同步
- 理解线程

## Console.WriteLine 方法
- 命名参数、可选参数和重载

## 约束，泛型参数
- 使用泛型类型

## 构造函数
- 添加一些数据

## 消费数据
- 使用数据库
- 使用数据库
- 使用数据库
- 连接数据库
- 更新数据
- 使用参数
- 使用参数
- 使用事务
- 使用对象关系映射 (ORM
- 创建 WCF 服务
- 消费 XML
- XmlReader
- XmlWriter
- XmlWriter
- XmlDocument

# 数据库
- 使用数据库
- 使用数据库
- 使用数据库
- 连接数据库
- 更新数据
- 使用参数
- 使用参数
- 使用事务

## 连接到
- 使用数据库

## ORM (对象关系映射)
- 使用事务

## 参数
- 使用参数

### 提供程序
- 使用数据库

### 读取数据
- 连接数据库

### 事务
- 使用参数

### 更新数据
- 更新数据

## JSON
- XmlDocument

## Web 服务
- 使用对象关系映射 (ORM

## XML
- 创建 WCF 服务
- 消费 XML
- XmlReader
- XmlWriter
- XmlWriter

## .NET Framework
- 消费 XML

## XmlDocument 类
- XmlWriter

## XmlReader 类
- XmlReader

## XmlWriter
- XmlWriter

## 消费类型
- 目标 2.2：消费类型
- 目标 2.2：消费类型
- 装箱和拆箱
- 使用动态类型

## 值类型的装箱和拆箱
- 目标 2.2：消费类型





# 目录

- `转换`, 装箱与拆箱
- `动态类型`, 使用动态类型
- `Contains 方法`, 使用哈希算法
- `内容, XML 文档`, 消费 XML
- `上下文切换`, 理解线程
- `延续性任务`, 使用任务
- `ContinueWith 方法`, 使用任务
- `合约, WCF 服务`, 创建 WCF 服务
- `逆变性`, 理解委托程序
- `转换, 类型`, 装箱与拆箱, 管理数据完整性
- `拷贝文件`, 处理路径
- `协变性`, 理解委托程序
- `CPU 采样选项, 应用程序分析`, 分析您的应用程序
- `CPUs (中央处理器), 和线程`, 目标 1.1: 实现多线程和异步处理
- `Create 方法`, 文件系统不仅仅是为了为你准备
- `CreateAndRaise 属性`, 使用 Lambda 表达式
- `CreateText 方法`, 基 Stream 类
- `创建`, 理解线程, 资源同步, 抛出异常, 创建并使用类型, 目标 2.1: 创建类型, 目标 2.1: 创建类型, 创建枚举, 值类型和引用类型, 值类型和引用类型, 添加行为, 使用蓝图, 使用泛型类型, 使用泛型类型, 使用泛型类型, 将类型保持在程序集内部, 创建和使用基类, 读取属性, Lambda 表达式, 管理非托管资源, 程序集版本化, 生成配置, 目录, 处理路径, 对象初始化语法, Lambda 表达式, 使用队列和栈
- `匿名方法`, 对象初始化语法
- `匿名类型`, Lambda 表达式
- `特性`, 读取属性
- `基类`, 创建和使用基类
- `编译指令`, 生成配置
- `自定义集合`, 使用队列和栈
- `自定义异常`, 抛出异常
- `自定义结构体`, 值类型和引用类型
- `死锁`, 资源同步
- `目录`, 目录
- `扩展方法`, 使用泛型类型
- `FileStream`, 处理路径
- `终结器`, 管理非托管资源
- `泛型类型`, Lambda 表达式
- `方法`, 添加行为
- `属性`, 将类型保持在程序集内部
- `线程`, 理解线程
- `类型`, 创建并使用类型, 目标 2.1: 创建类型, 目标 2.1: 创建类型, 创建枚举, 值类型和引用类型, 使用蓝图, 使用泛型类型, 使用泛型类型
- `体`, 值类型和引用类型
- `类别`, 目标 2.1: 创建类型
- `类设计`, 使用蓝图
- `枚举`, 目标 2.1: 创建类型
- `扩展方法`, 使用泛型类型
- `泛型类型`, 使用泛型类型
- `值类型和引用类型`, 创建枚举
- `程序集`, 程序集版本化
- `加密`, 使用加密
- `CultureInfo`, 使用 CultureInfo
- `格式化`, 格式化
- `自定义`, 使用队列和栈
- `数据访问`, 事件访问
- `事件`, 使用事件
- `异常`, 抛出异常
- `结构体`, 自定义结构体
- `序列化`, 序列化
- `数据`, 数据访问
- `动态`, 动态类型
- `导出`, 导出到
- `Excel`, 使用 Excel





# 数据结构
- `List`, 使用数组
- `queues and stacks`, 使用队列和栈
- `sets`, 使用集合

# 数据消费
- `consuming data`, 目标回顾, 与数据库交互, 使用对象关系映射 (ORM), 创建 WCF 服务, `XmlDocument`
- `databases`, 与数据库交互
- `JSON`, `XmlDocument`
- `web services`, 使用对象关系映射 (ORM)
- `XML`, 创建 WCF 服务

# I/O 操作
- `I/O operations`, 实现数据访问, 目标 4.1: 执行 I/O 操作, 处理路径, 一起使用不同类型的流, 文件系统不仅仅是为你用的, 实现异步 I/O 操作
- `asynchronous I/O operations`, 实现异步 I/O 操作`
- `file infrastructure`, 目标 4.1: 执行 I/O 操作
- `file system`, 一起使用不同类型的流
- `network communication`, 文件系统不仅仅是为你用的
- `streams`, 处理路径

# LINQ
- `LINQ`, 目标回顾, 目标 4.3: 使用 LINQ 查询和操作数据及对象, 匿名类型, 标准 LINQ 查询操作符
- `functionality`, 标准 LINQ 查询操作符`
- `language features`, 目标 4.3: 使用 LINQ 查询和操作数据及对象`
- `queries`, 匿名类型`

# 序列化与反序列化
- `serialization/deserialization`, 目标 4.4: 序列化和反序列化数据, 目标 4.4: 序列化和反序列化数据`, 使用 XmlSerializer`, 使用二进制序列化`, 使用二进制序列化`, 使用 DataContract`
- `binary serialization`, 使用二进制序列化`
- `DataContract Serializer`, 使用二进制序列化`
- `functionality`, 目标 4.4: 序列化和反序列化数据`
- `JSON serializer`, 使用 DataContract`
- `XmlSerializer`, 使用 XmlSerializer`
- `data consumption`, 与数据库交互` (参见数据消费)

# 安全与完整性
- `Data Encryption Standard (DES) algorithm`, 使用对称和非对称加密`
- `data integrity, validating application input`, 目标 3.1: 验证应用输入`
- `data transfer object (DTO)`, 目标 4.4: 序列化和反序列化数据`

# 数据库
- `Database First approach (Entity Framework)`, 使用对象关系映射 (ORM)
- `databases`, 与数据库交互`, 与数据库交互`, 与数据库交互`, 连接到数据库`, 更新数据`, 使用参数`, 使用参数`, 使用事务`
- `connecting to`, 与数据库交互`
- `ORM (Object Relational Mapper)`, 使用事务`
- `parameters`, 使用参数`
- `providers`, 与数据库交互`
- `reading data`, 连接到数据库`
- `transactions`, 使用参数`
- `updating data`, 更新数据`
- `DataContract Serializer`, 使用二进制序列化`
- `DbConnection base class`, 与数据库交互`
- `DbConnectionString classes`, 连接到数据库`
- `DbContext class`, 使用属性`
- `deadlocks`, 同步资源`
- `Debug class`, 日志和跟踪`
- `debug mode configuration`, 目标 4.4: 调试应用程序`
- `DebuggerAttribute`, 创建和管理编译器指令`
- `debugging applications`, 调试应用程序并实现安全`, 目标 3.1: 验证应用输入`, 目标 3.1: 验证应用输入`, 管理数据完整性`, 使用 Parse`, `TryParse`, 和 `Convert`, 使用正则表达式`, 目标回顾`, 使用对称和非对称加密`, 使用对称和非对称加密`, 在 .NET Framework 中处理加密`, 管理和创建证书`, 管理和创建证书`, 使用代码访问权限`, 目标回顾`, 什么是程序集？, 使用强签名程序集`, 将程序集放入 GAC`, 将程序集放入 GAC`, 程序集版本化`, 目标 4.4: 调试应用程序`, 目标 4.4: 调试应用程序`, 构建配置`, 创建和管理编译器指令`, 目标回顾`, 目标回顾`, 分析你的应用程序`, 分析你的应用程序`

### 程序集与调试
- `assembly management`, 目标回顾`, 什么是程序集？, 使用强签名程序集`, 将程序集放入 GAC`, 将程序集放入 GAC`, 程序集版本化`
- `creating a WinMD assembly`, 程序集版本化`
- `defining assemblies`, 什么是程序集？
- `putting an assembly in the GAC`, 将程序集放入 GAC`
- `signing with a strong name`, 使用强签名程序集`
- `versioning assemblies`, 将程序集放入 GAC`
- `compiler directives`, 构建配置`
- `configurations`, 目标 4.4: 调试应用程序`
- `diagnostics`, 目标回顾`, 目标回顾`, 分析你的应用程序`, 分析你的应用程序`
- `logging and tracing`, 目标回顾`
- `performance counters`, 分析你的应用程序`
- `profiling applications`, 分析你的应用程序`





### 数字证书
管理和创建证书

哈希，在 .NET Framework 中处理加密

保护字符串数据安全，使用代码访问权限

对称和非对称加密，使用对称和非对称加密

PDB 文件和符号，创建和管理编译器指令

### 验证应用输入
调试应用并实现安全, 目标 3.1: 验证应用输入, 目标 3.1: 验证应用输入, 管理数据完整性, 使用 Parse、TryParse 和 Convert, 使用正则表达式

数据完整性，目标 3.1: 验证应用输入

JSON 和 XML 数据，使用正则表达式

类型间转换方法，管理数据完整性

验证的原因，目标 3.1: 验证应用输入

正则表达式，使用 Parse、TryParse 和 Convert

### 调试工具
PDBCopy，管理程序数据库文件和符号

### 决策语句，程序流
处理布尔表达式, 处理布尔表达式, if 语句, if 语句, switch 语句

条件运算符，if 语句

if 语句，处理布尔表达式

空合并运算符，if 语句

switch 语句，switch 语句

### 声明式 CAS
使用代码访问权限

声明数组，目标 4.5: 在集合中存储和从集合中检索数据

解码标准，Stream 类

装饰器模式，流，编码和解码

递减运算符，Volatile 类

解密，使用对称和非对称加密

DefaultTraceListener，日志记录和跟踪

延迟执行，标准 LINQ 查询操作符

### #define 指令
创建和管理编译器指令

委托，使用 Thread 类, 目标 1.4: 创建并实现事件和回调, 理解委托, 理解委托

协变和逆协变，理解委托

多路委托，理解委托

ParameterizedThreadStart，使用 Thread 类

### 目录和文件
删除，目录, 处理文件

目录，目录

文件，处理文件

### 部署
程序集，将程序集放入 GAC

Dequeue 方法，使用队列和栈

### 类设计
派生类，创建和使用基类

DES（数据加密标准）算法，使用对称和非对称加密

Descendants 方法，查询 XML

反序列化（数据），目标 4.4: 序列化和反序列化数据

设计，使用蓝图, 设计类, 目标 2.4: 创建并实现类层次结构

类，使用蓝图

接口，使用蓝图

SOLID 原则，设计类

诊断，设计类, 复习, 复习, 复习

性能，复习

计数器，复习

应用，复习

分析，复习

字典类，使用字典

字典，使用字典

数字证书，管理和创建证书

目录，目录

目录树，目录

DirectoryNotFoundException，目录

DirectorySecurity，目录

DirectoryInfo 对象，目录

DriveInfo 类，目录

Dispose 方法，接口

do-while 循环，if 语句

DTD 文件（类型定义），使用 XML

域完整性，管理数据完整性

DSACryptoServiceProvider，在 .NET Framework 中处理加密

DTD 文件（类型定义），使用 XML

DTO（数据传输对象），序列化和反序列化数据

持久性属性，参数

dynamic 关键字，动态类型

DynamicObject 类，Office 自动化 API

### E
else 块，if 语句

封装，目标 2.3: 强制封装, 目标 2.3: 强制封装, 目标 2.3: 强制封装, 私有, 在继承层次结构中保护可访问性, 在继承层次结构中保护可访问性, 在程序集内部保持类型, 使用属性

访问修饰符，目标 2.3: 强制封装, 目标 2.3: 强制封装, 私有, 在继承层次结构中保护可访问性, 在继承层次结构中保护可访问性

内部，在继承层次结构中保护可访问性

私有，私有 (此处应为私有)，私有](#ch02.html_iddle1490)

保护，在继承层次结构中保护可访问性

公共，目标 2.3: 强制封装

显式接口实现，使用属性

属性，在程序集内部保持类型

编码标准，Stream 类





# 加密
- `encryption`, 目标回顾
- 使用对称加密和非对称加密
- 使用对称加密和非对称加密
- 在 .NET Framework 中处理加密
- 管理和创建证书
- 管理和创建证书
- 使用代码访问权限

## .NET Framework
- `symmetric and asymmetric encryption`, 使用对称加密和非对称加密
- `code access permissions`, 管理和创建证书
- `digital certificates`, 管理和创建证书
- `hashing`, 在 .NET Framework 中处理加密
- `securing string data`, 使用代码访问权限

## 字符串搜索
- `EndsWith` 方法, 搜索字符串
- `enumeration strings`, 搜索字符串

### 目标 2.3: 强制封装
- `enforcing encapsulation`, 目标 2.3: 强制封装, 目标 2.3: 强制封装, 目标 2.3: 强制封装
- 使用 private 隐藏
- 在继承层次结构中保护可访问性, 在继承层次结构中保护可访问性
- 保持类型对程序程序集内部
- 使用属性
- `access modifiers`, 目标 2.3: 强制封装, 目标 2.3: 强制封装, 使用 private 隐藏, 在继承层次结构中保护可访问性, 在继承层次结构中保护可访问性
- `internal`, 在继承层次结构中保护可访问性
- `private`, 使用 private 隐藏
- `protected`, 在继承层次结构中保护可访问性
- `public`, 目标 2.3: 强制封装
- `explicit interface implementations`, 使用属性
- `properties`, 保持类型对程序程序集内部

## 队列和栈
- `Enqueue` 方法, ConcurrentStack 和 ConcurrentQueue, 使用队列和栈
- `enumerating a ConcurrentBag collection`, BlockingCollection<T>

## Entity Framework
- `Entity Framework`, 使用属性, 管理数据完整性, 使用对象关系映射 (ORM)
- `approaches`, 使用对象关系映射 (ORM)
- `DbContext` 类, 使用属性
- `NuGet package`, 管理数据完整性
- `entity integrity (data integrity)`, 管理数据完整性
- `EntityValidationErrors` 属性, 管理数据完整性

### 目标 2.1: 创建类型
- `enums`, 目标 2.1: 创建类型, 日志和跟踪, 使用事务
- `creating`, 目标 2.1: 创建类型
- `TraceEventType`, 日志和跟踪
- `TransactionScopeOption`, 使用事务

## 异常处理
- `Environment.FailFast` 方法, 处理异常
- `equality operators`, 处理布尔表达式

## 编译指令
- `#error` 指令, 创建和管理编译指令

## 错误处理与验证
- `error handling`, 调试应用程序并实现安全, 目标 3.1: 验证应用程序输入, 目标 3.1: 验证应用程序输入, 管理数据完整性
- `diagnostics`, 分析你的应用程序
- `performance`, 分析你的应用程序
- `validating application input`, 目标 3.1: 验证应用程序输入





# 异常

- `AggregateExceptions`, 使用 `Thread` 类, 使用 async 和 await, 使用并行语言集成查询 (PLINQ)
- 取消任务, 目标 1.5: 实现异常处理, 处理异常, 处理异常, 处理异常
- 抛出异常, 抛出异常, 抛出异常
- 装箱和拆箱, 管理非托管资源
- 使用 `Parse`, `TryParse` 和 `Convert`, 使用 `Parse`, `TryParse` 和 `Convert`, 使用 `Parse`, `TryParse` 和 `Convert`
- 验证 JSON 和 XML, 程序集版本控制
- 目录, 目录

- `ArgumentException`, 验证 JSON 和 XML
- `ArgumentNullException`, 处理异常, 使用 `Parse`, `TryParse` 和 `Convert`
- `DirectoryNotFoundException`, 目录
- `FileNotFoundException`, 程序集版本控制
- `FormatException`, 目标 1.5: 实现异常处理, 使用 `Parse`, `TryParse` 和 `Convert`
- `inspecting`, 处理异常
- `InvalidCastException`, 装箱和拆箱
- `MessageQueueException`, 抛出异常
- `ObjectDisposedException`, 管理非托管资源
- `OperationCanceledException`, 取消任务
- `OverflowException`, 使用 `Parse`, `TryParse` 和 `Convert`
- `popular`, 抛出异常
- `runtime`, 抛出异常
- `ThreadAbortException`, 使用 `Thread` 类
- `throwing`, 处理异常
- `UnauthorizedAccessException`, 目录

## 运算符与方法

- `异异运算符`, 处理布尔表达式
- `ExecuteNonQuery` 方法, 更新数据
- `ExecuteNonQueryAsync` 方法, 更新数据
- `execution context (threads)`, 使用 `Thread` 类
- `ExecutionContext.SuppressFlow` 方法, 使用 `Thread` 类
- `Exists` 方法, 目录
- `ExpandoObject` 类, Office 自动化 API
- `explicit cast operators`, 查询 XML
- `explicit conversions, types`, 隐式转换
- `explicit interface implementations, encapsulation`, 使用属性
- `explicit typing`, 目标 4.3: 使用 LINQ 查询和操作数据及对象

## 动态类型与加密

- `exporting`, 使用动态类型, 在 .NET Framework 中处理加密
- `data to Excel`, `dynamic` 关键字, 使用动态类型
- `public keys`, 在 .NET Framework 中处理加密
- `exposing public events`, 使用 Lambda 表达式
- `expression trees, reflection`, Lambda 表达式

## XML 和 LINQ

- `Extensible Markup Language (XML)`, 使用正则表达式, 创建 WCF 服务, 处理 XML, `XmlReader`](ch04.html_iddle1596), `XmlWriter`](ch04.html_iddle1597), LINQ 如何工作？
- `consuming data`, 创建 WCF 服务, 处理 XML, `XmlReader`](ch04.html_iddle1596), `XmlWriter`](ch04.html_iddle1597)
- `.NET Framework`, 处理 XML
- `XMLDocument` 类, `XmlWriter`](ch04.html_iddle1595)
- `XMLReader` 类, `XmlReader`](ch04.html_iddle1596)
- `XMLWriter`, `XmlWriter`](ch04.html_iddle1597)
- `data validation`, 使用正则表达式
- `LINQ`, LINQ 如何工作？
- `extension methods`, 使用泛型
- `extension methods`, Lambda 表达式
- `fields`, `named arguments`](ch02.html_iddle1587)
- `first in, first out (FIFO) collections`, ConcurrentStack and ConcurrentQueue, 使用队列和栈

## 文件系统与流

- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1583)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1584)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1585)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1586)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1587)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1588)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1589)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1590)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1591)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1592)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1593)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1594)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1595)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1596)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1597)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1598)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1599)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1600)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1601)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1602)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1603)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1604)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1605)
- `File` 类, `Directory` 类, `FileInfo` 类`](ch04.html_iddle1606)
- `FileStream` 类, `异步方法`, 使用 async 和 await
- `FileStream` 类, `创建`, 处理路径`
- `finalization`, `非托管资源`, 理解垃圾回收`
- `finalizers`, 管理非托管资源, 实现 IDisposable 和终结函数`
- `finally blocks`, 处理异常





## 控制流语句

控制流语句，处理布尔表达式, 处理布尔表达式, if 语句, if 语句, switch 语句

条件运算符，if 语句

if 语句，处理布尔表达式

空合并运算符，if 语句

switch 语句，switch 语句

## 循环与集合

for each 循环，遍历集合，foreach 循环

for 循环，遍历集合，遍历集合

For 方法，并行性，使用任务

ForAll 运算符，使用并行语言集成查询 (PLINQ)

ForEach 方法，并行性，使用任务

## 线程与数据

前景线程，使用 Thread 类

外键，管理数据完整性

格式，程序集版本控制，将程序集放入 GAC

FormatException，目标 1.5: 实现异常处理, 使用 Parse, TryParse 和 Convert

字符串格式化，搜索字符串

## 函数式编程与 LINQ

`Func<>` 委托，使用 lambda 表达式

`Func<..>` 类型，Lambda 表达式

函数式构造，创建 XML

功能性，使用反射, 标准 LINQ 查询运算符, LINQ 是如何工作的？, LINQ 是如何工作的？, 创建 XML, 创建 XML, 目标 4.4: 序列化和反序列化数据, 目标 4.4: 序列化和反序列化数据

反序列化（数据），目标 4.4: 序列化和反序列化数据

LINQ，标准 LINQ 查询运算符, LINQ 是如何工作的？, LINQ 是如何工作的？, 创建 XML, 创建 XML

创建 XML，创建 XML

LINQ to XML，LINQ 是如何工作的？

查询 XML，LINQ 是如何工作的？

更新 XML，创建 XML

反射，使用反射

序列化（数据），目标 4.4: 序列化和反序列化数据

函数，值类型和引用类型](#ch02.html_iddle1660)

## G

GAC（全局程序集缓存），部署程序集，将程序集放入 GAC

垃圾回收，目标 2.6: 管理对象周期

第 0 代，垃圾回收，理解垃圾回收

泛型集合，使用数组

泛型类型，创建接口，设计和实现接口

泛型类型，使用泛型类型, Lambda 表达式

创建（Lambda），Lambda 表达式

Nullable 的支持，使用泛型类型

get 和 set 访问器，使用属性

`GetConsuming` 方法，`BlockingCollection<T>`

`GetData` 函数，`WeakReference`，弱引用](#ch02.html_iddle1671)

`GetDirectoryName` 方法，使用路径

`GetEnumerator` 方法，`IEnumerable`, 搜索字符串

`GetExtensions` 方法，使用路径

`GetFileName` 方法，使用路径

`GetHashCode` 方法，使用哈希

`GetInvocationList` 方法，使用事件

`GetObjectData` 方法，使用二进制序列化

`GetOrAdd` 方法，`ConcurrentDictionary`

`GetPathRoot` 方法，使用路径

`GetStringAsync` 方法，使用 async 和 await, `Async/await`

全局程序集缓存 (GAC)，部署程序集，将程序集放入 GAC

全局唯一标识符 (GUID)，管理数据库文件

`goto` 语句，switch 语句

LINQ 分组操作，标准 LINQ 查询运算符

GUID（全局唯一标识符），管理数据库文件

`GZipStream`，编码和解码

## H

处理错误，调试应用程序并实现, 目标 3.1: 验证应用输入, 目标 3.1: 验证应用输入, 管理数据完整性, 使用 Parse, TryParse 和 Convert, 使用正则表达式, 目标回顾, 分析你的应用程序, 分析你的应用程序

诊断，分析你的应用程序, 分析你的应用程序

性能计数器，分析你的应用程序

分析应用程序，分析你的应用程序

日志记录与追踪，目标回顾

验证应用输入，调试应用程序并实现, 目标 3.1: 验证应用输入, 目标 3.1: 验证应用输入, 管理数据完整性, 使用 Parse, TryParse 和 Convert, 使用正则表达式

数据完整性，目标 3.1: 验证应用输入

JSON 和 XML 数据，使用正则表达式

类型转换方法，管理数据完整性

验证原因，目标 3.1: 验证应用输入

正则表达式，使用 Parse, TryParse 和 Convert

处理异常，目标回顾, 处理异常, 抛出异常

自定义异常，抛出异常

抛出异常，处理异常

哈希，在 .NET 框架中使用加密

`Hashtable` 类，使用哈希

堆（类型存储），值类型和引用类型](#ch02.html_iddle1704), 目标 2.6: 管理对象周期

辅助类，类型转换，自定义转换

## I

I/O 操作，使用 Parallel 类, 实现数据访问, 目标 4.1: 执行 I/O 操作, 目标 4.1: 执行 I/O 操作, 目录, 处理文件, 处理路径, 处理路径, 一起使用不同类型的流, 文件系统不仅仅是属于你的, 实现异步 I/O 操作

异步 I/O 操作，实现异步 I/O 操作](#ch04.html_iddle1783)

异步处理，使用 Parallel 类





# 文件基础
- **文件基础**: 目标 4.1: 执行 I/O 操作, 目标 4.1: 执行 I/O 操作, 目录, 文件操作, 路径操作
- **目录**: 目录
- **驱动器**: 目标 4.1: 执行 I/O 操作
- **操纵文件**: 文件操作
- **路径**: 路径操作
- **文件系统**: 共同使用不同类型的流
- **网络通信**: 文件系统不仅仅是为了你
- **流**: 路径操作

# 接口与继承
- **IComparable 接口**: 里氏可替换原则
- **IDisposable 接口**: IEnumerable, 管理未托管资源
- **IEnumerable 接口**: IComparable
- **IEnumerator 接口**: IComparable
- **IFormatProvider 接口**: IFormatProvider 和 IFormattable
- **IFormattable 接口**: 使用辅助类进行转换, IFormatProvider 和 IFormattable

## 程序流与逻辑
- **#if 指令**: 生成配置
- **if 语句**: 使用布尔表达式
- **程序流**: 目标回顾, 目标回顾, 使用布尔表达式, 遍历集合
- **布尔表达式**: 目标回顾
- **决策语句**: 使用布尔表达式

## 实现与数据处理
- **不可变性，字符串**: 目标 2.7: 字符串字符串
- **命令式 CAS**: 使用代码访问权限
- **实现**: 目标回顾, 目标回顾, 使用布尔表达式, 遍历集合, 目标回顾, 处理异常, 抛出异常, 目标 2.4: 创建并实现类层次结构, 调试应用程序并实现安全, 目标回顾, 在 .NET Framework 中处理加密, 目标回顾, 目标 3.4 调试应用程序, 目标回顾, 实现数据访问, 目标回顾, 目标总结, 目标回顾
- **数据访问**: 实现数据访问, 目标回顾, 目标总结, 目标回顾
- **集合**: 目标回顾
- **消费数据**: 目标回顾
- **I/O 操作**: 实现数据访问
- **LINQ**: 目标总结

## 异常处理
- **异常处理**: 目标回顾, 处理异常, 抛出异常
- **自定义异常**: 抛出异常
- **抛出异常**: 处理异常

## 类层次结构与安全
- **接口**: 目标 2.4: 创建并实现类层次结构
- **遍历集合**: 遍历集合
- **安全**: 调试应用程序并实现安全, 目标回顾, 里氏可替换原则, 目标 3.4 调试应用程序, 目标回顾
- **程序集管理**: 目标回顾
- **调试应用程序**: 目标 3.4 调试应用程序
- **诊断**: 目标回顾
- **加密**: 目标回顾
- **输入验证**: 调试应用程序并实现安全
- **集合**: 在 .NET Framework 中处理加密
- **隐式转换，类型**: 装箱和拆箱
- **隐式类型变量，LINQ**: 目标 4.3 使用 LINQ 查询和处理数据
- **增量运算符**: volatile 类
- **索引器**: 添加数据
- **IndexOf 方法**: 搜索字符串

## 详细文件操作
- **基础，文件**: 目标 4.1: 执行 I/O 操作, 目标 4.1: 执行 I/O 操作, 目录, 文件操作, 路径操作
- **目录**: 目录
- **驱动器**: 目标 4.1: 执行 I/O 操作
- **操纵文件**: 文件操作
- **路径**: 路径操作

## 继承与多态
- **继承**: 继承层次结构中的访问受保护, 目标回顾, 目标 2.4: 创建并实现类层次结构, 使用基类, 抽象和密封基类, 里氏可替换原则
- **类层次结构**: 目标回顾, 目标 2.4: 创建并实现类层次结构, 使用基类, 里氏可替换原则
- **.NET Framework 标准接口**: 里氏可替换原则
- **基类**: 使用基类
- **设计与实现接口**: 目标 2.4: 创建并实现类层次结构
- **里氏可替换原则**: 抽象和密封基类
- **protected 访问修符**: 继承层次结构中的访问受保护

## 输入与验证
- **初始化向量 (IV)**: 使用对称和非对称加密
- **InnerExceptions 属性**: 使用并行语言查询 (PLINQ)
- **普通用户**: 目标 3.1: 验证应用程序输入
- **输入（应用程序），验证**: 调试应用程序并实现安全, 目标 3.1: 验证应用程序输入, 目标 3.1: 验证应用程序输入, 管理数据完整性, 使用 Parse, TryParse 和 Convert, 使用正则表达式
- **数据完整性**: 目标 3.1: 验证应用程序输入
- **JSON 和 XML 数据**: 使用正则表达式
- **类型转换方法**: 管理数据完整性
- **验证原因**: 目标 3.1: 验证应用程序输入
- **正则表达式**: 使用 Parse, TryParse 和 Convert
- **输入/输出操作**: 实现数据访问（查看 I/O 操作）

## 高级主题
- **检查异常**: 处理异常
- **实例化具体类型，接口实现**: 设计与实现接口
- **实例化委托**: 理解委托
- **插桩方法，分析应用程序**: 分析您的应用程序





### `int.Parse` 方法，目标 1.5：实现异常处理

### `interfaces`，使用辅助类进行转换, 使用属性, 目标 2.4：创建并实现类层次结构, 里氏夫替换原则, 使用反射, 管理非托管资源, `IFormatProvider` 和 `IFormattable`, `IFormatProvider` 和 `IFormattable`, 使用二进制序列化

### `.NET Framework`，里氏夫替换原则

### 设计与实现，目标 2.4：创建并实现类层次结构

### `encapsulation`，使用属性

### `IDisposable`，管理非托管资源

### `IFormatProvider`，`IFormatProvider` 和 `IFormattable`

### `IFormattable`，使用辅助类进行转换, `IFormatProvider` 和 `IFormattable`

### `IPlugin`，使用反射

### `ISerializable`，使用二进制序列化

### `Interlocked` 类，为多线程应用程序同步资源，`Volatile` 类

### `internal` 访问修饰，在继承层次结构中保护可访问性

### `InternalsVisibleToAttribute` 特性，保持类型对程序内部

### `InvalidCastException`，装箱和拆箱

### `Invoke` 方法，并行性，使用任务

### `IPlugin` 接口，使用反射

### `is` 运算符，使用辅助类进行转换

### `IsDefined` 方法，读取属性

### `ISerializable` 接口，使用二进制序列化

### `Isolation` 属性（事务），使用参数

### 遍历集合，遍历集合, 遍历集合, while 和 do-while 循环, foreach 循环, foreach 循环

### for each 循环，foreach 循环

### for 循环，遍历集合

### 跳转语句，foreach 循环

### while 和 do-while 循环，while 和 do-while 循环

### 迭代器模式，标准 LINQ 查询操作符

### `IUnknown` 接口，`IUnknown`

### `IV`（初始化向量），使用对称和非对称加密

### `IXPathNavigable` 接口，`XmlDocument`

### J

### 锯齿数组，目标 4.5：在集合中存储和从中检索数据

### JavaScript 对象表示法 (JSON)，使用正则表达式, `XmlDocument`

### 消费数据，`XmlDocument`

### 数据验证，使用正则表达式

### `JavaScriptSerializer`，验证 JSON 和 XML](#ch03.html_iddle1810)

### 连接操作符，标准 LINQ 查询操作符

### JSON (JavaScript 对象表示法)，使用正则表达式, `XmlDocument`

### 消费数据，`XmlDocument`

### 数据验证，使用正则表达式

### JSON 序列化，使用 DataContract

### 跳跃语句，遍历集合，foreach 循环

### K

### 密钥容器，存储密钥，在 .NET Framework 中处理加密

### 密钥，算法，使用对称和非对称加密

### 关键字，值类型和引用类型](#ch02.html_iddle1822), 扩展方法, 使用动态类型, `IEnumerable`, 实现异步 I/O 操作](#ch04.html_iddle118), 实现异步 I/O 操作](#ch04.html_iddle1819), 目标 4.3：使用 LINQ 查询和处理数据与对象

### `async`，实现异步 I/O 操作](#ch04.html_iddle118)

### `await`，实现异步 I/O 操作](#ch04.html_iddle1819)

### `dynamic`，使用动态类型

### `sealed`，扩展方法

### `struct`，值类型和引用类型

### `var`，目标 4.3：使用 LINQ 查询和处理数据与对象

### `yield``IEnumerable`

### L

### lambda 表达式，理解委托](#ch01.html_iddle1825), lambda 表达式, 对象初始化语法

### LINQ，对象初始化语法](#ch04.html_iddle1826)

### 反射，lambda 表达式](#ch02.html_iddle1827)

### 语言特性，LINQ，目标 4.3：使用 LINQ 查询和处理数据与对象, 目标 4.3：使用 LINQ 查询和处理数据与对象, 隐式类型变量, 对象初始化语法, lambda 表达式, lambda 表达式

### 匿名类型，lambda 表达式](#ch04.html_iddle1829)

### 扩展方法，lambda 表达式](#ch04.html_iddle1830)

### 隐式类型变量，目标 4.3：使用 LINQ 查询和处理数据与对象

### lambda 表达式，对象初始化语法](#ch04.html_iddle1832)

### 对象初始化语法，隐式类型变量](#ch04.html_iddle1833)

### 集成查询，使用 async and await

### 后进先出 (LIFO) 集合，`ConcurrentStack and ConcurrentQueue`, 使用队列和栈

### `LastIndexOf` 方法，搜索字符串

### LIFO（后进先出）集合，`ConcurrentStack and ConcurrentQueue`, 使用队列和栈

### #line 指令，创建和管理编译器指令

### LINQ (集成查询)，使用 async and await, 扩展方法, 目标总结, 目标 4.3：使用 LINQ 查询和处理数据与对象, 目标 4.3：使用 LINQ 查询和处理数据与对象, 隐式类型变量, 对象初始化语法, lambda 表达式, lambda 表达式, 匿名类型, 标准 LINQ 查询操作符, LINQ 如何工作？, LINQ 如何工作？, 创建 XML`, 创建 XML`

### 功能性，标准 LINQ 查询操作符, LINQ 如何工作？, LINQ 如何工作？, 创建 XML`, 创建 XML`

### 创建 XML，创建 XML

### LINQ to XML，LINQ 如何工作？

### 查询 XML，LINQ 如何工作？

### 更新 XML，创建 XML





# 语言特性

- 目标 4.3：使用 LINQ 查询和操作数据及对象
- 目标 4.3：使用 LINQ 查询和操作数据及对象
- 隐式类型变量
- 对象初始化语法
- Lambda 表达式
- Lambda 表达式
- 匿名类型、Lambda 表达式
- 扩展方法、Lambda 表达式
- 隐式类型变量、目标 4.3：使用 LINQ 查询和操作数据及对象
- lambda 表达式、对象初始化语法
- 对象初始化语法、隐式类型变量
- 查询、匿名类型
- LINQPad、标准 LINQ 查询操作符
- Liskov 原则、抽象和密封基类
- `List` 类、使用 List
- `List` 集合、数据访问、使用数组
- `List<T>` 集合类型、添加某些数据
- `Listeners` 属性、`TraceSource` 类、日志记录和跟踪
- `lock` 操作符、同步资源
- `lock` 语句、同步、同步资源
- 日志记录策略、目标回顾
- 长期任务、`CancellationToken`、`Interlocked` 类
- 循环、遍历集合、遍历集合、`while` 和 do-while 循环、`while` 和 do-while 循环、`foreach` 循环
- do-while、`while` 和 do-while 循环
- for each 循环、`foreach` 循环
- for 循环、遍历集合
- while、`while` 和 do-while 循环

# M

- 配置文件、程序集版本控制
- 主版本（程序集）、程序集版本控制
- `Makecert.exe` 工具、管理和创建证书
- 恶意用户、目标 3.1：验证应用程序输入
- 托管扩展框架 (MEF)、使用反射
- 管理、目标 1.1：实现多线程和异步处理、目标回顾、目标 1.4：创建和实现事件与回调、目标回顾、目标 2.6：管理对象生命周期、目标 2.6：管理对象生命周期、理解垃圾回收、目标回顾、什么是程序集？、使用强名称签名程序集、将程序集放入 GAC、将程序集放入 GAC、程序集版本控制、生成配置、创建和管理编译器指令
- 程序集、目标回顾、什么是程序集？、使用强名称签名程序集、将程序集放入 GAC、将程序集放入 GAC、程序集版本控制
- 创建 WinMD 程序集、程序集版本控制
- 定义程序集、什么是程序集？
- 将程序集放入 GAC、将程序集放入 GAC
- 使用强名称签名、使用强名称签名程序集
- 程序集版本控制、将程序集放入 GAC
- 编译器指令、生成配置
- 对象生命周期、目标 2.6：管理对象生命周期、目标 2.6：管理对象生命周期、理解垃圾回收
- 垃圾回收、目标 2.6：管理对象生命周期
- 非托管资源、理解垃圾回收
- PDB 文件和符号、创建和管理编译器指令
- 程序流、目标 1.1：实现多线程和异步处理、目标回顾、目标 1.4：创建和实现事件与回调、目标回顾
- 异常处理、目标 1.4：创建和实现事件与回调
- 管理多线程、目标回顾
- 多线程应用、目标 1.1：实现多线程和异步处理
- 操作字符串、目标回顾、目标 2.7：操作字符串、使用 .NET 框架中的字符串、字符串、字符串
- 类、使用 .NET 框架中的字符串
- 举举、字符串
- 格式化、字符串
- 查找字符串、字符串
- 手动引发事件、目标 1.4：创建和实现事件与回调
- `Marshal` 类、字符串数据
- MEF (托管扩展框架)、使用反射
- 内存管理、垃圾回收、目标 2.6：管理对象生命周期（见垃圾回收）
- `MessageQueueException`、抛出异常
- 元数据、反射、目标 2.5：通过反射运行时查找并创建类型、目标 2.5：通过反射运行时查找并创建类型、使用反射](#ch02.html_iddle1905)、使用反射](#ch02.html_iddle1903)、Lambda 表达式](#ch02.html_iddle1904)、Lambda 表达式](#ch02.html_iddle1906)
- 特性、目标 2.5：通过反射运行时查找并创建类型
- CodeDOM、使用反射
- 表达式树、Lambda 表达式
- 功能、使用反射





# 方法

- 使用 Thread 类
- 使用 Thread 类
- 使用 Thread 类
- 使用 Thread 类
- 使用 Tasks
- 使用 Tasks
- 使用 Tasks
- 使用 Tasks
- 使用 Tasks
- 使用 Tasks
- 使用 Tasks
- 使用 Parallel 类
- 使用 Parallel 类
- 使用 async and await
- 使用 async and await
- 使用 async and await
- 使用 async and await
- 使用 async and await
- 使用并行语言集成查询 (PLINQ)
- 使用并行语言集成查询 (PLINQ)
- 使用并行语言集成查询 (PLINQ)
- BlockingCollection<T>
- BlockingCollection<T>
- BlockingCollection<T>
- BlockingCollection<T>
- ConcurrentStack and ConcurrentQueue
- ConcurrentStack and ConcurrentQueue
- ConcurrentStack and ConcurrentQueue
- ConcurrentStack and ConcurrentQueue
- ConcurrentStack and ConcurrentQueue
- ConcurrentStack and ConcurrentQueue
- ConcurrentDictionary
- ConcurrentDictionary
- ConcurrentDictionary
- ConcurrentDictionary
- Volatile class
- Volatile class
- The Interlocked class
- The Interlocked class
- Canceling tasks
- Using lambda expressions
- Using lambda expressions
- Using events
- 目标 1.5: 实现异常处理
- Handling exceptions
- Throwing exceptions
- Value and reference types
- Value and reference types
- Adding behaviors
- Adding behaviors
- Adding behaviors
- Named arguments, optional arguments, and overloading visibility
- Adding some data
- Extension methods
- Objective 2.2: Consume types
- User-defined conversions
- User-defined conversions
- Creating and using base classes
- Liskov substitution principle
- IEnumerable
- IEnumerable
- Reading attributes
- Lambda expressions
- StringWriter and StringReader
- Searching for strings
- Searching for strings
- Searching for strings
- Searching for strings
- Searching for strings
- Formatting strings
- Managing data
- Working with encryption in the .NET Framework
- Using hashing
- Using hashing
- Managing and creating certificates
- Managing and creating certificates
- Securing string data
- Directories
- Directories
- Working with paths
- Working with paths
- Working with paths
- Working with paths
- The base Stream class
- The file system is not just for you
- Async/await
- Async/await
- Updating data
- Updating data
- How does LINQ work?
- How does LINQ work?
- Querying XML
- Querying XML
- Using binary
- Using queues and stacks
- Using queues and stacks
- Using queues and stacks
- Using queues and stacks
- adding behaviors to classes (ch02.html_iddle1907)
- Value and reference types (ch02.html_iddle1907)
- AddOrUpdate (ch01.html_iddle1908)
- Lambda expressions (ch02.html_iddle1909)
- AsParallel, Using async and await (ch01.html_iddle1910)
- Parallel Language Query (PLINQ) (ch01.html_iddle1911)
- Securing string data (ch03.html_iddle1912)
- Querying XML (ch04.html_iddle1913)
- Adding behaviors (ch02.html_iddle1914)
- The Interlocked class (ch01.html_iddle1915)
- Canceling tasks (ch01.html_iddle1916)
- Working with paths (ch04.html_iddle1917)
- The Interlocked class (ch01.html_iddle1918)
- Liskov substitution principle (ch02.html_iddle1919)
- BlockingCollection<T> (ch01.html_iddle1920)
- ConcurrentDictionary collections (ch01.html_iddle1921)
- ConfigureAwait (ch01.html_iddle1922)
- Using hashing (ch03.html_iddle1923)
- Using Tasks (ch01.html_iddle1924)
- The file system is not just for you (ch04.html_iddle1925)
- Using lambda expressions (ch01.html_iddle1926)
- The base Stream class (ch04.html_iddle1927)
- Adding behaviors (ch02.html_iddle1928)
- Using queues and stacks (ch04.html_iddle1929)
- Descendants (ch04.html_iddle1930)
- Searching for strings (ch02.html_iddle1931)
- ConcurrentStack and ConcurrentQueue (ch01.html_iddle1932)
- Using queues and stacks (ch04.html_iddle1933)
- Handling exceptions (ch01.html_iddle1934)
- Throwing exceptions (ch01.html_iddle1935)
- ExecuteNonQuery (ch04.html_iddle1936)
- ExecuteNonQueryAsync (ch04.html_iddle1937)
- ExecutionContext.SuppressFlow (ch01.html_iddle1938)
- Directories (ch04.html_iddle1939)
- Using Tasks (ch01.html_iddle1940)
- ForEach, parallelism, Using Tasks (ch01.html_iddle1941)
- Value and reference types (ch02.html_iddle1942)
- BlockingCollection<T> (ch01.html_iddle1943)
- Working with paths (ch04.html_iddle1944)
- Using hashing (ch03.html_iddle1949)
- Using Tasks (ch01.html_iddle1948)
- Using events (ch01.html_iddle1950)
- Using binary (ch04.html_iddle1951)
- Volatile class collections (ch01.html_iddle1952)
- Using async and await (ch01.html_iddle1954)
- Async/await (ch04.html_iddle1955)
- Searching for strings (ch02.html_iddle1956)
- Searching for strings (ch02.html_iddle1960)
- Reading attributes (ch02.html_iddle1959)
- Using Parallel class (ch01.html_iddle1966)
- Extension methods (ch02.html_iddle1964)
- Using Parallel class (ch01.html_iddle1967)
- Adding behaviors (ch02.html_iddle1968)
- ConcurrentStack and ConcurrentQueue (ch01.html_iddle1972)
- Using queues and stacks (ch04.html_iddle1973)
- Using lambda expressions (ch01.html_iddle1975)
- Volatile class (ch01.html_iddle1976)
- Using async and await (ch01.html_iddle1977)
- Searching for strings (ch02.html_iddle1978)
- Managing and creating certificates (ch03.html_iddle1979)
- Searching for strings (ch02.html_iddle1980)
- Adding some data (ch02.html_iddle1981)
- Formatting strings (ch02.html_iddle1987)
- Managing data (ch03.html_iddle1996)
- BlockingCollection<T> (ch01.html_iddle1991)
- User-defined conversions (ch02.html_iddle1990)
- ConcurrentDictionary (ch01.html_iddle1995)
- Creating and using base classes (ch02.html_iddle1965)
- Managing and creating certificates (ch03.html_iddle1997)
- Using Tasks (ch01.html_iddle1998)
- Using Tasks (ch01.html_iddle1999)
- Using Tasks (ch01.html_iddle2000)
- Using Parallel Language Integrated Query (PLINQ) (ch01.html_iddle2001)
- Using Parallel Language Integrated Query (PLINQ) (ch01.html_iddle2002)
- Async/await (ch04.html_iddle2005)
- StringWriter and StringReader (ch02.html_iddle2006)




# 目录
- `IsDefined`, 读取属性
- `LastIndexOf`, 查找字符串
- `MoveNext`, IEnumerable, LINQ 是如何工作的？
- `MoveTo`, 目录
- `overriding`, 扩展方法, 创建和使用基类
- `Parallel.Break`, 使用 Parallel 类
- `Parallel.Stop`, 使用 Parallel 类
- `parameters`, 添加行为
- `Parse`, 自定义转换
- `Peek`, 使用队列和栈
- `Pop`, 使用队列和栈
- `Push`, ConcurrentStack 和 ConcurrentQueue, 使用队列和栈
- `PushRange`, ConcurrentStack 和 ConcurrentQueue
- `Raise`, 使用 lambda 表达式
- `Read`, Volatile 类
- `ReadAsync`, 使用 async 和 await
- `returning data`, 命名参数、可选参数和重载可见性
- `SignHash`, 管理和创建证书
- `StartsWith`, 查找字符串
- `static`, 添加一些数据
- `string.Concat`, 目标 2.2: 消费类型
- `t.Join`, 使用 Thread 类
- `Thread.Abort`, 使用 Thread 类
- `Thread.Join`, 使用 Thread 类
- `ToList`, LINQ 是如何工作的？
- `ToString`, 格式化字符串
- `ToXmlString`, 在 .NET Framework 中处理加密
- `TryDequeue`, ConcurrentStack 和 ConcurrentQueue
- `TryParse`, 自定义转换
- `TryPeek`, BlockingCollection<T>
- `TryPop`, ConcurrentStack 和 ConcurrentQueue
- `TryPopRange`, ConcurrentStack 和 ConcurrentQueue
- `TryTake`, BlockingCollection<T>
- `TryUpdate`, ConcurrentDictionary
- `type conversions`, 管理数据完整性
- `VerifyHash`, 管理和创建证书
- `WaitAll`, 使用 Tasks
- `WaitAny`, 使用 Tasks
- `WhenAll`, 使用 Tasks
- `WithDegreeOfParallelism`, 使用并行语言查询 (PLINQ)
- `WithExecutionMode`, 使用并行语言查询 (PLINQ)
- `Write`, Volatile 类
- `WriteAsync`, 使用 async 和 await, Async/await
- `XmlWriter.Create`, StringWriter 和 StringReader
- `Minor Version (assembly)`, 程序集版本控制
- `Model First approach (Entity Framework )`, 使用对象关系映射器 (ORM)
- `Modules window`, 管理程序数据库文件和符号
- `MoveNext method`, IEnumerable, LINQ 是如何工作的？
- `MoveTo method`, 目录
- `moving files`, 处理文件
- `multicasting delegates`, 理解委托
- `multidimensional arrays`, 目标 4.5: 在集合中存储数据并从集合中检索数据
- `multiple inheritance`, 使用接口
- `multithreaded applications`, 目标 1.1: 实现多线程和异步处理, 目标 1.1: 实现多线程和异步处理, 理解线程, 使用 Thread 类
- `thread pools`, 使用 Thread 类
- `Thread class`, 理解线程
- `thread pools`, 使用 Thread 类
- `arguments`, 添加行为
- `namespaces`, 理解线程
- `System.Threading`, 理解线程
- `Parallel class`, 使用 Tasks
- `Thread class`, 理解线程
- `.NET Framework`, 使用 Office API
- `encryption`, 使用对称和异步加密
- `Nullables`, 使用泛型
- `standard interfaces`, Liskov 替换原则
- `strings`, 目标 2.7: 处理字符串
- `TraceListeners`, 日志和跟踪
- `transactions`, 使用参数
- `XmlSerializer`, 使用 XmlSerializer
- `asynchronous processing`, 使用 Parallel 类
- `concurrent collections`, 使用并行语言查询 (PLINQ)
- `Parallel class`, 使用 Tasks
- `PLINQ`, 使用 async 和 await
- `synchronizing resources`, 同步资源, `Volatile class`](ch01.html_iddle2022)
- `Interlocked class`, `Volatile class`](ch01.html_iddle2022)
- `binary serialization`, 使用二进制序列化
- `built-in types`, 管理数据完整性
- `consuming XML`, 使用 XML
- `creating web services`, 使用对象关系映射器 (ORM)
- `data access code`, 处理数据库
- `database providers`, 处理数据库
- `DataContract`, 使用二进制序列化





# `NuGet`, 管理数据完整性
# `null 合并运算符`, if 语句
# `可空类型`, 使用泛型类型
# `NumberOfItems32` (性能计数器), 创建和监控性能计数器
# `NumberOfItems64` (性能计数器), 创建和监控性能计数器

## O

- `对象构造函数`, 添加一些数据
- `对象初始化语法`, `LINQ`, 隐式类型变量
- `对象生命周期，管理`, 目标 2.6: 管理对象的生命周期, 目标 2.6: 管理对象的生命周期, 理解垃圾回收
- `垃圾回收`, 目标 2.6: 管理对象的生命周期
- `未托管资源`, 理解垃圾回收
- `对象关系映射 (ORM)`, 使用事务
- `对象-关系阻抗不匹配`, 使用事务
- `ObjectDisposedException`, 管理未托管资源
- `对象`, 使用 Parallel 类, 目标 2.3: 强制封装, 目录, 处理文件, 连接数据库, XmlWriter`, 目标 4.4: 序列化和反序列化数据
- `循环引用`, 目标 4.4: 序列化和反序列化数据
- `DirectoryInfo`, 目录
- `封装`, 目标 2.3: 强制封装 (参见封装)
- `FileInfo`, 处理文件
- `ParallelLoopState`, 使用 Parallel 类
- `SqlCommand`, 连接数据库
- `XmlNode`, XmlWriter`
- `Office 自动化 API`, 使用动态类型
- `OnChange 属性`, 使用 lambda 表达式
- `OnDeserializedAttribute`, 使用二进制序列化
- `OnDeserializingAttribute`, 使用二进制序列化
- `OnSerializedAttribute`, 使用二进制序列化
- `OnSerializingAttribute`, 使用二进制序列化
- `OperationCanceledException`, 取消任务
- `OperationContract 特性`, 使用对象关系映射 (ORM)
- `运算符`, Volatile 类, Volatile 类, 处理布尔表达式, 处理布尔表达式, 处理布尔表达式, 处理布尔表达式, 使用辅助类进行转换, 使用辅助类进行转换, 标准 LINQ 查询运算符, 查询 XML`, 查询 XML`, 查询 XML`
- `AND`, 处理布尔表达式
- `as`, 使用辅助类进行转换
- `Decrement`, Volatile 类
- `相等性`, 处理布尔表达式
- `异或`, 处理布尔表达式
- `显式类型转换`, 查询 XML`
- `Increment`, Volatile 类
- `is`, 使用辅助类进行转换
- `OR`, 处理布尔表达式
- `OrderBy`, 查询 XML`
- `标准 LINQ 查询运算符`, 标准 LINQ 查询运算符
- `Where`, 查询 XML`
- `可选参数`, 添加行为
- `OptionalField 特性`, 使用二进制序列化 (注：此处原文链接可能对应属性，已按逻辑翻译)
- `OracleConnectionString 类`, 连接数据库
- `OrderBy 运算符`, 查询 XML`
- `有序并行查询`, 并行语言查询 (PLINQ)
- `OrderProcessingException`, 抛出异常
- `ORM (对象关系映射)`, 使用事务
- `OverflowException`, 解析和转换`
- `重载`, 添加行为
- `重写方法`, 创建基类
- `分页`, 标准 LINQ 查询运算符
- `并行`, 处理 I/O 操作
- `Parallel 类，多线程`, 使用任务
- `并行语言查询 (PLINQ)`, 使用和等待
- `并行查询`, 使用和等待
- `并行性`, 使用和等待
- `Parallel.Break 方法`, 使用类
- `Parallel.Stop 方法`, 使用类
- `参数化 SQL 语句`, 使用参数
- `参数化 ThreadStart 委托`, 使用类
- `父类`, 创建基类
- `父任务，将子任务附加`, 使用任务
- `Parse 方法`, 用户定义转换`
- `部分签名，程序集`, 使用强名称签名程序集
- `Path 类`, 处理路径
- `路径，文件`, 处理路径
- `PDB (程序数据库)文件`, 创建和管理编译器指令
- `PDBCopy 工具`, 管理程序数据库文件和符号
- `Peek 方法`, 使用队列和栈`
- `性能`, 使用对称和非对称加密
- `计数器`, 分析你的应用程序





- 权限，代码访问，管理和创建证书
- PIA（主互操作程序集），与 COM 集成，使用动态类型
- PKI（公密钥基础设施），管理和创建证书
- PLINQ（并行语言集成查询），使用 async 和 await
- 指针类型，目标 2.1: 创建类型
- 池化，连接，连接到数据库
- Pop 方法，使用队列和栈
- 常见异常，抛出异常
- #pragma warning 指令，创建和管理编译器指令
- 预处理器指令，生成配置
- 主互操作程序集 (PIA)，与 COM 集成，使用动态类型
- 主键，管理数据完整性
- private 访问修饰符，使用 private 隐藏内容
- 私有算法，使用对称和非对称加密
- 私有密钥，强名称程序集，使用强名称签名程序集
- 私有符号文件，管理程序数据库文件和符号
- 探测节，定位程序集，程序集版本控制
- 过程化代码，更新 XML，更新 XML
- 应用程序性能分析，分析你的应用程序
- 性能分析工具，分析你的应用程序
- 程序流，目标 1.1: 实现多线程和异步处理, 目标 1.1: 实现多线程和异步处理, 线程池, 使用 Tasks, 使用 Parallel 类, 使用 async 和 await, 使用并行语言集成查询 (PLINQ), 目标复, Interlocked 类, 目标复, 目标复, 处理布尔表达式, 遍历集合, 目标 1.4: 创建和实现事件与回调, 目标 1.4: 创建和实现事件与回调, 理解委托, 使用 lambda 表达式, 目标复, 处理异常, 抛出异常
- 事件和回调，目标 1.4: 创建和实现事件与回调, 目标 1.4: 创建和实现事件与回调, 理解委托, 使用 lambda 表达式
- 委托，目标 1.4: 创建和实现事件与回调
- lambda 表达式，理解委托
- 使用事件，使用 lambda 表达式
- 异常处理，目标复, 处理异常, 抛出异常
- 自定义异常，抛出异常
- 抛出异常，处理异常
- 实现实现，目标复, 目标复, 处理布尔表达式, 遍历集合
- 布尔表达式，目标复
- 决策语句，处理布尔表达式
- 遍历集合，遍历集合
- 多线程应用，目标 1.1: 实现多线程和异步处理, 目标 1.1: 实现多线程和异步处理, 线程池, 使用 Tasks, 使用 Parallel 类, 使用 async 和 await, 使用并行语言集成查询 (PLINQ), 目标复, Interlocked 类
- 异步处理，使用 Parallel 类
- 取消任务，Interlocked 类
- 并发集合，使用并行语言集成查询 (PLINQ)
- Parallel 类，使用 Tasks
- PLINQ，使用 async 和 await
- 同步资源，目标复
- 任务，线程池
- 线程，目标 1.1: 实现多线程和异步处理
- LINQ 操作，标准 LINQ 运算符
- 序言，创建 WCF 服务
- 属性，使用并行语言集成查询 (PLINQ), 使用 lambda 表达式, 使用 lambda 表达式, 处理异常, 将类型设为程序集内部, 将类型设为程序集内部, 使用属性
- 自动实现，使用属性
- CreateandRaise，使用 lambda 表达式
- 创建，将类型设为程序集内部
- 强制封装，将类型设为程序集内部
- 内部异常，使用并行语言集成查询 (PLINQ)
- OnChange，使用 lambda 表达式
- `System.Exception` 类，处理异常
- protected 访问修饰符，保护继承层次中的访问权限
- 保护应用程序，目标复
- 提供程序，数据库，处理数据库
- public 访问修饰符，目标 2.3: 强制封装
- 公有算法，使用对称和非对称加密
- 公有事件暴露，使用 lambda 表达式
- 公密钥基础设施 (PKI)，管理和创建证书
- 公钥，在 .NET Framework 中处理加密, 使用强名称签名程序集
- 导出，在 .NET Framework 中处理加密
- 强名称程序集，使用强名称签名程序集
- 公有符号文件，管理程序数据库文件和符号
- 发布-订阅设计模式，使用 lambda 表达式
- 发布者策略文件，程序集版本控制
- Push 方法，ConcurrentStack 和 ConcurrentQueue, 使用队列和栈
- PushRange 方法，ConcurrentStack 和 ConcurrentQueue

### Q
- 查询，使用 async and await, 使用 async and await, 使用 async and await, 连接到数据库, 匿名类型
- 转换为并行查询，使用 async and await
- 数据库，连接到数据库
- LINQ，匿名类型





LINQ (语言集成查询),使用 async 和 await

PLINQ (并行语言集成查询),使用 async 和 await

查询语法，匿名类型

`Queue` 类，使用队列和栈

队列，`ConcurrentStack` 和 `ConcurrentQueue`](ch01.html_iddle2212), 使用队列和栈

数据访问集合，使用队列和栈

FIFO（先进先出）集合，`ConcurrentStack` 和 `ConcurrentQueue`](ch01.html_iddle2212)

将工作排入线程池，使用 `Thread` 类

### R

`Raise` 方法，使用 lambda 表达式

引发事件，使用事件, 使用事件

异常，使用事件

手动，使用事件

`RanToCompletion` 状态，取消任务

`RateOfCountsPerSecond32`（性能计数器），创建和监控性能计数器

`RateOfCountsPerSecond64`（性能计数器），创建和监控性能计数器

`Read` 方法，`Volatile` 类`

`ReadAsync` 方法，使用 async 和 await

读取，应用属性, 处理路径, 连接数据库

属性，应用属性

数据，数据库，连接数据库

从流中，处理路径

引用类型，创建，创建枚举

参照完整完整性（数据完整性），管理数据完整性

反射，目标 2.5: 使用反射在运行时查找、执行并创建类型, 目标 2.5: 使用反射在运行时查找、执行并创建类型, 使用反射, 使用反射, Lambda 表达式, Lambda 表达式

属性，目标 2.5: 使用反射在运行时查找、执行并创建类型

`CodeDOM`,使用反射

表达式树，Lambda 表达式

功能，使用反射

lambda 表达式，Lambda 表达式

`ReflectionPermission`,使用代码访问权限

正则表达式，使用 Parse, TryParse 和 Convert（参见正则表达式）

常规程序集，使用强名称签名程序集, 使用强名称签名程序集

正则表达式，验证应用程序输入，使用 Parse, TryParse 和 Convert

发布生成，生成配置

发布模式默认生成配置，目标 3.4 调试应用程序

`Repository` 基类，创建和使用基类

资源竞争数据方法，分析应用程序，分析您的应用程序

资源同步，多线程，目标回顾, 同步资源, `Volatile` 类`

`Interlocked` 类，`Volatile` 类`

`Volatile` 类，同步资源

`Resume` 选项（`TraceEventType` 枚举），日志和跟踪

重新抛出异常，处理异常

返回值（任务），使用 Tasks

返回数据，方法，命名参数、可选参数和重载可见性

`Revision`（程序集），程序集集](#ch03.html_iddle2249)

权限，代码访问权限，管理和创建证书

`RSACryptoServiceProvider` 类，在 .NET Framework 中加密

运行时异常，抛出异常](#ch01.html_iddle2252)

运行时，反射，目标 2.5: 使用反射在运行时查找、执行并创建类型, 目标 2.5: 使用反射在运行时查找、执行并创建类型, 使用反射, 使用反射, Lambda 表达式, Lambda 表达式

属性，目标 2.5: 使用反射在运行时查找、执行并创建类型

`CodeDOM`,使用反射

表达式树，Lambda 表达式

功能，使用反射

lambda 表达式，Lambda 表达式

`ReflectionPermission`,使用代码访问权限

正则表达式，使用 Parse, TryParse 和 Convert（参见正则表达式）

常规程序集，使用强名称签名程序集, 使用强名称签名程序集

正则表达式，验证应用程序输入，使用 Parse, TryParse 和 Convert

发布生成，生成配置

发布模式默认生成配置，目标 3.4 调试应用程序

`Repository` 基类，创建和使用基类

资源竞争数据方法，分析应用程序，分析您的应用程序

资源同步，多线程，目标回顾, 同步资源, `Volatile` 类`

`Interlocked` 类，`Volatile` 类`

`Volatile` 类，同步资源

`Resume` 选项（`TraceEventType` 枚举），日志和跟踪

重新抛出异常，处理异常

返回值（任务），使用 Tasks

返回数据，方法，命名参数、可选参数和重载可见性

`Revision`（程序集），程序集版本](#ch03.html_iddle2249)

权限，代码访问权限，管理和创建证书

`RSACryptoServiceProvider` 类，在 .NET Framework 中加密

运行时异常，抛出异常](#ch01.html_iddle2252)

运行时，反射，目标 2.5: 使用反射在运行时查找、执行并创建类型, 目标 2.5: 使用反射在运行时查找、执行并创建类型, 使用反射, 使用反射, Lambda 表达式, Lambda 表达式





# 编译器指令与配置

- 编译器指令，生成配置
- 配置，目标 3.4 调试应用程序
- PDB 文件和符号，创建和管理编译器指令
- 诊断信息，目标回顾, 目标回顾, 分析你的应用程序, 分析你的应用程序
- 日志与跟踪，目标回顾
- 性能计数器，分析你的应用程序
- 应用程序分析，分析你的应用程序

# 加密与安全

- 加密，目标回顾, 使用对称和非对称加密, 使用对称和非对称加密, 在 .NET Framework 中处理加密, 管理和创建证书, 管理和创建证书, 使用代码访问权限
- .NET Framework，使用对称和非对称加密
- 代码访问权限，管理和创建证书
- 数字证书，管理和创建证书
- 哈希处理，在 .NET Framework 中处理加密
- 字符串数据保护，使用代码访问权限
- 对称和非对称加密，使用对称和非对称加密
- 验证应用程序输入，调试应用程序并实现安全, 目标 3.1: 验证应用程序输入, 目标 3.1: 验证应用程序输入, 管理数据完整性, 使用 Parse, TryParse 和 Convert, 使用正则表达式
- 数据完整性，目标 3.1: 验证应用程序输入
- JSON 和 XML 数据，使用正则表达式
- 类型间转换的方法，管理数据完整性
- 验证的原因，目标 3.1: 验证应用程序输入
- 正则表达式，使用 Parse, TryParse 和 Convert

# 安全属性

- SecurityPermission，使用代码访问权限
- SecurityPermission 属性，使用二进制序列化

# 序列化与数据访问

- 寻寻流，处理路径
- 顺序并行查询，使用并行语言集成查询 (PLINQ)
- SerializableAttribute 属性，目标 2.5: 使用反射在运行时查找、执行和创建类型
- 序列化（数据），目标 4.4: 序列化和反序列化数据, 目标 4.4: 序列化和反序列化数据, 使用 XmlSerializer, 使用二进制序列化, 使用二进制序列化, 使用 DataContract
- 二进制序列化，使用二进制序列化
- DataContract Serializer，使用二进制序列化
- 功能，目标 4.4: 序列化和反序列化数据
- JSON 序列化器，使用 DataContract
- XmlSerializer，使用 XmlSerializer
- ServiceContract 属性，使用对象关系映射器 (ORM)

# 集合与多线程

- 集合实现，在 .NET Framework 中处理加密
- 基于集合的集合，使用队列和栈
- 集合，数据访问集合，使用集合
- SHA256 算法，哈希处理
- 多线程应用程序中的共享数据，目标回顾
- 短路运算符，布尔值
- 侧边托管，程序集
- Sign 方法，管理证书
- 签名数据，管理证书
- 单维数组，目标 4.5: 从集合存储数据
- 标准接口，里可夫替换原则
- 标准 LINQ，标准 LINQ
- Start 选项（TraceEventType），日志与跟踪
- 启动任务，任务
- StartsWith 方法，搜索字符串
- 静态方法，添加某些数据
- Stop 选项（TraceEventType），日志与跟踪
- 停止线程，使用 Thread 类
- Stopwatch 类，分析应用程序
- 存储，值类型和引用类型
- 类型，值类型和引用类型
- 值类型，值类型和引用类型
- Stream 类，处理路径
- StreamReader，编码与解码
- 流，处理路径, 处理路径, 基础 Stream 类, 编码与解码
- 基础 Stream 类，处理路径
- 装饰器模式，编码与解码
- 编码与解码，基础 Stream 类
- 字符串数据保护，使用代码访问权限
- string.Concat 方法，目标 2.2: 使用类型
- StringBuilder 类，在 .NET Framework 中使用字符串
- StringReader 类，StringWriter and StringReader





# 字符串
- 目标回顾
- 目标 2.7: 操作字符串
- 在 .NET Framework 中使用字符串
- 搜索字符串
- 搜索字符串
- 搜索字符串
- 管理数据完整性

## .NET Framework
- 目标 2.7: 操作字符串

# 输入
- 管理数据完整性

# 类
- 在 .NET Framework 中使用字符串

# 枚举
- 搜索字符串

# 格式化
- 搜索字符串

# 搜索
- 搜索字符串

# StringWriter 类
- StringWriter 和 StringReader

# 强名称工具
- 使用强名称签名程序集

# 强命名程序集
- 使用强名称签名程序集

# struct 关键字
- 值类型和引用类型

# Suspend 选项 (TraceEventType 枚举)
- 日志记录与跟踪

# switch 语句
- switch 语句

# 符号服务器，PDB 文件
- 管理程序数据库文件和符号

# 对称加密
- 使用对称和非对称加密

# SymmetricAlgorithm 类
- 在 .NET Framework 中处理加密

# 同步，Console 类
- 理解线程

# SynchronizationContext, 异步代码
- 使用 async 和 await

# 资源同步，多线程
- 目标回顾
- 资源同步
- 资源同步
- Volatile 类

# Interlocked 类
- Volatile 类

# lock 语句
- 资源同步

# Volatile 类
- 资源同步

# 同步代码
- 实现异步 I/O 操作

# System.BitConverter 辅助类
- 自定义转换

# System.Data 强命名程序集
- 使用强名称签名程序集

# System.Exception 类，属性
- 处理异常

# System.Linq.ParallelEnumerable 类
- 使用 async 和 await

# System.MulticastDelegate 类
- 理解委托

# System.Threading 命名空间
- 理解线程
- 使用 Task

### Parallel 类
- 使用 Task

# Thread 类
- 理解线程

### T
- t.Join 方法
- 使用 Thread 类
- Take 运算符
- 标准 LINQ 查询运算符
- 任务调度器
- 使用 Task
- Task.WaitAll 方法
- 使用 Task
- Task<T> 类
- 使用 Task
- TaskFactory
- 使用 Task
- Tasks
- Interlocked 类
- 取消任务
- 取消中
- Interlocked 类
- 设置超时
- 取消任务
- Tasks, 多线程应用程序
- 线程池
- 使用 Task
- 使用 Task
- 使用 Task
- 使用 Task
- 使用 Task
- 使用 Task
- 将子任务附加到父任务
- 使用 Task
- 延续
- 使用 Task
- TaskFactory
- 使用 Task
- WaitAll 方法
- 使用 Task
- WaitAny 方法
- 使用 Task
- WhenAll 方法
- 使用 Task
- Team Foundation Server (TFS)
- 管理程序数据库文件和符号
- TraceWriter
- 日志记录与跟踪
- TFS (Team Foundation Server)
- 管理程序数据库文件和符号
- Thread 类
- 理解线程
- 线程池
- 使用 Thread 类
- Thread.Abort 方法
- 使用 Thread 类
- Thread.Current 类
- 使用 Thread 类
- Thread.Join 方法
- 使用 Thread 类
- ThreadException
- 使用 Thread 类
- ThreadLocal<T> 类
- 使用 Thread 类
- 线程
- 目标 1.1: 多线程处理
- 理解线程
- 使用 Thread 类
- Thread 类
- 理解线程
- 线程池
- 使用 Thread 类
- ThreadStatic 属性
- 抛出异常
- 处理异常 (修正 ID)
- 超时, Tasks
- 取消任务
- ToList 方法
- LINQ 如何工作？
- 工具
- 验证 JSON 和 XML
- 管理并创建证书
- 使用强名称签名程序集
- 管理程序数据库文件和符号
- 性能分析
- Makecert.exe
- 管理并创建证书
- PDB
- 管理程序数据库文件和符号
- 性能分析
- 性能分析
- 强名称
- 使用强名称签名程序集
- XML 定义
- 验证 JSON 和 XML
- ToString 方法
- 格式化字符串
- ToXml 方法
- 在 .NET Framework 中处理加密
- TraceEventType 枚举
- 日志记录与跟踪
- TraceListeners
- 日志记录与跟踪
- TraceSource 类
- 日志记录与跟踪
- 跟踪策略
- 目标回顾
- Trait 属性
- 读取属性
- 事务，数据完整性
- 管理数据完整性
- 事务，数据库
- 使用参数
- TransactionScope 类
- 使用参数
- TransactionScopeOption 枚举
- 使用事务
- Transfer 选项 (TraceEventType 枚举)
- 日志记录与跟踪
- 转换
- 创建 XML
- 触发器
- 管理数据完整性
- try/catch 语句，处理异常
- 目标 1.5: 实现异常处理
- Dequeue 方法
- ConcurrentStack 和 ConcurrentQueue
- Parse 方法
- 自定义转换
- Peek 方法
- BlockingCollection<T`
- Pop 方法
- ConcurrentStack 和 ConcurrentQueue
- PopRange 方法
- ConcurrentStack 和 ConcurrentQueue
- Take 方法
- BlockingCollection<T`
- Update 方法
- ConcurrentDictionary
- 类型参数，约束
- 使用泛型类型





# 类型
- 创建和使用类型
- 目标 2.1: 创建类型
- 目标 2.1: 创建类型
- 创建枚举
- 值类型和引用类型
- 值类型和引用类型
- 使用蓝图
- 使用泛型
- 使用泛型
- 目标 2.2: 消费类型
- 目标 2.2: 消费类型
- 装箱和拆箱
- 使用动态类型
- 目标 2.3: 强制封装
- 目标 2.3: 强制封装
- 将类型保持在你的程序集内部
- 使用属性
- 目标回顾
- 目标 2.4: 创建并实现类层次结构
- 创建和使用基类
- 里斯科替换原则
- 目标 2.5: 使用反射在运行时查找、执行和创建类型
- 目标 2.5: 使用反射在运行时查找、执行和创建类型
- 使用反射
- 使用反射
- Lambda 表达式
- Lambda 表达式
- Lambda 表达式
- 目标 2.6: 管理对象生命周期
- 目标 2.6: 管理对象生命周期
- 理解垃圾回收
- 目标回顾
- 目标 2.7: 操作字符串
- 在 .NET Framework 中使用字符串
- 搜索字符串
- 搜索字符串
- 搜索字符串
- 管理数据完整性

# 类层次结构
- 目标回顾
- 目标 2.4: 创建并实现类层次结构
- 创建和使用基类
- 里斯科替换原则

# .NET Framework 标准接口
- 里斯科替换原则

# 基类
- 创建和使用基类

## 设计和实现接口
- 目标 2.4: 创建并实现类层次结构

# 消费
- 目标 2.2: 消费类型
- 目标 2.2: 消费类型
- 装箱和拆箱
- 使用动态类型

# 值类型的装箱和拆箱
- 目标 2.2: 消费类型

### 转换
- 装箱和拆箱

# 动态类型
- 使用动态类型

### 转换
- 管理数据完整性

# 在 C# 中创建
- 创建和使用类型
- 目标 2.1: 创建类型
- 目标 2.1: 创建类型
- 创建枚举
- 值类型和引用类型
- 使用蓝图
- 使用泛型
- 使用泛型

# 主体
- 值类型和引用类型

# 类别
- 目标 2.1: 创建类型

### 设计类
- 使用蓝图

# 枚举
- 目标 2.1: 创建类型

### 扩展方法
- 使用泛型

# 泛型
- 使用泛型

### 值类型和引用类型
- 创建枚举

# 封装
- 目标 2.3: 强制封装
- 目标 2.3: 强制封装
- 将类型保持在你的程序集内部
- 使用属性

# 访问修饰符
- 目标 2.3: 强制封装

# 显式接口实现
- 使用属性

### 属性
- 将类型保持在你的程序集内部

# 泛型创建
- Lambda 表达式

# 生命周期生命周期
- 目标 2.6: 管理对象生命周期
- 目标 2.6: 管理对象生命周期
- 理解垃圾回收

# 垃圾回收
- 目标 2.6: 管理对象生命周期

# 非托管资源
- 理解垃圾回收

# 字符串操作
- 目标回顾
- 目标 2.7: 操作字符串
- 在 .NET Framework 中使用字符串
- 搜索字符串
- 搜索字符串
- 搜索字符串

## .NET Framework
- 目标 2.7: 操作字符串

# 类
- 在 .NET Framework 中使用字符串

# 枚举
- 搜索字符串

# 格式化
- 搜索字符串

# 搜索
- 搜索字符串

# 反射
- 目标 2.5: 使用反射在运行时查找、执行和创建类型
- 目标 2.5: 使用反射在运行时查找、执行和创建类型
- 使用反射
- 使用反射

### 属性
- 目标 2.5: 使用反射在运行时查找、执行和创建类型

# 表达式树
- 使用反射

# 功能
- Lambda 表达式

### Lambda 表达式
- Lambda 表达式

# 存储
- 值类型和引用类型

### U
# 意外异常
- 目录

# 值类型的装箱
- 目标 2.2: 消费类型

# #undef 指令
- 创建编译器指令

# Unicode
- 基类

# Unicode 联盟
- 基类

# 统一资源定位符 (URL)
- 创建枚举

# UnitTestAttribute
- 创建自定义属性

# 非托管资源，终结
- 理解垃圾回收

# 无序并行查询
- 使用并行语言查询 (PLINQ)

# 更新数据，数据库
- 更新数据

# 更新 XML，LINQ
- 创建 XML

# URL (统一资源定位符)
- 创建枚举

# 用户账户控制
- 隐式转换 (见 UAC)

# 用户定义转换，类型
- 隐式转换

# 用户定义完整性（数据完整性）
- 管理数据完整性

# 用户
- 目标 3.1: 验证应用输入
- 目标回顾

# 身份
- 目标回顾 (见加密)

# 验证应用输入
- 目标 3.1: 验证应用输入

# UTF-32 编码标准
- 基类

# UTF-7 编码标准
- 基类

# UTF-8 编码标准
- 基类

### V





## 验证
- 使用辅助类进行转换
- 调试应用程序并实现安全性
- 目标 3.1: 验证应用程序输入
- 目标 3.1: 验证应用程序输入
- 管理数据完整性
- 使用 Parse、TryParse 和 Convert
- 使用正则表达式

## 应用输入
- 调试应用程序并实现安全性
- 目标 3.1: 验证应用程序输入
- 目标 3.1: 验证应用程序输入
- 管理数据完整性
- 使用 Parse、TryParse 和 Convert
- 使用正则表达式

## 数据完整性
- 目标 3.1: 验证应用程序输入

## JSON 和 XML 数据
- 使用正则表达式

## 类型间的转换方法
- 管理数据完整性

## 验证原因
- 目标 3.1: 验证应用程序输入

## 正则表达式
- 使用 Parse、TryParse 和 Convert

## 类型转换
- 使用辅助类进行转换

## ValidationEventHandler
- 验证 JSON 和 XML

## 值类型
- 目标 2.1: 创建类型
- 创建枚举
- 值类型和引用类型
- 目标 2.2: 消费类型
- 目标 2.6: 管理对象生命周期

## 装箱与拆箱
- 目标 2.2: 消费类型

## 创建
- 创建枚举

## 枚举
- 目标 2.1: 创建类型

## 存储
- 值类型和引用类型
- 目标 2.6: 管理对象生命周期

## var 关键字
- 目标 4.3: 使用 LINQ 查询和操作数据及对象

## 详细性选项 (TraceEventType 枚举)
- 日志记录和跟踪

## VerifyHash 方法
- 管理和创建证书

## 验证数据、数字证书
- 管理和创建证书

## 程序集版本
- 将程序集放入 GAC

## Visual Studio
- 使用强名称签名程序集
- 生成配置
- 分析你的应用程序

## 性能向导
- 分析你的应用程序

## 设置断点
- 生成配置

## 签名页面
- 使用强名称签名程序集

## Visual Studio 调试器，异步代码
- 使用 async 和 await

## Volatile 类，多线程应用程序的资源同步
- 同步资源

### W
## WaitAny 方法
- 使用任务

## #warning 指令
- 创建和管理编译器指令

## 警告选项 (TraceEventType 枚举)
- 日志记录和跟踪

## WCF (Windows 通信框架)，创建服务
- 使用对象关系映射器 (ORM)

## WeakReference
- 实现 IDisposable 和终结器

## Web 服务，数据存储
- 使用对象关系映射器 (ORM)

## WebRequest 类
- 文件系统不仅仅是为了为你准备的

## WebResponse 类
- 文件系统不仅仅是为了为你准备的

## WhenAll 方法
- 使用任务

## Where 运算符
- 查询 XML](#ch04.html_iddle2531)

## while 循环，跨集合
- while-do 循环

## 通配符，模式
- 目录

## windows
- 管理程序文件

## 调用栈
- 管理程序文件

## 模块
- 管理程序文件

## Windows Communication Foundation (WCF) 服务
- 使用对象关系映射器 (ORM)

## Windows Metadata (WinMD) 文件
- 程序集版本

## Windows Runtime
- 创建 WinMD 程序集

## WinMD (Windows Metadata) 文件
- 程序集版本

## WinMD 程序集，创建
- 程序集版本

## WinRT runtime
- 程序集版本

## WithDegreeParallelism 方法
- 并行集成查询 (PLINQ)

## WithExecutionMode 方法
- 并行集成查询 (PLINQ)

## Wizards，性能
- 分析你的应用程序

## 包装类，IUnknown 接口
- IUnknown

## Write 方法
- Volatile 类

## WriteAsync 方法
- 使用 async 和 await

## 从流写入
- 路径

### X
## X.509 证书
- 管理和创建证书

## XElement 类
- 创建 XML

## XElement 构造函数
- 创建 XML

## XML (扩展标记语言)
- 使用正则表达式
- 创建 WCF 服务
- 消费 XML
- XmlReader
- XmlWriter
- XmlWriter
- LINQ 如何工作？

## 消费数据
- 创建 WCF 服务
- 消费 XML
- XmlReader
- XmlWriter
- XmlWriter

## .NET Framework
- 消费 XML

## XMLDocument 类
- XmlWriter

## XMLReader 类
- XmlReader

## XMLWriter
- XmlWriter

## 数据验证
- 使用正则表达式

## LINQ to
- LINQ 如何工作？

## XML 定义工具
- 验证 JSON 和 XML

## XmlArray 特性
- 使用 XmlSerializer

## XmlArrayItem 特性
- 使用 XmlSerializer

## XmlAttribute 特性
- 使用 XmlSerializer

## XmlDocument 类
- 消费 XML
- XmlWriter

## XmlElement 特性
- 使用 XmlSerializer

## XmlIgnore 特性
- 使用 XmlSerializer

## XmlNode 对象
- XmlWriter

## XmlReader 类
- 消费 XML
- XmlReader

## XmlSerializer
- 使用 XmlSerializer

## XmlWriter 类
- 消费 XML
- XmlWriter

## XmlWriter.Create 方法
- StringWriter 和 StringReader

## XOR (异或) 运算符
- 处理布尔表达式

## XPath
- XmlDocument

## XPathNavigator 类
- 消费 XML

### Y
## yield 关键字
- IEnumerable

## yield 语句
- 标准 LINQ 查询操作符

# 关于作者





Wouter de Kort 是 Seize IT 的独立技术教练、培训师和开发者。他拥有 MCSD 认证。作为一名软件架构师，他曾指导过复杂的 Web 应用程序开发。他还曾担任技术宣讲，帮助机构保持在 Web 开发的前沿水平。Wouter 从 `C#` 和 `.NET` 诞生起一直使用它们；他的专业知识还包括 `Visual Studio`、`Team Foundation Server`、`Entity Framework`、`Unit Testing`、设计模式、`ASP.NET` 和 `JavaScript`。

# Exam Ref 70-483：C# 编程

# 特别升级优惠
如果您是从 O’Reilly 以外的零售商购买的本电子书，可以在 oreilly.com 以 4.99 美元的价格进行升级，只需[点击此处](http://opds.oreilly.com/buy/9780735676817.EBOOK?source=ibooks)。

## 作者与贡献者
### Wouter de Kort
 编辑
### Russell Jones

版权所有 © 2013 O’Reilly Media, Inc.

经微软公司授权出版，由以下实体出版：

保留所有权利。未经出版商书面许可，不得以任何形式或通过任何手段复制或传输本书的内容。

1 2 3 4 5 6 7 8 9 QG 8 7 6 5 4 3

Microsoft Press 书籍通过全球书商和分销商提供。如果您需要与此书相关的支持，请电子邮件至 mspinput@microsoft.com 联系 Microsoft Press 书籍支持。请在 [`www.microsoft.com/learning/booksurvey`](http://www.microsoft.com/learning/booksurvey) 告诉我们对这本书的意见。

微软以及 [`www.microsoft.com/about/legal/en/us/IntellectualProperty/Trademarks/EN-US.aspx`](http://www.microsoft.com/about/legal/en/us/IntellectualProperty/Trademarks/EN-US.aspx) 列出的商标均为微软集团公司的商标。所有其他标记均为其所有者的财产。

书中描述的示例公司、组织、产品、域名、电子邮件地址、标志、人物、地点和事件均为虚构。无意或不应推断与任何真实的公司、组织、产品、域名、电子邮件地址、标志、人物、地点或事件有任何关联。

本书表达了作者的观点和意见。书中包含的信息不提供任何明示、法定或暗示的保证。作者、O’Reilly Media, Inc.、微软公司或其销售商、分销商均不对本书直接或间接引起或据称由本书造成的任何损害不承担责任。

- **收购与开发编辑：** Russell Jones
- **制作编辑：** Melanie Yarbrough
- **编辑制作：** Box Twelve Communications
- **技术审核员：** Auri Rahimzadeh
- **校对编辑：** Ginny Munro
- **封面设计：** Twist Creative • Seattle
- **封面排版：** Ellie Volck
- **插画师：** Rebecca Demarest

Microsoft Press
微软公司下部门
One Microsoft Way
Redmond, Washington 98052-6399
2013-07-09T11:09:00-07:00

