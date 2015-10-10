# selenium-scripts
package seleniumScripts;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;

public class Google {

	public static void main(String[] args) {
		WebDriver driver=new FirefoxDriver();
		driver.get("https://edit.europe.yahoo.com/registration?.intl=uk");
		//driver.findElement(By.id("Sign up"));//
		driver.findElement(By.xpath(".//*[@id='first-name']")).sendKeys("indhu");
driver.findElement(By.xpath(".//*[@id='last-name']")).sendKeys("balasubramanian");
driver.findElement(By.xpath(".//*[@id='user-name']")).sendKeys("indhu229");
driver.findElement(By.xpath(".//*[@id='password']")).sendKeys("abc1234");
driver.findElement(By.xpath(".//*[@id='mobile']")).sendKeys("123456789");


WebElement ele1=driver.findElement(By.id("Day"));
Select sel=new Select(ele1);
sel.selectByValue("13");

WebElement ele2=driver.findElement(By.id("Month"));
Select sel1=new Select(ele2);
sel1.selectByValue("July");

WebElement ele3=driver.findElement(By.id("Year"));
Select sel2=new Select(ele3);
sel2.selectByValue("1993");

driver.findElement(By.xpath(".//*[@id='male']")).click();
driver.findElement(By.xpath(".//*[@id='gender-wrapper']/fieldset/div/label[1]"));
driver.findElement(By.xpath(".//*[@id='female']")).click();
driver.findElement(By.xpath(".//*[@id='gender-wrapper']/fieldset/div/label[2]"));
driver.findElement(By.xpath(".//*[@id='mobile-rec']")).sendKeys("987654321");
driver.findElement(By.xpath(".//*[@id='relationship']")).sendKeys("single");
driver.findElement(By.linkText("Yahoo Terms")).click();
driver.findElement(By.linkText("Privacy")).click();
driver.findElement(By.linkText("Cookie Use")).click();
driver.findElement(By.className("Create account")).click();

	}

}
