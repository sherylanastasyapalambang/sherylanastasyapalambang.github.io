---
title: "STQA (Lesson 8) - Introduction to Cypress"
date: 2025-10-18 20:55:00 +0800
categories: [Software Testing, Quality Assurance]
image: /assets/img/stqa8.png
tags: [cypress, end-to-end testing, javascript, saucedemo, frontend testing]
excerpt: "Discover Cypress, a modern, fast, and developer-friendly testing tool for automating frontend tests with features like live preview, time travel, and easy setup."
---

After learning Selenium for browser automation, it’s time to meet its modern cousin, **Cypress**.  
Cypress is built for **modern web apps**, offering a smooth testing experience right inside your browser.  
  
Let’s dive in 👇

---

## ⚙️ What Is Cypress?

**Cypress is a JavaScript-based end-to-end testing framework** that runs directly in the browser.  
It’s designed for **modern web apps** (especially those built with frameworks like React, Vue, or Angular).  
  
Unlike Selenium, which runs outside the browser and uses a separate driver, Cypress runs *inside the browser itself*.  
That means it sees everything your users see, making it super reliable for frontend testing.  
  
In simple terms:  
Selenium watches the browser from the outside.
Cypress *lives inside the browser*.

---

## 🚀 Why Cypress Is Different

Cypress stands out because of its **modern architecture** and developer-friendly features.
  
Here are a few things that make it special:

1. **Fast and Reliable** ⚡  
  Tests run directly in the browser without needing drivers or servers.

2. **Test Runner UI** 🧭  
  Cypress shows real-time test execution, you can watch your browser performing actions step by step.  
  
3. **Time Travel** ⏪  
  After your test runs, you can hover over each step to *see the state of the UI* at that moment.

4. **Automatic Waiting** 🕒  
  No more `sleep()`, Cypress waits automatically for elements to appear before interacting.

5. **Built-in Debugging Tools** 🪄  
  Cypress integrates perfectly with Chrome DevTools for debugging.

---

## 🧰 Installing Cypress
You’ll need Node.js installed first.  
Once ready, open your terminal and install Cypress using **npm** or **yarn**.

```bash
# Using npm
npm install cypress --save-dev

# Or using yarn
yarn add cypress --dev
```

After installation, open Cypress with:
```bash
npx cypress open
```

This command launches the Cypress Test Runner, a visual interface where you can see and run your tests live.

---

## 🧠 Anatomy of a Cypress Test
Cypress tests are written in JavaScript, and the structure is quite simple.  

A typical Cypress test file looks like this:

```javascript
describe('Login Page Tests', () => {
  it('should load the login page successfully', () => {
    cy.visit('https://www.saucedemo.com/')
    cy.contains('Login').should('exist')
  })
})
```

Let’s break that down:
- `describe()` → groups related tests together (like a test suite).
- `it()` → defines an individual test case.
- `cy` → the Cypress global object used for interacting with the browser.

---

## 💡 Common Cypress Commands
Here are some of the most used Cypress commands you’ll use almost every day:

### ⚙️ Common Cypress Commands

| Command         | Description               | Example                                      |
| --------------- | ------------------------- | -------------------------------------------- |
| `cy.visit()`    | Opens a website           | `cy.visit('https://www.saucedemo.com/')`     |
| `cy.get()`      | Finds an element          | `cy.get('#user-name')`                       |
| `cy.type()`     | Types into an input field | `cy.get('#user-name').type('standard_user')` |
| `cy.click()`    | Clicks an element         | `cy.get('#login-button').click()`            |
| `cy.contains()` | Finds text on the page    | `cy.contains('Products')`                    |
| `cy.url()`      | Checks the current URL    | `cy.url().should('include', '/inventory')`   |

---

## 🧪 Case Study: Login Test with SauceDemo

Let’s build a simple end-to-end test for [SauceDemo.com](https://www.saucedemo.com/).
  
Create a new file, e.g. `saucedemo_login.cy.js`, inside `cypress/e2e/`.
```javascript
describe('SauceDemo Login Test', () => {
  it('should login successfully with valid credentials', () => {
    cy.visit('https://www.saucedemo.com/')

    // Enter username and password
    cy.get('#user-name').type('standard_user')
    cy.get('#password').type('secret_sauce')

    // Click login
    cy.get('#login-button').click()

    // Verify successful login
    cy.url().should('include', '/inventory')
    cy.contains('Products').should('be.visible')
  })
})
```

When you run this test in Cypress, you’ll actually *see the browser typing*, *clicking*, and *checking results in real time*.

---

## 🎯 Final Thoughts
Cypress is one of the most enjoyable and intuitive tools for frontend automation testing.  
With its built-in UI, time-travel debugging, and fast execution, it makes testing web apps feel less like a chore and more like a creative process.