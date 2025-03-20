# Builder Pattern

## Type: Creational

## Description
Separate the construction of a complex object from its representing so that the same construction process can create different representations.

## Structure
![Builder Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Builder.png)

## Implementation
The example implements the Builder pattern to create objects in a systematic way:

## Sample Code

```php

$builder = new Builder\Car();
$manager = new Manager($builder);
$manager->buildProduct();
$product = $manager->getProduct();

$this->assertEquals("car", $product->getName());
$this->assertEquals(15000, $product->getPrice());

$builder = new Builder\Plane();
$manager = new Manager($builder);
$manager->buildProduct();
$product = $manager->getProduct();

$this->assertEquals("plane", $product->getName());
$this->assertEquals(100500, $product->getPrice());
```

## When to Use
- When the construction process must allow different representations for the object constructed
- When you need to isolate the code for construction and representation
- When you want to give the client the ability to construct complex objects step by step
