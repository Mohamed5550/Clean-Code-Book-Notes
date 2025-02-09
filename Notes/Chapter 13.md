# Chapter 13: Concurrency

- Writing clean concurrent program is hard

## Why concurrency?

- When we need to decouple what happens from when it happens
- When we need to handle muptiple resources at the same time instead of running all of them sequentially on the same loop

## Myths and Misconceptions

- Concurrency improves the performance only when there is a lot of waiting time

- The design of an algorithm significantly change when making it concurrent

- Understaning concurrency is important even if you work with containers like Web or EJB

- Concurrency incures some overhead

- Correct concurrency is complex

- Concurrency bugs are not always repeatable

- Concurrency often requires fundemental change in design strategy

## Challenges

- Some of the compiling paths may run over each other and results in wrong results

## Concurrency Defense Principles

- Single responsibility principle: keep your concurrent related code separate from other code
- Limit the scope of data: limit the access of any data that may be shared
- Threads should be as independent as possible: make threads be treated as it's the only thread in its world

## Know Your Library

- Be familiar with your library classes, there may be concurrent versions

## Know Your Execution Models

- There are some concepts:
  - Bound resources
  - Mutual exclution
  - Starvation
  - Deadlock
  - Livelock
- Producer-Consumer
- Readers-Writers
- Dining Philosophers

## Beware Dependencies Between Shared Methods

- Avoid using more one methods on shared objects
- If necessasry, you can use locking:
  - Client-locking
  - Server-locking
  - Adapted server

## Keep Synchronized sections small

- Keep your synchronized sections as small as possible

## Writing Correct Shut-Down Code Is Hard

## Testing Threaded Code

## Treat Spurios Failure as Candidate Threading Issue

## Get Your Nonthreaded Code Working First

- Fix nonthreading bugs first, then go to threading bugs

## Make Your Threaded Code Pluggable

- Make your threaded code can be run on various configurations

## Make Your Threaded Code Tunable

## Run with More Threads than Processors

- The more your code swaps, the more you will encounter threading errors

## Run on Different Platforms

- Different operating systems have different multithreading policies

## Instrument Your Code to Try and Force Failures

- Multithreading errors happend rarly
- You can use `Object.sleep()` for example to try to force errors
- There are two ways
  - Hand-Coded
  - Automated: tools like `Aspect-Oriented Framework`, `CGLIB` or `ASM`
