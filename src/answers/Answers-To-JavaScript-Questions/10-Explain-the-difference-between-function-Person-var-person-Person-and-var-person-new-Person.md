# Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()` ?

 - `function Person(){}` declares the function `Person`
 - `var person = Person()` executes the function `Person` and set its returned value `undefined` to variable person.
 - `var person = new Person()` creates an instance by `Person` function, since it uses the `new` keyword, it will call the constructor of `Person` and has its own prototype ( \_\_proto\_\_ property )
