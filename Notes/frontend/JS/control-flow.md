

## If

``` js
if(age>=18){
 console.log("Adult");
}
```

## if...else

``` js
if(mark>=35){
 console.log("Pass");
}else{
 console.log("Fail");
}
```

## Switch

``` js
switch(day){
 case 1:
   console.log("Monday");
   break;
 default:
   console.log("Unknown");
}
```

## Loops

### for

``` js
for(let i=0;i<5;i++){
 console.log(i);
}
```

### while

``` js
while(i<5){
 i++;
}
```

### do...while

Runs at least once.

## break

Stops loop.

## continue

Skips current iteration.

## Scope

-   Global
-   Function
-   Block (`let`,`const`)

## Functions

``` js
function add(a,b){
 return a+b;
}
```

Arrow function:

``` js
const add=(a,b)=>a+b;
```
