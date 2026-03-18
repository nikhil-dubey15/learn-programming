# Phase 3 - 3.3 UI Automation: Controlling the Browser

You have Cypress open. It's time to write your very first automated E2E Script! 

We are going to tell Cypress to navigate to a real website, find an input box, type something into it, and verify the result.

## Step 1: Create the Test File
1. In VS Code, open the newly generated `cypress` folder.
2. Open the `e2e` folder.
3. Inside the `e2e` folder, create a new file named: `my_first_test.cy.js`

## Step 2: Write the Test
Copy and paste this code into your file. Notice that it uses the `describe` and `it` framework vocabulary we learned about!

```javascript
describe('My First UI Test', () => {

  it('Visits the Kitchen Sink website and checks a button', () => {
    
    // Command 1: Go to the website
    cy.visit('https://example.cypress.io');

    // Command 2: Find a specific piece of text on the screen and click it
    cy.contains('type').click();

    // Assertion 1: We clicked 'type', so the URL should have changed!
    cy.url().should('include', '/commands/actions');

    // Command 3: Find the email input box (using a CSS class), and type into it
    cy.get('.action-email').type('nikhil@fake-email.com');

    // Assertion 2: Verify that the text we typed actually stayed in the box
    cy.get('.action-email').should('have.value', 'nikhil@fake-email.com');

  });

});
```

## Step 3: Run the Test!
1. Go back to the Cypress Graphical Window that you left open (`npx cypress open`).
2. Click on your `my_first_test.cy.js` file in the list.
3. **Take your hands off the keyboard!**

You will literally watch Chrome open by itself, zoom to the website, click the button, type your email, and verify the assertions. It happens in less than 2 seconds!

When it finishes, look at the left side of the Cypress runner. You will see beautiful green checkmarks (`✅ ASSERT`) proving that your UI test passed successfully.

### The Time Travel Feature
Hover your mouse over the commands on the left side of the Cypress runner (like the `Click` or `Type` steps). You will see the website on the right physically rewind in time to show you *exactly* what the browser looked like at that exact millisecond. 
This makes debugging failing tests incredibly easy for QA Engineers!

---

## 📺 Recommended Video Lesson

**Write Your First Cypress Test**
- Watch a developer write this exact code and explain how Cypress finds elements on the screen.
- [Watch on YouTube (approx 15 mins)](https://www.youtube.com/watch?v=7CYgItuHq5M)

---

**Next Step:** UI Testing is fun, but what about API Testing? In Phase 3 - Section 1 we learned that the Backend API is faster and more reliable than the UI. Let's automate that too! Move to **3.4 API Automation**.
