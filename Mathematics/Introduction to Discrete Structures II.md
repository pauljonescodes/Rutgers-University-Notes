Discrete Structures II <small>with Professor David Cash</small>
===============================================================

Description
-----------

Provides the background in combinatorics and probability theory required
in design and analysis of algorithms, in system analysis, and in other
areas of computer science.

-   Topics:
    -   Counting: Binomial Coefficients, Permutations, Combinations,
        Partitions.
    -   Recurrence Relations and Generating Functions.
    -   Discrete Probability:
        -   Events and Random Variables;
        -   Conditional Probability, Independence;
        -   Expectation, Variance, Standard Deviation;

    -   Binomial, Poisson and Geometric Distributions;
    -   law of large numbers.
    -   Some Topics from Graph Theory:
        -   Paths,
        -   Components,
        -   Connectivity,
        -   Euler Paths,
        -   Hamiltonian Paths,
        -   Planar Graphs,
        -   Trees.

Syllabus
--------

### Course Overview

This course is an introduction to *probability* and *combinatorics*,
including their basic mathematical foundations as well as several
non-trivial applications of each. The first topic explores how to think
about *random processes* in a rigorous and sensical way, and second is
about techniques for *counting* the number of objects fitting a given
description. As we will see, the techniques involved in both topics are
strongly related.

Roughly, we expect to cover the following list of topics. Lecture
summaries will be posted at the bottom of this page.

-   Review of prerequisites, set theory, countability
-   Random experiments, sample spaces, events, probability measures
-   Conditional probability, Bayes' Theorem, Independence
-   Combinatorics and Counting
-   Recurrences, Generating Functions
-   Random Variables
-   Bernoulli Trials
-   Expectation, Variance
-   Markov Chains
-   Applications of Probability and Combinatorics

### General Information

-   Instructor: [David Cash](david.cash@cs.rutgers.edu)
-   [Course
    website](http://www.research.rutgers.edu/~dc789/206-spring-13/index.html)
-   Recommended textbooks:
    -   S. Ross, *A First Course in Probability, 8th Edition*
    -   H. Rosen, *Discrete Mathematics and its Applications, 7th
        edition*

-   Lecture meetings: Monday and Wednesday 5:00pm -- 6:20pm in Hill 116
-   Recitations:
    -   Section 1: Monday 6:55pm -- 7:50pm in SEC 220
    -   Section 2: Wednesday 6:55pm -- 7:50pm in ARC 110
    -   Section 3: Monday 8:25pm -- 9:20pm in Hill 120

-   Instructor office hours: Tuesday 1:30pm-3:00pm in Hill 411 and by
    appointment
-   Teaching assistant: TBA (TAB@cs.rutgers.edu)
-   Teaching assistant office hours: TBA in TBA and by appointment

### Assignments and Grading

Homework will be assigned roughly every 1.5 weeks. There will be one
in-class midterm and one final exam. Final grades will be an average of
homework grades (30%), midterm grades (30%), and final exam grades
(40%).

January 23rd, 2012 - Lecture: Introduction
------------------------------------------

### Topics

-   Review of sets and induction.
-   Samples spaces and events.

### Introduction

-   This title of this class is funny because it tells you nothing about
    it.
-   What this class is really about is **discrete probability** and
    **combinatorics**.
    -   Discrete means "not continuous."
    -   Probability means about change and percentage.
    -   Combinatorics is the study of combining things.
    -   More specifically, it is the study of counting the number of
        discrete objects fitting some description.

-   Probability in computer science
    -   Random number generator (RNG)
    -   Average case algorithms
    -   Information security and cryptography
    -   Networking, TCP/IP

### Formalizaing Probability

-   A set is a collection of objects. Ex:
    -   $S = {a, b, c} $
    -   $ \mathbb{N} = 1, 2, 3, … $ (natural numbers)
    -   $ \mathbb{Z} = {…, -2, -1, 0, 1, 2, …} $ (integers)

-   Notation:
    -   $\emptyset = {} $
    -   Write `{x |` "statement about `x}`" to mean all `x` satisfying
        statement.

-   Relations between sets
    -   `A` and `B` are sets.
    -   $A \subseteq B $ means "`A` is a subset of `B`"
    -   $B \subseteq A $ means "`A` is a superset of `B`"

-   Operations on sets
    -   $ A \cup B $ means "union of `A` and `B`"
    -   $ A \cap B $ means "intersection of `A` and `B`"
    -   $ A \setminus B $ means "set difference of `A` and `B`" which
        means everything in `A` that is not in `B`
    -   When a "universe" is understood, we can define $A^{c}$ as the
        "complement" of `A`

-   Set identities $$ A \cup (B \cap C) = $$
    $$(A \cup B) \cap (A \cup C)$$
    $$A \cap (B\cup C) = (A\cap B) \cup (A \cap C)$$
    -   Prove: $(A \cup B)^{c} = A^c \cap B^c $
        1.  Show: $(A \cup B)^{c} \subseteq A^c \cap B^c $
        2.  Show: $A^c \cap B^c \subseteq (A \cup B)^{c}$

    -   A good way to remember these is to use Venn diagrams.

-   DeMorgan's laws
-   Proofs by Induction
    -   Let's say you want to prove a statement for all natural numbers
        `n`.
    -   For example, for all `n > 0`, $\sum_{i=0}^{n}2^i = 2^{n + 1}$
        -   Call the statements $s\_0, s\_1, s\_2, … $
        -   Suppose it's not true for all of them.
        -   Key obeservation: If they're not all true, then there is a
            smallest `i` such that $S_i$ is false.

    -   A proof by induction works in 2 steps:
        1.  Prove statement for first `n`
        2.  Give a conditional proof, prove that for all `n`, if
            $S_{n-1}$ is true, then $S_{n}$

-   Countability
    -   A set `S` is countable if it is finite, or if it can be pun in
        one-to-one correspondence with the natural numbers.

-   Sample space
    -   Fix a "sample space" that represents everything that could
        happen in our random experiment
    -   A sample space is always a set
    -   Examples of samples spaces
        1.  Tossing a coin: $ S = (H, T) = ({0, 1})$
        2.  Tossing two coins: $S = ({HH, HT, TH, TT}) $
        3.  Rolling a die: $ S = ({1, 2, 3, 4, 5, 6})$
        4.  Rolling 2 dice: $ S = ((i, j) | $ i, j in$
            (1,2,3,4,5,6))$

January 23rd, 2013 - Reading
----------------------------

### 2.1 Introduction

> In this chapter, we introduce the concept of the probability of an
> event and then show how probabilities can be computed in certain
> situations. As a preliminary, however, we need the concept of the
> sample space and the events of an experiment.

### 2.2 Sample Space and Events

-   The set of all possible outcomes of an experiment is known as the
    **sample space** of the experiment and is denoted by S. Examples:
    1.  The sex of a newborn child: S = {g, b}
    2.  Horse race with seven horses: S = {all 7! permutations of (1, 2,
        3, 4, 5, 6, 7)}
    3.  Flipping two coins: S = {(H, H), (H, T), (T, H), (T, T)}
    4.  Tossing two dice: S = {(i, j): i, j = 1, 2, 3, 4, 5, 6}

-   Any subset E of the sample space is known as an **event**. For the
    previous examples,
    1.  E = {g} would be having a girl.
    2.  E = {all outcomes in S beginning with 3} would be 3 winning the
        race.
    3.  E = {(H, H), (H, T)} would be an event where you get heads
        first.
    4.  E = {(1, 6), (2, 5), (3, 4), (4, 3), (5, 2), (6, 1)} would be an
        event where the sum of the two rolls is seven.

-   A **union** of any two events E and F results in an event with all
    outcomes in both E and F.
-   An **intersection** of any two events E and F results in a event
    with only those outcomes in both E and F.
-   If E and F share no outcomes, making their intersection the empty
    set (denoted by $\emptyset$, they are said to be **mutually
    exclusive**.
-   The complement of E is defined as all events not in E that are in
    the sample space, denoted by $ E^c $.

January 28th, 2013 - Lecture: Probability Measures
--------------------------------------------------

### Announcements

-   Recitation starts this week.
-   Homework 1 will be out tonight and due in a week.

### Topics

-   Operations on events.
-   Abstract definition of probability measure.
-   Equivalent definition for countable sample spaces.
-   Basic consequences of the definition.

### Probability

-   Sample space = any set
-   "Event" = an subset of the sample space
-   Fix a sample space `S`
-   Take any events $ E \subseteq S, E\_2 S $
-   Consider the set $ E\_1 \cup E\_2 \subseteq S $
-   Example: Flip two coins
    -   $ S = HH, HT, TH, TT $
    -   $ E\_1 = HT, HH $
    -   $ E\_2 = TH, HH $
    -   $ E\_1 \cup E\_2 = HT, HH, TH $ = "heads came up", "either
        heads came up on the 1st or 2nd toss"
    -   $ E\_1 \cap E\_2 = HH $

-   Example: Rolling a die
    -   $ E\_1 = $ "die was rolled" = {1, 3, 5}
    -   $ E\_2 = $ "die roll was divisible by 3" = {3, 6}
    -   $ E\_1 \cap E\_2 = 3$

-   Note: If $E\_1 = \emptyset $ and $ E\_2$ is any event, then $
    E\_1, E\_2$ are mutually exclusive.
-   Complement: If E is an event, then so is $ E^c \subseteq s $
    means "not E" or "E didn't happen."
    -   For the example of the two coins,
        -   E = "1st coin was heads" means that $ E^c = TH, TT $

-   If $ E\_1 \subseteq E\_2 $, then what can we say?
    -   Proposal: If E1 happened then E2 also happened.
    -   Example: two dice:
        -   First event: "a one was rolled" = {1}
        -   Second event: "the dice summed to 3" = {(1,2),(2,1)}
        -   The second event is a subset of the first event.

### Probability measures

-   We've been talking about whether or not something happened, but
    we'll now move to how *likely* it is for something to happen.
-   We want to assign to even event a number between zero and one
    represent how "likely" that event is.
    -   We are going to assume things about randomness and
        predictibility, we quickly get into philosophy otherwise.

-   We want a function P that givens the probabilty P(E) for every E $
    \subseteq $ S
-   Example: A coin flip
    -   S = {H, T}
    -   P({H}) = 1/2
    -   P({T}) = 1/2
    -   P({H, T}) = 1
    -   P( $ \emptyset $ ) = 0

-   Example: Tossing two coins
    -   S + {HH, HT, TH, TT}
    -   P({HH}) = 1/4 (and for HT, TH, ... )
    -   If E $ \subseteq $ S, P(E) = $\frac{|E|}{|S|} $

-   Definition: A function P is a probability measure if it maps every
    event E $ \subseteq $ S to a number and satisfies the following
    three rules:
    1.  For every E, O \<= P(E) \<= 1
    2.  P(S) = 1
    3.  Countable additivity
        -   For every sequence $ E\_1, E\_2, ... $ of event, if the $
            E\_i$ are all mutually exlcusive, so $E\_i \cap E\_j =
            \emptyset $
            $$ P\left(\bigcup_{i=1}^\infty E_i\right)=\sum_{i=1}^\infty P(E_i) $$

-   Claim: If P is a probabilty measure, then P($ \emptyset $ ) = 0
    -   Proof: Take $ E\_1, E\_2, ... $ where $ E\_i = \emptyset $
        for every i. The sequence is mutually exclusive.

-   When S is finite, we can replace (3) with the "finite additivity":
    \> $ P \left(\bigcup*{i = 1}^n E\_1 \right) = \sum*{i = 1}^n
    P(E\_i) $
-   Definition: If S is countable then we can say that P is discrete.
    -   Every sample set in this class will be countable.

-   Claim: If P is discrete, then it is completely determined by its
    value on one-element sets.
-   If you know that P({x}) for every $ x \in S $, then you know that
    P(E) for every E $ \subseteq $ S
-   Write E = {$ x\_1, x\_2, ... $} Let $ E\_i = x\_i $
    -   The $E\_i $ are mutually exclusive.
    -   $ \bigcup\_{i = 1}^\infty E\_1 = E $
    -   So by rule 3,

January 28th, 2013 - Reading
----------------------------

### 2.3 Axioms of Probability

-   One way of defining probability is in relative frequency.
-   For some event E in sample space S, we define n(E) to be the number
    of times in the first n repetitions of the experiment that the event
    E occurs. Therefore, $P(E) = \lim\_{x \to \infty}\frac{n{E}}{n} $
-   While intuitive, how do we know that n(E)/n will converge to some
    constant limiting value that will be the same for each possible
    sequence of repetitions of the experiment?
    -   Proponents of this definitions say that this is an "axiom" of
        the system, an assumption.
    -   Critics say that this is too complicated an assumption.

-   Would it not be more reasonable to assume a set of simpler and more
    self-evident axioms about probability and then attempt to prove that
    such a constant limiting frequency does in some sense exist?
-   Axioms:
    1.  $ 0 \le P(E) \le 1 $
        -   The probability that the outcome of the experiment is an
            outcome in E is some number between 0 and 1

    2.  $ P(S) = 1 $
        -   The outcome will be a point in the sample space S

    3.  $
        P\left(\bigcup\_{i=1}^\infty E\_i\right)=\sum\_{i=1}^\infty P(E\_i)
        $
        -   For any sequence of mutually exclusive events, the
            probability of at least one of these events occurring is
            just the sum of their respective probabilities.

### 2.4 Some simple propositions (through proposition 4.3)

-   Proposition 4.1: $$ P(E^c) = 1 − P(E) $$
-   Proposition 4.2: $$ If E \subset F, then P(E) \le P(F). $$
-   Proposition 4.3: $$ P(E \cup F) = P(E) + P(F) − P(EF) $$

January 28th, 2013 - Homework 1
-------------------------------

1.  Let $n\geq 2$ and $A_1,\ldots,A_n$ be sets in some universe S. In
    this problem we will give a proof by induction of the identity
    $$ \left(\bigcap_{i=1}^n A_i\right)^c = \bigcup_{i=1}^n A_i^c. $$
    1.  (5 points) State and prove the base case for an inductive proof,
        meaning that the identity is true when $n=2$.
        1.  $\left(\bigcap_{i=1}^2 A_i\right)^c = \bigcup_{i=1}^2 A_i^c$
        2.  $ \left(A\_1 \bigcap A\_2 \right)^c = A\_1^c
            \bigcup A\_2^c$ is true by DeMorgan’s

    2.  (5 points) State and prove the inductive step, where one shows
        that the identity is true for general $n>2$, assuming it is true
        for $n-1$.
        1.  $ \left(\bigcap*{i=1}^n A\_i\right)^c = \bigcup*{i=1}^n
            A\_i^c $ assume true for n
        2.  $ \left(\bigcap*{i=1}^{n - 1} A\_i\right)^c =
            \bigcup*{i=1}^{n - 1} A\_i^c $ induction for n - 1
        3.  $\bigcup*{i = 1}^n A\_i^c \cup A*{n + 1}^c = $
            $$ \left( \bigcap_{i = 1}^n A_i \right) \cup A_{n + 1}^c$$
        4.  $\left(\bigcap*{i=1}^n A\_i\right)^c = $ $$ \left(
            \bigcap*{i = 1}^n A\_i \right) \cup A\_{n + 1}^c$

2.  Give sample spaces that model the outcomes for the following
    experiments. You may use a regular expression or other formalisms
    that you find convenient. (2 points each)
    1.  Rolling 3 dice. $$S = \lbrace (i,j,k) \: | \: i,j,k \in $$
        $$\lbrace 1, 2, 3, 4, 5, 6 \rbrace \rbrace  \!\,$$
    2.  Rolling a die until an even result comes up, or the die is
        rolled three times.
        $$S = \lbrace  ( i ) , ( j , i ), (  j , j , \lbrace i,j\rbrace  ) \: |$$
        $$ \: i \in \lbrace 1,2,4\rbrace , j \in \lbrace 1,3,5\rbrace  \rbrace  $$
    3.  Tossing a pair of coins until they both come up tails.
        $$S = \lbrace  (e_1), (e_2,e_1), (e_2,e_2,e_1), $$
        $$(e_2,e_2,e_2, ..., e_1) \: | $$
        $$e_1 = TT, e_2 \in \lbrace HT, TH, HH\rbrace \rbrace $$
    4.  Draw 2 balls from an urn which contains 6 balls, each with a
        distinct label from $\lbrace 1,2,3,4,5,6\rbrace $.
        $$S = \lbrace i,j \: | \: i,j \in \lbrace 1,2,3,4,5,6\rbrace $$
        $$  \land i \neq j \rbrace $$
    5.  Draw 1 ball from the same urn, then replace it and draw a ball
        again. $$S = \lbrace (i,j) \: | $$
        $$\: i,j \in \lbrace 1,2,3,4,5,6\rbrace \rbrace $$

3.  For each of the sample space, describe the events (as sets)
    $A\cup B$ and $A \cap B$, when A and B are as follows. (2 points
    each)
    1.  A = "5 is rolled exactly twice" and B = "dice values add to an
        odd number".
        $$A \cup B = \lbrace  \lbrace i, i, i\rbrace , \lbrace j, j, i\rbrace  \: | $$
        $$ \: i \in \lbrace 1, 3, 5 \rbrace , j \in \lbrace 2, 4, 6\rbrace \rbrace  $$
        $$A \cap B = \lbrace \lbrace 5, 5, i\rbrace  \: \mid $$
        $$ \: i \in \lbrace 1,3\rbrace \rbrace  $$
    2.  A = "1 comes up exactly twice" and B = "3 comes up exactly
        twice".
        $$A \cup B = \lbrace (1,1,i), (j, 1, 1), (1, j, 1) \: | $$
        $$ \: i \in \lbrace 2,3,4,5,6\rbrace  $$
        $$\land j \in \lbrace 3,5\rbrace  \rbrace  $$
        $$\cup \lbrace (3,3,i), (j, 3, 3), (3, j, 3) \: | $$
        $$ \: i \in \lbrace 1,2,4,5,6\rbrace $$
        $$\land j \in \lbrace 1,5\rbrace  \rbrace  $$
        $$A \cap B = \emptyset $$
    3.  A = "both coins come up heads at the same time at some point"
        and B = "both coins come up tails at the same time at some
        point," $$A \cup B = S = $$
        $$\lbrace  (e_1), (e_2,e_1), (e_2,e_2,e_1), (e_2,e_2,e_2, ..., e_1) \: $$
        $$| \:e_1 = TT, e_2 \in \lbrace HT, TH, HH\rbrace \rbrace $$
        $$A \cap B = A = \lbrace  (e_1, e_2, e_3, ... , e_n) \: $$
        $$\mid \: e_n = TT \land e_i \in \lbrace HT, TH, HH\rbrace $$
        $$ \land 1 \le i \le n - 1 \land $$
        $$ n \in N \land \exists j e_j = HH $$
        $$\land 1 \le j \le n - 1 \rbrace $$
    4.  A = "1 is drawn at least once" and B = "1 is drawn twice".
        $$A\cup B = A = \lbrace \lbrace i,j\rbrace  \: | $$
        $$\: i,j \in \lbrace 1,2,3,4,5,6\rbrace  \land $$
        $$(i \neq j) \land (i = 1 \oplus j = 1) \rbrace  $$
        $$A \cap B = \emptyset $$
    5.  A = "1 is drawn at least once" and B = "1 is drawn twice"
        $$A \cup B = \lbrace \lbrace 1,1\rbrace ,\lbrace 1,2\rbrace ,\lbrace 1,3\rbrace$$
        $$ ,\lbrace 1,4\rbrace ,\lbrace 1,5\rbrace ,\lbrace 1,6\rbrace \rbrace $$
        $$A \cap B = \lbrace \lbrace 1,1\rbrace \rbrace  $$

January 30th, 2013 - Lecture: Begin counting and its applications
-----------------------------------------------------------------

### Topics

-   Finish proof about probability of a union.
-   Counting: The multiplication rule, permutations of n objects and
    k-out-of-n objects.
-   The birthday problem.
-   Permutations when some objects are indistinguishable.
-   Counting walks on grids.

### Introduction

-   Claim: If P is a probability measure on S and $ E \subseteq S $,
    $F \subseteq S $ are events, then $ P(E \cup F) = P(E) + P(F) -
    P(E \cap F) $. Proof:
    -   $P( E \cup F)$
        -   The first step in a lot of these proofs is to "disjointify"
            $E \cup F $
        -   The handy way to do this is to write that as $ E \cup (E^c
            \cap F) = P(E) + P(E^c \cap F)$

    -   Now we need $ P(E^c \cap F) = P(F) - P(E \cap F) $
        -   Equivilently, $P(F) = P(E \cap F) + P(E^c \cap F) $. This
            is true because:
            -   $ F = (E \cap F) \cup (E^c F) $
            -   $ E \cap F $ and $ E^c \cap F $ are mutually
                exclusive.

### Counting

-   Multiplication rule: If I have $n\_1 $ choices in an experiment,
    and if I have for each of my first choices another $n_2$ choices,
    and the same $n_3$ choices, up to $n_r$. In that setting, then I
    have $ n\_1 \times n\_2 \times n\_3 \times ... \times n\_r $ total
    choices.
    -   Example: How many license plate numbers are there if they
        consist of 6 characters, the first six being letters and the
        last three being numbers? (ABX 161)
        -   26 choices for first letter
        -   26 choices for the second letter
        -   26 choices for the third letter
        -   10 choices for the first number
        -   10 choices for the second number
        -   10 choices for the third number
        -   Therefore, 26 x 26 x 26 x 10 x 10 x 10 =

    -   Example: What if no repetitions are allowed?
        -   26 possibilities
        -   25 possibilities
        -   24 possibilities
        -   10 possibilities
        -   9 possibilities
        -   8 possibilities
        -   26 x 25 x 24 x 10 x 9 x 8 =

-   Permutations: "How many ways can I arrage n distinct objects in a
    line? (i.e. in order)
    -   Answer: Build an arrangement by picking 1st element, then 2nd
        element, etc, euntil nth.
    -   Definition: n! = n(n + 1) ... x 2 x 1
        -   0! = 1 (There is only one way to arrange zero items)

    -   What is we only arrange k \< n of the objects?
        -   $n - k + 1 = \frac{n!}{(n - k)!} $

    -   Example: A class of 6 men and 4 women
        1.  How many ways can they be ranked?
            -   10!

        2.  What if you rank men and women seperately?
            -   6! + 4!

    -   Birthday "Paradox" (Surprise)
        -   Assume birthdays are random, you can be born on any day, and
            ignore February 29th.
        -   What is the size of the group required to give us a 50%
            chance of getting a match?
        -   Use your intuition: There are 365 days, so probably around
            1/365?
        -   You'd expect 100 people, 200 people, once you approach half
            the number of days.
        -   Let's study this using our probability.
        -   Take n people, n random birthdays.
        -   Sample space will be S = {1, ..., 365}^n
        -   $ E \subseteq S $ represents "there is at least one match"
        -   $ P(E) = 1 - P(E^c) $
        -   It's kind of hard to account for E, with multiple matches,
            all matches, etc.
        -   The complement of E is "there are no matches."
        -   How big is E complement?
        -   $ E^c \subseteq S $ is a lists of n numbers without
            match.
        -   $ |E^c| = 365 \times 364 \times 363 \times (365 - n + 1)
            $
        -   $ P(E^c) = \frac{|E^c|}{|S|} =
            \frac{365 \times 364 \times 363 \times (365 - n + 1)}{365^n}
            $
        -   $ \approx .507 | n = 23 $
        -   $ \approx .97 | n = 50 $
        -   $ \approx \> .999999 | n = 100 $
        -   Intuition: It's not the number of people that matters, it's
            the number of pairs, $O(n^2)$ type of growth.

-   How many distinct strings can be formed from the letters in
    "remember"? Answer:
    -   There are 8! ways to arrange the letters in total.
    -   There are 3! ways to arrange the Es without changing the word.
    -   There are 2! ways to arrange the Rs without changing the word.
    -   There are 2! ways to arrange the Ms without changing the word.
    -   There is 1 way to rearrange the B without changing the word.
    -   $\mathrm{R_1 E_1 M_1 E_2 M_2 B_1 E_3 R_2} $
    -   $ \frac{8!}{3!\times 2!\times 2! \times 1!} $
    -   How many times does "remember" show up in the list?
    -   Permutations when some elements are interchangable: When putting
        n objects in order if n\_1 are interchangabl and N\_2 are
        interchangable, and ..., n\_r are interchangable, the number of
        permutations $ \frac{n!}{n_1!n_2! ... n_r!} $

January 30th, 2013 - Recitation
-------------------------------

1.  Give an inductive proof of the identity: $
    \left(\bigcup*{i=1}^{n}\right)^c =
    \bigcap*{i=1}^n\left(A\_i^c\right)$. You may use the fact that for
    any two sets A and B, $(A \cup B)^c = A^c \cap B^c $.

2.  What are the sample spaces for the following experiments?
    -   Throwing three dice
    -   Flipping a coin until either (a) "heads" occurs, or (b) the coin
        is flipped 8 times.
    -   Throwing a die until "6" occurs.
    -   Drawing 2 balls from an urn, where the urn contains 5 balls,
        each with a distinct label from 1 to 5.
    -   Picking one ball from the same urn as above, and then putting it
        back into the urn and again picking a ball.

3.  Which of the sample spaces from Exercise 2 are finite? Which are
    countable? (Justify your answers.)
4.  For the sample spaces you presented in Exercise 2, describe the
    events $A \cup B $ and $A \cap B$ when A and B are:
    -   A = "at least one 6" and B = "an odd total".
    -   A = "heads occurs twice" and B = "tails occurs twice"
    -   A = "5 occurs an infinite number of times" and B = "6 occurs"
    -   A = "5 is drawn at least once" and B = "5 is drawn twice"
    -   A = "5 is drawn at least once" and B = "5 is drawn twice"

January 30th, 2013 - Reading
----------------------------

### 1.2 The Basic Principle of Counting

> The basic principle of counting will be fundamental to all our work.
> Loosely put, it states that if one experiment can result in any of m
> possible outcomes and if another experiment can result in any of n
> possible outcomes, then there are mn possible out- comes of the two
> experiments.

-   **The basic principle of counting**: Suppose that two experiments
    are to be performed. Then if experiment 1 can result in any one of m
    possible outcomes and if, for each outcome of experiment 1, there
    are n possible outcomes of experiment 2, then together there are mn
    possible out- comes of the two experiments.
-   **The generalized basic principle of counting**: If r experiments
    that are to be performed are such that the first one may result in
    any of n1 possible outcomes; and if, for each of these n1 possible
    outcomes, there are $n_2$ possible outcomes of the second
    experiment; and if, for each of the possible outcomes of the first
    two experiments, there are $n_3$ possible outcomes of the third
    experiment; and if ..., then there is a total of $n\_1 \cdot n\_2 …
    n\_r $ possible outcomes of the r experiments.

#### Example 2a

-   A small community consists of 10 women, each of whom has 3 children.
    If one woman and one of her children are to be chosen as mother and
    child of the year, how many different choices are possible?
-   Solution. By regarding the choice of the woman as the outcome of the
    first experiment and the subsequent choice of one of her children as
    the outcome of the second experiment, we see from the basic
    principle that there are $10 \times 3 = 30$ possible choices.

#### Example 2b

-   A college planning committee consists of 3 freshmen, 4 sophomores, 5
    juniors, and 2 seniors. A subcommittee of 4, consisting of 1 person
    from each class, is to be chosen. How many different subcommittees
    are possible?
-   Solution. We may regard the choice of a subcommittee as the combined
    outcome of the four separate experiments of choosing a single
    representative from each of the classes. It then follows from the
    generalized version of the basic principle that there are $3
    \times 4 \times 5 \times 2 = 120 $ possible subcommittees.

#### Example 2c

-   How many different 7-place license plates are possible if the first
    3 places are to be occupied by letters and the final 4 by numbers?
-   Solution. By the generalized version of the basic principle, the
    answer is
    $26 \times 26 \times 26 \times 10 \times 10 \times 10 \times 10=175,760,000$.

#### Example 2d

-   How many functions defined on n points are possible if each
    functional value is either 0 or 1?
-   Solution. Let the points be 1,2,...,n. Since $f(i)$ must be either 0
    or 1 for each i = 1, 2, . . . , n, it follows that there are $2_n$
    possible functions.

#### Example 2e

-   In Example 2c, how many license plates would be possible if
    repetition among letters or numbers were prohibited?
-   Solution. In this case, there would be
    $26 \times 25 \times 24 \times 10 \times 9 \times 8 \times 7 = 78,624,000$
    possible license plates.

### 1.3 Permutations

-   How many different ordered arrangements of the letters a, b, and c
    are possible?
-   By direct enumeration we see that there are 6, namely, abc, acb,
    bac, bca, cab, and cba.
-   Each arrangement is known as a **permutation**. Thus, there are 6
    possible permutations of a set of 3 objects.

$n(n − 1)(n − 2) … 3 \times 2 \times 1 = n!$

#### Example 3a

-   How many different batting orders are possible for a baseball team
    consisting of 9 players?
-   Solution. There are 9! = 362,880 possible batting orders.

#### Example 3b

-   A class in probability theory consists of 6 men and 4 women. An
    examination is given, and the students are ranked according to their
    performance. Assume that no two students obtain the same score.
    1.  How many different rankings are possible?
    2.  If the men are ranked just among themselves and the women just
        among themselves, how many different rankings are possible?

-   Solution.
    1.  Because each ranking corresponds to a particular ordered
        arrangement of the 10 people, the answer to this part is 10! =
        3,628,800.
    2.  Since there are 6! possible rankings of the men among themselves
        and 4! possi- ble rankings of the women among themselves, it
        follows from the basic principle that there are (6!)(4!) =
        (720)(24) = 17,280 possible rankings in this case.

#### Example 3c

-   Ms. Jones has 10 books that she is going to put on her bookshelf. Of
    these, 4 are mathematics books, 3 are chemistry books, 2 are history
    books, and 1 is a language book. Ms. Jones wants to arrange her
    books so that all the books dealing with the same subject are
    together on the shelf. How many different arrangements are possible?
-   Solution. There are 4! 3! 2! 1! arrangements such that the
    mathematics books are first in line, then the chemistry books, then
    the history books, and then the language book. Similarly, for each
    possible ordering of the subjects, there are 4! 3! 2! 1! possible
    arrangements. Hence, as there are 4! possible orderings of the
    subjects, the desired answer is 4! 4! 3! 2! 1! = 6912.

#### Example 3d

-   How many different letter arrangements can be formed from the
    letters PEPPER?
-   Solution. We first note that there are 6! permutations of the
    letters $P_1E_1P_2P_3E_2R$ when the 3P’s and the 2E’s are
    distinguished from each other. However, consider any one of these
    permutations—for instance, P1P2E1P3E2R. If we now permute the P’s
    among themselves and the E’s among themselves, then the resultant
    arrangement would still be of the form PPEPER.

#### Example 3e

-   A chess tournament has 10 competitors, of which 4 are Russian, 3 are
    from the United States, 2 are from Great Britain, and 1 is from
    Brazil. If the tournament result lists just the nationalities of the
    players in the order in which they placed, how many outcomes are
    possible?
-   Solution: There are $ \frac{10!}{4!3!2!1!} = 12600 $ possible
    outcomes

#### Example 3f

-   How many different signals, each consisting of 9 flags hung in a
    line, can be made from a set of 4 white flags, 3 red flags, and 2
    blue flags if all flags of the same color are identical?
-   Solution: There are $ \frac{9!}{4!3!2!1!} = 1260 $ possible
    outcomes

### 2.4 Some Simple Propositions (after proposition 4.3)

February 4th, 2013 - Lecture: Combinations
------------------------------------------

### Topics

-   Deriving the formula for combinations.
-   Basic identities and examples.
-   The antenna problem (Ex. 4c of Ross).
-   Counting divisions where all sets non-empty and where sets are
    allowed to be empty.

### Combinations

-   How many ways can we choose k out of n objects when order does not
    matter?
-   Take S = {$x_1, ... , x_n$}. How many k-element subsets does S have?
-   Call the number of k element subsets C(n,k)
-   In general,
    -   C(n,1) = n
    -   C(n,n) = 1
    -   C(n,2) = \# of 2-element subsets

-   S = {$x_1, ... , x_n$}
    -   From every 2 element list -\> n(n - 1)

-   Number of subsets will equal
    $$ \frac{\mathrm{number \: of \: 2 \: element \: sets}}{2} = \frac{n(n - 1)}{2} $$
-   C(n,k) for general k (S = {$x_1, ... , x_n$})
    -   $\frac{n!}{(n - k)!} $ ways to list k-out-of-n elements
    -   Every k-element subset is represented k! times in big list
    -   Big list has $\frac{n!}{(n-k)!} $ entries
    -   $ C(n,k) \times k! = \frac{n!}{(n-k)!} $

-   Notation: $ {{n} \choose {k}} = \frac{n!}{(n-k)!k!}$
    $$ {n \choose 1} = \frac{n!}{(n-1)!1!} = n$$
-   Claim: $ {n \choose k} = {n \choose n-k} $
    $$ {n \choose n - k} = \frac{n!}{(n - (n - k))!(n - k)!} = $$
    $$\frac{n!}{k!(n - k)!} = {n \choose k} $$
-   The number of possible 5-card poker hands is: $ {52 \choose 5} =
    2578960 $

February 4th, 2013 - Reading
----------------------------

### 1.4 Combinations (through example 4c)

-   How many groups of *r* objects can be formed from a total of *n*
    objects?
    -   How many groups of 3 could be formed from the 5 items *A, B, C,
        D,* and *E*.
    -   Since there are 5 ways to select the initial item, 4 ways to
        select the next item, and 3 ways to select the final item, there
        are thus $5 \times 4 \times 3 $ ways of selecting the group of
        3 (order relevant).
    -   In this formulation, each group as a set will be counted 6
        times.
    -   The total number of groups that can be formed is:
        $$ \frac{5 \times 4 \times 3}{3 \times 2 \times 1} = 10$$
    -   In general, *n(n - 1) … (n - r + 1)* represents the number of
        different ways that a group of *r* items could be selected from
        *n* items when order is relevant.
    -   It follows that the number of different groups of *r* items that
        could be formed from a set of *n* items is
        $$ \frac{n(n-1) … (n - r + 1)}{r!} = \frac{n!}{(n - r)!r!}$$

-   **Notation and terminology**
    -   We define $ n \choose r $, for $ r \le n $ by
        $$ {n \choose r} = \frac{n!}{(n - r)!r!}$$ and say that $ n
        \choose r $ represents the number of possible combinations of
        *n* objects taken *r* at a time.

#### Example 4a

-   A committee of 3 is to be formed from a group of 20 people. How many
    different committees are possible?
-   Solution: There are ${20 \choose 3} =
    \frac{20 \cdot 19 \cdot 18}{3 \cdot 2 \cdot 1} = 1140 $ possible
    combinations.

#### Example 4b

-   From a group of 5 women and 7 men, (1) how many different committees
    consisting of 2 women and 3 men can be formed? (2) What if 2 of the
    men are feuding and refuse to serve on the committee together?
    1.  Solution: $ {5 \choose 2}{7 \choose 3} = 350 $ possible
        combinations of 2 women and 3 men.
    2.  I'll ask about this problem in office hours.

#### Example 4c

-   Consider a set of *n* antennas of which m are defective and *n − m*
    are functional and assume that all of the defectives and all of the
    functionals are considered indistinguishable. How many linear
    orderings are there in which no two defectives are consecutive?
-   Solution: $$ n - m + 1 \choose m $$ possible orders in which there
    is at least once functional antenna between any two defective ones.

### 1.6 The Number of Integer Solutions of Equations

February 6th, 2013 - Lecture: Binomial and Multinomial Coefficients
-------------------------------------------------------------------

### Topics

-   Pascal's relationship and Pascal's triangle.
-   The binomial theorem and proofs by combinatorial reasoning and
    induction.
-   Some consequences and examples.
-   Multinomial coefficients and their applications to dividing groups
    and counting strings.

### Introduction

-   For all *n, k \>= 0*. $$
    {n \choose k} = {n - 1 \choose k - 1} + {n - 1 \choose k}
    $$

-   Proof:
    -   ${n \choose k}$ = the number of k-elements of subsets of $x\_1
        ... x\_n $.
    -   Observation: Take any of the $x\_1 .. x\_n $, say $x_n$. Then
        every k-element subset either cointains $x_n$ or it doesn't.
    -   $n - 1 \choose k - 1$ is the number that do contain $x_n$ and
        $n - 1 \choose k $ is the number that don't.
    -   The number that do contain $x_n$ is $n - 1 \choose k - 1 $.

-   Pascal's Triangle
    -   Put $ 0 \choose 0 $ at the top.
    -   The next level is two instances of $1 \choose 0 $
    -   ...

                        1
                    1   2   1
                1     3   3    1
            1     4     6   4    1

### Binomial Theorem

-   For all *x, y*, all *n \>= 1*, $$
    (x + y)^n = \sum_{k = 0}^n {n \choose k}x^ky^{n - k}
    $$
-   Intuitive Combinatorial Proof (Simpler)
    -   When you expand $(x + y)^n$, it equals $(x + y)(x+y) ... (x +
        y) $ "*n*-times"
    -   One way to compute all "monomials" in product is to start with
        *x*, and then pick all the way done, one per time, and repeat
        the exercise until all combinations are exhausted, and you have
        every monomial.
    -   Which monomials show up in sum?
    -   $x^a y^b$ shows up $n \choose a$

-   Proof by induction
    -   We've already checked *n = 1*.
    -   Now assume true for *n - 1* and prove for *n \> 1*
        $$ (x+y)^n = (x+y)(x+y)^{n-1} $$
        $$= (x+y)\cdot\sum_{k=0}^{n-1}{n - 1 \choose k}x^k y^{n - 1 -k}$$
        $$= x\sum_{k = 0}^{n - 1}{n - 1 \choose k}x^k y^{n - 1 - k} + $$
        $$= y\sum_{k = 0}^{n - 1}{n - 1 \choose k}x^k y^{n - 1 - k} $$
    -   Write *i* for *k + 1*:
        $$\sum_{i = 1}^n {n - 1 \choose i - 1}x^i y^{n - 1} + $$
        $$\sum_{i = 1}^n {i \choose n - 1}x^i y^{n - 1}$$
        $$ = x^n + \sum_{i = 1}^{n - 1} \left[ {n - 1 \choose i - 1} + {n - 1 \choose i} \right] \times$$
        $$x^i y^{n - i} + y^n $$

-   Corollary: For any *n \>= 1*, $\sum\_{k = 0}^{n}{n \choose k} =
    2^n $
    -   Proof: $$2^n = (1 + 1)^n = \sum_{k = 0}^n{n \choose k}$$
    -   Intuition: This sum should be the number of wqys to pick a
        subset of any size from a set of size *n*.
        -   To pick a subset, we have *n* decisions where we decide if
            each $x_i$ is in the subset or not.

### Multinomial Coefficients

-   Arise from the following type of problem:
    -   Given a set of *n* distinct items, you need to divide them up
        into *r* groups of given sites $n\_1, n\_2, ..., n\_r $ where
        $n\_1 + n\_2 + ... + n\_r = n $.
    -   How many ways can this be done, for a given *n*, *r*, and $n_1$
        up to $n_r$ where there all add up to *n*.

-   This is very close to something we've already seen, and there are
    two ways of thinking about it.
    1.  How many choices for 1st group? Then into the second, then into
        the third ... $$ n \choose n_1 $$ ways to choose the first group
        $$ n - n_1 \choose n_2 $$ ways to choose the second group, etc,
        and for the $r^{th}$ group:
        $$n - n_1 - n_2 - ... - n_{r-1} \choose n_r = 1 $$ so the
        multiplication principle tells us that if we multiply these all
        together, we get our answer. It cancels nicely:
        $$=\frac{n!}{(n - n_1)!n!}\cdot\frac{n-n_1}{(n - n_1 - n_2)!n!} ...  $$
        and this cancels to $$\frac{n!}{n_1!n_2!...n_r!}$$

-   Example: There are 10 TAs in the department, and we need 3 TAs for
    OSs, 2 for algorithms, and 5 for databases. There there are:
    $$ \frac{10!}{3!2!5!} $$ ways to assign them, which is $2520$.

February 6th, 2013 - Recitation
-------------------------------

5.  Determine the number of vectors $x\_1, x\_2, x\_3, ..., x\_n $
    such that each $x_i$ is either 0 or 1.
    $$ \sum_{i = 1}^{n} x_i \le k $$ (constraint)
    -   Solution $$x_i \in \lbrace 0, 1 \rbrace  $$
        -   The set should be less than $2^n$
        -   Three cases:
            1.  *n = k*: everything should be 1
            2.  *n \< k*: everything something 0
            3.  *n \> k*: the only interesting *k*, $ n \gt k$

7.  Prove that $${n + m \choose r} = {n \choose 0}{m \choose r} + $$
	$${n \choose 1 }{m \choose r - 1} ... + {n\choose r} {m \choose 0} $$

February 6th, 2013 - Reading
----------------------------

### 1.5 Multinomial Coefficients

-   **Notation**
    -   If $ n\_1 + n\_2 + … + n\_r = n $, we define $n \choose n\_1
        + n\_2 + … + n\_r $ by

$$ {n \choose n_1 + n_2 + … + n_r} = \frac{n!}{n_1! + n_2! + … + n_r!} $$
+ Thus, $n \choose n\_1 + n\_2 + … + n\_r $ represents the number of
possible divisions of *n* distinct objects into r distinct groups of
respective sizes $n\_1, n\_2, … , n\_r $.

-   **The multinomial theorem** $$ (x_1 + x_2 + … + x_r)^n = $$
    $$ \sum_{(n_1, …, n_r) : } $$

February 7th, 2013 - Homework 2
-------------------------------

1.  (8 points) Prove that $P(A \cup B) \le P(A) + P(B)$ for any events A
    and B. Prove the general version by induction, which says that if
    $A_1, ..., A_n$ are events then
    $P(\bigcup_{i = 1}^n A_i) \le P(\sum_{i = 1}^n A_i)$. When does this
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

2.  (4 points) If $P(A) = \frac{1}{2}$, $P(B) = \frac{1}{5}$, and
    $P(A\cup B) = 3/5$, what are $P(A\cap B)$, $P(A^c \cup B)$, and
    $P(A^c \cap B)$?

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

February 11th, 2013 - Lecture: Multinomial Theorem, Counting Problems, Inclusion-Exclusion
------------------------------------------------------------------------------------------

### Topics

-   The multinomial theorem and applications
-   The "tree method" for various counting problems involving card hands
    and committees
-   Inclusion-exclusion

### Lecture

-   **Multinomial coefficients**: see reading 1.5 in February 7th
    reading
    -   **Multinomial theorem**: see reading 1.5 in February 7th reading
        -   Sum runs over all vectors of non-negative integers that sum
            to *n*.
        -   Example: $ (x\_1 + x\_2 + x\_3)^2 $ =
            $$\sum_{(n_1, n_2, n_3) : n_1, n_2, n_3 = 2} {2 \choose n_1, n_2, n_3} x_{1}^{n_1} x_{2}^{n_2} x_{3}^{n_3} $$
            $$ = {2 \choose 2, 0, 0} x_{1}^{2} x_{2}^{0} x_{3}^{0} +  $$
            $$ {2 \choose 0, 2, 0} x_{1}^{0} x_{2}^{2} x_{3}^{0} + $$
            $$ {2 \choose 0, 0, 2} x_{1}^{0} x_{2}^{0} x_{3}^{2} + $$
            $$ {2 \choose 1, 1, 0} x_{1}^{1} x_{2}^{1} x_{3}^{0} + $$
            $$ {2 \choose 1, 0, 1} x_{1}^{1} x_{2}^{0} x_{3}^{1} + $$
            $$ {2 \choose 0, 1, 1} x_{1}^{0} x_{2}^{1} x_{3}^{1} $$

        -   Example: What is the coefficient of $x^3 y^4 z$ when $(x +
            y + z)^13 $ is expanded? It corresponds to:
            $$ {13 \choose 3, 9, 1} = 2860 $$
        -   Question: How many terms are in the sum? Equivilently, how
            many monomials are in the expansion? (If *n = 2*, *r = 3*,
            then 6)

-   **More on counting**
    -   Deck of cards: 52 cards, 4 suits, 13 ranks, one of each
        suit/rank combination
    -   Number of 5 card hands: $$ 53 \choose 5 $$
    -   Number of flushes:
        -   4 different suits for flushes
        -   For each suit, the number of flushes is $ 13 \choose 5 $
        -   Therefore, $$4 \times {13 \choose 5}$$

    -   Example: Suppose a committe of *k* people from a group of 7
        women and 4 men.
        -   How many ways can form the committee if it has:
            1.  3 women and 3 men exactly
                $${7 \choose 3} \times {4 \choose 3} $$
            2.  The committee is any size, but it has equal number of
                men and women. Choices:
                1.  1 each $$= {7 \choose 1} \times {4 \choose 1} + $$
                2.  2 each $${7 \choose 2} \times {4 \choose 2} + $$
                3.  3 each $${7 \choose 3} \times {4 \choose 3} + $$
                4.  4 each $${7 \choose 4} \times {4 \choose 4} $$

            3.  If the commitee has 4 people, at least 2 of which are
                women?
                -   Steps:
                    1.  Pick the number of women
                    2.  Pick the women
                    3.  Pick men for the remaining spots.

                -   Possibilities:
                    1.  2 women
                        $$= {7 \choose 2} \times {4 \choose 2} + $$
                    2.  3 women
                        $${7 \choose 3} \times {4 \choose 1} + $$
                    3.  4 women $${7 \choose 4} \times {4 \choose 0} $$

    -   Example: How many hands have exactly 3 aces? "Pick 3 aces, then
        pick 2 non-aces" $${4 \choose 3}\times{48 \choose 2}$$
    -   Example: How many full houses?
        -   Pick the rank of 3-of-a-kind (AAA, 222, ...)
        -   Pick the rank of 2-of-a-kind
        -   Pick the B-of-a-kind
        -   Pick the 2-of-a-kind
            $$13 \times 12 \times {4 \choose 3}\times {4 \choose 2} $$

-   Probability theory $$ P(A \cup B \cup C) = $$
    $$ P(A) + P(B) + P(C) - $$ $$ P(A \cap B) - P(A \cap C) -  $$
    $$ P(A \cap C) + P(A \cap B \cap C) $$

    -   If P is a probability measure an $ A\_1, ... A\_n $ are
        events: $$P(A_1 \cup A_2 \cup ... \cup A_n) = $$
        $$\sum_{i = 1}^n P(A) - \sum_{i \lt j} P(A_i \cap A_j) + $$
        $$ \sum_{i \lt j \lt k}P(A_i \cap A_j \cap A_k) - ... $$
        $$+ (-1)^{n + 1} P(A_1 \cap ... A_n)$$

    -   Include/Exclude Set Version
        -   Some formula, but with set-size intead of P(1)
            $$|A_1 \cup ... \cup A_n| = $$
            $$\sum|A_1| - \sum|A_i \cap A_j $$
            $$\sum A_i \cap A_j \cap A_k $$

    -   Symmetry: For any *i*, |A\_i| is the same.
        $$A_i = {39 \choose 5} $$
        -   For any $i \le j $, $|A_i \cap A_j|$ is the same
            $$26 \choose 5 $$

February 11th, 2013 - Reading
-----------------------------

### 2.4 Some Simple Propositions (from page 31)

February 13th, 2013 - Lecture
-----------------------------

### Include/Exclude Formula

-   If $E_1, ..., E_n$ be events, then

$$P(E_1 \cup E_2 \cup ... \cup E_n) = $$

$$\sum_{i = 1}^n P(E_1) - \sum_i \le j P(E_i \land E_j) + $$

$$\sum_{i \lt j \lt k}P(E_i \cap E_j \cap E_K - ... $$

$$(-1)^{n+1} P(E_i \cap ... E_n) $$

### de MontMort's Problem (1713)

-   Have n students seated in class, no empty seats.
-   Students 1 through n.
-   Everyone stands up, all are assigned, random seats.
-   What's the probability that somebody gets own seat?

#### Dearrangements

-   $ E = $ "someone gets own seat"
-   $E\_i = $ "student i gets own seat"

$$ E = E_1 \cup E_2 \cup ... \cup E_n $$

#### Exploit "symmetry"

$$P(E) = P(E_1 \cup E_2 \cup ... \cup E_n) = $$

-   Observe what is $P(E\_1) = \frac{1}{n} = \frac{n-1}{n!} $
-   Moreover, $P(E\_1) = \frac{1}{n} $ for any i.

-   The number of arrangements that put 1 and 2 in seats 1 and 2 over
    the number of all possible arrangements is

$$\frac{(n-2)!}{n!} = \frac{1}{n(n-1)} $$

-   Works for any i and j:

$$P(E_1 \cap E_j \cap E_k) = \frac{1}{n(n-1)(n-2)} $$

### Conditional probability

-   How we update "beliefs" as new information comes to light.
-   Determine for events A, B, P(A/B) =

$$\frac{P(A \cap B)}{P(B)} $$

    + When B does not equal zero.

#### Explanation \#1

$$P(\lbrace 1 \rbrace) | B) $$

#### Explanation \#2 - "Frequentist"

-   We have some experiment we are going to repeat, generating data.

        01011010 A
        11101011 B
        00010110 
        11010100
        ...

-   Count number of times B happens
-   Count number of times that A happens.

#### Example - Flipping two coinis

-   S = {HH, TH, HT, TT}, all 1/4
-   What's the probabilty of getting 2 heads, given that first toss was
    heads? It's 1/2
    -   A = {HH}
    -   B = {HT, HH}

    $$P(A|B) = \frac{P(\lbrace HH \rbrace)}{\lbrace HT, HH \rbrace}$$

-   What's the probability of HH, given that at least one heads came up?
    -   A = {HH}
    -   B = {HT, TH, HH}

    $$P(A|B) = \frac{P(HH)}{P(HT, TH, HH)} = $$
    $$ \frac{\frac{1}{4}}{\frac{1}{4} + \frac{1}{4} + \frac{1}{4}} = \frac{1}{3} $$

### Example 2 - Fuses

-   Suppose we have 7 fuses, and 5 are working and 2 are broken.
-   We want to find the broken ones, we're going to pick them one at a
    time, and we test.
    -   What's the probability that we only need 2 tests?
        -   Define $E_1$ as "first test shows up broken.
        -   $E_2$ as "second ..." ...

### Gigerenzer's Experiment

-   He did the following experiment:
    -   He got the doctors to agree on some numbers.
    -   They agreed a given patient (say 40-50 year old woman), you know
        nothing about her except she's in good health.
    -   She has cancer with probability 0.008.
    -   They had a cancer test that, if patient has cancer, returns
        positive .9 rightly.
    -   If they don't, it will return positive .07 of they time.

-   He asked 24 doctors:
    -   Suppose a woman's test is positive, what is the probability that
        she has cancer?
        -   First once said he didn't konw.
        -   The other 24 returned this:

                8 said <= 10%
                8 said    50% - 80%
                8 said    90%

-   Lets do some math
    -   C = "patient has cancer"
    -   T = "test is positive" $$P(C) = 0.008 $$ $$P(T|C) = 0.9 $$
        $$P(T|C^c) = 0.07 $$
    -   What's the probability of illness given that the test came up
        positive? $P(C|T) = ? $ $$P(C|T) = \frac{P(C\cap T)}{P(T)} $$
        $$P(T|C) = \frac{P(C \cap T)}{P(C)} $$
    -   Want P(T)

-   **Lemma**: For any event T, C
    $$P(T) = P(T \cap C) + P(T \cap C^c) $$

-   Answer: 9.4%

#### Intuition, not a proof at all

-   Say you take 1000 women,
    -   Should have 8 with cancer ill.
    -   How may should test positive? \~7 will be positive

February 13th, 2013 - Recitation
--------------------------------

1.  Prove the following is true:
    $$ {n \choose 2} = {k \choose 2} + K(n - k) + {{n-k} \choose 2} $$
    -   What is $n \choose 2$?
    -   We're going to have to put a *k* into the left hand side.
    -   So you have n object, I can select 2 object as n choose 2
    -   I could do the same selection of 2 objects by partitioning them
        into n and n-k objects.
    -   Or I could select one from one side, etc.
    -   Since I am selecting two objects, what are the possibilities.
    -   Both of them could be from the left or right, or one could be on
        both sides.

2.  Prove: $$\sum_{k=1}^n k {n \choose k} = n2^{n-1} $$
    -   If you expand out the left hand side:
        $$1 \times {n \choose 1} + 2 \times {n \choose 2} + ... + n {n \choose n} = n2^{n-1} $$

3.  Let n be the number of people and we have to form a commitee of
    arbitrary size and select a chair from that committee.
    -   Method 1 $$k {n \choose k} $$ is the number of ways to select a
        commite of size k and a chair
        -   Hence, the total number of ways to form a commite of
            arbitrary size is $$\sum_{k=1}^{n} k {n \choose k} $$

    -   Method 2
        -   We can first select the chair in n-ways. From the remaining
            n - 1 people we can select a subset in $2^{n-1} ways.

4.  Prove: $$\sum_{i=0}^n (-1)^i {n \choose 1} = 0 $$

February 18th, 2013 - Lecture: Bayes's Theorem
----------------------------------------------

### Topics:

-   Bayes's theorem: Statement, examples, applications to spam filtering
    and other fields.
-   General version of Bayes's theorem and the red/black hat problem.

### Boxes and balls

-   **Example**: There two boxes, the first contains 2 green balls and 7
    res and the second contains 4 green and 3 red. I pick a random box,
    then a ball from that box. If I pick a red ball, what is the
    probability that I picked the first box?
    -   E = "red ball was picked"
    -   F = "1st box was picked
        $$P(F | E) = \frac{P(E \cap F)}{P(E)} = $$
        $$\frac{\frac{7}{18}}{\frac{38}{63}} $$

    (I) $$P(E \cap F) = P(E | F) \times P(F) = $$
        $$\frac{7}{9} \times \frac{1}{2} = \frac{7}{18} $$
    (II) $$ P(E) = P(E \cap F) + P(E \cap F^c) = $$
        $$\frac{7}{18} + P(E | F^c) \times P(F^c) = $$
        $$\frac{7}{18} + \frac{3}{7} \times \frac{1}{2}$$

### "Bayesian Reasoning"

-   A method for updating "belief"/"uncertainty" based on evidence.
-   This is useful when you want to know the probability of some outcome
    given some evidence when you know the probability of the outcome and
    you also konw the quality of your evidence, and the probability of
    the evidence given the outcome, and finally, the probability of the
    evidence showing up if the outcome didn't happen.
    1.  P(outcome|evidence)
    2.  P(outcome)
    3.  P(evidence|outcome)
    4.  P(evidence|outcome^c)

### Bayesian Spam Filtering

-   Outdated but interesting anyway
-   The idea is that you estimate P(Email contains some word w | it's
    spam)
    -   Rolex
    -   Viagra
    -   Rutgers
    -   Cash
    -   LaTeX

-   Then the probability of the P(Emails contains the same word w | it's
    not spam)
-   P(Email is spam)
-   Using these, there is Bayes theorem, which computes
    P(outcome|evidence) = P(spam | contains w)
-   The attack is called Bayesian poisoning
    -   You retrain this when you email it everyday.
    -   Spammers pass it the words you are interested in, which you mark
        as spam, and then the ones you aren't interested in eventually
        pass.

### Bayes Theorem

-   If E and F are events with $P(E) \neq 0 $ and $P(E) \neq 0 $,
    then
    $$ P(F | E) = \frac{P(E | F) \times P(F)}{P(E | F)\times P(F) + P(E | F^c) \times P(F^c)} $$
    1.  $P(E \cap F) = P(E | F) \times P(F) $
    2.  $P(E) = P(E | F) \times P(F) + P(E | F^c) \times P(F^c) $

### General version of Bayes theorem

-   For multiple outcomes
-   Let $F_1 ... F_n$ be events that
    1.  Are mutually exclusive
    2.  $F\_1 \cup ... \cup F\_n = S $
    3.  $\forall i P(F\_i \neq 0) $

-   Then for any j $$ P(F_j | E) = $$
    $$\frac{P(E|F_j) \times P(F_j)}{\sum_{i=1}^n P(E|F_i) \times P(F_i)} $$

#### Example with Lizards

-   $F_1 ... F_n$ are lizards in the family i
-   E = "something genome of new lizard"
-   Need to estimate the priors

February 18th, 2013 - Reading
-----------------------------

### Ross 3.3

### Rosen 7.3

February 19th, 2013 - Homework 3
--------------------------------

1.  (6 points) What the probability that a 5 card hand contains exactly
    3 spades? What if we condition on the hand containing at least 1
    spade?

    -   A deck of cards has 52 cards, 4 suits, 13 ranks, one of each
        suit/rank combination.

    -   There are $52 \choose 5$ possible hands.

    -   There are $13$ cards which are spades.

    -   Let $E\_i = $ “a spade was drawn” and $F\_i = $ “anything
        except a spade was drawn.”

    -   We want $P(E_1 \cap E_2 \cap E_3 \cap F_1 \cap F_2)$.

    -   The probability of $E_1$ is $\frac{13}{52}$, because thirteen of
        the cards are spades.

    -   Assuming $E_1$, the probability of $E_2$ is $\frac{12}{51}$,
        because there is one less spade and one less card in general.

    -   Assuming $E_2$, the probability of $E_3$ is $\frac{11}{50}$,
        because there are now two less spades and two less cards in
        general.

    -   There are now 49 cards in all, 10 of which *are* spades.

    -   Assuming $E_1$ through $E_3$, the probability of
        $F_1 = \frac{39}{49}$.

    -   Assuming $F_1$, the probability of $F_2 = \frac{38}{48}$.

        $$\frac{13}{52}\times\frac{12}{51}\times\frac{11}{50}\times\frac{39}{49}\times\frac{38}{48} = 0.008154261704$$

    -   Alternatively, there are 13 choose 3 ways of picking a spade, 39
        choose 2 way of picking a “not spade,” and there are 52 choose 5
        possible options:

        $$\frac{{13 \choose 3} {39 \choose 2}}{{52 \choose 5}} = \frac{{286} \times {741}}{{2598960}} = 0.008154261704$$

    -   For part two, you only have to pick four cards out of 51,
        because one is a space already.

        $$\frac{{13 \choose 2} {39 \choose 2}}{{51 \choose 4}}$$

2.  (7 points) Suppose $n$ people each throw a six-sided die. Let $A_n$
    be the event that at least two distinct people roll the same number.
    Calculate $P(A_n)$ for $n=1,2,3,4,5,6,7$.

    -   For $A_1$, It is impossible for two distinct people to roll the
        same number if only person rolls. $$P(A_1) = 0$$

    -   For $A_2$, there are 36 possible throws, but only 6 of could
        contain two distinct people rolling the same number.
        $$P(A_2) = \frac{6}{6^2} = \frac{1}{6} = 0.1666666667$$

    -   For $A_3$ consider the complement, which can be described as “No
        two distinct people roll the same number.” The probability that
        all three people roll unique numbers is
        $1 \times \frac{5}{6} \times \frac{4}{6} \times$,
        $$P(A_3) = 1 - P(A_3^c) = 1 - \frac{5}{6} \times \frac{4}{6} = 0.4444444444$$

    -   For $A_4$, consider the complement again, and apply the same
        reasoning.
        $$P(A_4) = 1 - 1 \times \frac{5}{6} \times \frac{4}{6} \times \frac{3}{6} = \frac{13}{18} =0.7222222222$$

    -   For $A_5$, consider the complement again, and apply the same
        reasoning.
        $$P(A_5) = 1 - \frac{5}{6} \times \frac{4}{6} \times \frac{3}{6} \times \frac{2}{6} = 0.9074074074$$

    -   For $A_6$, consider the complement again. There are $6!$ ways of
        arranging the integer elements in the string “123456.” This is
        out of a $6^6$ ways of writing a string with integers from one
        to six. $$P(A_6) = 1 - \frac{6!}{6^6} = 0.98456790123$$

    -   If 7 people roll a dice with 6 sides, it is inevitable that at
        least two distinct people roll the same number. $$P(A_7) = 1$$

3.  (3 points) Suppose we draw 2 balls at random from an urn that
    contains 5 distinct balls, each with a different number from
    $\{1,2,3,4,5\}$, and define the events $A$ and $B$ as
    $$A = \text{``5 is drawn at least once"} \quad \text{and} \quad
        B = \text{``5 is drawn twice"}$$ Compute $P(A)$ and $P(B)$.

    -   $P(B) = 0$

    -   $P(A) = \frac{4}{{5\choose 2}} = 0.4$

4.  (4 points) In the previous problem, suppose we place the first ball
    back in the urn before drawing the second. Compute
    $P(A),P(B),P(A|B),P(B|A)$ in this version of the experiment.

    -   $P(A) = 1 - \left(\frac{4}{5}\right)^2 = .36 $

    -   $P(B) = \left(\frac{1}{5}\right)^2 = .04$

    -   $P(A|B) = 1$

    -   $P(B|A) = \frac{1}{5}$

5.  (4 points) Suppose $5$ percent of cyclists cheat by using illegal
    doping. The blood test for doping returns positive $98$ percent of
    the people doping and $12$ percent who do not. If Lance’s test comes
    back positive, what the probability that he is doping? (Ignoring all
    other evidence, of course...)

    -   $P(C) = $ “the probability a cyclist cheated by doping”
        $= .05$

    -   $P(T|C) = $ “the probability a cyclist giving a positive test
        if they doped” $= .98$

    -   $P(T|C^c) = $ “the probability a cyclist giving a positive
        test if they *did not* dope” $ = .12$

    -   We want the probability of a cyclist doping given a positive
        test, which is $P(C|T)$.

        $$P(T|C) = .98 = \frac{P(T \cap C)}{P(C)} = \frac{P(T \cap C)}{.05}$$

        $$P(T \cap C) = .049$$

        $$P(T \cap C^c) = .12 = \frac{P(T \cap C^c)}{P(C^c)} = \frac{P(T \cap C^c)}{.95}$$

        $$P(T \cap C^c) = .114$$

    -   For any event $T$ and $C$,

        $$P(T) = P(T \cap C) + P(T \cap C^c)$$

        $$P(T) = .049 + .114 = .163$$

        $$P(C|T) = \frac{P(C \cap T)}{P(T)} = \frac{.049}{.163} = 0.3006134969 \approx .30$$

    -   Intuition:

        -   Take 100 cyclists, 5 of them actually doped according to
            these numbers.

        -   If all 100 cyclists are tested, it’s very, very likely the 5
            will return positive.

        -   Of the remaining 95 cyclists, 12 percent of them will also
            return positive, which makes a little less than 12 cyclists.

        -   So for each of the 17 who tested positive, there are five
            who actually doped, which means each has a
            $\frac{5}{17} = 0.2941176471 \approx .30$ probability of
            doping.

6.  (6 points) If $A \subseteq B$, can $A$ and $B$ be independent? What
    we if require that $P(A)$ and $P(B)$ both not equal $0$ or $1$?

    -   $A$ and $B$ are independent if they satisfy the condition
        $P(A \cap B) = P(A)P(B)$

    -   If $A \subseteq B$, it is true that $A \cap B = B$.

    -   This means that $P(A \cap B)=P(B)$.

    -   In order to be independent when $A \subseteq B$ is true, $P(B)$
        must equal $P(A)\cdot P(B)$.

    -   The only way anything multiplied by something can equal itself
        is if that something is one.

    -   Therefore, when $A \subseteq B$, $A$ and $B$ can be independent
        when $P(A) = 1$.

    -   Furthermore, being as anything multiplied by zero yields zero,
        when $A \subset B$, $A$ and $B$ can be independent if
        $P(B) = 0$.

    -   So no.

7.  **Extra credit (5 points)** Consider the experiment where two dice
    are thrown. Let $A$ be the event that the sum of the two dice is 7.
    For each $i \in \{1,2,3,4,5,6\}$ let $B_i$ be the event that at
    least one $i$ is thrown.

    1.  Compute $P(A)$ and $P(A|B_1)$.

        -   $P(A) = \frac{6}{6^2} = \frac{1}{6}$

        -   $P(A|B_1) = \frac{P(A \cap B_1)}{P(B_1)}= \frac{\frac{3}{{6 \choose 2}}}{\frac{1}{6} + \frac{1}{6}} = 0.6$

    2.  Prove that $P(A|B_i) = P(A|B_j)$ for all $i$ and $j$.

        -   Being as the sum has to be seven, there is one and only way
            to sum to seven for the integers 1 through 6.

        -   So it doesn’t matter what is rolled on the first roll, the
            probability “rides on” the second roll being the number the
            first roll needs to sum to seven.

        -   The probability of rolling any given number on a fair die is
            always $\frac{1}{6}$.

        -   Therefore, for all $i$ and $j$, the probability cannot be
            anything but $\frac{1}{6}$.

    3.  Since you know that some $B_i$ always occurs, does it make sense
        that $P(A) \neq P(A | B_i)$? (After all, if $E$ is an event with
        $P(E) = 1$, then for any event $F$, $P(F|E) = P(F)$. What is
        going on? Does this seem paradoxical?)

February 20th, 2013 - Lecture: Independence
-------------------------------------------

### Topics

-   Multiplication rule for conditional probability.
-   Independent events: two equivalent definitions and several examples
    with cards and dice.
-   People v. Collins and the prosecutor's fallacy.
-   Mutual independence.

### Multiplication Rule for Conditional Probability

-   **Example**: Hat contains 3 cards, RR, RB, BB. Pick a card, put it
    on table, see a R side, what's the probability the other side is B?
    -   Wrong: 1/2
    -   Right: 1/3

-   If E\_1 through E\_2 are events, all P(E\_i) do not equal zero,
    $$P(E_1 \cap E_2 \cap ... \cap E_n) = $$
    $$P(E_1) \times P(E_2 | E_1) \times ... \times P(E_n | E_1 \cap ... \cap E_{n-1}) $$
    -   This might be easier to express as the intersection of smaller
        events.
    -   This is really easy thing to prove.
    -   "Proves itself."
    -   **Proof**:
        1.  $P(E_1) \times \frac{P(E_2 \cap E_1)}{P(E_1)} \times ... \times \frac{P(E_1 \cap ... \cap E_n)}{P(E_1 \cap ... \cap E_{n-1}})$
        2.  Cancel. Beautiful cancellation.

    -   This allows you to say, what happens when the first once
        happens? And now, what about the second one? So on so forth.
    -   **Example**: What is the probability of a five card hand not
        containing a pair?
        -   E\_i = "first i cards in hard do not contain a pair"
        -   *Claim*: What we want is $E\_1 \cap E\_2 \cap ... \cap E\_5
            $
        -   What's funny about this is that we don't want E\_1 through
            E\_4, we are actually only interested in E\_5.
        -   The reason we do this, however, is because it makes this
            calculation easier.
        -   Possibilities:
            1.  $P(E\_1) = 1 $
                -   The probaility of the first hand not being a pair is
                    1, because it's one card.

            2.  $P(E\_2 | E\_1) = \frac{48}{51} $
            3.  $P(E\_3 | E\_1 \cap E\_2) = \frac{44}{50} $
            4.  $P(E\_4 | E\_1 \cap ... \cap E\_3) = \frac{40}{44} $
            5.  $P(E\_5 | E\_1 \cap ... \cap E\_4) = \frac{36}{48} $

        -   Multiply these values together to get 50.7%.

### Independence

-   **Definition**: Say events E and F are independant if $P(E \cap F)
    - P(E) \times P(F)
    $. + **Equivalent definition**: E and F are independent i(P(F) = 0 or P(E|F) = P(E)$.
    -   **Proof**:
        1.  Take E and F set $P(E \cap F) = P(E) \times P(F) $.
        2.  If $P(F) = 0 $, then done.
        3.  If not, then $P(E|F) = \frac{P(E \cap F)}{P(F)}$

-   **Exercise**: Toss two coins
    -   E = "1st coin was H"
    -   F = "2nd coin was H"
    -   P(E) = P(F) = 1/2

-   **Exercise**: Tossing two dice
    -   E = "sum of dice is 6"
    -   F = "first die was 4"
    -   $P(E) = P(\lbrace(1,5),(2,4),(3,3),(4,2),(5,1)\rbrace) = \frac{5}{36}$
    -   P(F) = 1/6
    -   $P(E \cap F) = P(\lbrace(4,2)\rbrace) = \frac{1}{36} $
    -   $P(E) \times P(F) = \frac{5}{36} \times \frac{1}{6} $

-   **Exercise**: Suppose a family has 3 kids.
    -   E = "family has at least 1 boy and 1 girl"
    -   F = "family has at most 1 boy"
    -   Are these indepedant?
        -   $S = \lbrace BBB, BBG, BGB, GBB, BGG, GBG, GGB, GGG\rbrace$
        -   $E = S - \lbrace BBB, GGG \rbrace $
        -   $F = \lbrace BGG, GBG, GGB, GGG \rbrace $
        -   $E \cap F = \lbrace BGG, GBG, GGB \rbrace $
        -   $ P(E \cap F) = \frac{3}{8} $
        -   $ P(E) \times P(F) = \frac{3}{4} \times \frac{1}{2} =
            \frac{3}{8} $
        -   Therefore, independent.

#### "Independent" and "Mutually Exclusive" are not the same

-   **Example**: 2 dice
    -   E = "sum was 6"
    -   F = "first die was 6"
    -   E and F are not mutually exclusive, but not independent.

#### Prosecutor's Fallacy: People v. Collins (1968)

-   The prosectution came up with these numbers:
    -   The probability of a black man with a beard is 1 in 10
    -   The probability of a man with a mustache is 1 in 4
    -   White woman with ponytail is 1 in 10
    -   So on so forth, 1 in 3, 1 in 10, 1 in 1000
    -   So he made this calculation:
        $$\frac{1}{10} \times \frac{1}{4} \times \frac{1}{10} \times \frac{1}{10} \times \frac{1}{3} \times \frac{1}{1000} = \frac{1}{12 \times 10^6} $$
    -   *Say* that the population of LA was $24 \times 10^6$
    -   Then, you'd "expect" to have 2 couples fitting this evidence.
    -   P(evidence | innocent) $\neq$ P(innocent | evidence)

#### With 3 events

-   E is indepedant of F and G
-   F is indepedant of G
-   Then is E indepedant of F intersect G?
-   **Example**: rolling two die
    -   E = "sum to 7"
    -   F = "first die was 4"
    -   G = "second die was 3" $$P(E | F \cap G) = 1$$
        $$P(E) = \frac{1}{6} $$
    -   **Definition**: E, F, and G are independant (alternatively
        "mutually independant") if: $$P(E \cap F) = P(E) \times P(F) $$
        $$P(E \cap G) = P(E) \times P(G) $$
        $$P(F \cap G) = P(F) \times P(G) $$
        $$P(E \cap F \cap G) = P(E) \times P(F) \times P(G) $$

#### With n events

-   **Definition**: $E\_1, ..., E\_n $ are indepedant if for every
    subset $I \subseteq \lbrace 1, 2, ..., n \rbrace$ of at least size 2
-   **Example**: Flip n coins

February 20th, 2013 - Recitation
--------------------------------

-   Proove: $${n \choose n_1 \cdot n_2 \cdot ... \cdot n_r} = $$ [[[{n-1
    \choose n\_1 - 1 \cdot ... \cdot n\_r} + ... + {n-1 \choose n\_1
    \cdot ... \cdot n*{r-1} \cdot n*{r-1} $$

February 20th, 2013 - Reading
-----------------------------

### 3.3 Bayes' Formula

### 3.4 Independent Events

-   **Equation 4.1**: $P(EF) = P(E)P(F)$
-   **Independent events**: Two events E and F are said to be
    independent if Equation (4.1) holds.
-   **Dependent events**: Two events E and F that are not independent
    are said to be dependent.

### Optional: People v. Collions court opinion.

### British case involving Sally Clark.

February 25th, 2013 - Lecture
-----------------------------

### Announcements

1.  HW 3 due Wednesday
2.  Review on Wednesday
3.  Midterm on Monday

### Independence of Several Events

-   Event are indepedant if $P(EF) = P(E)P(F)$
-   **Example**: Three events with dice:
    -   E = "sum is 7"
    -   F = "1st die is four"
    -   G = "2nd die is three"
    -   E, F, G are *pairwise independant*
    -   But the $P(E | F \cap G) = 1$, not $P(E) = \frac{1}{u}$

-   **Definition**: Events $E\_1, E\_2, ... E\_n $ are **indepedent**
    (or **mutually independent**) if for every subset of numbers from 1
    through n of size greater than or equal to 2:
    $$P\left(\bigcap_{i \in I} E_i\right) = \prod_{i \in I} P(E_i)$$
    -   Equivilently,
        $$ P(E_{i_1} \cap E_{i_2} \cap ... \cap E_{i_n}) = P(E_{i_1}) \cdot P(E_{i_2}) \cdot ... \cdot P(E_{i_k}) $$

-   **Claim**: For any $i$ and $j_i, ..., j_k$ (not including i)
    $$P(E_i | E_{j_1} \cap ... \cap E_{j_k}) = P(E_i)$$
    -   **Proof**: This equation equals
        $$ \frac{P(E_1 \cap E_{j_1} \cap ... \cap E_{j_k})}{P(E_{j_1} \cap ... \cap E_{j_k})}$$

-   **Example**: Suppose we flip a "biased" coin $n$ times
    $$ P(H) = p, \: P(T) = 1 - p, \: (O \lt p \lt 1)$$
    1.  What is the probability we getting heads all n times?
        -   Define $E\_i = $ "ith flip was heads."
            $$E = E_1 \cap ... \cap E_n, \: P(E) = P(E_1) \times ... \times P(E_n)$$

    2.  What is the probability we get at least one H?
        -   $F = $ "at least on H"
        -   $C(F) = $"all T on n flips"
        -   $P(F) = 1 - C(F) = 1 - (1 - p)^n$
        -   $P(F^c) = (1 - p)^n$

    3.  What is the probability of getting exactly k heads?
        -   First find the probability of HHHH...H (k heads) TTTTT...T
            (n-k tails) (h times)
        -   $p \times p \times p \times p ... $ (k times)
            $\times (1-p) \times (1 -p) \times ... \times (1 - p) =
            p^k (1-p)^{n - k} $
        -   How many H/T strings, length n, with k Hs? $n \choose k$
        -   P(exactly k Hs) =
            ${n \choose k} \cdot p^k \cdot (1 - p)^{n-k}$

### Primality Testing

-   One way to check if a number is prime is to divide by the square
    root of number (or something)
-   So people found what's called the
    [Miller-Rabin](http://en.wikipedia.org/wiki/Miller–Rabin_primality_test)
    test

        when running MR on x
            if x is not prime
                then MR outputs "not prime" with probability 1/4
                else says "don't know" the other 3/4 times
            if x is prime
                then MR always says "don't know"

#### Algorithmic amplification

-   The idea is to run MR n times on x
    -   If it ever says "not prime", output "not prime"
    -   If not, output "probabily prime"

-   What is the probability of outputting "probability prime" if X is
    not prime
    -   $ \left(\frac{3}{4}\right)^n $

-   [AKS test](http://en.wikipedia.org/wiki/AKS_primality_test)

### Ramsey Numbers

-   **Example**: "The probabilistic method"
    -   Take a complete graph $n$ vertices, color every edge R or B, and
        you "lose" if you color in a triangle.
    -   Avoid making an all red or all blue $K_k$

            o----R----o
            |\        |
            |  \      |
            B    R    B
            |      \  |
            |        \|
            o----B----o (or something)

-   **Theorem** If n is large enough relative to k, then you can't avoid
    making all R or B $K_k$ $$n \gt R(k)$$
-   $R(3) = 6$, $R(4) = 18$ (1979), $R(5)$ is unknown
-   **Theorem**: $R(k) \ge n^{\frac{k}{2}} $ when $k \gt 4$, if $ n
    = 2^{\frac{k}{2}}$, then you can color $K_n$ and avoid a all R or
    B $K_K$
    -   **Outline**: (Erdos)
        1.  Calculate the probability that a random coloring "works",
            not that is greater than 0
        2.  Therefore one exists, and done.

    -   Color each edge independently Red or Blue with probability of
        one half
        -   E = "some K\_k gets all Red or Blue edges"
        -   How many $K_K$ are these in $K\_K $? $n \choose k$
        -   Want:
            $$ P(E) = P\left( \bigcup_{i =1}^{n \choose k} E_i \right) \lt 1 $$
            $$]

February 25th, 2013 - Lecture: Mutual Independence and Applications
-------------------------------------------------------------------

### Topics

-   Definition of mutual independence
-   Examples
-   Applications to biased coin flips
    -   primality testing
    -   the bound on Ramsey numbers

February 25th, 2013 - Reading
-----------------------------

### Ross 3.4.

### Rosen 7.2.

Midterm 1 Review
----------------

### Review Sheet 1

#### Set Theory Review

-   $x \in A$ means "x is an element of A"; $x \notin A$ means it's not.
-   **relations between sets**
    -   $A \subseteq B$ means that if x is in A, then x is in B
    -   $A \supseteq B$ means $B \subseteq A$
    -   $A = B$ means $A \subseteq B$ and $B \subseteq A$

-   **operations on sets**
    -   $A^c = \{x \in S : x \notin A\}$ (complement)
    -   $\emptyset = S^c$ (the empty set)
    -   $A \cap B = \{x \in S : x \in A \land x \in B\}$ (intersection)
    -   $A \cup B = \{x \in S : x \in A \lor x \in B \}$ (union)
    -   $A \setminus B =\{x\in S :x\in A \land x \notin B \} = A \cap B^c$

-   **set identities**
    -   $A \cup (B \cap C) = (A \cup B) \cap (A \cup C)$
    -   $A \cap (B \cup C) = (A \cap B) \cup (A \cap C)$
    -   $(A \cap B)^c = (A^c) \cup (B^c)$ (de Morgan's law)
    -   $(A \cup B)^c = (A^c) \cap (B^c)$ (de Morgan's law)

#### Probability Theory

-   **Random experiment**
    -   Idealized or conceptual experiment.
    -   It can be useful to imagine that the experiment can be repeated
        infinitely often under identical conditions, but with different
        outcomes.

-   **Sample Space**
    -   The set of outcomes (elementary events) of a random experiment.

-   **An event**
    -   A subset of the sample space of an experiment.
    -   If the experiment is performed and the out of $x \in S$ we say
        that "x occurs."
    -   If not, "x does not occur"

-   **Probability measure**
    -   A real-valued non-negative function on events in S which satisfy
        these axioms:
        -   $P(S) = 1$
        -   $P(A \cup B) = P(A) + P(B)$ whenever $A \cap B = \emptyset$

#### Conditional Probability

-   **Conditional probability formula**

$$ P(B|A) = \frac{P(A \cap B)}{P(A)} $$

-   **Hypotheses**

$$ P(A) = \sum_{i = 1}^{n} P(H_1)P(A|H_i) $$

-   **Bayes' rule**

$$P(H_i|A) = \frac{P(A|H_1)P(H_1)}{\sum_{j = 1}^n P(H_j)P(A|H_j)}$$

#### Independence

-   Events are **independent** if and only if

$$P(B|A) = P(B) $$

-   This means that the probability of B given the information that A
    has occurred is the original probability of B, so A gives no new
    information about B's probability. Using the conditional probability
    formula, for the left-hand side we see that

$$P(A \cap B) \setminus P(A) = P(B) $$

-   Multiplying both sides of this equation by $P(A)$ we get the
    **product law** for independent events

$$P(A \cap B) = P(A)P(B)$$

### Axioms of Probability - Self Test Problems and Exercises

1.  A cafeteria offers a three-course meal consisting of an entree, a
    starch, and a dessert. The possible choices are given in the
    following table:

        Course          Choices
        Entree          Chicken or roast beef
        Starch          Pasta or rice or potatoes
        Dessert         Ice cream or Jello or apple pie or a peach

    A person is to choose one course from each category.
    1.  How many outcomes are in the sample space?
        -   There are there points a person gets to choose something.
        -   At each of those points, there are 2, 3, and 4 choices.
        -   So I think it's $2! + 3! + 4!$, but I'm pretty bad at math.
        -   In hindsight, that's about putting things in order, and has
            nothing to do with this problems.
        -   It's simply: $2 \cdot 3 \cdot 4$

    2.  Let A be the event that ice cream is chosen. How many outcomes
        are in A?
        -   This only says something about the final decision.
        -   Therefore, the previous number still holds, with a
            restriction on the final choice.
        -   Therefore, $2 \cdot 3$

    3.  Let B be the event that chicken is chosen. How many outcomes are
        in B?
        -   Similar formula.
        -   $3 \cdot 4$

    4.  List all the outcomes in the event AB.
        1.  Chicken
        2.  (Pasta|Rice|Potatoes)
        3.  Ice cream
            -   More formally, {(chicken, x, ice cream) | x $\in$
                {pasta, rich, potatoes}

    5.  Let C be the event that rice is chosen. How many outcomes are in
        C?
        -   $2 \cdot 3$

    6.  List all the outcomes in the event ABC.
        -   {(Chicken, rice, ice cream)}

2.  A customer visiting the suit department of a certain store will:
    -   purchase a suit, $.22$
    -   purchase a shirt, $ .30$
    -   purchase a tie, $.28$
    -   both a suit and a shirt, $ .11$
    -   both a suit and a tie, $.14$
    -   both a shirt and a tie, $.10$
    -   all 3 items with probability $ .06$

    What is the probability that a customer purchases

    -   none of these items?
        -   I think it's too easy for them to just give us the .06
            number and then have us calculate the complement. But that's
            my first guess, .94. (I know this is wrong.)
        -   We're interested in the union of purchasing a suit,
            purchasing a shirt, and purchasing a tie.
        -   The probability of buying all of these items is:
            $$P(A \cap B \cap C) = .22 + .30 + .28 + .11 + .14 + .10 + .06$$
        -   Subtract one from this to get the probability of buying
            none.
        -   I worry that I would not see this on a test.

    -   exactly 1 of these items?
        -   Add the probabilities that correspond *to* the sample space.
        -   Subtract the probabilities that *do not* correspond to this
            event. $$.22 + .30 + .28 - .11 - .14 - .10 - .06$$
        -   Of course, this is totally wrong.
        -   Right, so formally, where A is "purchase suit", B is
            "purchase shirt", and C is "purchase tie." We want:
            $$P(AB \cup AC \cup BC)$$

3.  A deck of cards is dealt out. What is the probability that the 14th
    card dealt is an ace? What is the probability that the first ace
    occurs on the 14th card?
    -   So there are four aces in a deck, meaning there are 48 that
        aren't.
    -   But every card is equally likely to be pulled at any time.
    -   This is called **symmetry**.

4.  Let A denote the event that the midtown temperature in Los Angeles
    is 70◦F, and let B denote the event that the midtown temperature in
    New York is 70◦F. Also, let C denote the event that the maximum of
    the midtown temperatures in New York and in Los Angeles is 70◦F. If
    P(A) = .3, P(B) = .4, and P(C) = .2, find the probability that the
    minimum of the two midtown temperatures is 70◦F.
    -   A is "the temp of LA is 70F", .3
    -   B is "the temp of NY is 70F", .4
    -   $P(A \cap B) = .3 + .4 - P(AB)$
    -   Call D "the minimum of the two is 70F"
    -   Observe that $A \cap B = D \cap C$, and therefore $AB = DC$.
    -   $P(D \cap C) = P(D) + .2 - P(DC)$
    -   $P(D) + .2 - P(DC) = .3 + .4 - P(AB)$
    -   $P(D) + .2 = .3 + .4$
    -   $P(D) = .3 + .4 - .2 = .5$

5.  An ordinary deck of 52 cards is shuffled. What is the probability
    that the top four cards have
    1.  different denominations?
        -   There are $52!$ total possibilities.
        -   I think that each of the four top cards can be counted as
            $13 \choose 1$.
        -   Wait no.
        -   You're picking four cards, ignore the rest of the deck.
        -   There are $52 \cdot 51 \cdot 50 \cdot 49$ total ways.
        -   Denomiation means 1 or 2 or 3 or ... or King or Ace.
        -   After each is picked, there are four less cards that are
            "available."
            $$\frac{52 \cdot 48 \cdot 44 \cdot 40}{52 \cdot 51 \cdot 50 \cdot 49}$$

    2.  different suits?
        -   Like the last problem, there are
            $52 \cdot 51 \cdot 50 \cdot 49$ total ways.
        -   But this time, each time a card is picked, there are 13 less
            choices.
            $$\frac{52 \cdot 39 \cdot 26 \cdot 13}{52 \cdot 51 \cdot 50 \cdot 49}$$

6.  Urn A contains 3 red and 3 black balls, whereas urn B contains 4 red
    and 6 black balls. If a ball is randomly selected from each urn,
    what is the probability that the balls will be the same color?
    -   R = "both balls were red."
    -   B = "both balls were black."
    -   There is a probability of zero that both these events happen.
    -   $P(R \cup B) = P(R) + P(B) - 0$
    -   $P(R) = \frac{3 \cdot 4}{6 \cdot 10}$
    -   $P(R) = \frac{3 \cdot 6}{6 \cdot 10}$

7.  In a state lottery, a player must choose 8 of the numbers from 1 to
    40. The lottery commission then performs an experiment that selects
        8 of these 40 numbers. Assuming that the choice of the lottery
        commission is equally likely to be any of the $40 \choose 8$
        combinations, what is the probability that a player has

    -   all 8 of the numbers selected by the lottery commission?
        -   They can only have one of the combinations.
            $$\frac{1}{40 \choose 8}$$

    -   7 of the numbers selected by the lottery commission?
        -   I think that there are $40 \cdot 39 ... \cdot 32$ total
            combinations.
        -   Having one of them would mean, I think,
            $$\frac{40 \cdot 39 ... \cdot 33}{40 \cdot 39 ... \cdot 32}$$
        -   Unfortunately, this is very wrong. The better way to think
            of this is there are 8 choose 7 ways of picking 7 numbers.
        -   I can't work out on my own what you need to multiply this
            by, I think it has something to do with the number of 7
            combination choices in a 40 choice pool.

    -   at least 6 of the numbers selected by the lottery commission?

8.  From a group of 3 freshmen, 4 sophomores, 4 juniors, and 3 seniors a
    committee of size 4 is randomly selected. Find the probability that
    the committee will consist of
    1.  1 from each class
        $$\frac{3 \times 4 \times 4 \times 3}{14 \choose 4}$$
        -   Every number in the numerator is like "number in class"
            choose 1, which is just "number in class."

    2.  2 sophomores and 2 juniors
        $$\frac{{4 \choose 2} \times {4 \choose 2}}{14 \choose 4}$$
        -   You have to pick two out of each 4, and then divide it by
            the entire sample space.

    3.  only sophomores or juniors $$\frac{8 \choose 4}{14 \choose 4}
        -   It could be all sophomores or all juniors, or a combination
            thereof, so just count them as one group with 8 choose 4.

9.  For a finite set A, let N(A) denote the number of elements in A.
    Show that: $$ N(A \cup B) = N(A) + N(B) − N(AB) $$

             +--------------+    +-------------+
            /                \  /               \
           /                  \/                 \
          /                   /\                  \
         /                   /  \                  \
        |                   |    |                 | 
        |          A        | AB |       B         |
        |                   |    |                 |
         \                   \  /                  /
          \                   \/                  /
           \                  /\                 /
            \                /  \               /
             +--------------+    +-------------+

    -   $A \cup B$ is equal to those elements in A plus all the elements
        in B.
    -   But that's double counting! Region AB is both in A and B, so you
        need to substract one instance of AB from the outcome.
    -   Therefore, $N(A \cup B) = N(A) + N(B) - N(AB)$

10. Consider an experiment that consists of six horses, numbered 1
    through 6, running a race, and suppose that the sample space
    consists of the 6! possible orders in which the horses finish. Let A
    be the event that the number-1 horse is among the top three
    finishers, and let B be the event that the number-2 horse comes in
    second. How many outcomes are in the event $A \cup B$?
    -   $A = $ "the number-1 horse is among the top three finishers"
    -   $B = $ "B be the event that the number-2 horse comes in
        second"
    -   $A \cup B = $ "the number-1 horse is among the top three
        finishers and the number-2 horse came second."
    -   For $B$, only one outcome is necessary, that the number-2 horse
        is second, the rest are totally variable.
    -   I think this means that the possible outcomes are therefore:
        $$\frac{5!}{6!}$$ because you're only taking one of the choices
        "off the table."
    -   Similarly, there are $5!$ ways of specifying the position of
        horse one.
    -   So what is $N(AB)$?
        -   There is only one way for the number two horse to be in the
            second position.
        -   There are two options for the first horse to be in the top
            three, then, in position one and position three.
        -   For each of these options, there are 4 choices for the
            unclaimed spot. $2 \times 4!$
            $$N(A \cup B) = \frac{5!}{6!} + \frac{5!}{6!} - (2 \times 4!)$$

11. A 5-card hand is dealt from a well-shuffled deck of 52 playing
    cards. What is the probability that the hand contains at least one
    card from each of the four suits?
    -   This is event is really asking what is the probability that the
        first four cards are of different suits. (The fifth isn't
        relevant because it *has* to be a repreated suit.)
        $$\frac{{52 \choose 1}}{52} \frac{{39 \choose 1}}{51} \frac{{26 \choose 1}}{50} \frac{{13 \choose 1}}{49}$$

12. A basketball team consists of 6 frontcourt and 4 backcourt players.
    If players are divided into roommates at random, what is the
    probability that there will be exactly two roommate pairs made up of
    a backcourt and a frontcourt player?

### Midterm Review Powerpoint

#### Counting

-   **Multiplication principle**
    -   If we can classify a set of objects by a sequence of decisions,
        then the (\# objects) = (\# choices on first decisions) x ... x
        (\# of choices in last decision)
    -   Mathematically,
        $$|A_1 \times A_2 \times ... \times A_n| = |A_1| \cdot |A_2| \cdot ... \cdot |A_n|$$

-   **Permutations**
    -   Number of ways to put $n$ things in order:
        $$n(n - 1)\times(n - 2)\times...\times 2 \times 1 = n!$$
    -   Number of ways to put $k$-out-of-$n$ things in order:
        $$n(n - 1)\times(n - 2)\times ... \times (n - k + 1) = \frac{n!}{(n -k)!}$$

-   **Permutations with repeats**
    -   Ways to order $n$ objects, with $n_1$ alike, ..., $n_r$ alike.
        $$\frac{n!}{n_1! ... n_r!} = {n \choose n_1, ..., n_r}$$

-   **Combinations**
    -   Ways to choose $k$-out-of-$n$ things where order doesn't matter:
        $$\frac{n!}{k!(n - k)!} = {n \choose k}$$

-   **Partitions**
    -   Number of ways to divide $n$ indistinguishable obects in $r$
        non-empty piles: $${n - 1 \choose r - 1}$$
    -   Number of ways to divide $n$ indistinguishable objects in $r$
        piles, empty allowed: $$n + r - 1 \choose r - 1 $$

-   **Binomial theorem**
    $$(x + y)^n = \sum_{k = 0}^n {n \choose k}x^k y^{n-k}$$
-   **Combinatorial identities** $$\sum_{k = 0}^n {n \choose k} = 2^n$$
    $${n \choose k} = {n - 1 \choose k} + {n - 1 \choose k - 1}$$
-   **Multinomial theorem**
    $$(x_1 + ... + x_r)^n =$$
    $$\sum_{0 \lt n_1 \lt ... \lt n_r \lt n} {n \choose n_1, ..., n_r} x_1^{n_1}...x_r^{n_r}$$
    
	-   Sum over all ways to express $n$ as sum of $r$ non-negative
        integers:
        $$0 \le n_1 \le ... \le n_r \le n : n_1 + ... + n_r = n$$

#### Probability

-   **Sample spaces and events**
    -   Sample spaces is a set $S$
    -   Events are subsets of $S$
    -   Intersection of $E$ and $F$: “Both $E$ and $F$ happen”
    -   Union of $E$ and $F$: “Either $E$ or $F$ or both happen”
    -   Complement of $E$: “$E$ does not happen”
    -   $E$ and $F$ are mutually exclusive if intersection of $E$ and
        $F$ is empty

-   **Basic identities**
    -   $P(\emptyset) = 0$
    -   $P(E^c) = 1 - P(E)$
    -   $P(E \cup F) = P(E) + P(F) - P(E \cap F)$
    -   $P(E) = P(E \cap F) + P(E \cap F^c)$
    -   If $P$ and $F$ are mutually exclusive, then
        $$P(E \cup F) = P(E) + P(F)$$

-   **Uniform probability measure**
    -   If all outcomes are equally likely (fair dice, fair coin, random
        card, poker hand, etc) then, $$P(E) = \frac{|E|}{|S|}$$

-   **Conditional probability**
    -   Probability of $E$, given that $F$ happened
        $$P(E|F) = \frac{P(E \cap F)}{P(F)}$$

-   **Bayes's theorem**
    -   Think $E$ is "evidence" and $F$ is "outcome"
        $$P(F|E) = \frac{P(E|F)P(F)}{P(E|F)P(F) + P(E|F^c)P(F^c)}$$

-   **Multiplication rule for conditional probability**
    $$P(E_1 \cap ... \cap E_n) = $$
    $$P(E_1)P(E_2|E_1)P(E_3|E_1\cap E_2) ... $$
    $$P(E_n | E_1 \cap E_2 \cap ... \cap E_{n-1})$$
-   **Indepedant events**
    -   $E$ and $F$ are *independant* if
        $$P(E \cap F) = P(E) \times P(F) $$
    -   Equivilently, $$P(E|F) = P(E) \lor P(F) = 0$$

-   **Prosectutor's fallacy** $$P(E|F) \neq P(F|E)$$

#### Review Problems

1.  How many ways can we walk up/right from point A to point B?

          +----+----+----+ B
          |    |    |    |
          +----+----+----+
          |    |    |    |
          +----+----+----+
          |    |    |    |
          +----+----+----+
          |    |    |    |
        A +----+----+----+

    -   A clever way to solve this problem is to represent "ups" and
        "right" as characters in a string.
    -   You have to traverse "on the lines" - the strings will have to
        be seven characters long.
    -   You can only go "up" four times in any given run.
    -   You can only go "right" 3 times. $$7 \choose 3, 4$$

2.  You have 18 non-identical children.
    1.  Assign them to 4 possibily empty teams.
        -   Again, you can cleverly solve this problem with strings.
        -   But I'll do it with sets just to be different.
        -   You have four sets, $A, B, C, D$, each of which can have can
            have an elements from the set $\lbrace 1, ..., 18 \rbrace$
        -   Because each of the four sets can possibly have 18 children
            in it, there are $4^18$ possibilities.
        -   Gosh that didn't go as well as planned.

    2.  How many ways can 18 identical balls be divided into 4 possibily
        empty groups.
        -   The formula for putting $n$ objects into $r$ possibly empty
            groups is $$n + r - 1 \choose r - 1 $$
        -   There are 18 identical balls ($n$) and 4 possibly empty
            groups ($R$) $$18 + 4 - 1 \choose 4 - 1 $$
        -   Refer to stars and bars, partitions.

3.  How many ways can 18 children be divided into 4 groups so that:
    Group 1 has 4 children, Group 2 has 6 children, Group 3 has 5
    children, Group 4 has 3 children?
4.  Suppose we deal a random 5-card poker hand. What is the probability
    that we get exactly 1 Queen? What about exactly 4 Hearts? Are they
    independent?
    -   $E = $ "get exactly one Queen"
        -   There are 52 choose 5 possible hands.
        -   There are 4 Queens in every deck.
        -   Observe there is symettry.
            $$\frac{{4 \choose 1} \times {48 \choose 4}}{52 \choose 5}$$

    -   $F = $ "exactly four Hearts"
        -   There are 52 choose 5 possible hands.
        -   There are 13 hearts in every deck.
            $$\frac{{13 \choose 4}\times{39 \choose 1}}{52 \choose 5}$$

    -   Events are independant if $P(E \cap F) = P(E) \times P(F) $
        -   What is the probability of getting one Queen and exactly
            four Hearts?
        -   Of course, the Queen *could be* the Heart.
        -   So you have to count the instances that the Queen is the
            fifth card (not heart) as well as those where as the one
            where *it is* a Heart.
        -   There are 12 choose 4 ways of picking an Heart which is
            *not* a queen, and then 3 choose 1 ways of picking a Queen
            which *is not* a Heart.
        -   There is only one Queen of Hearts, and you need 3 more
            hearts out of th remaining 12 Hearts after that.
        -   Then you need to pick 1 of the remaining 36 cards which are
            not Hearts *and* not Queens.
            $$\frac{{12 \choose 4}{3 \choose 1} + {12 \choose 3}{36 \choose 1}}{{52 \choose 5}}$$
        -   I can eyeball that I'd very much doubt this multiplication
            adds up, and if this were the test, I'd show it. But being
            as I know it actually doesn't multiply based on the answers,
            I'm just going to skip the step. "Leave it as an exercise
            for the reader", as textbooks would say.

5.  In a 5-card poker hand, how many ways can we get a 3-of-a-kind? Full
    house does not count.
    -   There are 13 different ranks, and this requires you choose one
        of them.
    -   Of that rank, which has 4 members, you must choose 3 of them.
    -   There are 12 ranks left, of which you must choose 2.
    -   Because full houses don't count (which I assume is when the
        other two cards are of the same suit as well), you have to pick
        1 from 4, and then 1 from 3 (they *can't* be the same).
        $${13 \choose 1}\times{4 \choose 3}\times{12 \choose 2}\times{4 \choose 1}\times{3 \choose 1}$$

### Conditional Probability and Independence - Self Test Problems and Exercises

1.  In a game of bridge, West has no aces. What is the probability of
    his partner’s having (a) no aces? (b) 2 or more aces? (c) What would
    the probabilities be if West had exactly 1 ace?
    -   I would answer this, but like most people under the age of 64, I
        have no idea how bridge works.

2.  The probability that a new car battery functions for over 10,000
    miles is .8, the probability that it functions for over 20,000 miles
    is .4, and the probability that it functions for over 30,000 miles
    is .1. If a new car battery is still working after 10,000 miles,
    what is the probability that
    -   its total life will exceed 20,000 miles?
        -   $E = $ "battery functions for over 10,000 miles"
        -   $F = $ "battery functions for over 20,000 miles"
        -   $G = $ "battery functions for over 30,000 miles"
        -   I think what the question is asking is what is the
            probability that the the battery functions for 20,000 miles
            given that it went for 10,000 miles. I don't *quite* have
            the intuition behind that, but I just kind of "smell" that
            that is what this problem wants.
            $$P(F|E) = \frac{P(E \cap F)}{P(E)}$$
        -   Because $E \in F$, $E \cap F$ is simply $F$.
            $$P(F|E) = \frac{P(F)}{P(E)} = \frac{.4}{.8}$$

    -   its additional life will exceed 20,000 miles?
        -   This is the probability that the car reaches 30,000 miles
            given that it's gone both 20,000 and 10,000.
            $$P(G|E) = \frac{P(E \cap G)}{P(E)} = \frac{.1}{.8}$$

3.  How can 20 balls, 10 white and 10 black, be put into two urns so as
    to maximize the probability of drawing a white ball if an urn is
    selected at random and a ball is drawn at random from it?
    -   This question is actually pretty cool.
    -   I can't quite work out how you'd prove it rigoursly, but the
        basic idea is that the number will always float around 50%
        **unless** you do one clever trick.
    -   Make it so that one of the urns has only one white ball in it,
        making it so 100% of the time you at least get one white.
    -   Then place the rest in the other, waste none of the white on the
        "hole in one" so they jack up the probability on the second
        draw.

4.  Urn A contains 2 white balls and 1 black ball, whereas urn B
    contains 1 white ball and 5 black balls. A ball is drawn at random
    from urn A and placed in urn B. A ball is then drawn from urn B. It
    happens to be white. What is the probability that the ball
    transferred was white?
    -   $P(E) = $ "the transferred ball was white"
    -   $P(F) = $ "the ball drawn from B was white"
        $$P(E|F) = \frac{P(E \cap F)}{P(F)}$$

### Homework 1

2.  Give sample spaces that model the outcomes for the following
    experiments. You may use a regular expression or other formalisms
    that you find convenient.

    1.  Rolling 3 dice:

        $$\lbrace (i, j, k) \:|\: i, j, k \in \lbrace 1, 2, 3, 4, 5, 6 \rbrace\rbrace$$

    2.  Rolling a die until an even result comes up, or the die is
        rolled three times:

        $$\lbrace (i), (ji), (jji), (jjj...ji) \: | \: i \in \lbrace 2, 4, 6\rbrace j \in \lbrace 1, 3, 5\rbrace\rbrace $$

    3.  Tossing a pair of coins until they both come up tails.

        $$\lbrace (i), (j, i), (j, j, i), (j, j, j, ..., i) \: | \: i = (TT), j = \lbrace HH, TH, HT \rbrace\rbrace$$

    4.  Draw 2 balls from an urn which contains 6 balls, each with a
        distinct label from $\lbrace 1,2,3,4,5,6\rbrace$.

        $$\lbrace i,j \: | \: i, j \in \lbrace 1,2,3,4,5,6\rbrace \land i \neq j \rbrace $$

    5.  Draw 1 ball from the same urn, then replace it and draw a ball
        again.

        $$\lbrace i,j \: | \: i, j \in \lbrace 1,2,3,4,5,6\rbrace$$

### Homework 2

2.  If $P(A) = \frac{1}{2}$, $P(B) = \frac{1}{5}$, and
    $P(A\cup B) = 3/5$, find:
    -   $P(A\cap B)$
        -   The idea is that the probability of both $A$ and $B$
            happening is equal to the probability of $A$ happening
            multiplied by the probability of $B$ happeneing.
            $$\frac{1}{2} \times \frac{1}{5} = \frac{1}{10}$$

    -   $P(A^c \cup B)$
        $$P(A^c \cup B) = P(A^c) + P(B) - P(A^c \cap B)$$
        $$\frac{1}{2} + \frac{1}{5} - \frac{1}{10} = .6$$
    -   $P(A^c \cap B)$
        -   The idea is that being as $P(A) = \frac{1}{2}$, the
            complement is equally likely to happen, because $P(S) = 1$
            and $P (A) = 1- P(A^c)$ $$\frac{1}{10}$$

3.  How many elements are there in the set

    $\lbrace x : 10^7 \le x \le 10^8$, and the base 10 representation of
    x has no digit used twice$\rbrace$?

    -   $10^7 = 10000000$, and $10^8 = 100000000$
    -   The smallest number possible is $12345678$
    -   The largest number possible is $98765432$
    -   For the first number, you have 9 total integers to choose from
        (it can't be zero). $$9 \choose 1$$
    -   For the second number, zero is now an option. So likewise,
        $$9 \choose 1$$
    -   Now, for every value after this one, you still have to choose
        one, you just have one less choice, all the way down to there
        being 2 remaining numbers that will be left out of your element.
        $${9 \choose 1}{9 \choose 1}{8 \choose 1}{7 \choose 1}{6 \choose 1}{5 \choose 1}{4 \choose 1}{3 \choose 1}$$

4.  An army output has 19 posts to staff using 30 indistinguishable
    guards. How many ways are there to distribute the guards if no post
    is left empty?

    -   Stars and bars. $${{30 - 1} \choose {19 - 1}}$$

5.  What is the coefficient of $x^{10}y^{13}$ when $(x + y)^{23}$ is
    expanded?

    -   Binomial theorem:
        $$(x + y)^n = \sum_{k = 0}^n {n \choose k}x^k y^{n-k}$$
        -   $n = 23$
        -   $k = 10$ $$(x + y)^23 = {23 \choose 10}x^10 y^{23 - 10}$$

6.  What is the coefficient of $w^{9}x^{31}y^{4}z^{19}$ when
    $(w + x + y + z)^{63}$ is expanded? How many monomials appear in the
    expansion?
    -   This is the multinomial theorem when $r = 4$ and $n = 63$.
        $${63 \choose 4, 9, 19, 32} x_1^{4}x_2^{9}x_3^{19}x_4^{31}$$

### Homework 3

1.  What is the probability that a 5 card hand has exactly 3 spades?
    -   This problem has symmetry, every card is equally likely at any
        given point.
    -   Therefore the answer can be expressed by taking the primality of
        the relevant subset over the sample space.
    -   How many 5 card hands contain exactly 3 spades?
        $${13 \choose 3}{39 \choose 2}$$
    -   The answer is this value over $${52 \choose 5}$$

2.  What is the probability that a 5 card hand has exactly 3 spades,
    conditioned on having at least one spade?
    -   $P(E|F)$ where $E = $ "having 3 spades," and $F = $ "having
        a least one spade" $$P(E|F) = \frac{P(E \cap F)}{P(F)}$$
    -   If you have 3 spades, you definitely have at least one spade.
    -   Therefore, $E \cap F = E$ $$P(E|F) = \frac{P(E)}{P(F)}$$
    -   We know $P(F)$, and will calculate $P(E)$ using the complement.
    -   The complement is that none of the cards are spades.
    -   There are 13 spades in a deck, so there are 39 choose 5 ways of
        getting a hand with no spades.
    -   There are 52 choose 5 total hands, the probability of event $E$
        is: $$ 1 - \frac{{39 \choose 5}}{{52 \choose 5}} $$

3.  Suppose $n$ people each throw a six-sided die. Let $A_n$ be the
    event that at least two distinct people roll the same number.
    Calculate $P(A_n)$ for $n=1,2,3,4,5,6,7$.
    -   For $n_7$, the event that two distinct people roll the same
        number is inevitable.
    -   For the remaining 6 rolls, the complement will be much easier to
        calculate.
    -   What is the likelihood for events 1 through 6 that every roll is
        unique?
    -   $n_1$ will *always* be unique.
    -   $n_2$ will be unique 5 out of 6 times, as $n_1$ rolled some
        number.
    -   $n_3$, similarly, will be unique 4 out of 6 times.
    -   $n_4$ will be unique 3 out of 6 times.
    -   $n_5$ will be unique 2 out of 6 times.
    -   $n_6$ will be unique 1 out of 6 times.
    -   (Note that $n_7$ will never be unique.)
        $$P(A_i) = 1 - \prod_{n = 0}^i \frac{7 - i}{6}$$

4.  Suppose we draw 2 balls at random from an urn that contains 5
    distinct balls, each with a different number from $\{1,2,3,4,5\}$,
    and define the events $A$ and $B$ as
    $$A = \text{"5 is drawn at least once"} \quad \text{and} \quad
        B = \text{"5 is drawn twice"}$$ Compute $P(A)$ and $P(B)$.
    -   There are four ways to pick five along with another number.
        $$P(A) = \frac{4}{5 \choose 2} = 0.4 $$
    -   Observe that there is zero probability of getting *any* number
        twice. $$P(B) = 0$$

5.  In the previous problem, suppose we place the first ball back in the
    urn before drawing the second. Compute $P(A),P(B),P(A|B),P(B|A)$ in
    this version of the experiment.
    -   I think it would be helpful, again, to consider the complement.
    -   The complement of $A$, is that 5 is never drawn.
    -   Each time you draw, considering that you replace, you have a one
        in five chance of picking 5.
    -   For the complement, then, you have a 4 in five chance of drawing
        *not* five. (Apparently not that helpful.)
        $$P(A) = 1 - \frac{4}{5}^2 = .36$$
    -   Okay I think I messed that one up.
    -   Much simpler version:
        -   There are $5^2$ possible drawings.
        -   There are 4 ways of drawing 5 first, 4 ways of drawing 5
            second, and 1 way of drawing 2 fives which makes for nine
            ways. $$P(A) = \frac{9}{25} = .36$$

    -   For $P(B)$, there are still 25 possible ways of drawing.
    -   What's changed is that there is now only one way to draw five
        twice - actually getting it twice.
    -   Therefore, $$\frac{1}{25}$$
    -   For $P(A|B)$, the translation is, "what is the probability of A
        given than B happened."
    -   Well if five was drawn twice, it was *definitely* drawn once.
        $$P(A|B) = \frac{P(A \cap B)}{P(B)}$$
    -   $A \cap B$ is equal to $B$. $$P(A|B) = \frac{P(B)}{P(B)} = 1$$
    -   For $P(B|A)$, the "translation" is, what is the probability of
        rolling a five twice given that a five was rolled once?
        $$P(B|A) = \frac{P(B \cap A)}{P(A)}$$
    -   $B \cap A$ is still $B$
        $$P(B|A) = \frac{\frac{1}{25}}{.36} = \frac{1}{9}$$

6.  Suppose $5$ percent of cyclists cheat by using illegal doping. The
    blood test for doping returns positive $98$ percent of the people
    doping and $12$ percent who do not. If Lance’s test comes back
    positive, what the probability that he is doping? (Ignoring all
    other evidence, of course...)
    -   This is a Bayes's theorem type of question.
        $$P(F|E) = \frac{P(E|F)P(F)}{P(E|F)P(F) + P(E|F^c)P(F^c)}$$
    -   Think of $E$ as "evidence" and $F$ as "outcome."
    -   Call $E$ "Lance's blood test came back positive."
    -   Call $F$ "Lance was doping."
    -   Before we know anything else, Lance being a random cyclist, we
        know the probability of his doping, $P(F) = .05$
    -   We also know the probability of Lance's test coming back
        positive given that he doped, $P(E|F) = .98$
    -   We *also* know the probability of Lance's test coming back
        positive given that he *didn't* dope, $P(E|F^c) = .12$.
    -   Finally, we *also* know the probability of Lance *not* doping,
        $P(F^c) = .95$.
    -   We now have all the elements for Bayes's theorem.
        $$P(F|E) = \frac{(.98)(.05)}{(.98)(.05) + (.12)(.95)}$$

March 6th, 2013 - Lecture
-------------------------

### Random variables

-   **Random variables**: $A$ random variable on a sample space, space
    $S$ is any function from $S$ to $\mathbb{R}$.
    $$X \cdot S \to \mathbb{R} $$
-   **Example**: Tossing 3 coins
    $$S = \lbrace HHH, ... TTT \rbrace$$
    -   Define $X = $ "number of heads that came up."
        $$X \cdot R \to R$$
        $$X(HHH) = 3$$
        $$X(TTT) = 0$$
    -   $Y =$ "number of tails that come up."
    -   Then, $Y(w) = 3 - X(w)$ for all $w \in S$.
    -   $Z = $ "winnings in game where you win a dollar for each H, lose
        a dollar for each T."
        $$Z(HHH) = 3$$
-   If $X$ and $Y$ are RVs (random variables), and $a, b, c \in \mathbb{R}$,
    then $Z = aX + bY + c$ is a RV.
    -   **Indicator random variable** for each event $A \subseteq S$
-   **Example**: Suppose we toss $b$ balls into $N$ bins. Define $X_i$ as
    the number of balls that land in the $i$th bin (for $i = 1, ... , n$).
    So $X_1 + X_2 = $ numbers of balls in the 1st or 2nd bincs,
    $$\forall w \left(\sum_{i = 1}^n X_i(w) = b\right)$$
-   **Example**: When rolling two dice
    $$X((i, j)) = i + j$$
    $$\to Y((i, j)) = |i - j|$$

### Range of a random variable

-   **Range of a RV**: The set of values that $X$ takes.
-   **Example**: For $X = $ "number H's in 3 win tosses."
    $$Range(X) = \lbrace0,1,2,3\rbrace$$
    $$Range(X) = \lbrace0,1,2,3\rbrace$$
    
### Partition of a random variable

            S
        +-------+    x     +-------+ 
        |  A_1  | -------> |  a_1  |
        |  A_2  | -------> |  a_2  |
        |  A_3  | -------> |  a_3  |
        |   .   |          |   .   |
        |   .   | -------> |   .   |
        |   .   |          |   .   |
        |  A_k  | -------> |  a_k  |
        +-------+          +-------+
        
$$A_1 = \lbrace w \in S \: : \: X(w) = a_1 \rbrace $$
$$A_2 = \lbrace w \in S \: : \: X(w) = a_2 \rbrace $$

-   Suppose $Range(X) = \lbrace a_1, ... a_k \rbrace$,
    -   For each $i$, define $A_i = \lbrace w \in S \: : \: X(w) = a_i \rbrace$ for $i = 1 ... k$.
    $$A_1 \subseteq S$$
    -   **Claim**: For all $i \neq j$, $A_i \cap A_j = \emptyset$.
    -   **Claim**: Every $w \in S$ is some $A_i$.
    -   This means that $\lbrace A_1, ..., A_k \rbrace$ "partition $S$."
-   **Example**: If $x = $ "number of Hs in 3 tosses," what is $A_x$?
    $$Range(X) = \lbrace 0, 1, 2, 3 \rbrace (k = 4)$$
    -   Need $\lbrace A_0, A_1, A_2, A_3 \rbrace$ where $A_i = \lbrace w \in S \: : \: X(w) = i \rbrace$
        $$A_0 = \lbrace TTT \rbrace$$
-   **Example**: Flip a coin until we get $H$, on $n$ flips
    $$S = \lbrace H, TH, ..., T^{n - 1}H, T^n \rbrace$$
    -   $X = $ "number of flips"
    -   What is $A_x$?
        -   $Range(X) = \lbrace1, ... , n \rbrace$
        -   Need $A_1, ..., A_n$ where $A_i = X^{-1}(i)$

### Frequency Function of a random variable

-   Formalize "$X$ takes value $I$ with probability $p$"
-   If $Range(X) = \lbrace a_1, ... , a_n \rbrace$, we write
    $$P(X = a_i) = P(A_i) = P({w : X(w) = a_i})$$
    -   **Frequency function of x** (also probability mass function):
        $$f_x(a_i) = P(x = a_i)$$
        
-   **Example**: $X = $ "number of Hs in 3 tosses"
    -   $f_x(0) = P(X = 0) = \frac{1}{8}$
    -   $f_x(1) = P(X = 1) = \frac{3}{8}$
    -   $f_x(2) = P(X = 2) = \frac{3}{8}$
    -   $f_x(3) = P(X = 3) = \frac{1}{8}$
    
### Independent random variables

-   **Independent**: If $X$ and $Y$ are RVs on $S$, they are **independant** if for all $i, j$
    $$P(X = i \land Y = j)$$
    
### Repeated Indepedent Trials

-   Start with a sample space $T$ with probability measure $P$.
-   Formalize repeating $n$ times:
    $$S^{(n)} = \lbrace w = (w_1, ..., w_2) \: : \: w_i \in T \rbrace = T^n$$

### Bernoulli trials

-   Sample space $S = \lbrace s, f \rbrace$, "success" and "failure."  
    -   Define $P(s) = p$, $P(f) = 1 - p$
    -   Consider repeat $n$ times $S^{(n)} = $ "all string of length $n$ with $s$ and $t$"
        $$P^{(n)}(w) = P(w_1)P(w_2) ... P(w_n)$$
        
March 11th, 2013 - Reading
--------------------------

### 4.1 Random Variables

-   These quantities of interest, or, more formally, these real-valued 
    functions defined on the sample space, are known as **random 
    variables**.
-   The total number of events that occur without specifying the order
    in which they came up.

#### Example 1a

-   Suppose that our experiment consists of tossing 3 fair coins. 
    If we let Y denote the number of heads that appear, then Y is a 
    random variable taking on one of the values 0, 1, 2, and 3 with 
    respective probabilities
    
    $$P\lbrace Y = 0 \rbrace = P \lbrace (T, T, T) \rbrace = \frac{1}{8} $$
    $$P\lbrace Y = 1 \rbrace = P \lbrace (H, T, T), (T, H, T), (T, T, H), \rbrace = \frac{3}{8} $$
    $$P\lbrace Y = 2 \rbrace = P \lbrace (H, H, T), (T, H, H), (H, T, H), \rbrace = \frac{3}{8} $$
    $$P\lbrace Y = 3 \rbrace = P \lbrace (H, H, H) \rbrace = \frac{1}{8} $$
    
March 11th, 2013 - Lecture: More on Random Variables; Expectation
-----------------------------------------------------------------

### Introduction

-   Topics: More on binomial random variables. 
-   Geometric and negative binomial random variables. 
-   Definition of expectation and the alternative formulation.
-   Reading: See notes part 3 on Sakai.

### Warmup for Homework

-   **Example**: Deal a 5 card hand, let $X = $ "the number of aces",
    $Y = $ "the number of spades", and $Z = X(w) \cdot Y(w)$
    $$ Range(X) = \lbrace 0, 1, 2, 3, 4 \rbrace $$
    $$ Range(Y) = \lbrace 0, 1, 2, 3, 4, 5 \rbrace $$
    $$ Range(Z) = Range(XY) = \lbrace 0, ..., 9 \rbrace $$

#### Are $X$ and $Y$ Independent?

-   If indepedent, then dor all $i \in Range(X), j \in Range(Y)$
    $$ P(X = i \cap Y = j) = P(X = i)P(Y = j) $$
    $$ P(X = 2 \cap Y = 5) = \emptyset $$
    -   But $P(X = 2) \gt 0, P(Y = 5)$ so not independent.

### Binomial Frequency Function

-   $S^{(n)} = $ "all strings of length $N$ formed with $s$ and $t$ characters"
-   $S^{(n)}(w) = P(w_1) ... P(w_n)$ where $w = w_1 ... w_n$
    $$ p^k (q - p)^{n - k} $$
-   $S_n = $ "the number of $s$s in $n$ trials"
-   $Range(S_n) = \lbrace 0, 1, ... n \rbrace $
-   $f_{s_n}(k) = {n \choose k}P^k (1 - p)^{n - k} = P(S_n = k)$
-   Need
    $$ \sum_{k = 0}^n f_{s_n}(k) 1$$
    $$ = \sum_{k = 0}^n {n \choose k} P^k (1 - p)^{n - k} = $$
    $$ (p + P(1 - p))^n = 1^n = 1 $$
    
-   **Example**: An airplane has 200 seats, but we should 202 tickets.
    Assume passengers fail to show with probability $0.03$ *indepedantly*.
    What is the chance that flight is over full?
    -   This "$s$" is "passenger $i$ fails to show."
    -   $X = $ "the number of passengers who failr to show"
    -   Event we want is $X = 1 \cup X = 1$
        $$ P(X = 0) = {202 \choose 0}p^0 (1 - p)^{202 - 0} = .03$$
        $$ P(X = 1) = {202 \choose 2}p^1 (1 - p)^{202 - 1}$$
        
### Repeat Bernoulli trial until success

-   $S'= \lbrace s, fs, ffs, ... \rbrace $
-   $P^{(n)} = $ as before
-   Define $W_1 = $ "the number of trials until success."
-   $Range(W_1) = \lbrace 1, 2, ... \rbrace$
-   $A_{w_1} = \lbrace A_1, A_2, ... \rbrace$, where $A_i = \lbrace W : W_1(w) = i \rbrace \subseteq S$.
-   $P(i) = P(W_1 = 1) = P(A_i) = (1 - p)^{i - 1} p$
    $$\sum_{i  = 1}^\infty (1 - p)^{i - 1}$$
    $$ = p \cdot \frac{1}{p} =  $$
    
### Negative Binomial Frequency Fun

-   Repeat Bernoulli unti lwe get $k$ $s$'s
    $$ S = f\ast s f\ast s ... f \ast s $$
    -   $W_k = $ "number of triials until $k$ $s$'s"
    -   $A_{w_k} = \lbrace k, k + 1, ... \rbrace
    -   $A_k = \lbrace ss ... s \rbrace$
    -   $A_{k + 1} = \lbrace fs ... s, sfs ... s, ..., ss...sfs \rbrace$
        $$|A_{k+1}| = k$$
        
### Miracle of the linearity of expectation

-   For any random variables $X$ and $Y$, the expectation splits and you
    sum it.
    $$E(X + Y) = E(X) + E(Y)$$
    
### St. Petersburg Paradox

-   You pay c dollars
-   I flip coin until H. Say it takes $i$ flips.
-   I give you $2^{i - 1}$ dollars

March 13th, 2013 - Homework 4
-----------------------------

1.  (3 points) In the card game bridge we deal 13-card hands to 4
    players named North, South, East, and West (all 52 cards are dealt).
    What is the probability that East and West have no spades?

    -   The total number of possibilities in the sample space for this
        situation is the total number of possible card orders over the
        number of cards each player is dealt factorial raised to the
        fourth.

        $$\frac{52!}{13!^4}$$

    -   There are 13 Spades in a deck of cards, and then 39 non-Spade
        cards.

    -   For the hands of East and West, who collectively represent 26
        cards, and who are vying for 39 non-Spade cards, this is the
        number of possibilities:

        $$39 \choose 26$$

    -   North and South also account for 26 total cards, and they are
        vying for the remaining cards including Spades. Twenty-six cards
        were taken out of the deck by East and West.

        $${26 \choose 26} = 1$$

    -   The probability is therefore:

        $$\frac{{39 \choose 13}\times{26 \choose 13}\times{26 \choose 13}\times{13 \choose 13}}{\frac{52!}{13!^4}}$$

2.  (4 points) An urn contains $n>0$ white balls and $m>0$ black balls.
    Suppose we draw two balls without replacement. What is the
    probability that the balls are of the same color? What if we draw
    them with replacement? Show your work. Which of these probabilities
    is larger? Briefly explain some intuition for why one should be
    larger.

    -   Without replacement

        -   There are $n + m$ balls in all, and we’re interested in
            choosing 2 of them. The sample space is:

            $${m + n \choose 2}$$

        -   Call $W$ “drawing two white balls” and $B$ \`\`drawing two
            black balls. Then $W \cup B$ is either of those events
            happening or both.

        -   The events are mutually exclusive, the drawings cannot all
            be the same for the same drawing.

            $$P(W \cup B) = P(W) + P(B)$$
            $$= \frac{{m \choose 2} + {n \choose 2}}{{m + n \choose 2}}$$

    -   With replacement

        -   The events are, again, mutually exclusive.

        -   Being as the balls are placed back in the urn, each event is
            equally likely to occur.

        -   Count the number of either color, place it over total balls,
            and multiply it by itself to represent that the event has to
            happen twice.

        -   Do the same for the other color, add the two values.

            $$\left(\frac{m}{m + n}\right)^2 + \left(\frac{n}{m + n}\right)^2$$

3.  (4 points) Again consider an urn with $n>0$ white balls and $m >0$
    black balls. Suppose we draw $r\geq 1$ balls from the urn without
    replacement. What is the probability that we draw exactly $k$ white
    balls?

    -   The probability of getting a white, where $i$ is the number of
        total balls already drawn, is

        $$\left(\frac{n - i}{m + n - i}\right)$$

    -   And the probability of getting a black under the same conditions
        is

        $$\left(\frac{m - i}{m + n - i}\right)$$

    -   So draw $k$ white balls, and then transfer the counter to
        drawing the remaining balls to avoid over-counting

        $$\left(\prod_{i = 0}^{k - 1} \frac{n - i}{m + n - i} \right) \times \left(\prod_{i = k}^{r - 1} \frac{m - (i - k)}{m + n - i} \right)$$

4.  (4 points) A box contains a mixture of cubes and spheres and any of
    these objects can be either white or black. Suppose the box contains
    $4$ black cubes, $6$ black spheres, $6$ white cubes, and $x$ white
    spheres. Consider the experiment of drawing a random object from the
    box, and let $A$ be the event that a cube is drawn and $B$ be the
    event that a black object is drawn. If $A$ and $B$ are independent,
    what is $x$?

    -   The probability of a cube being drawn is the total number of
        cubes over the total number of cubes and spheres.

        $$\frac{4 + 6}{4 + 6 + 6 + x}$$

    -   The probability of a black object being drawn is similarly the
        total number of black objects divided by the total number of
        objects

        $$\frac{6 + 4}{4 + 6 + 6 + x}$$

    -   Consider the complement of $A \cup B$, it is the event that a
        non-black and non-cube item is draw, which is a white sphere.

        $$P(x) = P((A \cup B)^c)$$

5.  (10 points total) Two fair dice are rolled. Define the random
    variables $X =$ the sum of the two rolls, $Y =$ the maximum of the
    two rolls, $Z =$ the absolute value of the difference of the two
    rolls and $W = XY$ (i.e., the product of $X$ and $Y$).

    1.  (2 points) What are ${\mathrm{Range}}(X)$,
        ${\mathrm{Range}}(Y)$, ${\mathrm{Range}}(Z)$ and
        ${\mathrm{Range}}(W)$?

        -   ${\mathrm{Range}}(X) = \lbrace 2, 3, 4, ... , 11, 12 \rbrace $

        -   ${\mathrm{Range}}(Y) = \lbrace 1, 2, 3, 4, 5, 6 \rbrace $

        -   ${\mathrm{Range}}(Z) = \lbrace 0, 1, 2, 3, 4, 5 \rbrace$

        -   ${\mathrm{Range}}(W) = \lbrace i \times j \: : \: i \in \lbrace 2, 3, 4, ... , 11, 12 \rbrace, j \in \lbrace 1, 2, 3, 4, 5, 6 \rbrace\rbrace $

    2.  (2 points) What are the partitions ${\mathcal{A}}_X$ and
        ${\mathcal{A}}_Z$?

        -   ${\mathcal{A}}_X$

            -   $2 = 1 + 1$

            -   $3 = 1 + 2$

            -   $4 = 1 + 3 = 2 + 2$

            -   $5 = 1 + 4 = 3 + 2$

            -   $6 = 1 + 5 = 2 + 4 = 3 + 3$

            -   $7 = 1 + 6 = 2 + 5 = 3 + 4$

            -   $8 = 2 + 6 = 3 + 5 = 4 + 4$

            -   $9 = 3 + 6 = 4 + 5$

            -   $10 = 4 + 6 = 5 + 5$

            -   $11 = 5 + 6$

            -   $12 = 6 + 6$

        -   ${\mathcal{A}}_Z$

            -   $0 = 1 - 1 = 2 - 2 = 3 - 3 = 4 - 4 = 5 - 5 = 6 - 6$

            -   $1 = 6 - 5 = 5 - 4 = 4 - 3 = 3 - 2 = 3 - 2 = 2 - 1$

            -   $2 = 5 - 4 = 5 - 3 = 4 - 2 = 3 - 1$

            -   $3 = 6 - 3 = 5 - 2 = 4 - 1$

            -   $4 = 6 - 2 = 5 - 1$

            -   $5 = 6 - 1$

March 13th, 2013 - Lecture: Linearity of expectation
----------------------------------------------------

### Introduction

-   Topics: 
    -   Linearity of expectation. 
    -   Expectation of binomial, geometric, and negative binomial frequency functions. 
    
-   Applications to computing expectations: 
    -   Birthday problem, 
    -   balls into bins, 
    -   and coupon collecting.
    
-   Reading: See notes part 3 on Sakai.

March 25th, 2013 - Lecture: Markov's Inequality; Begin Variance
---------------------------------------------------------------

### Introduction

-   Topics: 
    -   Markov's inequality for non-negative random variables. 
    -   Definition of variance and some calculations of variance.
    
-   Reading: See notes part 4 on Sakai.
            
March 26th, 2013 - Office Hours
-------------------------------

1.  Norwa on number one
2.  Notes on number two
    -   There are no tricks, apply the formula.
        $$E(X) = \sum_{a_i \in R(X)}a_i P(X = a_1)$$
    -   What is E(X) for X = minimum of two dice?
        $$P(x = 6) = P(\lbrace(6, 6) \rbrace) = \frac{1}{36} $$
        $$P(x = 5) = P(\lbrace (5, 6), (6, 5), (5, 5) \rbrace) = \frac{3}{36}$$
3.  Notes on number three
    -   Find $E(X)$
        1.  Find some random variables $X_1, ..., X_n$ such that $x = x_1 + ... + x_n$
        2.  Now $E(X) = E(x_1) + ... E(x_n)$
    -   We're going to buy x boxes of cereal
    -   Call x the number of unique toys
    -   We're always stopping at n boxes.
    -   Imagine there six types of toys, red, green, blue, purple, orange, indigo.
        -   When I open my n boxes, I check off the color I got until I get them all.
        -   Call $x_1$ "got a red toy indicator"
        -   There's another for each toy, 1 through 6.
4.  Notes on number four
    -   There m men and w women in a line in a single line, random order, all orders equally likely.
    -   You can pick any pair of seats, this pair has formed a couple, if a mw or a wm occur.
    -   Use linearity of expectation
    -   x = number of couples
    
                m w m
            _ _ _ _ _ _ _ _
            1 2 3 4 5 6 7 8
            x_1
            
    -   $E(X_1) = $ P(couple in a seat 1 and 2)
5.  Notes on five
    -   What is a Bernoulli trial?
    -   So you see this problem there are $2^12$ different outcomes, different trials.
        -   Big number, don't want to work it out by hand.
    -   We know something about this though, it's connected to something we've seen before.
        $$ E(\frac{S}{12}) $$

March 27th, 2013 - Homework 4
-----------------------------

1.  (10 points total) Two teams $x$ and $y$ are playing each other in
    the World Series, which is a best-of-seven-game match that ends when
    one team wins 4 games. Assume that team $x$ wins each game with
    probability $p$, and that the outcome of each game constitutes an
    independent trial.

    1.  (0.5 points) What is the probability that $x$ wins the first
        four games?

        -   There is one way for x to win in four, and that’s winning
            four in a row.

        -   By the multiplicity principle, we can multiply the chance of
            winning each game to get the probability of winning all
            games.

            $$p^4$$

    2.  (2 points) What is the probability that $x$ wins four games
        after at most five game have been played?

        -   Sample space, strings, x character means x won, y character
            means y won.

                        
                        xxxx
                        yxxxx
                        xyxxx
                        xxyxx
                        xxxyx
                        
                        

        -   The team represented by y cannot win at the end because
            after 4 x wins, the games halt.

        -   P(x wins in less than five games) =
            $P(\mathrm{\{xxxx, yxxxx, xyxxx, xxyxx, xxxyx\}})$

        -   There is a $(1 - p)$ chance of y winning.

        -   The x team still needs to win 4 games, which has a
            probability of $p^4$.

        -   Multiplying these two values gets you the likelihood that
            this happens for any given instance of x winning in less
            than five games.

        -   To get all of the possible less than 5 games combinations,
            multiply by the number there are, which is 4.

        -   Then, add the probability of just 4 straight victories.
            $$(1 - p) \times p^4 \times 4 + p^4$$

    3.  (2 points) What is the probability that $x$ will win four games
        before $y$ wins four games? (i.e., What is the probability that
        $x$ wins the Series?)

        -   To begin, lets enumerate some possibilities using strings.

            $$\{\mathrm{xxxx}\}$$

            $$\{\mathrm{yxxxx,
                    xyxxx,
                    xxyxx,
                    xxxyx}\}$$

            $$\{\mathrm{yyxxxx,
                    yxyxxx,
                    ...,
                    xxxyyx}\}$$

            $$\{\mathrm{yyyxxxx,
                    yyxyxxx,
                    ...,
                    xxxyyyx}\}$$

        -   These are all the possibilities for x winning. Name these
            $X_1$ through $X_4$ and notice the sum of their
            probabilities to be the probability that $x$ wins four
            games.

        -   For $X_3$, there are ${5 \choose 2,3}$ ways of ordering x
            and y, y has to win twice, and x still has to win four
            times.

        -   You have to subtract off the cases where there is a y at the
            end,

            $${4 \choose 1,3} \times (1 - y)^2 \times p^4$$

        -   For $X_4$, there are ${6 \choose 3,3}$ ways of ordering x
            and y, y has to win thrice, and x still has to win four
            times.

            $${5 \choose 2,3} \times (1 - y)^3 \times p^4$$

        -   Now add 4 straight victories:

            $${4 \choose 1,3} \times (1 - y)^2 \times p^4 + {5 \choose 2,3} \times (1 - y)^3 \times p^4 + p^4$$

    4.  (0.5 points) Calculate and simplify your answer in part (c) when
        $p=1/2$ and when $p=2/3$.

        -   $p = 1 / 2 : 1/2$

        -   $p = 2 / 3 : 1808/2187$

    5.  (1 point) Let $X$ be the random variable that counts the number
        of games that are played. What is ${\mathrm{Range}}(X)$?

        $$R(X) = \{4, 5, 6, 7 \}$$

    6.  (2 points) What is $P(X=7)$?

        $${6 \choose 3}(1 - p)^3 p^4 + {6 \choose 3} p^3 (1 - p)^3 p^4$$

    7.  (2 points) What is $P(X\geq 6)$?

        $${5 \choose 2}(1 - p)^2 p^4 + {5 \choose 2} p^2 (1 - p)^4 + {6 \choose 3} (1 - p)^3 p^4 + {6 \choose 3} p^3 (1 - p)^4$$

2.  (4 points) Suppose we roll two fair dice. Let the random variable
    $X=$ “the minimum of the two dice” and $Y =$ “the absolute value of
    the difference of the two dice”. Find $E(X)$ and $E(Y)$.

    -   $E(X)$

        -   The formula to solve this is

            $$E(X) = \sum_{a_i \in R(X)}a_i P(X = a_1)$$

        -   The sample space has a cardinality of 36, as there 6 choices
            for each of the two choices.

        -   All rolls are equally likely in a fair dice.

        -   Starting with the highest element in the range (which is the
            set containing 1 through 6), there is only one way 6 can be
            the minimum.

            $$P(x = 6) = P(\lbrace(6, 6) \rbrace) = \frac{1}{36}$$

        -   There are 3 ways of “getting 5”, and that’s rolling two
            fives, and then both variations of a five and a six.

            $$P(x = 5) = P(\lbrace(5, 5), (5, 6), (6,5) \rbrace) = \frac{3}{36}$$

        -   Apply the same pattern,

            $$P(x = 4) = P(\lbrace(4, 4), (4, 5), (5,4), (4,6), (6,4) \rbrace) = \frac{5}{36}$$
            $$P(x = 3) = P(\lbrace(3, 3), (3, 4), (4,3), (3,5), (5,3), (3,6), (6,3) \rbrace) = \frac{7}{36}$$
            $$P(x = 2) = P(\lbrace(2, 2), (2, 3), (3,2), (2, 4), (4, 2), (2, 5), (5,2), (2,6), (6,2)) = \frac{9}{36}$$

        -   Notice that there 2 more each time.

            $$P(x = 1) = \frac{11}{36}$$

        -   Now sum them and multiply them by their value ($a_i$) to
            find expected value,

            $$E(X) = \left(6 \times \frac{1}{36}\right) + \left(5 \times \frac{3}{36}\right) + \left(4 \times \frac{5}{36}\right) + \left(3 \times \frac{7}{36}\right) + \left(2 \times \frac{9}{36}\right) + \frac{11}{36} = 2.5277777778$$

    -   $E(Y)$

        -   The range is $\{0, 1, 2, 3, 4, 5\}$.

        -   This is another application of the formula
            $$E(X) = \sum_{a_i \in R(X)}a_i P(X = a_1)$$

        -   There are 6 ways of getting 0, $\{6 - 6, 5 - 5, ...\}$. For
            $i = 0$, $$0 \times P(X = 0) = 0 \times \frac{6}{36} = 0$$

        -   There are 10 ways of getting 1,
            $\{6 - 5, 5 - 6, 5 - 4, 4 - 5, 4 - 3, 3 - 4, 3 - 2, 2 - 3, 2 - 1, 1 - 2\}$.
            For $i = 1$, $$1 \times P(X = 1) = 1 \times \frac{10}{36}$$

        -   There are 8 ways of getting 2,
            $\{6 - 4, 4 - 6, 5 - 3, 3 - 5, 4 - 2, 2 - 4, 1 - 5, 5 - 1\}$.
            For $i = 2$,
            $$2 \times P(X = 2) = 2 \times \frac{8}{36} = \frac{4}{9}$$

        -   There are 6 ways of getting 3,
            $\{6 - 3, 3 - 6, 5 - 2, 2 - 5, 4 - 1, 1 - 4\}$. For $i = 3$,
            $$3 \times P(X = 3) = 3 \times \frac{6}{36} = \frac{2}{3}$$

        -   There are 4 ways of getting 4,
            $\{6 - 2, 2 - 6, 5 - 1, 1 - 5\}$. For $i = 4$,
            $$4 \times P(X = 4) = 4 \times \frac{4}{36} = \frac{4}{9}$$

        -   There are 2 ways of getting 5, $\{6 - 1, 1 - 6\}$. For
            $i = 5$,
            $$5 \times P(X = 5) = 5 \times \frac{2}{36} = \frac{5}{18}$$

        -   We know we’ve covered the sample space because the sum of
            the specific instances is the same as the cardinality of the
            sample space.

        -   The expected value,
            $$E(X) = 0 + \frac{2}{9} + \frac{4}{9} + \frac{2}{3} + \frac{4}{9} +  \frac{5}{18} = 1.94 \approx 2$$

3.  (4 points) Suppose boxes of cereal are filled with a random prize,
    each drawn from independently and uniformly from $6$ possible
    prizes. If we buy $N$ boxes of cereal, what is the expected number
    of distinct prizes we will collect?

    -   Let $X_1 ... X_6$ be the identifier for each of 6 unique toys

        $$E\left(\sum I_{E_i}\right) = \sum_{i = 1}^6 E(I_{E_i}) = 6(1 - \left(5/6)\right)^n$$

4.  (4 points) A group of $m$ men and $w$ randomly sit in a single row
    at a theater. If a man and woman are seated next to each other we
    say they form a couple. (Couples can overlap, meaning that one
    person can be a member of two couples.) What is the expected number
    of couples?

    -   Use linearity of expectation for each pair of seats.

    -   Let $x$ equal the number of seats.

    -   Then, $E(X_1) = P($couple in a seat 1 and 2$)$,
        $E(X_2) = P($couple in a seat 2 and 3$)$, etc.

    -   For any given seat, there is a $\frac{1}{2}$ chance of their
        being a man or a woman in the seat.

    -   The four possibilities are {mw, wm, mm, ww}.

5.  (3 points) Suppose an experiment tosses a fair coin twice; the
    experiment “succeeds” if both tosses were Heads. We repeat this
    experiment for 12 independent trials. Let $N$ be the random variable
    that counts the fraction of trials that are successful (so
    $N = S/12$, where $S$ is the number of successful trials). Find
    $E(N)$.

    $$E(N) = E\left(\frac{S}{12}\right)$$ $$S = \{ x_1 + ... + x_12 \}$$
    $$\frac{1}{12} E(S)$$
    $$E(S) = \sum_{a_i \in R(S)} a_i \times P(X_i)$$
    $$P(X_i) = \frac{1}{4}$$ $$E(S) = 12 \times E(X_i)$$
    $$\frac{1}{12}E(S) = 12 \times \frac{1}{4}$$ $$E(S) = \frac{1}{4}$$
        
March 27th, 2013 - Lecture: Computing Variances
-----------------------------------------------

### Introduction 

-   Topics: 
    -   Expectation of a function of a random variable. 
    -   Variance of a sum of independent random variables. 
    -   Variance of the bernoulli, binomial, geometric, and negative binomial distributions.

-   Reading: See notes part 4 on Sakai.

<table border=1 style="text-align:center;margin-left:auto; margin-right:auto;">
  <tbody>
    <!-- Results table headers -->
    <tr>
      <th></th>
      <th>"story"</th>
      <th>$R(X)$</th>
      <th>fx</th>
      <th>$E$</th>
      <th>$V$</th>
    </tr>
    <tr>
      <td>Bernoulli(P)</td>
      <td>s/f with prob p</td>
      <td>$\lbrace 0, 1 \rbrace$</td>
      <td>$p, 1 + p$</td>
      <td>$p$</td>
      <td>$p(1 - p)$</td>
    </tr>
    <tr>
      <td>Binom(n, p)</td>
      <td>#$s$ in $n$ trials</td>
      <td>$\lbrace 0, ... , n \rbrace $</td>
      <td>$f_x(i) = {n \choose i} p^i (1 - p)^{n - i}$</td>
      <td>$pn$</td>
      <td>...</td>
    </tr>
    <tr>
      <td>Geom(p)</td>
      <td># of trials until first s</td>
      <td>$\lbrace 1, 2, ... \rbrace $</td>
      <td>$f_x(i) = (1 - p)^{i - 1} p$</td>
      <td>$\frac{1}{p}$</td>
      <td>...</td>
    </tr>
    <tr>
      <td>NegBiom(k,p)</td>
      <td># trials until kth s</td>
      <td>$\lbrace k, k + 1, ... \rbrace$</td>
      <td>$f_x (i) = {i - 1 \choose k - 1} p^k (1 - p)^{i -k}$</td>
      <td>$k \times \frac{1}{p}$</td>
      <td>...</td>
    </tr>
  </tbody>
</table>

April 1st, 2013 - Lecture: Covariance and Chebyshev's Inequality
----------------------------------------------------------------

### Topics 

-   Variance of a sum of dependent random variables and the definition of covariance. 
-   Properties of covariance. Independence implies correlation but the converse does not hold. 
-       Statement of Chebyshev's inequality and a basic application.

### Introduction

-   If $X$ and $Y$ are indepedant, then 
    $$V(X + Y) = V(X) + V(Y)$$
    
-   If not, then equality may or may not hold.
-   **Example**: A case where equality does not hold.
    -   Take $P(X = 1) = \frac{1}{2}$, $P(X = 0) = \frac{1}{2}$, $x = 1 \to Y = 0$, $x = 1, Y = 1$.
        $$V(Y) = \frac{1}{4}$$
    -   So 
        $$V(X) + V(Y) = \frac{1}{4} + \frac{1}{4} = \frac{1}{2}$$
    -   $V(X + Y)$ equals 0? $X + Y$ will always be 1.
        $$V(X + Y) \lt V(X) + V(Y)$$
        
### Variance

-   "Swinging together"
    $$V(X + Y) \lt V(X) + V(Y)$$
    
-   "Swings unrelated"
    $$V(X + Y)  =  V(X) + V(Y)$$
    
-   "Swings are opposite each other"
    $$V(X + Y) \gt V(X) + V(Y)$$
    
-   We want to measure "how much they're together or opposite."
-   The **covariance of $X$ and $Y$** is defined to be:
    $$Cov(x, y) = E[E(x - E[x])(y - E[y])]$$
    
-   Intuition
    -   "Swing together"
        $$Cov(X, Y) \gt 0$$
    
    -   "Swings unrelated"
        $$Cov(X, Y)  =  0$$
        
    -   "Swings opposite"
        $$Cov(X, Y) \lt 0$$
        
-   **Example** (non rigourous pictures)
    -   Examples, $x$ is height and $y$ is shoe size
        $$Cov(X, Y) \gt 0$$

              v |               .
              a |             . .
              l |          . . .
              u |        . . .
              e |      . . .
                |    . .  .
              y |    . . 
                |  . 
              0 +-----------------
               0    value of X
    
    -   Examples, $x$ is temp and $y$ is sales of hot chocolate
        $$Cov(X, Y) \lt 0$$
           
              v | .
              a |  . .     
              l |   .  . . 
              u |    .  .  . 
              e |     .  .  .
                |      .  .  .
              y |        .   .
                |            .
              0 +-----------------
               0    value of X
               
-   **Formula**:
    $$Cov(X, Y) = E(XY) - E(X) \times E(Y)$$
    
-   **Claim**: If $X, Y$ are indepedant, $Cov(X, Y) = 0$
    -   **Proof**
        $$Cov(X, Y) = E(XY) - E(X)E(Y)$$
        $$= E(X)E(Y) - E(X)E(Y)$$
        $$= 0$$
        
### Tchbycheff's Inequility

-   Recall Markov's give tail bound base only on $E(X)$
-   Chebyshev's give tail bound using $E(X)$ and $V(X)$
-   **Chebyshev's Theorem**: Let $X$ be a random variable with $E(X) = \mu$
    -   Then for any $\epsilon \gt 0$.
    
-   **Example**: Roll a fair die 100 times and let $Z$ be the sum
    and $X_1$, ..., $X_{100}$ be the outcomes.
    -   What's the probability that $Z$ are within 50 of its mean?
        

               
April 2nd, 2013 - Office Hours
------------------------------

### Number 3

$$Cov(X,Y) = E(XY) - E(X)E(Y)$$

-   Call $z_1$ the first roll, $z_2$ the second.

$$E(XY) = \sum_{w \in S} X(w) Y(w) P(w)$$

-   We can do this in principle, it takes fifteen minutes.
-   More elegantly, however, take two random variables that represents the rolls, and it's nice because they're indepedant.

$$X = z_1 + z_2$$
$$Y = z_1 - z_2$$

$$XY = (z_1 + z_2)(z_1 - z_2)$$
$$ = z_1^2 - z_2^2 $$
$$E(XY) = E(z_1^2) - E(z_2^2) $$
$$ = 0 $$

### Banach-Torski Paradox

-   There are lots of functions which are not integrable.
-   Take the function $f(x)$, which is 0 if x is rational, 1 otherwise.
-   $[0, 1] \to \mathbb{R}$
    $$ \int_{0}^{1} f(x)dx$$
-   Ball in 3-space, cut it up into peices and put them in sets, move the set around.
-   And you can double the volume! (???)
-   Axiom of choice.

> Physics is looking around you and drawing conclusions,
> but something really meaningful to me is that what you have infallible premises,
> you have an infallible conclusion. <cite>David Cash</cite>

### Zero-knowledge proof

-   Zero knowledge proofs are a different way of thinking of proofs.
    -   A regular proof involves a prover and verifier.
    -   If each step is right, the then conclusion is right, and you've proven something.
    
-   If the statement "$x$ is not prime" (where $x$ is a hundred digit number).
-   You want to prove to a server that I know my password, you know I know it, but you don't know my password.

#### Journal of Craptology: Zero-Knowledge Proofs for Kids

-   There's a Waldo, you don't know where he is, but there is one.
-   Take a big piece of cardboard, and cut a Waldo sized hole, and show the person Waldo.
-   They know there's a Waldo, but have no knowledge about where the Waldo is.

April 3rd, 2013 - Lecture
-------------------------

### Public polling

-   Say we want to estimate how much of the country will vote
    independent in the next presidential election.
    -   Call $n$ random people and ask what they'll do, with a country
        of $m$ people.
    -   Average response to estimate fraction of country that will vote
        independent.
    -   How big should $n$ be to be wintin $\pm 3 \%$ with probability $\ge 95\%$
    -   Let $x_i = $ "ith person we call say will vote indepedant."
        $$ A_n = \frac{x_1 + ... + x_n}{n} $$
    
    -   Say a $p$ fraction of the country will vote independant (unknown).
    -   Want to know:
        $$ P(|A_n - p| \gt 0.03) \le 0.05 $$
    
    -   Use Cheb.
        $$ P(|A_n - p| \gt 0.03) \le \frac{V(A_n)}{(0.03)^2} \le \frac{1}{n \times 0.03^2}$$
        
        $$ V(A_n) = V(\frac{x_1 + ... x_n}{n}) = \frac{1}{n} V(X_1) $$
        
        $$ = \frac{p(1 - p)}{n} $$
        
        $$ \le \frac{1}{n} $$
    
    -   Want $\frac{1}{n \times 0.03^2} \le 0.05 $
    
### Back to counting! Trees

-   Counting number of binary trees with $n$ nodes
    1.  $n = 0$, $a_0 = 1$
    1.  $n = 1$, $a_1 = 1$
    1.  $n = 2$, $a_2 = 2$
    1.  $n = 3$, $a_3 = 5$
    1.  $n = 4$, $a_4 = 14$
        $$a_n = \frac{1}{n + 1} {2n \choose n} $$
        
### Generating functions

-   Want to find formula for $a_0, a_1, a_2, ...$. 
-   Write $\lbrace a_i \rbrace_{i = 0}^\infty$ or $\lbrace a_i \rbrace$
    for the sequence.
-   **Definition**: The *generating function for* $\lbrace a_i \rbrace$
    is the function $A(x)$ defined by
    $$ A(x) = \sum_{k = 0}^\infty a_k x^k $$

-   (Treat as "formula sum", meaning ignore convergence)
-   Problem sovling recipe for generating functions
-   Want to find $a_0, a_1, a_2, ... , a_n$
    1.  Show that $A(x) has some simple "closed form"
    
April 8th, 2013 - Lecture
-------------------------

### Announcements

-   Ungraded HW on Sakai
-   New noes on generating functions
-   From *Applied Combinatorics* by Alan Tucker
-   HW07 online tonight, due next Monday
-   Office hours this weeks:
    -   3:00PM to 4:00PM on Thursday
    -   2:00PM to 3:00PM on Friday
    
### Generating functions revisited

-   **Question**: How many solutions are there to $z_1 + z_2 = 11$, with
    $z_1, z_2$ as non-negative integers.
    -   Some mediocre ways:
        -   You can list these by hand ...
        -   There are 12, you can list them but I won't.
        -   It can also be a stars and bars problem, 11 stars, 2 groups, 
            empty allowed.
    
    -   But consider multipling out:
        $$(1 + x + x^2 + ... + x^{11})(1 + x + x^2 + ... + x^{11})$$
    -   This is going to be:
        $$\sum_{x = 0}^{22} a_k x^k$$
    -   Take a look at this pattern:
        $$a_0 = 1 | ()$$
        $$a_1 = 2 | (x^0 x^1 + x^1 x^0 = 2x)$$
        $$a_2 = 3 | (x^0 x^2 + x^1 x^1 + x^2 x^0 = 3x^2)$$
    -   Now consider that $a_11 = 12$. This is not a coefficient.
    -   Somehow counting the number of polynomials counted this other number we wanted.
    -   Generating functions are about doing this counting with shortcuts.
    
-   Considering multiplying out $(1 + x + x^2)^4 = $
    $$(1 + x + x^2)(1 + x + x^2)(1 + x + x^2)(1 + x + x^2)$$
    -   How to "expand"?
        -   Pick $x^0, x^1, x^2$ from each group, multiplying choices.
        -   Repeat for all possible choices ($3^4$ of them).
        -   Add up results, collect like terms.
        -   Each term is of the form:
            $$x^{e_1}x^{e_2}x^{e_3}x^{e_4}$$
        -   Each $e_i = 0, 1, 2$
        -   Expanded version collects for all possible allowed.

-   What is the coefficient of $x^5$ in $(1 + x + x^2)^4$.
    -   This equals the number of ways $x^5$ "shows up" in terms.
    -   Coefficient is number of ways to wrte $5 = e_1 + e_2 + e_3 + e_4, e_i = 0, 1$
    
-   **Examples**: Find polynomial where $a_k =$ is equal to the number of ways
    to pick $k$ balls from a pile of 3 green, 2 white, 3 blue, and 3 gold.
    -   Stated as "equ problem", this means that $a_k = $ numer of solutions to
        $$e_1 + e_2 + e_3 + e_4 = k, e_i \in \lbrace 0 2 3 4 \rbrace$$
        -   With grreen, white, blue, and gold (respectively)
        
-   **Example**: Same problem, but 7 green, 2 blue, 5 gold.
    -   The polynomial is
        $$(x^0 + x^1 + ... + x^7)(x^0 + x^1)(x^0 + x^1 + ... + x^5)$$
        
-   **Example**: Find the polynomial with $a_k = $ "number of ways to pick 6 objects
    where each one is one of 3 types, but you can't have four of any one type."
    
April 15th, 2013 - Homework 7
-----------------------------


1.  (1.5 points each) Find the generating function for the sequence
    $a_0, a_1, a_2, \ldots$, where $a_k$ is each of the following. Your
    solution does not need to be closed form.

    1.  $a_k = $ the number of solutions to $e_1 + e_2 + e_3 = k,$ where
        $0 \leq e_i \leq 4$ for each $i$.

        $$(1 + x^1 + x^2 + x^3 + x^4)^3$$

    2.  $a_k = $ the number of solutions to $e_1 + e_2 + e_3 + e_4 = k,$
        where $0 \leq e_i < 4$ for each $i$, $e_1$ is odd, and $e_2$ is
        even.

        $$(x^1 + x^3)(x^0 + x^2)(1 + x^1 + x^2 + x^3 + x^4)^2$$

    3.  $a_k = $ the number of solutions to $e_1 + e_2 + e_3 + e_4 = k,$
        where $0 \leq e_i$ for each $i$.

        $$\left(\sum_{i = 0}^{\infty} x^i \right)^4$$

    4.  $a_k = $ the number of solutions to
        $e_1 + e_2 + e_3 + e_4 + e_5= k,$ where $0 \leq e_i$ for each
        $i$, $e_1$ and $e_3$ are odd, and $e_2$ is even.

        $$\left(\sum_{i = 0}^{\infty} x^{2i + 1} \right)^2 \times \left(\sum_{i = 0}^{\infty} x^{2i} \right) \times \left(\sum_{i = 0}^{\infty} x^{i} \right)^2$$

2.  (3 points each) Model the following problems using a generation
    function, which does not need to be in closed form:

    1.  Count the number of outcomes of rolling $6$ dice that sum to
        $r$.

        $$(x_1 + x_2 + x_3 + x_4 + x_5 + x_6)^6, \: 1 \le x_i \le 6$$

    2.  Count the number of outcomes of rolling $6$ dice that sum to
        $r$, where the first three dice are odd and the last three are
        even.

        $$(x_1 + x_3 + x_5)^3 \times (x_2 + x_4 + x_6)^3, \: 1 \le x_{2i + 1} \le 3, 0 \le x_{2i} \le 2$$

    3.  Count the number of outcomes of rolling $6$ dice that sum to
        $r$, where for each $i$ the $i$-th dice is not equal to $i$ (so
        the first die is not $1$, the second is not $2$, and so on).

        $$= (x^2 + x^3 + x^4 + x^5 + x^6) \times (x^1 + x^3 + x^4 + x^5 + x^6) \times$$
        $$(x^1 + x^2 + x^4 + x^5 + x^6) \times (x^1 + x^2 + x^3 + x^5 + x^6) \times$$
        $$(x^1 + x^2 + x^3 + x^4 + x^6) \times (x^1 + x^2 + x^3 + x^4 + x^5)$$

3.  (1.5 points each) Find the following coefficients. Show your work.

    1.  The coefficient of $x^{10}$ in the series expansion of
        $(x^5+x^6 + x^7+ \cdots)^8$.

        $$\mathrm{DNE}$$

    2.  The coefficient of $x^{20}$ in the series expansion of
        $(x+x^2 + x^3+x^4+x^5) (x+x^2 + x^3+x^4+\cdots)^5 $.

        $$18 \choose 14$$

    3.  The coefficient of $x^{12}$ in the series expansion of
        $x^2/(1+x)^8$.

        $$8 + 10 - 1 \choose 10$$

    4.  The coefficient of $x^{12}$ in the series expansion of
        $1/(1+x^3)^2$.
        
April 15th, 2013 - Lecture
--------------------------

-   **Idea**: To solve $a_1, a_2, ... $
    -   Part 1: Define generating function
        $$A(x) = \sum_{k = 0}^\infty$$
        -   "Pull out" the initial conditions
        -   Substitute recurance relation formula
        -   Expand, algebra, etc until you can substitute $A(x)$
        -   Get $A(x) =$ "some formula of A(x)"
        -   Solve for A(x)
        
    -   Part 2: Find the series expansion 
        -   Easiest case, like above, $A(x)$ is in the table.
        -   Work harder, use partial fraction decomposition
        
April 17th, 2013 - Notes pt. 5
------------------------------

### Generating functions

-   Let $a_0, a_1, ...$ (or more briefly $\lbrace a_i \rbrace$) denote
    an infinite sequence of real numbers. Its **generating function** is
    defined by
    
    $$ A(s) = \sum_{k = 0}^{\infty} a_k s^k = a_0 + a_1 s + ... + a_k s^k + ... $$
    
    -   We are not claiming this series converges.
    -   In some sense, you can view this as a formalism for infinite series.
    -   When the series does converge with a function with algebraic properties,
        we will make use of this correspondance.
        
- Facts:
    1.  $ A(0) = a_0$
        -   The first element in the sequence.
        
    2.  $ A(1) = \sum_{k = 0}^{\infty} a_k$
        -   The sum of the elements.
    
    3.  $ A`(1) = \sum_{k = 1}{\infty} k a_k s^{k - 1} |_{s = 1}$
        -   Differentiate each term of the sum in (1) and substitute.
        
    4.  $ A + B = \sum_{k = 0}^\infty (a_k + b_k) s^k$
        -   Sum
        
    5.  $ A(s)B(s) = a_0 b_0 + (a_0 b_1 + a_1 b_0) s + ... $
        $ + (a_0 b_k + ... + a_k b_0) s^k                  $
        -   Multiplication, convolutions
        
### Generating Functions and Recurrence Relations

-   Given a recurrence relation for the sequence $\lbrace a_i \rbrace$,
    1.  Deduce from it an equation satisfied by the generation function
    
        $$ a(x) = \sum_{i} a_i x^i $$
        
    2.  Solve this equation to get an explicit expression for the generating
        function.
    3.  Extract the coeeficient $ a_n $ of $ x^n $ from $ a(x) $ by expanding
        $a(x)$ as a power series.
        
-   Alternate steps [wikiHow](http://www.wikihow.com/Solve-Recurrence-Relations)
    1.  Consider the sequence 2, 5, 14, 41, 122 ... given by this formula:
        
        $$ a_0 = 2 $$
        $$ a_n = 3 a_{n - 1} - 1 $$
        
    2.  Write the genrating function of the sequence. A generating function is 
        simply a formula power series where the coeeficient of $ x^n $ is the
        nth term of the sequence.
        
        $$ A(x) = \sum_{k = 0}^{\infty} a_k x^k $$
        
    3.  Manipulate the generating function. The objective in this step is to find
        an equation that will allow us to solve for the generating function 
        $ A(x) $. User the formula for the sum a geomtric series.
        
        -   Original formula:
        
        $$ A(x) = \sum_{k = 0}^{\infty} a_k x^k $$
        
        -   "Take out" when a is 0:
        
        $$ A(x) = 2 + \sum_{k = 1}^{\infty} a_k x^k $$
        
        -   Make the first term addition by referring to the original
            definition of this series.
        
        $$ A(x) = 2 + \sum_{k = 1}^{\infty} (3 a_{k - 1} - 1) x^k $$
        
        -   Split the sum
        
        $$ A(x) = 2 + \sum_{k = 1}^{\infty} 3 a_{k - 1} x^k -  \sum_{k = 1}^{\infty} x^k $$
        
        -   Now recognize that if you take out the 3 as well as *an* $x$, 
            you have the original formula.
            
        $$ = 2 + 3x A(x) - \frac{x}{1 - x} $$
        
    4.  Solve for $A(x)$:
    
        $$ A(x) = \frac{ 3x - 2 }{ (3x - 1)(1 - x)} $$
        
    5.  Find the coefficient of $x^n$ using partial fractions or some other
        method.
    6.  Write the formual for $a_n$ by identifying the coefficient of $x^n$ in
        $A(x)$.
        
        $$ a_n = \frac{3^{n + 1} + 1}{2} $$
        
April 17th, 2013 - Lecture
--------------------------

-   Counting number of binary trees on n nodes
    -   Let $b_n$ be the number of binary trees given $n$ nodes.
    -   $ b_0 = 1$, $b_1 = 1$, $b_2 = 2$, etc
    -   What does an n node ree "look like"?

Practice Final Exam
-------------------

1.  What is the coefficient of $x^{12} x^{9}$ when $(x + y)^{21}$ is expanded?
	How many monomials are in the expansion?
	-   This requires the binomial theorem.
	-   You plug in $21$ for $n$ and $9$ for $k$.
		$$22 \choose 12$$
2.  If $P(A \cap B) \lt P(A)$, is it always true that $P(A|B) \lt P(A)$? 
    Either prove it, or disprove it by finding a counterexample.
	-   You can disprove this with the values $P(A) = .5$, P(B) = .25$.
3.  If we throw $n$ balls into $m$ urns, what is the probability that all of
    the balls land in exactly 1 urn? At most 2 urns?
	-   The number of possible ways to distribute $n$ balls into $m$ possible
		urns is, according to the partition formula,
		$$n + m - 1 \choose m - 1$$
	-   Let this be our sample space.
	-   For exactly one urn, how many ways are there to distribute all the balls
		into one urn?
		$$m$$
	-   Making our answer $m$ divided by the sample space.
	-   How many ways are there to distribute $n$ balls into at most $2$ urns?
		This means that $1$ urn is possible, but we're interested in $2$ urns
		*as well*.
	-   The number of ways to divide $n$ indistinguishable balls into $r$ possibly
		empty bins is:
		$$n + r - 1 \choose r - 1$$
	-   Our answer, therefore is,
		$$\frac{m + {n + 2 - 1 \choose 2 - 1}}{n + m - 1 \choose m - 1}$$
4.  Suppose we shuffle a standard deck of 52 cards and deal a 5 card hand.
    What is the probability we get a straight? What about a straight flush?
	-   Our sample space is the beyond astronmically large:
		$$56 \choose 5$$
	-   Let's look at how many straights there are:
		
			A  2  3  4  5  6  7  8  9  10  J  Q  K  A
			+-----------+  +-----------+
		       +-----------+  +------------+
			      +-----------+  +------------+
			         +-----------+  +------------+
							+----------+    +-----------+
	-   I count 10 different ways of getting a straight.
	-   So compared to our sample space, you must select 1 of 10 straights,
		then for each card, you must pick a suit.
		$$\frac{{10 \choose 1}{4 \choose 1}^5}{56 \choose 5}$$
	-   If we're only interested in the case where all of the suits are the
		same, you can simply take of the $5$th power on the suit value.
5.  We roll a die 10 times. Let $X$ be the number of time a roll of 1, 2, or
    3 comes up. Find the range of $X$, $P(X = 3)$, $E(X)$, and $V(X)$.
	-   So we're interested in the frequnecy function where we get "the number
		of trials until the first success" which is "geometric."
	-   Our range, therefore, is from $0$ to potentially inifinite.
	-   The probability of success for any given trial, because of linearity
		of expectation, is:
		$$\frac{3}{6}$$
		because there are $3$ values that represent a sucess and $6$ total possible
		values.
		$$P(X = n) = \frac{1}{2}(1 - \frac{1}{2})^{n - 1}$$
		$$E(X) = \frac{1}{\frac{1}{2}}$$
		$$V(X) = \frac{1 - \frac{1}{2}}{(\frac{1}{2})^2}$$

6.  Suppose again we shuffle a standard deck of 52 cards and deal a five card
    hand. Let $A_i$ be the event that the $i$-th card is red.
    1.  What is the probability of the event $E = $ "exactly two cards
        are red"?
		-   You can exploit symettry and linearity of expectation here.
		-   There are $56$ cards in the first drawing, $55$ cards in the second
			drawing.
		-   There are $26$ red cards in the first drawing, $25$ red cards
			in the second (because we already "got one" in this calculation).
		-   Now the rest of the cards have to be not red out of $26$, $25$, $24$
			non-red cards in a deck of $54$, $53$, $52$.
		-   Every fraction must be multiplied by the multiplicative principle.
			$${5 \choose 2}\left(\frac{26}{56} \times \frac{25}{55} \times \frac{26}{54} \times \frac{25}{53} \times \frac{24}{52}\right)$$
		-   Please note that there are in fact $52$ cards in a deck.

    2.  What is the probability of the event $F = $ "the first two cards
        are red"? 
		-   This is like the first question, but we just don't care about the
			cards after the first two. They could be red, they might not be,
			whatever the case, we do not have to account for it.
			$$\frac{26}{56} \times \frac{25}{55}$$
	3.  Are $E$ and $F$ indepedant? Explain your answer.
		-   Two events are indepedant if and only if the probability of their
			intersection is equal to the product of their individual probabilities.
			Formally,
			$$P(A \cap B) = P(A) \times P(B)$$
		-   What is $A \cap B$? It is both that "the first two cards are red" and
			"exactly two cards are red." Which is the event that only the first
			two cards are red. 
		-   The probability that both of these events happen is not equal to
			the product of the individual probilities, and therefore this
			particular tuple of events are dependent on one another.

7.  Consider an experiment where we flip three coins. Suppose we repeat this
	experiment until we get all Heads. Let $X$ be the random variable that
	is the number of experiments needed. Find $E(X)$ and $V(X)$.
	-   Again, we are dealing with a geometric frequency function because
		we're interested in the number of trials until the first success.
	-   The success of any given trial is going to be the cube of the 
		success of a single coin toss,
		$$\left(\frac{1}{2}\right)^3$$
	-   Therefore, based on the formula for the geometric frequency function,
		$$P(X = n) = \left(\frac{1}{2}\right)^3 \left(1 - \left(\frac{1}{2}\right)^3\right)^{n - 1}$$
		$$E(X) = \frac{1}{\left(\frac{1}{2}\right)^3}$$
		$$V(X) = \frac{1 - \left(\frac{1}{2}\right)^3}{\left(\left(\frac{1}{2}\right)\right)^3)^2}$$

8.  Consider the same experiment as before, except now we flip the coins 100
	times. Let $W$ be the random variable representing the number of time you
	get all Heads. Is the frequency function of $W$ Bernoulli, binomial,
	geometric, or negative binomial? Find $E(W)$ and $V(W)$. Use Chebyshev's
	inequality to bound the probability that $|W - E(W)| is more than 10.
	-   This is a binomial frequency function, as it represents the number
		of successes in $n$ trials.
	-   The range is limited by $n$.
	-   $n$ is equal to $100$, as we are performing the trial that many times.
	-   The probability of success in any given trial is still:
		$$ \left(\frac{1}{2}\right)^3$$
		$$P(X = k) = {100 \choose k} \left(\frac{1}{2}\right)^3 \left( 1 - \left( \frac{1}{2} \right)^3\right)^k$$ 
		$$E(X) = \left(\frac{1}{2}\right)^3 \times 100 $$
		$$V(X) =  \left(\frac{1}{2}\right)^3 \left(1 - \left(\frac{1}{2}\right)^3\right)\times 100$$	
9.  Consider a group of $n$ married couples which are seated at a rectangular
	table with $n$ seats on each side. Let $X$ be a random variable that counts
	the number of married couples that are seated next to each other. Find
	$E(X)$.
10. Suppose that 51 percent of babies are born girls. Suppose also that there
	is a prenatal test such that 98 percent of the baby girls come back
	positive. Use Bayes Theorem to compute the probability that the baby
	is a girl.
	-   Bayes's theorem:
		$$ P(F|E) = \frac{P(E|F)P(F)}{P(E|F)P(F) + P(E|F^c)P(F^c)} $$
	-   $E = $ "the test for girl is positive"  
	-   $F = $ "the baby is a girl" = $.51$
	-   $P(E|F) = $ "the prenatal test is right" $ = .98$
		$$ \frac{.98 \times .51}{.98 \times .51 + .02 \times .49} $$
11. Give the generating function with the $n$-coefficient equal to the number
	of ways to solve $e_1 + e_2 + e_3 = n$ with $e_1, e_2 \ge 0$ and $e_3$ a
	multiple of $3$. Give a close form version of your function.
	$$e_1 = x^0 + x^1 + x^2 + x^3 ...$$
	$$e_2 = x^0 + x^1 + x^2 ... $$
	$$e_3 = x^0 + x^3 + x^6 + x^9 ... $$
	-   Referring the "the chart", not that $e_1$ and $e_2$ are of the form:
		$$ \frac{1}{x - 1} $$
	-   And similarly, $e_3$ is of the form:
		$$ \frac{1}{x^3 - 1} $$
	-   Yielding the closed form:
		$$ \left( \frac{1}{1 - x} \right)^2 \left( \frac{1}{1-x^3} \right)$$
    
12. Find a formula for $a_n$, which is defined by the following recurrence
	relation for all $n \gt 0$:
	$$a_0 = 9$$
	$$a_n = 2a_{n - 1} + 2$$
	$$2a_{n - 1} 2 + 9 = a_n + a_0 $$
	$$\sum_{n = 0}^{\infty} a_n x^n $$
	$$x^n (2a_{n - 1} $$

13. Consider the coin flipping game, where player $A$ pays $B$ one dollar
	for each Heads, and vice versa for each Tails. (The coin is unbiased here.)
	Let $X_1$ be the random variable recordin the first time player $A$ is
	"ahead." Find $P(X_1 \le 7)$. What is the probability that $X$ is odd?
	Even?
14. Continuing with the coin flipping game, also define $X_2$ to record the
	first time $A$ is up two dollars, $Z_1$ be the first time any player is
	up one dollar, and $Z_2$ the first time any player is up two dollars. 
	Which pairs of random variables from $\lbrace X_1, X_2, Z_1, Z_2 \rbrace$
	are indepedant? Let $W = Z_2 - Z_1$. Is $W$ indepedant of $Z_1$? Explain
	your answers carefully, but explicit calculations are not necessary.



