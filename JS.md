# Types
- **Primitive Types** : String, Number, Boolean, Undefined, Null, Symbol
- **Composite Types** : Object, Functions

# Hoisting

### Definition
Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables, classes, or imports to the top of their scope, prior to execution of the code.

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

# Passed by value and Passed by reference

# Higher Order Functions

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

# Scope, Scope chain

# Closure

# Object prototypes

# Callbacks

# Types of Errors in JS

1. Syntax Error
2. Logical Error

# Memoization

# Constructor function

# DOM

# client-side vs server-side in JS

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
