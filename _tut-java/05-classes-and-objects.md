---
title: "Classes & Objects"
permalink: /tut-java/classes-objects/
excerpt: "An in-deth walkthrough on classes and objects in java"
modified: 2016-06-30
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

## Class Declaration

While looking at some standard code snippets, one can generally see classes declared as below

```java
public class Employee {
  private String employeeID;
  private int age;
  private String name;

  public void setName(String name){
    //.. some code goes here
  }

  public String getName(){
    //.. some code goes here
  }

  // ...
}
```

There are a few new keywords, `public`, `private` etc. These are Access Modifiers, and can be applied to Classes, and its member variables and methods.

**public**: The public access modifiers specifies, that the marked class, variable or method is publicly available for use. It can be accessed by other classes as required.

**private**: This access modifier specifies that the marked variable or method, is not accessible to the out side world, and can be used accessed with class, by class members.

**Note**: there are other access modifiers as well, which we'll study in upcoming articles.

In general, class has the following basic structure

```java
<class-modifiers> class <class-name> {
    <field-declarations> // These are the member variables/fields/properties of a class. They define 'State'
    <method-declarations> // These are the member methods/function of a class. They define 'Behavior'
    <constructor-declarations>
}
```

+ Full declaration of a methods is called as __method signature__.

----

## Java Code Conventions

**classes & Interfaces**: Should start with a Capital Letter, and follow 'camelCase', for example: Account, EmployeeDetails, PrintWriter, etc.

**variables & methods**: First letter should be lower case and follow 'camelCase'. In case of methods the names should typically be verb-noun pair. e.g.: Variables (accountBalance, buttonWidth), Methods (getBalance, doCalculation, setName) etc

**constants**: to create constants in java, create a varibale marked `static` and `final`. They should be named using uppercase letter, using underscores as separators. e.g. : MIN_BALANCE, MAX_WIDTH.


## Source File Declaration Rules

  + There can only be one public class in a source file.
  + If there is a public class in file, then the class name must match the name of the source file, i.e. a class named `public class Account {}` must be must be in a source file named `Account.java`.
  + (optional) The first non-comment line in the file should be package statement. If no package is defined, its given a default package.
  + (optional) The import statements must go between the package statement and the class declaration.
  + If there is no 'package' or 'import' statements defined, then class declaration must be the first non-comment line in the source file.
  + A file can have more than one non-public class, but only one public class per file is allowed.
  + A file with no public class, can take any name.
