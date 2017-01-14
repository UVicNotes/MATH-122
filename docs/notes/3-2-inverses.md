# Section 3.2 &ndash; Inverses and Compositions

**Example**

$$
\begin{aligned}
    A &= \{ 1,2,3,4 \} \newline
    B &= \{ w,x,y,z \} \newline
    C &= \{ a,b,c \} \newline
\end{aligned}
$$

Let $f: A \mapsto B$,

$$
\begin{aligned}
    f = \{ (1,x),(2,y),(3,z),(4,w) \}
\end{aligned}
$$

and,

$$
\begin{aligned}
    g = \{ (1,a),(2,b),(3,c),(4,c) \}
\end{aligned}
$$

**_Solution_**

$f$ is one-to-one and onto since every element in $B$ is related to exactly one element in $A$, it is therefore a bijection. $g$ is not one-to-one since both $3$ and $4$ map to $c$ but it is onto since every element in $C$ is mapped to.

Reversing the order of each pair in $f$ gives its inverse $f^{-1}: B \mapsto A$, where,

$$
\begin{aligned}
    f^{-1} = \{ (x,1),(y,2),(z,3),(w,4) \}
\end{aligned}
$$

$g$ does not have an inverse since it wouldn't be a function.

## Inverses

_definition_: A function $f: A \mapsto B$ has an __inverse__,

$$
    f^{-1}: B \mapsto A
$$

if and only if the relation obtained by reversing $f$'s ordered pairs is a function and is defined by,

$$
    f^{-1} = \{(y,x): (x,y) \in f \}.
$$

To find the inverse,

1. Switch $x$ and $y$,
2. Solve for $y$.

**Example**

Find $f^{-1}: \mathbb R \setminus \{ 1\} \mapsto \mathbb R \setminus \{2\}$ where,

$$
    f(x) = y =\frac{2x}{x-1}
$$

**_Solution_**


$$
\begin{aligned}
    \frac{2y}{y-1} &= x \newline
    2y &= x (y-1) \newline
    2y - xy &= -x \newline
    y(2-x) &= -x \newline
    y &= \frac{-x}{2-x} \newline
    y &= \frac{x}{x-2} \newline
\end{aligned}
$$

### Proposition

A function $f$ has an inverse if and only if $f$ is a bijection (it's one-to-one and onto).

#### Fact

$$
    (f^{-1})^{-1} = f
$$

So every inverse is a bijection as well.

## Compositions

_definition_: The __composition__ of $g: B \mapsto C$ with $f: A \mapsto B$ is,

$$
    g \circ f = g(f(x)), \forall x \in A
$$


**Example**

$$
\begin{aligned}
    A &= \{ 1,2,3,4 \} \newline
    B &= \{ w,x,y,z \} \newline
    C &= \{ a,b,c \} \newline
\end{aligned}
$$

$$
\begin{aligned}
    f&: A \mapsto B &\text{ where } f = \{ (1,w),(2,z),(3,x),(4,w) \} \newline
    g&: B \mapsto C &\text{ where } g = \{ (w,a),(x,c),(y,b),(z,a) \} \newline
\end{aligned}
$$

**_Solution_**

Potatoes.

$$
\begin{aligned}
    g \circ f = \{ (1,a),(2,a),(3,c)(4,a) \}
\end{aligned}
$$
$$
\begin{aligned}
    f \circ g = \text{ not a function}
\end{aligned}
$$
$$
\begin{aligned}
    (g \circ f)^{-1} = \text{ not a function}
\end{aligned}
$$

### Notation

* $f^2 = f \circ f$
* $f^n = f \circ f \circ ... \circ f$

### Proposition

if $f: A \mapsto B$ and $g: B \mapsto C$ are bijections, then $g \circ f$ is also a bijection.

#### Proof

_(one-to-one)_ Supposed that $g \circ f(x_1) = g \circ f(x_2)$, for some $x_1, x_2 \in A$, or in another notation,

$$%Aligned
\begin{aligned}
    g(f(x_1)) = g(f(x_2))
\end{aligned}
$$

Since $g$ is one-to-one and $g(f(x_1)) = g(f(x_2))$,

$$ %Aligned
\begin{aligned}
    f(x_1) = f(x_2)
\end{aligned}
$$

then since, $f$ is one-to-one and $f(x_1) = f(x_2)$,

$$ %Aligned
\begin{aligned}
    x_1 = x_2
\end{aligned}
$$

So $g \circ f$ is one-to-one.

_(onto)_ Consider $c \in C$, since $g$ is onto,

$$ %Aligned
\begin{aligned}
    \exists b \in B \text{ such that } g(b) = c
\end{aligned}
$$

and since $f$ is onto,

$$ %Aligned
\begin{aligned}
    \exists a \in A \text{ such that } f(a) = b
\end{aligned}
$$

$$ %Aligned
\begin{aligned}
    \therefore g(b) = g(f(a)) = c
\end{aligned}
$$

and $g \circ f$ is onto.

Since $g \circ f$ is one-to-one and onto it is a bijection.

## Inverses and Identities

### Proposition

Given two functions $f: A \mapsto B$ and $g: B \mapsto A$ are inverses if and only is their compositions are identities.

$$ %Aligned
\begin{aligned}
    g \circ f &= i_A \newline
    f \circ g &= i_B \newline
\end{aligned}
$$

**Example**

$$ %Aligned
\begin{aligned}
    f(x) &= \frac{2x}{x-1} \newline
    g(x) &= \frac{x}{x-2} \newline
\end{aligned}
$$

**_Solution_**

$$ %Aligned
\begin{aligned}
    g \circ f &= \frac{\frac{2x}{x-1}}{\frac{2x}{x-1}-2} \newline
    &= \frac{\frac{2x}{x-1}}{\frac{2x}{x-1}-2} \cdot \frac{x-1}{x-1} \newline
    &= \frac{2x}{2x-2x+2} \newline
    &= \frac{2x}{2} \newline
    &= x \newline
\end{aligned}
$$

$$ %Aligned
\begin{aligned}
    f \circ g &= \frac{2\left( \frac{x}{x-2} \right)}{\left( \frac{x}{x-2} \right)-1} \newline
    &= \frac{2\left( \frac{x}{x-2} \right)}{\left( \frac{x}{x-2} \right)-1} \cdot \frac{x-2}{x-2} \newline
    &= \frac{2x}{2} \newline
    &= x \newline
\end{aligned}
$$
