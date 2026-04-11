---
categories:
  - "[[Classes]]"
course: CS310
source:
teacher:
email:
date:
---


# Table of Contents

--- 
# Topics
## Big O 

 **The Question**: How does ==algorithm speed== scale when input scales becoming ==very large==?

<svg id="chart" width="900" height="600" xmlns="http://www.w3.org/2000/svg"><path d="M50 450 L 50 0 L 800 0 L 800 450 Z" fill="#ff8989"></path><path d="M50 450 L 800 0 L 800 450 Z" fill="#FFC543"></path><path d="M50 450 L 800 450 L 800 330 Z" fill="yellow"></path><path d="M50 450 L 800 450 L 800 410 Z" fill="#C8EA00"></path><path d="M50 450 L 800 450 L 800 440 Z" fill="#53d000"></path><path d="M50 0 L 50 450 L 800 450" fill="transparent" stroke="black" stroke-width="2"></path><path d="M50 448 L 800 448" fill="transparent" stroke="black" stroke-width="2"></path><text x="700" y="438" fill="green">O(log n), O(1)</text> <path d="M50 450 L 800 400" fill="transparent" stroke="black" stroke-width="2"></path><text x="760" y="390" fill="black">O(n)</text> <path d="M50 450 Q 400 350, 800 150" fill="transparent" stroke="black" stroke-width="2"></path><text x="630" y="190" fill="black">O(n log n)</text> <path d="M50 450 Q 180 380, 250 0" fill="transparent" stroke="black" stroke-width="2"></path><text x="260" y="30" fill="black">O(n^2)</text> <path d="M50 450 C 100 430, 120 350, 120 0" fill="transparent" stroke="black" stroke-width="2"></path><text x="125" y="20" fill="black">O(2^n)</text> <path d="M50 450 C 80 450, 80 350, 80 0" fill="transparent" stroke="black" stroke-width="2"></path><text x="80" y="20" fill="black">O(n!)</text> <text x="0" y="0" transform="translate(30 230) rotate(-90)" style="dominant-baseline: middle; text-anchor: middle; font-size:20px; color: #555; font-size:20px; color: #555; font-style: italic;" fill="white">Operations</text> <text x="0" y="0" transform="translate(420 470)" style="dominant-baseline: middle; text-anchor: middle; font-size:20px; color: #555; font-style: italic;" fill="white">Elements</text></svg>

We know that no matter how far [[O(n)]] goes, it is bounded below [[O(nlog(n))]], and above [[O(log(n))]] & [[O(1)]].

--- 

 1. What is n?
	1. String Length?
	2. Total tree Nodes?
	3. Array Size?
	- Depends on the input and the operations
	- Example: Input = 2 strings &rarr; Then we have an `m` & `n`
		- `m` = s1.length
		- `n` = s2.length
	&rarr; O could be anything like O(`m + n`), O(`m * n`). It depends on what the problem is
2. Common Runtime Complexity (O)
 
The tail behavior of the Big O is the most important thing to consider, because it shows the behavior of an algorithm as it scales




---

## Space Complexity

The same as Big O but different question

Space Complexity = Input Space + [[Auxiliary Space]]

1. What counts as space
	1. **Extra** memory beyond the input itself
		- Extra variables (counters, pointers, temp values).
		- Extra data structures (arrays, lists, hash maps, stacks, queues).
		- Extra call stack frames from recursion 
2. Space depends on Depth
3. Optimizing

Time &darr; Space &uarr; `or` Time &uarr; Space &darr;

**Question**: How does the ==space usage scale== as input gets ==very large==?

> **Fibonacci Function** `fib(n)` takes [[O(n)]] space because the recursion depth is n & O($2^n$) time because Each call to `fib(n)` makes **two calls**.
> $$Fn = F_{n-1} + F_{n-2}$$



## [[Logarithmic]]
## [[Asymptotic Notations]]

## [[Static Array]]

## [[Linked List]]

## [[Dynamic Array]]

## [[Amortization]]

## [[Stacks]]

## [[Queue]]

## [[Total Order]]
- Every pair of such keys must be comparable according to a total order 
- Each entry is a pair (key, value)

## [[Priority Queue ]]

## [[Heaps]]

## [[Heap Sort]]
## [[Tree]] 

## [[Balanced Binary Tree]]

## [[Binary Search]]

## [[Maps]]

## [[Hash Function]]
## [[Hash Tables]]

## [[Bloom Filters]]

## [[Union Find]]

## [[Merge Sort]]

## [[Inversions]]

## [[Quick Sort]]

## [[Insertion Sort]]

## [[Counting Sort]]

## [[Radix Sort]]

## [[Bucket Sort]]

## [[Bubble Sort]]
## [[Breadth First Search]]

## [[Depth First Search]]