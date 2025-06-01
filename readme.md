#### Execution context (EC) -The environment in which javascript code is executed.it contains memory for variables/functions and code to execute.

#### Lexical environment (LE) - The environment where a function is physically written (defined) in code. it includes the function's local variable and a reference to its parent scope.

##### Scope chain: chain of Lexical Environment that js follows to find variables.
##### Call Stack: Stack that keeps track of active Execution contexts.

### Difference between let,const and var

| Feature              | `var`                                | `let`                                  | `const`                                |
|----------------------|--------------------------------------|----------------------------------------|----------------------------------------|
| Scope               | Function-scoped                      | Block-scoped                           | Block-scoped                           |
| Re-declaration      | ✅ Allowed                           | ❌ Not allowed                         | ❌ Not allowed                         |
| Re-assignment       | ✅ Allowed                           | ✅ Allowed                             | ❌ Not allowed                         |
| Hoisting            | ✅ Hoisted (Initialized as `undefined`) | ✅ Hoisted (But not initialized)      | ✅ Hoisted (But not initialized)      |
| Temporal Dead Zone  | ❌ No TDZ                            | ✅ Has TDZ                             | ✅ Has TDZ                             |
| Use Case            | Old JS (pre-ES6)                     | Modern JS (ES6+)                       | When value should not change           |

## 🧠 Heap Memory (JavaScript)

### 📌 Definition
Heap memory is an area in memory where JavaScript stores **non-primitive data types** like objects, arrays, and functions. It is used for **dynamic memory allocation**, allowing flexible and long-term storage of complex data.

---

### ⚙️ How It Works
- When an object, array, or function is created, JavaScript allocates space in the heap.
- A **reference (pointer)** to that object is stored in the stack memory.
- Multiple variables can point to the same object in the heap.
- JavaScript's **Garbage Collector** automatically removes objects from the heap when they are no longer referenced.

---

### 💡 Example
```js
let user = {
  name: "Ayush",
  age: 13
};

## 🧠 Stack Memory (JavaScript)

### 📌 Definition
Stack memory is a region in memory used by JavaScript to **store primitive values** (like numbers, strings, booleans) and references to heap objects. It follows the **LIFO (Last In, First Out)** principle and is used for managing function calls and execution contexts.

---

### ⚙️ How It Works
- Each time a function is called, a new **execution context** is pushed to the stack.
- When the function finishes execution, its context is **popped off** the stack.
- Primitive data types (`string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`) are stored **directly in the stack**.
- Stack is **fast and automatically managed**.

---

### 💡 Example
```js
let name = "Ayush";
let age = 13;
