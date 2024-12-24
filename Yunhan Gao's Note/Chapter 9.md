# Ch9-Software Evolution
## Handover Problems
1. 开发团队已经使用了敏捷方法，但是演进团队不熟悉敏捷方法，更喜欢基于计划的方法。（演进团队期望更多细节的文档，敏捷开发不提供）
2. 开发团队使用基于计划的方法，演进团队更喜欢敏捷方法。（演进团队要重新开发，***自动测试***和代码没有按照敏捷方法的要求***重构和简化***）
## Software Maintenance
### Reengineering
>Restructuring or rewriting part or all of a legacy system without changing its functionality.

Advantages:
- Reduced risk
- Reduced cost

### Refactoring 
>The process of making improvements to a program to slow down degradation through change.
### Refactoring VS Reengineering
**Reengineering:**
在系统维护了一段时间后，维护成本在提升时，使用自动化工具创建新系统。

**Refactoring:**
重构是贯穿开发和演化过程的持续改进过程。它的目的是避免结构和代码退化，从而增加维护系统的成本和困难。