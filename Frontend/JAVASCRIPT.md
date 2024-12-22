Sure! Here are the topics with simple explanations and examples:

**1. Closures**  
A closure is when a function remembers its lexical scope, even when the function is called outside of that scope.

Example:  
```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}

const counter = outer();
counter(); // 1
counter(); // 2
```

**2. Hoisting**  
Hoisting is when JavaScript moves variable and function declarations to the top of their scope.

Example:  
```javascript
console.log(x); // undefined (not an error)
var x = 5;
```
Explanation: `var x` is hoisted, but its value (`5`) is not assigned until later.

**3. Event Loop & Callbacks**  
The event loop manages asynchronous code by using callbacks, which are functions executed later.

Example:  
```javascript
console.log("Start");

setTimeout(() => {
  console.log("Inside setTimeout");
}, 1000);

console.log("End");
// Output: Start, End, Inside setTimeout
```
Explanation: `setTimeout` is asynchronous, and the callback runs after 1 second.

**4. Promises**  
A promise is an object that represents a task that may complete in the future. You can attach `.then()` for success and `.catch()` for errors.

Example:  
```javascript
let promise = new Promise((resolve, reject) => {
  let success = true;
  if (success) {
    resolve("Task completed!");
  } else {
    reject("Task failed!");
  }
});

promise.then((message) => {
  console.log(message); // Task completed!
}).catch((error) => {
  console.log(error); // Task failed!
});
```

**5. Async/Await**  
`async` makes a function return a promise, and `await` pauses the code until the promise resolves.

Example:  
```javascript
async function fetchData() {
  let data = await new Promise(resolve => resolve("Data loaded"));
  console.log(data); // Data loaded
}

fetchData();
```

**6. Arrow Functions**  
Arrow functions are a shorter way to write functions and don't have their own `this`.

Example:  
```javascript
const add = (a, b) => a + b;
console.log(add(2, 3)); // 5
```

**7. Destructuring**  
Destructuring lets you extract values from arrays or objects into variables.

Example (Object Destructuring):  
```javascript
const person = { name: "John", age: 30 };
const { name, age } = person;
console.log(name); // John
console.log(age); // 30
```
Example (Array Destructuring):  
```javascript
const colors = ["red", "green", "blue"];
const [first, second] = colors;
console.log(first); // red
console.log(second); // green
```

**8. Spread & Rest Operators**  
The spread operator `...` spreads elements of an array or object. The rest operator `...` collects multiple values into a single array.

Example (Spread):  
```javascript
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5];
console.log(arr2); // [1, 2, 3, 4, 5]
```

Example (Rest):  
```javascript
function sum(...numbers) {
  return numbers.reduce((acc, num) => acc + num, 0);
}
console.log(sum(1, 2, 3)); // 6
```

**9. Prototypes**  
Every object has a prototype, which is an object it inherits methods and properties from.

Example:  
```javascript
function Person(name) {
  this.name = name;
}

Person.prototype.greet = function() {
  console.log("Hello " + this.name);
};

const person1 = new Person("Alice");
person1.greet(); // Hello Alice
```

**10. This Keyword**  
`this` refers to the object that called the function.

Example (In an object method):  
```javascript
const person = {
  name: "Bob",
  greet: function() {
    console.log("Hello " + this.name);
  }
};
person.greet(); // Hello Bob
```

**11. Classes**  
Classes are templates for creating objects. They allow you to create multiple instances with shared properties and methods.

Example:  
```javascript
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log("Hello " + this.name);
  }
}

const person1 = new Person("John");
person1.greet(); // Hello John
```

**12. Modules**  
Modules let you split your code into separate files. You can `export` and `import` code from different files.

Example (Exporting in `person.js`):  
```javascript
export const person = { name: "Alice" };
```
Example (Importing in `app.js`):  
```javascript
import { person } from './person.js';
console.log(person.name); // Alice
```

**13. Map and Filter**  
`map()` creates a new array by applying a function to each item. `filter()` creates a new array with items that pass a test.

Example (`map`):  
```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6]
```

Example (`filter`):  
```javascript
const numbers = [1, 2, 3, 4];
const even = numbers.filter(num => num % 2 === 0);
console.log(even); // [2, 4]
```

**14. Reduce**  
`reduce()` combines all items in an array into one value.

Example:  
```javascript
const numbers = [1, 2, 3];
const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum); // 6
```

**15. SetTimeout & SetInterval**  
`setTimeout()` runs a function once after a delay. `setInterval()` runs a function repeatedly.

Example (`setTimeout`):  
```javascript
setTimeout(() => console.log("After 2 seconds"), 2000);
```

Example (`setInterval`):  
```javascript
setInterval(() => console.log("Every 2 seconds"), 2000);
```

**16. Template Literals**  
Template literals let you embed expressions and write multi-line strings.

Example:  
```javascript
const name = "John";
const greeting = `Hello, ${name}!`;
console.log(greeting); // Hello, John!
```

**17. Type Coercion**  
Type coercion is JavaScript automatically converting types, like changing a string `"5"` into a number `5`.

Example:  
```javascript
console.log("5" + 5); // "55" (string)
console.log("5" - 5); // 0 (number)
```

**18. Truthy & Falsy Values**  
Falsy values are `false`, `0`, `""`, `null`, `undefined`, `NaN`. Everything else is truthy.

Example:  
```javascript
if ("") { // falsy
  console.log("True");
} else {
  console.log("False"); // False
}
```

**19. Debouncing & Throttling**  
Debouncing limits how often a function is called. Throttling limits the frequency of function calls.

Example (Debouncing):  
```javascript
let timer;
function search() {
  clearTimeout(timer);
  timer = setTimeout(() => console.log("Searching..."), 500);
}
```

Example (Throttling):  
```javascript
let lastExecutionTime = 0;
function throttle() {
  const now = Date.now();
  if (now - lastExecutionTime > 1000) {
    console.log("Action executed");
    lastExecutionTime = now;
  }
}
```

**20. Currying**  
Currying is when a function returns another function to handle each argument.

Example:  
```javascript
function add(a) {
  return function(b) {
    return a + b;
  };
}

const add5 = add(5);
console.log(add5(3)); // 8
```

I hope these examples make each topic clearer and help you remember them better!
