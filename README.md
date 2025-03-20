# Design Patterns in PHP

This repository contains examples of common design patterns implemented in PHP.

| ![Behavioral](~images/B.png) [Behavioral](Behavioral/) | ![Creational](~images/C.png) [Creational](Creational/) | ![Structural](~images/S.png) [Structural](Structural/) |
| ------------- | ------------- | ------------- |
| [Chain of Responsibility](Behavioral/ChainOfResponsobility/) | [Abstract Factory](Creational/AbstractFactory/) | [Adapter](Structural/Adapter/) |
| [Command](Behavioral/Command/) | [Builder](Creational/Builder/) | [Bridge](Structural/Bridge/) |
| [Interpreter](Behavioral/Interpreter/) | [Factory Method](Creational/FactoryMethod/) | [Composite](Structural/Composite/) |
| [Iterator](Behavioral/Iterator/) | [Prototype](Creational/Prototype/) | [Decorator](Structural/Decorator/) |
| [Mediator](Behavioral/Mediator/) | [Singleton](Creational/Singleton/) | [Facade](Structural/Facade/) |
| [Memento](Behavioral/Memento/) | | [Flyweight](Structural/Flyweight/) |
| [Observer](Behavioral/Observer/) | | [Proxy](Structural/Proxy/) |
| [State](Behavioral/State/) | | |
| [Strategy](Behavioral/Strategy/) | | |
| [Template Method](Behavioral/TemplateMethod/) | | |
| [Visitor](Behavioral/Visitor/) | | |

![Design Patterns Categories](~images/BCS.png)

## Class Relationships

The following relationship types are used in the UML diagrams throughout this repository:

![Aggregation](~images/aggregation.png) **Aggregation** - Describes a "whole-part" relationship where the "part" can exist independently of the "whole". The diamond is placed on the "whole" side.

![Composition](~images/composition.png) **Composition** - A subtype of aggregation in which the "parts" cannot exist separately from the "whole".

![Dependency](~images/dependency.png) **Dependency** - A dashed arrowhead line indicates a class that instantiates objects of another class. The arrow points to the class of the instantiated objects.

![Generalization](~images/generalization.png) **Generalization** - Represents inheritance or interface implementation relationships. The arrow points to the superclass or interface.

## Installation and Testing

1. Clone the repository
2. Run `composer install`
3. Execute tests with `vendor/bin/phpunit`


## License

This project is licensed under the MIT License - see the LICENSE file for details.

