# Ch2-Software Processes
## Software Process Models (各种模型特点，优缺点，适用场景)
### Waterfall model
**Plan-driven model. Separate and distinct phases of specification and development.**
**Benefits:**
- Easy to understand and implement.
- Reinforces good habits: define-before-design, design-before-code.
- Identifies deliverables and milestones.
- Works well on mature products and weak teams.

**Problems:**
- The difficulty of accommodating change after the process is underway. In principle, a phase has to be complete before moving onto the next phase. (难以使用开发中的变化)
- This model is only appropriate when the requirements are well-understood and changes will be fairly limited during the design process. (只有充分理解需求，在设计过程中更改很少部分时才适用)

![](./Pic/屏幕截图%202024-12-21%20114122.png
)
### Prototype Model
**Def:**
A prototype is an initial version of a system used to demonstrate concepts and try out design options.
**Can be used in:**
- The requirements engineering process to help with requirements elicitation and validation
- In design processes to explore options and develop a UI design
**Benefits:**
- Improved system usability
- A closer match to users’ real needs
- Improved design quality
- Reduced development effort
![](./Pic/屏幕截图%202024-12-21%20123432.png)

### Incremental Model
**Def:**
- 不是将系统作为单个交付交付，而是将开发和交付**分解为增量**，每个增量交付所需功能的一部分。
- **用户需求优先级高**，优先级高需求包含在早期的增量中。
- 一旦开始开发增量，则需求通过稍后的需求被**冻结**，后续增量可以继续发展。

**Benefits:**
- The cost of accommodating changing customer requirements is reduced. (适应变化的成本降低)
- It is easier to **get customer feedback** on the development work that has been done.
- **More rapid delivery and deployment** of useful software to the customer is possible.
- Lower risk of overall project failure.
- The highest priority system services tend to receive the most testing.

**Problems:**
- The process is not visible, managers need regular deliverables to measure progress.
- Regular change tends to **corrupt its structure**.
- The iterative processes is developed in **conjunction of specification and software**, which is conflicts with organizations, where the complete system specification is part of the **system development contract**.

| **模型**         | **优点**                                                      | **缺点**                                                      | **使用场景**                                      |
|------------------|---------------------------------------------------------------|---------------------------------------------------------------|--------------------------------------------------|
| **瀑布模型**     | 结构清晰，阶段严格，易于管理和控制                            | 不灵活，难以适应需求变更，缺乏快速迭代                        | 需求明确且变动少，短期或小型项目，监管要求严格的行业 |
| **原型模型**     | 快速迭代、用户反馈频繁、适应需求变更                          | 可能导致低质量代码，管理困难                                  | 需求不明确或用户体验设计复杂，需求不断变化的项目   |
| **增量模型**     | 分阶段交付、灵活应对需求变更、加速开发周期                  | 初期规划不清晰可能影响后续增量，可能产生系统架构维护问题      | 长期项目，需求优先级明确，需分阶段交付的项目       |
