# Template Method Pattern

## Type: Behavioral

## Description
The Template Method pattern defines the skeleton of an algorithm in an operation, deferring some steps to subclasses. It allows subclasses to redefine certain steps of an algorithm without changing the algorithm's structure.

## Structure
![Template Method Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/TemplateMethod.png)

## Implementation
The example implements the Template Method pattern using a game scenario:
- An abstract `Game` class defines the template method `play()` which calls three abstract methods in sequence
- Concrete subclasses (`FootballGame` and `BasketballGame`) implement these abstract methods with their specific behavior

## Sample Code

```php
$game = new FootballGame;
$result = $game->play();
$this->assertTrue($result);

$game = new BasketballGame;
$result = $game->play();
$this->assertTrue($result);
```

## When to Use
- When you want to let clients extend only particular steps of an algorithm
- When you have several classes that contain nearly identical algorithms with some minor differences
- When you want to avoid code duplication by moving common behavior to a single class
