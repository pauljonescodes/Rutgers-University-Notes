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
the character ’’ to signify the end of a C string).

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

-   What you want to take from this is that it's pass by value.
    -   The function can change the copies.
    -   Cannot change the original values.

September 30th, 2013 <small>Programming Assignment 2: Sorted List</small>
-------------------------------------------------------------------------

### Introduction

In this assignment, you will practice with more complex data structures,
as well as practice using function pointers (along with using data
pointers as in the last assignment).

Your task is to write a set of types and functions that implement a
sorted list. The sorted list will contain opaque objects. That is, the
objects will be given to you as void\* objects. When a sorted list is
first created, the caller will provide you with a pointer to a
comparator function. This comparator function will understand the actual
type of the objects to be stored in the sorted list, and, given two
objects, will return an ordering of the two objects. Subsequently, when
new objects are inserted into the list, you will use the given
comparator function to insert the new objects such that the list will
remain sorted in descending order; that is, objects are ordered from
largest (front of the list) to smallest (end of the list).

You will also implement an iterator to help users walk through lists.
This iterator, together with returning pointers to your sorted list
objects as void\*, will help you practice implementation hiding. That
is, your implementation is similar to a Java class, where the users do
not know about the implementation and so cannot access parts of the
objects directly. (In C, there are obviously ways to get around your
hiding; nevertheless, it is good programming practice because it
requires effort to violate the hiding.)

### Implementation

Your implementation needs to export the interface given in the attached
sorted-list.h file. Specif- ically, you need to implement four functions
for creating sorted lists, destroying sorted lists, and inserting and
deleting an object into/from a sorted list. Your sorted-list data will
be of the type void, so that you can pass any type into data struct.
Rather, this is a way in C for you to practice a bit of implementation
hiding. When writing your code for the sorted list, you will need to
define a type for your sorted list objects. For example:

    struct SortedList {
            
    };
    typedef struct SortedList* SortedListPtr;

You should create a pointer to struct `SortedList` object in
`SLCreate()`.

    SortedListPtr SLCreate(CompareFuncT cf) {
             SortedListPtr sl;
             ... /* do what is needed to create the sorted list object. */
    return sl; }

The comparator function must obey the following semantics: return -1 if
the 1st object is smaller, 0 if the two objects are equal, and 1 if the
2nd object is smaller. You will also need to define a helper iterator
type together with three functions for creating sorted list iterators,
destroying sorted list iterators, and obtaining the objects in a sorted
list one at a time. In this assignment, the iterator is just a wrapper
around a sorted list that is used to help the caller walk through the
list. Again, data is returned as void\* to hide your implementation.

One complication that you must deal with is what happens if the sorted
list is modified (e.g., a new object inserted or an existing object is
removed) while an iterator is being used. You should explain how your
implementation deals with this complication as a comment in your code.

As always, your code should be well-designed, well-organized, and
well-commented. Both your design and implementation should be efficient.
However, for this assignment, you may use a linear structure rather than
implement a more complex data structure such as a tree, heap, or hash
table to make insertion/deletion more efficient. It is sufficient that
you implement your linear structure efficiently.

### What to turn in

A sorted-list.c file containing all of your data structure code. At the
top of the file, you should include as a comment a big-O analysis of the
runtime of your code. You should also carefully comment all of your
code. Your grade will be based on how well your code is working as well
as how well written your code is (including analysis of runtime and
comments) and how carefully you tested your code. A main.c file should
including test cases and code to call the libaray.

A tarred gzipped file named pa2.tgz that contains a directory called pa2
with the following files in it:

-   An sorted-list.h file containing the interface we gave you and your
    structure definition. The function defintions must remain unaltered!

-   A sorted-list.c file containing your implementation of the sorted
    list.

-   A main.c file containing a main function that exercise your sorted
    list implementation using the test plan outlined in testplan.txt.

-   A Makefile that is used to compile your sorted list implementation
    into a library called libsl.a and an executable called sl that runs
    the code in main.c.

-   A file called testplan.txt that contains a test plan for your code,
    including input and expected output.

-   A readme.pdf file that contains analyses of the running time and
    memory usage of each of your sorted-list functions. Use big-O
    notation to describe the end result of each analysis.

Suppose that you have a directory called pa2 in your account (on iLab),
containing the above required files. Here’s how you create the required
tar file. (The ls commands are just to help show you where you should be
in relation to pa2. The only necessary command is the tar command.)

    $ ls
    pa2
    $ tar cfz pa2.tgz pa2

You can check your pa2.tgz by either untarring it or running tar tfz
pa2.tgz (see man tar). Your grade will be based on:

-   Correctness (how well your code is working),
-   Quality of your design (did you use reasonable algorithms),
-   Quality of your code (how well written your code is, including
    modularity and comments),

-   Efficiency (of your implementation), and
-   Testing thoroughness (quality of your test cases).

September 24th, 2013 <small>Lecture, Multi-file Projects, Makefiles, and Directory I/O</small>
----------------------------------------------------------------------------------------------

    ar key libfile obj1.o obj2.o ...
        r - add
        t
        d
        v - verbose
        c
        
    ar rv libsl.a sorted_list.o

    basename [directory path]/[basename].[extension]
    [basename].[extension]

    drname [directory path]/[basename].[extension]
    [directory path]

September 26th, 2013 <small>GDB</small>
---------------------------------------

### Reference Counter

-   You increment a reference counter for every time a new pointer
    points to the node.

-   You decrement a reference counter for every time you remove a
    pointer from a node.

-   You free the memory for a node when you decrement it to zero.
-   An iterator pointing to a node that is printing or up to some
    operation can make the reference counter not zero or one, leading to
    some interesting scenarios.

October 2nd, 2013 <small>Programming Assignment 3: Indexer</small>
------------------------------------------------------------------

**Warning**: As you will see below, the descriptions of the assignments
will be increasingly complex because we are asking you to build
increasingly bigger programs. \*Make sure to read the assignment
carefully!\* This is critical because this document essentially
describes the requirements for your program.

### Introduction

In this assignment, you will practice using the file system API (as well
as pointers in different data structures). In particular, you will be
creating, opening, reading, writing, and deleting files.Your task is to
write an indexing program, called an *indexer*. Given a set of files, an
indexer will parse the files and create an *inverted index*, which maps
each term found in the files to the subset of files that contain that
term. In your indexer, you will also maintain the frequency with which
each term appears in each file.Here is an example of how the indexer
should work. If you are given the following set of files:

    +----------+---------------------+
    | Filename | File Content        |
    +----------+---------------------+
    | boo      | A dog name name Boo |
    +----------+---------------------+
    | baa      | A cat name Baa      |
    +--------------------------------+

The indexer should read the files and produce the following inverted
index, in sorted order by word:

    “a” → (“boo”, 1), (“baa”, 1) “baa” → (“baa”, 1) “boo” → (“boo”, 1)  “cat” → (“baa”, 1)  “dog” → (“boo”, 1)  “name” → (“boo”, 2), (“baa”, 1)

After constructing the entire inverted index in memory, the indexer will
save it to a file.Some observations:

-   An inverted index is just a sequence of mappings, where each mapping
    maps a term (e.g., “dog”) to a list of records, with each record
    containing the name of a file whose content contains the term and
    the frequency with which the term appears in the file.

-   The above depiction just gives a logical view of the inverted index.
    In your program, you have to define data structures to hold the
    mappings (term → list), the list of records, and the records (file
    name, count).

-   The mappings are maintained in sorted order of the terms. You will
    see later why this is useful. Sorting in ascending or descending
    order doesn’t matter so much. We will just arbitrarily say for this
    assignment that the sequence should be maintained in ascending
    sorted order based on the ASCII coding of characters (i.e., “a”
    before “b” and “aa” before “ab”).

-   Records in each list are maintained in descending sorted order based
    on frequency counts of the terms in the files. Again, you will see
    later why this is useful.

-   Capitalization has been removed. For your indexer, “A” and “a”
    should be

-   considered the same term. Thus, you will need to normalize all upper
    case letters to lower case letters in the terms. (The other way
    around is OK too.)

-   It should be obvious that the tokenizer and sorted-list that you
    wrote in earlier assignments are useful for this assignment
    (although you have to modify the tokenizer to work with a file,
    rather than a string). Use the improved tokenizer.c file attached to
    this assignment.

### Implementation

Since you are implementing a program in this assignment, there is no
programming interface to follow. Instead, your program must support the
following invocation interface:

    index <inverted-index file name> <directory or file name>

The first argument, <inverted-index file name>, gives the name of a file
that you should create to hold your inverted index. The second argument,
<directory or file name>, gives the name of the directory or file that
your indexer should index. You need to check whether the second name is
a directory or a file. If a directory, you need to recursively index all
files in the directory (and its sub-directories). If a file, you just
need to index that single file.When indexing files in a directory, you
may have files that have the same name (but different pathnames). To
differentiate between them, for now, you may use the pathname (relative
to the input directory name) in each record in the inverted index,
rather than just the file name.Tokenization is a little different in
this assignment than in the previous assignment. You are not given a set
of separators. Instead, we define terms as any sequence of consecutive
alphanumeric characters (a-z, A-Z, 0-9). All other characters are
separators. Note that you can use the entire ASCII coding minus the
alphanumeric characters as your separators to minimize the change to
your tokenizer. But, this is not efficient, since the alphanumeric
characters is only a small subset of ASCII. This would be even truer if
we extend the character set beyond ASCII. So, you should not take this
easy way out.

Examples of tokens according to the above definition include:

    a, aba, c123, 1, 454

If a file contains This an\\\\\$example12 mail@rutgersit should tokenize
to this an example12 mail rutgers

The inverted index file that your indexer writes must follow the
following format, where I’m showing each space as a \_ to make it more
clear:

    <list>_term 
    name1_count1_name2_count2_name3_count3_name4_count4_name5_count5 
    </list>

with the lists arranged in ascending sorted order of the terms. Note you
must obey the line breaks as shown. Each line containing the (file name,
count) records can contain at most 5 records. So, the example inverted
index from Section 1 could look like:

    <list> a    boo 1 baa 1 </list> <list> baa baa 1 </list> <list> boo boo 1 </list> <list> cat baa 1  </list> <list> dog boo 1    <list> name boo 2 baa 1 </list>

This format is quite inefficient in a number of ways. We will optimize
later. For now, we want to be able to easily read the inverted index for
debugging.

You should carefully consider all possible exception cases, outline a
strategy to deal with them, and implement your strategy. For example, if
a file already exists with the same name as the inverted-index file
name, you should give the user the option of not overwriting it. If the
name of the directory or file you are to index does not exist, your
indexer should print an error message and exit gracefully rather than
crash. There are many other error cases that you will need to
consider.You should use multi-file compilation to carefully organize
your code. For example, the tokenizer should be in its own .c file, with
a .h file that callers should include. The same applies for the sorted
list. You should also write a makefile to efficiently compile and link
your indexer.

### Hints

-   Data structures that might be useful include the sorted list you
    just implemented (of course) and a hash table.

-   An object (e.g., a record {“baa”, 3}) can be inserted into multiple
    containing data structures, such as a sorted list and a hash table).

-   You can use your sorted list to maintain the set of terms in
    ascending order. But, since we are asking for records for each term
    sorted in descending order, you have to flip the meaning of \< and
    \> in your comparator function.

-   You should probably approach this in steps.
-   First, you might get your tokenizer to generate correct tokens from
    a file. - Next, you might get your program to walk through a
    directory. - Next, you might implement a data structure that allows
    you to countthe number of occurrences of each unique term in a file.
    o Andsoon...

### What to Turn In

A tarred gzipped file name pa3.tgz that contains a directory called pa3
with the following files in it:

-   All the .h and .c files necessary to produce an executable named
    index.

-   A makefile used to compile and produce index. It must have a target
    clean toprepare a fresh compilation of everything.

-   A file called testplan.txt that contains a test plan for your
    indexer. You should include the example files and/or directories
    that you test your indexer on but keep these from being too large,
    please. (We might test your program with a very large data set
    though so don’t skip testing your program for scalability. In your
    test plan, you should discuss the larger scale testing and the
    results, but you can skip including the data set).

-   A readme.pdf file that describes the design of your indexer. This
    should also include the usual analysis of time and space usage of
    your program. Starting in this assignment, you do not need analyze
    every single function. Rather, you need to analyze the overall
    program. (So, for example, analyzing initialization code is
    typically not too important unless this initialization depends on
    the size of the inputs.)

As usual, your grade will be based on:

-   Correctness (how well your code is working),
-   Quality of your design (did you use reasonable algorithms),
-   Quality of your code (how well written your code is, including
    modularity andcomments),

-   Efficiency (of your implementation), and
-   Testing thoroughness (quality of your test cases).

October 19th, 2013 <small>Programming Assignment 4: Search</small>
------------------------------------------------------------------

### Introduction

In this assignment, you will put everything that you have done together
into a simple search tool. For now, your search tool will look much like
the `grep` utility. Your task is to implement a search tool that will
load an inverted index produced by your indexer into memory and use it
to answer users’ search queries. Using the same example from the indexer
assignment, if you are given the following set of files:

  Filename   File Content
  ---------- ---------------------
  `boo`      A dog name name Boo
  `baa`      A cat name Baa

you would use your indexer to generate the following inverted list and
save it to an index file:

    “a” → (“boo”, 1), (“baa”, 1) 
    “baa” → (“baa”, 1) 
    “boo” → (“boo”, 1)  
    “cat” → (“baa”, 1)  
    “dog” → (“boo”, 1)  
    “name” → (“boo”, 2), (“baa”, 1)

When you run your search tool, it should read the content of the index
file into memory. Then, it should continuously poll for user queries and
output the names of the files with matching content. For example, if the
user gives the query dog, your search tool should output boo. If the
user gives the query name, your search tool should output boo, baa.

### Code Reuse

Your implementation will require the use of inverted-index files
produced by the indexer you wrote for Assignment 4. If you could not get
the previous assignment fully working, you must do so now. The search
tool program must work with the index files produced by both partners’
indexers. This means that, for example, if you did not get your indexer
working, but your partner for the search tool project did, you must fix
your indexer rather than simply relying on your partner’s. Either
indexer’s output files should be able to support your search tool.In
order to do this, you should encapsulate the reading and parsing of an
index file into a module that is separate from the rest of the search
tool. This module should have a fixed interface. You and your partner
should each write a version of this module, conforming to the fixed
interface, that reads and parses your own indexer output file.You should
write a makefile that efficiently compiles and links your search tool.
The makefile must allow the search tool to be linked with either of the
two index file parsing modules, at the user’s option.

### Implementation

Your program must support the following invocation interface:

    search <inverted-index file name>

The first (and only) argument, `<inverted-index file name>`, gives the
name of an index file that your search tool should read into memory. For
now, you may assume that the entire index file will fit into memory (you
will relax this assumption next week). You should design an in-memory
data structure to make the search efficient.

Once search has successfully read and process the index file, it should
go into a loop asking for queries. It should be able to respond to at
least two commands: 1. `sa <term> ...` : search for files containing the
given terms. A query may contain 1 or more terms. If there are more than
1 term, the search tool should return only files that contain all terms
in the query. (The query is a “logical and” of all the given terms.)2.
`so <term> ...`: search for files containing the given terms. A query
may contain 1 or more terms. If there are more than 1 term, the search
tool should return any file that contains any subset of the terms in the
query. (The query is a “logical or” of all the given terms.)3. `q`: the
search tool should gracefully shut itself down.The following example
shows how a user of your application would search for all files
containing ALL of the words ”cat”, ”dog”, and ”bird”:

    sa cat dog bird

As in the last assignment, you should carefully consider all possible
exception cases, outline a strategy to deal with them, and implement
your strategy.

### What to Turn In

-   A writeup documenting your design, including exception handling and
    paying particular attention to the memory requirements of your
    application. Your writeup should detail the format with which the
    inverted index is written into a file.

-   A file called hw5-testcases.txt that contains a thorough set of test
    cases for your code, includ- ing inputs and expected outputs.

-   All source code (for search tool and both versions of all parts of
    the indexer) including both implementation (.c) and interface(.h)
    files.

-   A makefile for producing an executable search tool, with multiple
    targets allowing selection of a compatible indexer.

Your grade will be based on:

-   Correctness (how well your code is working).- Testing thoroughness
    (quality of your test cases).- Efficiency.- Good design (how well
    written your design document and code are, including modularity and
    comments).- Code reuse (that your index works with both indexers).

November 5th, 2013 <small>Midterm Study Guide</small>
-----------------------------------------------------

### The C Programming Language <small>Syntax</small>

#### Pointers and `const`

  Code                           Can change data?   Can change pointer?   Initiliaze data?   Initialize pointer?
  ------------------------------ ------------------ --------------------- ------------------ ---------------------
  `int * ptr;`                   Yes                Yes                   Optional           Optional
  `const int * ptr;`             No                 Yes                   Yes                Optional
  `int * const ptr = &x`         Yes                No                    Optional           Yes
  `const int * const ptr = &x`   No                 No                    Yes                Yes

#### Macros and the preprocessor

-   The C preprocessor (cpp)
    -   Macro processor
    -   Transform code before compilation

-   Initial processing
    -   Read into memory and broken into lines
    -   Merge continued lines
    -   Replace comments with single spaces

-   Tokenization
    -   Identifiers
    -   Preprocessing numbers
    -   String literals
    -   Punctuators

-   Preprocessing languages
    -   Include header files
    -   Macro expansion
    -   Conditional compilations
    -   Line control
    -   Diagnostics

#### Functions and function pointers

Consider this code:

    int compareInts(void * p1, void * p2) {
        int i1 = *(int*)p1;
        int i2 = *(int*)p2;

        return i1 - i2;
    }

    typedef int (*CompareFuncT)(void *, void *);

    CompareFunct cf = &compareInts;
    cf = &compareDoubles;;

    SortedListPtr SLCreate(CompareFuncT cf);

Now, for another example.

Let's start with a basic function which we will be *pointing to*:

    int addInt(int n, int m) {
        return n+m;
    }

First thing, lets define a pointer to a function which receives 2 `int`s
and returns and `int`:

    int (*functionPtr)(int,int);

Now we can safely point to our function:

    functionPtr = &addInt;

Now that we have a pointer to the function, lets use it:

    int sum = (*functionPtr)(2, 3); // sum == 5

Passing the pointer to another function is basically the same:

    int add2to3(int (*functionPtr)(int, int)) {
        return (*functionPtr)(2, 3);
    }

We can use function pointers in return values as well (try to keep up,
it gets messy):

    // this is a function called functionFactory which receives parameter n
    // and returns a pointer to another function which receives two ints
    // and it returns another int
    int (*functionFactory(int n))(int, int) {
        printf("Got parameter %d", n);
        int (*functionPtr)(int,int) = &addInt;
        return functionPtr;
    }

But it's much nicer to use a `typedef`:

    typedef int (*myFuncDef)(int, int);
    // note that the typedef name is indeed myFuncDef
        
    myFuncDef functionFactory(int n) {
        printf("Got parameter %d", n);
        myFuncDef functionPtr = &addInt;
        return functionPtr;
    }

[Source](http://stackoverflow.com/questions/840501/how-do-function-pointers-in-c-work)

#### Header Files

-   Include a file
-   Why use headers?
    -   Copy and paste the same possible large amount of code many
        times.

            #include <stdlib.h>
            #include "myheader.h"

-   Include headerfile only **once**

        #ifndef SORTED_LIST_H
        #define SORTED_LIST_H

        /*
        * Your header file content
         */

        #endif

-   Select a header from many

        #if SYSTEM_1
        #include "system_1.h"

        #elif   SYSTEM_2
        #include "system_2.h"

        #endif

#### Enumeration types

    enum Boolean {true, false};
    Boolean flag = true;

    if (flag == true) {
        printf("true\n");
    } else if (flag == false) {
        printf("false\n");
    { else {
        printf("impossibru\n");
    }

#### Types, Operators, Expressions

Variables & Constants
:   Basic objects

:   Variables are memory location in computer's memory to store data. To
    indicate the memory location, each variable should be given a unique
    name called identifier. Variable names are just the symbolic
    representation of a memory location.

Declarations
:   Name the variables to be used, and additionally their initial
    values.

Operators
:   Specify what to do to varaibles and constants.

Expressions
:   Combine variables, constants, and operators to produce new values.

Types
:   Object belongs to a specific type, which determines what range of
    values it can have, which operations canbe performed.

Variable names
:   Names are made of letters and digits and underscores.

:   Case-sensitive

:   C language-specific keyword such as `if`, `else`, `for`, `int`, are
    reserved.

:   It's advisiable to give variables descriptive names, plus
    prefix/suffix to indicate type and/or scope.

        strABC; // string
        iXYZ; // integer
        g_iXYZ; // global variable
        a_iXYZ; // a function argument

Data types
:   Same as Java

    For integer, there is `signed` and `unsigned`

      Type                  Description                                    Size
      --------------------- ---------------------------------------------- --------
      `char`                Capable of hold one character in ASCII table   1-byte
      `short int`           16-bit integer                                 2-byte
      `int/long/long int`   32-bit integer                                 4-byte
      `long long`           64-bit integer                                 8-byte
      `float`               Single-precision floating point                4-byte
      `double`              Double-precision floating point                8-byte

Character constants
:   Is an integer written as one character within single quote, such as
    `x`, and can be used used like any other intger.

Enumeration constant
:   An enumeration is a list of constant integers

        enum Color { BLACK, WHITE, YELLOW };

    You can achieve the same purpose with `#define`.

#### Functions and Program Structure

Functions
:   Functions break large tasks into smaller ones.

:   Functions help hiding parts of code from other parts which do not
    need to know about them, readibility, source code organizition.

:   Functions allow reusability.

:   C is essentially a functional language.

#### Pointers

Pointer
:   A pointer is a variable that contains the address of a variable.

:   Points are used very often in a high-performance program because of
    direct memory access.

Pointers as function arguments
:   The wrong way of doing it:

        void swap(int x, int y) {
            int temp;

            temp = x;
            x = y;
            y = temp;
        }

        swap(a, b);

:   The right way of doing it:

        void swap(int *px, int *py) {
            int temp;

            temp = *px;
            *px = *py;
            *py = temp;
        }

        swap(&a, &b);

### Makefiles

Target
:   A file to becreated.

    Target depends on a set of source files or other targets in the
    dependency list.

Rules
:   Commands to create the target.

    Each command occupies 1 line, starting with TAB. Be careful with
    space.

<!-- -->



    app: main.o mod_a.o mod_b.o
        cc -o app main.o mod_a.o mod_b.o

    main.o: main.c inc_a.h inc_b.h 
        cc -c main.c

    mod_a.o: mod_a.c inc_a.h 
        cc -c mod_a.c

    mod_b.o: mod_b.c inc_b.h 
        cc -c mod_b.c

    clean:
        rm -f app
        rm -f *.o

-   Name of your makefile should be `Makefile` or `makefile`.
-   Commands you can use:

        make
        make target_label
        make clean

-   What to write in makefile

        target: dependency1 dependency2
        <tab> system command

        # build executable file tokenizer from tokenizer.c
        all: tokenizer.c
            gcc -g -Wall -o tokenizer tokenizer.c

        #remove tokenizer file:
        clean:
            $(RM) tokenizer

-   General form:

        CC = gcc
        CFLAG = -g -Wall
        EXECUTABLE = tokenizer

### I/O and Directory

Linux file structure
:   In Linux, everything is seen as a file:

    -   Disk files
    -   Ports
    -   Network connections
    -   Devices

    The difference is in how they are treated, however, but the general
    principle holds.

File I/O
:   File I/O low-level system calls:

      Function    Description
      ----------- ------------------------------------
      `open()`    Open a file or device
      `read()`    Read from an open file or device
      `write()`   Write to an open file or device
      `close()`   Close the file or device
      `ioctl()`   Pass control info to device driver

:   There's a performance penality in making a system call. It's a good
    idea to keep the number of system calls to a minimum, and do more
    work in each call, such as reading or writing in bulk.

:   Standard (high-level) I/O library provides buffered I/O, and
    arranged system calls to reduce overhead. Library functions are
    provided in `<stdio.h>`.

Standard I/O library
:   It is:

    -   Part of ANSI C
    -   Takes care of buffering
    -   Provides formatted input/output
    -   Functions:
        -   `fopen`
        -   `fclose`
        -   `fread`
        -   `fwrite`
        -   `fseek`
        -   `fflush`
        -   `fprintf`
        -   `fscanf`
        -   `fputc`

### Libraries

-   Group multiple compiled object files into a single file.
-   Used for sharing common pieces of code.
-   Software developers can package code and release an API without the
    actual source code.

-   Libraries (or components) can be created for dynamic use.
    -   Library is separate from executable, thus reduced its size.
    -   Libraries can be invoked when needed.

-   There are two types, dynamic and static libraries.

Static library (`.a`)
:   Library of object code which is linked with, and becomes part of
    something.

:   In computer science, a static library or statically-linked library
    is a set of routines, external functions and variables which are
    resolved in a caller at compile-time and copied into a target
    application by a compiler, linker, or binder, producing an object
    file and a stand-alone executable.

Dynamic library (`.so`)
:   There is only one form of this library but it can be used in two
    ways.

    1.  Dynamically linked at run time but statically aware. The
        libraries must be available during compile/link phase. The
        shared objects are not included into the executable component
        but are tied to the executable.

    2.  Dynamically loaded/unloaded and linked during execution (i.e.
        browser plug-in) using the dynamic linking loaded r system
        functions.

-   Naming convention: `lib` prefix.
-   Example:

        gcc src-file.c -lm -lpthread

#### Static library

-   How to generate a library
    1.  Compile:

            cc -Wall -c ctest1.c ctest2.c

    2.  Create `.a`:

            ar -cvq libctest.a ctest1.o ctest2.o

    3.  List files in library:

            ar -t libctest.a

    4.  Linking:

            cc -o prog prog.c libctest.a 

#### Shared Library

-   How to create:

        gcc -Wall -fPIC -c *.c
        gcc -shared -Wl, -shared, libctrst.so.1 -o libctest.so.1.0 *.o

`-fPIC`
:   Compiler directive to output position independent code, a
    characteristic required by shared libraries, also see `-fpic`

`-shared`
:   Produce a shared object which can then be linked with other objects
    to form an executable.

`Wl,options`
:   Pass options to linker.

        -soname libctest.so.1

-   Cascade the linkageL

        ln -sf /opt/lib/libctest.so.1.0 /opt/lib/libtest.so.1
        ln -sf /opt/lib/libctest.so.1.0 /opt/lib/libtest.so

-   The link to `/opt/lib/libctest.so` allows the naming convention for
    the compile flag `-litest` to work.

-   The link to `/opt/lib/libctest.so.1` allows the run time binding to
    work.

-   Now, for adding the library to a program:

        gcc -Wall -L/opt/lib prog.c -lctest -o prog

-   To list dependancies:

        ldd prog

-   Add library directories to be included during dynamic linking to the
    file

        /etc/ld.so.conf 

-   Add specified directory to library cache:

        ldconfig -n /opt/lib

-   Specify the environment variable `LD_LIBRARY_PATH` to point to the
    directory paths containing the shared object library

### Processes

Process
:   an address space with one or more threads executing within that
    address space, and the required system resources for those threads.

:   Each instance of a running program constitutes a process.

:   a program - or process - that is running consists of program code,
    data, variables (occupying system memory), open files (file
    descriptors), and an environment.

:   A process has its own stack space, used for local variables in
    functions and for controlling function calls and returns. It also
    has its own environment space, containing environment variables that
    may be established solely for this process to use. A process must
    also maintain its own program counter, a record of where it has
    gotten to in its execution, which is the execution thread.

:   All proceeses have:

    -   Process ID (PID)
    -   Parent process ID (PPID)
    -   Signal mask
    -   Signal dispositions
    -   File descriptors

:   Every process belongs to one process group. A *child* process
    inherits the process group of it's a parent.

Process ID
:   a number used by most operating system kernels to temporarily
    uniquely identify a process

:   `PID 0`
    :   Scheduler process

        -   Kernal level process
        -   Responsible for all the process scheduling that takes place
            inside the system always running.

        -   Always running.

    `PID 1`
    :   Initilization process

        -   User level process running with root privileges.
        -   Responsible for bringing up linux system, the first process
            started once a system boot up.

        -   Always running.

File descriptors
:   In POSIX, a file descriptor is an integer, specifically of the C
    type int. There are three standard POSIX file descriptors,
    corresponding to the three standard streams, which presumably every
    process (save perhaps a daemon) should expect to have:

      Integer value   Name
      --------------- ----------------------------
      0               Standard input (`stdin`)
      1               Standard output (`stdout`)
      2               Standard error (`stderr`)

Process Table
:   The Linux process table is like a data structure describing all of
    the processes that are currently loaded with their PID, status, and
    command string etc.

Parent process
:   A parent process shares the following this it's children:

    -   Memory
    -   File descriptors
    -   File positions
    -   Signal dispositions
    -   Signal mask

:   A parent process *does not* share the following with's children:

    -   A parent must *wait* on a child
    -   `fork != 0` for parent (`-1` for error)
    -   `fork == 0` for child
    -   Execute asynchrously

Zombie process
:   Using `forkto` create processes can be very useful, but you must
    keep track of child processes. When a child process terminates, an
    association with its parent survives until the parent in turn either
    terminates normally or calls wait. The child process entry in the
    process table is therefore not freed up immediately. Although no
    longer active, the child process is still in the system because its
    exit code needs to be stored in case the parent subsequently calls
    wait. It becomes what is known as defunct, or a zombie process.

:   A process that has completed execution but still has an entry in the
    porcess table.

    -   Refer to child process.
    -   Child dies before parent.
    -   Parent process does not `wait` so it is unaware of the
        termination of the child.

    -   `kill` does not work for zombie process

Orphan process
:   -   Refer to child process
    -   Parent dies before child
    -   Will be immediately adopted by `init` process

Process state
:   In POSIX,

      `STAT` Code   Description
      ------------- --------------------------------------------
      `S`           Sleeping
      `R`           Running
      `D`           Uninterruptible sleep
      `T`           Stopped
      `z`           Defunct
      `N`           Low priority
      `W`           Paging
      `s`           Process is session leader
      `+`           Process is in the foreground process group
      `1`           Process is multithreaded
      `<`           High priority task

### Signals

Signal
:   A signal is an event generated by the UNIX and Linux systems in
    response to some condition, upon receipt of which a process may in
    turn take some action.
:   Software interrupt mechanism. Notifies a process that a particular
    event has occurred. Events may originate synchronously within the
    process or asynchronously from outside the process.
:   Signals are *raised* by some error conditions, such as memory
    segment violations, floating-point processor errors, or illegal
    instructions. They are *generated* by the shell and terminal
    handlers to cause interrupts and can also be explicitly sent from
    one process to another as a way of passing information or modifying
    behavior.
:   Here's a table!

      Valye   Name        Default Action      Description
      ------- ----------- ------------------- ------------------------------------------------
      1       SIGHUP      terminate process   terminal line hangup
      2       SIGINT      terminate process   interrupt program
      3       SIGQUIT     create core image   quit program
      4       SIGILL      create core image   illegal instruction
      5       SIGTRAP     create core image   trace trap
      6       SIGABRT     create core image   abort program (formerly SIGIOT)
      7       SIGEMT      create core image   emulate instruction executed
      8       SIGFPE      create core image   floating-point exception
      9       SIGKILL     terminate process   kill program
      10      SIGBUS      create core image   bus error
      11      SIGSEGV     create core image   segmentation violation
      12      SIGSYS      create core image   non-existent system call invoked
      13      SIGPIPE     terminate process   write on a pipe with no reader
      14      SIGALRM     terminate process   real-time timer expired
      15      SIGTERM     terminate process   software termination signal
      16      SIGURG      discard signal      urgent condition present onsocket
      17      SIGSTOP     stop process        stop (cannot be caught orignored)
      18      SIGTSTP     stop process        stop signal generated fromkeyboard
      19      SIGCONT     discard signal      continue after stop
      20      SIGCHLD     discard signal      child status has changed
      21      SIGTTIN     stop process        background read attempted fromcontrol terminal
      22      SIGTTOU     stop process        background write attempted tocontrol terminal
      23      SIGIO       discard signal      I/O is possible on a descriptor(see fcntl(2))
      24      SIGXCPU     terminate process   cpu time limit exceeded (seesetrlimit(2))
      25      SIGXFSZ     terminate process   file size limit exceeded (seesetrlimit(2))
      26      SIGVTALRM   terminate process   virtual time alarm (seesetitimer(2))
      27      SIGPROF     terminate process   profiling timer alarm (seesetitimer(2))
      28      SIGWINCH    discard signal      Window size change
      29      SIGINFO     discard signal      status request from keyboard
      30      SIGUSR1     terminate process   User defined signal 1
      31      SIGUSR2     terminate process   User defined signal 2

Raise
:   Used to indicate the generation of a signal.

Catch
:   Used to indicate the receipt of a signal.

#### Signal handling

    void (*signal(int sig, void (*func)(int)))(int);

-   It takes two parameters, sig and func.
    -   The signal to be caught or ignored is given as argument sig.
    -   The function to be called when the specified signal is received
        is given as func.

    -   This function must be one that takes a single int argument (the
        signal received) and is of type void.

-   The signal function itself returns a function of the same type,
    which is the previous value of the function set up to handle this
    signal, or one of these two special values:

-   Not large
-   Should not use global or static data structures
-   The signal that cause invocation of the signal handler is
    **blocked** during the handler execution

-   Different signals can use the same handler function.
-   Allow multiple handlers (in the same functions)
-   Allow different handlers for the same signal at different points of
    program execution.

-   Args determined by OS, not out program

  Value       Meaning
  ----------- --------------------------
  `SIG_IGN`   Ignore the signal
  `SIG_DFL`   Restore default behavior

-   Sending signals (even to self):

        int kill(pid_t pid, int sig);

-   The kill function sends the specified signal, sig, to the process
    whose identifier is given by pid. It returns 0 on success. To send a
    signal, the sending process must have permission to do so. Normally,
    this means that both processes must have the same user ID.

-   Alarm clock (SIGALRM):

        unsigned int alarm(unsigned int seconds);

-   The alarm call schedules the delivery of a SIGALRM signal in seconds
    seconds. In fact, the alarm will be delivered shortly after that,
    due to processing delays and scheduling uncertainties. A value of 0
    will cancel any outstanding alarm request. Each process can have
    only one outstanding alarm. Alarm returns the number of seconds left
    before any outstanding alarm call would be sent, or -1 if the call
    fails.

-   Be sure to know:
    -   Signals and threads
    -   Signals and event-based programming
    -   Signals and processes

-   Disposition
    -   For a delivered signal, the process can:
        -   Ignore
        -   Catch - invoke user-written code in the process
        -   Default action - kill process w/o core dump

-   `signal.h`
    -   Each process has a **signal mask** - the set of blocked signals
        for that process.

    -   C uses opaque type sigset\_t for signal mask implementation

        static void sigint\_handler( int signo ); static void
        timeout\_handler( int signo, siginfo\_t \* info, void \* p);

#### Signal Info

    signinfo_t struct {
        int si_signo;
        int si_errno;
        int si_code;
    }

-   And a union of structure determined by different signals with
    detailed information.

#### Signal Action

    int sigaction ( int signo, const struct sigaction * action,
                    struct sigaction * oldaction );

`signo`
:   any valid signal except kill and stop

`action`
:   pointer to an sigaction struct that specifies new process response
    to signo. Can be null (default action will be set to oldaction).

`oldaction`
:   pointer to previous sigaction for signo. Can be null

  Member type                           Name             Description
  ------------------------------------- ---------------- ---------------------------------------------------------------------------------------
  `void(*)(int)`                        `sa_handler`     `SIG_DFL`, `SIG_IGN`, or pointer to function.
  `sigset_t`                            `sa_mask`        Additional set of signals to be blocked during execution of signal catching function.
  `int`                                 `sa_flags`       Special falgs to affect behavior of signal.
  `void(*)(int, siginfo_t *, void *)`   `sa_sigaction`   Signal catching function.

### Timer

    struct itimerval {
        struct timeval it_interval;
        struct timeval it_value;
    }

-   Activate: call `setitimer` with non-zero `it_value`
-   Deactivate: call `setitimer()` with zero `it_value`, or when timer
    expires with a zero `it_interval`.

-   No multiple, seperate timers for the same process at the same time.

#### Timer activation

  `it_value`   `it_interval`   Result
  ------------ --------------- ----------------------------------
  2,0          5,0             2 second wait, 5 second interval
  2,0          0,0             2 second wait, no repeat
  0,0          5,0             nothing
  0,0          0,0             nothing

### Threads

-   Threads are multiple strands of execution in a single program.
-   A single is a sequence of control within a process.
-   A process runs at least one thread, `main`.
-   `fork()`ing a process: A new copy is created with its own everything
    memory.

-   Starting a new thread: It only has it's own *memory stack*,
    everything else is shared with the process which created it.

-   Advantages
    -   Make a program do a few things at once
    -   Logically is not multicore.
    -   Physically if multicore.
    -   A program can mix input, calculation, and output efficiently.
    -   Accelerate processing on proper multi-core processors.
    -   Switching between threads requires less work than switching
        between processes.

-   Disadvantages
    -   Requires careful design.
        -   Threads are also know as "how to shoot yourself in both feet
            at once."

    -   Debugguging hell. By using a good IDE the job is largely
        mitigated.

    -   A program that split a large calculation into two and the the
        two parts a different threads will not necessarily run more
        quickly on a single processor machine.

#### POSIX Specification

    #include <pthread.h>
    int pthread_create(pthread_t *thread, pthread_attr_t *attr,
                            void *(*start_routine)(void *), void *arg); 
    void pthread_exit(void *retval); 
    int pthread_join(pthread_t th, void **thread_return); /* termination callback */

#### Thread synchronization

Mutex locks
:   Gatekeepers around a piece of code, mutex "guards an object".

:   In computer science, a lock is a synchronization mechanism for
    enforcing limits on access to a resource in an environment where
    there are many threads of execution. A lock is designed to enforce a
    mutual exclusion concurrency control policy.
    [↪](http://en.wikipedia.org/wiki/Lock_(computer_science))

Semaphores
:   Protect sections of code, semaphore "controls a set of objects"

:   In computer science, particularly in operating systems, a semaphore
    is a variable or abstract data type that is used for controlling
    access, by multiple processes, to a common resource in a parallel
    programming or a multi user environment.
    [↪](http://en.wikipedia.org/wiki/Semaphore_(programming))

##### Semaphores

-   A semaphore is a special type of variable that can be incremented or
    decremented, but crucial access to the variable is guaranteed to be
    atomic, even in a multi-threaded program.

-   If two or more threads in a program attempt to change the value of a
    semaphore, the system guarantees that all the operations will in
    fact take place in sequence.

-   Binary semaphore is commonly used. It means only one thread is able
    to execute the guarded piece of code.

    -   Counting semaphore can allow a number of threads to execute
        simultaneously.

            #include <semaphore.h>
            int sem_init(sem_t * sem, int pshared, unsigned int value);

-   This function intializaes a semaphore object pointed to by `sem`,
    sets it sharing option, and gives it an initial integer value.

-   The `pshared` parameter controls the type of semaphore.
    -   If the value is 0, the semaphore is local to the current
        process.

-   Wait until allowed to execute:

        int sem_wait(sem_t *sem);

-   `sem_wait()` **atomically** decreases the value of the semaphore by
    one, but always waits until the semaphore has a non-zero count
    first.

    -   If sem\_wait is called on a semaphore with a value of 0, the
        function will wait until some other thread has incremented the
        valuye so that it is no longer 0.

-   Post when enter the guarded execution.

        int sem_post(sem_t * sem);

-   `sem_post()` **atomically** increases the value of the semaphore by
    one.

    -   If the both programs try to increase the value by 1, the
        semaphore will always be correctly increased in value by 2.

    int sem\_destroy(sem\_t \* sem);

##### Mutex

-   Mutual exclusion
-   Allowing programmer to lock an object, only one thread can access
    it.

-   Must local the mutex before entering and unlock it when you finish.

        #include <pthread.h>
        int pthread_mutex_init(pthread_mutex_t *mutex, const pthread_mutexattr_t *mutexattr); 
        int pthread_mutex_lock(pthread_mutex_t *mutex));
        int pthread_mutex_unlock(pthread_mutex_t *mutex); 
        int pthread_mutex_destroy(pthread_mutex_t *mutex);

November 9th, 2013 <small>Programming Assignment 5: Multithreaded Book Order System</small>
-------------------------------------------------------------------------------------------

### Introduction

For this assignment, you will write a multithreaded book order
simulation program. This will give you an opportunity to exercise
mutexes and thread coordination. You will write a producer- consumer
program with a single producer and multiple consumers. Your producer and
your con- sumers will run as separate threads, so you will use mutexes
to protect and manage shared data structures.

### Producer: Book Order Input Thread

Your program will spawn a single order input thread (the producer). The
input thread will read in a data file containing multiple book orders,
one book order per line. Each book order will consist of:

-   Book Title (a string in double quotes)
-   Customer ID number (a unique integer)
-   Category (a unique alphanumeric string)

Each book order will be handled by a separate book order processor
thread (the consumers). You have (at least) two choices for where the
producer thread puts the book orders. First, you may opt to put the book
orders into separate queues, one for each category. Each consumer thread
will have exclusive access to a specialized queue. Second, you may
choose to put all book orders into a single shared buffer that will be
used by all the consumer threads. The book order queues (or buffer) are
initially empty.Example book categories may include `Sports`, `Housing`
or `Politics`.

### Consumers: Book Order Processor Threads

Your program will also spawn multiple Book Order Processor threads (the
consumers), one con- sumer thread for each book category. The Book Order
Processor threads will extract all book orders for their category from
the data structure shared with the producer and print the individual
orders as they are processed. See below for a description of order
processing. Remember that individual customers can and will make
different book orders for books from different categories.The Book Order
Processor thread will also use a customer database that holds:

-   Customer name
-   Customer ID number (should match order entered into queue)
-   Credit Limit (a dollar amount)

An order is processed by first finding the customer in the database,
then deciding if the customer’s credit limit is greater than or equal to
the price of the ordered book. If the customer has sufficient funds, the
credit limit is debited and the order processor thread prints an order
confirmation listing the book name, price and shipping information
(customer name, address, state, zip code). If the customer does not have
sufficient funds, the order processor thread should print out an order
rejection that identifies the customer name, the book order details and
the remaining credit limit value for the customer. After all book orders
have been processed, the program must print out a final report listing
the following for each customer:

-   Customer name
-   Customer ID number
-   Remaining credit balance after all purchases (a dollar amount)

And for each customer, make two lists. The first list is for successful
book orders (the ones they can afford), and the second is for
unsuccessful book orders (the ones they could not afford). Each line of
the successful book orders should include:

-   Book title
-   Book price (a dollar amount)
-   Remaining credit balance after this purchase (a dollar amount)

Each line of unsuccessful book orders would include:

-   Book title
-   Book price (a dollar amount)

The program should also print the total revenue gained from all
successful book orders.You may have to spawn other threads to make this
book ordering system work.

> Requirement 1: there should be NO BUSYWAITING in any of your code.
>
> Requirement 2: there should be NO DEADLOCKS and NO RACE CONDITIONS in
> your code.

### Program Start-up

The command-line arguments will specify the following:

-   `Arg 1: the name of the database input file`
-   `Arg 2: the name of the book order input file`
-   `Arg 3: the list of category names (alphanumeric strings      separated by blanks in a single- or double-quoted string)`

Your program starts by reading in the customer database file and setting
up the customer data base. It then spawns the producer thread and the
consumer threads, one consumer thread for each category.

### Program Termination

After all in input has been processed, the producer and all the consumer
threads shut shut down and the program should print out the final report
as described above.

### Extra Credit

Normally, the producer and consumer threads run in the same process. For
extra credit, you can make the producer and consumer threads run as
separate processes that communicate through `shared memory`. Your
producer program would set up the shared memory and then use `fork()`
and `exec()` to spawn the consumer process(es). You could have a single
consumer process that handles all book categories (maybe with separate
threads for each category) or you could have separate consumer
processes, each of which handles a separate book category. As a
responsible parent process, the producer process would use wait() to
clean up the child consumer process(es) and clean up the shared
memory.If you choose to use separate processes, it would be useful (and
look cool) to have the producer process print out messages about the
consumer process(es) is creates–something like ”Created child consumer
process `<PID>` to handle category `<CATEGORY>`”. You can also add
similar messages about how the producer parent wait()s for each of its
children. You could also add messages about set up and removal of shared
memory.

### What to turn in

A writeup documenting your design paying particular attention to the
thread syn- chronization requirements of your application.All source
code including both implementation (.c) and interface(.h) files. A
makefile for producing an executable program file.Your grade will be
based on:

-   Correctness (how well your code is working, including avoidance of
    deadlocks.

-   Efficiency (avoidance of recomputation of the same results,
    avoidance of busy-waits).

-   Good design (how well written your design document and code are,
    including modularity and comments).

November 8th, 2013 <small>Shared Memory</small>
-----------------------------------------------

-   The lifetime is larger than a process but less than a file.
    -   If you reboot, it goes away.
    -   If no process is using them, they still remain, or can.

-   Shut down the system and the shared memory ceases to exit.
    -   We have shared memory segments that exist indepedant of
        procesesses.

-   Are not tied to the file memory model we're familiar with.
    -   They do, however, have read/write permissions just like files
        do.

-   Instead of a directory structure, shared memory exists in a shared,
    flat list.

    -   They're identified by a numeric key, a number.

-   They key is generated from existing files and directories.
    -   Metadata *about* the files.

-   It's like virtual memory.
    -   The shared memory system has a lifetime that's shorter than the
        directory structure.

        -   This is how we have *persistance* of identification.

    -   But if the file goes away, **heaven help you**.
        -   Something something, that would be bad.

> If you change the file, what happens?

-   If you delete the file, you may no longer be able to find the key.

    -   I'll talk about this later.

-   Multiple shared memory segments can exist.
    -   These things can be of different sizes.
    -   You can get *multiple* shared memory segments.

> Is this like caches?

-   No, because we're not getting efficiency from this.
    -   It *is* faster than reads or writes or socket connections.

-   Different processes may attach the same addresses to different
    segments.

    -   Any attempt to share pointers will be dangerous.

> Is there any reason that different processes have different pointers?

-   Probably not.
    -   He understands *part of it*.

-   The same program may attach the same memory segment to different
    addresses at different invocations.

-   The shared memory does not have an address until you "attach" to it.

    -   Processes *attach* and *detach* to and from shared memory
        segments.

-   Multiple programs running simultaneously may attach different
    addresses to the same memory segments.

-   Because these things exist indepedantly of any process, not only do
    we have an API but because we have commands.

`ipcs -m`
:   This is like "list all shared memory segments"

        nbp-168-15:~ pauljones$ ipcs -m
        IPC status from <running system> as of Tue Nov 12 20:31:44 EST 2013
        T     ID     KEY        MODE       OWNER    GROUP
        Shared Memory:

        nbp-168-15:~ pauljones$ 

`ipcrm -m ID`
:   Removes shared memory with ID.

> Could there be two addresses for the same one?

-   Only within programs, not physically.

        for i in `ipcs -m | grep morbius`; do
            ipcrm -m $i > /dev/null 2 >& 1
        done

-   The maximum size of shared segments seems to be `2147483647` and
    `256` of them.

    -   But this is machine dependant.

> CLEAN UP.

    for i in `ipcs -m | grep [your id here] | colrm 1 11 \ colrm 11`; do
        ipcrm -m $i
        done
        ipcs -m

<!-- -->


    #include <sys/types.h>
    #include <sys/ipc.h>

-   The beauty of `ftoke` is ...

        int shmctl(int shmid, int cmd, struct shmid_ds *);

November 14th, 2013 <small></small>
-----------------------------------

-   We have two ways of resolving an interesting problem:
    1.  How does a program find out how big a peice of shared memory is?
        -   These programs have *shared knowledge*.

-   If the same process which creates the linked list also *accesses*
    the linked list, that's fine.

    -   On the other hand, if another process creates and another
        acceses, big trouble.

-   The idea is to say, "Oh, yeah, the idea is to have not pointers, but
    offsets by which we access shared memory in multiple programs."

-   *Do not put pointers in shared memory*.
    -   *Array is a **really good idea***.

December 5th, 2013 <small>Lecture</small>
-----------------------------------------

### Exam topics

1.  mutex locks
2.  signal locks
3.  signal handling
4.  multiprogramming, fork, exec, wait
5.  shell scripting
6.  shared memory
7.  pointers to functions
8.  deadlock
9.  semaphores

### Shell Programming

-   All programs return signal numbers back to the shell.
-   They use exit, return.
-   The if, while, for, until return an exit status.
    -   The last symbol command

-   Pipelines and lists
    -   The exit status is captured in the `\$?`

#### Tests

  Flag          Function
  ------------- -------------------------------------------------------------
  `-e`          file exists
  `-a`          file exists[^1]
  `-f`          file is a *regular* file (not a directory or device file)
  `-s`          file is not zero size
  `-d`          file is a directory
  `-b`          file is a block device
  `-c`          file is a character device
  `-p`          file is a pipe
  `-h`          file is a [symbolic link](basic.html#SYMLINKREF)
  `-L`          file is a symbolic link
  `-S`          file is a [socket](devref1.html#SOCKETREF)
  `-t`          file descriptor is associated with a terminal device
  `-r`          file has read permission (*for the user running the test*)
  `-w`          file has write permission (for the user running the test)
  `-x`          file has execute permission (for the user running the test)
  `-g`          set-group-id (sgid) flag set on file or directory
  `-u`          set-user-id (suid) flag set on file
  `-k`          *sticky bit* set
  `-O`          you are owner of file
  `-G`          group-id of file same as yours
  `-N`          file modified since it was last read
  `f1 -nt f2`   file `f1` is newer than `f2`
  `f1 -ot f2`   file `f1` is older than `f2`
  `f1 -ef f2`   files `f1` and `f2` are hard links to the same file

#### Functions via (Tutorials Point)[http://www.tutorialspoint.com/unix/unix-shell-functions.htm]

Functions enable you to break down the overall functionality of a script
into smaller, logical subsections, which can then be called upon to
perform their individual task when it is needed.

Using functions to perform repetitive tasks is an excellent way to
create code reuse. Code reuse is an important part of modern
object-oriented programming principles.

Shell functions are similar to subroutines, procedures, and functions in
other programming languages.

##### Creating Functions:

To declare a function, simply use the following syntax:

    function_name () { 
       list of commands
    }

The name of your function is function\_name, and that's what you will
use to call it from elsewhere in your scripts. The function name must be
followed by parentheses, which are followed by a list of commands
enclosed within braces.

##### Example:

Following is the simple example of using function:

    #!/bin/sh

    # Define your function here
    Hello () {
       echo "Hello World"
    }

    # Invoke your function
    Hello

When you would execute above script it would produce following result:

    $./test.sh
    Hello World
    $

##### Pass Parameters to a Function:

You can define a function which would accept parameters while calling
those function. These parameters would be represented by \$1, \$2 and so
on.

Following is an example where we pass two parameters *Zara* and *Ali*
and then we capture and print these parameters in the function.

    #!/bin/sh

    # Define your function here
    Hello () {
       echo "Hello World $1 $2"
    }

    # Invoke your function
    Hello Zara Ali

This would produce following result:

    $./test.sh
    Hello World Zara Ali
    $

##### Returning Values from Functions:

If you execute an exit command from inside a function, its effect is not
only to terminate execution of the function but also of the shell
program that called the function.

If you instead want to just terminate execution of the function, then
there is way to come out of a defined function.

Based on the situation you can return any value from your function using
the **return** command whose syntax is as follows:

    return code

Here *code* can be anything you choose here, but obviously you should
choose something that is meaningful or useful in the context of your
script as a whole.

##### Example:

Following function returns a value 1:

    #!/bin/sh

    # Define your function here
    Hello () {
       echo "Hello World $1 $2"
       return 10
    }

    # Invoke your function
    Hello Zara Ali

    # Capture value returnd by last command
    ret=$?

    echo "Return value is $ret"

This would produce following result:

    $./test.sh
    Hello World Zara Ali
    Return value is 10
    $

##### Nested Functions:

One of the more interesting features of functions is that they can call
themselves as well as call other functions. A function that calls itself
is known as a *recursive function*.

Following simple example demonstrates a nesting of two functions:

    #!/bin/sh

    # Calling one function from another
    number_one () {
       echo "This is the first function speaking..."
       number_two
    }

    number_two () {
       echo "This is now the second function speaking..."
    }

    # Calling function one.
    number_one

This would produce following result:

    This is the first function speaking...
    This is now the second function speaking...

##### Function Call from Prompt:

You can put definitions for commonly used functions inside your
*.profile* so that they'll be available whenever you log in and you can
use them at command prompt.

Alternatively, you can group the definitions in a file, say *test.sh*,
and then execute the file in the current shell by typing:

    $. test.sh

This has the effect of causing any functions defined inside test.sh to
be read in and defined to the current shell as follows:

    $ number_one
    This is the first function speaking...
    This is now the second function speaking...
    $

To remove the definition of a function from the shell, you use the unset
command with the .f option. This is the same command you use to remove
the definition of a variable to the shell.

    $unset .f function_name

December 8th, 2013 <small>Error detecting `malloc()` and `free()`</small>
-------------------------------------------------------------------------

### Introduction

In this assignment, you will implement `malloc()` and `free()` library
calls for dynamic memory all- cation that detect common dynamic memory
errors. You can use the `malloc()` and `free()` code from the Kernighan
and Ritchie C book or use the algorithms presented in lecture. To keep
things simple, you can use a static char array (e.g. static char
`myblock[5000]`) for your `malloc()` and `free()` to use to manage
dynamic memory. This eliminates worries about where the dynamic memory
comes from. The basic functionality of `malloc( size t size )` is to
return a pointer to a block of the requested size. This memory comes
from a memory resource managed by the `malloc()` and `free()` functions.
To keep things simple, you can use a static char array (e.g.
`static char myblock[5000]`) for your `malloc()` and `free()` as your
memory resource. This eliminates worries about where the dynamic memory
comes from. The `free( void * )` function returns the allocated block to
the memory resource, making it available to use in later `malloc()`
calls.The reason we need an error-detecting dynamic memory manager is to
detect commonly-made errors made by programmers using dynamic memory.
Some of these problems are described in the next section.

### Detectable Errors

Your `malloc()` and `free()` implementation should be able to catch at
least the following errors:

-   free()ing pointers that were never allocated. For example

        int x;
        free( x );

-   `free()`ing pointers to dynamic memory that were not returned from
    `malloc()`. For example

        p = (char *) malloc( 200 );     
        ...     
        free( p + 10 );

-   redundant `free()`ing of the same pointer. For example

        free( p );      
        free( p );  

    is an error, but

        p = (char *)malloc( 100 ); 
        free( p );
        p = (char *)malloc( 100 ); 
        free( p );

    is perfectly valid, even if `malloc()` returned the same pointer
    both times.

-   **Saturation**. What happens when you have a test program that
    allocates all of available dynamic memory? Your implementation
    should be able to handle this contingency.

-   **Fragmentation**. It is possible to allocate and free many small
    blocks in a way that leaves only small blocks available for
    allocation. When a request for a large block is made, the request
    fails even though the total amount of free memory is larger than the
    requested block size. There are ways to deal with this problem.
    First, one part of your memory resource can be reserved for small
    blocks, leaving the rest available for larger blocks. Second, large
    blocks can be allocated from one end of your memory resource and
    small blocks can be allocated from the opposite end. You can use
    these ideas or invent your own.

### Responding to Detected Errors

Your modified `malloc()` and `free()` should report the precise calls
that caused dynamic memory problems during program execution. Let’s take
advantage of a couple of preprocessor features in the following sample
macro definitions:

    #define malloc( x ) mymalloc( x, FILE , LINE )
    #define free( x ) myfree( x, FILE , LINE )

I'll leave it to you to make the best use of what’s in these macros.

### What to turn in

-   A writeup documenting your design.
-   A file called `hwextra-testcases.txt` that contains a thorough set
    of test cases for your code, including inputs and expected outputs.
-   All source code including both implementation (`.c`) and
    header(`.h`) files.
-   A makefile for producing executable test program, with multiple
    targets allowing selection of test programs.

Your grade will be based on:

-   Correctness (how well your code is working).
-   Testing thorough ness (quality of your test cases).
-   Efficiency.
-   Good design (how well written your design document and code are,
    including modularity and comments).

<!-- Abbreviations -->

<!-- Footnotes -->

[^1]: This is identical in effect to -e. It has been "deprecated," and
    its use is discouraged.
