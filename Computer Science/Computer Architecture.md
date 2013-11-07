Computer Architecture <small>with Professor Brian Russell</small> {#computer-architecture-with-professor-brian-russell}
=================================================================

Description {#description}
-----------

This course covers the fundamental issues in the design of modern
computer systems, including the design and implementation of key
hardware components such as the processor, memory, and I/O devices, and
the software/hardware interface.

-   Topics:
    -   C programming
    -   Data representation and computer arithmetic
    -   Assembly language programming
    -   Boolean algebra
    -   Basic digital logic design
    -   Processor design
    -   Cache design
    -   Main memory design

Syllabus {#syllabus}
--------

-   Instructor: Brian Russell
    -   <a href = "mailto:morbius@cs.rutgers.edu">Email</a>
    -   Office Hours: Wednesdays 8:00-9:00 pm, Hill 403.

-   TAs
    -   Yuanzhen Gu
        -   <a href = "mailto:yg185@cs.rutgers.edu">Email</a>
        -   Office Hours: Thursdays, 3:00-4:00 pm, Hill 418

    -   Longhao Shu
        -   <a href = "mailto:ls675@cs.rutgers.edu">Email</a>
        -   Office Hours: Thursdays, 5:00-6:00 pm, Hill 416

    -   Chaowei Tan
        -   <a href ="mailto:ct382@cs.rutgers.edu">Email</a>
        -   Office Hours: Fridays, 9:00-10:00 am, Hill 488

    -   Vilemini Kalambratsidou
        -   <a href = "mailto:vilelmini.kalabratsidou@gmail.com">Email</a>
        -   Office Hours: Wednesdays 10:00 am-Noon, Hill 410

### Objective {#objective}

The aim of CS 211 is to provide an understanding of the fundamental
logical organization of a computer (its parts and their relationship)
and how it actually works; exposure to a central processor's native
language, and to basic computer components. Basic Architecture for high
performance design.

### Prerequisite Knowledge {#prerequisite-knowledge}

-   Prior programming experience in a high-level language (such as
    Java).
-   01:198:112. Credit not given for this course and 14:332:331.

### Topics {#topics}

The following list is organized by topic, not by chronological order of
coverage in the course.

1.  Von Neumann Architecture, Hardware trends, Importance of Speed,
    Cost, Energy
2.  Intro to C programming
3.  Data Representation, Computer Arithmetic
4.  Assembly language techniques, including macro-instruction definition
5.  Digital logic, registers, instruction counter
6.  Processor Architecture
7.  Pipelining
8.  Memory hierarchies, Caching (L0, L1, L2 caches)
9.  Virtual Memory
10. Interrupts
11. Input and Output, buses

### Schedule {#schedule}

1.  Jan 22 Into to hardware trends, Moore's law. Chap 1.
2.  Jan 24 Into to C programming
3.  Jan 29 C program structure, control flow structures
4.  Jan 31 Pointers and arrays, C functions
5.  Feb 05 Dynamic memory management
6.  Feb 07 C preprocessor, formatted I/O
7.  Feb 12 Data representation. Chap 2.1 2.2 2.4.
8.  Feb 14 Computer Arithmetic.31
9.  Feb 19 Assembly Language Programming Chap 3.
10. Feb 21 Assembly Language Programming
11. Feb 26 Assembly Language Programming
12. Feb 28 Assembly Language Programming
13. Mar 05 Assembly Language Programming
14. Mar 07 Assembly Language Programming
15. Mar 12 Spring Break -- no class
16. Mar 14 Spring Break -- no class
17. Mar 19 Digital Logic Chap 4.2
18. Mar 21 Digital Logic
19. Mar 26 Processor Design
20. Mar 28 Midterm
21. Apr 02 Processor Design
22. Apr 04 Processor Design
23. Apr 09 Processor Design
24. Apr 11 Caches
25. Apr 16 Caches
26. Apr 18 Caches
27. Apr 23 Caches
28. Apr 25 I/O and Disks
29. Apr 30 Review

### Expected Work {#expected-work}

Students are expected to attend all lectures and perform all reading
assignments prior to lecture. Students are also expected to attend all
recitation section meetings. Students will be evaluated according to
their performance on four programming projects, programming project, a
mid-term examination, and a final examination.

### Grading {#grading}

-   40% Correctness
    -   Percent based on number of test cases

-   40% Code Quality
    -   20% Algorithmic
    -   10% Reusability/Modularity
    -   10% Decomposition

-   20% Documentation
    -   10% Test Cases from Students
    -   5% Comments
    -   5% Documentation (Analysis, readme files, etc...)

### Project Warning {#project-warning}

This is a project course, which means that this course should give you
more than a passing knowledge of computer architecture. The project work
will be a major undertaking. If you complete the projects, you will have
learned a lot. However, assess your commitment to this course
realistically. If you don't have the time or the inclination to work
hard on the project, you would be better off not taking the course. You
will have to learn how to build and debug C and Assembly programs and
make them robust to outside errors. You will also have to describe how
your program work in a written document. There are three or four
programming assignments. Students are required to complete the parts by
the scheduled deadlines. Failure to turn in the project by the deadline
using the electronic handin website will result in a zero grade. No
exceptions! There are many different operating systems and variants of C
out there and we cannot test your program on all of them. So all program
assignments must run on the local iLab Linux machines. We will be
grading your assignments on those machines as well.

### Working Together and Academic Honesty {#working-together-and-academic-honesty}

Cheating on projects and exams will not be tolerated. We want to protect
the fairness and integrity of the class, so we run code similarity
detectors on the projects and scrutinize exams for copying. Both parties
in the exchange are liable; e.g. if you give away solutions to friends,
you're putting yourself at risk too. If you get caught, it's a nasty
process---| just don't go there! You're better off asking for help, or
at worst, dropping the course and trying it again. The department
academic integrity policy can be found at
[here](http://www.cs.rutgers.edu/policies/academicintegrity/). You now
need to click explicitly on a link when first login to our computing
facilities,use handin, etc., that says you acknowledge being aware of
the policy (which you can read through the login screen). If you fail to
do the click-through by the end of September, your access to our
facilities will cease October 1.

#### The Gilligan's Island Rule {#the-gilligans-island-rule}

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

January 22nd, 2013 - Lecture: Hardware trends, Moore's law, Chapter 1 {#january-22nd-2013---lecture-hardware-trends-moores-law-chapter-1}
---------------------------------------------------------------------

-   The modern computer is a general purpose computer which stores
    programs as data.
-   The hardware understands the encoded instructions and reacts
    predictably.
-   The way the hardware executes a program is specific to the hardware,
    yet with similar results.
-   We'll look at assembly for the Intel structure.
-   Instructions as data - ones and zeros.
-   Main components of computer
    -   CPU
    -   Memory
        -   It is sometimes still called "core memory" for hustorical
            reasons.
        -   It is now "transistorized", computer programs "barf and
            die."
        -   It is random access - it can be done in constant time.
        -   It is volatile - turn the power off and memory is gone.

    -   Bus
    -   I/O devices
        -   Human interface
        -   Storage
        -   Network cards
        -   Graphics cards

-   Control flow - any computer program can be written as three things:
    1.  sequencing,
    2.  alteration, and
    3.  repetition

-   Von Neumann Model
    -   Fetch and execute cycle
        -   What the CPU is doing is taking a bunch of instructions
            physcially next to each other in memory.
        -   The Intel architecture, and I love this, takes the address
            `0xFFFFFFF0` to boot the machine.
        -   First step is the fetch cycle, go get the instruction at the
            startup address.
        -   Then decode the instruction, what is encoded? What do I do
            with it?
        -   There are input operands on the instructions.
        -   Then execute the operation, put the operations back on the
            register operands, get the pointer to the next instruction.

    -   This guy got credit for work that was done previously, by Alan
        Turing.
    -   This was known as the "Turing Machine", which was a theoretical
        machine at the time.
    -   A few other contempories applied for pantents about instructions
        in memory.
    -   There was some dispute with Von Neumann and drafts and whose
        names appeared.
    -   A CPU and memory are connected by a bus.
    -   The Von Neumann bottleneck.

-   Moore's law

January 22nd, 2013 - Assignment 1: Wordstat {#january-22nd-2013---assignment-1-wordstat}
-------------------------------------------

### Introduction {#introduction}

This assignment is designed to get you some initial experience with
programming in C, as well as compiling, linking, running, and debugging
a C program in our environment.

Your task is to write a C program called `wordstat` that reads a text
file, finds all the unique words in the file, prints them in
lexicographical order along with the total number of times each word
appears (case-insensitive) and a count of different case-sensitive
versions of the word.

A word is defined as any sequence of letters (A-Z, a-z) and digits (0-9)
that starts with a letter, followed by 0 or more letters and/or digits.
This definition is equivalent to the following regular expression:

    ([A-Z]|[a-z])([A-Z]|[a-z]|[0-9])*

Words in the input file correspond to the longest sequences that match
the above expression when reading the file from beginning to end. Each
unique word is case-insensitive. That is, “book” and “Book” and “bOOk”
are all occurrences of the same word. However, they represent three
different case-sensitive versions of the word “book”.

As an example, running `wordstat` on a text file with the following
content:

    Some Bogus ?Random1> (random1modnar) [34ranDom1] (Random1) boGus-$con@tent.

should produce:

    Word            Total No. Occurrences   No. Case-Sensitive Versions
    bogus           2                       2
    con             1                       1
    random1         3                       2
    random1modnar   1                       1
    some            1                       1
    tent            1                       1

### Implementation {#implementation}

Implement a program called `wordstat` with the following usage
interface:

    wordstat <argument>

where `<argument>` is either the name of the file that `wordstat` should
process, or -h, which means that `wordstat` should print out a help menu
to guide the user on how to use the program.

As discussed above, when invoked with a valid file name, `wordstat`
should find and output all the unique words in the file in
lexicographical order, along with the total number of times each word
appears (case-insensitive) and a count of different case-sensitive
versions of the word.

We leave the choice of data structures and algorithms up to you.
However, your implementation must be reasonably efficient. For example,
maintaining an array of records and doing linear search through this
array would be unacceptable. You are allowed to use functions from
standard libraries (e.g., `strcmp()`) but you cannot use third- party
libraries downloaded from the Internet (or from anywhere else). If you
are unsure whether you can use something, ask us. We will compile and
test your program on the iLab machines so you should make sure that your
program compiles and runs correctly on these machines. You must compile
all C code using the gcc compiler with the `-ansi -pedantic -Wall`
flags.

### Submission {#submission}

You have to e-submit the assignment using Sakai. Your submission should
be a tar file named pa1.tar. To create this file, put everything that
you are submitting into a directory (folder) named pa1. Then, cd into
the directory containing pa1 (that is, pa1’s parent directory) and run
the following command:

    tar cvf pa1.tar pa1

To check that you have correctly created the tar file, you should copy
it (pa1.tar) into an empty directory and run the following command:

    tar xvf pa1.tar

This should create a directory named pa1 in the (previously) empty
directory. The pa1 directory in your tar file must contain: \*
readme.pdf: This file should briefly describe the main data structures
being used in your program, a big O analysis of the run time and space
requirement of your program, and any challenges you encounter in this
assignment \* Makefile: there should be at least two rules in your
Makefile: 1. `wordstat`: build your `wordstat` executable. 2. clean:
prepare for rebuilding from scratch. \* source code: all source code
files necessary for building `wordstat`. Your source code should \*
contain at least 2 files: `wordstat.h` and `wordstat.c`.

We will provide a small script that you can use to check for the above
required items. You do not have to run it, but it might help you to
check that you are handing in everything that we are asking for.

### Grading Guidelines {#grading-guidelines}

#### Functionality {#functionality}

This is a large class so that necessarily the most significant part of
your grade will be based on programmatic checking of your program. That
is, we will build a binary using the Makefile and source code that you
submitted, and then test the binary for correct functionality against a
set of inputs. Thus: \* You should make sure that we can build your
program by just running make. \* You should test your code as thoroughly
as you can. In particular, your code should be adept at handling
exceptional cases. For example, `wordstat` should not crash if the
argument file does not exist.

Be careful to follow all instructions. If something doesn’t seem right,
ask.

#### Design {#design}

Having said the above about functionality, design is a critical part of
any programming exercise. In particular, we expect you to write
reasonably efficient code based on reasonably performing algorithms and
data structures. More importantly, you need to understand the
performance (time & space) implications of the algorithms and data
structures you chose to use. Thus, the explanation of your design and
big O analyses in the readme.pdf will comprise a non-trivial part of
your grade. Give careful thoughts to your writing of this file, rather
than writing whatever comes to your mind in the last few minutes before
the assignment is due.

#### Coding Style {#coding-style}

Finally, it is important that you write “good” code. Unfortunately, we
won’t be able to look at your code as closely as we would like to give
you good feedback. Nevertheless, a part of your grade will depend on the
quality of your code. Here are some guidelines for what we consider to
be good: \* Your code is modularized. That is, your code is split into
pieces that make sense, where the pieces are neither too small nor too
big. \* Your code is well documented with comments. This does not mean
that you should comment every line of code. Common practice is to
document each function (the parameters it takes as input, the results
produced, any side-effects, and the function’s functionality) and add
comments in the code where it will help another programmer figure out
what is going on. \* You use variable names that have some meaning
(rather than cryptic names like i). Further, you should observe the
following protocols to make it easier for us to look at your code: \*
Define prototypes for all functions. \* Place all prototype, typedef,
and struct definitions in header (.h) files. \* Error and warning
messages should be printed to stderr using fprintf.

January 24th, 2013 - Lecture: Introduction to C programming {#january-24th-2013---lecture-introduction-to-c-programming}
-----------------------------------------------------------

-   `.java` -\> `.class` (machine independant)
-   `c` code -\> machine / OS specific -\> executable
-   "Hello world" in C

        #include <stdio.h>
        int
        main() {
            printf("cogito ero sum\n");
            return 0;
        }

-   To run the program above, `cogito.c`:

        gcc cogito.c
        gcc -o cogito cogito.c
        gcc -c cogito.c
        gcc cogito.o

-   command line arguments:

        #include <stdio.h>
        int
        main(int argc, char**argv) {
            int i;
            for(i = 0; i < argc, i++) {
                printf("arg %d is %s\n", i, argv[i]);
            }

-   structs
    -   there are no constructors
    -   there are no member functions
    -   there are no visibility restrictions (all public)
    -   no need for dynamically allocating them

January 29th, 2013 - Lecture: C program structure, control flow structures {#january-29th-2013---lecture-c-program-structure-control-flow-structures}
--------------------------------------------------------------------------

-   Sometimes we as programmers we need some a variable that can only
    take on a few values.
-   Java, evidently, screwed this up.

        enum stoplight {
            red,yellow,green
        }

        enum stoplight x;
        int y;
        x = red;
        y = green;
        x = (enum stoplight) 37;

-   The internal numbering scheme for this unmodified syntax makes:
    -   `red = 1`
    -   `yellow = 2` and
    -   `green = 3`

-   If the first line was `red = 5`, then the following values would be
    incremeneted from that.
-   `typedef`

        typedef int size;

    -   my ability to decalre an alias for a new type
    -   now I get to say things like `size x,y`
    -   I am defining an alias for an existing type.

-   `struct`

        typedef struct pt {
            int x,y;
        } point;

        point left_bot, right_top;

-   `sizeof`

        sizeof unary-expression;
        sizeof (typename)
        & // "give me the address of this variable"
        * // unary prefix operator - "d-reference pointer"
        , // underutilized in java and c - "me seperating multiple expression"
        -> // "I use that to get at pointers or members of struct"

-   To prompt for input

        while(printf("enter an integer>>"),scanf("%d",$x)>0) {
            printf("%d\n",x);
        }

-   Pointers

        int *p;
        int x;

    -   In C, C++ you get pointers, which are the address in memory of
        an variable.
    -   `p` is a pointer to an integer

-   functions

        void
        swap(int *p1, int *p2) {
            int temp;
            temp = *p1;
            *p1 = *p2;
            *p2 = temp;
        }

    -   this is afunction in C that swaps two values
    -   if you try to pass two integers directly, the compiler will
        complain
    -   I want to pass something that I want to change, and if I want to
        do that, I should pass the address of what I want to change.

-   Pointers and arrays

        int *p, A[10],x;

        p = &A[0]; // the address of an int I can put in a pointer
        p = A; // the name of an array, A with no subscripts, is the address to the array
        x = *p; //

        p[1] = 5; // p is still a reference to apoointer, but I get to use subscripts
        *(p+1) = 5 // identical to above
        ++p;
        P++;

-   void star

        void *p;
        int *pi;
        float * pf;

        p = pi;
        p = pf;
        pf = (float *)p;
        pi = (int *)p;

-   array addresses

        int
        main() {
            int A[10],I;
            printf("addr of i is %#x\n",&I);
            for (int i = 0; i<=10;i++) {
                printf("addr of A[%d] is %#x\n",i,&A[i]);
                A[i]=0;
            }
        }

-   strings

        char * p3 = "hello";
        char array[] = "hello";
        char a2[10] = "hello";

January 30th, 2013 - Office hours {#january-30th-2013---office-hours}
---------------------------------

-   Linux is a descendant if UNIX, which is derivative from command line
    operating systems from Bell labs.
-   The wanted a nice, modular OS.
-   There's a directory structure. Everyone has a "subtree"
-   gcc commands
-   cat - concatenate files
    -   essentially, this prints,
    -   this puts it on the screen
    -   if you put a bunch in the command, it outputs them all.
    -   you can redirect: 'cat a.c b.c d.c \> big.c\`
    -   you can append using `>>`

-   we can copy and move files around
    -   `mv ...`

-   `date` tells you the time of day and the date
-   `diff` tells you the difference between two files
-   `grep regexp [files]`
    -   this is only in the present directory

-   `find` goes through folders and files recursively
-   `man` gets a manual
-   `ls` and `mkdir [name]`
    -   `-F` will distinguish between exe, subdirectory, etc.

-   linux does not care about suffixes
-   `pg` or `more`: "I want to see the file, but it might be larger than
    my screen."
-   `ps` for "process status"
-   `rm` and `rmdir` for "remove" and "remove directory"
-   `pwd`: "I am printing the working directory"
-   `who`: who else, including you, is on the system

January 31st, 2013 - Lecture: Pointers and arrays, C functions {#january-31st-2013---lecture-pointers-and-arrays-c-functions}
--------------------------------------------------------------

-   String functions ('<string.h>')

        char * strcpy(char * s1. const char * s2); // string copy
        char * strncpy(char * s1, const char * s2, int n); // up to n bytes
        char * strcat(char * s1, const char * s2); // string concatenate
        char * strncat(char * s1, const char * s2, int n); // up to n bytes
        int strcmp(const char * s1, const char * s2); // string compare
        int strncmp(const char * s1, const char *s2, int n); // upt to n bytes
        int stricmp(const char * s1, const char *s2, int n); // case insensitive
        int strlen(const char * s); // number of bytes

    -   `strncopy` says I will copy at most `n` bytes.
    -   both of these argument pointers better be set to something valid
        in memory.

-   Something with memory

        void * memcpy(void * s1, const void * s2, int n);
        int memcmp (const void *s1, const void *s2, int n);
        void * memset (char * s1, char c, int n);

-   Header files
    -   Sample header

            #ifndef point_h
            #define point_h

            struct point {
                int x,y;
            };
            #include "other.h"
            #endif

    -   Things to put in a header file
        -   Things to share
        -   Trees, lists, something
        -   Linked list operations
        -   Definitions of nodes
        -   Types I make up, `structs`, `enums`, `typedefs`
        -   Functions I want to use

-   Dynamic memory allocation
    -   Three operations:
        1.  `malloc`
        2.  `realloc`
        3.  `free`

    -   Definitions:

            void * malloc(size_t size);
            void * realloc (void * p, size_t newsize);
            void free(void*);

February 5th, 2013 - Recitation {#february-5th-2013---recitation}
-------------------------------

-   The `include` command is used to use other code in your `.c` files,
    you include `.h` files.
-   Typical files to include are `stdio.h` and `stdlib.h` (standard
    input/output and library, respectively).

        [return_type] [function_name] ([datatype arg1, ... ) {
            [function body]
        }

-   Because C is parsed line by line, you must define a function before
    you use it otherwise it doesn't know it exists.
-   So you can make a function prototype.

        [return_type] [function_name] ([datatype arg1, ... )

-   You should include these things before `main`.
-   `fopen` and `fclose` are commands you use one `FILE`s to get
    information from them.
    -   Specify parameters for read, write, etc.

            FILE * fopen(const char * filename, const char * mode);
            FILE * fclose(const char * filename);

-   `fscanf` and `fprint`

        fscanf(FILE *fp, "%d", &age);
        fprintf(FILE *fp, "%d", age);

-   String specifiers
    -   `%d` is an integer
    -   `%f` is a float
    -   `%s` is

-   `fputs` and `puts`

        fputs(char *str, FILE *fp);
        puts(char *str);

-   `fwrite` and `fread`

        int fwrite(*buf, int size, int count, FILE *fp);

    -   `*buf` is the pointer
    -   `size` is the size of data type
    -   `count` is ...
    -   `*fp` is the file in question

-   Example

        #include <stdio>
        #include <stderr>

        main() {
            float f1, f2, f3, f4;
            file *fp;
            if ((fp = fopen("file.txt", "r")) = null) {
                fprint("stderr, "Error: could not read file. \n");
            }
            fscanf(fp, "%f %f %f %f", &f1, &f2, &f3, &f4);
            fclose(fp);
            return 0;
        }

February 5th, 2013 - Lecture: Dynamic memory management {#february-5th-2013---lecture-dynamic-memory-management}
-------------------------------------------------------

        #include <stdio.h>
        int printf(const char *, ...);
        int fprintf(FILE *, const char *, ...);
        int sprintf(char *, const char *, ...); // value of this is the length of string created
        -[character] %[-][width]c \\ %c %3c %-3c
        %[-][#][width][l]

> Don't change the program, change the goals

         int scanf(const char * fmt, ...);

-   remember, C passes by value, so pass the address of the thing you
    want to change.

February 7th, 2013 - Lecture: C preprocessor, formatted I/O {#february-7th-2013---lecture-c-preprocessor-formatted-io}
-----------------------------------------------------------

-   To print an error,

        fprintf(stderr, "fmt string", ...);

-   Some code

        size_t fread(void * ptr, size_t size, sizeIt nobj, file *);

    -   `void * ptr` is the input buffer
    -   `size_t size` is the element size
    -   `size_t nobj` is the number of objects

-   `fwrite`

        fwrite(const void * ptr, size_t size, size_t nobj, file*)

-   `getc`

        int getc(file*);
        int fgetc(file*);
        char * gets (file*)
        char * fgets(char *s, int n, file *);

    -   `fgetc` and `getc` are basically interchangable for our
        purposes.
    -   you are getting the next character from the file.
    -   `gets` wil read a string until a new line or an end of file.
        -   reading by file one line at a time.

    -   `fgets` will read a maximum of `n` characters or a new line,
        whicever ccomes first.

-   some overlap

        void rewing(file*);
        fseek(file*, ol, seek_set);
        long ftell(file*);

-   C preprocessor

        #include <stdio.h>
        #include "myheader.h

-   Macros

        #define some_id
        #define asize 100
        #define max(a,b) ((a>b ? a : b)

-   conditional compilation

        #if expression
        #elif expression
        #else
        #endif

        #ifdef some #define
        #endif
        #ifndef some #define
        #endf

February 10th, 2013 - [Notes: The ANSI C `string.h`](http://www.csse.uwa.edu.au/programming/ansic-library.html#string) {#february-10th-2013---notes-the-ansi-c-string.h}
----------------------------------------------------------------------------------------------------------------------

-   Copy ct to s including terminating `NUL`. Return s.

        char* strcpy(char* s, const char* ct);

-   Copy at most n characters of ct to s Pad with `NUL`s if ct is of
    length less than n. Return s.

        char* strncpy(char* s, const char* ct, int n);

-   Concatenate ct to s. Return s.

        char* strcat(char* s, const char* ct);

-   Concatenate at most n characters of ct to s. Terminate s with `NUL`
    and return it.

        char* strncat(char* s, const char* ct, int n);

-   Compare cs and ct. Return negative if `cs < ct`, zero if `cs == ct`,
    positive if `cs > ct`.

        int strcmp(const char* cs, const char* ct);

-   Compare at most n characters of cs and ct. Return negative if
    `cs < ct`, zero if `cs == ct`, positive if `cs > ct`.

        int strncmp(const char* cs, const char* ct, int n);

-   Return pointer to first occurrence of c in cs, or `NULL` if not
    found.

        char* strchr(const char* cs, int c);

-   Return pointer to last occurrence of c in cs, or `NULL` if not
    found.

        char* strrchr(const char* cs, int c);

-   Return length of prefix of cs consisting entirely of characters in
    ct.

        size_t strspn(const char* cs, const char* ct);

-   Return length of prefix of cs consisting entirely of characters
    *not* in ct.

        size_t strcspn(const char* cs, const char* ct);

-   Return pointer to first occurrence within cs of any character of ct,
    or `NULL` if not found.

        char* strpbrk(const char* cs, const char* ct);

-   Return pointer to first occurrence of ct in cs, or `NULL` if not
    found.

        char* strstr(const char* cs, const char* ct);

-   Return length of cs.

        size_t strlen(const char* cs);

-   Return pointer to implementation-defined string corresponding with
    error n.

        char* strerror(int n);

-   A sequence of calls to `strtok` returns tokens from s delimted by a
    character in ct. Non-`NULL` s indicates the first call in a
    sequence. ct may differ on each call. Returns `NULL` when no such
    token found.

        char* strtok(char* s, const char* t);

-   Copy n characters from ct to s. Return s. Does not work correctly if
    objects overlap.

        void* memcpy(void* s, const void* ct, int n);

-   Copy n characters from ct to s. Return s. Works correctly even if
    objects overlap.

        void* memmove(void* s, const void* ct, int n);

-   Compare first n characters of cs with ct. Return negative if
    `cs < ct`, zero if `cs == ct`, positive if `cs > ct`.

        int memcmp(const void* cs, const void* ct, int n);

-   Return pointer to first occurrence of c in first n characters of cs,
    or `NULL` if not found.

        void* strchr(const char* cs, int c, int n);

-   Replace each of the first n characters of s by c. Return s.

        void* strchr(char* s, int c, int n);

February 12th, 2013 - Recitation {#february-12th-2013---recitation}
--------------------------------

### What is GDB {#what-is-gdb}

-   GDB is a debugger that helps you debug your program.
-   The time you spend now learning gdb will save you days of debugging
    time.
-   A debugger will make a good programmer and better programmer.

### Compiling a program for GDB {#compiling-a-program-for-gdb}

-   You need to compile with the `-g` option to be able to debug a
    program with gdb.
-   The `-g` option adds debugging information to your program.

        gcc -g -o hello hello.c

### Running a program with GDB {#running-a-program-with-gdb}

-   To run a program with `gdb` type

        gdb progname
        (gdb)

-   Then set a breakpoint in the main function

        (gdb) break main

-   A breakpoint is a marker in your program to tell the porgram to stop
    and return control back to `gdb`

### Stepping through your program {#stepping-through-your-program}

-   Your porgram will start running and when it reaches `main()` it will
    stop.

        gdb>

-   Now you have the folloiwing commands to run your program step by
    step:
    -   Run the next line of code and stop, it will enter into a
        function

            gdb step

    -   Run the next line of code and stop, do not go into function

            gdb next

### Printing the Value of a Variable {#printing-the-value-of-a-variable}

-   This command prints a variable

        (gdb) print var

February 13th, 2013 - Lecture {#february-13th-2013---lecture}
-----------------------------

### Binary Numbers {#binary-numbers}

-   base 2, each digit is 0 or 1
-   Numbers are written as \\( d\_n, ..., d\_2, d\_1, d\_0 \\)
-   Value of number is computer as \\[ \_{i = 0}\^n d\_i 2\^i \\]

### Hexadecimal numbers {#hexadecimal-numbers}

-   Base 16
-   Each digit c an be one of 16 different valyes
    -   Symbols = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F}

-   Value \\[ \_{i = 0}\^n d\_i 16\^i \\]

### Octal numbers {#octal-numbers}

-   Little more awkward
-   Same basic idea, except power of 8
-   Grabbing 3 bits at a time
-   Value =

\\[ \_{i = 0}\^n d\_i 8\^i \\]

### Converting hex to binary {#converting-hex-to-binary}

-   Each hexademical digit can be represented by 4 binary digits
-   What is `0o45` in binary?
    1.  0b01000101
    2.  0b100101
    3.  0b010010

-   What is the general rule for conversion?

> Real programmers use hex

### Converting binary to hex {#converting-binary-to-hex}

-   Grab 4 bits at a time, change to corresponding digit in hex
-   Go from right to left
-   Example: `1011011110011100`

        0b1011011110011100 = 0xb79

### Decimal to binary {#decimal-to-binary}

-   What is the largest power of 2, q, r... such that \\[ n = 2\^p +
    r\_1 \\] where \\(r\_1 2\^p \\) \\[n - 2\^p = 2\^q + r\_2\\] where
    \\(\*r\_2 2\^q \\) \\[ n - (2\^p + 2\^q) = 2\^r + r\_3\\] where
    \\(r\_3 \< r\^r\\)

### Decimal and binary fractions {#decimal-and-binary-fractions}

-   In decimal, digits to the right of radix point have value \\(\^i\\)
    for each digit in the \\(i\^{th}\\) place
    -   0.25 is 2/10 + 5/100

-   Similarly, ib binary, digits to the right of radix point have value
    \\(1/2\^i\\) for each ith place
    -   Just the base is different

### Data sizes {#data-sizes}

        C           32      64
        char        1       1
        shot int    2       2
        int         4       4
        pointer     4       8

### Big endian vs. small endian {#big-endian-vs.-small-endian}

-   How toi determine value when have a sbinary number spread across
    multiple bytes

        A0 BC 00 12

    -   Is this `A0BC0012` or `1200BCA0`
        -   One is called little endian and the other is called big
            endian
        -   Makes no difference to computer architecture

    -   Why do we care?
        -   Interpret machine code and values
        -   One computer sending data to another computer
        -   Need to convert to standard before transmitting

-   **Big endian**: MSB first, decreasing numeric significiance as byte
    address increases
-   **Little endian**: LSB first, increasing numeric significane as byte
    address increase

### Representing integers {#representing-integers}

-   How do we represent negative number in computers?
    -   You use a bit

-   Signed magnitude

        0100 = 4
        0011 = 3
        1100 = -4
        1011 = -3

-   Unsigned integers n bits \\[0 ... 2\^n - 1\\]

-   Signed magnitude \\[ 10000\*{10} = 00002710\\] \\[-10000\*{10} =
    80002710 \\] \\[-2\^{n-1} ... 2\^{n-1} \\]

        00000000 = 0
        80000000 = 0

    -   This complicated the hardware because two representaitons equal
        the same thing.

-   The complelemtn

        10000_{10} = 00002710
        -10000 = FFFFD8EF

-   Two's complement

        00002710
        FFFFD8EF FLIP
        FFFFD8F0 ADD 1

        00000000
        FFFFFFFF FLIP
        00000000 ADD 1

-   You are not required to nkow these numbers

        8 bits      -128 to +127
        16 bits     -32768 to +32767
        32 bits     -2147483648 to +2147483647

-   Two's complement in n bits

    -   value \\[-d\_{n-1}2\^{n-1}
        \\]\\[\_{i=0}<sup>{n-1}d\_is</sup>i\\]
    -   range \\[ \\]

-   Some math

\\[1000\*{10} = 000003E8 = \\] \\[0x2\^{31} + 1000\*{10} = 1000 \\]

\\[-1000\_{10} = FFFFFC18\\]

### ASCII table {#ascii-table}

        DEC OCT HEX BIN Symbol  HTML Number HTML Name   Description
        0   000 00  00000000    NUL &#000;      Null char
        1   001 01  00000001    SOH &#001;      Start of Heading
        2   002 02  00000010    STX &#002;      Start of Text
        3   003 03  00000011    ETX &#003;      End of Text
        4   004 04  00000100    EOT &#004;      End of Transmission
        5   005 05  00000101    ENQ &#005;      Enquiry
        6   006 06  00000110    ACK &#006;      Acknowledgment
        7   007 07  00000111    BEL &#007;      Bell
        8   010 08  00001000     BS &#008;      Back Space
        9   011 09  00001001     HT &#009;      Horizontal Tab
        10  012 0A  00001010     LF &#010;      Line Feed
        11  013 0B  00001011     VT &#011;      Vertical Tab
        12  014 0C  00001100     FF &#012;      Form Feed
        13  015 0D  00001101     CR &#013;      Carriage Return
        14  016 0E  00001110     SO &#014;      Shift Out / X-On
        15  017 0F  00001111     SI &#015;      Shift In / X-Off
        16  020 10  00010000    DLE &#016;      Data Line Escape
        17  021 11  00010001    DC1 &#017;      Device Control 1 (oft. XON)
        18  022 12  00010010    DC2 &#018;      Device Control 2
        19  023 13  00010011    DC3 &#019;      Device Control 3 (oft. XOFF)
        20  024 14  00010100    DC4 &#020;      Device Control 4
        21  025 15  00010101    NAK &#021;      Negative Acknowledgement
        22  026 16  00010110    SYN &#022;      Synchronous Idle
        23  027 17  00010111    ETB &#023;      End of Transmit Block
        24  030 18  00011000    CAN &#024;      Cancel
        25  031 19  00011001     EM &#025;      End of Medium
        26  032 1A  00011010    SUB &#026;      Substitute
        27  033 1B  00011011    ESC &#027;      Escape
        28  034 1C  00011100     FS &#028;      File Separator
        29  035 1D  00011101     GS &#029;      Group Separator
        30  036 1E  00011110     RS &#030;      Record Separator
        31  037 1F  00011111     US &#031;      Unit Separator

### Code {#code}

        int at01(char * s) {
            int value,mult;

            if (*s == '_') {
                mult = -1;
                ++s;
            } else if (*s == '+') {
                mult = 1;
                ++s;
            } else {
                mult = 1;
            }

            value = 0;

            while (isdigit(*s)) {
                value = 10*value + (*s - '0');
                ++s;
            }

            return mult * value;
        }

### IEEE floating point standard {#ieee-floating-point-standard}

-   Most computer follow IEEE 754 standard
    -   Single precision
        -   32 bits
        -   1 bit for sign, 8 bits for exponent, 23 bits for mintissa
        -   Has two zeroes

    -   Double precision
        -   64 bits

    -   Extended precision
        -   80 bits

February 12th, 2013 - [Singly Linked List Implementation](http://www.cprogramming.com/snippets/source-code/singly-linked-list-insert-remove-add-count) {#february-12th-2013---singly-linked-list-implementation}
------------------------------------------------------------------------------------------------------------------------------------------------------

        #include<stdio.h>
        #include<stdlib.h>
         
        struct node
        {
            int data;
            struct node *next;
        }*head;
         
        void append(int num)
        {
            struct node *temp,*right;
            temp= (struct node *)malloc(sizeof(struct node));
            temp->data=num;
            right=(struct node *)head;
            while(right->next != NULL)
            right=right->next;
            right->next =temp;
            right=temp;
            right->next=NULL;
        }
         
        void add( int num )
        {
            struct node *temp;
            temp=(struct node *)malloc(sizeof(struct node));
            temp->data=num;
            if (head== NULL)
            {
            head=temp;
            head->next=NULL;
            }
            else
            {
            temp->next=head;
            head=temp;
            }
        }
        void addafter(int num, int loc)
        {
            int i;
            struct node *temp,*left,*right;
            right=head;
            for(i=1;i<loc;i++)
            {
            left=right;
            right=right->next;
            }
            temp=(struct node *)malloc(sizeof(struct node));
            temp->data=num;
            left->next=temp;
            left=temp;
            left->next=right;
            return;
        }
         
        void insert(int num)
        {
            int c=0;
            struct node *temp;
            temp=head;
            if(temp==NULL)
            {
            add(num);
            }
            else
            {
            while(temp!=NULL)
            {
                if(temp->data<num)
                c++;
                temp=temp->next;
            }
            if(c==0)
                add(num);
            else if(c<count())
                addafter(num,++c);
            else
                append(num);
            }
        }
         
        int delete(int num)
        {
            struct node *temp, *prev;
            temp=head;
            while(temp!=NULL)
            {
            if(temp->data==num)
            {
                if(temp==head)
                {
                head=temp->next;
                free(temp);
                return 1;
                }
                else
                {
                prev->next=temp->next;
                free(temp);
                return 1;
                }
            }
            else
            {
                prev=temp;
                temp= temp->next;
            }
            }
            return 0;
        }
         
        void  display(struct node *r)
        {
            r=head;
            if(r==NULL)
            {
            return;
            }
            while(r!=NULL)
            {
            printf("%d ",r->data);
            r=r->next;
            }
            printf("\n");
        }
         
        int count()
        {
            struct node *n;
            int c=0;
            n=head;
            while(n!=NULL)
            {
            n=n->next;
            c++;
            }
            return c;
        }
         
        int  main()
        {
            int i,num;
            struct node *n;
            head=NULL;
            while(1)
            {
            printf("\nList Operations\n");
            printf("===============\n");
            printf("1.Insert\n");
            printf("2.Display\n");
            printf("3.Size\n");
            printf("4.Delete\n");
            printf("5.Exit\n");
            printf("Enter your choice : ");
            if(scanf("%d",&i)<=0){
                printf("Enter only an Integer\n");
                exit(0);
            } else {
                switch(i)
                {
                case 1:      printf("Enter the number to insert : ");
                         scanf("%d",&num);
                         insert(num);
                         break;
                case 2:     if(head==NULL)
                        {
                        printf("List is Empty\n");
                        }
                        else
                        {
                        printf("Element(s) in the list are : ");
                        }
                        display(n);
                        break;
                case 3:     printf("Size of the list is %d\n",count());
                        break;
                case 4:     if(head==NULL)
                        printf("List is Empty\n");
                        else{
                        printf("Enter the number to delete : ");
                        scanf("%d",&num);
                        if(delete(num))
                            printf("%d deleted successfully\n",num);
                        else
                            printf("%d not found in the list\n",num);
                        }
                        break;
                case 5:     return 0;
                default:    printf("Invalid option\n");
                }
            }
            }
            return 0;
        }

February 12th, 2013 - Programming Assignment 2: Data Representation and Computer Arithmetic {#february-12th-2013---programming-assignment-2-data-representation-and-computer-arithmetic}
-------------------------------------------------------------------------------------------

### Introduction {#introduction-1}

This assignment is designed to help you learn the representation,
interpretation, and manipulation of data as bits. There are two parts.
In the first part, you will implement a program calc to add and subtract
numbers specified in different bases (multiplication is extra credit).
In the second part, you will implement a program format that will print
the decimal values of bit sequences representing integer and floating
point data types.

### Numeric Base Conversion and Calculator {#numeric-base-conversion-and-calculator}

Implement a program called calc with the following usage interface:

        calc <op> <number1> <number2> <output base>

The first argument, `<op>`, is either the string `+`, for addition, or
`-`, for subtraction. If you want to implement multiplication, then
`<op>` can also be the string `*`. (If you do implement multiplication,
make sure to say so in your readme.pdf file so that the TAs know to
check your program for this functionality.) The next two arguments,
`<number1>` and `<number2>` are integers of arbitrary size. Each of
these numbers will be given in the form of:

        −?(b|o|d|x)d_n d_{n−1} ...d_1 d_0 

which can be interpreted as: a number can optionally start with a `−`
sign, followed by a base indicator, where `b` means the number is a
binary number, `o` means octal, `d` means decimal, and `x` means
hexadecimal. \\(d\_nd\_{n−1}...d\_1d\_0 \\) are the digits of the
number.

The final argument, `<output base>`, gives the base that the resulting
number should be printed out in. Like the base indicator for the input
numbers, this argument can be one of four strings: `b` for binary, `o`
for octal, `d` for decimal, and `h` for hexadecimal. Your program should
output the answer in the same form as the input numbers (that is, the
output number should follow the regular expression given above). Some
examples:

        $ ./calc + d1111111111111111 d1111111111111111 d
        d222222222222222
        $ ./calc + b1101 b1 d
        d14
        $ ./calc + d999999999 d1 d
        d1000000000
        $ ./calc - d10 -d4 b
        b1110
        $ ./calc + -d10 -d4 b
        -b1110

**Note**: The numbers in the first example are too large to fit in a
32-bit integer type in C; this is why the arbitrary size is emphasized
above. Using a 64-bit integer type is not the solution since the input
integers can be arbitrarily large. Rather, you need to design data
structures and algorithms that can handle arbitrarily large numbers.

**Assignment update**: any decimal number that we ask you to
handle—either an input decimal number or output in decimal format—will
be less than a 32-bit integer. Important: You must write the base
conversion code yourself. You may not use type-casting, libraries, or
output formats in printf(). You may use standard C arithmetic
operations. You may use the C standard libraries for functionality not
related to the conversion (e.g., string handling functions).

**Important**: If calc detects an error in the inputs, it should print
out an error message that starts with the string “ERROR”, followed by a
string that gives an informative message about the error that it
detected.

### Format Interpretation {#format-interpretation}

Implement a program called format with the following usage interface:
format `<input bit sequence> <type>` The first argument,
`<input bit sequence>`, is a sequence of 32 bits. Remember that your C
program will get it as a string of 1 and 0 characters in the `argv[1]`
argument to main. This sequence of bits represents the binary values
stored in 4 contiguous bytes in memory. The leftmost bits are stored in
the byte with the smallest address while the rightmost bits are stored
in the byte with the largest address. The second argument, `<type>`,
gives the type that you should use to interpret the input bit sequence,
and can be either int (integer) or float. The formats for the input bit
sequence is as follows. If the type is: int: the format is two’s
complement; float: the format is IEEE 74 single precision; Note that the
input bit sequence can correspond to negative numbers.

Your program should print out the decimal representation of the input
bit sequence, assuming a big endian byte ordering. Floating point
numbers should be printed in scientific notation, where a number 1.5x105
would be printed as 1.5e5. For positive infinity, output pinf, for
negative infinity, output ninf, and for “NaN”, output NaN. Here are some
examples:

        $ ./format 01000001010000100100001101000100 int
        1094861636
        $ ./format 10000001010000100100001101000100 int
        -2126363836
        $ ./format 01000001010000100100001110000100 int
        1094861700
        $ ./format 00000000000000000000000000000001 int
        1
        $ ./format 01000000110000110100001111010100 float
        6.10203e0
        $ ./format 00111010000111111111011000001000 float
        6.1e-4
        $ ./format 10000000000000000000000000000000 float
        -0.0e0
        $ ./format 01000000010010010000111111011011 float
        3.141593e0

Important: You must write the interpretation code yourself. You may not
use type-casting, libraries, or output formats in printf(). You may use
standard C arithmetic operations. You may use the C standard libraries
for functionality not related to the value interpretation (e.g., string
handling functions). Important: If format detects an error in the
inputs, it should print out an error message that starts with the string
“ERROR”, followed by a string that gives an informative message about
the error that it detected. For this program, you can assume that any
input bit sequence that is shorter or longer than 32 bits is erroneous.

### Submission {#submission-1}

You have to e-submit the assignment using Sakai. Your submission should
be a tar file named pa2.tar that can be extracted using the command:

        tar xf pa2.tar

Your tar file must contain: + A sub-directory named calc. calc must
contain: – readme.pdf: this file should describe your design and
implementation of the calc pro- gram. In particular, it should detail
your design, any design/implementation challenges that you ran into, and
an analysis (e.g., big-O analysis) of the space and time perfor- mance
of your program. – Makefile: there should be at least two rules in this
Makefile: calc build your calc executable. clean prepare for rebuilding
from scratch. – source code: all source code files necessary for
building calc. At a minimum, this should include two files, calc.h and
calc.c. + A sub-directory named format. format must contain: –
readme.pdf: this file should describe your design and implementation for
the format program. In particular, it should detail your design, any
design/implementation chal- lenges that you ran into, and an analysis
(e.g., big-O analysis) of the space and time performance of your
program. – Makefile: there should be at least two rules in your
Makefile: format build your format executable. clean prepare for
rebuilding from scratch. – source code: all source code files necessary
for building format. At minimum, this should include two files, format.h
and format.c. We will compile and test your program on the iLab machines
so you should make sure that your program compiles and runs correctly on
these machines. You must compile all C code using the gcc compiler with
the -ansi -pedantic -Wall flags.

### Grading Guidelines {#grading-guidelines-1}

#### Functionality {#functionality-1}

This is a large class so that necessarily the most significant part of
your grade will be based on programmatic checking of your program. That
is, we will build a binary using the Makefile and source code that you
submitted, and then test the binary for correct functionality against a
set of inputs. Thus: + You should make sure that we can build your
program by just running make. + You should test your code as thoroughly
as you can. In particular, your code should be adept at handling
exceptional cases. Be careful to follow all instructions. If something
doesn’t seem right, ask.

#### Design {#design-1}

Having said the above about functionality, design is a critical part of
any programming exercise. In particular, we expect you to write
reasonably efficient code based on reasonably performing algorithms and
data structures. More importantly, you need to understand the
performance (time & space) implications of the algorithms and data
structures you chose to use. Thus, the explanation of your design and
analyses in the readme.pdf will comprise a non-trivial part of your
grade. Give careful thoughts to your writing of this file, rather than
writing whatever comes to your mind in the last few minutes before the
assignment is due.

#### Coding Style {#coding-style-1}

Finally, it is important that you write “good” code. Unfortunately, we
won’t be able to look at your code as closely as we would like to give
you good feedback. Nevertheless, a part of your grade will depend on the
quality of your code. Here are some guidelines for what we consider to
be good: - Your code is modularized. That is, your code is split into
pieces that make sense, where the pieces are neither too small nor too
big. - Your code is well documented with comments. This does not mean
that you should comment every line of code. Common practice is to
document each function (the parameters it takes as input, the results
produced, any side-effects, and the function’s functionality) and add
comments in the code where it will help another programmer figure out
what is going on. - You use variable names that have some meaning
(rather than cryptic names like i). Further, you should observe the
following protocols to make it easier for us to look at your code: -
Define prototypes for all functions. - Place all prototype, typedef, and
struct definitions in header (.h) files. • Error and warning messages
should be printed to stderr using fprintf.

February 13th, 2013 - Office hours {#february-13th-2013---office-hours}
----------------------------------

-   Exceptions are bad.
-   `strcasecmp` is fine.
-   A buffer of 128 bytes is fine.

February 15th, 2013 - Wordstat Readme {#february-15th-2013---wordstat-readme}
-------------------------------------

### Data Structures {#data-structures}

The overarching design philosophy I have is object-oriented in
perspective. I designed my `struct`s to behave like objects, with the
following properties:

-   Every structure is contained in its own header file.

-   Every structure has helper functions that handle allocating of
    memory.

-   Every structure has helper functions which “put” and “get”
    references.

This allowed the main function to work as a *tour de force*, where
nothing is defined and everything is used.

The short hand version of my implementation is: a balanced character BST
of ‘a’ through ‘z’ with a nested BST of case insensitive words with a
nested linked list of case sensitive word.

#### `struct char_tree_node` {#struct-char_tree_node}

This is my foundational data structure. It is a binary search tree which
is loaded with character ‘a’ through ‘z’. They’re loaded in such a way
that this particular tree ends up being balanced. Here’s a
representation of the tree after the function `bld_char_tree` is called:

##### `char letter` {#char-letter}

Represents the character which this node is responsible for. Every word
in the subtree, defined later in this document, will begin with this
character.

##### char\_tree\_node *left, *right {#char_tree_node-left-right}

These represent the edges between two nodes, forming a tree structure.

##### `word_tree_node *words` {#word_tree_node-words}

This points to a struct which is another nested binary search tree.

#### `struct word_tree_node` {#struct-word_tree_node}

Every character node has a word node. A word node is the principal store
for information of the statistic of a document. Any given word tree is
limited to words which begin with a single character, by virtue of its
“parent” structure, the character tree.

In order to make processing simple, the word tree is stored in its own
file with a header which defines convenience functions for allocation,
insertion, and retrieval.

##### `char *case_insensitive_word` {#char-case_insensitive_word}

This string stores the word that this node is representing. It is case
insensitive in that it may change the case when it is inserted or it may
not, but when used you should disregard any case information.

As the spec dictates, this stores any sequence of letters and digits
that starts with a letter, followed by 0 or more letters and/or digits.

##### `int total_instances` {#int-total_instances}

This integer is the number of time that `case_insensitive_word` has
appeared in total. It is case-insensitive instances.

When outputted, this will be called “Total No. Occurrences.”

##### struct word\_tree\_node *left, *right {#struct-word_tree_node-left-right}

So as to create a tree structure, these pointers represent a left and
right, where every sub-tree to the left contains values strictly smaller
than the root, and everything to the right is strictly greater than
root.

The “number” of a string is determined lexicographically.

##### `int cases_instances` {#int-cases_instances}

Closely linked with the `struct` defined below, this number represents
the number of case-sensitive variations on the word this node represents
exist in the document.

When outputted, this will be called “No. Case-Sensitive Versions.”

##### struct word\_list\_node \*case\_sensitive\_list {#struct-word_list_node-case_sensitive_list}

This is a singly-linked-list which is defined below.

#### `struct word_list_node` {#struct-word_list_node}

Every character has a node in a tree. Every character node has a tree of
case-insensitive words. Every case-insensitive node has a case-sensitive
singly-linked-list.

##### `char *case_sensitive_word` {#char-case_sensitive_word}

A string which is case-sensitive, used to compare against when deciding
if this is a new or previously discovered case instance.

##### `struct word_list_node *next` {#struct-word_list_node-next}

A linked-list needs a pointer to the next element in the list.

### Big-O Analysis {#big-o-analysis}

#### Space complexity {#space-complexity}

Where *r* is the number of words in a text,
*n*<sub>0</sub>, *n*<sub>1</sub>, . . . *n*<sub>*t*</sub> represents the
set of case-insensitive words, and
*m*<sub>0</sub>, *m*<sub>1</sub>, . . . , *m*<sub>*t*</sub> represents
the number of case-sensitive variations on each corresponding *t* word.

-   The character tree requires 26 × 8 bytes for the characters.

-   Each word tree node’s case-insensitive string requires the number of
    bytes of each of the *n* words.

-   Each word list node’s case-sensitive string requires the number of
    bytes of each of the *m* case-sensitive variations.

The “specific” space is:

*O*(∑ <sub>0</sub><sup>*r*</sup>*n*<sub>*r*</sub> + *m*<sub>*r*</sub>)

The worst case is a double-nested linear time, along with every single
case being unique, resulting in:

*O*(*n*<sup>3</sup>)

#### Time complexity {#time-complexity}

##### Worst case {#worst-case}

Where we count assignments and steps with *n* words:

-   If every word in the document begins with a letter at the bottom of
    the character tree, there will be +4 assignments to get the
    character. Say every word begins with the same one.

-   If every word is lexicographically greater than the previous one or
    lexicographically less the previous one, you end up with a
    “linked-list.”

-   If every word is a unique case-variation, you have to step through
    the whole-linked list every time.

*O*(*n*<sup>3</sup>)

##### Best case {#best-case}

-   Every word begins with ‘p’

-   The nested word tree ends up being balanced

-   Every case is the same

This makes the runtime equal to the best case of insert on a BST. Where
*n* is the number of words:

*O*(log(*n*))

### Challenges {#challenges}

#### Functionality {#functionality-2}

The functionality of the program was difficult to write in that it was a
totally new language for me. This was ameliorated somewhat because I
have developed for iOS in Objective-C, in a version of iOS before
automatic reference counting.

Admittedly, I’m still uncertain about what the proper way to both keep
declarations and operations separate (as the C90 standard dictates), and
still keep complex operations from being complicated one-liners.

#### Coding Style and Design {#coding-style-and-design}

I struggled with what the best way to use C as C is. What I mean is my
solution pastes onto functional programming an object-oriented mindset.
I am still uncertain as to what veteran C programmers would do to solve
this problem. I think that this will be lessened as the semester
continues. In this one experience, however, I have come to like C more
than Java. Objective-C holds a special place in my heart, however.

February 18th, 2013 - Recitation {#february-18th-2013---recitation}
--------------------------------

### Decimal to Binary {#decimal-to-binary-1}

    _   _   _   _   _  
    2^4 2^3 2^2 2^1 2^0

### Binary to Decimal {#binary-to-decimal}

    1   0   0   1   0
    2^4 2^3 2^2 2^1 2^0

    2^4 = 16
    2^1 = 2
    ____+___
          18

### Hex to Binary {#hex-to-binary}

The general algorithm is to convert each individual number into binary,
and then concatenate the results.

    2   A   8   C

    2 -> 0010
    A -> 1010
    8 -> 1000
    C -> 1100
    ____+____
    0001001001011010

#### Hex alphabet values {#hex-alphabet-values}

    A -> 10
    B -> 11
    C -> 12
    D -> 13 
    E -> 14
    F -> 15

February 18th, 2013 - Lecture {#february-18th-2013---lecture}
-----------------------------

    _______
    7     0

    _______________
    15            0

    _______________________________
    31                            0

-   The byte ordering in the real world starts with the most
    significiant and ends with the least significant.

### Left shifting {#left-shifting}

-   A byte to shift on and a direction.
-   It can be evrything but negative.
-   Shfiting by zero is nothing is changing.
-   Sometimes your calcuation is dynamically shifting based on some
    information, which could result in zero.
-   If in 32 bit quantity 0 is our least significant and 31 is the most,
    then shifting to the left yields to the left bit being lost (?)
-   In C operators are `<<` and `<<=`
-   Shifting left n bits is exactly euivilent to mutiplying 2\^n
    -   if you want a nice way to multiply something by two, this is
        ideal.

            //__ these two bits get discarded
                0000 1000 << 2
                0010 0000
                   //^^ these two bits get zeroes

-   If I had a 32 bit number, you'd just move the "thrown out stuff"
    into 64 bits, else you lose information.
-   If you shift an n bit number by n, it results in 0.

### Right shift {#right-shift}

#### Logical {#logical}

-   This means our new high bits are zero, including sign.

#### Arithmetic {#arithmetic}

-   Preserves sign, if you shift a negative number, it wont discard the
    last bit.

### Bitwise operations {#bitwise-operations}

-   **And**: C operator is `&`

        1100
        1011
        &___
        1000

    -   This is all the posibilites for a single bit, evidently.
    -   They both have to be one. They both have to be one.
    -   This is comparing numbers to their respective others in the
        other number and returning a number which represents where they
        are both one, or there is at least one zero.

-   **Or**: C operator is `|`

        1100
        1010
        |___
        1110

    -   Just like the last operation, but the result is or.
    -   This means only and at least on of the bits must be one for the
        final bit to be one.

-   Exclusive or: C operator is `^`

            1100
        ^ 1010
        ______
          0110

-   **Not** C operator is `~`

        ~10
         01

### DeMorgan's Law {#demorgans-law}

        A || B = !(!A && !B)
        A && V = !(!A || !B)

### Using two's complement {#using-twos-complement}

-   Do x and y have the same sign?

        (x^y) < 0

### Swapping fixed-point x and y {#swapping-fixed-point-x-and-y}

        x ^= y
        y ^= x
        x ^= y

### Rotation {#rotation}

        unsigned int rshift (unisgned int val, unisgned int n) {
            unisgned int intsize = sizeof(int)*8;

            if (n == 0)
                return;
            else {
                return value >> n | value << (intsize - n);
            }
        }

February 20th, 2013 - Lecture {#february-20th-2013---lecture}
-----------------------------

-   CPU
    -   ALU
    -   Control logic
    -   PC (Instruction Pointer)
    -   Registers
    -   Condition Codes

-   Memory
    -   OS code and data
    -   Object code
    -   Program data

### Memory {#memory}

-   I've got these buses which I communicate addresses through from the
    CPU to the memory.
-   "Go to address 3 and read"
-   Go to address 4 and write.

### Processes: ALU and Registers {#processes-alu-and-registers}

-   There are functions on operarnds A nd B

### Why do we need registers? {#why-do-we-need-registers}

-   (iCQ): The register file looks just like a mini-memory

### Basic CPU function {#basic-cpu-function}

1.  Fetch[PC++]
2.  Decode
3.  Execute
4.  See 1.

### Assembly characteristics {#assembly-characteristics}

-   Minimal data types
    -   Integer data of 1, 2, or 4 bytes
        -   Data values
        -   Addresses

    -   Floating point data of 4, 8, or 10 bytes
    -   No aggregate types such as arrays or structures
        -   Just continuosly allocated bytes in memory.

-   No type checking
    -   Interpretation of data format depends on instruction
    -   No protection against misinterpretation of data

-   There's the idea of a process
    -   Every program is running in its own virtual address space
    -   If I do something and I can read only the stuff on my process

-   Primitive operationnnnnns
    -   Perform arithmattttic function or memory data
    -   Transfer data between memory and regggister
        -   Load data from memory into register

### x86 Characteristic {#x86-characteristic}

-   Variable length between 1 and 15 bytes
-   Can address memory directly in most instructions
-   Uses little endian format

### `MOV` instruction {#mov-instruction}

-   Most common instruction is data transfer instruction
    -   `mov s, d`
        -   Copy value at S to D

-   Used to copy data from:
    -   Memory to register
    -   Register to memory
    -   Register to register
    -   Constant to register
    -   Constant to memory

-   Registers

                         +-----------------------------+
                         | 32 bit| 16 bit    |   8 bit |
                         +-------+-----------+---------+
                         | %eax |   %ax     |   %ah   |
                         | %ebx |   %bx     |   %bh   |
                         | %ecx |   %cx     |   %ch   |
                         | %edx |   %dx     |   %dh   |
                         | %ebp |   %bp     |   %ac   |
        points to stack->| %esp |   %sp     |   %bc   |
        program counter->| %eip |   %ip     |   %cc   |
        seg addressing ->| %esi |   %si     |   %dl   |
                         +-------+-----------+---------+

             +-----------------------------------+
             |                    +-------------+|
        %eax |                 %ax|%ah   |  %al || 
             |                    +-------------+|
             +-----------------------------------+
             31                   15             0

### A little bit about the stack {#a-little-bit-about-the-stack}

-   I am pushing and popping individual values on this stack, a word
    byte
-   Double word, quad work.
-   1, 2, 4 eight byte values.
-   From the stack I can build a call stack, indivudal values for all I
    need for a particular function invocation.
-   "Call brain" or "activation brain"
-   With the intel arch, a few things to take away:
    -   Grow towards smaller addresses
    -   `%esp` always points to the top
    -   When we push to the stack, we do it in two steps:
        1.  Decrement `%esp` register by 4, has an address in it.
        2.  Copy whatever operand to wherever the `%esp` pointer points.

    -   Pop
        1.  Copy that value, wherever you're going to take it.
        2.  Add 4 to `%esp`

### Instructions {#instructions}

-   An assembly program is just an ASCII file.
-   You make it in text editors.
-   An assembly program is a sequence of assembly instructions.
-   The general form of the assembly instruction is the neumonic which
    is intented, and then operands.
-   The neumonic defines the operation.
-   There may be zero or more operands depending on the operation.
-   Multiple operands are seperated by commas.
-   Instructions:

        movb    movsbw    movzbw
        movw    movsbl    movzbl
        movl    movswl    movswl
        movq    movswq    movswq
                movslq    movslq

February 26th, 2013 - Recitation {#february-26th-2013---recitation}
--------------------------------

### Binary number to floating point numbers {#binary-number-to-floating-point-numbers}

-   Lets assume we have 0.625 in the decimal system.
-   We use a linear array

         __    __    __     __    __    __
        |  |  |  |  |  |   |  |  |  |  |  |
        |__|  |__|  |__| . |__|  |__|  |__|
        2^3   2^1   2^0    2^-1  2^-2  2^-3

February 26th, 2013 - Lecture: Assembly Language Programming {#february-26th-2013---lecture-assembly-language-programming}
------------------------------------------------------------

> How are you? <cite>Student</cite> Not dead yet. <cite>Brian
> Russel</cite>

### Indexed Mode Addressing {#indexed-mode-addressing}

-   Add content of two registers to get address of operand

        movl (%eab, %esi), %eax
        // Copy value at address = eab + esi into eax
        movl 8(%eab, %esi), %eax
        // Copy value at address = 8 + eab + esi into eax

-   Useful for dealing with arrays
-   Autovariables and formal parameters are treated pretty much the
    same.

### Address Computation Examples {#address-computation-examples}

        %edx   0xf0000
        %ecx   0x100
        
        Expression    Computation      Adress
        0x8 (%edx)    0xf0000 + 0x8    0xf008

February 28th, 2013 - Lecture {#february-28th-2013---lecture}
-----------------------------

### Some Arithmetic Operations {#some-arithmetic-operations}

    Instruction      Computation
    adll  Src,Dest   Dest = Dest +  Src
    subl  Src,Dest   Dest = Dest -  Src
    imull Src,Dest   Dest = Dest *  Src
    sall  src,Dest   Dest = Dest << Src (left shift)

    sarl  Src,Dest   Dest = Dest >> Src (right shift)
    xorl  Src,Dest   Dest = Dest ^  Src
    andl  Src,Dest   Dest = Dest &  Src
    orl   Src,Dest   Dest = Dest |  Src

March 1st, 2013 - Notes: [IEEE 754](http://en.wikipedia.org/wiki/Single-precision_floating-point_format#IEEE_754_single-precision_binary_floating-point_format:_binary32) {#march-1st-2013---notes-ieee-754}
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

        sign           exponent (8 bits)            fraction (23 bits)
        +--+    +--++--++--++--++--++--++--++--+    +--+          +--+
        |01|    |02||03||04||05||06||07||08||09|    |10|    ...   |23|
        +--+    +--++--++--++--++--++--++--++--+    +--+          +--+
        

( − 1)<sup>sign</sup> × 
(1 + ∑ <sub>*i* = 1</sub><sup>23</sup>*b*<sub>23 − *i*</sub>2<sup> − *i*</sup>)
 × 2<sup>(*e* − 127)</sup>

March 5th, 2013 - Lecture {#march-5th-2013---lecture}
-------------------------

-   Flags

        cf  carry
        zf  zero
        sf  sign
        of  overflow

-   You can think of the compare as a "non destrutive subtraction."

        cmp  [b w l q] src,dst
        test [b w l w] src,dst

-   These, evidently, are not very interesting bu we need to know them
    anyway.
-   A column of "conditional jumps" to some target, the target being
    some lable we can specify in the program.

        ==          je
        !=          jne
        signed >    jg
        unsigned >  ja
        signed <    jl
        unsigned <  jb
        signed <=   jle
        unsigned <= jbe

-   Negatives

        negative?       js
        not negative?   jns

-   Jumps
    -   Direct

            jmp .l37 (?)

-   if-else

        movl    12(%ebp),%edx
        cmp     $3,%edx
        jne     elsepart
        .
        .
        .
        jmp     done
        elsepart:
        .
        .
        .
        done

-   more code

        movl    12(%ebp),%edx
        test    8(%ebp), %edx
        jz      elsez
        .
        .
        .
        jmp     donez

-   for loop

        top:
            movl    $i, %eax
            jge     done
            .           -+
            .            | body of loop
            .           -+
            inc     %eax
            jmp     top
        done:

-   condition flags

        ==          zf
        !=          ~zf
        signed >    ~(sf^of)&~zf
        unsigned >  ~cf & ~zf
        signed >=   ~(sf^of)
        unsigned <= ~cf
        signed <    sf^of
        unsigned <  cf

March 8th, 2013 - Calc and Format Readme {#march-8th-2013---calc-and-format-readme}
----------------------------------------

### Calc {#calc}

#### Design and Implementation {#design-and-implementation}

-   My design uses a string as the primary data structure.
-   When numbers are inputted, no matter what the are, they go through
    this process:
    1.  Parse their "metadata" - length, are the negative, base;
    2.  Send their string to the relevant helper function to conversion,
        which convert it to binary;
    3.  Decide based on metadata how to add or use two's complement
        subtraction;
    4.  Based on the requested output format, send the string to the
        relevant helper function for conversion;
    5.  Print.

-   I picked this because I believe that linked list are too difficult
    to traverse, data types have to little room (and are against spec),
    and it isn't really sensible to talk about hash tables or trees in
    this context.
-   My alogrithm can handle arbintraily large hex, octal, and binary
    input and output.
-   This ended up being a good method for binary, octal, and hexadecimal
    addition and manipulation, but very poor for decimal.
    -   The decimal input and output is limited to 128 bytes, as a
        `long double` is used.

#### Challenges {#challenges-1}

-   Time became a huge concern. I wrote one implementation using
    integers after that was given the okay, but having learned that this
    would not receive full credit I set about on the more ambitious
    route.
    -   Ultimate I think this will lower my grade, but I learned enough
        along the way to justify the expense.
    -   I think this is a good investment because it will serve me
        better in the future and on exams.
    -   I did not get `format` done for this reason.

-   Decimal is a terrible number system for computers, or at very least
    how computers operate presently.
    -   I could not find an algorith to go to or from binary and decimal
        that could handle arbitrily large input.

#### Analysis {#analysis}

##### Space {#space}

-   The space is linearly related to the input.
-   The only space that is allocated is for three strings: input one,
    input two, and output.
-   The results in a space complexity 2*n* in the worst case, if input
    makes for a long binary string.

*O*(*n*)

##### Time {#time}

-   Small and linear operations are performed while processing.
-   Parsing as an activity rarely leads to anything other than linear.
    -   In processing, there are no nested for loops or anything that
        would make it exponential, quadratic.

*O*(*n*)

#### Test cases {#test-cases}

##### Conversions to binary {#conversions-to-binary}

Conversions to binary have been flawless in every tested case. The
family of functions which do the conversion are rigorous and basic. My
internal representation of *every* number is a binary string, so these
functions are core to my functionality.

    char * oct_to_bin (char * oct);
    char * dec_to_bin (char * dec);
    char * hex_to_bin (char * hex);

Now for some examples!

###### Binary {#binary}

    Inputted    111111111111111111111111111111111
    Expected    111111111111111111111111111111111
    Actually    111111111111111111111111111111111

    Note: MAX_INT

Binary is successful 100% of the time because I'm being fed a binary
string representation and my internal representation is a string.
Granted that the computer does not run out of memory and I parsed my
input correctly, this will never, ever break.

###### Octal {#octal}

    Inputted    7654321
    Expected    111110101100011010001
    Actually    111110101100011010001

The conversion algorithm that I used to convert octal to my internal
binary string representation is "grabbing" 1 binary bit at a time in
input and 3 bits at a time on output.

This approach has yielded a 100% success rate so far.

###### Decimal {#decimal}

    Inputted    987654321
    Expected    111010110111100110100010110001
    Actually    111010110111100110100010110001

While this superficially seems to work, it has a dark secret. It uses
`atoi` and an `int` to do the conversion. As with output, I could not
find or invent an algorithm to consistently convert decimal to binary or
the other way around.

If decimal is selected as an option on either input or output, then
arbitrarily large numbers are not possible.

###### Hexademical {#hexademical}

    Inputted    FEDCBA987654321
    Expected    111111101101110010111010100110000111011001010100001100100001
    Actually    111111101101110010111010100110000111011001010100001100100001

    Note: more that 32 bit

Hexadecimal is performed the same as octal, for both input and output,
except I "grab" 4 bits at a time on output.

##### Addition {#addition}

-   When both are not negative and you're adding, I add the values and
    display it

        ./calc + d10 d10 d
        -d20

-   Neither are negative and you're adding, so I add and do not display
    as negative.

        ./calc + -d200 -d200 d
        -d400

-   Number one is negative
    -   Neither number has a greater absolute value

            ./calc + -h999 h999 d
            d0

    -   The first number has a greater absolute value

            ./calc + -d1000 d125 d
            -d875

    -   The second number has a greater absolute value

            ./calc + -d1000 d1250 d
            d250

-   Number two is negative
    -   Neither number has a greater absolute value

            ./calc + o765 -o765 h
            h0

    -   The first number has a greater absolute value

            ./calc + d1350 -d1250 d
            d100

    -   The second number has a greater absolute value

             ./calc + d1000 -d1250 d
            -d250

##### Subtraction {#subtraction}

-   Both numbers are negative
    -   but neither number has a greater absolute value, so zero

            ./calc - -h1250 -h1250 o
            o0

    -   and the first has a greater absolute value to the first

            ./calc - -d1250 -d100 d
            -d1150

    -   The second has a greater absolute value to the first

            ./calc - -d1250 -d10000 d
            d8750

##### Binary {#binary-1}

    Inputted    ./calc + d1111111 d1111111 b
    Expected    b1000011110100010001110
    Actually    b1000011110100010001110

##### Octal {#octal-1}

    Inputted    ./calc + d1111111 d1111111 o
    Expected    o10364216
    Actually    o10364216

##### Hexadecimal {#hexadecimal}

    Inputted    ./calc + hFFFFFFFFFFFFFFFFFFFF hFFFFFFFFFFFFFFFFFFFF h
    Expected    h1FFFFFFFFFFFFFFFFFFFE
    Actually    h1FFFFFFFFFFFFFFFFFFFE

### Format {#format}

#### Design and Implementation {#design-and-implementation-1}

-   Very basic, I take ints and mask them into an int, and then form a
    string from that int for output.
-   Format float does not work.

#### Challenges {#challenges-2}

-   Time was a massive concern.

#### Analysis {#analysis-1}

##### Space {#space-1}

*O*(*c*)

##### Time {#time-1}

*O*(*c*)

March 12th, 2013 - Lecture {#march-12th-2013---lecture}
--------------------------

### Topics {#topics-1}

-   IA32 stack disciple
-   Register saving conventions
-   Creating pointers to local variables

### Push instructions {#push-instructions}

-   16 bits

        pushw   reg16   %esp-=2 %reg16->(%esp)
        pushl   mem16   %esp-=2 %reg16->(%esp)
        pushl   imm16   %esp-=2 %imm16->(%esp)

-   32 bits

        pushw   reg32   %esp-=4 %reg32->(%esp)
        pushl   mem32   %esp-=4 %reg32->(%esp)
        pushl   imm32   %esp-=4 %imm32->(%esp)

-   64 bits (quad words)

        pushw   reg32   %esp-=4 %reg32->(%esp)
        pushl   mem32   %esp-=4 %reg32->(%esp)
        pushl   imm32   %esp-=4 %imm32->(%esp)   

### Pop instructions {#pop-instructions}

-   16 bits

        popw    reg16   (%esp)->reg16,  %esp+=2 
        popw    mem16   (%esp)->mem16,  %esp+=2

-   32 bits

        popl    reg32   (%esp)->reg32,  %esp+=4 
        popl    mem32   (%esp)->mem32,  %esp+=4

-   64 bits

        popq    reg64   (%esp)->reg64,  %esp+=8
        popq    mem64   (%esp)->mem64,  %esp+=8

### Discussion {#discussion}

-   If you push your bytes, pop your bytes.
-   The call stack frames, or activation records.
    -   Each stack frame corresponds to each function call in C.
    -   The stack frame contains space for formal parameters and
        automatic variables.
        -   If I have a recursive function, every formal parameter gets
            a seperate space with a seperate activation record.

    -   We are not limited to 2, 4, 8 bytes.
    -   Each stack frame needs a return address.
    -   The way to resume execution when we're done with the call.
    -   The same way we use the `%esp` register to point to the top of
        the stack, we use the `%ebp` call frame to point to the most
        recently called stack frame.

### Call instructions {#call-instructions}

        call    label       direct
        call    *operand    indirect
        

-   The first call just has a label as an operand, we call this a direct
    call
    -   Hard-coded

-   The indirect call can specify a memory location or a register.
    -   Goes to the place and pulls the traget location and transfers
        control there.

### Variables {#variables}

        pushl   %ebp
        movel   %esp, %ebp
        .
        .
        .
        movl    %ebp, %esp
        popl    %ebp
        ret

### Vertical picture {#vertical-picture}

                |                 |
                |Local autos      |
                |Formal parameters|
                +-----------------+
          %ebp->|old %ebp         |
                +-----------------+
                |return address   |
                +-----------------+
                         .
                         .
                         .
                +-----------------+
                |old %ebp         |
                +-----------------+
                |return address   |
                +-----------------+
                

March 5th, 2013 - Programming Assignment 3: Assembly Language Programming {#march-5th-2013---programming-assignment-3-assembly-language-programming}
-------------------------------------------------------------------------

### Introduction {#introduction-2}

This assignment is designed to give you additional practice in reading
and writing Assembly Lan- guage programs. As discussed in lecture,
unless you are working in increasingly rare areas such as low-level OS
development, you are unlikely to be reading and/or writing Assembly
Language pro- grams in the remainder of your career. However, we are
still requiring you to read and write some here to make sure you
understand the computing model underlying your C and Java programs. In
addition, being able to read Assembly Language is particularly important
because there are times when you need to understand what the compiler is
doing to your code. There are two parts. In the first part, you will
write two small functions in Assembly. In the second part, you will be
deciphering (that is, write equivalent C code) an Assembly Language
program, much like you have done in your homework and the Midterm Exam.
You will also be asked to compare unoptimized and optimized versions of
the code and explained what the compiler did when it optimized the code.
Important: On most of the iLab machines that we checked, e.g., several
of the Design Pattern machines, including adapter.rutgers.edu,
command.rutgers.edu, and factory.rutgers.edu, gcc by de- fault will
generate x86 Assembly, which is what we want. Do be careful and check
the generated assembly, though, in case some of the machines are 64-bit
processors, with gcc configured to gen- erate x86-64 code. If you see
Assembly code with registers beginning with %r (e.g., %rbx or %r9), then
it is x86-64 and not what you want. Move to another iLab machine.

### Writing x86 Assembly {#writing-x86-assembly}

In this part, you will implement a program formula that will print the
formula for (1 + x)n. In particular, your program formula should support
the following usage interface:

    formula <power>

where the argument `<power>` should be a non-negative integer. Your
program should print out the "long" form of (1 + *x*)*n*, where *n* is
equal to the argument `<power>`. Your program should also print out its
execution time (in microseconds). For example:

    ./formula 5
    (1+x)^5 =1 +5*x^1+10*x^2+10*x^3+5*x^4+1*x^5 
    Time Required = 50 microsecond

    ./formula 10
    1 + x)^10  = 1 + 10*x^1 + 45*x^2 + 120*x^3 + 210*x^4 + 252*x^5
              + 210*x^6 + 120*x^7 + 45*x^8 + 10*x^9 + 1*x^10
    Time Required = 55 microsecond

(Hint: You can use the system call `gettimeofday()` to measure the
running time of a chunk of code.) More generally, given the argument n,
your code needs to generate:

(1 + *x*)<sup>*n*</sup> = 1 + *n**C*1 \* *x* + *n**C*2 \* *x*<sup>2</sup> + . . .  + *n**C**r* \* *x*<sup>*r*</sup> + . . .  + *n**C**n* \* *x*<sup>*n*</sup>

Your program should also print a usage message if the user runs formula
with the help flag (-h). For example:

     $ ./formula -h
     Usage: formula <positive integer>

### nCr Calculation {#ncr-calculation}

Hopefully, you remember from one of your Math classes that each of the
constant nCr above can be computed using the formula:
\$nCr = n! \\frac{r!}{(n − r)!}\$
 Your task is to implement this computation in Assembly. In particular,
you need to implement two functions in Assembly:

`int nCr(int n, int r)`: This function computes the nCr constant
according to Equation (1).

`int Factorial(int n)`: This function computes the factorial of the
input (that is, n!).

To help you get started, we are providing two files:

`nCr.s`: contains the necessary GAS (Gnu ASsembler) directives so that
your Assembly code can be compiled and linked in with your C code (in
format.c).

`nCr.h`: contains the prototype for the function nCr() so that you can
compile your C code which calls `nCr()`.

**Important**: As n becomes large, you will not be able to compute n!
and nCr. Both nCr() and Factorial() must detect overflow conditions
using the processor’s condition codes and return 0 to indicate that an
error has been encountered.

### Reading x86 Assembly Code {#reading-x86-assembly-code}

In this part, you are asked to decipher the Assembly Language program in
the attached mystery.s file. Specifically, you need to provide a concise
description of what the program does and how it does it. You should also
implement a C program mystery that performs the same task in the same
manner that the code in the attached file mystery.s does. The provided
program takes a single integer as input.

     $ gcc -o mystery mystery.s
     $ ./mystery 41
     Value: 165580141

**Hint**: This program performs a well known and easily recognizable
computation. However, it includes an optimization to speedup the
computation. You need to figure out both the basic functionality as well
as the optimization, describe them, and replicate them in your C code.
Another Hint: You are not strictly required to go backward from the
mystery.s file that we give you. That is, when you start writing your
mystery.c program, you can compile it to Assembly (gcc -S), and compare
the generated code against our mystery.s. Our mystery.s was generated on
factory.rutgers.edu so you should be able to generate the exact same
code. Once you have implemented your C program, you should compile it
with and without the -O option (optimization). You should then compare
the two versions and explain the differences inside the mystery
function.

For example:

    \$ gcc -S mystery.c 
    \$ mv mystery.s mystery.unoptimized.s
    \$ gcc -S -O mystery.c 
    \$ diff --side-by-side mystery.unoptimized.s
    mystery.s

The last command in the above sequence will show you the differences
between the two .s files side by side (use a large terminal window). You
should look at the differences inside the mystery function and explain
why the compiler made the changes that it did when optimizing the code.
Collaboration: Please do not share your solution with your classmates as
this gives the problem away. You may help each other with understanding
Assembly details but not the solution.

### Submission {#submission-2}

You have to e-submit the assignment using Sakai. Your submission should
be a tar file named pa3.tar that can be extracted using the command:
Your tar file must contain: tar xf pa3.tar

-   A sub-directory named formula. formula must contain:
-   readme.pdf: this file should describe your design and implementation
    of the formula program. In particular, it should detail your design,
    any design/implementation chal- lenges that you ran into, and an
    analysis (e.g., big-O analysis) of the space and time performance of
    your program.
-   Makefile: there should be at least two rules in this Makefile:
    formula build your formula executable. clean prepare for rebuilding
    from scratch.
-   source code: all source code files necessary for building formula.
    At a minimum, this should include four files, formula.h, formula.c,
    nCr.s, and nCr.h. - A sub-directory named mystery. mystery must
    contain:
-   readme.pdf: this file should describe how you went about figuring
    out what the mystery program does. It also should describe the
    changes that the compiler made when opti- mizing your C code and why
    you think that the compiler made those changes. (That is, why might
    the changes make your program run faster?)
-   Makefile: there should be at least two rules in your Makefile:
    mystery build your mystery executable. clean prepare for rebuilding
    from scratch.
-   source code: all source code files necessary for building mystery.
    At minimum, this should include two files, mystery.h and mystery.c.
    We will compile and test your programs on the iLab machines so you
    should make sure that your programs compile and run correctly on
    these machines. You must compile all C code using the gcc compiler
    with the `-ansi -pedantic -Wall` flags.

### Grading Guidelines {#grading-guidelines-2}

#### Functionality {#functionality-3}

This is a large class so that necessarily the most significant part of
your grade will be based on programmatic checking of your program. That
is, we will build a binary using the Makefile and source code that you
submitted, and then test the binary for correct functionality against a
set of inputs. Thus: - You should make sure that we can build your
program by just running make. - You should test your code as thoroughly
as you can. In particular, your code should be adept at handling
exceptional cases. Be careful to follow all instructions. If something
doesn’t seem right, ask.

#### Design {#design-2}

Having said the above about functionality, design is a critical part of
any programming exercise. In particular, we expect you to write
reasonably efficient code based on reasonably performing algorithms and
data structures. More importantly, you need to understand the
performance (time & space) implications of the algorithms and data
structures you chose to use. Thus, the explanation of your design and
analyses in the readme.pdf will comprise a non-trivial part of your
grade. Give careful thoughts to your writing of this file, rather than
writing whatever comes to your mind in the last few minutes before the
assignment is due.

#### Coding Style {#coding-style-2}

Finally, it is important that you write "good" code. Unfortunately, we
won’t be able to look at your code as closely as we would like to give
you good feedback. Nevertheless, a part of your grade will depend on the
quality of your code. Here are some guidelines for what we consider to
be good:

-   Your code is modularized. That is, your code is split into pieces
    that make sense, where the pieces are neither too small nor too big.
-   Your code is well documented with comments. This does not mean that
    you should comment every line of code. Common practice is to
    document each function (the parameters it takes as input, the
    results produced, any side-effects, and the function’s
    functionality) and add comments in the code where it will help
    another programmer figure out what is going on.
-   You use variable names that have some meaning (rather than cryptic
    names like i). Further, you should observe the following protocols
    to make it easier for us to look at your code: - Define prototypes
    for all functions. - Place all prototype, typedef, and struct
    definitions in header (.h) files. - Error and warning messages
    should be printed to stderr using fprintf.

March 27th, 2013 - Midterm Study Guide <small>with special thanks to Matthew Resch</small> {#march-27th-2013---midterm-study-guide-with-special-thanks-to-matthew-resch}
------------------------------------------------------------------------------------------

### Number conversion {#number-conversion}

#### Methods {#methods}

1.  Expansion
    -   To convert a number, such as binary number, to decimal, use the
        definition of a number representation as an abbreviated
        polynomial.

        10101. 1 = 1*x*2<sup>4</sup> + 0*x*2<sup>3</sup> + 1*x*2<sup>2</sup> + 0*x*2<sup>1</sup> + 1*x*2<sup>0</sup> + 1*x*2<sup> − 1</sup>
        16 + 0 + 4 + 0 + 1 + . 5 = 21. 5

2.  Division Method
    -   To convert a number from one base to another, take the number,
        divide it by the target base, keep the remainder and divide the
        quotient by the base until the quotient that remains is zero.
        Number generated from right/left.
    -   Example:
        13%2 = 1
        6%2 = 0
        3%2 = 1
        1%2 = 1

3.  Multiplication Method
    -   This method is generally used to convert fractions
    -   Multiply the number by the base, and keep the digit that is
        generated, then multiply the thing to the right of the decimal
        by the base again, until you have nothing to the right of the
        decimal.
    -   Ex:
        . 7812510 → . 110012
        . 78125*x*2 = 1. 56250
        . 56250*x*2 = 1. 1250
        . 1250*x*2 = 0. 250
        . 250*x*2 = 0. 50
        . 50*x*2 = 1. 0

#### Binary {#binary-2}

-   To octal
-   To decimal
-   To hexadecimal

#### Octal {#octal-2}

-   To binary
-   To decimal
-   To hexadecimal

#### Decimal {#decimal-1}

-   To binary
-   To octal
-   To hexadecimal

#### Hexadecimal {#hexadecimal-1}

-   To decimal
-   To octal
-   To binary

### Endianess {#endianess}

-   There are generally two forms of Endian-ness, **Big Endian** and
    **Little Endian**.
-   Endian-ness refers to the ordering of bytes stored in memory,
    determined by the significance of the byte.
-   What’s the difference between the two different types?
    -   Little Endian machines store the **least** significant byte
        first, at the **lowest** byte address
        -   Most machines that we use in our day-to-day life is Little
            Endian.

    -   Big Endian machines store the **most** significant byte first,
        at the **lowest** byte address
        -   Most machines that use Big Endian do not run an architecture
            that we are likely to come in contact with.

### Assembly Language (x86, AT&T, 32-bit) {#assembly-language-x86-att-32-bit}

-   Basic assembly instructions are read from right to left source,
    right to left destination.
    -   For example, 96(%ebp, %eax, 8) means “multiply 8 by the memory
        of eax, add to ebp and then add 96 to that.

-   Parenthesis always denotes memory being used
-   The difference between leal and mov is mov actually moves the
    contents, leal simply copies the address but not the contents
-   Operands can have the following types:
    -   Register: These operands refer directly to the contents of the
        CPU’s registers, and are denoted with a % in front of them.
        -   If you want to deal with address, put a ( ) around register
        -   Offset can be specified as an immediate

-   Sample program

        movl $1, -4(%ebp);    // we move 1 into "up four bits" from the base pointer
        movl $2, -8(%ebp);    // we move 2 into "up eight bits" from the base pointer
        movl -8(%ebp), %eax;  // move what in "up eight bits" from base pointo into eax
        addl -4(%ebp), %eax;  // add to it what's "up four bits"
        movl %eax, -12(%ebp); // move what's in eax to -12 bits from base pointer

-   Another sample program

        mov al,[L1];     // copy byte at L1 into AL
        mov eax,L1;      // EAX now stores the address of byte at L1
        mov [L1],ah;     // copy AH into byte at L1
        mov eax,[L6];    // copy double word at L6 into EAX
        add eax,[L6];    // EAX = EAX + double word at L6
        add [L6],eax;    // double word at L6 += EAX
        mov al, [L6];    // copy first byte of double word at L6 into AL

#### Basic commands {#basic-commands}

-   `MOV`
    -   The mov instruction moves data from one location to another, but
        cannot take two locations in memory as operands. The operands
        must also be the same size.
    -   Format: mov source, destination

-   `ADD`
    -   Used to add two integers together
    -   Format: add destination, source
    -   Example:

            add eax, 4 -> eax = eax + 4
            add al, ah -> al = al + ah

-   `SUB`
    -   Used to subtract two integers
    -   Format: sub destination, source
    -   Example:

        sub bx, 10 -\> bx = bx -10 sub ebx, edi -\> ebx = ebx – edi

-   `INC`/`DEC`
    -   Used to increment or decrement values by one.
    -   Since one is implicit operand, code is smaller than for add/sub
    -   Example:

        inc ecx -\> ecx++ dec dl -\> dl—

#### Operand Types {#operand-types}

-   Immediate
    -   Constant integer data
    -   `$0x400`, `$-533`
    -   Encoded with 1, 2, or 4 bytes

-   Register
    -   One of 8 integer registers
    -   `%esp` and `%ebp` reserved for special use
        -   **S** tack **p** ointer
        -   **B** ase **p** ointer

    -   Others have special uses for particular instructions

#### Memory {#memory-1}

-   4 consecutive bytes of memory
-   Various “address modes”

#### Parameter order {#parameter-order}

-   Source before the destination
-   `eax := 5` is `mov $5, %eax`

#### Parameter size {#parameter-size}

-   `q` for qword,
-   `l` for long (dword)
-   `w` for word
-   `b` for byte

#### Immediate value sigils {#immediate-value-sigils}

-   Values prefixed with a `$`
-   registers must be prefixed with a `%`

#### Registers {#registers}

-   `AX` multiply/divide, string load & store
-   `CX` count for string operations & shifts
-   `DX` port address for `IN` and `OUT`
-   `BX` index register for `MOVE`
-   `SP` points to top of stack
    -   `BP` points to base of stack frame
    -   `SI` points to a source in stream operations
    -   `DI` points to a destination in stream operations

### Call stack {#call-stack}

### DeMorgan's laws {#demorgans-laws}

### Circuits {#circuits}

### Radix {#radix}

### Computer internals {#computer-internals}

-   CPU,
    -   registers,
    -   a program counter,
    -   ALU (Arithmetic Logic Unit),
        -   Gets instructions to do things on floating, bitwise, set
            point, or comparison operations, and gives the results in a
            condition code.

    -   and a control unit

-   Memory,
    -   any part can be accessed in constant time
    -   Addresses are stored in either hex, or octal, points to a
        specific piece of memory

-   BUS,
-   I/O devices,
    -   Mouse
    -   Keyboard
    -   Screen
    -   Magic Trackpad
    -   Magic Mouse

-   storage, NIC (network interface cards)

April 11th, 2013 - Lecture {#april-11th-2013---lecture}
--------------------------

-   What I encourage you to do is to write minituare programs
    -   For example, the .size directives, write a program that does
        nothing but read those strings of bytes, and turn them into a
        hex number just to show that I can read these numbers and
        properly convert them.
    -   With this, you have a piece of code you can trust and transplant
        and really make sure it works.
    -   This is not a requirement, but it is strongly encouraged

-   Moving on, the flags that affect various `Y86` instructions.

                zf  sf  of
        addl    y   y   y
        subl    y   y   y
        amdl    y   y   0
        xori    y   y   0
        mull    y   y   y
        readb   y   0   0
        readw   y   0   0

April 15th, 2013 - Programming Assignment 4: Y86 Emulation {#april-15th-2013---programming-assignment-4-y86-emulation}
----------------------------------------------------------

### Introduction {#introduction-3}

This assignment is designed to help you really understand how the
fetch-and-execute cycle works as well as the idea of program-as-data. It
will require a substantial implementation effort. The usual warning goes
double for this assignment: *Do not procrastinate*.

### Y86 Architecture {#y86-architecture}

The Y86 architecture has eight registers, three condition codes, a
program counter and memory that holds machine instructions and data. All
addresses, immediate values and displacements are 32 bit little-endian
values. Each of the eight registers has a 4-bit ID that fits into the
Y86 instructions. The eight registers and their encoding in the Y86
machine instructions are as follows:

     %eax 0
     %ecx 1
     %edx 2
     %ebx 3
     %esp 4
     %ebp 5
     %esi 6
     %edi 7
     

The condition codes are single-bit flags set by arithmetic or logical
instructions. The three condition codes are:

     OF overflow
     ZF zero
     SF negative
     

The program counter is the address of the next machine instruction to
execute. Total memory size will have to be determined as part of
emulator execution. The Y86 instruction set is modeled on the larger
Intelx86 instruction set, but is not a direct subset.

### Y86 Emulator {#y86-emulator}

An emulator is hardware or software that duplicates (or emulates) the
functions of one computer system (in this case Y86 instructions) on
another computer system (the Intel host). The Y86 instructions are
different from the Intel x86 instructions. Your assignment is to write
an emulator for the Y86 instruction set.

Implement a program y86emul that executes Y86 executable files. Your
program y86emul should support the following user interface:

    y86emul [-h] <y86 input file>

where <y86 input file> is the name of a Y86 input file, whose structure
is defined in Section 5.

If -h is given as an argument, your program should just print out help
for how the user can run the program and then quit.

Erroneous inputs should cause your program to print out:

    ERROR: <an informative error message>

Otherwise, your program should run the Y86 code which may read whatever
Y86 inputs from the terminal and/or write Y86 outputs to the terminal as
your Y86 program executes.

Your emulator will read the input file, allocate a chunk of memory of
appropriate size which will act as the Y86 address space, populate that
chunk of memory with data and machine instructions from the input file
and then starts execution of the Y86 machine instructions. The entire
address space of the Y86 program fits within this block of allocated
memory. The lowest byte of the address of the allocated block is Y86
address 0 and all other Y86 addresses are offsets within this block.

Your emulator will fetch, decode and execute Y86 instructions. This
execution is tied to an status code that may take on the value AOK, HLT,
ADR, INS. AOK means that everything is fine, no detected errors during
execution. HLT means a halt instruction has been encountered, which is
how Y86 programs normally end. ADR means some sort of invalid address
has been encountered, which also stops Y86 program execution. INS is set
for an invalid instruction, which also stops Y86 program execution. Your
emulator should print out how the Y86 program execution ended.

### Y86 Instructions {#y86-instructions}

The definition and encoding of the Y86 instructions are presented in the
slides (also an attachment) and in the Bryant and O’Halloran book in
Chapter 4.1. The instruction set presented there is minimal and almost
functionally complete. What is missing are instructions for input and
output. Your Y86 emulator will also handle instruction to read from and
write to the terminal.

Read byte and read long instructions

    Encoding Bytes 
    0 1 2 3 4 5
    readb d(rA) C0 rA F D 
    readl d(rA) C1 rA F D

The readb instruction reads a single byte from the terminal into memory,
and the readl instruction reads a single 4-byte little-endian word into
memory. The little-endian word is already compatible with the
little-endian Intel architecture, where your emulator will run. Both
instructions set the ZF condition code. On normal input, the ZF flag is
set to zero, on end-of-file the ZF flag is set to one. Testing the
conditon code is how the Y86 code can detect end of file. Note that the
F in the second half of the second byte means ”no register”, just as it
does for some of the other Y86 instructions. Both instructions are six
bytes long with a 4-byte offset D.

Write byte and write long instructions

    Encoding Bytes 
    0 1 2 3 4 5
    writeb d(rA) D0 rA F D 
    writel d(rA) D1 rA F D

The writeb instruction writes a single byte from memory to the terminal,
and the writel instruction writes a single 4-byte little-endian word
from memory to the terminal. Neither instruction alters the condition
codes. Both instructions are six bytes long with a 4-byte offset D.

Multiplcation Instruction

Encoding Bytes 0 1 2 3 4 5 mull rA,rB 64 D

The mull instruction multiplies the values in rA and rB and leaves the
product in rB. This instruc- tion set the condition codes. The
instruction is five bytes long.

### Y86 Input file format {#y86-input-file-format}

The input file to your Y86 emulator does not contain Y86 assembler
instructions. Instead, it contains an ASCII representation of the
information needed to start and execute a ready-to-run program,
including Y86 machine instructions. An input file will contain
directives that specify data and Y86 machine instructions.

#### Specifying Total Program Size and Base of Stack {#specifying-total-program-size-and-base-of-stack}

The .size directive

    .size hex-address

This specifies the total size of the program in memory. The hex address
also specifies the address of the bottom of the stack. The Y86 stack
grows from larger addresses toward smaller addresses. There should be
only one .size directive in the input file.

#### Specifying String Constants {#specifying-string-constants}

The .string directive

    .string hex-address "double-quoted string"

specifies a string contained in the double quotes. The hex-address
specifies the location of the string in the memory block allocated by
your emulator. The input string will contain only printable characters
and nothing that requires a backslash.

#### Specifying Integer Values {#specifying-integer-values}

The .long directive

    .long hex-address decimal-number

specifies a 4-byte signed integer. The hex address specifies the
location of the value and the decimal number is the initial value at
that Y86 address. All Y86 arithmetic is 4-byte signed integer
arithmetic.

#### Setting Aside Chunks of Memory {#setting-aside-chunks-of-memory}

The .bss directive

    .bss hex-address decimal-size

specifies a chunk of uninitialzed memory in the Y86 address space. The
hex address specifies the location of the uninitialized chunk and the
decimal size specifies the size.

#### Specifying One-Byte Values {#specifying-one-byte-values}

The .byte directive

    .byte hex-address hex-number

specifies a one-byte value. The hex address specifies the location of
the byte and the initial value is the hex number whose value is between
00 and FF, inclusive.

#### Specifying Y86 Machine Instructions {#specifying-y86-machine-instructions}

The .text directive

    .text hex-address ASCII string of hex Y86 instructions

specifies the Y86 machine instructions. The hex address specifies where
the machine instructions should be placed in the Y86 address space. This
same address is also the initial value of the Y86

April 16th, 2013 - Processor Design I: Sequential Processor (Y86) {#april-16th-2013---processor-design-i-sequential-processor-y86}
-----------------------------------------------------------------

-   **Instruction Set Architecture** (ISA) is the interface between
    software and hardware.
-   Y86 is a simplified ISA modeled after x86.
-   Processor states
    -   Program registers are the same as IA32, each 32 bits.
    -   Three condition codes, `OF` for overflow, `ZF` for zero, and
        `SF` for negative.
    -   Momery is byte addressable storage array, words stored in
        little- endian byte order.

### Instructions {#instructions-1}

-   `nop`
    -   no effect

-   `halt`
    -   stop execution

-   `rrmovl rA, rB`
    -   `rB <- rA`

-   `irmovl V, rb`
    -   `rB <- V`

-   `rmmovl rA, D(rb)`
    -   `Mem[rB + D] <- rA`

-   `mrmovl D(rA), rB`
    -   `rb <- Mem[rA + D]`

-   `OP rA, rB`
    -   `rB<-rBOPrA` (OP )

-   `jXX Dest`
    -   `PC <- Dest`

-   `call Dest`
    -   invoke function at Dest

-   `ret`
    -   return from function

-   `pushl rA`
    -   `%esp <- %esp – 4; Mem[%esp] <- rA`

-   `popl rA`
    -   `rA <- Mem[%esp]; %esp <- %esp + 4`

### Registers {#registers-1}

-   `%eax` - 0
-   `%ecx` - 1
-   `%edx` - 2
-   `%ebx` - 3
-   `%esp` - 4
-   `%ebp` - 5
-   `%esi` - 6
-   `%edi` - 7

### Condition codes {#condition-codes}

-   `OF` - overflow
-   `ZF` - zero
-   `SF` - negative

### Error codes {#error-codes}

-   `AOK` - "everything is fine"
-   `HLT` - "halt instruction has been encountered"
-   `ADR` - "means some sort of invalid address"
-   `INS` - "an invalid instruction"

> Your emulator should print out how the Y86 program execution ended.

### Directives {#directives}

#### The `.size` directive {#the-.size-directive}

    .size hex-address

-   total size of the program in memory
-   address at the bottom of the stack
-   stack grows from largers addresser toweard smaller address
-   **there can be only one**

#### The `.string` directive {#the-.string-directive}

    .string hex-address "double-quoted string"

-   the hex address
    -   specifies the location of the given string

-   the double-quotes string
    -   will contain only printable characters

-   This is a contrived string, local to the program.
    -   To implement, save in an array, it seems.

#### The `.long` directive {#the-.long-directive}

    .long hex-address decimal-number

-   The hex address specifies the location of the value
-   The decimal number is the initial value at that address.
-   **all arithmatic is 4-byte signed integer arithmatic**

#### The `.bss` directive {#the-.bss-directive}

    .bss hex-address decimal-size

-   specifies a chuck of uninitialized memory in Y86 address space
-   the hex address is the location
-   the decimal size is the size

#### The `.byte` directive {#the-.byte-directive}

    .byte hex-address hex-number

-   specifies a one-byte value
-   the hex address specifcs the location
-   the hex number is between 00 and FF (inclusive)

#### The `.text` directive {#the-.text-directive}

    .text hex-address "ASCII string of hex Y86 instructions"

-   The hex address specifies where the machine instructions should be
    placed in the Y86 address space.
-   The ASCII string in a single long encoding of the hex bytes on the
    machine instructions, two characters per byte, no leading ”0x”.

### Instruction Encoding {#instruction-encoding}

    Byte                0   1   2   3   4   5
    nop                 0   0
    halt                1   0
    rrmovl rA, rB       2   0   rA  rB
    irmovl V, rb        3   0   8   rB
    rmmovl rA, D(rb)    4   0   rA  rB
    mrmovl D(rB), rA    5   0   rA  rB
    OPl rA, rB          6   fn  rA  rB
    jXX Dest            7   fn  Dest
    call Dest           8   0   Dest
    ret                 9   0 
    pul rA              A   0   rA  8
    popl rA             B   0   rA  8

-   The decimal values of operations (instructions are data):

        +-------------+-----+---+
        | Instruction | Hex |Siz|
        +-------------+-----+---+
        | nop         | 00  | 1 | 
        | halt        | 10  | 1 | 
        | rrmovl      | 20  | 2 | 
        | irmovl      | 30  | 6 |
        | rmmovl      | 40  | 6 |
        | mrmovl      | 50  | 6 |
        | addl        | 60  | 2 |
        | subl        | 61  | 2 |
        | andl        | 62  | 2 |
        | mull        | 64  | 2 |
        | xorl        | 63  | 2 |
        | jmp         | 70  | 5 |
        | jle         | 71  | 5 |
        | jl          | 72  | 5 | 
        | je          | 73  | 5 |
        | jne         | 74  | 5 | 
        | jge         | 75  | 5 | 
        | jg          | 76  | 5 |
        | call        | 80  | 5 |
        | ret         | 90  | 1 |
        | pushl       | a0  | 2 |
        | popl        | b0  | 2 |
        +-------------+-----+---+
        this chart pushed my vim knowledge to the limit
        ask @Tazato

### Summary {#summary}

-   Similar state and instruction as IA32
-   Simpler encodings
-   Somewhere between CISC and RISC

### Stages {#stages}

-   Fetch, read instructions from memory
-   Decode, read operand register
-   Execute, computer value or address
-   Memory, read/write date from/to main memory
-   Write back, write destination register
-   PC, update program counter

April 15th, 2013 - Lecture: Memory {#april-15th-2013---lecture-memory}
----------------------------------

-   RAM
    -   Key features
        -   RAM is packaged as a chip
        -   Basic storage unit is a cell
        -   Multiple RAM chips form a memory

    -   Static RAM (SRAM)
        -   Each cell stores bit with a six-transistor circuit
        -   Retains value indefinitely, as long as it is kept powered
        -   Relative insnsitive to disturbances
        -   Faster and more expensive than DRAM

    -   Dynamic RAM (DRAM)
        -   Each cell stores bit with a capacitor and transistor
        -   Value must be refereshed every 10-100ms
        -   Sensitive to disturbances
        -   Slower and cheaper than SRAM


