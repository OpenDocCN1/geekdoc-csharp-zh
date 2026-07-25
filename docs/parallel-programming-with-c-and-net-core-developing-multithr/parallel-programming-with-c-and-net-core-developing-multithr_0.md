# C# 和 .NET Core 并行编程：从零开始使用 C# 和 .NET Core 3.1 开发多线程应用








## 献给
全球所有正在与这种致命病毒斗争、冒着生命危险拯救人类的热心读者们！向他们致敬！

## 关于作者
**Rishabh Verma** 是微软认证专业人士，在微软担任高级顾问，帮助客户设计、开发和部署企业级应用程序。他在 .NET 技术栈上拥有 12 年以上的硬核开发经验。他的兴趣是创建工具、Visual Studio 扩展、代码生成和 .NET Foundation。他的 LinkedIn 页面为：`https://www.linkedin.com/in/rishabhverma/`。

**Neha Shrivastava** 是微软认证专业人士，在微软印度开发中心的 Cloud & AI 组担任软件工程师。她拥有约十年的开发经验，在金融、医疗保健和电子商务领域拥有专长。她的兴趣是 ASP.NET 栈、Azure 和跨平台开发。她热衷于学习新技术并与最新进展同步。她的 LinkedIn 简介为：`https://www.linkedin.com/in/neha-shrivastava-99a80135/`。

**Ravindra Akella** 在微软担任高级顾问，拥有 13 年以上的软件开发经验。他精通 .NET 和 Web 相关技术，目前的工作涉及从架构到使用 Azure 及相关技术交付复杂解决方案的端到端产品所有。他是一个精通技术的开发者，热于拥抱新技术。他曾在国际会议上进行过 Azure 及其他技术的演讲和会议。他的 LinkedIn 简介为：`https://www.linkedin.com/in/ravindra-akella/`。

## 致谢
当一本书出版时，只有作者和编辑的名字会被提及，但许多无名英雄发挥了同样重要的作用，没有他们，项目无法完成或取得成功。我有很长的一名单英雄需要感谢。衷心感谢架构师们（`Ranjiv Sharma`、`Shrenik Jhaveri`、`Prasad Ganganunta`），因为他们的每一次讨论都给我提供了问题的全新视角和新知识。衷心感谢我的经理们（`Ashwani Sharma`、`Manish Sanga`），他们在专业工作之外一直鼓励并支持我写这本书。感谢所有的同事、朋友和团队成员，他们让我对写作感到愉快并给予了支持。

如果没有家人的可靠支持，事情似乎相当难以完成，尤其是当它们占据了你的时间时。感谢我的父母（`Smt. Pratibha Verma` & `Shri R C Verma`）和我的兄弟（`Rishi Verma`）持续的支持，他们是我不断的能量来源。我要感谢我的妻子和合著者 `Neha`，她牺牲了无数周末并支持我完成截止日期。最后，但同样，我要感谢我的团队（`Neha`、`Ravindra`）以及 BPB 出版的优秀团队，为我们提供了这个分享学习经验并为社区贡献的机会。 — **Rishabh Verma**

我要以最诚挚的感谢父母（`Smt. Archana Shrivastava` 和 `Shri O.P. Shrivastava`）的支持和爱；我的兄弟（`Dr. Utkarsh Shrivastava`）、嫂子（`Dr. Samvartika Shrivastava`），以及最后同样重要的，我的丈夫，他也是这本书的合著者 `Rishabh`。他们通过持续的支持和鼓励一直让我坚持下去。 — **Neha Shrivastava**

我想感谢几位在写书期间给予我持续和进行性支持的人。我非常感谢父母的爱、祈祷、关怀和牺牲；非常感谢我的妻子 `Srividya` 和儿子 `Vaarush` 的爱、理解、祈祷和完成这本书的持续支持。最后，感谢我的合著者 `Rishabh` 和 BPB Publications 的机会。

## 前言
应用程序开发在过去十年中发生了演变，随着 `Angular`、服务器端 `ASP.NET Core` 等最新技术的出现，消费者的期望也随之提高。软件开发的新格言是“慢即是快”，这意味着性能是应用程序开发中最关键的因素之一。本书的主要目标是帮助读者理解异步编程的重要性以及使用 `.NET Core` 构建并发应用程序的各种方法。通过这十章，你将学习线程的基础、异步编程、各种同步结构、单元测试方法、调试应用程序以及技巧。


*   下载 Windows 必备工具
*   安装带有 .NET Core 的 Visual Studio 2019
*   使用 Visual Studio 2019 配合 `.NET Core 3.1`
*   使用 `Perfmon、Procmon、PerfView、JustDecompile、DebugDiag、WinDbg`

*   C# 8 平台依赖
*   新功能和增强
*   可空类型 / 非可空类型
*   异步流
*   范围和索引 (`System.Index`、`System.Range`)
*   接口的默认实现
*   结构体上的只读成员
*   模式匹配增强（Switch 表达式、递归模式、位置模式）
*   `Using` 声明
*   静态本地函数
*   `ref` 结构体
*   空合并赋值
*   插值字符串
### 3. .NET Core 3.1
*   .NET Core 版本 API
*   Windows Desktop 应用程序支持
*   Windows Desktop MSIX
*   COM 调用组件 – Windows Desktop
*   WinForms 高 DPI
*   .NET Standard 2.1
*   C# 8 及其新功能支持
*   编译和部署（默认执行文件、单执行文件）
*   程序集
*   分层编译
*   ReadyToRun 
*   跨平台/架构限制
*   运行时/SDK（构建副本、本地工具）
*   垃圾回收堆
*   垃圾回收大页（可选）
*   IEEE 浮点改进
*   内置 JSON 支持 (`JsonReader`、`JsonWriter`、`Json`)
*   HTTP/2 支持
*   加密导入和导出
### 4. 揭秘线程
*   为什么需要线程？什么是线程？
*   `ThreadException` 处理
*   `ThreadPool` 的限制
*   `ThreadPool` 中的异常
*   线程池的限制
*   `ThreadPool` 实战
*   `Task`、`TaskCreationOptions`
*   使用任务的异常处理
*   取消、续接
*   `WhenAll`、`WhenAny`
*   `Task Scheduler`,`Task Factory`

*   理解术语
*   并行扩展
*   任务并行库 (`TPL`)
*   数据并行、任务并行
*   `PLINQ`
*   并行数据结构
*   `IEnumerator` 和 `yield return`
*   `async await`（控制流、底层原理）
*   语言特性（使用 `async await` 的原则、`async await` 的限制）
*   CPU（计算）密集对比 I/O 密集工作
*   死锁、异步流、值

### 6. 线程模式
*   基于任务的异步模式 (`TAP`)
*   CPU 密集对比 I/O 密集
*   异常处理
*   取消、进度报告
*   异步编程模型 (`APM`)
*   基于事件的异步模式 (`EAP`)

### 7. 同步结构
*   线程安全
*   锁结构（互斥、非互斥）
*   信号结构 (`AutoResetEvent`、`ManualResetEvent`、`Semaphore`、`SemaphoreSlim`、读/写锁、`AutoResetEvent`、`ManualResetEventSlim`、`CountdownEvent`、`Barrier`、`Interlocked`、`Volatile`)

### 8. 并行和异步程序的单元测试
*   使用 `XUnit`单元测试的基础
*   实时单元测试
*   测试异步方法
*   测试异步方法中的异常
*   使用模拟 (`Moq`) 测试异步方法

### 9. 调试与故障排除
*   使用 `Visual Studio 2019` 进行入门调试
*   多线程应用程序分析
*   内存转储（收集与分析）
*   识别高 CPU 问题

### 10. 技巧与窍
*   线程与 `TPL`
*   `async await`
*   `async void` 与 `async Task`
*   `ConfigureAwait`

---

# 第 1 章：入门

## 下载 Windows 必备工具
为了开发并行应用程序，我们需要正确的工具。在本节中，我们将讨论先决条件。

## 安装带有 .NET Core 的 Visual Studio 2019
为了开发并行应用程序，我们需要正确的工具。在本节中，我们将讨论先决条件。

