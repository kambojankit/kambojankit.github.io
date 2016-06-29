---
title: "Classes & Objects"
permalink: /tut-java/classes-objects/
excerpt: "An in-deth walkthrough on classes and objects in java"
modified: 2016-06-28
---

{% include base_path %}

This article takes you to the details of creating classes and working with objects in java.

## Class

A class is essentially a template, used to represent a real world entity in java. Consider for example, to create a building in real world, we would first create its blueprint detailing the structure that needs to be build. Similarly in the java world a class defines the specification, which would be used to create an object during the program execution.

The class specifies the structure to represent the __state__ and __behavior__ of an object or Instance of the class.

## Object

They are the representation of real world objects in java, as per the specification of their template i.e. class. So Objects are the instances of classes and have **state** and **behavior**.

__State__: state refers to the value of an entity at a particular moment in time. for example, an engine can be in running or stopped state or the state of an ATM machine can be the amount of cash present in the machine.

state of an object is represented by variables defined in a class.

```java
/* In ATM below, the state of ATM is
    maintained using cash variable of type int
*/
class Atm {
  int cash;
}
```

__Behavior__: behavior represents the actions than can be performed on the instance of a class. for example, car can be started or stopped. The behavior in java world is specified using methods or functions.

```java
/* In ATM below, the state of ATM is
    maintained using cash variable of type int
*/
class Atm {
  int cash;

  // withdraw represents the behavior of ATM machine, to pull out cash.
  int withdraw(int amount) {
    if(this.cash >= amount) {
      this.cash -= amount;
      return amount;
    }else {
      return 0;
    }
  }
}
```

**Remember**: We can interact with the object, using the methods specified. The methods are responsible for changing the state of the object. We can create multiple ATM machine objects, and each one would have its own state i.e each one can have different amount of cash present in the ATM. But we can perform same actions on all instances of ATM and i.e withdraw cash from the ATM.


## Class Structure
