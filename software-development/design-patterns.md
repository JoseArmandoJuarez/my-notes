## History of design patterns
* 1997 Christopher Alexander introduced the idea of patterns: Successful solutions to problems.
* 1987 Ward Cunningham and Kent Beck leverage Alexanders idea in the context of an object oriented language.
* 1987 Eric Gammas dissertation on importance of patterns and how to capture them.

---

## Patterns Catalogue
* Fundamental patterns (Basic)
    * Delegation Pattern
    * Interface Pattern
    * Proxy Pattern
* Creation Patterns (support object creation)
    * Abstract factory pattern
    * Factory method pattern
    * Lazy initialization Pattern
    * Singleton Pattern
* Structural Patterns (help compose objects, put objects together)
    * Adapter Pattern
    * Bridge Pattern
    * Decorator Pattern
* Behavioral Patterns(focused an realizing interactions among different objects)
    * Chain of responsibility pattern
    * Iteration Pattern
    * Observe Pattern
    * State Pattern
    * Strategy Pattern
    * Visitor Pattern
* Concurrency Patterns
    * Active Object
    * Monitor Object
    * Thread pool Pattern

---

## Pattern format (Subset)
* Name
* Intent
* Motivation
* Applicability
* Structure
* Consequences
* Implementation
* Sample Code
* Related Patterns

## Factory Method Pattern
* (is a creational design pattern)
* Intent
    * Allows for creating objects without specifying their class, by invoking a factory method (example: a method whose main goal is to create class instances)
* Applicability 
    * Class cannot anticipate the type of object it must create (the type of an object that is not known at compile time, is known until the code runs, a typical example - Frameworks)
    * Frameworks
        * Active X
        * .NET for windows development
        * Cocoa for Mac OS X
        * Cocoa for touch for IOS
        * Android Application Framework
    * Class wants it's subclasses to specify the type of objects it creates
    * Class need control over the creation of it's objects (when there is a limit of # of objects that it can create)
* Structure
    * Creator - provides interface for factory method
    * Concrete creator - Provides method for creating actual object
    * Product - object created by the factory method


(What are classes?
It defines a set of properties and methods that are common to all objects of one type)


## Strategy Pattern
* Provides a way to configure a class with one of many behaviors.
* What does that mean?
    * This pattern allows for defining a family of algorithms, encapsulating them into separate classes, so each algorithm in one class and making these classes interchangeable but providing a common interface for all the encapsulated algorithms

* Intent
    * Allows for switching between different algorithms for accomplishing a task.
    * Example: Having different sorting algorithms with different space or time tradeoffs. Might want to be able to have them all available and use different ones in different situations.

* Applicability
    * Different variants of an algorithm
    * Many related classes differ only in their behavior.

* Structure/Participants
    * Context: interface to outside world
    * Algorithm(strategy): common interface for the different algorithms
    * Concrete strategy: Actual implementation of the algorithm

---

## Other common patterns
    
* Visitor: 
    * a way of separating an algorithm from an object structure on which it operates.
* Decorator: 
    * A wrapper that adds functionality to a class :  stackable.
* Iterator: 
    * Access elements of a collection without knowing underlying representation.

## Choosing a Pattern
* Understand your design context
* Examine the patterns catalogue
* Identify and study related patterns
* Apply suitable pattern

## Pitfalls
* Selecting wrong patterns
* Abussing patterns
