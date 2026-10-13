const { Builder, By } = require("selenium-webdriver");
async function testCalculator() {
let driver = await new Builder()
.forBrowser("chrome")
.build();

69

try {
await driver.get(
"file:///C:/Users/ADMIN/OneDrive/Desktop/SeleniumJavaScriptTest/index.html"
);
await driver.sleep(1000);
await driver.findElement(By.id("num1"))
.sendKeys("10");
await driver.findElement(By.id("num2"))
.sendKeys("20");
await driver.findElement(By.id("addButton"))
.click();
let result = await driver.findElement(By.id("result"))
.getText();
console.log("Actual Result:", result);
if (result === "Result: 30") {
console.log("TEST PASSED");
} else {
console.log("TEST FAILED");
}
} finally {
await driver.quit();
}
}
testCalculator();
