# JavaScript Identifier Rules

**Example File:** `Chapter_02_Java_Concepts/03_let_concepts.js`

```javascript
let myVariable = 10;       // ✅ valid — starts with letter
let _private = "secret";   // ✅ valid — starts with underscore
let $element = "div";      // ✅ valid — starts with dollar sign
let userName = "Bhumika";  // ✅ valid — camelCase convention
```

---

## What is an Identifier?

An **identifier** is a name you give to a variable, function, class, property, or label in JavaScript. Identifiers are how you refer to things in your code.

---

## The 5 Rules of JavaScript Identifiers

| # | Rule | ✅ Valid | ❌ Invalid |
|---|------|---------|-----------|
| 1 | **Must start with a letter, `_`, or `$`** | `name`, `_count`, `$root` | `1name` (starts with digit), `-value` (starts with hyphen) |
| 2 | **After the first character: letters, digits, `_`, or `$` only** | `user1`, `item_2`, `$price3` | `first-name` (hyphen not allowed), `item.name` (dot not allowed) |
| 3 | **Cannot be a reserved keyword** | `myVar`, `total`, `find` | `let`, `function`, `class`, `return`, `if` |
| 4 | **Case-sensitive** | `name` and `Name` are *two different* identifiers | `name` ≠ `Name` ≠ `NAME` |
| 5 | **No spaces allowed** | `userName`, `full_name` | `user name`, `full name` |

---

## Valid vs Invalid — Examples

| Expression | Valid? | Why |
|-----------|--------|-----|
| `firstName` | ✅ | Starts with letter, no spaces, not a keyword |
| `_tempValue` | ✅ | Starts with underscore (common for "private" vars) |
| `$` | ✅ | Yes — jQuery famously uses this |
| `$$` | ✅ | Valid (though unusual) |
| `_` | ✅ | Valid — lodash/underscore use this |
| `count1` | ✅ | Digits allowed after the first character |
| `user_name` | ✅ | Underscores are allowed (snake_case) |
| `1stPlace` | ❌ | Starts with a digit |
| `first-name` | ❌ | Hyphen `-` is not allowed (minus operator) |
| `first name` | ❌ | Space is not allowed |
| `let` | ❌ | Reserved keyword |
| `class` | ❌ | Reserved keyword |
| `return` | ❌ | Reserved keyword |
| `void` | ❌ | Reserved keyword |
| `myVar@2024` | ❌ | `@` is not allowed |

---

## Identifier vs Keyword vs Literal

| # | Aspect | 🆔 Identifier | 🔑 Keyword | 📦 Literal |
|---|--------|--------------|-----------|-----------|
| 1 | **What is it?** | A name you choose | A reserved word in the language | A fixed value written in code |
| 2 | **Created by** | You (the developer) | ECMAScript language authors | You (the developer) |
| 3 | **Examples** | `myVar`, `calculateTotal`, `User` | `let`, `function`, `if`, `return` | `10`, `"hello"`, `true`, `null` |
| 4 | **Can you change its meaning?** | ✅ Yes — assign any value | ❌ No — fixed by the language | ❌ No — a value is a value |
| 5 | **Memory?** | Points to a memory location | Does not occupy memory — it's an instruction | Occupies memory as a value |

---

## Naming Conventions (not rules, but standard practice)

| Convention | Style | Example | Used for |
|-----------|-------|---------|---------|
| **camelCase** | First letter lower, each word capitalised | `userName`, `getData`, `totalAmount` | ✅ Variables, Functions |
| **PascalCase** | Every word capitalised | `UserProfile`, `HttpClient`, `Person` | ✅ Classes, Constructors |
| **snake_case** | Words separated by underscores | `user_name`, `total_amount` | ⚠️ Rare in JS (common in Python) |
| **UPPER_SNAKE_CASE** | All caps, underscores | `MAX_SIZE`, `API_URL`, `PI` | ✅ Constants (true constants) |
| **$_prefix** | Starts with `$` or `_` | `$element`, `_privateVar` | ✅ `$` for DOM elements, `_` for "private" |

---

## How the JavaScript engine validates identifiers

```
┌──────────────────────────────────────────────────────────┐
│                     SOURCE CODE                           │
│  `let 1stPlace = 5;`                                     │
└──────────────────────┬───────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────┐
│ ① TOKENIZATION (Lexical Analysis)                       │
│   Scanner reads character by character:                   │
│     'l' 'e' 't' → Keyword token (let)                    │
│     '1' → starts token ... '1' is digit                  │
│     BUT the parser expects an Identifier after 'let'     │
│     Identifier must start with letter/_/$                │
│     '1' is a digit → ❌ INVALID                           │
└──────────────────────┬───────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────┐
│ ② PARSER THROWS SyntaxError                              │
│   "Unexpected number" or                                 │
│   "Invalid or unexpected token"                          │
│                                                          │
│   ✅ `let firstPlace = 5;`  → Parses successfully        │
│   ❌ `let 1stPlace = 5;`   → SyntaxError                 │
└──────────────────────┬───────────────────────────────────┘
                       ▼
┌──────────────────────────────────────────────────────────┐
│ ③ KEYWORD CHECK                                         │
│   Even if the identifier pattern is valid:                │
│   `let function = 5;` → passes tokenization              │
│   But 'function' is in the reserved keyword list         │
│   → ❌ SyntaxError: "Unexpected token 'function'"         │
└──────────────────────────────────────────────────────────┘
```

---

## TL;DR

- **Identifier** = a name you give to variables, functions, classes, etc.
- **5 rules:** (1) Start with letter/`_`/`$`, (2) Rest can include digits, (3) No reserved keywords, (4) Case-sensitive, (5) No spaces.
- **`_` and `$`** are valid identifier characters — libraries like lodash (`_`) and jQuery (`$`) use this.
- **Conventions** are not enforced by the engine, but the community expects them: `camelCase` for variables/functions, `PascalCase` for classes.
- If you break an identifier rule, the JavaScript engine throws a **SyntaxError** before any code runs.
