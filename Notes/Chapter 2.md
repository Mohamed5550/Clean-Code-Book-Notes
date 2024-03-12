# Chapter 2: Meaningful names

```text
We name many things in software, so let's name them well
```

## Intention-Revealing Names

- Names of variables, methods, and classes make the code easy or hard to understand, even if the logic is simple.
- Good names don't need comments to explain them.
- In this example:

```java
int d; // elapsed time in days
```

- It's better to write it in this way:

```java
int elapsedTimeInDay
```

- You should specify what is `measured` and the `unit`
- Choosing names that reveal intent makes the code easy to understand:

```java
// code without intentional names
public List<int> getThem()
{
    List<int> list1 = new ArrayList<int[]>();
    for(int[] x: theList) {
        if(x[0] == 4) {
            list1.add(x);
        }
    }
    return list1;
}
```

- It is hard to understand what it does, so let's try to add meaningful names

```java
// code with intentional names
public List<int> getFlaggedCells()
{
    List<int> flaggedCells = new ArrayList<int[]>();
    for(int[] cell: gameBoard) {
        if(cell[STATUS_VALUE] == FLAGGED) {
            flaggedCells.add(cell);
        }
    }
    return flaggedCells;
}
```

- Now you understand what it does, right?
- We can do better. Let's encapsulate the status checking in an object called `Cell`

```java

.
.

List<Cell> flaggedCells = new ArrayList<Cell>();
.
.
if(cell.isFlagged()) 
.
.

```

- Now it is more easier to understand what it does

## Avoid Disinformation

- Don't give abbreviations that are usually known as something else like `hp`
- Don't use names that vary in small ways like these
  - `XYZControllerForEfficientHandlingOfStrings`
  - `XYZControllerForEfficientStorageOfStrings`
- Spelling is important, right?

## Make Meaningful Distinctions

- when you name two things with a deffernt prefix or suffix, the addition should mean a different thing
  - `customer` is indistinguishable from `theCustomer`
- Don't Ad unnecessty suffixed
  - `nameString` is not better than name. The different is for what? distinguishing it from floats? So it will break another rule of disinformation
  - `table` shouldn't appear in tables, `variable` shouldn't appear in variables and so...

## Use Pronounceable Names

- Programming is a social activity
- Write names that you can pronounce like `CreationTimestamp`, don't write `ctnymdhms`

## Use Searchable Names

- Short names are hard to search in a body of text
- *The length of the name should correspond to its scope*
- Names that are in many places, give them a search-friendly names
- It is easy to locate all variables names `WORK_DAYS_PER_WEEK` but it is hard to find `5`

## Avoid Encodings

- There are many things encoded in programming, don't add more
- Encoded things add more burden to decode them

### Hungarian Notions

- In old compilers it was hard to remember names types
- Now it is more easier so we don't use them

### Member prefixes

- You don't need to prefix member variables with `m_` anymore
- Old code:

```java
public class Part {
    private String m_desc; // the textual description
    void setName(String name) {
        s_desc = name;
    }
}
```

- New code:

```java
public class Part {
    private String description
    void setName(String description) {
        this.description = description;
    }
}
```

### Implementations and Interfaces

- If you had to prefix `interface` or its `implementation`, the author chooses to encode the implementation

## Avoid Mental Mapping

- Readers shouldn't translate your names into other meaningful names
- Difference between smart programmers and professional programmers is that professionals understand that `clarity` is king

## Class Names

- Class names should be nouns not verbs

## Method Names

- method names should start with verb
- Accessors and mutatos should be names for their value and prefixed with `set`, `get`, and `is`

## Don't be cute

- Don't use jokes or culture-affected phrases in naming
- Say what you mean, mean what you say

## Use One Word per Concept

- `get`, `retrieve`, and `fetch` shoudn't do the same thing in different classes
- When you use a word, don't use any synonym of it in another place

## Don't pun

- The opposite of the previous rule
- Don't use the same word for two different things

## Use solution Domain Names

- Use terms that all programmers know, don't use terms affected by the business

## Use Problem Domain Names

- When there is no programmer terms for what you are doing, you can use terms related to the domain you are working on

## Add Meaningful Context

- Variables can tell what it does when they belong to a context
- Keep the variables in a context, otherwise you may have to use prefixes

## Don't add Gratuitous Context
