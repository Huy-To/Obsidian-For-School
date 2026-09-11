# Question 1
| State (A, B, C) | Reached By            | Contains 2?  |
| --------------- | --------------------- | ------------ |
| (0, 7, 4)       | Start                 | No           |
| (7, 0, 4)       | Pour B→A              | No           |
| (4, 7, 0)       | Pour C→A              | No           |
| (7, 4, 0)       | Pour C→B from (7,0,4) | No           |
| (4, 3, 4)       | Pour B→C from (4,7,0) | No           |
| (3, 4, 4)       | Pour A→C from (7,4,0) | No           |
| (8, 3, 0)       | Pour C→A from (4,3,4) | No           |
| (3, 7, 1)       | Pour A→B from (3,4,4) | No           |
| (8, 0, 3)       | Pour B→C from (8,3,0) | No           |
| (9, 0, 2)       | Pour B→C from ...     | **c = 2 **   |
| **(2, 7, 2)**   | Pour A→B from (9,0,2) | **b=2, c=2** |
Algorithm: BFS
# Question 2
```
FUNCTION computeTwoDegree(G):
    // Step 1: compute degree of every node — O(V + E)
    FOR each node u in G
        deg[u] = length of G.adj[u]

    // Step 2: for each node, sum degrees of its neighbors — O(V + E)
    FOR each node u in G
        twodegree[u] = 0
        FOR each neighbor v in G.adj[u]
            twodegree[u] += deg[v]

    RETURN twodegree
```
