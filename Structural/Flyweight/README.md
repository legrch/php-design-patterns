# Flyweight Pattern

## Type: Structural

## Description
Use sharing to support large numbers of fine grained objects efficiently.

## Structure
![Flyweight Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/Flyweight.png)

## Implementation
The example implements the Flyweight pattern to organize classes and objects:

## Sample Code

```php

$factory = new CharacterFactoryFlyweight();
$character1 = $factory->findCharacter('A');
$character2 = $factory->findCharacter('A');
$character3 = $factory->findCharacter('B');

$this->assertInstanceOf('Structural\Flyweight\Character', $character1);
$this->assertInstanceOf('Structural\Flyweight\Character', $character2);
$this->assertInstanceOf('Structural\Flyweight\Character', $character3);

$this->assertTrue($character1 === $character2);
$this->assertFalse($character1 === $character3);
```

## When to Use
- When an application uses a large number of objects that have some shared state
- When the storage costs are high because of the quantity of objects
- When most object state can be made extrinsic
