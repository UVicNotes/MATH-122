
# Section 4.1 &ndash; The Division Algorithm

## Properties of $\mathbb Z$ vs $\mathbb R$

Let $a,b \in \mathbb R$.

### Closure ($\mathbb R$ and $\mathbb Z$)

* $a + b \in \mathbb R$
* $a \cdot b \in \mathbb R$


### Commutivity ($\mathbb R$ and $\mathbb Z$)

* $a + b = b + a$
* $a \cdot b = b \cdot a$


### Associativity ($\mathbb R$ and $\mathbb Z$)

* $(a + b) + c = a + (b + c)$
* $(ab)c = a(bc)$


### Identity ($\mathbb R$ and $\mathbb Z$)

* $\exists 0 \in \mathbb R$ such that, $\forall a \in \mathbb R, 0+a = a$
* $\exists 1 \in \mathbb R$ such that, $\forall a \in \mathbb R, 1 \cdot a = a$


### Distribution ($\mathbb R$ and $\mathbb Z$)

* $a \cdot (b + c) = a \cdot b + a \cdot c$

### Inverses ($\mathbb R$ and _some_  $\mathbb Z$)

($\mathbb Z$) For any $a \in \mathbb R, \exists -a \in \mathbb R$, such that,

$$
    a + (-a) = 0.
$$

(not $\mathbb Z$) For any $a \in \mathbb R, \exists \frac{1}{a} \in \mathbb R$, such that,

$$
    a \cdot \frac{1}{a} = 1
$$

**Example**

$\mathbb Z ^\text{o} =$ the set of odd integers.

Is $\mathbb Z ^\text{o}$ closed under addition and multiplication?

**_Solution_**

IT is not closed under addition since $5 + 3 = 8$.

Closed under multiplication. Proof:

Let $a,b \in \mathbb Z ^\text{o}$, so,

$$ %Aligned
\begin{aligned}
    a &= 2m + 1 \newline
    b &= 2n + 1 \newline
\end{aligned}
$$

where $m,n \in \mathbb Z$. So,

$$ %Aligned
\begin{aligned}
    a \cdot b &= (2m+1)(2n+1) \newline
    &= 4mn + 2m + 2n + 1 \newline
    &= 2(2mn + m + n) + 1. \newline
\end{aligned}
$$

Since $2mn + m + n \in \mathbb Z$, $a \cdot b \in \mathbb Z^\text{o}$.

## Subtraction and Division

We define subtraction and division using inverses.

* $a - b = a + (-b)$
* $\frac{a}{b} = a \cdot \frac{1}{b}$

### Theorem: The Well-Ordering Principal

Any set of natural numbers ($\mathbb N$) has a smallest element*.

*Does note hold for $\mathbb Z$ or $\mathbb R$.

## The Division Algorithm

**Example**

Divide $278$ by $13$

**_Solution_**

Can't do long division :(.

### Theorem

For integers $a$ and $b$, both not zero, there exist _unique_ integers $q$ and $r$ such that,

$$
    a = bq + r
$$

where $0 \lt r \lt |b|$. We call,

| Symbol | Name |
|:-:|:--|
|$a$| Dividend |
|$b$| Divisor |
|$q$| Quotient |
|$r$| Remainder |

### Proposition

Let $a,b \in \mathbb Z$ where $b \neq 0$. If $a = bq + r$, with $0 \lt r \lt |b|$, then,

$$
    q = \left\{
     \begin{array}{lr}
       \left\lfloor \frac{a}{b} \right\rfloor &\text{ if } b \gt 0 \newline
       \left\lceil \frac{a}{b} \right\rceil &\text{ if } b \lt 0 \newline
     \end{array}
   \right.
$$

## Number in Other Bases

**Example**

Consider in base 10,

$$ %Aligned
\begin{aligned}
    7132 &= 7 \cdot 1000 + 1 \cdot 100 + 3 \cdot 10 + 2 \cdot 1 \newline
    &= 7 \cdot 10^3 + 1 \cdot 10^2 + 3 \cdot 10^1 + 2 \cdot 10^0 \newline
\end{aligned}
$$

Now consider in base 8,

$$ %Aligned
\begin{aligned}
    (7132)_8 = 7 \cdot 8^3 + 1 \cdot 8^2 + 3\cdot 8^1 + 2 \cdot 8^0
\end{aligned}
$$


_definition_: The __base $b$ representation of a natural (base 10) number $n$__ is written,

$$
    (d_k d_{k-1} d_{k-2} ... d_1 d_0)_b
$$

where $0 \le d_i \lt b$ and

$$
    n = d_kb^k + d_{k-1}b^{k-1} + d_{k-2}b^{k-2} + ... + d_1b^1 + d_0b^0.
$$

### Theorem

If $b \gt 1$, then every integer $n$ has a __unique__ base $b$ representation.

> Proof in G. MacGillivray notes (NT pg. 4)

**Example**

Convert $(613)_{10}$ to binary, octal and hexadecimal.

**_Solution_**

##### Binary (Method 1)

$$ %Aligned
\begin{aligned}
    (613)_{10} &= 2^9 + 101 \newline
    &= 2^9 + 2^6 + 37 \newline
    &= 2^9 + 2^6 + 2^5 + 5 \newline
    &= 2^9 + 2^6 + 2^5 + 2^2 + 1 \newline
    &= 2^9 + 2^6 + 2^5 + 2^2 + 2^0 \newline
    &= (1001100101)_2 \newline
\end{aligned}
$$

##### Binary (Method 2)

$$ %Aligned
\begin{aligned}
    \frac{613}{2} &= 306 r 1 \newline
    \frac{306}{2} &= 153 r 0 \newline
    \frac{153}{2} &= 76 r 1 \newline
    \frac{76}{2} &= 38 r 0 \newline
    \frac{38}{2} &= 19 r 0 \newline
    \frac{19}{2} &= 9 r 1 \newline
    \frac{9}{2} &= 4 r 1 \newline
    \frac{4}{2} &= 2 r 0 \newline
    \frac{2}{2} &= 1 r 0 \newline
    \frac{1}{2} &= 0 r 1 \newline
\end{aligned}
$$

##### Octal

$$ %Aligned
\begin{aligned}
    613 \div 8 &= 76 ~r~ 5 \newline
    76 \div 8 &= 9 ~r~ 4 \newline
    9 \div 8 &= 1 ~r~ 1 \newline
    1 \div 8 &= 0 ~r~ 1 \newline
\end{aligned}
$$

So,

$$ %Aligned
\begin{aligned}
    (613)_{10} = (1145)_8
\end{aligned}
$$

##### Hexadecimal

$$ %Aligned
\begin{aligned}
    613 \div 16 &= 38 ~r~ 5 \newline
    38 \div 16 &= 2 ~r~ 6 \newline
    2 \div 16 &= 0 ~r~ 2 \newline
\end{aligned}
$$

So,

$$ %Aligned
\begin{aligned}
    (613)_{10} = (613)_10
\end{aligned}
$$

**Example**

Convert $1222$ to hexadecimal.

**_Solution_**

Use your calculator,

$$ %Aligned
\begin{aligned}
    (1222)_{10} = (4C6)_{16}
\end{aligned}
$$
