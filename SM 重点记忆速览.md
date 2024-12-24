# SM 重点记忆速览

## 6-Architectural Design

### 4 +1视图模型

1. Logic View: 系统功能需求，描述系统的静态结构。（类图）
2. Process View：系统运行的动态行为。（时序图）
3. Development View：系统模块化结构和代码组织。（包图）
4. Physical View：系统硬件和软件组件部署结构。（部署图）
5. Scenario View：使用用例将上述四种视图连接。（用例图）

### 架构模式（给特定情景，选出对应的架构模式）

**Pipe-and-Filter**

类似流水线工作模式，将系统分为 **过滤器** 和 **管道**。每个过滤器负责处理一件任务，将处理后的任务它通过管道传到下一个过滤器执行下一个任务。

**Client-server Architecture**

**客户端**发起请求，**服务端**处理请求并返回结果。在这个架构中，系统中的功能被组织为服务，通过调用不同的服务端执行。

**Event-based Architecture**

系统组件通过事件进行通信。某个组件发生变化，会触发一个事件，其他对这个事件感兴趣的组件对其变化进行响应。在运动日历安卓项目中，对应时区改变，全局重新响应。核心思想是一个发布-订阅模型

**Layered Architecture**

将系统分为不同的层，每一层处理特定的职责。上层可以调用下层功能，下层不依赖上层。

**Repository Architecture**

通过一个仓库来组织和管理数据，系统中的所有组件通过改仓库进行通信和交互。

**Model-View-Controller Architecture**

| Name         | MVC                                                          |
| ------------ | ------------------------------------------------------------ |
| Description  | Separates presentation and interaction ftom the system data.<br />**Model**: Manages data and operations.<br />**View**: Displays the data.<br />**Controller**: Handles user inputs and updates Model and View. |
| When to Use  | When the same data needs different presentations.<br />When future interaction or presentation needs are unclear. |
| Advantages   | Data and its display can change independently.<br />Same data can have various representations, all kept in sync. |
| Disadvantage | For simple systems, MVC might add unnecessary code and complexity. |

###Architectural Design Decisions

- Perfomance: Localize critical operations; MInimize communications; Use large-grain components.
- Security: Protect critical assets in inner layers.
- Availability: Use fault-tolerance mechanisms.
- Maintainability: Use fine-grain, replaceable components.



## 7- Design and Implementation

### OOD Principles (SOLID)

**Single Responsibility Principle**

每个类只有一个职责。

**Open Closed Principle**

实体对扩展开放，对修改封闭

**Liskov Substitution Principle**

子类必须能够替换其基类而不影响程序的正确性。子类应该继承父类的所有行为，而不改变其功能。

**Interface Segregation Principle**

一个类不应该依赖于它不使用的接口。

**Dependencey Inversion Principle**

High-level modules should not depend on low-level modules. Both should depend on abstractions. 具体实现（类）应该依赖于接口或抽象类，而不是直接依赖于其他具体实现。

### Refactoring 概念

Refactoring is a systematic process of improving code without creating new functionality that can transform a mess into clean code and simple design.

### 六种重构技术

- Composing Methods
- Moving Features between Objects
- Organizing Data
- Simplifying Conditional Expressions
- Simplifying Method Calls
- Dealing with Generalization

### Reuse Levels

- Abstaction Level: Reuse design ideas and abstractions, not actual code.
- Object Level: Directly reuse objects or code from libraries.
- Component Level: Reuse collections of objects or classes as components.
- System Level: Reuse entire application systems.

### Open Source Licensing

源代码免费提供，但是不意味着所有人可以随意使用

- GNU General Public License (GPL)

  用了GPL代码，你的软件也必须GPL

- GNU Lesser General Public License (LGPL)

  使用 LGPL 代码时，只要不修改原代码，你的项目可以不用开源。

- Berkeley Standard Distribution (BSD) License

  BSD 代码可以自由使用，不强制开源修改内容。

## 8- Software Testing

### Defect Clustering VS Pesticide Paradox

缺陷聚集指的是，在一个软件应用中，大部分缺陷（错误）集中在少量的模块中。

杀虫剂悖论指的是，如果长时间使用**同一组测试用例**进行测试，这些测试用例可能无法发现新的缺陷。

### Static Testing VS Dynamic testing

静态测试是在**不运行程序**的情况下，对代码、文档或设计进行检查。

动态测试是在**运行软件程序**的情况下，测试软件的行为和功能。

### White Box Testing(控制流图)

**白盒测试**是一种基于代码实现的测试方法，测试人员需要了解程序的内部逻辑和代码结构，通过检查代码的逻辑路径、条件分支、循环等，来验证程序是否按照预期工作。

<img src="E:/WeChat%20Files/wxid_l2ot4hx7gopw22/FileStorage/Temp/84b5c604254f819c3ac01ccc21e601d.jpg" alt="84b5c604254f819c3ac01ccc21e601d" style="zoom:25%;" />

<img src="E:/WeChat%20Files/wxid_l2ot4hx7gopw22/FileStorage/Temp/36e53d20577a6f5bc61710edb6cf747.jpg" alt="84b5c604254f819c3ac01ccc21e601d" style="zoom:25%;" />

决策判定：每个if语句都有T/F

条件判定：每个> < != ==都要判定

### Black Box Testing(等价类划分)

**有效等价类**：是输入值的有效范围内，程序应该正确处理的输入数据。

**无效等价类**：是输入值的无效范围内，程序应该拒绝或处理异常的输入数据。

### 黑盒 VS 白盒

| Black                                            | White                                          |
| ------------------------------------------------ | ---------------------------------------------- |
| Tests **external behavior** (input-output)       | Tests **internal logic** and code structure.   |
| No programming knowledge required                | Requires programming knowledge.                |
| Ideal for **System** and **Acceptance Testing**. | Best for **Unit** and **Integration Testing**. |
| Done by **end users, testers, or developers**.   | Done by **testers or developers**.             |
| **Faster** and less exhaustive.                  | **Slower** and more detailed.                  |

### Development Testing

- Unit Testing: Tests individual program units or object classes.
- Integration Testing: Tests **groups of software modules** when combined.
- System Testing: Tests the **entire integrated system**.



### 集成测试

**Integration Testing** checks how different software modules work together when combined. The goal is to ensure that the interaction between the modules is correct and functional

### 集成测试 VS 系统测试

| Integration                                             | System                                            |
| ------------------------------------------------------- | ------------------------------------------------- |
| Tests module **interactions**                           | Tests the **entire system** against requirements. |
| After **Unit Testing**, whenever a new module is added. | After **Integration Testing**, before UAT.        |
| **Low-level** testing.                                  | **High-level** testing.                           |
| Tests **interfaces** between components.                | Simulates **real-world scenarios**.               |



### 用户测试的类型（理解）

- Alpha 测试

  用户和开发人员一起，在开发环境进行早期测试

- Beta 测试

  发行软件的预发布版本，允许用户真实测试并反馈问题

- Acceptance testing 验收测试

  用户测试的**最后阶段**，由客户决定软件是否准备好投入使用。

  重点在于检查软件是否符合**指定的需求**。

## 9- Software Evolution

### Reengineering

Reengineering involves **restructuring or rewriting** parts of a legacy system **without changing functionality**, to make it easier to maintain.

优点：

- Reduced Risk
- Reduced Cost



### Refactoring

Refactoring is the process of improving a program's **structure and readability** without changing its functionality. It acts as **preventative maintenance** to reduce future issues caused by changes.

### refactoring vs Reengineering

| Refactoring                                | Reengineering                                        |
| ------------------------------------------ | ---------------------------------------------------- |
| Continuous improvement during development. | Done after prolonged maintenance when costs rise.    |
| Prevents code and structure degradation.   | Modernizes legacy systems to improve maintainability |
| Usually manual or with lightweight tools.  | Uses automated tools to transform the system.        |
| Small, incremental changes                 | Large-scale system overhaul.                         |

### Handover Problem

- 开发团队使用agile approach；evolution team使用planed-based approach. 
- 开发团队使用plan-based approach；evolution team使用agile approach

### 根据不同情况选择适应的Legacy System处理方式

- Low quality, low business value: Scrapped 废除
- Low-quality, high-business value；Re-engineered or replaced
- High-quality, low-business value: Scrap or maintain
- High-quality, high business value: Continue in operation using normal system maintenance
