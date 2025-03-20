# Adapter Pattern

## Type: Structural

## Description
The Adapter pattern converts the interface of a class into another interface that clients expect. It allows classes to work together that couldn't otherwise because of incompatible interfaces.

## Structure
![Adapter Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Adapter.png)

## Implementation
The example implements the Adapter pattern:
- A `RectangleLegacy` class with an incompatible interface
- A `RectangleShapeAdapter` that adapts the legacy rectangle to a new interface
- The adapter translates calls from the client to the adaptee (legacy object)

## Sample Code

```php
$rectangle = new RectangleShapeAdapter(new RectangleLegacy());
$result = $rectangle->display($x1=10, $y1=10, $x2=20, $y2=20);
$this->assertTrue($result);
```

## When to Use
- When you want to use an existing class, but its interface doesn't match what you need
- When you want to create a reusable class that cooperates with classes that don't necessarily have compatible interfaces
- When you need to use several existing subclasses but it's impractical to adapt their interface by subclassing each one
- When you need to make components work together that weren't designed to work together
- When you need to integrate components from different libraries or frameworks
