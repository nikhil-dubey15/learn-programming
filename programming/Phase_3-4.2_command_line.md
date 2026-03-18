# Phase 3 - 4.2 Command Line Execution: Headless Mode

So far, every time you ran a test, you watched Google Chrome physically pop open on your screen. You watched the mouse move and the keys type.

This is great for debugging! But what if your company has 5,000 automated tests?
If you tried to open Google Chrome 5,000 times, your laptop would catch on fire and crash. 

## The Solution: Headless Mode

"Headless Mode" means the browser is running completely invisibly in the background. It doesn't use your computer's graphics card, so it runs **insanely fast** and takes almost zero RAM.

Professionals almost always run their tests in Headless mode using the Terminal!

## Running Your Suite from the Command Line

1. Make sure your VS Code Terminal is open, and you are inside your `my-first-automation` folder.
2. Close any Cypress windows you currently have open.
3. Instead of typing `npx cypress open` (which opens the graphical UI), type this command:

```bash
npx cypress run
```

4. Press Enter.

### What happens?
Watch your terminal! 
1. Cypress will detect every single `.cy.js` file inside your `cypress/e2e` folder.
2. It will spin up an invisible, headless browser.
3. It will execute the UI test and the API test.
4. It will print a beautiful summary directly in your text terminal:

```
  ✔  Should successfully log a user in via the Graphical Interface (1200ms)
  ✔  Should successfully return user data from the Backend API (150ms)

  2 passing (1.35s)
```

Look at that speed! You tested a frontend UI and a backend Database in 1.3 seconds, and you never even saw a browser open.

## Running a Specific File
If you only want to run your combined suite, and not the other files, you can use the `--spec` flag!

```bash
npx cypress run --spec "cypress/e2e/full_login_suite.cy.js"
```

---

## 📺 Recommended Video Lesson

**Run Cypress Tests from Command Line (Headless)**
- Watch how developers use the terminal to run hundreds of tests silently in the background, ignoring the slow graphical UI.
- [Watch on YouTube (approx 8 mins)](https://www.youtube.com/watch?v=UTFh9ideHus)

---

**Next Step:** Terminal text is hard for non-engineers to read. How do we turn these results into a beautiful report we can attach to Jira? Move to **4.3 HTML Reports**!
