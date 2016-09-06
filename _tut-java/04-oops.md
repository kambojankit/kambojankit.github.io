---
title: "Object Oriented Programming"
permalink: /tut-java/oops/
excerpt: "Understanding the concept and principles of OOPs paradigm"
modified: 2016-05-28
---

{% include base_path %}

We have had a look at the primitive data types supported in Java. But the real strength of the language lies in its support for Object Oriented Programming Paradigm. I say supports because its not a pure OOPs language, since it supports primitive types. In a pure OOPs language, everything including the pre-defined types must be objects, which is not the case with java. Now we will try to dive into the concepts of OOPs and how is it different from procedural language like C.

## OOPs
__Object Oriented Programming__ paradigm emphasize on 'data' and how to operate on that 'data'. This is a different approach, when compared to procedural programming where emphasis is on procedures ( routines or sub-routines) and on the steps of execution, where in order for data to be available to more than one function it must be declared GLOBAL.

Putting it in simple terms, in procedural language, the behavior of the system is written as a sequence of steps in routines or procedures. Then these behaviors can be triggered by some other routine or sub-routine.

In OOPs, the system is defined in terms of data objects. The data can have a 'state' and 'behavior'.

'__State__' of data object refers to its properties at a particular time in the program.'State' in java is maintained with fields/properties.

'__Behavior__' as the name implies refers to what can the data object do. Its defined using the methods or functions. Using an analogy of shopping cart, if cart is an object, its 'state' refers to the amount of items the cart has at some point of time, while behavior of the cart can be 'Add Item To Cart', 'Remove Item from Cart', 'Checkout' etc.

All the interaction with the objects is done using its methods.

## Object

Its a representation of '__state__' and '__behavior__' as defined above. They are often used to model/represent a real-world object.
Example: Cars has state (engine, gear, wheels, doors etc) and behavior (start engine, shifting gear, accelerate, apply brake etc ), similarly Person has state (mouth, hands, leg etc) and behavior (talk, walk, eat etc).

To understand OOPs, we should try to view and identify the state and behavior of the real-world objects.

## Class

It represents a blueprint or prototype from which objects can be created. Class is a way to represent template, a structure that can be used to create Object representation of the real world entities.
For example: Shopping Cart, in real world is a container for items which we shop. The items can be added or removed from the cart. To represent such a cart, lets try to identify it's state.
At any point of time, a cart will hold an item. So our cart in java, will have a state representing the items it can hold.

Hence we can view our cart as below:

```java
  // A cart capable of holding one item at a time.
  class Cart{
    string itemName;

    //Behavior yet to be added.
  }
```

But in this example, we can hold, only one item, which is not what we intend to do, thus to hold more than one item, we can define our cart in java to hold an array of items as below:

```java
  // A cart capable of holding more than one item at a time.
  class Cart{
    string[] itemName;

    //Behavior yet to be added.
  }
```
Now to add behavior to our cart, lets think what can we do to cart in real world. Well we can add or remove items to/from cart.
Hence we can add the behavior to our cart as below:

```java
  // A cart capable of holding more than one item at a time.
  class Cart{
    string[] itemName;

    //behavior (add item)
    void addItemToCart(){
      //... code to add item to array itemName
    }

    // behavior (removal of item)
    void removeItemFromCart(){
      //... code to remove item from array itemName
    }
    //...
  }
```

___Thus classes are templates representing structure of the real world object in java world. Objects are Instances of these classes, which hold data (state) and behave during the execution of program. These objects (instances of class) are created using the template (class defined) during the program execution.___

**Note**: Don't worry, if syntax sound unfamiliar, we will cover it all, in further articles.

## Principles of OOPs

### Abstraction
The process of abstraction in Java is used to hide certain details (mainly implementation of logic) and only show the essential features of the object. Its a generic terms, which refers mostly to generalization of functionality of Object types.

For example, Phone in general, exposes dial as a functionality or we can say abstracts, dial as a function of all phones.

'Dial' function is available in all types of phone. We can always dial a number to make a call, on almost all types of phones, even though how those phones processes the dial instruction can be different.

### Encapsulation
Encapsulation can be defined as a way to enclose the state and behavior together as a unit. It thus enables to hide the state of the objects from the outer world, and allows interaction only through its exposed methods.

It can be viewed as a tool or strategy, used as part of abstraction.

For example, the dial functionality of a Nokia phone, may be implemented inside a class NokiaPhone, having a state (to store number to be dialled) and a behavior dial ( to dial the number), as shown below

```java
class NokiaPhone {
  ...
  String numberToDial;
  ...

  void dial(){
    // code to dial the number
  }

  void addNumberToDial(String number){
    this.numberToDial = number;
  }
}
```

Now BlackBerryPhone, may have a different implementation as shown below:

```java
class BlackBerryPhone {
  ...
  long num;   // holds number to dial
  ...

  void dial(){
    // code to dial the number
  }

  void setNumber(long number){
    this.num = number;
  }
}
```

Thus classes above have different implementations for 'dial' behavior and are encapsulated inside of classes NokiaPhone and BlackBerryPhone.

### Inheritance

Inheritance as the name implies refers to inheriting the state and behavior from the parent of a class. Its a way to derive one class from another, further extending the features of the parent class.

Its a very useful and powerful way of organizing the code.

Java provides a keyword `extends`, which allows to create a class from a parent class, having all the exposed behavior of the parent class.

For example, A class MountainBike, RoadBike, LeisureBike from the parent Bike.

```java
  class Bike {
    int currentGear;
    int gearCount;
    ...

    void changeGear() {
      //Change gear by +1
    }
    ...
  }

  class MountainBike extends Bike {
    //Code goes here, and all elements of Bike available here.
  }

  class RoadBike extends Bike {
    //Code goes here, and all elements of Bike available here.
  }

  class LeisureBike extends Bike {
    //Code goes here, and all elements of Bike available here.
  }
```

### Polymorphism
A greek term, wherein Poly mean **many**, Morph means **forms**. Polymorphism is a way to allow different functionalities under the same name. Methods Overloading and Overriding are two ways in which we achieve polymorphism in Java.

We study polymorphism at length in further articles.
