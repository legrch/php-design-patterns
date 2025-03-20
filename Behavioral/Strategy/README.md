# Strategy Pattern

## Type: Behavioral

## Description
The Strategy pattern defines a family of algorithms, encapsulates each one, and makes them interchangeable. It allows the algorithm to vary independently from clients that use it.

## Structure
![Strategy Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/Strategy.png)

## Implementation
The example implements the Strategy pattern using different billing strategies:
- A `Customer` class that can use different billing strategies
- Concrete strategy implementations (`NormalBillingStrategy` and `HappyHourBillingStrategy`)
- The ability to switch strategies at runtime

## Sample Code

```php
$customer = new Customer(new NormalBillingStrategy);
$customer->addToBilling($price=2.5, $quantity=2);
$this->assertEquals(5.0, $customer->sumOfBilling());

$customer->setStrategy(new HappyHourBillingStrategy);
$customer->addToBilling($price=2.5, $quantity=4);
$this->assertEquals(10.0, $customer->sumOfBilling());
```

## When to Use
- When you need different variants of an algorithm
- When you want to avoid exposing complex algorithm-specific structures
- When an algorithm uses data that clients shouldn't know about
- When a class defines many behaviors that appear as multiple conditional statements
