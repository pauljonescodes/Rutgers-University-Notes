Discrete Structures II <small>pt. II with Professor David Cash</small>
======================================================================

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