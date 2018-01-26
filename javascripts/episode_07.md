# Episode 07

Now, the problem of the day!!!

**check if your name characters present in a given string**

write a function that takes a a string as an argument represents your name that checks if **all your name characters** presents in this string
```
 "hello all my great friends";
```

**For example**
```
check("karl"); // false
check("sally"); // true
```
Good luck


# My solution

First split the string then using reduce function to return true or false with initial value true `the return value of the reduce callback just becomes the value of previous ( p ) parameter in the next iteration`.

```javascript
let chekString = "hello all my great friends";
const check = str => str.split("").reduce((p,c,i,arr) => p && (chekString.indexOf(c)>-1),true);

console.log(check("karl"));  //false
console.log(check("sally"));  //true
console.log(check("islam")); //true
```
