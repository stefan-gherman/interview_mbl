# General enterprise questions

## Software engineering

### Architectures

#### What is n-tier (or multi-tier) architecture?
#### What are microservices? Advantages and disadvantages?
#### What is Separation of Concerns?
#### What is a layered design and why is it important in enterprise applications?
#### What is Dependency Injection?
#### What is the DAO pattern? When and how to implement?
#### What is SOA? When to use?

### Testing
#### What are unit test, integration test, system test, regression test, acceptance test? What is the major difference between these?
#### What is code coverage? Why is it used? How you can measure?
#### What does mocking mean? How would you do it 'manually' (i. e. without using any fancy framework)?
#### What is a test case? What is an assertion? Give examples!
#### What is TDD? What are the benefits?
#### What are the unit testing best practices? (Eg. how many assertion should a test case contain?)
#### What is arrange/act/assert pattern?

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
#### What is a UML diagram? What kind of diagram types do you know?
#### What is a UML class diagram? What are the typical elements?
#### What kind of design patterns do you know? Bring at least 3 examples.
#### What is the purpose of the Iterator Pattern?
#### What do you know about the SOLID principles?
#### How would you separate data storage code and business logic code (which uses stored data) in an application?

## Computer science

### Data Structures
#### What is the difference between Stack and Queue data structure?
#### What is a graph? What are simple graphs? What are directed graphs? What are weighted graphs?
#### What are trees? What are binary trees? What are binary search trees?
#### How can you store graphs in programs? What are the advantages/disadvantages per each?
#### What are graph traversal algorithms? What is BFS, how does it work? What is DFS, how does it work?
#### How does dictionary work?
#### Why is it important for keys in a hashmap to have an immutable type? (Consider string for example.)

### Algorithms
#### What is QuickSort? Describe the main logic of this sorting algorithm.

## Software design

### Security

#### What is OAuth2?
#### What is Basic Authentication?
#### What is CORS, why it’s needed in browsers?
#### How can you initialize a CSRF attack?
#### What is JWT used for? Where to store it on client side?

### Threaded programming

#### When do you need to use threads in an application?
#### What is a daemon thread?
#### What is the difference between concurrent and parallel execution of code?
#### What is the most important problem developers are faced when using threads?
#### In what kind of situations can deadlocks occur?
#### What are possible ways to prevent deadlocks from occurring?
#### What does critical section or critical region mean in the context of concurrent programming?
