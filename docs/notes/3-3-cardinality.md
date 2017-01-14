
# Section 3.3 - One-to-one correspondences and the Cardinality of a Set

## Cardinality

_definition_: The __cardinality__ of set $A$, denoted $|A|$, is the number of elements in set $A$.

**Example**

$$ %Aligned
\begin{aligned}
    A &= \{ a,b,c \} \newline
    |A| &= 3 \newline
\end{aligned}
$$

## One-to-one Correspondences

_definition_: A function $f: A \mapsto B$ that is a bijection is also a __one-to-one correspondence__. We say $\exists$ a one-to-one correspondence between $A$ and $B$.

### Fact

$$ %Aligned
\begin{aligned}
    |A| = |B| \iff \exists ~f:A \mapsto B \text{ that is a bijection.}
\end{aligned}
$$

### Claim

$$ %Aligned
\begin{aligned}
    |(0,1)| = |(2,5)|
\end{aligned}
$$

#### Proof

Consider $f: (0,1) \mapsto (2,5)$, where,

$$ %Aligned
\begin{aligned}
    f = 2x + 3 \newline
\end{aligned}
$$

_(one-to-one)_ Supposed $f(x_1) = f(x_2)$,

$$ %Aligned
\begin{aligned}
    3x_1 + 2 &= 3x_2 + 2 \newline
    3x_1 &= 3x_2 \newline
    x_1 &= x_2 \newline
\end{aligned}
$$

_(onto)_ Let $y \in (2,5)$, if $f(x) = y$,

$$ %Aligned
\begin{aligned}
    3x + 2 &= y \newline
    3x &= y - 2 \newline
    x &= \frac{y-2}{3} \newline
\end{aligned}
$$

$$ %Aligned
\begin{aligned}
    \therefore f \text{ is a bijection.}
\end{aligned}
$$



**Example**

Let $2 \mathbb Z = \{ ...,-4,-2,0,2,4,... \}$, show $|\mathbb Z| = |2 \mathbb Z|$.

**_Solution_**

Define $f: \mathbb Z \mapsto \mathbb 2Z$, where,

$$
    f(x) = 2x
$$

which is a bijection (easy to prove).

## Countability

_definition_: A set $A$ is __countably infinite__ if,

$$ %Aligned
\begin{aligned}
    |A| = |\mathbb N|
\end{aligned}
$$

So if I can line up a value in a with a value in the countable numbers (natural numbers) it's countably infinite.

* $A$ is __countable__ if it is countably infinite or finite.
* If $A$ is not countable it is __uncountable__.

#### Note

Sometimes $|\mathbb N$ is denoted $\aleph_0$ ("Aleph naught").

### Proposition

A set $A$ is countable if and only if $\exists$ a bijection $f: A \mapsto \mathbb N$ (i.e. you can list the elements of $A$).

### Proposition

$\mathbb Z$ is countable. We can show a correspondence,

$$ %Aligned
\begin{aligned}
    \mathbb Z&: 0,-1,1,-2,2,-3,3,-4,4,... \newline
    \mathbb N&: 0,1,2,3,4,5,6,7,8,9,... \newline
\end{aligned}
$$

This is a sufficient correspondence. However we can show a more mathy correspondence,

$$ %Aligned
\begin{aligned}
    f(x) = (-1)^n \lceil \frac{n}{2} \rceil
\end{aligned}
$$

### Fact

A subset of a countable set is also countable.

### Proposition

A set $A$ is countable if there exists a bijection $f: A \mapsto B$ where $B$ is any countable set.

### Fact

$\mathbb N \times \mathbb N$ is countable! Lets make a table!

| $~$  | $0$ | $1$ | $2$ | $...$ |
|:-:|:-:|:-:|:-:|:-:|
| $0$ | $(0,0)$ | $(0,1)$ | $(0,2)$ | $...$ |
| $1$ | $(1,0)$ | $(1,1)$ | $(1,2)$ | $...$ |
| $2$ | $(2,0)$ | $(2,1)$ | $(2,2)$ | $...$ |
| $...$ | $...$ | $...$ | $...$ | $...$ |

Using _diagonal sweeping_ we get,

$$
    (0,0),(0,1),(1,0),(2,0),(1,1),(0,2),...
$$

### Fact

$\mathbb Q$ is countable.

| $~$  | $0$ | $1$ | $-1$ | $2$ | $-2$ | $...$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $1$ | $\frac{0}{1}$ | $\frac{1}{1}$ | $\frac{-1}{1}$ | $\frac{2}{1}$ | $\frac{-2}{1}$ | $...$ |
| $2$ | $\frac{0}{2}$ | $\frac{1}{2}$ | $\frac{-1}{2}$ | $\frac{2}{2}$ | $\frac{-2}{2}$ | $...$ |
| $...$ | $...$ | $...$ | $...$ | $...$ |

Using _diagonal sweeping_ we get,

$$
     \frac{0}{1}, \frac{1}{1}, \frac{0}{2}, ...
$$

### Fact

The union of countably infinite sets is countable, e.g.,

$$
    \mathbb Z \cup \mathbb Q, \mathbb Z \cup \mathbb N \cup \{a,b,c \}
$$

## Countability Summary

A set $A$ is countable if,

* It's finite,
* It's the union of countable sets,
* It's a subset of a countable set,
* There exists bijection $f: A \mapsto \mathbb N$,
* We can list the elements of $A$.


### Recall

A set is __countable__ if it is not countable.

### Fact

The open interval $(0,1)$ is uncountable.

#### Proof

> _Proof Idea_: Let's use a proof by contradiction by trying to list the elements between zero and one. Then we'll show that no matter how we list the elements we always miss something.

Suppose to the contrary $(0,1)$ is countable, and we can list its elements,

$$
    [0.d_{10}d_{11}d_{12}d_{13}...],[0.d_{20}d_{21}d_{22}d_{23}...],[0.d_{30}d_{31}d_{12}d_{33}...],...
$$

where any $d_{ij} \in \{0,1,2,...,8,9 \}$ and $d_{ij}$ is the $j$^th digit of the $i$^th number.

Lets construct a new element $x$ on the interval $(0,1)$ and show that $x$ is not in the list. Since $x \in (0,1)$,

$$
    x = 0.x_{1}x_{2}x_{3}x_{4}x_{5}...
$$

where $x_i = \{ 0,1,2,...,9 \}$. Now let,

$$
    x_i = \left\{
      \begin{array}{lr}
        5 &\text{ if } d_{ii} \neq 5 \newline
        6 &\text{ if } d_{ii} = 5 \newline
      \end{array}
    \right.
$$

New we'll compare $x$ to our list,

$$
\begin{aligned}
    x = 0.x_{1}x_{2}x_{3}x_{4}... &\neq 0.d_{10}d_{11}d_{12}d_{13}... \newline
    &\neq 0.d_{20}d_{21}d_{22}d_{23}... \newline
    &\neq 0.d_{30}d_{11}d_{32}d_{33}... \newline
    &~~\vdots\newline
\end{aligned}
$$

Since $x$ is not in our list, the list does not count all elements and is therefore not countable.

##### Note

This technique is called __Cantor Diagonalization__.

### Fact

A set $A$ is uncountable if it has an uncountable subset. So the real numbers $\mathbb R$ are uncountable since $(0,1) \subset \mathbb R$.

**Example**

Is $[0,1]$ countable?

**_Solution_**

$$
\begin{aligned}
    \left[0,1\right] &= (0,1) \cup \{ 0\} \cup \{1\} \newline
    (0,1) &\subseteq [0,1] \newline
\end{aligned}
$$

So $[0,1]$ is uncountable.

### Fact

The irrational numbers $\mathbb I$ are uncountable.

#### Proof

Consider

$$ %Aligned
\begin{aligned}
    \mathbb R = \mathbb Q \cup mathbb I.
\end{aligned}
$$

Suppose to the contrary that $\mathbb I$ is countable. Since $\mathbb Q$ is countable this would make $\mathbb R$ countable. $\mathbb R$ is not countable therefore $\mathbb I$ must be uncountable.

## Cantor's Continuum Hypothesis

There is no set $A$ such that,

$$ %Aligned
\begin{aligned}
    \aleph_0 \lt |A| \lt |\mathbb R|
\end{aligned}
$$

where $\aleph_0 = |\mathbb N|$.

* In 1940 Godel showed that we cannot prove the continuum hypothesis to be __false__.
* In 1963 Cohen showed that we cannot prove the continuum hypothesis to be __true__.

