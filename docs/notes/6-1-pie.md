
# Section 6.1 - Principal of Inclusion-Exclusion (PIE)

**Example**

Let $\mathcal U$ be the students in the first three rows. Let $C$ be the students in the first three rows who have owned a cat. Let $D$ be the students in the first three rows who have owned a dog. Let $N$ be the students in the first three rows who have owned neither a cat or a dog. So,

$$
    N = C^C \cap D^C
$$

Claim,

$$
    |\mathcal U| = |C| + |D| + |N|
$$

in general this doesn't work, since a student could own a cat and a dog.

## Theorem -- 2-PIE

For sets $A$ and $B$ of some universal set $\mathbb U$,

$$
    |A \cup B| = |A| + |B| - |A \cap B|
$$

**Example**

Of $50$ feline contestants at the Ladysmith cat show, $40\%$ ($20$) are short-haired and $32$ like laser pointers.

A) Find a formula for the number roof long haired cats that don't like laser pointers.

Let,

$$\begin{aligned}
    \mathcal U &= \text{cats at the Ladysmith cat show} \newline
    S &= \text{cats with short hair at the show} \newline
    L &= \text{cats that like laser pointers at the show} \newline
\end{aligned}$$

So,

$$\begin{aligned}
    |S^C \cap L^C| &= |(S \cup L)^C| \newline
    &= |\mathcal U| - |S \cup L| \newline
    &= |\mathcal U| - |S| - |L| + |S \cap L| \newline
    &= 50 - 20 - 32 + |S \cap L| \newline
    &= |S \cap L| - 2 \newline
\end{aligned}$$

If $\left|S \cap L\right| = 2$ then $\left|S^C \cap L^C\right| = 0$ (the minimum). One the other hand if $|S \cap L| = 20$ then $\left|S^C \cap L^C\right| = 18$.

## 2-set Counting Principals

Let $A$ and $B$ be sets of the universal set $\mathcal U$.

1. $\left| A \cup B \right| = \left| A \right| + \left| B \right| - \left| A \cap B \right|$
2. $\left| A \cap B \right| \le \min(\left| A \right|,\left| B \right|)$
3. $\left| A^C \right| = \left| \mathcal U \right| - \left| A \right|$
4. $\left| A \setminus B \right| =  \left| A \right| - \left| A \cap B \right|$
5. $\left| A \oplus B \right| = \left| A \right| + \left| B \right| - 2\left| A \cap B \right|$


## Recall

* $|A \cup B| = |A| + |B| - |A \cap B|$
* $|A \cup B \cup C| = |A|+|B|+|C|-|A \cap B|-|A \cap C| - |B \cap C| + |A \cap B \cap C|$

**Example**

On an exam there are 25 questions, of which 18 are "hard", 10 are Multiple Choice and 6 are proofs.

#### How many hard multiple choice could there be?

We have

$$
    25 - 18 = 7
$$

"easy" multiple choice questions. We therefore can;t have zero hard multiple choice questions since that would imply we need 10 easy multiple choice questions.

$$\begin{aligned}
    |H| &= 18 \newline
    |M| &= 10 \newline
    |E| &= |H^C| = 25 - 18 = 7
\end{aligned}$$

We want to find,

$$\begin{aligned}
    |H \cap M| \ge 3
\end{aligned}$$

### How many easy, long, non-proof could there be?

We want,

$$\begin{aligned}
    |H^C \cap M^C \cap P^C| &= |(H \cup M \cup P)^C| \newline
    &= 25 - (|M| + |P| + |H| - |M \cap P| - |M \cap H| - |P \cap H| + |M \cap P \cap H|) \newline
\end{aligned}$$

## PIE Theorem

Let $A_1,A_2,A_3,…,A_n$ be subsets of sue universal set $\mathcal U$, then,

$$\begin{aligned}
    |A_1 \cup A_2 \cup … \cup A_n| &= |A_1| + |A_2| + … + |A_n| \newline
    &- |A_1 \cap A_2| - |A_1 \cap A_3| - … - |A_{n-1} \cap A_n| \newline
    &~\vdots \newline
    &\pm … \pm |A_1 \cap A_2 \cap … \cap A_n| \newline
    &= \sum_{i = 1}^{n} |A_i| \newline
    &- \sum_{1 \le i \lt j \le n} |A_i \cap A_j| \newline
    &~\vdots \newline
    &+ (-1)^{n+1} |A_1 \cap A_2 \cap … \cap A_n|
\end{aligned}$$

**Example**

Find $\Phi(150)$ where phi is the Euler function, i.e. al numbers less than $150$ that are cop rime to $150$.

**_Solution_**

$$\begin{aligned}
    150 = 2 \cdot 3 \cdot 5^2
\end{aligned}$$

* $n$ is cop rime to $150$ if $n$'s prime decomposition does not contain a $2,3$ or $5$.
* Let $A$ be the set of $1 \le n \le 150$ that do contain a $2$ in it's prime decomposition.
