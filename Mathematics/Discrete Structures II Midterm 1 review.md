Introduction to Discrete Structures <small>Midterm 1 Review</small>
===================================================================

Review Sheet 1
--------------

### Set Theory Review

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

### Probability Theory

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

### Conditional Probability

-   **Conditional probability formula**

$$ P(B|A) = \frac{P(A \cap B)}{P(A)} $$

-   **Hypotheses**

$$ P(A) = \sum_{i = 1}^{n} P(H_1)P(A|H_i) $$

-   **Bayes' rule**

$$P(H_i|A) = \frac{P(A|H_1)P(H_1)}{\sum_{j = 1}^n P(H_j)P(A|H_j)}$$

### Independence

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

Axioms of Probability - Self Test Problems and Exercises
--------------------------------------------------------

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

Midterm Review Powerpoint
-------------------------

### Counting

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
    $$(x_1 + ... + x_r)^n = \sum_{0 < n_1 < ... < n_r < n} {n \choose n_1, ..., n_r} x_1^{n_1}...x_r^{n_r}$$
    -   Sum over all ways to express $n$ as sum of $r$ non-negative
        integers:
        $$0 \le n_1 \le ... \le n_r \le n : n_1 + ... + n_r = n$$

### Probability

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

### Review Problems

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

Conditional Probability and Independence - Self Test Problems and Exercises
---------------------------------------------------------------------------

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

Homework 1
----------

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

Homework 2
----------

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

Homework 3
----------

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

2.  Suppose $n$ people each throw a six-sided die. Let $A_n$
    be the event that at least two distinct people roll the same number.
    Calculate $P(A_n)$ for $n=1,2,3,4,5,6,7$.
    -   For $n_7$, the event that two distinct people roll the same
        number is inevitable.
    -   For the remaining 6 rolls, the complement will be much easier
        to calculate.
    -   What is the likelihood for events 1 through 6 that every
        roll is unique?
    -   $n_1$ will *always* be unique.
    -   $n_2$ will be unique 5 out of 6 times, as $n_1$ rolled some
        number.
    -   $n_3$, similarly, will be unique 4 out of 6 times.
    -   $n_4$ will be unique 3 out of 6 times.
    -   $n_5$ will be unique 2 out of 6 times.
    -   $n_6$ will be unique 1 out of 6 times.
    -   (Note that $n_7$ will never be unique.)
        $$P(A_i) = 1 - \prod_{n = 0}^i \frac{7 - i}{6}$$

3.  Suppose we draw 2 balls at random from an urn that
    contains 5 distinct balls, each with a different number from
    $\{1,2,3,4,5\}$, and define the events $A$ and $B$ as
    $$A = \text{"5 is drawn at least once"} \quad \text{and} \quad
    B = \text{"5 is drawn twice"}$$ Compute $P(A)$ and $P(B)$.
    -   There are four ways to pick five along with another 
        number.
    $$P(A) = \frac{4}{5 \choose 2} = 0.4 $$
    -   Observe that there is zero probability of getting *any* 
        number twice.
    $$P(B) = 0$$

4.  In the previous problem, suppose we place the first ball
    back in the urn before drawing the second. Compute
    $P(A),P(B),P(A|B),P(B|A)$ in this version of the experiment.
    -   I think it would be helpful, again, to consider the
        complement.
    -   The complement of $A$, is that 5 is never drawn.
    -   Each time you draw, considering that you replace,
        you have a one in five chance of picking 5.
    -   For the complement, then, you have a 4 in five chance
        of drawing *not* five. (Apparently not that helpful.)
        $$P(A) = 1 - \frac{4}{5}^2 = .36$$
    -   Okay I think I messed that one up.
    -   Much simpler version:
        -   There are $5^2$ possible drawings.
        -   There are 4 ways of drawing 5 first, 4 ways of 
            drawing 5 second, and 1 way of drawing 2 fives
            which makes for nine ways.
            $$P(A) = \frac{9}{25} = .36$$
    -   For $P(B)$, there are still 25 possible ways of
        drawing.
    -   What's changed is that there is now only one way
        to draw five twice - actually getting it twice.
    -   Therefore,
        $$\frac{1}{25}$$
    -   For $P(A|B)$, the translation is, "what is the
        probability of A given than B happened."
    -   Well if five was drawn twice, it was *definitely*
        drawn once.
        $$P(A|B) = \frac{P(A \cap B)}{P(B)}$$
    -   $A \cap B$ is equal to $B$.
        $$P(A|B) = \frac{P(B)}{P(B)} = 1$$
    -   For $P(B|A)$, the "translation" is, what is the 
        probability of rolling a five twice given that 
        a five was rolled once?
        $$P(B|A) = \frac{P(B \cap A)}{P(A)}$$
    -   $B \cap A$ is still $B$
        $$P(B|A) = \frac{\frac{1}{25}}{.36} = \frac{1}{9}$$

5.  Suppose $5$ percent of cyclists cheat by using illegal
    doping. The blood test for doping returns positive $98$ percent of
    the people doping and $12$ percent who do not. If Lance’s test comes
    back positive, what the probability that he is doping? (Ignoring all
    other evidence, of course...)
    -   This is a Bayes's theorem type of question.
        $$P(F|E) = \frac{P(E|F)P(F)}{P(E|F)P(F) + P(E|F^c)P(F^c)}$$
    -   Think of $E$ as "evidence" and $F$ as "outcome."
    -   Call $E$ "Lance's blood test came back positive."
    -   Call $F$ "Lance was doping."
    -   Before we know anything else, Lance being a random cyclist,
        we know the probability of his doping, $P(F) = .05$
    -   We also know the probability of Lance's test coming back 
        positive given that he doped, $P(E|F) = .98$
    -   We *also* know the probability of Lance's test coming back
        positive given that he *didn't* dope, $P(E|F^c) = .12$.
    -   Finally, we *also* know the probability of Lance *not* doping,
        $P(F^c) = .95$.
    -   We now have all the elements for Bayes's theorem.
        $$P(F|E) = \frac{(.98)(.05)}{(.98)(.05) + (.12)(.95)}$$