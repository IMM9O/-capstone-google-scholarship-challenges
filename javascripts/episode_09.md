# Episode 9

Now the problem of the day!!

We have number of containers, every container contains a number of oranges, this number can be even or odd, the seller needs to populate the containers on the table but in a certain pattern, he needs to sort them from left to right in a **ascending order but** every two even number oranges containers should have **one odd in between**, odd containers also should be arranged in ascending pattern, if there are no more containers of one type, the seller would continue populating the containers of the type still present in ascending way till there are no more containers.

Write a function that populates the containers in ascending pattern depending on the number of oranges taking in consideration the type of this number even or odd.

**For example**
The final result can be like this

```
[0,3,12,7,22,13,28,17,42,53,50,54,72,76]
```

**You can use sort as you want**
Good luck guys

# My Solution

Here is my solution, First filter out odd/even numbers then sorted it into new array then lopping over even array with start index = 1 and iterator step += 2 and index with start point to 0 for odd number then in each iterator if index for odd number exeed the length of odd array so break the loop if not just add the odd number from the current index into even array using splice method, and after that loop just check if odd arr length greater that even number just push the rest to the even arry and finally return even array.


```javascript
function populatingContainers(arr) {
    const even = arr.filter(res => !(res%2)).sort((p,c) => p > c);
    const odd = arr.filter(res => res%2).sort((p,c) => p > c);
    let index = 0;
    for(let i = 1; i < even.length ; i+=2) {
        if(index >= odd.length) break;
        even.splice(i, 0, odd[index]);
        index++;
    }
    if(odd.length > even.length) {
        even.push(...odd.splice(index, odd.length-1));
    }
    return even; 
}

console.log(populatingContainers([5,27,22,34,24,12,7,3,9,13,17,23]));
```



