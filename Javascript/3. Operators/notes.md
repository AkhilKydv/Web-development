## Operators
* Operators are special symbols or keywords in JavaScript used to perform operations on values
(operands).
* You’ll use them in calculations, comparisons, logic, assignments, and even type checks.

##  **1. Arithmetic Operators**

Used to perform mathematical operations.

| Operator | Name                | Example  | Result      |
| -------- | ------------------- | -------- | ----------- |
| `+`      | Addition            | `5 + 2`  | `7`         |
| `-`      | Subtraction         | `5 - 2`  | `3`         |
| `*`      | Multiplication      | `5 * 2`  | `10`        |
| `/`      | Division            | `5 / 2`  | `2.5`       |
| `%`      | Modulus (Remainder) | `5 % 2`  | `1`         |
| `**`     | Exponentiation      | `2 ** 3` | `8`         |
| `++`     | Increment           | `a++`    | `a = a + 1` |
| `--`     | Decrement           | `a--`    | `a = a - 1` |

---

##  **2. Assignment Operators**

Used to assign values to variables.

| Operator | Description         | Example   | Equivalent to |
| -------- | ------------------- | --------- | ------------- |
| `=`      | Assignment          | `x = 5`   | `x = 5`       |
| `+=`     | Add and assign      | `x += 2`  | `x = x + 2`   |
| `-=`     | Subtract and assign | `x -= 2`  | `x = x - 2`   |
| `*=`     | Multiply and assign | `x *= 2`  | `x = x * 2`   |
| `/=`     | Divide and assign   | `x /= 2`  | `x = x / 2`   |
| `%=`     | Modulo and assign   | `x %= 2`  | `x = x % 2`   |
| `**=`    | Exponent and assign | `x **= 2` | `x = x ** 2`  |

---

##  **3. Comparison Operators**

Used to compare two values and return a boolean.

| Operator | Description              | Example     | Result  |
| -------- | ------------------------ | ----------- | ------- |
| `==`     | Equal to (loose)         | `5 == '5'`  | `true`  |
| `===`    | Strict equal to (both type and value)        | `5 === '5'` | `false` |
| `!=`     | Not equal to (loose)     | `5 != '5'`  | `false` |
| `!==`    | Strict not equal to      | `5 !== '5'` | `true`  |
| `>`      | Greater than             | `5 > 3`     | `true`  |
| `<`      | Less than                | `5 < 3`     | `false` |
| `>=`     | Greater than or equal to | `5 >= 5`    | `true`  |
| `<=`     | Less than or equal to    | `3 <= 5`    | `true`  |

---

##  **4. Logical Operators**

Used to combine multiple conditions.

| Operator | Name | Description                 | Example                 |  
| -------- | ---- | ---------------------       | ----------------------- | 
| &&    | AND  | True if both are true       | true && false → false |  
|     |  OR  |True if at least one is true | true || false → true | 
| !     | NOT  | Inverts the value           |!true → false        |   

> or symbol - ||
---


##  **5. Ternary Operator**

Short form of if-else.

```js
condition ? exprIfTrue : exprIfFalse
```

**Example:**

```js
let age = 20;
let msg = age >= 18 ? "Adult" : "Minor";
```

---

## **6. typeof Operator**
```js
typeof 123                 // "number"
typeof "hi"                // "string"
typeof true                // "boolean"
typeof undefined           // "undefined"
typeof null                // "object" (JS bug)
typeof []                  // "object"
typeof {}                  // "object"
typeof function(){}        // "function"
```
---

## Type Coercion (Auto-Conversion)
Type coercion is the automatic or implicit conversion of values from one data type to another by the JavaScript engine. It happens behind the scenes when you perform operations on mismatched data types, forcing them to "fit" together.

###Three Forms of Coercion
JavaScript performs coercion across three primary primitive types: `Strings`, `Numbers`, and `Booleans`.

#### 1. String Coercion
Triggered primarily by the + operator. If either side of a + operation is a string, JavaScript defaults to text concatenation and coerces the non-string value into a string.

```js
let result1 = "5" + 5;     // "55" (Number 5 becomes string "5")
let result2 = "True is " + true; // "True is true" (Boolean becomes string)
```

#### 2. Number Coercion
Triggered by arithmetic operators like -, *, /, and %. These mathematical operators only work with numbers, so JavaScript coerces strings or booleans into numeric equivalents.
* Booleans convert to numbers: true becomes 1, and false becomes 0.
* Valid numeric strings convert to their actual digit, while non-numeric strings yield NaN (Not a Number).

```js
let result1 = "5" - 5;     // 0   (String "5" becomes number 5)
let result2 = true * 3;    // 3   (true becomes 1)
let result3 = "apple" - 2; // NaN (String cannot be converted to a number)
```

#### 3. Boolean Coercion
Triggered by logical contexts like if statements, ternary operators, or logical operators (&&, ||, !). JavaScript evaluates any value as either truthy or falsy.
There are only a few strictly falsy values in JavaScript:
*false
*0 and -0
*"" (empty string)
*null
*undefined
*NaN
> Everything else is truthy, including empty arrays [] and empty objects {}.

```js
if ("hello") { 
  console.log("This will run!"); // Truthy string
}

if (0) {
  console.log("This won't run."); // Falsy number
}
```
