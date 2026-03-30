The same as Big O but different question

Space Complexity = Input Space + [[Auxiliary Space]]

1. Optimizing

Time &darr; Space &uarr; `or` Time &uarr; Space &darr;

**Question**: How does the ==space usage scale== as input gets ==very large==?

> **Fibonacci Function** `fib(n)` takes [[O(n)]] space because the recursion depth is n & O($2^n$) time because Each call to `fib(n)` makes **two calls**.
> $$Fn = F_{n-1} + F_{n-2}$$
