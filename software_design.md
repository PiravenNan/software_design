# Software Design Methodologies

## Introduction

There is no single correct way to approach a software engineering problem. Designing a product which satisfies a customer's needs while leveraging a team's skillset (and delivering on time and on budget) isn't something with a one-size-fits-all solution. There is, however, usually one option which is a better fit for a given situation than others. In this exercise we will find out about some of the different ways in which we could go about designing a system.

## Design Strategies

There are three principle design strategies used in software engineering:

- Structured design
- Function oriented design
- Object oriented design

None of these are compulsory when designing a product but following one will greatly aid the process. Each has its benefits and each has its drawbacks. Unlike many other aspects of software engineering they generally exist in isolation as the principles of each sit in direct opposition to each other in some scenarios.

There is no scenario where one of these strategies _can't_ be used, but we may be making our lives harder by choosing one over another. Likewise the majority of programming languages can be used with any strategy, but some are better fits for one strategy than another. For example Java is an excellent choice for an object oriented design while Scala would be a better choice for a functional design. Some languages such as Python can be used effectively with either, but have to sacrifice some features to achieve that flexibility.

Within each methodology there are various **design patterns** which provide further structure for us. In general though these are much more easily transferred across methodologies, although the precise implementation will vary by language. In practice the language used for a project will likely be the last thing to be chosen, determined by a combination of methodology and design pattern.


1.What do we mean by **coupling** and **cohesion** when discussing structured design?

- Coupling measures how much one part of the system relies on another. Low coupling means parts are independent, making the system easier to change and maintain.

- Cohesion measures how well elements in a module work together. High cohesion means elements have a clear purpose and are closely related, making modules easier to understand and manage. 
 - Coupling and cohesion play a role in achieving the Open/Closed Principle:
- Low Coupling: When modules are loosely coupled, adding new functionality (extension) to one module is less likely to impact other modules. Low coupling supports the Open/Closed Principle because you can extend the system without changing existing, independent modules.
- High Cohesion: Modules with high cohesion have related functions grouped together. When a module has high cohesion, it's easier to identify what needs to be extended without modifying existing, unrelated code. High cohesion supports the Open/Closed Principle by allowing you to add new functionality to a module without changing the entire module.

2. What is the difference between **top-down** and **bottom-up** design? Which best describes a function oriented design?
 - Top-down design: Start with the big picture and break it down into smaller parts.
 - Bottom-up design: Begin with small components and build them up into larger structures.
 - Function-oriented design organizes a system's functionality into distinct functions or procedures. These functions perform specific tasks and are structured into modules, promoting modularity, reusability, and sequential execution. It is commonly used in procedural programming languages like C, enhancing code readability and maintainability.

3. In which design methodology would a **class diagram** be most useful?
 - Class diagrams are most beneficial in Object-Oriented Design (OOD) because they serve as visual blueprints, capturing essential elements of object-oriented systems. They model classes, their attributes, methods, and relationships, illustrating fundamental concepts like inheritance and polymorphism. Class diagrams encapsulate dynamic behaviors, such as method interactions, and promote abstraction by focusing on essential details. They also facilitate the design of frameworks and libraries, providing a clear understanding of classes and aiding in the integration and extension of complex systems.

4. What are the **four pillars of object oriented programming**? Give a single-sentence description of each.
 - Encapsulation: Bundling data and methods into a class, controlling access to the data.
 - Inheritance: Allows classes to inherit properties and behaviors, promoting code reuse.
 - Polymorphism: Enables objects to be treated interchangeably, fostering flexibility in the code.
 - Abstraction: Simplifies complex systems, focusing on essential features and hiding irrelevant details.

6. What is the **strategy pattern**? How would its implementation differ between a functional and object oriented system?
 - The strategy pattern lets you switch between different algorithms without changing the code using them.

*In Functional Systems:*
 - Different algorithms are represented as functions.
 - Functions are chosen and applied based on the context.
 

*In Object-Oriented Systems:*

 - Algorithms are implemented as classes with a common interface.
 - The system selects and uses the appropriate algorithm class.
7. Imagine your company is creating a new online payment system. In order to gain maximum market share it can't be tied to a particular sector - it needs to work just as well when ordering a takeaway as when buying a new coat. Which design methodology would you suggest following? Give some justification for your decision.
 - For this, OOD may be the best design methology to use. This is because of it's use of classes and objects, which can all use the same interface or parent class to maintain the same basic functionality while also being able to create new objects which use these methods in different ways to use to fit different situations.