Principle of Programming Languages <small>with Professor Louis Steinberg</small>
================================================================================

Description
-----------

The course is aimed at making the student familiar with the general
concepts common to all programming languages so as to facilitate
learning new languages. Language paradigms (i.e., logic, functional,
procedural, object-oriented) are compared and implementation strategies
are discussed.

-   Credits: 4
-   Prerequisites:
    -   14:332:331 or 01:198:211;
    -   01:198:205 or 14:332:312.

-   Please note that courses for which a student has received a grade of
        D cannot be used to satisfy prerequisite requirements.

-   Semesters Offered: Spring and fall

### Topics

-   BNF and context free grammars; Data visibility (i.e., lexical and
        dynamic scoping);

-   Procedures and parameter passing techniques;
-   Types, type checking and type equivalence;
-   Functional programming paradigm:
    -   higher-order functions,
    -   recursive data structures,
    -   programming with recursion (i.e., without iteration);

-   Logic programming paradigm:
    -   unification, generate and test;
    -   Programming with pointers in C.

### Expected Work

There are three graded programming projects and textbook homework
assignments.

-   Exams:
    -   1 hourly, Final Exam

### Department Learning Goals

-   Computer Science majors ...
    -   will be prepared to contribute to a rapidly changing field by
            acquiring a thorough grounding in the core principles and
            foundations of computer science (e.g., techniques of program
            design, creation, and testing; key aspects of computer hardware;
            algorithmic principles).

    -   will acquire a deeper understanding on (elective) topics of more
            specialized interest, and be able to critically review, assess,
            and communicate current developments in the field.

    -   will be prepared for the next step in their careers, for
            example, by having done a research project (for those headed to
            graduate school), a programming project (for those going into
            the software industry), or some sort of business plan (for those
            going into startups).

Syllabus
--------

### Objective

-   Primary objective: Learn new ways of thinking about problems and
        programs.

-   Secondary objective: Make it easier to learn new languages by
        learning principles that apply to many languages.

-   Tertiary objective: Learn some interesting languages.

### Prerequisite

-   CS 205, CS 211
-   Java; the memory model of C, including pointers; predicate calculus

### Book

-   Michael L. Scott, Programming Language Pragmatics, 3rd Edition.
        Morgan Kaufman

\*\*The textbook does not cover all of the material for this course, and
is not a substitute for attending class.\*\*

### Work

-   You are expected to attend all lectures and recitations, in both
        body and mind. That is, please do not access Facebook, games, email,
        or the like during class.

-   There will be two midterms exams and a final, as well as graded
        programing projects and ungraded exercises. The projects only count
        for a small part of your grade directly, because there is no way to
        be sure that they are really your own work. However, they count for
        a large part of your grade indirectly. If you do not do the
        exercises and projects you will not learn the material. Furthermore,
        there will be exam questions directly based on the projects and
        exercises.

### Tentative Grading

Your course grade is based on projects and exams, with the following
tentative weighting:

-   Projects (all together): 10%
-   Midterm 1: 25%
-   Midterm 2: 25%
-   Final exam: 40%

### Course grades

Your course grade will be computed as follows: Each score (for each exam
and each project) will be converted to a percentage score, and the
percentages will be added, with weights as above. Cutoffs for letter
grades are:

-   A: 90%
-   B+: 85%
-   B: 80%
-   C+: 75%
-   C: 70%
-   D: 60%

### Grading disputes

If you feel an exam or a project has been misgraded, you must bring it
to our attention within 2 weeks of when we first give back the graded
exam or project.

### Collaboration

All students in this class are expected to be familiar with the The DCS
academic integrity policy, which can be found at
http://www.cs.rutgers.edu/policies/academicintegrity/ , and to abide by
it.

We do encourage you to us the Piazza site to discuss the concepts behind
course material and assignments, but please do not post code. If you
need help with code, email it to the professor or a TA.

### Exams

Exam schedules and rules are in Resources \> Exam info. You are expected
to know and to abide by these rules.

### Poor grades

If you get less than 70% on an exam please contact the 314 TA's or
instructor immediately. Often students wait until after the final, and
then ask how they can raise their grade. At that point there is no way
to raise their grade. The earlier you contact us the more chance we can
be of help.

### Topics

The following list is organized by topic, not by chronological order of
coverage in the course.

1.  Formal Languages
    -   Context free grammars
    -   Regular grammars
    -   Finite state automata
    -   Regular expressions
    -   Using all of the above to define a language
    -   Functional Programming

2.  Scheme
    -   Repetition through recursion, not iteration
    -   Stateless programming
    -   Closures
    -   Continuations and coroutines.
    -   Logic Programming

3.  Prolog
    -   Scripting

4.  Python
    -   Principles
    -   Types and type inference
    -   Scope & binding,lexical and dynamic
    -   Parameter passing modes

September 16th, 2013 <small>Assignment 1</small>
------------------------------------------------

1.  Given grammar `G`: (capitals are non-terminals, everything else is a
        terminal)

        S -> A | S # S | S @ S      
        A -> C | C A        
        C -> a | b | c

    -   For each of the strings below:
        1.  if it is in `L(G)` prove it by giving both - a leftmost
                derivation

        2.  a parse tree. If it is ambiguous demonstrate that fact with
                parse trees.

        3.  if it is not in `L(G)` say so and explain why

    -   Strings:
        1.  `aa # bb`
            1.  `S`
            2.  `S # S`
            3.  `A # A`
            4.  `C # C`
            5.  `a # a`

        2.  `a @ b # c`
            1.  `S`
            2.  `S # S`
            3.  `S # S @ S`
            4.  `A # A @ A`
            5.  `C # C @ C`
            6.  `a @ b # c`

        3.  `ab`
            1.  `SS`
            2.  `AA`
            3.  `CC`
            4.  `ab`

2.  Rewrite the grammar `G` above so that no string in its language is
        ambiguous. Make \# have higher precedence than `@` and make both `#`
        and `@` be left-associative.

        S -> A | @ S       
        A -> C | # A        
        C -> a | b | c

3.  Given grammar G':

        S -> A B
        A -> x | A a
        B -> y | b B

    1.  Give a string that is in `L(G')` and one that is not
        1.  `xy`
        2.  `x`

    2.  Describe in English what strings are in `L(G')`.

        `L(G')` contains a series of `x`s followed by a series of `y`s,
        each with at least one `x` or `y` followed by potentially
        infinite `x`s or `y`s.

4.  Let `L1` be a formal language using the binary digits `0` and `1` as
        its character set, such that a string is in `L1` if and only if it
        has `3` or more `1`'s in a row somewhere in it.

    1.  Draw a deterministic finite state automaton that recognizes
            `L1`.

                +---+    +---+    +---+    +---+
              ->| 1 |--->| 1 |--->| 1 |--->| 0 |
                +---+    +---+    +---+    +---+
                |                  |       |
                ---------------------------+

    2.  Write a regular expression whose language is `L1`.

            /([01]*[111]+[01]*)/

5.  Let `L3` be a formal language using the letters `o`, `a`, and `y`,
        such that a string is in `L3` if and only if it has the string
        `yoya` somewhere within it.

    1.  Draw a nondeterministic FSA that recognizes `L3`.

                  ______________________         _
                  |         |          |        | |
                +---+ o  +----+ y  +-----+ a  +------+
              ->| y |--->| yo |--->| yoy |--->| yoya |
                +---+    +----+    +-----+    +------+

    2.  Write a regular expression whose language is `L3`.

        (y|o|a)*(yoya)+(y|o|a)*

6.  Describe in English the language accepted by this DFSA: `S1` is the
        start state and only `S2` is an accepting state.

    A series of zeroes and ones with at least a single one and possibly
    no zeroes.

7.  Describe in English the language of each of the following RE's:
    1.  `ab*c*`
        -   This is a series `b`s preceded by an `a`, followed by any
                number of `c`s.

    2.  `a*|b*`

    -   Any number of `a`s followed by any number of `b`s.

    1.  `(ab)*`

    -   A possibly empty series of repeating `ab`.

September 23rd, 2013 <small>Assignment 2</small>
------------------------------------------------

1.  View the video: https://www.youtube.com/watch?v=prAwkQt3ARg
2.  Answer these questions:
    1.  What is the main point the speaker is trying to make
    2.  List two examples the speaker uses and explain for each how it
            supports his point, or, if you think that it does not, why not.

October 3rd, 2013 <small>Exercise 4: Scheme</small>
---------------------------------------------------

For these problems, you must use pure functional scheme. That is: You
may not use a functions like set! whose name ends with '!'. You may not
use for or while loops or do loops. All repetition must be via explicit
recursion or the recursion implicit in map or similar functions. (You
can do problems 1 – 3 before we cover map in class.) You may, however,
use define – in fact you must use it. You may use any implementation of
scheme that complies with the R5RS standard.

1.  Write the function echo. This function doubles each top-level
        element of it argument. E.g., (echo '(a b c)) returns (a a b b c c).
        (echo '(a (b c))) returns (a a (b c) (b c))

2.  Write the function nth. (nth i lst) returns the ith element of lst.
        E.g., (nth 0 '(a b c)) returns a, (nth 1 '(a b c)) returns b. You
        may assume that 0 ≤ i \< (length lst).

3.  Write the function deep-reverse, which reverses its argument at all
        levels. E.g., (deep-reverse '(a (b c) (d))) returns ((d) (c b) a).

4.  Write a scheme function (assoc-all lst a-list) where lst is a list
        of symbols and a-list is an assoc-list. assoc-all returns a list of
        the data associated with elements of lst by assoc-list. E.g.
        (assoc-all '(a d c d) '((a apple)(b boy)(c cat)(d dog))) returns
        (apple dog cat dog). Use map. Note that you can't simply use assoc
        as one of the arguments to map. You need a lambda.

5.  Write a function filter-evens which takes a list of numbers as its
        argument and returns a new list containing only the even numbers in
        the input list. E.g., (filter-evens '(23 33 44 2 1 8)) returns (44 2
        8). Use even? to test if a number is even. You must use map. You may
        use a helper function but the only recursion should be the recursion
        implicit in map. Hint: Note that the result of map is exactly as
        long as its second argument. E.g. the result of (map foo '(23 33 44
        2 1 8)) will be a list of 6 elements no matter what function foo is.
        So how can this problem be solvable? Do something to the result of
        map before you return it. E.g., suppose the result of (map foo '(23
        33 44 2 1 8)) is ( ( ) ( ) (44)(2)( ) (8)). Then (apply append (map
        foo '(23 33 44 2 1 8))) will result in (44 2 8) .

October 15th, 2013 <small>Midterm 1 Study Guide</small>
-------------------------------------------------------

### Formal Languages

#### Grammars

-   **Parsing** works from the terminal string to the start

        terminal string => ... => <start>

    -   A **parse-tree** has internal nodes as nonterminals, where the
            children make up the right-hard side of one of the productions
            for that nonterminal.

-   **Derivation** works from the start and *to* the terminal string

        <start> => ... => terminal string

-   ambiguity and removing ambiguity:
    -   To add **precedence** to a parse tree, make the edge "higher in
            the tree" where higher means lower precedence.

    -   **Associativity** can distinguish `a ~ b ~ c` in two ways: 1.
            `(a ~ b) ~ c` or 2. `a ~ (b ~ c)`.

-   **Regular grammars** are used to specify the structure of tokens.
-   **Context-free grammars** are used to specify the overall structure
        of a programming language.

#### Regular Expressions

-   The letter itself represents just itself.
-   The empty string represents just itself.
-   The "or" operator will union the sets of two definitions.
-   Placing to expressions next to one another will place both sets
        right next to each other, "Cartesian product."

-   Two letters next to one another contain only those two letters.

        a             {a}
        e             {e}
        R|S           L_r U L_s
        a|b           {a, b}
        RS            L_r L_s
        ab            {ab}

-   `*` will make the represented set the empty string and any number of
        the contained expression.

-   `+` will make any number of the contained expression excluding the
        empty string.

        a             {a}
        b             {b}
        ab            {ab}
        a|b           {a, b}
        ab|ac         {ab, ac}
        (a|b)(b|c)    {ac, ad, bc, bd}
        (abc|e)d      {abcd, ed}

        a*            {e, a, aa, aaa, ...}
        ab*           {a, ab, abb, abbb, ...}
        (ab)*         {e, ab, abab, ababab, ...}
        (a|b)*        {e, a, b, aa, ab, ba, bb, ...}
        a+            {a, aa, aaa, ...} 
        ab+           {ab, abb, abbb, etc}

-   is this string in the language defined by this regular expression?
-   describe in English the language defined by this regular expression
-   write an regular expression that defines this language

#### Finite State Automata

-   An **automaton** is a machine *which corresponds to a language*.
    -   it *inputs* a *string*, one character at a time.
    -   it *outputs* a *boolean*: is the string in the language?

-   **Finite automata** accepts or recognizes an input string if and
        only if there exists a path from its start state to a final state
        such that the labels on the path are the terminals in that string.

-   To construct a **nondeterministic** finite state automata,
    1.  Allow more than one transition with the same label.
    2.  Allow *ε* transition
    3.  Recognize an input string just in case there exists *some* path
            from start state to a final state such that the labels on the
            path are the terminals in the string.

-   If the finite state automata does not follow these rules, it is a
        **deterministic** finite state automata.

##### Types of questions

-   is this string accepted by this finite automata?
    -   To solve this, use the starting state as the first letter in the
            string and only go through those states with edges with ensuing
            letters. If there exists no path from the start state to a valid
            end state through existing edges, then the string is not valid.

-   describe in English the language accepted by the finite automata.
    -   To solve this, step through a few possible and valid paths for
            the FSA and generalize from the pattern.

-   write an finite automata that accepts this language

### Functional Programming & Scheme

-   shallow and deep recursion on lists
-   accumulator recursion and tail recursion
-   lambda and closures
-   functions that take functions as arguments
    -   apply, map, foldr, plot, compose, etc.

-   functions that return functions
    -   null-safe, repeat-cols, add-check
    -   encapsulating patterns

-   functions stored in data structures

### Midterm Fall 2011

1.  Consider the Finite State Automaton (FSA) defined by the following
        diagram:

    -   Is this FSA deterministic or non-deterministic? Why?
        -   The necessary and sufficient conditions for a NFA are at
                least one *ε* or multiple state transitions (multiple
                edges).

    -   Write a Regular Expression that specifies the same language as
            the FSA

2.  Consider the following grammar, `G1`:

        S   => Foo # S | Foo
        Foo => Foo % Fie | Fie
        Fie => 0 | 1 | a | b | ( S )

    -   Draw a parse tree to show that

            a # b % 1

        is in the language of `G1`

                      S
                  Foo # S
                  Fie # Foo
                 a  # Foo % Fie
                 a  # Fie % 1
                 a   # b   % 1

        Roughly, a methodology for solving these is to begin with
        whatever your start symbol is on scratch paper, write at the
        bottom whatever your desired expression is, and fill in the
        paths using your fantastic powers of intuition and foresight as
        a human being. This would be harder to do algorithmically than
        intutively for small cases, I suspect.

    -   Add parentheses to the following to show the order of operations
            implied by `G1`.

        -   `(a % b) % 0`
        -   `0 # (1 % a)`
        -   I think the strategy to solve these is to begin with the
                "deepest" level of the language, the furthest from the
                starting expression, and those expressions that are together
                there are "implied" to be connected with higher precedence
                than those are higher levels. Because the `#` is "higher"
                than the `%` operator, it's precedence is lower.

3.  Describe in English the language accepted by the following
        Nondeterministic Finite State Automaton. The start state is D. The
        only accepting state is F.

4.  The function `(repeat n x)` returns a list of `n` copies of `x`.
        E.g., `(repeat 3 'w)` should return `(w w w)`. `(repeat 2 '(a b))`
        returns `((a b) (a b))`. If `n` is `0` repeat should return `( )`.

        ;WRONG:
        (define (repeat n x)
            (if (eq? n 0)
                x                             ; this a number, not a list
                (repeat (- n 1) (append x x)) ; this is just shitty, but ...
            )
        )

        ;RIGHT:
        (define (repeat n x) 
            (if (eq? n 0)                 ; if n == 0
                '()                       ; return the empty list
                (cons (repeat (- n 1) x)) ; else build a list with the return value
                                          ; of repeat(n - 1, x)
            )
        )

5.  The function `(deep-member x lst)` returns true if `x` is a member
        of list `lst` at any depth and false otherwise. E.g.,
        `(deep-member 's '(e r ((x s) t))` returns `#t` (true) while
        `(deep-member 'a '(e r ((x s) t)))` returns `#f` (false). You may
        assume `x` is a number or symbol, not a list.

        (define (deep-member x lst)
            (if (null? lst)
                #f
                (if (eq? (car lst) x)
                    #t
                    (or (deep-member x (cdr lst)) (deep-member x ()))
                )
            )
        )

6.  Define `(for-n start stop fn)`. It takes three arguments: start and
        stop, which are numbers, and fn which is a function of one argument.
        `For-n` calls `fn` several times, first with the argument `start`,
        then with `start+1` then ... finally with `stop`. It returns a list
        of the results of these calls. If `start > stop`, `for-n` simply
        returns the empty list without doing any calls to `fn`.

        (define (for-n start stop fn)
            (if (> start stop)
                '()
                (cons (fn start) (for-n (+ start 1) stop fn))
            )
        )

7.  `(protect-zero fn)` takes one argument, `fn`, a function which
        itself takes one argument. The value of `protect-zero` is also a
        function of one argument. Let us call this the result function. If
        its argument is not `0`, the result function just calls `fn` and
        returns whatever `fn` returns. If the result function's argument is
        `0`, it does not call `fn` but instead returns the symbol `OOPS`.

        (define (protect-zero fn)

        )

### Midterm Fall 2012

1.  Consider the Finite State Automaton (FSA) defined by the following
        transition table:

    -   Is this FSA deterministic or non-deterministic? Why?
    -   Complete the following grammar. It must specify the language
            accepted by the FSA above.

    -   Write a Regular Expression that specifies the same language as
            the FSA above.

2.  Suppose a language had logical expressions using the operators \\\^
        and v, with \^ having higher precedence. The letters t and f are
        constants and p and q are variables. An expression of the form
        <value> \^ <value> \^ <value> means (<value> \^ <value>) \^ <value>
        and <value> v <value> v <value> means <value> v (<value> v <value>)
        Complete the following grammar for these expressions.

3.  Write scheme functions for each of the following. You may write
        additional helper functions if you wish.

    1.  Function countFie takes a list as its argument and returns a
            count of how many times the symbol fie appears as a top-level
            element in the list. E.g., (countFie ‘(a fie (fie b) fie))
            returns 2. Use recursion, but not higher-order functions, e.g.
            not map.

            (define (countFie lst)                ; function definition
                (if (null? lst)                   ; base case
                    0                             ; base case return value
                    (if (eq? (car lst) 'fie)      ; current equal "fie"?
                        (+ 1 (countFie (cdr lst))); then return 1 plus the rest
                        (countFie (cdr lst))      ; else keep counting
                    )
                )
            )

    2.  Write (countAllFie lst) takes a list and returns a count of how
            many times the symbol fie appears at any level of the list.
            E.g., (countAllFie '(fie foo ((fie 3)))) returns 2. (countAllFie
            'fie) returns 1. Your definition must use map.

    3.  Finish the function add-squares-h below. Add-squares-h is a
            helper function for add-squares. Add-squares takes a list of
            numbers and returns the sum of the squares of these numbers.
            E.g., (add-squares '(3 4)) returns 25. Accum is an accumulator.
            Add-squares-h must be tail-recursive.

            (define (add-squares lst) (add-squares-h lst 0)) ; given
            (define (add-squares-h lst accum)                ; given
                (if (eq? lst null)                           ; if list is null
                    accum                                    ; then return accum
                    (add-squares-h (cdr lst) ; otherwise, call a-s-q on the next lst
                                   (+ accum (* (car lst) (car lst))) ; can square the
                                                                     ; current thing
                    )
                )
            )

    4.  Define (compose f g) The arguments f and g are each a function
            of one argument. The value returned by compose is a function,
            the composition of f and g. That is, ((compose (lambda (x) (+ 1
            x))(lambda (x)(\* x x))) 5) returns 26.

            (define compose(f g) ; definition line
                (lambda(x)       ; this returns a function, need lambda
                    (f(g x))     ; perform `f` on return of performing `g` on `x`
                )
            )

October 26th, 2013 <small>Exercise Set 5: Prolog</small>
--------------------------------------------------------

1.  Translate the following into a set of prolog facts and rules. It
        should be possible for Prolog to infer 5 from 1 through 4.

    1.  Joe is in the toy department

            inside(joe, toy_dept).

    2.  If someone is in a department they report to the head of that
            department.

            report(X, Y, dept) :- inside(x, dept), head(y, dept). 

    3.  Sam is the head of the toy department.

            head(sam, toy_dept).

    4.  Everyone's salary is less that the salary of the person they
            report to.

            paid_less(X, Y) :- report(X, Y, Z).

    5.  Joe's salary is less than Sam's salary.

            paid_less(joe, sam).

2.  Write a definition in Prolog for the predicate `fib(N, F)` which is
        true if *F* is the *N*th fibonacci number, *f**i**b*<sub>*N*</sub>,
        defined as follows: *f**i**b*<sub>0</sub> is 0,
        *f**i**b*<sub>1</sub> is 1, and for *N* \> 1,

    *f**i**b**N* = *f**i**b**N* − 1 + \*f**i**b\*\*N\* − 2

        fib(0, 0).
        fib(1, 1).
        fib(N, F) :- A is N - 1, 
            B is N - 2,fib(A, AF), 
            fib(B, BF),NF is AF + BF.

3.  Write a definition in Prolog for the predicate double, where
        double(A, B) is true for lists A and B if B has the same elements as
        A, but repeated. E.g. double([dog, cat], [dog, dog, cat, cat]) is
        true, but double([dog, cat], [dog, cat, dog, cat] is not true.
        double([dog, cat], L) should bind L to [dog, dog, cat, cat]. The
        query double([a, b], L). should succeed, binding L to [1, 1, b, b].

        double_up([], []).
        double_up([A | As], [A, A | Rest]) :- double_up(As, Rest).

        double([], []).
        double(A, B) :- double_up(A, A) = B.

4.  Write a definition in Prolog for the predicate without0(L1, L2)
        which is true if L2 is a copy of L1 with all 0's removed. E.g.,
        without0([4, 0, 5, 6, 0], [4, 5, 6]) is true and without0([4, 0, 5],

    1.  binds L to [4, 5].

        remove0([], A, []). remove0([H | T], A, Result) :- H = A,
        remove0(T, A, Result). remove0([H | T], A, [H | Result]) :-
        remove0(T, A, Result).

        without0([], []). without0(A, B) :- remove0(A,0,Result), Result
        = B.

October 19th, 2013 <small>Logic Programming</small>
---------------------------------------------------

Constants
:   Represent entities, which are "things" and not functions or
    relations.

:   In Prolog, start with lower case.

        albert, my_house

Variables
:   Stands for constants

    In Prolog, start with upper case or `_`

        X, House, _xyz, _321

Functors
:   -   Represent a function from entities to an entity.
        -   "Function" = "Mapping" as in math, not a computation.

:   -   In Prolog, start with lower case like constants.
        -   In fact, a constant is just a term with no arguments.

Terms
:   Represent an entity.

:   -   Constant, variable, or `<functor>[(<term> {, <term>})]`
        -   `father(albert)` might represent the father of albert
        -   `successor(victoria)` might represent the successor of
                victoria

        -   `sum(1, 2)` might represent the sum of 1 and 2

Predicates
:   Represent a function from entity (terms) to a boolean.

:   In Prolog, start with lower case like functors.

Atoms
:   Logical statement without and, or, not, etc.

        <predicate>(<term> {, <term>})
        older( father(Person), Person) 
        square(X, 4)

Horn clauses
:   A horn clause is

        c h1 ^ h2 ^ h3 ^ ... ^ h_n

    Antecedent `h`
    :   Conjunction of zero or more conditions which are \*atomic
        formulas\*.

        Alternatively, **subgoal** or **tail**.

    Consequent `c`
    :   The consequent is true just in case all the antecedents are
        true.

        Alternatively, called **goal** or **head**.

:   Written as,

        c :- h1 , ... , hn.

:   A horn clause with no tail is a **fact**.

    A horn clause with tail is a **rule**.

List
:   A sequence of elements separated by commas.

        [ first element | rest_of_list ]

    |list|head|tail|
    |----|----|----|
    |`[a, b, c]`|`a`|`[b, c]`|
    |`[X,[cat],Y]`|`X`|`[[cat],Y]`|
    |`[a,[b, c],d]`|`a`|`[[b,c],d]`|
    |`[X | Y]`|`X`|`Y`|

:   List functions:

    -   `append`
    -   `last`
    -   `reverse`
    -   `reverse-conc`

Member Function
:   Goal-oriented semantics
    :   can get value assignment for goal member(A,[B|C]) by showing
        truth of subgoal member(A,C) and retaining value bindings of the
        variables

    Procedural semantics
    :   think of head of clause as procedure entry, terms as parameters.
        then body consists of calls within this procedure to do the
        calculation. variables bindings are like "returned values".

October 29th, 2013 <small>[Quick'n'Dirty Prolog Tutorial](http://www.cs.utexas.edu/~cannata/cs345/Class%20Notes/12%20prolog_intro.pdf)</small>
----------------------------------------------------------------------------------------------------------------------------------------------

### Prolog Program Components

-   A **fact** is a *single piece of information*.
    -   To represent that the sky is blue, you would write:

            blue(sky).

    -   Simiarly, `mammal(rabbit).` says that rabbits are mammals.
    -   Facts can have multiple arguments,

            plays(john, hockey).

        Which represents that John plays hockey.

> Prolog constants are in lower case, variables are in upper case,
> domains are not defined explicitly, and entries always end with a
> period.

-   **Rules** are used to generate new information from facts, other
        rules, and themselves. They have the form:

        head :- body.

    Where the head and the body are clauses that typically use variables
    instead of constants.
    -   For instance, consider the rule:

            grandparent(X, Z) :- parent(X, Y), parent (Y, Z).

        The rule says that `X` is the grandparent of `Z` when `X` is a
        perent of `Y` and `Y` is a parent of `Z`.
    -   Rules can be recursive. Consider:

            ancestor(X,Y) :- parent(Z,Y), ancestor(X,Z).

-   Now there are **queries**. When you want to ask Prolog a question,
        you supply a query.

    -   Queries are like rules without bodies. Prolog will take the head
            and find out if it is true or false.

    -   If the query has variables, Prolog will attempt to find all
            possible values that can be used in place of the variables to
            make the query true and tell you what they are.

    -   Consider the database:

            parent(amy,bob).
            parent(bob,cathy).
            parent(bob,doug).
            grandparent(X,Z) :- parent(X,Y) , parent(Y,Z).
            ancestor(X,Y) :- parent(X,Y).
            ancestor(X,Y) :- parent(Z,Y) , ancestor(X,Z).

        -   The query `parent(amy,bob)` will be true.
        -   The query `ancestoru(bob, doug)` is also true.
        -   The query `parent(bob,X)` will return all the facts that
                would make the query true.

### Connecting Prolog to Predicate Logic

-   Think of the `:-` symbol in Prolog as representing the word "if".
    -   Interanlly, Prolog represents rules in a form known as \*\*horn
            clauses**. These are the disjuction of predicates in which at
            most one of the predicates is not negated. Consider the
            grandparent clause:

            grandparent(X,Z) :- parent(X,Y) , parent(Y,Z).

    -   Rewritten in logical notiation,

        ∀ *x*∀ *y*∀ *z*((*P*(*x*, *y*) ∧ *P*(*y*, *z*)) → *G*(*x*, *z*))

    -   We know that *p* → *q* ≡ ¬*p* ∨ *q*, so the above is also:

        ∀ *x*∀ *y*∀ *z*(¬(*P*(*x*, *y*) ∧ *P*(*y*, *z*)) ∨ *G*(*x*, *z*))

    -   Apply de Morgans for a horn clause:

        ∀ *x*∀ *y*∀ *z*(¬*P*(*x*, *y*)¬*P*(*y*, *z*) ∨ *G*(*x*, *z*))

November 9th, 2013 <small>Midterm 2 Study Guide</small>
-------------------------------------------------------

### Textbook <small>Chapter 11.2 *Prolog*</small>

#### Introduction

-   A Prolog interpreters runs in the context of *databases*
    and *clauses* that are assumed to be true.
    -   Each clause is composed of *terms*, which may be constants
        variables, or *structures*.
    -   A constant is either an tom or a number.
    -   A Structure can be thought of as either a logical predicate
        or data structure.

-   Atoms in Prolog looks like an identifier beginning with a lowercase
    letter, a sequences of "punctuation" characters.
-   Variables can be *instantiated*.
-   Structures consist of an atom called a *functor* and a list of
    arguments:

        rainy(rochester).
        teaches(scott, cs254).
        bin_tree(foo(bin_tree(bar, glarch))).

-   Prolog requires the opening parenthesis to come immediately after
    the functor, with no intervening space.
    -   Arguments can be arbitrary terms: constants, variables, or
        nested structures.
    -   We use the term *predicate* to refer to the combination of a
        functor and an arity.

-   The clauses in a Prolog database can be classified as *facts* or
    *rules*, each of which ends with a period.
    -   A fact is a horn clause without a right-hand side.

-   A rule has a right hand side:

        snowy(X) :- rainy(X), cold(X).

-   The token `:-` is the implication symbol.
    -   The comma indicates "and."
    -   Variables that appear in the head of a Horn clause are
        universally quantified: for all `X`, `X` is snowy is `X` is
        raining and `X` is cold.

-   It is possible to write a clause with an empty left-hand side.
    Such a clause is called a *query* or a *goal*.
    -   Queries do not appear in Prolog programs.
        -   Rather, one build a database of facts and rules and then
            initiates execution by giving the Prolog interpreter
            a query to be answered.

-   It most implementation of Prolog, queries are entered with
    a special `?-` version of the implication symbol. An example:

        rainy(seattle).
        rainy(rochester).
        ?- rainy(C).

    -   The Prolog interpreter would respond with:

            C = seattle

    -   Of course, `C = rochester` would also be a valid answer, but
        Prolog will find `seattle` first, because it comes first in
        the database.
        -   If we want to find all possible solutions, we can ask the
            interpreter to continue by typing a semicolon:

                C = seattle ;
                C = rochester ;
                No

    -   Similarly, given:

            rainy(seattle).
            rainy(rochester).
            cold(rochester).
            snowy(X) :- rainy(X), cold(X).

        -   The query:

                ?- snowy(C).

            Will yield only one solution.

#### Resolution and Unification

-   The *resolution principle*, says that if $C_1$ and $C_2$ are
    Horn clauses and the head of $C_1$ mathches on of the terms in
    the body of $C_2$, then we can replace the term in $C_2$ with
    the body of $C_1$.
    -   Consider the following example:

            takes(jane_doe, his201).
            takes(jane_doe, cs254).
            takes(ajit_chandra, art302).
            takes(ajit_chandra, cs254).
            classmates(X, Y) :- takes(X, Z), takes(Y, Z).

        -   If we let `X` be `jane_doe` and `Z` be `cs254`, we can replace
            the first term on the right hand side of the last clause with
            the empty body of the second clause, yielding the new rule:

                classmates(jane_doe, Y) :- takes(Y, cs 254).

            In other words, `Y` is a classmate of `jane_doe` if `Y` takes
            `cs254`.

        -   The pattern-matching process ised to associate `X` with `jane_doe`
            and `Z` with `cs254 is known as *unification*.
        -   Variables that are given values as a result of unification are
            said to be *instantiated*

-   The unification rules for Prolog state:
    1.  A constant unifies only with itself.
    2.  Two structures unify if and only if they have the same functor
        and the same arity, and the corresponding arguments unify
        recursively.
    3.  A variable unifies with anything. If the other thing has a value,
        then the variable is instantiated. If the other thing is an
        uninstantiated variable, then the two variables are associated
        in such a way that if either is given a value later,
        that value will be shared by both.

-   Equality in Prolog is defined in terms of "unifiability."

        ?- a = a.
        Yes             % constant unifies with itself
        ?- a = b.
        No              % but not with another constant
        ?- foo(a, b) = foo(a, b).
        Yes
        ?- X = a.
        X = a ;
        No
        ?- foo(a, b) = foo(X, b).
        X = a ;         % arguments must unify
        No              % only one possibility

    -   It is possible for two variable to be unified wihout
        instantiating them. If we type:

            ?- A = B.

        the interpreter will simply respond

            A = B

        -   If, however, we type

                ?- A = B, A = a, B = Y.

            (unifying `A` and `B` before binding `a` to `A`) the interpreter
            will respond

                A = a
                B = a
                Y = a

    -   In a similar vein, suppose we are given the following rules:

            takes_lab(S) :- takes(S, C), has_lab(C).
            has_lab(D) :- meets_in(D, R), is_lab(R).

        -   (S takes a lab class if S takes C and C is a lab class. 
            Moreover D is a lab class if D meets in room R and R is a lab.) 
            An attempt to resolve these rules will unify the head of the 
            second with the second term in the body of the first, causing 
            C and D to be unified, even though neither is instantiated.

#### Lists

-   Like equality checking, list manipulation is a sufficiently common
    operation in Prolog to warrant its own notation.
    -   The constuct `[a, b, c]` is syntatic sugar for the structure
        `.(a, .(b, .(c, [])))` where `[]` is the empty list and
        `.` is a built in `cons`-like predicate.
    -   Prolog adds an extra convinience, however: an optional vertical
        bar that delimits the "tail" of the list.
        -   Using this notiation, `[a, b, c]` could be expressed as
            `[a, | [b ,c]], [a, b | [c]], or [a, b, c | []]`.

    -   This vertical bar-notation is particularly handy when the
        tail of the list is a vraible:

                member(X, [X | _]).
                member(X, [_ | T]) :- member(X, T).
                sorted([]).         % empty list is sorted
                sorted([_]).        % singleton is sorted
                sorted([A, B | T]) :- A =< B, sorted([B | T]).
                   % compound list is sorted if first two elements are in order and
                   % remainder of list (after first element) is sorted

        -   Here `<=` is a built-in predicate that operates on numbers.
            -   The underscode is a placeholder for a variable that is not 
                needed anywhere else in the clause.
            -   Note that `[a, b | c]` is the *improper* list `.(a, .(b
                c)).`
            -   The sequence of tokens `[a | b, c]` is syntactically invalid.

-   One of the interesting about Prolog resolution is that it does not
    in general distinguish between "input" and "output" arguments.
    -   Thus, given:

            append([], A, A).
            append([H | T], A, [H | L]) :- append(T, A, L).

        We can type:

            ?- append([a, b, c], [d, e], L).
            L = [a, b, c, d, e]
            ?- append(X, [d, e], [a, b, c, d, e]).
            X = [a, b, c]
            ?- append([a, b, c], Y, [a, b, c, d, e]).
            Y = [d, e]

    -   This example highlight the difference between functions and Prolog
        predicates.
        -   The former have a clear notion of inputs (arguments) and
            outputs (results).

#### Arithmetic

-   The usual arithmetic operators are available in Prolog, but they play
    a role of predicates, not of functions.
    -   Thus, `+(2, 3)`, which may also be written `2 + 3` is a two-
        argument structure, not a function call.
        -   It will not unify with `5`:

                ?- (2 + 3) = 5
                No

-   To handle arithmetic, Prolog provides a built-in predicate, `is`, that
    unifies its first argument with the arithmetic value of its second
    argument:

        ?- is(X, 1+2). X=3
        ?- X is 1+2.
        X = 3
        ?- 1+2 is 4-1.
        No
        ?- X is Y.
        ERROR
        % infix is also ok
        % first argument (1+2) is already instantiated
        % second argument (Y) must already be instantiated
        ?- Y is 1+2, X is Y.
        Y=3
        X = 3 % Y is instantiated by the time it is needed

#### Search/Execution Order

> How does Prolog go about answering a query? 

-   What it needs is a sequence of resolution steps that will
    build the goal out of clauses in the database, or a proof
    that no such sequence exists. 
    -   In the realm of formal logic, one can imagine two
        principal search strategies:
        -   Starting with the existing clauses and work forward,
            attempting to derive the goal. This strategy is known
            as *forward chaining*.
        -   Start with the goal and work backward, attempting to
            "unresolve" it into a set of preexisting clauses.
            This strategy is known as *backward chaining*.

    -   If the number of existing rules is very large, but the number
        of facts is small, it is possible for forward chaining to
        discover a solution more quickly than backward chaining.
        -   In most circumstances, however, backward chaining turns
            out to be more efficient.
        -   Prolog is defined to use backward chaining.

-   Because resolution is associative and commutative, a backward
    chaining theorem prover can limit its search to sequences of
    resolutions in which terms on the righ-hand side of a cluase
    are unified with the heads of other cluases on by one in some
    particular order.
    -   The resulting search can be described in terms of a tree of
        subgoals.
    -   The Prolog interpreter explores this tree-depth first,
        from left to right.
    -   It starts at the beginning of the database, searching for
        a rule $R$ whose head can be unified with the top-level goal.
    -   It then considers the terms in the body or $R$ as subgoals,
        and attempts to satisfy them, recursively, from left to right.
    -   If at any point a subgoal fails, the interpreter returns to the
        previous subgoal and attempts to satisfy it in a different way.

![Backtracking search in Prolog](../img/cs-pl-prolog.png)

-   The process of returning to previous goals is known as *backtracing*
    -   Whenever a unification operation is "undone" in order to pursue
        a different path through the search tree, variables that were given
        values or associated with one another as a result of that unification
        are returned to their uninstantiated or unassociated state.
    -   The effect is similar to the breaking of bindings between actual and
        formal parameters in an imperative programming language, except
        that Prolog couches the bindings in terms of unification rather
        than subroutine calls.

-   Space management for backtracking search in Prolog usually follows
    the single-stack implementation of iterators.
    -   The interpreter pushes a frame onto its stack every time it begins
        to pursue a new subgoal $G$.
    -   If $G$ succeeds, control returns to the "caller.""
        -   But $G$'s frame remains on the stack.

    -   Later subgoals will be given space *above* this dormant frame.
        -   If subsequent backtracing causes the interpreter to search
            for alternative ways of satisfying $G$, control will be able
            to resume where it last left off.
            
-   The fact that clauses are ordered, and that the interpreter considers
    them from first to last, means that the results of a Prolog program
    are determinitic and predictable.
    -   In fact, the combinatino of ordering and depth-first search means
        that the Prolog programmer must oftern consider the order to ensure
        that recursive programs will terminate.
    -   Suppose for example that we have a database describing a directed
        acyclic graph:

            edge(a, b).  edge(b, c).  edge(c, d).
            edge(d, e).  edge(b, e).  edge(d, f).
            path(X, X).
            path(X, Y) :- edge(Z, Y), path(X, Z).

        The last two clause tell us how to determine whether there is
        a path from node `X` to node `Y`.
        -   If we were to reverse the order of the terms in the right-hand
            side of the final clause, the the Prolog interpreter would search
            for node `Z` that is reachable from `X` before checking to see 
            whether there is an edge from `Z` to `Y`.
        -   The program would still work, but it would not be as efficient.

-   Consider what would happen if in addition we were to reverse the
    order of the last two clauses:

        path(X, Y) :- path(X, Z), edge(Z, Y).
        path(X, X).

    From a logical point of view, our database still defines the same
    relationships.
    -   A Prolog interpreter, however, will no longer be able to find answers.
        -   Even a simple query like `?- path(a, a)` will never terminate.

    -   The interpreter first unifies `path(a, a)` with the left-hand side of 
        `path(X, Y) :- path(X, Z), edge(Z, Y).` It then considers the goals 
        on the right-hand side, the first of which `(path(X, Z))`, 
        unifies with the left-hand side of the very same rule, leading 
        to an infinite regression.


#### Imperative Control Flow

-   We have seen that the ordering of clauses and of terms in Prolog is
	significant, with ramifications for efficient, termination, and choice
	among alternatives.
	-   In addition  to simple ordering, Prolog provides the programmer
		with several explicit control-flow features
		-   The most important of these features is known as `cut`.

-   The `cut` is a zero-argument predicate written as an exclamation point
	-   As a sungal it alwauys succeeds, but with a crucual side effect: 
		it commit the interpreter to whatever choices have been made
		since unfifying the parent goal with the left-hand side of the
		current rule, including the choice of the unification itself.
	-   If a given atom `a` appears in list `L` $n$ times, the goal
		then the goal `?- member(a, L)` can succeed $n$ times.
	-   They can lead to wasted computation, particularly from long
		lists, when `member` is following by a goal that may fail:

			prime_candidate(X) :- member(X, candidates), prime(X).

		Suppose that `prime(X)` is expensive to compute. To determine
		whether `s` is a prime candidate, we first check to see whether
		it is a member of the `candidates	 list, and then check to see
		whether it is prime.
		-   If `prime(a)` fails, Prolog will backtrack and attempt to 
			satisfy `member(a, candidates)` again. If `a` is in the
			`candidates` list more than once, then the goal will suceed
			again, leading to the reconsideration of the `prime(a)` subgoal,
			even though it is doomed to fail. *We can save substantial
			time by cutting off all further searches for `a` after
			the first is found:

				member(X, [X | _]) :- !.
				member(X, [_ | T]) :- member(X, T).

			The cut on the right hand side of the first rule says that if
			`X` is the head of `L`, we should not attempt to unify
			`member(X, L)` with the left hand side of the second rule,
			the cut commits us to the first rule.

-   An alternative way to ensure that `member(X, L)` succeeds no more than
	once is ember a use of `\+` in the seoncd cluase:

		member(X, [X | _]).
		member(X, [H | T]) :- X \= H, member(X, T).

	Here `X \= H` means `X` and `H` will not unify.

### Scheme Macros <small>via [Will Donnelly](http://www.willdonnelly.net/blog/scheme-syntax-rules/)</small>

-   You use define-syntax to create a top level binding, and let-syntax 
	bears the same relationship to define-syntax as you’d expect.

		;; define-syntax is used to create
		;;  a top-level binding of a macro
		(define-syntax macro
		  <syntax transformer>)

-   Lets say we want to define a `while` loop to work like this:

		;; A simple while loop
		(define x 0)
			(while (< x 5)
			(set! x (+ x 1))
			(print x))

-   To do this, we need to use a **syntax transformer**.

		(define-syntax while
			(syntax-rules (<keywords>)
			((<pattern>) <template>)
			...
			((<pattern>) <template>)))

-   This is how to code a `while` loop in Scheme:

		(let loop ()
			(if condition
				(begin
					body ...
					(loop))
				#f)
			)

-   This code above is what is to be placed in `<template>`.

		(define-syntax while
		  (syntax-rules ()
		    ((while condition body ...)
		     (let loop ()
		       (if condition
		           (begin
		             body ...
		             (loop))
		           #f)))))



### Prolog <small>Basic operation of Prolog</small>

Unification
:   An algorithmic process of solving equations between symbolic
	expressions. 

:   Prolog unification matches two Prolog terms T1 and T2 by finding
	a substitution of variables mappich M such that if M is applied
	T1 and M is applied to T2 and the results are equal.

	For example, Prolog uses unification in order to satisfy
	equations ...

		?- p(X, f(Y), a) = p(a, f(a), Y).
		X = a  Y = a

		?- p(X, f(Y), a) = p(a, f(b), Y).
		No

	In the first case the successful substitution is `{X/a, Y/b}`,
	and for the second example there is no substitution that would
	result in equal terms.

Backward chaining
:   An inference method that can be described as working backwards
	from the goal(s). It is used in automated theorem provers,
	proof assistants, and other AI application, but it has also
	been observed in primates. 

Backtracking
:   Suppose that we have the following database:

		eats(fred, pears).
		eats(fred, t_bone_steak).
		eats(fred, apples).

	So far we have only been able to ask if Fred eats specific thing.
	Suppose that I wish to instead to answer the question, "What are
	all the things that Fred eats?" To answer this I can use variables
	again. Thus, I can type in the query.
	
		?- eats(fred, FootItem).

	As we have seen earlier, Prolog will answer with

		FoodItem = pears

	This is because it has found the first clause in the database.
	If you keep asking, Prolog will respond `t_bone_steak` then
	`apples` then `no`. 

### Logical meaning of Prolog

> The token `:-` is the implication symbol.
>
> The comma indicates "logical and."
> 
> Variables that appear in the head of a Horn clause are
> universally quantified.

### Prolog programming

Unification (on lists)

:   Consider the rule:

		append([A|B],Y,[A|Z]):- ...

	And the query:

		?- append([a,b],[c],W)

	Unify?

		A=a, B=[b], Y=[c], W=[a | Z]

Cut
:   The cut, in Prolog, is a goal, written as !, which always succeeds, 
	but cannot be backtracked past. It is best used to prevent unwanted 
	backtracking, for example, to prevent extra solutions being found by 
	Prolog and avoid additional computations that are not desired or 
	required in a program.

	The cut should be used sparingly. There is a temptation to insert 
	cuts experimentally into code that is not working correctly. If a 
	test is unnecessary because a cut has guaranteed that it is true, 
	it is good practice to say so in a comment at the appropriate place.

:   Green cut

	:   A use of a *cut* which only improves efficiency is referred to as a *green cut*. 
		For example:

			gamble(X) :- gotmoney(X),!.
			gamble(X) :- gotcredit(X), \+ gotmoney(X).

		This is called a green cut operator. The `!` simply tells the interpreter to 
		stop looking for alternatives. But you'll notice that if `gotmoney(X)` fails 
		it will check the second rule. Checking for `gotmoney(X)` in the second rule 
		seems useless since you already know that if Prolog is there then 
		`gotmoney(X)` failed before, otherwise the second rule wouldn't be 
		evaluated in the first place. However, by explicitly writing `\+ gotmoney(X)`, 
		you guarantee that the second rule will always work, even if the first 
		one is removed by accident or changed.

	Red Cut

	:   A *cut* that isn't a *green cut* is referred as a *red cut*, for example:

			gamble(X) :- gotmoney(X),!.
			gamble(X) :- gotcredit(X).

		You depend on the proper placement of the cut operator and the order 
		of the rules to determine their logical meaning. If for any reason the 
		first rule is removed (e.g. by a cut-and-paste accident), the second 
		rule will be broken, i.e., it will not guarantee the rule `\+ gotmoney(X)`.

:   A cut, simply stated, commits Prolog to the instantiations made prior to it.

Numbers, `is`
:   The is built-in predicate is used in Prolog to force the evaluation of 
	arithmetic expressions. If you just write something like `X = 2 + 4`, the 
	result is to bind `X` to the unevaluated term `2 + 4`, not to `6`.

		?- X = 2 + 4.
		X = 2+4

	If instead you write X is 2 + 4, Prolog arranges for the second argument, 
	the arithmetic expression 2 + 4, to be evaluated (giving the result 6) 
	before binding the result to X.

		?- X is 2 + 4.
		X = 6

	If you want to check some arithmetic with a function or something or another,
	it would look like this:

		0 is N mod 2

Trees
:   -   Really have built an evaluation tree for the query `member(X,[a,b,c])`.
	-   Search trees provide a formalism to consider all possible computation paths.
	-   Leaves are success nodes or failures where computation can proceed no further.
	-   By convention, to model Prolog, leftmost subgoal is tried first.

Graphs
:   A list of nodes.

	Node

	:   `node(Name, Color, Nbrnames).`

		`node_structure(Name, Graph, node).`

		1.  How to grab all *names* of a node? 
			`all_names(+Graph, -Names) =>`

				all_names([], []).
				all_name([H | T], Namelist) :- 
					node_structure(Name, [H | T], H),
					all_names(T, Tnamelist),           ; until the end level of recursion
					append([Name], Tnamelist, Namelist).

		2.  How to grab the *neighbor* of a node?
			`node_backlinks_valid(+Name, +Nbrnames, +Graph) =>`

				node_backlinks_valid(_, [], _).
				node_backlinks_valid(Name, [H | T], Graph) :-
					node_structure(H, Graph, node(H, _, NbrNames)),
					member(Name, Nbrnames),
					node_backlinks_valid(Name, T, Graph).

		3.  How to grab the *color* of a node?
			`colors_of(+Names, +Graph, -Colors) =>`

				colors_of([], _, []).
				colors_of([H | T], Graph, Colorslist) :-
					node_structure(H, Graph, node(H, Color, _)),
					colors_of(T, Graph, Tcolorlist),
					append([Color], Tcolorlist, Colorlist).

### Practice Exam 2

1.  Finish the definition below of the scheme macro and-not, so that
    (and-not x y) is the equivalent of (and x (not y)). Note that
    `and-not` should have the same kind of “short cut” behavior as `and` and
    `or` have, and as `x && y` has in Java: if `x` is false, it should not
    evaluate `y`, but should just return false. (This is why `and-not` needs
    to be a macro.)

        (define-syntax and-not
			(syntax-rules()
				((_ x y)
					(and x (not y) ; <- this is the answer fill-in
		           ; the exam will provide the name of the macro
				))
			)

2.  Fill in the following prolog predicates.
    1.  `inOrder(List)`. Assume `List` is a list of numbers;
        `inOrder(List)` is true if and only if the numbers in `List` are
        in increasing order. If `List` has `0` or `1` element it is in
        order.

            inOrder([]).  ; if it has no elements
            inOrder([_]). ; if it has one element, any element
            inOrder([ N1, N2 | T]) :- N1 <= N2, inOrder([N2 | T]).

    2.  `suffix(L1, L2)`. Assumes `L1` and `L2` are lists. It is true if
        `L2` is a tail of `L1`. E.g., `suffix([x, a, b], [a, b])` is
        true, as is `suffix([x, y, a, b], [a, b])`,
        `suffix([x, y, z, a, b], [a, b])`, and so on.

			suffix([H | T], T).                  ; general pattern
			suffix([H, T], L2) :- suffix(T, L2). ; split first list,
			                                     ; implies T is equal to L2

3.  For each of the following pairs of fact and goal, say whether they
    will unify, and if so with which bindings

	| Fact              | Goal              | Unify                     |
	|-------------------|-------------------|---------------------------|
	|`foo(Bar, baz).`   |`foo(baz, Bletch).`|`Bar = baz`, `Bletch = baz`|
	|`foo(a, b)`        |`fie(X,Y)`         | Will not unify            |
	|`foo(a, fie(Y, X))`|`foo(X, fie(a,a))` | `X = a, X = Y = a`[^1]    |

1.  The predicate `odd(All, Odds)` is true if `Odds` and `All` are lists
    and `Odds` contains the 1st, 3rd, 5th, etc, elements of `All` (in
    that order), Hint: `[a, b | c]` is a list whose first two elements
    are `a` and `b`, and whose tail after `b` (i.e. the `cddr`) is c.
    `odds([],[])` is also true. Define `odds`:

		odds([],[]).                             ; trivially true base case
		odds([X], [X]).                          ; equality clause
		odds([A, B | C], [H | T]) :- odds(C, T). ; ignores evens in first list

2.  What is the translation into predicate calculus of the prolog rule:
    `cousin(X,Y):- grandparent(X, G), grandparent(Y, G), nonsibling(X, Y)`.

	For all `X` and `Y`, if `X` and `Y` are cousins, then there exists 
	`G` is a grandparent of `X`, `G` is a grandparent for `Y`, and `X` 
	and `Y` are not siblings.

	$$ \forall x y (C(x, y) \to \exists g (G(x, g) \land G(y, g) \land \lnot S(x, y)))$$

3.  What will this print for the query `foo(X, Y).`? (The predicate
    write simply prints its argument.

		foo(1, 2) :- write(12), 1 < 1.
		foo(X, 2) :- fie(X), write(x2), 2<1. 
		foo(1, Y) :- write(y1).

		fie(a) :- write(a). 
		fie(b) :- write(b).

4.  Define the predicate `insertInOrder(Lst, Num, Res)`, where `Lst` is
    a list of numbers in ascending order and `Res` is the result of
    inserting `Num` in its correct place in `Lst`. E.G.,
    `insertInOrder([1, 3, 6, 9], 5, [1, 3, 5, 6, 9])` is `true`.

		insertInOrder([], N, [N | T]).
		insertInOrder([H | T], N, [H, N | T]).
		insertInOrder([H1 | T1], N, [H2 | T2]) :- H1 <= N, 
			                                      insertInOrder(T1, N, T2).

5.  Given the following code, what will the query `vacation(A)` print?
    Hint: If the variable `V` has value `a`, `write([fun, V])` prints
    `[fun, a]`. fail is a predicate that always fails.

		vacation(Activity) :- fun(Activity), write([fun, Activity]),
		                       cheap(Activity), write([cheap, Activity]), !, fail.       
		fun(Activity):- speed(Activity, S), S > 50. 
		fun(Activity):- outdoors(Activity). 
		speed(skiing, 75).
		outdoors(skiing).
		outdoors(hiking). 
		cheap(hiking).

		?- vacation(A)
		[fun,skiing][fun,skiing][fun,hiking][cheap,hiking] 
		false
		

December 15th, 2013 <small>Final Exam Study Guide</small>
-----------------------------------------------------------

### Meta interpreters

Meta-interpreter

:   A *meta* interpreter is an interpreter for a language written in
	the language it interprets.

	> Why do such a thing?

	-   The easiest language to write a Prolog interpreter is Prolog.
	-   Once you have an interpreter, you can modify it.

### Types

#### What is a type?

-   A set of values and the valid operations on those values.
	-   Integers

			+ - * div < <= = >= >

	-   Arrays

			lookUp(<array>, <index>)
			assign(<array>, <index>, <value>)
			initialize(<array>)
			setBound(<array>)

	-   User-defined types:
		-   Structs
		-   Classes

-   Program semantics embedded in types used
	-   Additional correctness check provided beyond valid syntax.

##### Constructed types

-   Constructive point-of-view
	-   Primitive types, `int`, `char`, `bool`, `enum`
	-   Composition/constructive types:

		Structure | Function
		----------|----------
		reference | pointerTo(int)
		array | arrayOf(char)
		record | record(age:int, name:string)
		subrange | int[1..20]
		union | union(int, pointerTo(char))
		list | list(...)
		set | setOf(color)
		function | float, int

##### Varieties

-   Implicit
	-   Values are typed, but variables aren't
	-   Prolog, Scheme, Lisp, Smalltalk, Python

-   Explicit
	-   Declarations bind types to variables at compile time
	-   Pascal, Algol68, C, C++, Java

-   Mixture
	-   Implicit by default but allows explicit declarations
	-   Haskell, ML, Common Lisp
	-   Trust declarations result in speed
	-   Test declarations result in correctness

##### Systems

-   Rules for constructing types
-   Rules for determining/inferring the type of expressions
-   Rules for compatibility
	-   In what contexts can values of a type be used?

-   Rules for type equivalence or type conversion
	-   Determining that an expression can be used in some context

##### Expressions

-   If $f$ has type $S$ and $T$, $x$ has type $S$, then $f(x)$ has
	type $T$
	-    Type of `3 div 2` is `int`
	-    Type of `round(3.5)` is `int`

-   *Type error* is using wrongly typed operands in an operation
	
		round("Nancy")
		3.5 div 2
		"abc" + 3

#### Type checking

-   *Goal*: To find out as early as possible, if each procedure and operator is
	supplied with the correct type of arguments.
	-   Type error: when a type is used improperly in a context.
	-   Type checking performed to prevent type errors

-   Modern PLs often designed to do type checking during compilation.

##### Varieties of type checking

-   Compile-time (static)
	-   At compile, uses declaration information or can infer types from
		variable uses.

-   Run-time (dynamic)
	-   During executing, checks type of a value before doing operations
		on it.
	-   Uses type tags to record types of values.

-   Combined (compile and run time)

##### Type safety

-   A *type safe* program executes on all inputs without type errors.
	-   Goal of type checking is to ensure type safety.
	-   Type safe does not mean without error.

			read n;
			if n>0 then { y :="ab";
							if n<0 then x := y - 5; }

		-   Not that the assignment to `x` is never executed so program
			is type safe but contains an error.

##### Strong typing

-   Strongly typed PL by definition, PL requires all programs to be type
	checkable.
-   Statically strongly typed PL means that the compiler allows only programs
	that can be type checked fully at compile time.
	-   Algol68
	-   ML

-   Dynamically strongly typed PL means that operations include code to check
	runtime types of operands, if type cannot be determined compile-time.
	-   Pascal
	-   Java

##### Hierarchy of types

![Hierarchy of programs](../img/cs-pl-types.png)

Type | Static checking | Dynamic checking
-----|-----------------|------------------
**Implicit types** | ML | Scheme
**Explicit types** | Algol68 | C, Pascal

##### Difficulties in Static Type Checking

-   If validity of expression depends not only on the types of the operands
	but on their values, static type checking cannot be accomplished.
	-   Taking successors of enumeration types
	-   Using unions without type test guard
	-   Converting ranges into subranges
	-   Reading values from input
	-   Dereferencing `void *` pointers

#### Type conversion

##### Implicit conversion 

-   Also known as *coercion*
-   In C, mixed mode numerical operations
	
		double d, e; e = d + 2 // 2 coerced to 2.0

-   Usually can use widening or conversion without loss of precision
-   Cannot coerce user-defined types or structures
-   But you can do `Shape s = new Circle();`

##### Explicit conversion

-   In Pascal, can explicitly convert types which may lose precision,
	also known as narrowing.

		round(s); // int by rounding
		trunc(s); // int by truncating

-   In C, casting sometimes is explicit conversion

		dqstr((double) n); // where n is declared to be an int
		free list * s; ... (char *) s; // forces s to be considered
		// as pointing to a char for purposes of pointer arithmetic


##### Overloading operators

-   Primitive type of *polymorphism*
	-   When an operator allows operands of more than one type, in
		different contexts

-   Examples
	-   Integer addition: 1 + 2 versus real addition: 1.0 + 2.0
	-   Addition: 2 + 3 is 5, versus concatenation: "abc" + "def" 
		is "abcdef"
	-   Comparision operator used for two different types: 2 == 3
		verssus "abc" == "def" in Python.

##### Primitive Types

-   Issues
	-   Type checking
	-   Representation in the machine

-   Boolean
	-   Use of integer 0 / non-0 versus true/false

-   Char versus string
-   Integer
	-   Length fixed by standards or implementation (portability issues)
	-   Multiplie lengths (C: short, int, long)
	-   Signs

-   Float/real
	-   Should value comparisons be allowed?

#### Arrays

##### Definition

-   Indexed collection of values, often homogenous
-   Access to individual elements through subscript
-   Choices made by PL design:
	-   Subscript syntax
	-   Subscript type, element type
	-   When to set bounds, compile time or run time?
	-   Are bounds changeable
	-   How to initialize? 
	-   What operations allowed on whole arrays?

##### Array type

-   What is part of the array type?
	-   Size?
	-   Bounds?
		-   Pascal: bounds are part of the type
		-   C, Algol68: bounds are not part of type
		-   Must be fixed at compile-time in Pascal but can be set at
			runtime in C and Fortran

	-   Dimension? always part of the type

-   Choice has ramifications on kind of type-checking needed

##### Choices for Arrays

-   Global lifetime, static shape (in static memory)
-   Local lifetime
	-   Static shape
	-   Shape bound at elaboration time when control enters a scope
		-   Ada, Fortran, allow definition of array bounds when function
			is elaborated

-   Arrays as objects (Java)
	-   Shape bound at elaboration time (kept in heap)

			int[] a; a = new int[size];

##### Implementation

-   For fixed length array, symbol table keeps track of name, element type,
	bounds etc during compilation, can allocate in static storage or on
	frame of declaring method.
-   For arrays whose length is not knowable at compile-time, we use a dope
	vector, a designator of fixed size on the stack frame, and then allocate
	space for the array data separately.
-   Dope vector contains
	-   Name, type of subscript, bounds, type of elements, number of bytes
		in each element, point to first storage location of array
	-   Allows calculation of actual address of an array element from these
		values.

##### Universal Indirection

-   C++: 

		struct point{int x, int y} center;

-   Java:

		Point center = new Point(0, 0);

-   Extra indirection allows 

		Shape s = new Square (2);

-   But costs:
	-   Extra cost of heap allocation
	-   Boxing and unboxing

-   This is why ints, floats, chars, are not objects in Java.

##### Strong typing

-   Type errors caught as type errors
	-   Rather than "bus error" or just garbage out

-   Prevents certain "efficient" techniques
	-   Union record types
	-   Casting void* pointers

-   Efficient in what?
-   Modern languages avoid need for unsafe operations
	-   Checking casting of references

##### Explicit types

-   Allow many type errors to be caught by compiler
-   Require programmer to enter types
	-   But if problem well-understood and large, probably should
		have pre-planned this information anyway.

-   Prevent some convenient program methods
	-   Lists of non-homogenous types of elements
	-   Modern languages reduce need for these methods

#### Type rules

	E e1: integer E e2:integer
	--------------------------
	E (e1 + e2):integer

-   If both operands of `+` are integers, the result is an integer
-   E is a *type-environment* that maps constant and variables to their
	types.

### Scripting and Dynamic Langues

-   Examples of scripting languages
	-   Python, Ruby, Perl

-   Goals
	-   Rapid prototyping
	-   Easy implementation of simple programs
	-   Pasting together existing programs

#### History

-   Unix approach: combine simple programs
-   EG: To find largest files

		du -a /Applications/Racket* | sort -nr -k1

-   Need automation, shell scripts
	-   Eg post-slides-314

-   Note interface on a pipe is a stream of chars
	-   Normally a stream of lines, sort sorts lines

-   Data as stream of lines, line as array of fields, awk

#### Awk

-   Awk program: sequence of statements
	
		Line-selection {action}

-   Line selector: one or two regular expressions or boolean expr or BEGIN
	or END
-   Action: assign, functions, print, if, ...
-   Variables, arrays with string indices
-   For each line of input
	
		for each line of the program
			if selector then do action

##### Examples

-   Average 2nd field when it exists

		NF >= 2 {total += $2; ct+=1}
		END (if (ct>0) print total/ct; else print nothing to average

-   Count of each word

		NR > 0 {ct[$1]++}
		END {for (a in ct) print a, ct[a]}

#### Perl

-   Awk not enough power for anything for anything but smallest programs
	-   Weak handling of user-defined functions and local variables

-   Perl: general programming languages
	-   But with syntax for "do this regexp munge to each line"

-   Perl "just grew" from a personal language
	-   Lots of special global variables, `@ARGS, @_`
	-   Not `@` sign: array. Also `$var` scalar value.
	-   Influenced by shell command langage. 

#### Dynamic Languages

-   E.g. scheme
-   Blur runtime / compile time
-   Interactive read-eval-print loop
-   Data has a type, variable does not
-   Built in syntax for I/O of lists, arrays, etc.
-   Good for rapid prototyping
-   Provides manual access to a body of code, R, Matlab

#### Newer Scripting Languages

-   Python, Ruby
	-   Web scripting languages (Javascript, PHP, ASP) are something
		different

-   Dynamic
-   Scripting
	-   Facilities to handle processes, files
	-   Facilities to handle file as list of lines
	-   Regular expressions
	-   Embeddable, extensible
	-   High-level data structures

-   Extensive libraries
	-   Standard central repository on the web

-   Still started as personal languages but by people with
	exposure to more modern languages.

### Python

-   Indentation instead of `{}`

		while j < 5:
			k = 0
			while k < j:
				print k + j, ' ',

			print '\n'

		print 'Done'

#### Data Sequence Types

-   Sequence types: strings, lists, tuples
	-   Indices start 0, like Java
	-   Slice: like Java substring

			a = 'help'
			a[0:2] is 'he'
			a[2:] is 'lp', so is a[2:4] and a[2:20]
			len( a[2:4] ) is 2

-   Iteration over sequences

		for b in a:
			print b

#### Lists

-   List

		[2, 3.1, 'foo']

-   Can slice

		a = [3, 4.5, 'foo']
		a[2:3] is ['foo']
		a[2] is 'foo'

-   Can assign to slice

#### Other data

-   Tuple
	-   Like list but cannot be changed
	-   Use paren(4, 7)

-   Set
	-   No duplicates, no order
	
			set([1, 4, 2, 1]) == set([2, 1, 4]) == true

-   Dictionary
	-   A hash table, a set of key value pairs
	
			a = {'horse':4, 'fish':0}
	
	-   `a['fish']` returns 0
	-   Key must be immutable

#### Tuple Assignment

-   `(x, y) = (0, 1)`
	-   Sets `x` to `o` and `y` to `1`

-   `(x, y) = (y, x)`
	-   Swaps `x` and `y` valyes
	-   Evaluate both `y` and `x` first, then do assignment

#### Conditionals

	if a<0:
		print 'negative'
	elif a==0:
		print 'zero'
	else:
		print 'positive'

#### Loops

-  while a =1
		
		while a<=n: 
			print a

-   for

		for a in range(1, n, 2):

-   range

		range(start, end, step)

#### Tuple Assignment

-   Tuple assignment works in both function calls and for loops

		def foo( (x,y), z) 
			print x
			print z 

		a = (1, 2)
		foo(a, 3)

		$ 1 
		$ 3

#### Break and Else <small>for loops</small>


	for n in range(len(lst)): 
		if lst[n]==0:
			print n
			break
		else:
			print 'not ' + ('%i' % n)
	
	else:
		print 'none' 

	print 'done'

#### Filer, Map, and Reduce

-   filter(fn, list)

		filter(lambda n: n+1 !=5, [3, 4, 6])
		returns [3, 6]

-   map(fn, list)

		map(lambda n: n+1, [3, 4, 6])
		returns [4, 5, 7]

-    reduce(fn, list)

		reduce(lambda x, y: x+y, [3, 2, 1])
		returns 6

#### List Comprehensions

-   [ <expression> for <var> in <list> ] 
-   [n*n for n in [3, 4, 6] if n+1 != 5]
	-   returns [9, 36]

-   Like a combination of map and filter, may be more readable
-   Multiple fors: leftmost = outer loop
	-   [(x,y) for x in [2,3,4] if x>2 for y in [5, 6] if x*y!=20] 
	-   returns [(3, 5), (3, 6), (4, 6)]

#### Objects

-   Everything is an object
-   See `objects.py`
-   Any object can have a new field, that is "attribute," added to it.

#### Duck Typing

> If it waddles like a duck, quacks like a duck, and looks like a duck
> it is a duck.

-   Can you do operation O on data D?
	-   Try it at run time and see if it raises and exception.

-   Cf.Java: ensure at compile time that object is of type T and that any
	any object of type T can handle message with name O.

### Scope

-   The scope of a variable is the part of the program that can refer to
	that variable.
-   It's purpose is to limit the number of name "in use" at any one point.
	-   To limit the number of names the programmer has to remember to 
		avoid.
	-   To limit the region in the program where a bug can change a variable
		name.

#### Nested Scope

-   As in Scheme, also Algol, Pascal
-   Assumes languages already has nested constructs life nested if, nested
	loops, etc.
-   Some constructs create new variables and functions
	-   Loop variables
	-   Scope of a new name is the construct
	-   Except where shadowed

Advantages | Disadvantages
-----------|--------------
Simple | The struct isn't uniform
Uniform | Functions
Recursive | files
Elegant | 
Varied size scope | 

### Parameters

#### Association

-   Positional association
	-   Arguments associated with formals one-by-one
		-   C, Pascal, Scheme, Java

-   Keyword association
	-   Ada uses a mixtures

#### Passing Modes

-   Pass by value
	-   C, Pascal, Ada, Scheme, Algol68

-   Pass by result
	-   Ada

-   Pass by value result
	-   Fortran, sometimes Ada

-   Pass by reference
	-   Fortran, Pascal var params, sometimes Cobol

-   Pass by name (outmoded)
	-   Algol60

##### Pass by Value

	c: array [1..10] of integer; 
	m,n : integer;
	procedure r (k, j : integer) 
	begin
		k := k+1;
		j := j+2; 
	end r;
	...
	m := 5;
	n := 3; r(m,n); 
	write m,n;

> Output: `5 3`

-   Advantages
	-   Argument protected from changes in callee

-   Disadvantages
	-   Copying of values takes executing time and space,
		especially for aggregate values.

##### Pass by Result

	c: array [1..10] of integer; 
	m,n : integer;
	procedure r (k, j : integer) 
	begin
		k := k+1;
		j := j+2; 
	end r;
	...
	m := 5;
	n := 3; 
	r(m,n); 
	write m,n;

> Output: `6 5`

-   Assume we have `procedure P(k, j : int)` with `k` and `j`
	as result parameters. What is the interpretation of `p(m,m)`?
	-   Assume parameter `k` has value 2 and `j` has value 3 at end of `p`.
		-   What value is `m` on return?

##### Pass by Value-Result

	c: array [1..10] of integer; 
	m,n : integer;
	procedure r (k,j : integer) 
	begin
		k := k+1;
		j := j+2; 
	end r;
	...
	m := 5;
	n := 3; 
	r(m,n); 
	write m,n;

> Output: `6 5`

##### Comparisons

-   Value-result
	-   Has all the advantages and disadvantages of value and result
		together

-   Reference
	-   Advantage: more efficient than copying
	-   Disadvantage: aliasing - when there are two or more different names
		for the same storage location
		-   Side effect not visible from code itself.

### Parameter Passing <small>v2</small>

#### Terms

Function definition

:   Where the details of the function are presented.

Function call

:   Where the function is invoked.

Parameters

:   Names of local variables in function that are given during
	call.

Local variables

:   Variables in function that are given values during call.

Arguments

:   Values provided for parameters.

Parameter passing

:   Methods used to determine how argument values relate to parameters.

Overloading

:   When thje same function name can have one or more set of parameters

L-value

:   Location of the variable

R-value

:   Contents of the variable (or result of the expression)

#### Call by Value

-   Calling mechanism
	-   Arguments are evaluated for their values
	-   Local variables created for each parameter
	-   Values resulting from arguments copied to new parameter variables
	-   When function call ends, parameter variables are discarded

-   During function execution, value of parameters may diverge from argument
	values (function does not affect arguments)
-   Call by Value used in
	-   C
	-   Most C++ paremeters

-   Variables are change in functions only indirectly
	-   Point values are passed to functions
	-   Variables that the point point at may be changed in a function

-   Characteristics:
	-   Variables may not directly be changed in function body
	-   Arguments can be complex expressions
	-   Mechanism is simple (easy to explain)

-   Example

		int x = 1;

		void func1 (int a) {
			// Location 2
			x = 2;
			// Location 3
			a = 5;
			// Location 4
		}

		void main () {
			// Location 1
			funct1(x);
			// Location 5
		}

	Location | `a =?` | `x =?`
	---------|--------|--------
	1 | undefined | 1
	2 | 1 | 1
	3 | 1 | 2
	4 | 5 | 2
	5 | undefined | 2

#### Call by Reference

-   Calling mechanism
	-   Variables locations for arguments determined
	-   Parameter names added to the location for each argument
	-   When function call ends, extra names are discarded

-   During function call, changes to referenced variables persist
	even after function ends.
-   Call by Reference used
	-   Pascal
	-   C++ (& parameters)
	-   Some version of FORTRAN

-   Characteristics:
	-   Changed to parameters change corresponding argument variables
	-   Arguments must be variables

-   Example 

		int x = 1;

		void func1 (int a) {
			// Location 2
			x = 2;
			// Location 3
			a = 5;
			// Location 4
		}

		void main () {
			// Location 1
			funct1(x);
			// Location 5
		}

	Location | `a =?` | `x =?`
	---------|--------|--------
	1 | undefined | 1
	2 | 1 | 1
	3 | 2 | 2
	4 | 5 | 5
	5 | undefined | 5

#### Call by Value-Result

-   Calling mechanism
	-   Arguments are evaluated for their values
	-   Local variables created for each parameter
	-   Values resulting from arguments coped to new parameter variables
	-   When function call ends, values from parameters copied back to
		calling variables

-   Operates like Call by Reference but differs under certain circumstances
-   Used in some versions of FORTRAIN, inout param in CORBA
-   Example

		int x = 1; // global x		
		void func1 (int a) {			// Location 2			a = 3;			// Location 3			x = 4;			// Location 4		}		void main () {			// Location 1			func1(x);			// Location 5		}

	Location | `a =?` | `x =?`
	---------|--------|--------
	1 | undefined | 1 
	2 | 1 | 1 
	3 | 3 | 2 
	4 | 3 | 4 
	5 | undefined | 3

December 15th, 2013 <small>Practice Final Exam</small>
------------------------------------------------------

### Question 1

Each of the following, involves a language over the four characters 
a, b, c, and d. For each one either give a Regular Expression that 
generates the language or explain why this is impossible:

1.  L = The set of strings that start with three or more a’s followed 	by any number (including 0) of a’s and b’s.

		(aaa)(a|b*)

2.  L = The set of strings in which every ‘a’ is followed immediately 
	by a ‘b’ and every ‘b’ is immediately preceded by an ‘a’., and 
	similarly for ‘c’ and ‘d’. In other words, the strings must be 
	made up of combinations of ab and cd. E.g., ‘abcdab’ is in L but 
	‘abccd’ is not.

		((ab)|(cd))*

### Question 2

Consider the following FSA:

![Finite State Automata Diagram](../img/cs-pl-final-fsa.png)

1.  Is this a deterministic or non-deterministic FSA? Why?
	-   A non-deterministic FSA has at least one state which has two
		arrows with the same label or an epsilon transisition.
	-   So this one is deterministic.

2.  Write a regular expression that specifies the same language 
	that this FSA accepts.

		(b|m)(a)((d|n)(x))*

3.  Complete the following grammar for the language this FSA accepts:

		S      -> PREFIX | PREFIX TAIL
		PREFIX -> BORM a

	1.  `BORM -> b | m`
	2.  `TAIL -> NORD x | NORD x TAIL`
	3.  `NORD -> n | d`

### Question 3

In the following Scheme function, `num-list` is a list of numbers and threshold 
is a single number. The function `list-greater` returns a `list` equal in length 
to `num-list` but with each number replaced by either `#t` or `#f`, depending 
on whether the number is or is not greater than threshold. E.g., 
`(list-greater '(2 5 3 6) 4))` should return `(#f #t #f #t)`. Finish the 
definition below. You must use `map`[^map].

	(define (list-greater num-list threshold)
		(map (lambda(x)(x > threshold)) num-list)
	)

### Question 4

The following Scheme code defines `sumsqtr`, a function that takes a
list of numbers as its argument and returns the sum of the squares of 
those numbers. Eg `(sumsqtr '(1 4))` returns `17`. 
`Sumsqtr` and its helper function `sumsqtrh` are tail recursive. 
Fill in the blanks.

	(define (sumsqtr lst)
		(sumsqtrh lst 0))
	(define (sumsqtrh lst accum)
		(if (null? lst) accum
			(sumsqtrh (crd lst)
						(+ accum (* car let)(car list)))
		))

### Question 5

1.  `inOrder(List)`. Assume List is a list of numbers; 
	`inOrder(List)` is true if and only if the numbers in List 
	are in increasing order. If List has `0` or `1` element it is 
	in order.

		inOrder( [] ).
		inOrder( [_] ).
		inOrder([N1, N2 | T]) :- N1 < N2, inOrder[N2 | T]

2.  Suppose a graph is represented as a list of node structures like 
	`node(a, 3, [b, c])` where a is the node's name, 3 is its color, 
	and `[b, c]` is a list of its neighbors' names. The 
	predicate `allNames(Graph, Names)` assumes `Graph` is a graph and 
	binds `Names` to a list of all the names of nodes in the graph 
	(just the names, not the node(...) structures).

		allNames( ??? , ??? ).
		allNames( ??? , ??? ) :- ??? .

### Question 6

Given the rules

	suffix([H | T], T).
	suffix([H | T], T1):- suffix( T, T1 ).

1.  What would be the first result of the query `suffix([a, b, c], S)`?
2.  What would be the second result of the query, if the user 
	typed ‘;’ after the first result?

### Question 7

	int a;

	procedure foo(int x) {
		x = x + 10;
		a = a + x;
	}

	procedure fie( ) {
		a = 5;
		foo(a);
		print (a);
	}

For each of the following parameter passing methods, show what would be 
printed by a call to fie.

1. Call by value
2. Call by value-result
3. Call by reference

### Question 8

For each of the following language features, circle “functional” if having 
the feature makes a language more of a functional language and “not” if it 
does not:

Feature | Functional? | Why?
--------|-------------|-----
closures | Yes | They're little functions.
arrays | No | They're not functions.
dynamic types | No | Probably not functions.
garbage collection | Yes | Lets you just do functions.
linked-lists are a built-in data type | No | Not functions.

### Question 9

Given the declarations below:

	int: size, size2, j;
	float: x;
	array[1:30] of int: nums;

For the assignment statements below, circle the ones that cannot be 
fully type- checked at compile time. Assume that an array’s subscript 
range is considered part of its type. Assume that numeric overflow and 
is not considered a type-error.

1.  size = size2 + 1;
2.  x = size;
3.  nums[j]=33;
4.  nums[3] = nums[4];
5.  nums[j] = nums[j+1]

### Question 10

The following python function takes a list of numbers as its argument 
and returns a list of the squares of those numbers. Finish it.

	def listSq(lst):

*[FSA]: Finite State Automaton

[^map]: How does map work? It transforms a list by applying a 
function to each of its members. Furthermore, it returns the
transformed list. Map takes a function and then a list.

		elements(map (lambda (x) (* x 2)) numbers)