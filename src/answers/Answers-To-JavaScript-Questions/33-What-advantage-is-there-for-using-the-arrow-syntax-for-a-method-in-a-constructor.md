# What advantage is there for using the arrow syntax for a method in a constructor ?
Once the arrow function is set in consturctor, its `this` cannot be changed.

```js
class Person {

  constructor(name) {

    this.name = name;
    this.sayName1 = () => console.log(this.name);
    this.sayName2 = function() {
      console.log(this.name);
    };
  }
}

const jeff = new Person('jeff');
const alice = new Person('alice');

jeff.sayName1.call(alice);    // jeff
jeff.sayName2.call(alice);    // alice, `this` has been changed to instance alice
```

### References
 - https://github.com/yangshun/front-end-interview-handbook/blob/master/questions/javascript-questions.md#what-advantage-is-there-for-using-the-arrow-syntax-for-a-method-in-a-constructor
