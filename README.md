# Amazon-functional-test1




package demo;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;

public class amazonTesting {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		System.setProperty("webdriver.chrome.driver", "C:\\Users\\user\\Downloads\\chromedriver_win32\\chromedriver.exe");
		WebDriver driver = new ChromeDriver();
	    driver.get("https://www.amazon.co.uk/");     
	}

}



Testcase 


package demo;

import org.testng.annotations.Test;

public class Add {

	//Add item to the basket
	
	@Test
	public void additem_basket(){
	System.out.println("Add item to the basket");    
    }
	@Test
	public void searchfor_item(){
	System.out.println("Search for item");  
	}
    }


Features 


#Each feature contains one feature
#Feature files use Gherkin langauge - business language
Feature: Search and add an item to basket

 #A feature may have given different specific scenarios
 #Scenarios use Given - When - Then structure
 Scenario: User search and add item to basket
 
    Given user launch amazon Website
    When user click enter button   
    Then user navigate to amazon Website 


stepImplementations

package stepImplementations;

import cucumber.api.java.en.Given;
import cucumber.api.java.en.Then;
import cucumber.api.java.en.When;

public class BDDLoginTest {

	@Given("^user launch amazon Website$")
	public void user_launch_amazon_Website(){
	System.out.println("user launch amazon application");  
	}
	
	@When("^user click enter button$") 
	public void user_click_button(){
	System.out.println("user click enter button");  
	}
	
	@Then("^user navigate to amazon Website$")
	public void user_navigate_Website(){
	System.out.println("user navigate to amazon Website");   
	}
    }


TestRunner

package CucumberTest;

import org.junit.runner.RunWith;

import cucumber.api.CucumberOptions;
import cucumber.api.junit.Cucumber;

@RunWith(Cucumber.class)
@CucumberOptions(
		features = "Features", glue = {"stepImplementations"}   
		)
public class CucumberTestRunner {

}

