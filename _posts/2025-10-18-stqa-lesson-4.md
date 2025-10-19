---
title: "STQA (Lesson 4) - Test Scenario, Test Case, and Bug Report"
date: 2025-10-18 08:45:00 +0800
categories: [Software Testing, Quality Assurance]
image: /assets/img/stqa4.png
tags: [test scenario, test case, bug report, QA documentation, software testing basics]
excerpt: "This post explores test scenarios, test cases, and bug reports,three essential elements that bring structure and clarity to the testing process."
---

After learning how to plan testing in lesson 3, it’s time to get a bit more practical.  
This lesson, we’ll dive into Test Scenarios, Test Cases, and Bug Reports, three key components that testers use every day to ensure quality and consistency in software testing.

---

## 🎯 What Is a Test Scenario?
A **Test Scenario is** a *high-level description* of what needs to be tested.  
It focuses on *what to test*, not *how to test it.*  
  
Think of it like a story of how a user would interact with the system.  
  
For example:  
**Scenario**: Verify that a user can log in using valid credentials.  

Test scenarios help testers think about real-world use cases, how users will actually use the software, rather than just focusing on code or UI.

---

## 🧪 What Is a Test Case?
A **Test Case** is a detailed set of steps that explain *how* to test a particular feature.  
Each test case includes inputs, expected results, and conditions for success or failure.  
  
In short:  
🧭 *Test Scenario* = *What to test*
🧾 *Test Case* = *How to test it*

---

## 🧱 Simple Template for Test Scenario and Test Case
Here’s a simple example you can use or adapt:  
- **🧩 Test Scenario Example:**  

| ID   | Scenario Description                            | Priority                  |
|:----:|------------------------------------------------------|:--------:|
| TS01 | Verify that a user can log in using valid credentials |   High   |



- **🧪 Test Case Example:**  

| ID   | Test Scenario ID | Test Case Description                                    | Precondition                  | Steps                                                                              | Expected Result                     | Status    |
|:----:|:----------------:|----------------------------------------------------------|-------------------------------|------------------------------------------------------------------------------------|-------------------------------------|:---------:|
| TC01 | TS01             | Verify successful login with valid username and password | User has a registered account | 1. Open login page <br> 2. Enter valid username and password <br> 3. Click “Login” | User is redirected to the dashboard | Pass/Fail |

---

## 🐞 What Is a Bug Report?
Even with great planning and testing, bugs happen, and that’s okay!  
The key is **how we report them**.  
  
A **Bug Report** is a document used to describe an issue found during testing. It helps developers reproduce and fix the problem quickly.  

A good bug report should include:  
- **Bug ID** – unique identifier.
- **Title** – short description of the problem.
- **Steps to Reproduce** – how to trigger the bug.
- **Expected Result** – what should have happened.
- **Actual Result** – what actually happened.
- **Severity/Priority** – how serious the bug is.
- **Attachments** – screenshots, logs, or videos if available.

**🐞 Bug Report Example:**  

| Field              | Description                                                                |
|:------------------:| -------------------------------------------------------------------------- |
| **Bug ID**         | BUG-101                                                                    |
| **Title**          | Login button does not respond on mobile view                               |
| **Steps to Reproduce** | 1. Open login page on mobile <br> 2. Enter credentials <br> 3. Tap “Login” |
| **Expected Result** | User should be redirected to the dashboard                                 |
| **Actual Result**  | Nothing happens when tapping the button                                    |
| **Severity**       | High                                                                       |
| **Status**         | Open                                                                       |
| **Reported By**    | Tester A                                                                   |
| **Date**           | 2025-11-08                                                                 |

---

## 💡 Final Thoughts
Test scenarios, test cases, and bug reports are the heart of the testing workflow.  
They turn chaos into clarity guiding testers through what to check, how to check it, and how to communicate what’s broken.  
  
If Lesson 3’s testing plan is the blueprint, then Lesson 4’s materials are the tools that make testing effective. 🧠🔧