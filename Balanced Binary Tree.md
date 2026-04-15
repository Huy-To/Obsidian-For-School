 $$|Left Subtree Height - RightSubTreeHeight| \quad \leq 1$$

1. Approach
	1. At each node get `Left` & `Right` subtree's height
	2. Drill down recursion, as we come up we care about 2 things
		1. A node's height in the tree
		2. If a node's `Left` & `Right` subtrees are balanced