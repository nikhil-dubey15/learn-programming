# Phase 3 - 4.3 HTML Reports: Proof of Work

You ran your tests headlessly in the terminal. The terminal said "2 passing". 

But your Product Manager doesn't know how to read a terminal! If you are attaching test results to a Jira ticket or Confluence page, you need a beautiful, readable document.

We can tell Cypress to automatically generate an **HTML Webpage Report** every time it finishes running tests!

*(This is exactly how massive companies generate their daily QA status emails).*

## Step 1: Install a Reporter Tool

We need to download a specialized plugin that knows how to turn raw test data into pretty colors. 
The industry standard for Cypress is called **Mochawesome**.

1. Open your VS Code Terminal.
2. Tell NPM to go fetch the tool:
   ```bash
   npm install --save-dev cypress-mochawesome-reporter
   ```

## Step 2: Configure Cypress

We need to edit the "Instruction Manual" of Cypress so it knows to use the new tool.

1. Look in your main project folder for a file named `cypress.config.js`. Open it.
2. Replace everything inside with this code:
```javascript
const { defineConfig } = require("cypress");

module.exports = defineConfig({
  reporter: 'cypress-mochawesome-reporter', // Tell Cypress to use the tool!
  e2e: {
    setupNodeEvents(on, config) {
      require('cypress-mochawesome-reporter/plugin')(on); 
    },
  },
});
```

3. Almost done! Open `cypress/support/e2e.js` and paste this exactly at the top of the file:
```javascript
import 'cypress-mochawesome-reporter/register';
```

## Step 3: Run the Tests and Generate the Report!

Now, simply run your headless command again:

```bash
npx cypress run
```

### The Magic Result
When the tests finish, look at your VS Code file explorer on the left.
A brand new folder magically appeared called **`cypress/reports/html`**.

Inside that folder is a file named `index.html`. 
1. Right-click `index.html`
2. Select "Reveal in Finder" (Mac)
3. Double click the file to open it in Google Chrome!

You will see a gorgeous dashboard showing exactly how many tests passed, how long they took, and pie charts of the success rate! You can save this HTML file and attach it directly to Jira for your manager!

---

## 📺 Recommended Video Lesson

**Generate HTML Reports in Cypress (Mochawesome)**
- A step-by-step video of the exact installation we just did, ending with a view of the beautiful HTML dashboard pie charts!
- [Watch on YouTube (approx 10 mins)](https://www.youtube.com/watch?v=PEA42oMnjks)

---

**Next Step:** Incredible work. You have built a fully functional QA Automation pipeline from scratch. 

**Go to your checklist in `engineering_transition_plan.md` to check off Phase 3: Sections 3 and 4.** 

We only have the final Phase 3 Wrap-Up remaining!
