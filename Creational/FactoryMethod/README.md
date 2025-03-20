# FactoryMethod Pattern

## Type: Creational

## Description
Define an interface for creating an object, but let subclasses decide which class to instantiate. Lets a class defer instantiation to subclasses.

## Structure
![FactoryMethod Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/FactoryMethod.png)

## Implementation
The example implements the FactoryMethod pattern to create objects in a systematic way:

## Sample Code

```php

$factory = (new Factory\Plane())->instance();
$this->assertInstanceOf('Creational\FactoryMethod\Product\Plane', $factory);

$factory = (new Factory\Car())->instance();
$this->assertInstanceOf('Creational\FactoryMethod\Product\Car', $factory);
```

## When to Use
- When a class can't anticipate the type of objects it must create
- When a class wants its subclasses to specify the objects it creates
- When you want to localize the knowledge of which class gets created
