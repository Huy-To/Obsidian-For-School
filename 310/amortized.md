_Average_ cost per operation over a long sequence, even if some individual operations are more expensive.

- An operation like push on a dynamic array stack is usually O(1), but occasionally O(n) when the array resizes; amortized analysis spreads that rare O(n) cost over many cheap operations, so each counts as O(1) amortized.
- Formally, if a sequence of m operations takes total time T(m), then the amortized cost per operation is T(m)/m, and we say the operation is O(1) (or O(log n), etc.) amortized if this average is bounded that way.