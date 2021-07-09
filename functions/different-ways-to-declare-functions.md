# Different Ways to Declare Functions

## Anonymous Functions

```javascript
function(firstName) {
  return `Dr. ${firstName}`;
}
```

## Function Expressions

```javascript
// function expression
const doctorize = function (firstName) {
  return `Dr. ${firstName}`;
};
```

## What is the difference between a function declaration and a function expression?

### Hoisting <a id="hoisting"></a>

There is only one real difference which is how they operate in something called **hoisting**. 

```javascript
doctorize("wes");

const doctorize = function (firstName) {
  return `Dr. ${firstName}`;
};

function doctorize2 (firstName) {
  return `Dr. ${firstName}`;
}
```

Uncaught ReferenceError: Cannot access 'doctorize' before initialization

```javascript
console.log(doctorize2("wes"));
const doctorize = function (firstName) {
  return `Dr. ${firstName}`;
};
function doctorize2 (firstName) {
  return `Dr. ${firstName}`;
}
```

## Arrow Functions

```javascript
const inchToCM = (inches) => {
  return inches * 2.54;
};
```

To get rid of the **explicit** return:

* first put the function on one line
* then delete the curly brackets`{` `}`
* finally, delete the `return` keyword

```text
const inchToCM = (inches) => inches * 2.54;
```

```text
const inchToCM = inches => inches * 2.54;
```

**Returning an object**

```javascript
const makeABaby = (first, last) => {
  return {
    name: `${first} ${last}`,
    age: 0,
  };
};
```

```javascript
const makeABaby = (first, last) => ({ name: `${first} ${last}`, age: 0 });
```

## IIFE

That is an **immediately invoked function expression**.\(pronounced **iffy**\).

```text
(function () {
  console.log("Running the Anon function");
  return `Your are cool`;
})();
```

## Methods

A method is simply a function that lives inside of an object.

```javascript
const wes = {
  name: "Wes Bos",
  // Method!
  sayHi: function sayHi() {
    console.log("Hey Wes!");
    return "Hey Wes!";
  },
  //Short hand Method
  yellHi() {
    console.log("HEY WESSSSS");
  },
};
```

What we did here is instead of writing `sayHi: function()` _\(which does work\)_, we can get rid of the `function` keyword and the `:`. That makes it into a property, `yellHi()`, which is set to the function `yellHi`.



There is another way, which is an arrow function. 👇

```javascript
const wes = {
  name: 'Wes Bos',
  // Method!
  sayHi: function sayHi() {
    console.log('Hey Wes!');
    return 'Hey Wes!';
  },
  // Short hand Method
  yellHi() {
    console.log('HEY WESSSSS');
  },
  // Arrow function
  whisperHi: () => {
     console.log('hiii wess im a mouse');
  }
};
```

## This

```javascript
const wes = {
  name: 'Wes Bos',
  // Method!
  sayHi: function sayHi() {
    console.log('Hey Wes!');
    console.log(this);  //{name: "Wes Bos", sayHi: ƒ, yellHi: ƒ, whisperHi: ƒ}
    console.log(`Hey ${this.name}`); //Hey Wes Bos
    return 'Hey Wes!';
  },
  // Short hand Method
  yellHi() {
    console.log('HEY WESSSSS');
  },
  // Arrow function
  whisperHi: () => {
     console.log(this.name); // not working
     console.log('hiii wess im a mouse');
  }
};
```

That will not work in an arrow function because they take the parent scope of `this`.   


## Callback Functions

### Click Callback

```javascript
const button = document.querySelector(".clickMe");
button.addEventListener("click", wes.sayHi);
```

What is happening there is that `.addEventListener()` is an **event listener** that we are listening for a click on, and the callback function is `wes.sayHi()`.

Another thing you can do is just pass it an anonymous function, as shown below.

```javascript
button.addEventListener("click", function () {
  console.log("nice Job!");
});
```

What you need to know is that a **callback function is a function that gets passed into another function and then it is called by the browser at a later point in time.**

### Timer Callback​

```javascript
setTimeout();
```

It takes two things:

1. a function to call after a certain amount of time
2. a duration in milliseconds \(after how long should I run this\)

```javascript
setTimeout(wes.yellHi, 1000);

setTimeout(() => {
  console.log("DONE TIME TO EAT");
}, 1000);
```

