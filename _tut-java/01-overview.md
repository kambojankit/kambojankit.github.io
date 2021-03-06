---
title: "Overview"
permalink: /tut-java/overview/
excerpt: "This is the overview of java programming language"
modified: 2016-05-20
header:
  teaser: teaser/default.jpg
categories:
  - Java, Java 8
tags:
  - Java, Java-8, Java Index,
---

{% include base_path %}

Welcome to the tutorial series on Java. This tutorial is designed not only as an introduction to the language, but also serves the purpose of gaining in-depth knowledge of the Java world. It is equally beneficial for beginner to intermediate programmers.

What makes java special is its ease of use and rich set of functionalities it provides. Java has widespread adoption and is language of choice for writing most of the enterprise applications.

## Pre-Requisites

This tutorial is targeted towards the group attending online/classroom training in Java. However a person with basic programming knowledge in language like C, C++ etc, should be able to follow through without any supervision.

In case you are interested in attending the training, please contact-us through e-mail.

## Java: What's In a Word

The first question that comes in most of our minds is: _'What is Java?'_. Most of us, do have an answer though partially correct.
_'Java, is a programming language'_, thats what we initially think of. But, Java is not only a Programming Language.
More than a language, Java is a *Platform*, with a rich set of Libraries, an Execution Environment, reusable code API etc.

> Java is a whole *Platform*, with a huge library, containing lots of reusable code, and an execution environment that provides services such as security, portability across operating systems and automatic garbage collection. - Cay S. Horstmann

We can summarize the key aspects of Java as below:

+ __Simple__ : Java as a programming language has simple and cleaner syntax, then its previous counterparts like C++. Its easy to understand and work with.
+ __Object Oriented__ : Java belongs to  Object Oriented Programming Paradigm. We will study OOPs as we call it, at length in topics to come, but simply put, with OOPs we focus on Data and Interfaces on that Data.
+ __Network Savvy__ : Java has built in library to allow Network Programming, and accessing network, is as easy as communicating to the local file system.
+ __Robust__ : Java focuses, not only on early error detection but also on Runtime error detection. This allows for capability in the program to behave well in error situations.
+ __Secure__ : Java has a very high use in Networked/Distributed environments, and Java complements it equally with security built right into the platform. Java has had very few security bugs. Java enables creating virus free and tamper-free systems.
+ __Architecture Neutral__ : The Java compiled code, called byte-code executes on a Virtual Machine (VM). byte-code is independent of the underlying machine architecture. Hence it can easily be converted by VM to machine language on any machine architecture on the fly.
+ __Portable__ : There are no machine dependent aspects of the language specification. The byte-code executes on VM. Any machine with a compatible VM can be used to execute the Java Programs.
+ __High Performance__ : The VM interprets the byte-code to machine code. VM has the capability to compile the byte-code to machine code for a particular architecture, through Just-In time compiler (JIT). Thus the sluggishness introduced due to interpretation is to much extent overcome, using JIT.
+ __Multi-Threaded__ : Java allows programming using thread. Thus for a multiprocessor system, if Operating System utilizes the multi processor environment, Thread in Java can lead to better interactive responsiveness and real time behavior.

## A little History
Java originated back in 1991, at Sun Micro Systems (now taken over by Oracle), by engineers led by James Gosling & Patrick Naughton. The Problem statement they tried to solve was creating a language to use in consumer micro systems like cable T.V. switch boxes. It had to be small and lightweight. An important aspect required was Machine Independence, since different manufacturers may choose different CPUs.
The project was code named 'Green'. Gosling however wanted to name the language 'Oak', but since the name was already taken, it came to be known as 'Java'.

However, Java as a product was not accepted by any manufacturers at that time. Hence the actual purpose for which it was designed was not realized, yet. Outside of Sun, the world wide web part of internet was growing, and so was the need of a good browser and the java team, realized, the ideas their language was built on (architecture-neutral, real-time, reliable, secure etc) was what, more or less was needed by browsers.

The Browser was built by Patrick Naughton & Jonathan Payne. They made java capable of executing code inside of browsers.  This "Proof Of Technology", was showcased on 1995 at SunWorld, and proved to be the game changer.

In 1998, soon to be more popular, Java 1.2 was released, and change the world with "Write Once, Run Anywhere" tagline. Then came Java 1.5 as a major release (the rest 1.3 and 1.4 were mostly incremental improvements to Java 1.2), with many new language specifications.
It was renamed to Java 5, later in 2004 JavaOne conference.

Version 6 was introduced in 2006, with mostly performance improvements.

Version 7 was released in 2011, with basic language enhancements like string handling in switch statements etc.

Version 8 was released in 2014, with significant improvements like lambda expressions, security enhancements etc.

## Versioning

+ Java Version SE 8
  - released on March 18, 2014.
  - Lambda expressions
  - default methods
  - Streams API
  - Nashorn - Javascript Runtime
  - New Date API
  - Functional Programming

+ Java Version SE 7
  - Code named Dolphin and released on July 28, 2011.
  - Strings in switch Statement
  - Type Inference for Generic Instance Creation - Multiple Exception Handling
  - Support for Dynamic Languages
  - Try with Resources
  - Java NIO Package
  - Binary Literals, underscore in literals
  - Diamond Syntax
  - Automatic null Handling

+ Java Version SE 6
  - Code named Mustang and released on December 11, 2006.
  - Scripting Language Support
  - JDBC 4.0 API
  - Java Compiler API
  - Pluggable Annotations
  - Native PKI, Java GSS, Kerberos and LDAP support.
  - Integrated Web Services.
  - Lot more enhancements.

+ J2SE Version 5.0
  - Code named Tiger and released on September 30, 2004.
  - Generics
  - Enhanced for Loop
  - Autoboxing/Unboxing
  - Typesafe Enums
  - Varargs
  - Static Import
  - Metadata (Annotations)
  - Instrumentation

+ J2SE Version 1.4
  - Code named Merlin and released on February 6, 2002 (first release under JCP).
  - XML Processing
  - Java Print Service
  - Logging API
  - Java Web Start
  - JDBC 3.0 API
  - Assertions
  - Preferences API
  - Chained Exception
  - IPv6 Support
  - Regular Expressions  
  - Image I/O API

+ J2SE Version 1.3
  - Code named Kestrel and released on May 8, 2000.
  - Java Sound
  - Jar Indexing
  - A huge list of enhancements in almost all the java area.


+ J2SE Version 1.2
  - Code named Playground and released on December 8, 1998.
  - Collections framework.
  - Java String memory map for constants.
  - Just In Time (JIT) compiler.
  - Jar Signer for signing Java Archive (JAR) files.
  - Policy Tool for granting access to system resources.
  - Java Foundation Classes (JFC) which consists of Swing 1.0, Drag and Drop,
  and Java 2D class libraries.
  - Java Plug-in
  - Scrollable result sets, BLOB, CLOB, batch update, user-defined types in JDBC.
  - Audio support in Applets.

+ JDK Version 1.1
  - Released on February 19, 1997
  - JDBC (Java Database Connectivity)
  - Inner Classes
  - Java Beans
  - RMI (Remote Method Invocation)
  - Reflection (introspection only)


+ JDK Version 1.0
  Codenamed Oak and released on January 23, 1996.

#### References
+ *Core Java Vol - I*
