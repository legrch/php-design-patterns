# Mediator Pattern

## Type: Behavioral

## Description
Define an object that encapsulates how a set of objects interact. Promotes loose coupling by keeping objects from referring to each other explicitly and it lets you vary their interactions independently.

## Structure
![Mediator Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/Mediator.png)

## Implementation
The example implements the Mediator pattern to define object behaviors and communication:

## Sample Code

```php

$book = new BookMediator(
    $title = "Design Patterns",
    $author = "Erich Gamma"
);

$title = $book->getTitle();
$author = $book->getAuthor();

$this->assertEquals("Design Patterns", $title->getName());
$this->assertEquals("Erich Gamma", $author->getName());

$book->setTitle("Design Patterns: Elements of Reusable Object-Oriented Software");
$book->setAuthor("Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides");


$this->assertEquals("Design Patterns: Elements of Reusable Object-Oriented Software", $title->getName());
$this->assertEquals("Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides", $author->getName());
```

## When to Use
- When a set of objects communicate in well-defined but complex ways
- When reusing an object is difficult because it refers to and communicates with many other objects
- When behavior that's distributed between several classes should be customizable without a lot of subclassing
