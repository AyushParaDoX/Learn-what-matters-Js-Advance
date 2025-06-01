#### Execution context (EC) -The environment in which javascript code is executed.it contains memory for variables/functions and code to execute.
--------------------------------------------------------------------------
#### Lexical environment (LE) - The environment where a function is physically written (defined) in code. it includes the function's local variable and a reference to its parent scope.
---------------------------------------------------------------------------
##### Scope chain: chain of Lexical Environment that js follows to find variables.
---------------------------------------------------------------------------
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
