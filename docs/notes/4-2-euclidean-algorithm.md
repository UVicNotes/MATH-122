
# Section 4.2 Divisibility & the Euclidean Algorithm

__definition__: For integers $a$ and $b$, we say $a$ divides $b$, if $\exists k in \mathbb Z$ such that,

$$
    b = a \cdot k
$$

this is denoted $a \mid b$. In this case we can say $a$ is a __divisor__ or __factor__ of $b$. We can also say $b$ is __divisible__ by $a$.

If $a$ _is not_ a divisor of $b$, then we write,

$$
    a \nmid b
$$

Alternatively,

$$
    a \mid b \iff \frac{b}{a} \in \mathbb Z
$$

### Example

$$ %Aligned
\begin{aligned}
    3 &\mid 12 &\text{since } 12 = 3(4) \newline
    7 &\mid 7  &\text{since } 7 = 7(1) \newline
    -5 &\mid 5 &\text{since } -5 = 5(-1) \newline
\end{aligned}
$$

### Facts

For any integer $n$,

* $n \mid 0 $ since $0 = n(0)$
* $0 \nmid n$ since $\not\exists k$ such that $0 = nk$

### Proposition

Let $a,b,c \in \mathbb Z$. If $a \mid b$ and $b \mid c$ then $a \mid c$.

#### Proof

Since $a \mid b$, then $\exists k \in \mathbb Z$ such that $b = ak$. Likewise, since $b \mid c$, $\exists m \in \mathbb Z$ such that $c = bm$. So,

$$
    c = bm = (ak)m = a(km)
$$

and $km \in \mathbb Z$ since the integers are closed under multiplication. Therefore, since $c = a(km)$, $a \mid c$.

### Proposition 1

Let $a,b \in \mathbb Z$. If $a \mid b$ and $a \mid c$ the we can say,

$$
    a \mid (bx + cy)
$$

for _any_ $x,y \in \mathbb Z$.

#### Proof

Since $a \mid b$, $\exists k \in \mathbb Z$ such that $b = ak$ and since $a \mid c$, $\exists m \in \mathbb Z$ such that $c = am$. Let $x,y \in \mathbb Z$,

$$ %Aligned
\begin{aligned}
    bx + cy &= (ak)x + (am)y \newline
    &= a(kx) + a(my) \newline
    &= a(kx + my) \newline
\end{aligned}
$$

since the integers are close under addition and multiplication, $kx + my \in \mathbb Z$. Therefore $a \mid bx + cy$.

## Common Divisors

_definition_: Let $a$ and $b$ be integers, such that they are not both zero. Then $g$ is the __greatest common divisor__ of $a$ and $b$ if,

1. $g \mid a$ and $g \mid b$ ("common divisor")
2. if $c$ is also a common divisor, $g \ge c$ ("greatest")

and we write $g = \gcd(a,b)$

### Example

Find $\gcd(6,15)$.

#### Solution

List the divisors,

* $6: 1,2,3,6$
* $15: 1,3,5,15$

So $\gcd(6,15) = 3$

### Facts

For any integer $a$,

* $\gcd(a,0) = |a|$
* $\gcd(a,1) = 1$
* If $a \mid b$, then $\gcd(a,b) = |a|$

### Proposition 2

If $a,b \in \mathbb Z$, not both zero, and $a = bq + r$ (for some $q,r \in \mathbb Z$) then $\gcd(a,b) = \gcd(b,r)$.

#### Proof

> We'll show that $\gcd(a,b) \le \gcd(b,r)$ and $\gcd(b,r) \le \gcd(b,r)$

We know, $\gcd(a,b) \mid a$ and $\gcd(a,b) | b$ so we can say,

$$
    \gcd(a,b) \mid ax + by
$$

and we'll let $x = 1$ and $y = -q$,

$$ %Aligned
\begin{aligned}
    \gcd(a,b) &\mid a + b(-q) \newline
\end{aligned}
$$

note that $r = a - bq$, so,

$$
    \gcd(a,b) \mid r
$$

> So right now we know $\gcd(a,b) \le \gcd(b,r)$

We also know $\gcd(b,r) \mid b$ and $\gcd(b,r) \mid r$ so,

$$
    \gcd(b,r) \mid qb + 1r
$$

since $qb + r = a$,

$$
    \gcd(b,r) \mid a
$$

$$
    \therefore \gcd(b,r) \le \gcd(b,a)
$$

and $\gcd(a,b) = \gcd(b,r)$.


## The Euclidean Algorithm for find GCD

Let $a,b \in \mathbb N$, with $b < A$. To find the $\gcd(a,b)$, write,

$$ %Aligned
\begin{aligned}
    a &= bq_1 + r_1 \newline
    b &= r_1q_2 + r_2 \newline
    r_1 &= r_2q_3 + r_3 \newline
    r_2 &= r_3q_4 + r_4 \newline
    &~~\vdots \newline
    r_{i-2} &= r_{i-1}q_i + \underset{r_i}0 \newline
\end{aligned}
$$

and $\gcd(a,b) = r_{i-1}$.

### Example

Find $\gcd(88,72)$.

#### Solution

$$ %Aligned
\begin{aligned}
    \underset{a}88 &= \underset{b}72 \cdot \underset{q}1 + \underset{r}16 \newline
    72 &= 16 \cdot 4 + 8 \newline
    16 &= 8 \cdot 2 + \underset{r_i}0\newline
\end{aligned}
$$

So $\gcd(88,72) = 8$.

### Example

Find $\gcd(78,35)$.

#### Solution

$$ %Aligned
\begin{aligned}
    \underset{a}78 &= \underset{b}35 \cdot \underset{q}2 + \underset{r}8 \newline
    35 &= 8 \cdot 4 + 3 \newline
    8 &= 3 \cdot 2 + 2\newline
    3 &= 2 \cdot 1 + 1 \newline
    2 &= 1 \cdot 2 + \underset{\text{stop}}0 \newline
\end{aligned}
$$

So $\gcd(78,35) = 1$, they are _relatively prime_.

## Relative Primes

_definition_: If $a,b \in \mathbb Z$ and $\gcd(a,b) = 1$ then we say $a$ and $b$ are __relatively prime_ since they have no common factors.


### Fact

For $a,b \in \mathbb Z$, not both zero, $\exists x,y \in \mathbb Z$ such that,

$$
    \gcd(a,b) = \underset{\text{Linear Combo}}{ax + by}.
$$

To find $x$ and $y$ we must use the _Euclidean Algorithm_ in reverse.

### Example

Find $x,y$ such that $1 = 78x + 35y$.

#### Solution

$$ %Aligned
\begin{aligned}
    1 &= 3 - 2 \cdot 1 \newline
    &= 3 - (8 - 3 \cdot 2) \cdot 1 \newline
    &= 3 - 8 + 3 \cdot 2 \newline
    &= 3 \cdot 3 - 8 \newline
    &= 3 \cdot (35 - 8 \cdot 4) - 8 \newline
    &= 3 \cdot 35 - 12 \cdot 8 - 8 \newline
    &= 3 \cdot 35 - 13 \cdot 8 \newline
    &= 3 \cdot 35 - 13 \cdot (78 - 35 \cdot 2) \newline
    &= 3 \cdot 35 - 13 \cdot 78 - 26 \cdot 35 \newline
    &= \underset{x}{-13} \cdot 78 + \underset{y}{29} \cdot 35 \newline
\end{aligned}
$$

So $1 = \gcd(78,35) = 78x + 35y$ where $x = -13$ and $y = 29$.

### Corollary

Let $a,b,x \in \mathbb Z$ such that $a \mid bx$. If $a$ and $b$ are relatively prime, then,

$$
    a \mid x
$$

#### Proof

Let $a,b,x \in \mathbb Z$ such that $a \mid bx$, and suppose, $a$ and $b$ are coprime, then,

$$
    \gcd(a,b) = 1
$$

By the last fact $\exists y,z \in \mathbb Z$ such that $\gcd(a,b) = ay + bz$. Multiplying by $x$ yields,

$$
    x = axz + bxy
$$

clearly, $a \mid axz$, since $a \mid bx$, $a \mid bxy$.

$$ %Aligned
\begin{aligned}
    &\therefore a \mid axz + bxy \newline
    &\therefore a \mid x \newline
\end{aligned}
$$

### Corollary

Let $a,b,c \in \mathbb Z$ such that $c \mid a$ and $c \mid b$.

$$
    c \mid \gcd(a,b)
$$

## LCM

_definition_: If $a,b \neq 0$ are integers, we say $\ell$ is their __least common multiple__ if,

1. $a \mid \ell$ and $b \mid \ell$
2. if $a \mid m$ and $b \mid m$ then $\ell \le m$

and we write $\ell = \text{lcm}(a,b$).

### Examples

* $\text{lcm}(3,4) = 12$
* $\text{lcm}(4,6) = 12$
* $\text{lcm}(1,a) = a$

### Fact

$$
    \text{lcm}(a,b) = \frac{|ab|}{\gcd(a,b)}
$$
