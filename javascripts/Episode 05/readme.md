# Episode 5

Now with the problem of the day!!!!

**Sum of two largest numbers in array**

Write a function that takes an array of numbers as argument and returns a number represent the sum of the two largest numbers in it.

**Examples**:

```
sum([5,12,4,2,36]); // 48
sum([60,70,80,90,100,200] ); //300
```

**Note:** assume array elements are positive numbers

Good luck guys


# My Solution

First using **[sort](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)** function to sort array then using **[slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)** to get the last two digit in array then using **[reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)** to get the final result which is sum of last two digit

```javascript
const sumLastTwoLargeDigit = arr => arr.sort((a,b) => a>b).slice(-2).reduce((a,b) => a+b, 0);
console.log(sumLastTwoLargeDigit([60,70,80,90,100,200]));
```

> Not my soultion but updated
```javascript
const sum = a => Math.max(...a) + Math.max(...a.filter(e => e < Math.max(...a)));
```

