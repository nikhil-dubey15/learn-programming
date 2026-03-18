# Phase 3 - 2.1 The Test Pyramid: What do we automate?

As a Manual QA, you are used to opening a website and clicking through the entire user journey (e.g., Logging in, searching for a product, adding it to the cart, and checking out). 

This is called **End-to-End (E2E) Testing**.

When you shift to QA Automation, your instinct will be to write a script that does that exact same E2E test. But in the engineering world, E2E tests are actually the *worst* type of test! We use the **Testing Pyramid** to decide what to automate.

## The Testing Pyramid (Bottom to Top)

### 1. The Base: Unit Tests (70% of all tests)
* **What it is:** Testing a single, tiny piece of code (usually a single Function) in complete isolation. 
* **The Analogy:** Testing a single spark plug before you stick it inside the car engine.
* **Who writes them?** The Software Developers.
* **Why are there so many?** They run incredibly fast (milliseconds) and they are extremely reliable. If a Unit Test fails, the developer knows *exactly* which line of code is broken.

### 2. The Middle: Integration Tests (20% of all tests)
* **What it is:** Testing how two different pieces of the application talk to each other (e.g., Does the API correctly talk to the Database?). 
* **The Analogy:** Plugging the spark plug into the engine and making sure the engine starts.
* **Who writes them?** Developers and QA Engineers. (Using tools like Postman or Jest).
* **Why are there fewer?** They are slower than unit tests because they require the network and a database to be running. 

### 3. The Tip: E2E / UI Tests (10% of all tests)
* **What it is:** Writing a script that opens a real Google Chrome browser and clicks buttons just like a human user. 
* **The Analogy:** Driving the fully-built car on the highway to see if it feels right. 
* **Who writes them?** QA Automation Engineers (This will be your primary job!).
* **Why are there so few?** 
  1. They are incredibly slow (takes minutes to run). 
  2. They are **Brittle** (If a developer changes the color of a button or moves it 2 pixels to the left, the whole automated test might crash, even though the website still works!).

## The QA Trap ("The Ice Cream Cone")
Junior QA Engineers often try to flip the pyramid upside down (The Ice Cream Cone anti-pattern). They write 500 massive, slow UI/Browser tests and zero fast Unit tests. 

This causes the company's deployment pipeline to take 4 hours to run, making the developers furious. As a QA Automation Engineer, you must strongly advocate for the Pyramid!

---

## 📺 Recommended Video Lesson

**The Testing Pyramid Explained**
- A great breakdown of why UI testing is too slow and fragile to rely on for everything.
- [Watch on YouTube (approx 5 mins)](https://www.youtube.com/watch?v=u6QfIXgjwGQ)

---

**Next Step:** Now that we know what to test, how do we physically write the tests? Move to **2.2 Frameworks vs. Runners**.
