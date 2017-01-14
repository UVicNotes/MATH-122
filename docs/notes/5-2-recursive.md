# Section 5.2 &ndash; Recursive Sequences

_definition_: A __recursive definition of a sequence__, $a_n$, has two parts,

1. One or more base cases
    * e.g. $a_0=1$, $a_1=7$
2. A recursive function
    * e.g. $a_i = 2 \cdot a_{i-1}$

**Example** 1

The sequence of numbers,

$$\begin{aligned}
    1,2,4,8,16,32,...
\end{aligned}$$

is defined as,

$$\begin{aligned}
    a_0 &= 1 \newline
    a_1 &= 2 \newline
    a_n &= 2a_{n-1}
\end{aligned}$$

for $n \ge 1$. Non recursively this is defined as,

$$\begin{aligned}
    a_n = 2^n
\end{aligned}$$

for all $n \ge 0$ (this is the closed form).

**Example** 2

The Fibonacci Sequence is another example. It can be defined as,

$$\begin{aligned}
    f_1 &= 1 \newline
    f_2 &= 1 \newline
    &~\vdots \newline
    f_n &= f_{n-1} + f_{n-2} \newline
\end{aligned}$$

for $n \ge 2$.

**Example** 3

Consider,

$$\begin{aligned}
    a_0 = 1 \newline
    a_n &= 3a_{n-1} + 1 \newline
\end{aligned}$$

**_Solution_**

$$\begin{aligned}
    a_0 &= 1 \newline
    a_1 &= 3(1) + 1 = 4 \newline
    a_2 &= 3(4) + 1 = 13 \newline
    a_3 &= 3(13) + 1 = 40 \newline
    a_4 &= 3(40) + 1 = 121 \newline
\end{aligned}$$

or,

$$\begin{aligned}
    a_0 &= 1 \newline
    a_1 &= 3(1) + 1 = 3 +1 \newline
    a_2 &= 3(3 + 1) + 1 = 3^2 + 3 + 1 \newline
    a_3 &= 3(3^2 + 3 + 1) + 1 = 3^3 + 3^2 + 3 + 1 \newline
    &~\vdots \newline
    a_n &= \sum_{i = 0}^{n} 3^i \newline
\end{aligned}$$

which isn't a closed form but is better.

**Example**

Let $a_0 = 0$, $a_1 = 3$ and for $n \ge 2$,

$$\begin{aligned}
    a_n = a_{n-1} + 2a_{n-2}
\end{aligned}$$

**_Solution_**

$$\begin{aligned}
    a_0 &= 0 \newline
    a_1 &= 3 \newline
    a_2 &= 3 + 2(0) = 3 \newline
    a_3 &= 3 + 2(3) \newline
    &= 3 + 2 \cdot 3 \newline
    &= 9 \newline
    a_3 &= 3 + 2 \cdot 3 + 2 (3) \newline
    &= 3 + 4 \cdot 3 \newline
    &= 15 \newline
    a_4 &= 3 + 4 \cdot 3 + 2(3 + 2 \cdot 3) \newline
    &= 3 \cdot 3 + 5 \cdot 3 \newline
    &= 33.
\end{aligned}$$

We're going to say this is of the form,

$$\begin{aligned}
    a_n = 2^n + (-1)^{n+1}
\end{aligned}$$

for $n \ge 0$.

#### Proof

> By strong induction

Let $P(n)$ be the statement,

$$\begin{aligned}
    a_n = 2^n + (-1)^{n+1}
\end{aligned}$$

for $n \ge 0$.

__Base:__ Consider $P(0)$ and $P(1)$, from the recursive function,

$$\begin{aligned}
    a_0 &= 0 \newline
    a_1 &= 3 \newline
\end{aligned}$$

and from our closed form,

$$\begin{aligned}
    a_0 &= 2^0 + (-1)^{0+1} \newline
    &= 0 \newline
    a_1 &= 2^1 + (-1)^{1+1} \newline
    &= 2 + 1 \newline
    &= 3 \newline
\end{aligned}$$

so $P$ holds for $n = 0,1$.

__Induction Hypothesis:__ Let $k \gt 1$, suppose that $P(m)$ is true for $1 \le m \lt k$. That is,

$$\begin{aligned}
    a_m = 2^m + (-1)^{m+1}
\end{aligned}$$

__Induction Step:__ Consider $P(k)$,

$$\begin{aligned}
    a_k &= a_{k-1} + 2 a_{k-2} \newline
    &= 2^{k-1} + (-1)^{k-1 + 1} + 2 \left( 2^{k-2} + (-1)^{k-2+1} \right) \newline
    &= 2^{k-1} + (-1)^{k} + 2 \cdot 2^{k-2} + 2 \cdot (-1)^{k-1} \newline
    &= 2^{k-1} + (-1)^{k} + 2^{k-2+1} + (-1)^{-1} \cdot 2 \cdot (-1)^{k} \newline
    &= 2^{k-1} + (-1)^{k} + 2^{k-1} - 2 \cdot (-1)^{k} \newline
    &= 2 \cdot 2^{k-1} + (-1)(-1)^{k} \newline
    &= 2^{k-1+1} + (-1)^{k+1} \newline
    &= 2^{k} + (-1)^{k+1} \newline
\end{aligned}$$

therefore, by induction, $P(n)$ holds.

