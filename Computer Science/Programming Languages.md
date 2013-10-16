Principle of Programming Languages <small>with Professor Louis Steinberg</small>
================================================================================

Description
-----------

The course is aimed at making the student familiar with the general concepts common to all programming languages so as to facilitate learning new languages.  Language paradigms (i.e., logic, functional, procedural, object-oriented) are compared and implementation strategies are discussed.

-   Credits: 4
-   Prerequisites:
    -   14:332:331 or 01:198:211; 
    -   01:198:205 or 14:332:312.

-   Please note that courses for which a student has received a grade of D cannot be used to satisfy prerequisite requirements.
-   Semesters Offered: Spring and fall

### Topics

-   BNF and context free grammars; Data visibility (i.e., lexical and dynamic scoping); 
-   Procedures and  parameter passing techniques; 
-   Types, type checking and type equivalence; 
-   Functional programming paradigm:
    -   higher-order functions, 
    -   recursive data structures, 
    -   programming with recursion (i.e., without iteration);  

-   Logic programming paradigm:  
    -   unification, generate and test;  
    -   Programming with pointers in C.

### Expected Work

There are three graded programming projects and textbook homework assignments.

-   Exams:
    -   1 hourly, Final Exam

### Department Learning Goals

-   Computer Science majors ...
    -   will be prepared to contribute to a rapidly changing field by acquiring a thorough grounding in the core principles and foundations of computer science (e.g., techniques of program design, creation, and testing; key aspects of computer hardware; algorithmic principles).
    -   will acquire a deeper understanding on (elective) topics of more specialized interest, and be able to critically review, assess, and communicate current developments in the field.
    -   will be prepared for the next step in their careers, for example, by having done a research project (for those headed to graduate school), a programming project (for those going into the software industry), or some sort of business plan (for those going into startups).

Syllabus
--------

### Objective

-   Primary objective: Learn new ways of thinking about problems and programs.
-   Secondary objective: Make it easier to learn new languages by learning principles that apply to many languages.
-   Tertiary objective: Learn some interesting languages.

### Prerequisite

-   CS 205, CS 211
-   Java; the memory model of C, including pointers; predicate calculus

### Book

-   Michael L. Scott, Programming Language Pragmatics, 3rd Edition. Morgan Kaufman

**The textbook does not cover all of the material for this course, 
and is not a substitute for attending class.**

### Work

-   You are expected to attend all lectures and recitations, in both body and mind. That is, please do not access Facebook, games, email, or the like during class.
-   There will be two midterms exams and a final, as well as graded programing projects and ungraded exercises. The projects only count for a small part of your grade directly, because there is no way to be sure that they are really your own work. However, they count for a large part of your grade indirectly. If you do not do the exercises and projects you will not learn the material. Furthermore, there will be exam questions directly based on the projects and exercises.

### Tentative Grading

Your course grade is based on projects and exams, with the following tentative weighting:

-   Projects (all together): 10%
-   Midterm 1: 25%
-   Midterm 2: 25%
-   Final exam: 40%

### Course grades

Your course grade will be computed as follows: Each score (for each exam and each project) will be converted to a percentage score, and the percentages will be added, with weights as above. Cutoffs for letter grades are:

-   A: 90%
-   B+: 85%
-   B: 80%
-   C+: 75%
-   C: 70%
-   D: 60%

### Grading disputes

If you feel an exam or a project has been misgraded, you must bring it to our attention within 2 weeks of when we first give back the graded exam or project.

### Collaboration

All students in this class are expected to be familiar with the The DCS academic integrity policy, which can be found at http://www.cs.rutgers.edu/policies/academicintegrity/ , and to abide by it.

We do encourage you to us the Piazza site to discuss the concepts behind course material and assignments, but please do not post code. If you need help with code, email it to the professor or a TA.

### Exams

Exam schedules and rules are in Resources > Exam info. You are expected to know and to abide by these rules.

### Poor grades

If you get less than 70% on an exam please contact the 314 TA's or instructor immediately. Often students wait until after the final, and then ask how they can raise their grade. At that point there is no way to raise their grade. The earlier you contact us the more chance we can be of help.

### Topics

The following list is organized by topic, not by chronological order of coverage in the course.

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
            1. `SS`
            2. `AA`
            3. `CC`
            4. `ab`

2.  Rewrite the grammar `G` above so that no string in its language is
    ambiguous. Make # have higher precedence than `@` and make both `#`
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
    
        `L(G')` contains a series of `x`s followed by a series
        of `y`s, each with at least one `x` or `y` followed by
        potentially infinite `x`s or `y`s.

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

6.  Describe in English the language accepted by this DFSA:
    `S1` is the start state and only `S2` is an accepting state.
    
    A series of zeroes and ones with at least a single one and
    possibly no zeroes. 

7.  Describe in English the language of each of the following RE's:
    1.  `ab*c*` 
        -   This is a series `b`s preceded by an `a`, followed by
            any number of `c`s.
        
	2.  `a*|b*` 
	   -   Any number of `a`s followed by any number of `b`s.
	
	3.  `(ab)*`
	   -   A possibly empty series of repeating `ab`.

September 23rd, 2013 <small>Assignment 2</small>
------------------------------------------------


1.  View the video: https://www.youtube.com/watch?v=prAwkQt3ARg
2.  Answer these questions:
    1.  What is the main point the speaker is trying to make
    2.  List two examples the speaker uses and explain for each
        how it supports his point, or, if you think that it does not, 
        why not.
        
October 3rd, 2013 <small>Exercise 4: Scheme</small>
---------------------------------------------------

For these problems, you must use pure functional scheme. That is:
You may not use a functions like set! whose name ends with '!'.
You may not use for or while loops or do loops. All repetition must be via explicit recursion or the recursion implicit in map or similar functions. (You can do problems 1 – 3 before we cover map in class.)
You may, however, use define – in fact you must use it.
You may use any implementation of scheme that complies with the R5RS standard.
 
1. Write the function echo. This function doubles each top-level element of it argument. E.g., (echo '(a b c)) returns (a a b b c c). (echo '(a (b c))) returns (a a (b c) (b c))
2. Write the function nth. (nth i lst) returns the ith element of lst. E.g., (nth 0 '(a b c)) returns a, (nth 1 '(a b c)) returns b. You may assume that 0 ≤ i < (length lst).
3. Write the function deep-reverse, which reverses its argument at all levels. E.g., (deep-reverse '(a (b c) (d))) returns ((d) (c b) a).
4. Write a scheme function (assoc-all lst a-list) where lst is a list of symbols and a-list is an assoc-list. assoc-all returns a list of the data associated with elements of lst by assoc-list. E.g. (assoc-all '(a d c d) '((a apple)(b boy)(c cat)(d dog))) returns (apple dog cat dog). Use map. Note that you can't simply use assoc as one of the arguments to map. You need a lambda.
4. Write a function filter-evens which takes a list of numbers as its argument and returns a new list containing only the even numbers in the input list. E.g., (filter-evens '(23 33 44 2 1 8)) returns (44 2 8). Use even? to test if a number is even. You must use map.  You may use a helper function but the only recursion should be the recursion implicit in map. 
Hint:  Note that the result of map is exactly as long as its second argument.  E.g. the result of  (map foo '(23 33 44 2 1 8)) will be a list of 6 elements no matter what function foo is.  So how can this problem be solvable?  Do something to the result of map before you return it.  E.g., suppose the result of   (map foo '(23 33 44 2 1 8)) is ( ( ) ( ) (44)(2)( ) (8)).  Then (apply append   (map foo '(23 33 44 2 1 8))) will result in (44 2 8) .

October 15th, 2013 <small>Midterm Study Guide</small>
-----------------------------------------------------

### Formal Languages

#### Grammars 

-   parsing, derivation
-   ambiguity and removing ambiguity: precidence, associativity
-   regular grammars and context free grammars

#### Regular Expressions
	
-   is this string in the language defined by this RE?
-   describe in English the language defined by this RE
-   write an RE that defines this language

#### Finite State Automata

-   deterministic and nondeterministic
-   is this string accepted by this FA?
-   describe in English the language accepted by the FA.
-   write an FA that accepts this language


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






