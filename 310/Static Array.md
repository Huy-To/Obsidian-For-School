---
categories:
  - Data Structure
---

1. Key: Word RAM model of computation
	- Assume w-bit >= $log(n)$
	- In order to process more `n` w-bit has to grow too
	- Memory = array of w-bit words
	- "Array" = Consecutive chunk of memory
&rarr; Array[i] = Memory[addresses(array) + i]
&rarr; Array access is [[O(1)]] time
2. [[O(1)]] per [[get_at(i)]] / [[set_at(i)]] / [[len]]
3. [[O(n)]] per [[build(x)]] / [[iter_seq()[[iter_seq()]]]]