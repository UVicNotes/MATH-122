# Section 5.1 -- Mathematical Induction

### Fact

The punctured $2^n \times 2^n$ chessboard can be tiled by the 3-square corner piece. Once you have the initial $2 \times 2$ board and you know the centre tile trick, you can solve any board.

### Example

Consider a line of dominos, $1,2,3,...,n-1,n,n+1,...$ where domino $n$ falls over. This infers that dominos $n+1,n+2,...$ will fall.

We need two things to ensure all the dominos fall over,

1. We need to know one domino falls, an initial push (Basis)
2. We need to know that one domino falling will cause the others to fall (Inductive step)

## Induction

_definition_:


### Example

Prove that for any natural number $n \gt 1$,

$$
    \sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

#### Solution

Let $P(n)$ be the statement,

$$
    \sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

where $n \in \mathbb N$ and $n \gt 0$.

##### Basis

Consider the base case $P(1)$, on the left hand side,

$$\begin{aligned}
    \sum_{i=1}^{1} i &= 1
\end{aligned}$$

on the right hand side,

$$\begin{aligned}
    \frac{1 \cdot (1 + 1)}{2} &= \frac{2}{2} \newline
    &= 1 \newline
\end{aligned}$$

since the left hand side is equal to the right hand side $P(1)$ is true.

###### Inductive Hypothesis

Suppose that $P(k)$ is true for some $k \in \mathbb N$ where $k \gt 1$, i.e.,

$$\begin{aligned}
    \sum_{i=1}^{k} i = \frac{k(k+1)}{2}
\end{aligned}$$

##### Inductive Step

Consider $P(k+1)$, on the left hand side,

$$\begin{aligned}
    \sum_{i=0}^{k+1} i &= 1 + 2 + 3 + ... + k + k + 1 \newline
    &= \sum_{i=0}^{k} i + k + 1
\end{aligned}$$

by the inductive hypothesis,

$$\begin{aligned}
    \sum_{i=0}^{k+1} i &= \frac{k(k+1)}{2} + k + 1 \newline
    &= \frac{k(k+1) + 2k + 2}{2} \newline
    &= \frac{k^2 + 3k + 2}{2} \newline
    &= \frac{(k+2)(k+1)}{2} \newline
\end{aligned}$$

and if we consider the right hand side of $P(k+1)$,

$$\begin{aligned}
    \frac{(k+1)((k+1)+1)}{2} = \frac{(k+1)(k+2)}{2}.
\end{aligned}$$

The right hand side is equal to the left hand side, therefore, by induction,

$$
    \sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

for all $n \in \mathbb N$.


### Example

Prove that for all $n \ge 1$,

$$\begin{aligned}
    \frac{1}{1\cdot2} + \frac{1}{2\cdot3} + \frac{1}{3\cdot4} + ... + \frac{1}{n(n+1)} &= \frac{n}{n+1} \newline
\end{aligned}$$

#### Solution

Let $P(n)$ be the statement,

$$\begin{aligned}
    \sum_{i=1}^{n} \frac{1}{i(i+1)} = \frac{n}{n+1}
\end{aligned}$$

where $n \in \mathbb N$, $n \ge 1$.

##### Base

Consider the base case $P(1)$ where $n = 1$, on the left hand side,

$$\begin{aligned}
    \sum_{i=1}^{n} \frac{1}{i(i+1)} &= \sum_{i=1}^{1} \frac{1}{i(i+1)} \newline
    &= \frac{1}{1(1+1)} \newline
    &= \frac{1}{2}
\end{aligned}$$

on the right hand side,

$$\begin{aligned}
    \frac{n}{n+1} &= \frac{1}{1+1} \newline
    &= \frac{1}{2} \newline
\end{aligned}$$

since the left hand side equals the right hand side, $P(1)$ holds.

##### Inductive Hypothesis

Suppose $P(k)$ is true for $k \ge 1$,

$$\begin{aligned}
    \sum_{i=1}^{k} \frac{1}{i(i+1)} = \frac{k}{k+1}
\end{aligned}$$

##### Inductive Step

Consider $P(k+1)$, on the left hand side,

$$\begin{aligned}
    \sum_{i=1}^{k+1} \frac{1}{i(i+1)} &= \frac{1}{1\cdot2} + \frac{1}{2\cdot3} + ... + \frac{1}{k\cdot(k+1)} + \frac{1}{(k+1)\cdot((k+1)+1)} \newline
    &= \frac{1}{1\cdot2} + \frac{1}{2\cdot3} + ... + \frac{1}{k\cdot(k+1)} + \frac{1}{(k+1)\cdot(k+2)} \newline
    &= \left(\sum_{i=1}^{k} \frac{1}{i(i+1)} \right) + \frac{1}{(k+1)\cdot(k+2)} \newline
    &= \frac{k}{k+1} + \frac{1}{(k+1)\cdot(k+2)} \newline
    &= \frac{k(k+2)}{(k+1)\cdot(k+2)} + \frac{1}{(k+1)\cdot(k+2)} \newline
    &= \frac{k(k+2) + 1}{(k+1)\cdot(k+2)} \newline
    &= \frac{k^2 + 2k + 1}{(k+1)\cdot(k+2)} \newline
    &= \frac{(k + 1)\cdot(k+1)}{(k+1)\cdot(k+2)} \newline
    &= \frac{k+1}{k+2} \newline
\end{aligned}$$

 on the right hand side,

 $$\begin{aligned}
    \frac{k+1}{(k+1) + 1} = \frac{k+1}{k+2}
\end{aligned}$$

since the left hand side is equal to the right hand side, $P(k+1)$ holds. Therefore, by induction, $P(n)$ holds for all $n \in \mathbb N$ where $n \ge 1$.

### Example

Prove that for $n \in \mathbb N$ where $n \ge 5$, $4n \le 2^n$.

#### Solution

Let $P(n)$ be the statement,

$$
    4n \le 2^n
$$

for all $n \in \mathbb n$ where $n \ge 5$.

##### Base

Consider $P(5)$, on the left hand side,

$$\begin{aligned}
    4n &= 4 \cdot 5 \newline
    &= 20 \newline
\end{aligned}$$

on the right hand side,

$$\begin{aligned}
    2^n &= 2^5 \newline
    &= 32 \newline
\end{aligned}$$

since the left hand side is less than the right hand side, $P(5)$ holds.

##### Inductive Hypothesis

Suppose $P(k)$ is true for $k \ge 5$, i.e.,

$$\begin{aligned}
    4k \le 2^k
\end{aligned}$$

##### Inductive Step

Consider $P(k+1)$, on the left hand side,

$$\begin{aligned}
    4(k+1) &= 4k + 4 \newline
    &\le 2^k + 4 \newline
    &= 2^k + 2^2 \newline
    &\le 2^k + 2^k \newline
    &= 2\cdot2^k \newline
    &= 2^{k+1} \newline
\end{aligned}$$

on the right hand side,

$$\begin{aligned}
    2^{k+1}
\end{aligned}$$

since the left hand side is less than or equal to the right hand side, if $P(k)$ is true then $P(k+1)$ holds for all $k \in \mathbb N$ where $k \ge 5$. Therefore, by induction, $P(n)$ is true for all $n \in \mathbb N$.


### Example

Prove for $n \ge 1$,

$$
    2^n \mid (2n)!
$$

#### Solution

Let the tameness $P(n)$ be,

$$
    2^n \mid (2n)!
$$

for $n \in \mathbb N$ where $n \ge 1$.

##### Base

Consider the case $P(1)$, on the left hand side,

$$\begin{aligned}
    2^1 = 2
\end{aligned}$$

and on the right hand side,

$$\begin{aligned}
    (2\cdot2)! &= (4)! \newline
    &= 1 \cdot 2 \cdot 3 \cdot 4 \newline
    &= 2 \cdot 12
\end{aligned}$$

since $2 \mid 2 \cdot 12$, $P(1)$ holds.

##### Inductive Hypothesis

Suppose $P(k)$ holds for some $k \in \mathbb N$ where $k \ge 1$, i.e.,

$$\begin{aligned}
    2^k \mid (2k)!
\end{aligned}$$

##### Inductive Step

Consider $P(k+1)$, on the left hand side,

$$\begin{aligned}
    2^{k+1} &= 2 \cdot 2^k \newline
    &= 2 \cdot (2k)!
\end{aligned}$$

by the induction hypothesis, and on the right hand side,

$$\begin{aligned}
    (2(k+1))! &= (2k + 2)! \newline
    &= 1 \cdot 2 \cdot ... \cdot 2k \cdot (2k + 1) \cdot (2k + 2) \newline
    &= (2k)! \cdot (2k + 1) \cdot (2k+2) \newline
    &= 2 \cdot (2k)! \cdot \left[ \left(2k+1\right) \cdot \left(k+1\right) \right]
\end{aligned}$$

since the right hand side has the left hand side as a factor the left hand side divides the right hand side. Therefore, by induction, $P(n)$ holds.

## Strong Induction

> Induction with expanded base cases

_definition_: Let $P(n)$ be a statement whose truth-value depends upon $n$. If the following hold then  $P(n)$ is true for all $n \ge n_0$,

1. $P(n)$ is true for all $n = n_0, n_0 + 1, n_0 +2, ... ,t$ for some $t \ge n_0$. (Base)
2. If $P(m)$ is true for some $n_0 \le m \lt k$, then $P(k)$ is true. (Inductive Step)

### Strategy

1. Show $P(n)$ is true for $n = n_0, n_0 + 1, n_0 +2, ... ,t$.
2. Suppose $P(m)$ is true for $n_0 \le m \lt k$.
3. Show $P(k)$ is also true.

### Example

Show that any amount of postage greater than $12$ cents can be paid using only $3$ cent stamps and $7$ cent stamps.

#### Solution

Let $P(n)$ be the statement,

$$\begin{aligned}
    \text{postage of } n \text{ cents can be paid using } 3 \text{ and } 7 \text{ cent stamps.}
\end{aligned}$$

where $n \ge 12$.

##### Base

For $n = 12$,

$$\begin{aligned}
    4 \cdot 3 = 12
\end{aligned}$$

and for $n = 13$,

$$\begin{aligned}
    2 \cdot 3 + 7 = 13
\end{aligned}$$

and for $n = 14$,

$$\begin{aligned}
    2 \cdot 7 = 14
\end{aligned}$$

and for $n = 15$,

$$\begin{aligned}
    4 \cdot 3 + 3 = 12 + 3 = 15
\end{aligned}$$

and for $n = 16$,

$$\begin{aligned}
    2 \cdot 3 + 7 + 3 = 13 + 3 = 16
\end{aligned}$$

##### Inductive Hypothesis

Suppose $P(m)$ is true for some $12 \le m \le k$ where $k \in \mathbb N$ and $k \gt 12$.

##### Inductive Step

Consider $P(k+1)$, this implies $k+1 \gt 12$, by the induction hypothesis,

$$\begin{aligned}
    (k+1)-3 = k - 2
\end{aligned}$$

or $P(k-2)$ is payable, and therefore, by adding $3$ cents $P(k+1)$ is payable. Therefore, by induction $P(n)$, is payable.

