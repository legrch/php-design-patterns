# Memento Pattern

## Type: Behavioral

## Description
Without violating encapsulation, capture and externalize an object's internal state so that the object can be restored to this state later.

## Structure
![Memento Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Memento.png)

## Implementation
The example implements the Memento pattern to define object behaviors and communication:

## Sample Code

```php

$originator = new Originator();
$originator->setState("On");

$memento = $originator->createMemento();

$caretaker = new Caretaker();
$caretaker->setMemento($memento);

$originator->setState('Off');

$memento = $caretaker->getMemento();

$originator->restore($memento);
```

## When to Use
- When you need to capture an object's internal state for later restoration
- When a direct interface to obtaining the state would expose implementation details
- When you need to implement checkpoints and an undo mechanism
