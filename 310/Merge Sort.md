---
categories:
  - "[[Algorithm]]"
---

Time: [[O(nlog(n))]] 
- $log(n)$ levels of splitting
- $n$ works merging
Space: [[O(n)]]
- Call stack space: [[O(log(n))]] from recursion depth.
- Auxiliary array(s) for merging: [[O(n)]] extra.
- &rarr; Total Space Complexity =  [[O(log(n))]] + [[O(n)]]  = [[O(n)]] , dominated by [[O(n)]] 
1. In the recursions. We will be splitting the inputs up to $log(n)$ levels of work
2. On each level of work, we are doing linear work [[O(1)]]
3. Recurrence Relation and The actual Complexity gets fine-tuned in terms of the exact operations that we use
4. Worst case
	1. `n - 1` comparisons
5. Recurrence Relation To Find Total Comparisons
	1. I want to recursively define the sub answer of the problem
	2. Example: Worst Case
		1. `n = 8`
		2. T(n)  = T($\frac{n}{2}$) + T($\frac{n}{2}$) + $n - 1$= Left Split + Right Split + How much work we're doing when merging
6. Solving for a concrete mathematical formula
	1. Level * Work
	2. Level 1: $$1(n-1) = 2^0(\frac{n}{2^0}-1)$$
	3. Level 2: $$2(\frac{n}{2} - 1) =2^1(\frac{n}{2^1}-1)$$ 
	4. Level 3: $$4(n-1) = 2^2(\frac{n}{2^2} - 1)$$ 
	5. `i` = level
	6. &rarr; Generic Equation
		$$2^i(\frac{n}{2^i} - 1)$$
	7. Special rule
		1. `r` = base term which is 2
		2. `k` = log(n) - 1, which is the top bound. -1 because the first node does not do any work
		3. if `|r|` > 1  $$\rightarrow \quad \frac{r^{k+1} - 1}{r - 1}$$
		4. 