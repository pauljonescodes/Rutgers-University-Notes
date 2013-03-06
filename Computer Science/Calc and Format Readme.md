Calc and Format Readme
======================

Calc
----

### Test cases

#### Conversions to binary

##### Binary

        Inputted    111111111111111111111111111111111
        Expected    111111111111111111111111111111111
        Actually    111111111111111111111111111111111
        
        Note: MAX_INT

##### Octal
    
        Inputted    7654321
        Expected    111110101100011010001
        Actually    111110101100011010001

##### Decimal

        Inputted    987654321
        Expected    111010110111100110100010110001
        Actually    111010110111100110100010110001
        
##### Hexademical

        Inputted    FEDCBA987654321
        Expected    111111101101110010111010100110000111011001010100001100100001
        Actually    111111101101110010111010100110000111011001010100001100100001
        
        Note: more that 32 bit

#### Conversions from binary

#### Addition

                    Binary
        Inputted    1 + 1
        Expected    10
        Actually    10
        
                    Octal
        Inputted    FEDCBA + ABCDEF
        Expected    1101010101010101010101001 (binary)
        Actually    1101010101010101010101001
        
                    Decimal
        Inputted    255 + 255
        Expected    111111110 (binary)
        Actually    111111110
        
        
Format
------