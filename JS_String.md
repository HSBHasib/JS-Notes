## 8️⃣ JS Strings
### 🧠 What is a String?
• Strings are used to store and manipulate text. 

• Key Concept: Strings are Immutable in JS (Original string-ke change kora jay na, shudhu notun string create kora jay).

```js
    // Create a string
    let name = "Tony Stark"; 
    let msg = 'Hello World';
```

---

### ⚙️ Common String Methods
#### 🧱 Basic Modifiers (Returns a NEW string)
```js
    let str = "  JavaScript  ";

    str.trim();        // "JavaScript" (Removes spaces from start & end)
    str.toUpperCase(); // "JAVASCRIPT"
    str.toLowerCase(); // "javascript"
```

---

### 🔍 Search & Indexing
```js
    let text = "Hello Developers";

    text.indexOf("Dev");   // Output: 6 (Returns first match index)
    text.indexOf("z");     // Output: -1 (If value is not found)
    text.includes("Hi");   // Output: false (Checks if value exists)
    text.startsWith("H");  // Output: true
    text.endsWith("s");    // Output: true
```

---

### ✂️ Extractors (Cutting strings)
```js
    let code = "JavaScript";

    // slice(start, end)
    code.slice(0, 4);   // "Java" (End index is excluded)
    code.slice(4);      // "Script" (Takes everything from index 4 to end)
    code.slice(-3);     // "ipt" (Starts counting from the end)
```

---

### 🔄 Method Chaining
```js
    let msg = "  hello  ";
    let newMsg = msg.trim().toUpperCase(); // "HELLO"

    • Multiple methods can be used together in one line.
    • They execute from left to right.
```

---

### 🧪 Advanced Operations
```js
  // replace: Replaces ONLY the first match found
  "Hello World".replace("World", "JS"); // "Hello JS"

  // replaceAll: Replaces all matches
  "Lili".replaceAll("i", "a"); // "Lala"

  // repeat: Repeats the string
  "Ha ".repeat(3); // "Ha Ha Ha "

  // split: Converts string to an Array
  "a,b,c".split(","); // ["a", "b", "c"]
```
---

### ⚡ Important Notes

#### 1. Immutability 🔒
```js
  let pet = "Cat";
  pet[0] = "B"; 
  console.log(pet); // Output: "Cat" (Not "Bat"!)

  • You cannot change a specific character of a string by its index.
  • You must assign the result to a new variable or overwrite the old one.
```

#### 2. Template Literals (The Modern Way)
```js
  let user = "Bruce";
  let greet = `Welcome, ${user}! Result: ${10 + 20}`;

  • Uses backticks (``) instead of quotes.
  • Allows variables and logic inside ${ }.
  • Perfect for multi-line strings.
```
