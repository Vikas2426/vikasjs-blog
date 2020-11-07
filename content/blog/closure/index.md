---
title: "What are closures ?"
date: "2020-11-04T22:00:03.284Z"
description: "A simple answer to the question 'What is a closure?' is Closures are a phenomenon where an inner function..."
---

A simple answer to the question 'What is a closure?' is Closures are a phenomenon where an inner function remembers the variables defined in outer function even after the outer function has finished executing.

Let's learn this with the help of an example :

```js
function outer() {
  let name = "Javascript"
  return function inner() {
    console.log(name)
  }
}

const printName = outer()
printName()
```

In the code snippet above we see that when function 'outer' is called and it finishes execution it returns a reference to function 'inner' which is passed to the variable 'printName' and using this reference we call the function 'inner' for execution which remembers and logs to console the value of variable 'name' declared and defined inside function 'outer';

Now the thing that makes this concept interesting is that actually when functions are finished executing all variables defined locally inside those functions get removed from memory which means 'name', from our example above, should have been cleared from memory and 'inner' should have thrown an error but due to the concept of closure when 'outer' finished execution, 'name' was remembered/saved by 'inner'.

Stay tuned for more blogs...
Coming up next is Currying.
