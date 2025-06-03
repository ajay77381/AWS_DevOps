Reference url - https://www.geeksforgeeks.org/software-design-patterns/#types-of-software-design-patterns

# Software Design Patterns

## What are Design Patterns?
Design patterns are reusable solutions to common problems in software design. They represent best practices used by experienced object-oriented software developers. Design patterns provide a standard terminology and are specific to particular scenarios.

## Key Characteristics of Design Patterns
- **Reusability:** Patterns can be applied to different projects and problems, saving time and effort in solving similar issues.
- **Standardization:** They provide a shared language and understanding among developers, facilitating communication and collaboration.
- **Efficiency**: By using established patterns, developers can avoid reinventing the wheel, leading to faster and more reliable development.
- **Flexibility**: Patterns are abstract solutions that can be adapted to fit various contexts and requirements.

## Why Learn Design Patterns?

There are several reasons to learn design patterns:

1- **Improve Code Quality**: Design patterns help in creating code that is easier to understand, maintain, and extend. They promote best practices and provide solutions that have been tested and proven effective.

2- **Enhance Problem-Solving Skills**: Learning design patterns equips developers with a book of standard solutions to common problems. This enables them to quickly and effectively address similar challenges in various projects.

3- **Promote Reusability and Efficiency**: By applying design patterns, developers can create reusable components that can be used across multiple projects. This reduces redundancy and saves development time.

4- **Learn from Experts**: Explanation: Design patterns are derived from the collective experience of skilled developers and architects. Learning these patterns allows developers to benefit from the wisdom and insights of industry experts

## Types of Software Design Patterns

There are three types of Design Patterns:

- Creational Design Pattern
- Structural Design Pattern
- Behavioral Design Pattern

### Creational Design Patterns

Creational Design Pattern abstract the instantiation process. They help in making a system independent of how its objects are created, composed and represented.

Types of Creational Design Patterns:



![Image](https://github.com/user-attachments/assets/daa6cc10-08ba-44d6-b5c6-b0423234a3bc)

. [Factory Method Design Pattern](https://www.geeksforgeeks.org/factory-method-for-designing-pattern)
The Factory Method pattern is used to create objects without specifying the exact class of object that will be created. This pattern is useful when you need to decouple the creation of an object from its implementation.

2. [Abstract Factory Method Design Pattern](https://www.geeksforgeeks.org/abstract-factory-pattern)
Abstract Factory pattern is almost similar to Factory Pattern and is considered as another layer of abstraction over factory pattern. Abstract Factory patterns work around a super-factory which creates other factories.

3. [Singleton Method Design Pattern](https://www.geeksforgeeks.org/singleton-design-pattern)
The Singleton method or Singleton Design pattern is one of the simplest design patterns. It ensures a class only has one instance, and provides a global point of access to it.

4. [Prototype Method Design Pattern](https://www.geeksforgeeks.org/prototype-design-pattern)
Prototype allows us to hide the complexity of making new instances from the client. The concept is to copy an existing object rather than creating a new instance from scratch, something that may include costly operations. The existing object acts as a prototype and contains the state of the object.

5. [Builder Method Design Pattern](https://www.geeksforgeeks.org/builder-design-pattern)
Builder pattern aims to “Separate the construction of a complex object from its representation so that the same construction process can create different representations.” It is used to construct a complex object step by step and the final step will return the object.

[Structural Design Patterns](https://www.geeksforgeeks.org/structural-design-patterns)
Structural Design Patterns are concerned with how classes and objects are composed to form larger structures. Structural class patterns use inheritance to compose interfaces or implementations.


Types of Structural Design Patterns:



![Image](https://github.com/user-attachments/assets/22c709ae-9a71-45b2-a50e-d175b496af7f)


. [Adapter Method Design Pattern](https://www.geeksforgeeks.org/adapter-pattern)
The adapter pattern convert the interface of a class into another interface clients expect. Adapter lets classes work together that couldn’t otherwise because of incompatible interfaces.

2. [Bridge Method Design Pattern](https://www.geeksforgeeks.org/bridge-design-pattern)
The bridge pattern allows the Abstraction and the Implementation to be developed independently and the client code can access only the Abstraction part without being concerned about the Implementation part.

3. [Composite Method Design Pattern](https://www.geeksforgeeks.org/composite-design-pattern)
Composite pattern is a partitioning design pattern and describes a group of objects that is treated the same way as a single instance of the same type of object. The intent of a composite is to “compose” objects into tree structures to represent part-whole hierarchies.

4. [Decorator Method Design Pattern](https://www.geeksforgeeks.org/decorator-pattern)
It allows us to dynamically add functionality and behavior to an object without affecting the behavior of other existing objects within the same class. We use inheritance to extend the behavior of the class. This takes place at compile-time, and all the instances of that class get the extended behavior.

5. [Facade Method Design Pattern](https://www.geeksforgeeks.org/facade-design-pattern-introduction)
Facade Method Design Pattern provides a unified interface to a set of interfaces in a subsystem. Facade defines a high-level interface that makes the subsystem easier to use.

6. [Flyweight Method Design Pattern](https://www.geeksforgeeks.org/flyweight-design-pattern)
This pattern provides ways to decrease object count thus improving application required objects structure. Flyweight pattern is used when we need to create a large number of similar objects.

7. [Proxy Method Design Pattern](https://www.geeksforgeeks.org/proxy-design-pattern)
Proxy means ‘in place of’, representing’ or ‘in place of’ or ‘on behalf of’ are literal meanings of proxy and that directly explains Proxy Design Pattern. Proxies are also called surrogates, handles, and wrappers. They are closely related in structure, but not purpose, to Adapters and Decorators.

[Behavioral Design Patterns](https://www.geeksforgeeks.org/behavioral-design-patterns)
Behavioral Patterns are concerned with algorithms and the assignment of responsibilities between objects. Behavioral patterns describe not just patterns of objects or classes but also the patterns of communication between them. These patterns characterize complex control flow that’s difficult to follow at run-time.

[Behavioral Design Patterns](https://www.geeksforgeeks.org/behavioral-design-patterns)

Behavioral Patterns are concerned with algorithms and the assignment of responsibilities between objects. Behavioral patterns describe not just patterns of objects or classes but also the patterns of communication between them. These patterns characterize complex control flow that’s difficult to follow at run-time.

Types of Behavioral Design Patterns:



![Image](https://github.com/user-attachments/assets/3177e94a-fdfe-4c20-b5d4-f1b9eaf7e8ed)

1. [Chain Of Responsibility Method Design Pattern](https://www.geeksforgeeks.org/chain-responsibility-design-pattern)
Chain of responsibility pattern is used to achieve loose coupling in software design where a request from the client is passed to a chain of objects to process them. Later, the object in the chain will decide themselves who will be processing the request and whether the request is required to be sent to the next object in the chain or not.

2. [Command Method Design Pattern](https://www.geeksforgeeks.org/command-pattern)
The Command Pattern is a behavioral design pattern that turns a request into a stand-alone object, containing all the information about the request. This object can be passed around, stored, and executed at a later time

3. [Interpreter Method Design Pattern](https://www.geeksforgeeks.org/interpreter-design-pattern)
Interpreter pattern is used to defines a grammatical representation for a language and provides an interpreter to deal with this grammar.

4. [Mediator Method Design Pattern](https://www.geeksforgeeks.org/mediator-design-pattern)
It enables decoupling of objects by introducing a layer in between so that the interaction between objects happen via the layer.

5. [Memento Method Design Patterns](https://www.geeksforgeeks.org/memento-design-pattern)
It is used to restore state of an object to a previous state. As your application is progressing, you may want to save checkpoints in your application and restore back to those checkpoints later. Intent of Memento Design pattern is without violating encapsulation, capture and externalize an object’s internal state so that the object can be restored to this state later.

6. [Observer Method Design Pattern](https://www.geeksforgeeks.org/observer-pattern-set-1-introduction)
It defines a one-to-many dependency between objects, so that when one object (the subject) changes its state, all its dependents (observers) are notified and updated automatically.

7. [State Method Design Pattern](https://www.geeksforgeeks.org/state-design-pattern)
A state design pattern is used when an Object changes its behavior based on its internal state. If we have to change the behavior of an object based on its state, we can have a state variable in the Object and use the if-else condition block to perform different actions based on the state.

8. [Strategy Method Design Pattern](https://www.geeksforgeeks.org/strategy-pattern-set-1)
The Strategy Design Pattern allows the behavior of an object to be selected at runtime. It is one of the Gang of Four (GoF) design patterns, which are widely used in object-oriented programming. The Strategy pattern is based on the idea of encapsulating a family of algorithms into separate classes that implement a common interface.

9. [Template Method Design Pattern](https://www.geeksforgeeks.org/template-method-design-pattern)
Template method design pattern is to define an algorithm as a skeleton of operations and leave the details to be implemented by the child classes. The overall structure and sequence of the algorithm are preserved by the parent class.

10. [Visitor Method Design Pattern](https://www.geeksforgeeks.org/visitor-design-pattern)
It is used when we have to perform an operation on a group of similar kind of Objects. With the help of visitor pattern, we can move the operational logic from the objects to another class.


## Design Patterns in Different Languages
Please follow the url for know about design pattern- https://www.geeksforgeeks.org/software-design-patterns/#types-of-software-design-patterns



## Frequently Asked Questions About Software Design Patterns
Q 1. What are software design patterns?
Software design patterns are reusable solutions to common problems that arise during software development. They are templates for solving recurring design issues and provide a way to create flexible, scalable, and maintainable software systems.

Q 2. Why are design patterns important in software development?
Design patterns promote best practices, enhance code readability, and facilitate code reuse. They help in creating software that is modular, extensible, and easier to maintain, reducing development time and efforts.

Q 3. How do design patterns differ from algorithms?
Design patterns focus on solving recurring design problems at the architectural or structural level, emphasizing the organization of code. Algorithms, on the other hand, are step-by-step procedures for solving specific problems at the computational level.

Q 4. How do design patterns enhance code flexibility?
Design patterns promote loose coupling between components, making it easier to replace or extend parts of the system without affecting others. This flexibility is crucial for adapting to changing requirements.

Q 5. When should I use design patterns?
Design patterns should be used when you encounter recurring problems in software design. They are particularly beneficial in complex systems where a systematic and proven approach to design is required.

Q 6. Are design patterns language-specific?
No, design patterns are not tied to a specific programming language. They are conceptual solutions that can be implemented in various languages. However, the syntax and implementation details may vary.

Q 7. What’s the difference between a design pattern and an anti-pattern?
Design patterns are proven solutions to common problems, promoting best practices. In contrast, anti-patterns are common pitfalls or bad practices that can lead to poor software design and should be avoided.

Q 8. Can I create my own design patterns?
Yes, you can create custom design patterns based on your project’s specific needs. However, it’s crucial to ensure that the pattern addresses a recurring problem and follows the principles of good design.

Q 9. How do design patterns relate to code smell?
Design patterns help eliminate code smells (indications of poor design) by providing proven solutions to common problems. Recognizing and addressing code smells is essential for creating maintainable and efficient software.

Q 10. Can design patterns be used in microservices architecture?
Yes, design patterns can be applied in microservices architecture to address common challenges such as service discovery, communication between services, and fault tolerance. Patterns like the Service Registry and Circuit Breaker are relevant.

Q 11. How do design patterns impact system performance?
Properly applied design patterns can enhance system performance by promoting efficient code organization and reducing redundancy. However, poorly chosen or overused patterns may introduce unnecessary complexity, potentially impacting performance.

Q 12. Do freshers need to learn design patterns?
While not mandatory, learning design patterns can significantly benefit fresehrs by providing them with proven solutions to common problems. It can expedite the learning process and contribute to writing more maintainable code.

Q 13. Are there design patterns for web development?
Yes, many design patterns are applicable in web development. Patterns like MVC, Observer, and Singleton are commonly used to organize and structure code in both frontend and backend development.

Q 14. How do design patterns differ from architectural patterns?
Design patterns address specific design issues at a lower level, focusing on object creation, composition, and interaction. Architectural patterns, on the other hand, deal with higher-level structures of an entire application or system.
