
# Episode 29

Now the problem of the day
After i got many complaints about the difficulty of the problems, i should return back to easier problems still with useful ideas so....

## Multiple Of Sums

Write a function that takes an **array of numbers** as argument and returns a **number** respresents **multipe of sums** of every two next numbers in the array

**Examples**
```
multSum([1,2,3,4,5,6]); // 3 * 7 * 11= 231
multSum([1,2,5]) //  3 * 5 = 15
```
Good luck guys

# My Solution

Here is my solution first i used while loop to loop over the array to split array into chunks then using reduce to return total numbers for small array, after while loop using reduce to return multiplication of numbers.

```javascript
function multSum(arr){
    if(!arr.length) return 0;
    const chunks = [];
    let i = 0;
    while (i < arr.length) {
      chunks.push(arr.slice(i, i += 2).reduce((p, c) => p+c,0));
    }
    return chunks.reduce((p,c) =>  p*c, 1);
}

console.log(multSum([1,2,3,4,5,6]));  // 231
console.log(multSum([1,2])); //3
console.log(multSum([])); // handle empty array
console.log(multSum([1,2,5])); // 15

```
