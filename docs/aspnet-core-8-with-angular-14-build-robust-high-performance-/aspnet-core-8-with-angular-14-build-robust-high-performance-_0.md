
![](img/image_rsrc58Y.jpg)

# ASP.NET Core 8 与 Angular 14

构建健壮、高性能的 Web 应用程序，实现离线功能的渐进式 Web 应用（PWAs），并探索使用 `SignalR` 等工具进行实时通信！

作者

Katie Millie

* * *

版权声明

版权所有 © 2024 Katie Millie。保留所有权利。

* * *

本网站及其内容受版权法和国际协议的保护。未经 Katie Millie 明确书面同意，严禁复制、分发或使用本内容的任何部分。这涵盖了广泛的材料，如文本、图形、徽标、图像、视频和音频录制。此外，本网站上显示的所有商标、服务标志和徽标均属于其各自的所有者。访问或使用本网站，即表示您承认并同意遵守所有版权和知识产权法规。我们非常感谢您尊重 Katie Millie 的知识产权。如果您有任何关于许可或权限的疑问，请使用提供的联系信息与我们联系。

## 目录

引言

第 1 章

解析全栈开发：理解前端与后端技术

选择合适的技术：ASP.NET Core 8 与 Angular 14

第 2 章

搭建开发环境

配置 ASP.NET Core 8 和 Angular 14 开发工具

使用 Git 设置版本控制

第 3 章

精通 ASP.NET Core 8 构建健壮后端

理解控制器与路由

使用 ASP.NET Core MVC 处理 HTTP 请求与响应

第 4 章

在 ASP.NET Core 8 中处理数据

建模数据实体与关系

使用 Web API 创建 CRUD 操作（创建、读取、更新、删除）

第 5 章

ASP.NET Core 8 中的身份验证与授权

使用 JWT（JSON Web 令牌）保护 Web API

基于角色的授权实现安全访问控制

第 6 章

部署 ASP.NET Core 8 Web API

在 Azure 应用服务或云平台上托管

监控与调试已部署的应用程序

第 7 章

深入 Angular 14 构建动态前端

理解 Angular 应用中的数据绑定与用户交互

第 8 章

构建功能丰富的 Angular 14 组件

Angular 应用中的表单与数据验证

使用 Angular HttpClient 调用 Web API

第 9 章

Angular 14 应用中的状态管理

使用 ngRx 进行全局状态管理

在组件中实现本地状态管理

第 10 章

使用 Angular 14 特性增强用户体验

实现服务端渲染（SSR）以提升性能

第 11 章

测试与部署 Angular 14 应用

构建与优化用于生产的 Angular 应用

Angular Web 应用的部署选项

第 12 章

集成 ASP.NET Core 8 与 Angular 14

集成身份验证与授权流程到 Angular

第 13 章

构建包含身份验证与数据的全栈 Web 应用

为用户管理与数据访问构建 API 端点

在 Angular 组件中显示与管理用户数据

第 14 章

高级集成技术与可扩展性

构建支持离线功能的渐进式 Web 应用（PWAs）

利用 SignalR 实现实时通信

第 15 章

超越基础：高级全栈开发

保护 Web API 免受常见漏洞攻击

第 16 章

调试与故障排除全栈应用

识别常见错误与故障排除策略

第 17 章

持续集成与持续交付（CI/CD）

使用 Azure DevOps 等工具实施 CI/CD 流水线

第 18 章

全栈开发的未来

紧跟最新技术发展

结语

附录

A：术语表

## 引言

### 铸就 Web 开发的未来：精通 ASP.NET Core 8 与 Angular 14 全栈开发

想象一下构建动态、交互式的 Web 应用程序，吸引用户并驱动创新。停止在零散的技术间疲于奔命——使用 `ASP.NET Core 8` 和 `Angular 14` 释放全栈开发的潜力。这一强大组合让您能够从熟悉的 `C#` 环境出发，打造无缝的后端和引人入胜的前端。

`ASP.NET Core 8` 与 `Angular 14`：全栈 Web 开发是您掌握这一前沿技术栈的全面指南。告别不同语言和框架的复杂性——本书为您提供必要的知识和实用技能，以无与伦比的效率构建健壮、高性能的 Web 应用程序。

以下是您在这段全栈开发之旅中将收获的内容：

● 深入 `ASP.NET Core 8`：构建可扩展且安全的 Web API，它们是您应用程序的基石。利用 `Entity Framework Core 8` 的强大功能无缝管理数据访问和操作。使用 `IdentityServer` 等工具实现用户身份验证和授权，确保强大的安全措施。学习部署、监控和故障排除服务器端代码的最佳实践。

● 用 `Angular 14` 征服前端：使用 Angular 创新的基于组件的架构构建动态且交互式的用户界面。掌握数据绑定、用户交互和路由，以创造引人入胜的体验。探索高级功能，如使用 `ngRx` 进行复杂应用的状态管理。学习优化和测试您的 Angular 应用程序以获得卓越性能。

● 弥合鸿沟：无缝集成：本书超越了单独的技术。我们将向您展示如何将 `ASP.NET Core 8` 后端与 `Angular 14` 前端无缝集成。学习从您的 Angular 应用程序中调用 Web API，确保流畅的数据流。实现跨越服务器和客户端的用户身份验证和授权流程，保证整体体验的安全性。

但等等，还有更多！我们超越基础，让您能够构建尖端的 Web 应用程序。深入研究构建支持离线功能的渐进式 Web 应用（PWAs）等技术，并探索使用 `SignalR` 等工具进行实时通信。我们还将指导您遵循安全、调试和实施 CI/CD 流水线的最佳实践，以简化开发工作流程。



无论你是希望拓展全栈技能的 Web 开发者，还是渴望掌握最新技术的热心学习者，《ASP.NET Core 8 与 Angular 14：全栈 Web 开发》都是你的终极伙伴。

拥抱 Web 开发的未来。立即订购，开启开发可能性的新世界！

## 第 1 章

### 揭秘全栈开发：理解前端与后端技术

#### 使用 Angular 14 进行前端开发

Angular 是一个流行的前端框架，允许开发者构建动态且交互式的 Web 应用。在本节中，我们将介绍设置 Angular 项目和创建简单组件的基础知识。

##### 设置 Angular 14 项目

首先，确保你已安装`Node.js`和`npm`。然后，你可以使用 Angular CLI 创建一个新的 Angular 项目：

```bash
npm install -g @angular/cli   # 全局安装 Angular CLI
ng new my-angular-app # 创建一个新的 Angular 项目
cd my-angular-app # 进入项目目录
```

##### 创建一个简单组件

让我们创建一个简单的 Angular 组件来显示问候消息。在你的终端中运行以下命令：

```bash
ng generate component greeting  # 生成一个名为'greeting'的新 Angular 组件
```

此命令将创建一个包含组件所需文件的`greeting`文件夹。

现在，让我们编辑`greeting.component.html`文件来显示我们的消息：

```html
<!-- greeting.component.html -->
<h1>欢迎来到我的 Angular 应用！</h1>
```

##### 运行 Angular 应用

你可以使用 Angular CLI 在本地运行你的 Angular 应用：

```bash
ng serve --open   # 启动开发服务器并在默认浏览器中打开应用
```

在浏览器中导航到`http://localhost:4200/`，即可看到你的 Angular 组件显示的问候消息。

#### 使用 ASP.NET Core 8 进行后端开发

ASP.NET Core 是一个多功能框架，专为创建支持云、可跨平台运行且性能优化的现代应用而设计。让我们深入了解如何设置一个基本的 ASP.NET Core API 并将其与我们的 Angular 前端连接。

##### 设置 ASP.NET Core 8 项目

首先，确保你的机器上安装了.NET SDK 8。然后，启动你的终端或命令提示符并执行以下命令：

```bash
dotnet new webapi -n MyApi  # 创建一个名为'MyApi'的新 ASP.NET Core Web API 项目
cd MyApi  # 进入项目目录
```

##### 创建控制器和 API 端点

让我们创建一个简单的 API 控制器来返回问候消息。在你的 ASP.NET Core 项目的`Controllers`文件夹中创建一个名为`GreetingController.cs`的新文件，并添加以下代码：

```csharp
// GreetingController.cs
using Microsoft.AspNetCore.Mvc;

namespace MyApi.Controllers
{
    [ApiController]
    [Route("api/[controller]")]
    public class GreetingController : ControllerBase
    {
        [HttpGet]
        public IActionResult Get()
        {
            return Ok("欢迎来到我的 API！");
        }
    }
}
```

##### 运行 ASP.NET Core API

你可以使用以下命令运行你的 ASP.NET Core API：

```bash
dotnet run
```

在浏览器中导航到`https://localhost:5001/api/greeting`，或使用 Postman 等工具发送 GET 请求，即可看到你的 API 返回的问候消息。

#### 集成前端与后端

现在我们已经设置了 Angular 前端和 ASP.NET Core API，让我们将它们集成起来，从 API 获取数据并在我们的 Angular 应用中显示。

##### 从 Angular 发起 HTTP 请求

打开你 Angular 项目中的`greeting.component.ts`文件，并更新它以向你的 API 发起 HTTP 请求：

```typescript
The request was rejected because it was considered high risk



# 设置你的开发环境

## 安装 Visual Studio 或 Code

为 `ASP.NET Core 8` 和 `Angular 14` 开发安装 Visual Studio 或 Visual Studio Code 是一个简单直接的过程，它为开发者提供了构建现代 Web 应用程序的强大工具和功能。让我们逐步了解如何安装 Visual Studio 和 Visual Studio Code，以及用于 `ASP.NET Core` 和 `Angular` 开发所需的必要扩展。

### 安装 Visual Studio

Visual Studio 是微软推出的一款功能全面的集成开发环境（IDE），支持多种编程语言和平台，包括 `ASP.NET Core` 开发。以下是为 `ASP.NET Core 8` 开发安装 Visual Studio 的步骤：

1.  **下载 Visual Studio**：访问 Visual Studio 官方网站 (`https://visualstudio.microsoft.com/downloads/`) 并下载 Visual Studio 安装程序。
2.  **运行安装程序**：下载安装程序后，运行它。你将看到选择要安装的工作负载和组件的选项。对于 `ASP.NET Core` 开发，请确保选择“.NET 桌面开发”工作负载，其中包含 `ASP.NET` 和 `.NET Core` 组件。
3.  **安装 ASP.NET Core SDK**：在安装过程中，安装程序会提示你安装必要的 SDK。请确保安装 `ASP.NET Core SDK`，这是开发 `ASP.NET Core` 应用程序所必需的。
4.  **安装其他组件（可选）**：根据你的项目需求，你可能需要安装其他组件，例如 Azure 开发工具、SQL Server 工具等。
5.  **完成安装**：按照屏幕上的说明完成安装过程。安装完成后，你可以启动 Visual Studio 并开始创建 `ASP.NET Core` 项目。

## 创建新项目

现在，让我们创建一个 Angular 服务来调用 API：

```bash
ng generate service api # 生成一个名为 'api' 的新 Angular 服务
```

更新该服务以向我们的 API 发送 HTTP GET 请求：

```typescript
// api.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class ApiService {
  private apiUrl = 'https://localhost:5001/api/greeting';

  constructor(private http: HttpClient) { }

  getGreeting(): Observable<string> {
    return this.http.get<string>(this.apiUrl);
  }
}
```

最后，更新一个组件以使用 API 服务：

```typescript
// greeting.component.ts
import { Component, OnInit } from '@angular/core';
import { ApiService } from './api.service';

@Component({
  selector: 'app-greeting',
  templateUrl: './greeting.component.html',
  styleUrls: ['./greeting.component.css']
})
export class GreetingComponent implements OnInit {
  greetingMessage: string;

  constructor(private apiService: ApiService) { }

  ngOnInit(): void {
    this.apiService.getGreeting().subscribe({
      next: (message) => {
        this.greetingMessage = message;
      },
      error: (error) => {
        console.error('Error fetching greeting:', error);
      }
    });
  }
}
```

这个示例演示了如何将 `Angular` 前端与 `ASP.NET Core` API 集成，以无缝地获取和显示数据。

使用 `ASP.NET Core 8` 和 `Angular 14` 的全栈方法提供了诸多优势，包括无缝集成、一致的开发环境、增强的生产力、代码可重用性以及性能优化。通过结合利用这些技术，开发者可以高效地构建健壮、可扩展且现代化的 Web 应用程序。

## 选择合适的技术：ASP.NET Core 8 & Angular 14

为 Web 开发项目选择合适的技术对其成功至关重要。`ASP.NET Core` 和 `Angular` 都是构建现代 Web 应用程序的热门选择，提供了强大的功能和可扩展性。让我们探讨一下为什么 `ASP.NET Core 8` 和 `Angular 14` 是 Web 开发的绝佳组合，并深入一些代码示例来说明它们的能力。

### ASP.NET Core 8

`ASP.NET Core` 是一个跨平台、高性能的框架，专为构建基于云和互联网连接的现代应用程序而量身定制。版本 8 带来了许多改进和特性，提升了开发者的生产力和应用程序性能。

`ASP.NET Core` 的一个关键优势是它支持构建 RESTful API，这对于创建可被 `Angular` 等前端应用程序调用的后端服务至关重要。让我们使用 `ASP.NET Core 8` 创建一个简单的 API 端点：

```csharp
// Startup.cs
public void ConfigureServices(IServiceCollection services)
{
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

// WeatherForecastController.cs
[ApiController]
[Route("api/[controller]")]
public class WeatherForecastController : ControllerBase
{
    [HttpGet]
    public IEnumerable<WeatherForecast> Get()
    {
        var rng = new Random();
        return Enumerable.Range(1, 5).Select(index => new WeatherForecast
        {
            Date = DateTime.Now.AddDays(index),
            TemperatureC = rng.Next(-20, 55),
            Summary = Summaries[rng.Next(Summaries.Length)]
        })
        .ToArray();
    }
}
```

这段代码设置了一个简单的 API 端点 `/api/weatherforecast`，它返回一个天气预报列表。

### Angular 14

`Angular` 是由 Google 开发的一个强大的前端框架，用于构建动态的单页 Web 应用程序。`Angular 14` 引入了新的特性和优化，以提升开发者体验和应用程序性能。

让我们创建一个 `Angular` 组件，它调用我们之前创建的 API 端点并显示天气预报数据：

```typescript
// weather-forecast.component.ts
import { Component, OnInit } from '@angular/core';
import { HttpClient } from '@angular/common/http';

@Component({
  selector: 'app-weather-forecast',
  templateUrl: './weather-forecast.component.html',
  styleUrls: ['./weather-forecast.component.css']
})
export class WeatherForecastComponent implements OnInit {
  forecasts: any[];

  constructor(private http: HttpClient) { }

  ngOnInit(): void {
    this.http.get<any[]>('https://localhost:5001/api/weatherforecast').subscribe(data => {
      this.forecasts = data;
    });
  }
}
```

在这个 `Angular` 组件中，我们使用 `HttpClient` 模块向我们的 `ASP.NET Core` API 端点发送 HTTP GET 请求，并检索天气预报数据。

### HTML 模板

现在，让我们创建 HTML 模板，以便在我们的 `Angular` 组件中显示天气预报数据：

```html
<!-- weather-forecast.component.html -->
<div *ngIf="forecasts">
  <h2>Weather Forecasts</h2>
  <ul>
    <li *ngFor="let forecast of forecasts">
      Date: {{ forecast.date | date }}, Temperature: {{ forecast.temperatureC }}°C, Summary: {{ forecast.summary }}
    </li>
  </ul>
</div>
```

这个 HTML 模板使用了 `Angular` 的数据绑定和结构指令（`*ngIf` 和 `*ngFor`）来动态显示从 API 获取的天气预报数据。

通过结合使用 `ASP.NET Core 8` 进行后端 API 开发和 `Angular 14` 进行前端开发，你将获得一个强大且现代化的技术栈，用于构建可扩展的 Web 应用程序。`ASP.NET Core` 在创建 RESTful API 方面的健壮性，与 `Angular` 在创建动态和交互式用户界面方面的能力相辅相成，使它们成为 Web 开发项目的绝佳选择。




## 2. 安装 Visual Studio Code

Visual Studio Code (VS Code) 是一款轻量级且功能强大的代码编辑器，具有高度可扩展性，支持多种编程语言和框架，包括 Angular 开发。以下是为 Angular 14 开发安装 Visual Studio Code 的步骤：

1.  **下载 Visual Studio Code**：访问 Visual Studio Code 官方网站 (https://code.visualstudio.com/)，下载适合您操作系统（Windows、macOS 或 Linux）的版本。
2.  **安装 Visual Studio Code**：下载安装程序后，运行它以在您的系统上安装 Visual Studio Code。通常，安装过程很简单，您只需同意许可条款并选择安装偏好设置。
3.  **安装 Angular Essentials 扩展**：安装完成后，打开 Visual Studio Code。您首先要做的一件事就是安装 Angular Essentials 扩展包，其中包含 Angular 开发所需的基本扩展。操作如下：
    *   从侧边栏选择扩展图标（或使用快捷键 `Ctrl+Shift+X`）。
    *   在扩展市场中搜索 "Angular Essentials"。
    *   点击安装以安装该扩展包。
4.  **安装 .NET Core SDK**：除了 Visual Studio Code，您还需要单独安装 .NET Core SDK 才能处理 ASP.NET Core 项目。您可以从 .NET 官方网站 (https://dotnet.microsoft.com/download) 下载该 SDK。
5.  **设置 Angular CLI（可选）**：如果您计划使用 Angular CLI 创建新的 Angular 项目，则需要在系统上全局安装它。在 Visual Studio Code 中启动终端并执行此命令：
    ```
    npm install -g @angular/cli
    ```
6.  **开始编码**：安装好 Visual Studio Code、Angular Essentials 扩展、.NET Core SDK 以及 Angular CLI（如果需要）后，您就可以开始编写 ASP.NET Core 8 API 和 Angular 14 前端应用程序了。

为 ASP.NET Core 8 和 Angular 14 开发安装 Visual Studio 或 Visual Studio Code 涉及下载相应的安装程序、选择必要的组件或扩展，并完成安装过程。安装完成后，您就拥有了一个强大的开发环境，可以无缝地创建和构建现代 Web 应用程序。

## 配置 ASP.NET Core 8 和 Angular 14 开发工具

配置 ASP.NET Core 8 和 Angular 14 的开发工具对于确保流畅的开发体验至关重要。在本指南中，我们将逐步介绍为后端 (ASP.NET Core) 和前端 (Angular) 开发设置必要工具和配置的步骤。

### 1. 安装所需软件

在深入配置特定工具之前，请确保您的开发机器上已安装以下软件：

*   **Visual Studio 或 Visual Studio Code**：根据您的偏好选择其一。Visual Studio 是一个功能齐全的 IDE，而 Visual Studio Code 是一个轻量级的代码编辑器。
*   **Node.js 和 npm**：Angular 需要 `Node.js` 和 `npm`（Node 包管理器）来管理依赖项和运行脚本。您可以选择从其官方网站 [`nodejs.org/`](https://nodejs.org/) 下载并安装 `Node.js`。
*   **.NET Core SDK**：从 .NET 官方网站 (https://dotnet.microsoft.com/download) 安装 .NET Core SDK，因为 ASP.NET Core 开发需要它。

### 2. 配置 ASP.NET Core 8

如果您使用 Visual Studio，ASP.NET Core 项目的设置过程在 IDE 中是简化的。如果您使用 Visual Studio Code，则需要手动或通过命令行设置您的 ASP.NET Core 项目。

#### 使用 Visual Studio

1.  **创建新的 ASP.NET Core 项目**：打开 Visual Studio 并创建一个新的 ASP.NET Core Web 应用程序项目。根据您的项目需求选择适当的模板（例如，API、MVC、Razor Pages）。
2.  **配置启动项和中间件**：在 ASP.NET Core 项目的 `Startup.cs` 文件中，根据您的应用程序需求配置中间件、服务和路由。例如，要启用 CORS（跨域资源共享），您可以在 `ConfigureServices` 方法中添加以下代码：
    ```csharp
    services.AddCors(options =>
    {
        options.AddPolicy("AllowAll",
            builder =>
            {
                builder.AllowAnyOrigin()
                       .AllowAnyMethod()
                       .AllowAnyHeader();
            });
    });
    ```
3.  **创建控制器和模型**：创建 ASP.NET Core 控制器来处理 API 端点。定义模型来表示您的数据结构。以下是一个基本控制器的示例：
    ```csharp
    [ApiController]
    [Route("api/[controller]")]
    public class TodoController : ControllerBase
    {
        private readonly ITodoRepository _todoRepository;

        public TodoController(ITodoRepository todoRepository)
        {
            _todoRepository = todoRepository;
        }

        [HttpGet]
        public async Task<IActionResult> GetAllTodos()
        {
            var todos = await _todoRepository.GetAllTodos();
            return Ok(todos);
        }

        // 可以在此处添加其他 CRUD 操作
    }
    ```
4.  **运行和测试应用程序**：您可以直接从 Visual Studio 运行您的 ASP.NET Core 应用程序。使用 Postman 或 Swagger 等工具验证您的 API 端点。

#### 使用 Visual Studio Code

1.  **创建新的 ASP.NET Core 项目**：在 Visual Studio Code 中打开终端，并使用 .NET CLI 创建新的 ASP.NET Core 项目。例如，要创建一个 Web API 项目，请运行：
    ```
    dotnet new webapi -n MyWebApi
    ```
2.  **安装所需的包**：如果您的项目需要额外的包或依赖项，请使用 `npm` 处理前端依赖项，使用 NuGet 处理后端依赖项。
3.  **配置 CORS 和中间件**：与 Visual Studio 设置类似，在 `Startup.cs` 文件中手动配置中间件、服务和其他配置。
4.  **添加控制器和模型**：根据您的应用程序逻辑需要创建控制器和模型。使用 `dotnet` CLI 或 Visual Studio Code 的内置功能来搭建控制器和 CRUD 操作。
5.  **运行和测试应用程序**：使用 `dotnet run` 命令从终端运行您的 ASP.NET Core 应用程序。使用 Postman 或 Swagger 等工具验证您的 API 端点。

### 3. 配置 Angular 14

Angular 开发需要设置 Angular CLI、创建组件、服务以及管理依赖项。让我们逐步介绍在项目中配置 Angular 14 的步骤。

1.  **创建新的 Angular 项目**：在 Visual Studio Code 或任何首选的代码编辑器中打开终端，并使用 Angular CLI 创建新的 Angular 项目。运行以下命令：
    ```
    ng new my-angular-app
    ```
2.  **安装 Angular Material（可选）**：如果您计划使用 Angular Material 作为 UI 组件，可以通过运行以下命令安装它：
    ```
    ng add @angular/material
    ```
3.  **创建组件和服务**：使用 Angular CLI 生成组件、服务、模块等。例如，要创建一个新组件，请运行：
    ```
    ng generate component my-component
    ```
4.  **配置 HttpClient 模块**：如果您的 Angular 应用程序需要与后端 API (ASP.NET Core) 通信，请在 Angular 应用模块 (`app.module.ts`) 中配置 `HttpClientModule`。在导入列表中导入并包含 `HttpClientModule`。
    ```typescript
    import { HttpClientModule } from '@angular/common/http';

    @NgModule({
      declarations: [
        // 您的组件
      ],
      imports: [
        BrowserModule,
        HttpClientModule
      ],
      providers: [],
      bootstrap: [AppComponent]
    })
    export class AppModule { }
    ```
5.  **调用后端 API**：使用 Angular 的 `HttpClient` 向您的 ASP.NET Core API 端点发出 HTTP 请求。以下是一个发出 HTTP GET 请求的服务示例：
    ```typescript
    import { Injectable } from '@angular/core';
    import { HttpClient } from '@angular/common/http';

    @Injectable({
      providedIn: 'root'
    })
    export class ApiService {
      apiUrl = 'https://localhost:5001/api';

      constructor(private http: HttpClient) { }

      getAllTodos() {
        return this.http.get<any[]>(`${this.apiUrl}/todo`);
      }

      // 可以在此部分包含其他 CRUD 操作。
    }
    ```



6\. 运行并测试 Angular 应用：使用 `ng serve` 命令在本地运行你的 Angular 应用程序。在浏览器中访问你的 Angular 应用（默认运行在 `http://localhost:4200`）并测试其功能。

配置 ASP.NET Core 8 和 Angular 14 开发工具涉及设置必要的软件、创建项目、配置中间件、服务、路由以及管理依赖项。通过使用 Visual Studio 或 Visual Studio Code，以及 Angular CLI 和 .NET Core SDK，你将拥有一个强大的开发环境，可以无缝构建现代 Web 应用程序。使用适当的工具测试和调试你的应用程序，可以确保流畅的开发体验。

## 使用 Git 设置版本控制

使用 Git 设置版本控制对于管理代码更改、与团队成员协作以及维护项目修订历史至关重要。无论你是在开发 ASP.NET Core 8 后端还是 Angular 14 前端（或两者兼有），Git 都提供了一个可靠的版本控制系统。让我们逐步了解如何为包含 ASP.NET Core 和 Angular 开发的项目设置 Git。

1\. 安装 Git：如果你尚未安装 Git，可以从官方网站 (https://git-scm.com/) 下载。请遵循适用于你的操作系统（Windows、macOS 或 Linux）的安装指南。

2\. 创建 Git 仓库：安装 Git 后，使用终端或命令提示符导航到项目的根目录。

对于新项目，你可以使用以下命令初始化一个新的 Git 仓库：

```bash
git init
```

此命令在当前目录中创建一个新的 Git 仓库，并将其标记为版本控制项目。

3\. 设置 `.gitignore`：在 ASP.NET Core 和 Angular 项目中，有些文件和目录你不想包含在版本控制中。例如，构建产物、临时文件和依赖项。在项目根目录创建一个 `.gitignore` 文件，以指定 Git 应忽略哪些文件和目录。

以下是一个适用于 ASP.NET Core 和 Angular 项目的 `.gitignore` 文件示例：

```
### ASP.NET Core
bin/
obj/
*.csproj.user
*.dll
*.exe

### Angular
node_modules/
dist/
```

根据你的具体项目结构和依赖项调整 `.gitignore` 文件。

4\. 添加和提交更改：设置好 `.gitignore` 后，你可以开始将文件添加到 Git 仓库并提交更改。

要将所有文件添加到暂存区以进行下一次提交，请使用：

```bash
git add .
```

使用以下命令将更改提交到仓库：

```bash
git commit -m "Initial commit"
```

将 `"Initial commit"` 替换为描述你所做更改的适当提交消息。

5\. 远程仓库（可选）：如果你在团队中工作，或者想在远程服务器（如 GitHub、GitLab 或 Bitbucket）上备份代码，你可以添加一个远程仓库。

例如，要在 GitHub 上添加一个远程仓库：

1\. 在 GitHub 上创建一个新仓库。

2\. 使用以下命令添加远程仓库：

```bash
git remote add origin https://github.com/username/repo-name.git
```

将 `https://github.com/username/repo-name.git` 替换为你的 GitHub 仓库的 URL。

3\. 将你的代码推送到远程仓库：

```bash
git push -u origin main
```

此命令将你的代码推送到远程仓库的 `main` 分支。如果你使用的是不同的分支，请将 `main` 替换为该分支的名称。

6\. 分支和合并（可选）：Git 允许你在单独的分支上处理不同的功能或错误修复，这些分支稍后可以合并到主分支（或其他目标分支）。

要创建一个新分支并切换到它：

```bash
git checkout -b feature-name
```

将 `feature-name` 替换为适当的分支名称。

在分支中进行更改后，你可以提交它们，然后使用 Git 命令（如 `git merge`）或使用 GitHub 等 Git 托管平台的拉取请求机制将分支合并到主分支。

7\. 拉取更改（可选）：如果你在团队中工作或与他人协作，你可能需要从远程仓库拉取更改以保持本地仓库的更新。

要从远程仓库拉取更改：

```bash
git pull origin main
```

将 `main` 替换为你想要拉取更改的分支。

为 ASP.NET Core 8 和 Angular 14 项目设置 Git 版本控制涉及初始化 Git 仓库、创建 `.gitignore` 文件、添加和提交更改，以及可选地设置远程仓库以进行协作。分支、合并和拉取更改是额外的 Git 操作，可以增强你的开发工作流程，尤其是在团队环境中。通过遵循这些步骤，你可以有效地管理代码版本、跟踪更改，并在项目中无缝协作。

## 第 3 章

### 掌握 ASP.NET Core 8 以构建健壮的后端

构建你的第一个 ASP.NET Core 8 Web API 是开始后端开发的好方法。我们将逐步介绍在 Visual Studio 中创建新的 ASP.NET Core 项目、设置一个简单的 Web API 以及使用 Postman 等工具进行测试的过程。同时，我们将考虑与 Angular 14 前端开发的集成。

1\. 在 Visual Studio 中创建 ASP.NET Core 8 项目：

1\. 打开 Visual Studio：在你的开发机器上启动 Visual Studio。

2\. 开始新项目：单击“创建新项目”或导航到“文件” > “新建” > “项目”。

3\. 选择项目模板：在“创建新项目”窗口中，选择“ASP.NET Core Web 应用程序”作为项目类型。单击“下一步”。

4\. 配置项目：为你的项目提供名称和位置。选择所需的框架（ASP.NET Core 8）和项目类型（如 API 或 Web 应用程序）。单击“创建”。

5\. 选择模板：在“创建新的 ASP.NET Core Web 应用程序”窗口中，选择“API”模板。确保选择了“ASP.NET Core 8”作为目标框架。

6\. 配置身份验证（可选）：你可以根据项目要求选择配置身份验证。目前，如果不需要，你可以选择“无身份验证”。

7\. 创建项目：单击“创建”以基于选定的模板和配置创建 ASP.NET Core 项目。

2\. 设置一个简单的 Web API：

项目创建后，你将拥有一个包含 `Controllers`、`Models` 和 `Startup.cs` 等文件夹的基本结构。让我们创建一个简单的 Web API 控制器来处理请求。

1\. 创建控制器：在解决方案资源管理器中右键单击“Controllers”文件夹，然后选择“添加” > “控制器”。

2\. 选择控制器模板：选择“API 控制器 - 空”模板，然后单击“添加”。

3\. 添加控制器代码：在新创建的控制器文件（例如 `ValuesController.cs`）中，添加一些示例代码以创建 API 端点。

```csharp
using Microsoft.AspNetCore.Mvc;
using System;
using System.Collections.Generic;

namespace YourNamespace.Controllers
{
    [Route("api/[controller]")]
    [ApiController]
    public class ValuesController : ControllerBase
    {
        // GET: api/values
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
        public ActionResult Post([FromBody] string value)
        {
            // Save the value or perform necessary actions
            return Ok();
        }

        // PUT api/values/5
        [HttpPut("{id}")]
        public ActionResult Put(int id, [FromBody] string value)
        {
            // Update the value with the provided ID
            return Ok();
        }

        // DELETE api/values/5
        [HttpDelete("{id}")]
        public ActionResult Delete(int id)
        {
            // Delete the value with the provided ID
            return Ok();
        }
    }
}
```



4\. 运行应用程序：使用 Visual Studio 构建并运行你的 ASP.NET Core 应用程序。这将启动开发服务器，允许你测试 Web API 端点。

3\. 测试 Web API：

你可以使用 Postman 等工具测试你的 Web API，该工具允许你发送 HTTP 请求并检查响应。

1\. 打开 Postman：在你的机器上启动 Postman。

2\. 发送 GET 请求：输入你的 Web API 端点的 URL（例如，`https://localhost:5001/api/values`）并选择 GET 方法。提交请求以查看响应。

3\. 测试其他端点：尝试使用 Postman 测试其他端点，如 POST、PUT 和 DELETE。根据需要，在 POST 和 PUT 请求的请求体中提供适当的数据。

4\. 与 Angular 14 集成（可选）：如果你正在将 ASP.NET Core Web API 与 Angular 前端集成，你可以从 Angular 应用程序发出 HTTP 请求以从 API 获取数据。

1\. 创建 Angular 服务：

在你的 Angular 项目中，创建一个服务来处理 HTTP 请求。例如，创建一个名为 `ApiService` 的服务。

```typescript
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class ApiService {
  apiUrl = 'https://localhost:5001/api/values'; // 根据你的 API 更新 URL

  constructor(private http: HttpClient) { }

  getValues(): Observable<string[]> {
    return this.http.get<string[]>(this.apiUrl);
  }

  // 根据需要实现其他 HTTP 方法（POST、PUT、DELETE）
}
```

2\. 在组件中使用服务：在需要发出 API 请求的 Angular 组件中注入 `ApiService`。

```typescript
import { Component, OnInit } from '@angular/core';
import { ApiService } from './api.service';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent implements OnInit {
  values: string[] = [];

  constructor(private apiService: ApiService) {}

  ngOnInit(): void {
    this.apiService.getValues().subscribe(data => {
      this.values = data;
    });
  }
}
```

3\. 在 Angular 模板中显示数据：使用 Angular 的数据绑定在组件的 HTML 模板中显示获取的数据。

```html
<h1>Values from API:</h1>
<ul>
  <li *ngFor="let value of values">{{ value }}</li>
</ul>
```

4\. 运行 Angular 应用程序：构建并运行你的 Angular 应用程序（`ng serve`），以查看从 ASP.NET Core Web API 获取的数据在前端显示。

在 Visual Studio 中创建 ASP.NET Core 8 Web API 涉及设置项目、创建带有 API 端点的控制器，以及使用 Postman 等工具测试 API。与 Angular 14（或任何前端框架）的集成允许你构建一个全栈应用程序，其中前端与后端 API 通信以获取和操作数据。这种方法使你能够开发可扩展且交互式的 Web 应用程序，并在前端和后端功能之间实现清晰的关注点分离。

理解控制器和路由

理解控制器和路由是使用 ASP.NET Core 8 作为后端和 Angular 14 作为前端构建 Web 应用程序的基础。ASP.NET Core 中的控制器处理传入的 HTTP 请求并生成响应，而路由将 URL 映射到特定的控制器操作。让我们通过 ASP.NET Core 和 Angular 的代码示例来深入探讨这些概念。

1\. ASP.NET Core 8 中的控制器：ASP.NET Core 中的控制器是处理传入 HTTP 请求并返回适当响应的类。它们负责处理客户端请求、从模型或服务访问数据，并返回视图或数据作为响应。

以下是一个简单的 ASP.NET Core 控制器示例：

```csharp
using Microsoft.AspNetCore.Mvc;
using System.Collections.Generic;

namespace MyApp.Controllers
{
    [ApiController]
    [Route("api/[controller]")]
    public class ProductsController : ControllerBase
    {
        private readonly IProductService _productService;

        public ProductsController(IProductService productService)
        {
            _productService = productService;
        }

        [HttpGet]
        public IEnumerable<Product> GetAllProducts()
        {
            return _productService.GetAllProducts();
        }

        [HttpGet("{id}")]
        public IActionResult GetProductById(int id)
        {
            var product = _productService.GetProductById(id);
            if (product == null)
            {
                return NotFound();
            }
            return Ok(product);
        }

        [HttpPost]
        public IActionResult CreateProduct([FromBody] Product product)
        {
            _productService.AddProduct(product);
            return CreatedAtAction(nameof(GetProductById), new { id = product.Id }, product);
        }

        [HttpPut("{id}")]
        public IActionResult UpdateProduct(int id, [FromBody] Product product)
        {
            var existingProduct = _productService.GetProductById(id);
            if (existingProduct == null)
            {
                return NotFound();
            }
            existingProduct.Name = product.Name;
            existingProduct.Price = product.Price;
            _productService.UpdateProduct(existingProduct);
            return NoContent();
        }

        [HttpDelete("{id}")]
        public IActionResult DeleteProduct(int id)
        {
            var existingProduct = _productService.GetProductById(id);
            if (existingProduct == null)
            {
                return NotFound();
            }
            _productService.DeleteProduct(id);
            return NoContent();
        }
    }
}
```

在这个示例中，`ProductsController` 处理产品的 CRUD 操作。它定义了各种 HTTP 方法（`HttpGet`、`HttpPost`、`HttpPut`、`HttpDelete`），这些方法对应于对产品资源的不同操作。

2\. ASP.NET Core 8 中的路由：ASP.NET Core 中的路由根据 URL 模式将传入的 HTTP 请求映射到特定的控制器操作。它使框架能够确定哪个控制器和操作应该处理每个请求。

路由通常在 `Startup.cs` 文件中使用 `MapControllerRoute` 方法或属性路由进行配置。

以下是在 `Startup.cs` 中使用属性路由配置路由的示例：

```csharp
using Microsoft.AspNetCore.Builder;
using Microsoft.AspNetCore.Hosting;
using Microsoft.Extensions.DependencyInjection;
using Microsoft.Extensions.Hosting;

namespace MyApp
{
    public class Startup
    {
        public void ConfigureServices(IServiceCollection services)
        {
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

在这个示例中，我们通过在 `ConfigureServices` 方法中调用 `services.AddControllers()` 为控制器启用路由。`UseEndpoints` 中的 `MapControllers` 方法为应用程序设置默认路由。

3\. Angular 14 中的路由：在 Angular 中，路由用于根据 URL 在不同组件之间导航。Angular 内置的 `RouterModule` 提供了强大的路由功能。

以下是在 Angular 中配置路由的示例：

1\. 创建路由模块：在你的 Angular 项目中为路由创建一个新模块（例如，`app-routing.module.ts`）。

```typescript
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { HomeComponent } from './home/home.component';
import { ProductsComponent } from './products/products.component';

const routes: Routes = [
  { path: '', component: HomeComponent },
  { path: 'products', component: ProductsComponent }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

2\. 使用路由器出口：在你的主 `app.component.html` 中，使用 `<router-outlet></router-outlet>` 标签根据路由渲染组件。

```html
<router-outlet></router-outlet>
```

3\. 定义组件：为不同的视图或页面创建 Angular 组件（例如，`home.component.ts`、`products.component.ts`）。



4\. 在路由间导航：使用 Angular 的 `Router` 服务或 HTML 模板中的 `routerLink` 指令，通过编程方式或用户交互在路由间导航。

```typescript
import { Component } from '@angular/core';
import { Router } from '@angular/router';

@Component({
  selector: 'app-navbar',
  templateUrl: './navbar.component.html'
})
export class NavbarComponent {
  constructor(private router: Router) {}

  navigateToProducts() {
    this.router.navigate(['/products']);
  }
}
```

```html
<button (click)="navigateToProducts()">前往产品页</button>
```

ASP.NET Core 中的控制器处理 HTTP 请求，并根据定义的操作生成响应，而路由则将 URL 映射到特定的控制器操作。在 Angular 中，路由支持基于 URL 在组件之间导航。理解这些概念并正确实现它们，对于构建使用 ASP.NET Core 8 作为后端、Angular 14 作为前端的健壮 Web 应用程序至关重要。

## 使用 ASP.NET Core MVC 处理 HTTP 请求和响应

处理 HTTP 请求和响应是使用 ASP.NET Core MVC 作为后端、Angular 14 作为前端构建 Web 应用程序的核心方面。在本指南中，我们将探讨如何在 ASP.NET Core MVC 应用程序中处理各种类型的 HTTP 请求（`GET`、`POST`、`PUT`、`DELETE`）和响应，并将其与 Angular 14 前端集成。

### 1. 设置 ASP.NET Core MVC 项目

首先，让我们在 Visual Studio 中创建一个 ASP.NET Core MVC 项目，并设置必要的控制器、模型和视图。

1.  **创建 ASP.NET Core MVC 项目**：打开 Visual Studio，创建一个新的 ASP.NET Core Web 应用程序项目。选择模板 "ASP.NET Core Web App (Model-View-Controller)"。
2.  **添加模型类**：创建一个模型类来表示你的数据。作为示例，我们来生成一个 `Product` 模型：

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
}
```

3.  **创建控制器**：添加一个控制器来处理与产品相关的 HTTP 请求。右键单击 `Controllers` 文件夹，添加一个名为 `ProductsController` 的新控制器。

```csharp
using Microsoft.AspNetCore.Mvc;
using System.Collections.Generic;
using System.Linq;

namespace MyApp.Controllers
{
    [ApiController]
    [Route("api/[controller]")]
    public class ProductsController : ControllerBase
    {
        private static List<Product> _products = new List<Product>
        {
            new Product { Id = 1, Name = "Product 1", Price = 10.99m },
            new Product { Id = 2, Name = "Product 2", Price = 20.39m }
        };

        [HttpGet]
        public IActionResult GetProducts()
        {
            return Ok(_products);
        }

        [HttpGet("{id}")]
        public IActionResult GetProductById(int id)
        {
            var product = _products.FirstOrDefault(p => p.Id == id);
            if (product == null)
            {
                return NotFound();
            }
            return Ok(product);
        }

        [HttpPost]
        public IActionResult CreateProduct([FromBody] Product product)
        {
            product.Id = _products.Count + 1;
            _products.Add(product);
            return CreatedAtAction(nameof(GetProductById), new { id = product.Id }, product);
        }

        [HttpPut("{id}")]
        public IActionResult UpdateProduct(int id, [FromBody] Product product)
        {
            var existingProduct = _products.FirstOrDefault(p => p.Id == id);
            if (existingProduct == null)
            {
                return NotFound();
            }
            existingProduct.Name = product.Name;
            existingProduct.Price = product.Price;
            return NoContent();
        }

        [HttpDelete("{id}")]
        public IActionResult DeleteProduct(int id)
        {
            var existingProduct = _products.FirstOrDefault(p => p.Id == id);
            if (existingProduct == null)
            {
                return NotFound();
            }
            _products.Remove(existingProduct);
            return NoContent();
        }
    }
}
```

### 2. 在 ASP.NET Core MVC 中处理 HTTP 请求和响应

现在我们已经设置好了带有 `ProductsController` 的 ASP.NET Core MVC 项目，让我们来理解每种 HTTP 方法是如何被处理的。

*   **GET 请求**：`GetProducts` 方法处理 `GET` 请求以检索所有产品，而 `GetProductById` 处理 `GET` 请求以通过 ID 检索特定产品。
*   **POST 请求**：`CreateProduct` 方法处理 `POST` 请求以创建新产品。产品详情在请求体（`[FromBody]`）中接收。
*   **PUT 请求**：`UpdateProduct` 方法处理 `PUT` 请求以更新现有产品。它期望在 URL 中提供产品 ID，并在请求体中提供更新后的产品详情。
*   **DELETE 请求**：`DeleteProduct` 方法处理 `DELETE` 请求以通过 ID 删除产品。

### 3. 与 Angular 14 前端集成

让我们将 ASP.NET Core MVC 后端与 Angular 14 前端集成，以演示如何从客户端处理 HTTP 请求和响应。

1.  **创建 Angular 服务**：在你的 Angular 项目中，创建一个服务来处理对 ASP.NET Core API 的 HTTP 请求。

```typescript
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';
import { Product } from './product.model';

@Injectable({
  providedIn: 'root'
})
export class ProductService {
  private apiUrl = 'https://localhost:5001/api/products'; // 根据你的 API 更新 URL

  constructor(private http: HttpClient) { }

  getProducts(): Observable<Product[]> {
    return this.http.get<Product[]>(this.apiUrl);
  }

  getProductById(id: number): Observable<Product> {
    return this.http.get<Product>(`${this.apiUrl}/${id}`);
  }

  createProduct(product: Product): Observable<Product> {
    return this.http.post<Product>(this.apiUrl, product);
  }

  updateProduct(id: number, product: Product): Observable<Product> {
    return this.http.put<Product>(`${this.apiUrl}/${id}`, product);
  }

  deleteProduct(id: number): Observable<void> {
    return this.http.delete<void>(`${this.apiUrl}/${id}`);
  }
}
```

2.  **在 Angular 组件中使用服务**：在需要发起 API 请求的 Angular 组件中注入 `ProductService`。

```typescript
import { Component, OnInit } from '@angular/core';
import { ProductService } from './product.service';
import { Product } from './product.model';

@Component({
  selector: 'app-products',
  templateUrl: './products.component.html'
})
export class ProductsComponent implements OnInit {
  products: Product[] = [];

  constructor(private productService: ProductService) {}

  ngOnInit(): void {
    this.productService.getProducts().subscribe(data => {
      this.products = data;
    });
  }
}
```

3.  **在 Angular 模板中显示数据**：使用 Angular 的数据绑定在组件的 HTML 模板中显示获取的数据。

```html
<h1>产品列表</h1>
<ul>
  <li *ngFor="let product of products">
    {{ product.id }} - {{ product.name }} - ${{ product.price }}
  </li>
</ul>
```

4.  **添加创建产品功能**：在你想要创建产品的 Angular 组件中，实现调用 `ProductService` 的 `createProduct` 方法的逻辑。

```typescript
import { Component } from '@angular/core';
import { ProductService } from './product.service';
import { Product } from './product.model';

@Component({
  selector: 'app-product-form',
  templateUrl: './product-form.component.html'
})
export class ProductFormComponent {
  newProduct: Product = { id: 0, name: '', price: 0 };

  constructor(private productService: ProductService) {}

  createProduct() {
    this.productService.createProduct(this.newProduct).subscribe(() => {
      // 刷新产品列表或根据需要执行其他操作
      this.newProduct = { id: 0, name: '', price: 0 }; // 创建后清空表单
    });
  }
}
```

5.  **添加更新产品功能**：类似地，在你的 Angular 组件中实现更新产品的逻辑。




## Angular 组件：产品编辑

```typescript
import { Component } from '@angular/core';
import { ProductService } from './product.service';
import { Product } from './product.model';

@Component({
  selector: 'app-product-edit',
  templateUrl: './product-edit.component.html'
})
export class ProductEditComponent {
  selectedProduct: Product | null = null;

  constructor(private productService: ProductService) {}

  editProduct(product: Product) {
    this.selectedProduct = { ...product }; // 创建副本以避免直接修改
  }

  updateProduct() {
    if (this.selectedProduct) {
      this.productService.updateProduct(this.selectedProduct.id, this.selectedProduct).subscribe(() => {
        // 刷新产品列表或根据需要执行其他操作
        this.selectedProduct = null; // 更新后清除选择
      });
    }
  }
}
```

## 6. 添加删除产品功能

最后，在你的 Angular 组件中添加删除产品的功能。

```typescript
import { Component } from '@angular/core';
import { ProductService } from './product.service';
import { Product } from './product.model';

@Component({
  selector: 'app-product-list',
  templateUrl: './product-list.component.html'
})
export class ProductListComponent {
  products: Product[] = [];

  constructor(private productService: ProductService) {}

  deleteProduct(id: number) {
    this.productService.deleteProduct(id).subscribe(() => {
      // 刷新产品列表或根据需要执行其他操作
    });
  }
}
```

现在，让我们看看如何在 Angular 模板中使用这些功能。

## Angular 模板

### 1. 显示产品

使用 Angular 的数据绑定在组件的 HTML 模板 (`products.component.html`) 中显示产品。

```html
<h1>产品</h1>
<ul>
  <li *ngFor="let product of products">
    {{ product.id }} - {{ product.name }} - ${{ product.price }}
    <button (click)="editProduct(product)">编辑</button>
    <button (click)="deleteProduct(product.id)">删除</button>
  </li>
</ul>
```

### 2. 创建产品表单

创建一个表单来添加新产品 (`product-form.component.html`)。

```html
<h2>创建产品</h2>
<form (submit)="createProduct()">
  <input type="text" [(ngModel)]="newProduct.name" placeholder="产品名称" required>
  <input type="number" [(ngModel)]="newProduct.price" placeholder="价格" required>
  <button type="submit">添加产品</button>
</form>
```

### 3. 编辑产品表单

创建一个表单来编辑现有产品 (`product-edit.component.html`)。

```html
<h2>编辑产品</h2>
<form (submit)="updateProduct()">
  <input type="text" [(ngModel)]="selectedProduct.name" placeholder="产品名称" required>
  <input type="number" [(ngModel)]="selectedProduct.price" placeholder="价格" required>
  <button type="submit">更新产品</button>
</form>
```

有了这些模板和组件功能，你就拥有了一个完整的 Angular 应用程序，它可以与你的 ASP.NET Core MVC 后端交互，处理与产品相关的 HTTP 请求和响应。这种设置允许你在前端和后端之间无缝执行 CRUD 操作，提供全面的用户体验。

## 第 4 章：在 ASP.NET Core 8 中处理数据

### Entity Framework Core 8 数据库访问简介

Entity Framework Core 8 (`EF Core`) 是微软为 .NET 应用程序开发的一个现代对象关系映射器 (ORM) 框架。它提供了一种便捷高效的方式，使用面向对象编程技术与数据库交互，从而减少了数据访问任务所需的样板代码量。在本指南中，我们将介绍 `EF Core` 8，并演示如何在具有 Angular 14 前端的 ASP.NET Core 8 后端应用程序中使用它。

### 1. EF Core 8 入门

要在 ASP.NET Core 8 应用程序中使用 `EF Core` 8，你需要设置必要的依赖项并配置数据上下文。

#### 1.1 安装 EF Core 包

首先，在你的 ASP.NET Core 项目中安装 Entity Framework Core 包。打开 NuGet 包管理器控制台并运行以下命令：

```bash
Install-Package Microsoft.EntityFrameworkCore.SqlServer
```

此命令安装 `EF Core` SQL Server 提供程序，该程序允许 `EF Core` 与 SQL Server 数据库通信。

### 1.2 创建数据模型

通过创建表示数据库表的 C# 类来定义你的数据模型。例如，让我们创建一个 `Product` 类：

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
}
```

#### 1.3 创建 DbContext

`EF Core` 中的 `DbContext` 类表示数据库会话，并允许你查询和保存数据模型的实例。构建一个派生自 `DbContext` 的类：

```csharp
public class ApplicationDbContext : DbContext
{
    public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options)
        : base(options)
    {
    }

    public DbSet<Product> Products { get; set; }
}
```

#### 1.4 在 Startup 中配置 DbContext

在 `Startup.cs` 文件中，配置 `DbContext` 并指定数据库的连接字符串：

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddDbContext<ApplicationDbContext>(options =>
        options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));

    // 其他服务配置
}
```

确保你在 `appsettings.json` 文件中指定了连接字符串：

```json
"ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=YourDatabaseName;User=YourUsername;Password=YourPassword;"
}
```

### 2. 在控制器中使用 EF Core

现在你已经在 ASP.NET Core 应用程序中设置了 `EF Core`，你可以在控制器中使用它来执行数据库操作。

#### 2.1 将 DbContext 注入控制器

使用依赖注入将 `ApplicationDbContext` 注入到你的控制器中：

```csharp
public class ProductsController : ControllerBase
{
    private readonly ApplicationDbContext _context;

    public ProductsController(ApplicationDbContext context)
    {
        _context = context;
    }

    // 控制器操作
}
```

#### 2.2 执行 CRUD 操作

你现在可以使用 LINQ 查询和 `EF Core` 方法来执行 CRUD 操作。以下是一些示例：

- **检索产品：**

```csharp
[HttpGet]
public IActionResult GetProducts()
{
    var products = _context.Products.ToList();
    return Ok(products);
}
```

- **创建产品：**

```csharp
[HttpPost]
public IActionResult CreateProduct([FromBody] Product product)
{
    _context.Products.Add(product);
    _context.SaveChanges();
    return CreatedAtAction(nameof(GetProductById), new { id = product.Id }, product);
}
```

- **更新产品：**

```csharp
[HttpPut("{id}")]
public IActionResult UpdateProduct(int id, [FromBody] Product product)
{
    var existingProduct = _context.Products.FirstOrDefault(p => p.Id == id);
    if (existingProduct == null)
    {
        return NotFound();
    }

    existingProduct.Name = product.Name;
    existingProduct.Price = product.Price;
    _context.SaveChanges();
    return NoContent();
}
```

- **删除产品：**

```csharp
[HttpDelete("{id}")]
public IActionResult DeleteProduct(int id)
{
    var product = _context.Products.Find(id);
    if (product == null)
    {
        return NotFound();
    }

    _context.Products.Remove(product);
    _context.SaveChanges();
    return NoContent();
}
```

### 3. 将 EF Core 与 Angular 14 结合使用

要将 `EF Core` 与前端的 Angular 14 集成，你通常使用 HTTP 请求与你的 ASP.NET Core API 端点进行通信。

#### 3.1 Angular HTTP 服务

创建一个 Angular 服务来处理对你的 ASP.NET Core API 的 HTTP 请求：




# 建模数据实体与关系

建模数据实体与关系是设计数据库驱动应用程序的关键环节。在本指南中，我们将探讨如何在 ASP.NET Core 8 后端应用中使用 Entity Framework Core 8 来建模数据实体与关系，并将其与 Angular 14 前端集成。

## 1. 在 ASP.NET Core 8 中定义数据实体

数据实体代表映射到数据库表的对象。通过 Entity Framework Core，你可以将这些实体定义为 C#类，而 EF Core 会处理与底层数据库表的映射。

让我们以一个电子商务应用为例，其中包含`Product`和`Category`等实体。

### 1.1 创建数据模型类

在 ASP.NET Core 项目中定义你的数据模型类。例如：

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
    // Category 的导航属性
    public int CategoryId { get; set; }
    public Category Category { get; set; }
}

public class Category
{
    public int Id { get; set; }
    public string Name { get; set; }
    // Products 的导航属性
    public List<Product> Products { get; set; }
}
```

在此示例中，`Product`类有一个导航属性`Category`，表示产品与类别之间的关系。类似地，`Category`类有一个产品集合。

### 1.2 DbContext 配置

更新你的`DbContext`类以包含这些实体：

```csharp
public class ApplicationDbContext : DbContext
{
    public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options)
        : base(options)
    {
    }

    public DbSet<Product> Products { get; set; }
    public DbSet<Category> Categories { get; set; }

    protected override void OnModelCreating(ModelBuilder modelBuilder)
    {
        // 配置关系
        modelBuilder.Entity<Product>()
            .HasOne(p => p.Category)
            .WithMany(c => c.Products)
            .HasForeignKey(p => p.CategoryId);
    }
}
```

`OnModelCreating`方法用于配置实体之间的关系。

## 2. 与 Angular 14 前端集成

在 ASP.NET Core 后端建模好数据实体后，你可以将其与 Angular 14 前端集成，以获取和显示数据。

### 2.1 Angular 模型

在你的 Angular 项目中创建相应的 TypeScript 模型来表示数据实体。例如：

```typescript
export interface Product {
    id: number;
    name: string;
    price: number;
    categoryId: number;
    category: Category;
}

export interface Category {
    id: number;
    name: string;
    products: Product[];
}
```

### 2.2 Angular 服务

修改你的 Angular 服务，以便从 ASP.NET Core API 端点获取数据：

```typescript
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';
import { Product, Category } from './models';

@Injectable({
    providedIn: 'root'
})
export class DataService {
    private apiUrl = 'https://localhost:5001/api'; // API 端点 URL

    constructor(private http: HttpClient) { }

    getProducts(): Observable<Product[]> {
        return this.http.get<Product[]>(`${this.apiUrl}/products`);
    }

    getCategories(): Observable<Category[]> {
        return this.http.get<Category[]>(`${this.apiUrl}/categories`);
    }

    // 根据需要添加其他 CRUD 方法
}
```

### 2.3 Angular 组件使用

在你的 Angular 组件中，使用数据服务来获取和显示数据：

```typescript
import { Component, OnInit } from '@angular/core';
import { DataService } from './data.service';
import { Product, Category } from './models';

@Component({
    selector: 'app-product-list',
    templateUrl: './product-list.component.html'
})
export class ProductListComponent implements OnInit {
    products: Product[] = [];

    constructor(private dataService: DataService) { }

    ngOnInit(): void {
        this.dataService.getProducts().subscribe(products => {
            this.products = products;
        });
    }
}
```

### 2.4 在 Angular 模板中显示数据

使用 Angular 的数据绑定在组件模板中显示数据：

```html
<h1>Products</h1>
<ul>
    <li *ngFor="let product of products">
        {{ product.name }} - ${{ product.price }} - Category: {{ product.category.name }}
    </li>
</ul>
```

在 ASP.NET Core 8 中使用 Entity Framework Core 8 建模数据实体与关系，为数据库设计提供了一种结构化的方法。通过定义实体、配置关系并与 Angular 14 前端集成，你可以创建一个强大的应用程序，高效地管理和显示数据。后端与前端之间的这种关注点分离有助于构建可扩展且易于维护的 Web 应用程序。

# 使用 Web API 创建 CRUD 操作（创建、读取、更新、删除）

使用 Web API 创建 CRUD（创建、读取、更新、删除）操作是构建现代 Web 应用程序的基本方面。在本指南中，我们将演示如何使用 ASP.NET Core 8 实现后端 API 的 CRUD 操作，并将其与 Angular 14 前端集成。

## 1. 设置 ASP.NET Core Web API

首先，让我们设置一个 ASP.NET Core Web API 项目，以处理示例实体（如`Product`）的 CRUD 操作。

### 1.1 创建 ASP.NET Core Web API 项目

打开 Visual Studio 并创建一个新的 ASP.NET Core Web API 项目。

### 1.2 创建数据模型

为你的实体（例如`Product`）定义一个数据模型类：

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
}
```

### 1.3 创建控制器

添加一个控制器来处理`Product`实体的 CRUD 操作。右键单击`Controllers`文件夹，添加一个名为`ProductsController`的新控制器。

## 2. 在 Angular 组件中使用 API

将`ProductService`注入到你的 Angular 组件中，以获取和操作数据：

```typescript
import { Component, OnInit } from '@angular/core';
import { ProductService } from './product.service';
import { Product } from './product.model';

@Component({
    selector: 'app-product-list',
    templateUrl: './product-list.component.html'
})
export class ProductListComponent implements OnInit {
    products: Product[] = [];

    constructor(private productService: ProductService) {}

    ngOnInit(): void {
        this.productService.getProducts().subscribe(data => {
            this.products = data;
        });
    }
}
```

## 3. 在 Angular 模板中显示数据

使用 Angular 的数据绑定在组件模板中显示从 API 检索到的数据。

```html
<h1>Products</h1>
<ul>
    <li *ngFor="let product of products">
        {{ product.id }} - {{ product.name }} - ${{ product.price }}
    </li>
</ul>
```

Entity Framework Core 8 通过提供高级 ORM 框架，简化了 ASP.NET Core 8 应用程序中的数据库访问。按照上述步骤，你可以有效地将 EF Core 与你的 ASP.NET Core 后端和 Angular 14 前端集成，以执行 CRUD 操作并无缝管理数据。这种方法提高了 Web 应用程序开发的生产力和可维护性。



# ASP.NET Core 8 与 Angular 14 的 CRUD 操作与身份验证

## 1. ASP.NET Core Web API 控制器

```csharp
[ApiController]
[Route("api/[controller]")]
public class ProductsController : ControllerBase
{
    private static List<Product> _products = new List<Product>
    {
        new Product { Id = 1, Name = "Product 1", Price = 10.99m },
        new Product { Id = 2, Name = "Product 2", Price = 20.39m }
    };

    [HttpGet]
    public IActionResult GetProducts()
    {
        return Ok(_products);
    }

    [HttpGet("{id}")]
    public IActionResult GetProductById(int id)
    {
        var product = _products.FirstOrDefault(p => p.Id == id);
        if (product == null)
        {
            return NotFound();
        }
        return Ok(product);
    }

    [HttpPost]
    public IActionResult CreateProduct([FromBody] Product product)
    {
        product.Id = _products.Count + 1;
        _products.Add(product);
        return CreatedAtAction(nameof(GetProductById), new { id = product.Id }, product);
    }

    [HttpPut("{id}")]
    public IActionResult UpdateProduct(int id, [FromBody] Product product)
    {
        var existingProduct = _products.FirstOrDefault(p => p.Id == id);
        if (existingProduct == null)
        {
            return NotFound();
        }
        existingProduct.Name = product.Name;
        existingProduct.Price = product.Price;
        return NoContent();
    }

    [HttpDelete("{id}")]
    public IActionResult DeleteProduct(int id)
    {
        var existingProduct = _products.FirstOrDefault(p => p.Id == id);
        if (existingProduct == null)
        {
            return NotFound();
        }
        _products.Remove(existingProduct);
        return NoContent();
    }
}
```

在此控制器中：
- `GetProducts`: 检索所有产品。
- `GetProductById`: 通过 ID 检索产品。
- `CreateProduct`: 创建新产品。
- `UpdateProduct`: 更新现有产品。
- `DeleteProduct`: 通过 ID 删除产品。

## 2. 在 Angular 14 中使用 Web API

接下来，我们将 ASP.NET Core Web API 与 Angular 14 前端集成，以执行 CRUD 操作。

### 2.1 用于 API 调用的 Angular 服务

在你的 Angular 项目中创建一个服务，使用 Angular 的 `HttpClient` 模块处理 API 调用。

```typescript
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';
import { Product } from './product.model';

@Injectable({
  providedIn: 'root'
})
export class ProductService {
  private apiUrl = 'https://localhost:5001/api/products'; // API 端点 URL

  constructor(private http: HttpClient) { }

  getProducts(): Observable<Product[]> {
    return this.http.get<Product[]>(this.apiUrl);
  }

  getProductById(id: number): Observable<Product> {
    return this.http.get<Product>(`${this.apiUrl}/${id}`);
  }

  createProduct(product: Product): Observable<Product> {
    return this.http.post<Product>(this.apiUrl, product);
  }

  updateProduct(id: number, product: Product): Observable<Product> {
    return this.http.put<Product>(`${this.apiUrl}/${id}`, product);
  }

  deleteProduct(id: number): Observable<void> {
    return this.http.delete<void>(`${this.apiUrl}/${id}`);
  }
}
```

### 2.2 Angular 组件使用

在你的 Angular 组件中使用该服务与 Web API 交互。

```typescript
import { Component, OnInit } from '@angular/core';
import { ProductService } from './product.service';
import { Product } from './product.model';

@Component({
  selector: 'app-product-list',
  templateUrl: './product-list.component.html'
})
export class ProductListComponent implements OnInit {
  products: Product[] = [];

  constructor(private productService: ProductService) { }

  ngOnInit(): void {
    this.loadProducts();
  }

  loadProducts(): void {
    this.productService.getProducts().subscribe(products => {
      this.products = products;
    });
  }

  deleteProduct(id: number): void {
    if (confirm('Are you certain you wish to remove this product?')) {
      this.productService.deleteProduct(id).subscribe(() => {
        this.loadProducts(); // 删除后刷新产品列表
      });
    }
  }
}
```

### 2.3 用于显示的 Angular 模板

在你的组件模板中使用 Angular 的数据绑定来显示产品并执行 CRUD 操作。

```html
<h1>Product List</h1>
<ul>
  <li *ngFor="let product of products">
    {{ product.id }} - {{ product.name }} - ${{ product.price }}
    <button (click)="deleteProduct(product.id)">Delete</button>
  </li>
</ul>
```

## 3. 测试 CRUD 操作

现在你已经设置了后端 API 并将其与 Angular 前端集成，你可以测试 CRUD 操作：
- **创建操作**：填写表单以创建新产品，它应被添加到列表中。
- **读取操作**：查看产品列表，并点击单个产品以查看详细信息。
- **更新操作**：编辑产品详细信息并保存更改。
- **删除操作**：点击产品旁边的删除按钮以将其从列表中移除。

确保数据在每个操作中都能在 Angular 前端和 ASP.NET Core Web API 后端之间正确流动。

在 ASP.NET Core 8 和 Angular 14 中使用 Web API 实现 CRUD 操作，使你能够构建交互式和数据驱动的 Web 应用程序。通过遵循上述步骤，你可以在前端和后端之间无缝地创建、检索、更新和删除数据实体，提供完整的用户体验。这种方法有助于高效的数据管理，并提高应用程序的可扩展性和可维护性。

# 第 5 章：ASP.NET Core 8 中的身份验证与授权

## 使用 IdentityServer 实现用户身份验证

实现用户身份验证对于保护 Web 应用程序至关重要。在本指南中，我们将逐步介绍如何使用 IdentityServer 与 ASP.NET Core 8 后端 API 实现用户身份验证，并将其与 Angular 14 前端集成。

### 1. 在 ASP.NET Core 中设置 IdentityServer

IdentityServer 是一个流行的 .NET OpenID Connect 和 OAuth 2.0 框架。它为 Web 应用程序提供强大的身份验证和授权功能。

#### 1.1 安装 IdentityServer 包

首先，在你的 ASP.NET Core 项目中安装必要的 IdentityServer 包。打开 NuGet 包管理器控制台并运行以下命令：

```bash
Install-Package IdentityServer4
Install-Package IdentityServer4.AspNetIdentity
```

#### 1.2 配置 IdentityServer

在你的 ASP.NET Core 应用程序中设置 IdentityServer。修改你的 `Startup.cs` 文件以包含 IdentityServer 服务并配置身份验证。

```csharp
public void ConfigureServices(IServiceCollection services)
{
    // 其他服务配置
    services.AddIdentity<ApplicationUser, IdentityRole>()
        .AddEntityFrameworkStores<ApplicationDbContext>()
        .AddDefaultTokenProviders();

    services.AddIdentityServer()
        .AddApiAuthorization<ApplicationUser, ApplicationDbContext>();

    services.AddAuthentication()
        .AddIdentityServerJwt();

    // 其他配置
}

public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    // 其他应用配置
    app.UseRouting();
    app.UseAuthentication();
    app.UseAuthorization();
    app.UseEndpoints(endpoints =>
    {
        endpoints.MapControllers();
        endpoints.MapRazorPages();
        endpoints.MapIdentityServer();
    });
}
```

#### 1.3 创建用户模型和 DbContext

定义用户模型并更新你的 `DbContext` 以包含用户相关实体。

```csharp
public class ApplicationUser : IdentityUser
{
    // 如果需要，可添加额外的用户属性
}

public class ApplicationDbContext : IdentityDbContext<ApplicationUser>
{
    public ApplicationDbContext(DbContextOptions<ApplicationDbContext> options)
        : base(options)
    {
    }

    // 如果需要，可添加其他实体的 DbSet
}
```

#### 1.4 填充默认用户和角色（可选）

你可以在应用程序启动期间填充默认用户和角色，用于测试目的或初始设置。

#### 1.5 在控制器中启用身份验证

向需要身份验证的控制器或操作添加身份验证属性。

```csharp
[Authorize]
public class ProductsController : ControllerBase
{
    // 控制器操作
}
```

### 2. 在 Angular 14 中集成身份验证

在 ASP.NET Core 后端设置 IdentityServer 后，你将把身份验证与你的 Angular 14 前端集成。




# Angular 认证服务

在你的 Angular 项目中创建一个认证服务，使用 Angular 的 `HttpClient` 模块处理用户认证。

```typescript
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  private apiUrl = 'https://localhost:5001/api/auth'; // 认证 API 端点 URL

  constructor(private http: HttpClient) { }

  login(credentials: { username: string, password: string }): Observable<any> {
    return this.http.post<any>(`${this.apiUrl}/login`, credentials);
  }

  logout(): Observable<any> {
    return this.http.post<any>(`${this.apiUrl}/logout`, {});
  }
}
```

# Angular 登录组件

创建一个登录组件，用户可以在其中输入凭据进行认证。

```typescript
import { Component } from '@angular/core';
import { AuthService } from './auth.service';

@Component({
  selector: 'app-login',
  templateUrl: './login.component.html'
})
export class LoginComponent {
  credentials = { username: '', password: '' };

  constructor(private authService: AuthService) { }

  login(): void {
    this.authService.login(this.credentials).subscribe(response => {
      // 处理登录成功（例如，存储令牌，重定向）
    }, error => {
      // 处理登录错误
    });
  }
}
```

# Angular 登录模板

在你的组件模板（`login.component.html`）中创建一个登录表单。

```html
<h1>登录</h1>
<form (submit)="login()">
  <input type="text" [(ngModel)]="credentials.username" placeholder="用户名" required>
  <input type="password" [(ngModel)]="credentials.password" placeholder="密码" required>
  <button type="submit">登录</button>
</form>
```

# 测试认证流程

现在你已经设置了认证，可以测试认证流程：

- **登录**：在登录表单中输入有效的凭据并提交。后端 API 验证凭据并颁发认证令牌（例如 JWT）。
- **授权**：已认证的用户可以通过在请求头中包含认证令牌来访问受保护的路由或 API 端点。
- **登出**：在你的 UI 中提供一个登出选项，以使认证令牌失效并让用户登出。

确保在你的 Angular 应用程序中处理令牌存储（例如本地存储）、令牌过期和令牌续期，以实现无缝的认证体验。

在 ASP.NET Core 8 中使用 IdentityServer 实现用户认证，并将其与 Angular 14 前端集成，为 Web 应用程序提供了强大的认证和授权机制。通过遵循上述步骤，你可以保护应用程序的端点并高效地认证用户，从而增强整体安全性和用户体验。

# 使用 JWT（JSON Web 令牌）保护 Web API

确保 Web API 的安全性对于保护敏感数据并保证只有授权用户才能访问特定资源至关重要。JSON Web 令牌（JWT）通过生成携带用户信息并在服务器端进行验证的令牌，为保护 API 提供了一种可靠的机制。在本指南中，我们将探讨如何使用 ASP.NET Core 8 作为后端 API，并将其与 Angular 14 前端集成，来使用 JWT 保护 Web API。

## 在 ASP.NET Core 中设置 JWT 认证

ASP.NET Core 通过中间件和服务提供了对 JWT 认证的内置支持。

### 1. 安装 JWT 包

首先，在你的 ASP.NET Core 项目中安装必要的 JWT 包。打开 NuGet 包管理器控制台并运行以下命令：

```bash
Install-Package Microsoft.AspNetCore.Authentication.JwtBearer
```

### 2. 配置 JWT 认证

在你的 `Startup.cs` 文件中配置 JWT 认证。

```csharp
public void ConfigureServices(IServiceCollection services)
{
    // 其他服务配置
    services.AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
        .AddJwtBearer(options =>
        {
            options.TokenValidationParameters = new TokenValidationParameters
            {
                ValidateIssuer = true,
                ValidateAudience = true,
                ValidateLifetime = true,
                ValidateIssuerSigningKey = true,
                ValidIssuer = Configuration["Jwt:Issuer"],
                ValidAudience = Configuration["Jwt:Audience"],
                IssuerSigningKey = new SymmetricSecurityKey(Encoding.UTF8.GetBytes(Configuration["Jwt:SecretKey"]))
            };
        });
    // 其他配置
}

public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    // 其他应用配置
    app.UseAuthentication();
    app.UseAuthorization();
    // 其他配置
}
```

确保你已在 `appsettings.json` 文件中配置了 JWT 参数，如颁发者、受众和密钥。

### 3. 生成 JWT 令牌

创建一个服务或控制器方法，在用户成功认证时生成 JWT 令牌。

```csharp
public class AuthController : ControllerBase
{
    private readonly IConfiguration _configuration;

    public AuthController(IConfiguration configuration)
    {
        _configuration = configuration;
    }

    [HttpPost("login")]
    public IActionResult Login(LoginModel model)
    {
        // 验证用户凭据（例如，从数据库）
        var isValid = ...; // 你的验证逻辑
        if (!isValid)
        {
            return Unauthorized();
        }

        var token = GenerateJwtToken();
        return Ok(new { token });
    }

    private string GenerateJwtToken()
    {
        var tokenHandler = new JwtSecurityTokenHandler();
        var key = Encoding.ASCII.GetBytes(_configuration["Jwt:SecretKey"]);

        var tokenDescriptor = new SecurityTokenDescriptor
        {
            Subject = new ClaimsIdentity(new[]
            {
                new Claim(ClaimTypes.Name, "username"),
                // 根据需要添加更多声明
            }),
            Expires = DateTime.UtcNow.AddDays(1), // 令牌过期时间
            SigningCredentials = new SigningCredentials(new SymmetricSecurityKey(key), SecurityAlgorithms.HmacSha256Signature)
        };

        var token = tokenHandler.CreateToken(tokenDescriptor);
        return tokenHandler.WriteToken(token);
    }
}
```

## 在 Angular 14 中集成 JWT 认证

在 ASP.NET Core 后端设置好 JWT 认证后，你将把它与你的 Angular 14 前端集成。

### 1. Angular 认证服务

修改你在 Angular 中的认证服务，以处理 JWT 令牌存储和带有 JWT 头的 HTTP 请求。

```typescript
import { Injectable } from '@angular/core';
import { HttpClient, HttpHeaders } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  private apiUrl = 'https://localhost:5001/api/auth'; // 认证 API 端点 URL
  private authToken: string | null = null;

  constructor(private http: HttpClient) { }

  login(credentials: { username: string, password: string }): Observable<any> {
    return this.http.post<any>(`${this.apiUrl}/login`, credentials);
  }

  setAuthToken(token: string): void {
    this.authToken = token;
    // 将令牌存储在本地存储或会话存储中
  }

  getAuthToken(): string | null {
    // 从本地存储或会话存储中检索令牌
    return this.authToken;
  }

  logout(): Observable<any> {
    // 从存储中清除令牌
    this.authToken = null;
    return this.http.post<any>(`${this.apiUrl}/logout`, {});
  }

  // 添加方法以在 HTTP 头中包含 JWT 令牌
  getHeaders(): HttpHeaders {
    const token = this.getAuthToken();
    if (token) {
      return new HttpHeaders({
        'Authorization': `Bearer ${token}`
      });
    }
    return new HttpHeaders();
  }
}
```

### 2. 在 API 请求中使用 JWT

更新你的 Angular 服务方法，以便在需要认证的请求的 HTTP 头中包含 JWT 令牌。




```typescript
import { Injectable } from '@angular/core';
import { HttpClient, HttpHeaders } from '@angular/common/http';
import { Observable } from 'rxjs';
import { AuthService } from './auth.service';

@Injectable({
  providedIn: 'root'
})
export class ProductService {
  private apiUrl = 'https://localhost:5001/api/products'; // API 端点 URL

  constructor(private http: HttpClient, private authService: AuthService) { }

  getProducts(): Observable<Product[]> {
    const headers = this.authService.getHeaders();
    return this.http.get<Product[]>(this.apiUrl, { headers });
  }

  // 其他带有 JWT 头的 CRUD 方法
}
```

## 测试 JWT 认证

既然 JWT 认证已经实现，你可以测试认证流程：

- **登录**：使用 Angular 应用中的登录表单将凭据发送到后端。认证成功后，后端会颁发一个 JWT 令牌。
- **API 请求**：在 API 请求的 HTTP 头中包含 JWT 令牌。后端会验证令牌并允许访问受保护的资源。
- **登出**：在用户界面中提供登出选项，以清除存储中的 JWT 令牌并让用户登出。

为 ASP.NET Core 8 和 Angular 14 实现 JWT 认证以保护 Web API，提供了一种强大的用户认证和授权机制，确保只有授权用户才能访问受保护的资源。通过遵循上述步骤，你已经使用 JWT 令牌在 ASP.NET Core 后端和 Angular 前端之间建立了一个安全的认证流程。

在使用 JWT 认证时，以下是一些需要牢记的额外考虑因素和最佳实践：

1.  **令牌过期**：为 JWT 令牌设置适当的过期时间，以最小化安全风险。通常，令牌在短时间内（例如 15 分钟到几小时）过期，并需要刷新。
2.  **令牌刷新**：实现令牌刷新机制，以便在不要求用户重新输入凭据的情况下生成新的 JWT 令牌。当令牌即将过期时，前端可以使用刷新令牌（如果可用）来请求新令牌。
3.  **安全存储**：在客户端安全地存储 JWT 令牌。使用浏览器存储机制，如本地存储或会话存储，并在处理 JWT 令牌时避免将敏感信息存储在 Cookie 中。
4.  **HTTPS**：始终使用 HTTPS 来加密客户端和服务器之间传输的数据，包括 JWT 令牌。这有助于防止令牌被恶意方截获。
5.  **授权**：在 ASP.NET Core 后端实现基于角色或基于声明的授权，以根据用户角色或 JWT 令牌中的特定声明来控制对 API 不同部分的访问。
6.  **错误处理**：在服务器端优雅地处理 JWT 令牌验证错误，并向客户端提供适当的错误响应。这有助于调试和改善用户体验。
7.  **令牌撤销**：考虑实现令牌撤销机制，用于在令牌过期时间之前需要撤销用户访问权限的场景（例如，登出、账户停用）。

通过整合这些最佳实践并持续监控和更新你的认证机制，你可以为你的 Web 应用维护一个安全可靠的认证系统。

总的来说，JWT 认证为保护 Web API 提供了一种可扩展且无状态的方法，使其成为现代 Web 开发场景的热门选择。当与 ASP.NET Core 和 Angular 结合使用时，你可以创建强大、安全且用户友好的应用程序，满足现代安全标准。

## 基于角色的授权以实现安全访问控制

基于角色的授权是 Web 应用程序访问控制的一个关键方面，它允许你根据分配给用户的角色来限制对某些资源的访问。在本指南中，我们将探讨如何使用 ASP.NET Core 8 为后端 API 实现基于角色的授权，并将其与 Angular 14 前端集成。

### 1. 在 ASP.NET Core 中设置基于角色的授权

ASP.NET Core 使用属性和策略提供了灵活且强大的基于角色的授权机制。

1.  **定义角色**：首先定义你希望用于授权的角色。这些角色可以代表应用程序中不同的访问级别。

```csharp
public static class Roles
{
    public const string Admin = "Admin";
    public const string User = "User";
}
```

2.  **配置授权策略**：在你的 `Startup.cs` 文件中，基于角色配置授权策略。

```csharp
public void ConfigureServices(IServiceCollection services)
{
    // 其他服务配置
    services.AddAuthorization(options =>
    {
        options.AddPolicy(Roles.Admin, policy => policy.RequireRole(Roles.Admin));
        options.AddPolicy(Roles.User, policy => policy.RequireRole(Roles.User));
    });
    // 其他配置
}
```

3.  **应用基于角色的授权**：使用授权属性将基于角色的授权应用于你的控制器或操作。

```csharp
[Authorize(Roles = Roles.Admin)]
public class AdminController : ControllerBase
{
    // 仅对拥有 Admin 角色的用户可访问的操作
}

[Authorize(Roles = Roles.User)]
public class UserController : ControllerBase
{
    // 仅对拥有 User 角色的用户可访问的操作
}
```

### 2. 在 Angular 14 中集成基于角色的授权

在 ASP.NET Core 后端设置好基于角色的授权后，你将把它与你的 Angular 14 前端集成。

1.  **JWT 令牌中的用户角色**：修改你的 JWT 令牌生成，以在令牌负载中包含用户角色作为声明。

```csharp
private string GenerateJwtToken(ApplicationUser user)
{
    var tokenHandler = new JwtSecurityTokenHandler();
    var key = Encoding.ASCII.GetBytes(Configuration["Jwt:SecretKey"]);
    var tokenDescriptor = new SecurityTokenDescriptor
    {
        Subject = new ClaimsIdentity(new[]
        {
            new Claim(ClaimTypes.Name, user.UserName),
            new Claim(ClaimTypes.Role, Roles.Admin), // 示例：根据用户角色分配角色
            // 根据需要添加更多声明
        }),
        Expires = DateTime.UtcNow.AddDays(1), // 令牌过期时间
        SigningCredentials = new SigningCredentials(new SymmetricSecurityKey(key), SecurityAlgorithms.HmacSha256Signature)
    };
    var token = tokenHandler.CreateToken(tokenDescriptor);
    return tokenHandler.WriteToken(token);
}
```

2.  **Angular 授权服务**：在 Angular 中创建一个授权服务，以检查用户角色并控制对组件或路由的访问。

```typescript
import { Injectable } from '@angular/core';
import { AuthService } from './auth.service';

@Injectable({
  providedIn: 'root'
})
export class AuthorizationService {
  constructor(private authService: AuthService) { }

  isAdmin(): boolean {
    const userRoles = this.authService.getUserRoles();
    return userRoles.includes('Admin');
  }

  isUser(): boolean {
    const userRoles = this.authService.getUserRoles();
    return userRoles.includes('User');
  }
}
```

3.  **Angular 路由守卫**：使用 Angular 路由守卫根据用户角色限制对路由的访问。

```typescript
import { Injectable } from '@angular/core';
import { CanActivate, Router } from '@angular/router';
import { AuthService } from './auth.service';
import { AuthorizationService } from './authorization.service';

@Injectable({
  providedIn: 'root'
})
export class AdminGuard implements CanActivate {
  constructor(private authService: AuthService, private authorizationService: AuthorizationService, private router: Router) { }

  canActivate(): boolean {
    if (this.authService.isLoggedIn() && this.authorizationService.isAdmin()) {
      return true;
    } else {
      this.router.navigate(['/unauthorized']); // 重定向到未授权页面或根据需要处理
      return false;
    }
  }
}
```

### 3. 测试基于角色的授权

实现基于角色的授权后，你可以根据用户角色测试访问控制：



● 管理员访问：以具有管理员角色的用户身份登录，并访问受 `AdminGuard` 保护的路由或组件。

● 用户访问：以具有用户角色的用户身份登录，并访问受 `UserGuard` 保护的路由或组件。

● 未授权访问：尝试在没有相应角色的情况下访问路由或组件，并验证是否重定向到未授权页面或进行了适当处理。

基于角色的授权通过确保只有具有特定角色的授权用户才能访问应用程序内的受保护资源来增强安全性。通过在 ASP.NET Core 8 后端 API 中实现基于角色的授权，并使用路由守卫和授权服务将其与 Angular 14 前端集成，你可以有效地实施访问控制。这种方法有助于根据用户角色和权限维护数据的机密性、完整性以及整体应用程序安全性。

## 第 6 章：部署 ASP.NET Core 8 Web API

### 为生产环境发布 ASP.NET Core 应用程序

为生产环境发布 ASP.NET Core 应用程序涉及为部署准备应用程序、配置生产设置以及将其部署到托管环境。以下是关于如何为生产环境发布 ASP.NET Core 8 应用程序（包括 Angular 14 前端集成）的指南。

1.  **为生产环境准备 ASP.NET Core 应用程序：** 在发布之前，确保你的 ASP.NET Core 应用程序已针对生产使用进行了优化。
    1.  **优化代码和资源：**
        *   压缩和打包 JavaScript 和 CSS 文件以减少加载时间。
        *   为静态文件启用压缩以减少带宽使用。
        *   移除不必要的日志记录和调试信息。
    2.  **配置生产环境：** 使用生产特定的设置（如数据库连接字符串、日志级别和安全配置）更新你的 `appsettings.json` 或 `appsettings.Production.json` 文件。
    3.  **设置环境变量：** 为 API 密钥或连接字符串等敏感信息配置环境变量。在代码中使用 `IConfiguration` 或 `IOptions` 模式访问这些变量。

2.  **发布 ASP.NET Core 应用程序：** 你可以使用 Visual Studio 或命令行发布 ASP.NET Core 应用程序。以下是使用命令行的方法：
    1.  **打开命令提示符：** 打开命令提示符或终端窗口。
    2.  **导航到项目目录：** 更改目录到你的 ASP.NET Core 项目文件夹。
        ```bash
        cd path/to/your/project
        ```
    3.  **发布命令：** 运行 `dotnet publish` 命令来发布你的应用程序。
        ```bash
        dotnet publish -c Release
        ```
        如果你有用于生产的自定义配置，请将 `-c Release` 替换为 `-c Production`。
    4.  **输出目录：** 成功发布后，你的应用程序文件将被放置在指定的输出目录中（通常是 `bin/Release/netcoreappX.X/publish`）。

3.  **部署 ASP.NET Core 应用程序：** 发布后，将你的 ASP.NET Core 应用程序部署到托管环境。你可以选择各种托管选项，如 IIS、Azure App Service、Docker 容器或 AWS 或 Google Cloud 等云平台。
    1.  **部署到 IIS：**
        *   在服务器上安装 .NET Core Hosting Bundle。
        *   在 IIS 中创建一个新的站点或应用程序池，并将其配置为指向已发布的文件夹。
        *   设置适当的权限和绑定（HTTP 或 HTTPS）。
    2.  **部署到 Azure App Service：**
        *   为你的应用程序创建一个 Azure App Service（Web 应用）。
        *   使用 Azure DevOps、Visual Studio 发布或 FTP 将你发布的文件部署到 App Service。
    3.  **使用 Docker 部署：**
        *   使用 `Dockerfile` 将你的 ASP.NET Core 应用程序容器化。
        *   构建一个 Docker 镜像并将其上传到容器注册表。
        *   将 Docker 镜像部署到容器运行时环境，如 Docker Swarm 或 Kubernetes。

4.  **集成 Angular 14 前端：** 如果你的 ASP.NET Core 应用程序包含 Angular 14 前端，请在发布和部署过程中将其集成。
    1.  **Angular 构建：** 在发布 ASP.NET Core 应用程序之前，为生产环境构建你的 Angular 前端。
        ```bash
        ng build --prod
        ```
        此命令会在你的 Angular 项目的 `dist` 文件夹中生成优化的、可用于生产的文件。
    2.  **与 Angular 一起发布：** 将 Angular 生产文件（`dist` 文件夹）包含在你的 ASP.NET Core 应用程序的发布输出中。
        ```bash
        dotnet publish -c Release --output path/to/publish --source path/to/angular/dist
        ```
    3.  **部署组合应用程序：** 将组合的 ASP.NET Core 和 Angular 应用程序部署到你选择的托管环境，确保为后端 API 端点和前端路由进行正确的配置和路由。

5.  **监控和维护：** 部署后，监控你的应用程序的性能、错误和安全问题。设置日志记录和监控工具以跟踪应用程序健康状况和用户交互。定期更新依赖项、应用安全补丁并执行维护任务，以确保生产环境平稳且安全。

通过遵循这些步骤，你可以成功地为生产环境发布和部署集成了 Angular 14 前端的 ASP.NET Core 8 应用程序，为用户提供可靠且可扩展的 Web 应用程序体验。

### 在 Azure App Service 或云平台上托管

在 Azure App Service 或 AWS 或 Google Cloud 等其他云平台上托管集成了 Angular 14 前端的 ASP.NET Core 8 应用程序，可提供可扩展性、可靠性和部署的便捷性。在本指南中，我们将重点介绍在 Azure App Service 上的托管，包括部署和配置步骤。

1.  **为 Azure App Service 准备你的应用程序：** 在部署到 Azure App Service 之前，确保你的应用程序已准备好进行生产部署。
    *   使用 `ng build --prod` 为生产环境构建你的 Angular 前端。
    *   使用 `dotnet publish -c Release` 发布你的 ASP.NET Core 后端。
2.  **配置更新：** 使用生产设置（包括连接字符串、API 端点和安全配置）更新你的应用程序配置文件（`appsettings.json`、环境变量等）。
3.  **准备部署：** 确保你拥有必要的部署脚本或配置，以便顺利进行部署过程。

2.  **部署到 Azure App Service：** 按照以下步骤将集成了 Angular 14 前端的 ASP.NET Core 8 应用程序部署到 Azure App Service。
    1.  **创建 Azure App Service：**
        *   登录到 Azure 门户 (`portal.azure.com`)。
        *   导航到 App Services 并单击“创建 App Service”。
        *   配置所需的设置，例如资源组、应用名称、运行时堆栈（.NET Core）和区域。
    2.  **部署选项：** Azure App Service 支持多种部署方法，包括：
        *   **Azure DevOps：** 使用 Azure DevOps 设置 CI/CD 管道以自动化构建和部署。
        *   **Visual Studio 发布：** 直接从 Visual Studio 发布到 Azure App Service。
        *   **FTP 部署：** 通过 FTP 手动上传你发布的文件。
    3.  **使用 Visual Studio 部署：** 如果你选择从 Visual Studio 部署。
        *   右键单击你的 ASP.NET Core 项目并选择“发布”。
        *   选择 Azure App Service 作为目标，并按照向导选择你的 Azure 订阅和 App Service 实例。
        *   直接从 Visual Studio 发布应用程序。
    4.  **使用 Azure DevOps 部署：** 在 Azure DevOps 中设置 CI/CD 管道以自动化部署：
        *   创建一个构建管道来构建和打包你的 ASP.NET Core 和 Angular 应用程序。
        *   创建一个发布管道将打包的应用程序部署到 Azure App Service。
        *   配置触发器以在代码更改或手动批准时自动部署。

3.  **配置和扩展：** 部署后，配置你的 Azure App Service 并考虑扩展选项，以实现最佳性能和可扩展性。
    1.  **配置设置：**




● 在 Azure App Service 中配置环境变量和应用程序设置，以进行特定于生产环境的配置。

● 使用 Azure Application Insights 或其他监控工具设置日志记录和监控。

2\. 扩展选项：

● 通过选择更高层级的计划以获得更多资源（CPU、内存等），垂直扩展（增加规模）你的 App Service。

● 通过添加更多实例（虚拟机）或根据需求使用自动扩展，水平扩展（增加实例）。

4\. 安全访问和网络：确保安全访问，并根据应用程序需要配置网络设置。

1\. SSL/TLS 证书：

● 使用 SSL/TLS 证书保护你的应用程序，以启用 HTTPS。

● 在 Azure App Service 中上传和配置 SSL 证书，以实现安全通信。

2\. 防火墙和网络：

● 在 Azure App Service 中配置防火墙规则和 IP 限制以控制访问。

● 设置网络配置，例如虚拟网络（VNET）和专用终结点，以实现安全连接。

5\. 持续监控和维护：部署后，在 Azure App Service 上监控你的应用程序的性能、可用性和安全性。

1\. 监控工具：

● 使用 Azure Application Insights 或其他监控工具来监控应用程序的健康状况、性能指标和用户交互。

● 为关键事件、性能阈值和安全事件设置警报。

2\. 定期更新和维护：

● 定期更新应用程序中使用的依赖项、库和框架。

● 应用安全补丁和更新，以确保环境的安全性和最新状态。

遵循这些步骤和最佳实践，你就可以成功地将带有 Angular 14 前端的 ASP.NET Core 8 应用程序托管在 Azure App Service 或其他云平台上。Azure App Service 提供了一个具有可扩展性、安全性和监控功能的托管托管环境，使其成为托管现代 Web 应用程序的合适选择。

## 监控和调试已部署的应用程序

监控和调试是维护和优化已部署应用程序的关键方面。在本指南中，我们将探讨如何使用适用于后端和前端组件的工具和技术，监控和调试带有集成 Angular 14 前端的已部署 ASP.NET Core 8 应用程序。

### 1\. 监控 ASP.NET Core 应用程序

监控 ASP.NET Core 应用程序涉及跟踪性能指标、日志记录和错误处理，以确保应用程序在生产环境中平稳高效地运行。

1\. 配置日志记录：在你的 ASP.NET Core 应用程序中，配置日志记录以捕获重要事件和错误。使用 Serilog 等日志提供程序或内置的日志记录功能。

```csharp
public class Startup
{
    public void ConfigureLogging(IApplicationBuilder app, IWebHostEnvironment env)
    {
        // Configure logging
        ILoggerFactory loggerFactory = LoggerFactory.Create(builder =>
        {
            builder.AddConsole();
            builder.AddDebug();
            // Add other logging providers as needed
        });

        app.UseSerilogRequestLogging(); // Serilog request logging middleware

        ILogger logger = loggerFactory.CreateLogger<Startup>();
        logger.LogInformation("Application started.");
    }
}
```

2\. 集成 Application Insights：Azure Application Insights 为 ASP.NET Core 应用程序提供了强大的监控功能。

● 将 Application Insights SDK 集成到你的项目中。

```bash
dotnet add package Microsoft.ApplicationInsights.AspNetCore
```

● 在 `Startup.cs` 中配置 Application Insights：

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddApplicationInsightsTelemetry(Configuration["ApplicationInsights:InstrumentationKey"]);
    // Other configurations
}
```

3\. 监控性能指标：使用 Application Insights 或其他监控工具来跟踪性能指标，例如响应时间、请求速率、CPU 使用率、内存消耗等。

4\. 设置警报：根据关键事件或性能阈值配置警报，以便在需要立即关注的问题发生时收到通知。

### 2\. 调试 ASP.NET Core 应用程序

调试已部署的 ASP.NET Core 应用程序有助于识别和修复代码库中的问题，确保平稳运行和用户体验。

1\. 远程调试：Azure App Service 和其他托管平台支持远程调试，允许你将调试器附加到已部署的应用程序以进行实时调试。

2\. 日志记录和错误处理：增强 ASP.NET Core 应用程序中的日志记录和错误处理，以捕获生产环境中遇到的异常和错误的详细信息。

```csharp
public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    // Configure error handling
    if (env.IsDevelopment())
    {
        app.UseDeveloperExceptionPage();
    }
    else
    {
        app.UseExceptionHandler("/Home/Error");
        app.UseHsts();
    }
}
```

3\. 健康检查：在你的 ASP.NET Core 应用程序中实现健康检查，以监控关键组件（例如数据库连接、外部服务）的健康状况。

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddHealthChecks();
    // Other configurations
}

public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    app.UseHealthChecks("/health");
    // Other configurations
}
```

### 3\. 监控和调试 Angular 14 应用程序

监控和调试 Angular 14 应用程序侧重于跟踪客户端错误、性能问题和用户交互。

1\. Angular CLI 调试：在开发过程中使用 Angular CLI 工具调试 Angular 应用程序：

1.  运行带有 `--source-map` 选项的 `ng serve` 以生成用于调试的源映射

2.  使用浏览器开发者工具（Chrome DevTools、Firefox Developer Tools）调试 TypeScript 代码、检查网络请求和分析性能。

2\. 错误处理和日志记录：使用 Angular 的错误处理机制和日志记录服务（例如 ngxLogger）在你的 Angular 应用程序中实现错误处理和日志记录。

3\. 性能监控：使用 Google Analytics、New Relic 或自定义监控解决方案等工具来跟踪你的 Angular 应用程序中的用户交互、页面加载时间和性能指标。

### 4\. 组合监控和调试

要监控和调试整个应用程序栈（ASP.NET Core 后端和 Angular 前端），请考虑以下策略：

1\. 端到端跟踪：使用分布式跟踪工具，例如 Application Insights、OpenTelemetry 或 Jaeger，来跟踪跨后端和前端组件的请求，捕获端到端事务详情。

2\. 与监控平台集成：将你的 ASP.NET Core 应用程序的监控数据（日志、指标）与监控平台集成，以实现集中监控和警报。

3\. 跨域调试：在浏览器开发者工具中启用跨域调试，以调试 API 调用和前端与后端的交互。

4\. 实时调试：利用 Azure DevOps、Visual Studio 或其他集成开发环境提供的实时调试功能，在生产环境中进行实时调试会话。

### 5\. 持续改进和优化

定期审查监控数据、日志和调试见解，以识别需要改进、优化和错误修复的领域。实施反馈循环和敏捷实践，以迭代方式增强应用程序的性能、可靠性和用户体验。

通过为 ASP.NET Core 8 和 Angular 14 组件实施强大的监控和调试实践，你可以维护一个健康高效的应用程序环境，有效地排除故障，并为用户提供高质量的用户体验。

## 第 7 章：深入探索 Angular 14 以构建动态前端




Angular 14 是一个强大的 JavaScript 框架，用于构建具有丰富用户界面的动态 Web 应用程序。Angular 开发的核心是组件和模板，它们定义了应用程序 UI 的结构和行为。在本指南中，我们将探讨 Angular 组件和模板，包括如何有效地将它们与 ASP.NET Core 8 后端结合使用。

## 1. 理解 Angular 组件

Angular 应用程序使用组件构建，这些组件是可重用且封装的构建块，定义了应用程序的 UI 元素。每个组件由三个主要部分组成：组件类、HTML 模板和组件特定的样式。

## 2. 创建 Angular 组件

要创建一个新的 Angular 组件，你可以使用 Angular CLI（命令行界面）或手动创建文件。以下是使用 Angular CLI 创建新组件的方法：

```bash
ng generate component my-component
```

此命令会生成新组件所需的文件，包括 TypeScript 类、HTML 模板、CSS 样式，并更新应用模块以声明新组件。

## 3. Angular 组件的剖析

让我们更仔细地看看 Angular 组件的不同部分：

### 组件类 (TypeScript)

包含组件的逻辑和数据。此类使用 `@Component` 装饰器进行装饰，以定义选择器、模板、样式等元数据。

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-my-component',
  templateUrl: './my-component.component.html',
  styleUrls: ['./my-component.component.css']
})
export class MyComponent {
  // 组件逻辑和数据属性
}
```

### HTML 模板

定义组件 UI 的结构和布局。你可以使用 Angular 模板语法来绑定数据、处理事件和显示动态内容。

```html
<div>
  <h1>欢迎来到 MyComponent！</h1>
  <p>{{ message }}</p>
  <button (click)="onClick()">点击我</button>
</div>
```

### 组件样式

可选的、特定于组件的 CSS 样式。样式可以内联定义，在单独的 CSS 文件中定义，或使用 Sass 或 Less 等 CSS 预处理器定义。

```css
div {
  background-color: #f0f0f0;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
```

## 4. 使用 Angular 组件和模板

创建组件后，你可以在其他组件中或在应用程序的路由配置中使用它。

### 在模板中使用组件

要在另一个组件的模板中使用一个组件，只需引用其选择器标签。

```html
<app-my-component></app-my-component>
```

### 向组件传递数据

你可以使用输入属性向组件传递数据。在组件类中定义输入属性，并在父组件的模板中绑定它们。

```typescript
import { Component, Input } from '@angular/core';

@Component({
  selector: 'app-my-component',
  templateUrl: './my-component.component.html',
  styleUrls: ['./my-component.component.css']
})
export class MyComponent {
  @Input() message: string;
}
```

```html
<app-my-component [message]="'来自父组件的问候'"></app-my-component>
```

### 处理事件

组件可以发出事件，以通知父组件有关更改或用户交互的信息。使用 `EventEmitter` 定义自定义事件，并从组件类中发出它们。

```typescript
import { Component, Output, EventEmitter } from '@angular/core';

@Component({
  selector: 'app-my-component',
  templateUrl: './my-component.component.html',
  styleUrls: ['./my-component.component.css']
})
export class MyComponent {
  @Output() buttonClick: EventEmitter<void> = new EventEmitter<void>();

  onClick(): void {
    this.buttonClick.emit();
  }
}
```

```html
<app-my-component (buttonClick)="handleButtonClick()"></app-my-component>
```

Angular 组件和模板是创建动态和交互式 Web 应用程序的基本构建块。通过掌握熟练创建和利用组件的艺术，你可以开发出模块化、易于维护且可扩展的 Angular 14 应用程序。结合 ASP.NET Core 8 后端，Angular 组件为现代 Web 开发项目提供了强大的前端架构，实现了应用程序前端和后端组件之间的无缝集成。

## 理解 Angular 应用程序中的数据绑定和用户交互

理解数据绑定和用户交互在 Angular 开发中至关重要，因为它们能够实现动态和交互式的用户界面。在本指南中，我们将深入探讨 Angular 14 应用程序中的数据绑定类型、事件处理和用户交互，并提供基于 ASP.NET Core 8 后端集成的示例。

### 1. Angular 中的数据绑定

Angular 中的数据绑定允许你在 UI（用户界面）和应用程序的数据模型之间建立连接。Angular 支持多种数据绑定类型：

1.  插值 (`{{ }}`)：从组件到视图（模板）的单向数据绑定。
2.  属性绑定 (`[property]="value"`)：从组件到视图的单向数据绑定，用于元素属性。
3.  事件绑定 (`(event)="handler()"`)：绑定到 DOM 事件以处理用户交互。
4.  双向绑定 (`[(ngModel)]="property"`)：用于表单元素的双向数据绑定，结合了属性绑定和事件绑定。

### 2. 数据绑定的类型

让我们通过示例来探讨每种数据绑定类型：

#### 插值

插值用于在视图（模板）中显示组件数据。

```typescript
// 组件类
export class AppComponent {
  greeting: string = '你好，Angular！';
}
```

```html
<!-- 模板 -->
<h1>{{ greeting }}</h1>
```

#### 属性绑定

属性绑定用于根据组件数据动态设置元素属性。

```typescript
// 组件类
export class AppComponent {
  imageUrl: string = 'path/to/image.jpg';
}
```

```html
<!-- 模板 -->
<img [src]="imageUrl" alt="图片">
```

#### 事件绑定

事件绑定允许你处理由用户交互触发的 DOM 事件。

```typescript
// 组件类
export class AppComponent {
  handleClick(): void {
    alert('按钮被点击！');
  }
}
```

```html
<!-- 模板 -->
<button (click)="handleClick()">点击我</button>
```

#### 双向绑定（表单）

双向绑定通常用于表单，以同步输入字段和组件属性之间的数据。

```typescript
// 组件类
export class AppComponent {
  username: string = '';
}
```

```html
<!-- 模板 -->
<input type="text" [(ngModel)]="username">
<p>欢迎，{{ username }}！</p>
```

### 3. 处理用户交互

Angular 提供了处理用户交互的机制，例如点击、输入更改和表单提交。

#### 事件处理

使用事件绑定在组件类中处理用户触发的事件。

```typescript
// 组件类
export class AppComponent {
  handleClick(): void {
    alert('按钮被点击！');
  }
}
```

```html
<!-- 模板 -->
<button (click)="handleClick()">点击我</button>
```

#### 表单处理

Angular 通过 `ngModel`（用于双向绑定）和 `ngForm`（用于表单验证）等指令简化了表单处理。

```typescript
// 组件类
export class AppComponent {
  formData: any = {};

  onSubmit(): void {
    console.log('表单已提交：', this.formData);
  }
}
```

```html
<!-- 模板 -->
<form (ngSubmit)="onSubmit()">
  <input type="text" [(ngModel)]="formData.username" name="username" required>
  <button type="submit">提交</button>
</form>
```

## 响应式表单

Angular 还支持响应式表单，为表单管理提供了一种更具可扩展性和结构化的方法。

```typescript
import { Component } from '@angular/core';
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
```




`form: FormGroup;`

`constructor(private fb: FormBuilder) {`

`this.form = this.fb.group({`

`username: ['', Validators.required],`

`email: ['', [Validators.required, Validators.email]],`

`password: ['', [Validators.required, Validators.minLength(6)]]`

`});`

`}`

`onSubmit(): void {`

`if (this.form.valid) {`

`console.log('Form submitted:', this.form.value);`

`}`

`}`

`}`

```html
<!-- 模板 -->
<form [formGroup]="form" (ngSubmit)="onSubmit()">
  <input type="text" formControlName="username" placeholder="用户名">
  <input type="email" formControlName="email" placeholder="邮箱">
  <input type="password" formControlName="password" placeholder="密码">
  <button type="submit" [disabled]="form.invalid">提交</button>
</form>
```

4\. ASP.NET Core 集成：当将 Angular 与 ASP.NET Core 后端集成时，你可以在 Angular 中处理用户交互，并通过 HTTP 请求（使用 Angular 的 `HttpClient`）与后端通信。

```typescript
import { HttpClient } from '@angular/common/http';

export class AppComponent {
  constructor(private http: HttpClient) {}

  fetchData(): void {
    this.http.get('https://api.example.com/data')
      .subscribe((data: any) => {
        console.log('Received data:', data);
      });
  }
}
```

在此示例中，`HttpClient` 用于向 API 端点发起 GET 请求，以异步方式获取数据。

理解数据绑定和用户交互对于构建交互式和动态的 Angular 应用程序至关重要。无论是单向绑定、事件处理、表单管理还是双向数据绑定，Angular 都提供了强大的工具和指令来简化前端开发。通过将 Angular 与 ASP.NET Core 后端集成，你可以创建响应迅速、可扩展且用户友好的全栈 Web 应用程序，在整个应用程序中提供无缝的用户体验。

## 第 8 章：构建功能丰富的 Angular 14 组件

### 使用 Angular Router 实现路由

使用 Angular Router 实现路由对于创建具有多个视图或页面的单页应用程序（SPA）至关重要。Angular Router 提供了一种强大且灵活的方式来管理 Angular 应用程序中的导航、路由参数和嵌套路由。让我们通过基于 ASP.NET Core 8 后端和 Angular 14 前端的示例，探索如何使用 Angular Router 实现路由。

1\. 设置 Angular Router：首先，确保你的 Angular 项目中已安装 Angular Router。你可以使用 Angular CLI 生成一个带有路由的新 Angular 模块。

```bash
ng generate module app-routing --flat --module=app
```

此命令会生成一个包含必要路由配置的 `app-routing.module.ts` 文件。

2\. 配置路由：在 `app-routing.module.ts` 文件中，使用 `RouterModule.forRoot()` 方法定义你的应用程序路由。每个路由由一个路径、一个组件以及可选的附加配置（如路由参数或子路由）组成。

```typescript
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { HomeComponent } from './home/home.component';
import { AboutComponent } from './about/about.component';
import { ContactComponent } from './contact/contact.component';

const routes: Routes = [
  { path: '', component: HomeComponent },
  { path: 'about', component: AboutComponent },
  { path: 'contact', component: ContactComponent },
  // 根据需要添加更多路由
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

3\. 添加路由出口：在你的主 `app.component.html` 文件中，添加一个 `<router-outlet></router-outlet>` 标签，路由组件将根据当前路由在此处显示。

```html
<!-- app.component.html -->
<router-outlet></router-outlet>
```

4\. 创建路由组件：为路由配置中定义的每个路由创建 Angular 组件。例如，创建 `home.component.ts`、`about.component.ts` 和 `contact.component.ts`。

```bash
ng generate component home
ng generate component about
ng generate component contact
```

5\. 导航和链接：使用 Angular Router 的 `routerLink` 指令在应用程序中的路由之间进行导航。相应地更新你的导航菜单或链接。

```html
<!-- 示例导航菜单 -->
<ul>
  <li><a routerLink="/">首页</a></li>
  <li><a routerLink="/about">关于</a></li>
  <li><a routerLink="/contact">联系</a></li>
</ul>
```

6\. 路由参数：你可以使用路由参数向路由传递参数。更新你的路由配置，并在相应的组件中访问参数。

```typescript
const routes: Routes = [
  { path: 'product/:id', component: ProductComponent },
];

// 在组件中访问路由参数
import { ActivatedRoute } from '@angular/router';

export class ProductComponent implements OnInit {
  constructor(private route: ActivatedRoute) { }

  ngOnInit(): void {
    this.route.params.subscribe(params => {
      const productId = params['id'];
      // 在你的组件逻辑中使用 productId
    });
  }
}
```

7\. 子路由和嵌套路由：Angular Router 支持嵌套或子路由，允许你在其他路由内定义路由。这对于组织复杂的应用程序布局非常有用。

```typescript
const routes: Routes = [
  {
    path: 'admin',
    component: AdminComponent,
    children: [
      { path: 'dashboard', component: DashboardComponent },
      { path: 'users', component: UsersComponent },
      // 添加更多子路由
    ]
  },
];
```

8\. 路由守卫：Angular Router 中的路由守卫允许你根据特定条件控制导航和访问。例如，你可以实现一个认证守卫来限制对某些路由的访问。

```typescript
import { Injectable } from '@angular/core';
import { CanActivate, Router } from '@angular/router';
import { AuthService } from './auth.service';

@Injectable({
  providedIn: 'root'
})
export class AuthGuard implements CanActivate {
  constructor(private authService: AuthService, private router: Router) { }

  canActivate(): boolean {
    if (this.authService.isLoggedIn()) {
      return true;
    } else {
      this.router.navigate(['/login']); // 重定向到登录页面
      return false;
    }
  }
}
```

9\. 与 ASP.NET Core 后端集成：当将 Angular Router 与 ASP.NET Core 后端集成时，请确保你的后端 API 端点与 Angular 应用程序中预期的路由相匹配。例如，如果你的 Angular 应用有像 `/api/products` 这样的路由，请确保你的 ASP.NET Core 后端在 `/api/products` 处公开 API。

Angular Router 为在 Angular 应用程序中实现客户端路由和导航提供了强大的机制。通过配置路由、定义路由组件、处理路由参数和使用路由守卫，你可以创建动态且响应迅速的 SPA，提供无缝的用户体验。当与 ASP.NET Core 后端集成时，Angular Router 能够实现高效的客户端-服务器通信和导航功能，从而支持全栈 Web 开发。

### Angular 应用程序中的表单和数据验证

表单和数据验证是 Web 开发的重要方面，允许用户输入数据并确保其准确性和完整性。在 Angular 应用程序中，可以使用模板驱动表单或响应式表单来创建表单。让我们结合基于 ASP.NET Core 8 后端和 Angular 14 前端的示例，探讨这两种方法以及数据验证技术。

1\. 模板驱动表单：Angular 中的模板驱动表单基于指令和模板驱动验证。以下是使用模板驱动表单创建带有验证的基本表单的方法：

表单创建：在 Angular 组件的 HTML 模板中，使用 `ngForm` 指令和带有 `ngModel` 的表单控件（用于双向数据绑定）来创建表单。

```html
<form #myForm="ngForm" (ngSubmit)="onSubmit(myForm)">
  <div>
    <label for="name">姓名：</label>
```





# Angular 表单与数据验证

## 模板驱动表单

```html
<input type="text" id="name" name="name" [(ngModel)]="formData.name" required>
</div>
<div>
<label for="email">Email:</label>
<input type="email" id="email" name="email" [(ngModel)]="formData.email" required email>
<div *ngIf="myForm.controls.email.invalid && (myForm.controls.email.dirty || myForm.controls.email.touched)">
<div *ngIf="myForm.controls.email.errors.required">Email is required.</div>
<div *ngIf="myForm.controls.email.errors.email">Invalid email format.</div>
</div>
</div>
<button type="submit" [disabled]="myForm.invalid">Submit</button>
</form>
```

### 表单验证

使用 Angular 指令，如 `required` 和 `email` 进行内置验证。

● 根据表单控件的有效性和用户交互显示错误消息。

### 表单提交

在组件类中处理表单提交。

```typescript
import { Component } from '@angular/core';

@Component({
selector: 'app-my-form',
templateUrl: './my-form.component.html',
styleUrls: ['./my-form.component.css']
})
export class MyFormComponent {
formData: any = {};

onSubmit(form: any): void {
if (form.valid) {
console.log('Form submitted:', this.formData);
// You can perform HTTP requests to submit data to the backend
}
}
}
```

## 响应式表单

响应式表单在 Angular 中提供了一种更结构化、以代码为中心的表单处理方法。以下是创建带有验证的响应式表单的方法：

### 表单创建

在组件类中使用 `FormBuilder` 定义响应式表单。

```typescript
import { Component, OnInit } from '@angular/core';
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

@Component({
selector: 'app-my-reactive-form',
templateUrl: './my-reactive-form.component.html',
styleUrls: ['./my-reactive-form.component.css']
})
export class MyReactiveFormComponent implements OnInit {
myForm: FormGroup;

constructor(private fb: FormBuilder) { }

ngOnInit(): void {
this.myForm = this.fb.group({
name: ['', Validators.required],
email: ['', [Validators.required, Validators.email]]
});
}

onSubmit(): void {
if (this.myForm.valid) {
console.log('Form submitted:', this.myForm.value);
// You can perform HTTP requests to submit data to the backend
}
}
}
```

### 表单验证

使用 `Validators` 定义验证规则，如 `required` 和 `email`。

● 在表单初始化期间将验证器应用于表单控件。

## 表单模板

在 HTML 模板中将表单控件绑定到响应式表单。

```html
<form [formGroup]="myForm" (ngSubmit)="onSubmit()">
<div>
<label for="name">Name:</label>
<input type="text" id="name" formControlName="name">
<div *ngIf="myForm.controls.name.invalid && myForm.controls.name.touched">
<div *ngIf="myForm.controls.name.errors.required">Name is required.</div>
</div>
</div>
<div>
<label for="email">Email:</label>
<input type="email" id="email" formControlName="email">
<div *ngIf="myForm.controls.email.invalid && (myForm.controls.email.dirty || myForm.controls.email.touched)">
<div *ngIf="myForm.controls.email.errors.required">Email is required.</div>
<div *ngIf="myForm.controls.email.errors.email">Invalid email format.</div>
</div>
</div>
<button type="submit" [disabled]="myForm.invalid">Submit</button>
</form>
```

## ASP.NET Core 后端中的数据验证

虽然 Angular 处理客户端验证，但在服务器端（ASP.NET Core）验证数据对于确保数据完整性和安全性至关重要。在 ASP.NET Core 控制器和服务中实现服务器端验证逻辑。

```csharp
using System.ComponentModel.DataAnnotations;

public class FormData
{
[Required(ErrorMessage = "Name is required.")]
public string Name { get; set; }

[Required(ErrorMessage = "Email is required.")]
[EmailAddress(ErrorMessage = "Invalid email format.")]
public string Email { get; set; }
}

[ApiController]
[Route("api/[controller]")]
public class FormController : ControllerBase
{
[HttpPost("submit")]
public IActionResult SubmitForm([FromBody] FormData formData)
{
if (!ModelState.IsValid)
{
return BadRequest(ModelState);
}
// Process the valid form data (e.g., save to database, send email, etc.)
return Ok("Form submitted successfully.");
}
}
```

在此示例中，`FormData` 类使用数据注解，如 `[Required]` 和 `[EmailAddress]` 进行验证。控制器的 `SubmitForm` 操作检查 `ModelState.IsValid` 属性，以确保传入的数据在处理之前符合验证规则。

表单和数据验证是 Web 开发的关键方面，确保用户输入准确、完整且安全。在 Angular 应用程序中，您可以使用模板驱动表单或响应式表单来实现表单，每种方式都提供了其优势和灵活性。Angular 中的客户端验证通过向用户提供即时反馈来帮助改善用户体验。

在服务器端（本例中为 ASP.NET Core），再次执行数据验证以确保数据完整性和安全性至关重要。通过将 Angular 中的客户端验证与 ASP.NET Core 中的服务器端验证相结合，您可以创建一个健壮可靠的应用程序，有效且安全地处理用户输入。

## 使用 Angular HttpClient 消费 Web API

消费 Web API 是现代 Web 开发中的常见任务，Angular 提供了一个强大的 HTTP 客户端模块 `HttpClient`，用于向后端 API 发出 HTTP 请求。在本指南中，我们将探讨如何在 Angular 14 应用程序中使用 `HttpClient` 消费 Web API，示例基于 ASP.NET Core 8 后端。

### 设置 Angular HttpClient

Angular 应用程序使用 `HttpClientModule` 与 HTTP 服务交互。首先，确保在 Angular 模块（`app.module.ts`）中导入了 `HttpClientModule`。

```typescript
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { HttpClientModule } from '@angular/common/http';
import { FormsModule } from '@angular/forms'; // If using forms
import { AppComponent } from './app.component';

@NgModule({
declarations: [
AppComponent
],
imports: [
BrowserModule,
HttpClientModule,
FormsModule // If using forms
],
providers: [],
bootstrap: [AppComponent]
})
export class AppModule { }
```

### 发出 HTTP GET 请求

要从 ASP.NET Core 后端消费 GET 端点，请在 Angular 服务或组件中使用 `HttpClient`。

● **创建 Angular 服务**：创建一个服务来封装 HTTP 请求。使用 Angular CLI 生成服务：

```bash
ng generate service data
```

● **服务实现**：在您的服务（`data.service.ts`）中，注入 `HttpClient` 并定义发出 HTTP 请求的方法。

```typescript
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
providedIn: 'root'
})
export class DataService {
private apiUrl = 'https://localhost:5001/api/data'; // API endpoint

constructor(private http: HttpClient) { }

getData(): Observable<any> {
return this.http.get<any>(this.apiUrl);
}
}
```

● **在组件中使用服务**：在组件中使用该服务从 API 获取数据。

```typescript
import { Component, OnInit } from '@angular/core';
import { DataService } from './data.service';

@Component({
selector: 'app-root',
templateUrl: './app.component.html',
styleUrls: ['./app.component.css']
})
export class AppComponent implements OnInit {
data: any;

constructor(private dataService: DataService) { }

ngOnInit(): void {
this.loadData();
}

loadData(): void {
this.dataService.getData().subscribe(response => {
this.data = response;
});
}
}
```

● **在模板中显示数据**：在组件的模板（`app.component.html`）中显示获取的数据。

```html
<div *ngIf="data">
<h1>Data from API:</h1>
<ul>
<li *ngFor="let item of data">{{ item.name }}</li>
</ul>
</div>
```




```
3. 发起其他 HTTP 请求：除了 GET 请求，你还可以使用 `HttpClient` 的 `post`、`put`、`patch` 和 `delete` 等方法发起其他 HTTP 请求，如 POST、PUT、PATCH、DELETE 等。以下是一个 POST 请求的示例：

```typescript
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class DataService {
  private apiUrl = 'https://localhost:5001/api/data'; // API 端点

  constructor(private http: HttpClient) { }

  postData(data: any): Observable<any> {
    return this.http.post<any>(this.apiUrl, data);
  }
}
```

4. 处理错误和 Observable 管道：在使用 Web API 时，处理错误和管理 observable 管道非常重要。使用 RxJS 库中的 `catchError`、`map`、`tap` 等操作符可以进行高级 HTTP 请求处理。

```typescript
import { Injectable } from '@angular/core';
import { HttpClient, HttpErrorResponse } from '@angular/common/http';
import { Observable, throwError } from 'rxjs';
import { catchError } from 'rxjs/operators';

@Injectable({
  providedIn: 'root'
})
export class DataService {
  private apiUrl = 'https://localhost:5001/api/data'; // API 端点

  constructor(private http: HttpClient) { }

  getData(): Observable<any> {
    return this.http.get<any>(this.apiUrl)
      .pipe(
        catchError((error: HttpErrorResponse) => {
          console.error('发生错误:', error);
          return throwError('出了点问题。请稍后再试。');
        })
      );
  }
}
```

Angular 的 `HttpClient` 模块为在 Angular 应用中使用 Web API 提供了一种便捷高效的方式。通过创建服务来封装 HTTP 请求并处理 observable 管道，你可以轻松地与 ASP.NET Core 等后端 API 集成，以获取和发送数据。请记住，要优雅地处理错误，并使用 RxJS 操作符管理异步操作，以在你的 Angular 应用中实现健壮的 API 使用。

## 第 9 章：Angular 14 应用中的状态管理

### 理解状态管理的必要性

状态管理是现代 Web 应用的关键方面，尤其是那些使用 Angular 和 ASP.NET Core 等框架构建的应用。它指的是管理应用数据及其在应用不同组件或模块间的同步。在复杂的应用中，适当的状态管理可确保数据在各种视图或组件间保持一致和最新。让我们深入探讨状态管理的必要性，以及如何在 Angular 14 应用与 ASP.NET Core 8 后端中解决这一问题。

1. 状态管理的必要性：
    - 组件通信：在 Angular 应用中，组件经常需要通信和共享数据。简单的数据绑定或输入/输出机制可能足以满足父子组件间的通信。然而，当组件之间没有直接关系时（例如，兄弟组件），就需要一种集中式的状态管理方法。
    - 复杂的 UI 和交互：现代 Web 应用通常具有复杂的用户界面，包含多个视图、表单和交互元素。如果没有结构化的状态管理方法，管理这些 UI 组件的状态（包括用户输入、表单数据和应用状态）可能会很困难。
    - 异步数据处理：在处理异步操作（如 HTTP 请求、数据获取或实时更新（例如通过 WebSocket 连接））时，管理获取的数据或应用加载状态对于提供无缝的用户体验至关重要。
    - 可扩展性和可维护性：随着应用复杂性和规模的增长，使用本地组件状态或基于服务的数据共享进行临时状态管理可能会导致代码重复、数据不一致和维护挑战。集中式的状态管理解决方案有助于组织和扩展应用的数据处理逻辑。

2. Angular 中的状态管理选项：
    - 本地组件状态：特定于组件且不与其他组件共享的简单状态可以使用本地组件状态（例如组件类中的属性）来管理。
    - 服务：Angular 服务可用于在组件间共享状态和数据。然而，服务通常是单例实例，其状态在应用中共享。这种方法适用于管理全局应用状态或共享数据。
    - RxJS 和 Observables：RxJS 提供了管理异步数据流和状态的强大工具。Observable 和 subject 可用于表示和管理随时间变化的状态，从而在 Angular 应用中实现响应式编程范式。
    - NgRx（Redux 模式）：NgRx 是一个用于 Angular 的状态管理库，它实现了 Redux 模式。它提供了一个集中式的存储来管理应用状态，用于状态更改的操作，用于处理操作并不可变地更新状态的 reducer，以及用于访问状态特定部分的 selector。

3. 使用 NgRx 进行状态管理的示例：NgRx 是 Angular 应用中状态管理的流行选择。以下是如何使用 NgRx 进行状态管理的简化示例：
    - 安装 NgRx：

```bash
npm install @ngrx/store @ngrx/effects @ngrx/entity @ngrx/store-devtools
```

    - 定义 Actions、Reducers 和 Effects：为管理状态和处理副作用（例如 HTTP 请求）创建操作类型、操作创建者、reducer 和 effect。
    - 定义状态结构：定义应用状态的结构，包括实体、集合和与 UI 相关的状态。
    - 设置 Store 和 Effects：在 Angular 模块中配置 NgRx store、effect 和 reducer。使用初始状态值初始化 store。
    - 分发 Actions：从你的组件或服务中分发操作以触发状态更改和副作用。
    - 使用 Selectors 获取数据：在组件中使用 selector 来获取状态的特定部分。selector 有助于维护数据获取的单一事实来源。
    - 响应式更新 UI：在组件中使用 observable 订阅状态更改。根据状态更改响应式地更新 UI。

状态管理在构建可扩展、可维护和响应迅速的 Web 应用中起着至关重要的作用。虽然简单的应用可能依赖本地组件状态或服务进行数据共享，但复杂的应用可以从 Angular 中像 NgRx 这样的集中式状态管理解决方案中受益。通过理解状态管理的必要性并选择适当的策略和工具，开发者可以有效地管理应用状态，提高数据一致性，并在与 ASP.NET Core 后端集成的 Angular 应用中增强用户体验。

### 利用 NgRx 进行全局状态管理

在 Angular 应用中利用 NgRx 进行全局状态管理是一种强大的方法，可以高效地处理复杂的应用状态和数据流。NgRx 实现了 Redux 模式，它集中管理应用状态，并通过操作和 reducer 提供了一种可预测的方式来管理状态更改。让我们探讨如何在集成 ASP.NET Core 8 后端的 Angular 14 应用中利用 NgRx 进行全局状态管理。

1. 安装 NgRx：在利用 NgRx 之前，你需要安装所需的 NgRx 包。NgRx 包含多个包，如 `@ngrx/store`、`@ngrx/effects`、`@ngrx/entity` 和 `@ngrx/store-devtools`。

```bash
npm install @ngrx/store @ngrx/effects @ngrx/entity @ngrx/store-devtools
```

2. 设置 NgRx Store：
    - 定义 Actions：操作代表可以触发应用状态更改的事件或操作。为每个操作定义操作类型和操作创建者。

```typescript
// data.actions.ts
import { createAction, props } from '@ngrx/store';

export const loadData = createAction('[Data] Load Data');
```




export const loadDataSuccess = createAction('[Data] Load Data Success', props<{ data: any[] }>());

export const loadDataFailure = createAction('[Data] Load Data Failure', props<{ error: any }>());

## 定义 Reducers

Reducers 是纯函数，负责根据分发的 actions 处理状态转换。为应用状态的每个切片定义 reducers。

```typescript
// data.reducer.ts
import { createReducer, on } from '@ngrx/store';
import * as DataActions from './data.actions';

export interface DataState {
  data: any[];
  loading: boolean;
  error: any;
}

export const initialState: DataState = {
  data: [],
  loading: false,
  error: null
};

export const dataReducer = createReducer(
  initialState,
  on(DataActions.loadData, state => ({ ...state, loading: true })),
  on(DataActions.loadDataSuccess, (state, { data }) => ({ ...state, data, loading: false })),
  on(DataActions.loadDataFailure, (state, { error }) => ({ ...state, error, loading: false }))
);
```

## 设置 Effects

Effects 用于处理副作用，例如 HTTP 请求，并根据这些副作用的结果分发新的 actions。

```typescript
// data.effects.ts
import { Injectable } from '@angular/core';
import { Actions, createEffect, ofType } from '@ngrx/effects';
import { of } from 'rxjs';
import { catchError, map, switchMap } from 'rxjs/operators';
import * as DataActions from './data.actions';
import { DataService } from './data.service';

@Injectable()
export class DataEffects {
  loadData$ = createEffect(() => this.actions$.pipe(
    ofType(DataActions.loadData),
    switchMap(() =>
      this.dataService.getData().pipe(
        map(data => DataActions.loadDataSuccess({ data })),
        catchError(error => of(DataActions.loadDataFailure({ error })))
      )
    )
  ));

  constructor(private actions$: Actions, private dataService: DataService) { }
}
```

## 注册 NgRx 模块

在 Angular 模块（`app.module.ts`）中注册 NgRx 模块（store, effects 等）。

```typescript
import { StoreModule } from '@ngrx/store';
import { EffectsModule } from '@ngrx/effects';
import { dataReducer } from './data.reducer';
import { DataEffects } from './data.effects';

@NgModule({
  imports: [
    StoreModule.forRoot({ data: dataReducer }),
    EffectsModule.forRoot([DataEffects]),
    // Other imports
  ],
  providers: [DataEffects],
  // Other configurations
})
export class AppModule { }
```

## 在组件中使用全局状态

### 分发 Actions

从组件中分发 NgRx actions 以触发状态更改。

```typescript
import { Component, OnInit } from '@angular/core';
import { Store } from '@ngrx/store';
import { loadData } from './data.actions';

@Component({
  selector: 'app-data',
  templateUrl: './data.component.html',
  styleUrls: ['./data.component.css']
})
export class DataComponent implements OnInit {
  constructor(private store: Store<{ data: DataState }>) { }

  ngOnInit(): void {
    this.loadData();
  }

  loadData(): void {
    this.store.dispatch(loadData());
  }
}
```

### 使用 Selectors 访问状态

使用 NgRx selectors 在组件中访问全局状态的特定部分。

```typescript
import { Component } from '@angular/core';
import { Store, select } from '@ngrx/store';
import { Observable } from 'rxjs';
import { DataState } from './data.reducer';
import { selectData } from './data.selectors';

@Component({
  selector: 'app-data-view',
  templateUrl: './data-view.component.html',
  styleUrls: ['./data-view.component.css']
})
export class DataViewComponent {
  data$: Observable<any[]>;

  constructor(private store: Store<{ data: DataState }>) {
    this.data$ = this.store.pipe(select(selectData));
  }
}
```

NgRx 为 Angular 应用中的全局状态管理提供了强大的解决方案。通过定义 actions、reducers、effects 和 selectors，您可以高效地管理复杂的应用状态。这种方法为您的应用数据提供了单一事实来源，并促进了组件间可预测的状态更改。当与 ASP.NET Core 后端集成时，NgRx 有助于无缝管理应用数据流，并确保一致的用户体验。

## 在组件中实现本地状态管理

在 Angular 组件中实现本地状态管理对于管理特定于组件的数据和 UI 状态至关重要。与适用于管理应用范围状态的全局状态管理库（如 NgRx）不同，本地状态管理侧重于特定于某个组件的数据。让我们探讨如何在基于 ASP.NET Core 8 后端的 Angular 14 组件中实现本地状态管理。

### 1. 使用组件类属性

管理 Angular 组件本地状态最简单的方法之一是在组件类中直接使用属性。

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-example',
  templateUrl: './example.component.html',
  styleUrls: ['./example.component.css']
})
export class ExampleComponent {
  count: number = 0;
  message: string = '';

  increment(): void {
    this.count++;
  }

  decrement(): void {
    this.count--;
  }

  updateMessage(newMessage: string): void {
    this.message = newMessage;
  }
}
```

在此示例中，`count` 和 `message` 是 `ExampleComponent` 的本地状态变量。`increment`、`decrement` 和 `updateMessage` 方法用于更新这些状态变量。

### 2. 使用模板绑定显示状态

您可以将本地状态变量绑定到组件的模板以显示动态数据。

```html
<!-- example.component.html -->
<p>Count: {{ count }}</p>
<p>Message: {{ message }}</p>
<button (click)="increment()">Increment</button>
<button (click)="decrement()">Decrement</button>
<input type="text" [(ngModel)]="newMessage">
<button (click)="updateMessage(newMessage)">Update Message</button>
```

在模板中，`{{ count }}` 和 `{{ message }}` 分别显示 `count` 和 `message` 变量的当前值。`(click)` 事件绑定调用相应的方法来更新状态。

### 3. 管理 UI 状态和交互性

本地状态管理通常用于管理与 UI 相关的状态，例如可见性、表单输入值、加载指示器等。

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-example',
  templateUrl: './example.component.html',
  styleUrls: ['./example.component.css']
})
export class ExampleComponent {
  showDetails: boolean = false;
  inputValue: string = '';

  toggleDetails(): void {
    this.showDetails = !this.showDetails;
  }

  handleInputChange(value: string): void {
    this.inputValue = value;
  }

  submitForm(): void {
    // Handle form submission with inputValue
  }
}
```

### 4. 处理组件生命周期和本地状态

Angular 组件具有生命周期钩子，允许您在组件生命周期的特定阶段执行操作。这些钩子可用于相应地管理本地状态。

```typescript
import { Component, OnInit, OnDestroy } from '@angular/core';

@Component({
  selector: 'app-example',
  templateUrl: './example.component.html',
  styleUrls: ['./example.component.css']
})
export class ExampleComponent implements OnInit, OnDestroy {
  timer: any;
  counter: number = 0;

  ngOnInit(): void {
    this.timer = setInterval(() => {
      this.counter++;
    }, 1000);
  }

  ngOnDestroy(): void {
    clearInterval(this.timer);
  }
}
```




在此示例中，`ngOnInit` 初始化了一个计时器，该计时器每秒递增 `counter`。`ngOnDestroy` 在组件销毁时清理资源，防止内存泄漏。

本地状态管理对于管理 Angular 应用程序中的特定于组件的数据和 UI 状态至关重要。通过利用组件类属性、模板绑定和生命周期钩子，你可以有效地管理 Angular 组件内的本地状态。这种方法使组件保持自包含，促进可重用性，并增强 Angular 应用程序的可维护性。当与 NgRx 等用于应用程序范围状态的全局状态管理解决方案结合使用时，本地状态管理有助于构建与 ASP.NET Core 后端服务集成的健壮且可扩展的 Angular 应用程序。

## 第 10 章：使用 Angular 14 特性增强用户体验

### 使用动画和指令构建交互式 UI

在 Angular 14 中使用动画和指令构建交互式 UI，为你的 Web 应用程序增加了一层用户体验增强。Angular 提供了强大的工具和库来创建动态和动画化的用户界面。让我们探索如何将动画和指令集成到基于 ASP.NET Core 8 后端的 Angular 14 应用程序中。

1.  **使用 Angular 动画**：Angular 的内置动画模块 (`@angular/animations`) 允许你为各种 UI 元素（如组件、过渡和状态更改）创建动画。以下是如何在 Angular 中使用动画的示例：

    *   **安装 Angular 动画**：

        ```bash
        npm install @angular/animations
        ```

    *   **导入 BrowserAnimationsModule**：在你的 Angular 模块 (`app.module.ts`) 中导入 `BrowserAnimationsModule` 以在应用程序中启用动画。

        ```typescript
        import { BrowserModule } from '@angular/platform-browser';
        import { NgModule } from '@angular/core';
        import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
        import { AppComponent } from './app.component';

        @NgModule({
          declarations: [
            AppComponent
          ],
          imports: [
            BrowserModule,
            BrowserAnimationsModule
          ],
          providers: [],
          bootstrap: [AppComponent]
        })
        export class AppModule { }
        ```

    *   **定义动画**：在你的组件中使用 Angular 的 `trigger`、`transition` 和 `style` 函数创建动画。

        ```typescript
        import { Component } from '@angular/core';
        import { trigger, transition, style, animate } from '@angular/animations';

        @Component({
          selector: 'app-example',
          templateUrl: './example.component.html',
          styleUrls: ['./example.component.css'],
          animations: [
            trigger('fadeInOut', [
              transition(':enter', [
                style({ opacity: 0 }),
                animate('500ms', style({ opacity: 1 })),
              ]),
              transition(':leave', [
                animate('500ms', style({ opacity: 0 })),
              ]),
            ]),
          ]
        })
        export class ExampleComponent {
          showElement: boolean = false;

          toggleElement(): void {
            this.showElement = !this.showElement;
          }
        }
        ```

    *   **在模板中应用动画**：在你的组件模板 (`example.component.html`) 中应用定义的动画。

        ```html
        <div @fadeInOut *ngIf="showElement">
          <p>This element will fade in and out</p>
        </div>

        <button (click)="toggleElement()">Toggle Element</button>
        ```

        在此示例中，`@fadeInOut` 动画根据 `showElement` 状态应用于 `div` 元素。

2.  **使用 Angular 指令**：Angular 指令是 DOM 元素上的标记，它告诉 Angular 对该元素或其子元素执行某些操作。指令可用于创建可重用组件、控制元素的行为以及增强 UI 的交互性。

    *   **创建自定义指令**：你可以创建自定义指令来封装行为并将其应用于模板中的元素。

        ```typescript
        import { Directive, HostListener, ElementRef } from '@angular/core';

        @Directive({
          selector: '[appHighlight]'
        })
        export class HighlightDirective {
          constructor(private el: ElementRef) { }

          @HostListener('mouseenter') onMouseEnter(): void {
            this.highlight('yellow');
          }

          @HostListener('mouseleave') onMouseLeave(): void {
            this.highlight(null);
          }

          private highlight(color: string | null): void {
            this.el.nativeElement.style.backgroundColor = color;
          }
        }
        ```

    *   **使用自定义指令**：在你的组件模板中应用自定义指令以添加高亮行为。

        ```html
        <div appHighlight>
          Hover over me to highlight!
        </div>
        ```

        在此示例中，当鼠标进入或离开 `div` 元素时，`appHighlight` 指令会更改其背景颜色。

利用 Angular 动画和指令可以增强 Web 应用程序 UI 的交互性和视觉吸引力。动画可用于创建平滑的过渡、效果和视觉提示，而指令允许你封装行为并创建可重用组件。通过将动画和指令集成到你的 Angular 14 应用程序中，你可以构建引人入胜且动态的用户界面，从而提供更好的用户体验。这些技术与 ASP.NET Core 8 后端结合使用，使你能够创建满足用户对响应性和交互性期望的现代交互式 Web 应用程序。

### 实现服务器端渲染 (SSR) 以提升性能

在 Angular 应用程序中实现服务器端渲染 (SSR) 可以通过在将页面发送到客户端之前在服务器上预渲染页面来提高性能并增强搜索引擎优化 (SEO)。在本指南中，我们将探讨如何在与 ASP.NET Core 8 后端集成的 Angular 14 应用程序中实现 SSR。

1.  **为 SSR 设置 Angular Universal**：Angular Universal 是在 Angular 应用程序中实现 SSR 的解决方案。它允许使用 Node.js 或其他服务器平台在服务器端渲染 Angular 应用程序。

    *   **安装 Angular Universal**：首先，安装必要的 Angular Universal 包。

        ```bash
        ng add @nguniversal/express-engine
        ```

    *   **生成 SSR 文件**：Angular Universal 生成与 SSR 相关的文件和配置。

        ```bash
        ng generate universal --clientProject [your-project-name]
        ```

        将 `[your-project-name]` 替换为你的 Angular 项目名称。

2.  **将 Angular Universal 与 ASP.NET Core 配置**：设置好 Angular Universal 后，将其与你的 ASP.NET Core 后端集成。

    *   **Angular SSR 中间件**：配置 ASP.NET Core 以提供 Angular Universal SSR 输出。

        ```csharp
        // Startup.cs
        public void ConfigureServices(IServiceCollection services)
        {
            // Add Angular Universal services
            services.AddSpaStaticFiles(configuration =>
            {
                configuration.RootPath = "ClientApp/dist";
            });
        }

        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            // Other middleware configurations
            app.UseSpaStaticFiles();
            app.UseSpa(spa =>
            {
                spa.Options.SourcePath = "ClientApp";

                if (env.IsDevelopment())
                {
                    // Use Angular CLI server in development mode
                    spa.UseAngularCliServer(npmScript: "start");
                }
            });
        }
        ```

    *   **SSR 构建和运行**：构建并运行你的应用程序以确保 SSR 按预期工作。

        ```bash
        npm run build:ssr
        dotnet run
        ```

3.  **在 Angular 组件中处理 SSR**：

    *   **修改 App 模块**：在你的 `app.module.ts` 中，确保将 ` BrowserModule` 替换为 `BrowserModule.withServerTransition({ appId: 'your-app-id' })`。

        ```typescript
        // app.module.ts
        import { BrowserModule } from '@angular/platform-browser';
        import { NgModule } from '@angular/core';
        import { AppModule } from './app.module';
        import { AppComponent } from './app.component';
        import { ServerModule } from '@angular/platform-server';

        @NgModule({
          imports: [
            BrowserModule.withServerTransition({ appId: 'your-app-id' }),
            ServerModule,
            AppModule
          ],
          bootstrap: [AppComponent]
        })
        export class AppServerModule { }
        ```

    *   **使用 TransferState 服务**：要在服务器和客户端之间传输状态，请使用 Angular 的 `TransferState` 服务。

        ```typescript
        import { Component, OnInit } from '@angular/core';
        ```



import { TransferState, makeStateKey } from '@angular/platform-browser';
import { HttpClient } from '@angular/common/http';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent implements OnInit {
  constructor(private transferState: TransferState, private http: HttpClient) {}

  ngOnInit(): void {
    const key = makeStateKey<any>('your-data-key');
    const data = this.transferState.get(key, null);
    if (!data) {
      this.http.get<any>('your-api-url').subscribe(apiData => {
        this.transferState.set(key, apiData);
      });
    }
  }
}

```
在此示例中，`TransferState` 用于在 SSR 期间将数据从服务器传输到客户端。
```

## SSR 的优势

1.  **提升性能**：SSR 减少了初始加载时间并提升了感知性能，尤其对于网络连接较慢或设备性能较低的用户。
2.  **SEO 优化**：搜索引擎可以更有效地抓取和索引 SSR 渲染的页面，从而提升搜索引擎排名。
3.  **增强用户体验**：用户能更快地看到内容渲染，从而获得更流畅、响应更及时的用户体验。

在 Angular 应用中使用 Angular Universal 实现服务端渲染（SSR），并将其与 ASP.NET Core 8 后端集成，能带来显著的性能和 SEO 优势。它加快了初始页面加载速度，提升了 SEO 排名，并增强了整体用户体验。通过遵循上述步骤并理解 SSR 和 Angular Universal 的概念，你可以创建高性能的 Angular 应用，提升其可访问性和搜索引擎可见性。

# 第 11 章：测试与部署 Angular 14 应用

## Angular 的单元测试与端到端测试策略

单元测试和端到端（E2E）测试是确保 Angular 应用质量和可靠性的关键环节。让我们探讨一下与 ASP.NET Core 8 后端集成的 Angular 应用的单元测试和 E2E 测试策略。

### Angular 中的单元测试

单元测试涉及在隔离环境中测试代码的各个单元或组件，以验证其正确性。在 Angular 中，单元测试通常使用 Jasmine 等框架编写，并通过 Angular 测试工具执行。

**设置单元测试**：Angular CLI 内置了对单元测试的支持。你可以使用 Angular CLI 为组件生成单元测试文件。

```bash
ng generate component my-component --skip-tests=false
```

此命令会生成一个组件及其对应的单元测试文件。

**编写单元测试**：让我们看一个使用 Jasmine 和 Angular 测试工具对组件方法进行单元测试的简单示例。

```typescript
import { TestBed } from '@angular/core/testing';
import { MyComponent } from './my-component.component';

describe('MyComponent', () => {
  beforeEach(async () => {
    await TestBed.configureTestingModule({
      declarations: [MyComponent]
    }).compileComponents();
  });

  it('should create the component', () => {
    const fixture = TestBed.createComponent(MyComponent);
    const component = fixture.componentInstance;
    expect(component).toBeTruthy();
  });

  it('should increment count', () => {
    const fixture = TestBed.createComponent(MyComponent);
    const component = fixture.componentInstance;
    component.increment();
    expect(component.count).toEqual(1);
  });
});
```

在此示例中，我们测试了组件的创建以及其 `increment` 方法的行为。

### Angular 中的端到端（E2E）测试

E2E 测试涉及从开始到结束测试整个应用流程，模拟用户交互并验证预期结果。Angular 应用可以使用基于 Selenium WebDriver 的 Protractor 等工具进行 E2E 测试。

**设置 E2E 测试**：Angular CLI 支持使用 Protractor 进行 E2E 测试。你可以使用 Angular CLI 生成 E2E 测试配置。

```bash
ng e2e
```

此命令会生成一个 E2E 测试配置文件（`protractor.conf.js`）和一个示例 E2E 测试文件（`app.e2e-spec.ts`）。

**编写 E2E 测试**：以下是使用 Protractor 测试登录功能的 E2E 测试示例。

```typescript
import { browser, by, element } from 'protractor';

describe('Login Page', () => {
  beforeEach(() => {
    browser.get('/login');
  });

  it('should display login form', () => {
    expect(element(by.tagName('form'))).toBeTruthy();
  });

  it('should login with valid credentials', () => {
    element(by.id('username')).sendKeys('user1');
    element(by.id('password')).sendKeys('password');
    element(by.id('loginBtn')).click();
    browser.waitForAngular();
    expect(browser.getCurrentUrl()).toContain('/dashboard');
  });

  it('should show error message with invalid credentials', () => {
    element(by.id('username')).sendKeys('invalidUser');
    element(by.id('password')).sendKeys('invalidPassword');
    element(by.id('loginBtn')).click();
    browser.waitForAngular();
    expect(element(by.className('error-msg')).getText()).toContain('Invalid credentials');
  });
});
```

在此 E2E 测试中，我们模拟了用户操作，如输入凭据和点击登录按钮，然后验证预期结果，例如成功登录重定向或错误消息显示。

### 测试策略的优势

**单元测试优势**：

1.  确保各个组件在隔离环境中按预期工作。
2.  便于重构和代码维护。
3.  在开发早期阶段识别错误和问题。

**E2E 测试优势**：

1.  从用户角度验证应用的功能。
2.  测试实际的用户交互和用户流程。
3.  有助于识别集成问题和端到端场景。

单元测试和 E2E 测试是 Angular 应用健壮测试策略不可或缺的组成部分。单元测试确保各个组件和函数的正确性，而 E2E 测试则从用户角度验证整个应用流程。通过采用这些测试策略并使用 Jasmine、Protractor 和 Angular 测试工具等工具，开发者可以确保与 ASP.NET Core 8 后端集成的 Angular 应用的质量、可靠性和性能。

## 构建和优化用于生产的 Angular 应用

构建和优化用于生产的 Angular 应用涉及多个步骤，以确保高性能、可靠性和效率。让我们深入了解为生产部署构建和优化与 ASP.NET Core 8 后端集成的 Angular 应用的过程。

### Angular 中的生产构建

Angular CLI 提供了工具来为 Angular 应用构建优化的生产就绪包。生产构建会减小文件大小、优化代码，并启用高效缓存以提升性能。

**运行生产构建**：执行 Angular CLI 命令以生成 Angular 应用的生产构建。

```bash
ng build --prod
```




此命令会创建一个 `dist` 文件夹，其中包含已优化、可直接部署的构建文件。

## 2. 优化技术

1.  **代码压缩**：在生产构建期间，Angular CLI 会自动压缩和混淆 JavaScript 和 CSS 文件，以减小其体积。
2.  **摇树优化**：Angular CLI 执行摇树优化以移除未使用的代码和依赖项，从而减小打包体积。
3.  **预编译**：生产构建默认启用预编译。它在构建过程中编译 Angular 模板和组件，减少运行时开销。
4.  **优化资源加载**：Angular CLI 通过高效打包图像、字体和样式表等资源来优化资源加载。

## 3. Angular 生产环境最佳实践

1.  **延迟加载**：使用延迟加载仅在需要时加载模块和组件，减小初始打包体积并提升应用启动性能。
2.  **优化打包**：根据你的应用结构配置 Angular CLI 以生成优化的打包文件。智能地拆分打包文件可以提升应用特定部分的加载时间。
3.  **生产环境配置**：使用特定于环境的配置文件（`environment.prod.ts`）来设置生产环境特有的变量，如 API 端点、调试标志等。
4.  **Service Worker 与渐进式 Web 应用**：实现 Service Worker 并启用 PWA 功能，以提供离线能力、更快的加载速度以及更接近原生应用的用户体验。

## 4. 优化 ASP.NET Core 后端

虽然 Angular 负责前端优化，但优化后端（ASP.NET Core）对于整体应用性能也起着至关重要的作用。

- **启用压缩**：配置 ASP.NET Core 以启用响应压缩，减少服务器与客户端之间的数据传输量。
- **缓存策略**：为频繁访问的数据或静态内容实现缓存策略，以减少服务器负载并提升响应时间。
- **数据库优化**：优化数据库查询、索引和数据检索策略，确保高效的数据访问和处理。

## 5. 部署策略

- **部署流水线**：使用 Azure DevOps、Jenkins 或 GitHub Actions 等工具设置部署流水线，以自动化构建和部署过程。
- **持续集成/持续部署**：实现 CI/CD 流水线以自动化测试、构建和部署工作流，确保部署的一致性和可靠性。
- **部署环境**：使用独立的部署环境（例如，开发、预发布、生产）在受控环境中测试变更，然后再部署到生产环境。

## 6. 监控与性能分析

- **监控工具**：使用 Application Insights、New Relic 或 Google Analytics 等监控工具来监控应用性能、跟踪错误并收集使用分析数据。
- **性能优化**：持续监控和分析应用性能指标，如加载时间、服务器响应时间和资源利用率。根据从监控工具获得的洞察来优化性能。

构建和优化用于生产的 Angular 应用涉及前端和后端优化、部署策略以及性能监控的结合。通过遵循最佳实践，如运行生产构建、优化代码和资源、实现延迟加载、启用缓存以及设置部署流水线，开发者可以确保与 ASP.NET Core 后端集成的 Angular 应用在生产环境中具有高性能、可扩展性和可靠性。定期的监控和性能分析有助于识别和解决性能瓶颈，确保为终端用户提供流畅高效的体验。

## Angular Web 应用的部署选项

部署 Angular Web 应用涉及选择正确的部署选项，以确保高效、可靠且可扩展的部署流程。让我们探讨一些与 ASP.NET Core 8 后端集成的 Angular Web 应用的部署选项。

### 1. 传统托管

- **手动部署**：使用传统托管时，你需要手动将 Angular 应用和 ASP.NET Core 后端部署到 Web 服务器。这可以是共享主机提供商、虚拟专用服务器（VPS）或专用服务器。
- **FTP/SFTP 上传**：你可以使用 FTP（文件传输协议）或 SFTP（SSH 文件传输协议）将你的 Angular 构建文件（`dist` 文件夹）和 ASP.NET Core 后端文件上传到服务器。

### 2. 云托管

- **Microsoft Azure 应用服务**：Azure 应用服务提供了一个平台即服务（PaaS）环境来托管 Web 应用。你可以将 Angular 应用和 ASP.NET Core 后端都部署到 Azure 应用服务。
- **AWS Elastic Beanstalk**：AWS Elastic Beanstalk 是一个用于部署和扩展 Web 应用及服务的平台。你可以在 Elastic Beanstalk 中将 Angular 和 ASP.NET Core 应用部署为独立的环境。
- **Google Cloud Platform (GCP) App Engine**：GCP App Engine 提供了一个用于部署和扩展 Web 应用的环境。你可以将 Angular 和 ASP.NET Core 应用部署到 App Engine，并受益于自动扩展和托管基础设施。

### 3. 容器化部署

1.  **Docker 容器**：使用 Docker 将你的 Angular 和 ASP.NET Core 应用容器化，可以实现跨不同环境的一致部署。你可以为前端和后端创建 Docker 镜像，然后将它们部署到 Kubernetes 等容器编排平台。
2.  **Azure 容器实例**：Azure 容器实例提供了一个无服务器的容器托管解决方案。你可以将 Docker 容器部署到 ACI，无需管理虚拟机。
3.  **Amazon ECS/EKS**：Amazon ECS（弹性容器服务）和 EKS（弹性 Kubernetes 服务）是 AWS 上的容器编排服务。你可以将 Docker 容器部署到 ECS 集群或 EKS 集群，以实现可扩展和托管的部署。

### 4. 部署脚本与自动化

- **CI/CD 流水线**：使用 Azure DevOps、GitHub Actions、Jenkins 或 GitLab CI/CD 等工具设置持续集成和持续部署（CI/CD）流水线。这些流水线自动化了构建、测试和部署过程，确保高效可靠的部署。
- **部署脚本**：使用 Shell 脚本、PowerShell 脚本或配置管理工具（例如 Ansible、Chef、Puppet）编写部署脚本，以自动化构建、打包、上传和配置应用程序等部署步骤。

### 5. 部署示例

以下是使用 Azure 应用服务和 Azure DevOps CI/CD 流水线部署带有 ASP.NET Core 后端的 Angular 应用的示例：

1.  配置你的 Angular 应用以进行生产构建（`ng build --prod`）。
2.  配置你的 ASP.NET Core 应用以进行生产部署。
3.  为你的 Angular 前端设置一个 Azure 应用服务，为你的 ASP.NET Core 后端设置另一个应用服务。
4.  在 Azure DevOps 中创建一个 CI/CD 流水线，该流水线在代码提交到你的仓库时触发。
5.  配置流水线以构建你的 Angular 和 ASP.NET Core 应用，将它们打包，并部署到各自对应的 Azure 应用服务。

选择正确的部署选项取决于可扩展性需求、自动化需求、云提供商偏好以及基础设施管理偏好等因素。无论你选择传统托管、云托管、容器化部署，还是这些方式的组合，确保与 ASP.NET Core 后端服务集成的 Angular Web 应用部署流程无缝、高效和可靠都至关重要。定期的测试、监控和自动化有助于随时间推移维护和改进部署工作流。

# 第 12 章：集成 ASP.NET Core 8 与 Angular 14

## 从 Angular 调用 ASP.NET Core 8 Web API

从 Angular 应用调用 ASP.NET Core 8 Web API 是现代 Web 开发中的常见场景。在本指南中，我们将探讨如何在 Angular 中发起 HTTP 请求并处理响应，以与使用 ASP.NET Core 8 构建的后端 API 进行交互。

### 1. 设置 Angular HTTP 客户端

Angular 提供了 `HttpClientModule` 用于向外部 API 发起 HTTP 请求。在使用之前，请确保在 Angular 应用的根模块（`app.module.ts`）中导入了 `HttpClientModule`。

```typescript





// app.module.ts

import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';
import { HttpClientModule } from '@angular/common/http'; // 导入 HttpClientModule
import { AppComponent } from './app.component';

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    HttpClientModule // 将 HttpClientModule 添加到 imports 中
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }

```

## 2. 发起 HTTP GET 请求

让我们从发起一个简单的 HTTP GET 请求开始，从 ASP.NET Core Web API 端点获取数据。

### 服务实现

创建一个 Angular 服务来封装与 API 相关的 HTTP 请求。

```typescript
// api.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';
import { catchError } from 'rxjs/operators';

@Injectable({
  providedIn: 'root'
})
export class ApiService {
  private apiUrl = 'https://your-api-url/api/';

  constructor(private http: HttpClient) {}

  getData(): Observable<any> {
    return this.http.get<any>(this.apiUrl + 'data')
      .pipe(
        catchError((error) => {
          throw 'Error in fetching data: ' + error;
        })
      );
  }
}
```

### 组件使用

现在，在你的组件中使用 `ApiService` 来从 API 获取数据。

```typescript
// app.component.ts
import { Component } from '@angular/core';
import { ApiService } from './api.service';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  responseData: any;

  constructor(private apiService: ApiService) {}

  fetchData(): void {
    this.apiService.getData().subscribe(
      (data) => {
        this.responseData = data;
      },
      (error) => {
        console.error('Error fetching data:', error);
      }
    );
  }
}
```

### HTML 模板

在你的组件 HTML 模板中显示获取到的数据。

```html
<!-- app.component.html -->
<button (click)="fetchData()">获取数据</button>
<div *ngIf="responseData">
  <p>来自 API 的数据：</p>
  <ul>
    <li *ngFor="let item of responseData">{{ item.name }}</li>
  </ul>
</div>
```

## 3. 发起 HTTP POST 请求

让我们扩展示例，加入一个 HTTP POST 请求，向 ASP.NET Core Web API 发送数据。

### 服务实现

在你的服务中添加一个方法来处理 HTTP POST 请求。

```typescript
// api.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';
import { catchError } from 'rxjs/operators';

@Injectable({
  providedIn: 'root'
})
export class ApiService {
  private apiUrl = 'https://your-api-url/api/';

  constructor(private http: HttpClient) {}

  getData(): Observable<any> {
    return this.http.get<any>(this.apiUrl + 'data')
      .pipe(
        catchError((error) => {
          throw 'Error in fetching data: ' + error;
        })
      );
  }

  postData(data: any): Observable<any> {
    return this.http.post<any>(this.apiUrl + 'post', data)
      .pipe(
        catchError((error) => {
          throw 'Error in posting data: ' + error;
        })
      );
  }
}
```

### 组件使用

修改你的组件，添加一个用于向 API 发送数据的方法。

```typescript
// app.component.ts
import { Component } from '@angular/core';
import { ApiService } from './api.service';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  responseData: any;
  postDataInput: string = '';

  constructor(private apiService: ApiService) {}

  fetchData(): void {
    this.apiService.getData().subscribe(
      (data) => {
        this.responseData = data;
      },
      (error) => {
        console.error('Error fetching data:', error);
      }
    );
  }

  postData(): void {
    const data = { message: this.postDataInput };
    this.apiService.postData(data).subscribe(
      (response) => {
        console.log('Response from API:', response);
      },
      (error) => {
        console.error('Error posting data:', error);
      }
    );
  }
}
```

### HTML 模板

添加一个输入框和一个按钮来触发 POST 请求。

```html
<!-- app.component.html -->
<button (click)="fetchData()">获取数据</button>
<div *ngIf="responseData">
  <p>来自 API 的数据：</p>
  <ul>
    <li *ngFor="let item of responseData">{{ item.name }}</li>
  </ul>
</div>
<input type="text" [(ngModel)]="postDataInput" placeholder="输入消息">
<button (click)="postData()">发送数据</button>
```

## 4. 处理响应与错误处理

在上面的示例中，我们使用 `subscribe` 方法处理 API 响应，其中指定了成功和错误处理的独立函数。这使我们能够处理 API 响应，并处理 HTTP 请求期间可能发生的任何错误。

从 Angular 应用程序使用 ASP.NET Core 8 Web API 涉及利用 Angular 的 `HttpClientModule` 发起 GET 和 POST 等 HTTP 请求。通过将 API 交互封装在 Angular 服务中、处理响应并与 Angular 组件集成，你可以在 Angular 前端和 ASP.NET Core 后端之间创建无缝通信。请记住，在 Angular 应用程序中处理 API 时，要优雅地处理错误，并考虑身份验证和授权等安全方面。

## 将身份验证和授权流程与 Angular 集成

集成身份验证和授权流程对于保护与 ASP.NET Core 8 Web API 交互的 Angular 应用程序至关重要。此过程涉及实现用户身份验证、管理用户会话，以及基于用户角色和权限强制执行访问控制。让我们深入了解如何将身份验证和授权流程与 Angular 集成，使用基于 ASP.NET Core 8 后端的示例。

### 1. Angular 中的身份验证

身份验证验证访问应用程序的用户的身份。Angular 应用程序通常使用 JSON Web Tokens (JWT) 进行身份验证，其中后端在成功登录时颁发令牌，前端在后续 API 请求中包含此令牌。

#### 用户身份验证服务

创建一个 Angular 服务来处理用户身份验证任务，如登录、注销和令牌管理。

```typescript
// auth.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { BehaviorSubject, Observable } from 'rxjs';
import { tap } from 'rxjs/operators';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  private apiUrl = 'https://your-api-url/auth/';
  private tokenSubject: BehaviorSubject<string | null>;

  constructor(private http: HttpClient) {
    // 如果 localStorage 中有令牌，则用它初始化 tokenSubject
    this.tokenSubject = new BehaviorSubject<string | null>(
      localStorage.getItem('token')
    );
  }

  get token(): Observable<string | null> {
    return this.tokenSubject.asObservable();
  }

  login(username: string, password: string): Observable<any> {
    return this.http.post<any>(this.apiUrl + 'login', { username, password })
      .pipe(
        tap(response => {
          const token = response.token;
          localStorage.setItem('token', token);
          this.tokenSubject.next(token);
        })
      );
  }

  logout(): void {
    localStorage.removeItem('token');
    this.tokenSubject.next(null);
  }
}
```

### 登录组件

创建一个登录组件，用户可以在其中输入凭据并进行身份验证。

```typescript
// login.component.ts
import { Component } from '@angular/core';
import { AuthService } from './auth.service';

@Component({
  selector: 'app-login',
  templateUrl: './login.component.html',
  styleUrls: ['./login.component.css']
})
export class LoginComponent {
  username: string = '';
  password: string = '';

  constructor(private authService: AuthService) {}

  login(): void {
    this.authService.login(this.username, this.password).subscribe(
      () => {
        // 登录成功后重定向到主页/仪表板或执行必要的操作
      },
      error => {
        console.error('Login failed:', error);
        // 处理登录错误（例如，显示错误消息）
      }
    );
  }
}
```




● 登录组件模板：为登录组件创建一个 HTML 模板。

```html
<!-- login.component.html -->
<form (ngSubmit)="login()">
  <input type="text" [(ngModel)]="username" placeholder="Username">
  <input type="password" [(ngModel)]="password" placeholder="Password">
  <button type="submit">Login</button>
</form>
```

2\. 授权与访问控制：授权根据用户的角色和权限，决定他们可以访问哪些操作和资源。Angular 可以通过根据从后端获取的用户角色来控制 UI 元素和路由，从而处理授权。

● 基于角色的授权服务：创建一个服务来管理用户角色和权限。

```typescript
// auth.service.ts (extended for authorization)
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { BehaviorSubject, Observable } from 'rxjs';
import { tap } from 'rxjs/operators';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  // Existing code for authentication...
  private rolesSubject: BehaviorSubject<string[]>;

  constructor(private http: HttpClient) {
    // Initialize rolesSubject with roles from localStorage if available
    this.rolesSubject = new BehaviorSubject<string[]>(
      JSON.parse(localStorage.getItem('roles')) || []
    );
  }

  get roles(): Observable<string[]> {
    return this.rolesSubject.asObservable();
  }

  setRoles(roles: string[]): void {
    localStorage.setItem('roles', JSON.stringify(roles));
    this.rolesSubject.next(roles);
  }

  clearRoles(): void {
    localStorage.removeItem('roles');
    this.rolesSubject.next([]);
  }
}
```

● 授权守卫：创建一个 Angular 路由守卫，根据用户角色控制对特定路由的访问。

```typescript
// auth.guard.ts
import { Injectable } from '@angular/core';
import { CanActivate, ActivatedRouteSnapshot, RouterStateSnapshot, Router } from '@angular/router';
import { Observable } from 'rxjs';
import { AuthService } from './auth.service';

@Injectable({
  providedIn: 'root'
})
export class AuthGuard implements CanActivate {
  constructor(private authService: AuthService, private router: Router) {}

  canActivate(
    next: ActivatedRouteSnapshot,
    state: RouterStateSnapshot): Observable<boolean> | Promise<boolean> | boolean {
    const requiredRoles = next.data.roles as string[];
    const userRoles = this.authService.getRolesFromLocalStorage(); // Implement this method in AuthService
    if (userRoles && requiredRoles.every(role => userRoles.includes(role))) {
      return true;
    } else {
      // Redirect to unauthorized page or handle unauthorized access
      this.router.navigate(['/unauthorized']);
      return false;
    }
  }
}
```

● 路由配置：配置你的应用程序路由，并使用 `AuthGuard` 来控制访问。

```typescript
// app-routing.module.ts
import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { AuthGuard } from './auth.guard';
import { DashboardComponent } from './dashboard.component';
import { AdminComponent } from './admin.component';

const routes: Routes = [
  { path: '', component: DashboardComponent, canActivate: [AuthGuard], data: { roles: ['user', 'admin'] } },
  { path: 'admin', component: AdminComponent, canActivate: [AuthGuard], data: { roles: ['admin'] } },
  { path: 'unauthorized', component: UnauthorizedComponent },
  { path: '**', redirectTo: '' } // Handle other routes or 404
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

在 ASP.NET Core 8 后端集成 Angular 应用程序中的认证和授权流程，涉及管理用户认证、处理 JWT 令牌、基于用户角色控制访问以及保护路由。通过实现认证和授权服务、使用路由守卫以及配置基于角色的访问控制，你可以确保你的 Angular 应用程序在与后端 API 交互时，提供安全且受控的用户体验。定期测试和验证认证与授权机制对于维护应用程序的安全标准至关重要。

## 第 13 章：构建具有认证和数据的全栈 Web 应用程序

### 实现安全的用户登录系统

实现一个安全的用户登录系统涉及多个步骤，以确保认证并保护用户凭证。我们将介绍使用 ASP.NET Core 8 作为后端 API 和 Angular 14 作为前端的实现方法。以下是如何创建一个安全的用户登录系统：

1\. 后端实现 (ASP.NET Core 8)：

● 用户模型和数据库设置：首先，定义一个 `User` 模型来表示用户信息，如用户名、密码（哈希值）和角色。

```csharp
// User.cs
using System.ComponentModel.DataAnnotations;

public class User
{
    [Key]
    public int Id { get; set; }

    [Required]
    public string Username { get; set; }

    [Required]
    public string PasswordHash { get; set; }

    // Add other user properties as needed (e.g., roles, email)
}
```

确保你已在 ASP.NET Core 项目中设置并配置了数据库，以安全地存储用户数据。

● 认证控制器：创建一个认证控制器来处理用户登录请求，并在认证成功后颁发 JWT 令牌。

```csharp
// AuthController.cs
using Microsoft.AspNetCore.Mvc;
using Microsoft.Extensions.Configuration;
using Microsoft.IdentityModel.Tokens;
using System;
using System.IdentityModel.Tokens.Jwt;
using System.Security.Claims;
using System.Text;

[Route("api/[controller]")]
[ApiController]
public class AuthController : ControllerBase
{
    private readonly IConfiguration _config;
    private readonly IUserRepository _userRepository; // Inject user repository

    public AuthController(IConfiguration config, IUserRepository userRepository)
    {
        _config = config;
        _userRepository = userRepository;
    }

    [HttpPost("login")]
    public IActionResult Login([FromBody] LoginModel loginModel)
    {
        var user = _userRepository.GetUserByUsername(loginModel.Username);
        if (user == null || !VerifyPassword(loginModel.Password, user.PasswordHash))
        {
            return Unauthorized(); // Invalid credentials
        }

        var token = GenerateJwtToken(user);
        return Ok(new { Token = token });
    }

    private string GenerateJwtToken(User user)
    {
        var claims = new[]
        {
            new Claim(ClaimTypes.Name, user.Username),
            // Add other claims (e.g., roles) as needed
        };

        var key = new SymmetricSecurityKey(Encoding.UTF8.GetBytes(_config["Jwt:Secret"]));
        var creds = new SigningCredentials(key, SecurityAlgorithms.HmacSha256);

        var token = new JwtSecurityToken(
            issuer: _config["Jwt:Issuer"],
            audience: _config["Jwt:Audience"],
            claims: claims,
            expires: DateTime.Now.AddMinutes(30), // Token expiration time
            signingCredentials: creds);

        return new JwtSecurityTokenHandler().WriteToken(token);
    }

    private bool VerifyPassword(string password, string passwordHash)
    {
        // Implement password verification logic (e.g., using hashing algorithms)
    }
}
```

● JWT 配置：在 `Startup.cs` 中配置 JWT 认证，以验证传入的 JWT 令牌并认证用户。

```csharp
// Startup.cs
public void ConfigureServices(IServiceCollection services)
{
    // Other service configurations
    services.AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
        .AddJwtBearer(options =>
        {
            options.TokenValidationParameters = new TokenValidationParameters
            {
                ValidateIssuer = true,
                ValidateAudience = true,
                ValidateLifetime = true,
                ValidateIssuerSigningKey = true,
                ValidIssuer = Configuration["Jwt:Issuer"],
                ValidAudience = Configuration["Jwt:Audience"],
                IssuerSigningKey = new SymmetricSecurityKey(Encoding.UTF8.GetBytes(Configuration["Jwt:Secret"]))
            };
        });
}
```

2\. 前端实现 (Angular 14)：

● 登录组件：创建一个 Angular 登录组件，用于捕获用户凭证并将其发送到后端进行认证。

```typescript
```



# 构建用户管理与数据访问的 API 端点

构建用于用户管理和数据访问的 API 端点是开发健壮 Web 应用程序的关键部分。在本指南中，我们将介绍如何使用 ASP.NET Core 8 作为后端、Angular 14 作为前端，为用户 CRUD 操作和数据访问创建 API 端点。

## 1. 用户管理 API 端点

### 用户模型

首先，在 ASP.NET Core 8 应用程序中定义一个 `User` 模型来表示用户数据。

```csharp
// User.cs
using System.ComponentModel.DataAnnotations;

public class User
{
    [Key]
    public int Id { get; set; }

    [Required]
    public string Username { get; set; }

    [Required]
    public string PasswordHash { get; set; }

    // 根据需要添加其他用户属性（例如，角色、电子邮件）
}
```

### 用户仓储接口

创建一个仓储接口来定义用户 CRUD 操作的方法。

```csharp
// IUserRepository.cs
using System.Collections.Generic;

public interface IUserRepository
{
    IEnumerable<User> GetAllUsers();
    User GetUserById(int id);
    User GetUserByUsername(string username);
    void AddUser(User user);
    void UpdateUser(User user);
    void DeleteUser(int id);
}
```

### 用户仓储实现

在具体类中实现 `IUserRepository` 接口。

```csharp
// UserRepository.cs
using System;
using System.Collections.Generic;
using System.Linq;

public class UserRepository : IUserRepository
{
    private readonly List<User> _users = new List<User>();

    public UserRepository()
    {
        // 使用示例数据初始化（替换为数据库操作）
        _users.Add(new User { Id = 1, Username = "user1", PasswordHash = "hashed_password" });
        _users.Add(new User { Id = 2, Username = "user2", PasswordHash = "hashed_password" });
    }

    public IEnumerable<User> GetAllUsers()
    {
        return _users;
    }

    public User GetUserById(int id)
    {
        return _users.FirstOrDefault(u => u.Id == id);
    }

    public User GetUserByUsername(string username)
    {
        return _users.FirstOrDefault(u => u.Username == username);
    }

    public void AddUser(User user)
    {
        user.Id = _users.Count + 1; // 生成新 ID（替换为数据库生成的 ID）
        _users.Add(user);
    }

    public void UpdateUser(User user)
    {
        var existingUser = _users.FirstOrDefault(u => u.Id == user.Id);
        if (existingUser != null)
        {
            existingUser.Username = user.Username;
            existingUser.PasswordHash = user.PasswordHash;
            // 根据需要更新其他属性
        }
    }

    public void DeleteUser(int id)
    {
        var userToRemove = _users.FirstOrDefault(u => u.Id == id);
        if (userToRemove != null)
        {
            _users.Remove(userToRemove);
        }
    }
}
```

### 用户控制器

创建一个控制器来处理与用户管理相关的 HTTP 请求。

```csharp
// UserController.cs
using Microsoft.AspNetCore.Mvc;

[Route("api/[controller]")]
[ApiController]
public class UserController : ControllerBase
{
    private readonly IUserRepository _userRepository;

    public UserController(IUserRepository userRepository)
    {
        _userRepository = userRepository;
    }

    [HttpGet]
    public IActionResult GetAllUsers()
    {
        var users = _userRepository.GetAllUsers();
        return Ok(users);
    }

    [HttpGet("{id}")]
    public IActionResult GetUserById(int id)
    {
        var user = _userRepository.GetUserById(id);
        if (user == null)
        {
            return NotFound(); // 未找到用户
        }
        return Ok(user);
    }

    [HttpPost]
    public IActionResult AddUser([FromBody] User user)
    {
        _userRepository.AddUser(user);
        return CreatedAtAction(nameof(GetUserById), new { id = user.Id }, user);
    }

    [HttpPut("{id}")]
    public IActionResult UpdateUser(int id, [FromBody] User user)
    {
        var existingUser = _userRepository.GetUserById(id);
        if (existingUser == null)
        {
            return NotFound(); // 未找到用户
        }
        existingUser.Username = user.Username;
        existingUser.PasswordHash = user.PasswordHash;
        // 根据需要更新其他属性
        _userRepository.UpdateUser(existingUser);
        return NoContent();
    }

    [HttpDelete("{id}")]
    public IActionResult DeleteUser(int id)
    {
        var existingUser = _userRepository.GetUserById(id);
        if (existingUser == null)
        {
            return NotFound(); // 未找到用户
        }
        _userRepository.DeleteUser(id);
        return NoContent();
    }
}
```

## 2. 数据访问 API 端点

### 数据模型

为应用程序实体定义数据模型。

```csharp
// Product.cs
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
    // 根据需要添加其他产品属性
}
```

### 产品仓储接口与实现

创建用于管理产品的仓储接口和实现。

```csharp
// IProductRepository.cs
using System.Collections.Generic;

public interface IProductRepository
{
    IEnumerable<Product> GetAllProducts();
    Product GetProductById(int id);
    void AddProduct(Product product);
    void UpdateProduct(Product product);
    void DeleteProduct(int id);
}
```

```csharp
// ProductRepository.cs
using System;
using System.Collections.Generic;
using System.Linq;

public class ProductRepository : IProductRepository
{
    private readonly List<Product> _products = new List<Product>();

    public ProductRepository()
    {
        // 使用示例数据初始化（替换为数据库操作）
        _products.Add(new Product { Id = 1, Name = "Product 1", Price = 10.99m });
        _products.Add(new Product { Id = 2, Name = "Product 2", Price = 24.99m });
    }

    public IEnumerable<Product> GetAllProducts()
    {
        return _products;
    }

    public Product GetProductById(int id)
    {
        return _products.FirstOrDefault(p => p.Id == id);
    }

    public void AddProduct(Product product)
    {
        product.Id = _products.Count + 1; // 生成新 ID（替换为数据库生成的 ID）
        _products.Add(product);
    }

    public void UpdateProduct(Product product)
    {
        var existingProduct = _products.FirstOrDefault(p => p.Id == product.Id);
        if (existingProduct != null)
        {
            existingProduct.Name = product.Name;
            existingProduct.Price = product.Price;
            // 根据需要更新其他属性
        }
    }

    public void DeleteProduct(int id)
    {
        var productToRemove = _products.FirstOrDefault(p => p.Id == id);
        if (productToRemove != null)
        {
            _products.Remove(productToRemove);
        }
    }
}
```

## Angular 前端集成

### 登录组件

```typescript
// login.component.ts
import { Component } from '@angular/core';
import { AuthService } from './auth.service';

@Component({
  selector: 'app-login',
  templateUrl: './login.component.html',
  styleUrls: ['./login.component.css']
})
export class LoginComponent {
  username: string = '';
  password: string = '';

  constructor(private authService: AuthService) {}

  login(): void {
    this.authService.login(this.username, this.password).subscribe(
      (response) => {
        // 登录成功后重定向到主页/仪表板或执行必要操作
      },
      (error) => {
        console.error('Login failed:', error);
        // 处理登录错误（例如，显示错误消息）
      }
    );
  }
}
```

### 认证服务

创建一个 Angular 服务来处理与认证相关的任务和 HTTP 请求。

```typescript
// auth.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  private apiUrl = 'https://your-api-url/auth/';

  constructor(private http: HttpClient) {}

  login(username: string, password: string): Observable<any> {
    return this.http.post<any>(this.apiUrl + 'login', { username, password });
  }
}
```

### 登录组件模板

为登录组件创建 HTML 模板。

```html
<!-- login.component.html -->
<form (ngSubmit)="login()">
  <input type="text" [(ngModel)]="username" placeholder="Username">
  <input type="password" [(ngModel)]="password" placeholder="Password">
  <button type="submit">Login</button>
</form>
```

通过使用 ASP.NET Core 8 实现后端认证逻辑，并将其与 Angular 14 前端集成，您可以创建一个安全的用户登录系统。确保在后端安全地处理密码哈希、JWT 令牌生成和令牌验证，以保护用户凭据并确保安全的认证过程。定期更新和审查您的认证机制，以解决安全漏洞并维护安全的登录系统。



// 根据需要更新其他属性

}

}

public void DeleteProduct(int id)

{

var productToRemove = _products.FirstOrDefault(p => p.Id == id);

if (productToRemove != null)

{

_products.Remove(productToRemove);

}

}

}

```

● 产品控制器：创建一个控制器来处理与产品管理相关的 HTTP 请求。

```csharp

// ProductController.cs

using Microsoft.AspNetCore.Mvc;

[Route("api/[controller]")]

[ApiController]

public class ProductController : ControllerBase

{

private readonly IProductRepository _productRepository;

public ProductController(IProductRepository productRepository)

{

_productRepository = productRepository;

}

[HttpGet]

public IActionResult GetAllProducts()

{

var products = _productRepository.GetAllProducts();

return Ok(products);

}

[HttpGet("{id}")]

public IActionResult GetProductById(int id)

{

var product = _productRepository.GetProductById(id);

if (product == null)

{

return NotFound(); // 未找到产品

}

return Ok(product);

}

[HttpPost]

public IActionResult AddProduct([FromBody] Product product)

{

_productRepository.AddProduct(product);

return CreatedAtAction(nameof(GetProductById), new { id = product.Id }, product);

}

[HttpPut("{id}")]

public IActionResult UpdateProduct(int id, [FromBody] Product product)

{

var existingProduct = _productRepository.GetProductById(id);

if (existingProduct == null)

{

return NotFound(); // 未找到产品

}

existingProduct.Name = product.Name;

existingProduct.Price = product.Price;

// 根据需要更新其他属性

_productRepository.UpdateProduct(existingProduct);

return NoContent();

}

[HttpDelete("{id}")]

public IActionResult DeleteProduct(int id)

{

var existingProduct = _productRepository.GetProductById(id);

if (existingProduct == null)

{

return NotFound(); // 未找到产品

}

_productRepository.DeleteProduct(id);

return NoContent();

}

}

```

通过在 ASP.NET Core 8 中实现用于用户管理和数据访问的 API 端点，你为 Angular 14 前端创建了一个健壮的后端系统进行交互。确保安全地处理 CRUD 操作、验证输入数据并实施适当的错误处理，以构建可靠且可扩展的 Web 应用程序。使用 Postman 等工具定期测试你的 API，确保它们按预期运行并满足应用程序的要求。

在 Angular 组件中显示和管理用户数据

在 Angular 组件中显示和管理用户数据涉及从后端 API（使用 ASP.NET Core 8 构建）获取用户数据，并使用 Angular 组件在前端呈现。让我们通过代码示例来了解如何实现这一点。

1\. 用于用户数据的 Angular 服务：首先，创建一个 Angular 服务来处理从后端 API 获取用户数据的 HTTP 请求。

```typescript

// user.service.ts

import { Injectable } from '@angular/core';

import { HttpClient } from '@angular/common/http';

import { Observable } from 'rxjs';

import { User } from './user.model'; // 假设你有一个 User 模型

@Injectable({

providedIn: 'root'

})

export class UserService {

private apiUrl = 'https://your-api-url/api/user/';

constructor(private http: HttpClient) {}

getUsers(): Observable<User[]> {

return this.http.get<User[]>(this.apiUrl);

}

getUserById(id: number): Observable<User> {

return this.http.get<User>(`${this.apiUrl}${id}`);

}

addUser(user: User): Observable<User> {

return this.http.post<User>(this.apiUrl, user);

}

updateUser(user: User): Observable<User> {

return this.http.put<User>(`${this.apiUrl}${user.id}`, user);

}

deleteUser(id: number): Observable<any> {

return this.http.delete(`${this.apiUrl}${id}`);

}

}

```

2\. 在 Angular 组件中显示用户数据：

● 用户列表组件：创建一个组件来显示从 API 获取的用户列表。

```typescript

// user-list.component.ts

import { Component, OnInit } from '@angular/core';

import { UserService } from './user.service';

import { User } from './user.model';

@Component({

selector: 'app-user-list',

templateUrl: './user-list.component.html',

styleUrls: ['./user-list.component.css']

})

export class UserListComponent implements OnInit {

users: User[] = [];

constructor(private userService: UserService) {}

ngOnInit(): void {

this.loadUsers();

}

loadUsers(): void {

this.userService.getUsers().subscribe(

(users) => {

this.users = users;

},

(error) => {

console.error('获取用户时出错:', error);

}

);

}

}

```

● 用户列表组件模板：创建一个 HTML 模板来显示用户列表。

```html

<!-- user-list.component.html -->

<div *ngIf="users.length > 0">

<ul>

<li *ngFor="let user of users">

{{ user.id }} - {{ user.username }}

</li>

</ul>

</div>

<div *ngIf="users.length === 0">

<p>没有可用的用户。</p>

</div>

```

● 包含用户列表组件：将用户列表组件包含在你的主应用组件或任何其他父组件中。

```typescript

// app.component.ts (或父组件)

import { Component } from '@angular/core';

@Component({

selector: 'app-root',

template: '<app-user-list></app-user-list>',

})

export class AppComponent {}

```

3\. 管理用户数据：

● 用户详情组件：创建一个组件来查看和编辑用户详情。

```typescript

// user-details.component.ts

import { Component, OnInit } from '@angular/core';

import { ActivatedRoute } from '@angular/router';

import { UserService } from './user.service';

import { User } from './user.model';

@Component({

selector: 'app-user-details',

templateUrl: './user-details.component.html',

styleUrls: ['./user-details.component.css']

})

export class UserDetailsComponent implements OnInit {

userId: number;

user: User;

constructor(private route: ActivatedRoute, private userService: UserService) {}

ngOnInit(): void {

this.route.params.subscribe(params => {

this.userId = params['id'];

this.loadUserDetails();

});

}

loadUserDetails(): void {

this.userService.getUserById(this.userId).subscribe(

(user) => {

this.user = user;

},

(error) => {

console.error('获取用户详情时出错:', error);

}

);

}

updateUser(): void {

this.userService.updateUser(this.user).subscribe(

(updatedUser) => {

console.log('用户已更新:', updatedUser);

},

(error) => {

console.error('更新用户时出错:', error);

}

);

}

}

```

● 用户详情组件模板：创建一个用于查看和编辑用户详情的 HTML 模板。

```html

<!-- user-details.component.html -->

<div *ngIf="user">

<h2>用户详情</h2>

<p>ID: {{ user.id }}</p>

<p>用户名: {{ user.username }}</p>

<!-- 添加其他用户详情 -->

<button (click)="updateUser()">更新用户</button>

</div>

<div *ngIf="!user">

<p>未找到用户。</p>

</div>

```

● 路由配置：配置 Angular 路由以在用户列表和用户详情组件之间导航。

```typescript

// app-routing.module.ts

import { NgModule } from '@angular/core';

import { Routes, RouterModule } from '@angular/router';

import { UserListComponent } from './user-list.component';

import { UserDetailsComponent } from './user-details.component';

const routes: Routes = [

{ path: '', redirectTo: '/users', pathMatch: 'full' },

{ path: 'users', component: UserListComponent },

{ path: 'users/:id', component: UserDetailsComponent },

];

@NgModule({

imports: [RouterModule.forRoot(routes)],

exports: [RouterModule]

})

export class AppRoutingModule { }




通过实现如 `user list` 和 `user details` 这样的 Angular 组件，以及一个用于从 ASP.NET Core 8 后端获取和管理用户数据的 Angular 服务，你可以在 Web 应用程序中有效地显示和管理用户数据。请确保处理错误情况，实现正确的路由，并遵循数据获取和操作的最佳实践，以创建无缝的用户体验。定期测试和验证用户数据操作对于维护数据完整性和应用程序可靠性至关重要。

## 第 14 章：高级集成技术与可扩展性

### 实现延迟加载以提升性能

在 Angular 应用程序中实现延迟加载可以显著提升性能，因为它仅在需要时才加载模块、组件和资源。这种方法减少了初始包大小，加快了应用程序加载时间，并增强了整体用户体验。让我们深入探讨如何在与 ASP.NET Core 8 后端通信的 Angular 14 应用程序中实现延迟加载。

#### 1. Angular 延迟加载设置

- **模块结构**：将你的 Angular 应用程序组织成特性模块。每个特性模块将拥有自己的路由配置和组件。
- **路由配置**：在主应用模块（`app-routing.module.ts`）中设置路由以延迟加载特性模块。

```typescript
// app-routing.module.ts

import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';

const routes: Routes = [
  { path: '', redirectTo: 'home', pathMatch: 'full' },
  { path: 'home', loadChildren: () => import('./home/home.module').then(m => m.HomeModule) },
  { path: 'users', loadChildren: () => import('./users/users.module').then(m => m.UsersModule) },
  // 在此添加其他延迟加载的模块
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule { }
```

在上面的代码中，`HomeModule` 和 `UsersModule` 是延迟加载的模块。Angular 将在访问相应路由时按需加载这些模块。

#### 2. 延迟加载的特性模块

- **创建特性模块**：使用 Angular CLI 生成一个新的特性模块。

```bash
ng generate module users --routing
```

- **特性模块路由**：为特性模块（`users-routing.module.ts`）设置特定的路由。

```typescript
// users-routing.module.ts

import { NgModule } from '@angular/core';
import { Routes, RouterModule } from '@angular/router';
import { UserListComponent } from './user-list.component';
import { UserDetailsComponent } from './user-details.component';

const routes: Routes = [
  { path: '', component: UserListComponent },
  { path: ':id', component: UserDetailsComponent },
];

@NgModule({
  imports: [RouterModule.forChild(routes)],
  exports: [RouterModule]
})
export class UsersRoutingModule { }
```

**延迟加载的组件**：确保延迟加载模块内的组件（`UserListComponent`、`UserDetailsComponent` 等）被正确定义和导出。

#### 3. ASP.NET Core 后端集成

- **API 路由**：确保你的 ASP.NET Core 后端提供 API 以支持延迟加载的功能。例如，在用户管理的情况下：

```csharp
// UsersController.cs

using Microsoft.AspNetCore.Mvc;
using System.Collections.Generic;

[Route("api/[controller]")]
[ApiController]
public class UsersController : ControllerBase
{
    // 在此实现 CRUD 操作
    // 示例操作：获取所有用户、按 ID 获取用户、创建用户、更新用户、删除用户
}
```

- **来自 Angular 的 HTTP 请求**：更新你的 Angular 服务，使其向相应的后端 API 发送 HTTP 请求。例如，在 `UserService` 中：

```typescript
// user.service.ts

import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';
import { User } from './user.model';

@Injectable({
  providedIn: 'root'
})
export class UserService {
  private apiUrl = 'https://your-api-url/api/users/';

  constructor(private http: HttpClient) {}

  getUsers(): Observable<User[]> {
    return this.http.get<User[]>(this.apiUrl);
  }

  getUserById(id: number): Observable<User> {
    return this.http.get<User>(`${this.apiUrl}${id}`);
  }

  // 根据需要包含其他 CRUD 操作
}
```

#### 4. 测试延迟加载

实现延迟加载后，请确保测试你的 Angular 应用程序，以验证模块和组件是否按预期延迟加载。使用浏览器开发者工具分析网络请求和包大小，以确认延迟加载行为。

#### 5. 延迟加载的好处

- **提升初始加载时间**：仅加载必要的模块，从而减少应用程序的初始加载时间。
- **减小包大小**：每个延迟加载的模块都有自己的包，从而减小初始包大小并加快用户下载速度。
- **更好的用户体验**：用户可以更快地开始与应用程序交互，而无需等待所有模块预先加载。

遵循这些步骤和最佳实践，你可以在 Angular 14 应用程序中有效地实现延迟加载，从而提升性能和用户体验，特别是对于具有多个功能和模块的大型应用程序。

### 构建具有离线功能的渐进式 Web 应用程序（PWA）

构建具有离线功能的渐进式 Web 应用程序（PWA）对于提供无缝的用户体验至关重要，尤其是在用户可能具有有限或间歇性互联网连接的场景中。在本指南中，我们将探讨如何使用 ASP.NET Core 8 和 Angular 14 创建具有离线功能的 PWA。

### 设置环境

在深入代码之前，请确保已安装必要的工具：

1. **ASP.NET Core 8 SDK**：从 Microsoft 官方网站安装。
2. **Node.js 和 npm**：Angular 开发所需。你可以从 Node.js 网站下载。
3. **Angular CLI**：使用 npm 全局安装，命令为 `npm install -g @angular/cli`。

安装好先决条件后，让我们创建项目。

#### 创建 ASP.NET Core Web API

请打开终端或命令提示符并执行提供的命令：

```bash
dotnet new webapi -n MyPwaApi
cd MyPwaApi
```

这将创建一个名为 `MyPwaApi` 的新 ASP.NET Core Web API 项目。接下来，让我们添加一个用于测试的简单 API 端点：

```csharp
// Controllers/ValuesController.cs

using Microsoft.AspNetCore.Mvc;
using System.Collections.Generic;

namespace MyPwaApi.Controllers
{
    [Route("api/[controller]")]
    [ApiController]
    public class ValuesController : ControllerBase
    {
        private static List<string> _values = new List<string> { "Value1", "Value2", "Value3" };

        [HttpGet]
        public ActionResult<IEnumerable<string>> Get()
        {
            return _values;
        }
    }
}
```

#### 设置 Angular 14

现在，让我们创建 Angular 前端。在终端中运行：

```bash
ng new MyPwaApp --routing --style=scss
cd MyPwaApp
```

这将搭建一个带有路由和 SCSS 样式的新 Angular 应用程序。接下来，让我们创建一个服务来从 ASP.NET Core API 获取数据：

```bash
ng generate service api
```

修改 `api.service.ts` 文件：

```typescript
// src/app/api.service.ts

import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class ApiService {
  private apiUrl = 'https://localhost:5001/api/values'; // 更新为你的 API URL

  constructor(private http: HttpClient) { }

  getData(): Observable<string[]> {
    return this.http.get<string[]>(this.apiUrl);
  }
}
```

#### 实现离线功能

为了启用离线功能，我们将利用 Angular 提供的 service worker 和 workbox 来管理 service worker。

1. **安装 workbox**：

```bash
npm install workbox-cli --save-dev
```

2. **在 Angular 项目根目录创建 `sw-config.js` 文件**：

```javascript
// sw-config.js

module.exports = {
```




## 配置 Workbox

```javascript
globDirectory: 'dist/MyPwaApp/',
globPatterns: ['**/*.{html,js,css}'],
swDest: 'dist/MyPwaApp/service-worker.js',
};
```

3. 修改 `angular.json` 文件以包含 Workbox 配置：

```json
// angular.json
"architect": {
  "build": {
    "options": {
      "serviceWorker": true,
      "ngswConfigPath": "sw-config.js"
    }
  }
}
```

4. 使用 Workbox 生成 Service Worker：

```bash
npx workbox generateSW sw-config.js
```

## 测试离线功能

构建你的 Angular 应用：

```bash
ng build --prod
```

现在，启动你的 ASP.NET Core API 并在浏览器中导航到 `https://localhost:5001`。你应该能看到具有离线功能的 Angular 应用。

在本指南中，我们介绍了使用 ASP.NET Core 8 和 Angular 14 创建具有离线功能的渐进式 Web 应用的基础知识。通过利用 Service Worker 和 Workbox，你可以通过允许用户在离线时访问应用来增强用户体验。请务必进行彻底测试，以确保你的 PWA 在各种网络条件下都能无缝工作。

## 利用 SignalR 进行实时通信

在 Web 应用中利用 SignalR 进行实时通信可以显著提升用户体验，实现诸如实时更新、聊天功能和实时通知等特性。在本指南中，我们将探讨如何将 SignalR 集成到使用 ASP.NET Core 8 作为后端、Angular 14 作为前端的应用程序中。

### 设置环境

首先，确保你已安装必要的工具：

1. ASP.NET Core 8 SDK：从 Microsoft 官方网站安装。
2. Node.js 和 npm：Angular 开发所需。你可以从 Node.js 网站下载。
3. Angular CLI：使用 `npm install -g @angular/cli` 全局安装。

### 创建 ASP.NET Core SignalR Hub

让我们从创建一个 ASP.NET Core Web API 项目并添加 SignalR 支持开始：

```bash
dotnet new webapi -n MySignalRApp
cd MySignalRApp
dotnet add package Microsoft.AspNetCore.SignalR --version 5.0.0
```

接下来，创建一个 SignalR Hub：

```csharp
// Hubs/ChatHub.cs
using Microsoft.AspNetCore.SignalR;
using System.Threading.Tasks;

namespace MySignalRApp.Hubs
{
    public class ChatHub : Hub
    {
        public async Task SendMessage(string user, string message)
        {
            await Clients.All.SendAsync("ReceiveMessage", user, message);
        }
    }
}
```

### Angular 设置与 SignalR 集成

现在，让我们设置 Angular 前端并集成 SignalR 以实现实时通信。

```bash
ng new MySignalRApp --routing --style=scss
cd MySignalRApp
npm install @microsoft/signalr
```

创建一个服务来处理 SignalR 通信：

```bash
ng generate service signalr
```

修改 `signalr.service.ts` 文件：

```typescript
// src/app/signalr.service.ts
import { Injectable } from '@angular/core';
import { HubConnection, HubConnectionBuilder } from '@microsoft/signalr';
import { Observable, Subject } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class SignalRService {
  private hubConnection: HubConnection;
  private messageSubject: Subject<{ user: string, message: string }> = new Subject();

  constructor() {
    this.hubConnection = new HubConnectionBuilder()
      .withUrl('https://localhost:5001/chatHub') // Update with your SignalR hub URL
      .build();

    this.hubConnection.start()
      .then(() => console.log('SignalR connection started.'))
      .catch(err => console.error('Error while starting SignalR connection:', err));

    this.hubConnection.on('ReceiveMessage', (user: string, message: string) => {
      this.messageSubject.next({ user, message });
    });
  }

  sendMessage(user: string, message: string): void {
    this.hubConnection.invoke('SendMessage', user, message)
      .catch(err => console.error('Error while sending message:', err));
  }

  getMessage(): Observable<{ user: string, message: string }> {
    return this.messageSubject.asObservable();
  }
}
```

### 在 Angular 组件中使用 SignalR

现在，让我们在 Angular 组件中使用 SignalR 服务来演示实时通信。

修改 `app.component.ts` 文件：

```typescript
// src/app/app.component.ts
import { Component, OnInit } from '@angular/core';
import { SignalRService } from './signalr.service';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.scss']
})
export class AppComponent implements OnInit {
  user = 'User';
  message = '';
  messages: { user: string, message: string }[] = [];

  constructor(private signalRService: SignalRService) {}

  ngOnInit(): void {
    this.signalRService.getMessage().subscribe(msg => {
      this.messages.push(msg);
    });
  }

  sendMessage(): void {
    if (this.message.trim() !== '') {
      this.signalRService.sendMessage(this.user, this.message);
      this.message = '';
    }
  }
}
```

修改 `app.component.html` 文件以包含聊天界面：

```html
<!-- src/app/app.component.html -->
<div>
  <input type="text" [(ngModel)]="user" placeholder="Enter your name">
  <input type="text" [(ngModel)]="message" placeholder="Type your message">
  <button (click)="sendMessage()">Send</button>
</div>
<div *ngFor="let msg of messages">
  <strong>{{ msg.user }}:</strong> {{ msg.message }}
</div>
```

### 测试实时通信

运行你的 ASP.NET Core 后端（`dotnet run`）并启动你的 Angular 应用（`ng serve`）。打开多个浏览器窗口，观察使用 SignalR 如何实时发送和接收消息。

在本指南中，我们演示了如何在 ASP.NET Core 8 和 Angular 14 应用中利用 SignalR 进行实时通信。通过集成 SignalR，你可以轻松地为 Web 应用添加实时聊天、通知和协作编辑等功能，从而增强用户参与度和交互性。

## 第 15 章：超越基础——高级全栈开发

实施安全最佳实践，如输入验证和清理，对于保护 Web 应用免受 SQL 注入、跨站脚本（XSS）和跨站请求伪造（CSRF）等各种攻击至关重要。在本指南中，我们将介绍如何使用 ASP.NET Core 8 在后端、Angular 14 在前端实施输入验证和清理。

## 后端：ASP.NET Core 8

#### 输入验证

ASP.NET Core 提供了内置的验证属性，可用于验证输入数据。

1. 模型验证：使用验证属性装饰你的模型类。

```csharp
// Models/User.cs
using System.ComponentModel.DataAnnotations;

public class User
{
    [Required]
    public string Username { get; set; }

    [Required]
    [EmailAddress]
    public string Email { get; set; }

    [Required]
    [StringLength(100, MinimumLength = 6)]
    public string Password { get; set; }
}
```

2. 控制器操作验证：在控制器操作中使用 `ModelState.IsValid` 来检查模型验证。

```csharp
// Controllers/UserController.cs
using Microsoft.AspNetCore.Mvc;

[ApiController]
[Route("api/[controller]")]
public class UserController : ControllerBase
{
    [HttpPost]
    public IActionResult CreateUser([FromBody] User user)
    {
        if (!ModelState.IsValid)
        {
            return BadRequest(ModelState);
        }
        // Process valid user data
        return Ok("User created successfully.");
    }
}
```

## 清理

为防止 XSS 攻击，在将用户输入渲染到视图之前对其进行编码。

```csharp
// Views/Home/Index.cshtml
@model string
<div>
    <p>@Html.DisplayForModel()</p>
</div>
```

## 前端：Angular 14

#### 输入验证

Angular 提供了内置的验证器和响应式表单用于输入验证。

1. 响应式表单设置：在 Angular 组件中定义带有验证器的表单控件。

```typescript
// src/app/user/user.component.ts
import { Component } from '@angular/core';
import { FormBuilder, FormGroup, Validators } from '@angular/forms';

@Component({
  selector: 'app-user',
  templateUrl: './user.component.html'
})
export class UserComponent {
  userForm: FormGroup;
```





## 表单组件

```typescript
constructor(private formBuilder: FormBuilder) {
  this.userForm = this.formBuilder.group({
    username: ['', Validators.required],
    email: ['', [Validators.required, Validators.email]],
    password: ['', [Validators.required, Validators.minLength(6)]]
  });
}

onSubmit(): void {
  if (this.userForm.invalid) {
    return;
  }
  // 处理有效的表单数据
}
```

## 表单模板

在模板中绑定表单控件并显示验证消息。

```html
<!-- src/app/user/user.component.html -->
<form [formGroup]="userForm" (ngSubmit)="onSubmit()">
  <input type="text" formControlName="username" placeholder="Username">
  <div *ngIf="userForm.get('username').hasError('required')">Username is required.</div>

  <input type="email" formControlName="email" placeholder="Email">
  <div *ngIf="userForm.get('email').hasError('required')">Email is required.</div>
  <div *ngIf="userForm.get('email').hasError('email')">Invalid email format.</div>

  <input type="password" formControlName="password" placeholder="Password">
  <div *ngIf="userForm.get('password').hasError('required')">Password is required.</div>
  <div *ngIf="userForm.get('password').hasError('minlength')">Password must be at least 6 characters long.</div>

  <button type="submit" [disabled]="userForm.invalid">Submit</button>
</form>
```

## 清理

Angular 会自动清理模板中的用户输入，以防止 XSS。

```html
<!-- src/app/user/user.component.html -->
<p>{{ unsafeHtmlContent }}</p>
```

在组件 TypeScript 文件中，使用 `DomSanitizer` 将 HTML 内容标记为安全：

```typescript
// src/app/user/user.component.ts
import { Component } from '@angular/core';
import { DomSanitizer, SafeHtml } from '@angular/platform-browser';

@Component({
  selector: 'app-user',
  templateUrl: './user.component.html'
})
export class UserComponent {
  unsafeHtmlContent: SafeHtml;

  constructor(private sanitizer: DomSanitizer) {
    const unsafeHtml = '<script>alert("XSS attack!")</script>';
    this.unsafeHtmlContent = this.sanitizer.bypassSecurityTrustHtml(unsafeHtml);
  }
}
```

实施输入验证和清理对于增强 ASP.NET Core 8 和 Angular 14 Web 应用程序的安全性至关重要。遵循这些最佳实践，你可以缓解常见的安全威胁，如 SQL 注入、XSS 和 CSRF，确保你的应用程序安全可靠地处理用户输入。请始终记住在客户端和服务器端都进行验证，以实现全面的安全覆盖。

## 保护 Web API 免受常见漏洞攻击

保护 Web API 免受常见漏洞攻击是 Web 开发的一个关键方面，旨在保护敏感数据并确保用户信息的完整性和机密性。在本指南中，我们将讨论如何保护使用 ASP.NET Core 8 构建的后端 Web API，并从 Angular 14 前端安全地调用它们，重点关注 SQL 注入、跨站脚本（XSS）和跨站请求伪造（CSRF）等常见漏洞。

## 后端：ASP.NET Core 8

#### SQL 注入防护

ASP.NET Core 通过使用参数化查询和实体框架进行数据库操作，提供了内置的 SQL 注入攻击防护。

```csharp
// Controllers/UserController.cs
using Microsoft.AspNetCore.Mvc;
using Microsoft.EntityFrameworkCore;
using System.Threading.Tasks;

[ApiController]
[Route("api/[controller]")]
public class UserController : ControllerBase
{
    private readonly ApplicationDbContext _context;

    public UserController(ApplicationDbContext context)
    {
        _context = context;
    }

    [HttpGet("{id}")]
    public async Task<IActionResult> GetUser(int id)
    {
        var user = await _context.Users.FindAsync(id);
        if (user == null)
        {
            return NotFound();
        }
        return Ok(user);
    }
}
```

#### XSS 防护

为了防止跨站脚本（XSS）攻击，ASP.NET Core 提供了自动请求验证和 HTML 编码。

```csharp
// Controllers/HomeController.cs
using Microsoft.AspNetCore.Mvc;

public class HomeController : Controller
{
    public IActionResult Index()
    {
        ViewData["Message"] = "<script>alert('XSS attack!');</script>";
        return View();
    }
}
```

```html
<!-- Views/Home/Index.cshtml -->
<div>@Html.Raw(ViewData["Message"])</div>
```

#### CSRF 防护

ASP.NET Core 提供了防伪令牌来防止跨站请求伪造（CSRF）攻击。

```csharp
// Startup.cs
public void ConfigureServices(IServiceCollection services)
{
    services.AddControllersWithViews();
    services.AddDbContext<ApplicationDbContext>(options =>
        options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));
    services.AddRazorPages();
    services.AddAntiforgery(options =>
    {
        options.HeaderName = "X-CSRF-TOKEN";
    });
}
```

```html
<!-- Views/Shared/_Layout.cshtml -->
<form id="logoutForm" asp-area="" asp-controller="Account" asp-action="Logout" method="post" class="d-none">
    <button type="submit" class="nav-link btn btn-link" style="padding: 0; border: none">Logout</button>
</form>

@inject Microsoft.AspNetCore.Antiforgery.IAntiforgery Antiforgery
<script>
    var token = '@Antiforgery.GetAndStoreTokens(HttpContext).RequestToken';
    document.cookie = 'X-CSRF-TOKEN=' + token;
</script>
```

## 前端：Angular 14

#### 安全的 API 调用

从 Angular 调用 API 时，确保使用 HTTPS，验证输入数据，并安全地处理身份验证。

```typescript
// src/app/user.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';
import { User } from './user.model';

@Injectable({
  providedIn: 'root'
})
export class UserService {
  private apiUrl = 'https://localhost:5001/api/user'; // 更新为你的 API URL

  constructor(private http: HttpClient) { }

  getUser(id: number): Observable<User> {
    return this.http.get<User>(`${this.apiUrl}/${id}`);
  }
}
```

#### 身份验证和授权

在你的 Angular 应用中使用 JWT（JSON Web Tokens）和基于角色的访问控制（RBAC）等技术来实现身份验证和授权机制。

```typescript
// src/app/auth.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root'
})
export class AuthService {
  private apiUrl = 'https://localhost:5001/api/auth'; // 更新为你的 API URL

  constructor(private http: HttpClient) { }

  login(credentials: { username: string, password: string }): Observable<any> {
    return this.http.post<any>(`${this.apiUrl}/login`, credentials);
  }

  logout(): Observable<any> {
    return this.http.post<any>(`${this.apiUrl}/logout`, {});
  }

  isAuthenticated(): boolean {
    // 检查用户是否已认证（例如，JWT 令牌是否存在）
    return true; // 占位符，实现实际逻辑
  }
}
```




# 保护 Web API 与调试全栈应用程序

保护 Web API 免受常见漏洞的侵害，对于保护您的应用程序和用户数据至关重要。通过遵循最佳实践，例如使用参数化查询防止 SQL 注入、在 ASP.NET Core 中使用自动请求验证防止 XSS 以及使用防伪令牌防止 CSRF，同时在 Angular 中使用 HTTPS、输入验证和安全的身份验证机制，您可以显著降低安全漏洞的风险，并确保更安全的用户体验。请始终关注最新的安全标准和指南，以适应不断演变的威胁并增强应用程序的安全态势。

## 第 16 章：调试和故障排除全栈应用程序

有效利用开发者工具和日志记录，对于调试和排除使用 ASP.NET Core 8 作为后端、Angular 14 作为前端构建的 Web 应用程序中的问题至关重要。在本指南中，我们将探讨如何利用开发者工具和日志技术来增强调试过程。

## 后端：ASP.NET Core 8

#### 日志配置

ASP.NET Core 提供了一个灵活的日志框架，允许开发者配置日志级别、提供程序和目标。

1.  在 `Startup.cs` 中配置日志：

    ```csharp
    // Startup.cs
    public void Configure(IApplicationBuilder app, IWebHostEnvironment env, ILoggerFactory loggerFactory)
    {
        loggerFactory.AddFile("Logs/myapp-{Date}.txt");
        if (env.IsDevelopment())
        {
            app.UseDeveloperExceptionPage();
            loggerFactory.AddDebug(LogLevel.Debug); // 在开发模式下添加调试日志
        }
        else
        {
            app.UseExceptionHandler("/Home/Error");
            loggerFactory.AddDebug(LogLevel.Information); // 在生产模式下添加信息日志
        }
        // 其他中间件配置
    }
    ```

2.  在控制器或服务中记录日志：

    ```csharp
    // Controllers/UserController.cs
    using Microsoft.Extensions.Logging;

    [ApiController]
    [Route("api/[controller]")]
    public class UserController : ControllerBase
    {
        private readonly ILogger<UserController> _logger;

        public UserController(ILogger<UserController> logger)
        {
            _logger = logger;
        }

        [HttpGet("{id}")]
        public IActionResult GetUser(int id)
        {
            _logger.LogInformation("Getting user with ID {Id}", id);
            // 处理并返回用户数据
        }
    }
    ```

## 前端：Angular 14

#### 浏览器开发者工具

可以使用 Chrome DevTools 或 Firefox Developer Tools 等浏览器开发者工具来调试 Angular 应用程序。

1.  检查元素：
    *   使用 Elements 选项卡检查 HTML 元素及其样式。
    *   直接在浏览器中调试 CSS 和布局问题。

2.  控制台日志：
    *   利用 `console.log()`、`console.debug()`、`console.error()` 等来记录消息和调试 JavaScript 代码。

3.  网络监控：
    *   监控网络请求和响应，以调试 API 交互并识别性能瓶颈。

#### Angular 日志服务

在 Angular 中创建一个日志服务，以处理应用程序不同部分的日志记录。

1.  日志服务：

    ```typescript
    // src/app/logger.service.ts
    import { Injectable } from '@angular/core';

    @Injectable({
      providedIn: 'root'
    })
    export class LoggerService {
      log(message: string): void {
        console.log(`[INFO] ${message}`);
      }

      error(message: string): void {
        console.error(`[ERROR] ${message}`);
      }

      debug(message: string): void {
        console.debug(`[DEBUG] ${message}`);
      }
    }
    ```

2.  在组件或服务中使用：

    ```typescript
    // src/app/user/user.service.ts
    import { Injectable } from '@angular/core';
    import { LoggerService } from '../logger.service';

    @Injectable({
      providedIn: 'root'
    })
    export class UserService {
      constructor(private logger: LoggerService) { }

      getUser(id: number): void {
        this.logger.log(`Fetching user with ID ${id}`);
        // API 调用和其他逻辑
      }
    }
    ```

### 有效的调试实践

1.  使用断点：
    *   在代码中设置断点以暂停执行，并检查变量和状态。
    *   在 Visual Studio 或 VS Code 中调试服务器端代码，在浏览器开发者工具中调试客户端代码。

2.  日志记录最佳实践：
    *   记录相关信息，如输入参数、方法调用和错误，以跟踪应用程序流程并识别问题。
    *   根据消息的严重性，适当使用不同的日志级别（info、debug、error）。

3.  测试和重现问题：
    *   在开发或预发布环境中重现报告的问题，以便有效调试。
    *   编写单元测试和集成测试，以捕获和防止回归问题。

4.  持续监控：
    *   在生产环境中监控应用程序日志、性能指标和错误报告，以主动识别和修复问题。

通过利用浏览器控制台等开发者工具、日志服务以及在 ASP.NET Core 中正确配置日志，您可以简化调试过程，并确保构建一个健壮可靠的 Web 应用程序。调试是一个持续的过程，因此请根据反馈和经验不断迭代和改进您的调试实践。

### 识别常见错误和故障排除策略

识别常见错误并实施有效的故障排除策略，对于维护和提高使用 ASP.NET Core 8 作为后端、Angular 14 作为前端构建的 Web 应用程序的可靠性至关重要。让我们深入探讨一些常见错误以及在两种环境中排除这些错误的策略。

## 后端：ASP.NET Core 8

**常见错误**

1.  HTTP 500 内部服务器错误：
    *   由于服务器端问题（如未处理的异常或配置错误的中间件）而发生。

2.  数据库连接错误：
    *   数据库连接、身份验证或查询错误的问题。

3.  依赖注入错误：
    *   与依赖注入配置或服务注册相关的问题。

**故障排除策略**

1.  日志记录和异常处理：
    *   使用日志记录来跟踪应用程序流程并识别错误。实现结构化异常处理，以优雅地捕获和处理异常。

    ```csharp
    // Startup.cs
    public void Configure(IApplicationBuilder app, IWebHostEnvironment env, ILoggerFactory loggerFactory)
    {
        if (env.IsDevelopment())
        {
            app.UseDeveloperExceptionPage();
        }
        else
        {
            app.UseExceptionHandler("/Home/Error");
        }
        loggerFactory.AddFile("Logs/myapp-{Date}.txt");
        // 其他中间件配置
    }
    ```

2.  数据库连接调试：
    *   检查数据库连接字符串、凭据，并确保数据库服务器正在运行。
    *   使用日志记录和 try-catch 块来处理与数据库相关的异常。

    ```csharp
    // Services/UserService.cs
    public class UserService
    {
        private readonly ApplicationDbContext _context;

        public UserService(ApplicationDbContext context)
        {
            _context = context;
        }

        public async Task<User> GetUserByIdAsync(int id)
        {
            try
            {
                return await _context.Users.FindAsync(id);
            }
            catch (Exception ex)
            {
                _logger.LogError(ex, "Error fetching user from database.");
                throw;
            }
        }
    }
    ```

3.  依赖注入问题：
    *   仔细检查 `Startup.cs` 中的服务注册。
    *   使用构造函数注入，并确保依赖项被正确注入。

    ```csharp
    // Startup.cs
    public void ConfigureServices(IServiceCollection services)
    {
        services.AddDbContext<ApplicationDbContext>(options =>
            options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));
        services.AddTransient<IUserService, UserService>();
        // 其他服务注册
    }
    ```



## 前端：Angular 14

## 常见错误

1.  **JavaScript 运行时错误：**
    *   TypeScript 或 JavaScript 代码中的语法错误、未定义变量或方法未找到错误。

2.  **Angular 模板错误：**
    *   与模板语法相关的错误、绑定错误或缺失组件。

3.  **网络错误：**
    *   API 调用中的错误、CORS 问题或不正确的 URL 配置。

## 故障排除策略

1.  **浏览器开发者工具：**
    *   使用浏览器开发者工具（Chrome DevTools、Firefox Developer Tools）检查 JavaScript 错误、网络请求和控制台日志。

2.  **Angular CLI 调试：**
    *   利用 Angular CLI 命令，如 `ng serve --aot` 进行提前编译，以及 `ng build --prod` 进行生产构建，以尽早发现潜在错误。

3.  **调试 TypeScript：**
    *   使用 `console.log()` 语句记录变量值并跟踪代码执行。
    *   利用浏览器断点，在调试器中单步执行代码。

4.  **处理 API 错误：**
    *   在 Angular 服务中为 API 调用实现错误处理，使用 RxJS 操作符如 `catchError` 和 `retry`。

```typescript
// src/app/user/user.service.ts
import { Injectable } from '@angular/core';
import { HttpClient, HttpErrorResponse } from '@angular/common/http';
import { Observable, throwError } from 'rxjs';
import { catchError } from 'rxjs/operators';

@Injectable({
  providedIn: 'root'
})
export class UserService {
  private apiUrl = 'https://api.example.com/users'; // Update with your API URL

  constructor(private http: HttpClient) { }

  getUser(id: number): Observable<User> {
    return this.http.get<User>(`${this.apiUrl}/${id}`).pipe(
      catchError((error: HttpErrorResponse) => {
        console.error('API Error:', error);
        return throwError('Something went wrong.');
      })
    );
  }
}
```

识别常见错误并实施有效的故障排除策略，对于维护 ASP.NET Core 8 和 Angular 14 Web 应用程序的可靠性和性能至关重要。通过使用日志记录、异常处理、浏览器开发者工具和调试技术，开发人员可以快速诊断问题、追踪错误并高效地实施解决方案。持续监控、测试以及紧跟最新框架和最佳实践是提高 Web 应用程序整体质量和健壮性的关键。

# 第 17 章：持续集成与持续交付 (CI/CD)

自动化构建和部署是现代软件开发的一个关键方面，它有助于确保一致的发布、简化开发工作流程并提高整体生产力。在本指南中，我们将探讨如何使用流行的工具和实践，为使用 ASP.NET Core 8 作为后端、Angular 14 作为前端构建的 Web 应用程序自动化构建和部署。

## 后端：ASP.NET Core 8

### 持续集成与持续部署 (CI/CD)

1.  **设置 CI/CD 流水线：**
    *   使用 CI/CD 平台，如 Azure DevOps、GitHub Actions 或 Jenkins 来自动化构建和部署过程。

2.  **CI 流水线：**
    *   配置 CI 流水线，以便在每次代码提交或拉取请求时构建、测试和打包你的 ASP.NET Core 应用程序。

```yaml
# azure-pipelines.yml
trigger:
  branches:
    include:
      - main
      - development

pool:
  vmImage: 'windows-latest'

jobs:
  - job: Build
    steps:
      - task: DotNetCoreCLI@2
        inputs:
          command: 'build'
          projects: '**/*.csproj'
          arguments: '--configuration Release'
      - task: DotNetCoreCLI@2
        inputs:
          command: 'test'
          projects: '**/*Tests.csproj'
          arguments: '--configuration Release'
      - task: DotNetCoreCLI@2
        inputs:
          command: 'publish'
          publishWebProjects: true
          arguments: '--configuration Release --output $(Build.ArtifactStagingDirectory)/publish'
      - task: PublishPipelineArtifact@1
        inputs:
          targetPath: '$(Build.ArtifactStagingDirectory)/publish'
          artifact: 'publish'
```

3.  **CD 流水线：**
    *   配置 CD 流水线，将构建的工件部署到你的目标环境（例如 Azure App Service、Docker 等）。

```yaml
# azure-pipelines.yml (CD section)
- deployment: Deploy
  pool:
    vmImage: 'windows-latest'
  environment: 'production'
  strategy:
    runOnce:
      deploy:
        steps:
          - task: AzureWebApp@1
            inputs:
              azureSubscription: 'AzureSubscription'
              appName: 'YourApp'
              package: $(Pipeline.Workspace)/publish/*.zip
              deploymentMethod: 'zipDeploy'
```

## 前端：Angular 14

### 自动化构建与部署

1.  **Angular CLI 构建：**
    *   使用 Angular CLI 命令来构建和打包你的 Angular 应用程序。

```bash
ng build --prod
```

2.  **自动化部署：**
    *   使用 CI/CD 平台或脚本来自动化你的 Angular 应用程序的部署。

```yaml
# Example GitHub Actions workflow for Angular deployment
name: Angular Deployment

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Setup Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14'
      - name: Install Angular CLI
        run: npm install -g @angular/cli
      - name: Build Angular App
        run: ng build --prod
      - name: Deploy to GitHub Pages
        uses: JamesIves/github-pages-deploy-action@4.1.2
        with:
          ACCESS_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          BRANCH: gh-pages
          FOLDER: dist/your-angular-app
```

### 自动化构建与部署的好处

1.  **一致性：**
    *   自动化确保跨环境的构建和部署一致，减少人为错误和配置漂移。

2.  **效率：**
    *   开发人员可以更专注于编码，减少手动构建和部署任务，从而加快发布周期。

3.  **可靠性：**
    *   自动化测试和部署流水线有助于尽早发现问题，并确保可靠的发布过程。

4.  **可扩展性：**
    *   随着应用程序和团队的增长，自动化可以无缝扩展，以处理增加的复杂性和工作量。

为 ASP.NET Core 8 和 Angular 14 应用程序自动化构建和部署是一项最佳实践，它能提高开发效率、减少错误，并实现更快、更可靠的发布。通过利用 CI/CD 平台、版本控制系统和脚本工具，团队可以建立一个强大的持续集成、测试和部署流水线，最终自信且一致地向用户交付高质量的软件。将这些自动化实践融入你的开发工作流程，以简化流程并提高整个开发团队的生产力。

# 使用 Azure DevOps 等工具实施 CI/CD 流水线

实施持续集成与持续部署 (CI/CD) 流水线对于自动化使用 ASP.NET Core 8 作为后端、Angular 14 作为前端构建的 Web 应用程序的构建、测试和部署过程至关重要。在本指南中，我们将重点介绍如何使用 Azure DevOps（一个用于管理整个软件开发生命周期的流行工具）来设置 CI/CD 流水线。

## 后端：ASP.NET Core 8

### 在 Azure DevOps 中为 ASP.NET Core 设置 CI/CD

1.  **创建 Azure DevOps 项目：**
    *   登录 Azure DevOps 并为你的 ASP.NET Core 应用程序创建一个新项目。

2.  **创建构建流水线：**
    *   导航到 Pipelines > Builds 并创建一个新的流水线。
    *   选择你的代码仓库并选择 ASP.NET Core 模板。
    *   配置构建步骤，如还原包、构建解决方案、运行测试和发布工件。

```yaml
# azure-pipelines.yml
trigger:
  - main

pool:
  vmImage: 'windows-latest'

steps:
  - task: DotNetCoreCLI@2
    inputs:
      command: 'restore'
      projects: '**/*.csproj'
  - task: DotNetCoreCLI@2
    inputs:
      command: 'build'
      projects: '**/*.csproj'
      arguments: '--configuration Release'
  - task: DotNetCoreCLI@2
    inputs:
      command: 'test'
      projects: '**/*Tests.csproj'
      arguments: '--configuration Release'
  - task: DotNetCoreCLI@2
    inputs:
      command: 'publish'
      publishWebProjects: true
      arguments: '--configuration Release --output $(Build.ArtifactStagingDirectory)/publish'
  - task: PublishBuildArtifacts@1
    inputs:
      pathtoPublish: '$(Build.ArtifactStagingDirectory)/publish'
```




## 在 Azure DevOps 中为 Angular 设置 CI/CD

### 1. 创建 Azure DevOps 项目：

*   如果你还没有，请为你的 Angular 应用程序创建一个新的 Azure DevOps 项目。

### 2. 创建构建管道：

*   与 ASP.NET Core 管道类似，为你的 Angular 应用程序创建一个构建管道。
*   使用 Angular CLI 命令来构建和打包你的应用程序。

```yaml
# azure-pipelines.yml for Angular
trigger:
- main

pool:
  vmImage: 'ubuntu-latest'

steps:
- task: NodeTool@0
  inputs:
    versionSpec: '14.x'
    checkLatest: true
- script: npm install -g @angular/cli
  displayName: 'Install Angular CLI'
- script: npm install
  displayName: 'Install npm dependencies'
- script: ng build --prod
  displayName: 'Build Angular app'
- task: PublishBuildArtifacts@1
  inputs:
    pathtoPublish: '$(Build.SourcesDirectory)/dist'
    artifactName: 'angular-app'
```

### 3. 创建发布管道：

*   与 ASP.NET Core 发布管道类似，为你的 Angular 应用程序创建一个发布管道。
*   配置部署任务，将 Angular 构件部署到所需的托管环境（例如，Azure App Service、GitHub Pages）。

## 使用 Azure DevOps 进行 CI/CD 的优势

### 1. 自动化：

*   CI/CD 管道自动化了重复性任务，包括构建、测试和部署代码变更，为开发者节省了时间和精力。

### 2. 一致性：

*   自动化管道确保了构建和部署过程的一致性，减少了人为错误，并确保了可靠的发布。

### 3. 可见性和可追溯性：

*   Azure DevOps 提供了对整个开发生命周期的可见性，从代码变更到部署，并提供详细的日志和指标。

### 4. 可扩展性：

*   随着应用程序的增长，CI/CD 管道可以无缝扩展，以处理增加的工作负载和复杂的部署场景。

为 ASP.NET Core 8 和 Angular 14 应用程序使用 Azure DevOps 实施 CI/CD 管道是现代软件开发的最佳实践。通过自动化构建、测试和部署流程，团队可以实现更快的发布周期，提高代码质量，并向用户交付可靠的软件。Azure DevOps 提供了一个全面的平台来管理工作流，与版本控制、构建自动化、测试框架和部署目标无缝集成。将这些实践融入你的开发工作流，以简化流程并提高开发团队的效率。

## 第 18 章：全栈开发的未来

截至我上次训练数据截止日期 2022 年，我可以提供截至该时间点 ASP.NET Core 和 Angular 新兴趋势的见解。请记住，此后技术格局可能已经演变，因此我将重点关注截至该时期的趋势。

### ASP.NET Core

1.  **微服务架构：** 由于其轻量级和模块化的特性，ASP.NET Core 在微服务架构中的使用日益增多。这一趋势允许开发者构建和部署小型、独立的服务，这些服务可以更高效地进行扩展和维护。
2.  **容器化和 Kubernetes：** 使用 Docker 进行容器化和使用 Kubernetes 进行编排已成为 ASP.NET Core 开发中的流行趋势。这些技术使得应用程序的部署、扩展和管理变得容易，增强了跨不同环境的可移植性。
3.  **无服务器计算：** 无服务器架构已获得关注，ASP.NET Core 应用程序可以使用 Azure Functions 或 AWS Lambda 等平台部署为无服务器函数。这一趋势促进了成本效益、可扩展性和事件驱动架构。
4.  **实时通信：** 随着实时应用程序的兴起，ASP.NET Core SignalR 已成为在 Web 应用程序中实现实时通信功能（如聊天、通知和实时更新）的热门选择。
5.  **GraphQL 集成：** 虽然 RESTful API 仍然广泛使用，但 GraphQL 因其在数据获取方面的灵活性和效率而受到关注。ASP.NET Core 拥有库和工具，可以将 GraphQL 端点集成到应用程序中，提供对数据查询的更多控制。

### Angular

1.  **Angular Elements：** 微前端和可重用组件的趋势导致了 Angular Elements 的采用。此功能允许开发者将 Angular 组件打包为自定义元素，这些元素可以在非 Angular 环境或其他框架中使用。
2.  **状态管理：** 复杂的应用程序通常需要强大的状态管理解决方案。虽然 Angular 提供了其内置机制（如 RxJS 和服务），但像 NgRx（使用 Redux 原则）这样的外部库因其能够以更结构化和可扩展的方式管理应用程序状态而日益流行。
3.  **服务端渲染 (SSR)：** 使用 Angular Universal 进行 SSR 已成为一种趋势，用于提高初始加载性能、优化搜索引擎索引并增强用户体验，特别是对于内容丰富或对 SEO 敏感的应用程序。
4.  **PWA 支持：** 渐进式 Web 应用程序 (PWA) 持续成为一种趋势，Angular 提供了构建 PWA 的功能和最佳实践，包括服务工作者、应用清单和离线功能。
5.  **TypeScript 和 JavaScript 生态系统：** TypeScript 作为 Angular 开发的主要语言，由于其强类型、增强的开发者体验以及与现代 JavaScript 特性的兼容性，其受欢迎程度持续增长。

### 代码片段示例

对于 ASP.NET Core：

```csharp
// Startup.cs - Example of configuring SignalR
public void ConfigureServices(IServiceCollection services)
{
    services.AddSignalR();
}

public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
{
    // Other middleware configurations
    app.UseEndpoints(endpoints =>
    {
        endpoints.MapHub<ChatHub>("/chatHub");
    });
}
```

对于 Angular：

```typescript
// app.module.ts - Example of NgRx setup
import { StoreModule } from '@ngrx/store';
import { reducers } from './store';

@NgModule({
  imports: [
    StoreModule.forRoot(reducers)
  ],
  declarations: [
    AppComponent
  ],
  bootstrap: [AppComponent]
})
export class AppModule { }
```





这些趋势反映了现代开发实践的持续演进与采用，旨在提升 ASP.NET Core 和 Angular 应用程序的性能、可扩展性以及开发者体验。请关注最新版本发布、社区讨论和最佳实践，以便在项目中有效利用这些趋势。

## 保持对最新技术的了解

对于使用 ASP.NET Core 8 和 Angular 14 的开发者而言，保持对最新技术的了解至关重要，这有助于他们利用新功能、提升性能、确保安全，并在快速发展的技术环境中保持竞争力。以下是一些保持对这些框架最新技术了解的策略和资源：

### ASP.NET Core 8

1.  **官方文档：**
    ASP.NET Core 官方文档是学习新功能、最佳实践和更新的绝佳资源。它涵盖了从入门指南到高级主题和 API 的广泛内容。

2.  **社区博客和论坛：**
    关注 ASP.NET Core 专家、微软开发者和社区成员的博客、论坛和社交媒体频道。Stack Overflow、GitHub 讨论区和 Reddit 等网站非常适合获取最新信息和寻求帮助。

3.  **Microsoft Learn 和 Channel 9：**
    Microsoft Learn 提供关于 ASP.NET Core 和其他微软技术的交互式学习路径、模块和实践实验室。Channel 9 提供与 ASP.NET Core 更新和创新相关的视频教程、网络研讨会和活动。

4.  **GitHub 仓库：**
    探索与 ASP.NET Core 相关的 GitHub 仓库，以发现新的库、工具和社区驱动的项目。参与开源项目，贡献代码并从他人那里学习。

5.  **在线课程和研讨会：**
    报名参加微软、Pluralsight、Udemy、Coursera 等教育平台，或通过本地技术社区和聚会提供的在线课程、研讨会和认证。

### Angular 14

1.  **官方 Angular 博客和文档：**
    官方 Angular 博客和文档是了解 Angular 新版本发布、更新、功能和主要信息来源。它们涵盖了从核心概念到高级技术的所有内容。

2.  **Angular GitHub 仓库：**
    关注 Angular GitHub 仓库，以跟踪 Angular 团队和社区的问题、发布和贡献。参与讨论并为框架的开发做出贡献。

3.  **社区聚会和会议：**
    参加本地的 Angular 聚会、会议和网络研讨会，与其他开发者建立联系，了解行业趋势，并向专家演讲者学习。ng-conf 和 AngularConnect 等活动提供了宝贵的见解。

4.  **在线学习平台：**
    在 Pluralsight、Udemy、LinkedIn Learning 和 Coursera 等平台上报名参加 Angular 课程，以保持技能更新并了解 Angular 版本中引入的新功能。

5.  **Angular CLI 和 DevTools：**
    熟悉`Angular CLI`命令和开发者工具（如用于调试、分析和优化 Angular 应用程序的 Augury）。探索更新中引入的新 CLI 功能和优化。

## 示例代码片段

ASP.NET Core 示例：

```csharp
// 使用新 C#功能（C# 8 及以上）的示例
public class Person
{
    public string Name { get; set; }
    public int? Age { get; set; }
    public string Greet() => $"Hello, {Name}!";
}
```

Angular 示例：

```typescript
// 使用 Angular 12+功能（如带 else 语法的 ngIf）的示例
<div *ngIf="user; else loading">
    <p>Welcome, {{ user.name }}!</p>
</div>
<ng-template #loading>
    <p>Loading...</p>
</ng-template>
```





# 结论

总而言之，ASP.NET Core 8 与 Angular 14 的结合，为构建健壮、可扩展且功能丰富的 Web 应用程序提供了一个强大而现代的框架栈。在本次探索中，我们深入研究了这些技术的各个方面，从构建具有离线功能的渐进式 Web 应用程序（PWA），到实施安全最佳实践、利用 SignalR 进行实时通信，以及设置用于自动化构建和部署的 CI/CD 流水线。

ASP.NET Core 8 凭借其跨平台能力、高性能架构以及丰富的库和工具生态系统，为开发者提供了灵活高效的后端开发环境。无论是处理 HTTP 请求、管理数据库、实施身份验证，还是与第三方服务集成，ASP.NET Core 都提供了必要的工具和框架来简化开发工作流程并交付高质量的应用程序。

在前端方面，Angular 14 以其基于组件的架构、强大的数据绑定以及用于构建动态交互式用户界面的丰富功能集而大放异彩。借助 Angular Elements 用于微前端、使用 NgRx 进行状态管理以及服务器端渲染（SSR）等功能，Angular 赋能开发者创建响应迅速、可扩展且易于维护的现代 Web 应用程序。

随着技术的不断发展，开发者紧跟最新趋势、最佳实践和创新至关重要。无论是探索微服务、容器化、无服务器计算等新兴趋势，还是采用 ASP.NET Core 和 Angular 更新中引入的新功能和优化，持续学习和适应都是保持竞争力并交付前沿解决方案的关键。

此外，拥抱协作、知识共享和社区参与的文化能够提升开发旅程。利用官方文档、社区论坛、在线课程、聚会和会议等资源，不仅能让开发者保持信息更新，还能培育一个支持性强、充满活力的生态系统，在这个系统中，创意得以蓬勃发展，挑战得以克服，技能得以磨练。

本质上，ASP.NET Core 8 与 Angular 14 之间的协同作用，赋能开发者应对复杂挑战，交付卓越的用户体验，并在不断演变的 Web 开发领域推动创新。通过充分利用这些技术的全部潜力，开发者可以构建满足当今用户需求的现代 Web 应用程序，同时为数字领域未来的进步和可能性铺平道路。

# 附录

## A：术语表

以下是与 ASP.NET Core 8 和 Angular 14 相关的术语表，旨在帮助理解这些技术中使用的关键概念和术语：

### ASP.NET Core 8 术语表

1.  **ASP.NET Core**：一个跨平台、高性能的框架，用于构建现代、基于云和互联的应用程序。
2.  **中间件**：ASP.NET Core 管道中处理请求和响应的组件，例如身份验证、路由和错误处理。
3.  **路由**：根据 URL 模式将传入的 HTTP 请求映射到应用程序中特定操作或端点的过程。
4.  **依赖注入（DI）**：ASP.NET Core 中的一种设计模式，其中依赖项被注入到类中，而不是在类本身内部实例化，从而促进松散耦合和可测试性。
5.  **Entity Framework Core（EF Core）**：一个用于 .NET Core 的对象关系映射（ORM）框架，使开发者能够使用 C# 对象与数据库交互，提供数据库访问和管理功能。
6.  **模型-视图-控制器（MVC）**：ASP.NET Core 中使用的一种设计模式，用于将关注点分离为模型（数据）、视图（UI）和控制器（逻辑），促进代码组织和可维护性。
7.  **中间件管道**：HTTP 请求流经的一系列中间件组件，允许开发者在请求处理的各个阶段添加、移除或修改行为。
8.  **Razor Pages**：ASP.NET Core 中 MVC 的一种轻量级替代方案，用于以更简单、更专注的方式构建网页，非常适合以页面为中心的应用程序。
9.  **身份验证和授权**：在 ASP.NET Core 应用程序中，基于用户角色或策略验证用户身份（身份验证）和授予访问权限（授权）的过程。
10. **日志记录和诊断**：ASP.NET Core 中的内置日志功能，用于捕获运行时信息、错误和性能指标，便于故障排除和监控。

### Angular 14 术语表

1.  **Angular**：一个基于 TypeScript 的开源框架，用于构建客户端 Web 应用程序，由 Google 维护。
2.  **组件**：Angular 中可复用的构建块，封装了 HTML 模板、逻辑和样式，促进模块化和可复用性。
3.  **指令**：Angular HTML 模板中的特殊标记，用于修改 DOM 元素的行为或外观，例如 `*ngIf`、`*ngFor` 和自定义指令。
4.  **模块**：Angular 中的容器，用于将相关的组件、指令、管道和服务分组，促进应用程序的组织和模块化。
5.  **服务**：Angular 中的单例对象，用于封装可复用逻辑、数据获取以及组件间的通信。
6.  **数据绑定**：Angular 中用于在组件类及其模板之间同步数据的机制，包括单向绑定（`{{ }}`）和双向绑定（`[(ngModel)]`）。
7.  **路由**：在 Angular 应用程序中，基于 URL 更改在不同视图或组件之间导航的过程，由 Angular Router 提供支持。
8.  **表单**：Angular 提供模板驱动和响应式两种表单，用于处理应用程序中的用户输入、表单验证和表单提交。
9.  **插值**：Angular 中使用 `{{ }}` 语法在 HTML 模板中显示动态值或表达式的数据绑定技术。
10. **NgRx**：一个基于 Redux 原则的 Angular 应用程序状态管理库，支持集中的状态管理、操作、reducer 和 effect。

理解这些术语和概念对于使用 ASP.NET Core 8 和 Angular 14 的开发者至关重要，因为它们构成了构建现代和可扩展 Web 应用程序的基础。持续探索和掌握这些技术及其相关术语，使开发者能够充分利用其潜力，并交付满足用户和业务需求的高质量解决方案。

