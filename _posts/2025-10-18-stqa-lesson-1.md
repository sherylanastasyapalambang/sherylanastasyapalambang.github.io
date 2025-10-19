---
title: "STQA (Lesson 1) - Testing Strategies"
date: 2025-10-18 01:30:00 +0800
categories: [Software Testing, Quality Assurance]
image: /assets/img/stqa1.png
tags: [testing, test plan, software quality, SDLC, introduction]
excerpt: "The first lesson covers the basics of software testing from what testing is, why it's important, to how the process works from planning to reporting results."
---

In this first lesson, we’ll start with the basics, understanding what Software Testing is, why it’s so important in software development, and how the process works from start to finish.

---

## 🔍 What Is Testing?
Simply put, software testing is the process of making sure that software works as expected. The goal isn’t just to find bugs, but also to ensure that the application truly meets user needs and runs stably.

Imagine you’re creating an attendance application, and it turns out that the data isn’t being saved correctly, that’s a bug that can be detected through testing before users experience it.

---

## 🎯 Purpose and Importance of Testing
The main goals of testing are:
- To detect errors early, preventing costly issues in the production stage.
- To ensure software quality, both in terms of functionality and performance.
- To increase user trust, since a bug-free application feels more professional.
- To save repair costs, because the earlier a bug is found, the cheaper it is to fix.
Testing isn’t just a final step, it’s an essential part of the Software Development Life Cycle (SDLC). Without proper testing, an application that looks perfect can easily fail when used by real users.

---

## 🔄 Testing Life Cycle
Testing has its own life cycle, which usually includes the following steps:
1. **Test Planning**: Determining what will be tested and how it will be tested. The key documents here are the Test Plan and Test Case.
2. **Test Case Design**: At this stage, the team writes detailed testing steps: what inputs will be used, what results are expected, and what conditions are being tested.
3. **Test Execution**: Executing the test cases in a prepared environment. This can be done manually or automatically using tools such as Selenium, JUnit, or PyTest.
4. **Test Reporting**: All results are recorded both passed and failed tests in a Test Report so the team can understand the current state of the software.
5. **Result Analysis and Bug Fixing**: Once bugs are found, developers fix them, and then testers perform retesting to ensure the issues have been resolved.

---

## 🧭 Classification of Testing Strategies
Testing has many approaches depending on what is being tested and how it’s tested. Here’s the basic classification:
1. **Based on Level of Abstraction**
- **Unit Testing** → tests the smallest parts of the code (usually functions or modules).
- **Integration Testing** → ensures that modules which work individually can function properly together.
- **System Testing** → tests the entire system end-to-end.
- **Acceptance Testing** → ensures the software meets user requirements and is ready for release.

2. **Based on Functionality**
- **Functional Testing** → focuses on what the software does. Examples: login, data input, output generation.
- **Non-Functional Testing** → focuses on how the software works. Examples:
  - **Performance Testing** – how fast the application responds.
  - **Security Testing** – how secure the system is from threats.
  - **Usability Testing** – how easy it is to use.
  - **Reliability Testing** – how stable the system remains over time.

3. **Based on Structure**
- **Black Box Testing** → tests functionality without looking at the internal code. Focuses on inputs and outputs.
- **White Box Testing** → tests the internal structure of the program, such as logic, conditions, and execution paths.

4. **Based on Domain**
There are also domain-specific testing types, such as:
- Security Testing
- Performance Testing
- Usability Testing
- Compatibility Testing, and more.

---

💡 **Conclusion**

Testing isn’t just about finding bugs, it’s about building trust in the software we create. In this first week, we’ve learned that testing is a vital part of the development cycle, not just an extra step at the end of a project.