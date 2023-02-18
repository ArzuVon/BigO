# Misc. algo & problem solving
## [How To Problem Solve 101](https://www.freecodecamp.org/news/how-to-solve-coding-problems/)

      1. Understand the problem
      2. Make a plan
      3. Carry out the plan
      4. look back/revise
   ---

 #### Misc. algo & problem solving
   
   ##### Misc Problems
   
 - Problem Statement
    
    
    > Psedo
    
        ```javascript
        1.
        
        
        ```
        Big O

   ##### Cartesian Product
      - Problem Statement
         - Approach 1:
            - Create a new array.
            - Traverse the first array by outer loop and second array by inner loop.
            - In the inner loop, Concatenate the first array element with the second array element and push it in a new array.
        - Approach 2:
          - Create a new array.
          - The same approach is followed here, for every element of the first array, every element of the second array is concatenated and pushed to the new array with the help of .apply() and .map() method.
     > Psedo
     > 

           ```javascript
           1.


           ```
      Big O


   ##### Climbing Staircase
   - Problem Statement
   - This is actually a fibonacci sequence. Each number in a fibonacci sequence is the sum of the two preceding ones, starting from 0 and 1.
   0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
   Fib(n)=Fib(n−1)+Fib(n−2)

    
    > Psedo
    
        ```javascript
        1.
        
        
        ```
   Big O


   ##### Tower of Hanoi
- Problem Statement
    >Follow the steps below to solve the problem:

Create a function towerOfHanoi where pass the N (current number of disk), from_rod, to_rod, aux_rod.
Make a function call for N – 1 th disk.
Then print the current the disk along with from_rod and to_rod
Again make a function call for N – 1 th disk.
    <script>
// javascript recursive function to
// solve tower of hanoi puzzle
function towerOfHanoi(n, from_rod, to_rod, aux_rod)
{
		if (n == 0)
		{
			return;
		}
		towerOfHanoi(n - 1, from_rod, aux_rod, to_rod);
		document.write("Move disk " + n + " from rod " + from_rod +
		" to rod " + to_rod+"<br/>");
		towerOfHanoi(n - 1, aux_rod, to_rod, from_rod);
	}

	// Driver code
	var N = 3;
	
	// A, B and C are names of rods
	towerOfHanoi(N, 'A', 'C', 'B');

// This code is contributed by gauravrajput1
</script>

    > Psedo
    
        ```javascript
        1.
        
        
        ```
   Big O
   >Time complexity: O(2N), There are two possibilities for every disk. Therefore, 2 * 2 * 2 * . . . * 2(N times) is 2N
Auxiliary Space: O(N), Function call stack space


   ##### Further learning
- Problem Statement
    
    
    > Psedo
    
        ```javascript
        1.
        
        
        ```
   Big O

---

   ##### Array

   ##### Object

   ##### Set

   ##### Map

   ##### Stack

   ##### Queue

   ##### Circular Queue

   ##### Linked List

   ##### Doubly Linked List

   ##### Hash Table

   ##### Tree

   ##### Binary Search Tree

   ##### Graph
