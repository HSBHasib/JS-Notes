## 6️⃣ Functions

### 🧠 What are Functions?
• Functions are blocks of reusable logic.
Instead of repeating the same task again and again, wrap it in a function and reuse it with
different inputs.

---

### 🛠️ Function Declarations
```js
    unction greet() {
     console.log("Welcome to programming world!");
    }
    greet();

    // We define it once, then call it whenever needed.
```

---

### 🧾 Parameters vs Arguments
```js
    function greet(name) {
        console.log("Hello " + name);
    }
    greet("Hasib");

    • name is a parameter
    • "Hasib" is the argument you pass

```

---

### 🌀 Return Values
• Condition is checked before running
```js
    function sum(a, b) {
        return a + b;
    }
    let total = sum(5, 10); // total is 15

    • return sends back a result to wherever the function was called
    • After return , function exits
```

---

### 🧰 Function Expressions
```js
    const greet = function () {
        console.log("Hello!");
    };

    • Functions stored in variables
    • Cannot be hoisted (We can’t call them before they’re defined)
```

---

### 🏹 Arrow Functions
```js
    const greet = () => {
        console.log("Hi!");
    }; 

    • Cleaner syntax
    • No own 'this' , no 'arguments' object
```

---

### 🧂 Default + Rest + Spread 
```js
    function multiply(a = 1, b = 1) { 
        return a * b; // a = 1, b = 1 are "Default Parameters"
    }
    console.log(multiply(5)); // Output: 5 (5 * 1)


    function sum(...nums) { // ...nums is "Rest" Parameter (Collects elements into an array)
        return nums.reduce((acc, val) => acc + val, 0);
    }


    let nums = [1, 2, 3];
    console.log(sum(...nums)); // ...nums is "Spread" Operator (Expands array into elements)



    Quick Notes:
    • Default Parameter
           Error Prevention: It ensures the function doesn't break if an argument is missing or passed as undefined.
    
    • Rest Parameter (...)
        1. Handle Unlimited Arguments: Onek gulo argument pathale proti-tar jonno alada alada parameter create korar jhamela nai.
           Ekta single parameter-ei shob store kora jay.
    
        2. Automatic Array Conversion: Eita shob individual value-ke collect kore ekta Array banaye fele,
           fole amra shorasori map, filter, ba reduce use korte pari.
    
        3. Dynamic Handling: User koita argument pathabe sheta agey theke na janleo code smoothly kaj kore.
    
    • Spread Operator (...)
        1. Real Copy (Avoiding Reference): Normal assignment (arr2 = arr1) korle shudhu reference pass hoy, 
            fole ekta change korle arekta-o change hoye jay. 
            Spread use korle ekta notun memory space-e real copy toiri hoy.
    
        2. Merging & Combining: Khub shohoje ekta Array-r bhetore arekta array dhokano ba duita object-ke merge (ekshathe) kora jay.
    
        3. Unpacking: Array-ke bhenge tar value-gulo-ke individual arguments hishebe function call-e pathano jay.
```

---

### 🎯 First-Class Functions
• JavaScript treats functions as values:
```js
    function shout(msg) {
        return msg.toUpperCase();
    }

    function processMessage(fn) {
        console.log(fn("hello"));
    }

    processMessage(shout);


    • Assign to variables
    • Pass as arguments
    • Return from other functions
```

---

### 🧠 Higher-Order Functions (HOF)
• Functions that accept other functions or return functions.
```js
    // Accept a other function 
    function multipleGreet(func, count){
        for(let i=0; i<=count; i++) {
            func();
        }
    }

    let greet = function () {
        console.log("Hello");
    }

    multipleGreet(greet, 5);


    // Return a function
    function oddEvenTest (request) {
        if(request == "odd") {
            return function (n) {
                console.log(!(n%2 === 0));
            }
        } else if (request == "even") {
            return function (n) {
                console.log(n%2 === 0);
            }
        } else {
            console.log("wrong request");
        }
    }


    // Both Condition Mixed
    function createMultiplier(x) {
        return function (y) {
            return x * y;
            };
        }
    let double = createMultiplier(2);
    console.log(double(5)); // 10
```

---

### 🔐 Closures & Lexical Scope
```js
    function outer() {
      let count = 0;
      return function () {
           count++;
           console.log(count);
         };
     };

     let counter = outer();
     counter(); // 1
     counter(); // 2

    // Even after outer is done, counter still remembers count .


    • Closures = when a function remembers its parent scope, even after the parent has finished.

    • Lexical Scope = A variable defined outside a function can be accessible
      inside another function defined after the variable declaration.
                    *** [ The opposite is NOT true ] ***


```

---

### ⚡IIFE – Immediately Invoked Function Expression
```js
    function () {
        console.log("Runs immediately");
    })();

    // Used to create private scope instantly.
```

---

🚀 Hoisting: Declarations vs Expressions
```js
    // Function Declarations
    1. 
    2. hello(); // works
    3. 
    4. function hello() {
    5.     console.log("Hi");
    6. };

    // Function Expressions
    1. 
    2. greet(); // error
    3. 
    4. const greet = function () {
    5.     console.log("Hi");
    6. };


    • Declarations are hoisted
    • Expressions are not
```

---

### 🛠️ Methods
• Actions that can be performed on an object.
```js
const calculator = {
    add: function(a, b) {
        return a + b;
    },

    sub: function(a, b) {
        return a + b;
    },

    mul: function(a, b) {
        return a + b;
    }
} 
```

---

### ⚡ Important Notes
```js
    • Arrow functions don’t have their own this
    • We can’t break out of forEach
    • Closures often trap old variable values
```

