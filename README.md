# CodeEvolution JS and Data Structures, Pt 1 Fundamentals

## Overview

---

### Algorithm

- A set of well-defined instructions to solve a particular problem

- An algortithm should have inputs and outputs

- Each step should be clear and unambiguous

- Language independent(code in any language)

- World Example: Recipes to make food

- Computer Example:

  - Algorithm to add two numbers:

    - Two numbers 'a' and 'b'

    - Add numbers using '+'

    - return the value

    - Sum of 'a' and 'b'

---

### Measuring performance

`The absolute running time of an algorithm cannot be predicted, since it depends on a number of factors`

- Programming language used to implement the algortithm

- The computer the program runs on

- Other programs running at the same time

- Qality of the operating system

---

### Time & Space complexity

- Time Complexity: Amount of time taken by an algorithm to run, as a function of input size

- Space Complexity: Amount of memory taken by an algorithm to run, as a function of input size

  - No one solution that works every single time

  - Good to know multiple ways to solve a problem

  - Use best solutions

  - If app needs to be quick and has plenty of memory dont worry about space complexity

  - If little memory to work with, pick a solution that is slower and needs less space

---

### Big O notation

- Represent complexity by Asympototic notations

  - Mathematical tools to represent time and space complexity

    1.  BigO Notation - Worst case complexity\*\*\*\*

    2.  Omega Notation - Best case complexity (dont worry wont ask)

    3.  Theta Notation - Average case complexity (dont worry wont ask)

### Time Complexity

- Two important characteristics

  - It is expressed in terms of the input

    ```javascript

         1. function summation(n) {

         2.  let sum = 0;

         3.  for(let i = 1; i<= n; i++) {

         4.   sum += i;

         5.  }

         6.  return sum;

         7. }

    ```

    ```summation(4) = 10

          1 + 2 + 3 + 4 = 10



          n = 4

          line 2 is executed once

          line 4 is executed 4 times

          line 6 executes once

    ```

  - It is focuses on the bigger picture without getting caught up in the minute details

  - Total count executed is 4 plus 2 times shown above

    n + 2

    n = 100 100+2

    n = 1000 1000+ 2

    n = 10000 10000 + 2

    n + 2 = n

    Time Complexity= O(n)- Linear

#### Another example

```javascript

1.function summation(n) {

2.  return (n * (n + 1)) /2;

3.}

```

      line 2 is executed once

      Time Complexity = (1)- Constant



#### Another example

```javascript
for (i = 1; i <= n; i++) {
  for (j = 1; i <= n; j++) {}
}
```

    Time Complexity = O(n^2)- Quadratic<br>

    $3n^2 + 5n +1 == n^2$

#### Another example

```javascript
for (i = 1; i <= n; i++) {
  for (j = 1; i <= n; j++) {
    for (k = 1; k <= n; k++) {}
  }
}
```

    Time Complexity = O(n^3)- Cubic<br>

    $3n^3 + 5n +1 == n^3$

Input size reduces by half every iteration

Time Complexity = O(logn)- Logarithmic

### Space Complexity

- If algorithm does not need extra memory nor depend on size

  - O(1)- Constant

  -\*\*\*Sorting algorithms

- If algorithm space needed grows as size grows

  - O(n)- Linear

- If algorithm space needed grows but not the same as the size grows

  - O(n)- Logarithmic

---

### Algo section Objects Big O

An Object is a collection of key value pairs

```javascript

1. Const person ={

2.   firstName: 'Bruce'

3.   lastName: 'Wayne'

4.}

```

- Insert- O(1)

- Remove- O(1)

- Access- O(1)

- Search- O(n)

- Object.keys()- O(n)

- Object.values()- O(n)

- Object.entries()- O(n)

---

### Algo section Arrays Big O

An array is an ordered collection of values

```javascript

1. const odd = [1, 3, 5, 7, 9]

```

- insert/remove at end- O(n)

- insert/remove at beginning- O(n)

- Access- O(n)

- Search- O(n)

- Push/Pop- O(1)

- Shift/unshift/concat/slice/splice- O(n)

- forEach/map/filter/reduce- O(n)

---

### Algo sections

**Math**

- Fibonacci sequence

  -Problem- Given a number 'n', find the first 'n' elements of the Fibonacci sequence

  -Fibonacci sequence- a sequence in which each number is the sum of the two preceding(before) ones.

  - The first two numbers in the sequence are 0 and 1.

  - fibonacci(2)= [0,1]

  - fibonacci(3)= [0,1,1]

  - fibonacci(4)= [0,1,1,2]

  - fibonacci(7)= [0,1,1,2,3,5,8]

```javascript

1.function fibonacci(n) {

2.  const fib = [0, 1]

3.   for(let i = 2; i < n; i++) {

4.    fib[i] = fib[i-1] + fib[i-2] //adds previous numbers

5. }

6. return fib

7.}

8.

9.console.log(fibonacci(2)) //[0,1]

10.console.log(fibonacci(3)) // [0,1,1]

11.console.log(fibonacci(7)) // [0,1,1,2,3,5,8]



      Fibonaccci(8) = [0,1,1,2,3,5,8,13]



fibonacci(2) = 0 + 1 = 1



add prev two 1 + 1 = 2

add prev two 1 + 2 = 3

add prev two 2 + 3 = 5

add prev two 3 + 5 = 8

add prev two 5 + 8 = 13



      n = 2

      line 3 is executed n times

      BigO = O(n)

```

### Big O Cheat/Guide

- Loop- O(n)

- Nested loops $(O(n^2)$

- Input size reduced by half- O(logn)

---

#### Math

     - Factorial of a number

     - Problem- Given an integer 'n', find the factorial of that integer

     - Factorial of a non-negative int- 'n' detoned n!, is the product of all positive integers less than or equal to 'n'

     - Factorial of Zero is 1

     - factorial(4)= $4 x 3 x 2 x 1= 24$

     - factorial(5)= $5 x 4 x 3 x 2 x 1= 120$

```javascript

1. function factorial(n) {

2.   let result = 1;

3.   for(let i = 2, i <= n; i++) {

4.    result= result * i

5.  }

6.   return result

7.}

8.console.log(factorial(0)) // 1

9.console.log(factorial(1)) // 1

10.console.log(factorial(5)) //120

```

     Big O = O(n)

#### Math

- Prime number

- Problem- Given a natural number 'n' determine if the number is prime or not

- Prime number- a natural number greater than 1 that is not a product of two smaller natural numbers

- isPrime(5)= true(1 x 5 or 5 x 1)

- isPrime(4)= false(1 x 4 or 2 x 2 or 4 x 1)

  ```javascript

  1. function isPrime(n) {

  2.   if(n < 2) {

  3.     return false

  4.    }

  5.   for(let i = 2; i < n; i++) {

  6.     if(n%i === 0) {

  7.      return false

  8.   }

  9.  }

  10.return true

  11.}

  12.

  13.console.log(isPrime(0)) // false

  14.console.log(isPrime(3)) // true

  15.console.log(isPrime(90)) //true

  ```

  Big O = O(n)

##### Optimal Prime Solution

```javascript

1. function isPrime(n) {

2.   if(n < 2) {

3.     return false

4.    }

5.   for(let i = 2; i <= Math.sqrt(n); i++) {

6.     if(n % i === 0) {

7.      return false

8.   }

9.  }

10. return true

11.}

12.

13.console.log(isPrime(1)) // false

14.console.log(isPrime(5)) // true

15.console.log(isPrime(4)) // false

```

     Big O = O(sqrt(n))

#### Math

- Power of 2

- Problem- Given a positive integer 'n' determin if the number is a power of 2 or not

- Power of 2- if there exist an integer 'x' such that 'n' === $2^x$

- isPowerOfTwo(1)= true $(2^0)$

- isPowerOfTwo(2)= true $(2^1)$

- isPowerOfTwo(5)= false

- n = 8

- 8/2= 4(remainder 0)

- 4/2= 2(remainder 0)

- 2/2= 1(remainder 0)

  ```javascript

  1. function isPowerOfTwo(n) {

  2.   if(n < 2) {

  3.     return false

  4.    }

  5.   for(let i = 2; i < n; i++) {

  6.     if(n%i === 0) {

  7.      return true

  8.   }

  9.  }

  10.return false

  11.}

  12.

  13.console.log(isPowerOfTwo(0)) // false

  14.console.log(isPowerOfTwo(4)) // true

  15.console.log(isPowerOfTwo(90)) //true

  ```

  Big O = O(n)

#### Math

- Recursion

#### Math

- Fibonacci sequence with recursion

#### Math

- Factorial of a number with recursion

---

#### Sort

---

#### Search

---

#### Misc. algo & problem solving
