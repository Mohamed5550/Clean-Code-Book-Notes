# Chapter 9: Unit tests

- In 1997 no one heard about Test Driven Development

## The Three Laws of TDDD

- **First Law:** You may not write a production code until you write a failing test
- **Second Law:** You may not write more of a unit test than it is sufficient to fail
- **Third Law:** You may nor write more production code than it is sufficient to pass the the test case

## Keeping Test Clean

- Having dirty tests is equivalnce that having no tests, or worse
- Tests grows as the application code grows

## Tests Enable the -ilities

- If you don't keep your tests clean, you will lose them
- Without tests, you lose the thing that keeps your code flexible

## Clean Tests

- What makes tests clean is readability

## A Dual Standard

- There are things you shouldn't do in production code but they're fine in test code

## One Assert per Test

- We should minimize the number of asserts in each test

## Single Concept per Test

- Test just one concept per test function

## F.I.R.S.T

- **FAST**: Tests should run fast, to run them frequently
- **INDPENDENT**: Tests shouldn't depend on each other, and can run in any order
- **REPEATABLE**: Tests should run any number of times and on any environment
- **Self-Validating**: Testes should return boolean value not a log file
- **Timely**: Writing tests should be fast, and should be written exactly before the code that pass them
