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
#### Explain the process of calculating the average value in a linked list of numbers!

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
#### What’s the difference between const and var in JavaScript?
#### How the list comprehension looks like in Python?
#### How the “ternary expression” looks like in Python?
#### How the ternary expression looks like in JavaScript?
#### How to import a function from another module in Python?
#### How to import a function from another module in JavaScript?

### Functional
#### What is recursion?
#### Write a recursive function which calculates the Fibonacci numbers!
#### How to store a function in a variable in Python?
#### List the ways of defining a callable logical unit in JavaScript!
#### What is an event listener? How to attach one?
#### How to trigger an event in JavaScript?
<p>
By acting upon the element that has the event listener attached to it with the corresponding key or mouse event.
</p>

#### What is a callback function? Tell some examples of its usage.
#### What is a Python decorator? How does it work? Tell some examples of its usage.
#### What is the difference between synchronous and asynchronous execution?

## Programming languages

### SQL

#### How can you connect your application to a database server? What are the possible ways?
#### When do you use the DISTINCT keyword in SQL?
#### What are aggregate functions in SQL? Give 3 examples.
#### What kind of JOIN types do you know in SQL? Could you give examples?
#### What are the constraints in sql?
#### What is a cursor in SQL? Why would you use one?
#### What are database indexes? When to use?
#### What are database transactions? When to use?
#### What kind of database relations do you know? How to define them?
#### You have a table with an “address” field which contains data like “3525, Miskolc, Régiposta 9.” (postcode, city, street name and address). How would you query all records related to Miskolc?
#### How would you keep track of what kind of data has changed after an UPDATE or DELETE operation in a table?

### HTML & CSS

#### What’s the difference between XML, XHTML and HTML?
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
#### How to select elements using their class in CSS?
#### How to select elements which have the ‘alpha’ and ‘beta’ classes in CSS?
#### How to select all list items in all ordered lists on the page in CSS?
#### How to select elements using their attributes in CSS?
#### What are UX and UI?
#### Please list some points that an application should fulfill to have good UX.
#### What is XML, XSLT, DTD?
#### What is the difference between HTML and XML?

### Javascript

#### What is javascript?
#### When to use AJAX? Bring examples of its usage.
#### What is DOM and how to manipulate it from Javascript?
#### What are events and how/why to use them in Javascript?
#### What is event bubbling/capturing? How would you use it?
#### What is JSON and how do we use it?

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
