---
title: "Overview"
permalink: /tut-java/overview/
excerpt: "This is the overview of java programming language"
modified: 2016-06-20T15:54:02-04:00
header:
  teaser: teaser/default.jpg
categories:
  - Java
tags:
  - Java
---

{% include base_path %}

Welcome to the tutorial series on Java. This tutorial is designed not only as an introduction to the language, but also serves the purpose of gaining in-depth knowledge of the Java world. It is equally beneficial for beginner to intermediate programmers.

## Pre-Requisites

To understand the content, readers should have introductory knowledge on programming in any language, be it C, C++, Python, etc.

## Java: What's In a Word

_'Well, its a programming language'_, thats what this word bring up in most of our minds. But, Java is not only a Programming Language.
More than a language and Java is a *Platform*, with a rich set of Libraries, an Execution Environment, reusable code API etc.

> Java is a whole *Platform*, with a huge library, containing lots of reusable code, and an execution environment that provides services such as security, portability across operating systems and automatic garbage collection. - Cay S. Horstmann

We can summarize the key aspects of Java as below:

+ __Simple__ : Java as a programming language has simple and cleaner syntax, then its previous counterparts like C++. Its easy to understand and work with.
+ __Object Oriented__ : Java belongs to  Object Oriented Programming Paradigm. We will study OOPs as we call it, at length in topics to come, but simply put, with OOPs we focus on Data and Interfaces on that Data.
+ __Network Savvy__ : Java has built in library to allow Network Programming, and accessing network is as easy as communicating to the local file system.
+ __Robust__ : Java focuses, not only on early error detection but also on Runtime error detection. This allows for capability in the program to behave well in error situations.
+ __Secure__ : Java has a very high use in Networked/Distributed environments, and Java complements it equally with security built right into the platform. Java has had very few security bugs. Java enables creating virus free and tamper-free systems.
+ __Architecture Neutral__ : The Java compiled code, called byte-code executes on a Virtual Machine (VM). byte-code is independent of the underlying machine architecture. Hence it can easily be converted by VM to machine language on any machine architecture on the fly.
+ __Portable__ : There are no machine dependent aspects of the language specification. The byte-code executes on VM. Any machine with a compatible VM can be used to execute the Java Programs.
+ __High Performance__ : The VM interprets the byte-code to machine code. VM has the capability to compile the byte-code to machine code for a particular architecture, through Just-In time compiler (JIT). Thus the sluggishness introduced due to interpretation is to much extent overcome, using JIT.
+ __Multi-Threaded__ : Java allows programming using thread. Thus for a multiprocessor system, if Operating System utilizes the multi processor environment, Thread in Java can lead to better interactive responsiveness and real time behavior.

## A little History
Java originated back in 1991, at Sun Micro Systems (now taken over by Oracle), by engineers led by James Gosling & Patrick Naughton. The Problem statement they tried to solve was creating a language to use in consumer micro systems like cable T.V. switch boxes. It had to be small and lightweight. An important aspect required was Machine Independence, since different manufacturers may choose different CPUs.
The project was code named 'Green'. Gosling however wanted to name the language 'Oak', but since the name was already taken, it came to be known as 'Java'.

However, Java as a product was not accepted by any manufacturers at that time. Hence the actual purpose for which it was designed was not realized yet. Outside of Sun, the world wide web part of internet was growing, and so was the need of a good browser and the java team, realized, the ideas their language was built on (architecture-neutral, real-time, reliable, secure etc) was what was more or less needed by browsers.

The Browser was built by Patrick Naughton & Jonathan Payne. They made java capable of executing code inside of browsers.  This "Proof Of Technology", was showcased on 1995 at SunWorld, and proved to be the game changer.

In 1998, soon to be more popular, Java 1.2 was released, and change the world with "Write Once, Run Anywhere" tagline. Then came Java 1.5 as a major release (the rest 1.3 and 1.4 were mostly incremental improvements to Java 1.2), with many new language specifications.
It was renamed to Java 5, later in 2004 JavaOne conference.

Version 6 was introduced in 2006, with mostly performance improvements.

Version 7 was released in 2011, with basic language enhancements like string handling in switch statements etc.

#### References
+ *Core Java Vol - I*
