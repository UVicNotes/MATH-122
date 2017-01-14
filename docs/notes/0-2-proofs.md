# Section 0.2 &ndash; Proofs in Math

To prove results, beyond those in formal logic, we use _word proofs_.

## Direct Proof

To show $ p \to q $, assume $p$ is true, then use known results (e.g. facts, logical equivalents) to show that $q$ is also true.

### Facts

#### Even Integers

If $n$ is an even integer, then,

$$ n = 2k $$

where $k$ is some integer.

#### Odd Integers

If $n$ is an odd integer, then,

$$ n = 2k +1 $$

where $k$ is some integer.

**Example**

If some integer $n$ is even, then $n^2$ is also even.

**_Solution_**


_Proof_: Supposed $n$ is even, then,

$$ n = 2k $$

For some $k \in \mathbb{Z}$.

So,

$$ n^2 = (2k)^2 = 2(2k^2) $$

and $2k^2$ is an integer.

$$ \therefore n^2 = 2k^2 \text{ is even.} $$

## Proof by Contrapositive

Assume that $\neg q$ is true, then use known result to prove that $\neg p$ is true.

> __Recall__
> The contrapositive of $p \to q$ is $\neg q \to \neg p$.

**Example**

$\forall n \in \mathbb{Z}$ if $n^2$ is even, then $n$ is even.

**_Solution_**

_Proof_ (by contrapositive): Supposed $n$ is odd, then,

$$ n = 2k+1 $$

and,

$$
    n^2 = (2k + 1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1.
$$

Since $2k^2 + 2k$ is an integer,

$$
    \therefore n^2 = 2(2k^2 + 2k) + 1 \text{ is odd.}
$$

## Proof by Contradiction

To show $p \to q$ assume that $p$ and $\neg q$ are true. Then, using known results, arrive at some contradiction.

> Show it's impossible for $\neg q$ to be true, and therefore for $q$ is true.

### Fact

If $x$ is a rational number ($x \in \mathbb{Q}$) then,

$$
    x = \frac{a}{b}
$$

where $a,b \in \mathbb{Z}$.

**Example**

Prove that $\sqrt{2}$ is irrational.

#### Soluiton

_Proof_: Suppose to the contrary that $\sqrt{2}$ is rational, then,

$$
    \sqrt{2} = \frac{a}{b}
$$

where $a,b \in \mathbb{Z}$.

Without loss of generality (WLOG), $a$ and $b$ are in reduced form. In particular $a$ and $b$ are not both even.

So,

$$
    2 = \frac{a^2}{b^2}
$$

and,

$$
    2 \cdot b^2 = a^2
$$

Therefore $a^2$ is even and by the previous proof $a$ is also even and can be written,

$$
    a = 2k
$$

for some $k \in \mathbb{Z}$.

Now,

$$
    2b^2 = (2k)^2 = 4k^2
$$

and,

$$
    b^2 = 2k^2
$$

thus $b$ is also even which is a contradiction.

$$
    \therefore \sqrt{2} \text{ is irrational.}
$$
