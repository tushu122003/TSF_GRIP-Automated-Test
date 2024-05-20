package Sparks_internship;
import java.time.Duration;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.support.ui.ExpectedConditions;
import org.openqa.selenium.support.ui.WebDriverWait;

public class sparkstestingtask {

    public static void main(String[] args) throws InterruptedException {
        // Initialize ChromeDriver
        WebDriver driver = new ChromeDriver();
        // Maximize the browser window
        driver.manage().window().maximize();

        // 1. Navigate to the website
        driver.get("https://www.thesparksfoundationsingapore.org/");
        
        Thread.sleep(2000);

        // 2. Verify Page Title
        String expectedTitle = "The Sparks Foundation | Home";
        String actualTitle = driver.getTitle();
        if (actualTitle.equals(expectedTitle)) {
            System.out.println("Page Title is correct: " + actualTitle);
        } else {
            System.out.println("Page Title is incorrect: " + actualTitle);
        }
        
        
        // 3. Check if the logo is displayed
        WebElement logo = driver.findElement(By.xpath("//div[@id='home']//h1/a/img"));
        if (logo.isDisplayed()) {
            System.out.println("Logo is displayed");
        } else {
            System.out.println("Logo is not displayed");
        }
        // 4. Check if the navigation bar is displayed
        WebElement navbar = driver.findElement(By.xpath("//*[@id=\"link-effect-3\"]"));
        if (navbar.isDisplayed()) {
            System.out.println("Navigation bar is displayed");
        } else {
            System.out.println("Navigation bar is not displayed");
        }
        // Locate the "About Us" dropdown and check id about us is there
        WebElement aboutUsMenu = driver.findElement(By.xpath("//*[@id=\"link-effect-3\"]/ul/li[1]/a"));
        if (aboutUsMenu.isDisplayed()) {
            System.out.println("About us is displayed");
        } else {
            System.out.println("About us is not displayed");
        }
        aboutUsMenu.click();
        Thread.sleep(2000);
        // Create an Actions object to perform mouse actions
        Actions actions = new Actions(driver);
        
        // Hover over the "About Us" dropdown to reveal the submenu
        actions.moveToElement(aboutUsMenu).perform();
        
        WebDriverWait wait = new WebDriverWait(driver, Duration.ofSeconds(15));
        WebElement firstOption = wait.until(ExpectedConditions.elementToBeClickable(By.xpath("//*[@id=\"link-effect-3\"]/ul/li[1]/ul/li[1]/a")));

        firstOption.click();
        Thread.sleep(2000);
        // Print the page title to verify navigation
        WebElement innertitle = driver.findElement(By.xpath("//*[@id=\"home\"]/div/div[2]/h2"));
        String innerTitle=innertitle.getText().trim();
        if (innerTitle.contains("Vision, Mission And Values")) {
            System.out.println("Test Passed: Navigated to'Vision, Mission And Values'");
        } else {
            System.out.println("Test Failed");
        }
        
     // Locate the element containing the text "The Sparks Foundation"
        WebElement logoElement = driver.findElement(By.cssSelector("a.navbar-brand"));
        
        // Get the text from the element
        String logoText = logoElement.getText().trim();
        
        // Print the text to verify
        System.out.println("Logo Text: " + logoText);
        
        // Verify that the text is "The Sparks Foundation"
        if (logoText.contains("The Sparks Foundation")) {
            System.out.println("Test Passed: The text is 'The Sparks Foundation'");
        } else {
            System.out.println("Test Failed: The text is not 'The Sparks Foundation'");
        }
        Thread.sleep(2000);
        // Locate the "Policies and Code" dropdown and check id about us is there
        WebElement Policies_code = driver.findElement(By.xpath("//*[@id=\"link-effect-3\"]/ul/li[2]"));
        if (Policies_code.isDisplayed()) {
            System.out.println("Policies and Code is displayed");
        } else {
            System.out.println("Policies and Code is not displayed");
        }
        Policies_code.click();
        //check if dropdown works
        WebElement dropdown = driver.findElement(By.xpath("//*[@id=\"link-effect-3\"]/ul/li[2]/ul"));
        if (dropdown.isDisplayed()) {
            System.out.println("Drop Down Working");
        } else {
            System.out.println("Drop Down NOT working.");
        }		
        
        Thread.sleep(2000);
        // Create an Actions object to perform mouse actions
        Actions actions2 = new Actions(driver);
        
        // Hover over the "Policies_code" dropdown to reveal the submenu
        actions2.moveToElement(Policies_code).perform();
        
        WebDriverWait wait2 = new WebDriverWait(driver, Duration.ofSeconds(15));
        WebElement policies = wait2.until(ExpectedConditions.elementToBeClickable(By.xpath("//*[@id=\"link-effect-3\"]/ul/li[2]/ul/li[1]")));

        policies.click();
        Thread.sleep(2000);
        // Locate the "Contact Us" dropdown and check id about us is there
        WebElement ContactUs = driver.findElement(By.xpath("//*[@id=\"link-effect-3\"]/ul/li[6]"));
        if (ContactUs.isDisplayed()) {
            System.out.println("Contact us is displayed");
        } else {
            System.out.println("Contact us is not displayed");
        }
        ContactUs.click();
        // Print the page title to verify navigation
        WebElement innertitle2 = driver.findElement(By.xpath("//*[@id=\"home\"]/div/div[2]/h2"));
        String innerTitle2=innertitle2.getText().trim();
        if (innerTitle2.contains("Contact Us")) {
            System.out.println("Test Passed: Navigated to'Contact Us' ");
        } else {
            System.out.println("Test Failed");
        }

        Thread.sleep(2000);
        // Print the page title to verify navigation
        WebElement Workshopsec = driver.findElement(By.xpath("/html/body/div[4]/div/div[1]/div[4]/h3"));
        String Workshop=Workshopsec.getText().trim();
        if (Workshop.contains("Workshop")) {
            System.out.println("Workshop Is available ");
        } else {
            System.out.println("Workshop is not available");
        }

        Thread.sleep(2000);
        // Locate the "Glimpses for Kids"  and check if It there
        WebElement Glimps = driver.findElement(By.xpath("/html/body/div[4]/div/div[1]/div[4]/ul/li[1]/a"));
        if (Glimps.isDisplayed()) {
            System.out.println("Glimps For Kids is displayed");
        } else {
            System.out.println("Glimps for Kids is not displayed");
        }
        Glimps.click();
        Thread.sleep(10000);
        //locate kids poster and check if its displayed
        WebElement kidsposter=driver.findElement(By.xpath("/html/body/div[2]/div/div[1]/div/div[1]/div/div/img"));
        if (kidsposter.isDisplayed()) {
            System.out.println("Kids poster is displayed");
        } else {
            System.out.println("Kids poster is not displayed");

        }
        // Close the browser
        driver.quit();
  }
}

