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