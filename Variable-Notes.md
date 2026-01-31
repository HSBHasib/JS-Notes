# 📘 JavaScript Notes

---

## 1️⃣ Variables & Declarations

### What is a Variable?

A variable is a named container to store data.

```js
var studentId = 101;
let age = 20;
const country = "Bangladesh";
```

---

### var vs let vs const (🔥 Important Qs for Interview)

| Feature   | var       | let   | const |
| --------- | --------- | ----- | ----- |
| Scope     | Function  | Block | Block |
| Redeclare | ✅         | ❌     | ❌     |
| Reassign  | ✅         | ✅     | ❌     |
| Hoisting  | undefined | TDZ   | TDZ   |

### Scope

```js
{
  var a = 1;
  let b = 2;
  const c = 3;
}
console.log(a); // 1
console.log(b); // Error
console.log(c); // Error
```

### Redeclare 

```js
// Declaring variables using different keywords
{
  var age = 12;
  let myId = 101;
  const name = "hasib";

  // It is called Redeclare 
  var age = 14; ✅ (Possible with var)
  let myId = 120; ❌ (Error: Already declared)
  const name = "asif" ❌ (Error: Already declared)
}
```

### Reassign

```js
// Declaring variables using different keywords
{
  var age = 12;
  let myId = 101;
  const name = "hasib";

  // It is called Reassign
  age = 14; ✅ (Possible with var)
  myId = 120; ✅ (Possible with let)
  name = "asif" ❌ (Error: Assignment to constant variable)
}
```

### Variable Hoisting in JavaScript
```js
↪ In JavaScript, when a variable is declared, the process is internally split into two distinct parts.
Declaration and Initialization/Assignment
Declaration is moved to the very top of it's scope and Initialization remains exactly where you wrote it in your code.
```

### Example:
```js
// If We Write 
{
  console.log(name); // Output: undefined
  console.log(age); // Uncaught ReferenceError: Cannot access 'age' before initialization
  console.log(pi); // Uncaught ReferenceError: Cannot access 'pi' before initialization
  
  var name = "Anis";
  let age = 25;
  const pi = 3.1416;
}
```

---

### The JavaScript engine interprets it like this:
```js
// If We Write 
{
  // For var Keyword
  1: var name = undefined;
  2:
  3: console.log(name); // Output: undefined
  4: 
  5: name = "Anis";

  // For let and const Keyword
  1: let age; (Uninitialized)
  2:
  3: console.log(age); // Uncaught ReferenceError: Cannot access 'age' before initialization
  4:
  5: age = 25;

  1: const pi; (Uninitialized)
  2:
  3: console.log(pi); // Uncaught ReferenceError: Cannot access 'pi' before initialization
  4:
  5: pi = 3.1416;

---

  // Quick Notes:

  🌐 English Version:
  ↪ For var: The JavaScript engine hoists the declaration and automatically assigns undefined as a default value.
    This is why you can access a var before its declaration without getting an error.
  
  ↪ For let and const: The engine hoists the declaration but does not assign any default value (not even undefined).
    This leaves the variable in an 'uninitialized' state until the code execution reaches its actual declaration line.
  
  
  🌐 Bangla Version:
  ↪ var: Hoisting-er shomoy var ke memory-te jayga dewar pasapashi automatic undefined diye initialize kore dewa hoy.
    Tai declare korar age access korle undefined dekhay.
  
  ↪ let & const: Erao hoist hoy, kintu tader initialization hoy na.
    Tara Temporal Dead Zone (TDZ) namer ekta obosthay thake.
    Joto khon na code-e ashol line-ta (jekhane variable declare kora hoyeche) execute hochhe, toto khon eita access kora jay     na.
    Access korle ReferenceError dey.
}
```
---

### ⏳ What is Temporal Dead Zone (TDZ)?

#### 🌐 English Version:
↪ The Temporal Dead Zone (TDZ) is the block area where a variable exists in memory (due to hoisting) but cannot be accessed. Even though the JavaScript engine is aware of the variable, it prevents any interaction with it until the execution reaches the specific line where the variable is formally declared and initialized.


#### 🌐 Bangla Version:
↪ Temporal Dead Zone hocche code-er oi totutuk area JavaScript engine jane je variable-ti memory-te exist kore (hoisting-er karone), kintu shey amader oi variable-er value access korte dey na. 
Joto khon na execution point variable-er declaration line-e pouchay, toto khon sheti ekti "locked zone"-e thake.

```js
{
  1: [TDZ starts for 'a']
  2: 
  3: console.log(a); ❌ ReferenceError (Still in TDZ)
  4:
  5:
  6: let a = 3; // Line 5: [TDZ ENDS HERE] - Initialization
  7: console.log(a); // ✅ Output: 3 (Safe to access)

  // For Variable 'a' TDZ area is fromline 1 to line 5
}
```

