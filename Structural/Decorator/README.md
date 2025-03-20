# Decorator Pattern

## Type: Structural

## Description


## Structure
![Decorator Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Decorator.png)

## Implementation
The example implements the Decorator pattern to organize classes and objects:

## Sample Code

```php

$widget = new BorderDecorator(
    new ScrollDecorator(
        new TextField(100, 40)
    )
);
$result = $widget->draw();
$this->assertTrue($result);
```

## When to Use
- When you need to add responsibilities to objects dynamically without affecting other objects
- When extension by subclassing is impractical or impossible
- When you want to add functionality to an object without changing its interface
