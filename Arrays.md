## 7️⃣ Arrays

### 🧠 What is an Array?.
• An array is like a row of numbered boxes, 
where each box holds a value and has a specific position called an index (starting from 0, 1, 2…).

• Arrays allow us to store multiple values in a single variable — whether they are numbers, strings, or even complex data 
like objects and other functions.

```js
    let fruits = ["apple", "banana", "mango"];
```

---

### 🏗️ Creating & Accessing Arrays
```js
    let marks = [90, 85, 78];
    console.log(marks[1]); // 85
    marks[2] = 80;         // Update index 2


    • Indexing starts from 0
    • You can access, update, or overwrite values by index
```

---

### ⚙️ Common Array Methods
#### 🧱 Modifiers (Change original array)

| Method      | Action                          | Example            |
| ----------- | ------------------------------- | ------------------ |
| `push()`    | Add to end                      | `arr.push(5)`      |
| `pop()`     | Remove from end                 | `arr.pop()`        |
| `unshift()` | Add to start                    | `arr.unshift(0)`   |
| `shift()`   | Remove from start               | `arr.shift()`      |
| `splice()`  | Add / Remove / Replace anywhere | `arr.splice(1, 2)` |
| `reverse()` | Reverse array order             | `arr.reverse()`    |


#### 🧪 Quick Examples
```js
    let arr = [1, 2, 3];

    arr.push(4);      // [1,2,3,4]
    arr.pop();        // [1,2,3]
    
    arr.unshift(0);   // [0,1,2,3]
    arr.shift();      // [1,2,3]

    // splice(start, deleteCount, item0...itemN)
    arr.splice(1, 1); // removes 1 element from index 1 → [1,3]
    
    arr.reverse();    // [3,2,1]

```

#### 🧠 Explain in One line
```js
    • push() → “Adds element to the end of the array.”
    • pop() → “Removes last element from the array.”
    • unshift() → “Adds element at the beginning.”
    • shift() → “Removes first element of the array.”
    • splice() → “Used to add, remove, or replace elements at any position.”
    • reverse() → “Reverses the order of elements in place.”
```


###🔍 Search & Combine
```js
    let primary = ["red", "yellow", "blue", "green"];
    let secondary = ["pink", "gray", "orange"];
    

    // indexOf: Returns index of something
    primary.indexOf(yellow); // Output 1
    primary.indexOf(pink); // Output -1
    primary.indexOf(Yellow); // Output -1


    // includes: Search for a value
    primary.includes(yellow); // Output true
    primary.indexOf(pink); // Output false

    
    // concat: merge 2 arrays
    primary.concat(secondary); // output ['red', 'yellow', 'blue', 'green', 'pink', 'gray', 'orange']


    // reverse: reverse an array
    primary.reverse(); // output ['green', 'blue', 'yellow', 'red']


    // join: array elements ke ekta string banay
    let colors = ["red", "blue", "green"];
    console.log(colors.join("-")); // output "red-blue-green"
```

---

### 🔍 Extractors (Don't modify original array)
```js
    // slice: copy a portion of an array
    let newArr = arr.slice(1, 3); // Copy from index 1 to 2

    // sorts an arrya
    arr.sort(); // Lexical sort by default
```

---

### 🔄 Iteration Methods
These methods are used to loop through arrays efficiently.

| Method      | Returns      | Purpose                             |
| ----------- | ------------ | ----------------------------------- |
| `map()`     | New Array    | Transform each element              |
| `filter()`  | New Array    | Keep elements that pass a condition |
| `reduce()`  | Single Value | Accumulate array into one result    |
| `forEach()` | `undefined`  | Run function for each item          |
| `find()`    | First Match  | Returns first element that matches  |
| `some()`    | Boolean      | At least one element matches        |
| `every()`   | Boolean      | All elements must match             |


#### 🧪 Quick Examples

```js
    let nums = [1,2,3,4];
    
    // map
    nums.map(n => n * 2);             // Output - [2,4,6,8]
    
    // filter
    nums.filter(n => n % 2 === 0);     // Output - [2,4]
    
    // reduce
    nums.reduce((a,b) => a + b);       // Output - 10
    
    // forEach
    nums.forEach(n => console.log(n)); // Output - undefined
    
    // find
    nums.find(n => n > 2);   // Output - 3
    
    // some
    nums.some(n => n > 3);   // Output - true
    
    // every
    nums.every(n => n > 0);  // Output - true

```

#### 🧠 Explain in One line
```js
    • map()     → “Transforms data and returns a new array.”
    • filter()  → “Selects elements based on a condition.”
    • reduce()  → “Reduces array into a single value.”
    • forEach() → “Runs a function for each element but returns nothing.”
    • find()    → “Returns the first matching element.”
    • some()    → “Checks if any element satisfies the condition.”
    • every()   → “Checks if all elements satisfy the condition.”
```

---

### ✂️ Destructuring & Spread
```js
    let name = ["tony", "bruce", "steve", "peter"];

    // Destructuring
    let [winner, runnerup] = name;

    console.log(winner, runnerup) // Output: "tony" "bruce"

--------------------------------------------------------------------------------

    let nums = [1, 2, 3, 4];

    // Creating a new array using spread    
    let newArr = [...nums, 99];

    console.log(newArr); // [1, 2, 3, 4, 99]
    console.log(nums);   // [1, 2, 3, 4] (Original remains unchanged)
```

---

### ⚡ Important Notes
```js
    • Reference vs Value: Normal assignment arr2 = arr1 only copies the reference (memory address).
      Use [...arr1] for a real copy.

    • Lexical Sort: [10, 2, 3].sort() results in [10, 2, 3] because it converts numbers to strings.
      Use arr.sort((a, b) => a - b); for numeric sort.

    • Splice vs Slice: splice modifies the original; slice creates a new copy.

    • forEach vs map : map returns a new array
```


