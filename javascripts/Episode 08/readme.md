# Episode 08

HI guys!!!

Now the problem of the day

Write a function that takes a **number** as an argument and returns a **string** represents **random** characters present in a given string, number of characters of string returned should be the same with the number value of the argument.
characters are **just letters**, spaces should not be considered.


**The given string**

```
"Hi all udacity students"
```

Examples
```
numChars(5); // uyhsa
numChars(5); // hadln
numchars(7);  // sdlituh
```
With  every call of of the function, it returns different results(random characters)



# My Solution

First get the string without space
Second generate new array with es6 spread operator then map the res from array to get random characters from string using accessing character in string with array position and the index will be Math.random() multiply be length of string without space

```javascript
const str = "Hi all udacity students";
const numChars = nums => {
     const strWspaces = str.replace(/\s/g, '');
     return [...new Array(nums)].map(res => strWspaces[Math.floor(Math.random() * strWspaces.length)]).join("");
}
console.log(numChars(5));
```