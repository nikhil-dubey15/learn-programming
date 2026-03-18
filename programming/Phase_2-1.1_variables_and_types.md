# Phase 2 - 1.1 Variables & Types: Storing Information

Welcome to Phase 2! We are officially moving from understanding how a computer works to *telling the computer what to do*. We will be using **JavaScript (JS)**, the common language of the web.

You can write and run all of this code directly in the **Console** tab of your Browser Developer Tools, or in a simple text file!

**The Analogy: Labeled Boxes**
Imagine you are packing to move to a new house. You take an empty box, put your books inside it, and write "Books" on the side with a marker. 
A **Variable** is just a labeled box where the computer stores information so it can use it later!

## 1. Creating the Boxes (`let` and `const`)
In modern JavaScript, there are two ways to build a box.

### `const` (Constant)
* **What it means:** A box that is glued shut permanently. Once you put something in it, you can NEVER change it.
* **When to use it:** Always use this **by default**. (e.g., your birth date, or the URL of a website).
```javascript
const myName = "Nikhil";
// If I try to do myName = "John" later, the computer will throw an error!
```

### `let` (Changeable)
* **What it means:** A box with a lid you can easily open. You can put something in, take it out, and put something else in.
* **When to use it:** When you know the value will change (e.g., your age, or a score in a video game).
```javascript
let myScore = 10;
myScore = 15; // I just leveled up! The box now holds 15.
```

## 2. The Things Inside the Boxes (Data Types)
What exactly can we put inside these boxes? JavaScript has a few core "Types" of data.

1. **Strings (Text):** Absolutely anything wrapped in quotes (`""` or `''`). 
   - `const greeting = "Hello World!";`
   - `const ageText = "25";` *(Even though it's a number, because it has quotes, the computer treats it as pure text).*

2. **Numbers:** Just numbers. No quotes. You can do math with them!
   - `let myAge = 25;`
   - `let totalApples = 10 + 5;`

3. **Booleans (True/False):** A simple Yes or No. A light switch (On or Off). 
   - `const isWebsiteWorking = true;`
   - `let isUserLoggedIn = false;`

---

## 🛠️ Practical Exposure: Let's Pack Some Boxes

Let's test this in your browser!

1. Open **Google Chrome**, right-click anywhere, and click **Inspect**. 
2. Go to the **Console** tab.
3. Type the following code:
   ```javascript
   let QA_Tickets = 5;
   QA_Tickets = 6;
   console.log(QA_Tickets);
   ```
4. Press Enter. The console should print `6`. You successfully created a box, changed the number inside, and printed it!
5. Now, try testing a `const`. Type this:
   ```javascript
   const myCity = "New York";
   myCity = "London";
   ```
6. Press Enter. You will see a scary red `TypeError` because you tried to change a box that was glued shut!

---

## 📺 Recommended Video Lesson

**JavaScript Variables & Data Types for Beginners**
- A fantastic visual explanation of `let` vs `const` and how boxes hold data.
- [Watch on YouTube (approx 7 mins)](https://www.youtube.com/watch?v=HGCDMJXS1cc)

---

**Next Step:** Packing one item per box is fine, but what if you have a massive list of items? Move to **1.2 Data Structures** to learn how to organize complex data!
