# Phase 3 - 3.1 Project Setup: The NPM Package Manager

Before we can use Cypress to automate our tests, we need to understand how to download it.

We don't download coding tools from website download buttons. We download them using the Terminal and a Package Manager!

## What is a Package Manager?
A Package Manager is an automatic tool that goes to the internet, finds the exact code library you want, downloads it, and perfectly organizes it inside your project folder. 

In the JavaScript world, the undisputed king is **NPM (Node Package Manager)**.
* When you install Node.js (which we talked about in Day 2), NPM is automatically installed on your Mac.

## Initializing a Project (`npm init`)
Every JavaScript/Automation project starts the exact same way. You must create a `package.json` file. 

This file is essentially the "Receipt" or "Instruction Manual" for your project. It keeps a strict list of every single tool your project needs to survive (like Cypress!).

### The Setup Steps:
Ready to build your first automation project? Open your Mac Terminal and let's go!

1. **Go to your Desktop:** 
   `cd Desktop`
2. **Create the Project Folder:** 
   `mkdir my-first-automation`
3. **Go inside the folder:** 
   `cd my-first-automation`
4. **Initialize NPM!** 
   `npm init -y`

*(The `-y` flag just means "Say Yes to all the default questions, don't ask me for my name and email").*

### Look what happened!
If you type `ls` in the terminal, you will see a brand new file called `package.json`. 

If you open that file in VS Code, it looks like this:
```json
{
  "name": "my-first-automation",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}
```

This is just a simple JSON Object (Lesson 1.2!) that describes your project. Right now, your project doesn't have any tools installed. 

---

**Next Step:** Let's use NPM to actually download the massive Cypress testing tool! Move to **3.2 Installation**.
