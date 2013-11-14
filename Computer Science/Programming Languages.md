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
    -   A Strucutre can be thought of as either a logical predicate
        or data strucutre.

-   Atoms in Polorg looks like an identifier beignning with a lowercase
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

-   The clauses in a Prolog databse can be classified as *facts* or
    *rules*, each of which ends with a period.
    -   A fact is a horn clause without a right-hand side.

-   A rule has a right hand side:

        snowy(X) :- rainy(X), cold(X).

-   The toke `:-` is the implication symbol.
    -   The comma indicates "and."
    -   Variables that appear in the head of a Horn cluase are
        universally quantified: for all `X`, `X` is snowy is `X` is
        raining and `X` is cold.

-   It is possible to write a clause with an empty left-hand side.
    Such a clause is called a *query* or a *goal*.
    -   Queiries do not appear in Prolog programs.
        -   Rather, one build a databse of facts and rules and then
            initiates execution by giving the Prolog interpreter
            a query to be answered.

-   It most implementation of Prolog, queiries are entere with
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

-   The unfication rules for Prolog state:
    1.  A constant unifies only with itself.
    2.  Two strctures unify if and only if they have the same functor
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

-   The useual arithmetic operators are available in Prolog, but they play
    a role of predicates, not of functions.
    -   Thus, `+(2, 3)`, which may also be written `2 + 3` is a two-
        argument structure, not a functino call.
        -   It will not unifiy with `5`:

                ?- (2 + 3) = 5
                No

-   To handle arithmetic, Prolog procides a built-in predicate, `is`, that
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

#### Search/Excution Order

#### Imperative Control Flow

#### Database Manipulation

### Prolog <small>Basic operation of Prolog</small>

Unification
:   TBD

Backward chaining
:   TBD

Backtracking
:   TBD

### Logical meaning of Prolog

### Prolog programming

Ordering goals & clauses
:   TBD

Cut
:   TBD

Numbers, is
:   TBD

Recursion
:   TBD

Lists
:   TBD

Trees
:   TBD

Graphs
:   TBD

### Practice Exam 2

1.  Finish the definition below of the scheme macro and-not, so that
    (and-not x y) is the equivalent of (and x (not y)). Note that
    and-not should have the same kind of “short cut” behavior as and and
    or have, and as x && y has in Java: if x is false, it should not
    evaluate y, but should just return false. (This is why and-not needs
    to be a macro.)

        (define-syntax and-not          (syntax-rules ( )               ((_ x y) (      )))

2.  Fill in the following prolog predicates.
    1.  `inOrder(List)`. Assume `List` is a list of numbers;
        `inOrder(List)` is true if and only if the numbers in `List` are
        in increasing order. If `List` has `0` or `1` element it is in
        order.

            inOrder( ___ ) .

            inOrder( ____ ) .

            nOrder( [ N1, N2 | T ] ) :- 

    2.  `suffix(L1, L2)`. Assumes `L1` and `L2` are lists. It is true if
        `L2` is a tail of `L1`. E.g., `suffix([x, a, b], [a, b])` is
        true, as is `suffix([x, y, a, b], [a, b])`,
        `suffix([x, y, z, a, b], [a, b])`, and so on.

            suffix( ______ ).           suffix( ______ ):- 

3.  For each of the following pairs of fact and goal, say whether they
    will unify, and if so with which bindings

|Fact|Goal|Unfify?|
|----|----|-------|
|`foo(Bar, baz).`|`foo(baz, Bletch).`|???|
|`foo(a, b)`|`fie(X,Y)`|???|
|`foo(a, fie(Y, X))`|`foo(X, fie(a,a))`|???|

1.  The predicate `odd(All, Odds)` is true if `Odds` and `All` are lists
    and `Odds` contains the 1st, 3rd, 5th, etc, elements of `All` (in
    that order), Hint: `[a, b | c]` is a list whose first two elements
    are `a` and `b`, and whose tail after `b` (i.e. the `cddr`) is c.
    `odds([],[])` is also true. Define `odds`:

2.  What is the translation into predicate calculus of the prolog rule:
    `cousin(X,Y):- grandparent(X, G), grandparent(Y, G), nonsibling(X, Y)`.

3.  What will this print for the query `foo(X, Y).`? (The predicate
    write simply prints its argument.
            foo( 1, 2):-write(12), 1<1.     foo(X, 2):- fie(X), 
            write(x2), 2<1. foo(1,Y):- write(y1).       fie(a):-write(a). 
            fie(b):-write(b).

4.  Define the predicate `insertInOrder(Lst, Num, Res)`, where `Lst` is
    a list of numbers in ascending order and `Res` is the result of
    inserting `Num` in its correct place in `Lst`. E.G.,
    `insertInOrder([1, 3, 6, 9], 5, [1, 3, 5, 6, 9])` is `true`.

5.  Given the following code, what will the query `vacation(A)` print?
    Hint: If the variable `V` has value `a`, `write([fun, V])` prints
    `[fun, a]`. fail is a predicate that always fails.

        vacation(Activity):- 
        fun(Activity), 
        write([fun, Activity]),     cheap(Activity), 
        write([cheap, Activity]), 
        !,      fail.       fun(Activity):- speed(Activity, S), S > 50. 
        fun(Activity):- outdoors(Activity). 
        speed(skiing, 75).      outdoors(skiing).       outdoors(hiking). 
        cheap(hiking).


