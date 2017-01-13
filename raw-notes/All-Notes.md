# Lecture 1 - Notes  

### May 5, 2015  

## Why Math 122?

It's thought in elementary school that everything builds up to calculus. This ignores a bunch of things like Analysis, Algebra and Combinatorics.

### Foundations

We're going to look at:

* Sets
* Relations
* Functions

#### Example

> * Socrates is a man  
> * All men are mortal  
> Is socrates Mortal?

__Solution__: Yes. Socrates is mortal.

## Chapter 0.1: Compound Statements

_definition_: A __statement__ or __proposition__ has a truth value.

#### Examples

If we denote our statement as `p`.

```
p = "7 is a prime number"
```

In this case `p = true`.

```
q = "The square root of 2 is an integer"
```

In this case `q = false`.

```
r = "Every positive integer except two is the sum of two primes"

e.g.

6 = 3 + 3
10 = 3 + 7

```

This statement is unknown and is an outstanding question in mathematics.

#### _Non_ Examples

```
"Is 187698736 prime?"
```

This is a _question_ not a statement.

```
"If n is even"
```

This is a _condition_ not a statement.

---

_definition_: A __compound statement__ is formed by combining multiple statements.

### Conjunction

Let $p$ and $q$ be statements. The conjunction of $p$ and $q$ is written:

$$ p \wedge q $$

#### Truth Table

| $p$   | $q$   | $ p \wedge q $ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | False          |
| False | False | False          |

### Disjunction

Let $p$ and $q$ be statements. The disjunction[^math-inclusive-or] of $p$ and $q$ is written:
[^math-inclusive-or]: In mathematics or is always inclusive.

$$ p \vee q $$

#### Truth Table

| $p$   | $q$   | $ p \vee q $ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | True           |
| False | True  | True           |
| False | False | False          |

### Implication

Let $p$ and $q$ be statements. The implication of $p$ to $q$ is written:

$$ p \rightarrow q $$

This implies a `if p then q` relationship.

#### Truth Table

| $p$   | $q$   | $ p \rightarrow q $ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | True           |
| False | False | True           |

		
# Lecture 2 - Notes  

### May 6, 2015  

## Section 0.1 Continued

### Implication

$$ p \rightarrow q $$

$p$ is the _hypothesis_, $q$ is the _conclusion_.

* $p$ is sufficient for $q$
* $q$ is necessary for $p$

#### Examples

(9 is odd) $\to$ (cats have fur)

This is `true`, because nine is odd.

---

(Fish live on land) $\to$ (10 is prime)

This is `false` because fish don't live on land.

### Bicondition or Double Implication

* Means $ p \to q $ and $ q \to p $
* $p$ and $q$ have the same truth value


| $p$   | $q$   | $ p \leftrightarrow q $ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | False           |
| False | False | True           |

Said as "$p$ if and only if $q$" or "$p$ iff $q$"

### Negation

_definition_: The __negation__ of a statement $p$, written:

$$ \rightharpoondown p $$


| $p$   | $\rightharpoondown p $   |
|-------|-------|
| True  | False |
| False  | True |

Notation: $\rightharpoondown$ supersedes any other notation. So:

$$ \rightharpoondown p \vee q = (\rightharpoondown p) \vee q $$

#### DeMorgan's Laws

$$ \rightharpoondown ( p \wedge q ) = (\rightharpoondown p) \vee (\rightharpoondown q) $$

$$ \rightharpoondown ( p \vee q ) = (\rightharpoondown p) \wedge (\rightharpoondown q) $$


#### Example

$p =$ "John owns a cat"

$q =$ "John owns a dog"

Find:

$$ \rightharpoondown ( p \wedge q ) $$

##### Solution

We only need to break on one half to negate it. 

So $ \rightharpoondown ( p \wedge q ) =$ "John doesn't own a cat or he does not own a dog"


### Contrapositive

_definition_: The __contrapositive__ of $p \to q$ is written:

$$ \rightharpoondown q ~ \to ~ \rightharpoondown p $$

#### Example

The contrapositive of "If it rains in the morning I will bring an umbrella" is "If I did not bring an umbrella than it did not rain this morning".

### Converse

_definition_: The __converse__[^f1] of $p \to q$ is written:

$$ q \to p $$

#### Example

The converse of "If it rains in the morning I will bring an umbrella" is "If I brought an umbrella it was raining this morning"[^f2].

[^f1]: While the contrapositive is is logically equivalent to the statement the converse is not.
[^f2]: this is not logically equivalent.


| $p$   | $q$   | $ p \to q $ | $ \rightharpoondown q \to \rightharpoondown p $ | $ q \to p $ |
|---|---|---|---|---|
| True  | True  | True | True | True |
| True  | False | False | False | True |
| False | True  | True | True | False |
| False | False | True | True | True |

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

#### Example

"Some rectangles are squares" can be written "$\exists$ a rectangle $R$, such that $R$ is square"




# Lecture 3 - Notes  

### May 8, 2015  

## Section 0.1 Continued

#### Example

Write the following in plain english:

$$ \forall x, \exists y, x + y = 0 $$

Where the universe of $x$ and $y$ is the integers. 

##### Solution

For all integers $x$ there exists a $y$ such that the sum of $x$ and $y$ is zero.

#### Example

Write the following in plain english:

$$ \exists y, \forall x, x + y = 0 $$

Where the universe of $x$ and $y$ is the integers. 

##### Solution

This is not true because there not all $x$'s would make zero for any $y$.

### Negation of Quantifiers

$$ \neg \forall ~ x, s(x) = \exists ~ x, \neg s(x) $$
$$ \neg \exists ~ x, s(x) = \forall ~ x, \neg s(x) $$

#### Example

Prove,

$$ \neg (\forall ~ n \ge 0, n^2 - n + 41 ~\text{is prime}) $$

##### Solution

This becomes,

$$ \exists ~ n \ge 0, n^2 - n + 41 ~\text{is not prime} $$

Which we can prove by example.

### Set Notation

$$ \mathbb{Z} = \text{The set of all integers} $$

$$ \mathbb{R} = \text{The set of all real numbers} $$

$$ \mathbb{N} = \text{The set of all natural numbers} $$

$$ \mathbb{Q} = \text{The set of all rational numbers} $$

$ \in $ denotes that something belongs to a set.

#### Example

$$ x \in \mathbb{Z} = x \text{ is an integer} $$

## Section 1.1 - Truth Tables

#### Example

Construct,

$$ (\neg p \to r) \to (q ~\vee \neg r) $$

##### Solution

A giant truth table.

## Section 1.2 - The Algebra of Propositions

If a statement is always true we call it a __tautology__. For example,

$$ p ~\vee \neg p $$

If a statement is always false we call it a __contradiction__. For example,

$$ p ~\wedge \neg p $$

### Logical Equivalence

_definition_: Two statements, $s_1$ and $s_2$ are __logically equivalent__ if the biconditional, $ s_1 \leftrightarrow s_2 $, is a tautology. It is then written,

$$ s_1 \iff s_2 $$

($ s_1 \leftrightarrow s_2 $ is a statement that can be true or false, $ s_1 \iff s_2 $ is a fact that they are logically equivalent)

#### Notation


* $\mathbb{1}$ denotes a tautological statement.
* $\mathbb{0}$ denotes a contradiction statement.

### Laws of Logic

#### Idempotence

$$ p \vee p \iff p $$
$$ p \wedge p \iff p $$

#### Commutative

$$ p \vee q \iff q \vee p $$
$$ p \wedge q \iff q \wedge p $$

#### Associative

$$ (p \vee q) \vee r \iff p \vee (q \vee r) $$
$$ (p \wedge q) \wedge r \iff p \wedge (q \wedge r) $$

Note, 

$$ (p \wedge q) \vee r \nLeftrightarrow p \wedge (q \vee r) $$


#### Distributive

$$ p \wedge (q \vee r) \iff (p \wedge q) \vee (p \wedge r) $$
$$ p \vee (q \wedge r) \iff (p \vee q) \wedge (p \vee r) $$


#### DeMorgan's Laws

$$ \neg ( p \wedge q ) = (\neg p) \vee (\neg q) $$

$$ \neg ( p \vee q ) = (\neg p) \wedge (\neg q) $$



#### Identity

$$ p \wedge \mathbb{1} \iff p$$
$$ p \vee \mathbb{0} \iff p$$

#### Dominance

$$ p \wedge \mathbb{0} \iff \mathbb{0} $$
$$ p \vee \mathbb{1} \iff \mathbb{1} $$

#### Other

$$ p \to q \iff \neg p \vee q $$
$$ \neg p \to q \iff p \vee q $$
$$ p \leftrightarrow q \iff (p \to q) \wedge (q \to p) \iff (\neg p \vee q) \wedge (p  \vee \neg q ) $$


# Lecture 4 - Notes  

### May 12, 2015  

## Section 1.2 Continued

### Using Laws of Logic to prove logical equivalence


#### Example

Show $ p \leftrightarrow q \iff (p \wedge q) \vee (\neg p \wedge \neg q) $.

##### Solution

Proof:

We know,

$$ p \leftrightarrow q \iff (p \to q) \vee (q \to p) $$

and,

$$ p \leftrightarrow q \iff (\neg p \vee q) \wedge (\neg q \vee p) $$

Using distribution twice,

$$ p \leftrightarrow q \iff [(\neg p \vee q) \wedge \neg q] \vee [(\neg p \vee q) \wedge p] $$

$$ p \leftrightarrow q \iff [(\neg p \wedge \neg q) \vee (q \wedge \neg q)] \vee [(\neg p \wedge p) \vee (q \wedge p)] $$

and using identities,

$$ p \leftrightarrow q \iff [(\neg p \wedge \neg q) \vee \mathbb{0}] \vee [\mathbb{0} \vee (q \wedge p)] $$

$$ p \leftrightarrow q \iff (\neg p \wedge \neg q) \vee (q \wedge p)$$

By commution,

$$ p \leftrightarrow q \iff (p \wedge q) \vee (\neg p \wedge \neg q) $$

#### Example

Show $ \neg q \vee ( p \to q ) $ is a tautology.

##### Solution

Proof:

We know, 

$$ p \to q \iff \neg p \vee q $$

substituting,

$$ \neg q \vee ( \neg p \vee q ) $$

By commution,

$$ (\neg q \vee \neg p) \wedge ( \neg q \vee q ) $$

then using identities,

$$ (\neg q \vee \neg p) \wedge \mathbb{1} $$

and dominance,

$$ \mathbb{1} $$

__This is wrong :(__

## Section 1.3 - Logical Arguments

_definition_: an __argument__ is a type of implication, were we have many premises and one conclusion

$$ (p_1 \wedge p_2 \wedge p_3 \wedge ... \wedge p_n) \to q $$







# Lecture 6 - Notes  

### May 15, 2015  

## Section 0.2 - Proofs in Math

To prove results, beyond those in formal logic, we use _word proofs_.

### Direct Proof

To show $ p \to q $, assume $p$ is true, then use known results (e.g. facts, logical equivalents) to show that $q$ is also true.

#### Facts

##### Even Integers

If $n$ is an even integer, then,

$$ n = 2k $$

where $k$ is some integer.

##### Odd Integers

If $n$ is an odd integer, then,

$$ n = 2k +1 $$

where $k$ is some integer.

#### Example

If some integer $n$ is even, then $n^2$ is also even.

##### Solution


_Proof_: Supposed $n$ is even, then,

$$ n = 2k $$

For some $k \in \mathbb{Z}$.

So,

$$ n^2 = (2k)^2 = 2(2k^2) $$

and $2k^2$ is an integer.

$$ \therefore n^2 = 2k^2 \text{ is even.} $$

### Proof by Contrapositive

Assume that $\neg q$ is true, then use known result to prove that $\neg p$ is true.

> __Recall__  
> The contrapositive of $p \to q$ is $\neg q \to \neg p$.

#### Example

$\forall n \in \mathbb{Z}$ if $n^2$ is even, then $n$ is even.

##### Solution

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

### Proof by Contradiction

To show $p \to q$ assume that $p$ and $\neg q$ are true. Then, using known results, arrive at some contradiction.

> Show it's impossible for $\neg q$ to be true, and therefore for $q$ is true.

#### Fact

If $x$ is a rational number ($x \in \mathbb{Q}$) then,

$$
    x = \frac{a}{b}
$$

where $a,b \in \mathbb{Z}$.

#### Example

Prove that $\sqrt{2}$ is irrational.

##### Soluiton

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
# Lecture 7 - Notes  

### May 19, 2015  

# Chapter 2 - Sets and Relations

## Section 2.1 - Sets

_definition_: A __set__ is a collection of objects. The objects are called __elements__ or __members__.

* If $x$ is and element of set $S$ then we write $x \in S$.

### Explicit Listing Notation

Listing all the elements in a set.

#### Examples

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

### Implicit Listing Notation

List enough elements to make the pattern obvious.

#### Examples

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

### Set Builder Notation

Describe the elements by providing some characteristic of them.

#### Example

Suppose we want the prime numbers,

$$
    \{ x : x \text{ is prime} \}
$$

Translates to "All values of $x$ such that $x$ is prime".

#### Examples

$$
    \{ n \in \mathbb{Z} : n < 20, n \text{ is even}, n > 0 \} = \{ 2,4,6, ... , 18 \}
$$
$$
    \mathbb{Q} = \{ \frac{a}{b} : a,b \in \mathbb{Z}, b \neq 0 \}
$$
$$
    \mathbb{C} = \{ a + bi : a, b \in \mathbb{R} \}
$$ 

### Set Properties

_definition_: Sets $A$ and $B$ are equal ($A = B$) if they have the same elements. That is,

$$
    x \in A \iff x \in B
$$

##### Note:

* Sets are unordered,

$$
    \{ 1,2,3 \} = \{ 3,1,2 \}
$$

* Unless specified repeated elements are ignored,

$$
    \{ 1,2,2,3,3,3 \} = \{ 1,2,3 \}
$$

### Empty Set

_definition_: The __empty set__ is the set with no elements written, $\emptyset$ or $\{\}$.

#### Example

The years that Vancouver has won the Stanley Cup $= \emptyset$.

#### Example

$$
    \{ \frac{a}{b} \in \mathbb{Q} : \frac{a}{b} = \sqrt{2} \} = \emptyset
$$

#### Example

Does $\emptyset = \{ \emptyset \}$?

##### Solution

No. The second set has one element, the first set has no elements.

#### Example

How many elements does,

$$
    \{ \emptyset, \{ \emptyset, \{ \{ \emptyset \} \} \}, \{ \emptyset \} \}
$$

have?

##### Solution

Three,

* $\emptyset$
* $\{ \emptyset, \{ \{ \emptyset \} \} \}$
* $\{ \emptyset \}$

### Subsets

_definition_: Let $A$ and $B$ be sets. $A$ is a __subset__ of $B$ ($A \subseteq B$) if every element in $A$ is also in $B$ (but not necessarily the reverse). That is $x \in A \Rightarrow x \in B$.

*  If $A$ is not a subset of $B$ we write $A \not\subseteq B$
# Lecture 8 - Notes  

### May 20, 2015  

## Section 2.1 Continued

#### Example

Let $A = \{ 1 ,2 , \emptyset \}$ and $B = \{ 1,3,A \}$. Which of the following are true?

1. $\emptyset \in A$
2. $\{ 1 \} \in A$
3. $2 \in B$
4. $A \in B$
5. $\{A\} \in B$
6. $A \subseteq B$

##### Solution

Only 1 and 4 are true. 2, 3, 5 and 6 are false.

### Proper Subsets

_definition_: $A$ is a __proper subset__ of $B$ if $A \subseteq B$ and $A \neq B$. It is written $A \subset B$.

### Properties of Sets

* Any set $S$ has $S \subseteq S$.
* Any set $S$ has $\emptyset \subseteq S$.
* An $n$ element set has $2^n$ subsets.

#### Example

How many subsets does $\{ a,b \}$ have?

##### Solution

Four,

* $\{ a \}$
* $\{ b \}$
* $\{ a, b \}$
* $\emptyset$

### The Transitive Property of Subsets

If $A$, $B$ and $C$ are sets such that,

$$
    A \subseteq B \text{ and } B \subseteq C
$$

then,

$$
    A \subseteq C
$$

#### Proof

(RTP: Must show every element  in $A$ is also in $C$)

Suppose that $A \subseteq B$ and $B \subseteq C$. Let $x \in A$. So then since $A \subseteq B$, $x \in B$. And so, since $B \subseteq C$, $x \in C$.

$$
    \therefore A \subseteq C
$$

#### Proposition

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

### Power Sets

_defnition_: The __power set__ of a set $A$ (denoted $\mathcal{P}(A)$) is the set whose elements are the subsets of $A$.

#### Example

Let $A = \{ a, b, \}$. What is the power set of $A$?

Subsets of $A$ are:

* $\{ a \}$
* $\{ b \}$
* $\{ a, b \}$
* $\emptyset$

##### Solution

$$
    \mathcal{P}(A) = \{\{ a \}, \{ b \}, \{ a, b \}, \emptyset \}
$$

### Properties of Power Sets

Let $\mathcal{P}(A)$ be a power set of $A$.

* Every element of $\mathcal{P}(A)$ is a set.
* If $A$ has $n$ elements, $\mathcal{P}(A)$ has $2^n$ elements.
* $\emptyset \in \mathcal{P}(A)$
* $A \in \mathcal{P}(A)$
* $X \in \mathcal{P}(A) \iff X \subseteq A$

#### Proposition

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

## Section 2.2 - Set Operations

### Union

_definition_: Let $A$ and $B$ be sets. The __union__ of $A$ and $B$ (denoted $A \cup B$) is the set,

$$
    A \cup B = \{ x : x \in A \vee x \in B \}
$$

### Intersection

_defninition_: The __intersection__ of $A$ and $B$ (denoted $A \cap B$) is the set,

$$
    A \cap B = \{ x : x \in A \wedge x \in B \}
$$

#### Example

Let $W = \{ a,b,c,d,e \}$ and $V = \{ a,b,c,x,y,z \}$.

##### Solution

$$
    W \cup V = \{ a,b,c,d,e,x,y,z \}
$$
$$
    W \cap V = \{ a,b,c \}
$$
# Lecture 9 - Notes  

### May 22, 2015  

## Section 2.2 - Continued

#### Example

* $A = \{ a, b, c \}$
* $B = \{x,y,z\}$
* $C = \{a,b,x,z\}$
* $\mathcal{U} = \{ a,b,x,y,z \}$

##### Solution


### Set Difference

$$
    A \setminus B
$$

![](http://upload.wikimedia.org/wikipedia/commons/8/83/Set_difference.svg)

### Symmetric Difference

$$
    A \oplus B = B \oplus A
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/4/46/Venn0110.svg/1280px-Venn0110.svg.png)

### Universe

All the objects that can occur in the set.

$$
\mathcal U
$$

### Compliment

$$
    A^C = \mathcal U \setminus A
$$

![](http://upload.wikimedia.org/wikipedia/commons/thumb/e/eb/Venn1010.svg/1280px-Venn1010.svg.png)


#### Theorem

For sets $A$ and $B$,

$$
    (A \cup B)^C = A^C \cap B^C
$$

##### Proof

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

### Cartesian Product

_definition_: The __cartesian product__ of $A$ and $B$ is,

$$
    A \times B = \{ (a,b): a \in A, b \in B \}
$$

#### Note:

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

#### Fact

For any set $A$,

$$
    A \times \emptyset = \emptyset
$$

#### Proposition

$$
    A \times (A \cup C) \subseteq (A \times B) \cup (A \times C)
$$

##### Proof

Let $(x,y) \in A \times (B \cup C)$, then $x \in a$ and $y \in B \cup C$.

###### Case 1:

If $y \in B$, then,

$$
    (x,y) \in A \times B
$$

###### Case 2:

If $y \in C$, then,

$$
    (x,y) \in A \times C
$$

In either case $(x,y) \in (A \times B) \cup (A \times C)

$$
    \therefore A \times (A \cup C) \subseteq (A \times B) \cup (A \times C)
$$


# Lecture 10 - Notes  

### May 26, 2015  

## Section 2.2 Continued

#### Example

$$
    A = \{ 1,2 \}
$$

$$
    \mathcal P (A) = \{ \{ 1 \}, \{ 2 \}, \{ 1,2 \}, \emptyset \}
$$

##### Solution

$$
    A \not\subseteq \mathcal P (A)
$$

$$
    A \in \mathcal P (A)
$$

### Venn Diagrams

Can help us see that,

$$
    A^C \cap B = (A \cup B ) \setminus A
$$

but it doesn't prove it.

#### Example

Show by counter example that,

$$
    A \setminus (B \setminus C) \neq (A \setminus B) \setminus C
$$

![](http://www.math.csusb.edu/notes/sets/setsex5/venn3p.gif)

##### Solution

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

## Section 2.3 - Binary Relations


_definition_: A __binary relation__  from a set $A$ to a set $B$ is a subset,

$$
    \mathcal R \subseteq A \times B.
$$

#### Note:

Binary refers to a relationship between 2 sets, and we will only consider binary relationships in this course.

#### Example

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

### Notation

When an ordered pair $(a,b)$ is in a relationship $\mathcal R$ we say "$a$ is related to $b$" and write $(a,b) \in \mathcal R$ or, using Infix notation,


$$
    a \mathcal R b
$$

$$
   3 \not\mathcal R z
$$

### Types of Relations

For a relation $\mathcal R_1$ on a $A \times A, \mathcal R$ is,

#### Reflexive

If $(x,x) \in \mathcal R$ for all $x \in A$.

#### Symmetric

If $(y,x) \in \mathcal R$ whenever $(x,y) \in \mathcal R$.
# Lecture 11 - Notes  

### May 27, 2015  

## Section 2.3 Continued

### Relations

A set that defines a relationship between two or more sets.

### Antisymmetry

If $(x,y) \in \mathcal R$ and $(y,x) \in \mathcal R$ then $x = y$.

This is not the same as not symmetric (Antisymmetric $\not\Leftrightarrow$ not Symmetric ).

### Transitivity

If $(x,y) \in \mathcal R$ and $(y,z) \in \mathcal R$ then $(x,z) \in \mathcal R$.

__Note__: It is possible for $x = z$.

## Section 2.4 Equivalence Relations


_definition_: A relation $\mathcal R$ on a set $A$ is an __equivalence relationship__ if it is,

1. Reflexive
2. Symmetric
3. Transitive

#### Example

Consider $\mathcal R$ on $\mathbb Z \times \mathbb Z$, defined by,

$$
    a \mathcal R b \iff a-b \text{ is a multiple of 3}.
$$

##### Solution

###### Reflexivity

Let $a \in \mathbb Z$, then,

$$
    a - a = 0 = 0 \cdot 3
$$

Therefore $(a,a) \in \mathcal R$.

###### Symmetry

Let $(a,b) \in \mathcal R$, so,

$$
    a - b = 3k
$$

for some $k \in \mathbb Z$.

$$
    b - a = -3k = 3 \cdot (-k)
$$

Since $-k \in \mathbb Z$, $b - a$ is a multiple of $3$ and therefore $(b,a) \in \mathcal R$.

###### Transitivity

Let $(a,b) \in \mathcal R$ and $(b,c) \in \mathcal R$, so,

$$
    a - b = 3k
$$

and

$$
    b -c = 3m
$$

for $k, m \in \mathbb Z$. Adding the equations,

$$
\begin{aligned}
    a - b + b - c &= 3k + 3m \newline
    a - c &= 3 \cdot (k + m)
\end{aligned}
$$

Therefore since $(k + m) \in \mathbb Z$, $a - c$ is a multiple of $3$ and therefore $(a,c) \in \mathcal R$.
# Lecture 12 - Notes  

### May 29, 2015  

## Section 2.4 Continued

If $\mathcal R$ is an equivalence relation,

$$
    \mathcal R \subseteq A \times B
$$

can $A \neq B$?

No, $\mathcal R \subseteq A \times A$.

### Equivalence Class

_definition_: For an equivalence relation $\sim$ on a set $A$, the __equivalence class__ of $a \in A$, is the set of all elements equivalent to $a$.

$$
    \frac{[a]}{a} = \{ x \in A: a \sim x \}
$$

The set of equivalence classes is called the __Quotient set of $A$ mod $\sim$__, denoted $A \setminus \sim$.

### Partition

_definition_: A __partition__ of set $A$ is a collection of subsets $A_1, A_3, A_3,...,A_n$ such that,

* Each is non empty ($A_i \neq \varnothing$)
* They are pairwise disjoint ($A_i \cap A_j = \varnothing$)
* They union to $A$ ($\cup_{i=0}^{n} ~A_i = A$)

#### Fact

If $\sim$ is equivalent to $A$, then,

1. The set of all its equivalence classes forms a partition of $A$
2. If $x,y \in A$ then either $[x] = [y]$ or $[x] \cap [y] = \varnothing$

#### Example

Let $\mathcal R \subseteq \mathbb Z \times \mathbb Z$, such that $(x,y) \in \mathcal R$. if and only if $a - b$ is a multiple of $3$.

##### Solution

1) What elements are equivalent to $0$?

$$
    a \mathcal R 0 \iff a - 0 = 3k
$$

For $k \in \mathbb Z$. So $3 \mathcal R 0, 6 \mathcal R 0, ...$

$$
    [0] = \{ ..., -9, -6, -3, 0, 3, 6, 9,...  \}
$$

Next lets consider $[3]$,

$$
    [3] = [0] = [9] = [-9] = ...
$$

2) What elements are equivalent to $1$?

$$
\begin{aligned}
    a \mathcal R 1 &\iff a - 1 = 3k, k \in \mathbb Z \newline
    &\iff a = 3k + 1
\end{aligned}
$$

So,

$$
\begin{aligned}
    [1] &= \{ ..., -5, -2, 1, 4, 7, ... \} \newline
    &= [4] = [-5] = ...
\end{aligned}
$$

3) What elements are equivalent to 2?

$$
\begin{aligned}
    a \mathcal R 2 &\iff a - 2 = 3k, k \in \mathbb Z \newline
    &\iff a = 3k + 2
\end{aligned}
$$

$$
\begin{aligned}
    \left[ 2 \right] &= \{ ..., -7 ,-4 ,-1 ,2, 5, 8, 11, ... \} \newline
    &= [-1] = [5] = ...
\end{aligned}
$$

So our equivalence classes are,

$$
\begin{aligned}
    \left[ 0 \right] &= \{ ..., -9, -6, -3, 0, 3, 6, 9,...  \} \newline
    [1] &= \{ ..., -5, -2, 1, 4, 7, ... \} \newline
    [2] &= \{ ..., -7 ,-4 ,-1 ,2, 5, 8, 11, ... \} \newline
\end{aligned}
$$

And the partition is,

$$
    \{ [0], [1], [2] \}
$$

To confirm this we must check that,

$$
    \mathbb Z = [0] \cup [1] \cup [2]
$$

#### Example

Let $A = \{ a,b,c,d,e,f \}$ and $\mathcal R = \{ (a,a), (b,b), ..., (f,e) \}$

We can represent this in a matrix (which is good because I didn't write the whole thing),

| $a$ | $b$ | $c$ | $d$ | $e$ | $f$ | $g$ |
|-----|-----|-----|-----|-----|-----|-----|
| $a$ | $x$ | $~$ | $~$ | $~$ | $~$ | $~$ |
| $b$ | $~$ | $x$ | $~$ | $~$ | $~$ | $~$ |
| $c$ | $~$ | $~$ | $x$ | $~$ | $~$ | $~$ |
| $d$ | $~$ | $~$ | $~$ | $x$ | $x$ | $x$ |
| $e$ | $~$ | $~$ | $~$ | $x$ | $x$ | $x$ |
| $f$ | $~$ | $~$ | $~$ | $x$ | $x$ | $x$ |

From this we can tell that $\mathcal R$ is,

1. Reflective (the diagonal is filled)
2. Symmetric (across the diagonal line)
3. Equivalence Classed (Each 'square' of $x$'s is an equivalence class.
# Lecture 13 - Notes  

### June 2, 2015  

#### Example

Let $D = \{ \text{All binary strings of length } 5 \}$ and $\mathcal T$ be the relation on $ D \times D$ defined by $x \mathcal T y $ the first $3$ digits of $x$ match $y$.

##### Solution

$$
\begin{aligned}
    \left[00000\right] &= \{ 00000, 00001, 00010, 00011 \} \newline
                       &= [00001] \newline
    \left[00100\right] &= \{ 00100, 00101, 00110, 00111 \} \newline
    \left[11100\right] &= \{ 11100, 11101, 11110, 11111 \} \newline
\end{aligned}
$$

# Chapter 3: Functions

## Section 3.1: Basic Terminology

_definition_: A __function__ from a set $A$ to $B$ is a binary relation where every element in $A$ corresponds to exactly one element in $B$. We write,

$$
    f: A \to B
$$

"$f$ is a function from $A$ to $B$".

We typically define functions using equations (e.g. $f(x) = x^2$) but they can also be lists.

#### Example

$$
\begin{aligned}
    A &= \{ 1,2,3,4 \} \newline
    B &= \{ w,x,y,z \} \newline
\end{aligned}
$$

##### Sub-example

$$
\begin{aligned}
    f &= \{ (1,x), (2,y), (3,w), (4,y) \}
\end{aligned}
$$

This is a function since everything in $A$ corresponds to one thing in $B$. It's okay for multiple things in $A$ to go to one thing in $B$.

##### Sub-example

$$
\begin{aligned}
    g = \{ (1,x), (2,y), (3,z) \}
\end{aligned}
$$

This is __not__ a function since $4$ is not mapped to anything.

##### Sub-example

$$
\begin{aligned}
    h = \{ (1,x),(2,x),(3,x),(4,x) \}
\end{aligned}
$$

This is a function.

##### Sub-example

$$
\begin{aligned}
    i = \{ (1,y),(2,z),(2,x),(3,w),(4,x) \}
\end{aligned}
$$

This is __not__ a function since $2$ corresponds to two values.

#### Recall

The vertical line test.

This is a function since every point in $x$ maps to one point in $y$.

![](http://www.algebra-class.com/image-files/vertical-line-answer-2.gif)

This is not a function since some points in $x$ correspond to two values of $y$.

![](http://www.algebra-class.com/image-files/vertical-line-3.gif)

#### Notation

if $(a,b) \in f$ then we write,

$$
\begin{aligned}
    &f(a) = b \newline
    &f : a \mapsto b \newline
\end{aligned}
$$

where $b$ is the __image__ of $a$.

### Onto and One-to-One

__definitions__: For a function $f: A \mapsto B$,

* $f$ is __onto__ (or __subjective__) if $\forall b \in B, \exists a \in A$ such that $f(a) = b$.
* $f$ is __one-to-one__ (or __injective__) if all elements of $A$ map to different elements of $B$.
    * _intuitive definition_: if $x_1 \neq n_2 \Rightarrow f(x_1) \neq f(x_2)$
    * _proof definition_: if $f(x_1) = f(x_2) \Rightarrow x_1 = x_2$

#### Example

$$
\begin{aligned}
    F &: A \mapsto B\newline
    A &= \{ 1,2,3,4 \} \newline
    B &= \{ w,x,y,z \} \newline
\end{aligned}
$$

$$
\begin{aligned}
    f &= \{ (1,y), (2,w), (3,x), (4,z) \}
\end{aligned}
$$

##### Solution

This is onto since every element in $B$ is mapped to. It is also one-to-one since every element in $A$ points to something different.

### Domain

For a function $f: A \mapsto B$, 

* the __domain__ of $f$ is $A$
* the __target__ of $f$ is $B$
* the __range__ of $f$ the set $\{ b \in B, \exists a \in A, f(a) = b \}$
# Lecture 14 - Notes  

### June 3, 2015  

## Section 3.1 Continued

### Functions with Formulas

#### Example

$$
    f(x) = \frac{3x + 4}{5}
$$

where $f: \mathbb Z \mapsto \mathbb R$.

Is $f$ one-to-one or onto?

##### Solution

###### Required to Prove One-to-One

Suppose $f(x_1) = f(x_2)$ then $x_1 = x_2$.

###### So

Suppose $f(x_1) = f(x_2)$,

$$
\begin{aligned}
     \frac{3x_1 + 4}{5} &=  \frac{3x_2 + 4}{5} \newline
     3x_1 + 4 &=  3x_2 + 4 \newline
     3x_1 &=  3x_2 \newline
     x_1 &=  x_2 \newline
\end{aligned}
$$

$$
    \therefore \text{One-to-one}
$$

###### Required to Prove Onto
We need $b \in \mathbb R$ such that $a \in \mathbb Z$ where $f(a) = b$.

###### So

Suppose $b \in \mathbb R$ such that $a \in \mathbb Z$ where $f(a) = b$.

$$
\begin{aligned}
    b &=  \frac{3a + 4}{5} \newline
    5b &= 3a + 4 \newline
    5b - 4 &= 3a \newline
    \frac{5b - 4}{3} &= a \in \mathbb Z \newline
\end{aligned}
$$

Consider $b = 1$,

$$
\begin{aligned}
    \frac{5\cdot1 - 4}{3} &= \frac{1}{3} \notin \mathbb Z \newline
\end{aligned}
$$

$$
    \therefore \text{Not onto}
$$

##### Solution

If $f: \mathbb R \mapsto \mathbb R$ instead.

Supposed $b \in \mathbb R$ and suppose $\exists a in \mathbb R$ such that $f(a) = b$.

Then,

$$
\begin{aligned}
    a &= \frac{5b - 4}{3} \newline
    &\in \mathbb R \newline
\end{aligned}
$$

$$
    \therefore \text{Onto}
$$

#### Example

Let $f: \mathbb R \mapsto \mathbb R$ where,

$$
\begin{aligned}
    f(x) = x^2 + 1 \newline
\end{aligned}
$$ 

##### Solution

Not one-to-one since,

$$
\begin{aligned}
    (-1)^2 + 1 &= (1)^2 + 1 \newline
    \text{but } -1 &\neq 1 \newline
\end{aligned}
$$

Not onto since,

$$
\begin{aligned}
    x^2 + 1 &\ge 1 \newline
    \text{and } 0 &\in \mathbb R \newline
    \therefore \not\exists a \in \mathbb R, f(a) &= 0
\end{aligned}
$$

### Bijection

_definition_: If a function $f$ is both one-to-one and onto it is a __bijection__.

### Functional Equality

_definition_: Two functions, $f$ and $g$ are equal if,

1. They have the same target
2. They have the same domain
3. $f(x) = g(x)$, $\forall x \in$ domain

### Floor and Ceiling

_definition_: The floor of $x$ is the function,

$$
\begin{aligned}
    f(x) = \lfloor x \rfloor, f: \mathbb R \mapsto \mathbb Z
\end{aligned}
$$

#### Example



_definition_: The ceiling of $x$ is the function,

$$
\begin{aligned}
    f(x) = \lceil x \rceil, f: \mathbb R \mapsto \mathbb Z
\end{aligned}
$$
# Lecture 15 - Notes  

### June 9, 2015  

## Section 3.1 Continued

### Function Equality

_definition_: Two functions $f$ and $g$ are equal if:

* They have the same target
* They have the same domain
* $f(x) = g(x)$ for all $x$ in the domain of $f$

#### Example

Let $f: \mathbb R \mapsto \mathbb Z$ defined by,

$$
    f(x) = \lfloor x \rfloor
$$

and let $g: \mathbb Z \mapsto \mathbb Z$ defined by,

$$
    g(x) = \lfloor x \rfloor
$$

and let $h: \mathbb Z \mapsto \mathbb R$ defined by,

$$
    h(x) = \lfloor x \rfloor
$$

##### Solution

$f \neq g$ since they have different domains but the range of $h$ is equal to the range of $g$. However since they have different targets $h \neq g$.

### Special Functions

_definition_: For any set $A$ the __identity function__, $i_A: A \mapsto A$, where,

$$
    i_A (x) = x, \forall x \in A
$$

we can also say this is the set of ordered pairs, $i_A = \{ (a,a):  a \in A \}

_definition_: The __absolute value__ of $x$, $|x|$ is defined as,

$$
   \left|x\right| = \left\{
     \begin{array}{lr}
       x & \text{ if } x \ge 0 \newline
       -x & \text{ if } x \lt 0 \newline
     \end{array}
   \right.
$$

## Section 3.2 - Inverses and Compositions

#### Example

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

#### Solution

$f$ is one-to-one and onto since every element in $B$ is related to exactly one element in $A$, it is therefore a bijection. $g$ is not one-to-one since both $3$ and $4$ map to $c$ but it is onto since every element in $C$ is mapped to.

Reversing the order of each pair in $f$ gives its inverse $f^{-1}: B \mapsto A$, where,

$$
\begin{aligned}
    f^{-1} = \{ (x,1),(y,2),(z,3),(w,4) \}
\end{aligned}
$$

$g$ does not have an inverse since it wouldn't be a function.

### Inverses

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

#### Example

Find $f^{-1}: \mathbb R \setminus \{ 1\} \mapsto \mathbb R \setminus \{2\}$ where,

$$
    f(x) = y =\frac{2x}{x-1}
$$

##### Solution


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

#### Proposition

A function $f$ has an inverse if and only if $f$ is a bijection (it's one-to-one and onto).

##### Fact

$$
    (f^{-1})^{-1} = f
$$

So every inverse is a bijection as well.

### Compositions

_definition_: The __composition__ of $g: B \mapsto C$ with $f: A \mapsto B$ is,

$$
    g \circ f = g(f(x)), \forall x \in A
$$
# Lecture 16 - Notes  

### June 10, 2015  

## Section 3.2 Continued

#### Example

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

##### Solution

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

#### Notation

* $f^2 = f \circ f$
* $f^n = f \circ f \circ ... \circ f$

#### Proposition

if $f: A \mapsto B$ and $g: B \mapsto C$ are bijections, then $g \circ f$ is also a bijection.

##### Proof

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

### Inverses and Identities

#### Proposition

Given two functions $f: A \mapsto B$ and $g: B \mapsto A$ are inverses if and only is their compositions are identities.

$$ %Aligned
\begin{aligned}
    g \circ f &= i_A \newline
    f \circ g &= i_B \newline
\end{aligned}
$$

#### Example

$$ %Aligned
\begin{aligned}
    f(x) &= \frac{2x}{x-1} \newline
    g(x) &= \frac{x}{x-2} \newline
\end{aligned}
$$

##### Solution

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

## Section 3.3 - One-to-one correspondences and the Cardinality of a Set

### Cardinality

_definition_: The __cardinality__ of set $A$, denoted $|A|$, is the number of elements in set $A$.

#### Example

$$ %Aligned
\begin{aligned}
    A &= \{ a,b,c \} \newline
    |A| &= 3 \newline
\end{aligned}
$$

### One-to-one Correspondences

_definition_: A function $f: A \mapsto B$ that is a bijection is also a __one-to-one correspondence__. We say $\exists$ a one-to-one correspondence between $A$ and $B$.

#### Fact

$$ %Aligned
\begin{aligned}
    |A| = |B| \iff \exists ~f:A \mapsto B \text{ that is a bijection.}
\end{aligned}
$$

#### Claim

$$ %Aligned
\begin{aligned}
    |(0,1)| = |(2,5)|
\end{aligned}
$$

##### Proof

Consider $f: (0,1) \mapsto (2,5)$, where,

$$ %Aligned
\begin{aligned}
    f = 2x + 3 \newline
\end{aligned}
$$

_(one-to-one)_ Supposed $f(x_1) = f(x_2)$,

$$ %Aligned
\begin{aligned}
    3x_1 + 2 &= 3x_2 + 2 \newline
    3x_1 &= 3x_2 \newline
    x_1 &= x_2 \newline
\end{aligned}
$$

_(onto)_ Let $y \in (2,5)$, if $f(x) = y$,

$$ %Aligned
\begin{aligned}
    3x + 2 &= y \newline
    3x &= y - 2 \newline
    x &= \frac{y-2}{3} \newline
\end{aligned}
$$

$$ %Aligned
\begin{aligned}
    \therefore f \text{ is a bijection.}
\end{aligned}
$$
# Lecture 17 - Notes  

### June 12, 2015  

## Section 3.3 Continued

#### Example

Let $2 \mathbb Z = \{ ...,-4,-2,0,2,4,... \}$, show $|\mathbb Z| = |2 \mathbb Z|$.

##### Solution

Define $f: \mathbb Z \mapsto \mathbb 2Z$, where,

$$
    f(x) = 2x
$$

which is a bijection (easy to prove).

### Countability

_definition_: A set $A$ is __countably infinite__ if,

$$ %Aligned
\begin{aligned}
    |A| = |\mathbb N|
\end{aligned}
$$

So if I can line up a value in a with a value in the countable numbers (natural numbers) it's countably infinite.

* $A$ is __countable__ if it is countably infinite or finite.
* If $A$ is not countable it is __uncountable__.

##### Note

Sometimes $|\mathbb N$ is denoted $\aleph_0$ ("Aleph naught").

#### Proposition

A set $A$ is countable if and only if $\exists$ a bijection $f: A \mapsto \mathbb N$ (i.e. you can list the elements of $A$).

#### Proposition

$\mathbb Z$ is countable. We can show a correspondence,

$$ %Aligned
\begin{aligned}
    \mathbb Z&: 0,-1,1,-2,2,-3,3,-4,4,... \newline
    \mathbb N&: 0,1,2,3,4,5,6,7,8,9,... \newline
\end{aligned}
$$

This is a sufficient correspondence. However we can show a more mathy correspondence,

$$ %Aligned
\begin{aligned}
    f(x) = (-1)^n \lceil \frac{n}{2} \rceil
\end{aligned}
$$

#### Fact

A subset of a countable set is also countable.

#### Proposition

A set $A$ is countable if there exists a bijection $f: A \mapsto B$ where $B$ is any countable set.

#### Fact

$\mathbb N \times \mathbb N$ is countable! Lets make a table!

| $~$  | $0$ | $1$ | $2$ | $...$ |
|:-:|:-:|:-:|:-:|:-:|
| $0$ | $(0,0)$ | $(0,1)$ | $(0,2)$ | $...$ |
| $1$ | $(1,0)$ | $(1,1)$ | $(1,2)$ | $...$ |
| $2$ | $(2,0)$ | $(2,1)$ | $(2,2)$ | $...$ |
| $...$ | $...$ | $...$ | $...$ | $...$ |

Using _diagonal sweeping_ we get,

$$
    (0,0),(0,1),(1,0),(2,0),(1,1),(0,2),...
$$

#### Fact

$\mathbb Q$ is countable. 

| $~$  | $0$ | $1$ | $-1$ | $2$ | $-2$ | $...$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $1$ | $\frac{0}{1}$ | $\frac{1}{1}$ | $\frac{-1}{1}$ | $\frac{2}{1}$ | $\frac{-2}{1}$ | $...$ |
| $2$ | $\frac{0}{2}$ | $\frac{1}{2}$ | $\frac{-1}{2}$ | $\frac{2}{2}$ | $\frac{-2}{2}$ | $...$ |
| $...$ | $...$ | $...$ | $...$ | $...$ |

Using _diagonal sweeping_ we get,

$$
     \frac{0}{1}, \frac{1}{1}, \frac{0}{2}, ... 
$$

#### Fact

The union of countably infinite sets is countable, e.g.,

$$
    \mathbb Z \cup \mathbb Q, \mathbb Z \cup \mathbb N \cup \{a,b,c \}
$$

### Countability Summary

A set $A$ is countable if,

* It's finite,
* It's the union of countable sets,
* It's a subset of a countable set,
* There exists bijection $f: A \mapsto \mathbb N$,
* We can list the elements of $A$.
# Lecture 18 - Notes  

### June 16, 2015  

## Section 3.3 Continued

#### Recall

A set is __countable__ if it is not countable.

#### Fact

The open interval $(0,1)$ is uncountable.

##### Proof

> _Proof Idea_: Let's use a proof by contradiction by trying to list the elements between zero and one. Then we'll show that no matter how we list the elements we always miss something.

Suppose to the contrary $(0,1)$ is countable, and we can list its elements,

$$
    [0.d_{10}d_{11}d_{12}d_{13}...],[0.d_{20}d_{21}d_{22}d_{23}...],[0.d_{30}d_{31}d_{12}d_{33}...],...
$$

where any $d_{ij} \in \{0,1,2,...,8,9 \}$ and $d_{ij}$ is the $j$^th digit of the $i$^th number.

Lets construct a new element $x$ on the interval $(0,1)$ and show that $x$ is not in the list. Since $x \in (0,1)$,

$$
    x = 0.x_{1}x_{2}x_{3}x_{4}x_{5}...
$$

where $x_i = \{ 0,1,2,...,9 \}$. Now let,

$$
    x_i = \left\{
      \begin{array}{lr}
        5 &\text{ if } d_{ii} \neq 5 \newline
        6 &\text{ if } d_{ii} = 5 \newline
      \end{array}
    \right.
$$

New we'll compare $x$ to our list,

$$
\begin{aligned}
    x = 0.x_{1}x_{2}x_{3}x_{4}... &\neq 0.d_{10}d_{11}d_{12}d_{13}... \newline
    &\neq 0.d_{20}d_{21}d_{22}d_{23}... \newline
    &\neq 0.d_{30}d_{11}d_{32}d_{33}... \newline
    &~~\vdots\newline
\end{aligned}
$$

Since $x$ is not in our list, the list does not count all elements and is therefore not countable.

###### Note

This technique is called __Cantor Diagonalization__.

#### Fact

A set $A$ is uncountable if it has an uncountable subset. So the real numbers $\mathbb R$ are uncountable since $(0,1) \subset \mathbb R$.

#### Example

Is $[0,1]$ countable?

##### Solution

$$
\begin{aligned}
    \left[0,1\right] &= (0,1) \cup \{ 0\} \cup \{1\} \newline
    (0,1) &\subseteq [0,1] \newline
\end{aligned}
$$

So $[0,1]$ is uncountable.

#### Fact

The irrational numbers $\mathbb I$ are uncountable.

##### Proof

Consider

$$ %Aligned
\begin{aligned}
    \mathbb R = \mathbb Q \cup mathbb I.
\end{aligned}
$$

Suppose to the contrary that $\mathbb I$ is countable. Since $\mathbb Q$ is countable this would make $\mathbb R$ countable. $\mathbb R$ is not countable therefore $\mathbb I$ must be uncountable.  

### Cantor's Continuum Hypothesis

There is no set $A$ such that,

$$ %Aligned
\begin{aligned}
    \aleph_0 \lt |A| \lt |\mathbb R|
\end{aligned}
$$

where $\aleph_0 = |\mathbb N|$.

* In 1940 Godel showed that we cannot prove the continuum hypothesis to be __false__.
* In 1963 Cohen showed that we cannot prove the continuum hypothesis to be __true__.

# Lecture 19 - Notes  

### June 17, 2015  

# Chapter 4: The Integers

## Section 4.1 - The Division Algorithm

### Properties of $\mathbb Z$ vs $\mathbb R$

Let $a,b \in \mathbb R$.

#### Closure ($\mathbb R$ and $\mathbb Z$)

* $a + b \in \mathbb R$
* $a \cdot b \in \mathbb R$


#### Commutivity ($\mathbb R$ and $\mathbb Z$)

* $a + b = b + a$
* $a \cdot b = b \cdot a$


#### Associativity ($\mathbb R$ and $\mathbb Z$)

* $(a + b) + c = a + (b + c)$
* $(ab)c = a(bc)$ 


#### Identity ($\mathbb R$ and $\mathbb Z$)

* $\exists 0 \in \mathbb R$ such that, $\forall a \in \mathbb R, 0+a = a$
* $\exists 1 \in \mathbb R$ such that, $\forall a \in \mathbb R, 1 \cdot a = a$


#### Distribution ($\mathbb R$ and $\mathbb Z$)

* $a \cdot (b + c) = a \cdot b + a \cdot c$

#### Inverses ($\mathbb R$ and _some_  $\mathbb Z$)

($\mathbb Z$) For any $a \in \mathbb R, \exists -a \in \mathbb R$, such that,

$$
    a + (-a) = 0.
$$

(not $\mathbb Z$) For any $a \in \mathbb R, \exists \frac{1}{a} \in \mathbb R$, such that,

$$
    a \cdot \frac{1}{a} = 1
$$

#### Example

$\mathbb Z ^\text{o} =$ the set of odd integers.

Is $\mathbb Z ^\text{o}$ closed under addition and multiplication?

##### Solution

IT is not closed under addition since $5 + 3 = 8$.

Closed under multiplication. Proof:

Let $a,b \in \mathbb Z ^\text{o}$, so,

$$ %Aligned
\begin{aligned}
    a &= 2m + 1 \newline
    b &= 2n + 1 \newline
\end{aligned}
$$

where $m,n \in \mathbb Z$. So,

$$ %Aligned
\begin{aligned}
    a \cdot b &= (2m+1)(2n+1) \newline
    &= 4mn + 2m + 2n + 1 \newline
    &= 2(2mn + m + n) + 1. \newline
\end{aligned}
$$

Since $2mn + m + n \in \mathbb Z$, $a \cdot b \in \mathbb Z^\text{o}$.

### Subtraction and Division

We define subtraction and division using inverses.

* $a - b = a + (-b)$
* $\frac{a}{b} = a \cdot \frac{1}{b}$

#### Theorem: The Well-Ordering Principal

Any set of natural numbers ($\mathbb N$) has a smallest element*.

*Does note hold for $\mathbb Z$ or $\mathbb R$.

### The Division Algorithm

#### Example

Divide $278$ by $13$

##### Solution

Can't do long division :(.

#### Theorem

For integers $a$ and $b$, both not zero, there exist _unique_ integers $q$ and $r$ such that,

$$
    a = bq + r
$$

where $0 \lt r \lt |b|$. We call,

| Symbol | Name |
|:-:|:--|
|$a$| Dividend |
|$b$| Divisor |
|$q$| Quotient |
|$r$| Remainder |

#### Proposition

Let $a,b \in \mathbb Z$ where $b \neq 0$. If $a = bq + r$, with $0 \lt r \lt |b|$, then,

$$
    q = \left\{
     \begin{array}{lr}
       \left\lfloor \frac{a}{b} \right\rfloor &\text{ if } b \gt 0 \newline
       \left\lceil \frac{a}{b} \right\rceil &\text{ if } b \lt 0 \newline
     \end{array}
   \right.
$$

### Number in Other Bases

#### Example

Consider in base 10,

$$ %Aligned
\begin{aligned}
    7132 &= 7 \cdot 1000 + 1 \cdot 100 + 3 \cdot 10 + 2 \cdot 1 \newline
    &= 7 \cdot 10^3 + 1 \cdot 10^2 + 3 \cdot 10^1 + 2 \cdot 10^0 \newline
\end{aligned}
$$

Now consider in base 8,

$$ %Aligned
\begin{aligned}
    (7132)_8 = 7 \cdot 8^3 + 1 \cdot 8^2 + 3\cdot 8^1 + 2 \cdot 8^0
\end{aligned}
$$
# Lecture 20 - Notes  

### June 19, 2015  

## Section 4.1 Continued

_definition_: The __base $b$ representation of a natural (base 10) number $n$__ is written,

$$
    (d_k d_{k-1} d_{k-2} ... d_1 d_0)_b
$$

where $0 \le d_i \lt b$ and

$$
    n = d_kb^k + d_{k-1}b^{k-1} + d_{k-2}b^{k-2} + ... + d_1b^1 + d_0b^0.
$$

#### Theorem 

If $b \gt 1$, then every integer $n$ has a __unique__ base $b$ representation.

> Proof in G. MacGillivray notes (NT pg. 4)

#### Example

Convert $(613)_{10}$ to binary, octal and hexadecimal.

##### Solution

###### Binary (Method 1)

$$ %Aligned
\begin{aligned}
    (613)_{10} &= 2^9 + 101 \newline
    &= 2^9 + 2^6 + 37 \newline
    &= 2^9 + 2^6 + 2^5 + 5 \newline
    &= 2^9 + 2^6 + 2^5 + 2^2 + 1 \newline
    &= 2^9 + 2^6 + 2^5 + 2^2 + 2^0 \newline
    &= (1001100101)_2 \newline
\end{aligned}
$$

###### Binary (Method 2)

$$ %Aligned
\begin{aligned}
    \frac{613}{2} &= 306 r 1 \newline
    \frac{306}{2} &= 153 r 0 \newline
    \frac{153}{2} &= 76 r 1 \newline
    \frac{76}{2} &= 38 r 0 \newline
    \frac{38}{2} &= 19 r 0 \newline
    \frac{19}{2} &= 9 r 1 \newline
    \frac{9}{2} &= 4 r 1 \newline
    \frac{4}{2} &= 2 r 0 \newline
    \frac{2}{2} &= 1 r 0 \newline
    \frac{1}{2} &= 0 r 1 \newline
\end{aligned}
$$

###### Octal

$$ %Aligned
\begin{aligned}
    613 \div 8 &= 76 ~r~ 5 \newline
    76 \div 8 &= 9 ~r~ 4 \newline
    9 \div 8 &= 1 ~r~ 1 \newline
    1 \div 8 &= 0 ~r~ 1 \newline
\end{aligned}
$$

So,

$$ %Aligned
\begin{aligned}
    (613)_{10} = (1145)_8
\end{aligned}
$$

###### Hexadecimal

$$ %Aligned
\begin{aligned}
    613 \div 16 &= 38 ~r~ 5 \newline
    38 \div 16 &= 2 ~r~ 6 \newline
    2 \div 16 &= 0 ~r~ 2 \newline
\end{aligned}
$$

So,

$$ %Aligned
\begin{aligned}
    (613)_{10} = (613)_10
\end{aligned}
$$

#### Example

Convert $1222$ to hexadecimal.

###### Solution

Use your calculator,

$$ %Aligned
\begin{aligned}
    (1222)_{10} = (4C6)_{16}
\end{aligned}
$$



# Lecture 21 - Notes  

### June 23, 2015  

## Section 4.2 Divisibility & the Euclidean Algorithm

__definition__: For integers $a$ and $b$, we say $a$ divides $b$, if $\exists k in \mathbb Z$ such that,

$$
    b = a \cdot k
$$

this is denoted $a \mid b$. In this case we can say $a$ is a __divisor__ or __factor__ of $b$. We can also say $b$ is __divisible__ by $a$.

If $a$ _is not_ a divisor of $b$, then we write,

$$
    a \nmid b
$$

Alternatively,

$$
    a \mid b \iff \frac{b}{a} \in \mathbb Z
$$

#### Example

$$ %Aligned
\begin{aligned}
    3 &\mid 12 &\text{since } 12 = 3(4) \newline
    7 &\mid 7  &\text{since } 7 = 7(1) \newline
    -5 &\mid 5 &\text{since } -5 = 5(-1) \newline
\end{aligned}
$$

#### Facts

For any integer $n$,

* $n \mid 0 $ since $0 = n(0)$
* $0 \nmid n$ since $\not\exists k$ such that $0 = nk$

#### Proposition

Let $a,b,c \in \mathbb Z$. If $a \mid b$ and $b \mid c$ then $a \mid c$.

##### Proof

Since $a \mid b$, then $\exists k \in \mathbb Z$ such that $b = ak$. Likewise, since $b \mid c$, $\exists m \in \mathbb Z$ such that $c = bm$. So,

$$
    c = bm = (ak)m = a(km)
$$

and $km \in \mathbb Z$ since the integers are closed under multiplication. Therefore, since $c = a(km)$, $a \mid c$.

#### Proposition 1

Let $a,b \in \mathbb Z$. If $a \mid b$ and $a \mid c$ the we can say,

$$
    a \mid (bx + cy)
$$

for _any_ $x,y \in \mathbb Z$.

##### Proof

Since $a \mid b$, $\exists k \in \mathbb Z$ such that $b = ak$ and since $a \mid c$, $\exists m \in \mathbb Z$ such that $c = am$. Let $x,y \in \mathbb Z$,

$$ %Aligned
\begin{aligned}
    bx + cy &= (ak)x + (am)y \newline
    &= a(kx) + a(my) \newline
    &= a(kx + my) \newline
\end{aligned}
$$

since the integers are close under addition and multiplication, $kx + my \in \mathbb Z$. Therefore $a \mid bx + cy$.

### Common Divisors

_definition_: Let $a$ and $b$ be integers, such that they are not both zero. Then $g$ is the __greatest common divisor__ of $a$ and $b$ if,

1. $g \mid a$ and $g \mid b$ ("common divisor")
2. if $c$ is also a common divisor, $g \ge c$ ("greatest")

and we write $g = \gcd(a,b)$

#### Example

Find $\gcd(6,15)$.

##### Solution

List the divisors,

* $6: 1,2,3,6$
* $15: 1,3,5,15$

So $\gcd(6,15) = 3$

#### Facts

For any integer $a$,

* $\gcd(a,0) = |a|$
* $\gcd(a,1) = 1$
* If $a \mid b$, then $\gcd(a,b) = |a|$

#### Proposition 2

If $a,b \in \mathbb Z$, not both zero, and $a = bq + r$ (for some $q,r \in \mathbb Z$) then $\gcd(a,b) = \gcd(b,r)$.

##### Proof

> We'll show that $\gcd(a,b) \le \gcd(b,r)$ and $\gcd(b,r) \le \gcd(b,r)$

We know, $\gcd(a,b) \mid a$ and $\gcd(a,b) | b$ so we can say,

$$
    \gcd(a,b) \mid ax + by
$$

and we'll let $x = 1$ and $y = -q$,

$$ %Aligned
\begin{aligned}
    \gcd(a,b) &\mid a + b(-q) \newline
\end{aligned}
$$

note that $r = a - bq$, so,

$$
    \gcd(a,b) \mid r
$$

> So right now we know $\gcd(a,b) \le \gcd(b,r)$

We also know $\gcd(b,r) \mid b$ and $\gcd(b,r) \mid r$ so,

$$
    \gcd(b,r) \mid qb + 1r
$$

since $qb + r = a$,

$$
    \gcd(b,r) \mid a
$$

$$
    \therefore \gcd(b,r) \le \gcd(b,a)
$$

and $\gcd(a,b) = \gcd(b,r)$.
# Lecture 22 - Notes  

### June 24, 2015  

## Section 4.2 Continued

### The Euclidean Algorithm for find GCD

Let $a,b \in \mathbb N$, with $b < A$. To find the $\gcd(a,b)$, write,

$$ %Aligned
\begin{aligned}
    a &= bq_1 + r_1 \newline
    b &= r_1q_2 + r_2 \newline
    r_1 &= r_2q_3 + r_3 \newline
    r_2 &= r_3q_4 + r_4 \newline
    &~~\vdots \newline
    r_{i-2} &= r_{i-1}q_i + \underset{r_i}0 \newline
\end{aligned}
$$

and $\gcd(a,b) = r_{i-1}$.

#### Example

Find $\gcd(88,72)$.

##### Solution

$$ %Aligned
\begin{aligned}
    \underset{a}88 &= \underset{b}72 \cdot \underset{q}1 + \underset{r}16 \newline
    72 &= 16 \cdot 4 + 8 \newline
    16 &= 8 \cdot 2 + \underset{r_i}0\newline
\end{aligned}
$$

So $\gcd(88,72) = 8$.

#### Example

Find $\gcd(78,35)$.

##### Solution

$$ %Aligned
\begin{aligned}
    \underset{a}78 &= \underset{b}35 \cdot \underset{q}2 + \underset{r}8 \newline
    35 &= 8 \cdot 4 + 3 \newline
    8 &= 3 \cdot 2 + 2\newline
    3 &= 2 \cdot 1 + 1 \newline
    2 &= 1 \cdot 2 + \underset{\text{stop}}0 \newline
\end{aligned}
$$

So $\gcd(78,35) = 1$, they are _relatively prime_.

### Relative Primes

_definition_: If $a,b \in \mathbb Z$ and $\gcd(a,b) = 1$ then we say $a$ and $b$ are __relatively prime_ since they have no common factors.


#### Fact

For $a,b \in \mathbb Z$, not both zero, $\exists x,y \in \mathbb Z$ such that,

$$
    \gcd(a,b) = \underset{\text{Linear Combo}}{ax + by}.
$$

To find $x$ and $y$ we must use the _Euclidean Algorithm_ in reverse.

#### Example

Find $x,y$ such that $1 = 78x + 35y$.

##### Solution

$$ %Aligned
\begin{aligned}
    1 &= 3 - 2 \cdot 1 \newline
    &= 3 - (8 - 3 \cdot 2) \cdot 1 \newline
    &= 3 - 8 + 3 \cdot 2 \newline
    &= 3 \cdot 3 - 8 \newline
    &= 3 \cdot (35 - 8 \cdot 4) - 8 \newline
    &= 3 \cdot 35 - 12 \cdot 8 - 8 \newline
    &= 3 \cdot 35 - 13 \cdot 8 \newline
    &= 3 \cdot 35 - 13 \cdot (78 - 35 \cdot 2) \newline
    &= 3 \cdot 35 - 13 \cdot 78 - 26 \cdot 35 \newline
    &= \underset{x}{-13} \cdot 78 + \underset{y}{29} \cdot 35 \newline
\end{aligned}
$$

So $1 = \gcd(78,35) = 78x + 35y$ where $x = -13$ and $y = 29$.

#### Corollary

Let $a,b,x \in \mathbb Z$ such that $a \mid bx$. If $a$ and $b$ are relatively prime, then,

$$
    a \mid x
$$

##### Proof

Let $a,b,x \in \mathbb Z$ such that $a \mid bx$, and suppose, $a$ and $b$ are coprime, then,

$$
    \gcd(a,b) = 1
$$

By the last fact $\exists y,z \in \mathbb Z$ such that $\gcd(a,b) = ay + bz$. Multiplying by $x$ yields,

$$
    x = axz + bxy
$$

clearly, $a \mid axz$, since $a \mid bx$, $a \mid bxy$.

$$ %Aligned
\begin{aligned}
    &\therefore a \mid axz + bxy \newline
    &\therefore a \mid x \newline
\end{aligned}
$$

#### Corollary

Let $a,b,c \in \mathbb Z$ such that $c \mid a$ and $c \mid b$.

$$
    c \mid \gcd(a,b)
$$

### LCM

_definition_: If $a,b \neq 0$ are integers, we say $\ell$ is their __least common multiple__ if,

1. $a \mid \ell$ and $b \mid \ell$
2. if $a \mid m$ and $b \mid m$ then $\ell \le m$

and we write $\ell = \text{lcm}(a,b$).

#### Examples

* $\text{lcm}(3,4) = 12$
* $\text{lcm}(4,6) = 12$
* $\text{lcm}(1,a) = a$

#### Fact

$$
    \text{lcm}(a,b) = \frac{|ab|}{\gcd(a,b)}
$$
# Lecture 23 - Notes  

### June 26, 2015  

## Section 4.3 -- Primes

_definition_: A natural number $p > 1$ is called a __prime number__ if it is divisible only by itself and $1$.

A number $n > 1$ that is not prime is __composite__.

__Note__: $1$ is neither prime nor composite (it is "the unit").

#### Lemma

Given a natural number $n > 1$,

$$
    \exists \text{ a prime } p \text{ such that } p \mid n.
$$

##### Proof

> By Contradiction

Suppose to the contrary that there are natural numbers that are not divisible by a prime. By the Well-Ordering principal there is a smallest such natural number, $n$. If $n$ is prime,

$$
    n \mid n
$$

which is a contradiction. If $n$ is composite, then there exist $k \in \mathbb N$ where  $0 < k < n$ is not prime where,

$$
    k \mid n
$$

but since $n$ the smallest natural number that is not divisible by a prime,

$$
    p \mid k
$$

so $p \mid n$ which is a contradiction.

$$
    \therefore p \mid n
$$

### Fundamental Theorem of Algebra

Every natural number $n > 1$ can be written as the product of prime powers in exactly one way (up to ordering). That is, for any $n > 1$, we can write $n$ as a __prime factorization__.

$$
    n = p_1^{e_1} p_3^{e_2} p_3^{e_3}... p_k^{e_k}
$$

where $p_1$ is prime, and $e_i \ge 1$.

#### Examples

$$
\begin{aligned}
    6 &= 2^1 \cdot 3^1 = 3^1 \cdot 2^1 \newline
    18 &= 2^1 \cdot 3^2 \newline
    20 &= 2^2 \cdot 5 \newline
    7 &= 7 \newline
\end{aligned}
$$

#### Consequences of $\mathcal{FTA}$

If $n = p_1^{e_1} p_3^{e_2} p_3^{e_3}... p_k^{e_k}$ then,

$$
    p_i \mid n
$$

for $1 \le i \le k$.

If $n = p_1^{e_1} p_3^{e_2} p_3^{e_3}... p_k^{e_k}$ and,

$$
    d \mid n
$$

then,

$$
    d = p_1^{d_1} p_3^{d_2} p_3^{d_3}... p_k^{d_k}
$$

where $0 \le d_i \le e_i$.

If $p$ is prime and $p \mid a^2$, then,

$$
    p \mid a
$$

and in fact $p^2 \mid a^2$.

If $a = kb$, then $a$ and $kb$ have the same decomposition. 

#### Example

$$\begin{aligned}
    126 &= 2 \cdot 3^2 \cdot 7 \newline
    (2 \cdot 3 \cdot 7) &\mid 126 \newline
    (2 \cdot 3^3) &\nmid 126 \newline
\end{aligned}$$

#### Proposition

For a prime $p$, if $p \mid a \cdot b$, then,

$$
    p \mid a \text{ or } p \mid b
$$

##### Proof

If $p \mid a$ then we're done.

If $p \nmid a$ then , the $\gcd(p,a) = 1$, so by yesterday's corollary $p \mid b$. 
# Lecture 24 - Notes  

### June 30, 2015  

## Section 4.3 Continued

#### Theorem

There are infinitely many primes.

##### Proof

Suppose to the contrary that there are only a finite number of primes, call them,

$$
    p_1, p_2, ... p_n.
$$

Consider,

$$
    N = p_1p_2...p_n + 1
$$

since $N$ is larger than any $p_i$, $N$ is not prime ($N$ is composite). By the Lemma some prime divides $N$, since $p_1,p_2,...,p_n$ are all the primes,

$$
    p_i \mid N
$$

where $0 \le i \le n$. So,

$$\begin{aligned}
    N &= p_i(p_1 p_2...p_{i-1}p_{i-2}...p_n) + 1 \newline
    &= p_i m + \underbrace{1}_r \newline
\end{aligned}$$

where $m = p_1 p_2...p_{i-1}p_{i-2}...p_n$. So when we divide $N$ by $p_i$ we have a remainder of $1$. So $p_i \mid n$ which a contradiction.

$$
    \therefore \text{There are infinitely many primes.}
$$

### Paired Primes

Like,

$$
\begin{aligned}
    3&,5 \newline
    11&,13 \newline
    17&,19 \newline
\end{aligned}
$$

theres a conjecture that there are infinitely many paired primes. However it has yet to be proven.

#### Proposition (Test for Primality)

If $n > 1$ is composite,

then we know it has a prime divisor $p$ between $1 \le p \le \sqrt{n}$.

#### Example

Is $353$ prime?

##### Solution

$\sqrt{353} = 18.7$ so we need to test,

$$
    2,3,5,7,11,13,17
$$

Since none of these number divide $353$, $353$ is prime.

### Finding GCD using Prime Factorizations

If,

$$
    a = p_1^{a_1} p_2^{a_2} p_3^{a_3}... p_n^{a_n}
$$

for $a_i \ge 0$ and,

$$
    b = p_1^{b_1} p_2^{b_2} p_3^{b_3}... p_n^{b_n}
$$

for $b_i \ge 0$ then,

$$
    \gcd(a,b) = p_1^{\min(a_1,b_1)} p_2^{\min(a_2,b_2)} p_3^{\min(a_3,b_3)}... p_n^{\min(a_n,b_n)}
$$

and,

$$
    \text{lcm}(a,b) = p_1^{\max(a_1,b_1)} p_2^{\max(a_2,b_2)} p_3^{\max(a_3,b_3)}... p_n^{\max(a_n,b_n)}
$$



#### Example

Find $\gcd(270,1575)$. Using the $\mathcal{FTA}$,

$$\begin{aligned}
    270 &= 2 \cdot 3^3 \cdot 5 \newline
    1575 &= 3^2 \cdot 5^2 \cdot 7. \newline
\end{aligned}$$

So,


$$\begin{aligned}
    \gcd(270,1575) &= 3^2 \cdot 5\newline
    &= 45 \newline
\end{aligned}$$

and,


$$\begin{aligned}
    \text{lcm}(270,1575) &= 2 \cdot 3^3 \cdot 5^2 \cdot 7 \newline
    &= 9450 \newline
\end{aligned}$$

## Section 4.4 -- Congruences

_definition_: For a natural number $n \gt 1$, given integers $a$ and $b$, we says, $a$ is __congruent__ to $b$ modulo $n$,

$$
    a \equiv b \pmod n
$$

if,

$$
    n \mid (a - b)
$$

or $\frac{a}{n}$ and $\frac{b}{n}$ have the same remainder.

#### Example

Since,

$$\begin{aligned}
    9 &\equiv 2 \pmod 7 \newline
    16 &\equiv 9 \pmod 7 \newline
\end{aligned}$$
 
 we can say,
 
 $$
    2 \equiv 16 \equiv 9 \pmod 7
 $$

#### Example

It's 11 AM. What time will it be in 22 hours?

##### Solution

It will be 9 AM (not 33 AM).

Why? Times rollover after 24 hours.

#### Example

Draw a $405^\circ$ ray.

#### Solution

Since angles rollover after $360^\circ$, we can draw $45^\circ$.

### Least Residue mod $n$

_definition_:For integers $a$ and $b$ where $a \equiv b \pmod n$, we say $b$ is the __least residue mod $n$__ if $0 \le b \le n$.
# Lecture 25 - Notes  

### July 3, 2015  

## Section 4.4 Continued

#### Notice

$$
    \equiv \mod n
$$

is an equivalence relation with equivalence classes,

$$
    [0],[1],[2],...,[n-1]
$$

#### Example

The equivalence classes for $\bmod 3$ are,

$$\begin{aligned}
    \left[0\right] &= \{...,-9,-6,-3,0,3,6,9,... \} \newline
    [1] &= \{ ...,-8,-5,-2,1,4,7,... \} \newline
    [2] &= \{ ...,-7,-4,-1,2,5,8,... \} \newline
\end{aligned}$$

### Arithmetic $\bmod n$

#### Proposition

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

##### Proof

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

#### Warning

$$
    ac \equiv bd \pmod n
$$

__does not imply__ $a \equiv b \pmod n$

#### Example

Let $b \equiv 2 \pmod 4$,

$$\begin{aligned}
    2\cdot3 &\equiv 2 \cdot 1 \pmod 4 \newline
    3 &\not\equiv 1 \pmod 4 \newline
\end{aligned}$$
 
#### Proposition

If $ac \equiv bc \pmod n$ __and__ $\gcd(c,n) = 1$ then,

$$
    a \equiv b \pmod n
$$

#### Example

Solve,

$$
    3x - 34 \equiv 2 \pmod 7
$$

##### Solution

$$\begin{aligned}
    3x - 34 &\equiv 2 \pmod 7 \newline
    3x &\equiv 3 + 34 \pmod 7 \newline
    3x &\equiv 36 \pmod 7 \newline
    3x &\equiv 3 \cdot 12 \pmod 7 \newline
\text{since $\gcd(3,7) = 1$} \newline
    x &\equiv 12 \pmod 7 \newline
    &\equiv 5 \pmod 7
\end{aligned}$$

#### Example

Solve,

$$
    2x \equiv 30 \pmod 4
$$

##### Solution

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

# Lecture 26 - Notes  

### July 7, 2015  

## Section 4.4 Continued

#### Fact

$$
    9 \equiv -1 \pmod{10}
$$

#### Example

Find the last digit of $3^{123}$.

##### Solution

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

#### Application of Divisibility by 3

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

# Chapter 5 -- Induction

## Section 5.1 -- Mathematical Induction

#### Fact

The punctured $2^n \times 2^n$ chessboard can be tiled by the 3-square corner piece. Once you have the initial $2 \times 2$ board and you know the centre tile trick, you can solve any board.

#### Example

Consider a line of dominos, $1,2,3,...,n-1,n,n+1,...$ where domino $n$ falls over. This infers that dominos $n+1,n+2,...$ will fall.

We need two things to ensure all the dominos fall over,

1. We need to know one domino falls, an initial push (Basis)
2. We need to know that one domino falling will cause the others to fall (Inductive step)

### Induction

_definition_: 


#### Example

Prove that for any natural number $n \gt 1$,

$$
    \sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

##### Solution

Let $P(n)$ be the statement,

$$
    \sum_{i=1}^{n} i = \frac{n(n+1)}{2}
$$

where $n \in \mathbb N$ and $n \gt 0$.

###### Basis

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

####### Inductive Hypothesis

Suppose that $P(k)$ is true for some $k \in \mathbb N$ where $k \gt 1$, i.e.,

$$\begin{aligned}
    \sum_{i=1}^{k} i = \frac{k(k+1)}{2}
\end{aligned}$$

###### Inductive Step

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








# Lecture 27 - Notes  

### July 8, 2015  

### Mathematical Induction

Let $P(n)$ be a statement whose truth-value is dependant upon the variable $n$. Then $P(n)$ is true for all $n \ge n_0$ if both of the following hold,

1. $P(n)$ is true for $n = n_0$ (base)
2. If $P(k)$ is true for $K \ge n_0$, then $P(k+1)$ is also true (inductive step)

#### Example

Prove that for all $n \ge 1$,

$$\begin{aligned}
    \frac{1}{1\cdot2} + \frac{1}{2\cdot3} + \frac{1}{3\cdot4} + ... + \frac{1}{n(n+1)} &= \frac{n}{n+1} \newline
\end{aligned}$$

##### Solution

Let $P(n)$ be the statement,

$$\begin{aligned}
    \sum_{i=1}^{n} \frac{1}{i(i+1)} = \frac{n}{n+1}
\end{aligned}$$

where $n \in \mathbb N$, $n \ge 1$.

###### Base

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

###### Inductive Hypothesis

Suppose $P(k)$ is true for $k \ge 1$,

$$\begin{aligned}
    \sum_{i=1}^{k} \frac{1}{i(i+1)} = \frac{k}{k+1}
\end{aligned}$$

###### Inductive Step

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

#### Example

Prove that for $n \in \mathbb N$ where $n \ge 5$, $4n \le 2^n$.

##### Solution

Let $P(n)$ be the statement,

$$
    4n \le 2^n
$$

for all $n \in \mathbb n$ where $n \ge 5$.

###### Base

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

###### Inductive Hypothesis

Suppose $P(k)$ is true for $k \ge 5$, i.e.,

$$\begin{aligned}
    4k \le 2^k
\end{aligned}$$

###### Inductive Step

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



 


# Lecture 28 - Notes  

### July 10, 2015  

#### Example

Prove for $n \ge 1$,

$$
    2^n \mid (2n)!
$$

##### Solution

Let the tameness $P(n)$ be,

$$
    2^n \mid (2n)!
$$

for $n \in \mathbb N$ where $n \ge 1$.

###### Base

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

###### Inductive Hypothesis

Suppose $P(k)$ holds for some $k \in \mathbb N$ where $k \ge 1$, i.e.,

$$\begin{aligned}
    2^k \mid (2k)!
\end{aligned}$$ 

###### Inductive Step

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

### Strong Induction

> Induction with expanded base cases

_definition_: Let $P(n)$ be a statement whose truth-value depends upon $n$. If the following hold then  $P(n)$ is true for all $n \ge n_0$,

1. $P(n)$ is true for all $n = n_0, n_0 + 1, n_0 +2, ... ,t$ for some $t \ge n_0$. (Base)
2. If $P(m)$ is true for some $n_0 \le m \lt k$, then $P(k)$ is true. (Inductive Step)

#### Strategy

1. Show $P(n)$ is true for $n = n_0, n_0 + 1, n_0 +2, ... ,t$.
2. Suppose $P(m)$ is true for $n_0 \le m \lt k$.
3. Show $P(k)$ is also true.

#### Example

Show that any amount of postage greater than $12$ cents can be paid using only $3$ cent stamps and $7$ cent stamps.

##### Solution

Let $P(n)$ be the statement,

$$\begin{aligned}
    \text{postage of } n \text{ cents can be paid using } 3 \text{ and } 7 \text{ cent stamps.}
\end{aligned}$$

where $n \ge 12$.

###### Base

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

###### Inductive Hypothesis

Suppose $P(m)$ is true for some $12 \le m \le k$ where $k \in \mathbb N$ and $k \gt 12$.

###### Inductive Step

Consider $P(k+1)$, this implies $k+1 \gt 12$, by the induction hypothesis,

$$\begin{aligned}
    (k+1)-3 = k - 2
\end{aligned}$$

or $P(k-2)$ is payable, and therefore, by adding $3$ cents $P(k+1)$ is payable. Therefore, by induction $P(n)$, is payable.

# Lecture 29 - Notes  

### July 14, 2015  

## Section 5.2 -- Recursive Sequences

_definition_: A __recursive definition of a sequence__, $a_n$, has two parts,

1. One or more base cases
    * e.g. $a_0=1$, $a_1=7$
2. A recursive function
    * e.g. $a_i = 2 \cdot a_{i-1}$

#### Example 1

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

#### Example 2

The Fibonacci Sequence is another example. It can be defined as,

$$\begin{aligned}
    f_1 &= 1 \newline
    f_2 &= 1 \newline
    &~\vdots \newline
    f_n &= f_{n-1} + f_{n-2} \newline
\end{aligned}$$

for $n \ge 2$.

#### Example 3

Consider,

$$\begin{aligned}
    a_0 = 1 \newline
    a_n &= 3a_{n-1} + 1 \newline
\end{aligned}$$

##### Solution

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

#### Example

Let $a_0 = 0$, $a_1 = 3$ and for $n \ge 2$,

$$\begin{aligned}
    a_n = a_{n-1} + 2a_{n-2}
\end{aligned}$$

##### Solution

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

##### Proof

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
 
# Lecture 30 - Notes  

### July 15, 2015  

### Arithmetic Sequence

_definition:_ The __Arithmetic Sequence__ with the first term $a$ and the __common difference__ $d$ is defined recursively as,

$$\begin{aligned}
    a_0 &= a \newline
    a_n &= a_{n-1} + d \newline
\end{aligned}$$

The closed form is,

$$\begin{aligned}
    a_n = a + nd
\end{aligned}$$

for all $n \ge 0$.

### Geometric Sequence

_definition:_ The __Geometric Sequence__ with first term $a$ and __common ratio__ $r$ is recursively defined by,

$$\begin{aligned}
    a_0 &= a \newline
    a_n &= r \cdot a_{n-1} \newline
\end{aligned}$$


# Lecture 31 - Notes  

### July 21, 2015  

# Chapter 6

## Section 6.1 -- Principal of Inclusion - Exclusion (PIE)

#### Example

Let $\mathcal U$ be the students in the first three rows. Let $C$ be the students in the first three rows who have owned a cat. Let $D$ be the students in the first three rows who have owned a dog. Let $N$ be the students in the first three rows who have owned neither a cat or a dog. So,

$$
    N = C^C \cap D^C
$$

Claim,

$$
    |\mathcal U| = |C| + |D| + |N|
$$

in general this doesn't work, since a student could own a cat and a dog.

### Theorem -- 2-PIE

For sets $A$ and $B$ of some universal set $\mathbb U$,

$$
    |A \cup B| = |A| + |B| - |A \cap B|
$$

## Example

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

### 2-set Counting Principals

Let $A$ and $B$ be sets of the universal set $\mathcal U$.

1. $\left| A \cup B \right| = \left| A \right| + \left| B \right| - \left| A \cap B \right|$
2. $\left| A \cap B \right| \le \min(\left| A \right|,\left| B \right|)$
3. $\left| A^C \right| = \left| \mathcal U \right| - \left| A \right|$
4. $\left| A \setminus B \right| =  \left| A \right| - \left| A \cap B \right|$
5. $\left| A \oplus B \right| = \left| A \right| + \left| B \right| - 2\left| A \cap B \right|$
# Lecture 33 - Notes  

### July 24, 2015  

## Section 6.1 Continued

### Recall

* $|A \cup B| = |A| + |B| - |A \cap B|$
* $|A \cup B \cup C| = |A|+|B|+|C|-|A \cap B|-|A \cap C| - |B \cap C| + |A \cap B \cap C|$

#### Example

On an exam there are 25 questions, of which 18 are "hard", 10 are Multiple Choice and 6 are proofs.

##### How many hard multiple choice could there be?

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

#### How many easy, long, non-proof could there be?

We want,

$$\begin{aligned}
    |H^C \cap M^C \cap P^C| &= |(H \cup M \cup P)^C| \newline
    &= 25 - (|M| + |P| + |H| - |M \cap P| - |M \cap H| - |P \cap H| + |M \cap P \cap H|) \newline
\end{aligned}$$

### PIE Theorem

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

#### Example

Find $\Phi(150)$ where phi is the Euler function, i.e. al numbers less than $150$ that are cop rime to $150$.

##### Solution

$$\begin{aligned}
    150 = 2 \cdot 3 \cdot 5^2
\end{aligned}$$

* $n$ is cop rime to $150$ if $n$'s prime decomposition does not contain a $2,3$ or $5$.
* Let $A$ be the set of $1 \le n \le 150$ that do contain a $2$ in it's prime decomposition.
