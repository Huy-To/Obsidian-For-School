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


FUNCTION TwoSum_NLogN(A, k):
    sorted_A <- MergeSort(A)       // O(n log n)
    left  <- 0
    right <- sorted_A.length - 1

    WHILE left < right DO
        total <- sorted_A[left] + sorted_A[right]

        IF total == k THEN
            RETURN TRUE            // found a valid pair

        ELSE IF total < k THEN
            left <- left + 1       // need a larger sum → move left to right

        ELSE                       // total > k
            right <- right - 1    // need a smaller sum → move right to left

    END WHILE

    RETURN FALSE                   // no pair found


FUNCTION MergeSort(A):
    IF A.length <= 1 THEN
        RETURN A
    mid        <- A.length // 2
    leftHalf   <- MergeSort(A[0 : mid])        //  0 to mid-1
    rightHalf  <- MergeSort(A[mid : A.length]) //  mid to end
    RETURN Merge(leftHalf, rightHalf)


FUNCTION Merge(L, R):
    result <- []
    i <- 0, j <- 0
    WHILE i < L.length AND j < R.length DO
        IF L[i] <= R[j] THEN
            APPEND L[i] TO result
            i <- i + 1
        ELSE
            APPEND R[j] TO result
            j <- j + 1
    // Append any remaining elements
    APPEND L[i:] TO result
    APPEND R[j:] TO result
    RETURN result
	
	
```
