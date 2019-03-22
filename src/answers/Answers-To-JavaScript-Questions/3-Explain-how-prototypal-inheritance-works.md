# Explain how prototypal inheritance works.
Unlike other class-based languages, JavaScript uses `prototype` object to implement its inheritance model.

```js
function People(name) {
  this.name = name;
}

// Instance function should be defined in People.prototype to share memory.
People.prototype.speak = function() {
  console.log('Hello, my name is ' + this.name)
};

console.log(People.hasOwnProperty('name'));    // true, name is defined in function People, not its prototype

const p = new People('Alice');    // Create people instance

console.log(p.name);    // Alice
console.log(p instanceof People);    // true, Alice is an instance of People
p.speak();

Object.prototype.test = 'test';    // Set a test property to Object.prototype
console.log(p.test);    
// Property search path:
// Is p.test defined ? No
// Is p.__proto__.test defined ? No
// Is p.__proto__.__proto__.test defined ?  Yes

console.log(p.__proto__.__proto__ === Object.prototype);    // true
```

## Object.create
Another way to create inheritance is to use Object.create

```js
let Computer = {
  brand: 'Apple'
};

let obj = Object.create(Computer);

console.log('here', obj.__proto__);    // { brand: 'Apple' }
```
