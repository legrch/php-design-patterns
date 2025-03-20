# Interpreter Pattern

## Type: Behavioral

## Description
Given a language, define a representation for its grammar along with an interpreter that uses the representation to interpret sentences in the language.

## Structure
![Interpreter Pattern](https://github.com/legrch/php-design-patterns/blob/master/~images/Interpreter.png)

## Implementation
The example implements the Interpreter pattern to define object behaviors and communication:

## Sample Code

```php

// "a b c - +";
$expression = new Plus(
    new Variable("a"),
    new Minus(
        new Variable("b"),
        new Variable("c")
    )
);

$context = new Context(["a"=>25, "b"=>6, "c"=>5]);
$result = $expression->interpret($context);
$this->assertEquals(26, $result);

// "d a b c - + -";
$expression = new Minus(
    new Variable("d"),
    new Plus(
        new Variable("a"),
        new Minus(
            new Variable("b"),
            new Variable("c")
        )
    )
);

$context = new Context(["a"=>25, "b"=>6, "c"=>5, "d"=>30]);
$result = $expression->interpret($context);
$this->assertEquals(4, $result);
```

## When to Use
- When you need to implement a simple language
- When you have a language to interpret, and you can represent statements as abstract syntax trees
- When the grammar is simple and efficiency is not a critical concern
