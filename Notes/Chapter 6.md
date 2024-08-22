# Chapter 6: Objects and Data Structures

```text
If we make our variables private to prevent anoyone from depending on them, so why many programmers authomatically add getters and setters?
```

## Data Abstraction

- A datastructure should hide its implementation because it's not about adding a layer between the data and the user, but it is about abstractions!

## Data/Object Anti-Symmetry

- Objects hide their data behind abstractions
- Data structures expose their data and have no meaning functions
- Procedural code allows adding new functions without affecting the data structure
- OO code allows adding new classes without changing the current functions
- The things that are hard for OO are east for procedural and the opposite is right

## The Law of Demeter

- Each function should call methods of one of these

  - The current class
  - Created by the current function
  - Passed to the current function
  - Object held in an instance variable of the current class

- Functions should call friends not foreigners

### Train Wrecks

- Instead of chaining methods, just chain the variables, they should be public
- If the methods return data structures then, there is no violation for the law of demeter

### Hybrids

- Hybrids are half objects and half data structures
- Avoid hybrids

### Hiding Structures

- Don't ask an object about its internals, ask them to do something

## Data Transfer Objects

- It is a class with public variables and no functions

### Active Records

- Active records are data structures with some navigation methods like `find` and `save`
- They are typically models that translate database tables
- Adding bussiness logic inside them making it be hybrid between a datastructure and an object
- Try to write the business logic in a separate class
- Treat the `active records` as data structures
