# Section 4.3 -- Primes

_definition_: A natural number $p > 1$ is called a __prime number__ if it is divisible only by itself and $1$.

A number $n > 1$ that is not prime is __composite__.

__Note__: $1$ is neither prime nor composite (it is "the unit").

### Lemma

Given a natural number $n > 1$,

$$
    \exists \text{ a prime } p \text{ such that } p \mid n.
$$

#### Proof

> By Contradiction

Suppose to the contrary that there are natural numbers that are not divisible by a prime. By the Well-Ordering principal there is a smallest such natural number, $n$. If $n$ is prime,

$$
    n \mid n
$$

which is a contradiction. If $n$ is composite, then there exist $k \in \mathbb N$ where  $0 < k < n$ is not prime where,

$$
    k \mid n
$$

but since $n$ the smallest natural number that is not divisible by a prime,

$$
    p \mid k
$$

so $p \mid n$ which is a contradiction.

$$
    \therefore p \mid n
$$

## Fundamental Theorem of Algebra

Every natural number $n > 1$ can be written as the product of prime powers in exactly one way (up to ordering). That is, for any $n > 1$, we can write $n$ as a __prime factorization__.

$$
    n = p_1^{e_1} p_3^{e_2} p_3^{e_3}... p_k^{e_k}
$$

where $p_1$ is prime, and $e_i \ge 1$.

**Examples**

$$
\begin{aligned}
    6 &= 2^1 \cdot 3^1 = 3^1 \cdot 2^1 \newline
    18 &= 2^1 \cdot 3^2 \newline
    20 &= 2^2 \cdot 5 \newline
    7 &= 7 \newline
\end{aligned}
$$

### Consequences of $\mathcal{FTA}$

If $n = p_1^{e_1} p_3^{e_2} p_3^{e_3}... p_k^{e_k}$ then,

$$
    p_i \mid n
$$

for $1 \le i \le k$.

If $n = p_1^{e_1} p_3^{e_2} p_3^{e_3}... p_k^{e_k}$ and,

$$
    d \mid n
$$

then,

$$
    d = p_1^{d_1} p_3^{d_2} p_3^{d_3}... p_k^{d_k}
$$

where $0 \le d_i \le e_i$.

If $p$ is prime and $p \mid a^2$, then,

$$
    p \mid a
$$

and in fact $p^2 \mid a^2$.

If $a = kb$, then $a$ and $kb$ have the same decomposition.

**Example**

$$\begin{aligned}
    126 &= 2 \cdot 3^2 \cdot 7 \newline
    (2 \cdot 3 \cdot 7) &\mid 126 \newline
    (2 \cdot 3^3) &\nmid 126 \newline
\end{aligned}$$

### Proposition

For a prime $p$, if $p \mid a \cdot b$, then,

$$
    p \mid a \text{ or } p \mid b
$$

#### Proof

If $p \mid a$ then we're done.

If $p \nmid a$ then , the $\gcd(p,a) = 1$, so by yesterday's corollary $p \mid b$.


### Theorem

There are infinitely many primes.

#### Proof

Suppose to the contrary that there are only a finite number of primes, call them,

$$
    p_1, p_2, ... p_n.
$$

Consider,

$$
    N = p_1p_2...p_n + 1
$$

since $N$ is larger than any $p_i$, $N$ is not prime ($N$ is composite). By the Lemma some prime divides $N$, since $p_1,p_2,...,p_n$ are all the primes,

$$
    p_i \mid N
$$

where $0 \le i \le n$. So,

$$\begin{aligned}
    N &= p_i(p_1 p_2...p_{i-1}p_{i-2}...p_n) + 1 \newline
    &= p_i m + \underbrace{1}_r \newline
\end{aligned}$$

where $m = p_1 p_2...p_{i-1}p_{i-2}...p_n$. So when we divide $N$ by $p_i$ we have a remainder of $1$. So $p_i \mid n$ which a contradiction.

$$
    \therefore \text{There are infinitely many primes.}
$$

## Paired Primes

Like,

$$
\begin{aligned}
    3&,5 \newline
    11&,13 \newline
    17&,19 \newline
\end{aligned}
$$

theres a conjecture that there are infinitely many paired primes. However it has yet to be proven.

### Proposition (Test for Primality)

If $n > 1$ is composite,

then we know it has a prime divisor $p$ between $1 \le p \le \sqrt{n}$.

**Example**

Is $353$ prime?

**_Solution_**

$\sqrt{353} = 18.7$ so we need to test,

$$
    2,3,5,7,11,13,17
$$

Since none of these number divide $353$, $353$ is prime.

## Finding GCD using Prime Factorizations

If,

$$
    a = p_1^{a_1} p_2^{a_2} p_3^{a_3}... p_n^{a_n}
$$

for $a_i \ge 0$ and,

$$
    b = p_1^{b_1} p_2^{b_2} p_3^{b_3}... p_n^{b_n}
$$

for $b_i \ge 0$ then,

$$
    \gcd(a,b) = p_1^{\min(a_1,b_1)} p_2^{\min(a_2,b_2)} p_3^{\min(a_3,b_3)}... p_n^{\min(a_n,b_n)}
$$

and,

$$
    \text{lcm}(a,b) = p_1^{\max(a_1,b_1)} p_2^{\max(a_2,b_2)} p_3^{\max(a_3,b_3)}... p_n^{\max(a_n,b_n)}
$$



**Example**

Find $\gcd(270,1575)$. Using the $\mathcal{FTA}$,

$$\begin{aligned}
    270 &= 2 \cdot 3^3 \cdot 5 \newline
    1575 &= 3^2 \cdot 5^2 \cdot 7. \newline
\end{aligned}$$

So,


$$\begin{aligned}
    \gcd(270,1575) &= 3^2 \cdot 5\newline
    &= 45 \newline
\end{aligned}$$

and,


$$\begin{aligned}
    \text{lcm}(270,1575) &= 2 \cdot 3^3 \cdot 5^2 \cdot 7 \newline
    &= 9450 \newline
\end{aligned}$$
