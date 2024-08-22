# Chapter 3: Functions

```
In the early days of computers there was routines and subroutines
```

What makes a function better than another?

## Small

- The first rule: functions should be very small
- The second rule: functions should be smaller than that
- Functions should be 2, 3, or 4 lines long
- Blocks like `if` and `while` should be one line, probabbly calling a function

## Do one thing

- Functions should do one thing, they should do it well, they should do it only
- What one thing is? it may be more than one thing but in the same level of abstraction
- Function should be described as a `TO` function
- `To do something, we first do thing1, then thing2, then thing3`

## One level of abstraction per function

- Mixing levels of abstraction at one function is always confusing
- The readers cannot determine easliy whethere this is a main concept or a detail
- Reading code from top to bottom
  - We need to read the program as a set of TO statements
  - It is difficult to learn this skill but it is so important

## Switch statements

- It is hard to make a switch statement

```java
public Money calculatePay(Employee e)
throws InvalidEmployeeType {
    switch (e.type) {
        case COMMISSIONED:
            return calculateCommissionedPay(e);
        case HOURLY:
            return calculateHourlyPay(e);
        case SALARIED:
            return calculateSalariedPay(e);
        default:
            throw new InvalidEmployeeType(e.type);
    }
}
```

- The last switch statement has many problems:
  - If we add a new feature we will change it (violates the Open Closed principle)
  - It does more than one thing
  - There is more than one reason to change it (vioaltes the Single Responsibility principle)
- The solution is to use polymorphism
- Rules for switch statements:
  - There should be only one
  - It creates instances of the inherited classes
  - No one should see it

## Use Descriptive names

- Don't be afraid to use a long name
- Don't be afraid to spend time thinking of a good name
- A clean code should be what you expect functions to be, like a story

## Function Arguments

- Best number of arguments:
  - Zero: ideal
  - One: monadic
  - Two: dyadic
  - Three: triadic (should be avoided as possible)
  - More: polyadic (shouldn't be used anyway)

- Common monadic forms:
  - there are two reasons to pass one parameter
    - to ask some question about the value
    - to transform the value and return it again
  - There is a less common reason (an event to change the system state)

- Flag arguments:
  - Flag arguments are ugly
  - Don't use them
  - Instead, separate the functions into two

- Dyadic functions:
  - functions with two arguments are harder to understand than functions with one argument
  - It may be required to use two arguments but try to avoid this
  - It is confusing to know the right order of the arguments

- Triads
  - They are very hard to deal with
  - Try to avoid it when it is possible

- Argument objects:
  - When some arguments can be enapsulated in one object, do it and pass it only as a one argument

- Argument Lists:
  - When there is a variable number of arguments, you can pass them as monads, dyads or triads, but not more

- Verbs and keywords:

## Have no side effects

- Side effects are lies
- Side effects are things you do, but you didn't tell about
- There will be problems when the user runs the function in another context

- Output arguments
  - Avoid output arguments
  - If the function needs to change the state of anything, make it to change the state of its owning object

## Command query separation

- Functions should do something, or answer a question, but not both

## Prefer exceptions to returning error codes

- Don't return error codes, but reutrn exceptions with `try...catch`

- Extract Try/Catch blocks
  - Separate the error handling logic from processing logic

- Error handling is one thing
  - functions should do one thing
  - The try/catch is one thing
  - So, the try/catch block should be the first and last thing in the function

- Error codes dependency magnet
  - When you change the `Enum` that contains the error codes, you will change all the functions depends on it

## Don't repeat yourself

- Duplication is the evil of any software
- There are many techniques developed to eliminate or control duplication
- Strategies for eliminating duplication
  - Structured programming
  - Aspect oriented programming
  - Component oriented programming

## Structured programming

- Dikjstra's rules of structured programming
  - Every block of code should have only one entry and one exit
  - one return statement in a function
  - no break or continue statements in a loop
  - and never goto statements

## How do you write functions like this?

- Writing code is like any kind of writing
- You write clumsy code first then you organize it
- He writes unit tests before organizing to keep the program working well after organizing

## Conclusion

- Mater programmers think of software as a story to tell rather than a code to write
