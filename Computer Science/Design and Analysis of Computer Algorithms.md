Design and Analysis of Computer Algorithms <small>with Professor Kostas Bekris</small>
=========================================================================

Syllabus
--------

### Topics

We will cover a large subset of the following and possibly some new
algorithmic topics and applications, as time permits:

-   Mathematical tools. Review of mathematical background, concepts of
    algorithm design, complexity, asymptotics, induction, and
    randomization. Fibonacci numbers. Euclidean gcd algorithms.
    Universal hashing.

-   Divide and conquer. Fast integer multiplication; recurrences; the
    master theorem; mergesort; randomized median and selection
    algorithms; quicksort; fast matrix multiplication.

-   Sorting. Lower bounds for comparison-based sorting; binsort and
    radix sort.

-   Dynamic programming; Paradigm of SPs in DAGs; longest increasing
    subsequence; approximate string matching; integer and (0,1) knapsack
    problems; chain matrix multiplication; single-pair reliable SPs,
    all-pairs SPs; independent sets.

-   Graph search. Graph classes and representations; depth first search
    in undirected and directed graphs; topological search; strongly
    connected components. Breadth first search and layered DAGs.

-   Shortest Paths (SPs) in digraphs. Single-source SPs for nonnegative
    edge weights; priority queues and Dijkstra; SPs in DAGs;
    single-source SPs for general edge weights. Maximum adjacency
    search.

-   Greedy algorithms. Spanning trees and cuts, analysis of union-find
    and path compression; MST algorithms; randomized algorithm for
    global minimum cuts; approximate set cover.

-   Network flows. Max flow min cut theorem and integrality; fast
    algorithms; disjoint (s,t)-dipaths; maximum bipartite matching &
    minimum vertex cover. Global minimum cuts.

-   Elements of NP-completeness & problem reductions.
-   NP-hard problems. Search and selected approximation algorithms.

### Prerequisites

Courses:

-   CS 112 Data Structures
-   CS 206 Introduction to Discrete Structures II

We assume (and briefly review early on in the class) elements of
discrete mathematics, such as logarithms, proofs by induction, series
and sums, permutations, asymptotics (big-Oh, big-Omega notation), basics
of solving recurrences, as well as concepts of programming and data
structures, e.g., linked lists, stacks, queues, trees, binary search,
recursion, hashing, priority queues, graph algorithms, sorting.

### Reading Material

The class will primarily draw upon material from the following book:

-   "Algorithms" by Dasgupta, Papadimitriou & Vazirani, McGraw Hill,
    2008.

The following book may also be used as reference:

-   "Introduction to Algorithms" by Cormen, Leiserson, Rivest & Stein,
    McGraw Hill (The chapters in the calendar below refer to the 2nd
    edition)

The books are not required for the class. Students are expected to take
notes during the presentation of the material in the classroom and the
recitations. Homeworks and exams will be based on the presented
material.

### Exams

There will be three exams: two midterms and one final. The first midterm
will cover the material of the first third of the course, and the second
midterm will cover the second third of the course. The final exam will
cover material from the entire class. Check the tentative schedule for
updates. All exams will be in-class on a date arranged and announced
ahead of time.

A missed exam draws zero credit. Emergencies will be considered upon
submitting a University-issued written verification to the Instructor;
for assistance contact your Dean's Office. Also, check the definition of
[Final Exam](http://sasundergrad.rutgers.edu/forms/final-exam-conflict)
by SAS.

### Homework Assignments

There will be 4 to 5 homeworks. You will be informed in advance when an
assignment is due. A tentative scheduled is available on the course's
website. The homeworks consist of practice questions which are intended
to assist students in mastering the course content. They may also
potentially involve limited programming effort.

Homeworks should be completed by teams of students - three at most. No
additional credit will be given for students that complete a homework
individually. Please inform Athanasios Krontiris about the members of
your team (email: tdk.krontir/AT/gmail.com).

Students will receive 10% extra credit if they typeset their report
using LaTeX or 5\\% extra credit if they typewrite their answers (e.g.,
using Word). Submit only PDF documents. For instance, if a pair was to
receive a score of 62/100 and they typeset their report, then their
score will be 68/100, i.e,. they receive a bonus of +10\\% of 62 points.
Resources on how to use LaTeX are available below.

### Submission Rules

No late submission is allowed. If you don't submit a homework on time,
you get 0 points for that homework. The deadline will typically
correspond to the beginning of a lecture. Students can submit their
homeworks electronically via Sakai.

### Grading System

The final grade will be computed according to the following rule
\*\*(this is tentative and can change)\*\*:

final grade = max(Case A: With Homeworks, Case B: Without Homeworks)

Case A: With Homeworks

-   Homeworks: 20 points total
-   First midterm: 25 points
-   Second midterm: 25 points
-   Final exam: 30 points
-   Participation: +/- 5 points (this is up to the discretion of the
    instructor and the TAs)

Case B: Without Homeworks

-   First midterm: 30 points
-   Second midterm: 30 points
-   Final exam: 40 points
-   Participation: +/- 5 points (this is up to the discretion of the
    instructor and the TAs)

On any assignment (homework or exam), you can either attempt to answer
the question, in which case you will receive between 0 and 100% credit
for that question, or you can write "I don't know", in which case you
receive 25% credit for that question. Leaving the question blank is the
same as writing "I don't know." You can and will get less than 25%
credit for a question that you answer erroneously.

Finally, the first exam is a make-or-break situation. If your score on
the first exam is 26% or less (which amounts to a blank exam) then you
fail the class. The first exam will be early enough for you to drop the
class.

Your participation grade can be positive or negative. By default your
participation grade is 0..., e.g., if you typically come to the
lectures/recitations but you rarely answer questions during the lectures
or the recitations, your participation grade will be 0. Positive
participation grades will be given to students that actively participate
in lectures and recitations. You can also receive a negative
participation grade depending on the level of your involvement in the
course lectures and recitations (or lack there of) or because of issues
related to collusion or cheating in homeworks and exams.

The mapping of scores to letter grades will be determined at the end of
the semester. As a **rough** guide, the following rule may be used for
the final grade \*\*(it will be adapted close to the end of the
semester)\*\*:

-   A: \> 89
-   B+: 80-89
-   B: 70-79
-   C+: 60-69
-   C: 50-59
-   D: 40-49
-   F: less than 40

Students interested in a recommendation letter by the instructor will be
offered one only if they achieve a score above 95 after the completion
of the course.

### Questions about Grading

If you have a question or complaint regarding the points you received on
specific parts of a HW assignment, or an exam, staple a sheet of paper
on the graded item, stating specifically but very briefly what parts of
that document you wish to have reviewed and forward it to Athanasios
Krontiris, who will handle the process of communicating with the
instructor and the other TAs. Please refrain from verbal arguments about
grades with the instructor or with any of the TAs. We will try to get
back to you within two weeks. The deadline for submitting such requests
is the last lecture.

### Academic Standards

Exams are to be treated as individual efforts. Homeworks are not to be
treated as collective efforts beyond the participation of the team
members! Discussions are not allowed on how to solve specific questions
in homeworks. Do not discuss assignments with students that are not
currently taking the class.

A severe penalty will be given to any assignment which indicates
collusion or cheating. The usual penalty for cheating on an assignment
or an exam is failure in the course. At a minimum your participation
grade will be influenced negatively. Stealing another person's listing
or having another person "ghost write" an assignment will be considered
cheating.

Turning in work without properly citing the sources of the content
included in your work is plagiarism. All kinds of sources are included
in this definition, even those downloaded from the web, in which case an
operable link must be cited. Plagiarism from the web or other sources is
considered cheating and has the same effects. Even with a reference,
submitting an answer to a homework question, verbatim from any source
and without any contribution on your part, draws zero credit.

You should carefully study the website of Rutgers University on
[Academic Integrity](http://academicintegrity.rutgers.edu/) and the
corresponding
[policy](http://academicintegrity.rutgers.edu/policy-on-academic-integrity),
as well as the corresponding
[policy](http://www.cs.rutgers.edu/policies/academicintegrity/) from the
department of Computer Science. Your continued enrollment in this course
implies that you have read these policies, and that you subscribe to the
principles stated therein.

### LaTeX Resources

General info on what you can do with LaTeX: [Getting Started
with](http://www.maths.tcd.ie/%7Edwilkins/LaTeXPrimer/) [The Not So
Short Introduction
to](http://www.cse.unr.edu/robotics/bekris/cs482_f09/sites/cse.unr.edu.robotics.bekris.cs482_f09/files/lshort.pdf)
[Comprehensive List of
Latex](http://www.cse.unr.edu/robotics/bekris/cs482_f09/sites/cse.unr.edu.robotics.bekris.cs482_f09/files/comprehensive.pdf)
[Latex for Logicians](http://www.logicmatters.net/latex-for-logicians/)

Mac [Tex on Mac OS X](http://ii2.sourceforge.net/tex-index.html)
[MacTex](http://www.tug.org/mactex/)

The first link describes many alternatives that are available for
installing Tex on a Mac. The second link forwards to the MacTex package,
one of the alternatives mentioned in the first website. MaxTex provides
everythink that you need to use Latex on Mac except from a text editor.
It is, however, compatible with a wide variety of popular editors (e.g.,
Alpha, BBEdit, Emacs, VIM, iTeXMac, TeXShop). Note that MaxTex is a
large package.

Carbon Emacs has been succesfully tested with MacTex. After installing
MacTex, it is possible to directly compile and view \*.tex files from
Carbon Emacs's UI.

Note for Mac users: You will probably have problems previewing your PDF
output when using the postscript images provided by the instructor for
developing the notes. Nevertheless, the PDF file can be printed
properly. Prepare your document without the images and then add them.
You will probably still be able to preview the intermediate .dvi output
file with the "xdvi" program.

Linux (Ubuntu) [Latex on
Ubuntu](https://help.ubuntu.com/community/LaTeX) [Tex
Live](http://www.tug.org/texlive/)

You just have to download and install the proper packages described
above (e.g., through apt-get), use your favorite editor (e.g., emacs) to
prepare a \*.tex file and then you compile (run at least two times:
"latex filename.tex") to get the \*.dvi output. You can go from dvi to
postscript with the command "dvips" and you can convert postscript to
pdf with the command "ps2pdf".

Windows [Latex for Windows help](http://faculty.smu.edu/barr/latex/)
[MikTex (Latex for Windows)](http://miktex.org/)

If you follow the instructions on the first link you should be able to
get it working on a Windows system.

Below you can find Windows executables (32 bit) for the following
programs (follow the order when installing):

[MiKTeX](http://www.cse.unr.edu/robotics/bekris/cs482_f09/sites/cse.unr.edu.robotics.bekris.cs482_f09/files/setup-2.7.3092.exe)

[Ghostscript](http://www.cse.unr.edu/robotics/bekris/cs482_f09/sites/cse.unr.edu.robotics.bekris.cs482_f09/files/gs863w32.exe)

[Ghostview](http://www.cse.unr.edu/robotics/bekris/cs482_f09/sites/cse.unr.edu.robotics.bekris.cs482_f09/files/gsv49w32.exe)

[WinEdt](http://www.cse.unr.edu/robotics/bekris/cs482_f09/sites/cse.unr.edu.robotics.bekris.cs482_f09/files/winedt55.exe)

January 24th, 2014 - Lecture
----------------------------

### Fibonacci

-   He was an Italian mathematician in the 13th century who designed a
    famous sequence of numbers.

    $$ 0, 1, 2, 3, 5, 8, 13, ... $$

    -   We can design an algorithm to compute this.

        $$F_n = F_{n - 1} + F_{n - 2} $$

    -   And this can be expressed as a psuedocode function

            fib(n) {
                if (n == 0 | n == 1) {
                    return n;
                } else {
                    return fib(n - 1) + fib(n - 2)
                }
            }

    -   $T(n)$ grows at least as much as the value of $Fn$.

        $$ F_n \approx 2^{0.694n} $$

        -   This grows exponetially as a function of n.

-   If today, you can compute the 100th number, then after a year,
    hardware will allow you to computer the 101th number in a sequence.

-   A new function for Fibonacci:

        fib(n) {
            if (n <= 1) {
                return n;
            }

            int F[n];
            F[0] = 0;
            F[1] = 1;

            for (int i = 2; ; n++) {
                F[i] = F[i - 1] + F[1 - 2];

                return F[n];
            }
        }

-   Eventually, the cost is not exponetial, as now our function is
    linear, it's in the order of n.

-   Now, it's quite feasible to get to 200,000th number in the sequence.

### Computations

-   So far, all computations were treated as equal cost operations.
    -   This is a convinient simplication, but it is not true.
    -   For instance, addition.
        -   For numbers that can fit within your computer's register,
            say, 32-bits or 64-bits, then it takes only steps.

        -   But for big numbers like the Fibonacci numbers, like
            $0.69 / n$ bits.

-   Arithemetic operations on large numbers cannot be treated as a
    single step. You need to think about their representation.

    -   We need to think in terms of the representation of numbers.
        -   For example, a number *N* in base *b*.
        -   You need $\lceil{log_b (N+1) \rceil$ digits.

-   If cost of addition is linear to the size of bit representation,
    what is the cost of `fib(n)`?

### Running Time Simplification

-   If you have two functions that represent two running times for
    algorithms,

    $$f(n) = O(g(n))$$

    $$\exists c, n_0, f(n) \le c \times g(n) \forall n \ge n_0$$

January 29th, 2013 <small>Lecture</small>
-----------------------------------------

### Multiplication

-   Example: 13 times 11

            1101
            1011
            ----
            1101
           1101
          0000
         1101
         10001111

-   To compute each row, eitther "X" or "0", left-shifted.
    -    The rows are in the order of "2N"
    -    You have to sum them up, and you can do this pairwise.

-   If you do *n* times an operation which costs *n*, your runtime
    is going to be $n^2$.
    -   Multiplication is more expensive than addition.
    -   Multiplication is quadratic, where addition is linear (with
        respect to the size of the input).

### Alternative Multiplication

-   If you have two decimal numbers, *x* and *y*, write them next
    to each other.

        11           13
        5            26
        2   IGNORE   52
        1            104
        ----------------
                    143 (= 13 + 26 + 104)

-   Notice that the third row is ignored in both varieties of
    multiplication.

<!--    $$ x \times y =\begin{cases} 2 (x \times \lfloor \frac{y}{2} \rfloor, & \text{if $y$ is even}.\\ x + 2(x \times \lfloor \frac{y}{2} \rfloor, & \text{if $y$ is odd}. \end{cases} $$
-->

-   The expensive operation is the addition if $y$ is odd.
    So O(n) due to addition.
    -   Again, big-O is quadratic.

### Modula Arithmetic

$$ O(n) $$

### Modulo Multiplication

-   The product can be in the order of $(N - 1)^2$.
    -   The product will be at most *2N* bits long.

$$ O(n^2) $$

### Problems

Primality 

:   Given a number N, determine whether it is prime.

Factorning

:   Given a number N, express it as a product of prime
    numbers.

January 29th, 2014 <small>Recitation</small>
--------------------------------------------

### Asymptotic Bounds

-   There are three types we'll use
    1.  Tight bound
    2.  Lower bound
    3.  Upper bound, "big O"

#### Upper Bound (Big-O)

$$f(n) = O(g(n))$$

> G is upper upper bound for F if and only if there exists
> a constant and $n_0$ such that:
>
> $ 0 \le f(n) \le c g(n) $

**O(f) grows no faster than ..**

#### Lower Bound (Big Omega)

$$f(n) = \Omega(g(n))$$
$$\exists c, n_0 (0 \le c g(n) \le f(n) \forall n \ge n_o)$$

**O(f) grows faster than ...**

#### Tightly Bound (Big Theta)

**O(f) grows equal to**

### Runtimes

Name | Function
-----|---------
Logarithmic | *O(log(n))*
Constant | *O(n)*
Power | $O(n^a)$
Exponential | $O(a^n)$

January 31st, 2014 <small>Lecture</small>
-----------------------------------------

-   All cryptography is based on number theory and number
    theoretic properties.
    -   Think of message as modulo *N*.
    -   Longer message can be broken into smaller pieces.
    -   What is a good value for *N*?

### Property

-   Pick any two primes, and lets call them *p* and *q*.
    -   Then let *N* be their product, *N* = *p* \* *q*.
    -   For any *e* so that gcd(e, (p - 1)(q - 1)) = 1
    -   Then the following are true:
        1.  Take a number x and think of it as your message
            in your communication, then $x \to x^e$ is a 
            bijection.
            -   An a bijection is a one-to-one mapping.
        
        2.  Let $d = e^{-1} mod (p - 1)(q - 1)$, then,

            $$\forall x \in [0, N - 1] (x^e)^d \equiv x mod N$$

#### Example

-   Lets say our two prime numbers are p = 5, q = 11.
    -   Our N = pq = 55.
    -   Now we need to find e such that gcd(e, (5 - 1)(11 - 1)).
        -   So the GCD is 1.

    -   So lets pick e = 3 is sufficient??
        -   So what is the valye of d?

            $$d \equiv e^{-1} \bmod (p - 1)(q - 1) \equiv 3^{-1} \bmod 40 $$

    -   This means that 3 times d is equal to modulo 40, which is the
        modular inverse.
        -   For d = 27, we have 3 times 27 which equals 81 or modulo 40.

    -   For any message, x modula 55, ecryption is 

        $$ y = x^3 \bmod 55 $$

    -   For any message, decryption is

        $$ x = y^{27} \bmod 55 $$

### Proof of property

-   We have to show that

    $$(x^e)^d \bmod N \equiv x \bmod N $$

    -   The following are true if e and d have been selected
        as specific

        $$ e \times d \equiv 1 \bmod (p - 1)(q - 1) \equiv e \times d = k (p - 1)(q - 1) + 1 $$

> **Fermat's Little Theorem**: If *p* is prime, then
> $\forall 1 \le a \le p$:
> 
> $a^p \equiv a \bmod p$
> $a^{p -1} \equiv 1 \bmod p$

### Summary of RSA

#### Bob

1.  Pick two prime numbers, this is the *p* and *q*
    -   And for the security of the system, pick two
        *large* primes.

2.  You announce to the world that everyone should be
    sending your message, that is, publish (N, e) where
    N equals p times q and e relative prime to
    (p - 1)(q - 1).
3.  Internally compute the private key, which is d equal
    the inverse of e module (p - 1)(q - 1).
    -   If you mulitply the two and modulo product, the value
        should be one.

#### Alice

1.  Generate encrypted message $x^e \bmod N$ where e and N come from
    Bob public key.
2.  When Bob receives this message $x = y^d \bmod N$.

### Why is this secure?

-   To break the system, Eve must be able to compute x that has
    never left Alice given the publically available information,
    and the public key (N, e).
    -   How do you do this?
        -   Try to guess x so that $y = x^e$

-   Alternatively, she can try to factor out p and q from N,
    hence, the intractable factoring problem.

### Analysis

> What are the operations of RSA and what is the running time?

-   Modular exponentiation, plus the decoding.
-   We have to select e, a small integer, but it has to be a relative
    prime
-   Compute $d = e^{-1} \bmod (p - 1)(q - 1)$ which always exists
    when $e$ is a relative prime.
-   Pick 2 large prime numbers.

February 7th, 2013 <small>Lecture</small>
-----------------------------------------

### RSA

-   Pick 2 large *n*-bit primes.

    $$ N = pq $$

    $$ e : \gcd(e, (p - 1), (q - 1)) = 1 $$

    $$ d : d = e^{-1} \bmod (p - 1) (q - 1) $$

### Greatest Common Divisor

-   If you could perform factoring efficiently, the you could solve
    the problem.
    -   But we do not have one. So RSA is safe.

Euclid's observation

:   $\gcd(x, y) = \gcd(x \bmod  y, y)$

        function euclid(a, b) {
            if (b == 0) {
                return a;
            } else {
                return euclid(b, a \bmod b);
            }
        }

February 12th, 2014 <small>Lecture</small>
-----------------------------------------

### Review of RSA

-   Sender
    -   Picks two random primes *p* and *q*.
    -   Sets *N* equal to *pq*.
    -   `gcd(e, (p - 1)(q - 1))`

> **Fermat**: If a number *p* is prime, then for all smaller numbers,
> it is the case that $a^{p - 1} \equiv 1 \mod p$

-   How probable is it that this test succeeds? Less than half.

-   A way of generating random primes
    -   Pick a random number.
    -   Apply the primality test accounrd to Fermat.
    -   If it succeeds, then return it.

-   Good news:
    -   Prime numbers are abundant, frequently arising.
    -   A random *n*-bit number has roughly $\frac{1}{n}$ chance of 
        being prime.
    
> **Lagrange's Prime Number Theorem**: Let $\pi(x)$ be the number of primes
> $\le x$.
>
> $$ \pi(x) \approx \frac{x}{\ln(x)} $$
>
> Or more precisely,
>
> $$ \lim_{x \to \infty} \frac{\pi(x)}{\frac{x}{\ln(x)}} = 1 $$

### Hashing <small>Another Application of Number-Theoretic Algorithms</small>

-   **Objective**: Store and efficiently retrieve IP addresses of the form
    `128.32.168.80`.
    -   There are $2^{32}$ possibilities.
    
-   Let's say you have *n* of them ($n << 2^{32}$).

-   One possible way of storing them is an *array* of 2 to the 32 size that 
    indicates whether an IP address is in the set *n* IP addresses.

-   Another possibility is a *linked list*, where you only store the *n*
    IP addresses.
    -   But *O(n)* time to access them.

-   Hash tables try to provide a trade-off.
    -   Create an array in the order of *n*.

-   We need hash function that can return an index to the array and
    have the following properties:
    -   The function will scatter the elements in the array, it will
        be "random" where they're going to be placed. 
        -   If your given the same placement, you should get the same 
            value.
        -   Consistency for the same input, it should always return
            the same index in the array.

-   Picking one of the four numbers can work as a hash function under the
    assumption that that input is uniformly distributed.
-   **Objective**: Regardless of the input, we need the "random" property.
-   **Realization**: There is no single hash function that behaves well on
    all input data.
-   **Idea**: Pick from a family of hash functions randomly so that the
    probability of 2 elements to be mapped to the same index is
    $ \frac{1}{257} $ size of the array.

-   Every IP address is a tuple : $ \lbrace x_1, x_2, x_3, x_4 \rbrace $
    where $ x_1 \in [1, 256] $.
    -   Consider the has function

        $$ h_\alpha (x_1, x_2, x_3, x_4) = \sum_{i = 1}^{4} \alpha_1 \times x_i \mod N $$

        If you pick the numbers alpha-1 at random, then $h_\alpha$ is likely
        to be good.

-   **Property**: Consider any 2 elements *x*-1 through *x*-4 and 
    corresponding *y*s. If the coefficients are chosen and uniformly
    at random mod *N*, then

February 12th, 2014 <small>Recitation</small>
---------------------------------------------

### Probability Theorem

-   If you have event *A*, and you want to measure how *probable* this
    event is.
    -   We have some axioms. The axioms of probability.

> 1.  $ 1 \ge P(A) \ge 0 $
> 2.  $ P(S) = 1 $
> 3.  $ P(A \bigcup B) = P(A) + P(B)$ if *A* and *B* are mutually exclusive.

#### Event of throwing a dice

-   **Output**: {1, 2, 3, 4, 5, 6}
-   The probability of any individual role is one in six.
-   The events are independant.
-   The event can be mutually exclusive (with themselves).

#### Bayes Theorem

> **Bayes' Theorem**:
>
> $$ P(A | B) = \frac{P(B | A) \times P(A)}{P(B)} $$

February 14th, 2014 <small>Lecture</small>
------------------------------------------

### Divide and Conquer Algorithms

-   What is the characteristic here? 
    -   Break your problem into smaller instances.
    -   In the case of the number-theoretic algorithms, the
        way we were evaluating the run-time was with bits.
    -   Then, recursively solve smaller sub-problems and then
        combine these answers.

-   What was the recursively algorithm for multiplication? It
    was already an instance of *divide and conquer*.
    -   Before for multiplcation, the running time had a
        big-O of "n-squared"

#### New Multiplication

-   Now we'll get a better running time for multiplication,
    with *another idea for multiplcation.*
    -   Cnosider the following way of writing numbers:
        -   *x* is written as two numbers, with *x* "sub left"
            and *x* "sub right", where if it's 10 bits, you have
            two five bit numbers.

            $$ x = 2^{\frac{n}{2}} \times x_L + x_R $$
            $$ y = 2^{\frac{n}{2}} \times y_L + y_R $$
            $$ x \times y = (2^{\frac{n}{2}} \times x_L + x_R)(2^{\frac{n}{2}} \times y_L + y_R) $$

-   Lets think about the new operations and how much they
    cost.
    -   In the above representation, we have:
        -   Additions (linear)
        -   Multiplecation with powers of 2 (linear)
        -   Four multiplications between "n over two" bit numbers where
            we call recursively the same operation.

    -   We can define a recursive relation:

        $$ T(n) = 4 \times T(\frac{n}{2}) + O(n) $$

-   Gauss observation reowkred the above expression so as to make use of
    only 3 of the "n over two" multiplications.
-   At the $(log_2 n$)^{2n}$ level, we get down to size-1.
    -   At each level we have $3^k$ subproblems, each of them of size $\frac{n}{2^k}$
    -   At each level you have a linear cost for combining the subproblems.
    -   At depth *k*,

        $$ 3^k \times O(\frac{n}{2^k}) = (\frac{3}{2})^k \times O(n)$$

    -   Now, we've managed to decrease the run-time to something like *n* to-the
        1.59 as opposed to *n*-squared.

-   We are solving multiplication with a divide-and-conquer approach.
    -   By decreasing the number of recursive calls, we managed to get a running
        time that is *better*, i.e. the branching factor in terms of recursive calls
        matters.
    -   As a matter of fact, when you have something like ...

        $$ T(n) = \alpha \times T(\frac{n}{b}) + O(n^d) $$

### Sorting Problems

> **Master theorem**: If you have a recurisve cost-function of
> the form $T(n) = a \times T(\frac{n}{b}) + O(n^2)$ then:
>

<!-- $$ T(n) =   \begin{cases} O(n^d) & \text{if } d \lt log_b a \\ O(n^d \log(n)) & \text{if } d = \log_b a \\ O(n^{log_b a} & \text{if } d \lt log_b a \end{cases} $$
-->

-   Assume that *n* is a power of *b* for convinience.
    -   The size of the problem decreases by *b* at every level.

-   We need $log_b n$ level to stop the recursion.
    -   At level *k* we have $a^k$ subproblems of size $\frac{n}{b^k}$
        -   Work at level *k*:

            $$ a^k \times O((\frac{n}{b^k})^d) = O(n^d) \times (\frac{a}{b^d})^k $$

#### Three cases

1.  If $\frac{a}{b^d} \lt 1$, series is decreasing.
    -   The "first term" dominates.
    -   Running time:

        $$ O(n^d) $$

2.  If $\frac{a}{b^d} \gt 1$, series is increasing
    -   The "last term dominates"
    -   Running time:

        $$ O(n^{\log_b a}) $$

3.  If $\frac{a}{b^d} = 1$, all terms are equivilent.

    $$ O(n^d) = O(n^{\log_b a}) $$ 

February 16th, 2014 <small>Reading</small>
------------------------------------------

### Chapter 1 <small>Algorithms with numbers</small>

Factoring

:   Given a number *N*, express it as a product of its prime factors.

Primality

:   Given a number *N*, determine whether it is a prime.

-   Factoring is hard.
    -   Despite lots of effot, the fastest method is exponetial to the number of
        bits.

-   We *can* efficiently test whether something *is* prime!

#### Basic arithmetic

##### Addition

> **Basic property of decimal numbers**: The sum of any three single-digit numbers
> is *at most* two digits long.

-   This simple rule gives us a way to add two numbers in any base:
    -   Align their right-hand ends, and then perform single right-to-left pass in
        which the sum in which the sum is computed digit-by-digit, maintaining the
        overflow as a carry.
        -   Since we know each individual sum is a two-digit number, *the carry is
            always a single digit*, and so at any given step, three single digit
            numbers are added.

                Carry: 1        1  1  1     
                          1  1  0  1  0  1  (53)
                          1  0  0  0  1  1  (35)
                       -------------------
                       1  0  1  1  0  0  0  (88)

-   *Given two binary numbers, how long does our algorithm take to add them?*
    -   We want the answer expressed as a function of *the size of input*.
        -   The number of bits.

    -   Suppose that *x* and *y* are *n* bits longs.
        -   The the sum of *x* and *y* is *n + 1* bits *at most*.
        -   Each bit of the sum is computed in a fixed amount of time.
        -   The total running time for addition:
            -   Of the form $c_0 + c_1 n$ where "c-zero" and "c-one" are some
                constant.
            -   In other words, it is *linear*.
            -   The running time is *O(n)*.

-   *Is there a faster algorithm?*
    -   In order to add two *n*-bit numbers, we must at least read them and
        write down the answer, and even that requires *n* operations.
    -   The algorithm is optimal, up to multiplicative constants!

-   *Why O(n) operations? Isn't binary addition done in one instruction?*
    1.  Only addition operations that are within a computers word-length, often
        32 or 64.
        -   It is often useful and necessary to handle number much larger than
            this, several thousand bits long.
        -   Operations on these big numbers is often like operating bit-by-bit.

    2.  When we want to understand algorithms, it makes sense to study the basic
        algorithms that encoded to the hardware.
        -   Focus on *bit complexity*.

##### Multiplication and division

-   The grade-school algorithm for multiplying to numbers is to create an array
    of intermiediate sums, each representing the product of the first number by a
    single digit of the second.
    -   These values are left-shifted and right-shifted and added.

-   Thirteen times eleven in binary:

                    1  1  0  1  (binary 13)
                 x  1  0  1  1  (binary 11)
        ----------------------
                    1  1  0  1  (1101 times 1, shifted no)
                 1  1  0  1     (1101 times 1, shifted once)
              0  0  0  0        (1101 times 0, shifted twice)
        +  1  1  0  1           (1101 times 1, shifted thrice)
        ----------------------
        1  0  0  0  1  1  1  1  (binary 143)

-   Psuedo code:

        function multiply(x, y) {
            if (y == 0) {
                return 0
            }

            z = multiply(x, floor(y / 2));

            if (y is even) {
                return 2z;
            } else {
                return x + 2z;
            }
        }

-   *How long does this take?*
    -   If *x* and *y* are both *n*-bits, then there are *n* intermediate rows,
        with lengths of up to *2n* bits (taking the shiting into account).
    -   The total time to add up these rows, doing two numbers at a time:

        $$ O(n) + O(n) + ... + O(n) $$

        *(n - 1)* times.

        -   This is $O(n^2)$, or *quadratic* in the size of the inputs.
        -   Still polynomial but much slower than addition.

-   *Can this be improved?*
    -   Al Khwarizmi knew another way to multiple.
    -   To multiply two decimal numbers, write them next to each other.
        -   Then, repeat: Divide the first number by 2, rounding down the result,
            and double the second number. Keep going until the first number gets
            down to 1.
        -   Then, strike out all the rows in which the first number is even, and add
            up whatever remains in the second column.

                11  13
                 5  26
                 2  52  (strike out)
                 1 104
                ------
                   143  (answer)

-   Pseudocode!

        function divide(x, y) {
            if (x == 0) {
                return (q, r) = (0, 0);
            }

            (q, r) = divide(floor(x / 2), y);
            q = 2 * q;
            r = 2 * r;

            if (x is odd) {
                r = r + 1;
            } 

            if (r >= y) {
                r = r - y;
                q = q + 1;
            }

            return (q, r)
        }

-   *Is this algorithm correct?*
    -   Verify that it mimics the description of the rules.

-   *How long does this algorithm take?*
    -   It must terminate after *n* recursive calls, because at each call
        *y* is halved.
        -   That is, the number of bits is decreased by one.

    -   Each recursive call requires these operations:
        -   A division by 2 (right shift)
        -   A test for odd/even (looking up the last bit)
        -   A multiplication by 2 (left shift)
        -   Possible on addition, O(n).

    -   The total time is $O(n^2)$ therefore.

-   *Can we do better?*
    -   Intuitively, you think that you need to, at most, do *n* operations
        *n* times to add.
    -   But no! Chapter 2 will show you can do better.

#### Modular arithmetic

-   With repeated addition or multiplication, numbers get very big.
    -   We "reset to zero" whenever time reaches 24.
    -   Similarly, the built-in arithmetic operations of computer processors,
        numbers are restricted to a size, say 32 or 64, which is generous for
        most purposes.

-   For primality testing and cryptography, it is necessary to deal
    with numbers that are significantly bigger.
-   *Modular arithmetic* is a system for dealing with restricted ranges of integers.
    
*x* *modulo* *N*

:   The remainder when *x* is divided by *N*.

    If *x = qN + r* with *0 <= r < N*, then *x* modulo *N* is equal to *r*.

-   One way to think of modular arithmetic deals with all the integers,
    but divides them in *N* *equivilence classes*, each of the form
    $ \lbrace i + kN : k \in \mathbb{Z} \rbrace $ for some *i* between ) and
    *N - 1*.
    -   For example, there are three equivilence classes of modulo 3:

            ...  -9  -6  -3  0  3  6  9  ...
            ...  -8  -5  -2  1  4  7  10 ...
            ...  -7  -4  -1  2  5  8  11 ...

        Any member of the class is substituable for any other.

> **Substitution rule**: If $ x \equiv x' ( \bmod N)$ and $y \equiv y' (\bmod N)$, then:
>
> $$ x + y \equiv x' + y' (\bmod N) $$
> 
> $$ xy \equiv x' y' (\bmod N) $$

-   It is not hard to check that in modular arithmetic, the usual associate, commutative,
    and distributive properties of addition and multiplication continue to apply.
    -   For instance:
        -   Associativity
        -   Commutativity
        -   Distributivity

    -   You can simplify big numbers with this. Witness:

        $$ 2^{345} \equiv (2^5)^{69} \equiv 32^{69} \equiv 1^69 \equiv 1 (\bmod 31) $$

##### Modular addition and multiplication

-   To *add* two numbers "*x* and *y* modulo *N*", we start with regular addition.
    -   Since *x* and *y* are both in the range of 0 to *N - 1*, their sum is between
        *0* and *2(N - 1)*.
    -   If the sum exceeds *N - 1*, we merely need to subtract of *N* to bring it back
        to the required range.
    -   The overal computation therefore consists of an addition, and possibly a
        substraction, of numbers that never exceed *2N*.
    -   Its running time is linear in the sizes of these numbers.
        -   In other words, *O(n)*, where *n = ceil(log N)*, is the size of *N*.
    
-   To *multiply* two mod-*N* numbers *x* and *y*, we again just start with regular
    multiplication and then reduce the answer modilo *N*.
    -   The produce can be as large as $(N - 1)^2$.
        -   But this is still at most *2n* bits long.

    -   To recude the answer modulo *N*, we compute the remainder upon dividing it by
        *N*, using our quadratic-time division algorith,
    -   Multiplication remains a quadratic operation.

-   *Division* is not so easy.
    -   Will be do later.

-   To complete the suit of modular arithmetic primitives we need for cryptography,
    we next turn to *modular exponentiation*, and then to *greatest common divisor*,
    which is the key to division.

##### Modular exponentiation

-   *What is the algorithm?*

        function modular-exponentiation(x, y, N) {
            if (y == 0) {
                return 1;
            }

            z = modulor-exponentiation(x, floor(y / 2), N);

            if (y is even) {
                return (z ** 2) % N;
            } 
            
            else {
                return (x * (z ** 2)) % N;
            }
        }

-   In the cryptosystem we are working towards, it is necessary to compute
    "*x* to the *y* mod *N*" for the values of *x*, *y*, and *N* that are
    several hundred bits long. *How can this be done quickly?*
-   The result is some number modulo *N* and is therefore itself a few hundred
    bits long.
    -   However, the raw value of "*x* to the *y*" could be much, much longer
        than this.
        -   Even when *x* and *y* are just 20-bit numbers, "*x* to the *y*" is
            *at least* $(2^{19})^{2^{19}} = 2^{(19)(524288)}$, about 10 million
            bits long!

-   To make sure the numbers we are dealing with never grow too large, we need
    to perform all intermediate computations modulo *N*.
    -   Here's the idea:
        -   Calculate $x^y \bmod N$ by repeatedly multiplying by *x* modulo *N*.
            The resulting sequence of intermediate products,

            $$ x \bmod N \to x^2 \bmod N \to x^3 \bmod N \to ... \to x^y \bmod N $$

            consists of number that are smaller than *N*, and so the individual
            multiplications do not take too long.
        -   But there's a problem! If *y* is 500 bits long, we need to perform
            "2 to the 500" multiplication! The algorithm is clearly exponetial
            in the size of *y*.

-   Luckily, we can do better.
    -   Starting with *x* and *squaring repeatedly* modulo *N*, we get:

        $$ x \bmod N \to x^2 \bmod N \to \cdots \to x^{2^{\log y}} \bmod N $$

    -   Each takes $O(log^2 N)$ to compute, with only *log y* multiplications.
        -   To determine this, multupli together these powers.

            $$ x^{25} = x^{11001_2} = x^{10000_2} \times x^{1000_2} \times x^{1_2} = x^{16} \times x^8 \times x^1 $$

        -   A polynomial time algorithm

-   We can package this idea in a simply recusrive algorithm described at this begninng
    of this section.
    -   Let *n* be the size of bits *x*, *y*, and *N* (whichever of the three is largest)
        -   Like multiplication, the algorithm will halt after *at most* *n* recursive
            calls.
        -   During each call it multiplies *n*-bit numbers
        -   Doing computation modulo *N* saves us here.

    -   Running time of $O(n^3)$

##### Euclids algorithms for greatest common divisor

-   Given to integerns *a* and *b*, find the largest integer that divides both of
    them, known as their *greatest common divisor* (gcd).
-   The most obvious approach is to first factor *a* and *b*, and the multiply
    together their common factors.
    -   For instance, $1035 = 3^2 \cdot 5 \cdot 23$ and $759 = 3 \cdot 11 \cdot 23$,
        so their GCD is $ 3 \cdot 23 = 69 $. 
    -   However, we have no efficient algorithm for factoring.
        -   *Is there some other way?*

-   Euclid's algorithm uses the following simple formula.

    > **Euclid's rule**: If *x* and *y* are positive integers with $x \ge y$, then
    > $\gcd(x, y) = \gcd(x \bmod y, y)$.

-   Euclid's rule allows us to write down an elegant recursive algorithm:

        function Euclid(a, b) {
            if (b == 0) {
                return a;
            }

            return Euclid(b, a % b);

        }

    -   This means that after any two consective rounds, both arguments *a* and *b*
        are *at very least* halved in value - the length of each decreases by at least
        on bit.
        -   If they are initially *n*-bit integers, then the base case will be reached
            within *2N* recursive calls.
        -   And since each call involves a quadratic-time division, the total time
            is $O(n^3)$.

##### An extension of Euclid's algorithm

-   A small extensions is the key to dividing in the modular world.
-   Suppose someone claims that *d* is the GCD of *a* and *b*:
    -   How can we check this?

    > **Lemma**: If *d* divides both *a* and *b*, and *d = ax + by* for some integers
    > *x* and *y*, then necessarily *d = gcd(a, b)*.

-   So, if we can supply two numbers *x* and *y* such that *d = ax + by*, then we can
    be sure that *d = gcd(a, b)*.
    -   What is even better is that those *x* and *y*s can be found by a small extension
        of Euclid's algorithm.

    > **Lemma**: For any positive integers *a* and *b*, the extended Euclid algorithm
    > returns integers *x*, *y*, and *d* such that *gcd(a, b) = d = ax + by*.

##### Modular division

-   In real arithmetic, every number that doesn't equal zero has an inverse,
    that is, one over itself.
    -   Dividing by a number is the same as multiplying by its inverse.
        -   In *modular* arithmeric, we can make a similar definition.

Multiplicative inverse

:   We say *x* is the *multiplicative inverse* of *a* modulo *N* if 
    $ax \equiv 1 (mod N)$.

-   There can only be one, and we denote it with $a^{-1}$.
    -   However, it doesn't *always* exist.
    -   For instance, 2 is not invertible modulo 6.
        -   2 multiplied by *x* is not equivilient to 1 modulo 6 for any and every
            number.
        -   In this case, *a* and *N* are both even and thus *a mod N* is alwaus even,
            since *a mod N = a - kN* for some *k*.

-   In fact, this is the only circumstance in which *a* is not invertible.
    -   The *gcd(a, N) = 1* (this is called *relatively prime*), the extended Euclid
        algorithm gives us integers *a* and *y* such that *ax + Ny = 1*, which means
        that $ax \equiv 1 (mod N)$.
        -   This, *x* is *a*'s sought inverse.


Example

:   -   Continuing with our previous example, supose we computer $1^{-1} \bmod 25$.
        -   Using the extended Euclid algorithm we find that

            $$ 15 \cdot 25 - 34 \cdot 11 = 1 $$

        -   Reducing both sides modulo 25, wh have

            $$ -34 \cdot 11 \equiv 1 \bmod 25 $$

        -   Therefore, $-34 \equiv 16 \bmod 25$ is the inverse of $ 11 \bmod 25$.

Modular division theorem

:   For any $a \bmod N$, *a* has the a multiplicative inverse modulo *N* 
    iff it is relatively prime to *N*. When this inverse exists, it can be found
    in time $O(n^3)$ by running the extended Euclid algorith,

-   This resolve the issue of modular division.
    -   When working with modulo *N*, we can divide by numbers realtively prime to *N*.
        -   And *only by* these.

    -   To carry out the division, we multiply the inverse.

#### Primality testing

Fermat's little theorem

:   If $ p $ is prime, then for every $ 1 \le a \lt p $

    $$ a^{p - 1} \equiv 1 (\bmod p) $$

:   ~~~
    function primality(N) {
        a = random(less than N); 

        if ((a ** (N - 1)) == (1 % N)) {
            return YES;
        }

        else {
            return NO;
        }
    }
    ~~~

-   The problem is that Fermat's theorem is not an iff condition.
    -   It doesn't say what happens when *N* is *not* prime.
    -   In fact, it *is* possible for a composite number *N* to pass Fermat's
        test.

-   In analyzing the bahvior of this algorithm, we first need to get a minor bad
    case out the way.
    -   There are extremely rare composite numbers called *Carmichael numbers*,
        and they pass Fermat's test for all *a* relatively prime to *N*.
        -   On such numbers our algorithm will fail.

-   In a Carmichael-free universe, our algirothms work well.

Lemma 

:   If $a^{N - 1} \not\equiv 1 \bmod N$ for some *a* relatively prime to *N*, then it
    must hold for at least half the choices of $a \lt N$.

-   We are ignoring Charmichael numbers, so we now assert,
    -   If *N* is prime, then $a^{N - 1} \equiv 1 \bmod N $ for all *a* less than *N*.
    -   If *N* is not prime, then $ a^{N - 1} \equiv 1 \bmod N $ for at most half of
        the values of $a \lt N$.

-   The probability of our primality algorithm returning yes when a number is prime
    is 1, that is it happens 100% percent of the time.
    -   On the other hand, the probability of reutrning yes with a number is *not
        prime* is one half, that is, false positives happen half of the time.
    -   If you run the test *k* times, the probability of *N* not being prime is
        $\le \frac{1}{2^k}$.

~~~
function primarilty2(N) {
    pick positive integers a1, a2, ..., ak < N at random;

    if ((a[i] ** N - 1) == 1 (mod N)) for all i ... k {
        return yes;
    else
        return no;
    }
~~~

-   This probability of error drops exponentially fast, and can be driven *arbitrarily
    low* by choosing a large enough *k*. 
    -   If you do it a 100 times, the probability of a cosmic ray ruining your 
        computation is higher than the probability of error.

##### Generating random primes

-   We are now close to having everything we need for cryptography.
    -   We need a fast algorithm for choosing random primes.
        -   Hundred bits long.

    -   What makes this aks quite easy is that prime are abundant
        -   A random, *n*-bit number has a roughly one-on-*n* chance of being
            prime.
        -   For instance, about 1 in 20 social security numbers are prime!

Lagrange's prime number theorem

:   Let $\pi(x)$ be the number of primes $\le x$. Then, $\pi(x) \approx \frac{x}{\ln n}$,
    or more precisely,

    $$ \lim_{x \to \infty} \frac{\pi(x)}{(x / \ln x)} = 1 $$

    Such abundance makes it simple to generate a random *n*-bit prime:

    -   Pick a random *n*-bit number *N*.
    -   Run a primality test on *N*.
    -   If it passes the test, output *N*, else repeat the test.

-   *How fast is this algoritm?*
    -   If the randomly chosen *N* is truly prime, which happen with probability at
        least $\frac{1}{n}$, then it will certainly pass the test.
    -   So on each iteration, this procedure has at least a $\frac{1}{n}$ chance of
        halting.
    -   Therefore, on average it will halt within $ O(n) $ rounds.

-   Next, exactly which primality test should be used?
    -   In this application, since the number we are testing for primality are chosen
        at random rather than by adversary, it is sufficient to perform the Fermat test
        with *a* as 2.
        -   For random numbers the Fermat test has a mihc samller failur probability
            than the worst-case one-half bound proven earlier.
        -   The resulting algorithm is quite fast, generating primes that are hundreds
            of bits long in a fraction of a second on a PC.

-   The important question: *What is the probability that the output of the algorithm
    is really prime?*
    -   To answer, we must first understnad how discerning the Fermat test is.
    -   As a concrete example, perform the operation on base *a* equal to 2 for
        all numbers less than or equal to 25 times 10 to the 9th power.
    -   In this range, there are about $10^9$ primes, and about 20,000 composites
        that pass the test.
        -   Thus, the chance of erronesouly outputting a composite numbers is
            
            $$ 20,000 / 10^9 = 2 \times 10^{-5} $$

#### Cryptography

-   The next topic is the RSA cryptosystem.
    -   It derives very strong guarantees of security by ingeniously exploiting the
        wide gulf between the polynomial-time computability of certain number-theoretic
        tasks and the intractability of others.

-   The typical setting for cryptography is described with a cast of three characters:
    Alice and Bob, who want to communicate in private, and Eve, the eavesdropper who
    will go to great length to find out what they're saying.
    -   Imagine Alice sends her message "*x*" which is written in binary.
        -   She encodes it as *e(x)*, sends it over, and then Bob applies his
            decryption function *d()* to decode it: *d(e(x)) = x*.

~~~
Alice                                                Bob
            +----------+  e(x)   +----------+
  x  ---->  | Encoder  |  ---->  | Decoder  |  ----> x = d(e(x))  
            +----------+    |    +----------+
                            |
                            +--->  Eve
~~~

-   Alice and Bob are worried that the eavesdropper, Eve, will intercept *e(x)*.
    -   She might be a sniffer on the network. 
    -   The function *e()* is chosen so that without knowing *d()*, Even cannot
        do anything with the information she has picked up.
        -   *e(x)* tells you little or nothing about *x*.

-   For centuries, cryptography was based on *private-key protocols*.
    -   In such a scheme, Alice and Bob would have to actually meet before hand
        and agree on the scheme.
        -   Eve's only hope is to get the codebook and a message.

-   *Public-key protocols* such as RSA are significantly more subtle and tricky.
    -   They allow Alice to send a message to Bob without ever having to meet him.
    -   The central idea behind RSA is the dramatic constrast between facting and
        primality.
        -   Bob is able to implement a *digital lock*, to which only he has the key.

    -   By making his digital lock public, he gives Alice a way to send him a secure
        message that only he can decrypt.
        -   This is how the Internet sends private and sensitive information.

-   In the RSA protocol, Bob need only perform the simplest of calculations, such as
    multiplcation, for a digital log.
    -   By contrast, Eve must perform operations like factoring large numbers that
        would require more than the world's most powerful computers combined.

##### RSA

-   RSA is *public-key cryptography*.
    -   Anybody can send a message to anybody else using publically available
        information.
    -   Each person has a public key known to the whole world and a secret key known
        only to themselves.
    -   When Alice wants to send a message to Bob, this happens:
        1.  She encodes it using his public key.
        2.  He decrypts it with his secret key.

-   The RSA scheme is based heavily on number theory
    -   Think of messages from Alice to Bob as numbers modulo *N*.
        -   Messages larger than *N* are broken into smaller peices.

    -   The encryption function will the be a bijection on $ \lbrace 0, 1, \cdots N - 1\rbrace $
        -   The decryption function will be its inverse.

Property

:   Pick any two primes *p* and *q* and let *N = pq*. For any *e* relatively prime to
    *(p - 1)(q - 1)*:

    1.  The mapping $x \mapsto x^e \bmod N$ is a bijection on 
    
        $$ \lbrace 0, 1, \cdots , N - 1 \rbrace $$
    
    2.  Moreover, the inverse mapping is easily realized: led *d* be the inverse of
        *e* modulo *(p - 1)(q - 1)*. Then for $x \in \lbrace 0, 1, \cdots N - 1 \rbrace$,

        $$ (x^e)^d \equiv x \bmod N $$

> **Example**
>
> -   **Bob chooses his public and secret keys**
>     -   He starts by picking two large (*n*-bit) random primes *p* and *q*.
>     -   His public key is $(N, e)$ where $N = pq$ and $e$ is a $2n$-bit number
>         relatively prime to $(p - 1)(q - 1)$.
>         -   A common choise is $ e = 3 $ because it permits fast encoding.
>  
>     -   His secret key is $d$, the inverse of $e$ modulo $(p - 1)(q - 1)$, computed
>         using the extended Euclid algorithm.
>
> -   **Alice wishes to send message $x$ to Bob**.
>     -   She looks up his public key $(N, e)$ and sends him $y = (x^e \bmod N)$,
>         computed using an efficient modular exponentiation algorith,
>     -   He decodes the message by computing $y^d \bmod N$.

-   This RSA protocol is convinient.
    -   The computations for Alice and Bob are easy.
    -   But what about Eve?
        -   The security of RSA hinges upon a simple assumption:

            > Given $N$, $e$, and $y = x^e \bmod N$, it is computationally intractable
            > to determine $x$.

-   This assumption is quite plausible
    -   She coould try all possible values of $x$, each time checking
        $x^e \equiv y \bmod N$
        -   This would take exponetial time.

    -   She could try to factor $N$ to retrieve $p$ and $q$, and then figure our
        $d$ by inverting $e$ modulo $(p - 1)(q - 1)$.
        -   This factoring would be hard.

    -   Intractibility is normally a source of dismay, RSA uses it as an advantage.

*[GCD]: Greatest common divisor

*[iff]: if and only if

*[RSA]: Rivest-Shamir-Adelman
