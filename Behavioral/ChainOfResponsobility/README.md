# ChainOfResponsobility Pattern

## Type: Behavioral

## Description
Avoid coupling the sender of a request to its receiver by giving more than one object a chance to handle the request. Chain the receiving objects and pass the request along the chain until an object handles it.

## Structure
![ChainOfResponsobility Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/ChainOfResponsobility.png)

## Implementation
The example implements the ChainOfResponsobility pattern to define object behaviors and communication:

## Sample Code

```php

$loger1 = new Logger\Email(LoggerHelper::PRIORITY_ERROR);
$loger2 = new Logger\File(LoggerHelper::PRIORITY_NOTICE, $loger1);
$loger = new Logger\Profiling(LoggerHelper::PRIORITY_DEBUG, $loger2);

$loger->message('Start profiling module1', LoggerHelper::PRIORITY_DEBUG);
$loger->message('Access denied for User1', LoggerHelper::PRIORITY_NOTICE);
$loger->message('Roll back the transaction', LoggerHelper::PRIORITY_ERROR);
```

## When to Use
- When more than one object may handle a request, and the handler isn't known
- When you want to issue a request to one of several objects without specifying the receiver explicitly
- When the set of objects that can handle a request should be specified dynamically
