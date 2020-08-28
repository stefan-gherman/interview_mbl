# General enterprise questions

## Software engineering

### Architectures

#### What is n-tier (or multi-tier) architecture?
N-tier architecture is also called multi-tier architecture because the software is engineered to have the processing, data management, and presentation functions physically and logically separated.  That means that these different functions are hosted on several machines or clusters, ensuring that services are provided without resources being shared and, as such, these services are delivered at top capacity.  The “N” in the name n-tier architecture refers to any number from 1.
#### What are microservices? Advantages and disadvantages?
Microservices are a popular software design architecture that breaks apart monolithic systems. Applications are built as collections of loosely coupled services. Each microservice is responsible for a single feature. They interact with each other through communication protocols such as HTTP and TCP.

The biggest pro of microservices architecture is that teams can develop, maintain, and deploy each microservice independently. This kind of single-responsibility leads to other benefits as well. Applications composed of microservices scale better, as you can scale them separately, whenever it’s necessary. Microservices also reduce the time to market and speed up your CI/CD pipeline. This means more agility, too. Besides, isolated services have a better failure tolerance. It’s easier to maintain and debug a lightweight microservice than a complex application, after all.

Cons
- Needs more collaboration (each team has to cover the whole microservice lifecycle)
- Harder to test and monitor because of the complexity of the architecture
- Poorer performance, as microservices need to communicate (network latency, message processing, etc.)
- Security issues (harder to maintain transaction safety, distributed communication goes wrong more likely, etc.)

#### What is Separation of Concerns?
 Separation of concerns is a design principle for separating a computer program into distinct sections such that each section addresses a separate concern. A concern is a set of information that affects the code of a computer program. A concern can be as general as "the details of the hardware for an application", or as specific as "the name of which class to instantiate". A program that embodies SoC well is called a modular
#### What is a layered design and why is it important in enterprise applications?
Layered architecture patterns are n-tiered patterns where the components are organized in horizontal layers. This is the traditional method for designing most software and is meant to be self-independent. This means that all the components are interconnected but do not depend on each other.

It is easy to test as components belong to specific layers. As such, they can be tested separately.
It is simple and easy to implement because naturally, most applications work in layers.

#### What is Dependency Injection?
Dependency Injection (DI) is a design pattern used to implement IoC. It allows the creation of dependent objects outside of a class and provides those objects to a class through different ways. Using DI, we move the creation and binding of the dependent objects outside of the class that depends on them.
#### What is the DAO pattern? When and how to implement?
Data Access Object Pattern or DAO pattern is used to separate low level data accessing API or operations from high level business services.

Implementation is made using the following participants:
- Data Access Object Interface - This interface defines the standard operations to be performed on a model object(s).
- Data Access Object concrete class - This class implements above interface. This class is responsible to get data from a data source which can be database / xml or any other storage mechanism
- This object is simple entity containing get/set methods to store data retrieved using DAO class.

#### What is SOA? When to use?

A service-oriented architecture (SOA) is an architectural pattern in computer software design in which application components provide services to other components via a communications protocol, typically over a network. The principles of service-orientation are independent of any product, vendor or technology.

The web services themselves can exchange data with each other and because of the underlying principles on which they are created, they don't need any sort of human interaction and also don't need any code modifications. It ensures that the web services on a network can interact with each other seamlessly.

### Testing
#### What are unit test, integration test, system test, regression test, acceptance test? What is the major difference between these?
Unit test: when it fails, it tells you what piece of your code needs to be fixed.

Integration test: when it fails, it tells you that the pieces of your application are not working together as expected.

Acceptance test: when it fails, it tells you that the application is not doing what the customer expects it to do.

Regression test: when it fails, it tells you that the application no longer behaves the way it used to.
#### What is code coverage? Why is it used? How you can measure?
Code coverage is a measurement of how many lines/blocks/arcs of your code are executed while the automated tests are running.

Code coverage is collected by using a specialized tool to instrument the binaries to add tracing calls and run a full set of automated tests against the instrumented product. A good tool will give you not only the percentage of the code that is executed, but also will allow you to drill into the data and see exactly which lines of code were executed during a particular test.
#### What does mocking mean? How would you do it 'manually' (i. e. without using any fancy framework)?
Mocking is primarily used in unit testing. An object under test may have dependencies on other (complex) objects. To isolate the behavior of the object you want to replace the other objects by mocks that simulate the behavior of the real objects. This is useful if the real objects are impractical to incorporate into the unit test.

In short, mocking is creating objects that simulate the behavior of real objects.

To give an example: You can stub a database by implementing a simple in-memory structure for storing records. The object under test can then read and write records to the database stub to allow it to execute the test. This could test some behavior of the object not related to the database and the database stub would be included just to let the test run.
#### What is a test case? What is an assertion? Give examples!
A TEST CASE is a set of actions executed to verify a particular feature or functionality of your software application. A Test Case contains test steps, test data, precondition, postcondition developed for specific test scenario to verify any requirement. 

In test automation, assertion is the validation step that determines whether the automated test case succeeded or not.

#### What is TDD? What are the benefits?
Test Driven Development is a software development practice enabling developers to create proper specifications about how their code should be written and implemented. Fundamentally, TDD is a practice when a programmer writes a functional test before building a code.

Advantages
- Better program design and higher code quality
- TDD reduces the time required for project development
- Code flexibility and easier maintenance
#### What are the unit testing best practices? (Eg. how many assertion should a test case contain?)
Usually, a good test is:

- Trustworthy. That means that it fails only if it is broken. If tests can sometimes fail then it is flaky and can’t be called a good test.
Readable/maintainable. From reading a test, it should be clear what it tests and how it is done. It should have no boilerplate or tricky tweaks of state or control.

- Should verify a single use case. This is related to the single responsibility principle. If a test verifies multiple cases then if it fails, we can’t say why exactly. A good test verifies a single use case and when it fails, we immediately know what went wrong.
- 
- Isolated. The test should not be able to influence other tests. This particularly implies that tests should not share a global state. If tests are not isolated, then the order in which they are executed can lead to unexpected results.
#### What is arrange/act/assert pattern?
Apattern for arranging and formatting code in UnitTest methods:

Each method should group these functional sections, separated by blank lines:

- Arrange all necessary preconditions and inputs.
- Act on the object or method under test.
- Assert that the expected results have occurred.
### DevOps
#### What is continuous integration? Why is CI important?
Developers practicing continuous integration merge their changes back to the main branch as often as possible. The developer's changes are validated by creating a build and running automated tests against the build. By doing so, you avoid the integration hell that usually happens when people wait for release day to merge their changes into the release branch.
#### Why are tests important in the CI workflow?
Continuous integration puts a great emphasis on testing automation to check that the application is not broken whenever new commits are integrated into the main branch.
#### Name some software that help the CI workflow!
Jenkins, Travis CI, GitLab Ci
#### What is Continuous Delivery?
Continuous delivery is an extension of continuous integration to make sure that you can release new changes to your customers quickly in a sustainable way. This means that on top of having automated your testing, you also have automated your release process and you can deploy your application at any point of time by clicking on a button.
#### What is Continuous Deployment?
Continuous deployment goes one step further than continuous delivery. With this practice, every change that passes all stages of your production pipeline is released to your customers. There's no human intervention, and only a failed test will prevent a new change to be deployed to production.

Continuous deployment is an excellent way to accelerate the feedback loop with your customers and take pressure off the team as there isn't a Release Day anymore. Developers can focus on building software, and they see their work go live minutes after they've finished working on it.

#### What is DevOps?
DevOps is the combination of cultural philosophies, practices, and tools that increases an organization’s ability to deliver applications and services at high velocity: evolving and improving products at a faster pace than organizations using traditional software development and infrastructure management processes. This speed enables organizations to better serve their customers and compete more effectively in the market.



### Software Methodologies
#### What kind of software-lifecycle models do you know?
Waterfall, Agile
#### What is a UML diagram? What kind of diagram types do you know?
UML is an acronym that stands for Unified Modeling Language. Simply put, UML is a modern approach to modeling and documenting software. In fact, it’s one of the most popular business process modeling techniques.

Types:
- Activity Diagram
- Use Case Diagram
- State Machine UML diagram
- Class Diagram
#### What is a UML class diagram? What are the typical elements?
In a nutshell, class diagrams contain classes, alongside with their attributes (also referred to as data fields) and their behaviors (also referred to as member functions). More specifically, each class has 3 fields: the class name at the top, the class attributes right below the name, the class operations/behaviors at the bottom. The relation between different classes (represented by a connecting line), makes up a class diagram.
#### What kind of design patterns do you know? Bring at least 3 examples.
- Factory Pattern: In Factory pattern, we create object without exposing the creation logic to the client and refer to newly created object using a common interface.
- Singleton: This pattern involves a single class which is responsible to create an object while making sure that only single object gets created. This class provides a way to access its only object which can be accessed directly without need to instantiate the object of the class.
- Data Access Object:  is used to separate low level data accessing API or operations from high level business services.
#### What is the purpose of the Iterator Pattern?
This pattern is used to get a way to access the elements of a collection object in sequential manner without any need to know its underlying representation.
#### What do you know about the SOLID principles?
SOLID is a mnemonic acronym for five design principles intended to make software designs more understandable, flexible and maintainable.

S — Single Responsibility: If a Class has many responsibilities, it increases the possibility of bugs because making changes to one of its responsibilities, could affect the other ones without you knowing.

O — Open-Closed: Changing the current behaviour of a Class will affect all the systems using that Class.
If you want the Class to perform more functions, the ideal approach is to add to the functions that already exist NOT change them.

L — Liskov Substitution: If you have a Class and create another Class from it, it becomes a parent and the new Class becomes a child. The child Class should be able to do everything the parent Class can do. This process is called Inheritance.
The child Class should be able to process the same requests and deliver the same result as the parent Class or it could deliver a result that is of the same type.

I — Interface Segregation: A Class should perform only actions that are needed to fulfil its role. Any other action should be removed completely or moved somewhere else if it might be used by another Class in the future.

D — Dependency Inversion: This principle says a Class should not be fused with the tool it uses to execute an action. Rather, it should be fused to the interface that will allow the tool to connect to the Class.
#### How would you separate data storage code and business logic code (which uses stored data) in an application?
With the MVC pattern or DAO pattern

## Computer science

### Data Structures
#### What is the difference between Stack and Queue data structure?
Stack works on the FIFO principle(First in First Out) while a Queue works on the LIFO principle (Last in First Out)
#### What is a graph? What are simple graphs? What are directed graphs? What are weighted graphs?
A graph is a pictorial representation of a set of objects where some pairs of objects are connected by links. The interconnected objects are represented by points termed as vertices, and the links that connect the vertices are called edge

- Simple Graph: A graph with no loops and no parallel edges is called a simple graph.
- Directed Graphs: A graph where edges have orientations from one node to the other
- Weigthed Graphs: A graph where edges have a cost associated to them
#### What are trees? What are binary trees? What are binary search trees?
- Tree: An acyclic graph
- Binary Tree: A tree where each node has at most 2 children
- Binary Search Tree: A binary tree where all children of the root smaller than it are on its left subtree while all the children bigger than the root are on the right subtree
#### How can you store graphs in programs? What are the advantages/disadvantages per each?


- Storing nodes as objects with pointers to one another

The memory complexity for this approach is O(n) because you have as many objects as you have nodes. The number of pointers (to nodes) required is up to O(n^2) as each node object may contain pointers for up to n nodes.
The time complexity for this data structure is O(n) for accessing any given node.

- Storing a matrix of edge weights

This would be a memory complexity of O(n^2) for the matrix.
The advantage with this data structure is that the time complexity to access any given node is O(1).
#### What are graph traversal algorithms? What is BFS, how does it work? What is DFS, how does it work?
A graph traversal alghoritm is a set of instructions used to go through nodes of the graph

A depth-first search (DFS) explores a path all the way to a leaf before backtracking and exploring another path. 
- Takes less memory
- The disadvantages are that it takes longer, and will not always find the shortest path
- Can get struck if Tree has loops
- Uses stack as underlying data structure

A breadth-first search (BFS) explores nodes nearest the root before exploring nodes further away
- Will Always find shortest path
- Can Deal with Looping Structures
- Takes lot of memory
- Uses queue as underlying data structure

#### How does dictionary work?
The Dictionary class in C# represents a generic data structure that can contain keys and values of data. Hence, you can store data of any type in a Dictionary instance.
#### Why is it important for keys in a hashmap to have an immutable type? (Consider string for example.)
If immutable, the object's hashcode wont change and it allows caching the hashcode of different keys which makes the overall retrieval process very fast.

### Algorithms
#### What is QuickSort? Describe the main logic of this sorting algorithm.
QuickSort is a Divide and Conquer algorithm. It picks an element as pivot and partitions the given array around the picked pivot.

The key process in quickSort is partition(). Target of partitions is, given an array and an element x of array as pivot, put x at its correct position in sorted array and put all smaller elements (smaller than x) before x, and put all greater elements (greater than x) after x. All this should be done in linear time.


## Software design

### Security

#### What is OAuth2?
OAuth 2 is an authorization framework that enables applications to obtain limited access to user accounts on an HTTP service, such as Facebook, GitHub, and DigitalOcean. It works by delegating user authentication to the service that hosts the user account, and authorizing third-party applications to access the user account. OAuth 2 provides authorization flows for web and desktop applications, and mobile devices.
#### What is Basic Authentication?
Basic authentication is a simple authentication scheme built into the HTTP protocol. The client sends HTTP requests with the Authorization header that contains the word Basic word followed by a space and a base64-encoded string username:password.
#### What is CORS, why it’s needed in browsers?
Cross-Origin Resource Sharing (CORS) is a mechanism that uses additional HTTP headers to tell browsers to give a web application running at one origin, access to selected resources from a different origin. A web application executes a cross-origin HTTP request when it requests a resource that has a different origin (domain, protocol, or port) from its own.

The CORS standard is needed because it allows servers to specify not just who can access its assets, but also how the assets can be accessed.

Cross-origin requests are made using the standard HTTP request methods. Most servers will allow GET requests, meaning they will allow resources from external origins (say, a web page) to read their assets. HTTP requests methods like PATCH, PUT, or DELETE, however, may be denied to prevent malicious behavior. For many servers, this is intentional. For example, it is likely that server A does not want servers B, C, or D to edit or delete its assets.

With CORS, a server can specify who can access its assets and which HTTP request methods are allowed from external resources.

#### How can you initialize a CSRF attack?
Cross site request forgery (CSRF), also known as XSRF, Sea Surf or Session Riding, is an attack vector that tricks a web browser into executing an unwanted action in an application to which a user is logged in.

CSRFs are typically conducted using malicious social engineering, such as an email or link that tricks the victim into sending a forged request to a server. As the unsuspecting user is authenticated by their application at the time of the attack, it’s impossible to distinguish a legitimate request from a forged one.
#### What is JWT used for? Where to store it on client side?
JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA

It is recommended that you store your JWT in cookies for web applications, because of the additional security they provide, and the simplicity of protecting against CSRF with modern web frameworks. HTML5 Web Storage is vulnerable to XSS, has a larger attack surface area, and can impact all application users on a successful attack.
### Threaded programming

#### When do you need to use threads in an application?
When an application needs do do multiple things at once like fetching data from a server and keeping the ui active, or when timers or other clocked events are used.
#### What is a daemon thread?
Daemon thread is a low priority thread (in context of JVM) that runs in background to perform tasks such as garbage collection (gc) etc.
#### What is the difference between concurrent and parallel execution of code?
A system is said to be concurrent if it can support two or more actions in progress at the same time. A system is said to be parallel if it can support two or more actions executing simultaneously.

Concurrency means executing multiple tasks at the same time but not necessarily simultaneously. There are two tasks executing concurrently, but those are run in a 1-core CPU, so the CPU will decide to run a task first and then the other task or run half a task and half another task, etc. Two tasks can start, run, and complete in overlapping time periods i.e Task-2 can start even before Task-1 gets completed. It all depends on the system architecture.

Parallelism means that an application splits its tasks up into smaller subtasks which can be processed in parallel, for instance on multiple CPUs at the exact same time.

#### What is the most important problem developers are faced when using threads?
Thread synchronization
#### In what kind of situations can deadlocks occur?
In an operating system, a deadlock occurs when a process or thread enters a waiting state because a requested system resource is held by another waiting process, which in turn is waiting for another resource held by another waiting process.

A deadlock occurs when

- A limited number of a particular resource.
- The ability to hold one resource and request another.
- No preemption capability - this means that one thread can't force another thread to release a lock.
- A circular wait condition - This means that there is a cycle of threads, each of which is waiting for the next to release a resource before it can continue.
#### What are possible ways to prevent deadlocks from occurring?
Deadlocks can be avoided by avoiding at least one of the four conditions, because all this four conditions are required simultaneously to cause deadlock.

- Mutual Exclusion
Resources shared such as read-only files do not lead to deadlocks but resources, such as printers and tape drives, requires exclusive access by a single process.

- Hold and Wait
In this condition processes must be prevented from holding one or more resources while simultaneously waiting for one or more others.

- No Preemption
Preemption of process resource allocations can avoid the condition of deadlocks, where ever possible.

- Circular Wait
Circular wait can be avoided if we number all resources, and require that processes request resources only in strictly increasing(or decreasing) order.
#### What does critical section or critical region mean in the context of concurrent programming?

- When more than one processes access a same code segment that segment is known as critical section. Critical section contains shared variables or resources which are needed to be synchronized to maintain consistency of data variable.
- In simple terms a critical section is group of instructions/statements or region of code that need to be executed atomically such as accessing a resource (file, input or output port, global data, etc.).
- In concurrent programming, if one thread tries to change the value of shared data at the same time as another thread tries to read the value (i.e. data race across threads), the result is unpredictable.