---
categories:
  - "[[Classes]]"
course: MATH 345
source:
teacher:
email:
date:
---

## Parameter & Statistic
1. Parameter
	- Whole population
2. Statistic
	- Sample of a population
## Type of Variables
1. Categorical
	- Nominal: No order
	- Ordinal: ORDer or ranked
2. Numerical
	- Discrete: Countable (The Number)
	- Continuous: Within a range, and the number of possible values within that range is ==infinite==
## Description of Data
1. Graphical Methods
	1. `Charts`: Compares different categories
	2. `Histograms`: Groups numbers into a range
	3. `Relative Frequency Distribution`: Shows the relative Frequencies with percentages
	4. `Frequency Curve`: Represents the frequencies of the distribution graphically
## Numerical Descriptive Measures
1. Population Mean
$$\mu = \frac{\sum_{i = 1}^Nx_i}{N}$$
2. Sample Mean
$$\bar{X} = \frac{\sum_{i = 1}^nx_i}{n}$$
==They are basically the same, just different symbols==
### Central Tendency and Dispersion or Variation
1. `Mean`: Average
2. `Mode`: Most popular
3. `Median`: Average of the middle items
==When `Mean = Mode = Median` &rarr; `Normal (Gaussian) Distribution`==
4. Unimodal distribution 
	- ![[{10066267-D193-4989-891B-2E52307C62AC}.png]]
5. Bimodal Distribution
	- ![[{A6E1F08A-18FF-4825-BA76-6FB15140D398} 2.png]]
6. Left-Skewed Distribution:
	- $$Mean < Median$$
7. Right-Skewed Distribution
	 - $$Mean > Median$$
8. Variance
	- Measures the divergence of data from its `Mean`
	- Sample Variance
		$$s^2 = \frac{\sum(x - \bar{x})^2}{n - 1}$$
9. Standard Deviation
	1. Population Standard Deviation 
		 $$s = \sqrt{\text{Sample Varience}}$$ 
	2. Sample Standard Deviation
		- $$\sigma^2 = \frac{\sum(x - \mu)^2}{N}$$
	- Sample Variance and Sample Standard Deviation are squared to avoid positive/negative cancellation, to make the math work nicely, and to connect with models like the normal distribution 
	- Squaring them also allows us to observe the data more precisely &rarr; clarity for errors and outliers
## Normal Distribution
Can be known as a Bell Curve
	- Symmetrical both sides of the `Mean`
	- $$Mean = Median$$
## Probability Sample Space
- Set of all possible outcomes, events
## Probability of An Event
- $$Pr(E) = \frac{\text{Possible Outcomes}}{\text{Total Outcomees}}$$
## Mutually Exclusive Events
- 2  Disjoint Events that can not occur at the same time
## Probability Axioms
$$E \subseteq S $$
1. $$0 \leq P(E) \leq 1$$
2. $$P(S) = 1$$
3. Any countable sequence of disjoint events satisfies $$\sum_{i = 1}^\infty P(E_i)$$
## Combinations
- ==Selection== of objects where the order does not matter
- The number of combinations of n objects taken r at a time is the number of subsets, each of size r, that can be formed from the nn objects
- $$C(n,r) = C_r^n = \binom{n}{r} = \frac{n!}{(n-r)!r!}$$
- $n$ = Number of Items in the set
- $r$ = number of items selected from the set
- $$C_r^n \quad | \quad C(n,r) \quad | \quad nC_r $$
- $\binom{n}{r}$ is ==binomial coefficient== since $(x+y)^n = \sum_{r=0}^n \binom{n}{r}x^{n-r}y^r$
- $$\binom{n}{r} = \binom{n}{n-r}$$
## Permutations
 - Ordered ==arrangement== of object
 - The number of permutations of $n$ objects is $n!$
 1. R-permutation
	 1. Without Repetitions
		 - Ordered arrangement of r distinct objects of a set of $n$ distinct items
		 - $P(n,r)$ or $P_r^n$
		 - $P(n,r) = \frac{n!}{(n-r)!}$
	2. With Repetitions
	     - $n^r$
## Partitions
- A partition of a positive integer n, is a way of writing n as a sum of positive integers
- $n$ distinct objects can be arranged into $k$ distinct groups containing $𝑛_1, 𝑛_2, n_3, … , 𝑛_k$ objects, respectively, where each object appears in exactly one group and $\sum_{i=1}^kn_i = n$
- $$N = \binom{n}{n_1n_2...n_k} = \frac{n!}{n_1!n_2!...n_k!}$$
- That is ==multinomial coefficient== since $(y_1 + y_2 + ... + y_k)^n = \sum\binom{n}{n_1n_2...n_k}y_1^{n_1}y_2^{n_2}...y_k^{n_k}$

## Conditional Probability: Bayes' Theorem
1. Conditional Probability Formula
$$P(A | B) = \frac{P(A \cap B)}{P(B)}$$
	- $P(A|B)$: Probability that A occurs given that B ahs already occurred
$$P(A|B) = \frac{P(B|A)P(A)}{P(B)}$$
2. Independent Events
	1. $$P(A|B) = P(A) \quad | \quad P(B|A) = P(B)$$
3. Mutually Exclusive Events
	1. $$P(A|B) = 0 \quad | \quad P(B|A) = 0$$
4. Chain Rule or ==Multiplication Rule==
5. $$P(A \cap B) = P(A|B) P(B)$$
## Additive Law of Probability
1. Probability of Union of 2 events
	- $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
2. Mutually Exclusive
	- $P(A \cup B) = P(A) + P(B)$
3. **Summary**
	- A & B are 2 events &rarr;
		1. $P(A \cap B) = P(A|B)P(B)$
		2. $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
## Event Composition Method
- Check week 4

## Random Variable
- A variable which represents outcome of an experiment, or an event. 
- A function from possible outcomes onto real numbers
- $X$
1. Discrete Random Variables
	- ![[{336410AB-9859-4147-A912-8BC7716D00CE}.png]]
## Probability Distribution Function
- Probability Distributions = Convenient "modeling" tools
- How do we model a function $f(x) = P(X = x), \forall x$
1. Probability Mass Function
	- The probability distribution of a discrete random variable $X$ is a list of each possible value of $X$ together with the probability that $X$ takes that value in one trial of the experiment.
	- $$P_X(x) = P(X = x) = P(x)$$
	- We call $P_X(x) = P(X = x) = P(x)$ probability distribution function or probability mass function.
	- $F(x)$ finds the probability that a random variable is within a range of values ==(What lies between)==
	- $$P(x_1 < X \leq x_2) = ?$$
2. `Mean`(expected) value of a discrete random variable
	- To find `Mean`, we multiply each possible value of $x_i$ with their corresponding probabilities $$P(X = x_i) = P(x_i), 1 \leq i \leq n$$Then we add all the products
	- $$\mu = E(X) =$$