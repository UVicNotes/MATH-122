# Section 4.4 -- Congruences

_definition_: For a natural number $n \gt 1$, given integers $a$ and $b$, we says, $a$ is __congruent__ to $b$ modulo $n$,

$$
    a \equiv b \pmod n
$$

if,

$$
    n \mid (a - b)
$$

or $\frac{a}{n}$ and $\frac{b}{n}$ have the same remainder.

**Example**

Since,

$$\begin{aligned}
    9 &\equiv 2 \pmod 7 \newline
    16 &\equiv 9 \pmod 7 \newline
\end{aligned}$$

 we can say,

 $$
    2 \equiv 16 \equiv 9 \pmod 7
 $$

**Example**

It's 11 AM. What time will it be in 22 hours?

**_Solution_**

It will be 9 AM (not 33 AM).

Why? Times rollover after 24 hours.

**Example**

Draw a $405^\circ$ ray.

**_Solution_**

Since angles rollover after $360^\circ$, we can draw $45^\circ$.

## Least Residue mod $n$

_definition_:For integers $a$ and $b$ where $a \equiv b \pmod n$, we say $b$ is the __least residue mod $n$__ if $0 \le b \le n$.


### Notice

$$
    \equiv \mod n
$$

is an equivalence relation with equivalence classes,

$$
    [0],[1],[2],...,[n-1]
$$

**Example**

The equivalence classes for $\bmod 3$ are,

$$\begin{aligned}
    \left[0\right] &= \{...,-9,-6,-3,0,3,6,9,... \} \newline
    [1] &= \{ ...,-8,-5,-2,1,4,7,... \} \newline
    [2] &= \{ ...,-7,-4,-1,2,5,8,... \} \newline
\end{aligned}$$

## Arithmetic $\bmod n$

### Proposition

Let $a,b,c,d \in \mathbb Z$ and $n \in \mathbb N$, if,

$$\begin{aligned}
    a &\equiv b \pmod n \newline
    c &\equiv d \pmod n \newline
\end{aligned}$$

then,

$$\begin{aligned}
    a + c &\equiv b + d \pmod n \newline
    a - c &\equiv b - d \pmod n \newline
    a \cdot c &\equiv b \cdot d  \pmod n \newline
\end{aligned}$$

#### Proof

Suppose $a \equiv b \pmod n$ and $a \equiv d \pmod n$ so,

$$
    n \mid a - b
$$

and,

$$
    n \mid c - d
$$

so,

$$\begin{aligned}
    a - b &= nk \text{ for some } k \in \mathbb Z \newline
    a - d &= n\ell \text{ for some } \ell \in \mathbb Z \newline
\end{aligned}$$

so,

$$\begin{aligned}
    a &= nk + b \newline
    c &= n\ell + d \newline
\end{aligned}$$

so,

$$\begin{aligned}
    a + c &= (nk + b) + (n\ell + d) \newline
    &= n(\ell + k) + (b+d) \newline
\end{aligned}$$

therefore,

$$\begin{aligned}
    (a+b)-(b+d) &= n(\ell+k)\newline
\end{aligned}$$

$$\begin{aligned}
    n \mid (a+c)-(b+d)
\end{aligned}$$

$$\begin{aligned}
    a+c \equiv b+d \pmod n
\end{aligned}$$

### Warning

$$
    ac \equiv bd \pmod n
$$

__does not imply__ $a \equiv b \pmod n$

**Example**

Let $b \equiv 2 \pmod 4$,

$$\begin{aligned}
    2\cdot3 &\equiv 2 \cdot 1 \pmod 4 \newline
    3 &\not\equiv 1 \pmod 4 \newline
\end{aligned}$$

### Proposition

If $ac \equiv bc \pmod n$ __and__ $\gcd(c,n) = 1$ then,

$$
    a \equiv b \pmod n
$$

**Example**

Solve,

$$
    3x - 34 \equiv 2 \pmod 7
$$

**_Solution_**

$$\begin{aligned}
    3x - 34 &\equiv 2 \pmod 7 \newline
    3x &\equiv 3 + 34 \pmod 7 \newline
    3x &\equiv 36 \pmod 7 \newline
    3x &\equiv 3 \cdot 12 \pmod 7 \newline
\text{since $\gcd(3,7) = 1$} \newline
    x &\equiv 12 \pmod 7 \newline
    &\equiv 5 \pmod 7
\end{aligned}$$

**Example**

Solve,

$$
    2x \equiv 30 \pmod 4
$$

**_Solution_**

By trial and error, let $x \in [0]$,

$$
    2(0) \equiv 0 \not\equiv 30 \pmod 4
$$

(note $30 \pmod 4 \equiv 2 \pmod 4$), let $x \in [1]$,

$$
    2(1) \equiv 2 \pmod 4
$$

let $x \in [2]$,

$$
    2(2) \equiv 4 \not\equiv 2 \pmod 4
$$


### Fact

$$
    9 \equiv -1 \pmod{10}
$$

**Example**

Find the last digit of $3^{123}$.

**_Solution_**

We can find $3^{123} \pmod{10}$ instead

$$\begin{aligned}
    3^{123} &= 3^{120+3} \newline
    &= 3^{2 \cdot 60 + 3} \newline
    &= (3^2)^{60} \cdot 3^3 \newline
    &= 9^{60} \cdot 3^3 \newline
    &\equiv (-1)^{60} \cdot 3^3 \pmod{10} \newline
    &\equiv 27 \pmod{10} \newline
    &\equiv 7 \pmod{10} \newline
\end{aligned}$$

### Application of Divisibility by 3

Notice if $3 \mid n$, then,

$$
    n \equiv 0 \pmod{3}
$$

also,

$$
    10 \equiv 1 \pmod{3}
$$

To test if $3 \mid n$ we will start by writing,

$$\begin{aligned}
    n &= d_k 10^k + d_{k-1} 10^{k-1} + d_{k-2} 10^{k-2} + ... + d_0 10^0 \newline
    &\equiv d_k + d_{k-1} + d_{k-2} + ... + d_0 \pmod{3} \newline
\end{aligned}$$

so

$$
    3 \mid n \iff 3 \mid \left( d_k + d_{k-1} + d_{k-2} + ... + d_0 \right)
$$