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
    
March 11th, 2013 - Lecture
--------------------------

### Warmup for Homework

-   **Example**: Deal a 5 card hand, let $X = $ "the number of aces",
    $Y = $ "the number of spades", and $Z = X(w) \cdot Y(w)$
    $$ Range(X) = \lbrace 0, 1, 2, 3, 4 \rbrace $$
    $$ Range(Y) = \lbrace 0, 1, 2, 3, 4, 5 \rbrace $$
    $$ Range(Z) = Range(XY) = \lbrace 0, ..., 9 \rbrace $$

#### Are $X$ and $Y$ Indepedent?

-   If indepedent, then dor all $i \in Range(X), j \in Range(Y)$
    $$ P(X = i \cap Y = j) = P(X = i)P(Y = j) $$
    $$ P(X = 2 \cap Y = 5) = \emptyset $$
    -   But $P(X = 2) \gt 0, P(Y = 5)$ so not indepedent.

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
    
-   **Example**: An airplan has 200 seats, but we should 202 tickets.
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