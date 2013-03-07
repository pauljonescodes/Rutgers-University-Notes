Calc and Format Readme
======================

Calc
----

### Design and Implementation

- My design uses a string as the primary data structure.
- When numbers are inputted, no matter what the are, they go through this process:
    1. Parse their "metadata" - length, are the negative, base;
    2. Send their string to the relevant helper function to conversion, which convert it to binary;
    3. Decide based on metadata how to add or use two's complement subtraction;
    4. Based on the requested output format, send the string to the relevant helper function for conversion;
    5. Print.
- I picked this because I believe that linked list are too difficult to traverse, data types have to little room (and are against spec), and it isn't really sensible to talk about hash tables or trees in this context.
- This ended up being a good method for binary, octal, and hexadecimal addition and manipulation, but very poor for decimal.

### Challenges

- Time became a huge concern. I wrote one implementation using integers after that was given the okay,
but having learned that this would not receive full credit I set about on the more ambitious route.
    - Ultimate I think this will lower my grade, but I learned enough along the way to justify the expense.
    - I think this is a good investment because it will serve me better in the future and on exams.
    - I did not get `format` done for this reason.
- Decimal is a terrible number system for computers, or at very least how computers operate presently.
    - I could not find an algorith to go to or from binary and decimal that could handle arbitrily large input.

### Analysis

#### Space

- The space is linearly related to the input.
- The only space that is allocated is for three strings: input one, input two, and output.
- The results in a space complexity $2n$ in the worst case, if input makes for a long binary string.

$$O(n)$$

#### Time

- Small and linear operations are performed while processing.
- Parsing as an activity rarely leads to anything other than linear.
    - In processing, there are no nested for loops or anything that would make it exponential, quadratic.
    
$$O(n)$$

### Test cases

#### Conversions to binary

Conversions to binary have been flawless in every tested case. The family
of functions which do the conversion are rigorous and basic. My internal
representation of *every* number is a binary string, so these functions
are core to my functionality.

    char * oct_to_bin (char * oct);
    char * dec_to_bin (char * dec);
    char * hex_to_bin (char * hex);
Now for some examples!

##### Binary

    Inputted    111111111111111111111111111111111
    Expected    111111111111111111111111111111111
    Actually    111111111111111111111111111111111
    
    Note: MAX_INT

Binary is successful 100% of the time because I'm being
fed a binary string representation and my internal
representation is a string. Granted that the computer
does not run out of memory and I parsed my input correctly,
this will never, ever break.

##### Octal
    
    Inputted    7654321
    Expected    111110101100011010001
    Actually    111110101100011010001
    
The conversion algorithm that I used to convert
octal to my internal binary string representation is "grabbing" 1 
binary bit at a time in input and 3 bits at a time on output.

This approach has yielded a 100% success rate so far, the only
ever failure is when it is fed bad input. GIGO.

##### Decimal

    Inputted    987654321
    Expected    111010110111100110100010110001
    Actually    111010110111100110100010110001
    
While this superficially seems to work, it has a dark secret.
It uses `atoi` and an `int` to do the conversion.
As with output, I could not find or invent an algorithm to consistenly
convert decimal to binary or the other way around. 

If decimal is selected as an option on either input or output,
then arbitrarily large numbers are not possible.    

##### Hexademical

    Inputted    FEDCBA987654321
    Expected    111111101101110010111010100110000111011001010100001100100001
    Actually    111111101101110010111010100110000111011001010100001100100001
    
    Note: more that 32 bit
    
Hexadecimal is performed the same as octal, for both input and output,
except I "grab" 4 bits at a time on output.

#### Addition

Addition is admittedly more flawed. Let's explore some test cases and then discuss them.

##### Binary

    Inputted    ./calc + d1111111 d1111111 b
    Expected    b1000011110100010001110
    Actually    b1000011110100010001110
    
    SUCCESS
    
##### Octal

    Inputted    ./calc + d1111111 d1111111 o
    Expected    o10364216
    Actually    o10364216
    
    SUCCESS
    
##### Decimal
    
    Inputted    ./calc + d1111111 d1111111 d
    Expected    d2222222
    Actually    d2222222.0000001000011110100010@<
    
    FAILURE 
    
This failure is a product of a limitation of my program.
I was unable to devise a consistent algorithm to convert
my binary representation of the inputted values (which have
always been correct) to a decimal representation for the user.

The problem is a hard one because unlike octal and hexadecimal,
decimal does not take an even number of bits to each digit.

##### Hex

    Inputted    ./calc + d1111111 d1111111 h
    Expected    h21E88E
    Actually    h21E88E
    
    SUCCESS
    
##### A bigger number
    
    Inputted    ./calc + d11111111 d11111111 h
    Expected    h153158E
    Actually    h155158E
    
    FAILURE 
    
Over a certain point, addition itself begins to break.
I've been unable to determine the reason.

#### Subtraction and negatives

Subtract and negative have been put into the same section because they
both use the same process - two's complement. Based on the most significant
bit and the length of the binary representation of input, I determine
which number has a greater absolute value. Then I decided how to perform
two's complement and whether the number should be negative. 