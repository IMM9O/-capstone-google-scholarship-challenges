
# Episode 21

Now the problem of the day

write a function that takes an **array of numbers** as arguments and returns **true or false** depending on the following:

* **true** if sum of two numbers in the array  results a number also represented in it
* **false** if there is no two elements do this

**For example**
```
check([1,2,3]); // true as 1+2 =3
check([5,4,6,8,3])  // true as 5+3 =8 all of them represented in the array
check([1,2,4])   // false
check([12,10,16,3,20]) // false 

```
I hope this is clear enough
Good luck guys

# My Solution

Make two nested loops, outer loop for entire arry and the nested loop to lopping over same array to make a sum for each number in the array
except if ( i == j) we use continue to escape it as we don't need to calc same number
else calc two number in the array and make a check if the result included in the array if so return true otherwise return false

```javascript
function check(arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      if(i === j) continue;
      else if (arr.includes(arr[i] + arr[j])) return true;
    }
  }
  return false;
}

console.log(check([5, 4, 6, 8, 3]));
```