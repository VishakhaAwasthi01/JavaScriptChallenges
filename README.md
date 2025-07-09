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

<details><summary>Solution 2</summary>
 
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
<details><summary>Solution 1</summary>

```js
let sum = 0;
function sumOfNumbers(arr) {
  sum = arr.reduce((acc, curr) => acc + curr, sum);
  return sum;
}
```
 </details>

 <details><summary>Solution 2</summary>

```js
function sumofAllNum(arr){
  let sum = 0;
  for(let i = 0; i< arr.length; i++){
    sum +=arr[i]
  }
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
 
<details><summary>Solution 1</summary>
 
```js
function isPalindrome(str) {
  let lowerCase = str.toLowerCase();
  return lowerCase === lowerCase.split("").reverse().join("");
}
```
 </details> 

 <details><summary>Solution 2</summary>
 
```js
function isPalindrome(str){
  let reverseString=""
  for(let i = str.length-1; i>=0; i--){
    reverseString = reverseString + str[i]
  }
  return str == reverseString;
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
 
<details><summary>Solution 1</summary>
 
```js
const concatArray = (arr) => {
  return [...arr, ...arr];
};
```
 </details> 

 <details><summary>Solution 2</summary>
 
```js
function mergeTwoArray(arr1, arr2){
  let res=[]
  for(let i=0; i<arr1.length; i++){
    if(!arr1[i]){
      res.push(arr2)
    }
    else{
      res.push(arr1[i])
    }
  }
  for(let j=0; j<arr2.length; j++){
    if(!arr2[j]){
      return;
    }
    else{
      res.push(arr2[j])
    }
  }
  return res;
}
```
 </details> 

  ## 13. Missing number in an Array.
### Write a function that given an array of consecutive numbers, returns the missing number.

```js
console.log(missingNumber([1, 2, 3, 5, 6])); //4
```
 
<details><summary>Solution</summary>
 
```js
function missingNumber(arr){
  let totalSum = 0;
  let expectedSum = 0;
  for(let i= 0; i<arr.length; i++){
    totalSum = totalSum + arr[i];
  }
  for(let i=1; i<= arr.length+1; i++){
    expectedSum = expectedSum+ i;
  }
  return expectedSum-totalSum;
}
```
 </details> 

 ## 14. Largest number in an Array.
### Write a function that given an array of numbers, returns the largest number.

```js
console.log(largestNumber([1, 2, 3, 8, 5, 6])); //8
```
 
<details><summary>Solution</summary>
 
```js
function largestNumber(arr){
  let largestNum = 0;
  for(let i=0; i<arr.length; i++){
    if(arr[i]>largestNum)
     { 
       largestNum=arr[i];
     }
  }
  return largestNum;
}
```
 </details> 

 ## 15. Remove duplicates from an Array.
### Write a function that given an array with duplicate values, removes the duplicates and return new array.

```js
console.log(removeDuplicates(["a","b","c","b"])) //["a","b","c"]
```
 
<details><summary>Solution</summary>
 
```js
function removeDuplicates(arr){
  let newArr=[];
  for(let i=0; i<= arr.length; i++){
    let isDuplicate = false;
    for(let j=0; j<=newArr.length; j++ ){
       if(arr[i]=== newArr[j]){
     isDuplicate = true;
         break;
    }
    }
    if(!isDuplicate){
      newArr.push(arr[i])
    }
   
  }
  return newArr;
}
```
 </details> 

  ## 16. Captitalise first letter of each word.
### Write a function that given a string captitalise first letter of each word.

```js
console.log(capitalizeWords("hello world")) //"Hello World"
```
 
<details><summary>Solution</summary>
 
```js
function capitalizeWords(str) {
  return str
    .split(' ')
    .map(word => word.charAt(0).toUpperCase() + word.slice(1))
    .join(' ');
}
```
 </details> 

  ## 17. Find the First Non-Repeating Character
### Write a function that given a string return the first character that does not repeat anywhere in the string.
If all characters repeat, return null
```js
console.log(firstNonRepeatingChar("xxyz")) //"y"
console.log(firstNonRepeatingChar("aabb"))  //null
```
 
<details><summary>Solution</summary>
 
```js
function firstNonRepeatingChar(str) {
  const freq = {};

  for (let char of str) {
    freq[char] = (freq[char] || 0) + 1;
  }

  for (let char of str) {
    if (freq[char] === 1) {
      return char;
    }
  }

  return null; 
}

```
 </details> 

  ## 18. Object Grouping
### Given an object where each key maps to a value with a city, group the keys by city.
```js
const obj ={
    "name" : {
             "city" : "agra",
             "status" : "new"
     },
  "name2" : {
             "city" : "agra",
             "status" : "new"
     },
 
  "name3" : {
             "city" : "delhi",
             "status" : "new"
     },
 
 
  "name4" : {
             "city" : "mumbai",
             "status" : "new"
     },
}
console.log(groupByObject(obj)) // {
   "agra" : [ name, name2 ],
   "delhi" : [name3],
   "mumbai" : [name4]  
}
```
 
<details><summary>Solution</summary>
 
```js
function groupByObject(obj){
let result = {};
for (let key in obj) {
  const city = obj[key].city;
  if (!result[city]) {
    result[city] = [];
  }
   result[city].push(key);
}
  return result
}

```
 </details> 
