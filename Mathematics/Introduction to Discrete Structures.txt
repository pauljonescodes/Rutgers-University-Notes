# Discrete Structures
## Chapter 2 - Sets, Functions, Sequences, Sums, and Matrices
### Section 1 - Sets
#### Introduction
- Sets are collections of objects
- Sets are used to group objects together
- **Set**: A *set* is an unordered collection of objects, called elements or members of the set. A set is said to contain its *elements*. We write a ∈ **A** to denote that a is an element of the set **A**. The notation a ̸∈ **A** denotes that a is not an element of the set **A**.
- Conventional sets:
	- **N** = {0,1,2,3,...}, the set of natural numbers;
	- **Z** = {...,−2,−1,0,1,2,...}, the set of integers;
	- **Z+** = {1, 2, 3, . . .}, the set of positive integers;
	- **Q** = {p/q | p ∈ Z, q ∈ Z, and q ̸= 0}, the set of rational numbers;
	- **R,** the set of real numbers;
	- **R+**, the set of positive real numbers;
	- **C**, the set of complex numbers;
- Datatypes in computer science are built upon the concept of a set. Interestingly, boolean values are all subsets of `{0, 1}`.
- The Empty Set
	- The empty set is a special set which is a set containing no elements. Denoted by either `∅` or `{}`, but not `{∅}`, which is a set containing the empty set, which would be `{{}}`.
- A Singleton Set
	- Singleton sets contain one element, for instance `{∅}`.

#### Subsets
- **Subset**: The set A is a subset of B if and only if every element of A is also an element of B. We use the notation A ⊆ B to indicate that A is a subset of the set B.
- The quantification for the sets A and B, a being a subset of B, is `∀x(x ∈ A → x ∈ B)`. This translates to "For all `x` it is true that if `x` is an element in `A`, then `x` is an element in `B`.
	- Some conditions for proving subset relationships:
		- To show that `A` is a subset of `B`, show that if x belongs to A then x also belongs to B.
		- To show that A is not a subset of B, find a single `x ∈ A` such that `x` is not an element in `B`.
- *Theorem*: For every set `S`,`∅ ⊆ S` and `S ⊆ S`.
- **Proper subset**: ∀x(x ∈ A → x ∈ B) ∧ ∃x(x ∈ B ∧ x ̸∈ A)
- **Equal sets**: For two equal sets, `A` is a subset of `B` and `B` is a subset of `A`.

#### The Size of a Set
- **The size of a set**: Let `S` be a set. If there are exactly n distinct elements in `S` where `n` is a nonnegative integer, we say that `S` is a finite set and that `n` is the cardinality of `S`. The cardinality of `S` is denoted by `|S|`.

#### Power Sets
- Given a set `S`, the power set of S is the set of all subsets of the set `S`. The power set of `S` is denoted by `P(S)`.
- **Formula**: If a set has `n` elements, then its power set has `2n` elements.

#### Cartesian Products
- **Ordered n-tuples**: The ordered `n`-tuple (`a_1`, `a_2`, … , `a_n`) is the ordered collection that has `a_1` as its first element, `a_2` as its second element, . . . , and `a_n` as its `n`th element.
- It's interesting to note that in a Cartesian system of 4 quadrants, the one that you learnt in elementary school and have been relearning in every math class since, can be expressed in terms of an ordered n-tuple. Specifically, it's a Cartesian product, an ordered pair.
- **Cartesian product**: Let `A` and `B` be sets. The Cartesian product of `A` and `B`, denoted by `A × B`, is the set of all ordered pairs `(a, b)`, where `a ∈ A` and `b ∈ B`. Hence, `A × B = {(a, b) | a ∈ A ∧ b ∈ B}`.
- **Relation**: A subset R of the Cartesian product `A × B` is called a relation from the set `A` to the set `B`.

#### Exercises
- List the members of these sets.
	- `{x | x is a real number such that x^2 = 1}`
		- The two numbers that satisfy the quantification are `-1` and `1`. Thus, this set is the set: 
	- `{x | x is a positive integer less than 12}`
		- `{1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11}`
	- `{x | x is the square of an integer and x < 100}` 
		- `{1^2, 2^2, 3^2, 4^2, 5^2, 6^2, 7^2, 8^2, 9^2}`	
	- `{x | x is an integer such that x^2 = 2}`
		- `{}` (It's the empty set you dirty bastards. Or I'm bad at math.) (Just checked. It's the empty set. There's no tricking me motherfucker!)
- For each of these pairs of sets, determine whether the first is a subset of the second, the second is a subset of the first, or neither is a subset of the other.
	- the set of airline flights from New York to New Delhi, the set of nonstop airline flights from New York to New Delhi
		- Every element in the set of nonstop airline flights will also be an element in the set of all flights. Therefore, the second is subset of the first.
	- the set of people who speak English, the set of people who speak Chinese
		- Neither of these are subsets of the other.
	- the set of flying squirrels, the set of living creatures that can fly
		- The set of flying squirrels is *probably* an empty set. By definition, if it is the first set, then it will be a subset of the second set.
- Determine which of these sets are equal:
	- `{1,3,3,3,5,5,5,5,5},{5,3,1}`
		- These sets are equal because duplicates do not count.
	- `{{1}},{1,{1}} `
		- These sets are not equal because `{1}` does not equal `1`
	- `∅,{∅}`
		- This is covered at the beginning of the chapter.
- For each of the following sets, determine whether 2 is an element of that set.
	- `{x ∈ R|x is an integer greater than 1}`
		- Two is an element in that set.
	- `{x ∈ R|x is the square of an integer}`
	- Two is not an element in that set. There exists no integer such that that same number squared will equal 2.
	- `{2,{2}} `
		- Two is an element in that set.
	- `{{2},{{2}}}`
		- Two is not an element in that set. {2} does not equal 2.
	- `{{2},{2,{2}}}` 
		- Two is not an element in that set.
	- `{{{2}}}`
		- Two is not an element in that set. It doesn't matter how many times you nest it.
- Determine whether each of these statements is true or false.
	- `0∈∅` is false. Zero is not an element of the empty set.
	- `∅ ∈ {0}` is false. The empty set is a subset of all sets, not an element. Hmm. Curious. 
	- `{0} ⊂ ∅` is false.
	- `∅ ⊂ {0}` is true.
	- `{0} ∈ {0}` is false. 
	- `{∅} ⊆ {∅}` is false.
	- `{0} ⊂ {0}` is true.
- Determine whether each of these statements is true or false.
	- `x ∈ {x}` is true.
	- `{x} ⊆ {x}` is false.
	- `{x} ∈ {x}` is false.
	- `{x} ∈ {{x}}` is true.
	- `∅ ⊆ {x}` is true.
	- `∅ ∈ {x}` is false.
- What is the cardinality of each of these sets?
	- The cardinality of `{a}` is 1.
	- The cardinality of `{{a}}` is 1.
	- The cardinality of `{a, {a}}` is 2.
	- The cardinality of `{a, {a}, {a, {a}}}` is 3.
- Find the power set of each of these sets, where a and b are distinct elements.
	- `P({a}) = {{a}, {}}` 
	- `P({a,b}) = {{a}, {b}, {a, b}, {}}`
	- `P({∅,{∅}}) = {{∅}, {{∅}}, {∅, {∅}}, ∅}`
- How many elements does each of these sets have where a and b are distinct elements? (Read: What is the cardinality of these power sets?)
	- `|P({a,b,{a,b}})| = 2^3`
	- `|P({∅,a,{a},{{a}}})| = 2^4`
	- `|P(P(∅))| =` (I would like an explanation for this.)
- Let A = {a,b,c,d} and B = {y,z}. Find:
	- `A×B = {(a, y), (b, y), (c, y), (d, y), (a, z), (b, z), (c, z),(d, z)}`
	- `B×A = {(y, a), (y, b), (y, c), (y, d), (z, a), (z, b), (z, c), (z, d)}`

### Section 2 - Set Operations
#### Introduction
- **Union**: Let A and B be sets. The union of the sets A and B, denoted by A ∪ B, is the set that contains those elements that are either in A or in B, or in both.
	- Quantification: A ∪ B = {x | x ∈ A ∨ x ∈ B}
- **Intersection**: Let A and B be sets. The intersection of the sets A and B, denoted by A ∩ B, is the set containing those elements in both A and B.
- **Disjoint**: Two sets are called disjoint if their intersection is the empty set.
- **Difference**: Let A and B be sets. The difference of A and B, denoted by A − B, is the set containing those elements that are in A but not in B. The difference of A and B is also called the complement of B with respect to A.
- **Complement**: Let U be the universal set. The complement of the set A, denoted by A, is the complement of A with respect to U . Therefore, the complement of the set A is U − A.

#### Set Identities
- Identity laws
	- A ∩ U = A 
	- A ∪ ∅ = A
- Domination laws
	- A ∪ U = U 
	- A ∩ ∅ = ∅
- Idempotent laws
	- A ∪ A = A 
	- A ∩ A = A
- Complementation law
	- comp(comp(A)) = A
- Commutative laws
	- A∪B=B∪A 
	- A∩B=B∩A
- Associative law
	- A ∪ (B ∪ C) = (A ∪ B) ∪ C 
	- A ∩ (B ∩ C) = (A ∩ B) ∩ C
- Distributive law
	- A ∪ (B ∩ C) = (A ∪ B) ∩ (A ∪ C) 
	- A ∩ (B ∪ C) = (A ∩ B) ∪ (A ∩ C)
- DeMorgan's laws
	- comp(A ∩ B) = comp(A) ∪ comp(B)
	- comp(A ∪ B) = comp(A) ∩ comp(B)
- Absorption laws
	- A ∪ (A ∩ B) = A 
	- A ∩ (A ∪ B) = A
- Complement laws
	- A ∪ comp(A) = U 
	- A ∩ comp(A) = ∅

#### Exercises
1. Let A be the set of students who live within one mile of school and let B be the set of students who walk to classes. Describe the students in each of these sets.
- `A ∩ B` 
- A∪B
- A−B 
- B−A
3. Let A = {1,2,3,4,5} and B = {0,3,6}. Find
- A∪B 
- A∩B 
- A−B 
- B−A

### Section 3 - Functions
- Let A and B be non empty sets. A function from A to B is an assignment of exactly one element of B to each element of A. We write f(a) = b if b is the unique element of B assigned by the function f to the element a of A. If f is a function from A to B, we write f : A → B.
	+ Also called functions and transformations.
- If f is a function from A to B, we say that A is the domain of F and B is the codomain of f. If f(a) = b, we say that b is the image of a and a is the pre image of b. The range, or image, of f is the set of all images of elements of A. 
	+ Also, if f is a function from A to B. we say that f maps A to B.
- Two functions are equal when they have the same domain, same codomain, and map each element identically.

#### Types of functions
##### Injective functions (One-to-One)
- A function `f` is said to be one-to-one, or an injunction, where `f(a) = f(b) ⇔ a = b` for all a and b in the domain of `f`. `A` functions said to be injective if it is one to one.
	- We can express that f is one to one with the quantification: `∀a∀b(f(a) = f(b) → a = b)`, where the universe of discourse is the domain of the function.

##### Surjective functions (Onto)
- A function `f` from `A` to `B` is called onto, or a surjection, if and only if for every `b ∈ B` there is an element `a ∈ A` with `f(a) = b`. a function `f` is called surjective if it is onto. 
	- What this means that if you have two sets of things, A and B, a function f is said to be onto if every element b ∈ B has an element a ∈ A such that `f(a) = b`. 
- `∀ a ∈ A(∃ b ∈ B(f(a) = b)))`

##### Bijective functions (Onto and One-to-One)
- If and only if `(f(a) = f(b) → a = b) ∧ (∀ b ∈ B(∃ a ∈ A f(a) = b))`

##### Partial functions
- A **partial function** f from a set A to a set B is an assignment to each element a in a subset of A, called the domain of definition of f , of a unique element b in B. 
- The sets A and B are called the domain and codomain of f, respectively. We say that f is undefined for elements in A that are not in the domain of definition of f. 
- When the domain of definition of f equals A, we say that f is a **total function**.

##### Increasing and decreasing
- A function f whose domain and codomain are subsets of real numbers is called **increasing** if f(x) ≤ f(y), and strictly increasing if f(x) \< f(y), whenever x \< y and x and y are in the domain of f. Invert all of that for decreasing and strictly decreasing.

##### Inverse functions
- A one-to-one correspondence is called invertible because we can define an inverse of this function. A function is not invertible if it is not a one-to-one correspondence, because the inverse of such a function does not exist. 
- A function must be injective to be invertible.

##### Rules
- To show that f is **injective**: Show that if f(x) = f(y) for arbitrary x,y ∈ A with x != y then x = y.
- To show that f is **not injective**: Find particular elements x, y ∈ A such that x != y and f(x) = f(y).
- To show that f is **surjective**: Consider an arbitrary element y ∈ B and find an element x ∈ A such that f (x) = y.
- To show that f is **not surjective**: Find a particular y ∈ B such that f(x) != y for all x ∈ A.

### CS 205 Quiz #4B
1. For each of the following statements, provide the cardinality of the result.
	* `{1, 2, 3, 3, 4}` - Being as there is a duplicate, it does not count towards the cardinality of the result, which is just the count of the elements. 4
	* `∅ ∪ {1, 2, ∅, ∅}` - Union means that one includes the elements from both sets in the final set. In the second set, there are two of the same element. Only one counts towards the cardinality. There are no elements to union in the first set, so effectively, the second set is the only one that counts. The cardinality is therefore, 3.
	* `∅ ∩ {1, 2, ∅, ∅}` - The question in English is something like, "What is the cardinality of the set of things that the empty set and this set share?" The empty set intersected with anything will yield a cardinality of 0.
	* `{1, 2, ∅, ∅} - ∅` - "Take away all the elements in the empty set away from this set." Inevitably, I think that the result of this operation will be the unchanged set on the left of the operation. Being as there is a duplicate element, the cardinality is 3.
	* `∅ ∩ {∅, {∅}}` - "What does the empty set share with with this set containing the empty set and a set containing the empty set." It can only be an empty set … right? 0.
	* `∅ ∪ {∅} ∪ {{∅}}` - "What is the resulting set from combining the empty set set with a set containing the empty set and a set containing a set which contains the empty set." Cardinality: 2. (The empty set contains no elements, but the other two are sets containing the empty set and a set containing a set which contains the empty set."
	* `{∅} × {∅}` - I think this results in a set that looks like this: `{(∅, ∅)}`. That would be the Cartesian double of the operation, but I'm not sure if the item inside the set is a set, but it doesn't matter, it doesn't affect this particular problem. The cardinality is 1. Interesting to note: the Cartesian product of any set with the empty set is the empty set.
	* `{1, 1} × {3, 3}` - This yields: `{{1,3}, {1, 3}, {1,3}, {1, 3}}`. Bobby says the answer is 4, but I think those sets are duplicates. So 4.
	* `({1, 2} × {3, 4}) × {5, 6}`
		+ Yields: `{{1, 3}, {1, 4}, {2, 3}, {2, 4}} × {5, 6}`
		+ Contin: `{{{1, 3}, 5}, {{1, 4}, 5}, {{2, 3}, 5}, {{2, 4}, 5} … }`
		+ The cardinality is 8.
	* `∅ × ∅` - The empty set multiplied by any other set, including the empty set, yields the empty set, thus the cardinality must be zero. Additionally, I just read the proof that the cardinality of a product of sets is the number of elements in both sets multiplied by each other, which also leads me to zero.
	* `{{1, 2} × {3, 4}} - {{3, 4} × {2, 1}}`
		+ `A = {{1, 3}, {1, 4}, {2, 3}, {2, 4}}`
		+ `B = {{3, 2}, {3, 1}, {4, 2}, {4, 1}}`
		+ `A - B` will equal the set that has all the elements of A which B does not have. Cardinality: 4.
2. For each of the following statements, provide the cardinality of the result:
	* `P({1, 2})` - There is no trickery here, so the cardinality of this power set is simply two raised to the number of elements in the set.
	* `P({}) ∩ P({1})` - So the power set of the empty set yields a set containing the empty set. The power set of the set containing one is a set containing a set containing one and the empty set. Thus:
	* + `|{∅} ∩ {{1}, ∅}| = 1`
	* `P({}) ∪ P({1})` - `|{∅} ∪ {{1}, ∅}| = 2`
	* `P({∅}) ∩ P({1})` - `|{{∅}, ∅} ∩ {{1}, ∅}| = |{∅}| = 1`
	* `P({∅}) ∪ P({1})` - Alright, so what we're looking at is the union of the power set of a set containing the empty set with a set containing the integer one. Each set has a cardinality of 2 because they contain one element. - `|{{∅}, ∅} ∪ {{1}, ∅}| = |{{∅}, {1}, ∅}| = 3`
	* `P({{∅}}) ∩ P({1})` - The general idea surrounding the power set of a nested empty set is that the resulting set will always be the empty set and the set containing the nested empty set. - `|{∅, {{{∅}}}} ∩ {∅, {1}}| = |{∅}| = 1`
	* `P({{∅}}) ∪ P({1})` - `|{∅, {{{∅}}}} ∪ {∅, {1}}| = |{∅, {{{∅}}}, {1}}| = 3`
	* `P({1, 2} ∪ {3})` - `|P({1, 2} ∪ {3})| = |P({1, 2, 3})| = 2^3`
	* `P({1, 2}) ∪ P({3})` - `|{{}, {1}, {2}, {1, 2}} ∪ {{3}, {}}| = 5`
	* `P({1, 2} ∪ P({3}))` - `|P({1, 2} ∪ {{3}, ∅})| = |P({1, 2, {3}, ∅})| = 2^4`
	* `P({1, 2, 3, 4, 5}) ∩ P({5, 6, 7, 8, 9})`
	* `P({1, 2, 3, 4, 5}) ∪ P({5, 6, 7, 8, 9})`
3. For each of the following statements, provide the cardinality of the result.
	* `P({1, 2, 3}) - P({1, 2, 3, 4, 5})` - `A = P({1, 2, 3}) = {∅, {1}, {2}, {3}, {1, 2}, {1, 2, 3}, {2, 3}, {1, 3}}` -  So I think that every element in the set above will be contained in the power set of the set to the right of the question. In which case, if I'm taking away every element in B (the one on the right of question) from A, and B contains every element in A, I'll be left with the empty set. Which has a cardinality of 0.
	* `P({1, 2, 3, 4, 5}) - P({1, 2, 3})` - Now this is much more interesting. So, as an informal proof of the answer, call the power set on the left A and the power set on the right B. Every element in B will be an element in A. A will have 2^5 elements, and B will have 2^3 elements. A ha! I was right, my test is marked wrongly.
	* `P(P(∅) - P(∅))` -  The power set of the empty set is `{∅, {∅}}`. This question is basically asking for the cardinality of the power set of the empty set, which is 2.
	* `P(P(P(P(∅))))` - 

     |P(P(P(P(∅))))| = |P(P(P({∅, {∅}})))| = |P(P({∅, {∅, {∅}}, {∅}, {{∅}}))| = |P({{}, {{}}, {{{}, {{}}}}, {{{}}}, {{{{}}}}, {{}, {{}, {{}}}}, {{}, {{}}}, {{}, {{{}}}}, {{{}, {{}}}, {{}}}, {{{}, {{}}}, {{{}}}}, {{{}}, {{{}}}}, {{}, {{}, {{}}}, {{}}}, {{}, {{}, {{}}}, {{{}}}}, {{}, {{}}, {{{}}}}, {{{}, {{}}}, {{}}, {{{}}}}, {{}, {{}, {{}}}, {{}}, {{{}}}}})| = 2^16

	* `P(P(∅) ∩ P(∅))`
	* `P(P(∅) × P(∅))`
	* `P(P(∅) × P(∅) × ∅)`

## Chapter 3 - Algorithms
### Recitation - November 6, 2012
1. Recall our discussion from lecture regarding loops of the follow form:
	* `x <- x_0`
	* `while x < a`
		+ `x <- x + 1`
	* `end`
	- Assuming `a > x_0`:
		* If we're looking for the value of `x`, after the first iteration, it will equal `x_0 + 1`.
		* In terms of `x_0`, after the second iteration it will be incremented again.
		* This stops when `x >= a`
		* `x_0 + i >= a`
		* `i >= a - x_0`
2. How many iterations are performed for the following loop?
	- `x <- x_0`
	- `while x < a`
		+ `x <- 5x`
	- `end`
3. How many iterations are performed for the following loop?
	- `x <- x_0`
	- `while x < a`
		* `x <- x^2`
	- `end`
	- This performs `x = ((x_0^2)^2)^2) … ^2` "i times"
4. How many iterations are performed for the following loop?
	- `x <- x_0`
	- `while x < a`
		+ `x <- x^{1/3}`
	- `end`
	- Assuming `x_0 < a` and `a < 1`
5. Determine whether each of these function is `O(x^2)`
	- `f(x) = 17x + 11`
	- `f(x) = x^2 + 1000`
	- `f(x) = xlog(x)`
	- `f(x) = x^4 / 2`
	- `f(x) = 2^x`
	- `f(x) = floor(x) * ceil(x)`

### Section 1 - Algorithms
#### Introduction
- An **algorithm** is a finite sequence of precise instructions for performing a computation or for solving a problem.
- Properties of Algorithms
	- Input. An algorithm has input values from a specified set.
	- Output. From each set of input values an algorithm produces output values from a specified set. The output values are the solution to the problem.
	- Definiteness. The steps of an algorithm must be defined precisely.
	- Correctness. An algorithm should produce the correct output values for each set of input values.
	- Finiteness. An algorithm should produce the desired output after a finite (but perhaps large) number of steps for any input in the set.
	- Effectiveness. It must be possible to perform each step of an algorithm exactly and in a finite amount of time.
	- Generality. The procedure should be applicable for all problems of the desired form, not just for a particular set of input values.

#### Searching Algorithms
- **Linear search**, searching through a list of items one at a time until the desired value is found.
- **Binary search**, which is performing a search on an ordered list of entries, starting in the middle, then going to the "middle of the middle", then its middle, until the item is either found or shown to not exist.

#### Sorting
- **Sorting** is putting these elements into a list in which the elements are in increasing order.

#### Exercises  
### Section 2 - The Growth of Functions
#### Big-O Notation
- Let `f(x)` and `g(x)` be functions. We say that `f(x)` is `O(g(x))` if there are constants `C` and `k` such that `|f(x)| ≤ C|g(x)|` whenever `x > k`. 
	* Intuitively, the definition that `f(x)` is `O(g(x))` says that `f(x)` grows slower that some fixed multiple of `g(x)` as `x` grows without bound.
	* To show that `f(x)` is `O(g(x))`, we need find only one pair of constants `C` and `k`, the witnesses, such that `|f(x)| ≤ C|g(x)|` whenever `x > k`.
- A useful approach for finding a pair of witnesses is to first select a value of `k` for which the size of `|f(x)|` can be readily estimated when `x > k` and to see whether we can use this estimate to find a value of `C` for which `|f(x)| ≤ C|g(x)|` for `x > k`.

##### Example 1
Show that `f(x)= x^2 + 2x + 1` is `O(x2)`.

- When `x > 1`, `x^2 + 2x + 1 < x^2 + 2x^2 + x^2 = 4x^2`
- Stripping coefficients, `O(x^2)` where `C = 4` and `k = 1`

##### Example 2
Show that `7x^2` is `O(x^3)`.

- When `x > 1`, `7x^2 < 7x^3`.
- Where `C = 7` and `K = 1` are witnesses, `7x^2' is `O(x^3)` 

##### Example 3
Show that `n^2` is not `O(n)`.

- Where `n > 1`, `n^2` is not less than `n`

##### Example 4
Example 2 shows that `7x^2` is `O(x^3)`. Is it also true that `x^3` is `O(7x^2)`?

### Lecture (Assorted)
#### Algorithms
- An algorithm is a "recipe", a finite set of instructions that precisely outline how to accomplish a task, function, etc.
- Something we always have to deal with in computer science is lists. For instance, the list:
	- `13, 4, 9, 10, 7`
	- Which is the maximum? 
		- The way to answer this is to have an algorithm.

#### Complexity
- Two considerations:
	1. Space
	2. Time (number of operations, comparisons perhaps)
- "If my unit of work is a comparison, then the complexity of the max algorithm is going the same as the number of inputs."
- There are algorithms that are more "efficient" than others in that they take less comparisons or operations than an alternative algorithm which performs the same function. For instance, for the greatest element example, binary search on a sorted array is more efficient, that is, takes less operations to perform the same function (but requires a sorted array).
- He is now going through binary search.
- Some questions about any given algorithm:
	- What is the best case?
	- What is the average case?
	- What is the average case?

#### Big O and Efficiency Analysis
##### Big O
- What's quite not completely correct about this?
	- Big O allows you to filter out constants
	- This can cause problems with certain constants
	- There exists c_1, c_2, and k such that c * g(x)
##### P = NP ?
- NP-complete
	- Was defined in the early 70s
	- Two classes of programs.
		- Polynomial - solvable?
		- Exponential - not solvable.
	- NP stands for "Non-deterministic polynomial"

## Chapter 10 - Graphs
### Section 1 - Graphs and Graph Models
#### Graphs
- A **graph** `G = (V,E)` consists of `V`, a nonempty set of vertices (or nodes) and `E`, a set of edges. 
- Each **edge** has either one or two vertices associated with it, called its **endpoints**. 
	- An edge is said to connect its endpoints.
- Types of graphs
	- **Infinite graphs** are graphs with an infinite vertex set or infinite number of edges.
	- **Finite graphs** are graphs that they have a finite number of vertices and edges.
	- **Simple graphs** are graphs in which each edge connects two different vertices and where no two edges connect the same pair of vertices.
		- Undirected
		- No multiple edges allowed
		- No loops allowed
	- **Multigraphs** are graphs which have multiple edges connecting the same vertices.
		- Undirected
		- Multiple edges allowed
		- Loops not allowed
	- **Psuedographs** are multigraphs that may contain loops.
		- Undirected
		- Multiple edges allowed
		- Loops allowed
	- **Directed graphs** consist of a nonempty set of vertices `V` and a set of directed edges (or arcs) `E`. Each directed edge is associated with an ordered pair of vertices. The directed edge associated with the ordered pair `(u, v)` is said to start at `u` and end at `v`.
	- **Directed simple graphs** are directed graphs that have no loops and have no multiple directed edges
		- Directed
		- No multiple edges
		- No loops allowed
	- **Directed multigraphs** have multiple directed edges.
		-  Directed
		-  Multiple edges allowed
		-  Loops allowed
	- **Mixed graphs**
		-  Directed and undirected 
		-  Multiple edges allowed
		-  Loops allowed

#### Graph Models
- Examples of graphs
	- Social networks
		-  Acquaintanceship and Friendship Graphs
		-  Influence Graphs
		-  Collaboration Graphs
	- Communication networks
		-  Call graphs
	- Information networks
		-  The web graph
		-  Citation graphs
		-  A call graph
	- Software design applications
		-  Module dependency graphs
		-  Precedence graphs and concurrent processing
	- Transportation networks
		-  Airline routes
		-  Road networks
	- Biological networks
		-  Niche overlap graphs in ecology
		-  Protein interaction graphs
	- Tournaments
		- Round-Robin tournaments
		- Single elimination tournaments

#### Exercises 
3. Simple graph
5. Pseudograph
7. Directed graph
9. Directed multigraph 
1. Draw graph models, stating the type of graph used, to represent airline routes where every day there are:
	- four flights from Boston to Newark, 
	- two flights from Newark to Boston
	- three flights from Newark to Miami, 
	- two flights from Miami to Newark, 
	- one flight from Newark to Detroit, 
	- two flights from Detroit to Newark, 
	- three flights from Newark to Washington, 
	- two flights from Washington to Newark, and 
	- one flight from Washington to Miami, with
		* an edge between vertices representing cities that have a flight between them (in either direction).
		* an edge between vertices representing cities for each flight that operates between them (in either direction).
		* an edge between vertices representing cities for each flight that operates between them (in either direction),
		* plus a loop for a special sightseeing trip that takes off
and lands in Miami.
		* an edge from a vertex representing a city where a flight
starts to the vertex representing the city where it ends.
		* an edge for each flight from a vertex representing a city where the flight begins to the vertex representing
the city where the flight ends.

13\. The **intersection graph** of a collection of sets `A_1, A_2,…,A_n` is the graph that has a vertex for each of these sets and has an edge connecting the vertices representing two sets if these sets have a nonempty intersection. Construct the intersection graph of these collections of sets.

a.

    A_1 = {0,2,4,6,8}
    A_2 = {0,1,2,3,4}
    A_3 = {1,3,5,7,9} 
    A_4 = {5,6,7,8,9}
    A_5 = {0,1,8,9}

b.

    A_1 = {...,−4,−3,−2,−1,0}
    A_2 = {...,−2,−1,0,1,2,...}
    A_3 = {...,−6,−4,−2,0,2,4,6,...}
    A_4 = {...,−5,−3,−1,1,3,5,...}
    A_5 = {...,−6,−3,0,3,6,...}

- `A_1` is adjacent with all other vertices.
- `A_2` is adjacent with all other vertices.
- `A_3` is adjacent with everything but `A_4`.
- `A_4` is adjacent with everything but `A_3`.
- `A_5` is adjacent with all other vertices.


### Section 2 - Graph Terminology and Special Types of Graphs
#### Basic Terminology
- Two vertices `u` and `v` in an undirected graph G are called **adjacent** (or neighbors) in `G` if `u` and `v` are endpoints of an edge `e` of `G`. 
- An edge `e` is called **incident** with the vertices `u` and `v` and `e` is said to connect `u` and `v`.
- The set of all neighbors of a vertex v of `G = (V,E)`, denoted by `N(v)`, is called the **neighborhood** of `v`. If `A` is a subset of `V`, we denote by `N(A)` the set of all vertices in `G` that are adjacent to at least one vertex in `A`. So, `N(A) = U ∈ A N(v)`.
- The *degree of a vertex in an undirected graph* is the number of edges incident with it, except that a loop at a vertex contributes twice to the degree of that vertex. The degree of the vertex `v` is denoted by `deg(v)`.
- A vertex of degree zero is called **isolated**.
- A vertex is **pendant** if and only if it has degree one.

#### Some Special Simple Graphs
- **Complete graphs** are simple graphs that contain exactly one edge between each pair of distinct vertices.
- **Non-complete** graphs have at least one pair of distinct vertices not connected by an edge.
- **Cycles** consist of `n` vertices and `n` edges between distinct vertices. 
- **Wheels** are where cycles receive a center which each vertices connects to.
- **N-dimensional hypercubes**, or n-cube, denoted by `Q_n`, are a graph that has vertices representing the `2^n` bit strings of length `n`. Two vertices are adjacent if and only if the bit strings that they represent differ in exactly one bit position.
 
#### Bipartite Graphs
- A simple graph G is called **bipartite** if its vertex set `V` can be partitioned into two disjoint sets `V_1` and `V_2` such that every edge in the graph connects a vertex in `V_1` and a vertex in `V_2` (so that no edge in `G` connects either two vertices in `V_1` or two vertices in `V_2`). When this condition holds, we call the pair `(V_1, V_2)` a bipartition of the vertex set `V` of `G`.
- A **complete bipartite graph** `K_{m,n}` is a graph that has its vertex set partitioned into two subsets of `m` and `n` vertices, respectively with an edge between two vertices if and only if one vertex is in the first subset and the other vertex is in the second subset.

#### Exercises
9\. 

- `deg+(a) = 1`
- `deg-(a) = 6`
- `deg+(b) = 5`
- `deg-(b) = 1`
- `deg+(c) = 5`
- `deg-(c) = 2`
- `deg+(d) = 2`
- `deg-(d) = 4`
- `deg+(e) = 0`
- `deg-(e) = 0`

### Section 3 - Representing Graphs and Graph Isomorphism
#### Introduction
- When two graphs have exactly the same form, in the sense that there is a one-to-one correspondence between their vertex sets that preserves edges, they are called **isomorphic**.

#### Representing Graphs
- One way to represent a graph is with an **adjacency list**, which lists vertices on one side and all their adjacent vertices on the other.
- By listing vertices with their corresponding terminal vertices, it's possible to construct a **directed adjacency list**.

#### Adjacency Matrices
- It's also possible to define a graph using a matrices, which is convenient for complex graphs and computation.
- If `A_{ij}` = 1, then there is an edge between them.
- Else `A_{ij}` = 0, and there is no edge between them.
- When a graph does not contain many edges, it is **sparse**.
- Conversely, when a graph does contain many edges, it is **dense**.
- So each column represents a vertices, and each 1 in a given row represents the other vertices it is connected to.

#### Incidence Matrices
- `m_{ij} = is edge e_j incident with v_i ? 1 : 0`
- What this means is that each column with have two ones in it, and each row represents a vertices. 

#### Isomorphism of Graphs
- The simple graphs `G1 = (V1, E1)` and `G2 = (V2, E2)` are isomorphic if there exists a one- to-one and onto function f from `V_1` to `V_2` with the property that a and b are adjacent in G1 if and only if `f(a)` and `f(b)` are adjacent in `G_2`, for all `a` and `b` in `V_1`. Such a function `f` is called an isomorphism. Two simple graphs that are not isomorphic are called non-isomorphic.
- The bipartite graph `G = (V , E)` with bipartition `(V_1,V_2)` has a complete matching from `V_1` to `V_2` if and only if `|N(A)| ≥ |A|` for all subsets `A` of `V_1`.

#### Exercises
Determine wether the given graphs are isomorphic.
- 61
	+ `v_1 <=> u_4`
		* `v_1` is the sink for `v_4` and `v_2`
		* `u_4` is the sink for `u_2	` and `u_3`
	+ `v_2 <=> u_3`
		* `v_2` is the source for `v_1`, `v_3, and `v_4`
		* `u_3` is the source for `
		* `v_2` is the sink for `v_3`
	+ `v_3 <=> u_1`
	+ `v_4 <=> u_2`


### Recitation - November 9th, 2012
- A graph is an ordered pair with two elements, a set of vertices and a collection of edges.	
	* You cannot have an empty set of vertices.
	* Every edge in the set of edges
- If a vertices has no edges, it is isolated.
- A simple graph is undirected, no multiple edges, no loops.
- A loop is an edge that is incident with only one vertices.
- A pseudo graph can have loops and multiple edges.
- A directed graph has tuples instead of sets for the definition of an edge, so order matters.
- When two vertices are adjacent, they share an edge.
	* Adjacent *with* means that a vertices points to another vertices.
	* Adjacent *from* means that a vertices is pointed to from another vertices.
- Incident means an edge has two vertices.

### Lecture - November 15th, 2012
#### Questions
- Can a directed simple graph have two vertices connected by two edges of opposition directionality?
- Is there a way to prove isomorphism or can you simply disprove isomorphism to the best of your ability?
	* When putting two graphs into an matrices to prove isomorphism, what constitutes isomorphic? (See 57 on page 677)
- How can you represent a graph with direction in matrix form?
`{b,c,e,f}, {a,b,g}, {a,d,g}, {d,e,g}, {b,e,g}`

## Chapter 11 - Trees
### Section 2 - Application of Trees
#### Introduction
- Three problems:
	1. How should items in a list be stored so that an item can be easily located?
	2. What series of decisions should be made to find an object with a certain property in a collection of objects of a certain type? 
	3. How should a set of characters be efficiently coded by bit strings?

#### Binary Search Trees
- a **binary search tree** a binary tree in which:
	1. each child of a vertex is designated as a right or left child, 
	2. no vertex has more than one right child or left child, and 
	3. each vertex is labeled with a key, which is one of the items.
- Vertices are assigned keys so that the key of a vertex is both larger than the keys of all vertices in its left subtree and smaller than the keys of all vertices in its right subtree.

#### Decision Trees
- a **decision tree** is a rooted tree in which each internal vertex corresponds to a decision, with a subtree at these vertices for each possible outcome of the decision.

#### Prefix Codes
- **Prefix codes** are one way to ensure that no bit string corresponds to more than one sequence of letters is to encode letters so that the bit string for a letter never occurs as the first part of the bit string for another letter.

##### Huffman Coding
- **Huffman coding** is an algorithm that takes as input the frequencies (which are the probabilities of occurrences) of symbols in a string and produces as output a prefix code that encodes the string using the fewest possible bits, among all possible binary prefix codes for these symbols.

#### Game Trees
- **Game trees** are trees that can be used to analyze certain types of games such as tic-tac-toe, nim, checkers, and chess. In each of these games, two players take turns making moves.
- The vertices of these trees represent the positions that a game can be in as it progresses; the edges represent legal moves between these positions.

#### Examples
##### Example 1
Form a binary search tree for the words mathematics, physics, geography, zoology, meteorology, geology, psychology, and chemistry (using alphabetical order).

									mathematics
									/					\
						geography					physics
						/				\				/					\
				chemistry	geology	meteorology	psychology
																					\
																				zoology
##### Example 2
Suppose there are seven coins, all with the same weight, and a counterfeit coin that weighs less than the others. How many weighings are necessary using a balance scale to determine which of the eight coins is the counterfeit one? Give an algorithm for finding this counterfeit coin.

1. Put 3 coins on one side of the scale and 3 coins on the other. There are three possibilities:
	1. The left weighs more than than the right, continue operations on the left.
	2. The right weighs more than the left, continue operations on the right.
	3. They are of equal weight. The unused coin is counterfeit. End.
2. Put one of the remaining three coins on the right and another on the left. There are three possibilities:
	1. The left weighs more than than the right, the left coin is counterfeit. End.
	2. The right weighs more than the left, the right coin is counterfeit. End.
	3. They are of equal weight. The unused coin is counterfeit. End.

##### Example 5
Use Huffman coding to encode the following symbols with the frequencies listed: `A: 0.08, B:0.10, C: 0.12, D: 0.15, E: 0.20, F: 0.35`. What is the average number of bits used to encode a character?

1. `A: 0.08, B:0.10, C: 0.12, D: 0.15, E: 0.20, F: 0.35`
	- Use `A` and `B` to form a tree of probability `.18`.
2. `AB:0.18, C: 0.12, D: 0.15, E: 0.20, F: 0.35`
	- Use `C` and `D` to form a tree of probability `.27`.
3. `AB:0.18, CD:.27, E: 0.20, F: 0.35`
	- Use `AB` and `E` to form a tree of probability `.38`.
4. `E,AB:0.38, CD:.27, F: 0.35`
	- Use `CD` and `F` to form a tree of probability `.62`
5. `E, AB:0.38, F, CD:.62`

Therefore, `A = 111 (3)`, `B = 110 (3)`, `C = 011 (3)`, `D = 010 (3)`, `E = 10 (2)`, and `F = 00 (2)`, and the average encoding length will be those numbers probabilities multiplied by their encoding length (in parentheses).

`(3)*(.08) + (3)*(.10) + (3)*(.12) + (3)*(.15) + (2)*(.20) + (2)*(.35) = 2.45`
#### Exercises
1. Build a binary search tree for the words banana, peach, apple, pear, coconut, mango, and papaya using alphabetical order.
9. How many weighings of a balance scale are needed to find a counterfeit coin among 12 coins if the counterfeit coin is lighter than the others? Describe an algorithm to find the lighter coin using this number of weighings.
23. Use Huffman coding to encode these symbols with given frequencies: `a: 0.20, b: 0.10, c: 0.15, d: 0.25, e: 0.30`. What is the average number of bits required to encode a character?

### Section 3 - Tree Traversal
#### Traversal Algorithms
- Procedures for systematically visiting every vertex of an ordered rooted tree are called **traversal algorithms**. 
- We will describe three of the most commonly used such algorithms, 
	1. **Preorder traversal**: Visit root, visit subtrees left to right. *(VLR)*
		+ Let `T` be an ordered rooted tree with root `r`. If `T` consists only of `r`, then `r` is the preorder traversal of `T`. Otherwise, suppose that `T_1, T_2, … , T_n` are the subtrees at `r` from left to right in `T`. The preorder traversal begins by visiting `r`. It continues by traversing `T_1` in preorder, then `T_2` in preorder, and so on, until `T_n` is traversed in preorder.
		+ Example from standard tree: `a, b, e, j, k, n, o, p, f, c, d, g, l, m, h, i`
		+ Algorithm:

				procedure preorder(T : ordered rooted tree) 
					r :=root of T
					list r
					for each child c of r from left to right
						T (c) := subtree with c as its root preorder(T (c))
	2. **Inorder traversal**: Visit left subtree, visit root, visit right subtree. *(LVR)*
		+ Let `T` be an ordered rooted tree with root `r`. If `T` consists only of `r`, then r is the inorder traversal of `T`. Otherwise, suppose that `T_1, T_2, … , T_n` are the subtrees at r from left to right. The inorder traversal begins by traversing `T_1` in inorder, then visiting `r`. It continues by traversing T_2 in inorder, then T_3 in inorder, … , and finally `T_n` in inorder.
		+ Example from standard tree: `j, e, n, k, o, p, b, f, a, c, l, g, m, d, h, i`
		+ Algorithm:

				procedure inorder(T : ordered rooted tree) 
				r := root of T
				if r is a leaf, then list r
				else
					l := first child of r from left to right
					T (l) := subtree with l as its root inorder(T (l))	
					list r
					for (each child c of r except for l from left to right)
						T(c) := subtree with c as its root
						inorder(T (c))
	3. **Postorder traversal**: Visit subtrees left to right, visit root. *(LRV)*
		+ Let `T` be an ordered rooted tree with root `r`. If `T` consists only of `r`, then r is the postorder traversal of `T`. Otherwise, suppose that `T_1, T_2, … , T_n` are the subtrees at `r` from left to right. The postorder traversal begins by traversing `T_1` in postorder, then `T_2` in postorder, … , then `T_n` in postorder, and ends by visiting `r`.
		+ Example from standard tree: `j, n, o, p, k, e, f, b, c, l, m, g, h, i, d, a`
		+ Algorithm:

				procedure postorder(T : ordered rooted tree) 
				r :=rootofT
				for each child c of r from left to right
					T (c) := subtree with c as its root
					postorder(T (c)) 
				list r

#### Infix, Prefix, and Postfix Notation
- To make such expressions unambiguous it is necessary to include parentheses in the *inorder traversal* whenever we encounter an operation. The fully parenthesized expression obtained in this way is said to be in **infix form**.
- We obtain the **postfix form** of an expression by traversing its binary tree in *postorder*.

#### Examples
##### Example 5
What is the ordered rooted tree that represents the expression `((x + y)↑2) + ((x − 4)/3)`?

##### Examples 6
What is the prefix form for `((x + y) ↑ 2) + ((x − 4)/3)`?

- To solve this problem, you would perform a preorder traversal on the tree representation of this expression.

##### Example 7
What is the value of the prefix expression `+−∗235/↑234`?

- `+−∗235/↑234`
- `+−∗235/84`
- `+−∗2352`
- `+−652`
- `+12`
- `3`

##### Example 8
What is the postfix form of the expression `((x + y) ↑ 2) + ((x − 4)/3)`?

- To solve this problem, you would perform a postorder traversal on the tree representation of the expression.

##### Example 9
What is the value of the postfix expression `7 2 3 ∗ − 4 ↑ 9 3/+`?

- `7 2 3 ∗ − 4 ↑ 9 3 / +`
- `7 6 − 4 ↑ 9 3 / +`
- `1 4 ↑ 9 3 / +`
- `1 9 3 / +`
- `1 3 +`
- `4`

##### Example 10
Find the ordered rooted tree representing the compound proposition `(¬(p ∧ q)) ↔ (¬p ∨ ¬q)`. Then use this rooted tree to find the prefix, postfix, and infix forms of this expression.

#### Exercises
22. Draw the ordered rooted tree corresponding to each of these arithmetic expressions written in prefix notation. Then write each expression using infix notation.
	- `+∗+−53214`
	- `↑+23−51`
	- `∗/93+∗24−76`
23. What is the value of each of these prefix expressions?
		- `−∗2/843`
	- `↑−∗33∗425`
		- `+−↑32↑23/6−42` 
	- `∗+3+3↑3+333`
24. What is the value of each of these postfix expressions?
	- `521−−314++∗`
	- `93/5+72−∗`
		- `32∗2↑53−84/∗−`

### Recitation and Lecture, November 20th, 2012
#### Huffman Coding
- So we have some text we want to consider and we want to encode.
- How do we store data? It's all in binary.
- How can we store the Gettysburg address using the minimum amount of bits possible?
- How do we compress the data?
- For this text specifically, if we convert all lower case to upper case, and we ignore the special symbols, but we do have space and break, and comma, dash, period, question mark, all characters. The numbers of those are as follows, <insert here>
- If we want to use binary to represent this address, what is the first way we might do that?
	+ We may be tempted to use ASCII or UTF8
	+ If we encoded the Gettysburg address using 8 bits, it would result in 11856 total bits, almost twelve thousand.
- What are some ways we can do better than this?
	+ We could come up with unique coding attempt using solely 5 bits, as there are 32 unique characters in the Gettysburg address.
		* This result in 7410.
	+ We could take the most frequent characters and give them shorter codes.
- In order to find out the average over an entire document, we have to do a weighted sum, ex, we have 282 three bit, 165 three bit … etc.

#### Quiz 8a
1. For each of the following trees, write "True" if it is a binary search tree.
	- A: **False**

							A
						/		\
						B		C
					/	 \	/	\
					D		E	F	 G
	- B: **False**

							A
						/		\
						B		 E
					/	 \	/	\
					C		D	F	 G
	- C: **True**

							D
						/		\
						B		 F
					/	 \	/	\
					A		C	F	 G
	- D: **True**

				A
					\
						B
							\
								C
									\
										D
											\
												E
													\
														F
															\
																G

2. Given the following codes, write True is it is a prefix code: (To solve this, a whole code has to be the prefix to an whole other code)
	- A: `a: 11, e: 00, t: 10, s: 01`, **True**
	- B: `a: 0, e: 1, t:01, s: 001`, **False**
	- C: `a: 101, e: 11, t: 001, s: 001, n: 010`, **True**
	- D: `a: 010, e:11, t:011, s:1011, n:1001, i:10101` **True**
3. For each of the following codes, compute the average number of bits we'll use per character.
	- A: bits: **2**, Huffman? **False**
		+ code: `a: 10, b: 11`
		+ frequency: `a: 0.1, b: 0.9`
	- B: bits: **`(.2)(2)+(.3)(2)+(.5)(1)`** Huffman? **True**
		+ code: `a:10, b: 11, c: 0`
		+ frequency: `a:.2, b:.3, c:.5`
	- C: bits:

## Chapter 13 - Modeling Computation
### Section 1 - Languages and Grammars
#### Introduction
- **Syntax** is the form of a sentence.
- **Semantics** is the meaning of a sentence.
- The syntax of a **natural language** is extremely complex.
- The syntax of a **formal language** is specified by a well-defined set of rules.
- Syntax in English:
	1. a **sentence** is made up of a noun phrase followed by a verb phrase; 
	2. a **noun phrase** is made up of an article followed by an adjective followed by a noun, 
	3. a **noun phrase** is made up of an article followed by a noun; 
	4. a **verb phrase** is made up of a verb followed by an adverb, or 
	5. a **verb phrase** is made up of a verb; 
	6. an **article** is a, or 
	7. an **article** is the; 
	8. an **adjective** is large, or 
	9. an **adjective** is hungry; 
	10. a **noun** is rabbit, or 
	11. a **noun** is mathematician; 
	12. a **verb** is eats, or 
	13. a **verb** is hops; 
	14. an **adverb** is quickly, or 15. an **adverb** is wildly.
- You can use this to build valid sentences 
	- **sentence** - **noun phrase verb phrase** 
	- **article adjective noun verb phrase article adjective noun verb adverb the adjective noun verb adverb** 
	- *the large* **noun verb adverb** 
	- *the large rabbit* **verb adverb** 
	- *the large rabbit hops* **adverb** 
	- *the large rabbit hops quickly*

#### Phrase-Structure Grammars
##### Definition 1 - Vocabulary and Word
- A *vocabulary* (or *alphabet*) V is a finite, nonempty set of elements called symbols. A *word* (or *sentence*) over `V` is a string of finite length of elements of `V`. The *empty string* or *null string*, denoted by `λ`, is the string containing no symbols. The set of all words over `V` is denoted by `V∗`. A language over `V` is a subset of `V∗`.
- A *grammar* provides a set of symbols of various types and a set of rules for producing *words*. More precisely, a grammar has a **vocabulary** `V`, which is a set of symbols used to derive members of the language.
- Some of the elements of the *vocabulary* cannot be replaced by other symbols. These are called **terminals**, and the other members of the *vocabulary*, which can be replaced by other symbols, are called **nonterminals**.
- There is a special member of the vocabulary called the **start symbol**, denoted by `S`, which is the element of the vocabulary that we always begin with.

##### Definition 2 - Terminal Symbols
- A *phrase-structure grammar* `G = (V, T, S, P)` consists of a vocabulary `V`, a subset `T` of `V` consisting of **terminal symbols**, a start symbol `S` from `V`, and a finite set of productions `P`. The set `V − T` is denoted by `N`. Elements of `N` are called **nonterminal symbols**. Every production in `P` must contain at least one nonterminal on its left side.

###### Example 1
- Let `G = (V,T,S,P)`, where `V = {a,b,A,B,S}`, `T = {a,b}`, `S` is the **start symbol**, and `P = {S → ABa, A → BB, B → ab, AB → b}`. `G` is an example of a **phrase-structure grammar**.

##### Definition 3 - 
- Let `G = (V , T , S, P)` be a phrase-structure grammar. Let `w_0 = l*z_0*r` (that is, the concatenation of `l,z_0`, and `r`) and `w_1 = l*z_1*r` be strings over `V`. If `z_0 → z_1` is a production of `G`, we say that `w_1` is directly derivable from `w_0` and we write `w0 ⇒ w1`. If `w_0, w_1, …, w_n` are strings over `V` such that `w_0 ⇒ w_1, w_1 ⇒ w_2,…, w_n−1 ⇒ w_n`, then we say that `w_n` is derivable from `w_0`, and we write `w_0 ⇒∗ w_n`. The sequence of steps used to obtain `w_n` from `w_0` is called a derivation.

###### Example 2
- The string `Aaba` is directly derivable from `ABa` in the grammar in Example 1 because `B → ab` is a production in the grammar. The string `abababa` is derivable from `ABa` because `ABa ⇒ Aaba ⇒ BBaba ⇒ Bababa ⇒ abababa`, using the productions `B → ab, A → BB, B → ab,` and `B → ab` in succession.

##### Definition 4 
- Let `G = (V , T , S, P)` be a phrase-structure grammar. The **language generated** by `G` (or the language of G), denoted by `L(G)`, is the set of all strings of terminals that are derivable from the starting state S. In other words, `L(G)={w∈T∗|S⇒∗ w}`.

###### Example 3
- Let `G` be the grammar with vocabulary `V = {S, A, a, b}`, set of terminals `T = {a, b}`, starting symbol S, and productions `P = {S → aA, S → b, A → aa}`. What is `L(G)`, the **language of this grammar**?
	+ There are odd numbers of `a`s greater than 1 terminated by a `b`.
	+ `L(G) = {b, aaa}`

###### Example 4
- Let `G` be the grammar with vocabulary `V = {S, 0, 1}`, set of terminals `T = {0, 1}`, starting symbol `S`, and productions `P = {S → 11S, S → 0}`. What is `L(G)`, the **language of this grammar**?
	+ `L(G) = {110, 11110, 1111110, … }

###### Example 5
- Give a **phrase-structure grammar** that generates the set `{0^n1*n | n = 0, 1, 2, . . . }`.

###### Example 6
- Find a phrase-structure grammar to generate the set {0m1n | m and n are nonnegative integers}.

###### Example 7
- One grammar that generates the set `{0n1n2n | n = 0,1,2,3,…}` is `G = (V,T,S,P)` with `V = {0,1,2,S,A,B,C}`; `T = {0,1,2}`; starting state `S`; and production `S → C`, `C → 0CAB`, `S → λ`, `BA → AB`, `0A → 01`, `1A → 11`, `1B → 12`, and `2B → 22`.

#### Types of Phrase-Structure Grammars
- A **type 0 grammar** has no restrictions on its productions. 
- A **type 1 grammar** can have productions of the form `w1 → w2`, where `w_1 = lAr` and `w_2 = lwr`, where `A` is a nonterminal symbol, `l` and `r` are strings of zero or more terminal or nonterminal symbols, and `w` is a nonempty string of terminal or nonterminal symbols.
	+ A language generated by a type 1 grammar is called a **context-sensitive language**.
- A **type 2 grammar** can have productions only of the form `w1 → w2`, where `w_1` is a single symbol that is not a terminal symbol.
	+ Type 2 grammars are called **context-free grammars** because a *nonterminal symbol* that is the left side of a *production* can be replaced in a string whenever it occurs, no matter what else is in the string. 
	+ A language generated by a type 2 grammar is called a **context-free language**. 
- A **type 3 grammar** can have productions only of the form `w1 → w_2` with `w_1 = A` and either `w_2 = aB` or `w_2 = a`, where A and B are nonterminal symbols and a is a terminal symbol, or with `w1 =S` and `w2 = λ`.
	+ Type 3 grammars are also called **regular grammars**.
- The other way that context-sensitive grammars are defined is by specifying that all productions are **noncontracting**. A grammar with this property is called **noncontracting** or **monotonic**.

###### Example 8
- From Example 6 we know that `{0^m 1^n | m,n = 0,1,2,…}` is are regular language,because it can be generated by a regular grammar, namely, the grammar `G2` in Example 6.

###### Example 9
- It follows from Example 5 that `{0^n 1^n | n = 0, 1, 2, ... }` is a **context-free language**, because the productions in this grammar are S → 0S1 and S → λ.

###### Example 10
- The set `{0^n 1^n 2^n | n = 0, 1, 2, ... }` is a **context-sensitive language**, because it can be generated by a **type 1 grammar**, as Example 7 shows, but not by any type 2 language.

##### Types of Grammars

- **Type 0**: No restrictions
- **Type 1**: `w_1 = lAr` and `w_2 = lwr`, where `A ∈ N, l, r, w ∈ (N ∪ T )∗` and `w  ̸= λ`;
		+ or `w_1 = S` and `w_2 = λ` as long as `S` is not on the right-hand side of another production 
- **Type 2**: `w_1 = A`, where `A` is a nonterminal symbol
- **Type 3**: `w_1 = A` and `w_2 = aB` or `w_2 = a`, where `A ∈ N, B ∈ N`, and `a ∈ T` ; or `w_1 = S` and `w_2 = λ`

#### Derivation Trees
- A derivation in the language generated by a **context-free grammar** can be represented graphically using an **ordered rooted tree**, called a **derivation**, or **parse tree**.
	+ If the production `A → w` arises in the derivation, where `w` is a word, the vertex that represents `A` has as children vertices that represent each symbol in `w`, in order from left to right.

##### Example 11
- Construct a **derivation tree** for the derivation of the "hungry rabbit eats quickly", given in the introduction of this section.

##### Example 12
- Determine whether the word cbab belongs to the language generated by the grammar `G = (V,T,S,P)`, where `V = {a,b,c,A,B,C,S}`, `T = {a,b,c}`, `S` is the starting symbol, and the productions are:
	+ `S → AB` 
	+ `A → Ca`
	+ `B → Ba`
	+ `B → Cb`
	+ `B → b`
	+ `C → cb`
	+ `C → b`

#### Backus–Naur Form
- The Backus–Naur form is used to specify the syntactic rules of many computer languages, including Java. 
	+ The *productions* in a *type 2 grammar* have a single *nonterminal symbol* as their left-hand side. 
	+ Instead of listing all the *productions* separately, we can combine all those with the same *nonterminal symbol* on the left-hand side into one statement. 
	+ Instead of using the symbol `→` in a production, we use the symbol `::=`. 
	+ We enclose all *nonterminal symbols* in brackets, `⟨⟩`, and we list all the right-hand sides of *productions* in the same statement, separating them by bars. 
- For instance, the productions `A → Aa`, `A → a`, and `A → AB` can be combined into `⟨A⟩ ::= ⟨A⟩a | a | ⟨A⟩⟨B⟩`.

##### Example 14
- What is the Backus–Naur form of the grammar for the subset of English described in the introduction to this section?

#### Exercises
1. Use the set of productions to show that each of these sen- tences is a valid sentence. 
	+ the happy hare runs 
	+ the sleepy tortoise runs quickly 
	+ the tortoise passes the hare 
	+ the sleepy hare passes the happy tortoise
3. Show that the hare runs "the sleepy tortoise is not a valid" sentence.
5. Let `G = (V , T , S, P)` be the phrase-structure grammar with `V = {0,1,A,B,S}, T = {0,1}`, and set of productions `P` consisting of `S → 0A`, `S → 1A`, `A → 0B`, `B → 1A`, `B → 1`. 
	+ Show that 10101 belongs to the language generated by G. 
	+ Show that 10110 does not belong to the language generated by G. 
	+ What is the language generated by G?
7. Construct a derivation of `0313` using the grammar given in Example 5.
13. Find a phrase-structure grammar for each of these languages. 
	+ the set consisting of the bit strings `0`,`1`, and `11` 
	+ the set of bit strings containing only `1`s 
	+ the set of bit strings that start with `0` and end with `1` 
	+ the set of bit strings that consist of a `0` followed by an even number of `1`s
17. Construct phrase-structure grammars to generate each of these sets. 
	+ `{0n |n≥0} `
	+ `{1n0|n≥0} `
	+ `{(000)n|n≥0}`

#### Recitation
- If you have some sentence `S`, then you can split it into a noun `N` and a verb `V`, which can be variable.
- Where a graph is a set of vertices and a set of edges, a grammar  is composed of:
	1. `V`, the **vocabulary**, which is all the symbols possible;
	2. `T`, the **terminals**, which is a subset of `V`, and it is the symbols that are not used to generate new symbols, this means that they do not contain any symbols which can be translated into any other symbols;
		+ Lower case letters denote terminals.
		+ Upper case letters denote non-terminals, and they are defined by `N = V - T`.
	3. `S`, the **start symbol**, which is a member of the vocabulary, and where you start from; and
	4. `P`, the **productions**, which are what you can derive from symbols or set of symbols.

##### Chomsky Hierarchy
+ If we have some production `W_1 → W_2` and it is **type 0**, it is said to have no restrictions
	* recursively enumerable
	+ If it is of **type 1**, we have to have `w_1 = lAr` where `l` is a possibly empty string, `A` is nonterminal, and `r` is a possibly empty string, and `w_2 = lwr` where `w` is a nonempty string.
		* except when `w_1 = s` and `w_2 = \Alpha` as long as `S` is never `S` on right side of `S -> aS`
		* type 1 is context senstive
	+ If it said to be of **type 3**, `w_1 = A` and `w_2 = aB` or `w_2  = a`
		* regular

##### Examples
4. Let `G = (V, T, S, P)` be the phrase-structure grammar with `V = {0, 1, A, S}`, `T = {0, 1}`, and a set of productions `P` consisting of `S → 1S`, `S → 00A`, `A → 0A`, and `A → 0`.
	+ Show that 111000 belongs to the language generated by `G`.
	+ Show that 11001 does not belong to the language generated by `G`.
	+ What is the language generated by `G`?

19. Let `V = {S,A,B,a,b}` and `T = {a,b}`. Determine whether `G = (V,T,S,P)` is a type 0 grammar but not a type 1 grammar, a type 1 grammar but not a type 2 grammar, or a type 2 grammar but not a type 3 grammar if `P` , the set of productions, is
	+ `S→aAB, A→Bb, B→λ` - this is type 2 because each of these products start with a non-terminal
	+ `S → aA, A → a, A → b` - this is type 3 because all satisfy the very restrictive rules of beginning with a terminal and ending with either nothing or a non-terminal
	+ `S → ABa, AB → a`
	+ `S→ABA, A→aB, B→ab` 
	+ `S→bA, A→B, B→a`
	+ `S→aA, aA→B, B→aA,A→b` 
	+ `S →bA, A→b, S →λ`
	+ `S → AB, B → aAb, aAb → b`
	+ `S → aA, A → bB, B → b, B → λ`
	+ `S → A, A → B, B → λ`
