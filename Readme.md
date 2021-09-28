# Everyday_js_learning
Purpose of this learning is to choose a js topics for a day and explore deepdown into it. 

## Day_01

### Topics: Js variable and hoisting

#### Hoisting
JavaScript Hoisting refers to the process whereby the interpreter allocates memory for variable and function declarations prior to execution of the code. Declarations that are made using var are initialized with a default value of undefined. Declarations made using let and const are not initialized as part of hoisting. 

This allows variables to appear in code before they are defined. Note however, that any variable initialization in the original code will not happen until the line of code is executed.

One of the advantages of JavaScript putting function declarations into memory before it executes any code segment is that it allows you to use a function before you declare it in your code.
- Only declarations are hoisted, JavaScript only hoists declarations, not initializations
- example

```JS
fn(5) // 5
function f1( num){
    console.log(num)
}

fn(5) // 5

```
```JS
console.log(num); // Returns 'undefined' from hoisted var declaration (not 5)
var num; // Declaration
num = 5; // Initialization
console.log(num);// returns '5'

console.log(b); // Throws ReferenceError exception
console.log(a); // Throws ReferenceError exception
a = 5; // Initialization
console.log(a); // 5

console.log(c) //ReferenceError
console.log(d) //ReferenceError
let c = 10
const d= 20

console.log(c,d) // 10,20
```
(Mozilla)



#### key words: interpreter, JavaScript engine , compiler and interpreter
1. interpreter:
 An interpreter is a program which translates code into machine code, instruction by instruction - the CPU executes each instruction before the interpreter moves on to translate the next instruction.
2. JavaScript engine:
 A JavaScript engine is a program or an interpreter which executes JavaScript code.
3. Compiler and Interpreter: 
 Interpreter translates just one statement of the program at a time into machine code. Compiler scans the entire program and translates the whole of it into machine code at once. An interpreter takes very less time to analyze the source code. ... A compiler takes a lot of time to analyze the source code.


