# Phase 3 - 3.4 API Automation: Testing the Backend

In Phase 1, you learned the HTTP Protocol (GET, POST).
In Phase 2, you learned how JavaScript uses Promises (`fetch`) to call those APIs.
In Phase 3, you learned the rules of RESTful APIs.

Now, we are going to write a tiny automated script that tests an API directly, *without* opening a UI browser at all! Remember the Testing Pyramid? API Tests (Integration) are much faster than UI Tests!

## Step 1: Create the Test File
1. In VS Code, inside the `cypress/e2e` folder, create a new file named: `my_first_api_test.cy.js`

## Step 2: Write the Test
Copy and paste this code. We are going to use Cypress to act exactly like Postman!

```javascript
describe('My First API Test', () => {

  it('Fetches a list of public users and verifies it is correct', () => {
    
    // Command 1: Call the RESTful API Endpoint (The same as hitting "Send" in Postman)
    cy.request('GET', 'https://jsonplaceholder.typicode.com/users')
      .then((response) => {
        // We received the Waiter's response! Now we write assertions.
        
        // Assertion 1: Did the server correctly return a 200 OK Status Code?
        expect(response.status).to.eq(200);

        // Assertion 2: Did the server return exactly 10 users in the Array?
        expect(response.body.length).to.eq(10);

        // Assertion 3: Is the very first user named Leanne Graham? 
        // (Remember, JS Arrays start at index 0!)
        expect(response.body[0].name).to.eq('Leanne Graham');
      });

  });

});
```

## Step 3: Run the Test!
1. Go back to your Cypress Graphical Window.
2. Click on your `my_first_api_test.cy.js` file.

Notice how the browser opens, but it's completely blank! Cypress never loaded a website. It just fired an invisible request across the internet to the database, received a JSON payload, ran 3 mathematical assertions, and colored the screen green. 

It did all of this in **less than 0.2 seconds**! 

*This* is why the Testing Pyramid tells you to write more API tests than UI tests. They are lightning-fast and never break because a button changed color!

---

## 📺 Recommended Video Lesson

**Cypress API Testing For Beginners**
- A fantastic walkthrough of how QA Engineers use Cypress to replace Postman for automated backend testing, ensuring the database is sending the right data to the frontend!
- [Watch on YouTube (approx 15 mins)](https://www.youtube.com/watch?v=zWO1-XkhaRw)

---

**Next Step:** Phenomenal! You have successfully completed Phase 3 and written your first automation code.

Look back at your `engineering_transition_plan.md` list. You have conquered all of it. Proceed to the final End-of-Day Review and Mentor check-in to wrap up your 3-Day Journey into Software Engineering!
