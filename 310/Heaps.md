- A binary tree storing keys at its nodes
- A heap is a data structure that keeps track of an evolving set of objects with ==keys== and can quickly ==identify the object== with the ==smallest key==
 	> If your application requires fast min (max) computation on a dynamically changing set of objects use a heap
- Heap-Order: for every [[internal node]] v other than the root $key(value) \ge key(parent(value))$
- The ==**height of a tree**== is the ==maximum depth== of any node, where the ==**depth**== of a node is the number of ancestors it has.
- 
- Complete Binary Tree
	- Height (`h`) 
	- Number of Nodes (`n`) = $2^{h + 1} - 1$
		- $2^{h + 1} - 1$ is derived from the [[Geometric Series]] with ratio of 2 because $n = 2^0 + 2^1 + 2^2 +..... + 2^h$ 
	- &rarr; $h \approx log_2(n + 1) -1$ 
	- Proof 
		$$n = 2^{h + 1} - 1$$
	- $$\rightarrow n + 1 = 2^{h + 1}$$
	- Take $log_2$ on both side &rarr; $$log_2(n+1) = h + 1 $$
	- $$\rightarrow h = log_2(n + 1) - 1$$
1. Array-based Heap Implementation
	1. For the node at rank (order) $i$
		- The left child is at rank $2i$ 
		- The right child is at rank $2i + 1$
2. Insertion into a Heap
	1. The insertion algorithm consists of three steps:
		- Find the insertion node `z` (the new last node)
		- Store `k` at `z`
		- Restore the heap-order property ==(Upheap | Downheap)==
3. Upheap (Bubble Up)
	1. Algorithm upheap restores the heap-order property by swapping `k` along an ==upward path== from the insertion node
	2. Stops when `k` $\ge$ `parent(root_of_k)`
	3. Since a heap has height [[O(log(n))]], upheap runs in [[O(log(n))]] time
4. Removal from a Heap
	1. The removal algorithm consists of three steps
		- Replace the `root key` with the `key` of the last node `w`
		- Remove `w`
		- Restore the heap-order property
5. Downheap
	1. Algorithm downheap restores the heap-order property by swapping key `k` along a downward path from the root
	2. Stops when `k` <= `values_children(node)`
	3. [[O(log(n))]] time
6. Heap Guarantees
	1. In a heap with 𝑛 objects, the Insert and ExtractMin (or ExtractMax) operations run in 𝑂(log 𝑛) time.
	2. FindMin: given a heap H, return an object with the smallest key [[O(1)]]
	3. Heapify: given objects 𝑥1, 𝑥2, … , 𝑥𝑛 create a heap containing them [[O(nlog(n))]] but there is a smart way to achieve this in [[O(n)]]
	4. Delete: given a heap 𝐻 and a pointer to an object 𝑥 in 𝐻 delete 𝑥 [[O(nlog(n))]]
