# Web with Python questions

## Software design

### Clean code

#### Point out 5 suggestions, how to format an SQL query!
<ul>
<li>Language specific words should be typed in all caps</li>
<li>Table names should be typed with lowercase letters.</li>
<li>Write keywords on a new line.</li>
<li>When selecting multile columns from different tables, write them as {tableName}.{columnName} in order to avoid confusion.</li>
<li>Use as statement when using aggregate functions</li>
</ul>

#### What layers can you name in a simple web application?
<p>
<ul>
<li>
    User Interface
</li>
<li>
    Business Logic
</li>
<li>
    Data Acess
</li>
</ul>
</p>

### Error handling
#### What error can occur, when an array does not have an element on the requested index?
<p>
    Undefined error
</p>

#### What is the “finally” block, and how would you use it?
<p>
    It is a block that gets executed after the try block ends its execution. It is often used to perform clean up actions as it gets executed in all situations. 
</p>

#### Why should we catch special exception types?
<p>
Because, if we don't handle them, erronuos execution may propagate throughout the program, also it is reccomended to catch all exceptions 
</p>

### Security
#### What is SQL injection? How to protect an application against it?

<p>
    SQL injection is a web security vulnerability that allows an attacker to interfere with the queries that an application makes to its database. It generally allows an attacker to view data that they are not normally able to retrieve.
</p>

<p>
    Most instances of SQL injection can be prevented by using parameterized queries (also known as prepared statements) instead of string concatenation within the query.
    To sanitize data is basically to convert all characters to ”harmless” encoded characters so that symbols like # $ ? /” \” don't pass through directly to the processing part of the script.
</p>

#### What is XSS? How to protect an application against it?
<p>
    Cross-Site Scripting (XSS) attacks are a type of injection, in which malicious scripts are injected into otherwise benign and trusted websites. XSS attacks occur when an attacker uses a web application to send malicious code, generally in the form of a browser side script, to a different end user. 
</p>

<p>
        In order to prevent one can filter user input, encode output data, or disable cookie trace.
</p>

#### How to properly store passwords?
<p>
    Passwords must be stored in a hashed format.
</p>

#### What is HTTPS?
<p>
    HTTPS stands for Hypertext Transfer Protocol Secure. It is the protocol where encrypted HTTP data is transferred over a secure connection. By using secure connection such as Transport Layer Security or Secure Sockets Layer, the privacy and integrity of data are maintained and authentication of websites is also validated.
</p>

#### What is encryption and decryption?
<p>
<strong>Encryption:</strong>is the method by which information is converted into secret code that hides the information's true meaning. 
</p>
<p>
<strong>Decryption:</strong>is the process of taking encoded or encrypted text or other data and converting it back into a format than can be read and understood.
</p>

#### What is hashing?
<p>
    Hashing is generating a value or values from a string of text using a mathematical function.
</p>

#### What is the difference between encryption and hashing? When would you use which?
<p>
    Whereas encryption is a two-way function, hashing is a one-way function. While it’s technically possible to reverse-hash something, the computing power required makes it unfeasible. Hashing is one-way.
Now, whereas encryption is meant to protect data in transit, hashing is meant to verify that a file or piece of data hasn’t been altered—that it is authentic. In other words, it serves as a check-sum.
</p>

<p>
    Encryption can be used to store files or folders on a remote location whereas Hashing may be used when storing a password or when generating a checksum for a file. 
</p>

#### What encryption methods do you know?
<p>AES – Advanced Encryption Standard, ECC – Elliptic Curve Cryptography, RSA – Rivest-Shamir-Adlemen</p>

#### What hashing methods do you know?
<p>SHA, MD5</p>

#### How/where would you store sensitive data (like db password, API key, ...) of your application?

<p>In an encrypted file in an encrypted folder on another server than the one on which the rest of the app is being hosted.
</p>

## Computer science

### Algorithms

#### What is the difference between Stack and Queue data structure?
<p>
    A stack is a data structure where the last added element is the first to be removed (LIFO), whereas a queue is a data structure where the first added element is the first to be removed (FIFO).
</p>

#### What is BubbleSort? Describe the main logic of this sorting algorithm.
<p>Bubble Sort is the simplest sorting algorithm that works by repeatedly swapping the adjacent elements if they are in wrong order.</p>

#### Explain the process of finding the maximum and minimum value in a list of numbers!\

        minimum:
    
        let minNumber = array[0];

        for (let num of array){
            if(minNumber > num){
                minNumber = num;
            }
        }

   
    maximum: 
  
    let maxNumber = array[0];

        for (let num of array){
            if(maxNumber < num){
                maxNumber = num;
            }
        }

#### Explain the process of calculating the average value in an array of numbers!
<p>
The sum of all the numbers in the array is divided by the length of the array.
</p>

#### What is Big O complexity? Explain time and space complexity!

<p>
Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.
</p>

<p>
Time complexity of an algorithm quantifies the amount of time taken by an algorithm to run as a function of the length of the input.
</p>

<p>
Space complexity of an algorithm quantifies the amount of space or memory taken by an algorithm to run as a function of the length of the input.
</p>

#### Explain the process of calculating the average value in a linked list of numbers!
<p>
    The process is similar to the one for an array.
</p>

### Procedural
#### How the CASE condition works in SQL?
<p>
It works exactly like an if in other programming languages
</p>

#### How the switch-case condition works in JavaScript?
<p>
It works like a multi branch if structure where the condition is encapsulated inside a switch statement while the possible results are written after case statements.
</p>

#### How to achieve a switch-case-like structure in Python?

<p>
With multiple elif statements.
</p>

#### Explain variable scoping in Python!
<p>
    A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.
</p>

<p>
    A variable created in the main body of the Python code is a global variable and belongs to the global scope.

Global variables are available from within any scope, global and local.
</p>

#### What’s the difference between const and var in JavaScript?
<p>var declarations are globally scoped or function/locally scoped, can be redeclared and updated, while const (introduced in ES6) are only block scoped and can't be updated and redeclared. Also const must be initialized after it is declared.</p>

#### How the list comprehension looks like in Python?
<p>
    [ expression for item in list if conditional ]
</p>

#### How the “ternary expression” looks like in Python?
<code>
    min = a if a < b else b 
</code>

#### How the ternary expression looks like in JavaScript?
<code>
    a === 3 ? a = 4 : a= 5;
</code>

#### How to import a function from another module in Python?
<code>
    import function_name from module
</code>

#### How to import a function from another module in JavaScript?
<p>First the function must have the export keyword typed before declaration.</p>
<code>
    import {fumctionName} from 'module.js'
</code>

### Functional
#### What is recursion?
<p>
    The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. 
</p>

#### Write a recursive function which calculates the Fibonacci numbers!

<code>
    def fibonacci(n):
        if n < 0:
            ValueError("Input 0 or greater only!")
        if n <= 1:
            return n
        return fibonacci(n - 1) + fibonacci(n - 2)
</code>

#### How to store a function in a variable in Python?
<code>
    def return_num(num):
        return num
    a = return_num    
</code>

#### List the ways of defining a callable logical unit in JavaScript!
<ul>
<li>arrow function</li>
<li> const + arrow function </li>
<li>function name</li>
</ul>

#### What is an event listener? How to attach one?

<p>
    An event listener is a procedure in JavaScript that waits for an event to occur.
</p>

<code>
    const playButton = document.getElementByID('startButton');
    play.addEventListener('click', function(){
        //some logic
    });
</code>

#### How to trigger an event in JavaScript?
<p>
By acting upon the element that has the event listener attached to it with the corresponding key or mouse event.
</p>

#### What is a callback function? Tell some examples of its usage.

<p>
A callback is a function that is to be executed after another function has finished executing.
</p>

<p>A callback may be used on an event listener or on a window function such as setTimeout()</p>

#### What is a Python decorator? How does it work? Tell some examples of its usage.
    
<p>
    Decorators allow us to wrap another function in order to extend the behavior of wrapped function, without permanently modifying it.
</p>

<p>
In Decorators, functions are taken as the argument into another function and then called inside the wrapper function.
</p>
<p>
Database Connection, password hashing, queries, routing.  
</p>

#### What is the difference between synchronous and asynchronous execution?
<p>
    When you execute something synchronously, you wait for it to finish before moving on to another task. When you execute something asynchronously, you can move on to another task before it finishes.
</p>

## Programming languages

### SQL

#### How can you connect your application to a database server? What are the possible ways?
<p>
    Via \connect command from psql, from the ui of PyCharm, or with the use of a function.
</p>

#### When do you use the DISTINCT keyword in SQL?
<p>
    You may use DISTINCT when data from a query repeats itself, ex: array_agg(DISTINCT names.first_name)
</p>

#### What are aggregate functions in SQL? Give 3 examples.
<p>
    An aggregate function performs a calculation on a set of values, and returns a single value ,ex: SUM, AVG, COUNT
</p>

#### What kind of JOIN types do you know in SQL? Could you give examples?
<p>
JOIN(data from both tables is displayed if a match is found), LEFT/RIGHT JOIN (data from one table is displayed regardless if a match is found in the other table.)
</p>

#### What are the constraints in sql?
<p>
    Rules applied to table data.
</p>

#### What is a cursor in SQL? Why would you use one?
<p>
    A database cursor is an object that enables traversal over the rows of a result set. It allows you to process individual row returned by a query.
</p>

#### What are database indexes? When to use?

<p>
    Indexes are special lookup tables that the database search engine can use to speed up data retrieval. Simply put, an index is a pointer to data in a table. An index in a database is very similar to an index in the back of a book.
</p>

#### What are database transactions? When to use?
<p>
    A transaction is a unit of work that is performed against a database. Transactions are units or sequences of work accomplished in a logical order, whether in a manual fashion by a user or automatically by some sort of a database program.
</p>

#### What kind of database relations do you know? How to define them?
<p>
    1:1, 1:Many, Many:Many
</p>

#### You have a table with an “address” field which contains data like “3525, Miskolc, Régiposta 9.” (postcode, city, street name and address). How would you query all records related to Miskolc?
<code>
    SELECT *
    FROM address
    WHERE city = 'Miskolc';
</code>

#### How would you keep track of what kind of data has changed after an UPDATE or DELETE operation in a table?
<p>
    Implementing a log system or having a separate table where you store changes.
</p>

### HTML & CSS

#### What’s the difference between XML, XHTML and HTML?
<p>
    HTML is the HyperText Markup Language, which is designed to create structured documents and provide for semantic meaning behind the documents. HTML5 is the next version of the HTML specification.
</p>
<p>
    XML is the Extensible Markup Language, which provides rules for creating, structuring, and encoding documents. You often see XML being used to store data and to allow for communication between applications. It's programming language-agnostic - all of the major programming languages provide mechanisms for reading and writing XML documents, either as part of the core or in external libraries.
</p>

<p>
    XHTML is an XML-based HTML. It serves the same function as HTML, but with the same rules as XML documents. These rules deal with the structure of the markup.
</p>

#### How to include a JavaScript file in a webpage?

<p>
<code>
< script src = "myscript.js" > < /script >
</code>
</p>

#### How to include a CSS file in a webpage?
<p>
    By linking it in the head of the html document.
</p>

#### How to select an element using its id in CSS?
<code>
    elem #id
</code>

#### How to select elements using their class in CSS?
<code>
    elem .class
</code>

#### How to select elements which have the ‘alpha’ and ‘beta’ classes in CSS?

<code>
    .alpha.beta
</code>

#### How to select all list items in all ordered lists on the page in CSS?
<code>
 ol li {}
 </code>

#### How to select elements using their attributes in CSS?
<code>element[attribute = 'value'] </code>

#### What are UX and UI?
 <p>
  UX - the way user interracts with the application, its ease of use, responsiveness
 </p>
 
 <p>
    UI - the way the app looks and feels.
 </p>

#### Please list some points that an application should fulfill to have good UX.
<p>
 Use menus for navigation, add buttons with clear concise text of what their purpose is.
</p>

#### What is XML, XSLT, DTD?
<p>
    XSL (eXtensible Stylesheet Language) is a styling language for XML.
</p>
    
<p>
    A DTD is a Document Type Definition.

    A DTD defines the structure and the legal elements and attributes of an XML document.
</p>


#### What is the difference between HTML and XML?
<p>
       HTML is the HyperText Markup Language, which is designed to create structured documents and provide for semantic meaning behind the documents. HTML5 is the next version of the HTML specification.
</p>

<p>
     XML is the Extensible Markup Language, which provides rules for creating, structuring, and encoding documents. You often see XML being used to store data and to allow for communication between applications. It's programming language-agnostic - all of the major programming languages provide mechanisms for reading and writing XML documents, either as part of the core or in external libraries.
</p>

### Javascript

#### What is javascript?
<p>
    A programming language used mainly on the web
</p>

#### When to use AJAX? Bring examples of its usage.

<p>
    AJAX may be used when fetching something from an api endpoint, or from a local database.
</p>

#### What is DOM and how to manipulate it from Javascript?
<p>
    The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.
</p>

<code>
    document.getElementByID('id1').setAttribute('title', 'New Title')
</code>

#### What are events and how/why to use them in Javascript?
<p>
Events are a part of the Document Object Model (DOM) Level 3 and every HTML element contains a set of events which can trigger JavaScript Code.
</p>

#### What is event bubbling/capturing? How would you use it?
<p>
    When an event happens on an element, it first runs the handlers on it, then on its parent, then all the way up on other ancestors. It may used when certain elements trigger the same event on the parent.
</p>

#### What is JSON and how do we use it?
<p>
    JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate. It may be used when exchanging data with a server, api, .etc
</p>

## Software engineering

### Version control

#### What type of branching strategy would you use?
#### What would you do if you find a bug on the production code (master branch)?
#### How can you move changes from one branch to another in GIT?
#### How does a VCS help with code reviews?
#### What is your favorite git command? Why?
#### What does remote/local mean in Git? 

### DevOps

#### Why is it good to use a package manager software?
#### Why is it good to use a virtual environment for a project?

### Networks

#### What kind of HTTP status codes do you know?
#### What is a API?
#### What is REST API?
#### What is JSON? When to use?
#### What is TCP/IP? What layers does it define, what are they responsible for?
#### What’s the difference between TCP and UDP?
#### How does an HTTP Request look like? What are the most relevant HTTP header fields?
#### How does an HTTP Response look like? What are the most relevant HTTP header fields?
#### What is DNS? How does it work?
#### What is a web server?
#### Explain the client-server architecture.
#### What would you use a session for?
#### What would you use a cookie for?

## Software Development Methodologies

#### What kind of software development methodologies do you know? What are the main features of these?
#### What are the SCRUM roles?
#### What are the SCRUM ceremonies?
#### What are the SCRUM artifacts?
#### What is the main goal of a retrospective meeting?
#### Explain, when would you recommend to use the waterfall methodology?
