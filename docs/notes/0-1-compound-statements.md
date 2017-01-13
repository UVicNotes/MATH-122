# Section 0.1: Compound Statements

_definition_: A __statement__ or __proposition__ has a truth value.

### Examples

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

### _Non_ Examples

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

## Conjunction

Let $p$ and $q$ be statements. The conjunction of $p$ and $q$ is written:

$$ p \wedge q $$

### Truth Table

| $p$   | $q$   | $ p \wedge q $ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | False          |
| False | False | False          |

## Disjunction

Let $p$ and $q$ be statements. The disjunction[^math-inclusive-or] of $p$ and $q$ is written:
[^math-inclusive-or]: In mathematics or is always inclusive.

$$ p \vee q $$

### Truth Table

| $p$   | $q$   | $ p \vee q $ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | True           |
| False | True  | True           |
| False | False | False          |

## Implication

Let $p$ and $q$ be statements. The implication of $p$ to $q$ is written:

$$ p \rightarrow q $$

This implies a `if p then q` relationship.

### Truth Table

| $p$   | $q$   | $ p \rightarrow q $ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | True           |
| False | False | True           |


## Implication

$$ p \rightarrow q $$

$p$ is the _hypothesis_, $q$ is the _conclusion_.

* $p$ is sufficient for $q$
* $q$ is necessary for $p$

### Examples

(9 is odd) $\to$ (cats have fur)

This is `true`, because nine is odd.

---

(Fish live on land) $\to$ (10 is prime)

This is `false` because fish don't live on land.

## Bicondition or Double Implication

* Means $ p \to q $ and $ q \to p $
* $p$ and $q$ have the same truth value


| $p$   | $q$   | $ p \leftrightarrow q $ |
|-------|-------|----------------|
| True  | True  | True           |
| True  | False | False          |
| False | True  | False           |
| False | False | True           |

Said as "$p$ if and only if $q$" or "$p$ iff $q$"

## Negation

_definition_: The __negation__ of a statement $p$, written:

$$ \rightharpoondown p $$


| $p$   | $\rightharpoondown p $   |
|-------|-------|
| True  | False |
| False  | True |

Notation: $\rightharpoondown$ supersedes any other notation. So:

$$ \rightharpoondown p \vee q = (\rightharpoondown p) \vee q $$

### DeMorgan's Laws

$$ \rightharpoondown ( p \wedge q ) = (\rightharpoondown p) \vee (\rightharpoondown q) $$

$$ \rightharpoondown ( p \vee q ) = (\rightharpoondown p) \wedge (\rightharpoondown q) $$


### Example

$p =$ "John owns a cat"

$q =$ "John owns a dog"

Find:

$$ \rightharpoondown ( p \wedge q ) $$

#### Solution

We only need to break on one half to negate it.

So $ \rightharpoondown ( p \wedge q ) =$ "John doesn't own a cat or he does not own a dog"


## Contrapositive

_definition_: The __contrapositive__ of $p \to q$ is written:

$$ \rightharpoondown q ~ \to ~ \rightharpoondown p $$

### Example

The contrapositive of "If it rains in the morning I will bring an umbrella" is "If I did not bring an umbrella than it did not rain this morning".

## Converse

_definition_: The __converse__[^f1] of $p \to q$ is written:

$$ q \to p $$

### Example

The converse of "If it rains in the morning I will bring an umbrella" is "If I brought an umbrella it was raining this morning"[^f2].

[^f1]: While the contrapositive is is logically equivalent to the statement the converse is not.
[^f2]: this is not logically equivalent.


| $p$   | $q$   | $ p \to q $ | $ \rightharpoondown q \to \rightharpoondown p $ | $ q \to p $ |
|---|---|---|---|---|
| True  | True  | True | True | True |
| True  | False | False | False | True |
| False | True  | True | True | False |
| False | False | True | True | True |

## Quantifiers

### Universal Quantifier

"_For all_ integers $n$, $2n$ is even".

_For all_ is the quantifier as it quantifies the amount. In this case it is the __universal quantifier__ equivalent to:

* For all... (duh)
* For each...
* For every...
* $\forall$

### Existential Quantifier

_definition_: The __existential quantifier__ states that this statement applies for some but not all things. It can be written:

* For some...
* There exists a...
* $\exists$

### Example

"Some rectangles are squares" can be written "$\exists$ a rectangle $R$, such that $R$ is square"


### Example

Write the following in plain english:

$$ \forall x, \exists y, x + y = 0 $$

Where the universe of $x$ and $y$ is the integers.

#### Solution

For all integers $x$ there exists a $y$ such that the sum of $x$ and $y$ is zero.

### Example

Write the following in plain english:

$$ \exists y, \forall x, x + y = 0 $$

Where the universe of $x$ and $y$ is the integers.

#### Solution

This is not true because there not all $x$'s would make zero for any $y$.

## Negation of Quantifiers

$$ \neg \forall ~ x, s(x) = \exists ~ x, \neg s(x) $$
$$ \neg \exists ~ x, s(x) = \forall ~ x, \neg s(x) $$

### Example

Prove,

$$ \neg (\forall ~ n \ge 0, n^2 - n + 41 ~\text{is prime}) $$

#### Solution

This becomes,

$$ \exists ~ n \ge 0, n^2 - n + 41 ~\text{is not prime} $$

Which we can prove by example.

## Set Notation

$$ \mathbb{Z} = \text{The set of all integers} $$

$$ \mathbb{R} = \text{The set of all real numbers} $$

$$ \mathbb{N} = \text{The set of all natural numbers} $$

$$ \mathbb{Q} = \text{The set of all rational numbers} $$

$ \in $ denotes that something belongs to a set.

### Example

$$ x \in \mathbb{Z} = x \text{ is an integer} $$
