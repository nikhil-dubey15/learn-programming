# 3-Day Engineering & Technology Transition Plan

Welcome to your transition into Engineering! Coming from a Commerce and QA background, you already have a strong foundation in understanding how applications should behave, testing APIs, and documenting workflows. This plan is designed to bridge the gap between manual QA and software engineering/QA automation over 3 intensive days (8-10 hours per day).

**Tips for Success:**
- 🕒 **Pace Yourself:** Take a 10-15 minute break every 1.5 to 2 hours. Your brain needs time to absorb technical concepts.
- 🙋‍♂️ **Leverage Your Network:** Compile a list of questions throughout the day. Consult your experienced mentors at the end of each day or whenever you are completely stuck for more than 30 minutes. 
- 🛠️ **Hands-on is Key:** Don't just read. Type out the commands in the terminal, write the code, and experiment in the browser.

---

## Phase 1: Computing Fundamentals, Networking & Essential Tools
*Focus: Understanding how computers work, how the internet operates, and getting comfortable with developer tools.*

### 1. Computer Architecture Basics (1.5 - 2 Hours)
- [x] **CPU, RAM, and Storage:** Understand the role of the CPU (Central Processing Unit) and how it executes instructions. Differentiate between RAM (Memory) and ROM/Disk (Storage).
- [x] **Memory Management:** Learn generally how the OS manages memory and what a "memory leak" is.

### 2. Command Line / Terminal Mastery (1.5 - 2 Hours)
- [x] **Navigation:** Move around directories (`cd`, `ls`, `pwd`).
- [x] **File Management:** Create, move, and remove files/directories (`mkdir`, `touch`, `cp`, `mv`, `rm`).
- [x] **File Reading:** View file contents (`cat`, `less`, `tail`) and search text (`grep`).
- [x] **Paths:** Understand relative vs. absolute file paths.

### 3. Networking, IP, and DNS (2 Hours)
- [x] **IP & Ports:** Learn what an IP Address is (IPv4 vs IPv6) and what Ports are (e.g., Port 80 for HTTP, 443 for HTTPS).
- [x] **DNS:** Understand the Domain Name System – how typing `www.google.com` resolves to an IP address.
- [x] **Protocols:** The difference between TCP (reliable) vs. UDP (fast) protocols.
- [x] **HTTP/HTTPS Lifecycle:** Deep dive into Request/Response cycles, Headers, Body payloads, and HTTP Status Codes (200s, 300s, 400s, 500s).

### 4. Git & Version Control Workflow (2 Hours)
- [x] **Git Basics:** Understand what Git is, why it's used, and local vs. remote repositories.
- [x] **Core Commands:** `git init`, `git clone`, `git status`, `git add`, `git commit`.
- [x] **Branching:** `git branch`, `git checkout` (or `git switch`), `git merge`.
- [x] **Collaborating:** Push and pull from GitHub/GitLab (`git push`, `git pull`), and the concept of Pull Requests (PRs).
- [x] **Conflicts:** Understand how merge conflicts happen and the basics of resolving them.


### 5. Browser Developer Tools (1 Hour)
- [x] **Elements:** Viewing and changing HTML/CSS on the fly.
- [x] **Console:** Running JavaScript directly in the browser and reading errors.
- [x] **Network Tab:** Inspecting API calls, viewing request/response headers, and simulating slow network speeds.
- [x] **Application Tab:** Looking at LocalStorage, SessionStorage, and Cookies.

### 6. End-of-Day Review (1 Hour)
- [x] Revisit any concepts that felt difficult.
- [x] **Meeting with Mentors:** Discuss blockers, review the day's topics, and ask them to explain how they use Git and the Terminal in their daily jobs.

---

## Phase 2: Programming Foundations (JS/TS) & Data Management
*Focus: Writing code, understanding application logic, and learning how data is stored and retrieved.*

### 1. JavaScript (JS) & TypeScript (TS) Basics (3 Hours)
- [x] **Variables & Types:** `let`, `const`, strings, numbers, booleans.
- [x] **Data Structures:** Arrays (lists) and Objects (key-value pairs / JSON manipulation).
- [x] **Control Flow:** `if/else` statements, `switch`, `for` loops, and `while` loops.
- [x] **Functions:** Declarations, arrow functions, parameters, and return statements.
- [x] **TypeScript Intro:** Understanding static typing, basic types (`string`, `number`, `boolean`), and defining `Interfaces`/`Types`.

### 2. Asynchronous Programming (1.5 Hours)
- [x] **Sync vs Async:** Understand synchronous (blocking) vs. asynchronous (non-blocking) execution.
- [x] **Promises:** Learn what a Promise is (Pending, Resolved, Rejected).
- [x] **Async/Await:** Master the modern `async` and `await` syntax for handling API calls and delays without blocking the code.

### 3. Databases & SQL (2 Hours)
- [x] **Relational vs. NoSQL:** Understand the difference between SQL (PostgreSQL/MySQL) and NoSQL (MongoDB).
- [x] **Basic SQL Queries:** `SELECT`, `INSERT`, `UPDATE`, `DELETE`, and `WHERE` clauses.
- [x] **Relations:** Primary & Foreign Keys (how tables relate to each other).
- [x] **Joins:** Understand `INNER JOIN` and `LEFT JOIN`.

### 4. Caching Concepts (1 Hour)
- [x] **Purpose:** Understand why caching is used (improving performance and reducing database load).
- [x] **Types of Cache:** Client-side (Browser) vs. Server-side caching.
- [x] **Redis:** Introduction to Redis (in-memory data structure store) and the concept of Key-Value storage.

### 5. End-of-Day Review & Practice (1.5 Hours)
- [x] **Hands-on Script:** Write a small JS/TS script run via Node.js that combines variables, loops, arrays, and an async API call (e.g., fetching a public API using `fetch`).
- [x] **Meeting with Mentors:** Review your written script together and clarify Database & Promise concepts.

---

## Phase 3: APIs, Web Architecture & QA Automation
*Focus: Pulling everything together, understanding system design, and transitioning into automated testing.*

### 1. Web Architecture & Advanced APIs (1.5 Hours)
- [ ] **Architecture:** Understand Client-Server Architecture and the separation of Frontend and Backend.
- [ ] **RESTful APIs:** Deep dive into REST principles, Resource-based URLs, and the Idempotency of PUT/DELETE.
- [ ] **GraphQL Intro:** Understand how GraphQL differs from REST (preventing over-fetching and under-fetching).

### 2. QA Automation Test Strategies (1 Hour)
- [ ] **The Test Pyramid:** Unit Tests -> Integration Tests -> E2E (End-to-End) Tests.
- [ ] **Frameworks vs. Runners:** Understand the difference between testing frameworks (e.g., Jest/Mocha) and automation tools (e.g., Selenium, Cypress, Playwright).
- [ ] **Modern Tools:** Learn why Playwright and Cypress are often preferred for modern web apps over older tools like Selenium.

### 3. Writing First Automated Tests (2.5 Hours)
- [ ] **Project Setup:** Initialize a basic Node project (`npm init -y`) in your terminal.
- [ ] **Installation:** Install an automation framework (Recommendation: **Playwright**).
- [ ] **UI Automation:** Write a test to navigate to a webpage, click a button, type text into a box, and assert that a certain element is visible.
- [ ] **API Automation:** Write an automated API test (using `axios` or Playwright's built-in API request methods) that mirrors what you already know how to do manually in Postman.

### 4. Building a Mini Project / Script (2 Hours)
- [ ] Combine UI and API tests into a single test suite in your IDE (like VS Code).
- [ ] Run the tests from the command line/terminal.
- [ ] Learn how to make the tests generate an HTML report showing passes/failures (similar to Jira/Confluence test runs).

### 5. Final Review & Next Steps with Mentors (1 Hour)
- [x] **Code Walkthrough:** Present your automation tests to your mentors.
- [x] **Review:** Ask them for an extensive code review and best practices on structuring test files.
- [x] **Next Steps:** Discuss the path forward (e.g., building a GitHub portfolio, deeper TypeScript learning, or diving into CI/CD pipelines like GitHub Actions).
