# Question 1

```
FUNCTION partition(arr, lo, hi)
    p = arr[lo]
    i = lo + 1

    FOR j = lo+1 TO hi
        IF arr[j] < p THEN
            swap(arr[i], arr[j])
            i = i + 1
        END IF
    END FOR

    swap(arr[lo], arr[i-1])
    RETURN i - 1
END FUNCTION


FUNCTION quickSort(arr, lo, hi)
    IF lo < hi THEN
        idx = partition(arr, lo, hi)
        quickSort(arr, lo, idx - 1)
        quickSort(arr, idx + 1, hi)
    END IF
END FUNCTION
```

# Question 2

```
FUNCTION hanoi(n, src, aux, dst)
    IF n = 1 THEN
        print "move disc from " + src + " to " + dst
        RETURN
    END IF

    hanoi(n-1, src, dst, aux)   // clear the top stack
    print "move disc from " + src + " to " + dst
    hanoi(n-1, aux, src, dst)   // place top stack on destination
END FUNCTION
```