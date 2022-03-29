
## What is Selenium?

In order to test a web application manually a multitude of test cases have to be written. Enacting and reenacting hundreds of scenarios on all benchmarked browsers, flagging what broke and trying to pinpoint the source of that breakage. Selenium is an open-source automated testing framework which facilitates this, it is used to validate web applications across different browsers and platforms simultaneously. 

## Advantages of Selenium

Selenium is platform-independent, meaning it can be used on every operating system (Linux, Windows, Macintosh etc) and it can test web applications against various browsers (Firefox,Chrome, Safari etc). It also features a lot of flexibility for the tester since tests can be coded in several programming languages such as Java, Python, Perl, PHP, and Ruby. It can also be integrated with tools like JUnit and TestNG for test management. 


## Adding Selenium Maven dependencies 💻


Maven provides pom.xml which is the core of any project. This is the configuration file containing project information and configuration details used by Maven build. It is located in the root directory of each project. 
You can add these Selenium Maven dependencies in your pom.xml as shown below:

<pre class="file" data-filename="./katacoda-maven-selenium/test-project/pom.xml" data-target="insert"  data-marker="<!--Add dependency for Selenium-->">
&lt;dependency>
   &lt;groupId>org.seleniumhq.selenium&lt;/groupId>
   &lt;artifactId>selenium-java&lt;/artifactId>
   &lt;version>4.1.2&lt;/version>
&lt;/dependency>
</pre>


Apache POI is the most commonly used API for Selenium data driven tests. Add the dependency below:

<pre class="file" data-filename="./katacoda-maven-selenium/test-project/pom.xml" data-target="insert"  data-marker="<!--Add dependency for poi-->">
&lt;dependency>
   &lt;groupId>org.apache.poi&lt;/groupId>
   &lt;artifactId>poi&lt;/artifactId>
   &lt;version>3.17&lt;/version>
&lt;/dependency>
</pre>

Apache POI is also the master project for developing pure Java ports of file formats based on Office Open XML. Add the dependy below: 

<pre class="file" data-filename="./katacoda-maven-selenium/test-project/pom.xml" data-target="insert"  data-marker="<!--Add dependency for poi-ooxml-->">
&lt;dependency>
   &lt;groupId>org.apache.poi&lt;/groupId>
   &lt;artifactId>poi-ooxml&lt;/artifactId>
   &lt;version>3.17&lt;/version>
&lt;/dependency>
</pre>
