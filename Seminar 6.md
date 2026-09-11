# Question 1
```
FUNCTION iterative_inorder(root, n):
    output = []
    stk = empty stack
    node = root

    WHILE node != NULL or stk is not empty
        while node != NULL
            PUSH node onto stk
            node = node.left

        node = POP from stk
        APPEND node.data to output
        node = node.right

    RETURN output
```

# Question 2
```
FUNCTION TFM(A, n)
    low = 0
    mid = 0
    high = n - 1

    WHILE mid <= high
        IF A[mid] == False
            SWAP A[low] and A[mid]
            low += 1
            mid += 1

        ELIF A[mid] == Maybe
            mid += 1        // already in the right zone

        ELSE:               // A[mid] == True
            SWAP A[mid] and A[high]
            high -= 1
    RETURN A
```