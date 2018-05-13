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

## Chain of Responsibility Design Pattern
In the Chain of Responsibility pattern, a group of objects is chained together in a sequence and a
responsibility(a request) is provided in order to be handled by the group. If an object in the group
can process the particular request, it does so and returns the corresponding response. Otherwise, it 
forwards the request to the subsequent object in the group.

The intent of this pattern is to avoid coupling the sender of a request to its receiver by giving more than
one object a chance to handle the request. We chain the receiving objects and pass the request along the 
chain until an object handles it.

When there is more than one objects that can handle or fulfill a client request, the pattern recommends
 giving each of these objects a change to process the request in some sequential order.

### When to use the Chain of Responsibility Pattern
* More than one objects may handle a request, and the handler isn’t known a priori. 
The handler should be ascertained automatically.
* You want to issue a request to one of several objects without specifying the receiver explicitly.
* The set of objects that can handle a request should be specified dynamically.

### Chain of Responsibility in JDK
* java.util.logging.Logger#log() 
* javax.servlet.Filter#doFilter()

## Memento Design Pattern
Sometimes it's necessary to record the internal state of an object. This is required when implementing
checkpoints and "undo" mechanisms that let uses back out of tentative operations or recover from errors.

The Memento Pattern's intent is, without violating encapsulation, to capture and externalize an object's
internal state so that the object can be restored to this state later.

### When to use Memento Design Pattern
* A snapshot of(some portion of) an object's stats must be saved so that it can be restored to that state later
* A direct interface to obtaining the state would expose implementation details and break the object's encapsulation.

### Memento Pattern in JDK
* java.util.Date
* java.io.Serializable

## Template Design Pattern
The Template Design Patter, as the name suggests, provides a template or a structure of an algorithm
which is used by user. A user provides its own implementation without changing the algorithm's structure.

The Template Pattern defines the skeleton of an algorithm in an operation, deferring some steps to subclasses.
Template Method lets subclasses to redefine certain steps of an algorithm without changing its structure.

The Template class does not necessarily have to leave the implementation to subclasses in its entirety.
Instead, as part of providing the outline of the algorithm, the Template class can also provide some amount
of implementation that can be considered as invariant across different implementations. It can even provide
default implementation for the variant parts, if appropriate.

### When to use the Template Design Pattern
* To implement the invariant parts of an algorithm core and leave it to subclasses to implement the behavior that can vary.
* When common behavior among subclasses should be factored and localized ina common class to avoid duplication. You 
    first identify the differences in the existing code and then separate the differences into new operations. Finally, 
    you replace the differing code with a template method that calls one of these new operations.
* To control subclasses extensions. You can define a template method that calls "hook" operations as specific points,
    thereby permitting extensions only at those points.
    
### Template Pattern in JDK
* java.util.Collections#sort()
* java.io.InputStream#skip()
* java.io.InputStream#read()
* java.util.AbstractList#indexOf()

## State Design Pattern
The State Design Pattern allows an object to alter its behavior when its internal state changes.
THe object will appear to change its class.

The state of an object can be defined as its exact condition at any given point of time, depending on the values
of its properties or attributes. The set of methods implemented by a class constitutes the behaviors of its instances.

The State pattern is useful in designing an efficient structure for a class, a typical instance of which
can exist in many different states and exhibit different behavior depending on the state it is in.

### When to use the State Design Patten
* An object's behavior depends on its state, and it must change its behavior at run-time depending on that state.
* Operations have large, multipart conditional statements that depend on the object's state. This state is usually 
    represented by one or more enumerated constants. Often, several operations will contain this same conditional structure.
    The State pattern puts each branch of the conditional in a separate class. This lets yo treat object's state
    as an object in its own right that can very independently from other object.
    
### State Design in JDK
* javax.faces.lifecycle.LifeCycle#execute()

## Strategy Design Pattern
The Strategy Design Pattern defines a family of algorithm, encapsulating each other, and making them interchangeable.
Strategy lets the algorithm vary independently from the clients that use it.

The Strategy pattern is useful when there is a set of related algorithms and a client object needs 
to be able to dynamically pick and choose an algorithm from this set that suits its current need. 
The Strategy pattern suggests keeping the implementation of each of the algorithms in a separate class. 

### When to use the Strategy Design Pattern
* Many related classes differ only in their behavior. Strategies provides a way to configure a class with one of many behavior;
* You need different variants of an algorithm
* An algorithm uses data that clients should not know about. Use the Strategy pattern to avoid exposing complex,
    algorithm-specific data structure.
* A class defines man behaviors, and these appear as multiple conditional statements in its operations. 
    Instead of many conditionals, move related conditional branches into their own Strategy class.
    
### Strategy Pattern in JDK
* java.util.Comparator#compare() 
* javax.servlet.http.HttpServlet 
* javax.servlet.Filter#doFilter()

## Command Design Pattern
The Command pattern would help to decouple the invoker from a receiver and helps to execute any type of
job without knowing its implementation.
The intent of the Command Design Pattern is to encapsulate a request as an object, thereby letting the
developer to parameterize clients with different requests, queue or log requests, and support undoable operations.

In terms of implementation, the application may depend on a designated object that invokes methods on these objects
by passing the required data as arguments. The designated object can be referred to as an invoker 
as it invokes operations on different objects. The Command pattern suggests creating an abstraction
 for the processing to be carried out or the action to be taken in response to client requests.
 
### When to use the Command Design Pattern
* Parameterize objects by an action to perform
* Specify, queue, and execute requests at different times. A Command object can have a lifetime     
    independent of the original request. If the receiver of a request can be represented in an 
    address space-independent way, then you can transfer a command object for the request to a 
    different process and fulfill the request there.
* Support undo. The Command's execute operation can store state for reversing its effects in the command itself.
* Support logging changes so that they can be reapplied in case of a system crash.
* Structure a system around high-level operations built on primitives operations.

### Command Design Pattern in JDK
* java.lang.Runnable 
* javax.swing.Action

## Interpreter Design Pattern
The Interpreter Design Pattern is a heavy-duty pattern. It' s all about putting together your own 
programming language, or handling an existing one, by creating an interpreter for that language. Giving
 a language, define a representation for its grammar along with an interpreter that uses the representation
 to interpret sentences in the language.
 
In such cases, instead of treating every distinct combination of rules as a separate case, it may
be beneficial for the application to have the ability to interpret a generic combination of rules.
A class hierarchy can be designated to represent the set of grammar rules with every class in the
hierarchy representing a separate grammar rule. An interpreter module can be designed to interpret 
the sentences constructed using the class hierarchy designed above and carries out the necessaries operations.  

### When to use the Interpreter Design Pattern
* The grammar is simple. For complex grammars, the class hierarchy fo the grammar becomes large and
    unmanageable. Tools such as parser generator are a better alternative in such cases.
* Efficiency is not a critical concern. The most efficient interpreters are usually not implemented by 
    interpreting parse trees directly but by first translating them into another form.
    
### Interpreter Design Pattern in JDK
* java.util.Pattern
* java.text.Normalizer 
* java.text.Format

## Iterator Design Pattern
The intent of the Iterator Design Pattern is to provide a way to access the elements of an aggregate
object sequentially without exposing its underlying representation. The Iterator pattern allows a client
object to access the contents of a container in a sequential manner, without having any knowledge about the internal
representation of its contents.

### When to use Iterator Design Pattern
* To access an aggregate object's contents without exposing its internal representation
* To support multiple traversals of aggregate objects.
* To provide a uniform interface for traversing different aggregate structures.

### Iterator Pattern in JDK
* java.util.Iterator
* java.util.Enumeration