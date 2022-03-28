# TestNG with WebDrivers

Now that you have set up your Maven project and integrated your Selenium environment, it’s time to test it out and start writing your tests. 

To be able to use TestNG with Maven we need to add the dependency in the pom.xml file.

`pom.xml`{{open}}

Add the following dependency: 

`
    <dependency>
        <groupId>org.testng</groupId>
        <artifactId>testng</artifactId>
        <version>7.5</version>
        <scope>test</scope>
    </dependency>

`{{copy}}

Start by locating the AppTest.java file.

`AppTest.java`{{open}}

Add the needed imports to the AppTest.java file:

<pre class="file" data-target="clipboard">
import org.openqa.selenium.chrome.ChromeDriver;

import io.github.bonigarcia.wdm.WebDriverManager;

import org.testng.Assert;
import org.testng.annotations.Test;

import static org.testng.Assert.assertTrue;
</pre>

Add a dummy test to make sure the environment is working: 

<pre class="file" data-target="clipboard">
 @Test
    public void dummyTest(){
        assertTrue(true);
    }
</pre>

And after that, go ahead and try out using the WebDriver Test! 
<pre class="file" data-target="clipboard">
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
</pre>

To make sure that your tests are running correctly, run the command mvn test in the terminal:

`mvn test`{{execute}}

Happy testing! 