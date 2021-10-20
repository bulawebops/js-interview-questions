## How is JavaScript different from Java?
JavaScript back in 1995, founder of Netscape Marc Andreessen envisioned a scripting language that was simple for amateur coders to use. Sadly Java wasn't that. Java is an Object Oriented Programming (OOP) language created by James Gosling of Sun Microsystems. Netscape recruited Brendan Eich with the goal of embedding the Scheme programming language into Netscape Navigator. History states that in just 10 days Brendan created the first version of Mocha > LiveScript which is now referred to as JavaScript.

## Can you differentiate between var and let?
Both let and var are used for variable and method declaration in JavaScript. A difference between these two keywords would be that var keyword is function scoped, the let keyword is block scoped.

## What is function scoped mean?


## What is block scoped mean?


## Name three built-in methods in JavaScript that you have used recently?
``` Date(), pop(), slice() ```

## Explain Self Invoking Function
Functions that are automatically invoked are termed as Self Invoking Functions. These are also known as Immediately Invoked Function Expressions and Self Executing Anonymous Functions. The general syntax of a Self Invoking Function is:
```
(some_function () {
 return () }) ();
}
```
Typically, a function is defined and then invoked. However, if there is a need to automatically execute a function at the place where it is given and not be called again, then anonymous functions can be used. Such functions have no name, and thus the name.

## What are Closures?
Closures supposely a better, concise, and efficient way of writing code. Closure is a locally declared variable that is related to a function and stays in the memory when the related function has returned. The closure contains all local variables that were in-scope at the time of the closure creation.

### Example of a normal function:
```
function greet(message) {
  console.log(message);
}```

```function greeter(name, age) {
  return name + " says Hey!! He is " + age + " years old";
}```

```var message = greeter("John", 56);
greet(message);```

### The function can be represented in a better way by using closures below:
```
function greeter(name, age) {
  var message = name + " says Hey!! He is " + age + " years old";
  return function greet() {
  console.log(message);
 };
}

let johnGreeter = greeter("John", 56);
// Use the closure

johnGreeter();
```
