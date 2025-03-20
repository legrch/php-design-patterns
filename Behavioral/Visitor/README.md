# Visitor Pattern

## Type: Behavioral

## Description
Represent an operation to be performed on the elements of an object structure. Lets you define a new operation without changing the classes of the elements on which it operates.

## Structure
![Visitor Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Visitor.png)

## Implementation
The example implements the Visitor pattern to define object behaviors and communication:

## Sample Code

```php

$visitor  = new PriceItemVisitor();
$item = new BookItem($name = "Im Westen nichts Neues, Erich Maria Remarque", $price = 22.50);
$price = $item->accept($visitor);
$this->assertEquals(17.5, $price);

$item = new FruitItem($name = "apple", $pricePerKg = 1.5, $weight = 2);
$price = $item->accept($visitor);
$this->assertEquals(3.0, $price);
```

## When to Use
- When you need to perform operations on all elements of a complex object structure
- When you want to avoid polluting the classes with operations that are only needed for specific operations
- When the classes defining the object structure rarely change, but you often want to define new operations over the structure
