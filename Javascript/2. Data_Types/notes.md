## Data Types In Javascript
* In JavaScript, every value has a type.
* These types define what kind of data is being stored — a number, text, boolean, object, etc.
There are two categories:
* **Primitive types** – stored directly.
* **Reference types** – stored as memory references.

### 1. **Primitive Types** (Immutable, stored by value)
> They hold **single values** and are **copied** when assigned or passed.
| Type        | Example                      |
| ----------- | ---------------------------- |
| `String`    | `'hello'`, `"JS"`            |
| `Number`    | `42`, `3.14`, `NaN`          |
| `Boolean`   | `true`, `false`              |
| `undefined` | declared but not assigned    |
| `null`      | intentional absence of value |
| `Symbol`    | unique value (ES6)           |
| `BigInt`    | large integers: `123n`       |

```js
let str = "Hello";
let num = 100;
let isDone = false;
let nothing = null;
let notAssigned;
let big = 123456789012345678901234567890n;
let uniqueId = Symbol("id");
```

### 2. **Reference Types** (Mutable, stored by reference)
> Objects are stored in memory and **referenced** via variables.

| Type                   | Example                     |
| ---------------------- | --------------------------- |
| `Object`               | `{ name: "John" }`          |
| `Array`                | `[1, 2, 3]`                 |
| `Function`             | `function() {}` or `()=>{}` |
| `Date`, `RegExp`, etc. | `new Date()`                |

```js
let obj = { name: "Alice" };
let arr = [1, 2, 3];
let greet = () => console.log("Hi");
```


### 📌 Key Difference: Primitive vs Reference

| Feature       | Primitive           | Reference                  |
| ------------- | ------------------- | -------------------------- |
| Stored by     | Value               | Reference (memory address) |
| Copy behavior | Copies actual value | Copies reference           |
| Mutability    | Immutable           | Mutable                    |

```js
let x = 10;
let y = x;
y = 20;
console.log(x); // 10 (unchanged)

let obj1 = { age: 25 };
let obj2 = obj1;
obj2.age = 30;
console.log(obj1.age); // 30 (changed via reference)
```
