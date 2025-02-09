# Chapter 17: Smells and Heuristics

These are the heuristics of all the author opinions of refactoring bad code

## Comments

- Inappropriate information
- Obsolete comments
- Redundant comments
- Poorly written comments
- Commented-out code

## Environment

- Build requires more than one step
- Tests require more than one step

## Functions

- Too many arguments
- Output arguments
- Flag Arguments
- Dead functions

## General

- Multiple languages in one source file
- Obvious behaviour is unemplemented
- Incorrect behaviour at the boundaries
- Overridden safeties
- Duplication
- Code at wrong level of abstraction
- Base classes depening on their derivatives
- Too much information
- Dead code
- Vertical separation
- Inconsistency
- Clutter
- Artifical coupling
- Feature envy
- Selector Argument
- Obsecured Intent
- Misplaced responsibility
- User explanatory variables
- Function name should say what they do
- Understand the algorithm
- Make logical dependencies physical
- Prefer polymorphism to if/else or switch/case
- Follow standard conventions
- Replace magic numbers with names constants
- Be precise
- Structure over convention
- Encapsulate conditionals
- Avoid negative conditionals
- Functions should do one thing
- Hidden temporal couplings
- Don't be arbitrary
- Encapsulate boundary conditions
- Functions should descend only one level of abstraction
- Keep configurable data at high levels
- Avoid transitive navigation

## Java

- Avoid long import lists by using wildcards
- Don't inherit constants
- Constants versus enums

## Names

- Choose descriptive names
- Choose names at appropriate level of abstraction
- Use standard nomenclature where possible
- Unambiguous names
- Use long names for long scopes
- Avoid encodings
- Names should describe side-effects

## Tests

- Insufficient tests
- Use a coverage tool
- Don't skip trivial tests
- An ignored test is a question about ambiguity
- Test boundary conditions
- Exauhstively test near bugs
- Patterns of failure are revealing
- Test coverage patterns are revealing
- Tests should be fast
