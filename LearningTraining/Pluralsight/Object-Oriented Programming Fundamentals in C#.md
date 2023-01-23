# Core Principle of Object Oriented (OO) Programming  
## Encapsulation  
## Inheritance  
## Interfaces  
## Extension Methods  
  
Notes from “[Object-Oriented Programming Fundamentals in C#](https://app.pluralsight.com/library/courses/object-oriented-programming-fundamentals-csharp/table-of-contents)”   
by Deborah Kurata ( Pluralsight )  
  
__Four Pillars of OOP__  
  - Abstraction
  - Encapsulation
  - Inheritance
  - Polymorphism
  
__Constructor__  
A special method of a class or structure in object-oriented programming that initializes an object of that type.  
  
__Key Steps__  
  - Identifying Classes
  - Represents business entities
  - Defines properties (data)
  - Defines methods (actions/behavior)  
  
__Separating Responsibilities (Separation of Concerns)__
  - Minimizes coupling  
    - The degree to which classes are dependant on each other  
    - Low coupling makes better testability and maintainability  

__Maximizes cohesion__
  - The measure of how related everything in a class is to the purpose of the class
  - High cohesion makes the class easier to maintain and test  

__Simplifies Maintenance__
  - Improves Testability  

__Establishing Relationships__  
  - Define how objects work together to perform the operations of the application  
    - Defining relationships  
    - Types of relationships  
    - Collaboration (“uses a” relationship)  
    - Composition (“has a” relationship)
      - Aggregation is a special type of composition where by the component parts do not exist except as part of the composition  
    - Composition: References
    - Composition: Ids
    - Inheritance (“is a” relationship)

__Leveraging Reuse__
  - Involves extracting commonality
  - And building reusable classes/components
    - Build it once
    - Test it once
    - Update it once
    - Enhance it once

__NOTE:__ By convention, the class responsible for retrieving and saving the data for an entity is called a ‘Repository Class’

__Design Pattern:__ Repository Pattern




## Encapsulation
(top)


## Inheritance 
(top)


## Interfaces
__Understanding Interfaces__  
- Class Interface
- Interface Metaphors
- Defining an Interface
- Implementing and Interface
- Interface-based Polymorphism  
 __Benefits of Interfaces and Polymorphism__  
   - Strong typing
   - Defines commonality among unrelated classes
   - Aids in building generalized utility methods with class-unique functionality


## Extension Methods
(top)


## Final Words and Next Steps
__Indentifying Classes__  
When given a specification for a feature or a new application start by identifiying the classes from the requirements source specification.
- __Represents business entities__ - Object-oriented programing represents the entities and concepts of an application as a set of classes. 
- __Defines properties (data)__ - Each class has properties that define the data each object will manage. 
- __Defines methods (action/behavior)__ - Each class has methods, which are the actions and behaviors that each object can perform. Then analyze the classes you identified and separate responsibilites as needed.

__Separating responsibility__
- __Minimizes coupling__ - Minimize coupling by ensuring each class has a single purpose.
- __Maximies cohesion__ - Maximize cohesion by reviewing the properties and methods of each class to confirm each one belongs to that class.
- __Simplifies maintenance__ - Single-focus classes simplify maintenance and improve testablity
- __Improves testability__ - 

__Establishing relationships__
- Defines how objects work together to perform the operations of the application

__Leveraging reuse__
- Involves extracting commonality
- Building reusable classes / components
- Defining interfaces


## Four Pillars of OOP
Abstraction | Encapsulation | Inheritance | Polymorphism  

- Abstraction describes an entity in simple terms
- Encapsulation allows hiding the data in implementation in the class
- Inheritance allows derived or child classes to use the parent classes  
  - Inheritance polymorphism 
- Polymorphism 
  - Interface-based polymorphism
  
  
## OOP Is the Foundation

OOP opens doors to these related topics:
- Clean Code
- Defnsive Coding
- Iterative Agile
- API
- Design Patterns
- Domain Driven Design
- .NET apps

## Additional Pluralsight Courses

- Defensive Coding in C#
- Clean Code: Writing Code for Humans
- C# Interfaces
- Design Patterns On-Ramp
- C# Best Practices: Improving on the Basics
- C# Best Practices: Collections and Generics


## Questions

Q. What is encapsulation?  
A. A way to hide the data and implementatino details within a class.

Q. What is a constructor?  
A. A special method named with the class name.  

Q. What is a class?  
A. A set of code that defines a type that represents an entity.  

Q. What is an auto-implemented property?  
A. A short-cut for creating a C# property with a hidden backing field.  

Q. How cohesive should your classes be and why?  
A. Maximize cohesion so class members relate to the class purpose.  

Q. What is a static class?  
A. A class that cannot be instantiated.  

Q. How coupled should your classes be and why?  
A. Minimize coupling to reduce dependencies between classes.  

Q. What is an explicit interface?  
A. A type defined with the interface keyword.  

Q. Which of the following defines a collaboration relationship?  
A. Customer Repository class "uses a" instance of the Customer class.  

Q. What is a sealed class?  
A. A class that cannot be extended with inheritance.  

Q. What is the difference between a static method and an extension method?  
A. An extension method has the "this" keyword as part of the first parameter.  

Q. What does the Protected access modifier on a member do?  
A. Allows the class and any class that inherits from it to access the member.  

Q. When is a constructor executed?  
A. When an object is created from a class using the new keyword.  

Q. Which of the following defines an inheritance relationship?  
A. Business Customer "is a" Customer.  

Q. How is an explicit interface implemented in a class?  
A. 1. Writing code for each of the interface members.  
   2. Adding the interface name to the class signature.  
   
Q. What is an implicit class interface?  
A. The set of plublic members defined in a class.  

Q. What is an object?  
A. An instance of a class.  

Q. Which syntax creates a new object from the Customer class?  
A. Customer currentCustomer = new Customer();  

Q. What is an extension method?  
A. A static method that appears as a method on an existing class.  

Q. What is the principle of Separation of Concerns?  
A. 1. Each part is responsible for a separate concern.  
   2. Defining parts with minimal overlap.  
   3. Decomposing an application into parts.  
   
Q. What is the difference between a virtual and abstract method?  
A. 1. An abstract method cannot have any code in it.  
   2. A virtual method has an implementation, but can be overriden.  
   3. An abstract method MUST be overridden in a derived class.  

Q. A collaboration relationship between Class A and Class B can be implemented by:  
A. Class A creating and using an instance of Class B.  

Q. What is a design pattern?  
A. Common practices for defining sets of classes and their relationships.  

Q. What is the difference between an abstract and concrete class?  
A. Abstract classes don't allow construction using the new keyword.  

Q. Which of the following defines a composition relationship?  
A. Customer class "has a" set of Address objects.  

Q. What is object-oriented programming?  
A. Focusing on objects that interact cleanly with one another.  

Q. What is a property?  
A. Data managed by a class.  

Q. A composition relationship between Class A and Class B can be implemented by:  
A. Class A defining a property that references Class B.  

Q. Implementing composition using an Id instead of a reference:  
A. 1. Makes it easier to save the entity.  
   2. Can make the entity retrieval more efficient.  
   3. Minimizes coupling.  
   
Q. What is the purpose of the Override keyword?  
A. Define a custom implementation of an inherited member.  







