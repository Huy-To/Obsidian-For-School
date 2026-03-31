---
categories:
  - Data Structure
---

```mermaid

	graph LR

    A[1] --> B[2]

    B --> C[3]

    C --> D[4]

    D --> NULL
```

1. Storing a bunch of items in a node
	1. Item
	2. Next [[Pointer]]
2. Keep track of the `head` of the list and the `len`
3. Very efficient at inserting and deleting (O(1) time )
4. [[get_at(i)]] / [[set_at(i)]] takes O(i) time and O(n) worst case
5. To solve [[get_at(i)]] / [[set_at(i)]] we only need to add the `tail` [[Pointer]]