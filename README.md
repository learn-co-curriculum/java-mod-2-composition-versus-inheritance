# Composition vs. Inheritance

## Learning Goals

- Explain the difference between inheritance and composition

## What is Composition?

**Composition** is when a class has references to other classes as members.
We can think of composition as having a "has-a" relationship:

- A library has a book.
- A house has a kitchen.
- A car has a steering wheel

Consider the following example:

```java
public class Book {
    private String title;
    private String author;
    
    Book(String title, String author) {
        this.title = title;
        this.author = author;
    }
}

public class Library {
    
    // A library has an array of books
    Book[] books = new Book[10];
    
}
```

This is a very simplified example, but it shows that we know a library has
several books. So we can represent this in code by using the `Book` objects in
the composition of a `Library`.

## When to use Composition and Inheritance

As we can see, composition differs from inheritance since inheritance is
associated with an "is-a" relationship:

- A cat is an animal.
- Football is a sport.
- A car is a vehicle.

When deciding on whether to use composition or inheritance, it is important to
remember the "is-a" versus "has-a" relationships as they serve different
purposes.
