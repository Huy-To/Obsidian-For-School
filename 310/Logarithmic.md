Logarithms in Complexities

1. What question does Logarithmic ask?
$$log_2(8) \rightarrow 2^? = 8$$

$$log_{10}(100) \rightarrow 10^? = 100$$

&rarr; It asks what do I need to power the base by to get `x` in $$log_2(x)$$
$$\rightarrow log_2(8) \rightarrow 2^3 = 8$$
$$8 \rightarrow 4 \rightarrow 2 \rightarrow 1 $$

3 steps to go from 8 &rarr; 1 by [[halving]]

2. Definition
		Logarithm is an expression of [[halving]] when it is under the base of `log_function`

3. Where does Logarithm appear in Computer Science?
	1. Any Binary Structure (Binary Trees)
		```mermaid

			graph TD

		    A((Root))

		    A --> B((Left))

		    A --> C((Right))

		    B --> D((Left.Left))

		    B --> E((Left.Right))

		    C --> F((Right.Left))

		    C --> G((Right.Right))
    
		    D --> H((Left.Left.Left))
	
			D --> I((Left.Left.Right))
		```

		`n` = 9 (Number of elements)

		Levels at least = $floor(log_2(9))$

		`Levels` = 1 + levels at least  

		$$\rightarrow Levels = 1 + floor(log_2(9))$$
		$$\rightarrow Levels = 1 + 3.17$$
		$$\rightarrow Levels = 4$$
	2. Unordered Array 
	$$A = [1,3,2,5,7,8,2,9] \quad n = 8$$
		1. How many times can we cut it in half
			```mermaid

				graph TD

			    A([1,3,2,5,7,8,2,9])

			    A --> B([1,3,2,5])

			    A --> C([7,8,2,9])

			    B --> D([1,3])

			    B --> E([2,5])

			    C --> F([7,8])

			    C --> G([2,9])
    
			    D --> H([1])
	
				D --> I([3])
				
				E --> J([2])
				
				E --> K([5])
				
				F --> L([7])
				
				F --> M([8])
				
				G --> N([2])
				
				G --> O([9])
			```

			The number of times we cut this into half is $$log_2(8) = 2^? = 8 \rightarrow ? = 3$$
	3. Ordered Array
	$$B = [1,2,3,4,5,6,7,8] \quad k = 1$$
	$$Indexes = B[i] = [0,1,2,3,4,5,6,7]$$

		&rarr; We automatic know we we can do [[Binary Search]], because the invariants that if we cut the array in half at anypoint, we will have a sorted array

		1. Set the bounds
			1. `Start` = 1
			2. `End` = 8
			3. `MidPoint` = 4 
		2. Compare
			1. $4 \neq 1$
			2. $\rightarrow$ Overshot $\rightarrow$ narrow the bounds
			3. `1+` time narrowing down the bounds
		3. New Bounds
			1. `Start` = 1
			2. `End` = 3
			3. `MidPoint` = 2
		4. Compare 
			1. 1. $2 \neq 1$
			2. $\rightarrow$ Overshot $\rightarrow$ narrow the bounds
			3. `1+` time narrowing down the bounds
		5. New Bounds
			1. `Start` = 1
			2. `End` = 1
			3. `MidPoint` = 1
		6. Compare
			1. $1 = 1$
			2. Found item `k` 
		7. Conclusion
			1. We performed a total of 2 [[halving]] operations to find item `k`
			2. Even if the item is not there, the worst case is that the algorithm will return nothing and still do a third check because $$log_2(8) = 3$$