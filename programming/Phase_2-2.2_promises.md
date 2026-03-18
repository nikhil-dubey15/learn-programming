# Phase 2 - 2.2 Promises: The Restaurant Ticket

In the last lesson, we learned that Asynchronous code allows the computer to skip a slow task, keep working, and come back to the slow task later.

But how does the computer actually keep track of the slow task? It uses a **Promise**.

**The Analogy: Ordering Food**
1. You go to a busy restaurant and order a pizza. 
2. The cashier doesn't hand you a pizza immediately. Instead, they hand you a **Receipt (A Promise)**. 
3. The receipt represents a *future* pizza. You can't eat the receipt, but it is a guarantee that *eventually* you will get an answer.

## The 3 States of a Promise
While you are holding that receipt, it can only be in one of three states:

1. **Pending:** The kitchen is currently cooking. You are just standing there holding the receipt. 
2. **Resolved (Fulfilled):** The buzzer rings! The chef hands you a hot, delicious pizza. The promise was kept successfully.
3. **Rejected:** The chef comes out and says, "Sorry, we ran out of cheese." You didn't get your pizza; you got an Error instead. The promise was broken.

## How to use a Promise (`.then` and `.catch`)

When you ask JavaScript to grab data from an API (like fetching a list of users from a database), it returns a Promise. 

We have to tell the computer what to do when the buzzer finally rings!
* We use `.then()` to handle a successful pizza (Resolved).
* We use `.catch()` to handle the out-of-cheese error (Rejected).

```javascript
// Imagine 'fetchUserData()' is a function that calls a database over the internet.
// It instantly returns a Promise (The Receipt).

fetchUserData()
  .then((userData) => {
    // This code ONLY runs if the buzzer rings and the data is successfully found!
    console.log("Success! Here is the data:", userData);
  })
  .catch((error) => {
    // This code ONLY runs if the database crashed or the wifi dropped!
    console.log("Oh no, something went wrong:", error);
  });
```

### Why QA Engineers Love `.catch()`
As a QA testing APIs, you will often find that developers forgot to write `.catch()` blocks! 
If an API fails and there is no `.catch()` block to handle the error properly, the whole website might crash, or the loading spinner might spin forever! Finding these missing error handlers is a huge part of QA.

---

## 🛠️ Practical Exposure: Fetching a Real API

Let's make a real network request to a public API right now using Promises!

1. Open your Chrome Console.
2. We will use the built-in `fetch()` tool. Type this exact code to ask a free API for a random fact about cats:
   ```javascript
   fetch("https://catfact.ninja/fact")
     .then(response => response.json()) // The API gives raw text. We convert it to a JSON Object.
     .then(data => {
       console.log("SUCCESS! Got the data:");
       console.log(data.fact); // Print just the cat fact string
     })
     .catch(error => {
       console.log("FAILED! Note: The network might be down.");
     });
   ```
3. Press Enter. 
4. Look at the console! You should see a random fact about a cat printed to your screen. You just successfully used a Promise to grab data across the internet!

---

## 📺 Recommended Video Lesson

**JavaScript Promises in 100 Seconds**
- FireShip's incredibly fast breakdown of Pending, Resolved, and Rejected states.
- [Watch on YouTube (approx 2 mins)](https://www.youtube.com/watch?v=li7FzDHYZpc)

---

**Next Step:** Promises are great, but chaining a bunch of `.then()` blocks together gets really ugly to read. Modern developers created a cleaner way to write this. Move to **2.3 Async / Await**!
