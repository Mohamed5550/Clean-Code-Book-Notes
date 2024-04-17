# Chapter 4: Comments

```
Don't comment bad code, rewrite it
```

- Comments are a necessary evil
- We use comments to compensate for our failure to express ourselves in code
- Everytime you want to write a comment, try to express yourself in code first
- If you can't, write it, but feel sad for your failure
- Comments often don't change with code
- Inacurate comments are far worse than no comments at all

## Comments Don't make up for bad code

- When you find a mess, don't comment it. Rewrite it
- Spend time in cleaning the mess

## Explain yourself in code

- What is better?

```java
// Check to see if the employee is eligible for full benefits
if ((employee.flags & HOURLY_FLAG) &&
    (employee.age > 65))
```

or

```java
if (employee.isEligibleForFullBenefits())
```

- The second one is better, explain yourself in the code, not comment

## Good comments

```
The only truly good comment is the comment you find a way not to write it
```

- Legal comments
  - These are the comments that contain license or author information
  - They are put at the begging of the file
  - They should refer to the details, not contain the details

- Informative comment
  - like a comment describing the return value
  - or a comment to tell the formate of a matched timestamp

- Explanation of intent
  - When you take a strange decission, you can write a comment to explain your intent

- Clarification
  - To clarify some obsequre arguments or strange library arguments
  - If you can change the code do it
  - If not, you can write a clarification comment
  - But it is risky, because if they are incorrect, there will be a big problem

- Warning of consequences
  - It is useful to write an explanation comment to warn the developers of something bad will happen if he proceeds

- TODO comments
  - These are comments to tell someone (or yourself) to modify something later becuase you can't at the moment
  - They are not an execuse to write bad code
  - You have to find them and clear them when you can

- Amplification
  - You can write a comment to amplify something that may seem not important

## Bad comments

- Mumbling
  - These are needed comments but are written bad
  - Any comment makes you open anothe module to check what is goind on is a bad comment

- Redundant comments
  - These are the comments that add nothing new to the reader

- Misleading comments
  - These are the comments that give wrong information

- Mandated comments
  - This happend when you add comments for every class or every function

- Journal comments
  - These are the comments that describe the history of the function
  - We needed them a long time ago
  - But now we have source control systems

- Noice comments
  - These are comments that add nothing new and we learn to ignore them

- Scary noice
  - These are doc comments that are pasted

- Don't use comments when you can use a function or a variable
  - You can rephrase the code to contain some meaningful variables instead of writine one line of code with a big comment

- Position markers
  - Use as many markers as possible

- Closing braces
  - Instead of writing comments in closing braces try to shorten your function instead

- Attributions and bylines
  - Don't use them
  - Source code control systems remembers who added what

- Commented out code
  - Don't do this
  - Source code control systems can remember it for you

- HTML comments
  - They make the comment hard to read in the place it should be easy

- Nonlocal information
  - Like giving default data that is changed in other place

- Too much information
  - Comments that contain too much information to read

- Inobvious connection
  - Don't write a comment that needs another comment to clear it out

- Function headers
  - Choose a good name for the function instead of writing a comment at the head of the function
