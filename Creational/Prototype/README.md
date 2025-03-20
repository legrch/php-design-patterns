# Prototype Pattern

## Type: Creational

## Description
Define an interface for creating an object, but let subclasses decide which class to instantiate. Lets a class defer instantiation to subclasses.

## Structure
![Prototype Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Prototype.png)

## Implementation
The example implements the Prototype pattern to create objects in a systematic way:

## Sample Code

```php

$prototype = new MySQLBookPrototype();
$clone = clone $prototype;

$this->assertEquals($prototype, $clone);
$this->assertTrue($prototype !== $clone);
```

## When to Use
- When a system should be independent of how its products are created
- When you need to avoid building a class hierarchy of factories that parallels the class hierarchy of products
- When instances of a class can have one of only a few different combinations of state
