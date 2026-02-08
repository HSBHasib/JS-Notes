## 🔟 Try & Catch (Error Handling)
### 🧠 Why use Try & Catch?
• Code-e jodi kono error thake, tobe pura program bondho (crash) hoye jay. 

• Try & Catch use korle amra error-ke handle korte pari jate program-er baki part thikmoto chole.
```js
    try {
        // Code that might cause an error
    } catch (err) {
        // What to do if an error happens
    }
```

### 🏗️ Basic Usage
```js
    console.log("Start");

    try {
        console.log(a); // 'a' is not defined (Error!)
    } catch (err) {
        console.log("Error caught: Variable a thik nai!");
    }

    console.log("End"); // Code ekhono cholbe, crash korbe na.
```

---

### ⚙️ How it works
#### 🧱 The Parts
```js
    try {
        // Ekhane oi code thakbe jeta niye doubt ache (Error hote pare)
    } 
    catch (error) {
        // Jodi error hoy, tobe eita execute hobe.
        // 'error' object-er bhetore details thake (error.message)
    } 
    finally {
        // Eita shob somoy cholbe (Error hok ba na hok)
        // (Optional part)
    }
```

---

### 🧪 Quick Example with Message
```js
    try {
        let x = 10 / y; 
    } catch (error) {
        console.log("Error Message: " + error.message); 
    }

    • error.message → Exactly ki error hoyeche sheta bole dey.
```

---

### ⚡ Important Notes

```js
    • Syntax Error vs Runtime Error: Try-Catch shudhu runtime error (e.g. variable not defined) handle kore.
        Syntax-e bhul thakle eita kaj korbe na.


    • Silent Error: Catch block faka rakhle error-ta "silent" hoye jay, jeta debug kora kothin. 
        Always print the error in catch.
```