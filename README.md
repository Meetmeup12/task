




     
  Selenium Eclipse Webdrive   
     
     package selenium;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.support.ui.Select;
import org.testng.annotations.AfterClass;
import org.testng.annotations.AfterMethod;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.BeforeMethod;
import org.testng.annotations.Test;

import io.github.bonigarcia.wdm.WebDriverManager;

public class FirstTest {

	static WebDriver driver;
	
	
	
	public static void main(String[] args) {
		
    
		WebDriverManager.chromedriver().setup();
		WebDriver driver = new ChromeDriver();;

		driver.get("https://i6.io/");

		driver.findElement(By.cssSelector(".fs-cc-banner_button")).click();
		
		driver.findElement(By.xpath("/html/body/div[16]/div[1]/div/nav/a[1]")).click();
		
		driver.findElement(By.xpath("/html/body/div[5]/div/div[3]/a")).click();
		
		driver.findElement(By.id("First-Name")).sendKeys("Test");
		driver.findElement(By.id("Last-Name")).sendKeys("Quality");
		
		
		//driver.findElement(By.id("Company-2")).sendKeys("Leave Blank");
		
		driver.findElement(By.id("Email")).sendKeys("aaaa88888");
		
		//driver.findElement(By.id("Number-2")).sendKeys("075-5554332");
		
		WebElement element =driver.findElement(By.xpath("//*[@id=\"Enquiry-2\"]"));
		Select sel = new Select(element);
		sel.selectByValue("Careers");
		
		WebElement firstEle = sel.getFirstSelectedOption();
		System.out.println("first element ="+firstEle.getText());
		

		//driver.findElement(By.id("Message-2")).sendKeys("Leave Blank");
		
		driver.findElement(By.xpath("//*[@id=\"Subscribe-to-Email\"]")).click();
		
		driver.findElement(By.cssSelector(".i6-button.features-button")).click();
		
		driver.quit();
		
		
	}
	}
	
	//Maven Dependencies
	<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	 <modelVersion>4.0.0</modelVersion>
	<groupId>SeleniumTraining</groupId>
	 <artifactId>Selenium</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<dependencies>
	 <dependency>
	  <groupId>org.seleniumhq.selenium</groupId>
	   <artifactId>selenium-java</artifactId>
	    <version>3.141.59</version>
	</dependency>
			<dependency>
		    <groupId>io.github.bonigarcia</groupId>
		    <artifactId>webdrivermanager</artifactId>
		    <version>5.0.3</version>
		</dependency>
			  </dependencies>
			</project>

// Please follow the instruction to run the test
1.	Lunch eclipse 
2.	Copy and paste the Maven dependencies in the porn.xml file in eclipse 
3.	Create New Java Project  and create Class
4.	Copy and paste the test script
	
5	import org.openqa.selenium.By;
	
6	import org.openqa.selenium.WebDriver;

7	import org.openqa.selenium.WebElement;

8	import org.openqa.selenium.support.ui.Select;

9	Create WebDriverManager.chromedriver().setup();

	WebDriver driver = new ChromeDriver();
	
10.	Run the script 



The Test failed! Please fill in this field pop-up after Clicked on the submit button. 
This occurred due to the incorrect email and blank mandatory field (message field & Company field) were not completed and it returned. 
First Name, Last Name, Enquiry Type and phone number passed
Error : (SLF4J: Failed to load class "org.slf4j.impl.StaticLoggerBinder"}
