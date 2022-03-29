# Maven Dependency for TestNG

Now that you have set up your Maven project and integrated your Selenium environment, it’s time to test it out and start writing your tests. 

To be able to use TestNG with Maven we need to add the dependency in the pom.xml file.

`./katacoda-maven-selenium/test-project/pom.xml`{{open}}

Add the following dependency: 

<pre class="file" data-filename="./katacoda-maven-selenium/test-project/pom.xml" data-target="insert"  data-marker="<!--Add dependency for TestNG-->">
&lt;dependency>
    &lt;groupId>org.testng&lt;/groupId>
    &lt;artifactId>testng&lt;/artifactId>
    &lt;version>7.5&lt;/version>
    &lt;scope>test&lt;/scope>
&lt;/dependency>
</pre>

# Test Structure

Start by locating the AppTest.java file.

`./katacoda-maven-selenium/test-project/src/test/java/AppTest.java`{{open}}

Add the needed imports to the AppTest.java file:

<pre class="file" data-filename="./katacoda-maven-selenium/test-project/src/test/java/AppTest.java" data-target="insert"  data-marker="//Add imports here">
import org.openqa.selenium.chrome.ChromeDriver;

import io.github.bonigarcia.wdm.WebDriverManager;

import org.testng.Assert;
import org.testng.annotations.Test;

import static org.testng.Assert.assertTrue;
</pre>



Add a dummy test to make sure the environment is working:

<pre class="file" data-filename="./katacoda-maven-selenium/test-project/src/test/java/AppTest.java" data-target="insert"  data-marker="//Add dummyTest here">
@Test
public void dummyTest(){
    assertTrue(true);
}
</pre>


Now you can run `mvn compile`{{execute}} and `mvn test`{{execute}} to see your test in action!

# Test WebDrivers locally 
And after that, go ahead and try out using the WebDriver Test! 🎉
This is not supported by Katacoda so to make sure you've understood all the steps - repeat them locally and add the following code to your AppTest.java file!


<pre class="file" data-target="clipboard">
import org.openqa.selenium.chrome.ChromeDriver;

import io.github.bonigarcia.wdm.WebDriverManager;

import org.testng.Assert;
import org.testng.annotations.Test;

import static org.testng.Assert.assertTrue;

public class AppTest {
    
    @Test
    public void dummyTest(){
        assertTrue(true);
    }

    @Test
    public void testNew(){
        WebDriverManager.chromedriver().setup();

        ChromeDriver driver = new ChromeDriver();

        driver.manage().window().maximize();
        driver.get("https://www.google.com/");
        String actualUrl="https://www.google.com/";

        String expectedUrl= driver.getCurrentUrl();
        Assert.assertEquals(expectedUrl,actualUrl);
        driver.close();
    }
}
</pre>

To make sure that your tests are running correctly, run the command mvn test in the terminal:
`mvn compile`{{execute}}
`mvn test`{{execute}}

# Endless possibilities of WebDrivers 🤯

Here are some useful examples that you can do with WebDrivers to explore your testing further:

* get() - The command launches a new browser and opens
the specified URL in the browser instance
* getTitle() - The command is used to retrieve the title of the webpage the user is currently working on.
* getAttribute() - The command is used to retrieve the value of the specified attribute
* Select selectByValue = new Select(driver.findElement(By.id("SelectID_One"))); & selectByValue.selectByValue - allows you to select multiple values to make sure the webpage works as expected.

Happy testing! 
