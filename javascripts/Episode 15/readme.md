# Episode 15

Now, the problem of the day

Write a function that takes an array of **any level of nesting** , the function return an array represents the original array but the flattened version of it.


**For example**
```
flatten([1,5,6,[2,5,[10,12,15,[]],3,8],6,7); // [1,5,6,2,5,10,12,15,3,8,6,7]
```

Good luck guys


# My Solution

First i using toString to convert array to string and then search on ( [ or ] ) and remove it using regular expression split string with ( , ) then filter array to remove any empty string then finally map the result to convert it to number :slight_smile:  

```javascript
const flatten = x => x.toString().replace(/\[|\]/g,'').split(",").filter(s => s).map(t => Number(t));
console.log(flatten([1,5,6,[2,5,[10,12,15,[]],3,8],6,7]));
```