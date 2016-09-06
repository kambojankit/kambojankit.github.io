---
title: "Installation"
permalink: /tut-java/installation/
excerpt: "Here we learn how to install Java, on our machines for development"
modified: 2016-05-21
---

{% include base_path %}

To start building programs in java, we need to install JDK i.e Java Development Kit.

But before we proceed, lets try to understand how everything is wired together.

![Java basic flow](/images/tutorials/tut-java/java-basic-1.jpg)

For now consider that there are two main components that we would be dealing with:

+ __Java Compiler__: Its used to convert the java code into a intermediate format called byte-code. This byte-code is what JRE understands.
+ __Java Runtime (JRE)__: Java Runtime Environment, understand the byte-code, and interprets it to machine code, respective to the architecture on which its installed.

Java Development Kit, provides us all the required tools and utilities to write Java code. It contains 'Java Compiler', 'JRE' and many other utilities, which we will take a look at later.

___Note___: Generally, JRE is preinstalled on most of the machines, sometimes referred to as Java-Plugin.

To Install JDK, please follow the following steps:

+ __*Windows*__:
  1. Download the installer, as per your operating system from [Oracle Website](https://java.com/en/download/manual.jsp). Ensure that you download 32-bit or 64-bit installed as per the architecture of your machine.
  2. Follow the instructions in the installer, to complete the install.
  3. Add the `javac` and `java` path, to the 'PATH' Environment Variable.
      1. Go to `Start > Control Panel > System and Security > System > Advanced system settings`
      2. Now click on `Environment Variable`, and under `System Variable`, click `New`
      3. Use `JAVA_HOME` as the `Variable Name` and `<Java-Directory>` as `Variable Value`.
      4. `<Java-Directory>` is the where java is installed and is generally `C:\Program Files\Java\jdk<version>`, and same path should be used as `JAVA_HOME`. Also ensure that path doesn't include the bin folder.
      5. Now find `PATH` variable under `System Variable` and select `Edit`.
      6. Append `;%JAVA_HOME/jre/bin;%JAVA_HOME/bin;` at the end of `Variable Value`.
  4. Now Java installation can be verified using instructions provided in _Verify Installation_ section below.
  5. Your machine is now ready for Java Development

+ __*Ubuntu*__:

  **Installing Java on Ubuntu**

  1. Use the command `sudo apt-get update` to update the `apt-get` package lists.
  2. Now use the below command to install Oracle Java on ubuntu. (Open JDK is not recommended)

  ```bash
  $ sudo add-apt-repository ppa:webupd8team/java
  $ sudo apt-get install oracle-java8-installer
  $ sudo apt-get install oracle-java8-set-default
  ```

  Java 8 is now setup on your machine.

  **Setting JAVA_HOME**

  1. Open terminal, and type `sudo nano /etc/environment`, this will open nano editor, to edit the environment variables.
  2. Now add the line `JAVA_HOME="/usr/lib/jvm/java-8-oracle"`, to the opened file.
  3. Reload this file by executing command `source /etc/environment`
  4. Now JAVA_HOME has been set up. Please verify by executing command `echo $JAVA_HOME`.

+ __*Mac*__: [see instructions here](http://docs.oracle.com/javase/7/docs/webnotes/install/mac/mac-jdk.html)

## Verify Installation

Installation can be verified using the below instructions.

#### Verify JRE Installation

```bash
   C:\>java -version
   java version <your-java-version>
   ...
```
If you successfully get the displayed output, on executing `java -version`, then JRE is successfully installed on your machine.

#### Verify Compiler Installation
Now to verify that Java compiler has also been set up properly, execute the below command

```bash
   C:\>javac -version
   java <your-java-version>
```
If you successfully get the displayed output, then be assured that Java setup is complete on your machine.
---
## Installing Library Source & Documentation

Library source code is downloaded as part of the JDK bundle, in `src.zip` file, at JAVA_HOME. All we need to do is unpack the files to a src folder in JAVA_HOME, so follow the below steps (in a command line shell):

```bash
   C:\> cd %JAVA_HOME%

```
