### Big Ideas from W1D2

- developers do not write code for themselves but for other developers. REALLY important to prioritize readability
  - akin to how authors write for others to read and understand thier thoughts
  - [19 Best Practice Tips](https://code.tutsplus.com/tutorials/top-15-best-practices-for-writing-super-readable-code--net-8118)

* process.exit() is the way to end an entire script
* break is how to end / break out of a loop
* return is how to end a function
* to see if a number is a whole number
  - num % 1 === 0 will evaluate to true -- language agnostic
  - Number.isInteger(num) - javascript specific
* when possible try to build functions with "Single Responsibility Principle"
  - functions should have a single purpose instead of many purposes
  - better to have multiple smaller functions than large functions doing many things
  - best to build functions that are lightweight, reuseable, not specific, simple, and single tasked
  - smaller less specific functions are more reuseable, while large funcitons with a lot going on in them are only really good for the specific use at hand
* ideal to have functions NOT read / access variables from outer scops
* if a function needs a variable, best to pass it in as a paramenter / arguement

bad example

```javascript
let person = 'Martha';

const sayHello = () => {
  console.log(`Hello ${person}!`);
};
```

- bad example:
  - accesses person variable in an outer scope
  - function cannot be moved without also moving the outside variable it depends on
  - throws an unecasary side effect
  - ASIDE: side effects are not always a bad thing

good example

```javascript
let person = 'Susan';

const sayHello = (name) => {
  return `Hello ${name}!`;
};

console.log(sayHello(person));
```

- good example:
  - brings needed variables into its own scope
  - function can be moved into other programs and re-used
  - returns a value that can be used by another function
  - does a single task - creates the hello string
