# Question 1
```
FUNCTION isConnected(G)
    s = any vertex in G

    // Forward pass
    seen1 = {u: false for all u in G}
    DFS(G, s, seen1)
    FOR each u in G
        IF seen1[u] == false
            RETURN false

    // Reverse pass
    G_rev = reverse all edges in G
    seen2 = {u: false for all u in G}
    DFS(G_rev, s, seen2)
    FOR each u in G
        IF seen2[u] == false
            RETURN false

    RETURN true


def DFS(G, u, seen)
    seen[u] = true
    FOR each v in G.adj[u]
        IF seen[v] == false
            DFS(G, v, seen)
```

# Question 2
```
FUNCTION checkTownHall(G, townHall)

    // Who can townHall reach?
    reachable = {u: false for all u in G}
    DFS(G, townHall, reachable)

    // Who can reach townHall back?
    G_rev = reverse all edges in G
    canReturn = {u: false for all u in G}
    DFS(G_rev, townHall, canReturn)

    // Any node reachable but can't come back = problem
    FOR each v in G
        IF reachable[v] == true and canReturn[v] == false
            RETURN false

    RETURN true


FUNCTION DFS(G, u, visited)
    visited[u] = true
    FOR each v in G.adj[u]
        IF visited[v] == false
            DFS(G, v, visited)
```