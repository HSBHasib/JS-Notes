## 2️⃣ Data Types & Type System

### 📦 What Are Data Types?
In JavaScript, every value has a type.
These types define what kind of data is being stored — a number, string, boolean, object, array, etc.

#### There are two categories:
```js
  1. Primitive types – stored directly.
  2. Reference types – stored as memory references.
```

### 🔹Primitive Data Types

```js
  1. String → Text
     "hello" , 'Sheryians'

  2. Number → Any numeric value
     3 , -99 , 3.14

  3. Boolean → True or false
     true , false

  4. Undefined → Variable declared but not assigned
     let x; → x is undefined

  5. Null → Means you intentionally set it to "nothing".
     let x = null;

  6. Symbol → Unique identifier (rarely used)

  7. BigInt → Very large integers
     123456789012345678901234567890n
```
  
### 🔹Reference Data Types

```js
  • Object → { name: "Harsh", age: 26 }
  • Array → [10, 20, 30]
  • Function → function sumOfTwoValue() {}

  // These are not copied directly, but by reference.
```

###  🔁Type Coercion (Auto-Conversion)

#### ↪ JavaScript auto-converts types in some operations:

```js
  "5" + 1 // "51" → number converted to string
  "5" - 1 // 4 → string converted to number
  true + 1 // 2
  null + 1 // 1
  undefined + 1 // NaN
```

### 🚨Loose vs Strict Equality


```js
  == compares value with type conversion
  === compares value + type (no conversion)

  5 == "5" // true
  5 === "5" // false

  // Always prefer === for accurate comparisons
```

### 🧪NaN – Not a Number

```js
  typeof NaN  // "number"

  // Even though it means “Not a Number”, NaN is actually of type number, but it represents an invalid number
```

### 🔦Truthy and Falsy Values
  ```js
  • Falsy values:
    false , 0 , "" , null , undefined , NaN

  • Everything else is truthy, including:
    "0" , "false" , [] , {} , function(){}
  ```

#### Example:
```js
  if ("0") {
   console.log("Runs"); // "0" is a non-empty string = truthy
  }
```


### ⚡ Important Notes
```js
  • typeof null is "object" — this is a bug. 
  • undefined means the variable was never assigned.
  • null means you intentionally set it to "nothing".
  • '5' + 1 is "51" but '5' - 1 is 4 .
  
  • JavaScript will often auto-convert types behind the scenes.
  Always stay aware of what data type you’re working with.
```
  
