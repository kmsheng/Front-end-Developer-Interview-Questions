---
title: JavaScript Questions
layout: layouts/page.njk
permalink: /questions/javascript-questions/index.html
---

* [Explain event delegation.](../answers/Answers-To-JavaScript-Questions/1-Explain-event-delegation.md)
* [Explain how `this` works in JavaScript.](../answers/Answers-To-JavaScript-Questions/2-Explain-how-this-works-in-JavaScript.md)
  * [Can you give an example of one of the ways that working with `this` has changed in ES6?](../answers/Answers-To-JavaScript-Questions/2-Explain-how-this-works-in-JavaScript.md)
* [Explain how prototypal inheritance works.](../answers/Answers-To-JavaScript-Questions/3-Explain-how-prototypal-inheritance-works.md)
* [What's the difference between a variable that is: `null`, `undefined` or undeclared?](../answers/Answers-To-JavaScript-Questions/5-Whats-the-difference-between-a-variable-that-is-null-undefined-or-undeclared.md)
  * [How would you go about checking for any of these states?](../answers/Answers-To-JavaScript-Questions/5-Whats-the-difference-between-a-variable-that-is-null-undefined-or-undeclared.md)
* [What is a closure, and how/why would you use one?](../answers/Answers-To-JavaScript-Questions/6-What-is-a-closure-and-howwhy-would-you-use-one.md)
* [What language constructions do you use for iterating over object properties and array items?](../answers/Answers-To-JavaScript-Questions/7-What-language-constructions-do-you-use-for-iterating-over-object-properties-and-array-items.md)
* [Can you describe the main difference between the `Array.forEach()` loop and `Array.map()` methods and why you would pick one versus the other?](../answers/Answers-To-JavaScript-Questions/8-Can-you-describe-the-main-difference-between-the-ArrayforEach-loop-and-Arraymap-methods-and-why-you-would-pick-one-versus-the-other.md)
* [What's a typical use case for anonymous functions?](../answers/Answers-To-JavaScript-Questions/9-Whats-a-typical-use-case-for-anonymous-functions.md)
* [What's the difference between host objects and native objects?](../answers/Answers-To-JavaScript-Questions/10-Whats-the-difference-between-host-objects-and-native-objects.md)
* [Explain the difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?](../answers/Answers-To-JavaScript-Questions/11-Explain-the-difference-between-function-Person-var-person-Person-and-var-person-new-Person.md)
* [Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}`](../answers/Answers-To-JavaScript-Questions/12-Explain-the-differences-on-the-usage-of-foo-between-function-foo-and-var-foo-function.md)
* [Can you explain what `Function.call` and `Function.apply` do? What's the notable difference between the two?](../answers/Answers-To-JavaScript-Questions/13-Can-you-explain-what-Functioncall-and-Functionapply-do-Whats-the-notable-difference-between-the-two.md)
* [Explain `Function.prototype.bind`.](../answers/Answers-To-JavaScript-Questions/14-Explain-Function-prototype-bind.md)
* [What's the difference between feature detection, feature inference, and using the UA string?](../answers/Answers-To-JavaScript-Questions/15-Whats-the-difference-between-feature-detection-feature-inference-and-using-the-UA-string.md)
* [Explain "hoisting".](../answers/Answers-To-JavaScript-Questions/16-Explain-hoisting.md)
* [Describe event bubbling.](../answers/Answers-To-JavaScript-Questions/17-Event-bubbling.md)
* [Describe event capturing.](../answers/Answers-To-JavaScript-Questions/18-Event-capturing.md)
* [What's the difference between an "attribute" and a "property"?](../answers/Answers-To-JavaScript-Questions/19-Whats-the-difference-between-an-attribute-and-a-property.md)
* [What are the pros and cons of extending built-in JavaScript objects?](../answers/Answers-To-JavaScript-Questions/20-What-are-the-pros-and-cons-of-extending-built-in-JavaScript-objects.md)
* [What is the difference between `==` and `===`?](../answers/Answers-To-JavaScript-Questions/21-What-is-the-difference-between-abstract-equality-comparison-and-strict-equality-comparison.md)
* Explain the same-origin policy with regards to JavaScript.
* Why is it called a Ternary operator, what does the word "Ternary" indicate?
* What is strict mode? What are some of the advantages/disadvantages of using it?
* What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?
* What tools and techniques do you use debugging JavaScript code?
* Explain the difference between mutable and immutable objects.
  * What is an example of an immutable object in JavaScript?
  * What are the pros and cons of immutability?
  * How can you achieve immutability in your own code?
* Explain the difference between synchronous and asynchronous functions.
* What is event loop?
  * What is the difference between call stack and task queue?
* What are the differences between variables created using `let`, `var` or `const`?
* What are the differences between ES6 class and ES5 function constructors?
* Can you offer a use case for the new arrow `=>` function syntax? How does this new syntax differ from other functions?
* What advantage is there for using the arrow syntax for a method in a constructor?
* What is the definition of a higher-order function?
* Can you give an example for destructuring an object or an array?
* Can you give an example of generating a string with ES6 Template Literals?
* Can you give an example of a curry function and why this syntax offers an advantage?
* What are the benefits of using `spread syntax` and how is it different from `rest syntax`?
* How can you share code between files?
* Why you might want to create static class members?

## Coding questions
* Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```
* Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`
