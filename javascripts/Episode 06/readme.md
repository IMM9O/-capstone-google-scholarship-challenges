# Episode 06

Now, the problem of the day 

**Concatenating mid characters in array of words**

Write a function that takes an **array of words** as an argument and returns a **string** represents every **middle** characters in **odd** number letters words

For example:
```
midChars(["Happy","New","Year","All","Friends"]); // pele
```

Good luck


# My Solution

First **[filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)** array to extract only strings with odd length then using **[map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)** to extract middle character from string and finally using **[join](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)** to concat the final array and preuce it as string  

```javascript
const midChars = arr => arr.filter(res => res.length % 2).map(res => res.substr(res.length / 2, 1)).join("");
console.log(midChars(["Happy","New","Year","All","Friends"])); 
```


