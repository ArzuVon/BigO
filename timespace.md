# Time & Space complexity

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

    1. BigO Notation - Worst case complexity\*\*\*\*

    2. Omega Notation - Best case complexity (dont worry wont ask)

    3. Theta Notation - Average case complexity (dont worry wont ask)

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


## [Worst Case](https://www.geeksforgeeks.org/worst-average-and-best-case-analysis-of-algorithms/)

> Worst Case Analysis (Mostly used) 
In the worst-case analysis, we calculate the upper bound on the running time of an algorithm. We must know the case that causes a maximum number of operations to be executed. For Linear Search, the worst case happens when the element to be searched (x) is not present in the array. When x is not present, the search() function compares it with all the elements of arr[] one by one. Therefore, the worst-case time complexity of the linear search would be O(n).

## Worst Case Analysis: 
Most of the time, we do worst-case analyses to analyze algorithms. In the worst analysis, we guarantee an upper bound on the running time of an algorithm which is good information. 

### Example

  ```javascript
  // javascript implementation of the approach

	// Linearly search x in arr. If x is present then
	// return the index, otherwise return -1
	function search(arr , n , x) {
		var i;
		for (i = 0; i < n; i++) {
			if (arr[i] == x) {
				return i;
			}
		}
		return -1;
	}

	/* Driver program to test above functions */
	
		var arr = [ 1, 10, 30, 15 ];
		var x = 30;
		var n = arr.length;
		document.write(x+" is present at index "+ search(arr, n, x));
  ```
  
#### Time Complexity Analysis: (In Big-O notation)

- Best Case: O(1), This will take place if the element to be searched is on the first index of the given list. So, the number of comparisons, in this case, is 1.
- Average Case: O(n), This will take place if the element to be searched is on the middle index of the given list.
- Worst Case: O(n), This will take place if:
- The element to be searched is on the last index
- The element to be searched is not present on the list
