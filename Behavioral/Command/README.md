# Command Pattern

## Type: Behavioral

## Description
The Command pattern encapsulates a request as an object, allowing you to parameterize clients with different requests, queue or log requests, and support undoable operations.

## Structure
![Command Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/Command.png)

## Implementation
The example implements the Command pattern using a calculator scenario:
- A `Calculator` class that serves as the receiver with operations and state
- Concrete command classes (`Plus`, `Minus`, `Multiplication`, `Division`) that encapsulate specific operations
- A `Window` class that acts as the invoker, accepting and executing commands

## Sample Code

```php
$window = new Window();
$calculator = new Calculator();

$window->placeOperation(new Plus($calculator, 10));
$this->assertEquals(10, $calculator->getResult());

$window->placeOperation(new Minus($calculator, 4));
$this->assertEquals(6, $calculator->getResult());

$window->placeOperation(new Multiplication($calculator, 3));
$this->assertEquals(18, $calculator->getResult());

$window->placeOperation(new Division($calculator, 2));
$this->assertEquals(9, $calculator->getResult());
```

## When to Use
- When you want to parameterize objects with operations
- When you want to queue operations, schedule their execution, or execute them remotely
- When you need to implement undo/redo functionality
- When you want to structure a system around high-level operations built on primitive operations
- When you need to decouple an object that invokes operations from the objects that actually perform these operations
