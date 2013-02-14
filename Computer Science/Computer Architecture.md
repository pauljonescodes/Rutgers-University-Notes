# Computer Architecture Notes 

## Description 
This course covers the fundamental issues in the design of modern computer systems, including the design and implementation of key hardware components such as the processor, memory, and I/O devices, and the software/hardware interface.

- Topics:
    + C programming
    + Data representation and computer arithmetic
    + Assembly language programming
    + Boolean algebra
    + Basic digital logic design
    + Processor design
    + Cache design
    + Main memory design

## Syllabus

- Instructor: Brian Russell 
	- Email: [morbius@cs.rutgers.edu][1]    
	- Office Hours: Wednesdays 8:00-9:00 pm, Hill 403. 
- TAs
	+ Yuanzhen Gu 
		* Email: [yg185@cs.rutgers.edu][2]    
		* Office Hours: Thursdays, 3:00-4:00 pm, Hill 418 
	+ Longhao Shu 
		* Email: [ls675@cs.rutgers.edu][3]
		* Office Hours: Thursdays, 5:00-6:00 pm, Hill 416 
	+ Chaowei Tan 
		* Email: [ct382@cs.rutgers.edu][4]    
		* Office Hours: Fridays, 9:00-10:00 am, Hill 488 
	+ Vilemini Kalambratsidou 
		* [vilelmini.kalabratsidou@gmail.com][5]   
		* Office Hours: Wednesdays 10:00 am-Noon, Hill 410 

### Objective 

The aim of CS 211 is to provide an understanding of the fundamental logical organization of a computer (its parts and their relationship) and how it actually works; exposure to a central processor's native language, and to basic computer components. Basic Architecture for high performance design. 

### Prerequisite Knowledge

- Prior programming experience in a high-level language (such as Java). 
- 01:198:112. Credit not given for this course and 14:332:331.  

### Topics 

The following list is organized by topic, not by chronological order of coverage in the course. 

1. Von Neumann Architecture, Hardware trends, Importance of Speed, Cost, Energy
1. Intro to C programming
1. Data Representation, Computer Arithmetic
1. Assembly language techniques, including macro-instruction definition
1. Digital logic, registers, instruction counter
1. Processor Architecture
1. Pipelining
1. Memory hierarchies, Caching (L0, L1, L2 caches)
1. Virtual Memory
1. Interrupts
1. Input and Output, buses

### Schedule

1. Jan 22	 Into to hardware trends, Moore's law. Chap 1.
2. Jan 24	 Into to C programming
3. Jan 29	 C program structure, control flow structures
4. Jan 31	 Pointers and arrays, C functions
5. Feb 05	 Dynamic memory management
6. Feb 07	 C preprocessor, formatted I/O
7. Feb 12	 Data representation. Chap 2.1 2.2 2.4.
8. Feb 14	 Computer Arithmetic.31
9. Feb 19	 Assembly Language Programming	Chap 3.
10. Feb 21	 Assembly Language Programming
11. Feb 26	 Assembly Language Programming
12. Feb 28	 Assembly Language Programming
13. Mar 05	 Assembly Language Programming
14. Mar 07	 Assembly Language Programming
15. Mar 12	 Spring Break -- no class
16. Mar 14	 Spring Break -- no class
17. Mar 19	 Digital Logic Chap 4.2
18. Mar 21	 Digital Logic
19. Mar 26	 Processor Design
20. Mar 28	 Midterm
21. Apr 02	 Processor Design
22. Apr 04	 Processor Design
23. Apr 09	 Processor Design
24. Apr 11	 Caches
25. Apr 16	 Caches
26. Apr 18	 Caches
27. Apr 23	 Caches
29. Apr 25	 I/O and Disks
30. Apr 30	 Review

### Expected Work 

Students are expected to attend all lectures and perform all reading assignments prior to lecture. Students are also expected to attend all recitation section meetings. Students will be evaluated according to their performance on four programming projects, programming project, a mid-term examination, and a final examination.
                   
### Grading

- 40% Correctness
	- Percent based on number of test cases
- 40% Code Quality
	- 20% Algorithmic
	- 10% Reusability/Modularity
	- 10% Decomposition
- 20% Documentation
	- 10% Test Cases from Students
	- 5% Comments
	- 5% Documentation (Analysis, readme files, etc...)

                                         
### Project Warning

This is a project course, which means that this course should give you more than a passing knowledge of computer architecture. The project work will be a major undertaking. If you complete the projects, you will have learned a lot. However, assess your commitment to this course realistically. If you don't have the time or the inclination to work hard on the project, you would be better off not taking the course. You will have to learn how to build and debug C and Assembly programs and make them robust to outside errors. You will also have to describe how your program work in a written document.  There are three or four programming assignments. Students are required to complete the parts by the scheduled deadlines. Failure to turn in the project by the deadline using the electronic handin website will result in a zero grade. No exceptions!  There are many different operating systems and variants of C out there and we cannot test your program on all of them. So all program assignments must run on the local iLab Linux machines. We will be grading your assignments on those machines as well. 
                                                            
### Working Together and Academic Honesty 

Cheating on projects and exams will not be tolerated. We want to protect the fairness and integrity of the class, so we run code similarity detectors on the projects and scrutinize exams for copying. Both parties in the exchange are liable; e.g. if you give away solutions to friends, you're putting yourself at risk too. If you get caught, it's a nasty process\---| just don't go there! You're better off asking for help, or at worst, dropping the course and trying it again. The department academic integrity policy can be found at http://www.cs.rutgers.edu/policies/academicintegrity/. You now need to click explicitly on a link when first login to our computing facilities, use handin, etc., that says you acknowledge being aware of the policy (which you can read through the login screen). If you fail to do the click-through by the end of September, your access to our facilities will cease October 1. 
                                                                      
#### The Gilligan's Island Rule 

We do encourage you to talk to your classmates, provided you follow the Gilligan's Island Rule. After a joint discussion of an assignment or problem, each student should discard all written material and then go do something mind-numbing for half an hour. For example, go watch an episode of Gilligan's Island (or jersey Shore in modern terms), and then recreate the solutions. The idea of this policy is to ensure that you fully understand the solutions or ideas that the group came up with. If you follow the Gilligan's island rule, often best route to follow to get a question answered is to ask, in order: 1. A classmate smarter than you. 2. Your TA. 3. The professor. 

 [1]: mailto:morbius%40cs.rutgers.edu
 [2]: mailto:yg185%40cs.rutgers.edu
 [3]: mailto:ls675%40cs.rutgers.edu
 [4]: mailto:ct382%40cs.rutgers.edu
 [5]: mailto:vilelmini.kalabratsidou%40gmail.com
 [6]: http://en.wikibooks.org/wiki/C_Programming
 [7]: http://paul.rutgers.edu/texts/C_programming.pdf
 [8]: http://publications.gbdirect.co.uk/c_book/
 [9]: http://paul.rutgers.edu/texts/the_c_book.pdf
 [10]: http://paul.rutgers.edu/creference.pdf  


## January 22nd, 2013 - Lecture: Hardware trends, Moore's law, Chapter 1
- The modern computer is a general purpose computer which stores programs as data.
- The hardware understands the encoded instructions and reacts predictably.
- The way the hardware executes a program is specific to the hardware, yet with similar results.
- We'll look at assembly for the Intel structure.
- Instructions as data - ones and zeros.
- Main components of computer
	+ CPU
	+ Memory
		* It is sometimes still called "core memory" for hustorical reasons. 
		* It is now "transistorized", computer programs "barf and die." 
		* It is random access - it can be done in constant time. 
		* It is volatile - turn the power off and memory is gone.
	+ Bus
	+ I/O devices
		* Human interface
		* Storage
		* Network cards
		* Graphics cards
- Control flow - any computer program can be written as three things: 
	1. sequencing, 
	2. alteration, and 
	3. repetition
- Von Neumann Model
	+ Fetch and execute cycle
		* What the CPU is doing is taking a bunch of instructions physcially next to each other in memory.
		* The Intel architecture, and I love this, takes the address `0xFFFFFFF0` to boot the machine.
		* First step is the fetch cycle, go get the instruction at the startup address.
		* Then decode the instruction, what is encoded? What do I do with it?
		* There are input operands on the instructions.
		* Then execute the operation, put the operations back on the register operands, 
		get the pointer to the next instruction.
	+ This guy got credit for work that was done previously, by Alan Turing.
	+ This was known as the "Turing Machine", which was a theoretical machine at the time.
	+ A few other contempories applied for pantents about instructions in memory.
	+ There was some dispute with Von Neumann and drafts and whose names appeared.
	+ A CPU and memory are connected by a bus.
	+ The Von Neumann bottleneck.
- Moore's law

## January 22nd, 2013 - Assignment 1: Wordstat

### Introduction

This assignment is designed to get you some initial experience with programming in C, as well as compiling, linking, running, and debugging a C program in our environment.

Your task is to write a C program called `wordstat` that reads a text file, finds all the unique words in the file, prints them in lexicographical order along with the total number of times each word appears (case-insensitive) and a count of different case-sensitive versions of the word.

A word is defined as any sequence of letters (A-Z, a-z) and digits (0-9) that starts with a letter, followed by 0 or more letters and/or digits. This definition is equivalent to the following regular expression:

	([A-Z]|[a-z])([A-Z]|[a-z]|[0-9])*

Words in the input file correspond to the longest sequences that match the above expression when reading the file from beginning to end. Each unique word is case-insensitive. That is, “book” and “Book” and “bOOk” are all occurrences of the same word. However, they represent three different case-sensitive versions of the word “book”.

As an example, running `wordstat` on a text file with the following content:

	Some Bogus ?Random1> (random1modnar) [34ranDom1] (Random1) boGus-$con@tent.

should produce:

	Word			Total No. Occurrences	No. Case-Sensitive Versions
	bogus			2						2
	con				1						1
	random1			3						2
	random1modnar	1						1
	some			1						1
	tent			1						1

### Implementation

Implement a program called `wordstat` with the following usage interface: 

	wordstat <argument>

where `<argument>` is either the name of the file that `wordstat` should process, or -h, which means that `wordstat` should print out a help menu to guide the user on how to use the program.

As discussed above, when invoked with a valid file name, `wordstat` should find and output all the unique words in the file in lexicographical order, along with the total number of times each word appears (case-insensitive) and a count of different case-sensitive versions of the word.

We leave the choice of data structures and algorithms up to you. However, your implementation must be reasonably efficient. For example, maintaining an array of records and doing linear search through this array would be unacceptable.
You are allowed to use functions from standard libraries (e.g., `strcmp()`) but you cannot use third- party libraries downloaded from the Internet (or from anywhere else). If you are unsure whether you can use something, ask us.
We will compile and test your program on the iLab machines so you should make sure that your program compiles and runs correctly on these machines. You must compile all C code using the gcc compiler with the `-ansi -pedantic -Wall` flags.

### Submission

You have to e-submit the assignment using Sakai. Your submission should be a tar file named pa1.tar. To create this file, put everything that you are submitting into a directory (folder) named pa1. Then, cd into the directory containing pa1 (that is, pa1’s parent directory) and run the following command:

	tar cvf pa1.tar pa1

To check that you have correctly created the tar file, you should copy it (pa1.tar) into an empty
directory and run the following command:

	tar xvf pa1.tar

This should create a directory named pa1 in the (previously) empty directory.
The pa1 directory in your tar file must contain:
* readme.pdf: This file should briefly describe the main data structures being used in your program, a big O analysis of the run time and space requirement of your program, and any challenges you encounter in this assignment
* Makefile: there should be at least two rules in your Makefile: 
	1. `wordstat`: build your `wordstat` executable.
	2. clean: prepare for rebuilding from scratch.
* source code: all source code files necessary for building `wordstat`. Your source code should
* contain at least 2 files: `wordstat.h` and `wordstat.c`.

We will provide a small script that you can use to check for the above required items. You do not have to run it, but it might help you to check that you are handing in everything that we are asking for.

### Grading Guidelines 

#### Functionality
This is a large class so that necessarily the most significant part of your grade will be based on programmatic checking of your program. That is, we will build a binary using the Makefile and source code that you submitted, and then test the binary for correct functionality against a set of inputs. Thus:
* You should make sure that we can build your program by just running make.
* You should test your code as thoroughly as you can. In particular, your code should be adept at handling exceptional cases. For example, `wordstat` should not crash if the argument file does not exist.

Be careful to follow all instructions. If something doesn’t seem right, ask.

#### Design
Having said the above about functionality, design is a critical part of any programming exercise. In particular, we expect you to write reasonably efficient code based on reasonably performing algorithms and data structures. More importantly, you need to understand the performance (time & space) implications of the algorithms and data structures you chose to use. Thus, the explanation of your design and big O analyses in the readme.pdf will comprise a non-trivial part of your grade. Give careful thoughts to your writing of this file, rather than writing whatever comes to your mind in the last few minutes before the assignment is due.

#### Coding Style
Finally, it is important that you write “good” code. Unfortunately, we won’t be able to look at your code as closely as we would like to give you good feedback. Nevertheless, a part of your grade will depend on the quality of your code. Here are some guidelines for what we consider to be good:
* Your code is modularized. That is, your code is split into pieces that make sense, where the pieces are neither too small nor too big.
* Your code is well documented with comments. This does not mean that you should comment every line of code. Common practice is to document each function (the parameters it takes as input, the results produced, any side-effects, and the function’s functionality) and add comments in the code where it will help another programmer figure out what is going on.
* You use variable names that have some meaning (rather than cryptic names like i). Further, you should observe the following protocols to make it easier for us to look at your code:
* Define prototypes for all functions.
* Place all prototype, typedef, and struct definitions in header (.h) files. 
* Error and warning messages should be printed to stderr using fprintf.

## January 24th, 2013 - Lecture: Introduction to C programming

- `.java` -> `.class` (machine independant)
- `c` code -> machine / OS specific -> executable
- "Hello world" in C

	    #include <stdio.h>
	    int
	    main() {
	    	printf("cogito ero sum\n");
	    	return 0;
	    }

- To run the program above, `cogito.c`:

		gcc cogito.c
		gcc -o cogito cogito.c
		gcc -c cogito.c
		gcc cogito.o

- command line arguments:

		#include <stdio.h>
		int
		main(int argc, char**argv) {
			int i;
			for(i = 0; i < argc, i++) {
				printf("arg %d is %s\n", i, argv[i]);
    		}

- structs
	+ there are no constructors
	+ there are no member functions
	+ there are no visibility restrictions (all public)
	+ no need for dynamically allocating them

## January 29th, 2013 - Lecture: C program structure, control flow structures

- Sometimes we as programmers we need some a variable that can only take on a few values.
- Java, evidently, screwed this up.

		enum stoplight {
			red,yellow,green
		}
		
		enum stoplight x;
		int y;
		x = red;
		y = green;
		x = (enum stoplight) 37;

- The internal numbering scheme for this unmodified syntax makes:
	+ `red = 1`
	+ `yellow = 2` and
	+ `green = 3`
- If the first line was `red = 5`, then the following values would be incremeneted from that.
- `typedef`

		typedef int size;

	+ my ability to decalre an alias for a new type
	+ now I get to say things like `size x,y`
	+ I am defining an alias for an existing type.

- `struct`

		typedef struct pt {
			int x,y;
		} point;
		
		point left_bot, right_top;

- `sizeof`

		sizeof unary-expression;
		sizeof (typename)
		& // "give me the address of this variable"
		* // unary prefix operator - "d-reference pointer"
		, // underutilized in java and c - "me seperating multiple expression"
		-> // "I use that to get at pointers or members of struct"
- To prompt for input

		while(printf("enter an integer>>"),scanf("%d",$x)>0) {
			printf("%d\n",x);
		}

- Pointers

		int *p;
		int x;

	+ In C, C++ you get pointers, which are the address in memory of an variable.
	+ `p` is a pointer to an integer

- functions

		void
		swap(int *p1, int *p2) {
			int temp;
			temp = *p1;
			*p1 = *p2;
			*p2 = temp;
		}
	
	+ this is afunction in C that swaps two values
	+ if you try to pass two integers directly, the compiler will complain
	+ I want to pass something that I want to change, and if I want to do that, I should pass the address of what I want to change.

- Pointers and arrays

		int *p, A[10],x;

		p = &A[0]; // the address of an int I can put in a pointer
		p = A; // the name of an array, A with no subscripts, is the address to the array
		x = *p; //

		p[1] = 5; // p is still a reference to apoointer, but I get to use subscripts
		*(p+1) = 5 // identical to above
		++p;
		P++;

- void star

		void *p;
		int *pi;
		float * pf;

		p = pi;
		p = pf;
		pf = (float *)p;
		pi = (int *)p;

- array addresses

		int
		main() {
			int A[10],I;
			printf("addr of i is %#x\n",&I);
			for (int i = 0; i<=10;i++) {
				printf("addr of A[%d] is %#x\n",i,&A[i]);
				A[i]=0;
			}
		}

- strings

		char * p3 = "hello";
		char array[] = "hello";
		char a2[10] = "hello";

## January 30th, 2013 - Office hours

- Linux is a descendant if UNIX, which is derivative from command line operating systems from Bell labs.
- The wanted a nice, modular OS.
- There's a directory structure. Everyone has a "subtree"
- gcc commands
- cat - concatenate files
	+ essentially, this prints, 
	+ this puts it on the screen
	+ if you put a bunch in the command, it outputs them all.
	+ you can redirect: 'cat a.c b.c d.c > big.c`
	+ you can append using `>>`
- we can copy and move files around
	+ `cp file1 [files ...] target`
	+ `mv ... `
- `date` tells you the time of day and the date
- `diff` tells you the difference between two files
- `grep regexp [files]`
	+ this is only in the present directory
- `find` goes through folders and files recursively
- `man` gets a manual
- `ls` and `mkdir [name]`
	- `-F` will distinguish between exe, subdirectory, etc.
- linux does not care about suffixes 
- `pg` or `more`: "I want to see the file, but it might be larger than my screen."
- `ps` for "process status"
- `rm` and `rmdir` for "remove" and "remove directory"
- `pwd`: "I am printing the working directory"
- `who`: who else, including you, is on the system

## January 31st, 2013 - Lecture: Pointers and arrays, C functions

- String functions ('<string.h>')
	
		char * strcpy(char * s1. const char * s2); // string copy
		char * strncpy(char * s1, const char * s2, int n); // up to n bytes
		char * strcat(char * s1, const char * s2); // string concatenate
		char * strncat(char * s1, const char * s2, int n); // up to n bytes
		int strcmp(const char * s1, const char * s2); // string compare
		int strncmp(const char * s1, const char *s2, int n); // upt to n bytes
		int stricmp(const char * s1, const char *s2, int n); // case insensitive
		int strlen(const char * s); // number of bytes

	+ `strncopy` says I will copy at most `n` bytes.
	+ both of these argument pointers better be set to something valid in memory.

- Something with memory

		void * memcpy(void * s1, const void * s2, int n);
		int memcmp (const void *s1, const void *s2, int n);
		void * memset (char * s1, char c, int n);

- Header files
	+ Sample header

			#ifndef point_h
			#define point_h

			struct point {
				int x,y;
			};
			#include "other.h"
			#endif

	+ Things to put in a header file
		* Things to share
		* Trees, lists, something
		* Linked list operations
		* Definitions of nodes
		* Types I make up, `structs`, `enums`, `typedefs`
		* Functions I want to use
- Dynamic memory allocation
	* Three operations:
		1. `malloc`
		2. `realloc`
		3. `free`
	* Definitions:

			void * malloc(size_t size);
			void * realloc (void * p, size_t newsize);
			void free(void*);

## February 5th, 2013 - Recitation

- The `include` command is used to use other code in your `.c` files, you include `.h` files.
- Typical files to include are `stdio.h` and `stdlib.h` (standard input/output and library, respectively).

		[return_type] [function_name] ([datatype arg1, ... ) {
			[function body]
		}

- Because C is parsed line by line, you must define a function before you use it otherwise it doesn't know it exists.
- So you can make a function prototype.

		[return_type] [function_name] ([datatype arg1, ... )

- You should include these things before `main`.
- `fopen` and `fclose` are commands you use one `FILE`s to get information from them.
	+ Specify parameters for read, write, etc.

			FILE * fopen(const char * filename, const char * mode);
			FILE * fclose(const char * filename);

- `fscanf` and `fprint`

		fscanf(FILE *fp, "%d", &age);
		fprintf(FILE *fp, "%d", age);

- String specifiers
	+ `%d` is an integer
	+ `%f` is a float
	+ `%s` is 

- `fputs` and `puts`

		fputs(char *str, FILE *fp);
		puts(char *str);

- `fwrite` and `fread`

		int fwrite(*buf, int size, int count, FILE *fp);

	+ `*buf` is the pointer
	+ `size` is the size of data type
	+ `count` is ...
	+ `*fp` is the file in question

- Example

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

## February 5th, 2013 - Lecture: Dynamic memory management

		#include <stdio.h>
		int printf(const char *, ...);
		int fprintf(FILE *, const char *, ...);
		int sprintf(char *, const char *, ...); // value of this is the length of string created
		-[character] %[-][width]c \\ %c %3c %-3c
		%[-][#][width][l]
		
> Don't change the program, change the goals

		 int scanf(const char * fmt, ...);
- remember, C passes by value, so pass the address of the thing you want to change.

## February 7th, 2013 - Lecture: C preprocessor, formatted I/O

- To print an error,

		fprintf(stderr, "fmt string", ...);
		
- Some code

		size_t fread(void * ptr, size_t size, sizeIt nobj, file *);

	+ `void * ptr` is the input buffer
	+ `size_t size` is the element size
	+ `size_t nobj` is the number of objects
	
- `fwrite`

		fwrite(const void * ptr, size_t size, size_t nobj, file*)
		
- `getc`

		int getc(file*);
		int fgetc(file*);
		char * gets (file*)
		char * fgets(char *s, int n, file *);
		
	+ `fgetc` and `getc` are basically interchangable for our purposes.
	+ you are getting the next character from the file.
	+ `gets` wil read a string until a new line or an end of file.
		* reading by file one line at a time.
	+ `fgets` will read a maximum of `n` characters or a new line, whicever ccomes first.
- some overlap

		void rewing(file*);
		fseek(file*, ol, seek_set);
		long ftell(file*);
		
- C preprocessor

		#include <stdio.h>
		#include "myheader.h
		
- Macros

		#define some_id
		#define asize 100
		#define max(a,b) ((a>b ? a : b)
		
- conditional compilation

		#if expression
		#elif expression
		#else
		#endif
		
		#ifdef some #define
		#endif
		#ifndef some #define
		#endf
		
## February 10th, 2013 - [Notes: The ANSI C `string.h`](http://www.csse.uwa.edu.au/programming/ansic-library.html#string)

- Copy ct to s including terminating `NUL`. Return s. 

		char* strcpy(char* s, const char* ct);

- Copy at most n characters of ct to s Pad with `NUL`s if ct is of length less than n. Return s. 

		char* strncpy(char* s, const char* ct, int n);

- Concatenate ct to s. Return s. 

		char* strcat(char* s, const char* ct);

- Concatenate at most n characters of ct to s. Terminate s with `NUL` and return it. 

		char* strncat(char* s, const char* ct, int n);

- Compare cs and ct. Return negative if `cs < ct`, zero if `cs == ct`, positive if `cs > ct`. 

		int strcmp(const char* cs, const char* ct);

- Compare at most n characters of cs and ct. Return negative if `cs < ct`, zero if `cs == ct`, positive if `cs > ct`. 

		int strncmp(const char* cs, const char* ct, int n);

- Return pointer to first occurrence of c in cs, or `NULL` if not found. 

		char* strchr(const char* cs, int c);

- Return pointer to last occurrence of c in cs, or `NULL` if not found. 

		char* strrchr(const char* cs, int c);

- Return length of prefix of cs consisting entirely of characters in ct. 

		size_t strspn(const char* cs, const char* ct);

- Return length of prefix of cs consisting entirely of characters *not* in ct. 

		size_t strcspn(const char* cs, const char* ct);

- Return pointer to first occurrence within cs of any character of ct, or `NULL` if not found. 

		char* strpbrk(const char* cs, const char* ct);

- Return pointer to first occurrence of ct in cs, or `NULL` if not found. 

		char* strstr(const char* cs, const char* ct);

- Return length of cs. 
		
		size_t strlen(const char* cs);

- Return pointer to implementation-defined string corresponding with error n. 

		char* strerror(int n);

- A sequence of calls to `strtok` returns tokens from s delimted by a character in ct. Non-`NULL` s indicates the first call in a sequence. ct may differ on each call. Returns `NULL` when no such token found. 

		char* strtok(char* s, const char* t);

- Copy n characters from ct to s. Return s. Does not work correctly if objects overlap.

		void* memcpy(void* s, const void* ct, int n);

- Copy n characters from ct to s. Return s. Works correctly even if objects overlap. 

		void* memmove(void* s, const void* ct, int n);

- Compare first n characters of cs with ct. Return negative if `cs < ct`, zero if `cs == ct`, positive if `cs > ct`. 

		int memcmp(const void* cs, const void* ct, int n);

- Return pointer to first occurrence of c in first n characters of cs, or `NULL` if not found. 

		void* strchr(const char* cs, int c, int n);

- Replace each of the first n characters of s by c. Return s.  

		void* strchr(char* s, int c, int n);
		
		
## February 12th, 2013 - Recitation

### What is GDB

- GDB is a debugger that helps you debug your program.
- The time you spend now learning gdb will save you days of debugging time.
- A debugger will make a good programmer and better programmer.

### Compiling a program for GDB

- You need to compile with the `-g` option to be able to debug a program with gdb.
- The `-g` option adds debugging information to your program.

		gcc -g -o hello hello.c
		
### Running a program with GDB

- To run a program with `gdb` type

		gdb progname
		(gdb)

- Then set a breakpoint in the main function

		(gdb) break main
		
- A breakpoint is a marker in your program to tell the porgram to stop and return control back to `gdb`

### Stepping through your program

- Your porgram will start running and when it reaches `main()` it will stop.

		gdb>
		
- Now you have the folloiwing commands to run your program step by step:
	+ Run the next line of code and stop, it will enter into a function

			gdb step
			
	+ Run the next line of code and stop, do not go into function
	
			gdb next
			
### Printing the Value of a Variable

- This command prints a variable

		(gdb) print var

## February 13th, 2013 - Lecture

### Binary Numbers

- base 2, each digit is 0 or 1
- Numbers are written as \\( d_n, ..., d_2, d_1, d_0 \\)
- Value of number is computer as 
\\[ \sum_{i = 0}^n d_i \times 2^i \\]

### Hexadecimal numbers

- Base 16
- Each digit c an be one of 16 different valyes
	+ Symbols = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F}
- Value
\\[ \sum_{i = 0}^n d_i \times 16^i \\]

### Octal numbers

- Little more awkward
- Same basic idea, except power of 8
- Grabbing 3 bits at a time
- Value = 

\\[ \sum_{i = 0}^n d_i \times 8^i \\]

### Converting hex to binary

- Each hexademical digit can be represented by 4 binary digits
- What is `0o45` in binary?
	1. 0b01000101
	2. 0b100101
	3. 0b010010
- What is the general rule for conversion?

> Real programmers use hex

### Converting binary to hex

- Grab 4 bits at a time, change to corresponding digit in hex
- Go from right to left
- Example: `1011011110011100`

		0b1011011110011100 = 0xb79
		
### Decimal to binary

- What is the largest power of 2, q, r... such that
	\\[ n = 2^p + r_1 \\] where \\(r_1 \le 2^p \\)
	\\[n - 2^p = 2^q + r_2\\] where \\(*r_2 \le 2^q \\)
	\\[ n - (2^p + 2^q) = 2^r + r_3\\] where \\(r_3 < r^r\\)
	
### Decimal and binary fractions

- In decimal, digits to the right of radix point have value \\(\frac{1}{10}^i\\) for each digit in the \\(i^{th}\\) place
	+ 0.25 is 2/10 + 5/100
- Similarly, ib binary, digits to the right of radix point have value \\(1/2^i\\) for each ith place
	+ Just the base is different

### Data sizes

		C			32		64
		char		1		1
		shot int	2		2
		int			4		4
		pointer		4		8
		
### Big endian vs. small endian

- How toi determine value when have a sbinary number spread across multiple bytes

		A0 BC 00 12
		
	+ Is this `A0BC0012` or `1200BCA0`
		* One is called little endian and the other is called big endian
		* Makes no difference to computer architecture
	+ Why do we care?
		* Interpret machine code and values
		* One computer sending data to another computer
		* Need to convert to standard before transmitting

- **Big endian**: MSB first, decreasing numeric significiance as byte address increases
- **Little endian**: LSB first, increasing numeric significane as byte address increase

### Representing integers

- How do we represent negative number in computers?
	+ You use a bit
- Signed magnitude
		
		0100 = 4
		0011 = 3
		1100 = -4
		1011 = -3
		
- Unsigned integers n bits
\\[0 ... 2^n - 1\\]

- Signed magnitude
\\[ 10000_{10} = 00002710\\]
\\[-10000_{10} = 80002710 \\]
\\[-2^{n-1} ... 2^{n-1} \\]

		00000000 = 0
		80000000 = 0
		
	+ This complicated the hardware because two representaitons equal the same thing.
- The complelemtn

		10000_{10} = 00002710
		-10000 = FFFFD8EF
		
- Two's complement

		00002710
		FFFFD8EF FLIP
		FFFFD8F0 ADD 1
		
		00000000
		FFFFFFFF FLIP
		00000000 ADD 1
		
- You are not required to nkow these numbers

		8 bits		-128 to +127
		16 bits		-32768 to +32767
		32 bits		-2147483648 to +2147483647
		
- Two's complement in n bits

	+ value
 	\\[-d_{n-1}2^{n-1} + \sum-{i=0}^{n-1}d_is^i\\]
	+ range
	 \\[ \left[ -2^{n-1}, 2^{n-1}-1\right]\\]

- Some math

\\[1000_{10} = 000003E8 = \\]
\\[0x2^{31} + 1000_{10} = 1000 \\]

\\[-1000_{10} = FFFFFC18\\]

### ASCII table

		DEC	OCT	HEX	BIN	Symbol	HTML Number	HTML Name	Description
		0	000	00	00000000	NUL	&#000;	 	Null char
		1	001	01	00000001	SOH	&#001;	 	Start of Heading
		2	002	02	00000010	STX	&#002;	 	Start of Text
		3	003	03	00000011	ETX	&#003;	 	End of Text
		4	004	04	00000100	EOT	&#004;	 	End of Transmission
		5	005	05	00000101	ENQ	&#005;	 	Enquiry
		6	006	06	00000110	ACK	&#006;	 	Acknowledgment
		7	007	07	00000111	BEL	&#007;	 	Bell
		8	010	08	00001000	 BS	&#008;	 	Back Space
		9	011	09	00001001	 HT	&#009;	 	Horizontal Tab
		10	012	0A	00001010	 LF	&#010;	 	Line Feed
		11	013	0B	00001011	 VT	&#011;	 	Vertical Tab
		12	014	0C	00001100	 FF	&#012;	 	Form Feed
		13	015	0D	00001101	 CR	&#013;	 	Carriage Return
		14	016	0E	00001110	 SO	&#014;	 	Shift Out / X-On
		15	017	0F	00001111	 SI	&#015;	 	Shift In / X-Off
		16	020	10	00010000	DLE	&#016;	 	Data Line Escape
		17	021	11	00010001	DC1	&#017;	 	Device Control 1 (oft. XON)
		18	022	12	00010010	DC2	&#018;	 	Device Control 2
		19	023	13	00010011	DC3	&#019;	 	Device Control 3 (oft. XOFF)
		20	024	14	00010100	DC4	&#020;	 	Device Control 4
		21	025	15	00010101	NAK	&#021;	 	Negative Acknowledgement
		22	026	16	00010110	SYN	&#022;	 	Synchronous Idle
		23	027	17	00010111	ETB	&#023;	 	End of Transmit Block
		24	030	18	00011000	CAN	&#024;	 	Cancel
		25	031	19	00011001	 EM	&#025;	 	End of Medium
		26	032	1A	00011010	SUB	&#026;	 	Substitute
		27	033	1B	00011011	ESC	&#027;	 	Escape
		28	034	1C	00011100	 FS	&#028;	 	File Separator
		29	035	1D	00011101	 GS	&#029;	 	Group Separator
		30	036	1E	00011110	 RS	&#030;	 	Record Separator
		31	037	1F	00011111	 US	&#031;	 	Unit Separator

### Code

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

### IEEE floating point standard

- Most computer follow IEEE 754 standard
	+ Single precision
		* 32 bits
		* 1 bit for sign, 8 bits for exponent, 23 bits for mintissa
		* Has two zeroes
	+ Double precision 
		* 64 bits
	+ Extended precision 
		* 80 bits
		
## February 12th, 2013 - [Singly Linked List Implementation](http://www.cprogramming.com/snippets/source-code/singly-linked-list-insert-remove-add-count)

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
		
## February 12th, 2013 - Programming Assignment 2: Data Representation and Computer Arithmetic

### Introduction

This assignment is designed to help you learn the representation, interpretation, and manipulation of data as bits. There are two parts. In the first part, you will implement a program calc to add and subtract numbers specified in different bases (multiplication is extra credit). In the second part, you will implement a program format that will print the decimal values of bit sequences representing integer and floating point data types.

### Numeric Base Conversion and Calculator

Implement a program called calc with the following usage interface:

		calc <op> <number1> <number2> <output base>

The first argument, `<op>`, is either the string `+`, for addition, or `-`, for subtraction. If you want to implement multiplication, then `<op>` can also be the string `*`. (If you do implement multiplication, make sure to say so in your readme.pdf file so that the TAs know to check your program for this functionality.)
The next two arguments, `<number1>` and `<number2>` are integers of arbitrary size. Each of these numbers will be given in the form of:

\\[ −?(b|o|d|x)d_n d_{n−1} ...d_1 d_0 \\]

which can be interpreted as: a number can optionally start with a `−` sign, followed by a base indicator, where `b` means the number is a binary number, `o` means octal, `d` means decimal, and `x` means hexadecimal. \\(d_nd_{n−1}...d_1d_0 \\) are the digits of the number.
The final argument, `<output base>`, gives the base that the resulting number should be printed out in. Like the base indicator for the input numbers, this argument can be one of four strings: `b` for binary, `o` for octal, `d` for decimal, and `h` for hexadecimal. Your program should output the answer in the same form as the input numbers (that is, the output number should follow the regular expression given above).
Some examples:

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

Note that the numbers in the first example are too large to fit in a 32-bit integer type in C; this is why the arbitrary size is emphasized above. Using a 64-bit integer type is not the solution since the input integers can be arbitrarily large. Rather, you need to design data structures and algorithms that can handle arbitrarily large numbers. Assignment update: any decimal number that we ask you to handle—either an input decimal number or output in decimal format—will be less than a 32-bit integer.
Important: You must write the base conversion code yourself. You may not use type-casting, libraries, or output formats in printf(). You may use standard C arithmetic operations. You may use the C standard libraries for functionality not related to the conversion (e.g., string handling functions).
Important: If calc detects an error in the inputs, it should print out an error message that starts with the string “ERROR”, followed by a string that gives an informative message about the error that it detected.

### Format Interpretation

Implement a program called format with the following usage interface: format `<input bit sequence> <type>`
The first argument, `<input bit sequence>`, is a sequence of 32 bits. Remember that your C program will get it as a string of 1 and 0 characters in the `argv[1]` argument to main. This sequence of bits represents the binary values stored in 4 contiguous bytes in memory. The leftmost bits are stored in the byte with the smallest address while the rightmost bits are stored in the byte with the largest address.
The second argument, `<type>`, gives the type that you should use to interpret the input bit sequence, and can be either int (integer) or float.
The formats for the input bit sequence is as follows. If the type is: int: the format is two’s complement;
float: the format is IEEE 74 single precision;
Note that the input bit sequence can correspond to negative numbers.

Your program should print out the decimal representation of the input bit sequence, assuming a big endian byte ordering. Floating point numbers should be printed in scientific notation, where a number 1.5x105 would be printed as 1.5e5. For positive infinity, output pinf, for negative infinity, output ninf, and for “NaN”, output NaN.
Here are some examples:

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

Important: You must write the interpretation code yourself. You may not use type-casting, libraries, or output formats in printf(). You may use standard C arithmetic operations. You may use the C standard libraries for functionality not related to the value interpretation (e.g., string handling functions).
Important: If format detects an error in the inputs, it should print out an error message that starts with the string “ERROR”, followed by a string that gives an informative message about the error that it detected. For this program, you can assume that any input bit sequence that is shorter or longer than 32 bits is erroneous.

### Submission

You have to e-submit the assignment using Sakai. Your submission should be a tar file named pa2.tar that can be extracted using the command:

		tar xf pa2.tar

Your tar file must contain:
+ A sub-directory named calc. calc must contain:
	– readme.pdf: this file should describe your design and implementation of the calc pro- gram. In particular, it should detail your design, any design/implementation challenges that you ran into, and an analysis (e.g., big-O analysis) of the space and time perfor- mance of your program.
	– Makefile: there should be at least two rules in this Makefile: calc build your calc executable.
	clean prepare for rebuilding from scratch.
	– source code: all source code files necessary for building calc. At a minimum, this should
	include two files, calc.h and calc.c.
+ A sub-directory named format. format must contain:
	– readme.pdf: this file should describe your design and implementation for the format program. In particular, it should detail your design, any design/implementation chal- lenges that you ran into, and an analysis (e.g., big-O analysis) of the space and time performance of your program.
	– Makefile: there should be at least two rules in your Makefile: format build your format executable.
	clean prepare for rebuilding from scratch.
	– source code: all source code files necessary for building format. At minimum, this should
	include two files, format.h and format.c.
We will compile and test your program on the iLab machines so you should make sure that your program compiles and runs correctly on these machines. You must compile all C code using the gcc compiler with the -ansi -pedantic -Wall flags.

### Grading Guidelines

#### Functionality

This is a large class so that necessarily the most significant part of your grade will be based on programmatic checking of your program. That is, we will build a binary using the Makefile and source code that you submitted, and then test the binary for correct functionality against a set of inputs. Thus:
	+ You should make sure that we can build your program by just running make.
	+ You should test your code as thoroughly as you can. In particular, your code should be adept
at handling exceptional cases.
Be careful to follow all instructions. If something doesn’t seem right, ask.

#### Design

Having said the above about functionality, design is a critical part of any programming exercise. In particular, we expect you to write reasonably efficient code based on reasonably performing algorithms and data structures. More importantly, you need to understand the performance (time & space) implications of the algorithms and data structures you chose to use. Thus, the explanation of your design and analyses in the readme.pdf will comprise a non-trivial part of your grade. Give careful thoughts to your writing of this file, rather than writing whatever comes to your mind in the last few minutes before the assignment is due.

#### Coding Style

Finally, it is important that you write “good” code. Unfortunately, we won’t be able to look at your code as closely as we would like to give you good feedback. Nevertheless, a part of your grade will depend on the quality of your code. Here are some guidelines for what we consider to be good:
- Your code is modularized. That is, your code is split into pieces that make sense, where the pieces are neither too small nor too big.
- Your code is well documented with comments. This does not mean that you should comment every line of code. Common practice is to document each function (the parameters it takes as input, the results produced, any side-effects, and the function’s functionality) and add comments in the code where it will help another programmer figure out what is going on.
- You use variable names that have some meaning (rather than cryptic names like i). Further, you should observe the following protocols to make it easier for us to look at your code:
- Define prototypes for all functions.
- Place all prototype, typedef, and struct definitions in header (.h) files. • Error and warning messages should be printed to stderr using fprintf.

## February 13th, 2013 - Office hours

- Exceptions are bad.
- `strcasecmp` is fine.
- A buffer of 128 bytes is fine.