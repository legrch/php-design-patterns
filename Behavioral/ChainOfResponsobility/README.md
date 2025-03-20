# Chain of Responsibility Pattern

## Type: Behavioral

## Description
Avoid coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. Chain the receiving objects and pass the request along the chain until an object handles it.

## Structure
![Chain of Responsibility Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/ChainOfResponsibility.png)

## Implementation
The example implements the Chain of Responsibility pattern:
- A handler interface with a method to process requests
- Concrete handlers that implement the processing logic
- Each handler has a reference to the next handler in the chain
- Handlers either process the request or pass it to the next handler

## Sample Code

```php
$handler = new Handler\ConcreteHandler1();
$handler->successor(new Handler\ConcreteHandler2());

$this->assertTrue($handler->handleRequest('request1'));
$this->assertTrue($handler->handleRequest('request2'));
$this->assertFalse($handler->handleRequest('request3'));
```

## When to Use
- When more than one object may handle a request, and the handler isn't known
- When you want to issue a request to one of several objects without specifying the receiver explicitly
- When the set of objects that can handle a request should be specified dynamically
