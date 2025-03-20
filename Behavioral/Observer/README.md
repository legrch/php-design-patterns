# Observer Pattern

## Type: Behavioral

## Description
The Observer pattern defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.

## Structure
![Observer Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/Observer.png)

## Implementation
The example implements the Observer pattern using a weather station scenario:
- A `WeatherStationObservable` that maintains a list of observers and notifies them of state changes
- Multiple `WeatherCustomerObserver` instances that react to changes in the station
- Methods for attaching, detaching, and notifying observers

## Sample Code

```php
$station = new WeatherStationObservable();
$station->setTemperature(15);
$this->assertEquals(15, $station->getTemperature());

$customer1 = new WeatherCustomerObserver();
$customer2 = new WeatherCustomerObserver();

$station->attach($customer1);
$station->attach($customer2);

$this->assertEquals(null, $customer1->getTemperature());
$this->assertEquals(null, $customer2->getTemperature());

$station->setTemperature(26);
$station->notify();

$this->assertEquals(26, $station->getTemperature());
$this->assertEquals(26, $customer1->getTemperature());
$this->assertEquals(26, $customer2->getTemperature());

$station->setTemperature(10);
$station->notify();

$this->assertEquals(10, $station->getTemperature());
$this->assertEquals(10, $customer1->getTemperature());
$this->assertEquals(10, $customer2->getTemperature());
```

## When to Use
- When changes to one object require changing others, and you don't know how many objects need to be changed
- When an object should be able to notify other objects without making assumptions about those objects
- For establishing loose coupling between objects that interact with each other
- When you need a one-to-many dependency between objects
