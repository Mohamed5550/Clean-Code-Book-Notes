# Chapter 10: Classes

- In the book we talked about how to write clean small parts of the system. Let's talk about a higher level

## Class Organization

- Public variables
- Public static variables
- Private variables
- Private static variables
- public functions, and each public function should be followed byt the private functions it calls

## Classes Should Be small

- Class name determines its size
- We should choose a name that describe what the class fulfills
- We shoul be able to write a brief description of the class in about 25 words without using the wordds "if", "and", "or", or "but"

## The Single Responsibility Principle

- Class should have one and only one reason to change
- It's one of the simpler principles of OO and one of the important ones

## Choesion

- Class should have a small number of instance variables
- Methods should manipulate as much as possible instance variables
- Maximum conhesion is when all methods manipulate all variables
- When classes loose cohesion, split them

## Organizing for Change

- **OCP principle:** classes should be open for extension, closed for modification
