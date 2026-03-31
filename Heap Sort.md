[[O(nlog(n))]] for Best, Worst, Overall

1. Phases
	1. Build Heap
	2. Extraction
2. Equations
	1. Parent: $\frac{i - 1}{2}$ for `i` = index
	2. Left Child: $2* parent +1$
	3. Right Child: $2 * parent + 2$
3. Total Comparisons
	1. Comparisons at each node * numbers of nodes in each level