# Creational Design Patterns

## Singleton Design Pattern
Sometimes it's important for some classes to have exactly one instance(like, the context of an application, 
a thread manageable pool, registry setting, a driver to connect to the input or output console, etc.). 
There are many objects we only need one instance of them and if we, instantiate more than one, 
we will run into all sort of problems,like incorrect program behavior, overuse of resources, or inconsistent results.

### When to use Singleton
* There must be exactly on instance o a class, and it must be accessible to clients from a well-known point
* When the sole instance should be extensible by sub-classing, and clients should be able to use an extended instance without modifying their code.

## Builder Design Pattern
The Builder pattern suggests moving the construction logic out of the object class to separate class 
referred to as a builder class.

The intent of the Builder Pattern is to separate the construction of a complex object from its representation, 
so that the same construction process can create different representation. The separation reduces
the object size. The design turns out to be more modular with each implementation contained in a different builder object.
Adding a new implementation becomes easier. The object construction process becomes independent of the components
that make up the object. This provides more control over the object construction process.

### When to use the Builder Pattern
* The algorithm for creating a complex object should be independent of the parts that make up the object and how they're assembled.
* The construction process must allow different representations for the object that's contructed

### Builder Pattern in JDK 
* java.lang.StringBuilder#append() (unsynchronized)
* java.lang.StringBuffer#append() (synchronized)
* java.nio.ByteBuffer#put()(also on CharBuffer,ShortBuffer,IntBuffer,LongBuffer,FloatBuffer and DoubleBuffer) 
* javax.swing.GroupLayout.Group#addComponent()
* All implementations of java.lang.Appendable

## Factory Method Design Pattern
The Factory Method pattern gives us a way to encapsulate the instantiations of concrete types.
The Factory Method pattern encapsulates the functionality required to select and instantiate an appropriate
class, inside a designated method referred to as a factory method.

### When to use Factory Method Design Pattern
* A class can't anticipate the class of objects it must create
* A class want its subclasses to specify the objects it creates.
* Classes delegate responsibility to one of several helper subclasses, and you want to locate the knowledge
    of which helper subclass is  the delegate.

### Factory Method Pattern is JDK
* java.util.Calendar#getInstance()
* java.util.ResourceBundle#getBundle()
* java.text.NumberFormat#getInstance()
* java.nio.charset.Charset#forName()
* java.net.URLStreamHandlerFactory#createURLStreamHandler(String) (Returns singleton object per protocol)

## Abstract Factory Method Design Pattern
The Abstract Factory(a.k.a. Kit) provides an interface for creating families of related or dependent
objects without specifying their concrete classes.

The Abstract Factory pattern is useful when a client object want to create instance of one of a suite
 of related, dependent classes without having to know which specific concrete class is to be instantiated.
 
The Abstract Factory pattern is also useful for plugging in a different group of objects to alter the behaviour
of the system.

### When to use Abstract Factory Design Pattern
* A system should be independent of how its products are created, composed and represented
* A system should be configured with one of multiple families of products
* A family of related product objects is designed to be used together, and you need to enforce this constraint
* You want to provide a class library of products, and you wan to reveal just their interfaces, not their implementation

### Abstract Factory Pattern in JDK
* java.util.Calendar#getInstance()
* java.util.Arrays#asList()
* java.util.ResourceBundle#getBundle()
* java.sql.DriverManager#getConnection()
* java.sql.Connection#createStatement()
* java.sql.Statement#executeQuery()
* java.text.NumberFormat#getInstance()
* javax.xml.transform.TransformerFactory#newInstance()

## Prototype Design Pattern
The Prototype Design Pattern is used to specify the kinds of objects to create using a prototypical
instance, and create new objects by copying this prototype.

The concept is to copy an existing object rather than a new instance from scratch, something that may
include costly operations. The existing object acts as a prototype and contains the state of the object.
The newly copied object may change some properties only if required.

### When to use Prototype Design Pattern
* When the classes to instantiate are specified at run-time, for example, dynamic loading
* To avoid building a class hierarchy of factories that parallels the class hierarchy of products
* When instances of a class can have one of only a few different combinations of stats. It may be
more convenient to install a corresponding number of prototypes and clone them rather than instantiating
the class manually, each time with the appropriate state.

### Prototype Pattern in JDK
* java.lang.Object#clone() 
* java.lang.Cloneable
