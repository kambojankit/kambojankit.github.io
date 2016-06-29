---
title: "Basics"
permalink: /tut-java/basics/
excerpt: "Learn the basics building blocks of the language, and write something big."
modified: 2016-06-23
---

{% include base_path %}

Computer Programming can be defined as writing logically (semantically) legal statements, using the valid language constructs in a syntactically legal approach. Legal syntax of a language are specified in the grammar rules of the language.

To put it more simply, programming is making use of basic elements of the language, in a valid way, defined by that language. This valid way is called language grammar.

So now we will study these basic constructs of the Java Programming Language.

## Basic Language Constructs

+ __Lexical Token__: The low level language elements, like Identifiers, numbers, operators, and special characters are all lexical tokens of the language. They can be used to make more complex high level language elements like expressions, statements, methods, and classes.

+ __Identifiers__: They are used to denote classes, methods, variables and labels. They are made up of characters, which can letters or digits. *First character must be a letter*. `Unicode Character Set` defines letter and digits in Java. These are the rules the compiler uses to determine whether a name is legal.
    + *Connecting Punctuation* like \_  and *Currency Symbols* like $, ¢, ¥, or £ are valid letters, but should be avoided.
    + Identifiers in Java are *Case Sensitive*.
    + Examples:
        + Valid: name, Name, add_$, $$\_100, grß
        + Invalid: name@, grand-sum, 45rik
+ __Keywords__: Reserved words, predefined in the language and cannot be used to denote entities. They are in *Lowercase*.
    + These 3 keywords are reserved as predefined *literals*, `null`, `true`, `false`
    + `const` and `goto`, are als reserved keywords but are not in use.
    + Below is the list of valid keywords in Java.

    | :---------: |  :------:  | :----------: | :---------:   | :------:  | :---------: |
    | abstract    |  assert    | boolean      | break         | byte      | case        |
    | catch       |  char      | class        | continue      | default   | do          |
    | double      |  else      | enum         | extends       | final     | finally     |
    | float       |  for       | if           | implements    | import    | instanceof  |
    | int         |  interface | long         | native        | new       | package     |
    | private     |  protected | public       | return        | short     | static      |
    | strictfp    |  super     | switch       | synchronized  | this      | throw       |
    | throws      |  transient | try          | void          | volatile  | while       |

+ __Integer Literals__
    + Integer literals in java are represented by the following data types
        + **int**  : this is the default type of integer literals.
        + **long** : suffixing `L` or `l` to integer literals, makes them a long literal type. It is recommended that you use the upper case letter L because the lower case letter l is hard to distinguish from the digit 1.
        + **byte** : there is *no direct way* to specify byte literal
        + **short**: there is *no direct way* to specify short literal
    + Integers can be represented in following number systems.
        + *decimal (base 10)* : default representation
        + *Octal (base 8)*    : specified by using prefix `0` (zero).
        + *hexadecimal (base 16)* : specified by using prefix `0x` or `0X`. Hexadecimals from 'a' to 'f', can also be represented by 'A' to 'F'.
    + Negative numbers are represented by prefixing `-` sign to literal, irrespective of number system.

    |  Decimal    |  Octal    | Hexadecimal |
    | :---------: |  :------: | :----------: |
    | 8           | 010       | 0x8         |
    | 90L         | 0132L     | 0x5aL       |

+ __Floating Point Literals__
    + These literals are represented using following data types.
        + *`float`*  : The literal suffixed with 'f' or 'F', is a float.
        + *`double`* : This is the default for floating point literals. Literal can be explicitly declared double using suffix 'D' or 'd'
    + These can represented in exponential notation using `E`. For example double literal 1.949 can be represented as 194.9E-2.

+ __Escape Sequences__: Certain escape sequences used in the language, like `\t (\u0009)`,`\n (\u000a)`, `\r (\u000d)` etc represent special characters.
    + Remember, these **unicode escape sequences, are pre-processed by the compiler**. So if we character literals `\u000a` or `\u000d`, are used in the program to represent `\r` (CR or Carriage Return) or `\n` (LF or Line Feed or. New Line), compile time errors will be encountered. This is because the unicode representation, will be processed before compiler is run, causing line feeds and carriage returns in the code snippet. Hence always use `\r or \n`, to represent CR or LF. [see example here](http://stackoverflow.com/questions/3866187/why-cant-i-use-u000d-and-u000a-as-cr-and-lf-in-java)

+ __String Literals__: A string literal is a sequence of characters which must be enclosed in double quotes and must occur on a single line. All string literals in java are objects of class `String`. For example: `"Here comes a tab.\t And here comes another one\u0009!"`,  `"What's on the menu?"`

+ __White Spaces__: A white space is a sequence of spaces, tabs, form feeds, and line terminator characters in a Java source file. Line terminators can be newline, carriage return, or a carriage return-newline sequence. A Java program is a free-format sequence of characters that is tokenized by the compiler, i.e., broken into a stream of tokens for further analysis.Separators and operators help to distinguish tokens, but sometimes white space has to be inserted explicitly as a separator. For example, the identifier classRoom will be interpreted as a single token, unless white space is inserted to distinguish the keyword class from the identifier Room. [Ref](https://books.google.co.in/books/about/A_Programmer_s_Guide_to_Java_Certificati.html?id=Q0Xm0o8n-WYC)

+ __Comments__: Comments are a integral part of your code. They allow documenting the code, and enabling other programmers to easily understand your codebase. *Comments are ignored by compiler*. Three types of comments are allowed, as below:
    + **Single Line Comments**: comment starts with `//`, and valid till end of line.

  ```java
    // This is a single line comment.,
    // This is second, single line comment.
  ```
    ----

    + **Multiple Line Comments**:  `/*....*/` represents a multi-line comment. These can be nested and is used as below:

  ```java
    /*
      This is a Multiline comment
      This is the second line of comment
      /* This is nested comment */
    */
  ```

    ----

    + **Documentation Comments**: Documentation comments are usually placed in front of classes, interfaces, methods, and field definitions. Special tags can be used inside a documentation comment to provide more specific information. Such a comment starts with the sequence `/** and ends with the sequence */`

  ```java
    /**
    * This class is SampleClass
    * @author Ankit Kamboj
    * @version 1.0.4
    */
  ```
   ----

## Primitive Data Types

Java has the following primitive data types:

+ __Integer Type__: They represent signed integers through `byte`, `short`, `int` & `long` and unsigned character value (`char`).
    + *byte* : 8 bits long, ranging from -128 to +127
    + *short*: 16 bits long, ranging from -32768 to +32767
    + *int*  : 32 bits long, ranging from -2147483648 to +2147483647
    + *long* : 64 bits long, ranging from -9223372036854775808L to +9223372036854775807L

    ----

    + *char* : 16 bits long, ranging from unicode 0x0 (\u0000) to 0xffff (\uffff). The values are unsigned integers, denote all value in unicode character set, including letter digits and special characters.  
+ __Floating-Point Type__: They represent fractional signed  numbers with, `double` (64 bits) & `float` (32 bits)
+ __Boolean Type__: represents logical values. Have a look at interesting [details about boolean storage here](http://stackoverflow.com/questions/1907318/java-boolean-primitive-type-size)

Note that these primitives are not objects, and each of the primitive type has a range of value and width as shown above, and are operated through special operators in the language, which we discuss later.

## Variable Declarations

Variables are language constructs that are used to store data, of a particular type. Remember Data types in a language are used to identified the type of data. A *variable has a name, type and value associated with it*.

Variables which store references to objects (don't view them as pointers in C++), are called **reference variables**.

Variables declaration is used to specify 'type' and 'name' of the variable. It helps in determining their memory allocation & the values that can be stored in them.

Variable Initialization refers to providing an initial value to the variable.

We can declared & initialize variables as below:

```java
//Variable Declaration, storing Primitive types
char base; // This is a variable of 'char' data type, with name 'base'.
int count; // This is a variable of 'int' data type, with name 'count'.
boolean flag;

// Variable Initialization
char ini = 'C';
int age = 45;
long big = 2147483648L;
double area = 32.563;
float value = 321.34f;

```
### Default Initial Values

Java assigns default initial values to variables, in case no initial value is defined. The default values given are as below

| Data Type | Default Value |
| :-------: | :-----------: |
| boolean   | false         |
| char      | '\u0000'      |
| short     | 0             |
| byte      | 0             |
| int       | 0             |
| `long`    | 0L            |
| double    | 0.0d          |
| float     | 0.0f          |
| objects   | null          |

__Note__: All variables are not provided default values in java. for example, variables declared inside methods are not initialised by default. We will study about them in detail, in chapters to follow.
