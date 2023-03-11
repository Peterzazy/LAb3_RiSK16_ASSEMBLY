# LAb3_RiSK16_ASSEMBLY
-)Code for 8 instructions idea  : 
This code implements four tests to check if one number is less than, greater than, less than or equal to, or greater than or equal to another number.
The code starts by initializing eight registers (R1 through R8) with different values for testing. Then, for each test case, it loads the values of a and b into the appropriate registers (R4 and R5, respectively).
To perform the "less than" test, the code uses the NAND (not-and) instruction to compute the bitwise negation of the logical AND of a and b. If a is less than b, then a & b will not be equal to b, 
so the result of the NAND operation will not be zero, causing the code to branch to the 
"incorrect result" label and set R1 to 1. If a is greater than or equal to b, 
then a & b will be equal to b, so the result of the NAND operation will be zero, causing the code to continue to the HALT instruction.

The "greater than" test is similar to the "less than" test, but the operands to the NAND operation are swapped, so the result of the test is inverted.
The "less than or equal to" test is also similar to the "less than" test, but the operands to the NAND operation are swapped, so the result of the test is inverted.
The "greater than or equal to" test is also similar to the "greater than" test, but the operands to the NAND operation are swapped, so the result of the test is inverted.
Overall, the code is checking if a is less than, greater than, less than or equal to, or greater than or equal to b, and setting R1 to 1 if the test fails.

-)Code for operators with Special IS1
