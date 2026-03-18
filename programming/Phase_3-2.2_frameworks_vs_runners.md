# Phase 3 - 2.2 Frameworks vs Runners: The Testing Tools

To write automated tests in JavaScript, you need two separate pieces of software: a **Test Framework** and a **Test Runner**. 

Sometimes they are combined into one tool, and sometimes they are separate. It's important to understand the difference!

## 1. The Test Framework (The Language)
A Framework gives you the special vocabulary and commands to actually write your test. It provides functions to define what you are testing, and "Assertions" to declare what the result *should* be.

**The Vocabulary (Jest / Mocha / Jasmine):**
* `describe()`: Creates a group of tests (e.g., "The Login Page").
* `it()`: Defines a specific test (e.g., "it should show an error on bad password").
* `expect()`: The Assertion (e.g., "expect the error text to be red").

**Example of Test Framework Code:**
```javascript
describe("Math Functions", () => {
    
    it("should correctly add two numbers", () => {
        let result = 2 + 2;
        expect(result).toBe(4); // This is the Assertion!
    });

});
```

## 2. The Test Runner (The Engine)
You wrote the test above, but how does the computer actually execute it? It uses a Test Runner.

* **What it does:** It searches your entire laptop for any file that ends in `.test.js`. It runs the code inside them, catches any errors, and paints your terminal beautiful colors (Green for Pass ✅, Red for Fail ❌).
* **Examples:** Karma, Jest CLI.

## All-In-One Solutions
In modern JavaScript, the most popular tool for Unit and API Integration testing is **Jest** (created by Facebook). 
Jest is incredibly popular because it acts as BOTH the Framework (gives you the `expect` vocabulary) AND the Runner (executes the tests in the terminal). 

As a QA Automation Engineer, learning Jest vocabulary (`describe`, `it`, `expect`) is mandatory! Almost every modern tool uses this exact same syntax.

---

## 📺 Recommended Video Lesson

**Test Runners vs Frameworks vs Assertion Libraries**
- A deeper dive into the exact differences between the tools that write the test and the tools that run the test. 
- [Watch on YouTube (approx 10 mins)](https://www.youtube.com/watch?v=EKU6KC7aURg)

---

**Next Step:** Jest is great for testing APIs and Functions (The bottom of the Pyramid). But what about clicking buttons in a real browser (The top of the Pyramid)? Move to **2.3 Modern Tools (Cypress/Playwright)**!
