# Phase 3 - 3.2 Installation: Downloading Cypress

Now that we have our `package.json` instruction manual ready, we can tell NPM to go to the internet and fetch Cypress!

## Step 1: Install Cypress

Make sure your Terminal is still inside your `my-first-automation` folder. Run this command:

```bash
npm install cypress --save-dev
```

* **`npm install`**: "Hey NPM, go to the internet."
* **`cypress`**: "Find the folder named Cypress."
* **`--save-dev`**: "Write Cypress down in my `package.json` file, but mark it as a 'Developer Tool', because our normal customers don't need UI Testing tools downloading to their phones."

### The `node_modules` Folder (The Black Hole)
When the installation finishes, type `ls` in your terminal. You will see a new folder called `node_modules`.

**WARNING:** Never, ever open the `node_modules` folder, and never commit it to Git/GitHub! It contains thousands and thousands of complex files that Cypress needs to run. The computer manages this folder; humans ignore it.

## Step 2: Open Cypress for the first time!

Now that Cypress is downloaded, we need to turn it on. Cypress has a beautiful graphical interface. 

To run it, type this in the terminal:
```bash
npx cypress open
```
*(Note: We use `npx` when we want to execute a tool, and `npm` when we want to download a tool).*

### The Setup Wizard
1. The Cypress window will pop open on your screen!
2. Click **"E2E Testing"**.
3. Cypress will say, *"Hey, you don't have any configuration files yet. Can I make them?"* Click **Continue**.
4. Choose your favorite browser (like Chrome) and click **Start E2E Testing**.

Look closely at your VS Code screen. Cypress automatically created a `cypress` folder with sub-folders like `e2e` and `fixtures`. This is where all of your automated tests will live!

---

## 📺 Recommended Video Lesson

**Cypress Setup and Download Tutorial**
- If you get stuck at any point in the terminal, watch this developer follow the exact same steps you just took!
- [Watch on YouTube (approx 12 mins)](https://www.youtube.com/watch?v=69SFwgWHUig)

---

**Next Step:** The environment is fully set up. We are finally ready to write code that controls the browser! Move to **3.3 UI Automation**.
