## What is Maven and why use it?

Maven is an open-source build automation tool developed by the Apache software foundation. The tool allows developers to build and document the lifecycle framework. Maven includes features to compile source code, run tests, package your results and upload these packages to remote repos. It is widely used to manage project dependencies and the whole lifecycle of any project.


## Installing Maven

Maven is a Java tool, so you must have Java installed in order to proceed. 
Then, [download Maven](https://maven.apache.org/download.cgi) and follow the [installation instructions](https://maven.apache.org/install.html). After that, type the following in a terminal to make sure that maven is correctly installed:

`mvn --version`{{execute}}

## Using Maven 💻

For the purpose of this tutorial we have provided a basic Maven project to work from. 

To begin this tutorial clone the following repo:


`git clone https://github.com/isabelredtzer/katacoda-maven-selenium.git`{{execute}}

In order to gain understanding about the structure of a maven project we recommend you to click around to become familiar with it.

To resume this tutorial, navigate to the root of this maven project navigate in the terminal using:

`cd katacoda-maven-selenium/test-project/`{{execute}}

Now you want to compile your Java sources. For this trigger the following Maven command:

`mvn compile`{{execute}}

You should now receive a message in the terminal saying "Build Success"

To run your test use the command:

`mvn test`{{execute}}

You should now receive a message in the terminal saying "Build Success" and information on how many tests were ran aswell as information about how many of them passed and failed.

To test in Maven you can add your tests to the files in the “test”-folder. Click here to open the test-file `./katacoda-maven-selenium/test-project/src/test/java/AppTest.java`{{open}}.

Don't worry if you don't know how to do this yet, you will learn in Step 4 🎉

