# Episode 2

## Find next square

Complete **the findNextSquare method** that **finds the next integral perfect square** after the one passed as a parameter. Recall that an integral perfect square is an integer n such that sqrt(n) is also an integer.

If the parameter is itself not a perfect square, then -1 should be returned. You may assume the parameter is positive.

**For example**
```
findNextSquare(4) --> returns 9
findNextSquare(121) --> returns 144
findNextSquare(114) --> returns -1 since 114 is not a square
```

# My Solution

First,get the square root of the number then compare it with same number after use math floor function if it the same then get the square of the next integer by using math pow function.

```javasscript
function findNextSquare(sq) {
  // Return the next square if sq if a perfect square, -1 otherwise
  var num = Math.sqrt(sq);
  if(num === Math.floor(num)) {
      return Math.pow(num+1, 2);
  }
  return -1;
}
```