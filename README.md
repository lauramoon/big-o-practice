# Big-O Practice
Unit 47.2 Exercises

## Step 1
1. `O(n + 10) => O(n)`
2. `O(100 * n) => O(n)`
3. `O(25) => O(1)`
4. `O(n^2 + n^3) => O(n^3)`
5. `O(n + n + n + n) => O(n)`
6. `O(1000 * log(n) + n) => O(n)`
7. `O(1000 * n * log(n) + n) => O(n * log(n))`
8. `O(2^n + n^2) => O(2^n)`
9. `O(5 + 3 + 1) => O(1)`
10. `O(n + n^(1/2) + n^2 + n * log(n)^10) => O(n^2)`

## Step 2
```
function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
```  
`O(n)`

```
function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}
```
`O(n)`

```
function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}
```
`O(1)`

```
function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
```
`O(n)`

```
function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
```
`O(n^2)`

```
function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
```
`O(n)`

## Part 3
Time complexity:  
1. `n^2 + n` is `O(n^2)
2. `n^2*n` is `O(n^3)`
3. `n^2 + n` is not `O(n)`
4. .indexOf: `O(n)`
5. .includes: `O(n)`
6. .forEach: `O(n)` (or worse, depending on callback)
7. .sort: `O(n * log(n))`
8. .unshift: `O(n)`
9. .push: `O(1)`
10. .splice: `O(n)`
11. .pop: `O(1)`
12. Object.keys(): `O(n)`
13. Space complexity of Object.keys(): `O(n)`
