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
   Fib(n)=Fib(nā1)+Fib(nā2)

    
    > Psedo
    
        ```javascript
        1.
        
        
        ```
   Big O


   ##### Tower of Hanoi
- Problem Statement
    >Follow the steps below to solve the problem:

Create a function towerOfHanoi where pass the N (current number of disk), from_rod, to_rod, aux_rod.
Make a function call for N ā 1 th disk.
Then print the current the disk along with from_rod and to_rod
Again make a function call for N ā 1 th disk.
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
   
   #### Chat GPT

- *LAWYER check:

Ā Ā  - contracts

Ā Ā  - nda

- Questions and follow up questions w/ any tech

- Write Code w/ folllow up questions

- computer science questions

- question on code shift enter and write code

- Translate code from Python => JavaScript etc.

- Generates dummy data. id. firstname,lastname, city

- you can ask for data w/o code i.e js or pythonn script

- manipulate data as a class

- Can write mark up language in html & Css and rewrite w/ tailwind css

- javascript interactive w/ html....http request

- axios

- compile X runtime errors

- destructure props parameter =>

#### Improving Prob Solve Refresher

- Visualize examples

- Find an appropriate subproblem

- Find relationships among subproblems

- Generalize the relationship

- Implement by solving subproblems in order

-**Jenny's Lectures

- Patience & Practice || Dont give up

- Theory & Knowledge

- Use Pen and papper

- Try run your code, use debugger

- Do as many questions as you cann|| keep moving on dont stick to 1 prob

- Regularity...consistency

- go from basic to advance

- DSA

- Dont see the solution until solved

- ***Projects Last...Intresting to you

Ā Ā  - No database proj



   
