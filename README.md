# 📘 JavaScript Notes

---

## 1️⃣ Variables & Declarations

### What is a Variable?

A variable is a named container to store data.

```js
let age = 20;
const country = "Bangladesh";
```

---

### var vs let vs const (🔥 Interview Favorite)

| Feature   | var       | let   | const |
| --------- | --------- | ----- | ----- |
| Scope     | Function  | Block | Block |
| Redeclare | ✅         | ❌     | ❌     |
| Reassign  | ✅         | ✅     | ❌     |
| Hoisting  | undefined | TDZ   | TDZ   |

```js
{
  var a = 1;
  let b = 2;
}
console.log(a); // 1
console.log(b); // Error
```

### ❓ TDZ মানে কী? (Interview‑এ যেভাবে বলবে)

**TDZ = Temporal Dead Zone**

👉 Simple ভাষায়:

> Variable memory তে থাকে, কিন্তু value assign না হওয়া পর্যন্ত use করা যাবে না।

```js
console.log(x); // ❌ ReferenceError
let x = 10;
```

**Interview line:**
👉 “TDZ means the time between hoisting and initialization where accessing the variable throws ReferenceError.”

---

## 2️⃣ Data Types & Type System

### Primitive Types

`string, number, boolean, undefined, null, symbol, bigint`

### Reference Types

`object, array, function`

```js
typeof null; // "object" ❌ (JS bug)
typeof [];   // "object"
```

**Interview line:**
👉 “typeof null is object due to an old JavaScript bug.”

---

## 3️⃣ Type Coercion (🔥 Very Important)

JavaScript নিজে নিজে data type convert করে — একে বলে **type coercion**

```js
"5" + 1; // "51"
```

👉 **কেন?**
`+` operator এর **২টা কাজ** আছে:

1. Addition
2. Concatenation

এখানে একটা operand string → তাই number কে string বানিয়ে concatenate করেছে

**Interview line:**
👉 “If any operand is string, + works as concatenation.”

---

```js
"5" - 1; // 4
```

👉 **কেন?**
`-` operator শুধু **numeric operation** জানে → string কে number এ convert করেছে

**Interview line:**
👉 “Minus operator forces numeric conversion.”

---

```js
true + 1; // 2
```

👉 **কেন?**
`true` → 1
`false` → 0

**Interview line:**
👉 “Boolean converts to number in arithmetic operations.”

---

## 4️⃣ == vs === (Asked Every Time)

```js
5 == "5";  // true
5 === "5"; // false
```

👉 **কেন?**

* `==` → value compare করে (type convert করে)
* `===` → value + type দুটাই compare করে

**Interview line:**
👉 “Always prefer === to avoid implicit type conversion.”

---

## 5️⃣ Truthy & Falsy

### Falsy values (Must Memorize)

`false, 0, "", null, undefined, NaN`

```js
if ("0") console.log("Runs");
```

👉 **কেন run করে?**
Non‑empty string সবসময় truthy

**Interview line:**
👉 “Only specific values are falsy; everything else is truthy.”

---

## 6️⃣ Control Flow

### Early Return (Clean Code)

```js
function check(age){
 if(age < 18) return "Denied";
 return "Allowed";
}
```

👉 **কেন ব্যবহার করি?**
Nested if কমে → code readable হয়

**Interview line:**
👉 “Early return avoids deep nesting and improves readability.”

---

## 7️⃣ Functions (🔥 High Priority)

```js
function sum(a,b){ return a+b; }
const add = (a,b) => a+b;
```

👉 Arrow function এ নিজের `this` নাই

**Interview line:**
👉 “Arrow functions do not have their own this.”

---

## 8️⃣ Closures (🔥 Very Common)

```js
function counter(){
 let c = 0;
 return function(){ c++; return c; }
}
```

👉 **কেন কাজ করে?**
Inner function outer scope এর variable মনে রাখে

**Interview line:**
👉 “Closure allows a function to remember its lexical scope.”

---

## 9️⃣ Arrays (Top Interview Topic)

```js
[10,2,3].sort();
```

❌ Output: `[10,2,3]`

👉 **কেন ভুল?**
sort() default ভাবে string হিসেবে sort করে

```js
[10,2,3].sort((a,b)=>a-b);
```

**Interview line:**
👉 “sort() needs compare function for numeric sorting.”

---

## 🔟 Objects & Reference

```js
let a = {x:1};
let b = a;
b.x = 5;
console.log(a.x); // 5
```

👉 **কেন?**
Object reference দিয়ে pass হয়

**Interview line:**
👉 “Objects are passed by reference, not by value.”

---

## 🧠 Final Interview Mindset

* const > let > var
* === always
* Explain **WHY**, not just output
* Use correct JS terms
