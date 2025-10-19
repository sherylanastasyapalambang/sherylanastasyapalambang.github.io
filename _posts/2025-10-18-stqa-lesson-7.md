---
title: "STQA (Lesson 7) - Introduction to Selenium WebDriver"
date: 2025-10-18 16:40:00 +0800
categories: [Software Testing, Quality Assurance]
image: /assets/img/stqa7.png
tags: [selenium, python, webdriver, browser automation, saucedemo]
excerpt: "Learn the basics of Selenium WebDriver — what it is, why testers love it, and how to start automating browser interactions using Python."
---

This week, we’ll explore how testers can **automate web applications** using **Selenium WebDriver**. If you’ve ever thought, *“Can I make my browser click buttons or fill out forms automatically?”*, that’s exactly what Selenium does. 🚀

---

## 🧩 What Is Selenium and Selenium WebDriver?
**Selenium** is an open-source tool for automating web browsers.
It lets you simulate user actions like clicking buttons, typing text, or verifying if something appears on a webpage, just like a real user would do.  
  
**Selenium WebDriver**, specifically, is the component that directly controls the browser.  
It interacts with the browser’s native API to perform actions and check results.  
  
Think of it this way:  
Selenium = the whole testing framework 🧰
Selenium WebDriver = the driver behind the wheel 🚗

---

## 🌟 Why Use Selenium?
There are many reasons why Selenium is a favorite among testers and developers alike:
1. **Cross-Browser Testing** – Works with Chrome, Firefox, Edge, Safari, etc.
2. **Multi-Language Support** – Compatible with Python, Java, C#, JavaScript, and more.
3. **Automation of Real User Flows** – You can test login, checkout, navigation, etc.
4. **Integration-Friendly** – Works well with testing frameworks like Pytest or CI/CD tools.
5. **Open Source** – 100% free and widely supported by the testing community.

In short: Selenium helps you ensure your website behaves exactly how users expect it to automatically.

---

## ⚙️ Installing Selenium (Python Version)
Before we start testing, let’s install Selenium in Python.  
Make sure you already have Python installed on your system.  

```bash
pip install selenium
```

Then, install a WebDriver (a browser controller). For Chrome, use:  
- Download ChromeDriver:  
  [https://sites.google.com/chromium.org/driver/](https://sites.google.com/chromium.org/driver/)
- Make sure the ChromeDriver version matches your Chrome browser version.   
  
After that, you’re ready to automate! 🎉

---

## 🌍 Opening a Browser with Selenium
Here’s how to open a browser and visit a website using Selenium and Python:

```python
from selenium import webdriver

# Create a new Chrome browser
driver = webdriver.Chrome()

# Open a website
driver.get("https://www.saucedemo.com/")

# Wait a bit before closing
input("Press Enter to close browser...")
driver.quit()
```

After running this code, Chrome will open automatically and go to the [SauceDemo](https://www.saucedemo.com/) website.

---

## 🧠 Interacting with HTML Elements
Once the browser is open, Selenium allows you to **interact with page elements** such as input boxes, buttons, and links.  
  
You can find elements using various locators:
- `find_element(By.ID, "id_name")`
- `find_element(By.NAME, "username")`
- `find_element(By.XPATH, "//input[@type='text']")`
- `find_element(By.CSS_SELECTOR, ".btn-primary")`
  
Example:  
```python   
from selenium.webdriver.common.by import By

driver.find_element(By.ID, "user-name").send_keys("standard_user")
driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()
```

In the code above, Selenium:
1. Finds the username input box and types the username.
2. Finds the password field and types the password.
3. Finds the login button and clicks it.
  
Just like a real person using the browser! 🖱️

---

## 💻 Example: Simple Interaction with SauceDemo

Let’s put it all together in one simple test script.

```python
from selenium import webdriver
from selenium.webdriver.common.by import By
import time

# Create browser instance
driver = webdriver.Chrome()
driver.get("https://www.saucedemo.com/")

# Interact with login form
driver.find_element(By.ID, "user-name").send_keys("standard_user")
driver.find_element(By.ID, "password").send_keys("secret_sauce")
driver.find_element(By.ID, "login-button").click()

# Wait for 3 seconds
time.sleep(3)

# Verify login success (check page title or element)
if "inventory" in driver.current_url:
    print("✅ Login successful!")
else:
    print("❌ Login failed!")

# Close browser
driver.quit()
```

---

When you run this script:

1. The browser opens SauceDemo.
2. It enters a username and password.
3. Clicks “Login.”
4. Checks if you’re redirected to the inventory page.

---

## 🧾 Final Thoughts

Selenium WebDriver is a powerful way to test **web apps automatically**, from simple form interactions to full workflows.  
It’s a great foundation for testers who want to learn automation and build reliable end-to-end tests.