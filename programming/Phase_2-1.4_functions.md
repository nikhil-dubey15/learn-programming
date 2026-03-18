# Phase 2 - 1.4 Functions: Building Reusable Tools

So far, we have written code line-by-line. The computer reads from top to bottom and runs every piece of math, every logic check, and every print statement immediately.

But what if we have a piece of code that calculates the total price of a Shopping Cart (with taxes), and we want to use that exact same code 50 times throughout our website? Writing the math 50 different times would be messy and terrible if the tax rate ever changes!

**Functions** solve this problem.

**The Analogy: A Magic Vending Machine**
Imagine a vending machine. It's a heavy metal box with complex mechanics inside. You don't care how it works. 
You simply input something the machine needs (Coins), you press a button to tell it to run its internal magic (Selection), and it spits out a result (A soda).

A **Function** is literally just a Custom Vending Machine you build yourself!

## 1. Defining a Function

Here is how you build a custom tool.
* **The Name:** What is this tool called? (e.g., `calculateTotal`)
* **The Parameters (Input):** What information does this tool need to run? (e.g., The Shopping Cart items).
* **The Block (Inside Magic):** The `{}` curly braces holding the instructions.
* **The Return (Output):** What does the tool spit back out at the end? (e.g., The final dollar amount).

```javascript
// Step 1: We "declare" (build) the function
function calculateTotal(price, taxRate) {
  // Step 2: The magic inside
  let totalWithTax = price + (price * taxRate);
  
  // Step 3: Spit out the answer
  return totalWithTax;
}
```

## 2. Calling a Function

*Crucial rule:* Simply writing a function does absolutely nothing. The machine sits there silently. It does not run until you "invoke" or "call" it!

You call it by writing its name and giving it the inputs it asked for in parentheses.

```javascript
// Step 4: Use the tool!
let finalPrice1 = calculateTotal(100, 0.05); // Total is 105
let finalPrice2 = calculateTotal(50, 0.10);  // Total is 55

console.log(finalPrice1);
```

## 3. The Power of Functions (Arrow Functions)
In modern JavaScript, you will often see functions written differently. Instead of the word `function`, developers use an `=>` arrow. 
Don't be scared! It means the exact same thing, it's just a shorter way to write it.

```javascript
// This is exactly identical to the function built above!
const calculateTotal = (price, taxRate) => {
  return price + (price * taxRate);
};
```

---

## 🛠️ Practical Exposure: A Greeting Machine

Let's build a machine that takes in a user's name and spits out a personalized greeting message.

1. Open your Chrome Console.
2. Type this to build the machine:
   ```javascript
   function greetUser(firstName) {
     let message = "Welcome back, " + firstName + "! You have 3 new notifications.";
     return message;
   }
   ```
3. Press Enter. Note that absolutely nothing prints. The machine is built and waiting!
4. Call the machine:
   ```javascript
   console.log( greetUser("Nikhil") );
   ```
5. Press Enter. It prints: `Welcome back, Nikhil! You have 3 new notifications.`
6. Call it again with a different name:
   ```javascript
   console.log( greetUser("Sarah") );
   ```

---

## 📺 Recommended Video Lesson

**JavaScript Functions Explained Simply**
- A brilliant animated comparison of inputs, parameters, and arrow functions.
- [Watch on YouTube (approx 15 mins)](https://www.youtube.com/watch?v=FOD408a0EzU)

---

**Next Step:** You've mastered JS basics! But JavaScript has a dangerous flaw. Move to **1.5 Intro to TypeScript** to find out how to fix it!
