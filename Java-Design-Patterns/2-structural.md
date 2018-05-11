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

## Proxy Design Pattern
The Proxy Pattern is used to create a representative object that controls access to another object, 
which may be remote, expensive to creator in need of being secured.

One reason fo controlling access to an object is to defer the full cost of its creation and initialization
until we actually need to use it. Another reason could be to act as a local representative for an object that lives in a 
different JVM. The Proxy can be very useful in controlling the access to the original object, 
especially when objects should have different access rights.
 
### When to use the Proxy Pattern
* Remote Proxy: A remote proxy provides a local representative for an object in a different address space
* Virtual Proxy: A virtual proxy provides expensive objects on demand
* Protection Proxy: A protection proxy controls access to the original object. Protection proxies are useful when objects
    should have different access right.
* Cache Proxy/Server Proxy: To provide the functionality required to store the results of most frequently used target operation.
* Firewall Proxy: To protect target objects from bad client or prevent clients from accessing harmful targets.
* Synchronization Proxy: To provide the required functionality to allow safe concurrent accesses to a target object by different
    client object.
* Smart Reference Proxy: To provide functionality to prevent the accidental disposal/deletion of the target
    object when there are clients currently with references to it.
* Counting Proxy: To provide some kind of audit mechanism before executing a method on the target object.

### Proxy Pattern in JDK
* java.lang.reflect.Proxy
* java.rmi.* (whole package)