# Chapter 1: Clean Code

- There will be code in the book, alot of it, we will examine it by all the ways to see how to make it better

## There Will Be Code

- Some people say we are close to the end of coding era
- They say that code will not be written but generated from specifications
- But the author says ther will be always code because of these reasons:
  - Code represents details, those details that cannot be ignored or abstracted, they are the specifications to send to machine to run the program
  - The domain-specific languages will grow, and the level of abstraction of languages will increase, but the code will not be eliminated because we will still need to be accurate, detailed, rigorous and so formal
  - People who think code will disappear are like mathematicians who hope one day to discover a mathematics that doesn't have to be formal

## Bad Code

- The author showed a story of a company that had an app with a killer idea but the application stopped later because they couldn't manage bad code
- We all had written bad code, it may because we wanted to go fast or to do some other things, but we know it is bad

## The Total Cost of Owning a Mess

- Bad code leads to a mess, which leads to less productivity approaching zero

### The grand redisign in the sky

- Developers will ask managers to redesign the project, but the managers don't want to expend resources in the refactoring process, although, they see the bad productivity. But at last, they decide to refactor
- The author told a story of the redesigning which the chosen team redesign the project while the other maintain the old one. This process may take 10 year. At last, the current member of the new project are not the ones who started it. Now they want to redesign the new code again because it is a mess.
- He wants to say spending time in making the code clean is very important

### Attitude

- Why code gets bad? we have many explanations
  - The new requirements
  - The stupid managers
  - The untolerant clients
- But the author says it is **our fault**
- managers and marketers look to us when they want to make promises and commitments; and even if they don't, we shouldn't be shy about telling them what we think
- Someone may say, if I don't do what the manager says, I will be fired, but the author says propabbly this will not happen; because managers wants truth event if they don't act like it
- The managers may defent the schedules and the timeline with passion, it is their job. But it is your job to defent the code with equal passion

### The art of clean code

- Suppose we agreed to wrte a clean code. Now what is clean code?
- Knowing that the code is clean or not doesn't mean we can write a clean code
- The secret is the code-sense
- Some of us born with it, and some of us have to fight to ackquire it
- People without code-sense will know that the code is bad, but will not have any idea how to make it good
- People with code-sense will know that the code is bad and will see options about how to make it good

## What Is Clean Code?

- `Bjarne Stroustrup: C++`: straightforward, optimally optimized, does only one thing well, dependencies are minimal
  - Reading clean code makes you smile
  - One broken window starts the mess
  - Error handling is important, clean code interests in details

- `Grady Booch: OOA&D`: simple and direct. like a well-written prose
  - Focuses on readability

- `“Big” Dave Thomas: OTI and eclipse`: can be enhanced by another developer, unit tests, meaningful names, one way to do one thing, minimal dependencies, clear API
  - Clean code makes it easy for other people to enhance it
  - There is a difference between a code that is easy to read and a code that is easy to change
  - clean code has tests
  - Small code is better than large code

- `Michael Feathers: working with legacy code`: written by someone who cares
  - Micheal hit it on the head
  - The entire book is about caring for code

- `Ron Jeffries: Extreme Programming`: runs all tests, no duplication, expresses design ideas, minimal entities
  - Duplication means there is an issue
  - Expressiveness is meaningful names

- `Ward Cunningham: Wiki, Fit`: looks like the language was made for the problem
  - when you read clean code, you will not be surprised at all
  - You won't expend much effort
  - It is obvious, simple and compelling
  - Each module tell you how the next will be written
  - The programmer make it appear simple, not the language

## Schools of Thought

- Martial artists don't all agree about the best martial art or best techniques
- Students learn from one school and when they grow, they may learn from other masters, or found their own schools
- None of these schools is absolutely right
- There is a right way to practice a technique, but there is no best technique

## We Are Authors

- The next time you read a code remember that you have readers to care about
- Coding is 10:` reading to writing
- Because the ratio is so heigt, we need reading to be easy
- make the code easy to read to be easy to write

## The Boy Scout Rule

- It is not enought to write a clean code, you have to keep it clean over time
- `Leaave the campground cleaner than you found it`
- Suggestions about cleaning code
  - Improve a name of a variable
  - Devidie a large function
  - Eliminate one duplication
  - Clean up one composite `if` statement
