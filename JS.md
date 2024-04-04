## JS

# #**Commonly asked JavaScript Interview Questions:**

## *****1. What are the different data types present in javascript?**

JavaScript data types can be broadly categorized into primitive and non-primitive (also known as reference) types.

**Primitive Data Types:**

1. **Number**: Represents numeric values, such as integers or floating-point numbers. For example: **`5`**, **`3.14`**.
2. **String**: Represents text enclosed within single ('') or double ("") quotes. For example: **`"Hello, world!"`**, **`'JavaScript is fun!'`**.
3. **Boolean**: Represents a logical value, either **`true`** or **`false`**, used for logical operations and conditions.
4. **Undefined**: Represents **a variable that has been declared but has not been assigned a value yet.** When you declare a variable without assigning a value to it, it's automatically assigned the value **`undefined`**.
5. **Null**: Represents the intentional **absence of any value**. It's often used to explicitly indicate that a variable does not have a value.

Primitive data types are immutable, meaning their values cannot be changed. When you assign a new value to a variable holding a primitive data type, it creates a new value in memory.

**Non-Primitive (Reference) Data Types:**

1. **Object**: Represents a collection of key-value pairs, where keys are strings (or symbols in ES6+) and values can be of any data type, including other objects. Objects are used to store complex data structures.
2. **Array**: Represents an ordered list of elements, where each element can be of any data type. Arrays are used to store collections of similar or related items.

Non-primitive data types are mutable, meaning their values can be changed. When you assign a non-primitive value to a variable, it actually holds a reference (memory address) to the location where the value is stored in memory. Therefore, if you change the value, all references to that value will reflect the change.

## *****2. Explain Hoisting in javascript.**

Hoisting in JavaScript is a behavior where variable and function declarations are moved to the top of their containing scope during the compilation phase. This means that you can use variables and functions before they are declared in your code without raising an error.

it's important to note that only the declarations are hoisted, not the initializations:

hello(); // Outputs: "Hello, world!"

function hello() {
console.log("Hello, world!");
}

console.log(x); // Outputs: undefined
var x = 5;

## *****3. Difference between [“==” and “===”](https://www.geeksforgeeks.org/difference-between-and-operator-in-javascript/) ?**

” ==” only compares values “===” compare values and type both.

5 == "5" // true

5 === "5" // false

## ***4. Difference between var, let and const keyword in javascript ?

1. **`var`:**
    - **`var`** declarations are globally scoped.
    - They are hoisted to the top of their containing function or global scope.
    - **`var`** variables can be re-declared and updated.
    - Example:
        
        ```jsx
        javascriptCopy code
        var x = 5;
        var x = 10; // Redeclaration allowed
        x = 15;     // Value can be updated
        
        ```
        
2. **`let`:**
    - **`let`** declarations are block-scoped.
    - They are not hoisted to the top of the block.
    - **`let`** variables can be updated but not re-declared within the same scope.
    - Example:
        
        ```jsx
        javascriptCopy code
        let y = 5;
        y = 10;     // Value can be updated
        let y = 15; // Error: Identifier 'y' has already been declared
        
        ```
        
3. **`const`:**
    - **`const`** declarations are block-scoped.
    - They are not hoisted to the top of the block.
    - **`const`** variables must be initialized with a value and cannot be reassigned.
    - Example:
        
        ```jsx
        javascriptCopy code
        const z = 5;
        z = 10;     // Error: Assignment to constant variable
        const z = 15; // Error: Identifier 'z' has already been declared
        
        ```
        

## *****5. Explain passed by value and passed by reference.**

**Passed by Value:**

- When a value is passed by value, a copy of the value is passed to a function or assigned to a variable.
- Modifying the value inside the function or variable does not affect the original value.
- Example:
    
    ```jsx
    
    let x = 5;
    
    function increment(num) {
      num++; // Increment num
      return num;
    }
    
    console.log(increment(x)); // Output: 6
    console.log(x); // Output: 5 (original value remains unchanged)
    ```
    

**Passed by Reference:**

- When a value is passed by reference, a reference to the original value is passed to a function or assigned to a variable.
- Modifying the value inside the function or variable affects the original value.
- Example:
    
    ```jsx
    
    let obj = { value: 5 };
    
    function increment(objRef) {
      objRef.value++; // Increment value property of objRef
      return objRef;
    }
    
    console.log(increment(obj)); // Output: { value: 6 }
    console.log(obj); // Output: { value: 6 } (original object is modified)
    ```
    

In summary:

- Passed by value means working with a copy of the value, so modifications inside a function or variable do not affect the original.
- Passed by reference means working directly with the original value, so modifications inside a function or variable affect the original.

## *** 6. **What is an Immediately Invoked Function in JavaScript?**

An Immediately Invoked Function Expression (IIFE) in JavaScript is a function that is executed immediately after it's defined. IIFEs are often used to encapsulate code, avoid naming conflicts and define and execute a piece of code . 

```jsx

(function() {
  // Code inside this function is executed immediately
  console.log("This is an IIFE");
})();
```

## ***** 7. Explain Higher Order Functions in javascript.**

Higher-order functions in JavaScript are functions that can accept other functions as arguments and/or return functions as output. 

1. **Accepting Functions as Arguments**:
    - A higher-order function can take another function as an argument.
    - It allows you to pass behavior as data.
    - Example:
        
        ```jsx
        
        function applyOperation(operation, x, y) {
          return operation(x, y);
        }
        
        function add(a, b) {
          return a + b;
        }
        
        function subtract(a, b) {
          return a - b;
        }
        
        console.log(applyOperation(add, 5, 3)); // Output: 8
        console.log(applyOperation(subtract, 5, 3)); // Output: 2
        ```
        
2. **Returning Functions**:
    - A higher-order function can also return another function.
    - It allows you to create functions on the fly based on certain conditions or parameters.
    - Example:
        
        ```jsx
        
        function createMultiplier(factor) {
          return function(number) {
            return number * factor;
          };
        }
        
        const double = createMultiplier(2);
        console.log(double(5)); // Output: 10
        
        ```
        

## *** 8. what is this?

In JavaScript, the `this` keyword refers to an **object**.

**Which** object depends on how `this` is being invoked (used or called).

The `this` keyword refers to different objects depending on how it is used:

——————

In an object method, `this` refers to the **object**.

Alone, `this` refers to the **global object**.

In a function, `this` refers to the **global object**.

In a function, in strict mode, `this` is `undefined`.

In an event, `this` refers to the **element** that received the event.

Methods like `call()`, `apply()`, and `bind()` can refer `this` to **any object**.

——————

*** 9.  **What is currying in JavaScript?**

currying is a powerful technique in functional programming that allows for the creation of specialized functions by breaking down functions with multiple arguments into a series of single-argument functions. It promotes code reusability, composability, and expressiveness in JavaScript programs.

For example:

`codeconst add = x => y => x + y;
const add2 = add(2);
console.log(add2(3)); // Output: 5`

## ***** 9. Explain call(), apply() and, bind() methods.**

## *** 10. scope :

**1. Global Scope:**

- Variables declared outside of any function or block have global scope.
- They are accessible from anywhere in the code, including inside functions.
- Example:
    
    ```jsx
    
    const globalVariable = 10;
    
    function greet() {
      console.log(globalVariable); // Output: 10
    }
    
    greet();
    ```
    

**2. Local Scope:**

- Local scope refers to the scope of variables declared within a function.
- Variables with local scope are only accessible within the function in which they are declared.
- Local scope variables are not accessible outside the function.
- Example:
    
    ```jsx
    
    function greet() {
      const localVariable = 'Hello'; // localVariable has local scope
      console.log(localVariable); // Output: Hello
    }
    
    greet();
    console.log(localVariable); // Error: localVariable is not defined
    
    ```
    

**3. Block Scope (ES6 and later):**

- Block scope refers to the scope of variables declared with **`let`** and **`const`** within a block of code (e.g., **`{}`**).
- Variables with block scope are only accessible within the block in which they are declared.
- Block scope variables are not accessible outside the block.
- Example:
    
    ```jsx
    
    if (true) {
      let blockVariable = 'Hello'; // blockVariable has block scope
      console.log(blockVariable); // Output: Hello
    }
    
    console.log(blockVariable); // Error: blockVariable is not defined
    ```
    

**Key Differences:**

- Local scope is associated with functions, while block scope is associated with blocks of code (e.g., **`if`**, **`for`**, **`while`**).
- Variables with local scope are accessible within the entire function, while variables with block scope are only accessible within the block in which they are declared.
- Block scope was introduced in ES6 with the **`let`** and **`const`** keywords, allowing for more fine-grained control over variable visibility and avoiding issues like variable hoisting

## **** 11. Closure :

A closure is a function having access to the parent scope, even after the parent function has closed.

```jsx
function temp() {
    let counter = 0

    return function () {
        counter = counter + 1;
    }
}

const add = temp()
add()
console.dir(add)

// counter = 1 
```

Closures in JavaScript are a powerful concept where a function retains access to variables from its parent scope even after the parent function has finished executing. This allows for data encapsulation, creation of private variables, and maintaining state. Closures are created when a function is defined within another function, and the inner function captures and retains access to the variables of the outer function's lexical environment. They are widely used in JavaScript for tasks like creating factory functions, implementing modules, and managing asynchronous code.

## *** 12.  callback :

callbacks in JavaScript are functions passed as arguments to other functions, commonly used for handling asynchronous operations, event handling, and error handling. They provide a way to manage the flow of execution in asynchronous code and enable more flexible and responsive applications.

1. **Example**:
    
    ```jsx
    javascriptCopy code
    function fetchData(callback) {
      // Simulating an asynchronous operation (e.g., fetching data from a server)
      setTimeout(function() {
        const data = 'Some data';
        callback(data); // Invoking the callback function with the fetched data
      }, 1000);
    }
    
    function processData(data) {
      console.log('Processing data:', data);
    }
    
    fetchData(processData); // Pass processData function as a callback
    
    ```
    

## *** 13. Recursion :

1. **Function Calling Itself**: In recursion, a function calls itself within its definition.
2. **Base Case**: Recursion involves breaking down a problem into smaller instances until reaching a base case, which is a simple case that can be solved directly without further recursion.
3. **Example**: A classic example of recursion is computing factorial or calculating Fibonacci numbers.

### ⇒ **What are arrow functions?**

Arrow functions were introduced in the ES6 version of javascript. They provide us with a new and shorter syntax for declaring functions.

const  ****arrowAdd = (a,b) => a + b;

## ##Rest parameter  and spread operator…

1. **Rest Parameter (`...`)**:
    - Used in function parameters to collect an indefinite number of arguments into an array.
    - It gathers up all the remaining parameters passed to a function into a single array variable.
    - Typically used in function definitions.
    
    Example:
    
    ```jsx
    
    function sum(...numbers) {
      // 'numbers' is an array containing all the arguments passed to the function
      // Do something with 'numbers'...
    }
    
    ```
    
2. **Spread Operator (`...`)**:
    - Used to expand an array into individual elements or to combine multiple arrays.
    - It allows an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected.
    - Typically used in function calls or array literals.
    
    Example:
    
    ```jsx
    
    const numbers = [1, 2, 3];
    console.log(...numbers); // Prints: 1 2 3
    
    const arr1 = [1, 2, 3];
    const arr2 = [4, 5, 6];
    const combinedArray = [...arr1, ...arr2]; // Combining two arrays
    
    ```
    

In summary, the rest parameter gathers up multiple arguments into an array within a function, while the spread operator spreads out an array into individual elements or combines multiple arrays.

### async and await **:**

**`async`** and **`await`** are features in JavaScript used with promises to simplify and write asynchronous code in a more synchronous style, making it easier to work with asynchronous operations.

- **`async` Function:**
    - An **`async`** function is a function that always returns a promise.
    - It allows you to write asynchronous code in a more linear and readable manner by using the **`await`** keyword to wait for promises to resolve.
- **`await` Operator:**
    - The **`await`** operator can only be used inside an **`async`** function.
    - It pauses the execution of an **`async`** function until the promise is settled (resolved or rejected).
    - When used with a promise, **`await`** "waits" for the promise to resolve, and it returns the resolved value.

## Promises :

 The ***Promise*** object represents the eventual completion (or failure) of an asynchronous operation and its resulting value.

A `Promise` is in one of these states:

- *pending*: initial state, neither fulfilled nor rejected.
- *fulfilled*: meaning that the operation was completed successfully.
- *rejected*: meaning that the operation failed.

### **What is Object Destructuring?**

Object destructuring is a new way to extract elements from an object or an array.

## ***** Difference between “undefine” and “NULL” Keywords?**

**Undefine :** 

It typically means that a variable has been declared but has not been assigned a value.  "undefined" usually indicates an unintentional absence of a value, such as when you access a variable that has been declared but not initialized.

```jsx

let x;
console.log(x); // Output: undefined

const obj = {};
console.log(obj.property); // Output: undefined
```

 **Null**:

**`null`** is a special value that represents the intentional absence of any object value.  When using loose equality (**`==`**), **`null`** is only equal to **`undefined`** and itself. In strict equality (**`===`**), **`null`** is not equal to anything except **`null`**.

let y = null;
console.log(y); // Output: null

## ***** What is prototypal Inheritance?**

Prototypal inheritance is a way objects in JavaScript can share properties and behaviors with other objects. It works like a chain, where each object has a link to another object called its "prototype." When you try to access a property or method on an object, JavaScript first looks for it directly on that object. If it doesn't find it, it looks at the object's prototype. If it's not there, it looks at the prototype's prototype, and so on, until it finds the property/method or reaches the end of the chain.

## ****** What is SetTimeout()?**

**`setTimeout()`** is a function in JavaScript used to schedule the execution of a function after a specified delay in milliseconds. It allows you to create timed events that occur asynchronously.

**`setTimeout()`** is commonly used in web development for tasks like delaying the execution of animations, showing pop-ups, making HTTP requests after a certain time, etc.

```jsx

setTimeout(function, delay);
```

- The first argument is the function you want to execute after the delay.
- The second argument is the delay in milliseconds before the function is executed.

### ⇒ map, filter, reduce:

1. **`map()`**:
    - The **`map()`** method in JavaScript is used to transform elements of an array by applying a provided function to each element and returning a new array with the results. **It creates a new array without modifying the original array**
    
    ```jsx
    
    const numbers = [1, 2, 3, 4, 5];
    const squaredNumbers = numbers.map((num) => num * num);
    // Output: [1, 4, 9, 16, 25] - Each number in 'numbers' squared
    ```
    
2. **`filter()`**:
    - The **`filter()`** method in JavaScript is used to create a new array by filtering out elements from an existing array that satisfy a specified condition defined by a provided function. **It returns a new array containing only the elements that pass the condition.**
    
    ```jsx
    
    const numbers = [10, 20, 30, 40, 50];
    const filteredNumbers = numbers.filter((num) => num > 25);
    // Output: [30, 40, 50] - Numbers greater than 25 from 'numbers'
    ```
    
3. **`reduce()`**:
    - The **`reduce()`** method in JavaScript is used to **accumulate or reduce an array into a single value**. It executes a provided function for each element of the array, resulting in a single output value.
    
    ```jsx
    
    const numbers = [1, 2, 3, 4, 5];
    const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
    // Output: 15 - Sum of all numbers in 'numbers'
    ```
    
    - The **`reduce()`** method takes an accumulator (initially set to **`0`** in the example) and a function that performs the accumulation operation.
    - It executes the function on each element in the array, accumulating a single result.
    
    # ⇒ setTimeOut and setInterval:
    
    setTimeOut and setInterval are both functions in JavaScript used for executing code after a certain amount of time has passed.
    
    1. **setTimeout:**
        - **`setTimeout`** is a function that executes a specified function or piece of code once after a specified delay (in milliseconds).
        - It takes in two parameters: a callback function to execute and a delay time in milliseconds.
        - For example:
        
        ```jsx
        
        // Example of setTimeout
        setTimeout(function() {
          console.log('This message will appear after 2000 milliseconds (2 seconds)');
        }, 2000);
        
        ```
        
    2. **setInterval:**
        - **`setInterval`** is a function that **repeatedly executes** a specified function or piece of code at defined intervals.
        - It also takes in two parameters: a callback function to execute and the interval time in milliseconds.
        - For example:
        
        ```jsx
        
        // Example of setInterval
        let counter = 0;
        const intervalId = setInterval(function() {
          counter++;
          console.log(`Counter: ${counter}`);
          if (counter === 5) {
            clearInterval(intervalId); // Stops the interval after counter reaches 5
          }
        }, 1000);
        
        ```
        
    
    Key differences:
    
    - **`setTimeout`** executes the code once after the specified delay.
    - **`setInterval`** executes the code repeatedly at the specified interval until it's explicitly stopped using **`clearInterval`**.
    
    # What does it mean when we say JavaScript is single-threaded?
    
    It means that the main thread where JavaScript code is run, runs in one line at a time manner and there is no possibility of running code in parallel.
    
    # How do Event loops work?
    
    1. **Call Stack:**
        - JavaScript uses a call stack to keep track of the currently executing function (where the program is in its execution).
    2. **Callback Queue:**
        - Asynchronous operations, such as I/O operations or timers, are handled by the browser or Node.js runtime. When these operations are complete, corresponding functions (callbacks) are placed in the callback queue.
    3. **Event Loop:**
        - The event loop continuously checks the call stack and the callback queue. If the call stack is empty, it takes the first function from the callback queue and pushes it onto the call stack for execution.
    4. **Execution:**
        - The function on top of the call stack is executed. If this function contains asynchronous code, it might initiate further asynchronous operations.
    5. **Callback Execution:**
        - When an asynchronous operation is complete, its callback is placed in the callback queue.
    6. **Repeat:**
        - The event loop continues this process, ensuring that the call stack is always empty before taking the next function from the callback queue.
    
    **Example:** In this example, a JavaScript script demonstrates synchronous blocking behavior. It starts by logging “Before delay,” then uses a function `delayBySeconds` to create a delay of 5 seconds using a busy-wait loop. The script then logs “After delay” after the 5-second delay completes.
