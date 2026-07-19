# JavaScript Keywords

**Example File:** `Chapter_02_Java_Concepts/03_let_concepts.js`

```javascript
let x = 10;   // 'let' and 'var' are keywords
function foo(){} // 'function' is a keyword
if (x > 5) {}    // 'if' is a keyword
```

---

## What is a Keyword?

A **keyword** is a reserved word in the JavaScript language that has a predefined, fixed meaning. You cannot use keywords as variable names, function names, or identifiers — they belong to the language itself.

---

| # | Aspect | 🔑 Keyword | 🆔 Identifier | 📦 Reserved Word |
|---|--------|-----------|--------------|-----------------|
| 1 | **What is it?** | A word with a built-in meaning in the language | A name you choose for variables, functions, or classes | Broad category — includes keywords + words set aside for future use |
| 2 | **Can you use it as a variable name?** | ❌ No — throws `SyntaxError` | ✅ Yes — that's the whole point | ❌ No (same restriction) |
| 3 | **Who created it?** | The ECMAScript specification authors | You (the developer) | ECMAScript spec authors |
| 4 | **Examples** | `let`, `function`, `if`, `return`, `class`, `new` | `myVar`, `userName`, `calculateTotal`, `Person` | `enum`, `implements`, `interface`, `private` |
| 5 | **When does the meaning change?** | Never — it's baked into the language | It means whatever you assign it to | Never — they can't be used either |
| 6 | **Real-world analogy** | 🚦 **Traffic light colors** — red means stop, universally | 🏪 **Store name** — you get to name your own shop | 🚫 **Empty lot** — no building allowed, maybe later |

---

## All JavaScript Keywords (ES2023+)

### Declaration & Scope
| Keyword | Purpose | Example |
|---------|---------|---------|
| `let` | Block-scoped variable declaration | `let x = 10;` |
| `const` | Block-scoped constant (can't reassign) | `const PI = 3.14;` |
| `var` | Function-scoped variable (legacy) | `var old = 1;` |
| `function` | Declare a function | `function add(a, b) { ... }` |
| `class` | Declare a class | `class Person { ... }` |
| `import` | Import modules | `import fs from 'fs';` |
| `export` | Export modules | `export const x = 1;` |

### Control Flow
| Keyword | Purpose | Example |
|---------|---------|---------|
| `if` | Conditional branch | `if (x > 0) { ... }` |
| `else` | Alternative branch | `if (x) { ... } else { ... }` |
| `switch` | Multi-way branch | `switch(val) { case 1: ... }` |
| `case` | A branch in switch | `case 1:` |
| `default` | Default case | `default: ...` |
| `for` | Loop (counter-based) | `for (let i=0; i<10; i++)` |
| `while` | Loop (condition-based) | `while (x < 10) { ... }` |
| `do` | Loop (runs at least once) | `do { ... } while (x < 10)` |
| `break` | Exit a loop/switch | `if (done) break;` |
| `continue` | Skip to next iteration | `if (skip) continue;` |
| `return` | Exit a function (with value) | `return result;` |

### Error Handling
| Keyword | Purpose | Example |
|---------|---------|---------|
| `try` | Begin a try block | `try { risky() }` |
| `catch` | Handle an error | `catch (err) { ... }` |
| `finally` | Always runs (cleanup) | `finally { cleanup() }` |
| `throw` | Throw/cause an error | `throw new Error("oops");` |

### Object & Operators
| Keyword | Purpose | Example |
|---------|---------|---------|
| `new` | Create an instance | `new Date()` |
| `this` | Current execution context | `this.name` |
| `super` | Parent class reference | `super()`, `super.method()` |
| `extends` | Inherit from a class | `class Dog extends Animal` |
| `delete` | Remove a property | `delete obj.prop` |
| `typeof` | Get the type as a string | `typeof x === "number"` |
| `instanceof` | Check prototype chain | `x instanceof Array` |
| `void` | Evaluate expression, return undefined | `void 0` |
| `in` | Check if property exists | `"key" in obj` |
| `of` | Used in for...of loop | `for (val of arr)` |

### Literals (also reserved)
| Keyword | Purpose |
|---------|---------|
| `true` | Boolean true |
| `false` | Boolean false |
| `null` | Intentional absence of value |

### Async & Generators
| Keyword | Purpose | Example |
|---------|---------|---------|
| `async` | Declare async function | `async function fetch() { ... }` |
| `await` | Wait for a Promise | `let data = await api()` |
| `yield` | Pause/resume a generator | `yield value` |

### Debugging
| Keyword | Purpose | Example |
|---------|---------|---------|
| `debugger` | Pause execution (dev tools) | `debugger;` |

### Misc
| Keyword | Purpose | Example |
|---------|---------|---------|
| `with` | Extend scope chain (❌ deprecated) | `with (obj) { ... }` |

---

## Reserved for Future Use (strict mode)

These were reserved in ES3/ES5 for potential future features. You cannot use them as identifiers in strict mode:

`implements` · `interface` · `let` (already active) · `package` · `private` · `protected` · `public` · `static` · `yield` (already active) · `enum`

---

## How the JavaScript engine processes keywords

```
┌──────────────────────────────────────────────────────────────┐
│                     SOURCE CODE                              │
│  `let x = 10;`                                              │
└──────────────────────┬───────────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────────┐
│ ① TOKENIZATION (Lexical Analysis)                           │
│   `let`    → Keyword token  (TYPE: Keyword)                  │
│   `x`      → Identifier token (TYPE: Identifier)            │
│   `=`      → Punctuator token (TYPE: Operator)               │
│   `10`     → Numeric literal  (TYPE: Literal)                │
│   `;`      → Punctuator token (TYPE: Terminator)             │
└──────────────────────┬───────────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────────┐
│ ② PARSING (AST Construction)                                │
│   Encountering a `let` keyword → expect a VariableDeclaration │
│   Encountering a `function` keyword → expect a FunctionDecl.  │
│   Encountering a `if` keyword → expect an IfStatement         │
│                                                              │
│   🚫 If you write: `let function = 5;` → SyntaxError        │
│      (Because 'function' is a keyword, not an identifier)    │
└──────────────────────┬───────────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────────┐
│ ③ EXECUTION (Bytecode → Machine Code)                       │
│   Keywords are compiled into fixed operations:                │
│   - `let` → creates a new binding in block scope             │
│   - `function` → creates a new function object               │
│   - `if` → conditional jump in the bytecode                  │
│   - `return` → pop stack frame + push return value           │
└──────────────────────────────────────────────────────────────┘
```

---

## TL;DR

- **Keyword** = a word the language reserves for itself — you can't use it as a variable name.
- **Identifier** = a name you create (variable, function, class name).
- **Reserved word** = umbrella term — includes keywords + future-reserved words like `enum`, `implements`.
- JavaScript has ~40+ keywords covering: declarations (`let`/`const`/`function`/`class`), control flow (`if`/`for`/`while`/`return`), error handling (`try`/`catch`/`throw`), object ops (`new`/`this`/`typeof`), and async (`async`/`await`/`yield`).
- **Key rule:** If you try `let function = 5;`, the engine throws `SyntaxError` — because `function` is a keyword, not an identifier.
