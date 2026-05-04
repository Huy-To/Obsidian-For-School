---
categories:
  - "[[Classes]]"
course:
source:
teacher:
email:
date:
---
## Question 1

S = [3, -2, 5, -1, 4, -7, 2, 3]

```
	FUNCTION MaxProfit(A):
		current_sum <- S[0] // 
		best_sum <- S[0]
		
		FOR i = 1 to S.length - 1 DO 
			current_sum <- max(S[i], current_sum + S[i])
			best_sum <- max(current_sum, best_sum)
		END FOR
		RETURN best_sum
```

## Question 2

1. $O(n^2)$
```
A = [8,4,1,6]
k = 10
sum = 0

FOR i = 0 to A.length - 1 DO
	FOR j = i + 1 to A.length - 1 DO
		SUM = A[i] + A[j]
		IF SUM = k DO
			PRINT("YES")
			RETURN (A[i],A[j])
		ELSE DO
			PRINT("NO")
			RETUNR False
```

2. $O(nlogn)$
```
A = [8,4,1,6]
k = 10


FUNCTION SPLIT(A):
	mid = A.length // 2 
	First_Half = A[0 : mid]
	Second_Half = A[mid + 1: -1]
	
	RETURN SPLIT(A)
	
	
```
