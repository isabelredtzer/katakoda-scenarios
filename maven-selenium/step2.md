
## What is Selenium?

In order to test a web application manually a multitude of test cases have to be written. Enacting and reenacting hundreds of scenarios on all benchmarked browsers, flagging what broke and trying to pinpoint the source of that breakage. Selenium is an open-source automated testing framework which facilitates this, it is used to validate web applications across different browsers and platforms simultaneously. 

## Advantages of Selenium

Selenium is platform-independent, meaning it can be used on every operating system (Linux, Windows, Macintosh etc) and it can test web applications against various browsers (Firefox,Chrome, Safari etc). It also features a lot of flexibility for the tester since tests can be coded in several programming languages such as Java, Python, Perl, PHP, and Ruby. It can also be integrated with tools like JUnit and TestNG for test management. 


## Adding Selenium Maven dependency

You can add these Selenium Maven dependencies in your pom.xml as shown below:
`<dependency>
   <groupId>org.seleniumhq.selenium</groupId>
   <artifactId>selenium-java</artifactId>
   <version>4.1.2</version>
</dependency>
<dependency>
   <groupId>org.apache.poi</groupId>
   <artifactId>poi</artifactId>
   <version>3.17</version>
</dependency>
<dependency>
   <groupId>org.apache.poi</groupId>
   <artifactId>poi-ooxml</artifactId>
   <version>3.17</version>
</dependency>`{{copy}}