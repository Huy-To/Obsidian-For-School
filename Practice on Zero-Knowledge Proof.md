

---

## Setup

**System Parameters:**

- $g, h \in \mathbb{Z}_p^*$, both of order $q$

**Public Commitment:** $$c = g^x h^r \pmod{p}$$

**Private Knowledge:** $x, r \in \mathbb{Z}_q^*$

---

## Protocol

|Step|Party|Action|
|---|---|---|
|**Commit**|Prover $P$|Picks random $y, s \in [1..q]$, sends $d = g^y h^s \pmod{p}$|
|**Challenge**|Verifier $V$|Sends random challenge $e \in [1..q]$|
|**Response**|Prover $P$|Sends $u = y + ex \pmod{q}$, $v = s + er \pmod{q}$|
|**Verify**|Verifier $V$|Accepts if $g^u h^v \equiv d \cdot c^e \pmod{p}$|

---

## Proof 1 — Completeness

> **Claim:** If $P$ knows valid $(x, r)$ and follows the protocol honestly, then $V$ always accepts.

**Goal:** Show that the verification equation $g^u h^v \equiv d \cdot c^e \pmod{p}$ holds whenever $P$ is honest.

**Proof:**

Substitute $u = y + ex$ and $v = s + er$ into the left-hand side:

$$g^u h^v = g^{y+ex} \cdot h^{s+er} = g^y \cdot g^{ex} \cdot h^s \cdot h^{er}$$

Regroup:

$$= (g^y h^s)(g^x h^r)^e = d \cdot c^e \pmod{p}$$

This equals the right-hand side exactly. Therefore, an honest prover always passes verification. 

---

## Proof 2 — Soundness

> **Claim:** A cheating prover who does not know valid $(x, r)$ cannot convince $V$ except with negligible probability.

**Proof (by rewinding / knowledge extractor argument):**

Suppose a cheating prover $P^_$ successfully responds to **two different challenges** $e$ and $e'$ (with $e \neq e'$) on the **same commitment** $d$. That is, $P^_$ produces:

- $(u, v)$ satisfying $g^u h^v \equiv d \cdot c^e \pmod{p}$
- $(u', v')$ satisfying $g^{u'} h^{v'} \equiv d \cdot c^{e'} \pmod{p}$

**Divide** the two equations:

$$g^{u - u'} h^{v - v'} \equiv c^{e - e'} \pmod{p}$$

Since $c = g^x h^r$, this becomes:

$$g^{u-u'} h^{v-v'} \equiv g^{x(e-e')} h^{r(e-e')} \pmod{p}$$

Let $\Delta e = e - e' \neq 0 \pmod{q}$, which is invertible in $\mathbb{Z}_q$. Then:

$$\tilde{x} = \frac{u - u'}{\Delta e} \pmod{q}, \qquad \tilde{r} = \frac{v - v'}{\Delta e} \pmod{q}$$

satisfy $g^{\tilde{x}} h^{\tilde{r}} \equiv c^{1} \pmod{p}$, i.e., $c = g^{\tilde{x}} h^{\tilde{r}}$.

So if $P^_$ can answer two different challenges, a knowledge extractor can **rewind** $P^_$ and extract the witness $(x, r)$ efficiently.

Therefore, a cheating prover who does not know $(x, r)$ can answer at most **one** challenge per commitment $d$ — winning only with probability $\frac{1}{q}$, which is negligible.

---

## Proof 3 — Zero-Knowledge

> **Claim:** The protocol reveals no information about the private witness $(x, r)$ beyond the fact that $P$ knows a valid opening of $c$.

**Proof (via simulator):**

We construct a **simulator** $\mathcal{S}$ that, given only the public values $(g, h, p, q, c)$ and the challenge $e$, produces a transcript $(d, e, u, v)$ that is **indistinguishable** from a real interaction — without knowing $(x, r)$.

**Simulator $\mathcal{S}$:**

1. Pick random $u, v \in [1..q]$
2. Compute $d = g^u h^v \cdot c^{-e} \pmod{p}$
3. Output transcript $(d, e, u, v)$

**Verification check on simulated transcript:**

$$g^u h^v \stackrel{?}{\equiv} d \cdot c^e = (g^u h^v \cdot c^{-e}) \cdot c^e = g^u h^v \pmod{p} \checkmark$$

The equation holds by construction.

**Indistinguishability:**

In a **real** transcript:

- $y, s$ are uniform random in $[1..q]$
- $u = y + ex$, $v = s + er$ are therefore also **uniformly distributed** in $\mathbb{Z}_q$ (since $y, s$ are fresh random masks)
- $d = g^y h^s$ is determined by $u, v, e$ via $d = g^u h^v c^{-e}$

In the **simulated** transcript:

- $u, v$ are chosen uniformly at random in $[1..q]$
- $d$ is computed as $g^u h^v c^{-e}$

Both distributions are **identical**: $(d, e, u, v)$ has the same joint distribution in both cases. Therefore, $V$ cannot distinguish a real proof from a simulated one, and no information about $(x, r)$ is leaked.

---

