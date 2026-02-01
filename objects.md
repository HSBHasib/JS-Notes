## 7️⃣ Objects Literals

### 🧠 What is an Objects Literals?.
  • Objects are a collection of properties

  • Used to store keyed collections & complex entities.
```js
    // Create a object
    let student = {
        name: "hasib",
        age: 20,
        isEnrolled: true
    };
```

### 🧪 Get Values
```js
    let student = {
        name: "hasib",
        marks: 94.4  
    }

    // Access object value
    student["name"] // dot notation
    student.name    // bracket notation

    // Dot for fixed keys, bracket for dynamic keys.
```

### 🧱 Add / Update Value
```js
    let student = {
        name: "hasib",
        age: 20,
        isEnrolled: true 
    }

    student.name = "adib";     // 'Update' the name to "adib"
    student.gender = "male";   // 'Add' new property "gender"

    delete student.gender;     // 'Delete' gender property from object.
```

---

### 🔑 Key-Value Structure
  • JS automatically coverts objects keys to strings. (even if we made the number as a key, the number will be converted to string.) 
   
  • Values can be anything – string, number, array, object, function, etc.
```js
  const obj = {    // ✅
    1: "a",
    2: "b",
    true: "c",
    null: "d",
    undefined: "e",
  }

  console.log(obj["1"]);     // "a"
  console.log(obj["true"]);  // "b"
```

---

### 📍 Dot vs Bracket Notation
  • Use dot notation for fixed key names
   
  • Use bracket notation for dynamic or multi-word keys
```js
    student["full name"] = "hasibur rahman"; // ✅
    student.course = "JavaScript";           // ✅

    • Space / dynamic key → bracket
    • Normal key → dot
```

---

### 🏗️ Nested Objects and Deep Access
  • Objects can have nested objects (objects inside objects)
```js
    let user = {
        name: "Amit",
        address: {
            city: "Dhaka",
            pincode: 1010
        }
    };

    // Access the city value
    console.log(user.address.city); // dhaka
```

---

### ✂️ Array of Object
```js
    // Sorting infomation od multiple students
    const classInfo = [
        {
            name: "hasib",
            age: 20,
            city: Uttara
        },

        {
            name: "adib",
            age: 21,
            city: "Mirpur"
        },

        {
            name: "samia",
            age: 19,
            city: "Banani"
        }
    ];

    // Access the second index student name
    console.log(classInfo[1].name); // output 'adib' 
```

---

### ✂️ Object Destructuring
  • You can extract values directly:
```js
    let { name, age } = student;
```

  • For nested objects:
```js
    let {
        address: { city }
    } = user;
```

---

### 🔁 Looping Through Objects
  • for-in Loop
```js
    for (let key in student) {
        console.log(key, student[key]);
    }
```

#### Object.keys(), Object.values(), Object.entries()
```js
    Object.keys(student); // keys : output - ["name", "age", "isEnrolled"]
    Object.values(student); // values : output - hasib, 20, true
    Object.entries(student); // key-value : output - [["name", "hasib"], ["age", 20], ...]
```

---

### 📦 Copying Objects
#### • Shallow Copy (one level deep)
```js
    let newStudent = { ...student };
    let newOne = Object.assign({}, student);
```

#### • Deep Copy (nested levels)
```js

    let deepCopy = JSON.parse(JSON.stringify(user));
 
```
#### ❗ Note: JSON-based copy works only for plain data (no functions, undefined, etc.)

---

### ❓ Optional Chaining
  • Avoids errors if a nested property is undefined:
```js
    console.log(user?.address?.city);  // dhaka
    console.log(user?.profile?.email); // undefined (no error)
```

---

### 🧠 Computed Properties
  • We can use variables as keys:
```js
    let key = "marks";
    let report = {
        [key]: 89
    };

    // Computed properties allow dynamic keys.
```

---

### ⚡ Important Notes
```js
  • Objects are reference types (copied by reference, not value)
  • Spread operator ( ... ) creates shallow copy, not deep copy
  • Nested objects still share the same reference
  • Shallow copy copies only the first level
  • for-in includes inherited keys (be cautious!)
  • delete obj.key removes the property
  • Spread ≠ deep copy
  • for-in loop includes inherited enumerable keys (use carefully)
  • Object.keys / values / entries return arrays
  • Optional chaining (?.) prevents runtime errors
  • JSON.stringify deep copy works only for plain data (no function, undefined)
```
