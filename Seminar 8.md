# Question 1
```
def canPartition(nums):
    total = sum(nums)

    if total % 2 != 0:
        return false

    target = total 
    reachable = {0}       

    for num in nums:
        updated = empty set
        for s in reachable:
            updated.add(s)
            updated.add(s + num)
        reachable = updated

    return target in reachable
```

# Question 2
```
def findContentChildren(greed, cookies)
    sort greed ascending
    sort cookies ascending

    kid = 0
    cookie = 0
    satisfied = 0

    while kid < len(greed) and cookie < len(cookies)
        if cookies[cookie] >= greed[kid]:
            satisfied += 1
            kid += 1       // this kid is happy, move to next
        cookie += 1        // always try the next cookie

    return satisfied
```