1.  Exception handling:  

    -   software application's reaction and recovery mechanisms in the event of an error.  

    -   Program or application doesn't crash and Maintains the regular execution flow 

    -   Recover smoothly 

    -   Provide us much information for the cause which caused it. 

    -   If occur again , can send the related data to error queue. 

2.  Performance issue 

3.  Difference between function and method : 

    If you have a function that is accessing/muttating the fields of your class, it becomes method. Otherwise, it is a function. 

4.  What is the [difference](https://www.mindprod.com/jgloss/interfacevsabstract.html) between [abstract class and interface in C#?](https://stackoverflow.com/questions/761194/interface-vs-abstract-class-general-oo) 

    multiple inheritance, default implementation, constants,third party convenience, s-a vs -able or can-do, plug-in, homogeneity, speed, terseness, adding functionality 

5.  [When to use an interface instead of an abstract class and vice versa](https://stackoverflow.com/questions/479142/when-to-use-an-interface-instead-of-an-abstract-class-and-vice-versa) 

    -   When we talk about abstract classes we are defining characteristics of an object type; specifying what an object is. 

    -   When we talk about an interface and define capabilities that we promise to provide, we are talking about establishing a contract about what the object can do. 

    -   [Use abstract clases and inheritance if you can make the statement "A is a B". Use interfaces if you can make the statement "A is capable of [doing] as", or also, abstract for what a class is, interface for what a class can do.](http://www.devfields.com/abstract-classes-and-interfaces/) 

    -   An abstract class can have shared state or functionality. An interface is only a promise to provide the state or functionality.  

    -   A good abstract class will reduce the amount of code that has to be rewritten because it's functionality or state can be shared. The interface has no defined information to be shared. 

    -   For example, an abstract base class is used for the template method design pattern, whereas an interface is used for the strategy design pattern. 

    -   An interface is a programming construct that defines a set of methods, properties, and events that a class or struct can implement to provide a certain functionality. 

    -   An abstract class is a class that is declared abstract---it may or may not include abstract methods. Abstract classes cannot be instantiated, but they can be subclassed. 

1.  SOLID 

2.  [Why solid is important](https://in.indeed.com/career-advice/interviewing/solid-principles-interview-questions#:~:text=Why%20is%20it%20important%20to%20utilise%20the%20SOLID%20design%20principles) ? 

    -   code that is logical, easy to read, convenient to maintain and possible to extend. That makes it easy to modify the software, add new features and make it more adaptable.' 

3.  Single responsibility  

4.  Open closed principle  

    1.  Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification. 

    2.  You should be able to extend a classes behaviour, without modifying it 

    3.  Some ways to do this include Polymorphism/Inheritance, Composition, Inversion of Control (a.k.a. DIP), Aspect-Oriented Programming, Patterns such as Strategy, Visitor, Template Method, and many other principles, patterns, and techniques of OOAD. 

5.  [Liskov substitute principle](https://youtu.be/8IaMgQkzhWM?t=1674)  

    1.  Definition : Substitutability is a principle in object-oriented programming stating that, in a computer program, if S is a subtype of T, then objects of type T may be replaced with objects of type S (i.e., an object of type T may be substituted with any object of a subtype S) without altering any of the desirable properties of the program (correctness, task performed, etc.).  

    2.  Let Φ(x) be a property provable about objects x of type T. Then Φ(y) should be true for objects y of type S where S is a subtype of T. 

    3.  some standard requirements 

        -   [Contravariance](https://blog.ndepend.com/covariance-and-contravariance-in-csharp-explained/) of method parameter types in the subtype. 

        -   Covariance of method return types in the subtype. 

    4.  restrictions 

        -   Preconditions cannot be strengthened in the subtype. 

        -   Postconditions cannot be weakened in the subtype. 

        -   Invariants must be preserved in the subtype. 

        -   History constraint 

    5.  5 rules of liscove 

        -   [Contravariance of method arguments in sub class and Covariance of return type in sub class](https://codeworx-web.azurewebsites.net/the-solid-principles/#:~:text=Contravariance%20of%20method%20arguments%20in%20sub,not%20the%20more%20generic%20type%20Car) 

        -   [No new exception types are allowed to be thrown, unless they are subclasses of previously used ones](https://codeworx-web.azurewebsites.net/the-solid-principles/#:~:text=No%20new%20exception%20types%20are%20allowed%20to%20be%20thrown%2C%20unless%20they%20are%20subclasses%20of%20previously%20used%20ones%0AMeans%20that%20if%20code%20that%20uses%20the%20baseclass%20might%20use%20try%20catch%20clauses%20for%20specific%20exceptions%20and%20if%20new%20ones%20comes%20along%20they%20might%20go%20through%20the%20catches%20and%20finally%20crash%20the%20system) 

        -   [Preconditions cannot be strengthend in a subclass and Postconditions cannot be weakend in a subclass](https://codeworx-web.azurewebsites.net/the-solid-principles/#:~:text=Preconditions%20cannot%20be%20strengthend,anymore%20in%20the%20subclass) 

        -   [The history constraint](https://codeworx-web.azurewebsites.net/the-solid-principles/#:~:text=The%20history%20constraint,by%20the%20subclass) 

        -   [Invariants of the baseclass must be preserved by the subclass](https://codeworx-web.azurewebsites.net/the-solid-principles/#:~:text=Invariants%20of%20the,rule%20is%20followed.) 

6.  Interface segregation principle  

7.  Dependency inversion principle  

    1.  The Dependency Inversion Principle (DIP) is a software design guideline which boils down to two recommendations about [de-coupling a class from its concrete dependencies](https://lostechies.com/derickbailey/2011/09/22/dependency-injection-is-not-the-same-as-the-dependency-inversion-principle/): 

        -   'High-level modules should not depend on low-level modules. Both should depend on abstractions.' 

        -   'Abstractions should not depend upon details. Details should depend upon abstractions.' 

        -   "Abstractions should not depend upon details" is that the design or blueprint of the system should not be influenced by the details of how the individual parts are made or where they come from. The design should only focus on what the parts do and how they fit together to create the desired functionality. 

        -   "Details should depend upon abstractions" means that the individual parts of the system should be designed in a way that conforms to the overall design or abstraction. This makes it easier to swap out or modify individual parts without affecting the overall functionality of the system, much like being able to swap out Lego pieces without affecting the overall design of the house. 

    2.  [Dependency Inversion](https://stackoverflow.com/questions/46709170/difference-between-dependency-injection-and-dependency-inversion#:~:text=an%20IoC%20Container)-,Dependency%20Inversion%20Principle%20(DIP),-Dependency%20Inversion%20is) is broadly about de-coupling concrete classes by preventing those classes having any direct reference to each other. 

    3.  boilerplate and singleton 

    4.  subclassing thing 

8.  [Dependency injection](https://stackoverflow.com/questions/130794/what-is-dependency-injection?rq=1)  

    1.  [What is it](https://www.jamesshore.com/v2/blog/2006/dependency-injection-demystified)?  

        -   A mechanism to invert the dependency from end user class to the beginning. 

        -   Dependency injection means giving an object its instance variables. 

        -   Dependency injection is basically providing the objects that an object needs (its dependencies) instead of having it construct them itself. 

    2.  Types of Dependency Injection 

        -   Constructor Injection 

        -   Property Injection 

        -   Method Injection 

    3.  It involves below type of classes: 

        -   Client Class: The client class (dependent class) is a class which depends on the service class 

        -   Service Class: The service class (dependency) is a class that provides service to the client class. 

        -   Injector Class: The injector class injects the service class object into the client class. 

    4.  Why do we need to use this? 

        -   Loose coupling -- app is not tightly coupled as it is not creating the object. 

        -   Mock dependency for testing 

        -   Last principle of solid 

9.  What is DI containers and how does they work. 

    1.  A DI Container is a framework to create dependencies and inject them automatically when required. DI Container helps us to manage dependencies within the application in a simple and easy way. 

    2.  a software library that that provides DI functionality and allows automating many of the tasks involved in Object Composition, Interception, and Lifetime Management. 

    3.  Lifecycle of the DI Containers --  

        -   Register 

        -   Resolve  

        -   Dispose 

    4.  A Composition Root is a (preferably) unique location in an application where modules are composed together. 

    5.  The Composer is the part of the Composition Root that does the actual construction of the object graphs. It's an important part of the Composition Root. The Composer is often a DI Container, but it can also be any method that constructs object graphs manually. 

    6.  [Why do we need it](https://stackoverflow.com/questions/871405/why-do-i-need-an-ioc-container-as-opposed-to-straightforward-di-code) [_2](https://blog.ploeh.dk/2012/11/06/WhentouseaDIContainer/)- your dependencies chain can become nested, and it quickly becomes unwieldy to wire them up manually. Even with factories, the duplication of your code is just not worth it. DI Container keeps it simple. 

10. Difference between DI & DIP 

    1.  Dependency Injection is an [Inversion of Control](https://en.wikipedia.org/wiki/Inversion_of_control) technique for supplying objects ('dependencies') to a class by way of the [Dependency Injection Design Pattern](https://www.martinfowler.com/articles/injection.html).   

    2.  The Dependency Inversion Principle (DIP) is a software design guideline which boils down to [de-coupling a class from its concrete dependencies](https://lostechies.com/derickbailey/2011/09/22/dependency-injection-is-not-the-same-as-the-dependency-inversion-principle/) 

    3.  Dependency Injection == "Gimme it" and Dependency Inversion == "Someone take care of this for me, somehow.". 

11. [What is IOC?](https://stackoverflow.com/questions/3058/what-is-inversion-of-control#:~:text=Inversion%20of%20Control%20is%20what%20you%20get%20when%20your%20program%20callbacks) 

    1.  [What is it](https://www.codeproject.com/Articles/592372/Dependency-Injection-DI-vs-Inversion-of-Control-IO#:~:text=caller%20program%20flow-,.,-DI%20provides%20objects)?-  

        -   IoC is a generic term meaning rather than having the application call the methods in a framework, the framework calls implementations provided by the application. 

        -   It is a practice where you let the actual behavior come from outside of the boundary (Class in Object Oriented Programming). The boundary entity only knows the abstraction (e.g interface, abstract class, delegate in Object Oriented Programming) of it. 

        -   IoC / DI to me is pushing out dependencies to the calling objects. 

    2.  Which problem does it solve? 

    3.  When is it appropriate to use and when not? 

    4.  basic techniques to implement inversion of control. These are: 

        -   Using a [service locator pattern](https://en.wikipedia.org/wiki/Service_locator_pattern) 

        -   Using [dependency injection](https://en.wikipedia.org/wiki/Dependency_injection);  

        -   Using a contextualized lookup 

        -   Using the [template method design pattern](https://en.wikipedia.org/wiki/Template_method_design_pattern) 

        -   Using the [strategy design pattern](https://en.wikipedia.org/wiki/Strategy_design_pattern) 

12. Composition Root : A Composition Root is a (preferably) unique location in an application where modules are composed together. 

13. Design patterns 

    Design patterns are typical solutions to commonly occurring problems in software design. They are like pre-made blueprints that you can customize to solve a recurring design problem in your code. 

14. Factory Method : 

    1.  What is it - Factory Method is a creational design pattern that provides an interface for creating objects in a superclass, but allows subclasses to alter the,आ%++ type of objects that will be created. 

    2.  allows an interface or a class to create an object, but let's subclasses decide which class or object to instantiate. 

    3.  The Factory Method pattern suggests that you replace direct object construction calls (using the new operator) with calls to a special factory method. 

    4.  Why we use it : 

    5.  Did you use it and what was the scenario ?  

15. Abstract Factory is a creational design pattern that lets you produce families of related objects without specifying their concrete classes 

16. Difference between factory, abstract factory and factory method 

    1.  The [Factory Method](https://refactoring.guru/pattern/factory-method) is a design pattern that relies on inheritance. If you make it static, you can no longer extend it in subclasses, which defeats the purpose of the pattern. 

    2.  When a static creation method returns new objects it becomes an alternative constructor. 

    3.  The Simple factory pattern  describes a class that has one creation method with a large conditional that based on method parameters chooses which product class to instantiate and then return. 

17. Singleton pattern : 

    1.  What is it. 

    2.  Why to use this 

    3.  Advantages and disadvantage 

    4.  Static vs singleton  

    5.  Usages of it 

18. [Strategy](https://refactoring.guru/design-patterns/strategy) 

    1.  What is it? 

    2.  Why should we use it? 

    3.  Did you use it and what was the scenario ? 

19. [Observer](https://refactoring.guru/design-patterns/observer) 

    1.  What is it? 

    2.  Why should we use it? 

    3.  Did you use it and what was the scenario ? 

20. [Chain of Responsibility](https://refactoring.guru/design-patterns/chain-of-responsibility) 

    1.  What is it? 

    2.  Why should we use it? 

    3.  Did you use it and what was the scenario ? 

21. [Adapter](https://refactoring.guru/design-patterns/adapter) 

    1.  What is it? 

    2.  Why should we use it? 

    3.  Did you use it and what was the scenario ? 

22. [Builder](https://refactoring.guru/design-patterns/builder) 

    1.  What is it? 

    2.  Why should we use it? 

    3.  Did you use it and what was the scenario ? 

1.  What is the Repository Pattern? 

    1.  Repository: Mediates between the domain and data mapping layers using a collection-like interface for accessing domain objects. 

    2.  Benefits of the Repository Pattern 

        1.  it abstracts the database behind it or decouples the application from persistence framework.  

        2.  Minimizes duplicate query logic. 

        3.  you can use dependency injection and make your code more testable. 

        4.  queries in a central place; otherwise your queries are scattered around and are harder to maintain. 

    3.  how does Repository Pattern work? 

        -   A layer between ORM(or Database) and application which keeps all the queries in one place and easy to maintain. All the calls to ORM or database are made from repository from the different methods. 

    4.  What is the Unit of Work Pattern?- A unit of work maintains a list of object affected by business  transaction and coordinates the writing off changes . 

    5.  Does Entity Framework Really Implement Repository and Unit of Work Patterns? 

        1.  DBSet and dbcontext work like repository and Unit of work but EF returns iqueryable which is used to query with different way. So implementing of repository . 

        2.  All the iqueryable all over the app means lots of query and hard to manage  

    6.  what is the difference between Repository Pattern and  Entity Framework ? 

        1.  EF returns iqueryable  while repository not. 

        2.  User can write some query to EF(will translate to DB) but not to repository. 

    7.  Why would you want to use a Repository Pattern with an ORM? 

        1.  iqueryable vs ienumerable 

        2.  All the orm query in repository only . 

        3.  Which leads to less duplicate code. 

        4.  Easily replacing the orm 

    8.  In OOP, what is the difference between the Repository Pattern and a Service Layer? 

    9.  Is Unit Of Work equals Transaction? 

        Unit of work is business transcation , not DB transaction. 

    10. What is an [Aggregate Root](https://stackoverflow.com/questions/1958621) in the context of Repository Pattern? 

        -   In the [Context of a Repository the Aggregate Root](https://stackoverflow.com/questions/1958621/whats-an-aggregate-root#:~:text=In%20the%20Context%20of%20a%20Repository%20the%20Aggregate%20Root%20is%20an%20Entity%20with%20no%20parent%20Entity.%20It%20contains%20zero%2C%20One%20or%20Many%20Child%20Entities%20whose%20existence%20is%20dependent%20upon%20the%20Parent%20for%20it%27s%20identity.%20That%27s%20a%20One%20To%20Many%20relationship%20in%20a%20Repository.%20Those%20Child%20Entities%20are%20plain%20Aggregates.) is an Entity with no parent Entity. It contains zero, One or Many Child Entities whose existence is dependent upon the Parent for it's identity. That's a One To Many relationship in a Repository. Those Child Entities are plain Aggregates. 

        -   [Aggregate Root is the mothership entity inside the aggregate](https://stackoverflow.com/questions/1958621/whats-an-aggregate-root#:~:text=Aggregate%20Root%20is%20the%20mothership%20entity%20inside%20the%20aggregate%20(in%20our%20case%20Computer)%2C%20it%20is%20a%20common%20practice%20to%20have%20your%20repository%20only%20work%20with%20the%20entities%20that%20are%20Aggregate%20Roots%2C%20and%20this%20entity%20is%20responsible%20for%20initializing%20the%20other%20entities.) (in our case Computer), it is a common practice to have your repository only work with the entities that are Aggregate Roots, and this entity is responsible for initializing the other entities. 

    11. How should I be grouping my Repositories when using Repository Pattern? 

        1.  [Repository should be per Aggregate root and not table.](https://stackoverflow.com/questions/1495553/how-to-use-the-repository-pattern-correctly#:~:text=Repository%20should%20be%20per%20Aggregate%20root%20and%20not%20table.) 

        2.  if entity shouldn't live alone. if it's just an entity, it doesn't need a repository, it should be updated/created/retrieved through repository of aggregate root it belongs.  

    12. Is Repository Pattern as same as Active Record Pattern? 

        [Active Record Pattern](https://stackoverflow.com/questions/3486916/is-repository-pattern-as-same-as-active-record-pattern#:~:text=Active%20Record%20Pattern%20defines,via%20instance%20methods.) defines An object that wraps a row in a database table or view, encapsulates the data access, and adds domain logic on that data. 

        In the Repository pattern all of the data access is put in a separate class and is accessed via instance methods. 

    13. What is relationship between Repository and Unit of Work? 

        1.  One Unit of work contains many repository and complete after the business transaction. 

    14. Is the repository pattern useful with Entity Framework Core? 

        1.  No, the repository/unit-of-work pattern (shortened to Rep/UoW) isn't useful with EF Core. EF Core already implements a Rep/UoW pattern, so layering another Rep/UoW pattern on top of EF Core isn't helpful. 

2.  What is SDLC? [1](https://www.guru99.com/sdlc-interview-questions.html)   ,   [2](https://www.educba.com/sdlc-interview-questions/)  ,  [3](https://www.tutorialsmate.com/2020/05/sdlc-interview-questions.html)  

    1.  What is SDLC and what is it used for? 

    2.  What are the different types of SDLC methodologies? 

    3.  What are the different phases of the Waterfall model? 

    4.  What is CMM Maturity Level and what is its importance? 

    5.  What are the drawbacks of Waterfall model? 

    6.  Who are the different team members involved in the different phases of the Waterfall model? 

    7.  What are LLDs or HLDs in SDLC? 

    8.  What are the different phases in the Agile model? 

    9.  What are the advantages of the agile model? 

    10. What is a V-shaped model in SDLC? 

3.  What is Azure Dev Ops? 

4.  What is ci cd and  repo,build,release in dev ops? 

5.  What is repository ? 

6.  What is a Build , debugger ? 

7.  Ef 

    1.  What is ADO.Net EF? 

    2.  How does the entity framework is differ from ADO.Net? 

    3.  List and explain the components of the entity framework. 

    4.  Functions of entity framework. 

    5.  List out the primary parts of the entity data model. 

    6.  What is migration in the entity framework? 

    7.  What are the types of inheritance in the entity framework? 

    8.  How to load related entities? 

    9.  What is the difference between entity framework and LINQ? 

    10. List out approaches used in the Entity framework. 

8.  Rest APi 

    1.  What is REST? 

          REST, or REpresentational State Transfer, is an architectural style for providing standards between computer systems on the web, making it easier for systems to communicate with each other. 

    2.  What is a REST API? 

        An API, or application programming interface, is a set of rules that define how applications or devices can connect to and communicate with each other. A REST API is an API that conforms to the design principles of the REST, or representational state transfer architectural style. 

    3.  What are the principles of REST? 

        -   Stateless 

        -   client server,  

        -   uniform interface  

          All API requests for the same resource should look the same, no matter where the request comes from. The REST API should ensure that the same piece of data, such as the name or email address of a user, belongs to only one uniform resource identifier (URI). 

        -   cacheble,  

        -   layered system,  

        -   code on deman 

    4.  What does it mean for an API to be stateless? 

    5.  Which protocol do REST APIs use? 

    6.  Which markup languages are primarily used to represent resources in REST APIs? 

    7.  Which HTTP request methods are supported by REST? 

    8.  What is the difference between the POST method and the PUT method? 

    9.  What is CRUD? 

    10. What is messaging in the context of REST? 

    11. What are the main parts of an HTTP request? 

    12. What are the main parts of an HTTP response? 

    13. What are some common HTTP response status codes you might see when working with a REST API? 

    14. What is a resource? 

    15. What is a URI? 

    16. What is caching? 

    17. What is payload? 

    18. What's a real-world example of a REST API? 

    19. What is the difference between REST and SOAP? 

    20. What is the difference between REST and AJAX? 

    21. What are some benefits of REST? 

    22. What are some drawbacks of REST? 

    23. How do you test APIs? 

    24. How do you keep REST APIs secure? 

    25. What are some main characteristics of REST? 

9.  Micro service 

    1.  [List down the advantages of Microservices Architecture.](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#advantagesofmicroservices) 

    2.  [What do you know about Microservices?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#whataremicroservices) 

    3.  [What are the features of Microservices?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#featuresofmicroservices) 

    4.  [What are the best practices to design Microservices?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#bestpractices) 

    5.  [How does Microservice Architecture work?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#workingofmicroservices) 

    6.  [What are the pros and cons of Microservice Architecture?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#prosandconsofmicroservices) 

    7.  [What is the difference between Monolithic, SOA and Microservices Architecture?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#monoliticvssoavsmicroservices) 

    8.  [What are the challenges you face while working Microservice Architectures?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#challengesformicroservices) 

    9.  [What are the key differences between SOA and Microservices Architecture?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#soavsmicroservices) 

    10. [What are the characteristics of Microservices?](https://www.edureka.co/blog/interview-questions/microservices-interview-questions/#characteristicsofmicroservices) 

10. MVC 

    1.  What is MVC Life Cycle? Explain in detail? 

    2.  Explain the difference between MVC and three-layered architecture? 

    3.  Name the different types of controller action methods? 

    4.  Explain the function of beforFilter(),beforeRender  and  afterFilter  in Controller? 

    5.  What are the filters? Name a few MVC filters? 

    6.  Explain the difference between ViewData and ViewBag? 

    7.  Name the three segments that are important in routing? 

    8.  What is MVC Scaffolding? 

    9.  What is a partial view in MVC? 

    10. What is the difference between TempData and ViewData? Will data be preserved in TempData in the next request as well? 

11. SQL Server 

    1.  What is SQL? Describe the importance of SQL in RDBMS? 

        -   Structured query language (SQL) is a programming language for storing and processing information in a relational database. 

        -   RDBMS stands for Relational DataBase Management System.  

        -   A database management system supports the development, administration and use of database platforms through sql 

    2.  What is the difference between SQL and PL/SQL? 

        -   SQL is a non-procedural language that executes a single query at a time whereas, PL/SQL is a procedural language and executes blocks of code at once which helps reduce traffic and increases processing speed. 

        -   Sql does not support variable, conditional  and iterative  constructs. 

    3.  What are the main components of SQL? 

        -   DATA DEFINITION LANGUAGE 

        -   DATA MANIPULATION LANGUAGE 

        -   DATA CONTROL LANGUAGE 

        -   TRANSACTIONAL CONTROL LANGUAGE 

        -   DATA QUERY LANGUAGE 

    4.  What is the difference between delete and truncate commands? 

        1.  Delete -- DML, can contains where 

        2.  TRUNCATE is a [DDL(Data Definition Language)](https://www.geeksforgeeks.org/difference-between-ddl-and-dml-in-dbms/) , delete all the rows , fast 

    5.  Write a SQL query to find the 3rd highest salary from the table without using the TOP/limit keyword? 

    6.  How will you perform pattern matching operations in SQL? 

        1.  Like with wildcards 

    7.  Write a query to get employee names ending with a vowel? 

        1.  LIKE '%[AEIOU]' 

    8.  How will you copy rows from one table to another table? 

    9.  What is the difference between the 'WHERE' clause and the 'HAVING' clause? 

    10. How will you get a first name, salary, and round the salary to thousands? 

    11. Display the first name and experience of the employees? 

    12. Write a query to get the first name and last name after converting the first letter of each name to upper case and the rest to lower case? 

    13. Display the length of the first name for employees where the last name contain the character 'b' after the 3rd position? 

    14. Change the salary of employee 115 to 8000 if the existing salary is less than 6000? 

    15. How will you Insert a new employee into employees with all the required details? 

    16. Display employees who joined in the month of May? 

    17. What is the meaning of TRIGGER  in SQL? 

        1.  DML Events 

        2.  DDL Events 

        3.  LOGON Event 

12. Oracle 

    1.  Find the error from the below SQL Query? 

    2.  What is Semijoin? How to implement it in SQL? 

    3.  What is PL/SQL? 

    4.  How to handle errors in PL/SQL? 

    5.  What are the constraints? How to add a named PRIMARY KEY constraint in SQL? 

    6.  What are savepoints? 

    7.  What is BLOB? 

    8.  Find the error in the below code snippet if any? 

    9.  Write a query to display a list of tables owned by the user. 

    10. What is dynamic SQL? When to use dynamic SQL? 

    11. What is a database trigger? How to create it? 

    12. Tell me about set operations in SQL? 

    13. What is the answer to the below query? Additionally, implement a correction so that the query below behaves as expected? 

    14. What is the purpose of COALESCE and NVL functions? 

    15. What is the use of HAVING clause? 

13. Databases 

-   what is index  

A database index is a data structure that improves the speed of data retrieval operations on a database table at the cost of additional writes and storage space to maintain the index data structure.  

 index is a copy of selected columns of data, from a table, that is designed to enable very efficient search. 

 An index normally includes a "key" or direct link to the original row of data from which it was copied, to allow the complete row to be retrieved efficiently.  

-   What do you understand by the terms Entity, Entity Type, and Entity Set in DBMS? 

-   What are relationships and mention different types of relationships in the DBMS 

-   What is concurrency control? 

-   What are the different levels of abstraction in the DBMS? 

-   What is normalization and what are the different types of normalization? 

-   What are the different types of keys in the database? 

-   What is the difference between two and three-tier architectures? 

-   Mention the differences between Unique Key and Primary Key 

-   Mention the differences between Trigger and Stored Procedures 

-   What are the differences between Hash join, Merge join and Nested loops? 

-   What are indexes? Mention the differences between the clustered and non-clustered index 

-   What do you understand by cursor? Mention the different types of cursor. 

-   Explain what is a deadlock and mention how it can be resolved? 

-   Mention the differences between UNION and UNION ALL 

-   What do you understand by CLAUSE in SQL? 

-   Mention the differences between HAVING and WHERE clause? 

-   What are joins in SQL and what are the different types of joins? 

-   What is a view 

1.  .Net core 

2.  C# 

3.  benefits of async 

4.  why to do it 

5.  did you implement it  

6.  what was the scenario 

7.  covariant and contravariant functional and actional delegates 

8.  builder , adapter , repository  problem statement and solution with pattern 

9.  What are queues. 

10. Database queues 

11. Active MQ
