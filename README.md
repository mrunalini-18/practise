# Sample Selenium Script to Open a Website and Print Page Title

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.service import Service
from webdriver_manager.chrome import ChromeDriverManager

# Step 1: Setup Chrome driver
driver = webdriver.Chrome(service=Service(ChromeDriverManager().install()))

# Step 2: Open a website
driver.get("https://example.com")

# Step 3: Print page title
print("Page Title is:", driver.title)

# Step 4: Find an element and print text (example)
heading = driver.find_element(By.TAG_NAME, "h1")
print("Heading text:", heading.text)

# Step 5: Close the browser
driver.quit()
