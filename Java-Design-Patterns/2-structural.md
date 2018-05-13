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

## Flyweight Design Pattern
The Flyweight Pattern is design to control similar and heavy object and provides you with a basic
caching mechanism. It allows you to create on object per type, and if you ask for na object with the 
same property, it will return you the same object instead of creating a new one.

The intent of the Flyweight Pattern is used to share objects to support large numbers of fine-grained
objects efficiently. A flyweight is a shared object that can be used in multiple contexts simultaneously.
The flyweight acts as an independent object in each context. Flyweight can not make assumptions about
the context in which they operate. The key concept here is the distinction between intrinsic and extrinsic
state.

### When to use the Flyweight Pattern
* An application uses a large number of objects
* Storage costs are high because of the sheer quantity of objects
* Most object state can be made extrinsic
* Many groups of objects may be replaced by relatively few shared objects once extrinsic status is removed.
* The application does not depend on object identity. Since flyweight objects may be shared, identity
    tests will return tru for conceptually distinct objects.
    
### Flyweight in the JDK
* java.lang.Integer#valueOf(int) (also on Boolean, Byte, Character, Short and Long)

## Decorator Design Pattern
The intent of the Decorator Design Pattern is to attach additional responsibilities to an object dynamically.
Decorators provide a flexible alternative to sub-classing for extending functionality. This is accomplished
 by creating object wrapper referred to as a Decorator around the actual object.

Decorators prevent the proliferation of subclasses leading to less complexity and confusion. It is easy
to add any combination of capabilities. The sam capability can even be added twice. It becomes possible to have
different decorator objects for a given object simultaneously. A client can choose what capacities it wants
by sending messages to an appropriate decorator.
 
### When to use the Decorator Design Pattern
* To add responsibilities to individual objects dynamically and transparently, that is, without affecting other objects
* For responsibilities that can be withdrawn.
* When extension by sub-classing is impractical. Sometimes a large number of independent extensions are possible
     and would produce an explosion of subclasses to support every combination. OR a class definition may be hidden
     or otherwise unavailable for sub-classing.
        
### Decorator Design Pattern in JDK
* java.io.BufferedInputStream(InputStream)
* java.io.DataInputStream(InputStream)
* java.io.BufferedOutputStream(OutputStream)
* java.util.zip.ZipOutputStream(OutputStream)
* java.util.Collections#checked()(List|Map|Set|SortedSet|SortedMap)

## Visitor Design Pattern
The intent of the Visitor Design Pattern is to represent an operation to be performed on the elements
of an object structure. Visitor lets you define a new operation without changing the classes of the elements
on which it operates.
To accomplish this, the Visitor pattern suggests defining the operation in separate class referred to as a visitor
class. This separates the operation from the object collection that it operates on.

### When to use Visitor Design Pattern
* An object structure contains many classes of objects with differing interfaces, and you want to  perform operations
    on these objects that depend on their concrete classes.
* Many distinct and unrelated operations need to be performed on objects in an object structure, and 
    you want to avoid "polluting" their classes with these operations. Visitor lets you keep related
    operations together by defining them in one class. When the object structure is shared by many applications,
    use Visitor to put operations in jus those applications that need them.
* The classes defining the object structure rarely change, but you often want to define new operation over the
    structure. Changing the object structure classes requires redefining the interface to all visitors,
    which is potentially costly.

### Visitor Design Pattern in JDK
* javax.lang.model.element.Element and javax.lang.model.element.ElementVisitor 
* javax.lang.model.type.TypeMirror and javax.lang.model.type.TypeVisitor