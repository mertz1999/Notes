# Design Pattern Quera Course Notes

This file include some notes which I extracted from design pattern quera course.

## Factory

This pattern is a **creational** pattern which contain of 4 different stages:
* **Product Interface** : Abstract layer of a product
* **Concrete Product Classes** : Different class for each product type
* **Interface for Product Factory** : We use prv. instances in this class, we don't use those classes and instances directly.
* **Product Factory** : Hole system join together in this stage.

### Advantages:
* Open/Closed SOLID principle
* Without coupling and classes dependencies

### Disadvantages:
* It can be more complicated
* In most use cases you can find dependency injection as simpler way.



## Singleton

This pattern is also **creational** method like factory and the most important thing about this method is: we can make only one instance of this class.
* Can be used for classes which we need to make an instance for the whole system. Like database management system.


## Observer
Is one of the **behavioral** pattern in software engineering.
In this pattern we have 2 important classes:
* **Publisher** : This class will send messages to others.
* **Observer** : Linsten to publisher class for recieving messages.


## Mediator
Another **behavioral** pattern. This pattern is used to make relationship between different classes. You know in SOLID you need to break the relation between classes.

* ** Mediator ** : for making relation.
* **Other objects** : Other objects which need to have relation together but they can not do this without **Mediator**.
