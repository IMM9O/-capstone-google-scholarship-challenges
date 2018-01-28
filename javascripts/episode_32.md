
# Episode 32

Now, the problem of the day :grinning:
## Check Primes

Write a function that takes a number as an argument and return true or false depending on if the number is prime number or not
returns true ===> if the number is prime
returns false ===> if the number is not prime

**For Example**
```
checkPrime(13); // true
checkPrime(4);  // false

```
Good luck guys :grinning:



# My Solution

Here is my solution

```javascript
const checkPrime = num => {
   if(num <= 1) return false;
    for(let i = num-1; i > 1 ; i--){
        if(num%i === 0) return false;
    } 
    return true;
}

console.log(checkPrime(13));
console.log(checkPrime(4));
```
