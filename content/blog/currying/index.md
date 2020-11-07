---
title: "What is currying ?"
date: "2020-11-07T22:00:03.284Z"
description: "A process of transforming a function with multiple arguments into a function with fewer..."
---

Currying is a process of transforming a function with multiple arguments into a function with fewer arguments.
It can also be defined as partial evaluation of function.

Let's learn this with the help of an example :

```js
function add(x, y) {
  return function sum(y) {
    return x + y
  }
}

const add5 = add(5)
add5(6)

Output: 11
```

In the above example function 'add' which takes two arguments is transformed to a function which takes only one argument. Since, 'add' returns a reference to function 'sum' which takes the second argument, both arguments can be given in separate steps.
It also helps in creating a third function like 'add5' which will always return a sum of 5 and the value of arguments passed to it.
Similiarly several functions can be created without actually having to type their specific definitions.

```js
const add10 = add(10)
add10(20)

Output: 30
```

If we go by the second definition of currying, the example code snippets also show us that function 'add' gets partially evaluated when 5 is passed as its first argument. So, at this point 'add' knows that it has to add 5 to its second argument which has not been passed yet.

The above code snippet is also an example of a closure but not all curried functions are closures. Closure is only when a function references a variable that is out of its scope. For instance the code below is an example of currying but not closure.

```js
function add() {
  return function sum(y) {
    return y + y
  }
}

const add5 = add()
add5(6)

Output: 12
```

Now the concept that makes currying and closures possible is that javascript is a garbage collecting programming language, therefore whenever it sees that a variable/function is being referenced in forth coming code/steps that variable/ function is preserved.
