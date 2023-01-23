May 8, 2014  

# [Defensive Coding in C#](https://app.pluralsight.com/player?course=defensive-coding-csharp&author=deborah-kurata&name=defensive-coding-csharp-m1-overview&clip=0&mode=live)
by Deborah Kurata

INTRODUCTION
Want to write great maintainable code, even when faced with constantly changing requirements, Legacy issues, intensive time pressures, and a repidly evolving environment, and want to keep that code great after maintenance activities, multiple developers, and the ravages of time? Welcome to Defensive Coding in C#.

This course will teach you how to write great, maintainable code, and keep that code great using defensive coding techniques.

WHAT IS DEFENSIVE CODING?  
>  ... an approach to improve software and source code, in terms of:  
> - General **quality** - Reducing the number of software bugs and problems.  
> - Making the source code **comprehensible** - the source code should be readable and understandable so it is approved in a code audit.  
> - Making the software behave in a **predictable** manner despite unexpected inputs or user actions.  
\- Wikipedia as of 4/14/2014  

The process of restructuring your code without changing its behavior is called **Refactoring**; the cleaner your code, the easier it is to understand, maintain, and test. 

DEFENSIVE CODING  
---  

  __CLEAN CODE__  
    - Improves Compreshension  
    - Simplifies Maintenance  
    - Reduces Bugs  
  
   __TESTABLE CODE + UNIT TESTS__  
     - Improves Quality  
     - Confirms Maintenance  
     - Reduces Bugs  
  
   __VALIDATION + EXCEPTION HANDLING__  
     - Improves Predictablity  
     - More Consistent  
     - Reduces Bugs  
  
## 1. Clean Code

**Good code vs Bad code**  
  - Bad code has a 'code smell'
  - Write Good code following clean coding techniques
  - Transform Bad code to Good code through refactoring
  
**Clean Code** has the following characteristics:
  - Easy to read
  - Clear intent
  - Simple
  - Minimal
  - Thoughtfull
  
## Refactoring
The act of restructuring code to make it clearer, cleaner, and testable, without changing its behavior is called Refactoring.

---  

## Defending Your Methods Part 1

Clean, Testable, Predictable Methods  
- Clear Purpose  
- Good Name  
- Focused Code  
- Short Length (recommended length: number of lines that fit on a screen) 
- Automated Code Test   
- Predictable Result  
  
---  


## Guard Clauses  
Examples:  

Check for value:  
``if (string.IsNullOrWhiteSpace(goalSteps)) throw new ArgumentException("Goal must be entered", "goalSteps);  ``
``if (string.IsNullOrWhiteSpace(actualSteps)) throw new ArgumentException("Actual steps must be entered", "actualSteps);  ``

Check if decimal:  
``if (!decimal.TryParse(goalSteps, out goalStepsCount)) throw new ArgumentException("Goal must be numeric", "goalSteps);  ``

``if (!decimal.TryParse(actualSteps, out actualStepsCount)) throw new ArgumentException("Actual must be numeric", "actualSteps);  ``

``if (goalStepCount <= 0) throw new ArgumentException("Goal must be greater than 0", "goalSteps);  ``
   
"Use Method Overloading any time you need one operation to take different sets of input."  

## Design by Contract  
- What does a method expect?  
- What does a method guarantee?  
- What does the method maintain?  










