- Enqueue could also grow the underlying array by a factor of 2
- Operation enqueue throws an exception if the array is full
	```
	  Algorithm enqueue(o)
		if size() = N − 1 then
			signal queue full error
		else
			r <- (f + sz) mod N
		Q[r] <- o
		sz <- (sz + 1)
	  ```
- `f` is the index of the front element
- `sz` is the # of stored elements
- `N` is the size of the array
- The rear element is at index  (f + sz − 1)   mod N, so the next position after it is (f + sz) mod N, which must be the first empty slot as long as `sz < N`