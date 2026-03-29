- Characteristics are similar to Binary Search Tree, but
-  One side is bigger than the other
	-  Example: Link list

```mermaid

graph TD

    A((Root))

  

    %% Level 1

    A --> B((L))

    A --> C((R))

  

    %% Left subtree gets deeper

    B --> D((L2))

    D --> E((L3))

    E --> F((L4))

    F --> G((L5))

  

    %% Right subtree stays shallow

    C --> H((R2))

```

1. Why Does an Unbalanced BST Become **O(n)**?
	- If the tree becomes **unbalanced**, the height can degrade to:
	- **Worst case height:** n (all values inserted in sorted order, or pathological insertion patterns)
	- Search cost = walk down the entire chain
	- Insert cost = search cost first
	- Delete cost = search + restructure
	&rarr; **O(n)** time, because you may have to traverse every node to reach the bottom.