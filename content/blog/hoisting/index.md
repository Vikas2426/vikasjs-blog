<!-- ---
title: "Hoisting"
date: "2020-11-02T23:46:37.121Z"
description: "In Javascript programming language declarations are hoisted.
Now what do I mean by hoisting ? Is it like hoisting a flag..."
---

In Javascript programming language declarations are hoisted.
Now what do I mean by hoisting ? Is it like hoisting a flag...Yes, definitely like hoisting a flag.
Just as a flag when hoisted rises up the pole to which it is attached, declarations in Javascript rise up the top of the .js file.

This means no matter where in the file the declaration was actually made, upon compiling it will be hoisted to the top of the file.

```js
name = "Javascript"
console.log(name)
var name
```

The above code snippet upon compiling will become below snippet:

```js
var name
name = "Javascript"
console.log(name)
```

Hoisting is actually limited to variables declared using the keyword 'var' and functions declared using the keyword 'function'.

As of ES6 we have new ways of declaring variables which include 'const' and 'let' and we also get the beautiful arrow functions ()=> as well. These new features are excluded from the hoisting. So when you declare a variable using 'const' or 'let' or an arrow function do not expect it to be hoisted to the top.

Hoisting is what let us declare variables and functions after they were actually called in our javascript code.
But, if the value of those variables and functions were not defined before the code where they get called then we get and 'undefined' value.

Let's understand this with an example:

1. Defining > Calling > Declaring

```js
name = "Javascript"
console.log(name)
var name
```

The above code snippet will correctly log 'Javascript' in the console because the variable 'name' was actually defined before its value was called in the 'console.log(name)'.

2. Calling > Defining > Declaring

```js
console.log(name)
name = "Javascript"
var name
```

The above code snippet will log 'undefined' in the console because the variable was defined after its value was called for logging.

I hope this clears your fundamentals on hoisting in Javascript.
Stay tuned for more soon... -->
