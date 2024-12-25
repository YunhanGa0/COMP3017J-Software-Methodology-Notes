# Ch4-Requirements Engineering
## User/System requirements
### User requirements
- Statements in natural language plus diagrams of the services the system provides and its operational constraints
### System requirements
- A structured document setting out detailed descriptions of the system’s functions, services and operational constraints. Defines what should be implemented so may be part of the contract between the system buyer and the software developers.

## Functional/Non-functional Requirements
### Functional Requirements
- Describe functionality or system services.
- **Functional user requirements** may be high-level statements of what the system should do.
- **Functional system requirements** should describe the system services in detail.

### Non-functional Requirements
- Non-functional requirements usually specify or constrain characteristics of the system as a whole. (约束)
- Non-functional requirements **may be more critical** than functional requirements. If these are not met, the system may be useless.

### Functional vs Non-functional
![](./Pic/屏幕截图%202024-12-22%20164258.png)

## Requirements Engineering Processes (三个主要活动)
Requirements engineering involves **three key activities**:
1. Discovering requirements by interacting with stakeholders **(elicitation and analysis)**
2. Converting these requirements into a standard form **(specification)**
3. Checking that the requirements actually define the system that the customer want **(validation)**

### Technique Selection
![](./Pic/屏幕截图%202024-12-22%20164743.png)

## Use case diagram

### IEEE 830 and User Stories
- IEEE 830风格的需求声明侧重于属性，而用户故事关注的是用户的目标。
- IEEE 830需求规范鼓励团队这样做把所有的需求陈述写在前面，而不是在里面迭代的方式，就像用户故事一样。

### Requirements Validation - Checking                   
**Validity**（是否提供最有效的功能？）
- Does the system provide the functions which best support the customer’s needs?

**Consistency**（需求是否冲突？）
- Are there any requirements conflicts?

**Completeness**（所有需求都满足了吗？）
- Are all functions required by the customer included?

**Realism**（现有预算和技术可以实现需求吗？）
- Can the requirements be implemented given available budget and technology?

**Verifiability**（需求可以被验证吗？）
- Can the requirements be checked?