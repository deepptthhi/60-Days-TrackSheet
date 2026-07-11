

## Classes

``` js
class Student{
 constructor(name){
  this.name=name;
 }
}
```

### Inheritance

``` js
class Animal{}
class Dog extends Animal{}
```

## Promises

``` js
fetch(url)
.then(res=>res.json())
.catch(err=>console.log(err));
```

## async / await

``` js
async function load(){
 const data=await fetch(url);
}
```

## Event Loop

JavaScript executes synchronous code first, then asynchronous tasks.

## Modules

Export:

``` js
export function add(){}
```

Import:

``` js
import {add} from "./math.js";
```
