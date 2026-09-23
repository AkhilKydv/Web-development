## Variables
* containers that hold data.
* They help us store, reuse, and update information in JavaScript — from simple values like
numbers to complex data like arrays and objects.
* In JavaScript, you create variables using keywords: `var` , `let` , or `const`.

### Variable declaration
#### 1.var : 
* Can be **redeclared** and **reassigned**.
* Old and risky. do not use this.
```js
var name = "john";         // assigns value "john" to the variable 'name'
console.log(name);         // logs the value of variable name as output on console/terminal
```
#### 2.let
* Can be **reassigned** but not **redeclared**
```js
let age = 40;
console.log(age);
age = 30;
console.log(age);

let age = 55;                // --> this will throw error as we are again redeclaring the age variable using let keyword
```
#### 3.const
* canot be **reassigned** and **redeclared**
```js
const marks = 90;
marks = 100;                 // --> will throw error as we cannot reassign value to a const variable
```
