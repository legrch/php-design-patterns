# Proxy Pattern

## Type: Structural

## Description
Provide a surrogate or placeholder for another object to control access to it.

## Structure
![Proxy Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Proxy.png)

## Implementation
The example implements the Proxy pattern to organize classes and objects:

## Sample Code

```php

$image = new ProxyImage('photo_10000.jpg');

$this->assertInstanceOf('Structural\Proxy\Image\Proxy', $image);
$this->assertNull($image->getImage());

$result = $image->display();

$this->assertTrue($result);
$this->assertInstanceOf('Structural\Proxy\Image\Real', $image->getImage());
```

## When to Use
- When you need a more versatile or sophisticated reference to an object than a simple pointer
- When you want to control access to an object
- When you need to add functionality when accessing an object
