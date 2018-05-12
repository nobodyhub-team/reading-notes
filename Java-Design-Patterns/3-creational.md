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
