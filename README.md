## DotNet and Object-Oriented Programming (OOP) in C#

_____________________________

### DotNet

#### Internet Information Services (IIS)

Internet Information Services (IIS) for Windows Server is a flexible, secure and manageable Web server for hosting anything on the Web

#### Kestrel

Kestrel is a cross-platform web server built for ASPNET Core based on libuv – a cross-platform asynchronous I/O library.
It is secure and good enough to use it without a reverse proxy server (IIS, Nginx or Apache)

#### WebListener

ASPNET Core ships two server implementations Kestrel and WebListener. WebListener is also a web server for ASPNET Core that runs only on Windows. It’s built on the Http.Sys kernel mode driver. WebListener is an alternative to Kestrel that can be used for direct connection to the Internet without relying on IIS as a reverse proxy server.

#### Common Language Runtime (CLR)

A CLR handles memory allocation and management. A CLR is also a virtual machine that not only executes apps but also generates and compiles code on-the-fly using a JIT compiler.

#### Core Common Language Runtime (Core CLR)

The Common Language Runtime for .NET 5 (and .NET Core) and later versions. Core CLR is a runtime for .NET Core. It includes JIT, GC and several low-level classes. 

#### Base Class Libraries (BCL)

A set of libraries that comprise the System.* 

#### Framework Class Library (FCL) 

FCL is the wider library that contains the totality: ASPNET, WinForms, the XML stack, ADONET and more. You could say that the FCL includes the BCL.

#### CoreFX

CoreFX is the foundational class libraries for .NET Core. It includes types for collections, file systems, console, JSON, XML, async and many others.

#### Common Intermediate Language (CIL)

Higher-level .NET languages, such as C#, compile down to a hardware-agnostic instruction set, which is called Common Intermediate Language (CIL). 

#### Just In Time Compiler (JIT)

JIT translates CIL to machine code that the processor understands. 

#### .NET Framework, .NET Core and .NET Standard

<p align="center">
  <img src="https://github.com/RobertoFreireFerrazPassos/dotNet-OOP/blob/main/images/dotNET_Core_dotNET_CLI_Compilation.png?raw=true">
</p>

##### .NET Framework

* It can run applications on Windows platform only.
* Web applications built using this platform can only be hosted on IIS.
* It supports ASPNET Web Forms, WinForms, WCF, Silverlight, etc. 
* The building blocks of .NET Framework are Common Language Runtime (CLR) and Base Class Libraries (BCL) and Common Intermediate Language (CIL).
* The Code written in C#, F# or VB is converted by the compiler into CIL. The code is executed by CLR using JIT to machine-specific code.

<p align="center">
  <img src="https://github.com/RobertoFreireFerrazPassos/dotNet-OOP/blob/main/images/CLR_CIL_JIT.jpg?raw=true">
</p>

##### .NET Core

* .NET Core is the cross-platform and open-source implementation of .NET.
* It supports modern application frameworks such as gRPC, ASPNET Core Razor Pages, Blazor (for WebAssembly), UWP and etc.
* The building blocks of .NET Core are Core CLR and CoreFX. 

##### .NET Standard

* NET Standard is a specification that can be used across all .NET implementations. 
* It is used for developing library projects only. This means if we are creating a library in .NET Standard we can use those in .NET Framework and .NET Core.

<p align="center">
  <img src="https://github.com/RobertoFreireFerrazPassos/dotNet-OOP/blob/main/images/NET_Core_NET%20Framework.png?raw=true">
</p>

#### Features provided by ASPNET Core

* Cross-platform.
* Built-in supports for Dependency Injection.
* Fast and cross-platform web server – Kestrel.

#### Assembly

An assembly is a .dll or .exe created by compiling one or more .cs files in a single compilation. 

#### Process

A process is an executing application. 

#### Thread

A Thread is a small set of executable instructions. The operating system executes code within a thread. The operating system switches between threads, allowing each to execute in turn, thus giving the impression that multiple applications are running at the same time.

#### Task

A Task is a higher level concept than Thread. We can easily implement Asynchronous using ’async’ and ‘await’ keywords. Task does use thread pool thread.

#### Thread vs Task

* Task can return a result. There is no direct mechanism to return the result from a thread.
* Task supports cancellation through the use of cancellation tokens. But Thread doesn't.
* A task can have multiple things happening at the same time. Threads can only have one thing running at a time.

<p align="center">
  <img src="https://github.com/RobertoFreireFerrazPassos/dotNet-OOP/blob/main/images/thread_task.png?raw=true">
</p>

#### Garbage collector.

The garbage collector is an implementation of automatic memory management. The GC frees memory occupied by objects that are no longer in use.

https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/

#### Metapackages

The framework .NET Core 2.0 introduced Metapackage that includes all the supported packages code with their dependencies into one package. It helps us to do fast development as we don’t require to include the individual packages. Example: Microsoft.AspNetCore.All.

<p align="center">
  <img src="https://github.com/RobertoFreireFerrazPassos/dotNet-OOP/blob/main/images/Metapackages.png?raw=true">
</p>

#### Middleware

##### ASPNET Core Middleware vs ASPNET Core Filters?

##### What is the difference between IApplicationBuilder.Use() and IApplicationBuilder.Run()

##### What is the use of “Map” extension while adding middleware to the ASP.NET Core pipeline

##### What is the Run extension?

##### How to enable Session in ASPNET Core?

#### ASPNET Core Dependency Injection

#### Singleton

#### Transient

#### Scoped

### Managed and Unmanaged Code

https://docs.microsoft.com/en-us/dotnet/standard/managed-code
_____________________________

### Object-Oriented Programming (OOP) in C#

### Access Modifiers

| Caller's location  | public | protected internal | protected | internal | private protected | private |
| ------------- | :---:  | :---:  |  :---:  | :---:  |  :---:  | :---:  |
| Within the class |✔️ |  ✔️ | ✔️ | ✔️ | ✔️ | ✔️ | 
| Derived class (same assembly) | ✔️ |  ✔️ | ✔️ | ✔️ | ✔️ | ❌ |
| Non-derived class (same assembly) | ✔️  | ✔️  | ❌ |✔️  |  ❌ | ❌ |
| Derived class (different assembly) | ✔️ |  ✔️  | ✔️  |  ❌ | ❌ | ❌ |
| Non-derived class (different assembly) | ✔️  | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |

### Continue and break in loop

### Constant vs readonly

A variable in C# can be made into a compile-time constant by adding the const keyword before the data type. This modifier means that the variable cannot be changed and it must therefore be assigned a value at the same time as it is declared. Any attempts to assign a new value to the constant will result in a compile-time error.

https://www.c-sharpcorner.com/UploadFile/puranindia/C-Sharp-interview-questions/

### Ref vs out

### Sealed 

### Late binding and early binding

### IEnumerable vs IQueryable

### IEnumerable<>

### Yield

### Equality Operator (==) vs Equals()

### Is vs As

### Anonymous Types

### Reflection 

### LINQ 

### Using statement

https://www.c-sharpcorner.com/UploadFile/manas1/usage-and-importance-of-using-in-C-Sharp472/

### Operators and expressions (.? ?? :: )

https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/

### Serialization

### Lock and DeadLock

https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/statements/lock

### Value types vd Reference type

### What happens if the inherited interfaces have conflicting method names?

### Can “this” be used within a static method?

### Array.CopyTo() vs Array.Clone()

### Array vs ArrayList

### Dispose vs finalize 

### Delegates and multicast delegate

### Abstract Class vs Interfaces

#### Interfaces

Interface defines a contract between an object and its user. It can be implemented by a class or a struct that adheres to the contract.

**Cannot** create an instance of interface
```cs
public interface IA {}
... 
var classB = new IA(); // Compiler Error
```

An interface can contain methods and properties but **not fields**.
```cs
public interface Ib 
{
  public string Field1; // Compiler Error

  public string Property1 { get; set; }  

  // It is possible to create property like below.
  // But, it will not acessable by the class which implements this interface.
  public string Property2 {
      get
      {
          return "text";
      }
      set
      {
          Console.WriteLine(value);
      }
  }
}
...
public class ClassB : Ib
{
    public string Property1 { get => "test ClassB"; set => Console.WriteLine(value); }
}
```

Class can implement multiple interfaces 

```cs
public interface IA {
    public void Function1();
}

public interface IB {
    public void Function2();
}

public class C : IA, IB
{
    public void Function1() { }

    public void Function2() { }
}
```

#### Abstract Class

An abstract class provides a partial implementation that other classes can build on. When a class is declared as abstract, it means that the class can contain incomplete members that must be implemented in derived classes, in addition to normal class members.


A method/property **cannot** be an abstract member of a nonabstract class.
```cs
public class ClassA 
{
    public abstract string Property1 { get; set; } // Compiler Error

    public abstract void Function1(); // Compiler Error
}
```

The modifier 'abstract' is not valid on fields. Try using a property instead
```cs
public abstract class ClassA 
{
    public abstract string Property1; // Compiler Error
}
```

**Cannot** create an instance of the abstract class
```cs
public abstract class ClassA {}
... 
var classA = new ClassA(); // Compiler Error
```

Class **cannot** inherit multiple classes/abstract classes. 
```cs
public class A {}

public abstract class B {}

public class D : A, B // error 
{}
```

Implementation of an abstract class
```cs
public abstract class ClassA 
{
    public abstract string Property1 { get; set; }
    
    public abstract void Function1(); 

    public string Function2()
    {
        return "test2";
    }
}
...
public class ClassB : ClassA
{
    private string property;

    public override string Property1 { get => property; set => property = value; }

    public override void Function1()
    {
        property = property + " add value";
    }
}
...
var b = new ClassB();
b.Property1 = "test value";
b.Function1();
Console.WriteLine(b.Property1);
Console.WriteLine(b.Function2());

// Console Output
// test value add value
// test2
```

### Composition vs Inheritance

#### Composition

#### Inheritance

### Overloading vs Overriding

#### Overloading

#### Overriding

### Static methods vs Static class

### Struct vs Class

### Encapsulation

### Polymorphism

### Virtual

### Data Abstraction

### Try catch finally and exception

### Boxing vs unboxing 

https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/types/boxing-and-unboxing

https://docs.microsoft.com/en-us/dotnet/framework/performance/performance-tips

### Collections and Data Structures

https://docs.microsoft.com/en-us/dotnet/standard/collections/

https://docs.microsoft.com/en-us/dotnet/standard/collections/commonly-used-collection-types

### Concurrent Collections

https://docs.microsoft.com/en-us/dotnet/standard/collections/thread-safe/

### Memory and span

https://docs.microsoft.com/en-us/dotnet/standard/memory-and-spans/

### SOLID

#### Single Responsiblity Principle

#### Open-Closed Principle

#### Liskov Substitution Principle

#### Interface Segregation Principle

#### Dependency Inversion Principle



## Reference:

https://docs.microsoft.com/en-us/dotnet/csharp/