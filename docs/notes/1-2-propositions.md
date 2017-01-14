# Section 1.2 &ndash; The Algebra of Propositions

If a statement is always true we call it a __tautology__. For example,

$$ p ~\vee \neg p $$

If a statement is always false we call it a __contradiction__. For example,

$$ p ~\wedge \neg p $$

## Logical Equivalence

_definition_: Two statements, $s_1$ and $s_2$ are __logically equivalent__ if the biconditional, $ s_1 \leftrightarrow s_2 $, is a tautology. It is then written,

$$ s_1 \iff s_2 $$

($ s_1 \leftrightarrow s_2 $ is a statement that can be true or false, $ s_1 \iff s_2 $ is a fact that they are logically equivalent)

### Notation


* $\mathbb{1}$ denotes a tautological statement.
* $\mathbb{0}$ denotes a contradiction statement.

## Laws of Logic

### Idempotence

$$ p \vee p \iff p $$
$$ p \wedge p \iff p $$

### Commutative

$$ p \vee q \iff q \vee p $$
$$ p \wedge q \iff q \wedge p $$

### Associative

$$ (p \vee q) \vee r \iff p \vee (q \vee r) $$
$$ (p \wedge q) \wedge r \iff p \wedge (q \wedge r) $$

Note,

$$ (p \wedge q) \vee r \nLeftrightarrow p \wedge (q \vee r) $$


### Distributive

$$ p \wedge (q \vee r) \iff (p \wedge q) \vee (p \wedge r) $$
$$ p \vee (q \wedge r) \iff (p \vee q) \wedge (p \vee r) $$


### DeMorgan's Laws

$$ \neg ( p \wedge q ) = (\neg p) \vee (\neg q) $$

$$ \neg ( p \vee q ) = (\neg p) \wedge (\neg q) $$



### Identity

$$ p \wedge \mathbb{1} \iff p$$
$$ p \vee \mathbb{0} \iff p$$

### Dominance

$$ p \wedge \mathbb{0} \iff \mathbb{0} $$
$$ p \vee \mathbb{1} \iff \mathbb{1} $$

### Other

$$ p \to q \iff \neg p \vee q $$
$$ \neg p \to q \iff p \vee q $$
$$ p \leftrightarrow q \iff (p \to q) \wedge (q \to p) \iff (\neg p \vee q) \wedge (p  \vee \neg q ) $$

## Using Laws of Logic to prove logical equivalence

**Example**

Show $ p \leftrightarrow q \iff (p \wedge q) \vee (\neg p \wedge \neg q) $.

**_Solution_**

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

**Example**

Show $ \neg q \vee ( p \to q ) $ is a tautology.

**_Solution_**

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