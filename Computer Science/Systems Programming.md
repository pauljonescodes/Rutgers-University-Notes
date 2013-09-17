Systems Programming <small>with Professor Brian Russel</small>
==============================================================

Description
-----------

This course teaches students how to think about, build, debug, and test
large computer programs. The course stresses learning how to use tools
such as debuggers, profilers, source version control systems, and
integrated development environments as an essential part of developing
large programs. The course also stresses the understanding of how
programs execute on today's computers and how to measure and optimize
performance. Programming will be in C on Unix systems to introduce
students to a new programming eco system, as well as enable the mapping
of high-level language constructs to the underlying machine.

### Topics

Systems programming in C and Unix: C programming Memory management and
the C memory model System calls I/O Caching Multi-threaded programming
Shell scripts

Software development: Performance (space and time) analysis and
measurement Debugging Testing Performance optimization

Tools: IDE (e.g., Eclipse) Source version control (e.g., CVS) Debugger
(e.g., gdb) Memory errors (e.g., valgrind) Profiling (e.g., gprof,
valgrind)

### Expected Work

Large programming project spread across several parts

### Department Learning Goals:

Computer Science majors ...

will be prepared to contribute to a rapidly changing field by acquiring
a thorough grounding in the core principles and foundations of computer
science (e.g., techniques of program design, creation, and testing; key
aspects of computer hardware; algorithmic principles). will acquire a
deeper understanding on (elective) topics of more specialized interest,
and be able to critically review, assess, and communicate current
developments in the field. will be prepared for the next step in their
careers, for example, by having done a research project (for those
headed to graduate school), a programming project (for those going into
the software industry), or some sort of business plan (for those going
into startups).

Syllabus
--------

### Instructor

Brian Russell <morbius@cs.rutgers.edu>    Office Hours: Wednesdays
8:00-9:00 pm, Hill 403.

### TAs

Ying Zhan <yz280@cs.rutgers.edu>    Office Hours: Tuesdays 10:00-11:00
am Hill 418

Sejong Yoon <sjyoon@cs.rutgers.edu>    Office Hours: Wednesdays
2:00-3:00 pm CBIM cubicle 1

Yuanzhen Gu <yg185@cs.rutgers.edu>    Office Hours: Mondays 10:00-11:00
am Hill 418

Zi Yan <zy56@cs.rutgers.edu>    Office Hours: Thursdays 1:00 pm 2:00 pm
Hill 405

### Objective

The aim of CS214 is to introduce the student to the process of writing
low-level programs that interact directly with a computer's operating
system and hardware, as well as to develop the student's ability to
build large applications in a team environment. Upon completion of this
course, the successful student should be able to design, write, test,
and analyze moderately complicated programs using the C programming
language and UNIX/Linux operating systems.

### Prerequisite Knowledge

Structured programming in a high-level language (such as Java). Standard
data structures (lists, trees, graphs, hash tables).

### Textbook

The following texts are available online, free of charge.

*C Programming* *The C Book* Mike Banahan, Declan Brady and Mark Doran

The textbooks do not cover all material discussed in class, and are not
a substitute for attending lectures.

### Topics Covered in CS214

The following list is organized by topic, not by chronological order of
coverage in the course.

1.  Programming in C

    Basic syntax, standard I/O, data manipulation, flow control Pointer
    manipulation, dynamic memory management Error handling and debugging

2.  Programming under UNIX

    Advanced debugging (gdb) Performance profiling (gprof) File I/O
    Signal handling Scripting

3.  Large-scale development

    Modules, headers, linking, makefiles Version control

4.  Concurrent programming

    Process creation and communication Multithreaded programming,
    synchronization

5.  (optional) Embedded systems programming

    Developing an embedded application

### Lecture Schedule

1.  Sept 04 Into to C
2.  Sept 06 C program structure, C functions
3.  Sept 11 C preprocessor, formatted I/O
4.  Sept 13 Dynamic memory management
5.  Sept 18 Data Structure design
6.  Sept 20 File I/O
7.  Sept 25 multi-file projects, makefiles, directory I/O
8.  Sept 27 gdb
9.  Oct 02 libraries
10. Oct 04 signals and event-based programming
11. Oct 09 signals and processes
12. Oct 11 valgrind and memory-related bugs
13. Oct 16 caching
14. Oct 18 version control, CVS
15. Oct 23 Threads
16. Oct 25 Thread synchonization (mutex locks, semaphores)
17. Oct 30 Thread synchronization (condition variables), thread patterns
18. Nov 01 Thread patterns
19. Nov 06 signals and threads
20. Nov 08 midterm
21. Nov 13 UNIX/Linux commands, BASH shell
22. Nov 15 BASH shell scripting
23. Nov 20 regular expressions, grep, awk, sed, tr
24. Nov 27 more shell scripting
25. Nov 29 more shell scripting
26. Dec 04 still more shell scripting
27. Dec 06 Event-driven architectures
28. Dec 12 Review

This schedule may change as needed.

### Expected Work

Students are expected to attend all lectures and perform all reading
assignments prior to lecture. Students are also expected to attend all
recitation section meetings. Students will be evaluated according to
their performance on a semester long programming project, a mid-term
examination, and a final examination.

### Project

WARNING: This is a project course, which means that this course should
give you more than a passing knowledge of what writing working network
programs entails. The project will be a major undertaking. If you
complete the projects, you will have learned a lot. However, assess your
commitment to this course realistically. If you don't have the time or
the inclination to work hard on the project, you would be better off not
taking the course. You will have to learn how to build and debug
reasonably sized C programs and make them robust to outside errors. You
will also have to describe how your program work in a written document.

This one large project will be assigned, as three sub-projects. Up to 2
students can work as a group for each sub-project and you can change
group members for each project . Students are required to complete the
parts by the scheduled deadlines. Failure to turn in the project by the
deadline using the electronic handin website will result in a zero for
all team members. No exceptions!

There are many different operating systems and variants of C out there
and we cannot test your program on all of them. So all program
assignments must run on the local iLab Linux machines. We will be
grading your assignments on those machines as well.

### Working Together and Academic Honesty

Cheating on projects and exams will not be tolerated. We want to protect
the fairness and integrity of the class, so we run code similarity
detectors on the projects and scrutinize exams for copying. Both parties
in the exchange are liable; e.g. if you give away solutions to friends,
you're putting yourself at risk too. If you get caught, it's a nasty
process--just don't go there! You're better off asking for help, or at
worst, dropping the course and trying it again. The department academic
integrity policy can be found at
http://www.cs.rutgers.edu/policies/academicintegrity/. You now need to
click explicitly on a link when first login to our computing facilities,
use handin, etc., that says you acknowledge being aware of the policy
(which you can read through the login screen). If you fail to do the
click-through by the end of September, your access to our facilities
will cease October 1.

### Grading

Midterm: 20 % Final: 30 % Project: 50%

The programming part of the projects are typically graded on how close
they are to the functional requirements. The written portion is graded
on how well the TAs can figure out how your project is constructed only
from the written description. Exams are typically graded on a curve. As
a rule of thumb, the mean is a "C'" and each standard deviation is one
letter grade. This rule can be altered, however, if the class does
exceptionally well or poorly.

I felt we should do our best to clarify up front how we grade your
programming assignments. The TAs do the grading, but have all agreed to
the same criteria for grading each programming assignment. Each
programming assignment is worth 100 points. here are our grading
criteria:

40% Correctness Percent based on number of test cases

40% Code Quality 20% Algorithmic 10% Reusability/Modularity 10%
Decomposition

20% Documentation 10% Test Cases from Students 5% Comments 5%
Documentation (Analysis, readme files, etc...)

### The Gilligan's Island Rule

We do encourage you to talk to your classmates, provided you follow the
Gilligan's Island Rule. After a joint discussion of an assignment or
problem, each student should discard all written material and then go do
something mind-numbing for half an hour. For example, go watch an
episode of Gilligan's Island (or jersey Shore in modern terms), and then
recreate the solutions. The idea of this policy is to ensure that you
fully understand the solutions or ideas that the group came up with. If
you follow the Gilligan's island rule, often best route to follow to get
a question answered is to ask, in order: 1. A classmate smarter than
you. 2. Your TA. 3. The professor.

September 5th, 2013 <small>Lecture on C program structure, C functions</small>
------------------------------------------------------------------------------

### General Syntax

    struct point {
        int x,
        int y,
    } a, b, c; // three variables

    a.x = 3;
    b.y = 42; // accesing them

    struct rectangle {
        struct point top_left;
        struct point top_right;
    } d, *p;

    d.top_left.x = 30;
    p = &d;
    p->top_left.y = 40;

    struct rectangle box = {{0, 5}, {5, 6}};

    union f {
        int int_part;
        char char_part[sizeof(int)];
    }

    int array[10];

    char string_array[] = "hello";

    int square[10][10] = {{0, 1, 2, 3, 4, 5}, 
                          {6, 7, 8, 9, 10,11}};
                          
    switch (expression) {
        case constant_expression_1:
            statements;
        case constant_expression_2:
            statements;
        case default: 
            statements;
    }
      

A string is a series of characters, and array, followed by a null byte.
Before there were no classes, there were structs. No visibility classes.
No message passing, methods.

### Pointers

    int x;
    int *px;

    int y, *py;

    px = &x; 

    int *p1, *p2;

    p1 = 0;
    p2 = p1;

    char * s = "hello";

    struct point * p, point_var;

    p = &point;
    p->x = p->y = 0;     // these are 
    (*p).x = (*p).y = 0; // equivalent

    char array[] = "hi there";
    char * p_char;

    p_char = array; 
    * p_char = 'z'; // these are
    p[0] = 'z';     // equivalent

    struct point * pp, point[10];

    pp = point;
    pp *= 1;

A pointer variable contains an address. If I say "pointer to" and
"address of", it's equivalent.

Subscripts can be positive, negative, and zero. When you use arrays in
C, there is no array bounds checking. If you have a ten element array, C
does not mind if you just meander in either direction.

### Pointers to Functions

    int f(int);     // defined but not implemented function

    int (*pf)(int); // pointer to a function, parentheses necessary
                    // returns an int
                    
    int g(int);
    int f(int);
    int x;

    x = f(3);
    pf = f;
    x = (*pf)(3);
    pf = g;

September 18th, 2013 <small>Programming Assignment 1: Tokenizer</small>
-----------------------------------------------------------------------

### Introduction

In this assignment, you will practice programming with C pointers. Much
of the pointer manipulation will come in the form of operating on C
strings, although you will be dealing with some pointers to structs as
well.

Your task is to write a type and a set of functions in essence, the
equivalent of a Java class that implements a tokenizer. The tokenizer
should accept two strings, the first of which will contain a set of
*separator characters* while the second will contain a set of terms
separated by one or more separator characters. The tokenizer should
return the *terms* in the second string one at a time, each term is
called a token, hence your program is called a tokenizer. For example,
when given the following two strings:

    " ", "today is a beautiful day"

your tokenizer should return:

    "today", "is", "a", "beautiful", and "day"

When given the following two strings:

    "/?", "/usr/local/?/bin/? share"

your tokenizer should return:

    "usr", "local", "bin", and " share"

A string is a sequence of characters delimeted by double quotes (").
Strings can contain newline or double-quote characters, but special
syntax is required to contain them and certain other characters. These
special characters are represented with escape sequences:

    newline \n 
    horizontal tab \t 
    vertical tab \v 
    backspace \b 
    carriage return \r 
    form feed \f 
    audible alert \a 
    backslash \\
    question mark \? 
    single quote \′ 
    double quote \” 
    octal number \000 
    hex number \xhh

### Implementation

Your implementation needs to export the interface given in the attached
tokenizer.c file. In particular, you need to define the type needed to
represent a tokenizer and three functions for creating and destroying
tokenizer objects and getting the next token. Note that we have only
defined the minimal interface needed for external code (e.g., our
testing code) to use your tokenizer. You will likely need to design and
implement additional types and functions.

A token is a sequence of any ASCII character that does not contain a
separator character. Separator characters are provided as a string of
one or more ASCII characters. Each pair of tokens are separated by one
or more separator characters. Multiple separators may be next to each
other (see second example above), and/or at the beginning and/or end of
the term string. When this happens, your tokenizer should discard all
separators.

Your implementation must not modify the two original strings in any way.
Further, your implementation must return each token as a C string in a
character array of the exact right length. For example, the token usr
should be returned in a character array with 4 elements (the last holds
the character ’\0’ to signify the end of a C string).

You may use string functions from the standard C library accessible
through string.h (e.g, strlen()). However, you may not use strtok(),
strsep() or any similar function that already performs the complete
tokenization process.

You should also implement a main() function that takes 2 string
arguments, as defined above. Each character in the first string is a
separator. The second string contains zero or more tokens separated by
separator characters. Your main() function should print out all the
tokens in the second string in left-to-right order. Each token should be
printed on a separate line. Here is an example invocation of the
tokenizer and its output.

    tokenizer ” ” ”today is sunny” today
    is
    sunny

Keep in mind that coding style will affect your grade. Your code should
be well-organized, well- commented, and designed in a modular fashion.
In particular, you should design reusable functions and structures, and
minimize code duplication. You should always check for errors. For
example, you should always check that your program was invoked with the
minimal number of arguments needed.

Your code should compile correctly (no warnings and errors) with the
-Wall and either the -g or -O flags. For example

                      gcc -Wall -g -o tokenizer tokenizer.c
                     

should compile your code to a debug-able executable named tokenizer
without producing any warnings or error messages. (Note that -O and -o
are different flags.)

Your code should also be efficient in both space and time. When there
are tradeoffs to be made, you need to explain what you chose to do and
why.

**IMPORTANT NOTE**: You may write your code on any machine and operating
system you desire, but the code you turn in MUST tar (see below),
compile and execute on the iLab machines or a zero grade will be given.
Be sure to compile and execute your code on an Ilab machine before
handing it in.

### What to turn in

A tarred gzipped file named pa1.tgz that contains a directory called pa1
with the following files in it: - A tokenizer.c file containing all of
your code. - A file called testcases.txt that contains a thorough set of
test cases for your code, including inputs and expected outputs. - A
readme.pdf file that contains a brief description of the program and any
great features you want us to notice. Suppose that you have a directory
called pa1 in your account (on the iLab machine(s)), containing the
above required files. Here is how you create the required tar file. (The
ls commands are just to help show you where you should be in relation to
pa1. The only necessary command is the tar command.) ls pa1 ls pa1
Makefile readme.pdf testcases.txt tokenizer.c tar cfz pa1.tgz pa1

You can check your pa1.tgz by either untarring it or running tar tfz
pa1.tgz (see man tar). Your grade will be based on: - Correctness (how
well your code works). - Quality of your design (did you use reasonable
algorithms). - Quality of your code (how well written your code is,
including modularity and comments). - Efficiency (of your
implementation). - Testing thoroughness (quality of your test cases).

September 10th, 2013 <small>Lecture</small>
-------------------------------------------

    int gcd(int a, int b) {
        if (b == 0) { 
            return a;
        } else {
            return gcd(b, a % b);
        }
    }
    
-   What you want to take from this is that it's pass by
    value.
    -   The function can change the copies.
    -   Cannot change the original values.
    
