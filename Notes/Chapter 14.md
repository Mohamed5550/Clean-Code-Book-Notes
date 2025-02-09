# Chapter 14: Successive Refinement

`Case Study of a Command Line Argument Parser`

- *After reading the code*

## How Did he Do This?

- It was not written from the begining to the end in its current form
- If we have learned anything over the last couple of decades,
it is that programming is a craft more than it is a science
- To write clean code, you must first write dirty code and then clean it
- At first when the writer wrote it for one argument ttype it was clean
- But After adding more arguments it started to get dirty

## So He Stopped

- The author started to make tiny changes at some positions
- Making huge change at one time, may ruine the program
- Before changing anything, he wrote tests
- Then, the `ArgumentMarshaller` was born
- The exception class was then separated from the Args class
