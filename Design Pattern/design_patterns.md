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


## State
* **behavioral** pattern
* Like **finite states** in FPGA designing.
* 1. **state interface class** : This class is an abstract layer for each state. 
  2. **state classes** : For each new state we implement new state class based in state interface.
  3. **context class** : Defining behaviors methods.
 
## Strategy
* **behavioral** pattern
* Can be use for situation which we need to group some functions


## Iterator
* For problems like music playlist for play one-by-one and also going back or forward
* 1. **Iterator Interface** : All Iteration workflow
  2. **PostIterator Class** : Implement all next or other functions
  3. **IterableCollection Interface** and **PostCollection Class**: for getting a list of all content and pass them through PostIterator class


## Abstrct Factory
* For example: make an application which can be loaded automatically for each os
* 1. **Abstract Products** : main abstract class for hole product features
  2. **Concrete Products** : for each products (different os) implement products features
  3. **Abstract Factory** : a factory abstract class for creation of classes
  4. **Concrete Factory** : for each product use this for build a product
 
## Visotor
* This pattern include a class which can automatically capture some information like number of views per post

