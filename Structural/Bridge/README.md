# Bridge Pattern

## Type: Structural

## Description
Convert the interface of a class into another interface clients expect. Lets classes work together that couldn't otherwise because of incompatible interfaces.

## Structure
![Bridge Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/Bridge.png)

## Implementation
The example implements the Bridge pattern to organize classes and objects:

## Sample Code

```php

$square = new SquareShape(new GreenColor());
$result =$square->applyColor();
$this->assertEquals('#00FF00', $result);

$circle = new SquareShape(new RedColor());
$result =$circle->applyColor();
$this->assertEquals('#FF0000', $result);
```

## When to Use
- When you want to avoid a permanent binding between an abstraction and its implementation
- When both the abstractions and their implementations should be extensible through subclasses
- When changes in the implementation should not impact the client code
