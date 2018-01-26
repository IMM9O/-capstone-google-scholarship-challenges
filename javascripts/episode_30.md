
# Episode 30

Now the problem of the day

## Add Negatives
Write a function that takes  an **array of elements of any  data type** and return a number represents **sum** of (**multiplication** result of all **non negative numbers**(and 0 included) and **sum of all negative numbers**)

**For example**
```
AddNeg([1,"5",NaN,2,3,-5,4,-6,7,8,-9]);// (1*2*3*4*7*8)+(-5-6-9) = 1324
AddNeg([-1,-5,-3,4,-1,6,true]) // (4*6) + (-1-5-3-1) // 14
AddNeg([0,-2,3,-1]) // -3
```
Really simple, good luck

# My Solution

```javascript
var neg = arr => {
    const sumNeg = arr.filter(n => (typeof n === 'number' && n < 0 )).reduce((p,c) => p+c, 0);
    const multiNum = arr.filter(n => (typeof n === 'number' && n >= 0)).reduce((p,c) => p*c, 1);
    return multiNum + sumNeg;
}
console.log(neg([1,"5",NaN,2,3,-5,4,-6,7,8,-9]));
console.log(neg([-1,-5,-3,4,-1,6,true]));
console.log(neg([0,-2,3,-1]));

```