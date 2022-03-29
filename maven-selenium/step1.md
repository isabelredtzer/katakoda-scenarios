## What is maven and why use it?

Maven is an open-source build automation tool developed by the Apache software foundation. The tool allows developers to build and document the lifecycle framework. Maven includes features to compile source code, run tests, package your results and upload these packages to remote repos. It is widely used to manage project dependencies and the whole lifecycle of any project.

The project structure of a Java project in Maven generally looks like this: 

![Image](/maven-selenium/img/mvnimage.png) 


## Installing maven

Maven is a Java tool, so you must have Java installed in order to proceed. 
Then, [download Maven](https://maven.apache.org/download.cgi) and follow the [installation instructions](https://maven.apache.org/install.html). After that, type the following in a terminal to make sure that maven is correctly installed:

`mvn --version`{{execute}}

## Using maven

For the purpose of this tutorial we have provided a basic maven project to work from. 

To begin this tutorial clone the following repo:


`git clone https://github.com/isabelredtzer/katacoda-maven-selenium.git`{{execute}}


In order to get to the the root of this maven project navigate in the terminal using:

`cd katacoda-maven-selenium/test-project/`{{execute}}

Now you want to compile your Java sources. For this trigger the following Maven command:

`mvn compile`{{execute}}

You should now receive a message in the terminal saying "Build Success"

To run your test use the command:

`mvn test`{{execute}}

You should now receive a message in the terminal saying "Build Success" and information on how many tests were ran aswell as inforamtion about how many of them passed and failed

To test in Maven you can add your tests to the files in the “test”-folder. An example of this is that the tests for the class src/main/java/App.java are located in src/test/java/AppTest.java
Don't worry if you don't know how to do this yet, you will learn in step4
