# Enterprise module (C# branch)

### ASP.NET Core, WCF

#### What Is the difference between .NET Core and .NET Standard? How do them relate to “classic” .NET?
.NET Core is a free, cross-platform, open source implementation of the managed framework. It supports four types of applications: console, ASP.NET Core, cloud, and Universal Windows Platform (UWP)

.NET Standard is a specification for implementing the BCL. Since a .NET implementation is required to follow this standard, application developers will not have to worry about different versions of the BCL for each managed framework implementation.

The relationship between .NET Standard and a .NET implementation is the same as between the HTML specification and a browser. The second is an implementation of the first.
#### What is ASP.NET MVC?
ASP.NET MVC is basically a web development framework from Microsoft, which combines the features of MVC (Model-View-Controller) architecture, the most up-to-date ideas and techniques from Agile development, and the best parts of the existing ASP.NET platform.
#### Can you explain Model, Controller and View in MVC?
- The Model − A set of classes that describes the data you are working with as well as the business logic.

- The View − Defines how the application’s UI will be displayed. It is a pure HTML, which decides how the UI is going to look like.

- The Controller − A set of classes that handles communication from the user, overall application flow, and application-specific logic.
#### Explain the page lifecycle of MVC.

#### What is Razor View Engine?
#### What you mean by Routing in MVC?
#### What is Layout in MVC?
#### What ConfigureServices() method does in Startup.cs?
#### What Configure() method does in Startup.cs?
#### What is wwwroot folder in ASP.NET Core?
#### What’s the usage of [InternalsVisibleTo] attribute? What are pros and cons of it?
#### Explain what is WCF?
Windows Communication Foundation (WCF) is a framework for building service-oriented applications. Using WCF, you can send data as asynchronous messages from one service endpoint to another. A service endpoint can be part of a continuously available service hosted by IIS, or it can be a service hosted in an application. An endpoint can be a client of a service that requests data from a service endpoint. The messages can be as simple as a single character or word sent as XML, or as complex as a stream of binary data
#### Mention what is the endpoint in WCF and what are the three major points in WCF?
It defines the address where a message is to be sent or received. It also specifies the communication mechanism to describe how the messages will be sent along with defining the set of messages.

- Address: Specifies the location of the service which will be like http://Myserver/MyService.Clients will use this
location to communicate with our service.
- Contract: Specifies the interface between client and the server. It’s a simple interface with some attribute.
- Binding  Specifies how the two paries will communicate in term of transport and encoding and protocols
#### Object Relational Mapping, Entity Framework
#### What is an ORM? What are benefits, when to use?
Object-Relational Mapping (ORM) is a technique that lets you query and manipulate data from a database using an object-oriented paradigm

An ORM library is a completely ordinary library written in your language of choice that encapsulates the code needed to manipulate the data, so you don't use SQL anymore; you interact directly with an object in the same language you're using.

Advantages
- You write your data model in only one place, and it's easier to update, maintain, and reuse the code.
- A lot of stuff is done automatically,
- You don't have to write sql
- Sanitizing; using prepared statements or transactions are as easy as calling a method

When to use: Speeding development. For example, eliminating repetitive code like mapping query result fields to object members and vice-versa.
#### What is Entity Framework? What are the advantages, limitations?
Entity Framework is an Object Relational Mapper (ORM) which is a type of tool that simplifies mapping between objects in your software to the tables and columns of a relational database.

Advantages of Entity Framework
- It provides auto generated code
- It reduce development time
- It reduce development cost
- It enables developers to visually design models and mapping of database
- It provides capability of programming a conceptual model.
- It provides unique syntax (LINQ / Yoda) for all object queries whether it is database or not
- It allow multiple conceptual models to mapped to a single storage schema
- It’s easy to map business objects (with drag & drop tables).

Disadvantages of Entity Framework
- Lazy loading is the main drawbacks of EF
- Its syntax is complicated
- Its logical schema is not able to understand business entities and relation among each other
- Logical schema of database is not capable of using certain parts of application
- It is not available for every RDMS
Need to handle data in nontraditional way
- It does not work if we change any schema of the database. We need to update the schema on the solution.
- It is not good for huge domain model.
#### What is lazy loading?
Lazy loading is the process whereby an entity or collection of entities is automatically loaded from the database the first time that a property referring to the entity/entities is accessed. Lazy loading means delaying the loading of related data, until you specifically request for it.
#### What is the difference between code first and DB first approach?
In code first the database and all the queries are built from the data model classes, essentially from the code.

In DB first approach the database is built first and all data models must be built afterwards by hand 
#### What is a migration script?
The migrations feature in EF Core provides a way to incrementally update the database schema to keep it in sync with the application's data model while preserving existing data in the database.

A migration script contains the required instructions in order to perform a migration(including table udates, key updates, etc)

#### What is a navigation property?
A property defined on the principal and/or dependent entity that references the related entity.

#### Name 3 different attributes used in EF Core, what can they do for you?
- *MaxLength*: The MaxLength attribute is applied to a property to specify a maximum number of characters or bytes for the column that the property should map to.
- *Required*: The Required attribute is applied to an entity property to configure the mapped database column as not nullable.
- *ForeignKey*: The ForeignKey attribute is used to specify which property is the foreign key in a relationship.