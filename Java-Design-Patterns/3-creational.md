# Creational Design Patterns

## Singleton Design Pattern
Sometimes it's important for some classes to have exactly one instance(like, the context of an application, 
a thread manageable pool, registry setting, a driver to connect to the input or output console, etc.). 
There are many objects we only need one instance of them and if we, instantiate more than one, 
we will run into all sort of problems,like incorrect program behavior, overuse of resources, or inconsistent results.

### When to use Singleton
* There must be exactly on instance o a class, and it must be accessible to clients from a well-known point
* When the sole instance should be extensible by sub-classing, and clients should be able to use an extended instance without modifying their code.
