## 4️⃣ What is Control Flow?
Control flow decides which code runs, when it runs, and how many times it runs.
It's like decision-making + direction in our JavaScript program.


### 🧱 if, else if, else
```js
    if (condition) {
   // runs if condition is true
  } else if (anotherCondition) {
   // runs if first was false, second is true
  } else {
   // runs if none are true
  }
```

#### Example:
```js
    let marks = 78;
    if (marks >= 90) {
     console.log("A");
    } else if (marks >= 75) {
     console.log("B");
    } else {
     console.log("C");
    }
```


### 🌀 switch-case
Great for checking one variable against many values.
```js
  switch (value) {
   case value1:
     // code
     break;
   case value2:
     // code
     break;
   default:
     // fallback
  }
```

#### ✅ Example:
```js
  let color = "red";
  switch (color) {
   case "yellow":
     console.log("it is yellow");
   break;
   case "blue":
     console.log("it is blue");
   break;
   default:
     console.log("Unknown");
  }
```


### 🔁 Early Return Pattern
Used in functions to exit early if some condition fails.
```js
   function checkAge(age) {
     if (age < 18) return "Denied";
   return "Allowed";
  }

  // Early return method avoids deep nesting and makes logic cleaner.
```


### ⚡ Important Notes
```js
  • Control flow = conditional storytelling.
  • switch-case executes all cases after a match unless you break
  • else if chain works top-down — order matters
  • You can use truthy/falsy values directly in if
```
