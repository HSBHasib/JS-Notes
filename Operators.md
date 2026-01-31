## 3️⃣ Operators

### 🔧 What are Operators?
Operators are special symbols or keywords in JavaScript used to perform operations on values


### ➕ Arithmetic Operators
Used for basic math.

```js
  + // addition
  - // subtraction
  * // multiplication
  / // division
  % // modulus (remainder)
  ** // exponentiation (power)
```

#### Example:
```js
  let a = 10, b = 3;
  console.log(a + b); // 13
  console.log(a % b); // 1
  console.log(2 ** 3); // 8
```


### 🧮 Assignment Operators
Assign values to variables

```js
  = // assigns value
  += // a += b => a = a + b
  -= // a -= b
  *=, /=, %=
```

#### Example:
```js
  let score = 5;
  score += 2; // score = 7
```


### 🧾 Comparison Operators
Used in condition checks.
```js
  == // equal (loose)
  === // equal (strict – value + type)
  != // not equal (loose)
  !== // not equal (strict)
  >  // greater
  <  // less
  >= // greater and equal
  <= // less and equal
```

#### Example:
```js
  console.log(5 == "5"); // true
  console.log(5 === "5"); // false
```


### ✅ Logical Operators
Used to combine multiple conditions.
```js
  && // AND – both must be true
  || // OR – either one true
  ! // NOT – negates truthiness
```

#### Example:
```js
  let age = 20, name = true;
  if (age >= 18 && name) {
   console.log("Allowed");
  }
```


### 🌀 Unary Operators
Used on a single operand.
```js
 + // tries to convert to number
  - // negates
  ++ // increment
  -- // decrement
  typeof // returns data type

```

#### Example:
```js
  let x = "5";
  console.log(+x); // 5 (converted to number)
```


### ❓ Ternary Operator (Conditional)
Shorthand for if...else
```js
  condition ? valueIfTrue : valueIfFalse
```

#### Example:
```js
  let score = 80;
  let grade = score > 50 ? "Pass" : "Fail";
```


### 🔍typeof Operator
↪ Used to check the data type of a value:
```js
  typeof "hasib" // "string"
  typeof 99 // "number"
  typeof true // "boolean"
  typeof undefined // "undefined"
  typeof null // "object" → (JS bug)
  typeof [] // "object"
  typeof {} // "object"
  typeof function(){} // "function"

  // Note: typeof null === "object" is a bug, but has existed since the early days of JS.
```


### ⚡ Important Notes
```js
  • Use === instead of == to avoid type bugs.
  • Use ternary for quick decisions, not complex ones.
  • Think in truthy/falsy when using && , || , ! .
  • "5" + 1 is "51" (string concat), but "5" - 1 is 4 (number subtract)
  • !!value is a quick trick to convert anything into a boolean
  • Pre-increment ( ++i ) vs post-increment ( i++ ) return different results
```
