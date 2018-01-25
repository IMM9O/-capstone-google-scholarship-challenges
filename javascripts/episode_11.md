# Episode 11

Now the problem of the day!!!

Write a function that takes an array as an argument and finds the smallest number divisible by all array elements

For example
```
smallestDivisible([1,2,4,9]); // 36
```
**consider** all numbers of the array to be > 0

**Please** guys, explain your code, consider a fellow  wants to understand your code and can not do

Good luck guys


# My Solution

Here is my solution, using while loop to find the GCD starting from number one and in each iterator using reduce with initialValue equal to reminder of current iterator number by first number in array and if the result is zero break the loop otherwise continue the iterations.


```javascript
function smallestDivisible(arr) {
    let iterator = 1;
    while(true) {
        const isZero = !arr.reduce((p,c) => p+iterator%c,  iterator%arr[0]);
        if(isZero) break;
        else iterator++;
    }
    return iterator;
}
console.log(smallestDivisible([1,2,4,9,10])); // 180
```

