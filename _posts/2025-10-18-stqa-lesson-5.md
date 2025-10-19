---
title: "STQA (Lesson 5) - Introduction to Unit Testing"
date: 2025-10-18 10:10:00 +0800
categories: [Software Testing, Quality Assurance]
image: /assets/img/stqa5.png
tags: [unit testing, JUnit, Pytest, Jest, AAA pattern, assertions]
excerpt: "This lesson post introduces Unit Testing, what it is, why it matters, and how frameworks like JUnit, Jest, and Pytest make it easier to write reliable and maintainable code."
---

In this lesson, we’ll explore one of the most essential testing methods used by developers, Unit Testing.  
It’s the first line of defense in ensuring your code works correctly, even before integration or system testing begins.

---

## 💡 What Is Unit Testing?

**Unit Testing** is a process where individual parts of a program (usually functions, classes, or modules) are tested in *isolation*.  
The goal is to verify that each “unit” performs exactly as expected.  
  
For example:  
If you have a function that calculates discounts, a unit test would check whether it returns the correct result for different prices and percentages without worrying about the rest of the application.  
  
In short:  
🧩 *Unit* = *smallest piece of code that can be tested independently*.

---

## 🚀 Why Is Unit Testing Important?

Unit testing might feel tedious at first, but it has some big advantages:  
1. **Catches bugs early** – Problems are found before they spread into larger parts of the system.
2. **Makes code easier to maintain** – When you modify code, you can quickly verify nothing else broke.
3. **Improves design*** – Writing tests often reveals unclear or overly complex code.
4. **Supports refactoring** – You can safely rewrite parts of the program because you know tests will catch any mistakes.
5. **Increases confidence** – Both developers and testers can trust that the core logic is working.

In short, unit tests give you peace of mind that your building blocks are solid. 

---

## 🧰 Popular Frameworks for Unit Testing
There are many tools that make writing and running unit tests easier. Here are three of the most popular across different programming languages:  
- *JUnit (Java)*  
A widely used testing framework for Java. It integrates seamlessly with IDEs like IntelliJ or Eclipse and is the foundation for many CI/CD pipelines.
- **Pytest (Python)**  
A powerful yet simple framework for Python testing. It supports fixtures, parameterization, and concise test syntax.
- **Jest (JavaScript)**  
Commonly used for testing web apps and React components. It provides fast feedback and built-in mocking utilities.

Example frameworks by language:  

| Language   | Framework | Command Example          |
| ----------- | ---------- | ------------------------ |
| Java        | JUnit      | `mvn test`               |
| Python      | Pytest     | `pytest test_example.py` |
| JavaScript  | Jest       | `npm test`               |

---

## 🧩 Structure of a Unit Test: Arrange, Act, Assert (AAA)
A good unit test usually follows the **AAA pattern** short for **Arrange**, **Act**, **Assert**.  
This helps keep tests clear and consistent.  

| Step        | Meaning                                                             | Example                             |
| ------------ | ------------------------------------------------------------------- | ----------------------------------- |
| **Arrange** | Set up everything you need for the test (data, variables, objects). | Create a new `Calculator` instance. |
| **Act**     | Perform the actual action you want to test.                         | Call `add(2, 3)`.                   |
| **Assert**  | Verify the result matches your expectations.                        | Check if the result equals `5`.     |


**🧠 Example (in Python using Pytest)**
```python
def test_addition():
    # Arrange
    a, b = 2, 3

    # Act
    result = a + b

    # Assert
    assert result == 5
```
---

## 🧾 Understanding Assertions
An assertion is how a test confirms whether a function works correctly.  
If the assertion passes, the test succeeds. If not, the test fails, giving you immediate feedback.  
  
Common examples:  
- `assert x == y` → checks if values are equal.
- `assert result is not None` → ensures a result exists.
- `assert len(items) > 0` → verifies that a list isn’t empty.  

Assertions are the *truth-checkers* of testing.  
They turn code behavior into measurable, testable outcomes.  

---

## 💡 Final Thoughts
Unit testing is where quality begins.  
By breaking your testing process into small, focused tests, you gain control over your code and reduce the risk of hidden bugs.  
And with frameworks like **JUnit**, **Pytest**, or **Jest**, testing becomes not just easy, but enjoyable.