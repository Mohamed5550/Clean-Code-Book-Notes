# Chapter 7: Error Handling

- *Error handling is important, but if it obsecures logic, it is wrong*

## Exceptions vs Return Codes

- Use exceptions and don't use return codes

## Write Your Try-Catch-Finally first

- Try/Catch defines scope in your program
- If any error happended, it stops and completes after tha catch
- They're like transactions
- Write your tests first with the exception then write your code (TDD)

## Use Unchecked Exceptions

- Checked exceptions violates Open/Closed principle
- Don't use checked exceptions

## Provide Context With Exceptions

- Create informative error message describes
  - The operation thay failed
  - The type of the failure

## Define Exceptions Classes in Terms of a User Needs

- Defining exception classes is a best practice

## Define The Normal Flow

- Use Special Case Pattern [Fowler]

## Don't Return Null

- Don't return null
- Use special case instead
- If an external API returns null, wrap it in a method that returns a Special Case Object or throws an exception

## Don't Pass Null

- Don't pass null to methods because it is difficult to cleanly handle it
