---
categories:
  - Data Structure
---

A searchable collection of key-value entries

1. Operations
	1. `get(k)`: if the map M has an entry with key k, return its associated value; else, return null
	2. `put(k, v)`: insert entry (k, v) into the map M; if key k is not already in M, then return null; else, return old value associated with k
	3. `remove(k)`: if the map M has an entry with key k, remove it from M and return its associated value; else, return null
	4. size(), isEmpty()
2. Performance of a List-Based Map
	1. The unsorted list implementation is effective only for maps of small size or for maps in which puts are the most common operations
