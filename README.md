# JavaScript Challenges :computer:
## 1. Multiple of 3 and 5.
### Write a solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.

```js
console.log(solution(0)); // 0
console.log(solution(-15)); // 0
```
 
<details><summary>Solution</summary>
 
```js
 
  const solution = (number) => {
  let sum = 0; 
  for (let i = 3; i < number; i++) {
  if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    } 
  }
  return sum;
};
```
 </details> 
 
 
## 2. FizzBuzz
 ### Write a program that prints the numbers from 1 to 100 and for multiples of ‘3’ print “Fizz” instead of the number, for the multiples of ‘5’ print “Buzz” and for multiple of both 3 and 5 print "FizzBuzz". 
                             
<details><summary>Solution</summary>
 
 ```js
 function fizzBuzz() {
  for (let i = 1; i <= 100; i++) {
    let x = i % 3 === 0;
    let y = i % 5 === 0;
    if (x && y) {
      console.log("FizzBuzz");
    } else if (x) {
      console.log("Fizz");
    } else if (y) {
      console.log("Buzz");
    } else {
      console.log(i);
    }
  }
  return i;
}
```
</details> 

## 3. Count Vowel.
### Count the number of vowels in a string.

```js
console.log(countVowels('hello')); // 2
```

<details><summary>Solution 1</summary>

 ```js
function countVowels(str) {
  let vowelArr = ["a", "e", "i", "o", "u"];
  let vowelCount = 0;
  for (let char of str) {
    if (vowelArr.includes(char)) {
      vowelCount++;
    }
  }
  return vowelCount;
}
```
</details> 
<details>
 <summary>Solution 2</summary>
 ```js
 function countVowels(str){
  let count =0;
  let vowels = ['a','e','i','o','u']
  for(let i =0; i < str.length ;i++){
    var chars= str[i].toLowerCase()
    for(let j =0 ;j< vowels.length; j++){
      if(chars===vowels[j]){
        count++;
      }

    }
  }
  return count;
}
 ```
</details>
## 4. Reverse an Array.
### Reverse an array without using javaScript reverse() method.

```js
console.log(reverseArray([1, 2, 3, 4, 5])); //  [5, 4, 3, 2, 1]

```
<details><summary>Solution</summary>

```js
let reversedArray = [];
function reverseArray(arr) {
  for (let i = arr.length - 1; i >= 0; i--) {
    reversedArray.push(arr[i]);
  }
  return reversedArray;
}
```
 </details>
 
## 5. Sum of Array. 
### Calculate the sum of numbers within an array. 

```js
console.log(sumOfNumbers([1, 2, 3, 4, 5])); //15
```
<details><summary>Solution</summary>

```js
let sum = 0;
function sumOfNumbers(arr) {
  sum = arr.reduce((acc, curr) => acc + curr, sum);
  return sum;
}
```
 </details>
 
 ## 6. Filter negative numbers. 
### Create a function that filters out negative numbers from an array.

```js
console.log(filterNegative([0, 1, -2, 3, 4, 5])); //[0, 1, 3, 4, 5]
```
 
<details><summary>Solution</summary>
 
```js
 
let newArr = [];
function filterNegative(arr) {
  newArr = arr.filter((e) => e >= 0);
  return newArr;
}
```
 </details> 

 ## 7. Check Anagram.
### Writ a program to check whether two strings are Anagram of each other.

```js
console.log(isAnagram("LISTEN", "silent")); //true
```
 
<details><summary>Solution</summary>
 
```js
 function isAnagram(str1, str2) {
  let checkStr1 = str1.split("").sort().join("").toLowerCase();
  let checkStr2 = str2.split("").sort().join("").toLowerCase();
  if (checkStr1.length !== checkStr2.length) {
    return console.log("Invalid Input");
  } else if (checkStr1.length === checkStr2.length && checkStr1 === checkStr2) {
    return true;
  }
  return false;
}
```
 </details> 
 
 ## 8. Occurence of duplicates.
### Writ a program to count duplicate elements in an array.

```js
console.log(counts); //{1: 2, 2: 3, 3: 2, 4: 2, 5: 2}
```
 
<details><summary>Solution</summary>
 
```js
 const counts = {};
const sampleArray = [1, 2, 2, 3, 4, 5, 2, 4, 5, 3, 1];
sampleArray.forEach(function (x) {
  counts[x] = (counts[x] || 0) + 1;
});
```
 </details> 
 
 ## 9. Check Palindrome.
### Write a javaScript program to check whether a string is palindrome or not.

```js
console.log(isPalindrome("Madam")); //true
console.log(isPalindrome("game")); //false 
```
 
<details><summary>Solution</summary>
 
```js
function isPalindrome(str) {
  let lowerCase = str.toLowerCase();
  return lowerCase === lowerCase.split("").reverse().join("");
}
```
 </details> 
 
 ## 10. Longest string in an Array.
### Write a javaScript function that accepts an array of strings. Return the longest string.

```js
console.log(longestString(["hi", "hey", "there"])); //there
```
 
<details><summary>Solution</summary>
 
```js
function longestString(arr) {
  let longest = "";
  arr.forEach((item) => {
    if (item.length > longest.length) {
      longest = item;
    }
  });
  return longest;
}
```
 </details> 
 
 ## 11. Flat nested Array.
### Flatten an array without using .flat() method of javaScript.

```js
console.log(flatten([1, [2, [3], 4, [5, 6, [7]]]])); //[1, 2, 3, 4, 5, 6, 7]
```
 
<details><summary>Solution</summary>
 
```js
function flattenArray(nestedArray) {
  return nestedArray.reduce(function(flat, toFlatten) {
    if (Array.isArray(toFlatten)) {
      return flat.concat(flattenArray(toFlatten));
    } else {
      return flat.concat(toFlatten);
    }
  }, []);
}
```
 </details> 
 
 ## 12. Concatenation of Array.
### Write a function that given an integer array arr of length n, returns an array of length 2n where arr is concatenated to itself.

```js
console.log(concatArray([1, 2, 3])); //[1, 2, 3, 1, 2, 3]
```
 
<details><summary>Solution</summary>
 
```js
const concatArray = (arr) => {
  return [...arr, ...arr];
};
```
 </details> 
