# **Lab Exercise: Working with ENV Variables**

## **🎯 Objectives**

This lab exercise focuses on:

- Understanding the importance of **Environment (ENV) variables**.
- Learning to use the **dotenv** package for managing these variables.
- Implementing a script that securely retrieves and utilizes ENV variables.

---

## **📚 Prerequisites**

Before starting, ensure you have:

- Basic knowledge of **JavaScript**.
- Familiarity with **terminal/command line** operations.

---

## **🚀 Steps**

### **1. Install the dotenv Package**

Install the `dotenv` package using npm to help load ENV variables from a `.env` file into your application.

Run the following command:

```bash
npm install dotenv
```

---

### **2. Create an .env File**

Create a file named `.env` in your project directory and add the following variables:

```plaintext
API_KEY=
SERVER_SECRET=
IS_KALVIAN=true
```

Fill in the values for `API_KEY` and `SERVER_SECRET` as needed.

---

### **3. Read the ENV Variables**

Write a JavaScript script to retrieve and use these variables with the **dotenv** package.

Here’s an example:

```javascript
// Load the dotenv package
require('dotenv').config();

// Access environment variables
const config = {
  apiKey: process.env.API_KEY,
  serverSecret: process.env.SERVER_SECRET,
  isKalvian: process.env.IS_KALVIAN === 'true',
};

// Export the config object
module.exports = config;

// Log the variables (Optional for testing)
console.log(config);
```

---

### **4. Run the Script**

Execute the script to verify that the environment variables are loaded and accessible.

```bash
node <your_script_name>.js
```

You should see the environment variables printed in the console if everything is set up correctly.

---

## **🏁 Outcome**

By completing this exercise, you will have:

- Created a script that securely retrieves and uses ENV variables.
- Learned the importance of **dotenv** in managing environment configurations.
- Enhanced the **security** and **flexibility** of your code by separating sensitive data from your source files.

🎉 **Congratulations!** You've successfully implemented a secure environment variable management system using the **dotenv** package.
