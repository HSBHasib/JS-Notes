## 5️⃣ Loops

### 🔄 Why Loops?
Loops help us repeat code efficiently without rewriting it. 
If a task needs to be performed multiple times, loops automate the process, making the code cleaner and more maintainable.


### 🔄 for Loop
```js
    for(initialization; condition; updation) {
        // do something
    };

    //Example:
    for (let i = 0; i < 5; i++) {
        console.log(i);
    }

    • Start from i = 0
    • Run till i < 5
    • Increase i each time
```

### 🌀 Nested for Loop
```js
    let arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    for(let i=0; i<arr.length; i++) {
        for(let j=i; j<arr.length; j++) {
            console.log(j);
        }    
    }
```


### 🔄 while Loop
• Condition is checked before running
```js
    initialization
    while (condition) {
        // do something
    };

    //Example:
    let i = 0;
    while (i < 5) {
        console.log(i);
        i++;
    }

```


### 🔄 do-while Loop
• Runs at least once, even if condition is false
```js
    initialization
    do {
        // do something
    }
    while (condition); 

    let i = 0;
    do {
     console.log(i);
     i++;
    } while (i < 5);

```


### ⛔ break and continue
```js
    • break : Exit loop completely

    //Example
    for (let i = 1; i <= 5; i++) {
        if (i === 3) break; // exits from the loop.
    }
    console.log("I am out"); // 


    • continue : Skip current iteration and move to next

    //Example
    for (let i = 1; i <= 5; i++) {
        if (i === 3) continue;
        console.log(i); // Skips 3
    }
```

### 🌀 for-of Loop 
• Generally used to iterate over Arrays and Strings.
```js
    for (element of collection) {
        // do something
        // code to be executed on each value
    }

    let fruits = ["mango", "apple", "banana", "orange"];
    for(let fruit of fruits) {
        console.log(fruit);
    }
    
    for (let char of "hasib") {
        console.log(char);
    }
```

### 🌀 Nested for-of Loop
```js
    let heros = [["ironman", "spiderman"], ["thor", "superman"]];
    for(let listOfHero of heros) {
        for(let hero of listOfHero) {
            console.log(hero);
        }
    }
```


### 🧱 forEach Loop 
• Generally use in Arrays
```js
    let nums = [10, 20, 30];
    nums.forEach((num) => {
        console.log(num);
    });

    // forEach is cleaner than the traditional 'for loop' for arrays,
    // but it has a limitation: we cannot use break or continue.
```


### 🧱 for-in Loop
• Generally we use in Objects (and arrays if needed)
```js
    let user = { name: "Hasib", age: 20 };
    for (let key in user) {
     console.log(key, user[key]);
    }
```


### ⚡ Important Notes

```js
    • for-in is for objects, not arrays (may cause issues with unexpected keys)
    • forEach can't use break or continue
    • while and do-while work best when number of iterations is unknown
    • You can use truthy/falsy values directly in if
```

• Use the right loop for the job:
| Loop Type  | Characteristic                         | Best For                     |
| ---------- | -------------------------------------- | ---------------------------- |
| `for`      | Initialization → Condition → Update    | Known number of iterations   |
| `while`    | Condition checked **before** execution | Unknown number of iterations |
| `do-while` | Condition checked **after** execution  | Must run at least once       |
| `for-of`   | Iterates over **values**               | Arrays & Strings             |
| `for-in`   | Iterates over **keys / properties**    | Objects                      |