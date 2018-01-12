# Episode 12

Now the problem of the day, Ready??

## A big random number

Write a function that takes an array of two elements (numbers < 10) as argument, and returns a **number** composed of all the numbers between the two numbers with minimum and maximum numbers inclusives  **randomly** every time you call the function,  numbers that composes our returned number should be **different**( no repeated numbers)  and number of these numbers should be the **same** with the numbers in all range between the maximum and minimum number in array, with minimum and maximum **inclusive**, the array is **not sorted** so no strict places for  maximum or minimum number in it

Really i have wrote tons of word "number" so it may be confusing, lets jump to examples

**for example**

```
randomNum([1,5]);  // 45132
randomNum([5,1]);  // 31452
randomNum([0,9]); // 7429850136
randomNum([0,9])  // 5682910347
```

Good luck guys

# My Solution

Here is my soultion
First **[sort](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort)** the array from min to max then get the size of genrated random array ( `randomNums` ) by subtraction min number from max number in the array, then using **[while](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)** loop with stop condation when size of `randomNums` equal to the size of range then genrate random number between min and max  if genrated radom number not **[included](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes)** in `randNums` array then push it to the array and finally return the `randomNums` array.


```javascript
function randomNum(arr) {
    let sortedArr =  arr.sort((p,c) => p > c);
    let sizeOfRandomArry = sortedArr[1] - sortedArr[0];
    let ranNums = [];
    while (ranNums.length < sizeOfRandomArry) {
        let j = Math.floor(Math.random() * (sortedArr[1]-sortedArr[0]+1)+sortedArr[0]);
        if(!ranNums.includes(j)) ranNums.push(j);
    }
    return ranNums;
}

console.log(randomNum([10,9]));
console.log(randomNum([1,5]));
console.log(randomNum([5,1]));
console.log(randomNum([0,9]));
console.log(randomNum([0,9]));
```