

---

## Problem 1
**Proof:**

By hypothesis:

- $p \mid (10a - b)$
- $p \mid (10c - d)$

Consider the linear combination:

$$c(10a - b) - a(10c - d) = 10ac - bc - 10ac + ad = ad - bc$$

Since $p$ divides both $(10a - b)$ and $(10c - d)$, it divides any linear combination of them. Therefore:

$$p \mid ad - bc \qquad$$

---

## Problem 2

**Proof by induction on odd $n$:**

**Base case:** $n = 1$ $$2^1 + 1 = 3, \quad 3 \mid 3$$

**Inductive step:** Assume $3 \mid 2^n + 1$ for some odd $n$. We show $3 \mid 2^{n+2} + 1$:

$$2^{n+2} + 1 = 4 \cdot 2^n + 1 = 4(2^n + 1) - 3$$

Since $3 \mid 4(2^n + 1)$ by the inductive hypothesis, and $3 \mid 3$, we get:

$$3 \mid 4(2^n + 1) - 3 = 2^{n+2} + 1 \qquad$$

---

## Problem 3

$$(2n+1) \mid 1^{2k+1} + 2^{2k+1} + \cdots + (2n)^{2k+1}$$

**Proof:**

Let $S = \displaystyle\sum_{j=1}^{2n} j^{2k+1}$.

Pair the $j$-th term with the $(2n+1-j)$-th term for $j = 1, 2, \ldots, n$:

$$j^{2k+1} + (2n+1-j)^{2k+1}$$

By the algebraic identity for odd exponents $m$: $$a^m + b^m = (a + b)(a^{m-1} - a^{m-2}b + \cdots + b^{m-1})$$

Setting $a = j$, $b = 2n+1-j$, we get $a + b = 2n+1$. Therefore:

$$(2n+1) \mid j^{2k+1} + (2n+1-j)^{2k+1}$$

Since $S$ decomposes into exactly $n$ such pairs:

$$(2n+1) \mid S \qquad$$

---

## Problem 4


**Proof:**

$$ (mq + np) - (mn + pq) = mq - mn + np - pq = m(q-n) - p(q-n) = (m-p)(q-n) $$

Rearranging:

$$mq + np = (mn + pq) + (m - p)(q - n)$$

Since $m - p \mid mn + pq$ by hypothesis, and $m - p \mid (m-p)(q-n)$:

$$m - p \mid mq + np \qquad$$

---

## Problem 5

**Proof:**

Since $x \equiv 1 \pmod{m^k}$, write $x = 1 + t \cdot m^k$ for some integer $t$.

Expanding $x^m$ via the **Binomial Theorem**:

$$x^m = (1 + tm^k)^m = \sum_{j=0}^{m} \binom{m}{j}(tm^k)^j$$

Analyzing each term by its power of $m$:

| $j$      | Term                                                  | Divisible by $m^{k+1}$?    |
| -------- | ----------------------------------------------------- | -------------------------- |
| $0$      | $1$                                                   | No (this is our remainder) |
| $1$      | $t \cdot m^{k+1}$                                     | Yes                        |
| $\geq 2$ | $\binom{m}{j}t^j m^{kj}$, where $kj \geq 2k \geq k+1$ | Yes                        |

Therefore:

$$x^m = 1 + t \cdot m^{k+1} + (\text{terms divisible by } m^{k+1}) \equiv 1 \pmod{m^{k+1}} \qquad$$
