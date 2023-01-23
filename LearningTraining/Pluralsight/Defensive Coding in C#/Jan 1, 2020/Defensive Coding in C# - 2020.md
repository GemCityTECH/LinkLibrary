Jan 1, 2020  

# Defensive Coding in C# by Deborah Kurata
Resources: [https://github.com/DeborahK/CSharp-Defense](https://github.com/DeborahK/CSharp-Defense)  

Learn techniques for strengthening your application’s defenses against the perils awaiting it in the real world. You will see how to write clean code, create unit tests, build clear methods, and prepare for the unexpected.

Great applications perform required operations as expected, help users enter correct data, handle system and application exceptions, and make it easy for future developers to modify and maintain the code. Defensive coding focuses on improving code comprehension through clean code, improving code quality with unit tests, and improving code predictability by building clear methods and preparing for the unexpected. In this course, Defensive Coding in C#, you will gain the ability to strengthen your application’s defenses against the perils awaiting it in the real world. First, you will learn how to improve your code comprehension by following techniques such as the Single Responsibility principle. Next, you will discover how to improve your code quality through unit tests. Finally, you will explore how to improve your code predictability by validating method arguments, handling nulls appropriately, returning predictable results, and managing exceptions. When you are finished with this course, you will have the skills and knowledge needed to strengthen your code’s defenses.

## Why Defensive Code Matters  
__What Are We Defending Our Code From?__  
- Incorrect Entry  
  - Add Validation  
- Inalid Operations  
  - Check arguments  
  - Unit test operations  
- System mishaps  
  - Add checks  
  - Manage exceptions  
- Future Developers  
  - Write clean code  
  - Rerun unit tests  
  
__What is Defensive Coding?__  


>__[Defensive programming (coding)](https://en.wikipedia.org/wiki/Defensive_programming)__ is an approach to improve software and source code, in terms of:
>
>General quality – reducing the number of software bugs and problems.
>Making the source code comprehensible – the source code should be readable and understandable so it is approved in a code >audit.
>Making the software behave in a predictable manner despite unexpected inputs or user actions. - Wikipedia  

__Defensive Coding Helps Us Improve:__
- Code comprehension 
- Code quality  
- Code predicability  

__Competing Goals:__
- INCREASE CODE: Improving code predictability by __writing more validation and exception management code__  
- REDUCE CODE: Improving code comprehension by __eliminating unnecessary code__  

__Fitness for a Purpose__  
__Risk vs. Defenses__  

---

__Course Overview__

__Strengthening our defenses__
- Code comprehension  
- Code quality  
- Code predictability  

__Validating method arguments__  

__Handling nulls__  

__Returning predictable results__  

__Managing exceptions__  

---  
## Strengthening Our Codes Defenses  

__Evaluating Weaknesses__
- Identify Potential Weaknesses  
  - Code was Copy/paste  
  - Presentation logic mixed with business logic  
  - Difficult to unit test  
  - No validation  
  - No exception handling  
  
__Code comprehension__  
- Easy to read  
- Have a clear intent  
- Simple  
- Thoughtful  

>__Refactoring__ is the process of restructuring code, altering it's organization without changing its behavior.

__Improving Code Comprehension__  
- Single responsibility principle  
- Separation of concerns  
- Don't repeat yourself (DRY)  

__Single Responsibility Principle__  
- Single focus  

__DEMONSTRATION:__  
Show simple example of exctracting code into single focus tasks.  
- Calculate profit margin  
- Check the profit margin  
- Save the new price information  

__Naming Convention for exctracted code__
- Since methods perform __actions__ the method name shoudl eb a __Verb__ with and option subject that __Verb__ is acting on.
  - Examples:
    - CalculateMargin
    - CheckMinimumMargin
    - SavePrice

__Separation of concerns__  
- Separating an application into distinct parts where each part addresses a specific concern or aspect of the application. This is often done with __domains__ or __layers__.  
  - __Presentation layer__ - for user interface and visual appearance  
  - __Business Logic or Services Layer__ - for the logical calcualtions and operations of the application  
  - __Data layer__ - for the collection of data and interface to the data stores  

__Don't Repeat Yourself__  


__Improving Code Quality__  
- Is the code pleasant to work with?  
- Does it work as expected?  
- Does it meet the requirements?  

__Checks for quality__  
- Code reviews  
- Code execution  
- Unit testing  

__Visual Studio Unit Testing Options__  
- MS Test  
- NUnit  
- XUnit  

__Unit Testing Steps__  
- Define test cases  
- Create a unit test for each case  
- Execute the tests  
- RE-execute tests  

__Defining Test Cases__  
- Valid inputs  
- Data entry rules  
- Edge cases  
- Invalid inputs  
- Possible exceptions  
- Empty and null  

>// __Arrange__ - Set up variables and define expected results  
>// __Act__ - Execute the method to test   
>// __Assert__ - We assert the results of the test match the expect results  

NOTE: You will find lots of repeated code in unit tests because unit tests prefer clarity of DRY. 

__Improving Code Predictibility__  
- Code predictibility: __[Principle of Least Surprise](https://en.wikipedia.org/wiki/Principle_of_least_astonishment)__  
>More generally, the principle means that a component of a system should behave in a way that most users will expect it to behave; the behavior should not astonish or surprise users. - Wikipedia

__What Should Happen If...?__  
- The user enters invalid data?  
- The user breaks a business rule?  
- An operation suceeds, or fails?  
- Something goes wrong?  

__Line of Defense:__
- User Interface  
- Our Methods  


__Guidelines and Summary__  
- Improve Code Comprehension  
- Improve Code Quality  
- Improve Predictibility  

---  

## Validating Method Arguments  

__Refactoring Our Method__  
- Helper method  
- Method overloading  
- Guard class  

__Helper Method__  
- Move all the guard clauses into a dedicated helper method  
- Each helper method validates one of the arguments, checking all of its business rules and throwing an exception if the argument is not valid  

__Method Overloading__  
- Separate the guard clauses from the actual method using method overloading  
- Method overloading are multiple methods using the same method name but a different set of method parameters     
__Guard Class__  
- The Guard class has it's own set of generalized validation methods. Unlike the helper methods which focus on defining business rules for a specific argument  
- The guard class contains a set of more generalized methods that can be reused for any validation in the application  

__Guidelines and Summary__  
- Define a clear method signature  
  - A good method name use a [verb] followed by an optional [subject] that the verb is acting on  
- Define good parameter names that describes the data type of that parameter
- Carefully consider parameter order  
  - Start with the primary values  
  - List remaining parameters in a logical and predictable order  
  - Then include and flags or configuration parameters  
  - Add optional parameters last  
- Surrounding the operations with conditionals  
- Fail fast with guard clauses  
  - Fail fast by throwing an exception  
  - Protected from invalid values  
  - Provide validation information  
  - They leave the operation unobsucured  
- Refactor  
  - Build a set of helper methods
  - OR Use method overloading  
  - OR build a guard class  


























