# Structural Design Patterns

## Adapter Design Patterns

### Types of adapters
* the object adapter: use object's composition 
* the class adapter: relies n multiple inheritance to adapt one interface to another. 

### When to use Adapter Pattern
* There are existing class, and its interface does not match the one you need
* You want to create a reusable class tha cooperates with unrelated or unforeseen classes, that is 
    classes that don't necessarily have compatible interfaces.
* There are several existing subclasses to be use, but it's impractical to adapt their interface by
    subclassing every one. An object adaptor can adapt the interface of its parent class. 
    
## Facade/fəˈsɑːd/ Pattern
The Facade Pattern makes a complex interface easier to use, using a Facade class.
The Facade Pattern provides a unified interface to a set of interface in a subsystem.
Facade Pattern defines a higher-level interface that makes the subsystem easier to use.

The Facade unifies the complex low-level interfaces of a subsystem in order to provide a simple way 
to access that interface. It just provides a layer to the complex interfaces of the subsystem.

The Facade do not encapsulate the subsystem classes or interfaces; it just provides a simplified interface
to their functionality. A client can access these classes directly. It still exposes the full functionality of the system
for the clients who may need it.

### Use of Facade Pattern
* You want to provide a simple interface to a complex subsystem. Subsystems often get more complex as they evolve. 
    Most patterns, when applied, result in more and smaller. This makes the subsystem more reusable and easier to customize,
    but it also becomes harder to used for clients that don't need to customize it. A facade can provide a simple default view
    of the subsystem that is good enough for most clients. Only clients needing more customization will need to look beyond
    the facade.
* There are many dependencies between client and the implementation classes of an abstraction. 
    Introduce a facade to decouple the subsystem from clients and other subsystem, thereby promoting 
    subsystem independence and portability.
* You can layer your subsystem. Use a facade to define an entry point to each subsystem level. If subsystems are dependent, 
    then you can simplify the dependencies between them by making them communicate with each other solely through their facades.
 
## Composite Design Pattern
Composite Pattern allows yo to compose objects into structures to represent part-whole hierarchies.
Composite lets clients to treat individual objects and compositions of objects uniformly.

The Composite Pattern allows us to build structures of objects in the form of trees that contains both 
composition of objects and individual objects as nodes. Using a composite structure, we can apply the
same operations over both composites and individual objects.

### When to use Composite Pattern
* When you want to represent part-whole hierarchies of objects
* When you want clients to be able to ignore the difference between compositions of objects and individual objects.
    Clients will treat all objects in the composite structure uniformly.
    
## Bridge Design Pattern
The Bridge Pattern's intent is to decouple an abstraction from its implementation so that the two can vary independently. 
It puts an abstraction and implementation into two different class hierarchies so that both can be extend independently.

### Use of Bridge Pattern
* You want to avoid a permanent binding between an abstraction and its implementation. This might be the case, for example, 
    when the implementation must be selected or switched at run-time.
* Both the abstractions and their implementations should be extensible by sub-classing. In this case, the Bridge pattern lets
    you combine the different abstractions and implementations and extend them independently.
*  Changes in the implementation of an abstraction should have no impact on clients; that is the code should not have to be recompiled
* You want to share an implementation among multiple objects(perhaps using reference counting), and this fact should be hidden from the client.

