May 8, 2014

# Table of Contents - Defensive Coding in C#  

## Introduction  
- Introduction  
- What is Defensive Coding?  
- Clean Code  
- Testable Code and Unit Tests  
- Predictable Code  
- Topics  
---  
## Defending Your Methods Part 1  
- Introduction  
- Clean, Testable, and Predictable Methods  
- Example: Clean, Testable, and Predictable Methods 
- Demo: Creating a Class Library Component  
- Demo: Clean, Testable, and Predictable Methods  
- Demo: Named Arguments  
- Key Points  
---  
## Defending Your Methods Part 2  
- Introduction  
- Validating Method Parameters  
- Demo: Validating Method Parameters  
- Key Points  
---  
## Automated Code Testing  
- Introduction  
- I Don't Have Time to Test!  
- Code First vs. Test First  
- Defining Unit Test Cases  
  - Valid Inputs  
  - Invalid Inputs  
  - Guard Clause  
  - Assumptions  
  - Bug Fixes  
- Creating Unit Tests  
  - One Test Case  
  - Structure (Arrange, Act, Assert)  
  - Self Documented  
- Using Test Explorer  
- Generating Unit Tests  
- Unit Tests and Exceptions  
- Dependencies  
- Summary  
  - Structured  
  - Self-documented  
  - Automatic  
  - Repeatable  
  - TARDIS  
---  
## Defending Your Methods Part 3: Returning Predictable Results  
- Introduction  
- Method Results  
- Demo: Returning a Value  
- Demo: Returning Exceptions  
- Demo: Returning Multiple Values  
- Returning Null  
- Summary  
---  
## Defending Your Code Constructs  
- Introduction  
- Local Variable Declarations  
- If Statements  
- Switch Statements  
- Enums  
- Summary  
---  
## Asserts, Errors, and Exceptions  
- Introduction  
- Demo: Preparing the Sample Code  
- Asserts  
  - Invariants  
- Anticipated Errors  
  - Invalid User Entry  
    -- Use an appropriate control  
    -- Use built in data validation  
    -- Write a validation method  
    --  == Display message to the user  
    -- Validate with guard clauses  
    --  == Display message to the user  
    -- Proceed wiht a good default value  
  - Invalid or Missing Data  
    -- Validate in coming data  
    -- Proceed without the value  
    -- Proceed with a good default value  
    -- Display a message to the user  
  - Code Construct Issues  
    -- Proceed wiht a default operation  
    -- Ignore the issue  
    -- Log it and display a message to the user  
  - System Issues  
    -- Try again  
    -- Proceed with an alternate operation  
    -- Ignore the issue  
    -- Log it and display a message to the user  
```
  - Use restrictive controls and binding  
  - Use validation methods  
  - Use good defaults  
  - Return Operation Result  
  - Throw exceptions  
  - Notify the user only when necessary  
```  
- Unexpected Exceptions and a Global Exception Handler  
  >_"To expect the unexpected shows a thoroughly modern intellect"_ - Oscar Wilde  
- Exception Handling  
  - Use controls  
  - Use code  
  - Use Debug.Assert to check Invariants  
  - Catch exceptions from guard clauses  
  - Catch exceptions from systems issues  
  - Define a global exception handler  
  - __Best Practices:__  
    - Don't use the global exception handler  
    - Handle Locally  
    - Do Something  
    - Catch Specific Exceptions  
    - Log  
    - Don't try to catch every exception (Pokemon method)  
    - Use 'Throw' to propogate  
    - Additional topics:  
       - Multiple catch blocks  
       - Finally clause  
       - Custom Exceptions  
- Summary  
---  
## Final Words  
- Introduction  
- Legacy Code  
  - Evaluate assumptions  
  - Write automated code tests  
  - Tests pass  
  - Refactor  
  - Test pass  
  - Make the change  
  - Test pass  
- For More Information  
  - Clean Code: Writing Code for Humans  
  - Code Contracts  
  - Reactoring Fundamentals  
  - Understanding and Eliminating Technical Debt  
  - Mastering Visual Studio 2012 (Automated Code Testing Module)  
- Summary  
  - Clean Code  
    - Improves Comprehension  
    - Simplifies Maintenance  
    - Reduces Bugs  
  - Testable Code + Unit Tests  
    - Improves Quality  
    - Confirms Maintenance  
    - Reduces Bugss  
  - Validation + Exception Handling  
    - Improves Predictability  
    - More Consistent  
    - Reduce Bugs 











