# Behavioral Design Patterns

##  Observer Design Pattern
The Observer Pattern is a kind of behavior pattern which sis concerned with the assignment of 
responsibilities between objects. The behavior pattern s characterize complex control flows that 
are difficult to follow at run-tim. They shift your focus away from the flow of control to the let 
you concentrate just on the way objects are interconnected.

The Observer Pattern defines a one-to-many dependency between objects so the when one object changes
state, all its dependents are notified and update automatically.
The other way to understand the Observer Pattern is the way Publisher-Subscriber relationship works.

### When to use the Observer Pattern
* When an abstract has two aspects, one dependent on the other. Encapsulating these aspects in separate
    objects lets you vary and reuse them independently.
* When a change to one object required changing others, and you don't know how many objects need to be changed.
* When an object should be able to notify other objects without making assumptions about who there objects
    are. In other words, you don't want these objects tightly coupled.
    
## Mediator Design Pattern
The Mediator Pattern defines an object that encapsulate how a set of objects interact. 
Mediator promotes loose coupling by keeping objects from referring to each other explicitly, 
and it lets you vary their interaction independently.

Rather than interacting directly with each other, objects ask the Mediator to interact on their behalf
 which results in re-usability and loose coupling. It encapsulates the interaction between the 
 objects and makes them independent from each other. Using a Mediator means the interaction code has 
 to reside in only one place, and that makes it easier to maintain.
 
### When to use the Mediator Pattern
* A set of objects communicate in well-defined but complex ways. The resulting inter-dependencies are
    unstructured an difficult to understand.
* Reusing an object is difficult because it refers to and communicates with many other objects.
* A behavior that's described between several classes should be customizable without a lot of sub-classing.

### Mediator Pattern in JDK
* java.util.concurrent.ScheduledExecutorService (all scheduleXXX() methods) 
* java.util.concurrent.ExecutorService (the invokeXXX() and submit() methods) • java.util.concurrent.Executor#execute()
* java.util.Timer (all scheduleXXX() methods)
* java.lang.reflect.Method#invoke()
