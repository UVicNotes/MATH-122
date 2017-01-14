
## Union

_definition_: Let $A$ and $B$ be sets. The __union__ of $A$ and $B$ (denoted $A \cup B$) is the set,

$$
    A \cup B = \{ x : x \in A \vee x \in B \}
$$

## Intersection

_defninition_: The __intersection__ of $A$ and $B$ (denoted $A \cap B$) is the set,

$$
    A \cap B = \{ x : x \in A \wedge x \in B \}
$$

**Example**

Let $W = \{ a,b,c,d,e \}$ and $V = \{ a,b,c,x,y,z \}$.

**_Solution_**

$$
    W \cup V = \{ a,b,c,d,e,x,y,z \}
$$
$$
    W \cap V = \{ a,b,c \}
$$


**Example**

* $A = \{ a, b, c \}$
* $B = \{x,y,z\}$
* $C = \{a,b,x,z\}$
* $\mathcal{U} = \{ a,b,x,y,z \}$

**_Solution_**


## Set Difference

$$
    A \setminus B
$$

![](http://upload.wikimedia.org/wikipedia/commons/8/83/Set_difference.svg)

## Symmetric Difference

$$
    A \oplus B = B \oplus A
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Venn0110.svg/1280px-Venn0110.svg.png)

## Universe

All the objects that can occur in the set.

$$
\mathcal U
$$

## Compliment

$$
    A^C = \mathcal U \setminus A
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Venn1010.svg/1280px-Venn1010.svg.png)


### Theorem

For sets $A$ and $B$,

$$
    (A \cup B)^C = A^C \cap B^C
$$

#### Proof

1) Show $(A \cup B)^C \subseteq A^C \cap A^C$

Let $x \in (A \cup B)^C$, so $x \not\in A$ and $x \not\in B$.

Thus $x$ is in $A^C$ and $B^C$.
$$
    \therefore x \in A^C \cap B^C
$$

2) Show $A^C \cap B^C  \subseteq (A \cup B)^C$

$x \in A^C \cap B^C$, so $x \in A^C$ and $x \in B^C$.

Then $x \not\in A$ and $x \not\in B$.

$$
    \therefore x \not\in A \cup B
$$
$$
    \therefore x \in (A \cup B)^C
$$
$$
    \therefore A^C \cap B^C \subseteq (A \cup B)^C
$$

Thus $(A \cup B)^C = A^C \cap B^C$.

## Cartesian Product

_definition_: The __cartesian product__ of $A$ and $B$ is,

$$
    A \times B = \{ (a,b): a \in A, b \in B \}
$$

### Note:

In ordered pairs,

$$
    (a,b) \neq (b,a)
$$

**Example**

$$
    A = \{ 1,2 \}
$$
$$
    B = \{ x,y,z \}
$$

**_Solution_**

$$
    A \times B = \{ (1,x), (1,y), (1,z), (2,x), (2,y), (2,z) \}
$$
$$
    B \times A = \{ (x,1), (x,2), (y,1), (y,2), (z,1), (z,2) \}
$$

### Fact

For any set $A$,

$$
    A \times \emptyset = \emptyset
$$

### Proposition

$$
    A \times (A \cup C) \subseteq (A \times B) \cup (A \times C)
$$

#### Proof

Let $(x,y) \in A \times (B \cup C)$, then $x \in a$ and $y \in B \cup C$.

##### Case 1:

If $y \in B$, then,

$$
    (x,y) \in A \times B
$$

##### Case 2:

If $y \in C$, then,

$$
    (x,y) \in A \times C
$$

In either case $(x,y) \in (A \times B) \cup (A \times C)

$$
    \therefore A \times (A \cup C) \subseteq (A \times B) \cup (A \times C)
$$


**Example**

$$
    A = \{ 1,2 \}
$$

$$
    \mathcal P (A) = \{ \{ 1 \}, \{ 2 \}, \{ 1,2 \}, \emptyset \}
$$

**_Solution_**

$$
    A \not\subseteq \mathcal P (A)
$$

$$
    A \in \mathcal P (A)
$$

## Venn Diagrams

Can help us see that,

$$
    A^C \cap B = (A \cup B ) \setminus A
$$

but it doesn't prove it.

**Example**

Show by counter example that,

$$
    A \setminus (B \setminus C) \neq (A \setminus B) \setminus C
$$

![](http://www.math.csusb.edu/notes/sets/setsex5/venn3p.gif)

**_Solution_**

* $A \to 2,3,5,6$
* $B \to 3,4,5,7$
* $C \to 5,6,7,8$

$$
    A \setminus (B \setminus C) \to 2,5,6
$$

$$
    (A \setminus B) \setminus C \to 1
$$

$$
    1 \neq 2,5,6
$$

$$
    \therefore A \setminus (B \setminus C) \neq (A \setminus B) \setminus C
$$
