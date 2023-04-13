# JavaScript Challenges
## 1. Multiple of 3 and 5
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
 ---
 
## 2. FizzBuzz
 ### Write a program that prints the numbers from 1 to 100 and for multiples of ‘3’ print “Fizz” instead of the number, for the multiples of ‘5’ print “Buzz” and for multiple of both 3 and 5 print "FizzBuzz" 
                             
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
 
