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
increasingly bigger programs. *Make sure to read the assignment
carefully!* This is critical because this document essentially describes
the requirements for your program.

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

If a file contains This an\$example12 mail@rutgersit should tokenize to
this an example12 mail rutgers

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

    +----------+---------------------+
    | Filename | File Content        |
    +----------+---------------------+
    | boo      | A dog name name Boo |
    +----------+---------------------+
    | baa      | A cat name Baa      |
    +--------------------------------+

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

