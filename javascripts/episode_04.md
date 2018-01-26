# Episode 4

Now with the problem of the day!!

**Instructions:**

Write a function that takes a string as an argument and return another string exactly as examples below

**For example**
```
letterManip("abcd");    // "A-Bb-Ccc-Dddd"
letterManip("HeLlo"); // "H-Ee-Lll-Llll-Ooooo"
letterManip("chAt");    // "C-Hh-Aaa-Tttt"
```

Good luck

# My Solution

Here's is my solution
I use **[split](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/split)** to split string into array of chracters then use **[map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)** to convert each chracter to **[upper case](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toUpperCase)** then concat it with repacted same character after convert it to **[lower case](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/toLowerCase)** using new es6 feature **[repeat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/repeat)** and finally join the finall array produced from map function with `-` using **[join](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)** 

```javascript
function letterManip(str){
	return str.split("").map((res, index, arr) => res.toUpperCase()+res.toLowerCase().repeat(index)).join("-");  
}
console.log(letterManip("HeLlo"));
```
