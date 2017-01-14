
# Section 2.1 &ndash; Sets

_definition_: A __set__ is a collection of objects. The objects are called __elements__ or __members__.

* If $x$ is and element of set $S$ then we write $x \in S$.

## Explicit Listing Notation

Listing all the elements in a set.

**Examples**

$$
    A = \{ 1,2 \}
$$
$$
    B = \{ a,b,c \}
$$
$$
    C = \{ -1, \pi, \text{cat} \}
$$
$$
    D = \{ \{\underset{\text{set}}a\},\underset{\text{set}}B, \underset{\text{#}}5 \}
$$

## Implicit Listing Notation

List enough elements to make the pattern obvious.

**Examples**

$$
    \{ 2,4,6,8,... \}
$$
$$
    \mathbb{Z} = \{ ..., -3,-2,-1,0,1,2,3,... \}
$$
$$
    \mathbb{Z}+ = \{ 1,2,3,... \}
$$
It's debated whether or not the natural numbers contain $0$.
$$
    \mathbb{N} = \{ 1,2,3,... \}
$$
$$
    \mathbb{N}_0 = \{ 0,1,2,3,... \}
$$

## Set Builder Notation

Describe the elements by providing some characteristic of them.

**Example**

Suppose we want the prime numbers,

$$
    \{ x : x \text{ is prime} \}
$$

Translates to "All values of $x$ such that $x$ is prime".

**Examples**

$$
    \{ n \in \mathbb{Z} : n < 20, n \text{ is even}, n > 0 \} = \{ 2,4,6, ... , 18 \}
$$
$$
    \mathbb{Q} = \{ \frac{a}{b} : a,b \in \mathbb{Z}, b \neq 0 \}
$$
$$
    \mathbb{C} = \{ a + bi : a, b \in \mathbb{R} \}
$$

## Set Properties

_definition_: Sets $A$ and $B$ are equal ($A = B$) if they have the same elements. That is,

$$
    x \in A \iff x \in B
$$

#### Note:

* Sets are unordered,

$$
    \{ 1,2,3 \} = \{ 3,1,2 \}
$$

* Unless specified repeated elements are ignored,

$$
    \{ 1,2,2,3,3,3 \} = \{ 1,2,3 \}
$$

## Empty Set

_definition_: The __empty set__ is the set with no elements written, $\emptyset$ or $\{\}$.

**Example**

The years that Vancouver has won the Stanley Cup $= \emptyset$.

**Example**

$$
    \{ \frac{a}{b} \in \mathbb{Q} : \frac{a}{b} = \sqrt{2} \} = \emptyset
$$

**Example**

Does $\emptyset = \{ \emptyset \}$?

**_Solution_**

No. The second set has one element, the first set has no elements.

**Example**

How many elements does,

$$
    \{ \emptyset, \{ \emptyset, \{ \{ \emptyset \} \} \}, \{ \emptyset \} \}
$$

have?

**_Solution_**

Three,

* $\emptyset$
* $\{ \emptyset, \{ \{ \emptyset \} \} \}$
* $\{ \emptyset \}$

## Subsets

_definition_: Let $A$ and $B$ be sets. $A$ is a __subset__ of $B$ ($A \subseteq B$) if every element in $A$ is also in $B$ (but not necessarily the reverse). That is $x \in A \Rightarrow x \in B$.

*  If $A$ is not a subset of $B$ we write $A \not\subseteq B$


**Example**

Let $A = \{ 1 ,2 , \emptyset \}$ and $B = \{ 1,3,A \}$. Which of the following are true?

1. $\emptyset \in A$
2. $\{ 1 \} \in A$
3. $2 \in B$
4. $A \in B$
5. $\{A\} \in B$
6. $A \subseteq B$

**_Solution_**

Only 1 and 4 are true. 2, 3, 5 and 6 are false.

## Proper Subsets

_definition_: $A$ is a __proper subset__ of $B$ if $A \subseteq B$ and $A \neq B$. It is written $A \subset B$.

## Properties of Sets

* Any set $S$ has $S \subseteq S$.
* Any set $S$ has $\emptyset \subseteq S$.
* An $n$ element set has $2^n$ subsets.

**Example**

How many subsets does $\{ a,b \}$ have?

**_Solution_**

Four,

* $\{ a \}$
* $\{ b \}$
* $\{ a, b \}$
* $\emptyset$

## The Transitive Property of Subsets

If $A$, $B$ and $C$ are sets such that,

$$
    A \subseteq B \text{ and } B \subseteq C
$$

then,

$$
    A \subseteq C
$$

### Proof

(RTP: Must show every element  in $A$ is also in $C$)

Suppose that $A \subseteq B$ and $B \subseteq C$. Let $x \in A$. So then since $A \subseteq B$, $x \in B$. And so, since $B \subseteq C$, $x \in C$.

$$
    \therefore A \subseteq C
$$

### Proposition

Let $A$ and $B$ be sets. $A = B$ if and only if $A \subseteq B$ and $B \subseteq A$.

Must show:

* $A = B \Rightarrow A \subseteq B \text{ and } B \subseteq A$
* $A \subseteq B \text{ and } B \subseteq A \Rightarrow A = B$

($\Rightarrow$) Suppose $A = B$. Let $x \in A$, and so $x \in B$ since $A = B$.

$$
    \therefore A \subseteq B
$$

Let $y \in B$, and so $y \in A$, since $A = B$

$$
    \therefore B \subseteq A
$$

($\Leftarrow$) Suppose $A \subseteq B$ and $B \subseteq A$. Suppose then to the contrary $A \neq B$.

WLOG, $\exists x \in A \text{ such that } x \not\in B$.

Which is a contradiction since $A \subseteq B$.

$$
    \therefore A = B
$$

## Power Sets

_defnition_: The __power set__ of a set $A$ (denoted $\mathcal{P}(A)$) is the set whose elements are the subsets of $A$.

**Example**

Let $A = \{ a, b, \}$. What is the power set of $A$?

Subsets of $A$ are:

* $\{ a \}$
* $\{ b \}$
* $\{ a, b \}$
* $\emptyset$

**_Solution_**

$$
    \mathcal{P}(A) = \{\{ a \}, \{ b \}, \{ a, b \}, \emptyset \}
$$

## Properties of Power Sets

Let $\mathcal{P}(A)$ be a power set of $A$.

* Every element of $\mathcal{P}(A)$ is a set.
* If $A$ has $n$ elements, $\mathcal{P}(A)$ has $2^n$ elements.
* $\emptyset \in \mathcal{P}(A)$
* $A \in \mathcal{P}(A)$
* $X \in \mathcal{P}(A) \iff X \subseteq A$

### Proposition

Let $A$ and $B$ be sets.

$$
    A \subseteq B \iff \mathcal{P}(A) \subseteq \mathcal{P}(B)
$$

($\Rightarrow$) Suppose $A \subseteq B$. Let $X \in \mathcal{P}(A)$. Then $X \subseteq A \subseteq B$.

$$
    \therefore X \subseteq B \text{ and } X \in \mathcal{P}(B)
$$
$$
    \therefore \mathcal{P}(A) \subseteq \mathcal{P}(B)
$$

($\Leftarrow$) Suppose $\mathcal{P}(A) \subseteq \mathcal{P}(B)$. Recall $A \subseteq \mathcal{P}(A) \subseteq \mathcal{P}(B)$.

$$
    \therefore A \in \mathcal{P}(B)
$$
$$
    \therefore A \subseteq B
$$