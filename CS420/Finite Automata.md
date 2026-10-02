# The Formal Definition
------------

- A (mathematical) **function** is a mapping of elements in a **domain** set to elements in a **range** set
- A ***finite automation*** is a `mk-DFA`$(Q, \sum, \delta, q_0, F)$
	- mk-DFA = Constructor Function
	- Q = set of states
	- $\sum$ = set of alphabets
	- $\delta$ = $Q \times \sum \rightarrow Q$
	- $q_0 \in Q$ = the innitial state
	- $F \subseteq Q$ = set of accepted states


# Multi - Step Transition Function
--------------

- Base Case $$\hat{\delta}(q,c) = q$$
- Recursive Case $$\hat{\delta}(q,w',w_n) = \delta (\hat{\delta}(q,w'),w_n)$$where $w' = w_1.....W_{n-1}$
