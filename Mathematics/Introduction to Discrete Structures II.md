# Introduction to Discrete Structures II <small>with Professor David Cash</small>

## Description 

Provides the background in combinatorics and probability theory required in design and analysis of algorithms, in system analysis, and in other areas of computer science.

- Topics:
    + Counting: Binomial Coefficients, Permutations, Combinations, Partitions.
    + Recurrence Relations and Generating Functions.
    + Discrete Probability:
        * Events and Random Variables;
        * Conditional Probability, Independence;
        * Expectation, Variance, Standard Deviation;
    + Binomial, Poisson and Geometric Distributions; 
    + law of large numbers.
    + Some Topics from Graph Theory: 
        * Paths,  
        * Components,  
        * Connectivity,  
        * Euler Paths,  
        * Hamiltonian Paths,  
        * Planar Graphs,  
        * Trees.

## Syllabus

### Course Overview

This course is an introduction to *probability* and *combinatorics*, including their basic mathematical foundations as well as several non-trivial applications of each. The first topic explores how to think about *random processes* in a rigorous and sensical way, and second is about techniques for *counting* the number of objects fitting a given description. As we will see, the techniques involved in both topics are strongly related.   

Roughly, we expect to cover the following list of topics. Lecture summaries will be posted at the bottom of this page.

- Review of prerequisites, set theory, countability
- Random experiments, sample spaces, events, probability measures
- Conditional probability, Bayes' Theorem, Independence
- Combinatorics and Counting
- Recurrences, Generating Functions
- Random Variables
- Bernoulli Trials
- Expectation, Variance
- Markov Chains
- Applications of Probability and Combinatorics

### General Information

* Instructor: [David Cash](david.cash@cs.rutgers.edu)
* [Course website](http://www.research.rutgers.edu/~dc789/206-spring-13/index.html)
* Recommended textbooks:
	* S. Ross, *A First Course in Probability, 8th Edition*
	* H. Rosen, *Discrete Mathematics and its Applications, 7th edition*
* Lecture meetings: Monday and Wednesday 5:00pm -- 6:20pm in Hill 116 
* Recitations:
	* Section 1: Monday 6:55pm -- 7:50pm in SEC 220
	* Section 2: Wednesday 6:55pm -- 7:50pm in ARC 110
	* Section 3: Monday 8:25pm -- 9:20pm in Hill 120 
* Instructor office hours: Tuesday 1:30pm-3:00pm in Hill 411 and by appointment 
* Teaching assistant: TBA (TAB@cs.rutgers.edu) 
* Teaching assistant office hours: TBA in TBA and by appointment 

### Assignments and Grading

Homework will be assigned roughly every 1.5 weeks. There will be one in-class midterm and one final exam. Final grades will be an average of homework grades (30%), midterm grades (30%), and final exam grades (40%).

## January 23rd, 2012 - Lecture: Introduction

### Topics

* Review of sets and induction. 
* Samples spaces and events.

### Introduction

- This title of this class is funny because it tells you nothing about it.
- What this class is really about is **discrete probability** and **combinatorics**.
	+ Discrete means "not continuous."
	+ Probability means about change and percentage.
	+ Combinatorics is the study of combining things.
	+ More specifically, it is the study of counting the number of discrete objects fitting some description.
- Probability in computer science
	+ Random number generator (RNG)
	+ Average case algorithms
	+ Information security and cryptography
	+ Networking, TCP/IP

### Formalizaing Probability
- A set is a collection of objects. Ex:
	- \\(S = {a, b, c} \\)
	- \\( \mathbb{N} = 1, 2, 3, … \\) (natural numbers)
	- \\( \mathbb{Z} = {…, -2, -1, 0, 1, 2, …} \\) (integers)
- Notation:
	+ \\(\emptyset = {} \\)
	+ Write ` {x |` "statement about `x}`" to mean all `x` satisfying statement.
- Relations between sets
	+ `A` and `B` are sets.
	+ \\(A  \subseteq B \\) means "`A` is a subset of `B`"
	+ \\(B  \subseteq A \\) means "`A` is a superset of `B`"
- Operations on sets
	+ \\( A \cup B \\) means "union of `A` and `B`"
	+ \\( A \cap B \\) means "intersection of `A` and `B`"
	+ \\( A \setminus B \\) means "set difference of `A` and `B`" which means everything in `A` that is not in `B`
	+ When a "universe" is understood, we can define \\(A^{c}\\) as the "complement" of `A`
- Set identities
 \\[ A \cup (B \cap C) = \\]
\\[(A \cup B) \cap (A \cup C)\\]
\\[A \cap (B\cup C) = (A\cap B) \cup (A \cap C)\\]
	+ Prove: \\((A \cup B)^{c} = A^c \cap B^c \\) 
		1. Show: \\((A \cup B)^{c} \subseteq A^c \cap B^c \\)
		2. Show: \\(A^c \cap B^c  \subseteq (A \cup B)^{c}\\)
	+ A good way to remember these is to use Venn diagrams.
- DeMorgan's laws
- Proofs by Induction
	+ Let's say you want to prove a statement for all natural numbers `n`.
	+ For example, for all `n > 0`, \\(\sum_{i=0}^{n}2^i = 2^{n + 1}\\)
		* Call the statements \\(s_0, s_1, s_2, … \\)
		* Suppose it's not true for all of them.
		* Key obeservation: If they're not all true, then there is a smallest `i` such that \\(S_i\\) is false.
	+ A proof by induction works in 2 steps:
		1. Prove statement for first `n`
		2. Give a conditional proof, prove that for all `n`, if \\(S_{n-1}\\) is true, then \\(S_{n}\\)
- Countability
	+ A set `S` is countable if it is finite, or if it can be pun in one-to-one correspondence with the natural numbers.
- Sample space
	+ Fix a "sample space" that represents everything that could happen in our random experiment
	+ A sample space is always a set
	+ Examples of samples spaces
		1. Tossing a coin: \\( S = (H, T) = ({0, 1})\\)
		2. Tossing two coins: \\(S = ({HH, HT, TH, TT}) \\)
		3. Rolling a die: \\( S = ({1, 2, 3, 4, 5, 6})\\)
		4. Rolling 2 dice: \\( S = ((i, j) | \\) i, j in\\( (1,2,3,4,5,6))\\)
		
## January 23rd, 2013 - Reading

### 2.1 Introduction

> In this chapter, we introduce the concept of the probability of an event and then show how probabilities can be computed in certain situations. As a preliminary, however, we need the concept of the sample space and the events of an experiment.	

### 2.2 Sample Space and Events

- The set of all possible outcomes of an experiment is known as the **sample space** of the experiment and is denoted by S. Examples:
	1. The sex of a newborn child: S = {g, b}
	2. Horse race with seven horses: S = {all 7! permutations of (1, 2, 3, 4, 5, 6, 7)}
	3. Flipping two coins: S = {(H, H), (H, T), (T, H), (T, T)}
	4. Tossing two dice: S = {(i, j): i, j = 1, 2, 3, 4, 5, 6}
- Any subset E of the sample space is known as an **event**. For the previous examples,
	1. E = {g} would be having a girl.
	2. E = {all outcomes in S beginning with 3} would be 3 winning the race.
	3. E = {(H, H), (H, T)} would be an event where you get heads first.
	4. E = {(1, 6), (2, 5), (3, 4), (4, 3), (5, 2), (6, 1)} would be an event where the sum of the two rolls is seven.
- A **union** of any two events E and F results in an event with all outcomes in both E and F.
- An **intersection** of any two events E and F results in a event with only those outcomes in both E and F.
- If E and F share no outcomes, making their intersection the empty set (denoted by \\(\emptyset\\), they are said to be **mutually exclusive**.
- The complement of E is defined as all events not in E that are in the sample space, denoted by \\( E^c \\).

## January 28th, 2013 - Lecture: Probability Measures

### Announcements

- Recitation starts this week.
- Homework 1 will be out tonight and due in a week.

### Topics

* Operations on events. 
* Abstract definition of probability measure. 
* Equivalent definition for countable sample spaces. 
* Basic consequences of the definition.

### Probability

- Sample space = any set
- "Event" = an subset of the sample space
- Fix a sample space `S`
- Take any events \\( E \subseteq S, E_2 S \\)
- Consider the set \\( E_1 \cup E_2 \subseteq S \\)
- Example: Flip two coins
	+ \\( S = HH, HT, TH, TT \\)
	+ \\( E_1 = HT, HH \\)
	+ \\( E_2 = TH, HH \\)
	+ \\( E_1 \cup E_2 =  HT, HH, TH \\) = "heads came up", "either heads came up on the 1st or 2nd toss"
	+ \\( E_1 \cap E_2 = HH \\)
- Example: Rolling a die
	+ \\( E_1 = \\) "die was rolled" = {1, 3, 5} 
	+ \\( E_2 = \\) "die roll was divisible by 3" = {3, 6}
	+ \\( E_1 \cap E_2 = 3\\)
- Note: If \\(E_1 =  \emptyset \\) and \\( E_2\\) is any event, then \\( E_1, E_2\\) are mutually exclusive.
- Complement: If E is an event, then so is \\( E^c \subseteq s \\) means "not E" or "E didn't happen."
	+ For the example of the two coins,
		* E = "1st coin was heads" means that \\( E^c = TH, TT \\)
- If \\( E_1 \subseteq E_2 \\), then what can we say?
	+ Proposal: If E1 happened then E2 also happened.
	+ Example: two dice:
		* First event: "a one was rolled" = {1}
		* Second event: "the dice summed to 3" = {(1,2),(2,1)}
		* The second event is a subset of the first event.

### Probability measures
- We've been talking about whether or not something happened, but we'll now move to how *likely* it is for something to happen.
- We want to assign to even event a number between zero and one represent how "likely" that event is.
	+ We are going to assume things about randomness and predictibility, we quickly get into philosophy otherwise.
- We want a function P that givens the probabilty P(E) for every E \\( \subseteq \\) S
- Example: A coin flip
	+ S = {H, T}
	+ P({H}) = 1/2
	+ P({T}) = 1/2
	+ P({H, T}) = 1
	+ P( \\( \emptyset \\) ) = 0
- Example: Tossing two coins
	+ S + {HH, HT, TH, TT}
	+ P({HH}) = 1/4 (and for HT, TH, ... )
	+ If E \\( \subseteq \\) S, P(E) = \\(\frac{|E|}{|S|} \\)
- Definition: A function P is a probability measure if it maps every event E \\( \subseteq \\) S to a number and satisfies the following three rules:
	1. For every E, O <= P(E) <= 1
	2. P(S) = 1
	3. Countable additivity
		- For every sequence \\( E_1, E_2, ... \\) of event, if the \\( E_i\\) are all mutually exlcusive, 
		so \\(E_i \cap E_j = \emptyset \\)
	 \\[ P\left(\bigcup_{i=1}^\infty E_i\right)=\sum_{i=1}^\infty P(E_i) \\]
- Claim: If P is a probabilty measure, then P(\\( \emptyset \\) ) = 0
	+ Proof: Take \\( E_1, E_2, ... \\) where \\( E_i = \emptyset \\) for every i. The sequence is mutually exclusive.
- When S is finite, we can replace (3) with the "finite additivity":
> \\( P \left(\bigcup_{i = 1}^n E_1 \right) = \sum_{i = 1}^n P(E_i) \\)
- Definition: If S is countable then we can say that P is discrete.
	+ Every sample set in this class will be countable.
- Claim: If P is discrete, then it is completely determined by its value on one-element sets.
- If you know that P({x}) for every \\( x \in S \\), then you know that P(E) for every E \\( \subseteq \\) S
- Write E = {\\( x_1, x_2, ... \\)} Let \\( E_i = x_i \\)
	+ The \\(E_i \\) are mutually exclusive.
	+ \\( \bigcup_{i = 1}^\infty E_1 = E \\)
	+ So by rule 3, 
	
## January 28th, 2013 - Reading

### 2.3 Axioms of Probability

- One way of defining probability is in relative frequency.
- For some event E in sample space S, we define n(E) to be the number of times in the first n repetitions of the experiment that the event E occurs. Therefore,
\\(P(E) = \lim_{x \to \infty}\frac{n{E}}{n} \\)
- While intuitive, how do we know that n(E)/n will converge to some constant limiting value that will be the same for each possible sequence of repetitions of the experiment?
	+ Proponents of this definitions say that this is an "axiom" of the system, an assumption.
	+ Critics say that this is too complicated an assumption.
- Would it not be more reasonable to assume a set of simpler and more self-evident axioms about probability and then attempt to prove that such a constant limiting frequency does in some sense exist?
- Axioms:
	1. \\( 0 \le P(E) \le 1 \\)
		+ The probability that the outcome of the experiment is an outcome in E is some number between 0 and 1
	2. \\( P(S) = 1 \\)
		+ The outcome will be a point in the sample space S
	3. \\( P\left(\bigcup_{i=1}^\infty E_i\right)=\sum_{i=1}^\infty P(E_i) \\)
		+ For any sequence of mutually exclusive events, the probability of at least one of these events occurring is just the sum of their respective probabilities.
		
### 2.4 Some simple propositions (through proposition 4.3)

- Proposition 4.1: 
\\[ P(E^c) = 1 − P(E) \\]
- Proposition 4.2: 
\\[ If E \subset F, then P(E) \le P(F). \\]
- Proposition 4.3: 
\\[ P(E \cup F) = P(E) + P(F) − P(EF) \\]

## January 28th, 2013 - Homework 1

1. Let \\(n\geq 2\\) and \\(A_1,\ldots,A_n\\) be sets in some universe S. In this problem we will give a proof by induction of the identity 
\\[ \left(\bigcap_{i=1}^n A_i\right)^c = \bigcup_{i=1}^n A_i^c. \\]
	1. (5 points)  State and prove the base case for an inductive proof, meaning that the identity is true when \\(n=2\\).
		1.  \\(\left(\bigcap_{i=1}^2 A_i\right)^c = \bigcup_{i=1}^2 A_i^c\\)
		2.  \\( \left(A_1 \bigcap A_2 \right)^c = A_1^c \bigcup A_2^c\\) is
			true by DeMorgan’s
	2. (5 points)  State and prove the inductive step, where one shows that the identity is true for general \\(n>2\\), assuming it is true for \\(n-1\\).
		1.  \\( \left(\bigcap_{i=1}^n A_i\right)^c = \bigcup_{i=1}^n A_i^c \\)
			assume true for n
		2.  \\( \left(\bigcap_{i=1}^{n - 1} A_i\right)^c = \bigcup_{i=1}^{n - 1} A_i^c \\)
			induction for n - 1
		3.  \\(\bigcup_{i = 1}^n A_i^c \cup A_{n + 1}^c = \\)
		\\[ \left( \bigcap_{i = 1}^n A_i \right) \cup A_{n + 1}^c\\]
		4.  \\(\left(\bigcap_{i=1}^n A_i\right)^c = \\)
		\\[ \left( \bigcap_{i = 1}^n A_i \right) \cup A_{n + 1}^c\\)

2. Give sample spaces that model the outcomes for the following experiments. You may use a regular expression or other formalisms that you find convenient. (2 points each)
	1. Rolling 3 dice.
\\[S = \lbrace (i,j,k) \: | \: i,j,k \in \\]
\\[\lbrace 1, 2, 3, 4, 5, 6 \rbrace \rbrace  \!\,\\]
	2. Rolling a die until an even result comes up, or the die is rolled three times.
		\\[S = \lbrace  ( i ) , ( j , i ), (  j , j , \lbrace i,j\rbrace  ) \: |\\]
		\\[ \: i \in \lbrace 1,2,4\rbrace , j \in \lbrace 1,3,5\rbrace  \rbrace  \\]
	3. Tossing a pair of coins until they both come up tails.
		\\[S = \lbrace  (e_1), (e_2,e_1), (e_2,e_2,e_1), \\]
		\\[(e_2,e_2,e_2, ..., e_1) \: | \\]
		\\[e_1 = TT, e_2 \in \lbrace HT, TH, HH\rbrace \rbrace \\]
	4. Draw 2 balls from an urn which contains 6 balls, each with a
distinct label from \\(\lbrace 1,2,3,4,5,6\rbrace \\).
		\\[S = \lbrace i,j \: | \: i,j \in \lbrace 1,2,3,4,5,6\rbrace \\]
		\\[  \land i \neq j \rbrace \\]
	5. Draw 1 ball from the same urn, then replace it and draw a ball again.
		\\[S = \lbrace (i,j) \: | \\]
		\\[\: i,j \in \lbrace 1,2,3,4,5,6\rbrace \rbrace \\]
3. For each of the sample space, describe the events (as sets) \\(A\cup B\\) and \\(A \cap B\\), when A and B are as follows.  (2 points each)
	1. A = "5 is rolled exactly twice" and B = "dice values add to an odd number".
		\\[A \cup B = \lbrace  \lbrace i, i, i\rbrace , \lbrace j, j, i\rbrace  \: | \\]
		\\[ \: i \in \lbrace 1, 3, 5 \rbrace , j \in \lbrace 2, 4, 6\rbrace \rbrace  \\]
		\\[A \cap B = \lbrace \lbrace 5, 5, i\rbrace  \: \mid \\]
		\\[ \: i \in \lbrace 1,3\rbrace \rbrace  \\]
	2. A = "1 comes up exactly twice" and B = "3 comes up exactly twice".
		\\[A \cup B = \lbrace (1,1,i), (j, 1, 1), (1, j, 1) \: | \\]
		\\[ \: i \in \lbrace 2,3,4,5,6\rbrace  \\]
		\\[\land j \in \lbrace 3,5\rbrace  \rbrace  \\]
		\\[\cup \lbrace (3,3,i), (j, 3, 3), (3, j, 3) \: | \\]
		\\[ \: i \in \lbrace 1,2,4,5,6\rbrace \\] 
		\\[\land j \in \lbrace 1,5\rbrace  \rbrace  \\]
		\\[A \cap B = \emptyset \\]
	3. A = "both coins come up heads at the same time at some point" and B = "both coins come up tails at the same time at some point,"
		\\[A \cup B = S = \\]
		\\[\lbrace  (e_1), (e_2,e_1), (e_2,e_2,e_1), (e_2,e_2,e_2, ..., e_1) \: \\]
		\\[| \:e_1 = TT, e_2 \in \lbrace HT, TH, HH\rbrace \rbrace \\]
		\\[A \cap B = A = \lbrace  (e_1, e_2, e_3, ... , e_n) \: \\]
		\\[\mid \: e_n = TT \land e_i \in \lbrace HT, TH, HH\rbrace \\]
		\\[ \land 1 \le i \le n - 1 \land \\]
		\\[ n \in N \land \exists j e_j = HH \\] 
		\\[\land 1 \le j \le n - 1 \rbrace \\]
	4. A = "1 is drawn at least once" and B = "1 is drawn twice".
		\\[A\cup B = A = \lbrace \lbrace i,j\rbrace  \: | \\] 
		\\[\: i,j \in \lbrace 1,2,3,4,5,6\rbrace  \land \\]
		\\[(i \neq j) \land (i = 1 \oplus j = 1) \rbrace  \\]
		\\[A \cap B = \emptyset \\]
	5. A = "1 is drawn at least once" and B = "1 is drawn twice"
\\[A \cup B = \lbrace \lbrace 1,1\rbrace ,\lbrace 1,2\rbrace ,\lbrace 1,3\rbrace\\]
\\[ ,\lbrace 1,4\rbrace ,\lbrace 1,5\rbrace ,\lbrace 1,6\rbrace \rbrace \\]
\\[A \cap B = \lbrace \lbrace 1,1\rbrace \rbrace  \\]

## January 30th, 2013 - Lecture: Begin counting and its applications

### Topics

- Finish proof about probability of a union. 
- Counting: The multiplication rule, permutations of n objects and k-out-of-n objects. 
- The birthday problem. 
- Permutations when some objects are indistinguishable. 
- Counting walks on grids.

### Introduction

- Claim: If P is a probability measure on S and \\( E \subseteq S \\), \\(F \subseteq S \\) are events, then
\\( P(E \cup F) = P(E) + P(F) - P(E \cap F) \\). Proof:
	+ \\(P( E \cup F)\\)
		* The first step in a lot of these proofs is to "disjointify" \\(E \cup F \\)
		* The handy way to do this is to write that as \\( E \cup (E^c \cap F) = P(E) + P(E^c \cap F)\\)
	+ Now we need \\( P(E^c \cap F) = P(F) - P(E \cap F) \\)
		* Equivilently, \\(P(F) = P(E \cap F) + P(E^c \cap F) \\). This is true because:
			* \\( F = (E \cap F) \cup (E^c F) \\)
			* \\( E \cap F \\) and \\( E^c \cap F \\) are mutually exclusive.

### Counting

- Multiplication rule: If I have \\(n_1 \\) choices in an experiment, and if I have for each of my first choices another \\(n_2\\) choices, and the same \\(n_3\\) choices, up to \\(n_r\\). In that setting, then I have \\( n_1 \times n_2 \times n_3 \times ... \times n_r \\) total choices.
	+ Example: How many license plate numbers are there if they consist of 6 characters, the first six being letters and the last three being numbers? (ABX 161)
		* 26 choices for first letter
		* 26 choices for the second letter
		* 26 choices for the third letter
		* 10 choices for the first number
		* 10 choices for the second number
		* 10 choices for the third number
		* Therefore, 26 x 26 x 26 x 10 x 10 x 10 = 
	+ Example: What if no repetitions are allowed?
		* 26 possibilities
		* 25 possibilities
		* 24 possibilities
		* 10 possibilities
		* 9 possibilities
		* 8 possibilities
		* 26 x 25 x 24 x 10 x 9 x 8 = 
- Permutations: "How many ways can I arrage n distinct objects in a line? (i.e. in order)
	+ Answer: Build an arrangement by picking 1st element, then 2nd element, etc, euntil nth.
	+ Definition: n! = n(n + 1) ... x 2 x 1
		* 0! = 1 (There is only one way to arrange zero items)
	+ What is we only arrange k < n of the objects?
		* \\(n - k + 1 = \frac{n!}{(n - k)!} \\)
	+ Example: A class of 6 men and 4 women
		1. How many ways can they be ranked? 
			* 10!
		2. What if you rank men and women seperately?
			* 6! + 4!
	+ Birthday "Paradox" (Surprise)
		* Assume birthdays are random, you can be born on any day, and ignore February 29th.
		* What is the size of the group required to give us a 50% chance of getting a match?
		* Use your intuition: There are 365 days, so probably around 1/365?
		* You'd expect 100 people, 200 people, once you approach half the number of days.
		* Let's study this using our probability.
		* Take n people, n random birthdays.
		* Sample space will be S = {1, ..., 365}^n
		* \\( E \subseteq S \\) represents "there is at least one match"
		* \\( P(E) = 1 - P(E^c) \\)
		* It's kind of hard to account for E, with multiple matches, all matches, etc.
		* The complement of E is "there are no matches."
		* How big is E complement?
		* \\( E^c \subseteq S \\) is a lists of n numbers without match.
		* \\( |E^c| = 365 \times 364 \times 363 \times (365 - n + 1) \\) 
		* \\( P(E^c) = \frac{|E^c|}{|S|} = \frac{365 \times 364 \times 363 \times (365 - n + 1)}{365^n} \\)
		* \\( \approx .507 | n = 23 \\)
		* \\( \approx .97 | n = 50 \\)
		* \\( \approx > .999999 | n = 100 \\)
		* Intuition: It's not the number of people that matters, it's the number of pairs, \\(O(n^2)\\) type of growth.
- How many distinct strings can be formed from the letters in "remember"? Answer: 
	+ There are 8! ways to arrange the letters in total.
	+ There are 3! ways to arrange the Es without changing the word.
	+ There are 2! ways to arrange the Rs without changing the word.
	+ There are 2! ways to arrange the Ms without changing the word.
	+ There is 1 way to rearrange the B without changing the word.
	+ \\(\mathrm{R_1 E_1 M_1 E_2 M_2 B_1 E_3 R_2} \\)
	+ \\( \frac{8!}{3!\times 2!\times 2! \times 1!} \\)
	+ How many times does "remember" show up in the list?
	+ Permutations when some elements are interchangable: When putting n objects  in order if n_1 are interchangabl and N_2 are interchangable, and ..., n_r are interchangable, the number of permutations \\( \frac{n!}{n_1!n_2! ... n_r!} \\)

## January 30th, 2013 - Recitation

1. Give an inductive proof of the identity: \\( \left(\bigcup_{i=1}^{n}\right)^c = \bigcap_{i=1}^n\left(A_i^c\right)\\). You may use the fact that for any two sets A and B, \\((A \cup B)^c = A^c \cap B^c \\).

2. What are the sample spaces for the following experiments?
	- Throwing three dice
	- Flipping a coin until either (a) "heads" occurs, or (b) the coin is flipped 8 times.
	- Throwing a die until "6" occurs.
	- Drawing 2 balls from an urn, where the urn contains 5 balls, each with a distinct label from 1 to 5.
	- Picking one ball from the same urn as above, and then putting it back into the urn and again picking a ball.

3. Which of the sample spaces from Exercise 2 are finite? Which are countable? (Justify your answers.)
4. For the sample spaces you presented in Exercise 2, describe the events \\(A \cup B \\) and \\(A \cap B\\) when A and B are:
	- A = "at least one 6" and B = "an odd total".
	- A = "heads occurs twice" and B = "tails occurs twice"
	- A = "5 occurs an infinite number of times" and B = "6 occurs"
	- A = "5 is drawn at least once" and B = "5 is drawn twice"
	- A = "5 is drawn at least once" and B = "5 is drawn twice"

## January 30th, 2013 - Reading

### 1.2 The Basic Principle of Counting

> The basic principle of counting will be fundamental to all our work. Loosely put, it states that if one experiment can result in any of m possible outcomes and if another experiment can result in any of n possible outcomes, then there are mn possible out- comes of the two experiments.

- **The basic principle of counting**: Suppose that two experiments are to be performed. Then if experiment 1 can result in any one of m possible outcomes and if, for each outcome of experiment 1, there are n possible outcomes of experiment 2, then together there are mn possible out- comes of the two experiments.
- **The generalized basic principle of counting**: If r experiments that are to be performed are such that the first one may result in any of n1 possible outcomes; and if, for each of these n1 possible outcomes, there are \\(n_2\\) possible outcomes of the second experiment; and if, for each of the possible outcomes of the first two experiments, there are \\(n_3\\) possible outcomes of the third experiment; and if ..., then there is a total of \\(n_1 \cdot n_2 … n_r \\) possible outcomes of the r experiments.

#### Example 2a

- A small community consists of 10 women, each of whom has 3 children. If one woman and one of her children are to be chosen as mother and child of the year, how many different choices are possible?
- Solution. By regarding the choice of the woman as the outcome of the first experiment and the subsequent choice of one of her children as the outcome of the second experiment, we see from the basic principle that there are \\(10 \times 3 = 30\\) possible choices.

#### Example 2b

- A college planning committee consists of 3 freshmen, 4 sophomores, 5 juniors, and 2 seniors. A subcommittee of 4, consisting of 1 person from each class, is to be chosen. How many different subcommittees are possible?
- Solution. We may regard the choice of a subcommittee as the combined outcome of the four separate experiments of choosing a single representative from each of the classes. It then follows from the generalized version of the basic principle that there are \\(3 \times 4 \times 5 \times 2 = 120 \\) possible subcommittees.

#### Example 2c

- How many different 7-place license plates are possible if the first 3 places are to be occupied by letters and the final 4 by numbers?
- Solution. By the generalized version of the basic principle, the answer is \\(26 \times 26 \times 26 \times 10 \times 10 \times 10 \times 10=175,760,000\\).

#### Example 2d

- How many functions defined on n points are possible if each functional value is either 0 or 1?
- Solution. Let the points be 1,2,...,n. Since \\(f(i)\\) must be either 0 or 1 for each i = 1, 2, . . . , n, it follows that there are \\(2_n\\) possible functions.

#### Example 2e

- In Example 2c, how many license plates would be possible if repetition among letters or numbers were prohibited?
- Solution. In this case, there would be \\(26 \times 25 \times 24 \times 10 \times 9 \times 8 \times 7 = 78,624,000\\) possible license plates.

### 1.3 Permutations

* How many different ordered arrangements of the letters a, b, and c are possible? 
* By direct enumeration we see that there are 6, namely, abc, acb, bac, bca, cab, and cba. 
* Each arrangement is known as a **permutation**. Thus, there are 6 possible permutations of a set of 3 objects.

\\(n(n − 1)(n − 2) … 3 \times 2 \times 1 = n!\\)

#### Example 3a

- How many different batting orders are possible for a baseball team consisting of 9 players?
- Solution. There are 9! = 362,880 possible batting orders.

#### Example 3b

- A class in probability theory consists of 6 men and 4 women. An examination is given, and the students are ranked according to their performance. Assume that no two students obtain the same score.
	1. How many different rankings are possible?
	2. If the men are ranked just among themselves and the women just among themselves, how many different rankings are possible?
- Solution. 
	1. Because each ranking corresponds to a particular ordered arrangement of the 10 people, the answer to this part is 10! = 3,628,800.
	2.  Since there are 6! possible rankings of the men among themselves and 4! possi- ble rankings of the women among themselves, it follows from the basic principle that there are (6!)(4!) = (720)(24) = 17,280 possible rankings in this case.

#### Example 3c

- Ms. Jones has 10 books that she is going to put on her bookshelf. Of these, 4 are mathematics books, 3 are chemistry books, 2 are history books, and 1 is a language book. Ms. Jones wants to arrange her books so that all the books dealing with the same subject are together on the shelf. How many different arrangements are possible?
- Solution. There are 4! 3! 2! 1! arrangements such that the mathematics books are first in line, then the chemistry books, then the history books, and then the language book. Similarly, for each possible ordering of the subjects, there are 4! 3! 2! 1! possible arrangements. Hence, as there are 4! possible orderings of the subjects, the desired answer is 4! 4! 3! 2! 1! = 6912.

#### Example 3d

- How many different letter arrangements can be formed from the letters PEPPER?
- Solution. We first note that there are 6! permutations of the letters \\(P_1E_1P_2P_3E_2R\\) when the 3P’s and the 2E’s are distinguished from each other. However, consider any one of these permutations—for instance, P1P2E1P3E2R. If we now permute the P’s among themselves and the E’s among themselves, then the resultant arrangement would still be of the form PPEPER.

#### Example 3e

- A chess tournament has 10 competitors, of which 4 are Russian, 3 are from the United States, 2 are from Great Britain, and 1 is from Brazil. If the tournament result lists just the nationalities of the players in the order in which they placed, how many outcomes are possible?
- Solution: There are \\( \frac{10!}{4!3!2!1!} = 12600 \\) possible outcomes

#### Example 3f

- How many different signals, each consisting of 9 flags hung in a line, can be made from a set of 4 white flags, 3 red flags, and 2 blue flags if all flags of the same color are identical?
- Solution: There are \\( \frac{9!}{4!3!2!1!} = 1260 \\) possible outcomes

### 2.4 Some Simple Propositions (after proposition 4.3)

## February 4th, 2013 - Lecture: Combinations

### Topics

- Deriving the formula for combinations. 
- Basic identities and examples. 
- The antenna problem (Ex. 4c of Ross). 
- Counting divisions where all sets non-empty and where sets are allowed to be empty.

### Combinations

+ How many ways can we choose k out of n objects when order does not matter?
+ Take S = {\\(x_1, ... , x_n\\)}. How many k-element subsets does S have?
+ Call the number of k element subsets C(n,k)
+ In general,
	* C(n,1) = n
	* C(n,n) = 1
	* C(n,2) = # of 2-element subsets
+ S = {\\(x_1, ... , x_n\\)}
	* From every 2 element list -> n(n - 1)
+ Number of subsets will equal \\[ \frac{\mathrm{number \: of \: 2 \: element \: sets}}{2} = \frac{n(n - 1)}{2} \\]
+ C(n,k) for general k (S = {\\(x_1, ... , x_n\\)})
	* \\(\frac{n!}{(n - k)!} \\) ways to list k-out-of-n elements
	* Every k-element subset is represented k! times in big list
	* Big list has \\(\frac{n!}{(n-k)!} \\) entries
	* \\( C(n,k) \times k! = \frac{n!}{(n-k)!} \\)
+ Notation: \\( {{n} \choose {k}}  = \frac{n!}{(n-k)!k!}\\)
	\\[ {n \choose 1} = \frac{n!}{(n-1)!1!} = n\\]
+ Claim: \\( {n \choose k} = {n \choose n-k} \\)
	\\[ {n \choose n - k} = \frac{n!}{(n - (n - k))!(n - k)!} = \\]
	\\[\frac{n!}{k!(n - k)!} = {n \choose k} \\]
+ The number of possible 5-card poker hands is: \\( {52 \choose 5} = 2578960 \\)

## February 4th, 2013 - Reading

### 1.4 Combinations (through example 4c)

- How many groups of *r* objects can be formed from a total of *n* objects?
	+ How many groups of 3 could be formed from the 5 items *A, B, C, D,* and *E*.
	+ Since there are 5 ways to select the initial item, 4 ways to select the next item, and 3 ways to select the final item, there are thus \\(5 \times 4 \times 3 \\) ways of selecting the group of 3 (order relevant).
	+ In this formulation, each group as a set will be counted 6 times.
	+ The total number of groups that can be formed is: 
	\\[ \frac{5 \times 4 \times 3}{3 \times 2 \times 1} = 10\\]
	+ In general, *n(n - 1) … (n - r + 1)* represents the number of different ways that a group of *r* items could be selected from *n* items when order is relevant.
	+ It follows that the number of different groups of *r* items that could be formed from a set of *n* items is
	\\[ \frac{n(n-1) … (n - r + 1)}{r!} = \frac{n!}{(n - r)!r!}\\]
- **Notation and terminology**
	+ We define \\( n \choose r \\), for \\( r \le n \\) by
	\\[ {n \choose r} = \frac{n!}{(n - r)!r!}\\]
	and say that \\( n \choose r \\) represents the number of possible combinations of *n* objects taken *r* at a time.

#### Example 4a

- A committee of 3 is to be formed from a group of 20 people. How many different committees are possible?
- Solution: There are \\({20 \choose 3} = \frac{20 \cdot 19 \cdot 18}{3 \cdot 2 \cdot 1} = 1140 \\) possible combinations.

#### Example 4b

- From a group of 5 women and 7 men, (1) how many different committees consisting of 2 women and 3 men can be formed? (2) What if 2 of the men are feuding and refuse to serve on the committee together?
	1. Solution: \\( {5 \choose 2}{7 \choose 3} = 350 \\) possible combinations of 2 women and 3 men.
	2. I'll ask about this problem in office hours.

#### Example 4c

- Consider a set of *n* antennas of which m are defective and *n − m* are functional and assume that all of the defectives and all of the functionals are considered indistinguishable. How many linear orderings are there in which no two defectives are consecutive?
- Solution:
\\[ n - m + 1 \choose m \\] possible orders in which there is at least once functional antenna between any two defective ones.

### 1.6 The Number of Integer Solutions of Equations


## February 6th, 2013 - Lecture: Binomial and Multinomial Coefficients

### Topics
- Pascal's relationship and Pascal's triangle.
- The binomial theorem and proofs by combinatorial reasoning and induction.
- Some consequences and examples.
- Multinomial coefficients and their applications to dividing groups and counting strings.

### Introduction

- For all *n, k >= 0*.
\\[
{n \choose k} = {n - 1 \choose k - 1} + {n - 1 \choose k}
\\]

- Proof:
	+ \\({n \choose k}\\) = the number of k-elements of subsets of \\(x_1 ... x_n \\).
	+ Observation: Take any of the \\(x_1 .. x_n \\), say \\(x_n\\). Then every k-element subset either cointains \\(x_n\\) or it doesn't.
	+ \\(n - 1 \choose k - 1\\) is the number that do contain \\(x_n\\) and \\(n - 1 \choose k \\) is the number that don't.
	+ The number that do contain \\(x_n\\) is \\(n - 1 \choose k - 1 \\).

- Pascal's Triangle
	+ Put \\( 0 \choose 0 \\) at the top.
	+ The next level is two instances of \\(1 \choose 0 \\)
	+ ...

						1
					1	2	1
				1	  3	  3    1
			1	  4	    6	4	 1
			
### Binomial Theorem

+ For all *x, y*, all *n >= 1*,
\\[
(x + y)^n = \sum_{k = 0}^n {n \choose k}x^ky^{n - k}
\\]
+ Intuitive Combinatorial Proof (Simpler)
	* When you expand \\((x + y)^n\\), it equals \\((x + y)(x+y) ... (x + y) \\) "*n*-times"
	* One way to compute all "monomials" in product is to start with *x*, and then pick all the way done, one per time, and repeat the exercise until all combinations are exhausted, and you have every monomial.
	* Which monomials show up in sum?
	* \\(x^a y^b\\) shows up \\(n \choose a\\)
- Proof by induction
	+ We've already checked *n = 1*.
	+ Now assume true for *n - 1* and prove for *n > 1*
		\\[ (x+y)^n = (x+y)(x+y)^{n-1} \\]
		\\[= (x+y)\cdot\sum_{k=0}^{n-1}{n - 1 \choose k}x^k y^{n - 1 -k}\\]
		\\[= x\sum_{k = 0}^{n - 1}{n - 1 \choose k}x^k y^{n - 1 - k} + \\]
		\\[= y\sum_{k = 0}^{n - 1}{n - 1 \choose k}x^k y^{n - 1 - k} \\]
	* Write *i* for *k + 1*:
		\\[\sum_{i = 1}^n {n - 1 \choose i - 1}x^i y^{n - 1} + \\]
		\\[\sum_{i = 1}^n {i \choose n - 1}x^i y^{n - 1}\\]
		\\[ = x^n + \sum_{i = 1}^{n - 1} \left[ {n - 1 \choose i - 1} + {n - 1 \choose i} \right] \times\\]
		\\[x^i y^{n - i} + y^n \\]
- Corollary: For any *n >= 1*, \\(\sum_{k = 0}^{n}{n \choose k} = 2^n \\)
	+ Proof:
		\\[2^n = (1 + 1)^n = \sum_{k = 0}^n{n \choose k}\\\]
	+ Intuition: This sum should be the number of wqys to pick a subset of any size from a set of size *n*.
		* To pick a subset, we have *n* decisions where we decide if each \\)x_i\\) is in the subset or not.

### Multinomial Coefficients
+ Arise from the following type of problem:
	* Given a set of *n* distinct items, you need to divide them up into *r* groups of given sites \\(n_1, n_2, ..., n_r \\) where \\(n_1 + n_2 + ... + n_r = n \\).
	* How many ways can this be done, for a given *n*, *r*, and \\(n_1\\) up to \\(n_r\\) where there all add up to *n*.
+ This is very close to something we've already seen, and there are two ways of thinking about it.
	1. How many choices for 1st group? Then into the second, then into the third ...
		\\[ n \choose n_1 \\]
		ways to choose the first group
		\\[ n - n_1 \choose n_2 \\]
		ways to choose the second group, etc, and for the \\(r^{th}\\) group:
		\\[n - n_1 - n_2 - ... - n_{r-1} \choose n_r = 1 \\]
		so the multiplication principle tells us that if we multiply these all together, we get our answer. It cancels nicely:
		\\[=\frac{n!}{(n - n_1)!n!}\cdot\frac{n-n_1}{(n - n_1 - n_2)!n!} ...  \\]
		and this cancels to
		\\[\frac{n!}{n_1!n_2!...n_r!}\\]
+ Example: There are 10 TAs in the department, and we need 3 TAs for OSs, 2 for algorithms, and 5 for databases. There there are:
	\\[ \frac{10!}{3!2!5!} \\]
	ways to assign them, which is \\(2520\\).

## February 6th, 2013 - Recitation

5. Determine the number of vectors \\(x_1, x_2, x_3, ..., x_n \\) such that each \\(x_i\\) is either 0 or 1.
\\[ \sum_{i = 1}^{n} x_i \le k \\] (constraint)
	- Solution
	\\[x_i \in \lbrace 0, 1 \rbrace  \\]
		+ The set should be less than \\(2^n\\)
		+ Three cases:
			1. *n = k*: everything should be 1
			2. *n < k*: everything something 0
			3. *n > k*: the only interesting *k*, \\( n \gt k\\)
6. Determine the number of vectors \\(x_1, x_2, x_3, ..., x_k \\) such that each \\(x_i\\) is a positive integer such that \\( 0 \le n \le n \\) and \\( x_1 < x_2 < x_3 ... < x_k \\)
	\\[n \choose k\\]
	
		123 234 134 145 145 345
		124 235 135 245
		125

8. Prove that 
\\[{n + m \choose r} = {n \choose 0}{m \choose r} + \\]
\\[{n \choose 1 }{m \choose r - 1} ... + {n\choose r} {m \choose 0} \\]

## February 6th, 2013 - Reading

### 1.5 Multinomial Coefficients

- **Notation**
	+ If \\( n_1 + n_2 + … + n_r = n \\), we define \\(n \choose n_1 + n_2 + … + n_r \\) by

\\[ {n \choose n_1 + n_2 + … + n_r} = \frac{n!}{n_1! + n_2! + … + n_r!} \\]
	+ Thus, \\(n \choose n_1 + n_2 + … + n_r \\) represents the number of possible divisions of *n* distinct objects into r distinct groups of respective sizes \\(n_1, n_2, … , n_r \\).

- **The multinomial theorem**
\\[ (x_1 + x_2 + … + x_r)^n = \\]
\\[ \sum_{(n_1, …, n_r) : } \\]

## February 7th, 2013 - Homework 2

Paul Jones\
Professor David Cash\
Introduction to Discrete Structures II (01:198:206)\

Homework 1

1.  (8 points) Prove that \\(P(A \cup B) \le P(A) + P(B)\\) for any events A
    and B. Prove the general version by induction, which says that if
    \\(A_1, ..., A_n\\) are events then
    \\(P(\bigcup_{i = 1}^n A_i) \le P(\sum_{i = 1}^n A_i)\\). When does this
    inequality become an equality?

    -   Base case

        $$P(A_1 \cup A_2) \le P(A_1) + P(A_2)$$

    -   Assume it holds for a general case $(n=k)$

        $$P\left(\bigcup_{i = 1}^k A_i\right) \le \sum_{i = 1}^k P(A_i)$$

        $$P(A_1 \cup A_2 \cup ... \cup A_k) \le P(A_1) + P(A_2) + ... + P(A_k)$$

    -   Prove that it hold for next case using your assumption.

        $$P\left(\bigcup_{i = 1}^{k+1} A_i\right) \le \sum_{i = 1}^{k+1} P(A_i)$$

        $$P(A_1 \cup A_2 \cup ... \cup A_k \cup A_{k+1}) \le P(A_1) + P(A_2) + ... + P(A_k) + P(A_{k+1})$$

        $$(A_1 \cup A_2 \cup ... \cup A_k) = C$$

        $$P(A_1) + P(A_2) + ... + P(A_k) = D$$

        $$P(C \cup A_{k+1}) \le P(D) + P(A_{k+1})$$

        By the base case, this is true, and expression is proven for all
        events.

2.  (4 points) If \\(P(A) = \frac{1}{2}\\), \\(P(B) = \frac{1}{5}\\), and
    \\(P(A\cup B) = 3/5\\), what are \\(P(A\cap B)\\), \\(P(A^c \cup B)\\), and
    \\(P(A^c \cap B)\\)?

    -   $P(A\cap B) = \frac{1}{10}$

    -   $P(A^c \cup B) = 3/5$ because the probability of $A$ is the same
        as $A^c$

    -   $P(A^c \cap B) = \frac{1}{10}$

3.  (3 points) How many elements are there in the set

    {$x : 10^7 \le x \le 10^8$, and the base 10 representation of x has
    no digit used twice}?

    -   $10^7 = 10000000$, and $10^8 = 100000000$

    -   The smallest number possible is $12345678$, the greatest number
        possible is $98765432$

    -   For the first number in any element, the first option is {1, 2,
        3, 4, 5, 6, 7, 8, 9}.

    -   Then for the every second number, it’s every number besides the
        first choice plus 0.

    -   The “tree” looks as follows, where
        $i\neq j\neq k\neq l\neq m\neq n\neq o\neq p$:

        1.  $$\{1 i j k l m n o \}$$ where
            $$\{i,j,k,l,m,n,o\} \in \{0,2,3,4,5,6,7,8,9\}$$

        2.  $$\{2 i j k l m n o \}$$ where
            $$\{i,j,k,l,m,n,o\} \in \{0,1,3,4,5,6,7,8,9\}$$

        3.  $$\{3 i j k l m n o \}$$ where
            $$\{i,j,k,l,m,n,o\} \in \{0,1,2,4,5,6,7,8,9\}$$

        4.  $$\{4 i j k l m n o \}$$ where
            $$\{i,j,k,l,m,n,o\} \in \{0,1,2,3,5,6,7,8,9\}$$

        5.  $$\{5 i j k l m n o \}$$ where
            $$\{i,j,k,l,m,n,o\} \in \{0,1,2,3,4,6,7,8,9\}$$

        6.  $$\{6 i j k l m n o \}$$ where
            $$\{i,j,k,l,m,n,o\} \in \{0,1,2,3,4,5,7,8,9\}$$

        7.  $$\{7 i j k l m n o \}$$ where
            $\{i,j,k,l,m,n,o\} \in \{0,1,2,3,4,5,6,8,9\}$$

        8.  $$\{8 i j k l m n o \}$$ where
            $$\{i,j,k,l,m,n,o\} \in \{0,1,2,3,4,5,6,7,9\}$$

        9.  $$\{9 i j k l m n o \}$$ where
            $$\{i,j,k,l,m,n,o\} \in \{0,1,2,3,4,5,6,7,8\}$$

    -   Every “node” (a) through (i) is $9 \choose 1$.

    -   When you pick the first number, you still have 9 choices because
        zero is added. When you choose the second number, you have 8
        choices because a number is taken out and non are put back into
        the set of choices. When you pick your third number, you have 7
        choices because a number is taken out and none put back in. ...

    -   So for integer strings $i$ through $o$:

        $$[i]\quad\quad[j]\quad\quad[k]\quad\quad[l]\quad\quad[m]\quad\quad[n]\quad\quad[o]\quad\quad[p]$$

    -   The number of elements is equal to

        $${9 \choose 1}\times{9 \choose 1}\times{8 \choose 1}\times{7 \choose 1}\times{6 \choose 1}\times{5 \choose 1}\times{4 \choose 1}\times{3 \choose 1}$$

4.  (3 points) An army output has 19 posts to staff using 30
    indistinguishable guards. How many ways are there to distribute the
    guards if no post is left empty?

    -   This is a “stars and bars” problem, where the number of “stars”
        $k$ is equal to 30, and the number of “bars,” “bins,” or “posts”
        $n$ is equal to 19.

        $${k - 1 \choose n - 1} = {30 - 1 \choose 19 - 1} = {29 \choose 18} = 34597290$$

5.  (1 point) What is the coefficient of $x^{10}y^{13}$ when
    $(x + y)^{23}$ is expanded?

    -   This problem requires the binomial theorem, where $n = 23$:

        $$(x + y)^{23} = \sum_{k = 0}^{23} {23 \choose k}x^ky^{23 - k}$$

    -   When $k = 10$, $23 - k$ will equal 13.

        $${23 \choose 10}x^{10} y^{13}$$

    -   So the coefficient for $x^{10} y^{13}$ will be

        $${23 \choose 10} = 1144066$$

6.  (4 points) What is the coefficient of $w^{9}x^{31}y^{4}z^{19}$ when
    $(w + x + y + z)^{63}$ is expanded? How many monomials appear in the
    expansion?

    -   This is a multinomial coefficient problem where $k = 4$ and
        $n = 63$:

        $$(a_1+a_2+...+a_k)^n=\sum_{\substack{n_1,n_2,...,n_k\ge 0 \\ 
        n_1+n_2+...+n_k=n}}\frac{n!}{n_1!n_2!...n_k!}a_1^{n_1}a_2^{n_2}...a_k^{n_k}$$

    -   Set $n_1 = 9$, $n_2 =31$, $n_3 = 4$, and $n_4 = 19$.

        $$\left(\frac{63!}{9!31!4!19!}\right)\times w^{9}x^{31}y^{4}z^{19}$$

    -   Therefore, the coefficient is

        $$\frac{63!}{9!31!4!19!}$$

    -   The number of monomials in a multinomial coefficient can be
        expressed as a “stars and bars” problem.

        $$66 \choose 3$$

7.  (6 points) Let $p$ be a prime number and $1 \le k \le p - 1$. Prove
    that $p \choose k$ is a multiple of $p$. Show that this is not true
    if $p$ is not prime.

    $${p\choose k} = \frac{p(p-1) \times ... \times (p - k + 1)}{1 \times 2 \times ... \times (k - 1) \times k} = p{p - 1 \choose k}$$

    $${4\choose 2} = 6$$

    6 is not a multiple of 4 and is not prime.

8.  Verify that for any $n \ge k \ge 1$

    $${n \choose 2} = {k \choose 2} + k(n - k) + {n - k \choose 2}$$

    Then give a combinatorial argument for why this is true.

    -   Observe that the binomial coefficient with two for all reals:

        $${r\choose 2} = \frac{r (r - 1)}{ 2}$$

    -   Apply fact to both sides:

        $$\frac{n (n - 1)}{ 2} = \frac{k (k - 1)}{ 2} + k(n - k) + \frac{(n - k) (n - k - 1)}{ 2}$$

    -   Multiply everything by two

        $$n (n - 1) = k (k - 1) + 2k(n - k) + (n - k)(n - k - 1)$$

    -   Expand out

        $$n (n - 1) = k^2 - k + 2kn - 2k^2 + k+k^2-n-2 k n+n^2$$

    -   Simplify

        $$n (n - 1) = -n+n^2$$

    -   Change form

        $$n (n - 1) = n (n - 1)$$

    -   Combinatorial argument:

        -   $n \choose 2$ is the number of ways we can arrange $n$
            objects into groups of 2.

        -   Splitting $n$ into 2, one of those groups will be of size
            $k$, making the other set of size $n - k$

        -   Using the new partitions $k$ and $n-k$, arrange $n$ “things”
            into groups of two.

        -   The first partition is of length $k$, resulting in
            $k\choose 2$ ways, and for the second part, we have $n-k$
            choose 2 ways, explaining the first and last terms.

        -   Now choose 2 “things”, one from different groups of 2, we
            can choose 1 of the k objects and all of $n-k$ “things”,
            which is equal to $k(n-k)$.




## February 11th, 2013 - Lecture: Multinomial Theorem, Counting Problems, Inclusion-Exclusion

### Topics

- The multinomial theorem and applications 
- The "tree method" for various counting problems involving card hands and committees
- Inclusion-exclusion

### Lecture

- **Multinomial coefficients**: see reading 1.5 in February 7th reading
	+ **Multinomial theorem**: see reading 1.5 in February 7th reading
		* Sum runs over all vectors of non-negative integers that sum to *n*.
		* Example: \\( (x_1 + x_2 + x_3)^2 \\) =
		\\[\sum_{(n_1, n_2, n_3) : n_1, n_2, n_3 = 2} {2 \choose n_1, n_2, n_3} x_{1}^{n_1} x_{2}^{n_2} x_{3}^{n_3} \\]
		\\[ = {2 \choose 2, 0, 0} x_{1}^{2} x_{2}^{0} x_{3}^{0} +  \\]
		\\[ {2 \choose 0, 2, 0} x_{1}^{0} x_{2}^{2} x_{3}^{0} + \\]
		\\[ {2 \choose 0, 0, 2} x_{1}^{0} x_{2}^{0} x_{3}^{2} + \\]
		\\[ {2 \choose 1, 1, 0} x_{1}^{1} x_{2}^{1} x_{3}^{0} + \\]
		\\[ {2 \choose 1, 0, 1} x_{1}^{1} x_{2}^{0} x_{3}^{1} + \\]
		\\[ {2 \choose 0, 1, 1} x_{1}^{0} x_{2}^{1} x_{3}^{1} \\]
		
		* Example: What is the coefficient of \\(x^3 y^4 z\\) when \\((x + y + z)^13 \\) is expanded? It corresponds to:
		\\[ {13 \choose 3, 9, 1} = 2860 \\]
		* Question: How many terms are in the sum? Equivilently, how many monomials are in the expansion? (If *n = 2*, *r = 3*, then 6)
- **More on counting**
	+ Deck of cards: 52 cards, 4 suits, 13 ranks, one of each suit/rank combination
	+ Number of 5 card hands:
	\\[ 53 \choose 5 \\]
	+ Number of flushes:
		* 4 different suits for flushes
		* For each suit, the number of flushes is \\( 13 \choose 5 \\)
		* Therefore,
		\\[4 \times {13 \choose 5}\\]
	+ Example: Suppose a committe of *k* people from a group of 7 women and 4 men.
		* How many ways can form the committee if it has:
			1. 3 women and 3 men exactly
			\\[{7 \choose 3} \times {4 \choose 3} \\]
			2. The committee is any size, but it has equal number of men and women. Choices:
				1. 1 each
				\\[= {7 \choose 1} \times {4 \choose 1} + \\]
				2. 2 each
				\\[{7 \choose 2} \times {4 \choose 2} + \\]
				3. 3 each
				\\[{7 \choose 3} \times {4 \choose 3} + \\]
				4. 4 each
				\\[{7 \choose 4} \times {4 \choose 4} \\]
			3. If the commitee has 4 people, at least 2 of which are women? 
				* Steps:
					1. Pick the number of women
					2. Pick the women
					3. Pick men for the remaining spots.
				* Possibilities:
					1. 2 women
					\\[= {7 \choose 2} \times {4 \choose 2} + \\]
					2. 3 women
					\\[{7 \choose 3} \times {4 \choose 1} + \\]
					3. 4 women
					\\[{7 \choose 4} \times {4 \choose 0} \\]
	+ Example: How many hands have exactly 3 aces? "Pick 3 aces, then pick 2 non-aces"
	\\[{4 \choose 3}\times{48 \choose 2}\\]
	+ Example: How many full houses?
		* Pick the rank of 3-of-a-kind (AAA, 222, ...)
		* Pick the rank of 2-of-a-kind 
		* Pick the B-of-a-kind
		* Pick the 2-of-a-kind
	\\[13 \times 12 \times {4 \choose 3}\times {4 \choose 2} \\]
+ Probability theory
\\[ P(A \cup B \cup C) = \\]
\\[ P(A) + P(B) + P(C) - \\]
\\[ P(A \cap B) - P(A \cap C) -  \\]
\\[ P(A \cap C) + P(A \cap B \cap C) \\]

	+ If P is a probability measure an \\( A_1, ... A_n \\) are events:
	\\[P(A_1 \cup A_2 \cup ... \cup A_n) = \\]
	\\[\sum_{i = 1}^n P(A) - \sum_{i \lt j} P(A_i \cap A_j) + \\]
	\\[ \sum_{i \lt j \lt k}P(A_i \cap A_j \cap A_k) - ... \\]
	\\[+ (-1)^{n + 1} P(A_1 \cap ... A_n)\\]

	- Include/Exclude Set Version
		+ Some formula, but with set-size intead of P(1)
		\\[|A_1 \cup ... \cup A_n| = \\]
		\\[\sum|A_1| - \sum|A_i \cap A_j \\]
		\\[\sum A_i \cap A_j \cap A_k \\]
	
	+ Symmetry: For any *i*, |A_i| is the same.
		\\[A_i = {39 \choose 5} \\]
		- For any \\(i \le j \\), \\(|A_i \cap A_j|\\) is the same
		\\[26 \choose 5 \\]
		
## February 11th, 2013 - Reading

### 2.4 Some Simple Propositions (from page 31)	


		
## February 13th, 2013 - Lecture

### Include/Exclude Formula

- If \\(E_1, ..., E_n\\) be events, then

\\[P(E_1 \cup E_2 \cup ... \cup E_n) = \\]

\\[\sum_{i = 1}^n P(E_1) - \sum_i \le j P(E_i \land E_j) + \\]

\\[\sum_{i \lt j \lt k}P(E_i \cap E_j \cap E_K - ... \\]

\\[(-1)^{n+1} P(E_i \cap ... E_n) \\]

### de MontMort's Problem (1713)

- Have n students seated in class, no empty seats.
- Students 1 through n.
- Everyone stands up, all are assigned, random seats.
- What's the probability that somebody gets own seat?

#### Dearrangements

- \\( E = \\) "someone gets own seat"
- \\(E_i = \\) "student i gets own seat"

\\[ E = E_1 \cup E_2 \cup ... \cup E_n \\]

#### Exploit "symmetry"

\\[P(E) = P(E_1 \cup E_2 \cup ... \cup E_n) = \\]

- Observe what is \\(P(E_1) = \frac{1}{n} = \frac{n-1}{n!} \\)
- Moreover, \\(P(E_1) = \frac{1}{n} \\) for any i.

- The number of arrangements that put 1 and 2 in seats 1 and 2 over the number of all possible arrangements is

\\[\frac{(n-2)!}{n!} = \frac{1}{n(n-1)} \\]

- Works for any i and j:

\\[P(E_1 \cap E_j \cap E_k) = \frac{1}{n(n-1)(n-2)} \\]

### Conditional probability

- How we update "beliefs" as new information comes to light.
- Determine for events A, B, P(A/B) = 

\\[\frac{P(A \cap B)}{P(B)} \\]

	+ When B does not equal zero.
	
#### Explanation #1

\\[P(\lbrace 1 \rbrace) | B) \\]

#### Explanation #2 - "Frequentist"

- We have some experiment we are going to repeat, generating data.

		01011010 A
		11101011 B
		00010110 
		11010100
		...
		
 + Count number of times B happens
 + Count number of times that A happens.
 
#### Example - Flipping two coinis

- S = {HH, TH, HT, TT}, all 1/4
- What's the probabilty of getting 2 heads, given that first toss was heads? It's 1/2
	+ A = {HH}
	+ B = {HT, HH}
	
	\\[P(A|B) = \frac{P(\lbrace HH \rbrace)}{\lbrace HT, HH \rbrace}\\]
	
- What's the probability of HH, given that at least one heads came up?
	+ A = {HH}
	+ B = {HT, TH, HH}
	
	\\[P(A|B) = \frac{P(HH)}{P(HT, TH, HH)} = \\] 
	\\[ \frac{\frac{1}{4}}{\frac{1}{4} + \frac{1}{4} + \frac{1}{4}} = \frac{1}{3} \\]
	
### Example 2 - Fuses

- Suppose we have 7 fuses, and 5 are working and 2 are broken.
- We want to find the broken ones, we're going to pick them one at a time, and we test.
	+ What's the probability that we only need 2 tests?
		* Define \\(E_1\\) as "first test shows up broken.
		* \\(E_2\\) as "second ..." ...
		
### Gigerenzer's Experiment

- He did the following experiment:
	+ He got the doctors to agree on some numbers.
	+ They agreed a given patient (say 40-50 year old woman), you know nothing about her except she's in good health.
	+ She has cancer with probability 0.008.
	+ They had a cancer test that, if patient has cancer, returns positive .9 rightly.
	+ If they don't, it will return positive .07 of they time.
- He asked 24 doctors:
	+ Suppose a woman's test is positive, what is the probability that she has cancer?
		* First once said he didn't konw.
		* The other 24 returned this:
		
				8 said <= 10%
				8 said    50% - 80%
				8 said    90%
				
- Lets do some math
	+ C = "patient has cancer"
	+ T = "test is positive"
	\\[P(C) = 0.008 \\]
	\\[P(T|C) = 0.9 \\]
	\\[P(T|C^c) = 0.07 \\]
	+ What's the probability of illness given that the test came up positive? \\(P(C|T) = ? \\)
	\\[P(C|T) = \frac{P(C\cap T)}{P(T)} \\]
	\\[P(T|C) = \frac{P(C \cap T)}{P(C)} \\]
	+ Want P(T)
- **Lemma**: For any event T, C
\\[P(T) = P(T \cap C) + P(T \cap C^c) \\]

- Answer: 9.4%

#### Intuition, not a proof at all

- Say you take 1000 women,
	+ Should have 8 with cancer ill.
	+ How may should test positive? ~7 will be positive
	
## February 13th, 2013 - Recitation

1. Prove the following is true:
\\[ {n \choose 2} = {k \choose 2} + K(n - k) + {{n-k} \choose 2} \\]
	+ What is \\(n \choose 2\\)?
	+ We're going to have to put a *k* into the left hand side.
	+ So you have n object, I can select 2 object as n choose 2
	+ I could do the same selection of 2 objects by partitioning them into n and n-k objects.
	+ Or I could select one from one side, etc.
	+ Since I am selecting two objects, what are the possibilities.
	+ Both of them could be from the left or right, or one could be on both sides.
2. Prove:
\\[\sum_{k=1}^n k {n \choose k} = n2^{n-1} \\]
	+ If you expand out the left hand side:
	\\[1 \times {n \choose 1} + 2 \times {n \choose 2} + ... + n {n \choose n} = n2^{n-1} \\]
3. Let n be the number of people and we have to form a commitee of arbitrary size and select a chair from that committee.
	+ Method 1
	\\[k {n \choose k} \\] is the number of ways to select a commite of size k and a chair
		* Hence, the total number of ways to form a commite of arbitrary size is
		\\[\sum_{k=1}^{n} k {n \choose k} \\]
	+ Method 2
		* We can first select the chair in n-ways. From the remaining n - 1 people we can select a subset in \\(2^{n-1} ways.
		
3. Prove:
\\[\sum_{i=0}^n (-1)^i {n \choose 1} = 0 \\]

## February 18th, 2013 - Lecture: Bayes's Theorem

### Topics: 
- Bayes's theorem: Statement, examples, applications to spam filtering and other fields. 
- General version of Bayes's theorem and the red/black hat problem.

### Boxes and balls

- **Example**: There two boxes, the first contains 2 green balls and 7 res and the second contains 4 green and 3 red. I pick a random box, then a ball from that box. If I pick a red ball, what is the probability that I picked the first box?
	+ E = "red ball was picked"
	+ F = "1st box was picked
	\\[P(F | E) = \frac{P(E \cap F)}{P(E)} = \\]
	\\[\frac{\frac{7}{18}}{\frac{38}{63}} \\]
	(I) \\[P(E \cap F) = P(E | F) \times P(F) = \\]
	\\[\frac{7}{9} \times \frac{1}{2} = \frac{7}{18} \\]
	(II) \\[ P(E) = P(E \cap F) + P(E \cap F^c) = \\]
	\\[\frac{7}{18} + P(E | F^c) \times P(F^c) = \\]
	\\[\frac{7}{18} + \frac{3}{7} \times \frac{1}{2}\\]

### "Bayesian Reasoning"

+ A method for updating "belief"/"uncertainty" based on evidence.
+ This is useful when you want to know the probability of some outcome given some evidence 
when you know the probability of the outcome and you also konw the quality of your evidence, and the probability
of the evidence given the outcome, and finally, the probability of the evidence showing up if the outcome didn't 
happen.
	1. P(outcome|evidence)
	2. P(outcome)
	3. P(evidence|outcome)
	4. P(evidence|outcome^c)

### Bayesian Spam Filtering
- Outdated but interesting anyway
+ The idea is that you estimate P(Email contains some word w | it's spam)
	* Rolex
	* Viagra
	* Rutgers
	* Cash
	* LaTeX
+ Then the probability of the P(Emails contains the same word w | it's not spam)
+ P(Email is spam)
+ Using these, there is Bayes theorem, which computes P(outcome|evidence) = P(spam | contains w)
+ The attack is called Bayesian poisoning
	* You retrain this when you email it everyday.
	* Spammers pass it the words you are interested in, which you mark as spam, 
		and then the ones you aren't interested in eventually pass.

### Bayes Theorem

- If E and F are events with \\(P(E) \neq 0 \\) and \\(P(E) \neq 0 \\), then
\\[ P(F | E) = \frac{P(E | F) \times P(F)}{P(E | F)\times P(F) + P(E | F^c) \times P(F^c)} \\]
	1. \\(P(E \cap F) = P(E | F) \times P(F) \\)
	2. \\(P(E) = P(E | F) \times P(F) + P(E | F^c) \times P(F^c) \\)
	
### General version of Bayes theorem

- For multiple outcomes
- Let \\(F_1 ... F_n\\) be events that
	1. Are mutually exclusive
	2. \\(F_1 \cup ... \cup F_n = S \\)
	3. \\(\forall i P(F_i \neq 0) \\)
- Then for any j
\\[ P(F_j | E) = \\]
\\[\frac{P(E|F_j) \times P(F_j)}{\sum_{i=1}^n P(E|F_i) \times P(F_i)} \\]

#### Example with Lizards

- \\(F_1 ... F_n\\) are lizards in the family i
- E = "something genome of new lizard"
- Need to estimate the priors

## February 18th, 2013 - Reading

### Ross 3.3

### Rosen 7.3

## February 19th, 2013 - Homework 3

1.  (6 points) What the probability that a 5 card hand contains exactly
    3 spades? What if we condition on the hand containing at least 1
    spade?

2.  (7 points) Suppose \\(n\\) people each throw a six-sided die. Let \\(A_n\\)
    be the event that at least two distinct people roll the same number.
    Calculate \\(P(A_n)\\) for \\(n=1,2,3,4,5,6,7\\).

3.  (3 points) Suppose we draw 2 balls at random from an urn that
    contains 5 distinct balls, each with a different number from
    \\(\{1,2,3,4,5\}\\), and define the events \\(A\\) and \\(B\\) as
    \\(\\)A = \text{"5 is drawn at least once"} \quad \text{and} \quad
    B = \text{"5 is drawn twice"}\\(\\) Compute \\(P(A)\\) and \\(P(B)\\).

4.  (4 points) In the previous problem, suppose we place the first ball
    back in the urn before drawing the second. Compute
    \\(P(A),P(B),P(A|B),P(B|A)\\) in this version of the experiment.

5.  (4 points) Suppose \\(5\\) percent of cyclists cheat by using illegal
    doping. The blood test for doping returns positive \\(98\\) percent of
    the people doping and \\(12\\) percent who do not. If Lance’s test comes
    back positive, what the probability that he is doping? (Ignoring all
    other evidence, of course...)

6.  (6 points) If \\(A \subseteq B\\), can \\(A\\) and \\(B\\) be independent? What
    we if require that \\(P(A)\\) and \\(P(B)\\) both not equal \\(0\\) or \\(1\\)?

7.  **Extra credit (5 points)** Consider the experiment where two dice
    are thrown. Let \\(A\\) be the event that the sum of the two dice is 7.
    For each \\(i \in \{1,2,3,4,5,6\}\\) let \\(B_i\\) be the event that at
    least one \\(i\\) is thrown.

    1.  Compute \\(P(A)\\) and \\(P(A|B_1)\\).

    2.  Prove that \\(P(A|B_i) = P(A|B_j)\\) for all \\(i\\) and \\(j\\).

    3.  Since you know that some \\(B_i\\) always occurs, does it make sense
        that \\(P(A) \neq P(A | B_i)\\)? (After all, if \\(E\\) is an event with
        \\(P(E) = 1\\), then for any event \\(F\\), \\(P(F|E) = P(F)\\). What is
        going on? Does this seem paradoxical?)

## February 20th, 2013 - Lecture: Independence

### Topics

- Multiplication rule for conditional probability. 
- Independent events: two equivalent definitions and several examples with cards and dice. 
- People v. Collins and the prosecutor's fallacy. 
- Mutual independence.
	
### Multiplication Rule for Conditional Probability

- **Example**: Hat contains 3 cards, RR, RB, BB. Pick a card, put it on table, see a R side, what's the probability the other side is B?
	+ Wrong: 1/2
	+ Right: 1/3

- If E_1 through E_2 are events, all P(E_i) do not equal zero,
\\[P(E_1 \cap E_2 \cap ... \cap E_n) = \\]
\\[P(E_1) \times P(E_2 | E_1) \times ... \times P(E_n | E_1 \cap ... \cap E_{n-1}) \\]
	+ This might be easier to express as the intersection of smaller events.
	+ This is really easy thing to prove.
	+ "Proves itself."
	+ **Proof**:
		1. \\(P(E_1) \times \frac{P(E_2 \cap E_1)}{P(E_1)} \times ... \times \frac{P(E_1 \cap ... \cap E_n)}{P(E_1 \cap ... \cap E_{n-1}})\\)
		2. Cancel. Beautiful cancellation.
	+ This allows you to say, what happens when the first once happens? And now, what about the second one? So on so forth.
	+ **Example**: What is the probability of a five card hand not containing a pair?
		* E_i = "first i cards in hard do not contain a pair"
		* *Claim*: What we want is \\(E_1 \cap E_2 \cap ... \cap E_5 \\)
		* What's funny about this is that we don't want E_1 through E_4, we are actually only interested in E_5.
		* The reason we do this, however, is because it makes this calculation easier.
		* Possibilities:
			1. \\(P(E_1) = 1 \\)
				* The probaility of the first hand not being a pair is 1, because it's one card.
			2. \\(P(E_2 | E_1) = \frac{48}{51} \\)
			3. \\(P(E_3 | E_1 \cap E_2) = \frac{44}{50} \\)
			4. \\(P(E_4 | E_1 \cap ... \cap E_3) = \frac{40}{44} \\)
			5. \\(P(E_5 | E_1 \cap ... \cap E_4) = \frac{36}{48} \\)
		* Multiply these values together to get 50.7%.
		
### Independence

- **Definition**: Say events E and F are independant if \\(P(E \cap F) - P(E) \times P(F) \\).
	+ **Equivalent definition**: E and F are independent i(P(F) = 0 or P(E|F) = P(E)\\).
	+ **Proof**:
		1. Take E and F set \\(P(E \cap F) = P(E) \times P(F) \\).
		2. If \\(P(F) = 0 \\), then done.
		3. If not, then \\(P(E|F) = \frac{P(E \cap F)}{P(F)}\\)
- **Exercise**: Toss two coins
	+ E = "1st coin was H"
	+ F = "2nd coin was H"
	+ P(E) = P(F) = 1/2
- **Exercise**: Tossing two dice
	+ E = "sum of dice is 6"
	+ F = "first die was 4"
	+ \\(P(E) = P(\lbrace(1,5),(2,4),(3,3),(4,2),(5,1)\rbrace) = \frac{5}{36}\\)
	+ P(F) = 1/6
	+ \\(P(E \cap F) = P(\lbrace(4,2)\rbrace) = \frac{1}{36} \\)
	+ \\(P(E) \times P(F) = \frac{5}{36} \times \frac{1}{6} \\)
- **Exercise**: Suppose a family has 3 kids.
	+ E = "family has at least 1 boy and 1 girl"
	+ F = "family has at most 1 boy"
	+ Are these indepedant?
		* \\(S = \lbrace BBB, BBG, BGB, GBB, BGG, GBG, GGB, GGG\rbrace\\)
		* \\(E = S - \lbrace BBB, GGG \rbrace \\)
		* \\(F = \lbrace BGG, GBG, GGB, GGG \rbrace \\)
		* \\(E \cap F = \lbrace BGG, GBG, GGB \rbrace \\)
		* \\( P(E \cap F) = \frac{3}{8} \\)
		* \\( P(E) \times P(F) = \frac{3}{4} \times \frac{1}{2} = \frac{3}{8} \\)
		* Therefore, independent.
		
#### "Independent" and "Mutually Exclusive" are not the same

- **Example**: 2 dice
	+ E = "sum was 6"
	+ F = "first die was 6"
	+ E and F are not mutually exclusive, but not independent.
	
#### Prosecutor's Fallacy: People v. Collins (1968)

- The prosectution came up with these numbers:
	+ The probability of a black man with a beard is 1 in 10 
	+ The probability of a man with a mustache is 1 in 4
	+ White woman with ponytail is 1 in 10
	+ So on so forth, 1 in 3, 1 in 10, 1 in 1000
	+ So he made this calculation:
	\\[\frac{1}{10} \times \frac{1}{4} \times \frac{1}{10} \times \frac{1}{10} \times \frac{1}{3} \times \frac{1}{1000} = \frac{1}{12 \times 10^6} \\]
	+ *Say* that the population of LA was \\(24 \times 10^6\\)
	+ Then, you'd "expect" to have 2 couples fitting this evidence.
	+ P(evidence | innocent) \\(\neq\\) P(innocent | evidence) 

#### With 3 events

- E is indepedant of F and G
- F is indepedant of G
- Then is E indepedant of F intersect G?
- **Example**: rolling two die
	+ E = "sum to 7"
	+ F = "first die was 4"
	+ G = "second die was 3"
	\\[P(E | F \cap G) = 1\\]
	\\[P(E) = \frac{1}{6} \\]
	+ **Definition**: E, F, and G are independant (alternatively "mutually independant") if:
	\\[P(E \cap F) = P(E) \times P(F) \\]
	\\[P(E \cap G) = P(E) \times P(G) \\]
	\\[P(F \cap G) = P(F) \times P(G) \\]
	\\[P(E \cap F \cap G) = P(E) \times P(F) \times P(G) \\]

#### With n events

- **Definition**: \\(E_1, ..., E_n \\) are indepedant if for every subset \\(I \subseteq \lbrace 1, 2, ..., n \rbrace\\) of at least size 2
- **Example**: Flip n coins

## February 20th, 2013 - Recitation

- Proove:
\\[{n \choose n_1 \cdot n_2 \cdot ... \cdot n_r} = \\]
[[[{n-1 \choose n_1 - 1 \cdot ... \cdot n_r} + ... + {n-1 \choose n_1 \cdot ... \cdot n_{r-1} \cdot n_{r-1} \\]

## February 20th, 2013 - Reading

### Ross 3.3

### Rose 3.4. 

### Optional: People v. Collions court opinion. 

### British case involving Sally Clark.