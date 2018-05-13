# Introduction to Design Patterns

Design Patterns are general reusable solution to commonly occurring problems.
In general, a pattern has four essential elements:
* Pattern name: is used to provide a single and meaningful name to the pattern which defines a design problem and a solution for it.
* The problem describes when to apply the pattern. It explains the problem and its context.
* The solution describes the elements that make up the design, their relationships, responsibilities, and collaborations.
* The results and consequences of applying the pattern. The consequences of software often concern space and time trade-offs. 
    They may address language and implementation issues as well. Since reuse is often a factor in object-oriented design,
    the consequences of a pattern include its impact on a system's flexibility, extensibility, or portability.
    
### Why use them
* Flexibility: Using design patterns your code becomes flexible. It helps to provide the correct
    level of abstraction due to which objects become loosely coupled to each other which makes your code easy to change.
* Reusability: Loosely coupled and cohesive objects and classes can make your code more reusable. 
    This kind of code becomes easy to be tested as compared to the highly coupled code.
* Shared Vocabulary: Shared vocabulary makes it easy to share your code and thought with other team members. 
    It creates more understanding between the team members related to the code.
* Capture best practice: Design patterns capture solutions which have been successfully applied to problems. 
    By learning these patterns and related problem, an inexperienced developer learns a lot about software design.

### Categorization of patterns
* Creational patterns: are used to design the instantiation process of objects. 
    The creational pattern uses the inheritance to vary the object creation.
* Structural patterns: are concerned with how classes and objects are composed to form large structures. 
    Structural class patterns use inheritance to compose interface or implementations.
* Behavioral patterns: are concerns with algorithms and the assignment of responsibility between objects.
    Behavioral patterns describe not just patterns of objects or classes but also the patterns of communication between them.
    
|Creational Patterns|Structural Patterns|Behavioral Patterns|
|:-----------------:|:-----------------:|:-----------------:|
|[Abstract Factory](3-creational.md#abstract-factory-method-design-pattern)|[Adaptor](2-structural.md#adapter-design-patterns)|[Chain of Responsibility](4-behavioral.md#chain-of-responsibility-design-pattern)|
|[Builder](3-creational.md#builder-design-pattern)|[Bridge](2-structural.md#bridge-design-pattern)|[Command](4-behavioral.md#)|
|[Factory Method](3-creational.md#factory-method-design-pattern)|[Composite](2-structural.md#composite-design-pattern)|[Interpreter](4-behavioral.md#command-design-pattern)|
|[Prototype](3-creational.md#prototype-design-pattern)|[Decorator](2-structural.md#decorator-design-pattern)|[Iterator](4-behavioral.md#iterator-design-pattern)|
|[Singleton](3-creational.md#singleton-design-pattern)|[Facade](2-structural.md#facade-design-pattern)|[Mediator](4-behavioral.md#mediator-design-pattern)|
|-|[Flyweight](2-structural.md#flyweight-design-pattern)|[Memento](4-behavioral.md#memento-design-pattern)|
|-|[Proxy](2-structural.md#proxy-design-pattern)|[Observer](4-behavioral.md#observer-design-pattern)|
|-|-|[State](4-behavioral.md#state-design-pattern)|
|-|-|[Strategy](4-behavioral.md#strategy-design-pattern)|
|-|-|[Template](4-behavioral.md#template-design-pattern)|
|-|-|[Visitor](4-behavioral.md#visitor-design-pattern)|

[Home](README.md), [Next](2-structural.md)