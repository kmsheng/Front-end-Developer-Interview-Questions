# What is a closure, and how / why would you use one ?
Closure is a combination of a function and the lexical environment it creates.

## Lexical scoping
Inner block can reference outer block's variable, but not vice versa.

```js
function createFunc() {
  const secret = 'blah';    // declare secret in createFunc
  return function showSecret() {
    console.log(secret);    // reference secret from outer context
  }
}

let show = createFunc();

show();
```

```js
function outer() {

  function inner() {
    const secret = 'blah';
  };
  console.log(secret);    // ReferenceError
}

outer();
```

## Closure
By creating indiviual counters using closure, each `num` can be added separately.

```js
function createAdder() {
  let num = 0;
  return {
    add: function() {
      num++;
    },
    getNum: function() {
      return num;
    }
  };
}

const adder1 = createAdder();
adder1.add();
adder1.add();

const adder2 = createAdder();
adder2.add();

console.log('adder1: ', adder1.getNum());    // adder1: 2
console.log('adder2: ', adder2.getNum());    // adder2: 1
```

### References
 - https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures
