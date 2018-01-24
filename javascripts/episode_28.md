
# Episode 28    

Now the problem of the day

## Word recognition
Write a function that **takes two arguments** the first is an **array of words** and the second is a **word** and returns **array of words** containing **all words** that includes **all letters** of the second argument in the **same order** of letters, your program should be able recognize the word in a **mess of letters**

**For example**
```
wordRecog(["true","trea","track","utre"],"true") //["true"]
wordRecog(["drows","words","wtorssds","downward"],"word")// ["words","wtorssds"]
```

Good luck guys


# My Solution

Here is My solution looping over array using forEach inside the loop evaluate if the string is same as the current item in iterator after filter out any character not included in the string if it true the push it to final array otherwise do nothing and finally return the array.

```javascript

function wordRecog(arr, str) {
    const final = [];
    arr.forEach(element => {
        if (element.split("").filter(c => str.includes(c)).join("") === str) final.push(element);
    });
    return final;
}

console.log(wordRecog(["true","trea","track","utre"],"true")); //["true"]
console.log(wordRecog(["drows","words","wtorssds","downward"],"word")); // ["words","wtorssds"]

```

