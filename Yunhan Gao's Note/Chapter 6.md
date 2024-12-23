# Ch6-Architectural Design
## 4+1 View Model of Software Architecture
1. **Logical view:** which shows the key abstractions in the system as objects or object classes.
2. **Process view:** which shows how, at run-time, the system is composed of interacting processes.
3. **Development view:** which shows how the software is decomposed for development.
4. **Physical view:** which shows the system hardware and how software components are distributed across the processors in the system.
- Related using use cases or scenarios.

## Architectural Patterns
>**An architectural pattern is a stylized description of good design practice**, which has been tried and tested in different environments.
### Pipe-and-filter Architecture (Not really suitable for interactive systems.)
>The  processing  of  the  data  in  a  system  is  organized  so  that  each processing  component  (filter)  is  discrete  and  carries  out  one  type  of data transformation. The data flows (as in a pipe) from one component to another for processing.

**When use:**
Commonly used in data processing applications (both  batch- and transaction-based)  where inputs are processed in separate stages to generate related outputs. (数据处理应用程序)

### Client-server Architecture
>A system that follows the client-server pattern is organized as a set of services and associated servers, and clients that access and use the services.

**When use:**
Used  when  data  in  a  shared  database  has  to  be  accessed  from  a range of locations. Because servers can be replicated, may also be used when the load on a system is variable.

### Event-based Architecture
**Examples:**
- Debugging systems (listen for particular breakpoints)
- Graphical user interfaces

### Layered Architecture
>Organises the system into a set of layers each of whichprovide a set of services.

**When use:**
Used when building new facilities on top of existing systems; when the  development  is  spread  across  several  teams  with  each  team responsibility for a layer of functionality; when there is a requirement for multi-level security.

**Examples:**
- Operating systems
- Communication protocols

### Repository Architecture
>The repository contains a single datastructure called Repository and a number of modules called Knowledge Sources that modify this datastructure.

**When use:**
You  should  use  this  pattern  when  you  have  a  system  in  which  large volumes  of  information  are  generated  that  has  to  be  stored  for  a  long time.  You  may  also  use  it  in  data-driven  systems  where  the  inclusion  of data in the repository triggers an action or tool.
**Examples:**
- Database
- Programming environments

### Model-View-Controller Architecture (记细节)
| Name | MVC (Model-View-Controller) |
|----------|----------|
| **Description** | Separates presentation and interaction from the system data. The system is  structured  into  three  logical  components  that  interact  with  each  other. The Model component manages the system data and associated operations on that data. The View component defines and manages how the data is presented to the user. The Controller component manages user interaction  (e.g.,  key  presses,  mouse  clicks,  etc.)  and  passes  these interactions to the View and the Model. |
| **When used** | Used  when  there  are  multiple  ways  to  view  and  interact  with  data. Also used when the future requirements for interaction and presentation of data are unknown.  |
| **Advantages** | Allows  the  data  to  change  independently  of  its  representation  and  vice versa.  Supports  presentation  of  the  same  data  in  different  ways  with changes made in one representation shown in all of them. |
| **Disadvantages** | Can  involve  additional  code  and  code  complexity  when  the  data  model and interactions are simple. |

## Architectural Design Decisions (四个设计原则)
1. **Performance**
 Localize critical operations and minimize communications. Use large rather than fine-grain components.
2. **Security**
Use a layered architecture with critical assets in the inner layers.
3. **Availability**
Include redundant components and mechanisms for fault
tolerance.
4. **Maintainability**
Use fine-grain, replaceable components.