# JavaScriptChallenges
## Multiple of 3 and 5
### 1.Write a solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in.
 e.g. console.log(sumOfMultiples(10)) // 23;
 
> Solution
   > const sumOfMultiples = (number) => {
  let sum = 0;
  for (let i = 3; i < number; i++) {
    if (i % 3 === 0 || i % 5 === 0) {
      sum += i;
    }
  }
  return sum;
};
