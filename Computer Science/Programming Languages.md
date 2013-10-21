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
    -   unification, generate and test;\
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

**The textbook does not cover all of the material for this course, and
is not a substitute for attending class.**

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

    3.  `(ab)*`

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

October 15th, 2013 <small>Midterm Study Guide</small>
-----------------------------------------------------

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
    2.  Allow $\epsilon$ transition
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

-   shallow and deep recursion on lists\
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
            least one $\epsilon$ or multiple state transitions (multiple
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

2.  Suppose a language had logical expressions using the operators \^
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


