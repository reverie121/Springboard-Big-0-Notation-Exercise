# Big O Notation Practice

## Step One: Simplifying Expressions
1. 0(n)
2. 0(n)
3. 0(1)
4. 0(n^3 + n^2)
5. 0(n)
6. 0(n log n)
7. 0(n log n + n)
8. 0(2^n + n^2)
9. 0(1)
10. 0(n + n^(1/2) + n^2 + n * log(n)^10)

---

## Step Two: Calculating Time Complexity

function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}  
**Time Complexity: O(n)**


function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(i);
  }
}  
**Time Complexity: O(n)**

function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(i);
  }
}  
**Time Complexity: O(1)**

function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}  
**Time Complexity: O(n)**

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
}  
**Time Complexity: O(n^2)**

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
**Time Complexity: O(n)**

---

## Part 3 - short answer

1. False
2. True
3. False
4. O(n)
5. O(n)
6. O(n)
7. O(n)
8. O(n)
9. O(1)
10. O(n)
11. O(1)
12. O(n)
13. O(n)