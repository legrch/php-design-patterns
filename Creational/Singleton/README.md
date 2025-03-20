# Singleton Pattern

## Type: Creational

## Description
The Singleton pattern ensures a class only has one instance and provides a global point of access to it.

## Structure
![Singleton Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Singleton.png)

## Implementation
The example implements the Singleton pattern:
- A `Singleton` class with a private constructor to prevent direct instantiation
- A static method `instance()` that returns the single instance, creating it if necessary
- The instance is stored in a static variable

## Sample Code

```php
$singleton = Singleton::instance();
$singleton2 = Singleton::instance();
$this->assertTrue($singleton===$singleton2);
```

## When to Use
- When exactly one instance of a class is needed throughout the application
- When you need stricter control over global variables
- When you want to avoid creating a global variable but still need global access
- When you need to coordinate actions across the system

## Considerations
- The pattern can make the code harder to test
- It introduces global state into the application
- Thread safety must be ensured in multithreaded environments
