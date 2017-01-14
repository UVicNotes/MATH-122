
# Section 2.4 &ndash; Equivalence Relations


_definition_: A relation $\mathcal R$ on a set $A$ is an __equivalence relationship__ if it is,

1. Reflexive
2. Symmetric
3. Transitive

**Example**

Consider $\mathcal R$ on $\mathbb Z \times \mathbb Z$, defined by,

$$
    a \mathcal R b \iff a-b \text{ is a multiple of 3}.
$$

**_Solution_**

##### Reflexivity

Let $a \in \mathbb Z$, then,

$$
    a - a = 0 = 0 \cdot 3
$$

Therefore $(a,a) \in \mathcal R$.

##### Symmetry

Let $(a,b) \in \mathcal R$, so,

$$
    a - b = 3k
$$

for some $k \in \mathbb Z$.

$$
    b - a = -3k = 3 \cdot (-k)
$$

Since $-k \in \mathbb Z$, $b - a$ is a multiple of $3$ and therefore $(b,a) \in \mathcal R$.

##### Transitivity

Let $(a,b) \in \mathcal R$ and $(b,c) \in \mathcal R$, so,

$$
    a - b = 3k
$$

and

$$
    b -c = 3m
$$

for $k, m \in \mathbb Z$. Adding the equations,

$$
\begin{aligned}
    a - b + b - c &= 3k + 3m \newline
    a - c &= 3 \cdot (k + m)
\end{aligned}
$$

Therefore since $(k + m) \in \mathbb Z$, $a - c$ is a multiple of $3$ and therefore $(a,c) \in \mathcal R$.


If $\mathcal R$ is an equivalence relation,

$$
    \mathcal R \subseteq A \times B
$$

can $A \neq B$?

No, $\mathcal R \subseteq A \times A$.

## Equivalence Class

_definition_: For an equivalence relation $\sim$ on a set $A$, the __equivalence class__ of $a \in A$, is the set of all elements equivalent to $a$.

$$
    \frac{[a]}{a} = \{ x \in A: a \sim x \}
$$

The set of equivalence classes is called the __Quotient set of $A$ mod $\sim$__, denoted $A \setminus \sim$.

## Partition

_definition_: A __partition__ of set $A$ is a collection of subsets $A_1, A_3, A_3,...,A_n$ such that,

* Each is non empty ($A_i \neq \varnothing$)
* They are pairwise disjoint ($A_i \cap A_j = \varnothing$)
* They union to $A$ ($\cup_{i=0}^{n} ~A_i = A$)

### Fact

If $\sim$ is equivalent to $A$, then,

1. The set of all its equivalence classes forms a partition of $A$
2. If $x,y \in A$ then either $[x] = [y]$ or $[x] \cap [y] = \varnothing$

**Example**

Let $\mathcal R \subseteq \mathbb Z \times \mathbb Z$, such that $(x,y) \in \mathcal R$. if and only if $a - b$ is a multiple of $3$.

**_Solution_**

1) What elements are equivalent to $0$?

$$
    a \mathcal R 0 \iff a - 0 = 3k
$$

For $k \in \mathbb Z$. So $3 \mathcal R 0, 6 \mathcal R 0, ...$

$$
    [0] = \{ ..., -9, -6, -3, 0, 3, 6, 9,...  \}
$$

Next lets consider $[3]$,

$$
    [3] = [0] = [9] = [-9] = ...
$$

2) What elements are equivalent to $1$?

$$
\begin{aligned}
    a \mathcal R 1 &\iff a - 1 = 3k, k \in \mathbb Z \newline
    &\iff a = 3k + 1
\end{aligned}
$$

So,

$$
\begin{aligned}
    [1] &= \{ ..., -5, -2, 1, 4, 7, ... \} \newline
    &= [4] = [-5] = ...
\end{aligned}
$$

3) What elements are equivalent to 2?

$$
\begin{aligned}
    a \mathcal R 2 &\iff a - 2 = 3k, k \in \mathbb Z \newline
    &\iff a = 3k + 2
\end{aligned}
$$

$$
\begin{aligned}
    \left[ 2 \right] &= \{ ..., -7 ,-4 ,-1 ,2, 5, 8, 11, ... \} \newline
    &= [-1] = [5] = ...
\end{aligned}
$$

So our equivalence classes are,

$$
\begin{aligned}
    \left[ 0 \right] &= \{ ..., -9, -6, -3, 0, 3, 6, 9,...  \} \newline
    [1] &= \{ ..., -5, -2, 1, 4, 7, ... \} \newline
    [2] &= \{ ..., -7 ,-4 ,-1 ,2, 5, 8, 11, ... \} \newline
\end{aligned}
$$

And the partition is,

$$
    \{ [0], [1], [2] \}
$$

To confirm this we must check that,

$$
    \mathbb Z = [0] \cup [1] \cup [2]
$$

**Example**

Let $A = \{ a,b,c,d,e,f \}$ and $\mathcal R = \{ (a,a), (b,b), ..., (f,e) \}$

We can represent this in a matrix (which is good because I didn't write the whole thing),

| $a$ | $b$ | $c$ | $d$ | $e$ | $f$ | $g$ |
|-----|-----|-----|-----|-----|-----|-----|
| $a$ | $x$ | $~$ | $~$ | $~$ | $~$ | $~$ |
| $b$ | $~$ | $x$ | $~$ | $~$ | $~$ | $~$ |
| $c$ | $~$ | $~$ | $x$ | $~$ | $~$ | $~$ |
| $d$ | $~$ | $~$ | $~$ | $x$ | $x$ | $x$ |
| $e$ | $~$ | $~$ | $~$ | $x$ | $x$ | $x$ |
| $f$ | $~$ | $~$ | $~$ | $x$ | $x$ | $x$ |

From this we can tell that $\mathcal R$ is,

1. Reflective (the diagonal is filled)
2. Symmetric (across the diagonal line)
3. Equivalence Classed (Each 'square' of $x$'s is an equivalence class.


**Example**

Let $D = \{ \text{All binary strings of length } 5 \}$ and $\mathcal T$ be the relation on $ D \times D$ defined by $x \mathcal T y $ the first $3$ digits of $x$ match $y$.

**_Solution_**

$$
\begin{aligned}
    \left[00000\right] &= \{ 00000, 00001, 00010, 00011 \} \newline
                       &= [00001] \newline
    \left[00100\right] &= \{ 00100, 00101, 00110, 00111 \} \newline
    \left[11100\right] &= \{ 11100, 11101, 11110, 11111 \} \newline
\end{aligned}
$$
