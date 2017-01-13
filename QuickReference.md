# MATH 122 Quick Reference

## Statements

### Conjunction

Let $p$ and $q$ be statements. The conjunction of $p$ and $q$ is written:

$$
	p \wedge q 
$$

#### Truth Table

| $p$   | $q$   | $p \wedge q$ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | False          |
| False | False | False          |

### Disjunction

Let $p$ and $q$ be statements. The disjunction[^math-inclusive-or] of $p$ and $q$ is written:
[^math-inclusive-or]: In mathematics or is always inclusive.

$$
	p \vee q 
$$

#### Truth Table

| $p$   | $q$   | $p \vee q$ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | True           |
| False | True  | True           |
| False | False | False          |

### Implication

Let $p$ and $q$ be statements. The implication of $p$ to $q$ is written:

$$
	p \rightarrow q 
$$

This implies a `if p then q` relationship.

#### Truth Table

| $p$   | $q$   | $p \rightarrow q$ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | True           |
| False | False | True           |

### Bicondition or Double Implication

* Means $p \to q$ and $q \to p$
* $p$ and $q$ have the same truth value


| $p$   | $q$   | $p \leftrightarrow q$ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | False           |
| False | False | True           |

Said as "$p$ if and only if $q$" or "$p$ iff $q$"

### Negation

_definition_: The __negation__ of a statement $p$, written:

$$
	\neg p 
$$


| $p$   | $\neg p$   |
|-------|-------|
| True  | False |
| False  | True |

Notation: $\neg$ supersedes any other notation. So:

$$
	\neg p \vee q = (\neg p) \vee q 
$$

### Contrapositive

_definition_: The __contrapositive__ of $p \to q$ is written:

$$
	\neg q ~ \to ~ \neg p 
$$

### Converse

_definition_: The __converse__[^f1] of $p \to q$ is written:

$$
	q \to p 
$$


### Quantifiers

#### Universal Quantifier

"_For all_ integers $n$, $2n$ is even".

_For all_ is the quantifier as it quantifies the amount. In this case it is the __universal quantifier__ equivalent to:

* For all... (duh)
* For each...
* For every...
* $\forall$

#### Existential Quantifier

_definition_: The __existential quantifier__ states that this statement applies for some but not all things. It can be written:

* For some...
* There exists a...
* $\exists$

### Laws of Logic

#### Idempotence

$$
	p \vee p \iff p 
$$
$$
	p \wedge p \iff p 
$$

#### Commutative

$$
	p \vee q \iff q \vee p 
$$
$$
	p \wedge q \iff q \wedge p 
$$

#### Associative

$$
	(p \vee q) \vee r \iff p \vee (q \vee r) 
$$
$$
	(p \wedge q) \wedge r \iff p \wedge (q \wedge r) 
$$

Note, 

$$
	(p \wedge q) \vee r \nLeftrightarrow p \wedge (q \vee r) 
$$

#### Distributive

$$
	p \wedge (q \vee r) \iff (p \wedge q) \vee (p \wedge r) 
$$
$$
	p \vee (q \wedge r) \iff (p \vee q) \wedge (p \vee r) 
$$


#### DeMorgan's Laws

$$
	\neg ( p \wedge q ) = (\neg p) \vee (\neg q) 
$$

$$
	\neg ( p \vee q ) = (\neg p) \wedge (\neg q) 
$$

#### Identity

$$
	p \wedge \mathbb{1} \iff p
$$
$$
	p \vee \mathbb{0} \iff p
$$

#### Dominance

$$
	p \wedge \mathbb{0} \iff \mathbb{0} 
$$
$$
	p \vee \mathbb{1} \iff \mathbb{1} 
$$

#### Other

$$
	p \to q \iff \neg p \vee q 
$$
$$
	\neg p \to q \iff p \vee q 
$$
$$
	p \leftrightarrow q \iff (p \to q) \wedge (q \to p) \iff (\neg p \vee q) \wedge (p  \vee \neg q ) 
$$

## Proofs

### Direct Proof

To show $ p \to q $, assume $p$ is true, then use known results (e.g. facts, logical equivalents) to show that $q$ is also true.

### Proof by Contrapositive

Assume that $\neg q$ is true, then use known result to prove that $\neg p$ is true.

> __Recall__  
> The contrapositive of $p \to q$ is $\neg q \to \neg p$.

### Proof by Contradiction

To show $p \to q$ assume that $p$ and $\neg q$ are true. Then, using known results, arrive at some contradiction.

> Show it's impossible for $\neg q$ to be true, and therefore for $q$ is true.

## Sets

### Properties

#### Equality

_definition_: Sets $A$ and $B$ are equal ($A = B$) if they have the same elements. That is,

$$
    x \in A \iff x \in B
$$

or

$$
    A = B \iff A \subseteq B \wedge B \subseteq A
$$

#### Other

* Any set $S$ has $S \subseteq S$.
* Any set $S$ has $\varnothing \subseteq S$.
* An $n$ element set has $2^n$ subsets.

__Note:__

* Sets are unordered,

$$
    \{ 1,2,3 \} = \{ 3,1,2 \}
$$

* Unless specified repeated elements are ignored,

$$
    \{ 1,2,2,3,3,3 \} = \{ 1,2,3 \}
$$

### Subsets

_definition_: Let $A$ and $B$ be sets. $A$ is a __subset__ of $B$ ($A \subseteq B$) if every element in $A$ is also in $B$ (but not necessarily the reverse). That is $x \in A \Rightarrow x \in B$.

*  If $A$ is not a subset of $B$ we write $A \not\subseteq B$
*  If $A$ is only a subset of $B$ ($A \neq B$), we call is a proper subset we write $A \subsetneq B$.

### Special Sets

#### Empty Set

_definition_: The __empty set__ is the set with no elements written, $\varnothing$ or $\{\}$.

#### Universe

_definition_: The __universe__ is all the objects that can occur in the set. Written,

$$
\mathcal U
$$

### Power Sets

_defnition_: The __power set__ of a set $A$ (denoted $\mathcal{P}(A)$) is the set whose elements are the subsets of $A$.

Let $A = \{ a, b, \}$. 

$$
    \mathcal{P}(A) = \{\{ a \}, \{ b \}, \{ a, b \}, \varnothing \}
$$

#### Properties

Let $\mathcal{P}(A)$ be a power set of $A$.

* Every element of $\mathcal{P}(A)$ is a set.
* If $A$ has $n$ elements, $\mathcal{P}(A)$ has $2^n$ elements.
* $\varnothing \in \mathcal{P}(A)$
* $A \in \mathcal{P}(A)$
* $X \in \mathcal{P}(A) \iff X \subseteq A$
* $A \subseteq B \iff \mathcal{P}(A) \subseteq \mathcal{P}(B)$

### Operations

#### Union

_definition_: Let $A$ and $B$ be sets. The __union__ of $A$ and $B$ (denoted $A \cup B$) is the set,

$$
    A \cup B = \{ x : x \in A \vee x \in B \}
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/3/30/Venn0111.svg/1280px-Venn0111.svg.png)

#### Intersection

_defninition_: The __intersection__ of $A$ and $B$ (denoted $A \cap B$) is the set,

$$
    A \cap B = \{ x : x \in A \wedge x \in B \}
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Venn0001.svg/1280px-Venn0001.svg.png)

#### Set Difference

$$
    A \setminus B = B \cap A^C
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/Venn0010.svg/1200px-Venn0010.svg.png)

#### Symmetric Difference

$$
    A \oplus B = B \oplus A
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Venn0110.svg/1280px-Venn0110.svg.png)


#### Compliment

$$
    A^C = \mathcal U \setminus A
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Venn1010.svg/1280px-Venn1010.svg.png)

#### Cartesian Product

_definition_: The __cartesian product__ of $A$ and $B$ is,

$$
    A \times B = \{ (a,b): a \in A, b \in B \}
$$

__Note:__

In ordered pairs,

$$
    (a,b) \neq (b,a)
$$

#### Example

$$
    A = \{ 1,2 \}
$$
$$
    B = \{ x,y,z \}
$$

##### Solution

$$
    A \times B = \{ (1,x), (1,y), (1,z), (2,x), (2,y), (2,z) \}
$$
$$
    B \times A = \{ (x,1), (x,2), (y,1), (y,2), (z,1), (z,2) \}
$$

## Relations

_definition_: A __binary relation__  from a set $A$ to a set $B$ is a subset,

$$
    \mathcal R \subseteq A \times B.
$$

__Note:__

Binary refers to a relationship between 2 sets, and we will only consider binary relationships in this course.

#### Notation

When an ordered pair $(a,b)$ is in a relationship $\mathcal R$ we say "$a$ is related to $b$" and write $(a,b) \in \mathcal R$ or, using Infix notation,

$$
    a \mathcal R b
$$

### Types

For a relation $\mathcal R_1$ on a $A \times A, \mathcal R$ is,

#### Reflexive

If $(x,x) \in \mathcal R$ for all $x \in A$.

#### Symmetric

If $(y,x) \in \mathcal R$ whenever $(x,y) \in \mathcal R$.

#### Antisymmetric

If $(x,y) \in \mathcal R$ and $(y,x) \in \mathcal R$ then $x = y$.

__Note:__

This is not the same as not symmetric (Antisymmetric $\not\Leftrightarrow$ not Symmetric ).

#### Transitive

If $(x,y) \in \mathcal R$ and $(y,z) \in \mathcal R$ then $(x,z) \in \mathcal R$.

__Note:__

It is possible for $x = z$.

### Equivalence

_definition_: A relation $\mathcal R$ on a set $A$ is an __equivalence relationship__ if it is,

1. Reflexive
2. Symmetric
3. Transitive


