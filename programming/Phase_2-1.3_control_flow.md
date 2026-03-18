# Phase 2 - 1.3 Control Flow: Making Decisions

A computer program is pretty stupid on its own. It only does exactly what we tell it. 

**Control Flow** is how we give the computer a brain. It's how we teach it to make decisions ("If this happens, do that") and how we tell it to repeat boring things ("Do this specific action 100 times").

## 1. The `if / else` Statement (The Fork in the Road)
* **What it is:** A logic gate. The computer checks a condition (`true` or `false`). Depending on the answer, it chooses a different path.
* **The Analogy:** A bouncer at a club. "If you are 18 or older, you can enter. Else, go home."

```javascript
let userAge = 20;

if (userAge >= 18) {
  // If the statement above is TRUE, this code runs
  console.log("Welcome to the website!");
} else {
  // If the statement is FALSE, this code runs instead
  console.log("Access Denied! You are too young.");
}
```

### The `===` Operator (Checking Equivalency)
When we check if two things are identical, we use three equal signs. 
*(Note: A single `=` is for putting things in boxes, `===` is for asking a question!)*

```javascript
let userRole = "Admin";

if (userRole === "Admin") {
  console.log("Show the secret delete button.");
}
```

## 2. Loops (The Repetitive Worker)
* **What it is:** A way to tell the computer to do the exact same thing over and over again without copying and pasting the code 100 times.
* **The Analogy:** Eating a bowl of cereal. "While the bowl is not empty, take another bite."

### The `for` Loop
This loop is perfect for Arrays (Lists). It lets us look at every single item in the list, one by one.

```javascript
const names = ["Nikhil", "John", "Sarah"];

// A basic loop that goes through the list from start to finish
for (let i = 0; i < names.length; i++) {
  console.log("Hello, " + names[i] + "!");
}
```
*(The computer looks at position 0, prints "Hello Nikhil". Looks at position 1, prints "Hello John", etc).*

---

## 🛠️ Practical Exposure: Let's check a password

Open your Chrome Console and try combining variables with an `if/else` check!

1. Type this code into the Console and press Enter:
   ```javascript
   let typedPassword = "password123";
   let correctPassword = "SuperSecretPassword";

   if (typedPassword === correctPassword) {
     console.log("Login Successful! Taking you to the dashboard.");
   } else {
     console.log("ERROR: Incorrect Password. Please try again.");
   }
   ```
2. The computer should print the ERROR message. 
3. **Change it!** Press the `Up Arrow` on your keyboard (which magically brings back the code you just typed!). Change `typedPassword` to match `"SuperSecretPassword"` and press Enter again. Watch the logic path change! 

---

## 📺 Recommended Video Lesson

**JavaScript If Else and Loops (Control Flow)**
- A fantastic visual explanation covering logical questions, greater-than/less-than signs, and the basics of repeating code.
- [Watch on YouTube (approx 12 mins)](https://www.youtube.com/watch?v=A3OPVFqqqqQ)

---

**Next Step:** Doing this manually is exhausting. How do we package up this code into a reusable "tool"? Move to **1.4 Functions**!
