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

#### Math Fibonacci W/Recursion

   - Fibonacci sequence with recursion
   - Problem- Given a number 'n' find the nth element of the Fibonacci sequence
   - Fibonacci sequence is a sequence in which each number is the sum of two preceding ones
   - The first two numbers in the sequence are 0 and 1. (0,1,1,2,3,5,8...)
   - recursiveFibonacci(0)= 0
   - recursiveFibonacci(1)= 1
   - recursiveFibonacci(6)= 8

   - If F represents a function to calaulate the fibonacci number, then
   - Fn = F(n-1) + F(n-2)

    -Base Case:

    - F0 = 0 and F1 = 1
    - F2 = F1 + F0
    - F1 = 1
    - F2 = 1 + 0
    - F2 = 1

   ```javascript
   1.function recursiveFibonacci(n){
   2.  if(n < 2 ) {
   3.     return n
   4.  }
   5. return recursiveFibonacci(n-1) + recursiveFibonacci(n-2)
   6.}
   7.
   8.console.log(recursiveFibonacci(0)) //0
   9.console.log(recursiveFibonacci(1)) //1
   10.console.log(recursiveFibonacci(6)) //8
   11.
   ```
Time Complexity:

- F7 = F6 + F5  
- F6 = F5 + F4 $2^1$
- F5 = F4 + F3 $2^3$
- F4 = F3 + F2 $2^4$
- F3 = F2 + F1 $2^5$
- = $2^n$ = Time Complexity 0($2^n$)

#### Math Factorial W/Recursion

   - Problem- Given an integer 'n', find the factorial of that integer
   - Factorial of a non-negative integer 'n', denoted n!, is the product of all positive integers less than or equal to 'n'.
   - Factorial of zero is 1.
   - factorial(4) = 4*3*2*1 = 24
   - factorial(5) = 5*4*3*2*1= 120
   - 5! = 5*4*3*2*1    5*4!
   - 4! = 4*3*2*1      4*3!
   - 3! = 3*2*1        3*2!
   - 2! = 2*1          2*1!
   - 1! = 1*1          1*0!
   - Base Case: 0! = 1 
   - n! = n*(n-1)!
 

   ```javascript
   1.function recursiveFactorial(n){
   2.  if(n === 0) {
   3.     return 1
   4.  }
   5. return n * recursiveFactorial(n-1)
   6.}
   7.
   8.console.log(recursiveFactorial(0)) //1
   9.console.log(recursiveFactorial(1)) //1
   10.console.log(recursiveFactorial(5)) //120
   11.
   ```   

   ---

 #### Search Algorithm


 ##### Linear Search

   - Problem Statement: Given an array of 'n' elements and a target element 't', find the index of 't' in the array. Return -1 if the target element is not found.

        - arr = [-5,2,10,4,6], t =10 -> Should return 2
        - arr = [-5,2,10,4,6], t =6 -> Should return 4
        - arr = [-5,2,10,4,6], t =20 -> Should return -1

- pseudocode
     - start at the first element in the array and move towards the last
     - at each element check the element is equal to target element
     - if element found, return the index of the element
     - if element not found, return -1

   ```javascript
   1.function lSearch(arr, target) {
   3.  for(let i = 0; i < arr.length; i++){
   4.     if( arr[i] === target) {
   5.        return i
   6.   }
   7. }
   8. return -1
   9.}
   10.
   11.console.log(lSearch([-5,2,10,4,6], 10)) //2
   12.console.log(lSearch([-5,2,10,4,6], 6)) //4
   13.console.log(lSearch([-5,2,10,4,6], 20)) //-1
   14.
   ```
   
Time Complexity is O(n) because we need to iterate n times the array to check and find targets. size of the array determines size of execution. as it increases so does the execution.

   ##### Binary Search

- Problem- Given a sorted array of 'n' elements and a target element 't', find the index of 't' in the array. Return -1 if the target element is not found.
     - Binary search ONLY works on a sorted array
     - Use linear search to sort the array if not sorted then binary search
     - arr = [-5,2,4,6,10], t =10 -> Should return 4
     - arr = [-5,2,4,6,10], t =6 -> Should return 3
     - arr = [-5,2,4,6,10], t =20 -> Should return -1

- Pseudocode

     - If the array is empty, return -1 as the element cannot be found.
     - If the array has elements, find the middle element in the array. If target is equal to the middle element, return the middle element index.
     - If target is less than the middle element, binary search left half of the array.
     - If target is greater than the middle element, binary search right half of the array.
     - finding the middle element is key for searching
 
   ```javascript
   1.function bSearch(arr, target) {
   2.     let leftIndex = 0
   3.     let rightIndex = arr.length -1
   4.    
   5.   while(leftIndex <= rightIndex) {
   6.     let middleIndex = Math.floor((leftIndex - rightIndex) /2)
   7.     if(target === arr[middleIndex]){
   8.       return middleIndex
   9.     }
   10.    if(target < arr[middleIndex]) {
   11.      rightIndex = middleIndex -1
   12.    } else {  
   13.      leftIndex = middleIndex + 1 
   14.    }
   15.  }
   16.  return -1
   17. }
   18. console.log(bSearch([-5,2,4,6,10], 10)) // 4
   19. console.log(bSearch([-5,2,4,6,10], 6))  // 3
   20. console.log(bSearch([-5,2,4,6,10], 20   //-1
   ```

     Big O: our function contains 1 while loop and inside of it we reduce size by half so
     Olog(n), instruction increases as growns and not in same amount

     

 ##### Binary Search w/ Recursion

- Problem- Given a sorted array of 'n' elements and a target element 't', find the index of 't' in the array. Return -1 if the target element is not found.

   - arr = [-5,2,4,6,10], t =10 -> Should return 4
   - arr = [-5,2,4,6,10], t =6 -> Should return 3
   - arr = [-5,2,4,6,10], t =20 -> Should return -1

     - TIPS FOR RECURSIVE SOLUTIONS
     - Figure out how to break down the problem into smaller versions of the same problem
     - Identify the base case for recursion

- Pseudocode

- BREAKDOWN: If the array is empty, return -1 as the element cannot be found.
- BREAKDOWN: If the array has elements, find the middle element in the array. If target is equal to the middle element, return the middle element index.
- BASE CASE: If target is less than the middle element, binary search left half of the array.
- BASE CASE:If target is greater than the middle element, binary search right half of the array.

 

   ```javascript
   1.function recursiveBSearch(arr, target) {
   2.   return search(arr, target, 0, arr.legnth -1)
   3. } 
   4.
   5. function search(arr, target, leftIndex, rightIndex) {
   6.   if( leftIndex > rightIndex) {
   7.   return -1
   8.   }
   9.  
   10. let middleIndex = Math.floor((leftIndex - rightIndex) / 2)
   11.    if(target === arr[middleIndex]) {
   12.       return middleIndex
   13.     }
   14.    
   15.    if(target < arr[middleIndex]) {
   16.      return search(arr, target, leftIndex, middleIndex -1)
   17.    } else {  
   18.      return search(arr, target, middleIndex + 1, rightIndex) 
   19.    }
   20.  }
   21. console.log(bSearch([-5,2,4,6,10], 10)) // 4
   22. console.log(bSearch([-5,2,4,6,10], 6))  // 3
   23. console.log(bSearch([-5,2,4,6,10], 20   //-1
   ```

    BigO:The same function search is getting called over and over and reducing by half making Olog(n)

---

#### Sort Algorithm

   ##### Bubble Sort

   - Compare adjacent elements in the array and swap the positions if they are not in the intended order
   - Repeat the instruction as you step through each element in the array
   - Once you step through the whole array with no swaps, the array is sorted

   - problem: Given an array of integers, sort the array.
   - const arr = [-6, 20, 8, -2, 4]
   - bubbleSort(arr) => Should return [-6, -2, 4, 8, 20]

   -Pseudocode

    -[-6, 20, 8, -2, 4]
    -[-6, 8, 20, -2, 4]  Swap since 20 > 8
    -[-6, 8, -2, 20, 4]  Swap since 20 > -2
    -[-6, 8, -2, 4, 20]  Swap since 20 >  4
    -[-6, 8, -2, 4, 20]
-End of array. Elements swapped? Yes? Repeat the comparison.

    -[-6, 8, -2, 4, 20] 
    -[-6, -2, 8, 4, 20]  Swap since 8 > -2
    -[-6, -2, 4, 8, 20]  Swap since 8 > 4
-End of array. Elements swapped? Yes? Repeat the comparison.

    -[-6, -2, 4, 8, 20]
-End of array. Elements swapped? No? Arrauy is sorted.

- Bubble Sort Solution

     ```javascript
     1. function bSort(arr){
     2.  let swapped
     3.  do {
     4.   swapped = false
     5.   for(let i = 0; i < arr.length -1; i++) {
     6.    if(arr[i] > arr[i+1]) {
     7.     let temp = arr[i]
     8.     arr[i] = arr[i+1]
     9.     arr[i+1] = temp
     10.     swapped = true
     11.    }
     12.   }  
     13. } while(swapped)
     14.}
     15.
     16.const arr = [8, 20, -2, 4, -6]
     17.bSort(arr)
     18.console.log(arr) // [-6,-2,4,8,20]
     ```

    Big O of bubble sort has a for loop and do while loop. Big O is quadratic time complexity
    Big O is $O(n)^2$
    
    
