
# Section 2.3 - Binary Relations

_definition_: A __binary relation__  from a set $A$ to a set $B$ is a subset,

$$
    \mathcal R \subseteq A \times B.
$$

### Note:

Binary refers to a relationship between 2 sets, and we will only consider binary relationships in this course.

**Example**

* $A = \{ 1,2,3 \}$
* $B = \{ x,y,z \}$

$$
    A \times B  = \{ (1,x), (1,y), (1,z), (2,x), (2,y), (2,z),(3,x),(3,y),(3,z)\}
$$

$$
    \mathcal R_1 = \{ (1,x), (1,z), (2,y), (2,z) \}
$$

$$
    \mathcal R_2 = \{ (1,x), (1,y), (1,z) \}
$$

$$
    \mathcal R_3 = \{ (1,x), (2,y), (3,z) \}
$$

$$
    \mathcal R_4 = A \times B
$$
$$
    \mathcal R_5 = \emptyset
$$

## Notation

When an ordered pair $(a,b)$ is in a relationship $\mathcal R$ we say "$a$ is related to $b$" and write $(a,b) \in \mathcal R$ or, using Infix notation,


$$
    a \mathcal R b
$$

$$
   3 \not\mathcal R z
$$

## Types of Relations

For a relation $\mathcal R_1$ on a $A \times A, \mathcal R$ is,

### Reflexive

If $(x,x) \in \mathcal R$ for all $x \in A$.

### Symmetric

If $(y,x) \in \mathcal R$ whenever $(x,y) \in \mathcal R$.

## Relations

A set that defines a relationship between two or more sets.

## Antisymmetry

If $(x,y) \in \mathcal R$ and $(y,x) \in \mathcal R$ then $x = y$.

This is not the same as not symmetric (Antisymmetric $\not\Leftrightarrow$ not Symmetric ).

## Transitivity

If $(x,y) \in \mathcal R$ and $(y,z) \in \mathcal R$ then $(x,z) \in \mathcal R$.

__Note__: It is possible for $x = z$.
