# Selenium Web Drivers 
A Selenium Webdriver allows you to accept commands and send them to the browser. This allows you to write tests that can test the functionality of websites in different browsers in parallel. The driver will control the browser by communicating with it and asking it to perform tasks. However, keep in mind that this is only for web applications. 

The Selenium WebDrivers are available for many languages such as Java, C#, Ruby, Python, and more. It can be easily integrated with Gradle and Maven. It can also be integrated with CI tools such as Jenkins. 

In this specific tutorial, you will learn how to integrate Selenium WebDrivers Testing in a Maven project. 


# How to install Selenium WebDriver
There are three ways to install a Selenium WebDriver. Keep in mind that these are browser specific. In this tutorial we will show you different methods to install WebDrivers. However, this specific tutorial will be using Driver Management Software and use the ChromeDriver. 

## Driver Management Software
There are multiple versions of drivers and to make sure that you have the correct one there are thrid party libraries which can help you. This library is integrated with Maven and will make sure that you have the correct driver for your browser. 

Start by adding the following dependecy to your pom.xml file:

<pre class="file" data-filename="./katacoda-maven-selenium/test-project/pom.xml" data-target="insert"  data-marker="<!--Add dependency for WebDriver-->">

    &lt;dependency>
        &lt;groupId>org.testng&lt;/groupId>
        &lt;artifactId>testng&lt;/artifactId>
        &lt;version>7.5&lt;/version>
        &lt;scope>test&lt;/scope>
    &lt;/dependency>

</pre>

On the next page you will get to use the webdriver to test! 

## Alternative methods to install Selenium WebDriver

**Alternative Method 1. PATH environment variable** 

This is how it's done from a Bash terminal. You can click [here](https://www.selenium.dev/documentation/webdriver/getting_started/install_drivers/#quick-reference) if you are working in a Zsh or Windows terminal. 

To see what directories are already on PATH, open a Terminal and execute:

    echo $PATH

If the location to your driver is not already in a directory listed, you can add a new directory to PATH:

    echo 'export PATH=$PATH:/path/to/driver' >> ~/.bash_profile
    source ~/.bash_profile

You can test if it has been added correctly by starting the driver:
 
    chromedriver

If your PATH is configured correctly above, you will see some output relating to the startup of the driver:

    Starting ChromeDriver 95.0.4638.54 (d31a821ec901f68d0d34ccdbaea45b4c86ce543e-refs/branch-heads/4638@{#871}) on port 9515
    Only local connections are allowed.
    Please see https://chromedriver.chromium.org/security-considerations for suggestions on keeping ChromeDriver safe.
    ChromeDriver was started successfully. 

You can regain control of your command prompt by pressing Ctrl+C

**Alternative Method 2. Hardcoded location**

If you prefer to download the driver and store it locally you can do so and then integrate it in your Java code as follows: 

    System.setProperty("webdriver.chrome.driver","/path/to/chromedriver");

    ChromeDriver driver = new ChromeDriver();



