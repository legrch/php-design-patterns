# Iterator Pattern

## Type: Behavioral

## Description
Provide a way to access the elements of an aggregate object sequentially without exposing its underlying representation.

## Structure
![Iterator Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Iterator.png)

## Implementation
The example implements the Iterator pattern with a shop collection:
- A `Shop` class that acts as an aggregator for a collection of items
- An Iterator interface that defines the traversal methods (`next()`)
- The shop provides a `createIterator()` method to return an appropriate iterator
- The client uses the iterator to access elements without knowing the internal structure

## Sample Code

```php
$aggregator = new Aggregator\Shop();
$iterator = $aggregator->createIterator();

$this->assertEquals(1, $iterator->next());
$this->assertEquals(2, $iterator->next());
$this->assertEquals(3, $iterator->next());
$this->assertEquals(null, $iterator->next());
```

## When to Use
- When you want to access an aggregate object's contents without exposing its internal representation
- When you want to support multiple traversals of aggregate objects
- When you want to provide a uniform interface for traversing different aggregate structures
