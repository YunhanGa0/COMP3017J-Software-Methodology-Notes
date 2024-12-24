# Ch7-Design and Implementation
## SOLID (给例子问违反了哪个)
### Single Responsibility Principle (每个类只能有一个责任)
- **Each class should have only one responsibility**, meaning it should do one thing and do that thing well.
### Open Closed Principle (向扩展开放，向更改关闭)
- Software components should be open for extension but closed for modification.
### Liskov Substitution Principle (子类型必须能够完全替换其父类型！)
- Subtypes must be substitutable for their base types without having to alter the base type.
### Interface Segregation Principle (使用接口的对象可以自由选择使用的内容)
- Clients should not be forced to depend on properties and methods that they do not use.
### Dependency Inversion Principle (高层模块与底层模块分离，使它们都依赖于抽象，而不是具体实现)
- High-level modules should not depend on low-level modules. Both should depend on abstractions.
- Abstractions should not depend on details. Details should depend on abstractions.

## Reuse Levels (四个等级要背)
### The abstraction level
- At this level, you don’t reuse software directly but use knowledge of successful abstractions in the design of your software.
### The object level (复用对象)
- At this level, you directly reuse objects from a library rather than writing the code yourself.
### The component level (复用的对象和对象类的集合)
- Components are collections of objects and object classes that you reuse in application systems.
### The system level (复用整个系统)
- At this level, you reuse entire application systems.

## Open Source Licensing
| **许可证**   | **是否强制开源衍生作品** | **是否允许闭源使用** | **适用场景**                             |
|--------------|--------------------------|---------------------|-----------------------------------------|
| **GPL**      | 是                       | 否                  | 如果你希望保护代码的开源性，并强制所有衍生作品也保持开源            |
| **LGPL**     | 仅库部分强制             | 是                  | 如果你的项目是一个库，想要广泛传播，但又希望允许商业闭源软件使用          |
| **BSD**      | 否                       | 是                  | 如果你想最大限度地推广你的代码，而不关心使用者是否开源          |
