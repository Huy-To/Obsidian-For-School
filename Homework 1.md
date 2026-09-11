# Question 1
```
def reverse(A)
    if len(A) == 1
        return A

    left = 0
    right = len(A) - 1

    while left < right
        temp     = A[left]
        A[left]  = A[right]
        A[right] = temp
        left  += 1
        right -= 1

    return A
```
## Proof
After each iteration `x`, the first `x` and last `x` elements are in their correct reversed positions.
**1. Initialization** — before any swaps, `left = 0` and `right = n-1`. No elements have moved yet, so the invariant holds trivially (zero elements are in place).
**2. Maintenance** — each iteration swaps `A[left]` with `A[right]`, putting both into their final reversed spots, then moves the pointers inward. The invariant holds after every step.
**3. Termination** — the loop stops when `left >= right`, meaning the pointers have crossed the middle. At that point every element has been swapped into its correct position and the array is fully reversed.

# Question 2
1. Preorder
	```
	FUNCTION preorder(node) 
		IF node = null THEN 
			RETURN 
			print node.name 
			preorder(node.left) 
			preorder(node.right)
	```
2. Post order
	```
	FUNCTION postOrder(node) 
		IF node = null THEN 
			RETURN 
			postOrder(node.left) 
			postOrder(node.right) 
			print node.name
	```
3. Inorder
	```
	FUNCTION inOrder(node) 
		IF node = null THEN 
		RETURN 
		inOrder(node.left) 
		print node.name 
		inOrder(node.right)
	```

# Question 3
```
def permutations(n)
    if n == 1:
        return [[1]]       

    prev = permutations(n - 1)   
    result = empty list

    for each perm in prev
        for pos = 0 to len(perm)    
            newPerm = insert n at index pos in perm
            result.add(newPerm)
    return result
```

# Question 4
```
def height(node)
    if node is NULL
        return 0

    left  = height(node.left)
    right = height(node.right)

    return 1 + max(left, right)
```

# Question 8
1. By RightMost: bca baa acb abc bbc acc bac
2. By Middle: baa bac abc bbc bca acb acc
3. By First: abc acb acc baa bac bbc bca

# Question 11
```
def firstOccurrence(A, x)
    left  = 0
    right = len(A) - 1
    found = -1              

    while left <= right
        mid = (left + right) // 2

        if A[mid] == x
            found = mid
            right = mid - 1   // keep searching left for earlier occurrence

        elif A[mid] < x
            left = mid + 1

        else:
            right = mid - 1

    return found
```

# Question 12
```
def commonElements(A, B)
    i = 0
    j = 0

    while i < len(A) and j < len(B)
        if A[i] == B[j]
            print A[i]
            i += 1
            j += 1

        elif A[i] < B[j]
            i += 1    

        else:
            j += 1    
```

# Question 17
```
def majority(A, low, high)
    if low == high
        return A[low]       // single element is the majority

    mid   = (low + high) // 2
    left  = majority(A, low, mid)
    right = majority(A, mid + 1, high)

    if left == right
        return left         

    // check which one actually dominates
    leftCount  = countOccurrences(A, low, high, left)
    rightCount = countOccurrences(A, low, high, right)
    total      = high - low + 1

    if leftCount > total // 2
        return left
    if rightCount > total // 2
        return right

    return NULL             


def countOccurrences(A, low, high, x)
    count = 0
    for i = low to high
        if A[i] == x
            count += 1
    return count
```
## Explanation
- Two Recursive calls on $\frac{n}{2}$ each, plus `countOccurrences` which is O(n)
- $$T(n)=2T\frac{n}{2}+O(n)$$
- By Master Theorem: $a = 2$, $b = 2$, $f(n) = n$. Since $n^{log_22} = n$
- Case 2 O(nlogn)

# Question 18
```
def closestPair(A, low, high)
    if high - low <= 1:
        return infinity        // only one element, no pair exists

    if high - low == 2:
        return A[low + 1] - A[low]   // exactly two elements

    mid    = (low + high) // 2
    dLeft  = closestPair(A, low, mid)
    dRight = closestPair(A, mid, high)

    d     = min(dLeft, dRight)
    cross = A[mid] - A[mid - 1]    

    return min(d, cross)
```

## Explanation
- Each call does O(1) work and splits into two halves:
- $$T(n)=2T\frac{n}{2}+O(1)$$
- By Master Theorem: $a = 2$, $b = 2$, $f(n) = 1$. Since $n^{log_22} = n$ dominates $f(n)$
- Case 1 O(n)