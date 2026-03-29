1. What is Auxiliary Space?
	1. **Auxiliary space** is the _extra_ temporary memory an algorithm needs **in addition to** the memory used to store the input itself.
	2. **Auxiliary Space** = the extra workspace your algorithm uses while running (temporary variables, recursion stack, buffers, etc.)
2. Example 1: Counting elements in an array:

```
	int count = 0;
	int length = sizeof(array) / sizeof(array[0]);
	for (int i = 0; i < length; i++) {
	    count++;
	}
```
- Input: the array (not counted as auxiliary)
- Extra memory: just one `count` variable → **O(1) auxiliary space**

3. Example 2: Recursive Fibonacci
```
function fib(n):

    if n <= 1:

        return n

    return fib(n-1) + fib(n-2)
```
- Uses the _[[recursion stack]]_
- Depth of recursion ≈ n  
    → **[[O(n)]] auxiliary space**

4. Why Auxiliary Space Matters?
	1. It tells you how memory‑efficient your algorithm is **beyond just storing the input**.  
	2. Two algorithms might take the same time but use very different amounts of extra memory.