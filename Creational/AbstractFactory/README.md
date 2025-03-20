# Abstract Factory Pattern

## Type: Creational

## Description
Provides an interface for creating families of related or dependent objects without specifying their concrete class.

## Structure
![Abstract Factory Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/AbstractFactory.png)

## Implementation
The example implements the Abstract Factory pattern with a book publishing scenario:
- An abstract `BookFactory` interface defines methods for creating related products (PHP and MySQL books)
- Concrete factories (`Piter` and `Williams`) implement this interface to create books from specific publishers
- Abstract product interfaces (`PHPBook`, `MySQLBook`) with concrete implementations for each publisher
- The client works with factories and products through their abstract interfaces

## Sample Code

```php
$factory = new BookFactory\Piter();
$book = $factory->createPHPBook();

$this->assertEquals('php', $book->getType());
$this->assertEquals(BookHelper::PUBLISHER_PITER, $book->getPublisher());

$book = $factory->createMySQLBook();

$this->assertEquals('mysql', $book->getType());
$this->assertEquals(BookHelper::PUBLISHER_PITER, $book->getPublisher());

$factory = new BookFactory\Williams();
$book = $factory->createPHPBook();

$this->assertEquals('php', $book->getType());
$this->assertEquals(BookHelper::PUBLISHER_WILLIAMS, $book->getPublisher());

$book = $factory->createMySQLBook();

$this->assertEquals('mysql', $book->getType());
$this->assertEquals(BookHelper::PUBLISHER_WILLIAMS, $book->getPublisher());
```

## When to Use
- When a system needs to be independent from the way its products are created
- When a system should be configured with one of multiple families of products
- When you want to provide a class library of products, and you want to reveal just their interfaces, not their implementations
