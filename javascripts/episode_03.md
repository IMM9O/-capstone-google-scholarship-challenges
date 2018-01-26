# Episode 3

Now with the  problem of the day!!!


Write a function that takes **an array as a parameter** and **return string** that represents two words, one represent evey first character in every word in array and the second represent every last characters in array words concatenated together with is in between

**For example**
["Umbrella","drum", "aka",  "cartz", "ini", "toon", "young"];

**Output**: Udacity is amazing.



# My Solution

Here is my solution i use map to return a new array with first and last character then using join to return first and second word 
What i use to get the result
* **[Slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/slice)**
* **[Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)**
* **[Join](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)**

```javascript
var arr = ["Umbrella","drum", "aka", "cartz", "ini", "toon", "young"];
function firstLast(arr) {
    return  arr.map(res => res.slice(0,1)).join("") + " is " + arr.map(res => res.slice(-1)).join("");
}
firstLast(arr);
```
