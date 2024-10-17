# Chapter 8: Boundaries

- We don't control the whole software, we may use third-party code
- We will talk about keeping the boundaries of our software clean

## Using Third-Party Code

- Avoid accepting or sending general data structures to public API's
- Use Generics to store data strucures instead of casting
- use interfaces to wrap data structures

```java
public class Sensors {
    private Map sensors = new HashMap();
    public Sensor getById(String id) {
        return (Sensor) sensors.get(id);
    }
    //snip
}
```

- Not every use of `Map` should be encapsulated, but when you use it, make sure you use it inside the class but not passing them to outer system

## Exploring and Learning Boundaries

- It's better to write tests of how you will use the package

## Learning Tests Are Better Than Free

- learning tests cost nothing, we will learn the API anyway
- writing tests is an encapsulated way to get this knowledge
- It increases our understanding

## Using Code That Doesn't Yet Exist

- Use Adapter design pattern to interact with unkown APIS' yet

## Clean Boundaries

- We should avoid letting too much of our code know about the external code
