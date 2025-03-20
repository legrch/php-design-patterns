# Facade Pattern

## Type: Structural

## Description
Provide a unified interface to a set of interfaces in a subsystem. Defines a high- level interface that makes the subsystem easier to use.

## Structure
![Facade Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/Facade.png)

## Implementation
The example implements the Facade pattern to organize classes and objects:

## Sample Code

```php

$computer = new ComputerFacade;
$result = $computer->start();
$this->assertNotEmpty($result);

---
Facade::start():

$this->processor->freeze();
$data = $this->hd->read($lba = self::BOOT_SECTOR, $size = self::SECTOR_SIZE);
$this->memory->load(
    $position = self::BOOT_ADDRESS,
    $data
);
$this->processor->jumpTo($position = self::BOOT_ADDRESS);
$this->processor->execute();
```

## When to Use
- When you want to provide a simple interface to a complex subsystem
- When there are many dependencies between clients and implementation classes
- When you want to layer your subsystems
