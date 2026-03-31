---
categories:
  - Data Structure
---

1. Relax constraint that the `size(array)` = `n`
2. Enforce `size(array)` = $\theta(n)$ (`size(array)` must be at least the number of `n`)
3. Maintain $A[i]$ = $X_i$
4. `Insert(x)` &rarr; $A[len] = X$ | $len += 1$ unless ==size(array) = length==
5. If n = size &rarr; allocate new array of $2 * size$  &rarr Resize at n = 1, 2, 4, 8, 16,...
6. &rarr Resize cost = $\theta(1 + 2 + 4 + 8 + 16 +.... + n)$ = $\theta(\sum_{i=1}^{log(n)} 2^i)$ = $\theta(2^{log(n)})$ = $\theta(n)$ because  
	1. $\theta(\sum_{i=1}^{log(n)} 2^i)$ can be interpreted as $\theta(\sum_{i=1}^k 2^i)$
	2. [[Geometric Series]]