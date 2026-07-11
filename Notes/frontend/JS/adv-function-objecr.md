

## Functions

### Function Expression

``` js
const greet=function(){ console.log("Hi"); };
```

### Arrow Functions

``` js
const square=n=>n*n;
```

### Callback Functions

A function passed as an argument to another function.

### Higher-Order Functions

Functions that accept or return other functions.

### Closures

An inner function remembers variables from its outer function even after
the outer function finishes.

## Objects

Objects store data as key-value pairs.

``` js
const user={
  name:"Deepthi",
  age:21
};
```

### this Keyword

Refers to the current object.

### Destructuring

``` js
const {name}=user;
```

### Spread Operator

``` js
const copy={...user};
```

### Rest Parameter

``` js
function sum(...nums){}
```
