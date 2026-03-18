# Phase 2 - 2.3 Async / Await: The Modern Standard

You now know how Promises work (`.then` and `.catch`). For many years, this was the only way to handle Asynchronous code in JavaScript. 

However, if you needed to make 5 different API calls in a row (e.g., Log the user in, *then* get their profile, *then* get their friends list, *then* load the images), you ended up with a massive, ugly pyramid of `.then()` blocks.

In 2017, JavaScript released a massive upgrade: **`async` and `await`**.

## What is it?
`async / await` is literally just "Syntactic Sugar". 
*(Syntactic Sugar is a programming term meaning: "It does the exact same thing underneath, but we made the code much sweeter and easier for humans to read.")*

It allows you to write Asynchronous code that *looks* exactly like normal, top-to-bottom Synchronous code!

## How it works

### 1. The `async` Keyword
You must put the word `async` in front of your function. This warns the computer: *"Hey, this vending machine is going to do some slow network requests inside it."*

### 2. The `await` Keyword
Inside that function, you put the word `await` in front of any Promise (like a `fetch` call). 
It tells the computer: *"Pause this specific function right here. Do not go to the next line until the Promise gives us the data. But let the rest of the website keep running in the background."*

### 3. Error Handling (`try / catch`)
Instead of `.catch()`, we wrap our code in a `try / catch` block. It reads like English: *"Try to do this dangerous network stuff. If the wifi drops, catch the error so the app doesn't crash."*

```javascript
// 1. Mark the function as async
const getCatFact = async () => {
  
  try {
    // 2. We try the dangerous stuff. 
    // We AWAIT the fetch. We don't need .then() anymore!
    const response = await fetch("https://catfact.ninja/fact");
    const data = await response.json();
    
    console.log("Success:", data.fact);
    
  } catch (error) {
    // 3. This catches any network errors that happen in the 'try' block!
    console.log("The API broke!", error);
  }

};

// Call the function
getCatFact();
```

Look how clean that is! It reads exactly like normal top-to-bottom code, even though it's doing complex networking in the background.

---

## 🛠️ Practical Exposure: Try / Catch in Action

Let's use the exact code above, but intentionally break it to watch the `catch` block save the day.

1. Open your Chrome Console.
2. Copy and paste this severely broken API call:
   ```javascript
   const breakTheAPI = async () => {
     try {
       console.log("Attempting to fetch...");
       // This URL is fake and literally does not exist!
       const response = await fetch("https://this-is-a-totally-fake-website-123.com/api");
       const data = await response.json();
       console.log(data);
     } catch (error) {
       console.log("Phew! The catch block caught the error so the website didn't crash!");
       console.error(error); // This prints the error in bright red for the developer to see
     }
   };

   breakTheAPI();
   ```
3. Press Enter. 
4. You will instantly see the `Phew!` message, followed by the actual network error explaining that the fetching failed.

This `async`, `await`, `try`, `catch` pattern is the gold standard for modern Software Engineering. You will use it on almost every single project you ever build!

---

## 📺 Recommended Video Lesson

**JavaScript Async Await (Explained for Beginners)**
- An elegant video reviewing Promises, and showing exactly why Async/Await makes code so much cleaner to read. 
- [Watch on YouTube (approx 10 mins)](https://www.youtube.com/watch?v=li7FzDHYZpc) *(Note: this is the same creator as the previous video, reviewing the progression!)*

---

**Next Step:** You have mastered the most difficult concept in JavaScript! Now that we know how to fetch data from a Database seamlessly, let's learn how Databases actually store that data. 

**Go to your checklist in `engineering_transition_plan.md` to check off Phase 2: Section 2, and get ready for Databases & SQL!**
