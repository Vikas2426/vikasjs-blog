---
title: "Arrow Functions"
date: "2020-11-18T22:12:03.284Z"
description: "Arrow functions are one of the best features introduced in ES6..."
---

Arrow functions are one of the best features introduced in ES6, although at first glance they can be a little confusing and intimidating.
So, here is your favourite blog explaining arrow functions with simple examples.

Arrow functions are actually arrow function expressions, they are nameless and mostly used as inline callback functions.

**1.Basic syntax**

```js
const add = (a, b) => {
  let c = a + b
  return c
}
```

Here, **add** is a const variable which is assigned the arrow function.<br/>
The function definition, as traditional function, lies between the curly braces and the parenthesis hold parameters.

**2.Parenthesis**

```js
const square = a => {
  let c = a * a
  return c
}
```

Here, observe that we have omitted the parenthesis but the important thing to notice is that we are passing only **one parameter**.<br/>
If we have exactly one parameter then we can omit the parenthesis.
This rule does not apply when there are zero or more than one parameters.<br/> So, the following code snippet will throw error

**two or more parameters, need parenthesis**

```js
const add = a, b =>{  //error at this line
  let c = a + b;
  return c;
}
```

**no parameters, need parenthesis**

```js
const add = =>{   //error at this line
  let c = 3+5;
  return c;
}
```

**3.Curly braces**

```js
const square = a => a * a
```

Here, we are able to omit the curly braces that hold the definition of the function, because we only have **one return statement**.<br/>
The important thing to notice here is that curly braces can be omitted when there is only one line of code in the definition of the function and the line of code is a return statement.

**4.Arrow functions as callbacks**

```js
const materials = ["Hydrogen", "Helium", "Lithium", "Beryllium"]

console.log(materials.map(material => material.length))
// expected output: Array [8, 6, 7, 9]
```

Here, we can see an arrow function being used as a callback function as well as previous examples at play.<br/>
"material" is the **single** parameter being passed to the arrow function therefore, there no paranthesis around it and the callback function **returns** the length of "material" therefore no curly braces either.

Thanks for reading, see you soon with another amazing JS feature...
