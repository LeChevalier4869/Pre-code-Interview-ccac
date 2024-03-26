## Problem 1: Counting Bits

กำหนดให้ integer n; return array “ans” (length n+1) ที่ในแต่ละ index (0 <= index <= n); ans[i] = จำนวนของ 1 ที่เป็น binary representation ของ i

### Example Inputs

```js
// Example 1
Input: n = 2
Output: [0,1,1]
Explanation:
0 --> 0
1 --> 1
2 --> 10
```

```js
// Example 2
Input: n = 5
Output: [0,1,1,2,1,2]
Explanation:
0 --> 0
1 --> 1
2 --> 10
3 --> 11
4 --> 100
5 --> 101
```

### Code

```js
/*
IDEA and Observation
-- add empty array
-- loop n+1 
-- every time has zero, so if first number is zero give 0 to 0 in array
-- since 1+ has 1 in binary number
-- change decimal to binary
-- find 1 in binary and count
*/

function countBits(n) {
  // TODO: Implement
  let arr = [];
  for(let i=0; i<n+1; i++) {
    if(i === 0) {
      arr.push(0);
    } else {
      arr.push(Number(i).toString(2).match(/1/g).length);
    }
  }
  return arr;
}
```

### Constraints

0 <= n <= 10^5

---

Challenge: ลองหา algorithm ที่ให้คำตอบใน O(n)

## Problem 2: Integer To Roman

Given an integer, convert it to a roman numeral.

![https://cdn1.byjus.com/wp-content/uploads/2020/11/Roman-Numerals-chart.png](https://cdn1.byjus.com/wp-content/uploads/2020/11/Roman-Numerals-chart.png)

### Example Inputs

```js
Input: num = 3
Output: "III"
Explanation: 3 is represented as 3 ones.
```

```js
Input: num = 58;
Output: "LVIII";
Explanation: (L = 50), (V = 5), (III = 3);
```

```js
Input: num = 1994
Output: "MCMXCIV"
Explanation: M = 1000, CM = 900, XC = 90 and IV = 4.
```

### Code

```js
/*
IDEA and Observation
-- the same number is repeating = number + number 
-- number in roman can repeating 3 time no more than
-- lower number is front of higher number = higher - lower
-- opposite if higher number is front of lower number = higher + lower
-- check lower to higher digit
-- create roman number
*/


function intToRoman(num) {
  // TODO: Implement
  const I = 1;
  const V = 5;
  const X = 10;
  const L = 50;
  const C = 100;
  const D = 500;
  const M = 1000;


}
```

### Constraints

1 <= num <= 3999

## Problem 3: Eval

ให้เขียนโปรแกรม เปลี่ยน string ที่มีตัวเลขและ operations + - เลข ให้กลายเป็นผลลัพท์

NOTE: don't allowed to use `eval` function.

### Example Inputs

```js
evaluate("2 + 3 - 1"); // Return 4
```

### Code

```js
/*
IDEA and Observation
-- find operator
-- split at operator
-- trim for delete empty space
-- get number to array
-- evaluate
*/

function evaluate(str) {
  // TODO: Implement
}
```

## Problem 4: Strictly Palindromic Number

Integer n จะเป็น strictly palindromic ถ้าหากว่า ในทุก ๆ base b (โดยที่ b มีค่าตั้งแต่ 2 ถึง n - 2) มี string representation เป็น palindromic.

Return true ถ้า n เป็น strictly palindromic (ถ้าไม่ใช่ก็เป็น false)

> A string is palindromic if it reads the same forward and backward.

### Example Inputs

```js
Input: n = 9
Output: false
Explanation: In base 2: 9 = 1001 (base 2), which is palindromic.
In base 3: 9 = 100 (base 3), which is not palindromic.
Therefore, 9 is not strictly palindromic so we return false.
Note that in bases 4, 5, 6, and 7, n = 9 is also not palindromic.
```

```js
Input: n = 4
Output: false
Explanation: We only consider base 2: 4 = 100 (base 2), which is not palindromic.
Therefore, we return false.
```

### Code

```js
/*
IDEA and Observation
-- I have no idea
*/

function isStrictlyPalindromic(n) {
  // TODO: Implement
}
```

### Constraints

4 <= n <= 10^5
