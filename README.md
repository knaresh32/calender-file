# calender-file
import static org.junit.jupiter.api.Assertions.*;

import org.junit.jupiter.api.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.Dimension;
import org.openqa.selenium.Keys;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.interactions.Actions;

class Testcalendar {

	@Test
	//pass
	void TC1001() throws InterruptedException {
		WebDriver driver = null;
		String browser = "firefox";
		
		if(browser.equalsIgnoreCase("firefox")) {
			System.setProperty("webdriver.gecko.driver", "C:\\Users\\Chawakorn Buakaew\\Desktop\\geckodriver.exe");
			driver = new FirefoxDriver();
		}

		 driver.get("http://localhost/viewcalendar/");
		    driver.manage().window().setSize(new Dimension(699, 728));
		    driver.findElement(By.name("Month")).click();
		    {
		      WebElement dropdown = driver.findElement(By.name("Month"));
		      dropdown.findElement(By.xpath("//option[. = 'February']")).click();
		    }
		    driver.findElement(By.name("Month")).click();
		    driver.findElement(By.name("Day")).click();
		    {
		      WebElement dropdown = driver.findElement(By.name("Day"));
		      dropdown.findElement(By.xpath("//option[. = '3']")).click();
		    }
		    driver.findElement(By.name("Day")).click();
		    driver.findElement(By.cssSelector("button")).click();
	    Thread.sleep(4000);
	    
	    String result = driver.findElement(By.id("date")).getText();
	    assertEquals("Wednesday",result);
	    
	    driver.close();
	}
	
	@Test
	//pass
	void TC1002() throws InterruptedException {
		WebDriver driver = null;
		String browser = "firefox";
		
		if(browser.equalsIgnoreCase("firefox")) {
			System.setProperty("webdriver.gecko.driver", "C:\\Users\\Chawakorn Buakaew\\Desktop\\geckodriver.exe");
			driver = new FirefoxDriver();
		}

		 driver.get("http://localhost/viewcalendar/");
		    driver.manage().window().setSize(new Dimension(699, 728));
		    driver.findElement(By.name("Month")).click();
		    {
		      WebElement dropdown = driver.findElement(By.name("Month"));
		      dropdown.findElement(By.xpath("//option[. = 'January']")).click();
		    }
		    driver.findElement(By.name("Month")).click();
		    driver.findElement(By.name("Day")).click();
		    {
		      WebElement dropdown = driver.findElement(By.name("Day"));
		      dropdown.findElement(By.xpath("//option[. = '15']")).click();
		    }
		    driver.findElement(By.name("Day")).click();
		    driver.findElement(By.cssSelector("button")).click();
	    Thread.sleep(4000);
	    
	    String result = driver.findElement(By.id("date")).getText();
	    assertEquals("Friday",result);
	    
	    driver.close();
	}
	
	@Test
	//pass
	void TC1003() throws InterruptedException {
		WebDriver driver = null;
		String browser = "firefox";
		
		if(browser.equalsIgnoreCase("firefox")) {
			System.setProperty("webdriver.gecko.driver", "C:\\Users\\Chawakorn Buakaew\\Desktop\\geckodriver.exe");
			driver = new FirefoxDriver();
		}

		 driver.get("http://localhost/viewcalendar/");
		    driver.manage().window().setSize(new Dimension(699, 728));
		    driver.findElement(By.name("Month")).click();
		    {
		      WebElement dropdown = driver.findElement(By.name("Month"));
		      dropdown.findElement(By.xpath("//option[. = 'April']")).click();
		    }
		    driver.findElement(By.name("Month")).click();
		    driver.findElement(By.name("Day")).click();
		    {
		      WebElement dropdown = driver.findElement(By.name("Day"));
		      dropdown.findElement(By.xpath("//option[. = '20']")).click();
		    }
		    driver.findElement(By.name("Day")).click();
		    driver.findElement(By.cssSelector("button")).click();
	    Thread.sleep(4000);
	    
	    String result = driver.findElement(By.id("date")).getText();
	    assertEquals("Tuesday",result);
	    
	    driver.close();
	}
	
}
