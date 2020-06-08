# OOP questions

## Software design

### Error handling

#### What does 'fail fast' mean in terms of exception handling? Why is it a good practice?

  Fail fast means that the exceprion is detected and the subsequent program is stopped before it can cause any damage. It is a good practice because the damage is reduced.

## Computer Science

### Data structures

#### How to find the middle element of singly linked list in O(n)?

  First you need to find the size, afterwards you iterate through it until you reach the element at position: size/2

#### Given an array of integers going from 1 to 100 (both inclusive) there is a duplicated entry. How to find it?

You use either a set(it does not support duplicates) or a Map that acts as a frequency map, if the map already contains that value, you raise an error or do something similar

    List<Integer> intList = new ArrayList();
            for (int i = 0; i < 100 ; i ++) {
            intList.add(i);
        }

        for (int i = 12; i< 25; i++) {
          intList.add(i);
        }

        intList.add(12);
        for(int num : intList) {
          System.out.println(num);
        }
        Map<Integer, Integer> duplicateMap = new HashMap<>();

        for(int num : intList) {
          if(duplicateMap.containsKey(num)) {
            System.out.print("Duplicate " + num);
            return;
          } else {
            duplicateMap.put(num, 1);
          }
        }

#### What is a linked list? How to find if a linked list has a loop?

 A linked list is a data structure where each node contains data and a pointer to the next node(singly linked) or also to the previous node (doubly linked).

 To detect a loop you may traverse the list and add node to a set. If the set already contains a node, it means there is a loop.

#### What is the Big O time complexity of the common operations in an ArrayList, LinkedList, HashMap? And of a bubble sort, quicksort, finding items in a Binary Search tree?

Array List

- get => O(1);
- add => O(1) best case, O(n) worst case because of potential array resizing;
- remove => O(n)

LinkedList

- get => O(n), O(1) when getting first or last items as it stores pointers for its head and tail.
- add => O(n), O(1) for first or last since there are built-in methods to add at he begininnig or at the end.
- remove => O(n), O(1) for first or last elements.

HashMap

- get => O(1) best case, O(n) worst case in case of good hashcode implementation
- add => O(1) best case, O(n) worst case in case of good hashcode implementation
- delete => O(1) best case, O(n) worst case in case of good hashcode implementation

BubbleSort

- best case: O(n)
- worst case: O(n^2)
  
QuickSort

- best case: O(n log n)
- worst case: O(n^2)

BST Search

- O(n) where n is the heigth of the tree
  
#### How does HashMap work?

A HashMap works the same way as a dictionary in Python, it stores key value pairs.

#### Why is it important for keys in a map to have an immutable type? (Consider String for example.)

If immutable, the object's hashcode wont change and it allows caching the hashcode of different keys which makes the overall retrieval process very fast.

### Other

#### What is a garbage collector, in a nutshell?

It is a mechanism that removes unused data from memory in order to free up space

## Programming paradigms

### Procedural

#### What is casting? What is the difference between up vs downcasting?

Casting may refer to either:

- typecasting: you assign the value of one primitive datatype to another
- objectcasting: you turn an object from a particular type into another one'

Upcasting

  - casting a subtype to a supertype, upward to the inheritance tree.

Downcasting

  - casting to a subtype, downward to the inheritance tree.


#### Which order should we catch the exceptions? Why?

You must catch the most specific exception first and the more generic ones later, as this approach ensures that no exceptions will be omitted on code execution.

### Object-oriented

#### What is a class?

A class is a blueprint usually representing a real life objects from which objects are created, made of fields and method.

#### What is an object?

An object is the instance of a class.

#### What is a constructor?

A method that creates objects of a certain class type.
#### Do we require parameter for constructors?

Not all the time, Java builds no parameter constructors automatically.

#### What is an interface?

Interface generally defines the set of methods (or messages) that an instance of a class that has that interface could respond to. 

#### What are access modifiers?

They are keywords that restrict the scope of a field, class, method, etc.

#### What is data hiding?

Data hiding is the process in which  the variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class.

#### Can a static method use non-static members?

They can use them only with object reference.


#### What is the difference between hiding a static method and overriding an instance method?

Overiding
 
 - it's decided at run time which method will be called. It is for non-static methods.

Hiding
 - is for all other members (static methods, instance members, static members), he method or member to be called or used is decided during compile time. 


#### Define the following terms: Instantiation, Attribute, Method

Instantiation
 - the process of creating a new object of a certain class

Attribute
 - class variables or fields that store data.

Method
 - a block of a code that runs when called and performs a specific task


#### Could we access a static variable (or method) from a non-static method? Why?

Instance methods can access class variables and class methods directly.
 

#### Could we access a non-static variable (or method) from a static method? Why?

Non-static variables cannot be accessed from a static context without a refference.



#### How many instances you have of a static variable of a given class?

Only one that persists among all the instances of that class.


#### Why is it not a good practice to write a lot of static methods?

They are basically global variables and their number and usage should be kept at minimum.

#### What are the features of static attributes and static methods of a class? What are the benefits, when to use them?

They do not need an instance of the class, they are useful for something like a singleton.

#### What is the ‘this’ reference?

'this' is a reference to the current object 


#### What are base class, subclass and superclass?
A class that is derived from another class is called a subclass. The class from which the subclass is derived is called a superclass (also a base class or a parent class).

#### Draw an object oriented family (as entities, with relations) on the whiteboard.

![UML](/docs/assets/images/pic.png)


#### Difference between overloading and overriding?

Overloading

- is a feature that allows a class to have more than one method having the same name, if their argument lists are different.
  

Overididng
 
 - declaring a method in sub class which is already present in parent class is known as method overriding. Overriding is done so that a child class can give its own implementation to a method which is already provided by the parent class.

Overloading happens at compile-time while Overriding happens at runtime: The binding of overloaded method call to its definition has happens at compile-time however binding of overridden method call to its definition happens at runtime.

#### What are the Object Oriented Principles? Explain the concepts with realistic examples!

- Encapsulation
   - is the mechanism of hiding of data implementation by restricting access to public methods. Instance variables are kept private and accessor methods are made public to achieve this. Ex: keeping sensitive data private. 
- Abstraction 
  - abstraction is to hide information that is not relevant to context or rather show only relevant information. Ex: when you drive car, you don't need to know how a diesel engine works but rather how to interact with it
- Polymorphism 
  - polymorphism gives a way to use a class exactly like its parent so there’s no confusion with mixing types but each child class keeps its own methods as they are. Java Collections
- Inheritance
  - expresses “is-a” and/or “has-a” relationship between two objects, using Inheritance, in derived classes we can reuse the code of existing super classes. Ex: A parent class animal can have multiple subclasses for different types of animals
  
#### What is method overloading?

Is a feature that allows a class to have more than one method having the same name, if their argument lists are different.

#### What is method overriding?

Declaring a method in sub class which is already present in parent class is known as method overriding.

#### Explain how object oriented languages attempt to simplify memory management for Programmers.
Memory Management is being aided by automatic Garbage collecting.

#### Explain the “Single Responsibility” principle!
Every module or class should have responsibility over a single part of the functionality provided by the software, and that responsibility should be entirely encapsulated by the class.

#### What is an object oriented program? Explain, show.
It is a program that uses classes and objects and has OOP principles applied throughout.
#### How do you make a class immutable? What do you need to watch out for?

 - Make the class final
 - Make all fields private
 - Don't provide setters
 - Assign values for the fields in the constructor
 - Return clones in getter methods

#### How many instances can be created for an abstract class?
Unlimited instances

## Programming languages

### Java

#### What is autoboxing and unboxing?
#### If you have a variable, that shall store a positive whole number between 0 and 200, what primitive type would you use to store it?
#### What is the "golden rule" of variable scoping in Java? What is the lifetime of variables?
#### What is the purpose of the ‘equals()’ method?

To compare objects.

#### What is the difference between '==' and 'equals()'?

#### What does the ‘static’ keyword mean?
#### Why is the main() method declared as static? Explain.
#### What is the default access modifier in a class?
#### What is the JVM?
#### What is the difference between the JRE and the JDK?
#### What is the difference between long and Long?
#### Can a long store bigger numbers than a Long?
#### What kind of packages do you know under java.util.* ? Bring at least 3 examples.
#### What are the access modifiers in Java? Which one could we use for class?
#### Can an “enum” contain methods in Java? Explain.
#### When would you use a private/protected/public attribute? What is the difference?
#### How do you prevent developers from subclassing a class?
#### How do you prevent developers from overriding a method in a subclass?
#### How do you prevent developers from changing the value of a variable?
#### Think about money ;) How would you store a currency value, that shall support decimal parts? Think it through again, and try to think outside of the box!
#### What happens if you try to call something, that you have no access to, because of data hiding?
#### What happens if you try to delete/drop an item from an array, while you are iterating over it?
#### What happens if you try to delete/drop/add an item from a List, while you are iterating over it?
#### What happens if you try to add an item to the end of an array, while you are iterating over it?
#### If you need to access the iterator variable after a for loop, how would you do it?
#### Which interfaces extend the Collection interface in Java. Which classes?
#### What is the connection between equals() and hashCode()? How are they used in HashMap?
#### What is the difference between checked exceptions and unchecked exceptions? Could you bring example for each?
#### What is Error in Java and how does it relate to Exception?
#### When does 'finally' block run? What it is used for? Could you give an example from your projects when you would use 'finally'?
#### What is the largest number you can work with in Java?
#### When you use method overriding, can you change the access level of the method, from protected to public? Why?When you use method overriding, can you change the access level of the method, from public to protected? Why?
#### Can the main method be overridden? Explain your answer!
#### When you use method overriding, can you throw fewer exceptions in the subclass than in the parent class? Why?
#### When you use method overriding, can you throw more exceptions in the subclass than in the parent class? Why?
#### What does "final" mean in case of a variable, method or a class?
#### What is the super keyword?
#### What are “generics”? When to use? Show examples.
#### What is the benefit of having “generic” containers?
#### Given two Java programs on two different machines. How can you communicate between the two? What are the possible ways?

  Sockets, HttpServlets, Tunneling.
#### What is an annotation? What can be annotated and how? Show examples.

### C&#35;

#### Explain the purpose of IL and how does it relate to CLR?
#### What does “managed code” mean?
#### What is an assembly?
#### What is the difference between an EXE and a DLL?
#### What is strong-typing versus weak-typing? Which is preferred? Why?
#### What is a namespace?
#### Explain sealed class in C#?
#### What is explicit vs. implicit conversion? Give examples of both of them.
#### Is a struct stored on the heap or stack?
#### Can a struct have methods?
#### Can DateTimes be null?
#### List out the differences between Array and ArrayList in C#?
#### How is the using() pattern useful? What is IDisposable? How does it support deterministic finalization?
#### How can you make sure that objects using dedicated resources (database connection, files, hardware, OS handle, etc.) are released as early as possible?
#### Why to use keyword “const” in C#? Give an example.
#### What is the difference between “const” and “readonly” variables in C#?
#### What is a property in C#?
#### List out two different types of errors in C#?
#### What is the difference between “out” and “ref” parameters in C#?
#### Can we override private virtual method in C#?
#### What's the difference between IEquatable and just overriding Object.Equals()?
#### Explain the differences between public, protected, private and internal. Explain access modifier – “protected internal” in C#!
#### What’s the difference between using `override` and `new` keywords when defining method in child class?
#### Explain StringBuilder class in C#!
#### How we can sort the array elements in descending order in C#?
#### Can you use a value type as a generic type argument in C#? For example when implementing an interface like (IEquatable).
#### What are Nullable Types in C#?
#### Conceptually, what is the difference between early-binding and late-binding?
#### What is delegate, event, callback, multicast delegate?
#### What is enum in C#?
#### What is null-conditional operator?
#### What is null-coalescing operator?
#### What is serialization?
#### What is the difference between Finalize() and Dispose() methods?
#### How do you inherit a class from another class in C#?
#### What is difference between “is” and “as” operators in C#?
#### What are indexers in C# .NET?
#### What is the difference between returning IQueryable<T> vs. IEnumerable<T>?
#### What is LINQ? Explain the idea of extension methods.
#### What are the advantages and disadvantages of lazy loading?
#### How to use of “yield” keyword? Mention at least one practical scenario where it can be used?
#### What are attributes in C#? Give some examples of usage of them.
#### By what mechanism does NUnit know what methods to test?
#### What is the GAC? What problem does it solve?
#### What is the largest number you can work with in C#?

### Database

#### How can you connect your application to a database server? What are the possible ways?

You may use a driver ( JDBC Postgres driver) that facilitates the connection between your persistance layer and the database. For this you may use a singleton or connection pooling.

#### What do you know about database normalization?

Normalization is a technique that organizes the database in such a way as to reduce redundancy and dependeny of data, by dividing larger tables into smaller tables and using relationships to link them


