# Phase 3 - 4.1 Combine Test Suite: UI & API Together

In the previous lessons, you wrote one script that clicked buttons on a website (UI), and a separate script that pinged a database (API).

But in the real world, an Engineering team wants to run *all* of their tests together in a massive batch to ensure the whole application works. We call this a **Test Suite**.

## The Power of `describe` Blocks
Remember the `describe()` function from Jest/Cypress? Its entire purpose is to group related tests together!

Let's build a unified suite that tests the Login flow from *both* the Frontend and the Backend perspectives!

## Step 1: Create the Suite File
1. In VS Code, go to your `cypress/e2e` folder.
2. Create a new file named: `full_login_suite.cy.js`

## Step 2: Write the Unified Code
Copy and paste this code. Notice how we have one massive `describe` block that holds two separate `it` blocks!

```javascript
// This describes the entire feature we are testing
describe('Complete User Login Suite', () => {

  // Test 1: The UI Perspective
  it('Should successfully log a user in via the Graphical Interface', () => {
    
    // 1. Visit the demo site
    cy.visit('https://example.cypress.io/commands/actions');

    // 2. Type an email
    cy.get('.action-email').type('test_user@gmail.com');

    // 3. Assert it worked
    cy.get('.action-email').should('have.value', 'test_user@gmail.com');
  });

  // Test 2: The API Perspective
  it('Should successfully return user data from the Backend API', () => {
    
    // 1. Hit the REST API
    cy.request('GET', 'https://jsonplaceholder.typicode.com/users/1')
      .then((response) => {
        
        // 2. Assert the Database is online (200 OK)
        expect(response.status).to.eq(200);

        // 3. Assert it returned the correct User ID
        expect(response.body.id).to.eq(1);
      });
  });

});
```

## Step 3: Run the Suite!
1. Open the Cypress Graphical Window (`npx cypress open`).
2. Click on `full_login_suite.cy.js`.

Cypress will immediately run Test 1 (visiting the website and typing). 
The exact millisecond Test 1 finishes, it will immediately run Test 2 (pinging the API silently). 

You just proved that the Frontend *and* the Backend are both functioning correctly using a single JavaScript file!

---

**Next Step:** Opening the graphical window and manually clicking files takes too much time. Professional developers run everything through the Terminal. Move to **4.2 Command Line Execution**!
