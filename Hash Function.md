To map keys that are not integers in the range from 0 &rarr; N - 1

1. Hash function is used to map general keys to corresponding indexes in a table
	1. Example:
			$$h(x) = x \quad mod \quad N$$
			$h(x)$ = hash value of key `x`
2. Hash function is specified as the composition of two functions:
	1. Hash code:
		1. $h_1:$ keys &rarr; integers
	2. Compression Function
		1. $h_2$: integers &rarr; [0, N - 1]
	3. Conclusion
		1. $h(x) = h_2(h_1(x))$ 