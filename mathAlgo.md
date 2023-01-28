# Algo sections

## Math

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

#### Math Recursion

   - Recursion is a problem solving technique where the solution depends on solutions to smaller instances of the same problem
   - Recursion is when a function calls itself
   - Simplify's your solution
   - If you find yourself breaking down your problem into smaller versions of the same problem, recursion is very useful
   - Every recursive solution needs to have a base case--a condition to terminate the recursion
   - Worst for iterative solution
   - May not be faster despite simplified tactic

#### Math

- Fibonacci sequence with recursion

#### Math

- Factorial of a number with recursion

---
