# Everyday_js_learning
Purpose of this learning is to choose a js topics for a day and explore deepdown into it. 

## Day_01

### Topics: Js  hoisting

#### Hoisting
JavaScript Hoisting refers to the process whereby the interpreter allocates memory for variable and function declarations prior to execution of the code. Declarations that are made using var are initialized with a default value of undefined. Declarations made using let and const are not initialized as part of hoisting.
conceptually saying,  Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.
variable declarations are processed before any code is executed.
This allows variables to appear in code before they are defined. Note however, that any variable initialization in the original code will not happen until the line of code is executed.

One of the advantages of JavaScript putting function declarations into memory before it executes any code segment is that it allows you to use a function before you declare it in your code.
- Only declarations are hoisted, JavaScript only hoists declarations, not initializations
- example

```JS
ex-1:
f1(5) // 5
function f1( num){
    console.log(num)
}
f1(5) // 5

ex-2:

// function expression are not hoisted even if it's declared with var keyword 
f2() // ReferenceError
console.log(f2)// print undefined because f2 is considered as a variable so it's declaration is hoisted with initialized value undefined

var f2 = function (){
    console.log('f2')
} p
f2()// f2


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

(Mozilla)

undeclared variables do not exist until code assigning them is executed.
Therefore, assigning a value to an undeclared variable implicitly creates it as a global variable when the assignment is executed. This means that, all undeclared variables are global variables.


interesting case: 
var name = "Baggins";

(function () {
    // Outputs: "Original name was undefined" // here name isn't in global scopes but locally scooped inside the function because it's hoisted by declaration with var keyword otherwise it's value would be Baggins
    console.log("Original name was " + name);

    var name = "Underhill";

    // Outputs: "New name is Underhill"
    console.log("New name is " + name);
})();

```

#### key words: interpreter, JavaScript engine , compiler and interpreter
1. interpreter:
 An interpreter is a program which translates code into machine code, instruction by instruction - the CPU executes each instruction before the interpreter moves on to translate the next instruction.
2. JavaScript engine:
 A JavaScript engine is a program or an interpreter which executes JavaScript code.
3. Compiler and Interpreter: 
 Interpreter translates just one statement of the program at a time into machine code. Compiler scans the entire program and translates the whole of it into machine code at once. An interpreter takes very less time to analyze the source code. ... A compiler takes a lot of time to analyze the source code.




## Day02

### Topics: Let, const, var

#### const
must initialized with a value together with declaration. Value can't be changed or reassigned. cannot redeclare.
The code block and a function body create a scope for const variables. 
you can access the const variable value only after the declaration statement.

#### let
can be declare with without initialization. new value can be assign but cannot declaRe again.
while being declared, isn’t initialized so it has an undefined.
The scope of the let variables is defined the same way as for const: by a code block or function body.
Same as with const, you cannot access a let variable before the declaration. it will show reference errors if try to access before declaration.

#### var
can be declare with without initialization. new value can be assign and also can be declaRe again.
By default, JavaScript considers uninitialized variables as having the special value undefined.
In contrast to const and let, the scope of the var variables is defined only by the function body.
can be accessed in its scope before declaration  and value Will be undefined

all variable declaration are being hoisted so a memory space is being created for it.
only variable declare with var (in outside of function , it's attached to global /window object ) are hoisted and moved  to the top of it's scope and initialized with value 'undefined' during hoisting. so unlike let nd const, it can be accessed even before declaration but with default assigned value 'undefined'.
so Variables declared with let and const remain uninitialised at the beginning of execution whilst variables declared with var are initialised with a value of undefined.
Variables declared with let and const remain uninitialised at the beginning of execution whilst variables declared with var are initialised with a value of undefined.
##### Notes:
1. scope: The concept of scope defines the limits where the variable is accessible. new value can be assign to it but can't be redeclare.
