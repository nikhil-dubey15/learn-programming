# Phase 2 - 5.1 Hands-On: Your First Script

You've learned enough today to write a real program! You are going to write a script that does everything we covered: it will use Variables, Arrays, Functions, and an Asynchronous API call.

## The Goal
We are going to write a JavaScript script that fetches a list of famous Star Wars characters from a public database, loops through the Array, and prints out our favorite characters exactly how we want them formatted.

## Step 1: Set up your environment
1. On your Mac, open the **Terminal**.
2. Go to your Desktop: `cd Desktop`
3. Create a new project folder: `mkdir star_wars_script`
4. Go inside: `cd star_wars_script`
5. Create a new JavaScript file: `touch app.js`

## Step 2: Open your Code Editor
You need a place to write code. As a QA/Dev, you should download **Visual Studio Code (VS Code)**. It is free and used by almost every developer on Earth.
1. Download it from [code.visualstudio.com](https://code.visualstudio.com/) if you haven't already.
2. Open VS Code, click `File -> Open Folder` and select your `star_wars_script` folder on the Desktop.
3. Click on `app.js` to open your blank file!

## Step 3: Write the Code
Copy and paste this code into your `app.js` file. Read the comments (the text after `//`) closely to understand what every single line is doing!

```javascript
// We create an async function because we are fetching data!
const getStarWarsCharacters = async () => {
    try {
        console.log("1. Contacting the Rebel Database...");

        // We use AWAIT to pause our code until the database answers us!
        const response = await fetch("https://swapi.dev/api/people/");
        const data = await response.json(); // Convert it from raw text to a JSON Object

        // The data has an Array (List) called "results" that holds all the characters.
        // We put that list into a const variable box.
        const characterList = data.results;

        console.log("2. Data received! Analyzing characters...");
        console.log("---------------------------------------");

        // We use a FOR LOOP to go through every single character in the Array!
        for (let i = 0; i < characterList.length; i++) {
            
            // We use If/Else Control Flow!
            // If their name is exactly 'Luke Skywalker', print a special message.
            if (characterList[i].name === "Luke Skywalker") {
                console.log("⭐ THE HERO ARRIVES: " + characterList[i].name);
            } else {
                // Otherwise, just print their name and height normally!
                console.log("Found: " + characterList[i].name + " (Height: " + characterList[i].height + "cm)");
            }
        }

        console.log("---------------------------------------");
        console.log("3. Script successfully finished!");

    } catch (error) {
        // If your WiFi is off, this block will catch the error!
        console.log("ERROR: Could not reach the database.");
    }
}

// Don't forget to actually CALL the machine, or it won't run!
getStarWarsCharacters();
```

## Step 4: Run the Script!
To run JavaScript files directly on your computer without a browser, you need a program called **Node.js**. 
* If you don't have it, ask your mentors to help you install it! (It's free).

1. In VS Code, open the built-in Terminal (`Terminal -> New Terminal` at the top of the screen).
2. Type exactly this:
   ```bash
   node app.js
   ```
3. Press Enter. 
4. Watch the magic happen! You will see the computer contact the API, pause, receive the data, loop through it, single out Luke Skywalker, and print the resulting list.

**Congratulations! You just wrote a fully functional Asynchronous JavaScript program!**

---

## 📺 Recommended Video Lesson

**JavaScript Fetch API Tutorial for Beginners**
- A perfect recap video showing you how developers use the `fetch` function to grab data, just like you did above!
- [Watch on YouTube (approx 10 mins)](https://www.youtube.com/watch?v=cuEtnrL9-H0)

---

**Next Step:** It is incredibly important that you show this code to an experienced developer. Move to **5.2 Meeting with Mentors** to prepare!
