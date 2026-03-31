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
4. 
