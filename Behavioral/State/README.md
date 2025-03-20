# State Pattern

## Type: Behavioral

## Description
Allow an object to alter its behavior when its internal state changes. The object will appear to change its class.

## Structure
![State Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/State.png)

## Implementation
The example implements the State pattern to define object behaviors and communication:

## Sample Code

```php

$context = new context(new StateA());
$this->assertInstanceOf('Behavioral\State\State\A', $context->getState());

$context->request();
$this->assertInstanceOf('Behavioral\State\State\B', $context->getState());

$context->request();
$this->assertInstanceOf('Behavioral\State\State\C', $context->getState());

$context->request();
$this->assertInstanceOf('Behavioral\State\State\A', $context->getState());
```

## When to Use
- When an object's behavior depends on its state, and it must change its behavior at runtime
- When operations have large, multipart conditional statements that depend on the object's state
- When a context can be in one of many states, with state-specific behavior
