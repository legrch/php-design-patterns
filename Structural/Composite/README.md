# Composite Pattern

## Type: Structural

## Description
Convert the interface of a class into another interface clients expect. Lets classes work together that couldn't otherwise because of incompatible interfaces.

## Structure
![Composite Pattern](https://github.com/olegre/DesignPatterns/blob/master/~images/Composite.png)

## Implementation
The example implements the Composite pattern to organize classes and objects:

## Sample Code

```php

$sentence = new Sentence();

$wHello = new Word();
$wHello->add(new Character('H'));
$wHello->add(new Character('e'));
$wHello->add(new Character('l'));
$wHello->add(new Character('l'));
$wHello->add(new Character('o'));

$sentence->add($wHello);

$sentence->add(new Character(','));
$sentence->add(new Character(' '));

$wWorld = new Word();

$wWorld->add(new Character('w'));
$wWorld->add(new Character('o'));
$wWorld->add(new Character('r'));
$wWorld->add(new Character('l'));
$wWorld->add(new Character('d'));

$sentence->add($wWorld);
$sentence->add(new Character('!'));

$this->assertEquals('Hello, world!', $sentence->display());
```

## When to Use
- When you want to represent part-whole hierarchies of objects
- When you want clients to be able to ignore the difference between compositions of objects and individual objects
- When the structure can have any level of complexity
