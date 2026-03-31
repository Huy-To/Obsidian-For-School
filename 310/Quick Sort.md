---
categories:
  - "[[Algorithm]]"
---
Find the Position for the Pivot by cutting the list into two halves ==Less than== `i` and ==Greater than== `i` &rarr; swap(pivot, i + 1) 
[[O(nlog(n))]] runtime

- Pivot
	- The value within the partitioning space that `I` want to find a position for
	- Item that we want to find the ==Position== for
- Partitioning
	- To choose a pivot
		```
			while L <= R:
				while array[L] <= pivot:
					L++
				while array[R] >= pivot:
					R--
				if L <= R:
					array[L], array[R] = array[R], array[L]
					L++
					R--
			return L
		```
1. How do those parts above play in quicksort

	```
		quicksort(A,I,r){
			if (I<r){
				pivot = partition(A,I,r)
				quicksort(A,I,pivot - 1)
				quicksort(A,pivot + 1, r)
			}
	}
	```

	1. Split the data
	2. Call the partition function
	3. Based on the pivot that we got from partition &rarr; split the data &rarr; Go Left &rarr; Right
2. Partitioning Example
	$$[3, 7, 8, 2, 1]$$
	$$Indexes = [0, 1, 2, 3, 4]$$
	1. Left Bound Value = 3 | Right Bound Value = 1
	2. Left Bound POS = 0 | Right Bound POS = 4
	3. `i` = pointer = 0
		- Remember the last position that an element was placed in, that was less than the pivot
	4. `j` = pointer2 = 4
		1. `j` starts at the Left Bound
		2. To scan from Left Bound & rarr; Right Bound - 1
	5. Start `i` at `index -1` because the `pivot` already takes one space
	6. Compare `j` to `i`
	7. Swapped with `i + 1` if `j < i` 
3. Keys
	1. Worst Case
		1. Pivot = Greatest Item
		2. Pivot = Least Item
		3. &rarr; unevenly chopped the space &rarr; O($n^2$)
	2. Best Case
		1. Pivot = Median Item = $$\frac{LeftBound + RightBound} {2}$$
	3. Example of Worst Case
			$$[9, 8, 6, 7, 1]$$
			$$Pivot = 1$$
			$$\rightarrow \quad n - 1 \quad comparisons \quad as \quad it \quad goes \quad down$$
			$$\rightarrow \quad \sum_{i=1}^{n-1} i$$
			Using Gaussian's Trick$$\rightarrow \quad Gaussian's \quad = \frac{n * (n + 1)}{2}$$
			$$\rightarrow \quad \frac{(n-1) * ((n - 1) + 1)}{2} = \frac{(n-1) * n}{2} $$
			&rarr; This is why O($n^2$) in the worst case
	4. Example of the Best Case
			$$[9, 8, 7, 6, 3]$$
			$$Pivot = 7$$
			&rarr; Similar to [[Merge Sort]]