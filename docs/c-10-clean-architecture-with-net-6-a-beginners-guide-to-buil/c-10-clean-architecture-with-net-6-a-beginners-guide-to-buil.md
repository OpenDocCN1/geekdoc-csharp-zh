

# C# 10 与 .NET 6 的整洁架构

构建可维护、可测试、可扩展且富有弹性的应用程序的初学者指南。

凯蒂·米莉

## 版权声明

版权所有 © 2024 凯蒂·米莉。保留所有权利。

未经凯蒂·米莉明确书面同意，严禁复制或未经授权使用本内容。但是，在给予凯蒂·米莉适当署名并提供指向原始内容的精确指引的前提下，允许摘录和超链接。感谢您认可凯蒂·米莉的辛勤付出和创造性贡献。

## 目录

- [引言](#)
- [第 1 章](#)
    - [传统软件开发的挑战](#)
    - [介绍整洁架构：构建持久的软件](#)
- [第 2 章](#)
    - [整洁架构的核心原则](#)
        - [依赖规则：高层模块不应依赖于低层模块](#)
        - [抽象：关注“做什么”，而非“怎么做”](#)
        - [框架与依赖：工具，而非基础](#)
    - [在 C# 10 项目中应用整洁架构原则](#)
- [第 3 章](#)
    - [揭示 C# 10 为整洁架构带来的特性](#)
        - [最小接口：简化抽象并封装功能](#)
        - [模式匹配增强：提升代码可读性和可维护性](#)
        - [其他 C# 10 特性及其与整洁架构实践的协同作用](#)
- [第 4 章](#)
    - [为整洁架构设置开发环境](#)
        - [配置 .NET 6 和 C# 10 以进行整洁架构开发](#)
        - [理解项目模板和整洁架构结构](#)
- [第 5 章](#)
    - [在整洁架构中使用 .NET 6 进行依赖注入](#)
        - [在 C# 10 中使用 .NET 6 实现依赖注入](#)
        - [依赖注入对松散耦合和可测试性的好处](#)
- [第 6 章](#)
    - [构建核心逻辑：业务规则层](#)
        - [在 C# 10 中实现业务规则层以提高可维护性](#)
        - [对业务规则层进行单元测试以确保代码质量和信心](#)
- [第 7 章](#)
    - [表示层：用户界面与交互](#)
        - [从表示层使用业务逻辑层](#)
        - [在表示层实现依赖注入以提高灵活性](#)
- [第 8 章](#)
    - [使用 .NET 实现数据持久化](#)
        - [定义数据模型和映射实体以进行持久化](#)
        - [实现关注点分离的数据访问逻辑](#)
        - [对持久化层进行单元测试以确保可靠的数据处理](#)
- [第 9 章](#)
    - [使用 ASP.NET Core MVC 6 实现整洁架构](#)
        - [从 ASP.NET Core MVC 控制器使用业务逻辑层](#)
        - [在 ASP.NET Core MVC 应用程序中实现依赖注入](#)
        - [利用最小 API 实现简洁高效的控制器（.NET 6 新特性）](#)
- [第 10 章](#)
    - [健壮的整洁架构应用程序的测试策略](#)
        - [集成测试：测试层之间的交互](#)
        - [利用测试框架（xUnit, NUnit）与 C# 10 特性](#)
        - [使用 .NET 6 的整洁架构项目的测试注意事项](#)
- [第 11 章](#)
    - [依赖倒置原则实现松散耦合和灵活性](#)
    - [用于数据访问抽象的仓储模式](#)
    - [使用 C# 10 和 .NET 6 为微服务实现整洁架构](#)
- [第 12 章](#)
    - [整洁架构的最佳实践和设计模式](#)
        - [整洁架构的设计模式：适配器、外观等](#)
        - [在项目演进过程中使用 C# 10 和 .NET 6 维护整洁架构](#)
- [第 13 章](#)
    - [C# 和 .NET 整洁架构的未来](#)
        - [整洁架构项目的持续集成与持续交付（CI/CD）](#)
        - [利用整洁架构实现 C# 和 .NET 6 项目的长期成功](#)
- [结论](#)
- [附录](#)
    - [术语表](#)
    - [展示使用 C# 10 和 .NET 6 实现整洁架构的示例应用程序代码](#)

## 引言

**打造持久软件：掌握 C# 10 与 .NET 6 的整洁架构**

在当今不断发展的技术格局中，仅仅构建功能性的软件是不够的。你需要构建**富有弹性、适应性强且为应对变化而生**的应用程序。**《C# 10 与 .NET 6 的整洁架构》**应运而生，它将赋能你掌握这一强大组合，构建卓越的软件解决方案。

本书超越了单纯的代码编写。它关乎于打造持久的代码。我们将深入探索整洁架构的变革性世界，这是一种设计哲学，赋能你构建如下特性的软件：

- **解耦：** 业务逻辑独立于表示层和数据访问层，从而提升灵活性和对变化的适应性。
- **可测试：** 松散耦合便于进行单元测试，确保代码质量并降低回归风险。
- **可维护：** 清晰的关注点分离提升了代码的可读性，并简化了未来的修改。

为什么选择 C# 10 和 .NET 6？这对前沿组合为实现你的整洁架构愿景提供了完美的平台。C# 10 凭借其开创性的特性，如全局 using 和最小接口，简化了代码并提升了开发者的生产力。结合 .NET 6 的强大功能，如改进的最小 API 和增强的性能，你将拥有构建整洁、高效且可扩展应用程序所需的工具。

**无论你是经验丰富的 C# 开发者，还是刚刚踏上架构之旅，本书都为你量身打造：**

- **整洁架构新手？** 别担心！我们将分解核心原则，引导你理解定义这种设计方法的分层结构和关注点分离。
- **C# 老手？** 探索 C# 10 特性在整洁架构框架内的激动人心的可能性。了解全局 using 如何简化代码组织，最小接口如何精简抽象，以及模式匹配如何增强代码的可读性和可维护性。
- **.NET 爱好者？** 利用 .NET 6 的强大功能来实施整洁架构的最佳实践。学习如何利用最小 API 构建简洁高效的控制器，拥抱配置管理以实现灵活配置，并利用异步编程构建高效、响应迅速的应用程序。

**超越基础：**

本书不仅介绍整洁架构；它还为你提供了有效实施它的实用技能。我们将深入探讨：

- **真实案例：** 通过我们逐步引导你构建一个实际应用程序的过程，掌握整洁架构原则的实际应用。
- **高级主题：** 探索依赖倒置和仓储模式等高级概念，巩固你对整洁架构最佳实践的理解。
- **测试策略：** 学习如何为你的整洁架构应用程序编写有效的单元测试，确保代码质量和可维护性。
- **深入 .NET 6：** 在整洁架构的特定背景下，释放 .NET 6 特性的潜力，如最小 API 和增强的性能优化策略。

**在本旅程结束时，你将能够：**

- **自信地使用 C# 10 和 .NET 6，基于整洁架构原则设计和构建软件。**
- **掌握创建解耦、可维护且可测试的应用程序的技能，这些应用程序能够经受时间的考验。**
- **凭借对最佳实践和高级概念的深入理解，有能力为整洁架构项目做出贡献。**

**《C# 10 与 .NET 6 的整洁架构》**不仅仅是一本书；它是你对构建能够蓬勃发展、适应变化并赋能你交付卓越价值的软件的投资。**准备好释放你开发技能的真正潜力了吗？立即订购，开启打造卓越软件解决方案的旅程！**

## 第一章

### 传统软件开发的挑战

传统软件开发面临诸多挑战，尤其是在维护代码质量、可扩展性以及适应需求变化方面。让我们在 C# 10 和 .NET 6 的背景下，结合整洁架构原则来深入探讨这些挑战。

1.  **单体架构：** 传统软件通常采用单体架构，整个应用被构建为一个紧密耦合的单元。随着应用的增长，这使得扩展和维护变得困难。在 C# 10 和 .NET 6 中，这可能导致代码库庞大且依赖关系错综复杂。

```csharp
// 单体架构方式
public class MonolithicApplication
{
    private readonly DatabaseContext _dbContext;
    private readonly ILogger _logger;

    public MonolithicApplication()
    {
        _dbContext = new DatabaseContext();
        _logger = new Logger();
    }

    public void ProcessData()
    {
        // 业务逻辑与数据访问和日志记录紧密耦合
        var data = _dbContext.GetData();
        _logger.Log("Processing data...");
        // 处理数据
    }
}
```

2.  **可扩展性问题：** 单体架构使得独立扩展应用的不同部分变得具有挑战性。在某些组件需要更多资源的场景下，扩展会变得低效。

```csharp
// 难以独立扩展组件
public class MonolithicApplication
{
    // ...
    public void ProcessData()
    {
        // 处理数据
        // 独立扩展此组件具有挑战性
    }

    public void HandleRequests()
    {
        // 处理 HTTP 请求
        // 独立扩展此组件具有挑战性
    }
}
```

3.  **依赖关系错综复杂：** 随着应用的增长，不同模块之间的依赖关系变得错综复杂，使得在不产生意外副作用的情况下理解和修改代码库变得困难。

```csharp
// 依赖关系错综复杂
public class MonolithicApplication
{
    private readonly DatabaseContext _dbContext;
    private readonly ILogger _logger;
    private readonly EmailService _emailService;

    public MonolithicApplication()
    {
        _dbContext = new DatabaseContext();
        _logger = new Logger();
        _emailService = new EmailService();
    }

    public void ProcessData()
    {
        // 业务逻辑与数据访问、日志记录和电子邮件服务紧密耦合
        var data = _dbContext.GetData();
        _logger.Log("Processing data...");
        _emailService.SendEmail("Data processed successfully!");
    }
}
```

4.  **可测试性有限：** 在单体架构中，由于组件紧密耦合，测试变得具有挑战性。在不测试整个应用的情况下，很难隔离和测试单个模块。

```csharp
// 可测试性有限
public class MonolithicApplicationTests
{
    [Fact]
    public void ProcessData_Should_Process_Data_Successfully()
    {
        // 测试需要数据库连接、日志记录和电子邮件服务
        var application = new MonolithicApplication();

        // 断言
        // 难以隔离并仅测试数据处理逻辑
    }
}
```

为了应对这些挑战，在 C# 10 和 .NET 6 中采用整洁架构方法是有益的。整洁架构强调关注点分离、模块化和框架无关性。以下是其实现方式：

1.  **关注点分离：** 将应用划分为层（如表示层、应用层、领域层和基础设施层），具有清晰的边界，且依赖关系向内流动。
2.  **模块化：** 将每一层封装到单独的项目或模块中，便于管理和独立开发。
3.  **依赖倒置原则：** 依赖抽象而非具体实现，从而实现灵活性和更便捷的测试。
4.  **使用接口和依赖注入：** 利用接口定义组件之间的契约，并利用依赖注入在运行时提供实现。

```csharp
// 整洁架构方式
// 应用层
public class DataProcessor
{
    private readonly IDataRepository _dataRepository;
    private readonly ILogger _logger;

    public DataProcessor(IDataRepository dataRepository, ILogger logger)
    {
        _dataRepository = dataRepository;
        _logger = logger;
    }

    public void ProcessData()
    {
        var data = _dataRepository.GetData();
        _logger.Log("Processing data...");
        // 处理数据
    }
}
```

通过整洁架构，可以缓解传统软件开发的挑战，从而在 C# 10 和 .NET 6 中构建出更易于维护、扩展和测试的代码库。

## 介绍整洁架构：构建持久的软件

整洁架构是一种软件设计哲学，强调关注点分离、模块化和可维护性。遵循整洁架构原则，开发者可以创建出能够长期保持健壮并适应变化的软件。在 C# 10 和 .NET 6 的背景下，实施整洁架构确保了软件项目的长期性和可扩展性。

## 理解整洁架构

整洁架构基于将代码组织成层的理念，每一层都有明确的职责，且依赖关系向内流动。这些层通常包括：

1.  **表示层：** 该层处理用户交互和输入/输出操作。它由负责向用户显示信息和捕获用户输入的组件组成。
2.  **应用层：** 应用层包含业务逻辑，并协调表示层和领域层之间的数据流。它封装了用例和特定于应用的逻辑。
3.  **领域层：** 领域层代表应用的核心业务实体、规则和逻辑。它独立于任何外部框架或技术，应该是系统中最稳定和可重用的部分。
4.  **基础设施层：** 该层为外部依赖（如数据库、文件系统和外部服务）提供实现。它抽象了这些依赖的细节，使应用能够与特定技术保持解耦。

## 在 C# 10 和 .NET 6 中实施整洁架构

让我们探讨如何使用 C# 10 和 .NET 6 实施整洁架构，并重点关注代码示例。

##### 表示层

在表示层，组件负责处理用户交互并向用户呈现信息。这可能包括 Web 界面、API 或用户界面。

```csharp
// 表示层（例如，ASP.NET Core Web API）
public class UserController : ControllerBase
{
    private readonly IUserService _userService;

    public UserController(IUserService userService)
    {
        _userService = userService;
    }

    [HttpGet("{id}")]
    public async Task<ActionResult<UserDto>> GetUserById(int id)
    {
        var user = await _userService.GetUserById(id);
        if (user == null)
        {
            return NotFound();
        }
        return Ok(user);
    }

    // 用于用户管理的其他 API 端点
}
```

### 应用层

应用层包含用例和业务逻辑。它协调表示层和领域层之间的交互。

```csharp
// 应用层
public interface IUserService
{
    Task<UserDto> GetUserById(int id);
}

public class UserService : IUserService
{
    private readonly IUserRepository _userRepository;

    public UserService(IUserRepository userRepository)
    {
        _userRepository = userRepository;
    }

    public async Task<UserDto> GetUserById(int id)
    {
        var user = await _userRepository.GetById(id);
        if (user == null)
        {
            return null;
        }
        return MapToDto(user);
    }
    // 与用户管理相关的其他业务逻辑
}
```

### 领域层

领域层包含业务实体、规则和逻辑。它应该独立于任何外部框架或技术。

```csharp
// 领域层
public class User
{
    public int Id { get; set; }
    public string FirstName { get; set; }
    public string LastName { get; set; }
    // 其他属性

    // 领域逻辑和验证规则
}
```

### 基础设施层

基础设施层为外部依赖（如数据库和外部服务）提供实现。

```csharp
// 基础设施层（例如，Entity Framework Core）
public class UserRepository : IUserRepository
{
    private readonly ApplicationDbContext _dbContext;

    public UserRepository(ApplicationDbContext dbContext)
    {
        _dbContext = dbContext;
    }

    public async Task<User> GetById(int id)
    {
        return await _dbContext.Users.FindAsync(id);
    }
}
```

## 清洁架构的优势

在 C# 10 和 .NET 6 中实施清洁架构具有以下几大优势：

1.  **可维护性：** 通过清晰的关注点分离，可以更轻松地维护和修改应用程序的不同部分，而不会影响其他组件。
2.  **可测试性：** 清洁架构通过允许每一层独立测试来提升可测试性，从而实现更全面的测试覆盖。
3.  **可扩展性：** 清洁架构的模块化结构使得随着应用程序的增长，更容易进行扩展，允许在无需大量重构的情况下添加新功能和特性。
4.  **灵活性：** 清洁架构在选择和替换外部依赖方面提供了灵活性，使其更容易适应需求或技术的变化。

清洁架构提供了一种经得起时间考验的、构建软件的原则性方法。通过将代码组织成具有明确职责的不同层次，开发者可以创建可维护、可测试且可扩展的软件。在 C# 10 和 .NET 6 中，可以实施清洁架构原则来创建健壮且适应性强的软件解决方案，以满足用户和企业不断变化的需求。

## 第 2 章

### 清洁架构的核心原则

#### 分层架构：关注点分离

分层架构是一种基本的设计模式，它通过将代码组织成具有特定职责的不同层次来强调关注点分离。在 C# 10 和 .NET 6 的背景下，实施分层架构遵循清洁架构的原则，确保模块化、可维护性和可扩展性。

#### 理解分层架构

分层架构通常由三个主要层次组成：

1.  **表示层：** 此层负责处理用户交互并向用户呈现信息。它包括用户界面、API 或 Web 界面等组件。
2.  **业务逻辑层（应用层）：** 业务逻辑层包含核心应用程序逻辑，包括用例和业务规则。它协调表示层和数据访问层之间的交互。
3.  **数据访问层：** 数据访问层负责与外部数据源（如数据库或外部服务）进行交互。它抽象了数据存储和检索的细节。

#### 在 C# 10 和 .NET 6 中实施分层架构

让我们探讨如何使用 C# 10 和 .NET 6 实施分层架构，并通过代码示例说明每一层。

##### 表示层

在表示层中，组件处理用户交互并向用户呈现信息。这可以使用 ASP.NET Core 来构建 Web 应用程序，或使用 ASP.NET Core Web API 来构建 RESTful API。

```csharp
// 表示层（例如，ASP.NET Core Web API）
[ApiController]
[Route("[controller]")]
public class UserController : ControllerBase
{
    private readonly IUserService _userService;

    public UserController(IUserService userService)
    {
        _userService = userService;
    }

    [HttpGet("{id}")]
    public async Task<ActionResult<UserDto>> GetUserById(int id)
    {
        var user = await _userService.GetUserById(id);
        if (user == null)
        {
            return NotFound();
        }
        return Ok(user);
    }

    // 其他用于用户管理的 API 端点
}
```

##### 业务逻辑层（应用层）

业务逻辑层包含特定于应用程序的逻辑，并协调表示层和数据访问层之间的交互。

```csharp
// 应用层
public interface IUserService
{
    Task<UserDto> GetUserById(int id);
}

public class UserService : IUserService
{
    private readonly IUserRepository _userRepository;

    public UserService(IUserRepository userRepository)
    {
        _userRepository = userRepository;
    }

    public async Task<UserDto> GetUserById(int id)
    {
        var user = await _userRepository.GetById(id);
        if (user == null)
        {
            return null;
        }
        return MapToDto(user);
    }

    // 其他与用户管理相关的业务逻辑
}
```

##### 数据访问层

数据访问层负责与外部数据源（如数据库）进行交互。这可以使用 Entity Framework Core 来实现数据库访问。

```csharp
// 数据访问层（例如，Entity Framework Core）
public interface IUserRepository
{
    Task<User> GetById(int id);
}

public class UserRepository : IUserRepository
{
    private readonly ApplicationDbContext _dbContext;

    public UserRepository(ApplicationDbContext dbContext)
    {
        _dbContext = dbContext;
    }

    public async Task<User> GetById(int id)
    {
        return await _dbContext.Users.FindAsync(id);
    }

    // 其他数据访问方法
}
```

#### 分层架构的优势

在 C# 10 和 .NET 6 中实施分层架构具有以下几大优势：

1.  **关注点分离：** 分层架构清晰地分离了不同的关注点，使得理解、维护和修改代码库变得更加容易。
2.  **模块化：** 每一层都可以独立开发和维护，从而实现更好的代码组织和可重用性。
3.  **可测试性：** 关注点分离使得测试更加容易，因为每一层都可以使用单元测试或集成测试进行独立测试。
4.  **可扩展性：** 分层架构允许通过轻松添加或修改层次来适应不断变化的需求或增加的负载，从而实现应用程序的可扩展性。

分层架构是一种强大的设计模式，它在软件开发中促进了关注点分离和模块化。在 C# 10 和 .NET 6 中，实施分层架构确保了代码库的整洁和可维护性，使得开发、测试和扩展软件应用程序变得更加容易。通过遵循清洁架构的原则，开发者可以构建健壮且可扩展的解决方案，以满足用户和企业的需求。

#### 依赖规则：高层模块不应依赖于低层模块

依赖规则是清洁架构中的一个关键原则，它主张高层模块不应依赖于低层模块。相反，两者都应依赖于抽象。此规则在软件开发中促进了松耦合、灵活性和可维护性。让我们深入探讨如何在 C# 10 和 .NET 6 中实施依赖规则，并通过代码示例说明其应用。

##### 理解依赖规则

依赖规则，也称为依赖倒置原则（DIP），是面向对象设计的 SOLID 原则之一。它强调高层模块需要依赖于抽象，而不是低层模块提供的具体实现。这种控制反转允许软件系统更易于维护、扩展和测试。

##### 在 C# 10 和 .NET 6 中实施依赖规则

要实施依赖规则，我们将遵循以下步骤：

1.  定义表示低层模块所提供功能的抽象（接口或抽象类）。
2.  确保高层模块依赖于这些抽象，而不是具体实现。
3.  使用依赖注入在运行时向高层模块提供具体实现。

让我们用一个实际的例子来说明这一点：

##### 高层模块

我们的高层模块代表一个负责用户身份验证的服务。

```csharp
// 高层模块
public interface IAuthenticationService
{
    Task<bool> AuthenticateUser(string username, string password);
}

public class AuthenticationService : IAuthenticationService
{
    private readonly IUserRepository _userRepository;

    public AuthenticationService(IUserRepository userRepository)
    {
        _userRepository = userRepository;
    }

    public async Task<bool> AuthenticateUser(string username, string password)
    {
        var user = await _userRepository.GetUserByUsername(username);
        if (user == null)
        {
            return false;
        }
        return user.Password == password;
    }
}
```

##### 低层模块

低层模块提供与数据源（如数据库）交互的具体实现。

```csharp
// 低层模块
public interface IUserRepository
{
    Task<User> GetUserByUsername(string username);
}

public class UserRepository : IUserRepository
{
    private readonly ApplicationDbContext _dbContext;

    public UserRepository(ApplicationDbContext dbContext)
    {
        _dbContext = dbContext;
    }

    public async Task<User> GetUserByUsername(string username)
    {
        return await _dbContext.Users.FirstOrDefaultAsync(u => u.Username == username);
    }
}
```

## 依赖倒置

为了遵循依赖规则，我们的高层模块依赖于 `IUserRepository` 接口提供的抽象，而不是具体的 `UserRepository` 实现。

```csharp
// Dependency Inversion
// High-Level Module depends on abstraction
public class AuthenticationService : IAuthenticationService
{
    private readonly IUserRepository _userRepository;

    public AuthenticationService(IUserRepository userRepository)
    {
        _userRepository = userRepository;
    }

    public async Task<bool> AuthenticateUser(string username, string password)
    {
        var user = await _userRepository.GetUserByUsername(username);
        if (user == null)
        {
            return false;
        }
        return user.Password == password;
    }
}
```

## 组合根

在组合根中，通常是 ASP.NET Core 应用程序中的 `Startup` 类，我们配置依赖注入，以便在运行时向高层模块提供具体实现。

```csharp
// Composition Root (e.g., Startup class in ASP.NET Core)
public void ConfigureServices(IServiceCollection services)
{
    services.AddScoped<IAuthenticationService, AuthenticationService>();
    services.AddScoped<IUserRepository, UserRepository>();
}
```

## 依赖规则的好处

在 C# 10 和 .NET 6 中实现依赖规则带来了以下好处：

- 1. **松耦合：** 高层模块与低层模块解耦，使得代码库更易于维护和修改。
- 2. **灵活性：** 抽象使得高层模块可以在不影响整体架构的情况下，切换由低层模块提供的不同实现。
- 3. **可测试性：** 高层模块变得更容易测试，因为依赖可以轻松地被模拟或存根，从而便于单元测试。
- 4. **可扩展性：** 依赖规则通过允许独立添加或修改新实现而不影响现有代码，促进了软件系统的可扩展性。

依赖规则是清洁架构的基本原则，它促进了软件设计中的松耦合和灵活性。通过在 C# 10 和 .NET 6 中实现这一规则，开发者可以创建遵循面向对象设计最佳实践的、可维护、可扩展且可测试的软件系统。正确应用依赖规则确保高层模块专注于应用特定的逻辑，而低层模块处理与外部依赖交互的细节。

## 抽象：关注“做什么”，而非“怎么做”

在软件开发领域，抽象在简化复杂性和实现更好设计方面扮演着至关重要的角色。当我们关注“需要做什么”而不是“应该如何做”时，我们可以创建更灵活、可维护和可扩展的代码。这一原则在清洁架构的背景下尤为重要，清洁架构是一种强调关注点分离和依赖倒置的设计哲学。

在 C# 10 和 .NET 6 中，我们拥有强大的工具和特性来使用抽象创建清晰、可维护的代码。让我们探讨如何在实践中应用这些概念。

### 依赖注入

依赖注入是清洁架构中管理组件间依赖关系的一项基本技术。通过注入依赖而不是硬编码它们，我们可以轻松替换实现并遵循依赖倒置原则。

```csharp
public class ProductService
{
    private readonly IProductRepository _productRepository;

    public ProductService(IProductRepository productRepository)
    {
        _productRepository = productRepository;
    }

    public async Task<IEnumerable<Product>> GetAllProducts()
    {
        return await _productRepository.GetAll();
    }
}
```

这里，`ProductService` 依赖于接口 `IProductRepository`，而不是具体的实现。这使我们能够更换仓库的不同实现，而无需更改服务本身。

## 接口与契约

接口定义了组件之间的契约，允许它们在不了解彼此实现细节的情况下进行通信。这促进了松耦合，并使得用一个组件替换另一个组件变得更容易。

```csharp
public interface IProductRepository
{
    Task<IEnumerable<Product>> GetAll();
}

public class SqlProductRepository : IProductRepository
{
    public async Task<IEnumerable<Product>> GetAll()
    {
        // Implementation for SQL database retrieval
    }
}

public class MongoProductRepository : IProductRepository
{
    public async Task<IEnumerable<Product>> GetAll()
    {
        // Implementation for MongoDB retrieval
    }
}
```

这里，`IProductRepository` 定义了检索产品的契约，而 `SqlProductRepository` 和 `MongoProductRepository` 提供了具体的实现。`ProductService` 类仅依赖于接口，而不是具体实现，从而实现了灵活性和可测试性。

## 服务抽象

在清洁架构中，业务逻辑应与基础设施关注点分离。服务抽象封装业务逻辑并协调不同组件之间的交互。

```csharp
public interface IOrderService
{
    Task PlaceOrder(Order order);
}

public class OrderService : IOrderService
{
    private readonly IOrderRepository _orderRepository;
    private readonly IEmailService _emailService;

    public OrderService(IOrderRepository orderRepository, IEmailService emailService)
    {
        _orderRepository = orderRepository;
        _emailService = emailService;
    }

    public async Task PlaceOrder(Order order)
    {
        await _orderRepository.Create(order);
        await _emailService.SendEmail("Order Confirmation", $"Your order {order.Id} has been placed.");
    }
}
```

这里，`OrderService` 依赖于订单仓库和电子邮件服务的接口。它通过创建订单和发送确认电子邮件来协调下单过程。仓库和电子邮件服务的实际实现在运行时注入。

## 可测试性

抽象通过允许我们在单元测试期间轻松模拟依赖来提高可测试性。这使我们能够隔离组件并独立验证其行为。

```csharp
public class ProductServiceTests
{
    [Fact]
    public async Task GetAllProducts_Returns_Products()
    {
        // Arrange
        var mockRepository = new Mock<IProductRepository>();
        var products = new List<Product> { new Product { Id = 1, Name = "Product 1" } };
        mockRepository.Setup(repo => repo.GetAll()).ReturnsAsync(products);
        var productService = new ProductService(mockRepository.Object);

        // Act
        var result = await productService.GetAllProducts();

        // Assert
        Assert.Equal(products, result);
    }
}
```

在这个单元测试中，我们使用产品仓库的模拟实现来模拟数据库行为。通过将模拟仓库注入到 `ProductService` 中，我们可以在不接触实际数据库的情况下测试其行为。

抽象是管理复杂性和提高软件系统可维护性的强大工具。通过关注“需要做什么”而不是“应该如何做”，我们可以创建清晰、灵活且可测试的代码。在 C# 10 和 .NET 6 中，我们可以利用依赖注入、接口和服务抽象等特性来有效地实现清洁架构原则。这种方法不仅提高了代码质量，还使其更容易适应不断变化的需求并扩展我们的应用程序。

## 框架与依赖：工具，而非基础

在软件开发中，框架和依赖是强大的工具，使我们能够更高效地构建复杂的应用程序。然而，至关重要的是要理解，它们应该作为支持我们代码的工具，而不是我们代码所依赖的基础。在 C# 10、清洁架构和 .NET 6 的背景下，让我们探讨如何在保持坚实架构基础的同时有效使用框架和依赖。

**依赖管理：**

依赖管理是清洁架构的一个关键方面。通过有效管理依赖，我们可以确保我们的代码保持灵活、可维护和可测试。NuGet 是 .NET 项目流行的包管理器，允许我们轻松添加、更新和移除依赖。

```bash
dotnet add package Newtonsoft.Json
```

这里，我们使用 `dotnet add package` 命令将 Newtonsoft.Json 包添加到我们的项目中。这个包提供了强大的 JSON 序列化功能，我们可以在应用程序中利用它。

**外部框架：**

外部框架提供了我们可以集成到应用程序中的预构建功能。虽然它们可以加速开发，但评估它们对我们架构的影响并确保它们符合我们的设计原则至关重要。

```csharp
public class WeatherService
{
```

## 管理框架版本：

保持框架和依赖项的最新状态对于安全性、性能和兼容性至关重要。然而，盲目更新依赖项可能会引入破坏性变更或兼容性问题。在将更新部署到生产环境之前，必须仔细审查发行说明并彻底测试更新。

```
dotnet list package --outdated
```

`dotnet list package --outdated` 命令会列出项目中所有过时的包。这使我们能够识别哪些依赖项需要更新，并评估这些更新的影响。

## 自定义抽象：

虽然框架提供了有用的功能，但它们不应决定我们架构的设计。相反，我们应该创建自定义抽象来封装特定于框架的逻辑，从而使我们的代码与底层实现解耦。

```csharp
public interface IEmailService
{
    Task SendEmail(string to, string subject, string body);
}

public class SmtpEmailService : IEmailService
{
    public async Task SendEmail(string to, string subject, string body)
    {
        // 使用 SMTP 协议的实现
    }
}

public class SendGridEmailService : IEmailService
{
    public async Task SendEmail(string to, string subject, string body)
    {
        // 使用 SendGrid API 的实现
    }
}
```

这里，`IEmailService` 定义了发送电子邮件的契约，而 `SmtpEmailService` 和 `SendGridEmailService` 使用不同的框架提供了具体实现。通过依赖接口而不是具体实现，我们可以轻松地在不同的电子邮件提供商之间切换。

## 最小化依赖足迹：

虽然框架可以提供有价值的功能，但我们应努力保持依赖足迹最小化。包含不必要的依赖项会使我们的应用程序膨胀，增加维护开销，并引入潜在的安全漏洞。必须仔细评估每个依赖项，只包含那些对我们的应用程序真正必要的。

框架和依赖项是使我们能够更高效地构建复杂应用程序的宝贵工具。然而，必须记住，它们应该作为支持我们代码的工具，而不是我们代码所依赖的基础。在 C# 10、整洁架构和 .NET 6 中，我们可以通过仔细管理框架和依赖项、创建自定义抽象以及最小化依赖足迹来有效地利用它们。通过这样做，我们可以确保我们的代码保持灵活、可维护和可扩展，同时利用 .NET 生态系统的最新进展。

## 在 C# 10 项目中应用整洁架构原则

整洁架构是一种设计哲学，它强调关注点分离和依赖倒置，以创建可扩展、可维护和可测试的软件系统。在使用 .NET 6 的 C# 10 项目中，我们可以利用整洁架构原则来有效地构建代码库。让我们通过代码示例来探讨如何应用这些原则。

### 整洁架构的层次：

整洁架构通常由几个层次组成，每个层次都有特定的职责：

1.  **表示层：** 负责用户交互和表示逻辑。
2.  **应用层：** 包含特定于应用程序的业务逻辑和用例。
3.  **领域层：** 定义核心业务实体、规则和逻辑。
4.  **基础设施层：** 处理外部关注点，如数据库、Web 服务和外部框架。

### 目录结构：

为了应用整洁架构原则，我们可以将代码库组织成每个层次一个单独的目录：

```
plaintext
MyProject/
├── MyProject.Domain/
├── MyProject.Application/
├── MyProject.Infrastructure/
└── MyProject.Presentation/
```

### 依赖规则：

在整洁架构中，依赖应向内流动，外层依赖于内层。这允许轻松替换组件，并促进模块化和可测试性。

```csharp
// 表示层依赖于应用层
// 应用层依赖于领域层
// 基础设施层依赖于应用层和领域层
```

### 示例代码：

让我们考虑一个应用了整洁架构原则的简单电子商务应用程序：

### 领域层：

```csharp
// MyProject.Domain/Entities/Product.cs
namespace MyProject.Domain.Entities
{
    public class Product
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public decimal Price { get; set; }
    }
}
```

### 应用层：

```csharp
// MyProject.Application/Interfaces/IProductService.cs
using System.Collections.Generic;
using System.Threading.Tasks;
using MyProject.Domain.Entities;

namespace MyProject.Application.Interfaces
{
    public interface IProductService
    {
        Task<IEnumerable<Product>> GetAllProducts();
    }
}
```

```csharp
// MyProject.Application/Services/ProductService.cs
using System.Collections.Generic;
using System.Threading.Tasks;
using MyProject.Application.Interfaces;
using MyProject.Domain.Entities;

namespace MyProject.Application.Services
{
    public class ProductService : IProductService
    {
        private readonly IProductRepository _productRepository;

        public ProductService(IProductRepository productRepository)
        {
            _productRepository = productRepository;
        }

        public async Task<IEnumerable<Product>> GetAllProducts()
        {
            return await _productRepository.GetAll();
        }
    }
}
```

### 基础设施层：

```csharp
// MyProject.Infrastructure/Repositories/ProductRepository.cs
using System.Collections.Generic;
using System.Threading.Tasks;
using MyProject.Application.Interfaces;
using MyProject.Domain.Entities;

namespace MyProject.Infrastructure.Repositories
{
    public class ProductRepository : IProductRepository
    {
        public async Task<IEnumerable<Product>> GetAll()
        {
            // 从数据库获取产品的实现
        }
    }
}
```

#### 表示层：

```csharp
// MyProject.Presentation/Controllers/ProductController.cs
using System.Collections.Generic;
using System.Threading.Tasks;
using Microsoft.AspNetCore.Mvc;
using MyProject.Application.Interfaces;
using MyProject.Domain.Entities;

namespace MyProject.Presentation.Controllers
{
    [ApiController]
    [Route("api/[controller]")]
    public class ProductController : ControllerBase
    {
        private readonly IProductService _productService;

        public ProductController(IProductService productService)
        {
            _productService = productService;
        }

        [HttpGet]
        public async Task<IEnumerable<Product>> GetAllProducts()
        {
            return await _productService.GetAllProducts();
        }
    }
}
```

### 测试：

整洁架构的一个关键优势是其可测试性。我们可以通过模拟依赖项并专注于单独测试各个组件，轻松地为应用程序的每一层编写单元测试。

```csharp
// MyProject.Application.Tests/ProductServiceTests.cs
using System.Collections.Generic;
using System.Threading.Tasks;
using Moq;
using MyProject.Application.Interfaces;
using MyProject.Application.Services;
using MyProject.Domain.Entities;
using Xunit;

namespace MyProject.Application.Tests
{
    public class ProductServiceTests
    {
        [Fact]
        public async Task GetAllProducts_Returns_Products()
        {
            // 准备
            var mockRepository = new Mock<IProductRepository>();
            var products = new List<Product> { new Product { Id = 1, Name = "Product 1", Price = 10 } };
            mockRepository.Setup(repo => repo.GetAll()).ReturnsAsync(products);
            var productService = new ProductService(mockRepository.Object);

            // 执行
            var result = await productService.GetAllProducts();

            // 断言
            Assert.Equal(products, result);
        }
    }
}
```

整洁架构为在 .NET 6 中构建 C# 10 项目提供了一个强大的框架，促进了关注点分离、模块化和可测试性。通过将代码库组织成不同的层次并强制执行依赖规则，我们可以创建可扩展、可维护且易于测试的软件系统。遵循这些原则，我们确保我们的代码保持灵活并适应不断变化的需求，最终带来更高质量的软件产品。

## 第三章

## 揭秘 C# 10 特性以实现整洁架构

### 全局 Using：简化代码组织以提升可读性

全局 Using 是 C# 10 和 .NET 6 中引入的一项功能，它允许开发者指定应自动导入到项目所有文件中的命名空间。此功能通过减少在整个代码库中重复编写 `using` 指令的需要，简化了代码组织并提升了可读性。当在 C# 10 项目的整洁架构上下文中应用时，全局 Using 可以增强代码的清晰度和简洁性。让我们探讨如何在整洁架构设置中利用全局 Using。

### 简化命名空间导入：

在整洁架构中，我们通常处理应用程序的多个层，每一层都包含自己的命名空间集合。通过全局 Using，我们可以消除在每个文件中手动导入命名空间的需要，从而减少杂乱并提升可读性。

```csharp
// GlobalUsings.cs
global using MyProject.Domain.Entities;
global using MyProject.Application.Interfaces;
global using MyProject.Infrastructure.Repositories;
```

通过在项目级别定义这些全局 Using，我们确保这些命名空间会自动导入到项目中的每个文件。这减少了重复 `using` 指令的需要，并使我们的代码更加整洁。

### 整洁架构示例：

让我们考虑一个使用整洁架构原则构建的简单电子商务应用程序示例，并应用了全局 Using。

```plaintext
MyProject/
├── MyProject.Domain/
├── MyProject.Application/
├── MyProject.Infrastructure/
└── MyProject.Presentation/
```

### 领域层：

```csharp
// MyProject.Domain/Entities/Product.cs
namespace MyProject.Domain.Entities
{
    public class Product
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public decimal Price { get; set; }
    }
}
```

### 应用层：

```csharp
// MyProject.Application/Interfaces/IProductService.cs
namespace MyProject.Application.Interfaces
{
    public interface IProductService
    {
        Task<IEnumerable<Product>> GetAllProducts();
    }
}

// MyProject.Application/Services/ProductService.cs
namespace MyProject.Application.Services
{
    public class ProductService : IProductService
    {
        private readonly IProductRepository _productRepository;

        public ProductService(IProductRepository productRepository)
        {
            _productRepository = productRepository;
        }

        public async Task<IEnumerable<Product>> GetAllProducts()
        {
            return await _productRepository.GetAll();
        }
    }
}
```

### 基础设施层：

```csharp
// MyProject.Infrastructure/Repositories/ProductRepository.cs
namespace MyProject.Infrastructure.Repositories
{
    public class ProductRepository : IProductRepository
    {
        public async Task<IEnumerable<Product>> GetAll()
        {
            // 从数据库获取产品的实现
        }
    }
}
```

### 表现层：

```csharp
// MyProject.Presentation/Controllers/ProductController.cs
namespace MyProject.Presentation.Controllers
{
    public class ProductController : ControllerBase
    {
        private readonly IProductService _productService;

        public ProductController(IProductService productService)
        {
            _productService = productService;
        }

        [HttpGet]
        public async Task<IEnumerable<Product>> GetAllProducts()
        {
            return await _productService.GetAllProducts();
        }
    }
}
```

### 全局 Using 的优势：

- **提升可读性：** 全局 Using 通过自动导入常用命名空间来减少杂乱，使代码更简洁、更易读。
- **一致性：** 通过在项目级别定义全局 Using，我们确保项目内所有文件的一致性，减少错误和不一致的可能性。
- **加快开发速度：** 开发者可以专注于编写代码，而无需在每个文件中手动导入命名空间，从而缩短开发时间。
- **更易于维护：** 由于需要管理的 `using` 指令更少，代码维护变得更加容易，尤其是在重构或重组代码库时。

### 注意事项：

虽然全局 Using 可以显著改善代码组织和可读性，但谨慎使用它们至关重要。过度使用全局 Using 或导入不必要的命名空间可能导致代码臃肿和可维护性下降。在减少杂乱和确保仅全局导入必要的命名空间之间取得平衡至关重要。

C# 10 和 .NET 6 中的全局 Using 提供了一种强大的机制，用于简化整洁架构项目中的代码组织并提升可读性。通过在项目级别定义常用命名空间，我们可以消除重复 `using` 指令的需要，并减少代码库中的杂乱。这不仅增强了可读性，还促进了代码的一致性、更快的开发速度和更轻松的维护。经过深思熟虑地应用，全局 Using 可以成为增强使用整洁架构原则构建的 C# 代码库清晰度和简洁性的宝贵工具。

### 最小接口：简化抽象并封装功能

在使用 .NET 6 的 C# 10 项目中，最小接口是简化抽象和封装功能的强大工具。通过仅定义具有必要成员的接口，我们可以在组件之间创建清晰简洁的契约，从而在整洁架构设置中促进模块化、灵活性和可测试性。让我们通过代码示例探讨如何有效利用最小接口。

### 最小接口的优势：

- **清晰性：** 最小接口专注于仅定义组件间交互所必需的成员，使契约清晰易懂。
- **简洁性：** 通过避免不必要的成员，最小接口保持接口定义简单明了，降低了复杂性和开发者的认知负担。
- **灵活性：** 最小接口在实现上提供了更大的灵活性，因为它们对组件如何履行其职责施加的约束更少。
- **可测试性：** 依赖于最小接口的组件更容易进行模拟和隔离测试，从而产生更健壮和可维护的测试套件。

### 整洁架构中的示例：

让我们考虑一个使用整洁架构原则构建的电子商务应用程序示例，并应用了最小接口。

```plaintext
MyProject/
├── MyProject.Domain/
├── MyProject.Application/
├── MyProject.Infrastructure/
└── MyProject.Presentation/
```

### 领域层：

```csharp
// MyProject.Domain/Entities/Product.cs
namespace MyProject.Domain.Entities
{
    public class Product
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public decimal Price { get; set; }
    }
}
```

### 应用层：

```csharp
// MyProject.Application/Interfaces/IProductService.cs
namespace MyProject.Application.Interfaces
{
    public interface IProductService
    {
        Task<IEnumerable<Product>> GetAllProducts();
        Task<Product> GetProductById(int id);
    }
}
```

### 基础设施层：

```csharp
// MyProject.Infrastructure/Repositories/ProductRepository.cs
namespace MyProject.Infrastructure.Repositories
{
    public class ProductRepository : IProductService
    {
        public async Task<IEnumerable<Product>> GetAllProducts()
        {
            // 从数据库获取所有产品的实现
        }

        public async Task<Product> GetProductById(int id)
        {

        }
    }
}
```

## 在表示层中的实现：

```csharp
// MyProject.Presentation/Controllers/ProductController.cs
namespace MyProject.Presentation.Controllers
{
    public class ProductController : ControllerBase
    {
        private readonly IProductService _productService;

        public ProductController(IProductService productService)
        {
            _productService = productService;
        }

        [HttpGet]
        public async Task<IEnumerable<Product>> GetAllProducts()
        {
            return await _productService.GetAllProducts();
        }

        [HttpGet("{id}")]
        public async Task<Product> GetProductById(int id)
        {
            return await _productService.GetProductById(id);
        }
    }
}
```

## 使用最小接口进行测试：

```csharp
// MyProject.Application.Tests/ProductServiceTests.cs
namespace MyProject.Application.Tests
{
    public class ProductServiceTests
    {
        [Fact]
        public async Task GetAllProducts_Returns_Products()
        {
            // Arrange
            var mockRepository = new Mock<IProductService>();
            var products = new List<Product> { new Product { Id = 1, Name = "Product 1", Price = 10 } };
            mockRepository.Setup(repo => repo.GetAllProducts()).ReturnsAsync(products);
            var productService = new ProductService(mockRepository.Object);

            // Act
            var result = await productService.GetAllProducts();

            // Assert
            Assert.Equal(products, result);
        }
    }
}
```

最小接口提供了一种强大的方式，可以在使用 .NET 6 的 C# 10 项目中简化抽象并封装功能，尤其是在清洁架构的背景下。通过专注于仅定义组件间交互所必需的成员，最小接口促进了清晰性、简洁性、灵活性和可测试性。它们提供了组件之间清晰而简洁的契约，使代码库更易于理解、维护和测试。当有效应用时，最小接口可以增强软件系统的质量和可维护性，从而促进更健壮和可扩展的解决方案。

## 模式匹配增强：提升代码可读性和可维护性

随着 C# 10 和 .NET 6 的发布，C# 中的模式匹配经历了重大增强。这些改进不仅使代码更具可读性，还通过提供简洁而富有表现力的语法来处理复杂的条件逻辑，从而增强了可维护性。在本文中，我们将探讨这些增强如何在清洁架构原则的背景下有助于提高代码质量。

## 模式匹配简介

模式匹配允许开发人员根据数据的结构和形状执行更高级的条件逻辑。它使得编写的代码比传统的条件语句更具表现力和简洁性。随着 C# 10 和 .NET 6 的推出，模式匹配能力得到了进一步扩展，为开发人员提供了更多的灵活性和强大功能。

## 简化的类型模式

C# 10 的关键增强之一是引入了简化的类型模式。这使得在检查对象类型时，代码更清晰、更易读。让我们在清洁架构应用程序的背景下考虑一个示例：

```csharp
public interface IEntity
{
    int Id { get; }
}

public class Customer : IEntity
{
    public int Id { get; set; }
    public string Name { get; set; }
}

public class Product : IEntity
{
    public int Id { get; set; }
    public string Description { get; set; }
}

public void ProcessEntity(IEntity entity)
{
    switch (entity)
    {
        case Customer customer:
            Console.WriteLine($"Processing Customer: {customer.Name}");
            break;
        case Product product:
            Console.WriteLine($"Processing Product: {product.Description}");
            break;
        default:
            throw new ArgumentException("Unknown entity type");
    }
}
```

在这个例子中，我们有一个由 `Customer` 和 `Product` 类实现的 `IEntity` 接口。`ProcessEntity` 方法接受任何实现 `IEntity` 的对象，并根据其类型进行处理。使用简化的类型模式，我们可以在 `case` 块中直接转换匹配的对象（`customer` 或 `product`），从而得到更清晰、更易读的代码。

## 属性模式

C# 10 引入的另一个强大增强是属性模式。属性模式允许开发人员根据对象的属性执行模式匹配。这在处理复杂数据结构时特别有用。让我们扩展之前的示例来演示属性模式的使用：

```csharp
public void ProcessEntity(IEntity entity)
{
    switch (entity)
    {
        case Customer { Name: var name }:
            Console.WriteLine($"Processing Customer: {name}");
            break;
        case Product { Description: var description }:
            Console.WriteLine($"Processing Product: {description}");
            break;
        default:
            throw new ArgumentException("Unknown entity type");
    }
}
```

在这个更新版本中，我们使用属性模式直接解构匹配的对象并提取特定属性（`Customer` 的 `Name` 和 `Product` 的 `Description`）。这导致了更简洁、更易读的代码，消除了在 `case` 块中进行额外转换或属性访问的需要。

## 关系和逻辑模式

C# 10 还引入了关系和逻辑模式，允许开发人员在模式匹配构造中直接表达复杂的条件。让我们用一个例子来说明这一点：

```csharp
public string GetDiscount(double amountSpent)
{
    return amountSpent switch
    {
        > 1000 => "10% Discount",
        >= 500 and <= 1000 => "5% Discount",
        _ => "No Discount"
    };
}
```

在这个例子中，我们在 switch 语句中使用关系模式（`>`、`>=`）和逻辑模式（`and`）来根据 `amountSpent` 确定折扣。这导致代码不仅更具表现力，而且更易于理解和维护。

C# 10 和 .NET 6 中引入的模式匹配增强显著提高了清洁架构原则背景下的代码可读性和可维护性。通过利用简化的类型模式、属性模式和关系/逻辑模式，开发人员可以编写更具表现力和简洁性的代码，从而带来更好的整体代码质量。这些增强使开发人员能够轻松处理复杂的条件逻辑，最终产生更健壮和可维护的应用程序。

## 其他 C# 10 特性及其与清洁架构实践的协同作用

C# 10 与 .NET 6 一起引入了几个与清洁架构实践协同良好的特性。这些特性不仅提高了开发人员的生产力，还有助于编写更清晰、更易维护的代码。在本文中，我们将探讨其中一些特性及其在清洁架构背景下的应用。

## 记录类型

记录类型在 C# 9 中引入，但在 C# 10 中得到了进一步增强。记录类型提供了一种简洁的语法来定义不可变的数据结构。在清洁架构中，不可变的数据结构被优先用于表示实体、值对象和 DTO（数据传输对象）。让我们看看记录类型如何在清洁架构场景中使用：

```csharp
public record Customer(int Id, string Name);
```

在这个例子中，我们定义了一个具有 `Id` 和 `Name` 属性的 `Customer` 记录类型。由于记录类型默认是不可变的，它们非常适合在清洁架构模式中表示领域实体，促进不可变性并提高代码清晰度。

### 文件范围命名空间

C# 10 引入了文件范围命名空间，允许开发人员直接在文件范围内定义命名空间，而无需将它们括在花括号中。此功能鼓励以逻辑方式组织代码并减少不必要的杂乱，与清洁架构的原则非常吻合。让我们演示如何使用文件范围命名空间：

```csharp
namespace MyApp.Domain;

public record Customer(int Id, string Name);
```

在这个例子中，`Customer` 记录类型直接在文件范围内的 `MyApp.Domain` 命名空间中定义。这促进了更清晰、更直观的代码组织，使其更易于导航和维护。

### 全局 using

全局 using 是 C# 10 引入的另一个功能，允许开发人员为整个项目全局指定 using 指令。这有助于减少样板代码，并通过消除在每个文件中重复 using 指令的需要来提高可读性。让我们说明全局 using 的使用：

```csharp
global using System;
global using MyApp.Domain;
```

## 可空引用类型

可空引用类型在 C# 8 中引入，并在后续版本中进一步改进，它通过允许开发者指定引用类型是否可以为 null 来帮助防止空引用异常。此特性促进了更安全、更健壮的代码，与整洁架构的原则非常契合。让我们看看如何使用可空引用类型：

```csharp
public class OrderService
{
    public void ProcessOrder(Customer? customer)
    {
        if (customer != null)
        {
            Console.WriteLine($"Processing order for customer: {customer.Name}");
        }
        else
        {
            throw new ArgumentNullException(nameof(customer), "Customer cannot be null");
        }
    }
}
```

在此示例中，`customer` 参数被标记为可空（`Customer?`），表明它可以被赋值为 null。然而，代码包含了空值检查以确保避免空引用异常，从而促进更安全、更可靠的代码。

C# 10 和 .NET 6 引入了多项补充整洁架构实践的特性，包括记录类型、文件作用域命名空间、全局 using 和可空引用类型。通过利用这些特性，开发者可以编写更整洁、更易于维护的代码，这些代码符合整洁架构的原则。这些特性促进了不可变性、代码的逻辑组织、减少样板代码以及更安全的代码实践，最终有助于开发健壮且易于维护的软件应用程序。

## 第 4 章

### 为整洁架构设置开发环境

#### 安装 Visual Studio 或您首选的 IDE

Visual Studio 是一个强大的集成开发环境（IDE），被 C# 开发者广泛用于构建面向 .NET 框架的应用程序。随着 .NET 6 和 C# 10 的发布，Visual Studio 为开发整洁架构应用程序提供了出色的支持。在本指南中，我们将逐步介绍安装 Visual Studio 并将其配置为使用 .NET 6 进行 C# 开发的过程。

#### 步骤 1：下载并安装 Visual Studio

1.  **访问 Visual Studio 网站：** 前往 Visual Studio 官方网站 https://visualstudio.microsoft.com/。
2.  **选择您的版本：** Visual Studio 提供不同的版本，例如 Community（免费版）、Professional（专业版）和 Enterprise（企业版）。对于大多数开发者，Community 版提供了足够的 C# 开发功能。
3.  **下载 Visual Studio：** 点击“下载 Visual Studio”按钮，并按照说明下载安装程序。

#### 步骤 2：运行 Visual Studio 安装程序

1.  **打开下载的安装程序：** 安装程序下载完成后，运行它以开始安装过程。
2.  **选择工作负载：** Visual Studio 提供了针对不同类型开发量身定制的各种工作负载。对于使用 .NET 6 进行 C# 开发，请确保选择“.NET Desktop Development”工作负载。
3.  **可选工作负载：** 根据您的需求，您可能还需要选择其他工作负载，例如“.NET Core 跨平台开发”或“ASP.NET 和 Web 开发”（如果您正在构建 Web 应用程序）。
4.  **安装：** 点击“安装”按钮开始安装过程。Visual Studio 将下载并安装所选的组件和依赖项。

#### 步骤 3：配置 Visual Studio

1.  **启动 Visual Studio：** 安装完成后，从“开始”菜单或桌面快捷方式启动 Visual Studio。
2.  **登录（可选）：** 系统可能会提示您使用 Microsoft 帐户登录。登录后可以访问其他功能，例如基于云的服务和许可证管理。
3.  **选择开发环境：** 首次启动时，Visual Studio 会提示您选择开发环境设置。您可以根据自己的喜好选择主题、键盘快捷键和其他首选项。
4.  **安装扩展（可选）：** Visual Studio 支持广泛的扩展，这些扩展可以提高生产力并添加额外功能。您可以浏览 Visual Studio Marketplace 来查找并安装适合您需求的扩展。

#### 步骤 4：创建新的 C# 项目

1.  **打开“新建项目”对话框：** 点击“文件” > “新建” > “项目...”以打开“新建项目”对话框。
2.  **选择项目模板：** 在“新建项目”对话框中，为您的整洁架构应用程序选择合适的项目模板。您可以根据要构建的应用程序类型，从“控制台应用 (.NET Core)”或“ASP.NET Core Web 应用程序”等模板中进行选择。
3.  **配置项目设置：** 为项目提供名称和位置，并配置任何其他设置，例如目标框架（.NET 6）和解决方案名称。
4.  **创建项目：** 点击“创建”按钮以创建项目。Visual Studio 将生成项目文件并在 IDE 中打开解决方案。

#### 步骤 5：开始编码

1.  **浏览解决方案资源管理器：** “解决方案资源管理器”窗口显示您的解决方案和项目的结构。您会找到用于源代码文件、引用和其他资源的文件夹。
2.  **编写代码：** 根据整洁架构原则，在适当的文件和文件夹中开始编写您的 C# 代码。您可以使用 IntelliSense、代码导航和调试工具等功能来辅助开发。
3.  **生成并运行：** 编写完代码后，通过点击“生成” > “生成解决方案”或按 Ctrl + Shift + B 来生成解决方案。然后，按 F5 或点击“调试” > “开始调试”来运行应用程序。

为使用 .NET 6 进行 C# 开发安装 Visual Studio 是一个简单直接的过程，它使开发者能够利用强大的 IDE 来构建整洁架构应用程序。按照本指南中概述的步骤操作，您将能够快速设置 Visual Studio 并开始编写 C# 代码。Visual Studio 提供了丰富的功能和工具，可以简化开发并提高生产力，使其成为 C# 开发者的绝佳选择。

### 为整洁架构开发配置 .NET 6 和 C# 10

整洁架构是一种设计模式，强调软件应用程序的关注点分离、可维护性和可测试性。随着 .NET 6 和 C# 10 的发布，开发者可以使用强大的工具和特性来简化整洁架构开发。在本指南中，我们将逐步介绍为整洁架构开发配置 .NET 6 和 C# 10 的过程，包括设置项目结构、依赖项和开发环境。

#### 步骤 1：安装 .NET 6 SDK

1.  **下载 .NET 6 SDK**：访问 .NET 官方网站 [https://dotnet.microsoft.com/download/dotnet/6.0](https://dotnet.microsoft.com/download/dotnet/6.0) 并下载适用于您操作系统的 .NET 6 SDK。
2.  **安装 .NET 6 SDK**：按照安装说明在您的计算机上安装 .NET 6 SDK。

#### 步骤 2：创建新解决方案

1.  **打开终端或命令提示符**：导航到您想要创建解决方案的目录。
2.  **创建解决方案**：运行以下命令创建一个新的解决方案：

```bash
dotnet new sln -n MySolution
```

#### 步骤 3：为每一层创建项目

整洁架构通常由多个层组成，例如表示层、应用层、领域层和基础设施层。让我们为每一层创建项目：

1.  **表示层（控制台应用）**：

```bash
dotnet new console -n MySolution.Presentation
```

2.  **应用层（类库）**：

```bash
dotnet new classlib -n MySolution.Application
```

3.  **领域层（类库）**：

```bash
dotnet new classlib -n MySolution.Domain
```

## 4. 基础设施层（类库）：

```bash
dotnet new classlib -n MySolution.Infrastructure
```

## 步骤 4：将项目添加到解决方案

**1. 将项目添加到解决方案：** 运行以下命令将项目添加到解决方案：

```bash
dotnet sln MySolution.sln add MySolution.Presentation/MySolution.Presentation.csproj
dotnet sln MySolution.sln add MySolution.Application/MySolution.Application.csproj
dotnet sln MySolution.sln add MySolution.Domain/MySolution.Domain.csproj
dotnet sln MySolution.sln add MySolution.Infrastructure/MySolution.Infrastructure.csproj
```

## 步骤 5：配置依赖项

**1. 引用项目：** 打开 `MySolution.Presentation.csproj` 文件，并添加对其他项目的引用：

```xml
<ItemGroup>
  <ProjectReference Include="..\MySolution.Application\MySolution.Application.csproj" />
  <ProjectReference Include="..\MySolution.Domain\MySolution.Domain.csproj" />
  <ProjectReference Include="..\MySolution.Infrastructure\MySolution.Infrastructure.csproj" />
</ItemGroup>
```

**2. 安装包：** 使用以下命令为每个项目安装所需的任何包：

```bash
dotnet add MySolution.Presentation package PackageName
dotnet add MySolution.Application package PackageName
dotnet add MySolution.Infrastructure package PackageName
```

## 步骤 6：配置 C# 10 功能

C# 10 引入了多项增强清晰架构开发的功能。让我们在项目中配置 C# 10 功能：

1.  **可空引用类型：** 通过在 `.csproj` 文件的 `<PropertyGroup>` 部分添加以下属性，在每个项目中启用可空引用类型：

```xml
<Nullable>enable</Nullable>
```

2.  **顶级语句：** 你可以在控制台应用程序中使用顶级语句，以获得更清晰、更简洁的入口点。在 `MySolution.Presentation` 的 `Program.cs` 文件中，将默认代码替换为：

```csharp
using System;

Console.WriteLine("Hello, Clean Architecture!");
```

## 步骤 7：设置开发环境

1.  **选择 IDE：** 使用你偏好的 C# 开发 IDE。Visual Studio、Visual Studio Code 和 JetBrains Rider 是热门选择。

2.  **安装扩展（可选）：** 安装任何能提高生产力并提供对 C# 10 和 .NET 6 功能支持的扩展或插件。

3.  **配置 Git（可选）：** 如果你使用版本控制，请配置 Git 并为你的解决方案初始化一个仓库。

## 步骤 8：开始开发

1.  **编写代码：** 开始为清晰架构应用程序的每一层编写代码。遵循关注点分离、依赖倒置和 SOLID 设计原则。

2.  **测试驱动开发（TDD）：** 考虑使用测试驱动开发，在实现功能之前编写测试，确保你的代码经过彻底测试并符合预期行为。

3.  **重构和迭代：** 持续重构代码以提高可读性、可维护性和性能。根据反馈和不断变化的需求迭代你的架构。

为清晰架构开发配置 .NET 6 和 C# 10 涉及设置项目结构、依赖项和开发环境。通过遵循本指南中概述的步骤，你可以创建一个组织良好的解决方案，并利用 C# 和 .NET 的最新功能来构建健壮且可维护的应用程序。清晰架构原则促进了关注点分离和模块化，使你的软件项目更易于维护、测试和扩展。

## 理解项目模板和清晰架构结构

项目模板为开发者提供了一个起点，用于创建具有预定义配置、结构和依赖项的新项目。在 C# 10 和 .NET 6 的背景下，项目模板对于有效实施清晰架构原则至关重要。在本指南中，我们将探讨项目模板以及它们如何促进清晰架构结构的创建，并提供基于 C# 10 和 .NET 6 的代码示例。

## .NET 中的项目模板

.NET 提供了多种针对不同类型应用程序量身定制的项目模板，包括控制台应用程序、Web API、MVC 应用程序和类库。这些模板提供了一个具有默认配置和结构的基础，使开发者能够专注于实现业务逻辑，而不是设置基础设施。

## 清晰架构结构

清晰架构倡导一种分层的架构模式，将关注点分离到不同的层中：表示层、应用层、领域层和基础设施层。每一层都有特定的职责，并通过定义良好的接口与相邻层交互。让我们分解清晰架构的结构：

1.  **表示层：** 负责用户界面逻辑和交互。它包括 UI 控制器、视图和视图模型等组件。在 Web 应用程序中，此层通常由控制器和视图组成，而在控制台应用程序中，它可能包括命令行界面或用户提示。
2.  **应用层：** 实现特定于应用程序的业务逻辑，并协调系统不同部分之间的交互。它充当表示层和领域层之间的桥梁，通常包含定义应用程序行为的用例或应用服务。
3.  **领域层：** 包含核心业务逻辑和领域实体。它代表应用程序的核心，封装了业务规则、行为和状态。此层中的实体应独立于任何外部关注点，仅专注于表示领域概念。
4.  **基础设施层：** 处理外部依赖，如数据库、文件系统或外部服务。它包括数据访问、日志记录、配置和其他横切关注点的实现细节。基础设施层与外部系统交互，并将实现细节从应用程序的其余部分抽象出来。

## 创建清晰架构项目

要使用 .NET 6 和 C# 10 创建清晰架构项目，我们将利用项目模板，并根据清晰架构原则构建解决方案。让我们逐步完成此过程：

**1. 创建解决方案：** 首先使用 `dotnet new sln` 命令创建一个新的解决方案：

```bash
dotnet new sln -n MySolution
```

**2. 创建项目：** 接下来，为清晰架构的每一层创建项目：

```bash
dotnet new console -n MySolution.Presentation
dotnet new classlib -n MySolution.Application
dotnet new classlib -n MySolution.Domain
dotnet new classlib -n MySolution.Infrastructure
```

**3. 将项目添加到解决方案：** 将新创建的项目添加到解决方案：

```bash
dotnet sln MySolution.sln add MySolution.Presentation/MySolution.Presentation.csproj
dotnet sln MySolution.sln add MySolution.Application/MySolution.Application.csproj
dotnet sln MySolution.sln add MySolution.Domain/MySolution.Domain.csproj
dotnet sln MySolution.sln add MySolution.Infrastructure/MySolution.Infrastructure.csproj
```

**4. 配置依赖项：** 在项目之间设置项目引用。表示层引用应用层，应用层引用领域层，基础设施层同时引用应用层和领域层。

**5. 实现清晰架构结构：** 根据清晰架构原则在每一层内编写代码。在领域层定义领域实体和业务逻辑，在应用层实现应用服务，并在基础设施层处理基础设施关注点。

项目模板为在 .NET 6 和 C# 10 应用程序中实现清晰架构结构奠定了基础。通过利用项目模板并遵循清晰架构原则，开发者可以创建结构良好、可维护且可测试的应用程序。理解清晰架构中每一层的作用以及它们如何相互交互，对于设计可扩展和健壮的软件系统至关重要。借助项目模板和清晰架构原则，开发者可以构建更易于理解、扩展和维护的软件。

## 第5章

## 在Clean Architecture中使用.NET 6进行依赖注入

## 依赖注入原则详解

依赖注入（DI）是软件开发中用于管理组件或类之间依赖关系的一种设计模式。它促进了松耦合，并提高了应用程序的可测试性、可维护性和可扩展性。在C# 10和.NET 6的背景下，理解依赖注入的原则对于有效实施Clean Architecture至关重要。在本指南中，我们将基于C# 10和.NET 6的代码示例，探讨依赖注入的原则。

## 什么是依赖注入？

依赖注入是一种技术，其中类的依赖项是外部提供的，而不是在类内部创建的。类不是直接创建其依赖项的实例，而是通过构造函数、属性或方法将这些依赖项注入到类中。这使得类与其依赖项解耦，使其更易于测试、维护和扩展。

## 依赖注入的三大原则：

1.  **依赖倒置原则（DIP）：** 依赖倒置原则指出，高层模块不应该依赖于低层模块，两者都应该依赖于抽象。该原则通过确保类依赖于接口或抽象类而不是具体实现，来促进组件之间的松耦合。

2.  **单一职责原则（SRP）：** 单一职责原则指出，一个类应该只有一个改变的理由。通过分离关注点并将职责委托给单独的类，SRP有助于减少耦合并提高代码的可维护性。依赖注入通过允许类专注于其主要职责，并将依赖项的管理委托给外部组件来促进SRP。

3.  **控制反转（IoC）：** 控制反转是一种设计原则，其中执行流程的控制权从调用者反转到外部组件。在依赖注入的背景下，IoC容器或框架负责管理对象的创建和生命周期，并将依赖项注入到类中。这使得类与其创建依赖项的职责解耦，并促进了灵活性和可扩展性。

## 在C# 10和.NET 6中实现依赖注入：

让我们说明如何在Clean Architecture场景中使用C# 10和.NET 6实现依赖注入：

```csharp
// 领域层
public interface IRepository<T>
{
    IEnumerable<T> GetAll();
    T GetById(int id);
}

public class Entity
{
    public int Id { get; set; }
    public string Name { get; set; }
}

// 基础设施层
public class Repository<T> : IRepository<T>
{
    private List<T> _entities = new List<T>();
    public void Add(T entity)
    {
        _entities.Add(entity);
    }
    public IEnumerable<T> GetAll()
    {
        return _entities;
    }
    public T GetById(int id)
    {
        return _entities.FirstOrDefault(e => e.Id == id);
    }
}

// 应用层
public class EntityService<T>
{
    private readonly IRepository<T> _repository;
    public EntityService(IRepository<T> repository)
    {
        _repository = repository;
    }
    public IEnumerable<T> GetAllEntities()
    {
        return _repository.GetAll();
    }
    public T GetEntityById(int id)
    {
        return _repository.GetById(id);
    }
}

// 表示层（控制台应用程序）
class Program
{
    static void Main(string[] args)
    {
        // 配置DI容器
        var services = new ServiceCollection();
        services.AddSingleton<IRepository<Entity>, Repository<Entity>>();
        services.AddSingleton<EntityService<Entity>>();
        var serviceProvider = services.BuildServiceProvider();

        // 解析服务
        var entityService = serviceProvider.GetRequiredService<EntityService<Entity>>();

        // 使用服务
        var entities = entityService.GetAllEntities();
        foreach (var entity in entities)
        {
            Console.WriteLine($"Id: {entity.Id}, Name: {entity.Name}");
        }
    }
}
```

在此示例中：

1.  `IRepository<T>`接口定义了访问存储库中实体的方法。
2.  `Repository<T>`类实现了存储库接口，并在内存中管理实体。
3.  `EntityService<T>`类依赖于存储库接口，并对实体执行操作。
4.  在表示层中，使用`Microsoft.Extensions.DependencyInjection`命名空间中的`ServiceCollection`和`ServiceProvider`类来配置和解析依赖项。

依赖注入是一种强大的设计模式，它促进了软件应用程序的松耦合、可维护性和可测试性。通过遵循依赖注入的原则并利用C# 10和.NET 6提供的功能，开发人员可以创建模块化、可扩展和可伸缩的应用程序。理解如何在Clean Architecture场景中实现依赖注入对于构建健壮且可维护的软件系统至关重要。

## 在C# 10和.NET 6中实现依赖注入

依赖注入（DI）是现代软件开发的一个关键方面，它促进了应用程序的松耦合和可测试性。随着C# 10和.NET 6的发布，实现依赖注入变得更加流畅和直观。在本指南中，我们将逐步介绍如何在Clean Architecture场景中使用C# 10和.NET 6实现依赖注入，并提供完整的代码示例。

## 设置依赖注入

首先，让我们使用C# 10和.NET 6设置一个Clean Architecture项目结构。我们将为表示层、应用层、领域层和基础设施层创建单独的项目。

**1. 创建解决方案：** 首先使用.NET CLI创建一个新的解决方案：

```bash
dotnet new sln -n MySolution
```

**2. 创建项目：** 为Clean Architecture的每一层创建项目：

```bash
dotnet new console -n MySolution.Presentation
dotnet new classlib -n MySolution.Application
dotnet new classlib -n MySolution.Domain
dotnet new classlib -n MySolution.Infrastructure
```

**3. 将项目添加到解决方案：** 将项目添加到解决方案文件：

```bash
dotnet sln MySolution.sln add MySolution.Presentation/MySolution.Presentation.csproj
dotnet sln MySolution.sln add MySolution.Application/MySolution.Application.csproj
dotnet sln MySolution.sln add MySolution.Domain/MySolution.Domain.csproj
dotnet sln MySolution.sln add MySolution.Infrastructure/MySolution.Infrastructure.csproj
```

## 实现依赖注入

现在，让我们在Clean Architecture项目中实现依赖注入。我们将定义接口、具体实现，并在表示层配置依赖注入。

**1. 定义接口：**

在领域层（`MySolution.Domain`）中，为存储库和其他任何服务定义接口：

```csharp
// IRepository.cs
namespace MySolution.Domain
{
    public interface IRepository<T>
    {
        IEnumerable<T> GetAll();
        T GetById(int id);
    }
}
```

**2. 实现存储库：**

在基础设施层（`MySolution.Infrastructure`）中，实现存储库接口：

```csharp
// Repository.cs
using MySolution.Domain;
using System.Collections.Generic;
using System.Linq;

namespace MySolution.Infrastructure
{
    public class Repository<T> : IRepository<T>
    {
        private List<T> _entities = new List<T>();
        public void Add(T entity)
        {
            _entities.Add(entity);
        }
        public IEnumerable<T> GetAll()
        {
            return _entities;
        }
        public T GetById(int id)
        {
            return _entities.FirstOrDefault(e => e.Id == id);
        }
    }
}
```

**3. 配置依赖注入：**

在表示层（`MySolution.Presentation`）中，使用内置的`Microsoft.Extensions.DependencyInjection`命名空间配置依赖注入：

```csharp
// Program.cs
using Microsoft.Extensions.DependencyInjection;
using MySolution.Application;
using MySolution.Domain;
using MySolution.Infrastructure;
using System;

namespace MySolution.Presentation
{
    class Program
    {
        static void Main(string[] args)
        {
            // 设置DI容器
            var serviceProvider = new ServiceCollection()
```

## 4. 使用依赖注入：

在应用层（`MySolution.Application`）中，使用依赖注入来访问仓储：

```csharp
// EntityService.cs
using MySolution.Domain;
using System.Collections.Generic;

namespace MySolution.Application
{
    public class EntityService
    {
        private readonly IRepository<Entity> _repository;

        public EntityService(IRepository<Entity> repository)
        {
            _repository = repository;
        }

        public IEnumerable<Entity> GetAllEntities()
        {
            return _repository.GetAll();
        }
    }
}
```

在 C# 10 和 .NET 6 中实现依赖注入非常直接，并且能带来诸多好处，包括提升可测试性、可维护性和灵活性。通过遵循整洁架构原则并使用 .NET 提供的内置依赖注入功能，开发者可以创建模块化且可扩展的应用程序。理解如何设置和配置依赖注入，对于在现代开发环境中构建健壮且可维护的软件系统至关重要。

## 依赖注入在实现松耦合和可测试性方面的优势

依赖注入（DI）是一种强大的设计模式，它促进了软件应用程序中组件之间的松耦合。它还通过在单元测试期间更容易地隔离依赖，极大地增强了代码的可测试性。在 C# 10 和 .NET 6 的背景下，在整洁架构场景中实现依赖注入能带来诸多好处。让我们结合基于 C# 10 和 .NET 6 的代码示例，来探讨这些好处以及它们如何促进松耦合和可测试性。

## 通过依赖注入实现松耦合

- 1. **解耦依赖：** 依赖注入通过从外部提供依赖来解耦类与其依赖项。这意味着一个类不需要知道如何创建它的依赖项；它只需依赖于这些依赖项被提供即可。
- 2. **依赖倒置原则（DIP）：** 依赖注入有助于遵循依赖倒置原则，即高层模块依赖于抽象而非具体实现。这促进了软件设计的模块化和灵活性。
- 3. **灵活性和可扩展性：** 通过解耦依赖，DI 允许在不影响系统其余部分的情况下轻松替换或修改组件。这种灵活性使其更容易适应不断变化的需求或集成新功能。

## 通过依赖注入提升可测试性

- 1. **依赖隔离：** 通过依赖注入，在单元测试期间可以轻松地将依赖替换为模拟（mock）或存根（stub）实现。这允许开发者隔离被测试的组件，并专注于独立验证其行为。
- 2. **改进的单元测试：** DI 通过提供控制和操作依赖的能力，实现了更有效的单元测试。这确保了测试是可靠的、确定性的，并且专注于单个组件的行为，而不是它们与外部系统的交互。
- 3. **模拟框架集成：** DI 框架通常与模拟框架无缝集成，进一步增强了测试能力。可以使用 Moq 或 NSubstitute 等模拟框架，以最小的工作量创建依赖项的模拟实现。

## 在整洁架构中实现依赖注入

让我们用一个基于 C# 10 和 .NET 6 在整洁架构场景下的代码示例来说明依赖注入的好处：

```csharp
// 领域层

public interface IRepository<T>
{
    IEnumerable<T> GetAll();
    T GetById(int id);
}

public class Entity
{
    public int Id { get; set; }
    public string Name { get; set; }
}

// 基础设施层

public class Repository<T> : IRepository<T>
{
    private List<T> _entities = new List<T>();

    public void Add(T entity)
    {
        _entities.Add(entity);
    }

    public IEnumerable<T> GetAll()
    {
        return _entities;
    }

    public T GetById(int id)
    {
        return _entities.FirstOrDefault(e => e.Id == id);
    }
}

// 应用层
public class EntityService
{
    private readonly IRepository<Entity> _repository;

    public EntityService(IRepository<Entity> repository)
    {
        _repository = repository;
    }

    public IEnumerable<Entity> GetAllEntities()
    {
        return _repository.GetAll();
    }
}

// 表现层（单元测试）
[TestClass]
public class EntityServiceTests
{
    [TestMethod]
    public void GetAllEntities_Returns_All_Entities()
    {
        // 准备
        var mockRepository = new Mock<IRepository<Entity>>();
        mockRepository.Setup(r => r.GetAll()).Returns(new List<Entity>
        {
            new Entity { Id = 1, Name = "Entity 1" },
            new Entity { Id = 2, Name = "Entity 2" },
            new Entity { Id = 3, Name = "Entity 3" }
        });

        var entityService = new EntityService(mockRepository.Object);

        // 执行
        var entities = entityService.GetAllEntities();

        // 断言
        Assert.AreEqual(3, entities.Count());
    }
}
```

在此示例中：

- 1. `EntityService` 类依赖于 `IRepository<Entity>` 接口。
- 2. 在单元测试期间，向 `EntityService` 类提供了一个仓储的模拟实现。
- 3. 测试验证了 `GetAllEntities` 方法返回了预期数量的实体。

依赖注入为软件开发带来了显著的好处，特别是在松耦合和可测试性方面。通过解耦组件并提供易于替换依赖的机制，DI 促进了模块化、灵活且可维护的代码。在整洁架构场景中，使用 C# 10 和 .NET 6 实现依赖注入增强了软件系统的设计、模块化和可测试性，最终带来更高质量和更易维护的应用程序。

## 第六章

## 构建核心逻辑：业务规则层

## 在整洁架构中定义业务规则和用例

在整洁架构中，定义清晰的业务规则和用例对于创建可维护、可扩展且符合业务需求的软件系统至关重要。业务规则代表了控制系统行为的逻辑和约束，而用例则描述了参与者（用户或外部系统）与系统之间的交互，以实现特定目标。在本指南中，我们将探讨如何在整洁架构的背景下定义业务规则和用例，并附上基于 C# 10 和 .NET 6 的代码示例。

## 定义业务规则

业务规则封装了定义系统如何运作和表现的逻辑和约束。这些规则源自业务领域的需求，代表了系统的核心功能。在实现整洁架构时，清晰地识别和记录这些业务规则至关重要，以确保软件解决方案与业务目标保持一致。

## 业务规则定义示例

让我们考虑一个银行应用程序中简单业务规则的示例：

```csharp
// 领域层

public class Account
{
    public decimal Balance { get; private set; }

    public Account(decimal initialBalance)
    {
        if (initialBalance < 0)
        {
            throw new ArgumentException("Initial balance cannot be negative.");
        }

        Balance = initialBalance;
    }
}
```

public void Deposit(decimal amount)
{
    if (amount <= 0)
    {
        throw new ArgumentException("存款金额必须为正数。");
    }

    Balance += amount;
}

public void Withdraw(decimal amount)
{
    if (amount <= 0)
    {
        throw new ArgumentException("取款金额必须为正数。");
    }

    if (amount > Balance)
    {
        throw new InvalidOperationException("余额不足。");
    }

    Balance -= amount;
}
}

在此示例中，业务规则规定账户的初始余额不能为负数。此外，存款和取款操作必须使用正数金额，且取款金额不能超过账户余额。

## 定义用例

用例描述了参与者（用户或外部系统）与系统之间的交互，以完成特定任务或目标。每个用例代表系统内一个独立且有意义的功能模块。在整洁架构中，用例被实现为应用服务，用于协调领域实体与基础设施组件之间的交互。

## 用例定义示例

继续以银行应用为例，我们来定义一个在两个账户之间转账的用例：

```csharp
// 应用层

public class TransferFundsUseCase
{
    private readonly IRepository<Account> _accountRepository;

    public TransferFundsUseCase(IRepository<Account> accountRepository)
    {
        _accountRepository = accountRepository;
    }

    public void Execute(int sourceAccountId, int targetAccountId, decimal amount)
    {
        var sourceAccount = _accountRepository.GetById(sourceAccountId);
        var targetAccount = _accountRepository.GetById(targetAccountId);

        if (sourceAccount == null || targetAccount == null)
        {
            throw new ArgumentException("无效的账户ID。");
        }

        sourceAccount.Withdraw(amount);
        targetAccount.Deposit(amount);

        _accountRepository.Update(sourceAccount);
        _accountRepository.Update(targetAccount);
    }
}
```

在此用例中，`Execute` 方法协调两个账户之间的资金转移。它从仓储中获取源账户和目标账户，执行必要的取款和存款操作，并在仓储中更新这些账户。

定义清晰的业务规则和用例是软件项目成功的基础，尤其是在整洁架构的背景下。通过清晰地识别和记录业务规则，开发者可以确保软件解决方案满足业务领域的需求并正确运行。同样，定义用例有助于澄清系统的功能需求，并指导应用服务的实现，这些服务协调系统的行为。有了明确定义的业务规则和用例，开发者可以创建健壮、可维护且符合业务需求的软件系统。

## 在 C# 10 中实现可维护的业务规则层

在整洁架构中，业务规则层封装了控制系统行为的核心逻辑和约束。有效地实现这一层对于构建可维护、可扩展和健壮的软件应用至关重要。在本指南中，我们将探讨如何在整洁架构的背景下，使用 C# 10 实现业务规则层，并重点关注增强可维护性的原则。我们将提供基于 C# 10 和 .NET 6 的代码示例来阐述关键概念。

## 业务规则层的结构

业务规则层通常位于整洁架构项目的领域层内。它由领域实体、值对象和封装应用核心业务逻辑的服务组成。通过有效地组织业务规则层，开发者可以确保系统的行为保持一致且易于维护。

## 可维护业务规则层的原则

1.  **单一职责原则 (SRP)：** 业务规则层中的每个类都应该只有一个职责，封装领域逻辑的特定方面。这确保了类是专注的、内聚的，并且更容易维护。
2.  **封装：** 将领域逻辑封装在领域实体和服务中，以促进模块化和封装性。避免在业务规则层之外暴露内部实现细节，以保持抽象和灵活性。
3.  **依赖倒置原则 (DIP)：** 依赖抽象而非具体实现，以实现灵活性和可扩展性。此原则允许更容易地替换组件，并促进业务规则层内的解耦。

## 实现业务规则层的示例

让我们考虑一个为简单电子商务应用实现业务规则层的示例：

```csharp
// 领域层
public class Product
{
    public int Id { get; private set; }
    public string Name { get; private set; }
    public decimal Price { get; private set; }
    public int StockQuantity { get; private set; }

    public Product(int id, string name, decimal price, int stockQuantity)
    {
        Id = id;
        Name = name;
        Price = price;
        StockQuantity = stockQuantity;
    }

    public void AddStock(int quantity)
    {
        if (quantity <= 0)
        {
            throw new ArgumentException("数量必须为正数。");
        }
        StockQuantity += quantity;
    }

    public void RemoveStock(int quantity)
    {
        if (quantity <= 0)
        {
            throw new ArgumentException("数量必须为正数。");
        }
        if (quantity > StockQuantity)
        {
            throw new InvalidOperationException("库存不足。");
        }
        StockQuantity -= quantity;
    }
}

// 应用层
public class ProductService
{
    private readonly IRepository<Product> _productRepository;

    public ProductService(IRepository<Product> productRepository)
    {
        _productRepository = productRepository;
    }

    public void AddStockToProduct(int productId, int quantity)
    {
        var product = _productRepository.GetById(productId);
        if (product == null)
        {
            throw new ArgumentException("未找到产品。");
        }
        product.AddStock(quantity);
        _productRepository.Update(product);
    }

    public void RemoveStockFromProduct(int productId, int quantity)
    {
        var product = _productRepository.GetById(productId);
        if (product == null)
        {
            throw new ArgumentException("未找到产品。");
        }
        product.RemoveStock(quantity);
        _productRepository.Update(product);
    }
}
```

在此示例中：

- `Product` 类代表一个领域实体，封装了电子商务系统中与产品相关的核心逻辑。
- `ProductService` 类提供管理产品的应用级服务，例如添加和移除库存数量。
- 依赖注入用于将仓储注入到服务类中，遵循整洁架构的原则。

在整洁架构的背景下，使用 C# 10 实现业务规则层对于构建可维护和健壮的软件应用至关重要。通过遵循 SRP、封装和 DIP 等原则，开发者可以创建一个专注、模块化且易于扩展的业务规则层。通过明确定义的领域实体和服务，开发者可以确保系统的行为保持一致并符合业务领域的需求。这种方法最终使得软件应用更易于维护、扩展和随时间演进。

## 对业务规则层进行单元测试以提升代码质量和信心

单元测试是软件开发中的一项基本实践，它确保了代码质量、可靠性和可维护性。在整洁架构和使用 .NET 6 的 C# 10 背景下，对业务规则层进行单元测试对于验证核心领域逻辑的正确性以及增强对系统的信心至关重要。在本指南中，我们将探讨对业务规则层进行单元测试的重要性，并提供基于 C# 10 和 .NET 6 的代码示例，以演示如何编写有效的单元测试。

## 对业务规则层进行单元测试的重要性

1.  **验证业务逻辑：** 单元测试验证在领域实体和服务的行为符合预期。通过单独测试每个组件，开发人员可以确保每段逻辑都能正确运行。

2. **早期发现缺陷：** 单元测试有助于在开发过程的早期识别业务规则层中的缺陷和问题。通过在单元测试层面捕获错误，开发人员可以在问题扩散到系统其他部分之前解决它们。

3. **代码信心与重构：** 单元测试为在业务规则层内进行更改或重构代码提供了信心。开发人员可以放心地进行重构，因为他们知道单元测试会捕获回归问题，并确保系统的行为保持一致。

## 编写有效的单元测试

要为业务规则层编写有效的单元测试，请遵循以下最佳实践：

1. **每个测试只测试一个行为：** 每个单元测试应专注于测试代码的单个行为或方面。这使得测试更具可读性、可维护性，并且更容易调试。

2. **使用描述性的测试名称：** 为单元测试选择描述性的名称，清楚地表明正在测试的行为。这提高了测试套件的可读性和清晰度。

3. **准备-执行-断言（AAA）模式：** 使用准备-执行-断言模式来组织单元测试，其中测试设置（准备）、被测代码的执行（执行）和预期行为的验证（断言）被清晰地分开。

4. **使用模拟和存根：** 模拟或存根外部依赖，以隔离被测代码，并专注于单独测试各个组件。这有助于避免意外的副作用，并使测试更可靠。

## 业务规则层单元测试示例

让我们继续使用电子商务应用程序示例，为 `Product` 实体和 `ProductService` 类编写单元测试：

```csharp
// Product 实体的单元测试

[TestClass]
public class ProductTests
{
    [TestMethod]
    public void AddStock_Should_Increase_StockQuantity()
    {
        // 准备
        var product = new Product(1, "Test Product", 100, 10);
        // 执行
        product.AddStock(5);
        // 断言
        Assert.AreEqual(15, product.StockQuantity);
    }

    [TestMethod]
    public void RemoveStock_Should_Decrease_StockQuantity()
    {
        // 准备
        var product = new Product(1, "Test Product", 100, 10);
        // 执行
        product.RemoveStock(3);
        // 断言
        Assert.AreEqual(7, product.StockQuantity);
    }
}

// ProductService 的单元测试
[TestClass]
public class ProductServiceTests
{
    [TestMethod]
    public void AddStockToProduct_Should_Increase_StockQuantity()
    {
        // 准备
        var mockRepository = new Mock<IRepository<Product>>();
        var product = new Product(1, "Test Product", 100, 10);
        mockRepository.Setup(r => r.GetById(1)).Returns(product);
        var productService = new ProductService(mockRepository.Object);

        // 执行
        productService.AddStockToProduct(1, 5);

        // 断言
        Assert.AreEqual(15, product.StockQuantity);
    }
}
```

在这些单元测试中：

- `ProductTests` 类包含对 `Product` 实体的 `AddStock` 和 `RemoveStock` 方法的测试。
- `ProductServiceTests` 类包含对 `ProductService` 类的 `AddStockToProduct` 方法的测试，使用了模拟仓库。

对业务规则层进行单元测试对于确保软件应用程序的代码质量、可靠性和可维护性至关重要。通过编写有效的单元测试来验证领域实体和服务的行为，开发人员可以建立对系统正确性的信心，并在开发过程的早期检测到缺陷。在基于 C# 10 和 .NET 6 的整洁架构项目中，对业务规则层进行单元测试是开发工作流程的一个关键方面，有助于提高软件解决方案的整体质量和稳定性。

# 第 7 章

## 表示层：用户界面与交互

### 设计用户界面时考虑关注点分离

在整洁架构中，关注点分离是一个基本原则，它促进了软件系统的模块化、可维护性和可扩展性。在 C# 10 和 .NET 6 的背景下设计用户界面（UI）时，遵守这一原则至关重要，以确保 UI 与业务逻辑和基础设施关注点保持解耦。在本指南中，我们将探讨如何在设计用户界面时考虑关注点分离，并附上基于 C# 10 和 .NET 6 的代码示例。

### 用户界面设计中的关注点分离

用户界面设计中的关注点分离涉及将 UI 划分为不同的组件，每个组件负责呈现或行为的特定方面。通过分离关注点，开发人员可以在 UI 代码库中实现更高的模块化、可测试性和可维护性。

### UI 设计中关注点分离的关键组件：

1. **视图组件：** 代表 UI 的视觉元素，如屏幕、表单或小部件。视图组件负责渲染 UI 元素和捕获用户输入。
2. **视图模型：** 充当 UI 和业务逻辑层之间的中介，包含特定于 UI 需求的数据和行为。视图模型封装了表示逻辑，并促进了 UI 和底层业务实体之间的数据绑定。
3. **表示逻辑：** 处理用户交互、输入验证和其他与 UI 相关的逻辑。此逻辑应封装在 UI 组件内，以保持 UI 代码库的专注和可维护性。

### 使用整洁架构设计用户界面

在整洁架构项目中设计用户界面时，请遵循以下准则以确保关注点分离：

1. **定义清晰的边界：** 清晰地定义 UI 层与应用程序其他层（如应用层和领域层）之间的边界。使用接口或抽象将 UI 组件与业务逻辑和基础设施关注点解耦。
2. **将业务逻辑委托给应用层：** 将复杂的业务逻辑和用例委托给应用层，使 UI 层专注于表示关注点。这确保了 UI 保持轻量级和响应性。
3. **使用视图模型进行数据绑定：** 使用视图模型来表示特定于 UI 需求的数据和行为。视图模型应封装表示逻辑，并在 UI 和业务逻辑层之间提供清晰的契约。

### 关注点分离的 UI 设计示例

让我们考虑一个为待办事项列表应用程序设计简单用户界面的示例：

```csharp
// 表示层

public class TodoItemViewModel
{
    public int Id { get; set; }
    public string Title { get; set; }
    public bool IsCompleted { get; set; }
}

public interface ITodoService
{
    IEnumerable<TodoItemViewModel> GetAllTodoItems();
    void AddTodoItem(TodoItemViewModel todoItem);
    void UpdateTodoItem(TodoItemViewModel todoItem);
    void DeleteTodoItem(int id);
}

public class TodoListViewModel
{
    private readonly ITodoService _todoService;
    public ObservableCollection<TodoItemViewModel> TodoItems { get; } = new ObservableCollection<TodoItemViewModel>();

    public TodoListViewModel(ITodoService todoService)
    {
        _todoService = todoService;
        LoadTodoItems();
    }

    private void LoadTodoItems()
    {
        TodoItems.Clear();
        var todoItems = _todoService.GetAllTodoItems();
        foreach (var todoItem in todoItems)
        {
            TodoItems.Add(todoItem);
        }
    }

    public void AddTodoItem(string title)
    {
        var newTodoItem = new TodoItemViewModel { Title = title };
        _todoService.AddTodoItem(newTodoItem);
        TodoItems.Add(newTodoItem);
    }

    public void UpdateTodoItem(TodoItemViewModel todoItem)
    {
        _todoService.UpdateTodoItem(todoItem);
    }

    public void DeleteTodoItem(int id)
    {
        _todoService.DeleteTodoItem(id);
        var todoItemToRemove = TodoItems.FirstOrDefault(item => item.Id == id);
        if (todoItemToRemove != null)
        {
            TodoItems.Remove(todoItemToRemove);
        }
    }
}
```

## 从表示层消费业务逻辑层

在整洁架构中，表示层负责与用户交互并向其呈现信息。该层应与业务逻辑层解耦，以确保应用程序的模块化、可维护性和可测试性。从表示层消费业务逻辑层涉及以清晰且解耦的方式访问和调用业务逻辑层提供的功能。在本指南中，我们将探讨如何在基于 .NET 6 构建的 C# 10 应用程序中，从表示层消费业务逻辑层，代码示例将遵循整洁架构原则。

## 消费业务逻辑层的原则

- 1. **依赖注入：** 使用依赖注入，从表示层提供对业务逻辑层组件的访问。这使得表示层可以依赖抽象而非具体实现，从而促进松耦合和灵活性。
- 2. **接口隔离：** 在业务逻辑层中定义清晰的接口，仅暴露表示层所需的功能。这确保了表示层只依赖于它所需的功能，避免了不必要的耦合。
- 3. **封装：** 将复杂的业务逻辑封装在业务逻辑层内部，并通过定义良好的接口将其暴露出来。这隐藏了实现细节，并促进了表示层与业务逻辑层之间的关注点分离。

## 从表示层消费业务逻辑层

让我们考虑一个在简单的待办事项列表应用程序中，从表示层消费业务逻辑层的示例：

```csharp
// 业务逻辑层（应用层）

public interface ITodoService
{
    IEnumerable<TodoItem> GetAllTodoItems();
    void AddTodoItem(TodoItem todoItem);
    void UpdateTodoItem(TodoItem todoItem);
    void DeleteTodoItem(int id);
}

public class TodoService : ITodoService
{
    private readonly IRepository<TodoItem> _todoRepository;
    public TodoService(IRepository<TodoItem> todoRepository)
    {
        _todoRepository = todoRepository;
    }
    public IEnumerable<TodoItem> GetAllTodoItems()
    {
        return _todoRepository.GetAll();
    }
    public void AddTodoItem(TodoItem todoItem)
    {
        _todoRepository.Add(todoItem);
    }
    public void UpdateTodoItem(TodoItem todoItem)
    {
        _todoRepository.Update(todoItem);
    }
    public void DeleteTodoItem(int id)
    {
        var todoItem = _todoRepository.GetById(id);
        if (todoItem != null)
        {
            _todoRepository.Delete(todoItem);
        }
    }
}
// 表示层
public class TodoListViewModel
{
    private readonly ITodoService _todoService;
    public ObservableCollection<TodoItem> TodoItems { get; } = new ObservableCollection<TodoItem>();

    public TodoListViewModel(ITodoService todoService)
    {
        _todoService = todoService;
        LoadTodoItems();
    }

    private void LoadTodoItems()
    {
        TodoItems.Clear();
        var todoItems = _todoService.GetAllTodoItems();
        foreach (var todoItem in todoItems)
        {
            TodoItems.Add(todoItem);
        }
    }

    public void AddTodoItem(string title)
    {
        var newTodoItem = new TodoItem { Title = title };
        _todoService.AddTodoItem(newTodoItem);
        TodoItems.Add(newTodoItem);
    }

    public void UpdateTodoItem(TodoItem todoItem)
    {
        _todoService.UpdateTodoItem(todoItem);
    }

    public void DeleteTodoItem(int id)
    {
        _todoService.DeleteTodoItem(id);

        var todoItemToRemove = TodoItems.FirstOrDefault(item => item.Id == id);

        if (todoItemToRemove != null)
        {
            TodoItems.Remove(todoItemToRemove);
        }
    }
}
```

在此示例中：

- 1. 业务逻辑层（`TodoService`）定义了一个接口 `ITodoService`，以暴露待办事项列表管理操作。
- 2. 表示层（`TodoListViewModel`）通过依赖注入消费 `ITodoService` 接口，从而与业务逻辑层交互。

从表示层消费业务逻辑层是整洁架构的一个关键方面，它确保了表示层与底层业务逻辑保持解耦。通过遵循依赖注入、接口隔离和封装等原则，开发者可以创建模块化且易于维护的应用程序。在表示层和业务逻辑层之间分离关注点，能够实现灵活性、可扩展性和可测试性，从而便于软件系统随时间推移进行演进和维护。

## 在表示层实现依赖注入以增强灵活性

依赖注入（DI）是一种强大的设计模式，它通过将依赖与其消费者解耦，来促进软件系统中的松耦合和灵活性。在整洁架构以及使用 .NET 6 的 C# 10 的背景下，在表示层实现依赖注入可以增强灵活性和可维护性。它允许表示层中的组件依赖于抽象而非具体实现，从而便于进行更轻松的测试、扩展和应用程序演进。在本指南中，我们将探讨如何在整洁架构应用程序的表示层中实现依赖注入，并提供基于 C# 10 和 .NET 6 的代码示例。

## 在表示层使用依赖注入的好处

- 1. **解耦：** 依赖注入将表示层中的组件与其依赖解耦，减少了紧耦合并促进了模块化。这使得在不影响系统其余部分的情况下替换或修改依赖变得更加容易。
- 2. **可测试性**：通过依赖抽象而非具体实现，表示层中的组件变得更容易测试。在测试期间可以提供模拟或桩实现，从而允许进行专注于特定行为的隔离单元测试。
- 3. **灵活性**：依赖注入通过促进使用依赖的不同实现，为表示层提供了更大的灵活性。这使得开发者能够更轻松地使应用程序适应不断变化的需求或集成新功能。

## 在表示层实现依赖注入

让我们演示如何在整洁架构应用程序的表示层中实现依赖注入：

```csharp
// 表示层

public interface ITodoListViewModel
{
    ObservableCollection<TodoItem> TodoItems { get; }

    void AddTodoItem(string title);

    void UpdateTodoItem(TodoItem todoItem);

    void DeleteTodoItem(int id);
}

public class TodoListViewModel : ITodoListViewModel
{
    private readonly ITodoService _todoService;

    public ObservableCollection<TodoItem> TodoItems { get; } = new ObservableCollection<TodoItem>();

    public TodoListViewModel(ITodoService todoService)
    {
        _todoService = todoService;

        LoadTodoItems();
    }

    private void LoadTodoItems()
    {
        // 加载待办事项的实现
    }
}
```

## 第8章

### 使用 .NET 实现数据持久化

### 选择合适的数据访问技术（.NET Entity Framework Core）

在整洁架构中，选择合适的数据访问技术对于构建可扩展、可维护和高效的应用程序至关重要。.NET Entity Framework Core 因其易用性、灵活性和丰富的功能集，成为 .NET 应用程序中数据访问的热门选择。在本指南中，我们将探讨在基于整洁架构原则的 C# 10 应用程序中，选择 .NET Entity Framework Core 作为数据访问技术的考量因素，并附有代码示例。

### 选择 .NET Entity Framework Core 的考量因素

1.  **易用性：** .NET Entity Framework Core 在数据库之上提供了高级抽象，允许开发者使用熟悉的面向对象概念（如实体、关系和 LINQ 查询）与数据库交互。这简化了数据访问代码，并减少了所需的样板代码量。
2.  **ORM 功能：** .NET Entity Framework Core 提供了广泛的功能，如自动变更跟踪、延迟加载和查询翻译。这些功能通过自动处理许多常见的数据库操作，简化了开发并提高了生产力。
3.  **跨平台支持：** .NET Entity Framework Core 是跨平台的，可用于 .NET Core、.NET Framework 和 .NET 5/6。这确保了在不同环境中的兼容性，并使开发者能够构建可在各种操作系统上运行的应用程序。
4.  **性能：** .NET Entity Framework Core 相较于其前代版本在性能上有了显著提升，为读写操作提供了更好的性能。它还提供了查询缓存和编译查询等功能，以进一步优化性能。
5.  **与整洁架构的集成：** .NET Entity Framework Core 与整洁架构原则集成良好，允许开发者设计与应用程序其他层解耦的数据访问代码。这有助于应用程序的测试、维护和演进。

### 在整洁架构中使用 .NET Entity Framework Core 的示例

让我们演示如何在整洁架构应用程序中使用 .NET Entity Framework Core 与数据库交互：

```csharp
// 基础设施层

public class TodoDbContext : DbContext
{
    public TodoDbContext(DbContextOptions<TodoDbContext> options) : base(options)
    {
    }

    public DbSet<TodoItem> TodoItems { get; set; }
}

public class TodoRepository : IRepository<TodoItem>
{
    private readonly TodoDbContext _dbContext;

    public TodoRepository(TodoDbContext dbContext)
    {
        _dbContext = dbContext;
    }

    public IEnumerable<TodoItem> GetAll()
    {
        return _dbContext.TodoItems.ToList();
    }

    public TodoItem GetById(int id)
    {
        return _dbContext.TodoItems.Find(id);
    }

    public void Add(TodoItem entity)
    {
        _dbContext.TodoItems.Add(entity);
        _dbContext.SaveChanges();
    }

    public void Update(TodoItem entity)
    {
        _dbContext.TodoItems.Update(entity);
        _dbContext.SaveChanges();
    }

    public void Delete(TodoItem entity)
    {
        _dbContext.TodoItems.Remove(entity);
        _dbContext.SaveChanges();
    }
}
```

在此示例中：

1.  `TodoDbContext` 类代表数据库上下文，并提供对 `TodoItem` 实体的访问。
2.  `TodoRepository` 类实现了仓储模式，并使用 .NET Entity Framework Core 与数据库交互。

### 在 Startup 类中配置 Entity Framework Core

要在应用程序中配置 .NET Entity Framework Core，你需要在 startup 类中注册数据库上下文和仓储：

```csharp
// Startup 配置
public void ConfigureServices(IServiceCollection services)
{
    services.AddDbContext<TodoDbContext>(options =>
        options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));

    services.AddScoped<IRepository<TodoItem>, TodoRepository>();

    // 其他服务注册...
}
```

选择合适的数据访问技术对于整洁架构应用程序的成功至关重要。.NET Entity Framework Core 提供了诸多优势，如易用性、跨平台支持以及与整洁架构原则的集成。通过利用 .NET Entity Framework Core，开发者可以构建健壮、可维护且高效的应用程序，并能轻松扩展。无论你是在构建小型应用程序还是大型企业系统，.NET Entity Framework Core 都提供了必要的工具和功能，以满足你的数据访问需求，同时遵循整洁架构原则。

### 定义数据模型和映射实体以实现持久化

定义数据模型和映射实体以实现持久化是软件开发的一个关键方面，尤其是在使用 C# 10 和 .NET 6 的整洁架构背景下。在本指南中，我们将深入探讨什么是数据模型、如何定义它们，以及如何在 C# 10 和 .NET 6 中映射实体以实现持久化。

### 什么是数据模型？

数据模型代表了系统中数据的结构和关系。它们是软件应用程序中组织和操作数据的蓝图。在 C# 10 和 .NET 6 中，数据模型通常使用类来表示。

让我们为一个博客应用程序定义一个简单的数据模型：

```csharp
public class Post
{
    public int Id { get; set; }
    public string Title { get; set; }
    public string Content { get; set; }
    public DateTime CreatedAt { get; set; }
    public DateTime UpdatedAt { get; set; }
}
```

在此示例中，`Post` 类代表一篇博客文章，具有 `Id`、`Title`、`Content`、`CreatedAt` 和 `UpdatedAt` 等属性。

### 映射实体以实现持久化

映射实体以实现持久化涉及定义数据模型如何从数据源（如数据库）存储和检索。在 C# 10 和 .NET 6 中，这通常通过使用像 Entity Framework Core 这样的对象关系映射器（ORM）来实现。

在此示例中：

1.  `TodoListViewModel` 类实现了一个接口 `ITodoListViewModel`，该接口定义了在表示层与待办事项交互的契约。
2.  `TodoListViewModel` 类依赖于一个抽象 `ITodoService` 来与待办事项交互，从而提供了灵活性和可测试性。

## 使用依赖注入容器注册依赖

要在表示层使用依赖注入，需要将依赖注册到依赖注入容器中。在应用程序的 startup 配置中，可以按如下方式注册依赖：

```csharp
// 依赖注入配置

services.AddSingleton<ITodoService, TodoService>();

services.AddSingleton<ITodoListViewModel, TodoListViewModel>();
```

在整洁架构应用程序的表示层实现依赖注入，可以提升灵活性、可测试性和可维护性。通过依赖抽象而非具体实现，表示层中的组件变得更容易测试，并且更能适应不断变化的需求。分离关注点和解耦依赖关系允许更高的模块化和可扩展性，使应用程序更容易随时间演进。通过依赖注入，开发者可以构建健壮、可维护且可扩展的整洁架构应用程序。

```csharp
{
    TodoItems.Clear();
    var todoItems = _todoService.GetAllTodoItems();
    foreach (var todoItem in todoItems)
    {
        TodoItems.Add(todoItem);
    }
}

public void AddTodoItem(string title)
{
    var newTodoItem = new TodoItem { Title = title };
    _todoService.AddTodoItem(newTodoItem);
    TodoItems.Add(newTodoItem);
}

public void UpdateTodoItem(TodoItem todoItem)
{
    _todoService.UpdateTodoItem(todoItem);
}

public void DeleteTodoItem(int id)
{
    _todoService.DeleteTodoItem(id);
    var todoItemToRemove = TodoItems.FirstOrDefault(item => item.Id == id);
    if (todoItemToRemove != null)
    {
        TodoItems.Remove(todoItemToRemove);
    }
}
```

让我们创建一个 `DbContext` 并映射 `Post` 实体以进行持久化：

```csharp
using Microsoft.EntityFrameworkCore;

public class BlogDbContext : DbContext
{
    public DbSet<Post> Posts { get; set; }

    protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
    {
        optionsBuilder.UseSqlServer("your_connection_string_here");
    }

    protected override void OnModelCreating(ModelBuilder modelBuilder)
    {
        modelBuilder.Entity<Post>(entity =>
        {
            entity.ToTable("Posts");
            entity.HasKey(e => e.Id);
            entity.Property(e => e.Title).IsRequired().HasMaxLength(100);
            entity.Property(e => e.Content).IsRequired();
            entity.Property(e => e.CreatedAt).IsRequired();
            entity.Property(e => e.UpdatedAt).IsRequired();
        });
    }
}
```

在这段代码中：

1.  我们定义了一个 `BlogDbContext` 类，它继承自 Entity Framework Core 提供的 `DbContext`。
2.  我们创建了一个 `DbSet<Post>` 属性来表示 `Post` 实体的集合。
3.  在 `OnConfiguring` 方法中，我们指定了数据库提供程序和连接字符串。
4.  在 `OnModelCreating` 方法中，我们定义了 `Post` 实体的配置。这包括指定表名、主键和列映射。

## 使用 DbContext

既然我们已经定义了 `DbContext` 并映射了 `Post` 实体，我们就可以用它来与数据库交互了：

```csharp
using System;
using System.Linq;
class Program
{
    static void Main(string[] args)
    {
        using var dbContext = new BlogDbContext();
        // 创建一个新帖子
        var newPost = new Post
        {
            Title = "Introduction to Clean Architecture",
            Content = "Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
            CreatedAt = DateTime.UtcNow,
            UpdatedAt = DateTime.UtcNow
        };
        dbContext.Posts.Add(newPost);
        dbContext.SaveChanges();
        // 检索所有帖子
        var posts = dbContext.Posts.ToList();
        foreach (var post in posts)
        {
            Console.WriteLine($"Title: {post.Title}, Content: {post.Content}");
        }
    }
}
```

在这段代码中：

1.  我们实例化了一个新的 `BlogDbContext` 对象。
2.  我们创建了一个新的 `Post` 实体，并将其添加到 `Posts` DbSet 中。
3.  我们调用 `SaveChanges` 将更改持久化到数据库。
4.  我们从数据库中检索所有帖子并显示它们的标题和内容。

定义数据模型并映射实体以进行持久化，对于构建健壮且可维护的软件应用程序至关重要。在使用 .NET 6 的 C# 10 中，这通常通过使用类来表示数据模型，并使用 Entity Framework Core 来映射实体以进行持久化来实现。遵循清洁架构原则，我们可以设计出模块化、可测试且易于维护的系统。

## 实现关注点分离的数据访问逻辑

实现关注点分离的数据访问逻辑是软件开发中的一项基本实践，尤其是在使用 C# 10 和 .NET 6 遵循清洁架构原则时。在本指南中，我们将探讨如何在保持关注点分离的同时实现数据访问逻辑。

### 关注点分离

关注点分离（SoC）是一种设计原则，它主张将软件系统划分为不同的部分，每个部分处理一个独立的关注点。这种分离增强了系统的可维护性、可扩展性和可测试性。在数据访问逻辑的上下文中，SoC 意味着将数据库操作与业务逻辑隔离开来。

### 仓库模式

仓库模式是实现数据访问逻辑同时遵循 SoC 原则的一种常见方法。它将数据访问代码从应用程序的其余部分中抽象出来，并提供一个清晰的接口来与底层数据存储进行交互。

让我们为我们的博客应用程序实现仓库模式：

```csharp
public interface IPostRepository
{
    Task<List<Post>> GetAllAsync();
    Task<Post> GetByIdAsync(int id);
    Task AddAsync(Post post);
    Task UpdateAsync(Post post);
    Task DeleteAsync(int id);
}

public class PostRepository : IPostRepository
{
    private readonly BlogDbContext _dbContext;
    public PostRepository(BlogDbContext dbContext)
    {
        _dbContext = dbContext;
    }
    public async Task<List<Post>> GetAllAsync()
    {
        return await _dbContext.Posts.ToListAsync();
    }
    public async Task<Post> GetByIdAsync(int id)
    {
        return await _dbContext.Posts.FindAsync(id);
    }
    public async Task AddAsync(Post post)
    {
        await _dbContext.Posts.AddAsync(post);
        await _dbContext.SaveChangesAsync();
    }
    public async Task UpdateAsync(Post post)
    {
        _dbContext.Posts.Update(post);
        await _dbContext.SaveChangesAsync();
    }
    public async Task DeleteAsync(int id)
    {
        var post = await _dbContext.Posts.FindAsync(id);
        if (post != null)
        {
            _dbContext.Posts.Remove(post);
            await _dbContext.SaveChangesAsync();
        }
    }
}
```

在这段代码中：

1.  我们定义了一个 `IPostRepository` 接口来指定与帖子交互的契约。
2.  我们实现了 `PostRepository` 类，该类实现了仓库接口。
3.  仓库类封装了数据库操作，例如获取所有帖子、通过 ID 获取帖子、添加新帖子、更新现有帖子和删除帖子。

### 依赖注入

为了在我们的应用程序中使用仓库，我们需要将其注册到 .NET Core 提供的依赖注入容器中：

```csharp
public class Startup
{
    public void ConfigureServices(IServiceCollection services)
    {
        services.AddDbContext<BlogDbContext>(options =>
            options.UseSqlServer("your_connection_string_here"));

        services.AddScoped<IPostRepository, PostRepository>();

        // 其他服务注册...
    }
}
```

通过将仓库注册为作用域服务，我们确保每个 HTTP 请求都能获得自己的仓库实例。

### 使用仓库

现在，让我们看看如何在应用程序中使用仓库：

```csharp
public class PostService
{
    private readonly IPostRepository _postRepository;

    public PostService(IPostRepository postRepository)
    {
        _postRepository = postRepository;
    }

    public async Task<List<Post>> GetAllPosts()
    {
        return await _postRepository.GetAllAsync();
    }

    public async Task<Post> GetPostById(int id)
    {
        return await _postRepository.GetByIdAsync(id);
    }

    public async Task CreatePost(Post post)
    {
        await _postRepository.AddAsync(post);
    }

    public async Task UpdatePost(Post post)
    {
        await _postRepository.UpdateAsync(post);
    }

    public async Task DeletePost(int id)
    {
        await _postRepository.DeleteAsync(id);
    }
}
```

在这段代码中：

1.  我们定义了一个 `PostService` 类，它封装了与帖子相关的业务逻辑。
2.  服务类依赖于 `IPostRepository` 接口，允许它通过仓库与数据库交互。
3.  服务类中的每个方法都对应于对帖子的特定操作，例如获取所有帖子、通过 ID 获取帖子、创建新帖子、更新现有帖子和删除帖子。

实现关注点分离的数据访问逻辑对于构建可维护和可扩展的软件应用程序至关重要。通过遵循仓库模式并利用依赖注入，我们可以将数据库操作与应用程序的其余部分隔离开来，并确保每个组件都有清晰且定义良好的职责。这种方法不仅改善了代码组织，还促进了单元测试和未来的增强。

## 对持久层进行单元测试以实现可靠的数据处理

对持久层进行单元测试对于确保软件中可靠的数据处理至关重要应用程序，尤其是在使用 C# 10 和 .NET 6 遵循整洁架构原则时。在本指南中，我们将探讨如何为持久层编写单元测试，以验证数据库操作是否按预期运行。

## 持久层单元测试的重要性

对持久层进行单元测试有助于确保：

1. 数据库操作，如插入、更新和删除数据，能够正确执行。
2. 数据访问代码能够优雅地处理边界情况和错误条件。
3. 数据库模式或 ORM 映射的更改不会破坏现有功能。
4. 业务逻辑能够按照预期方式与数据库交互。

## 测试策略

在测试持久层时，我们通常关注以下几个方面：

1.  **CRUD 操作：** 测试我们能否从数据库中创建、读取、更新和删除实体。
2.  **错误处理：** 验证错误条件（如数据库连接失败或约束冲突）是否得到妥善处理。
3.  **数据完整性：** 确保数据完整性约束（如外键关系或唯一约束）得到强制执行。
4.  **性能：** 测量数据库操作的性能，确保其满足应用程序的要求。

## 编写单元测试

让我们为之前实现的 `PostRepository` 类编写单元测试：

```csharp
public class PostRepositoryTests
{
    private BlogDbContext _dbContext;
    private IPostRepository _postRepository;

    [SetUp]
    public void Setup()
    {
        var options = new DbContextOptionsBuilder<BlogDbContext>()
            .UseInMemoryDatabase(databaseName: "TestDatabase")
            .Options;
        _dbContext = new BlogDbContext(options);
        _postRepository = new PostRepository(_dbContext);
    }

    [Test]
    public async Task AddPost_Should_Add_Post_To_Database()
    {
        // Arrange
        var post = new Post
        {
            Title = "Test Post",
            Content = "This is a test post.",
            CreatedAt = DateTime.UtcNow,
            UpdatedAt = DateTime.UtcNow
        };

        // Act
        await _postRepository.AddAsync(post);

        // Assert
        var result = await _dbContext.Posts.FirstOrDefaultAsync(p => p.Title == "Test Post");
        Assert.NotNull(result);
        Assert.AreEqual(post.Title, result.Title);
    }

    // 为其他 CRUD 操作和错误处理场景编写类似的测试
}
```

在此代码中：

1.  我们使用 NUnit 作为测试框架，但你可以使用任何你选择的测试框架。
2.  在 `Setup` 方法中，我们为每个测试初始化一个内存数据库上下文和仓储实例。
3.  我们编写了一个测试来验证向数据库添加帖子是否按预期工作。我们准备数据，通过调用仓储方法执行操作，然后断言结果。

## 模拟依赖项

在为持久层编写单元测试时，通常会模拟外部依赖项（如数据库上下文），以隔离被测代码。我们可以使用像 Moq 这样的模拟库来实现此目的：

```csharp
public class PostRepositoryTests
{
    private Mock<BlogDbContext> _dbContextMock;
    private IPostRepository _postRepository;

    [SetUp]
    public void Setup()
    {
        _dbContextMock = new Mock<BlogDbContext>();
        _postRepository = new PostRepository(_dbContextMock.Object);
    }

    [Test]
    public async Task AddPost_Should_Add_Post_To_Database()
    {
        // Arrange
        var post = new Post
        {
            Title = "Test Post",
            Content = "This is a test post.",
            CreatedAt = DateTime.UtcNow,
            UpdatedAt = DateTime.UtcNow
        };

        // Act
        await _postRepository.AddAsync(post);

        // Assert
        _dbContextMock.Verify(m => m.Posts.AddAsync(post, default), Times.Once);
        _dbContextMock.Verify(m => m.SaveChangesAsync(default), Times.Once);
    }

    // 为其他 CRUD 操作和错误处理场景编写类似的测试
}
```

在此代码中：

1.  我们使用 Moq 创建 `BlogDbContext` 的模拟实例。
2.  在测试方法中，我们准备数据，通过调用仓储方法执行操作，然后断言模拟对象上的相应方法被调用。

对持久层进行单元测试对于确保软件应用程序中可靠的数据处理至关重要。通过为 CRUD 操作、错误处理场景和数据完整性约束编写单元测试，我们可以验证数据库操作是否按预期运行，并优雅地处理边界情况。此外，通过使用模拟库来隔离依赖项，我们可以专注于测试代码逻辑，而无需依赖外部资源。总的来说，对持久层进行单元测试增强了应用程序的可靠性和可维护性。

# 第 9 章

## 使用 ASP.NET Core MVC 6 实现整洁架构

### ASP.NET Core MVC 6 作为整洁架构中的表示层

在使用 C# 10 和 .NET 6 的整洁架构方法中，将 ASP.NET Core MVC 6 实现为表示层是构建健壮且可维护的 Web 应用程序的强大组合。在本指南中，我们将探讨如何将 ASP.NET Core MVC 6 结构化并集成到整洁架构解决方案中。

## 整洁架构概述

整洁架构是一种软件设计模式，强调关注点分离以及框架和外部依赖项的独立性。它由多个层组成，包括：

1.  **表示层：** 处理用户交互并向用户显示信息。
2.  **应用层：** 包含特定于应用程序的业务逻辑，并协调表示层和领域层之间的交互。
3.  **领域层：** 包含核心业务逻辑和实体。
4.  **基础设施层：** 实现外部关注点，如数据库访问、外部服务和日志记录。

#### 集成 ASP.NET Core MVC 6

让我们从在整洁架构解决方案中设置 ASP.NET Core MVC 6 开始：

1.  创建一个新的 ASP.NET Core Web 应用程序项目：

```bash
dotnet new web -n MyApp.Web
```

2.  添加对领域层的引用：

```bash
dotnet add reference ../MyApp.Domain/MyApp.Domain.csproj
```

3.  添加对应用层的引用：

```bash
dotnet add reference ../MyApp.Application/MyApp.Application.csproj
```

## 构建表示层

在整洁架构解决方案中，表示层负责处理用户请求、呈现视图以及与应用层交互。让我们相应地构建表示层：

```
MyApp.Web/
|
├── Controllers/
│   └── HomeController.cs
|
├── Views/
│   └── Home/
│       └── Index.cshtml
|
└── Startup.cs
```

## 创建控制器

ASP.NET Core MVC 6 中的控制器处理传入的 HTTP 请求并执行相应的操作。让我们创建一个简单的 HomeController：

```csharp
using Microsoft.AspNetCore.Mvc;
using MyApp.Application;

namespace MyApp.Web.Controllers
{
    public class HomeController : Controller
    {
        private readonly IPostService _postService;

        public HomeController(IPostService postService)
        {
            _postService = postService;
        }

        public IActionResult Index()
        {
            var posts = _postService.GetAllPosts();
            return View(posts);
        }
    }
}
```

## 定义视图

ASP.NET Core MVC 6 中的视图负责向客户端呈现 HTML 标记。让我们创建一个简单的 Index 视图来显示帖子列表：

```html
<!-- Views/Home/Index.cshtml -->
@model List<MyApp.Domain.Post>
<h1>Posts</h1>
<ul>
    @foreach (var post in Model)
    {
        <li>@post.Title</li>
    }
</ul>
```

## 配置依赖注入

在 ASP.NET Core MVC 6 中，我们可以在 Startup 类中配置依赖注入。让我们注册来自应用层的服务：

```csharp
using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Hosting;
using Microsoft.Extensions.DependencyInjection;
using MyApp.Application;

namespace MyApp.Web
{
    public class Startup
    {
        public void ConfigureServices(IServiceCollection services)
        {
            services.AddControllersWithViews();
            // 注册应用服务
            services.AddScoped<IPostService, PostService>();
        }

        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            if (env.IsDevelopment())
            {
                app.UseDeveloperExceptionPage();
            }
            app.UseStaticFiles();
            app.UseRouting();
            app.UseEndpoints(endpoints =>
            {
                endpoints.MapControllerRoute(
                    name: "default",
                    pattern: "{controller=Home}/{action=Index}/{id?}");
            });
        }
    }
}
```

## 从 ASP.NET Core MVC 控制器中使用业务逻辑层

从 ASP.NET Core MVC 控制器中使用业务逻辑层，是构建遵循整洁架构原则、使用 C# 10 和 .NET 6 的健壮 Web 应用程序的关键方面。在本指南中，我们将探讨如何从 MVC 控制器中集成和使用包含业务逻辑的应用层。

## 整洁架构概述

整洁架构强调关注点分离和外部框架的独立性。它由多个层次组成，包括：

- 1. **表示层：** 处理用户交互并向用户显示信息。
- 2. **应用层：** 包含特定于应用程序的业务逻辑，并协调表示层与领域层之间的交互。
- 3. **领域层：** 包含核心业务逻辑和实体。
- 4. **基础设施层：** 实现外部关注点，如数据库访问、外部服务和日志记录。

## 集成业务逻辑层

让我们将包含业务逻辑的应用层集成到 ASP.NET Core MVC 项目中：

- 1. 在 ASP.NET Core MVC 项目中引用应用层项目：

```bash
dotnet add reference ../MyApp.Application/MyApp.Application.csproj
```

## 从控制器中使用业务逻辑

ASP.NET Core 中的 MVC 控制器负责处理传入的 HTTP 请求，并调用应用层中的相应方法。让我们创建一个控制器并使用业务逻辑：

```csharp
using Microsoft.AspNetCore.Mvc;
using MyApp.Application;

namespace MyApp.Web.Controllers
{
    public class PostController : Controller
    {
        private readonly IPostService _postService;

        public PostController(IPostService postService)
        {
            _postService = postService;
        }

        public IActionResult Index()
        {
            var posts = _postService.GetAllPosts();
            return View(posts);
        }

        public IActionResult Details(int id)
        {
            var post = _postService.GetPostById(id);
            if (post == null)
            {
                return NotFound();
            }

            return View(post);
        }

        // 其他用于 CRUD 操作的控制器操作
    }
}
```

在此代码中：

- 1. 我们使用依赖注入将 `IPostService` 接口的实例注入到控制器的构造函数中。
- 2. 在 `Index` 操作中，我们调用 `IPostService` 的 `GetAllPosts` 方法来检索所有文章，并将它们传递给视图。
- 3. 在 `Details` 操作中，我们调用 `IPostService` 的 `GetPostById` 方法通过 ID 检索特定文章，并将其传递给视图。

## 配置依赖注入

为确保 ASP.NET Core MVC 控制器能够从应用层解析依赖项，我们需要在 `Startup` 类中配置依赖注入：

```csharp
using Microsoft.Extensions.DependencyInjection;
using MyApp.Application;

namespace MyApp.Web
{
    public class Startup
    {
        public void ConfigureServices(IServiceCollection services)
        {
            services.AddControllersWithViews();

            // 注册应用服务
            services.AddScoped<IPostService, PostService>();
        }

        // 其他配置方法...
    }
}
```

在 `ConfigureServices` 方法中，我们将 `IPostService` 接口及其具体实现（`PostService`）注册为作用域服务。这允许 ASP.NET Core 为每个 HTTP 请求创建一个新的 `PostService` 实例，并根据需要将其注入到控制器中。

从 ASP.NET Core MVC 控制器中使用业务逻辑层对于构建可维护和可扩展的 Web 应用程序至关重要。通过使用依赖注入将应用层的依赖项注入到控制器中，我们确保了关注点分离，并促进了测试和维护。此外，通过遵循整洁架构原则，我们创建了一个清晰且结构化的架构，促进了代码重用、模块化和灵活性。总体而言，将业务逻辑层集成到 MVC 控制器中增强了应用程序的可靠性和可维护性。

## 在 ASP.NET Core MVC 应用程序中实现依赖注入

在 ASP.NET Core MVC 应用程序中实现依赖注入对于促进模块化、可测试性和可维护性至关重要。在本指南中，我们将探讨如何在基于整洁架构原则、使用 C# 10 和 .NET 6 的 ASP.NET Core MVC 应用程序中配置和使用依赖注入。

## 依赖注入概述

依赖注入是一种设计模式，其中依赖项从外部源提供给类，而不是在内部创建。在 ASP.NET Core MVC 中，依赖注入内置于框架中，允许我们注册服务并将其注入到控制器、视图和其他组件中。

## 设置依赖注入

让我们从在 ASP.NET Core MVC 应用程序中配置依赖注入开始：

- 1. 在 ASP.NET Core MVC 项目中打开 `Startup.cs` 文件。
- 2. 在 `ConfigureServices` 方法中，使用 `IServiceCollection` 注册服务：

```csharp
using Microsoft.Extensions.DependencyInjection;
using MyApp.Application;

namespace MyApp.Web
{
    public class Startup
    {
        public void ConfigureServices(IServiceCollection services)
        {
            services.AddControllersWithViews();

            // 注册应用服务
            services.AddScoped<IPostService, PostService>();
        }

        // 其他配置方法...
    }
}
```

在此代码中：

- 我们使用 `AddScoped` 方法将 `IPostService` 接口及其具体实现（`PostService`）注册为作用域服务。作用域服务每个请求创建一次，并在请求结束时被释放。

## 将依赖项注入到控制器中

一旦服务被注册，我们就可以使用构造函数注入将它们注入到控制器中。让我们将 `IPostService` 注入到一个控制器中：

```csharp
using Microsoft.AspNetCore.Mvc;
using MyApp.Application;

namespace MyApp.Web.Controllers
{
    public class PostController : Controller
    {
        private readonly IPostService _postService;

        public PostController(IPostService postService)
        {
            _postService = postService;
        }

        // 控制器操作...
    }
}
```

在此代码中：

- 1. 我们将 `IPostService` 接口的实例注入到控制器的构造函数中。
- 2. ASP.NET Core MVC 在创建 `PostController` 实例时会自动解析依赖项并提供 `PostService` 的实例。

## 在控制器操作中使用服务

一旦服务被注入到控制器中，我们就可以在控制器操作中使用它：

```csharp
public IActionResult Index()
{
    var posts = _postService.GetAllPosts();
    return View(posts);
}
```

在此代码中：

- 我们调用注入的 `IPostService` 的 `GetAllPosts` 方法来检索所有文章。

## 在视图中使用依赖注入

在 ASP.NET Core MVC 中，我们也可以使用 `@inject` 指令将服务直接注入到视图中。例如，要将 `IPostService` 注入到视图中，我们可以执行以下操作：

```html
@inject MyApp.Application.IPostService PostService
```

然后，我们可以在视图中使用 `@PostService` 来访问该服务。

在 ASP.NET Core MVC 应用程序中实现依赖注入对于构建可维护和可测试的代码库至关重要。通过在 `Startup` 类中注册服务并使用构造函数注入将它们注入到控制器中，我们促进了松散耦合并改善了应用程序的整体架构。此外，依赖注入使我们能够轻松地交换实现、为单元测试模拟依赖项以及遵循整洁架构原则。总体而言，将依赖注入融入 ASP.NET Core MVC 应用程序可提高代码质量、可扩展性和可维护性。

## 利用 Minimal APIs 构建简洁高效的控制器（.NET 6 中的新功能）

在 .NET 6 中利用 Minimal APIs 提供了一种简洁高效的方法来为 ASP.NET Core 应用程序构建控制器。此功能允许开发者以最少的仪式定义路由和处理请求，使其对于使用 C# 10 和 .NET 6 的整洁架构解决方案特别具有吸引力。在本指南中，我们将探讨如何利用 Minimal APIs 在整洁架构项目中创建控制器。

## Minimal APIs 概述

Minimal APIs 是在 .NET 6 中引入的，作为传统 MVC 控制器的轻量级替代方案。它们提供了一种简化的语法来定义路由和处理 HTTP 请求，而无需单独的控制器类。Minimal APIs 旨在简单、轻量且易于理解，使其成为中小型项目的理想选择。

## 设置 Minimal APIs

要在整洁架构项目中开始使用 Minimal APIs，请按照以下步骤操作：

- 1. 确保您的机器上安装了 .NET 6。
- 2. 使用 `web` 模板创建一个新的 ASP.NET Core 项目：
- 3. 添加对领域层和应用层的引用：

```bash
dotnet new web -n MyApp.Web
```

```bash
dotnet add reference ../MyApp.Domain/MyApp.Domain.csproj
```

## 运行应用程序

要运行应用程序，请在终端中使用以下命令：

```bash
dotnet run --project MyApp.Web
```

应用程序将开始在指定端口（默认为 5000）上监听，并对 `/posts` 请求以包含所有文章的 JSON 数组进行响应。

## 最小化 API 的优势

使用最小化 API 具有以下优势：

- **简洁性：** 最小化 API 语法极简，无需不必要的仪式感，即可轻松定义路由和处理请求。
- **性能：** 最小化 API 轻量高效，与传统的 MVC 控制器相比，启动时间更快，内存占用更少。
- **精炼性：** 借助最小化 API，你可以在单个文件中定义路由和处理请求，减少所需的样板代码量。
- **可测试性：** 最小化 API 可以轻松地使用单元测试进行测试，因为它们依赖于标准的 .NET Core 组件，如依赖注入和异步编程。

在 .NET 6 中利用最小化 API，为构建 ASP.NET Core 应用程序的控制器提供了一种简洁高效的方法。通过在单个文件中定义路由和处理请求，最小化 API 降低了复杂性并简化了开发流程。此外，最小化 API 轻量、高性能且易于测试，使其非常适合整洁架构项目。总的来说，采用最小化 API 可以提高开发人员的生产力，并增强 ASP.NET Core 应用程序的可维护性。

# 第 10 章

## 构建健壮整洁架构应用程序的测试策略

### 单元测试：独立验证业务逻辑

单元测试是软件开发的关键方面，尤其是在使用 C# 10 和 .NET 6 遵循整洁架构原则时。在整洁架构中，单元测试独立验证业务逻辑，确保每个组件在不依赖外部依赖项的情况下按预期运行。在本指南中，我们将探讨如何在整洁架构项目中编写单元测试来验证业务逻辑。

### 单元测试的优势

单元测试提供了多项优势：

- **早期缺陷检测：** 单元测试有助于在开发过程的早期识别缺陷和问题，降低后期修复成本。
- **回归测试：** 单元测试提供了一个安全网，确保在对代码库进行更改时，现有功能保持完好。
- **改进设计：** 编写测试通常会带来更好的代码设计，因为它鼓励关注点分离和模块化。
- **文档化：** 单元测试充当活文档，描述系统组件应如何行为。

### 为业务逻辑编写单元测试

让我们编写单元测试来验证整洁架构项目中的业务逻辑。我们将重点测试 `PostService` 类，该类包含与文章相关的特定于应用程序的业务逻辑。

```csharp
using System.Collections.Generic;
using System.Threading.Tasks;
using Moq;
using Xunit;
using MyApp.Application;
using MyApp.Domain;
public class PostServiceTests
{
    [Fact]
    public async Task GetAllPosts_Should_Return_All_Posts()
    {
        // Arrange
        var mockPostRepository = new Mock<IPostRepository>();
        var posts = new List<Post>
        {
            new Post { Id = 1, Title = "Post 1", Content = "Content 1" },
            new Post { Id = 2, Title = "Post 2", Content = "Content 2" },
        };
        mockPostRepository.Setup(repo => repo.GetAllAsync()).ReturnsAsync(posts);
        var postService = new PostService(mockPostRepository.Object);
        // Act
        var result = await postService.GetAllPosts();
        // Assert
        Assert.Equal(posts, result);
    }
    // 为 PostService 类中的其他方法编写类似的测试
}
```

在此测试中：

- 我们使用 XUnit 测试框架定义了一个测试方法 (`GetAllPosts_Should_Return_All_Posts`)。
- 我们使用 Moq 库创建了 `IPostRepository` 接口的模拟实现。这允许我们在测试期间控制存储库的行为。
- 我们设置模拟存储库，使其在调用 `GetAllAsync` 方法时返回文章列表。
- 我们使用模拟存储库实例化了 `PostService` 类的一个实例。
- 我们调用 `PostService` 的 `GetAllPosts` 方法，并断言返回的结果与预期的文章列表匹配。

### 运行单元测试

要在 .NET 项目中运行单元测试，请在终端中使用以下命令：

```bash
dotnet test
```

此命令将发现并执行项目中的所有单元测试，并在终端中显示结果。

### 独立测试的优势

通过独立测试业务逻辑，我们获得了多项优势：

- **快速执行：** 独立测试通常执行得更快，因为它们不依赖于数据库或 Web 服务器等外部依赖项。
- **减少不稳定性：** 独立测试因外部因素而失败的可能性较小，使其更可靠且结果更确定。
- **更易于调试：** 独立测试使识别故障原因更容易，因为它们专注于系统的特定组件。
- **提高测试覆盖率：** 独立测试使我们能够通过全面测试各个组件来实现更高的测试覆盖率。

单元测试是软件开发中的一项基本实践，尤其是在遵循整洁架构原则时。通过编写单元测试来独立验证业务逻辑，我们确保每个组件在不依赖外部依赖项的情况下按预期运行。这种方法提高了代码质量，减少了缺陷，并增强了可维护性，使其成为开发过程中不可或缺的一部分。

### 集成测试：测试层间交互

集成测试对于验证软件应用程序中层与层之间的交互至关重要，尤其是在使用 C# 10 和 .NET 6 遵循整洁架构原则时。集成测试确保组件协同工作并按预期通信，从而对整个系统的行为充满信心。在本指南中，我们将探讨如何编写集成测试来验证整洁架构项目中层与层之间的交互。

### 集成测试概述

集成测试涉及测试应用程序不同组件或层之间的交互。在整洁架构项目中，集成测试侧重于验证层与层之间的集成点（例如应用层和基础设施层）是否正常工作。这确保了当所有组件组合在一起时，系统按预期运行。

### 设置集成测试

要在整洁架构项目中开始集成测试，请按照以下步骤操作：

- 为集成测试创建一个新的测试项目：
- 添加对领域层、应用层和基础设施层的引用：

```bash
dotnet new xunit -n MyApp.IntegrationTests
```

## 编写集成测试

让我们编写一个集成测试，以验证用于获取所有文章（`/posts`）的 API 端点是否返回文章列表：

```csharp
using System.Net.Http;
using System.Text.Json;
using System.Threading.Tasks;
using Xunit;

public class PostControllerIntegrationTests : IntegrationTestBase
{
    [Fact]
    public async Task GetAllPosts_Should_Return_All_Posts()
    {
        // Arrange
        var client = _server.CreateClient();

        // Act
        var response = await client.GetAsync("/posts");
        response.EnsureSuccessStatusCode();
        var responseContent = await response.Content.ReadAsStringAsync();
        var posts = JsonSerializer.Deserialize<List<Post>>(responseContent);

        // Assert
        Assert.NotNull(posts);
        Assert.NotEmpty(posts);
    }
}
```

在此测试中：

1.  我们使用 `TestServer` 实例创建 `HttpClient` 类的一个实例。
2.  我们向 `/posts` 端点发送一个 GET 请求。
3.  我们确保响应状态码表示成功（2xx）。
4.  我们使用 JSON 序列化将响应内容反序列化为文章列表。
5.  我们断言文章列表不为 null 且不为空。

## 运行集成测试

要运行集成测试，请在终端中使用以下命令：

```bash
dotnet test
```

此命令将发现并执行项目中的所有集成测试，并在终端中显示结果。

## 集成测试的好处

集成测试提供了几个好处：

1.  **端到端验证：** 集成测试验证整个系统，包括不同组件和层之间的交互。
2.  **真实场景：** 集成测试通过与系统的外部接口（如 API 或数据库）交互来模拟真实场景。
3.  **检测集成问题：** 集成测试有助于识别与组件间集成点相关的问题，例如不正确的数据映射或通信错误。
4.  **部署信心：** 成功的集成测试提供了系统运行正常且可以安全部署到生产环境的信心。

集成测试对于验证整洁架构项目中各层之间的交互至关重要。通过编写集成测试，我们可以确保组件协同工作并按预期通信，从而对整个系统的行为提供信心。集成测试通过验证不同组件之间的集成点来补充单元测试，有助于在开发过程的早期识别和解决问题。总体而言，集成测试是构建可靠且可维护的软件应用程序的重要组成部分。

## 利用测试框架（xUnit、NUnit）与 C# 10 特性

利用 xUnit 和 NUnit 等测试框架与 C# 10 特性，可以增强基于 .NET 6 构建的整洁架构项目中单元测试的开发和维护。这些框架提供了高效编写和执行测试的强大功能，而 C# 10 引入的新语言特性进一步提高了测试代码的可读性和表达能力。在本指南中，我们将探讨如何在整洁架构项目中结合 C# 10 特性使用 xUnit 和 NUnit。

## 测试框架概述

xUnit 和 NUnit 是用于在 .NET 项目中编写和执行单元测试的流行测试框架。这两个框架都支持广泛的功能，包括测试夹具、断言、参数化测试和测试运行器。

## 设置测试框架

要在整洁架构项目中开始使用 xUnit 或 NUnit，请按照以下步骤操作：

1.  使用 NuGet 安装所需的测试框架包：

对于 xUnit：
```bash
dotnet add package xunit
dotnet add package xunit.runner.visualstudio
dotnet add package xunit.analyzers
```

对于 NUnit：
```bash
dotnet add package nunit
dotnet add package nunit3testadapter
```

2.  在解决方案中创建一个新的测试项目：
```bash
dotnet new xunit -n MyApp.Tests
```
或
```bash
dotnet new nunit -n MyApp.Tests
```

3.  添加对领域层和应用层的引用：
```bash
dotnet add reference ../MyApp.Domain/MyApp.Domain.csproj
dotnet add reference ../MyApp.Application/MyApp.Application.csproj
```

## 使用 C# 10 特性编写测试

C# 10 引入了几种新的语言特性，可用于编写更具表达力和简洁性的单元测试。让我们通过示例来探讨其中一些特性。

### 目标类型化的 `new` 表达式

目标类型化的 `new` 表达式通过根据上下文推断类型来简化对象创建。这减少了冗余并使代码更具可读性。

```csharp
// C# 9 及更早版本
List<int> numbers = new();

// C# 10
var numbers = new List<int>();
```

### 文件范围命名空间

文件范围命名空间允许我们直接在文件内定义命名空间，无需使用封闭命名空间。这减少了冗长性并改进了代码组织。

```csharp
// C# 9 及更早版本
namespace MyApp.Tests
{
    public class MyTestClass
    {
        // 测试方法...
    }
}

// C# 10
namespace MyApp.Tests;

public class MyTestClass
{
    // 测试方法...
}
```

### 全局 using

全局 using 通过允许我们在文件顶部指定常用的命名空间来简化导入命名空间的过程。这减少了杂乱并提高了可读性。

```csharp
// C# 9 及更早版本
using System;
using Xunit;

// C# 10
global using System;
global using Xunit;
```

## 使用 xUnit 编写测试

让我们使用 xUnit 结合 C# 10 特性编写一个示例单元测试：

```csharp
global using Xunit;

using MyApp.Application;

public class PostServiceTests
{
    [Fact]
    public void GetAllPosts_Should_Return_All_Posts()
    {
        // Arrange
        var postService = new PostService();

        // Act
        var posts = postService.GetAllPosts();

        // Assert
        Assert.NotEmpty(posts);
    }
}
```

## 使用 NUnit 编写测试

类似地，让我们使用 NUnit 结合 C# 10 特性编写一个示例单元测试：

```csharp
global using NUnit.Framework;
using MyApp.Application;

public class PostServiceTests
{
    [Test]
    public void GetAllPosts_Should_Return_All_Posts()
    {
        // Arrange
        var postService = new PostService();

        // Act
        var posts = postService.GetAllPosts();

        // Assert
        Assert.IsNotEmpty(posts);
    }
}
```

## 运行测试

要使用 xUnit 或 NUnit 运行测试，请在终端中使用以下命令：

对于 xUnit：
```bash
dotnet test --project MyApp.Tests
```

对于 NUnit：
```bash
dotnet test --project MyApp.Tests --logger:trx
```

利用 xUnit 和 NUnit 等测试框架与 C# 10 特性，可以增强整洁架构项目中单元测试的开发和维护。这些框架提供了高效编写和执行测试的强大功能，而 C# 10 特性（如目标类型化的 `new` 表达式、文件范围命名空间和全局 using）提高了测试代码的可读性和表达能力。通过结合这些工具和特性，开发人员可以编写高质量的单元测试，有效地验证其应用程序的行为。

## 针对 .NET 6 整洁架构项目的测试注意事项

测试注意事项对于确保基于 .NET 6 构建的整洁架构项目的可靠性、可维护性和可扩展性至关重要。整洁架构提倡关注点分离和组件独立性，这影响了测试策略以覆盖应用程序的各个层。在本指南中，我们将探讨针对 .NET 6 整洁架构项目的测试注意事项，涵盖单元测试、集成测试和端到端测试。

## 单元测试

单元测试是整洁架构项目中的基本实践，专注于在隔离环境中测试单个代码单元。在整洁架构中，单元测试通常覆盖领域层和应用层中的组件，例如实体、用例和服务类。

### 单元测试示例：

让我们为应用层中的一个简单用例编写一个单元测试：

```csharp
using Xunit;
```

## 集成测试

集成测试验证应用程序各组件或层之间的交互，确保它们协同工作。在整洁架构项目中，集成测试通常涵盖应用层与基础设施层之间的交互，例如数据库访问、外部服务和 API。

### 集成测试示例：

让我们编写一个集成测试来验证基础设施层中的数据库访问：

```csharp
using System.Threading.Tasks;
using Xunit;
using MyApp.Infrastructure.Persistence;
public class PostRepositoryTests
{
    [Fact]
    public async Task GetAllPosts_Should_Return_All_Posts_From_Database()
    {
        // Arrange
        var dbContext = DbContextHelper.CreateDbContext();
        var postRepository = new PostRepository(dbContext);

        // Act
        var posts = await postRepository.GetAllAsync();

        // Assert
        Assert.NotEmpty(posts);
    }
}
```

## 端到端测试

端到端测试验证整个系统的行为，包括所有层之间的交互和外部依赖。在整洁架构项目中，端到端测试通常涵盖面向用户的功能和场景，确保应用程序从用户视角按预期运行。

### 端到端测试示例：

让我们编写一个端到端测试，使用 Selenium 验证 Web 应用程序的用户场景：

```csharp
using OpenQA.Selenium;
using OpenQA.Selenium.Chrome;
using Xunit;

public class PostPageTests : IClassFixture<ChromeDriverFixture>
{
    private readonly ChromeDriverFixture _fixture;

    public PostPageTests(ChromeDriverFixture fixture)
    {
        _fixture = fixture;
    }

    [Fact]
    public void User_Can_View_All_Posts()
    {
        // Arrange
        var driver = _fixture.Driver;
        driver.Navigate().GoToUrl("http://localhost:5000/posts");

        // Act
        var posts = driver.FindElementsByCssSelector(".post");

        // Assert
        Assert.NotEmpty(posts);
    }
}
```

## 测试注意事项

在使用 .NET 6 测试整洁架构项目时，请考虑以下几点：

- 1. **依赖注入：** 利用依赖注入在单元测试中模拟外部依赖，并为集成和端到端测试配置测试环境。
- 2. **关注点分离：** 确保测试专注于特定组件或层，避免职责重叠并保持清晰性。
- 3. **覆盖率：** 旨在实现应用程序所有层的全面测试覆盖，包括领域逻辑、应用服务、基础设施和用户界面。
- 4. **性能：** 通过并行运行测试、最小化对外部资源的依赖以及在集成测试中使用内存数据库来优化测试执行时间。
- 5. **健壮性：** 设计测试使其健壮且能适应代码库的变化，可使用参数化测试、测试数据构建器和测试夹具等技术。

测试注意事项对于确保使用 .NET 6 的整洁架构项目的可靠性、可维护性和可扩展性至关重要。通过实施单元测试、集成测试和端到端测试策略，开发人员可以验证各个组件的行为、层之间的交互以及整体系统功能。采用全面的测试方法并遵循整洁架构原则，整洁架构项目可以交付满足业务需求和用户期望的高质量软件。

## 第 11 章

## 依赖倒置原则实现松耦合与灵活性

依赖倒置原则是构建在 .NET 6 上的整洁架构项目中的一个关键设计原则。它通过将高层模块与低层实现解耦，促进组件间的松耦合并增强灵活性。在本指南中，我们将探讨如何在使用 .NET 6 的 C# 10 整洁架构项目中应用依赖倒置原则，并通过代码示例说明其优势。

### 理解依赖倒置原则

依赖倒置原则指出，高层模块不应依赖于低层模块，而应依赖于抽象。该原则提倡使用接口或抽象类来定义组件之间的契约，允许实现独立变化。

### 在整洁架构中应用依赖倒置

在整洁架构项目中，应用依赖倒置原则是为了确保高层模块（如用例或应用服务）依赖于抽象（接口）而非具体实现（如数据访问或外部服务）。

### 示例场景

让我们考虑一个应用服务依赖于仓库进行数据访问的场景。如果不应用依赖倒置原则，应用服务将直接依赖于具体的仓库实现，导致紧耦合和灵活性降低。

### 未应用依赖倒置：

```csharp
namespace MyApp.Application
{
    public class PostService
    {
        private readonly PostRepository _postRepository;

        public PostService()
        {
            _postRepository = new PostRepository(); // 直接依赖于具体实现
        }
    }
}
```

### 实现依赖倒置

为了应用依赖倒置原则，我们引入一个接口来表示应用服务与仓库之间的契约。这个接口作为抽象，将服务与具体的仓库实现解耦。

### 应用依赖倒置：

```csharp
namespace MyApp.Application
{
    public interface IPostRepository
    {
        Task<List<Post>> GetAllPostsAsync();
        Task<Post> GetPostByIdAsync(int id);
        Task AddPostAsync(Post post);
        Task UpdatePostAsync(Post post);
        Task DeletePostAsync(int id);
    }
}
```

```csharp
namespace MyApp.Application
{
    public class PostService
    {
        private readonly IPostRepository _postRepository;

        public PostService(IPostRepository postRepository)
        {
            _postRepository = postRepository; // 通过构造函数注入实现依赖倒置
        }

        // 服务方法...
    }
}
```

### 依赖倒置的优势

在整洁架构项目中应用依赖倒置原则具有以下优势：

- 1. **松耦合：** 通过依赖抽象而非具体实现，组件变得松耦合，使得修改、替换或扩展单个模块而不影响其他模块变得更容易。
- 2. **灵活性：** 使用接口或抽象类允许可互换的实现，便于采用替代的数据访问策略、外部服务或第三方库。
- 3. **可测试性：** 依赖倒置通过在单元测试中用模拟或存根对象替代真实实现来增强可测试性，确保组件可以被隔离测试。
- 4. **可扩展性：** 具有依赖倒置的整洁架构项目本质上是可扩展的，因为它们允许添加新功能、模块或依赖项，而不会引入紧耦合或破坏现有功能。

依赖倒置原则是使用 .NET 6 的整洁架构项目中的一个基本设计原则。通过应用此原则，开发人员可以实现组件间的松耦合、增强灵活性、提高可测试性并确保可扩展性。通过依赖抽象而非具体实现，整洁架构项目可以适应不断变化的需求、与外部系统集成，并随时间演进，同时保持模块化和可维护的代码库。总体而言，依赖倒置原则是整洁架构设计的基石，能够创建健壮且灵活的软件系统。

## 用于数据访问抽象的仓库模式

仓储模式是一种设计模式，常用于基于 .NET 6 的整洁架构项目中，旨在抽象数据访问逻辑，并为与不同数据源交互提供统一接口。它促进了关注点分离，并提升了数据访问层的可测试性、可维护性和灵活性。在本指南中，我们将探讨如何在使用 C# 10 和 .NET 6 的整洁架构项目中实现仓储模式，并通过代码示例说明其用法和优势。

## 仓储模式概述

仓储模式在应用层和数据访问层之间定义了一个抽象层，允许应用通过一致的接口与数据对象交互。它通常由定义 CRUD（创建、读取、更新、删除）操作的接口以及与底层数据存储机制交互的具体实现组成。

## 实现仓储模式

让我们在一个整洁架构项目中实现仓储模式，以抽象管理文章的数据访问逻辑：

### 定义仓储接口：

```csharp
using System.Collections.Generic;
using System.Threading.Tasks;
using MyApp.Domain.Entities;

namespace MyApp.Application.Interfaces
{
    public interface IPostRepository
    {
        Task<List<Post>> GetAllAsync();
        Task<Post> GetByIdAsync(int id);
        Task AddAsync(Post post);
        Task UpdateAsync(Post post);
        Task DeleteAsync(int id);
    }
}
```

### 实现仓储：

```csharp
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;
using MyApp.Application.Interfaces;
using MyApp.Domain.Entities;
namespace MyApp.Infrastructure.Persistence
{
    public class PostRepository : IPostRepository
    {
        private readonly AppDbContext _context;
        public PostRepository(AppDbContext context)
        {
            _context = context;
        }
        public async Task<List<Post>> GetAllAsync()
        {
            return await _context.Posts.ToListAsync();
        }
        public async Task<Post> GetByIdAsync(int id)
        {
            return await _context.Posts.FindAsync(id);
        }
        public async Task AddAsync(Post post)
        {
            await _context.Posts.AddAsync(post);
            await _context.SaveChangesAsync();
        }
        public async Task UpdateAsync(Post post)
        {
            _context.Posts.Update(post);
            await _context.SaveChangesAsync();
        }
        public async Task DeleteAsync(int id)
        {
            var post = await _context.Posts.FindAsync(id);
            if (post != null)
            {
                _context.Posts.Remove(post);
                await _context.SaveChangesAsync();
            }
        }
    }
}
```

## 仓储模式的优势

仓储模式在整洁架构项目中提供了多项优势：

- 1. **抽象化：** 仓储接口清晰地抽象了数据访问操作，向应用层隐藏了底层数据存储机制的细节。
- 2. **解耦：** 通过依赖仓储接口而非具体实现，应用层与特定的数据访问技术解耦，从而更容易切换或替换数据源。
- 3. **可测试性：** 仓储模式通过在单元测试中使用模拟仓储来增强可测试性，便于在不依赖外部依赖的情况下隔离测试应用逻辑。
- 4. **灵活性：** 仓储模式允许实现不同的数据访问策略，例如使用 Entity Framework Core 访问关系数据库或使用 HttpClient 访问外部 API，而不会影响应用层。

## 在应用层中使用仓储模式

既然我们已经定义并实现了仓储，让我们在应用层中使用它来与文章交互：

```csharp
using System.Collections.Generic;
using System.Threading.Tasks;
using MyApp.Application.Interfaces;
using MyApp.Domain.Entities;

namespace MyApp.Application.Services
{
    public class PostService
    {
        private readonly IPostRepository _postRepository;

        public PostService(IPostRepository postRepository)
        {
            _postRepository = postRepository;
        }

        public async Task<List<Post>> GetAllPostsAsync()
        {
            return await _postRepository.GetAllAsync();
        }

        public async Task<Post> GetPostByIdAsync(int id)
        {
            return await _postRepository.GetByIdAsync(id);
        }
    }
}
```

在此示例中，`PostService` 依赖于 `IPostRepository` 接口，使其能够与文章交互，而无需了解数据访问实现的具体细节。

仓储模式是基于 .NET 6 的整洁架构项目中一种有价值的设计模式，为数据访问操作提供了清晰的抽象层。通过定义仓储接口并实现具体的仓储，开发者可以在数据访问层实现关注点分离、解耦、可测试性和灵活性。整合仓储模式有助于开发健壮、可维护和可扩展的软件应用程序，确保数据访问逻辑在应用程序的不同层之间保持有序和可管理。总体而言，仓储模式是构建基于 .NET 6 的整洁架构项目的基础工具。

## 使用 C# 10 和 .NET 6 为微服务实现整洁架构

使用 C# 10 和 .NET 6 为微服务实现整洁架构，提供了一种构建可扩展、可维护和松耦合系统的结构化方法。整洁架构强调关注点分离、依赖倒置和抽象层，使其非常适合微服务架构。在本指南中，我们将探讨如何使用 C# 10 和 .NET 6 为微服务实现整洁架构，包括代码示例以说明关键概念。

## 微服务整洁架构概述

整洁架构将系统划分为多个层，每层具有不同的职责和依赖关系。整洁架构的核心原则包括：

- 1. **框架独立性：** 核心业务逻辑独立于任何外部框架，允许为每个微服务灵活选择技术栈。
- 2. **可测试性：** 该架构通过确保业务逻辑可以轻松地与外部依赖隔离测试来促进可测试性。
- 3. **UI 独立性：** UI 与业务逻辑解耦，允许使用各种 UI 框架或技术而不影响核心功能。
- 4. **数据库独立性：** 数据库技术的选择从业务逻辑中抽象出来，允许无缝切换或扩展数据库实现。

## 为微服务实现整洁架构

让我们创建一个遵循整洁架构原则的微服务架构简单示例。

### 目录结构：

```
MyApp.Core/
    - 包含领域实体和业务逻辑
MyApp.Infrastructure/
    - 包含数据访问逻辑和外部依赖
MyApp.Services/
    - 包含应用服务和用例
MyApp.Api/
    - 包含微服务的 API 端点
```

### 核心层：

核心层包含领域实体和业务逻辑，代表应用程序的核心。这些实体独立于任何外部框架或技术。

```csharp
namespace MyApp.Core.Entities
{
    public class Product
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public decimal Price { get; set; }
    }
}
```

### 基础设施层：

基础设施层包含数据访问逻辑和外部依赖的实现，例如数据库访问、外部 API 或消息传递系统。

```csharp
namespace MyApp.Infrastructure.Persistence
{
    public class ProductRepository : IProductRepository
    {
        private readonly AppDbContext _context;
        public ProductRepository(AppDbContext context)
        {
            _context = context;
        }
        public async Task<List<Product>> GetAllAsync()
        {
            return await _context.Products.ToListAsync();
        }
        // 其他数据访问方法...
    }
}
```

### 服务层：

服务层包含应用服务和用例，它们协调核心领域实体与基础设施层之间的交互。

```csharp
namespace MyApp.Services
{
    public class ProductService : IProductService
    {
```

## API 层：

API 层包含微服务的 API 端点，这些端点通过 RESTful API 或其他通信协议向外部客户端暴露功能。

```csharp
namespace MyApp.Api.Controllers
{
    [ApiController]
    [Route("api/products")]
    public class ProductController : ControllerBase
    {
        private readonly IProductService _productService;
        public ProductController(IProductService productService)
        {
            _productService = productService;
        }

        [HttpGet]
        public async Task<ActionResult<List<Product>>> GetAllProducts()
        {
            var products = await _productService.GetAllProductsAsync();

            return Ok(products);
        }

        // 其他 API 端点...
    }
}
```

## 清洁架构对微服务的好处

为微服务实施清洁架构有几个好处：

- 1. **可扩展性：** 该架构允许微服务独立扩展，支持水平扩展以适应不断增长的工作负载。
- 2. **灵活性：** 清洁架构促进了技术选择的灵活性，允许每个微服务使用最合适的框架、语言或数据库技术。
- 3. **可维护性：** 关注点分离和层之间的清晰边界使系统更容易维护和随时间演进，因为一层的变化不会影响其他层。
- 4. **可测试性：** 清洁架构通过确保业务逻辑可以轻松地与外部依赖隔离测试来增强可测试性，从而促进自动化测试实践的采用。

使用 C# 10 和 .NET 6 为微服务实施清洁架构，为构建可扩展、可维护和松耦合的系统提供了一种结构化方法。遵循清洁架构的核心原则，开发人员可以创建独立于框架、可测试且技术选择灵活的微服务。通过清晰的关注点分离和层之间定义良好的边界，清洁架构有助于开发健壮且可扩展的微服务，以满足现代软件系统的需求。

# 第 12 章

## 清洁架构的最佳实践和设计模式

### 通过代码审查和指南强制执行清洁架构原则

通过代码审查和指南强制执行清洁架构原则对于在使用 .NET 6 的 C# 10 项目中保持一致性、遵守最佳实践以及代码库的整体质量至关重要。通过建立明确的指南并进行彻底的代码审查，开发团队可以确保架构保持健壮、可维护和可扩展。在本指南中，我们将探讨如何通过代码审查和指南强制执行清洁架构原则，并结合代码示例来说明最佳实践。

### 建立清洁架构指南

在通过代码审查强制执行清洁架构原则之前，有必要建立明确的指南，定义架构中每一层的结构、职责和依赖关系。这些指南应涵盖以下方面：

- 1. **层分离：** 明确定义核心域层、应用层、基础设施层和表示层之间的边界。
- 2. **依赖倒置：** 鼓励使用抽象和接口来解耦高级模块和低级实现，促进依赖倒置。
- 3. **单一职责原则 (SRP)：** 确保每个组件、类或方法只有一个职责，专注于系统功能的特定方面。
- 4. **可测试性：** 通过设计组件以促进单元测试、集成测试和端到端测试的方式来促进编写可测试的代码。

### 进行代码审查

代码审查在强制执行清洁架构原则方面发挥着至关重要的作用，它为团队成员提供了根据既定指南和最佳实践审查代码更改的机会。在代码审查期间，开发人员可以评估代码是否符合清洁架构原则，并在必要时提出改进建议或纠正措施。代码审查期间需要关注的关键方面包括：

- 1. **层依赖关系：** 验证层之间的依赖关系是否得到妥善管理，高级模块依赖于抽象而非具体实现。
- 2. **关注点分离：** 确保每一层都有清晰且独特的职责，业务逻辑封装在核心域层中，基础设施关注点单独处理。
- 3. **抽象使用：** 检查是否适当地使用了接口和抽象来解耦组件并促进依赖倒置，从而实现灵活性和可测试性。
- 4. **测试覆盖率：** 审查代码更改的测试覆盖率，确保关键路径得到充分测试，并在必要时包含单元测试、集成测试和端到端测试。

### 代码审查清单

以下是代码审查期间需要考虑的项目清单，以强制执行清洁架构原则：

- 1. 层之间的依赖关系是否得到妥善管理？
- 2. 业务逻辑是否封装在核心域层中？
- 3. 是否使用了抽象和接口来促进依赖倒置？
- 4. 代码是否模块化并遵守单一职责原则？
- 5. 测试覆盖率是否足够，包括单元测试、集成测试和端到端测试？
- 6. 命名约定是否一致且有意义？
- 7. 是否有效使用代码注释来解释复杂逻辑或设计决策？
- 8. 是否遵循了 SOLID 原则，包括 SRP、开闭原则、里氏替换原则、接口隔离原则和依赖倒置原则？

### 代码审查示例

让我们对一个清洁架构项目中的功能实现进行示例代码审查：

```csharp
// 应用层

public class ProductService : IProductService
{
    private readonly IProductRepository _productRepository;

    public ProductService(IProductRepository productRepository)
    {
        _productRepository = productRepository;
    }

    public async Task<List<Product>> GetAllProductsAsync()
    {
        return await _productRepository.GetAllAsync();
    }
}
```

在这次代码审查中：

- **依赖倒置**：`ProductService` 依赖于 `IProductRepository` 接口，遵守了依赖倒置原则。
- **关注点分离**：服务类负责协调与存储库的交互，保持了清晰的关注点分离。
- **可测试性**：代码设计为易于测试，依赖通过构造函数注入，便于单元测试。

通过代码审查和指南强制执行清洁架构原则对于在使用 .NET 6 的 C# 10 项目中保持一致性、质量和可维护性至关重要。通过建立明确的指南、进行彻底的代码审查并提供建设性反馈，开发团队可以确保架构保持健壮、可扩展并遵守最佳实践。通过持续应用清洁架构原则，团队可以构建灵活、可测试和可维护的软件系统，使其能够适应不断变化的需求和技术发展。

## 清洁架构的设计模式：适配器、外观等

设计模式在清洁架构项目中发挥着至关重要的作用，为常见的架构挑战提供解决方案，并促进模块化、灵活性和可维护性。在本指南中，我们将探讨在使用 C# 10 和 .NET 6 的清洁架构项目中常用的一些设计模式，包括适配器、外观等。我们将提供代码示例来说明这些模式在清洁架构上下文中的实现。

### 适配器模式

适配器模式通过提供一个桥梁来使不兼容的接口协同工作。在清洁架构中，适配器模式通常用于将外部系统或库与应用程序的核心逻辑集成。

### 示例：

假设我们有一个具有不兼容接口的外部支付网关库。我们可以创建一个适配器来在外部库的接口和我们的内部接口之间进行转换：

```csharp
// 外部支付网关库
public interface IPaymentGateway
```

## 外观模式

外观模式为复杂子系统提供了一个简化的接口，使其更易于使用和理解。在整洁架构中，外观模式常用于封装与多个组件或服务的交互。

### 示例：

假设我们有一个由多个服务组成的复杂订单处理子系统。我们可以创建一个外观来简化与该子系统的交互：

```csharp
// 外观类
public class OrderProcessingFacade
{
    private readonly IOrderService _orderService;
    private readonly IPaymentService _paymentService;
    private readonly IEmailService _emailService;

    public OrderProcessingFacade(IOrderService orderService, IPaymentService paymentService, IEmailService emailService)
    {
        _orderService = orderService;
        _paymentService = paymentService;
        _emailService = emailService;
    }

    public void ProcessOrder(Order order)
    {
        _orderService.CreateOrder(order);
        _paymentService.MakePayment(order.TotalAmount);
        _emailService.SendOrderConfirmationEmail(order);
    }
}
```

## 工厂模式

工厂模式提供了一个创建对象的接口，而无需指定其具体类，从而实现了灵活性和解耦。在整洁架构中，工厂模式常用于创建领域实体或服务的实例。

### 示例：

假设我们有一个用于在电子商务应用中创建产品实例的工厂：

```csharp
// 产品工厂接口
public interface IProductFactory
{
    Product CreateProduct(string name, decimal price);
}

// 具体产品工厂
public class ProductFactory : IProductFactory
{
    public Product CreateProduct(string name, decimal price)
    {
        return new Product { Name = name, Price = price };
    }
}
```

## 观察者模式

观察者模式定义了对象之间的一对多依赖关系，使得多个观察者可以被通知主体的变化。在整洁架构中，观察者模式常用于实现组件或层之间的事件驱动通信。

### 示例：

假设我们有一个通知服务，当新订单下达时通知订阅者：

```csharp
// 主体接口
public interface IOrderSubject
{
    void Attach(IOrderObserver observer);
    void Detach(IOrderObserver observer);
    void Notify(Order order);
}

// 具体主体
public class OrderSubject : IOrderSubject
{
    private List<IOrderObserver> _observers = new List<IOrderObserver>();
    public void Attach(IOrderObserver observer)
    {
        _observers.Add(observer);
    }

    public void Detach(IOrderObserver observer)
    {
        _observers.Remove(observer);
    }

    public void Notify(Order order)
    {
        foreach (var observer in _observers)
        {
            observer.Update(order);
        }
    }
}
```

诸如适配器、外观、工厂和观察者等设计模式在使用 C# 10 和 .NET 6 的整洁架构项目中扮演着至关重要的角色。通过理解和应用这些模式，开发者可以在其代码库中实现模块化、灵活性和可维护性。无论是与外部系统集成、简化复杂子系统、创建灵活的对象实例化机制，还是实现事件驱动通信，设计模式都为常见的架构挑战提供了经过验证的解决方案。通过将这些模式融入整洁架构项目，开发者可以构建出健壮、可扩展且适应性强的软件系统，以满足用户和利益相关者不断变化的需求。

## 在使用 C# 10 和 .NET 6 的项目演进中维护整洁架构

在使用 C# 10 和 .NET 6 的项目演进中维护整洁架构，对于确保可扩展性、灵活性和可维护性至关重要。随着需求的变化、新功能的添加以及技术的演进，持续地调整和重构架构以保持其整洁和高效至关重要。在本指南中，我们将探讨在项目演进过程中维护整洁架构的策略，并提供代码示例以说明最佳实践。

## 持续重构

持续重构是维护整洁架构的一项基本实践。重构涉及在不改变其外部行为的情况下，重组代码以改善其设计、可读性和可维护性。通过定期审查和重构代码库，你可以保持其整洁、有序并适应变化。

### 示例：

假设我们有一个服务类，其中的一个方法变得过于庞大和复杂。我们可以将其重构为更小、更易于管理的方法：

```csharp
// 重构前
public class OrderService
{
    public void ProcessOrder(Order order)
    {
        // 复杂逻辑在此...
    }
}

// 重构后
public class OrderService
{
    public void ProcessOrder(Order order)
    {
        ValidateOrder(order);
        CalculateTotalAmount(order);
        ApplyDiscounts(order);
        GenerateInvoice(order);
        SendConfirmationEmail(order);
    }

    private void ValidateOrder(Order order)
    {
        // 验证逻辑...
    }

    private void CalculateTotalAmount(Order order)
    {
        // 计算逻辑...
    }

    private void ApplyDiscounts(Order order)
    {
        // 折扣逻辑...
    }

    private void GenerateInvoice(Order order)
    {
        // 发票生成逻辑...
    }

    private void SendConfirmationEmail(Order order)
    {
        // 邮件发送逻辑...
    }
}
```

## 保持依赖关系的整洁

保持依赖关系的整洁对于维护整洁架构的完整性和模块化至关重要。随着项目的演进，确保组件和层之间的依赖关系定义明确并得到妥善管理。避免引入不必要的依赖或紧密耦合组件，因为这可能导致架构变得僵化和脆弱。

### 示例：

假设我们有一个依赖于外部库的服务类。为了保持依赖关系的整洁，我们可以使用依赖注入将外部依赖注入到服务类中：

```csharp
public class ProductService
{
    private readonly ILogger _logger;

    public ProductService(ILogger logger)
    {
        _logger = logger;
    }

    public void DoSomething()
    {
        _logger.Log("Doing something...");
    }
}
```

## 演进架构

随着项目的演进，要准备好相应地演进你的架构。关注新技术、最佳实践和架构模式，并愿意在适当的时候调整你的架构以融入它们。考虑定期审查和修订你的架构，以确保它继续满足你的项目和利益相关者的需求。

### 示例：

假设一种新的微服务架构模式成为扩展项目的最佳实践。你可以逐步将你的单体架构重构为微服务，遵循整洁架构原则以保持服务之间的模块化和独立性：

```csharp
// 单体架构
public class MonolithicProductService
{
    // 服务逻辑...
}

// 微服务架构
public class ProductService
{
    private readonly IProductRepository _productRepository;

    public ProductService(IProductRepository productRepository)
    {
        _productRepository = productRepository;
    }

    public List<Product> GetAllProducts()
    {
        return _productRepository.GetAll();
    }
}
```

## 测试驱动开发 (TDD)

测试驱动开发 (TDD) 是在项目演进过程中维护整洁架构的一项宝贵实践。通过在实现新功能或重构现有代码之前编写测试，你可以确保你的代码保持可测试性、可靠性和对变化的韧性。TDD 还有助于防止回归并维护架构的完整性。

### 示例：

假设我们想为订单处理系统添加一个新功能。我们可以从编写一个失败的测试开始，该测试指定了该功能的预期行为：

```csharp
public class OrderServiceTests
{
    [Fact]
    public void ProcessOrder_Should_SendConfirmationEmail()
    {
        // Arrange
        var order = new Order();
        var emailServiceMock = new Mock<IEmailService>();
        var orderService = new OrderService(emailServiceMock.Object);

        // Act
        orderService.ProcessOrder(order);

        // Assert
        emailServiceMock.Verify(x => x.SendConfirmationEmail(order), Times.Once);
    }
}
```

随着项目使用 C# 10 和 .NET 6 不断演进，要保持整洁架构需要持续的努力、对细节的关注以及对最佳实践的承诺。通过持续重构代码库、保持依赖关系清晰、演进架构以及实践测试驱动开发，你可以确保你的架构随着时间的推移保持可扩展性、灵活性和可维护性。通过优先考虑整洁代码和遵守架构原则，你可以构建健壮、可靠且适应性强的软件系统，以满足你的项目和利益相关者的需求。

## 第 13 章

### C# 和 .NET 整洁架构的未来

### 软件开发与整洁架构的新兴趋势

软件开发的新兴趋势正在不断塑造技术格局，影响着开发者设计、构建和维护软件系统的方式。整洁架构以其对模块化、可测试性和可维护性的关注，在面对这些趋势时仍然是一种相关且适应性强的架构方法。在本指南中，我们将探讨软件开发中的一些新兴趋势，以及它们如何与 C# 10 项目中使用 .NET 6 的整洁架构相交，并结合代码示例来说明其实现。

### 微服务架构

近年来，微服务架构获得了显著的发展，它提供了一种构建可扩展、弹性且可独立部署的软件系统的方式。整洁架构与微服务的原则非常契合，因为它促进了模块化、关注点分离以及组件之间的松耦合。

### 示例：

```csharp
// 用于产品管理的微服务

public class ProductService
{
    private readonly IProductRepository _productRepository;

    public ProductService(IProductRepository productRepository)
    {
        _productRepository = productRepository;
    }

    public List<Product> GetAllProducts()
    {
        return _productRepository.GetAll();
    }
}
```

### 无服务器计算

无服务器计算允许开发者构建和运行应用程序，而无需管理基础设施。整洁架构可以通过将业务逻辑封装在由事件或 HTTP 请求触发的函数或服务中，从而适应无服务器环境。

示例：

```csharp
// 用于处理订单的无服务器函数

public class OrderFunction
{
    public async Task<IActionResult> ProcessOrder([HttpTrigger(AuthorizationLevel.Function,
    "post", Route = "orders")] HttpRequest req)
    {
        // 处理订单逻辑...

        return new OkResult();
    }
}
```

### 容器化与编排

使用 Docker 等技术进行容器化，以及使用 Kubernetes 等平台进行编排，已成为大规模部署和管理应用程序的标准实践。整洁架构可以被打包到容器中，每个组件或服务被封装为一个单独的容器。

示例：

服务的 Dockerfile：

```dockerfile
FROM mcr.microsoft.com/dotnet/runtime:6.0 AS base
WORKDIR /app
FROM mcr.microsoft.com/dotnet/sdk:6.0 AS build
WORKDIR /src
COPY . .
RUN dotnet build -c Release -o /app/build
FROM build AS publish
RUN dotnet publish -c Release -o /app/publish
FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "MyService.dll"]
```

### 云原生开发

云原生开发专注于构建针对云环境优化的应用程序，利用云服务和 API。整洁架构通过将基础设施关注点从业务逻辑中抽象出来，并促进框架和平台的独立性，从而促进云原生开发。

### 示例：

```csharp
// 使用 Azure Blob Storage 的云原生服务
public class FileService
{
    private readonly BlobServiceClient _blobServiceClient;
    public FileService(BlobServiceClient blobServiceClient)
    {
        _blobServiceClient = blobServiceClient;
    }
    public async Task UploadFileAsync(Stream fileStream, string fileName)
    {
        var containerClient = _blobServiceClient.GetBlobContainerClient("files");
        var blobClient = containerClient.GetBlobClient(fileName);

        await blobClient.UploadAsync(fileStream, true);
    }
}
```

### 事件驱动架构

事件驱动架构通过事件的交换实现组件之间的解耦通信。整洁架构可以利用事件驱动模式来编排服务或组件之间的交互，促进松耦合和可扩展性。

示例：

```csharp
// 事件驱动的订单处理

public class OrderProcessor
{
    private readonly IMessageBus _messageBus;

    public OrderProcessor(IMessageBus messageBus)
    {
        _messageBus = messageBus;
    }

    public async Task ProcessOrder(Order order)
    {
        // 处理订单逻辑...
        await _messageBus.PublishAsync(new OrderProcessedEvent(order.Id));
    }
}
```

软件开发的新兴趋势正在推动创新，并重塑我们构建和部署软件系统的方式。整洁架构仍然是一种通用且适应性强的架构方法，与这些趋势非常契合，提供了促进模块化、可扩展性和可维护性的原则和实践。通过在整洁架构的背景下利用微服务、无服务器计算、容器化、云原生开发和事件驱动架构等技术和模式，开发者可以构建健壮、可扩展且面向未来的软件系统，以满足现代技术格局的需求。随着软件开发的不断发展，整洁架构为构建弹性且可持续的软件解决方案提供了坚实的基础。

### 整洁架构项目的持续集成与持续交付 (CI/CD)

持续集成与持续交付 (CI/CD) 是现代软件开发中的关键实践，它使团队能够自动化构建、测试和部署流程。当应用于使用 C# 10 和 .NET 6 的整洁架构项目时，CI/CD 有助于确保代码更改被顺利集成、彻底测试并可靠部署，从而维护软件系统的完整性和质量。在本指南中，我们将探讨如何为整洁架构项目实施 CI/CD，包括代码示例和最佳实践。

### 整洁架构的 CI/CD 概述

CI/CD 涉及自动化集成代码更改、运行测试以及将应用程序部署到生产环境的过程。对于整洁架构项目，CI/CD 流水线通常包括构建解决方案、运行单元测试、执行集成测试以及将工件部署到目标环境等步骤。通过自动化这些流程，团队可以减少人为错误、加速反馈循环，并更频繁、更可靠地交付软件。

### 设置 CI/CD 流水线

让我们概述为整洁架构项目设置 CI/CD 流水线所涉及的步骤：

1.  **源代码管理：** 将你的源代码托管在像 Git 这样的版本控制系统中，并使用像 GitFlow 这样的分支策略来管理功能分支、发布和热修复。
2.  **CI/CD 配置：** 使用像 Azure DevOps、GitHub Actions 或 Jenkins 这样的 CI/CD 平台定义 CI/CD 流水线。配置流水线阶段以构建、测试和部署应用程序。
3.  **构建阶段：** 在构建阶段，编译解决方案、恢复依赖项并打包用于部署的工件。
4.  **测试阶段：** 运行自动化测试，包括单元测试、集成测试和端到端测试，以确保代码更改符合质量标准。
5.  **部署阶段：** 使用像 Terraform 或 Azure Resource Manager 模板这样的基础设施即代码 (IaC) 工具，将应用程序部署到目标环境，如开发、预生产和生产环境。

### CI/CD 流水线示例

让我们使用 GitHub Actions 为整洁架构项目创建一个 CI/CD 流水线示例：

yaml
name: CI/CD

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: 检出代码
        uses: actions/checkout@v2
      - name: 设置 .NET
        uses: actions/setup-dotnet@v1
        with:
          dotnet-version: '6.0.x'
      - name: 还原依赖项
        run: dotnet restore
      - name: 构建解决方案
        run: dotnet build --configuration Release
      - name: 运行单元测试
        run: dotnet test --configuration Release --logger trx
      - name: 发布构建产物
        uses: actions/upload-artifact@v2
        with:
          name: publish
          path: bin/Release/net6.0
  deploy:
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: 下载构建产物
        uses: actions/download-artifact@v2
        with:
          name: publish
      - name: 部署到 Azure
        uses: azure/webapps-deploy@v2
        with:
          app-name: 'my-app'
          slot-name: 'production'
          publish-profile: ${{ secrets.AZURE_WEBAPP_PUBLISH_PROFILE }}
          package: .

## 使用整洁架构进行 CI/CD 的最佳实践

为了最大化 CI/CD 对整洁架构项目的效益，请考虑以下最佳实践：

1.  **自动化一切：** 尽可能自动化构建、测试和部署流程，以减少人工操作并降低出错风险。
2.  **流水线即代码：** 使用 YAML 或其他配置文件将 CI/CD 流水线定义为代码，将其与源代码一起进行版本控制，并将其视为仓库中的一等公民。
3.  **快速反馈：** 优化 CI/CD 流水线的速度，为开发者提供快速反馈。并行化测试、使用缓存机制并最小化构建时间，以缩短反馈循环。
4.  **环境一致性：** 确保开发、预生产和生产环境之间的一致性，以最小化部署问题并保持可靠性。
5.  **安全扫描：** 将安全扫描工具集成到 CI/CD 流水线中，以便在开发过程的早期识别和修复漏洞。
6.  **回滚策略：** 实施回滚策略，以便在部署失败或生产环境出现问题时回退更改，确保应用程序的稳定性和可用性。

## 示例部署策略

以下是一些可以作为整洁架构项目 CI/CD 流水线一部分实施的常见部署策略：

1.  **蓝/绿部署：** 将应用程序的新版本与现有版本并行部署，逐步将流量转移到新版本，并在出现问题时回滚。
2.  **金丝雀部署：** 逐步将应用程序的新版本推送给部分用户或服务器，在推送给整个用户群之前监控问题。
3.  **功能开关：** 使用功能开关在生产环境中启用或禁用新功能，允许受控的发布和在出现问题时快速回滚。

CI/CD 是维护使用 C# 10 和 .NET 6 的整洁架构项目的完整性、可靠性和敏捷性的关键实践。通过自动化构建、测试和部署流程，团队可以加速开发周期、减少人工错误，并更频繁、更可靠地交付软件。通过遵循最佳实践、实施部署策略并利用自动化工具，开发者可以建立强大的 CI/CD 流水线，以支持整洁架构项目的演进和发展，使团队能够自信且高效地交付高质量软件。

## 利用整洁架构实现 C# 和 .NET 6 项目的长期成功

在 C# 10 和 .NET 6 中利用整洁架构实现项目的长期成功，需要采用结构化、模块化和可维护的软件开发方法。整洁架构为构建可扩展、可测试和可适应的软件系统提供了坚实的基础，这些系统可以随时间演进以满足不断变化的需求和技术进步。在本指南中，我们将探讨如何利用整洁架构实现项目的长期成功，包括关键原则、最佳实践和代码示例。

## 整洁架构的关键原则

整洁架构强调几个对项目长期成功至关重要的关键原则：

1.  **关注点分离：** 将系统划分为多个层，每层负责功能的特定方面。这种分离使得系统更易于维护、测试和演进。
2.  **依赖规则：** 依赖应指向内部，高层模块依赖于低层模块。这促进了灵活性，因为高层模块不与特定实现耦合。
3.  **可测试性：** 设计组件使其易于独立测试，从而进行全面的单元测试、集成测试和端到端测试。
4.  **框架独立性：** 保持业务逻辑独立于任何外部框架或技术，从而在选择技术栈时保持灵活性，并使系统能够适应未来的技术变化。

## 在 C# 10 和 .NET 6 中实施整洁架构

让我们探讨如何在 C# 10 和 .NET 6 项目中实施整洁架构，从目录结构开始：

```
MyApp.Core/
    - 包含领域实体和业务逻辑
MyApp.Infrastructure/
    - 包含数据访问逻辑和外部依赖项
MyApp.Services/
    - 包含应用程序服务和用例
MyApp.Api/
    - 包含应用程序的 API 端点
```

## 示例代码：领域实体

```csharp
namespace MyApp.Core.Entities
{
    public class Product
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public decimal Price { get; set; }
    }
}
```

## 示例代码：数据访问逻辑

```csharp
namespace MyApp.Infrastructure.Persistence
{
    public class ProductRepository : IProductRepository
    {
        private readonly AppDbContext _context;
        public ProductRepository(AppDbContext context)
        {
            _context = context;
        }
        public async Task<List<Product>> GetAllAsync()
        {
            return await _context.Products.ToListAsync();
        }
        // 其他数据访问方法...
    }
}
```

## 示例代码：应用程序服务

```csharp
namespace MyApp.Services
{
    public class ProductService : IProductService
    {
        private readonly IProductRepository _productRepository;
        public ProductService(IProductRepository productRepository)
        {
            _productRepository = productRepository;
        }
        public async Task<List<Product>> GetAllProductsAsync()
        {
            return await _productRepository.GetAllAsync();
        }
        // 其他服务方法...
    }
}
```

## 示例代码：API 端点

```csharp
namespace MyApp.Api.Controllers
{
    [ApiController]
    [Route("api/products")]
    public class ProductController : ControllerBase
    {
        private readonly IProductService _productService;
        public ProductController(IProductService productService)
        {
            _productService = productService;
        }
        [HttpGet]
        public async Task<ActionResult<List<Product>>> GetAllProducts()
        {
            var products = await _productService.GetAllProductsAsync();
            return Ok(products);
        }
        // 其他 API 端点...
    }
}
```

## 整洁架构对长期成功的益处

在 C# 10 和 .NET 6 项目中实施整洁架构为项目的长期成功带来了多项益处：

1.  **可扩展性：** 整洁架构促进了模块化和关注点分离，使系统能够在复杂性和功能增长时优雅地扩展。
2.  **可维护性：** 层和依赖项的清晰分离使得系统更易于随时间维护和演进，降低了技术债务和代码腐化的风险。
3.  **灵活性：** 整洁架构在选择技术栈、框架和部署策略方面提供了灵活性，确保系统能够适应不断变化的需求和技术进步。
4.  **可测试性：** 通过设计，整洁架构促进了从单个组件的单元测试到整个系统的集成测试等各个层面的全面测试。这确保了系统随时间的可靠性和稳定性。

在 C# 10 和 .NET 6 中利用整洁架构实现项目的长期成功，需要采用结构化、模块化和可维护的软件开发方法。通过遵循关注点分离、依赖反转、可测试性和框架独立性等关键原则，开发者可以构建可扩展、灵活且可靠的软件系统，这些系统可以随时间演进以满足不断变化的需求和技术进步。通过在 C# 10 和 .NET 6 项目中实施整洁架构并遵循最佳实践，团队可以确保其软件项目的长期成功和可持续性，自信且高效地为用户和利益相关者交付价值。

## 结论

总而言之，结合 C# 10 和 .NET 6 的 Clean Architecture 为构建可扩展、可维护和可适应的软件系统提供了坚实的基础。遵循 Clean Architecture 的原则，开发者可以创建模块化、可测试且独立的组件，从而促进项目的长期成功。

通过 Clean Architecture，关注点分离确保了应用程序的每一层都有明确的职责，使代码库更易于理解、维护和扩展。这种分离也使得在选择技术和框架时具有灵活性，使系统能够抵御技术趋势变化的影响。

可测试性是 Clean Architecture 的基石，它允许开发者编写全面的单元测试、集成测试和端到端测试，以确保系统的可靠性和稳定性。通过设计易于测试的组件，开发者可以在开发过程的早期识别和修复问题，从而降低生产环境中出现缺陷和回归的风险。

此外，Clean Architecture 通过提供一个可扩展的结构来促进可扩展性，该结构能够随着时间的推移适应增长和复杂性。无论是构建单体应用程序还是分布式微服务，Clean Architecture 都提供了一种灵活且可适应的方法来构建能够随业务需求扩展的软件系统。

再者，Clean Architecture 中框架和技术的独立性确保了系统能够抵御技术栈和部署环境变化的影响。这种独立性允许开发者在新技术和工具出现时采用它们，而无需绑定到特定的框架或平台。

本质上，结合 C# 10 和 .NET 6 的 Clean Architecture 赋能开发者构建能够长期为用户和利益相关者提供价值的高质量软件系统。通过拥抱 Clean Architecture 的原则并利用 C# 10 和 .NET 6 的能力，开发者可以创建不仅功能可靠，而且能够适应技术和业务需求不断变化的软件。

## 附录

### 术语表

以下是基于 C# 10 Clean Architecture 与 .NET 6 的术语表：

1.  **Clean Architecture：** 一种软件架构模式，强调关注点分离、框架独立性和组件的可测试性。
2.  **C# 10：** C# 编程语言的最新版本，具有新的语言特性和增强功能，旨在提高开发者的生产力和代码表达力。
3.  **.NET 6：** .NET 平台的最新版本，在性能、生产力和跨平台支持方面有所改进，可用于构建各种应用程序。
4.  **领域实体：** 表示应用程序领域内现实世界概念或实体的对象，通常包含模拟实体行为的属性和方法。
5.  **仓储：** 负责抽象数据访问逻辑的组件，提供用于访问和操作来自外部数据源（如数据库）数据的接口。
6.  **应用服务：** 负责实现应用程序业务逻辑和用例的组件，协调领域实体和仓储之间的交互。
7.  **API 端点：** 与应用程序交互的入口点，在 Web 应用程序中通常实现为 HTTP 端点，允许客户端对资源执行 CRUD（创建、读取、更新、删除）操作。
8.  **依赖注入 (DI)：** 一种用于实现控制反转的设计模式和技术，其中依赖项从外部源注入到组件中，从而实现松耦合和更轻松的测试。
9.  **路由：** 将传入请求映射到应用程序中相应端点或控制器的过程，通常使用匹配特定 URL 模式的路由模式来定义。
10. **中间件：** 在 ASP.NET Core 应用程序的请求处理管道中执行的组件，允许将日志记录、身份验证和错误处理等横切关注点统一应用于传入请求。
11. **Entity Framework Core：** 一个用于 .NET 的对象关系映射 (ORM) 框架，使开发者能够使用面向对象的概念来操作关系数据库，从而简化数据访问和持久化操作。
12. **单元测试：** 编写自动化测试以单独验证单个组件或代码单元行为的实践，确保每个单元在不同条件下按预期运行。
13. **集成测试：** 测试应用程序多个组件或模块之间交互的实践，以确保它们作为一个整体正确工作，通常涉及跨层或跨边界的测试。
14. **端到端测试：** 从用户角度测试整个应用程序的实践，模拟用户交互并验证应用程序在真实场景中是否正确运行。
15. **持续集成 (CI)：** 一种开发实践，其中代码更改会自动集成到共享存储库中并持续进行测试，确保代码库保持稳定并随时可以部署。
16. **持续交付 (CD)：** 一种开发实践，其中代码库的更改在通过自动化测试和质量检查后，会自动部署到生产或预发布环境。

## 展示 Clean Architecture 与 C# 10 和 .NET 6 的示例应用程序代码

创建一个展示 Clean Architecture 与 C# 10 和 .NET 6 的示例应用程序涉及将应用程序构建为分层结构，实现领域实体、用于数据访问的仓储、用于业务逻辑的服务以及用于交互的端点。在本指南中，我们将使用 Clean Architecture 原则构建一个简单的电子商务应用程序。

### 目录结构

```
MyECommerce.Core/
    - 包含领域实体和业务逻辑
MyECommerce.Infrastructure/
    - 包含数据访问逻辑和外部依赖项
MyECommerce.Application/
    - 包含应用服务和用例
MyECommerce.Api/
    - 包含应用程序的 API 端点
```

### 示例领域实体

```csharp
// MyECommerce.Core/Entities/Product.cs
namespace MyECommerce.Core.Entities
{
    public class Product
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public decimal Price { get; set; }
    }
}
```

### 示例数据访问逻辑

```csharp
// MyECommerce.Infrastructure/Persistence/ProductRepository.cs
using MyECommerce.Core.Entities;
using System.Collections.Generic;
using System.Threading.Tasks;

namespace MyECommerce.Infrastructure.Persistence
{
    public interface IProductRepository
    {
        Task<List<Product>> GetAllAsync();
    }

    public class ProductRepository : IProductRepository
    {
        public async Task<List<Product>> GetAllAsync()
        {
            // 从数据库获取产品的逻辑
            return new List<Product>();
        }
    }
}
```

### 示例应用服务

```csharp
// MyECommerce.Application/Services/ProductService.cs
using MyECommerce.Core.Entities;
using MyECommerce.Infrastructure.Persistence;
using System.Collections.Generic;
using System.Threading.Tasks;

namespace MyECommerce.Application.Services
{
    public interface IProductService
    {
        Task<List<Product>> GetAllProductsAsync();
    }

    public class ProductService : IProductService
    {
        private readonly IProductRepository _productRepository;

        public ProductService(IProductRepository productRepository)
        {
            _productRepository = productRepository;
        }

        public async Task<List<Product>> GetAllProductsAsync()
        {
            return await _productRepository.GetAllAsync();
        }
    }
}
```

### 示例 API 端点

```csharp
// MyECommerce.Api/Controllers/ProductController.cs
```

## 依赖注入配置

```csharp
using Microsoft.AspNetCore.Mvc;
using MyECommerce.Application.Services;
using MyECommerce.Core.Entities;
using System.Collections.Generic;
using System.Threading.Tasks;

namespace MyECommerce.Api.Controllers
{
    [ApiController]
    [Route("api/products")]
    public class ProductController : ControllerBase
    {
        private readonly IProductService _productService;

        public ProductController(IProductService productService)
        {
            _productService = productService;
        }

        [HttpGet]
        public async Task<ActionResult<List<Product>>> GetAllProducts()
        {
            var products = await _productService.GetAllProductsAsync();
            return Ok(products);
        }
    }
}
```

```csharp
// MyECommerce.Api/Startup.cs
using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Hosting;
using Microsoft.Extensions.Configuration;
using Microsoft.Extensions.DependencyInjection;
using Microsoft.Extensions.Hosting;
using MyECommerce.Application.Services;
using MyECommerce.Infrastructure.Persistence;

namespace MyECommerce.Api
{
    public class Startup
    {
        public IConfiguration Configuration { get; }

        public Startup(IConfiguration configuration)
        {
            Configuration = configuration;
        }

        public void ConfigureServices(IServiceCollection services)
        {
            // 为仓储配置依赖注入
            services.AddScoped<IProductRepository, ProductRepository>();
            // 为服务配置依赖注入
            services.AddScoped<IProductService, ProductService>();
            services.AddControllers();
        }

        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            if (env.IsDevelopment())
            {
                app.UseDeveloperExceptionPage();
            }

            app.UseRouting();

            app.UseEndpoints(endpoints =>
            {
                endpoints.MapControllers();
            });
        }
    }
}
```

在这个示例应用中，我们演示了如何使用 C# 10 和 .NET 6 实现整洁架构，具体方法是将应用分层、定义领域实体、实现数据访问逻辑、创建应用服务以及暴露 API 端点。遵循整洁架构的原则，开发者可以创建可扩展、可维护且可测试的软件系统，这些系统能够随着时间的推移不断演进，以适应不断变化的需求和技术进步。这个示例应用是使用 C# 10 和 .NET 6 构建基于整洁架构的真实世界应用的起点。