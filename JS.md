# Types
- **Primitive Types** : String, Number, Boolean, Undefined, Null, Symbol
- **Composite Types** : Object, Functions

# Hoisting

### Definition
Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to the execution of the code.

1. Being able to use a variable's value in its scope before the line it is declared. ("Value hoisting") >> **`function`, `async function`**
2. Being able to reference a variable in its scope before the line it is declared, without throwing a ReferenceError, but the value is always undefined. ("Declaration hoisting") >> **`var`**
3. The declaration of the variable causes behavior changes in its scope before the line in which it is declared. >> **`let`, `const`, `class`**
4. The side effects of a declaration are produced before evaluating the rest of the code that contains it. >> **`import`**

### Note
- Variable initializations are not hoisted, only variable declarations are hoisted:
- Strict mode makes JS disable hoisting.

# Deffierence between `==` and `===`

“==” is used to compare **values** whereas, “ === “ is used to compare both **values and types**.

# `var`,`let`,`const`

|var|let,const|
|--|--|
|function scope|block scope|
|initialized when it's hoised|Not initialized when it's hoisted|

# Passed by value and Passed by reference

# Higher Order Functions

Higher-order functions operate on other functions, either by taking them as arguments or by returning them, as a function could be an argument or return values.

```
function higherOrder(fn) {
  fn();
}
higherOrder(function() { console.log("Hello world") });

function higherOrder2() {
  return function() {
    return "Do something";
  }
}      
var x = higherOrder2();
```

# `this`

### Definition
The “this” keyword refers to the object that the function is a property of. >> 실행된 함수가 어떤 객체(this)의 프로퍼티인지 보면 this를 쉽게 알 수 있다.

The value of the “this” keyword will always depend on the object that is invoking the function.

```
function doSomething() {
  console.log(this); // global object
}
   
doSomething();
```
Since the function is invoked in the global context, the function is a property of the global object.

# call(), bind(), apply()

Those are the method to bind the new object to `this`.

| call(), apply() | bind() |
| --- | --- |
| A predefined method | Returns a new function|

### Examples
```
function saySomething(message){
  return this.name + " is " + message;
}        
var person4 = {name:  "John"};
saySomething.call(person4, "awesome");
saySomething.apply(person4, ["awesome"]); // takes arguments as an **array**
```

```
var bikeDetails = {
    displayDetails: function(registrationNumber,brandName){
    return this.name+ " , "+ "bike details: "+ registrationNumber + " , " + brandName;
  }
}
var person1 = {name:  "Vivek"};

// returns a new function
var detailsOfPerson1 = bikeDetails.displayDetails.bind(person1, "TS0122", "Bullet");
detailsOfPerson1(); 
```

# Scope

### Definition
Scope lets us know where variables and functions we can or cannot access.

### Types

1. Global Scope
2. Local or Function Scope: Any variables or functions declared inside a function have local/function scope
3. Block Scope: Any variable declared inside a block { }. It's related to using `let` and `const`. ex) for loop, while, ...

# Scope Chain

### Definition
It is that JS engine uses scopes to find variables.

# Closure


# Object prototypes

# Callbacks

# Types of Errors in JS

1. Syntax Error: mistakes or spelling problems in the code
2. Logical Error: mistakes occur when the syntax is proper but the logic or program is incorrect.

# Memoization

# Constructor function

### Definition
Constructor functions are used to create objects in javascript. 

- The name should be always written in Pascal.
- When we want to create a new object of the constructor function, we need to use the `new` keyword (class, instance)


# DOM (Document Object Model)

When the browser tries to render an HTML document, it creates an object based on the HTML document called DOM. Using DOM, we can manipulate or change various elements inside the HTML document.

# client-side vs server-side in JS

<img width="476" alt="image" src="https://github.com/OHSOHYEON00/TIL/assets/132743799/352245c1-d03f-4939-91b1-1a2aea66f2f5">

------------------------------------------------------------

# Execution Context
https://www.freecodecamp.org/news/how-javascript-works-behind-the-scene-javascript-execution-context/

# `null`, `undefined`, `undeclared`

# Prototype inheritance works

# Annoymous function

1. Explanation
2. Typical use case





# Event bubbling

1. Event bubbling
2. event.preventDefault(), event.stoppropagation()





----
https://www.interviewbit.com/javascript-interview-questions/#object-prototypes
https://www.geeksforgeeks.org/javascript-interview-questions-and-answers/?ref=lbp


1. Explain about Ajax in as much detail as possible
2. What are the advantages and disadvantages of using Ajax
